### Apa yang akan kita pelajari???
  Topik:
  - Dasar Dasar Jaringan             
  - Amazon VPC (amazon virtual private cloud)
  - Jaringan VPC
  - Keamanan VPC
  - Amazon Route 53
  - Amazon CloudFront

### Dasar-Dasar Jaringan
   konsep jaringan dasar yang memberikan dasar yang diperlukan untuk pemahaman Anda 
   tentang layanan jaringan AWS, Amazon Virtual Private Cloud (Amazon VPC)

   **Jaringan komputer** adalah dua mesin klien atau lebih yang terhubung bersama-sama 
   untuk berbagi sumber daya. Sebuah jaringan dapat secara logis dipartisi menjadi subnet. 
   Jaringan memerlukan perangkat jaringan (seperti perute atau switch) untuk menghubungkan 
   semua klien bersama-sama dan memungkinkan komunikasi antarklien

![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/9012aedb-3117-4557-9d93-6bae4ec505f1)

Alamat IP 32 bit disebut sebagai alamat IPv4.Alamat IPv6, yang 128 bit, juga tersedia. Alamat IPv6 dapat menampung lebih banyak perangkat pengguna.Alamat IPv6 terdiri dari delapan grup empat huruf dan angka yang dipisahkan oleh titik dua (:)
Total gabungan dari delapan grup untuk alamat IPv6 adalah 128 bit dalam format biner

> Metode umum untuk mendeskripsikan jaringan
  Classless Inter-Domain Routing (CIDR). Alamat CIDR dinyatakan sebagai berikut:
  - Alamat IP (yang merupakan alamat pertama jaringan)
  - karakter garis miring (/)
  - nomor yang memberitahu Anda berapa banyak bit awalan perutean yang harus 
    ditetapkan atau dialokasikan untuk pengidentifikasi jaringan

Bit yang tidak tetap diperbolehkan untuk berubah. CIDR adalah cara untuk mengekspresikan grup alamat IP yang berturut-turut satu sama lain

### Amazon VPC

![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/cf58c2cd-e7de-4bfc-9eea-17c008ef6bf5)
> Amazon Virtual Private cloud (Amazon VPC) 

  adalah layanan yang memungkinkan anda menyediakan bagian yang terisolasi secara logis 
  dari AWS cloud, tempat meluncurkan sumber daya AWS.

  Amazon VPC memberikan kontrol atas sumber daya jaringan virtual, termasuk pilihan 
  rentang alamat IP, pembuatan subnet, serta konfigurasi tabel rute, dan gateway jaringan.

> VPC & SUBNET
  - VPC
    - terisolasi secara logis dari VPS lain
    - didedikasikan untuk akun AWS
    - bagian dari satu wilayah AWS dan dapat menjangkau beberapa Availability Zone
  
  - SUBNET
    - rentang alamat IP yang membagi VPC
    - bagian dari satu Availability Zone
    - diklasifikasikan sebagai publik atau privat

> pemberian alamat IP

  Alamat IP memungkinkan sumber daya di VPC Anda berkomunikasi satu sama lain dan dengan 
  sumber daya melalui internet. Ketika Anda membuat VPC, Anda menetapkan blok CIDR IPv4 
  (rentang alamat IPv4 privat) untuk VPC tersebut

> alamat IP yang dicadangkan

  Saat membuat subnet, subnet tersebut memerlukan blok CIDR-nya sendiri. Untuk setiap 
  blok CIDR yang Anda tentukan, AWS mencadangkan lima alamat IP dalam blok tersebut, dan 
  alamat ini tidak tersedia untuk digunakan. AWS mencadangkan alamat IP ini untuk:
  - Alamat jaringan
  - Perute lokal VPC (komunikasi internal)
  - Resolusi Domain Name System (DNS)
  - Penggunaan di masa mendatang
  - Alamat siaran jaringan

> jenis alamat IP publik
  - alamat IP Publik
    - ditetapkan secara manual melalui alamat IP Elastis
    - ditetapkan secara otomatis melalui pengaturan penetapan alamat IP publik otomatis di
      tingkat subnet

  - alamat IP elastis
    - berkaitan dengan akun AWS
    - dapat dialokasikan dan dipetakan ulang kapan saja
    - biaya tambahan mungkin berlaku

Alamat IP Elastisadalah alamat IPv4 publik dan statis yang dirancang untuk komputasi cloud dinamis.Anda dapat mengaitkan alamat IP Elastis dengan antarmuka instans atau jaringan apa pun untuk VPC apa pun dalam akun Anda

> Tabel rute dan rute

  Tabel rute berisi sekumpulan aturan (disebutrute)yang mengarahkan lalu lintas jaringan 
  dari subnet Anda. Setiap rute menentukan tujuandan target. Tujuan adalah blok CIDR 
  tujuan tempat Anda ingin mengarahkan lalu lintas dari subnet

  Target adalah target yang dilalui lalu lintas tujuan.Secara default, setiap rute tabel yang Anda 
  buat berisi rute lokal untuk komunikasi di VPC. Anda dapat menyesuaikan tabel rute dengan 
  menambahkan rute. Anda tidak dapat menghapus entri rute lokal yang digunakan untuk komunikasi 
  internal
  
### Jaringan VPC

> Gateway Internet

**gateway internet** adalah komponen VPC yang dapat diskalakan, redundan, dan tersedia dengan sangat baik yang memungkinkan komunikasi antara instans di VPC dan internet Anda. Gateway internet memiliki dua tujuan: untuk memberikan target dalam tabel rute VPC Anda untuk lalu lintas yang dapat dirutekan internet, dan untuk melakukan penerjemahan alamat jaringan untuk instans yang telah ditetapkan alamat IPv4 publik

Untuk membuat subnet publik, Anda melampirkan gateway internet ke VPC Anda dan menambahkan rute ke tabel rute untuk mengirim lalu lintas non-lokal melalui gateway internet ke internet (0.0.0.0/0)

> Gateway network address translation (NAT)

**Gateway network address translation (NAT)**  memungkinkan instans dalam subnet privat untuk terhubung ke internet atau layanan AWS lainnya, tetapi mencegah internet untuk memulai koneksi dengan instans

Untuk membuat gateway NAT, Anda harus menentukan subnet publik di mana gateway NAT seharusnya berada. Anda juga harus menentukan alamat IP Elastis untuk mengaitkannya dengan gateway NAT saat Anda membuatnya. Setelah Anda membuat gateway NAT, Anda harus memperbarui tabel rute yang terkait dengan satu atau lebih subnet privat Anda untuk mengarahkan lalu lintas yang terikat internet ke gateway NAT. Dengan demikian, instans di subnet privat Anda dapat berkomunikasi dengan internet

> Berbagi VPC

**Berbagi VPC** memungkinkan pelanggan berbagi subnet dengan akun AWS lainnya dalam organisasi yang sama di AWS Organizations. Berbagi VPC memungkinkan beberapa akun AWS untuk membuat sumber daya aplikasi. Berbagi VPC memungkinkan Anda memisahkan akun dan jaringan. Anda memiliki VPC yang lebih sedikit, lebih besar, dan dikelola secara terpusat

> Peering VPC

Koneksi peering VPC adalah koneksi jaringan antara dua VPC yang memungkinkan Anda merutekan lalu lintas di antaranya secara privat.Instans di masing-masing VPC dapat berkomunikasi dengan satu sama lain seakan-akan berada dalam jaringan yang sama. Anda dapat membuat koneksi peering VPC antar VPC Anda sendiri, dengan VPC di akun AWS yang lain, atau dengan VPC di wilayah AWS yang berbeda

Peering VPC memiliki beberapa batasan:
- Rentang alamat IP tidak dapat tumpang tindih
- Peering transitif tidak didukung. Misalnya, Anda memiliki tiga VPC: A, B, dan C. VPC A terhubung ke VPC B, dan VPC A terhubung ke VPC C. Namun, VPC B tidakterhubung ke VPC C secara implisit. Untuk menghubungkan VPC B ke VPC C, Anda harus secara eksplisit menetapkan konektivitas tersebut.
- Anda hanya dapat memiliki satu sumber daya peering antara dua VPC yang sama

> VPN AWS Site-to-Site

instans yang Anda luncurkan ke VPC tidak dapat berkomunikasi dengan jaringan jarak jauh. Untuk menghubungkan VPC Anda ke jaringan jarak jauh Anda (yaitu, membuat jaringan pribadi virtual atau koneksi VPN), Anda:
- Buat perangkat gateway virtual baru (disebut gateway virtual private network (VPN)) dan 
  lampirkan ke VPC Anda.
- Tentukan konfigurasi perangkat VPN atau customer gateway. Customer gateway bukan perangkat 
  tetapi sumber daya AWS yang menyediakan informasi untuk AWS tentang perangkat VPN Anda.
- Membuat tabel rute kustom untuk mengarahkan lalu lintas yang terikat pusat data perusahaan ke 
  gateway VPN. Anda juga harus memperbarui aturan grup keamanan. (Anda akan belajar tentang grup 
  keamanan di bagian berikutnya.)
- Membangun koneksi AWS Site-to-Site VPN (Site-to-Site VPN) untuk menghubungkan dua sistem 
  tersebut.
- Konfigurasikan perutean untuk melewati lalu lintas melalui koneksi.

  > AWS Direct Connect

Salah satu tantangan komunikasi jaringan adalah kinerja jaringan. Kinerja dapat terpengaruh secara negatif jika pusat data Anda terletak jauh dari Wilayah AWS Anda. Untuk situasi seperti itu, AWS menawarkan AWS Direct Connect, atau DX. AWS Direct Connect memungkinkan Anda membuat koneksi jaringan pribadi khusus antarjaringan dan salah satu lokasi DX Anda. Koneksi pribadi ini dapat mengurangi biaya jaringan, meningkatkan throughput bandwidth, dan memberikan pengalaman jaringan yang lebih konsisten dibandingkan dengan koneksi berbasis Internet. DX menggunakan jaringan area lokal virtual (VLAN) 802.1q standar terbuka

> Endpoint VPC

Endpoint VPC adalah perangkat virtual yang memungkinkan Anda menghubungkan VPC ke layanan AWS yang didukung dan layanan endpoint VPC yang didukung oleh AWS PrivateLink. Koneksi ke layanan ini tidak memerlukan gateway internet, perangkat NAT, koneksi VPN, atau koneksi AWS Direct Connect. Instans dalam VPC Anda tidak memerlukan alamat IP publik untuk berkomunikasi dengan sumber daya dalam layanan. Lalu lintas antara VPC Anda dan layanan lainnya tidak meninggalkan jaringan Amazon

Ada dua jenis endpoint VPC:
- Endpoint VPC antarmuka(endpoint antarmuka) memungkinkan Anda terhubung ke layanan yang didukung oleh AWS PrivateLink.Layanan ini mencakup beberapa layanan AWS, layanan yang di-host oleh pelanggan AWS lainnya dan Partner AWS Partner Network (APN) di VPC mereka sendiri (disebut sebagai layanan endpoint), dan layanan AWS Marketplace APN Partner yang didukung. Pemilik layanan adalah penyedia layanan, dan Anda—sebagai pelaku utama yang membuat endpoint antarmuka—adalah konsumen layanan. Anda dikenakan biaya untuk membuat dan menggunakan endpoint antarmuka untuk layanan. Tarif penggunaan per jam dan tarif pemrosesan data berlaku. Lihat Dokumentasi AWS untuk daftar endpoint antarmukayang didukung.
- Endpoint gateway: Penggunaan endpoint gateway tidak dikenakan biaya tambahan. Biaya standar untuk transfer data dan penggunaan sumber daya berlaku

> AWS Transit Gateway

Opsi dan gateway ini termasuk AWS Direct Connect (melalui gateway DX), gateway NAT, gateway internet, peering VPC, dll Menemukan pelanggan AWS dengan ratusan VPC yang didistribusikan di seluruh akun dan Wilayah AWS untuk melayani beberapa lini bisnis, tim, proyek, dan sebagainya adalah hal yang biasa. Hal-hal menjadi lebih kompleks ketika pelanggan mulai menyiapkan konektivitas antara VPC mereka. Semua opsi konektivitas benar-benar point-to-point, sehingga jumlah koneksi VPC-ke-VPC dapat tumbuh dengan cepat. Ketika jumlah beban kerja yang berjalan di AWS tumbuh, Anda harus dapat menskalakan jaringan Anda di beberapa akun dan VPC untuk mengikuti pertumbuhan tersebut

Meskipun Anda dapat menggunakan peering VPC untuk menghubungkan pasangan VPC, mengelola konektivitas point-to-point di banyak VPC tanpa kemampuan untuk mengelola kebijakan konektivitas secara terpusat bisa jadi mahal dan sulit secara operasional. Untuk konektivitas on-premise, Anda harus melampirkan VPN ke setiap VPC individu. Pembangunan solusi ini dapat memakan waktu dan sulit dikelola ketika jumlah VPC tumbuh menjadi ratusan

### Keamanan VPC

> Grup Keamanan

**Grup keamanan** bertindak sebagai firewall virtual bagi instans, serta mengontrol lalu lintas masuk dan keluar.Grup keamanan bertindak pada tingkat instans, bukan tingkat subnet. Oleh karena itu, setiap instans di subnet di VPC Anda dapat ditetapkan ke rangkaian grup keamanan yang berbeda

**Grup keamanan** memiliki aturanyang mengontrol lalu lintas masuk dan keluar. Saat Anda membuat grup keamanan, grup tersebut tidak memiliki aturan masuk. Oleh karena itu, tidak ada lalu lintas masuk yang berasal dari host lainnya ke instans Anda yang diizinkan, hingga Anda menambahkan aturan masuk ke grup keamanan. Secara default, grup keamanan mencakup aturan keluar yang mengizinkan semua lalu lintas keluar. Anda dapat menghapus aturan dan menambahkan aturan keluar yang hanya mengizinkan lalu lintas keluar tertentu saja. Jika grup keamanan Anda tidak memiliki aturan keluar, lalu lintas keluar yang bersumber dari instans Anda tidak ada yang diizinkan

>Access control list jaringan (ACL jaringan)

**Access control list jaringan (ACL jaringan)**adalah lapis keamanan opsional untuk Amazon VPC Anda.Ini bertindak sebagai firewall untuk mengendalikan lalu lintas masuk dan keluar dari satu subnet atau lebih.Untuk menambahkan lapis keamanan lain ke VPC, Anda dapat mengatur ACL jaringan dengan aturan yang mirip dengan grup keamanan Anda.

Setiap subnet di VPC Anda harus dikaitkan dengan ACL jaringan. Jika Anda tidak mengaitkan subnet dengan ACL jaringan secara eksplisit, subnet dikaitkan dengan ACL jaringan default secara otomatis. Anda dapat mengaitkan ACL jaringan dengan beberapa subnet; namun, subnet dapat dikaitkan hanya dengan satu ACL jaringan pada satu waktu. Ketika Anda mengaitkan ACL jaringan dengan subnet, asosiasi sebelumnya akan dihapus

> Grup keamamn versus ACL jaringan

Berikut adalah ringkasan dari perbedaan antara grup keamanan dan ACL jaringan:
- Grup keamananbertindak pada tingkat instans, tetapi ACL jaringan bertindak pada tingkat subnet
- Grup keamanan hanya mendukung aturan izinkan, namun ACL jaringan mendukung aturan izinkan dan 
  tolak
- Grup keamanan bersifat stateful, tetapi ACL jaringan adalah stateless.•Untuk grup keamanan, 
  semua aturan dievaluasi sebelum keputusan dibuat untuk mengizinkan lalu lintas. Untuk ACL 
  jaringan , aturan dievaluasi dalam urutan nomor sebelum keputusan dibuat untuk mengizinkan lalu 
  lintas

 ### Amazon Route 53

Amazon Route 53 adalah layanan web Domain Name System (DNS) cloud dengan ketersediaan tinggi dan dapat diskalakan. Amazon Route 53 dirancang untuk memberikan cara yang andal dan hemat biaya pada developer dan bisnis untuk merutekan pengguna ke aplikasi internet dengan menerjemahkan nama (seperti www.example.com) ke alamat IP numerik (seperti 192.0.2.1) yang digunakan komputer untuk terhubung satu sama lain. Selain itu, Amazon Route 53 sepenuhnya sesuai dengan IPv6

Amazon Route 53 menghubungkan permintaan pengguna secara efektif ke infrastruktur yang menjalankan AWS—seperti Amazon EC2 instance, load balancer Elastic Load Balancing, atau bucket Amazon S3—dan juga dapat digunakan untuk merutekan pengguna ke infrastruktur di luar AWS

> Resolusi DNS Amazon Route 53

Amazon Route 53 mendukung beberapa jenis kebijakan perutean, yang menentukan bagaimana Amazon Route 53 merespons kueri:
- Perutean sederhana (round robin)–Gunakan untuk sumber daya tunggal yang menjalankan fungsi 
  tertentu untuk domain Anda (seperti server web yang menyajikan konten untuk situs web 
  example.com)
- Perutean weighted round robin –Gunakan untuk merutekan lalu lintas ke beberapa sumber daya dalam 
  proporsi yang Anda tentukan. Memungkinkan Anda menetapkan beban ke serangkaian catatan sumber 
  daya untuk menentukan dengan frekuensi mana respons yang berbeda dilayani. Anda mungkin ingin 
  menggunakan kemampuan ini untuk melakukan pengujian A/B, yaitu ketika Anda mengirim sebagian 
  kecil lalu lintas ke server tempat Anda membuat perubahan perangkat lunak. 
- Perutean Latensi (LBR) -Gunakan ketika Anda memiliki sumber daya di beberapa Wilayah AWS dan 
  Anda ingin merutekan lalu lintas ke Wilayah yang menyediakan latensi terbaik. Perutean latensi 
  bekerja dengan merutekan pelanggan Anda ke endpoint AWS (misalnya, Amazon EC2 instance, alamat 
  IP Elastis,atau load balancer) yang memberikan pengalaman tercepat berdasarkan pengukuran 
  kinerja aktual dari Wilayah AWS yang berbeda tempat aplikasi Anda berjalan
- Perutean geolokasi–Gunakan saat Anda ingin merutekan lalu lintas berdasarkan lokasi pengguna 
  Anda. Saat Anda menggunakan perutean geolokasi, Anda dapat melokalkan konten dan menyajikan 
  beberapa bagian situs web dalam bahasa pengguna. 
- Perutean kedekatan geografis–Gunakan saat Anda ingin merutekan lalu lintas berdasarkan lokasi 
  sumber daya Anda dan, secara opsional, mengalihkan lalu lintas dari sumber daya di satu lokasi 
  ke sumber daya di lokasi lain
- Perutean failover (failover DNS) —Gunakan saat Anda ingin 
  mengonfigurasi failover aktif-pasif. Amazon Route 53 dapat membantu mendeteksi pemadaman situs 
  web dan mengalihkan pengguna ke lokasi alternatif tempat aplikasi Anda beroperasi dengan baik. 
  Saat Anda mengaktifkan fitur ini, agen pemeriksaan kesehatan Amazon Route 53 akan memantau 
  setiap lokasi atau endpoint aplikasi untuk menentukan ketersediaannya. Anda dapat memanfaatkan 
  fitur ini untuk meningkatkan ketersediaan aplikasi untuk pelanggan Anda
- Perutean jawaban multinilai—Gunakan jika Anda ingin Route 53 merespons kueri DNS dengan hingga 
  delapan catatan baik yang dipilih secara acak. Anda dapat mengonfigurasi Amazon Route 53 untuk 
  mengembalikan beberapa nilai—seperti alamat IP untuk server web Anda—sebagai respons dari kueri 
  DNS.
  
> Deployment Multiwilayah

  Deployment Multiwilayah adalah kasus penggunaan contoh untuk Amazon Route 53. Dengan Amazon 
  Route 53, pengguna secara otomatis diarahkan ke load balancerElastic Load Balancing yang paling 
  dekat dengan pengguna

  Manfaat Deployment Multiwilayah Route 53 meliputi:
  - Perutean berbasis latensi ke Wilayah
  - Perutean load balancer ke Availability Zone

> Failover DNS Amazon Route 53

  Amazon Route 53 memungkinkan Anda meningkatkan ketersediaan aplikasi Anda yang berjalan di AWS 
  dengan:
  - Mengonfigurasi skenario cadangan dan failover untuk aplikasi Anda sendiri
  - Memungkinkan arsitektur multi-Wilayah yang sangat tersedia di AWS
  - Membuat pemeriksaan kesehatan untuk memantau kesehatan dan kinerja aplikasi, server web, dan 
    sumber daya lainnya. Setiap pemeriksaan kesehatan yang Anda buat dapat memantau salah satu hal 
    berikut—kesehatan sumber daya tertentu, seperti server web; status pemeriksaan kesehatan 
    lainnya; dan status alarm Amazon CloudWatch

> Failover DNS untuk aplikasi web multitingkat

### Amazon CloudFront

> Penyampaian konten dan latensi jaringan

   Seperti yang dijelaskan sebelumnya dalam modul ini ketika Anda mempelajari AWS Direct Connect, 
  salah satu tantangan komunikasi jaringan adalah kinerja jaringan. Ketika Anda menjelajahi situs 
  web atau streaming video, permintaan Anda diarahkan melalui banyak jaringan yang berbeda untuk 
  menjangkau server asal

  Server asal (atau asal) menyimpan versi asli yang definitif dari objek (halaman web, gambar, dan 
  file media). Jumlah lompatan jaringan dan jarak yang harus ditempuh permintaan secara signifikan 
  memengaruhi kinerja dan responsivitas situs web. Selanjutnya, latensi jaringan berbeda di 
  berbagai lokasi geografis

> Jaringan penyampaian konten (CDN)

  Sebuah jaringan penyampaian konten (CDN) adalah sistem server pembuatan cache yang 
  didistribusikan secara global. CDN menyimpan salinan file yang biasa diminta dalam cache (konten   statis, seperti Hypertext Markup Language, atau HTML; Cascading Style Sheet, atau CSS; 
  JavaScript; dan file gambar) yang di-host di server asal aplikasi. CDN memberikan salinan lokal 
  dari konten yang diminta dari edge cache atau Point of Presence yang menyediakan pengiriman 
  tercepat untuk pemohon

> Amazon CloudFront

  Amazon CloudFront adalah layanan CDN cepat yang memberikan data, video, aplikasi, dan antarmuka 
  pemrograman aplikasi (API) dengan aman kepada pelanggan secara global dengan latensi rendah dan 
  kecepatan transfer yang tinggi. Hal Ini juga menyediakan lingkungan yang ramah developer

  Amazon CloudFront memberikan file ke pengguna melalui jaringan global edge location dan cache 
  edge Regional. Amazon CloudFront berbeda dari solusi penyampaian konten tradisional karena 
  memungkinkan Anda mendapatkan manfaat penyampaian konten kinerja tinggi dengan cepat tanpa 
  kontrak negosiasi, harga tinggi, atau biaya minimum. Seperti layanan AWS lainnya, Amazon 
  CloudFront adalah penawaran mandiri dengan harga bayar sesuai pemakaian

> Infrastruktur Amazon CloudFront

  Amazon CloudFront memberikan konten melalui jaringan pusat data di seluruh dunia yang disebut 
  edge location. Saat pengguna mengajukan permintaan konten yang Anda sajikan dengan CloudFront, 
  pengguna dirutekan ke edge location yang menyediakan latensi (atau penundaan waktu) terendah, 
  sehingga konten dikirimkan dengan kinerja terbaik. Edge location CloudFront dirancang untuk 
  menyajikan konten populer dengan cepat kepada pemirsa Anda

  ![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/f6c29e0a-680b-4f8a-a3ac-cea0ceabd3d4)

  Manfaat Amazon CloudFront
  - Cepat dan global
  - Keamanan di edge
  - Dapat diprogram sepenuhnya
  - Terintegrasi secara mendalam dengan AWS
  - Hemat Biaya

  Harga Amazon CloudFront
  Transfer data keluar
  - dikenai biaya untuk volume data yang ditransfer keluar dari edge location Amazon CloudFront ke 
    internet atau ke asal anda
  Permintaan HTTP(S)
  - dibebankan untuk jumlah permintaan HTTP(S)
  Permintaan pembatalan validasi
  - tidak ada biaa tambahan untuk 1.000 jalur pertama yang diminta untuk pembatalan validasi 
    setiap bulan
  SSL kustom IP khusus
  - 600 USD per bulan untuk tiap sertifikat SSL kustom yang diasosiasikan dengan satu atau lebih 
    distribusi CloudFront menggunakan IP khusus dari dukungan sertifikasi SSL 

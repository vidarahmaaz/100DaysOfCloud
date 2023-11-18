![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/66fb157e-e7c9-4b7c-bf1f-cdef0b49c4cf)

## KOMPUTASI

### apa yang akan kita pelajari?
    
topik:
- layanan komputasi
- Amazon EC2
- Amazon EC2 Cost Optimization
- layanan kontainer
- Pengantar AWS Lambda
- Pengantar AWS Elastic Beanstalk

### Tinjauan umum layanan komputasi

> Layanan Komputasi AWS

Berikut adalah ringkasan dari apa yang ditawarkan setiap layanan komputasi:
- Amazon Elastic Compute Cloud(Amazon EC2) menyediakan mesin virtual 
  yang ukurannya dapat diubah
- Amazon EC2 Auto Scaling mendukung ketersediaan aplikasi dengan 
  memungkinkan Anda menentukan kondisi yang secara otomatis akan 
  meluncurkan atau mengakhiri EC2 instance
- Amazon Elastic Container Registry(Amazon ECR) digunakan untuk 
  menyimpan dan mengambil image Docker
- Amazon Elastic Container Service (Amazon ECS)adalah layanan 
  orkestrasi kontainer yang mendukung Docker
- VMware cloud on AWSmemungkinkan Anda menyediakan cloud hybrid tanpa 
  perangkat keras kustom
- AWS Elastic Beanstalkmenyediakan cara sederhana untuk menjalankan 
  dan mengelola aplikasi web
- AWS Lambda adalah solusi komputasi nirserver. Anda cukup membayar 
  waktu komputasi yang digunakan
- Amazon Elastic Kubernetes Service (Amazon EKS) memungkinkan Anda 
  menjalankan Kubernetes terkelola di AWS
- Amazon Lightsail menyediakan layanan sederhana untuk membangun 
  aplikasi atau situs web
- AWS Batch menyediakan alat untuk menjalankan tugas batch pada 
  skala apa pun
- AWS Fargate menyediakan cara untuk menjalankan kontainer yang 
  mengurangi kebutuhan Anda untuk mengelola server atau kluster
  AWS Outposts menyediakan cara untuk menjalankan layanan AWS 
  pilihan di pusat data on-premise Anda
- AWS Serverless Application Repository menyediakan cara untuk 
  menemukan, men-deploy, dan memublikasikan aplikasi nirserver

> Kategori Layanan Komputasi

Anda dapat menganggap setiap layanan komputasi AWS sebagai salah satu bagian dari empat kategori besar: mesin virtual (VM) yang menyediakan infrastructure as a service (IaaS), nirserver, berbasis kontainer, dan platform as a service (PaaS)

Amazon EC2 menyediakan mesin virtual, dan Anda dapat menganggapnya sebagai infrastructure as a service (IaaS). Layanan IaaS memberikan fleksibilitas dan meninggalkan banyak tanggung jawab manajemen server untuk Anda. Anda memilih sistem operasinya, dan Anda juga yang memilih ukuran serta kemampuan sumber daya server yang diluncurkan. Bagi profesional IT yang memiliki pengalaman menggunakan komputasi on-premise, mesin virtual merupakan konsep yang tidak asing. Amazon EC2 adalah salah satu layanan AWS pertama, dan tetap menjadi salah satu layanan yang paling populer

AWS Lambda adalah platform komputasi tanpa administrasi. AWS Lambda memungkinkan Anda menjalankan kode tanpa menyediakan atau mengelola server. Anda cukup membayar waktu komputasi yang digunakan. Konsep teknologi nirserver ini relatif baru bagi banyak profesional IT. Namun, ini menjadi lebih populer karena mendukung arsitektur cloud-native, yang memungkinkan skalabilitas masif dengan biaya lebih rendah dibanding menjalankan server 24/7 untuk mendukung beban kerja yang sama

Layanan berbasis kontainer—termasuk Amazon Elastic Container Service, Amazon Elastic Kubernetes Service, AWS Fargate, dan Amazon Elastic Container

Registry—memungkinkan Anda menjalankan beberapa beban kerja pada sistem operasi tunggal (OS). Kontainer berputar lebih cepat daripada mesin virtual, sehingga lebih cepat tanggap. Popularitas solusi berbasis kontainer terus tumbuh

AWS Elastic Beanstalk menyediakan platform as a service (PaaS). Ini memfasilitasi deployment cepat aplikasi yang Anda buat dengan menyediakan semua layanan aplikasi yang Anda butuhkan. AWS mengelola OS, server aplikasi, dan komponen infrastruktur lainnya sehingga Anda dapat fokus mengembangkan kode aplikasi

### Amazon EC2
![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/4a00d990-91a7-4bfd-8beb-19828addc9f5)

Singkatan EC2 di Amazon EC2 adalah Elastic Compute Cloud:

- **Elastic** artinya Anda dapat dengan mudah menambah atau 
 mengurangi jumlah server yang dijalankan untuk mendukung aplikasi 
 secara otomatis, dan Anda juga dapat menambah atau mengurangi 
 ukuran server yang ada
- **Compute** mengacu pada alasan sebagian besar pengguna 
 menjalankan server, yaitu untuk meng-host aplikasi yang berjalan 
 atau memproses data—tindakan yang memerlukan sumber daya komputasi, 
 termasuk daya pemrosesan (CPU) dan memori (RAM)
- **Cloud** mengacu pada fakta bahwa EC2 instance yang Anda jalankan 
 di-host di cloud

Amazon EC2 menyediakan mesin virtual di cloud dan memberi Anda kontrol administratif penuh atas sistem operasi Windows atau Linux yang berjalan pada instans. Sebagian besar sistem operasi server didukung, termasuk: Windows 2008, 2012, 2016, dan 2019, Red Hat, SuSE, Ubuntu, dan Amazon Linux

Amazon Elastic Compute Cloud (Amazon EC2) menyediakan mesin virtual agar Anda dapat meng-host jenis aplikasi yang sama yang mungkin dijalankan pada server on-premise tradisional. Layanan ini menyediakan kapasitas komputasi yang aman dan ukurannya dapat diubah di cloud. EC2 instance dapat mendukung berbagai beban kerja. Penggunaan umum untuk EC2 instance termasuk, namun tidak terbatas pada:

- server aplikasi,
- server web,
- server basis data,
- server game,
- server email,
- server media,
- server katalog,
- server file,
- server komputasi,
- server proxy.

> meluncurkan Amazon EC2 instance

Pertama kali Anda meluncurkan Amazon EC2 instance, Anda mungkin akan menggunakan Wizard Peluncuran Instans AWS Management Console.

Adanya Wizard Peluncuran Instans mempermudah peluncuran instans. Contohnya, jika Anda memilih untuk menerima semua pengaturan default, Anda dapat melewati sebagian besar langkah-langkah yang disediakan oleh wizard dan meluncurkan EC2 instance hanya dalam enam klik.

> Pilih AMI

- Amazon Machine Image (AMI)
  - adalah template yang digunakan untuk membuat EC2 instance (yaitu 
    mesin virtual, VM, yang berjalan di AWS Cloud)
  - berisi sistem operasi Windows atau Linux
  - juga memiliki beberapa perangkat lunak pra-install
- Pilihan AMI
  - Quick Start : AMI Linux dan Windows yang disediakan oleh AWS
  - AMI Saya    : setiap AMI yang dibuat
  - AWS Marketplace : template yang dikonfigurasi dari pihak ketiga
  - AMI Komunitas   : AMI yang dibagikan oleh orang lain, gunakan 
                     secara hati-hati

  AMI berisi komponen berikut:
  - Templat untuk volume rootinstans.Volume root biasanya berisi 
    sistem operasi (OS) dan semua yang diinstal di OS itu (aplikasi, 
    library, dll.). Amazon EC2 menyalin templat ke volume root EC2 
    instance baru, lalu memulainya
  - Izin peluncuranyang mengontrol akun AWS mana yang dapat 
    menggunakan AMI
  - Pemetaan perangkat blokyang menentukan volume yang dilampirkan 
    ke instans (jika ada) ketika diluncurkan.

> Pilih tipe Instance

- pertimbangkan kasus penggunaan
  - bagaimana EC2 instance yang dibuat dan akan digunakan
- tipe instance yang dipilih menentukan:
  - memori (RAM)
  - daya pemrosesan (CPU)
  - ruang disk dan jenis disk (penyimpanan)
  - kinerja jaringan
- kategori tipe instance:
  - tujuan umum
  - dioptimalkan untuk komputasi
  - memori optimized
  - dioptimalkan untuk penyimpanan
  - accelerated computing
- tipe instance menawarkan family, generasi, dan ukuran

> penamaan dan ukuran jenis EC2 instance

penamaan tipe instance
contoh : t3.large
  - T adalah nama family
  - 3 adalah nomor generasi
  - Large adalah ukuran

> pilih tipe instance : berdasarkan kasus penggunaan

beberapa tipe instans lebih detail:
- **Instans T3** menyediakaninstans tujuan umum berkinerja burstable 
  yang memberikan garis dasar kinerja CPU dengan kemampuan untuk 
  melonjak di atas garis dasar. Kasus penggunaan untuk tipe instans 
  ini mencakup situs web dan aplikasi web, lingkungan pengembangan, 
  server pembangun, repositori kode, layanan mikro, lingkungan 
  pengujian dan tahapan, dan aplikasi lini bisnis
- **InstansC5** dioptimalkan untuk beban kerja dengan komputasi 
  intensif, dan memberikan kinerja tinggi hemat biaya dengan harga 
  rendah per rasio komputasi. Kasus penggunaannya meliputi pemodelan 
  ilmiah, pemrosesan batch, penayangan iklan, game multipemain yang 
  dapat diskalakan, dan pengodean video
- **Instans R5** dioptimalkan untuk aplikasi intensif memori. Kasus 
  penggunaan mencakup basis data kinerja tinggi, penambangan dan 
  analisis data, basis data dalam memori, cache dalam memori dengan 
  skala web terdistribusi, aplikasi yang menjalankan pemrosesan 
  real- time untuk big data tidak terstruktur, klaster Apache Hadoop 
  atau Apache Spark, dan aplikasi perusahaan lainnya

> tipe instance : fitur jaringan

- bandwitch jaringan (Gbps) bervariasi menurut tipe instance
- untuk memaksimalkan kinerja jaringan dan bandwitch dari tipe 
  instance:
  - jika  memiliki instance interdependen, luncurkan ke grup 
    penempatan kluster
  - aktifkan jaringan yang ditingkatkan
- jenis jaringan yang ditingkatkan didukung pada kebanyakan tipe 
  instance
- jenis jaringan yang ditingkatkan:
  - Elastic Network Adapter (ENA) : mendukung kecepatan jaringan 
    hingga 100 Gbps
  - Antarmuka Intel 85299 Virtual Function : mendukung kecepatan 
    jaringan hingga 10 Gbps

> pengaturan jaringan

Ketika Anda meluncurkan sebuah instans dalam VPC default, AWS akan memberinya alamatIP publik secara default. Ketika Anda meluncurkan instans ke VPC nondefault, subnet memiliki atribut yang menentukan apakah instans yang diluncurkan ke subnet itu menerima alamat IP publik dari kumpulan alamat IPv4 publik. 

Secara default, AWS tidak akan menetapkan alamat IP publik ke instans yang diluncurkan di subnet nondefault. Anda dapat mengontrol apakah instans Anda menerima alamat IP publik baik dengan memodifikasi atribut pemberian alamat IP publik subnet Anda, atau dengan mengaktifkan atau menonaktifkan fitur pemberian alamat IP publik selama peluncuran (yang menimpa atribut pemberian alamat IP publik milik subnet)

> lampirkan IAM Role (opsional)

Menggunakan EC2 instance untuk menjalankan aplikasi yang harus membuat panggilan API aman ke layanan AWS lain merupakan hal umum. Untuk mendukung kasus penggunaan ini, AWS memungkinkan Anda melampirkan peran AWS Identity and Access Management (IAM) untuk EC2 instance. Tanpa fitur ini, Anda mungkin tergoda untuk menempatkan kredensial AWS pada EC2 instance agar aplikasi yang berjalan pada instans tersebut dapat digunakan.

Profil instansadalah kontainer untuk IAM role.Jika Anda menggunakan AWS Management Console untuk membuat peran bagi Amazon EC2, konsol tersebut secara otomatis membuat profil instans dan memberikan nama yang sama dengan peran. Ketika Anda kemudian menggunakan konsol Amazon EC2 untuk meluncurkan instans dengan IAM role, Anda dapat memilih peran untuk dikaitkan dengan instans. Di konsol tersebut, daftar yang ditampilkan sebenarnya adalah daftar nama profil instans. 

> skrip data pengguna (opsional)

Ketika Anda membuat EC2 instance, Anda memiliki pilihan untuk mengirimkan data penggunake instans. Data pengguna dapat mengautomasi penyelesaian instalasi dan konfigurasi pada peluncuran instans. Contohnya, skrip data pengguna dapat melakukan patch dan memperbarui sistem operasi instans, mengambil dan menginstal kunci lisensi perangkat lunak, atau menginstal perangkat lunak tambahan.

Ketika EC2 instance dibuat, skrip data pengguna akan berjalan dengan hak istimewa root selama fase akhir proses booting. Pada instans Linux, itu dijalankan oleh layanan cloud-init. Pada instans Windows, itu dijalankan oleh utilitas EC2Config atau EC2Launch. Secara default, data pengguna hanya berjalan saat pertama kali instans dimulai.

> tentukan penyimpanan

Saat meluncurkan EC2 instance, Anda dapat mengonfigurasi opsi penyimpanan. Misalnya, Anda dapat mengonfigurasi ukuran volume root tempat sistem operasi tamu diinstal. Anda juga dapat melampirkan volume penyimpanan tambahan saat meluncurkan instans. Beberapa AMI juga dikonfigurasi untuk meluncurkan lebih dari satu volume penyimpanan secara default untuk menyediakan penyimpanan yang terpisah dari volume root

> pilihan penyimpanan Amazon EC2

**Amazon Elastic Block Store (Amazon EBS)** adalah layanan penyimpanan blok tahan lama yang mudah digunakan, berkinerja tinggi, dan dirancang untuk digunakan dengan Amazon EC2 untuk beban kerja dengan throughput serta transaksi yang intensif.

**Tempat Penyimpanan Instans Amazon EC2** menyediakan penyimpanan tingkat blok sementara untuk instans Anda. Penyimpanan ini terletak di disk yang secara fisik terpasang pada komputer host. Tempat Penyimpanan Instans bekerja dengan baik ketika Anda harus menyimpan sementara informasi yang sering berubah, seperti buffer, cache, data awal, dan konten sementara lainnya.

**Amazon Elastic File System (Amazon EFS)** memberikan Sistem File Jaringan (NFS) elastis yang sederhana, dapat diskalakan, dan terkelola sepenuhnya untuk digunakan dengan layanan AWS Cloud dan sumber daya on-premise. Dibuat untuk diskalakan sesuai permintaan hingga petabyte tanpa mengganggu aplikasi.

**Amazon Simple Storage Service (Amazon S3)** adalah layanan penyimpanan objek yang menawarkan skalabilitas, ketersediaan data, keamanan, dan kinerja.

> tambahkan tag

Tag adalah label yang dapat Anda tetapkan ke sumber daya AWS. Setiap tag berisikuncidan nilai opsional, keduanya Anda yang tentukan. Tag memungkinkan Anda mengategorikan sumber daya AWS, seperti EC2 instance, dengan cara berbeda. Misalnya, Anda dapat memberi tag pada instans berdasarkan tujuan, pemilik, atau lingkungan.

Pemberian tag adalah cara Anda dapat memasangkan metadata ke EC2 instance.Kunci tag dan nilai tag bersifat peka huruf besar dan kecil.

> pengaturan grup keamanan

Suatugrup keamananbertindak sebagai firewall virtual yang mengontrol lalu lintas untuk satu instans atau lebih. Ketika meluncurkan instans, Anda dapat menentukan satu grup keamanan atau lebih; jika tidak, grup keamanan default digunakan

Anda dapat menambahkan aturanke setiap grup keamanan. Aturan memungkinkan lalu lintas ke atau dari instans terkait.

Ketika Anda menentukan aturan, Anda dapat menentukan sumber komunikasi jaringan (aturan masuk) atau tujuan (aturan keluar) yang diizinkan. Sumberdapat berupa alamat IP, rentang alamat IP, grup keamanan lain, gateway titik akhir VPC, atau di mana saja (artinya semua sumber akan diizinkan).

> mengidentifikasi atau membuat pasangan kunci

Setelah Anda menentukan semua konfigurasi yang diperlukan untuk meluncurkan EC2 instance, dan setelah Anda menyesuaikan pengaturan konfigurasi launch wizard EC2 opsional, Anda akan melihat jendela Tinjau Peluncuran Instans. Jika Anda kemudian memilih Luncurkan, dialog akan meminta Anda untuk memilih pasangan kunci yang ada, melanjutkan tanpa pasangan kunci, atau membuat pasangan kunci baru sebelum Anda dapat memilih Luncurkan Instans dan membuat EC2 instance

Untuk terhubung kesuatu instans Windows, gunakan kunci pribadi untuk mendapatkan sandi administrator, lalu masuk ke EC2 instance milik Windows Desktop menggunakan Remote Desktop Protocol (RDP). Untuk membuat koneksi SSH darimesin Windows ke Amazon EC2 instance, Anda dapat menggunakan alat seperti PuTTY, yang akan memerlukan kunci pribadi yang sama.

> opsi lain : luncurkan EC2 instance dengan AWS Command Line 
              Interface

- EC2 instance dapat dibuat secara terprogram
- contoh dibawah ini menunjukkan sesederhana apa perintahnya
  
  ![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/661fe829-a265-4117-9886-c67f39dfa97c)

Dalam contoh perintah AWS CLI, Anda melihat satu perintah yang menentukan informasi minimal yang diperlukan untuk meluncurkan sebuah instans. Perintahnya mencakup informasi berikut:
- aws : menentukan pemanggilan utilitas baris perintah aws
- ec2 : menentukan pemanggilan perintah layanan ec2
- run-instances : adalah sub perintah yang sedang dipanggil

  Perintah akan berhasil membuat EC2 instance jika:
  - Perintah terbentuk dengan benar
  - Sumber daya yang dibutuhkan perintah sudah ada
  - Anda memiliki izin yang cukup untuk menjalankan perintah
  - Anda memiliki kapasitas yang cukup di akun AWSJika perintah 
    berhasil, API merespons perintah dengan ID instans dan data lain 
    yang relevan bagi aplikasi Anda untuk digunakan dalam permintaan 
    API berikutnya

> pertimbangkan untuk menggunakan alamat IP Elastis

- reboot instans tidak akan mengubah alamat IP atau nama host DNS
- ketika sebuah instans diberhentikan dan kemudian dimulai lagi:
  - alamat IPv4 publik dan nama host DNS eksternal akan berubah
  - alamat IPv4 publik dan nama host DNS eksternal tidak akan berubah
- jika anda memerlukan alamat IP publik persisten:
  - kaitkan alamat IP elastis dengan instance
- karakteristik alamat IP elastis
  - dapat dikaitkan seperlunya dengan instance di wilayah
  - tetap dialokasikan ke akun sampai memilih untuk melepaskannya
  
### pengoptimalan biaya Amazon EC2

> model harga Amazon EC2

Amazon menawarkan model harga yang berbeda yang dapat dipilih ketika Anda ingin menjalankan EC2 instance.

**Penagihan per detik** hanya tersedia untuk Instans Sesuai Permintaan, Instans Cadangan, dan Instans Spot yang menjalankan Amazon Linux atau Ubuntu.

**Instans** Sesuai Permintaan memenuhi syarat untuk AWS Tingkat Gratis. Instans ini memiliki biaya di muka paling rendah dan fleksibilitas paling besar. Tidak ada komitmen di muka atau kontrak jangka panjang. Ini adalah pilihan yang baik untuk aplikasi dengan beban kerja jangka pendek, agresif, atau tak terduga.

**Host Khusus** adalah server fisik dengan kapasitas instans yang khusus untuk Anda gunakan. Anda dapat menggunakan lisensi perangkat lunak per-soket, per-inti, atau per-VM yang ada, seperti untuk Microsoft Windows atau Microsoft SQL Server.

**Instans Khusus** adalah instans yang berjalan di virtual private cloud (VPC) dalam perangkat keras yang dikhususkan untuk satu pelanggan. Instans ini secara fisik diisolasi pada tingkat perangkat keras host dari instans milik akun AWS lainnya.

**Instans Cadangan** memungkinkan Anda memesan kapasitas komputasi untuk jangka waktu 1 tahun atau 3 tahun dengan biaya operasional per jam yang lebih rendah. Harga penggunaan diskon selalu tetap selama Anda memiliki Instans Cadangan. Jika Anda mengharapkan penggunaan yang konsisten dan berat, instans ini dapat memberikan penghematan besar dibandingkan dengan Instans Sesuai Permintaan

**Instans Cadangan Terjadwal** memungkinkan Anda membeli pencadangan kapasitas yang berulang secara harian, mingguan, atau bulanan, dengan durasi tertentu, untuk jangka waktu 1 tahun. Anda membayar untuk waktu yang dijadwalkan ke instans, bahkan jika Anda tidak menggunakannya. 

**Instans Spot** memungkinkan Anda menawar EC2 instance yang tidak terpakai, sehingga dapat menurunkan biaya Anda. Harga per jam untuk Instans Spot berfluktuasi tergantung pada penawaran dan permintaan. Instans Spot Anda berjalan setiap kali tawaran Anda melebihi harga pasar saat itu.

> 4 pilar pengomptimalan biaya

Untuk mengoptimalkan biaya, Anda perlu mempertimbangkan empat pendorong yang konsisten dan kuat:

- kurang tepat –Pilih keseimbangan tipe instans yang tepat. 
  Perhatikan bahwa server dapat dirampingkan atau dimatikan, namun 
  masih dapat memenuhi persyaratan kinerja Anda
- Tingkatkan elastisitas–Desain deployment Anda untuk mengurangi 
  jumlah kapasitas server menganggur dengan mengimplementasikan 
  deployment yang elastis, seperti penskalaan otomatis untuk 
  menangani beban puncak
- Model harga optimal –Kenali opsi harga yang tersedia. Analisis 
  pola penggunaan Anda sehingga Anda dapat menjalankan EC2 instance 
  dengan campuran opsi harga yang tepat
- Optimalkan pilihan penyimpanan –Analisis persyaratan penyimpanan 
  deployment Anda. Kurangi biaya penyimpanan yang tidak terpakai 
  bila memungkinkan, dan pilih opsi penyimpanan lebih murah jika 
  masih dapat memenuhi kebutuhan Anda untuk kinerja penyimpanan

### Layanan Kontainer

**Kontainer** merupakan metode virtualisasi sistem operasi yang memungkinkan Anda menjalankan aplikasi dan dependensinya dalam proses yang sumber dayanya terisolasi

> dasar-dasar kontainer

  - kontainer adalah metode virtualisasi sistem operasi
  - manfaat:
    - dapat diulang,
    - lingkungan mandiri,
    - perangkat lunak berjalan sama di lingkungan yang berbeda,
      - laptop developer, pengujian, produksi
    - lebih cepat dimulai, dan dihentikan atau diakhiri dibandingkan mesin virtual

![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/413af1e9-d8d0-4ee9-bfb5-770d6ea249be)

**What Is Docker?**
  **Docker** adalah platform perangkat lunak yang mengemas perangkat lunak (seperti aplikasi) ke dalam kontainer

Docker paling baik digunakan sebagai solusi bila Anda ingin:
- Menstandardisasi lingkungan
- Mengurangi konflik antara tumpukan bahasa dan versi
- Menggunakan kontainer sebagai layanan
- Menjalankan layanan mikro menggunakan kode deployment terstandardisasi
- Memerlukan portabilitas untuk pemrosesan data

> **Amazon Elastic Container Service (Amazon ECS)**

  layanan manajemen kontainer berkinerja tinggi dan sangat mudah diskalakan yang mendukung kontainer Docker. Amazon ECS memudahkan Anda menjalankan aplikasi di kluster Amazon EC2 instance yang terkelola

Fitur penting Amazon ECS meliputi kemampuan untuk:
- Meluncurkan hingga puluhan ribu kontainer Docker dalam hitungan detik
- Memantaudeployment kontainer
- Mengelolastatus kluster yang menjalankan kontainer
- Menjadwalkankontainer menggunakan penjadwal bawaan atau penjadwal pihak ketiga (misal, 
  Apache Mesos atau Blox)

> **APA ITU KUBERNETES?**

  - Kubernetes adalah perangkat lunak sumber terbuka untuk orkestrasi kontainer
    - men deploy dan mengelola aplikasi kontainer dalam skla besar
    - peralatan yang sama dapat digunakan di on premise dan di cloud
  - Melengkapi Docker
    - Docker memungkinkan anda menjalankan beberapa kontainer pada satu host OS
    - Kubernetes mengatur beberapa host Docker (node)
  - Mengautomasi
    - penyediaan kontainer,
    - jaringan,
    - distribusi muatan,
    - penskalaan
   
> **Amazon Elastic Kubernetes SErvice (Amazon EKS)**

  layanan **Kubernetes** terkelola yang memudahkan Anda untuk menjalankan Kubernetes di AWS tanpa perlu menginstal, mengoperasikan, dan memelihara bidang kontrol Kubernetes Anda sendiri. Layanan ini tersertifikasi kompatibel dengan Kubernetes, sehingga aplikasi yang berjalan di hulu Kubernetes kompatibel dengan Amazon EKS


> **Amazon Elastic Container Registry (Amazon ECR)**

  merupakan registri kontainer Docker yang dikelola sepenuhnya yang memudahkan developer 
  menyimpan, mengelola, dan men-deploy gambar kontainer Docker. Ini terintegrasi dengan 
  Amazon ECS, sehingga Anda dapat menyimpan, menjalankan, dan mengelola gambar kontainer 
  untuk aplikasi yang berjalan di Amazon ECS
  
### Pengantar AWS Lambda

   **AWS Lambda** adalah layanan komputasi nirserver yang digerakkan event. Lambda 
   memungkinkan Anda menjalankan kode tanpa menyediakan atau mengelola server. Anda 
   membuatfungsi Lambda, yaitu sumber daya AWS berisi kode yang Anda unggah. Anda 
   kemudian mengatur fungsi Lambda untuk dipicu, baik secara terjadwal atau dalam 
   merespons suatu peristiwa. Kode Anda hanya berjalan ketika dipicu

> **Manfaat Lambda**

  - mendukung banyak bahasa pemrograman,
  - administrasi yang sepenuhnya otomatis,
  - toleransi kesalahan terintegrasi,
  - mendukung orkestrasi berbagai fungsi,
  - harga bayar per penggunaan

> **sumber peristiwa AWS Lambda**

  Suatu sumber event adalah layanan AWS atau aplikasi buatan developer yang memproduksi 
  event yang memicu jalannya fungsi AWS Lambda

  sumber peristiwa:
  - amazon S3
  - amazon DynamoDB
  - amazon simple notification (amazon sns)
  - amazon simple queue (amazon sqs)
  - amazon API Gateway
  - application load balancer

  Jika Anda menggunakan AWS Management Console untuk membuat fungsi Lambda, Anda perlu 
  memberinya nama lebih dulu. Kemudian, tentukan:
  - Lingkungan runtime yang akan digunakan fungsi tersebut (misalnya, salah satu versi 
    Python atau Node.js)
  - Peran eksekusi (untuk memberikan izin IAM ke fungsi agar dapat berinteraksi dengan 
    layanan AWS lain yang diperlukan)

  Selanjutnya, setelah engeklik Buat Fungsi, konfigurasikan fungsinya. Konfigurasinya 
  meliputi:
  - Tambahkan pemicu(tentukan salah satu sumber event yang tersedia dari slide sebelumnya)
  - Tambahkan kode fungsi Anda (gunakan editor kode yang disediakan atau unggah file 
    berisi kode)
  - Tentukan memoridalam satuan MB untuk dialokasikan ke fungsi Anda (128 MB sampai 3.008 
    MB)
  - Secara opsional, tentukan variabel lingkungan, deskripsi, batas waktu, virtual 
    private cloud (VPC) tertentu untuk menjalankan fungsi, tag yang ingin Anda gunakan, 
    dan pengaturan lainnya. Detail lengkap ada di dokumentasiKonfigurasi Fungsi AWS Lambda

> **Batas AWS Lambda**

  batas lunak per wilayah:
  - eksekusi bersamaan = 1.000
  - penyimpanan fungsi dan lapisan = 75 GB

  Batas maksimal untuk fungsi individu:
  - alokasi memori fungsi maksimum = 3.008 MB
  - batas waktu fungsi = 15  menit
  - ukuran paket deployment = 250 MB unzip, termasuk lapisan
    
### Pengantar AWS Elastic Beanstalk

   **AWS Elastic Beanstalk** adalah opsi layanan komputasi AWS lain. Ini adalah platform 
   as a service (atau PaaS) yang memfasilitasi deployment, penskalaan, dan manajemen 
   cepat untuk aplikasi web dan layanan Anda.

> **Deployment AWS Elastic Beanstalk**
  - mendukung aplikasi web yang ditulis untuk platform umum
    - Java, NET, PHP, Node, js, Python, Ruby, Go, dan Docker
  - unggah kode anda
    - Elastic Beanstalk secara otomatis menangani deployment
    - men-deploy pada server seperti Apache, NGINX, Passanger, Puma, dan Microsoft 
      Internet Information Services (NIS)

> **Manfaat Elastic Beanstalk**

  - Dapat mulai digunakan dengan cepat dan sederhana
  - Produktivitas Developer
  - Sulit untuk dilampaui
  - Kontrol sumber daya penuh

## ☁️ knowledge




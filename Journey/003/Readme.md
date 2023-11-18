## Keamanan AWS Cloud
  Topik:
  - model tanggung jawab bersama AWS
  - AWS Identity and Access Management (IAM)
  - mengamankan akun AWS baru
  - mengamankan data di AWS
  - berupaya memastikan kepatuhan
    
### Model tanggung jawab bersama AWS
   Keamanan dan kepatuhan merupakan tanggung jawab bersama antara AWS dan pelanggan. Model 
   tanggung jawab bersama ini dirancang untuk membantu meringankan beban operasional 
   pelanggan

   **AWS** mengoperasikan, mengelola, dan mengontrol komponen dari lapisan virtualisasi 
   perangkat lunak ke keamanan fisik fasilitas di mana layanan AWS beroperasi.AWS 
   bertanggung jawab melindungi infrastruktur yang menjalankan semua layanan yang 
   ditawarkan di AWS Cloud. Infrastruktur ini terdiri atas perangkat keras, perangkat 
   lunak, jaringan, dan fasilitas yang menjalankan layanan AWS Cloud.Pelanggan bertanggung 
   jawab atas enkripsi data saat istirahat dan data dalam transit
   
   **Pelanggan** juga harus memastikan bahwa jaringan dikonfigurasi untuk keamanan dan v 
   kredensial keamanan dan login dikelola dengan aman. Selain itu, pelanggan bertanggung 
   jawab atas konfigurasi grup keamanan dan konfigurasi sistem operasi yang berjalan pada 
   instans komputasi yang mereka luncurkan (termasuk pembaruan dan patch keamanan)

> AWS bertanggung jawab atas infrastruktur fisik yang menyediakan sumber daya Anda, 
  termasuk:
  - Keamanan fisik pusat data dengan akses berbasis kebutuhan terkontrol; terletak di 
    fasilitas yang tidak mencolok, dengan penjagaan keamanan 24/7; autentikasi dua faktor; 
    logging dan peninjauan akses; pengawasan video; dan degaussing dan penghancuran disk
  - Infrastruktur perangkat keras,seperti server, perangkat penyimpanan, dan peralatan 
    lain yang diandalkan AWS
  - Infrastruktur perangkat lunak,yang menyediakan sistem operasi, aplikasi layanan, dan 
    perangkat lunak virtualisasi
  - Infrastruktur jaringan, sepertirouter, switch, load balancer, firewall, dan kabel. AWS 
    juga terus memantau jaringan di batas-batas eksternal, mengamankan jalur akses, dan 
    menyediakan infrastruktur redundan dengan deteksi gangguan

> Ketika pelanggan menggunakan layanan AWS, mereka tetap memiliki kontrol penuh atas 
  konten mereka. Pelanggan bertanggung jawab mengelola persyaratan keamanan konten 
  sensitif, termasuk:
  - Konten yang pelanggan pilih untuk disimpan di AWS
  - Layanan AWS yang digunakan bersama konten
  - Di negara mana konten tersebut disimpan
  - Format dan struktur dari konten tersebut, serta apakah konten tersebut disembunyikan, 
    dianonimkan, atau dienkripsi
  - Pelanggan yang memiliki akses ke konten tersebut serta bagaimana akses itu diberikan, 
    dikelola, dan ditarik kembali

> Karakteristik layanan dan tanggung jawab keamanan (lanjutan)
  - Software as a service (SaaS) mengacu pada layanan yang menyediakan perangkat lunak 
    yang di-hosting secara terpusat yang biasanya dapat diakses melalui web browser, 
    aplikasi seluler, atau antarmuka pemrograman aplikasi (API)
  - AWS Shield, danAmazon Chime—dapat dikategorikan sebagai penawaran SaaS, mengingat 
    karakteristik mereka
  - AWS Trusted Advisor adalah alat online yang menganalisis lingkungan AWS Anda dan 
    memberikan panduan real-time dan rekomendasi untuk membantu Anda menyediakan sumber 
    daya Anda dengan mengikuti praktik terbaik AWS
  - AWS Shield adalah layanan perlindungan distributed denial of service (DDoS) terkelola 
    yang melindungi aplikasi yang berjalan di AWS. AWS Shield menyediakan deteksi yang 
    selalu aktif dan mitigasi inline otomatis
  - Amazon Chime adalah layanan komunikasi bagi Anda untuk rapat, mengobrol, dan telepon 
    bisnis di dalam dan di luar organisasi Anda, semuanya dengan satu aplikasi.Ini adalah 
    layanan komunikasi bayar sesuai pemakaian tanpa biaya awal, komitmen, atau kontrak 
    jangka panjang

### AWS Identity and Access Management (IAM)

   AWS Identity and Access Management (IAM) memungkinkan Anda mengontrol akses ke komputasi, 
   penyimpanan, basis data, dan layanan aplikasi di AWS Cloud. IAM dapat digunakan untuk menangani 
   autentikasi, dan untuk menentukan dan menegakkan kebijakan otorisasi sehingga Anda dapat 
   menentukan pengguna yang dapat mengakses layanan.
   
   IAM adalah alat yang secara terpusat mengelola akses untuk meluncurkan, mengonfigurasi, 
   mengelola, dan mengakhiri sumber daya di akun AWS Anda. Ini memberikan kontrol detail atas 
   akses ke sumber daya, termasuk kemampuan untuk   menentukan dengan tepat panggilan API mana 
   yang diizinkan untuk dilakukan pengguna ke setiap layanan.

   Dengan IAM, Anda dapat mengelola sumber daya yangdapat diakses oleh siapa, dan bagaimanasumber 
   daya ini dapat diakses. Anda dapat memberikan izin yang berbeda kepada orang yang berbeda untuk 
   sumber daya yang berbeda. IAM adalah fitur akun AWS yang ditawarkan tanpa biaya tambahan.

 > IAM: Komponen Penting
   - Pengguna IAM   :  Seseorang atau aplikasi yang dapat mengautentikasi dengan akun AWS
   - Grup IAM       :  Koleksi pengguna IAM yang diberikan otorisasi identik
   - Kebijakan IAM  :  Dokumen yang menentukan sumber daya mana yang dapat diakses dan tingkat 
                       akses ke setiap sumber daya
   - IAM role       :  Mekanisme yang berguna untuk memberikan satu set izin untuk membuat 
                       permintaan layanan AWS

> Autentikasi sebagai pengguna IAM untuk mendapatkan akses
  - Akses Program
    - Autentikasi menggunakan:
      - access key ID
      - secret access key
    - Menyediakan akses AWS CLI dan AWS SDK

  - Akses AWS Management Console
    - Autentikasi menggunakan:
      - 12-digit akun ID atau alias
      - nama pengguna IAM
      - kata sandi IAM
   - jika diaktifkan, otentikasi multifaktor (MFA) meminta kode autentikasi

> IAM MFA
  - MFA memberikan peningkatan keamanan
  - selain nama pengguna dan kata sandi, MFA memerlukan kode autentikasi unik untuk mengakses 
    layanan AWS

Layanan dan sumber daya AWS dapat diakses dengan menggunakan AWS Management Console, AWS CLI, atau melalui SDK dan API. Untuk keamanan yang meningkat, sebaiknya aktifkan MFA.Dengan MFA, pengguna dan sistem harus memberikan token MFA—selain kredensial masuk biasa—sebelum mereka dapat mengakses layanan dan sumber daya AWS

> IAM Otorisasi
  - menetapkan izin dengan membuat kebijakan IAM
  - izin menentukan sumber  daya dan operasi yang diizinkan:
    - semua izin secara implisit ditolak secara default
    - jika ada sesuatu yang ditolak secara eksplisit, berarti tidak pernah diizinkan

Untuk menetapkan izin kepada pengguna, grup, atau peran, Anda harus membuatkebijakan IAM(atau menemukan kebijakan yang ada di akun). Tidak ada izin default. Semua tindakan dalam akun ditolak untuk pengguna secara default (pemblokiran implisit) kecuali tindakan tersebut diizinkan secara eksplisit. Tindakan apa pun yang tidak Anda izinkan secara eksplisit akan ditolak. Tindakan apa pun yang secara eksplisit Anda tolak akan selalu ditolak.

> Kebijakan IAM
  - kebijakan IAM adalah dokumen yang mendefinisikan izin
    -memberikan kontrol akses ketat
  - dua jenis kebijakan berbasis identitas dan berbasis sumber daya
  - kebijakan berbasis identitas 
    - pasang kebijakan pada entitas IAM apa pun
      - pengguna IAM, grup IAM, atau IAM role
    - kebijakan menentukan:
      - tindakan yang dapat dilakukan oleh entitas
      - tindakan yang mungkin tidak dapat dilakukan oleh entitas
    - satu kebijakan dapat dilekatkan ke beberapa entitas
    - satu entitas dapat memiliki beberapa kebijakan yang melekat
 - kebijakan berbasis sumber daya
   - terlampir ke sumber daya (seperti bucket S3)

Kebijakan IAM adalah pernyataan resmi izin yang akan diberikan kepada entitas. Kebijakan dapat dilampirkan ke setiap entitas IAM. Entitas mencakup pengguna, grup, peran, atau sumber daya

Terdapat dua jenis kebijakan IAM: Kebijakan berbasis identitasadalah kebijakan izin yang dapat Anda lampirkan pada pelaku (atau identitas), seperti pengguna, peran, atau grup IAM. Kebijakan ini mengontrol tindakan apa yang dapat dilakukan identitas, pada sumber daya apa, dan dalam kondisi apa.  

> Kebijakan berbasis identitas dapat dikategorikan lebih lanjut sebagai:
  - Kebijakan terkelola –Kebijakan berbasis identitas yang mandiri yang dapat Anda lampirkan pada 
    beberapa pengguna, grup, dan peran dalam akun AWS Anda
  - Kebijakan inline –Kebijakan yang Anda buat dan kelola, dan yang tertanam secara langsung dalam 
    grup atau peran pengguna tunggal

Kebijakan berbasis sumber daya adalah dokumen kebijakan JSON yang Anda lampirkan pada sumber daya, seperti bucket Amazon S3. Kebijakan ini mengatur tindakan apa yang dapat dilakukan pelaku tertentu pada sumber daya tersebut, dan dalam kondisi apa

> Izin IAM

Ketika IAM menentukan apakah izin diperbolehkan, pertama-tama IAM memeriksa keberadaan kebijakan penolakan eksplisit. Jika tidak ada penolakan eksplisit, IAM kemudian memeriksa kebijakan izin eksplisit yang berlaku. Jika keduanya tidak ada, IAM kembali ke default, yaitu memblokir akses. Proses ini disebut sebagai pemblokiran implisit. Pengguna akan diizinkan untuk mengambil tindakan hanya jika tindakan yang diminta tidak secara eksplisit ditolak dan secaraeksplisit diperbolehkan.

Sulit untuk mengetahui apakah akses ke sumber daya akan diberikan kepada entitas IAM ketika Anda mengembangkan kebijakan IAM

> Grup IAM

Grup IAMadalah kumpulan pengguna IAM.Grup IAM menawarkan cara yang nyaman untuk menentukan izin untuk kumpulan pengguna, yang dapat mempermudah pengelolaan izin bagi para pengguna

Karakteristik penting dari grup IAM:
- Sebuah grup dapat berisi banyak pengguna, dan pengguna dapat menjadi milik beberapa grup.•Grup tidak dapat ditumpuk. Grup hanya dapat berisi pengguna, dan grup tidak dapat berisi grup lain.
- Tidak ada grup default yang secara otomatis mencakup semua pengguna di akun AWS. Jika Anda ingin memiliki grup dengan semua pengguna akun di dalamnya, Anda perlu membuat grup dan menambahkan setiap pengguna baru ke dalamnya

> IAM role

IAM role adalah identitas IAM yang dapat Anda buat di akun Anda yang memiliki izin khusus.IAM role mirip dengan pengguna IAMkarena ini juga merupakan AWS identity yang dapat Anda lampirkan kebijakan izinnya, dan izin tersebut menentukan apa yang dapat dan tidak dapat dilakukan oleh identitas tersebut di AWS. Namun, bukannya dikaitkan dengan satu orang secara unik, peran dapat dijalankan oleh siapa saja yang membutuhkannya. Peran tidak memiliki standar kredensial jangka panjang (sandi atau access key) yang terkait dengannya. Sebaliknya, bila Anda mengambil peran, peran menyediakan kredensial keamanan sementara untuk sesi peran Anda.

#### Mengamankan  akun AWS baru

> Mengamankan akun AWS baru: pengguna root akun

Untuk berhenti menggunakan pengguna root akun, lakukan langkah-langkah berikut:
- Ketika Anda masuk ke pengguna root akun, buat pengguna IAM untuk Anda sendiri dengan akses AWS 
  Management Console diaktifkan (tetapi jangan lampirkan izin apa pun kepada pengguna). Simpan 
  access key pengguna IAM jika diperlukan.
- Berikutnya, buat grup IAM, beri nama (seperti FullAccess), dan lampirkan kebijakan IAM ke grup 
  yang memberikan akses penuh ke setidaknya beberapa layanan yang akan Anda gunakan. Selanjutnya, 
  tambahkan pengguna IAM ke grup.
- Nonaktifkan dan hapus access key pengguna root akun Anda, jika ada.
- Aktifkan kebijakan sandi untuk semua pengguna. Salin tautan masuk pengguna IAM dari halaman 
  Dasbor IAM. Kemudian, keluar sebagai pengguna root akun.
- Jelajahi tautan masuk pengguna IAM yang Anda salin, dan masuk ke akun dengan menggunakan 
  kredensial pengguna IAM baru Anda. 6.Simpan kredensial pengguna root Anda di tempat yang aman

> Mengamankan akun AWS baru: MFA

- Pilihan untuk mengambil token MFA
- Aplikasi yang kompatibel dengan MFA virtual: 
  - Google Authenticator
  - Authy Authenticator (aplikasi Windows phone).
  - Perangkat kunci keamanan UZF
- Sebagai contoh Yubikey
  Opsi MFA perangkat keras:
  - Key fob atau kartu display yang ditawarkan oleh Gemalto
 
> Mengamankan akun AWS baru: AWS CloudTrail

AWS CloudTrail adalah layanan yang mencatat semua permintaan API ke sumber daya di akun Anda

> Mengamankan akun AWS baru: layanan tagihan

Langkah yang direkomendasikan tambahan untuk mengamankan akun AWS baru adalah untuk mengaktifkan laporan penagihan, seperti Laporan Penggunaan dan Biaya AWS. Laporan tagihan memberikan informasi tentang penggunaan sumber daya AWS dan perkiraan biaya untuk penggunaan itu. AWS memberikan laporan kepada bucket Amazon S3 yang Anda tentukan dan AWS memperbarui laporan setidaknya sekali per hari

#### Mengamankan Akun AWS baru

> Mengamankan Akun

- AWS Organizations
AWS Organizations adalah layanan manajemen akun yang memungkinkan Anda mengonsolidasikan beberapa akun AWS ke sebuahorganisasiyang Anda buat dan kelola secara terpusat. Di sini, fokusnya adalah pada fitur keamanan yang disediakan AWS Organizations.

Salah satu fitur keamanan yang berguna adalah bahwa Anda dapat mengelompokkan akun ke unit organisasi(OU) dan melekatkan kebijakan akses yang berbeda untuk setiap OU. Misalnya, jika Anda memiliki akun yang seharusnya hanya diizinkan untuk mengakses layanan AWS yang memenuhi persyaratan peraturan tertentu, Anda dapat menempatkan akun tersebut ke dalam satu OU. Anda kemudian dapat menentukan kebijakan yang memblokir akses OU ke layanan yang tidak memenuhi persyaratan peraturan tersebut, dan kemudian melekatkan kebijakan untuk OU

-  AWS Organizations: Service control policies (SCP)
SCP menawarkan kontrol pusat atas izin maksimum yang tersediauntuk semua akun di organisasi Anda, sehingga memungkinkan Anda memastikan bahwa akun Anda tetap berada dalam pedoman kontrol akses organisasi Anda

SCP mirip dengan kebijakan izin IAMdan menggunakan sintaks yang hampir sama. Namun, SCP tidak pernah memberikan izin. Sebaliknya, SCP adalah kebijakan JSON yang menentukan izin maksimum untuk organisasi atau OU. Melekatkan SCP ke root organisasi atau unit organisasi (OU) mendefinisikan perlindungan untuk tindakan yang dapat dilakukan oleh akun di root organisasi atau OU. Namun, itu bukan pengganti untuk konfigurasi IAM yang dikelola dengan baik dalam tiap akun

- AWS Key Management Service (AWS KMS)
AWS Key Management Service (AWS KMS) adalah layanan yang memungkinkan Anda membuat dan mengelola kunci enkripsi, dan untuk mengontrol penggunaan enkripsi di berbagai layanan AWS dan aplikasi Anda. AWS KMS adalah layanan aman dan tangguh yang menggunakan modul keamanan perangkat keras (HSM) yang divalidasi di bawah Standar Pemrosesan Informasi Federal (FIPS) 140-2(atau sedang dalam proses divalidasi) untuk melindungi kunci Anda. AWS KMS juga terintegrasi dengan AWS CloudTrail guna menyediakan log untuk semua penggunaan kunci Anda untuk membantu memenuhi kebutuhan peraturan dan kepatuhan

#### Mengamankan Data di AWS

**Enkripsi data** adalah alat penting untuk digunakan ketika tujuan Anda adalah untuk melindungi data digital. Enkripsi data mengambil data yang dapat dibaca dan mengodekannya sehingga tidak dapat dibaca oleh siapa pun yang tidak memiliki akses ke kunci rahasia yang dapat digunakan untuk memecahkan kode itu. Jadi, bahkan jika penyerang mendapatkan akses ke data Anda, mereka tidak bisa melakukan apa pun

**Data** saat istirahat mengacu pada data yang tersimpan secara fisik pada disk atau pita

Anda dapat membuat sistem file terenkripsi pada AWS sehingga semua data dan metadata dienkripsi saat istirahat dengan menggunakan standar terbuka algoritma enkripsi Advanced Encryption Standard (AES)-256. Bila Anda menggunakan AWS KMS, enkripsi dan dekripsi ditangani secara otomatis dan transparan, sehingga Anda tidak perlu memodifikasi aplikasi Anda. Jika organisasi Anda tunduk pada kebijakan perusahaan atau peraturan yang memerlukan enkripsi data dan metadata saat istirahat, AWS menyarankan untuk mengaktifkan enkripsi pada semua layanan yang menyimpan data Anda. Anda dapat mengenkripsi data yang disimpan dalam layanan yang didukung oleh AWS KMS

## ☁️ knowledge
![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/538aab61-cf6f-40fb-b044-ad4417a63776)

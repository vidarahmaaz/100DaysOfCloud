
![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/5a4cb527-0108-460d-b6b8-23423b844d89)

# CLOUD COMPUTING [CHAPTER 2]

## Topik yang akan kita pelajari 
   - Dasar-Dasar Harga

## Dasar-Dasar Harga
   Model harga AWS
   - Komputasi : dikenai biaya per jam/detik, bervariasi sesuai tipe instans [hanya linux]
   - Penyimpanan : dikenai biaya biasanya per GB
   - Transfer Data : data keluar dijumlahkan dan dikenai biaya, data masuk tidak dikenai 
                     biaya dengan beberapa pengecualian, dikenai biaya biasanya pe GB 
                      
## Bagaimana cara membayar AWS?
   AWS menawarkan berbagai layanan komputasi cloud. Untuk setiap layanan, Anda membayar 
   persis dengan jumlah sumber daya yang benar-benar Anda perlukan. Model harga bergaya 
   utilitas ini meliputi:
   - bayar sesuai yang anda gunakan
   - bayar lebih sedikit ketika anda melakukan pemesanan
   - bayar lebih sedikit saat anda menggunakan lebih banyak
   - bayar jauh lebih sedikit seiring berkembangnya AWS

   Manfaat lain dari pertumbuhan AWS adalah bahwa sumber daya berperforma lebih tinggi di 
   masa depan akan menggantikan yang ada saat ini tanpa biaya tambahan
   - harga khusus : penuhi berbagai kebutuhan melalui harga khusus, tersedia untuk proyek 
                    bervolume tinggi dengan persyaratan yang unik
   - AWS tingkat gratis : AWS menawarkan tingkat penggunaan gratis (AWS Tingkat Gratis) 
                          untuk pelanggan baru hingga 1 tahun. AWS Tingkat Gratis berlaku 
                          untuk layanan dan opsi tertentu. Jika Anda adalah pelanggan 
                          baru AWS, Anda dapat menjalankan instans mikro T2 Amazon 
                          Elastic Compute Cloud (Amazon EC2) selama satu tahun, sekaligus 
                          menggunakan tingkat penggunaan gratis untuk Amazon S3, Amazon 
                          Elastic Block Store (Amazon EBS), Elastic Load 
                          Balancing, transfer data AWS, dan layanan AWS lainnya
   - layanan tanpa biaya : amazon vpc, elastic beanstalk, auto scaling, aws 
                           cloudformation, aws identity and access management (IAM)

   AWS juga menawarkan berbagai layanan tanpa biaya tambahan.
   - Amazon Virtual Private Cloud (Amazon VPC) memungkinkan Anda menyediakan bagian 
     yang terisolasi dari AWS Cloud secara logis, tempat Anda dapat meluncurkan sumber 
     daya AWS dalam jaringan virtual yang Anda tentukan
   - AWS Identity and Access Management (IAM)mengontrol akses pengguna Anda ke layanan 
     dan sumber daya AWS 
   - Tagihan Terkonsolidasi adalah fitur penagihan di AWS Organizations untuk 
     menggabungkan pembayaran untuk beberapa akun AWS atau beberapa akun Amazon Internet 
     Services Private Limited (AISPL). Tagihan terkonsolidasi menyediakan:
     Satu tagihan untuk beberapa akun, Kemampuan untuk dengan mudah melacak biaya setiap 
     akun, Kesempatan untuk mengurangi biaya sebagai hasil diskon harga volume dari 
     penggunaan gabungan, Anda juga dapat menggabungkan semua akun Anda menggunakan 
     Tagihan Terkonsolidasi dan mendapatkan manfaat bertingkat
   - AWS Elastic Beanstalk merupakan cara yang lebih mudah untuk Anda dalam men-deploy dan
     mengelola aplikasi dengan cepat di AWS Cloud
   - AWS CloudFormationmemberikan cara yang mudah kepada developer dan administrator 
     sistem untuk membuat kumpulan sumber daya AWS terkait dan menyediakannya secara 
     teratur dan dapat diperkirakan
   - Penskalaan Otomatis menambahkan atau menghapus sumber daya secara otomatis sesuai 
     dengan kondisi yang Anda tentukan. Sumber daya yang Anda gunakan meningkat dengan 
     lancar selama lonjakan permintaan untuk mempertahankan performa dan menurun secara 
     otomatis selama jeda permintaan untuk meminimalkan biaya
   - AWS OpsWorks merupakan layanan pengelolaan aplikasi yang memudahkan deploy dan 
     mengoperasikan aplikasi dengan berbagai bentuk dan ukuran

## AWS Organizations
   layanan manajemen akun yang memungkinkan Anda menggabungkan beberapa akun AWS ke 
   sebuah organisasi yang Anda buat dan kelola secara terpusat

   Manfaat utama AWS Organizations adalah:
   - Mengelola kebijakan akses secara terpusat di beberapa akun AWS
   - Mengontrol akses ke layanan AWS
   - Mengautomasi pembuatan dan pengelolaan akun AWS
   - Tagihan terkonsolidasi di beberapa akun AWS

   terminologi AWS Organizations:
   ![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/8f00d8bd-3c36-41f1-915a-4b390decc18a)

fitur utama dan manfaat:
- manajemen akun berbasis kebijakan
- manajemen akun berbasis grup
- antarmuka pemograman aplikasi (API) yang mengotomatiskan manajemen akun
- tagihan terkonsolidasi

  > keamanan dengan AWS Organizations
    - kontrol akses dengan AWS Identity and Access Management (IAM)
    - kebijakan IAM memungkinkan anda mengizinkan atau menolak akses ke layanan AWS untuk       pengguna, grup, dan peran
    - service control policies (SCP) memungkinkan anda ,mengizinkan atau menolak akses ke 
      layanan AWS untuk akun individu atau grup di unit organisasi (OU)

   > Manajemen Penagihan dan Biaya AWS
     - layanan yang Anda gunakan untuk membayar tagihan AWS, memantau penggunaan, dan 
     memprakirakan dan mendapatkan gambaran yang lebih baik mengenai besarnya biaya dan 
     penggunaan Anda di masa depan sehingga Anda dapat membuat rencana untuk ke depannya
  
## AWS Support
   - Menyediakan kombinasi alat dan keahlian yang unik:
     - aws support
     - paket aws support
   - Dukungan disediakan untuk:
     - bereksperimen dengan AWS
     - penggunaan produk AWS
     - penggunaan AWS untuk bisnis penting

   - Panduan proaktif:
     - manajer akun teknis (MAT)
   - Praktik terbaik:
     - AWS Trusted Advisor
   - Bantuan akun:
     - AWS Support Concierge

# CLOUD COMPUTING [CHAPTER 3]

## Topik yang akan kita pelajari
   - Infrastruktur Global AWS
   - Layanan AWS dan kategori layanan

## Infrastruktur Global AWS
   Infrastruktur Global AWS dirancang dan dibangun untuk memberikan lingkungan komputasi cloud 
   yang fleksibel, dapat diandalkan, dapat diskalakan, dan aman dengan kinerja jaringan global 
   berkualitas tinggi
    ![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/ccfd35cc-6a5f-44ea-bb07-09dcf24d36e4)

  > Wilayah AWS 
  - Wilayah AWS adalah daerah geografis
  - Replikasi data diseluruh wilayah dikendalikan oleh anda
  - Komunikasi lintas wilayah menggunakan infrastruktur jaringan backbone AWS
  - Setiap wilayah AWS menyediakan redundansi dan konektivitas penuh ke jaringan                      - Wilayah biasanya berisi dua atau lebih Availability Zone

  > Availability Zone
  - Setiap wilayah memiliki beberapa Availability Zone
  - Setiap Availability Zone adalah partisi yang sepenuhnya terisolasi dari infrastruktur 
    AWS

  > Pusat data AWS
  - Pusat data AWS dirancang demi keamanan
  - Pusat data adalah tempat data berada dan pemrosesan data terjadi
  - Setiap pusat data memiliki daya, jaringan, dan konektivitas berlebih, dan ditempatkan 
    di fasilitas yang terpisah
  - Pusat data biasanya memiliki 50.000 sampai 80.000 server fisik

Pusat data AWS dirancang dengan aman dengan mempertimbangkan beberapa faktor:
- Setiap lokasi dievaluasi dengan saksama untuk mengurangi risiko lingkungan
- Pusat data memiliki desain redundanyang mengantisipasi dan menoleransi kegagalan 
  sekaligus menjaga tingkat layanan
- Untuk memastikan ketersediaan, komponensistem penting dicadangkandi beberapa 
  Availability Zone
- Untuk memastikan kapasitas, AWS terus memantau penggunaan layanan untuk men-deploy 
  infrastruktur guna mendukung komitmen dan persyaratan ketersediaan.Lokasi Pusat data 
  tidak diungkapkandan semua akses ke sana dibatasi
- Jika terjadi kegagalan, proses otomatis memindahkan lalu lintas data dari area yang 
  terdampak

AWS Global Infrastructure memiliki beberapa fitur berharga:
- Pertama, elastis dan dapat diskalakan. Ini berarti sumber daya dapat menyesuaikan 
  dengan peningkatan atau penurunan kebutuhan kapasitas secara dinamis. Ini juga dapat 
  dengan cepat menyesuaikan untuk mengakomodasi pertumbuhan
- Kedua, infrastruktur initoleran terhadap kesalahan, yang berarti memiliki redundansi 
  komponen bawaan yang memungkinkannya melanjutkan operasi meskipun komponen gagal
- Terakhir, diperlukan sedikit atau tanpa intervensi manusia, sekaligus memberikan 
  ketersediaan tinggidengan sedikit waktu henti

## Ikhtisar Layanan AWS dan Layanan Kategori
   Infrastruktur Global AWS dapat dibagi menjadi tiga elemen: 
   - Wilayah,
   - Availability Zone, dan
   - Points of Presence, yang disertai edge location

> kategori layanan penyimpanan
  - Amazon Simple Storage Service (Amazon S3) adalah layanan penyimpanan objek yang 
    menawarkan skalabilitas, ketersediaan data, keamanan, dan kinerja
  - Amazon Elastic Block Store (Amazon EBS)adalah penyimpanan blok berkinerja tinggi, 
    yang dirancang untuk digunakan dengan Amazon EC2 untuk beban kerja intensif 
    throughput dan transaksi
  - Amazon Elastic File System (Amazon EFS)menyediakan Sistem File Jaringan (NFS) 
    elastis, dapat diskalakan, dan terkelola sepenuhnya untuk digunakan dengan layanan 
    AWS Cloud dan sumber daya on-premise
  - Amazon Simple Storage Services Glacieradalah kelas penyimpanan cloud Amazon S3 yang 
    aman, tahan lama, dan berbiaya sangat rendah untuk pengarsipan data dan pencadangan 
    jangka panjang

    Layanan komputasi AWS
    - Amazon Elastic Compute cloud (Amazon EC2)
    - Amazon EC2 Auto Scaling
    - Amazon Elastic Container Service (Amazon ECS)
    - Amazon Elastic Container Registry (Amazon ECR)
    - AWS Elastic Beanstalk
    - Amazon Elastic Kubernetes Service (Amazon EKS)
    - AWS Fargate
   
    Layanan basis data AWS
    - Layanan basis data AWS
    - Amazon Aurora
    - Amazon Redshift
    - Amazon Redshift

> kategori layanan jaringan dan penyampaian konten
  Layanan jaringan dan penyampaian konten AWS:
  - Amazon Virtual Private Cloud (Amazon VPC) memungkinkan Anda menyediakan bagian yang 
    terisolasi secara logis dari AWS Cloud
  - Elastic Load Balancing secara otomatis mendistribusikan lalu lintas aplikasi yang 
    masuk di beberapa target, seperti Amazon EC2 instance, kontainer, alamat IP, dan 
    fungsi Lambda
  - Amazon CloudFront adalah layanan jaringan penyampaian konten (CDN) cepat yang 
    memberikan data, video, aplikasi, dan antarmuka pemrograman aplikasi (API) dengan 
    aman kepada pelanggan secara global dengan latensi rendah dan kecepatan transfer 
    tinggi
  - AWS Transit Gateway adalah layanan yang memungkinkan pelanggan menghubungkan Amazon 
    Virtual Private Cloud (VPC) dan jaringan on-premise mereka ke satu gateway
  - Amazon Route 53 adalah layanan web Domain Name System (DNS) cloud yang dapat 
    diskalakan yang dirancang untuk memberikan cara yang dapat diandalkan untuk merutekan 
    pengguna akhir ke aplikasi internet
  - AWS Direct Connect menyediakan cara untuk membuat koneksi jaringan pribadi khusus 
    dari pusat data atau kantor Anda ke AWS, yang dapat mengurangi biaya jaringan dan 
    meningkatkan throughput bandwidth
  - AWS VPN menyediakan terowongan pribadi yang aman dari jaringan atau perangkat Anda ke 
    jaringan global AWS

> kategori layanan keamanan, identitas, dan kepatuhan
  - AWS Identity and Access Management (IAM)
  - AWS Organizations
  - Amazon Cognito
  - AWS Artifact
  - AWS Key Management Service (AWS KMS)
  - AWS Shield

> kategori layanan manajemen biaya AWS
  - Laporan Penggunaan dan Biaya AWS berisi kumpulan data biaya dan penggunaan AWS 
    terlengkap yang tersedia, termasuk metadata tambahan tentang layanan, harga, dan 
    reservasi AWS
  - AWS Budgets memungkinkan Anda mengatur anggaran kustom yang akan memberi Anda 
    peringatan saat biaya atau penggunaan Anda melebihi (atau diprakirakan akan melebihi) 
    jumlah yang Anda anggarkan
  - AWS Cost Explorer memiliki antarmuka yang mudah digunakan yang memungkinkan Anda 
    memvisualisasikan, memahami, serta mengelola biaya dan penggunaan AWS Anda dari waktu 
    ke waktu

> kategori layanan manajemen dan tata kelola
  - AWS Management Console memberikan antarmuka pengguna berbasis web untuk mengakses 
    akun AWS Anda
  - AWS Config menyediakan layanan yang membantu Anda melacak inventaris dan perubahan 
    sumber daya
  - Amazon CloudWatch memungkinkan Anda memantau sumber daya dan aplikasi
  - AWS Auto Scaling menyediakan fitur yang memungkinkan Anda menskalakan beberapa sumber 
    daya untuk memenuhi permintaan
  - AWS Command Line Interface menyediakan alat terpadu untuk mengelola layanan AWS
  - AWS Trusted Advisor membantu Anda mengoptimalkan kinerja dan keamanan
  - AWS Well-Architected Tool menyediakan bantuan dalam meninjau dan meningkatkan beban 
    kerja Anda
  - AWS CloudTrail melacak aktivitas pengguna dan penggunaan API

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
    
## Cloud Research

- ✍️ Document your trial and errors. Share what you tried to learn and understand about the cloud topic or while completing micro-project.
- 🖼️ Show as many screenshot as possible so others can experience in your cloud research.

## Try yourself

✍️ Add a mini tutorial to encourage the reader to get started learning something new about the cloud.

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

### Step 3 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

## ☁️ Cloud Outcome

✍️ (Result) Describe your personal outcome, and lessons learned.

## Next Steps

✍️ Describe what you think you think you want to do next.

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)

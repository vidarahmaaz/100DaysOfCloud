
# CLOUD COMPUTING [DAY 1]

## Introduction
Apa yang akan kita pelajari???

- Apa itu cloud computing
- Model layanan cloud computing
- Manfaat atau kelebihan cloud computing
- Model deployment cloud computing + contoh
- pengenalan AWS
- Infrastructure AWS ; Region, AZ, POP, Edge, data center
- Knowledge

# Cloud Research
## ![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/9a95eb63-9a56-49dc-8a95-e898d729ee6b)

Cloud Computing atau Komputasi cloud adalah pengiriman sesuai permintaan untuk daya komputasi, basis data, penyimpanan, aplikasi, dan sumber daya IT lain melalui internet dengan harga sesuai pemakaian.

## Model layanan cloud computing
Ada tiga model layanan cloud utama:
> IaaS >> Infrastructure as a Service
  Layanan dalam kategori ini adalah blok bangunan dasar untuk IT cloud dan biasanya   
  menyediakan akses ke fitur jaringan, komputer (virtual atau pada perangkat keras 
  khusus), dan ruang penyimpanan data. IaaS memberikan tingkat fleksibilitas dan 
  kontrol pengelolaan tertinggi atas sumber daya IT Anda. Ini adalah hal yang paling 
  mirip dengan sumber daya IT yang banyak dikenal oleh departemen dan developer IT saat 
  ini

> PaaS >> Platform as a Service
  Layanan dalam kategori ini menghilangkan kebutuhan organisasi untuk mengelola 
  infrastruktur dasarnya (biasanya perangkat keras dan sistem operasi), serta 
  memungkinkan Anda untuk fokus pada deployment dan pengelolaan aplikasi Anda

> SaaS >> Software as a Service
  Layanan dalam kategori ini memberikan Anda produk lengkap yang dijalankan dan 
  dikelola  oleh penyedia layanan. Dalam kebanyakan kasus, software as a servicemengacu 
  pada aplikasi pengguna akhir. Dengan penawaran SaaS, Anda tidak perlu lagi memikirkan 
  cara memelihara layanan atau cara mengelola infrastruktur dasar. Anda hanya perlu 
  memikirkan cara bagaimana Anda berencana untuk menggunakan perangkat lunak tertentu

## Manfaat / Kelebihan Cloud Computing
Berikut ini beberapa manfaat atau kelebihan cloud computing :
- Menukar biaya modal untuk biaya variabel, harga bayar yang di konsumsi,
- Skala ekonomi masif, harga lebih rendah dikarenakan adanya ratusan penggunaan di 
   cloud,
- Berhenti menebak kapasitas, kita tidak perlu menebak kapasitas yang diperlukan,
- Meningkatkan kecepatan dan ketangkasan,
- Berhenti menghabiskan uang untuk mrnjalankan dan memelihara pusat data,
- Merambah dunia global dalam hitungan menit, dapat men-deploy aplikasi di  beberapa 
   wilayah di dunia dalam beberapa kali klik.

## Model Deployment Cloud Computing + Contoh
Ada tiga model deployment komputasi cloud utama
> Cloud >>  Aplikasi berbasis cloud sepenuhnya diterapkan di cloud dan semua bagian 
            aplikasi yang berjalan di cloud. Aplikasi di cloud telah dibuat di cloud 
            atau telah dimigrasikan dari infrastruktur yang ada untuk mengambil manfaat 
            cloud computing.
  contoh : rackspace [private cloud]
           azure, alibaba, google cloud, [publik cloud]

> Hybrid >>  Deployment hybrid adalah cara untuk menghubungkan infrastruktur dan 
             aplikasi antara sumber daya berbasis cloud dan sumber daya yang ada yang 
             tidak terletak di cloud. Metode deployment hybrid yang paling umum adalah 
             antara cloud dan infrastruktur on-premise yang ada.
  contoh : server lokal kolaborasi dengan AWS

> On-premise >> Men-deploy sumber daya on-premise, dengan menggunakan alat manajemen 
                sumber daya dan virtualisasi, kadang-kadang disebut cloud privat. 
                Deployment on-premise tidak memberikan banyak manfaat komputasi cloud, 
                deployment ini terkadang dicari karena kemampuannya untuk menyediakan 
                sumber daya khusus.
  contoh : server private

![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/26271bdd-2d8f-4342-80f6-d187f8e81dbd)


## Pengenalan AWS
   Apa yang dimaksud AWS itu???
   - AWS adalah platform cloud yang aman, yang menawarkan serangkaian produk                  global berbasis cloud yang luas.
   - AWS menyediakan akses sesuai permintaan untuk komputasi, penyimpanan, jaringan, 
     basis data, dan sumber daya IT lainnya serta alat manajemen.
   - AWS menawarkan fleksibilitas, lingkungan AWS dapat dikonfigurasi ulang dan 
     diperbarui sesuai permintaan, ditingkatkan dan diturunkan sesuai pola penggunaan.
   - Hanya membayar layanan individual yang anda butuhkan, selama digunakan.
   - Layanan AWS bekerja sama seperti blok bangunan, ayanan AWS dirancang untuk bekerja 
     sama untuk mendukung hampir semua jenis aplikasi atau beban kerja. Pikirkan layanan 
     ini sepertiunsur fundamental, yang bisa Anda rakit dengan cepat untuk membangun 
     solusi canggih dan terukur, dan kemudian menyesuaikannya sesuai perubahan kebutuhan.
     
   Kategori Layanan AWS
   - Migration (Migrasi)
   - Cloud Computing (Komputasi Awan)
   - Storage (Penyimpanan)
   - Security services (Layanan keamanan)
   - Database services (Layanan database)
   - Analytics (Analitik)
   - Management services (Layanan manajemen)
   - Internet of Things
   - Application Services (Layanan Aplikasi)
   - Deployment and Management (Penerapan dan Manajemen)
   
## Infrastructure AWS
   
Infrastruktur Cloud Global AWS adalah platform cloud paling aman, luas, dan andal yang menawarkan 200 layanan unggulan penuh dari pusat data secara global.

> Region 
         
- AWS GovCloud (AS-Timur) Diluncurkan pada tahun 2018
  Zona Ketersediaan: 3
- AWS GovCloud (AS-Barat) Diluncurkan pada tahun 2011
  Zona Ketersediaan: 3
- Kanada Tengah Diluncurkan 2016
  Zona Ketersediaan: 3
- California Utara Diluncurkan tahun 2009
  Zona Ketersediaan: 3
- Virginia Utara Diluncurkan tahun 2006
  Zona Ketersediaan: 6 | Zona Lokal: 14 | Zona Panjang Gelombang: 8
- Ohio Diluncurkan 2016
  Zona Ketersediaan: 3
- Oregon Diluncurkan 2011
  Zona Ketersediaan: 4 | Zona Lokal: 6 | Zona Panjang Gelombang: 5

> Availability Zone >> Availability Zone adalah beberapa lokasi berbeda di dalam sebuah 
                       Wilayah AWS yang direkayasa sedemikian rupa agar terisolasi dari 
                       kegagalan di Availability Zone yang lain. Availability Zone 
                       menyediakan konektivitas jaringan murah berlatensi rendah untuk 
                       Availability Zone lain di Wilayah AWS yang sama.

> POP & Edge >> AWS Edge Location adalah lokasi fisik atau Point of Presence (PoP) yang 
                memampukan penggunaan edge computing, caching, dan memiliki 
                konektivitas ke AWS Global Network. AWS Global Network menghubungkan 
                semua AWS region, availability zone dan edge location dengan koneksi 
                yang private, low-latency, dan redundant.

> Data Center >> Data Center adalah adalah lokasi fisik yang menyimpan mesin komputasi 
                 dan peralatan perangkat keras terkait. Ini berisi infrastruktur 
                 komputasi yang dibutuhkan sistem TI, seperti server, drive penyimpanan 
                 data, dan peralatan jaringan.

![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/cebbac2b-07ff-4f6b-bfb5-f1dbfedd89a1)

## Knowledge
   ![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/05f9b03c-c4fb-42a2-8ff6-2396deed8693)

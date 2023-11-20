![image](https://github.com/vidarahmaaz/100DaysOfCloud/assets/140806084/8ae7deb2-c3c4-44f2-b320-60ba02673c8b)

## STORAGE

### APA YANG AKAN KITA PELAJARI?

berikut topik yang akan di pelajari:
- Amazon Elastic Block Store (Amazon EBS)
- Amazon Simple Storage Service (Amazon S3)
- Amazon Elastic File System (Amazon EFS)
- Amazon Simple Storage Service Glacier

> Layanan AWS Inti

  Penyimpanan adalah kategori layanan inti AWS lain. Beberapa kategori penyimpanan yang 
  luas meliputi:
  - tempat penyimpanan instans (penyimpanan sementara), Amazon EBS, Amazon EFS, Amazon 
    S3,dan Amazon S3 Glacier
  - Tempat penyimpanan instans, atau penyimpanan sementara, adalahpenyimpanan 
    sementara yang ditambahkan ke Amazon EC2 instance Anda
  - Amazon EBS adalah penyimpanan dapat dipasangpersistenyang dapat dipasang sebagai 
    perangkat untuk Amazon EC2 instance. Amazon EBS hanya dapat dipasang ke Amazon EC2 
    instance dalam Availability Zone yang sama. Hanya satu Amazon EC2 instance yang dapat 
    memasang volume Amazon EBS pada satu waktu
  - Amazon EFS adalah sistem file bersama yang dapat dipasangi beberapa Amazon EC2 
    instance secara bersamaan
  - Amazon S3 adalah penyimpanan persisten tempat setiap file menjadi objek dan tersedia 
    melalui Uniform Resource Locator (URL); dapat diakses dari mana saja
  - Amazon S3 Glacier adalah penyimpanan dingin bagi data yang jarang diakses (misalnya, 
    ketika Anda membutuhkan penyimpanan data jangka panjang untuk alasan arsip atau 
    kepatuhan)

### Amazon Elastic Block Store (Amazon EBS)

Amazon EBS memberikan volume penyimpanan tingkat blok yang persisten untuk digunakan dengan Amazon EC2 instance. Penyimpanan persisten adalah perangkat penyimpanan data yang menyimpan data setelah daya ke perangkat dimatikan. Terkadang, ini juga disebut penyimpanan non-volatile

Setiap volume Amazon EBS direplikasi secara otomatis dalam Availability Zone miliknya untuk melindungi Anda dari kegagalan komponen. Penyimpanan ini dirancang untuk ketersediaan dan ketahanan yang tinggi. Volume Amazon EBS menawarkan kinerja konsisten dan berlatensi rendah yang diperlukan untuk menjalankan beban kerja Anda

> Opsi penyimpanan AWS: penyimpanan blok vs penyipanan objek

  - Penyimpanan Blok
    - mengubah satu blok (bagian dari file) yang berisi karakter
  - Penyimpanan Objek
    - seluruh file harus dimutakhirkan

Amazon EBS memungkinkan Anda membuat volume penyimpanan individu dan melampirkannya ke Amazon EC2 instance. Amazon EBS menawarkan penyimpanan tingkat blok, tempat volume direplikasi secara otomatis dalam Availability Zone-nya. Amazon EBS dirancang untuk menyediakan penyimpanan tingkat blok yang tahan lama dan dapat dilepas (seperti hard drive eksternal) untuk Amazon EC2 instance. Karena dipasang secara langsung pada instans, volume tersebut dapat menyediakan latensi yang sangat rendah di antara tempat penyimpanan data dan tempat volume tersebut mungkin digunakan pada instans

Penggunaan volume Amazon EBS meliputi:
- Volume boot dan penyimpanan untuk Amazon EC2 instance
- Penyimpanan data dengan sistem file
- Hostbasis data
- Aplikasi perusahaan

> **Fitur Amazon EBS**
  - Snapshot
    - snapshot waktu tertentu
    - membuat ulang volume baru kapan saja
  - Enkripsi
    - volume Amazon EBS terenkripsi
    - tanpa biaya tambahan
  - Elastisitas
    - meningkatkan kapasitas
    - mengubah ke jenis yang berbeda

> Amazon EBS: Volume, IOPS, dan harga
  - Volume
    - volume amazon EBS bertahan secara independen dari instans
    - semua jenis volume dikenakan biaya dengan jumlah yang disediakan per bulan
  - IOPS
    - SSD tujuan umum:
      - dikenakan biaya dengan jumlah yang disediakan dalam GB per bulan sampai 
        penyimpanan dilepaskan
    - Magnetis:
      - dikenakan biaya dengan jumlah permintaan ke volume
    - SSD Provesioned IOPS
      - dikenakan biaya dengan jumlah yang disediakan di IOPS (dikalikan dengan presentase 
        hari yang disediakan untuk bulan tersebut) 

> Amazon EBS: Snapshot dan transfer data
  - Snapshot
    - biaya tambahan snapshot Amazon EBS ke Amazon S3 adalah per GB-bulan dari data yang 
      disimpan
  - Transfer data
    - transfer data masuk gratis
    - transfer data di seluruh wilayah terkena biaya
      
### Amazon Simple Storage Service (Amazon S3)

**Amazon S3** adalah penyimpanan tingkat objek, yang artinya jika Anda ingin 
mengubah satu bagian file, Anda harus melakukan perubahan lalu mengunggah ulang 
seluruh file yang diubah. Amazon S3 menyimpan data sebagai objek dalam sumber daya 
yang dikenal sebagai bucket.

Data yang Anda simpan di Amazon S3 tidak terkait dengan server tertentu, dan Anda 
tidak perlu mengelola infrastruktur sendiri. Anda dapat menempatkan objek ke 
Amazon S3 sebanyak yang Anda inginkan. Amazon S3 menyimpan triliunan objek dan 
secara teratur mencapai jutaan permintaan per detik.

> **kelas penyimpanan Amazon S3**
  - Amazon S3 Standard
  - Amazon S3 Intelligent-Tiering
  - Amazon S3 Standard-Infrequent Access (Amazon S3 Standard-IA)
  - Amazon S3 One Zone-Infrequent Access (Amazon S3 One Zone-IA)
  - Amazon S3 Glacier
  - Amazon S3 Glacier Deep Archive

Fleksibilitas untuk menyimpan jumlah data yang hampir tidak terbatas ini—dan untuk 
mengakses data tersebut dari mana saja—berarti bahwa Amazon S3 cocok untuk berbagai 
skenario.
Sekarang Anda akan mempertimbangkan beberapa kasus penggunaan untuk Amazon S3:
- Sebagai lokasi untuk data aplikasi apa pun, bucket Amazon S3 menyediakan lokasi bersama 
  untuk menyimpan objek yang dapat diakses oleh setiap instans aplikasi Anda—termasuk 
  aplikasi di Amazon EC2 atau bahkan server tradisional. Fitur ini dapat berguna untuk 
  file media yang dihasilkan pengguna, log server, atau file lain yang harus disimpan 
  aplikasi Anda di lokasi umum.
- Untuk hosting web statis, bucket Amazon S3 dapat melayani konten statis situs web Anda, 
  termasuk HTML, CSS, JavaScript, dan file lainnya.
- Daya tahan tinggi Amazon S3 membuatnya menjadi kandidat yang baik untuk menyimpan 
  cadangan data Anda. Untuk ketersediaan yang lebih besar dan kemampuan pemulihan 
  bencana, Amazon S3 bahkan dapat dikonfigurasi untuk mendukung replikasi antarwilayah 
  sehingga data dalam bucket Amazon S3 di satu Wilayah dapat secara otomatis direplikasi 
  ke Wilayah Amazon S3 lain.

> **skenario umum Amazon S3**
  - cadangan dan penyimpanan  : Menyediakan layanan pencadangan dan penyimpanan data 
                                untuk pengguna lain
  - hosting aplikasi          : Menyediakan layanan yang men-deploy, menginstal, dan 
                                mengelola aplikasi web
  - hosting media             : Membangun infrastruktur redundan, dapat diskalakan, dan 
                                tersedia dengan sangat baik yang dapat meng-host unggahan 
                                dan unduhan video, foto, atau musik
  - penyajian perangkat lunak : Meng-hostaplikasiperangkatlunakyang dapat di unduh 
                                pelanggan.

> **harga Amazon S3**
  - harga bayar apa yang di gunakan, termasuk:
    - GB per bulan
    - transfer OUT ke wilayah lain
    - permintaan PUT, COPY, POST, LIST, dan GET
  - tidak membayar untuk:
    - transfer IN ke Amazon S3
    - transfer OUT dari Amazon S3 ke Amazon CloudFRont atau Amazon EC2 di wilayah yang 
      sama

> **harga penyimpanan Amazon S3**
  - jenis kelas penyimpanan:
    - penyimpanan standar dirancang untuk:
      - daya tahan sebesar 99,999999999%
      - ketersediaan sebesar 99,99%
    - S3 Standart-Infrequent Access (S-IA) dirancang untuk:
      - daya tahan sebesar 99,999999999%
      - ketersediaan sebesar 99,99%
  - jumlah penyimpanan
    - jumlah dan ukuran objek
  - permintaan:
    -jumlah dan jenis permintaan (GET, PUT, COPY)
    - jenis permintaan:
      - tarif yang berbeda pada jumlah data yang ditransfer keluar dari wilayah Amazon S3
        - transfer data masuk gratis, tetapi akan dikenakan biaya untuk data yang 
          ditransfer keluar
      
### Amazon Elastic File System (Amazon EFS)

## ☁️ knowledge


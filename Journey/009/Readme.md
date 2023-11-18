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
  - tempat penyimpanan instans (penyimpanan sementara), Amazon EBS, Amazon EFS, Amazon S3, 
    dan Amazon S3 Glacier
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

### Use Case

### Cloud Research

## ☁️ knowledge


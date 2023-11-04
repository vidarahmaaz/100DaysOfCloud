## Apa yang akan kita pelajari???
  Topik:
  - Dasar Dasar Jaringan             
  - Amazon VPC (amazon virtual private cloud)
  - Jaringan VPC
  - Keamanan VPC
  - Amazon Route 53
  - Amazon CloudFront

## Dasar-Dasar Jaringan
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

## Amazon VPC

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

  Tabel ruteberisi sekumpulan aturan (disebutrute)yang mengarahkan lalu lintas jaringan 
  dari subnet Anda. Setiap rute menentukan tujuandan target. Tujuan adalah blok CIDR 
  tujuan tempat Anda ingin mengarahkan lalu lintas dari subnet
  
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

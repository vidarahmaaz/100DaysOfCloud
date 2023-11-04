### Keamanan AWS Cloud
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
  - AWS Shieldadalah layanan perlindungan distributed denial of service (DDoS) terkelola 
    yang melindungi aplikasi yang berjalan di AWS. AWS Shield menyediakan deteksi yang 
    selalu aktif dan mitigasi inline otomatis
  - Amazon Chimeadalah layanan komunikasi bagi Anda untuk rapat, mengobrol, dan telepon 
    bisnis di dalam dan di luar organisasi Anda, semuanya dengan satu aplikasi.Ini adalah 
    layanan komunikasi bayar sesuai pemakaian tanpa biaya awal, komitmen, atau kontrak 
    jangka panjang

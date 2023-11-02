**Add a cover photo like:**
![placeholder image](https://via.placeholder.com/1200x600)

# CLOUD COMPUTING [CHAPTER 2]

## Topik yang akan kita pelajari 
   - Dasar-Dasar Harga

## Dasar-Dasar Harga
   Model harga AWS
   - Komputasi : dikenai biaya per jam/detik, bervariasi sesuai tipe instans [hanya linux]
   - Penyimpanan : dikenai biaya biasanya per GB
   - Transfer Data : data keluar dijumlahkan dan dikenai biaya, data masuk tidak dikenai biaya 
                     dengan beberapa pengecualian, dikenai biaya biasanya pe GB 
                      
## Bagaimana cara membayar AWS?
   AWS menawarkan berbagai layanan komputasi cloud. Untuk setiap layanan, Anda membayar persis 
   dengan jumlah sumber daya yang benar-benar Anda perlukan. Model harga bergaya utilitas ini 
   meliputi:
   - bayar sesuai yang anda gunakan
   - bayar lebih sedikit ketika anda melakukan pemesanan
   - bayar lebih sedikit saat anda menggunakan lebih banyak
   - bayar jauh lebih sedikit seiring berkembangnya AWS

   Manfaat lain dari pertumbuhan AWS adalah bahwa sumber daya berperforma lebih tinggi di masa 
   depan akan menggantikan yang ada saat ini tanpa biaya tambahan
   - harga khusus : penuhi berbagai kebutuhan melalui harga khusus, tersedia untuk proyek bervolume 
                    tinggi dengan persyaratan yang unik
   - AWS tingkat gratis : AWS menawarkan tingkat penggunaan gratis (AWS Tingkat Gratis) untuk 
                          pelanggan baru hingga 1 tahun. AWS Tingkat Gratis berlaku untuk layanan 
                          dan opsi tertentu. Jika Anda adalah pelanggan baru AWS, Anda dapat 
                          menjalankan instans mikro T2 Amazon Elastic Compute Cloud (Amazon EC2) 
                          selama satu tahun, sekaligus menggunakan tingkat penggunaan gratis untuk 
                          Amazon S3, Amazon Elastic Block Store (Amazon EBS), Elastic Load 
                          Balancing, transfer data AWS, dan layanan AWS lainnya
   - layanan tanpa biaya : amazon vpc, elastic beanstalk, auto scaling, aws cloudformation, aws 
                           identity and access management (IAM)

## On-premise versus cloud
   

- ✍️ Document your trial and errors. Share what you tried to learn and understand about the cloud topic or while completing micro-project.
- 🖼️ Show as many screenshot as possible so others can experience in your cloud research.

## Try yourself

✍️ Add a mini tutorial to encourage the reader to get started learning something new about the cloud.

### Step 1 — Summary of Step

![Screenshot](https://via.placeholder.com/500x300)

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
  - Setiap Availability Zone adalah partisi yang sepenuhnya terisolasi dari infrastruktur AWS

  > Pusat data AWS
  - Pusat data AWS dirancang demi keamanan
  - Pusat data adalah tempat data berada dan pemrosesan data terjadi
  - Setiap pusat data memiliki daya, jaringan, dan konektivitas berlebih, dan ditempatkan di 
    fasilitas yang terpisah
  - Pusat data biasanya memiliki 50.000 sampai 80.000 server fisik

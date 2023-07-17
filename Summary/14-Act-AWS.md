
# Ikhtisar Pengoptimalan dan Ringkasan

Pada modul kali ini, kita telah belajar banyak, mulai dari mengulas arsitektur hingga cara-cara yang dapat digunakan untuk mengoptimalkan arsitektur cloud di AWS. Mari kita uraikan:

1. Kita telah mengulas arsitektur yang telah kita bangun melalui beberapa pertanyaan secara arsitektur. Dengan pertanyaan-pertanyaan tersebut, kita bisa semakin menyempurnakan arsitektur kita.

2. Kita juga telah melihat beberapa cara yang dapat membuat arsitektur kita semakin optimal, mulai dari mengubahnya menjadi loosely coupled, memanfaatkan model penetapan harga di EC2, mengubah arsitektur menjadi lebih tangguh, dan mengetahui beberapa praktik terbaik untuk membuat sistem di AWS.

## Praktik Terbaik untuk Membuat Sistem di AWS
Oke, sampai tahap ini kita telah melihat beberapa ulasan dan cara yang dapat mengoptimalkan arsitektur cloud. Walaupun begitu, Anda pun harus tetap mengetahui beberapa praktik terbaik yang dapat diterapkan saat mendesain atau membuat sistem di AWS, antara lain:

1. **Perhatikan skalabilitas** : AWS memiliki kemampuan untuk scale up maupun scale out. Pastikan Anda mengerti dan memanfaatkan keduanya dengan benar. 

2. **Automasikan lingkungan Anda** : Manfaatkan layanan-layanan AWS yang dapat membuat lingkungan secara otomatis, seperti AWS CloudFormation, AWS Elastic Beanstalk, dsb.

3. **Gunakan sumber daya sekali pakai** : Jika ada sumber daya di sistem Anda yang tidak terpakai (idle), pastikan apakah memungkinkan untuk diganti dengan sumber daya sekali pakai (disposable) atau dapat dimatikan saat tak terpakai seperti AWS Lambda.

4. **Pastikan komponen Anda loosely coupled** : Manfaatkan layanan AWS seperti SQS, SNS, dsb untuk membebaskan komponen sistem dari ketergantungan atau tightly coupled.

5. **Desain service, bukan server** : Ingat! Di AWS, Anda tidak perlu memikirkan hal-hal yang berkaitan dengan perangkat keras. Fokuskan diri Anda pada pengembangan aplikasi, bukan infrastruktur yang mendasarinya.

6. **Pilih solusi database yang tepat** : AWS memiliki layanan database berbasis SQL dan NoSQL yang bervariasi sesuai kebutuhan Anda. Jadi, pilihlah layanan database yang tepat.

7. **Hindari titik kegagalan tunggal** : Setiap layanan di AWS memiliki kemampuan untuk menghindari titik kegagalan tunggal (suatu komponen yang jika gagal, ia akan memiliki potensi menghentikan keseluruhan sistem). Pastikan Anda mengerti dan memanfaatkan hal ini.

8. **Optimasi biaya** : AWS didesain agar Anda dapat menjalankan sistem secara optimal dan hemat biaya. Tapi pastikan bahwa Anda juga memanfaatkan hal ini.

9. **Gunakan caching** : Caching akan sangat meningkatkan performa layanan sistem Anda.

10. **Amankan infrastruktur di setiap lapisan** : Keamanan sistem Anda adalah tanggung jawab Anda sendiri. Maka dari itu, pastikan Anda mengamankan infrastruktur Anda di setiap lapisannya. Misal pada lapisan jaringan, Anda menggunakan security group dan network ACL.

Ingat! Untuk memastikan lingkungan Anda telah menerapkan praktik terbaik dari AWS, gunakanlah AWS Well-Architected Tool. Tentu Anda masih ingat kan dengan layanan tersebut? Layanan tersebut telah kita bahas di modul pertama dari kelas ini. 

AWS Well-Architected Tool adalah tool gratis yang tersedia di AWS Management Console untuk membantu Anda dalam mengulas dan membandingkan beban kerja dengan praktik terbaik terbaru terkait arsitektur dari AWS. Tentu, praktik terbaik tersebut mengacu pada AWS Well-Architected Framework.
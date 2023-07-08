## Ikhtisar AWS Identity and Access Management (IAM)

INGATLAH! Jika ada satu hal yang bisa Anda ambil dari modul ini, jangan gunakan root account di lingkungan Production. Segera buat IAM User dan delegasikan akses admin ke akun ini, kemudian jaga akses ke root account secara ketat (atau Anda juga dapat menyimpan dan sebisa mungkin untuk tidak menggunakannya). Informasi lebih jauh untuk praktik keamanan root account dan juga langkah-langkah mengamankan resource AWS di akun Anda dapat dibaca lebih lanjut di tautan ini 

[Security best practices in IAM](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html)


    Alright. Di modul ini, kita telah mempelajari beberapa hal, antara lain:

1. Identity and Access Management (IAM) di AWS akan sangat membantu kita dalam memastikan keamanan dari aplikasi dan data. 

2. Kita bisa menggunakan IAM User, Group, dan Role untuk memudahkan kita mengorganisasi akses dan keamanan di dalam akun AWS.

3. Untuk mengelola akses, kita bisa menggunakan Policy & Permission. Policy dibuat untuk diasosiasikan/dikaitkan dengan IAM Identity atau Resources. AWS akan  mengevaluasi Policy ini saat ada permintaan dari identity principal atau resources. Sementara itu, permission akan menentukan apakah permintaan/request 5. tersebut diperbolehkan atau dilarang.

4. Selain menggunakan akun IAM User, kita dapat menggunakan Identity Provider lain misalnya dari amazon.com, google, maupun facebook sebagai pengganti IAM User.
Kita juga telah belajar mengenai AWS Organizations dan strukturnya, seperti root, OU, dan policy.
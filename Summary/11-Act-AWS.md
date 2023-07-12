# Ikhtisar Membangun Decoupled Architecture

Di modul ini kita telah mempelajari mengenai tiga jenis layanan dari AWS yang memungkinkan kita memisahkan (decouple) arsitektur menjadi komponen-komponen mandiri sehingga dapat beroperasi secara independen. 

Ketiga Layanan tersebut adalah Amazon Simple Queue Service (Amazon SQS), Amazon Simple Notification Service (Amazon SNS), dan Amazon MQ.

Amazon MQ, Amazon SQS, dan Amazon SNS adalah layanan perpesanan (messaging) yang cocok untuk siapa pun mulai dari startup hingga perusahaan yang sudah besar. Tabel di bawah ini menunjukkan perbedaan dan penggunaan ketiga layanan Message Broker dari AWS. 

Amazon MQ | Amazon SQS dan Amazon SNS
 — — — — — — | — — — — — — -
Untuk migrasi aplikasi | Untuk aplikasi cloud native
Banyak fitur | Unlimited throughput
Biaya per jam dan biaya per GB | Biaya per request
Bisa melakukan Pub/Sub | Tidak ada Pub/Sub di SQS, tetapi Anda bisa melakukan Pub/Sub di SNS


Jika Anda menggunakan messaging dengan aplikasi yang sudah ada dan ingin memindahkannya ke cloud dengan cepat dan mudah, maka pertimbangkanlah Amazon MQ.

Amazon MQ mendukung API dan protokol standar yang terbuka sehingga Anda dapat beralih dari message broker pesan berbasis standar ke Amazon MQ tanpa menulis ulang kode pesan di aplikasi Anda. 

Namun, jika Anda membangun aplikasi baru di cloud, maka gunakanlah Amazon SQS dan Amazon SNS. SQS adalah layanan antrean pesan (message queue), sedangkan SNS adalah layanan topic. Kedua layanan tersebut sangat ringan dan terkelola sepenuhnya yang berskala hampir tak terbatas dan menyediakan API sederhana serta mudah digunakan. 

Anda dapat menggunakan Amazon SQS dan Amazon SNS untuk decoupling dan scaling terhadap microservice, sistem terdistribusi, dan aplikasi serverless.
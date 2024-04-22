# Tutorial 8 Publisher

**a. How many data your publlsher program will send to the message broker in one
run?**

Berdasarkan code pada main function di file main.rs, dibuat sebuah publisher dimana publisher tersebut akan mengirimkan 5 pesan ke message broker. Pengiriman pesan oleh publisher ditandai oleh adanya pemanggilan fungsi `publish_envent` sebanyak 5 kali.

**b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
program, what does it mean?**

Url atau connection string yang digunakan oleh publisher dan subscriber sama berarti baik publisher dan subscriber terhubung ke message broker yang sama. Dengan menggunakan connection string yang sama, publisher dan subscriber dapat berkomunikasi pada message broker yang sama dan memastikan mereka berkomunikasi di sistem yang sama. Dimana amqp merujuk pada jenis protokol yang digunaka, pada kasus ini AMQP. Dan bagian guest:guest@localhost:5672 memiliki arti yang sama dengan penjelasan pada bagian subscriber sebelumnya.

**Running RabbitMQ as message broker**

![alt text](image-1.png)

**Sending and processing event**
![alt text](image-2.png)

Ketika publisher dijalankan,publisher akan mengirimkan 5 event atau pesan ke message broker.Subscriber kemudian menerima pesan ini melalui message broker dan menampilkan pesan tersebut di console seperti gambar diatas.

**Monitoring chart based on publisher**
![alt text](image-3.png)

Pada gambar ke 2. terlihat bahwa terjadi peningkatan message dalam suatu interval waktu.Hal ini berkaitan dengan publisher yang dijalankan menggunakan cargo run sebelumnya. Gambar tersebut menunjukkan bahwa setiap kali publisher dijalankan terjadi peningkatan message rate pada rabbitMQ.

**Simulation slow subscriber**
![alt text](image-4.png)

Pada gambar diatas terlihat bahwa, pada suatu waktu, terdapat 20 message pada queue. Hal ini terjadi karena subscriber memerlukan waktu yang lama untuk mengelola tiap event atau pesan dibandingkan publisher mengirim event atau pesan sehingga terjadi penumpukan messag.

# Tutorial 8 Publisher

** a. How many data your publlsher program will send to the message broker in one
run? **

Berdasarkan code pada main function di file main.rs, dibuat sebuah publisher dimana publisher tersebut akan mengirimkan 5 pesan ke message broker. Pengiriman pesan oleh publisher ditandai oleh adanya pemanggilan fungsi `publish_envent` sebanyak 5 kali.

** b. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber
program, what does it mean? **

Url atau connection string yang digunakan oleh publisher dan subscriber sama berarti baik publisher dan subscriber terhubung ke message broker yang sama. Dengan menggunakan connection string yang sama, publisher dan subscriber dapat berkomunikasi pada message broker yang sama dan memastikan mereka berkomunikasi di sistem yang sama. Dimana amqp merujuk pada jenis protokol yang digunaka, pada kasus ini AMQP. Dan bagian guest:guest@localhost:5672 memiliki arti yang sama dengan penjelasan pada bagian subscriber sebelumnya.

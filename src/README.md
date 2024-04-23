a. what is amqp?

Amqp adalah Advanced Message Queuing Protocol. Aplikasi client untuk berkomunikasi dengan aplikasi server yang mengirimkan data berbasis middleware. Middleware ini digunakan sebagai interface data yang dibutuhkan oleh client.

b. what it means? guest:guest@localhost:5672 , what is the first quest, and what is
the second guest, and what is localhost:5672 is for? 

- `guest` pertama adalah username untuk autentikasi.
- `guest` kedua adalah sebagai kata sandi untuk autentikasi.
- `localhost` adalah hostname atau alamat IP dimana komunikasi akan berjalan. 
- `5672` adalah nomor portnya.

![](high_load.png)

Banyaknya total antrian yang terjadi kurang lebih 10. `cargo run` dirun 2 kali yang seharusnya dijalankan dalam 10 detik (5 pesan per run x 2 kali run). Namun, karena  melakukan `cargo run` secara sequential, maka terdapat delay dan hanya tercapture antrian maksimal sebesar 10 dalam satu waktu.
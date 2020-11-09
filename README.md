# bookapp
NAMA : AMANDA RIZKY ROSSITIKA
NIM : 185150700111016

Pada praktikum kali ini, saya mengetahui tentang bagaimana cara untuk instalilasi dan menjalankan aplikasi Lumen, implementasi Migration, Seeder, Model, dan Controller. Untuk menjalankan praktikum ini, saya menggunakan aplikasi Visual Code, XAMPP, Postman, dan Phpmyadmin. 

MVC adalah konsep arsitektur dalam pembangunan aplikasi berbasis web yang membagi aplikasi web menjadi 3 bagian besar. Yang mana setiap bagian memiliki tugas-tugas serta tanggung jawab masing-masing. Tiga bagian tersebut adalah: model, view dan controller.

Model Berfungsi untuk mengatur, menyiapkan, memanipulasi dan mengorganisasikan data (dari database) sesuai dengan instruksi dari controller. Lalu View, berfungsi untuk menyajikan informasi (yang mudah dimengerti) kepada user sesuai dengan instruksi dari controller.Sedangkan controller berfungsi untuk mengatur apa yang harus dilakukan model, dan view mana yang harus ditampilkan berdasarkan permintaan dari user. Namun, terkadang permintaan dari user tidak selalu memerlukan aksi dari model. Misalnya seperti menampilkan halaman form untuk registrasi user.

Beberapa framework sudah menerapkan proses MVC, satu di antaranya adalah Laravel. Dengan Laravel, konsep MVC sangat dimudahkan karena terdapat fungsi-fungsi khusus yang memperpendek baris dan kode.

Controller yaitu berisi method-method yang berisi perintah yang harus dilakukan pada suatu method. Setelah Route menghubungkan ke controller dan method mana yang akan dituju, method suatu controller akan mengembalikan nilai atau tujuan url yang akan dituju. Pada laravel, direktori controller berada di app>Http>Controller. 
Untuk membuat controller menuliskan perintah di terminal yaitu : $router->get('books','BooksController@index');

Model merupakan salah satu komponen MVC yang berhubungan langsung dengan database. Di database sendiri model dipresentasikan tabel-tabel yang nantinya diisi dengan data. Model berisi atribut yang nantinya atribut tersebut menjadi kolom pada tabel database. 

Migration adalah sebuah fitur yang ada pada laravel yang merupakan Control Version System untuk database. Dengan menggunakan migration memungkinkan untuk mengelola database dengan lebih mudah. 
Untuk membuat migration, pertama kita menjalankan perintah untuk membuat tabel php artisan make:migration create_books_table --create=books. Jika sudah, kita membuat skema terlebih dahulu. Setelah membuat Skema, lalu kita menjalankan perintah di terminal php artisan mograte

Seeder dapat digunakan untuk membuat sample data dengan command yang sederhana. Maka kita tidak perlu repot untuk melakukan penginputan data secara berulang pada saat proses testing. Hal ini tentunya akan mempercepat proses development yang anda lakukan. 
Untuk melakukan seeding ke database, kita perlu menjalankan perintah php artisan db:seed

Setelah menjalankan semua perintah, kemudian akses localhost:8000/books untuk menyesuaikan 
hasil dengan data yang disimpan pada database.

CHALLANGE (MELANJUTKAN READ.ME)

GET digunakan untuk mengambil data dari server di sumber daya yang ditentukan . Misalnya, kita memiliki API dengan /userstitik akhir. Membuat permintaan GET ke titik akhir itu akan menghasilkan daftar semua pengguna yang tersedia. Karena permintaan GET hanya meminta data dan tidak mengubah sumber daya apa pun, itu dianggap sebagai metode yang aman dan idempoten .

POST digunakan untuk mengirim data ke server API untuk membuat atau menguduskan sumber daya. Data yang dikirim ke server disimpan di badan permintaan permintaan HTTP. Perlu diperhatikan bahwa POSTpermintaan tidak bersifat idempoten . Ini mengubah data di server backend (dengan membuat atau memperbarui sumber daya), berlawanan dengan GETpermintaan yang tidak mengubah data apa pun. 

PUT digunakan untuk mengirim data ke API untuk memperbarui atau membuat sumber daya . Perbedaannya adalah bahwa permintaan PUT bersifat idempoten . Artinya, memanggil permintaan PUT yang sama beberapa kali akan selalu menghasilkan hasil yang sama . Sebaliknya, memanggil permintaan POST berulang kali memiliki efek samping dari pembuatan sumber daya yang sama beberapa kali. Umumnya, saat PUT membuat sumber daya, server akan merespons dengan 201( Created), dan jika permintaan mengubah sumber daya yang ada, server akan mengembalikan 200( OK) atau 204( No Content).

Metode DELETE adalah menghapus sumber daya di URL tertentu . Metode ini adalah salah satu metode yang lebih umum di RESTful API. Jika pengguna baru dibuat dengan permintaan POST ke /users, dan itu dapat diambil dengan GETpermintaan ke /users/{{userid}}, maka membuat DELETEpermintaan untuk /users/{{userid}}akan menghapus pengguna itu sepenuhnya.




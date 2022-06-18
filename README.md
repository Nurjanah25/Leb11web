# lab11web

### Nama  : Nurjanah
### Kelas : TI.20.D1
### NIM   : 312010035

### Praktikum 11: PHP Framework (Codeigniter)
### Langkah-langkah
1. Mengaktifkan Ekstensi
- Aktifkan ekstensi tersebut melalui XAMPP Control Panel pada bagian Apache dengan cara klik Config -> PHP.ini seperti berikut.
![1](https://user-images.githubusercontent.com/101665497/174443787-0fa87fc2-008c-49cc-b8ce-eb271eac40f4.png)

- Lalu pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan seperti berikut. Kemudian simpan kembali filenya dan restart Apache web server.
![1](https://user-images.githubusercontent.com/101665497/174443830-ffb2af8a-74ac-4d33-9da6-ef855b2d2314.png)

2. Instalasi CodeIgniter 4
- Codeigniter dapat didownload dari website https://codeigniter.com/download

- Extrak file zip Codeigniter ke direktori htdocs/lab11_php_ci.

- Ubah nama directory framework-4.x.xx menjadi ci4.

- Buka browser dengan alamat http://localhost/lab11web_ci/ci4/public/ Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara manual seperti berikut.

![image](https://user-images.githubusercontent.com/101665497/174444046-d379bded-1024-403a-b3ba-ccae7c8cc74b.png)

3. Menjalankan CLI (Command Line Interface)
Codeigniter 4 menyediakan CLI untuk mempermudah proses development. Untuk mengakses CLI buka terminal/command prompt, lalu arahkan lokasi direktori sesuai dengan direktori kerja project dibuat (C:\xampp\htdocs\Lab11web_ci\ci4). Kemudian setelah itu jalankan perintah untuk memanggil CLI Codeigniter

![image](https://user-images.githubusercontent.com/101665497/174444056-feb46efb-747e-479f-82f0-06e082648416.png)

4.Mengaktifkan Mode Debugging Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program. Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan pesan kesalahan seperti berikut.

![image](https://user-images.githubusercontent.com/101665497/174444197-ae0d474e-98aa-4c68-b2bd-f730f14aaf8f.png)

Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya, maka perlu mengaktifkan mode debugging dengan mengubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development. Kemudian mengubah nama file env menjadi .env lalu setelah itu buka file tersebut dan ubah nilai variable CI_ENVORNMENT menjadi development. Setelah mengubah nilai konfigurasi pada environment variable CI_ENVIRONMENT menjadi development. maka hapus tanda tagar (#) pada awal baris CI_ENVIRONMENT. Dan yang terakhir, ubah kode pada file app/Controller/Home.php kemudian hilangkan titik koma (;) pada akhir kode seperti berikut.

![image](https://user-images.githubusercontent.com/101665497/174444240-e99d5613-a21f-40d6-8620-fc98ece92a3a.png)

Maka hasilnya akan terjadi error seperti berikut.

![image](https://user-images.githubusercontent.com/101665497/174444264-99c6ff1f-ae89-4331-a697-80f43f3f949d.png)

5.Membuat Route Baru. Menambahkan kode di dalam Routes.php seperti berikut.

![image](https://user-images.githubusercontent.com/101665497/174444426-5c9e672e-afeb-4a18-9178-b4d431b2a3b1.png)

Selanjutnya coba akses route yang telah dibuat dengan mengakses alamat url http://localhost:8080/about seperti berikut. Maka hasilnya akan terjadi error, yang artinya file/page tersebut tidak ada. Untuk dapat mengakses halaman tersebut, harus dibuat terlebih dahulu Contoller yang sesuai dengan routing yang dibuat yaitu Contoller Page.

![image](https://user-images.githubusercontent.com/101665497/174444509-cdf369b8-c705-499e-a03b-b85093887d77.png)

6.Membuat Controller Selanjutnya adalah membuat Controller Page. Buat file dengan nama page.php pada direktori Controller kemudian isi kodenya seperti berikut

![2](https://user-images.githubusercontent.com/101665497/174444681-acfc484a-797e-4015-931a-e1a02eaeb5aa.png)

7.Auto Routing Secara default fitur autoroute pada Codeigniter sudah aktif. Untuk mengubah status autoroute dapat mengubah nilai variablenya. Untuk menonaktifkan ubah nilai true menjadi false

![3](https://user-images.githubusercontent.com/101665497/174444730-aef03680-e5e0-4494-89ab-fed7b739a19a.png)

8.Membuat View Selanjutnya adalam membuat view untuk tampilan web agar lebih menarik. Buat file baru dengan nama about.php pada direktori view (app/view/about.php) kemudian isi kodenya seperti berikut. 

![image](https://user-images.githubusercontent.com/101665497/174444748-fc3f7b14-76d1-46bb-b028-bc77a8283b14.png)

Ubah method about pada class Controller Page menjadi seperti berikut: 
![image](https://user-images.githubusercontent.com/101665497/174444783-a2812276-ba1a-47cc-b88d-dbd96786d7c8.png)

Maka hasilnya akan seperti berikut: 
![image](https://user-images.githubusercontent.com/101665497/174444885-2ab32ab5-72f8-4f7b-90d5-9b23eab12e43.png)

9.Membuat Layout Web dengan CSS Pada dasarnya layout web dengan css dapat diimplementasikan dengan mudah pada codeigniter. Yang perlu diketahui adalah, pada Codeigniter 4 file yang menyimpan asset css dan javascript terletak pada direktori public.
Buat file css pada direktori public dengan nama style.css (copy file dari praktikum lab4_layout) Kita akan gunakan layout yang pernah dibuat pada praktikum 4.

![image](https://user-images.githubusercontent.com/101665497/174444927-9d662336-bca4-4cb1-a468-f2b810c5c88e.png)

Kemudian buat folder template pada direktori view kemudian buat file header.php dan footer.php 

![4](https://user-images.githubusercontent.com/101665497/174445001-8170127f-97d5-470c-b55b-f0d986a7d4c1.png)

![image](https://user-images.githubusercontent.com/101665497/174445025-d6a32053-cd20-4987-8184-e51209046377.png)

Maka hasilnya seperti berikut:

![image](https://user-images.githubusercontent.com/101665497/174445055-2f2f1558-4bc5-409b-895b-24e7c7e205ee.png)

- PERTANYAAN DAN TUGAS

Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang sama.

![5](https://user-images.githubusercontent.com/101665497/174445164-fe3bf484-e33e-4313-8abf-1cce0294cbc5.png)

![6](https://user-images.githubusercontent.com/101665497/174445205-56931fd6-6de3-44ec-9e9a-e2f581947f61.png)















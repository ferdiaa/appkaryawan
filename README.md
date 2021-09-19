## Tentang SMK

SMK merupakan aplikasi yang digunakan untuk mengelola karyawan oleh admin dibangun menggunakan Laravel dan MySQL.

EAMS is fast and easy to use and can be customized easily according to client project
SMK cepat dan mudah digunakan

![login](https://user-images.githubusercontent.com/44310818/133906479-d1d9e7f2-ed43-45a3-945f-b0ba652f3d19.png)

<p align="center">Login Page</p>

![admin](https://user-images.githubusercontent.com/44310818/133907508-3a430937-2c72-4d1a-98be-e340c765cf7e.jpeg)

<p align="center">Admin Dashboard</p>

![Web capture_19-9-2021_24659_127 0 0 1](https://user-images.githubusercontent.com/44310818/133907566-980d5c33-ff32-4430-b916-3d748166701c.jpeg)

<p align="center">Karyawan Dashboard</p>


### Fungsi

Dalam Aplikasi terdapat dua aktor karyawan dan admin.
**Karyawan** dapat:
- Kehadiran module
	- Isi kehadiran [Images menggunakan 127.0.0.1 sebagai IP karena digunakan di lokal komp.]
		- Dapat mencatat kehadiran berdasarkan lokasi karyawan pastikan allow access lokasi pada browser.
	- isi kehadiran

	![Web capture_20-9-2021_24816_127 0 0 1](https://user-images.githubusercontent.com/44310818/133907599-92d61407-442d-487f-b2dc-29b1e2a3d783.jpeg)
	<p align="center">Isi Kehadiran</p>
  
	![Web capture_20-9-2021_24848_127 0 0 1](https://user-images.githubusercontent.com/44310818/133907621-d0bea13a-3ee9-4674-8e93-8a7728ed4f1d.jpeg)
	<p align="center">Isi kehadiran masuk</p>
  
	![Web capture_19-9-2021_24741_127 0 0 1](https://user-images.githubusercontent.com/44310818/133907635-2def6d2a-2d82-4012-8609-04284c161c96.jpeg)
	<p align="center">Isi Absensi Keluar</p>
- Izin Module
	- Submit Izin
	- Review Status Izin
- Terlambat Module
	- Submit alasan terlambat
	- Review status submit
- Saya Module
	- Melihat Hari Libur

**Admin** dapat:
- Karyawan module
	- Menambah karyawan baru
	![Web capture_19-9-2021_24410_127 0 0 1](https://user-images.githubusercontent.com/44310818/133907676-e8221d99-a71c-427e-8a3d-c8608f9e4680.jpeg)
	<p align="center">Profil Karyawan</p>

	- Monitoring kehadiran karyawan
![Web capture_19-9-2021_2455_127 0 0 1](https://user-images.githubusercontent.com/44310818/133907713-f98d3681-4443-407e-8d1b-f5b96ce494de.jpeg)
	<p align="center">Profil Karyawan</p>
- Autorisasi module
	- Melakukan persutujuan atau penolakan dari izin karyawan
	- Melakukan persetujuan atau penolakan dari alasan keterlambatan karyawan
- Hari libur module
	- menambah, merubah, menghapus berdasarkan regulasi perusahaan

### Instalasi

Untuk menjalankan project pertama jalankan console

```console
composer install
```

Setelah berhasil copy dan rename env.example mendaji env.

```console
cp .env.example .env
```

Kemudian generate key

```console
php artisan key:generate
```
Setelah itu import database attend2.sql ke phpmyadmin, dan ubah dalam file .env menjadi

DB_CONNECTION=mysql

DB_HOST=127.0.0.1

DB_PORT=3306

DB_DATABASE=attend2(sesuaikan dengan nama database yang diimport)

DB_USERNAME=root(username default dari phpmyadmin)

DB_PASSWORD=


dan buka file config/database.php sesuaikan dengan file .env seperti dibawah


             'mysql' => [

            'driver' => 'mysql',
            
            'url' => env('DATABASE_URL'),
            
            'host' => env('DB_HOST', '127.0.0.1'),
            
            'port' => env('DB_PORT', '3306'),
            
            'database' => env('DB_DATABASE', 'attend2'),
            
            'username' => env('DB_USERNAME', 'root'),
            
            'password' => env('DB_PASSWORD', ''),
            
            'unix_socket' => env('DB_SOCKET', ''),
            
            'charset' => 'utf8mb4',
            
            'collation' => 'utf8mb4_unicode_ci',
            
            'prefix' => '',
            
            'prefix_indexes' => true,
            
            'strict' => true,
            
            'engine' => null,
            
            'options' => extension_loaded('pdo_mysql') ? array_filter([
            
                PDO::MYSQL_ATTR_SSL_CA => env('MYSQL_ATTR_SSL_CA'),
                
            ])
            

bisa dicek database menggunakan console
```console
php artisan migrate
```

tambah link public folder ke storage

```console
php artisan storage:link
```

```console
php artisan serve
```
admin login :

email : admin@gmail.com

pass  : admin


karyawan login

email : ferdi@gmail.com

pass  : ferdi123

Hope you like it

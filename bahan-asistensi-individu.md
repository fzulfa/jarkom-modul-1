## Penggunaan Wireshark ketika Mengakses FTP Server

1. Buka aplikasi Wireshark dan mulai mengcapture.
2. Akses FTP server yang berada di 10.151.36.30 dengan username 'jarkom' dan password 'ftpjarkom'. Hal ini bisa dilakukan dengan menggunakan aplikasi FileZilla atau lewat terminal Linux (supaya lebih keren). Untuk yang mencoba lewat command line, lakukan dengan mengetikkan perintah

```
$ ftp 10.151.36.30
```

Kemudian masukkan username lalu password. Anda bisa mencoba CLI apa saja yang bisa dilakukan lewat akses FTP. Misalkan `cd`, `ls`, `touch`, dll.

![AksesFTP](/images/ftp.png)

3. Coba unduh salah satu file yang berada pada direktori FTP. Untuk yang menggunakan terminal, perintah yang digunakan adalah

```
ftp> get [nama_file]
```

Lalu untuk keluar dari akses FTP bisa menggunakan perintah `bye` atau `exit`.

4. Sebutkan command apa saja yang muncul dari hasil packet capture beserta fungsinya. Coba juga gunakan display filter untuk memilih packet dengan protokol FTP saja. Berikut ini adalah contoh hasil packet capture ketika mengakses FTP server lewat terminal Linux.

![CaptureFTP](/images/ws-ftp.png)

## FYI gan

### Connections

Koneksi yang dilakukan dengan protokol HTTP sifatnya ada 2 macam: [http://whatis.techtarget.com/definition/persistent-connection-HTTP-persistent-connection](__Persistent__ dan __Non-Persistent__). Koneksi yang terbentuk ini ada 2 arah: dari Web Browser dan dari Web Server. Kebanyakan Web Browser mutakhir selalu menggunakan koneksi Persistent. Sedangkan Web Server ada yang menyediakan koneksi Persistent maupun non-Persistent, walaupun memang biasanya yang lebih banyak digunakan adalah yang Persistent. Jenis koneksi dari Web Server bisa diatur di file konfigurasinya, yang nanti mungkin akan kalian dapatkan di modul-modul selanjutnya.

- Web server yang menyediakan koneksi non-Persistent ketika kita lihat lebih detil isi paketnya kira-kira seperti ini:

![nonPersistent](/images/ws-nonpersistent.png)

- Sedangkan web server yang menyediakan koneksi Persistent, kurang lebih isi paketnya seperti ini:

![Persistent](/images/ws-persistent.png)

__Bisa temukan perbedaannya?__

### Authentication

Terdapat Web Server yang menyediakan fitur autentikasi ketika Web Browser akan mengakses sebuah halaman, salah satunya Apache. Apache memberikan pilihan jenis autentikasi: __Basic__ dan __Digest__. Dengan menjalankan Wireshark terlebih dahulu, coba kalian akses halaman `10.151.36.30/basic`, masukkan username 'jarkom' dan password 'basicjarkom'. Kemudian coba juga akses halaman `10.151.36.30/digest`, masukkan username 'jarkom' dan password 'jarkom'. Lihat paket yang ditangkap Wireshark, lalu jelaskan apa perbedaan Basic Authentication dan Digest Authentication!

- Contoh detil paket untuk basic authentication:
![BasicAuth](/images/ws-basic.png)

- Contoh detil paket untuk digest authentication:
![DigestAuth](/images/ws-digest.png)

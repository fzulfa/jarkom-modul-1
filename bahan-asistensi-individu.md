## Penggunaan Wireshark untuk Mengakses FTP Server

1. Buka aplikasi Wireshark dan mulai mengcapture.
2. Akses FTP server yang berada di 10.151.36.30 dengan username 'jarkom' dan password 'ftpjarkom'. Hal ini bisa dilakukan dengan menggunakan aplikasi FileZilla atau lewat terminal Linux (supaya lebih keren). Untuk yang mencoba lewat command line, lakukan dengan mengetikkan perintah

```
$ ftp 10.151.36.30
```

Kemudian masukkan username lalu password. Anda bisa mencoba CLI apa saja yang bisa dilakukan lewat akses FTP. Misalkan `cd`, `ls`, `touch`, dll.

![AksesFTP](/images/ftp.png)

3. Coba unduh salah satu file yang berada pada direktori FTP. Untuk yang menggunakan terminal, perintah yang digunakan adalah

```
get [nama_file]
```

Lalu untuk keluar dari akses FTP bisa menggunakan perintah `bye` atau `exit`.

4. Sebutkan command apa saja yang muncul dari hasil packet capture beserta fungsinya. Coba juga gunakan display filter untuk memilih packet dengan protokol FTP saja.

![CaptureFTP](/images/ws-ftp.png)


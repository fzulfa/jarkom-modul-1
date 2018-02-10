# MODUL 1 JARINGAN KOMPUTER 2018
## 1. Wire Crimping

Dalam membangun jaringan komputer, tentunya dibutuhkan segala hal yang dapat menghubungkan perangkat-perangkat komputer yang ada. Hingga saat ini, komponen paling fundamental dalam jaringan komputer adalah kabel. Sekalipun teknologi nirkabel sudah lama ditemukan dan dikembangkan, tapi peran kabel jaringan tetap belum bisa tergantikan. Oleh karena itu di sini kita akan belajar bagaimana membuat kabel jaringan (dalam hal ini kabel UTP) menjadi fungsional.

### 1.1. Kebutuhan

Peralatan dan bahan yang perlu dipersiapkan:
1. Tang Crimping

![Tang Crimping](/images/tang.jpg)

2. RJ-45

![RJ-45](/images/rj45.jpg)

3. Kabel UTP

![Kabel UTP](/images/kabelutp.jpg)

4. LAN Tester

![LAN Tester](/images/lantester.jpg)

### 1.2. Jenis-Jenis Pengkabelan

#### 1.2.1. Straight

Kabel straight merupakan kabel yang memiliki cara pemasangan yang sama antara ujung satu dengan ujung yang lainnya. Kabel straight digunakan __untuk menghubungkan 2 device yang berbeda__, misalnya antara switch dengan router dan komputer dengan switch. Urutan kabel straight jika dilihat dari sisi tembaga RJ-45 adalah seperti dibawah ini:

![Straight](/images/straight.jpg)

#### 1.2.2. Crossover

Kabel crossover merupakan kabel yang memiliki susunan berbeda antara ujung satu dengan ujung dua. Kabel crossover digunakan __untuk menghubungkan 2 device yang sama__. Jika dilihat dari sisi tembaga RJ-45, berikut susunan kabel crossover:

![Cross](/images/cross.jpg)

### 1.3. Cara Crimping

1. Mengupas kulit kabel selebar +-2 cm menggunakan tang crimping.

2. Menyusun rapi delapan kabel yang terdapat didalam kabel STP sesuai dengan jenis kabel mana yang ingin dibuat (straight atau cross).

3. Meluruskan kabel yang masih kusut.

4. Meratakan ujung kabel dengan memotong nya menggunakan tang crimping.

5. Memasukan kabel kedalam konektor RJ-45, pastikan ujung kabel menyentuh ujung RJ-45, dan jepitlah menggunakan tang crimping.

6. Lakukan hal serupa pada kedua ujung kabel.

7. Menguji menggunakan LAN tester, jika semua lampu menyala, berarti kabel tersebut telah di crimping dengan benar dan bisa digunakan.


## 2. WIRESHARK

Sebuah jaringan komputer dibangun dengan tujuan menghubungkan satu end-point dengan end-point lainnya. Tiap kali terjadi komunikasi antar perangkat dalam jaringan pasti melibatkan transaksi data yang dikirim dalam paket-paket jaringan. Struktur paket jaringan terdiri dari:

1. __*Header*__

Bagian header memuat instruksi tentang data yang dibawa oleh paket. Instruksi tsb di antaranya bisa meliputi:

Instruksi | Keterangan
--------- | ----------
_Panjang paket_ | Sebagian jaringan sudah memiliki panjang paket yang baku (fixed-length), sementara sebagian yang lain bergantung pada header untuk memuat informasi ini
_Sinkronisasi_ | Beberapa bit yang membantu paket mencocokkan jaringan yang dimaksud
_Nomor paket_ | Menunjukkan urutan dari total paket yang ada
_Protokol_ | Pada jaringan yang membawa lebih dari satu macam informasi, protokol ini menunjukkan jenis paket yang ditransmisikan, apakah termasuk e-mail, halaman web, atau yang lain
_Alamat tujuan_ | Ke mana paket dikirimkan
_Alamat asal_ | Dari mana paket dikirimkan

2. __*Payload*__

Payload juga disebut sebagai __*body*__ dari paket. Pada bagian inilah data yang akan dikirimkan lewat paket berada.

3. __*Trailer*__

Trailer, kadang-kadang disebut __*footer*__, biasanya memuat sepasang bit yang memberi sinyal pada perangkat penerima bahwa paket sudah mencapai ujungnya. Bisa juga trailer memuat semacam _error checking_.

### 2.1. Tujuan Penggunaan

### 2.2. Instalasi

### 2.3. Filters

Terdapat dua macam filter yang disediakan oleh Wireshark: __*Capture Filter*__ dan __*Display Filter*__.

#### 2.3.1. Capture Filter

- Definisi: Memilah paket yang akan ditangkap (_captured_). Artinya paket yang tidak memenuhi kriteria dibiarkan lewat tanpa ditangkap.
- Sintaks filter dapat terdiri dari 1 atau lebih __primitive__. Primitive sendiri biasanya terdiri dari sebuah __id__ (bilangan atau nama) yang didahului oleh 1 atau lebih jenis __qualifier__. Tapi perlu diingat bahwa dalam satu primitive tidak boleh ada 2 qualifier sejenis.
- Jenis qualifier:

	Qualifier | Keterangan | Contoh
	----------|--------|--------
	_type_ | Menentukan jenis id atau nama yang menjadi nilai filter | `host`, `net`, `port`, `portrange`
	_dir_ | Menentukan direction atau arah dari id | `src`, `dst`, dan lain-lain
	_proto_ | Menentukan protokol dari id | `tcp`, `udp`, `ether`, dan lain-lain.

- Sintaks filter dapat memuat operator, tanda kurung, negasi (`!` / `not`), dan konjungsi (`&&` / `and` atau `||` / `or`). Konjungsi digunakan untuk menghubungkan 2 primitive dalam satu sintaks.
- Contoh penggunaan filter dan maksudnya.

#### 2.3.2. Display Filter

- Definisi: Memilah paket yang akan ditampilkan (_displayed_) setelah sebelumnya ditangkap
	- Secara umum sintaks display filter terdiri dari `[protocol] [operator] [value]`
	- Sebagaimana capture filter, display filter juga bisa menggabungkan dua filter expression dengan logical operator:

		Logical Operator | Keterangan
		-----------------|-----------
		`and` atau `&&` | logical AND
		`or` atau `||` | logical OR
		`xor` atau `^^` | logical XOR
		`not` atau `!` | logical NOT
		`[...]` | substring operator
		`in` | membership operator
	
### 2.4. Export data hasil packet capture

### 2.5. HTTP basic + digest

### 2.6. HTTP request method GET + POST

### 2.7. FTP

## LATIHAN
1. Ketika mengakses suatu halaman web, berapakah port yang dituju oleh suatu paket?
2. Apa sajakah perbedaan ketika mengakses halaman utama website if.its.ac.id,
monta.if.its.ac.id, dan rbtc.if.its.ac.id? Jelaskan jawaban anda.
3. Ada berapa jumlah paket yang dikirimkan oleh web server ketika mengunduh file? Mengapa
terjadi yang seperti itu?
4. Dari hasil analisa paket, apa perbedaan ketika menggunakan persistent connection dan
non-persistent connection?
5. Apa perbedaan ketika autentikasi menggunakan method basic dengan digest?
6. Apa perbedaan ketika mengakses halaman web biasa dengan ketika proses login terjadi?
7. Apa saja yang selalu dikirimkan browser ke web server?
8. Apa perbedaan ketika mengakses suatu website dengan dan tanpa proxy?
9. Perintah apa saja yang dikirimkan oleh FTP client ketika login?
10. Perintah apa saja yang dikirimkan oleh FTP client ketika melihat isi direktori, upload, dan
download?
11. Perintah apa saja yang dikirimkan oleh FTP client ketika menyalin, memindahkan, dan
menghapus file?

## Referensi

https://computer.howstuffworks.com/question5251.htm

https://wiki.wireshark.org/

https://www.wireshark.org/docs/wsug_html_chunked/ChCapCaptureFilterSection.html

http://www.tcpdump.org/manpages/pcap-filter.7.html

https://www.wireshark.org/docs/wsug_html_chunked/ChWorkBuildDisplayFilterSection.html

https://wiki.wireshark.org/ProtocolReference

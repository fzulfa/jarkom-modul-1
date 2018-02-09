# Modul 1 Jaringan Komputer 2018

## 1. Wire Crimping

### 1.1. Kebutuhan

Peralatan dan bahan yang perlu dipersiapkan:

![Tang Crimping](/images/tang.jpg)
![RJ-45](/images/rj45.jpg)
![Kabel UTP](/images/kabelutp.jpg)
![LAN Tester](/images/lantester.jpg)

### 1.2. Jenis Kabel

#### 1.2.1. Straight

Kabel straight merupakan kabel yang memiliki cara pemasangan yang sama antara ujung satu dengan ujung yang lainnya. Kabel straight digunakan __untuk menghubungkan 2 device yang berbeda__, misalnya antara switch dengan router dan komputer dengan switch. Urutan kabel straight jika dilihat dari sisi tembaga RJ-45 adalah seperti dibawah ini:

#### 1.2.2. Crossover

Kabel crossover merupakan kabel yang memiliki susunan berbeda antara ujung satu dengan ujung dua. Kabel crossover digunakan __untuk menghubungkan 2 device yang sama__. Jika dilihat dari sisi tembaga RJ-45, berikut susunan kabel crossover:

### 1.3. Cara Crimping

1. Mengupas kulit kabel selebar +-2 cm menggunakan tang crimping.

2. Menyusun rapi delapan kabel yang terdapat didalam kabel STP sesuai dengan jenis kabel mana yang ingin dibuat (straight atau cross).

3. Meluruskan kabel yang masih kusut.

4. Meratakan ujung kabel dengan memotong nya menggunakan tang crimping.

5. Memasukan kabel kedalam konektor RJ-45, pastikan ujung kabel menyentuh ujung RJ-45, dan jepitlah menggunakan tang crimping.

6. Lakukan hal serupa pada kedua ujung kabel.

7. Menguji menggunakan LAN tester, jika semua lampu menyala, berarti kabel tersebut telah di crimping dengan benar dan bisa digunakan.


## 2. WIRESHARK

### Tujuan Penggunaan

### Instalasi

### Filters

Terdapat dua macam filter yang disediakan oleh Wireshark: Capture Filter dan Display Filter.

#### Capture Filter

- Definisi: Memilah paket yang akan ditangkap (captured). Artinya paket yang tidak memenuhi kriteria dibiarkan lewat tanpa ditangkap.
	- Sintaks filter dapat terdiri dari 1 atau lebih primitive. Primitive sendiri biasanya terdiri dari sebuah id (bilangan atau nama) yang didahului oleh 1 atau lebih macam qualifier. Tapi perlu diingat bahwa dalam satu primitive tidak boleh ada 2 qualifier sejenis.
	- Macam-macam qualifier:
		1. type		-> menentukan jenis id atau nama yang menjadi nilai filter. Contoh type adalah: host, net, port, portrange.
		2. dir		-> menentukan direction atau arah dari id. Di antara contoh dir adalah: src, dst, dan lain-lain.
		3. proto	-> menentukan protokol dari id. Contohnya adalah: tcp, udp, ether, dan lain-lain.
	- Sintaks filter dapat memuat operator, tanda kurung, negasi ('!' atau 'not'), dan konjungsi ('&&'/'and' atau '||'/'or'). Konjungsi digunakan untuk menghubungkan 2 primitive dalam satu sintaks.
	- Contoh penggunaan filter dan maksudnya.

#### Display Filter

- Definisi: Memilah paket yang akan ditampilkan (displayed) setelah sebelumnya ditangkap
	- Secara umum sintaks display filter terdiri dari [protocol] [operator] [value]
	- Sebagaimana capture filter, display filter juga bisa menggabungkan dua filter expression dengan logical operator:
		1. 'and' atau '&&'	-> logical AND
		2. 'or' atau '||'	-> logical OR
		3. 'xor' atau '^^'	-> logical XOR
		4. 'not' atau '!'	-> logical NOT
		5. [...]		-> substring operator
		6. 'in'			-> membership operator
	
### Export data hasil packet capture

### HTTP basic + digest

### HTTP request method GET + POST

### FTP

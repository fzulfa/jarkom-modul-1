# Modul 1 Jaringan Komputer

## 1. Wire Crimping

## 2. WIRESHARK

### Filters

	   Filter
       
       |
       
  -----------

  |		      |

Capture		Display

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
		5. [...]			-> substring operator
		6. 'in'				-> membership operator
	
### Export data hasil packet capture

### HTTP basic + digest

### HTTP request method GET + POST

### FTP

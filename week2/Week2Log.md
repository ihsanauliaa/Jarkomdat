# Jarkomdat

Repositori ini akan digunakan untuk pembuatan log mata kuliah pelajaran Jarkomdat. Log week yang sedang aktif dapat dibaca langsung di halaman ini atau di dalam folder week terkait. Log week yang telah dilewati dapat diakses di dalam folder week terkait.

## Week 2 - 30 September 2020 - Lesson Learned

Link Google Docs: https://docs.google.com/document/d/1IGGRtUsbkS2cJHRm7j5FY8BRkgR75z8jwkfO5I-SNsk/edit?usp=sharing

### Network Core

Sekumpulan router yang saling menghubungkan ke internet. Terdapat 2 approach: circuit switching dan packet switching. Internet kebanyakan menggunakan packet switching; jaringan telepon menggunakan circuit switching (Kurose & Ross, 2000). **Contoh**: Packet switching (jaringan internet), circuit switching (jaringan telepon).

### Regional ISP

Perusahaan penyedia layanan internet di tingkat regional/negara (Kurose & Ross, 2000); Regional ISP menggunakan jaringan dari Tier 1 ISP untuk transmisi data dari/ke Tier 1 ISP lainnya.  **Contoh**: Telkom Indonesia International, PT Mora Telematika Indonesia (“Tier 2 network”, 2020).

### Global ISP

Perusahaan penyedia layanan internet yang termasuk dalam Tier 1 ISP. Perusahaan dalam kategori ini dapat meraih seluruh internet melalui settlement-free peering sehingga tidak perlu membayar untuk mengakses dan menerima data dari jaringan Tier 1 lainnya. (“Tier 1 network”, 2020). **Contoh**: AT&T, CenturyLink (Level 3), Deutsche Telekom Global Carrier, Liberty Global, Tata Communications (“Tier 1 network”, 2020).

### Access ISP

Perusahaan penyedia layanan internet yang termasuk dalam Tier 3 ISP. Access ISP merupakan provider yang berfokus menyediakan layanan internet ke bisnis lokal dan end-customer. Access ISP hanya membeli peering untuk mengakses jaringan internet (“Tier 1 network”, 2020), tidak dapat dengan gratis mengakses beberapa jaringan/seluruh jaringan internet dengan gratis seperti Tier 1 dan Tier 2 ISP. **Contoh**: Indihome, FirstMedia, BaliFiber, dll.

### Tier 1 ISP

Perusahaan penyedia layanan internet yang melayani Tier 2 dan Tier 3 ISP. ISP dalam kategori ini dapat mengakses seluruh jaringan internet dengan gratis tanpa membeli akses peering/IP Transit. **Contoh**: AT&T, CenturyLink (Level 3), Deutsche Telekom Global Carrier, Liberty Global, Tata Communications (“Tier 1 network”, 2020).

### Tier 2 ISP

Perusahaan penyedia layanan internet yang dapat terkoneksi dengan gratis ke beberapa jaringan internet, tetapi juga membeli IP transit/peering untuk mengakses bagian internet lainnya melalui Tier 1 ISP. **Contoh**: Telkom Indonesia International, PT Mora Telematika Indonesia (“Tier 2 network”, 2020).

### Internet Exchange Point

Tempat fisik/infrastruktur di mana ISPs dan CDNs (Content Delivery Networks) terkoneksi dengan satu sama lain (“Internet exchange point”, 2020). **Contoh:** Indonesia Internet Exchange (IIX) (“List of Internet exchange points”, 2020), Equinix (“List of Internet exchange points by size”, 2020).

### Point of Presence

Suatu access point atau lokasi fisik di mana 2 atau lebih jaringan atau perangkat komunikasi terkoneksi dan menggunakan jaringan yang sama. Secara garis besar, PoP bekerja mirip dengan IXP, hanya saja dalam skala yang lebih kecil (Gibb, 2019). PoP juga tempat yang men-cache data-data CDN. **Contoh**: Meet-me rooms

### Packet Swtiching

Metode pengelompokan data yang ditransmisikan secara digital ke dalam suatu paket-paket. Paket terdiri dari header (berisi destinasi dari paket itu sendiri) dan payload (isi dari paket yang akan digunakan oleh suatu software tertentu). Packet Switching bekerja dengan asumsi bahwa waktu inactive pengguna jauh lebih besar dibanding waktu active-nya (Kurose & Ross, 2000). **Contoh:** Ethernet, Internet Protocol (IP), dan User Datagram Protocol (“Packet switching”, 2020).

### Circuit Switching

Metode koneksi jaringan di mana 2 node jaringan terhubung 1 sama lain di mana kedua node tersebut perlu terkoneksi kepada satu sama lain terlebih dahulu sebelum dapat mentransmisikan data (Kurose & Ross, 2000). **Contoh:** Public switched telephone network (PTSN), GSM, Datakit (“Circuit switching”, 2020).

### Time Division Multiplexing (TDM)

Metode transmisi dan penerimaan sinyal dalam circuit switching di mana waktu dibagi ke dalam frame-frame waktu. Frame tersebut dibagi kembali menjadi slot-slot waktu yang lebih kecil. Koneksi dua node atau lebih akan mengisi slot yang telah ada/disediakan (Kurose & Ross, 2000). **Contoh:** Jaringan telepon GSM, SDH, RIFF (WAV) audio standard (“Time-division multiplexing”, 2020).

### Frequency Division Multiplexing (FDM)

Teknik transmisi dan penerimaan sinyal di mana total bandwidth yang tersedia dari suatu medium (ex: frekuensi sinyal) dibagi ke dalam suatu seri pita frekuensi yang tidak saling overlapping (“Frequency-division multiplexing”, 2020). **Contoh:** Transmisi FM Radio, transmisi televisi (“Frequency-division multiplexing”, 2020).

### Routing

Untuk suatu packet dapat dikirim dari source ke suatu destination, jaringan perlu menentukan rute pengiriman packet tersebut. Rute tersebut ditentukan oleh routing protocol yang dibuat berdasarkan routing algorithm. Routing algorithm dioptimalisasi untuk menentukan rute yang paling efisien untuk suatu packet (Kurose & Ross, 2000). Misalnya, suatu paket memiliki destinasi pada suatu IP, maka router akan menghasilkan routing tables yang nantinya akan digunakan pada proses forwarding.

### Forwarding

Proses transit suatu packet dari 1 interface jaringan ke interface jaringan lainnya. Ketika routing tables telah terbentuk, maka routing algorithm akan membuat forwarding table untuk menghasilkan rute forwarding yang paling efisien (“Routing table”, 2020).

### Queueing Delay

Queuing delay adalah waktu yang diperlukan bagi suatu packet untuk diproses router yang terjadi ketika router masih memproses packet yang telah lebih dulu sampai.

#### Cara Menghitung

1/(μ-λ), di mana μ merupakan jumlah maksimal pemrosesan packet per detik router/perangkat terkait, dan λ untuk jumlah rata-rata datangnya suatu paket ke router/perangkat terkait (“Queuing delay”, 2019).

### Processing Delay

Waktu yang diperlukan oleh router untuk memproses packet header untuk menentukan destinasi dari packet. Dalam pemrosesan packet, router dapat mengecek error di level bit dalam suatu packet yang dapat terjadi ketika packet tersebut ditransmisikan (“Processing delay”, 2019).

#### Cara Menghitung

Tergantung kecepatan dan processing power dari router. Biasanya dalam rentang milisecond (“Processing delay”, 2019).

### Transmission Delay

Waktu yang dibutuhkan untuk mentransmisikan seluruh/jumlah bit dari packet ke dalam suatu medium (“Transmission delay”, 2019).

#### Cara Menghitung

DT = N / R seconds
Di mana DT adalah waktu transmission delay, N jumlah bit dari packet, dan R adalah rate of transmission (ex: bits per second) (“Transmission delay”, 2019).

### Propagation Delay

Jumlah waktu perjalanan yang dibutuhkan suatu sinyal dari tempat mulai sampai ke tujuannya.

#### Cara Menghitung

Dprop = D / S
Di mana Dprop adalah waktu propagasi, D merupakan panjang dari medium, dan S adalah kecepatan propagasi sinyal di medium (~2 x 108 m/s)

### Mekanisme *Tiering* dalam Internet

Jaringan Tier-1 merupakan jaringan IP yang dapat menjangkau keseluruhan internet melalui koneksi settlement-free pairing yang berarti ISP Tier-1 (ISP yang memiliki Tier-1 network) dapat mengirim dan menerima traffic dari jaringan Tier-1 lainnya secara gratis tanpa perlu membeli IP transit. ISP yang berada pada level Tier-1 dapat dianggap sebagai backbone dari internet karena ISP yang berada pada Tier-1 seringkali memberikan jasa bagi ISP Tier-2 dan ISP Tier-3 untuk mengakses jaringan Tier-1 lainnya/bagian internet lainnya melalui jaringan dan infrastruktur yang telah dimiliki oleh ISP Tier-1. Perbedaan dari ISP Tier-2 dan ISP Tier-3 adalah ISP Tier-2 dapat mengakses sebagian jaringan internet secara gratis dan sebagian sisanya perlu membayar ISP Tier-1 untuk mengakses jaringan yang tidak dapat mereka raih secara gratis, sedangkan ISP TIer-3 secara eksklusif membeli IP transit/peering ke ISP Tier-1 dan/atau ISP Tier-2 untuk mengakses jaringan internet.
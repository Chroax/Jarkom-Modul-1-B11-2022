# Jarkom-Modul-1-B11-2022
Praktikum Jaringan Komputer Modul 1 Tahun 2022


## Authors

- [@Cahyadi Surya Nugraha 5025201184](https://github.com/Chroax)
- [@Sarah Alissa Putri 5025201272](https://github.com/sharrju)
- [@Ravin Pradhitya 5025201068](https://github.com/ravinpradhitya)


## List Question
1. [Soal 1](#Question)
2. [Soal 2](#Question-2)
3. [Soal 3](#Question-3)
4. [Soal 4](#Question-4)
5. [Soal 5](#Question-5)
6. [Soal 6](#Question-6)
7. [Soal 7](#Question-7)
8. [Soal 8](#Question-8)
9. [Soal 9](#Question-9)
10. [Soal 10](#Question-10)
11. [Soal 11](#Question-11)
12. [Soal 12](#Question-12)
13. [Soal 13](#Question-13)
14. [Soal 14](#Question-14)
15. [Soal 15](#Question-15)
## Question 1
> Sebutkan web server yang digunakan pada "monta.if.its.ac.id"! 
### Screenshots
![App Screenshot](https://i.ibb.co/82LGq7f/part-1.png)

Pertama cari dengan mengetikkan pada filter `monta.if.its.ac.id`

### Screenshots
![App Screenshot](https://i.ibb.co/QJGcG6x/part-2.png)

Setelah itu klik kanan pada salah satu paket dan pilih `Follow > TCP Stream`

### Answer

Akan muncul beberapa informasi, informasi web server dapat dilihat pada tulisan server yang mana webserver yang digunakan adalah 

```bash
  nginx/1.10.3
```


## Question 2
> Ishaq sedang bingung mencari topik ta untuk semester ini , lalu ia datang ke website monta dan menemukan detail topik pada website “monta.if.its.ac.id” , judul TA apa yang dibuka oleh ishaq ?

### Screenshots
![App Screenshot](https://i.ibb.co/L9NMJ0S/part-1.png)

Pertama kita harus memfilter paket untuk mendapatkan paket hanya dari "monta.if.its.ac.id" dengan mengetikkan `tcp contains monta.if.its.ac.id`

### Screenshots
![App Screenshot](https://i.ibb.co/GF6ftFN/part-2.png)

Lalu klik kanan pada paket yang berisi detailTopik lalu klik `Follow > TCP Stream`. Kemudian ubah data dari ASCII menjadi raw dan save dengan extension '.zip'. Setelah itu extract file zip tersebut dan ubah extension yang didapatkan menjadi 'html', lalu buka pada browser yang ada

### Screenshots
![App Screenshot](https://i.ibb.co/6DbZ8Zn/part-3.png)

![App Screenshot](https://i.ibb.co/M1mhxs2/part-4.png)

Akan muncul html dan terlihat proposal yang dibuka oleh Ishaq

### Answer

Judul TA yang dibuka oleh Ishaq

```bash
  Perancangan Sistem Pengendali Panas Otomatis pada Mesin Sangrai Kopi dengan Logika Fuzzy
```


## Question 3
> Filter sehingga wireshark hanya menampilkan paket yang menuju port 80!

### Screenshots
![App Screenshot](https://i.ibb.co/P1Lmz02/part-1.png)

Cari dengan mengetikkan pada display filter `tcp.dstport == 80`


## Question 4
> Filter sehingga wireshark hanya mengambil paket yang berasal dari port 21!

### Screenshots
![App Screenshot](https://i.ibb.co/hBm8HH1/part-1.png)

Cari dengan mengetikkan pada display filter `tcp.srcport == 21`


## Question 5
> Filter sehingga wireshark hanya mengambil paket yang berasal dari port 443!

### Screenshots
![App Screenshot](https://i.ibb.co/2s484LW/part-1.png)

Cari dengan mengetikkan pada display filter `tcp.srcport == 443`


## Question 6
> Filter sehingga wireshark hanya menampilkan paket yang menuju ke lipi.go.id !

### Screenshots
![App Screenshot](https://i.ibb.co/PYmmtRN/part-1.png)

Cari dengan mengetikkan pada display filter `tcp contains lipi.go.id`


## Question 7
> Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

### Screenshots
![App Screenshot](https://i.ibb.co/6vnC3pp/part-2.png)

Cari settingan ip wifi yang kamu gunakkan, jika menggunakan windows silahkan cari settings, lalu cari `Network & Internet`, kemudian cari wifi, lalu klik wifi yang sedang kamu gunakkan, dan lihat di paling bawah ada ip untuk wifi yang kamu gunakkan

### Screenshots
![App Screenshot](https://i.ibb.co/3dnT3mG/part-1.png)

Cari dengan mengetikkan pada display filter `ip.src == 192.168.100.28`


## Question 8
> Telusuri aliran paket dalam file .pcap yang diberikan, cari informasi berguna berupa percakapan antara dua mahasiswa terkait tindakan kecurangan pada kegiatan
praktikum. Percakapan tersebut dilaporkan menggunakan protokol jaringan dengan
tingkat keandalan yang tinggi dalam pertukaran datanya sehingga kalian perlu
menerapkan filter dengan protokol yang tersebut.

### Screenshots
![Screenshot from 2022-09-19 21-50-07](https://user-images.githubusercontent.com/81427127/191049525-e3c757b1-5212-465f-9142-0b3a6285c327.png)
![Screenshot from 2022-09-19 21-50-12](https://user-images.githubusercontent.com/81427127/191049850-123c16ac-709f-46be-b595-1eaadb34d3fa.png)

Keterangan
Setelah mendownload file dari drive, buka file menggunakan Wireshark. Kemudian, apabila di scroll ke bawah, ditemukan percakapan seperti gambar di atas.

### Answer
Untuk mendapatkakn kompilasi percakapan, kami menggunakan filter ```tcp.stream eq 12``` kemudian klik di salah satu percakapan, lalu klik follow dan TCP Stream.

Berikut adalah kompilasi percakapannya,
![Screenshot from 2022-09-19 21-40-13](https://user-images.githubusercontent.com/81427127/191050336-a87e63bb-89e8-457b-93c3-8012dd2ae99d.png)



## Question 9
> Terdapat laporan adanya pertukaran file yang dilakukan oleh kedua mahasiswa dalam
percakapan yang diperoleh, carilah file yang dimaksud! Untuk memudahkan laporan
kepada atasan, beri nama file yang ditemukan dengan format
[nama_kelompok].des3 dan simpan output file dengan nama “flag.txt”.

### Screenshots
![save file](https://user-images.githubusercontent.com/90445721/191053282-db9142ff-ca78-47a3-b1f8-97d77c43103b.jpeg)
Keterangan
Selain menemukan percakapan setelah di scroll kami menemukan kode yang dicari. Selanjutnya, klik kanan pada kode tsb. kemudian klik Export Packet Bytes lalu beri nama file sesuai yang diminta.


### Screenshots
![terminal](https://user-images.githubusercontent.com/90445721/191054096-b61cdcb3-1fa7-4588-ad76-5a5099115158.jpeg)
Keterangan
Untuk decrypt codenya, gunakan terminal dan ketik sesuai gambar di atas dan masukkan ke file flag.txt


## Question 10
> Temukan password rahasia (flag) dari organisasi bawah tanah yang disebutkan di
atas!

### Screenshots
![password](https://user-images.githubusercontent.com/90445721/191054416-a04abb36-443b-4db6-8a2d-721b221261a8.jpeg)
Keterangan
Lanjut dari no.9, setelah flag.txt disimpan, buka files. Dan passwordnya akan muncul seperti gambar di atas.


## Kendala
- Keterangan kendala
- Harus menggunakan Ubuntu untuk nomor 8, 9, dan 10.

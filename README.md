# Jarkom-Modul-1-A09-2021
Laporan Resmi Praktikum Jarkom Modul 1

# Nama Anggota Kelompok #
1. Arvel Gavrilla Raissananda (05111940000040)
2. Johnivan Aldo Sudiono (05111940000051)
3. Vincent Yonathan (05111940000186)

# Praktikum Modul 1 #
### 1. Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!  ###
Server: nginx/1.18.0 (Ubuntu)
Cara : 
- Membuka file yang telah didownload (1-5) pada Drive
- Mengisi display filter dengan : http.host contains "ichimarumaru.tech"
- Lalu Follow TCP Stream, maka bisa dilihat server yang digunakan nginx/1.18.0 (Ubuntu)

![image](https://user-images.githubusercontent.com/36225278/134457739-83db4c8a-6d10-4b3e-9061-e1e3c4ada25a.png)

### 2. Temukan paket dari web-web yang menggunakan basic authentication method! ###
Cara : 
- Membuka file yang telah didownload dari drive (1-5)
- Mengisi display filter dengan : http.authbasic

![image](https://user-images.githubusercontent.com/36225278/134457856-b2c40b16-1311-493b-8e17-1cc7808dbe1d.png)

### 3. Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng! ###
Cara :
- Membuka file yang telah didownload dari drive (1-5)
- Mengisi display filter dengan : http.host contains "basic.ichimarumaru.tech"
![nomor3a](https://user-images.githubusercontent.com/73924235/134510153-04f50959-7977-425f-b944-325db47a8d23.png)

- Menuju ke Hypertext Transfer Protocol, Get, lalu ke Authorization, ada credentials disana.
![nomor3b](https://user-images.githubusercontent.com/73924235/134510173-8009d732-8e64-43ca-8e72-f8d4e560474b.png)

### 4. Temukan paket mysql yang mengandung perintah query select! ###

### 5. Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap! ###
Cara :
- Membuka File yang didownload pada Drive (1-5)
-	Memasukan display filter dengan `mysql.query contains INSERT`
-	Memilih Follow lalu Follow TCP Stream
![soal5a](https://user-images.githubusercontent.com/73924235/134495117-7ddd820c-19d8-444a-881f-6bdd000df563.png)
-	Terlihat bahwa Username nya adalah akakanomi dan passwordnya pemisah4lautan
-	Login ke http://portal.ichimarumaru.tech/
![soal5b](https://user-images.githubusercontent.com/73924235/134495806-0175083d-763e-4c22-af62-803021eb7421.png)


### 6. Cari username dan password ketika melakukan login ke FTP Server! ###
Username : secretuser
Password : aku.pengen.pw.aja
Cara :
- Membuka file yang telah didownload dari drive (6-7)
- ftp.request.command == PASS || ftp.request.command == USER

![image](https://user-images.githubusercontent.com/36225278/134457915-fc05a3ad-966e-4efc-a05e-b8187e1593b6.png)

### 7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf") ###

Cara :
- Membuka file yang telah didownload dari drive (6-7)
- Mengisi display filter dengan : frame contains "Real.pdf"

![image](https://user-images.githubusercontent.com/36225278/134458097-b0c04b34-2476-45b5-b833-920824022a85.png)

- Lalu klik kanan, dan pilih follow ⇒ TCP Stream

![image](https://user-images.githubusercontent.com/36225278/134458143-785723e9-b58a-4b33-bfe3-1489eb2add9b.png)

- Kemudian kita ubah show datanya, menjadi dalam bentuk RAW
![image](https://user-images.githubusercontent.com/36225278/134458208-0c9e8506-f4a7-4b10-a951-aed5666a7612.png)

- Lalu save as dengan nama Real.zip
- Kemudian kita convert menggunakan WinRAR file tersebut
![image](https://user-images.githubusercontent.com/36225278/134458252-0daf94fc-b124-4659-a996-bee08c2efde9.png)

- Lalu akan muncul file Real.pdf, dan tinggal kita buka. Voila, kita kena Rick Roll
![image](https://user-images.githubusercontent.com/36225278/134458310-09872871-23c0-4efd-b251-413d4dc83805.png)

### 8. Cari paket yang menunjukan pengambilan file dari FTP tersebut! ###

### 9. ari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut! ###
Cara :
- Buka File yang ada pada Drive (8-10)
-	Mengisi display filter dengan ftp-data.command contains “secret.zip” 
![soal9a](https://user-images.githubusercontent.com/73924235/134495308-37954fbb-b986-474d-bb72-a9d3ab0d784c.png)
-	Memilih follow dan follow TCP
![soal9b](https://user-images.githubusercontent.com/73924235/134495323-231862f6-0754-43e1-9883-6c5665d8d910.png)
-	Kemudian terlihat data yang masih ASCII, diganti menjadi raw
![soal9c](https://user-images.githubusercontent.com/73924235/134495340-8b42127e-0b23-41a3-a1f4-e30d65c327bc.png)
-	Lalu melakukan Save As dengan nama secret.zip
![soal9d](https://user-images.githubusercontent.com/73924235/134495387-90141451-90d1-4113-8036-4a2015f81bfd.png)
-	Kemudian membuka Folder berisi Wanted.pdf, namun belum bisa dibuka karena memiliki password
![soal9e](https://user-images.githubusercontent.com/73924235/134495398-cbc2d07c-0753-4461-bc83-75ff403bdfb7.png)

 
### 10. Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"! ###
-	Buka File yang ada pada Drive (8-10)
-	Mengisi display filter dengan `ftp-data.command contains “secret.zip”`
![soal10a](https://user-images.githubusercontent.com/73924235/134495482-4160e7ce-84a6-46bd-90da-d782ed36d3d4.png)

-	Memilih follow dan follow TCP
 ![soal10b](https://user-images.githubusercontent.com/73924235/134495514-e77d24b3-267e-4c72-8f5b-ccf5dea56330.png)

-	Kemudian terlihat data yang menunjukan bahwa password (key) ada pada file bukanapaapa.txt dari tail-1 (yaitu 1 dari yang paling bawah)
 ![soal10c](https://user-images.githubusercontent.com/73924235/134495528-d335ccb8-2ea4-430f-a902-fba2badb0115.png)

-	Mengisi display filter lagi dengan ftp-data.command contains “bukanapaapa.txt”
 ![soal10d](https://user-images.githubusercontent.com/73924235/134495547-ace13651-282d-42d4-b1f7-f772f514e399.png)

-	Kemudian melakukan follow TCP lagi
 ![soal10e](https://user-images.githubusercontent.com/73924235/134495563-ee65f051-8b93-4d4c-90ac-9c16e60f3a20.png)

-	Terlihat password untuk Wanted.pdf yaitu d1b1langbukanapaapajugagapercaya
 ![soal10f](https://user-images.githubusercontent.com/73924235/134495573-fc36dd2e-6e26-42e0-9cab-5b5fa99d9d46.png)

-	Memasukan password ke wanted.pdf.
![soal10g](https://user-images.githubusercontent.com/73924235/134495603-11783db4-7b98-400e-91ce-e850967bbf4f.png)


### 11. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!  ###

### 12. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21! ###
Cara :
- Mengisi Capture Filter dengan `port 21`
![soal12a](https://user-images.githubusercontent.com/73924235/134495705-648736d6-9354-45e8-aebc-7c2d11fae484.png)
- Hasil Kosong, karena port 21 harus menggunakan FTP yang bisa diakses melalui filezilla
![soal12b](https://user-images.githubusercontent.com/73924235/134495753-49286cf9-422e-43fe-af40-032200e1e0ed.png)


### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443! ###

### 14. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id! ###

### 15. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian! ###


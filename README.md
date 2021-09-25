# Jarkom-Modul-1-A09-2021
Laporan Resmi Praktikum Jarkom Modul 1

# Anggota Kelompok
Anggota  | NRP
---------|-------
Arvel Gavrilla Raissananda | 05111940000040
Johnivan Aldo Sudiono | 05111940000051
Vincent Yonathan | 05111940000186

## Link-link
- [Soal](https://docs.google.com/document/d/11wl424Kb-6_FegaR6fvUY2yBFKlMlCmGqc0yhA5b7Wc/edit)
- [File PCAP](https://drive.google.com/drive/folders/11lLVpFeBZ3XNx3Oc4k8BPutYxMgWtWq4)

# --- No 1 ---
Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!  

### Jawaban :
Server: nginx/1.18.0 (Ubuntu)

### Langkah Penyelesaian : 
- Membuka file yang telah didownload (1-5) pada Drive
- Mengisi display filter dengan : http.host contains "ichimarumaru.tech"
- Lalu Follow TCP Stream, maka bisa dilihat server yang digunakan nginx/1.18.0 (Ubuntu)

![image](https://user-images.githubusercontent.com/36225278/134457739-83db4c8a-6d10-4b3e-9061-e1e3c4ada25a.png)

# --- No 2 ---
Temukan paket dari web-web yang menggunakan basic authentication method!

### Langkah Penyelesaian : 
- Membuka file yang telah didownload dari drive (1-5)
- Mengisi display filter dengan : http.authbasic

![image](https://user-images.githubusercontent.com/36225278/134457856-b2c40b16-1311-493b-8e17-1cc7808dbe1d.png)

# --- No 3 ---
Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!

### Langkah Penyelesaian : 
- Membuka file yang telah didownload dari drive (1-5)
- Mengisi display filter dengan : `http.host contains "basic.ichimarumaru.tech"`
![nomor3a](https://user-images.githubusercontent.com/73924235/134510153-04f50959-7977-425f-b944-325db47a8d23.png)

- Menuju ke Hypertext Transfer Protocol, Get, lalu ke Authorization, ada credentials disana.
![nomor3b](https://user-images.githubusercontent.com/73924235/134510173-8009d732-8e64-43ca-8e72-f8d4e560474b.png)

# --- No 4 ---
Temukan paket mysql yang mengandung perintah query select!

### Langkah Penyelesaian : 
- Membuka file yang telah didownload dari drive (1-5)
- Mengisi display filter dengan : `mysql.query contains select || mysql.query contains SELECT`
![image](https://user-images.githubusercontent.com/72689610/134608740-19828052-d6f8-4135-8476-2c8a54cee3cf.png)
![image](https://user-images.githubusercontent.com/72689610/134608764-d1af4a13-833b-44ae-9c49-617cee3802ee.png)
![image](https://user-images.githubusercontent.com/72689610/134608798-e03248cb-caa9-4d38-8668-eaab9f3bc5fd.png)

# --- No 5 ---
Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap! 

### Jawaban :
Username : Akakanomi <br>
Password : pemisah4lautan

### Langkah Penyelesaian : 
- Membuka File yang didownload pada Drive (1-5)
-	Memasukan display filter dengan `mysql.query contains INSERT`
![image](https://user-images.githubusercontent.com/72689610/134609281-522648b6-c9c7-4fb7-b907-794d61df2053.png)
-	Memilih Follow lalu Follow TCP Stream
![soal5a](https://user-images.githubusercontent.com/73924235/134495117-7ddd820c-19d8-444a-881f-6bdd000df563.png)
-	Terlihat bahwa Username nya adalah akakanomi dan passwordnya pemisah4lautan
-	Login ke http://portal.ichimarumaru.tech/
![soal5b](https://user-images.githubusercontent.com/73924235/134495806-0175083d-763e-4c22-af62-803021eb7421.png)

# --- No 6 ---
Cari username dan password ketika melakukan login ke FTP Server!

### Jawaban :
Username : secretuser <br>
Password : aku.pengen.pw.aja

### Langkah Penyelesaian : 
- Membuka file yang telah didownload dari drive (6-7)
- Memasukkan display filter dengan `ftp.request.command == PASS || ftp.request.command == USER`
- Bisa terlihat apa username dan password yang diperlukan.
![image](https://user-images.githubusercontent.com/72689610/134610099-89e69316-1ead-431f-bfbb-7f4f13d78453.png)

# --- No 7 ---
Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")

### Langkah Penyelesaian : 
- Membuka file yang telah didownload dari drive (6-7)
- Mengisi display filter dengan : `frame contains "Real.pdf"`

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

# --- No 8 ---
Cari paket yang menunjukan pengambilan file dari FTP tersebut!

### Langkah Penyelesaian : 
- Membuka file yang telah didownload dari drive (8-10)
- Menjalankan command `ftp-data.command==RETR` pada display filter
- Tidak muncul list packet apapun
![image](https://user-images.githubusercontent.com/72689610/134615449-ef430ba4-f7d5-4bfc-aa29-070ecac22f06.png)

# --- No 9 ---
Cari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!

### Langkah Penyelesaian : 
- Buka File yang ada pada Drive (8-10)
-	Mengisi display filter dengan `ftp-data.command contains “secret.zip” `
![soal9a](https://user-images.githubusercontent.com/73924235/134495308-37954fbb-b986-474d-bb72-a9d3ab0d784c.png)
-	Memilih follow dan follow TCP
![soal9b](https://user-images.githubusercontent.com/73924235/134495323-231862f6-0754-43e1-9883-6c5665d8d910.png)
-	Kemudian terlihat data yang masih ASCII, diganti menjadi raw
![soal9c](https://user-images.githubusercontent.com/73924235/134495340-8b42127e-0b23-41a3-a1f4-e30d65c327bc.png)
-	Lalu melakukan Save As dengan nama secret.zip
![soal9d](https://user-images.githubusercontent.com/73924235/134495387-90141451-90d1-4113-8036-4a2015f81bfd.png)
-	Kemudian membuka Folder berisi Wanted.pdf, namun belum bisa dibuka karena memiliki password
![soal9e](https://user-images.githubusercontent.com/73924235/134495398-cbc2d07c-0753-4461-bc83-75ff403bdfb7.png)

# --- No 10 --- 
Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!

### Langkah Penyelesaian : 
-	Buka File yang ada pada Drive (8-10)
-	Mengisi display filter dengan `ftp-data.command contains “history.txt”`
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

# --- No 11 --- 
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!

### Langkah Penyelesaian :
- Mengisi capture filter dengan "src port 80" kemudian enter
![image](https://user-images.githubusercontent.com/72689610/134629218-62fc01c3-f740-4cc1-9ecc-fa54c00750a3.png)

- Membuka wireshark kembali, namun kali ini memilih `WIFI`
- Mengisi capture filter dengan "src port 80" kemudian enter
- Kemudian buka sebuah website, kali ini kami menggunakan website `http://monta.if.its.ac.id/index.php/progres/tugasakhir`
- Maka di wireshark akan muncul sebagai berikut :
![image](https://user-images.githubusercontent.com/72689610/134629869-4ffa8691-367b-4579-aa97-ad8ee3e71388.png)

# --- No 12 --- 
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!

### Langkah Penyelesaian :
- Mengisi Capture Filter dengan `port 21` pada Adapter for Loopback Traffic
![soal12a](https://user-images.githubusercontent.com/73924235/134495705-648736d6-9354-45e8-aebc-7c2d11fae484.png)
- Hasil Kosong, karena port 21 harus menggunakan FTP yang bisa diakses melalui filezilla
![soal12b](https://user-images.githubusercontent.com/73924235/134495753-49286cf9-422e-43fe-af40-032200e1e0ed.png)
- Ketika XAMPP dinyalakan dan Filezilla diconnect maka akan menghasilkan hasil berikut
![soal12c](https://user-images.githubusercontent.com/73924235/134642277-6e7a9cf6-aaf7-4ae9-98b9-a69d7546dee8.JPG)

# --- No 13 --- 
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!

### Langkah Penyelesaian :
- Mengisi capture filter dengan `dst port 443` kemudian enter
![image](https://user-images.githubusercontent.com/72689610/134630498-2dc8b4cd-9b90-444d-9e64-37394adc1cd2.png)

- Membuka wireshark kembali, namun kali ini memilih `WIFI`
- Mengisi capture filter dengan `dst port 443` kemudian enter
![image](https://user-images.githubusercontent.com/72689610/134630498-2dc8b4cd-9b90-444d-9e64-37394adc1cd2.png)

- Kemudian buka sebuah website, kali ini kami menggunakan website `http://monta.if.its.ac.id/index.php/progres/tugasakhir`
- Maka di wireshark akan muncul sebagai berikut :
![image](https://user-images.githubusercontent.com/72689610/134630813-acf1189e-b1ca-47a2-83d8-990101ce3e54.png)

# --- No 14 --- 
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!

### Langkah Penyelesaian :
- Mengisi capture filter dengan `dst host kemenag.go.id` kemudian enter
![image](https://user-images.githubusercontent.com/72689610/134632321-a70faa64-3571-42a2-8bf3-430370c82568.png)

- Membuka website `https://www.kemenag.go.id/`
![image](https://user-images.githubusercontent.com/72689610/134631528-9a25d2b3-15af-4a4f-ad09-6eabbf1f4138.png)

# --- No 15 --- 
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

### Langkah Penyelesaian :
- Mencari ip dengan membuka `command prompt` dan mengetikkan `ipconfig`
![image](https://user-images.githubusercontent.com/72689610/134631809-fd0fadf9-76bc-4a57-912b-90181c97378c.png)

- Membuka wireshark dan mengisi capture filter dengan `src host 192.168.1.4`
![image](https://user-images.githubusercontent.com/72689610/134632067-f600b66c-4d91-4ef6-bccd-136176b2bf66.png)

- Output :
![image](https://user-images.githubusercontent.com/72689610/134632169-5379cc0b-6cf3-4632-a5ec-af7d3735c261.png)

## Kendala Pengerjaan
- Saat dijalankan, terkadang output tidak keluar



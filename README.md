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

### 4. Temukan paket mysql yang mengandung perintah query select! ###

### 5. Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap! ###

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

### 10. Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"! ###

### 11. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!  ###

### 12. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21! ###

### 13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443! ###

### 14. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id! ###

### 15. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian! ###


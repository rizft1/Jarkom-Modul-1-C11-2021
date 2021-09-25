# Jarkom-Modul-1-C11-2021

## Anggota Kelompok C11 : <br>
- 05111940000001 Christopher Baptista
- 05111940000093 Riki Mi’roj Achmad
- 05111940000219 M Rizqi Fiqih Thalib

## Cara Pengerjaan
1. Sebutkan webserver yang digunakan pada "ichimarumaru.tech"! 
![image-000](https://user-images.githubusercontent.com/57831206/134773481-1516c950-065c-4f18-ab06-e0c370d0b85e.png)
![image-001](https://user-images.githubusercontent.com/57831206/134773484-5e0f68a4-f2b1-4fa9-9611-46809564a021.png)

2. Temukan paket dari web-web yang menggunakan basic authentication method!
![image-002](https://user-images.githubusercontent.com/57831206/134773489-fdecdc88-17fa-4ee5-9472-245ead4d24ec.png)

3. Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
![image-003](https://user-images.githubusercontent.com/57831206/134773490-feeee43e-e287-48d1-8e15-20a217a742f0.png)
![image-004](https://user-images.githubusercontent.com/57831206/134773491-4dd51269-d332-47b8-93eb-2fea4bfacf0c.png)

4. Temukan paket mysql yang mengandung perintah query select!
![image-005](https://user-images.githubusercontent.com/57831206/134773493-56fdbf1e-da50-456b-8ae7-da4d74bdbf12.png)
![image-006](https://user-images.githubusercontent.com/57831206/134773499-652f8750-7d01-47a7-9c6d-68b47c37945f.png)
![image-007](https://user-images.githubusercontent.com/57831206/134773501-752ad6a7-8027-47f3-8ae1-6a2a8b6c8f07.png)
![image-008](https://user-images.githubusercontent.com/57831206/134773503-20a3055d-c04f-4dbf-a5b9-4484442e9d96.png)

5. Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!
![image-009](https://user-images.githubusercontent.com/57831206/134773505-403bbc92-3ac7-4ec8-9306-c15cc3278166.jpg)
![image-010](https://user-images.githubusercontent.com/57831206/134773507-8bee6964-5d66-49a5-943a-2634c9bed4d5.png)

6. Cari username dan password ketika melakukan login ke FTP Server!
<br/>
Username dan Password dapat dicari menggunakan filter "ftp.request.command == USER || ftp.request.command == PASS". Akan muncul paket yang membawa username dan password seperti pada gambar berikut.
![image](https://user-images.githubusercontent.com/74702068/134773732-8f7e04ab-63cf-4b53-8695-e6172169bcd4.png)


7. Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")
<br/>
Filter yang dapat digunakan adalah "ftp-data contains Real.pdf" dan akan muncul paket yang membawa zip file nomor 201. File tersebut dapat dibuka menggunakan TCP Stream dan di save dengan ekstensi pdf. 
![image](https://user-images.githubusercontent.com/74702068/134773783-cb40e7b6-bf6d-4c22-a457-2b2d96eb434b.png)
![image](https://user-images.githubusercontent.com/74702068/134773807-e7702e66-19e5-4985-9aeb-24cf9b4e43cc.png)


8. Cari paket yang menunjukan pengambilan file dari FTP tersebut!
<br/>
Kata mas nya pada saat demo nomer 8 salah nomor. Jadi saya mengerjakan sebisa nya yaitu dengan menggunakan filter "ftp.response.code==150 || ftp.response.code==226" yaitu kode response untuk send data dan transfer complete.
![image](https://user-images.githubusercontent.com/74702068/134773853-89ff8ac5-1e75-4ff6-8ad8-7d01e93be781.png)


9. Dari paket-paket yang menuju FTP terdapat indikasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!
<br/>
File dapat dicari menggunakan filter "ftp.request.command == STOR"
![image](https://user-images.githubusercontent.com/74702068/134773870-2edb5098-e905-4a72-86d4-9f8a809b2527.png)
lalu file dapat di simpan dengan cara Follow > TCP Stream > show data as raw > save as dengan nama “secret.zip"
![image](https://user-images.githubusercontent.com/74702068/134773903-4b1c46b1-b501-4002-885d-fc8246f3b6f7.png)

10. Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!
<br/>
Langkah pertama ada memfilter paket untuk mendapatkan file bukanapapa.txt yaitu dengan filter "ftp-data.command contains "bukanapapa.txt"". Lalu setelah didapatkan paketnya didalamnya  terdapat sebuah password yaitu "d1b1langbukanapapajugagapercaya".
![image](https://user-images.githubusercontent.com/74702068/134773964-8ba0a389-d7b9-42dd-9d4f-fddaa1949417.png)
![image](https://user-images.githubusercontent.com/74702068/134773973-9d9515c3-a46c-49ad-9e99-b85d84e5646d.png)


11. Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80! 


12. Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!


13. Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!


14. Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!


15. Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!

## Kendala yang dialami

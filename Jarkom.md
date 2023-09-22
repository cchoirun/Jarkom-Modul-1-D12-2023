### Analisis Packet Capture

1. **Penggunaan Protokol FTP**

   - Untuk memeriksa aktivitas dengan protokol FTP, pertama-tama, kita filter dengan menggunakan `"ftp"`. Ini akan menampilkan semua aktivitas FTP.
   - Selanjutnya, kita mencari file yang menonjol, seperti `"grabThePhisher.zip"`.
   - Kemudian, kita mencatat sequence number (raw) dan acknowledge number (raw).
   - Setelah itu, kita mencari file responsenya yang berada tepat di bawahnya dan mencatat sequence number (raw) dan acknowledge number (raw).
   ![1.1](1.1.png)
   ![1.2](1.2.png)
   ![1.3](1.3.png)

2. **Web Server pada Portal Praktikum Jarkom**

   - Untuk mengidentifikasi web server yang digunakan dalam portal praktikum jarkom, kita menggunakan filter `"http"`.
   ![2.1](2.1.png)
   - Kita pilih entri paling atas dan melakukan follow tcp stream.
   - Hasilnya, dapat kita ketahui bahwa server portal praktikum jarkom menggunakan gunicorn.
   ![2.2](2.2.png)


3. **Pertanyaan Terkait Paket**
    ![3.1](3.1.png)
   - Dalam menjawab pertanyaan terkait paket dengan IP dan port tertentu, kita menggunakan display filtering yang sesuai.
   - Dalam contoh di bawah, terdapat 21 paket dengan protokol UDP.
    ![3.2](3.2.png)

4. **Header Checksum pada Paket No. 130**

   - Untuk mengetahui header checksum pada paket nomor 130, kita periksa paket tersebut.
   - Hasilnya, checksumnya adalah `0x18e5`.
    ![4.1](4.1.png)

5. **Analisis File Packet Capture**

   - Saat menganalisis file packet capture yang menarik, langkah-langkahnya adalah:
   - Mencoba membuka zip yang terkunci dengan mencari kunci.
   - Mengecek file tcp dan melakukan follow tcp stream.
   - Menemukan percakapan tentang password yang dienkripsi dalam base64.
   ![5.1](5.1.png)
   ![5.2](5.2.png)
   - Menggunakan base64 encoder online untuk menemukan kunci untuk membuka file zip.
   ![5.3](5.3.png)
   ![5.4](5.4.png)
   - Untuk mendapatkan port, kita bisa mengklik salah satu paket dengan protokol SMTP dengan port 25.
   - Kemudian, kita dapat melihat public IP dengan pola yang agak berbeda, yaitu `74.53.140.153`.
   ![5.5](5.5.png)

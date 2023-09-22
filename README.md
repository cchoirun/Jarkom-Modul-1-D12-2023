# Jarkom-Modul-1-D12-2023


## Anggota Kelompok

<table>
  <tr>
    <th>NRP</th>
    <th>Nama</th>
  </tr>
  <tr>
    <td>Muhammad Revel Wivanto</td>
    <td>5025211233</td>
  </tr>
  <tr>
    <td>Muhammad Choirun Ni'am</td>
    <td>5025221203</td>
  </tr>
</table>

<br>


## NO 6. 
 *Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.*

Untuk menyelesaikan soal ini, kita perlu memahami clue yang diberikan pada soal yakni "SOURCE ADDRESS 7812". Jadi kita mencurigai paket nomor 7812. Pertama kita pilih Go to Packet, kemudian masukkan 7812, lalu kita akan dibawa menuju paket 7812. Dari situ kita bisa melihat source addressnya yaitu 104.18.14.101.

![Screenshot soal 6](img/soal6.png)

Kemudian berdasarkan hint maka kita menggunakan substitusi a1z26 chiper, kemudian kita masukkan 10 4 18 14 10 1 dan saat di decode menunjukkan jdrnja. Karena dibatasi A-R yg merupakan huruf besar maka kita masukkan JDRNJA ke dalam ncat dan berhasil mendapatkan flag.

![Screenshot soal 6](img/soal6(2).png)

Kendala : Kita cukup kesulitan memahami maksud dan clue-clue yang diberikan soal pertama kali sehingga membutuhkan waktu yang cukup lama untuk menyelesaikan soal nomor 6.

## NO 7
*Berapa jumlah packet yang menuju IP 184.87.193.88?*

Untuk mengetahui jumlah packet yang menuju IP tersebut maka kita dapat melakukan display filter :
`ip.dst ==  184.87.193.88`

![Screenshot soal 7](img/soal7.png)

Dapat dilihat bahwa terdapat 6 paket.

## NO 8
*Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)!*

Untuk mengetahui paket yang menuju port 80 maka kita dapat meggunakan display filter :
`tcp.dstport == 80 || udp.dstport == 80`

![Screenshot soal 8](img/soal8.png)
![Screenshot soal 8](img/soal8(2).png)

## NO 9
*Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!*

Kita dapat menggunakan metode yang sama dengan nomor 8 yaitu melakukan display filter pada paket yang sudah tercapture yaitu dengan :
`ip.src == 10.51.40.1 && (ip.dst != 10.39.55.34)`

![Screenshot soal 9](img/soal9.png)



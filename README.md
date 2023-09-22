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
## Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak terdUga. ketika udin mereka membuka game tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan slamet untuk menemukan solusi kode error tersebut.

Untuk menyelesaikan soal ini, kita perlu memahami clue yang diberikan pada soal yakni "SOURCE ADDRESS 7812". Jadi kita mencurigai paket nomor 7812. Pertama kita pilih Go to Packet, kemudian masukkan 7812, lalu kita akan dibawa menuju paket 7812. Dari situ kita bisa melihat source addressnya yaitu 104.18.14.101.

![Screenshot soal 6](img/soal6.png)

Kemudian berdasarkan hint maka kita menggunakan substitusi a1z26 chiper, kemudian kita masukkan 10 4 18 14 10 1 dan saat di decode menunjukkan jdrnja. Karena dibatasi A-R yg merupakan huruf besar maka kita masukkan JDRNJA ke dalam ncat dan berhasil mendapatkan flag.

![Screenshot soal 6](img/soal6(2).png)

# Kendala : Kita cukup kesulitan memahami maksud dan clue-clue yang diberikan soal pertama kali sehingga membutuhkan waktu yang cukup lama untuk menyelesaikan soal nomor 6.
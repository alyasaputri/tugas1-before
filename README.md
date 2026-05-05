<!DOCTYPE html>
<html lang="id">    
Kode dimulai dengan <!DOCTYPE html> yang berfungsi untuk memberi tahu browser bahwa dokumen ini menggunakan HTML versi 5. Setelah itu terdapat tag <html lang="id"> yang menjadi elemen utama dari halaman web, di mana atribut lang="id" menunjukkan bahwa bahasa yang digunakan adalah Bahasa Indonesia sehingga membantu browser dan mesin pencari memahami konten halaman.
<head>
    </head>
Selanjutnya terdapat bagian <head></head> yang merupakan kepala dari dokumen HTML. Biasanya bagian ini digunakan untuk menyimpan metadata seperti judul halaman (<title>), pengaturan karakter (<meta>), atau link ke file CSS dan JavaScript. Namun pada kode ini, bagian head masih kosong karena styling langsung ditulis di dalam tag <style>.
<style>
        body {
            font-family: Arial;
            margin: 20px;
            background: #f696ce;
        }
Bagian <style> digunakan untuk menuliskan CSS yang berfungsi mengatur tampilan halaman. Di dalamnya, aturan pertama adalah body yang mengatur keseluruhan tampilan halaman seperti jenis font menggunakan Arial, jarak luar halaman dengan margin 20px, serta warna latar belakang berwarna pink (#f696ce), sehingga halaman terlihat lebih menarik.
form {
            background: #fff;
            padding: 20px;
            border-radius: 10px;
            margin-bottom: 20px;
        }
Selanjutnya terdapat styling untuk form, yang digunakan untuk mempercantik tampilan form input. Form diberi background warna putih agar kontras dengan background utama, diberi padding agar isi tidak menempel ke tepi, serta border-radius untuk membuat sudut menjadi melengkung. Margin-bottom juga ditambahkan agar ada jarak antara form dan elemen di bawahnya.
input, textarea, select {
            width: 100%;
            padding: 8px;
            margin: 5px 0 15px;
        }
Kemudian ada pengaturan untuk input, textarea, dan select yang membuat semua elemen input memiliki lebar penuh (100%), padding agar nyaman digunakan, serta margin untuk memberi jarak antar field sehingga tampilan lebih rapi dan tidak terlalu padat.
button {
            padding: 10px;
            margin-right: 5px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
Selanjutnya bagian button mengatur tampilan tombol agar lebih menarik, dengan padding untuk ukuran, margin untuk jarak antar tombol, border dihilangkan agar tampak modern, sudut dibuat melengkung, dan cursor diubah menjadi pointer saat diarahkan agar terlihat interaktif. Kemudian terdapat class .submit yang memberi warna hijau pada tombol submit dan .reset yang memberi warna merah pada tombol reset.
 table {
          width: 100%;
            border-collapse: collapse;
            background: #fff;
        }
        th, td {
            border: 1px solid #ccc;
            padding: 10px;
            text-align: center;
        }


Bagian berikutnya adalah styling untuk table, yang mengatur tabel agar memiliki lebar penuh, menggunakan border-collapse supaya garis tabel menyatu, serta background putih agar data mudah dibaca. Lalu th dan td diberi border, padding, dan teks rata tengah untuk memperjelas isi tabel.
        img {
            cursor: pointer;  
}
Terakhir di CSS terdapat aturan untuk img yang mengubah cursor menjadi pointer saat diarahkan ke gambar, biasanya digunakan jika gambar dijadikan tombol seperti tombol hapus.
<body>
    <h2>Form Data Mahasiswa</h2>
    <form id="formMahasiswa">
Masuk ke bagian <body>, terdapat judul pertama yaitu <h2>Form Data Mahasiswa</h2> yang berfungsi sebagai heading untuk bagian form. Setelah itu terdapat <form id="formMahasiswa"> yang digunakan sebagai tempat input data mahasiswa, dengan id yang nantinya bisa digunakan oleh JavaScript.
<label>NIM</label>
        <input type="text" id="nim" required>

        <label>Nama</label>
        <input type="text" id="nama" required>
Di dalam form terdapat beberapa input, dimulai dari NIM dan Nama yang menggunakan <input type="text"> untuk memasukkan teks biasa, serta atribut required yang berarti data tersebut wajib diisi sebelum form dikirim.
<label>Alamat</label>
        <textarea id="alamat"></textarea>
Selanjutnya terdapat bagian alamat yang menggunakan <textarea> karena memungkinkan pengguna menulis teks lebih panjang dibandingkan input biasa.
<label>Jenis Kelamin</label><br>
        <input type="radio" name="jk" value="Pria"> Pria
        <input type="radio" name="jk" value="Wanita"> Wanita
        <br><br>
Kemudian terdapat bagian jenis kelamin yang menggunakan radio button (type="radio"), di mana pengguna hanya bisa memilih satu dari dua pilihan yaitu Pria atau Wanita. Kedua radio memiliki atribut name="jk" yang sama agar saling terhubung sebagai satu grup pilihan.
<label>Tanggal Lahir</label>
        <select id="tanggal"></select>
        <select id="bulan">
            <option value="01">Januari</option>
            <option value="02">Februari</option>
            <option value="03">Maret</option>
            <option value="04">April</option>
            <option value="05">Mei</option>
            <option value="06">Juni</option>
            <option value="07">Juli</option>
            <option value="08">Agustus</option>
            <option value="09">September</option>
            <option value="10">Oktober</option>
            <option value="11">November</option>
            <option value="12">Desember</option>
        </select>
        <select id="tahun"></select>
Setelah itu terdapat bagian tanggal lahir yang menggunakan tiga dropdown (select) yaitu tanggal, bulan, dan tahun. Bagian bulan sudah memiliki daftar pilihan dari Januari sampai Desember, sedangkan tanggal dan tahun masih kosong karena biasanya akan diisi menggunakan JavaScript.
<label>Password</label>
        <input type="password" id="password">
Berikutnya terdapat input password dengan type="password" yang berfungsi untuk menyembunyikan teks yang diketik oleh pengguna agar lebih aman.
<button type="submit" class="submit">Submit</button>
        <button type="reset" class="reset">Reset</button>
Di bawahnya terdapat dua tombol yaitu tombol submit untuk mengirim data dan tombol reset untuk mengosongkan semua input dalam form. Masing-masing tombol memiliki class untuk mengatur tampilannya melalui CSS.


</form>

    <h2>Data Mahasiswa</h2>

    <table>
Setelah form, terdapat judul kedua yaitu <h2>Data Mahasiswa</h2> yang menandai bagian tabel. Tabel digunakan untuk menampilkan data mahasiswa yang telah diinput.
<thead>
            <tr>
                <th>NIM</th>
                <th>Nama</th>
                <th>Alamat</th>
                <th>JK</th>
                <th>TTL</th>
                <th>Password</th>
                <th>Aksi</th>
            </tr>
        </thead>
Bagian tabel terdiri dari <thead> yang berisi header kolom seperti NIM, Nama, Alamat, Jenis Kelamin, Tanggal Lahir, Password, dan Aksi. Kolom aksi biasanya digunakan untuk tombol seperti edit atau hapus data.
<tbody id="tableBody"></tbody>
    </table>
    </body>
</html>
Terakhir terdapat <tbody id="tableBody"></tbody> yang merupakan tempat data mahasiswa akan ditampilkan. Bagian ini masih kosong karena data biasanya dimasukkan secara dinamis menggunakan JavaScript.




# Lab7Web

|   INDIRA ALINE       |    312010042       |
| ---------------------|--------------------|
|  TI.20.A.1           | PEMROGRAMAN WEB    |
|  PERTEMUAN 9         | PRAKTIKUM 7        |

Di pertemuan ini akan mempelajari **PHP DASAR** dengan beberapa program code ***PHP*** nya.

## PHP DASAR

## LANGAKAH-LANGKAH PRAKTIKUM

## 1). INSTALL XAMPP UNTUK SERVER 

![Install-XAMPP](img/xampp_location.png)

**PENJELASAN**

Install **XAMPP** untuk ***WEB SERVER*** dan kemudian ekstrak file nya dan sesuaikan dimana Anda menyimpan file tersebut.

## 2). MENJALANKAN WEB SERVER

![Aktifkan-XAMPP](img/server.png)

**PENJELASAN**

Mengaktifkan **XAMPP** dengan menekan tombol  **START SERVER APACHE** Seperti gambar di atas.


## 3). MEMULAI PHP 

Buat folder lab7_php_dasar pada root directory web server (c:xampp\htdocs)

![Folder-lab7-php-dasar](img/start.png)

**PENJELASAN**

Di atas saya membuat folder ***lab7_php_dasar*** yang dimana folder itu disimpan dalam folder **Lab7Web** untuk repository. Kemudian akses directory pada web server dengan mengakses URL : http://localhost/Lab7Web/lab7_php_dasar/

![Tampilan-server](img/akses_directory.png)

**PENJELASAN**

Di atas adalah contoh dari tampilan dalam URl atau tampilan server folder tersebut.


## 4). PHP DASAR
Buat file baru dengan nama **php_dasar.php** pada directory tersebut kemudian buat kode seperti berikut.

![php-dasar](img/php_dasar.png)

**PENJELASAN** 

Kemudian akses URL untuk hasil nya : http://localhost/Lab7Web/lab7_php_dasar/php_dasar.php

Di atas adalah contoh hasil dari penggunaan **PHP** dalam file html atau **embed**

**code php**
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World";
    ?>
</body>
</html>
```


## 5). VARIABLE PHP

Menambahkan Variable pada program.

![variable-php](img/variable.png)

**PENJELASAN**

Di atas adalah contoh penggunaan Variable di **PHP**

**code php**
```php
<h2>Menggunakan Variable</h2>
    <?php
       $nim = "0411500400";
       $nama = 'Abdullah';
       echo "NIM : " . $nim . "<br>";
       echo "Nama : $nama"; 
    ?>
```

## 6). PREDEFINE VARIABLE $_GET

Menggunakan **Predefine Variable**

![predefine-variable](img/predefine_variable.png)

**PENJELASAN**

Buat file baru dalam directory **lab7_php_dasar** dengan nama file nya adalah **latihan2.php** dan buat code seperti dibawah dan untuk mengaksesnya gunakan URL: http://localhost/Lab7Web/lab7_php_dasar/latihan2.php?nama=Indira
dan tampilan nya seperti gambar diatas.

**code php**
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Dasar</title>
</head>
<body>
    <!-- Variable $_GET -->
    <h2>Predefine Variable</h2>
<?php
    echo 'Selamat Datang ' . $_GET['nama'];
?> 
</body>
</html>
```

## 7). MEMBUAT FORM INPUT

![membuat-form-input](img/form_input.png)

**PENJELASAN**

Buat file baru dengan nama **latihan3.php** dalam directory folder **lab7_php_dasar**  di atas adalah hasil atau tampilan dalam membuat ***form*** dalam php dengan variable $_POST contoh code seperti dibawah.

**code php**
```php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PHP Dasar</title>
</head>
<body>
    <h2>Form Input</h2>
    <form method="post">
        <label for="Nama">Nama: </label>
        <input type="text" name="nama">
        <input type="submit" value="Kirim">
    </form>
    <?php
        echo 'Selamat Datang ' . $_POST['nama'];
    ?>
</body>
</html>
```

## 8). OPERATOR 

![operator](img/operator.png)

**PENJELASAN**

Membuat ***OPERATOR*** dalam php seperti contoh hasil tampilan di atas beserta code nya.

**code php**
```php
    <?php
        $gaji = 1000000;
        $pajak = 0.1;
        $thp = $gaji - ($gaji*$pajak);
        echo "Gaji sebelum pajak = Rp. $gaji <br>";
        echo "Gaji yang dibawa pulang = Rp. $thp";
    ?>
```

## 9). KONDISI IF

![kondisi-if](img/kondisi_if.png)

**PENJELASAN**

Pengondisian **IF ELSE** seperti hasil tampilan dan code pada gambar atas.

**code php**
```php
    <?php
        $nama_hari = date("l");
        if ($nama_hari == "Sunday") {
            echo "Minggu";
        } elseif ($nama_hari == "Monday") {
            echo "Senin";
        } else {
            echo "Selasa";
        }
    ?>
```

## 10). KONDISI SWITCH

![kondisi-swicth](img/kondisi_switch.png)

**PENJELASAN**

Contoh penggunaan pengondisian **SWICTH CASE** dengan ***Break*** seperti contoh hasil di atas beserta code.

**code php**
```php
<?php
        $nama_hari = date("l");
        switch ($nama_hari) {
            case "Sunday":
                 echo "Minggu";
                 break;
            case "Monday":
                echo "Senin";
                break;
             case "Tuesday":
                 echo "Selasa";
                break;
            default:
                echo "Sabtu"; 
            }
            echo "/$nama_hari";
    ?>
```

## 11). PERULANGAN FOR

![perulangan-for](img/perulangan_for.png)

**PENJELASAN**

Menggunakan **PERULANGAN FOR** seperti hasil dan code di atas.

**code php**
```php
<?php
        echo "Perulangan 1 sampai 10 <br />";
        for ($i=1; $i<=10; $i++) {
            echo "Perulangan ke: " . $i . '<br />';
}
        echo "Perulangan Menurun dari 10 ke 1 <br />";
        for ($i=10; $i>=1; $i--) {
            echo "Perulangan ke: " . $i . '<br />';
}
?>
```

## 12). PERULANGAN WHILE

![perulangan-while](img/perulangan_while.png)

**PENJELASAN**

Menggunakan **PERULANGAN WHILE** seperti hasil gambar dan code di atas.

**code php**
```php
<?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    while ($i<=10) {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
}
?> 
```

## 13). PERULANGAN DOWHILE

![perulangan-dowhile](img/perulangan_dowhile.png)

**PENJELASAN**

Menggunakan **PERULANGAN DOWHILE** seperti hasil gambar di atas dan beserta code php.

**code php**
```php
<?php
    echo "Perulangan 1 sampai 10 <br />";
    $i=1;
    do {
        echo "Perulangan ke: " . $i . '<br />';
        $i++;
    } while ($i<=10);
?>  
```

------------------------------------------------------------------------------------------------------------------------------------------------

## PERTANYAAN DAN TUGAS

Buatlah program **PHP** sederhana dengan menggunakan ***form input*** yang menampilkan **nama** , **tanggal lahir** dan **pekerjaan** . Kemudian tampilkan outputnya dengan menghitung umur berdasarkan inputan **tanggal lahir** . Dan pilihan **pekerjaan** dengan gaji yang berbeda-beda sesuai pilihan **pekerjaan**.

![Tugas](img/tugas.png)

**Coding**
````php
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tugas</title>
</head>
<body>
   <h2>TUGAS</h2>
    <form class="form" method="post" >
            <label>Nama: </label>
            <br>
            <input type="text" name="nama">
            <br>
            <label>Tanggal Lahir: </label>
            <br>
            <input type="text" name="tgl_lahir">
            <br>
            <label>Pekerjaan: </label>
            <br>
            <select name='pekerjaan'>
                <option value="-">>---Pilih Pekerjaan---<</option>
                <option value='Operator'>Operator</option>
                <option value='Staff Admin'>Staff Admin</option>
                <option value='HRD'>HRD</option>
                <option value='Maintenance'>Maintenance</option>
                <option value="QC">QC</option>
            </select>
            <br>
            <br>
            <button type="submit">Kirim</button>
    </form>
    <h2>HASIL</h2>

    <?php
        # Memanggil Nama
        echo 'Nama: ' . $_POST['nama'];

        # Merubah Tanggal Lahir menjadi Umur (Tahun)
        $tgl_lahir = @$_POST['tgl_lahir'];

        $lahir = new DateTime($tgl_lahir);
        $hari_ini = new DateTime();

        $diff = $hari_ini->diff($lahir);

        # Memanggil fungsi umur yg sudah dibuat diatas
        echo "<br> Umur: ". $diff->y ." Tahun";

        # Memanggil pekerjaan
        echo "<br> Pekerjaan: ". $_POST['pekerjaan'];

        # Kondisi if pekerjaan untuk menentukan gaji
        $pekerjaan = @$_POST['pekerjaan'];

        if($pekerjaan == "Operator"){
            echo '<br> Gaji: Rp. 6.000.000,-';
        }elseif($pekerjaan == "Staff Admin"){
            echo '<br> Gaji: Rp. 7.500.000,-';
        }elseif($pekerjaan == "HRD"){
            echo '<br> Gaji: Rp. 10.000.000,-';
        }elseif($pekerjaan == "Maintenance"){
            echo '<br> Gaji: Rp. 9.000.000,-';
        }elseif ($pekerjaan == "QC"){
            echo '<br> Gaji: Rp. 7.000.000,-';
        }

    ?>
  </body>
</html>
````

------------------------------------------------------------------------------------------------------------------------------------------------

## TERIMA KASIH
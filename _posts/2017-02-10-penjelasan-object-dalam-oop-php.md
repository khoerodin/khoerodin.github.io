---
title: "#4. Penjelasan Object dalam OOP PHP"
date: '2017-02-10 15:30:00'
description: Artikel Seri Belajar Mudah OOP PHP, Apa itu Object dalam OOP PHP ? Di sini akan saya jelaskan...
tags:
- BelajarOOPPHP
published: true
---

**Object** adalah hasil konkrit atau *hasil cetakan* dari sebuah **class**. Sebagai contoh pada artikel sebelumnya saya telah membuat **Class User** maka object-nya adalah para User atau *account*, misalnya *Khoerodin*, *Andi* dan *Bagus*. Berikut contohnya, silakan praktekkan di komputer masing-masing ya, karena akan lebih faham jika dipraktekkan :smile:

```
class User {
    var $name;
    var $username;
    var $brithdate;
    var $address;

  function showBio()
    {
        echo "<b>Show Bio</b><br />";
        echo "<b>Name:</b> " . $this->name;
        echo "<br />";
        echo "<b>Username:</b> " .$this->username;
        echo "<br />";
        echo "<b>Brithdate:</b> " .$this->brithdate;
        echo "<br />";
    }

    function showAddress()
    {
        echo "<b>Show Address</b><br />";
        echo $this->address;
    }
}
// buat objek dari class User (instansiasi)
$Khoerodin = new User();

// set property
$Khoerodin->name = "Khoerodin";
$Khoerodin->username = "khoerodin";
$Khoerodin->brithdate = "01 Januari 2017";
$Khoerodin->address = "Ciamis, Indonesia";
  
// tampilkan property
echo "<b>Name:</b> " . $Khoerodin->name;
echo "<br />";
echo "<b>Username:</b> " .$Khoerodin->username;
echo "<br />";
echo "<b>Brithdate:</b> " .$Khoerodin->brithdate;
echo "<br /><br />";
  
// tampilkan method
echo $Khoerodin->showBio();
echo "<br />";
echo $Khoerodin->showAddress();
echo "<br /><br />";

// sekarang buat object Andi
$Andi = new User();

// set property
$Andi->name = "Andi";
$Andi->username = "andi";
$Andi->brithdate = "02 Januari 2017";
$Andi->address = "Cilacap, Indonesia";

// tampilkan property
echo "<b>Name:</b> " . $Andi->name;
echo "<br />";
echo "<b>Username:</b> " .$Andi->username;
echo "<br />";
echo "<b>Brithdate:</b> " .$Andi->brithdate;
echo "<br /><br />";

// tampilkan method
echo $Andi->showBio();
echo "<br />";
echo $Andi->showAddress();
echo "<br /><br />";
```

Hasilnya akan seperti ini
![Contoh Object PHP](https://raw.githubusercontent.com/khoerodin/khoerodin.github.io/master/assets/images/object-php.png "Contoh Object PHP")
---
title: "#4. Penjelasan Object dalam OOP PHP"
date: '2017-02-10 15:30:00'
description: Artikel Seri Belajar Mudah OOP PHP, Apa itu Object dalam OOP PHP ? Di sini akan saya jelaskan...
tags:
- BelajarOOPPHP
published: true
---

**Object** adalah hasil konkrit atau *hasil cetakan* dari sebuah **class**. Sebagai contoh pada artikel sebelumnya saya telah membuat **Class User** maka object-nya adalah para User atau *account*, misalnya *Khoerodin*, *Andi* dan *Bagus*. Berikut contohnya, silakan praktekkan di komputer masing-masing ya, karena akan lebih faham jika dipraktekkan :smile:

```php
class User {
    var $name;
    var $username;
    var $brithdate;
    var $address;

    function showSalam()
    {
        echo "<b>Salam...</b><br />Semoga sehat selalu... :)";
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
echo $Khoerodin->showSalam();
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
echo $Andi->showSalam();
echo "<br /><br />";
```

Mari kita bahas satu persatu.. :smile:

```php
class User {
...
```

Ini adalah mendefinisikan **Class** baru dengan nama **User**, diikuti pembuka kurung kurawal untuk mengawali Class dan tentunya pada baris terakhir ditutup oleh penutup kurung kurawal.

```php
...
    var $name;
    var $username;
    var $brithdate;
    var $address;
...
```

Baris selanjutnya ialah mendefinisikan property, dengan didahului menggunakan keyword **var**. Selain keyword **var** bisa saja menggunakan keyword **public** atau **protected** atau **private**, tapi di sini saya menggunakan **var**. Dalam artikel ini bisa kita abaikan saja pertanyaan *Apa sih fungsi var, public, protected dan private?* Karena bahasan mengenai keyword **public**, **protected** dan **private** akan dibahas dalam artikel tersendiri yaitu tentang **pewarisan**.

```php
...
    function showSalam()
    {
        echo "<b>Salam...</b><br />Semoga sehat selalu... :)";
    }
...
```

Ini adalah **method**, seperti yang sudah saya jelaskan pada <a href="https://khoerodin.id/method-dalam-oop-php/" target="_blank">artikel yang lain</a>.

```php
...
$Khoerodin = new User();
...
```

Nah ini adalah **instansiasi object** yaitu cara membuat **object** dari sebuah **class** yang dalam hal ini yaitu class `User`.

```php
...
$Khoerodin->name = "Khoerodin";
$Khoerodin->username = "khoerodin";
$Khoerodin->brithdate = "01 Januari 2017";
$Khoerodin->address = "Ciamis, Indonesia";
...
```

Baris berikutnya yaitu memberikan nilai kepada `property` yang berada dalam obejct **Khoerodin**

```php
...
echo "<b>Name:</b> " . $Khoerodin->name;
echo "<br />";
echo "<b>Username:</b> " .$Khoerodin->username;
echo "<br />";
echo "<b>Brithdate:</b> " .$Khoerodin->brithdate;
echo "<br /><br />";
...
```

Selanjutnya yaitu memanggil property yang isinya menampilkan nilai yaitu berupa nilai yang telah diberikan kepada **property dalam method Khoerodin**.

```php
...
echo $Khoerodin->showSalam();
...
```

Ini untuk memanggil method **showSalam()** dari class **Khoerodin**.

### Objek Sebagai Entitas Terpisah
Setiap objek merupakan bagian terpisah, pada contoh baris `code` di atas kita membuat object baru yaitu obejct **Andi**. Sama seperti object **Khoerodin** object **Andi** ini juga berasal dari satu class yang sama yaitu class **User**. Semua method dan property dalam obejct **Andi** akan sama persis dengan method dan property dalam object **Khoerodin**. Tapi object **Khoerodin** dan object **Andi** merupakan entitas berbeda atau terpisah, sehigga kita bisa memberikan nilai yang berbeda pada masing-masing object sebagaimana contoh dalam baris `code`. Coba deh jalankan baris `code` di atas biar lebih gamblang dan nanti hasilnya harusnya gini:

![Contoh Object PHP](https://raw.githubusercontent.com/khoerodin/khoerodin.github.io/master/assets/images/object-php.png "Contoh Object PHP")
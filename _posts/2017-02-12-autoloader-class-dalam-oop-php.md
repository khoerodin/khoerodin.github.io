---
title: "#7. Autoloader Class dalam OOP PHP"
date: '2017-02-12 21:00:00'
description: Artikel Seri Belajar Mudah OOP PHP, Apa itu Autoloader Class dalam OOP PHP ? Di sini akan saya jelaskan...
tags:
- BelajarOOPPHP
published: true
---

Umumnya pada pembuatan aplikasi berbasis _Object Oriented Programming_,  _programmer_ membuat setiap _class_ dalam satu _file_ tersendiri dan jika akan menggunakannya _programmer_ meng-*include*-kan satu per satu _file class_ pada permulaan baris kode. Ini bukanlah masalah jika hanya melakukan _include_ satu, dua atau lima _file_, tapi jika puluhan? ratusan bahkan lebih?

Mulai PHP 5 masalah itu sudah bisa diatasi dengan mudah. Misal kita membuat sebuah _class_ `Name` dan disimpan dalam _file_ `Name.php`: 

```php
class Name {
    function showName($name)
    {
    	echo 'Nama saya ' . $name . ' ';
    }
}
```

Buat lagi _class_ yaitu _class_ `Address` dan disimpan dalam _file_ `Address.php`.

```php
class Address {
    function showAddress($address)
    {
    	echo 'Alamat saya ' . $address;
    }
}
```

Selanjutnya kita panggil dua buah _class_ tersebut dalam satu _file_ `index.php`

```php
include 'Name.php';
$name = new Name();
$name->showName('Khoerodin');

include 'Address.php';
$address = new Address();
$address->showAddress('Ciamis');
```

Jika kode diatas dijalankan maka akan menghasilkan output `Nama saya Khoerodin Alamat saya Ciamis`. Kode tersebut benar alias tidak ada yang salah, namun seperti yang saya tulis di awal, bagaimana jika *class*nya puluhan bahkan ratusan? tentu akan merepotkan. Kita ubah `index.php` jadi seperti ini:

```php
spl_autoload_register(function ($class) {
    include $class . '.php';
});

$name = new Name();
$name->showName('Khoerodin');

$address = new Address();
$address->showAddress('Ciamis');
```

Coba jalankan kode tersebut. Ya inilah solusinya, kita tidak usah repot-repot meng-*include* satu per satu _file class_ yang dibutuhkan karena akan repot jika _class_ yang dibutuhkan tidak sedikit. Dengan ini PHP otomatis akan memanggil/melakukan `include` ketika `new Class()` dideklarasikan.

`spl_autoload_register()` fungsinya untuk me*register function* atau *static method*,  selanjutnya ketika `new Class()` dideklarasikan PHP akan melakukan antrian (queue/stack) dan memanggil secara berurutan. Mudah kan? :smile: ayo tetap semangaaat :muscle: :muscle: :muscle: .
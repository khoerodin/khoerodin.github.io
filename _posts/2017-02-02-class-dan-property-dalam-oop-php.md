---
title: "#2. Class dan Property dalam OOP PHP"
date: '2017-02-02 17:30:00'
description: >-
  Artikel Seri Belajar Mudah OOP PHP, Apa itu Class dan Property dalam
  OOP PHP ? Di sini akan saya jelaskan...
tags:
- BelajarOOPPHP
published: true
---

Setelah dalam[ artikel sebelumnya](http://khoerodin.id/apa-itu-oop-object-oriented-programming/) membahas apa itu OOP, kali ini akan coba saya jelaskan apa itu Class dan Property.

## Class
Simplenya Class adalah *blueprint* dari object. Class digunakan sebagai kerangka dasar atau cetakan yang menyimpan property dan Method, dan yang akan kita pakai adalah hasil cetakan tersebut yaitu Object. Aturan penamaan Class diawali dengan huruf atau underscore untuk karakter pertama, kemudian boleh diikuti dengan huruf, underscore atau angka untuk karakter kedua dan selanjutnya. Masih bingung ya? Berikut contoh cara penulisan Class dalam PHP, dalam contoh di bawah saya buat Class User

```
// diawali dengan kata class diikuti dengan nama class
// setelah nama class diikuti kurung kurawal buka 
// dan diakhiri kurung kurawal tutup

class User {
	// isi class nanti di sini
	// isi dari class bisa property dan method
	// property dan method akan dijelaskan kok
	// jangan khawatir...
}
```

## Property
Property sebenarnya hanyalah sebuah *Variable* yang terletak dalam sebuah Class. Dalam literatur yang lain Property disebut juga dengan *Attribute*. Cara penulisan Property ialah dengan didahului oleh **var** atau **visibility keyword** yaitu **public** atau **protected** atau **private** dan diikuti dengan penulisan nama Variable sebagaimana biasanya dalam PHP yaitu diawali dengan huruf atau underscore untuk karakter pertama, kemudian boleh diikuti dengan huruf, underscore atau angka untuk karakter kedua dan selanjutnya. Perhatikan contoh di bawah:

```
class User {
    var $name;
    public $username;
    protected $brithdate;
    private $address;
}
```
terus itu *visibility keyword* dalam property untuk apa? sabar..... akan dibahas dalam artikel tersendiri kok :smiley:
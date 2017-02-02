---
title: "#2. Class dan Property dalam OOP PHP"
date: '2017-02-02 17:30:00'
description: Artikel Seri Belajar Mudah OOP PHP, Apa itu Class dan Property dalam
  OOP PHP ? Disini akan saya jelaskan...
tags:
- Belajar Mudah OOP PHP (Series)
published: 'true'
---

Setelah dalam[ artikel sebelumnya](http://khoerodin.id/apa-itu-oop-object-oriented-programming/) membahas apa itu OOP, kali ini akan coba saya jelaskan apa itu Class dan Property.

## Class
Simplenya Class adalah *blueprint* dari object. Class digunakan sebagai kerangka dasar atau cetakan yang menyimpan property dan Method, dan yang akan kita pakai adalah hasil cetakan tersebut yaitu Object. Masih bingung ya? Berikut contoh cara penulisan Class dalam PHP, dalam contoh dibawah saya buat Class User

```
// diawali dengan kata class diikuti dengan nama class
// setelah nama class diikuti kurung kurawal buka 
// dan diakhiri kurung kurawal tutup

class User {
	// isi class nanti disini
	// isi dari class bisa property dan method
	// property dan method akan dijelaskan kok
	// jangan khawatir...
}
```

## Property
Property sebenarnya hanyalah sebuah *Variabel* yang terletak dalam sebuah Class. Dalam literatur yang lain Property disebut juga dengan *Attribute*. Cara penulisan Property ialah dengan didahului oleh Visibility keyword yaitu public atau protected atau private dan diikuti dengan penulisan Variable sebagaimana biasanya dalam PHP. Perhatikan contoh dibawah:

```
class User {
	private $id;
	public $username;
	public $name;
	public $email;
}
```
terus itu Visibility keyword dalam property untuk apa? sabar..... akan dibahas dalam artikel selanjutnya :smiley:
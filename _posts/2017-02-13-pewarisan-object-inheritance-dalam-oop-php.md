---
title: "Pewarisan (Obejct Inheritance) dalam OOP PHP"
date: '2017-02-13 10:08:00'
description: Apa itu Constructor dan Destructor dalam OOP PHP ? PHP menyediakan method khusus yang berjalan ketika sebuah object mulai dibuat dan dimatikan, yaitu method __construct() yang disebut constructor dan method __destruct() yang disebut destructor
tags:
- BelajarOOPPHP
published: true
---

Pewarisan atau _inheritance_ dalam _Object-Oriented PHP_ adalah menurunkan _property_ dan _method_ baik `public` maupun `protected` kepada _class_ lain. Ingat ya, hanya `public` dan `protected`. 

Konsep pewarisan ini sangat berguna jika kita ingin membuat _class_ lagi yang memiliki fungsi mirip dengan _class_ yang sudah ada, sehingga tidak usah membuat lagi _method_ atau _property_ yang memiliki fungsi mirip atau sama. Dengan _inheritance_ kita bisa menghindari duplikasi kode program, atau disebut juga _code reuse_.

Lebih jelasnya mari perhatikan dan praktekkan kode di bawah ini, keterangan langsung saya sematkan pada baris kode agar memudahkan. :blush:

```php
class User
{
    public $name;
    public $username;
    protected $brithdate = '03 Juni 2016';
    private $address = 'Yogyakarta';
    protected $gender = 'Male';

    public function showSalam(){
        echo "Salam... nama saya $this->name <br/>";
    }
}

// membuat class baru
// dengan extends class User
// artinya mewarisi property dan method
// dari class User 
class Bio extends User
{
    // mengubah visibility keyword menjadi piblic
    // juga mengubah nilai menjadi 01 Januari 2017
    public $brithdate = '01 Januari 2017';

    public function showBio(){
        echo "Username : $this->username <br/>";
        echo "Brithdate : $this->brithdate <br/>";
        echo "Gender : $this->gender <br/>";
    }

    public function showAddress(){
        echo "Address : $this->address";
    }
}

// membuat object Bagus
$Bagus = new Bio();

// memberikan nilai kepada property
$Bagus->name = 'Bagus';
$Bagus->username = 'tubagus';

// tidak bisa memberikan nilai:
// Cannot access protected property
// karean property gender adalah protected
// hanya boleh diakses dari dalam class itu sendiri
// dan dari dalam extended class 
$Bagus->gender = 'Female';

// memanggil property
// kode ini berjalan
echo $Bagus->username . '<br/>';

// Undefined property. 
// karena property gender adalah protected
echo $Bagus->gender;

// dalam class User property brithdate adalah protected
// tapi setelah di extends di class Bio
// diubah public dan di ganti nilainya
// jadi 01 Januari 2017
echo $Bagus->brithdate . '<br/>';

// memanggil method
// kode ini berjalan
$Bagus->showSalam();
$Bagus->showBio();

// PHP Notice:  Undefined property.
// Karena address adalah private
$Bagus->showAddress();
```

Ada yang ditanyakan? jangan sungkan untuk berkomentar sambil ngopi-ngopi.. :smiley: :coffee:
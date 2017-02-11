---
title: "#6. Enkapsulasi (Public, Protected, Private) pada OOP PHP"
date: '2017-02-10 20:38:00'
description: Artikel Seri Belajar Mudah OOP PHP, Apa itu Enkapsulasi (Public, Protected, Private) dalam OOP PHP ? Di sini akan saya jelaskan...
tags:
- BelajarOOPPHP
published: false
---

**Property**, **Method** dan **Constanta** dapat di kontrol aksesnya menggunakan visibility keyword. Terdapat tiga keyword yaitu **public**, **protected** dan **private**. Cara menggunakannya yaitu dengan memberikan prefix berupa salah satu dari tiga visibility keyword pada **Property**, **Method** dan **Constanta**.

Berikut penjelasan untuk masing-masing dari ketiga visibility keyword:

1. **Public**, Artinya Method, Property atau Constanta dapat diakses dari dalam dan luar Class. 
2. **Protected**, Artinya Method, Property atau Constanta dapat diakses dari dalam Class dan Extended/Inherited Class (akan dijelaskan pada artikel selanjutnya). 
3. **Private**, Artinya Method, Property atau Constanta dapat diakses dari dalam Class.

### Property Visibility
Property harus didefinisikan sebagai public, protected atau private, jika dideklarasikan menggunakan **var** maka otomatis didefinisikan sebagai public.

```
class User {
    public $name = 'Khoerodin';
    protected $username = 'khoerodin';
    private $brithdate = '01 Januari 2017';

    function showBio()
    {
        echo $this->name;
        echo $this->username;
        echo $this->brithdate;
    }
}

$User = new User();
echo $User->name; // Menampilkan Name
echo $User->username; // Fatal Error
echo $User->brithdate; // Fatal Error
$User->showBio(); // Menampilkan Name, Username dan Brtihdate
```

### 
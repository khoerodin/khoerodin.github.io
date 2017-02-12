---
title: "#5. Konstanta Class dalam OOP PHP"
date: '2017-02-12 08:06:00'
description: Artikel Seri Belajar Mudah OOP PHP, Apa itu Konstanta Class dalam OOP PHP ? Di sini akan saya jelaskan...
tags:
- BelajarOOPPHP
published: true
---

Konstanta Class atau **Class Constants** dapat juga didefinisikan di dalam sebuah *Class* dan sama seperti <a href="https://khoerodin.id/konstanta-dalam-php/" target="_blank">konstanta regular</a> konstanta *class* juga tidak dapat diubah nilainya. Nilai atau *value* dari konstanta harus berupa ekspresi *konstan* atau ekspresi tetap yaitu bukan merupakan *variable*, *property* atau *function* dan lain-lain.

### Mendefinisikan Konstanta Class
Berikut cara mendefinisikan konstanta dalam sebuah *class*

```php
class User
{
    const JK = 'Laki-laki';
}
```

Agar lebih mudah membedakan antara *variable* dengan konstanta, konstanta biasanya ditulis menggunakan huruf kapital.

### Cara Akses atau Menggunakan Konstanta Class
**1. Akses dari dalam Class itu sendiri**

Caranya yaitu dengan menggunakan *keyword self* diikuti dengan titik dua ganda *(double colon)* dan konstanta.

```php
class User
{
    const JK = 'Laki-laki';

    function showJK() {
        echo self::JK;
    }
}
```

**2. Akses dari luar Class**

Menggunakan nama *class*, *double colon* dan konstanta.

```php
class User
{
    const JK = 'Laki-laki';
}

echo User::JK;
```

**3. Akses dari object**

Caranya yaitu menggunakan *object*, *double colon* dan konstanta.  

```php
class User
{
    const JK = 'Laki-laki';
}

$objek = new User();
echo $objek::JK; // Mulai PHP 5.3.0
```

**3. Akses dari variable yang ber-value nama sebuah class**

Nama *class* terlebih dahulu dijadikan *variable value*.

```php
class User
{
    const JK = 'Laki-laki';
}
$classname = "User";
echo $classname::JK; // Mulai of PHP 5.3.0
```

### Tambahan
Mulai PHP 5.6.0 Konstanta *Class* juga dapat ber-*value* dari konstanta *regular*.

```php
const SATU = 1;

class User {
    // Mulai PHP 5.6.0
    const DUA = SATU * 2;
    const TIGA = SATU + self::DUA;
    const EMPAT = 'Nilai dari TIGA adalah '.self::TIGA;
}
```

Mulai PHP 7.1.0 **Visibility Modifier** juga bisa ditambahkan ke Konstanta *Class*.

```php
class User {
    // Mulai PHP 7.1.0
    public const JK = 'Laki-laki';
    private const PENDIDIKAN = 'Strata satu (S1)';
}
echo User::JK . "<br/>";
echo User::PENDIDIKAN;
```

Jika kode diatas dijalankan pasti akan error, karena `const PENDIDIKAN` adalah `private`.

Apa sih *Visibility Modifier* ? akan dijelaskan kok dalam artikel tersendiri tentang **encapsulation**, mungkin kali ini bisa diabaikan tentang *Visibility Modifier*.
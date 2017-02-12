---
title: "#3. Method dalam OOP PHP"
date: '2017-02-09 19:00:00'
description: Artikel Seri Belajar Mudah OOP PHP, Apa itu Method dalam OOP PHP ? Di sini akan saya jelaskan...
tags:
- BelajarOOPPHP
published: true
---

**Method** adalah tindakan atau aksi dari suatu *class*. Pada <a href="https://khoerodin.id/class-dan-property-dalam-oop-php/" target="_blank">artikel sebelumnya</a> pernah diberikan contoh *class* `User`, maka contoh methodnya adalah **register user**, **edit user**, **delete user**, **follow user** dan *method-method* atau aksi-aksi lain yang diinginkan untuk diterapkan dalam *class* `User`.

Mudahnya *method* adalah **function** yang berada di dalam suatu *class*. Ketika membuat *function* di luar *class/object* maka disebut *function*, namun ketika membuat *function* di dalam *class/object* maka disebut *method*. 

Semua sifat-sifat *function* bisa diterapkan ke dalam *method*, seperti parameter, mengembalikan nilai (akan dibahas pada artikel selanjutnya), dan lain-lain. *method* juga seperti *property* yaitu bisa memiliki salah satu *visibility keyword: Public* atau *Protected* atau *Private*. 

Berikut contoh *method*:

```php
class User {
	public function showBio()
	{
		//
	}

	private function showAddress()
	{
		//
	}
}
```

Cukup disini tentang *method*, semangat ganss... :muscle: :muscle: :muscle: dan ikuti terus <a href="https://khoerodin.id/tag/#BelajarOOPPHP" target="_blank">#BelajarOOPPHP</a>.
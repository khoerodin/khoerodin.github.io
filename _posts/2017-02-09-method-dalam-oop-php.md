---
title: "#3. Method dalam OOP PHP"
date: '2017-02-09 19:00:00'
description: Artikel Seri Belajar Mudah OOP PHP, Apa itu Method dalam OOP PHP ? Di sini akan saya jelaskan...
tags:
- BelajarOOPPHP
published: true
---

**Method** adalah tindakan atau aksi dari suatu *Class*. Pada <a href="https://khoerodin.id/class-dan-property-dalam-oop-php/" target="_blank">artikel sebelumnya</a> pernah diberikan contoh *Class* **User**, maka contoh methodnya adalah **register user**, **edit user**, **delete user**, **follow user** dan method-method atau aksi-aksi lain yang diinginkan untuk diterapkan dalam *class* User.

Mudahnya *Method* adalah **Function** yang berada di dalam suatu *Class*. Ketika membuat *Function* di luar *Class/Object* maka disebut *Function*, namun ketika membuat *Function* di dalam *Class/Object* maka disebut *Method*. 

Semua sifat-sifat Function bisa diterapkan ke dalam *Method*, seperti parameter, mengembalikan nilai (akan dibahas pada artikel selanjutnya), dan lain-lain. *Method* juga seperti *Property* yaitu bisa memiliki salah satu *Visibility Keyword* Public atau Protected atau Private. 

Berikut contoh *Method*:

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

Cukup disini tentang **Method**, semangat ganss... :muscle: :muscle: :muscle: dan ikuti terus <a href="https://khoerodin.id/tag/#BelajarOOPPHP" target="_blank">#BelajarOOPPHP</a>.
---
title: Pengelompokkan Route dalam Laravel
date: 2016-8-16
description: >-
  Memahami Route Groups atau pengelompokkan route oleh Laravel dengan mudah
tags:
  - laravel
  - routes
  - middleware
  - namespace
published: false
---

Salah satu kemudahan Laravel ialah masalah pengolahan route, seperti yang akan dibahas disini yaitu **Route Groups**. Dengan menggunakan Route Groups kita bisa mengumpulkan route berdasarkan group atau kelompok tertentu. Route Groups pada Laravel ada empat macam: 

1. Berdasarkan Middleware

Misal kita ingin mengelompokkan beberapa route ke dalam middleware `auth`

```php
Route::group(['middleware' => 'auth'], function () {
	Route::get('/', function ()    {
		// Uses Auth Middleware
  });

 	Route::get('user/profile', function () {
 		// Uses Auth Middleware
 	});
});
```

Eits.. ada yang masih bingung tentang middleware? 
> Middleware merupakan sebuah Class khusus yang berperan sebagai “penengah” antara request yang masuk dengan Controller yang dituju. Secara umum, prinsip kerja Middleware adalah mencegat request yang masuk untuk kemudian diproses terlebih dahulu sebelum diberikan kepada Controller yang dituju atau diarahkan ke Controller yang lain.

Begitu kira-kira penjelasan singkat tentang middleware, lebih lengkapnya baca di [tautan ini](http://id-laravel.com/post/middleware-manfaat-dan-penggunaannya/ "tautan ini") ya :blush:

2. Berdasarkan Namespace
3. Berdasarkan Sub-Domain
4. Berdasarkan Prefix

Lebih gampangnya ialah menyeragamkan prefix atau awalan route, misal kita ingin membuat route `/admin/messages`, `/admin/settings` dan `/admin/info` kita dapat dengan mudah mengelompokkannya seperti ini

```php
Route::group(['prefix'=>'admin'], function() {
	Route::get('messages', function() {
		return 'halaman admin > messages';
	});
	Route::get('settings', function() {
		return 'halaman admin > settings';
	});
	Route::get('info', function() {
		return 'halaman admin > info';
	});
});
```
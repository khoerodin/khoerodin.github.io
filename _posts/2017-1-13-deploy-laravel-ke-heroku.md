---
title: Deploy Laravel Ke Heroku
date: 2017-1-13
description: >-
  Langkah mudah deploy/install Laravel ke Heroku  
tags:
  - laravel
  - heroku
  - PaaS
published: true
---

Heroku merupakan _layanan cloud computing_ bertype <a href="https://rizkimufrizal.github.io/heroku-sebagai-komputasi-modern/" target="_blank">PaaS</a> _(Platform as a Service)_. Bagi para web developer lumayan lah versi gratisnya kalau hanya untuk sekedar demo aplikasi/website yang sedang dibangun.

![Laravel with Heroku](https://raw.githubusercontent.com/khoerodin/khoerodin.github.io/master/assets/images/laravel_heroku.jpg "Laravel with Heroku")

Sebelum dimulai, pastikan sudah punya akun Heroku ya, [baca ini dulu](https://devcenter.heroku.com/articles/getting-started-with-php "baca ini dulu").

#### Siap? Ayo kita mulai...

Buat project Laravel seperti biasa

```
$ laravel new herovel
...
$ cd herovel
```

#### Initialize Git

```
$ git init
$ git add .
$ git commit -m "initial commit laravel to heroku"
```

#### Membuat Procfile

```
$ echo web: vendor/bin/heroku-php-apache2 public/ > Procfile
$ git add .
$ git commit -m "procfile for heroku"
```

#### Create Heroku Apps

```
$ heroku create
```

#### Install Database Addons

```
// Jika menggunakan PostgreSQL
$ heroku addons:create heroku-postgresql:hobby-dev

// Ambil informasi koneksi
$ heroku config:get DATABASE_URL

// Maka akan muncul URL database dengan format:
// postgres://username:password@host:port/database_name
```

```
// Jika menggunakan MySQL
$ heroku addons:create cleardb:ignite

// Ambil informasi koneksi
$ heroku config:get CLEARDB_DATABASE_URL

// Maka akan muncul URL database dengan format:
// mysql://username:password@host/database_name?reconnect=true
````

#### Set ENV variables

```
// DB_HOST, DB_PORT, DB_DATABASE, 
// DB_USERNAME dan DB_PASSWORD 
// diambil dari URL database yang didapatkan ketika install database addons

$ heroku config:set \
APP_ENV=production \
APP_KEY=$(php artisan --no-ansi key:generate --show) \
APP_DEBUG=false \
APP_LOG=errorlog \
DB_CONNECTION=pgsql \
DB_HOST=host \
DB_PORT=port \
DB_DATABASE=database_name \
DB_USERNAME=username \
DB_PASSWORD=password
```

#### Push to Heroku and Migrate

```
$ git push heroku master
$ heroku run php artisan migrate
```

#### Open Apps
```
$ heroku open
```
Otomatis browser akan membuka aplikasi Heroku,
Tadaaaaa...... Laravel sudah di Heroku :smiley: :smiley: :smiley:

Mudah-mudahan bisa segera menyusul tutorial <a href="https://www.docker.com/" target="_blank">Docker</a> dan <a href="http://dokku.viewdocs.io/dokku/" target="_blank">Dokku</a>
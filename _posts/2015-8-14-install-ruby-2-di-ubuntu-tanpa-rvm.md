---
title: "Install Ruby 2 di Ubuntu Tanpa RVM"
date: 2015-8-14
description: Langkah mudah dan cepat install Ruby versi 2 di Ubuntu tanpa ribet mengggunakan Ruby Version Manager
tags:
- ruby
- ubuntu
- rvm
- programming
- web
- package
- brightbox
---

Ada banyak cara install Ruby versi 2.* di Ubuntu, salah satunya ialah menggunakan [RVM](https://rvm.io/ "RVM"), namun jika merasa ribet dengan RVM kita bisa mencoba menggunakan *Ruby Packages* dari [Brightbox](https://www.brightbox.com/docs/ruby/ubuntu/ "Brightbox").

Pada saat tulisan ini dibuat Brightbox menyediakan Ruby 1.8.7 sampai Ruby 2.3.

![Ruby Sticker from unixstickers.com](https://raw.githubusercontent.com/khoerodin/khoerodin.github.io/master/assets/images/ruby-sticker.jpg "Ruby Sticker from unixstickers.com")

## **Menambahkan repository**
Jika menggunakan **Ubuntu 14.04 atau yang terbaru**, gunakan perintah

```
$ sudo apt-get install software-properties-common
$ sudo apt-add-repository ppa:brightbox/ruby-ng
$ sudo apt-get update
```

jika **Ubuntu 12.04 atau sebelumnya**, gunakan perintah

```
$ sudo apt-get install python-software-properties
$ sudo apt-add-repository ppa:brightbox/ruby-ng
$ sudo apt-get update
```

Menginstall Package
Install Ruby sesuai versi yang diinginkan

```
$ sudo apt-get install ruby1.8 ruby1.9.3 ruby2.2
```

jika menginginkan juga **dev package**

```
$ sudo apt-get install ruby1.8-dev ruby1.9.3-dev ruby2.2-dev
```

Demikian, semoga berkah manfaat dan Happy Coding :blush: :coffee:
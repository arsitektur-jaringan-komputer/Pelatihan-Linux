<div align=center>

# Process and Monitoring

</div>

## Table of Contents

1. [Package dan Source Control](#package-dan-source-control)
2. [Process](#apa-itu-process)
3. [Perintah Terkait Process](#perintah-terkait-process)
4. [Resources Monitoring](#resources-monitoring)

## Package dan Source Control

Pada masa-masa awal Linux, program hanya didistribusikan sebagai kode sumber, bersama dengan halaman manual yang diperlukan, file konfigurasi yang diperlukan, dan banyak lagi. Saat ini, sebagian besar distributor Linux menggunakan program bawaan atau kumpulan program yang disebut package, yang disajikan kepada pengguna yang siap untuk diinstal pada distribusi tersebut. Berikut beberapa kkonsep dalam package management yang perlu diketahui :

- Package

  Package adalah suatu unit perangkat lunak yang telah dikemas bersama dengan informasi tambahan yang diperlukan untuk instalasi dan manajemen perangkat lunak tersebut. Contohnya adalah pacakge `.deb` jika di distro debian dan `.exe` jika pada windows.

- Package Manager

  Package manager adalah perangkat lunak yang dirancang untuk membantu pengguna mengelola instalasi, pembaruan, konfigurasi, dan penghapusan perangkat lunak pada sistem operasi. Package Manager dapat dikelompokkan menjadi 2 jenis yaitu `low-level` dan `high-level`. Seperti pada contoh dibawah ini :

  ![Pacakage-Manager](./assets/Package-Manager.jpg)

  contohnya dpkg pada debian hanya bisa menginstal package .deb yang sudah tersedia pada host saja, sedangkan apt bisa menginstal package .deb dan juga bisa menginstal package dependensinya dari repository. Package manager yang berada diatas package manager lainnya disebut dengan high-level package manager. Package manager yang berada dibawah package manager lainnya disebut dengan low-level package manager.

- Repository

  Repositori adalah penyimpanan sentral tempat paket perangkat lunak disimpan dan dikelola. Repositori ini berisi berbagai perangkat lunak yang telah dikompilasi untuk digunakan pada distribusi Linux tertentu. Repository ini yang nantinya akan diakses oleh package manager untuk menginstal package yang dibutuhkan. List konfigurasi dapat dikonfigurasi pada path `/etc/apt/sources.list` jika pada distro ubuntu. Contohnya ini adalah [repository ubuntu lokal yang ada di Indonesia](https://nugi.biz/2022/03/22/repository-lokal-indonesia-ubuntu-22-04-lts-jammy-jellyfish.xhtml).

- Dependency

  Dependency adalah suatu package yang dibutuhkan oleh package lainnya untuk bisa berjalan. Contohnya adalah package `libssl-dev` yang dibutuhkan oleh package `nginx` untuk bisa berjalan.

![Linux-package](./assets/linux-package.png)

Jadi kesimpulannya user linux akan menggunakan command package manager untuk menginstal package yang dibutuhkan. Package manager akan mengambil package yang dibutuhkan dari repository yang sudah dikonfigurasi sebelumnya. Package yang dibutuhkan tersebut bisa berupa package utama atau package dependensi. Package utama adalah package yang dibutuhkan oleh user untuk bisa berjalan. Package dependensi adalah package yang dibutuhkan oleh package utama untuk bisa berjalan.

## Command Package Management

Beberapa command yang dapat dilakukan untuk memanage package pada linux yang sering digunakan adalah sebagai berikut :

- `apt-get update`

  Command ini digunakan untuk mengupdate list package yang ada pada repository. Command ini harus dijalankan sebelum menginstal package agar package yang diinstal adalah package terbaru.

- `apt-get install <package-name>`
  Command ini digunakan untuk menginstal package yang dibutuhkan. Contohnya adalah `apt-get install nginx`.

- `apt-get remove <package-name>`
  Command ini digunakan untuk menghapus package yang sudah terinstal. Contohnya adalah `apt-get remove nginx`.

- `apt-get purge <package-name>`
  Command ini digunakan untuk menghapus package yang sudah terinstal beserta konfigurasinya. Contohnya adalah `apt-get purge nginx`.

- `apt-get autoremove`
  Command ini digunakan untuk menghapus package yang sudah terinstal dan tidak dibutuhkan oleh package lainnya. Contohnya adalah `apt-get autoremove`.

- `apt-get upgrade`
  Command ini digunakan untuk mengupgrade package yang sudah terinstal.

  Selain command command diatas masih banyak lagi command yang dapat digunakan untuk melihatnya dapat menggunakan command `apt-get --help` atau mengunjungi [link berikut](https://www.tecmint.com/useful-basic-commands-of-apt-get-and-apt-cache-for-package-management/).

## Apa Itu Process?

## Perintah Terkait Process

## Resources Monitoring

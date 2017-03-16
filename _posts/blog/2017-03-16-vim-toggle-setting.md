---
layout: post
title: "Vim Toggle Setting"
modified:
categories: blog
excerpt: "Cara mudah mengaktifkan dan menonaktifkan pengatuan di Vim yang sifatnya boolean"
tags: []
image:
  feature:
date: 2017-03-16T15:39:55-04:00
modified: 2016-06-01T14:19:19-04:00
comments: true
---

Kira-kira sampai saat ini saya sudah menggunakan Vim selama 9 bulan dan saya merasa nyaman menggunakannya hingga merasa kikuk jika harus menggunakan *editor* yang lain. Pada titik ini bisa dibilang saya mahir menggunakan Vim tetapi hal ini tidak membuat saya berhenti untuk mempelajari Vim. Vim itu luas jadi pasti ada saja hal-hal yang terlewatkan meskipun sifatnya dasar.

Baru-baru ini saya membeli 2 buah buku vim. Yang pertama adalah [Practical Vim](https://pragprog.com/book/dnvim2/practical-vim-second-edition) dan yang kedua [Painless Vm](https://leanpub.com/painless_vim). Judul yang pertama ditujukan bagi mereka yang sudah lancar menggunakan Vim tetapi menginginkan ilmu yang lebih sedangkan yang kedua ditargetkan untuk pemula.

Saat ini saya sedang membaca judul yang kedua karena ingin memastikan tidak ada ilmu dasar yang saya lewatkan. Dan ternyata ada!. Baru beberapa halaman membaca buku ini saya menemukan sebuah ilmu dasar baru yaitu tentang melakukan *togglet* terhadap konfigurasi di Vim yang sifatnya *boolean*.

Contohnya adalah `:set number` yang digunakan untuk menampilkan nomor baris di jendela Vim kita. Jika kita ingin menghilangkannya maka digunakan perintah yang berlawanan yaitu `:set nonumber`.

Nah daripada kita mesti mengetik bolak-balik di antara keduanya untuk mengaktifkan atau menonaktifkan *line number*, ada cara lain yang lebih simpel karena cukup dengan satu perintah kita bisa mengaktifkan mau pun menonaktifkan konfigurasi ini tergantung keadaan yang terpasang saat ini. Artinya jika saat ini dalam keadaan ada nomor baris maka perintah yang satu ini akan menghilankannya. Sebaliknya, jika saat ini tidak ada nomor baris maka menjalannya akan memunculkan si nomor baris.

Triknya adalah dengan menambahkan tanda ! pada akhir perintah seperti ini.

`:set number!`

Bentuk penambahan ! bisa digunakan pada perintah lain asal sifatnya *boolean*. Contoh lainnya adalah

`:set paste!`

Ada satu lagi selain tanda ! yang bisa ditambahkan yaitu tanda ?. Perintah *boolean* yang diakhiri tanda ? akan menampilkan konfigurasi yang terpasang saat ini.

---
layout: post
title: Nur Agus Suryoko
excerpt: "Infrastructure Architect, Virkea"
modified: 2017-03-21T14:17:25-04:00
categories: cerita
tags:
#image:
#  feature: so-simple-sample-image-1.jpg
#  credit: WeGraphics
#  creditlink: http://wegraphics.net/downloads/free-ultimate-blurred-background-pack/
comments: true
share: true
---

**Halo Mas Agus, perkenalan dulu ya**

Saya kenal linux pertama kali waktu semester 2 kuliah. Waktu itu distro yang pertama kali saya install adalah SuSE Linux (belum diambil alih sama Novell), SuSE 7 kalo tidak salah dan saat belajar Linux itulah saya pertama kali mengenal vi.

Berlanjut saya getol-getolnya belajar waktu itu mulai rame-rame ada wifi, jadi bisa "nembak" wifi kampus dari kosan, itu sekitar semester 6 kuliah. Kebetulan bapak saya juga baik, liat saya getol belajar Linux saya dibelikan 2 komputer, 1 laptop dan wireless-router. Tapi selama belajar Linux itu saya tidak menggunakan vi, saya menggunakan mcedit (mainly) dan nano (secondary).

Lompat ke 2008 ketika sudah mulai bekerja sebagai konsultan implementasi SAP saya menjadi konsultan SAP BASIS (bagian system dan infrastruktur). Pada saat itu mentor saya bilang *"kalau ngaku gemar Linux tapi tidak pake vi, itu namanya bohong"*. Malam hari setelah dibilang begitu, saya langsung belajar vi.

Pada tahun 2014 saya mencoba mendirikan startup bersama beberapa teman dan role saya masih sama di area system dan infrastruktur namun karena yang nge-trend pada saat ini adalah devops jadi saya (dan 1 orang teman) menamakan diri tim ops. Tugas kami adalah membuat developer semakin mudah bekerja dengan otomasi-otomasi, aplikasi semakin reliable dengan desain yang lebih baik, dll.

 Saat ini kami bekerja menggunakan mekanisme kanban dimana ide-ide kami tampung di "experiment" kemudian kita coba lakukan dan kalau sudah cukup percaya diri, kita anggap itu sebagai "production" yang artinya kurang lebih "ini adalah cara kita melakukan sesuatu". Karena sering kolaborasi (meskipun hanya 2 orang), kami memilih tool vim dan tmux untuk melakukan remote-pairing.

[![](/images/vim-banner.png)](http://agung-setiawan.com/bukuvim)

**Cool, menarik untuk dibahas satu-satu**

**Saat pertama belajar malam itu juga setelah dibilangin sama mentor Mas Agus, itu belajarnya lewat mana Mas?
internet? `:help`? atau yang lain?**

**Terus rasanya gimana pertama menginjakkan jari di vi, mengingat biasanya pakai mcedit (saya baru denger ini)**

Waktu malam-malam saya ngebut belajar itu tentu membuka lagi navigasi karena sudah lama tidak pakai vi jadi sudah banyak lupa. Memang waktu itu karena internet sudah cukup accessible saya langsung buka browser dan googling. Baru kemudian mengumpulkan cheatsheet sendiri untuk command-command sederhana seperti `dG`, `dgg`, dll (yang sampai sekarang kadang masih saya buka).  Seingat saya pada saat itu vim juga belum se-hipster sekarang dan belum banyak orang yang share konfigurasi vim mereka.

Kalau rasa sih biasa saja sih mas, justru merasa banyak terbantu karena pekerjaan lebih banyak ssh ke server UNIX dimana vim (at least vi) sudah menjadi paket bawaan. Dan memang sebelumnya saya sudah tau vim dimana h,j,k,l jadi navigasi utama.

**Belajarnya ngapain waktu itu? Ngetik-ngetik asal misalnya, atau ngetik konfigurasi dll**

Karena pada saat saya serius belajar vim pekerjaan saya adalah system administrator, jadi banyak practice  untuk meng-handle file konfigurasi dan log. Seperti konfigurasi oracle-db, dan alert-log nya oracle-db yang isinya banyak sekali baris. Dan sampai sekarang pun saya juga menggunakan vim kebanyakan untuk melakukan konfigurasi, membuat bash-shell-script dan pl/pgsql-script. Untuk mengetik normal saya sekarang hanya pakai untuk kepentingan personal. Dan dari dulu sampai sekarang pun saya tidak menggunakan vim untuk full-blown programming, karena di tmux jadi bisa split untuk mengetik bash dan split lain untuk eksekusi.

**Berarti bisa dikatakan belajar vimnya langsung dipraktikkan dikerjaan sehari-hari ya Mas**

Betul, kemudian kalau menemukan satu aktifitas yang belum tau, dicari di google kemudian di catet. Sebagai contoh, bagaimana memindahkan sebuah blok ke atas 4 baris. Setelah ketemu, catet. Begitu aja mas sederhana. Lama-lama catatannya juga jadi banyak. Hehehe

**Wah iya ya, saya malah ga pernah nyatet. Jadi kalau ada cara yang belum tahu, kemudian googling, terapkan, besoknya bisa lupa lagi kalau jarang dipakai**

**Soal pindah blok, kalau saya yang terpikiran gini mindahnya**

1. select blok pakai visual line (`shift+v`) atau pakai movement misal `6j`
2. delete
3. pindah kursor ke atas 4 baris (pakai cara apapaun)
4. paste

**Kalau Mas Agus gimana yang dilakukan?**

Kalau saya, untuk memindahkan blok:

1. `shift+v` visual line mode
2. pilih blok yang mau dipindahkan
3. ketik `:` langsung ketik `m -4` biarkan extra command nya ada. Tidak perlu dihapus

**Hahaha kool ilmu baru nih poin nomor 3**

Ini posisinya akan agak-agak gimana gitu kalau kita gak pas line nya akan nyelip  diantara line. Ya tinggal `u` aja trus ulangi `:m -x` tinggal `x` nya diatur. Hehehe

**Yup. Ngira-ngira `-x` itu yang kadang butuh feeling. Kalau pakai relative numbering mungkin bisa lebih jelas ya**

Persis, saya by default pakai relative number

**Berbicara soal istilah devops nih, sebenarnya apa ya devops itu? Istilah devops ini akhir2 ini gencar terdengar, bayangan saya sih devops itu tim infrastruktur yang ngurusin selain hal kodingan, berarti ya infra itu sendiri termasuk di dalamnya arsitektur server, yang mainannya kalau jaman sekarang mungkin bangsa Ansible, Docker dan kawan-kawan**

 Devops itu sebenarnya (menurut saya) adalah sebuah filosofi. Filosofi dimana:
1. Developer tidak perlu takut merusak sistem, bisa mendeploy kapan saja tanpa harus khawatir sistem rusak atau layanan menjadi tidak berfungsi
2. Developer tidak perlu repot memikirkan bagaimana sistem seharusnya bekerja, apa yang mungkin akan jadi broken, dll. Karena semua sudah diberi prosedur dan tools yang jelas.
3. Semua orang sebisa mungkin tidak melakukan pekerjaan berulang. Setelah satu pekerjaan selesai, seharusnya kalau membutuhkan outcome yang sama, bisa diotomasi.

Mengenai Ansible, Docker, dll itu adalah tools yang mungkin dibutuhkan untuk melakukan devops di sebuah perusahaan atau mungkin tidak dibutuhkan. Di kantor saya sendiri saat ini memakai Ansible tapi tidak memakai Docker. Kami pakai LXC yang berjalan di atas ZFS. Untuk saat ini kami rasa ini yang paling cocok. Mungkin akan berubah suatu saat nanti. Tapi prioritas kami saat ini ke hal yang lain daripada memikirkan bagaimana dan mengapa berpindah ke Docker

**Saya pernah datang di meetup devops Jakarta, speakernya bilang devops itu budaya, mirip-mirip yang disampaikan Mas Agus. Kalau begitu pada praktiknya berarti devops ini jelas bisa beda antar perusahaan ya, karena masing-masing memiliki detailnya sendiri-sendiri dengan garis besarnya ke 3 poin di atas tadi. Salah satu contohnya soal Docker itu tadi, di tempat Mas Agus ga pakai Docker, di tempat lain pakai.**

3 point di atas adalah interpretasi bebas saya dan yang kami terapkan di kantor. Untuk yang lebih umum sebenarnya adalah "hilangnya batas antara development dan operation".

Di perusahaan-perusahaan (enterprise pada umumnya), development dan operation ini terpisah. Yang terjadi adalah setelah project (development) selesai, kemudian di serah terimakan ke tim operation yang harus maintain. Yang mana operation tidak terlibat dalam development sehingga akhirnya mereka juga kurang baik dalam me-maintain aplikasi.

Selain itu, development dan operation memiliki sudut pandang yang berbeda. Development pada umumnya menginginkan bahwa fitur baru bisa segera launch, sementara operation menginginkan uptime atau disruption se minimal mungkin. Ini yang membuat organisasi jadi tidak _agile_  dan lambat dalam berkembang.

Sehingga devops adalah filosofi yang merombak itu dimana development dan operation menyatu, tidak ada lagi "serah terima". Perubahan dan fitur baru akan terus bertambah dengan tetap meminimalkan disruption. Kurang lebih begitu mas.

**Tadi sempat nyinggung tmux untuk remote pairing. Bisa dijelaskan remote pairing pakai tmux itu gimana?**

remote-pairing = seperti pair-programming tapi dalam hal ini yang dikerjakan oleh kami bukan programming, dan tentunya... remote.

Jadi kami di tim ops kan berdua. Terkadang kami harus melakukan sesuatu bersamaan karena harus dua orang melihat langsung apa yang terjadi di sistem dan saling diskusi.

Yang kami lakukan adalah kami ssh ke sebuah server, dimana kemudian kami membuka tmux di situ dengan sesi yang sudah disiapkan dalam sebuah bash-script. Setelah kedua orang membuka sesi yang sama, maka apa yang diketik oleh seseorang akan terlihat oleh orang yang lain dan sebaliknya. Seperti teamviewer tetapi untuk terminal begitu.

Di sini kami sering melakukan konfigurasi dan menyesuaikan  shell script secara bersama-sama. Ini yang kami sebut remote-pairing.

**Ooh I see. Konsepnya mirip ini ya berarti [https://codeshare.io/](https://codeshare.io/) cuma ini di web sedangkan tmux, ya di server kita sendiri lewat ssh**

**Btw pakai plugin apa saja untuk vimnya Mas? Sama share confignya dong 😆**

Saya pakai paket janus-vim: [https://github.com/carlhuda/janus](https://github.com/carlhuda/janus)

Config saya :

```
:set cursorline
:set wrap
:set rnu

nnoremap <F2> :set number!
nnoremap <F3> :set rnu!
nnoremap <F6> :GitGutterToggle
```

Kecewa karena terlalu sedikit? hahahaha

**Hahahaha lumayan kecewa, apalagi ternyata pakai distribusi Janus. Saya tidak menentang tapi agak gimana gitu pakai paketan karena vim itu kan memberikan kebebasan buat kita, istilahnya semau-mau gue konfignya mau gimana, mappingnya mau gimana dll. Kalau pakai paketan jadi serasa hilang nilai kebebasannya itu 😅**

**But again, pakai paketan juga termasuk bagian dari kebebasan**

Kalau pakai paket kan enak tinggal sekali run, no worries. Dan kemungkinan besar akan konsisten. Apalagi saya kan lebih sering ssh ke server mas. Pegel kalo harus config satu-per-satu, atau _bikin package sendiri_  yang kemudian bisa di deploy dengan mudah di banyak server. Ah, enggak deh.

Ya pilihan sih biasanya antara kemudahan dan kebebasan. Buat saya, yang dikasih sama janus udah cukup untuk hampir semua pekerjaan sih. Jadi, well... janus.
Hahahaha

**Haha yup, istilah kasarnya just f*cking works ya, ga perlu ngulik ke sana ke sini**

**Kalau pakai paketan gini, ada dokumentasi lengkapnya kah?, misalnya untuk ini gunakan mapping ini. Pakai paketan gini berarti kita ga tahu ya sebenarnya plugin apa aja yang dipakai?**

Tinggal dilihat aja di direktori nya, ada macem-macem kok.

**Kasih lihat tampilan vim-nya dong Mas**

![](/images/nuragus.png)

**Kalau lagi buka banyak file / buffer, Mas pakai split, tab, atau vim airline tab?**

Jarang buka banyak file dan agak menghindari .Saya cenderung: _One file at a time, one job at a time, one server at a time._

**vimscript pernah belajar Mas?**

Enggak mas. Tau sih tapi enggak ambil. Belum perlu sampai sekarang. Kalau mungkin nanti perlu ya kita liat.

**Bagi Mas Agus resouce yang paling berharga buat belajar Vim apa?**

Buku: O'Reilly Learning vim editors

Twitter: [@masteringvim](https://twitter.com/masteringvim)

Random googling, tapi biasanya kelempar ke vim.wikia.com

**Kalau soal trik vim baru-baru ini yang didapat apa Mas?**

Hmm apa ya. Oh, ini mungkin agak lumayan

 `:w !diff % -`

Buat ngeliat perbedaan buffer dan file yang ter-saved di disk. Yang lain paling standar, folding pake `zf`, `zR`

**Hhaa kool, baru tahu nih. Biasanya main diff cuma buat di git**

**Wii saya ga pernah pakai folding, tahu tapi ga pernah pakai sama kayak macro, ngerti tapi kadang malas bikinnya karena mikir dulu langkah-langkah yang mau direkam. Mas Agus sering pakai macro ga?**

Macro enggak, sama, males ngrekam-ngrekam

**Pakai vimnya yang mana Mas? vi, vim, neovim, gvim?**

Vim standar mas: `VIM - Vi IMproved 8.0 (2016 Sep 12, compiled Jan 27 2017 13:34:58)`

**Mungkin bisa kasih saran Mas ke mereka yang tertarik dengan devops atau ingin jadi orang infra, step-step belajarnya gimana dan mesti ngapaian**

Nah itu mas

Saya selalu promote bahwa kalo untuk belajar devops adalah mulai dari konsep dulu. Jadi misalnya kalau mau belajar networking, instead of belajar mikrotik (tools), sebaiknya belajar bagaimana network bekerja, misalnya buku: `Secrets of Network Cartography - A Comprehensive Guide to nmap`

Untuk belajar sistem operasi, saya menyarankan: `Solaris 10 Internal`, meskipun solaris tetapi cukup applicable untuk sistem operasi unix yang lain seperti Linux.

Untuk database, kalau postgresql udah sangat detail dokumentasinya di https://www.postgresql.org/docs/9.6/static/index.html  lengkap banget. Tapi untuk introductory reading, saya menyarankan `Oracle Database Concepts` disini: https://docs.oracle.com/cd/E11882_01/server.112/e40540/title.htm

Alasan terkuat saya kenapa harus mempelajari konsep adalah, ops itu yang diketik di terminal yang meaningful sedikit sekali. Nggak seperti developer yang hampir semua meaningful, ops kebanyakan `cd` dan hal-hal yang non-essential. Akan tetapi, di setiap command yang essential itu, risk nya lebih besar daripada developer.

Contoh-contoh yang sering terjadi: salah hapus file, salah login, mengira database standby sebagai primary (atau sebaliknya).

Sehingga menurut saya ops harus memiliki *sense of production* di mana ketika dia menghandle sistem production, maka cara berpikir dia berbeda.

Selain itu, banyak hal dari pekerjaan ops adalah membangun desain. Bagaimana supaya sistem availability tinggi, bagaimana supaya backup mudah di restore dan dilakukan test-restore, bagaimana caranya supaya deployment tidak harus malam hari, dll

Kurang lebih begitu mas.

[![](/images/vim-banner.png)](http://agung-setiawan.com/bukuvim)

**Saran atau petunjuk bagi mereka yang baru mulai belajar vim?**

Kalau menurut saya yang bisa memotivasi untuk pakai vim:
1. Memang berat di awal tetapi nanti ketika sudah terbiasa akan enak banget dengan navigasi. Buktinya sekarang ada banyak `vim keybinding` untuk firefox, chrome, dan IDE. Memang setelah mulai terbiasa dengan vim, tangan akan terbiasa dan enak.
2. Setelah terbiasa menggunakan vim, keystroke keyboard dan perpindahan tangan dari keyboard dan mouse akan sangat berkurang.

Sebenernya tidak mengerikan. Hanya karena dia sesuatu yang berbeda aja. Ibaratnya biasa makan nasi dari padi, diganti dengan makan nasi dari jagung 😄

**Wah pakai keybinding yang mana nih Mas buat browser? Kalau saya pakai vimium**

vimium sama yang di firefox, vimFX

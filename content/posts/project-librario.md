---
title: "Project: Librario 📚📖"
date: 2020-07-14T01:57:40+07:00
cover: "img/librario-cover.jpg"
description: "Librario: Perpustakaan Kolektif dan Media Literasi --- _Design / Front End Development_"
author: Satrio
draft: false
toc: true
---

---

## TL;DR

Project overview: _Web Design -- Front End Development_

Frameworks and tools: _React JS, Bootstrap, Redux, SAAS-SCSS_

> [Live Demo](https://librario.netlify.app/)
>
> [GitHub repo](https://github.com/halosatrio/librario-client-side)

---

Saya ngobrol dengan mas Warih Aji (co-founder Librario) tentang Librario pertama kali itu sekitar bulan April tahun lalu. Saat itu saya sedang proses mau gabung dengan tim Librario di bagian design grafis. Tapi saya tidak jadi bergabung karena suatu hal. Dari awal Librario muncul saya langsung penasaran dan tertarik karena pesan yang disampaikan merupakan pesan baik, dan produk/solusi yang ditawarkan merupakan barang baru bagi saya.

Fast forward satu tahun kemudian, ditengah-tengah pandemi global, saya kepikiran untuk membuat platform web-app untuk Librario. Dipikir-pikir bisa sekalian untuk portfolio saya 😁.

## Some Background

Librario merupakan platform perpustakaan kolektif yang basisnya ada di Yogyakarta. Para anggota dapat meminjam buku yang ada di katalog Librario. Selain itu anggota juga dapat menitipkan bukunya di katalog Librario sehingga dapat dipinjamkan ke anggota yang lain. Saat ini, platform Librario berjalan menggunakan layanan _instant messaging - Whatsapp_ sebagai perantara komunikasi admin dengan user (anggota), dan layanan _Google Spreadsheet_ sebagai arsip katalog buku.

### Challenges

- Membuat project dari nol
- One-man project
- Kurangnya informasi dari produk yang akan dibuat

### Key Goals

- Menyelesaikan tampilan web (front end)
- Responsive web interface
- Mempermudah alur penggunaan

## Development

Proses development dimulai dari nol banget. Di sisi informasi produk, saya kurang begitu paham dengan produknya sendiri baik dalam detail platform maupun rencana pengembangannya. Dari sisi ilmu, saya baru saja belajar menggunakan ReactJS. Benar-benar dari nol banget deh 😅😅

### Product Research

Riset produk saya lakukan dengan mengulik seluruh platform Librario yang ada. mulai dari akun [Instagram](https://instagram.com/librar.io/), media publikasi [Medium](https://medium.com/librario), spreadsheet katalog buku, sampai file PDF _User Guide_. Riset ini sangat penting untuk menentukan seperti apa design UI/UX dari platform yang akan dibuat. Selain itu juga untuk mengisi konten yang akan ditampilkan pada website.

### Design

Proses design bisa dibilang proses yang cukup menyita waktu bagi saya. Saya akui walaupun saya memiliki kemampuan design grafis, ternyata mendesign UI/UX yang baik dan sesuai produk itu tidak gampang. Bahkan saya harus bolak-balik mendesign ulang tampilan web yang sudah di-_coding_ setengah jadi karena ada elemen yang tidak sesuai.

{{< figure src="/img/librario-sketsa1.jpg" alt="sketsa 1" position="center" style="border-radius: 8px" caption="sketsa design UI/UX" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/librario-sketsa2.jpg" alt="sketsa 2" position="center" style="border-radius: 8px" caption="sketsa design UI/UX" captionPosition="center" captionStyle="color: crimson;" >}}

### Coding

Pada project ini saya menggunakan framework/library _ReactJS_ khususnya menggunakan _Create React App_. Tidak ada alasan khusus mengenai pemilihan framework. Saya hanya ingin mengetes kemampuan diri saya dalam membuat aplikasi menggunakan _ReactJS_. Untuk _state management_ saya menggunakan library [Redux](https://redux.js.org/). Selain itu, saya juga menggunakan _CSS framework_ [Bootstrap](https://getbootstrap.com/), dan _CSS preprocessing_ [SASS - SCSS](https://sass-lang.com/).

Perlu digarisbawahi bahwa project ini hanya mencakup Front End saja. Saya tidak sekalian membuat Back End karena memang saya belum mempunyai ilmu di bidang Back End.

_Deployment_ dilakukan menggunakan layanan [Netlify](https://netlify.com) yang diintegrasikan dengan GitHub repo.

## Result

Proses pengerjaan dari mulai sampai saya nyatakan selesai memakan waktu sekitar tiga bulan. Hasilnya dapat diakses di _Live Demo_ berikut:

> [Live Demo](https://librario.netlify.app/)
>
> [GitHub repo](https://github.com/halosatrio/librario-client-side)

Sebenarnya saya masih belum puas dengan hasilnya. Misalnya pada bagian halaman _User Guide_, konten tulisan masih sama persis dengan yang ditulis oleh pihak Librario. Isi tulisan tersebut menjadi tidak sinkron dengan fungsi dibuatnya platform web-app ini. Lalu masih terdapat beberapa fitur yang belum bisa digunakan seperti: checkout buku, login, dan register / daftar anggota baru.

### Conclusion

- Untuk membuat platform web-app seperti ini yang berfungsi dengan baik ternyata butuh tim yang berisi orang-orang dari berbagai bidang keahlian seperti: content writer, front end developer, back end developer, dan UI/UX designer. Sebenarnya bisa kalau mau disikat sendiri, tetapi butuh dedikasi dan semangat yang tinggi, serta resource tenaga dan waktu yang banyak 😫😫

- _"Done is better than perfect."_ Kalau saya masih ngotot buat sekalian bikin Back End, mungkin project ini belum selesai. Lagipula project ini masih bisa kembangkan lagi untuk kedepannya.

- Mencari _asset_ gambar cover buku yang baik dan sesuai ternyata butuh waktu yang lama. Itu sebabnya katalog buku pada aplikasi ini saya batasi cuma < 50 dari yang aslinya berjumlah 700 buku 😱😱

### Improvement

Hal-hal yang masih bisa untuk diperbaiki:

- Saya masih berencana untuk membuat _Back End services_ dan juga _API_ agar aplikasi ini bisa digunakan dengan sebagaimana mestinya. Untungnya kursus online yang saya ikuti juga membahas tentang _Back End_. Dari awal project ini memang direncanakan menggunakan _MERN stack_. ReactJS sudah, MongoDB lumayan paham, tinggal belajar ExpressJS dan NodeJS.

---

## Showcase

{{< figure src="/img/librario1.jpg" alt="librario landing" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Librario Homepage Wide" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/librario2.jpg" alt="librario landing responsive" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Librario Homepage Responsive" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/librario3.jpg" alt="librario katalog" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Librario Katalog Page" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/librario4.jpg" alt="librario details" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Librario Details Item Page" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/librario5.jpg" alt="librario checkout" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Librario Checkout Page" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/librario6.jpg" alt="librario register" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Librario Register Page" captionPosition="center" captionStyle="color: crimson;" >}}

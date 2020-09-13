---
title: "Project: Coffee Fest ☕"
date: 2020-08-12T17:03:01+07:00
cover: "img/coffee-cover.jpg"
description: "Jogja Coffee Festival: Online Marketplace for Curated Coffee --- _Design / Front End Development_"
author: Satrio
draft: false
toc: true
---

---

## TL;DR

Project overview: _Web Design -- Front End Development_

Highlighted feature: _state management_ using _React Context API_ and _Redux_

Frameworks and tools: _React JS, Bootstrap, Redux, Context API, SAAS-SCSS_

Duration: the first stage of development process tooks ~2 weeks (1-12 August)

> [Live Demo (Redux)](https://ngopidijogja.netlify.app/)
>
> [GitHub repo (Redux)](https://github.com/halosatrio/jogjacoffee/tree/redux)
>
> [GitHub repo (Context API)](https://github.com/halosatrio/jogjacoffee/tree/master)

---

## UPDATE [2020-08-28]

saya mengubah fitur _state management_ yang tadinya menggunakan _Context API_ dan browser localStorage, menjadi menggunakan library _Redux_. Dalam proses konversi saya mengamati pola penulisan code ketika menggunakan _Redux_ tidak jauh beda dengan _Context API_, hanya saja ketika menggunakan _Redux_ saya perlu mempersiapkan _boilerplate_ yang lebih kompleks. Selain itu, saya rasa _Redux_ lebih mempermudah ketika diimplementasikan ke aplikasi yang kompleks karena _Redux_ mudah untuk di tes (mempermudah debugging) dan saya sangat terbantu dengan hal itu.

## Some Background

Dalam mengerjakan project sebelumnya, saya menggunakan library _Redux_ untuk mengatasi _state management_. Bagi saya waktu itu, menggunakan _Redux_ untuk mengurusi data yang sederhana saja saya harus membuat _boilerplate_ khas _Redux_ yang bisa dibilang kompleks. Lalu setelah saya browsing di beberapa platform developer, saya menemukan istilah _React Context API_ yang dapat berfungsi sebagai pengganti _Redux_ untuk menangani _state management_. Dari situlah ide membuat project ini berasal. Saya ingin mencoba menggunakan _React Context API_ secara langsung sehingga nantinya saya bisa membandingkannya dengan _Redux_.

Pemilihan ide membuat online marketplace untuk specialty coffee di Jogja adalah karena saya pernah menjadi bagian dari komunitas penggiat kopi di Jogja. Tahun terakhir saya kuliah di Jogja saya sempat bekerja sebagai barista di kedai kopi tengah kota. Dari situ saya menjadi familiar dengan para penggiat kopi di Jogja mulai dari roastery, dan kedai kopinya.

### Challenges

- _State management_ menggunakan _React Context API_ (createContext, useContext, useReducer)

### Key Goals

- Menyelesaikan tampilan web (front end)
- Global state yang bisa diakses di seluruh komponen dan _Routes_
- Responsive web interface

## Development

Saya sudah mewanti-wanti diri saya sendiri bahwa project kali ini bukan lah project yang sangat serius, sehingga tidak perlu menanamkan fitur-fitur yang sebetulnya tidak dibutuhkan di rencana awal. Enaknya membatasi lingkup kerja seperti ini adalah saya jadi bisa mengestimasi waktu pengerjaan. Estimasi awal saya, project ini dapat selesai dalam waktu 10 hari. Tapi ternyata mundur 2 hari karena saya sakit di hari ke-sepuluh 🤒😷. Dengan membatasi lingkup kerja saya jadi lebih strategis dalam mengerjakan project ini. Apa yang harus dibuat terlebih dahulu, apa tahapan selanjutnya, kapan fitur ini bisa diimplementasikan, dan hal-hal lain yang membuat pengerjaan lebih efektif. Selain itu, pembatasan lingkup kerja ini mengingatkan saya untuk menyelesaikan rencana awal dulu, baru setelah itu saya boleh menambahkan fitur-fitur lainnya.

### Research

Proses riset dilakukan mulai dari memilih beberapa roastery di Jogja yang akan saya cantumkan. Saya tidak mengalami banyak kesulitan karena bisa dibilang saya dulu juga termasuk dalam komunitas kopi di Jogja sehingga nama-nama tersebut sudah familiar bagi saya. Setelah itu dilakukan proses mencari assets gambar dan informasi produk kopi yang akan ditampilkan. Saya ambil seluruh assets dari Instagram dan Tokopedia masing-masing roastery.

### Design

Proses design project kali ini tidak butuh waktu yang lama. Saya mengambil beberapa bagian/komponen dari sumber lain yang langsung saya implementasikan dengan sedikit modifikasi. Salah satu faktor yang mempercepat proses design adalah pengalaman saya dalam membuat project sebelumnya. Dari project sebelumnya saya paham komponen apa yang harus dibuat terlebih dahulu, bagaimana _interface_ yang bagus, bagaimana _behavior_ responsive yang diinginkan dan lain sebagainya. Satu hal yang mengambil waktu paling lama adalah penentuan _color palette_. Pemberian warna pada project ini masuk pada bagian terakhir dalam proses development. Saya baru bisa menentukan warna yang cocok untuk project ini setelah memakan waktu hampir seharian penuh. hehe 😆😅

### Coding

Pada project ini saya menggunakan framework/library _ReactJS_ khususnya menggunakan _Create React App_. Untuk _state management_ saya menggunakan Context API yang memang sudah ada di dalam ReactJS. Dalam penggunaan Context API ini, saya juga menggunakan bantuan localStorage untuk menyimpan data/state di browser sehingga dapat diakses oleh semua _Routes_ yang ada di dalam web. Selain itu, saya juga menggunakan _CSS framework_ [Bootstrap](https://getbootstrap.com/), dan _CSS preprocessing_ [SASS - SCSS](https://sass-lang.com/).

Perlu diingat bahwa project ini hanya mencakup Front End saja.

_Deployment_ dilakukan menggunakan layanan [Netlify](https://netlify.com) yang diintegrasikan dengan GitHub repo.

## Result

Proses pengerjaan dari mulai sampai saya nyatakan selesai memakan waktu sekitar 2 minggu. Hasilnya dapat diakses di _Live Demo_ berikut:

> [Live Demo (Redux)](https://ngopidijogja.netlify.app/)
>
> [GitHub repo (Redux)](https://github.com/halosatrio/jogjacoffee/tree/redux)
>
> [GitHub repo (Context API)](https://github.com/halosatrio/jogjacoffee/tree/master)

### Conclusion

- menurut saya _React Context API_ dapat digunakan sebagai pengganti Redux untuk menangani _state management_ jika sistem/project yang dikerjakan berskala kecil dan bukan sistem yang kompleks. saya pikir _Redux_ dan library Flux lainnya masih digunakan oleh banyak pengguna karena sistemnya sudah _mature_ sehingga lebih handal digunakan pada project dengan skala besar dan memiliki sistem yang kompleks.

- penggunaan localStorage sebagai media penyimpanan _state_ menurut saya berbahaya karena dapat dengan mudah diakses dan diubah oleh user. Jika digunakan untuk menyimpan data-data penting (misal: id, username dan password) akan sangat fatal. Saya pernah menemukan web yang menggunakan localStorage sebagai media penyimpanan _state_ tetapi dilakukan enkripsi terlebih dahulu, sehingga user tidak dapat mengakses dan mengubah isi _state_.

{{< figure src="/img/coffee-storage.jpg" alt="librario landing" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="penggunaan localStorage" captionPosition="center" captionStyle="color: DarkGoldenRod;" >}}

### Improvement

- Saya berencana untuk mengganti _Context API_ dengan _React-Redux_ untuk menangani _state management_. Sengaja ingin saya lakukan agar saya bisa merasakan dengan jelas perbedaan menggunakan keduanya. _Hands on experience_ seperti ini buat saya merupakan hal yang penting, karena dapat mengasah kemampuan pengambilan keputusan untuk project-project selanjutnya.

---

## Showcase

{{< figure src="/img/coffee1.jpg" alt="librario landing" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Librario Homepage Wide" captionPosition="center" captionStyle="color: DarkGoldenRod;" >}}
{{< figure src="/img/coffee2.jpg" alt="librario landing responsive" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Jogja Coffee Festival Homepage Responsive" captionPosition="center" captionStyle="color: DarkGoldenRod;" >}}
{{< figure src="/img/coffee3.jpg" alt="librario katalog" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Jogja Coffee Fest Katalog Page" captionPosition="center" captionStyle="color: DarkGoldenRod;" >}}
{{< figure src="/img/coffee4.jpg" alt="librario details" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Jogja Coffee Fest Details Item Page" captionPosition="center" captionStyle="color: DarkGoldenRod;" >}}
{{< figure src="/img/coffee5.jpg" alt="librario checkout" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Jogja Coffee Fest Cart Page" captionPosition="center" captionStyle="color: DarkGoldenRod;" >}}

---
title: "Tailwind CSS is Great but It Feels Weird 😐😬"
date: 2021-02-04T10:52:36+07:00
cover: "img/tailwind-cover.jpg"
description: "Yes Tailwind CSS is a great tool, and maybe it's just me, but it feels weird to not write dedicated css files with css syntax for specific components/pages that I built 😐😬"
author: Satrio
draft: false
---

## TL;DR

It's a great tool, but it feels weird, but it works!

---

Akhir-akhir ini saya jadi sering lihat postingan dan diskusi mengenai **[Tailwind CSS](tailwindcss.com/)** di timeline Twitter saya. Saya sebagai pengguna framework **[Bootstrap](getbootstrap.com/)** yang cukup rajin jadi penasaran ingin menjajal _CSS-Framework_ yang satu ini. Setelah kurang lebih satu minggu mencoba menggunakan **[Tailwind CSS](tailwindcss.com/)**, ada beberapa yang hal yang saya suka dan ada beberapa hal juga yang saya rasa aneh.

## The Goods 👍

### ~ hampir menyakup semua property di css ✨

Dibandingkan dengan framework sebelah: **[Bootstrap](getbootstrap.com/)**, Tailwind terasa lebih kaya karena hampir semua _style-property_ css ada di sini lengkap dengan berbagai variasi ukuran dan palete warna. Dari yang biasa seperti: _margin, padding, text, color, position_, sampai property _css grid_ dan _flexbox_ juga tersedia. _Pseudo-class_ seperti `hover:` pun ada di **Tailwind**.

### ~ bukan framework component/ui based 🎨

Hal yang saya suka dari Tailwind adalah karena Tailwind bukan component/ui based framework. Berbeda dengan Bootstrap, Tailwind tidak mempunyai _class-components_. User bisa membuat component sesuai dengan style yang dikehendaki. Jika di Bootstrap, component _button_ mempunyai beberapa pilihan style, seperti misalnya `btn-primary` akan menampilkan button dengan warna biru. Pada Tailwind tidak ada component class, sehingga user dapat menentukan sendiri style pada component yang hendak dibuat.

```html
// Bootstrap
<button class="btn btn-primary btn-sm">Click Me</button>

// Tailwind
<button
  class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded"
>
  Click Me
</button>
```

## The Weirds 😐

### ~ it feels weird to not writing your own css file

Poin ini mungkin hanya dirasakan oleh saya saja. Tapi beneran deh saya ngerasa aneh banget karena tidak menuliskan css syntax pada file css khusus untuk styling component yang saya buat. Ini memang preferensi berdasarkan dari workflow saya pribadi. Workflow saya dalam membuat project ReactJS, saya selalu menggunakan css-preprocessor: SASS, dan membuat file `sass` untuk styling tiap react component yang dibuat.

Saat saya menggunakan framework Bootstrap, saya masih menuliskan styling component pada file css/sass terpisah untuk tiap-tiap component. Saat menggunakan Tailwind, saya tidak membuat file css/sass terpisah untuk styling tiap-tiap component. Semuanya ditulis langsung di functional component pada file JSX. Kalau perlu menuliskan styling custom yang tidak ada di Tailwind, saya menuliskannya pada file `tailwind.css` yang menyakup seluruh styling pada project tersebut.

Sampai saat ini saya masih belum menemukan titik tengah agar bisa kembali ke workflow saya yang dahulu.

### ~ it gets messy pretty quickly

Jika hanya menuliskan tiga sampai lima _utility-class_, code yang ditulis masih bisa terlihat rapi. Beda cerita kalau sudah menuliskan sampai sepuluh _utility-classs_. Belum lagi kalau ditambah dengan _style-property_ untuk keperluan responsive design. Code HTML bisa jadi sangat _berisik_ dan terasa berantakan. Code menjadi berantakan benar-benar saya rasakan ketika membuat _React Component_ yang ditulis menggunaan syntax JSX. _Logic Function_ dan HTML class menjadi padat dan memenuhi _Function Component_.

Pada code snippet di bawah, contoh component Navbar yang lebih banyak `className` daripada inti dari component Navbarnya.

{{< figure src="/img/tailwind1.jpg" alt="tailwind css" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="code menjadi sangat 'berisik'" captionPosition="center" captionStyle="color: crimson;" >}}

> bisa diakali dengan cara extract component menggunakan `@apply` pada file `tailwind.css`

Berikut ini code snippet component box yang styling-nya saya extract ke file `tailwind.css` agar lebih mudah dibaca.

{{< figure src="/img/tailwind2.jpg" alt="tailwind css" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="membuat classname khusus untuk komponen" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/tailwind3.jpg" alt="tailwind css" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="menggunakan @apply untuk agar code JSX tidak 'berisik'" captionPosition="center" captionStyle="color: crimson;" >}}

### ~ specific size

Tailwind mempunyai rentang ukuran yang bisa dibilang banyak. Tetapi di beberapa kasus saya menemui saya tidak menemukan ukuran yang saya inginkan. Misalnya mau styling `margin-top: 30px` karena tidak ada ukuran untuk `30px == 1.875rem` saya ambil nilai yang mendekati yaitu `mt-7` atau `mt-8`. Contoh lain adalah ketika saya ingin styling `height: 200px` atau `height: 250px`. Karena tidak ada ukuran yang spesifik di angka tersebut, saya terpaksa untuk menuliskannya secara manual di file cssnya.

Memang tidak mungkin untuk menyediakan semua ukuran ke framework, maka dari itu disediakan opsi _customzation_. Tapi saya jarang banget custom ukuran. Lebih seringnya custom warna yang emang lebih sering dipakai. Kalau butuh custom size, saya lebih memilih untuk nulis ukuran sendiri di file `tailwind.css`. Tetapi proses ini saya rasa menghilangkan esensi menggunakan framework.

## It's a great tool, but it feels weird, but it works! 🤙🤙

Jujur, pengalaman menggunakan Tailwind rasanya sangat menyenangkan. Penamaan `class`, dan lengkapnya `utility` yang disediakan membuat proses pengerjaan styling jadi intuitif dan cepat. Karena bukan component/ui based framework, proses styling menjadi lebih leluasa dan mudah menyesuaikan selera. Tapi dari pengalaman tersebut, saya masih mengalami hal-hal yang saya rasa aneh seperti yang saya sudah jelaskan di poin-poin di atas.

Saya rasa saya kurang jam terbang saja menggunakan Tailwind 💻✈️.

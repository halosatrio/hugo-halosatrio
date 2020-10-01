---
title: "Typescript on React: My first experience 🤯🤯"
date: 2020-09-30T10:12:21+07:00
cover: "img/ts-react.png"
description: "My first experience learning Typescript on React project was super chaotic. I often found myself spending hours just to fix a type error 😫"
author: Satrio
draft: false
---

## TL;DR

My first experience learning Typescript on React project was super chaotic. There are a lot of additional types for React. I often use `type: any` to save myself from error I don't know how to fix. The linter error contains confusing message/solution and it overwhelmed me. By the end of the day, I don't see myself using Typescript for my React project in the near future.

---

### Coba-coba berhadiah skill baru ✨

Setelah berkutat dengan React selama 9 bulan, saya mulai tertarik untuk explore teknologi dan tools lain yang berkaitan dengan React yang sering muncul di linimasa. Beberapa nama yang sering muncul yaitu **GraphQL** dan **Typescript**. Salah satu teman saya menyarankan agar saya belajar Typescript. _"Biar lebih gampang ketika proses development dan debugging"_ katanya. Saya benar-benar mulai tertarik dengan Typescript ketika salah satu Youtuber penggiat webdev favorit saya **([Ben Awad](https://twitter.com/benawad))** sering membahas tentang Typescript di beberapa videonya. Sebenarnya sih saya masih ragu apakah perlu saya belajar Typescript (pada React), tetapi tidak ada salahnya juga untuk belajar hal baru. Jika saya berhasil mempelajarinya saya akan mendapatkan skill baru, kalaupun saya gagal dalam prosesnya saya mempelajari sesuatu.

Metode Belajar saya kali ini langsung praktik membuat sebuah project _React with Typescript_. Saya akan merekonstruksi ulang project React yang saya buat untuk keperluan tes lamaran pekerjaan beberapa waktu lalu. Selama proses pengerjaan saya pikir hanya akan _copy-paste_ dan deklarasi types saja, ternyata saya menemui banyak kejutan😳.

### Additional type annotation (A LOT OF THEM)

Dari yang saya baca basic types di TS (sejauh yang saya tahu) antara lain: _string, number, boolean, array, any, void, object, null, undefined_. Saya pikir ketika implement TS di React project, saya hanya akan menggunakan basic types itu saja. Surprise surprise, saya salah besar! 🤦‍♂️ Ternyata ada types tambahan lain seperti: `React.FC`, `React.ReactNode`, `React.ReactChildren` dan masih banyak lagi. Belum lagi untuk props khusus ketika menggunakan package pihak ketiga, misal package `react-router-dom` saya harus memasukkan `RouteComponentProps` untuk menggunakan props Location. Hal ini berlaku juga untuk package-package lainnya.

{{< figure src="/img/ts-react1.png" alt="librario details" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Type khusus untuk Route Props" captionPosition="center" captionStyle="color: royalBlue;" >}}
{{< figure src="/img/ts-react4.png" alt="librario details" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Type khusus untuk anchor tag Props" captionPosition="center" captionStyle="color: royalBlue;" >}}

### _"type: any"_ (hampir selalu) bisa menyelamatkanmu 

Pada proses pengerjaan saya mengalami banyak masalah mengenai types annotation. Seperti tidak bisa mengakses props Location pada package `react-router-dom`, padahal sudah saya tambahkan `RouteComponentProps` pada component yang saya gunakan. Ketika saya tambahkan `RouteComponentProps`, error di component Navbar hilang, tetapi muncul error di parent component, mengatakan kalau props _Location, Match and History is missing_. Saya sudah muter-muter cari solusinya masih aja belum bisa benerin error ini.

> solusi saya?
>
> _`props: any`_ 😅

{{< figure src="/img/ts-react2.png" alt="librario details" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Error pada parent component yang menunjukkan kesalahan pada component Navbar" captionPosition="center" captionStyle="color: royalBlue;" >}}
{{< figure src="/img/ts-react3.png" alt="librario details" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Solusi? _props: any_" captionPosition="center" captionStyle="color: royalBlue;" >}}

Solusi tadi membuat error messages di parent component hilang, begitu juga error di component Navbar. Terlebih lagi saya tidak perlu import `RouteComponentProps`. Saya tahu kalau _assign_ type menjadi `any` ke object yang memiliki type spesifik adalah sebuah praktik yang buruk, tetapi saya tidak tahan dengan pesan error yang selalu muncul dan tidak bisa saya perbaiki.

### Linter error messages yang seringnya membuat tambah bingung.

Error messages yang muncul di text editor ketika proses coding memang membantu saya menemukan di mana sisi yang error. Tetapi ketika saya menambahkan _interface props_ yang tidak sesuai dan kemudian muncul puluhan baris merah pada text editor, rasanya serem juga. Tidak masalah kalau ternyata error messagesnya cuman salah assign type pada variable karena mudah untuk diperbaiki. Seringnya, saya menemukan error messages yang walau sudah saya ikuti perintahnya masih saja muncul error. Bahkan di beberapa percobaan muncul error baru yang saya tidak tahu gimana cara memperbaikinya dengan benar. hhhhh!! 💢💢

{{< figure src="/img/ts-react5.png" alt="librario details" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="pesan error yang walau sudah saya ikuti solusinya malah muncul error baru" captionPosition="center" captionStyle="color: royalBlue;" >}}

> solusi saya untuk masalah di atas?
>
> hapus custom anchor component yang saya buat, lalu _hardcode_ anchor tag dan Link react-router langsung pada bagian yang dibutuhkan.

## Kesimpulannya?

Saya merasa percobaan pertama saya menggunakan TS ini merupakan pengalaman yang buruk. Saya beberapa kali harus menghabisakan waktu berjam-jam hanya untuk _googling_ cara memperbaiki type error yang kadang berhasil dan kadang juga tidak. Masih banyak hal yang harus saya pelajari tentang implementasi TS dengan React.

Sepertinya saya belum akan menggunakan Typescript 🤷‍♂️.

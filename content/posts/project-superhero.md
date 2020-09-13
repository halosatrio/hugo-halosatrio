---
title: "Project: Superhero 🦸‍♂️"
date: 2020-09-13T14:53:05+07:00
cover: "img/superhero-cover.jpg"
description: "Superhero Tanding: Fun app powered by Superhero-API --- _Web App/React js_"
author: Satrio
draft: false
toc: true
---

---

## TL;DR

Project overview: Web App -- Front End Development

Highlighted feature: Fetch data from Superhero-API

Frameworks and tools: **React js, Bootstrap, Axios, Sass**

Duration: ~1 week

> **[Live Demo](https://superhero-tanding.netlify.app/)**
>
> **[GitHub repo](https://github.com/halosatrio/tanding-hero)**

---

## Some Background

Project ini sebenernya hasil iseng saya untuk tetap produktif dalam masa-masa karantina selama pandemi. Setelah 5+ bulan pandemi tidak banyak hal menyenangkan yang dapat dilakukan selama _stay at home_. Suatu hari saya iseng mencari _public API_ yang cocok untuk _weekend project_. Ketemulah [Superhero-API](https://superheroapi.com/) ini. Pemilihan ide membuat applikasi ini terjadi begitu saja. Ketika saya lihat data hasil request dari API, saya lihat ada data `powerstats`. Dari data itulah saya kepikiran buat applikasi membandingkan kekuatan karakter-karakter superhero ini.

### Challenges

- Fetch data from the API
- Building the app logic

### Key Goals

- Berhasil fetch data dari Superhero-API
- Menyelesaikan tampilan web app
- Responsive web interface
- Rematch feature

## Development

Proses development bisa dibilang cepat karena tidak banyak yang harus dibuat selain _basic-logic_ dari applikasinya dan sedikit styling.

### Research

Proses riset dilakukan mulai dari request data API menggunakan aplikasi **POSTMAN**. Proses ini dilakukan untuk melihat _raw data_ yang diambil dari API. Setelah paham seperti apa data yang didapatkan, proses _development_ menjadi lebih mudah. Saya menjadi tahu keputusan apa yang akan saya ambil selanjutnya, misal: data penting apa saja yang akan digunakan dalam applikasi, apakah perlu dilakukan modifikasi atau tidak, dan disimpan di mana data tersebut nantinya.

### Design

Proses design juga tidak terlalu lama. Tidak ada styling yang spesial pada project kali ini. Styling yang diberikan sekadar positioning, layouting dan warna. Styling pada project kali juga menggunakan **[Bootstrap](https://getbootstrap.com/)** dan **[Sass](https://sass-lang.com/)** 😆😅.

### Coding

Pada project ini saya menggunakan **ReactJS** (Create React App). Untuk _request_ data dari API saya menggunakan Library **Axios** yang memang sudah banyak digunakan oleh developer React. Dalam urusan data management, saya tidak menggunakan library _state management_ seperti _Redux_ maupun Context API. Saya hanya menggunakan _state_ pada _class component_ saja pada _parent component_, yang kemudian diteruskan ke _component_ lain sebagai _props_.

Dalam proses coding, saya mengalami beberapa kesulitan yaitu _request_ data ke API yang selalu gagal pada awal-awal proses development. Padahal ketika saya _request_ ke API menggunakan aplikasi POSTMAN aman-aman saja. Ternyata gagalnya _request_ data ke API karena terdapat error fetch _CORS policy_. Saya mengakalinya dengan menggunakan tools **[cors-anywhere](https://github.com/Rob--W/cors-anywhere)**.

_Deployment_ dilakukan menggunakan layanan [Netlify](https://netlify.com) yang diintegrasikan dengan GitHub repo.

## Result

Proses pengerjaan dari awal sampai deployment memakan waktu sekitar satu minggu. Hasilnya dapat diakses di _Live Demo_ berikut:

> **[Live Demo](https://superhero-tanding.netlify.app/)**
>
> **[GitHub repo](https://github.com/halosatrio/tanding-hero)**

### Conclusion

- Well, bikin _weekend project_ kecil-kecilan kaya gini ternyata seru juga buat ngisi waktu selama _stay at home_ 🏠. Banyak public API yang seru-seru buat diulik dan dibikin sesuatu yang menarik. Gak bermanfaat buat orang lain juga gakpapa, asal bikin diri sendiri seneng saya rasa udah cukup. Apalagi di masa-masa seperti sekarang yang situasi dunia luar masih _chaos_.

- **Stay safe and healthy guys! 💖**

---

## Showcase

{{< figure src="/img/superhero-1.jpg" alt="superhero match" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Select User Character" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/superhero-2.jpg" alt="superhero match" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="User character vs Opponent Character" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/superhero-3.jpg" alt="librario katalog" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="Characters' stats" captionPosition="center" captionStyle="color: crimson;" >}}
{{< figure src="/img/superhero-4.jpg" alt="librario details" position="center" style="border-radius: 8px; border: 1px solid rgba(0,0,0,0.3)" caption="About Page" captionPosition="center" captionStyle="color: crimson;" >}}

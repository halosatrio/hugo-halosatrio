---
title: "Tutorial: Working on Collaborative Project for Beginner 👨‍💻👩‍💻"
date: 2020-11-22T00:56:44+07:00
cover: "img/collaborative.jpg"
description: "You may feel overwhelmed by your first collaborative project, but don't stop. Please just keep going, you may find great valuable lessons there. Fighting!! 💪💪"
author: Satrio
draft: false
toc: false
---

> _Photo by [Annie Spratt](https://unsplash.com/@anniespratt?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText) on [Unsplash](https://unsplash.com/?utm_source=unsplash&amp;utm_medium=referral&amp;utm_content=creditCopyText)_

---

Sudah hampir setahun saya menekuni web development, tetapi saya belum pernah mengerjakan proyek yang dikerjakan barengan orang banyak. Proyek-proyek yang pernah saya kerjakan adalah hasil kerjaan saya sendiri tanpa adanya kontributor lain. Saya pertama kali berkolaborasi pada sebuah proyek ketika saya bekerja. Sudah sekitar ±3 bulan ini saya mengerjakan sebuah proyek yang dikerjakan oleh tim kecil (±10 orang). Saya yang sebelumnya tidak pernah jadi kontributor di codebase orang lain merasa sangat tidak siap. Pikiran-pikiran impostor syndrome saya berisik di kepala seperti "gimana kalau nanti saya malah merusak codebase yang sudah jadi".

Jika ada di antara kalian yang juga merasa cemas mengerjakan _collaborative project_ pertama kalian, saya akan share pengalaman saya (yang sebenarnya biasa-biasa saja). Di sini saya akan share pengalaman dari kacamata seorang junior ke junior lain yang sedang mengalami hal yang sama. Bayangin aja lagi ngobrol santai di kedai kopi langganan, biar kesannya sepantaran dan gak menggurui gitu hehehe 😁😁

## Team Workflow
Pada project ini saya merupakan anggota tim tambahan. Artinya project sudah berjalan beberapa waktu sebelum saya bergabung. Workflow tiap tim untuk perusahaan/project yang berbeda tentu saja akan berbeda. Kali ini saya akan sedikit menjelaskan team workflow dari project yang saya kerjakan kali ini. Mungkin bisa jadi gambaran.

### - daily stand-up meeting
_Daily stand-up_ adalah istilah untuk meeting singkat sekitar 15 menit setiap pagi. _Daily stand-up_ berisi laporan dari masing-masing anggota tim yang isinya: kemarin selesai ngerjain apa, hari ini bakal ngerjain apa, dan apakah ada _blocker_ atau tidak. Bagi saya _stand-up_ meeting ini penting karena saya jadi tahu hari ini saya harus ngerjain apa. Saya sebagai junior dan juga anggota tim baru seringnya menunggu product manager memberikan task untuk saya kerjakan di hari itu.

### - task/assignment
Adalah seorang product manager yang bertugas mengatur pembagian _task_ (tugas) dalam project ini. _Task_ biasanya diberikan langsung ke anggota tim saat _daily stand-up_. Selain diberikan ketika _stand-up_ meeting _task_ juga sering diberikan saat ditengah-tengah hari. Misalnya: ketika ada _open feedback_ dari **QA Engineer** biasanya berupa _issue bug_, product manager sering melemparkan feedback QA tersebut ke anggota tim (bisa ke front-end atau back-end tergantung issuenya) untuk dikerjakan langsung.

### - communication
Komunikasi tim sangatlah penting dalam mengerjakan collaborative project. Dalam lingkup pekerjaan, setiap project akan memiliki _group chat_ sendiri. Media komunikasinya bisa bermacam-macam. Ada yang menggunakan _Telegram, WhatsApp, Slack_ dan beberapa aplikasi messenger lain. Pada project kali ini, tim menggunakan Slack yang memiliki chanel masing-masing seperti: chanel `dev-discussion`, `daily-discussion`, `fe-discussion`, dll. Selain _group chat_ sering juga berkomunikasi langsung ke anggota tim lain untuk `tek-tokan` terlebih saat proses _bugfix_. Misal langsung chat tim back-end untuk tanya __API__ yang akan digunakan untuk `fitur A` itu pakai yang mana, dan lain sebagainya.

## Git Workflow
Bagi saya, git workflow ini adalah momok terbesar. Sebelum saya bergabung collaborative project ini saya menggunakan git hanya seputar `git clone`, `git add`, `git commit`, `git push`. Saya lebih takut salah `push` ketimbang gak bisa ngerjain projectnya. Kalau salah `commit` dan `push` yang kena bisa production server, kalau masalah gak bisa ngerjain projectnya saya sih masih percaya diri bisa ngerjain dengan baik. hehehe 😅😅

### - belajar git command _(merge, checkout branch)_
Hal pertama yang saya lakukan beberapa hari sebelum _on boarding_ tim, saya belajar git untuk collaborative work. Mulai dari belajar _command_ seperti: `merge`, `rebase`, `fetch`, `pull` dll, sampai belajar best practice git workflow. Materi belajar saya dari [postingan ini](https://dev.to/lydiahallie/cs-visualized-useful-git-commands-37p1), dan [ini](https://dev.to/milu_franz/git-explained-proper-team-etiquette-1od).

### - follow the rule
Setiap perusahaan/tim/project punya peraturannya masing-masing terkait git workflow. Saran saya: ikuti dengan baik, kalau bingung tanya langsung ke _team lead_. Git workflow tidak jauh-jauh dengan _branch naming_ dan _push and merge request_. Di project saya kali ini, anggota tim _develop_ di branch tertentu (_bugfix atau feature_). Hanya _team lead_ yang bisa develop di branch `dev`. Lalu setelah selesai `push` dan `merge request` (kalau di GitHub `pull request`) laporan ke _team lead_ biar dicek terlebih dahulu. Kalau sudah ok bakal langsung `merge`.

#### Personal note
Install extension `gitlens` dan `git graph` di VSCode. Saya orangnya visual banget, jadi harus tahu grafik alur git. Setelah intall `git graph` saya jadi lebih nyaman kerjanya. Lalu untuk `gitlens` ini mempermudah saya dengan beberapa fitur yang ada, misalnya: `git blame` biar tahu siapa yang nulis `code`, dan `file history` untuk tahu perubahan apa saja yang terjadi pada file.

## When in doubt, ask someone!
Beneran deh! kalau bingung terkait sesuatu lebih baik tanya. Bisa tanya ke sesama anggota tim, bisa tanya ke _team lead_, bisa juga tanya ke manager. Saya inget dulu dua minggu pertama sering tanya ke _team lead_. Mungkin bagi beliau pertanyaan saya ini remeh banget, tapi ya namanya juga saya masih junior kalau gak tanya malah _kopong_. Ada beberapa pertanyaan yang sebenernya saya sendiri malu banget tapi yaaaa mau gimana lagi, saya gak tahu dan kalau mau asal sok tahu takutnya malah ngerusak production server dan ngerepotin satu tim. Untungnya _team lead_ saya baik dan mau menjelaskan dengan sabar. Thank you, Mas! 😘🥰

## Epilogue
akhirul kata, kerjakan dengan enjoy dan jangan kebanyakan takut. kalau udah dikerjain ntar juga bakal dapet feelnya. yang penting yakin aja, kalau gak yakin bisa tanya ke team lead atau ke anggota tim lain. jangan lupa have fun! hehehe 😁😁

> Even the greatest was once a beginner. Don't be afraid to take that first step.
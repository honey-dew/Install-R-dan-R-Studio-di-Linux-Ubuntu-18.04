---
title: "Install R dan R Studio di Linux ubuntu 18.04"
output: github_document
---

Untuk dapat menggunakan bahasa pemrograman R, maka terlebih dahulu harus menginstall [Program R](https://cran.r-project.org/) pada komputer. Dan Untuk mempermudah dalam menggunakan bahasa pemrograman R disarankan untuk menginstall IDE (Integrated Development Environment). Salah satu IDE untuk bahasa pemrograman R yang sudah sangat populer adalah [R Studio](https://www.rstudio.com/). Di bawah ini adalah langkah-langkah untuk menginstall Program R dan R Studio:

## Prerequisite

Sebelum Menginstall Program R dan R Studio pastikan hal-hal berikut ini:

- Ubuntu 18.04 LTS sudah terinstal
- Komputer dapat terkoneksi dengan internet, dan
- Bisa menggunakan perintah-perintah dasar pada terminal linux seperti cara untuk berpindah directory dan sebagainya.

## Install Program R

- Buka Terminal Linux dengan menekan Ctrl+Alt+T secara bersamaan.
- Edit file source.list dengan mengetikan perintah **sudo nano /etc/apt/source.list**.
- Ketikan repository berikut ini __deb https://cloud.r-project.org/bin/linux/ubuntu bionic-cran35/__ pada file source.list tersebut di bagian paling bawah.
- Tekan Ctrl+X kemudian Y untuk menyimpan hasil editan pada file source.list tersebut.
- Ketikan perintah **gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys E298A3A825C0D65DFD57CBB651716619E084DAB9**.
- Setelah itu ketik **gpg -a --export E298A3A825C0D65DFD57CBB651716619E084DAB9 | sudo apt-key add -**.
- Kemudian ketikan **sudo apt-get update** dan tunggu sampai selesai.
- Sampai pada tahapan ini, Program R siap untuk diinstall.
- Ketikan perintah **sudo apt-get install r-base** dan tunggu sampai selesai.
- Untuk bisa menjalankan Program R ketikan saja pada terminal perintah **R**, apabila berhasil maka akan terlihat tulisan seperti berikut ini.

*R version 3.5.3 (2019-03-11) -- "Great Truth"
Copyright (C) 2019 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)*

*R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details*.

  *Natural language support but running in an English locale*

*R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications*.

*Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R*.

- Ketikan perintah **q()** kemudian tekan **n** untuk keluar dari Program R dan tutup terminal linux dengan mengetikan perintah **exit**.

## Install R Studio

- Download R studio desktop di https://www.rstudio.com/.
- Masuk ke menu Products dan pilih RStudio.
- Pilih **DOWNLOAD RSTUDIO DESKTOP**.
- Kemudian pilih rstudio versi ubuntu terbaru.
- Setelah terdownload, masuk kembali ke terminal dan masuk ke directory atau tempat penyimpanan hasil download yang berada pada directory Downloads, dan ketikan perintah **cd Downloads**.
- Sebelum menginstal R Studio terlebih dahulu install dependencies dengan mengetikan perintah **sudo apt-get install libjpeg62**.
- Setelah menginstall dependencies, ketikan perintah **sudo dpkg -i *nama file hasil download***.
- Terakhir ketik perintah **sudo apt-get install -f**.
- Selesai dan R Studio sudah dapat digunakan.
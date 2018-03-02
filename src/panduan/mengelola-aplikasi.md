---
title: Mengelola Aplikasi Terinstall
type: panduan
order: 109
---

## Menginstall Software


### Menginstall aplikasi dengan menggunakan internet

Pastikan komputer anda terkoneksi dengan jaringan komputer karena penginstalan akan langsung mengunduh paket aplikasi yang ingin di install dari repository ubuntu. Cara paling mudah adalah melalui Software Center.

Atau lewat terminal, Buka terminal dan
Ketikan perintah: 

    sudo apt-get install nama_paket 

Masukkan password komputer anda.
Ketika ada dialog `“Do you want to continue? (Y/n)”` ketik `“y”`
Tunggu hingga proses pengunduhan dan pemasangan selesai.
Jalankan aplikasi dengan memanggil nama_paket di terminal atau anda dapat mencarinya di menu.

### Menginstall aplikasi tanpa internet
Jika anda memiliki aplikasi dengan ekstensi .tar.gz, .deb ataupun .tea anda dapat menginstalnya tanpa koneksi internet.

-    Menginstall aplikasi .tar.gz
    Buka terminal anda lalu ketikkan perintah 
    
        tar xzvf nama_file.tar.gz
    
    (perintah untuk mengekstrak file)
    Masuk ke folder yang telah di ekstrak 
    
        cd nama_file 
    
        ./configure 
    
        make 
    
        sudo su 
    
        #make install
    
    Pada umumnya penginstalan file tar.gz menggunakan perintah diatas namun jika aplikasi tidak terinstall atau terjadi error, sebaiknya anda membaca file README atau INSTALL yang biasanya disertakan dalam file aplikasi tersebut untuk panduan penginstalan.

-    Menginstall aplikasi .deb
    Jika anda ingin menginstall aplikasi berekstensi .deb yang merupakan debian paket ada dua langkah.
     -  Menggunakan Package Installer
        kliknya dua kali pada file .deb
        klik tombol Install Package
        Masukkan password anda
        Tunggu hingga muncul pesan Installation finished.

     -  Menggunakan Terminal
        Buka teminal ketikkan perintah 
        
            sudo dpkg -i nama_file.deb
            
## Uninstall Software

 Untuk menguinstall software tertentu anda dapat melakukannya dengan cara berikut:
Buka terminal dan pastikan terlebih dahulu nama paket yang ingin anda uninstall denganmenggunakan perintah: 

    dpkg –list

Setelah mamastikan paket yang ingin ada uninstall ketikkan perintah 

    sudo apt-get remove nama_paket 

Masukan password
Tunggu hingga proses uninstall selesai.

## Menambah Repository
Repository merupakan sekumpulan paket-paket aplikasi atau program untuk sebuah sistem operasi (Linux) yang digunakan untuk menunjang kinerja dari sebuah aplikasi, program dan sebagainya yang didapatkan dari server mirror website paket-paket tersebut. Ada dua cara untuk menambahkan repository ke sistem.

  -  Melalui Terminal
    Buka terminal, lalu ketikkan perintah: 
    
        sudo add-apt-repository ppa:nama_pembuat/nama_paket 
    
        sudo apt-get update 
    
        sudo apt-get install nama_paket

## Mengupdate software

 `→ Settings → Software Updater`
Mengupdate software dapat dilakukan melalui layanan Software Updater, sistem akan mengecek update software lalu akan mengunduh dari internet dan memasang update-update untuk software. 

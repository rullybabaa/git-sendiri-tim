<h1>Dasar Git</h2>
<p>Jadi, sebenarnya apa yang dimaksud dengan Git? Ini adalah bagian penting untuk dipahami, karena 
jika anda memahami apa itu Git dan cara kerjanya, maka dapat dipastikan anda dapat menggunakan Git 
secara efektif dengan mudah. Selama mempelajari Git, cobalah untuk melupakan VCS lain yang mungkin 
telah anda kenal sebelumnya, misalnya Subversion dan Perforce. Git sangat berbeda dengan sistem-sistem 
tersebut dalam hal menyimpan dan memperlakukan informasi yang digunakan, walaupun antar-muka penggunanya
 hampir mirip. Dengan memahami perbedaan tersebut diharapkan dapat membantu anda menghindari kebingungan
 saat menggunakan Git.</p>
 
 <h1>Cara Kerja Git</h2>
 <p>Git memperlakukan datanya sebagai sebuah kumpulan snapshot dari sebuah miniatur sistem berkas. 
 Setiap kali anda melakukan commit, atau melakukan perubahan pada proyek Git anda, pada dasarnya Git
 merekam gambaran keadaan berkas-berkas anda pada saat itu dan menyimpan referensi untuk gambaran 
 tersebut. Agar efisien, jika berkas tidak mengalami perubahan, Git tidak akan menyimpan berkas
 tersebut melainkan hanya pada file yang sama yang sebelumnya telah disimpan<P>
 
 <h1>Git untuk sendiri</h2>
 <p>Dalam menggunakan Version controll, anda akan selalu melakukan Commit pada Git, tempat tersebut
 dinamakan sebuah repository (a.k.a. “repo”). Dan untuk menyimpan project yang anda buat pada GitHub,
 anda perlu memiliki GitHub Repository. Berikut ini adalah cara untuk membuat repository pada GitHub.</p>

 <p>Selanjutnya masukkan informasi tentang anda. jika sudah di isi, selanjutnya click 
 “Create Repository.”</p>
 
 <p>Selanjutnya membuat file README. File  README bukanlah bagian yang diperlukan dari
 repo GitHub, tapi kita akan membuat file tersebut untuk uji coba apakah repo dapat digunakan. 
 File README adalah catatan yang bagus untuk menggambarkan proyek Anda atau menambahkan 
 beberapa dokumentasi seperti cara menginstal atau menggunakan proyek Anda. Anda mungkin 
 ingin menyertakan informasi kontak person – jika proyek Anda menjadi orang yang populer 
 akan ingin membantu Anda suatu saat.</p>
 
 <p>sekarang masuklah ke command prompt, lalu masukkan perintah seperti di bawah ini:</p>
 <body>mkdir ~/Hello-World  #Membuat direktori "Hello-World"<br>
cd ~/Hello-World #Masuk ke folder yang anda buat<br>
git init    #Sets up the necessary Git files<br>
touch README# Creates a file called "README" in your Hello-World directory<br>

<p>Sekarang file README sudah siap untuk di commit. Untuk meng -commit 
dibutuhkan snapshot dari semua file di project anda pada waktu yang sama.
 pada command prompt, ketikan perintah:</p>
 
git add README #untuk menambahkan file README<br>
git commit -m 'first commit' #Commit file anda, dengan menambahkan pesan "first commit"<br>

<p>Sampai pada step ini, anda telah melakukan commit pada lokal repository anda, tapi masih belum melakukan apapun pada repo GitHub.</p>
<p>Untuk menghubungkan lokal koneksi anda ke GitHub, anda perlu me remote repo dan melakukan push pada commit  anda.</p>
<p>Masukkan perintah ini untuk melakukannya :</p>
<br>git remote add origin https://github.com/namauser/Hello-World.git # membuat remote dengan nama "origin" pointing pada GitHub repo
<br>git push origin master# Mengirimkan perintah commit sebagai "master" branch pada GitHub

<p>Congratulations! anda sudah membuat sebuah repository di GitHub, membuat README, meng commit nya , dan push di GitHub.</p>
 
 <h1>Git untuk tim</h2>
 <p>GitHub memiliki apa yang disebut Organizations. Seperti akun pribadi, akun Organizations memiliki 
 namespace dimana semua proyek mereka ada, namun banyak hal lainnya yang berbeda. Akun ini mewakili 
 sekelompok orang dengan kepemilikan bersama atas proyek, dan ada banyak alat untuk mengelola subkelompok
 orang-orang tersebut. Biasanya akun ini digunakan untuk grup Open Source (seperti “perl” atau “rails”)
 atau perusahaan (seperti “google” atau “twitter”). </p>
 
 <p>Sebuah organization cukup mudah untuk dibuat; cukup klik pada ikon “+” di kanan atas halaman GitHub 
 manapun, dan pilih “New organization” dari menu.</p>
 
 <p>Pertama, Anda harus memberi nama Tim Anda dan memberikan alamat surel untuk kontak utama
 grup tersebut. Kemudian Anda dapat mengundang pengguna lain untuk menjadi pemilik akun bersama 
 jika Anda ingin.</p>
 
 <p>Sebagai pemilik Tim, ketika Anda mem-fork sebuah repositori, Anda akan memiliki 
 pilihan untuk mem-fork ke namespace Tim Anda. Ketika Anda membuat repositori baru,
 Anda dapat membuatnya di akun pribadi Anda atau di bawah Tim yang Anda miliki.
 Anda juga secara otomatis “watch” setiap repositori baru yang dibuat Tim ini.</p>
 
 <p>Organizations berhubungan dengan perorangan melalui tim, yang hanya merupakan 
 pengelompokan akun pengguna perorangan dan repositori di dalam organization dan 
 jenis akses apa yang dimiliki orang-orang di repositori tersebut.</p>
 
 <p>Contoh, katakanlah perusahaan Anda memiliki tiga repositori: frontend,backend,
 dan deployscripts. Anda ingin pengembang HTML/CSS/Javascript Anda memiliki akses
 ke frontend dan mungkin backend, dan orang operasi Anda memiliki akses ke backend 
 dan` deployscripts`. Tim membuat ini mudah, tanpa harus mengelola kolaborator
 untuk setiap repositori perorangan.</p>
 
 <p>Laman organization menunjukkan dasbor sederhana untuk semua repositori, pengguna,
 dan tim yang berada di bawah organization ini.</p>
 
 <p>Untuk mengelola Tim Anda, Anda dapat mengklik pada sidebar Tim di sisi kanan laman 
 di The Organization page.. Ini akan membawa Anda ke halaman yang dapat Anda gunakan
 untuk menambahkan anggota ke tim Anda, menambahkan repositori ke tim atau mengelola
 pengaturan dan mengakses tingkat kontrol untuk tim. Setiap tim hanya dapat membaca,
 membaca/menulis atau akses administratif ke repositori. Anda dapat mengubah tingkat
 itu dengan mengklik tombol “Settings” di The Team page..</p>
 
 <p>Ketika Anda mengundang seseorang ke tim, mereka akan mendapatkan surel yang
 memberitahukannya bahwa mereka telah diundang.</p>
 
 <p>Selain itu, tim @mentions (seperti @acmecorp/frontend) bekerja sama seperti yang 
 mereka lakukan dengan pengguna perorangan, kecuali semua anggota tim itu kemudian 
 berlangganan thread. Ini berguna jika Anda menginginkan perhatian dari seseorang 
 dalam tim, tapi Anda tidak tahu pasti dengan siapa yang harus ditanyakan.</p>
 
 <p>Seorang pengguna dapat masuk dalam jumlah tim, jadi jangan membatasi diri hanya
 dengan tim kontrol-akses. Tim minat khusus seperti ux, css, atau refactoring berguna
 untuk beberapa jenis pertanyaan, dan lainnya seperti legal dan colorblind untuk jenis
 yang sama sekali berbeda.</p>

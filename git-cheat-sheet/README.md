# Git

## Konfigurasi Pertama Git

Setelah menginstall git, kita harus mengatur email dan password sebagai identitas kita. Gunakan perintah di bawah.

Jangan lupa sesuaikan email & nama kamu, direkomendasikan menggunakan nama & email yang sama dengan yang digunakan di Github.com

```
git config --global user.name "Nama Saya"
git config --global user.email "emailsaya@email.com"
```

## Mengunggah project ke Github.com

### Jika belum ada Repository di Github, ikuti langkah-langkah ini

1. Masuk ke github.com. Pastikan kamu sudah terdaftar ya.

2. Pilih tanda `+` di pojok kanan atas, pilih `Create new repository`.

3. Berikan nama repository yang unik, tidak boleh sama dengan repository kamu yang lain. Tidak boleh menggunakan spasi, ganti spasi dengan tanda `-`.

4. Buat repository.

### Jika sudah ada Repository di Github, ikuti langkah langkah ini

1. Buat directory project di laptop kamu (jika belum ada).

2. Buka terminal.

3. `cd` ke directory project.

4. Jalankan perintah init

```
git init
```

5. Tambahkan alamat remote dengan perintah berikut. Sesuaikan `nama-user` dan `nama-repository` ya.

```
git remote add origin https://github.com/nama-user/nama-repository.git
```

6. Untuk mengunggah ke _Remote Repository_ jalankan perintah berikut.
   Perintah ini akan mengunggah ke _Remote Repository_ **origin** dengan nama branch **master**

Secara _default_, jika kita baru membuat repository, nama branch kita adalah **master**.

```
git add .
git commit -m "tulis pesanmu disini"
git push -u origin master
```

7. Ulangi step ke-6 ini setiap ada perubahan yang ingin kamu unggah ke _Remote Repository_.

Selamat belajar! :D

## Ilustrasi Alur kerja dengan Git

![Git Diagram](https://support.nesi.org.nz/hc/article_attachments/360004194235/Git_Diagram.svg)

Sumber: https://support.nesi.org.nz/hc/en-gb/articles/360001508515-Git-Reference-Sheet

## Perintah dalam Git

| Perintah                                       | Penjelasan                                                                                                                                           | Contoh                                                                                                                                                          |
| ---------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| git init                                       | Mengimplementasikan git pada _Work Directory_. Hanya perlu dilakukan 1x pada sebuah work directory.                                                  | `git init`                                                                                                                                                      |
| git add $path                                  | Menambahkan file tertentu dari _Work Directory_ ke _Staging Area_.                                                                                   | `git add .` untuk menambahkan semua file yang ada dalam _Work Directory_ ke _Staging Area_                                                                      |
| git commit -m "$pesan"                         | Memindahkan file yang berada di _Staging Area_ ke _Local Repository_ & memberikan pesan sebagai informasi commit.                                    | `git commit -m "memperbaiki masalah pada halaman home"` untuk memindahkan semua file yang ada dalam _Staging Area_ ke _Local Repository_                        |
| git push -u $nama_remote $nama_branch          | Mengunggah file yang berada di _Local Repository_ ke _Remote Repository_.                                                                            | `git push -u origin master` untuk mengunggah file yang berada di _Local Repository_ ke _Remote Repository_ bernama **origin** dengan nama branch **master**     |
| git status                                     | Menampilkan file-file yang mengalami perubahan di _Work Directory_ dan _Staging Area_                                                                | `git status`                                                                                                                                                    |
| git diff                                       | Menampilkan perubahan dari file-file yang mengalami perubahan di _Work Directory_                                                                    | `git diff`                                                                                                                                                      |
| git fetch --all                                | Melakukan cek adanya perubahan di _Remote Repository_, biasanya dilakukan sebelum perintah `pull`                                                    | `git fetch --all`                                                                                                                                               |
| git pull $nama_remote $nama_branch             | Jika file yang berada di _Remote Repository_ lebih baru dibanding file yang berada di _Local Repository_, unggah file tersebut ke _Local Repository_ | `git pull origin master` untuk mengunduh file terbaru yang berada di _Remove Repository_ bernama **origin** dengan nama branch **master** ke _Local Repository_ |
| git reset HEAD -- $path                        | Mengembalikan file tertentu dari _Staging Area_ ke _Work Directory_.                                                                                 | `git reset HEAD -- .` untuk mengembalikan semua file yang ada dalam _Staging Area_ ke _Work Directory_                                                          |
| git reset HEAD@{1}                             | Mengembalikan file tertentu dari _Local Repository_ yang di-commit terakhir ke _Work Directory_.                                                     | `git reset HEAD@{1}` untuk mengembalikan semua file yang ada dalam _Local Repository_ yang di-commit terakhir ke _Work Directory_                               |
| git remote -v                                  | Menampilkan nama dan alamat _Remote Repository_                                                                                                      | `git remote -v`                                                                                                                                                 |
| git remote add $nama_remote $alamat_remote     | Menambahkan nama & alamat _Remote Repository_, hanya bisa dilakukan jika namanya belum ada                                                           | `git remote add origin https://github.com/namasaya/repositorysaya.git` menambahkan alamat _Remote Repository_ dengan nama origin                                |
| git remote set-url $nama_remote $alamat_remote | Mengubah alamat _Remote Repository_, hanya bisa dilakukan jika namanya sudah ada                                                                     | `git remote set-url origin https://github.com/namasaya/repositorybaru.git` mengubah alamat _Remote Repository_ yang bernama origin                              |
| git remote remove $nama_remote                 | Menghapus _Remote Repository_ tertentu                                                                                                               | `git remote remove origin` menghapus alamat _Remote Repository_ yang bernama origin                                                                             |
| git remote show $nama_remote                   | Menampilkan alamat _Remote Repository_ tertentu                                                                                                      | `git remote show origin` menampilkan alamat _Remote Repository_ yang bernama origin                                                                             |
| git checkout -b $nama_branch                   | Membuat branch baru di _Local Repository_ dengan nama tertentu                                                                                       | `git checkout -b develop` membuat branch baru dengan nama develop                                                                                               |
| git checkout $nama_branch                      | Berpindah branch ke branch dengan nama tertentu, hanya bisa dilakukan jika branch sudah ada                                                          | `git checkout develop` berpindah ke branch develop                                                                                                              |
| git clone $alamat_remote                       | Mengunduh repository ke perangkat                                                                                                                    | `https://github.com/madeindra/belajar-git` akan mengunduh repository belajar- git ke perangkatmu                                                                |

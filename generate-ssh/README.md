# SSH

Kunci SSH dibutuhkan untuk mengupload/mendownload ke/dari Github, ikuti langkah-langkah ini untuk membuat kunci SSH

## Membuat Kunci SSH

1. Buka terminal
2. Jalankan perintah ini (ganti `email@example.com` dengan emailmu)

```
ssh-keygen -t rsa -b 4096 -C "email@example.com"
```

3. Tekan enter
4. Akan muncul dialog berikut (alamat akan menyesuaikan alamat `home` masing-masing)

```
Enter a file in which to save the key (/alamat/nama_user/.ssh/id_rsa):
```

5. Tekan enter untuk mengkonfirmasi pembuatan kunci SSH

Setelah langkah tersebut, kamu bisa menemukan kunci publik ssh mu di lokasi ini (`nama_user` akan menyesuaikan nama user di devicemu)

```
C:/Users/nugie/.ssh/id_rsa.pub
```

## Menyalin Kunci SSH ke Github

1. Buka terminal
2. Jalankan perintah ini (perintah di bawah menggunakan special symbol `~` yang selalu berarti alamat `home`)

```
cat ~/.ssh/id_rsa.pub
```

Akan muncul seperti ini

```
ssh-rsa randomcharactersrandomcharactersrandomcharacters
randomcharactersrandomcharactersrandomcharacters
randomcharactersrandomcharactersrandomcharacters
nama@device
```

3. Arahkan cursor ke hasil cetakan tersebut, tandai (blok) hasil cetakan tersebut kemudian salin (copy), sekarang saatnya tempel (paste) ke Github

NB: Perintah `cat` artinya mencetak isi dari sebuah file

4. Buka [Github](github.com), login jika belum
5. Klik foto profilmu di pojok kanan, pilih `Settings`
6. Di side bar kiri (menu vertikal di sisi kiri), pilih `SSH and GPG Key`
7. Klik tombol `New SSH Key`
8. Tempel (paste) isi kunci di kolom `Key`
9. Klik `Add SSH Key`
10. Jika ada konfirmasi password, masukkan passwordmu
11. Sekarang kamu sudah bisa melakukan download dari dan upload ke Github.

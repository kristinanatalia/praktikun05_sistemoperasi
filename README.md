
# Praktikum Sistem Operasi

**Nama:** Kristina Natalia Hutauruk  
**NIM:** 09011282328120  
**Matkul:** Sistem Operasi

## 1. Lihat peralatan I/O, character device, yang ada pada sistem komputer.

**Langkah-langkah:**
Ketik perintah `ls -l /dev` untuk melihat daftar peralatan I/O dan character devices yang tersedia pada sistem Anda.

![Peralatan I/O](https://github.com/kristinanatalia/praktikun05_sistemoperasi/blob/main/T1.png)

## 2. Buatlah sub direktori januari, februari dan maret sekaligus pada direktori latihan5.

**Langkah-langkah:**
Ketik `mkdir -p latihan5/{januari,februari,maret}` untuk membuat ketiga sub direktori tersebut secara bersamaan dalam direktori latihan5.

![Membuat Sub Direktori](https://github.com/kristinanatalia/praktikun05_sistemoperasi/blob/main/t2.png)

## 3. Buatlah file dataku yang berisi nama, nim dan alamat pada sub direktori januari dan copy-kan file tersebut ke sub direktori februari dan maret.

**Langkah-langkah:**
* Ketik `nano latihan5/januari/dataku` untuk membuat dan membuka file dataku.
* Masukkan informasi nama, nim, dan alamat, kemudian simpan file tersebut (Ctrl + O, Enter, Ctrl + X).
* Copy file tersebut ke sub direktori lain:

![Membuat File Dataku](https://github.com/kristinanatalia/praktikun05_sistemoperasi/blob/main/T3.png)
![Copy File Dataku](https://github.com/kristinanatalia/praktikun05_sistemoperasi/blob/main/T4.png)

## 4. Ubahlah ijin akses file dataku pada sub direktori januari sehingga group dan others dapat melakukan write.

**Langkah-langkah:**
* Ketik `chmod 766 latihan5/januari/dataku` untuk mengubah izin sehingga pemilik dapat membaca, menulis, dan menjalankan, sedangkan grup dan lainnya dapat membaca dan menulis saja.

## 5. Ubahlah ijin akses file dataku pada sub direktori februari sehingga user dapat melakukan baik write, read maupun execute, tetapi group dan others hanya bisa read dan execute.

**Langkah-langkah:**
* Ketik `chmod 755 latihan5/februari/dataku` untuk memberi izin kepada pemilik file untuk membaca, menulis, dan menjalankan, sementara grup dan lainnya hanya dapat membaca dan menjalankan.

## 6. Ubahlah ijin akses file dataku pada sub direktori maret sehingga semua dapat melakukan write, read dan execute.

**Langkah-langkah:**
* Ketik `chmod 777 latihan5/maret/dataku` untuk memberikan semua hak (baca, tulis, eksekusi) kepada semua pengguna.

![Mengubah Ijin Akses](https://github.com/kristinanatalia/praktikun05_sistemoperasi/blob/main/T5.png)

## 7. Hapuslah direktori maret.

**Langkah-langkah:**
* Ketik `rm -r latihan5/maret` untuk menghapus direktori maret.

## 8. Ubahkan kepemilikan sub direktori februari sehingga user dan group hanya dapat melakukan read, dan coba untuk membuat direktori baru haha pada sub direktori februari.

**Langkah-langkah:**
* Ubah kepemilikan: `chmod 440 latihan5/februari`
* Coba buat direktori: `mkdir latihan5/februari/haha` (Ini akan gagal jika tidak ada hak menulis).

## 9. Modifikasi umask dari file dataku pada sub direktori januari menjadi 027 dan berapakan nilai default-nya?

**Langkah-langkah:**
* Ketik `umask 027` untuk mengatur umask baru.
* Ciptakan file baru dan periksa perizinannya dengan `ls -l`.

![Modifikasi Umask](https://github.com/kristinanatalia/praktikun05_sistemoperasi/blob/main/T6.png)

## 10. Buatlah link dari file dataku ke file dataku.ini dan file dataku.juga dengan perintah list perhatikan berapa link yang terjadi?

**Langkah-langkah:**
* Ketik `ln latihan5/januari/dataku latihan5/januari/dataku.ini`
* Ketik `ln latihan5/januari/dataku latihan5/januari/dataku.juga`
* Cek jumlah link: `ls -l latihan5/januari/dataku`

![Membuat Link 1](https://github.com/kristinanatalia/praktikun05_sistemoperasi/blob/main/t7.png)
![Membuat Link 2](https://github.com/kristinanatalia/praktikun05_sistemoperasi/blob/main/T8.png)





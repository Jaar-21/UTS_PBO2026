# ✚ Sistem Manajemen Antrian Pasien pada Klinik

## 👤 Identitas

| Keterangan | Data |
|---|---|
| Nama | Ahmad Fajar Novia |
| NIM | [2509116041] |
| Mata Kuliah | Pemrograman Berorientasi Objek |
| Bahasa Pemrograman | Java |
| IDE | NetBeans |

---

## 📌 Deskripsi Proyek

Sistem Manajemen Antrian Pasien pada Klinik merupakan program berbasis Java yang digunakan untuk mengelola data pasien secara sederhana melalui Command Line Interface (CLI).

Program ini memiliki beberapa fitur utama, yaitu menampilkan data pasien, menambahkan pasien, mengubah data pasien, menghapus pasien, dan memanggil pasien berdasarkan ID. Pasien dibedakan menjadi dua jenis, yaitu Pasien Umum dan Pasien BPJS.

Program ini dibuat sebagai penerapan konsep Pemrograman Berorientasi Objek, seperti access modifier, encapsulation, inheritance, polymorphism, validasi input, serta struktur MVC sederhana.

---

## ⚙️ Fitur Program

| No | Fitur | Keterangan |
|---|---|---|
| 1 | Tampilkan Pasien | Menampilkan data pasien berdasarkan jenis pasien |
| 2 | Tambahkan Pasien | Menambahkan data pasien baru ke dalam sistem |
| 3 | Update Pasien | Mengubah data pasien berdasarkan ID |
| 4 | Hapus Pasien | Menghapus data pasien berdasarkan ID |
| 5 | Panggil Pasien | Memanggil pasien berdasarkan ID dan mengeluarkannya dari antrian |
| 6 | Keluar | Mengakhiri program |

---

## 🔄 Alur Program

Program dijalankan melalui `Main.java` yang memulai sistem dan menjalankan `PasienController`.

Ketika program pertama kali dijalankan, sistem menyiapkan satu data dummy pasien di dalam `ArrayList`. Data tersebut digunakan agar pengguna dapat langsung melihat data pasien tanpa harus menambahkan data terlebih dahulu.

Setelah program berjalan, pengguna akan melihat menu utama. Pengguna dapat memilih fitur dengan memasukkan angka sesuai dengan pilihan yang tersedia.

Input dari pengguna akan diproses melalui `PasienController`. Controller bertugas mengatur alur program dan menghubungkan input pengguna dengan proses yang terdapat pada `PasienCRUD`.

Pada saat pengguna memasukkan data angka, program menggunakan `ValidasiInput` untuk memastikan input sesuai dengan tipe data yang dibutuhkan. Jika input tidak sesuai, sistem akan menampilkan pesan kesalahan dan meminta pengguna memasukkan data kembali.

Pada menu **Tambahkan Pasien**, pengguna memasukkan ID, nama, umur, nomor telepon, dan jenis pasien. Sistem akan mengecek ID terlebih dahulu agar tidak terjadi ID pasien yang sama.

Jika pengguna memilih **Pasien Umum**, sistem akan meminta jenis pembayaran. Jika pengguna memilih **Pasien BPJS**, sistem akan meminta nomor BPJS.

Pada menu **Update Pasien**, pengguna memasukkan ID pasien yang ingin diubah. Jika ID ditemukan, data nama, umur, dan nomor telepon dapat diperbarui.

Pada menu **Hapus Pasien**, pengguna memasukkan ID pasien yang ingin dihapus. Jika ID ditemukan, data pasien akan dihapus dari daftar.

Pada menu **Panggil Pasien**, pengguna memasukkan ID pasien yang ingin dipanggil. Sistem akan menampilkan nama pasien yang dipanggil dan menghapus pasien tersebut dari daftar antrian.

Program akan terus berjalan sampai pengguna memilih menu **6. Keluar**.

---

## ▶️ Cara Menjalankan Program

1. Buka project menggunakan **NetBeans**.
2. Pastikan seluruh source code sudah berada pada package yang sesuai.
3. Buka file `Main.java`.
4. Jalankan program menggunakan tombol **Run**.
5. Menu utama akan ditampilkan pada terminal.
6. Masukkan angka sesuai menu yang ingin digunakan.
7. Ikuti instruksi yang diberikan oleh program.
8. Pilih menu **6. Keluar** untuk mengakhiri program.

---

## 🏗️ Struktur Program

Program menggunakan struktur MVC sederhana dengan membagi program menjadi beberapa bagian berdasarkan tugasnya.

**Struktur package:**

    com.mycompany.klinik
    │
    ├── Main.java
    │
    ├── model
    │   ├── Pasien.java
    │   ├── PasienUmum.java
    │   └── PasienBPJS.java
    │
    ├── service
    │   └── PasienCRUD.java
    │
    ├── controller
    │   └── PasienController.java
    │
    └── helper
        └── ValidasiInput.java

### Penjelasan Struktur Package

**`Main.java`**

Merupakan class utama yang digunakan untuk memulai program. Class ini menjalankan sistem dengan memanggil `PasienController`.

**`model`**

Berisi class yang digunakan untuk merepresentasikan data pasien.

`Pasien.java` merupakan superclass yang menyimpan data umum pasien.

`PasienUmum.java` dan `PasienBPJS.java` merupakan subclass yang mewarisi data dan method dari `Pasien` serta memiliki informasi tambahan sesuai jenis pasien.

**`service`**

Berisi `PasienCRUD.java` yang menangani proses pengelolaan data pasien. Class ini bertanggung jawab terhadap proses seperti menambah, menampilkan, mengubah, menghapus, dan memanggil pasien.

**`controller`**

Berisi `PasienController.java` yang mengatur alur interaksi antara pengguna dengan sistem. Controller menerima pilihan pengguna dan menghubungkannya dengan proses yang ada pada service.

**`helper`**

Berisi `ValidasiInput.java` yang digunakan untuk membantu melakukan validasi input, terutama input yang membutuhkan tipe data angka.

---

## 🧩 Penerapan Konsep Pemrograman Berorientasi Objek

### 1. Access Modifier

Access modifier digunakan untuk mengatur tingkat akses terhadap atribut dan method dalam class.

Program menggunakan beberapa access modifier seperti `private`, `protected`, dan `public`. Penggunaan access modifier membantu mengatur bagian program yang dapat diakses secara langsung dan bagian yang perlu diakses melalui method tertentu.

### 2. Encapsulation

Encapsulation diterapkan dengan membatasi akses langsung terhadap data yang terdapat pada object.

Pada class `Pasien`, atribut seperti `nama`, `umur`, dan `noTelepon` dikelola melalui method getter dan setter. Dengan demikian, perubahan data dilakukan melalui method yang telah disediakan oleh class.

### 3. Inheritance

Inheritance diterapkan dengan menggunakan class `Pasien` sebagai superclass dan dua subclass, yaitu `PasienUmum` dan `PasienBPJS`.

Struktur inheritance pada program:

    Pasien
    ├── PasienUmum
    └── PasienBPJS

`PasienUmum` dan `PasienBPJS` mewarisi atribut dan method dari class `Pasien`, kemudian memiliki data tambahan sesuai dengan jenis pasien masing-masing.

### 4. Polymorphism

Polymorphism diterapkan melalui method yang memiliki nama sama pada superclass dan subclass, tetapi dapat menghasilkan tampilan yang berbeda sesuai dengan object yang digunakan.

Pasien Umum dapat menampilkan informasi tambahan berupa jenis pembayaran, sedangkan Pasien BPJS dapat menampilkan nomor BPJS.

Dengan penerapan polymorphism, object dari subclass tetap dapat diperlakukan sebagai object dari superclass `Pasien`.

### 5. Validasi Input

Validasi input diterapkan menggunakan class `ValidasiInput`.

Validasi digunakan untuk memastikan input tertentu sesuai dengan tipe data yang dibutuhkan. Contohnya, ketika program meminta input angka tetapi pengguna memasukkan huruf, sistem akan memberikan pesan kesalahan dan meminta input kembali.

Program juga melakukan validasi umur dengan rentang 1 sampai 200 tahun serta melakukan pengecekan ID agar tidak terjadi ID pasien yang sama.

### 6. ArrayList

`ArrayList` digunakan untuk menyimpan data pasien selama program berjalan.

Program menyediakan satu data dummy pada awal program agar daftar pasien tidak kosong ketika fitur tampilkan pasien pertama kali digunakan.

Data pasien akan bertambah ketika pengguna menambahkan pasien baru dan dapat berkurang ketika pasien dihapus atau dipanggil.

---

## 🖼️ Penjelasan Screenshot Output

### 1. Menu Utama

<img width="401" height="206" alt="image" src="https://github.com/user-attachments/assets/34a2ae06-dfde-4eb8-a4b0-c45e54e32a8d" />

Screenshot menunjukkan tampilan awal program setelah dijalankan. Pada bagian ini terdapat enam pilihan menu yang dapat digunakan untuk mengelola data pasien, mulai dari menampilkan data sampai keluar dari program.

### 2. Menampilkan Pasien

<img width="712" height="680" alt="Screenshot 2026-09-23 233325" src="https://github.com/user-attachments/assets/127d29f4-0802-4cfc-b115-bb0f9aac0333" />

Screenshot menunjukkan proses ketika pengguna memilih menu **Tampilkan Pasien**. Pengguna dapat memilih untuk melihat data Pasien Umum atau Pasien BPJS.

Data dummy yang sudah disediakan di dalam `ArrayList` juga dapat langsung ditampilkan pada bagian ini.

### 3. Menambahkan Pasien

<img width="750" height="495" alt="Screenshot 2026-09-23 233202" src="https://github.com/user-attachments/assets/4043acf6-8247-4912-beac-c6a118670e5e" />

Screenshot menunjukkan proses ketika pengguna memilih menu **Tambahkan Pasien**. Pengguna diminta memasukkan ID, nama, umur, nomor telepon, dan jenis pasien.

Jika memilih Pasien Umum, pengguna akan memasukkan jenis pembayaran. Jika memilih Pasien BPJS, pengguna akan memasukkan nomor BPJS.

### 4. Validasi ID Pasien

<img width="763" height="277" alt="image" src="https://github.com/user-attachments/assets/755b9cd9-891e-450d-aefb-53df5301664b" />

Screenshot menunjukkan validasi ketika pengguna memasukkan ID yang sudah digunakan. Sistem akan memberikan pesan bahwa ID pasien sudah digunakan sehingga data dengan ID yang sama tidak dapat ditambahkan.

### 5. Update Pasien

<img width="672" height="727" alt="Screenshot 2026-09-23 233422" src="https://github.com/user-attachments/assets/c65dd97f-8814-430f-a84f-8db101716d5d" />

Screenshot menunjukkan proses perubahan data pasien berdasarkan ID. Setelah ID ditemukan, pengguna dapat memasukkan nama, umur, dan nomor telepon yang baru.

### 6. Menghapus Pasien

<img width="690" height="318" alt="Screenshot 2026-09-23 233443" src="https://github.com/user-attachments/assets/5d5f8e72-9640-4e84-b6a5-ea264a719a1b" />

Screenshot menunjukkan proses penghapusan data pasien berdasarkan ID. Jika ID ditemukan, sistem akan menghapus data pasien dari daftar.

### 7. Memanggil Pasien

<img width="662" height="593" alt="Screenshot 2026-09-23 233506" src="https://github.com/user-attachments/assets/45640522-2737-43f2-9621-bdfda2734293" />


Screenshot menunjukkan proses ketika pengguna memilih menu **Panggil Pasien**. Sistem akan menampilkan nama pasien yang dipanggil dan menghapus pasien tersebut dari daftar antrian.

### 8. Validasi Input Angka

<img width="404" height="250" alt="image" src="https://github.com/user-attachments/assets/6039583d-9a64-4a54-8186-df643b649806" />

Screenshot menunjukkan validasi ketika pengguna memasukkan input yang tidak sesuai dengan tipe data yang dibutuhkan. Contohnya adalah ketika menu meminta angka tetapi pengguna memasukkan huruf.

Sistem akan menampilkan pesan **"Input harus berupa angka"** dan meminta pengguna memasukkan input kembali.

### 9. Program Selesai

<img width="398" height="215" alt="Screenshot 2026-09-23 233522" src="https://github.com/user-attachments/assets/e0bca856-361b-4406-8bad-a5b9d567cbf4" />

Screenshot menunjukkan ketika pengguna memilih menu **6. Keluar**. Sistem akan menampilkan pesan bahwa program selesai dan proses program dihentikan.

---

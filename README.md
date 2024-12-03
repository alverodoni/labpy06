# labpy06
Nama : Doni Alvero <p>
Nim : 312410663 <p>
Kelas : TI.24.A.5 <P>
Mata Kuliah : Bahasa Pemrograman <p>

## Flowchart
![foto4](https://github.com/user-attachments/assets/321d87a3-31db-4f6d-b953-864734140da3)



## Kode Program 
![foto1](https://github.com/user-attachments/assets/4e519bcd-b54c-46b3-9e71-6ba32fc7ceca)
![foto2](https://github.com/user-attachments/assets/ea4304d5-d586-4ed4-8b91-653815bf8b8a)

### Penjelasan Program
Komponen Utama Program
1. Class Student

    Deskripsi: Kelas ini digunakan untuk merepresentasikan setiap mahasiswa.
    Atribut:
        nim: Nomor Induk Mahasiswa (string).
        nama: Nama mahasiswa (string).
        tugas: Nilai tugas (integer).
        uts: Nilai UTS (integer).
        uas: Nilai UAS (integer).
        akhir: Nilai akhir yang dihitung menggunakan metode calculate_final_grade.
    Metode:
        _init_: Konstruktor untuk menginisialisasi atribut ketika objek dibuat.
        calculate_final_grade: Menghitung nilai akhir dengan rumus:
        nilai_akhir=(tugas×0.3)+(uts×0.35)+(uas×0.35)
        nilai_akhir=(tugas×0.3)+(uts×0.35)+(uas×0.35)

2. Fungsi Utility
a. display_menu

    Menampilkan pilihan menu utama kepada pengguna.

b. display_students

    Menampilkan daftar nilai mahasiswa dalam bentuk tabel.
    Jika tidak ada data, akan menampilkan pesan "TIDAK ADA DATA".

c. find_student_index

    Mencari indeks mahasiswa berdasarkan nama.
    Digunakan untuk operasi ubah dan hapus.

3. Fungsi Utama main

    Deskripsi: Fungsi utama untuk menjalankan aplikasi. Fungsi ini mengelola seluruh alur kerja program, termasuk menerima input pengguna dan menjalankan fungsi sesuai pilihan.
    Alur Kerja:
        Tambahkan Data (T):
            Memasukkan NIM, nama, nilai tugas, UTS, dan UAS.
            Nilai mahasiswa disimpan sebagai objek Student di dalam list students.
        Lihat Data (L):
            Menampilkan semua data mahasiswa dalam tabel.
        Ubah Data (U):
            Mencari mahasiswa berdasarkan nama.
            Jika ditemukan, memperbarui data mahasiswa dengan nilai baru.
        Hapus Data (H):
            Menghapus data mahasiswa berdasarkan nama.
        Keluar (K):
            Mengakhiri program.

Cara Kerja Program

    Program dimulai dengan menjalankan fungsi main.
    Menu utama ditampilkan melalui fungsi display_menu.
    Pengguna memilih opsi dengan memasukkan huruf (T, L, U, H, K):
        Tambah Data: Menambahkan mahasiswa baru.
        Lihat Data: Menampilkan tabel daftar nilai mahasiswa.
        Ubah Data: Memperbarui informasi mahasiswa.
        Hapus Data: Menghapus informasi mahasiswa dari daftar.
        Keluar: Mengakhiri program.
    Program terus berjalan hingga pengguna memilih opsi Keluar.

## Ouput Program
![foto3](https://github.com/user-attachments/assets/083fdb48-f1dc-413f-baf5-7d8daa6ab79e)



## labpy06
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
1. Header dan Kelas Student:
   
```python
       print("\nProgram Input Nilai")
       print("===================")
      
       class Student:
           def __init__(self, nim, nama, tugas, uts, uas):
               self.nim = nim
               self.nama = nama
               self.tugas = tugas
               self.uts = uts
               self.uas = uas
               self.akhir = self.calculate_final_grade()
      
           def calculate_final_grade(self):
               return round((self.tugas * 0.3) + (self.uts * 0.35) + (self.uas * 0.35), 2)
   ```
   - tujuan Kode ini mencetak judul program dan mendefinisikan kelas ```Student``` yang memiliki atribut ```nim```, ```nama```, ```tugas```, ```uts```, ```uas```, dan ```akhir```.
   - ```calculate_final_grade``` adalah metode yang menghitung nilai akhir berdasarkan bobot tugas (30%), UTS (35%), dan UAS (35%).
       
2. Fungsi Menampilkan Menu dan Daftar Mahasiswa:

```python
       def display_menu():
                     print("\n[(L)ihat, (T)ambah, (U)bah, (H)apus, (K)eluar]: ", end=' ')
              
                 def display_students(students):
                     print("\nDaftar Nilai")
                     print("=" * 84)
                     print(f"| {'NO':<3} | {'NIM':<10} | {'NAMA':<30} | {'TUGAS':<6} | {'UTS':<4} | {'UAS':<4} | {'AKHIR':<5} |")
                     print("=" * 84)
                     if not students:
                        print(f"| {'TIDAK ADA DATA':^80} |")
                     else:
                         for i, student in enumerate(students, start=1):
                             print(f"| {i:<3} | {student.nim:<10} | {student.nama:<30} | {student.tugas:<6} | {student.uts:<4} | {student.uas:<4} | {student.akhir:<5} |")
                     print("=" * 84)
  ```        
   - ```display_menu``` menampilkan menu pilihan kepada pengguna.
   - ```display_students``` menampilkan daftar nilai mahasiswa dalam format tabel. Jika tidak ada data, pesan "TIDAK ADA DATA" akan ditampilkan.

3. Fungsi Mencari Indeks Mahasiswa:

```python
          def find_student_index(students, nim):
              for index, student in enumerate(students):
                  if student.nim == nim:
                     return index
              return None
```
   - ```find_student_index``` Fungsi ini mencari indeks mahasiswa dalam daftar students berdasarkan Nama. Jika Nama ditemukan, fungsi mengembalikan indeksnya; jika tidak, fungsi mengembalikan None.


4. Fungsi Utama:

```python
       def main():
           students = []
           while True:
               display_menu()
               choice = input().lower()
               if choice == 't':
                   nim = input("\nNIM: ")
                   nama = input("Nama: ")
                   tugas = int(input("Nilai Tugas: "))
                   uts = int(input("Nilai UTS: "))
                   uas = int(input("Nilai UAS: "))
                   students.append(Student(nim, nama, tugas, uts, uas))
               elif choice == 'l':
                   display_students(students)
               elif choice == 'u':
                   display_students(students)
                   nama = input("\nMasukkan nama mahasiswa yang akan diubah: ")
                   index = find_student_index(students, nama)
                   if index is not None:
                       print("Data baru:")
                       nama = input("Nama: ")
                       tugas = int(input("Nilai Tugas: "))
                       uts = int(input("Nilai UTS: "))
                       uas = int(input("Nilai UAS: "))
                       students[index] = Student(nim, nama, tugas, uts, uas)
                   else:
                       print("Mahasiswa dengan NIM tersebut tidak ditemukan.")
               elif choice == 'h':
                   display_students(students)
                   nama = input("\nMasukkan nama mahasiswa yang akan dihapus: ")
                   index = find_student_index(students, nama)
                   if index is not None:
                       del students[index]
                       print("Data mahasiswa berhasil dihapus.")
                   else:
                       print("Mahasiswa dengan NIM tersebut tidak ditemukan.")
               elif choice == 'k':
                   break
               else:
                   print("Pilihan tidak valid!")
       
       if __name__ == "__main__":
           main()
```

   - ```Fungsi main``` Menjalankan program utama dengan menginisialisasi daftar students dan menyediakan antarmuka menu untuk pengguna. Pengguna dapat menambah, melihat, mengubah, atau menghapus data mahasiswa, serta keluar dari program.
   - Variabel ```students``` menyimpan daftar objek ```Student```.
   - Program menampilkan menu dan menangani pilihan pengguna:
     - **Tambah (```T```)**: Menambah data mahasiswa baru ke dalam daftar ```students```.
     - **Lihat (```L```)**: Menampilkan daftar mahasiswa.
     - **Ubah (```U```)**: Mengubah data mahasiswa berdasarkan Nama yang diberikan. Jika Nama ditemukan, data mahasiswa diperbarui dengan data baru.
     - **Hapus (```H```)**: Menghapus data mahasiswa berdasarkan Nama yang diberikan. Jika Nama ditemukan, data mahasiswa dihapus dari daftar students.
     - **Keluar (```K```)**: Keluar dari program.

## Ouput Program
![foto3](https://github.com/user-attachments/assets/083fdb48-f1dc-413f-baf5-7d8daa6ab79e)



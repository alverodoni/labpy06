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
1. Header dan Kelas Student
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
   
    Penjelasan:
        Kode ini dimulai dengan mencetak judul program "Program Input Nilai" dan garis pemisah.
        Kelas Student didefinisikan dengan konstruktor __init__ yang menerima parameter untuk NIM, nama, nilai tugas, UTS, dan UAS.
        Atribut akhir dihitung dengan memanggil metode calculate_final_grade, yang mengalikan nilai tugas dengan 30%, UTS dengan 35%, dan UAS dengan 35%, lalu membulatkannya menjadi dua desimal.

   2. Fungsi Menampilkan Menu dan Daftar Mahasiswa
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
    
    Penjelasan:
        Fungsi display_menu mencetak pilihan menu yang tersedia untuk pengguna.
        Fungsi display_students menampilkan daftar nilai mahasiswa dalam format tabel yang rapi. Jika daftar mahasiswa kosong, akan ditampilkan pesan "TIDAK ADA DATA". Jika ada data, setiap mahasiswa ditampilkan dengan              informasi mereka, termasuk NIM, nama, nilai tugas, UTS, UAS, dan nilai akhir.

   3. Fungsi Mencari Indeks Mahasiswa
      def find_student_index(students, nim):
    for index, student in enumerate(students):
        if student.nim == nim:
            return index
    return None
    Penjelasan:
        Fungsi find_student_index mencari indeks mahasiswa dalam daftar berdasarkan NIM yang diberikan. Jika NIM ditemukan, fungsi ini mengembalikan indeksnya; jika tidak, mengembalikan None.

      4. Fungsi Utama
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
            nim = input("\nMasukkan NIM mahasiswa yang akan diubah: ")
            index = find_student_index(students, nim)
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
            nim = input("\nMasukkan NIM mahasiswa yang akan dihapus: ")
            index = find

## Ouput Program
![foto3](https://github.com/user-attachments/assets/083fdb48-f1dc-413f-baf5-7d8daa6ab79e)



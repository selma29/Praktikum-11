## TUGAS PERTEMUAN KE 13

Nama : Selma Ohoira

NIM : 312210727

Kelas : TI.22.C9

Mata Kuliah : Bahasa Pemograman

# PRAKTIKUM 11

## Program Data Mahasiswa dengan Except
Membuat program sederhana untuk membuat data mahasiswa menggunakan except, class, fungsi dan Dictionary dengan python

1. Langkah pertama, membuat sebuah dictionary kosong yang nantinya akan diinputkan data ketika program dijalankan.
Masukan syntax berikut:

    x = {}

2. Selanjutnya membuat class, gunakan syntax berikut:

    class data():

3. Membuat fungsi menu, dengan syntax berikut:

        def __init__(self,nama,nim,uts,uas,tugas,akhir):
                print("Program Input Nilai")
                print("="*19)
                while True:
                    c = input("\n(T)ambah, tampi(L)kan, (U)bah, (H)apus, (K)eluar: ")
                    if c.lower() == 't':
                        self.tambah()
                    elif c.lower() == 'l':
                        self.tampilkan()
                    elif c.lower() == 'u':
                        self.ubah()
                    elif c.lower() == 'h':
                        self.hapus()
                    elif c. lower() == 'k':
                        break
                    else:
                        print("Pilih menu yang tersedia")

4. Membuat fungsi "Tambah" untuk menambahkan data dan menambahkan exception
Gunakan syntax berikut:

    def tambah(self):
            try:
                print("\nTambah data")
                self.nama = input("Nama           : ")
                self.nim = int(input("NIM            : "))
                self.uts = int(input("Nilai UTS      : "))
                self.uas = int(input("Nilai UAS      : "))
                self.tugas = int(input("Nilai Tugas    : "))
                self.akhir = self.tugas*30/100 + self.uts*35/100 + self.uas*35/100
                x[self.nama] = self.nim, self.tugas, self.uts, self.uas, self.akhir
            except ValueError:
                print("Mohon hanya masukan angka untuk NIM dan Nilai")

Apabila kita input data yang tidak sesuai, maka akan memanggil except ValueError,
Contoh kita input nilai NIM dengan string maka except VelueError akan terpanggil.

5. Lalu membuat class mahasiswa dengan nilai class data.
Gunakan syntax berikut :

        class mahasiswa(data):

6. Membuat fungsi "Ubah" untuk mengubah data dan menambahkan exceptions
Gunakan syntax berikut:

        def ubah(self):
                print("\nUbah Data")
                self.nama = input("Nama           : ")
                if self.nama in x.keys():
                    del x[self.nama]
                    self.nama = input("Nama           : ")
                    self.nim = int(input("NIM            : "))
                    self.uts = int(input("Nilai UTS      : "))
                    self.uas = int(input("Nilai UAS      : "))
                    self.tugas = int(input("Nilai Tugas    : "))
                    self.akhir = self.tugas*30/100 + self.uts*35/100 + self.uas*35/100
                    x[self.nama] = self.nim, self.tugas, self.uts, self.uas, self.akhir
                    print()
                    print("|====================================|")
                    print("|        BERHASIL MENGUBAH DATA      |")
                    print("|====================================|")
                else:
                    print("Nama {0} tidak ditemukan".format(self.nama))

Apabila kita input data yang tidak sesuai, maka akan memanggil except ValueError,
Contoh kita input nilai NIM dengan string maka except VelueError akan terpanggil.

7. Membuat fungsi "Hapus" untuk menghapus data.
Gunakan syntax berikut:

        def hapus(self):
                print("\nHapus Data")
                self.nama = input("Masukan Nama    : ")
                if self.nama in x.keys():
                    del x[self.nama]
                    print()
                    print("|====================================|")
                    print("|       BERHASIL MENGHAPUS DATA      |")
                    print("|====================================|")
                else:
                    print("NIM {0} Tidak Ditemukan".format(self.nama))

8. Membuat fungsi "tampilkan" untuk menampilkan data (L)
Gunakan syntax berikut:

        def tampilkan(self):
                if x.items():
                    print("\nDaftar Nilai")
                    print("="*78)
                    print("|No. |      NAMA       |       NIM       |  TUGAS  |  UTS  |  UAS  |  AKHIR  |")
                    print("="*78)
                    i = 0
                    for z in x.items():
                        i += 1
                        print("| {no:2d} | {0:15s}| {1:15d}  | {2:5d}   | {3:5d} |{4:6d} | {5:7.2f} |"
                            .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
                        print("=" * 78)
                else:
                    print("\nDaftar Nilai")
                    print("="*78)
                    print("|No. |      NAMA       |       NIM       |  TUGAS  |  UTS  |  UAS  |  AKHIR  |")
                    print("="*78)
                    print("|                                TIDAK ADA DATA                              |")
                    print("="*78)

9. Terakhir, membuat syntax untuk menjalankan class mahasiswa dengan nilai "nama", "nim", "uts", "uas", "tugas", "akhir"
dan menambahkan exceptions. Gunakan syntax berikut:

        try:
            run = mahasiswa("nama", "nim", "uts", "uas", "tugas", "akhir")
        except KeyboardInterrupt:
            print("\n|====================================|")
            print("|             TERIMAKASIH            |")
            print("|====================================|")

Apabila terdapat KeyboardInterrupt maka akan memanggil except, contoh saat menekan CTRL + C maka akan terjadi
KeyboardInterrupt yang akan memanggil except.

## Hasil akhir Praktikum 6

    x = {}

    class data():
        def __init__(self,nama,nim,uts,uas,tugas,akhir):
            print("Program Input Nilai")
            print("="*19)
            while True:
                c = input("\n(T)ambah, tampi(L)kan, (U)bah, (H)apus, (K)eluar: ")
                if c.lower() == 't':
                    self.tambah()
                elif c.lower() == 'l':
                    self.tampilkan()
                elif c.lower() == 'u':
                    self.ubah()
                elif c.lower() == 'h':
                    self.hapus()
                elif c. lower() == 'k':
                    break
                else:
                    print("Pilih menu yang tersedia")

        
        def tambah(self):
            try:
                print("\nTambah data")
                self.nama = input("Nama           : ")
                self.nim = int(input("NIM            : "))
                self.uts = int(input("Nilai UTS      : "))
                self.uas = int(input("Nilai UAS      : "))
                self.tugas = int(input("Nilai Tugas    : "))
                self.akhir = self.tugas*30/100 + self.uts*35/100 + self.uas*35/100
                x[self.nama] = self.nim, self.tugas, self.uts, self.uas, self.akhir
            except ValueError:
                print("Mohon hanya masukan angka untuk NIM dan Nilai")


    class mahasiswa(data):
        def tampilkan(self):
            if x.items():
                print("\nDaftar Nilai")
                print("="*78)
                print("|No. |      NAMA       |       NIM       |  TUGAS  |  UTS  |  UAS  |  AKHIR  |")
                print("="*78)
                i = 0
                for z in x.items():
                    i += 1
                    print("| {no:2d} | {0:15s}| {1:15d}  | {2:5d}   | {3:5d} |{4:6d} | {5:7.2f} |"
                        .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
                    print("=" * 78)
            else:
                print("\nDaftar Nilai")
                print("="*78)
                print("|No. |      NAMA       |       NIM       |  TUGAS  |  UTS  |  UAS  |  AKHIR  |")
                print("="*78)
                print("|                                TIDAK ADA DATA                              |")
                print("="*78)
        
        def hapus(self):
            print("\nHapus Data")
            self.nama = input("Masukan Nama    : ")
            if self.nama in x.keys():
                del x[self.nama]
                print()
                print("|====================================|")
                print("|       BERHASIL MENGHAPUS DATA      |")
                print("|====================================|")
            else:
                print("NIM {0} Tidak Ditemukan".format(self.nama))

        def ubah(self):
            print("\nUbah Data")
            self.nama = input("Nama           : ")
            if self.nama in x.keys():
                try:
                    del x[self.nama]
                    self.nama = input("Nama           : ")
                    self.nim = int(input("NIM            : "))
                    self.uts = int(input("Nilai UTS      : "))
                    self.uas = int(input("Nilai UAS      : "))
                    self.tugas = int(input("Nilai Tugas    : "))
                    self.akhir = self.tugas*30/100 + self.uts*35/100 + self.uas*35/100
                    x[self.nama] = self.nim, self.tugas, self.uts, self.uas, self.akhir
                    print()
                    print("|====================================|")
                    print("|        BERHASIL MENGUBAH DATA      |")
                    print("|====================================|")
                except ValueError:
                    print("Mohon hanya masukan angka untuk NIM dan Nilai")
            else:
                print("Nama {0} tidak ditemukan".format(self.nama))
    try:
        run = mahasiswa("nama", "nim", "uts", "uas", "tugas", "akhir")
    except KeyboardInterrupt:
        print("\n|====================================|")
        print("|             TERIMAKASIH            |")
        print("|====================================|")

![Gambar](gambar/1.png)

SELESAI !!!
# Iman Setiawan

**Tugas Praktikum - Pertemuan 9**\
**Materi List, Tuple, dan Dictionary**

Berikut soal tugas dari modul.\
![screenshot output](screenshot/soal.png)

Ini adalah flowchart dari program yang akan saya buat.\
![screenshot output](screenshot/flowchart.jpg)

Dibawah ini adalah code saya\
Saya menggunakan ekstension PrettyTable pada code saya, yang membuatnya lebih mudah.
~~~

x = {}
selected_menu = ()

while True:
    print()
    print("Program Input Data Nilai Mahasiswa")
    print()
    print("Ketik (L) untuk Menampilkan Data")
    print("Ketik (T) untuk Menambahkan Data")
    print("Ketik (U) untuk Mengubah Data")
    print("Ketik (H) untuk Menghapus Data")
    print("Ketik (C) untuk Mencari Data")
    
    print("Ketik (K) untuk Keluar")
    
    print("--------------------------------")
    selected_menu = input("Pilih menu> ")

    if selected_menu == "L":
        if x.items():
            print("="*74)
            print("|                            Daftar Mahasiswa                            |")
            print("="*74)
            print("| No |     Nama        |     NIM     |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*74)
            i = 0
            for z in x.items():
                i += 1
                print("| {no:^2} | {0:15} | {1:^11d} | {2:^5d} | {3:^5d} | {4:^7d} | {5:^7.2f} |"
                      .format(z[0][:13], z[1][0], z[1][1], z[1][2], z[1][3], z[1][4], no=i))
            print("=" *74)
        else:
            print("="*73)
            print("|                             Daftar Mahasiswa                          |")
            print("="*73)
            print("|         Nama         |    NIM    |  UTS  |  UAS  |  Tugas  |   Akhir  |")
            print("="*73)
            print("|                             TIDAK ADA DATA                            |")
            print("="*73)
        print()
        input("Tekan Enter untuk ke Menu Utama. . .")

    if selected_menu == "T":
        print("Menambahkan Tambah Data Mahasiswa")
        nama = input("Nama\t\t: ")
        nim = int(input("NIM\t\t: "))
        uts = int(input("Nilai UTS\t: "))
        uas = int(input("Nilai UAS\t: "))
        tugas = int(input("Nilai Tugas\t: "))
        akhir = tugas*30/100 + uts*35/100 + uas*35/100
        x[nama] = nim, uts, uas, tugas, akhir
        print("Data telah di Input !")
        input("Tekan Enter untuk ke Menu Utama. . .")

    if selected_menu == "C":
        print("Mencari Data Mahasiswa")
        nama = input("Masukkan Nama : ")
        if nama in x.keys() :
            print("="*71)
            print("|                             Daftar Mahasiswa                        |")
            print("="*71)
            print("|         Nama        |    NIM    |  UTS  |  UAS  |  Tugas  |  Akhir  |")
            print("="*71)
            print("| {0:19} | {1:^9} | {2:^5} | {3:^5} | {4:^7} | {5:^7} |".format(nama, nim, uts, uas, tugas, akhir))
            print("="*71)
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
        input("Tekan Enter untuk ke Menu Utama. . .")

    if selected_menu == "U":
        print("Ubah Data Mahasiswa")
        nama = input("Masukkan Nama   : ")
        if nama in x.keys():
            nim = int(input("NIM\t\t: "))
            uts = int(input("Nilai UTS\t: "))
            uas = int(input("Nilai UAS\t: "))
            tugas = int(input("Nilai Tugas\t: "))
            akhir = tugas*30/100 + uts*35/100 + uas*35/100
            x[nama] = nim, uts, uas, tugas, akhir
            print("Data Telah di Ubah !")
        else:
            print("Nama {0} tidak ditemukan".format(nama))
        input("Tekan Enter untuk ke Menu Utama. . .")

    if selected_menu == "H":
        print("Hapus Data Mahasiswa")
        nama = input("Masukkan Nama  : ")
        if nama in x.keys():
            del x[nama]
            print("Data telah di hapus !")
        else:
            print("Nama {0} Tidak Ditemukan".format(nama))
        input("Tekan Enter untuk ke Menu Utama. . .")

    if selected_menu == "K":
        keluar = input("Yakin ingin keluar (Y/T) ? : ")
        if keluar == "Y":
            exit()
        else:
            input("Tekan Enter untuk ke Menu Utama. . .")
            
~~~

Contoh menambahkan data.\
![screenshot output](screenshot/ss1.png)

Contoh menampilkan Data.\
Dengan input data diri dan nilai-nilai.\
![screenshot output](screenshot/ss2.png)

Contoh mengubah data.\
Dengan input data diri dan nilai-nilai.\
![screenshot output](screenshot/ss3.png)\
![screenshot output](screenshot/ss4.png)

Contoh menghapus data.\
![screenshot output](screenshot/ss5.png)\
![screenshot output](screenshot/ss6.png)

Contoh mencari data.\
![screenshot output](screenshot/ss7.png)

#praktikum6
# LATIHAN 1 - DICTIONARY

    Dictionary adalah tipe data pada Python yang berfungsi untuk menyimpan kumpulan data
nilai dengan pendekatan "Key-Value".

    Dictionary sendiri memiliki dua buah komponen inti:

        1. Yang pertama adalah KEY, ia merupakan nama atribut suatu item pada Dictionary.
        2. Yang kedua adalah VALUE, ia adalah nilai yang disimpan pada suatu atribut.

## SOURCE CODE
![gambar1](https://github.com/nisanst11/praktikum6/blob/master/screenshoot/gambar1.jpeg)

## PENJELASAN

1. Membuat Dictionary Daftar Kontak. r = {'Ari' : '081267888', 'Dina' : '087677776'}.
2. Menampilkan kontak, untuk menampilkan salah satu kontak ialah menggunakan `r['Ari]`. r adalah variabel dictionary, sedangkan `['Ari]` adalah keys dari sebuah dictionary. Python `print("Menampilkan Kontak Ari: ", r['Ari']`).
3. Menambahkan kontak baru menggunakan `variable_dictionary['keys']=value;`. Python `r['Riko']= '087654544';`.
4. Mengubah kontak yang lama dengan yang baru, menggunakan `variable_dictionary['keys']=value;`. Disini saya akan mengubah value dari kontak Dina, yang awalnya `'Dina' : '087677776'` menjadi `r['Dina'] = '088999776'`.
5. Menampilkan keseluruhan nama pada kontak menggunakan `keys()`. Python `print(r.keys())`.
6. Menampilkan keseluruhan nomor kontak menggunakan `values()`. Python `print(r.values())`.
7.  Menampilkan keseluruhan nama beserta nomor kontak menggunakan `items()`. Python `print(r.items())`.
8. Untuk menghapus salah satu kontak menggunakan statement `del variable_dictionary[keys];`. Python `del r['Dina'];`.

## OUTPUT 
![gambar2](gambar/al2.png)

# PRAKTIKUM - DICTIONARY

## SOURCE CODE
![gambar3](gambar/al9.png)

![gambar4](gambar/al10.png)

## PENJELASAN

1. Membuat Dictionary kosong yang nanti akan diinput dengan sebuah data.
```
data={}
```
2. Membuat perulangan dengan while dan terdapat pilihan menu untuk menjalankan program.
```
while True:
print()
a=input("[(L)ihat, (T)ambah, (U)bah, (H)apus, (C)ari, (K)eluar] :")
print()
```
3. Menambahkan data nim, nama, nilai tugas, uts, dan uas. Data yang diinputkan akan masuk ke dalam Dictionary data dengan nim sebagai *keys_. sedangkan, nama, tugas, uts, dan uas sebagai _. sedangkan, nama, tugas, uts, dan uas sebagai _*values*_.
```
if a=="t" or a=="T":
    print("TAMBAH DATA")
    print("-----------")
    nim=int(input("NIM\t: "))
    nama=input("Nama\t: ")
    tugas=int(input("Tugas\t: ")) 
    uts=int(input("UTS\t: "))
    uas=int(input("UAS\t: "))
    akhir=(int(tugas)*30/100)+(int(uts)*35/100)+(int(uas)*35/100)
    data[nim]=nama, tugas, uts, uas, akhir
    print()
```
4. Menambahkan atau melihat data. Jika sebelumnya belum menginput data, maka tampilannya akan "Tidak ada data". Apabila sudah menginput data, maka data yang telah diinput tadi akan ditampilkan.
```
elif a=="l" or a=="L":
    if data.items():
        print("DAFTAR NILAI")
        print("------------")
        print(72*"=")
        print("| {0:^10} | {1:^10} | {2:^6} | {3:^6} | {4:^6} |   {5:^12}  |".format("NIM", "NAMA", "TUGAS", "UTS", "UAS", "NILAI AKHIR"))
        print(72*"=")
        for item in data.items(): 
            print("| {0:>10} | {1:>10} | {2:>6} | {3:>6} | {4:>6} |   {5:>12}  |".format(nim, nama, tugas, uts, uas, akhir))
            print(72*"=")
        print()
    else:
        print("DAFTAR NILAI")
        print("------------")
        print(72*"=")
        print("| {0:^10} | {1:^10} | {2:^6} | {3:^6} | {4:^6} |   {5:^12}  |".format("NIM", "NAMA", "TUGAS", "UTS", "UAS", "NILAI AKHIR"))
        print(72*"=")
        print("|                             TIDAK ADA DATA                           |")
        print(72*"=")
        print()
```
5. Apabila ingin mengubah data, maka anda akan diminta untuk menginput *NIM* terlebih dahulu. setelah itu input data yang ingin diubah.
```
elif a=="u" or a=="U":
        print("UBAH DATA")
        print("~~~~~~~~~~")
        b=input("Masukkan NIM anda: ")
        print()
        if data.keys():
            tugas=int(input("TUGAS\t: ")) 
            uts=int(input("UTS\t: "))
            uas=int(input("UAS\t: "))
            akhir=(int(tugas)*30/100)+(int(uts)*35/100)+(int(uas)*35/100)
```
6. Jika ingin menghapus data, anda akan diminta untuk menginput *NIM*terlebih dahulu. Lalu data yang telah diinput diawal tadi akan dihapus beserta _values_nya (nama, nilai tugas, nilai uts, dan nilai uas).
```
elif a=="h" or a=="H":
        print("HAPUS DATA")
        print("~~~~~~~~~~~")
        b=input("Masukkan NIM anda: ")
        print()
        if data.keys():
            del data[nim]
```
7. Apabila ingin mencari data, anda akan diminta untuk menginput *NIM* kemudian data yang anda cari akan muncul berdasarkan nim yang diinput tadi.
```
elif a=="c" or a=="C":
        print("CARI DATA")
        print("~~~~~~~~~~")
        b=input("Masukkan NIM anda: ")
        print()
        if data.keys():
            print(72*"=")
            print("| {0:^10} | {1:^10} | {2:^6} | {3:^6} | {4:^6} |   {5:^12}  |".format("NIM", "NAMA", "TUGAS", "UTS", "UAS", "NILAI AKHIR"))
            print(72*"=")
            print("| {0:>10} | {1:>10} | {2:>6} | {3:>6} | {4:>6} |   {5:>12}  |".format(nim, nama, tugas, uts, uas, akhir))
            print(72*"=")
            print()
```
8. Jika data sudah selesai diinput, pilih menu 'k'/'K' maka program akan terhenti.
```
 elif a=="k" or a=="K":
         break
```

## OUTPUT
![gambar5](gambar/al3.png)

![gambar6](gambar/al4.png)

![gambar7](gambar/al5.png)

![gambar8](gambar/al6.png)

![gambar9](gambar/al7.png)

![gambar10](gambar/al8.png)

## FLOWCHART
![gambar11](gambar/al11.png)

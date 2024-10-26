# LATIHAN 1

1. Penggunaan end dalam print
Menggunakan argumen end di dalam fungsi print() untuk menentukan karakter atau string yang akan ditampilkan di akhir setiap perintah print().

Input:
print('A', end='') # Tidak menambahkan karakter di akhir, jadi 'B' akan langsung diikuti setelah 'A'

print('B', end='') # Tidak menambahkan karakter di akhir, jadi 'C' akan langsung diikuti setelah 'B'

print('C', end='') # Tidak menambahkan karakter di akhir, print() berikutnya akan menambahkan newline

print()  # Tambahkan newline agar baris berikutnya dimulai di baris baru

print('X')
print('Y')
print('Z')

Output:
ABC
X
Y
Z

2. Penggunaan sep dalam print
Argumen sep digunakan dalam print() untuk menentukan karakter atau string yang akan digunakan sebagai pemisah (separator) antar nilai yang dicetak.

Input:
w, x, y, z = 10, 15, 20, 25
print(w, x, y, z)                 # Default pemisah (spasi)
print(w, x, y, z, sep=',')        # Menggunakan koma sebagai pemisah
print(w, x, y, z, sep='')         # Tidak ada pemisah (dicetak berdempetan)
print(w, x, y, z, sep=':')        # Menggunakan titik dua sebagai pemisah
print(w, x, y, z, sep='-----')    # Menggunakan string '-----' sebagai pemisah

Output:
10 15 20 25
10,15,20,25
10152025
10:15:20:25
10-----15-----20-----25

3. Contoh Format Sederhana pada String (String Formatting)
Mencetak nilai-nilai pangkat dari 10, di mana setiap baris mencetak nilai pangkat secara sederhana.

Input:
print(0, 10**0)
print(1, 10**1)
print(2, 10**2)
print(3, 10**3)
print(4, 10**4)
print(5, 10**5)
print(6, 10**6)
print(7, 10**7)
print(8, 10**8)
print(9, 10**9)
print(10, 10**10)

Output:
0 1
1 10
2 100
3 1000
4 10000
5 100000
6 1000000
7 10000000
8 100000000
9 1000000000
10 10000000000

4. Format String dengan Penyesuaian Lebar Kolom
Menggunakan format string untuk menyusun tampilan agar lebih rapi dengan pengaturan lebar kolom.

Input:
print('{0:>3} {1:>16}'.format(0, 10**0))
print('{0:>3} {1:>16}'.format(1, 10**1))
print('{0:>3} {1:>16}'.format(2, 10**2))
print('{0:>3} {1:>16}'.format(3, 10**3))
print('{0:>3} {1:>16}'.format(4, 10**4))
print('{0:>3} {1:>16}'.format(5, 10**5))
print('{0:>3} {1:>16}'.format(6, 10**6))
print('{0:>3} {1:>16}'.format(7, 10**7))
print('{0:>3} {1:>16}'.format(8, 10**8))
print('{0:>3} {1:>16}'.format(9, 10**9))
print('{0:>3} {1:>16}'.format(10, 10**10))

Output:
  0                1
  1               10
  2              100
  3             1000
  4            10000
  5           100000
  6          1000000
  7         10000000
  8        100000000
  9       1000000000
 10      10000000000

**LATIHAN 2**

1. Meminta Input untuk Variabel a dan b

Input:
a = input("masukkan nilai a: ")
b = input("masukkan nilai b: ")
# Program meminta input dari pengguna untuk variabel a dan b. Nilai yang dimasukkan adalah string.
print("variable a =", a)
print("variable b =", b)
# Menampilkan nilai a dan b yang diperoleh dari input sebelumnya.

Contoh Output:
variable a = 8
variable b = 4

2. Menggabungkan Dua String dalam Format Tertentu

Input:
print("hasil penggabungan {1} & {0} = {}".format(a, b, a + b))
# menggabungkan nilai a dan b sebagai string dan menampilkannya dalam format tertentu

Contoh Output:
hasil penggabungan 4 & 8 = 84

3. Konversi nilai variabel

Input:
a = int(a)
b = int(b)
# Mengonversi a dan b dari string menjadi integer agar bisa melakukan operasi aritmatika.
print("hasil penjumlahan [1]+[0]=%d".format(a,b) %(a+b))
# Kesalahan: format string salah. Perbaiki format string agar tidak menggunakan % bersama format().

Perbaikan:
print("hasil penjumlahan {1} + {0} = {}".format(a, b, a + b))

Contoh Output:
hasil penjumlahan 4 + 8 = 12

4. Menghitung Pembagian dengan Format yang Salah

print("hasil pembagian (1)/(B)=%d".format(a,b) %(a/b))
# Kesalahan: Penggunaan %d pada hasil pembagian menyebabkan error, karena hasil pembagian adalah tipe float.

Perbaikan: Gantilah %d dengan {:.2f} dalam format() untuk membatasi hasil pembagian hingga dua angka desimal.
print("hasil pembagian {1} / {0} = {}".format(a, b, a / b))

Contoh Output:
hasil pembagian 4 / 8 = 2.00

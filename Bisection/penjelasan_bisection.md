PENJELASAN PROGRAM METODE BISECTION

1. Pengertian Program

Program ini dibuat untuk menyelesaikan persamaan nonlinear menggunakan metode Bisection atau metode bagi dua. Metode ini digunakan untuk mencari nilai akar suatu persamaan dengan membagi interval menjadi dua bagian secara berulang.

2. Tujuan Program

Tujuan program ini adalah:

- Menentukan akar dari suatu persamaan nonlinear.
- Memahami proses pembagian interval menjadi dua bagian.
- Mendapatkan hasil perhitungan dengan tingkat ketelitian tertentu.
- Menerapkan metode Bisection menggunakan bahasa Python.

3. Penjelasan Kode Program

A. Mendefinisikan Fungsi

Kode:
"def f(x):"
"    return x**3 - x - 2"

Penjelasan:

Bagian ini digunakan untuk mendefinisikan fungsi matematika yang akan dicari akarnya, yaitu f(x) = x³ - x - 2.

B. Menentukan Interval

Kode:
"a = 1.0"
"b = 2.0"

Penjelasan:

Variabel a merupakan batas bawah interval, sedangkan b merupakan batas atas interval. Interval awal yang digunakan adalah 1 sampai 2.

C. Menentukan Toleransi dan Iterasi

Kode:
"toleransi = 1e-6"
"maks_iterasi = 100"

Penjelasan:

Toleransi digunakan untuk menentukan tingkat ketelitian hasil perhitungan. Maks_iterasi menentukan jumlah pengulangan maksimal agar proses tidak berjalan tanpa batas.

D. Memeriksa Interval Awal

Kode:
"if f(a) * f(b) >= 0:"

Penjelasan:

Bagian ini memeriksa apakah nilai fungsi pada kedua batas interval memiliki tanda yang berbeda. Jika hasil perkaliannya tidak negatif, program memberikan peringatan bahwa interval tersebut belum memenuhi syarat metode Bisection.

E. Menghitung Titik Tengah

Kode:
"c = (a + b) / 2"

Penjelasan:

Rumus tersebut digunakan untuk mencari titik tengah dari interval batas bawah dan batas atas.

F. Melakukan Perulangan

Kode:
"for i in range(1, maks_iterasi + 1):"

Penjelasan:

Perulangan digunakan untuk melakukan proses pembagian interval secara berulang sampai memenuhi batas toleransi atau jumlah iterasi maksimal.

G. Memperbarui Interval

Kode:
"if f(a) * f(c) < 0:"
"    b = c"
"else:"
"    a = c"

Penjelasan:

Bagian ini menentukan interval baru berdasarkan tanda nilai fungsi. Jika akar berada di antara a dan c, batas atas diganti menjadi c. Jika tidak, batas bawah diganti menjadi c.

H. Menampilkan Hasil

Kode:
"print("Akar persamaan =", c)"

Penjelasan:

Perintah print digunakan untuk menampilkan nilai akar persamaan yang diperoleh dari proses perhitungan.

4. Hasil Pengujian

Persamaan yang digunakan:

f(x) = x³ - x - 2

Interval awal:

- Batas bawah = 1
- Batas atas = 2
- Toleransi = 0,000001

Hasil perhitungan mendekati:

Akar persamaan = 1,52138

5. Kesimpulan

Berdasarkan pengujian, program berhasil menerapkan metode Bisection untuk mencari akar persamaan nonlinear. Proses dilakukan dengan membagi interval menjadi dua bagian secara berulang hingga mendapatkan nilai akar yang mendekati hasil sebenarnya.

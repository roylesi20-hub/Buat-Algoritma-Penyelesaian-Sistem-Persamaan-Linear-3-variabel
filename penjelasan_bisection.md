# PENJELASAN PROGRAM METODE BISECTION

## 1. Pengertian
Metode Bisection adalah metode numerik untuk mencari nilai akar dari suatu persamaan nonlinear. Metode ini menggunakan dua batas awal, yaitu a dan b, yang harus menghasilkan nilai fungsi dengan tanda berbeda.

## 2. Tujuan Program
Program ini dibuat untuk mencari nilai akar persamaan nonlinear menggunakan metode Bisection dengan bantuan bahasa pemrograman Python.

## 3. Penjelasan Kode

### Bagian 1: Membuat Fungsi
def f(x):
    return x**3 - x - 2

Fungsi tersebut merupakan persamaan nonlinear yang akan dicari nilai akarnya.

### Bagian 2: Menentukan Nilai Awal
a = 1.0
b = 2.0
toleransi = 1e-6
maks_iterasi = 100

Variabel a dan b merupakan batas awal pencarian akar. Toleransi menentukan tingkat ketelitian, sedangkan maks_iterasi menentukan jumlah pengulangan maksimal.

### Bagian 3: Memeriksa Interval
if f(a) * f(b) >= 0:
    raise ValueError("Interval tidak memenuhi syarat")

Bagian ini memeriksa apakah nilai fungsi pada kedua batas memiliki tanda yang berbeda. Jika tidak, proses dihentikan karena interval belum memenuhi syarat metode Bisection.

### Bagian 4: Proses Perulangan
for i in range(1, maks_iterasi + 1):
    c = (a + b) / 2

Perulangan dilakukan untuk mencari titik tengah interval. Variabel c merupakan hasil pembagian dua antara batas a dan b.

### Bagian 5: Memperbarui Interval
if f(a) * f(c) < 0:
    b = c
else:
    a = c

Program menentukan interval baru berdasarkan tanda hasil fungsi. Proses ini dilakukan berulang sampai ketelitian terpenuhi.

### Bagian 6: Menampilkan Hasil
print("Akar persamaan =", c)

Bagian ini menampilkan perkiraan nilai akar persamaan yang diperoleh dari proses perhitungan.

## 4. Kesimpulan
Metode Bisection dapat digunakan untuk mencari akar persamaan nonlinear dengan membagi interval menjadi dua bagian secara berulang. Semakin kecil toleransi yang digunakan, semakin tinggi ketelitian hasil perhitungan.

# Tugas-Matrikulasi-Algoritma-dan-Pemrograman
# operasi matriks 3x3 
# Matriks A dan B 
# Matriks A = 123 / 321 / 213    [[1,2,3], [3,2,1], [2,1,3]]
# Matriks B = 321 / 123 / 312    [[3,2,1], [1,2,3], [3,1,2]]

# Library Awal
A = [
[1, 2, 3],
[3, 2, 1],
[2, 1, 3]
]

B = [
[3, 2, 1],
[1, 2, 3],
[3, 1, 2]
]

def cetak_matriks(M) :
for i in range (3):
for j in range (3):
baris = baris + str(M[i][j])
if j < 2:
print(baris)
print()

def penjumlahan (A, B):
# C = A + B
C = [
    [0, 0, 0]
    [0, 0, 0]
    [0, 0, 0]
    ]
for i in range(3):
for j in range(3):
C[i][j] = A[i][j] + B[i][j]
  return C

def perkalian(A, B):
# C = A * B
C = [
    [0, 0, 0]
    [0, 0, 0]
    [0, 0, 0]
    ]
for i in range(3):
for j in range(3):
jumlah = 0
for k in range 
jumlah = jumlah + (A[i][k] * B[k][j]) 
C[i][j] = jumlah
   return C

def matriks_satuan(M):
# True jika M adalah matriks satuan 3x3 (1 di diagonal, 0 di luar diagonal)
for i in range(3):
for j in range(3):
if i == j:
if M[i][j] != 1:
return False
    else:
if M[i][j] != 0:
return False
    return True

# Program 
print("Matriks A:")
cetak_matriks(A)
print("Matriks B:")
cetak_matriks(B)

print("Pilihan Operasi Matriks:")
print("1. Penjumlahan A + B")
print("2. Pengurangan A - B")
print("3. Perkalian A * B")
print("4. Pemeriksaan Matriks A dan B apakah Matriks Satuan")

if pilihan == 1:
    print("Hasil Penjumlahan A + B:")
    hasil = penjumlahan(A, B)
    cetak_matriks(hasil)

elif pilihan == 2:
    print("Hasil Pengurangan A - B:")
    hasil = pengurangan(A, B)
    cetak_matriks(hasil)

elif pilihan == 3:
    print("Hasil Perkalian A * B:")
    hasil = perkalian(A, B)
    cetak_matriks(hasil)

elif pilihan == 4:
    a_satuan = matriks_satuan(A)
    b_satuan = matriks_satuan(B)
    print("Matriks A adalah matriks satuan:", "YA" if a_satuan else "TIDAK")
    print("Matriks B adalah matriks satuan:", "YA" if b_satuan else "TIDAK")
    if a_satuan and b_satuan:
        print("Kedua matriks adalah matriks satuan")
    else:
        print("Salah satu atau kedua matriks bukan matriks satuan")

else:
    print("Bukan Pilihan Yang Benar")

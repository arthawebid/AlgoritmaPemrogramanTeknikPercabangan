Berikut adalah materi perkuliahan untuk **Algoritma Pemrograman** dengan fokus pada **Pengenalan Teknik Percabangan** dan implementasinya menggunakan struktur **If**, **If-Else**, **Nested If**, dan **Switch**:

---

### **Materi Perkuliahan: Algoritma Pemrograman – Teknik Percabangan**

#### **1. Pengenalan Teknik Percabangan**

Percabangan (branching) adalah konsep dasar dalam pemrograman yang memungkinkan program untuk melakukan keputusan berdasarkan kondisi tertentu. Dalam percabangan, kita bisa menentukan alur eksekusi program berdasarkan hasil evaluasi kondisi (benar atau salah).

Pada umumnya, percabangan digunakan untuk:
- Memilih satu di antara beberapa jalur eksekusi.
- Menangani berbagai kemungkinan kondisi dalam program.

Percabangan umumnya digunakan untuk pengambilan keputusan yang melibatkan pernyataan **true/false** (kondisional). Dalam bahasa pemrograman, kita bisa menggunakan beberapa bentuk struktur percabangan seperti **if**, **if-else**, **nested if**, dan **switch**.

---

#### **2. Penggunaan Percabangan `If`**

Struktur percabangan `if` adalah bentuk percabangan yang paling sederhana. Pernyataan `if` digunakan untuk mengevaluasi suatu kondisi dan mengeksekusi blok kode tertentu jika kondisi tersebut **benar**.

**Sintaks:**
```python
if kondisi:
    # Blok kode yang dijalankan jika kondisi bernilai True
```

**Contoh:**
```python
x = 10
if x > 5:
    print("x lebih besar dari 5")
```

Pada contoh di atas, program akan mencetak "x lebih besar dari 5" karena kondisi `x > 5` bernilai **True**.

---

#### **3. Penggunaan Percabangan `If-Else`**

Struktur percabangan `if-else` digunakan untuk mengevaluasi kondisi dan mengeksekusi salah satu blok kode berdasarkan apakah kondisi tersebut **benar** atau **salah**. Jika kondisi bernilai **True**, blok kode setelah `if` yang dieksekusi; jika kondisi bernilai **False**, blok kode setelah `else` yang dieksekusi.

**Sintaks:**
```python
if kondisi:
    # Blok kode yang dijalankan jika kondisi bernilai True
else:
    # Blok kode yang dijalankan jika kondisi bernilai False
```

**Contoh:**
```python
x = 3
if x > 5:
    print("x lebih besar dari 5")
else:
    print("x tidak lebih besar dari 5")
```

Pada contoh ini, program akan mencetak "x tidak lebih besar dari 5" karena kondisi `x > 5` bernilai **False**.

---

#### **4. Penggunaan Percabangan `Nested If`**

**Nested if** adalah teknik di mana satu pernyataan `if` berada di dalam pernyataan `if` lainnya. Dengan menggunakan teknik ini, kita bisa membuat keputusan yang lebih kompleks dengan memeriksa beberapa kondisi secara bertingkat.

**Sintaks:**
```python
if kondisi1:
    if kondisi2:
        # Blok kode jika kondisi1 dan kondisi2 keduanya bernilai True
    else:
        # Blok kode jika kondisi1 True dan kondisi2 False
else:
    # Blok kode jika kondisi1 False
```

**Contoh:**
```python
x = 8
y = 10
if x > 5:
    if y > 5:
        print("x dan y keduanya lebih besar dari 5")
    else:
        print("x lebih besar dari 5, tapi y tidak lebih besar dari 5")
else:
    print("x tidak lebih besar dari 5")
```

Pada contoh ini, program akan mencetak "x dan y keduanya lebih besar dari 5" karena kedua kondisi `x > 5` dan `y > 5` bernilai **True**.

---

#### **5. Penggunaan `Switch` (atau `match` dalam Python)**

Pada beberapa bahasa pemrograman, kita memiliki struktur percabangan **switch-case** yang memungkinkan kita memeriksa berbagai kemungkinan nilai dalam satu variabel dan mengeksekusi kode sesuai dengan nilai tersebut. Namun, dalam Python, kita tidak memiliki pernyataan `switch` secara langsung, tetapi bisa menggunakan **`match-case`** (sejak Python 3.10).

**Sintaks `switch` di beberapa bahasa (misalnya Java, C++):**
```java
switch (variabel) {
    case nilai1:
        // Blok kode untuk nilai1
        break;
    case nilai2:
        // Blok kode untuk nilai2
        break;
    default:
        // Blok kode jika tidak ada yang cocok
}
```

**Contoh dalam bahasa Java:**
```java
int hari = 2;
switch (hari) {
    case 1:
        System.out.println("Senin");
        break;
    case 2:
        System.out.println("Selasa");
        break;
    case 3:
        System.out.println("Rabu");
        break;
    default:
        System.out.println("Hari tidak dikenal");
}
```

Pada contoh ini, program akan mencetak "Selasa" karena nilai variabel `hari` adalah 2.

**Contoh menggunakan `match-case` di Python (versi 3.10+):**
```python
hari = 2
match hari:
    case 1:
        print("Senin")
    case 2:
        print("Selasa")
    case 3:
        print("Rabu")
    case _:
        print("Hari tidak dikenal")
```

Output dari program di atas adalah "Selasa" karena nilai variabel `hari` adalah 2.

---

#### **6. Kapan Menggunakan Teknik Percabangan Tertentu?**

- **`If`**: Digunakan ketika Anda hanya membutuhkan satu keputusan sederhana untuk dijalankan ketika suatu kondisi benar.
- **`If-Else`**: Digunakan ketika Anda memiliki dua kemungkinan jalur eksekusi, yaitu ketika kondisi tersebut benar atau salah.
- **`Nested If`**: Digunakan saat Anda perlu membuat keputusan bertingkat, di mana setelah kondisi pertama, kondisi kedua (dan seterusnya) juga harus diperiksa.
- **`Switch`**: Berguna ketika Anda memiliki banyak kondisi dengan nilai tetap dan ingin memilih salah satu dari banyak kemungkinan yang dapat dipecahkan dengan lebih mudah.

---

### **Latihan**

1. Buatlah program untuk menentukan apakah sebuah angka adalah bilangan ganjil atau genap menggunakan percabangan `if-else`.
2. Buat program untuk menghitung grade mahasiswa berdasarkan nilai yang dimasukkan menggunakan percabangan `if-else if`.
3. Buat program yang menggunakan `switch-case` (atau `match-case` di Python) untuk mencetak nama hari berdasarkan angka yang dimasukkan (misalnya: 1 = Senin, 2 = Selasa, dst).
4. Buatlah program untuk menentukan apakah sebuah angka termasuk dalam kategori positif, negatif, atau nol menggunakan nested if.

---

### **Ringkasan**

- **Percabangan** memungkinkan pengambilan keputusan dalam program.
- **`if`** digunakan untuk kondisi sederhana.
- **`if-else`** digunakan untuk dua kondisi yang saling bertolak belakang.
- **`nested if`** digunakan untuk kondisi bertingkat.
- **`switch`** atau **`match-case`** digunakan untuk memilih salah satu dari beberapa kemungkinan nilai yang lebih kompleks.

Dengan memahami teknik percabangan ini, Anda akan dapat mengendalikan alur eksekusi program sesuai dengan kondisi yang ada.

--- 

Semoga materi ini membantu!

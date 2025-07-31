
---

````markdown

Laporan Praktikum - Kolaborasi Android Studio dengan GitHub  
Kelas: XII TJKT 1

---

Nama Anggota Kelompok:
- Pramudya Kalya Zaki  
- Liana Amaliyatussyarifa  
- Nur Aimah Auliya Aprilianingrum  


Tujuan Praktikum
Mempelajari cara membuat aplikasi Android sederhana menggunakan Kotlin dan Android Studio, serta memahami cara penggunaan Git dan GitHub untuk kolaborasi proyek secara tim.


 Fitur Aplikasi
- Menampilkan `TextView`
- Menampilkan tombol `Button` untuk memproses data input

````
## Struktur Layout (XML)
```xml
<EditText android:id="@+id/etNama" />
<EditText android:id="@+id/etKelas" />
<Button android:id="@+id/btnTampilkan" />
<TextView android:id="@+id/tvHasil" />
**Penjelasan Komponen:**

* `EditText`: Digunakan untuk input teks (nama dan kelas)
* `Button`: Tombol untuk memproses data saat diklik
* `TextView`: Menampilkan hasil input dari pengguna
  
## Kode Kotlin (MainActivity.kt)

```kotlin
private lateinit var inputName: EditText
private lateinit var inputKelas: EditText
private lateinit var btnSubmit: Button
private lateinit var txtResult: TextView
```

* `private`: Hanya dapat diakses dari dalam class (encapsulation)
* `lateinit`: Variabel akan diinisialisasi nanti

### Fungsi `onCreate()`

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
    setContentView(R.layout.activity_main)
}
```

* `onCreate()`: Dipanggil saat Activity pertama kali diluncurkan
* `setContentView()`: Menampilkan layout XML ke tampilan aplikasi

### Event Button (Klik)

```kotlin
btnSubmit.setOnClickListener {
    val nama = inputName.text.toString().trim()
    val kelas = inputKelas.text.toString().trim()
    val hasil = "Nama: $nama\nKelas: $kelas"
    txtResult.text = hasil
}
```

* Mengambil input dari `EditText`
* Menampilkan hasil input ke `TextView`

---

## 📷 Hasil Tampilan Aplikasi

<img width="275" height="564" alt="image" src="https://github.com/user-attachments/assets/792d6e44-2bce-47d8-aaaa-9da35c8d81ca" />
<img width="278" height="562" alt="image" src="https://github.com/user-attachments/assets/ca6bd3f4-6700-4db1-aaf8-222434374774" />

---

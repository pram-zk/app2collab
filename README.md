

---

````markdown
# 📱 Project Kolaborasi Android

Ini adalah proyek sederhana untuk belajar kolaborasi menggunakan **Git & Android Studio**

---

## 👥 Tim
- Pramudya Kalya Zaki: Inisialisasi & Merge PR  
- Liana Amaliyatussyarifa: Fitur TextView  
- Nur Aimah Auliya Aprilianingrum: Fitur Button  

---

## 📋 Fitur
- Menampilkan `TextView`  
- Menampilkan `Button` yang dapat diklik untuk menampilkan hasil input  

---

## 🔧 Teknologi
- Kotlin  
- Android Studio  
- Git + GitHub  

---

## 💡 Penjelasan code penting

```kotlin
private lateinit var inputName: EditText
private lateinit var inputKelas: EditText
private lateinit var btnSubmit: Button
private lateinit var txtResult: TextView
````

* `lateinit`: variabel diinisialisasi nanti, bukan langsung
* `private`: hanya bisa digunakan di dalam class

```kotlin
override fun onCreate(savedInstanceState: Bundle?) {
    setContentView(R.layout.activity_main)
}
```

* Fungsi `onCreate`: dijalankan pertama kali saat aplikasi dibuka

```kotlin
btnSubmit.setOnClickListener {
    val nama = inputName.text.toString().trim()
    val kelas = inputKelas.text.toString().trim()
    val hasil = "Nama: $nama\nKelas: $kelas"
    txtResult.text = hasil
}
```

* Saat tombol diklik, aplikasi akan mengambil data input dan menampilkannya di `TextView`.

---

## 📷 Screenshot

<img width="275" height="564" alt="image" src="https://github.com/user-attachments/assets/792d6e44-2bce-47d8-aaaa-9da35c8d81ca" />
<img width="278" height="562" alt="image" src="https://github.com/user-attachments/assets/ca6bd3f4-6700-4db1-aaf8-222434374774" />

---

```

```

# Project Kolaborasi Android

Ini adalah proyek sederhana untuk belajar kolaborasi menggunakan Git & Android Studio

## Tim
- Pramudya Kalya Zaki: Inisialisasi & Merge PR
- Liana Amaliyatussyarifa: Fitur TextView
- Nur Aimah Auliya Aprilianingrum: Fitur Button

## Fitur
- Menampilkan TextView
- Menampilkan Button yang dapat diklik

## Teknologi
- Kotlin
- Android Studio
- Git & GitHub

## Penjelasan Code Penting
<androidx.constraintlayout.widget.ConstraintLayout> = Layout utama yang fleksibel dan bisa mengatur posisi elemen berdasarkan "batas" (constraint) atas, bawah, kiri, kanan.

android:layout_width="match_parent" → Lebarnya mengikuti ukuran layar.

android:layout_height="match_parent" → Tingginya juga mengikuti layar.

android:background="#F5F5F5" → Warna latar abu-abu muda.

tools:context=".MainActivity" → Menandakan layout ini digunakan oleh MainActivity.

<LinearLayout
    android:orientation="vertical"
    ... /> = Untuk menata semua elemen isi secara vertikal (atas ke bawah).
    
layout_width="0dp" → Artinya akan mengikuti lebar yang ditentukan oleh constraint (Start dan End ke parent).

layout_height="wrap_content" → Tingginya menyesuaikan isi.

android:background="@android:color/white" → Latar putih agar terlihat seperti kartu.

android:elevation="4dp" → Memberikan bayangan (efek 3D).

android:padding="24dp" → Jarak ke dalam agar isi tidak mepet.

<TextView
    android:text="Form Biodata Siswa"
    android:textAlignment="center"
    ... /> = Menampilkan teks judul di tengah serta teks dibuat tebal dan besar

<EditText
    android:hint="Masukkan Nama"
    android:inputType="textPersonName"
    ... /> = Untuk mengisi nama siswa.

hint: teks petunjuk sebelum diketik.

inputType: khusus nama orang (huruf kapital otomatis).

backgroundTint="#6200EE" → garis bawah berwarna ungu.

<EditText
    android:hint="Masukkan Kelas"
    ... /> = Untuk mengisi kelas siswa. Sama seperti EditText sebelumnya, hanya berbeda hint dan inputType.

<Button
    android:text="Tampilkan"
    android:backgroundTint="#03DAC5"
    ... /> = Tombol yang akan ditekan untuk menampilkan biodata.

textAllCaps="false" → Huruf pada tombol tidak semua besar.

layout_gravity="center" → Tombol di tengah secara horizontal.

<TextView
    android:id="@+id/tvHasil"
    android:text=" "
    ... /> = Tempat menampilkan hasil biodata setelah tombol ditekan.

class MainActivity : AppCompatActivity() { = Artinya MainActivity adalah activity layar yang menggunakan fitur dari AppCompatActivity.

private lateinit var inputName: EditText
private lateinit var inputKelas: EditText
private lateinit var btnSubmit: Button
private lateinit var txtResult: TextView
lateinit: artinya variabel akan di-inisialisasi nanti, bukan langsung saat dideklarasikan.
Digunakan untuk menyambungkan elemen tampilan XML dengan Kotlin (findViewById).

override fun onCreate(savedInstanceState: Bundle?) { = Fungsi yang pertama kali dijalankan saat activity dibuka.

enableEdgeToEdge()
ViewCompat.setOnApplyWindowInsetsListener(...)
Ini bagian untuk menyesuaikan tampilan layar penuh dan memastikan UI tidak tertimpa oleh status bar atau navigation bar.

inputName = findViewById(R.id.etNama)
inputKelas = findViewById(R.id.etKelas)
btnSubmit = findViewById(R.id.btnTampilkan)
txtResult = findViewById(R.id.tvHasil)
Menghubungkan komponen dari XML dengan variabel Kotlin.

btnSubmit.setOnClickListener {
    val nama = inputName.text.toString().trim()
    val kelas = inputKelas.text.toString().trim()
    val hasil = "Nama: $nama\nKelas: $kelas"
    txtResult.text = hasil
}
Ambil input dari EditText → .text.toString().trim()
trim() untuk menghapus spasi di depan dan belakang.
Gabungkan hasil ke dalam satu string.
Tampilkan hasil ke TextView (tvHasil).

##
<activity
            android:name=".activity_splash"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
        <activity
            android:name=".MainActivity"
            android:exported="true" />
##

## Screenshoot
<img width="275" height="564" alt="image" src="https://github.com/user-attachments/assets/792d6e44-2bce-47d8-aaaa-9da35c8d81ca" />
<img width="278" height="562" alt="image" src="https://github.com/user-attachments/assets/ca6bd3f4-6700-4db1-aaf8-222434374774" />



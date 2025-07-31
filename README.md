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
1.
import android.os.Bundle = Digunakan untuk mengakses `Bundle`, yaitu objek yang digunakan untuk menyimpan data sementara saat `onCreate()` dijalankan.
Mengimpor class-class tampilan dari widget Android yang digunakan di layout XML.
import android.widget.Button Fungsinya Tombol yang bisa ditekan
import android.widget.EditText Fungsinya Kolom input teks
import android.widget.TextView Fungsinya Teks yang bisa ditampilkan di layar (statis/dinamis)
import androidx.activity.enableEdgeToEdge =
- Fungsi dari AndroidX yang memungkinkan desain layar penuh (edge-to-edge) agar UI lebih modern.
- Menyembunyikan status bar/navigation bar jika ingin tampilan aplikasi penuh dari ujung ke ujung layar.
import androidx.appcompat.app.AppCompatActivity = Mengimpor class AppCompatActivity, yaitu activity standar modern di Android.
import androidx.core.view.ViewCompat = Utility untuk kompatibilitas tampilan, misalnya menambahkan padding sesuai sistem (status bar, navigation bar)
import androidx.core.view.WindowInsetsCompat = Digunakan untuk mengelola ruang tampilan yang dipengaruhi sistem (misal status bar, keyboard, dll)

2.
- private lateinit var inputName: EditText
Menyimpan referensi ke EditText yang digunakan untuk input nama siswa.

R.id.etNama di XML.

- private lateinit var inputKelas: EditText
Menyimpan referensi ke EditText untuk input kelas siswa.

R.id.etKelas di XML.

- private lateinit var btnSubmit: Button
Menyimpan referensi ke Button yang ditekan untuk menampilkan hasil.

R.id.btnTampilkan di XML.

- private lateinit var txtResult: TextView
Menyimpan referensi ke TextView yang akan menampilkan hasil input setelah tombol ditekan.

R.id.tvHasil di XML.

3. override fun onCreate
- override
Menandakan bahwa kamu sedang menimpa fungsi (onCreate) dari superclass (AppCompatActivity).

- fun onCreate(savedInstanceState: Bundle?)
Fungsi dengan 1 parameter savedInstanceState yang bisa menyimpan data saat rotasi layar, navigasi ulang, dsb.

4. setContentView(R.layout.activity_main)
adalah perintah utama dalam Android untuk menampilkan tampilan (layout XML) ke layar saat Activity dijalankan.

5.
1. inputName = findViewById(R.id.etNama)
- Mencari komponen EditText yang memiliki ID etNama di XML.
- Hasil pencarian disimpan dalam variabel inputName.
- Sekarang kamu bisa membaca atau mengatur teks input dari inputName di Kotlin.

2. inputKelas = findViewById(R.id.etKelas)
- Sama seperti di atas, tapi untuk EditText dengan ID etKelas.

3. btnSubmit = findViewById(R.id.btnTampilkan)
- Menghubungkan tombol (Button) dari layout ke variabel btnSubmit.
- Dengan ini kamu bisa memberi aksi ketika tombol ditekan menggunakan btnSubmit.setOnClickListener { ... }.

4. txtResult = findViewById(R.id.tvHasil)
- Menghubungkan TextView yang digunakan untuk menampilkan hasil input ke dalam variabel txtResult.

6.
1. btnSubmit.setOnClickListener { ... }
- Fungsi ini akan menjalankan blok kode di dalam {} saat tombol ditekan.
- Tombolnya diambil dari findViewById(R.id.btnTampilkan) sebelumnya.
2. val nama = inputName.text.toString().trim()
- Mengambil teks dari EditText inputName (input nama siswa).
- text: mendapatkan teks dari EditText.
- toString(): mengubah ke format String.
- trim(): menghapus spasi kosong di awal dan akhir.
3. val kelas = inputKelas.text.toString().trim()
- Sama seperti di atas, tapi untuk input kelas siswa.
4. val hasil = "Nama: $nama\nKelas: $kelas"
- Membuat string hasil dari data yang diinputkan.
- \n digunakan untuk pindah baris.
5. txtResult.text = hasil
- Menampilkan hasil ke TextView (tvHasil) di layar.
- Teks akan langsung muncul begitu tombol ditekan.


##
<activity

            android:name=".activity_splash"  → Menambahkan halaman baru bernama activity_splash ke dalam aplikasi.

            android:exported="true"> → Artinya aktivitas ini bisa dijalankan dari luar aplikasi
            
            <intent-filter> → Digunakan untuk menjadikan halaman ini sebagai halaman awal saat aplikasi dibuka.
            
                <action android:name="android.intent.action.MAIN" /> → Menandai ini sebagai aktivitas utama aplikasi.
                
                <category android:name="android.intent.category.LAUNCHER" /> → Menjadikan ikon aplikasi membuka halaman ini saat diklik.
                
            </intent-filter>
            
        </activity>
        
        <activity
        
            android:name=".MainActivity"
            
            android:exported="true" />

Baris ini memberitahu Android bahwa activity_splash adalah halaman pertama (launcher) saat aplikasi dijalankan.
intent-filter dengan MAIN dan LAUNCHER digunakan untuk menjadikan SplashActivity sebagai titik masuk aplikasi.
MainActivity tetap dideklarasikan, tapi tidak dijadikan launcher.

##
Handler(Looper.getMainLooper()).postDelayed({

            val intent = Intent(this, MainActivity::class.java) → Membuat intent (perintah) untuk pindah dari SplashActivity ke MainActivity.
            
            startActivity(intent) → Menjalankan MainActivity.
            
            finish() → Menutup SplashActivity supaya tidak bisa dikembalikan dengan tombol Back.
            
        }, 3000) → Menjalankan kode setelah delay 3000 milidetik (3 detik).


##
<ImageView → Digunakan untuk menampilkan gambar di layar.

        android:id="@+id/logoSMK" → Nama ID komponen ini agar bisa dipanggil di Kotlin.
        
        android:layout_width="200dp" → Ukuran gambar 200dp x 200dp.
        android:layout_height="200dp" →
        android:src="@drawable/logo_smk" → Gambar yang ditampilkan berasal dari file drawable bernama logo_smk.png.

        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent" />

ConstraintLayout digunakan, jadi keempat sisi di-constraint ke parent untuk posisi tepat di tengah (centered).

##
## Screenshoot

<img width="275" height="590" alt="image" src="https://github.com/user-attachments/assets/f158d0cc-22dc-4eea-957b-126021ee7ed1" />
<img width="275" height="562" alt="image" src="https://github.com/user-attachments/assets/792d6e44-2bce-47d8-aaaa-9da35c8d81ca" />
<img width="275" height="562" alt="image" src="https://github.com/user-attachments/assets/ca6bd3f4-6700-4db1-aaf8-222434374774" />

Gambar-gambar menunjukkan:
Tampilan logo SMK saat splash screen.
Setelah 3 detik, layar berpindah ke MainActivity.


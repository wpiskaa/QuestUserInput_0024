# QuestUserInput_0024 - Pertemuan 5 (Aktivitas 4)

Proyek aplikasi Android berbasis **Jetpack Compose** untuk praktikum mata kuliah **Pengembangan Aplikasi Mobile (PAM)** Pertemuan 5 (Aktivitas 4). Aplikasi ini mengimplementasikan formulir biodata diri (*user input*) dengan validasi tombol dan menampilkan hasilnya ke dalam komponen *Card*.

---

## 👤 Identitas Mahasiswa
- **NIM:** 20220140024 (0024)
- **Mata Kuliah:** Pengembangan Aplikasi Mobile (PAM)
- **Topik:** Pertemuan 5 - Quest User Input (Act 4)

---

## 📱 Fitur & Komponen Utama
1. **Input Nama Lengkap:**
   - Komponen: `OutlinedTextField`
   - Kustomisasi: Menggunakan sudut membulat dengan `shape = MaterialTheme.shapes.large` dan `singleLine = true`.
2. **Pilihan Jenis Kelamin (Gender):**
   - Komponen: `Row` dengan modifier `selectable` dan `RadioButton`.
   - Data sumber: `listOf("Laki-Laki", "Perempuan")`.
3. **Input Alamat:**
   - Komponen: `OutlinedTextField`
   - Kustomisasi: Menggunakan lebar tertentu dengan `Modifier.width(250.dp)`.
4. **Garis Pemisah (`HorizontalDivider`):**
   - Dua buah pembatas horizontal (sebelum dan sesudah tombol submit).
   - Menggunakan padding vertikal `padding_medium` (30dp) dan ketebalan `divider_tipis` (1dp) dari resource `dimens.xml`.
5. **Tombol Submit (`Button`):**
   - Menggunakan teks `"Submit"` dari resource `strings.xml`.
   - **Validasi State:** Tombol hanya aktif (`enabled = textAlamat.isNotEmpty()`) saat kolom alamat tidak kosong.
   - Mengupdate state tampilan (`nama`, `jenis`, `alamat`) saat diklik.
6. **Tampilan Hasil Biodata (`ElevatedCard`):**
   - Berlatar belakang hitam (`Color.Black`) dengan elevasi `10.dp`, tinggi `100.dp`, dan lebar `300.dp`.
   - Menampilkan teks putih:
     - `Nama : <nama>`
     - `Gender : <jenis>`
     - `Alamat : <alamat>`

---

## 📷 Hasil Running Aplikasi

| Tampilan Form Input | Hasil Submit Biodata |

<img width="1080" height="2400" alt="image" src="https://github.com/user-attachments/assets/1f6795dc-aeff-4f3a-ac3b-311e17c4032c" />

> **Catatan:** Tangkapan layar (*screenshot*) di atas dapat diperbarui langsung melalui emulator Android Studio / device fisik dan disimpan di folder `screenshots/` atau diunggah langsung ke README GitHub.

---

## 🛠️ Tech Stack & Requirements
- **Language:** Kotlin
- **UI Framework:** Jetpack Compose (Material 3)
- **Min SDK:** 24 (Android 7.0)
- **Target / Compile SDK:** 34+
- **Gradle Version:** Gradle 8.x / Android Gradle Plugin

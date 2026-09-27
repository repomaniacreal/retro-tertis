# 🕹️ Retro Amber CRT Tetris

Game Tetris bergaya retro klasik dengan tampilan layar monitor CRT berbahan amber (oranye/cokelat tembaga). Game ini dibuat menggunakan **HTML5 Canvas**, **CSS3**, dan **JavaScript murni (Vanilla JS)** tanpa menggunakan *library* atau *framework* tambahan.

---

## 📸 Fitur Utama

- **Estetika Retro CRT**: Efek *scanlines*, *screen flicker*, font piksel arcade (`VT323`), dan pendaran cahaya (*amber glow*) yang memberikan nuansa komputer / mesin arcade era 80-an.
- **Single File & Ringan**: Semua kode (HTML, CSS, JavaScript) dikemas rapi dalam satu file tunggal tanpa *dependency* npm.
- **Sistem Leveling Otomatis**: Kecepatan jatuh balok (*gravity*) bertambah setiap kali Anda membersihkan 10 baris.
- **Kontrol Fleksibel**: Mendukung keyboard untuk pengguna PC/Laptop dan tombol sentuh (*touch screen*) untuk pengguna perangkat seluler/HP.
- **Penyimpanan High Score**: Skor tertinggi disimpan secara otomatis di *Local Storage* browser.
- **Efek Bayangan Balok (Ghost Piece)**: Memudahkan prediksi posisi jatuh balok di bagian bawah.

---

## 🚀 Cara Pemasangan & Menjalankan Game

Karena game ini berbasis *single-file*, pemasangannya sangat mudah dan tidak memerlukan instalasi *Node.js* atau server rumit.

### 1. Simpan Kode Game
1. Salin (*copy*) seluruh kode game yang telah dibuat.
2. Buat file baru di komputer Anda dan beri nama `index.html`.
3. Tempel (*paste*) kode tersebut ke dalam file `index.html` dan simpan.

### 2. Jalankan di Browser
- **Metode Langsung**: Klik ganda (*double click*) file `index.html` tersebut. File akan otomatis terbuka di browser favorit Anda (Google Chrome, Mozilla Firefox, Microsoft Edge, Safari, dll).
- **Metode Live Server (Opsional)**: Jika menggunakan **VS Code**, Anda dapat klik kanan pada file `index.html` dan pilih **"Open with Live Server"**.

---

## 🎮 Kontrol Permainan

### Keyboard (PC / Laptop)

| Tombol Keyboard | Aksi / Fungsi |
| :--- | :--- |
| **Panah Kiri ($\leftarrow$)** | Geser balok ke kiri |
| **Panah Kanan ($\rightarrow$)** | Geser balok ke kanan |
| **Panah Bawah ($\downarrow$)** | *Soft Drop* (Mempercepat balok jatuh perlahan) |
| **Panah Atas ($\uparrow$) / Z** | Putar balok (*Rotate*) |
| **Spasi (Spacebar)** | *Hard Drop* / *SLAM* (Balok langsung jatuh ke dasar) |
| **Enter** | Jeda permainan (*Pause / Resume*) |

### Tombol Layar Sentuh (Mobile / HP)
- **DROP ($\downarrow$)**: Geser balok ke bawah.
- **ROT A ($\circlearrowright$)**: Memutar arah balok.
- **SLAM ($\Downarrow$)**: Menjatuhkan balok secara instan ke paling bawah.

---

## 📊 Sistem Skor & Level

1. **Perhitungan Skor**:
   - **1 Baris Cleared**: $40 \times \text{Level}$
   - **2 Baris Cleared**: $100 \times \text{Level}$
   - **3 Baris Cleared**: $300 \times \text{Level}$
   - **4 Baris Cleared (Tetris)**: $1200 \times \text{Level}$
   - **Soft Drop**: $+1$ poin per langkah.
   - **Hard Drop / SLAM**: $+2$ poin per baris jatuh.

2. **Kenaikan Level (Next Level)**:
   - Level awal dimulai dari **LVL 01**.
   - Setiap kali Anda berhasil membersihkan **10 baris (*LINES*)**, level akan naik **+1**.
   - Kecepatan jatuh balok bertambah cepat seiring tingginya level.

---

## 🛠️ Kustomisasi (Opsional)

Jika Anda ingin mengubah tampilan atau kecepatan awal, Anda dapat mengedit variabel berikut pada bagian JavaScript di dalam `index.html`:

- `COLS = 10` & `ROWS = 20`: Ukuran papan permainan.
- `dropInterval = 1000`: Kecepatan jatuh awal balok dalam milidetik ($1000\text{ ms} = 1\text{ detik}$).
- Variabel CSS `:root` pada bagian `<style>` untuk menyesuaikan skema warna amber dan kekuatan efek visual.

---

Selamat bermain! Jangan ragu untuk mengembangkan fitur tambahan seperti efek suara (BGM/SFX) atau tema warna retro lainnya. 🕹️

# AsjaiRobi-PBO2-UTS
Kode program di atas merupakan implementasi GUI aplikasi Buku Alamat menggunakan Java Swing. Berikut adalah penjelasan mengenai komponen penting yang terdapat dalam kode tersebut:

### Fitur Utama
1. **Tambah Data**:  
   Data nama, alamat, dan nomor telepon ditambahkan ke tabel menggunakan `jButton1ActionPerformed`. Data disimpan ke file CSV melalui metode `saveToCSV()`.

2. **Edit Data**:  
   Mengedit baris data yang dipilih di tabel menggunakan `jButton4ActionPerformed`. Setelah pengeditan selesai, data diperbarui dan disimpan kembali ke file CSV.

3. **Hapus Data**:  
   Menghapus baris data yang dipilih di tabel menggunakan `jButton5ActionPerformed`. Data dihapus dari model tabel dan file CSV diperbarui.

4. **Pencarian**:  
   Pencarian dilakukan berdasarkan nama, alamat, atau nomor telepon menggunakan `jButton3ActionPerformed`. Pencarian ini memanfaatkan fitur `TableRowSorter` untuk menyaring hasil.

5. **Validasi Input**:  
   - Nomor telepon hanya menerima input berupa angka dengan menggunakan `jTextField2KeyTyped`.
   - Semua kolom input harus diisi; jika tidak, akan muncul pesan peringatan menggunakan `JOptionPane`.

6. **Load dan Simpan Data CSV**:  
   - Metode `loadCSV()` membaca file `data.csv` dan memuatnya ke dalam tabel.
   - Jika file tidak ditemukan, metode ini akan membuat file kosong secara otomatis.
   - Metode `saveToCSV()` menyimpan semua data dari tabel ke file `data.csv`.

### Komponen GUI
- **Tabel (`jTable1`)**: Untuk menampilkan daftar alamat.
- **Text Field dan Text Area**: Untuk menginput nama, alamat, dan nomor telepon.
- **Button**: 
  - `Simpan` untuk menambah data baru.
  - `Edit` untuk memperbarui data yang dipilih.
  - `Hapus` untuk menghapus data.
  - `Cari` untuk mencari data berdasarkan kata kunci.

### Masukan atau Perbaikan
1. **Penanganan Eror**: 
   - Tambahkan notifikasi jika file `data.csv` gagal dibuat atau dibaca.
   - Berikan pesan yang lebih informatif jika pencarian tidak menemukan hasil.

2. **UI yang Lebih Responsif**: 
   - Tambahkan margin dan padding untuk tampilan yang lebih rapi.
   - Gunakan dialog konfirmasi sebelum menghapus data.

3. **Ekstensi Fitur**: 
   - Tambahkan fitur ekspor data ke format lain (contoh: PDF).
   - Sertakan validasi lebih lanjut untuk nomor telepon (format).

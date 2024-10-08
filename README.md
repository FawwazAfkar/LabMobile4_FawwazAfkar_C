# tokokita

Pertemuan 5 (Pertemuan 4 ada di README2.MD)

Nama : Fawwaz Afkar Muzakky

NIM : H1D022067

SHIFT Lama: B

Shift Baru: C

# Penjelasan
Penjelasan proses yang terjadi dalam aplikasi Flutter meliputi login, register, dan operasi CRUD (Create, Read, Update, Delete) pada produk

1. Login (login_page.dart):

   a. Pengguna memasukkan email dan password pada form login.
   b. Saat tombol "Login" ditekan, metode `_submit()` dipanggil.
   c. `LoginBloc.login()` dipanggil dengan email dan password yang dimasukkan.
   d. Jika login berhasil (kode 200):
      - Token dan UserID disimpan menggunakan `UserInfo().setToken()` dan `UserInfo().setUserID()`.
      - Pengguna diarahkan ke `ProdukPage`.
   e. Jika login gagal, pesan kesalahan ditampilkan menggunakan `WarningDialog`.

2. Registrasi (registrasi_page.dart):

   a. Pengguna mengisi form registrasi dengan nama, email, password, dan konfirmasi password.
   b. Saat tombol "Registrasi" ditekan, metode `_submit()` dipanggil.
   c. `RegistrasiBloc.registrasi()` dipanggil dengan data yang dimasukkan.
   d. Jika registrasi berhasil, `SuccessDialog` ditampilkan.
   e. Jika registrasi gagal, `WarningDialog` ditampilkan.

3. Menampilkan Daftar Produk (produk_page.dart):

   a. `ProdukPage` menggunakan `FutureBuilder` untuk memanggil `ProdukBloc.getProduks()`.
   b. Daftar produk ditampilkan menggunakan `ListView.builder`.
   c. Setiap item produk ditampilkan menggunakan `ItemProduk` widget.

4. Create Produk (produk_form.dart):

   a. Pengguna mengakses form tambah produk dari `ProdukPage`.
   b. Pengguna mengisi form dengan kode produk, nama produk, dan harga.
   c. Saat tombol "SIMPAN" ditekan, metode `simpan()` dipanggil.
   d. `ProdukBloc.addProduk()` dipanggil dengan data produk baru.
   e. Jika berhasil, pengguna diarahkan kembali ke `ProdukPage`.
   f. Jika gagal, `WarningDialog` ditampilkan.

5. Read Produk Detail (produk_detail.dart):

   a. Pengguna menekan item produk di `ProdukPage`.
   b. `ProdukDetail` ditampilkan dengan informasi produk yang dipilih.

6. Update Produk (produk_form.dart):

   a. Pengguna menekan tombol "EDIT" di `ProdukDetail`.
   b. Form produk ditampilkan dengan data produk yang ada.
   c. Pengguna mengubah data produk.
   d. Saat tombol "UBAH" ditekan, metode `ubah()` dipanggil.
   e. `ProdukBloc.updateProduk()` dipanggil dengan data produk yang diperbarui.
   f. Jika berhasil, pengguna diarahkan kembali ke `ProdukPage`.
   g. Jika gagal, `WarningDialog` ditampilkan.

7. Delete Produk (produk_detail.dart):

   a. Pengguna menekan tombol "DELETE" di `ProdukDetail`.
   b. Dialog konfirmasi ditampilkan.
   c. Jika pengguna mengonfirmasi, `ProdukBloc.deleteProduk()` dipanggil.
   d. Jika berhasil, pengguna diarahkan kembali ke `ProdukPage`.
   e. Jika gagal, `WarningDialog` ditampilkan.

8. Logout (produk_page.dart):

   a. Pengguna membuka drawer menu dan menekan "Logout".
   b. `LogoutBloc.logout()` dipanggil.
   c. Pengguna diarahkan kembali ke `LoginPage`.


# Screeenshot
![](img/screenshots/register.png)
![](img/screenshots/successreg.png)
![](img/screenshots/login.png)
![](img/screenshots/produkpage1.png)
![](img/screenshots/addprodukform.png)
![](img/screenshots/afteraddproduk.png)
![](img/screenshots/detailprodukss.png)
![](img/screenshots/editprodukss.png)
![](img/screenshots/aftereditss.png)
![](img/screenshots/beforedeleteaoc.png)
![](img/screenshots/deleteaoc.png)
![](img/screenshots/afterdelaoc.png)
![](img/screenshots/sidebar1.png)


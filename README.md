# Tugas-Basis-Data-P6

Apa itu SQL, DDL, DML, DCL, dan TCL?

Apa itu SQL?

SQL (Structured Query Language) adalah bahasa standar yang digunakan untuk mengelola dan mengolah data dalam sistem manajemen basis data relasional (RDBMS) seperti MySQL, PostgreSQL, dan Oracle.

SQL memiliki beberapa kategori perintah, di antaranya:

1. DDL (Data Definition Language)

Digunakan untuk mendefinisikan struktur database — membuat, mengubah, atau menghapus tabel dan objek database.

Contoh perintah:

CREATE TABLE pelanggan (
    id_pelanggan INT PRIMARY KEY,
    nama VARCHAR(50),
    alamat VARCHAR(100)
);

ALTER TABLE pelanggan ADD no_telp VARCHAR(15);

DROP TABLE pelanggan;

#DDL digunakan untuk mendefinisikan struktur database.

2. DML (Data Manipulation Language)

Digunakan untuk memanipulasi data di dalam tabel, seperti menambah, mengubah, menampilkan, atau menghapus data.

Contoh perintah:

INSERT INTO pelanggan VALUES (1, 'Andi', 'Bandung');
UPDATE pelanggan SET alamat = 'Jakarta' WHERE id_pelanggan = 1;
DELETE FROM pelanggan WHERE id_pelanggan = 1;
SELECT * FROM pelanggan;2

#DML digunakan untuk memasukkan dan mengubah data.

3. DCL (Data Control Language)

Digunakan untuk mengatur hak akses pengguna (user privilege) terhadap database.

Contoh perintah:

GRANT SELECT, INSERT ON pelanggan TO user1;
REVOKE INSERT ON pelanggan FROM user1;

#DCL digunakan untuk mengatur izin akses database.

4. TCL (Transaction Control Language)

Digunakan untuk mengatur transaksi dalam database, terutama untuk menjaga konsistensi data.

Contoh perintah:

BEGIN;
UPDATE pelanggan SET alamat='Bekasi' WHERE id_pelanggan=2;
COMMIT;   -- menyimpan perubahan
ROLLBACK; -- membatalkan perubahan

#TCL digunakan untuk mengontrol proses transaksi agar aman dan konsisten.

- Jenis SQL	Kepanjangan	Fungsi Utama	Contoh Perintah,

- DDL	Data Definition Language	Mengatur struktur database	CREATE, ALTER, DROP
  
- DML	Data Manipulation Language	Mengolah data di tabel	SELECT, INSERT, UPDATE, DELETE
  
- DCL	Data Control Language	Mengatur hak akses user	GRANT, REVOKE
  
- TCL	Transaction Control Language	Mengelola transaksi data	COMMIT, ROLLBACK

NAMA   :  RIDHA MUHAMMAD RIFQI

NIM    :  312210491

KELAS  :  TI.22.A.5

## DDL : Membuat Database dan Tabel

```

-- Membuat database
CREATE DATABASE ContohDB;

-- Menggunakan database
USE ContohDB;

-- Membuat tabel `Mahasiswa`
CREATE TABLE Mahasiswa (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    Nama VARCHAR(50) NOT NULL,
    Jurusan VARCHAR(50),
    Angkatan YEAR
);

-- Membuat tabel `MataKuliah`
CREATE TABLE MataKuliah (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    NamaMataKuliah VARCHAR(50) NOT NULL,
    SKS INT NOT NULL
);

-- Membuat tabel `Nilai`
CREATE TABLE Nilai (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    MahasiswaID INT NOT NULL,
    MataKuliahID INT NOT NULL,
    Nilai CHAR(2),
    FOREIGN KEY (MahasiswaID) REFERENCES Mahasiswa(ID),
    FOREIGN KEY (MataKuliahID) REFERENCES MataKuliah(ID)
);


```
## DML : Menambahkan Data ke Tabel
```

INSERT INTO Mahasiswa (Nama, Jurusan, Angkatan) VALUES
('Andi', 'Teknik Informatika', 2020),
('Budi', 'Sistem Informasi', 2021),
('Citra', 'Teknik Komputer', 2019),
('Dina', 'Teknik Informatika', 2022),
('Eko', 'Sistem Informasi', 2020);

```
## Menambahkan 5 record ke Tabel MataKuliah
```

INSERT INTO Nilai (MahasiswaID, MataKuliahID, Nilai) VALUES
(1, 1, 'A'),
(2, 2, 'B'),
(3, 3, 'A'),
(4, 4, 'B'),
(5, 5, 'C');

```
## Verifikasi Data
```

-- Lihat data dari tabel Mahasiswa
SELECT * FROM Mahasiswa;

-- Lihat data dari tabel MataKuliah
SELECT * FROM MataKuliah;

-- Lihat data dari tabel Nilai
SELECT * FROM Nilai;

```
## Output 

## Tabel Mahasiswa

![Screenshot 2024-12-09 085924](https://github.com/user-attachments/assets/931b9c30-aa11-4b9d-b270-a747abbf1bbf)

## Tabel MataKuliah

![Screenshot 2024-12-09 090024](https://github.com/user-attachments/assets/ede202b7-6bea-4926-b087-b7ea892c4827)

## Tabel Nilai

![Screenshot 2024-12-09 090116](https://github.com/user-attachments/assets/bcc74ec1-15ad-4915-827e-c3e00afccbf4)






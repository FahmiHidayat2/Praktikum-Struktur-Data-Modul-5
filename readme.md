# <h1 align="center">Laporan Praktikum Modul Tipe Data</h1>
<p align="center">Fahmi Hidayat</p>

## Dasar Teori

Struct merupakan sebuah fitur yang memungkinkan pengguna untuk mendefinisikan sebuah tipe data baru yang terdiri dari beberapa anggota yang berbeda. Setiap anggota ini dapat memiliki tipe data yang berbeda pula. Secara umum, struct digunakan untuk mengelompokkan data terkait menjadi satu unit yang lebih besar. Kata kunci struct memberi tahu kompiler bahwa template struktur sedang ditentukan, yang dapat digunakan untuk membuat variabel struktur. Bidang-bidang yang membentuk struktur disebut anggota atau elemen struktur. Semua elemen dalam suatu struktur secara logis berhubungan satu sama lain [1].

## Guided 

### 1. Guided 1

```C++
// Guided 1
#include <iostream>
using namespace std;

struct buku {
	string JudulBuku;
	string pengarang;
	string penerbit;
	int tebalHalaman;
	int hargaBuku;
};

int main(){
	
buku mybook, mybook2;

mybook.JudulBuku = "Harry Potter";
mybook.pengarang = "J.K Rowling";
mybook.penerbit = "Scholastic Press";
mybook.tebalHalaman = 870;
mybook.hargaBuku = 2000000;

mybook2.JudulBuku = "Kata";
mybook2.pengarang = "Tere Liye";
mybook2.penerbit = "Scholastic Press";
mybook2.tebalHalaman = 250;
mybook2.hargaBuku = 3500000;


cout << "=== Deskripsi Buku ===" << endl;
cout <<"Judul Buku: " << mybook.JudulBuku << endl;
cout <<"Nama Pengarang: " << mybook.pengarang << endl;
cout <<"Nama penerbit: " << mybook.penerbit << endl;
cout <<"Tebal Halaman: " << mybook.tebalHalaman << endl;
cout <<"Harga Buku: " << mybook.hargaBuku << endl;
cout << "" << endl;
cout <<"Judul Buku: " << mybook2.JudulBuku << endl;
cout <<"Nama Pengarang: " << mybook2.pengarang << endl;
cout <<"Nama penerbit: " << mybook2.penerbit << endl;
cout <<"Tebal Halaman: " << mybook2.tebalHalaman << endl;
cout <<"Harga Buku: " << mybook2.hargaBuku << endl;


return 0;

}
```

### 2 Guided 2
```c++
// Guided 2

#include <iostream>
#include <string>
using namespace std;

struct hewan {
    string Nama_hewan;
    string Jenis_kelamin;
    string cara_berkembangbiak;
    string alat_pernafasan;
    string tempat_hidup;
    bool karnivora;
};

struct hewanDarat {
    hewan info_hewan;
    int jumlah_kaki;
    bool menyusui;
    string suara;
};

struct hewanLaut {
    hewan info_hewan;
    string sirip;
    string pertahanan_diri;
};

int main() {
    hewanDarat hewan_darat1; // Renamed variable to hewan_darat1
    hewanLaut hewan_laut1;   // Renamed variable to hewan_laut1
    
    hewan_darat1.info_hewan.Nama_hewan = "Kucing Ireng";
    hewan_darat1.info_hewan.Jenis_kelamin = "betina";
    hewan_darat1.info_hewan.cara_berkembangbiak = "Vivipar / melahirkan";
    hewan_darat1.info_hewan.alat_pernafasan = "Paru - Paru";
    hewan_darat1.info_hewan.tempat_hidup = "Darat";
    hewan_darat1.info_hewan.karnivora = true;
    hewan_darat1.jumlah_kaki = 4;
    hewan_darat1.menyusui = true;
    hewan_darat1.suara = "meow";

    hewan_laut1.info_hewan.Nama_hewan = "Ikan Hiu";
    hewan_laut1.info_hewan.Jenis_kelamin = "jantan";
    hewan_laut1.info_hewan.cara_berkembangbiak = "Ovovivipar";
    hewan_laut1.info_hewan.alat_pernafasan = "Insang";
    hewan_laut1.info_hewan.tempat_hidup = "Laut";
    hewan_laut1.info_hewan.karnivora = true;
    hewan_laut1.sirip = "besar dan kuat";
    hewan_laut1.pertahanan_diri = "menggunakan gigi dan sirip";

    cout <<"=== HEWAN DARAT ===" << endl;
    cout <<"Nama Hewan: " << hewan_darat1.info_hewan.Nama_hewan << endl;
    cout <<"Jenis Kelamin: " << hewan_darat1.info_hewan.Jenis_kelamin << endl;
    cout <<"Cara Berkembangbiak: " << hewan_darat1.info_hewan.cara_berkembangbiak << endl;
    cout <<"Alat Pernafasan: " << hewan_darat1.info_hewan.alat_pernafasan << endl;
    cout <<"Tempat Hidup: " << hewan_darat1.info_hewan.tempat_hidup << endl;
    cout <<"Apakah Karnivora?: " << (hewan_darat1.info_hewan.karnivora ? "Ya" : "Tidak") << endl;
    cout <<"Jumlah Kaki: " << hewan_darat1.jumlah_kaki << endl;
    cout <<"Apakah Menyusui?: " << (hewan_darat1.menyusui ? "Ya" : "Tidak") << endl;
    cout <<"Suara: " << hewan_darat1.suara << endl;

    cout <<"\n=== HEWAN LAUT ===" << endl;
    cout <<"Nama Hewan: " << hewan_laut1.info_hewan.Nama_hewan << endl;
    cout <<"Jenis Kelamin: " << hewan_laut1.info_hewan.Jenis_kelamin << endl;
    cout <<"Cara Berkembangbiak: " << hewan_laut1.info_hewan.cara_berkembangbiak << endl;
    cout <<"Alat Pernafasan: " << hewan_laut1.info_hewan.alat_pernafasan << endl;
    cout <<"Tempat Hidup: " << hewan_laut1.info_hewan.tempat_hidup << endl;
    cout <<"Apakah Karnivora?: " << (hewan_laut1.info_hewan.karnivora ? "Ya" : "Tidak") << endl;
    cout <<"Bentuk Sirip: " << hewan_laut1.sirip << endl;
    cout <<"Pertahanan Diri: " << hewan_laut1.pertahanan_diri << endl;

    return 0;
}
```

## Unguided 

### 1. Modifikasi tugas guided pertama, sehingga setiap item yang terdapat pada sruct buku berupa array yang berukuran 5, isi dengan data kemudian tampilkan.
```C++
#include <iostream>
#include <string>
using namespace std;

struct buku {
    string JudulBuku[5];
    string pengarang[5];
    string penerbit[5];
    int tebalHalaman[5];
    int hargaBuku[5];
};

int main() {
    buku mybook;

    // Memasukkan data buku dari input pengguna
    for (int i = 0; i < 5; ++i) {
        cout << "Masukkan data untuk buku " << i + 1 << ":" << endl;
        cout << "Judul Buku: ";
        getline(cin, mybook.JudulBuku[i]);
        cout << "Nama Pengarang: ";
        getline(cin, mybook.pengarang[i]);
        cout << "Nama penerbit: ";
        getline(cin, mybook.penerbit[i]);
        cout << "Tebal Halaman: ";
        cin >> mybook.tebalHalaman[i];
        cout << "Harga Buku: ";
        cin >> mybook.hargaBuku[i];
        cin.ignore(); // Membersihkan buffer untuk input berikutnya
        cout << endl;
    }

    // Menampilkan data buku
    cout << "=== Deskripsi Buku ===" << endl;
    for (int i = 0; i < 5; ++i) {
        cout << "Buku " << i + 1 << ":" << endl;
        cout << "Judul Buku: " << mybook.JudulBuku[i] << endl;
        cout << "Nama Pengarang: " << mybook.pengarang[i] << endl;
        cout << "Nama penerbit: " << mybook.penerbit[i] << endl;
        cout << "Tebal Halaman: " << mybook.tebalHalaman[i] << endl;
        cout << "Harga Buku: " << mybook.hargaBuku[i] << endl;
        cout << endl;
    }
    
    cout << "" << endl;
    cout << "" << endl;

    return 0;
    
    
}

```
Program C++ di atas mendefinisikan sebuah struktur buku yang memiliki array untuk menyimpan data tentang lima buku, termasuk judul buku, nama pengarang, nama penerbit, tebal halaman, dan harga buku. Dalam fungsi main, pengguna diminta untuk memasukkan data untuk lima buku secara berturut-turut melalui input pengguna. Setiap iterasi dalam loop for mengambil input untuk judul buku, nama pengarang, nama penerbit, tebal halaman, dan harga buku. Setelah data dimasukkan, program kemudian menampilkan semua data buku yang telah dimasukkan oleh pengguna dalam format yang terstruktur. Ada penggunaan cin.ignore() untuk membersihkan buffer input sehingga input berikutnya tidak terganggu oleh karakter newline yang tersisa. Setelah selesai menampilkan semua data buku, program berakhir dengan mengembalikan nilai 0 dari fungsi main.
#### Output:
<img width="292" alt="image" src="https://github.com/FahmiHidayat2/Praktikum-Struktur-Data-Modul-5/assets/161399477/41ee8261-1824-439e-8b10-c44713816a8a">

## Kesimpulan
Dalam praktikum ini, kita telah mempelajari penggunaan struct di C++ untuk mengelompokkan data yang berhubungan menjadi satu unit yang lebih terstruktur. Implementasi struct memudahkan pengelolaan data yang kompleks seperti buku atau hewan dengan atribut yang beragam. Melalui latihan yang dilakukan, kita melihat bagaimana struct dapat digunakan untuk menyimpan dan menampilkan data secara efisien, serta bagaimana menggunakan array dalam struct untuk menyimpan banyak entri data. Praktikum ini memperjelas pentingnya struktur data dalam pemrograman untuk membuat kode lebih terorganisir dan mudah dikelola.

## Referensi
[1] S. N Mohanty, P. K. Tripathy, Data Structure and Algorithms Using C++ A Practical Implementation, USA: Wiley, 2021.

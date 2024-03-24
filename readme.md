# <h1 align="center">Laporan Praktikum Modul Tipe Data</h1>
<p align="center">Ardianto Hafidz Prabowo</p>

## Dasar Teori

### Tipe Data Primitif
Tipe data primitif merupakan tipe data yang hanya menyimpan satu nilai saja dalam satu variabelnya. Berikut adalah macam-macam dari tipe data primitif :

1.  Integer: merupakan tipe data dasar berupa bilangan numerik yang tidak mengandung pecahan desimal.
2.  Float: merupakan tipe data yang dapat dinyatakan dalam bentuk pangkat maupun desimal.
3.  Char: merupakan tipe data yang paling sering dipakai dalam komputasi. Tipe data char tidak memiliki batasan, dan dalam penggunaanya dengan menggunakan tanda kutip (‘).
4.  Boolean: merupakan tipe data pemrograman yang memiliki dua nilai, yaitu benar (true) atau salah (false). Tipe data ini paling sering digunakan untuk range yang memiliki dua buah nilai.

### Tipe Data Abstrak
Tipe data abstrak adalah kelas/ tipe untuk objek yang perilakunya ditentukan oleh satu set nilai dan satu set operasi. Definisi ADT hanya menyebutkan operasi apa yang akan dilakukan, tetapi tidak menyebutkan bagaimana operasi ini akan dilakukan. Itu tidak menentukan bagaimana mengatur data dalam memori dan algoritma apa yang akan digunakan untuk mengimplementasikan operasi. Ini disebut "abstraksi" karena memberikan tampilan yang tidak bergantung pada implementasi. Proses memberikan hanya informasi dasar dan menyembunyikan detailnya disebut abstraksi.

### Tipe Data
Tipe data koleksi adalah tipe data yang digunakan untuk menyimpan lebih dari satu nilai dalam satu variabel. Berikut adalah beberapa tipe data koleksi yang umum digunakan dalam pemrograman:

1.  Array: kumpulan elemen-elemen yang memiliki tipe data yang sama. Elemen-elemen tersebut diakses menggunakan indeks. Contoh: int arr[5] = {1, 2, 3, 4, 5};
2.  Vector: kumpulan elemen yang dapat berubah ukurannya. Elemen-elemen tersebut diakses menggunakan indeks. Contoh: vector arr = {1, 2, 3, 4, 5};
3.  Set: kumpulan elemen yang tidak memiliki urutan tertentu dan tidak memiliki elemen yang berulang. Contoh: set arr = {1, 2, 3};
4.  Map: kumpulan pasangan kunci-nilai. Contoh: map arr = {{"kunci1", "nilai1"}, {"kunci2", "nilai2"}};
5.  List: mirip dengan vector, tetapi elemen-elemennya diakses menggunakan indeks. Contoh: list arr = {1, 2, 3, 4, 5};
6.  Stack: kumpulan elemen yang memiliki prinsip Last In First Out (LIFO). Contoh: stack arr = {1, 2, 3};
7.  Queue: kumpulan elemen yang memiliki prinsip First In First Out (FIFO). Contoh: queue arr = {1, 2, 3};

## Guided 

### 1. Tipe Data Primitif

```C++
#include <iostream>
using namespace std;
// Main program
int main()
{
    char op;
    float num1, num2;
    // It allows user to enter operator i.e. +, -, *, /
    cin >> op;
    // It allow user to enter the operands
    cin >> num1 >> num2;
    // Switch statement begins
    switch (op)
    {
    // If user enter +
    case '+':
        cout << num1 + num2;
        break;
    // If user enter -
    case '-':
        cout << num1 - num2;
        break;
    // If user enter *
    case '*':
        cout << num1 * num2;
        break;
    // If user enter /
    case '/':
        cout << num1 / num2;
        break;
    // If the operator is other than +, -, * or /,
    // error message will display
    default:
        cout << "Error! operator is not correct";
    } // switch statement ends
    return 0;
}
```
Kode di atas digunakan untuk mencetak teks "ini adalah file code guided praktikan" ke layar menggunakan function cout untuk mengeksekusi nya.

### 2. Tipe Data Abstrak

```C++
#include <stdio.h>
//Struct
struct Mahasiswa
{
    const char *name;
    const char *address;
    int age;
};
int main()
{
    // menggunakan struct
    struct Mahasiswa mhs1, mhs2;
    // mengisi nilai ke struct
    mhs1.name = "Dian";
    mhs1.address = "Mataram";
    mhs1.age = 22;
    mhs2.name = "Bambang";
    mhs2.address = "Surabaya";
    mhs2.age = 23;
    // mencetak isi struct
    printf("## Mahasiswa 1 ##\n");
    printf("Nama: %s\n", mhs1.name);
    printf("Alamat: %s\n", mhs1.address);
    printf("Umur: %d\n", mhs1.age);
    printf("## Mahasiswa 2 ##\n");
    printf("Nama: %s\n", mhs2.name);
    printf("Alamat: %s\n", mhs2.address);
    printf("Umur: %d\n", mhs2.age);
    return 0;
}
```
Kode di atas digunakan untuk mencetak teks "ini adalah file code guided praktikan" ke layar menggunakan function cout untuk mengeksekusi nya.

### 3. Tipe Data Koleksi

```C++
#include <iostream>
using namespace std;
int main()
{
    //deklarasi dan inisialisasi array
    int nilai[5];
    nilai[0] = 23;
    nilai[1] = 50;
    nilai[2] = 34;
    nilai[3] = 78;
    nilai[4] = 90;
    //mencetak array
    cout << "Isi array pertama :" << nilai[0] << endl;
    cout << "Isi array kedua :" << nilai[1] << endl;
    cout << "Isi array ketiga :" << nilai[2] << endl;
    cout << "Isi array keempat :" << nilai[3] << endl;
    cout << "Isi array kelima :" << nilai[4] << endl;
    return 0;
}
```
Kode di atas digunakan untuk mencetak teks "ini adalah file code guided praktikan" ke layar menggunakan function cout untuk mengeksekusi nya.

## Unguided 

### 1. Buatlah program menggunakan tipe data primitif minimal dua fungsi dan bebas. Menampilkan program, jelaskan program tersebut dan ambil kesimpulan dari materi tipe data primitif!

```C++
#include <iostream>
// Fungsi untuk menjumlahkan dua bilangan
int add(int a, int b) {
    return a + b;
}
// Fungsi untuk mengurangkan dua bilangan
int subtract(int a, int b) {
    return a - b;
}
// Fungsi untuk mengalikan dua bilangan
int multiply(int a, int b) {
    return a * b;
}
// Fungsi untuk membagi dua bilangan
float divide(int a, int b) {
    if (b != 0) {
        return static_cast<float>(a) / b;
    } else {
        std::cerr << "Error: TIDAK BISA DBAGI 0" << std::endl;
        return 0;
    }
}
int main() {
    // Sampel angka atau data angka
    int num1 = 10;
    int num2 = 5;

    // Operasional dan menampilkan hasil
    std::cout << "Penjumlahan: " << add(num1, num2) << std::endl;
    std::cout << "Pengurangan: " << subtract(num1, num2) << std::endl;
    std::cout << "Perkalian: " << multiply(num1, num2) << std::endl;
    std::cout << "Pembagian: " << divide(num1, num2) << std::endl;
    return 0;
}
```
#### Output:
![Cuplikan layar 2024-03-11 144524](https://github.com/HafidzPrabowo/Praktikum-Struktur-Data-Assignment/assets/162563702/7738a1a7-7fad-4cf9-a7df-6e807c96826c)

Kodingan di atas terdapat empat fungsi yang melakukan operasi aritmatika dasar (penjumlahan, pengurangan, perkalian, dan pembagian) yang menggunakan tipe data primitif, yaitu int untuk bilangan bulat dan float untuk bilangan pecahan.

#### Full code Screenshot:
![Cuplikan layar 2024-03-11 144704](https://github.com/HafidzPrabowo/Praktikum-Struktur-Data-Assignment/assets/162563702/be863d18-af2f-4184-ba7e-d543feec2355)

#### Kesimpulan:
Tipe data int digunakan untuk menyimpan bilangan bulat tanpa desimal. Kemudian tipe data float digunakan untuk menyimpan bilangan pecahan. Kemudian pemakaian tipe data primitif memungkinkan penyimpanan data secara efisien dalam memori komputer. Lalu operasi aritmatika dasar seperti penjumlahan, pengurangan, perkalian, dan pembagian dapat dilakukan dengan menggunakan tipe data primitif.

### 2. Jelaskan fungsi dari class dan struct secara detail dan berikan contoh programnya

Class dan struct dalam C++ memiliki fungsi yang mirip, yaitu untuk mendefinisikan tipe data baru yang dapat menggabungkan data dan fungsi (metode) yang beroperasi pada data tersebut. Class sendiri adalah blueprint untuk objek yang mendefinisikan struktur data untuk objek dan fungsi untuk mengoperasikannya. Class dapat menggabungkan data dan fungsi yang terkait ke dalam satu unit. Ini memungkinkan untuk membuat objek yang memiliki sifat dan perilaku tertentu. Di dalam class, variabel-variabel (disebut sebagai anggota atau atribut) dan fungsi-fungsi (disebut sebagai metode atau fungsi anggota) dapat didefinisikan.

Sedangkan struct adalah tipe data yang memungkinkan untuk menggabungkan berbagai jenis data yang berbeda dalam satu unit. Struct digunakan untuk menyimpan sekumpulan variabel yang mungkin memiliki tipe data yang berbeda. Ini mirip dengan class, tetapi secara default anggota-anggotanya bersifat publik (bisa diakses langsung dari luar struct) dan tidak dapat memiliki metode.

### Class
```C++
#include <iostream>
using namespace std;

// Mendefinisikan class
class Mobil {
public:
    string merek;
    string model;
    int tahun;

    void info() {
        cout << "Merek: " << merek << endl;
        cout << "Model: " << model << endl;
        cout << "Tahun: " << tahun << endl;
    }
};

int main() {
    // Membuat objek dari class Mobil
    Mobil mobil1;
    mobil1.merek = "Tayota";
    mobil1.model = "LightMC";
    mobil1.tahun = 2050;
    // Memanggil metode info() dari objek mobil1
    mobil1.info();

    return 0;
}
```
#### Output:
![Cuplikan layar 2024-03-11 151724](https://github.com/HafidzPrabowo/Praktikum-Struktur-Data-Assignment/assets/162563702/72223828-2ed5-4e91-8fa2-27f5f4b1ab04)

Dalam program di atas, sebuah class Mobil didefinisikan dengan atribut merek, model, dan tahun, serta sebuah metode info(). Objek mobil1 dibuat dari class Mobil dan atribut-atributnya diisi dengan nilai tertentu. Metode info() dipanggil pada objek mobil1 untuk mencetak informasi tentang mobil tersebut

#### Full code Screenshot:
![Cuplikan layar 2024-03-11 151849](https://github.com/HafidzPrabowo/Praktikum-Struktur-Data-Assignment/assets/162563702/195e9827-4b00-4a0a-9096-e52fec2c8a44)

### Struct
```C++
#include <iostream>
using namespace std;

// Mendefinisikan struct
struct Mahasiswa {
    string nama;
    int umur;
    float ipk;
};

int main() {
    // Mendeklarasikan variabel bertipe struct Mahasiswa
    Mahasiswa mhs1;

    // Mengisi nilai ke dalam variabel
    mhs1.nama = "Bowo";
    mhs1.umur = 19;
    mhs1.ipk = 3.99;

    // Mencetak nilai variabel
    cout << "Nama: " << mhs1.nama << endl;
    cout << "Umur: " << mhs1.umur << endl;
    cout << "IPK: " << mhs1.ipk << endl;

    return 0;
}
```
#### Output:
![Cuplikan layar 2024-03-11 160731](https://github.com/HafidzPrabowo/Praktikum-Struktur-Data-Assignment/assets/162563702/12cb7cfe-58d3-4640-989c-811cede07e82)

Dalam contoh program di atas, sebuah struct Mahasiswa didefinisikan dengan tiga anggota: nama, umur, dan ipk. Variabel mhs1 dideklarasikan dengan tipe struct Mahasiswa, kemudian nilai-nilai untuk anggota-anggotanya diisi. Nilai-nilai dari variabel mhs1 dicetak untuk ditampilkan.

#### Full code Screenshot:
![Cuplikan layar 2024-03-11 152821](https://github.com/HafidzPrabowo/Praktikum-Struktur-Data-Assignment/assets/162563702/4c511686-5d4f-4ad3-81d5-faa90a87d159)

### 3. Buat dan jelaskan program menggunakan fungsi map dan jelaskan perbedaan dari array dengan map

Perbedaan antara array dan map:

#### 1. Tipe Data yang Disimpan:
- Array: Menyimpan elemen-elemen dengan tipe data yang sama.
- Map: Menyimpan pasangan key-value, di mana key dan value dapat memiliki tipe data yang berbeda.

#### 2. Akses Data:
- Array: Elemen-elemen diakses menggunakan indeks numerik.
- Map: Data diakses menggunakan key-nya.

#### 3. Ukuran dan Penambahan Elemen:
- Array: Ukuran array biasanya tetap, dan penambahan elemen baru memerlukan pemindahan data jika ukuran array penuh.
- Map: Dinamis dalam ukuran dan tidak memerlukan pergeseran data saat menambahkan atau menghapus elemen.

#### 4. *Kemampuan Pencarian*:
- Array: Pencarian elemen biasanya dilakukan secara berurutan atau menggunakan teknik pencarian seperti binary search jika array terurut.
- Map: Pencarian menggunakan struktur data hash table, yang membuatnya memiliki waktu pencarian konstan (O(1)) dalam kasus rata-rata.

Pemilihan antara array dan map tergantung pada kebutuhan program dan jenis operasi yang akan dilakukan. Jika data yang disimpan membutuhkan hubungan key-value atau jika efisiensi pencarian dan penambahan data penting, map seringkali menjadi pilihan yang lebih baik.

```C++
#include <iostream>
#include <map>

int main() {
    // Membuat map yang menyimpan pasangan key-value berupa nama dan umur
    std::map<std::string, int> umur;

    // Menambahkan beberapa data ke dalam map
    umur["Alpha"] = 30;
    umur["Beta"] = 25;
    umur["Chasya"] = 35;

    // Mengakses nilai umur berdasarkan nama
    std::cout << "Umur Alpha: " << umur["Alpha"] << std::endl;

    // Menggunakan iterator untuk mengakses semua data dalam map
    std::cout << "Data umur:\n";
    for (auto it = umur.begin(); it != umur.end(); ++it) {
        std::cout << it->first << ": " << it->second << std::endl;
    }

    return 0;
}
```
#### Output:
![Cuplikan layar 2024-03-11 154854](https://github.com/HafidzPrabowo/Praktikum-Struktur-Data-Assignment/assets/162563702/3bc8833e-002f-4de0-8a78-f6b858a78b1e)

Program C++ di atas menggunakan fungsi map untuk membuat dan mengelola map yang menyimpan pasangan key-value berupa nama dan umur. Program ini menunjukkan cara menambahkan data ke dalam map, mengakses nilai umur berdasarkan nama, dan menggunakan iterator untuk mengakses semua data dalam map. Kemudian, program mencetak nilai umur untuk nama "Alpha" dan mencetak semua pasangan key-value dalam map. Program ini mengilustrasikan cara menggunakan map dalam C++ untuk menyimpan dan mengelola data dengan key dan value yang berbeda, serta cara mengakses dan mengiterasi melalui data dalam map.

#### Full code Screenshot:
![Cuplikan layar 2024-03-11 155007](https://github.com/HafidzPrabowo/Praktikum-Struktur-Data-Assignment/assets/162563702/d87f0739-b7bf-4e36-b3e4-0ba58025bda5)

## Kesimpulan
Mengenali tipe data memiliki beberapa manfaat, seperti memahami jenis data yang akan diproses, memastikan efisiensi penggunaan memori, dan memudahkan dalam pemrograman. Misalnya, jika kita menggunakan tipe data integer, maka program akan menganggap data tersebut sebagai bilangan bulat. Tipe data juga mempengaruhi efisiensi penggunaan memori. Misalnya, tipe data double membutuhkan lebih banyak memori dibandingkan dengan tipe data float. Oleh karena itu, jika kita tidak perlu menggunakan tipe data double, maka kita sebaiknya menggunakan tipe data float untuk menghemat memori. Mengenali tipe data juga memudahkan dalam pemrograman. Misalnya, jika kita tahu bahwa data yang akan diproses adalah bilangan bulat, maka kita bisa langsung menggunakan tipe data integer tanpa perlu memikirkan jenis data lainnya.

## Referensi
[1]Zein, A., Eriana, E.S., Algoritma Dan Struktur Data, Banten: Unpam Press; 2022.
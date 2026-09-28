# Laporan Praktikum Struktur Data - Modul 1

**Nama:** [muh rifqi irwanto]  
**NIM:** [109082500016]  
**Kelas:** [S1IF-13-01]  


## I. Dasar Teori

Bahasa C++ diciptakan oleh Bjarne Stroustrup di AT&T Bell Laboratories pada awal tahun 1980-an [3]. Bahasa ini dikembangkan dari bahasa C yang ditambahi fasilitas kelas (*class*), sehingga pada mulanya dikenal sebagai *"C with classes"*, sebelum akhirnya disempurnakan dengan penambahan pembebanlebihan operator (*operator overloading*) serta fungsi hingga dinamai C++ [3]. Pada praktikum ini, C++ digunakan sebagai bahasa pemrograman dasar untuk memahami konsep-konsep logika dan struktur pemrograman sebelum melangkah ke materi Struktur Data.

### A. Struktur Program dan Identifier
Secara umum, struktur program C++ terdiri dari pemanggilan pustaka (`#include`), pendefinisian konstanta, pendefinisian tipe data bentukan, deklarasi variabel, deklarasi fungsi/prosedur, serta fungsi utama `main()` [3]. Setiap instruksi atau pernyataan (*statement*) dalam C++ wajib diakhiri dengan tanda titik koma (`;`).

1. **Pustaka (*Header File*):**  
   Fungsi input-output seperti `cin` dan `cout` didefinisikan di dalam pustaka `<iostream>`, sehingga program harus menyertakan perintah `#include <iostream>` di bagian atas kode agar fungsi tersebut dapat digunakan [3].

2. **Pengidentifikasi (*Identifier*):**  
   *Identifier* merupakan nama yang diberikan untuk variabel, konstanta, fungsi, atau objek lainnya. Aturan penulisan *identifier* mencakup:
   * Harus diawali dengan huruf atau garis bawah (`_`).
   * Tidak boleh mengandung spasi.
   * Tidak boleh menggunakan operator aritmatika.
   * Bersifat sensitif terhadap huruf besar dan kecil (*case-sensitive*), sehingga variabel `panjang` dan `Panjang` dianggap dua variabel yang berbeda [3].

3. **Fungsi `main()`:**  
   Fungsi `main()` merupakan titik awal (*entry point*) eksekusi program C++. Seluruh blok kode program utama dituliskan di dalam kurung kurawal `{ }` dan umumnya diakhiri dengan perintah `return 0;` sebagai tanda bahwa program berjalan dengan normal [3].

---

### B. Tipe Data, Variabel, dan Konstanta

1. **Tipe Data Dasar:**  
   Tipe data menentukan jenis nilai yang dapat disimpan. Tipe data dasar yang umum digunakan meliputi:
   * `int` untuk bilangan bulat.
   * `float` dan `double` untuk bilangan real/pecahan (masing-masing presisi tunggal dan ganda).
   * `char` untuk menyimpan satu karakter [3].

2. **Variabel:**  
   Variabel digunakan sebagai wadah untuk menyimpan nilai data yang nilainya dapat berubah selama program mengeksekusi perintah. Deklarasinya ditulis dengan format `tipe_data nama_variabel;` dan dapat langsung diinisialisasi nilai awatnya, contohnya `int x = 20;` [3].

3. **Konstanta:**  
   Konstanta digunakan untuk menyimpan nilai yang bersifat tetap dan tidak dapat diubah selama program berjalan. Deklarasinya dilakukan dengan menambahkan kata kunci `const` di depan tipe data, misalnya `const float phi = 3.14;` [3].

---

### C. Masukan dan Keluaran (Input / Output)

Operasi input dan output standar pada C++ diakomodasi melalui pustaka `iostream` menggunakan objek `cin` dan `cout` [3].

1. **Keluaran dengan `cout`:**  
   `cout` digunakan untuk menampilkan data (teks maupun nilai variabel) ke layar monitor dengan bantuan operator *insertion* (`<<`). Untuk membuat baris baru, dapat digunakan perintah `endl` atau karakter escape `\n` [3].

2. **Masukan dengan `cin`:**  
   `cin` digunakan untuk menerima masukan data dari keyboard menggunakan operator *extraction* (`>>`). Nilai yang dimasukkan akan langsung disimpan ke dalam variabel tujuan tanpa membutuhkan penentu format (*format specifier*) [3].

3. **Karakter Escape (*Escape Sequence*):**  
   Merupakan kombinasi karakter khusus yang diawali dengan tanda garis miring terbalik (`\`), seperti `\n` untuk membuat baris baru dan `\t` untuk memberi jarak tabulasi [3].

---

### D. Operator

Operator adalah simbol khusus yang digunakan untuk melakukan operasi atau manipulasi data [3].

1. **Operator Aritmatika:**  
   Digunakan untuk operasi matematis, meliputi penjumlahan (`+`), pengurangan (`-`), perkalian (`*`), pembagian (`/`), dan sisa bagi/modulus (`%`) [3]. Tanda kurung `()` dapat digunakan untuk memprioritaskan urutan perhitungan. Pada pembagian dua bilangan bulat (*integer*), hasil pembagian juga berupa bilangan bulat sehingga bagian desimalnya akan dibuang.

2. **Operator Relasi dan Logika:**  
   Operator relasi (`==`, `!=`, `<`, `<=`, `>`, `>=`) digunakan untuk membandingkan dua nilai [3]. Sedangkan operator logika (`&&` [AND], `||` [OR], `!` [NOT]) digunakan untuk mengombinasikan atau membalikkan kondisi logika [3].

3. **Operator Increment dan Decrement:**  
   Operator `++` digunakan untuk menambah nilai variabel sebesar 1 (*increment*), sedangkan operator `--` digunakan untuk mengurangi nilai variabel sebesar 1 (*decrement*) [3].

---

### E. Kondisional dan Perulangan

1. **Struktur Kondisional (`if`, `if-else`, `switch`):**  
   * Pernyataan `if` mengeksekusi blok kode hanya jika kondisi bernilai benar (*true*), sedangkan `else` menyediakan alternatif blok kode jika kondisi bernilai salah (*false*) [3].
   * Pernyataan `switch` digunakan untuk percabangan dengan banyak opsi nilai konstan. Setiap cabang `case` biasanya diakhiri dengan instruksi `break`, dan blok `default` akan dieksekusi jika tidak ada nilai `case` yang cocok [3].

2. **Struktur Perulangan (`for`, `while`, `do-while`):**  
   Struktur perulangan digunakan untuk menjalankan instruksi secara berulang selama kondisi terpenuhi, dan setiap perulangan harus memiliki kondisi berhenti (*exit condition*) [3].
   * Perulangan `for` sangat cocok digunakan jika jumlah iterasi sudah diketahui secara pasti sejak awal [3].
   * Perulangan `while` melakukan pengecekan kondisi di awal sebelum eksekusi blok kode dilakukan [3].
   * Perulangan `do-while` melakukan pengecekan kondisi di akhir perulangan, sehingga blok kode dipastikan berjalan sekurang-kurangnya satu kali [3].
  
   ## II. Unguided / Tugas Praktikum

### Unguided 1: Operasi Aritmatika Dasar Dua Bilangan Float

#### A. Soal
> Buatlah program yang menerima input-an dua buah bilangan betipe float, kemudian memberikan keluaran-an hasil penjumlahan, pengurangan, perkalian, dan pembagian dari dua bilangan tersebut.

#### B. Kode Program
```cpp
#include <iostream>
using namespace std;

int main() {
    float bil1, bil2;
    float tambah, kurang, kali, bagi;

    cout << "Masukkan bilangan pertama : ";
    cin >> bil1;
    cout << "Masukkan bilangan kedua   : ";
    cin >> bil2;

    tambah = bil1 + bil2;
    kurang = bil1 - bil2;
    kali = bil1 * bil2;
    bagi = bil1 / bil2;

    cout << "\nHasil Penjumlahan : " << tambah << endl;
    cout << "Hasil Pengurangan : " << kurang << endl;
    cout << "Hasil Perkalian   : " << kali << endl;
    cout << "Hasil Pembagian   : " << bagi << endl;

    return 0;
}
```

#### C. Output / Screenshot Hasil Jalan
<img width="665" height="207" alt="Screenshot 2026-09-28 171921" src="https://github.com/user-attachments/assets/06860984-31d7-4783-a4f4-0ae8e3f50891" />
#### D. Penjelasan Kode

Program ini dibuat untuk menghitung empat operasi dasar dari dua bilangan yang diinputkan pengguna. Pertama, dideklarasikan dua variabel bertipe `float` (`bil1` dan `bil2`) untuk menyimpan bilangan, serta empat variabel `float` lain untuk menyimpan hasil. Bilangan dibaca dengan `cin`, lalu dihitung memakai operator aritmatika `+`, `-`, dan `*`, kemudian hasilnya ditampilkan dengan `cout`.

Untuk Pembagian, program memeriksa dulu dengan `if` apakah `bil2` tidak sama dengan 0. Kalau tidak nol, Pembagian...


#### A. Soal nomor 2
> Buatlah sebuah program yang menerima masukan angka dan mengeluarkan keluaran nilai angka tersebut dalam bentuk tulisan. Angka yang akan di-input-kan user adalah bilangan bulat positif mulai dari 0 sd 100. Contoh: 79 : tujuh puluh sembilan

#### B. Kode Program
```cpp
#include <iostream>
using namespace std;

int main() {
    int angka, puluhan, satuan;

    cout << "Masukkan angka (0 - 100): ";
    cin >> angka;

    if (angka < 0 || angka > 100) {
        cout << "Angka harus berada di antara 0 sampai 100!" << endl;
        return 0;
    }
    cout << angka << " : ";
    if (angka == 0) {
        cout << "nol";
    } else if (angka == 100) {
        cout << "seratus";
    } else if (angka == 10) {
        cout << "sepuluh";
    } else if (angka == 11) {
        cout << "sebelas";
    } else if (angka > 11 && angka < 20) {
        // angka belasan (12 sampai 19)
        satuan = angka % 10;
        switch (satuan) {
            case 2: cout << "dua"; break;
            case 3: cout << "tiga"; break;
            case 4: cout << "empat"; break;
            case 5: cout << "lima"; break;
            case 6: cout << "enam"; break;
            case 7: cout << "tujuh"; break;
            case 8: cout << "delapan"; break;
            case 9: cout << "sembilan"; break;
        }
        cout << " belas";
    } else {
        // angka 1-9 dan 20-99
        puluhan = angka / 10;
        satuan = angka % 10;
        if (puluhan > 0) {
            switch (puluhan) {
                case 2: cout << "dua"; break;
                case 3: cout << "tiga"; break;
                case 4: cout << "empat"; break;
                case 5: cout << "lima"; break;
                case 6: cout << "enam"; break;
                case 7: cout << "tujuh"; break;
                case 8: cout << "delapan"; break;
                case 9: cout << "sembilan"; break;
            }
            cout << " puluh";
        }
        if (satuan > 0) {
            if (puluhan > 0) {
                cout << " ";
            }
            switch (satuan) {
                case 1: cout << "satu"; break;
                case 2: cout << "dua"; break;
                case 3: cout << "tiga"; break;
                case 4: cout << "empat"; break;
                case 5: cout << "lima"; break;
                case 6: cout << "enam"; break;
                case 7: cout << "tujuh"; break;
                case 8: cout << "delapan"; break;
                case 9: cout << "sembilan"; break;
            }
        }
    }

    cout << endl;
    return 0;
}
```
#### C. Output / Screenshot Hasil Jalan
<img width="766" height="98" alt="Screenshot 2026-09-28 172039" src="https://github.com/user-attachments/assets/9d2d4e42-be43-400d-86de-6a0b9acaa809" />
#### D. Penjelasan Kode

Program ini mengubah angka 0 sampai 100 menjadi tulisan bahasa Indonesia. Setelah angka dibaca dengan cin, program memeriksa dulu apakah angkanya berada di rentang 0 sampai 100. Jika di luar rentang, program yang menampilkan pesan peringatan lalu berhenti.

Setelah itu, angka dibagi menjadi beberapa kondisi pemakaian if - else if. Angka yang punya penulisan khusus ditangani sendiri, yaitu 0 (nol), 10 (sepuluh), 11 (sebelas), dan 100 (seratus). Untuk angka 12 sampai 19, program mengambil digit satuannya dengan operator %, menuliskan nama angkanya lewat switch, lalu menambahkan kata "belas".

#### A. Soal nomor 3
> Buatlah program yang dapat memberikan input dan output sbb. (Gambar 1.25 Cermin)
#### B. Kode Program
```cpp
#include <iostream>
using namespace std;

int main() {
    int n;

    cout << "input: ";
    cin >> n;
    cout << "output:" << endl;

    for (int i = n; i >= 0; i--) {
        // spasi di depan supaya bentuknya rata tengah
        for (int s = 0; s < n - i; s++) {
            cout << " ";
        }

        // angka menurun dari i sampai 1
        for (int j = i; j >= 1; j--) {
            cout << j;
        }

        cout << "*";

        // angka menaik dari 1 sampai i
        for (int j = 1; j <= i; j++) {
            cout << j;
        }

        cout << endl;
    }

    return 0;
}
```
#### C. Output / Screenshot Hasil Jalan
<img width="688" height="215" alt="Screenshot 2026-09-28 172118" src="https://github.com/user-attachments/assets/4eb0c6eb-5fe0-43c7-8f1e-b60ad1dd4471" />
#### D. Penjelasan Kode
Program ini membuat pola "cermin" dari angka yang diinputkan. Kalau input-nya 3, baris pertama berisi 321*123, baris kedua 21*12, baris ketiga 1*1, dan baris terakhir saja *, dengan posisi yang rata tengah seperti pada gambar soal.

#### KESIMPULAN

Berdasarkan praktikum Modul 1 yang telah dilakukan, dapat disimpulkan bahwa:
1. Pemahaman struktur program C++ serta penggunaan alur I/O (`cin` dan `cout`) merupakan dasar utama dalam membangun sebuah program.
2. Tipe data `float` dan operator aritmatika terbukti efektif digunakan untuk menyelesaikan operasi perhitungan matematika dua bilangan.
3. Struktur keputusan `if-else` dan `switch` bersama operator aritmatika `/` dan `%` dapat dikombinasikan untuk memproses logika konversi angka menjadi teks.
4. Perulangan `for` mempermudah eksekusi instruksi yang berulang, seperti dalam pembuatan susunan pola angka.
5. Penguasaan terhadap sintaks dan logika dasar C++ ini menjadi modal penting sebelum mengimplementasikan struktur data yang lebih kompleks.

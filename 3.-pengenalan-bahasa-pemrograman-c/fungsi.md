# Fungsi

## 1. Penjelasan Fungsi

Fungsi merupakan kumpulan perintah yang digabung menjadi satu dan bisa dipanggil bersamaan

## 2. Cara Menggunakan Fungsi

### 2.1 Fungsi Sederhana

Berikut contoh pembuatan fungsi sederhana bernama `HitungLuasPersegiPanjang`. Setelah fungsi tersebut dibuat, maka bisa dijalankan berkali - kali

```csharp
// Program.cs

using System;

namespace HelloCSharp
{
  class Program
  {
    static void Main(string[] args)
    {
      // memanggil fungsi
      HitungLuasPersegiPanjang();
    }

    // membuat fungsi untuk menghitung luas persegi panjang
    static void HitungLuasPersegiPanjang()
    {
      int panjang = 5;
      int lebar = 6;
      int luas = panjang * lebar;
      Console.WriteLine(luas);
    }
  }
}
```

### 2.2 Fungsi dengan Parameter

Agar kita dapat mengubah nilai dari `panjang` dan `lebar` pada fungsi `HitungLuasPersegiPanjang`, maka kita dapat menggunakan parameter

```csharp
// Program.cs

using System;

namespace HelloCSharp
{
  class Program
  {
    static void Main(string[] args)
    {
      // memanggil fungsi dengan menginputkan nilai panjang dan lebar
      HitungLuasPersegiPanjang(5, 6);
      HitungLuasPersegiPanjang(10, 5);
      HitungLuasPersegiPanjang(15, 8);
    }

    // menambah parameter panjang dan lebar
    static void HitungLuasPersegiPanjang(int panjang, int lebar)
    {
      int luas = panjang * lebar;
      Console.WriteLine(luas);
    }
  }
}
```

### 2.3 Fungsi yang Mengembalikan Nilai

Agar nilai dari perhitungan luas persegi panjang dapat diolah kembali, kita dapat mengembalikan nilai dari fungsi `HitungLuasPersegiPanjang` menggunakan perintah `return` dan mengubah kata kunci `void` menjadi `int` mengikuti tipe data dari nilai yang dikembalikan

```csharp
// Program.cs

using System;

namespace HelloCSharp
{
  class Program
  {
    static void Main(string[] args)
    {
      // nilai yang dikembalikan dapat diolah kembali
      int hasil = HitungLuasPersegiPanjang(5, 6) + 30;
      Console.WriteLine(hasil); // output : 60
    }

    // mengembalikan nilai luas persegi panjang
    static int HitungLuasPersegiPanjang(int panjang, int lebar)
    {
      int luas = panjang * lebar;
      return luas;
    }
  }
}
```


# Pengenalan C\#

![c\#](../.gitbook/assets/cSharp.png)

## 1. Penjelasan C Sharp

**C\#** \(dibaca c sharp\) merupakan bahasa pemrograman berbasis objek \(OOP\) yang dikembangkan oleh microsoft sebagai bahasa pemrograman utama dalam lingkungan .NET framework, maka dari itu C\# membutuhkan .NET framework agar dapat dicompile

## 2. Instalasi C Sharp

Kita membutuhkan `.net core sdk` untuk mulai mengembangkan aplikasi berbasis C\#, silahkan unduh `.net core sdk` melalui link berikut :

[https://dotnet.microsoft.com/download](https://dotnet.microsoft.com/download)

## 3. Hello World dengan C Sharp

### 3.1 Membuat Folder Project

Pertama, silahkan buat folder baru, misalnya `HelloCSharp`, folder ini nantinya akan digunakan sebagai tempat project C\# kita

### 3.2 Membuat Project C Sharp Baru

Gunakan perintah berikut untuk membuat project C\# baru, jangan lupa untuk masuk ke folder yang tadi sudah dibuat terlebih dahulu

```bash
dotnet new console
```

Setelah perintah diatas dijalankan, maka `dotnet` akan membuat file baru bernama `Program.cs`, file ini merupakan file utama yang akan kita gunakan untuk melakukan pengembangan aplikasi

### 3.3 Menampilkan Pesan

Kita dapat menggunakan perintah `Console.WriteLine()`Untuk menampilkan pesan ke layar, silahkan ketikkan kode berikut ke `Program.cs`

```csharp
// Program.cs

using System;

namespace HelloCSharp
{
  class Program
  {
    static void Main(string[] args)
    {
      // Menampilkan pesan hello world
      Console.WriteLine("Hello World!");
    }
  }
}
```

### 3.4 Menjalankan Program

Untuk menjalankan program yang sudah kita buat, kita dapat menggunakan perintah `dotnet run`

```bash
dotnet run
```


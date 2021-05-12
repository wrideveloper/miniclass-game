# Dasar OOP Pada C\#

## 1. Penjelasan OOP

Object Oriented Programming \(OOP\) merupakan suatu paradigma atau konsep pemrograman yang berfokus pada pembuatan objek yang saling bekerjasama untuk memecahkan masalah

### 1.1 Penjelasan Object

Object merupakan seluruh hal yang bisa kita lihat dan deskripsikan, misalnya :

* Laptop
* Mobil
* Manusia
* Kucing
* Anjing

### 1.2 Penjelasan Attribute

Attribute merupakan hal yang dimiliki oleh suatu object, misalnya, mobil memiliki :

* Merk
* Warna
* Kecepatan
* Jumlah kursi
* Dll

### 1.3 Penjelasan Method

Method merupakan hal yang dapat dilakukan oleh suatu object, misalnya, mobil dapat melakukan :

* Maju
* Mundur
* Menambah kecepatan
* Mengurangi kecepatan
* Berbelok
* Dll

## 2. Penerapan OOP Pada C Sharp

### 2.1 Membuat Object

#### 2.1.1 Membuat Class

Sebelum membuat object, kita perlu membuat class terlebih dahulu, class merupakan suatu template yang nantinya dapat digunakan untuk membuat banyak object

```csharp
// Hero.cs

using System;

namespace AdventureGame
{
  class Hero
  {

  }
}
```

#### 2.1.2 Membuat Object

Untuk membuat object, kita dapat membuat variable baru menggunakan class `Hero` yang tadi sudah kita buat

```csharp
// Program.cs

using System;

namespace AdventureGame
{
  class Program
  {
    static void Main(string[] args)
    {
      // Membuat objek Hero baru bernama hero1
      Hero hero1 = new Hero();
    }
  }
}
```

### 2.2 Membuat Attribute

#### 2.2.1 Menambahkan Attribute

Untuk membuat attribute pada suatu objek, kita perlu menambahkan variable baru pada class `Hero`

```csharp
// Hero.cs

using System;

namespace AdventureGame
{
  class Hero
  {
    // menambahkan attribute name
    public String name;
    // menambahkan attribute health
    public int health;
  }
}
```

#### 2.2.2 Mengisi Nilai Attribute

Setelah membuat attribute pada class `Hero`, kita dapat mengisi nilainya pada objek `hero1` yang sudah kita buat

```csharp
// Program.cs

using System;

namespace AdventureGame
{
  class Program
  {
    static void Main(string[] args)
    {
      Hero hero1 = new Hero();

      // mengisi nilai attribute name
      hero1.name = "star platinum";
      // mengisi nilai attribute health
      hero1.health = 100;
    }
  }
}
```

### 2.3 Membuat Method

#### 2.3.1 Menambahkan Method

Untuk membuat method pada suatu objek, kita perlu menambahkannya pada class

```csharp
// Hero.cs

using System;

namespace AdventureGame
{
  class Hero
  {
    public String name;
    public int health;

    // method untuk terkena damage
    public void GetDamage() {
      this.health -= 30;
    }

    // method untuk menampilkan informasi hero
    public void ShowInfo() {
      Console.WriteLine("name : " + this.name);
      Console.WriteLine("health : " + this.health);
    }
  }
}
```

#### 2.3.2 Menggunakan Method

Setelah menambahkan method pada class `Hero`, kita dapat memanggilnya melalui objek `hero1` yang sudah dibuat

```csharp
// Program.cs

using System;

namespace AdventureGame
{
  class Program
  {
    static void Main(string[] args)
    {
      Hero hero1 = new Hero();

      hero1.name = "star platinum";
      hero1.health = 100;

      // hero terkena damage
      hero1.GetDamage();
      // menampilkan informasi hero
      hero1.ShowInfo();
    }
  }
}
```


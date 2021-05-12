# Constructor

## 1. Penjelasan Constructor

Constructor merupakan method spesial yang otomatis dijalankan ketika suatu objek dibuat

## 2. Cara Menggunakan Constructor

### 2.1. Membuat Constructor

Untuk membuat constructor, kita perlu membuat method baru dengan nama yang sama seperti class nya. Misal kita ingin membuat constructor pada class `Hero`, maka nama dari constructornya adalah `Hero()`

```csharp
// Hero.cs

using System;

namespace AdventureGame
{
  class Hero
  {
    public String name;
    public int health;

    // membuat constructor
    public Hero() {
      Console.WriteLine("constructor dijalankan");
    }

    public void Healing() {
      this.health += 100;
    }

    public void ShowInfo() {
      Console.WriteLine("name : " + this.name);
      Console.WriteLine("health : " + this.health);
    }
  }
}
```

### 2.2. Menjalankan Constructor

Untuk menjalankan constructor yang sudah dibuat pada class `Hero`, kita tinggal membuat object baru menggunakan class tersebut

```csharp
// Program.cs

using System;

namespace AdventureGame
{
  class Program
  {
    static void Main(string[] args)
    {
      // constructor otomatis dijalankan saat membuat object baru
      Hero hero1 = new Hero(); // output : constructor dijalankan
    }
  }
}
```

## 3. Contoh Penggunaan Constructor

Constructor biasanya digunakan untuk mengisi attribute dari suatu object saat object tersebut dibuat, contohnya sebagai berikut

```csharp
// Hero.cs

using System;

namespace AdventureGame
{
  class Hero
  {
    public String name;
    public int health;

    // mengisi attribute menggunakan constructor
    public Hero(String name, int health) {
      this.name = name;
      this.health = health;
    }

    public void Healing() {
      this.health += 100;
    }

    public void ShowInfo() {
      Console.WriteLine("name : " + this.name);
      Console.WriteLine("health : " + this.health);
    }
  }
}
```

```csharp
// Program.cs

using System;

namespace AdventureGame
{
  class Program
  {
    static void Main(string[] args)
    {
      // mengisi attribute saat object dibuat
      Hero hero1 = new Hero("star platinum", 100);

      Console.WriteLine(hero1.name) // output : star platinum
      Console.WriteLine(hero1.health) // output : 100
    }
  }
}
```


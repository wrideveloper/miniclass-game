# Getter dan Setter

## 1. Penjelasan Getter dan Setter

Getter digunakan untuk memberikan akses kepada suatu attribute agar dapat dibaca nilainya

Setter digunakan untuk memberikan akses kepada suatu attribute agar dapat dibaca nilainya

```csharp
// Hero.cs

using System;

namespace AdventureGame
{
  class Hero
  {
    // ubah attribute health menjadi private
    private int health;

    // getter dan setter untuk attribute health
    public int Health
    {
      get
      {
        return this.health;
      }

      set
      {
        this.health = value;
      }
    }
  }
}
```

## 2. Kenapa Butuh Getter dan Setter

Terkadang kita perlu membatasi akses dari suatu attribute, misalnya, hanya bisa dibaca saja \(get\) atau diubah saja \(set\)

Sebagai contoh, attribute `health` seharusnya hanya bisa di ubah nilainya menggunakan method `healing`, dan tidak bisa diubah secara langsung


# Collider Trigger

![](../.gitbook/assets/collider2d.png)

## 1. Penjelasan Collider Trigger

Collider trigger merupakan jenis collider yang digunakan untuk mendeteksi tabrakan pada suatu game object dengan game object lain. Apabila tabrakan terjadi maka kita bisa menghandle nya menggunakan script

## 2. Cara Menggunakan Collider Trigger

### 2.1 Menerapkan Collider

Terapkan collider kepada kedua game object

### 2.2 Menerapkan Collider Trigger

Terapkan collider trigger kepada salah satu game object dengan cara mencentang `Is Trigger` pada component collider

### 2.3 Mendeteksi Tabrakan

Gunakan method berikut pada salah satu game object untuk mendeteksi tabrakan

```csharp
using UnityEngine;
using System.Collections;

public class ExampleClass : MonoBehaviour
{
    void OnTriggerEnter2D(Collider2D other)
    {
        // dijalankan ketika object mulai bertabrakan
    }

    void OnTriggerStay2D(Collider2D other)
    {
        // dijalankan ketika object terus bertabrakan
    }

    void OnTriggerExit2D(Collider2D other)
    {
        // dijalankan ketika object berhenti bertabrakan
    }
}
```


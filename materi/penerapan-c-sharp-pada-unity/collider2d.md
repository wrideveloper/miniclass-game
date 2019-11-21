# Collider Trigger

![collider2d](collider2d.png)

## 1. Penjelasan Collider Trigger

Ada kalanya kita ingin menjalankan sebuah perintah ketika ada suatu game object yang sedang bertabrakan dengan game object lain, hal ini dapat diterapkan dengan cara menerapkan `Collider Trigger` pada salah satu game object tersebut.

Langkah - langkahnya seperti berikut :

1. Terapkan collider kepada kedua game object
2. Terapkan collider trigger kepada salah satu game object dengan cara mencentang `Is Trigger` pada component collider
3. Gunakan method berikut pada salah satu game object untuk mendeteksi tabrakan

```cSharp
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

**Untuk memahami lebih lanjut tentang `Collider2D` silahkan kunjungi link berikut :**

**Dokumentasi Collider 2D -** https://docs.unity3d.com/Manual/Collider2D.html

**Tutorial -** https://unity3d.com/learn/tutorials/topics/2d-game-creation/collider-2d

# Collider 2D

Ada kalanya ketika kita membuat game kita harus melakukan sesuatu ketika ada game object yang saling bertabrakan, hal ini dapat kita terapkan dengan menggunakan `Collider 2D`

![collider2d](collider2d.png)

## Apa Itu Collider 2D

Secara default apabila ada dua game object 2D yang akan bertabrakan maka kedua game object tersebut akan saling tembus dan tidak akan terjadi tabrakan

Hal ini terjadi karena kita tidak menerapkan `Collider2D` pada kedua game object tersebut, `Collider2D` merupakan component yang menentukan bentuk fisik dari suatu game object 2D agar kedua game object tadi dapat saling bertabrakan

![example](box-collider-2d-example.png)

## Collider Triger

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

# GetComponent

Saat membuat sebuah game, ada saatnya dimana kita harus mengubah nilai dari component pada suatu game object disaat runtime, hal ini bisa dilakukan dengan menggunakan method `GetComponent()`

![getcomponent](getcomponent.png)

## Apa Itu GetComponent

`GetComponent` merupakan method bawaan dari class `MonoBehaviour` yang bisa kita gunakan untuk mengambil suatu component pada game object kita, kemudian component yang didapatkan bisa diubah nilainya

```
void Start() {
  Rigidbody2D myRigidbody = GetComponent<Rigidbody2D>();
  myRigidbody.gravityScale = 0;
}
```

Misalnya pada script diatas kita mengambil component `Rigidbody2D` dari game object kita, lalu mengubah nilai `gravityScale` nya menjadi 0 untuk menghilangkan efek gravitasi, itulah contoh penggunaan `GetComponent`

**Untuk memahami lebih lanjut tentang `GetComponent` silahkan kunjungi link berikut :**

**Dokumentasi GetComponent -** https://docs.unity3d.com/ScriptReference/GameObject.GetComponent.html

**Tutorial -** https://unity3d.com/learn/tutorials/topics/scripting/getcomponent

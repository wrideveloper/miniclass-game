# Input

![](../.gitbook/assets/input.png)

## 1. Input.GetKey

Dengan menggunakan `Input.GetKey` kita bisa menghandle input secara langsung berdasarkan tombol pada keyboard atau mouse yang ditekan oleh user

```csharp
if (Input.GetKey(KeyCode.Space)) {
  // lakukan sesuatu saat tombol space ditekan
}
```

## 2. Input.GetButton

Dengan menggunakan `Input.GetButton` kita bisa memberikan label pada beberapa tombol, sehingga kita bisa menghandle banyak button dalam satu kondisi berdasarkan labelnya

misalnya kita memberi label `Jump` untuk tombol spasi dan up pada keyboard, sehingga :

```text
if (Input.GetButton("Jump")) {
  Jump()
}
```

Disini kita mendeteksi apakah button dengan label jump sudah ditekan atau belum, apabila ditekan maka kita akan menjalankan method `Jump()`, mungkin sekilas mirip seperti dengan menggunakan `Input.GetKey` namun akan kelihatan bedanya apabila kita membuka `Input Manager` \(Edit - Project Settings - Input\)

![input manager](../.gitbook/assets/input-manager.png)

Disitu bisa kita lihat bahwa label Jump memiliki dua tombol, yaitu space dan up, sehingga kita bisa melakukan `Jump()` dengan menekan tombol space atau up, disini kita juga bisa mengatur agar tombol Jump juga menerima input dari joysticks sehingga pada script yang kita buat kita tidak perlu menghandle banyak tombol, cukup panggil nama tombolnya saja \(misalnya Jump\) kemudian tinggal diatur di `Input Manager`

**Untuk lebih jelasnya bisa mengunjungi referensi berikut :**

**Dokumentasi GetButton -** [https://docs.unity3d.com/ScriptReference/Input.GetButton.html](https://docs.unity3d.com/ScriptReference/Input.GetButton.html)

**Tutorial -** [https://unity3d.com/learn/tutorials/topics/scripting/getbutton-and-getkey](https://unity3d.com/learn/tutorials/topics/scripting/getbutton-and-getkey)

## 3. Input.GetAxis

`Input.GetAxis` konsepnya mirip dengan `Input.GetButton` yaitu dengan memanggil nama labelnya kita bisa menghandle banyak tombol dengan melalui `Input Manager`, namun perbedaannya adalah `Input.GetAxis` tidak mereturn boolean seperti `Input.GetButton` melainkan nilai antara 1 dan -1

Misalnya kita mempunyai axis dengan label horizontal :

![input manager horizontal](../.gitbook/assets/input-manager-horizontal.png)

Disana kita mengeset left sebagai tombol negatif \(bernilai -1\) dan right sebagai tombol positif \(bernilai 1\)

Biasanya `Input.GetAxis` dimanfaatkan untuk menghandle pergerakan game object seperti berikut :

```text
void Update() {
  float horizontal = Input.GetAxis("Horizontal");
  transform.Translate(horizontal, 0, 0);
}
```

variabel horizontal akan bernilai 1 apabila kita menekan tombol right dan akan bernilai -1 apabila kita menekan tombol left

**Untuk lebih jelasnya bisa mengunjungi referensi berikut :**

**Dokumentasi GetAxis -** [https://docs.unity3d.com/ScriptReference/Input.GetAxis.html](https://docs.unity3d.com/ScriptReference/Input.GetAxis.html)

**Tutorial -** [https://unity3d.com/learn/tutorials/topics/scripting/getaxis](https://unity3d.com/learn/tutorials/topics/scripting/getaxis)


# Delta Time

![delta time](delta-time.png)

## Apa Itu Delta Time

Secara sederhana delta time merupakan sebuah teknik dalam unity yang berguna untuk mengubah satuan per frame menjadi per detik

## Permasalahan

Ketika kita membuat sebuah statement didalam method `update()` maka statement tersebut akan dijalankan dengan satuan FPS (Frame per second), artinya dalam satu detik komputer kita bisa menjalankan method update lebih dari satu kali tergantung kecepatan FPS

Misalnya kita akan memindahkan game object dengan menggunakan `transform.Translate` :

```
void Update() {
  transform.Translate(5, 0, 0);
}
```

Pada script diatas kita akan memindahkan game object ke kanan dengan kecepatan 5, yang kita bayangkan adalah game object tersebut akan berpindah ke kanan sebanyak 5 langkah per detik

Namun kenyataannya yang terjadi adalah game object akan bergerak dengan sangat cepat, mengapa ? karena method `update()` akan dijalankan lebih dari satu kali setiap detiknya, karena dalam satu detik komputer kita bisa menjalankan banyak frame

Misalnya :

> 30 FPS = dalam 1 detik bisa mengeksekusi 30 Frame

Artinya dalam 1 detik bisa menjalankan method update sebanyak 30 kali, sehingga dalam 1 detik game object kita akan bergerak sebanyak 30 x 5 = 150 langkah per detik

## Solusi

Kita bisa menggunakan delta time agar statement `transform.Translate` memindahkan game object sebanyak 5 langkah per detik (bukan per frame), sehingga script sebelumnya akan berubah menjadi seperti berikut :

```
void Update() {
  transform.Translate(5 * Time.deltaTime, 0, 0);
}
```

Kita tinggal mengalikan kecepatan translate dengan `Time.deltaTime` sehingga game object akan berpindah 5 langkah ke kanan setiap detik

## Tutorial

Untuk lebih jelasnya, silahkan lihat tutorial dibawah ini :
https://unity3d.com/learn/tutorials/topics/scripting/delta-time

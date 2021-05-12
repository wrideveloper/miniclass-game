# Delta Time

![](../.gitbook/assets/delta-time.png)

## 1. Penjelasan Delta Time

Secara sederhana delta time merupakan sebuah teknik dalam unity yang berguna untuk mengubah satuan per frame menjadi per detik

## 2. Permasalahan

Ketika kita membuat sebuah statement didalam method `update()`, maka statement tersebut akan dijalankan dengan satuan FPS \(Frame per second\). Artinya, dalam satu detik komputer kita akan menjalankan method update lebih dari satu kali tergantung kecepatan FPS

Misalnya kita akan memindahkan game object dengan menggunakan `transform.Translate` :

```text
void Update() {
  this.transform.Translate(5, 0, 0);
}
```

Pada script diatas kita akan memindahkan game object ke kanan sejauh 5 meter, yang kita bayangkan adalah game object tersebut akan berpindah ke kanan sebanyak 5 meter per detik

Namun kenyataannya yang terjadi adalah game object akan bergerak dengan sangat cepat, mengapa ? karena method `update()` akan dijalankan lebih dari satu kali setiap detiknya, karena dalam satu detik komputer kita bisa menjalankan banyak frame

Misalnya :

> 30 FPS = dalam 1 detik bisa mengeksekusi 30 Frame

Artinya dalam 1 detik bisa menjalankan method update sebanyak 30 kali, sehingga dalam 1 detik game object kita akan bergerak sebanyak 30 x 5 = 150 langkah per detik

## 3. Solusi

Kita bisa menggunakan delta time agar statement `transform.Translate` memindahkan game object sebanyak 5 langkah per detik \(bukan per frame\), sehingga script sebelumnya akan berubah menjadi seperti berikut :

```text
void Update() {
  transform.Translate(5 * Time.deltaTime, 0, 0);
}
```

Kita tinggal mengalikan kecepatan translate dengan `Time.deltaTime` sehingga game object akan berpindah 5 langkah ke kanan setiap detik

## 4. Referensi

Untuk lebih jelasnya, silahkan lihat tutorial dibawah ini : [https://unity3d.com/learn/tutorials/topics/scripting/delta-time](https://unity3d.com/learn/tutorials/topics/scripting/delta-time)


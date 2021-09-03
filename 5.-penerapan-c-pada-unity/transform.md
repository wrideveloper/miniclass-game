# Transform

![](../.gitbook/assets/transform.png)

## 1. Penjelasan Transform

![transform inspector](../.gitbook/assets/transform-inspector.png)

Transform dalam unity berguna untuk menentukan posisi, rotasi, serta ukuran dari suatu game object. Transform dapat diakses melalui `inspector` atau juga bisa melalui `script` dengan menggunakan attribute `transform`

## 2. Jenis Penggunaan Transform

### 2.1. `transform.Position`

berguna untuk menentukan posisi dari game object, disini kita bisa langsung memberikan koordinat \( X, Y \) dari game object

```csharp
// set posisi game object ke koordinat 0,0
this.transform.position = new Vector(0, 0);
```

### 2.2. `transform.Translate`

berguna untuk menggeser game object, disini kita bisa memasukkan kecepatan perpindahan game object untuk koordinat x, y, dan z

```csharp
// geser posisi game object ke arah atas sebesar 5 meter
this.transform.Translate(0, 5, 0);
```


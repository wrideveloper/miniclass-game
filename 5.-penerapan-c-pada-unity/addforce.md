# Add Force

![Jump](../.gitbook/assets/jump.png)

## 1. Penjelasan Add Force

AddForce merupakan method RigidBody yang digunakan untuk memberikan gaya pada suatu game objek

## 2. Cara Menggunakan Add Force

Kita bisa menerapkan AddForce pada suatu game objek seperti berikut ini :

```csharp
// ambil component rigid body dari game object
Rigidbody2D myRigidBody = GetComponent<Rigidbody2D> ();

// menambah gaya ke atas sebesar 10 meter
myRigidBody.AddForce(new Vector2(0, 10));
```

pada script diatas kita akan membuat game objek terdorong ke atas sebanyak 10 meter

## 3. Force Mode

Ada beberapa jenis force yang dapat kita gunakan dalam game 2D

| Jenis | Penjelasan | Contoh penggunaan |
| :--- | :--- | :--- |
| Force | Menerapkan force secara perlahan | Objek didorong |
| Impulse | Menerapkan force secara seketika | Objek terpental karena ledakan |

Kita bisa menggunakan jenis - jenis force tersebut dengan menggunakan parameter kedua pada method AddForce

```csharp
// ambil component rigid body dari game object
Rigidbody2D myRigidBody = GetComponent<Rigidbody2D> ();

// menerapkan Force Mode Force
myRigidBody.AddForce(new Vector2(0, 10), ForceMode2D.Force);

// menerapkan Force Mode Impulse
myRigidBody.AddForce(new Vector2(0, 10), ForceMode2D.Impulse);
```


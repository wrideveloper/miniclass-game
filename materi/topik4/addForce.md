# Add Force

![Jump](jump.png)

## Penjelasan

**AddForce** merupakan method Rigid Body yang digunakan untuk merubah kecepatan atau arah dari suatu game objek, misalnya apabila objek melompat, terpental entah karena hantaman atau ledakan, dan lain lain

## Penggunaan

Kita bisa menerapkan AddForce pada suatu game objek seperti berikut ini :

```cSharp
Rigidbody2D myRigidBody = GetComponent<Rigidbody2D> ();
myRigidBody.AddForce(new Vector2(0, 10));
```

pada script diatas kita akan membuat game objek terdorong ke atas sebanyak 10 meter

## Jenis Force

Ada beberapa jenis force yang dapat kita gunakan dalam game 2D

| Jenis   | Penjelasan                                                 | Contoh penggunaan              |
| ------- | ---------------------------------------------------------- | ------------------------------ |
| Force   | Menerapkan force secara terus menerus terhadap suatu objek | Objek didorong                 |
| Impulse | Menerapkan force secara seketika terhadap suatu objek      | Objek terpental karena ledakan |

Kita bisa menggunakan jenis - jenis force tersebut dengan menggunakan parameter kedua pada method AddForce

```cSharp
Rigidbody2D myRigidBody = GetComponent<Rigidbody2D> ();

myRigidBody.AddForce(new Vector2(0, 10), ForceMode2D.Force);
myRigidBody.AddForce(new Vector2(0, 10), ForceMode2D.Impulse);
```
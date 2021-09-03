# Velocity

![Velocity](../.gitbook/assets/velocity.jpeg)

## 1. Penjelasan Velocity

**Velocity** merupakan bagian dari Rigidbody yang menentukan kecepatan dan arah gerak suatu objek

## 2. Cara Menentukan Velocity

Velocity bisa ditentukan nilainya dengan cara berikut :

```csharp
// mengambil component rigid body dari game object
Rigidbody2D myRigidBody = GetComponent<Rigidbody2D> ();

// mengubah velocity dari rigid body
myRigidBody.velocity = new Vector2 (5, 0);
```

dengan menerapkan script diatas pada suatu objek maka objek tersebut akan bergerak ke kanan dengan kecepatan 5 meter perdetik

## 3. Player Control dengan Velocity

Dengan memanfaatkan velocity, kita bisa mengontrol suatu game objek

```csharp
public class PlayerMove : MonoBehaviour {

    private Rigidbody2D myRigidBody;
    public float speed = 10;

    void Start () {
        // mengambil component rigid body dari game object
        myRigidBody = GetComponent<Rigidbody2D> ();
    }

    void Update () {
        // mendapatkan nilai axis
        float horizontal = Input.GetAxis ("Horizontal");
        float vertical = Input.GetAxis ("Vertical");

        // mengubah velocity
        myRigidBody.velocity = new Vector2 (horizontal * speed, vertical * speed);
    }
}
```


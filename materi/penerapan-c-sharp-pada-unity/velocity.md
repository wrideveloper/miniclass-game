# Velocity

![Velocity](velocity.jpeg)

## Penjelasan

**Velocity** merupakan bagian dari Rigidbody yang menentukan kecepatan dan arah gerak suatu objek

Velocity bisa ditentukan nilainya dengan cara berikut :

```cSharp
Rigidbody2D myRigidBody = GetComponent<Rigidbody2D> ();
myRigidBody.velocity = new Vector2 (5, 0);
```

dengan menerapkan script diatas pada suatu objek maka objek tersebut akan bergerak ke kanan dengan kecepatan 5 meter perdetik

## Player Control dengan Velocity dan Input Axis

Dengan memanfaatkan velocity dan input axis, kita bisa mengontrol suatu game objek

```cSharp
public class PlayerMove : MonoBehaviour {

	private Rigidbody2D myRigidBody;
	public float speed = 10;

	// Use this for initialization
	void Start () {
		myRigidBody = GetComponent<Rigidbody2D> ();
	}

	// Update is called once per frame
	void Update () {
		float horizontal = Input.GetAxis ("Horizontal");
		float vertical = Input.GetAxis ("Vertical");
		myRigidBody.velocity = new Vector2 (horizontal * speed, vertical * speed);
	}
}
```

# GetComponent

![getcomponent](../.gitbook/assets/getcomponent.png)

## 1. Penjelasan GetComponent

`GetComponent` merupakan method yang bisa kita gunakan untuk mengambil suatu component pada game object kita

```csharp
void Start() {
  // mengambil component rigid body yang ada pada game object
  Rigidbody2D myRigidbody = GetComponent<Rigidbody2D>();

  // mengubah gravity scale rigid body menjadi 0
  myRigidbody.gravityScale = 0;
}
```


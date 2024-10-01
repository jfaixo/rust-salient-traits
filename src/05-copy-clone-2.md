# Copy & Clone : Le nom de mon chat

```rust
struct Cat {
  age: u8,
  name: String,
}

impl Cat {
  fn age(&self) -> u8 {
      self.age
  }

  fn name(&self) -> String {
    self.name
  }
}

fn main() {
  let my_cat = Cat { age: 2, name: "Grispoil".to_string() };

  println!("It is {} years old.", my_cat.age());
  println!("Its name is {}.", my_cat.name());
  println!("Its memory footprint is {} byte(s).", size_of_val(&my_cat));
}
```

<details>
<summary></summary>

Pourquoi cette implémentation de méthode fonctionne pour l'age, mais pas pour le nom ?

> Car le type [`u8`](https://doc.rust-lang.org/std/primitive.u8.html) implémente le trait [Copy](https://doc.rust-lang.org/std/marker/trait.Copy.html), mais pas le type [`String`](https://doc.rust-lang.org/std/string/struct.String.html).

</details>

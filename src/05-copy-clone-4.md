# Copy & Clone : Le nom de mon chat #1

Option de correction #1: on fait ce que le compilateur nous dit, ie cloner le nom.

[String](https://doc.rust-lang.org/std/string/struct.String.html) implémente le trait [Clone](https://doc.rust-lang.org/std/clone/trait.Clone.html)

```rust
struct Cat {
  age: u8,
  name: String,
}

impl Cat {
#  fn species(&self) -> String {
#      "cat".to_string()
#  }
#
#  fn age(&self) -> u8 {
#      self.age
#  }
#
  fn name(&self) -> String {
    self.name.clone()
  }
}

fn main() {
  let my_cat = Cat { age: 2, name: "Grispoil".to_string() };

  println!("This is a {}.", my_cat.species());
  println!("It is {} years old.", my_cat.age());
  println!("Its name is {}.", my_cat.name());
  println!("Its memory footprint is {} byte(s).", size_of_val(&my_cat));
}
```

L'appel à `clone` est volontairement explicite pour rappeler au développeur que c'est une opération potentiellement coûteuse.

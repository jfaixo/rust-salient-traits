# Copy & Clone : Le nom de mon chat #2

Option de correction #2: on comprend ce que l'on fait.


```rust,editable
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
  fn name(&self) -> &str {
    &self.name
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

[Deref Coercion](https://doc.rust-lang.org/std/ops/trait.Deref.html#deref-coercion)
# Un exemple de Trait 🐈

```rust
trait Pet {
  fn species(&self) -> String;
}

struct Cat {
  age: u8,
}

impl Cat {
  fn age(&self) -> u8 {
      self.age
  }
}

/// impl is also used to provide the implementation of a trait to a type.
impl Pet for Cat {
  fn species(&self) -> String {
      "cat".to_string()
  }
}

fn main() {
  let my_cat = Cat {
    age: 2,
  };

  println!("This is a {}.", my_cat.species());
  println!("It is {} years old.", my_cat.age());
  println!("Its memory footprint is {} byte(s).", size_of_val(&my_cat));
}
```
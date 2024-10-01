# Dessine moi un chat

```rust,editable
struct Cat {
  age: u8,
}

/// The impl keyword is used to implement functions related to a type.
impl Cat {
  pub fn new(age: u8) -> Self {
    Cat { age: age }
  }

  fn age(&self) -> u8 {
    self.age
  }

  fn birthday(&mut self) {
    self.age += 1;
  }

  fn explode(self) {
    println!("this {} year old cat is an exploding kitten!", self.age);
  }
}

fn main () {
  let mut my_cat = Cat::new(2);
  println!("It is {} years old.", my_cat.age());
  my_cat.birthday();

  // Move
  let also_my_cat = my_cat;

  // Errors
  // println!("It is {} years old.", my_cat.age());

  println!("It is {} years old.", also_my_cat.age());
  also_my_cat.explode();

  // Also errors
  // also_my_cat.birthday();
}
```

# Copy & Clone : L'age de mon chat

```rust
struct Cat {
  age: u8,
}

impl Cat {
  fn age(&self) -> u8 {
      self.age
  }
}

fn main() {
  let my_cat = Cat { age: 2 };

  println!("It is {} years old.", my_cat.age());
  println!("Its memory footprint is {} byte(s).", size_of_val(&my_cat));
}
```
# Copy & Clone : L'age de mon chat est copié

```rust,editable
struct Cat {
  age: u8,
}

impl Cat {
  fn age(&self) -> u8 {
    println!("addresse de l'age dans mon chat: {:p}", &self.age);
    self.age
  }
}

fn main() {
  let my_cat = Cat { age: 2 };

  println!("addresse de l'age retourné: {:p}", &my_cat.age());
}
```

Trait: [Pointer](https://doc.rust-lang.org/std/fmt/trait.Pointer.html)

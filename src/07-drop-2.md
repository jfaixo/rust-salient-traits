# Drop: le destructeur

Trait: [Drop](https://doc.rust-lang.org/std/ops/trait.Drop.html)

```rust
struct Cat {
  age: u8,
  name: String,
}

impl Drop for Cat {
  fn drop(&mut self) {
    println!("{} destroyed", self.name);
  }
}

fn main() {
  let cat_1 = Cat { age: 2, name: "Grispoil".to_string() };

  {
    let cat_2 = Cat { age: 18, name: "Berlioz".to_string() };
  }
}

```
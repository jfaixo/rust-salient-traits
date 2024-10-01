# Héritage de mutabilité

En Rust, la mutabilité est héritée.

```rust,editable

struct Necklace {
  text: String
}

struct Cat {
  age: u8,
  necklace: Necklace
}

fn main() {
  // Immutable
  let my_cat = Cat {
    age: 2,
    necklace: Necklace { text: "Purrfect".to_string() }
  };

  // Write is KO
  // my_cat.age = 3;
  // my_cat.necklace.text += " cat";

    // Read only is OK
  println!("My cat's necklace has a message: {}", my_cat.necklace.text);
}
```

Pour plus des détails, voir [Mutability](https://web.mit.edu/rust-lang_v1.25/arch/amd64_ubuntu1404/share/doc/rust/html/book/first-edition/mutability.html).
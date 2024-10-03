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

[Mutability](https://doc.rust-lang.org/beta/book/ch03-01-variables-and-mutability.html)
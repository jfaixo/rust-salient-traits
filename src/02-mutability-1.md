# Inférence de type, mutabilité

La mutabilité est vérifiée pour chaque variable. Le compilateur Rust valide que chaque utilisation de variable est faite dans le bon contexte, sans quoi, ça ne compile pas.

```rust,editable
struct Cat {
  age: u8,
}

fn main() {
  // Immutable variable by default
  let age_sample = 3;
  let my_cat = Cat { age: 2 };

  // Read only is OK
  println!("My cat is {} years old.", my_cat.age);

  // Write is KO
  // my_cat.age = 3;
}
```

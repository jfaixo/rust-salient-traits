# Syntaxe de fonction

En Rust, un chat ça peut ressembler à ça:
```rust
// A data type definition
struct Cat {
  age: u8,
  pub name: String,
}

fn do_nothing() {
  // (=ↀωↀ=)✧
}

fn still_do_nothing() -> () {
  // ლ(=ↀωↀ=)ლ
}

fn get_age(cat: Cat) -> u8 {
  return cat.age;
}

// Or better...

fn get_age_bis(cat: Cat) -> u8 {
  cat.age
}
```

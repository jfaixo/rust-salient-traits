# Encore un cas perturbant: Les boucles

```rust
let strings = vec!["a", "b", "c"];

for s in strings {
  println!("{}", s);
}
```

```rust
let strings = vec!["a", "b", "c"];

for s in strings {
  println!("{}", s);
}

for s in strings {
  println!("{}", s);
}
```

<details>
<summary></summary>

[Vec](https://doc.rust-lang.org/std/vec/struct.Vec.html)

Trait: [IntoIterator](https://doc.rust-lang.org/stable/std/iter/trait.IntoIterator.html)

```rust
let strings = vec!["a", "b", "c"];

for s in &strings {
  println!("{}", s);
}

for s in strings.iter() {
  println!("{}", s);
}
```

[iter()](https://doc.rust-lang.org/std/vec/struct.Vec.html#method.iter)  
Trait: [Iterator](https://doc.rust-lang.org/std/iter/trait.Iterator.html)


</details>
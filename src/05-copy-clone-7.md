# Implémentation par défaut

Le compilateur Rust est capable de générer des implémentations par défaut pour certains traits.

C'est par exemple le cas pour Copy et Clone.

```rust
struct Point {
  x: i32,
  y: i32,
}

let a = Point {x: 0, y: 1 };
// Move
let b = a;
// Error
println!("x_a={}", a.x);
```

```rust
#[derive(Clone)]
struct Point {
  x: i32,
  y: i32,
}

let a = Point {x: 0, y: 1 };
// a & b are both owned
let b = a.clone();

println!("x_a={}", a.x);
```

```rust
#[derive(Clone, Copy)]
struct Point {
  x: i32,
  y: i32,
}

let a = Point {x: 0, y: 1 };
// Copy
let b = a;

println!("x_a={}", a.x);
```


[Documentation: Derive](https://doc.rust-lang.org/rust-by-example/trait/derive.html)
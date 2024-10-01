# Un autre cas perturbant: Move semantic

```rust
let x = 42;
// That's a copy, both x and y are owned
let y = x;
println!("{}", y);
println!("{}", x);

```


```rust
let x = "Hello world".to_string();
// That's NOT a copy, s ownership is transfered
let y = x;

println!("{}", y);
println!("{}", x);

```

En Rust, le cas par défaut est un move lors de l'affectation. Une exception implicite s'applique aux types qui implémente Copy.
# Rust, stack et heap (1/2)

Q:Comment gérer le cas de variables dont on souhaite la taille dynamique ?  
A: En allouant dynamiquement de la mémoire, sur la heap.

Exemple: La structure `Vector` en Rust, qui est un tableau contigu de taille variable (l'équivalent d'un ArrayList Java, ou d'un.. vector en c++).

```rust
// A first way to create a vector
let mut my_first_vector = Vec::new();
println!("my_first_vector: {}", my_first_vector.capacity());
my_first_vector.push(42);
println!("my_first_vector: {}", my_first_vector.capacity());

// An other way
let mut my_second_vector = Vec::with_capacity(1);
println!("my_second_vector: {}", my_second_vector.capacity());
my_second_vector.push(42);
println!("my_second_vector: {}", my_second_vector.capacity());

// Yet another way
let mut i_m_a_pro_at_vector_now = vec![1, 2, 3];
println!("i_m_a_pro_at_vector_now: {}", i_m_a_pro_at_vector_now.capacity());
```
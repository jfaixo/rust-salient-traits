# Comment Rust gère la mémoire

[Doc: Lifetimes](https://doc.rust-lang.org/rust-by-example/scope/lifetime.html)

On a vu que les variables déclarées sont systématiquement sur la stack. La gestion mémoire de Rust est couplée à la durée de vie de chaque variable.


```rust
// Lifetimes are annotated below with lines denoting the creation
// and destruction of each variable.
// `i` has the longest lifetime because its scope entirely encloses 
// both `borrow1` and `borrow2`. The duration of `borrow1` compared 
// to `borrow2` is irrelevant since they are disjoint.
fn main() {
    let i = 3; // Lifetime for `i` starts. ────────────────┐
    //                                                     │
    { //                                                   │
        let borrow1 = &i; // `borrow1` lifetime starts. ──┐│
        //                                                ││
        println!("borrow1: {}", borrow1); //              ││
    } // `borrow1` ends. ─────────────────────────────────┘│
    //                                                     │
    //                                                     │
    { //                                                   │
        let borrow2 = &i; // `borrow2` lifetime starts. ──┐│
        //                                                ││
        println!("borrow2: {}", borrow2); //              ││
    } // `borrow2` ends. ─────────────────────────────────┘│
    //                                                     │
}   // Lifetime ends. ─────────────────────────────────────┘
```

Rust apporte ainsi la garantie que la mémoire est parfaitement gérée, les ressources étant automatiquement désallouées pour nous dès que leur lifetime expire (ie bien souvent, dès qu'elles sortent du scope).

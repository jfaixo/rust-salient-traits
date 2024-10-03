# Mutabilité externe et interne

Rust fait la distinction entre mutabilité *externe* et *interne*.

Exemple:
```rust,editable
use std::cell::RefCell;

fn main() {
  let x = 42;
  // Fail... try adding mut
  // x = 43;
  println!("x={}", x);

  let my_list = vec![1, 2, 3, 4];
  // Also fail... try adding mut
  // my_list.push(5);
  println!("list: {:?}", my_list);

  // To go further...
  let my_list = RefCell::new(vec![1, 2, 3, 4]);
  my_list.borrow_mut().push(5);
  println!("refcell: {:?}", my_list.borrow());
}
```

> Il est généralement déconseillé dans le cas général (et je déconseille personnellement) d'utiliser la mutabilité interne.
>
> En effet, dans ce cas le borrowing n'est vérifié qu'au runtime. De plus, l'écriture d'un tel code devient rapidement confus.
>
> Bien souvent, il est possible de procéder autrement pour contourner le problème rencontré par le compilateur.

- [RefCell and interior mutability](https://doc.rust-lang.org/beta/book/ch15-05-interior-mutability.html)
- [RefCell](https://doc.rust-lang.org/std/cell/struct.RefCell.html)
# Les principaux traits de Rust

Le compilateur Rust importe automatiquement un sous-ensemble de choses essentielles dans tous les programmes Rust: il s'agit des [<mark>prelude</mark>](https://doc.rust-lang.org/std/prelude/index.html).

  
### Les 26 traits au coeur de Rust
  
| v1 | marker | ops | iter | convert | others |
|---|---|---|---|---|---|
| Send | **Clone** | **Drop** | DoubleEndedIterator | AsMut | ToOwned |
| **Sized** | **Copy** | Fn | ExactSizeIterator | AsRef | ToString |
| Sync | Default | FnMut | Extend | From |
| Unpin | Eq | FnOnce | **IntoIterator** | Into |
| | Ord | | **Iterator** |
| | PartialEq | | |
| | PartialOrd | | |

Auxquels on peut ajouter les Traits notables suivants: [Display](https://doc.rust-lang.org/std/fmt/trait.Display.html), [Debug](https://doc.rust-lang.org/std/fmt/trait.Debug.html), et tous les traits [std::ops](https://doc.rust-lang.org/std/ops/index.html#traits)

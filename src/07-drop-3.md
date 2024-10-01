# Lifetime explicite

Lorsque l'on souhaite stocker des références dans des structures de données, le compilateur a besoin d'information pour connaitre la relation entre les durées de vie des données.

```rust
struct Necklace {
  text: String,
}

struct Cat {
  necklace: &Necklace,
}

let my_necklace = Necklace { text: "Purr".to_string() };
let my_cat = Cat {necklace: &my_necklace };
```

<details>
<summary></summary>

```rust
struct Necklace {
  text: String,
}

struct Cat<'a> {
  necklace: &'a Necklace,
}

let my_necklace = Necklace { text: "Purr".to_string() };
let my_cat = Cat {necklace: &my_necklace };
```

</details>
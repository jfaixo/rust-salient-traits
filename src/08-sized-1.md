# Utiliser les traits pour généraliser

```rust
trait Pet {
    fn age(&self) -> u8;
}

struct Cat {
    age: u8,
}

impl Pet for Cat {
    fn age(&self) -> u8 {
        self.age
    }
}

struct Dog {
    age: u8,
}

impl Pet for Dog {
    fn age(&self) -> u8 {
        self.age
    }
}

// Errors
fn print_pet(pet: Pet) {
    println!("The pet's age is {}", pet.age());
}

fn main() {
    let my_cat = Cat { age: 2 };
    let my_dog = Dog { age: 10 };
    print_pet(my_cat);
    print_pet(my_dog);
}

```
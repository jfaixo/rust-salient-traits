# Option 1: Dynamic dispatch

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
fn print_pet(pet: Box<dyn Pet>) {
    println!("The pet's age is {}", pet.age());
}

fn main() {
    let my_cat = Box::new(Cat { age: 2 });
    let my_dog = Box::new(Dog { age: 10 });
    print_pet(my_cat);
    print_pet(my_dog);
}

```
[Godbolt](https://godbolt.org/z/fvxrz8zTv)
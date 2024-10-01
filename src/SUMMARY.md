[Introduction](./00-introduction.md)
# Basiques de syntaxe
- [Une structure de donnée](./01-basic-syntax-1.md)
- [Syntaxe de fonction](./01-basic-syntax-2.md)
# Mutability
- [Inférence de type, mutabilité](./02-mutability-1.md)
- [Héritage de mutabilité](./02-mutability-2.md)
- [Mutabilité externe & interne](./02-mutability-3.md)
# Ownership
- [Variables et références](./03-ownership-1.md)
- [Encore de la syntaxe, ownership](./03-ownership-2.md)

# C'est quoi un Trait ?
- [Définition](./04-trait-1.md)
- [Un exemple de Trait](./04-trait-2.md)
- [Les principaux traits de Rust](./04-trait-3.md)

# Copy & Clone
- [L'age mon chat](./05-copy-clone-1.md)
- [Le nom de mon chat](./05-copy-clone-2.md)
- [L'age de mon chat est copié](./05-copy-clone-3.md)
  - [Rappel: Fonctionnement de la stack (1/2)](./05-stack-1.md)
  - [Rappel: Fonctionnement de la stack (2/2)](./05-stack-2.md)
  - [Rappel: stack et heap (1/2)](./05-heap-1.md)
  - [Rappel: stack et heap (2/2)](./05-heap-2.md)
- [Correction option #1](./05-copy-clone-4.md)
- [Correction option #2](./05-copy-clone-5.md)
  - [Parenthèse: les String en Rust, c'est pas si simple](./05-strings.md)
- [Un autre cas perturbant: Move semantic](./05-copy-clone-6.md)
- [Implémentation par défaut](./05-copy-clone-7.md)
# IntoIterator & Iterator
- [Encore un cas perturbant: Les boucles](./06-iterator.md)
# Variable lifetimes & Drop
- [Comment Rust gère la mémoire](./07-drop-1.md)
- [Drop: le destructeur](./07-drop-2.md)
- [Lifetime explicite](./07-drop-3.md)
# Sized
- [Utiliser les traits pour généraliser](./08-sized-1.md)
- [Option 1: Dynamic dispatch](./08-sized-2.md)
- [Option 2: Static dispatch](./08-sized-3.md)
- [Option 3: Static dispatch de référence](./08-sized-4.md)
- [Option 4: Dynamic dispatch de référence](./08-sized-5.md)
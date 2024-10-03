# Variables et références

En Rust, on peut posséder:
- une instance `my_cat: Cat`
- une instance mutable `mut my_cat: Cat`
- une référence `my_cat: &Cat`
- une référence mutable `my_cat: &mut Cat`

<table>
<tr><td>Syntaxe Rust</td><td>Description</td></tr>
<tr>
<td>

```rust
fn do_something_to(cat: Cat) {
  // ...
}
```
</td>
<td>Je te donne mon chat. Je ne l'ai plus.

Une seule personne peut posséder le chat à la fois.
</td>
</tr>

<tr>
<td>

```rust
fn do_something_to(mut cat: Cat) {
  // ...
}
```
</td>
<td>Je te donne mon chat, et tu peux immédiatement le modifier. Je ne l'ai plus.

Une seule personne peut posséder le chat à la fois.
</td>
</tr>

<tr>
<td>

```rust
fn observe(cat: &Cat) {
  // ...
}
```
</td>
<td>Je te laisse regarder mon chat, mais je le garde. Tu ne peux rien lui faire, juste l'observer.

Plusieurs personnes peuvent admirer mon chat en même temps.
</td>
</tr>

<tr>
<td>

```rust
fn visit(cat: &mut Cat) {
  // ...
}
```
</td>
<td>Je te laisse faire des trucs avec mon chat, mais je le garde. Tu me le rends après.

Une seule personne peut avoir le chat en même temps.
</td>
</tr>

</table>

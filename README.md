# fifteen_game
minor update to [Fifteen puzzle game](https://rosettacode.org/wiki/15_puzzle_game#Rust) to rust 1.68.0 nightly using clippy and fmt 

changed:
```Rust
r#try!(write!(f, "|\n")); --> (<stuff>)? --> (writeln!(f, "|"))?;
.gen_range(0, 16); --> .gen_range(0..16);
.position(|&cell| match cell {Cell::Card(value) if value == i => true, _ => false,}) --> .position(|&cell| matches!(cell, Cell::Card(value) if value == i))
println!("{value}"); --> println!("{}", value);

```

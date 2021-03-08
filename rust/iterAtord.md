### Iterator Type


- **iter()**  element are passed by reference eliminate the need for copying
- **into_iter()** element are passed by value -- each one are copied


```rust
let numbers_iterator = [0,2,3,4,5].iter();
let sum = numbers_iterator
  .fold(0, |total, next| total + next);
let squared = (1..10).iter()
  .map(|&x| x * x).collect();
```

### Runnable examples

#### For vec
```rust
fn main() {
    let vector = (1..)            // Infinite range of integers
        .filter(|x| x % 2 != 0)   // Collect odd numbers
        .take(5)                  // Only take five numbers
        .map(|x| x * x)           // Square each number
        .collect::<Vec<usize>>(); // Return as a new Vec<usize>
    println!("{:?}", vector);     // Print result
}

```

#### For String

```rust
fn main() {
    let sentence = "This is a sentence in Rust.";
    let words: Vec<&str> = sentence
        .split_whitespace()
        .collect();
    let words_containing_i: Vec<&str> = words
        .into_iter()
        .filter(|word| word.contains("i"))
        .collect();
    println!("{:?}", words_containing_i);
}
```

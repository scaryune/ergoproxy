# Rust Comments

In computer programming, comments are lines of text used to describe the purpose of code. For example,

```
// entry point of the program
fn main() {
    // print text on the screen
    println!("Hello, World!");
}
```

Here, `// entry point of the program` and `// print text on to the screen` are comments.

Comments are completely ignored and not evaluated during code execution. Ideally, a comment should allow the reader to understand what a piece of code is doing.

---

## Types of Comments

There are two important types of comments in Rust:

- `//` - Line Comment
- `/*...*/` - Block Comment

---

## Line Comment in Rust

In Rust, we use two forward slashes, `//`, to create a line comment. For example,

```
fn main () {
    // declare a variable
    let x = 1;
    println!("x = {}", x);
}
```

**Output**

x = 1

Here, `// Declare a variable` is a line comment. The comment extends up to the end of the line and is also known as **single-line comments**.

We can also use line comments in the same line as the code. For example,

```
fn main() {
    let x = 1;    // declare a variable
    println!("x = {}", x);
}
```

Here, `// Declare a variable` is also a line comment placed at the end of the line containing code.

---

## Block Comment in Rust

In Rust, we use the symbol `/*...*/` to denote the block comment. It starts with `/*` and ends with `*/`. For example,

```
fn main() {
    /*
    declare a variable
    and assign value to it
    */
    let x = 1;
    println!("x = {}", x);
}
```

**Output**

x = 1

Here,

```
/*
declare a variable
and assign value to it
*/
```

is a block comment. You can see the block comment extends for multiple lines. Hence, it is also known as **multi-line comments**.

We can also create multi-line comments using multiple line comments. For example,

```
fn main() {
    // declare a variable
    // and assign value to it
    let x = 1;
    println!("x = {}", x);
}
```

**Output**

x = 1

Here, we have used two single-line comments: `// declare a variable` and `// and assign value to it` instead of a multi-line comment.

**Note:** In the Rust ecosystem, line comments are preferred over block comments.

---

## Disable Parts of Code Using Rust Comments

Comments are also useful for temporarily disabling chunks of code. Let's see an example:

```
fn main() {
    let x = 1;
    let y = 2;
    let z = 3;
    println!("z = {}", z);
}
```

This piece of code will throw a warning because both x and y variables are unused. Instead of completely removing these declarations, we can comment them.

```
fn main() {
    /*
    temporarily disable x and y variable declarations.
    let x = 1;
    let y = 2;
    */

    let z = 3;
    println!("z = {}", z);
}
```

**Output**

z = 3

Now, only the code outside of the block comment will be evaluated. We have temporarily disabled part of the code that was triggering a warning. Code comments can be helpful in these scenarios.
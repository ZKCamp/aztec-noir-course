# Noir Quiz Solutions

**1) Which of the following comparators are supported on field datatype?**

A) !=

B) ==

C) >

D) <

Answer: A & B

Try this code

```rust
fn main(x: Field, y: Field){
    assert (x != y); // also change != and try ==
}
```

and then 

```rust
fn main(x: Field, y: Field){
    assert (x > y);
}
```

The second program should give you an error

**2) Among the given test cases, which ones are successful?**

```rust
use dep::std;

fn main(x: u1, y: u1)  {
    std::println(x);
    assert(x + y == 500);
}

#[test]
fn test_1() {
    main(100, 400);
}

#[test]
fn test_2() {
    main(100, 200);
}

#[test]
fn test_3() {
    main(1, 5);
}

#[test]
fn test_4() {
    main(5, 2);
}
```

A) Only test_1

B) Only test_1, test_2 and test_4

C) Only test_1, test_2 and test_3

D) test_1, test_2, test_3 and test_4

Answer: C)

Solution:

When you assert the condition `x + y == 500`, since x and y are u1, 500 is also implicitly converted to u1. The value of 500 as u1 is 0. Therefore, any value of `x+y` in u1 that is equal to zero will satisfy this condition. As we know that all even values will be 0 in u1, therefore the sum of x and y should be even.

**3) Which of these is more proving efficient?**

A)

```rust
fn main(x : u32, y : pub u32) {
    let z = add(x, y);
    assert(z == 3);
}

fn add(x : u32, y : u32) -> u32  {
    x + y
}

#[test]
fn test_main() {
    main(1, 2);
}
```

B)

```rust
fn main(x : Field, y : pub Field) {
    let z = add(x, y);
    assert(z == 3);
}

fn add(x : Field, y : Field) -> Field  {
    x + y
}

#[test]
fn test_main() {
    main(1, 2);
}
```

Answer: B)

Solution: Code A) uses u32 values. Noir uses additional range check constraints on u32 which add to the number of gates being used. 

You can use the command `nargo info` to see the gates being used for each program. Program A) will have a significantly large number of gates.

**4) What is returned by the `std::hash::pedersen` functions?**

A) An elliptic curve point

B) An unsigned integer

C) A single field element

Answer: A)

Solution: Pedersen hash returns an elliptic curve point. We generally use only the x co-ordinate of this point as the hash value as it is sufficiently collision free.

**5) In the line below we are initializing an array of size 10 with all zeroes**

```rust
let mut arr = [0; 10]
```

What is the type of each element in this array?

A) Polymorphic Integer

B) u32

C) u64

D) Field

Answer: A)

Solution:

When initializing this array, the type of element is a polymorphic integer. The actual type is inferred on the first assignment, so if during assignment the first element is assigned to a Field, the type of each element of this array becomes Field

**6) What is the return value of `main` when x=”4294967295” and y=”4294967295”?**

```rust
fn main(x : u32, y : u32) -> pub u32 {
    let z = x + y;
    z
}
```

A) 8589934590

B) 4294967295

C) 4294967294

D) None of these

Answer: C)

Solution: In Noir, the integers overflow. If we add 1 to the max value of u32 (2^32 - 1), it becomes 0. Similarly when we add two max values here, we get 4294967294.

**7) Which of the following statements is true about slices?**

A) They can be resized dynamically at runtime

B) “use dep::std::slice” import is required to use slices

C) They cannot be returned from the circuit’s **main** function

Answer: A, B, C)

Solution: Read about slices [here](https://noir-lang.org/language_concepts/data_types#slices)

**8) What is the return value of main function?**

```rust
use dep::std;

fn main() -> pub Field {
    let x = 3;

    helper(x);

    x
}

fn helper(mut x: Field) {
    x = 4;
}
```

A) 4

B) 3

C) 0

C) An error is thrown

Answer: 3)

Solution: Mutability in noir is local and everything is passed by value, so if a called function mutates its parameters then the parent function will keep the old value of the parameters.
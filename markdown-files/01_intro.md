```rust
fn main() {
    println!("sample string");
}

// **************************************
//             VARIABLES
// **************************************
fn main() {
    // var names are "snake_case"
    let x = 13;
    println!("{}", x); // 13

    // explicit types
    let x: f64 = 3.14159;
    println!("{}", x); // 3.14159

    // rare case
    let x;
    x = 0;
    println("{}", x); // 0
}
// **************************************
//              END VARIABLES
// **************************************


// **************************************
//         CHANGING VARIABLES
// **************************************
fn main() {
    // mutable
    let mut x = 42;
    println!("{}", x); // 42

    x = 13;
    println!("{}", x); // 13
}
// **************************************
//         END CHANGING VARIABLES
// **************************************


// **************************************
//               BASIC TYPES
// **************************************
fn main() {
    // u8, u16, u32, u64, u128
    // i8, i16, i32, i64, i128
    // f32, f64
    let x = 12; // default i32
    let a = 12u8;
    let b = 4.3; // default f64
    let c = 4.3f32;
    let bv = true;
    let t = (13, false);
    let sentence = "hello rust";
    println!("{} {} {} {} {} {} {} {}",
             x, a, b, c, bv, t.0, t.1, sentence
    );
}
// **************************************
//           END BASIC TYPES
// **************************************

// **************************************
//         BASIC TYPE CONVERSION
// **************************************
fn main() {
    let a = 13u8;
    let b = 7u32;
    let c = a as u32 + b;
    println!("{}", c); // 20

    let t = true;
    println!("{}", t as u8); // 1
}
// **************************************
//        END BASIC TYPE CONVERSION
// **************************************

// **************************************
//               CONSTANTS
// **************************************
// constants are in SCREAMING_SNAKE_CASE
const PI: f32 = 3.14159;

fn main() {
    println!("{}", PI);
}
// **************************************
//               END CONSTANTS
// **************************************

// **************************************
//              ARRAYS
// **************************************
fn main() {
    let nums: [i32; 3] = [1, 2, 3];
    println!("{:?}", nums); // [1, 2, 3]
    println!("{}", nums[1]); // 2
}
// **************************************
//              END ARRAYS
// **************************************

// **************************************
//              FUNCTIONS
// **************************************
// fn names are SNAKE_CASE
fn add(x: i32, y: i32) -> i32 {
    return x + y;
}

fn main() {
    println!("{}", add(42, 13)); // 55
}
// **************************************
//            END FUNCTIONS
// **************************************

// **************************************
//         MULTIPLE RETURN VALUES
// **************************************
fn swap(x: i32, y: i32) -> (i32, i32) {
    return (y, x);
}

fn main() {
    let result = swap(123, 321);
    println!("{} {}", result.0, result.1); // 321 123

    let (a, b) = swap(result.0, result.1):
    println!("{} {}", a, b); // 123, 321
}
// **************************************
//       END MULTIPLE RETURN VALUES
// **************************************

// **************************************
//       RETURNING NOTHING
// **************************************
fn make_nothing() {
    return ();
}

// return type implied as ()
fn make_nothing2() {
    // returns () if nothing specified to return
}

fn main() {
    let a = make_nothing();
    let b = make_nothing2();

    println!("value of a: {:?}", a); // value of a: ()
    println!("value of b: {:?}", b); // value of b: ()
}
// **************************************
//         END RETURNING NOTHING
// **************************************
```
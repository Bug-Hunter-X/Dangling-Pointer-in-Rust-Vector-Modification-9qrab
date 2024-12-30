# Dangling Pointer Bug in Rust

This repository demonstrates a common error in Rust: creating a dangling pointer when working with vectors.  The provided `bug.rs` file shows the erroneous code. The `bugSolution.rs` file provides a corrected version that avoids this error.

**Description:**

The bug arises from obtaining a raw pointer to the vector's data and then modifying the vector itself. This can lead to a dangling pointer, causing unpredictable behavior, memory corruption, or crashes.

**Solution:**

The solution involves avoiding raw pointers whenever possible and using safer methods to manipulate vector data. Using methods within the `Vec` struct provides bounds-checking and prevents dangling pointers.
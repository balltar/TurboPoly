# TurboPoly
Polynomial representations and polynomial arithmetic algorithms in Rust. 

# First Steps

- [ ] Implement some heirarchy for Rings.
  - [ ] For example, there are Rings and Ring Elements. These should probably be distinct types. For example, if x is a RingElement<Ring> type then x can call x.is_zero() function. Or really any operations I may want to perform on a ring element like x.add(y) would output x+y. Maybe could have an enum algorithm for functions like x.multiply(y, algorithm), where then the multiply function pattern matches to find the appropriate algorithm. One could have algorithm implement Default trait so there is always a default algorithm. Default example: https://www.kirillvasiltsov.com/writing/optional-arguments-in-rust/
    - [ ] It might be useful to have the type of a ring element be RingElement<Ring: Representation> or something. Just there should be some way to indicate which representation we are using. Maybe have representation type be something like "all representations are stored as a Default type. A Default type is an enum type so we can do pattern matching on representation, but it has a Default element. Also, the representation type has a default_representation function that converts from usual representation to default representation. This is mostly to provide a mechanism of performing operations between elements of same type with a different representation (probably in a very slow way: moral: make sure everything is represented in the same way). Alternatively, we could just omit the default_representation function to make the representation type just an enum that implements Default. 
  - [ ] Two different representations for integers (decide on default... infinite precision if default_representation above is to be used)
    - [ ] u128 
    - [ ] Infinite precision integers. This could be a mini project on its own probably
  - [ ] Could implement Z / 2^8 Z, Z / 2^16 Z, Z / 2^32 Z, Z / 2^64 Z with u8, u16, u32, and u64 and the wrapping functions. 
  - [ ] How to represent Z / n Z
    -[ ] Implement this representation

- [ ] Implement a Univariate polynomial representation for polynomials as coefficient vectors
- [ ] Implement a basic convolution with univariate coefficient vector representation 
- [ ] Implement a convolution using Karatsuba with univariate coefficient vector representation

# Goals

## Traits
- [ ] Have traits for Ring or FFTUnity (I dunno, something that implements what's needed for FFT)

## Representations to try:
- [ ] Two vectors
- [ ] Coefficient lists
- [ ] DAGs
- [ ] Hash tables

## Algorithms to implement

- [ ] Naive Algorithm
- [ ] Karatsuba
- [ ] Fast Fourier Transform

## Testing Tools
- [ ] How to make random polynomials
  - [ ]  Homogeneous
  - [ ]  Bounded Coefficients
  - [ ]  Sparse
  - [ ]  Given degree

## Putting it all together
- [ ] How to test an algorithm with a certain representation and certain test sets

# Setup for Linux Subsystem on Windows

This tutorial was helpful: https://harsimranmaan.medium.com/install-and-setup-rust-development-environment-on-wsl2-dccb4bf63700

# Resources

Could have useful info or references: http://www.cecm.sfu.ca/CAG/papers/SDMPheap08.pdf

List of algorithms: https://www.gaussianwaves.com/2014/02/survey-of-methods-to-compute-convolution/

Fast Fourier Transform:
  * http://www.ece.umn.edu/users/parhi/SLIDES/chap8.pdf
  * http://kaltofen.math.ncsu.edu/bibliography/87/CaKa87_techrep.pdf

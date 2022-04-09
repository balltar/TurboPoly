# TurboPoly
Polynomial representations and polynomial arithmetic algorithms in Rust. 

# First Steps

- [ ] Implement some heirarchy for Rings.
  - [ ] For example, there are Rings and Ring Elements. These should probably be distinct types. For example, if x is a RingElement<Ring> type then x can call x.is_zero() function. Or really any operations I may want to perform on a ring element like x.add(y) would output x+y. Maybe could have an enum algorithm for functions like x.multiply(y, algorithm), where then the multiply function pattern matches to find the appropriate algorithm. One could have algorithm implement Default trait so there is always a default algorithm. 
  - [ ] Decide on precision levels for integers. Infinite precision is probably the best option. Implement this as a ring example.
  - [ ] Could implement Z / 8 Z, Z / 16 Z, Z / 32 Z, Z / 64 Z with u8, u16, u32, and u64 and the wrapping functions. 
  - [ ] How to implement Z / n Z

- [ ] Implement a Univariate polynomial representation for polynomials as coefficient vectors
- [ ] Implement a basic convolution with univariate coefficient vector representation 
- [ ] Implement a convolution using Karatsuba with univariate ceofficient vector representation

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
- [ ] Wiedmann's Algorithm (https://www.enseignement.polytechnique.fr/informatique/profs/Francois.Morain/Master1/Crypto/projects/Wiedemann86.pdf)
- [ ] Method of Four Russians
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

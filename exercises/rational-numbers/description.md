# Description

A rational number is a number that can be expressed as a fraction, with an integer numerator `a` and a non-zero integer denominator `b`.

~~~~exercism/note
Note that mathematically, the denominator can't be zero.
However, in many implementations of rational numbers, you will find that the denominator is allowed to be zero, with behavior similar to positive or negative infinity in floating point numbers.
In those cases, the denominator and numerator generally still can't both be zero at once.
~~~~

## Operations on rational numbers

### Absolute value

The absolute value of the rational number `r = a / b` is given by:

```text
|r| = |a / b| = |a| / |b|
```

### Addition

The sum of two rational numbers `r₁ = a₁ / b₁` and `r₂ = a₂ / b₂` is given by:

```text
r₁ + r₂ = a₁ / b₁ + a₂ / b₂
        = (a₁ * b₂ + a₂ * b₁) / (b₁ * b₂)
```

### Subtraction

The difference of two rational numbers `r₁` and `r₂` is given by:

```text
r₁ - r₂ = a₁ / b₁ - a₂ / b₂
        = (a₁ * b₂ - a₂ * b₁) / (b₁ * b₂)
```

### Multiplication

The product of two rational numbers `r₁` and `r₂` is given by:

```text
r₁ * r₂ = (a₁ * a₂) / (b₁ * b₂)
```

### Division

The result of dividing two rational numbers `r₁` and `r₂`, where `r₂` is non-zero, is given by:

```text
r₁ / r₂ = (a₁ * b₂) / (a₂ * b₁)
```

### Exponentiation

#### Exponentiation of a rational number

Let `r = a / b`.

* Raising `r` to a non-negative integer `n` is given by:

  ```text
  r^n = (a^n) / (b^n)
  ```

* Raising `r` to a negative integer `n` is given by:

  ```text
  r^n = (b^m) / (a^m)
  ```

  where `m` is the absolute value of `n`.

#### Exponentiation of a real number

Let `r = a / b`. Raising the real (floating-point) number `x` to the rational number `r` is given by:

```text
x^r = x^(a / b)
    = root(x^a, b)
```

where `root(p, q)` is the *q*th root of p.

## Implementation requirements

Given that you should not use built-in support for rational numbers, implement the following operations:

- absolute value of a rational number
- addition, subtraction, multiplication, and division of two rational numbers
- exponentiation of a rational number to an integer number
- exponentiation of a real number to a rational number

Your implementation should always reduce fractions to their lowest terms.
For example, `4/4` should reduce to `1/1`, `30/60` should reduce to `1/2`, `12/8` should reduce to `3/2`, and so on.
To reduce a rational number `r = a/b`, divide both `a` and `b` by the greatest common divisor (GCD) of `a` and `b`.
For example, `GCD(12, 8) = 4`, so `r = 12/8` should be reduced to `(12/4) / (8/4) = 3/2`.

The reduced fraction should be in "standard form" meaning the denominator must always be a positive integer.
If the denominator is negative, multiply both the numerator and denominator by `-1` to achieve standard form.
For example, `3/-4` should be written as `-3/4`.

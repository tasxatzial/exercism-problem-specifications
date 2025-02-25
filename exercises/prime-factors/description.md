# Description

Compute the [**prime factors**][integer-factorization] of a given natural number.

* Natural numbers are the whole numbers that are greater than or equal to 1 (1, 2, 3, ...).
* A prime number is a natural number greater than 1 that is only divisible by itself and 1.
* The number `x` is a prime factor of number `y` if `x` is a prime number and divides `y`.

Note that when we use the words _divisible_ and _divides_, we mean division in a mathematical sense, where the result is a whole number without any remainder.

## Example

### What are the prime factors of 60?

We need to find the **prime numbers** that divide 60.

#### Step 1: Divide by 2 (the smallest prime)

- 60 is divisible by 2, so we divide:

```text
  60 ÷ 2 = 30 ➜ Factor found: 2
```

- 30 is still divisible by 2, so we divide by 2 again:

```text
  30 ÷ 2 = 15 ➜ Factor found: 2
```

- 15 is **not** divisible by 2, so we stop dividing by 2.

#### Step 2: Divide by 3 (the next prime)

- 15 is divisible by 3, so we divide:

```text
  15 ÷ 3 = 5 ➜ Factor found: 3
```

- 5 is **not** divisible by 3, so we stop dividing by 3.

#### Step 3: Divide by 5 (the next prime)

- 5 is divisible by 5, so we divide:

```text
  5 ÷ 5 = 1 ➜ Factor found: 5
```

Since we've reached **1**, we're done!

### Final Answer

The prime factors of **60** are **2, 2, 3, and 5**.

### Verification

Let's multiply the prime factors to check if we get back to 60:

```text
2 × 2 × 3 × 5 = 60
```

Since the product is 60, our prime factorization is correct!

[integer-factorization]: https://en.wikipedia.org/wiki/Integer_factorization

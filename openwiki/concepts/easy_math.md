---
type: module
title: easy_math
description: A collection of beginner-friendly utility functions for common mathematical operations.
tags: [python, math, utility, beginner-friendly]
verified:
  - by: openwiki/0.5.1
    at: 2026-10-02T10:05:03.134Z
sources:
  - id: openwiki-source-fd42d82e0d9df310748c0c5b
    resource: repo://py_simple_package/src/py_simple/easy_math.py
  - id: openwiki-source-681159c72987c1cb03ad99ef
    resource: repo://tests/test_math.py
generated: { by: "openwiki/0.5.1", at: "2026-10-02T10:05:03.134Z" }
---

# easy_math

The `easy_math` module provides a suite of simplified, intuitive helper functions for performing common mathematical calculations. It is designed for developers who need reliable implementations of mathematical routines without the complexity of low-level boilerplate code.

## Main Functions

The module includes functions for number theory, sequence generation, and general calculations:

- **Number Theory & Properties**: 
    - `get_least_common_multiple(a, b)`: Computes the LCM of two integers.
    - `divisors(n)`: Returns a list of divisors for a given number.
    - `is_perfect_square(n)`: Checks if a number is a perfect square.
    - `is_armstrong_number(n)`: Checks if a number is an Armstrong number.
    - `is_abundant_number(n)`: Determines if a number is abundant.
    - `is_harshad_number(n)`: Checks if a number is a Harshad (or Niven) number.
    - `prime_factorization(n)`: Returns the prime factors of a number.

- **Sequence Generation**:
    - `factorial(n)`: Calculates the factorial of a non-negative integer.
    - `fibonacci(count)`: Generates the first `count` numbers of the Fibonacci sequence.
    - `collatz_sequence(n)`: Produces the Collatz sequence starting at `n`.

- **General Calculations**:
    - `sum_of_digits(n)`: Returns the sum of the digits of a number.
    - `digit_count(n)`: Counts the number of digits in an integer.
    - `calculate_simple_interest(principal, rate, time)`: Computes simple interest.
    - `distance_between_points(p1, p2)`: Calculates the Euclidean distance between two points.

## Tests

The `easy_math` module is validated through a comprehensive suite of tests located at `repo://tests/test_math.py`. These tests cover edge cases and verify the accuracy of each mathematical helper function.

## Integration

`easy_math` is a fundamental module within the `py_simple` ecosystem. It is often used in conjunction with:

<!-- openwiki: broken internal link [/concepts/easy_numbers.md] file "/concepts/easy_numbers.md" does not exist. Fix the href or restore the target, then delete this comment. -->
- [`easy_numbers`](/concepts/easy_numbers.md): For further number-related utilities.
<!-- openwiki: broken internal link [/concepts/easy_stats.md] file "/concepts/easy_stats.md" does not exist. Fix the href or restore the target, then delete this comment. -->
- [`easy_stats`](/concepts/easy_stats.md): For statistical analysis.

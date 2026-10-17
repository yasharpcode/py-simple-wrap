---
type: module
title: easy_math
description: A collection of beginner-friendly utility functions for common mathematical operations.
tags: [python, math, utility, beginner-friendly]
sources:
  - id: openwiki-source-fd42d82e0d9df310748c0c5b
    resource: repo://py_simple_package/src/py_simple/easy_math.py
  - id: openwiki-source-681159c72987c1cb03ad99ef
    resource: repo://tests/test_math.py
generated: { by: "openwiki/0.5.1", at: "2026-10-17T08:11:38.702Z" }
verified:
  - by: openwiki/0.5.1
    at: 2026-10-17T08:11:38.702Z
---

# easy_math

The `easy_math` module provides a suite of simplified, intuitive helper functions for performing common mathematical calculations. It is designed for developers who need reliable implementations of mathematical routines without the complexity of low-level boilerplate code.

## Purpose

The primary purpose of `easy_math` is to offer mathematical utilities that abstract away boilerplate, making common numerical tasks more readable and easier to implement.

## Main Functions

The module includes functions for number theory, sequence generation, and general calculations:

- **Number Theory & Properties**: 
    - `get_least_common_multiple(a, b)`: Computes the LCM of two integers.
    - `divisors(n)`: Returns a list of divisors for a given number.
    - `is_perfect_square(n)`: Checks if a number is a perfect square.
    - `is_armstrong_number(n)`: Checks if a number is an Armstrong number.
    - `is_abundant_number(n)`: Determines if a number is abundant.
    - `is_harshad_number(n)`: Checks if a number is a Harshad (or Niven) number.
    - `is_triangular_number(n)`: Checks if a number is a triangular number.
    - `is_power_of_two(n)`: Checks if a number is a power of two.
    - `prime_factorization(n)`: Returns the prime factors of a number.

- **Sequence Generation & Manipulation**:
    - `factorial(n)`: Calculates the factorial of a non-negative integer.
    - `fibonacci(count)`: Generates the first `count` numbers of the Fibonacci sequence.
    - `collatz_sequence(n)`: Produces the Collatz sequence starting at `n`.
    - `reverse_digits(n)`: Reverses the digits of an integer.

- **General Calculations**:
    - `sum_of_digits(n)`: Returns the sum of the digits of a number.
    - `digit_count(n)`: Counts the number of digits in an integer.
    - `calculate_simple_interest(principal, rate, time)`: Computes simple interest.
    - `distance_between_points(x1, y1, x2, y2)`: Calculates the Euclidean distance between two points.
    - `midpoint(x1, y1, x2, y2)`: Calculates the midpoint between two 2D points.
    - `sum_of_squares(numbers)`: Calculates the sum of squares of a list of numbers.
    - `weighted_average(values, weights)`: Calculates the weighted average.
    - `keep_in_range(value, minimum, maximum)`: Limits a value to a range.
    - `cube_value(x)`: Returns the cube of a number.

## Tests

The `easy_math` module is validated through a comprehensive suite of tests located at `repo://tests/test_math.py`. These tests cover edge cases and verify the accuracy of each mathematical helper function.

## Related Modules

<!-- openwiki: broken internal link [/concepts/easy_modules.md] file "/concepts/easy_modules.md" does not exist. Fix the href or restore the target, then delete this comment. -->
- [easy_modules](/concepts/easy_modules.md) (Back-link)
<!-- openwiki: broken internal link [/concepts/easy_strings.md] file "/concepts/easy_strings.md" does not exist. Fix the href or restore the target, then delete this comment. -->
- [easy_strings](/concepts/easy_strings.md)
<!-- openwiki: broken internal link [/concepts/easy_json.md] file "/concepts/easy_json.md" does not exist. Fix the href or restore the target, then delete this comment. -->
- [easy_json](/concepts/easy_json.md)

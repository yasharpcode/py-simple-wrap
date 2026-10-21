---
type: concept
title: easy_json
description: A utility module designed to simplify common JSON file operations and data manipulation with consistent error handling.
tags: [json, utility, py_simple]
sources:
  - id: openwiki-source-942619f3d8244bc55818b59a
    resource: repo://py_simple_package/src/py_simple/easy_json.py
  - id: openwiki-source-66f9bdfbd018181ae2f17579
    resource: repo://tests/test_json.py
generated: { by: "openwiki/0.5.1", at: "2026-10-02T10:48:26.598Z" }
---

The `easy_json` module is a part of the `py_simple` package, providing a streamlined interface for interacting with JSON files and data structures. It focuses on reducing boilerplate code and implementing robust, uniform error handling using a custom exception class.

## Purpose

Working with standard JSON libraries in Python can often lead to repetitive `try-except` blocks or verbose file handling code. `easy_json` abstracts these operations, allowing developers to read, write, and safely inspect JSON data efficiently.

## Core Responsibilities

- **Simplified I/O**: Provides high-level functions for opening and saving JSON files.
- **Consistent Error Handling**: Wraps standard library exceptions in `EasyJsonError`, ensuring that file-system or syntax issues are reported in a predictable, developer-friendly way.
- **Data Navigation**: Offers utility functions for safely accessing nested data within dictionaries or lists.

## Main Functions

The module provides several key utilities:

- `open_json(filepath)`: Reads a JSON file into a Python dictionary.
- `save_json_data(filepath, data)`: Writes dictionary data to a JSON file.
- `get_nested(data, path, default)`: Safely retrieves values from deep within dictionaries or lists using a dot-separated string (e.g., `"users.0.name"`).

## Error Handling

All operations that interact with the file system or parse JSON content utilize the `EasyJsonError` exception. This ensures that when an error occurs—such as a missing file, invalid syntax, or permission restriction—the developer receives a clear, consistent error message without needing to catch multiple underlying Python exceptions.

## Tests

The module's reliability is validated through comprehensive unit tests located in `tests/test_json.py`. These tests cover:
- Successful reading and writing of JSON files.
- Appropriate error propagation for missing files, invalid syntax, and invalid file paths.
- Correct behavior of utility functions like `get_nested`.

## See Also

- [easy_modules](repo://openwiki/concepts/easy_modules.md)
- [easy_strings](repo://openwiki/concepts/easy_strings.md)
- [easy_math](repo://openwiki/concepts/easy_math.md)

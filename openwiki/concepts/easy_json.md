---
type: concept
title: easy_json
description: A utility module designed to simplify common JSON file operations and data manipulation with consistent error handling.
tags: [json, utility, py_simple]
verified:
  - by: openwiki/0.5.1
    at: 2026-10-17T08:11:38.702Z
sources:
  - id: openwiki-source-942619f3d8244bc55818b59a
    resource: repo://py_simple_package/src/py_simple/easy_json.py
  - id: openwiki-source-66f9bdfbd018181ae2f17579
    resource: repo://tests/test_json.py
generated: { by: "openwiki/0.5.1", at: "2026-10-17T08:11:38.702Z" }
---

The `easy_json` module is a part of the `py_simple` package, providing a streamlined interface for interacting with JSON files and data structures. It focuses on reducing boilerplate code and implementing robust, uniform error handling using a custom exception class, `EasyJsonError`.

## Core Responsibilities

- **Simplified I/O**: Provides high-level functions for opening and saving JSON files, including support for file updates and pretty-printing.
- **Consistent Error Handling**: Wraps standard library exceptions (e.g., file system or parsing errors) in `EasyJsonError`, ensuring that failures are reported in a predictable manner.
- **Data Inspection and Manipulation**: Offers utilities for navigating, flattening, and comparing JSON structures.

## Main Functions

- **File Operations**:
    - `open_json(filepath)`: Reads a JSON file into a Python dictionary.
    - `save_json_data(filepath, data)`: Writes dictionary data to a JSON file (prevents accidental overwriting).
    - `update_json(filepath, new_data)`: Merges new data into an existing JSON file.
    - `is_json_file(filepath)`: Validates if a file exists and has a `.json` extension.

- **Data Utilities**:
    - `get_nested(data, path, default)`: Safely retrieves values from deep within dictionaries or lists using a dot-separated string (e.g., `"users.0.name"`).
    - `pretty_json(data=None, filepath=None)`: Returns a pretty-printed JSON string.
    - `get_json_keys(data=None, filepath=None)`: Returns the top-level keys.
    - `is_nested_json(data=None, filepath=None)`: Checks for nested structures at the top level.
    - `flatten_json(seperator="-", data=None, filepath=None)`: Flattens nested data into a single-level dictionary.
    - `compare_json(data1=None, data2=None, filepath1=None, filepath2=None)`: Compares two JSON structures and reports added, removed, or changed values.

## Error Handling

All operations that interact with the file system or parse JSON content raise `EasyJsonError` upon failure. This abstracts the specific underlying Python exception (e.g., `FileNotFoundError`, `json.JSONDecodeError`), allowing callers to catch a single error type.

## Testing

The module's reliability is validated through unit tests in `tests/test_json.py`, which cover:
- Successful file I/O operations and round-trips.
- Correct behavior of data manipulation functions (e.g., `get_nested`, `flatten_json`, `compare_json`).
- Consistent propagation of `EasyJsonError` across all failure scenarios (missing files, invalid syntax, invalid inputs).

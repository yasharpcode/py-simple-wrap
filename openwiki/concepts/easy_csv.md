---
type: concept
title: easy_csv
description: A utility module for simplifying CSV file operations, providing intuitive methods to read from and write to CSV formats with minimal boilerplate.
tags: [csv, data-processing, py_simple]
verified:
  - by: openwiki/0.5.1
    at: 2026-10-17T08:11:38.702Z
sources:
  - id: openwiki-source-7cecb222a3e32477132f3be0
    resource: repo://py_simple_package/src/py_simple/easy_csv.py
generated: { by: "openwiki/0.5.1", at: "2026-10-17T08:11:38.702Z" }
---

`easy_csv` is a submodule of `py_simple` designed to streamline CSV file handling in Python. It abstracts away common file I/O operations associated with the standard `csv` module, such as managing file openers, encoding, and dictionary-based data extraction.

## Functionality

The module provides two primary functions for handling CSV data:

### Reading CSV Files
`read_csv_to_list` enables easy retrieval of CSV content into Python data structures.

- **`return_dict`**: When `True` (default), the module uses the first row of the CSV as headers, returning a list of dictionaries mapping header names to row values. When `False`, it returns a list of lists.
- **`delimiter`**: Allows customization of the field separator (default is `,`).

### Writing CSV Files
`write_csv_from_list` facilitates writing Python lists (of dicts or lists) back to CSV files.

- **Data structures**: It natively supports lists of dictionaries (using keys as headers) or simple lists of lists (optionally requiring a separate `headers` list).
- **`delimiter`**: Allows customization of the field separator.

## Implementation Details

The module relies on the standard library `csv` module and `os.path` for file validation. It enforces `utf-8` encoding by default and properly handles the `newline=""` argument required for robust cross-platform CSV handling.

### Key Characteristics
- **Safety**: Raises `FileNotFoundError` if the specified file does not exist, and `ValueError` if the file is empty.
- **Simplicity**: Significantly reduces the lines of code required for repetitive CSV I/O patterns.

## Example Usage

```python
from py_simple import read_csv_to_list, write_csv_from_list

# Reading
data = read_csv_to_list(filepath="people.csv")
print(data[0])  # {'Name': 'Alice', 'Age': '24'}

# Writing
people = [
    {"Name": "Alice", "Age": "24"},
    {"Name": "Bob", "Age": "30"}
]
write_csv_from_list(filepath="output.csv", data=people)
```

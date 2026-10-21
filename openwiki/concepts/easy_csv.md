<okf_front_matter>
---
type: Reference
title: easy_csv
description: A module to simplify reading and writing CSV files.
tags: [csv, data-processing]
---
</okf_front_matter>

# easy_csv

`easy_csv` simplifies the process of reading and writing CSV files in Python by providing higher-level abstractions over standard library functions.

## Main functions

- `read_csv_to_list`: Reads a CSV file and returns its content as a list of dictionaries or lists.
  ```python
  data = read_csv_to_list(filepath="data.csv")
  ```

## Related modules

- [easy_file_manager](easy_file_manager.md)
- [easy_archive](easy_archive.md)

## Back-link

[Easy Modules](index.md)

## Tests

The `tests/test_easy_csv.py` file covers file reading, CSV parsing, and error handling for empty or non-existent files.

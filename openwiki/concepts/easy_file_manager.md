<okf_front_matter>
---
type: Reference
title: easy_file_manager
description: A module to simplify common file system operations.
tags: [file-io, file-system]
---
</okf_front_matter>

# easy_file_manager

`easy_file_manager` provides simplified utilities for common file system operations, such as checking for file existence.

## Main functions

- `is_file_there`: Checks if a file exists in the current working directory.
  ```python
  exists = is_file_there("data.txt")
  ```

## Related modules

- [easy_csv](easy_csv.md)
- [easy_archive](easy_archive.md)

## Back-link

[Easy Modules](index.md)

## Tests

The `tests/test_easy_file_manager.py` file covers file existence checks and error handling for invalid operations.

<okf_front_matter>
---
type: Reference
title: easy_archive
description: A utility module for simplifying the creation and management of ZIP archives in Python.
tags: [python, utilities, file-management, zip]
---
</okf_front_matter>

The `easy_archive` module provides a simplified interface for zipping and unzipping files and folders, abstracting away the boilerplate code typically required when using the standard `zipfile` library.

## Main Functions

*   **`zip_folder(folder_path, zip_name=None)`**: Compresses an entire directory into a `.zip` file.
    ```python
    from py_simple.easy_archive import zip_folder
    zip_folder("my_data")  # Creates 'my_data.zip'
    ```

*   **`zip_files(file_paths, zip_name)`**: Creates an archive from a specific list of files.
    ```python
    from py_simple.easy_archive import zip_files
    zip_files(["data1.txt", "data2.txt"], "archive.zip")
    ```

## Related modules

- [easy_csv](easy_csv.md)
- [easy_file_manager](easy_file_manager.md)

## Back-link

[Easy Modules](index.md)

## Tests

The `tests/test_archive.py` file covers edge cases such as missing source files, invalid file extensions, and path handling.

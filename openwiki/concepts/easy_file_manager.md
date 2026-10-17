---
type: module
title: easy_file_manager
description: A simplified, restricted file manipulation utility for basic operations on specific file types.
tags: [python, file-management, simplicity, utilities]
verified:
  - by: openwiki/0.5.1
    at: 2026-10-17T08:11:38.702Z
sources:
  - id: openwiki-source-83f3147379f5afb734507230
    resource: repo://py_simple_package/src/py_simple/easy_file_manager.py
generated: { by: "openwiki/0.5.1", at: "2026-10-17T08:11:38.702Z" }
---

`easy_file_manager` is a Python module designed to simplify common file system operations by providing an abstraction layer over standard library modules like `os` and `shutil`. It enforces a strict set of allowed file extensions and manages errors consistently through a specialized exception class.

## Overview

The module prioritizes safety and simplicity, explicitly limiting operations to files with the following extensions: `.txt`, `.md`, `.log`, and `.csv`. This makes it ideal for lightweight tasks where maintaining a consistent environment and preventing accidental overwrites or operations on unknown file types is desirable.

## Key Features

* **Safety Checks**: Every operation validates that the target file extension is supported and that files do not accidentally overwrite existing ones.
* **Simplified API**: Provides one-line alternatives to common file patterns (e.g., creating blank files, appending lines, or reading file contents).
* **Consistent Error Handling**: Uses the `EasyFileManagerError` custom exception for descriptive reporting when an operation fails.

## Core Functions

* `is_file_there(filename)`: Checks for the existence of a file in the current working directory.
* `make_blank_file(filename, file_extension)`: Creates a new, empty file if one does not already exist.
* `add_a_line(filename, line)`: Appends a string to a file, creating it if it is missing.
* `read_file_to_list(filename)`: Reads an existing file and returns its content as a list of trimmed lines.
* `remove_file(filename)`: Deletes a specified file.
* `rename_file(old_name, new_name)`: Safely renames a file.
* `list_files(extension=None)`: Retrieves a sorted list of files matching the allowed extensions, with an optional filter.
* `copy_file(source, destination)`: Duplicates an existing file to a new destination.

## Usage Example

The following example demonstrates how to create a file, write content to it, and read it back.

```python
from py_simple import make_blank_file, add_a_line, read_file_to_list

# Create a file
make_blank_file("notes", "txt")

# Append data
add_a_line("notes.txt", "First line of content.")
add_a_line("notes.txt", "Second line of content.")

# Read data
lines = read_file_to_list("notes.txt")
print(lines) # Output: ['First line of content.', 'Second line of content.']
```

## Error Handling

The module raises `EasyFileManagerError` for violations such as unsupported file extensions, missing files during read/delete operations, or attempting to overwrite an existing file during a creation or copy process.

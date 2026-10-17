---
type: concept
title: easy_archive
description: A module simplifying ZIP archive operations by providing high-level wrappers around Python's standard library.
tags: [python, utilities, archive, zip]
verified:
  - by: openwiki/0.5.1
    at: 2026-10-17T08:11:38.702Z
sources:
  - id: openwiki-source-6046bd5b287516b6c7317d1d
    resource: repo://py_simple_package/src/py_simple/easy_archive.py
generated: { by: "openwiki/0.5.1", at: "2026-10-17T08:11:38.702Z" }
---

`easy_archive` is a utility module within the `py_simple` package designed to abstract and simplify common ZIP archive operations. It provides a safer and more convenient interface for creating, reading, and modifying ZIP files compared to standard library calls.

## Overview
The module centralizes file and directory archiving, including specialized handling for naming conflicts and common validation tasks. All operations are designed to be intuitive and require minimal boilerplate.

## Key Functionality

### Creating Archives
* **`zip_folder(folder_path, zip_name=None)`**: Archives an entire directory structure. By default, it generates a filename based on the folder name.
* **`zip_files(file_paths, zip_name)`**: Archives a list of specific files. If multiple files share the same name (even if they reside in different source directories), it automatically renames them to prevent data loss.

### Inspecting and Modifying
* **`unzip_file(zip_path, destination=".")`**: Extracts the entire contents of a ZIP file into a specified destination, automatically creating the directory if it is missing.
* **`extract_file_from_zip(zip_path, filename, destination=".")`**: Retrieves a single file from an archive.
* **`add_to_zip(zip_path, file_to_add)`**: Appends a file to an existing archive.
* **`list_zip_contents(zip_path)`**: Returns a list of all items currently stored in an archive.
* **`get_zip_file_count(zip_path)`**: Returns the total number of items in an archive.
* **`is_zip_file(path)`**: Validates if a given path is a readable ZIP file.

## Error Handling
The module defines `EasyArchiveError`, a custom exception class used to report failures during archive operations, such as missing files, invalid formats, or destination access errors.

## Design Invariants
- **Validation**: All modification and extraction functions verify the existence and integrity of ZIP files before processing.
- **Extension Enforcement**: Methods requiring an archive destination enforce the `.zip` file extension to ensure consistency.
- **Conflict Resolution**: The `zip_files` method proactively manages filename collisions, ensuring that files from different locations with identical names are preserved under unique, descriptive names within the archive.

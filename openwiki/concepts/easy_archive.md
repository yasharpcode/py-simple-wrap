---
type: concept
title: easy_archive
description: A utility module for simplifying file and folder compression and extraction tasks using the ZIP format.
tags: [python, compression, archive, filesystem, utility]
verified:
  - by: openwiki/0.5.1
    at: 2026-10-02T11:02:08.372Z
sources:
  - id: openwiki-source-6046bd5b287516b6c7317d1d
    resource: repo://py_simple_package/src/py_simple/easy_archive.py
generated: { by: "openwiki/0.5.1", at: "2026-10-02T11:02:08.372Z" }
---

The `easy_archive` module provides high-level abstractions over Python's standard `zipfile` library. Its primary goal is to minimize boilerplate code for common archival tasks, such as zipping entire directories or extracting archives, while providing safer defaults and automatic error handling.

## Purpose

`easy_archive` aims to replace complex, multi-step `zipfile` implementations with intuitive, single-call functions. It is designed for developers who need to perform basic archival operations without manually managing file walks or stream closures.

## Core Functions

- **`zip_folder(folder_path, zip_name=None)`**: Recursively compresses an entire directory into a `.zip` file. If no name is provided, it defaults to the folder name with the `.zip` extension.
- **`zip_files(file_paths, zip_name)`**: Compresses a specific list of files into a single archive. It handles file naming conflicts internally (e.g., if multiple files share the same name) to prevent accidental data overwriting.
- **`unzip(zip_path, extract_to=".")`**: Extracts the contents of a zip file to a specified directory.

## Mechanisms and Control Flow

- **Constraint Enforcement**: The module uses `_ensure_zip_extension` to validate that all output archive names end with the expected `.zip` extension, raising `EasyArchiveError` otherwise.
- **Conflict Resolution**: In `zip_files`, the module tracks names added to the archive to handle path collisions, ensuring that files from different source directories with the same filename are preserved uniquely within the zip structure.
- **Error Handling**: `EasyArchiveError` serves as a custom exception class for handling common failure states, such as missing source directories or invalid archive paths.

## Relationships

- **Related Modules**: Operates closely with `easy_file_manager` for path resolution and file system traversal.
- **Dependency**: Built atop the standard library `zipfile` and `os` modules.

## Testing Focus

Testing for `easy_archive` should prioritize:
1. **Recursion Accuracy**: Verifying that `zip_folder` correctly preserves the directory structure, including nested sub-folders.
2. **Conflict Handling**: Ensuring that `zip_files` gracefully handles files with identical basenames from different locations.
3. **Validation**: Confirming that invalid archive names or missing source paths trigger the expected `EasyArchiveError`.
4. **Integration**: Ensuring correct extraction of archives created by the module back to their original state (round-trip testing).

---
*For more information on general file operations, see the main [Py_simple](repo://py_simple_package/src/py_simple/__init__.py) concept page.*

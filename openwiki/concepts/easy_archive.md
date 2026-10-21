---
type: concept
title: easy_archive
description: A utility module for simplifying the creation, management, and extraction of .zip archives in Python.
tags: [python, file-management, zip, archiving]
verified:
  - by: openwiki/0.5.1
    at: 2026-10-21T08:23:23.109Z
sources:
  - id: openwiki-source-6046bd5b287516b6c7317d1d
    resource: repo://py_simple_package/src/py_simple/easy_archive.py
generated: { by: "openwiki/0.5.1", at: "2026-10-21T08:23:23.109Z" }
---

`easy_archive` is a Python module designed to simplify common file archiving tasks. It provides a high-level wrapper around Python's standard `zipfile` library, offering more intuitive interfaces for zipping folders, combining individual files, and inspecting or extracting archive contents.

## Overview

The module streamlines operations that typically require manual iteration over directory trees or explicit management of `zipfile.ZipFile` handles.

### Core Features

*   **Folder Archiving:** Recursively zip entire directory structures into a single file with simplified default naming conventions.
*   **File Aggregation:** Zip multiple specific files into an archive, with automatic handling of potential name collisions if files share filenames from different source directories.
*   **Content Inspection:** Methods for listing contents, verifying file existence within an archive, and checking counts.
*   **Extraction:** Streamlined extraction workflows.

## Relationships

*   **[easy_modules](/openwiki/concepts/easy_modules.md):** The primary registry for modular tools in the `py_simple` ecosystem.
<!-- openwiki: broken internal link [/openwiki/concepts/easy_csv.md] file "/openwiki/concepts/easy_csv.md" does not exist. Fix the href or restore the target, then delete this comment. -->
*   **[easy_csv](/openwiki/concepts/easy_csv.md):** Often used in conjunction when archiving generated CSV data sets.
<!-- openwiki: broken internal link [/openwiki/concepts/easy_file_manager.md] file "/openwiki/concepts/easy_file_manager.md" does not exist. Fix the href or restore the target, then delete this comment. -->
*   **[easy_file_manager](/openwiki/concepts/easy_file_manager.md):** Provides the underlying directory and file path management utilities that `easy_archive` leverages to ensure cross-platform path handling.

## Usage

### Examples

#### Zipping a Folder
The `zip_folder` function simplifies recursive archiving. If no output name is provided, it defaults to the directory name with a `.zip` extension.

```python
from py_simple.easy_archive import zip_folder

# Zips 'my_project' into 'my_project.zip'
zip_folder("my_project")
```

#### Zipping Specific Files
When zipping a list of files, the module automatically resolves filename conflicts, ensuring no data is lost during the compression process.

```python
from py_simple.easy_archive import zip_files

# Zips specific files into a named archive
zip_files(["data/report.pdf", "configs/settings.json"], "backup.zip")
```

## Error Handling

All operations are guarded by the `EasyArchiveError` exception class. This is raised in scenarios such as:

*   Attempting to archive non-existent files or directories.
*   Targeting a path that does not end in the `.zip` extension.
*   Providing an empty list of files for the `zip_files` operation.

## Testing

The module is validated by a comprehensive suite of tests (see `tests/test_archive.py`) that verify:

*   **Consistency:** Proper relative path structures within created archives.
*   **Resilience:** Correct handling of missing source files and directory navigation (e.g., using `.` as an input).
*   **Safety:** Enforcement of expected file extensions (`.zip` only) and protection against overwriting the archive file with itself during the compression process.

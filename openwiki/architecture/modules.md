---
type: module
title: Module Architecture
description: Overview of the supported modules and their primary functionalities in the py_simple package.
tags: [python, architecture, modules, documentation]
verified:
  - by: openwiki/0.5.1
    at: 2026-10-01T20:13:54.935Z
sources:
  - id: openwiki-source-942619f3d8244bc55818b59a
    resource: repo://py_simple_package/src/py_simple/easy_json.py
  - id: openwiki-source-fd42d82e0d9df310748c0c5b
    resource: repo://py_simple_package/src/py_simple/easy_math.py
  - id: openwiki-source-f2f5b73375793cffe298f0eb
    resource: repo://py_simple_package/src/py_simple/easy_strings.py
generated: { by: "openwiki/0.5.1", at: "2026-10-01T20:13:54.935Z" }
---

# Module Architecture

The `py_simple` package provides a suite of modules designed to simplify common programming tasks. Each module focuses on a specific domain, offering beginner-friendly wrappers and utility functions.

## Overview of Core Modules

This section details the most frequently used modules within the `py_simple` ecosystem.

| Module | Purpose | Primary Utility Functions |
| :--- | :--- | :--- |
| `easy_strings` | Simplifies common string manipulation tasks. | `remove_extra_spaces`, `to_snake_case`, `to_kebab_case`, `to_camel_case` |
| `easy_math` | Provides helpful wrappers for common mathematical operations. | `get_least_common_multiple`, `factorial`, `fibonacci` |
| `easy_json` | Streamlines reading, writing, and querying JSON data. | `open_json`, `save_json_data`, `get_nested` |

## Module Details

### easy_strings
The `easy_strings` module is intended for common string manipulation tasks. It provides abstraction layers for complex operations like text formatting, case conversion, and normalization.

### easy_math
The `easy_math` module offers simplified interfaces for common mathematical operations that might otherwise require more boilerplate code or imports. It handles edge cases and common error scenarios automatically, providing a smoother developer experience.

### easy_json
The `easy_json` module serves as an abstraction for handling JSON files. It simplifies I/O operations and provides safe ways to query nested JSON structures using simple dot-notation strings, reducing the need for explicit manual error handling and type checking.

---

For further details on how to use these modules in your projects, refer to the [Quickstart Guide](/openwiki/quickstart.md) or explore the [Testing Guide](/openwiki/testing/testing_guide.md) to see how these modules are validated.

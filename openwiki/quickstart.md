---
type: index
title: Quickstart Guide
description: Entry point for the py_simple ecosystem, providing an overview of core modules and development principles.
tags: [introduction, documentation, quickstart, overview]
verified:
  - by: openwiki/0.5.1
    at: 2026-10-02T10:05:03.134Z
sources:
  - id: openwiki-source-942619f3d8244bc55818b59a
    resource: repo://py_simple_package/src/py_simple/easy_json.py
  - id: openwiki-source-fd42d82e0d9df310748c0c5b
    resource: repo://py_simple_package/src/py_simple/easy_math.py
  - id: openwiki-source-f2f5b73375793cffe298f0eb
    resource: repo://py_simple_package/src/py_simple/easy_strings.py
  - id: openwiki-source-d5322b69be93b3d4e5ca555e
    resource: repo://tests/test_file_manager.py
  - id: openwiki-source-c539264d96229140719addde
    resource: repo://tests/test_sql.py
generated: { by: "openwiki/0.5.1", at: "2026-10-02T10:05:03.134Z" }
---

# Quickstart Guide

Welcome to the `py_simple` documentation. This guide provides a high-level entry point to the library, its design philosophy, and the core modules that simplify common Python development tasks.

## Getting Started

To explore the library, we recommend navigating through the following areas:

*   **[Module Map](/openwiki/concepts/module_map.md)**: A central index of all available modules.
*   **[Easy Modules Concept](/openwiki/concepts/easy_modules.md)**: Learn about the design pattern used to create beginner-friendly wrappers.

## Core Modules

The library is organized around the `easy_*` family of modules, which provide simplified interfaces for frequent tasks:

| Module | Description |
| :--- | :--- |
| [easy_strings](/openwiki/concepts/easy_strings.md) | Simplifies common string manipulation, cleaning, and formatting. |
| [easy_math](/openwiki/concepts/easy_math.md) | Intuitive wrappers for common mathematical operations. |
| [easy_json](/openwiki/concepts/easy_json.md) | Simplifies JSON file handling with standardized error reporting. |

## Design Philosophy

`py_simple` is built on three core pillars:

1.  **Reduce Boilerplate**: We abstract away complex setups for repetitive, common tasks.
2.  **Improve Readability**: Our API design prioritizes clarity, aiming for function signatures that read like plain English.
3.  **Ensure Safety**: We utilize standardized exceptions to provide clear, actionable feedback when operations fail, ensuring your applications remain robust.

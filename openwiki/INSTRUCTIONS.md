# Wiki brief

A code wiki for the Python library in py_simple_package/src/py_simple and its tests in tests/.
Ignore the landing site, docs build, module-book, scripts, and JavaScript tooling.

## Audience

A developer new to Python who wants to know what each module does and how modules relate.

## Work in phases

Only write pages for the modules in the CURRENT PHASE. Do not rewrite pages from other phases.
Edit an existing page only to add links to new pages.

CURRENT PHASE: 1

- Phase 1: easy_strings, easy_math, easy_json
- Phase 2: easy_csv, easy_file_manager, easy_archive
- Phase 3: easy_converter, easy_sql, easy_config
- Phase 4: easy_lists, easy_dict, easy_stats
- Phase 5: easy_logging, easy_validator, easy_regex

## One page per module

Write each page at concepts/<module_name>.md (for example concepts/easy_csv.md).
Keep every page under 40 lines. Include:

1. Purpose, in two or three sentences.
2. Main functions: a short list with one line each and one tiny example.
3. Related modules: links to at least two other module pages that genuinely connect.
4. Back-link: a link to the Easy Modules concept page.
5. Tests: what the matching test file covers, in one or two lines.

## Linking rules (important)

- Use relative Markdown links in the same style as the existing pages.
- Create concepts/module_map.md once. It must link to every module page that exists.
  In each later phase, only add links to it for the new pages.
- Update the Easy Modules concept page only to link to module_map.md and the new pages.
- If a page links to a module whose page does not exist yet, skip that link.

## Accuracy rules

- Describe only what exists in the source code. Do not invent functions.
- Prefer short pages that finish over long pages that might not.

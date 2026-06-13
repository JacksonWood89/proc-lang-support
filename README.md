# Pro*C/C++ Language Support

Syntax highlighting, snippets, and language configuration for Oracle **Pro\*C/C++** embedded-SQL source files (`.pc`, `.pcc`).

Pro\*C/C++ is Oracle's precompiler that lets you embed SQL and PL/SQL inside C/C++ source. This extension understands both layers — the host C/C++ code **and** the `EXEC SQL` / `EXEC ORACLE` embedded blocks — so the whole file reads cleanly.

## Features

- **Embedded SQL highlighting** — `EXEC SQL` and `EXEC ORACLE` blocks are scoped distinctly from the surrounding C/C++ code.
- **Host variables** — `:var` and `:var:indicator` references are highlighted inside SQL.
- **Broad SQL coverage** — DML, DDL, TCL, cursor operations, dynamic SQL, `WHENEVER` directives, 100+ functions, and 60+ Oracle/SQL types.
- **Oracle-specific constructs** — `BULK COLLECT`, `CONNECT BY`, `PRIOR`, `ROWNUM`, `PIVOT`/`UNPIVOT`, `FORALL`, `FLASHBACK`, and more.
- **Full C/C++ support** — preprocessor directives, comments, strings with escape sequences, keywords, types (including `SQLCA`, `SQLDA`, `VARCHAR`, and OCI types), numeric literals, and operators.
- **12 snippets** for the most common embedded-SQL patterns.
- **Language configuration** — comment toggling and auto-closing brackets/quotes.

## Snippets

| Prefix | Description |
|--------|-------------|
| `sqlsel` | `SELECT ... INTO` host variables |
| `sqlins` | `INSERT` statement |
| `sqlupd` | `UPDATE` statement |
| `sqldel` | `DELETE` statement |
| `sqlcursor` | Full cursor declare/open/fetch-loop/close pattern |
| `sqlcheck` | `SQLCA` error check |
| `sqlwhenever` | `WHENEVER` directives |
| `sqlconnect` | Database `CONNECT` |
| `sqlcommit` | `COMMIT` |
| `sqlrollback` | `ROLLBACK` |
| `sqldecl` | Host variable `DECLARE SECTION` |
| `sqlbulk` | `BULK COLLECT` cursor fetch |

## Supported file extensions

- `.pc` — Pro\*C/C++ source
- `.pcc` — Pro\*C/C++ source

## Installation

Install from the VS Code Marketplace (search for "Pro\*C/C++ Language Support"), or build from source:

```sh
npm install -g @vscode/vsce
vsce package
code --install-extension proc-language-support-0.1.0.vsix
```

## Notes

This is a **syntax-only** extension — it provides highlighting, snippets, and editor configuration. It does not compile, run, or validate Pro\*C code.

## License

[MIT](LICENSE)

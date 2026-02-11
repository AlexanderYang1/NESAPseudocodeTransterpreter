# NESAPseudocodeTransterpreter

A procedural transterpreter for NESA-style pseudocode.

## What it does

1. Reads NESA pseudocode from an input file.
2. Translates it to Python 3.
3. Writes the generated Python to `a.py` (default).
4. Runs `a.py`.

## Supported constructs

- `BEGIN ... END`
- assignment (`=`)
- `GET` / `READ`
- `DISPLAY` / `OUTPUT`
- `IF ... THEN ... ELSE ... ENDIF`
- `FOR ... TO ... NEXT`
- `WHILE ... ENDWHILE` (including optional trailing `DO`)
- `REPEAT ... UNTIL`
- `CASEWHERE ... is ... ENDCASE` with `Otherwise`
- `RETURN`
- operators: `<>`, `AND`, `OR`, `NOT`, `TRUE`, `FALSE`

## Usage

```bash
python3 transterpreter.py <input.pseudo>
```

Options:

- `--output <path>`: write generated Python to a custom file path.
- `--no-run`: generate only, do not execute the generated script.

## Example

```bash
python3 transterpreter.py example.pseudo
```

This will generate `a.py` and execute it.

## Test pseudocode files

The repository includes 12 `.pseudo` test files in `tests/` that exercise supported features and edge cases found during remediation.

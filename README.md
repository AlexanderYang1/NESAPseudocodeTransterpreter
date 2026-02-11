# NESAPseudocodeTransterpreter

A procedural transterpreter for NESA-style pseudocode.

## What it does

1. Reads NESA pseudocode from an input file.
2. Translates it to Python 3.
3. Writes the generated Python to `a.py` (default).
4. Runs `a.py`.

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

# init_files_variables_and_expansions

Shell scripts covering shell initialization files, aliases, environment and local variables, the `PATH`, and arithmetic/base expansions in `bash`.

## Requirements

- All scripts are written in `bash`, on Ubuntu 20.04 LTS (or compatible).
- All scripts start with `#!/bin/bash` on the first line.
- All scripts are executable (`chmod +x`).
- Some scripts must be run with `source` or `.` (dot) instead of `./`, since they modify the current shell's environment (aliases, `PATH`, variables) — noted per task.
- Some tasks have specific constraints (e.g. max script length) — noted per task.

## Tasks

| # | File | Description |
|---|------|-------------|
| 0 | `0-alias` | Creates an alias named `ls` with the value `rm *`. |
| 1 | `1-hello_you` | Prints `hello user`, where `user` is the current Linux user. |
| 2 | `2-path` | Adds `/action` to the end of `PATH`. |
| 3 | `3-paths` | Counts the number of directories in `PATH`. |
| 4 | `4-global_variables` | Lists all environment variables. |
| 5 | `5-local_variables` | Lists all local variables, environment variables, and functions. |
| 6 | `6-create_local_variable` | Creates a new local variable `BEST` with value `School`. |
| 7 | `7-create_global_variable` | Creates a new global variable `BEST` with value `School`. |
| 8 | `8-true_knowledge` | Prints the result of `128 + $TRUEKNOWLEDGE`. |
| 9 | `9-divide_and_rule` | Prints the result of `$POWER / $DIVIDE`. |
| 10 | `10-love_exponent_breath` | Prints the result of `$BREATH` raised to the power `$LOVE`. |
| 11 | `11-binary_to_decimal` | Converts the base-2 number in `$BINARY` to base 10. |
| 12 | `12-combinations` | Prints all two-letter combinations from `aa` to `zz`, alpha ordered, excluding `oo` (script limited to 64 characters). |
| 13 | `13-print_float` | Prints the number in `$NUM` formatted to two decimal places. |
| 14 | `14-decimal_to_hexadecimal` | Converts the base-10 number in `$DECIMAL` to base 16. |
| 15 | `15-rot13` | Encodes/decodes standard input text using ROT13. |
| 16 | `16-odd` | Prints every other line from input, starting with the first line. |
| 17 | `17-water_and_stir` | Adds the numbers in `$WATER` (base "water") and `$STIR` (base "stir"), printing the result in base "bestchol". |

## Usage

```bash
chmod +x <script_name>
./<script_name>
```

Scripts that change the current shell's environment (`0-alias`, `2-path`, `3-paths`, `4-global_variables`, `5-local_variables`, `6-create_local_variable`, `7-create_global_variable`) must be run with `source` or `.` instead of `./`:

```bash
source ./0-alias
. ./3-paths
```

Scripts that depend on environment variables need those variables exported first:

```bash
export TRUEKNOWLEDGE=1209
./8-true_knowledge
```

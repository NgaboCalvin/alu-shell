# io_redirections_and_filters

Shell scripts covering I/O redirection and text-filtering commands in Unix/Linux — writing output, reading and slicing files, searching with `grep`, transforming text with `tr`/`rev`/`sort`/`uniq`, and parsing logs.

## Requirements

- All scripts are written in `bash`, on Ubuntu 20.04 LTS (or compatible).
- All scripts start with `#!/bin/bash` on the first line.
- All scripts are executable (`chmod +x`).
- Some tasks explicitly forbid certain commands (e.g. `sed`, `grep`, `basename`) — noted per task.

## Tasks

| # | File | Description |
|---|------|-------------|
| 0 | `0-hello_world` | Prints "Hello, World" followed by a newline. |
| 1 | `1-confused_smiley` | Displays a confused smiley `"(Ôo)'`. |
| 2 | `2-hellofile` | Displays the content of `/etc/passwd`. |
| 3 | `3-twofiles` | Displays the content of `/etc/passwd` and `/etc/hosts`. |
| 4 | `4-lastlines` | Displays the last 10 lines of `/etc/passwd`. |
| 5 | `5-firstlines` | Displays the first 10 lines of `/etc/passwd`. |
| 6 | `6-third_line` | Displays the third line of the file `iacta` (no `sed`). |
| 7 | `7-file` | Creates a file with a complex literal name containing special characters, ending in a newline. |
| 8 | `8-cwd_state` | Writes the output of `ls -la` into `ls_cwd_content`, overwriting it if it exists. |
| 9 | `9-duplicate_last_line` | Duplicates the last line of the file `iacta`. |
| 10 | `10-no_more_js` | Deletes all regular `.js` files in the current directory and subdirectories. |
| 11 | `11-directories` | Counts the number of directories and subdirectories in the current directory (excluding `.` and `..`, including hidden ones). |
| 12 | `12-newest_files` | Displays the 10 newest files in the current directory, newest first. |
| 13 | `13-unique` | Reads a list of words (one per line) and prints only the words that appear exactly once, sorted. |
| 14 | `14-findthatword` | Displays lines containing "root" from `/etc/passwd`. |
| 15 | `15-countthatword` | Displays the number of lines containing "bin" in `/etc/passwd`. |
| 16 | `16-whatsnext` | Displays lines containing "root" and the 3 lines after each match in `/etc/passwd`. |
| 17 | `17-hidethisword` | Displays all lines in `/etc/passwd` that do **not** contain "bin". |
| 18 | `18-letteronly` | Displays lines of `/etc/ssh/sshd_config` starting with a letter (upper or lower case). |
| 19 | `19-AZ` | Replaces all `A` with `Z` and all `c` with `e` in the input. |
| 20 | `20-hiago` | Removes all occurrences of `c` and `C` from the input. |
| 21 | `21-reverse` | Reverses the input. |
| 22 | `22-users_and_homes` | Displays all users and their home directories from `/etc/passwd`, sorted by username. |
| 23 | `23-empty_casks` | Finds all empty files and directories (including hidden) recursively, printing names only, one per line (no `basename`/`grep` family). |
| 24 | `24-gifs` | Lists all `.gif` files recursively (hidden included, files only), names without extension, sorted case-insensitively (no `basename`/`grep` family). |
| 25 | `25-acrostic` | Decodes an acrostic by taking the first letter of each line of input (no `grep` family). |
| 26 | `26-the_biggest_fan` | Parses a TSV web server log and displays the 11 hosts/IPs with the most requests, most active first (no `grep` family). |

## Usage

```bash
chmod +x <script_name>
./<script_name>
```

Scripts that read from standard input (e.g. `13-unique`, `19-AZ`, `20-hiago`, `21-reverse`, `25-acrostic`, `26-the_biggest_fan`) should be run with input piped or redirected in:

```bash
cat list | ./13-unique
./25-acrostic < "An Acrostic"
./26-the_biggest_fan < nasa_19950801.tsv
```

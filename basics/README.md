# basics

Shell scripts covering the basics of Unix/Linux shell usage — navigating the filesystem, listing and inspecting files, managing directories, symbolic links, and basic file manipulation with `bash`.

## Requirements

- All scripts are written in `bash`, on Ubuntu 20.04 LTS (or compatible).
- All scripts start with `#!/bin/bash` on the first line.
- All scripts are executable (`chmod +x`).
- Scripts are as short as the task requires; length is checked with `wc`.

## Tasks

| # | File | Description |
|---|------|-------------|
| 0 | `0-current_working_directory` | Prints the absolute path name of the current working directory. |
| 1 | `1-listit` | Displays the contents of the current directory. |
| 2 | `2-bring_me_home` | Changes the working directory to the user's home directory (no shell variables allowed). |
| 3 | `3-listfiles` | Displays current directory contents in long format. |
| 4 | `4-listmorefiles` | Displays current directory contents, including hidden files, in long format. |
| 5 | `5-listfilesdigitonly` | Displays current directory contents in long format, with numeric user/group IDs, including hidden files. |
| 6 | `6-firstdirectory` | Creates a directory named `my_first_directory` in `/tmp/`. |
| 7 | `7-movethatfile` | Moves the file `betty` from `/tmp/` to `/tmp/my_first_directory`. |
| 8 | `8-firstdelete` | Deletes the file `betty` from `/tmp/my_first_directory`. |
| 9 | `9-firstdirdeletion` | Deletes the directory `my_first_directory` from `/tmp/`. |
| 10 | `10-back` | Changes the working directory to the previous one. |
| 11 | `11-lists` | Lists all files (including hidden) in the current directory, the parent directory, and `/boot`, in that order, in long format. |
| 12 | `12-file_type` | Prints the type of the file `/tmp/iamafile`. |
| 13 | `13-symbolic_link` | Creates a symbolic link named `__ls__` to `/bin/ls` in the current directory. |
| 14 | `14-copy_html` | Copies HTML files from the current directory to the parent directory, only if new or newer. |
| 15 | `15-lets_move` | Moves all files beginning with an uppercase letter to `/tmp/u`. |
| 16 | `16-clean_emacs` | Deletes all files in the current directory ending with `~`. |
| 17 | `17-tree` | Creates the nested directories `welcome/`, `welcome/to/`, and `welcome/to/school` using only two spaces/lines in the script. |

## Usage

```bash
chmod +x <script_name>
./<script_name>
```

Scripts that change the shell's current directory (`2-bring_me_home`, `10-back`) must be run with `source` instead of `./`:

```bash
source ./2-bring_me_home
```

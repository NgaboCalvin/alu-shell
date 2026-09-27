# permissions

Shell scripts covering Unix/Linux file permissions and ownership — switching users, checking identity and groups, changing owners and groups, and setting read/write/execute permissions with `chmod`.

## Requirements

- All scripts are written in `bash`, on Ubuntu 20.04 LTS (or compatible).
- All scripts start with `#!/bin/bash` on the first line.
- All scripts are executable (`chmod +x`).
- Some scripts have specific constraints (e.g. exact character count, no commas allowed) — noted per task.

## Tasks

| # | File | Description |
|---|------|-------------|
| 0 | `0-iam_betty` | Switches the current user to the user `betty` (exactly 8 characters + newline). |
| 1 | `1-who_am_i` | Prints the effective username of the current user. |
| 2 | `2-groups` | Prints all the groups the current user is part of. |
| 3 | `3-new_owner` | Changes the owner of the file `hello` to the user `betty`. |
| 4 | `4-empty` | Creates an empty file called `hello`. |
| 5 | `5-execute` | Adds execute permission to the owner of the file `hello`. |
| 6 | `6-multiple_permissions` | Adds execute permission to owner and group, and read permission to others, on `hello`. |
| 7 | `7-everybody` | Adds execute permission to owner, group, and others on `hello` (no commas allowed). |
| 8 | `8-James_Bond` | Sets `hello` permissions to `000` for owner/group and `777` for other users (no commas allowed). |
| 9 | `9-John_Doe` | Sets the mode of `hello` to `751` (no commas allowed). |
| 10 | `10-mirror_permissions` | Sets the mode of `hello` to match the mode of `olleh`. |
| 11 | `11-directories_permissions` | Adds execute permission for owner, group, and others to all subdirectories of the current directory (files unaffected). |
| 12 | `12-directory_permissions` | Creates a directory `my_dir` with permissions `751`. |
| 13 | `13-change_group` | Changes the group owner of `hello` to `school`. |
| 14 | `14-change_owner_and_group` | Changes the owner to `vincent` and group to `staff` for all files/directories in the working directory. |
| 15 | `15-symbolic_link_permissions` | Changes the owner and group of the symbolic link `_hello` to `vincent` and `staff`. |
| 16 | `16-if_only` | Changes the owner of `hello` to `vincent`, only if it is currently owned by `guillaume`. |

## Usage

```bash
chmod +x <script_name>
./<script_name>
```

Some scripts require elevated privileges (e.g. changing ownership) and should be run with `sudo`:

```bash
sudo ./3-new_owner
```

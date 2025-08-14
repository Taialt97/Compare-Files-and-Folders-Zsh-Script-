# Compare Files and Folders (Zsh Script)

A simple Zsh script for comparing two directories and reporting differences in a clear, organized format.  
It checks **only core folders** you define, then outputs differences in both folder structure and files.

## Features
- Compares folder structures against a predefined core list.
- Reports:
  - Missing folders in either directory.
  - Files present in one directory but not the other.
- Clean, easy-to-read output sections:
  - **Summary**
  - **Folders**
  - **Files**
- Ignores irrelevant folders and files outside the core list.

## Usage
```bash
chmod +x Compare\ Files\ and\ Folders.zsh
./Compare\ Files\ and\ Folders.zsh /path/to/folder_a /path/to/folder_b
```

## Example Output
```
==============================
SUMMARY
==============================
Match: FAIL
Missing from B: 1
Missing from A: 2
Type mismatch: 0
Pixel-size mismatch: 0
Byte mismatch (>50MB): 0

==============================
FOLDERS
==============================
PayTable/PSD in Dev_B does not exist
Visualizer in Dev_B does not exist

==============================
FILES
==============================
Exports/bg
    folder_a/bg.jpg
    folder_b/bg.png
------------------------------
Exports/slot
    folder_b/slot_dark copy.png
------------------------------
```

## Requirements
- **Zsh** (default on macOS, installable on Linux)
- `find` command

## License
MIT License

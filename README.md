# Linux & Git Cheat Sheet

This repo contains 15 Linux & Git commands.  
Each command was created in its own branch and merged to main.

## 01) ls — List files and directories
**What it does:** Lists directory contents.

**Common flags:**
- `-l` → long format (permissions, size, dates)
- `-a` → include hidden files
- `-h` → human-readable sizes

**Examples:**
```bash
ls -la
ls -lh /Applications


## 02) cd — Change directory
**What it does:** Moves between directories.

**Examples:**
```bash
cd ~        # go to home
cd ..       # go up one level
cd -        # go back to previous dir


## 03) pwd — Print working directory
**What it does:** Shows the full path of the current directory.

**Example:**
```bash
pwd


## 04) mkdir — Make directory
**What it does:** Creates a new directory.

**Flags:**
- `-p` → create parent directories if not present

**Examples:**
```bash
mkdir project
mkdir -p src/utils


## 05) touch — Create empty file
**What it does:** Creates a new empty file or updates timestamp.

**Example:**
```bash
touch notes.txt


## 06) cp — Copy files and directories
**What it does:** Copies files.

**Flags:**
- `-r` → recursive copy for directories

**Examples:**
```bash
cp file1.txt file2.txt
cp -r src src_backup


## 07) mv — Move or rename
**What it does:** Moves or renames files.

**Examples:**
```bash
mv old.txt new.txt
mv file.txt docs/


## 08) rm — Remove files
**What it does:** Deletes files or directories.

**Flags:**
- `-i` → interactive (ask before delete)
- `-r` → recursive (delete dirs)

**Examples:**
```bash
rm -i file.txt
rm -rf build/


## 09) grep — Search inside files
**What it does:** Finds patterns inside text.

**Flags:**
- `-n` → show line numbers
- `-R` → recursive search

**Examples:**
```bash
grep -n "main" README.md
grep -R "init" .


## 10) find — Locate files
**What it does:** Finds files by name or criteria.

**Examples:**
```bash
find . -name "*.md"
find /usr -type f -size +10M


## 11) git init — Initialize repository
**What it does:** Creates a new Git repo.

**Example:**
```bash
git init -b main


## 12) git status — Show working state
**What it does:** Displays staged, modified, or untracked files.

**Example:**
```bash
git status -sb


## 13) git add — Stage changes
**What it does:** Adds files to staging area.

**Examples:**
```bash
git add README.md
git add .


## 14) git commit — Save snapshot
**What it does:** Records staged changes in history.

**Example:**
```bash
git commit -m "docs: add new command section"


## 15) git log — View history
**What it does:** Shows commit history.

**Flags:**
- `--oneline` → compact view
- `--graph` → ASCII branch tree
- `--decorate` → show branch names/tags

**Examples:**
```bash
git log --oneline
git log --oneline --graph --decorate --all


# 🐧 Linux Text Processing Cheatsheet

A practical guide to essential Linux text processing tools: `grep`, `find`, `wc`, `sort`, `uniq`, `cut`, `awk`, and `sed`.

---

## 📌 1. grep (Search Text)

Search for patterns in files or input.

### Syntax

```bash
grep [options] "pattern" [file]

grep "hello" file.txt          # Search text
grep -i "hello" file.txt       # Case-insensitive
grep -r "text" /dir            # Recursive search
grep -n "text" file.txt        # Show line numbers
grep -v "text" file.txt        # Invert match
grep -c "text" file.txt        # Count matches
grep -w "word" file.txt        # Match whole word
```
---

## 📌 2. find (Search Files & Directories)

Search files based on name, type, size, etc..

### Syntax
```bash
find [path] [options]

find . -name "file.txt"        # Find by name
find . -type f                 # Only files
find . -type d                 # Only directories
find . -size +10M              # Files larger than 10MB
find . -name "*.log"           # Find all .log files
```
## 📌 3. wc (Word Count)

Count lines, words, and characters.

### Syntax
```bash
wc [options] file

wc file.txt                    # Lines, words, chars
wc -l file.txt                 # Count lines
wc -w file.txt                 # Count words
wc -c file.txt                 # Count characters
```
## 📌4. sort (Sort Text)

Sort lines alphabetically or numerically.

Syntax
### Syntax
```bash
sort [options] file

sort file.txt                  # Sort alphabetically
sort -r file.txt               # Reverse order
sort -n file.txt               # Numeric sort
sort -u file.txt               # Unique + sort
```
## 📌 5. uniq (Remove Duplicates)

Filter duplicate lines (works best with sorted input).

### Syntax
```bash
uniq [options] file

uniq file.txt                  # Remove duplicates
uniq -c file.txt               # Count occurrences
sort file.txt | uniq           # Proper duplicate removal
```
## 📌 6. cut (Extract Columns)

Extract sections from each line.

### Syntax
```bash
cut [options]

cut -d "," -f1 file.csv        # Get column 1
cut -c 1-5 file.txt            # Characters 1 to 5
```
## 📌 7. awk (Pattern Processing)

Powerful text processing and reporting tool.

### Syntax
```bash
awk 'pattern {action}' file

awk '{print $1}' file.txt              # Print first column
awk '{print $1, $3}' file.txt          # Print columns
awk '/error/ {print}' file.txt         # Search pattern
awk '{sum += $1} END {print sum}' file # Sum column
```
## 📌 8. sed (Stream Editor)

Edit and transform text.

### Syntax
```bash
sed 'command' file

sed 's/old/new/' file.txt              # Replace first match
sed 's/old/new/g' file.txt             # Replace all matches
sed -n '1,5p' file.txt                 # Print lines 1–5
sed '/pattern/d' file.txt              # Delete matching lines
```
## 🔗 Piping & Redirection

Combine commands using pipes |
```bash
cat file.txt | grep "error"            # Filter lines
grep "error" file.txt | wc -l          # Count matches
sort file.txt | uniq                   # Remove duplicates
cut -d "," -f1 file.csv | sort | uniq  # Unique column values
```
## ⚡ Powerful Combinations
```bash
ps aux | grep python                   # Find running processes
ls -l | grep ".txt"                   # Filter files
cat file.txt | sort | uniq -c | sort -nr  # Word frequency
```





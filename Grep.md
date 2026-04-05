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


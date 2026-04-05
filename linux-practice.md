# linux-practice
Commands and exercises from my Linux learning journey.

## cat Command(Concatenate)
Syntax 
`cat [options] [file(s)]`
### 10 Essential Use Cases
1)Display file content
  `cat file.txt`

2)Create a new file
  `cat >newfile.txt`

3)Concatenate two files into a third
  `cat file1.txt file2.txt > combined.txt`

4)Append one file to another 
  `cat file1.txt>>existing.txt`
  
5)Display line numbers
  `cat -n file.txt`

6)Remove repeated blank lines
  `cat -s file.txt`

7)Show $ at end of each line
  `cat -E file.txt`

8)Merge all .txt files
  `cat *.txt > all_notes.txt`

9)View file in reverse
  `tac file.txt`

10)Show everything
  `cat -A file.txt`


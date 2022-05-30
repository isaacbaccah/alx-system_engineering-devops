This readme file will be updated later

**This script prints "Hello, World"**
0-hello_world         
#!/bin/bash
echo "Hello, World"

**Write a script that displays a confused smiley "(Ôo)'.**
1-confused_smiley     
#!/bin/bash
echo \"\(\Ô\o\)\'
use contrl, shift 6, capital O to get Ô

**Display the content of the /etc/passwd file.**
2-hellofile           
#!/bin/bash
cat /etc/passwd

**Display the content of /etc/passwd and /etc/hosts**
3-twofiles            
#!/bin/bash
cat /etc/passwd /etc/hosts

**Display the last 10 lines of /etc/passwd**
4-lastlines           
#!/bin/bash
tail -n 10 /etc/passwd

**Display the first 10 lines of /etc/passwd**
5-firstlines          
#!/bin/bash
head -n 10 /etc/passwd

**Write a script that displays the third line of the file iacta.**
6-third_line          
#!/bin/bash
head -3 iacta | tail +3

**Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line.** 
7-file                 
#!/bin/bash
echo "Best School" > \\\*\\\\"'\"Best School\"\\'"\\\\\*\$\\\?\\\*\\\*\\\*\\\*\\\*\:\)

**Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.**
8-cwd_state           
#!/bin/bash
ls -la > ls_cwd_content

**Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it.**
9-duplicate_last_line 
#!/bin/bash
tail -n 1 iacta >> iacta
you can echo the text in the task to create iacta file

**Write a script that duplicates the last line of the file iacta**
10-no_more_js
#!/bin/bash
find . -type f -name "*.js" -delete

**Write a script that counts the number of directories and sub-directories in the current directory.
The current and parent directories should not be taken into account
Hidden directories should be counted**
11-directories
#!/bin/bash
find . -type d -not -name '.' | wc -l

**Create a script that displays the 10 newest files in the current directory.
One file per line
Sorted from the newest to the oldest**
12-newest_files
#!/bin/bash
ls -t1 | head -n 10

**Create a script that takes a list of words as input and prints only words that appear exactly once.
Input format: One line, one word
Output format: One line, one word
Words should be sorted**
13-unique
#!/bin/bash
sort | uniq -u
you can echo the txt in the task to creat list file

**Display lines containing the pattern “root” from the file /etc/passwd**
14-findthatword
#!/bin/bash
grep -i "root" /etc/passwd

**Display the number of lines that contain the pattern “bin” in the file /etc/passwd**
15-countthatword
#!/bin/bash
grep -c -i "bin" /etc/passwd

**Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd.**
16-whatsnext
#!/bin/bash
grep -i "root" -A 3 /etc/passwd

**Display all the lines in the file /etc/passwd that do not contain the pattern “bin”.**
17-hidethisword
#!/bin/bash
grep -i -v "bin" /etc/passwd

**Display all lines of the file /etc/ssh/sshd_config starting with a letter.
include capital letters as well**
18-letteronly
#!/bin/bash
grep -i "^[a-z]" /etc/ssh/sshd_config

**Replace all characters A and c from input to Z and e respectively.**
19-AZ
#!/bin/bash
tr "A" "Z" | tr "c" "e"

**Create a script that removes all letters c and C from input.**
20-hiago
#!/bin/bash
tr -d "cC"

**Write a script that reverse its input.**
21-reverse
#!/bin/bash
rev

**Write a script that displays all users and their home directories, sorted by users.
Based on the the /etc/passwd file**
22-users_and_homes
#!/bin/bash
cut -d ':' -f 1,6 /etc/passwd | sort

**Write a command that finds all empty files and directories in the current directory and all sub-directories.**
100-empty_casks
#!/bin/bash
find . -empty | rev | cut -d '/' -f 1 | rev

**Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories.**
101-gifs
#!/bin/bash
find -type f -name "*.gif" | rev | cut -d "/" -f 1 | cut -d '.' -f 2- | rev | LC_ALL=C sort -f

**Create a script that decodes acrostics that use the first letter of each line.**
102-acrostic
#!/bin/bash
cut -c 1 | paste -s -d ''

**Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests.**
103-the_biggest_fan
#!/bin/bash
tail -n +2 | cut -f -1 | sort -k 1 | uniq -c | sort -rnk 1 | head -n 11 | rev | cut -d ' ' -f -1 | rev

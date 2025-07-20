this is for bash scripting



# Shell, I/O Redirections and filters

* Task 0 Write a script that prints “Hello, World”, followed by a new line to the standard output. **echo Hello, World**
* Task 1 Write a script that displays a confused smiley "(Ôo)'. **echo "\"(Ôo)'"**
* Task 2 Display the content of the /etc/passwd file. **cat /etc/passwd**
* Task 3 Display the content of /etc/passwd and /etc/hosts. **cat /etc/passwd /etc/hosts**
* Task 4 Display the last 10 lines of /etc/passwd. **tail /etc/passwd**
* Task 5 Display the first 10 lines of /etc/passwd. **head /etc/passwd**
* Task 6 Write a script that displays the third line of the file iacta. **head -3 iacta | tail +3**
* Task 7 Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line. **echo "Best School" > "\*\\\'\"Best School\"\'\\\*$\?\*\*\*\*\*:)"**
* Task 8 Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it. **ls -la > 'ls_cwd_content'**
* Task 9 Write a script that duplicates the last line of the file iacta. **tail -n 1 iacta >> iacta**
* Task 10 Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders. **find . -type f -name "*.js" -delete**
* Task 11 Write a script that counts the number of directories and sub-directories in the current directory. **find . -mindepth 1 -type d | wc -l**
* Task 12 Create a script that displays the 10 newest files in the current directory. **ls -1t | head **
* Task 13 Create a script that takes a list of words as input and prints only words that appear exactly once. **sort | uniq -u **
* Task 14 Display lines containing the pattern “root” from the file /etc/passwd. **grep root /etc/passwd**
* Task 15 Display the number of lines that contain the pattern “bin” in the file /etc/passwd. **grep -c bin /etc/passwd**
* Task 16 Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd. **grep -A 3 root /etc/passwd**
* Task 17 Display all the lines in the file /etc/passwd that do not contain the pattern “bin”. **grep -L bin /ect/passwd **
* Task 18 Display all lines of the file /etc/ssh/sshd_config starting with a letter. **grep '^[A-Z | a-z]' /etc/ssh/sshd_config **
* Task 19 Replace all characters A and c from input to Z and e respectively. **tr A Z |tr c e**
* Task 20 Create a script that removes all letters c and C from input. **tr -d c | tr -d C **
* Task 21 Write a script that reverse its input. **rev**
* Task 22 Write a script that displays all users and their home directories, sorted by users. **cat /etc/passwd | cut -d : -f 1,6 /etc/passwd | sort **
* Task 23 Write a command that finds all empty files and directories in the current directory and all sub-directories. **find . -empty -printf %f'\n'**
* Task 24 Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories. **find . -type f -name "*.gif" -printf "%f\n" | LC_ALL=C sort -f | rev | cut -b 5- | rev **
* Task 25 Create a script that decodes acrostics that use the first letter of each line. **cut -c 1 | paste -s -d ' ' | tr -d ' '**
* Task 26 Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests. **tail -n +2 | cut -f 1 | sort | uniq -c | sort -n -r | head -n 11 | cut -b 9-**

### Resources
[How to display specific lines of a file in Linux Command Line](https://linuxhandbook.com/display-specific-lines/)

Nijat Hatamli (Creator)

Proyects from the week September 26, 2022 - September 30, 2022# Shell, I/O Redirections and filters

* Task 0 Write a script that prints “Hello, World”, followed by a new line to the standard output. **echo Hello, World**
* Task 1 Write a script that displays a confused smiley "(Ôo)'. **echo "\"(Ôo)'"**
* Task 2 Display the content of the /etc/passwd file. **cat /etc/passwd**
* Task 3 Display the content of /etc/passwd and /etc/hosts. **cat /etc/passwd /etc/hosts**
* Task 4 Display the last 10 lines of /etc/passwd. **tail /etc/passwd**
* Task 5 Display the first 10 lines of /etc/passwd. **head /etc/passwd**
* Task 6 Write a script that displays the third line of the file iacta. **head -3 iacta | tail +3**
* Task 7 Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line. **echo "Best School" > "\*\\\'\"Best School\"\'\\\*$\?\*\*\*\*\*:)"**
* Task 8 Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it. **ls -la > 'ls_cwd_content'**
* Task 9 Write a script that duplicates the last line of the file iacta. **tail -n 1 iacta >> iacta**
* Task 10 Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders. **find . -type f -name "*.js" -delete**
* Task 11 Write a script that counts the number of directories and sub-directories in the current directory. **find . -mindepth 1 -type d | wc -l**
* Task 12 Create a script that displays the 10 newest files in the current directory. **ls -1t | head **
* Task 13 Create a script that takes a list of words as input and prints only words that appear exactly once. **sort | uniq -u **
* Task 14 Display lines containing the pattern “root” from the file /etc/passwd. **grep root /etc/passwd**
* Task 15 Display the number of lines that contain the pattern “bin” in the file /etc/passwd. **grep -c bin /etc/passwd**
* Task 16 Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd. **grep -A 3 root /etc/passwd**
* Task 17 Display all the lines in the file /etc/passwd that do not contain the pattern “bin”. **grep -L bin /ect/passwd **
* Task 18 Display all lines of the file /etc/ssh/sshd_config starting with a letter. **grep '^[A-Z | a-z]' /etc/ssh/sshd_config **
* Task 19 Replace all characters A and c from input to Z and e respectively. **tr A Z |tr c e**
* Task 20 Create a script that removes all letters c and C from input. **tr -d c | tr -d C **
* Task 21 Write a script that reverse its input. **rev**
* Task 22 Write a script that displays all users and their home directories, sorted by users. **cat /etc/passwd | cut -d : -f 1,6 /etc/passwd | sort **
* Task 23 Write a command that finds all empty files and directories in the current directory and all sub-directories. **find . -empty -printf %f'\n'**
* Task 24 Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories. **find . -type f -name "*.gif" -printf "%f\n" | LC_ALL=C sort -f | rev | cut -b 5- | rev **
* Task 25 Create a script that decodes acrostics that use the first letter of each line. **cut -c 1 | paste -s -d ' ' | tr -d ' '**
* Task 26 Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests. **tail -n +2 | cut -f 1 | sort | uniq -c | sort -n -r | head -n 11 | cut -b 9-**

### Resources
[How to display specific lines of a file in Linux Command Line](https://linuxhandbook.com/display-specific-lines/)

Nijat Hatamli(Creator)

Proyects from the week September 26, 2022 - September 30, 2022# Shell, I/O Redirections and filters

* Task 0 Write a script that prints “Hello, World”, followed by a new line to the standard output. **echo Hello, World**
* Task 1 Write a script that displays a confused smiley "(Ôo)'. **echo "\"(Ôo)'"**
* Task 2 Display the content of the /etc/passwd file. **cat /etc/passwd**
* Task 3 Display the content of /etc/passwd and /etc/hosts. **cat /etc/passwd /etc/hosts**
* Task 4 Display the last 10 lines of /etc/passwd. **tail /etc/passwd**
* Task 5 Display the first 10 lines of /etc/passwd. **head /etc/passwd**
* Task 6 Write a script that displays the third line of the file iacta. **head -3 iacta | tail +3**
* Task 7 Write a shell script that creates a file named exactly \*\\'"Best School"\'\\*$\?\*\*\*\*\*:) containing the text Best School ending by a new line. **echo "Best School" > "\*\\\'\"Best School\"\'\\\*$\?\*\*\*\*\*:)"**
* Task 8 Write a script that writes into the file ls_cwd_content the result of the command ls -la. If the file ls_cwd_content already exists, it should be overwritten. If the file ls_cwd_content does not exist, create it. **ls -la > 'ls_cwd_content'**
* Task 9 Write a script that duplicates the last line of the file iacta. **tail -n 1 iacta >> iacta**
* Task 10 Write a script that deletes all the regular files (not the directories) with a .js extension that are present in the current directory and all its subfolders. **find . -type f -name "*.js" -delete**
* Task 11 Write a script that counts the number of directories and sub-directories in the current directory. **find . -mindepth 1 -type d | wc -l**
* Task 12 Create a script that displays the 10 newest files in the current directory. **ls -1t | head **
* Task 13 Create a script that takes a list of words as input and prints only words that appear exactly once. **sort | uniq -u **
* Task 14 Display lines containing the pattern “root” from the file /etc/passwd. **grep root /etc/passwd**
* Task 15 Display the number of lines that contain the pattern “bin” in the file /etc/passwd. **grep -c bin /etc/passwd**
* Task 16 Display lines containing the pattern “root” and 3 lines after them in the file /etc/passwd. **grep -A 3 root /etc/passwd**
* Task 17 Display all the lines in the file /etc/passwd that do not contain the pattern “bin”. **grep -L bin /ect/passwd **
* Task 18 Display all lines of the file /etc/ssh/sshd_config starting with a letter. **grep '^[A-Z | a-z]' /etc/ssh/sshd_config **
* Task 19 Replace all characters A and c from input to Z and e respectively. **tr A Z |tr c e**
* Task 20 Create a script that removes all letters c and C from input. **tr -d c | tr -d C **
* Task 21 Write a script that reverse its input. **rev**
* Task 22 Write a script that displays all users and their home directories, sorted by users. **cat /etc/passwd | cut -d : -f 1,6 /etc/passwd | sort **
* Task 23 Write a command that finds all empty files and directories in the current directory and all sub-directories. **find . -empty -printf %f'\n'**
* Task 24 Write a script that lists all the files with a .gif extension in the current directory and all its sub-directories. **find . -type f -name "*.gif" -printf "%f\n" | LC_ALL=C sort -f | rev | cut -b 5- | rev **
* Task 25 Create a script that decodes acrostics that use the first letter of each line. **cut -c 1 | paste -s -d ' ' | tr -d ' '**
* Task 26 Write a script that parses web servers logs in TSV format as input and displays the 11 hosts or IP addresses which did the most requests. **tail -n +2 | cut -f 1 | sort | uniq -c | sort -n -r | head -n 11 | cut -b 9-**

### Resources
[How to display specific lines of a file in Linux Command Line](https://linuxhandbook.com/display-specific-lines/)

Nijat Hatamli(Creator)



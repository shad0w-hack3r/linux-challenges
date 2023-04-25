# Introduction

### This file contains all the solutions of challenges which are available on <https://cmdchallenge.com>.

---

1. ### [Challenge 1](https://cmdchallenge.com/#/hello_world):
   ---
   Print "hello world"
   > `echo "hello world"`

2. ### [Challenge 2](https://cmdchallenge.com/#/current_working_directory):
   ---
   Print current working directory
   > `pwd`

3. ### [Challenge 3](https://cmdchallenge.com/#/list_files):
   ---
   List the names of all files in the current directory, one file per line.
   > `ls`

4. ### [Challenge 4](https://cmdchallenge.com/#/print_file_contents):
   ---
   There is a file named access.log in the current directory. Print the contents.
   > `cat access.log`

5. ### [Challenge 5](https://cmdchallenge.com/#/last_lines):
   ---
    Print the last 5 lines of "access.log".
    > `tail -5 access.log`

6. ### [Challenge 6](https://cmdchallenge.com/#/create_file):
   ---
   Create an empty file named take-the-command-challenge in the current working directory.
   > `touch take-the-command-challenge`

7. ### [Challenge 7](https://cmdchallenge.com/#/create_directory):
   ---
   Create a directory named tmp/files in the current working directory. 
   ##### *Hint: The directory "tmp/" doesn't exist, with one command you need to create both "tmp/" and "tmp/files"*
   > `mkdir -p tmp/files`

8. ### [Challenge 8](https://cmdchallenge.com/#/copy_file):
   ---
   Copy the file named take-the-command-challenge to the directory tmp/files.
   > `cp take-the-command-challenge tmp/files/`
   
9. ### [Challenge 9](https://cmdchallenge.com/#/move_file):
    ---
    Move the file named take-the-command-challenge to the directory tmp/files
    > `mv take-the-command-challenge tmp/files/`

10. ### [Challenge 10](https://cmdchallenge.com/#/create_symlink):
    ---
    Create a symbolic link named take-the-command-challenge that points to the file tmp/files/take-the-command-challenge.
    > `ln -s tmp/files/take-the-command-challenge take-the-command-challenge`

11. ### [Challenge 10](https://cmdchallenge.com/#/delete_files)
    ---
    Delete all of the files in this challenge directory including all subdirectories and their contents.
    ##### *Hint: There are files and directories that start with a dot ".", "rm -rf *" won't work here!*
    > `rm -rf * .*`

12. ### [Challenge 11](https://cmdchallenge.com/#/remove_files_with_extension):
    ---
    There are files in this challenge with different file extensions. Remove all files with the .doc extension recursively in the current working directory.
    > `find -name "*.doc" -type f -delete`

13. ## [Challenge 12](https://cmdchallenge.com/#/find_string_in_a_file):
    ---
    There is a file named access.log in the current working directory. Print all lines in this file that contains the string "GET".
    > `cat access.log | grep "GET"`

14. ### [Challenge 13](https://cmdchallenge.com/#/search_for_files_containing_string):
    ---
    Print all files in the current directory, one per line (not the path, just the filename) that contain the string "500".
    > ``

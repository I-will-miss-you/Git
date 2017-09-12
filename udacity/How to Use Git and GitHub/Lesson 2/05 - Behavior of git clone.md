# Behavior of ``` git clone ```

Select When each statement would be true

|  | True when you copy | True when you clone | True in both cases |
| ------ | ------ | ------ | ------ |
| If someone else gives you the location of their directory or repository, you can copy or clone it to your own computer. |  |  | x |
| The history of changes to the directory or repository is copied.| | x | |
| If you make changes to the copied directory or cloned repository, the original will not change.| | | x|
| The state of every file in the directory or repository is copied. | | | x |

## Behavior of git clone

### If someone else gives you the location of their directory or repository, you can copy or clone it to your own computer.

This is true for both copying a directory and cloning a repository.

As you saw in the previous lesson, if you have a URL to a repository, you can copy it to your computer using git clone.

For copying a directory, you weren't expected to know this, but it is possible to copy a directory from one computer to another using the command ``` scp ``` , which stands for "secure copy". The name was chosen because the ``` scp ``` command lets you securely copy a directory from one computer to another.

### The history of changes to the directory or repository is copied.

This is true for cloning a repository, but not for copying a directory. The main reason to use ``` git clone ``` rather than copying the directory is because ``` git clone ``` will also copy the commit history of the repository. However, copying can be done on any directory, whereas ``` git clone ``` only works on a Git repository.

### If you make changes to the copied directory or cloned repository, the original will not change.

This is true for both copying a directory and cloning a repository. In both cases, you're making a copy that you can alter without changing the original.

### The state of every file in the directory or repository is copied.

This is true for both copying a directory and cloning a repository. In both cases, all the files are copied.

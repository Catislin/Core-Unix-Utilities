# Core: Unix Utilities

_More powerful than the spiky blue shell_

## Working with this GitHub repository

Follow these steps to set up your own repository:

1. Fork this repository on GitHub to create your own version of this repo on your GitHub account, which should also be named `Core-Unix-Utilities`

1. Visit your fork and clone that repository onto your computer:
`git clone https://github.com/<your-username>/Core-Unix-Utilities.git`

1. Push your commits and link the local repo to your remote GitHub repo:
`git push -u origin master`

1. When you've completed a challenge and want to share it for code review, commit your work and push it to your own remote repo with:
`git push`

1. Add this GitHub repository as a _remote_ to the local one on your computer:
`git remote add core https://github.com/Product-College-Labs/Core-Unix-Utilities.git`

1. When you want to access new course materials, just pull from the origin remote repo:
`git pull core master`

## Challenges, Part 1

Challenges within each section are meant to be solved in order.

### Navigation

1.  Print the path of your working directory
  - `pwd`
1.  List the files in your working directory
  - `ls`
1.  List the files with a particular extension, like `.txt`
  - `ls *.md`
1.  List the files in a subdirectory, like `project`
  - `ls project/`
1.  Navigate to a subdirectory, like `project`
  - `cd project`
1.  Navigate to the parent directory of your working directory
  - `cd ..`
1.  Navigate to a nested subdirectory, like `path/to/project`
  - `cd path/to/project`
1.  Navigate to your home directory
  - `cd`
1.  Navigate back to the previous directory
  - `cd -`
### Variables

1.  Print a sentence, like `Hello world`
  - `echo "Hello world"`
1.  Print a variable value, like `$USER` or `$PATH`
  - `echo $PATH`
1.  Set a variable `NAME` equal to your first name, then print its value
  - `NAME=alirie`
1.  Set a variable `FULL_NAME` equal to your full name, then print its value
  - `FULL_NAME="alirie gray"`
1.  Print all environment variables (names and values)
  - `printenv`
1.  Make an alias named `hello` that prints `Hello world`
  - `alias hello='echo "hello world"'`
1.  Make an alias named `gocode` that navigates to your code directory
  - `alias gocode='cd /Users/alirie/Documents/make'`
1.  Print all aliases (names and values)
  - `alias`

### Getting Help

1.  Print what options a command accepts, like `bash` or `python`
  - `python -h`
1.  Read the manual for a command, like `echo` or `ls`
  - `man echo`
1.  Print the file path to a command, like `bash` or `python`
  - `which bash`

### Files

1.  Navigate to the directory `Animals`
  - `cd Animals`
2.  Print the contents of the file `Cats.txt`
  - `cat Cats.txt`
3.  Print the contents of both files `Cats.txt` and `Dogs.txt`
  - `cat Cats.txt Dogs.txt`
4.  Count the words in the file `Cats.txt`
  - `wc Cats.txt`
5.  Count the words in all files with the extension `.txt`
  - `wc *.txt`
6.  Copy the file `Dogs.txt` to a new file `BabyDogs.txt`
  - `cat Dogs.txt >> BabyDogs.txt`
7.  Rename the file `BabyDogs.txt` to `Puppies.txt`
  - `mv BabyDogs.txt Puppies.txt`
8.  Make a new directory named `Shelter` inside `Animals`
  - `mkdir Shelter`
9.  Move the file `Puppies.txt` into the directory `Shelter`
  - `mv Puppies.txt Shelter`
10.  Copy the file `Cats.txt` to `Kittens.txt` inside `Shelter`
  - `echo Cats.txt >> Shelter/Kittens.txt`
11.  List the files within the directory `Shelter`
  - `ls Shelter`
12.  Count the words in all `.txt` files inside `Shelter`
  - `wc Shelter/*.txt`
13.  Try to remove the directory `Shelter` (this should fail)
  - `rm Shelter`
14.  Remove all `.txt` files inside `Shelter`
  - `rm Shelter/*.txt`
15.  Remove the directory `Shelter` (this should succeed)
  - `rm -rf Shelter/`
16.  Now cry because you just deleted those poor tiny animals
  -  ;(

### Permissions

1.  Print out your user name
  - `echo $USER`
1.  List the permissions (and metadata) of all `.txt` files
  - `stat *.txt`
1.  Give all users write permission on the file `Cats.txt`
  - `chmod a+w Cats.txt`
1.  List the permissions (and metadata) of the file `Cats.txt`
  - `stat Cats.txt`
1.  Change the owner of the file `Cats.txt` to another user
  - `sudo chown temp Cats.txt`
1.  Now list the permissions (and owner) of the file `Cats.txt`
  - `stat Cats.txt`
1.  Try to change the owner of the file `Cats.txt` back to yourself
  - `chown alirie Cats.txt`
1.  Invoke the super-user to make the previous command succeed
  - `sudo chown alirie Cats.txt`
1.  List the permissions (and owner) of the file `Cats.txt` again
  - `stat Cats.txt`

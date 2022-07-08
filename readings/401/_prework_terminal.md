# Prework

[Back to the table of contents](../../README.md)

## The Command Line

Command line, terminal, or a term you'll hear a lot online, CLI (command line interface) is a text-based interface to your system. You enter commands for a task, it completes that task with varying levels of verbosity, and it gives you back the controls for another task.

* Shell - Your system takes inputs, but your shell is the application you use for said terminal inputs.

### Absolute vs Relative

When you type a location into the terminal, or recieve one, you are either being shown an absolute path, or a relative one. Absolute paths are from the root of your entire file system, starting at `/`, whereas relative pathing is the path to the destination from where YOU are right now. For example, if you're in a directory that has a folder called "Documents", you can reach it from just "Documents" relatively since it is one level down from you, OR absolutely by /path/from/root/to/Documents.

### Here's some funny linux file system concepts:

#### Everything is a file

Yeah you heard me. Even if it is not presented to you as such, EVERYTHING. IS. A. FILE. Directories are files, so is your keyboard, and monitor. You can rename the end of a .png to .txt, it'll still be an image file. That's just changing how your computer is supposed to handle said image file.

Only true way to find out what something is, is with `file [path]` command.

#### Linux is case sensitive

File.txt and file.txt are different things. That is not true for windows, and from personal experience, that has made some truly hellish file system errors in history for me when using windows file system.

#### Linux allows sapces

/home/Two Words.txt, as messed up as that is, is a valid file. But there are added complications when navigating to files with spaces, so maybe be careful and generally avoid it. You have to use escape characters which is never fun, or a string `'`

#### Linux has hidden files

Linux has hidden files, hidden of course by adding `.` to the start of a filename. Example: `.hidden` would be invisible. It's used to hide files that, while they can be revealed easily, really do not matter for humans at all. Stuff that machines write and read.

### Commands/shortcuts

* Up arrow/Down arrow: Goes through your history of past tasks, in case you want to repeat one.
* Tab: Tries to complete a file path from files in where your filepath is going.
* pwd: print working directory, shows where you are.
* ls: list, shows you what is in your current directory, or location.
  * -l: long option, which verbosely displays for each file in this order:
    * directory or file as `d` or `-`
    * permissions for the file (will learn more later but read or write)
    * number of blocks (will learn more later)
    * owner of the file ("hugo")
    * group the file belongs to ("users" instead of hugo for all access)
    * file size
    * last modified
    * NAME, FINALLY
  * -a: all(?), will show even hidden folders. Usually for folders that are not really in english or meant to be looked at by humans.
  * \[path\]: target argument. It lists not the directory you are in's contents, but the contents of the directory you specified.
* ~: Tilde, which is your home directory on your computer. Example: ~/Hugo reaches the Hugo profile from home on the computer.
* .: Dot, which is your current directory. Sometimes can be implicit, but there are uses for the explicit inclusion of it.
* ..: One dir up from you. ../ exits a dir, for example.
* cd: Change directory. supply it with a path, and you will go there.
  * \[path\]: required, where you want to go. You can go absolutely anywhere, relatively from where you are right now anywhere, either works.
* file: File. It shows you what file type something is truly.
  * \[path\]: required, what file you are looking at.
* mkdir: Makes a directory.
  * \<name\>: name of new directory.
  * -p: Parent dirs, Tells mkdir to make parent dirs as needed, so \<name\> can be a filepath and -p will create many dirs
  * -v: Verbose, tell us what you're actually doing.
* rmdir: Removes a directory
  * All arguments and options same as above mkdir.
* touch: Makes an empty file.
* cp: Copies a file
  * \<source\> What you're copying
  * \<destination\> Where you're copying to.
  * -r: Recursive copying, so it will copy the source, but also all subdirectories and subfiles of source.
* mv: moves a file
  * same as above, but no recursive option.
  * NOTE: supplying a filename that doesn't exist changes the name, so you can effectively rename files by moving them to the same directory but with a new name. Neat!
* rm: Removes a file
  * \<file\>: file to be deleted
  * -r (recursive) also works for this, removing all subdirs and subfiles

### Man

Yes, this is so important it requires a section.

* Man: Manual. input a command, get a name, description for what it does, and what args it takes. USEFUL!!!
  * \<command\>: what command you're looking up, like `ls`
  * -k \<search term\>: Instead of looking for what command you want, you can search keywords for what the command accomplishes. Good if you know what you want, but not what does it.
  * q: quits out of the manual once entered
  * n: next item in the manual. In case you wanted to read the whole damn book, I guess.
  * /\<term\>: searches for a special term while looking at the manual.

[And here's a cheat sheet ;)](https://ryanstutorials.net/linuxtutorial/cheatsheet.php)

## Summary

This was a nice refresher for the command line which, well, I've used extensively over the years but man oh man it never hurts to revisit. Another thing to note is that the majority of my time with the command line has been the windows one, and as such I'm a lot more familiar with the pains of the window command line (WHY IS IT NOT CAPS SENSITIVE AAAAH) than I am the linux/mac etc one. One big ah hah for me was the `man` command which I actually had no idea even existed. I suppose nobody wants to mention it online since they're already experienced with it but I think it'll help me out a ton in the future.

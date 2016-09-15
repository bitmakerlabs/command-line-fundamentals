#Command Line Fundamentals

* * *

#### By the end of this Unit, you'll be able to:

*   Differentiate between a command line interface and a graphical user interface
*   Summarize a basic filesystem structure
*   Open a file in a text editor and make changes from the command line
*   Identify when you might want to use absolute versus relative paths

Feeling good? Let's do some more practice.

* * *

##Your Turn

Go ahead an open up "Terminal" in any of the following ways.

1 . Navigate to your Applications folder and double-click on Terminal.

![img](http://fundamentals.generalassemb.ly/assets/Graphics/where_to_find_terminal.gif))

2 . Press <kbd>Command</kbd> + <kbd>Space</kbd> on your keyboard to bring up Spotlight – a tool that allows you to quickly find files and applications on our computer. Inside the search bar, type "Terminal", and select the Terminal application.

![img](http://fundamentals.generalassemb.ly/assets/Graphics/where_to_find_terminal_spotlight.gif)

Great! Now everyone who can see over your shoulder will think you're a badass hacker.

* * *

[On to the next lesson.](05_lesson.html)

## Think Like a Programmer

Most computer users move their mouse, click on icons, drag and drop files from one folder to another.

When you're using the computer this way, you're using what's called a Graphical User Interface or GUI. In a GUI (pronounced "gooey"), you communicate with your computer using a combination of text, images, and gestures.

You are on a journey to transcend being an ordinary user of computers. You are on your way to becoming a developer, and developers like to interact with computers in a different way – through the command line.

Unlike the GUI, the command line is a _text-based interface_, where you communicate with your computer using text alone.

Until the video display was introduced in the mid-1960s, the command line was the only way to interact with your computer. Today, the CLI is still preferred by programmers because it is explicit, simple, and (most importantly) fast... In fact, once you become comfortable using the CLI early in class, you'll be amazed at how much more productive you become!

We can perform actions using the command line by **entering commands**. There is a command to perform virtually any action you can imagine on your computer! There are commands to open an application, create new files, copy files from one place to another, and a lot more.

We'll access the command line using a terminal application, which can be found on all computers. Terminal applications are commonly known as "shells", and we will learn how to use the default shell provided on Mac OS X and Ubuntu Linux: **Bash**.

There are many different types of shells, and some are more similar to Bash than others. Fundamentals will not explore the shells that come with Windows computers, for example, because they use a different set of commands.

## Getting started with Git Bash (Windows Users)

If you're a _Windows_ user, we will be installing **Git Bash**, an environment that will allow you to use Bash. It will create a prompt that is similar to Mac OS X and Ubuntu Linux, allowing you to follow along in Fundamentals. Once you join us for WDI, you will need to use a Mac or Linux environment. Reach out to your local producer if you have any questions.

If you're following along on _Mac OS X or Ubuntu Linux_ feel free to skip the following section on installing Git Bash.

### Downloading Git Bash

*   Navigate to the [git website](https://git-scm.com/) and double click on "Windows".

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/download_1.jpg)

*   Your download should begin.

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/download_2.jpg)

### Installing Git Bash

Follow the prompts in the installation window.

*   Double click on the .exe file that you just downloaded to begin setup.
*   Accept the terms of use.

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/install_2.jpg)

*   Choose a location to install files.

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/install_3.jpg)

*   Select the following options in the "Select Components" prompt.

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/install_4.jpg)

*   Select a start menu folder (optional).
*   Select the "Use Git from Git Bash Only" option.

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/install_6.jpg)

*   Select the "Checkout Windows-style, commit Unix-style line endings" option.

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/install_7.jpg)

*   Select "Use MinTTY (the default terminal of MSYS2)".

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/install_8.jpg)

*   Check "Enable file system caching"

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/install_9.jpg)

*   Wait for files to install!

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/install_10.jpg)

<a name="terminal"></a>

## Get Started Using Terminal

**Mac/Ubuntu users:** When you open Terminal, you will see a window like this:

![:Blank Console](http://fundamentals.generalassemb.ly/assets/Graphics/terminal_blank.gif)

> Practice using Spotlight to open files and applications on your computer. It'll make you efficient as you navigate back and forth often between Terminal, your text editor, and your browser.

Open up a terminal with Bash. To do this on a Mac, press **⌘ + Space** to bring up Spotlight, then type in "terminal" and press **Return**.

**Windows users:** When you open Git Bash, you will see a window like this:

![:Git Website](http://fundamentals.generalassemb.ly/assets/chapter1/git_bash/git_bash.gif)

Double click on the Git Bash icon to open a new session.

* * *

The Terminal window is where you'll tell the computer what to do, and where the computer will display its reply. Let's break this window down:

*   The **prompt** is the that automatically shows up on the end of the first line. It's the command line equivalent of "stand-by" and indicates Terminal is ready to accept your **command**. We'll learn a few commands later in this lesson.

*   The **cursor** follows the prompt and the text you type will appear here. Just like in every other setting where you've ever seen a cursor.

*   The **username** of the person logged in precedes the prompt, and as you can see above, this user is named _Sarah_.

* * *
* * *

## How Your Computer is Organized

Before we tell the computer what to do, it's important we understand what it is we will be manipulating. You're probably used to seeing a graphical representation of files and folders as icons in a list or in columns.

![Folders in the GUI](http://fundamentals.generalassemb.ly/assets/chapter1/FileSystem.gif)

The way your computer organizes and stores files is called a **file system**. Let's take a minute to learn the vocabulary developers use to talk about the **file system**.

*   In programming-speak, all folders are called **directories**.

![Directories](http://fundamentals.generalassemb.ly/assets/chapter1/directory.png)

*   A directory within another directory is called a **subdirectory**.

*   A directory that contains a subdirectory or file is called a **parent directory**.

![Subdirectory and Parent Directory](http://fundamentals.generalassemb.ly/assets/chapter1/subdirectories.png)

*   The top-most directory of the filesystem is called the **root directory**. All files and directories are contained within the **root directory**, so they all share the same root.

![Root Directory](http://fundamentals.generalassemb.ly/assets/chapter1/root_directory.png)

For the purposes of this lesson, the root directory of everything on your computer is your home directory. It's aptly represented in the GUI by a house icon (if you're using a Mac).

![Home Directory](http://fundamentals.generalassemb.ly/assets/chapter1/home.png)

* * *

We know how file and directories appear in the GUI. Let's find our way around this system on the command line.

Before we get started, it's important to point out that, as smart as they seem, computers are really dumb. To ask for a specific directory or file in command line, we need to write out a precise address (called a **path**) so that the computer knows exactly where to find it.

For example, if you Google directions to "Main Street," without any additional information, Google wouldn't know which of the 10,466-plus Main Streets you want. Google might venture a guess, but your command line isn't as smart.

We have to be more specific when interacting with our computer on the command line.

Your computer understands two kinds of addresses or paths: absolute and relative.

*   An **absolute path** starts from the root. It's analogous to identifying a location on earth by latitude and longitude. The point on earth represented by (0, 0) is somewhere out in the middle of the Atlantic ocean. This (0,0) point never changes - it is a standard reference point, or "the root," from which we describe all locations on earth. If someone gave you the coordinates for a street in Paris, theoretically, you could start at (0, 0) and make your way north and east until you get there. **In this case you are defining where you're going from the root, so you're using an absolute path.**

*   On the other hand, if you were standing on a street corner in Anchorage, Alaska and wanted to head to the library, you wouldn't need the latitude and longitude. You could just jump in a taxi and say "Please head back two blocks, cut over to 3rd, and then turn right on Main Street." **In this case, you're defining where you're going based on your current location, so you're using a relative path.**

> It's important to know where you're working from so that you know whether to communicate with your computer using absolute or relative paths.

* * *


## Navigating the Command Line

We can perform actions using the command line by **entering commands**. There is a command to perform virtually any action you can imagine on your computer!

There are commands to open an application, create new files, copy files from one place to another, and a lot more.

Let's start typing commands together. In your open Terminal window, type `hello?` and press enter:

    $ hello?

Your terminal should respond rudely:

    -bash: hello?: command not found

This is the way your computer tells you that it did not understand the command that you typed in. Remember, we have left the GUI world behind us, so we will no longer have pretty warning messages and alert boxes. Do not worry! In due time, as we grow comfortable in this new environment, even these cryptic messages will be just as beautiful as any warning box you'll ever see.

Try typing this into your terminal:

    $ Where am I?

Again, a rude response:

    -bash: Where: command not found

Great. We've established that our command line doesn't understand plain English. We will have to use special words to make up our commands. Let's try this one:

    $ pwd

Whoa! It looks like our computer understood that one! It replied with a message like:

    /Users/corneliusfinch

(Note: On your machine, you should have seen `corneliusfinch` replaced with your username!)

If you're following along in **Git Bash on Windows**, this should look similar but slightly different:

    /c/Users/corneliusfinch

What did we just do?

The command `pwd` stands for "Print Working Directory".

This command is used when we want the command line to tell us what folder (or directory) of our computer we are currently in.

Just like the Finder on a mac, your command line interface (CLI) places you in a particular folder of your computer. `pwd` tells you where you currently are in your filesystem. Usually, when you open the Terminal application, you start off in your "home folder", which is the one that shares the name of your username on your computer.

If we were using Finder, we'd be able to see what files and folders are present in this folder. In a CLI however, if we want to see what files and folders exist in the current location, we need to ask for that with another command.

Let's find out what files are in the folder that we're in.

    $ ls

Lo and behold, the contents of the folder you are in:

    Applications       Desktop          Documents
    Downloads          Library          Movies
    Music              Pictures         Public

(Note: Again, on your machine, since you may have different files and folders, you may see a additional files and folders when you enter `ls`!)

If you're following along in **Git Bash on Windows**, it's alright if the files and folders that are listed out look a little different, but you should still see similar folders such as `Desktop`, `Documents`, and `Downloads`.

The `ls` command, which loosely stands for "list", lists the contents of a folder.

It looks like there are some folders in here. Let's find out what's inside our `Documents` folder. In order to do so, let's first navigate to the Documents folder.

    $ cd Documents

We have now navigated to the Documents folder.

The `cd` command, which stands for "change directory", is used to navigate to a particular folder on your computer.

This is equivalent to double-clicking the Documents folder in Finder to "go inside it". We can check that we're in the right place by using `pwd`.

    $ pwd
    /Users/corneliusfinch/Documents

Excellent! Now let's find out what's in here, using `ls`.

    $ ls
    funny_cat_picture.jpg
    office_stuff
    world_domination_checklist.txt

(Note: Again, your machine means you will probably see different files and folders!)

In our example, it looks like the `Documents` folder contains a JPG file of a funny cat, a folder full of "office stuff", and a text file that supposedly contains a checklist for world domination. Your `Documents` folder probably contains something different.

Now that we've investigated our `Documents` folder, let's go back up to our home folder. Since the home folder contains the `Documents` folder, we can say that the home folder is the "parent directory" of the `Documents` folder.

    $ cd ..

> `..` (two periods, or "dot-dot") is how we say to our command line "parent directory".

Many commands consist of three parts: the command, followed by flags (aka options), and finally, arguments.

    $ command -flag -otheroption

As the name implies, flags set options to tell the command how to do what it's about to do. There may be zero or more options. Options usually start with one or two dashes. Usually one dash is for a short one letter abbreviation, while two dashes is for long name for the option.

[http://catb.org/esr/writings/taoup/html/ch10s05.html#id2948149](http://catb.org/esr/writings/taoup/html/ch10s05.html#id2948149)

For example:

    $ ls -a

Will list _all_ files in a directory, which includes hidden files (files whose name begins with a `.`).

    $ cd Downloads

Calls the command `cd` to change directory. It is provided the option of where to navigate to.

Give it a try!

* * *

## Your Turn

We've gone ahead and created a new directory for you, called _World_. Download it [here](http://generalassembly.github.io/prework/assets/activity/World.zip).

When you double-click on the zip file, it will create a new folder next to the zip file in your Downloads folder.

Now that you can picture where the file is located, open the Terminal application

Using the command line alone,

1.  Navigate into your `Downloads` directory

2.  Move into the `World` directory from the `Downloads` directory

3.  List the contents of the `World` directory

4.  In one of the six continents within the `World` directory is a hidden file, `.carmen_sandiego.png`. Using only the command line, find out where in the World is Carmen Sandiego.

_Don't delete the World folder yet! We'll be working with it in another exercise in this unit._

> _Stuck? Check out the solutions at the bottom to see what you can do._

* * *

## Creating files and folders

We now know how to find our way around this mysterious world called the command line. Let's perform some lasting actions, like creating some files and folders. Before we start, let's make sure that we are in our home folder like so:

    $ cd ~

> `~` (tilde) is a shortcut to refer to your home folder. This is the folder on your computer that contains your Downloads, Pictures, and Documents folders. Each user on any given computer will have their own home folder.

The command above, regardless of where we currently are, will take us to our home folder.

Great! Now that we're in our home folder, let's create a file.

    $ touch joke.txt

The `touch` command creates files for us - in this case, we made a file called `joke.txt`. If we try to `touch` a file that already exists, the file will not be overwritten.

Let's open `joke.txt` in our default text editor so we can write a joke in it. Can we do that from our command line? Of course!

    $ open joke.txt

If you're following along using **Git Bash on Windows**, that probably didn't work! Instead, you'll want to use the following command to open the file. To do so, just type name the file you want to open:

    $ joke.txt

Your text editor should open up this file now. Go ahead and type this hilarious joke in there:

    A man walks into a bar. The other one ducks.

Now that you have a joke, save that file, quit your text editor application, and return to your command line.

Let's see what's inside our `joke.txt` file now.

    $ cat joke.txt

There's our joke!

    A man walks into a bar. The other one ducks.

We should probably make a folder called `funny_things` to put this joke in.

    $ mkdir funny_things

The `mkdir` command is used to create a specified folder. If the specified folder already exists, it will not be overwritten.

## Moving and Removing Things

Before we move on, let's navigate to our home folder.

    $ cd ~

We made a folder for our joke called `funny_things` (you can check that it is there by running the `ls` command). How do we move our `joke.txt` file into this folder? If we were using Finder, we might use our mouse to drag and drop `joke.txt` into `funny_things`. Can we achieve the same action with our command line? Of course!

    $ mv joke.txt funny_things/

Voila! Our hilarious joke has been moved, rightfully, into the `funny_things` folder.

> The `mv` command moves the specified files or folders to the specified destination.

This is the first time we've used a command that needed two pieces of information from us, or two arguments. The first argument is "what to move", and the second argument is "where to move it to".

> Notice how we specified we were moving our `joke.txt` into `funny_things/`. The `/` on the end of our folder's name specifies that this is a folder; not a file! Without it, you may unexpectedly rename your `joke.txt` to a new file called `funny_things`!

Let's navigate to our `funny_things` folder and check the contents to make sure that this worked.

    $ cd funny_things
    $ ls

Copying files is similar to moving them. Let's make a copy of our joke.

    $ cp joke.txt joke2.txt

> The `cp` command is used to copy the specified files or folders to the specified location.

After running this command, we have created a copy of `joke.txt` called `joke2.txt` in the same folder. In this case, notice how, the second argument was a filename and not a folder name. It turns out that the `mv` and `cp` commands are quite smart. When moving or copying a file, if the second argument is a **folder**, the specified file is moved or copied to that folder. If the second argument is a **filename**, the file in the first argument is moved or copied to a file with the filename specified in the second argument. Hence, when we copied our joke, our file `joke.txt` was copied to another file called `joke2.txt`.

Perhaps we should make another folder inside `funny_things` called `jokes`, and put our joke in there. After all, we could have funny jokes, funny pictures, and much more. In order to achieve this, we're going to follow a series of long-winded steps so we may familiarize ourselves with some more useful commands.

First, we're going to get rid of our duplicate joke file.

    $ rm joke2.txt

> The `rm` command, which stands for remove, deletes the specified files from your computer. `rmdir` (remove directory), deletes specified folders if they are empty. **Be careful with these commands!** These actions do not move files to your Trash, where you can recover them. These actions **permanently remove** the specified files and folders. They are **irrecoverable**.

Now that all the copycats are out of the way for good, let's make a `jokes` folder and put our joke inside.

    $ mkdir jokes
    $ mv joke.txt jokes/joke.txt

If you are trying to copy or remove folders, and not files, we need to add "an option" to our command. Options are extra settings that we want to apply to our commands. Options given to commands are always of the format `--word` or `-letter`. For example, let's try to copy our jokes folder.

    $ cp -r jokes copy_of_jokes

> The `-r` option stands for "recursive", and must be applied to the `cp` command when copying folders.

This is because not only do we want to copy the folder, we also want to recursively copy the contents of that folder, and the contents of any folders inside as well.

The same principle applies when removing a folder with files. The `rm -r` command will remove all of a folder's content as well as the folder itself.

    $ rm -r copy_of_jokes

Note that the `mv` command does not need a `-r` option to move folders.

Here's another exercise for you - give it a shot.

* * *

* * *

##  Your Turn

Part 1:

1.  Open up the terminal application

2.  Navigate into your Downloads directory

3.  Move the World directory that you downloaded in the previous from Downloads to your home directory.

4.  Check to see if you successfully moved the World directory by listing the contents of your home directory

Part 2:

You may have noticed that we neglected to include Antarctica in the `World` directory. Go ahead and correct this mistake straight from command line:

1.  Make sure you're in the `World` directory within your home directory

2.  Make a new directory titled `Antarctica` inside the `World` directory

3.  To be sure you created the directory in the right place, list the contents of the `World` directory

4.  If you haven't already, change back into the `World` directory

5.  List the contents of `South_America`. There should be three country directories, Argentina, Brazil, and Chile.

6.  Move the contents of `South_America` into the `North_America` folder

7.  Delete the now empty `South_America` directory

8.  Change the name of `North_America` to `Americas`

> Stuck? Check out the [solutions] at the bottom of the document to see what you can do.

* * *

## Command Line Cheat Sheet

#### Command Line

*   A text-based interface.
*   _Synonyms_: command-line interface (CLI), console

#### Terminal

*   An OSX application that provides text-based access to the operating system.
*   Any device or application used for data entry and display in a computer system.
*   _Synonyms_: client, computer terminal, terminal emulator

#### File System

*   A file system is a systematic way to control how information is stored and retrieved. It describes where one piece of information stops and where the next one begins. Each file system has its own structure and logic.
*   _Synonyms_: NTFS (Windows' File System), HFS+ (Apple's File System), file allocation table, GFS (Global File System)

#### Directory

*   An organizational unit, or container, used to organize computer files into a hierarchical structure.
*   _Synonyms_: folder, catalog, drawer

#### Path

*   A sequence of symbols and names that identifies a file or directory. The path always starts from your working directory or from the root directory, and each subdirectory is followed by a forward slash.
*   An _absolute_ or full path begins with the root directory and specifies every directory above the terminating file or directory name.
*   A _relative_ path does not include the root or parent directory names, and refers to a file or directory directly below the current working directory.
*   _Synonyms_: pathname

#### Command

*   The action we want the computer to take; always a single word.
*   _Synonyms_: utility

#### Option

*   Follows the "command" in a command line; used to modify the behavior of the command in some way.
*   _Synonyms_: flag

#### Argument

*   Follows the "command" and "options" (if any) in a command line and is used to explain what we want the command to act on.
*   The number of arguments used generally depends on the command: some don't need arguments, some require exactly one argument, some require lots of arguments, and some are flexible in the number they can take.

<table>

<thead>

<tr>

<th>Command</th>

<th>Description</th>

</tr>

</thead>

<tbody>

<tr>

<td>`pwd -options`</td>

<td>Prints the working directory; returns the absolute path name of the current directory</td>

</tr>

<tr>

<td>`ls [-options] [path/to/directory]`</td>

<td>Lists directory contents</td>

</tr>

<tr>

<td>`cd [-options] [path/to/directory]`</td>

<td>Changes the current working directory to the specified directory</td>

</tr>

<tr>

<td>`mkdir [-options] [path/to/directory]`</td>

<td>Makes a new directory</td>

</tr>

<tr>

<td>`rm -r [path/to/file] [path/to/file] ...`</td>

<td>Removes directories or files permanently</td>

</tr>

<tr>

<td>`mv [-options] [path/to/file] [path/to/directory]`</td>

<td>Moves directories or files to a new local</td>

</tr>

<tr>

<td>`mv [-options] [path/to/file] [NEW_FILE_NAME]`</td>

<td>Renames a file or directory</td>

</tr>

</tbody>

</table>

On Mac, your Terminal comes with a manual, and to access more (_a lot more_) information about any command, type `man` followed by the command name and press <kbd>Enter</kbd>:

![manual](http://fundamentals.generalassemb.ly/assets/chapter1/terminal_man.gif)

You can scroll through a manual entry with the arrow keys or space bar. To quit this view and return to your prompt, just type `q`.

* * *

## Solutions
### 6.2.1

1.  `$ cd Downloads`
2.  `$ cd World`
3.  `$ ls`
4.  `$ ls -a Europe`

### 6.2.1

Part 1:

1.  Command + Space. Inside search bar type "Terminal"
2.  `$ cd Downloads`
3.  `$ mv World ..` (will move to parent directory, in this case the Desktop)
4.  `$ ../` (move back to the parent directory) and then `$ ls`

Part 2:

1.  `$ cd World`
2.  `$ mkdir Antarctica`
3.  `$ ls`
4.  `$ cd World (only if pwd if not World)`
5.  `$ cd South America` `$ ls`
6.  `$ mv Argentina ../North_America` `$ mv Chile ../North_America` `$ mv Brazil ../North_America`
7.  `$../ (back to World Directory)` `$ rm -r South_America`
8.  `$ mkdir Americas` `mv North_America Americas`

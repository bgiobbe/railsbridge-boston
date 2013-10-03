# Using the Command Prompt

There are three commands that we'll be using at a command prompt to navigate the filesystem on your computer:  

```text
ls
pwd
cd
```

`ls` lists the contents of a directory.  
`pwd` gives the full directory path to your current directory.  (It stands for "print working directory".)  
`cd` moves you into a new directory. (It stands for "change directory".)

Let's practice using these commands.  

## Open a command prompt
**OS X**

You can find the Terminal application through Spotlight (click the magnifying glass in the top right of the screen and start typing "Terminal"), 
or navigate to `Applications/Utilities/Terminal` in Finder.

If you installed `vagrant`, type the following commands into the Terminal 
window to get to the command prompt of your Ruby development environment:

```text
cd ~/rbb
vagrant up
vagrant ssh
```

**Windows**

Open a Command Prompt window. You can find the Command Prompt application through 
the Start Menu, All Programs, probably in Accessories.

Type the following commands into the window to get to the command prompt of
your Ruby development environment:

```text
cd rbb
vagrant up
vagrant ssh
```

**Linux**

Ubuntu: Click the Ubuntu logo and start typing "Terminal".  
Fedora: From the Main Menu bar select "Applications > System Tools > Terminal".


### Practice using `ls`, `pwd`, and `cd`

Type each of these commands and hit enter:

This lists all the files in your home directory (ls is short for 'list'):

```text
ls
```


This displays the full directory path to your current directory, which is your home directory (pwd stands for Print Working Directory):

```text
pwd
```

This will change you into the `/` top-level (or 'root') directory ('cd' stands for Change Directory): 

```text
cd /
```


This lists the contents of the `/` root directory:

```text
ls
```


This will change you into the `Users` subdirectory of the `/` root directory:

For OS X, Linux:

```text
cd Users    
```

For Windows:

```text
cd /c/Users 
```


Now that you are in the 'Users' directory, list all the files there.
You should see a list of all the files in `/Users`, including the directory for your username—your home directory:

```text
ls
```


Print the working directory again. This displays the full directory path to your current directory, `/Users`:

```text
pwd
```


Change directories to the parent of the current directory.
`..` means "parent directory", so this command moved you up to the parent directory. 
You were in `/Users`, so now you are in `/`, the root directory:

```text
cd ..
```

This lists the contents of the '/', root directory, confirming where you are.

```text
ls
```


### Tab Completion
You can use Tab to auto-complete directory and file names. 
So from inside the root directory, if you type `cd U` and hit Tab, the command prompt will auto-complete the directory
name as much as it can.  

### Spaces in File and Folder Names
It's ok to include a space in a file or folder name, but it's a little tricky on the command line.
The command line expects a space means the end of a name, and you have to do extra work to show you mean a space.
Suppose you want to go to a folder called "My Files".

- The easiest way: type the beginning of the name and hit Tab for auto-complete.

```text
cd My<TAB>
```

- You can put the name inside double quotes or single quotes.

```text
cd "My Files"
cd 'My Files'
```

- You can put a backslash before the space. This is called "escaping".
It turns any character that the command line treats as special back into the un-special character. Space, backslash, and
single and double quotes are all special, and you'd write them as \ , \\, \', and \".

```text
cd My\ Files
```

- You can use a '\*', the wildcard character. Type in the beginning or end of the name and a \*
where it should fill in the blank, and hit Enter. If more than one file matches that pattern, you may get an error,
or the command line may pick the first match.

```text
cd My\*Files
cd My\*les
cd My\*
```


### Command History
The command prompt also maintains a command history. You can use the up arrow to cycle through old commands.

### Success!
You've practiced using `ls`, `pwd`, and `cd` to navigate your computer's filesystem from the command prompt.

[«Back](/installfest)

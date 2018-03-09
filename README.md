# DirectoryTree
Simple C program to display a graphical illustration of the directory tree of a current or given location.

The main distribution for tree is [here](http://mama.indstate.edu/users/ice/tree/). Tree was originally written by Steve Baker (ice@mama.indstate.edu) and has been further developed upon since.

I modified Tree to implement a **Happy Friday** directory display. Any file in the directory pointed to that was **last modified** on a Friday will display the 'HAPPY FRIDAY!!!' message infront of its name when tree.c is ran.

## Setup

To begin with, clone the repo.
```
git clone https://github.com/dooleyb1/DirectoryTree
```

Compile and build the code.
```
make
```

## Example

```
./tree
.
├── CHANGES
├── color.c
├── color.o
├── doc
│   ├── tree.1
│   ├── tree.1.fr
│   └── xml.dtd
├── fridaytree.c
├── fridaytree.o
├── hash.c
├── hash.o
├── html.c
├── html.o
├── INSTALL
├── json.c
├── json.o
├── LICENSE
├── Makefile
├── README
├── README.md
├── strverscmp.c
├── tree
├── tree.c
├── tree.h
├── tree.o
├── unix.c
├── unix.o
├── xml.c
└── xml.o

1 directory, 28 files
```


## HAPPY FRIDAY!!! Example
```
./tree -Z
.
├── CHANGES
├── HAPPY FRIDAY!!! color.c
├── HAPPY FRIDAY!!! color.o
├── doc
│   ├── tree.1
│   ├── tree.1.fr
│   └── xml.dtd
├── fridaytree.c
├── fridaytree.o
├── HAPPY FRIDAY!!! hash.c
├── HAPPY FRIDAY!!! hash.o
├── html.c
├── html.o
├── INSTALL
├── json.c
├── json.o
├── LICENSE
├── Makefile
├── HAPPY FRIDAY!!! README
├── README.md
├── strverscmp.c
├── tree
├── tree.c
├── tree.h
├── tree.o
├── HAPPY FRIDAY!!! unix.c
├── HAPPY FRIDAY!!! unix.o
├── xml.c
└── xml.o

1 directory, 28 files
```

## Usage
```
usage: tree [-acdfghilnpqrstuvxACDFJQNSUX] [-H baseHREF] [-T title ]
	[-L level [-R]] [-P pattern] [-I pattern] [-o filename] [--version]
	[--help] [--inodes] [--device] [--noreport] [--nolinks] [--dirsfirst]
	[--charset charset] [--filelimit[=]#] [--si] [--timefmt[=]<f>]
	[--sort[=]<name>] [--matchdirs] [--ignore-case] [--] [<directory list>]

  ------- Listing options -------
  -Z            Any files modified on a Friday display 'HAPPY FRIDAY!!!'
  -a            All files are listed.
  -d            List directories only.
  -l            Follow symbolic links like directories.
  -f            Print the full path prefix for each file.
  -x            Stay on current filesystem only.
  -L level      Descend only level directories deep.
  -R            Rerun tree when max dir level reached.
  -P pattern    List only those files that match the pattern given.
  -I pattern    Do not list files that match the given pattern.
  --ignore-case Ignore case when pattern matching.
  --matchdirs   Include directory names in -P pattern matching.
  --noreport    Turn off file/directory count at end of tree listing.
  --charset X   Use charset X for terminal/HTML and indentation line output.
  --filelimit # Do not descend dirs with more than # files in them.
  --timefmt <f> Print and format time according to the format <f>.
  -o filename   Output to file instead of stdout.

  -------- File options ---------
  -q            Print non-printable characters as '?'.
  -N            Print non-printable characters as is.
  -Q            Quote filenames with double quotes.
  -p            Print the protections for each file.
  -u            Displays file owner or UID number.
  -g            Displays file group owner or GID number.
  -s            Print the size in bytes of each file.
  -h            Print the size in a more human readable way.
  --si          Like -h, but use in SI units (powers of 1000).
  -D            Print the date of last modification or (-c) status change.
  -F            Appends '/', '=', '*', '@', '|' or '>' as per ls -F.
  --inodes      Print inode number of each file.
  --device      Print device ID number to which each file belongs.

  ------- Sorting options -------
  -v            Sort files alphanumerically by version.
  -t            Sort files by last modification time.
  -c            Sort files by last status change time.
  -U            Leave files unsorted.
  -r            Reverse the order of the sort.
  --dirsfirst   List directories before files (-U disables).
  --sort X      Select sort: name,version,size,mtime,ctime.

  ------- Graphics options ------
  -i            Don't print indentation lines.
  -A            Print ANSI lines graphic indentation lines.
  -S            Print with CP437 (console) graphics indentation lines.
  -n            Turn colorization off always (-C overrides).
  -C            Turn colorization on always.

  ------- XML/HTML/JSON options -------
  -X            Prints out an XML representation of the tree.
  -J            Prints out an JSON representation of the tree.
  -H baseHREF   Prints out HTML format with baseHREF as top directory.
  -T string     Replace the default HTML title and H1 header with string.
  --nolinks     Turn off hyperlinks in HTML output.
  ---- Miscellaneous options ----
  --version     Print version and exit.
  --help        Print usage and this help message and exit.
  --            Options processing terminator.
```
# Scripts/Makefile for CSCI-262: Data Structures
To install, clone this git repo onto your system:

    $ git clone https://github.com/jackrosenthal/mines-csci-makefiles

Then add the mines-csci-makefiles/CSCI-262 folder to your path in your `.zshrc` or `.bashrc`:

    ...
    export PATH="$PATH:$HOME/edit/this/path/mines-csci-makefiles/CSCI-262"
    ...

To use the Makefile, just copy it to your assingnment directories when you make them, then
edit the makefile and read the comments.

Requires Python 3 and the requests library for Python 3.

## Usage
### Labs
To test your labs: (using digitsum as an example)

    $ labtest digitsum

### Assignments

Self explanitory... your commands are:

    $ make

    $ make clean

    $ make zip

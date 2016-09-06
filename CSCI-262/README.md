# Scripts/Makefile for CSCI-262: Data Structures
These make your life so much easier... not even kidding. Makefile automatically installs Stanford
CPPLib for you and gives you a script to view documentation. `labtest` runs your labs on the test
server and gives you successes/failures.

## Installation
To install, clone this git repo onto your system:

    $ git clone https://github.com/jackrosenthal/mines-csci-makefiles

Then add the `mines-csci-makefiles/CSCI-262` folder to your path in your `.zshrc` or `.bashrc`:

    ...
    export PATH="$PATH:$HOME/edit/this/path/mines-csci-makefiles/CSCI-262"
    ...

To use the Makefile, just copy it to your assignment directories when you make them, then
edit the makefile and read the comments.

Requires Python 3 and the requests library for Python 3.

## Usage
### Stanford Library Viewer
Viewing documentation for the Stanford library, requires w3m:

    $ stanman           # View all of the documentation
    $ stanman Map       # View a specific page (ex. Map)

### Assignments Makefile

Self explanatory... your commands are:

    $ make              # Compile your code. Installs Stanford CPPLib if not installed yet.
    $ make run          # Run your code, compile if it needs it
    $ make clean        # Clean out code binaries
    $ make libclean     # Remove the Stanford CPPLib so it will be reinstalled on next run
    $ make zip          # Zip up your code

`make run` also supports passing command line arguments:

    $ make run ARGS="arg1 arg2 arg3 ..."

# Scripts/Makefile for CSCI-262: Data Structures
These make your life so much easier... not even kidding. Makefile Automatically installs Stanford
CPPLib for you and gives you a script to view documentation. `labtest` runs your labs on the test
server and gives you successes/failures.

## Installation
To install, clone this git repo onto your system:

    $ git clone https://github.com/jackrosenthal/mines-csci-makefiles

Then add the `mines-csci-makefiles/CSCI-262` folder to your path in your `.zshrc` or `.bashrc`:

    ...
    export PATH="$PATH:$HOME/edit/this/path/mines-csci-makefiles/CSCI-262"
    ...

To use the Makefile, just copy it to your assingnment directories when you make them, then
edit the makefile and read the comments.

Requires Python 3 and the requests library for Python 3.

## Usage
### Scripts
To test your labs: (using digitsum as an example)

    $ labtest digitsum

Viewing documentation for the stanford library, requires w3m:

    $ stanman           # View all of the documentation
    $ stanman Map       # View a specific page (ex. Map)

### Assignments

Self explanitory... your commands are:

    $ make              # Compile your code. Installs Stanford CPPLib if not installed yet.
    $ make clean        # Clean out code binaries and Stanford CPPLib
    $ make zip          # Zip up your code

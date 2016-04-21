# Makefile for shell

# Specify your compiler and linker
CXX = gcc
LD = $(CXX)

# Output binaries appear in bin/
# Sources all .c files from src/
SRCFILES = $(wildcard src/*.c)
OBJFILES = $(patsubst src/%.c, bin/%.o, $(SRCFILES))
OBJDEBUG = $(patsubst src/%.c, bin/%.debug.o, $(SRCFILES))

# Output file name
OUTFILE = MyShell

# Flags for the compiler and for the linker
CXXFLAGS = -Wall -xc -std=c11
LDFLAGS = -lreadline

all: $(OUTFILE)

$(OUTFILE): $(OBJFILES)
	$(LD) $(LDFLAGS) $(OBJFILES) -o $(OUTFILE)

bin/%.o: src/%.c
	$(CXX) $(CXXFLAGS) -o $@ -c $<

# Type 'make debug' to open gdb on your shell, creates MyShell.debug
debug: $(OUTFILE).debug
	gdb -tui $(OUTFILE).debug

$(OUTFILE).debug: $(OBJDEBUG)
	$(LD) $(LDFLAGS) $(OBJDEBUG) -o $(OUTFILE).debug

bin/%.debug.o: src/%.c
	$(CXX) $(CXXFLAGS) -ggdb3 -o $@ -c $<

clean:
	rm -f bin/*.o
	rm -f $(OUTFILE)
	rm -f $(OUTFILE).debug

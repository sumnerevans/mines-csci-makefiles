# List all the cpp files you would like this makefile to compile into a single
# file below...
# Additionally, write the name of the output binary
TARGETS=imgeditor.cpp strio.cpp
OUTFILE=imgeditior
# Set your compiler
CXX=clang++ -g -std=c++14 -Werror -Wall

all:
	$(CXX) -o $(OUTFILE) $(TARGETS)

zip:
	zip $(OUTFILE).zip $(TARGETS)

clean:
	rm $(OUTFILE)

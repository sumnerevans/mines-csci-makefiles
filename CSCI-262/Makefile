# List all the cpp files you would like this makefile to compile into a single
# file below...
# Additionally, write the name of the output binary
TARGETS=imgeditor.cpp strio.cpp
OUTFILE=imgeditor
# Set your compiler, stanford library must be complied with g++ for some very odd reasons anyway
CXX=clang++ -g -std=c++11

all: $(OUTFILE)

$(OUTFILE): $(HOME)/.lib/cpplib/cpplib.o
	@echo Compiling your code...
	$(CXX) -I$(HOME)/.lib/cpplib/include -o $(OUTFILE) $(TARGETS) -L $(HOME)/.lib/cpplib/cpplib.o

$(HOME)/.lib/cpplib/cpplib.o: $(HOME)/.lib/cpplib
	@echo Compiling stanford cpp library... This may take a while...
	@g++ -std=c++11 -I$(HOME)/.lib/cpplib/include -o $(HOME)/.lib/cpplib/cpplib.o $(shell find $(HOME)/.lib/cpplib/src -name \*.cpp -not -name main.cpp)
	@echo -e

$(HOME)/.lib/cpplib:
	@mkdir -p $(HOME)/.lib
	@wget -O$(HOME)/.lib/cpplib.zip http://eecs.mines.edu/Courses/csci262/resources/StanfordCPPLib/cpplib.zip
	@unzip -d $(HOME)/.lib -q -o $(HOME)/.lib/cpplib.zip
	@rm $(HOME)/.lib/cpplib.zip

run: $(OUTFILE)
	./$(OUTFILE) $(ARGS)

zip:
	zip $(OUTFILE).zip $(TARGETS) *.h *.hpp README

clean:
	-rm -f $(OUTFILE)

libclean:
	-rm -rf $(HOME)/.lib/cpplib

# Change this to the assignment number
HWNO=1
# On the next line, insert a # depending on how many labs you have for this assignment
TARGETS=HW$(HWNO) Lab$(HWNO)a Lab$(HWNO)b Lab$(HWNO)c
# This makes the DIRS variable with src/ in front of all the targets
DIRS=$(addprefix src/,$(TARGETS))
# Change this to wherever the template file you want for main.cpp is located on your system
TEMPLATE=~/classes/cs/261/template.cpp
# I like clang++ personally, but if you want to use g++, change this
# If you're debating clang or GCC, clang gives you pretty compile errors
CXX=clang++

# That's all you have to configure. Make sure to install SFML on your system:
# Arch Linux:
#     sudo pacman -S sfml
# Debian/Ubuntu/Mint:
#     sudo apt-get install libsfml-dev
# Fedora:
#     sudo yum install SFML
#
# macOS / OS X using Homebrew:
#     sudo brew install sfml
#
# And come to LUG!

all: $(TARGETS)

%: src/%/*.cpp
	$(CXX) -Wall -Werror -g -std=c++11 -o $(@) $(^) -lsfml-system -lsfml-graphics -lsfml-window

# If the zip submission format/name has changed since I took 261, please update this
# and submit a pull request!
zip:
	zip -r src$(HWNO).zip src/ -x *~

setup:
	mkdir -p $(DIRS)
	find src/* -type d -exec cp $(TEMPLATE) \{\}/main.cpp \;

clean:
	rm $(TARGETS)

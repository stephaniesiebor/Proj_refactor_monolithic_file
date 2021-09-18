# This is the makefile for refactoring the monolithic file
# Stephanie Siebor, 9/17/2021

CFLAGS = -Wall

#TODO link (-o) all object files into the executable myexe
all: fileio.o utils.o proj_refactor_file.o
	g++ $(CFLAGS) -o myexe fileio.o utils.o proj_refactor_file.o
	
#rebuild object file if fileio.cpp, or fileio.h or constants.h changes
#compile the .cpp file to an object file (-c)
fileio.o: ../fileio/fileio.cpp ../includes/fileio.h ../includes/constants.h
	g++ $(CFLAGS) -c ../fileio/fileio.cpp
	
#rebuild object file if utils.cpp or utils.h changes
#compile the .cpp file to an object file (-c)
utils.o: ../utils/utils.cpp ../includes/utils.h
	g++ $(CFLAGS) -c ../utils/utils.cpp
	
#rebuild object file if proj_refactor_file.cpp changes
#compile the .cpp file to an object file (-c)
proj_refactor_file.o: ../src/proj_refactor_file.cpp
	g++ $(CFLAGS) -c ../src/proj_refactor_file.cpp
	

#TODO type 'make clean' to remove myexe and all .o files	
clean:
	rm -f *.o myexe
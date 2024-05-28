# Makefile

# Compiler to use
CC = gcc

# Compiler flags
CFLAGS = -Wall -Werror -g

#-Wall: This flag enables all the commonly used warning messages about possible errors in the code.
#-Werror: This flag treats all warnings as errors. 
#-g: This flag includes debugging information in the compiled executable.


# Target executable
TARGET = lab2				#request: Using variable

# Object files
OBJ = lab2.o lab2_func.o		#request: All of the object files should be listed as part of the macro OBJ.
DEPS = lab2.h


# Default target: build the program
all: $(TARGET)
	@echo "The file name of the target of\
	the rule \"all\" is $@"		#request: using automatic variable
	@echo "Done"

# Rule to build the target executable
$(TARGET): $(OBJ)
	@$(CC) $(CFLAGS) -o $(TARGET) $(OBJ)

# Rule to build lab2.o
lab2.o: lab2.c $(DEPS)
	@$(CC) $(CFLAGS) -c lab2.c

# Rule to build lab2_func.o
lab2_func.o: lab2_func.c $(DEPS)
	@$(CC) $(CFLAGS) -c lab2_func.c

# Rule to run lab2.exe
run: 
	@./$(TARGET)

# Clean up the build
clean:					#request: Using target name clean to cleaning up your object file
	@rm -f $(OBJ) $(TARGET) *.exe

# Phony targets				#request: Using Phony Targets
.PHONY: all clean run

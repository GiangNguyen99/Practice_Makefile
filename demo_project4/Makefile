# Makefile

# Compiler to use
CC = gcc

# Compiler flags
CFLAGS = -Wall -Werror -g

#-Wall: This flag enables all the commonly used warning messages about possible errors in the code.
#-Werror: This flag treats all warnings as errors. 
#-g: This flag includes debugging information in the compiled executable.


INC_DIRS = ./include
SRC_DIRS = ./src
OBJ_DIRS = ./src/obj

# Target executable
TARGET = lab3				#request: Using variable

# Object files
OBJ = lab3.o lab3_func.o		#request: All of the object files should be listed as part of the macro OBJ.



#SRC_FILES = ./src/lab3.c ./src/lab3_func.c
SRC_FILES = $(foreach src_files_var, $(SRC_DIRS), $(wildcard $(SRC_DIRS)/*))

#INC_FILES = lab3.h
INC_FILES = $(foreach inc_files_var, $(INC_DIRS), $(wildcard $(INC_DIRS)/*))

#search path .c and .h files
vpath %.c $(SRC_DIRS)
vpath %.h $(INC_DIRS)





# Default target: build the program
all: $(TARGET)
	@echo "The file name of the target of\
	the rule \"all\" is $@"		#request: using automatic variable
	@echo "Done"

# Rule to build the target executable
$(TARGET): $(OBJ)
	@$(CC) $(CFLAGS) $(OBJ_DIRS)/*.o -o $(TARGET)

# Rule to build lab3.o
lab3.o: $(SRC_DIRS)/lab3.c $(INC_FILES )
	@$(CC) -I$(INC_DIRS) $(CFLAGS) -c $< -o $(SRC_DIRS)/obj/$@

# Rule to build lab3_func.o
lab3_func.o: $(SRC_DIRS)/lab3_func.c $(INC_FILES)
	@$(CC) -I$(INC_DIRS) $(CFLAGS) -c $< -o $(SRC_DIRS)/obj/$@

# Rule to run lab3.exe
run: 
	@./$(TARGET)

# Clean up the build
clean:					#request: Using target name clean to cleaning up your object file
	@rm -f $(OBJ_DIRS)/*.o *.exe

# Phony targets				#request: Using Phony Targets
.PHONY: all clean run

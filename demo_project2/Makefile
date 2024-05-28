# Makefile

# Compiler to use
CC = gcc

# Compiler flags
CFLAGS = -Wall -Werror -g

#-Wall: This flag enables all the commonly used warning messages about possible errors in the code.
#-Werror: This flag treats all warnings as errors. 
#-g: This flag includes debugging information in the compiled executable.


# Target executable
TARGET = lab1

# Object files
OBJ = lab1.o lab1_func.o

# Default target: build the program
all: $(TARGET)
	echo "Done"

# Rule to build the target executable
$(TARGET): $(OBJ)
	$(CC) $(CFLAGS) -o $(TARGET) $(OBJ)

# Rule to build lab1.o
lab1.o: lab1.c lab1.h
	$(CC) $(CFLAGS) -c lab1.c

# Rule to build lab1_func.o
lab1_func.o: lab1_func.c lab1.h
	$(CC) $(CFLAGS) -c lab1_func.c

# Rule to run lab1.exe
run: 
	@./$(TARGET)

# Clean up the build
clean:
	rm -f $(OBJ) $(TARGET) 

# Phony targets
.PHONY: all clean run

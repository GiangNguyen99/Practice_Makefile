#Makefile


PATH_OUTPUT = build

INC_DIRS = ./inc
SRC_DIRS = ./src


#SRC_FILE = ./src/main.c ./src/sum.c
SRC_FILES = $(foreach src_files_var, $(SRC_DIRS), $(wildcard $(SRC_DIRS)/*))
INC_FILES = $(foreach inc_files_var, $(INC_DIRS), $(wildcard $(INC_DIRS)/*))

OBJ_FILES := $(notdir $(SRC_FILES))
OBJ_FILES := $(subst .c,.o,$(OBJ_FILES))
PATH_OBJ := $(foreach OBJ_FILES, $(OBJ_FILES), $(PATH_OUTPUT)/$(OBJ_FILES))

#search path .c and .h files
vpath %.c $(SRC_DIRS)
vpath %.h $(INC_DIRS)

all: $(OBJ_FILES)


#generate object files

%.o: %.c $(INC_FILES)
	gcc -I$(INC_DIRS) -c $< -o $(PATH_OUTPUT)/$@
	
#main.o: .src/main.c
#	gcc -I.\inc -c .\src\main.c -o .\build\main.o

#generate executable file and run
build: $(OBJ_FILES)
	@gcc $(PATH_OBJ) -o $(PATH_OUTPUT)/main.exe
	@./$(PATH_OUTPUT)/main.exe

clean:
	@rm $(PATH_OUTPUT)/*

targets := target1 target3 target2 target4 target5

all_dot_c := $(wildcard *.c)

all: $(targets)
	echo "finished"

target1:
	echo "this is target1"
	touch target1
target2: main.i
	echo "this is target2"
	touch target2
	gcc -S main.i -o main.s
target3: $(all_dot_c)
	echo "this is target3"
	touch target3
	gcc -E main.c -o main.i
target4: main.s
	echo "this is target4"
	as main.s -o main.o
target5: main.o
	echo "this is target5"	
	gcc main.o -o main.exe
clean:
	rm -f $(targets)

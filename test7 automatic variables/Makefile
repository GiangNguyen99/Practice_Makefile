targets := target1 target3 target2

#all_dot_c := $(wildcard *.c)

all: $(targets)
	echo "finished"
target1:
	echo "target1: $'@' echo name of target"
	echo $@
target2: main.c func1.c
	echo "target2: $'<' echo name of the first prerequisite"
	echo $<
target3: main.c func1.c
	echo "target3: $'^' echo all the prerequisites"
	echo $^
clean:
	rm -f 

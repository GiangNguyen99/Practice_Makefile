#$(foreach var,list,text)

#$(notdir src/foo.c hacks)
#produces the result ‘foo.c hacks’.
cc := gcc

SRC_FILES := src/main.c src/foo.c src/helpers.c
OBJ_FILES := $(patsubst %.c,%.o,$(notdir $(SRC_FILES)))

all: $(OBJ_FILES)

%.o: src/%.c
	cc -c $< -o $@

%.o: src/%.c
	cc -c $< -o $@

%.o: src/%.c
	cc -c $< -o $@



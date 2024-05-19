#$(foreach var,list,text)

find_files = $(wildcard $(dir)/*)
dirs := a b c d
files := $(foreach dir,$(dirs),$(find_files))
all_target := target0 target1
all: $(all_target)
	echo "finished"

target0:
	echo "target0"
target1: $(files)
	echo "target1"
	echo "$^"
clean:
	rm -f $(files)


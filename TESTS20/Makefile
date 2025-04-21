.PHONY: all clean

all: 
	macro11 tests.mac -o tests.obj
	obj2bin.pl --rt11 --binary --bytes=100000 --outfile=- tests.obj | tail -c +7 | head -c -8 > tests.bin

clean:
	rm -f tests.obj
	rm -f tests.bin

.PHONY: all clean

all:
	macro11 micpul.mac -o micpul.obj
	obj2bin.pl --rt11 --binary --bytes=100000 --outfile=- micpul.obj | tail -c +7 | head -c -8 > micpul.bin

clean:
	rm -f micpul.obj
	rm -f micpul.bin

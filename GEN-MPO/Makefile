.PHONY: all clean

all: 
	macro11 genmpo.mac -o genmpo.obj
	obj2bin.pl --rt11 --binary --bytes=100000 --outfile=- genmpo.obj | tail -c +7 | head -c -8 > genmpo.bin

clean:
	rm -f genmpo.obj
	rm -f genmpo.bin

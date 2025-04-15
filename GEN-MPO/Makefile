.PHONY: all clean

all: 
	macro11 genmpo.mac -o genmpo.obj
	obj2bin.pl --rt11 --binary --nocrc --bytes=100000 --outfile=gmp.bin genmpo.obj
	dd if=gmp.bin of=genmpo.bin bs=1 skip=6
	rm gmp.bin

clean:
	rm -f genmpo.obj
	rm -f genmpo.bin

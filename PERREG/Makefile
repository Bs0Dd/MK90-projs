.PHONY: all clean

all:
	macro11 perreg.mac -o perreg.obj
	obj2bin.pl --rt11 --binary --bytes=100000 --outfile=- perreg.obj | tail -c +7 | head -c -8 > perreg.bin

clean:
	rm -f perreg.obj
	rm -f perreg.bin

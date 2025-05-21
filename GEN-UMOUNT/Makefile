.PHONY: all clean

all: basic10 basic20 gcreat.bin

basic10:
	mkdir basic10
	cat gumount.mac vars10.mac > basic10/gumou10.mac
	macro11 basic10/gumou10.mac -o basic10/gumou10.obj
	obj2bin.pl --rt11 --binary --bytes=100000 --outfile=- basic10/gumou10.obj | tail -c +7 | head -c -8 > basic10/gumount.bin
	
basic20:
	mkdir basic20
	cat gumount.mac vars20.mac > basic20/gumou20.mac
	macro11 basic20/gumou20.mac -o basic20/gumou20.obj
	obj2bin.pl --rt11 --binary --bytes=100000 --outfile=- basic20/gumou20.obj | tail -c +7 | head -c -8 > basic20/gumount.bin
	
gcreat.bin:
	macro11 gcreat.mac -o gcreat.obj
	obj2bin.pl --rt11 --binary --bytes=100000 --outfile=- gcreat.obj | tail -c +7 | head -c -8 > gcreat.bin
	cat basic10/gumount.bin >> gcreat.bin
	cat basic20/gumount.bin >> gcreat.bin

clean:
	rm -rf basic*
	rm -f gcreat.obj
	rm -f gcreat.bin

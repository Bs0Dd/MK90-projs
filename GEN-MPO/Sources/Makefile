.PHONY: smppro clean

smppro:
	./macro11 smppro.mac -o smppro.obj
	./obj2bin.pl --rt11 --binary --bytes=100000 --outfile=- smppro.obj | tail -c +7 | head -c -8 > smppro.bin

clean:
	rm -f smppro.obj
	rm -f smppro.bin

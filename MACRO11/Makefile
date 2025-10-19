.PHONY: project clean

project: 
	macro11 project.mac -o project.obj
	obj2bin.pl --rt11 --binary --bytes=100000 --outfile=- project.obj | tail -c +7 | head -c -8 > project.bin

clean:
	rm -f project.obj
	rm -f project.bin

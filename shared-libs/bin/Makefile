all: program

main.o: main.c
	gcc -g -Wall -I../libc -c $< -o $@

program: main.o 
	gcc -g -Wall $< -L../libc -lhello -o $@

clean:
	rm -f program *.o  
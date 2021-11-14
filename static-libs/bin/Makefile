all: program

test.o: test.c
	gcc -g -Wall -c $< -I../libc -o $@ 

# Notice *.o position in this step
program: test.o
	gcc -g -Wall $< -L../libc -lhello -o $@ 

clean:
	rm -f program *.o 
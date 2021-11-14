all: libhello.so

libhello.o: libhello.c
	gcc -g -Wall -fpic -c $< -o $@

libhello.so: libhello.o 
	gcc -g -Wall -shared -o $@ $<

clean:
	rm -f *.so *.o 


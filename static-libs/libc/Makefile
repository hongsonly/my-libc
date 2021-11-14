all: libhello.a 

# create a library object file that can be linked into other programs that use your library
# you can then use the libhello.o file as the "library file" and statically link it into other programs that use it, or...
libhello.o: libhello.c 
	gcc -g -Wall -o $@ -c $< 

libhello.a: libhello.o 
	ar -cvq $@ $<

clean: 
	rm -f *.a *.o

# C Libraries

In general, libraries are created from many library source files, and are either built as archive files (libmine.a) that are statically linked into executables that use them, or as shared object files (libmine.so) that are dynamically linked into executables that use them. To link in libraries of these types, use the gcc command line options -L for the path to the library files and -l to link in a library (a .so or a .a):
    -L{path to file containing library} -l${library name}

For example, if I have a library named libmine.so in /home/newhall/lib/ then I'd do the following to link it into my program:
   $ gcc -o myprog myprog.c  -L/home/newhall/lib -lmine 

You may also need to specify and include path so the compiler can find the library header file: -I /home/newhall/include
If you create your own shared object files and do not install them in /usr/lib, then you need to set your LD_LIBRARY_PATH environment variable so that the runtime linker can find them and load them at run time. For example, if I put my .so files in a directory named lib in my home directory, I'd set my LD_LIBRARY_PATH enviroment to the following:

  # if running bash:
  export LD_LIBRARY_PATH=/home/newhall/lib:$LD_LIBRARY_PATH

  # if running tcsh:
  setenv LD_LIBRARY_PATH /home/newhall/lib:$LD_LIBRARY_PATH

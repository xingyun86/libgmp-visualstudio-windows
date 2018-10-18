# MPIR

MPIR is built using VC9/VC11 projects files. No patch are necessary but to rename
the library to mpir__a.lib. Follow the instructions in the readme.txt in the
MPIR sources and build “lib_mpir_p4” to get the static library we use for PHP.

To build an ASM optimized version, you will have to install
[Yasm](http://www.tortall.net/projects/yasm/) assembler. Complete instructions
are available
[here](http://www.tortall.net/projects/yasm/wiki/VisualStudio2005).

### Building for PHP

PHP 5.4 and below requires the VC9 build of the MPIR library.<br>
PHP 5.5 and above requires the VC11 build of the MPIR library.

* cd win/
* 32 bit
 * configure --cpu=x86
* 64 bit
 * configure --cpu=x86_64 
* building
 * make
 * OR
 * make.vc11

### NOTE

If you plan to run PHP on a specific platform, the MPIR library can use the optimized assembler files. For more information on supported platforms see mpn\README. 


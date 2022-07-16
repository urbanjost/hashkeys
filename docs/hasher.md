NAME
====

**hasher**(1f) - \[M\_hashkeys\] exercise the string hash methods in the
**M\_hashkey**(3fm) module (LICENSE:PD)

SYNOPSIS
========

**hasher** \[ *input\_files* \[ **-hash** *hashname*\] \]\|\[
**-string** string\_value\]\|**--help**\|**--version**

DESCRIPTION
===========

**hasher**(1f) does a byte by byte hash of a file or a hash of a string
using the procedures available in the **M\_hashkey**(3fm) module. It is
up to the user to determine if the method is suitable for a specific
use.

When the I/O was not tuned at all and a simple byte-by-byte read was
used the program was sixty times slower; in addition the
**anything\_to\_bytes**(3f) function was slower than expected processing
one character at a time, so if you are going to do anything similar it
is at least worth a look to look at the sample code.

OPTIONS
=======

***input\_files***

:   files to generate a hash for

**hash**

:   name of hash algorithm. Currently allowed values are:

<!-- -->

                      djb2 (default)   calls djb2_hash(3f)
                      sdbm             calls sdbm_hash(3f)
                      crc32            calls cfc32_hash(3f)

****--help****

:   display this help and exit

****--version****

:   output version information and exit

AUTHOR
======

John S. Urban

LICENSE
=======

Public Domain

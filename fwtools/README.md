# Firmware tools

These are some simple tools to help you get started with reversing some firmware running on the TMS320C64x.

 * extractcoff.py will extract the a modified COFF file from inside a file containing the header described below
 * parsecoff.py will load a modified COFF file and extract all functions in the func/ subdir

Inside the parsecoff.py file you can find several python classes for loading and manipulating this modified COFF files.

# Header

The header must be equal to 128 bytes and have at least the following fields:
Bytes 0-3:   String 'MTCH'
Bytes 44-58: Name of the file
Bytes 60-63: Version of the file
Bytes 64-95: Description of the file

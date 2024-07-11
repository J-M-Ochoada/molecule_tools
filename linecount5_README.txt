For normal files like smiles file which have one molecule per line.



This C++ program reads an input file, counts the number of lines (up to 5 billion lines), and writes the line count to an output file. 
The program also prints a message indicating where the result has been written.

To run:

First you need to compile the code:

g++ -o line_counter line_counter.cpp

Then you can run the script to count the number of rows in a file.
This works very well for very large files where shell or python code is too slow

./line_counter input.txt testsmiles.smi

If you want to use this script on the cluster you can use the accompanying shell script wrapper.
It will compile the code and count the number of lines in any file (set extension in wrapper, default is .cxsmiles)
the source code needs to be in the same folder as the shell wrapper.



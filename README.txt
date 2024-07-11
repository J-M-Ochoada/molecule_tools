linecount5.cpp
For normal files like smiles file which have one molecule per line.
This C++ program reads an input file, counts the number of lines (up to 5 billion lines but can be changed in the script), and writes the line count to an output file. 
The program also prints a message indicating where the result has been written.
To run:
First you need to compile the code:
g++ -o line_count line_counte5.cpp
Then you can run the script to count the number of rows in a file.
This works very well for very large files where shell or python code is too slow
./line_count
It will prompt the user for the file they wish to count.
linecount5_cluster.sh
If you want to use this script on the LSF cluster you can use the accompanying shell script wrapper. Make sure the shell wrapper and linecount5.cpp are in the same directory.
It will compile the code and count the number of lines in all the files with specified extension (set extension in wrapper, default is .cxsmiles but can be changed in the shell script to any extension.)
To run:
./linecount5_cluster.sh
If the input files are test.cxsmiles and test2.cxsmiles the script will output test_count and test2_count files with .txt .out and .err outputs.


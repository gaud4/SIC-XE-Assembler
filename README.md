CSN-252 Tutorial-8


Name: GRANTH GAUD
Enrollment Number: 21114035
Second Year CSE

This assembler, developed using C++, can process SIC/XE programs efficiently. It functions through two passes and supports all four addressing modes (1, 2, 3, and 4). Key features of this assembler include:

1.	Expression handling
2.	Literal management
3.	Definition of symbols
4.	Control section management

Working of the assembler:

The core functionalities are executed by: loadtables(), assemblerpass1(), assemblerpass2(), and main(). The following C++ files are responsible for fulfilling these objectives:

1.	methodheaderfile.cpp - Header file hosts utility methods like getString, intToStringHex, readFirstNonWhiteSpace, readByteOperand, writeToFile, etc. It also contains structures such as struct_label, struct_extref, struct_csect, struct_opcode, struct_literal, etc.

2.	assemblerpass1.cpp – It generates a symbol table. It creates an Immediate file for pass2.cpp.

3.	assemblerpass2.cpp : 
a. It generates a listing file that includes the input assembly code, addresses, block numbers, and object codes for each instruction. 
b. It also produces an object program consisting of record types H, D, R, T, M, and E. 
c. An error file is generated to display any errors in the assembly program, if present. 
d. Additionally, a file containing the symbol table, literal table, and tables for external definition and external reference is generated.

Precautions :

1.	When the `CSECT` line appears, any comment indicated by a `.` should follow it.
2.	Terms separated by commas `,` must not have spaces between them.
3.	The Assembly code should not begin with a space.
4.	The Input File and the Executable should be in the same folder.
 


Input and Output file: 

1.	Input :-
a.	sampleinput.txt – contains question 3 of section 2.2

b.	csectinput.txt – contains example code with control section

c.	errorinput.txt – contains example code with error


2.	Outputs: - 
The generated output is stored in the folder with the .cpp files. I have included the output files for the above three inputs in the separate output folder.

For a given input, following 5 files are generated: -

a.	Intermediate file – contains intermediate text generated by assemblerpass1.cpp

b.	Listing file – contains listing file

c.	Object file – contains object file

d.	Error file – contains errors 

e.	Tables file – containing symbol table, literal table and table for external definition and external reference


Instructions to run:
1.	Go to the SIC-XE-Assembler folder in terminal (CMD for windows)

![image](https://github.com/gaud4/SIC-XE-Assembler/assets/125204835/e8ae1079-0480-4429-b1f2-7aaaa67e4a7f)

2.	Now use the command “g++ assemblerpass2.cpp -o assemblerpass2 && .\assemblerpass2” (assuming that g++ is already installed) (for Windows CMD)

![image](https://github.com/gaud4/SIC-XE-Assembler/assets/125204835/dfcd6481-b1c5-4f4d-8719-361d5cac68ba)

3.	Enter the name of input file (with .txt) in the terminal

![image](https://github.com/gaud4/SIC-XE-Assembler/assets/125204835/654ee691-6a24-4ee4-a547-98b4ad433ad2)

4.	Five new output files are generated in the same folder along with executable file assemblerpass2.exe

5.	We can also open assemblerpass2.exe directly and enter the input file from there and the output files will be generated correctly but the response from the Assembler will not be visible. (Performing PASS1 and PASS2, and error outputs from Assembler such as, file could not be read, etc.)









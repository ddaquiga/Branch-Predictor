To compile System 1 (static predicion) first compile 
the cpp file into the object code file "sys1.o":
 	g++ -c sys1.cpp

Next link to the object code creating the executable
file "sys1":
	g++ -o sys1 sys1.o

Now the executable file, "sys1.exe", can be called to run the program:
	./sys1 <filename>
where filename is the name of the trace file to be analyzed.

System 2 (2-bit predictor and branch target buffer) is compiled similarly
to System 1, but it the executable file requires additional arguments:
	./sys2 <filename> <#prediction entries> <#buffer entries> <verbose mode(optional with [-v])>
where #prediction entries and #buffer entries are powers of 2

I have included three trace files: test.trace, li1.trace, li2.trace. These can be used as inputs for either of the branch prediction systems.
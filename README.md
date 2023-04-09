# cumReg

#   PACKAGE:
     cumReg

This program finds the total length of genome in bp covered
in the bed file. Also, the program calculates the bp covered 
for each chromosomes. The program reports the result in bp 
for each chromosome.

The program needs one argument.
   1. bed file

## SYNTAX:
    ./sumCumReg bed_file.bed 

## INPUT:

The input file should be as follows:
CHR1 10 20
CHR1 30 40
CHR1 39 50
CHR1 35 39
CHR1 55 60
chr2 10 20
chr2 30 40
chr2 39 50
chr2 35 39
chr2 55 60
chr2 56 59
chr2 61 70

## OUTPUT:
With the above entries in a bed file, the program will output as:
CHR1 = 35
chr2 = 44



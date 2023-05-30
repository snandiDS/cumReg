#   PACKAGE:  cumReg

This program finds the total length of genome in bp covered
in the bed file. Also, the program calculates the bp covered 
for each chromosomes. The program reports the result in bp 
for each chromosome.

The program needs one argument.
   1. bed file

## SYNTAX:
    ./sumCumReg -f bed_file.bed -i [0/1]
    ./sumCumReg -fname BED_FILE.BED -ignore [0/1]
    ./sumCumReg -h
    ./sumCumReg --help

## OPTIONS:
    -f / -fname:    BED_FILE_NAME
    -i / -ignore:   0 OR 1 (1 to ignore overlapping, and 0 to impose overlapping)

## INPUT:

The input file should be as follows:
<pre>
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
</pre>
Column 1: Chromosome identifier  
Column 2: Start  
Column 3: End  
Each column should be seperated by space/s.  


## OUTPUT:
With the above entries in a bed file, the program will output as:
<pre>
CHR1 = 35
chr2 = 44
</pre>

<pre>
   In the version v2, we have made changes as follows:
   1. Now one can choose if the summation needs to be done considering
   the overlapping region/ignore overlapping.
   For example:
   If we have a bed file as,
   CHR1 10 20
   CHR1 15 25
   CHR1 30 40
   Then with the option '-i 1' (means ignore overlapping) the sum will 
   be 30. And with the option '-i 0' (means consider overlapping regoins)
   the sum will be 25.
</pre>



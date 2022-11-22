# pingpong

A simple program to count 5' overlaps in small RNA read datasets.

## Application

The 'ping pong signature', i.e. a disproportionate rate of 10 nucleotide long 5' overlaps of 
sense and antisense sequences, is a key characteristic of piRNAs, which is due to 
their specific secondary biogenesis mechanism. This feature can be analyzed and 
visualized as shown below with *pingpong*.

```
Number of read pairs per overlap length [nt]

                           || 
                           || 
                           || 
                           || 
                           || 
                           || 
                           ||  
                           ||  
                           ||  
                        || ||       ||
      || ||    || || || || || ||    || ||    || ||         
|| || || || || || || || || || || || || || || || || || ||   
------------------------------------------------------------
 1  2  3  4  5  6  7  8  9 10 11 12 13 14 15 16 17 18 19 20
```

## Installation

Binaries ('compiled' Perl code) are provided for Linux and macOS.<br />
Just download the respective binary for your operating system and run the program.<br />
However, it might be necessary to change permissions first, e.g. with the command:

```
chmod 777 pingpong
```

## Usage

```
./pingpong -i input.sam

 -i [file]      Input map file in SAM format
 -o [file]      Output file (optional)
```

The input for *pingpong* is a SAM file, which may be generated with *bowtie*, mapping small RNA reads to a genome or other sequences.

## Output

The output of *pingpong* is a simple two-column table with overlap length [nt] and the corresponding number of read pairs.

Additionally, *pingpong* calculates a z-score, which is printed to the STDERR.
 
## Contact
Daniel Gebert<br />
University of Cambridge, Department of Genetics<br />
email: dg572@cam.ac.uk

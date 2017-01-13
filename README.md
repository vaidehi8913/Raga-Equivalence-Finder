# Raga-Equivalence-Finder
Raga Equivalence Finder

This is a program written in Scheme (LISP) that finds equivalences between Carnatic 
(Indian classical) music ragas.  In Carnatic Music there are 72 numbered melakarta 
ragas, or scales.  For some scales, if you start on a note other than the base note,
and continue up seven notes, you get another scale in the system.  This is called a 
"graha bhedam".  You can find more information here: 
https://en.wikipedia.org/wiki/graha_bhedam .  

This program takes each of the 72 ragas and finds all of its equivalent ragas.  Because 
of the nature of the "graha bhedam" or equivalence, ragas are equivalent in groups.  The 
program finds all of the equivalence groups and prints them out.

It does this in steps.  First it takes the numbers from 1 to 72 and systematically finds 
their corresponding scale in terms of a list made up of the numbers 1 to 12, that 
represent the 12 possible notes that can be in the scale.  The program then shifts the 
scale in six different ways (one for each of the non-base notes in the scale) by calculating 
the number of steps between the notes.  It then checks to see if the resulting scales are 
legitimate and in this system.  If so, it converts back to the raga number, and looks up the 
name of the raga.  Lastly, the program eliminates duplicate cycles of equivalent ragas.  

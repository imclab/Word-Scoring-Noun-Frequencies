Word Scoring Program
July 01, 2012

Written by Justin Black (janthonyb1@hotmail.com)

This file scores a list of words, based on the frequency that each word is used in another data source

It takes a text file containing a list of words you want to score
and outputs a new text file where each word in that list is given a frequency score.
The frequency depends on which data source (corpus = body of text) you are using to
score it. This program uses 6 such data sources.

I assign no additional copyright to the combined database and the
software is explicitly being placed in the public domain. I
would appreciate credit for my work.


---------------------
INTENDED USE
---------------------
I have a list of words but I want them sorted by "populaity"
Popular words are words we use often in speech or text, unpopular words are typicaly
obscure dictionary/scrabble words.

I can then filter out words that are too obscure using
only the words with a score >= mylimit
You pick the mylimit value by opening one of the scored text files
and picking the cut-off point you prefer.

How you use it:
Assuming you are scoring nouns
Change the tfile value to point to the text file that contains
the words you want to score
All scores files will be written to the subdirectory mydir

------------------------------------------
INSTALLATION REQUIREMENTS + DIRECTIONS:
------------------------------------------
PYTHON VERSION: 2.5-2.7 (nltk requirement)
LIBRARIES: nltk, numpy
CORPORA*: brown, reuters, treebank, and gutenberg

*You must manually download the NLTK corpora, see the below instructions.

PYTHON
I wrote this in Python 2.7.2
You must use Python 2.5-2.7 for this script to work
because it uses NLTK, which has only been release for Python 2.5-2.7
at the time this program was written (July 2012)
Highest Pythn release at this point: 2.7.3, found here:
http://www.python.org/download/releases/2.7.3/

LIBRARIES:
nltk (natural language library, contains corpus data sources)
numpy (required by nltk)

I suggest you use easy install to install them
See easy_install directions here:
http://packages.python.org/distribute/easy_install.html

If you have easy install on you system, simply enter in
easy_install nltk
easy_install numpy

CORORA, CORPUS, TEXT SOURCE FOR SCORING
IMPORTANT: when you install nltk, it does not auto-install individual corpora (plural of corpus)
You have to install them by running python with the below lines:
import nltk
nltk.download()
Then a tk dialogue will pop up, click on the corpora tag
and download brown, reuters, treebank, and gutenberg

Then you are ready to run this file

CORPORA NOTE:
This program uses 4 nltk corpora, described above, and 2 wikipedia related corpora, see description below.

This distribution contains two text files in the folder 'freq_list', created by
Richard Mardsen, on April 12, 2012
His files may be found at:
http://www.monlp.com/2012/04/16/calculating-word-and-n-gram-statistics-from-a-wikipedia-corpora/
combined_wordfreq.txt -- wikipedia + gutenberg corpus word frequencies
wikipedia_wordfreq.txt -- wikipedia corpus word frequencies

CORPORA, ADDITIONAL:

This distribution also contains two text files, created by
Richard Mardse, on April 12, 2012
His files may be found at:
http://www.monlp.com/2012/04/16/calculating-word-and-n-gram-statistics-from-a-wikipedia-corpora/
combined_wordfreq.txt -- wikipedia + gutenberg corpus word frequencies
wikipedia_wordfreq.txt -- wikipedia corpus word frequencies


If you want to try additional corpora, it looks like the
COCA corpus, the Corpus of Contemporary American English is well maintained and it
contains source data from 1990 - 2012 (current year)

A free COCA 500,000 word-frequency sample list can be downloaded from the below site.
Davies, Mark. (2011) Word frequency data from the Corpus of Contemporary American English (COCA).
Downloaded from http://www.wordfrequency.info on July 01, 2012.

-------------------------------------
NOUN DATA SOURCE
-------------------------------------
Noun file is from:
http://code.google.com/p/passphrasegenerator/source/browse/trunk/Nouns.txt
Compiled by Kevin Atkinson <kevina@users.sourceforge.net> from
"Moby (tm) Part-of-Speech II" and the WordNet database
He compiled this list in 2000
His noun file contains 105,894 total nouns
including proper (capitalized) and common (uncapitalized) nouns

Additional english parts of speech could be downloaded from
http://www.ashley-bovan.co.uk/words/partsofspeech.html
Ashley Bonovan created her files from
the MOBY word lists and the UK Advanced Cryptics Dictionary
She created her files in 2009
Her noun file contains ~ 91,000 total nouns, proper and common

-------------------------------------
COPYRIGHT
-------------------------------------

The Moby database was explicitly pleased in the public domain:

    The Moby lexicon project is complete and has
    been place into the public domain. Use, sell,
    rework, excerpt and use in any way on any platform.
    
    Placing this material on internal or public servers is
    also encouraged. The compiler is not aware of any
    export restrictions so freely distribute world-wide.
    
    You can verify the public domain status by contacting
    
    Grady Ward
    3449 Martha Ct.
    Arcata, CA  95521-4884
    
    grady@netcom.com
    grady@northcoast.com


The WordNet database is under the following Copyright:

    This software and database is being provided to you, the LICENSEE, by
    Princeton University under the following license.  By obtaining, using  
    and/or copying this software and database, you agree that you have  
    read, understood, and will comply with these terms and conditions.:  
  
    Permission to use, copy, modify and distribute this software and
    database and its documentation for any purpose and without fee or
    royalty is hereby granted, provided that you agree to comply with  
    the following copyright notice and statements, including the disclaimer,  
    and that the same appear on ALL copies of the software, database and  
    documentation, including modifications that you make for internal  
    use or for distribution.  
  
    WordNet 1.6 Copyright 1997 by Princeton University.  All rights reserved.  
  
    THIS SOFTWARE AND DATABASE IS PROVIDED "AS IS" AND PRINCETON  
    UNIVERSITY MAKES NO REPRESENTATIONS OR WARRANTIES, EXPRESS OR  
    IMPLIED.  BY WAY OF EXAMPLE, BUT NOT LIMITATION, PRINCETON  
    UNIVERSITY MAKES NO REPRESENTATIONS OR WARRANTIES OF MERCHANT-  
    ABILITY OR FITNESS FOR ANY PARTICULAR PURPOSE OR THAT THE USE  
    OF THE LICENSED SOFTWARE, DATABASE OR DOCUMENTATION WILL NOT  
    INFRINGE ANY THIRD PARTY PATENTS, COPYRIGHTS, TRADEMARKS OR  
    OTHER RIGHTS.
  
    The name of Princeton University or Princeton may not be used in  
    advertising or publicity pertaining to distribution of the software  
    and/or database.  Title to copyright in this software, database and  
    any associated documentation shall at all times remain with  
    Princeton University and LICENSEE agrees to preserve same.

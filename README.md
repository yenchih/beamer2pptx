# beamer2pptx
python script to convert beamer (latex) presentations to PowerPoint presentations

## Goal
the goal of this script is to help automatize the process of converting  a Beamer Presentation (Latex) into a microsoft powerpoint.
It parses the file given in the variables texfile using regular expressions and creates a powerpoint document with the same number of slides, with the slides titles , the images in each slides (but does not keep the size or layaout yet) and creates an image for each equation that are also added to the slides

## Usage

replace the right part in line texfile='example.tex' using the name of you latex file
and then run the script using python

## Limitations

It is very basic for now, it doesn't even recreate the bullet points. But is it still usefull as a first step to speed up manual conversion.
The main problem is that it uses regular expression to parse the latex document. Parsing the latex robustly with regular expression seems difficult in case of nested brackets etc we should use a actual parser or maybe convert the document to xml using LaTexXML ?  http://dlmf.nist.gov/LaTeXML/get.html 
We could first convert to html using the commande htlatex and then parse the html but on my machine i get errors when running htlatex (Can't find/open #	file `mathkerncmssi8.tfm')
I get the same error using tex4ht and i  did not get the time to pin down the problem 
 plasTeX fails parsing when the latex uses 
 -\usepackage{mathtools}
  -french accents 



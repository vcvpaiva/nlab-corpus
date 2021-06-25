# nLab corpus

This repository contains a "cleaned" version of the contents of the nLab (as of c. December 2020), with the intention of being used as a training corpus for various machine learning projects.
The cleaning process simply strips out any non-textual elements (such as bullet points) and converts the LaTeX mathematics into unicode, wherever possible.

- `nlab_plain_normalized.txt` is the concatenation of all the pages into one large text file.
- `nlab_plain.json` has the same content as the plaintext file, but is organised into key-value pairs, with the key being the title of the page, and the value being its contents.
- `nlab_stats.json` contains some basic statistics about the corpus, generated by [spaCy](https://spacy.io).

A work-in-progress ontology of categorical concepts, extracted using Collard et al [root- and rule-based method](https://tsapps.nist.gov/publication/get_pdf.cfm?pub_id=919688), can be explored at [http://18.222.108.184:8080/](http://18.222.108.184:8080/). Note that the site may occasionally be down for updates and maintenance.

For licencing information, see the [nLab licence](https://ncatlab.org/nlab/show/HomePage#TermsOfUse).

## Corpus Statistics

There are two types of part-of-speech tags in the corpus statistics, both
generated by spaCy. The first tagset, labeled "pos" in `nlab_stats.json`,
represents course-grained part of speech and is taken from the 
[Universal POS tag set](https://universaldependencies.org/docs/u/pos/). The
second tagset, "tag", is specific to spaCy's pretrained English model. 

Details about the different tagsets, as well as other label schemes for this
model, can be found on [spaCy's website](https://spacy.io/models/en).

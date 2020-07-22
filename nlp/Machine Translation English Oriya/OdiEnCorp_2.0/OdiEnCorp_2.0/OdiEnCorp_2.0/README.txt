OdiEnCorp 2.0 Release Description
---------------------------------
http://hdl.handle.net/11234/1-3211

Shantipriya Parida
Idiap Research Institute
Martigny, Switzerland
 
Ondřej Bojar
Charles University, Faculty of Mathematics and Physics,
Institute of Formal and Applied Linguistics (UFAL)
Prague, Czech Republic
2020

Data
-----
We have collected English-Odia parallel data for the purposes of NLP
research of the Odia language.

The data for the parallel corpus was extracted from existing parallel
corpora such as OdiEnCorp 1.0 and PMIndia, and books which contain both
English and Odia text such as grammar and bilingual literature books. We
also included parallel text from multiple public websites such as Odia
Wikipedia, Odia digital library, and Odisha Government websites. 

The parallel corpus covers many domains: the Bible, other literature,
Wiki data relating to many topics, Government policies, and general
conversation. We have processed the raw data collected from the books,
websites, performed sentence alignments (a mix of manual and automatic
alignments) and released the corpus in a form suitable for various NLP
tasks.


Corpus Format
-------------
OdiEnCorp 2.0 is stored in simple tab-delimited plain text files, each
with three tab-delimited columns:

- a coarse indication of the domain
- the English sentence
- the corresponding Odia sentence

The corpus is shuffled at the level of sentence pairs.

The coarse domains are:
books       ... prose text
dict        ... dictionaries and phrasebooks
govt        ... partially formal text
odiencorp10 ... OdiEnCorp 1.0 (mix of domains)
pmindia     ... PMIndia (the original corpus)
wikipedia   ... sentences and phrases from Wikipedia


Data Statistics
---------------
The statistics of the current release are given below.

Note that the statistics differ from those reported in the paper due to
deduplication at the level of sentence pairs. The deduplication was
performed within each of the dev set, test set and training set and
taking the coarse domain indication into account. It is still possible
that the same sentence pair appears more than once within the same set
(dev/test/train) if it came from different domains, and it is also
possible that a sentence pair appears in several sets (dev/test/train).

Parallel Corpus Statistics
--------------------------

           	Dev  	Dev   	Dev   	Test 	Test  	Test  	Train	Train  	Train
           	Sents	# EN  	# OD  	Sents	# EN  	# OD  	Sents	# EN   	# OD
books      	 3523	 42011	 36723	 3895	 52808	 45383	 3129	  40461	  35300
dict       	 3342	 14580	 13838	 3437	 14807	 14110	 5900	  21591	  20246
govt       	-    	-     	-     	-    	-     	-     	  761	  15227	  13132
odiencorp10	  947	 21905	 19509	 1259	 28473	 24350	26963	 704114	 602005
pmindia    	 3836	 70282	 61099	 3836	 68695	 59876	30687	 551657	 486636
wikipedia  	 1896	  9388	  9385	 1917	 21381	 20951	 1930	   7087	   7122
Total      	13544	158166	140554	14344	186164	164670	69370	1340137	1164441

"Sents" are the counts of the sentence pairs in the given set (dev/test/train)
and domain (books/dict/...).

"# EN" and "# OD" are approximate counts of words (simply space-delimited,
without tokenization) in English and Odia

The total number of sentence pairs (lines) is 13544+14344+69370=97258. Ignoring
the set and domain and deduplicating again, this number drops to 94857.


Citation
--------

If you use this corpus, please cite the following paper:

@inproceedings{parida2020odiencorp,
  title={OdiEnCorp 2.0: Odia-English Parallel Corpus for Machine Translation},
  author={Parida, Shantipriya and Dash, Satya Ranjan and Bojar, Ond{\v{r}}ej and Motlicek, Petr and Pattnaik, Priyanka and Mallick, Debasish Kumar},
  booktitle={Proceedings of the WILDRE5--5th Workshop on Indian Language Data: Resources and Evaluation},
  pages={14--19},
  year={2020}
}


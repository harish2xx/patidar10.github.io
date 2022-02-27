#  CS657A: Information Retrieval Assignment 1


## to run assignment
------------------------

To run the script(s) assignment , run the command "$make ARGS= query_file_name"

----------
## PLUGINS
----------

Environment: Python 3.8.10  
   
---------------
## DEPENDENCIES
---------------

### Libraries: Python packages  
    Can be installed using the following command "$pip install -r requirements.txt"  

    -> Pandas 1.3.4             : For dataset manipulation, data analysis, time series & statistics.
    -> NumPy 1.21.4             : For mathematical functions & array computations.
    -> Math 3.10.2              : use mathematical function
    -> Glob 2.7.8               : read file 
    -> Re 2.2.1                 : regular experssion 
    -> Datefinder               : find out date in text
    -> Nltk 3.7                 : for stopwords , WordNetLemmatizer

-----------
## CONTENTS
-----------
   
	1. Main directory contains 23 files and 2 subdirectories named datasets and Outputs
	        1.1    english-corpora 
		1.2    processed-english-corpora
		1.3    txt files 
			 1.3.1. README.txt
			 1.3.2. Makefile
			 1.3.3  query.txt
			 1.3.4  QRels.txt
		1.4    python code (IR system)
		         1.4.1  boolean.py (boolean retrieval model)
			 1.4.2  tf-idf.py  (tf_idf retrieval model)
			 1.4.3  bm25.py    (mn25 retrieval model)
			 1.4.4  tokenization and stemming.py (processing and cleaning data)
	


---------------------------------
PERFORM TOKENIZATION AND STEMMING: 
---------------------------------
                    Reading each file and removing special  characters then tokenization and stemming after that store back the processed data in processed-english-corpora
		    code :tokenization and stemming.py

-----------
IR SYSTEM :
-----------
                  using processed data design three differnt ir system 
		  1. simple Boolean retrieval system (boolean.py)
		  2. Tf-Idf with query is matched using cosine similarity (tf-idf.py)
		  3. BM25 family with appropriate forms for the functions and tuned parameters (bm25.py)
		 
              
----------------
CONTACT DETAILS:
----------------

Harishchandra Patidar 
Roll Number: 21111029
Email: hpatidar21@iitk.ac.in

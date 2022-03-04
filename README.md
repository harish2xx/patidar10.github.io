#  CS657A: Information Retrieval Assignment 1


## to run assignment
------------------------

To run the script(s) assignment , run the command
1.   "$ make ARGS= pass english-corpora file name "  ,  it will 10-15 min to process all documents after that
2.   program will ask for query file as input (program will ask query files for 2 times 20-20 query each time )
3.   3 differnt qrels.txt files will be create after each 20 query files(for next 20 query output will be over write in same file)
     3.1  bm25_qrels.txt
     3.2  tf-idf_qrels.txt
     3.3  boolean_qrels.txt
  


----------
## PLUGINS
----------

Environment: Python 3.8.10  
   
---------------
## DEPENDENCIES :
---------------

### Libraries: Python packages  
     

    -> Pandas 1.3.4             : For dataset manipulation, data analysis, time series & statistics.
    -> NumPy 1.21.4             : For mathematical functions & array computations.
    -> Math 3.10.2              : use mathematical function
    -> Glob 2.7.8               : read file 
    -> Re 2.2.1                 : regular experssion 
    -> Datefinder               : find out date in text
    -> Nltk 3.7                 : for stopwords , WordNetLemmatizer

-----------
## CONTENTS :
-----------
   
	1. Main directory contains 23 files and 2 subdirectories named datasets and Outputs
	        1.1    english-corpora 
		1.2    txt files 
			 1.3.1. README.txt
			 1.3.2. Makefile
			 1.3.3  query.txt
			 1.3.4  QRels.txt
		1.5    python code (IR system)
		         1.4.1  boolean.py (boolean retrieval model)
			 1.4.2  tf-idf.py  (tf_idf retrieval model)
			 1.4.3  bm25.py    (mn25 retrieval model)
			 1.4.4  tokenization and stemming.py (processing and cleaning data)
	                 1.4.5  final.py  (it combine all parts in one )


------------
QUESTION 1 : 
------------
                    
                    Reading each file and performing following task
		     1. removing special  characters
		     2. finding dates in text and store all dates in same format
		     3. tokenization
		     4. removing stop words 
		     5. Stemming with lemmatization to get proper meaning words after tokenization 
		     6. store back the processed text in new folder "processed-english-corpora" with same file id name
		   
		    code :tokenization and stemming.py

-----------
QUESTION 2 :
-----------
                  using processed data design three different ir system 
		  1. simple Boolean retrieval system (boolean.py)
		  2. Tf-Idf with query is matched using cosine similarity (tf-idf.py)
		  3. BM25 family with appropriate forms for the functions and tuned parameters (bm25.py)
		 

-----------
QUESTION 3 :
----------- 
                set of 20 queries in the QRels format
		1. query.txt   contain 20 query 
		2. QRels.txt   conatin top 10 document for 20 query in QRels format



-----------
QUESTION 4 :
----------- 
		evaluated with  random 40 queries
		
		

-----------
QUESTION 5 :
-----------
              1. The submission contain a README file and a Makefile.
	      




----------------
CONTACT DETAILS:
----------------

Harishchandra Patidar 
Roll Number: 21111029
Email: hpatidar21@iitk.ac.in

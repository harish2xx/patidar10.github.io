#  CS657A: Information Retrieval Assignment 1


## to run assignment
------------------------

"$bash ir-systems.sh" runs the entire project pipeline.

To make the script(s) executable, run the command "$chmod u+x <script_name>.sh"
To run the script(s), run the command "$bash <script_name>.sh"

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
    -> ast 2.2                  : Abstract Syntax Trees
    -> math 3.10.2 
    -> glob 2.7.8               : read file 
    -> re 3.10.2                : regular experssion 


-----------
## CONTENTS
-----------
   
	1. Main directory contains 23 files and 2 subdirectories named datasets and Outputs
	        1.1  1  english-corpora 
		1.2. 1  processed-english-corpora
		1.3. 3  txt files 
			1.3.1. README.txt
			1.3.2. requirements.txt
		1.4. 4  
			

NOTE: Please do not modify directory structure, it may break the code. 


------------------------------
## NOTEBOOKS (PIPELINE STAGES)
------------------------------

Stage 1 (Data Extraction):
--------------------------

IPynb files in this stage are as follows:

    -> `myanimelist_url_scraper.ipynb`:
        Scraps the URLs of all anime(s) from `myanimelist.com` and saves them in `anime-urls-main.csv`
        Maximum number of threads for multithreading = 30  
        Maximum wait time between requests = 0.2 s  

        Run `$jupyter nbconvert --to notebook --execute --inplace myanimelist_url_scraper.ipynb` command to execute.

    -> `myanimelist_data_scraper.ipynb`:  
        Scraps the anime data (info & reviews) for all anime(s) from `myanimelist.com` and saves them in `anime-info-main.  csv` & `anime-review-main.csv`.  
        Optimal number of cores for multiprocessing = 8  
        Maximum number of threads for multithreading = 30  
        Maximum wait time between requests = 1.0 s  

        Run `$jupyter nbconvert --to notebook --execute --inplace myanimelist_data_scraper.ipynb` command to execute.  

Stage 2 (Data Cleaning & EDA):
------------------------------

## DATA CLEANING

## EXPLORATORY DATA ANALYSIS


-------------------------------------------
Stage 3 anime recommendation system :  
-------------------------------------------


----------------
CONTACT DETAILS:
----------------

Harishchandra Patidar 
Roll Number: 21111029
Email: hpatidar21@iitk.ac.in

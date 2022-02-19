# DM_PROJECT_Anime-Recommendation-System


## CS685A PROJECT README
------------------------

Project for CS685A: Data Mining by Group #35 
{
    Naman Rajput    : 2111043 
}.

"$bash proj.sh" runs the entire project pipeline.

To make the script(s) executable, run the command "$chmod u+x <script_name>.sh"
To run the script(s), run the command "$bash <script_name>.sh"

----------
## PLUGINS
----------

Software: Jupyter notebook  
    Shell scripts run jupyter notebooks in python3 env.

Environment: Python 3.8.10  
    Environment in which jupyter notebooks are executed.


---------------
## DEPENDENCIES
---------------

### Libraries: Python packages  
    Can be installed using the following command "$pip install -r requirements.txt"  

    -> Pandas 1.3.4             : For dataset manipulation, data analysis, time series & statistics.
    -> NumPy 1.21.4             : For mathematical functions & array computations.
    -> nbconvert 6.2.0          : Converts Jupyter Notebooks
    -> requests 2.22.0          : Python HTTP for Humans.
    -> beautifulsoup4 4.10.0    : Screen-scraping library.
    -> from fuzzywuzzy import process        : for matching anime name with some error
    -> scipy.sparse csr_matrix  : creating sparse matrix
    -> sklearn.neighbors  NearestNeighbors : train knn model



### Datasets: 
Use semicolon(;) as seperator while reading CSV files.  

    -> `anime-info-main.csv`:  
        Contains information(features) of anime(s) scraped from myanimelist platform.  
        SOURCE URL EXAMPLE: 'https://myanimelist.net/anime/1535/Death_Note'

    -> `anime-review-main.csv`:  
        Contains reviews of anime(s) by users scrapped from myanimelist platform.
        SOURCE URL EXAMPLE: 'https://myanimelist.net/anime/1535/Death_Note'
	
    -> rating.csv : three rating.csv file 
       


-----------
## CONTENTS
-----------
   
	1. Main directory contains 23 files and 2 subdirectories named datasets and Outputs
		1.1. 1 shell script
		1.2. 5 ipynb files
		1.3. 2 txt files 
			1.3.1. README.txt
			1.3.2. requirements.txt
		1.4. Subdirectories
			1.4.1. Datasets

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

After succesffully scraping all the data from the urls, the dataset is finally stored in the CSV files. The Anime information is stored in the anime-info-main.csv file. This files includes all the details of the Anime like Title, Genres, Type, Score, Episodes, Ranked, Favorites, Rating, etc. The User reviews are all stored in the anime-reviews.csv file.
Before analyzing the data, the files were first cleaned and then taken for exploratory data analysis.

## DATA CLEANING
----------------
1. The first step in the data cleaning done was changing the data types of the features. All the features were having data type as Object. So according to the features, the data type was finally converted to Categorical and Numerical.
2. The fields of each feature were containing some special characters and unrelated data which was finally removed.
3. After that, missing values were checked. Features which contains almost all the fields with null vlaues, the column of that feature was finally dropped. Some of the features were Premiered, Broadcast, Themes and Demographic.
4. To check if there any NaN values present in the dataset, all the unique values of important features were checked.
5. For cleaning of the user reviews, first all the reviews which were containing empty values were removed.
6. A single column of reviews were made by combining all the reviews.

## EXPLORATORY DATA ANALYSIS
----------------------------
After the data cleaning step was done, the cleaned dataset was then stored to anime-info-main-clean.csv file. Then the data analysis step was done with this file. We conducted the exploratory data analysis of all features, gathered some data insights and also how these features are correlated with each other.
The information gathered from data analysis includes:

1. Top 3 famous genres were collected like Comedy, Slice of Life and Action using word cloud technique.
2. The top ranked and scored anime was also shown by plotting the bar chart. The Anime which received the highest score was "Gintama': Enchousen"
3. Also, based on the community size , the most preferred Anime was "World Fool News (TV) Part II". 
4. It was also observed that the number pf episodes for all the Anime was not in equal proportion. It results with presence of outliers. The Anime with highest number of episodes is "Lan Mao".
5. The content of Anime for 13 or more age groups have higher as compared to all age groups, children and 17+.
6. Most of the sources of the Anime are original. Then few sources includes Mnaga and Game. A least number of sources were taken from books and radio.
7. Also, the anime content streaming is mostly of the type TV. Ohters type like OVA, ONA and Movies were less streamed.
8. Based on the Favorites given by the user, the most liked anime was "Black Lagoon: Roberta's Blood Trail".
9. The data distribution of all the numerical features were also shown. The score feature shows that most the anime were given score 1 and 6. A handfull of them received a score of 9. Other features shows that they are not evenly distributed and graph gradually decreases with increase in the episoes, members, favorites and ranked.
10. The correlation heatmap shows that features are not highly correlated. The feature score is related to the feature favorites. As the number of Scores of anime is increased then it is obvious that it is highly liked by the user and will be the favorite one.
11. It is also observed that most of the anime has already finished airing. A few anime is either still not aired or are currently airing.

## ANALYSIS OF USER REVIEWS

1. For data analysis of user reviews, we have used sentiment analysis. In this, the nltk library of Natural Language Processing is used. The sentiment analysis was performed using vader tool. It gives the polarity score of each review using SentimentIntensityAnalyzer. 
2. The sentiment analysis give positive, negative , neutral and compound score of each review.
3. After getting the scores for all the reviews, we analyzed the top 10 positive and negative review given by user to anime.
4. for going deep inside the kind of word used in the reviews, we generated a word cloud, which shows that words like beautiful, pretty, good, quick, better, first were used which shows the positive sentiments. Other words like saddest, issue, odd, awful represents some negative reviews.

After cleaning and analyzing the data, the dataset is now ready for making the recommendations. The data analysis is an essential step in any of the data mining projects as it helps in better understanding of the data which can then further used for predicion and recommender systems.

---------
    Run time of web scraper on personal system was around an hour and might need human intervention due to server defences against DDoS.


-------------------------------------------
Stage 3 anime recommendation system :  
-------------------------------------------
After Data Cleaning and analysis part here we build an anime recommendation system based on user ratings on different anime movies

## This model is based on Collaborative Filtering :
This filtration strategy is based on the combination of the user’s behavior and comparing and contrasting that with other users’ behavior in the database. The history of all users plays an important role in this algorithm. The main difference between content-based filtering and collaborative filtering is that in the latter, the interaction of all users with the items influences the recommendation algorithm while for content-based filtering only the concerned user’s data is taken into account.
There are multiple ways to implement collaborative filtering but the main concept to be grasped is that in collaborative filtering multiple users’ data influences the outcome of the recommendation. and doesn’t depend on only one user’s data for modeling.


  -> main file     :       anime recommendation file
  
  -> .sh file      :        anime_recommendation.sh     run this .sh file to run this recommendtation program
  
  -> anime info    :        anime_info.csv 
  
  -> rating csv    :        user_rating.csv
   
  -> python code   :        anime_recommendation.py     
  
  -> code notebook :        anime_recommendation.ipynb
                   


----------------
CONTACT DETAILS:
----------------

Naman Rajput
Roll Number: 21111043
Email: namanraj21@iitk.ac.in

Ayushi Mishra
Roll Number: 21111262
Email: ayushim21@iitk.ac.in 

Harishchandra Patidar 
Roll Number: 21111029
Email: hpatidar21@iitk.ac.in

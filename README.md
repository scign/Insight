# Hospitable Hospitals

This is a web application that assists hospital administrators with identifying key target areas to focus on to most efficiently improve patient satisfaction and public ratings.

Random forest regression was performed to predict a hospital's overall public rating based on parameters obtained from Yelp reviews that were processed using NLP topic modeling and sentiment analysis techniques as well as patient survey data.

## Project pipeline
1. Obtain Medicare Hospital Consumer Assessment of Healthcare Providers and Systems (HCAHPS) survey data of hospitals, pivot the table so columns are the various metrics (cleanliness, communication, etc.), and select only hospitals in MA and NY.
2. Find Yelp links for the various hospitals and use BeautifulSoup to perform web scraping of Yelp for their reviews.
3. Perform some preliminary exploratory data analysis of the ratings distributions.
4. Train LDA model using reviews to obtain topics
5. Use NLTK VADER to perform sentiment analysis sentence-by-sentence to determine overall sentiment on each topic and extract the most positive and most negative reviews
6. Perform linear regression on survey and Yelp data
7. Perform random forest regression on survey and yelp data

# RealEstate-Scraping-and-Analysis
The following scripts scrape data from a Realestate Website and stores it in a NoSQL Database (CouchDB) following which the data is analysed to find interesting insights into the stored data.


Note: Currently, only the scraper code is made available. The code for analysis shall be uploaded shortly but just to give an overview of what parameters are used to analyze the data and the type of analysis performed, look at the following:

1. Using the Dataset from ABS for population of any given suburb - Learning and Earning, identify if the number of property postings are more or less in areas where a majority of the residents are either learning or earning, if yes, whether the property is available for renting or for sale. If its for sale, is it a new property or is it pre-existing property and whether there are any factors atributing to that. Same analysis for areas with less number of residents learning or earning. 

The analysis would be a direct correlation with the number of property postings using matplotlib and scikit.

Dataset: SA2 Learning or Earning

Source: http://data.aurin.org.au/dataset/tua-phidu-sa2-learningorearning-sa2

2. Predict the price of a given property type in any given suburb (for example - Melbourne 3000) using its price and a score (created using the number of bathrooms, bedrooms, property type, and price of the property. Usually a property size would be a good indicator to be able to predict the price of a given property but since most of these postings have not specified this it becomes useless as the dataset which will be of use will decreases dramatically.

Regression is used in this to perform the analysis.

3. Identify the basic trends viewable based on Map Reduce of data in CouchDB. Various Map Reduce functions are written to attain a subset of the entire data (only the data relevant to us rather that thousands of rows) and use it for analysis using Python.

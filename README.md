# UdacityDataAnalysisProject
My submission for the first project for the advanced data analyst nano degree.

# Required Packages
<ul>
  <li>Pandas</li>
  <li>Seaborn</li>
  <li>Numpy</li>
  <li>Matplotlib</li>
  <li>Sklearn</li>
  <li>Dython</li>
</ul>

# Project Motivation
My girlfriends parents are very into wine, which is something that I have barely any experience with. Most weekends we often find ourselves in one of the various wineries around Southern Maryland. Conversation often turns towards the idea of opening a family winery. 

Since I am so inexperienced with wine I decided to test some of my business questions I came with when imagining myself as a general manager.

I wanted to answer the following three main questions:
<ol>
  <li>I want to introduce some real quality wine to my guests, what countries wine should I look out for?</li>
  <li>I want to ensure my customer's get the most out of their dollars spent. How related is the price of a bottle of wine and the score?</li>
  <li>If I wanted to deploy a predictive model to help predict the rating a bottle of wine would recieve, what accuracy could it achieve with this dataset?</li>
</ol>

# Repository File:
<ol>
  <li>wineInvestigation.ipynb : The driver script for the analysis.</li>
  <li>winemag-data-130k-v2.csv : The data supporting the analysis. Dataset obtained from Kaggle.</li>
  <li>HeatMetric.png : The heat map generated to show the correlation of a subset of the fields from the source data.</li>
  <li>AllFeaturesHeatMap.png : Heatmap of all countries and price.</li>
  <li>CoorMatrix2.png : Second correlation matrix.</li>
  <li>CountryHist.png : Histogram of all countries distribution.</li>
  <li>PointsAndPrice.png : Correlation matrix of points and price.</li>
</ol>

# Results of the analysis:
<ol>
  <li>After looking at all the visualizations the most popular countries wine was Austria. This is due to the amount of wine they had reviwed compared to the other top 5 countries and the average scoring of their wine.</li>
  <li>We can definetively say that as price increases the score a wine recieves doesn't necessarily increase. The data shows us that what winery the wine comes from is more indicative of the price.</li>
  <li>The results for this question were dissapointing. Many problems were encountered when devloping this model. Firslty, there were only two numeric fields out of 13 when first loading the data. So dummying the columns was required. This also meant that some features had to be dropped to maintain performance and to avoid too many columns being generated. This is amplified by having very few groups existing within these categorical fields. As a result, when I first ran the model with all dummy columns I got a negative r^2. An indication of an extremely ill fitting model. Dropping columns resulted in better and better r^2 scores so I had to only pass in one dummy column. Additionally the dataset had to be restricted in size to 25,000 records due to performance issues on my machine. After overcoming all these issues we recieved a very poor accuracy. If I wanted to improve upon this model I would look into different ways to encode the categorical variables in the data. As well as introducing new numeric fields to this data, such as acidity rating, sweetness, etc.</li>
</ol>

# Acknowledgments
<ol>
  <li>Data obtained from: https://www.kaggle.com/datasets/zynicide/wine-reviews</li>
  <li>Helpful article regarding categorical variables: https://blog.knoldus.com/how-to-find-correlation-value-of-categorical-variables/</li>
</ol>

# Blog Post:
Link to a blog post covering this project can be found [here](https://medium.com/@brandon.c.nutting/machine-learning-wine-c7d3b2cc20bc).
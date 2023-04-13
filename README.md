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
  <li>I want to ensure my customer's get the most out of their dollars spent. Does and increase in the price of a bottle of wine mean an increase in the score?</li>
  <li>If I wanted to deploy a predictive model to help predict the rating a bottle of wine would recieve, what accuracy could we achieve?</li>
</ol>

# Repository File:
<ol>
  <li>wineInvestigation.ipynb : The driver script for the analysis.</li>
  <li>winemag-data-130k-v2.csv : The data supporting the analysis. Dataset obtained from Kaggle.</li>
  <li>HeatMetric.png : The heat map generated to show the correlation of a subset of the fields from the source data.</li>
</ol>

# Results of the analysis:
<ol>
  <li>There are a couple way the results of the analysis for the first questions can be viewed. The highest average score goest to England with a value of: 91.55. Additionally, England recieves and average price of $51.6. The runner up for average score goes to India with a score of 90.2. More interestingly we see India recieves an average price of 13.333.</li>
  <li>We can definetively say that as price increases the score a wine recieves doesn't necessarily increase. The data shows us that what winery the wine comes from is more indicative of the price.</li>
  <li>The results for this question were dissapointing. Many problems were encountered when devloping this model. Firslty, there were only two numeric fields out of 13 when first loading the data. So dummying the columns was required. This also meant that some features had to be dropped to maintain performance and to avoid too many columns being generated. Additionally the dataset had to be restricted in size to 25,000 records due to performance issues on my machine. After all this we recieved a very poor accuracy. If I wanted to improve upon this model I would look into different ways to encode the categorical variables in the data. I belive the extremely low r^2 value is due to too many columns being added from the encoding.
  I reduced the number of encoded columns to only include one, country, and recieved an accuracy of 25%. Much better than before.
  </li>
</ol>

# Acknowledgments
<ol>
  <li>Data gotten from: https://www.kaggle.com/datasets/zynicide/wine-reviews</li>
  <li>Helpful article regarding categorical variables: https://blog.knoldus.com/how-to-find-correlation-value-of-categorical-variables/</li>
</ol>
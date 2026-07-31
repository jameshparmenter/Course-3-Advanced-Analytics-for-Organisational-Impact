# Course 3: Advanced Analytics for Organisational Impact

In the ‘Analytics for Organisational Impact’ course, we applied Python and RStudio for commercially focussed causation analysis. These included running linear regression modules, regression decision trees, multiple linear regression modules, all alongside using sentiment analysis and clustering.

<b>Grade: </b>

## The Assignment:

We were to complete a report and presentation for a decision making authority in the boardgame company ‘Turtle Games’. Turtle Games were looking to improve sales and provided their ‘Reviews’ dataset that reflected Loyalty Points, Customer Reviews and Sales.

## Building Context:

We identified the importance of refining their understanding of loyalty points:

‘The aim of the TG team is to refine their understanding of Loyalty Points and thus their customer base, to maximise sales.’

## Analytical Approach

We start by loading the dataset and the core libraries:
<ul>
<li>Pandas, Numpy, Matplotlib</li>
<li>For targeting statistics: ‘statsmodels.api’ and ‘statsmodels.stats.api’</li>
<li>For Machine Learning: sklearn</li>
<li>For Natural Language Processing: ntk</li>
<li>As phrase extraction packages: wordcloud, word_tokenize, stopwords, textblob</li>
<li>Rstudio: ‘summarytools’ and ‘gplot2’</li>
</ul>
From here, we wrangle the data:
<ul>
<li>Null Values: we identify zero</li>
<li>Transformation: dropping the bracketed content on ‘‘spending_score (1-100)’ and ‘remuneration (k£)’</li>
<li>Dropped Index: Language and ‘Sales Source’ as all are in ENG and from the Web</li>
</ul>

Here we decide to make ‘Loyalty Points’ our dependent variable with ‘spending’, ‘remuneration’ and ‘age’ core independent variables.


<b>Rstudio: Descriptive Statistics & Linear Regression</b>
In Rstudio, we installed the respective packages for exploratory analysis and to perform Multiple Linear Regression. 

RStudio Summarise:
    head(df)
    str(df)
    summary(df)
    dfSummary(df)

RStudio Exploration
    colSums(is.na(df))
    summary(df)

From here we produced histogram, boxplot, scatterplot and correlation matrix.

<img width="350" alt="TG1" src="https://github.com/user-attachments/assets/a504ec02-4610-4ab1-abfc-b54c844b5054" />
<img width="350" alt="TG2" src="https://github.com/user-attachments/assets/b2fbb11c-fea1-48dd-8f0c-dd6875396662" />
<img width="350" alt="TG3" src="https://github.com/user-attachments/assets/5030b6f7-b664-42c6-824d-8e6cb34260cd" />
<img width="350" alt="TG4" src="https://github.com/user-attachments/assets/7f226613-4ad8-46fa-b4f7-01860eb61987" />

We started our regression process with a linear regression of the dependent variable (Loyalty Points) against each of the independent variables - ‘spending’, ‘remuneration’ and ‘age’. We start by fitting ‘Age’ linearly - however with evidence of scatter plot , we inverse square age to create a new line of best fit.
We assess all the R-Squared values to find Remuneration and spending are the best values.

<b>Python: Decision Tree</b>
We built, fitted and pruned a decision tree to a max depth of three with an R-Squared of 0.914. Where it shows aspen and remuneration being significant in Loyalty Point increase.
 
<img width="400" alt="TG5" src="https://github.com/user-attachments/assets/4ada3aac-2606-4cff-a4f1-28fc20d2384d" />

<b>Python: Clustering</b>

We applied K-means to identity ‘five’ as the optimum number of clusters. The scattergraph below identifies 0 as the most valuable customer base - high spend and high remuneration. Notably, ‘one’ is our largest, with 774 observations, 39% per cent of the total group. These will be our two most valuable customer sets to target in marketing.

<img width="350" alt="TG6" src="https://github.com/user-attachments/assets/22df3802-4369-4995-9c47-e93c17d1bd95" />

<b>Python: Natural Language Processing</b>

Finally, using python, we retrieve wordclouds from the tokenised text in ‘summary’ and ‘reviews’, that also have stopwords removed. These clearly show that ‘Nan’ and words with positive sentiments such as ‘Love’ and ‘Great’ are the most frequent.

<img width="400" alt="TG7" src="https://github.com/user-attachments/assets/dbcc97a4-26b8-48b2-bff8-2c6a0f43abd0" />


<b>RStudio: MLR</b>
</br>Within R - we applied the inverse square of age to adapt our MLR model later to improve fit. We visualise both the regression models, with a line of best fit. 
There is little to no distinction between the two regression scatterplots, however both show a positive correlation between predicted and actual values.
The spread increases at higher values meaning predictions are more accurate at central values.







<b>Patterns, Trends & Insights</b>
<br>To maximise Loyalty Points and thus sales:
<ul>
<li>TG should focus on customers with high income and remuneration</li>
<li>Through linear regression analysis, we identified that a customer's age has the smallest impact</li>
<li>The largest and likely most valuable portion of the customer base are the mid income and spending.</li>
<li>Via NLP we identified positive  sentiments and consistent reference to ‘Nan’ in reviews. With this, TG should market the games towards families where older generations can still participate.</li>
<li>The next steps in the analysis will be to see if the Multiple Linear Regression can be better fit, testing more non-linear fitting to further improve the model and improve predictions. </li>
</ul>

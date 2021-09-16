# Modeling-Happiness
How does ‘happiness’ differ across the world? In particular what effects COVID-19 has had on happiness. We looked into regional variations in happiness and considered how missing data affected our approach and analysis.

### By: Blake G. Jones, Hannah G. Peha, Laura K. Pelayo Uribe

# Datasource
Our data is from the most recent World Happiness Report published in March of 2021. This annual report collates information from the Gallup World Poll survey. We performed our analysis on the last six years of data collected from 2015 to 2020. Before we began analyzing the data, we made a series of decisions in order to narrow the dataset; our intention was to be able to have more confidence in our conclusions even though they are less broadly applicable. 
Although we did not remove countries from the dataset if they were only missing a particular metric for one or multiple years, it is worth taking note of the specific metrics that are missing. For example, in the “Perceptions of Corruption" column, Bahrain, China, Jordan, Kuwait, Saudi Arabia, Turkmenistan, and the United Arab Emirates are all missing data for the entirety of the time they have partaken in the Gallup World Poll. By United States standards, these countries lack some human rights and personal freedoms. We review the differences between these countries and the rest of our dataset in the analyses sections below. 

We dubbed the majority of our data ‘Normal’ and a small group of countries ‘Extreme’. The countries given an ‘Extreme’ label were those discussed previously where the “Perception of corruption” column in the dataset is equal to zero. This is because they did not respond to the related survey questions. Based on this categorization, we formed three datasets to draw comparisons. The first is the complete dataset or ‘Global’ dataset. The second contains only those with the ‘Extreme’ countries. The third contains only the countries without an extreme designation and WHO membership, those dubbed ‘Normal’. 

# Happiness Over Time
According to our analysis, global happiness stays consistently average. 2020 did not veer from this trend showing people have been resilient through the pandemic. The boxplot below showcases our entire dataset. There are three outliers: Afghanistan in 2018 and 2019, and Zimbabwe in 2019.

<img src="https://raw.githubusercontent.com/LKPelayoUribe/Modeling-Happiness/main/Global_dataSET.PNG">

Below is the boxplot containing only the happiness distribution for the ‘Normal’ countries; it is almost identical to the global boxplot.

<img src="https://raw.githubusercontent.com/LKPelayoUribe/Modeling-Happiness/main/Normal_dataSET.PNG">

The final boxplot contains the happiness distribution for the ‘Extreme’ countries dataset. Its happiness ratings appear to be much more volatile than the ‘Normal’ country dataset. This effect is partially due to the smaller set of data. Drawing from a large pool of data has a smoothing effect on the other boxplots. The single outlier pictured in the ‘Extreme’ boxplot, Jordan in 2020, is not an outlier in the global dataset because of the larger standard deviation in the global dataset.

<img src="https://raw.githubusercontent.com/LKPelayoUribe/Modeling-Happiness/main/Extreme_dataSET.PNG">

# The Factors of Happiness
By analyzing only the ‘Normal’ countries, we determined the factors that had the greatest effect on the happiness score. With principal component analysis (PCA) we found “Social Support”, “log GDP per capita”, and “Healthy life expectancy at birth” explained the positive variance in the happiness scores while “Negative affect”, and “Perceptions of corruption” explained the negative variance in the happiness scores. 

<img src="https://raw.githubusercontent.com/LKPelayoUribe/Modeling-Happiness/main/Happiness%20Biplot.PNG">

The scatter plot below plots the first principal component against the second principal component and color codes the points based on their “Life Ladder” scores. The rainbow pattern shows the large amount of structure from the dataset contained in the first principal component. 

<img src="https://raw.githubusercontent.com/LKPelayoUribe/Modeling-Happiness/main/Happiness%20PCA.PNG">

# Happiness by Region
We looked at the happiness distributions across each region from our global dataset and from our cleaning process we found all the ‘Extreme’ countries are in the Middle East and Asia. 

<img src="https://raw.githubusercontent.com/LKPelayoUribe/Modeling-Happiness/main/Happiness%20By%20Region.PNG">

We can see both these regions have the largest ranges and gaps between their “Life Ladder” scores. 
This led us to ask, do ‘Extreme’ countries share the same “life ladder scores” as ‘Normal’ countries? And does regional location play a role on happiness?
In order to take a closer look at how different or similar the extreme countries behaved, we compared the correlations for each of the three most important happiness factors for our normal and extreme regions. 

# Analysis

First up is the economy and happiness. We made the choice to separate the extreme regions by country since if we had separated them by region, there would only be two colors to represent the middle east and Asia. But because of this, we where able to see how these extreme countries cluster for the years we did analysis from 2015-2020, and we can see this same clustering from the normal regions. 
There is a clear linear correlation between how well a region or country is doing financially and happiness. Even the extreme regions do a well job of staying within the trend of the normal regions, the higher the GDP is, the higher the life ladder score.

<img src="https://raw.githubusercontent.com/LKPelayoUribe/Modeling-Happiness/main/Economic%20Outlook%20vs.%20Happiness.PNG">

Next, we plotted health against happiness, we again see this upward trend between how happy a region is based on their healthy life expectancy. The ‘Extreme’ countries, on the other hand, do not exhibit such a strong linear correlation between health and happiness but if we where to place the extreme points onto the normal they would fit within the range.

<img src="https://raw.githubusercontent.com/LKPelayoUribe/Modeling-Happiness/main/Predicted%20Health%20vs.%20Happiness.PNG">

Finally, social support has the least linear correlation, but we can see it still is an important factor for the normal regions and for most of the extreme countries. We begin to see this upward trend when countries have at least a 0.8 social support rating. 
Turkmenistan for two years shows high social support, but their happiness score is not high enough to back up the positive trend we see from the normal regions. 

<img src="https://raw.githubusercontent.com/LKPelayoUribe/Modeling-Happiness/main/Social%20Support%20vs.%20Happiness.PNG">

# Conclusion

We found happiness does not change over time. Even through the pandemic, happiness scores stayed consistently average. We would like to note that although we believe happiness in this context means more than its average English definition, the GWP is offered in many languages to people who are part of many different cultures. While there are obviously interesting correlations between the metrics in the WHR, people are more complicated than numerical models. The metrics which improve happiness could be used to inform policy to improve the lives of people, but they are not holistic representations of any individual, community or nation. 

---
title: "test"
author: "Erika Cui, Varsha Bharath, Nithika Yechuri"
date: "2023-12-07"
output: html_document
---

**Introduction:**

  To provide some initial **context**, house pricing has drastically increased over the past few years, which has caused the housing market to be at an all-time low.  Based on what **we already know**, is that even though house prices are significantly lower from the  COVID years, the overall price ends up being much higher due to the high-interest rates buyers are now paying. It is also due to the fact that many people lost their jobs during COVID, causing there to be an average lower income in the USA. With the new prices now starting to up again, it typically takes a new buyer around 10 years minimum to pay off their mortgage. One thing we want to look into in our project is understanding how this affects people from different incomes. 

  **What we are exploring** in a broad sense is the housing industry in the USA. Overall, we want the audience to know that the process of buying a house can sometimes be hard, because of the affordability. Being able to buy a house and live comfortably is not easy in today's economy. The first question we want to explore is: What would be the minimal income someone would have to make to be able to afford a house? Another storyline we want to explore would be which top 10 places in the USA would be the most expensive for someone to buy a house. Lastly, we want to look more into the differences between the incomes of people living in the top 5 most expensive places versus the top 5 least expensive places. 

  There are various reasons as to **why this is an interesting topic** to explore and why people should care about reading our report. For starters, this is a rising issue for all home or potential buyers living in the USA. Many financial implications come with buying a house in the US. The cost of loaning money for the purchase of a home is directly impacted by house interest rates. People and families are probably curious to know how changes in interest rates can affect their monthly mortgage payments and the total costs associated with becoming a homeowner. One thing to consider is Homeownership and personal finances. Individuals and families must comprehend the complex relationships that exist between interest rates, mortgage availability, and state-specific home pricing. It has a direct bearing on choices about mortgage applications, homeownership, and general personal money management. 

  Another interesting factor is regarding real estate investment. The real estate industry is one of the major areas of interest for investors. The analysis could offer insightful information about which states might be better for real estate investment depending on the correlation between home prices, interest rates, and regional economic situations. Prices of homes are frequently used as economic indicators. Examining their relationship with per capita income can provide information about a region's economic health. Economists, investors, and legislators can use such data to assess the economy's general stability and growth prospects. 
  
  There are many regional disparities that come with housing in the USA as well. Regional differences can be better understood by looking at home prices at the state level. our study may shed information on both the challenging and rapidly growing housing markets in certain places, which would help to better comprehend the country's overall economic and demographic patterns. Another interesting factor to consider is Affordability and the socioeconomic impact house prices have in the USA today. In order to understand home affordability, the relationship between per capita income and house prices is essential. Policymakers and campaigners who wish to promote accessible housing options and alleviate socioeconomic inequities may find this information found in our report to be very helpful.  

  When looking at house prices and per capita income it is important to also think about the population dynamics. Examining the relationship between population and housing costs can reveal important information about trends in urbanization and what makes particular locations desirable for habitation. Understanding population movements is crucial for businesses, local governments, and city planners. Our report contents could be used by organizations and decision-makers for strategic planning. For instance, knowledge of the correlation between population increase and home prices may influence housing policy or infrastructure development. However, the most important reason why people would want to read our report is so that they could forecast future trends in the housing markets. The research may offer a foundation for predicting future trends in the population dynamics, real estate market, and economic growth by analyzing past data and correlations. This could yield insightful information for long-term planning. 

**Explain your Data:**

  In total, our group used three data sets. The reason **why we used these datasets** was because we thought that they had all the data we needed regarding house prices based on states in the USA, the needed data regarding the prices per capita, and finally also had the individual average income of people in different states. All of our **datasets are from** and **collected** by Kaggle. The datasets are freely available to everyone, as there are no restrictions on who can view the data.

  The first dataset, called Zillow House Price Data contains information about housing prices in various cities and states. The dataset includes details on rental prices for different types of housing situations over different time periods. One specific table, Sale_prices_state.csv, provides insights into the average house prices in each state from 2008 to 2020. It's a valuable resource for understanding how housing costs have evolved over time, allowing users to analyze trends and patterns in the real estate market across different states in the United States. 

  The second dataset is called Counties vs. PCI, and it's all about counties in America and their income stuff. It's got columns for things like the county name, the state it's in, and important money info like median household income and PCI (which stands for per capita income). You'll also find details on population size and the number of households in each county. Basically, it's a cool data set that helps you see how income is spread out across different counties in the U.S., so you can check out the money vibes in each place.

  The third dataset we used was the USA Real Estate Dataset, which is a comprehensive compilation of residential property information across the United States, inclusive of territories such as Puerto Rico. Each column within the dataset represents key details about individual houses, including their City, State, Zip Code, and specifications such as the number of bedrooms, bathrooms, and the corresponding house price. Its inclusion of data from U.S. territories adds a broader perspective, making it a valuable resource for those seeking a nuanced understanding of housing markets both within the continental U.S. and in its territorial extensions.

  A few **issues we saw in our data** were that the research was conducted during 2021. This makes the data a little bit outdated, as a lot has changed in the house marketing industry since then.

  A few **relevant variables we included** were states, average price of housing, per capita home price,  and region. However, the most important variables are states, price of housing, and per capita pricing. The main reason we think this is because these are the variables that help us answer our initially stated research questions.  

**Explaining Methods and Data:**

  In the provided Rmd file, several data processing and manipulation techniques were employed to handle multiple datasets. The code combines data from multiple sources, handles missing values, cleans and transforms data types, performs aggregations and summaries, merges datasets, and creates visualizations to explore and represent relationships between real estate prices, income, and geographical regions across various states in the United States.

  For our first dataset which we called **salePrice**, we only kept 3 variables from the columns included. These variables were called “RegionName”, “2020-2,” and “SizeRank”. We renamed “RegionName” to “State” as the values in this column were all names of the US States. We also renamed “2020-2” to price, as in this dataset, the original author collected data regarding the price of a given household for every month between 2008 and 2020. “2020-2” was the latest (therefore most accurate) price we decided to make conclusions regarding. Our second dataset was a dataset containing information about the financial status of counties in the US, which we called **countiesData**. From this dataset, we kept 2 variables which were the state name (states) and the per capita income of said state (PCI). 

	In terms of **processing the data**, we applied many of the concepts used in class and in the Problem Set assignments to format our data in a manner that was useful for us. For example, data filtering was used to filter out certain regions and areas when they were not relevant. Specifically, for the dataset that included US Territories as well as the mainland US states, we filtered out Puerto Rico, Virgin Islands, Guam, American Samoa, and the Northern Mariana Islands since it was decided the final visualizations would be confined to the 50 states in America. A **trade-off** that comes with this decision is that our conclusions are only applicable to some people, not all.  We already initially limited ourselves to just households in America, and through this decision, we further restricted the households analyzed. Another example of **data filtering** is in another visualization where we wanted to compare the average home price based on the region. For this, we assigned the names of states to a variable called “region” which assigned the states to either “West Coast,” “East Coast,” “Midwest,” or “Hawaii.” We also had to **mutate** some of the data for it to be in a form that was useful to us. An example of this is in the part where we had to mutate pciData to remove the dollar symbol in front of the price using gsub() and convert the value to numeric (asNumeric()).
	
	We selected our initial datasets by analyzing the contents of the columns and assessing whether the data was valuable for us. Later on in the code, we would pick and choose the variables we needed in the moment and create a **temporary sample dataset** with solely those aforementioned variables to use for the visualization.
	
	Some of the rows in all 3 of our datasets **contained missing values**, so we employed a few techniques to remove/bypass these values. We mainly used the filter(!is.na()) function to filter out the columns that are blank. The majority of replacing actions happened after merging the **salePrice** and **realEstateAvg** dataset by the column “States” (this dataset was called merge1).  We **replaced missing values** in the avg_price column of merge1 with corresponding non-missing values from the price column where avg_price is missing. Then we calculated an average for the remaining missing avg_price values based on non-missing price and avg_price values within the same row.
	
  In our code, we did not use any other **complex statistical methods** beyond those we used in class and in problem sets. In terms of **linear regression**, though we did not use it in the code, one manner it can be employed for better data analysis is by using it to predict house prices. Using the dataset that displays the price of a household from 2008-2020, we can use near regression to create an interactive visualization where a user can input their intended state, year of purchase, and size/type of house, and is returned an estimated sale value.

**Results**:

We created many graphs that answer various parts of our questions mentioned above. 


**Graph 1:**

![](dataset1.png)

**Graph 2:**

![](dataset2.png)

**Graph 3:**

![](average-price.png)

**Graph 4:**


![](story1.png)


**Graph 5:**

![](story3.png)

**Graph 6:**

![](region.png)

**Discuss your findings:**

**Graph 1:**

  Upon loading the initial dataset, this is the graph it produced and it compares the house prices across various states. According to our findings, Hawaii had the highest house prices within the dataset, while West Virginia had the lowest prices. This data-driven insight not only highlights the variation in real estate markets but also underscores the economic distinctions between states. The contrast between the highest and lowest prices serves as an informative starting point for further exploration into the factors influencing regional housing markets and the potential socio-economic implications associated with these pricing trends.

**Graph 2:**

	This graphical representation provides a visual overview of the average per capita income across different states. The x-axis represents the per capita income, while the y-axis represents the states being analyzed. The graph allows for a quick and comparative assessment of income levels, enabling viewers to discern variations in economic prosperity among states. For instance, states positioned higher on the y-axis indicate a higher per capita income, while those lower on the axis signify comparatively lower average incomes. This visual depiction serves as an accessible tool for understanding the income distribution landscape across various states, providing valuable insights for economic analysis and regional comparisons.
	
**Graph 3:**

  This graphical representation offers a visual depiction of the average house prices across the states. The y-axis corresponds to the states being analyzed, while the x-axis represents the average house prices. By presenting this information graphically, the viewer can easily observe and compare the relative cost of housing in different states. States positioned higher on the y-axis reflect higher average house prices, whereas those lower on the axis indicate comparatively lower average prices. This graph serves as a concise and accessible tool for gaining insights into the variation in real estate markets among the selected states, aiding in the quick identification of states with higher or lower average house prices.

**Graph 4:**

	Massachusetts has the highest average house price, coupled with a per capita income of around the high 40k range. In contrast, West Virginia exhibits the lowest average per capita income alongside the lowest average house prices. New York, on the other hand, stands out for having the highest average per capita income, exceeding 300k, with corresponding average house prices slightly above 300k. This comparative examination underscores the intricate relationship between regional income levels and real estate market dynamics, offering insights into the economic disparities and housing affordability across these states.
	
**Graph 5:** 

  This graph provides a focused exploration of the top and bottom 5 states in the United States concerning average housing prices. The x-axis represents the average price of housing, allowing for a straightforward comparison between states, while the y-axis delineates the specific states under consideration. By utilizing this visual representation, viewers can quickly discern the relative positioning of states in terms of housing costs. The states positioned higher on the y-axis are indicative of having higher average housing prices, while those lower on the axis reflect states with comparatively lower average prices. This graph serves as a concise yet informative tool for highlighting the variations in the real estate market among the selected top and bottom states.

**Graph 6:** 

  This graph illustrates the average price of homes across various coasts in the USA, with the x-axis representing the price and the y-axis denoting the different coasts. By employing this visual representation, the graph provides a clear and concise overview of the relative pricing trends among the different coastal regions. States or regions positioned higher on the y-axis indicate higher average home prices, while those lower on the axis suggest more affordable housing. This graphical representation serves as an effective means of quickly comparing and contrasting the real estate market dynamics along different coasts, aiding in the identification of potential trends and disparities in home prices across these regions.
Some limitations to our dataset could be that it is only within the US, so people who live in other countries cannot use this data. Another limitation is that it does not talk about the cities in America. I think to further our research in the future, we could add new data that checks and answers these questions in other countries as well as the USA. 

**Summary: **

  Interest rates have experienced a significant rise in recent years, leading to an unprecedented downturn in the housing market. Despite house prices being notably lower than during the COVID-19 years, the overall cost has risen substantially due to the elevated interest rates imposed on buyers. Typically, it takes a minimum of 10 years for a new buyer to fully pay off their mortgage. Our project aims to delve into the impact of these dynamics on individuals with varying family incomes. We find it intriguing to explore how the process of purchasing a home in today's market can be challenging, primarily due to affordability issues. The income of each individual plays a pivotal role in shaping the significance of embarking on the journey to buy a house. Achieving the ability to purchase a home and live comfortably is a formidable task. An essential question we seek to address is: What is the minimum income required for someone to afford a house? Another aspect we wish to investigate is identifying the top 10 places in the USA where buying a house is the most expensive. Additionally, we aim to compare the incomes of residents in the top 10 most expensive places with those in the top 10 least expensive places based on states. Upon completion of our data analysis, we plan to present the information in a user-friendly format, featuring a drop-down menu that allows users to select any state in the USA. On this page, users will find a graph displaying the average interest rates for housing on the right side. To enhance clarity, we will create a separate column dedicated solely to the state, especially considering that one database includes both addresses and states.
  
  The take-away we got from the final data is that for the target audience (people with minimal knowledge of the housing market which can vary from young adults to new house buyers), people with lower income that are looking to buy a house should buy their first house in the Midwest coast, because while the Midwest has a lower average per capita income, their average house prices are the lowest compared to Hawaii, West Coast, East Coast, and the Mountains.

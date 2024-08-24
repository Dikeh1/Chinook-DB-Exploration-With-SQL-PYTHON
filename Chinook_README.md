## THE CHINOOK DATABASE


#### The Chinook database is a sample database that simulates a digital media store and includes various tables that represent a store's structure and data. 

#### ![image2](ch.png)

#### Key Features of the Chinook Database:
#### Tables:

Artists: Contains information about the artists in the store.
 
 Albums: Stores details about albums, including the artist and album title.
 
 Tracks: Lists individual tracks (songs), along with details such as genre, composer, and the album they belong to.
 
 Genres: Categorizes tracks into different music genres.
 
 MediaTypes: Information about the types of media (e.g., MPEG, AAC audio files).
 
 Playlists: Contains playlists created by customers, with links to tracks.
 
 Customers: Stores customer information such as name, address, and contact details.
 
 Invoices: Contains sales records, including the date of purchase, total amount, and customer information.
 
 InvoiceItems: Breaks down each invoice into individual items, showing which tracks were purchased.
 
 Employees: Lists the employees working in the store, including their title and reporting structure.
 
 Stores: Represents the different physical or digital stores in the system.
 
## Methodologies
 
### Data Exploration:
 
 The database was first explored to see the tables embedded in it in the notebook, afterwhich each table was viewed on a different sql environment.
 
 The Join SQL was used to join most of the tables in the database that would be needed in exploring the project prompts, and this was then assigned to a dataframe
 
### Data Cleaning:

 The data types for each columns was examined, and the dates column (HireDate, BirthDate and InvoiceDate) on each tables were adjusted to the Datetime datatype.
 The column names from the dataframe were renamed to avoid duplication and confusions
 Duplicate data was checked and removed from the table
 
### Data Anaysis:

#### Top-sell Artist:

 The artist name, and revenue generated by year was collected from joinng appropriate tables.
 
#### Customer Purchase Pattern:
 To segment customers based on purchase behavior and identify key characteristics of high-value customers using the Chinook database, we can analyze customer purchase patterns by calculating total spending, number of purchases, and average purchase value. Then, we can identify key characteristics such as country, preferred genre, etc This was achieved by creating multiple temporary table: customer purchase pattern customer genre purchases and customer genre preferences.
 
#### Genre Popularity:
we explored the genre table on the chinook db. We join the invoice, tracks and the genre table for analysis
 
#### Sales Overtime:
Invoice table was queries to analysed sales overtime monthly and yearly.

### Customer Lifetime Value (CLV):
Calculate the lifetime value of customers based on their purchase history.
Customer table was analysed and the following information was filtered to get the following information:
FirstName, LastName, Country, State, TotalRevenue, AvgPurchaseValue and PurchaseFrequency





## Key Finding:

### 1. Top-Selling Artists:

#### ![image](download1.png)

#### Key Insights:

    --Lost and U2: These artists exhibit more dramatic revenue changes. Lost experiences a decline in revenue over time, while U2 shows a notable increase, particularly in the later years. This could be attributed to factors such as new album releases, successful tours, or changes in market trends.

    --Revenue Fluctuations: There's significant variation in revenue for all artists over time, indicating fluctuations in popularity, album releases, or other factors influencing sales.

    --Deep Purple and Iron Maiden: These artists demonstrate relatively stable revenue levels throughout the period, with minor fluctuations. This might suggest a consistent fan base and steady sales.
    

#### ![image](download2.png)
    
    --Dominant Artists: Iron Maiden and U2 significantly outpace the other artists in terms of revenue generation.
    
    --Revenue Disparity: There's a substantial gap in revenue between the top two artists and the rest of the list.
    
    --Revenue Tiers: The artists can be categorized into tiers based on revenue:
        --Top Tier: Iron Maiden, U2
        --Mid-Tier: Led Zeppelin, Metallica, Deep Purple
        --Lower Tier: Pearl Jam, Lenny Kravitz, Van Halen, The Office
        
### 2. Customer Purchase Patterns:

#### ![image](download3.png)

#### Key insights:

    --Significant Spending Disparity: The chart clearly shows a significant difference in spending between the top-ranking customers and the others. Helena Holý, the top spender, has a considerable lead over the rest.
    --Spending Clusters: There might be potential for customer segmentation based on spending levels. Customers can be grouped into high, medium, and low spenders. Customer Loyalty: The top spenders might represent loyal customers with a strong affinity for the brand or products. 
    --Potential for Targeted Marketing: Customers with higher spending might be ideal targets for loyalty programs, exclusive offers, or personalized marketing campaigns.

#### ![image](download4.png)

    --Rock Dominance: Customers who prefer Rock music tend to have the highest average purchase value.

    --Genre-Based Spending Patterns: The chart clearly shows distinct spending patterns across different genres. Metal follows Rock in terms of average purchase value, while Latin and Alternative & Punk genres exhibit lower average spending.

    --Potential for Segmentation: The variation in average purchase value across genres suggests potential for customer segmentation based on music preferences and spending behavior.
    
### 3. Genre popularity

#### ![image](download6.png)

#### Overall Trend:

Rock Dominance: Rock consistently holds a strong position as the most popular genre throughout the years 2009 to 2013.

Genre Fluctuation: There's a noticeable fluctuation in the popularity of other genres over time. Some genres experience periods of growth, while others decline.

Emergence of Alternative & Punk: There's a visible increase in the popularity of Alternative & Punk genres, particularly in the later years.

Declining Traditional Genres: Genres like Blues, Jazz, and Classical seem to be declining in popularity. Rising Electronic Music: Electronic genres (Electronic/Dance, Hip Hop/Rap) show increasing popularity, especially in later years.

The chart demonstrates a wide range of music preferences among listeners.

Potential Implications:

Market Targeting: Record labels and music platforms could focus on promoting Alternative & Punk and Electronic genres. Content Creation: Music producers and artists might consider catering to the growing demand for these genres


### 4. Sales Trend

#### ![image](download5.png)

Yearly Sales Trends:

#### 2009:

    --Total sales for the year: 449.46
    --Sales were relatively consistent throughout the year.

#### 2010:

    --Total sales for the year: 481.45
    --Notable increase in sales compared to 2009.
    --Indicates an upward trend, potentially due to increased customer base or successful promotions.
    
#### 2011:

    --Total sales for the year: 469.58
    --Slight decrease compared to 2010.
    --Indicates some fluctuations but overall stable sales performance.

#### 2012:
    --Total sales for the year: 477.53
    --Increase in sales compared to 2011.
    --Indicates recovery and growth in sales, potentially due to effective marketing or seasonal promotions.
    
#### 2013:

    --Total sales for the year: 450.58
    --Decrease in sales compared to 2012.
    --Indicates a potential decline, suggesting the need for analyzing factors affecting sales drop. probably due to inconsistency in effective marketing and seasonal promotion
    
#### Summary:

The yearly sales trend shows fluctuations with an overall peak in 2010.
2011 and 2013 show slight decreases, while 2012 shows recovery in sales.


### 5. Customer Lifetime Value (CLV):

#### ![image](download8.png)


Key Observations:
Right-skewed distribution: The majority of customers have a lower CLV, with a smaller number of customers contributing significantly higher values. This is indicated by the elongated tail on the right side of the histogram.

Concentration around lower CLV: The tallest bar is on the left side of the graph, suggesting a large portion of customers have a CLV within the lower range.

Outliers: There are some customers with exceptionally high CLV values, represented by the bars on the far right of the histogram. These customers contribute significantly to overall revenue.

Implications:
Focus on customer retention: Since a large portion of customers have lower CLV, efforts to improve customer retention and increase purchase frequency can be beneficial.

Identify high-value customers: The customers with exceptionally high CLV deserve special attention and tailored marketing strategies to maximize their value.

Customer segmentation: Dividing customers into segments based on CLV can help in targeted marketing and resource allocation.

#### ![image](download9.png)

#### Czech Republic and USA:
These countries have a higher median CLV compared to other countries. Additionally, they have a wider range of CLV values, indicating greater variation in customer spending habits.

#### Lower CLV Countries: 
Countries like Brazil, Portugal, and Canada have lower median CLV values and a narrower range, suggesting a more homogenous customer base with lower spending.

#### Outliers:
While present in multiple countries, some countries like the USA and Czech Republic have more pronounced outliers, indicating the presence of high-value customers

#### Recommendation:

Market Segmentation: Focus on understanding the factors contributing to higher CLV in countries like Czech Republic and the USA to replicate success in other markets.

Customer Retention: Implement targeted retention strategies for countries with lower CLV to increase customer lifetime value.

Outlier Analysis: Identify and analyze the characteristics of high-value customers (outliers) to understand their behavior and preferences.


## Key Recommendations

#### Customer Segmentation:

    --Identify high-value customers based on spending patterns and purchase frequency.
    --Analyze customer demographics to understand target market segments.
    --Implement personalized marketing strategies based on customer preferences and behavior.

#### Product Focus:

    --Prioritize products and genres with high sales and customer satisfaction.
    --Analyze product performance over time to identify trends and opportunities for new product development.
    --Consider cross-selling and upselling opportunities based on customer purchasing behavior.

#### Sales and Marketing Optimization:

    --Analyze sales trends by region, product category, or time period to identify peak sales times and optimize marketing efforts accordingly.
    --Utilize customer segmentation to target marketing campaigns effectively.
    --Explore pricing strategies based on product popularity and customer value.

#### Data-Driven Decision Making:

    --Continuously monitor key performance indicators (KPIs) to track business performance.
    --Use data analytics to identify trends, patterns, and opportunities.
    --Experiment with different marketing strategies and measure their impact on sales.

### Additional Considerations

Customer Lifetime Value (CLTV): Calculate CLTV to assess the long-term value of customers and focus on retention strategies.

Inventory Management: Optimize inventory levels based on product popularity and sales trends to avoid stockouts or overstocking.

Customer Feedback: Gather customer feedback to improve product offerings and customer satisfaction


```python

```


```python

```
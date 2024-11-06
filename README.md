{
 "cells": [
  {
   "cell_type": "markdown",
   "id": "aa514948",
   "metadata": {},
   "source": [
    "## THE CHINOOK DATABASE\n",
    "\n",
    "\n",
    "#### The Chinook database is a sample database that simulates a digital media store and includes various tables that represent a store's structure and data. \n",
    "\n",
    "#### ![ch](https://github.com/user-attachments/assets/b4221ae0-0f3f-4008-ad10-7414a47df758)\n",
    "\n",
    "#### Key Features of the Chinook Database:\n",
    "#### Tables:\n",
    "\n",
    "Artists: Contains information about the artists in the store.\n",
    " \n",
    " Albums: Stores details about albums, including the artist and album title.\n",
    " \n",
    " Tracks: Lists individual tracks (songs), along with details such as genre, composer, and the album they belong to.\n",
    " \n",
    " Genres: Categorizes tracks into different music genres.\n",
    " \n",
    " MediaTypes: Information about the types of media (e.g., MPEG, AAC audio files).\n",
    " \n",
    " Playlists: Contains playlists created by customers, with links to tracks.\n",
    " \n",
    " Customers: Stores customer information such as name, address, and contact details.\n",
    " \n",
    " Invoices: Contains sales records, including the date of purchase, total amount, and customer information.\n",
    " \n",
    " InvoiceItems: Breaks down each invoice into individual items, showing which tracks were purchased.\n",
    " \n",
    " Employees: Lists the employees working in the store, including their title and reporting structure.\n",
    " \n",
    " Stores: Represents the different physical or digital stores in the system.\n",
    " \n",
    "## Methodologies\n",
    " \n",
    "### Data Exploration:\n",
    " \n",
    " The database was first explored to see the tables embedded in it in the notebook, afterwhich each table was viewed on a different sql environment.\n",
    " \n",
    " The Join SQL was used to join most of the tables in the database that would be needed in exploring the project prompts, and this was then assigned to a dataframe\n",
    " \n",
    "### Data Cleaning:\n",
    "\n",
    " The data types for each columns was examined, and the dates column (HireDate, BirthDate and InvoiceDate) on each tables were adjusted to the Datetime datatype.\n",
    " The column names from the dataframe were renamed to avoid duplication and confusions\n",
    " Duplicate data was checked and removed from the table\n",
    " \n",
    "### Data Anaysis:\n",
    "\n",
    "#### Top-sell Artist:\n",
    "\n",
    " The artist name, and revenue generated by year was collected from joinng appropriate tables.\n",
    " \n",
    "#### Customer Purchase Pattern:\n",
    " To segment customers based on purchase behavior and identify key characteristics of high-value customers using the Chinook database, we can analyze customer purchase patterns by calculating total spending, number of purchases, and average purchase value. Then, we can identify key characteristics such as country, preferred genre, etc This was achieved by creating multiple temporary table: customer purchase pattern customer genre purchases and customer genre preferences.\n",
    " \n",
    "#### Genre Popularity:\n",
    "we explored the genre table on the chinook db. We join the invoice, tracks and the genre table for analysis\n",
    " \n",
    "#### Sales Overtime:\n",
    "Invoice table was queries to analysed sales overtime monthly and yearly.\n",
    "\n",
    "### Customer Lifetime Value (CLV):\n",
    "Calculate the lifetime value of customers based on their purchase history.\n",
    "Customer table was analysed and the following information was filtered to get the following information:\n",
    "FirstName, LastName, Country, State, TotalRevenue, AvgPurchaseValue and PurchaseFrequency\n",
    "\n",
    "\n",
    "\n",
    "\n",
    "\n",
    "## Key Finding:\n",
    "\n",
    "### 1. Top-Selling Artists:\n",
    "\n",
    "#### ![download1](https://github.com/user-attachments/assets/8c41e59e-dc84-45de-ad91-b58c6a897a73)\n",
    "\n",
    "#### Key Insights:\n",
    "\n",
    "    --Lost and U2: These artists exhibit more dramatic revenue changes. Lost experiences a decline in revenue over time, while U2 shows a notable increase, particularly in the later years. This could be attributed to factors such as new album releases, successful tours, or changes in market trends.\n",
    "\n",
    "    --Revenue Fluctuations: There's significant variation in revenue for all artists over time, indicating fluctuations in popularity, album releases, or other factors influencing sales.\n",
    "\n",
    "    --Deep Purple and Iron Maiden: These artists demonstrate relatively stable revenue levels throughout the period, with minor fluctuations. This might suggest a consistent fan base and steady sales.\n",
    "    \n",
    "\n",
    "#### ![download2](https://github.com/user-attachments/assets/ce5a666b-0304-48e5-8ed3-2d4a94f097ba)\n",
    "    \n",
    "    --Dominant Artists: Iron Maiden and U2 significantly outpace the other artists in terms of revenue generation.\n",
    "    \n",
    "    --Revenue Disparity: There's a substantial gap in revenue between the top two artists and the rest of the list.\n",
    "    \n",
    "    --Revenue Tiers: The artists can be categorized into tiers based on revenue:\n",
    "        --Top Tier: Iron Maiden, U2\n",
    "        --Mid-Tier: Led Zeppelin, Metallica, Deep Purple\n",
    "        --Lower Tier: Pearl Jam, Lenny Kravitz, Van Halen, The Office\n",
    "        \n",
    "### 2. Customer Purchase Patterns:\n",
    "\n",
    "#### ![download3](https://github.com/user-attachments/assets/170a922d-1009-4e57-af59-354044878ba6)\n",
    "\n",
    "#### Key insights:\n",
    "\n",
    "    --Significant Spending Disparity: The chart clearly shows a significant difference in spending between the top-ranking customers and the others. Helena Holý, the top spender, has a considerable lead over the rest.\n",
    "    --Spending Clusters: There might be potential for customer segmentation based on spending levels. Customers can be grouped into high, medium, and low spenders. Customer Loyalty: The top spenders might represent loyal customers with a strong affinity for the brand or products. \n",
    "    --Potential for Targeted Marketing: Customers with higher spending might be ideal targets for loyalty programs, exclusive offers, or personalized marketing campaigns.\n",
    "\n",
    "#### ![download4](https://github.com/user-attachments/assets/e07d5dfb-eb79-41c7-9138-ba2d0b1a2709)\n",
    "\n",
    "    --Rock Dominance: Customers who prefer Rock music tend to have the highest average purchase value.\n",
    "\n",
    "    --Genre-Based Spending Patterns: The chart clearly shows distinct spending patterns across different genres. Metal follows Rock in terms of average purchase value, while Latin and Alternative & Punk genres exhibit lower average spending.\n",
    "\n",
    "    --Potential for Segmentation: The variation in average purchase value across genres suggests potential for customer segmentation based on music preferences and spending behavior.\n",
    "    \n",
    "### 3. Genre popularity\n",
    "\n",
    "#### !![download6](https://github.com/user-attachments/assets/5a808104-83ea-4f83-b2dd-c66f379f794b)\n",
    "\n",
    "#### Overall Trend:\n",
    "\n",
    "Rock Dominance: Rock consistently holds a strong position as the most popular genre throughout the years 2009 to 2013.\n",
    "\n",
    "Genre Fluctuation: There's a noticeable fluctuation in the popularity of other genres over time. Some genres experience periods of growth, while others decline.\n",
    "\n",
    "Emergence of Alternative & Punk: There's a visible increase in the popularity of Alternative & Punk genres, particularly in the later years.\n",
    "\n",
    "Declining Traditional Genres: Genres like Blues, Jazz, and Classical seem to be declining in popularity. Rising Electronic Music: Electronic genres (Electronic/Dance, Hip Hop/Rap) show increasing popularity, especially in later years.\n",
    "\n",
    "The chart demonstrates a wide range of music preferences among listeners.\n",
    "\n",
    "Potential Implications:\n",
    "\n",
    "Market Targeting: Record labels and music platforms could focus on promoting Alternative & Punk and Electronic genres. Content Creation: Music producers and artists might consider catering to the growing demand for these genres\n",
    "\n",
    "\n",
    "### 4. Sales Trend\n",
    "\n",
    "#### ![download5](https://github.com/user-attachments/assets/b426deba-8966-4918-8338-71fb8c8727f8)\n",
    "\n",
    "Yearly Sales Trends:\n",
    "\n",
    "#### 2009:\n",
    "\n",
    "    --Total sales for the year: 449.46\n",
    "    --Sales were relatively consistent throughout the year.\n",
    "\n",
    "#### 2010:\n",
    "\n",
    "    --Total sales for the year: 481.45\n",
    "    --Notable increase in sales compared to 2009.\n",
    "    --Indicates an upward trend, potentially due to increased customer base or successful promotions.\n",
    "    \n",
    "#### 2011:\n",
    "\n",
    "    --Total sales for the year: 469.58\n",
    "    --Slight decrease compared to 2010.\n",
    "    --Indicates some fluctuations but overall stable sales performance.\n",
    "\n",
    "#### 2012:\n",
    "    --Total sales for the year: 477.53\n",
    "    --Increase in sales compared to 2011.\n",
    "    --Indicates recovery and growth in sales, potentially due to effective marketing or seasonal promotions.\n",
    "    \n",
    "#### 2013:\n",
    "\n",
    "    --Total sales for the year: 450.58\n",
    "    --Decrease in sales compared to 2012.\n",
    "    --Indicates a potential decline, suggesting the need for analyzing factors affecting sales drop. probably due to inconsistency in effective marketing and seasonal promotion\n",
    "    \n",
    "#### Summary:\n",
    "\n",
    "The yearly sales trend shows fluctuations with an overall peak in 2010.\n",
    "2011 and 2013 show slight decreases, while 2012 shows recovery in sales.\n",
    "\n",
    "\n",
    "### 5. Customer Lifetime Value (CLV):\n",
    "\n",
    "#### ![download8](https://github.com/user-attachments/assets/421af18d-3e0e-485a-9c72-e8715e425398)\n",
    "\n",
    "\n",
    "Key Observations:\n",
    "Right-skewed distribution: The majority of customers have a lower CLV, with a smaller number of customers contributing significantly higher values. This is indicated by the elongated tail on the right side of the histogram.\n",
    "\n",
    "Concentration around lower CLV: The tallest bar is on the left side of the graph, suggesting a large portion of customers have a CLV within the lower range.\n",
    "\n",
    "Outliers: There are some customers with exceptionally high CLV values, represented by the bars on the far right of the histogram. These customers contribute significantly to overall revenue.\n",
    "\n",
    "Implications:\n",
    "Focus on customer retention: Since a large portion of customers have lower CLV, efforts to improve customer retention and increase purchase frequency can be beneficial.\n",
    "\n",
    "Identify high-value customers: The customers with exceptionally high CLV deserve special attention and tailored marketing strategies to maximize their value.\n",
    "\n",
    "Customer segmentation: Dividing customers into segments based on CLV can help in targeted marketing and resource allocation.\n",
    "\n",
    "#### ![download9](https://github.com/user-attachments/assets/c7432364-ea66-40f3-9af4-565016524af8)\n",
    "\n",
    "#### Czech Republic and USA:\n",
    "These countries have a higher median CLV compared to other countries. Additionally, they have a wider range of CLV values, indicating greater variation in customer spending habits.\n",
    "\n",
    "#### Lower CLV Countries: \n",
    "Countries like Brazil, Portugal, and Canada have lower median CLV values and a narrower range, suggesting a more homogenous customer base with lower spending.\n",
    "\n",
    "#### Outliers:\n",
    "While present in multiple countries, some countries like the USA and Czech Republic have more pronounced outliers, indicating the presence of high-value customers\n",
    "\n",
    "#### Recommendation:\n",
    "\n",
    "Market Segmentation: Focus on understanding the factors contributing to higher CLV in countries like Czech Republic and the USA to replicate success in other markets.\n",
    "\n",
    "Customer Retention: Implement targeted retention strategies for countries with lower CLV to increase customer lifetime value.\n",
    "\n",
    "Outlier Analysis: Identify and analyze the characteristics of high-value customers (outliers) to understand their behavior and preferences.\n",
    "\n",
    "\n",
    "## Key Recommendations\n",
    "\n",
    "#### Customer Segmentation:\n",
    "\n",
    "    --Identify high-value customers based on spending patterns and purchase frequency.\n",
    "    --Analyze customer demographics to understand target market segments.\n",
    "    --Implement personalized marketing strategies based on customer preferences and behavior.\n",
    "\n",
    "#### Product Focus:\n",
    "\n",
    "    --Prioritize products and genres with high sales and customer satisfaction.\n",
    "    --Analyze product performance over time to identify trends and opportunities for new product development.\n",
    "    --Consider cross-selling and upselling opportunities based on customer purchasing behavior.\n",
    "\n",
    "#### Sales and Marketing Optimization:\n",
    "\n",
    "    --Analyze sales trends by region, product category, or time period to identify peak sales times and optimize marketing efforts accordingly.\n",
    "    --Utilize customer segmentation to target marketing campaigns effectively.\n",
    "    --Explore pricing strategies based on product popularity and customer value.\n",
    "\n",
    "#### Data-Driven Decision Making:\n",
    "\n",
    "    --Continuously monitor key performance indicators (KPIs) to track business performance.\n",
    "    --Use data analytics to identify trends, patterns, and opportunities.\n",
    "    --Experiment with different marketing strategies and measure their impact on sales.\n",
    "\n",
    "### Additional Considerations\n",
    "\n",
    "Customer Lifetime Value (CLTV): Calculate CLTV to assess the long-term value of customers and focus on retention strategies.\n",
    "\n",
    "Inventory Management: Optimize inventory levels based on product popularity and sales trends to avoid stockouts or overstocking.\n",
    "\n",
    "Customer Feedback: Gather customer feedback to improve product offerings and customer satisfaction"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "aa0fa00c",
   "metadata": {},
   "outputs": [],
   "source": []
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "e44adce2",
   "metadata": {},
   "outputs": [],
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.11.5"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
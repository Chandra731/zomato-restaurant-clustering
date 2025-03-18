## **Overview**

The primary objective of this project was to analyze and cluster restaurants listed on Zomato based on various features such as cost, ratings, reviews, and cuisines. By leveraging data visualization, sentiment analysis, and clustering algorithms, we aimed to uncover insights that can help improve customer satisfaction and optimize business strategies.

## **Data Understanding and Cleaning**

We began by loading two datasets: restaurant metadata and reviews. The datasets were merged on the restaurant name to create a comprehensive dataset. Initial examination revealed missing values and duplicate entries, which were addressed through a series of preprocessing steps:
- **Feature Engineering**: A binary feature 'Has_Collections' was created to indicate the presence of collections, and the original 'Collections' column was dropped.
- **Missing Values**: Missing values in columns such as 'Timings' and 'Time' were filled using the mode of related columns, while others like 'Reviewer', 'Review', and 'Metadata' were filled with placeholder values.
- **Data Type Conversions**: The 'Cost' column was converted to numeric after removing currency symbols, and datetime conversion was applied to the 'Time' column.
- **Standardization**: Column names were standardized to lowercase with underscores.

## **Data Visualization**

A variety of visualizations were created to explore the relationships between different variables:
1. **Heatmap**: Showed the relationship between cost, cuisines, and average ratings.
2. **Jointplot**: Visualized the distribution of cost vs. ratings using Kernel Density Estimation (KDE).
3. **Boxenplot**: Compared the impact of collections on ratings.
4. **Countplot**: Highlighted the most common cuisine types.
5. **Violin Plot**: Displayed the distribution and density of restaurant ratings.
6. **Donut Chart**: Represented the proportion of different restaurant cost categories.
7. **Swarmplot**: Showed the relationship between restaurant cost and customer ratings.
8. **Word Cloud**: Highlighted frequently mentioned words in reviews.
9. **Line Plot**: Illustrated the trend of customer reviews over time.
10. **Boxplot**: Visualized the spread and distribution of ratings across various cuisines.
11. **Histogram**: Showed the distribution of review lengths.
12. **Barplot**: Highlighted the most active reviewers.
13. **Correlation Heatmap**: Represented the relationships between numerical features.
14. **Pair Plot**: Visualized relationships between multiple numerical features.
15. **Sentiment Distribution Donut Chart**: Illustrated the proportions of different sentiments in reviews.

## **Textual Data Preprocessing**

Textual data preprocessing involved several steps to prepare the reviews for analysis:
- **Expanding Contractions**: Ensured consistency in text.
- **Lower Casing**: Converted all text to lowercase.
- **Removing Punctuations, URLs, and Digits**: Cleaned the text.
- **Removing Stopwords and White Spaces**: Reduced noise in the text.
- **Rephrasing Text**: Applied lemmatization to convert words to their base form.
- **Tokenization**: Split the text into individual words.
- **Text Vectorization**: Used Word2Vec to convert text into numerical features, capturing the context and meaning of words.

## **Sentiment Analysis**

Sentiment analysis was performed using VADER to classify reviews into positive, negative, and neutral sentiments. The distribution of sentiments was visualized to understand overall customer sentiment towards the restaurants.

## **Clustering**

Three clustering algorithms were applied:
1. **KMeans**: Identified clusters based on cost, rating, sentiment score, and reviews. The silhouette score was 0.26, indicating moderate clustering.
2. **DBSCAN**: Detected arbitrary-shaped clusters and outliers based on density. The silhouette score was -0.20, indicating poor clustering.
3. **Agglomerative Clustering**: A hierarchical clustering method that recursively merges data points into clusters. The silhouette score was 0.19, indicating weak clustering.

## **Key Insights**

- **Cost vs. Rating**: Higher cost doesn't always guarantee better ratings; some expensive cuisines had low ratings.
- **Cuisines**: North Indian and Chinese cuisines were the most popular, while certain mixed cuisines also showed high demand.
- **Review Trends**: Review activity increased significantly over time, indicating rising customer engagement.
- **Sentiments**: A majority of reviews were positive, suggesting high customer satisfaction. However, there were notable negative reviews that need attention.

## **Business Impact**

- **Pricing and Menu Adjustments**: Optimize pricing strategies and menu offerings to enhance customer satisfaction.
- **Marketing and Promotions**: Target highly rated and popular cuisines for promotions to attract more customers.
- **Quality Improvement**: Address negative reviews and improve the quality of lower-rated restaurants to enhance overall customer experience.

## **Future Work**

- **Model Deployment**: Deploy the final KMeans model for real-time clustering and analysis of new restaurant data.
- **Enhanced Sentiment Analysis**: Incorporate more advanced NLP techniques and pretrained models to improve sentiment analysis accuracy.
- **Additional Features**: Include more features such as location, ambiance, and service quality for deeper insights into customer preferences.

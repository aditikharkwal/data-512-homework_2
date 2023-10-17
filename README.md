# data-512-homework_2 - Considering Bias in Data

The goal of this assignment is to explore the concept of bias in data using Wikipedia articles. This assignment will consider articles about cities in different US states. For this assignment, you will combine a dataset of Wikipedia articles with a dataset of state populations, and use a machine learning service called ORES to estimate the quality of the articles about the cities.

# Helpful API Documentation

1) [ORES Wiki](https://www.mediawiki.org/wiki/ORES)
2) [Wikipedia Content Assessment](https://en.wikipedia.org/wiki/Wikipedia:Content_assessment)
3) [Wikimedia API Documentation](https://www.mediawiki.org/wiki/API:Info)

# Steps and associated files to analyze data

<h2> Step 1: Getting the Article, Population and Region Data</h2>

The Data for this needs to be colected from various resources. The Data is extracted from Wikipedia API to extract a csv file containing Article Titles and Lastrevision IDs into a file named - "wiki_page_info.csv"

<h2> Step 2: Getting Article Quality Predictions </h2>

We're using a machine learning system called ORES. This was originally an acronym for "Objective Revision Evaluation Service" but was simply renamed “ORES”. ORES is a machine learning tool that can provide estimates of Wikipedia article quality. The article quality estimates are, from best to worst:
FA - Featured article
GA - Good article (sometimes called A-class)
B - B-class article
C - C-class article
Start - Start-class article
Stub - Stub-class article

<h2> Step 3: Data preprocessing </h2>

Perform some preprocessing steps to clean the data obtained from ores_predictions.csv before merging it with the remaining dataset.

<h2> Step 4: Combining the Datasets </h2>

Consolidate the merged data into a single CSV file called:
wp_scored_city_articles_by_state.csv

| Column  |
| ------------- |
| state  |
| regional_division  |
| population |
| article_title |
| revision_id |
| article_quality |

<h2> Step 5: Analysis </h2>

Analysis is produced in the form of data tables. We produced six total tables, that show:

1) Top 10 US states by coverage: The 10 US states with the highest total articles per capita (in descending order) .
2) Bottom 10 US states by coverage: The 10 US states with the lowest total articles per capita (in ascending order) .
3) Top 10 US states by high quality: The 10 US states with the highest high quality articles per capita (in descending order) .
4) Bottom 10 US states by high quality: The 10 US states with the lowest high quality articles per capita (in ascending order).
5) Census divisions by total coverage: A rank ordered list of US census divisions (in descending order) by total articles per capita.
6) Census divisions by high quality coverage: Rank ordered list of US census divisions (in descending order) by high quality articles per capita.


# Research Implications

In conducting this assignment, I embarked on a comprehensive exploration of bias within data, using Wikipedia articles as the primary source. The focal point of the analysis was the coverage of cities across different US states, coupled with an evaluation of the quality of articles pertaining to these cities. To accomplish this, I integrated datasets containing Wikipedia articles and state populations, and employed the ORES machine learning service for article quality estimation.

During the data processing and analysis, several potential sources of bias were identified. One prominent bias stemmed from the influence of population centers on per capita rankings. Larger cities tend to have more extensive coverage on Wikipedia due to their higher population and greater historical significance. This led to an inherent bias towards urban areas, potentially overshadowing the contributions and significance of smaller cities and rural communities.

Another notable bias arose from the varying quality of articles related to major cities. These articles, being subjects of frequent edits and revisions, exhibited a wider range of quality assessments. This could be attributed to the constant influx of information and viewpoints from a diverse set of contributors. Consequently, major cities' articles may require special attention and handling to ensure accurate and reliable content.

Additionally, a bias was observed in the naming conventions of articles for major cities. Many major cities lacked state names in their titles, necessitating additional steps for accurate classification and analysis. This bias could potentially lead to misclassification or oversight, impacting the overall assessment of article quality.

The results of this analysis suggest that (English) Wikipedia, while a valuable data source, is not without its limitations and biases. It serves as a rich repository of information, covering a wide array of topics, including cities in different US states. However, it is essential to approach Wikipedia data with a critical eye and an awareness of potential biases. Wikipedia is a valuable data source, but researchers must approach it with an understanding of its inherent biases. Careful consideration of population influence, article quality, and naming conventions is crucial for extracting accurate and reliable information. Additionally, leveraging tools like the ORES model can enhance the reliability and scalability of data extraction efforts.



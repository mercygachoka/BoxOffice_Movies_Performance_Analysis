# Microsoft Box Office Movies - Data Analysis

1. Project Description
   This project will utilize exploratory data analysis and data visualization to derive actionable insights from BoxOffice data, enabling Microsoft movie studio heads to make decisions regarding the most profitable box office movies to produce.

1.1 Business Problem
Microsoft recognizes the growing trend of major corporations investing in original video content and aims to venture into this lucrative domain by establishing its own movie studio. However, lacking expertise in the film industry, Microsoft seeks insights into the current landscape of successful films at the box office. As a data analyst, my task is to explore and analyze the characteristics of top-performing movies, discerning patterns and trends that contribute to their success. The findings will be translated into actionable insights, empowering Microsoft's movie studio head to make informed decisions regarding the types of films to produce, thereby maximizing the studio's potential for success in the competitive entertainment market.

1.2 Objectives
Based on the business problem provided, the following objectives can be derived:

To investigate current box office trends: Conduct an in-depth analysis of box office performance to identify patterns and trends in film genres, themes, and audience preferences.

To identify successful film characteristics: Determine the key factors contributing to the success of top-performing movies, including factors such as genre, cast, budget, and release timing.

To understand audience preferences: Explore audience demographics and preferences to gain insights into the types of films that resonate most with viewers.

To analyze competitor strategies: Evaluate strategies employed by successful movie studios and competitors to understand their approaches to creating profitable films.

To provide actionable insights: Translate research findings into practical recommendations for Microsoft's new movie studio, suggesting specific film concepts or genres that align with identified trends and audience preferences.

To develop effective production strategies: Offer recommendations on production strategies, including budget allocation, talent acquisition, and marketing tactics, based on the identified opportunities in the market.

1.3 Scope of the Objectives
The scope of the objectives includes the following aspects:

Box Office Data Analysis:

Analyze data on box office performance from various sources.
Focus on different film genres, themes, cast members, budgets, and release timings.
Identify trends and patterns in the data that correlate with high box office revenues.
Film Success Factors:

Investigate the characteristics of top-performing films.
Analyze factors such as storyline, genre and ratings
Audience Demographics and Preferences:

Study audience preferences for different genres, themes, and film styles.
Identify major competitors in the film industry.
Examine their strategies for film production, marketing, and distribution.
Analyze case studies of successful films from these competitors to glean insights into their approaches.
Actionable Insights for Microsoft's Studio:

Synthesize findings from data analysis, audience studies, and competitor analysis
Provide specific recommendations on film genres, themes, and production strategies that are likely to succeed.
Develop a framework for translating these insights into practical decision-making processes.
1.5 Expected Outcomes
Identification of Profitable Film Genres and Themes: Clear understanding of which film genres and themes are currently performing best at the box office, providing a basis for decision-making in film production.

Audience Insight Report: Comprehensive report detailing audience demographics and preferences, enabling tailored film production that resonates with target viewers.

Competitive Strategy Analysis: Insightful analysis of competitor strategies, highlighting successful practices that can be adopted or adapted by Microsoft's new movie studio.

Actionable Recommendations: Practical and data-driven recommendations for the types of films to produce, including detailed strategies for budget allocation, talent acquisition, and marketing efforts.

1.6 Findings
It was observed that a significant portion of revenue comes from foreign markets, indicating a strong correlation (0.83) between a movie's overall performance and its performance in international markets.
The analysis revealed that most movies make modest revenue, but a few hit big, showing that movie revenue follows a 'few blockbusters, many small earners' pattern
The most popular genres in the movie industry, based on the data analysis, are Drama, Documentary, and Comedy.
Over the years, foreign gross has consistently shown better returns, possibly due to its broader market coverage.
Microsoft's potential competitors, identified as the top-performing studios (BV, FOX, and WB), present opportunities for collaboration, allowing Microsoft to leverage their success in the film industry and enhance its position and offerings within the entertainment sector.
Drama, Documentary, and Comedy emerged as the most popular genres in the movie industry.
Movies with the highest ratings span genres such as Music, Mystery, Comedy, Drama, Reality TV, Action, Adventure, and Musical. Notably, Music and Mystery, despite being part of this list, are not the most frequently produced genres in the industry.
Action, Adventure, and Animation genres received the highest number of votes, indicating their popularity among the audience based on voting data.
The correlation between Ratings and Votes is 0.187, representing a weak positive correlation. While higher-rated movies tend to receive more votes, the relationship is not very strong.
R-rated movies were most prevalent, closely followed by Not Rated movies. PG and PG-13 movies had similar frequencies. G-rated movies were less common, and NC-17 received only one rating.
The most prevalent genre-rating combination is Action and Adventure with a G rating, closely followed by NR and PG ratings.
1.7 Data
We used data from three datasets. Below is the data description as indicated in the original data sets:

df_bom_movies_gross:

title: Movie title
studio: Movie studio companies
domestic_gross: Revenue generated in local markets
foreign_gross: Revenue generated in foreign markets
year: Year of release
rt.movie_info.tsv.gz:

'id': This column typically represents a unique identifier for each movie in the dataset.
'synopsis': This column contains a brief summary or description of the movie's plot or storyline.
'rating': This column indicates the rating assigned to the movie, reflecting its suitability for different audience age groups. Common ratings include G (General Audiences), PG (Parental Guidance Suggested), PG-13 (Parents Strongly Cautioned), R (Restricted), and NC-17 (Adults Only)
'genre': This column lists the genre or genres of the movie, categorizing it into different thematic categories.
'director': This column contains the name of the director(s) who directed the movie.
'writer': This column includes the name(s) of the writer(s) who wrote the screenplay or story for the movie.
'theater_date': This column represents the date when the movie was released in theaters.
'dvd_date': This column indicates the date when the movie was released on DVD or for home viewing.
'currency': This column specifies the currency used to report the box office revenue.
'box_office': This column contains the box office revenue generated by the movie, typically in the currency specified in - the 'currency' column.
'runtime': This column represents the duration or runtime of the movie in minutes.
'studio': This column contains the name of the production studio responsible for producing the movie.
im.db datasets (combination of three datasets):

Description of the Combined Dataset
movie_id: Unique identifier for the movie.
primary_title: The main title of the movie.
original_title: The original title of the movie (if different).
start_year: The release year of the movie.
runtime_minutes: The duration of the movie in minutes.
genres: Genres associated with the movie.
aka_title: Alternative title of the movie.
region: Region where the alternative title is used.
language: Language of the alternative title.
types: Types of alternative titles (e.g., DVD title, TV title).
attributes: Additional attributes of the alternative title.
is_original_title: Indicates if the title is the original title.
averagerating: Average rating of the movie.
numvotes: Number of votes the movie has received.
1.8 Data Analysis
The steps followed in data analysis

Data Collection: Gather relevant data from various sources, such as databases, APIs, or surveys.

Data Cleaning and Preprocessing: Cleanse the data by removing errors, handling missing values, and transforming it into a usable format.

Exploratory Data Analysis (EDA): Explore the dataset to understand its characteristics, patterns, and relationships through visualizations and summary statistics.

Statistical Analysis/Modeling: Apply statistical methods or machine learning algorithms to analyze the data and extract meaningful insights or build predictive models.

Interpretation of Results: Interpret the findings from the analysis to draw meaningful conclusions and insights.

Communication of Findings: Present the results and insights in a clear and understandable manner through reports, visualizations, and presentations to stakeholders

2. Import Packages

# Package for numerical computing

import numpy as np
​

# Data manipulation and analysis library

import pandas as pd  
​

# Statistical data visualization libraries

import matplotlib.pyplot as plt
import seaborn as sns
import matplotlib.ticker as ticker
from matplotlib.ticker import FuncFormatter
from matplotlib.ticker import MultipleLocator

# Importing the SQLite3 library for working with SQLite databases

import sqlite3  
​

# Display Matplotlib plots inline

%matplotlib inline
3 Load Data
Loading data from Bom Movies Gross

# Read the compressed CSV file using Pandas

df_bom_movies_gross = pd.read_csv(r'./zippedData/bom.movie_gross.csv.gz')
​

# Display the first few rows of the DataFrame

df_bom_movies_gross.head()
title studio domestic_gross foreign_gross year
0 Toy Story 3 BV 415000000.0 652000000 2010
1 Alice in Wonderland (2010) BV 334200000.0 691300000 2010
2 Harry Potter and the Deathly Hallows Part 1 WB 296000000.0 664300000 2010
3 Inception WB 292600000.0 535700000 2010
4 Shrek Forever After P/DW 238700000.0 513900000 2010
Loading data from Bom Movies Gross from "im.db"
import sqlite3
import zipfile
import os
​

# Path to the ZIP file

zip_file_path = r"./zippedData/im.db.zip"
​

# Extract the SQLite database file

with zipfile.ZipFile(zip_file_path, 'r') as zip_ref:
zip_ref.extractall("./zippedData/")
​

# Path to the extracted SQLite database file

db_file_path = os.path.join("./zippedData/", "im.db")
​

# Connect to the SQLite database

conn = sqlite3.connect(db_file_path)
​

# Create a cursor object to execute queries

cursor = conn.cursor()
Combining im.db datasets
#Create Query view data from movie_ratings tables
query = """
SELECT
mb.movie_id,
mb.primary_title,
mb.original_title,
mb.start_year,
mb.runtime_minutes,
mb.genres,
ma.title AS aka_title,
ma.region,
ma.language,
ma.types,
ma.attributes,
ma.is_original_title,
mr.averagerating,
mr.numvotes
FROM
movie_basics mb
LEFT JOIN
movie_akas ma
ON
mb.movie_id = ma.movie_id
LEFT JOIN
movie_ratings mr
ON
mb.movie_id = mr.movie_id;
​
"""
​
df_im_db = pd.read_sql(query, conn)
​

# Display the first few rows of the DataFrame

df_im_db.head()
movie_id primary_title original_title start_year runtime_minutes genres aka_title region language types attributes is_original_title averagerating numvotes
0 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sangharsh IN hi None alternative transliteration 0.0 7.0 77.0
1 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sungharsh IN hi None alternative spelling 0.0 7.0 77.0
2 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh None None original None 1.0 7.0 77.0
3 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN None None None 0.0 7.0 77.0
4 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN hi None alternative transliteration 0.0 7.0 77.0
Load the movie_info.tsv.gz into a DataFrame

# Load the gzip-compressed TSV file into a DataFrame

df_movie_info = pd.read_csv(r"./zippedData/rt.movie_info.tsv.gz", compression='gzip', sep='\t')
​

# Display the first few rows of the DataFrame

df_movie_info.head()
id synopsis rating genre director writer theater_date dvd_date currency box_office runtime studio
0 1 This gritty, fast-paced, and innovative police... R Action and Adventure|Classics|Drama William Friedkin Ernest Tidyman Oct 9, 1971 Sep 25, 2001 NaN NaN 104 minutes NaN
1 3 New York City, not-too-distant-future: Eric Pa... R Drama|Science Fiction and Fantasy David Cronenberg David Cronenberg|Don DeLillo Aug 17, 2012 Jan 1, 2013 $ 600,000 108 minutes Entertainment One
2 5 Illeana Douglas delivers a superb performance ... R Drama|Musical and Performing Arts Allison Anders Allison Anders Sep 13, 1996 Apr 18, 2000 NaN NaN 116 minutes NaN
3 6 Michael Douglas runs afoul of a treacherous su... R Drama|Mystery and Suspense Barry Levinson Paul Attanasio|Michael Crichton Dec 9, 1994 Aug 27, 1997 NaN NaN 128 minutes NaN
4 7 NaN NR Drama|Romance Rodney Bennett Giles Cooper NaN NaN NaN NaN 200 minutes NaN
df_movie_info.columns
Index(['id', 'synopsis', 'rating', 'genre', 'director', 'writer',
'theater_date', 'dvd_date', 'currency', 'box_office', 'runtime',
'studio'],
dtype='object')
4 Exploratory Data Analysis and Visualization from Bom Movies Gross
Understanding the structure of data
#Check number of row and colums
df_bom_movies_gross.shape
(3387, 5)

# Checking unique data for studio column

df_bom_movies_gross["studio"]
0 BV
1 BV
2 WB
3 WB
4 P/DW
...  
3382 Magn.
3383 FM
3384 Sony
3385 Synergetic
3386 Grav.
Name: studio, Length: 3387, dtype: object
"""
Obtaining key insights about the DataFrame df_bom_movies_gross using the info() method,
including missing values, column names, data types, and memory usage
"""
df_bom_movies_gross.info()
​
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 3387 entries, 0 to 3386
Data columns (total 5 columns):

# Column Non-Null Count Dtype

---

0 title 3387 non-null object
1 studio 3382 non-null object
2 domestic_gross 3359 non-null float64
3 foreign_gross 2037 non-null object
4 year 3387 non-null int64  
dtypes: float64(1), int64(1), object(3)
memory usage: 132.4+ KB
Foreign_gross is in object format (should be type converted to enable deriving meaningful statistical insights)
Missing values in studio, domestic_gross and foreign_gross columns
Statistical summary
df_bom_movies_gross.describe()
domestic_gross year
count 3.359000e+03 3387.000000
mean 2.874585e+07 2013.958075
std 6.698250e+07 2.478141
min 1.000000e+02 2010.000000
25% 1.200000e+05 2012.000000
50% 1.400000e+06 2014.000000
75% 2.790000e+07 2016.000000
max 9.367000e+08 2018.000000
Statistical summary of the df_bom_movies_gross dataset:

The maximum recorded domestic gross revenue is 936,700,000.0.−𝑇ℎ𝑒𝑚𝑖𝑛𝑖𝑚𝑢𝑚𝑟𝑒𝑐𝑜𝑟𝑑𝑒𝑑𝑑𝑜𝑚𝑒𝑠𝑡𝑖𝑐𝑔𝑟𝑜𝑠𝑠𝑟𝑒𝑣𝑒𝑛𝑢𝑒𝑖𝑠 100.
The dataset comprises data spanning from 2010 to 2018.
Distribution of Gross Revenues

# Assuming df_bom_movies_gross is defined and contains the necessary data

​

# Convert 'foreign_gross' column to numeric

df_bom_movies_gross['foreign_gross'] = pd.to_numeric(df_bom_movies_gross['foreign_gross'], errors='coerce')
​

# Drop rows with missing values in 'foreign_gross'

df_bom_movies_gross = df_bom_movies_gross.dropna(subset=['foreign_gross'])
​

# Get the maximum value between domestic_gross and foreign_gross

max_value = max(df_bom_movies_gross['domestic_gross'].max(), df_bom_movies_gross['foreign_gross'].max())
​

# Set seaborn style

sns.set_style("whitegrid")
​

# Create subplots

fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(16, 8), sharex=True)
​

# Histogram and KDE of domestic_gross

sns.histplot(df_bom_movies_gross['domestic_gross'], bins=20, kde=True, color='skyblue', edgecolor='black', ax=ax1)
ax1.set_xlabel('Gross Revenue', fontsize=16, fontweight='bold')
ax1.set_ylabel('Frequency', fontsize=16, fontweight='bold')
ax1.set_title('Distribution of Domestic Gross Revenue', fontsize=18, fontweight='bold')
ax1.grid(False)
​

# Set y-ticks and minor ticks

ax1.yaxis.set_major_locator(MultipleLocator(200))
ax1.yaxis.set_minor_locator(MultipleLocator(100))
​

# Set x-ticks

ax1.xaxis.set_major_formatter(ticker.FuncFormatter(lambda x, pos: '$%1.0fM' % (x \* 1e-6)))
ax1.xaxis.set_minor_locator(MultipleLocator(0.1e9))
​

# Set x-limits and y-limits

ax1.set_xlim(0, max_value)
ax1.set_ylim(0, 1600) # Adjusted
​

# Histogram and KDE of foreign_gross

sns.histplot(df_bom_movies_gross['foreign_gross'], bins=20, kde=True, color='green', edgecolor='black', ax=ax2)
ax2.set_xlabel('Gross Revenue', fontsize=16, fontweight='bold')
ax2.set_ylabel('Frequency', fontsize=16, fontweight='bold')
ax2.set_title('Distribution of Foreign Gross Revenue', fontsize=18, fontweight='bold')
ax2.grid(False)
​

# Set y-ticks and minor ticks

ax2.yaxis.set_major_locator(MultipleLocator(200))
ax2.yaxis.set_minor_locator(MultipleLocator(100))
​

# Set x-ticks

ax2.xaxis.set_major_formatter(ticker.FuncFormatter(lambda x, pos: '$%1.0fM' % (x \* 1e-6)))
ax2.xaxis.set_minor_locator(MultipleLocator(0.1e9))
​

# Set x-limits and y-limits

ax2.set_xlim(0, max_value)
ax2.set_ylim(0, 1600) # Adjusted
​
plt.tight_layout()
plt.show()
​

The distributions of Foreign Gross and Domestic Gross both demonstrate positive skewness.
This skewness indicates that the majority of the data points are concentrated towards the lower end of the revenue scale, with fewer data points extending towards higher revenue values.
This suggests that most movies tend to generate relatively lower revenue, while a smaller proportion of movies achieve higher revenue levels.
The presence of data points trailing off to the right, beyond the bulk of the distribution, raises questions about their nature. It prompts us to investigate whether these outliers represent exceptional cases of movies that have generated substantial sales, or if they are simply anomalies within the dataset.
Checking Missing Data

# Check for missing values in each column

missing_values = df_bom_movies_gross.isnull().sum()
missing_values
title 0
studio 4
domestic_gross 28
foreign_gross 0
year 0
dtype: int64
Studio and domestic_gross have missing data
Handle Missing Values

# Handle Missing Values

​

# Drop rows with missing values in 'studio' and 'domestic_gross' columns

df_bom_movies_gross.dropna(subset=['studio', 'domestic_gross'], inplace=True)  
​

# Replace missing values in 'domestic_gross' with median

df_bom_movies_gross['domestic_gross'].fillna(df_bom_movies_gross['domestic_gross'].median(), inplace=True)
​

# Convert 'foreign_gross' to numeric

df_bom_movies_gross['foreign_gross'] = pd.to_numeric(df_bom_movies_gross['foreign_gross'], errors='coerce')
Dropped the 'studio' and 'domestic_gross' columns with missing values, as they were few compared to the size of the dataset.
Since 'domestic_gross' has a positive skew, median imputation was used to impute missing values.
Visualizing data after removing missing values
​

# Convert 'foreign_gross' column to numeric

df_bom_movies_gross['foreign_gross'] = pd.to_numeric(df_bom_movies_gross['foreign_gross'], errors='coerce')
​

# Drop rows with missing values in 'foreign_gross'

df_bom_movies_gross = df_bom_movies_gross.dropna(subset=['foreign_gross'])
​

# Get the maximum value between domestic_gross and foreign_gross

max_value = max(df_bom_movies_gross['domestic_gross'].max(), df_bom_movies_gross['foreign_gross'].max())
​

# Set seaborn style

sns.set_style("whitegrid")
​

# Create subplots

fig, (ax1, ax2) = plt.subplots(1, 2, figsize=(16, 8), sharex=True)
​

# Histogram and KDE of domestic_gross

sns.histplot(df_bom_movies_gross['domestic_gross'], bins=20, kde=True, color='skyblue', edgecolor='black', ax=ax1)
ax1.set_xlabel('Gross Revenue (in $)')
ax1.set_ylabel('Frequency')
ax1.set_title('Distribution of Domestic Gross Revenue')
ax1.grid(False)
​

# Set y-ticks and minor ticks

ax1.yaxis.set_major_locator(MultipleLocator(200))
ax1.yaxis.set_minor_locator(MultipleLocator(100))
​

# Set x-ticks

ax1.xaxis.set_major_formatter(ticker.FuncFormatter(lambda x, pos: '$%1.0fM' % (x \* 1e-6)))
ax1.xaxis.set_minor_locator(MultipleLocator(0.1e9))
​

# Set x-limits and y-limits

ax1.set_xlim(0, max_value)
ax1.set_ylim(0, 1600) # Adjusted
​

# Histogram and KDE of foreign_gross

sns.histplot(df_bom_movies_gross['foreign_gross'], bins=20, kde=True, color='green', edgecolor='black', ax=ax2)
ax2.set_xlabel('Gross Revenue (in $)')
ax2.set_ylabel('Frequency')
ax2.set_title('Distribution of Foreign Gross Revenue')
ax2.grid(False)
​

# Set y-ticks and minor ticks

ax2.yaxis.set_major_locator(MultipleLocator(200))
ax2.yaxis.set_minor_locator(MultipleLocator(100))
​

# Set x-ticks

ax2.xaxis.set_major_formatter(ticker.FuncFormatter(lambda x, pos: '$%1.0fM' % (x \* 1e-6)))
ax2.xaxis.set_minor_locator(MultipleLocator(0.1e9))
​

# Set x-limits and y-limits

ax2.set_xlim(0, max_value)
ax2.set_ylim(0, 1600) # Adjusted
​
plt.tight_layout()
plt.show()

Mediam imputation has not affected the data distribution
Handle Outliers
Visualize outliers using box plots for domestic gross revenues

# Set seaborn style

sns.set_style("whitegrid")
​

# Visualize outliers using box plot with seaborn

plt.figure(figsize=(16, 10))
​

# Box plot for 'foreign_gross'

ax = sns.boxplot(data=df_bom_movies_gross['domestic_gross'], color='skyblue')
ax.yaxis.set_major_formatter(ticker.FuncFormatter(lambda x, pos: '${:.0f}M'.format(x \* 1e-6))) # Format y-axis ticks
plt.title('Box Plot of Foreign Gross (Before Handling Outliers)', fontsize=18, fontweight='bold')
plt.ylabel('Foreign Gross Revenue', fontsize=16, fontweight='bold')
plt.xlabel('')
plt.yticks(fontsize=16, fontweight='bold')
plt.show()

In the context of movie sales data, it's possible that some movies make exceptionally high sales due to factors such as blockbuster releases, franchise popularity, or critical acclaim. In such cases, these outliers may provide valuable insights into trends or anomalies in the movie industry.

Visualize outliers using box plots for foreign gross revenues

# Set seaborn style

sns.set_style("whitegrid")
​

# Visualize outliers using box plot with seaborn

plt.figure(figsize=(16, 10))
​

# Box plot for 'foreign_gross'

ax = sns.boxplot(data=df_bom_movies_gross['foreign_gross'], palette='Blues')
ax.yaxis.set_major_formatter(ticker.FuncFormatter(lambda x, pos: '${:.0f}M'.format(x \* 1e-6))) # Format y-axis ticks
plt.title('Box Plot of Foreign Gross (Before Handling Outliers)', fontsize=18, fontweight='bold')
plt.ylabel('Foreign Gross Revenue', fontsize=16, fontweight='bold')
​
plt.yticks(fontsize=16, fontweight='bold')
plt.show()

Outliers in foreign gross revenue for movies could represent exceptional cases where certain films achieve unusually high levels of international box office success, potentially due to factors such as unexpected popularity in specific regions, large-scale marketing campaigns, or unique cultural appeal.

Data Types Conversions

# Convert 'year' to datetime

df_bom_movies_gross['year'] = pd.to_datetime(df_bom_movies_gross['year'], format='%Y')  
df_bom_movies_gross.info()
<class 'pandas.core.frame.DataFrame'>
Int64Index: 2002 entries, 0 to 3353
Data columns (total 5 columns):

# Column Non-Null Count Dtype

---

0 title 2002 non-null object  
 1 studio 2002 non-null object  
 2 domestic_gross 2002 non-null float64  
 3 foreign_gross 2002 non-null float64  
 4 year 2002 non-null datetime64[ns]
dtypes: datetime64[ns](1), float64(2), object(2)
memory usage: 173.8+ KB
To utilize the year column effectively, we converted its type to datetime.
Correlation heatmap

# Rename columns for clarity (optional, adjust names as needed)

renamed_cols = {'domestic_gross': 'Domestic Gross', 'foreign_gross': 'Foreign Gross'}
df_bom_movies_gross_heatmap = df_bom_movies_gross.rename(columns=renamed_cols)
​

# Calculate correlation matrix

correlation_matrix = df_bom_movies_gross_heatmap.corr()
​

# Create correlation heatmap

plt.figure(figsize=(10, 6))
sns.heatmap(correlation_matrix, annot=True, cmap='Blues', fmt='.2f', linewidths=0.5) # Add line width for better separation
​

# Customize title

plt.title('Correlation Between Domestic and Foreign Gross', fontsize=18, fontweight='bold')
​

# Rotate x-axis labels for readability (optional)

plt.xticks(rotation=45, ha='right', fontsize=14, fontweight='bold')
plt.yticks(rotation=0, ha='right', fontsize=14, fontweight='bold')
​
plt.tight_layout()
plt.show()

In the context of Microsoft's movie studio venture, a high positive (0.83) correlation between domestic and foreign gross revenue may indicate that movies with high domestic box office performance also tend to perform well in foreign markets, and vice versa. This insight can be valuable for decision-making processes related to budget allocation, marketing strategies, and international distribution efforts.
df_bom_movies_gross.info()
<class 'pandas.core.frame.DataFrame'>
Int64Index: 2002 entries, 0 to 3353
Data columns (total 5 columns):

# Column Non-Null Count Dtype

---

0 title 2002 non-null object  
 1 studio 2002 non-null object  
 2 domestic_gross 2002 non-null float64  
 3 foreign_gross 2002 non-null float64  
 4 year 2002 non-null datetime64[ns]
dtypes: datetime64[ns](1), float64(2), object(2)
memory usage: 173.8+ KB
Yearly Trends in Domestic Gross Revenue

# Convert 'year' column to datetime format

df_bom_movies_gross['year'] = pd.to_datetime(df_bom_movies_gross['year'], format='%Y')
​

# Accessing the year from the 'year' column

df_bom_movies_gross['year'] = df_bom_movies_gross['year'].dt.year
​
#Create a figure and axis for the foreign gross plot
plt.figure(figsize=(12, 6))
​
​

# Plot yearly trends for domestic gross revenue

sns.boxplot(x='year', y='domestic_gross', data=df_bom_movies_gross, color='skyblue')
plt.title('Yearly Trends in Domestic Gross Revenue', fontsize=18, fontweight='bold')
plt.xlabel('Year Movie Released', fontsize=16, fontweight='bold')
plt.ylabel('Domestic Gross Revenue', fontsize=16, fontweight='bold')
plt.xticks(rotation=45, fontsize=14, fontweight='bold') # Rotate x-axis labels for better readability
plt.yticks(fontsize=14, fontweight='bold')
​

# Format y-axis labels as $4M

formatter = FuncFormatter(lambda x, pos: f'${int(x/1e6)}M')
plt.gca().yaxis.set_major_formatter(formatter)
​

# Remove grid

plt.grid(False)
​

# Show plot

plt.tight_layout()
plt.show()
​

# Create a figure and axis for the foreign gross plot

plt.figure(figsize=(12, 6))
​

# Plot yearly trends for foreign gross revenue

sns.boxplot(x='year', y='foreign_gross', data=df_bom_movies_gross, color='darkgreen')
plt.title('Yearly Trends in Foreign Gross Revenue', fontsize=18, fontweight='bold')
plt.xlabel('Year Movie Released', fontsize=16, fontweight='bold')
plt.ylabel('Foreign Gross Revenue', fontsize=16, fontweight='bold')
plt.xticks(rotation=45, fontsize=14, fontweight='bold') # Rotate x-axis labels for better readability
plt.yticks(fontsize=14, fontweight='bold')
​

# Format y-axis labels as $4M

formatter = FuncFormatter(lambda x, pos: f'${int(x/1e6)}M')
plt.gca().yaxis.set_major_formatter(formatter)
​

# Remove grid

plt.grid(False)
​

# Show plot

plt.tight_layout()
plt.show()
​

For Domestic Gross: the median of domestic gross revenue is near the lower part of the box, an indication that a significant portion of the movies or revenue data points have relatively lower domestic gross earnings. This could imply that there are many movies with moderate to low domestic earnings, with fewer outliers or extreme high-earning movies.

For Foreign Gross: similarly, median of foreign gross revenue is near the lower part of the box, it suggests that a substantial portion of the movies or revenue data points have relatively lower foreign gross earnings. This might indicate that the distribution of foreign gross earnings is skewed towards lower values, with fewer movies achieving exceptionally high foreign revenues.

The above observations could indicate that there hasn't been significant growth in domestic and foreign gross revenue over the years.

Yearly Trends in Domestic Gross Revenue
​

# Calculate yearly totals for domestic and foreign gross

df_yearly_totals = df_bom_movies_gross.groupby('year').sum().reset_index()
df_yearly_totals
year domestic_gross foreign_gross
0 2010 1.015274e+10 1.436937e+10
1 2011 9.915690e+09 1.566287e+10
2 2012 1.069786e+10 1.700298e+10
3 2013 1.055885e+10 1.658024e+10
4 2014 1.014798e+10 1.695667e+10
5 2015 8.802869e+09 1.515435e+10
6 2016 1.086969e+10 1.898139e+10
7 2017 1.029077e+10 1.992893e+10
8 2018 1.008556e+10 1.747449e+10
​

# Calculate yearly totals for domestic and foreign gross

df_yearly_totals = df_bom_movies_gross.groupby('year').sum().reset_index()
​

# Create stacked bar chart with Matplotlib

plt.figure(figsize=(16, 10))
​

# Define bar width and offset

bar_width = 0.35
offset = bar_width / 2
​

# Plot domestic gross

plt.bar(df_yearly_totals['year'] - offset, df_yearly_totals['domestic_gross'], width=bar_width, color='skyblue', label='Domestic Gross')
​

# Plot foreign gross on top of domestic gross

plt.bar(df_yearly_totals['year'] + offset, df_yearly_totals['foreign_gross'], width=bar_width, color='navy', label='Foreign Gross')
​
plt.xlabel('Year Movie Released', fontsize=16, fontweight='bold')
plt.ylabel('Total Gross Revenue', fontsize=16, fontweight='bold')
​

# Format y-axis labels as $4M

formatter = ticker.FuncFormatter(lambda x, pos: f'${int(x/1e6)}M')
plt.gca().yaxis.set_major_formatter(formatter)
​

# Set x-tick locations and labels

plt.xticks(df_yearly_totals['year'], rotation=45, ha='right', fontsize=14, fontweight='bold')
plt.yticks(fontsize=16, fontweight='bold')
plt.title('Yearly Total Gross Revenue', fontsize=18, fontweight='bold')
plt.legend(fontsize=16)
plt.tight_layout()
​

# Remove grid

plt.grid(False)
​
plt.show()

Over the years, foreign gross has been delivering better returns. This could be attributed to the fact that foreign markets cover more regions.
Top Ten Performing Movie Studio Companies by Total Gross Revenue

# Calculate the total gross revenue (domestic + foreign) for each movie

df_bom_movies_gross['total_gross'] = df_bom_movies_gross['domestic_gross'] + df_bom_movies_gross['foreign_gross']
​

# Group the data by studio and calculate the total gross revenue for each studio

studio_gross = df_bom_movies_gross.groupby('studio')['total_gross'].sum().nlargest(10)
​

# Sort the studios based on their total gross revenue in descending order

top_ten_studios = studio_gross.sort_values(ascending=False)
​

# Convert studio names to uppercase

top_ten_studios.index = top_ten_studios.index.str.upper()
​

# Convert gross revenue to billions of dollars

top_ten_studios_billions = top_ten_studios / 1e9 # Divide by 1 billion
​

# Create a horizontal bar chart

plt.figure(figsize=(12, 8))
colors = sns.color_palette("coolwarm", len(top_ten_studios)) # Use a color palette for aesthetics
plt.barh(top_ten_studios.index, top_ten_studios_billions, color='Skyblue')
plt.xlabel('Total Gross Revenue ($B Dollars)', fontsize=14, fontweight='bold')
plt.ylabel('Movie Studio Companies', fontsize=14, fontweight='bold')
plt.title('Top Ten Performing Movie Studio Companies by Total Gross Revenue', fontsize=16, fontweight='bold')
plt.gca().invert_yaxis() # Invert y-axis to display the highest revenue studio at the top
​

# Add data labels

for index, value in enumerate(top_ten_studios_billions):
plt.text(value, index, f'${value:.2f}B', ha='left', va='center', fontsize=12, fontweight='bold')
​

# Remove grid

plt.grid(False)
​

# Hide x-axis ticks

plt.xticks([])
plt.yticks(fontsize=12, fontweight='bold')
​
plt.tight_layout() # Adjust layout
plt.show()

The top-performing studios, include BV, FOX, and WB.
Partnering with these successful movie companies could allow Microsoft to tap into their achievements in the film industry, potentially strengthening its foothold and offerings within the entertainment sector
5 Exploratory Data Analysis and Visualization on data from im.db
#View first rows
df_im_db.head()
movie_id primary_title original_title start_year runtime_minutes genres aka_title region language types attributes is_original_title averagerating numvotes
0 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sangharsh IN hi None alternative transliteration 0.0 7.0 77.0
1 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sungharsh IN hi None alternative spelling 0.0 7.0 77.0
2 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh None None original None 1.0 7.0 77.0
3 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN None None None 0.0 7.0 77.0
4 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN hi None alternative transliteration 0.0 7.0 77.0

# Print the dimensions (rows, columns) of the dataframe

df_im_db.shape
(355545, 14)
Number of columns: 355545
Number of rows: 14

# # Print information about the dataframe

df_im_db.info()
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 355545 entries, 0 to 355544
Data columns (total 14 columns):

# Column Non-Null Count Dtype

---

0 movie_id 355545 non-null object
1 primary_title 355545 non-null object
2 original_title 355513 non-null object
3 start_year 355545 non-null int64  
 4 runtime_minutes 314219 non-null float64
5 genres 348882 non-null object
6 aka_title 331703 non-null object
7 region 278410 non-null object
8 language 41715 non-null object
9 types 168447 non-null object
10 attributes 14925 non-null object
11 is_original_title 331678 non-null float64
12 averagerating 266085 non-null float64
13 numvotes 266085 non-null float64
dtypes: float64(4), int64(1), object(9)
memory usage: 38.0+ MB
All columns have missing data
Rename Columns
#View Columns
df_im_db.columns
Index(['movie_id', 'primary_title', 'original_title', 'start_year',
'runtime_minutes', 'genres', 'aka_title', 'region', 'language', 'types',
'attributes', 'is_original_title', 'averagerating', 'numvotes'],
dtype='object')

# Rename columns with appealing names

column_names = {
'movie_id': 'Movie ID',
'primary_title': 'Primary Title',
'original_title': 'Original Title',
'start_year': 'Start Year',
'runtime_minutes': 'Runtime (Minutes)',
'genres': 'Genres',
'aka_title': 'AKA Title',
'region': 'Region',
'language': 'Language',
'types': 'Types',
'attributes': 'Attributes',
'is_original_title': 'Is Original Title',
'averagerating': 'Average Rating',
'numvotes': 'Number of Votes'
}
​
df_im_db.rename(columns=column_names, inplace=True)
#Verify columns renamed
df_im_db.columns
Index(['Movie ID', 'Primary Title', 'Original Title', 'Start Year',
'Runtime (Minutes)', 'Genres', 'AKA Title', 'Region', 'Language',
'Types', 'Attributes', 'Is Original Title', 'Average Rating',
'Number of Votes'],
dtype='object')
#Statistical Summary for numerical values
df_im_db.describe()
Start Year Runtime (Minutes) Is Original Title Average Rating Number of Votes
count 355545.000000 314219.000000 331678.000000 266085.000000 2.660850e+05
mean 2014.391576 95.378647 0.134769 6.278564 2.831932e+04
std 2.702009 188.808216 0.341477 1.266803 9.403901e+04
min 2010.000000 1.000000 0.000000 1.000000 5.000000e+00
25% 2012.000000 83.000000 0.000000 5.600000 5.700000e+01
50% 2014.000000 94.000000 0.000000 6.400000 5.740000e+02
75% 2017.000000 107.000000 0.000000 7.100000 7.156000e+03
max 2115.000000 51420.000000 1.000000 10.000000 1.841066e+06
Movie Runtime:
Longest Runtime: A movie with a runtime of 51420 minutes (almost 857 hours) is incredibly long. This is likely an outlier and might represent a TV series, miniseries, or an exceptionally long documentary. Runtimes this long are highly - uncommon for movies.
Shortest Runtime: A movie with a runtime of 1 minute is also unusual. It could be inaccurate data, a very short film, or possibly a trailer included in the dataset.
Average Runtime:
The average runtime of 95 minutes falls within a normal range for movies. Most feature-length films typically range from 90 minutes to 120 minutes.
Movie Ratings:
The voting range of 1 to 10 seems standard for movie rating systems.
The average rating of approximately 6.2 indicates a slightly above-average user reception for the movies in this dataset.
Year: Year range seems to span 2115 to 2014, the minimum year is incorrect since we are in 2024
What to consider next:

Investigate the Longest Runtime: Check if the movie title or other details associated with the 51420-minute runtime entry can help determine if it's a movie, TV series, or something else.
Examine the Shortest Runtime: Verify the data source for the 1-minute movie. If it's not a genuine movie, consider removing it or addressing it in your data cleaning process.
Explore how runtime or ratings correlate with other movie attributes in the dataset.
Consider droopping minimum year

# Check rows with missing values

df_im_db.isna().sum()
Movie ID 0
Primary Title 0
Original Title 32
Start Year 0
Runtime (Minutes) 41326
Genres 6663
AKA Title 23842
Region 77135
Language 313830
Types 187098
Attributes 340620
Is Original Title 23867
Average Rating 89460
Number of Votes 89460
dtype: int64
11 out of 14 values have got missing values
Visualizing missing values

# Calculate the number of missing values for each column

missing_values = df_im_db.isnull().sum()
​

# Calculate the percentage of missing values for each column

percent_missing = (missing_values / len(df_im_db)) \* 100
​

# Convert missing values to "350k" format

missing_values_formatted = missing_values.apply(lambda x: f'{x/1000:.0f}k')
​

# Create a bar chart with Seaborn palette

fig, ax = plt.subplots(figsize=(16, 10))
bars = ax.bar(missing_values.index, missing_values.values, color="skyblue")
​

# Add percentage labels to each bar

for bar, percent in zip(bars, percent_missing.values):
height = bar.get_height()
ax.text(bar.get_x() + bar.get_width() / 2, height,
f'{percent:.2f}%', ha='center', va='bottom', fontsize=12, fontweight='bold')
​
ax.set_title('Missing Values in Bom Movies Gross Dataframe', fontsize=18, fontweight='bold')
ax.set_xlabel('Columns in Bom Movies Gross Dataframe', fontsize=16, fontweight="bold")
ax.set_ylabel('Number of Missing Values', fontsize=14, fontweight="bold")
​

# Set tick locations and labels

ax.set_xticks(range(len(missing_values)))
ax.set_xticklabels(missing_values.index, rotation=45, ha='right', fontsize=14, fontweight="bold")
​

# Format y-axis labels as "350k"

ax.yaxis.set_major_formatter(ticker.FuncFormatter(lambda x, pos: f'{x/1000:.0f}k'))
​

# Remove grid

ax.grid(False)
​
plt.tight_layout()
plt.show()

Columns like "Languages", "Types", and "Attributes" have the highest percentages of missing values, at 55.62%, 88.27%, and 95.80% respectively. This suggests that a significant portion of the data in these columns is absent.
Other columns with over 10% missing data include: Runtime(Minutes), Region, Is Original Title, Average Rating and Number of Votes
Overall The DataFrame likely has a considerable amount of missing data, especially in the columns mentioned. This could pose challenges when analyzing the data or drawing conclusions from it.
Handle Missing Values
df_im_db.columns
Index(['Movie ID', 'Primary Title', 'Original Title', 'Start Year',
'Runtime (Minutes)', 'Genres', 'AKA Title', 'Region', 'Language',
'Types', 'Attributes', 'Is Original Title', 'Average Rating',
'Number of Votes'],
dtype='object')
df_im_db.head()
Movie ID Primary Title Original Title Start Year Runtime (Minutes) Genres AKA Title Region Language Types Attributes Is Original Title Average Rating Number of Votes
0 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sangharsh IN hi None alternative transliteration 0.0 7.0 77.0
1 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sungharsh IN hi None alternative spelling 0.0 7.0 77.0
2 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh None None original None 1.0 7.0 77.0
3 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN None None None 0.0 7.0 77.0
4 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN hi None alternative transliteration 0.0 7.0 77.0

# Drop rows where 'Primary Title' or 'Start Year' have missing values

df_im_db.dropna(subset=['Movie ID', 'Primary Title', 'Start Year'], inplace=True)
​

# Display the resulting DataFrame

df_im_db
Movie ID Primary Title Original Title Start Year Runtime (Minutes) Genres AKA Title Region Language Types Attributes Is Original Title Average Rating Number of Votes
0 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sangharsh IN hi None alternative transliteration 0.0 7.0 77.0
1 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sungharsh IN hi None alternative spelling 0.0 7.0 77.0
2 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh None None original None 1.0 7.0 77.0
3 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN None None None 0.0 7.0 77.0
4 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN hi None alternative transliteration 0.0 7.0 77.0
... ... ... ... ... ... ... ... ... ... ... ... ... ... ...
355540 tt9916538 Kuambil Lagi Hatiku Kuambil Lagi Hatiku 2019 123.0 Drama None None None None None NaN NaN NaN
355541 tt9916622 Rodolpho Teóphilo - O Legado de um Pioneiro Rodolpho Teóphilo - O Legado de um Pioneiro 2015 NaN Documentary None None None None None NaN NaN NaN
355542 tt9916706 Dankyavar Danka Dankyavar Danka 2013 NaN Comedy None None None None None NaN NaN NaN
355543 tt9916730 6 Gunn 6 Gunn 2017 116.0 None None None None None None NaN NaN NaN
355544 tt9916754 Chico Albuquerque - Revelações Chico Albuquerque - Revelações 2013 NaN Documentary None None None None None NaN NaN NaN
355545 rows × 14 columns

Rows with missing movie_id, primary_title, or start_year are dropped because these columns are crucial for identifying and analyzing each movie

# Drop specific columns with too many missing values

df_im_db.drop(columns=['Language', 'Types', 'Attributes'], inplace=True)
​
Excessive Missing Data: Rows with excessive missing data (more than 50% missing) are dropped to maintain data quality.

# Fill missing 'original_title' with 'primary_title' if missing

df_im_db['Original Title'] = df_im_db['Original Title'].fillna(df_im_db['Primary Title'])
df_im_db['Original Title'].value_counts()
Frozen 77
Home 73
Star Wars: Episode VII - The Force Awakens 61
Inside Out 60
Robin Hood 59
..
Imágenes del Tío Sam 1
Chasing Chaplin 1
Six Strings of Separation 1
Lefty Loosey Righty Tighty 1
Kundbypigen: hvorfor ville min lillesøster være terrorist? 1
Name: Original Title, Length: 137787, dtype: int64
The rationale behind this is that the 'Primary Title' likely represents a valid substitute for the 'Original Title' when the original title is unavailable.

# Fill missing numeric values with the median

df_im_db['Runtime (Minutes)'] = df_im_db['Runtime (Minutes)'].fillna(df_im_db['Runtime (Minutes)'].median())
df_im_db['Average Rating'] = df_im_db['Average Rating'].fillna(df_im_db['Average Rating'].median())
df_im_db['Number of Votes'] = df_im_db['Number of Votes'].fillna(df_im_db['Number of Votes'].median())
Using median imputation is likely to distort the mean, providing a more accurate central tendency

# Fill missing categorical values with 'Unknown'

df_im_db['Genres'] = df_im_db['Genres'].fillna('Unknown')
df_im_db['Region'] = df_im_db['Region'].fillna('Unknown')
The substitution of "Original" in the 'Original Title' column where 'Types' is equal to 1.0 suggests a specific condition or category where the movie's original title is known.
This substitution assumes that when 'Types' is 1.0, it signifies a certain type or category of movies where the original title is explicitly provided.
df_im_db.info()
<class 'pandas.core.frame.DataFrame'>
Int64Index: 355545 entries, 0 to 355544
Data columns (total 11 columns):

# Column Non-Null Count Dtype

---

0 Movie ID 355545 non-null object
1 Primary Title 355545 non-null object
2 Original Title 355545 non-null object
3 Start Year 355545 non-null int64  
 4 Runtime (Minutes) 355545 non-null float64
5 Genres 355545 non-null object
6 AKA Title 331703 non-null object
7 Region 355545 non-null object
8 Is Original Title 331678 non-null float64
9 Average Rating 355545 non-null float64
10 Number of Votes 355545 non-null float64
dtypes: float64(4), int64(1), object(6)
memory usage: 32.6+ MB
df_im_db.head()
Movie ID Primary Title Original Title Start Year Runtime (Minutes) Genres AKA Title Region Is Original Title Average Rating Number of Votes
0 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sangharsh IN 0.0 7.0 77.0
1 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sungharsh IN 0.0 7.0 77.0
2 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh Unknown 1.0 7.0 77.0
3 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN 0.0 7.0 77.0
4 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN 0.0 7.0 77.0
Remove Duplicates

# Check Duplicated rows

duplicates = df_im_db.duplicated()
print(duplicates.sum())
650

# Drop duplicate movie_id rows, keeping the first occurrence

df_im_db.drop_duplicates(subset='Movie ID', keep='first')
df_im_db
Movie ID Primary Title Original Title Start Year Runtime (Minutes) Genres AKA Title Region Is Original Title Average Rating Number of Votes
0 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sangharsh IN 0.0 7.0 77.0
1 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sungharsh IN 0.0 7.0 77.0
2 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh Unknown 1.0 7.0 77.0
3 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN 0.0 7.0 77.0
4 tt0063540 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN 0.0 7.0 77.0
... ... ... ... ... ... ... ... ... ... ... ...
355540 tt9916538 Kuambil Lagi Hatiku Kuambil Lagi Hatiku 2019 123.0 Drama None Unknown NaN 6.4 574.0
355541 tt9916622 Rodolpho Teóphilo - O Legado de um Pioneiro Rodolpho Teóphilo - O Legado de um Pioneiro 2015 94.0 Documentary None Unknown NaN 6.4 574.0
355542 tt9916706 Dankyavar Danka Dankyavar Danka 2013 94.0 Comedy None Unknown NaN 6.4 574.0
355543 tt9916730 6 Gunn 6 Gunn 2017 116.0 Unknown None Unknown NaN 6.4 574.0
355544 tt9916754 Chico Albuquerque - Revelações Chico Albuquerque - Revelações 2013 94.0 Documentary None Unknown NaN 6.4 574.0
355545 rows × 11 columns

#Drop Movie ID column
df_im_db.drop(columns=['Movie ID'])
Primary Title Original Title Start Year Runtime (Minutes) Genres AKA Title Region Is Original Title Average Rating Number of Votes
0 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sangharsh IN 0.0 7.0 77.0
1 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sungharsh IN 0.0 7.0 77.0
2 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh Unknown 1.0 7.0 77.0
3 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN 0.0 7.0 77.0
4 Sunghursh Sunghursh 2013 175.0 Action,Crime,Drama Sunghursh IN 0.0 7.0 77.0
... ... ... ... ... ... ... ... ... ... ...
355540 Kuambil Lagi Hatiku Kuambil Lagi Hatiku 2019 123.0 Drama None Unknown NaN 6.4 574.0
355541 Rodolpho Teóphilo - O Legado de um Pioneiro Rodolpho Teóphilo - O Legado de um Pioneiro 2015 94.0 Documentary None Unknown NaN 6.4 574.0
355542 Dankyavar Danka Dankyavar Danka 2013 94.0 Comedy None Unknown NaN 6.4 574.0
355543 6 Gunn 6 Gunn 2017 116.0 Unknown None Unknown NaN 6.4 574.0
355544 Chico Albuquerque - Revelações Chico Albuquerque - Revelações 2013 94.0 Documentary None Unknown NaN 6.4 574.0
355545 rows × 10 columns

# Check dataset

df_im_db.info()
<class 'pandas.core.frame.DataFrame'>
Int64Index: 355545 entries, 0 to 355544
Data columns (total 11 columns):

# Column Non-Null Count Dtype

---

0 Movie ID 355545 non-null object
1 Primary Title 355545 non-null object
2 Original Title 355545 non-null object
3 Start Year 355545 non-null int64  
 4 Runtime (Minutes) 355545 non-null float64
5 Genres 355545 non-null object
6 AKA Title 331703 non-null object
7 Region 355545 non-null object
8 Is Original Title 331678 non-null float64
9 Average Rating 355545 non-null float64
10 Number of Votes 355545 non-null float64
dtypes: float64(4), int64(1), object(6)
memory usage: 32.6+ MB
AKA Title column has missing values, we are going to drop it since Primary Title and Original Title columns can serve as substitutions
Drop Columns not Useful in Analysis
​

# Dropping the specified columns

df_im_db.drop(columns=['AKA Title', 'Original Title', 'Is Original Title'], inplace=True)
​

# Display the DataFrame to ensure columns are dropped

df_im_db.head()
Movie ID Primary Title Start Year Runtime (Minutes) Genres Region Average Rating Number of Votes
0 tt0063540 Sunghursh 2013 175.0 Action,Crime,Drama IN 7.0 77.0
1 tt0063540 Sunghursh 2013 175.0 Action,Crime,Drama IN 7.0 77.0
2 tt0063540 Sunghursh 2013 175.0 Action,Crime,Drama Unknown 7.0 77.0
3 tt0063540 Sunghursh 2013 175.0 Action,Crime,Drama IN 7.0 77.0
4 tt0063540 Sunghursh 2013 175.0 Action,Crime,Drama IN 7.0 77.0
Check Cleaned Data
df_im_db.info()
<class 'pandas.core.frame.DataFrame'>
Int64Index: 355545 entries, 0 to 355544
Data columns (total 8 columns):

# Column Non-Null Count Dtype

---

0 Movie ID 355545 non-null object
1 Primary Title 355545 non-null object
2 Start Year 355545 non-null int64  
 3 Runtime (Minutes) 355545 non-null float64
4 Genres 355545 non-null object
5 Region 355545 non-null object
6 Average Rating 355545 non-null float64
7 Number of Votes 355545 non-null float64
dtypes: float64(3), int64(1), object(4)
memory usage: 24.4+ MB
Handling Outliers
Detecting Outliers in Runtime (Minutes)
​

# Set the figure size

plt.figure(figsize=(16, 10))
​

# Create a boxplot for the "Runtime (Minutes)" column

sns.boxplot(x=df_im_db["Runtime (Minutes)"], color='skyblue')
​

# Set title and labels

plt.title('Detecting Outliers in Runtime (Minutes)', fontweight="bold", fontsize=16)
plt.xlabel('Runtime (Minutes)', fontweight="bold", fontsize=14)
​

# Show the plot

plt.show()
​

From this plot, we observe the presence of extreme outliers. However, considering that most movies typically run for around 90 minutes, with some exceptions extending up to 360 minutes, and some good movies running for 65 minutes, we will filter out the movies that run for more than 360 minutes and less than 65 minutes.

# Filter out movies with a runtime of less than 65 minutes and more than 360 minutes

df_im_db = df_im_db[(df_im_db["Runtime (Minutes)"] >= 65) & (df_im_db['Runtime (Minutes)'] <= 360)]
​

# Set the figure size

plt.figure(figsize=(16, 10))
​

# Create a boxplot for the "Runtime (Minutes)" column

sns.boxplot(x=df_im_db['Runtime (Minutes)'], color='skyblue')
​

# Set title and labels

plt.title('After Removing Outliers in Runtime (Minutes)', fontweight="bold", fontsize=16)
plt.xlabel('Runtime (Minutes)', fontweight="bold", fontsize=14)
​

# Show the plot

plt.show()
​

We still have outliers within this range (65minutes - 360minutes), but these outliers fall within acceptable limits

#### Detecting Outliers in Start Years Columns

​

# Set the figure size

plt.figure(figsize=(16, 10))
​

# Create a boxplot for the "Years" column

sns.boxplot(x=df_im_db['Start Year'], color='skyblue')
​

# Set title and labels

plt.title('Outliers in Years', fontweight="bold", fontsize=16)
plt.xlabel('Movies Release Year', fontweight="bold", fontsize=14)
​

# Show the plot

plt.show()

There are movies with start years greater than 2024, which is a possibility because some movie productions announce movie start years ahead in some cases. However, in this analysis, movie release years that are greater than 2024 will be filtered out because they might interfere with data analysis, such as movie ratings and other data.
​

#### DFiltering years greater than 2024

import seaborn as sns
import matplotlib.pyplot as plt
df_im_db = df_im_db[df_im_db['Start Year'] <= 2024]

# Set the figure size

plt.figure(figsize=(16, 10))
​

# Create a boxplot for the "Years" column

sns.boxplot(x=df_im_db['Start Year'], color='skyblue')
​

# Set title and labels

plt.title('After Removing Outliers in Years', fontweight="bold", fontsize=16)
plt.xlabel('Movies Release Year', fontweight="bold", fontsize=14)
​

# Show the plot

plt.show()
​
​

Genre Distribution - Genres with Highest Number of Movies in the Industry
genre_distribution = df_im_db['Genres'].value_counts()
genre_distribution
Drama 46805
Documentary 34786
Comedy 18751
Comedy,Drama 11746
Drama,Romance 7878
...  
Music,Musical,Thriller 1
Comedy,Music,Mystery 1
Family,Sci-Fi,Thriller 1
Musical,Romance,Western 1
Horror,Musical,Thriller 1
Name: Genres, Length: 1039, dtype: int64
​
​

# Get the value counts of genres

genre_distribution = df_im_db['Genres'].value_counts()
​

# Select the top ten genres

top_ten_genres = genre_distribution.head(10)
​

# Create custom formatter for y-axis labels

def custom_formatter(x, pos):
if x == 0:
return str(int(x))
elif x < 1000:
return f'{int(x)}'
else:
return f'{int(x/1000)}K'
​

# Plot the graph

plt.figure(figsize=(12, 10))
top_ten_genres.plot(kind='bar', color='navy', linewidth=1.5, label='Movie Genres')
plt.title('Genres with Highest Number of Movies in Movie Industry', fontsize=22, fontweight='bold') # Increase title font size
plt.xlabel('Movie Genres', fontsize=18, fontweight='bold') # Increase x-axis label font size
plt.ylabel('Number of Movies Per Genre Combination', fontsize=18, fontweight='bold') # Increase y-axis label font size
plt.xticks(rotation=45, ha='right', fontsize=14, fontweight='bold') # Increase x-axis tick label font size
plt.yticks(fontsize=14, fontweight='bold') # Increase y-axis tick label font size
plt.gca().yaxis.set_major_formatter(FuncFormatter(custom_formatter)) # Set custom formatter for y-axis labels
plt.grid(False)
plt.legend(fontsize=16) # Increase legend font size
plt.tight_layout() # Adjust layout to prevent clipping of labels
plt.show()
​

Based on the data analysis, it's evident that the most popular genres in the movie industry are Drama, Documentary, and Comedy.
Possibly these genres consistently attract a significant audience and have proven to be lucrative investments.
Rating Distribution by Combination of Genre
df_im_db.columns
Index(['Movie ID', 'Primary Title', 'Start Year', 'Runtime (Minutes)',
'Genres', 'Region', 'Average Rating', 'Number of Votes'],
dtype='object')
​

# Group the data by genre and calculate the mean rating

rating_by_genre = df_im_db.groupby('Genres')['Average Rating'].mean().sort_values(ascending=False)
​

# Filter the top ten genres with the highest ratings

top_genres = rating_by_genre.head(10)
​

# Set the style

sns.set_style("whitegrid")
​

# Create the bar plot for the top ten genres

plt.figure(figsize=(16, 7))

# Use seaborn barplot to obtain the bar positions

sns_barplot = sns.barplot(x=top_genres.index, y=top_genres.values, color="navy")

# Extract the bar positions from the barplot

bar_positions = [bar.get_x() + bar.get_width() / 2 for bar in sns_barplot.patches]

# Add custom xticks with the adjusted positions

plt.xticks(ticks=bar_positions, labels=top_genres.index, rotation=45, ha='right', fontweight="bold", fontsize=12)
​

# Set title and labels

plt.title('Top Ten Movie Genres by Average Rating', fontweight="bold", fontsize=16)
plt.xlabel('Movie Genre', fontweight="bold", fontsize=16)
plt.ylabel('Average Movie Rating', fontweight="bold", fontsize=16)
​
plt.show()

Movies with the highest ratings encompass genres such as Music, Mystery, Comedy, Drama, Reality TV, Action, Adventure, and Musical.
It's intriguing that despite Music and Mystery being part of this list, they aren't the most frequently produced genres in the industry as observed earlier.
Vote Distribution by Genre
df_im_db.columns
Index(['Movie ID', 'Primary Title', 'Start Year', 'Runtime (Minutes)',
'Genres', 'Region', 'Average Rating', 'Number of Votes'],
dtype='object')
​
from matplotlib.ticker import FixedLocator
​

# Assuming vote_by_genre contains the sum of votes grouped by genre

vote_by_genre = df_im_db.groupby('Genres')['Number of Votes'].sum()
top_most_voted_genres = vote_by_genre.head()
​

# Plotting

plt.figure(figsize=(16, 8))
ax = top_most_voted_genres.sort_values().plot(kind='barh', color='skyblue')
plt.title('Vote Distribution by Genre', fontsize=18, fontweight='bold')
plt.xlabel('Total Votes Per Genre', fontsize=16, fontweight='bold')
plt.ylabel('Movie Genres', fontsize=16, fontweight='bold')
plt.xticks(fontsize=14, fontweight='bold')
plt.yticks(fontsize=14, fontweight='bold')
plt.grid(False)
​

# Formatting x-axis ticks

xticks = ax.get_xticks()
xtick_labels = [f"{int(val/1000)}k" for val in xticks]
ax.xaxis.set_major_locator(FixedLocator(xticks))
ax.set_xticklabels(xtick_labels)
​
plt.tight_layout()
plt.show()

Action, Adventure, and Animation genres received the highest number of votes" indicates that these three genres are the most popular or preferred among the audience, based on the voting data.
Correlation between Ratings and Votes
correlation = df_im_db['Average Rating'].corr(df_im_db['Number of Votes'])
print("Correlation between Ratings and Votes:", correlation)
Correlation between Ratings and Votes: 0.18749080047799094
0.187: This value indicates a weak positive correlation between the ratings and the number of votes. While there is a tendency for movies with higher ratings to receive more votes, the relationship is not very strong.
Genre Popularity Over Time

# Assuming you have a 'Year' column in your dataset

genre_popularity_over_time = df_im_db.groupby(['Start Year', 'Genres']).size().unstack(fill_value=0)
genre_popularity_over_time
Genres Action Action,Adult,Comedy Action,Adventure Action,Adventure,Animation Action,Adventure,Biography Action,Adventure,Comedy Action,Adventure,Crime Action,Adventure,Documentary Action,Adventure,Drama Action,Adventure,Family ... Sport Sport,Thriller Talk-Show Thriller Thriller,War Thriller,Western Unknown War War,Western Western
Start Year
2010 248 0 34 114 0 102 34 6 265 81 ... 33 0 5 356 19 6 423 26 0 11
2011 345 0 45 173 15 122 42 8 161 3 ... 41 0 3 338 0 0 478 16 0 27
2012 271 3 13 152 2 180 76 14 232 4 ... 35 0 4 453 0 0 386 23 0 22
2013 337 0 48 97 2 196 26 18 207 10 ... 41 0 4 485 0 12 377 19 0 12
2014 357 0 80 225 18 262 35 17 315 57 ... 39 0 2 509 0 0 466 12 1 15
2015 353 0 18 211 107 226 120 18 233 64 ... 23 0 11 540 1 0 699 31 0 24
2016 354 3 18 208 2 358 72 15 337 29 ... 36 0 6 632 0 0 1028 18 0 35
2017 454 0 41 154 35 309 77 8 178 16 ... 31 5 0 647 0 1 829 16 0 39
2018 408 0 33 213 35 223 31 15 111 18 ... 28 0 3 835 1 0 687 31 0 31
2019 239 0 8 150 3 159 27 1 18 29 ... 13 0 5 491 0 0 367 21 0 12
2020 48 0 7 1 1 7 16 0 7 16 ... 0 0 0 66 0 0 42 1 0 5
2021 6 0 4 8 0 1 8 0 5 0 ... 0 0 0 1 0 0 0 0 0 1
2022 5 0 0 0 0 0 0 10 0 0 ... 0 0 0 0 0 0 9 0 0 0
2023 1 0 0 0 0 0 0 0 5 0 ... 0 0 0 0 0 0 2 0 0 0
2024 0 0 0 0 0 0 0 0 0 0 ... 0 0 0 0 0 0 1 0 0 0
15 rows × 1039 columns

6 Exploratory Data Analysis and Visualization on data from rt.movie_info.tsv.gz dataset

# Display the first few rows of the DataFrame

df_movie_info.head(5)
id synopsis rating genre director writer theater_date dvd_date currency box_office runtime studio
0 1 This gritty, fast-paced, and innovative police... R Action and Adventure|Classics|Drama William Friedkin Ernest Tidyman Oct 9, 1971 Sep 25, 2001 NaN NaN 104 minutes NaN
1 3 New York City, not-too-distant-future: Eric Pa... R Drama|Science Fiction and Fantasy David Cronenberg David Cronenberg|Don DeLillo Aug 17, 2012 Jan 1, 2013 $ 600,000 108 minutes Entertainment One
2 5 Illeana Douglas delivers a superb performance ... R Drama|Musical and Performing Arts Allison Anders Allison Anders Sep 13, 1996 Apr 18, 2000 NaN NaN 116 minutes NaN
3 6 Michael Douglas runs afoul of a treacherous su... R Drama|Mystery and Suspense Barry Levinson Paul Attanasio|Michael Crichton Dec 9, 1994 Aug 27, 1997 NaN NaN 128 minutes NaN
4 7 NaN NR Drama|Romance Rodney Bennett Giles Cooper NaN NaN NaN NaN 200 minutes NaN

# Print the informational summary of the DataFrame.

df_movie_info.info()
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 1560 entries, 0 to 1559
Data columns (total 12 columns):

# Column Non-Null Count Dtype

---

0 id 1560 non-null int64
1 synopsis 1498 non-null object
2 rating 1557 non-null object
3 genre 1552 non-null object
4 director 1361 non-null object
5 writer 1111 non-null object
6 theater_date 1201 non-null object
7 dvd_date 1201 non-null object
8 currency 340 non-null object
9 box_office 340 non-null object
10 runtime 1530 non-null object
11 studio 494 non-null object
dtypes: int64(1), object(11)
memory usage: 146.4+ KB
From this dataset, we are interested in two columns: genre and rating.
Both genre and rating columns have missing data
Remove duplicates before filtering out columns

# Check for duplicates

duplicates = df_movie_info.duplicated()
print(f'Number of duplicate rows: {duplicates.sum()}')
Number of duplicate rows: 0

# Filtered out columns not required

df_movie_info_Filtered = df_movie_info[['genre', 'rating']]
df_movie_info.head()
id synopsis rating genre director writer theater_date dvd_date currency box_office runtime studio
0 1 This gritty, fast-paced, and innovative police... R Action and Adventure|Classics|Drama William Friedkin Ernest Tidyman Oct 9, 1971 Sep 25, 2001 NaN NaN 104 minutes NaN
1 3 New York City, not-too-distant-future: Eric Pa... R Drama|Science Fiction and Fantasy David Cronenberg David Cronenberg|Don DeLillo Aug 17, 2012 Jan 1, 2013 $ 600,000 108 minutes Entertainment One
2 5 Illeana Douglas delivers a superb performance ... R Drama|Musical and Performing Arts Allison Anders Allison Anders Sep 13, 1996 Apr 18, 2000 NaN NaN 116 minutes NaN
3 6 Michael Douglas runs afoul of a treacherous su... R Drama|Mystery and Suspense Barry Levinson Paul Attanasio|Michael Crichton Dec 9, 1994 Aug 27, 1997 NaN NaN 128 minutes NaN
4 7 NaN NR Drama|Romance Rodney Bennett Giles Cooper NaN NaN NaN NaN 200 minutes NaN
Stistical Summary
df_movie_info_Filtered .describe(include=['O'])
genre rating
count 1552 1557
unique 299 6
top Drama R
freq 151 521
There 6 Unique rating categories
Most Frequent Movie Genre is Drama
Handle Missing Values
df_movie_info_Filtered .info()
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 1560 entries, 0 to 1559
Data columns (total 2 columns):

# Column Non-Null Count Dtype

---

0 genre 1552 non-null object
1 rating 1557 non-null object
dtypes: object(2)
memory usage: 24.5+ KB

# Fill missing values in the 'rating' column with 'NR'

df_movie_info_Filtered.loc[:, 'rating'].fillna('NR', inplace=True)
​

# Fill missing values in the 'genre' column with 'Unknown'

df_movie_info_Filtered.loc[:, 'genre'].fillna('Unknown', inplace=True)
​
C:\Users\Mercy\anaconda3\envs\learn-env\lib\site-packages\pandas\core\series.py:4517: SettingWithCopyWarning:
A value is trying to be set on a copy of a slice from a DataFrame

See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
return super().fillna(

# Verify the changes

print(df_movie_info_Filtered.isnull().sum())
genre 0
rating 0
dtype: int64

# Splitting genres into individual genres

df_movie_info_Filtered.loc[:, 'genre_list'] = df_movie_info_Filtered['genre'].apply(lambda x: x.split('|'))
C:\Users\Mercy\anaconda3\envs\learn-env\lib\site-packages\pandas\core\indexing.py:1596: SettingWithCopyWarning:
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
self.obj[key] = \_infer_fill_value(value)
C:\Users\Mercy\anaconda3\envs\learn-env\lib\site-packages\pandas\core\indexing.py:1745: SettingWithCopyWarning:
A value is trying to be set on a copy of a slice from a DataFrame.
Try using .loc[row_indexer,col_indexer] = value instead

See the caveats in the documentation: https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
isetter(ilocs[0], value)
​

# Distribution of genres

genre_counts = df_movie_info_Filtered['genre_list'].explode().value_counts()
genre_counts
Drama 912
Comedy 550
Action and Adventure 366
Mystery and Suspense 309
Art House and International 265
Romance 198
Classics 193
Science Fiction and Fantasy 172
Horror 134
Kids and Family 99
Musical and Performing Arts 98
Documentary 69
Special Interest 61
Western 48
Animation 47
Television 23
Faith and Spirituality 11
Sports and Fitness 10
Unknown 8
Cult Movies 4
Gay and Lesbian 2
Anime and Manga 2
Name: genre_list, dtype: int64

# Distribution of ratings

rating_counts = df_movie_info_Filtered['rating'].value_counts()
rating_counts
R 521
NR 506
PG 240
PG-13 235
G 57
NC17 1
Name: rating, dtype: int64
​

# Plotting distribution of ratings

plt.figure(figsize=(16, 8)) # Adjust the figure size for better visualization
plt.bar(rating_counts.index, rating_counts.values, color='navy') # Adjust the color of the bars to navy blue
plt.xlabel('Movie Rating', fontsize=16, fontweight='bold') # Adjust label font size
plt.ylabel('Number of Movies', fontsize=16, fontweight='bold') # Adjust label font size
plt.title('Distribution of Movie Ratings', fontsize=18, fontweight='bold') # Adjust title font size and style
plt.grid(False) # Remove Grid
plt.xticks(fontsize=12, fontweight='bold') # Adjust x-axis tick font size
plt.yticks(fontsize=12, fontweight='bold') # Adjust y-axis tick font size
plt.tight_layout() # Adjust layout to prevent labels from being cut off
plt.show()

In the dataset, R-rated movies were most prevalent, closely followed by Not Rated movies.
PG and PG-13 movies had similar frequencies.
G-rated movies were less common, and NC-17 received only one rating.

# Popular genre-rating combinations

genre_rating_counts = df_movie_info_Filtered.explode('genre_list').groupby(['genre_list', 'rating']).size()
genre_rating_counts
genre_list rating
Action and Adventure G 13
NR 92
PG 79
PG-13 67
R 115
...
Western G 3
NR 24
PG 6
PG-13 6
R 9
Length: 95, dtype: int64
The most prevalent genre-rating combination is Action and Adventure with a G rating, closely followed by NR and PG ratings.

# Load the TSV file into a DataFrame

df_reviews = pd.read_csv(r'./zippedData/rt.reviews.tsv.gz', compression='gzip', sep='\t', encoding="latin-1")
​

# Display the first few rows of the DataFrame

df_reviews.head()
id review rating fresh critic top_critic publisher date
0 3 A distinctly gallows take on contemporary fina... 3/5 fresh PJ Nabarro 0 Patrick Nabarro November 10, 2018
1 3 It's an allegory in search of a meaning that n... NaN rotten Annalee Newitz 0 io9.com May 23, 2018
2 3 ... life lived in a bubble in financial dealin... NaN fresh Sean Axmaker 0 Stream on Demand January 4, 2018
3 3 Continuing along a line introduced in last yea... NaN fresh Daniel Kasman 0 MUBI November 16, 2017
4 3 ... a perverse twist on neorealism... NaN fresh NaN 0 Cinema Scope October 12, 2017

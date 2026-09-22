# Netflix Business Case Study — Exploratory Data Analysis

> **A Python-based exploratory and business analysis of Netflix's Movies and TV Shows catalogue.**

## Project Overview

This project analyzes the Netflix content catalogue using **Python, Pandas, NumPy, Matplotlib, and Seaborn**.

The objective is to understand the composition and evolution of Netflix's content library and identify patterns across **content type, release year, ratings, countries, actors, directors, and content growth**.

The analysis combines **data cleaning, preprocessing, non-graphical analysis, exploratory data analysis (EDA), data visualization, and business insights** to understand Netflix's content strategy.


## 🎯 Business Problem

Netflix has a large and diverse content catalogue consisting of Movies and TV Shows from different countries and production industries.

This analysis attempts to answer questions such as:

* What is the distribution of Movies vs TV Shows?
* How has Netflix's content catalogue evolved over time?
* Which content ratings are most common?
* Which countries contribute the most content?
* Which actors and directors appear most frequently?
* When are TV Shows most frequently added to Netflix?
* How has the growth of TV Shows compared with Movies?
* What business insights can be derived from these patterns?

## Tech Stack

| Tool / Library       - Purpose                        |

| **Python**           - Programming and analysis       |
| **Pandas**           - Data manipulation and analysis |
| **NumPy**            - Numerical operations           |
| **Matplotlib**       - Data visualization             |
| **Seaborn**          - Statistical visualization      |
| **Jupyter Notebook** - Interactive analysis           |

## Dataset

The dataset contains:

* **8,807 records**
* **12 columns**

Each record represents a Movie or TV Show available on Netflix.

### Key columns

| Column         - Description                                 |

| `show_id`      - Unique identifier                           |
| `type`         - Movie or TV Show                            |
| `title`        - Title of the content                        |
| `director`     - Director(s)                                 |
| `cast`         - Cast members                                |
| `country`      - Country/countries associated with the title |
| `date_added`   - Date the title was added to Netflix         |
| `release_year` - Original release year                       |
| `rating`       - Content rating                              |
| `duration`     - Movie duration or number of TV Show seasons |
| `listed_in`    - Genre/category                              |
| `description`  - Content description                         |


## Analysis Workflow

The project follows the following data-analysis workflow:

Raw Dataset
     ↓
Data Understanding
     ↓
Data Type Conversion
     ↓
Missing Value Analysis
     ↓
Duplicate Detection
     ↓
Data Preprocessing
     ↓
Data Unnesting
     ↓
Non-Graphical Analysis
     ↓
Exploratory Data Analysis
     ↓
Data Visualization
     ↓
Business Insights
     ↓
Recommendations

## Data Cleaning & Preprocessing

The notebook performs several preprocessing steps.

### Data Type Conversion

The following columns were converted to categorical data types:

* `type`
* `rating`

### Missing Value Analysis

Missing values were identified in several columns.

The largest number of missing values were found in:

* `director`
* `country`
* `cast`

Missing values in these fields were subsequently represented as: Unknown


### Duplicate Check

The dataset was checked for duplicate records.

### Data Unnesting

Several columns contain multiple values separated by commas.

The notebook separates these values into individual rows for more detailed analysis.

Unnested fields include:

* Country
* Genre
* Cast
* Director

This makes it possible to analyze individual countries, actors, directors, and genres independently.


# Exploratory Data Analysis

## 1. Movies vs TV Shows

Movies make up the majority of Netflix's catalogue.

| Content Type = Count |

| Movies       - 6,131 |
| TV Shows     - 2,676 |

Approximately **70% of the catalogue consists of Movies**, while around **30% consists of TV Shows**.

This indicates that Movies remain the dominant content type in the dataset.



## 2. Movie Release Trends

The analysis examines Movies released from **1990 to 2021**.

The number of movie releases increased substantially from around 2013 onward, with **2017 and 2018 reaching 767 releases each** in the dataset.

The analysis also shows a decline toward 2020–2021.



## 3. TV Show Launch Timing

The notebook analyzes the months in which TV Shows were added to Netflix.

The highest counts include:

| Month     - TV Shows Added |

| December  -            266 |
| July      -            262 |
| September -            251 |
| August    -            236 |

This shows a concentration of TV Show additions during several periods of the year, particularly toward the middle and latter part of the year.



## 4. Content Distribution by Country

The analysis compares Movies and TV Shows across countries.

The **United States** has the largest representation in the dataset, followed by **India and the United Kingdom**.

The analysis also identifies differences between countries in terms of their Movie and TV Show mix.

For example:

* The United States has substantially more Movies than TV Shows.
* India has a particularly strong Movie presence.
* Japan and South Korea show a relatively stronger TV Show presence compared with many other countries.



## 5. Actors & Directors

The project analyzes the most frequently appearing actors and directors after separating multi-value fields.

### Top Movie Actors

* Anupam Kher
* Shah Rukh Khan
* Naseeruddin Shah

### Top TV Show Actors

* Takahiro Sakurai
* Yuki Kaji
* Ai Kayano

### Frequently Appearing Movie Directors

* Rajiv Chilaka
* Jan Suter
* Raúl Campos

These results highlight the importance of Indian cinema and Japanese TV/anime content within the dataset.



# Visual Analysis

The notebook uses several visualization techniques.

### Univariate Analysis

* Content rating countplot
* Release-year histogram
* Release-year distribution with KDE

### Bivariate Analysis

* Release year vs content type boxplot
* Movie vs TV Show comparison
* Movie and TV Show release trends

### Visualizations Used

```text
Countplots
Histograms
KDE Distribution
Boxplots
Categorical Comparisons
Time-based Comparisons
```


# Key Findings

### 1. Movies dominate the catalogue

Netflix has considerably more Movies than TV Shows in the analyzed dataset.

### 2. TV Shows have grown rapidly

Although Movies remain more numerous, the analysis shows significant growth in TV Shows, particularly after 2015.

### 3. Recent content dominates

A large concentration of titles has release years between **2015 and 2021**, showing the strong representation of modern content.

### 4. TV-MA is the most common rating

The analysis identifies **TV-MA** as the most common content rating, followed by **TV-14**.

### 5. The United States leads content representation

The United States has the largest number of titles associated with it, followed by India and the United Kingdom.

### 6. International content is significant

The dataset contains substantial representation from international markets, particularly India, Japan, and South Korea.


# Business Insights

The analysis suggests several observations about Netflix's content catalogue:

* Movies continue to represent the largest portion of the catalogue.
* TV Shows have experienced substantial growth in recent years.
* Netflix's catalogue has a strong representation of modern content.
* Mature-audience content represents a significant portion of the catalogue.
* International content is an important component of Netflix's content strategy.
* Country-level content patterns differ significantly.
* Multi-season TV content can play an important role in sustained viewer engagement.



#  Business Recommendations

Based on the analysis performed in the notebook:

### 1. Continue investing in TV Shows

The rapid growth of TV Shows suggests continued investment in episodic content could be valuable.

### 2. Expand regional content

Developing regional-language content can help Netflix strengthen its presence in markets such as:

* India
* South Korea
* Japan
* Other emerging markets

### 3. Strengthen popular genres

The analysis supports continued attention to major catalogue categories such as:

* Drama
* Comedy
* Thriller
* International content

### 4. Broaden audience segments

Increasing family-friendly and children's programming could help diversify the audience represented by the catalogue.

### 5. Consider release timing

The observed concentration of TV Show additions in certain months can be considered when planning future content releases.

### 6. Develop talent partnerships

Long-term partnerships with successful actors and directors, alongside new talent development, could support continued content production.

### 7. Use country-specific strategies

The differences between countries suggest that a localized content strategy may be more appropriate than applying one global content strategy to every market.

### 8. Invest in multi-season content

Multi-season TV Shows can support continued engagement by encouraging viewers to return for additional episodes and seasons.




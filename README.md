# Social Network Analysis of the Boston Bombings

This project analyzes Twitter activity related to the **2013 Boston Marathon bombings** using social network analysis. The goal is to explore how crisis-related information spread online, which accounts or topics became important, and how communication changed during the event.

The project was completed as part of an **Introduction to Social Network Analysis** course.

## Dataset

The analysis uses data from **CrisisLexT26**, a collection of tweets from 26 crisis events that occurred between 2012 and 2013.

For this project, the **2013 Boston Bombings** dataset was selected.

Dataset source: [CrisisLex](https://crisislex.org/data-collections.html)

The repository also contains timestamp data used to study how the network changed throughout the crisis.

## What the project does

The analysis is implemented in `Project_3v2.ipynb` and includes:

* Cleaning and preprocessing tweet text
* Removing non-English tweets, URLs, emojis, stopwords, and duplicates
* Extracting mentions, retweets, replies, and hashtags
* Building a directed interaction network
* Building a hashtag co-occurrence network
* Calculating degree, closeness, betweenness, and eigenvector centrality
* Identifying important users and hashtags
* Detecting communities using the Louvain algorithm
* Studying network activity in 12-hour time windows
* Performing sentiment analysis with VADER
* Tracking trending hashtags during the crisis
* Visualizing network structures and changes over time

Because the available CrisisLex data does not provide the original user ID for every tweet, the interaction network uses tweet IDs as source nodes and mentioned or retweeted Twitter handles as target nodes.

## Technologies

The project is written in Python using mainly:

* `pandas`
* `NetworkX`
* `matplotlib`
* `NLTK`
* `spaCy`
* `langdetect`
* `emoji`
* `powerlaw`

## Running the project

Clone the repository:

```bash
git clone https://github.com/lpl2302/Analysis-on-Boston-Bombings.git
cd Analysis-on-Boston-Bombings
```

Install the required Python packages:

```bash
pip install pandas networkx matplotlib nltk spacy langdetect emoji powerlaw
python -m spacy download en_core_web_sm
```

Then open:

```text
Project_3v2.ipynb
```

in Jupyter Notebook or JupyterLab and run the cells in order.

## Repository structure

```text
Analysis-on-Boston-Bombings/
│
├── Project_3v2.ipynb
├── CrisisLexT26-v1.0/
├── 2013_Boston_bombings-tweetids_entire_period.csv
│
├── cleaned_tweets.csv
├── cleaned_with_timestamp.csv
├── user_interactions.csv
├── hashtag_usage.csv
├── hashtag_centrality.csv
├── extracted_tweets.csv
│
└── README.md
```

The additional CSV files are intermediate or processed datasets produced during the analysis.

## Goal

The project demonstrates how social network analysis can be used to better understand communication during a crisis, including the structure of online interactions, influential actors and topics, community formation, sentiment, and how these patterns evolve over time.

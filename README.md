# DS-scraping
## Scraping assignment for Intro to Data Science*

Because the main Twitter accounts for most major news outlets include all types of
content (including sports, style, etc.), not just “hard news,” I only wanted to examine
accounts from news organizations that used separate accounts dedicated to specific
verticals. I therefore examined Twitter accounts from two national news organizations,
the Wall Street Journal and the Washington Post. Within these two organizations, I
focused on “hard news” verticals such as breaking news, politics, economics, local and
regional news, national news, and foreign affairs.

Using the methods Pablo Barberá created to scrape tweets, I saved 500 tweets from each of
the following accounts using R:

Source | URL
----- | -----
1. @postworldnews | http://twitter.com/postworldnews
2. @wpinvestigates | http://twitter.com/wpinvestigates
3. @postlocal | http://twitter.com/postlocal
4. @WSJmarkets | http://twitter.com/WSJmarkets
5. @WSJbreakingnews | http://twitter.com/WSJbreakingnews
6. @washpostbiz | http://twitter.com/washpostbiz
7. @WSJbusiness | http://twitter.com/WSJbusiness
8. @WSJPolitics | http://twitter.com/WSJPolitics
9. @GovBeat | http://twitter.com/GovBeat
10. @postpolitics | http://twitter.com/postpolitics

The JSON files containing the individual and merged tweets are available in the "data"
folder: https://github.com/kz55/DS-scraping/tree/master/data

## Results

### Individual results

Using Barberá's methods and lexicon for basic sentiment analysis, I found each source to
have the following sentiment levels (n=500 for each):

Source | @TwitterName| Focus | % Positive | % Neutral | % Negative
----- | ----- | ----- | ----- | ----- | -----
Washington Post | @postworldnews | International | 17 | 45 | 38
Washington Post | @wpinvestigates | Investigative | 17 | 49 | 34
Washington Post | @postlocal | Local | 17 | 52 | 31
Wall Street Journal | @WSJmarkets | Business/Finance | 26 | 47 | 27
Wall Street Journal | @WSJbreakingnews | Breaking news | 25 | 50 | 25
Washington Post | @washpostbiz | Business/Finance | 26 | 52 | 22
Wall Street Journal | @WSJbusiness | Business/Finance | 25 | 53 | 22
Wall Street Journal | @WSJPolitics | Politics/Government | 31 | 47 | 22
Washington Post | @GovBeat | Politics/Government | 24 | 57 | 19
Washington Post | @postpolitics | Politics/Government | 25 | 56 | 19

[[CSV file](https://github.com/kz55/DS-scraping/blob/master/CSV%20results/indiv_results.csv)]

These results are illustrated in the output_individual.png file, created in R:

![Individual results](https://github.com/kz55/DS-scraping/blob/master/output_individual.png)

### Aggregate results

For all 5000 tweets, the overall sentiment levels are:

Source | % Positive | % Neutral | % Negative
----- | ----- | ----- | -----
Total (n=5000) | 23 | 51 | 26

[[CSV file](https://github.com/kz55/DS-scraping/blob/master/data/total_results.csv)]

This output is illustrated in the output_total.png file, created in R:

![Total results](https://github.com/kz55/DS-scraping/blob/master/output_total.png)

## Analysis


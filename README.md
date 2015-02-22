# DS-scraping
*Scraping assignment for Intro to Data Science*

Because the main Twitter accounts for most major news outlets include all types of
content (including sports, style, etc.), not just “hard news,” I only wanted to examine
accounts from news organizations that used separate accounts dedicated to specific
verticals. I therefore examined Twitter accounts from two national news organizations,
the Wall Street Journal and the Washington Post. Within these two organizations, I
focused on “hard news” verticals such as breaking news, politics, economics, local and
regional news, national news, and foreign affairs.

Using the methods Pablo Barberá created to scrape tweets, I saved 500 tweets from each of
the following accounts:

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

*Individual results*

Using Barberá's methods and lexicon for basic sentiment analysis, I found each source to
have the following sentiment levels:

Source | Positive | Neutral | Negative
----- | ----- | ----- | -----
1 | postworldnews | 17 | 45 | 38
2 | wpinvestigates | 17 | 49 | 34
3 | postlocal | 17 | 52 | 31
4 | WSJmarkets | 26 | 47 | 27
5 | WSJbreakingnews | 25 | 50 | 25
6 | washpostbiz | 26 | 52 | 22
7 | WSJbusiness | 25 | 53 | 22
8 | WSJPolitics | 31 | 47 | 22
9 | GovBeat | 24 | 57 | 19
10 | postpolitics | 25 | 56 | 19

These results are illustrated in the output_individual.png file.

*Aggregate results*

For all 5000 tweets, the overall sentiment levels are:

Source | Positive | Neutral | Negative
----- | ----- | ----- | -----
Total (n=5000) | 23% | 51% | 26%

This output is illustrated in the output_total.png file.
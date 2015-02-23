# DS-scraping
## Scraping assignment for Intro to Data Science*

Because the main Twitter accounts for most major news outlets include all types of
content (including sports, style, etc.), not just “hard news,” I only wanted to examine
accounts from news organizations that used separate accounts dedicated to specific
verticals. I therefore examined Twitter accounts from two national news organizations,
the Wall Street Journal and the Washington Post. Within these two organizations, I
focused on “hard news” verticals such as breaking news, politics, economics, local and
regional news, national news, and foreign affairs. The script is available [here](https://github.com/kz55/DS-scraping/blob/master/twitter_scraping_and_analysis).

Using the methods from Pablo Barberá's [social media workshop](https://github.com/pablobarbera/social-media-workshop) to scrape tweets, I saved
500 tweets from each of the following accounts using R:

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

Note:The files needed for Barbera’s scripts, functions.r and lexicon.csv, are available
[in the “files” folder](https://github.com/kz55/DS-scraping/tree/master/files), along with the generated oauth_token.

The [CSV](https://github.com/kz55/DS-scraping/tree/master/CSV%20results/tweets) and [JSON](https://github.com/kz55/DS-scraping/tree/master/JSON%20tweets) files containing the individual and merged tweets are also available.

## Results

### Individual results

Using Barberá's methods and [lexicon](https://github.com/kz55/DS-scraping/blob/master/files/lexicon.csv) for basic sentiment analysis, I found each source to
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

**Analysis**: As the table above shows, the accounts with the lowest proportions of
positive tweets (and the highest proportions of negative tweets) are from the verticals
devoted to international, investigative, or local news. For instance, the @postworldnews
account's tweets were 17% positive, 45% neutral, and 38% negative. Meanwhile, the least
negative accounts were all politics- or government-focused accounts, such as the
Washington Post's @GovBeat and @postpolitics accounts.

These results are illustrated in the output_individual.png file, created in R:

![Individual results](https://github.com/kz55/DS-scraping/blob/master/output_individual.png)

**Limitations**: Because I chose to only look at tweets from two main news outlets, it's
unclear whether these findings would apply to a broader array of news organizations'
accounts, even those devoted to similar "hard news" topics.

### Aggregate results

For all 5000 tweets, the overall sentiment levels are:

Source | % Positive | % Neutral | % Negative
----- | ----- | ----- | -----
Total (n=5000) | 23 | 51 | 26

This output is illustrated in the output_total.png file, created in R, which shows
the total number of tweets in each category:

![Total results](https://github.com/kz55/DS-scraping/blob/master/output_total.png)

## Conclusion

Based on an analysis of 5000 tweets from 10 dedicated "hard news" Twitter accounts, the
news appears to be slightly more "negative" than "positive", but not substantially so.
Perhaps surprisingly, it appears that accounts dealing with politics and government are
less "negative" than other types of hard news accounts such as local or international 
news, although our sample was far too small to make any claims beyond these 10 accounts.

In addition, it is possible that the lexicon used was not well suited to the specialized
types of language that is used in discussions of business/finance, politics, and other
types of "hard news". Additional analysis would be needed to examine how relevant the
lexicon was and whether there were any major terms that were not included which might
have biased the results.

Finally, these results are from a particular moment in time (the afternoon of Saturday,
February 22, 2015), and due to the real-time nature of Twitter, any recent news events
that were particularly  "positive" or "negative" might have affected the results for
this (non-random) sample.
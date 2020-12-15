# Module 1 Final Project - Movie Studio Recommendations

For: Microsoft Inc.

By: Jenny Wadkins

## Introduction

>Microsoft sees all the big companies creating original video content, and they want to get in on the fun. They have decided to create a new movie studio, but the problem is they don’t know anything about creating movies. They have hired you to help them better understand the movie industry. Your team is charged with doing data analysis and creating a presentation that explores what type of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the CEO can use when deciding what type of films they should be creating.

## Questions

* Should Microsoft focus on launching a franchise, or focus on single film IPs?
* What audience should the company aim for (based on MPAA rating)?
* What genre(s) should the company aim for?
* What combination of genre, franchise and rating will result in the lowest risk?
* What, if any, genres/ratings/franchises should be avoided?

## Methodology
* Source data using a combination of API calls and web scraping
* Clean and organize data
* Perform exploratory data analysis
* Provide conclusions based on analysis

## Table of Contents

#### [student.ipynb](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/student.ipynb)

> Notebook Preparation
* Recommended Extensions
* Importing our Modules
* Notebook-wide Functions

> Data Acquisition and Cleaning
* Source 1 - The Movie Database
* Source 2 - Box Office Mojo
* Source 3 - IMDB
* Source 4 - The Numbers

> Data Joins and Data Summary
* Data Join Plan
* Daraframe Joins
* Data Summary

> Exploratory Data Analysis
* Studying Correlations
* Franchises
* Genres
* User Ratings
* MPAA Rating
* Studios
* Failures
* Trends Over Time
* Director
* Writer
* Actors

> Conclusions
* Answers to business questions

> Recommendations

> Future Work

> Errors to Consider

#### [tmdb_api_calls.ipynb](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/tmdb_api_calls.ipynb)
* API tool to obtain IMDB IDs

#### [bom_scraper.ipynb](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/bom_scraper.ipynb)
* Web scraper to get box office numbers

#### [franchise_scraper.ipynb](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/franchise_scraper.ipynb)
* Web scraper to obtain franchise status

## Analysis and Conclusion

#### Should Microsoft focus on launching a franchise, or focus on single film IPs?
> Franchises generally have a higher budget, but their failure rate is far less and they are more likely to a) be profitable and b) yield a surprise hit. They do, however, have a higher variance in both budget and net income. This risk is offset by the observation that franchise films rarely fail, whereas non-franchise films make up the majority of failed films in the last 20 years. A franchise is recommended.
![Figure 1 - Net Income of Franchise vs Non-Franchise](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/franchise_vs_non.png)

#### What audience should the company aim for (based on MPAA rating)?
> Various analysis shows that a movie's performance range declines in both consistency and average net income as the rating increases from G to R. G movies have both the highest consistent income range, and the lowest rate of overall failure. PG is shortly behind. PG-13 is most likely to result in a breakout hit, but has a much lower consistent income range. Lower ratings are the safest and most consistent.
![Net by Rating](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/net_by_rating.png)

#### What genre(s) should the company aim for?
> The genres of Adventure, Animation, Fantasy, Sci-Fi and Action are the most strongly correlated with a positive net income.
![Net by Genre](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/net_by_genre.png)

#### What combination of genre, franchise and rating will result in the lowest risk?
> While franchises involve a higher variance in both budget and net, this risk is offset by their overall higher success rate, with very few franchise films failing to yield a positive net income. This risk is further reduced by sticking to lower MPAA ratings in the G or PG range, and selecting genres that complement these ratings from the animation, sci-fi, fantasy, adventure and action categories. Overall, a G or PG franchise that utilizes Animation and a complementary category such as Adventure should be a very safe endeavor.

#### What, if any, genres/ratings/franchises should be avoided?
> Analysis of the past 20 years first shows that non-franchise films both make less money and are more likely to fail. Most of the film failures in this time period were not franchises. Films are also more likely to fail as their MPAA rating increases. R-movies in particular have a very high rate of failure, with over 30% of the failures of the last 20 years rated R. Finally, certain genres are clearly more likely to fail, with the Drama and Comedy genres representing about 58% and 42% of failures respectively (these numbers add up to 100, but these genres may be shared together on one film, meaning that film is present in both numbers). Things to be avoided include non-franchise films, higher MPAA ratings, and the Comedy, Drama and Thriller categories. These things should certainly be avoided individually, and definitely avoided in combination.
![Failures by Rating](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/bombs_by_rating.png)
![Failures of Non-Franchise vs Franchise](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/franchise_status_fails.png)
![Failures by Genre](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/failures_by_genre.png)

## Recommendations

Exploring this data led to some really strong conclusions for Microsoft. We have evidence that a FRANCHISE is definitely the way to go, mining some existing IP. Family-friendly rated movies in G or PG are the least risky. They are less likely to result in a surprise breakout hit, but they are consistent performers. Finally, Animation, Adventure, and Fantasy are consistently performing genres. When you combine these components together, you can easily identify a Microsoft-owned IP which is family friendly, lends itself to Animation/Fantasy, and has a user base of 126 million, according to Statista. This IP is, of course, Minecraft.
![Minecraft](https://github.com/threnjen/dsc-mod-1-project-v2-1-online-ds-sp-000/blob/master/image14-3.png)

## Future Work

* We can look at the writers/directors that have worked on the genres/ratings we are focusing on
* As far as casting decisions - we can study the importance of big names and cast size for franchise films
* We can look at specific release dates and if any particular time of year is most successful for our rating and genres
* And of course, we can consider additional revenues possibilities from merchandising

## Presentation
[Data Science Module 1 Project](https://youtu.be/nZlwW4bKHPk)




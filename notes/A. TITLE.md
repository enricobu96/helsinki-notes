---
deleted: true
tags: [Introduction to Data Science]
title: A. TITLE
created: '2021-09-19T22:25:22.196Z'
modified: '2021-09-20T08:12:52.355Z'
---

# A. TITLE
Build-a-movie

# B. ELEVATOR PITCH

IMDb is a famous online database of information about movies and tv series; it offers many services, such as searching for a movie, discovering information about a movie (e.g. directors, actors, curiosities and so on) and searching for similar movies. We would like to concentrate on this last aspect: even if this feature is actually offered from the website, sometimes the users might get tired of navigating through the millions of pages that make it up. Our plan is then to build a tool for movie enthusiasts to play around with movie data with the goal of picking the best combination of actors, directors, and genres to build the highest-performing imaginary movie they can come up with. The performance is based on an estimated box office score model built from existing movie box office numbers and IMDB ratings. 
In addition to that, we would also like to address movie directors' problems: some of them, in fact, might want help during the creative phase, and having a tool like this helps. Last but not least, the same directors may not want to risk a complaint for plagiarism; using our platform will then be useful to them, since it will allow them to search for too much similar movies.

# C. DATA

Regarding the data, our intention is to use different data sources and combine them in order to get a consistent dataset. We would like to gather data from three different sources:
IMDb datasets: this data collection is composed of seven different datasets with some common fields (i.e. titleId/tconst and nconst) that can act as primary keys in table joining, and many other different values. We will make use of the IMDbPY library in order to get and better manage this data;
Wikipedia APIs;
OMDb APIs.

We are interested in gathering some specific fields for each movie; these are:
Box office numbers
IMDb ratings
Movie budget
Genre
Main actors
Synopsis
These fields are not meant to be static during the project; we will also gradually try to improve our models and our results, than it follows that we will also try to change the data to gather.

The basic idea is to use IMDb(PY) dataset as a baseline for further data, which will be acquired using the Wikipedia and OMDb APIs since some useful information may be missing (e.g. the synopsis of the movie is more likely to be picked up from Wikipedia than IMDb).

To be more specific, the data workflow will be the following:
First of all, we will download the movie data from IMDb datasets using IMDbPY python library; this operation will be performed only once, in a local environment;
The data will be cleaned. We still have to operate on this data, but our goal is to have a coherent dataset: this means that we will purge possible duplicated data, impute possible missing values, fix eventual errors and, most important, try to gather all the missing data from the other sources (e.g. synopsis from Wikipedia);
The cleaned data will be uploaded as a PostgreSQL database and hosted by some PaaS such as Amazon AWS or Heroku;
The database will be used for further data analysis and for operationalization (cf. next sections). Thus, this data is meant to be static and unchanged.

# D. DATA ANALYSIS
Coming to the data analysis, we will try to use the information gathered from the sources described above in order to find connections between the movies and then offer to the user a usable application (as described in the next sections).
These connections will be based on different variables (box office numbers, IMDb ratings and so on), and we will try to use different machine learning models based on the different use scenarios; two different models we want to try out are:
Linear Regression;
Cosine Similarity.
The use of these different algorithms will be defined better during the implementation, since we want to assess which is the most suitable for our application. For instance, we might want to use cosine similarity first in order to compute the similarity between two movies, and then use linear regression to find the most similar movies given one as input.

# E. COMMUNICATION OF RESULTS
Our final goal is to build a web application that will allow directors to perform two different tasks:
Given a synopsis, budget, actors (and so on) of an original film, directors will be able to find if such a movie is too much similar to another one. This part of the application is meant to prevent a complaint for plagiarism (as defined better in section F);
Directors will also be able to "build the perfect movie" through an interactive game.
As a side project, we would also implement a "web of interconnected movies", in which the user (typically a movie enthusiast) will be able to navigate similar movies in an interactive fashion.
The web application will be developed using the Next.JS framework.

# F. OPERATIONALIZATION

We see that there are few ways this project could be implemented. After a discussion, we finally decided to realize a web application using the Next.JS (React) framework, as discussed in section E, taking advantage of some original features such as gamification. 
The application is primarily meant for movie directors, which will be able to achieve both the task of building "the perfect movie" and the one to search for similar movies in order to prevent possible plagiarism complaints; we noticed that such features were not implemented yet by any other platform, thus making this an added value to the future users.
Furthermore, these features will be almost certainly useful to directors: this application could be in fact used at least to give a general direction to them during the creative phase of thinking and planning a new movie.
As a last thing, the application can be extended also to movie enthusiasts via the implementation of the previously mentioned web of interconnected movies. A feature similar to this one already exists: some websites, including also IMDb, offer the possibility to navigate through similar movies. Our idea, however, has an originality: using this network, the users will be able to discover new movies in an interactive manner, since one movie is connected to other movies which are, in turn, connected to others and so on. The research of new movies would therefore be easier and funnier.

# SOURCES
IMDb datasets: https://www.imdb.com/interfaces/
IMDbPY: https://imdbpy.github.io/
Wikipedia APIs: https://www.mediawiki.org/wiki/API:Main_page 
OMDb APIs: https://www.omdbapi.com/ 



# My-projects
# Movie Project.
Business Problem.
Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies. You are charged with exploring what types of films are currently doing the best at the box office. You must then translate those findings into actionable insights that the head of Microsoft's new movie studio can use to help decide what type of films to create.
GOALS.
1.To get the information on the best selling movies in the current film Industry.
2.To produce the and sell the most profitable films to our audience.
3.To capture and boost our popularity to the large audience of the film industry.
4.To make the most profitable business in the multibillion dollar industry.
DATA USED.
I used data three sets of suggested data from movie sites scrapped from the web.
.The IMDB
.The bom.movie_gross
.The Movie DB

1.THE IMDB DATA.
This was a set of data that potrayed two sets of information:
1.BASICS
.movie_id	
.primary_title	
.original_title	
.start_year	
.runtime_minutes	
.genres
2.RATINGS
.movie_id	
.averagerating
.numvotes
1.BASICS and RATINGS
Decided to work on the two sets together.
I first extracted the columns I needed for my analysis i.e
.start_year
.runtime_minutes
.averagerating
.numvotes
OBJECTIVES TO BE ANSWERED:
1.CHECK  IF THERE IS A CORRELATION BETWEEN runtime_minutes AND averagerating.
2.CHECK  IF THERE IS A CORRELATION BETWEEN averagerating AND numvotes.
3.CHECK  IF THERE IS A CORRELATION BETWEEN numvotes AND runtime_minutes.
I used the sql Query from the sqlite3 module to connect them.
In the first question:
I found out that The correlation coefficient of -0.006486571622673861 indicates that there is a weak, negative association between the Averagerating and Run_time columns. This means that movies with longer run times are slightly less likely to receive high average ratings, while movies with shorter run times are slightly more likely to receive high average ratings. However, the strength of this association is weak, which means that it may not be very meaningful or useful for predicting or analyzing trends in the data.
Note that correlation does not necessarily imply causation, and that other factors or variables may also influence the relationship between these two columns. Therefore, further analysis and exploration of the data may be necessary to fully understand the relationship between Averagerating and Run_time.
In the second question:
![image](https://user-images.githubusercontent.com/108216478/224564305-32abe953-93d5-4dba-8575-c2546a70661a.png)


















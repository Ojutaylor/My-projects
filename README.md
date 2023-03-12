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
1.In the first question:
I found out that The correlation coefficient of -0.006486571622673861 indicates that there is a weak, negative association between the Averagerating and Run_time columns. This means that movies with longer run times are slightly less likely to receive high average ratings, while movies with shorter run times are slightly more likely to receive high average ratings. However, the strength of this association is weak, which means that it may not be very meaningful or useful for predicting or analyzing trends in the data.
Note that correlation does not necessarily imply causation, and that other factors or variables may also influence the relationship between these two columns. Therefore, further analysis and exploration of the data may be necessary to fully understand the relationship between Averagerating and Run_time.
Below is a image of the scatter plot for better visualisation of the above correlation.
![image](https://user-images.githubusercontent.com/108216478/224564305-32abe953-93d5-4dba-8575-c2546a70661a.png)
2.In the second question:
I found out The correlation coefficient of 0.04704076576477309 indicates that there is a weak, positive association between the Averagerating and Num_votes columns. This means that movies with higher average ratings are SLIGHTLY more likely to have more votes, while movies with lower average ratings are SLIGHTLY less likely to have more votes. However, the strength of this association is weak, which means that it may not be very meaningful or useful for predicting or analyzing trends in the data.Also note that correlation does not necessarily imply causation, and that other factors or variables may also influence the relationship between these two columns. Therefore, further analysis and exploration of the data may be necessary to fully understand the relationship between Averagerating and Num_votes.
Below is a image of the scatter plot for better visualisation of the above correlation.
![image](https://user-images.githubusercontent.com/108216478/224564500-77ec7060-d8dd-4290-9c86-9c9e3600b299.png)
3.In the third question:
I found out This is a correlation coefficient of -0.028732762129942167 indicates that there is a weak, negative association between the Num_votes and Run_time columns. This means that movies with longer run times are slightly less likely to have more votes, while movies with shorter run times are slightly more likely to have more votes. However, the strength of this association is weak, which means that it may not be very meaningful or useful for predicting or analyzing trends in the data.REMEMBER that correlation does not necessarily imply causation, and that other factors or variables may also influence the relationship between these two columns. Therefore, further analysis and exploration of the data may be necessary to fully understand the relationship between Num_votes and Run_time.
Below is a image of the scatter plot for better visualisation of the above correlation.
![image](https://user-images.githubusercontent.com/108216478/224565095-0c4939c2-c935-4327-9a45-beedc507aa13.png)
I also also included a bar graph to improve the visualisation.
![image](https://user-images.githubusercontent.com/108216478/224565197-109ea2a0-f5c5-485e-9b30-9368fbbed12e.png)

2.The bom.movie_gross DATA.
.title	
.studio	
.domestic_gross	
.foreign_gross	
.year
I first extracted the columns I needed for my analysis i.e
.domestic_gross	
.foreign_gross	
.year
OBJECTIVES TO BE ANSWERED:
1.DOES THE DOMESTIC GROSS CORRELATE WITH THE FOREIGN GROSS.
2.DOES THE YEAR AND FOREIGN GROSS CORRELATE.
3.DOES THE YEAR AND DOMESTIC GROSS CORRELATE.
1.In the first question:
In this part I used the correlation matrix.
corr_matrix = new_bom.corr()
I found out there is a positive correlation between "domestic_gross" and "foreign_gross" with a correlation coefficient of 0.831178. This means that when the domestic gross revenue of a movie increases, there is a tendency for the foreign gross revenue to also increase. The strength of this positive correlation is considered to be strong as the coefficient is close to 1.
The scatter plot below shows the correlation.
![image](https://user-images.githubusercontent.com/108216478/224565952-0dffeb75-26fa-4237-95a8-edca0c9b2c08.png)
In the second question:
I found out there is also a positive correlation between "foreign_gross" and "year" with a correlation coefficient of 
0.14441. This means that as the year of the movie release increases, there is a tendency for the foreign gross revenue to increase as well. However, the correlation coefficient is relatively weak as it is less than 0.5.
The scatter plot below shows the correlation.
![image](https://user-images.githubusercontent.com/108216478/224566189-a0ae801f-3ff7-41f6-b0e9-3219ea74f01b.png)
In the third question:
I found out that There is a weak positive correlation between "domestic_gross" and "year" with a correlation coefficient of 0.11384. This means that there is a tendency for the domestic gross revenue to increase slightly with the year of the movie release, but the correlation is weak.
The scatter plot below shows the correlation:
![image](https://user-images.githubusercontent.com/108216478/224566455-c9bdf2b8-2f54-4f10-92e8-52387eae5784.png)

3.THE TMDB DATA
.genre_ids	
.id	
.original_language	
.original_title	
.popularity	
.release_date	
.title	
.vote_average	
.vote_count
I first extracted the columns I needed for my analysis i.e
.vote_average
.popularity
.vote_count
.genre_ids
OBJECTIVES TO BE ANSWERED:
1.FIRST QUESTION IS TO SEE IF POPULARITY AFFECTS THE VOTE_AVERAGE.
2.SECOND IS TO SEE IF THE VOTE_AVERAGE CORRELATES WITH THE VOTE_COUNT.
3.CHECK IF THE POPULARITY AND VOTE_COUNT CORRELATES.
1.In the first question:
I found out that the correlation coefficient of 0.1065 suggests a weak positive correlation between the variables "vote_average" and "popularity". This means that as the popularity of a movie increases, there is a slight tendency for the vote_average to also increase, but the relationship between the two variables is not very strong.
Always REMEMBER that correlation does not necessarily imply causation, and other factors may be contributing to the relationship between "vote_average" and "popularity". Additionally, correlation does not account for outliers or non-linear relationships, and it's essential to perform a thorough analysis of the data before making any conclusions based on the correlation coefficient alone.
The scatter plot below shows the correlation:
![image](https://user-images.githubusercontent.com/108216478/224568618-321eb7d8-2ccb-4db7-ab55-f55dd4707adc.png)
2.In the second question:
I found out that the correlation coefficient of 0.1069 suggests a weak positive correlation between the variables "vote_count" and "vote_average". This means that as the number of votes a movie receives increases, there is a slight tendency for the vote_average to also increase, but the relationship between the two variables is not very strong.
It is very IMPORTANT to note that correlation does not necessarily imply causation, and other factors may be contributing to the relationship between "vote_count" and "vote_average". Additionally, correlation does not account for outliers or non-linear relationships, and it's essential to perform a thorough analysis of the data before making any conclusions based on the correlation coefficient alone.
The scatter plot below shows the correlation:
![image](https://user-images.githubusercontent.com/108216478/224568748-e23ee338-c92a-42a4-a276-eafc0a80f34f.png)
3.In the third question:
I found the correlation coefficient of 0.6888 suggests a moderately strong positive correlation between the variables "popularity" and "vote_count". This means that as the popularity of a movie increases, there is a tendency for the number of votes it receives to increase as well, and vice versa.
It is very IMPORTANT to note that correlation does not necessarily imply causation, and other factors may be contributing to the relationship between "popularity" and "vote_count". Additionally, correlation does not account for outliers or non-linear relationships, and it's essential to perform a thorough analysis of the data before making any conclusions based on the correlation coefficient alone.
The scatter plot below shows the correlation:
![image](https://user-images.githubusercontent.com/108216478/224569076-02340095-e844-47e1-9bf5-f343ee323295.png)




























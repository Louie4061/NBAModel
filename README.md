# NBAModel
This will be a model that will optimise a teams success in the next timeframe. This will allow teams to decide what to do with their draft picks / strategy. We will implement a logistic regression at first and if we have time we will try and implement a neural network.

# ML techniques
We will create a model, and allow it to learn from data that I have on the NBA games from the previous 5 seasons, this will contain information such as draft pick numbers,
awards prior to that season, and we will see if there is correlation. Doing so we can further improve our model.

Data Collection:
We will just use an api to get all of the statistics of each game in the previous 5 NBA seasons. We need structured data, so we will most likely store our data as 

Data Preprocessing and Cleaning:
None to be done

Techniques:
We can use Multiclass Classification as we will try and see whether the correlation has a bias to ALL-NBA, Draft Pick Number, Players having previously won championships, etc
We will try and map a team to the result, using the features that we have above.

This will be done with sklearn as it has lots of ML model stuff that I can use.
After using logistic regression os sklearn I learnt that the weighting with the sigmoid played a big part of the results, just giving points scored and points conceeded did not directly correlate to the training of a win. I was using original information such as whether the rebounds per game, assists per game, points conceded, points scored and as a result and if they won the game followed this regression. They did not, as it was not linear, i.e in our model, really large score deficit: 140 - 70 impacted our weighting coefficients and hence we got inaccurate results. However this linear regression proved to be effective when used with the number of wins a team had in a season and whether they made the playoffs.

Initially I started off with an accuracy of 0.83 using just one seasons data. Once concatanating data from 2020 - 2025 the accuracy increased to 0.93. This however decreased when we got to 2017-18.

I will now try and predict an NBA team future success by using information about their team, we will use 

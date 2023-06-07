everaging Machine Learning to Predict NFL QB Passer Rating
Summary Report Warren K. Watson II
Overview
For my Senior Project, I was tasked with coming up with a project to spend the entire semester on to demonstrate my academic knowledge and progress in the field of Computer Science over the past 4 years. The task I came up with and chose to work on was leveraging Machine Learning to predict Passer Rating for NFL Quarterbacks.
Next Gen Stats are a huge thing in the NFL these days, and that is where the inspiration for this project has come from. There’s a lot more to track about a player in the NFL these days than just basic stats from the position they play (# of TD’s, yards, etc.). In today’s league, even the most specific stats are tracked: player speed on a play, difficulty of catch, probability of success on a play, etc. These are referred to as next generation or “next gen” stats.
Next Gen Stats was developed in partnership with Zebra Technologies, Wilson Sporting Goods, and Amazon Web Services (AWS). It provides American Football clubs with data to analyze trends and player performance, while enhancing the fans’ experience in-stadium, online, and during game telecasts. Tracking systems have been installed in every NFL venue and are composed of:
- 20–30 ultra-wide band receivers.
- 2–3 radio-frequency identification (RFID) tags installed into each players’
shoulder pads.
- RFID tags on officials, pylons, sticks, chains, and in the ball.
Sensors throughout the stadium track tags placed on players' shoulder pads, charting individual movements within inches for every player on every single play, all in real time! It is estimated that there are 250 devices total in a venue for any given game, with a team of three operators to confirm that all tracking systems are functioning properly at all times (this is required by the NFL). The tracking system captures player data such as location, speed, distance traveled and acceleration (at a rate of 10 times per second), and charts individual movements within inches.
 The raw data is then used to automate player participation reports, calculate performance metrics, and derive advanced statistics through machine learning on AWS. More than 200 new data points are created on every play of every game, and the system is run entirely on the AWS infrastructure AWS uses their own software called Amazon SageMaker to build, train, and run these predictive models. I wanted my project to model Next Gen Stats, but the lack of access to real time data made that very difficult, so, for this project, I used web scraping and data mining to help in the curation of my own Machine Learning Model to predict the passer rating of NFL QB’s based on previous week's statistics.
Main ideas/approach
In order to even begin to think about how I wanted to structure my model, there were a bunch of questions that needed to be answered. How will I get my data? How do I split up my data into training and testing sets? What IDE will I use? What packages will I need to download? How will I structure my model? What techniques do I need to use? First let’s start with the IDE and packages. I decided to use a Google Co-Lab Notebook with the following packages:
 The datasets needed to be engineered in a certain way, the pandas package was a big help with that. The sklearn packages helped with construction and compilation of my model seamlessly, and the Matplotlib packages helped with data plots as well.
Data
I knew I was going to need raw game by game data in order to set my model up correctly so that is what I looked for, it was very hard to find.
For this project, I used 2 data sets:
- NFL Offensive Player Statistics in the 2019-2020 season (game by game).

 - 26,601 rows, 70 columns/features
- NFL Defensive Statistics in the 2019-2020 season (game by game).
- 2,150 rows, 37 columns/features
*Both From: https://www.advancedsportsanalytics.com/nfl-raw-data*
This website unfortunately “expired”. This kind of shows how hard it is to find good data that isn’t play by play data. The Data Sets were pretty large so data mining and feature engineering were vital here. I did an 80/20 split on the data with 80% of the data going to the training sets, and 20% going to the test sets.
Machine Learning Techniques
In order to create my machine learning model and regularize my parameters I used lasso regression. Lasso stands for “Least Absolute Shrinkage and Selection Operator”. In Statistics and Machine Learning, it is a regression analysis method that performs both variable selection and regularization in order to enhance the prediction accuracy and interpretability of the model. Lasso Regression uses variable selection to decide which variables to include in a particular model, and regularization to avoid overfitting of the data, especially when the trained and test data are much varying. It is implemented by adding a “penalty” term to the best fit derived from the trained data, to achieve a lesser variance with the tested data. The “penalty” is equal to the absolute value of the magnitude of the coefficient. Some coefficients might become zero and get eliminated from the model, and larger penalties result in coefficient values that are closer to zero. This regularization type can result in sparse models with few coefficients.
Base Model
Base Model Architecture:
  Instantiating and Running the Base Model:

  Prediction Outputs (all the same):
 Base Model Results (No learning is taking place):
Final Model
Final Model Architecture:
 
  Instantiating and Running the Final Model:
Prediction Outputs:
  
Final Model Results:
Conclusion
I created a Machine Learning Model to predict future Passer Ratings of NFL QBs based on previous season statistics from earlier on in the season. I did an 80/20 training test split on my data and used lasso regression to regularize my parameters. The system ended up turning out pretty decent, but definitely needs some more work, which is promising.
Limitations:
- Lack of Quality Data
- Tensorflow download and installation problems
- Time
Future Work:
- I did not get a chance to work in defensive data into my predictions because of time, but I would love to get a chance to do that.
- I want to try to see if I can extrapolate this idea to more than just QB’s, maybe to all players.

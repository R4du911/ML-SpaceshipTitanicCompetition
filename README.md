# ML-SpaceshipTitanicCompetition

I implemented a solution with an accuracy rate of 0.795 for the competition Spaceship Titanic listed on Kaggle.
The purpose of this project is to successfully predict which passengers were transported or not to another dimension when the spaceship Titanic 
collided with the spacetime anomaly. The program has at its disposal .csv files containing data of the passengers.

What I learnt from this project:
- ML theory
- different types of classifiers
- different optimisation methods: data imputation, feature engineering

The first optimisation method I used is data imputation. I opted for the ‘most-frequent’ strategy, which fills in the gaps with the value that has the most appearances in each column. Data imputation is a good optimiser, because data that does not hold a value can’t be used by the program to learn. More values means more exercise, so the program can learn better. By using this method the accuracy grew to 0.7884.

Secondly, I tried to optimise the program by using feature engineering. Feature engineering means analysing the data and its features to see which ones have stronger relationships with the target or which derived features one can create in order to maximise the outcome. I began by analysing the mutual information plot of the features (Picture 2) which shows us that VIP feature has no real effect on the prediction of the target, so it shouldn’t be used in the learning process as it may confuse the program. Furthermore, I saw that the “PassengerId” feature is made of a group ID and a number that the person has within that group. PassengerId is unique, so alone it shouldn’t have any real impact on predicting the target, but the group ID feature may have an influence, as it may be that people from a group sticked with one another and managed to survive. Additionally, I experimented by analysing the importance of the trained features and seeing which features influenced the most the training session of the program. By using all these the accuracy grew to 0.79167. 

Lastly, I tried to select the hyperparameters of Random Forest Classifier which would help maximise the accuracy of the program. For that I used GridSearchCV from sklearn and gave it a list of possible values for the hyperparameters from which to choose the best combination. By using this the accuracy grew to 0.79494.


# Janatahack-Customer-Segmentation
AV organised weekend hackathon on customer segmentation.

Team: Last but not the least

Team member : [Atif Hassan](https://www.linkedin.com/in/atif-hassan-1a8a45127/) and Sayantan Basu

Public Leaderboard : 5

One of the main tricks to this hackathon was to identify the common IDs in Train.csv and Test.csv. And simply by copying the target variables( with common IDs) from Train.csv to Test.csv gave a jump from 0.54 to 0.91 in the leaderboard.

Upon identifying this leak the sole target was to build a model and improve the remaining part of the Test.csv data. A simple model with XGBoost gave us ~0.94 on leaderboard.

Finally with some more feature engineering and finetuning a score of ~0.96 was reached on public LB which resulted onto ~0.95 on private LB.

Train.csv and Test.csv are the original files provided in the competition.
I combined the above files and sorted them based on ID to create a new file( say Combined.csv).
Using this file I filled all the missing values in Combined.csv using ffil() and then separated the train and test files back as New_train.csv and New_test.csv. New_train.csv and New_test.csv are modified versions with all missing values filled based on previous rows in the combined sorted Train.csv and Test.csv file.

[Link to the competition page with LB details](https://datahack.analyticsvidhya.com/contest/janatahack-customer-segmentation/#ProblemStatement)

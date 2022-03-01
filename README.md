# Kindle Store Recommender Using PySpark

**Summary**
---
In this project, I attempt to build a recommender for Amazon Kindle Store items using the alternating least squares (ALS) method. The source data contains 3,205,467 records. Each record is a rating for a given item from a given user. Review scores are on a scale of 1 to 5. The ALS yields a root mean square error of 1.48 on validation data.

**Background Information**
---
[PySpark_Project.ipynb](https://github.com/RonaldLi-GitHub/Kindle_Store_Recommender_PySpark/blob/main/PySpark_Project.ipynb) is the main workbook for this project. The project was performed on Google Colab. The data on Amazon Kindle Store items comes from https://jmcauley.ucsd.edu/data/amazon/ [^1]

**Data Visualization**
---
* The first item to confirm that there is no null value in any of the columns
* The original data has user id and item id in string format. Because the ALS model requires both fields be numerical, I assigned ids based on sorted values of user id and item id and created unique ids for each user and item
* PySpark SQL lets us see which items have the most reviews and which have the highest average ratings
* It is shown that most items who have a perfect average rating of 5 have very small number of reviews

**Model Building**
---
* The data is split into 80% training and 20% testing
* The model yields a root mean square error of 1.48 on test data


[^1]: Image-based recommendations on styles and substitutes
J. McAuley, C. Targett, J. Shi, A. van den Hengel
SIGIR, 2015

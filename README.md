# Codsoft_taskno2
Movie Rating Prediction

The used datasets were provived by codsoft from kaggle. 
Explanation of the task :
1. **Importing Data**: The code starts by importing necessary libraries and then uses the `files.upload()` function from Google Colab to upload three datasets: `movies.dat`, `ratings.dat`, and `users.dat`.

2. **Handling Encoding**: The `movies.dat` dataset is read using different encodings (utf-8, latin1, ISO-8859-1, cp1252) to handle potential encoding issues. The first successful attempt is used to read the dataset, and any rows with missing values are dropped.

3. **Merging Datasets**: The `ratings` and `users` datasets are read and similarly processed. Then, the datasets `mov` and `rat` are merged based on the "MovieId" column, and the resulting dataset is stored in `movrat`. Next, `movrat` is merged with the `users` dataset based on the "Id" column, and the merged dataset is stored in `ratuser`.

4. **Exploratory Data Analysis (EDA)**: The code performs some EDA, such as checking for missing values, displaying the distribution of ages of users, and creating a heatmap of user ratings for movies. It also shows the top 25 movies with the most ratings in a bar plot.

5. **Feature Engineering**: The "Genres" column in the `ratuser` dataset is split into individual genres, and one-hot encoding is applied to create binary columns for each genre. Additionally, the "Year" is extracted from the "Title" column and stored in a new column.

6. **Visualizing Gender, Age, and Occupation with Ratings**: The code creates bar plots to visualize the distribution of ratings for different genders, age groups, and occupations.

7. *Modeling with Linear Regression*: A subset of the data (first 1000 rows) is selected for modeling. The feature matrix (X) contains "MovieId," "Age," and "Occupation," and the target variable (y) is "Rating." The data is split into training and testing sets, and a Linear Regression model is trained on the training set. The predictions are made on the test set, and metrics like Mean Squared Error (MSE) and R-squared are calculated.

8. **Visualization of Model Predictions**: A scatter plot is created to compare actual ratings against predicted ratings by the Linear Regression model.

This code performs basic data analysis and modeling on movie ratings data. It reads, cleans, and merges the datasets, explores the data, creates visualizations, and trains a simple Linear Regression model to predict movie ratings based on age, occupation, and movie features.

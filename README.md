# NFL-Match-Predictor
Sports Game Prediction App 
Description: Build a prediction market platform where users can predict the outcomes of upcoming sports games and see results. - 
Frontend: Use React to create a simple interface where users can select games, place predictions, and see historical results. - 
Backend: Node.js with Express or Python with Flask to manage game data, user predictions, and store results in a database. - 
Additional Features: -   Social features for users to share predictions. 
                            - Leaderboard system for users based on the accuracy of their predictions.  
                            - Integration with sports APIs to pull game schedules and results.

Backend Implementation:
  1. Imported the data from Pro Football Reference: https://www.pro-football-reference.com/years/ into .csv files
  2. Using the 22-23 Results, 22-23 Team Stats, 23-24 Results and 23-24 Team Stats, merge and preprocess the data to create a comprehensive dataset that links the results of games with the stats of teams
  3. Cleaned the combined dataset by transforming the Date object into a datetime64
  4. Created predictors for machine learning, Win_code(if the home team won or lost), Home_code and Away_code with each team having a unique respective number
  5. Split the dataset into features and target, the 22-23 Results for training and 23-24 testing
  6. Use RandomForest and estimators to determine the number of decision trees to use, the higher the number; longer algorithm runs potentially more accurate

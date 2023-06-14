# Sports-Betting-Aid-ML-NBA

This is an NBA machine learning program built using Python and the scikit-learn library. The program aims to predict the outcome of NBA games based on various features and historical data. It utilizes a Random Forest classifier and implements feature selection techniques to improve prediction accuracy.

## Table of Contents

- [Introduction](#introduction)
- [Data Collection](#data-collection)
- [Data Preprocessing](#data-preprocessing)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Feature Selection](#feature-selection)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Challenges](#challenges)
- [Future Features](#future-features)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The NBA Machine Learning Program is designed to predict the outcome of NBA games using historical data. By analyzing various features and applying machine learning techniques, the program aims to provide accurate predictions and insights into the factors that contribute to winning games. Through a combination of web scarping, cleaning data, analyzing data, and building a functional model, this project accomplishes the task of predicting NBA games' result.

## Data Collection

The program web scrapes NBA game data from the Basketball-Reference website. It retrieves game scores, team statistics, and other relevant information for each game in the specified seasons. The data is scraped using the BeautifulSoup library and saved to local files for further processing. Certain parts of each web page are selected using HTML/CSS analysis. 

## Data Preprocessing

After collecting the data, the program preprocesses it to prepare it for machine learning. Unnecessary columns are removed, missing values are handled, and the data is transformed or scaled as required. The preprocessing step ensures that the data is in a suitable format for training the machine learning model. Transforming this into a functional data frame, we can now analyze the data in a proper manner without accouting for outliers or exceotions. 

## Exploratory Data Analysis

To gain insights into the data, the program performs exploratory data analysis. It examines the distribution of features, explores correlations, and visualizes relationships between variables. This analysis helps in understanding the patterns and characteristics of the data. By doing this, it becomes clear the cause-and-effect certain factors have and helps in choosing those for usage in the model. 

## Feature Selection

Feature selection is an important step in machine learning to identify the most relevant features for prediction. The program utilizes a Sequential Feature Selector, combined with a Random Forest classifier, to select the optimal subset of features. This technique improves model performance by focusing on the most influential factors. By using a combination of these two, the model selectes the most pressing factors and navigates through each choice as a tree. 

## Model Training and Evaluation

The program trains a Random Forest classifier using the selected features and evaluates its performance. The data is split into training and testing sets, and cross-validation techniques, such as time series split, are used to assess the model's accuracy, precision, recall, and other metrics. Confusion matrices and other visualizations are generated to analyze the model's predictions. This is combined with visualization methods to depict the steps in arriving at the answer as well as understand the practicality of the model. 

## Challenges

1. Data Availability and Quality: Obtaining accurate and comprehensive data was a challenge. NBA data that was web scraped had
inconsistencies, missing values, or errors that needed to be addressed during the data collection and preprocessing stages. This sorting of over 12,000 games required careful analysis and multiple trials. With the right code and methods, I was able to streamline this process and sort the data efficiently.
2. Model Overfitting: The program needs to avoid overfitting, which happens when the model becomes too complex and performs well on training data but fails to generalize to new, unseen data. I grouped my data to train on seasons 2015 - 2020 and use the next 2 seasons as testing data. In this process, I had to make sure to not overfit the factors to fit previous years as the NBA is a ever-evolving game with dynamic features and styles of play. I did this by applying approiate regulariztion techniques and cross-validation methods to help prevent this occurence. 
3. Time: When I first began web scarping, while I knew it would take time I did not realize the true vast amount it would take. I would have
to leave the webscraper overnight in order to successfully have up-to-date data. In addition, running either XGBoost or Random Forest Classifer models with big number of trees caused the system to run very slow as well. It would often take hours for one go of these analysis to finish leading to inefficient data analysis. 


## Future Features

1. Social Media Sentiment Analysis: Integrating sentiment analysis of social media posts and fan discussions related to teams, players, and games would greatly improve model. This would accurately measure the influence of external factors, public perception, and fan sentiment on team performance and outcomes. If a player is doing well, for example, twitter would have an excess number of posts surrounding this player allowing for model to change and update based on this sentiment. 
2. Game Contextual Data: Incorporating contextual information about games, such as home court advantage, back-to-back games, travel distance, time zone changes, and game schedule density. These factors can impact team performance and introduce additional variables for prediction. Player fatigue and player advantages are often talked about by players but models don't usually represent them. In this way, by adding this feature, model would take into account indidual team circumstances and properly represent them. 
3. Visualization and User Interface: Enhancing the program with interactive visualizations, dashboards, and a user-friendly interface to enable users to explore and interpret the predictions, gain insights, and make informed decisions. This would help convey the information in the model more succintly and strongly. 

## Usage

To use the NBA Machine Learning Program:

1. Clone the repository: `git clone https://github.com/your-username/nba-machine-learning.git`
2. Install the required dependencies: `pip install -r requirements.txt`
3. Run the program: `python main.py`
4. Follow the prompts to interact with the program and view the prediction results.


## Contributing

Contributions to the NBA Machine Learning Program are welcome! If you want to contribute, just follow these steps:

1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`
3. Implement your changes and test thoroughly.
4. Commit your changes: `git commit -m "Add feature-name"`
5. Push to the branch: `git push origin feature-name`
6. Open a pull request to the original repository.

## License

This project is licensed under the [MIT License](LICENSE).










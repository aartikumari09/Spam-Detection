# Spam-Detection

***Spam Detection Using Machine Learning - Full Project Report
1. Project Overview
This project aims to classify text messages as 'Spam' or 'Not Spam' (Ham) using Natural Language Processing (NLP) and Machine Learning techniques. The complete pipeline includes data preprocessing, feature extraction, model training, evaluation, prediction, and deployment.
2. Dataset Collection
A dataset containing 200 SMS-like messages was used. Each message is labeled as 1 (Spam) or 0 (Ham).

Columns used:
- label
- message
- cleaned_message
3. Text Preprocessing
The text data was cleaned using standard NLP steps:
- Lowercasing
- Removing punctuation and special characters
- Removing stopwords
- Tokenization
- Lemmatization or stemming

Preprocessing is essential to reduce noise and standardize the data for better model performance.
4. Feature Extraction (TF-IDF)
TF-IDF (Term Frequency-Inverse Document Frequency) was used to convert cleaned text into numerical vectors.

TF-IDF helps highlight important words by reducing the weight of commonly occurring terms.
5. Model Selection & Comparison
The following Machine Learning models were selected:
•	→ Naive Bayes (MultinomialNB):
   - Probabilistic model, ideal for text classification.
•	→ Logistic Regression:
   - A linear model for binary classification.
•	→ Support Vector Machine (SVM):
   - Maximizes margin between classes.
•	→ Random Forest:
   - Ensemble of Decision Trees, powerful but more complex.
Each model was trained, and evaluated using metrics like accuracy, precision, recall, and F1-score.
6. Model Evaluation
The classification report and confusion matrix were used for evaluation. A seaborn bar graph was also plotted to visualize performance across models.
7. Predictions on New Messages
Tested the trained models on new, unseen text messages such as:
- 'Win a free iPhone today!' → Spam
- 'Can we meet at 5 PM?' → Ham

All models correctly predicted the output.
8. Extra Feature: Time-Based Analysis
Random message time stamps were generated using NumPy and datetime.
New columns 'Sent_time', 'Received_time', and 'hour' were added to analyze if spam frequency varies based on time.

2:- Spam vs Ham Messages by Hour of Day
	This bar graph shows how many spam and ham messages are received                                during each hour of the day.

	X-axis: Hours (from 8 AM to 11 PM).
	Y-axis: Number of messages received
	Green bars: Represent Ham (normal) messages.
	Red bars: Represent Spam messages.

	We used sns.countplot() to count how many spam and ham messages were received at each hour.
This analysis helps to understand at what time spam is more likely to occur, which can be useful for future spam filtering improvements.


3:- Hour-wise Spam Analysis
	To make the project more insightful, I added a time-based feature which shows how spam messages vary by the time of day.
      Using this line graph:
 •  Messages were grouped based on the hour they were received (df.groupby("hour")).
•  For each hour, the percentage of spam messages was calculated.
•  The graph helps identify if spam messages are more common at specific times                         (for example, evenings).


This adds a temporal dimension to spam behavior analysis.
9. Model Saving
The best performing model was saved using Pickle:
import pickle
pickle.dump(model, open('model.pkl', 'wb'))
10. Deployment
The project was pushed to GitHub successfully. The repository includes:
- Notebook files
- Trained model
- Graphs and evaluations
- All project source code

Git commands used:
- git init
- git add .
- git commit -m 'Initial commit'
- git remote add origin <repo-url>
- git push -u origin main
11. Challenges Faced
- Cleaning and preprocessing text effectively
- Handling Git errors during repository push
- Choosing the best model
- Understanding evaluation metrics and visualizations
12. Final Outcome
* A complete end-to-end Spam Detection System was built.
* Multiple models were compared.
* Extra features (time analysis) were added.
* Deployed on GitHub.

This project demonstrates a clear understanding of  ML, and project workflow.

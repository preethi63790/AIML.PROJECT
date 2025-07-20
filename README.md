 Project Summary
This project is about building a web application that can detect whether a news article is real or fake. The application is powered by a machine learning model trained on publicly available labeled news datasets. The goal is to allow users to paste a news article into the interface and receive an instant prediction of whether the article is trustworthy or deceptive.

Dataset Used
Two datasets were used in this project:

One dataset contains news articles that are labeled as fake

The other contains news articles that are labeled as true (real)

Each dataset includes the full text of news articles and metadata like title, subject, and publication date. These files were merged into a single dataset with an additional label column: one for fake news and another for real news.

 Data Cleaning and Preprocessing
Before training the model, the news content was preprocessed using standard natural language processing (NLP) techniques:

Lowercasing – All letters in the article text were converted to lowercase to ensure uniformity.

Removing punctuation – All punctuation symbols were stripped out.

Tokenization – The text was split into individual words.

Stopword removal – Common, non-informative words like "and", "the", "is", etc., were removed using a stopwords list from a popular NLP library.

Rejoining – The cleaned tokens were recombined into a cleaned version of each article.

This process helped simplify the text and remove noise before feature extraction.

 Feature Extraction
After cleaning, the articles were converted into numerical features using a method called TF-IDF (Term Frequency-Inverse Document Frequency). This method transforms the text into a format that a machine learning model can understand by quantifying the importance of each word in each article relative to the entire dataset.
 Model Training
The machine learning model used in this project was Naive Bayes, which is a common algorithm for text classification problems. It was trained to distinguish between fake and real news articles using the TF-IDF vectors as input. An optional alternative was Logistic Regression, which can also perform well in this context.

The dataset was split into training and testing sets. The model was trained on the training set and evaluated on the testing set.

 Model Evaluation
To assess performance, two metrics were used:

Accuracy, which tells how many predictions were correct overall.

F1 Score, which balances precision and recall, especially useful for imbalanced datasets.

Both metrics showed high performance, indicating the model was reliable for making predictions.

Streamlit Web Interface
A user interface was created using Streamlit, a lightweight Python framework for building data apps. The interface allows users to:

Paste or type any news article into a text box

Click a button to trigger prediction

See the model’s prediction (Real or Fake)

View the model’s confidence score for that prediction

The Streamlit app was designed to be simple, interactive, and user-friendly.

 Running the App
The app can be run locally on a computer by executing a single command in the terminal. It opens a web page on the browser, where users can interact with the app. Optionally, it can also be exposed publicly using tools that create a temporary public link, making it accessible from mobile devices or shared with others.

 Optional Deployment
For wider accessibility, the project can be deployed to a cloud platform that supports Python and Streamlit apps. This allows anyone with the link to use the app directly without needing to install anything locally.

 Summary
This project combined text classification, natural language processing, and interactive UI development to create a practical tool that detects fake news articles. It demonstrates the full machine learning pipeline — from data loading and cleaning to training, evaluation, and deployment. The result is a fully functional app that brings machine learning into the hands of everyday users.


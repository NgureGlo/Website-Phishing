# Predictive Analysis of Phishing Websites with ML
![alt text](Images/phishing_IPV-blog-1536x1024.png)

## Overview
- **Project Goal:** Develop a machine learning model to detect phishing websites.
- **Focus:** Enhance online security by proactively identifying and blocking potential phishing threats.

## Business Understanding
### Stakeholders
Security team, IT department, executive management.

### Key Business Questions
1. How can we reduce the risk of phishing attacks?
2. What impact will early detection have on business operations and customer trust?

## Data Understanding
### Source of Data
Two datasets from [Kaggle](https://www.kaggle.com/) were explored to see which one would best fit the solution.

### Description of Data
[<u>**Web Page Phishing Dataset**</u>](https://www.kaggle.com/datasets/danielfernandon/web-page-phishing-dataset)
- This dataset is the result of merging two datasets with identical features. Selective feature inclusion was done to retain the most relevant data and to avoid redundancy.
- The dataset had no missing data which posed as a good candidate for the modelling.
- It contains features like:
   1. url_length: The length of the URL.
   2. n_dots: The count of ‘.’ characters in the URL.
   3. n_hypens: The count of ‘-’ characters in the URL.
   4. n_underline: The count of ‘_’ characters in the URL.
   5. n_slash: The count of ‘/’ characters in the URL.

[<u>**Content-based Features Phishing and Legit Websites**</u>](https://www.kaggle.com/datasets/yuvistrange/content-based-features-phishing-and-legit-websites)
- The Dataset comprises 50,000 Websites each having numerical values for all the scraped 43 Content-based Features, with 25,000 labelled as Phishing Websites (assigned Label 1) and 25,000 as Legitimate Websites (assigned Label 0) meaning it has a balanced target class. Content-based Features for each website were extracted using web scraping techniques, specifically Beautiful Soup.
- This dataset also did not contain any missing data.
- It contains features like:
  1. URL
  2. label
  3. number_of_buttons
  4. number_of_images 
  5. has_title
  6. has_input

Both datasets were published this year (2024) which means the datasets captures the rapidly evolving phishing tactics used by attackers. This will make the analysis and solutions produced more relevant to current security challenges.

## Modelling
Classification modeling was used to sort websites into two categories: legitimate or phishing.

Two models, Logistic Regression and Decision Tree were employed to see which one performs the best with the given set of inputs.

Baseline models were built for the two categories of classifiers and then more complex models which had the hyper-parameters tuned were also built to see which kind of model fitted the best.

## Evaluation
The best classification algorithm was the Logistic Regression Model because it correctly identifies whether a website is legitimate or phishing about 99% of the time. It superseded the Decision Tree which correctly classifies 95% of the time.

It also had a precision of 99.7% which means, a given prediction is class 1, there is about a 99.7% chance that the model will correctly label it as class 1 (phishing) and about a 0.3% chance that the model will incorrectly label it as class 0 (legitimate).

Baseline models with default hyperparameters took the win. 


## Relevant Findings
- The best classification algrithm is the Logistic Regression Model because it correctly identifies whether a website is legitimate or phishing about 99% of the time. It superceeds the Decision Tree which correctly classifies 95% of the time.

- All features apart from 4 were important for the predictions.

- Both models produced very good performance metrics with the best Decision Tree model having ROC-AUC of 0.98 and Logistic Regression having a precision score of 99.7%. This means that both models can be used to effectively detect phishing attempts.

## Presentation
If PDF file presentation fails to open, access the slides [here](https://www.canva.com/design/DAGPb-WOw48/LFHBtHqwMTwS_e1dTioPLA/edit?utm_content=DAGPb-WOw48&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton).

## How to Use the Project
1. Clone the repository to your local machine. Use `git clone <repo_url>`
2. Install Dependencies by running `pip install -r requirements.txt` to install necessary Python packages.
3. Navigate to the project directory.
4. Launch Jupyter Notebook by running jupyter notebook in the terminal.
5. Open the `website_phishing.ipynb` notebook.
6. Follow the instructions and execute the cells in the notebook to replicate the analysis steps.
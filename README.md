# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP
## Eboni Lee, DSIR-824

# Executive Summary
Science and technology are often terms used interchangeably or in conjunction with each other, but they are distinct in many ways. One thing that sets them apart are their goals. 'The goal of science is the pursuit of knowledge for it's own sake while the goal of technology is to create products that solve problems and improve human life([Source](https://www.diffen.com/difference/Science_vs_Technology#:~:text=The%20words%20science%20and%20technology,the%20practical%20application%20of%20science)).' Technology is essentially just the practical application of science, a consequence of science and engineering. 

## Problem Statement
Can an NLP classifier be used to determine which subreddit a given post came from, science or technology? If so, how well can it accurately distinguish subreddit posts and what models do best?

### Contents:
- Presentation_Models
- Basic Models
- Pipeline & GridSearch Models
- data
    - all.csv
    - science.csv
    - test.csv
- Project 3 Presentation.pdf
- README.md

## Data 
- 10,000 Subreddit posts taken from 7/9/2020 - 8/31/2020 
- 5000 [Science Subreddit Posts](https://www.reddit.com/r/science)
- 5000 [Technology Subreddit Posts](https://www.reddit.com/r/technology)
- The data has 7 columns: 
    - 5 categorical
    - 1 boolean
    - 1 continuous
    
### Data Dictionary
|Feature|Type|Description|
|---|---|---|
|**title**|categorical|title of the subreddit post|
|**created_utc**|continuous|epoch time / when the post was created|
|**selftext**|categorical|subreddit post|
|**subreddit**|categorical|subreddit the post was located in|
|**author**|categorical|author of the post|
|**media_only**|boolean|was the post media only|
|**permalink**|categorical|url for the given post|

## Conclusion/Recommendations
Out of 12 models run, 4 simple and 8 pipelines, two models were able to predict whether a post was from the Science or the Technology subreddit with 89.36% accuracy. The first model used the TF-IDF Vectorizer and Naive Bayes, and no grid search was needed to get the 89.36% accuracy. The second model used a Lemmetizer, TF-IDF Vectorizer, and Logistic Regression to achieve an 89.36% accuracy, and a grid search was needed to determine the best hyperparameters. Considering all of the modeling I did with Naive Bayes and Logistic Regression, I don't think it will have a significant change in accuracy than what I was able to achieve in this project. In order to get a higher accuracy, I believe it would be worth exploring other modeling techniques such as KNN, SVM or Neural Networks. Also, I would look into adding more features, doing more data cleaning, and collecting more data.
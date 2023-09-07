# Fakenewschallenge-2

## Problem Definition
Stance detection involves determining the relative perspective or opinion expressed in one text in comparison to another text. In the FNC-1 dataset, the task involves comparing article bodies with headlines and classifying them into four categories: ‘unrelated’, ‘agree’, ‘disagree’, and ‘discuss’ without taking a position.

The dataset consists of two separate files: one containing article bodies and the other containing headlines with stances. Each article body is paired with several headlines, and each pair is assigned a stance classification. Therefore, the input for this task includes headlines and body texts, and the output is the corresponding stance category. The training dataset consists of 49,972 instances, with approximately 73% labelled as unrelated, 18% as 'discuss', 7% as 'agree', and 2% as 'disagree'.

## Problem Solution
This problem can be tackled in two steps, involving a hierarchical architecture. The first step is to determine whether the article content is related or unrelated to the headline. If the data is related, the pairs will be further classified into the stances of 'agree', 'disagree', or 'discuss'. Consequently, the data will be trained twice, with the first level using machine learning and deep learning models. The performance of each model will be compared using two different feature extraction techniques: Tf-idf and BERT. The best-performing model will then proceed to the second level, where it will be trained using deep learning techniques to perform multiple classifications.

## Feature Extraction
Before training a model on the data, the corpora need to be converted into numerical features. This report discusses two methods of feature extraction: Tf-idf and transformers, both of which can be used with machine learning and deep learning models. The following sections will explain how these methods work, along with their advantages and disadvantages.

## Training
In this report, we seperate this challenge into two cases: binary classification and multi-class classification. 

First, we classify the data into related and unrelated stances which are trained with TFIDF and XGBoost. Then, we use MLP+TFIDF to train multi-class classfication which have agree, disagree and discuss classes within related stances.


---
layout: post
title:  "Getting an 120/120 on TOEFL"
date:   2021-11-16 21:17:37 +0530
categories: jekyll update blog
---
## SEMANTIC SIMILARITY AND TOXICITY DETECTION IN QUORA QUESTIONS


### INTRODUCTION

300 million monthly active users use Quora, a question and answer platform for asking their queries on anything piquing their curiosity and also publish their unique experiences and knowledge in the answers. Such a tremendous platform used by seekers, writers, and viewers faces the issue of duplicate or similar meaning questions. This decreases the proliferation of good content and increases the effort of writers. With an increasingly social world, the polarization of content is also an issue to be tackled. Questions disparaging a community or posing a threat to the fabric of society need to be moderated. 

### PROBLEM DEFINITION
Online Social Networks continue to play an important role as information is regularly uploaded and exchanged. Abuses of such media of communication for various malicious purposes are very common. We need to identify such content and flag it appropriately for creating a safe platform.

Also, Question duplication is a major problem in any public discussion forum. Fragmentation of answers across various versions of the same question results in a lack of a sensible search, answer fatigue, segregation of information, and the paucity of response to the questioners. The duplicate questions can be detected using Machine Learning and Natural Language Processing. 

We are aiming to build an application that solves 2 problems: 
1. When 2 questions are given as an input, we find if they are similar or not?
2. When 1 question is given, we classify if the question is appropriate or not? and the output if there are any similar questions to the given on in the dataset.

### METHODS

For question-pair input

![alt text](./img_method_1.png)

For single question input

![alt text](./img_method_2.png)

We identify the two datasets we will use to solve this challenge. They are released by Quora.
#### Datasets:
1. Quora Question Pairs Dataset for finding the similarity between questions.
2. Quora Insincere Questions Classification Dataset for detecting any objectionable/toxic content in the questions.

To convert the initial corpus of text to a standard form, we perform the below data preprocessing steps. 
#### Data Pre-processing:
1. Stop-word, punctuation removal
2. Stemming/Lemmatization
3. Lower-case conversion

The next step is to generate embeddings from the cleaned data. We will compare the below methods that work best for our model.
#### Feature Engineering:
1. TF-IDF
2. Word2Vec/Glove neural network
3. Elmo-embeddings
4. Latent Semantic Indexing

Proceeding to perform unsupervised learning to cluster similar questions.
#### Clustering of similar questions:
1. K-means
2. DBSCAN
3. Spectral clustering

#### The machine learning methods can provide us good results on the classification of content as toxic or not:
1. Random Forest
2. SVM

#### State-of-the-art Deep learning methods will be trained on the datasets and the results of toxicity classification and similar question clustering will be benchmarked.
1. LSTM
2. BERT - Can generate own embeddings too.
3. Gated Recurrent Unit



### POTENTIAL RESULTS

The results will be presented with a Streamlit application, which can produce results for the two kinds of inputs - a question pair or a single question.

We will benchmark the following methods with state-of-the-art architectures.
1. Cosine similarity and Jaccard similarity for semantic text similarity
2. Precision, recall, f1-score, accuracy for toxicity detection.
3. Silhoutte Coefficient for evaluating clustering.


![alt text](./img_results_small.png)
### Split of Work


| Task | Timeline | Person(s) assigned |
| ------------ | ------------- | ------------ |
| Data Cleaning of 2 datasets | 1 week | Asha |
| Feature Engineering | 1 week |Amirtha and Rishabh |
| Unsupervised Learning (Clustering) | 1 week | Shyam |
| Supervised Learning (using ML methods) | 2 weeks | Asha and Amirtha |
| Supervised Learning (using DL methods) | 2 weeks | Madhumitha, Rishabh, Shyam |
| Results summary & Benchmarking | 1 week | Madhumitha |

### Checkpoint
- Data cleaning and feature engineering is done to get meaningful embeddings
- The embeddings are passed on to the machine learning models
- A clustering model is trained for the output of similar questions
- A classification model is trained to predict the toxicity of the question and also if two given questions are similar or not.


### References
- [1810.10641] Predicting the Semantic Textual Similarity with Siamese CNN and LSTM
- [1807.02854] Replicated Siamese LSTM in Ticketing System for Similarity Learning and Retrieval in Asymmetric Texts
-  Text Similarity with Siamese Recurrent Networks
- Proceedings of the 24th ACM International on Conference on Information and Knowledge Management: Short Text Similarity with Word
- A Survey of Text Similarity Approaches


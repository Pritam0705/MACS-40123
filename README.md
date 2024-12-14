## **Topic Modeling and Analysis of Misinformation Trends in India**

This Repository contains the preliminary analysis of the misinformation data.    
The structure of the repository is as follows:  
This folder contains the pdf file containing summaries of the recent three relevant academic articles, the results of the method used, and the social, cultural, and behavioral implications of the findings.  
ITR1:  
ITR2:  
ITR3:  
ITR4:  

Google Colab Link: [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1YBy1VNF1MnoWa_TAHplQ8o0kX7d0784z?usp=sharing]

## Data
Scraped debunked misinformation data from  the prominent Indian fact-checking platform- Boomlive. Boomlive is a member of the International Fact
Checking Network (IFCN) and partnered with Facebook’s Third Party Fact-Checking Program.  
The data contains the following fields:-  
- Link to the article
- Heading of the article
- Subheading of the article
- Author (fact-checker name)
- Date of publishing
- Claim
- Fact Check
- Claimed by (X users, Facebook users, WhatsApp, Media organization)
- Fact Check Summary (True, False, Misleading)
- Links (to archived post, Facebook post, or X post)

## Methods Used
### Top2Vec
Top2Vec (https://github.com/ddangelov/Top2Vec) is an algorithm that simultaneously learns the topic representations and the word embeddings. By mapping documents to a continuous vector space, Top2Vec identifies clusters of documents that share similar themes without requiring a pre-defined number of topics. This approach allows for the discovery of natural and meaningful topics directly from the data.  
  
Top2Vec involves the following steps:  
  
**Embedding Creation:** Top2Vec uses word embeddings to create document vectors.  
**Dimensionality Reduction:** The document vectors are reduced to a lower-dimensional space using techniques like UMAP.  
**Clustering:** The reduced vectors are clustered to identify topics.  
**Topic Words Identification:** The algorithm finds words that are closest to the cluster centroids, representing the topics.  

### BERTopic
BERTopic leverages transformer-based embeddings to create document representations and applies clustering algorithms to discover topics. It combines BERT embeddings with clustering techniques like HDBSCAN and dimensionality reduction methods like UMAP to generate coherent topics from text data.  
  
BERTopic involves the following steps:  
  
**Embedding Creation:** BERTopic uses transformer models to create document embeddings. 
**Dimensionality Reduction:** The embeddings are reduced in dimensionality using UMAP.  
**Clustering:** Density-based clustering algorithm such as HDBSCAN are applied to form clusters from the reduced embeddings.  
**Topic Representation:** The algorithm generates topics based on the clustered documents and their embeddings.  




# Machine-Learning
The aim of this project was to explore the effectiveness of a range of different machine learning techniques for predicting the sentiment of text movie reviews.

## Data Supplied
We were provided with the dataset from the paper:

Recursive Deep Models for Semantic Compositionality Over a Sentiment Treebank
Richard Socher, Alex Perelygin, Jean Wu, Jason Chuang, Christopher Manning, Andrew Ng and Christopher Potts
Conference on Empirical Methods in Natural Language Processing (EMNLP 2013)

The file included:
1. original_rt_snippets.txt contains 10,605 processed snippets from the original pool of Rotten Tomatoes HTML files. Please note that some snippet may contain multiple sentences.

2. dictionary.txt contains all phrases (parsed by the Stanford Parser) and their IDs, separated by a vertical line |

3. sentiment_labels.txt contains all phrase ids and the corresponding sentiment labels, separated by a vertical line.
Note that you can recover the 5 classes by mapping the positivity probability using the following cut-offs:
   [0, 0.2], (0.2, 0.4], (0.4, 0.6], (0.6, 0.8], (0.8, 1.0]
for very negative, negative, neutral, positive, very positive, respectively.
Please note that phrase ids and sentence ids are not the same.

## Our Strategy
### Cleaning The Corpus
We split each dictionary.txt entry into individual words; removed "stop words" (i.e. filler words), numbers and special characters; and lemmatized each remaining word (i.e. converted it to its grammatical root, so working -> work and worked -> work). The resulting lists of words, each representing a dictionary entry, I will hence refer to as phrases.

### Phrase Embedding
We tried three different embedding strategies: a count array (or one-hot encoding); a semantic embedding using the method 'word2vec' from the package 'gensim'; and a tf-idf encoding.
#### UMAP
We use a UMAP dimension reduction to visualise the data in each encoding. We hoped to see some sort of clustering or distinct variance, but the plots reveal all data to be very uniform, a sign that the encodings are not storing significant information. The word2vec visualisation shows the least variance, a bad omen which if also reflected in its poor prediction performance later. 

### Machine Learning Methods
For each encoding, we fitted a convolutional neural network (CNN) and a dense neural network.

### Findings
We found the TF-IDF encoding, fitted to a CNN the most accurate predictor on the evaluation set. For more information on this conclusion, our results and methods, see the submission file:  AML_Project__Sentiment_Analysis (1).pdf

## Files
#### AML_Project__Sentiment_Analysis (1).pdf
This was our project submission, and contains detailed explanation and discussion or results and methods.
#### 

# Machine-Learning
The aim of this project was to explore the effectiveness of a range of different machine learning techniques for predicting the sentiment of text movie reviews.

## Data Supplied
We were provided with the dataset of the paper:

Recursive Deep Models for Semantic Compositionality Over a Sentiment Treebank
Richard Socher, Alex Perelygin, Jean Wu, Jason Chuang, Christopher Manning, Andrew Ng and Christopher Potts
Conference on Empirical Methods in Natural Language Processing (EMNLP 2013)

The file included:
1. original_rt_snippets.txt contains 10,605 processed snippets from the original pool of Rotten Tomatoes HTML files. Please note that some snippet may contain multiple sentences.

2. dictionary.txt contains all phrases and their IDs, separated by a vertical line |

3. sentiment_labels.txt contains all phrase ids and the corresponding sentiment labels, separated by a vertical line.
Note that you can recover the 5 classes by mapping the positivity probability using the following cut-offs:
   [0, 0.2], (0.2, 0.4], (0.4, 0.6], (0.6, 0.8], (0.8, 1.0]
for very negative, negative, neutral, positive, very positive, respectively.
Please note that phrase ids and sentence ids are not the same.

## Our Strategy
We

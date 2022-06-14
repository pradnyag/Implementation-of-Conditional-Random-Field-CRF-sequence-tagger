# Implementation of Conditional Random Field (CRF) sequence tagger
Optimized the performance of a Conditional Random Field (CRF) sequence tagger for movie trivia questions and answers data, which consist of instances of data of word sequences with the target classes/labels for each word in a BIO (Beginning, Inside, Outside) tagging format.

There are 25 unique BIO tags in our dataset.

Read in, pre-processed, trained and developed the tagger on the training data from trivia10k13train.bio.txt and finally tested the tagger on the data trivia10k13test.bio.txt attempting to get the best performing tagger across the different labels in our development process. Optimized the performance of the tagger by improving its feature extraction function on the word sequences and incorporating POS tagging. 
After splitting the training data the average F-score was 0.55503, which slightly increased to 0.57720 on inclusion of POS tag feature. Also, the comparison between the precision and recall values for individual classes after adding part of speech tag showed increment for maximum number of classes.
Interestingly, B-Soundtrack and I- Soundtrack showed major improvements of F score from 0 to 0.14 and 0.18 to 0.39 respectively.
Tuning the c1 and c2 regularization parameters required more amount of time. The optimal values of c1=0.2 and c2=0.2 produced F score of 0.6346057 on 20% split test data and 0.635685 on the original test data.

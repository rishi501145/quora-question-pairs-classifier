# quora-question-pairs
A NLP project to find weather given 2 questions are same are not semantically speaking.


Dataset Link - https://www.kaggle.com/c/quora-question-pairs

## Check out the live demo: https://quora-question-classifier.herokuapp.com/

## Similarity Score :
How does it decide which item is most similar to the item user likes? Here come the similarity scores.

It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.

 ## How Cosine Similarity works?
 
Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.


![alt text](https://user-images.githubusercontent.com/36665975/70401457-a7530680-1a55-11ea-9158-97d4e8515ca4.png)




## Advanced Features

### 1. Token Features
**cwc_min**: This is the ratio of the number of common words to the length of the smaller question

**cwc_max**: This is the ratio of the number of common words to the length of the larger question

**csc_min:** This is the ratio of the number of common stop words to the smaller stop word count among the two questions

**csc_max:** This is the ratio of the number of common stop words to the larger stop word count among the two questions

**ctc_min:** This is the ratio of the number of common tokens to the smaller token count among the two questions

**ctc_max:** This is the ratio of the number of common tokens to the larger token count among the two questions

**last_word_eq:** 1 if the last word in the two questions is same, 0 otherwise

**first_word_eq:** 1 if the first word in the two questions is same, 0 otherwise

#### ctc_max_cwc_max_csc_max
![alt text](https://github.com/rishi501145/quora-question-pairs-classifier/blob/main/imgaes/ctc_max_cwc_max_csc_max.png)

#### ctc_min_cwc_min_csc_min

![alt text](https://github.com/rishi501145/quora-question-pairs-classifier/blob/main/imgaes/ctc_min_cwc_min_csc_min.png.png)



### 2. Length Based Features

**mean_len:** Mean of the length of the two questions (number of words)

**abs_len_diff:** Absolute difference between the length of the two questions (number of words)

**longest_substr_ratio:** Ratio of the length of the longest substring among the two questions to the length of the smaller question

#### first_last_word

![alt text](https://github.com/rishi501145/quora-question-pairs-classifier/blob/main/imgaes/first_last_word.png)

![alt text](https://github.com/rishi501145/quora-question-pairs-classifier/blob/main/imgaes/length_feature.png)


### 3. Fuzzy Features

**fuzz_ratio:** fuzz_ratio score from fuzzywuzzy

**fuzz_partial_ratio:** fuzz_partial_ratio from fuzzywuzzy

**token_sort_ratio:** token_sort_ratio from fuzzywuzzy

**token_set_ratio:** token_set_ratio from fuzzywuzzy

### Fuzzy Features
![alt text](https://github.com/rishi501145/quora-question-pairs-classifier/blob/main/imgaes/fuzzywuzzy.png)







## visualization

### How data look in 3d space using plotly

![alt text](https://github.com/rishi501145/quora-question-pairs-classifier/blob/main/imgaes/data%20in%203d.png)

### How data look in 2d space using plotly
![alt text](https://github.com/rishi501145/quora-question-pairs-classifier/blob/main/imgaes/isduplicated2d.png)

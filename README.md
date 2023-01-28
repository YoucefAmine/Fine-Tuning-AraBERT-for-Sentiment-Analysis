# Arabic Sentiment Analysis and Text Classification (Fine Tuning AraBERT)
Sentiment Analysis is to build machine learning models that can determine the tone (positive, negative, neutral) of the texts (e.g., movie reviews, tweets...). It is one of the most important and standard tasks in NLP. However, Arabic sentiment analysis has not been studied at a level as high as other languages (e.g., English, Chinese, French...). One of the key factors is the lack of high-quality and large-scale training data.
    
- ### Datasets:
  - **[ArSAS](https://homepages.inf.ed.ac.uk/wmagdy/resources.htm)**
    - Arabic Speech-Act and Sentiment Corpus of Tweets Dataset.
    - 21K Tweets.
    - 4 Classes: Negative, Positive, Mixed and Neutral.
  - **[LABR](https://github.com/mohamedadaly/LABR)**
    - Large-Scale Arabic Book Reviews Dataset.
    - 63K Book Reviews.
    - Rating: 1 to 5.
  - **[HARD](https://github.com/elnagara/HARD-Arabic-Dataset)**
    - Hotel Arabic Reviews Dataset.
    - 94K Hotel Reviews.
    - Rating: 1 to 5.

- ### Hyper parameters:
| Parameter        | Value |
| ---------------- | ----- |
| Batch Size       | 128   |
| Learning Rate    | 0.01  |
| Optimizer        | adam  |
| Number of Epochs | 2     |

- ### Model & Results:
 
![tallip2101-14-f01](https://user-images.githubusercontent.com/45196964/215270340-67d699d1-4f72-43d3-9e0e-f48331c5267b.jpg)

**[AraBERT](https://github.com/aub-mind/arabert/tree/master/arabert)** is a BERT-based model that was pretrained using the MLM approach. we used AraBERT v2 in which emojis were added to their vocabulary in addition to common words that weren’t at first present. The pre-training was done with a max sentence length of 64 only for 2 epoch. we got the following results in the table bellow

| Datasets  | Precision | Recall | F1-Score | **Accuracy** |
| --------- | --------- | ------ | -------- | ------------ |
| **ArSAS** | 77%       | 79%    | 77%      | `79.54%`     |
| **LABR**  | 92%       | 93%    | 92%      | `93.08%`     |
| **HARD**  | 96%       | 96%    | 96%      | `96.06%`     |

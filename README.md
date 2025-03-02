# NLP_QuestionPairSimilarity
NLP project which answers the similarity between two question input

# Quora Question Pairs Similarity Challenge (Kaggle)

The Quora Question Pairs competition on Kaggle challenged participants to build models that could identify duplicate questions. This competition was a significant challenge in natural language processing (NLP), requiring a combination of techniques from text preprocessing, feature engineering, and machine learning.

## The Problem:

* Quora aimed to improve the user experience by reducing the number of duplicate questions.
* The challenge was to determine whether pairs of questions had the same intent.
* This is a semantic similarity problem, where understanding the meaning of the questions is crucial, not just matching keywords.

## The Data:

* The dataset consisted of pairs of questions, along with a binary label indicating whether the questions were duplicates (1) or not (0).
* The questions themselves were text strings, often with variations in phrasing, spelling, and grammar.
* The data was imbalanced, with far more non-duplicate pairs than duplicate pairs.

## The Evaluation Metric:

The evaluation metric is:

* **Log Loss (Binary Logarithmic Loss):**
    * This metric is commonly used for binary classification problems, where the goal is to predict the probability of an instance belonging to a certain class.
    * In this case, it measures the "error" of the predicted probabilities compared to the actual binary labels (duplicate or not duplicate).
    * Essentially, it penalizes incorrect predictions, and the penalty increases as the predicted probability deviates further from the true label.
    * Therefore the goal was to minimize the log loss.

Key aspects of this metric in the context of the competition:

* It emphasizes the importance of accurate probability estimation.
* It heavily penalizes confident but incorrect predictions.

Therefore, participants were tasked with building models that could not only classify question pairs as duplicates or not, but also provide accurate probability scores for those classifications.
## Key Challenges:

* **Semantic Understanding:** Models needed to go beyond simple keyword matching and capture the underlying meaning of the questions.
* **Text Preprocessing:** Cleaning and normalizing the text data was essential, including handling misspellings, contractions, and punctuation.
* **Feature Engineering:** Creating relevant features from the text, such as word embeddings, TF-IDF vectors, and other semantic representations, was critical.
* **Imbalanced Data:** Dealing with the imbalance in the dataset was crucial to prevent models from being biased towards the majority class.
* **Computational Complexity:** working with large text datasets required efficient algorithms and computational resources.

## Common Approaches Competitors Used:

* **Word Embeddings:** Using pre-trained word embeddings like Word2Vec, GloVe, and FastText to represent words and phrases.
* **Sentence Embeddings:** Techniques like Siamese networks and LSTMs to generate sentence-level embeddings.
* **Machine Learning Models:** Training models like gradient boosting machines (e.g., XGBoost, LightGBM) and neural networks on the extracted features.
* **Deep Learning:** Utilizing deep learning architectures, particularly recurrent neural networks (RNNs) and convolutional neural networks (CNNs), to capture the sequential and structural information in the questions.
* **Feature Engineering:** extensive work was done to create features like fuzzy string matching, TFIDF, and other methods of comparing the strings.

## Solution details in this repository:
**QuoraQuestionPairSimilarity.ipynb:** This file describes the NLP approach to develop a machine learning project.
**DeploymentFile.ipynb:** This file uses the developed model and functions and demonstrates deployment.

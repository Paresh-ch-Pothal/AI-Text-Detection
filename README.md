# AI Text Detection Model

This project is a text detection model that determines whether a given text is written by an AI or a human. The model leverages both **semantic** and **linguistic features** to analyze the content and classify it accurately.

## Features

The model utilizes the following key features for detection:

- **avg_word_length**: The average length of words in the text.
- **stopword_ratio**: The ratio of stopwords (commonly used words like "the", "is", etc.) in the text.
- **noun_ratio**: The ratio of nouns in the text, which helps identify the grammatical structure.
- **type_token_ratio**: The ratio of unique words to total words in the text.
- **adj_ratio**: The ratio of adjectives in the text, providing insight into the descriptive nature.
- **perplexity**: A measure of how well a model predicts a sample of text. Lower perplexity often indicates more human-like text.
- **hapax_ratio**: The ratio of words that occur only once in the text.
- **answer_topic_relevance**: The relevance of the text to the given topic or question.

## Model Performance

After training the model with these features, it achieved an **AUC-ROC score of 0.94**, demonstrating excellent performance in distinguishing between AI-generated and human-written text.

## How It Works

1. **Data Preprocessing**: The text is preprocessed to extract linguistic features, including word length, noun and adjective ratios, and more.
2. **Feature Extraction**: The features listed above are calculated from the text.
3. **Model Training**: A machine learning model is trained using these features to classify the text as either AI-generated or human-written.
4. **Prediction**: The trained model predicts whether the given text is more likely to be written by an AI or a human based on the extracted features.

## Usage

To use this model, you can pass a text sample through the feature extraction and classification pipeline. The model will output a prediction of whether the text is written by an AI or a human.

## Results

The model has been evaluated using the **AUC-ROC** metric, which gives a value between 0 and 1:
- **AUC-ROC = 0.94**: This indicates that the model is highly accurate in distinguishing between AI and human text.

## Conclusion

With the combination of semantic and linguistic features, this AI Text Detection Model achieves a high level of accuracy, making it an effective tool for detecting AI-generated content.

## Future Work

- **Improving Feature Set**: Adding more features could potentially improve model performance.
- **Fine-Tuning the Model**: Further fine-tuning with more data could lead to even higher accuracy.
cd ai-text-detection
pip install -r requirements.txt

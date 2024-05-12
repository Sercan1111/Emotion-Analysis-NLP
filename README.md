# Emotion-Analysis-NLP

## Overview
This project leverages advanced Natural Language Processing (NLP) techniques to analyze and classify emotions from textual comments. The analysis categorizes text into various emotions like joy, anger, fear, sadness, and surprise. The project uses Python, with extensive use of libraries such as NLTK, scikit-learn, pandas, and seaborn for sophisticated data preprocessing, emotion analysis, and visualization.

## Dataset
The dataset initially comprises text comments labeled with emotions. To enhance the model's training data, we merge this dataset with another dataset, expanding the diversity and volume of our training samples. This combined dataset helps in improving the robustness and accuracy of our emotion classification model.

## Preprocessing Steps
1. **Text Normalization:** Convert all texts to lowercase to ensure uniformity.
2. **Tokenization and Cleaning:** Use regex and NLTK's tokenization to clean and tokenize text.
3. **Stopword Removal:** Remove stopwords to focus on more meaningful words. Custom adjustments keep negations like 'not' which are crucial for sentiment analysis.
4. **Emoji Extraction:** Emojis are extracted and analyzed as they provide significant emotional context.
5. **TF-IDF Vectorization:** Transform texts into a vectorized format using TF-IDF, emphasizing important but less frequent words.

## Feature Engineering
- **Phrase Enhancements:** Identify and weigh phrases highly indicative of specific emotions, like "feeling brave" or "im feeling stressed."
- **N-gram Analysis:** Incorporate bi-gram and tri-gram models to capture contextual information that single words might miss.

## Data Aggregation and Balancing
- **Data Merging:** Aggregate data from multiple sources to enrich the dataset.
- **Resampling Techniques:** Apply oversampling for underrepresented emotions and undersampling for overrepresented ones to balance the dataset, ensuring the model does not develop a bias toward more frequent labels.

## Visualization
- **Emotion Distribution:** Visualize the frequency of each emotion to understand dataset composition.
- **Word Frequency Analysis:** Identify and visualize the most frequent words and n-grams for each emotion to gain insights into common linguistic patterns.

## Model Training and Evaluation
- **Multinomial Naive Bayes:** Chosen for its effectiveness in text classification tasks.
- **Model Evaluation:** Assess model performance using accuracy, precision, recall, and F1-score metrics. Advanced techniques like grid search are used to fine-tune model parameters.

## Files in the Repository
- `emotion_analysis.py`: The main script with preprocessing, modeling, and evaluation logic.
- `requirements.txt`: Lists all the Python dependencies.
- `data/`: Directory containing the datasets used.

## How to Run
Ensure you have Python installed and proceed as follows:
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
2. Execute the script:
  python emotion_analysis.py

# Future Work
- Explore LSTM or BERT for potentially enhanced performance due to their state-of-the-art results in similar tasks.
- Experiment with additional preprocessing techniques and alternative machine learning algorithms.
- Consider implementing a web interface for real-time emotion analysis.

# Contributions
Feel free to fork this project and submit pull requests. You can also open an issue if you find bugs or have feature requests. Your contributions are welcome!



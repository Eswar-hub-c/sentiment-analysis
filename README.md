# sentiment-analysis

## Project Structure

- **Sentiment_Analysis_Tool.ipynb**: The Jupyter notebook that contains the complete code to build and test the sentiment analysis model.
- **README.md**: This file, containing the project description and instructions.

## Steps Included

1. **Data Preprocessing**: Cleansing of the text data, including removal of stop words and punctuation.
2. **Feature Extraction**: Converting text data into numerical form using `CountVectorizer`.
3. **Model Building**: Training a Naive Bayes classifier to predict the sentiment of customer feedback.
4. **Model Evaluation**: Assessing the model's performance using accuracy and confusion matrix.
5. **Testing**: Predicting sentiment for new customer feedback.

## How to Use

1. Clone this repository to your local machine.
2. Open the `Sentiment_Analysis_Tool.ipynb` in Jupyter Notebook or JupyterLab.
3. Run each cell step-by-step to execute the code and build the model.
4. You can modify the sample feedback data or input new customer feedback to test the tool.

## Example

Here’s how you can test the model with new feedback:

```python
new_feedback = ["The product is great and I love it!"]
cleaned_new_feedback = [clean_text(feedback) for feedback in new_feedback]
new_feedback_vector = vectorizer.transform(cleaned_new_feedback)

# Predict sentiment
predicted_sentiment = nb.predict(new_feedback_vector)
print(f"Predicted sentiment: {predicted_sentiment[0]}")

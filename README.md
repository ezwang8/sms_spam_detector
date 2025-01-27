# SMS Spam Detector

## Project Overview

The goal of this project is to develop a machine learning program that can classify SMS text messages as either "spam" or "not spam" with the help of the Support Vector Classifier (SVC) pipeline. By utilizing Gradio, we created an interactive web-based application that allows users to test the model with their own inputs.

## Installation Instructions

1. **Clone the Repository:**
   ```bash
   git clone <repository-link>
   ```

2. **Verify Python Installation:**
   Check if Python is installed by running:
   ```bash
   python --version
   ```
   If Python is not installed, download it from [python.org](https://www.python.org/downloads/).

3. **Install Required Packages:**
   Install the necessary Python libraries:
   ```bash
   pip install pandas scikit-learn gradio
   ```

4. **Navigate to the Project Directory:**
   ```bash
   cd sms_spam_detector
   ```

5. **Run the Gradio Application:**
   Launch the Gradio app:
   ```bash
   python gradio_sms_text_classification.py
   ```

6. **Access the Application:**
   The application will run on a local URL displayed in the terminal, such as `http://127.0.0.1:7863`. To create a shareable link, use:
   ```python
   sms_app.launch(share=True)
   ```

## Steps

1. **Prepare the Data:**
   - Load the dataset (`SMSSpamCollection.csv`) into a DataFrame.
   - Split the data into features (`text_message`) and labels (`label`), and preprocess it for training.

2. **Train the Model:**
   - Use a machine learning pipeline with `TfidfVectorizer` for text feature extraction and `LinearSVC` for classification.
   - Train the model on 67% of the data, reserving 33% for testing.

3. **Create the SMS Classification Function:**
   - Define a function to preprocess and train the model.
   - Return the trained model for predictions.

4. **Develop the Prediction Function:**
   - Define a function to predict whether an SMS is "spam" or "not spam."
   - Provide user-friendly output messages for the predictions.

5. **Build the Gradio Interface:**
   - Create an interactive Gradio app with text input for SMS messages and output displaying the classification result.
   - Test the app with example messages, including:
     - `"You won 2 free tickets to the Super Bowl."` (spam)
     - `"Hey, are we still on for dinner tonight?"` (not spam)

## Summary

- The spam detecting app successfully classified SMS messages as "spam" or "not spam" with the trained SVC model.
- Gradio was able to provide an easy-to-use interface for testing the model in real time.
- The program can be further improved upon by placing it online or adding more advanced natural language processing techniques.

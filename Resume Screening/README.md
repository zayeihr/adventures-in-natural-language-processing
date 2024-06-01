# Resume Screening App

This is a simple web application for resume screening using machine learning, created as part of my learning process. The application is built with Streamlit and utilizes pre-trained models to predict the category of a given resume.

## Features

- Upload resumes in `.txt` or `.pdf` format.
- Automatically clean and preprocess the resume text.
- Use a trained TF-IDF vectorizer and classification model to predict the category of the resume.
- Display the predicted category to the user.

## Requirements

- Python 3.x
- Streamlit
- scikit-learn
- nltk
- pickle

## Installation

1. Clone the repository or download the files.

2. Install the required packages:

    ```bash
    pip install streamlit scikit-learn nltk
    ```

3. Download the NLTK data:

    ```python
    import nltk
    nltk.download('punkt')
    nltk.download('stopwords')
    ```

## Files

- `app.py`: The main application file.
- `clf.pkl`: The pre-trained classification model.
- `tfidf.pkl`: The pre-trained TF-IDF vectorizer.

## Usage

1. Ensure you have the `clf.pkl` and `tfidf.pkl` files in the same directory as `app.py`.

2. Run the Streamlit app:

    ```bash
    streamlit run app.py
    ```

3. Open the provided local URL in your web browser.

4. Upload a resume in `.txt` or `.pdf` format.

5. The app will display the predicted category of the uploaded resume.

## Functionality

### `clean_resume(resume_text)`

Cleans the input resume text by removing URLs, special characters, and extra whitespace.

### `main()`

The main function of the Streamlit app which:

- Sets the title of the app.
- Provides a file uploader for the user to upload a resume.
- Reads and cleans the uploaded resume.
- Transforms the cleaned resume text using the TF-IDF vectorizer.
- Predicts the category of the resume using the classification model.
- Displays the predicted category to the user.

### Category Mapping

The app maps the predicted category ID to a category name using the following dictionary:

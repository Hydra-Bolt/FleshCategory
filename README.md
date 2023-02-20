# Text Classification with spaCy

This project trains a spaCy model to perform multi-label text classification on a cleaned English dataset, using a one-hot encoding approach for the target labels. The trained model can then be used to predict the category probabilities for new text inputs in the same format.

## Getting Started

1. Clone this repository to your local machine.
2. Install the necessary libraries by running `pip install -r requirements.txt` in your terminal.
3. Download the cleaned English dataset as a CSV file and save it in the project directory.
4. Update the filename and label column name in the script `train_spacy_model.py` to match your dataset.
5. Run the script `train_spacy_model.py` in your terminal to train the spaCy model and save it to disk as a directory.
6. To use the trained model for prediction on new text inputs, load the saved model using the `spacy.load()` function, and process the text inputs using the loaded model.

## Prerequisites

- Python 3
- `spacy` library
- `pandas` library
- `sklearn` library

## Dataset

The cleaned English dataset used in this project is a CSV file containing two columns: 'text' and 'category'. The 'text' column contains the cleaned English text data, and the 'category' column contains the one-hot encoded labels for each category.

## Training the Model

The `train_spacy_model.py` script reads in the cleaned English dataset as a Pandas dataframe, creates one-hot encoded labels, and splits the data into training and testing sets. It then creates a blank spaCy model for German language processing, adds a text categorization component to it, and trains the component on the training data using minibatch training. After training, the trained model is saved to disk as a directory for future use.

## Predicting with the Model

To use the trained model for prediction on new text inputs, first load the saved model using the `spacy.load()` function and the path to the saved directory. Then, process the text input using the loaded model to obtain a `Doc` object, and access the predicted category probabilities using the `doc.cats` attribute.

## Author

- Muneeb Ahmed

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

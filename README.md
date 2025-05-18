# Resume-Information-Extractor-using-Spacy

# Resume Data Extraction and Processing

This project utilizes a custom Spacy model to extract key information from resumes, specifically focusing on data read from a CSV file. The process involves loading a pre-trained Spacy model, reading resume data from a CSV, applying the model to identify and extract relevant entities, and organizing the extracted information for further use.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Concepts Used](#concepts-used)
- [Project Structure](#project-structure)
- [Sample Data](#sample-data)
- [Acknowledgements](#acknowledgements)
- [License](#license)

## Installation

To run this notebook, you need to have the necessary libraries installed. You can install them using pip:

bash !pip install spacy-transformers==1.2.5 !pip install fitz==0.0.1.dev2 !pip install transformers==4.37.2 !pip install ipython==7.34.0 !pip install PyMuPDF==1.23.12

You will also need to download and place the pre-trained Spacy model in the specified path: `/content/drive/MyDrive/Model for 1panel/assets/ResumeModel/output/model-best`. Ensure you have Google Drive mounted in your Colab environment if the model is stored there.

## Usage

1.  **Clone the repository:** If you are using this in a local environment, clone the repository to your machine. In Google Colab, you can simply use the notebook directly.
2.  **Ensure the Spacy model is in the correct path:** Make sure the `model-best` directory from your pre-trained Spacy model is located at `/content/drive/MyDrive/Model for 1panel/assets/ResumeModel/output/`.
3.  **Provide the input CSV file:** Place your `Sample data.csv` file in the `/content/` directory of your Colab environment or update the path in the code to where your file is located.
4.  **Run the notebook cells:** Execute each cell in the notebook sequentially.

The notebook will perform the following steps:
*   Install dependencies.
*   Load the Spacy resume parsing model.
*   Read data from `Sample data.csv`.
*   Process each row of the CSV data with the Spacy model.
*   Print the extracted entities and their labels.
*   Store the extracted entities in a dictionary.
*   Create a concatenated string of the extracted values.

## Concepts Used

*   **Spacy:** A powerful open-source library for advanced Natural Language Processing (NLP) in Python. It is used here for named entity recognition (NER) to extract specific information from resume text.
*   **Spacy Transformers:** This extension allows Spacy to utilize transformer models (like BERT, GPT-2, etc.) for better performance in various NLP tasks, including NER.
*   **Pre-trained Spacy Model:** A Spacy model that has been trained on a specific dataset (in this case, resume data) to perform particular tasks (like identifying skills, education, etc.).
*   **Named Entity Recognition (NER):** A subtask of information extraction that seeks to locate and classify named entities in text into pre-defined categories such as person names, organizations, locations, medical codes, time expressions, quantities, monetary values, percentages, etc. In this project, the entities are specific to resume components.
*   **PyMuPDF / fitz:** Libraries used for working with PDF documents. While the current code reads from a CSV, these libraries would be essential if the input were PDF resume files.
*   **CSV Processing:** Reading and processing data from a Comma Separated Values file.
*   **Python Dictionaries:** Used to store and organize the extracted entities with their corresponding labels.

## Project Structure

This project primarily consists of a single Google Colab notebook.

. ├── Resume_Data_Extraction_and_Processing.ipynb # The main notebook 
  └── Sample data.csv # Input CSV file



(Note: The Spacy model directory is assumed to be in your Google Drive as specified in the code.)

## Sample Data

The notebook expects an input file named `Sample data.csv`. This file should contain the resume data that you want to process. The current code reads one row at a time and processes it.

## Acknowledgements

*   This project relies on the Spacy library and potentially pre-trained transformer models.

## License

This project is open source and available under the [MIT License](https://opensource.org/licenses/MIT).

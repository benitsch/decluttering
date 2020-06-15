## Setup your environment to run the code
1. Install 64 Bit version of Python at https://www.python.org/downloads/
2. Install pandas for csv file read 
	- pip install pandas
3. Install spaCy and its EN language model (NLP tool). Only works for 64 Bit Python!
	- pip install -U spaCy
	- python -m spacy download en_core_web_sm
4. Install javalang	
	- pip install javalang

## Code
### download_code.ipynb
- Download the Java files from GitHub

### preprocess_data.ipynb
- Filters the comments with spaCy (remove PUNCT and DET)
- Split camelCase words
- Replace symbols with ' '
- Remove single char words
- Remove duplicate spaces in the comment
- Write all to lower case
- Remove URLs from the comment
- Replace defined words with defined words

### extract_comment_and_code.ipynb
- Extract the comment and first code line and saves into oneLineCode.csv (with columns: id, type, comment, code, non-information/Expected) and create a new csv file only with the columns comment, code and non-information/Expected to newFile.csv

### train.ipynb
- Machine learning (Embedding, CNN, RNN)
- Training with provided data
- Output: Result for test set (Kaggle challenge)

## General
### There are three different types of java comments:
1. Inline comments
2. Multi-line comments
3. JavaDoc comments (usually also multi-line)

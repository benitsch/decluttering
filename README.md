## Setup your environment to run the code:

1. Install 64 Bit version of Python at https://www.python.org/downloads/
2. Install pandas for csv file read 
	- pip install pandas
3. Install spaCy and its EN langauge model (NLP tool). Only works for 64 Bit Python!
	- pip install -U spaCy
	- python -m spacy download en_core_web_sm
4. Install javalang	
	- pip install javalang

## Code:
### mian.ipynb
- Filters the comments with spaCy (remove PUNCT, DET, AUX)
- Split camelCase words
- Replace symbols with ' '
- Remove single char words
- Remove duplicate spaces in the comment
- Write all to lower case
- Remove URLs from the comment
- Replace defined words with defined words

### DownloadCode.ipynb
- Download the Java files from GitHub

### get_code2.ipynb
- Extract the comment and first code line and saves into new csv file

### train.ipynb

### Word2vecs.ipynb

### data.ipynb

### getCodeAsBlock.ipynb


## General:
### There are three different types of java comments:
1. Inline comments
2. Multi-line comments
3. JavaDoc comments (usually also multi-line)

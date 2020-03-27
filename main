import pandas as pd
import spacy
import time


# Load dataset
url = "assets/declutter-gold_DevelopmentSet.csv"

#define column lables
names = ['id', 'type', 'path_to_file', 'begin_line', 'link_to_comment', 'comment', 'non-information']

#na_filter = false, because pandas read empty string as float (nan)!
#skiprows = 1, because the first row contains only the labels
dataframe = pd.read_csv(url, names=names, skiprows = 1, na_filter = False)



#load EN model to analyse sentences in english language
nlp = spacy.load("en_core_web_sm")

start_time = time.time()
# Get all values from the column "comment" and print
columns =  dataframe['comment'].tolist()
for idx, val in enumerate(columns):
	print(idx, val)
	print()
	doc = nlp(val)
	print([(w.text, w.pos_) for w in doc])
	print()

elapsed_time = time.time() - start_time
print(elapsed_time)


#Print all rows and not only the first 5 and the last 5
#pd.set_option('display.max_rows', None)

#other option settings if necessary:
#pd.set_option('display.max_columns', None)
#pd.set_option('display.width', None)
#pd.set_option('display.max_colwidth', -1)

# Only print comment and non-information column
#print(dataframe[['comment', 'non-information']])
#print(dataframe[['comment']])

# Print all information from csv file in a DataFrame (table object)
#print(dataframe)
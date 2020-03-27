Setup your environment to run the code:

1.) Install 64 Bit version of Python at https://www.python.org/downloads/
2.) Install pandas for csv file read
pip install pandas
3.) Install spaCy and its EN langauge model (NLP tool). Only works for 64 Bit Python!
pip install -U spaCy
python -m spacy download en_core_web_sm



Code:
The line number and the comment are printed. The syntax of the comment is also analyzed (via spaCy) and printed.
Duration: ~10.7 Sec.



Questions:
1.) Are the comments always in english? If not we should use the xx language model.
python -m spacy download xx_ent_wiki_sm
2.) How can we get Java soure code from a GitHub url in python?
3.) What tools/libraries are available in Python to analyse Java source code?



General:
There are three different types of java comments:
1.) inline comments
2.) multi-line comments
3.) JavaDoc comments (usually also multi-line)
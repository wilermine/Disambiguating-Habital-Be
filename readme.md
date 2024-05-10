# Leveraging syntactic dependencies in disambiguation: the case of African American English
## Habitual Be Tagger and Model Generator

**Authors:** Wilermine Previlon, Alice Rozet, Jotsna Gowda, William Dyer, Kevin Tang, and Sarah Moeller
**Date: 5.10.2024*

###Required Librariies

- import spacy
- nlp = spacy.load("en_core_web_sm")


- import pandas as pd
- import re

- import sklearn
- from sklearn.feature_extraction.text import CountVectorizer
- from sklearn.model_selection import StratifiedKFold, cross_val_predict, cross_val_score
- from sklearn.metrics import confusion_matrix, ConfusionMatrixDisplay, classification_report
- from sklearn.naive_bayes import MultinomialNB
- from sklearn.preprocessing import StandardScaler
- from sklearn.linear_model import LogisticRegression
- from sklearn.neural_network import MLPClassifier
- from sklearn.ensemble import VotingClassifier
- from sklearn.pipeline import Pipeline, make_pipeline
- from sklearn.svm import SVC, LinearSVC


- import nltk
- #nltk.download("stopwords")
- #nltk.download("wordnet")
- from nltk.corpus import stopwords
- from nltk.stem import WordNetLemmatizer
- from nltk.data import load
- #nltk.download('tagsets')
- tagdict = load('help/tagsets/upenn_tagset.pickle')

- import joblib
- import pylab as pl
- import copy
- import csv
- import numpy as np

## Project Structure
- Data
	
- Scripts
	- *Habitual Rule Tagger.ipynb* - Tags a corpus of sentences containing "be" as habitual or non-habitual according to our rule-based method
	- *Habitual Model Generator.ipynb* - Uses output from the Habitual Rule tagger to create and export a classification model that classifies sentences containing "be" as habitual or non-habitual.

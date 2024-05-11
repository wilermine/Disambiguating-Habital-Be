# Leveraging syntactic dependencies in disambiguation: the case of African American English
[*Link to Prepint*](https://osf.io/preprints/psyarxiv/ph7q8)

**Authors:** Wilermine Previlon, Alice Rozet, Jotsna Gowda, William Dyer, Kevin Tang, and Sarah Moeller

**Date: 5.10.2024**

### Project Description / Abstract:

African American English (AAE) has received recent attention in the field of natural language processing (NLP). Efforts to address bias against AAE in NLP systems tend to focus on lexical differences. Whenever the structural uniqueness of AAE is considered, the solution is often to remove or neutralize the differences. This work leverages knowledge about the unique morphosyntactic structures to improve automatic disambiguation of habitual and non-habitual meanings of “be” in naturally produced AAE transcribed speech. Both meanings are employed in AAE but examples of Habitual be are rare in the already limited AAE data. Generally, representing contextual syntactic information improves semantic disambiguation of habituality. Using an ensemble of classical machine learning model swith a representation of the unique POS and dependency patterns of Habitual be, we show that integrating syntactic information improves the identification of habitual uses of “be” by about 65 F1 points over a simple baseline model of n-grams, and as much as 74 points. The success of this approach demonstrates the potential impact when we embrace, rather than neutralize, the structural uniqueness of African American English.

### Requirements
See `requirements.txt` for a full list of requirements which can be installed using [pip](https://packaging.python.org/en/latest/tutorials/installing-packages/#use-pip-for-installing) and a [virtual environment](https://docs.python.org/3/tutorial/venv.html).

### Running the Project
This project aims to classify sentences containing a single "be" are either a habitual or non-habitual usage. 

#### Scripts

*Habitual Rule Tagger.ipynb* should be ran first. It takes in a corpus of sentences containing a single "be" and tags classifies them according to our rule-based method. If you simply want to annotate a corpus for the habitual *be*, this script accomplishes this on its own.

*Habitual Model Generator.ipynb* generates an automatic classification model, improving on the rule-based method. This script takes the output from the Habitual Tagger and a gold standard annotated data set to develop an ensemble classification model.

#### Data

*SPOHP Sentences.txt:* Sentences containing habitual and non-habitual be from the Samuel Proctor Oral History Program that were used in the development of the rule-based method (9296 sentences).

*CORAAL (no labels).txt:* Unlabeled sentences containing habitual and non-habitual be from the Corpus of Regional African American English. Data that was unseen during our development to test the accuracy of the classification models (4531 sentences).

*CORAAL (gold standard).txt:* Same as above but hand annotated to act as the gold standard for training and testing.

#### Models
*cv.joblib*: Current version of the Count Vectorizer model used for n-grams.

*n-gram.joblib*: Current version of the n-gram model, fed in as input for the habitual model.

*habituality_model.joblib*: Current version of the habitual model.

### Project Structure
- readme.md
- requirements.txt
- data
	- SPOHP Sentences.txt
   	- CORAAL (no labels).txt
   	- CORAAL (gold standard).txt 
- scripts
	- Habitual Rule Tagger.ipynb
	- Habitual Model Generator.ipynb
- models
  	- cv.joblib
  	- habituality_model.joblib
  	- n_gram.joblib

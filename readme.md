# Leveraging syntactic dependencies in disambiguation: the case of African American English
## Habitual Be Tagger and Model Generator
[*Link to Prepint*](https://osf.io/preprints/psyarxiv/ph7q8)

**Authors:** Wilermine Previlon, Alice Rozet, Jotsna Gowda, William Dyer, Kevin Tang, and Sarah Moeller
**Date: 5.10.2024*

### Project Description / Abstract:

African American English (AAE) has received recent attention in the field of natural language processing (NLP).Efforts to address bias against AAE in NLP systems tend to focus on lexical differences. Whenever the structuraluniqueness of AAE is considered, the solution is often to remove or neutralize the differences. This work leveragesknowledge about the unique morphosyntactic structures to improve automatic disambiguation of habitual and non-habitual meanings of “be” in naturally produced AAE transcribed speech. Both meanings are employed in AAE butexamples of Habitualbeare rare in the already limited AAE data. Generally, representing contextual syntactic infor-mation improves semantic disambiguation of habituality. Using an ensemble of classical machine learning modelswith a representation of the unique POS and dependency patterns of Habitualbe, we show that integrating syntacticinformation improves the identification of habitual uses of “be” by about 65 F1points over a simple baseline modelof n-grams, and as much as 74 points. The success of this approach demonstrates the potential impact when weembrace, rather than neutralize, the structural uniqueness of African American English.

### Requirements
See `requirements.txt` for a full list of requirements which can be installed using [pip](https://packaging.python.org/en/latest/tutorials/installing-packages/#use-pip-for-installing) and a [virtual environment](https://docs.python.org/3/tutorial/venv.html).

### Running the Project
This project aims to classify sentences containing a single "be" are either a habitual or non-habitual usage. The task is broken into two scripts:

*Habitual Rule Tagger.ipynb* should be ran first. It takes in a corpus of sentences containing a single "be" and tags classifies them according to our rule-based method. 
## Project Structure
- Data
	
- Scripts
	- *Habitual Rule Tagger.ipynb* - Tags a corpus of sentences containing "be" as habitual or non-habitual according to our rule-based method
	- *Habitual Model Generator.ipynb* - Uses output from the Habitual Rule tagger to create and export a classification model that classifies sentences containing "be" as habitual or non-habitual.

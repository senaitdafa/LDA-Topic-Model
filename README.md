# LDA Unsupervised Topic Model 

This project identifies salient themes from news articles collected by GDELT in Sierra Leone.
It contains two notebooks: 

  1.) extract_content.ipynb: Extracts text from online documents and articles.
  
  2.) topic_model.ipynb: Identifies the most common themes from the extracted textual data above.
  
## Requirements
#### System:
- Python 3 or higher
- pyLDAvis 3.3.1
- spacy

#### Packages:
**Content Extraction**:\
-import warnings\
-import pandas as pd\
-from datetime import * \
-from goose3 import Goose\
-import csv\
-import time


**Topic Model**:\
-import re\
-import nltk \
-from nltk.corpus import stopwords\
-import pyLDAvis\
-import pyLDAvis.gensim_models\
-import gensim\
-from gensim import models, similarities\
-import gensim.corpora as corpora\
-from gensim.corpora import Dictionary\
-from gensim.models.coherencemodel import CoherenceModel\
-from gensim.models.ldamodel import LdaModel\
-import re \
-import pyLDAvis\
-import pyLDAvis.gensim_models\
-import matplotlib.pyplot as plt \
-import spacy

## Setup
Open the project directory and verify that these six items are present:
- `README.md`
- `topic_model.ipynb`
- `extract_content.ipynb`
- `fuzzy_matching.html`
- `UpennBox_SL_2020_content_extracted.csv`

## Input data
### Content Extraction
-The content extration input is called `2020.csv`, and is included in the top level of this repository

### Topic Model
-The topic model input is called `UpennBox_SL_2020_content_extracted.csv` and is also included in this repository. This model was developed for a dataset contatining news articles from Sierra Leone in 2020. This file can be replaced with similar GDELT article data. 


## Results
The quality of the topics changes with the number of topics that we choose to identify for the model. Our goal was to find high quality, coherent topics that don’t have overlap or repeat. We produced and compared  the coherence score of 20 models, which is depicted in the graph below. We identified 3 models with high coherence scores: models with 6, 10, and 19 topics.


After examining the three models, we found that a model 10 topics to have the best coherence. We also were able to find the “dominant topic” for each article in the dataset. Each topic is a collection of keywords, from this, we can manually infer the topic name. Below is the output of the optimal model: it displays each topic, the keywords that describe the topic, the number of documents described by the dominant topic, and the percentage representation of the topic weight in the dataset. 

The visualization below is our qualitative interpretation of the topic labels, inferred from the keywords and their weights:
![Untitled Diagram](https://user-images.githubusercontent.com/29438079/165037857-17e0717a-344e-4bb3-92dc-1afe96dfa0fa.png)



## Usage
### Content Extraction
I have indcluded this code to assist with abstracting the topic model in the future. The output of this notebook on the GDELT 2020 Sierra Leone data is already included in this repository as, "UpennBox_SL_2020_content_extracted.csv". 

1. Verify existence of Input File in your repository:
   - A CSV dataset GDELT of news articles.
2. Configure execution settings:
   - Set the INPUT_CSV to your relative file path
   - Change start or end date for the articles, batch size, or output name. Further detail is included within the code itself. 
3. Execute:
   - Press "Run All Cells"

4. Confirm generation of output file:
   - Final output is saved as `OUTPUT.csv` in the `./output` directory.

### Topic Model
1. Verify existence of Input File in your repository:
   - A CSV dataset GDELT of news articles.
2. Configure execution settings:
   - Set the INPUT_CSV to your relative file path
3. Execute:
-    - Press "Run All Cells"

## Next steps
- Separate the interface and the implementation for the topic model code to allow for ease of abstraction
- Test implementation viability  on larger datasets such as longer time periods or multiple countries.


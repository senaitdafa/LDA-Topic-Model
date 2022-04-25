# LDA Unsupervised Topic Model 

This project identifies salient themes from news articles collected by GDELT in Sierra Leone.
It contains two notebooks: 
  1.) extract_content.ipynb: Extracts text from online documents and articles.
  2.) topic_model.ipynb: Identifies the most common themes from the extracted textual data above.
Video demo: 

## Requirements
#### System:
- Python 3 or higher
- pyLDAvis 3.3.1
- spacy

#### Packages:
Content Extraction:
Topic Model:

## Setup
Open the project directory and verify that these six items are present:
- `README.md`
- `topic_model.ipynb`
- `extract_content.ipynb`
- `fuzzy_matching.html`
- `./input`
- `./output`
 
## Input data
Save a CSV file of a GDELT database query of news articles in the `./input` folder. This model was developed for 2020 Sierra Leone Data, and the original input file can be found in the ./input folder.


## Results
The quality of the topics changes with the number of topics that we choose to identify for the model. Our goal was to find high quality, coherent topics that don’t have overlap or repeat. We produced and compared  the coherence score of 20 models, which is depicted in the graph below. We identified 3 models with high coherence scores: models with 6, 10, and 19 topics.


After examining the three models, we found that a model 10 topics to have the best coherence. We also were able to find the “dominant topic” for each article in the dataset. Each topic is a collection of keywords, from this, we can manually infer the topic name. Below is the output of the optimal model: it displays each topic, the keywords that describe the topic, the number of documents described by the dominant topic, and the percentage representation of the topic weight in the dataset. 

The visualization below is our qualitative interpretation of the topic labels, inferred from the keywords and their weights:



## Usage
### Content Extraction
1. Verify there are two files in the `./input` folder:
   - A CSV dataset GDELT of news articles.
2. Configure execution settings:
   - Set the GDELT_INPUT relative file path
   - Set the number and range of GDELT rows to process; each row represents one article, and the number of articles is the difference between the start and end rows.
3. Execute:
   - Press "Run All Cells"

4. Confirm generation of output file:
   - Final output is saved as `OUTPUT.csv` in the `./output` directory.

### Topic Model
 1. Intial Setup

 
## Next steps
- Separate the interface and the implementation for the topic model code to allow for ease of abstraction
- Test implementation viability  on larger datasets such as longer time periods or multiple countries.


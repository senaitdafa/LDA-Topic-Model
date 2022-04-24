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
todo

## Usage
### Content Extraction
1. Verify there are two files in the `./input` folder:
   - A CSV dataset GDELT of news articles.
2. Configure execution settings:
   - Set the GDELT_INPUT relative file path
   - Set the number and range of GDELT rows to process; each row represents one article, and the number of articles is the difference between the start and end rows.
3. Execute:
   - Press "Run All Cells"
   - The output data is saved in the `./output` folder in CSV format.
   - If execution stops, it can be resumed by starting at the most recent cell that loads a progress output file.
   - Keep the saved progress output files to avoid unnecessary re-execution of all cells.

4. Confirm generation of output file:
   - Final output is saved as `OUTPUT.csv` in the `./output` directory.

### Topic Model
 1. 
 

## Additional notes
todo

## Next steps
- Separate the interface and the implementation for the topic model code to allow for ease of abstraction
- Test implementation viability  on larger datasets such as longer time periods or multiple countries.


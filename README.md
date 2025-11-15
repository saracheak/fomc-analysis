# Sentiment Analysis on FOMC Statement

### Credits
This sentiment analysis was based on the ProsusAI model, which can be found at this github link: https://github.com/ProsusAI/finBERT

### Installation
Follow the instructions here for installing libraries https://github.com/ProsusAI/finBERT/blob/master/README.md 

### Model
The dataset used for this FinBert sentiment analysis was the Financial PhraseBank from Malo et al. (2014). The dataset can be downloaded from this [link](https://www.researchgate.net/profile/Pekka_Malo/publication/251231364_FinancialPhraseBank-v10/data/0c96051eee4fb1d56e000000/FinancialPhraseBank-v10.zip?origin=publication_list). 

### Input
The input for this model was the FOMC statement from March 2025 titled "Statement on Longer-Run Goals and Monetary Policy Strategy", which can be found at this [link](https://www.federalreserve.gov/monetarypolicy/files/FOMC_LongerRunGoals.pdf). The contents of this file is in `./fomc-report.txt`.  

### Running the code
Navigate to root folder and run the following code in the command line:
``` python
python -m scripts.predict --text_path fomc-report.txt --output_dir output/ --model_path models classifier_model/finbert-sentiment
```

### Output
Output file is in `output/prediction.csv` and is described by 'negative', 'neutral', or 'positive' for each sentence.

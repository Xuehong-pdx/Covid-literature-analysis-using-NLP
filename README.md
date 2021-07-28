# search-covid-literature-using-NLP
<b> Getting info from over 100K papers on covid using NLP </b>

Pubmed is a free search engine accessing primarily the MEDLINE database of references and abstracts on life sciences and biomedical topics.  
A simple search for 'covid-19' on pubmed resulted in 156,871 citations, an impossible number of papers for anyone to seep through.  
I set out to see whether I can get some kind of understanding of the literature using natural language processing.

The data were downloaded from pubmed after search for covid-19

Approaches:
1. Data Cleaning.  records with null values, abstracts ith length less than 50 words (not true abstracts after visual inspection) are removed
2. stop words were removed
3. Lemmatization was performed
4. Most frequent used words are ranked
5. WordCloud are used for better visualization of most used owrds
6. Model was trained to predict ducument labels to identify types of studies performed
7. Topic Modeling was performed using Latent Dirichlet Allocation technique
8. Recommeding collection of articles based on the the appearance of top words for each topic 

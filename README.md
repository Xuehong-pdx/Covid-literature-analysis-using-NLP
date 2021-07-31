# search-covid-literature-using-NLP
<b> Introduction </b>

Pubmed is a free search engine accessing primarily the MEDLINE database of references and abstracts on life sciences and biomedical topics.  
A simple search for 'covid-19' on pubmed resulted in 156,871 citations, an impossible number of papers for anyone to seep through.  
I set out to see whether I can get some kind of understanding of the trend in literature using natural language processing.

The data were downloaded from pubmed after search for covid-19

<b> Approaches: </b>
1. Cleaning data .  Records with null values, abstracts ith length less than 50 words (not true abstracts after visual inspection) are removed
2. Removing stopwords
3. Perfirming lemmatization
4. Ranking most frequently used words
5. Visualizing most used words using WordCloud 
6. Predicting ducument labels to identify types of studies performed
7. Topic Modeling using Latent Dirichlet Allocation technique
8. Recommeding collection of articles based on top words for each topic 

<b>Summary</b>

1. In this study, I imported csv fiels from pubmed that contains the dumped data for 2019-2020.  Three types of analysis were performed to get some insight on covid literature.

2. The first attempt was to examine the top words in the whole data set to see what insights one might be able to infer from the data.  I found that one can get a sense of what was discussed based on top words.  But, there is limit to get indepth information based on top words.

3. Next I took the advange of train test and validate data sets that have prelabels for the type of study for the abstract.  I tranied a SVC and predicted the labels for the test and validation data sets.  The labels in the train set has one or more labels.  The model was able to make about 44% correct predictions if one consider as long as the predicted label is one of the words in the set, it is a correct prediction.  A detailed examination of the result shown that this approach was not ddsirable since one only one label was predicted by the model.  To do this properly, the labels should be reexamined and cleaned.  

4. Thirdly, I performed topic modeling using Latent Dirichlet Allocation (LDA) method.  Since the original data sets has eight differnt labels, I first performed the analysis using 8 topics.  Then also tried 15 topics.  Based on the top ten words for the mostly discussed topic, I concluded that 8 topics is sufficient for teasing out the difference in topics.  BAsed on this analysis, it is possible to pick out papers that disccuss certain topics.  

5. Based on the results, WordNet Lemmatizer didn't do a good job removing the stem of some words.

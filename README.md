## Adverse Drug Reaction Classification on Twitter corpus

Adverse Drug Reactions (ADRs) are a major concern to the public health and results in thousands of incidents of death and serious injuries to the patients. Most of these deaths and injuries are believed to be preventable if an ADR is diagnosed early enough to be acted upon it. Social media is a source where people provide personal information about every aspect of their lives, including healthcare. Therefore, social media becomes an important tool for pharmacovigilance. This project focuses on using Natural Language Processing(NLP) and Machine Learning(ML) techniques to identify ADRs from the tweets posted by the users on their Twitter accounts. A feature super-set has been created by accumulating different features sets from the Tweets to attack the problem as a Binary Classification task.

#### Dataset -

* Twitter corpus is taken from Sarker, A., Gonzalez, G.: Portable automatic text classification for adverse drug reaction detection via multi-corpus training. Journal of biomedical informatics 53 (2015) 196-207 and can be downloaded from http://diego.asu.edu/index.php?downloads=yes

* Dataset folder contains **sentiment_score_dic_with_pmi.txt** for Sentiment score with PMI.

* Dataset contains following lexicon files -
  1. Sentiment lexicons
    * SentiWordnet 3.0
      
      article - Baccianella, S., Esuli, A., Sebastiani, F.: Sentiwordnet 3.0: An enhanced lexical resource for sentiment analysis and opinion mining. In: LREC. Volume 10. (2010) 2200-2204
      download - http://sentiwordnet.isti.cnr.it/

    * MPQA Subjectivity Lexicon
      
      article - Wilson, T., Wiebe, J., Hoffmann, P.: Recognizing contextual polarity in phraselevel sentiment analysis. In: Proceedings of the conference on human language technology and empirical methods in natural language processing, Association for Computational Linguistics (2005) 347-354
     download - https://github.com/kuitang/Markovian-Sentiment/blob/master/data/subjclueslen1-HLTEMNLP05.tff

  2. Word vector representation
    * Word2vec model
    
      article - Miftahutdinov Z. S., Tutubalina E. V., Tropsha A. E. Identifying disease-related expressions in reviews using conditional random fields //Komp’juternaja Lingvistika i Intellektual’nye Tehnologii. – 2017. – Т. 1. – №. 16. – С.     155-166.
      download - https://github.com/dartrevan/ChemTextMining/tree/master/word2vec/Health_2.5mreviews.s200.w10.n5.v15.cbow.bin

#### Requirements to run the code -
* Python version - 3.6 or above
* Libraries needed - 
  * NLTK Version 3.5
  * Gensim Version 3.5 or above
  * TextBlob Version 0.15
  * NumPy Version 1.11
  * scikit-learn version 0.21
  * Pandas Version 1.0.3
  * Scipy Version 1.4.1
  * Codecs Version 1.0 or above
  
 #### Steps to run the code -
 1. Pre-trained model **Health_2.5mreviews.s200** is used for word2Vec features. Health_2.5mreviews.s200 is required by ADR_Classification_on_Twitter_Data.ipynb file. This is available at https://github.com/dartrevan/ChemTextMining/tree/master/word2vec/Health_2.5mreviews.s200.w10.n5.v15.cbow.bin.
 2. Run ADR_Classification_on_Twitter_Data.ipynb to read the dataset and generate features for each tweet. Result for SVM and LR classifiers will generate results once feature extraction is completed. 
 
 ### IMPORTANT NOTE -
 The code has been written on Google Colab and it is advised to run the code on Colab as well.

This is a project for Text Analytics for Psychological-Information Research

## MAIN IDEA

The main idea is to aggregate resources here that a computational social scientist might use to analyse psychological aspects within text data. 
Assuming you have a large chunnk of text data that you want to parse, here are some helpful tips for you

## RELEVANT TOOLS

**Preprocessing**, **extracting a sample for annotations**
https://github.com/Telentovj/tpp

**Post-processing, Text Summarisation, Time series dashboard**
https://github.com/Jcheez/capstone-nlp

## IPYNB FILES
Here there are four .ipynb files that can be used for: 
 + extracting named entities within a text

 + doing weak supervision to get emotion and stance labels [I have done it in the fake news detection setting]

 + finding the agreement between classifiers

  + sentence pair classification: given a text and features, predict the subsequent label. In my use case. given a document, a target, the emotion, and the stance, predict if the text is fake news or not
  
## Recipes for projects

Assuming that you have collected a large chunk of text data and you want to train a classifier to label it by topics.
 step 1: use the preprocessing code to split into probable topics and it can extract a representative sample from the text data
 step 2: relabel your data into various topics (e.g., for hate speech: us-versus-them, death threats, etc.)
 step 3: train the relabelled data on a ML classifier. If the F1 is around or above >.8, you can try to use that dataset for classification
     step 3.5: When accuracy is not ideal, usually the solutions are to ensure that the dataset is balanced or add more data

Assuming that you want to summarise a transcript, put it in a text file and use the postprocessing file

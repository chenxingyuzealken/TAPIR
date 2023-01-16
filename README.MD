This is a project for Text Analytics for Psychological-Information Research

## MAIN IDEA

The main idea is to aggregate resources here that a social scientist might use to mine insights from text data to answer social science questions. 
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

RECIPE: TEXT CLASSIFICATION
Assuming that you have collected a large chunk of text data and you want to train a classifier to label it by topics. <br />
 step 1: use the preprocessing code to split into probable topics and it can extract a representative sample from the text data <br />
 step 2: relabel your data into various topics (e.g., for hate speech: us-versus-them, death threats, etc.) <br />
 step 3: train the relabelled data on a ML classifier. If the F1 is around or above >.8, you can try to use that dataset for classification on unseen data <br />
     step 3.1: When accuracy is not ideal, usually the solutions are to ensure that the dataset is balanced or add more data <br />
     step 3.1.1 An imbalanced dataset comes about when you have usually one class that has around 2x more records than another class. This would bias the model towards predicting that class <br />. Solutions for that include SMOTE or topping up the data <br />.
     step 3.2: Adding more data can be done by either using a classifier to add more data <br />.

RECIPE: TEXT SUMMARISATION <br />
 Assuming that you want to summarise a transcript, put it in a text file and use the postprocessing code and select the option to summarise the data <br />

 It can be useful for quickly sensitising yourself to the brief details of the content <br />

 You could also use topic modelling methods like top2vec and then summarise the content within each and every topic. This will probably give you a more
 granular understanding of your data <br />
<br />

 
RECIPE: EMOTION/STANCE CLASSIFICATION<br />

 This is the same for text classification, except that the categories are fixed (anger, fear, sad, happy, AGAINST or FAVOR etc.) <br />

 I would recommend users to use Aspect-based classification for more fine-grained analysis <br />

 Step 1: Extract the entities using NER. Then select entities of interest <br />

 Step 2: You could use emotion/stance classifiers that are available and get the labels which both classifiers agree upon. <br />
   step 2.1: In the literature, this step is known as weak supervision. I know we can try zero-shot, but zero-shot classification can be slow, 
     although I have not experimented with it yet
 
 Step 3: train the predicted data on a ML classifier. If the F1 is around or above >.8, you can try to use that dataset for classification on unseen data <br />


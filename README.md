# Cleaning-Parsing-and-Processing-Tweets
Parsing Text Files and Text Pre-Processing Extracting tweet id's, tweets and their creation date time from a large dataset of text file (by just using the below mentioned libraries): Reading the file, cleaning it, extracting only the unique tweets that are English, and writing it to an XML file. Generate corpus vocabulary, Calculate top 100 frequent unigram and top 100 frequent bigrams, Generate a sparse representation of the excel file

# Task 1: Parsing Text Files
This task touches the very first step of analyzing textual data, i.e., extracting data from semi-structured text files. The data-set provided consists of COVID-19 tweets. Each text file contains information about the tweets, i.e., “id”, “text”, and “created_at” attributes.
The task is to extract the data and transform the data into the XML format with the following elements:
1. id: is a 19-digit number.
2. text: is the actual tweet.
3. Created_at: is the date and time that the tweet was created

# Task 2: Text Pre-Processing
This task touches on the next step of analyzing textual data, i.e., converting the extracted data into a proper format. This task consists of Python code to preprocess a set of tweets and convert them into numerical representations (which are suitable for input into recommender-systems/ information-retrieval algorithms).

The data-set provided contains 80+ days of COVID-19 related tweets (from late March to mid July 2020). The task is to extract and transform the information of the excel file performing the following task:
1. For each day (i.e., sheet in your excel file), calculate the top 100 frequent unigram and
top-100 frequent bigrams 
2. Generate the sparse representation (i.e., doc-term matrix) of the excel file 

The following steps must be performed (not necessarily in the same order) to complete the task.
1. Using the “langid” package, only keeps the tweets that are in English language.
2. The word tokenization must use the following regular expression,
"[a-zA-Z]+(?:[-'][a-zA-Z]+)?"
3. The context-independent and context-dependent (with the threshold set to more than
60 days) stop words must be removed from the vocab. The provided
context-independent stop words list (i.e, stopwords_en.txt) must be used.
4. Tokens should be stemmed using the Porter stemmer.
5. Rare tokens (with the threshold set to less than 5 days) must be removed from the
vocab.
6. Creating sparse matrix using countvectorizer.
7. Tokens with the length less than 3 should be removed from the vocab.
8. First 200 meaningful bigrams (i.e., collocations) must be included in the vocab using
PMI measure.

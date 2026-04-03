
# <ins>NLP_Techniques_on_Text_Data</ins>

## **AIM** 
To study, implement, and analyze fundamental text preprocessing and Natural Language Processing (NLP) techniques using Python’s NLTK library to transform raw, unstructured text into a format suitable for computational analysis.<br/>

## **OBJECTIVES** 
* To perform **Text Cleaning** by removing noise such as punctuation and special characters.<br/>
* To execute Tokenization and Stop Word Removal to **isolate meaningful semantic units**.<br/>
* To contrast Stemming and Lemmatization for **word normalization**.<br/>
* To apply Part-of-Speech (POS) Tagging and Frequency Distribution for **structural and statistical analysis**.<br/>

## TOOLS & SOFTWARE
* **Programming Language:** Python 3.x 
* **Environment:** Google Colab / Jupyter Notebook.
* **Libraries:**
    * **NLTK:** For core NLP tasks (Tokenization, Stemming, Lemmatization, POS Tagging).
    * **Pandas/NumPy:** For data manipulation and array handling.

  
## **THEORY** 
### 1. Tokenization
  * **Tokenization:** the foundational step in NLP that involves breaking a raw string of text into smaller units called tokens.<br/>
  * **Word Tokenization:** Splitting a sentence into individual words (e.g., "Natural Language" becomes ['Natural', 'Language']).<br/>
  * **Sentence Tokenization:** Dividing a large paragraph into its constituent sentences based on punctuation cues.<br/>
### 2. Stop Word Removal
Stop words are common words (such as "is", "the", "and", "in") that appear frequently but carry minimal unique semantic information. <br/>
Removing these reduces the noise in the data, allowing the model to focus on the "content" words that define the meaning of the text.<br/>
### 3. Word Normalization: 
#### Stemming vs. Lemmatization
<ins>Both techniques aim to reduce inflectional forms of a word to a common base, but they differ in their approach:</ins><br/>
  * **Stemming:** A rule-based process that chops off the ends of words to find the "stem." It is fast but can result in non-dictionary words (e.g., "studies" becomes "studi").<br/>
  * **Lemmatization:** A more sophisticated process that uses a vocabulary and morphological analysis to return the lemma (dictionary form). It ensures the resulting word is linguistically valid (e.g., "studies" becomes "study").<br/>
### 4. Part-of-Speech (POS) Tagging
POS tagging is the process of marking up a word in a text as corresponding to a particular part of speech based on its definition and context. This helps the system understand the grammatical structure of a sentence. Common tags include:<br/>
  * **NNP:** Proper noun, singular.<br/>
  * **VBZ:** Verb, 3rd person singular present.<br/>
  * **JJ:** Adjective.<br/>
### 5. Word Frequency Distribution
This involves counting the occurrences of each token in a text corpus. <br/>
It is used to identify the most significant words or "keywords" in a document, which is essential for tasks like document summarization or sentiment analysis.<br/>
<br>

## ALGORITHMS
### A. Tokenization (Word & Sentence)<br/>
1. Start.<br/>
2. Input a raw string of text.<br/>
3. Load the **punkt** tokenizer from NLTK.<br/>
4. Apply **sent_tokenize()** to split the paragraph into a list of individual sentences.<br/>
5. Apply **word_tokenize()** to split sentences into a list of individual words/punctuation.<br/>
6. Stop.<br/>
### B. Stop Word Removal<br/>
1. Start.<br/>
2. Define a set of English stop words using **nltk.corpus.stopwords.words('english')**.<br/>
3. Tokenize the input text into a list of words.<br/>
4. Iterate through each word in the list.<br/>
5. Check if the word (in lowercase) exists in the stop words set.<br/>
6. If not in the set, append it to a new **filtered_list**.<br/>
7. Stop.<br/>
### C. Stemming (Porter Stemmer)<br/>
1. Start.<br/>
2. Initialize the **PorterStemmer()** object.<br/>
3. Provide a list of words to be reduced.<br/>
4. For each word, apply the stemming rule (heuristic chopping of suffixes).<br/>
5. Return the resulting "stems" (e.g., "flying" , "fli").<br/>
6. Stop.<br/>
### D. Lemmatization (WordNet)<br/>
1. Start.<br/>
2. Initialize the **WordNetLemmatizer()** object.<br/>
3. Ensure the **wordnet corpus** is downloaded.<br/>
4. For each word, look up its base form in the lexical database.<br/>
5. Return the valid dictionary "lemma" (e.g.: "was" , "be").
6. Stop.
### E. Part-of-Speech (POS) Tagging
1. Start.<br/>
2. Tokenize the input text into words.<br/>
3. Apply the **pos_tag()** function to the word list.<br/>
4. Assign a tag (NN, VB, JJ, etc.) to each token based on context and grammar.<br/>
5. Output the word-tag pairs.<br/>
6. Stop.
### F. Word Frequency Distribution
1. Start.<br/>
2. Tokenize the input text.<br/>
3. Create a **FreqDist** object from the list of tokens.<br/>
4. Count the occurrences of each unique word.<br/>
5. Identify and display the most common words.<br/>
6. Stop.<br/><br>

## **REAL-LIFE APPLICATIONS**
* **Chatbots and Virtual Assistants:** Applications like Siri, Alexa, and Google Assistant use **Tokenization** and **POS Tagging** to parse user commands and provide human-like responses.<br/>
* **Spam Email Detection:** Email services use **Stop Word Removal** and **Word Frequency** **(Bag of Words)** to identify patterns common in spam messages and filter them out of your inbox.<br/>
* **Search Engines:** Google and Bing use **Stemming and Lemmatization** so that if you search for "running shoes," you also get results for "run shoes" or "ran," improving search relevance.<br/>
* **Recommendation Systems:** Streaming platforms like Netflix use **Text Vectorization** to analyze movie descriptions and recommend similar content based on text similarity.<br/>


## **CONCLUSION**  
The preprocessing techniques and NLP techniques used for analyzing text data were studied successfully.


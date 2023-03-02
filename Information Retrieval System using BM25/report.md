# Building a Simple Information Retrieval System using BM25 and GPT-3 and evaluated in the CISI collection.

## How to test the IR system
You need to check the `dataset_folder_path` and use correct path to CISI dataset.
the  ***rank_bm25*** libary is required 
 -- may use pip install rank_bm25
 
### -- implementation details
The code is in python.
Fisrt we read the files from the CISI collection and process the data. The description of each file on CISI dataset is present on it's website <http://ir.dcs.gla.ac.uk/resources/test_collections/cisi/>
    * cisi.all - The documents
    * cisi.que - The queries
    * cisi.rel - Relevance assesments
    * cisi.bln - A list of boolean queries
    
After read all files, we perfomed some prepocessing steps, removing special characters and stop words, and performing also a normalization words process on the texts data

Then, we used the tokenized corpus of words and pass to BM25 API (BM25Okapi).

After this process, given a query data, we can get the computation and BM25 scores of the this data in relation to every item in corpus. Also we can rank the scores and get the top N best.


## How chatGPT helped with the project
ChatGPT was a usefull tool in some steps of this projects. It helped answering questions related to dataset and descriptions of used libraries we didn't know before. Also ChatGPT helped us providing some code syntax.
Some qustions made for ChatGPT:
1. What is bm25 library?
2. How to read data from cisi collection?
3. Give an example of normalization words in python using nltk
4. Give an example of Removing special characters  and numbers in python using regex
# Latent Semantic Index

This book is intended to calculate the latent semantic index in 500 documents to extract the top 5 topics using 10 most related words, extracting the 10 documents most related
to each topic

# Input Files
Please change the name of the path directories in which the data and the models can be saved. This are the
variables named "path#". The docs should be found in a local directory called docs.

# Libraries
Please install libraries required for the Python program to run. In case there is a problem, a google colab
link has been provided inside the code for usage online. It is linked to an open drive that contains the
data used for the analysis. Would require a google account to access it but is open to anyone.

Link:
https://colab.research.google.com/drive/1rXHVlykw__4ytPxVS8J9xs61uCEBnmti?usp=sharing

# Code Description
function reader = reads each file and appends it into a list. Outputs the data and the name of each file. The reader goes through each file in disorder, thus 
the outputs and their contents are accessed through indexes.

function corpus = creates a new dictionary and term-index matrix for the GenSim library. Outputs are the dictionary and the term-index matrix.

function gensim_sli = creates a latent semantix index model from the using the corpus function from the GenSim library. It outputs the model, the right hand side matrix
of the SVD, the dictionary used to create the Bag of Words and a dictionary with the n-top-topics and m-top-words per topic. 

path: strings for local paths were the data is located.

docs, docs_names = outputs from the reader function.

concepts, words = number of concepts and number of words required per concept.

LSI, V, dic, term_matrx, topics_words = outputs from the gensim_sli function.

LSI.projection.s = projected main values from the central diagonal matrix in SVD.

queries = list of queries created from the topics_words dictionary. One list per query.

tf_idf = TfidModel from term_matrix for GenSim similarities.

path2 = location in local directory to save the similarity model.

sims2 = model for finding similarities based on term frequency-inverse document model.

result_docs = indexes of each doc that is a result

finalres = values of the similarities in order highest to smallest.

finaldocs = array with the name of the documents.

# More on LSI

https://nlp.stanford.edu/IR-book/html/htmledition/latent-semantic-indexing-1.html

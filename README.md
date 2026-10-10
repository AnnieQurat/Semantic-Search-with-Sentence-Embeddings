# Semantic Search with Sentence Embeddings

A small weekend project: searching text by **meaning** instead of exact keywords (like ctrl+F) 

I built it to refresh my understanding of embeddings and how semantic search works, working through each step with real numbers.

## What the notebook does
1. Loads a pretrained model (`all-MiniLM-L6-v2`) with the Sentence Transformers library.
2. Turns 12 short sentences (data protection, cooking, cars, football) into embeddings: 384 numbers per sentence.
3. Shows what happens inside one sentence: tokens, token vectors, and averaging into a sentence embedding.
4. Compares all sentences with a colour-coded similarity table.
5. Runs a semantic search: a question is embedded and matched against the sentences.

## Example result
The query *"What rules protect personal data?"* returned the two data-protection sentences as the top matches (similarity 0.76 and 0.64), even though they share few exact words with the question. The cooking, car and football sentences scored near zero.

## What this is not
I did not train or fine-tune any model. The dataset is deliberately tiny so every number can be inspected.
Not covered: fine-tuning, large document collections, vector databases, splitting long documents into chunks.

## Run it
Open `Semantic_Search_with_Sentence_Embeddings.ipynb` in [Google Colab](https://colab.research.google.com/) (File → Upload notebook) and choose Runtime → Run all.

## Tools
Python, Sentence Transformers, pandas, Google Colab

# GORetrieval

GORetrieval: A Novel Two-Stage Literature Based Deep Information Retrieval Framework for Accurate Protein Function Annotation

# Requirements

python == 3.7.10

sentence-transformers == 2.2.2

pyserini == 0.19.0

numpy == 1.21.6

torch == 1.7.0

# inference

```
python predict.py --task bp --pro 3 --gpu 0
```

# File Structure

├── cross_model - Download

└────── *_PubMedBERT_epoch{}

└────── *_PubMedBERT_epoch1

├── data - training and testing data

└────── *_trans.txt - train set

└────── test.txt - test set

├── file

└────── bp_pro2go.npy - proteinid -> GO list

└────── pmid2text.npy - Pubmed ID -> title and abstract 

└────── proid2name.npy - proteinid -> protein name


└────── *_dev_t5_texts.npy - extracted sentences

└────── *_retrieval_all.npy

└────── *_retrieval_pro_3.npy - retrieval result

└────── *_t5_scores.npy - score cache


├── go_index
  
├── predict.py

├── pro_index

├── result - final result

├── test

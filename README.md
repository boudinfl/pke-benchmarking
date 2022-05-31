# Benchmarking keyphrase extraction models with `pke`

Repository for benchmarking keyphrase extraction (and generation) models
on commonly-used datasets.

## Getting started

```
# clone the tutorial code
git clone https://github.com/boudinfl/pke-benchmarking.git
cd pke-benchmarking

# (optional) set up a virtual environment for Python 
virtualenv -p python3 venv
source venv/bin/activate

# install the required modules
pip install -r requirements.txt

# install required spacy language models
!python -m spacy download en_core_web_sm
```

## Datasets

We use the datasets for benchmarking keyphrase extraction and generation
models that are available on [our HuggingFace space](https://huggingface.co/taln-ls2n).
Below are details about the currently available datasets :

- English
  - [inspec](https://huggingface.co/datasets/taln-ls2n/inspec) (paper abstracts)
  - [kp20k](https://huggingface.co/datasets/taln-ls2n/kp20k) (paper abstracts)
  - [semeval-2010](https://huggingface.co/datasets/taln-ls2n/semeval-2010) (full-text articles)
  - [pubmed](https://huggingface.co/datasets/taln-ls2n/pubmed) (full-text articles)
  - [kptimes](https://huggingface.co/datasets/taln-ls2n/kptimes) (news articles)
- French
  - [termith-eval](https://huggingface.co/datasets/taln-ls2n/termith-eval) (paper abstracts)
  - [taln-archives](https://huggingface.co/datasets/taln-ls2n/taln-archives) (paper abstracts)
  - [wikinews-fr-100](https://huggingface.co/datasets/taln-ls2n/wikinews-fr-100) (news articles)

## Models

We use the models implemented in the [Python Keyphrase Extraction (`pke`)](https://github.com/boudinfl/pke) toolkit.

## Results

Machine: 3,2 GHz Intel Core i5 4-cores

### inspec
| Model | it/s |  F@5 | F@10 |
| :---- | ----:| ---: | ---: |
| FirstPhrases  | 301.9 | 24.04 | 28.61 |
| TextRank  | 164.1 | 27.07 | 34.20 |
| SingleRank  | 176.9 | 27.83 | 34.18 |
| TopicRank  | 119.1 | 24.45 | 28.60 |
| PositionRank  | 167.3 | 28.04 | 33.20 |
| MultipartiteRank  | 92.2 | 24.69 | 29.59 |
| TfIdf  | 309.4 | 28.75 | 34.94 |
| TopicalPageRank  | 20.6 | 28.23 | 33.97 |

## semeval-2010-pre
| Model | it/s |  F@5 | F@10 |
| :---- | ----:| ---: | ---: |
| FirstPhrases  | 190.3 | 13.96 | 14.94 |
| TextRank  | 121.6 | 9.32 | 13.42 |
| SingleRank  | 116.9 | 11.55 | 16.29 |
| TopicRank  | 83.3 | 12.07 | 14.46 |
| PositionRank  | 115.7 | 12.54 | 17.32 |
| MultipartiteRank  | 60.9 | 13.84 | 15.61 |
| TfIdf  | 193.5 | 13.20 | 16.08 |
| TopicalPageRank  | 25.4 | 11.53 | 16.32 |



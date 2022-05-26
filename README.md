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

### inspec
| Model | it/s |  F@5 | F@10 |
| :---- | ----:| ---: | ---: |
| FirstPhrases  | 608.2 | 24.06 | 28.64 |
| TextRank  | 404.6 | 27.05 | 34.23 |
| SingleRank  | 404.6 | 27.83 | 34.21 |
| TopicRank  | 288.9 | 24.47 | 28.60 |
| PositionRank  | 392.7 | 28.07 | 33.23 |
| MultipartiteRank  | 212.1 | 24.72 | 29.61 |
| TfIdf  | 638.2 | 28.78 | 34.96 |
| TopicalPageRank  | 19.0 | 28.25 | 34.00 |


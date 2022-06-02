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
| FirstPhrases  | 296.3 | 24.04 | 28.61 |
| TextRank  | 160.8 | 27.07 | 34.20 |
| SingleRank  | 179.9 | 27.83 | 34.18 |
| TopicRank  | 123.7 | 24.45 | 28.60 |
| PositionRank  | 166.5 | 28.04 | 33.20 |
| MultipartiteRank  | 93.7 | 24.69 | 29.59 |
| TfIdf  | 300.1 | 28.75 | 34.94 |
| TopicalPageRank  | 20.3 | 28.23 | 33.97 |
| YAKE  | 46.3 | 29.46 | 33.01 |
| KPMiner  | 312.2 | 26.80 | 33.47 |
| Kea  | 237.0 | 28.70 | 33.54 |

## semeval-2010-pre
| Model | it/s |  F@5 | F@10 |
| :---- | ----:| ---: | ---: |
| FirstPhrases  | 188.7 | 13.96 | 14.94 |
| TextRank  | 116.9 | 9.32 | 13.42 |
| SingleRank  | 115.7 | 11.55 | 16.29 |
| TopicRank  | 72.6 | 12.07 | 14.46 |
| PositionRank  | 94.1 | 12.54 | 17.32 |
| MultipartiteRank  | 55.1 | 13.84 | 15.61 |
| TfIdf  | 190.3 | 13.20 | 16.08 |
| TopicalPageRank  | 24.8 | 11.53 | 16.32 |
| YAKE  | 36.5 | 15.73 | 17.97 |
| KPMiner  | 180.0 | 12.26 | 17.22 |
| Kea  | 154.6 | 14.32 | 16.89 |



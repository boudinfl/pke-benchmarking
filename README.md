# Benchmarking keyphrase extraction models with `pke`

Repository for benchmarking keyphrase extraction (and generation) models
on commonly-used datasets.

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
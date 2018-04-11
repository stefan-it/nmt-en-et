# Neural Machine Translation system for English to Estonian

This repository contains all data and documentation for building a neural
machine translation system for English to Estonian.

# Dataset

The *WMT18 English-Estonian* data comes from [EMNLP 2018 website](http://www.statmt.org/wmt18/translation-task.html).

## Training

The original training data from WMT18 is used. The training data for English-Estonian is the following:

| Data set         | Sentences | Download
| ---------------- | --------- | ---------------------------------------------------------------------------------------------------------------------------
| Europarl v8      |   652,944 | [WMT18](http://data.statmt.org/wmt18/translation-task/training-parallel-ep-v8.tgz)
| ParaCrawl corpus | 1,298,103 | [WMT18](https://s3.amazonaws.com/web-language-models/paracrawl/release1/paracrawl-release1.en-et.zipporah0-dedup-clean.tgz)
| Rapid corpus     |   226,978 | [WMT18](http://data.statmt.org/wmt18/translation-task/rapid2016.tgz)

## Development

For development data, the SGML tags needs to be stripped. For this purpose, the
`input-from-sgm.perl` script from [Moses](https://github.com/moses-smt/mosesdecoder/blob/master/scripts/ems/support/input-from-sgm.perl)
was used. The resulting development set was uploaded to this GitHub repository.

| Data set         | Sentences | Download
| ---------------- | --------- | --------------------------------------------------------------------------------------------
| Development      | 2,000     | via [GitHub](https://github.com/stefan-it/nmt-en-et/raw/master/data/newsdev2018-enet.tar.gz)

## Summary

Here comes a summary of training and development set:

| Data set         | Sentences
| ---------------- | ---------
| Training (all)   | 2,178,025
| Development      |     2,000

# *tensor2tensor* - Transformer

A NMT system for English-Estonian is built with the [*tensor2tensor*](https://github.com/tensorflow/tensor2tensor)
library.

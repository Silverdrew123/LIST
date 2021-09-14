# LM-BFF (**B**etter **F**ew-shot **F**ine-tuning of **L**anguage **M**odels)

This is the implementation of the paper [Making Pre-trained Language Models Better Few-shot Learners](https://arxiv.org/pdf/2012.15723.pdf). LM-BFF is short for **b**etter **f**ew-shot **f**ine-tuning of **l**anguage **m**odels.

## Quick links

* [Overview](#overview)
* [Requirements](#requirements)
* [Prepare the data](#prepare-the-data)
* [Run the model](#run-lm-bff)
  * [Quick start](#quick-start)
* [Citation](#citation)


## Overview

![](./figs/lmbff.png)

In this work we present LM-BFF, a suite of simple and complementary techniques for fine-tuning pre-trained language models on a small number of training examples. Our approach includes:

1. Prompt-based fine-tuning together with a novel pipeline for automating prompt generation.
2. A refined strategy for incorporating demonstrations into context.

You can find more details of this work in our [paper](https://arxiv.org/pdf/2012.15723.pdf).

## Requirements

To run our code, please install all the dependency packages by using the following command and update the transformers package to include Deberta model:

```
pip install -r requirements.txt
pip install git+https://github.com/huggingface/transformers
```

**NOTE**: Different versions of packages (like `pytorch`, `transformers`, etc.) may lead to different results from the paper. However, the trend should still hold no matter what versions of packages you use.

## Prepare the data

We pack the original datasets (SST-2, SST-5, MR, CR, MPQA, Subj, TREC, CoLA, MNLI, SNLI, QNLI, RTE, MRPC, QQP, STS-B) [here](https://nlp.cs.princeton.edu/projects/lm-bff/datasets.tar). Please download it and extract the files to `./data/original`, or run the following commands:

```bash
cd data
bash prepare_dataset.sh
```

philly folder is `PromptST/philly/Extra_exp`

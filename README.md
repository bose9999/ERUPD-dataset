# ERUPD: English to Roman Urdu Parallel Dataset
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

**Authors:** Mohammed Furqan, Raahid Bin Khaja, Rayyan Habeeb  
**Source Paper:** [arXiv:2412.17562v1](https://arxiv.org/abs/2412.17562)

## Overview

**ERUPD** is a novel parallel dataset designed for English ↔ Roman Urdu machine translation and other NLP tasks.  
Roman Urdu—a Latin-script form of Urdu commonly used in digital messaging—is non-standardized, phonetically variable, and code-switches frequently with English, making it challenging for computational processing.

This dataset addresses the resource gap for Roman Urdu by combining:

-  **Synthetic data** generated via prompt engineering using LLMs like GPT-3.5 and Claude.
-  **Conversational data** from WhatsApp group chats.
-  **Manual human refinement** for phonetic consistency, gender handling, and synonym diversity.

### Suitable For:
- Neural Machine Translation (NMT)
- Sentiment Analysis
- Code-Switching Detection
- Low-Resource NLP Research

## Repository Structure

This repository contains the **training data portion (~65,000 sentence pairs)** of the full ERUPD corpus.  
_Test data has been intentionally omitted for evaluation purposes._

### Files:
- `ERUPD_dataset.json` – A JSON file containing aligned sentence pairs.

#### JSON Format Example:
```json
[
  {
    "English": "He is eating an apple.",
    "Roman Urdu": "Woh aik seb kha raha hai."
  },
  {
    "English": "They are watching TV.",
    "Roman Urdu": "Woh TV dekh rahe hain."
  }

   {
    "English": "They are playing GTA.",
    "Roman Urdu": "Woh GTA khel rahe hai."
  }

]
```

Citation
If you use this dataset in your work, please cite:

<pre lang="markdown"> ```bibtex @misc{furqan2024erupd, title={ERUPD - English to Roman Urdu Parallel Dataset}, author={Mohammed Furqan and Raahid Bin Khaja and Rayyan Habeeb}, year={2024}, eprint={2412.17562}, archivePrefix={arXiv}, primaryClass={cs.CL} } ``` </pre>

### Translation Models Folder :
The translation_models folder contains downloaded Kaggle notebooks used for evaluating the **ERUPD** dataset. These notebooks include implementation code for transformer-based neural machine translation models such as *T5-Small* and *mBART*. The models were trained and tested on the dataset to assess translation quality using metrics like *BLEU* and *METEOR*.

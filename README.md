# Multilingual ASR Human Evaluation Dataset

This repository contains the human evaluation dataset accompanying our paper: **Advocating Character Error Rate for Multilingual ASR Evaluation.**

## Overview

Automatic Speech Recognition (ASR) systems have advanced significantly, but evaluating their performance across multiple languages remains a challenge. Traditional metrics like Word Error Rate (WER) are not consistently reliable for languages with complex morphology or unclear word boundaries. This dataset addresses these issues by providing:

- **Human Evaluation Data**: Ratings from human evaluators for ASR transcriptions in **Malayalam**, **English**, and **Arabic**—languages with diverse morphological characteristics—along with the corresponding transcriptions, ground truth sentences and audio samples.
- **Metrics Analysis Tools**: A Jupyter notebook (`metrics.ipynb`) for calculating error rates (WER, CER) and analyzing their correlation with human judgments.

Our goal is to highlight the limitations of WER in multilingual contexts and advocate for the use of alternate metrics. We currently support WER, CER, and PER (Phoneme Error Rate). With little modification, other metrics can be added and evaluated.


## Description

### Audio Samples (`samples/`)

Contains audio files for each language:
- `ar/`: Arabic samples.
- `en/`: English samples.
- `ml/`: Malayalam samples.

### Transcriptions (`transcriptions/`)

Includes transcriptions for each language:
- `ground.txt`: Ground truth transcriptions.
- `*.txt`: Transcriptions from different ASR systems (e.g., `mms.txt`, `whisper.txt`).

### Survey Results (`survey/`)

CSV files with human evaluation ratings:
- `survey_arabic.csv`
- `survey_english.csv`
- `survey_malayalam.csv`

**Format:**
- **Header Row**: Contains question IDs (e.g., `Demographics Q1`, `Q1_2`, `Q2_1`).
- **First Data Row**: Contains question texts and transcriptions.
- **Subsequent Rows**: Individual evaluator responses, with ratings from 0 to 5 (or the answers to demographic questions).

### Metrics Notebook (`metrics.ipynb`)

Jupyter notebook for calculating error rates and correlations between human judgments and ASR metrics.

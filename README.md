# How Reliable is MT Evaluation?

## Overview
This project is the third project proposed by Université Paris Cité for the Multilingual NLP class in the 2024-2025 school year. It investigates the reliability of the BLEU metric in machine translation (MT) evaluation. The work involves implementing BLEU from scratch, analyzing its limitations, and comparing it with more robust evaluation methods such as SacreBLEU.

## Table of Contents
1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Implementation Details](#implementation-details)
4. [Experiments](#experiments)
   - Using BLEU
   - Using SacreBLEU
   - Tokenization Impacts
5. [Key Findings](#key-findings)
6. [References](#references)

  
## Introduction
BLEU is one of the most widely used metrics for MT evaluation. However, recent studies highlight critical issues in its use, including potential flaws in interpretation and its sensitivity to tokenization methods. This project revisits BLEU's role in MT evaluation and examines its performance against modern tools like SacreBLEU.

## Objectives
- Understand the computation of BLEU scores.
- Investigate how BLEU scores can be manipulated through word permutations.
- Analyze the impact of tokenization on evaluation results.
- Compare the performance of BLEU and SacreBLEU in real-world scenarios.

## Implementation Details
1. BLEU Implementation
- Custom implementation of BLEU from scratch.
- Comparison with SacreBLEU for consistency.
2. Tokenization
- Raw text.
- Subword tokenization using HuggingFace tools.
- Character-level tokenization.

## Experiments
1. Evaluate Models
- Models: mBart and MarianMT.
- Dataset: WMT’15 test set.
- Metric: BLEU and SacreBLEU.
2. Permutation Analysis
- Quantify the number of permutations possible with bigram mismatches.
3. Tokenization Impact
- Compare scores across different tokenization methods (raw text, subword, character-level).

## Key Findings
- BLEU's sensitivity to tokenization methods can lead to inconsistent results.
- Permutations in translation hypotheses can artificially inflate BLEU scores.
- SacreBLEU provides a more robust and reproducible evaluation framework.

## References
- Chris Callison-Burch, Miles Osborne et Philipp Koehn. “Re-evaluating the Role of Bleu in Machine Translation Research”. In : 11th Conference of the European Chapter of the Association for Computational Linguistics. Trento, Italy : Association for Computational Linguistics, avr. 2006, p. 249-256. url : https://aclanthology.org/E06-1032.
- Benjamin Marie. Science Left Behind. http://blog.benjaminmarie.com/scienceleft-behind.html. Accessed : 2022-10-19.
- NLLB Team et al. No Language Left Behind : Scaling Human-Centered Machine Translation. 2022. doi : 10.48550/ARXIV.2207.04672. url : https://arxiv.org/abs/2207.04672.

# Machine_Translation_Evaluation

How Reliable is MT Evaluation?
Overview
This project investigates the reliability of the BLEU metric in machine translation (MT) evaluation. The work involves implementing BLEU from scratch, analyzing its limitations, and comparing it with more robust evaluation methods such as SacreBLEU.

Table of Contents
Introduction
Objectives
Implementation Details
Experiments
Using BLEU
Using SacreBLEU
Tokenization Impacts
Key Findings
Usage
Run Python Scripts
Explore Jupyter Notebook
References
Introduction
BLEU is one of the most widely used metrics for MT evaluation. However, recent studies highlight critical issues in its use, including potential flaws in interpretation and its sensitivity to tokenization methods. This project revisits BLEU's role in MT evaluation and examines its performance against modern tools like SacreBLEU.

Objectives
Understand the computation of BLEU scores.
Investigate how BLEU scores can be manipulated through word permutations.
Analyze the impact of tokenization on evaluation results.
Compare the performance of BLEU and SacreBLEU in real-world scenarios.
Implementation Details
1. BLEU Implementation
Custom implementation of BLEU from scratch.
Comparison with SacreBLEU for consistency.
2. Tokenization
Raw text.
Subword tokenization using HuggingFace tools.
Character-level tokenization.
Experiments
1. Evaluate Models
Models: mBart and MarianMT.
Dataset: WMT’15 test set.
Metric: BLEU and SacreBLEU.
2. Permutation Analysis
Quantify the number of permutations possible with bigram mismatches.
3. Tokenization Impact
Compare scores across different tokenization methods (raw text, subword, character-level).
Key Findings
BLEU's sensitivity to tokenization methods can lead to inconsistent results.
Permutations in translation hypotheses can artificially inflate BLEU scores.
SacreBLEU provides a more robust and reproducible evaluation framework.

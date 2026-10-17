# Midterm 1: answers

GitHub username: yernurramazanov
Session code: zebra-28
Fingerprint: 956cbc4b

> Fill in the three lines above from `my_data/DATA.md`. Do not rename headings or table columns: a script reads the numbers.
> Write only in the empty cells and lines. Percentages as 0.78 or 78 %, money as plain numbers.

## AI-use declaration

I used ChatGPT to read and clarify the repository instructions, run the supplied data generator with my GitHub username and session code, and help draft this file in English. ChatGPT used the GitHub connector to retrieve the README, generator and answer template. It ran Python in its execution environment to generate the synthetic data and calculate retrieval metrics, Wilson intervals, language-specific recall, annual costs and the numerical answers in Part 3.

ChatGPT also helped compare affordable retrieval candidates, interpret overlapping intervals, identify the weakest document-processing groups, and formulate a memo about personal-data handling and checkable safeguards. It consulted primary research on hallucination bounds to check the distinction between arbitrary facts and rule-based tasks in Q4. The calculations use the supplied synthetic data; they are not measurements of a real bank or real model. The generator produced fingerprint 956cbc4b for yernurramazanov and zebra-28.

The assistant proposed the recommendation and written explanations as well as performing calculations. This declaration therefore includes substantive AI assistance with analysis and writing, rather than translation alone. No other student's answers were used. This file is intended for my review and explanation during the oral check.

## Part 1: Retrieval and cost decision

### 1a. Metrics (all 60 questions)

| config | recall@1 | recall@3 | recall@5 | MRR@10 |
|---|---|---|---|---|
| A | 0.516667 | 0.766667 | 0.816667 | 0.634722 |
| B | 0.366667 | 0.516667 | 0.766667 | 0.488770 |

### 1b. Recall and 95 % Wilson interval of each candidate (recall at its own k)

| candidate | recall@k | lower | upper |
|---|---|---|---|
| A, k=3 | 0.766667 | 0.645635 | 0.855606 |
| A, k=5 | 0.816667 | 0.700800 | 0.894423 |
| B, k=3 | 0.516667 | 0.393076 | 0.638252 |
| B, k=5 | 0.766667 | 0.645635 | 0.855606 |

### 1c. Annual model cost in USD

| candidate | annual cost |
|---|---|
| A, k=3 | |
| A, k=5 | |
| B, k=3 | |
| B, k=5 | |

### 1d. Decision (at most 150 words)

Chosen candidate:

(Decision, using your intervals and the budget. Give the recall of your choice for EN, RU and KK separately.)

### 1e. Next measurement (at most 60 words)

## Part 2: A document pipeline you can defend

### 2a. Numbers

| pipeline | overall accuracy | weakest cell (language, condition) | accuracy there | lower | upper | annual cost |
|---|---|---|---|---|---|---|
| H | | | | | | |
| L | | | | | | |

Personal-data pages per year sent abroad under H:

### 2b. Memo (at most 300 words)

## Part 3: Explain your own numbers

### Q1

Number:
Why (at most 40 words):

### Q2

Number:
Why (at most 40 words):

### Q3

Number:
Why (at most 40 words):

### Q4

Number:
Why (at most 40 words):

### Q5

Number:
Why (at most 40 words):

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
| A, k=3 | 28117.75 |
| A, k=5 | 36655.71 |
| B, k=3 | 18728.66 |
| B, k=5 | 21007.22 |

### 1d. Decision (at most 150 words)

Chosen candidate: B, k=5

I choose B, k=5: its annual model cost is $21007.22, below the $24600 budget. Both A candidates exceed the budget. B, k=5 retrieves the correct chunk for 46/60 questions (76.67%; Wilson interval 64.56–85.56%), compared with 31/60 for B, k=3 (51.67%; 39.31–63.83%). These intervals do not overlap, so B, k=5 is the stronger affordable option under the course rule. Its interval overlaps both A intervals, so those comparisons do not establish a winner. Recall by language is EN 17/20 = 85%, RU 15/20 = 75%, and KK 14/20 = 70%. Kazakh is served worst in this sample and represents 38% of production traffic. These small language samples warrant further evaluation. Retrieval recall alone does not establish final answer correctness.

### 1e. Next measurement (at most 60 words)

Run a new paired, language-stratified evaluation of B, k=3 and B, k=5 on 200 fresh questions per language. Measure supported final-answer correctness and retrieval recall with Wilson intervals. If the extra chunks do not improve answer correctness, the cheaper candidate may become preferable; persistent Kazakh failures would motivate targeted retrieval changes.

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

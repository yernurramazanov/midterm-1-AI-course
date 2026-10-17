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
| H | 0.866667 | RU, degraded | 0.666667 | 0.487797 | 0.807697 | 18863.20 |
| L | 0.838889 | RU, degraded; KK, degraded (tie) | 0.733333 | 0.555517 | 0.858175 | 10800.00 |

Personal-data pages per year sent abroad under H: 992800

### 2b. Memo (at most 300 words)

To: Head of Operations

I recommend pipeline L with human review before extracted data affects payments. H achieves 156/180 = 86.67% overall accuracy; L achieves 151/180 = 83.89%. H's weakest group is degraded Russian scans: 20/30 = 66.67%, with a 95% Wilson interval of 48.78–80.77%. L has two equally weak groups, degraded Russian and degraded Kazakh: each 22/30 = 73.33%, interval 55.55–85.82%. Overall accuracy hides these failures. The overlapping weakest-cell intervals do not establish a difference between H and L, and 30 scans per cell leave substantial uncertainty.

Under H, scans go to a foreign data centre and 992800 personal-data pages would leave Kazakhstan annually. The external service processes them, but its storage, subprocessors, logs, backups, training use and retention periods are unknown. These require documented investigation and compliance review before deployment; a vendor assurance alone is insufficient. Law No. 94-V covers the IIN.

Under L, processing occurs on the bank's server in Kazakhstan, under bank control. We must still verify where files, outputs, logs and backups are stored, who can access them, and how long each copy remains. Local hosting alone does not resolve these questions.

Use network egress restrictions and traffic audits to verify local processing; role-based access and audit logs to check access; encryption for stored and transmitted scans; and documented retention rules tested by deleting sample files and checking logs and backup expiry. Check totals, identifiers and dates against validation rules, and route degraded scans or failed checks to human reviewers.

L costs $10800 annually for two servers versus H's $18863.20. It avoids routine foreign processing, but residual risks include extraction errors, unauthorised access, outages and human-review workload. Server prices exclude review and operational safeguards.

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

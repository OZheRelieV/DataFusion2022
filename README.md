# DataFusion2022

Here I represent my solutions of two tracks **DataFusion2022**. It aren't the best ones but it shows to you my thoughts flow.  

During these contest I faced with computational difficulties. It's too low computational power of my machine to deal with this contest good:

- CPU: 2 cores;
- RAM: 16 Gb.

Also I want to underline great size of an initial data files. Taking into account it, it was decided to produce initial data (*transactions.csv, clickstream.csv*) splitting by 1_000_000 elements in each file and data type conversion of given files (from .csv to .parquet). It allowed me to deal with contest data. After it I tried my best to solve some tracks of contest.

## "Puzzle" results (track №2)

It is necessary to solve the simplified Matching problem of matching customers in the format of a classic tabular competition.

It is necessary to create an algorithm that solves the problem in a situation where all candidates in a pair are known in advance,
but the pairs themselves are not provided.

Contest metric is `R1` (harmonic mean between **Precision@100** and **MRR@100**).

Used model is `CatBoostClassifier`.

`My results:`

|  Type    |      R1      |   MRR@100   |    p@100     |  Position |
|:--------:|:------------:|:-----------:|:------------:|:---------:|
| public   | 0.0213660899 | 0.011609980 | 0.1338063862 |  41 (62)  |
| private  | 0.0173880855 | 0.009342760 | 0.1252098010 |  41 (62)  |

Because of computational problems I made only 5 attempts and left thought to receive high score and good algorithm for clients matching.

## "Education" results (track №3)

An exercise for those who want to learn how to work with industrial data of transactions and clickstreams. It's necessary to create an algorithm that can predict whether a client has a higher education (description from organisators).  
It's classic binary classification problem.

Here I tried to apply auto machine learning approach from **SberAI** (`lightautoml`).

Contest metric is `ROC AUC`.

`My results:`

|  Type    |  ROC AUC |  Position |
|:--------:|:--------:|:---------:|
| public   | 0.790160 |  33 (85)  |
| private  | 0.785577 |  39 (85)  |

The whole struggle was for thousandths and sometimes ten thousandths after the decimal point.

## Results

This contest has generalized leaderboard. It accumulates all reached achievements into one table with some weights.  
Contest also provided two activities for those who shared his notebooks and who finded some interesting insights in data.

| Place | Track №1 score | Track №2 score | Track №3 score | Activity №1 score | Activity №2 score | Total score |
|:-----:|:--------------:|:--------------:|:--------------:|:-----------------:|:-----------------:|:-----------:|
|  59 (188)   |       ---      |  0.0173880855  |    0.785577    |   ---             |         ---       |    633      |

Possibly it's good results or maybe not :)

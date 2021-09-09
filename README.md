
Detecting Inspiring Content on Social Media
=================================================================================
Oana Ignat, Y-Lan Boureau, Jane Yu, Alon Halevy

This repository contains the dataset and code for our ACII 2021 paper:

[Detecting Inspiring Content on Social Media](https://arxiv.org/pdf/2109.02734.pdf) 

## Task Description
![Example instance](images/ACII2021.jpg)
The goal of this research is to develop models that can recognize whether a post on social media is likely to inspire someone who reads that post.

## Data
The submission ids of the inspiring and non-inspiring posts we collect for our paper: [`data_all_post_ids.csv`](data_all_post_ids.csv)

## Data Crawler
The code for crawling Reddit: [`collect_reddit_data.ipynb`](collect_reddit_data.ipynb)

## Annotation Details

#### We filter the data using the following heuristics: 
* (1) public posts with at least one comment that contains the substrings ``inspir`` or ``uplift`` (Reddit \& Facebook) 
* (2) public posts that authors mark as ``feeling inspired`` or ``feeling up`` (Facebook)
* (3) public posts that are shared at least 10 times (Facebook)
* (4) public posts from the subreddits that contain the substrings ``inspir`` or ``uplift`` (Reddit)
* (5) comments to the following four questions from the ``AskReddit`` subreddit:  
``When was the last time you felt inspired?``, ``Who or what inspired you?``, ``Who inspired you and how?``, 
``What is the most inspiring thing you have ever seen or heard?``  (Reddit).

As control, we also collect random posts: 
* (1) posts with no comment that contains the substrings ``inspir`` or ``uplift`` (Reddit \& Facebook)
* (2) posts from random subreddits that do not contain the substrings ``inspir`` or ``uplift`` (Reddit)

#### The resulting posts are annotated by crowd-sourced workers  to determine: 
* (1) whether the post is inspiring or not; 
* (2) if the post is inspiring, what influence it has on the reader; 
* (3) what emotions it evokes; 
* (4) the annotator's confidence in the answer.

## Citation information
If you use this dataset or any ideas based on the associated research article, please cite the following:

```bibtex
@misc{ignat2021detecting,
    title={Detecting Inspiring Content on Social Media},
    author={Oana Ignat and Y-Lan Boureau and Jane A. Yu and Alon Halevy},
    year={2021},
    eprint={2109.02734},
    archivePrefix={arXiv},
    primaryClass={cs.CL}
}
```
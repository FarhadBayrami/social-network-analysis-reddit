# social-network-analysis-reddit
Social Network Analysis of Reddit Subreddit Hyperlink Network

# Social Network Analysis: Subreddit Interactions

## Overview
This project analyzes the Reddit Subreddit Hyperlink Network using Social Network Analysis (SNA) techniques.

The network represents directed interactions between subreddits, where edges correspond to hyperlinks from one subreddit to another.

## Dataset
The dataset is provided by the Stanford Network Analysis Project (SNAP):

https://snap.stanford.edu/data/soc-RedditHyperlinks.html

### Dataset Characteristics
- Nodes: 55,863 subreddits
- Edges: 858,490 hyperlinks
- Type: Directed, signed, temporal network
- Time span: January 2014 – April 2017

The analysis focuses on the Largest Strongly Connected Component (SCC).

Final analyzed network:
- Nodes: 11,564
- Edges: 98,166
- Average degree: 17

## Methods Applied
- Louvain Community Detection
- Degree Centrality
- Betweenness Centrality
- Eigenvector Centrality
- PageRank
- Global and Local Clustering Coefficients
- Edge Betweenness Analysis

Tools used:
- Python (NetworkX)
- Gephi

## Key Findings
- 23 communities detected
- Largest community: 2754 nodes
- Key influential subreddits: askreddit, iama, subredditdrama
- Low global clustering coefficient (0.0711)
- High edge redundancy (robust network structure)

## Repository Structure
- `SNA_Report.pdf` → Final project report

## Authors
Farhad Bayrami  
Mahmut Kaan Molla  

## Course
Social Network Analysis  
August 2024
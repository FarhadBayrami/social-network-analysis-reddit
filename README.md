<div align="center">

# 🕸️ Social Network Analysis of Reddit Subreddit Hyperlink Network

[![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![NetworkX](https://img.shields.io/badge/NetworkX-Graph%20Analysis-blue?style=for-the-badge)](https://networkx.org)
[![Gephi](https://img.shields.io/badge/Gephi-Visualisation-9B59B6?style=for-the-badge)](https://gephi.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

<p align="center">
  <img src="https://img.shields.io/badge/Nodes-55%2C863%20subreddits-blue?style=flat-square"/>
  <img src="https://img.shields.io/badge/Edges-858%2C490%20hyperlinks-green?style=flat-square"/>
  <img src="https://img.shields.io/badge/Communities-23%20detected-orange?style=flat-square"/>
  <img src="https://img.shields.io/badge/Time%20Span-2014--2017-red?style=flat-square"/>
</p>

*Graph-theoretic analysis of directed subreddit interactions using centrality measures, community detection, and network topology metrics.*

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Dataset](#-dataset)
- [Methods](#-methods)
- [Key Findings](#-key-findings)
- [Network Statistics](#-network-statistics)
- [Getting Started](#-getting-started)
- [Project Structure](#-project-structure)
- [Future Work](#-future-work)
- [References](#-references)
- [Authors](#-authors)

---

## 🔬 Overview

This project applies **Social Network Analysis (SNA)** techniques to the Reddit Subreddit Hyperlink Network — a large-scale directed graph where nodes are subreddits and edges represent hyperlinks posted from one community to another.

The analysis uncovers:
- How information and influence flow across Reddit communities
- Which subreddits act as structural bridges or hubs
- How communities naturally cluster around shared topics or sentiment

---

## 📦 Dataset

**Reddit Subreddit Hyperlink Network** — Stanford Network Analysis Project (SNAP)

🔗 [snap.stanford.edu/data/soc-RedditHyperlinks.html](https://snap.stanford.edu/data/soc-RedditHyperlinks.html)

| Property       | Value                          |
|----------------|-------------------------------|
| Nodes          | 55,863 subreddits             |
| Edges          | 858,490 hyperlinks            |
| Network type   | Directed, signed, temporal    |
| Time span      | January 2014 – April 2017     |

The analysis focuses on the **Largest Strongly Connected Component (SCC)** to ensure meaningful path-based metrics:

| Property         | SCC Value   |
|------------------|-------------|
| Nodes            | 11,564      |
| Edges            | 98,166      |
| Average degree   | 17          |

---

## ⚙️ Methods

### Centrality Measures
| Measure                  | Purpose                                              |
|--------------------------|------------------------------------------------------|
| **Degree Centrality**    | Identifies the most connected subreddits             |
| **Betweenness Centrality** | Finds bridge nodes controlling information flow    |
| **Eigenvector Centrality** | Ranks nodes by the importance of their neighbours  |
| **PageRank**             | Authority-based ranking (like Google's algorithm)    |

### Community & Topology
- **Louvain Community Detection** — modularity-optimised clustering
- **Global & Local Clustering Coefficients** — measures of local cohesion
- **Edge Betweenness Analysis** — identifies structurally critical links

### Tools
- **Python / NetworkX** — graph construction, metrics, SCC extraction
- **Gephi** — large-scale network visualisation

---

## 📊 Key Findings

| Finding                        | Value / Detail                                 |
|-------------------------------|------------------------------------------------|
| Communities detected           | **23**                                         |
| Largest community              | **2,754 nodes**                                |
| Most influential subreddits    | `r/askreddit`, `r/iama`, `r/subredditdrama`    |
| Global clustering coefficient  | **0.0711** (sparse, scale-free structure)      |
| Network structure              | High edge redundancy → robust to node removal  |

> The low clustering coefficient combined with high hub centrality is consistent with a **scale-free network** — a small number of subreddits dominate cross-community linking behaviour.

---

## 📈 Network Statistics

**Full Network**

| Property | Value |
|----------|-------|
| Nodes | 55,863 subreddits |
| Edges | 858,490 hyperlinks |
| Type | Directed, signed, temporal (2014–2017) |

**Largest SCC (analysed subset)**

| Property | Value |
|----------|-------|
| Nodes | 11,564 |
| Edges | 98,166 |
| Avg degree | 17 |
| Global clustering coeff | 0.0711 |

**Community Structure**

| Property | Value |
|----------|-------|
| Communities | 23 |
| Largest community | 2,754 nodes |
| Key hubs | r/askreddit, r/iama, r/subredditdrama |
## 🚀 Getting Started

### Prerequisites

```bash
pip install -r requirements.txt
```

### Run

```bash
# 1. Clone the repository
git clone https://github.com/FarhadBayrami/social-network-analysis-reddit.git
cd social-network-analysis-reddit

# 2. Install dependencies
pip install -r requirements.txt

# 3. Download the dataset
#    → https://snap.stanford.edu/data/soc-RedditHyperlinks.html
#    → Place the .tsv files in a /data folder

# 4. Open the report for full methodology and results
#    → SNA_Report.pdf
```

---

## 📁 Project Structure

| File | Description |
|------|-------------|
| `SNA_Report.pdf` | Full report: methodology, results, visualisations |
| `requirements.txt` | Python dependencies |
| `LICENSE` | MIT License |
| `CITATION.cff` | How to cite this work |
| `README.md` | Project documentation |

## 🔮 Future Work

- [ ] Temporal analysis — track how community structure evolves 2014–2017
- [ ] Sentiment-aware graph — weight edges by positive/negative post sentiment
- [ ] Compare body vs. title hyperlink networks
- [ ] Interactive visualisation with Pyvis or D3.js
- [ ] Apply Graph Neural Networks for subreddit classification

---

## 📚 References

1. Kumar, S. et al. — *Community Interaction and Conflict on the Web*, WWW 2018.
2. Leskovec, J. & Krevl, A. — *SNAP Datasets: Stanford Large Network Dataset Collection*, 2014.
3. Blondel, V. et al. — *Fast unfolding of communities in large networks (Louvain)*, J. Stat. Mech., 2008.
4. Newman, M. — *Networks: An Introduction*, Oxford University Press, 2010.

---

## 👤 Authors

**Farhad Bayrami**
MSc Student — University of Bologna
📧 [farhad.bayrami@studio.unibo.it](mailto:farhad.bayrami@studio.unibo.it)
🔗 [GitHub](https://github.com/FarhadBayrami)

**Mahmut Kaan Molla**
MSc Student — University of Bologna

---

<div align="center">
  <sub>Built with ❤️ as part of a Social Network Analysis course project at the University of Bologna · August 2024</sub>
</div>
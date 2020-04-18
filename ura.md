# Guide for Waterloo Undergraduates

I'm always interested in working with bright and self-motivated Waterloo undergraduates, either as part of the formal [URA program](https://cs.uwaterloo.ca/current-undergraduate-students/research-opportunities/undergraduate-research-assistantship-ura-program) or informally otherwise.
The easiest point of entry is our [Anserini](http://anserini.io/) project, which powers our [Neural Covidex](http://covidex.ai/), a search engine that uses state-of-the-art neural network models.

If you'd like to work with me, start with the following:

+ Poke around the [Anserini GitHub repo](http://anserini.io/) and its [Pyserini](http://pyserini.io/) companion (which provides Python bindings).
+ Take a look at the [Anserini and Pyserini online notebooks](https://github.com/castorini/anserini-notebooks) &mdash; spend time to understand what's going on.
+ For an introduction to question answering, read [this paper](https://arxiv.org/pdf/1611.09268.pdf) and try to replicate the experiments [here](https://github.com/castorini/anserini/blob/master/docs/experiments-msmarco-passage.md). These results correspond to the BM25 baseline on the [MS MARCO Leaderboard](https://microsoft.github.io/msmarco/). If you've done this successfully, send a PR to add to the replication log at the bottom of the experiments page. In your PR describe your environment (and any issues you may have encountered).

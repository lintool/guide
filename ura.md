# Guide for Waterloo Undergraduates

I'm always interested in working with bright and self-motivated Waterloo undergraduates, either as part of the formal [URA program](https://cs.uwaterloo.ca/current-undergraduate-students/research-opportunities/undergraduate-research-assistantship-ura-program) or informally otherwise.
The easiest point of entry is the [Anserini](http://anserini.io/) project, which powers the [Neural Covidex](http://covidex.ai/), our search engine that uses state-of-the-art neural network models.

## What's In It For You?

For me, working with undergraduates is an opportunity to expose them to my research passion and also to recruit future graduate students.

What's in it for you?
You get to work on cool projects.
You get to learn new skills.
You get exposure to cutting-edge research.
Not at the start, of course... we work up to that.

The range of outcomes for undergrads working with me is very wide:
At one end of the spectrum, (in many cases) I never hear from you again after the first week.
At the other end of the spectrum, you love working with me so much that you decide to do your Ph.D. with me.
And everything in between... one common outcome is that you start as an URA and end up doing a thesis Masters with me. 

## Initial Screening

If you'd like to work with me, start with the following:

+ Poke around the [Anserini GitHub repo](http://anserini.io/) and its [Pyserini](http://pyserini.io/) companion (which provides Python bindings).
+ Take a look at the [Anserini and Pyserini online notebooks](https://github.com/castorini/anserini-notebooks) &mdash; spend time to understand what's going on.
+ For some general background, read the [Introduction](http://www.ir.uwaterloo.ca/book/01-introduction.pdf) of Büttcher et al's [IR textbook](http://www.ir.uwaterloo.ca/book/): in particular, 1.1, 1.2, and 1.4.
+ For an introduction to question answering, read [this paper](https://arxiv.org/pdf/1611.09268.pdf) and try to replicate the experiments [here](https://github.com/castorini/anserini/blob/master/docs/experiments-msmarco-passage.md) and [here](https://github.com/castorini/anserini/blob/master/docs/experiments-msmarco-doc.md). These results correspond to the BM25 baseline on the [MS MARCO Leaderboard](https://microsoft.github.io/msmarco/). If you've done this successfully, send a PR to add to the replication log at the bottom of the experiments page. In your PR describe your environment (and any issues you may have encountered).

You can send me an email after you've done all of the above.
In you email, mention the phrase "banana odyssey": this lets me know you've actually read this document.

**Note:** Don't bother emailing me until you've done the steps above; if you do, I'll just refer you to this document.
Think of the above as an "initial screen", which is necessary because I get many requests to work with me and don't have time to respond to them all in a customized manner.
Those tasks shouldn't take more than a few hours, and it's an opportunity to see if you're truly interested in my work.

## Different Paths

After the initial screen, you might be interested in different types of research that my students and I work on:

+ [Hedwig](https://github.com/castorini/hedwig): Document classification using neural networks.
+ [DeeBERT](https://github.com/castorini/DeeBERT): Efficiency issues in transformer-based models, or how do I make inference go vroom!
+ If you're more interested in the data engineering or systems-building side of my work, the next steps might be to play with [Solr](https://github.com/castorini/anserini/blob/master/docs/solrini.md) and [Elasticsearch](https://github.com/castorini/anserini/blob/master/docs/elastirini.md) integrations with Anserini.

## My Expectations

Students often ask what my expectations are: the answer is, I have _none_.
Yes, seriously.
If I don't hear from you after the first week, I won't think any less of you.
Life is short, everyone has conflicting demands on their time, and you should only work on something if you're interested in it.

My advice is simple: How much you get out of working with me is directly dependent on how much work you put in.
The single most important trait in successfully working with me, I believe, is being _self-motivated_; generally, technical background isn't an issue &mdash; you got into Computer Science at Waterloo, after all.
With me, there are no deadlines.
How much interaction you get with me depends on how fast you _choose_ to work.
Starting with the "Initial Screen", once you finish something, I'll (try to) give you something else to work on.
If you finish it in a day, I'll give you something else to work on, and the same after that.
Those things will increase in complexity and provide you bigger learning opportunities... until you either stop working (had enough), or you decide you like them so much you want a greater level of commitment (e.g., you want to do a Masters with me).

Note that, at least in the beginning, it may not be uncommon for me to assign the same task to multiple students.
Because of the voluntary nature of URAs, it is hard for me gauge a student's level of interest, or when (if ever) something will be completed.
Typically, I'll try to coordinate and reduce duplication on GitHub issues, but as tasks move on and off the critical path to my other projects, preemption is a possibility.

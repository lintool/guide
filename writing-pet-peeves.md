# Writing Pet Peeves

## Organization

+ Explicit "roadmaps" in prose (e.g., "In Section 2 we provide background... Section 3 describes our model... Experimental results are presented in Section 4") are useless and an absolute waste of space. Why spend a paragraph describing what I already expect (i.e., all technical papers share similar structure) and what I could figure out in two seconds (i.e., I could simply flip ahead and read your section titles).

+ Instead, let your prose implicitly lay out the structure for your reader. For example, if I say that my model has three novel features, then in the methods section there should be three subsections, each corresponding to each novel feature.

+ Use consistent terminology. Use the same words to describe your contribution throughout the paper. Don't say "soft alignment between words in phrases in the question and answer" in one place and then talk about "soft semantic matching" if you mean for them to be the same thing. Especially terms that sound similar but are slightly different, like in the example above. Don't confuse your reader. If stylistically the prose comes out too repetitive and mechanical, then consider mixing verbal and nominal forms, e.g., "matching at the semantic level" and "semantic matching", but make sure they _clearly_ mean the same thing.

## Grammar and Style

+ Use superlatives and "hype phrases" sparingly - things like "dramatically improves the user experience" - unless it's actually warranted. If you improve precision from 0.4 to 0.8, calling the improvements _dramatic_ might be warranted. A 5% improvement is not. I would let the results speak from themselves. Overuse of superlatives potentially turns off reviewers.

+ Related, use the term _significant_ only in the technical sense of statistically significant.

+ "State of the art" as a noun is written without hyphens, as in "Our algorithm represents the state of the art". As an adjective, "start-of-the-art" is hyphenated, as in, "These are state-of-the-art results".

+ "run" + "time" = ??? The answer is [this](https://homes.cs.washington.edu/~jrw12/runtime.html).

+ More generally, adjectival forms are hyphenated, i.e., "machine learning" but "machine-learned models".

+ It's "training set", "validation test", and "test set". Not "testing set". I know, it's odd. I think the non-parallel construction is just idiosyncratic, since "train set" sounds odd.

+ Stay in the same tense! Some authors like to describe experiments in the past tense, e.g., "The user received a push notification and clicked on it." Others like to describe experiments in the present tense, e.g., "The user receives a push notification and clicks on it." Both are fine, but stay consistent in the same tense. Don't write, "The user receives a push notification and clicks on it. The click was then recorded by the server."

+ "Related work", **not** "related works". "Work" is a collective noun, like "staff". You don't write "research staffs". Wait, you ask: if this is indeed the case, why would you write ["DaVinci is the creator of several famous _works_ of art"](https://twitter.com/mmparker/status/991012314332545024)? Well, that's a completely different context: "work" in "related work" is intended to refer to a body of work collectively, as in "the literature". You don't write "related literatures" (well, except in a very narrow sense, something like "isolated silos of related literatures"). Note that "DaVinci's work" and "DaVinci's works" are both fine, but in different contexts. The first might refer to his body of work collectively; the second focuses on individual pieces. Also, be aware of subject-verb agreement.

+ Common noun-verb (note that in Latex this would be an en-dash, see below) agreement issue: "number of sample increases", not "increase". The verb agrees with the head noun, which is number, singular in this case.

### Citations

+ **NEVER** *ever* begin a sentence with a citation. e.g., "[5] explored the use of..." The worst is related work that's simply a collection of such sentences, e.g. "[1] did this... [2] did that... [3] did other".

+ A citation is not a noun phrase, e.g., "is shown in [5]" is bad; should be "is shown by Smith et al. [5]". (Although I break this rule myself sometimes, especially if I'm trying to save a bit of space.)

+ Name your proceedings volumes consistently in the bibliography. I hate seeing "SIGIR 2015", "Proceedings of SIGIR 2014", and "Proceedings of the 40th International ACM SIGIR Conference on Research and Development in Information Retrieval" all in the same bibliography. The fact that NAACL can't even consistently name their conferences from year to year drives me nuts: its [NAACL HLT 2018](http://naacl2018.org/) (with a space), before it was [NAACL-HLT 2012](http://mirror.aclweb.org/hlt-naacl12/) (with a hyphen); back to a space with [NAACL HLT 2010](https://naaclhlt2010.isi.edu/), back to a dash with [NAACL-HLT 2007](http://mirror.aclweb.org/hlt-naacl07/); oh, let's swap the order now with [HLT-NAACL 2006](https://nlp.cs.nyu.edu/hlt-naacl06/), and for good measure let's use a slash in [HLT/NAACL 2004](http://mirror.aclweb.org/hlt-naacl04/); wait, we really wanted a dash in the beginning, with [HLT-NAACL 2003](http://mirror.aclweb.org/hlt-naacl03/) (bonus, that page refers to HLT-NAACL 2004). So the choice is inconsistent citations vs. regularization the name (which technically citing a proceedings volume that never existed).

## Latex

### Finer Points of Punctuation

+ Learn the difference between [an hyphen, en-dash, and em-dash](http://www.thepunctuationguide.com/hyphen-and-dashes.html).

  + It's `key--value` as in `key--value` store, not `key-value`.

  + It's `human--computer interaction`. Note that the [Wikipedia article](https://en.wikipedia.org/wiki/Human%E2%80%93computer_interaction) gets it right and [this incorrect URL](https://en.wikipedia.org/wiki/Human-computer_interaction) redirects to the correct article.

+ Footnotes go after the punctuation, as in `End of sentence.\footnote{...}`. Note, there is _no_ space between punctuation and the footnote.

+ There is a difference between end-of-sentence spacing and intra-sentence spacing after a period. For example, `cat vs.\ dog` but `I like cats. She likes dogs.`

+ Cite a reference as `Lin et al.~\cite{Lin}`. Note `~` prevents ugly breaks.

### Misc

+ Latex does weird hyphenation on line breaks sometimes. For example, analysis might get hyphenated as "anal-ysis", which just looks dirty. MapReduce gets hyphenated as "MapRe-duce", which bugs me. Insert in the preamble `\hyphenation{Map-Reduce}` to specify particular hyphenations you want, or use `\mbox{...}` to suppress hyphenation.

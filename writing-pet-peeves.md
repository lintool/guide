# Writing Pet Peeves

## Organization

+ **Explicit "roadmaps" in prose.**
By this, I mean a paragraph like "In Section 2 we provide background... Section 3 describes our model... Experimental results are presented in Section 4."
These are useless and an absolute waste of space.
Why spend a paragraph describing what I already expect (i.e., all research papers share similar structure) and what I could figure out in two seconds (i.e., I could simply flip ahead and read your section titles).

+ **Implicit narrative roadmaps.**
Instead, let your prose implicitly lay out the structure of the paper for your reader.
For example, if I say that my model has three novel features, then in the methods section there should be three subsections, each corresponding to each novel feature.

+ **Use consistent terminology.**
Use the same words to describe your methods, contributions, etc. throughout the paper.
Don't say "soft alignment between words in phrases in the question and answer" in one place and then talk about "soft semantic matching" if you mean for them to be the same thing.
Especially technical terms that sound similar but are slightly different, like in the example above.
Don't confuse your reader.
If stylistically the prose comes out too repetitive and mechanical, then consider mixing verbal and nominal forms, e.g., "matching at the semantic level" and "semantic matching", but make sure they _clearly_ mean the same thing.

## Grammar and Style

+ **Use of the term "performance".** Treatments across different sub-disciplines of computer science differ, but "performance" generally refer to measures like latency, throughput, etc. NLP researchers, however, often use "performance" to refer to "output quality", which sometimes throws me off. I like to be as precise as possible. For IR papers, I always use "effectiveness" to refer to output quality; otherwise, I like to explicitly say "accuracy" or "perplexity" if warranted. In IR papers, I typically use "efficiency" to refer to what other fields call "performance" (since IR folks routinely talk about effective/efficiency tradeoffs; it's well-established parlance), but where ever possible I like to be precise (e.g., lower query latency, higher query throughout, etc.). As a corollary I tend to avoid phrases like "performs well".

+ **Use of superlatives and "hype phrases".** In short, use sparingly - things like "dramatically improves the user experience" - unless it's actually warranted. If you improve precision from 0.4 to 0.8, calling the improvements _dramatic_ might be warranted. A 5% improvement is not. I would let the results speak from themselves. Overuse of superlatives potentially turns off reviewers.

+ **Use of the term "significant".** Related, use the term _significant_ only in the technical sense of statistically significant.

+ **Use of "STOA".** "State of the art" as a noun is written without hyphens, as in "Our algorithm represents the state of the art". As an adjective, "start-of-the-art" is hyphenated, as in, "These are state-of-the-art results".

+ **Hyphenate the compound adjectives.**
"run" + "time" = ??? The answer is [this](https://homes.cs.washington.edu/~jrw12/runtime.html).
More generally, adjectival forms (i.e., [compound adjectives](https://www.grammarbook.com/punctuation/hyphens.asp)) are hyphenated, i.e., "machine learning" but "machine-learned models".
STOA is a common special case of this.

+ **Use of training and test sets.** It's "training set", "validation test", and "test set". Not "testing set". I know, it's odd. I think the non-parallel construction is just idiosyncratic, since "train set" sounds odd.

+ **Stay in the same tense.**
Some authors like to describe experiments in the past tense, e.g., "The user received a push notification and clicked on it." Others like to describe experiments in the present tense, e.g., "The user receives a push notification and clicks on it." Both are fine, but stay consistent in the same tense. Don't write, "The user receives a push notification and clicks on it. The click was then recorded by the server."

+ **Related work.** "Related work", _not_ "related works". "Work" is a collective noun, like "staff". You don't write "research staffs". Wait, you ask: if this is indeed the case, why would you write ["DaVinci is the creator of several famous _works_ of art"](https://twitter.com/mmparker/status/991012314332545024)? Well, that's a completely different context: "work" in "related work" is intended to refer to a body of work collectively, as in "the literature". You don't write "related literatures" (well, except in a very narrow sense, something like "isolated silos of related literatures"). Note that "DaVinci's work" and "DaVinci's works" are both fine, but in different contexts. The first might refer to his body of work collectively; the second focuses on individual pieces. Also, be aware of subject-verb agreement.

+ **Subject-verb agreement issues.** Common subject-verb (note that in Latex this would be an en-dash, see below) agreement issue: "number of sample increases", not "increase". The verb agrees with the head noun, which is number, singular in this case.

+ **Always use the [Oxford Comma](https://en.wikipedia.org/wiki/Serial_comma)**.

## Appearance

+ **Aesthetics matter.**
I often take a paper, zoom out in my PDF viewer so the text is unreadable, flip through the pages, and see if it "looks right".
Does it have the right balance of sections, sub-sections, figures, equations, tables, etc.?
Unfortunately, I can't operationalize this into an imperative, other than to say that "appearances count".

+ **Get rid of orphan lines.**
Orphan lines are final lines in paragraphs that are really short, e.g., a single word on its own line that ends a paragraph.
Get rid of them by rewriting the prose slightly.
This is a common space-saving trick.
Never have orphan lines that span page break, i.e., a single word or short phrase that ends a paragraph on a new page.
Latex does this sometimes and it looks terrible.

+ **Opposite of orphan lines.**
If the final line of a paragraph runs all the way to the rightmost edge of the column or page, it looks terrible also because the looks like a run-on with the next paragraph.
Rewrite slightly so this doesn't happen.

## Citations

+ **NEVER *ever* begin a sentence with a citation.** For example, "[5] explored the use of..." The worst is related work that's simply a collection of such sentences, e.g. "[1] did this... [2] did that... [3] did other".

+ **A citation is not a noun phrase.** For example, "... is shown in [5]" is bad; should be "... is shown by Smith et al. [5]". However, I break this rule myself sometimes, especially if I'm trying to save a bit of space.

+ **Name your proceedings volumes consistently in the bibliography.**
I hate seeing "SIGIR 2015", "Proceedings of SIGIR 2014", "SIGIR'12", and "Proceedings of the 40th International ACM SIGIR Conference on Research and Development in Information Retrieval" all in the same bibliography.
The fact that NAACL can't even consistently name its conferences from year to year drives me nuts: it's [NAACL HLT 2018](http://naacl2018.org/) (with a space), before it was [NAACL-HLT 2012](http://mirror.aclweb.org/hlt-naacl12/) (with a dash); back to a space with [NAACL HLT 2010](https://naaclhlt2010.isi.edu/), back to a dash with [NAACL-HLT 2007](http://mirror.aclweb.org/hlt-naacl07/); oh, let's swap the order now with [HLT-NAACL 2006](https://nlp.cs.nyu.edu/hlt-naacl06/), and for good measure let's use a slash in [HLT/NAACL 2004](http://mirror.aclweb.org/hlt-naacl04/); wait, we really wanted a dash in the beginning, with [HLT-NAACL 2003](http://mirror.aclweb.org/hlt-naacl03/) (bonus, that page refers to HLT-NAACL 2004).
So the choice as an author referencing papers is inconsistent citations vs. regularizing the name (which is technically citing a proceedings volume that never existed).

## Polish

+ **Fixed-point reading.** This is a technique that I've found to be time consuming but effective in catching typos and final polishing (e.g., for camera-ready submissions).
I named this technique after the [fixed-point combinator](https://en.wikipedia.org/wiki/Fixed-point_combinator).
Here's what I do:
I print out the paper (yes, on dead trees) and read over with a pen in hand.
To make sure I actually read each word (and not miss typos), I _point_ to each word with my pen.
I then enter all corrections into latex.
At first, I catch a lot of typos.
Then I do it again.
I catch fewer typos.
Then I do it again.
And even fewer.
I repeat until I take a pass and find nothing more I wish to change (or the number of corrections is below a threshold _epsilon_).
This typically takes around half a dozen passes for me.
A few details: 

  + Somehow for me, printing on dead trees is critical to catching typos.
  + I've done this on screen and with an iPad, and it somehow doesn't work quite as well: I print out on dead trees and I still find more typos.
  + _Pointing_ to each word is critical, to make your eyes [saccade](https://en.wikipedia.org/wiki/Saccade) to it; otherwise your brain has a tendency to just interpolate and error-correct the typos.
  + To combat fatigue and learning effects, in each pass I vary the order in which I read sections: e.g., start with the intro, start from the conclusion, start from the experiments, etc.

## Latex

### Finer Points of Punctuation

+ [Details matter!](https://twitter.com/aacooper/status/1109678683877310464)

+ Learn the difference between [an hyphen, en-dash, and em-dash](http://www.thepunctuationguide.com/hyphen-and-dashes.html).

  + It's `key--value` as in `key--value` store, not `key-value`.

  + It's `human--computer interaction`. Note that the [Wikipedia article](https://en.wikipedia.org/wiki/Human%E2%80%93computer_interaction) gets it right and [this incorrect URL](https://en.wikipedia.org/wiki/Human-computer_interaction) redirects to the correct article.

+ Footnotes go after the punctuation, as in `End of sentence.\footnote{...}`. Note, there is _no_ space between punctuation and the footnote.

+ There is a difference between end-of-sentence spacing and intra-sentence spacing after a period. For example, `cat vs.\ dog` but `I like cats. She likes dogs.`

+ Cite a reference as `Lin et al.~\cite{Lin}`. Note `~` prevents ugly breaks.

### Appearance

+ **Watch out for overfull lines.**
Latex does its best to lay out lines in paragraphs, hyphenating words as necessary.
Sometimes, however, it can't do so and will just give up, in which case, it'll let words spill into the margin.
Knuth's design decision was that, instead of producing something that would be distasteful to a discerning typographer, the system should force the author to "deal with it".
The problem is that many authors forget to "deal with it", and so sometimes final versions of papers have terrible overfull lines; see [multiple examples in this classic paper](https://dl.acm.org/citation.cfm?id=1076115).
Sometimes, manually forcing hyphenation works; otherwise, a minor rewrite will do the trick.
Either way, "deal with it"!

+ **Watch out for weird hyphenation.**
Latex does weird hyphenation on line breaks sometimes. For example, analysis might get hyphenated as "anal-ysis", which just looks dirty. MapReduce gets hyphenated as "MapRe-duce", which bugs me. Insert in the preamble `\hyphenation{Map-Reduce}` to specify particular hyphenations you want, or use `\mbox{...}` to suppress hyphenation.



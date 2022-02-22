# Writing Pet Peeves

## Organization

+ **Use consistent terminology.**
Use the same words to describe your methods, contributions, etc. throughout the paper.
Don't say "soft alignment between words in phrases in the question and answer" in one place and then talk about "soft semantic matching" if you mean for them to be the same thing.
Especially technical terms that sound similar but are slightly different, like in the example above.
Don't confuse your reader.
If stylistically the prose comes out too repetitive and mechanical, then consider mixing verbal and nominal forms, e.g., "matching at the semantic level" and "semantic matching", but make sure they _clearly_ mean the same thing.
Don't do this, even for things that _you_ think mean the same thing.
For example, "neural seq2seq model", "seq2seq neural network", and "seq2seq neural model" are all roughly interchangeable, but there are nuanced differences in emphasis.
If you mix these references, the reader might infer that you are trying to establish some contrast that is likely not your intention.

+ **Use parallel structure.**
Use parallel structure throughout your paper to help your reader quickly grasp what you are trying to convey. For example:

  - If you describe three models in your methods section, then make sure that in your results section, the tables or figures show results on those same three models, _in the same presentation order_, with _exactly_ the same name (see point about consistency above).
  - If you organize your paper in terms of research questions (RQs), you'll present your RQs in the intro.
    Make sure in the results section that each RQ is answered, _in the same order_, clearly delineated (e.g., with subsections).
  - If you claim four model innovations in your introduction, then your methods section should discuss each innovation _in the same order_; ideally, your experiments will show ablations for each of these innovations.

  It would be ideal if you can extend the parallel structure consistently throughout the entire paper, from abstract to conclusion.
  For example,
  
  - abstract: this paper is about two innovations, A1 and A2; 
  - introduction: here is why A1 and A2 are important; 
  - related work: A1 is related to this, A2 is related to that; 
  - methods: see how A1 and A2 translate directly to M1 and M2; 
  - results/discussion: I'll show you that M1 and M2 empirically work and M1+M2 work even better;
  - conclusion: you should now care about A1 and A2.

+ **Explicit "roadmaps" in prose.**
By this, I mean a paragraph like "In Section 2 we provide background... Section 3 describes our model... Experimental results are presented in Section 4."
These are useless and an absolute waste of space.
Why spend a paragraph describing what I already expect (i.e., all research papers share similar structure) and what I could figure out in two seconds (i.e., I could simply flip ahead and read your section titles).
An exception to this rule is for theses, where it is common to write something like, "In Chapter 3, I present my model for..."
However, what follows is typically a paragraph summary of the chapter, so all considered, a roadmap that spans several paragraphs (or often, a bulleted list) isn't that jarring.

+ **Implicit narrative roadmaps.**
Instead, let your prose implicitly lay out the structure of the paper for your reader.
For example, if I say that my model has three novel features, then in the methods section there should be three subsections, each corresponding to each novel feature.
This is merely an elaboration of the "use parallel structure" guidance above.

## Grammar and Style

+ **Possessives.**
In English, "A's B" and "B of A" are both acceptable ways to indicate possession.
This is mostly personal style, but I prefer "B of A" since it reads more natural to me.
So, I would prefer "popularity of dense retrieval" over "dense retrieval's popularity".
The issue in my mind is the scoping of the possessive morpheme: the actual syntactic structure of the latter is "[ dense retrieval ] 's popularity".
As the noun phrase corresponding to the possessor increases in complexity, I find the possessive construction increasingly awkward.
For example, "state-of-the-art dense retrieval models' popularity" is grammatically correct but I find difficult to read.
I would rephrase as "the popularity of state-of-the-art dense retrieval models".

  I encounter this issue frequently with native Mandarin speakers, likely because of 的-constructions, where the A in "A 的 B" can be arbitrarily complex.
For example, "[ I want to go ] 的 place" (word for word gloss; translation: "the place where I want to go") is perfectly grammatical in Mandarin, whereas in English there is no grammatical counterpart using the possessive morpheme.

+ **Use of the term "performance".** Treatments across different sub-disciplines of computer science differ, but "performance" generally refers to measures like latency, throughput, etc.
NLP (and often IR) researchers, however, often use "performance" to refer to "output quality", which annoys me.
This is especially annoying in papers that _actually_ discuss performance (for example, on model compression), because "better performance" is ambiguous between "faster" (e.g., lower inference latency) and "better" (e.g., higher prediction accuracy).

  I like to be as precise as possible.
In IR papers, I typically use "effectiveness" to refer to output quality in the general sense.
In NLP papers, I either use "effectiveness" ("our model is more effective") or "output quality" ("our model produces higher quality output").
Unless the prose becomes awkward (e.g., when comparing many different metrics that measure different things), I try to be as precise as possible with terms like "accuracy", "precision", "recall", "loss", "likelihood", "BLEU score", "ROUGE score", "perplexity", etc. as appropriate.
(Side note, writing something like "higher BLEU/ROUGE scores" makes a factual statement without getting into a debate on whether higher BLEU/ROUGE scores actually yield better translations/summaries.)

  In all papers, I typically use "efficiency" to refer to what other sub-disciplines call "performance" (since IR folks routinely talk about effectiveness/efficiency tradeoffs; it's well-established parlance), but where ever possible I also like to be precise, e.g., lower query latency, higher query throughout, less training time, etc.

  As a corollary, I tend to avoid phrases like "performs well".
An exception, however, is the verb "to outperform", which I sometimes use, since in English there is no verbal form that conveys more precision, e.g., "to outprecise".
So I might write "our model outperforms the baseline" to either mean "faster" or "better output quality"; often, the sense is clear from context.

+ **Use of superlatives and "hype phrases".** In short, use sparingly - things like "dramatically improves the user experience" - unless it's actually warranted. If you improve precision from 0.4 to 0.8, calling the improvements _dramatic_ might be warranted. A 5% improvement is not. I would let the results speak from themselves. Overuse of superlatives potentially turns off reviewers.

+ **Use of the term "significant".** Related, use the term _significant_ only in the technical sense of statistically significant.

+ **Use of "SOTA".** "State of the art" as a noun is written without hyphens, as in "Our algorithm represents the state of the art". As an adjective, "start-of-the-art" is hyphenated, as in, "These are state-of-the-art results".
Also, don't forget the determiner in the nominal form, i.e., _the_ state of the art.

+ **Use of training and test sets.** It's "training set", "validation test", and "test set". Not "testing set". I know, it's odd. I think the non-parallel construction is just idiosyncratic, since "train set" sounds odd.

+ **"Plural" of words like "performance", "effectiveness", "evidence", etc.** The "performance of different models", _not_ "performances of different models". Same with "effectiveness" and "evidence". Mistake also appears in forms like "evidences from multiple experiments support our hypothesis".

+ **Continuation of above... you probably don't mean "codes".** If you're talking about source code, the source code of two different programs is still "source code", not "source codes".
Unless you mean something like "Huffman codes"...

+ **Another continuation of above... the case of analysis vs. analyses.** "Analysis" vs. "analyses" is an interesting case.
I personally have a slight preference for analysis, but analyses sounds fine in most contexts.
In an analysis, you might be running multiple trials, tests, ablations, etc., so it might be tempting to use the plural.
However, even if you do run multiple tests to analyze something (e.g., "Is A better than B?"), at least to me, it is more natural to call it an analysis (singular).
What if you're analyzing different things?
For example, "parameter analysis" or "parameter analyses"?
In this specific case, I have a strong preference for the former, even if you're analyzing multiple parameters.
But what if you're analyzing two completely different hypotheses?
For example, "In this analysis/these analyses we examine our proposed hypotheses..."
I think both sound fine to me.

+ **Hyphenate compound adjectives.**
"run" + "time" = ??? The answer is [this](https://homes.cs.washington.edu/~jrw12/runtime.html).
More generally, adjectival forms (i.e., [compound adjectives](https://www.grammarbook.com/punctuation/hyphens.asp)) are hyphenated, i.e., "machine learning" but "machine-learned models".
SOTA is a common special case of this.
Hyphenation rules are actually much more complex... see [this guide](https://www.dailywritingtips.com/adverbs-and-hyphens/) for more details.
The Chicago Manual of Style has [an even more complex list of rules](https://docs.google.com/viewer?url=https://github.com/lintool/guide/blob/master/docs/CMS_list.pdf?raw=true).

+ **Be consistent in the capitalization of hyphenated words.** This applies in paper titles and section headings. For words like "multi-aspect" and "cross-lingual", be consistent. Don't have "Multi-aspect" in one place and "Cross-Lingual" in another.

+ **Stay in the same tense.**
Some authors like to describe experiments in the past tense, e.g., "The user received a push notification and clicked on it." Others like to describe experiments in the present tense, e.g., "The user receives a push notification and clicks on it." Both are fine, but stay consistent in the same tense. Don't write, "The user receives a push notification and clicks on it. The click was then recorded by the server."

+ **Tense when describing experiments.**
Related to the above point.
Some authors describe experiments in the present tense, e.g., "We apply our models on three benchmark datasets."
I think this is fine, but personally, I prefer past tense, e.g., "We applied our models on three benchmark datasets."
This makes a sequence like the following sound more natural, e.g., "We applied our models on three benchmark datasets. Based on preliminary experiments, a fourth dataset was discarded because..."
In consistent present tense, the above sequence sounds really odd, "We apply our models on three benchmark datasets. Based on preliminary experiments, we discard a fourth dataset / a fourth dataset is discarded (?) because..."
Writing about experiments in the past tense more accurately mirrors reality; you already ran those experiments, now you're just describing them.

+ **Related work.** "Related work", _not_ "related works". "Work" is a collective noun, like "staff". You don't write "research staffs". Wait, you ask: if this is indeed the case, why would you write ["DaVinci is the creator of several famous _works_ of art"](https://twitter.com/mmparker/status/991012314332545024)? Well, that's a completely different context: "work" in "related work" is intended to refer to a body of work collectively, as in "the literature". You don't write "related literatures" (well, except in a very narrow sense, something like "isolated silos of related literatures"). Note that "DaVinci's work" and "DaVinci's works" are both fine, but in different contexts. The first might refer to his body of work collectively; the second focuses on individual pieces. Also, be aware of subject-verb agreement.

+ **Mass vs. count nouns.** "Related work" is actually a specific instance of the mass/count dichotomy in English. What makes it confusing is that for many words, both count and mass interpretations are possible. For example, "Over the course of several internships, I have gained experience in deep learning" (_not_ "experiences"). But, "I love having new experiences when visiting different countries". We write, "Preceding sentences form the context of the dialogue" (_not_ "contexts"), but "In different contexts, people may act differently".

+ **Subject-verb agreement issues.** Common subject-verb (note that in Latex this would be an en-dash, see below) agreement issue: "number of sample increases", not "increase". The verb agrees with the head noun, which is number, singular in this case.

+ **Learn the difference between "that" and "which".** There are already lots of explanations available on the web, so there's no need for me to repeat them: [here's](https://blog.apastyle.org/apastyle/2012/01/that-versus-which.html) a good one.

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
Rewrite the text slightly so this doesn't happen.

## Citations

+ **NEVER *ever* begin a sentence with a citation.** For example, "[5] explored the use of..." The worst is related work that's simply a collection of such sentences, e.g. "[1] did this... [2] did that... [3] did other".

+ **A citation is not a noun phrase.** For example, "... is shown in [5]" is bad; should be "... is shown by Smith et al. [5]". However, I break this rule myself sometimes, especially if I'm trying to save a bit of space.

+ **Name your proceedings volumes consistently in the bibliography.**
I hate seeing "SIGIR 2015", "Proceedings of SIGIR 2014", "SIGIR'12", and "Proceedings of the 40th International ACM SIGIR Conference on Research and Development in Information Retrieval" all in the same bibliography.
The fact that NAACL can't even consistently name its conferences from year to year drives me nuts: it's [NAACL HLT 2018](http://naacl2018.org/) (with a space), before it was [NAACL-HLT 2012](http://mirror.aclweb.org/hlt-naacl12/) (with a dash); back to a space with [NAACL HLT 2010](https://naaclhlt2010.isi.edu/), back to a dash with [NAACL-HLT 2007](http://mirror.aclweb.org/hlt-naacl07/); oh, let's swap the order now with [HLT-NAACL 2006](https://nlp.cs.nyu.edu/hlt-naacl06/), and for good measure let's use a slash in [HLT/NAACL 2004](http://mirror.aclweb.org/hlt-naacl04/); wait, we really wanted a dash in the beginning, with [HLT-NAACL 2003](http://mirror.aclweb.org/hlt-naacl03/).
So the choice as an author referencing papers is inconsistent citations vs. regularizing the name (which is citing a proceedings volume that never existed).

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

+ Here's an interesting way to proofread: [say the text back to you](https://kmicinski.com/writing/2017/09/22/reading-text-back/).

## Latex

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">pro·fes·sor — noun<br>***the member of a research lab with the deepest intuitions about how LaTeX \vspace, page breaks, and figure placement work.***</p>&mdash; Zachary Lipton (@zacharylipton) <a href="https://twitter.com/zacharylipton/status/1282700969386684422?ref_src=twsrc%5Etfw">July 13, 2020</a></blockquote>

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">And correctly distinguish uses of hyphens, n-dashes, and m-dashes.</p>&mdash; Jimmy Lin (@lintool) <a href="https://twitter.com/lintool/status/1282725293895979008?ref_src=twsrc%5Etfw">July 13, 2020</a></blockquote>

### Finer Points of Punctuation

+ [Details matter!](https://twitter.com/aacooper/status/1109678683877310464)

+ Learn the difference between [an hyphen, en-dash, and em-dash](http://www.thepunctuationguide.com/hyphen-and-dashes.html).

  + It's `key--value` as in `key--value` store, not `key-value`.

  + It's `human--computer interaction`. Note that the [Wikipedia article](https://en.wikipedia.org/wiki/Human%E2%80%93computer_interaction) gets it right and [this incorrect URL](https://en.wikipedia.org/wiki/Human-computer_interaction) redirects to the correct article.

  + It's one of my favorite obscure rules, but yes, there are cases when you mix an en-dash and a hyphen _in the same word_! See [this explanation](https://www.thepunctuationguide.com/en-dash.html). In things that we are likely to write, "pre--fine-tuning" is one such word.

+ Footnotes go after the punctuation, as in `End of sentence.\footnote{...}`. Note, there is _no_ space between punctuation and the footnote.

+ There is a difference between end-of-sentence spacing and intra-sentence spacing after a period. For example, `cat vs.\ dog` but `I like cats. She likes dogs.`

+ Cite a reference as `Lin et al.~\cite{Lin}`. Note `~` prevents ugly breaks.

### Appearance

+ **Watch out for overfull lines.**
Latex does its best to lay out lines in paragraphs, hyphenating words as necessary.
Sometimes, however, it can't do this _well_ (according to its internal algorithm) and will just give up, in which case, it will let words spill into the margin.
Knuth's design decision was that, instead of producing something that would be distasteful to a discerning typographer, the system should force the author to "deal with it".
The problem is that many authors forget to "deal with it", and so sometimes final versions of papers have terrible overfull lines; see [multiple examples in this classic paper](https://dl.acm.org/citation.cfm?id=1076115) (just to pick on a random example).
Sometimes, manually forcing hyphenation works; otherwise, a minor rewrite will do the trick.
Either way, "deal with it"!

+ **Watch out for weird hyphenation.**
Latex does weird hyphenation on line breaks sometimes. For example, analysis might get hyphenated as "anal-ysis", which just looks dirty. MapReduce gets hyphenated as "MapRe-duce", which bugs me. Insert in the preamble `\hyphenation{Map-Reduce}` to specify particular hyphenations you want, or use `\mbox{...}` to suppress hyphenation.

## Cross-Paper Consistency

+ **Choose your name... wisely.**
Choose the name you want to use professionally in your papers ("professional name") and make sure to stick to that form _exactly_, across all your publications.
For a typical "anglicized name", decide if you want to include your full middle name, just the middle initial, or no middle name at all.
This will help various scholarly aggregators do their thing (e.g., Google Scholar, DBLP, etc.).
I regret that in some early publications I was inconsistent between "Jimmy J. Lin" and "Jimmy Lin" (until I started exclusively using only the latter form).
A few additional issues to consider:

    - If you decide to use a professional name that is _not_ the same as your legal name, you might run into issues with governmental authorities. A common case is if you need a visa, the invitation letter is likely going to reference your professional name (or the paper itself, obviously), which will not match your legal name (on your passport). There are of course ways around this, but beware of the additional hassles.
    - For people whose surnames comprises two tokens, be aware of a bunch of annoying corner cases. I'll use "Zeynep Akkalyoncu Yilmaz" as a specific example. Properly, "Akkalyoncu Yilmaz", is the surname, but most people will likely parse out "Yilmaz" as the surname, leading to the proliferation of variants like "Zeynep Yilmaz" and "Zeynep A. Yilmaz" with automatically generated tools. Citations will also appear as Yilmaz et al. (2019). Yes, there is a way to make bibtex "do the right thing", but most authors aren't going to (and if you cite yourself correctly, that might confuse the readers). There aren't good alternatives to deal with these cases; either (a) accept that your name will be mangled, or (b) proactively manage the situation by using a professional name that's different from your given name (and more easily and consistently parsed).
    - For people whose names comprise accent characters, similar advice applies also. If you decide to retain accent characters, then be prepared that your name might be mangled in some cases. The alternative of just writing your name consistently without accents would be a reasonable alternative.

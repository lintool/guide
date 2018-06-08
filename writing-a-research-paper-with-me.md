
# Writing a Research Paper With Me

I can't stress this enough. Start early.

## Writing Order

Start writing your paper from the results section. In fact, start with
the results figures or tables. Usually, we would have discussed the
contribution claims of the paper well in advance. Make sure the
results support those claims. For example, if your claimed
contribution is to demonstrate that technique *X* improves over
competitive baselines for task *Y*, there'd better be a results table
(or figure) that shows technique *X* vs. competitive
baselines. Typically, there will be a main set of results and a set of
secondary results that flesh out your experiments, e.g., exploring
different parameter settings, ablation experiments where you examine
the impact of different components, etc.

Once you're done with the results section, write the experimental
setup section. This includes things like what dataset you used, the
machine/cluster you ran your experiments on, training regime,
hyperparameter settings, etc.

Once you're done with the results section, write the methods
section. That is, how your model actually works, the architecture of
your system, etc.

Then write your related work. I've noticed over the years that systems
and DB papers tend to have related work late in the paper, e.g., after
results, but other fields (IR, NLP, KDD, etc.) tend to have related
work right after the intro. So I usually follow these community
standards. In the latter case I usually call the section "Background
and Related Work", directly following the introduction.

Save the introduction for last.

## Different Sections of the Paper

### Results

Walk your reader through the results.
Don't just throw up a big table and lots of numbers and expect the reader to figure out what's going on.
For example, something like, "The baseline is shown in the top row... our technique is shown on the row below... based on this, we can clearly see that our model yields significantly higher precision across all datasets."

### The Story

The introduction is
where you "tell the story" and attempt to convince the reviewer why
they should care, relating the work to the broader context of what
people in the field consider important. 

At the end of the introduction, I typically include an explicit contributions paragraph, e.g., "We believe this work makes the following contributions..."
Writing the contributions is difficult, but a necessary part of academic writing.
It is absolutely essential that claimed contributions are supported (empirically or otherwise) in the paper.
Typically, these claims evolve with the rest of the paper: for example, initially, we expect our experimental results to support one assertion, but then the results are a bit unexpected, so we need to tweak our claim.
Or, alternatively, we would like to strengthen our claim or make a slightly different assertion, so this leads running slightly different experiments as support.
It is not unusual for these changes to happen in a few rounds before we finally converge on a set of claims we're happy with and the evidence that supports those claims.

## My Input

If you're a junior student, I will usually write the introduction for you, because that's the hardest part to write (see above).
As you gain experience, I expect you to be able to start telling your own story.
This is the hardest skill to master.

Typically, I will communicate with you about a rough time period where
I will set aside time to help you with your paper. Help consists of
two forms: (1) reading and giving feedback, and (2) substantially
revising your paper.

In many cases, especially if you are a junior student, I will probably
end up completely rewriting your paper such that the final product may
contain the same ideas, algorithms, models, results, but with a
completely different expression. Realize that this is the most
valuable part of your interactions with me: this is where you get my
undivided attention working on *your* problem, helping you refine and
improve your work. These interactions are also where you learn to
write research papers. For example:

+ I help you explain your complex algorithm in the simplest possible
way that helps the reader understand its underlying intuitions.

+ I help you untangle your experimental results into a series of clear
findings that reveals insights about your system or technique.

These cases focus on how to clearly articulate your ideas, so it is
important that your draft already contains the "raw ingredients". For
example, there should already be a rough attempt at explaining the
algorithm or model in a sufficient level of detail. All the
experimental results should be present for analysis. I call this the
"fodder" that serves as the input to refined prose.

An implication of this is that it is in your best interest to get
everything in the draft before I start to work on it. While I'm
working on it, also be available on Slack to answer questions on
missing details. If there is "not enough" for me to work on or if you
are not responsive, I will context switch and work on other things. I
try to minimize my context switches so it might be a while until I
return to your paper.

The proportion of time I spend substantially revising your paper will
decrease as you gain experience. For senior students, I might write
the introduction and that's it. For students close to graduating and
postdocs, I might only read a close-to-final draft to offer comments
with no "hands-on-keyboard" work. For postdocs, I might not even be a
co-author.

If you are unclear what type of help you are going to get from me,
**ask**! I will be clear and up front to you and say things like, "I'll
have all of Thursday morning to devote to your paper" or "I have too
many other deadlines. I'll write your introduction but otherwise you
are on your own."

## After I've Done a Major Rewriting Pass

### Comparing Before and After

For any part of your paper that I have rewritten, it is important that
you compare "before" and "after" (look at the `git` commit), for three
reasons:

1. I might have messed up your text. For example, I might have
described your algorithm wrong.

2. Comparing "before" and "after" is critical to your learning
experience. This is a case study approach: you will see how I have
better re-expressed your ideas, and over time, your own ability to do
so will improve. If you have questions about why I have expressed
something in a certain manner, ask and I will be happy to explain.

3. I may not have actually improved the writing. Senior students come
up with better ways of "telling the story" than I do. I will engage
with you and vigorously debate the merits of alternative approaches. I
will certainly concede if your approach is superior, and I will most
likely defer to your own judgment if there are pros and cons to
alternative approaches. I very much welcome these debates and they are
satisfying, because it means that I have trained you well. I am not
surprised that you can tell your story better than I can, because,
after it, it is *your* research.

### Smoothing Pass

After I've done a major rewriting of sections in your paper, you need to do what I call a "smoothing pass".
That is, go back through the entire paper and make sure the writing is consistent.
For example, if in the introduction I use a particular phrase to describe a technique, then make sure the phrasing is propagated forward in the results section.
See ["use consistent terminology"](https://github.com/lintool/guide/blob/master/writing-pet-peeves.md).


# Writing a Research Paper With Me

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">:<a href="https://twitter.com/squarecog?ref_src=twsrc%5Etfw">@squarecog</a> to me: dude, you&#39;re just a glorified technical writer.</p>&mdash; Jimmy Lin (@lintool) <a href="https://twitter.com/lintool/status/205133813330870272?ref_src=twsrc%5Etfw">May 23, 2012</a></blockquote>

I can't stress this enough.
Start early.
Most students grossly underestimate the time they take to write.

## Plan to Run Experiments Twice

Plan to run your experiments twice.
The first time is to figure out what experiments you need to run, the second time is to actually run them for inclusion in the paper.

Why?
Because when you run your experiments for the first time, you don't know the relevant experimental factors.
You may have some ideas, but you don't know definitively, because otherwise you wouldn't need to run the experiments.
Inevitably, you'll discover something you didn't know before, which is the whole point of research.
A set of experiments will inform a previous set of experiments, which will compel you to go back to the first experiment to verify.
In these cases, you might be comparing experiment results from today with a condition you tried some time ago (maybe a week, maybe months).
Lots of things might have changed in the meantime (the code has changed slightly, for example).
Thus, it's better to just run through all the experiments again.

For the second time through, you should be able to script all your experimental conditions:
if you can't it is likely that you don't understand the design or parameter space well enough.
Make sure your code is able to execute all the conditions through command-line parameters or an external config file.
Preliminary exploration is okay, but if you intend for a set of results to make its way into a paper, _never_ run those experiments by code modifications (e.g., commenting out a line) &mdash; turn them into command-line options.
Otherwise, it will be virtually impossible (especially over time) to keep track of which code led to which results.

## Don't Procrastinate on Writing by More Coding

Most students find it easier to build implementations (and run experiments, etc.) than to write papers.
So, they put off writing the paper and continue coding, even when they've collected enough experimental results for their paper.
Recognize that this happens (it's okay, I see it all the time), but resist the urge.

## Writing Order

Start writing your paper from the results section.
In fact, start with the results figures or tables.
Usually, we would have discussed the contribution claims of the paper well in advance.
Make sure the results support those claims.
For example, if your claimed contribution is to demonstrate that technique *X* improves over competitive baselines for task *Y*, there'd better be a results table
(or figure) that shows technique *X* vs. competitive baselines.
Typically, there will be a main set of results and a set of secondary results that flesh out your experiments, e.g., exploring different parameter settings, ablation experiments where you examine the impact of different components, etc.
Focus on the main results first.

Even if you don't have all the experimental results yet, you can still set up the results tables (with missing entries) or put in a stub for a figure.
As your experiments progress, it's a matter of filling in values in an empty table, or adding another line in a plot...
Having these placeholder will allow you to proceed concurrently on the prose.

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

If you're a junior student, I often write the introduction for you, because that's the hardest part to write (see above).
As you gain experience, I expect you to be able to start telling your own story.
This is the hardest skill to master.

Typically, I will communicate with you about a rough time period where I will set aside time to help you with your paper.
My input is usually in the form of one of the following: (1) reading and giving feedback, (2) substantially revising your paper directly, and (3) meta-writing.

In some cases, especially if you are a junior student, I may end up completely rewriting your paper such that the final product may contain the same ideas, algorithms, models, results, but with a completely different expression.
Realize that this is the most valuable part of your interactions with me: this is where you get my undivided attention working on *your* problem, helping you refine and improve your work.
These interactions are also where you learn to write research papers. For example:

+ I help you explain your complex algorithm in the simplest possible way that helps the reader understand its underlying intuitions.

+ I help you untangle your experimental results into a series of clear findings that reveals insights about your system or technique.

These cases focus on how to clearly articulate your ideas, so it is important that your draft already contains the "raw ingredients". 
For example, there should already be a rough attempt at explaining the algorithm or model in a sufficient level of detail.
All the experimental results should be present for analysis.
I call this the "fodder" that serves as the input to refined prose.

An implication of this is that it is in your best interest to get everything in the draft before I start to work on it.
While I'm working on it, also be available on Slack to answer questions on missing details.
If there is "not enough" for me to work on or if you are not responsive, I will context switch and work on other things.
I try to minimize my context switches so it might be a while until I return to your paper.

For more senior students, instead of actually editing your paper, I often do what I call "meta-writing", which is writing what you should write about&mdash;directly into your draft (e.g., on Overleaf).
This often appears in red font, so it's difficult to miss.
Examples of meta-writing include reorganization suggestions, e.g., "you should move the model description here to improve the flow",
missing logical chains of reasoning, e.g., "here you're missing the argument that recall is the most important metric for this task",
specific requests, e.g., "let's cherry pick a better example here", etc.
When I do this, I leave the implementation of the suggestions up to you, i.e., to execute a suggestion into fluent prose that flows smoothly with the surrounding text.
Often, my meta-writing is fragmentary, frequently not even complete sentences.
Sometimes, my meta-writing might contain colorful language, like, "here you want to say, this is stupid", and "here, you want to brag about your results".
Obviously, you should turn these suggestions into academically acceptable writing.

The proportion of time I spend substantially revising your paper will decrease as you gain experience.
For more senior students, I might mostly focus on meta-writing and leave the excecution to you.
In these cases, I might edit your introduction and that's it.
For students close to graduating and postdocs, I might only read a close-to-final draft to offer comments with no "hands-on-keyboard" work.
For postdocs, I might not even be a co-author.

If you are unclear what type of help you are going to get from me, **ask**!
I will be clear and up front to you and say things like, "I'll have all of Thursday morning to devote to your paper" or "I have too many other deadlines. I'll write your introduction but otherwise you are on your own."

## After My Input

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

After I've worked on your paper, you usually need to do what I call a "smoothing pass".
The amount of smoothing depends on how extensive my edits were and how much I changed.
For example, if I rewrote a paragraph here, you'll need to make sure that the flow from the preceding to the following paragraph remains smooth; you might need to add a transition sentence.
Sometimes I'm missing this because I focused on making local edits; you'll likely have a more accurate global view than I do.

Note that often my edits trigger the need for changes to propagate non-locally to other parts of the paper.
For example, if I tweak the story in the introduction, then we need to make sure the narrative in the rest of the paper is consistent.
As an another example, if I change a particular phrasing, then we need to make sure the phrasing is propagated everywhere else.
What is it that we're proposing?
A model? Technique? Approach? Method?
Whatever we decide (let's discuss), make it consistent.
That is, don't say in the intro "We propose an approach to..." and then later say, "Our method does this..."
See ["use consistent terminology"](https://github.com/lintool/guide/blob/master/writing-pet-peeves.md).

## As the Deadline Approaches

As the deadline approaches, the magnitude of changes should decrease, because the chances you'll make the paper worse increase.
You've been working hard, haven't been getting enough sleep, you're tired, stressed out, etc. and this makes it likely you'll make a mistake.
Say you've come up with a better way to tell your story, but it's two days before the deadline and it'll require major surgery on the paper (moving sections around, etc.).
_Resist that urge._
Chances are you'll leave out some major component accidentally (because you're not left with adequate time for proofreading) and end up making the narrative more confusing.

The truth is that, close to the deadline, you're often agonizing over details that make epsilon difference with respect to acceptance probability.
Do I add this sentence or take it out?
Do I use this phrase in the intro or not?
It likely doesn't matter: the effects of the decisions are far smaller than the variance due to reviewer assignment.
So, don't stress over it.
tl;dr &mdashl be careful not to make things worse.

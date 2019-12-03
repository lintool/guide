# Leaderboard Micropublications: A Proposal

Initial post: December 2, 2019

Our field (more narrowly, *ACL, and more broadly, human language technologies) has been blessed with explosive popularity and tremendous amounts of attention from students, industry, and even the media.
This is undoubtedly an exciting area to be working in!

However, the downside is that our existing models of knowledge dissemination (i.e., publications) are on the verge of collapse, both from sheer volume, different styles of research, and different norms for sharing results.
Although there is no agreement on how to address our woes, there is little doubt that the status quo is unsustainable.
As they say, something's gotta give.

I'd like to propose a constructive, concrete suggestion that might help address the deluge: leaderboard micropublications.

## Huh?

In short, a leaderboard micropublication is a short paper that is tied to a particular entry on a leaderboard.
Recognizing that there are many different possible types of micropublications, which is already an established genre [[1](#footnote1)], for rhetorical convenience (but at the risk of some confusion) I'll simply use the term micropublication in this post.
By virtue of a tight coupling with a leaderboard, a micropublication can be very short and information dense, making it easy to write and to evaluate.
Much of the prose in a traditional research paper that goes into establishing context is no longer necessary, since the shared context is captured in the leaderboard itself.
A micropublication has methods, results, and discussion, and that's pretty much it.

For concreteness, I offer an example micropublication co-authored with Rodrigo Nogueira for the [MS MARCO passage retrieval task](http://www.msmarco.org/leaders.aspx) describing our [docTTTTTquery technique](https://cs.uwaterloo.ca/~jimmylin/publications/Nogueira_Lin_2019_docTTTTTquery.pdf).
Consider this as a starting point to begin the conversation.

How can a micropublication be so short and yet have something to offer?

A micropublication doesn't need an introduction.
It doesn't need to define the task.
It doesn't need to motivate the task.
Whether the task is interesting, meaningful, well-designed, etc. lies outside the scope of the micropublication itself.
In nearly all cases, the developers of the leaderboard already have a separate paper describing the motivation of the task, the construction of the dataset, the choice of evaluation metrics, etc.
There is no need to repeat those arguments.

A micropublication doesn't need an explicit related work section.
It only needs to reference the previous work it directly depends on.
It doesn't need a long list of references for signalling purposes.
The "background" related work?
Well, that's all the other entries and their corresponding micropublications on the leaderboard!

A micropublication doesn't need a future work section or a conclusion.
Future work?
Get a higher position on the leaderboard!
Wait until the next micropublication!

A micropublication only needs to focus on the methods, contrastive results, and discussion.
Furthermore, the methods can exclusively focus on things like model design, training regime, etc.
Other aspects of the evaluation design, like description of the dataset, evaluation metrics, etc.?
Well, that's already defined in the leaderboard!
While the "main result" of the micropublication is captured in the leaderboard entry itself, authors can (and should) discuss contrastive conditions, ablation experiments, and the associated analyses that contextualize a proposed approach.

## How can this help?

How can micropublications improve the dissemination of knowledge?

**Easier to write, easier to evaluate.**
Many papers submitted to the standard venues today _are_ already micropublications, just wrapped in lots of "fluff".
Let's just dispense with all the fluff.
Explicitly acknowledging this type of contribution will make such papers easier to write and easier to evaluate.

Easier to write?
Authors won't need to justify the task, pay homage to the influential (but only marginally related) papers, or engage in any other signalling that's often necessary to get a paper accepted.
The authors can dive directly into exactly what they did.

Easier to evaluate?
For a micropublication, there is a ready pool of qualified reviewers... the organizers as well as the other participants on the leaderboard!
They are well qualified because they have likely thought about the problem deeply already, and would be well-equipped to recognize innovative ideas.
Furthermore, reviewers don't need to do an in-depth literature search to verify the SOTA claims of the authors &mdash; the results are right on the leaderboard!

Thus, micropublications can improve the overall publication ecosystem by increasing the efficiency with which the community evaluates a subset of its research output.

**Micropublications are compatible with blind review.**
So long as the leaderboard accepts anonymous submissions (in the case of MS MARCO, they do), it would be possible to couple the leaderboard with a system like OpenReview to support blind review.

**Micropublications are compatible with researchers who rapidly iterate via preprints.**
I think this is self-evident and needs no elaboration.

**Recognizing a different category of contribution.**
To be clear, I am not suggesting that micropublications receive any sort of preferential treatment.
And I'm definitely not suggesting that micropublications replace any existing publication types; researchers can continue writing the same types of papers that exist today.
All I'm suggesting is that micropublications be recognized as a (new) distinct category of contribution.
We already have full papers, short papers, demo papers (and other categories, depending on the conference).
Let's add micropublications as another.

## Potential Objections and Unresolved Issues

The purpose of this post is to begin a conversation.
I don't have all the answers, and right off the bat I can anticipate a number of questions and potential objections.
I'll try to address some of them.

**Is it meaningful?**
I use this as a catch-all for a host of related questions:
Is the task captured by the leaderboard meaningful?
Are there data artifacts or biases in the data?
Do the metrics reflect human preferences?
Are we overfitting?
Yes, these are all very important questions, but they are orthogonal to my micropublication proposal.
A traditional paper needs to contend with all these issues also, so a micropublication does not make things worse.

In fact, I would argue that a micropublication puts everyone on more equal footing, since the reviewers are forced to evaluate only what's in front of them.
Imagine a scenario where two papers, _A_ and _B_ present comparable, SOTA-achieving results on some leaderboard task.
By bad luck, paper _A_ has a reviewer who questions the very premise of the task, while no reviewers of paper _B_ do.
Assume that, roughly, everything else about the quality of the two papers is equal.
Because the two papers are not handled by the same area chair, there is no "normalization", and thus paper _B_ is accepted while paper _A_ is rejected.
At least to me, the papers were not treated equitably since they were subjected to different reviewing standards.
With micropublications, this would not happen.
A reviewer can't question the premise of the task in a micropublication; it's simply outside the scope of evaluation.

But yes, we should absolutely discuss all the questions raised above.
However, those questions are orthogonal to doing well on the task _as defined_.
In fact, the burden of answering those questions should be placed on the leaderboard organizers, and likely those arguments are better made via traditional publication types.
The leaderboard organizers, with a behind-the-scenes view, are far better equipped to determine, for example, if new entries just overfitting.
(And if the answer is yes, the leaderboard should be shut down.)

My feeling is that since there are so many leaderboards out there today competing for our attention, they are themselves under the selective pressure of being interesting, relevant, meaningful, etc.
Thus, it might make sense to let everyone "vote with their feet"; researchers will, over time, gravitate towards tasks that interesting, fun, challenging, easy to make progress in, etc.
But on the flip side, leaderboard popularity is likely to suffer from a [Matthew effect](https://en.wikipedia.org/wiki/Matthew_effect).
Furthermore, tasks and datasets proposed by a few organizations automatically gain more cachet than others.

However, this proposal is not designed to critique or change the current research culture around leaderboard chasing.
The problem I'm trying to address is: given this style of research, can we at least more efficiently evaluate the outputs?

**How should micropublications be evaluated?**
This leads to the next important point: micropublications need to be evaluated differently.
In fact, building on the "easier to evaluate" theme raised above, the typical *ACL evaluation form could be dramatically simplified.
Gone are all the questions about scope (does this work belong in *ACL?).
Gone are all the questions about meaningful comparisons and related work: check the leaderboard!
The question about "soundness/correctness" should be rolled up with the standard *ACL question about originality.
In fact, stripping away all these unnecessary elements allows the reviewer to focus on what I propose to be the most important criterion: originality.
To wit, I've taken the standard wording and rephrased it in this context:

+ 5 = Innovative: Highly original and significant new technique, approach, or insight.
+ 4 = Creative: An intriguing technique or approach that is substantially different from previous entries.
+ 3 = Respectable: A nice research contribution that represents a notable extension of previous entries.
+ 2 = Uninspiring: Obvious, or a minor improvement on previous entries.
+ 1 = Significant portions have actually been done in previous entries.

This focus, for example, would allow us to accept papers that don't achieve SOTA, but demonstrate some remarkable insight, and reject papers that achieve SOTA, but in an uninteresting way.
At a high level, I think this is what we'd want?
The [docTTTTTquery example](https://cs.uwaterloo.ca/~jimmylin/publications/Nogueira_Lin_2019_docTTTTTquery.pdf), trying to be as objective as possible, I would rate between a "2" and a "3".
While using T5 for document expansion is perhaps an obvious extension of the original doc2query model, it's more than a "minor improvement" since we report a 6 point gain.

Once again, the proposal here simply aims to begin the conversation.
I'm not totally committed to this rubric, but the broader point remains: we need different evaluation criteria for micropublications.

**How do I demonstrate that an approach is general?**
Reviewers like to see a technique applied to multiple tasks to demonstrate its generality.
I see no problem with this.
A micropublication can certainly contain results for multiple leaderboards, although with the increased length we might have to call these millipublications.

**What if the increased efficiency of evaluating micropublications is offset by more micropublications to evaluate?**
This is an interesting point.
My rebuttal is that all micropublications must be associated with actual leaderboard submissions, so if the number of submissions increases, it means that micropublications have enabled the community to iterate and share findings faster?
I'd consider this a net win.

**The overall benefit to the broader publication ecosystem is dependent on the number of research outputs that can be evaluated as micropublications.**
Agreed.
But based on the frequent complaints I hear about leaderboard chasing on social media, the savings seem like they would be substantial?

**Formal recognition and "worth".**
Students still need to get jobs, faculty still need to be promoted.
None of this harebrained scheme is going to work until micropublications are valued by the powers that be (hiring committees, tenure and promotion committees, letter writers, etc.).
Of course.
This is a problem faced by any new attempt to do something different.
There are the standard answers:
Let's try to convince an established reputable venue to "take on" micropublications as a track or new category of contribution.
Let's try to create a new journal devoted to micropublications.
Over time, "the market" will converge on the value or "worth" of micropublications, relative to, say, full and short papers.

However, that's putting the cart before the horse.
Nothing will happen until at least enough people think this is a good idea.
What do you think?

## Footnotes

[<a name="footnote1">1</a>] For example, there is a journal actually called [microPublication Biology](https://www.micropublication.org/); in computer science, Dittrich proposed the concept of [PaperBricks](https://arxiv.org/abs/1102.3523) in 2011.

## Acknowledgments

I want to thank the following people for feedback on various drafts of this post: Ashutosh Adhikari, Martin Gauch, Yoav Goldberg, Rodrigo Nogueira.
Feedback, however, does not imply endorsement.

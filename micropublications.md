# Leaderboard Micropublications: A Proposal

Our field (more narrowly, *ACL, and more broadly, human language technologies) has been blessed with explosive popularity and tremendous amounts of attention from students, industry, and even the media (a mixed blessing).
This is undoubtedly an exciting area to be working in!
However, the downside is that our existing models of knowledge dissemination (i.e., publications) are on the verge of collapse, both from sheer volume, different styles of research, and different norms for sharing results.
There doesn't seem to be a single silver bullet that will fix all our woes, but there is no one I've talked to who believes that the status quo is sustainable.
As they say, something's gotta give.

I'd like to propose a constructive, concrete suggestion that might help address the deluge: leaderboard micropublications.

## Huh? Micropublications

In short, a leaderboard micropublication is a short paper that is tied to a particular entry on a leaderboard.
Recognizing that there are many different possible types of micropublications, which is already an established genre [1], for rhetorical convenience (but at the risk of some confusion) I'll simply use the term micropublication in this post.
By virtue of a tight coupling with a leaderboard, a micropublication can be very short and information dense, make it easy to write and evaluate.
Much of the prose in a traditional research paper that goes into establishing context is no longer necessary, since the shared context is captured in the leaderboard itself.
A micropublication has methods, results, and discussion, and that's pretty much it.

For concreteness, I offer two examples of micropublications that I have recently co-authored with Rodrigo Nogueira, one for the [MS MARCO keyphrase extraction task]() and one for the [MS MARCO passage retrieval task]().
Consider these as starting points of what a micropublication might look like, to begin the conversation.

How can a micropublication be so short and yet have something to offer?

A micropublication doesn't need an introduction.
It doesn't need to define the task.
It doesn't need to motivate the task.
Whether the task is interesting, meaningful, well-designed, etc. lies outside the scope of the micropublication itself.
In nearly all cases, the developers of the leaderboard already have a separate paper describing the motivation of the task, the construction of the dataset, the choice of evaluation metric, etc.
There no need to repeat these arguments.

A micropublication doesn't need an explicit related work section.
It only needs to reference the previous work it directly depends on.
It doesn't need a long list of references for signalling purposes.
The "background" related work?
Well, that's all the other entries and their corresponding micropublications on the leaderboard!

A micropublication doesn't need a future work section or a conclusion.
Future work?
Wait until the next micropublication!

A mircopublication only needs to focus on the methods, contrastive results, and discussion.
Furthermore, the methods can exclusively focus on things like model design, training regime, etc.
Other aspects of the evaluation design, like description of the dataset, evaluation metrics, etc.?
Well, that's already defined in the leaderboard!
While the "main result" of the micropublication is captured in the leaderboard entry itself, authors can (and should) discuss contrastive conditions, ablation experiments, and the associated discussions that contextualize a proposed approach.

## How can this help?

How can micropublications improve the dissemination of knowledge?

**Easier to write, easier to evaluate.**
Many papers submitted to our typical venues _are_ already micropublications, just wrapped in lots of "fluff".
Let's just dispense of all this fluff.
Explicitly acknowledging this "genre" will make such papers easier to write and easier to evaluate.

Easier to write?
Authors won't need to justify the task, pay homage to the influential (but only marginally related) papers in the area, or engage in any other signalling that's often necessary to get a paper accepted.
The authors can dive right into exactly what they did.

Easier to evaluate?
For a micropublication, there is a ready pool of qualified reviewers... the organizers as well as the other participants on the leaderboard!
They are well qualified because they have likely thought about the problem deeply already, and would be well-equipped to recognize innovative ideas.
Furthermore, reviewers don't need to do an in-depth literature search to verify the SOTA claims of the authors---the results are right on the leaderboard!

Thus, micropublications can improve the overall publication ecosystem by increasing the efficiency with which the community evaluates a subset of its research output.

**Micropublications are compatible with blind review.**
So long as the leaderboard accepts anonymous submissions (in the case of MS MARCO, they do), it would be possible to couple the leaderboard with a system like OpenReview to support blind review.

**Micropublications are compatible with researchers who rapidly iterate via preprints.**
I think this is self-evident and needs no elaboration.

## Potential Objections and Unresolved Issues

The purpose of this blog post is to begin a conversation.
I don't have all the answers, and right off the bat I can anticipate a number of questions and potential objections.
I'll try to address some of them.

**Is it meaningful?**
I use this as a catch-all for a host of related questions:
Is the task captured by the leaderboard meaningful?
Are there data artifacts or biases in the data?
Do the metrics reflect human preferences?
Are we overfitting?
Yes, I argue these are all very important questions, but they are orthogonal to the micropublication proposal.
A traditional publication needs to contend with all these issues also, so a micropublication does not make things worse.

In fact, I would argue that a micropublication puts everyone on a more equal footing, since the reviewers are forced to evaluate only what's in front of them.
Imagine a scenario where two papers, _A_ and _B_ present comparable, SOTA-achieving results on some leaderboard task.
By bad luck, paper _A_ has a reviewer that questions the very premise of the task, while no reviewers of paper _B_ do.
Assume that, roughly, everything else is equal.
Because the two papers are not handled by the same area chair, there is no "normalization", and thus paper _B_ is accepted while paper _A_ is rejected.
I would argue that the papers are were not treated equitably since they were subjected to different reviewing standards.
With micropublications, this would not happen.
You can't question the premise of the task in a micropublication; it's simply outside the scope of evaluation.

Yes, we should absolutely discuss all the questions raised above.
But those questions are orthogonal to doing well on the task _as defined_.
In fact, the burden of answering those questions should be placed on the leaderboard organizers.
And the leaderboard organizers, with a behind-the-scenes view, are far better equipped to answer the question:
"Are new entries just overfitting?"
(And if the answer is yes, the leaderboard should be shut down.)

**How should micropublications be evaluated?**
This leads to the next important point: micropublications need to be evaluated differently.
In fact, building on the "easier to evaluate" theme raised above, the typical *ACL evaluation form could be dramatically simplified.
Gone are all the questions about scope (does this work belong in *ACL?).
Gone are all the questions about meaningful comparisons and related work: check the leaderboard!
The question about "soundness/correctness" should be rolled up with the standard *ACL question about originality.
In fact, stripping away all these unnecessary elements allows the reviewer to focus on what I think is the most important criterion: originality.
To wit, I've taken the standard wording and rephrased it in this context:

+ 5 = Innovative: Highly original and significant new technique, approach, or insight.
+ 4 = Creative: An intriguing technique or approach that is substantially different from previous entries.
+ 3 = Respectable: A nice research contribution that represents a notable extension of previous entries.
+ 2 = Uninspiring: Obvious, or a minor improvement on previous entries.
+ 1 = Significant portions have actually been done in previous entries.

This focus, for example, would allow us to accept papers that don't achieve SOTA, but demonstrate some remarkable insight, and reject papers that achieve SOTA, but in an uninteresting way (for example, more effort spent tuning hyperparameters).

**How do I demonstrate that an approach is general?**
Reviewers like to see a technique applied to multiple tasks to demonstrate its generality.
I see no problem with this.
A micropublication can certainly contain results for multiple leaderboards, although with the increased length we might have to call these millipublications.

**What if the increased efficiency of evaluating micropublications is offset by more micropublications to evaluate?**
This is an interesting point.
My rebuttal is that all micropublications need to be associated with an actual leaderboard submission, so if the number of submission increases, it means that micropublications have enabled the community to iterate and share findings faster?
I'd consider that a net win.

**The overall benefit to the broader publication ecosystem is dependent on the number of research outputs that can be evaluated as micropublications.**
Agreed.
But based on the frequent complaints I hear about leaderboard chasing on social media, the savings seem like they would be substantial?

**Formal recognition.**
Students still need to get jobs, faculty still need to be promoted.
None of this harebrained scheme is going to work until micropublications are valued by the powers that be.
Of course.
This is a problem faced by any new attempt to do something different.
There are the standard answers:
Let's try to convince an established reputable venue to "take on" micropublications as a track or new category of contribution.
Let's found a new journal devoted to micropublications.

However, that's putting the cart before the horse.
Nothing will happen until at least enough people think this is a good idea.
What do you think?

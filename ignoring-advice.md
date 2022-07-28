# Should You Follow My Advice?

I often say to my students, "I am your advisor, not your boss."
As an advisor, I dispense advice, explaining the consequences of specific actions (both positive and negative), but I rarely tell you what to do.
I explain to you what the design space looks like, or, alternatively, what the loss landscape is.
It's up to you to decide on your course of action.
Ultimately, it's _your_ research and _your_ degree.

However, this doesn't mean that all my advice is equal in terms of "assertiveness" or "firmness" &mdash; the degree to which you should follow my guidance.
At one end of the spectrum, some advice I offer is quite close to a directive, i.e., "please do it".
At the other end of the spectrum, some advice I offer comprises merely suggestions, i.e., "feel free to ignore me".
Given subtle nuances in communication, particularly for non-native English speakers [1], I've decided to explicitly elaborate on communicative intent here.

Think of this as a way to translate between "what I say" and "what I really mean".
Of course, this guide is idiosyncratic with respect to the particular way I communicate, but in general, for many advisors, the "surface form" of an utterance often diverges from its underlying intent.

## "Advice" That Really Means "Please Do It!"

To begin, there _are_ cases where what I say should be interpreted as directives, even though it sounds like advice.
These generally fall into two categories:
The first is externally imposed rules, which if ignored, leads to negative consequences.
For example,

+ "You should get that form signed"... otherwise you can't graduate.
+ "You shouldn't go over the page limit specified in the call for papers"... otherwise your paper will be desk rejected.

Thus, even though these statements are phrased in the [subjunctive](https://en.wikipedia.org/wiki/Subjunctive_mood) ("should"), understand these directives as "please do it".

The other main category comprises commitments we (as a group) made.
For example,

+ A deliverable in the context of a proposal.
+ A feature in a piece of software for a downstream user.
+ A particular model variant for a collaborator.

Not honoring these commitments has negative consequences (e.g., unhappy collaborators).
In these contexts, statements I make should be interpreted as _requests_, i.e., you should do it.
And if you can't, let's discuss further and figure something out (for example, prioritize between competing responsibilities).
Please don't just ignore me.

## Advice That Really Is Advice

With the "please do it" stuff out of the way, everything else below _really_ is advice, but to various degrees of assertiveness.
Yes, in many cases, it _is_ okay to ignore me.

I'll sketch out common things I say, in decreasing order of assertiveness:

**"It's a bad idea to..."** or **"You shouldn't..."** or **"Don't..."**
When I phrase advice negatively, it should be understood as "don't do it unless you have a very good reason otherwise".
There are (likely) negative consequences (in my experience) to a course of action.
For example:

+ "You shouldn't introduce _X_ here in Section 3 because you don't define _X_ until Section 4."
Likely negative consequence: your reader is not going to understand your paper.
+ "You shouldn't talk for more than _Y_ minutes."
Likely negative consequence: your audience is going to get annoyed.

Advice along these lines isn't a "100% rule", but if you're going to ignore me, you'd better have good reasons [2].

**"It's a good idea to..."** or **"You should..."**
When I phrase advice positively, it usually means that I am telling you about best practices, norms, or preferred solutions.
For example:

+ "It's a good idea to have an explicit statement of contributions in your introduction." (Many reviewers except such a statement, perhaps elevating it to a norm.)
+ "You should add some ablation conditions here." (Running ablations falls under "experimental best practices".)

Advice along these lines should be interpreted as less assertive than the "it's a bad idea" variants above.
There are plenty of violations of best practices [3], but just remember that best practices exist for a reason, and if you wish to violate them, be deliberate in terms of what you hope to accomplish.

**"You might want to..."** or **"You should think about..."** or **"Have you considered..."**
Take these as suggestions.
For example:

+ "You might want to move that figure here."
+ "You should think about adding this feature to your model." [4]

Often, these comments are made in the context of a discussion where I may not have "thought things through" (completely).
In these cases, give my suggestions some thought, and if they don't make sense, feel free to ignore them.
However, if I bring up the same issue again (at a later point in time), it would be nice for you to demonstrate that you've at least considered my feedback, e.g., "Yes, I thought about moving that figure here, but that doesn't make sense because..."

**"... your call"** or **"... I don't feel strongly either way"** or **"I'm agnostic..."**
This happens often after a discussion wherein multiple options are considered, all of which represent reasonable choices or actions.
For example:

+ "You could phrase it like this... or like that... your call."
+ "You could structure your results section this way... or that way... I don't feel strongly either way."

It really means... up to you...

I strive to communicate clearly and directly, but the bottom line is: If you don't understand the level of assertiveness in the advice I'm offering, **ASK ME TO CLARIFY**!

## Footnotes

[1] I once said to a student (non-native English speaker) "[do this at your peril](https://www.ldoceonline.com/dictionary/do-something-at-your-peril)" and the student didn't understand what I meant.

[2] Yes, there indeed cases (but relatively rare) where a student ignore my advice in the category, but ended up with a better outcome than would have occurred if my advice had been followed.

[3] In fact, violation of best practices is one approach to progress. Learning to rank using tree-based models constituted best practices before the "neural age". Of course, they've since been supplanted (or at the least, augmented) by neural networks.

[4] Note the subtle difference between "you should..." and "you should think about/consider..."

# Be Paranoid! (Someone is working on your idea right now!)

Initial post: November 15, 2019

First off: of course I don't mean it in a pathological [DSM](https://www.psychiatry.org/psychiatrists/practice/dsm) sense.
So seriously, save your judgmental "oh it must be terrible to be your student" derision and go back under the bridge whence you came.
Of course when I say it to my students it is couched within a broader context, and they understand that context.
_You don't_, because you read my slogan in a tweet.
I mean what I say in the "only the paranoid survive" Andy Grove sense and the "customer obsession" Jeff Bezos sense.

With that aside, back to the slogan.
First, let me illustrate, (pseudo-)mathematically, why this statement is likely to be true when uttered to a broad audience.
Hinton estimates that [there are around 10k graduates students in China "doing neural nets"](https://youtu.be/Mqt8fs6ZbHk?t=124).
Assume that's a reasonable estimate.
That's just in China.
So the entire worldwide population of "people doing neural nets" is likely a multiplicative factor of that.
Let's then consider the [pigeonhole principle](https://en.wikipedia.org/wiki/Pigeonhole_principle): How many distinct novel "ideas" do you think there are on the frontier of deep learning?
Are there 10k?
If there are less (which I believe), then a collision is inevitable.
Even if there are more than 10k (even way more), there is a [birthday paradox](https://en.wikipedia.org/wiki/Birthday_problem) effect when referring to an audience.
Of course ideas aren't discrete and countable, and of course the distributions of ideas and effort aren't uniform.
This isn't meant to be a formal proof, just a [prima facie](https://en.wikipedia.org/wiki/Prima_facie) argument about the veracity of the claim.

Now let's consider the objections.

Okay, your solution is simple.
Don't work on deep learning.
Knuth [says this](https://twitter.com/lintool/status/1057722875942068225).
Yes, if you're Knuth you can work on anything you want.
If you don't want to work on deep learning, that's of course completely fine.
However, consider this: often, the reason why a particular approach is popular is usually _because it works_.
Today, we if encounter someone who refuses to adopt data-driven techniques and stubbornly insists on _only_ writing rules, we'd think that's kinda silly.
It is likely that in a few years, a categorical resistance to deep learning would seem just as silly.

I'll provide a bit of historical context: the previous major paradigm shift in NLP was from rule-based to "statistical" approaches in the 1990s [[1](#footnote1)].
Yes, there were researchers back then who simply refused to count tokens and compute likelihoods.
I know because I lived through those years (as a student).
Today, most people would find that laughable.

Oh, there's also a practical matter: You'll struggle getting your *ACL papers accepted.

Next, the old, trite, uninspired retort: "well, if you're in danger of being scooped, you should work on a more interesting problem."
I argue the exact opposite: many people are working on a problem _precisely_ because it's interesting.
Or useful, impactful, etc.
It is this reason why DL/NLP/etc. has advanced so quickly: because people quickly pick the low hanging fruit (tasty!), rush to ask all the obvious questions, quickly determine the answers, and then tell everyone else about it (what you call flag planting derisively I call rapid dissemination of knowledge).
In this way, the research frontier expands rapidly, to everyone's benefit.
It feels absolutely exhilarating to be _on_ this frontier, to be working on something that boatloads of people care about.
It feels absolutely intoxicating to sit atop a leaderboard, knowing that you and your colleagues, _at that moment_ are the best in the world that this very thing.

But the downside is that you might get scooped.
Hence the slogan.

You're not in danger of getting scooped?
That doesn't mean you're working on an interesting problem.
It may just mean that you're working on a problem no one cares about.

Many of the remaining retorts I've heard could be characterize as _hubris_ (defined by [Merriam-Webster](https://www.merriam-webster.com/dictionary/hubris) as "exaggerated pride or self-confidence").

"I work on something that I'm uniquely suited for...", "... that only I can do", "... that plays to my strengths", or something along those lines.
Oh really?
You must have a high opinion of yourself.
You may truly be unique, or it's just _hubris_.
As Bill Gates famously said, [in China when you are one in a million, there are thirteen hundred people just like you](https://books.google.com/books?id=CfHCBUepsXIC&pg=PA353&lpg=PA353&dq=%22one+in+a+million%22).

"I like to take my time to think", "... look further ahead", "... work on really difficult problems", or something along those lines.
Oh really?
The rest of us are just running around like headless chickens, and our work is no more principled than [Brownian motion](https://en.wikipedia.org/wiki/Brownian_motion)?
You can think two steps ahead of everyone else without rolling up your sleeves and actually working on step one?
Wow, that's amazing.
Perhaps you're just so insightful that you see something all of us have missed.
It may be true, or it's just _hubris_.

Thomas Kuhn talks about paradigm shifts followed by ["normal science"](https://en.wikipedia.org/wiki/Normal_science).
Clayton Christensen talks about [sustaining innovating vs. disruptive innovative](https://en.wikipedia.org/wiki/The_Innovator%27s_Dilemma).
If you think you can bring about a paradigm shift and disrupt the status quo, then, sure, you're less likely to be scooped.
I truly look forward to being enlightened by your brilliance when you change the world.
Maybe it'll happen, or it's just _hubris_.

While you are thinking "your deep thoughts", I'll be here, grinding away, [poking tiny new frontiers in knowledge, bit by bit](http://matt.might.net/articles/phd-school-in-pictures/).
Perhaps it is through this process that I will stumble upon upon some brilliant, revolutionary idea.

_Nah_, that's just _hubris_.

I end this essay noting, with great relish, that even Albert Einstein [was nearly scooped](https://en.wikipedia.org/wiki/Relativity_priority_dispute).

## Footnotes

[<a name="footnote1">1</a>] I put "statistical" in quotes because that was the term of art back then, but "statistical" is better characterized as "data-driven" in today's parlance.

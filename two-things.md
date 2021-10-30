# Two Things That Every Graduate Students Needs

## A Research Notebook

> Most scientists keep a research notebook. You should too. You've probably been told this in every science class since fifth grade, but it's true. Different systems work for different people; experiment.
> [[Chapman, 1988](https://dspace.mit.edu/bitstream/handle/1721.1/41487/AI_WP_316.pdf#page=13)]

### What is it?

### How do I do it?

What I do:
I keep my research notebook in a private GitHub.
The README.md contains entries in reverse chronological order (latest entries on top).

At the very top of the notebook, I create a cheat sheet for myself containing all those mysterious command-line invocations that are necessary for setting up my environment.
For example, those crytic conda commands I can never remember.

So, I open up README.md in emacs, copy and paste into the shell, and I'm ready to go.
As I'm working, I'm constantly copying things back and forth from my notebook into the shell and vice versa.
I rarely type a complex command (e.g., with many parameters) directly into the shell: typically, I compose the command in emacs, _then_ copy into the shell.
I do this because I'm usually running the same command over and over again with slight variations, e.g., different input files, different output locations, different parameters, etc.
Modifying a long and complex command in emacs is far easier than trying to do it in the shell... and plus, I want to record my commands anyway, so starting in emacs is just easier.
I copy the output of commands (e.g., execution trace, evaluation results, etc.) back into emacs.

Usually, I'm concurrently writing new code, so I'm tabbing back and forth between emacs and my IDE (and Slack, and Teams, and email, and my calendar, and all the other things that are constantly calling for my attention).
If I encounter a bug (e.g., some exception is thrown) or some really weird result (e.g., MAP of 0.003? There's got to be _something_ obviously wrong), I record the error trace also.
This is important because if (or rather, _when_) I get interrupted, this helps me remember what I was doing, i.e., "oh, I remember, I was in the middle of debugging this exception".
These intermediate traces get cleaned up later (see below).

At the end of a "working session", which might be a few hours later (if I'm lucky enough to have been working continuously) or might be a few days later (when I get interrupted... which happens _a lot_), I go back and clean up the entry.

By "cleaning up", I reorganize the entry into something that's actually readable, instead of a random jumble of commands and shell output.
For example, I remove all the intermediate error traces and debug output since by now the bug should have been fixed.
I add some prose around that describes what I was doing.

The final result is a sample entry that looks this this:

<img width="571" alt="notebook-sample" src="https://user-images.githubusercontent.com/313837/139533737-fe32a3ac-e642-4135-9208-e84809035b5b.png">

Associated files (detailed results that are too verbose to report in the main entry, config files, etc.) are stored in directories by date, e.g., `YYYY-MM-DD`.

Other possible systems:

+ Google Docs
+ [Notion](https://notion.so/)
+ Microsoft OneNote

## A Literature "Database"

You'll be reading a lot of papers.
You'll need some system to keep track of them.

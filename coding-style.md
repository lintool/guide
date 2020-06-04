# Coding Style

These are general coding style guidelines we've adopted for my research group.

**Background on UNIX command-line options:**
Many (most?) UNIX style command-line options have "long form" and a "short form", where the latter is a single character.
For example `-a` and `--all` for `ls` (although, interestingly, `-l` doesn't have a long form).

Short form options can be strung together, e.g., `ls -l -a` becomes `ls -la`.
Thus `--abc` and `-abc` mean very different things; the first represents a single option, the second is a shorthand for multiple options, e.g., `-a -b -c`.

For more details, see [GNU Program Argument Syntax Conventions](https://www.gnu.org/software/libc/manual/html_node/Argument-Syntax.html).

## General

+ We use a maximum line length of 120 character.
The rationale for this limit is that 120 is (approximately) the number of characters that will render in GitHub without horizontal scrolling.
This maximizes use of screen real estate.

### Describing Arguments in Command-Line Applications

+ The description should be a short phrase that begins with a capital letter an ends with a period. It prescribes the function or method's effect as a command ("Do this", "Return that"), not as a description; e.g. don't write "Returns the pathname...". This overarching guideline is adapted from [PEP 257: Docstring Conventions](https://www.python.org/dev/peps/pep-0257/).
+ The description should be as succinct as possible, typically a noun phrase. For example, for `-index`, "Path to input collection." is preferred to "Set the path to the input collection.".
+ Omit articles, e.g., "Number of Hits." is preferred over "The number of hits."
+ Boolean flags should be written as verb phrases, and there is generally no need to indicate that it's a flag in the description. For example, for `-storeRaw`, "Store raw source documents." is preferred to "Flag to determine whether raw source documents are stored." or "Whether or not to store raw documents.".
+ Prefer prepositional phrases over possessives for clarity, e.g., "Foo parameter of Bar." is preferred to "Bar's Foo parameter." even though the latter is shorter. This is especially the case if Bar has multiple tokens.

## Python

+ We adopt [PEP8](https://pep8.org/).
+ We adopt single quotes `'` for strings; unless another approach is obviously better, we use [f-strings](https://www.python.org/dev/peps/pep-0498/) for formatting.

### Docstrings

+ We adopt the [numpy docstring style](https://numpydoc.readthedocs.io/en/latest/format.html).
+ In general, follow guidelines in "Describing Arguments in Command-Line Applications".

### Command-Line Options

We try to stay true to the UNIX convention, which is what `argparse` (implicitly) endorses anyway.
This means that Java and Python counterparts of script that do the same thing will have different parameters.
Thus:

+ Options begin with two dashes: `--index` instead of `-index`.
+ Use single dash (instead of underscore) for multi-token options: `--max-value` instead of `-max_value`.
+ Use `.` to group parameters, e.g., `--bm25` (use BM25) and `--bm25.b` (set the BM25 _b_ parameter). This looks better than `--bm25-b`.

## Java

+ Two space indent, otherwise standard conventions.

### Command-Line Options

Java breaks the UNIX convention and is a total mess.
For example, `-classpath` and `--class-path` both work (although the first is much more common).
For command-line programs written in Java, we try to maintain consistency to Java options:

+ Options begin with a single dash: `-index` instead of `--index`.
+ Use camel case instead of snake case: `-maxValue` instead of `-max_value`.
+ Use `.` to group parameters, e.g., `-bm25` (use BM25) and `-bm25.b` (set the BM25 _b_ parameter).

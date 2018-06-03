---
layout: page
title: Turn scripts into reproducible reports
description: Brief discussion of the use of literate programming
             (using documents that mix text and chunks of code).
---

What we've discussed so far is sufficient for a project to be fully
reproducible:

- [Write a script for each step](scripts.html)
- [Organize the data and the scripts](organize.html)
- [Automate the process with GNU Make](automate.html)

But scripts will define _what_ you did and not necessarily _why_ you
did it. And it's better to include the motivation, such as the
different figures that you looked at. This is particularly important
for the data cleaning process; for example, _why_ did you omit those particular
samples?

My preference is to replace most of those scripts with _reproducible
reports_ (using [R Markdown](https://rmarkdown.rstudio.com) and
[knitr](https://yihui.name/knitr/), or
[Jupyter notebooks](https://jupyter.org/)). Such a report
is a mixture of code and text: the code that does the work and your
text that describes what you're doing and why you're doing it.

With either R Markdown/knitr or IPython notebooks, chunks of code will
be run and figures created, and a nicely formatted report will be
produced. Rather just running a script, you'll compile the report.
Compiling the report will do the work that the script would have done,
but will also produce a report that describes the what and the _why_,
with figures and tables that support your decisions.

To learn more about [knitr](https://yihui.name/knitr) and
[R Markdown](https://rmarkdown.rstudio.com), see my
[knitr in a knutshell tutorial](https://kbroman.org/knitr_knutshell).

To learn more about Jupyter notebooks, see the
[documentation](https://jupyter.org/documentation)
at [the Jupyter Project website](https://jupyter.org/index.html).

The construction of such reports is definitely more work than writing
a simple script, but the product may save you a lot of time and effort
down the road. For example, imagine that a reviewer (or coauthor)
asks, &ldquo;Why did you omit those samples?&rdquo; You won't be left
scratching your head; you'll have a document that explains why.

---

Now go to the page about [turning repeated code into functions](functions.html).

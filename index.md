---
layout: page
title: initial steps toward reproducible research
description: Suggestions of how to get started, in seeking to adopt a
             reproducible workflow for one's computational research.
---

A minimal standard for data analysis and other scientific computations is
that they be _reproducible_: that the code and data are assembled in a
way so that another group can re-create all of the results (e.g., the
figures in a paper). Adopting a workflow that will make your results
reproducible will ultimately make your life easier; if a problem (or
question) arises somewhere down the line, it will be much easier to
correct (or explain).

Organizing analyses so that they are reproducible is not easy. It
requires diligence and a considerable investment of time: to learn new
computational tools, and to organize and document analyses as you go.

But _partially reproducible_ is better than _not at all
reproducible_. Just try to make your next paper or project better organized
than the last.

There are many paths toward reproducible research, and you shouldn't
try to change all aspects of your current practices all at once. Identify
one weakness, adopt an improved approach, refine that a bit, and then
move on to the next thing.

Inspired by
[Christine Bahlai](https://practicaldatamanagement.wordpress.com)'s
&ldquo;[Baby steps for the open-curious](https://practicaldatamanagement.wordpress.com/2014/10/23/baby-steps-for-the-open-curious/),&rdquo;
I thought I'd write some suggestions for the initial steps to take
towards making one's work reproducible.

I'm focusing primarily on [R](https://www.r-project.org), because
that's what I know, but I'll try to at least sketch what a
[python](https://www.python.org) person might do.

Again, you shouldn't try to do these things all at once; start with one, or part of
one. Then in your next project, do that plus another thing.

- [Organize your data and code](pages/organize.html)
- [Everything with a script](pages/scripts.html)
- [Automate the process](pages/automate.html)
- [Turn scripts into reproducible reports](pages/reports.html)
- [Turn repeated code into functions](pages/functions.html)
- [Package functions for reuse](pages/packages.html)
- [Use version control](pages/version_control.html)
- [License your software](pages/licenses.html)

- [Other resources](pages/resources.html)

---


The source for this minimal tutorial is [on github](https://github.com/kbroman/steps2rr).
If you have suggestions for changes or improvements,
please [submit an issue](https://github.com/kbroman/steps2rr/issues).


Also see my [tutorials](https://kbroman.org/pages/tutorials) on
[git/github](https://kbroman.org/github_tutorial),
[GNU make](https://kbroman.org/minimal_make),
[knitr](https://kbroman.org/knitr_knutshell),
[R packages](https://kbroman.org/pkg_primer),
[data organization](https://kbroman.org/dataorg),
and [making a web site with GitHub Pages](https://kbroman.org/simple_site).

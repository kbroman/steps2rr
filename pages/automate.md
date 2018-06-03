---
layout: page
title: Automate the process
description: Brief discussion of the use of GNU Make for automation,
             as part of a reproducible research workflow.
---

You have the full process encoded in scripts, and the data and
code are nicely documented and organized. But there'll be a lot of
scripts. Your ReadMe file may explain how to run them, and in what
order, but it'll be a pain to do all of that. (And your ReadMe file
might be a tad out of date!)

Ideally, the reproduction of your results is a one-button
operation. And this is valuable not just for others, but also for
yourself (or your future self). For example, if the primary data
should change (and it often does), wouldn't it be nice to have one
command that re-runs everything?

You could do this with a single all-encompassing script. Even better,
though, is to use [GNU Make](https://www.gnu.org/software/make). I
would argue that Make is the single most important tool for
reproducible research.

[GNU Make](https://www.gnu.org/software/make) was written for compiling
programs from their source code, but it can be used to coordinate any
command-line driven process, such as the various scripts that underlie
a data analysis project, or the construction of the figures and tables
for a paper.

The beauty of Make is that it both automates a process and documents
the dependencies in the project: this file is turned into that file
with this line of code, and this graph is produced from those files
with that script.

You create a file, called `Makefile`, and then on the command line
type `make`. Here's part of
[an example](https://github.com/kbroman/Paper_Rqtl_Experiences/blob/master/Makefile)
(for
[this paper](https://openresearchsoftware.metajnl.com/article/view/jors.at/43)):

    rqtlexper.pdf: rqtlexper.tex rqtlexper.bib fig1.eps fig2.eps
        pdflatex rqtlexper
        bibtex rqtlexper
        pdflatex rqtlexper
        pdflatex rqtlexper

    rqtlexper.tex: rqtlexper.Rnw Data/lines_code_detail.txt
        R -e 'library(knitr);knit("rqtlexper.Rnw")'

    Data/lines_code_detail.txt: Data/lines_code_by_version.csv Python/countStuff.py
        Python/countStuff.py > Data/lines_code_detail.txt

    fig1.eps: R/lodcurve_fig1.R
        cd R;R CMD BATCH lodcurve_fig1.R

    fig2.eps: R/colors.R Data/lines_code_by_version.csv R/rqtl_lines_code.R
        cd R;R CMD BATCH rqtl_lines_code.R

    Data/lines_code_by_version.csv: Perl/grab_lines_code.pl Data/versions.txt
        cd Perl;grab_lines_code.pl

Each batch of lines is like this:

    targetfile: dependencies
        [code to make the target from the dependencies]

In the example, there are bits of code for reformatting some data
files, for creating the two figures for the paper, for converting a
`.Rnw` file (Latex with R code chunks) into a `.tex` file, and for
creating the final PDF for the paper.

An advantage of GNU Make is that it will just re-run the necessary
bits, based on what files have changed. So if I've edited the text of
the paper (in `rqtlexper.Rnw`) but haven't changed the figures at all,
the first two bits in the example will be re-run, but the figures
won't be reconstructed. If I just edit part of the bibliography (in
`rqtlexper.bib`), only `rqtlexper.pdf` will be reconstructed;
`rqtlexper.tex` won't be.

To learn more about GNU Make, see my
[minimal make tutorial](https://kbroman.org/minimal_make) and the
resources listed there. It's quirky but hugely valuable.

---

Now go to the page about [turning scripts into reproducible reports](reports.html).

---
layout: page
title: Everything with a script
---

The most basic aspect of reproducible research is that everything
you do (convert data files, clean data, analyse data) should be
accomplished via _code_. Pointing and clicking, and copy-paste, are
not reproducible.

- Ideally, **get the data in the most-raw form** possible. And get any/all
  data and metadata possible. And keep track of the _provenance_ of
  all data files. (You don't want to be asking, &ldquo;Where did these
  microarray annotations come from?&rdquo;)

- If you need to **download external data**, such as from the web, it's
  best to do so via a script, for example with
  [wget](http://www.gnu.org/software/wget/). If that's not feasible,
  at least document the source of the data (and perhaps the date/time
  it was acquired).

- If you need to **convert a data file** from one form to another, use a
  script. For example, to convert an Excel file to a CSV file, I use
  [xls2csv.py](https://pypi.python.org/pypi/xls2csv) or
  [xlsx2csv.py](https://github.com/dilshod/xlsx2csv). Rather than
  opening the file in excel and saving each sheet by hand, do this
  with code.

- **Don't hand-edit data files**. If you need to delete some initial rows,
  or if you want to change some column names, don't open up the file
  and edit it by hand. Write a script that does so. I like to write
  [ruby](https://www.ruby-lang.org) scripts for this sort of thing;
  you might use [python](http://www.python.org) or
  [perl](https://www.perl.org), or even
  [R](http://www.r-project.org).

- All aspects of **data cleaning should be in scripts**. If you decide
  that you need to omit a couple of subjects, don't go into the data
  file and delete those rows, but rather write a script that will
  delete those subjects and create a separate, revised data file. If
  you find some errors in the data, don't go into the file and change
  it by hand, but rather make those changes via a script (or have the
  changes made to the primary database, in a documented and versioned
  way).

- Each aspect of the **analysis should be in scripts**. Make these
  straight-forward to run. It shouldn't be &ldquo;run this set of lines
  to do this and those lines to do that,&rdquo; or even worse,
  &ldquo;change this variable and then re-run it to do that.&rdquo;
  (I've written _lots_ of scripts like that in the past; they're
  neither pretty nor reproducible.) Ideally, break things up into
  functions, to make the code easier to follow and to avoid repeated
  code. [More on this later](functions.html).

Initially, it may seem like a hassle to do many of these things via
code rather than by hand. But if the primary data should change (and
it often does), repeating all of that by-hand extraction and editing
is a huge hassle, while re-running the scripts should be super easy
(particularly if automated, [more on that later](automate.html)).


---

Now go to the page about [organizing your data and code](organize.html).

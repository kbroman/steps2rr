---
layout: page
title: Turn repeated code into functions
description: A key step towards making your code understandable (and
             reusable) is to make it modular, including breaking
             things up into functions.
---

Scripts for data cleaning or analysis (or that produce graphs) often
include long stretches of code that are hard to read and
understand. For example, consider
[this one](https://github.com/kbroman/Paper_Rqtl_Experiences/blob/master/R/lodcurve_fig1.R)
and
[this one](https://github.com/kbroman/Paper_Rqtl_Experiences/blob/master/R/rqtl_lines_code.R),
which produce the two figures for
[this paper](https://openresearchsoftware.metajnl.com/article/view/jors.at/43).
(Those scripts could use some comments, couldn't they?)

Scripts often contain long stretches of repeated code, too. You do
the same thing a number of times, by copy-paste-edit.

It's better to break things up into functions.

- Pull out the bits of largely repeated code as a more-general
  function, and replace the repeated bits with simpler function calls.

- Pull out long stretches of complicated code as a separate function
  (or, ideally, multiple simple functions).

I'll often have a file called `func.R` containing those
project-specific functions. (Yeah, brilliantly clear file name,
right?)

Advantages to this:

- The main scripts will be shorter and easier to read, particularly if
  the functions are well-named.

- If parts of the formerly-repeated code need to be changed, you won't
  need to change them repeatedly, but just once, in the derived
  function.

- You may be able to reuse the functions for other purposes.

---

Now go to the page about [packaging functions for reuse](packages.html).

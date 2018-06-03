---
layout: page
title: Package functions for reuse
description: Brief discussion of the value of turning R code into a
             package, with links to tutorials.
---

Pulling out the major parts of your scripts as separate functions has
the advantage that you can more easily reuse that code.

But functions sitting deep within some project directory are not likely
to be used again. (&ldquo;It's in a file called `func.R`, but which
project was I working on?&rdquo;)

When possible, package up those useful functions as a stand-alone
thing. This will make it easier for you (and others) to reuse them.
It's also a good opportunity to _document_ those functions.

Writing R packages is really not so hard as one might think. See my
[R package primer](https://kbroman.org/pkg_primer),
[Hadley Wickham](http://had.co.nz/)'s
[R packages book](http://r-pkgs.had.co.nz/), or
[Hilary Parker](https://hilaryparker.com/)'s
[tutorial on R packages](https://hilaryparker.com/2014/04/29/writing-an-r-package-from-scratch/).
If you've written a
[personal R package](https://hilaryparker.com/2013/04/03/personal-r-packages/),
you might include your miscellaneous functions there, or write a
separate small package specific to your project.

If you prefer python to R, this may be even easier for you: a
[python module](https://docs.python.org/3/tutorial/modules.html) is
not much more than a file with a bunch of function definitions. Just
add some [docstrings](http://tovid.wikia.com/wiki/Python_tips/Docstrings).

---

Now go to the page about [version control](version_control.html).

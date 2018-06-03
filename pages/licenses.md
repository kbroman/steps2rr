---
layout: page
title: License your software
description: Brief discussion of software copyright and the importance
             of choosing a software license.
---

Your interest in making your computational work reproducible may be
entirely personal: it's more efficient and trustworthy. But ideally
you will choose to share the data and code that underlies your work, so
that others may share a similar level of trust in the results, and
so that they may further explore, learn from, and expand upon your work.

If you distribute software (such as the basic scripts for the
analyses in a paper), it is critical that you choose a _software
license_ and make that license clear.

Software licenses are about two things: _copyright_, and _protecting
yourself_ from being held liable if your software screws something up
somewhere down the line.

In the US, [copyright](https://www.copyright.gov/circs/circ01.pdf)
is _automatic_, and it gives you exclusive rights to copy your code. So if
you don't choose a license for your software, _no one else can use it!_

So, [pick a license, any license](https://blog.codinghorror.com/pick-a-license-any-license/).

There are
[lots of different software licenses](https://tldrlegal.com/) to
choose from. That's part of why this is such a painful topic. (That they are almost
all really boring to read is another part of the pain. The
[WTFPL](http://www.wtfpl.net/) is one of the few that is not boring.)

Personally, I choose between the
[MIT license](https://en.wikipedia.org/wiki/MIT_License) and the
[GNU General Public License (GPL)](https://www.gnu.org/copyleft/gpl.html). The
MIT license is among the more permissive. The GPL is
&ldquo;viral&rdquo; in that it extends to derivative works: software
that incorporates code that was licensed under the GPL must also be
licensed under the GPL. So I use the GPL _if I have to_ (that is, if
I've incorporated others' GPL code), and I use the MIT license
otherwise.

### Don't use a Creative Commons license for software

An important thing to remember: **don't use a
[Creative Commons](https://creativecommons.org/) (CC) license for
software**. Creative Commons licenses (like [CC-BY](https://creativecommons.org/licenses/by/3.0/))
are great, but they're for things like articles, books, and
videos, **but not software**. As
[they say in their FAQ](https://wiki.creativecommons.org/FAQ#Can_I_use_a_Creative_Commons_license_for_software.3F):

> We recommend against using Creative Commons licenses for software.

Use CC licenses for your lecture notes, slides, and articles, but not
for your software.

### What about CC0?

[CC0](https://creativecommons.org/publicdomain/zero/1.0/) (public
domain) seems appropriate for software: you're just saying that anyone
can do anything with the code.

But in some states (e.g., Maryland, I think), software is treated as a
&ldquo;good&rdquo; (like a car), and so if your code causes something
terrible to happen, you could be sued for damages. Using a lenient
license, like the
[MIT license](https://en.wikipedia.org/wiki/MIT_License), eliminates
that potential problem through the &ldquo;no warranty&rdquo; clause.

So, use [CC0](https://creativecommons.org/publicdomain/zero/1.0/) for
your lecture notes, slides, and web sites, but use a lenient license,
like the [MIT license](https://en.wikipedia.org/wiki/MIT_License), for
your software.

### Indicating your choice

So, pick a license, any license. And then indicate your choice, either
in a `ReadMe` file with your project, or in a separate `License` file,
or both.

With the MIT license, I would include the
[full text](https://opensource.org/licenses/MIT), filling in your
personal details.

With the GPL, take a look at
[these instructions](https://www.gnu.org/licenses/gpl-howto.html):

> the process involves adding two elements to each source file of your
> program: a copyright notice (such as &ldquo;Copyright 1999 Terry Jones&rdquo;),
> and a statement of copying permission, saying that the program is
> distributed under the terms of the GNU General Public License.

---

That's it! Now consider the [resources page](resources.html).

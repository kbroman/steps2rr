---
layout: page
title: Use version control
description: Brief discussion of the value of using formal version
             control, though it's not strictly necessary for
             reproducibility.
---

[Version control](https://git-scm.com/book/en/v2/Getting-Started-About-Version-Control)
is not strictly necessary for _reproducibility_, but it can be hugely
useful for _sanity_ (and for managing collaborative projects, and for
long-term efficiency).

Periodically zipping things up into a numbered and dated file is
great, but formal version control:

- Can make it easier to explore the history of changes
- Enables you to go back to an earlier state to find the source of a bug
- Allows you to try things out without worrying about breaking the things that work
- Can make it easier to incorporate changes from collaborators, even
  if you're all making simultaneous changes to the same set of files.

There are a number of different version control systems, but I'd
recommend starting with [git](https://git-scm.com), because it's widely
used, and because of [GitHub](https://github.com), which simplifies
collaboration and exploration.

To get started, consider my
[git/github guide](https://kbroman.org/github_tutorial).

Version control is a tough sell. It requires a big initial investment
in time and effort, initial experiences are often rocky, and the
advantages are mostly long-term. And it may seem like a big day-to-day
hassle, though trust me that, after a month or so, it will become a
natural part of your daily workflow.

Start by putting a single project under version control. Ideally
convince a collaborator to work on it with you. (Version control has
huge _short-term_ advantages in collaborative projects, such as in
merging simultaneous changes, or just keeping in sync.)


---

Now go to the page about [software licenses](licenses.html).

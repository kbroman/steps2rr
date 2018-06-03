---
layout: page
title: Organize your data and code
description: Brief discussion of file/directory organization, perhaps
             the most important step to take towards ease of
             reproducibility.
---

Perhaps the most important step to take towards ease of
reproducibility is to be _organized_. Ideally, the names of files and
subdirectories are self-explanatory, so that one can tell at a glance
what data files contain, what scripts do, and what came from what.

- **Encapsulate everything within one directory**. Have a single
    directory for a project, containing all of the data, code, and
    results for that project. This makes it easier to find things, or
    to zip it all up and hand it off to someone else.

- **Separate raw data from derived data** and other data summaries. I
    prefer to have a subdirectory `RawData/` and then another
    subdirectory `Data/`, or perhaps two other subdirectories
    `DerivedData/` (containing reformatted, reorganized, or cleaned
    data files) and `DataSummaries/` (containing summary information,
    like lists of subjects or genetic markers, or summary statistics
    extracted from the primary data in order to make a particular
    graph). This makes it easier to tell the nature of the data in a
    file, by its location within the project directory.

- **Separate the data from the code**. I prefer to put code and data in
    separate subdirectories. I'll have an `R/` subdirectory and
    perhaps also `Python/` and `Ruby/` subdirectories.

- **Use relative paths** (never absolute paths). If you encapsulate
    all data and code within a single project directory, then you can
    refer to data files with relative paths (e.g.,
    `../RawData/some_file.csv`). If you were to use an _absolute_
    path (like `~/Projects/SomeProject/RawData/some_file.csv` or
    `C:\Users\SomeOne\Projects\SomeProject\RawData\some_file.csv`)
    then anyone who wanted to reproduce your results but had the
    project placed in some other location would have to go in and edit
    all of those directory/file names.

- **Choose file names carefully**. I try not to change the names of
    raw data files that I get from a collaborator (though I'm often
    tempted to replace spaces with underscores). But scripts need
    names, and files with derived or cleaned data need names. Be as
    clear and explicit as possible. The same holds for the variables
    and functions within your scripts.

- **Avoid using &ldquo;final&rdquo; in a file name**. Nothing is ever
    final, and if you call something &ldquo;final&rdquo; you'll end up
    with things like `cleandata_final_rev3.csv`. If you want to keep
    multiple versions of a file, just append a number, like
    `cleandata_v8.csv`.

- **Write ReadMe files**. Even if you've organized and named things
    perfectly, you'll still want to include some documentation that
    explains what's what. A `ReadMe.txt` file (or `ReadMe.md`, for
    [Markdown](https://daringfireball.net/projects/markdown/)) in the
    main directory and perhaps also in each subdirectory may be
    sufficient. Describe the files and the process. And keep the
    ReadMe files up to date as things are added or changed.

---

Now go to the page about [doing everything with a script](scripts.html).

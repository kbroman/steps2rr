---
layout: page
title: Organize your data and code
---

Perhaps the most important step to take towards ease of
reproducibility is to be _organized_. Ideally, the names of files and
subdirectories are self-explanatory, so that one can tell at a glance
what data files contain, what scripts do, and what came from what.

- **Encapsulate everytihng within one directory**. Have a single
    directory for a project, containing all of the data, code, and
    results for that project. This makes it easier to find things, or
    to zip it all up and hand it off to someone else.

- **Separate raw data from derived data** and other data summaries. I
    prefer to have a subdirectory `RawData` and then another
    subdirectory `Data`, or perhaps two other subdirectories
    `DerivedData` (containing reformatted, reorganized, or cleaned
    data files) and `DataSummaries` (containing summary information,
    like lists of subjects or genetic markers, or summary statistics
    extracted from the primary data in order to make a particular
    graph). This makes it easier to tell the nature of the data in a
    file, by its location within the project directory.

- **Separate the data from the code**

- **Use relative paths** (never absolute paths)

---

Now go to the page about [automating the process and documenting dependencies](automate.html).

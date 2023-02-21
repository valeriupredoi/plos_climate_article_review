### Article: Pangeo-Enabled ESM Pattern Scaling

- name: Pangeo-Enabled ESM Pattern Scaling (PEEPS):  A customizable dataset of emulated Earth System Model output
- serial: PCLM-D-22-00161R1
- due date for review: February 23, 2023
- submission link: https://www.editorialmanager.com/pclm/
- reviewer: Valeriu Predoi
- review date: February 21, 2023

### General comments

Comments marked with ">>>...<<<" were initial comments for the unrevised version (from November 2022);
I am mostly looking at these being addressed.

>>> The article reads well, and is easy to follow, including good illustration and support of statements via figures. Structurally, it follows well, and the reader doesn't get lost in a myriad of sections and sub-sections; references are well places when they are needed, as well as pointers to available code on various code-sharing websites; figures are well captioned.
<<<

VP-R1: still stands 

>>> However, my view is that, even if it describes well
the experimental setup and its conditions, together with the results (figures and tables), the article needs to demonstrate a bit more how PEEPS, the computational toolthat is the main focus of the article, integrates and relates to other such tools and software packages, available elsewhere. I'd suggest this be addressed by adding a subsection where the authors demonstrate that:
- PEEPS is comparable to other similar tools performing pattern scaling, both in terms of performance and results;
- PEEPS offers net performance benefits compared to running a number of metrics on the actual model (ESM) data (which is clearly much more resource-intensive, but the authors don't tell us by how much, in rough numbers of computing resources)
I am aware this is more of a methods paper, than it is
a systematic review of available tools, but even so, as a reader, I would like to be reassured that PEEPS is a solid tool for my work, and I
shouldn't look elsewhere for another tool that does the same type of analysis. If these comparison results are available elsewhere, then simply referencing that source would be fine.
<<<

VP-R1: this has been addressed and I could find a decent amount of comparisons to other similar tools/approacehs; performance was
aslo touched upon, not exhaustively but with a fair amount of info so the user has some idea what to expect in terms of resources - runtimes and memory

>>> As a final point, I'd suggest the authors include a quick example on how to use the Jupyter notebook (configuration, guidelines for a basic used case, not anything too detailed) or, alternatively, a pointer to the technical documentation.
<<<

VP-R1: instructions and documentation are still lacking a tad (I just had a look at the GitHub repo as well, which would benefit from a doc repo), but provided this is work in progress, and the submitted article's purpose is not to document the data producing runs, but rather, to document why one should run them at all,
I am going to let this one go, provided the authors promise to improve he code's documentation :)

Specific questions and minor suggestions below
----------------------------------------------

- GitHub repository that holds a frozen copy of the code: `https://github.com/JGCRI/linear_pattern_scaling` - great to have it on GitHub!
- couple more cases of lower case "python" instead of "Python"
- consider updating base Python to Python >= 3.9, 3.7 is already obsolete, and barely supported at all
- consider using a dependency/package manager like e.g. Miniconda with the Mamba solver for the environment where the Jupyter notebook runs
- consider implementing automated tests
- these last points are very technical, so no need to address them in the manuscript, just recommending them to improve PEEPS' quality as a piece of software (I can help with any of these, should authors need assistance)

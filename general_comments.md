### Article: Pangeo-Enabled ESM Pattern Scaling

- serial: PCLM-D-22-00161
- reviewer: Valeriu Predoi
- review start: 14 November 2022


### General comments

The article reads well, and is easy to follow, including good illustration and support of statements via figures. Structurally, it follows well, and the reader doesn't get lost in a myriad of sections and sub-sections; references are well places when they are needed, as well as pointers to available code on various code-sharing websites; figures are well captioned.

However, my view is that, even if it describes well
the experimental setup and its conditions, together with the results (figures and tables), the article needs to demonstrate a bit more how PEEPS, the computational toolthat is the main focus of the article, integrates and relates to other such tools and software packages, available elsewhere. I'd suggest this be addressed by adding a subsection where the authors demonstrate that:

- PEEPS is comparable to other similar tools performing pattern scaling, both in terms of performance and results;
- PEEPS offers net performance benefits compared to running a number of metrics on the actual model (ESM) data (which is clearly much more resource-intensive, but the authors don't tell us by how much, in rough numbers of computing resources)

I am aware this is more of a methods paper, than it is
a systematic review of available tools, but even so, as a reader, I would like to be reassured that PEEPS is a solid tool for my work, and I
shouldn't look elsewhere for another tool that does the same type of analysis. If these comparison results are available elsewhere, then simply referencing that source would be fine.

As a final point, I'd suggest the authors include a quick example on how to use the Jupyter notebook (configuration, guidelines for a basic used case, not anything too detailed) or, alternatively, a pointer to the technical documentation.

Specific questions and minor suggestions below -

### Tech/sci questions

- is T(x, t) in fact a 3-dim space-time vector? Then it should be expressed as T(x, y, t);
- are you setting a threshold for the lowest percentage that the residuals are within 1-sigma?
- why choose a 20 year averaging period (please explain briefly) - variability can still be detected if averaging period is set to, say 2-4 years,
for monthly means data
- lines 174-176: worse/better performance is a vague term if a performance metric is not quoted, are we still looking at the deviation
from the baseline? If so please give some numbers that support your performance statements
- line 226 onwards (code and output): please specify the Python version (major version, to the very least); please specify the type of netCDF file the code outputs (netCDF4, 3, or classic); are the netCDF output files CF-compliant and/or CMOR compliant? (I assume CMOR, if CMIP6 data was used from ESGF)
- line 239 - performance: please specify clockspeed of CPU of said "laptop", rough estimation of memory i.e. are you loading all the data in memory, or are you using memory-efficient tools like Dask or xarray+Dask?


### Typos and suggestions

- typo: line 51: python packages -> Python packages
- suggestion: line 53: ESM output -> ESM output data
- suggestion: line 54: "library" can be confused with its software meaning, suggest "database" instead
- suggestion: line 59: "Because of Pangeo" -> briefly explain (e.g. cloud-based analysis platform etc)
- suggestion: line 59: "the dataset and the PEEPS Jupyter notebook are effectively the same thing" - colloquial and incorrect,
  a netCDF is a file type, whereas a Jupyter notebook is a web-based Python runtime ecosystem, please rephrase;
- typo: line 114: error -> errors
- suggestion: line 188: "There is strong reason to suspect that it would" -> "There is strong reason to believe that it would" (suspect bears a negative conotation)
- ty[e: line 226: python -> Python

### Article: Pangeo-Enabled ESM Pattern Scaling

- serial: PCLM-D-22-00161
- reviewer: Valeriu Predoi
- review start: 14 November 2022


### General comments


### Tech/sci questions

- is T(x, t) in fact a 3-dim space-time vector? Then it should be expressed as T(x, y, t);
- are you setting a threshold for the lowest percentage that the residuals are within 1-sigma?
- why choose a 20 year averaging period (please explain briefly) - variability can still be detected if averaging period is set to, say 2-4 years,
for monthly means data
- lines 174-176: worse/better performance is a vague term if a performance metric is not quoted, are we still looking at the deviation
from the baseline? If so please give some numbers that support your performance statements
(end line 183)


### Typos and suggestions

- typo: line 51: python packages -> Python packages
- suggestion: line 53: ESM output -> ESM output data
- suggestion: line 54: "library" can be confused with its software meaning, suggest "database" instead
- suggestion: line 59: "Because of Pangeo" -> briefly explain (e.g. cloud-based analysis platform etc)
- suggestion: line 59: "the dataset and the PEEPS Jupyter notebook are effectively the same thing" - colloquial and incorrect,
  a netCDF is a file type, whereas a Jupyter notebook is a web-based Python runtime ecosystem, please rephrase;
- typo: line 114: error -> errors

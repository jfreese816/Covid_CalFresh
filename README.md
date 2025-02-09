# Charting Covid-19 Impact to California's Food Assistance Program




## Table of Contents
* [Project Proposal](#project-proposal)
* [Data Sources](#data-sources)
* [Key Takeaway](#key-takeaway)
* [Built With](#built-with)



## Project Proposal
We wanted to understand if usage of California's CalFresh program surged as a result of increased COVID-19 infection rates. CalFresh is California's implementation of the Federal Supplemental Nutrition Assistance Program (SNAP), which provides food benefits to help people purchase food at the grocery store. Three datasets were merged, munged, shaped and visualized to understand how COVID affected various counties and the relationship of COVID to employment, population and usage of CalFresh benefits.

###### Scope
Key assumption: As Covid infection rates increased, so did usage of CalFresh benefits.
* Geographic coverage: California
* Timeframe: January 2020 through February 2021

###### Key Questions
The team wrote out a list of questions that we wanted to seek from the data.
*  What were the 10 counties with the highest infection rates?
*  What was the worst affected county?
*  What was the least affected county?
*  What is the relationship between rural and urban infection rates?
*  What are the worst covid infection rates as a percentage of population? Are the counties rural, urban, or mixed?
*  Show the correlation between COVID-19 infection rates and CalFresh usage

## Data Sources
We needed to find data that would provide infection rates, population, unemployment, and CalFresh information. Additionally, the data had to be available by year, month, state, and county. There was no single source for the information, so we investigated several sources; www.cdss.ca.gov, www.data.nal.usda.gov, www.data.ca.gov, www.fns.usda.gov, www.github.com/nytimes, www.covidtrackering.com, www.census.gov

After examining several datasets, we settled on three. Subsquently, we discovered that there was A LOT of data munging and clean up that had to happen in order to make it usable.  
1. CalFresh. https://www.cdss.ca.gov/inforesources/research-and-data/calfresh-data-tables/dfa256
1. US_Counties. https://github.com/nytimes/covid-19-data
1. US Census. https://www.census.gov/data/datasets/time-series/demo/popest/2010s-counties-total.html


## Key Takeaway
We found that COVID-19, initially did not have a direct impact on CalFresh usage. Rather, goverment containment policies, which created a massive spike in unemployment, primarily contributed to the marked increase of CalFresh usage. In fact, CalFresh usage increased with unemployment and decreased in sympathy with declining unemployment. It was only after the second-wave of infections, in the fall of 2020, that we see a direct correlation between increased CalFresh benefit usage and a surge in COVID cases. 

##### Retrospective
The project was fun and challenging. It was great to be able to employ the knowledge gained over the past 5-weeks. Working, watching the lines of code take shape, transforming data into visual information was intensely satisfying. Having worked on the project with a team, we learned several things, and areas that we could have improved upon. In no particular order:
###### Project
> “Give me six hours to chop down a 
> tree and I will spend the first four 
> sharpening the axe.” – Abraham Lincoln
1. Quickly come up with your supposition, explore areas of interest to help develop the key question/hypothesis that you wish to explore.
1. Develop 5-8 supporting questions that will support the hypothesis.
1. Review the datasets to see what data clean up needs to be done, e.g. harmonizing column names, identify data that needs str or int converted, etc.
1. Develop a list of actions, milestones and a timeline. Otherwise you will get into the last minute crunch of wrangling everyone's part into a coherent flow.
###### Process
2. One person will need to step up to help project manage otherwise time will slip away.
3. Commit to your branch often. It's free and it'll save your butt should you or someone else makes a mistake, by being able to rollback to a prior commit.
4. Learn bash/terminal commands to reset, revert, return to a previous commit state. https://tinyurl.com/hrejd4hw
5. Gold for me was learning that you can do a 'git checkout x', where x can be main, your branch, someone elses branch, or even the ssh of a prior commit. 

###### Would Like to...
* Further examine if the later uptake of CalFresh benefits was due to exhaustion of financial resources
* Understand the relationship of the mean income of a county versus when the uptake in CalFresh benefits started
* Use of a heatmap to visualize the above relationship of income to CalFresh uptake

## Built With
* Jupyter notebook Code Version: 6.0.3
Chrome: 87.0.4280.141
Node.js: 12.18.3
OS: Windows_NT x64 10.0.19042
* conda 4.10.0
* Python 3.6.10 Anaconda, Inc.
* Kite Pro Version: 1.2021.310.0

```python
# Dependencies & Setup
import matplotlib.pyplot as plt
import pandas as pd
import scipy.stats as st
import numpy as np
import calendar
```

## Contributing
* DeJuan Hall
* Jackson Freese
* Siddharth Das
* John Chan


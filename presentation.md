
Feature Names Format Pleaser
========================================================
author: Davis Clark
date: July 26, 2015
font-import: http://fonts.googleapis.com/css?family=Arial
font-family: 'Arial'
incremental:true

The Problem
========================================================

Too often, we receive a dataset of feature names, filled with ridiculous punctuation marks and capitalization schemes.

```r
data.frame(Features1=names(data)[1:5], Features2=names(data)[6:10])
```

```
             Features1  Features2
1                    X new_window
2            user_name num_window
3 raw_timestamp_part_1  roll_belt
4 raw_timestamp_part_2 pitch_belt
5       cvtd_timestamp   yaw_belt
```
Analysis requires **obnoxious amounts of validation**, as no mortal man will remember such feature names.

Yesterday's Solution
========================================================
Yesterday, you were forced to type the following, many times, everyday:

```r
names(data)<-tolower(names(data))
names(data)<-gsub("\\_", "", names(data))
```

```
          Features1 Features2
1                 x newwindow
2          username numwindow
3 rawtimestamppart1  rollbelt
4 rawtimestamppart2 pitchbelt
5     cvtdtimestamp   yawbelt
```
**And what of today?**

Today, You Have Format Pleaser
========================================================
Feature Names Format Pleaser is a tiny, Shiny app that makes feature name formatting... pleasurable.

**It keeps your fingers nimble** and **shortens the time to analysis**. 

Thanks to Format Pleaser, you'll be running random forests and writing documentation in no time.

Features: Today & Tomorrow
========================================================

**Features**:
- Support for .csv files, not exceeding 15MB
- Numerous formatting options, including uppercase and lowercase transformations
- Instant previewing of the resultant dataframe names

**Future developments**:
- Ability to directly download a newly formatted file
- Support for XLS files

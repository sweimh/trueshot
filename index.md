---
title       : True Shooting Percentage Calculator
subtitle    : A Data Project from Coursera
author      : Mark H.
job         : October, 2016
framework   : io2012   # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [mathjax]     # {mathjax, quiz, bootstrap}
mode        : selfcontained   # {selfcontained, standalone, draft}
knit        : slidify::knit2slides
---

## Introduction

This presentation is part of the Course Project for the Coursera Developing Data Products class. The peer assessed assignment has two parts. First, we need to create a Shiny application and deploy it on Rstudio's servers. 

Second, we should use Slidify or Rstudio Presenter to prepare a reproducible pitch presentation about the application. This presentation adresses the second part of the course project.

The app developed for the first part of the assignment is avalilable at: https://markh.shinyapps.io/TrueShot/

Source code for ui.R and server.R files are available on the GitHub: https://github.com/sweimh/Shiny-Application-True-Shot-Prct

--- .class #id 

## True Shooting Percentage (TS%)

In basketball, shooting percentage is a general measure of the likeliness of a player's shooting attempt converts (scores). 

However, all shots are not weighted equally - one point for free throws (FT), two points for a field goals made within certain distance from a basket, or three points for attempts made from further away. As a result, the proliferation of a player's shot tends to be measured separately, by FT%, FG%, and three-point FG%.

True shooting percentage (TS%) intends to be the one measure that  "more accurately calculate a player's shooting than field goal percentage, free throw percentage, and three-point field goal percentage taken individually. Two- and three-point field goals and free throws are all considered in its calculation."

Over 170 NBA players took more than 500 shots during the 2015-16 NBA regular season*. Based on their calculated TS%, ranging from 0.437 to 0.669.

*Data source: http://www.sportingcharts.com/nba/stats/player-true-shooting-percent-leaders/2015/

--- .class #id2

## TS% Formula and Sample Run
$$TS\% = \frac{PTS}{2{(FGA + {0.44 \times FTA}})}$$

- PTS = points scored
- FGA = field goal attempts
- FTA = free throw attempts

<b>Sample Run</b>

Calculate TS%, given a player who scores 60 points from 50 field goal attemps and 12 free throw attempts


```r
TSPct_calc <- function(pts, fga, fta) {pts/(2*(fga+(0.44*fta)))}
TSPct_calc(60, 50, 12)
```

```
## [1] 0.5426918
```

--- .class #id3

## Links to App and Source

The app developed for the first part of the assignment is avalilable at:

https://markh.shinyapps.io/TrueShot/

Source code for ui.R and server.R files are available on the GitHub:

https://github.com/sweimh/Shiny-Application-True-Shot-Prct

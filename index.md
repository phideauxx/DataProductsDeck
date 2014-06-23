---
title       : Class Project Presentation
subtitle    : 
author      : Phideaux
job         : 
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : [bootstrap, quiz]            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Grade Calculator

1. Did you ever want to know where you stood in your class?
2. Did you ever want to know how well you needed to do on your exam to get the grade you wanted?
3. Have you ever just wanted to slide some sliders around and see what happens?


--- .class #id 

## Then this is the app for you!



Just move the sliders to your scores or potential scores and see where you stand. 

Check out the app at:

https://phideaux.shinyapps.io/DevelopingDataProd/

And check out the easily modifiable code at:

https://github.com/phideauxx/DevelopingDataProdProj

---

Here is some R code from the Grade Checking App


```r
#Add up total points earned
totalScore <- function(quiz, homework, test){
  total <- quiz + homework + test
  total
}

#Calculate total percent based on total points earned / total points possible * 100
totalPercent <- function(quiz, homework, test, totalPP = 170){
  percent <- (totalScore(quiz, homework, test) / totalPP) * 100
  percent
}

totalPercent(quiz = 30, homework = 40, test = 70, totalPP = 150)
```

```
## [1] 93.33
```

--- &radio

## Did you like what you saw?

1. _Yes_

2. No

*** .hint
You DO like it

*** .explanation
Go check it out: https://phideaux.shinyapps.io/DevelopingDataProd/


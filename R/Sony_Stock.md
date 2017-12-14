---
title: "Sony Stock"
author: "Allan Brooks"
date: "6/27/2017"
output: 
    html_document:
        keep_md: true
---
library(xts)
library(zoo)
library(quantmod)

#### R Markdown

This is an R Markdown document. Markdown is a simple formatting syntax for authoring HTML, PDF, and MS Word documents. For more details on using R Markdown see <http://rmarkdown.rstudio.com>.

When you click the **Knit** button a document will be generated that includes both content as well as the output of any embedded R code chunks within the document. You can embed an R code chunk like this:

```{r}
library(quantmod)
getSymbols('SNE', src='yahoo')
```


The is the sony stock from Jan 2017 to June 2017. This graphs includes Bollinger Bands, Commodity Channel Indicators
```{r}
chartSeries(SNE, theme='white', TA="addVo();addBBands();addCCI()", subset='2017-01-01::2017-06-01')
```


Note that the `echo = FALSE` parameter was added to the code chunk to prevent printing of the R code that generated the plot.

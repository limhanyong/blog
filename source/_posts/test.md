---
title: "test"
output:
  html_document:
    keep_md: true
date: '2022-06-21 17:00:01'
---

## csv 파일 불러오기
- csv 파일을 볼러옵니다.



```r
mpg1 <- read.csv("mpg1.csv")
str(mpg1)
```

```
## 'data.frame':	234 obs. of  5 variables:
##  $ manufacturer: chr  "audi" "audi" "audi" "audi" ...
##  $ trans       : chr  "auto" "manual" "manual" "auto" ...
##  $ drv         : chr  "f" "f" "f" "f" ...
##  $ cty         : int  18 21 20 21 16 18 18 18 16 20 ...
##  $ hwy         : int  29 29 31 30 26 26 27 26 25 28 ...
```

## 데이터 시각화 하기
-cty, hwy 산점도를 그려본다.

```r
library(ggplot2)
ggplot(mpg1, aes(x = cty, y = hwy)) + geom_point()
```

![](/images/rmd_0620/unnamed-chunk-2-1.png)<!-- -->

## 새로운 그림 
- 새로운 시각화를 함
![](/images/rmd_0620/pressure-1.png)

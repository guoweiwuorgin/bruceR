# bruceR

**BR**oadly **U**seful **C**ollections and **E**xtensions of **R** functions

![](https://img.shields.io/badge/R-package-success)
![](https://img.shields.io/badge/Version-0.4.7-success)
![](https://img.shields.io/github/license/psychbruce/bruceR?label=License&color=success)
[![](https://img.shields.io/badge/lifecycle-maturing-blue.svg)](https://www.tidyverse.org/lifecycle/#maturing)
[![](https://img.shields.io/github/stars/psychbruce/bruceR?style=social)](https://github.com/psychbruce/bruceR/stargazers)

[![](https://img.shields.io/badge/Follow%20me%20on-Zhihu-blue)](https://www.zhihu.com/people/psychbruce/ "Personal profile on Zhihu.com")


## Citation
Bao, H.-W.-S. (2020). bruceR: Broadly useful collections and extensions of R functions [R package]. https://github.com/psychbruce/bruceR


## User Guide
### Install
```r
#### 安装步骤 ####

## 第1步：安装基础R包（如果已经安装过，请忽略）
install.packages("devtools")
install.packages("tidyverse")
install.packages("ggstatsplot")

## 第2步：更新所有R包（为了避免第3步频繁出错）
update.packages(ask=F)

## 第3步：安装bruceR包
devtools::install_github("psychbruce/bruceR")
```
- Please DO NOT use `install.packages("bruceR")`, because this package HAS NOT BEEN put on the [CRAN](https://cran.r-project.org/).
- [Installation Bugs and Solutions (安装遇到问题时请阅读！)](https://github.com/psychbruce/bruceR/blob/master/Installation%20Bugs%20and%20Solutions.md)


### Package dependency
> *We are all standing on the shoulders of giants.*

`bruceR` depends on some important packages and also automatically installs many other useful packages for users. Many functions in `bruceR` are extensions of the functions in these packages.

Once you load `bruceR` to the global environment with `library()`, it will also load these packages:
- `rio`: Data input/output for almost all file formats within one function (`import`/`export`).
- `dplyr`: Data manipulation and preprocessing.
- `stringr`: Toolbox for dealing with strings and regular expressions.
- `lubridate`: Toolbox for dealing with dates and times.
- `data.table`: Advanced 'data.frame' with higher efficiency.
- `performance`: Assessment of regression models performance.
- `ggplot2`: Data visualization.
- `cowplot`: Useful add-on for ggplot2.

No need to load each one with its own call. Loading `bruceR` is enough.


### Main functions in `bruceR`
- [x] Basic use and analyses (e.g., correlation matrix with plot)
  + `Print()`, `Describe()`, `Freq()`, `Corr()`, ...
  + `set.wd()`, `set.seeds()`, `dtime()`, ...
  + `%notin%`, `%partin%`, ...
  + `LOOKUP()`, ...
- [x] Multivariate computing (e.g., scale mean score with reverse scoring)
  + `RECODE()`, `RESCALE()`
  + `COUNT()`, `MODE()`, `SUM()`, `MEAN()`, `STD()`, `CONSEC()`
- [x] Reliability and validity analyses (e.g., Cronbach's α, exploratory/confirmatory factor analysis)
  + `Alpha()`
  + `EFA()`, `CFA()`
- [x] *t*-test, ANOVA, simple-effect analyses, and multiple comparisons
  + `MANOVA()`, `EMMEANS()`
- [x] Advanced toolbox and output for general/generalized ordinary/multilevel linear models
  + `grand_mean_center()`, `group_mean_center()`
  + `GLM_summary()`, `HLM_summary()`, `regress()`, `model_check()`
  + `med_mc()`, `simple_slope()`
- [x] Nice themes of `ggplot2` ready for scientific publication
  + `theme_bruce()`


### Learn more by running code
```r
library(bruceR)

## Overview of Package
?bruceR

## See Help Pages of Functions
?MANOVA
?EMMEANS
?GLM_summary
?HLM_summary

## Check Update
check_update()

## Run Some Examples
example("Print")
example("Describe")
example("Freq")
example("Corr")

example("MEAN")
example("LOOKUP")

example("GLM_summary")
example("HLM_summary")
example("model_check")
```


## Release Notes
### Current version: `0.4.7`
### Major changes:
+ `0.4.0` - 2019.12
  + Added citation information
  + General bug-fixes and improvements
+ `0.3.0` - 2019.10
  + Added new functions for ANOVA, simple-effect analyses, and multiple comparisons
  + General bug-fixes and improvements
+ `0.2.0` - 2019.08
  + Added help pages
  + General bug-fixes and improvements
+ `0.1.0` - 2019.06
  + Initial commit


## Author
[Han-Wu-Shuang (Bruce) Bao - 包寒吴霜](https://www.zhihu.com/people/psychbruce/ "Personal profile on Zhihu.com")

E-mail: baohws@psych.ac.cn or psychbruce@qq.com

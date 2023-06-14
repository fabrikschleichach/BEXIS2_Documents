# R

<!-- TOC -->

- [1 General Information](#1-general-information)
- [2 Requirements](#2-requirements)
- [3 Install](#3-install)
- [4 Preparation](#4-preparation)
- [5 Functions](#5-functions)


<!-- /TOC -->

## 1 General Information

With the ![rBExIS](https://github.com/BEXIS2/rBExIS) package you can work with your BEXIS2 data and metadata directly in R or RStudio. 

## 2 Requirements

- **R** (e.g. https://cran.r-project.org/bin/windows/base/ for Windows, otherwise start ![here](https://cran.r-project.org/bin/))
- **RStudio** (https://www.rstudio.com/products/rstudio/download/#download)
- **Rtools** (e.g. https://cran.r-project.org/bin/windows/Rtools/ for Windows, , otherwise start ![here](https://cran.r-project.org/bin/)) 

## 3 Install

Unfortunately, rBExIS is not available via RStudio package manager. You have to install it from GitHub. Therefore, you have to install and load **devtools** first:

```
install.packages("devtools")
library(devtools)
```

Second, install and load **rBExIS**:

```
install_github("BEXIS2/rBExIS", subdir = "rBExIS")
library(rBExIS)
```

## 4 Preparation

Before you can start working with rBExIS, you have to configure it by adding some values / options. 

To get an overview of the current configuration, use the following command:

```
bexis.options()
```

You have to set at least the *base_url*, which is the domain/url of the BEXIS2 instance you would like to connect with. In our case **betafor.biozentrum.uni-wuerzburg.de**.

```
bexis.options("base_url" = "https://www.betafor.biozentrum.uni-wuerzburg.de/")
```




![Go to top](#1-general-information)
   

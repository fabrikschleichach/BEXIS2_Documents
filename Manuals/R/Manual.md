# R

<!-- TOC -->

- [1 General Information](#1-general-information)
- [2 Requirements](#2-requirements)
- [3 Install](#3-install)
- [4 Preparation](#4-preparation)
- [5 Functions](#5-functions)
	- [5.1 List of Dataset Ids](#51-list-of-dataset-ids)
   - [5.2 Primary Data of a specific Dataset](#52-primary-data-of-a-specific-dataset)
   - [5.3 List of Metadata Objects](#53-list-of-metadata-objects)
   - [5.4 Metadata of a specific Dataset](#54-metadata-of-a-specific-dataset)
   - [5.5 List of Data Structures](#55-list-of-data-structures)
   - [5.6 Data Structure of a specific Dataset](#56-data-structure-of-a-specific-dataset)


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

For authentication / authorization you can set your **username and password** and / or use your **token**:

```
bexis.options("authorization_basic" = "username:password")

bexis.options("authorization_bearer" = "KJkSKJxEoiXwk9ipAvKkNEJ9isGGi64drtQDRf9KKCDRKSE5JYvz5j8Yx5Unvto5")

```

You can find your token by clicking on your account and selecting _Token_:

![Token](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/R/Images/Token.PNG)



## 5 Functions

### 5.1 List of Dataset Ids

To get a list of all dataset ids in our BEXIS2 instance, type:

```
bexis_dataset_ids <- rBExIS::bexis.GetDatasetIds()
```

![bexis_dataset_ids](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/R/Images/bexis_dataset_ids.PNG)

### 5.2 (Primary) Data of a specific Dataset

To get the (primary) data of a specific dataset, use the following function. As parameter _id_, use the id of the dataset you want to get the data from. 

```
bexis_data <- rBExIS::bexis.GetDatasetById(id)
```

![bexis_data](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/R/Images/bexis_data.PNG)

### 5.3 List of Metadata Objects

To get a list of all metadata objects, type: 

```
bexis_metadata_list <- rBExIS::bexis.GetMetadata()
```

![bexis_metadata_list](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/R/Images/bexis_metadata_list.PNG)

### 5.4 Metadata of a specific Dataset

To get the metadata of a specific dataset, use the following function. As parameter _id_, use the id of the dataset you want to get the metadata from. 

```
bexis_metadata <- rBExIS::bexis.GetMetadataById(id)
```

![bexis_metadata](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/R/Images/bexis_metadata.PNG)

### 5.5 List of Data Structures

To get a list of all data structures in our BEXIS2 instance, type:

```
bexis_structures <- rBExIS::bexis.GetDataStructures()
```

![bexis_structures](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/R/Images/bexis_structures.PNG)

### 5.6 Data Structure of a specific Dataset

To get the data structure of a specific dataset, use the following function. As parameter _id_, use the id of the **data structure** you want to get.

```
bexis_structure <- rBExIS::bexis.GetDataStructureById(id)
```

![bexis_structure](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/R/Images/bexis_structure.PNG)

![Go to top](#1-general-information)
   

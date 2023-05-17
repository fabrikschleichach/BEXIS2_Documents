# Get Started

<!-- TOC -->

- [1 General Information](#1-general-information)
- [2 How to start?](#2-how-to-start?)
- [3 Upload Data](#3-upload-data)
- [4 Search Data](#4-search-data)
- [5 Dashboard](#5-dashboard)


<!-- /TOC -->

## 1 General Information

*BETA-FOR Data* is the Data Platform of BETA-FOR. For all data created within BETA-FOR there should be a Dataset in *BETA-FOR Data*. 

In BEXIS2, data is stored and managed as part of a **Dataset**. You can think of a Dataset as a container for the (primary) data on the one hand, and the metadata on the other. 

![Dataset](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Get%20Started/Images/Dataset.PNG)

* **Metadata**: describing facts about the dataset, e.g. who created the dataset and when
* **(Primary) Data**: can be files or tabular data
* **File**: unstructured data, e.g. an audio file or image
* **Tabular Data**: structured data; supported formats are Excel and ASCII
* **Data Structure**: describes the structure of the data

Big raw data cannot be stored in *BETA-FOR Data* directly. Upload it to ... and include a reference to the exact storage location in the ![metadata](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#38-alternate-identifiers).

To ensure that all features work as intended, it is recommended to use **Chrome** as browser. Make sure that you always have the ![latest version](https://www.google.com/intl/de/chrome/update/) installed. 

## 2 How to start?

Most features are only applicable if you are succesfully logged in. 

Information about how to get an *BETA-FOR Data* account can be found ![here](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Registration%20and%20Login/Manual.md#1-registration).

More information about the Login is collected ![here](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Registration%20and%20Login/Manual.md#2-login).

## 3 Upload Data

How to upload Data to BEXIS2 depends on the type of your (primary) Data: 

Workflow for Files (e.g. Images, Audio files, scripts, ...):

1. ![Create a Dataset](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#2-create-a-dataset) as Container for your data
2. ![Describe your data](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#3-provide-some-metadata) by filling in the Metadata form
3. ![Upload your data](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#4-upload-data)

(Best practice) Workflow for Tabular Data (e.g. Excel files)

1. ![Create a Data Structure](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Manual.md#21-create-a-data-structure) for your tabular data
2. Download the Data Structure as an ![Excel template](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Manual.md#24-download-an-excel-template)
3. ![Fill the template](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Manual.md#25-work-with-an-excel-template) with your data
4. ![Create a Dataset](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#2-create-a-dataset) as Container for your data
5. ![Describe your data](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#3-provide-some-metadata) by filling in the Metadata form
6. ![Upload your data](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#4-upload-data)

## 4 Search Data

If you want to have an overview of all Datasets that have been created so far or if you are looking for some particular data, e.g. of another subproject, go to the _Search_ page.

![Search](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Get%20Started/Images/Search.PNG)

If the checkbox _public only_ is selected, only Datasets that have already been published, are displayed.

You can limit your search results by selecting a Facet. If you, for example, are only interested in Datasets of the project BETA-FOR, select "BETA-FOR".

If you want to have a look at the Datasets of a particular subproject, e.g. SP9, enter "BETA-FOR_SP9" in the textfield and click on _Search_.
Note, that there is a schema for depicting ![titles](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#34-titles): **Project_Subproject_Organism_Method/Device_Year**.
All parts of the title are searchable. 

If you are not the ![Creator](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#33-creators) nor a ![Contributor](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#36-contributors) of a Dataset, you can only see its Metadata, not the (Primary) Data. To get access, send an ![Access Request](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Dataset%20Permissions/Manual.md#23-dataset-requests) to the Owners.

## 5 Dashboard

![Dashboard](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Get%20Started/Images/Dashboard.PNG)

The Dashboard is like your personal homepage. Here you can find an overview of all your Datasets, your Requests and Requests concerning your Datasets. 

![My Datasets](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Get%20Started/Images/My_Datasets.PNG)

The Datasets are grouped by ![permission](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Dataset%20Permissions/Manual.md#2-unpublished-datasets): 
* **Own**: full permission, including granting permission
* **Edid**: write permission
* **Download**: read permission

Datasets which are marked red have incomplete metadata.

![Go to top](#1-general-information)
   

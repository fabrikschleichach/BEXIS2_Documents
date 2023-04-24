# Data Collection: Metadata and Data


<!-- TOC -->

- [Data Collection: Metadata and Data](#data-collection-metadata-and-data)
	- [1 Overview](#1-overview)
	- [2 Create a Dataset](#2-create-a-dataset)
	- [3 Provide some Metadata](#3-provide-some-metadata)
		- [3.1 General Information](#31-general-information)
		- [2 Upload data](#2-upload-data)
			- [2.1. Upload Tabular Data](#21-upload-tabular-data)
				- [Select File](#select-file)
				- [Get File Information](#get-file-information)
				- [Specify Dataset](#specify-dataset)
				- [Choose Update Method](#choose-update-method)
				- [Validation](#validation)
				- [Summary](#summary)
			- [2.2 Upload File](#22-upload-file)
		- [3 Import Data](#3-import-data)
			- [3.1 Select File](#31-select-file)
			- [3.2 Metadata](#32-metadata)
			- [3.3 Select Areas](#33-select-areas)
			- [3.4 Verification](#34-verification)
			- [3.5 Summary](#35-summary)
	- [4 Push Big File](#4-push-big-file)
	

<!-- /TOC -->

## 1: Overview

In BEXIS2, data is stored and managed as part of a dataset. You can think of a Dataset as a container for the (primary) data on the one hand, and the metadata on the other.

![grafik](https://user-images.githubusercontent.com/68608907/233026141-c3e39d31-be31-46c5-924b-18d11406d5d7.png)

* **Metadata**: describing facts about the dataset, e.g. who created the dataset and when
* **(Primary) Data**: can be files or tabular data
* **File**: unstructured data, e.g. an audio file or image
* **Tabular Data**: structured data; supported formats are Excel and ASCII
* **Data Structure**: describes the structure of the data

You can upload a file or tabular data to the system in three steps:
1. [Create a Dataset](#2-create-dataset) as Container for your data
2. Describe your data by filling in the Metadata form
3. Upload your data


## 2 Create a Dataset

Select the Collect menu and click on Create Dataset. 

![CreateDataset](https://user-images.githubusercontent.com/68608907/233044507-d88d6393-2693-4841-ac2b-91f76962f3c5.PNG)

You can either create a new Dataset or select an existing one to copy its metadata.  

![NewDataset](https://user-images.githubusercontent.com/68608907/233046860-ba247d11-0149-4c0a-9e61-6b5079e15885.PNG)

Select a Data Structure that fits to your data.

Note: Tabular data can only be uploaded to the system if there is a corresponding Data Structure which defines its variables. If you have not created a Data Structure for your data yet, do it now (check the "Create a Data Structure"-Manual).

![grafik](https://user-images.githubusercontent.com/68608907/233047930-2b1cf861-6269-428b-9f2f-3ad3afdd29ae.png)

Finally, select DataCite_bexis as Metadata Structure and click the Next button.


## 3 Provide some Metadata

### 3.1 General Information

**DataCite_bexis** is a DataCite profile. For more information about the DataCite metadata scheme, visit: https://schema.datacite.org/meta/kernel-4.4/.

The metadata form contains different icons. Here is an explanation:

![Required](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/red_star.png)           Required attributes

![Add](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/plus.png)        Add an attribute

![Mines](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/mines.png)        Remove an attribute

![Up Down](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/up_down.png)  Change order of the attribute

![Expand](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/expand.png)![Collapse](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/collapse.png)      Expand / collapse

![Help](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/help.png)   	Show help information. The button on the right top hides / shows all help information. 

There are some fields, e.g. *Identifier*, that cannot be selected because they are set automatically by the system.
Other fields, e.g. *Publisher*, have a note: “If possible, use an entry from autocomplete list.”. In this case, you may only enter the first letter of the item and the system will automatically complete it.

### 3.1.1 Basic

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Identifier			| Will be set automatically.	| 1		|
| @Identifier type		| Will be set by the data manager.	| DOI	|
| Publisher			| Use an entry from autocomplete list. Fill in the first letter of the publisher. Default is **University of Würzburg**.				| University of Würzburg |
| Publication Year 		| Enter the year, when you plan to publish the dataset, or leave the field empty. | 2025
| Resource Type 		| There are 3 options: **Human Observation**, **Machine Observation** and **Material Citation**. Check the info button for more information. | Human Observation |
| @Resource type general 	| Select one of the following options: Audiovisual, ComputationalNotebook, Dataset, Image, Software, Sound, Text, Other. Default is **Dataset**. | Dataset |
| Language			| The Language of the (primary) data. | en 	|
| Version 			| Will be set automatically. 	| 2		|

### 3.1.2 Creators

Creators are the main researchers involved working on the data in priority order. All creators are owners of the dataset and have **write permission**. 
The form is repeatable, i.e. you can enter as many creators (e.g. PhDs, PIs) as appropriate.

**!!! Due to software issues, please fill the field "Name identifier scheme" (= ORCID) first !!!**


| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Creator name			| Use an entry from autocomplete list. Fill in the first letter of the last name of the creator | Kümmet, Sonja |
| Given name			| Will be set automatically. 	| Sonja 	|
| Family name			| Will be set automatically.	| Kümmet	|
| Name identifier		| Will be set automatically. An unique identifier for the person. Default is ORCID. | 0000-0002-8954-0200 |
| @Name identifier scheme       | The name of the identifier scheme. Default is **ORCID** | ORCID |
| Affiliation 			| Will be set automatically. Format: University, Institute (e.g. University of Würzburg, Zoology III), or Institution (e.g. Nationalpark Bayerischer Wald)	| University of Würzburg, Zoology III |

### 3.1.3 Titles 

The title field is repeatable. 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Title 			| Format: **Project_Subproject_Organism_Method/Device_Year**; For depicting time ranges, use the following syntax: YYYY/YYYY, e.g. 2022/2023. | BETA-FOR_SP9_Bat_BatRecorder_2022, BETA-FOR_SPZ_Temperature_Tomst_2022/2023 |
| @Title type			| Leave the field empty if you have only one (main) title. | |

### 3.1.3 Subjects

The subject field is repeatable. 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Subject			| You can provide the **scientific name of an organism** here. Ideally, the name supplied is at species level or below. If the determination only allows for information on a higher level, this is acceptable as well. Valid scientific names are Latin names following the syntax rules of the respective taxon group (e.g. botanical nomenclature). | Parus major |

### 3.1.4 Contributors

Persons responsible for collecting, creating or otherwise contributing to the development of the dataset. All contributors have **read permission** on the dataset. 
The form is repeatable, i.e. you can enter as many contributors (e.g. Studentische Hilfskräfte) as appropriate.

**!!! Due to software issues, please fill the field "Name identifier scheme" (= ORCID) first !!!**

| Element / @Attribute Name       | How to fill it		    | Example 	    |
|-------------------------------|-------------------------------|---------------|
| Contributor name		| Use an entry from autocomplete list. Fill in the first letter of the last name of the creator | Kümmet, Sonja |
| Given name			| Will be set automatically. 	| Sonja 	|
| Family name			| Will be set automatically.	| Kümmet	|
| Name identifier		| Will be set automatically. An unique identifier for the person. Default is ORCID. | 0000-0002-8954-0200 |
| @Name identifier scheme       | The name of the identifier scheme. Default is **ORCID** | ORCID |
| Affiliation 			| Will be set automatically. Format: University, Institute (e.g. University of Würzburg, Zoology III), or Institution (e.g. Nationalpark Bayerischer Wald)	| University of Würzburg, Zoology III |

### 3.1.5 Dates 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Date				| Will be set automatically. Date, when the dataset was created. | 2023-06-12 |
| @Date type			| Select **Created**            | Created	|


### 3.1.6 Alternate Identifiers

The element *Alternate Identifiers* should be used in cases of large raw data, that cannot be stored directly in BEXIS2. 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Alternate identifier		| Enter the storage location of the (large raw) data here. | |
| @Alternate Identifier		| Fill in **External storage location**	| External storage location |

### 3.1.7 Related Identifiers

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Related identifier		| 				|		|


### 3.1.8 Formats

### 3.1.9 Rights List

Choose a ![Creative Commons](https://creativecommons.org/licenses/?lang=de) licence under which your dataset should be available after publication. If you want to use a licence that is not yet in the selection list, write an email to your data manager (betafor@uni-wuerzburg.de).


| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Rights			| **!!! Leave this field empty !!!** | --- 	|
| @Rights identifier		| Select a Licence. Default is **CC BY-NC-SA**. | CC BY-NC-SA |

### 3.1.10 Descriptions

### 3.1.11 Funding References 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Funder name 	
| 				|		|
### 3.1.12 Related Items



On the bottom of the page, there is a button titled Validate to examine whether required attributes have been filled and values fit to the expected data format. 

You could edit a submitted dataset or make a copy of that by clicking on the Edit or Copy buttons.

When an input is wrong or missing, the input field is highlighted in red. 

#### 1.2 Dataset links
It is possible to create relations between different datasets of one type or different types of datasets (e.g. dataset and publication). Links always refer to a specific version of a dataset. Dataset links are shown under *Links* and divided into *Links to* the dataset and *Links from* the dataset. This shows the direction of the link and clearly defines what is source and target, which might be relevant related to the type of the selected reference (e.g. parent, child ...). 

There are two options to create relations / links between datasets:

##### Link via Metadata
Fields in the metadata form can contain lists of datasets stored within the system. If one is selected also a link in both directions based on the most current versions is created.

##### Direct links
Links can also be created directly under *Link > Create link*. Here you can also choose  which version you like to refer to and what kind of link it is. In addition, you can also give more details to it.

![Create links](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/create_links.png) 

### 2 Upload data

To upload your data, please go to the *Collect > Upload Data* via main menu. This wizard will assist you in uploading data into the BEXIS2 repository. A dataset can be structured or unstructured (i.e tabular or file).

![Upload Data](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/upload_data.png) 

#### 2.1. Upload Tabular Data

The term "Tabular data" is used for all datasets where there internal structure of the data is "known" to the system. For example, in a data table the header, which defines the columns (i.e. variables) is the structure of the data. Before uploading/importing data to the system the data structure needs to be created through the Data Structure Manager.

Uploading a tabular data follows the following steps.

##### Select File

In the first step an existing file containing your data needs to be selected. You can either select a file from your local computer or a file that has been uploaded to the server prior to starting the Upload Wizard. The second option is designed for files larger than 4 MB that may take several minutes to transfer. The wizard supports file formats of Microsoft Excel or ASCII. Microsoft Excel files are required to use a template created while creating a Data Structure (refer to [Data Planning User Guide](~/rpm/Help/index#_overview) for more details). Once a file has been successfully selected, click the Next button and proceed to the next step.

![Upload_Tabular](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/upload_tabular.jpg) 

##### Get File Information

For all Microsoft Excel files using a BEXIS2 template the file information and data structure is automatically extracted and this step is omitted. Please refer to the [Data Planning User Guide](~/rpm/Help/index#_overview) for more details on how to create such a template.

For all other Excel files, users need to provide the information by selection the data on the screen.

![Upload_Tabular](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/GetFileInformations.png) 

For all ASCII files users need to provide information on the file structure and formatting.

First, please choose a separator that is being used to separate data values from each other in your ASCII file.

Depending on your language different punctuation is used for decimal values. Please choose the one present in your ASCII file.

Next please specify whether the orientation of your data is column-wise or row-wise (see figure below).

Datasets may contain empty rows or columns on top or to the left before the header and the actual data values start. Please specify this offset in number of columns or rows. 

Further, your data file may contain a header defining variable names, types etc. The row/column where this header starts needs to be specified (see figure below).

![Offset.JPG](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/columnwise.jpg)![Variables.JPG](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/rowwise.jpg) 

Finally, the row/column where the actual data values start needs to be specified.

##### Specify Dataset

In BEXIS2 your data is stored and managed as part of a dataset. A dataset may contain one or more of your data files. But all data files within one dataset must be of the same data structure, i.e. the number of variables and their properties must be identical in each file. To upload your data to the system, please select one existing dataset from the dropdown list.

##### Choose Update Method

While adding data to an existing dataset you need to specify how you want to update.

By Update the user need to specify a unique identifier (e.g. primary key) for each tuple (i.e. row) in your dataset. If your dataset already contains a variable with such a key, please select it. Otherwise, a primary key can be created by combining available variables. Please click the Check button to verify whether the selected combination is unique. If you go back and change something in the process of uploading, you need to check the primary key again.

![Choose Update Method](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/ChooseUpdateMethod.png) 

By Append, the lines are uploaded directly to the data without checking for duplication.

##### Validation

With this step, the selected data file is validated against the selected data structure. Both, the structure of the data (e.g. variable properties) and whether the data values fit to the specified structure (e.g. data type, value range) is evaluated.

Click on Validate button to validate the data file.

If you go back and change something in the process of uploading, you need to validate the file again.

##### Summary

With this final step a summary of your uploaded data file is provided. Please check the information and click the Finish button to confirm and finalize the upload.

#### 2.2 Upload File

An unstructured data could be either selected from your local computer or could be a file that has been uploaded to the server. In the case of unstructured data, we do not read the contents of the data. We copy the files to the server and place them in relation to the dataset.

BEXIS2 application can support many file formats which are referred on the relevant page.

The Maximum acceptable file size up to now is: 1024 MB.

![Select File](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/select_file.png)

### 3 Import Data

The Import Data wizard enables you to import both a tabular data structure and data in a single workflow. Import a file follows the following steps.

#### 3.1 Select File

In the first step an existing file containing both your data and the names of the variables needs to be selected. You can either select a file from your local computer or a file that has been uploaded to the server prior to starting the Upload Wizard. The second option is designed for files larger than 4 MB that may take several minutes to transfer. The wizard supports file formats of Microsoft Excel (*.xlsm, *.xlsx). Once a file has been successfully selected, click the Next button to proceed to the next step.

![Select File](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/Help_easy_upload_select_file.png)

#### 3.2 Metadata

This step allows you to select the metadata schema that you would like to use for the dataset. There is no need to enter any metadata yet - after the last step you will be redirected to a page that allows you to enter the metadata. You can, however, change the title of the dataset. If you don't wish to change it, it will default to the name of the file you are using. Once you have selected a schema, click the Next button to proceed to the next step.

![Metadata Schema](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/Help_easy_upload_metadata.png)

#### 3.3 Select Areas

You will see a table that represents the file that you selected during the first step. Here you can select, which part of the file should be used as variables and which parts should be interpreted as data.

For the variables, select a row or one part of a row and click the "Header" button. The selected area should now be highlighted in red. If you are using a BEXIS2 template file there is no need to select the whole header with unit, datatype, etc. Just select the names of the variables.

For the data, you can select multiple rows and click the "Data" button. The selected area should now be highlighted in blue. Please make sure that the data area contains as many columns as the header area. You can skip one or more rows by selecting the area above them, mark it as data, and then select the area below them and mark it as well. You can use the "Expand Selection" button to expand the last data area you selected to the last row of the file. This can be very helpful when working with large datasets.

If you made any mistakes during the selection process just use the "Reset" button to remove all markings and start over.

If you wish to upload data from a different worksheet you can select it from the dropdown-menu and click the "Change Worksheet" button. Please be aware that you can only upload data from one sheet at a time. Once you have selected the header and at least one data area, click the Next Button to proceed to the next step.

![Select Areas](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/Help_easy_upload_select_areas.png)

The representation of the data you will see in the table might differ from what you see in Microsoft Excel or similar programs.

Don't worry, your data will be uploaded correctly if you choose the correct datatypes during the next step.

The following differences are known:

*   Dates and times

*   Microsoft Excel users: Dates and times will be displayed as full timestamps, containing both a time and a date.
*   Libre Office users: Dates and times will be displayed as real numbers.

*   Boolean values

*   Libre Office users: Boolean values might be displayed as "0" and "1".

*   Real Numbers

*   Real numbers might be displayed with scientific notation.

#### 3.4 Verification

With this step you can define which units and datatypes your variables are using. The first column of dropdown-menus provides suggestions for attributes that are being used in other datasets and are similar to your variables. If you select one of the suggestions, unit and datatype are automatically adjusted. If you don't wish to use the suggestions, feel free to choose unit and datatype yourself.

The "Validate" button allows you to check if the datatypes you selected are suitable for the data you selected in the previous step. This allows you to recognize errors early and correct your selection. Once you've selected your units and datatypes, click the Next button to proceed.

![Verification](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/Help_easy_upload_verification.png)

#### 3.5 Summary

The summary step provides an overview of the dataset that is about to be created. When you click the Finish button, datastructure and dataset will be created and the data will be added. This might take a while, depending of the size of your file.

![Upload_Tabular_1](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/Help_easy_upload_summary.png)

As soon as this process is finished, you will be redirected to your new dataset and can add metadata, view primary data and datastructure, set permissions or publish the dataset.

## 4 Push Big File

Each user has a personal folder on the server where files are stored temporary. On this page you can see the uploaded files. You can delete each file by clicking on the X, or use these files later, when you want to upload data to a dataset.

![Push Big File](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/push_big_file.png)








[Go to top](#_overview)

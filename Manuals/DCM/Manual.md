# Data Collection: Metadata and Data


<!-- TOC -->

- [Data Collection: Metadata and Data](#data-collection-metadata-and-data)
	- [1 Overview](#1-overview)
	- [2 Create a Dataset](#2-create-a-dataset)
	- [3 Provide some Metadata](#3-provide-some-metadata)
		- [3.1 General Information](#31-general-information)
		- [3.2 Basic](#32-basic)
		- [3.3 Creators](33-creators)
		- [3.4 Titles](34-titles)
		- [3.5 Subjects](35-subjects)
		- [3.6 Contributors](36-contributors)
		- [3.7 Dates](37-dates)
		- [3.8 Alternate Identifiers](38-alternate-identifiers)
		- [3.9 Related Identifiers](39-related-identifiers)
		- [3.10 Formats](310-formats)
		- [3.11 Rights List](311-rights-list)
		- [3.12 Descriptions](312-descriptions)
		- [3.13 Funding References](313-funding-references)
		- [3.14 Related Items](314-related-items)
	- [4 Upload data](#4-upload-data)
		- [4.1 Upload File](#41-upload-file)
		- [4.2 Push Big File](#42-push-big-file)
		- [4.3 Upload Tabular Data](#43-upload-tabular-data)
			- [Select File](#select-file)
			- [Get File Information](#get-file-information)
			- [Specify Dataset](#specify-dataset)
			- [Choose Update Method](#choose-update-method)
			- [Validation](#validation)
			- [Summary](#summary)
	
	

<!-- /TOC -->

## 1 Overview

In BEXIS2, data is stored and managed as part of a dataset. You can think of a Dataset as a container for the (primary) data on the one hand, and the metadata on the other.

![grafik](https://user-images.githubusercontent.com/68608907/233026141-c3e39d31-be31-46c5-924b-18d11406d5d7.png)

* **Metadata**: describing facts about the dataset, e.g. who created the dataset and when
* **(Primary) Data**: can be files or tabular data
* **File**: unstructured data, e.g. an audio file or image
* **Tabular Data**: structured data; supported formats are Excel and ASCII
* **Data Structure**: describes the structure of the data

You can upload a file or tabular data to the system in three steps:
1. [Create a Dataset](#2-create-a-dataset) as Container for your data
2. [Describe your data](#3-provide-some-metadata) by filling in the Metadata form
3. [Upload your data](#4-upload-data)


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

At the bottom of the page there is a button titled Validate, which can be used to check whether the required attributes have been filled in and the inputs match the expected data format. 

You can edit a submitted dataset or make a copy of that by clicking the Edit or Copy buttons.

If an input is wrong or missing, the corresponding field is highlighted in red. 

### 3.2 Basic

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Identifier			| Will be set automatically.	| 1		|
| @Identifier type		| Will be set by the data manager.	| DOI	|
| Publisher			| Use an entry from autocomplete list. Fill in the first letter of the publisher. Default is **University of Würzburg**.				| University of Würzburg |
| Publication Year 		| Enter the year, when you plan to publish the dataset, or leave the field empty. Format: YYYY .| 2025
| Resource Type 		| There are 3 options: **Human Observation**, **Machine Observation** and **Material Citation**. Check the info button for more information. | Human Observation |
| @Resource type general 	| Select one of the following options: Audiovisual, ComputationalNotebook, Dataset, Image, Software, Sound, Text, Other. Default is **Dataset**. | Dataset |
| Language			| The Language of the (primary) data. | en 	|
| Version 			| Will be set automatically. 	| 2		|

### 3.3 Creators

Creators are the main researchers involved working on the data in priority order. All creators are owners of the dataset and have **write permission**. 
The form is repeatable, i.e. you can enter as many creators (e.g. PhDs, PIs) as appropriate.

**!!! Due to software issues, please fill the field "@Name identifier scheme" (= ORCID) first !!!**


| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Creator name			| Use an entry from autocomplete list. Fill in the first letter of the last name of the creator. | Kümmet, Sonja |
| Given name			| Will be set automatically. 	| Sonja 	|
| Family name			| Will be set automatically.	| Kümmet	|
| Name identifier		| Will be set automatically. An unique identifier for the person. Default is an ORCID ID. | 0000-0002-8954-0200 |
| @Name identifier scheme       | The name of the identifier scheme. Default is **ORCID** | ORCID |
| Affiliation 			| Will be set automatically. Format: University, Institute (e.g. University of Würzburg, Zoology III), or Institution (e.g. Nationalpark Bayerischer Wald).	| University of Würzburg, Zoology III |

### 3.4 Titles 

The title field is repeatable. 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Title 			| Format: **Project_Subproject_Organism_Method/Device_Year**; For depicting time ranges, use the following syntax: YYYY/YYYY, e.g. 2021/2023. | BETA-FOR_SP9_Bat_BatRecorder_2022, BETA-FOR_SPZ_Temperature_Tomst_2022/2023 |
| @Title type			| Leave the field empty if there is only one (main) title. | |

### 3.5 Subjects

The subject field is repeatable. 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Subject			| You can provide the **scientific name of an organism** here. Ideally, the name supplied is at species level or below. If the determination only allows for information on a higher level, this is acceptable as well. Valid scientific names are Latin names following the syntax rules of the respective taxon group (e.g. botanical nomenclature). | Parus major |

### 3.6 Contributors

Persons responsible for collecting, creating or otherwise contributing to the development of the dataset. All contributors have **read permission** on the dataset. 
The form is repeatable, i.e. you can enter as many contributors (e.g. Studentische Hilfskräfte) as appropriate.

**!!! Due to software issues, please fill the field "@Name identifier scheme" (= ORCID) first !!!**

| Element / @Attribute Name       | How to fill it		    | Example 	    |
|-------------------------------|-------------------------------|---------------|
| Contributor name		| Use an entry from autocomplete list. Fill in the first letter of the last name of the creator. | Kümmet, Sonja |
| Given name			| Will be set automatically. 	| Sonja 	|
| Family name			| Will be set automatically.	| Kümmet	|
| Name identifier		| Will be set automatically. An unique identifier for the person. Default is an ORCID ID. | 0000-0002-8954-0200 |
| @Name identifier scheme       | The name of the identifier scheme. Default is **ORCID** | ORCID |
| Affiliation 			| Will be set automatically. Format: University, Institute (e.g. University of Würzburg, Zoology III), or Institution (e.g. Nationalpark Bayerischer Wald).	| University of Würzburg, Zoology III |

### 3.7 Dates 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Date				| Will be set automatically. Date, when the dataset was created. | 2023-06-12 |
| @Date type			| Select **Created**            | Created	|


### 3.8 Alternate Identifiers

The element *Alternate Identifiers* should be used in cases of large raw data, that cannot be stored directly in BEXIS2. 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Alternate identifier		| Enter the storage location of the (large raw) data here. | |
| @Alternate Identifier		| Fill in **External storage location**.	| External storage location |

### 3.9 Related Identifiers

The field *Related Identifiers* should be used if there are related datasets INSIDE BEXIS2. If you want to state a relationship to an EXTERNAL publication, use the *Related Items* field. 

Note: If you enter the field *Related Identifier*, a link is created in both directions, based on the current versions of the datasets.

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Related identifier		| Use an entry from autocomplete list. Fill in the name of the related dataset. | BETA-FOR_SPZ_Temperature_Tomst_2022/2023 |
| @Related identifier type 	| Default is **URL**. 		| URL		|
| @Related type			| Specifiy the type of relationship. The current dataset is the source, the related dataset the target. Example: If you want to specify the relationship to a dataset (B) from which the current dataset (A) was compiled, use (A) *Compiles* (B). For more information about the different relation types, visit: https://github.com/UB-LMU/DataCite_BestPracticeGuide/blob/4.4/bestpractice.md#relationtypes | Compiles |

### 3.10 Formats

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Format			| Use ![iana media types](https://www.iana.org/assignments/media-types/media-types.xhtml) for specifying the technical format of the (primary) data. | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |

Some common formats: 

| File extension| iana media type |
|---------------|-----------------|
| .xlsx		| application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| .xls		| application/vnd.ms-excel |
| .csv		| text/csv |
| .jpg		| image/jpg |
| .png		| image/png |
| .txt		| text/plain |

### 3.11 Rights List

Choose a ![Creative Commons](https://creativecommons.org/licenses/?lang=de) licence under which your dataset should be available after publication. If you want to use a licence that is not yet in the selection list, write an email to your data manager (betafor@uni-wuerzburg.de).

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Rights			| **!!! Leave this field empty !!!** | --- 	|
| @Rights identifier		| Select a Licence. Default is **CC BY-NC-SA**. | CC BY-NC-SA |

### 3.12 Descriptions

The field *Description* is repeatable. Please provide at least an **Abstract** (@DescriptionType="Abstract") and some information about the underlying **Methods** (@DescriptionType="Methods"). 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Description			| Enter some free text information. | This is my Abstract... (= Description Field No. 1) / These are my Methods... (= Description Field No. 2).|
| @Description type		| Select **Abstract** for your abstract and **Methods** for your description of your methods. | Abstract / Methods |

### 3.13 Funding References 

**!!! Due to software issues, please select the "@Funder identifier type" (= ROR) first !!!**

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Funder name 			| Will be set automatically. The name of the project funder. | Deutsche Forschungsgemeinschaft (DFG) |			
| Funder identifier		| Will be set automatically. An unique identifier for the funder. | https://ror.org/018mejw64 |
| @Funder identifier type 	| Select **ROR**. A scheme for identifying organizations. | ROR |
| Award number			| Will be set automatically. The number of the grant. | 459717468 |
| Award URI			| Will be set automatically. The URI of the grant. | https://gepris.dfg.de/gepris/projekt/459717468 |
| Award title 			| Use an entry from autocomplete list. Fill in the first letter(s) of the project name. | BETA-FOR: Enhancing the structural diversity between patches for improving multidiversity and multifunctionality in production forests. | 

### 3.14 Related Items

If your data has been published in a journal, you can share this information by entering the following fields:

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Related item identifier 	| The identifer of the publication. | https://doi.org/10.3897/BDJ.9e77092 |
| @Related item identifier type	| The type of identifier.	| DOI		|
| Publication year		| Format: YYYY			| 2021		|
| Volume			|				| 9		|
| Issue				|				| 		|
| First page			|				|		|
| Last page			|				|		|
| Journal publisher		| The publisher of the journal.	| Pensoft	|
| Journal title 		| The title of the journal (NOT the data). | Biodiversity Data Journal		|
| @Title type			|				|		|


## 4 Upload data

In BEXIS2, you can only upload your (primary) data as part of a dataset. If you have not created a dataset yet, [do it now](#2-create-a-dataset). 

There are 2 ways to upload (primary) data:

* Click the **Primary Data** tab in the dataset details view.
* Select **Upload Data** in the Collect menu.

In the next step you have to specify whether your (primary) data is structured (tabular data) or unstructured (file).

![Upload Data](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/upload_data.png)

### 4.1 Upload File 

Select a file from your local computer or pick a file that has already been uploaded to the server.

BEXIS2 supports the following file formats:

![Select File](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/select_file.png)

Note, that the maximum supported file size is: **1024 MB**. If your file is larger than that, store it at ... and refer to the external storage location in the metadata / ![Alternate identifiers](38-alternate-identifiers). 

If your file is larger than 4 MB, use the ![*Push Big File*](#42-push-big-file) function.

### 4.2 Push Big File

If you have a large file (> 4 MB), upload it to the server first. For this case, every user has a personal folder where files can be stored temporarily. 
Files that are stored here, can be selected via the ![upload wizard](#4-upload-data) and loaded into the BEXIS2 environment.

![Push Big File](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/push_big_file.png)

### 4.3. Upload Tabular Data

Note: Tabular data can only be uploaded to the system if there is a corresponding Data Structure which defines its variables. If you have not created a Data Structure for your (tabular) data yet, do it now (check the "Create a Data Structure"-Manual).


#### Select File

In the first step an existing file containing your data needs to be selected. You can either select a file from your local computer or a file that has been uploaded to the server prior to starting the Upload Wizard. The second option is designed for files larger than 4 MB that may take several minutes to transfer. The wizard supports file formats of Microsoft Excel or ASCII. Microsoft Excel files are required to use a template created while creating a Data Structure (refer to [Data Planning User Guide](~/rpm/Help/index#_overview) for more details). Once a file has been successfully selected, click the Next button and proceed to the next step.

![Upload_Tabular](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/upload_tabular.jpg) 

#### Get File Information

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

#### Specify Dataset

In BEXIS2 your data is stored and managed as part of a dataset. A dataset may contain one or more of your data files. But all data files within one dataset must be of the same data structure, i.e. the number of variables and their properties must be identical in each file. To upload your data to the system, please select one existing dataset from the dropdown list.

#### Choose Update Method

While adding data to an existing dataset you need to specify how you want to update.

By Update the user need to specify a unique identifier (e.g. primary key) for each tuple (i.e. row) in your dataset. If your dataset already contains a variable with such a key, please select it. Otherwise, a primary key can be created by combining available variables. Please click the Check button to verify whether the selected combination is unique. If you go back and change something in the process of uploading, you need to check the primary key again.

![Choose Update Method](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/ChooseUpdateMethod.png) 

By Append, the lines are uploaded directly to the data without checking for duplication.

#### Validation

With this step, the selected data file is validated against the selected data structure. Both, the structure of the data (e.g. variable properties) and whether the data values fit to the specified structure (e.g. data type, value range) is evaluated.

Click on Validate button to validate the data file.

If you go back and change something in the process of uploading, you need to validate the file again.

#### Summary

With this final step a summary of your uploaded data file is provided. Please check the information and click the Finish button to confirm and finalize the upload.












[Go to top](#_overview)

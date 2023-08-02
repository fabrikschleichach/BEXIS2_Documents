# Upload Data


<!-- TOC -->

- [1 Overview](#1-overview)
- [2 Create a Dataset](#2-create-a-dataset)
- [3 Provide some Metadata](#3-provide-some-metadata)
	- [3.1 General Information](#31-general-information)
	- [3.2 Basic](#32-basic)
	- [3.3 Creators](#33-creators)
	- [3.4 Titles](#34-titles)
	- [3.5 Subjects](#35-subjects)
	- [3.6 Contributors](#36-contributors)
	- [3.7 Dates](#37-dates)
	- [3.8 Alternate Identifiers](#38-alternate-identifiers)
	- [3.9 Related Identifiers](#39-related-identifiers)
	- [3.10 Formats](#310-formats)
	- [3.11 Rights List](#311-rights-list)
	- [3.12 Descriptions](#312-descriptions)
	- [3.13 GeoLocations](#313-geolocations)
	- [3.14 Funding References](#314-funding-references)
	- [3.15 Related Items](#315-related-items)
- [4 Upload data](#4-upload-data)
	- [4.1 Upload File](#41-upload-file)
	- [4.2 Push Big File](#42-push-big-file)
	- [4.3 Upload Tabular Data](#43-upload-tabular-data)
		- [4.3.1 Select File](#431-select-file)
		- [4.3.2 Get File Information](#432-get-file-information)
		- [4.3.3 Specify Dataset](#433-specify-dataset)
		- [4.3.4 Validation](#434-validation)
		- [4.3.5 Summary](#435-summary)	

<!-- /TOC -->

## 1 Overview

In BEXIS2, data is stored and managed as part of a **Dataset**. You can think of a Dataset as a container for the (primary) data on the one hand, and the metadata on the other.

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

Select the _Collect_ menu and click on _Create Dataset_.

![Create_Dataset_Button](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Create_Dataset_Button.PNG)

You can either create a new Dataset or select an existing one to copy its metadata.  

![New_Dataset](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/New_Dataset.PNG)

Select a Data Structure that fits to your data.

Note: Tabular data can only be uploaded to the system if there is a corresponding Data Structure which defines its variables. If you have not created a Data Structure for your data yet, do it ![now](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Manual.md#21-create-a-data-structure).

Finally, select DataCite_bexis as Metadata Structure and click the _Next_ button.

![Choose_Data_Structure](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Choose_Data_Structure.png)


## 3 Provide some Metadata

![Metadata](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Metadata.PNG)

### 3.1 General Information

**DataCite_bexis** is a DataCite profile. For more information about the DataCite metadata scheme, visit: https://schema.datacite.org/meta/kernel-4.4/.

The metadata form contains different icons. Here is an explanation:

![Required](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/red_star.png)           Required attributes

![Add](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/plus.png)        Add an attribute

![Mines](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/mines.png)        Remove an attribute

![Up Down](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/up_down.png)  Change order of the attribute

![Expand](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/expand.png)![Collapse](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/collapse.png)      Expand / collapse

![Help](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/help.png)   	Show help information. The button on the right top hides / shows all help information. 

Some fields, e.g. *Identifier*, cannot be selected because they are set automatically by the system.
Other fields, e.g. *Publisher*, have a note: “If possible, use an entry from autocomplete list.”. In this case, you may only enter the first letter of the item and the system will automatically complete it.

At the bottom of the page there is a button titled _Validate_, which can be used to check whether the required attributes have been filled in and the inputs match the expected data format. 

You can edit a submitted dataset or make a copy of that by clicking the _Edit_ or _Copy_ buttons.

If an input is wrong or missing, the corresponding field is highlighted in red. 

There are a few 🔴**Mandatory fields**, that must be filled out. The others are 🟣strongly recommended. Provide at least as much information as you would need to be able to classify the data without further contextual information.

### 3.2 Basic

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Identifier			| Will be set automatically.	| 1		|
| @Identifier type		| Will be set by the data manager.	| DOI	|
| 🔴**Publisher**		| Default is **University of Würzburg**.				| University of Würzburg |
| 🟣Publication Year 		| Enter the year, when you plan to publish the dataset, or leave the field empty. Format: YYYY .| 2025
| 🔴**Resource Type** 		| Select a ![Darwin Core class label](https://docs.gbif.org/course-data-use/en/basis-of-record.html) as *Basis of Record*. | Human Observation |
| 🟣@Resource type general 	| Select one of the following options: Audiovisual, ComputationalNotebook, Dataset, Image, Software, Sound, Text, Other. Default is **Dataset**. | Dataset |
| 🟣Language			| The Language of the (primary) data. | en 	|
| Version 			| Will be set automatically. 	| 2		|

### 3.3 Creators

Creators are the main researchers involved working on the data in priority order. All creators are owners of the dataset and have **write permission**. 
The form is repeatable, i.e. you can enter as many creators (e.g. PhDs, PIs) as appropriate.

**!!! Due to software issues, please enter the field "@Name identifier scheme" (= ORCID) first !!!**


| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🔴**Creator name**		| Use an entry from autocomplete list. Fill in the first letter of the last name of the creator. (Note: Only persons with a BEXIS account can be selected via autocomplete).  | Kümmet, Sonja |
| Given name			| Will be set automatically. 	| Sonja 	|
| Family name			| Will be set automatically.	| Kümmet	|
| Name identifier		| Will be set automatically. An unique identifier for the person. Default is an ORCID ID. | 0000-0002-8954-0200 |
| 🟣@Name identifier scheme       | The name of the identifier scheme. Default is **ORCID** | ORCID |
| Affiliation 			| Will be set automatically. Format: University, Institute (e.g. University of Würzburg, Zoology III), or Institution (e.g. Nationalpark Bayerischer Wald).	| University of Würzburg, Zoology III |

### 3.4 Titles 

The title field is repeatable. 

To make sure that same things have same naming, pick the Method/Device name from ![here](https://docs.google.com/document/d/1DKHSOQrK5LqxLlfZqJu-fhkgmu5ahpPzNj9slEb2f24/edit?usp=sharing). The bold one is the preferred name. 
If your Method/Device is missing, add it to the list to make sure that others will reuse the term you picked. 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🔴**Title** 			| Format: **Project_Subproject_Organism/Function_Method/Device_Year**; For depicting time ranges, use the following syntax: YYYY/YYYY, e.g. 2021/2023. | BETA-FOR_SP9_Bat_BatRecorder_2022, BETA-FOR_SPZ_Temperature_Tomst_2022/2023 |
| @Title type			| Leave the field empty if there is only one (main) title. | |


### 3.5 Subjects

The subject field is repeatable. 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🟣Subject			| Select one or more Taxonomic Term(s).| Aves	|

### 3.6 Contributors

Persons responsible for collecting, creating or otherwise contributing to the development of the dataset. All contributors have **read permission** on the dataset. 
The form is repeatable, i.e. you can enter as many contributors (e.g. Site Manager, TAs, Studentische Hilfskräfte, Praktiker, ...) as appropriate.

**!!! Due to software issues, please enter the field "@Name identifier scheme" (= ORCID) first !!!**

| Element / @Attribute Name     | How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🟣Contributor name		| Use an entry from autocomplete list. Fill in the first letter of the last name of the creator. (Note: Only persons with a BEXIS account can be selected via autocomplete). | Kümmet, Sonja |
| Given name			| Will be set automatically. 	| Sonja 	|
| Family name			| Will be set automatically.	| Kümmet	|
| Name identifier		| Will be set automatically. An unique identifier for the person. Default is an ORCID ID. | 0000-0002-8954-0200 |
| 🟣@Name identifier scheme       | The name of the identifier scheme. Default is **ORCID** | ORCID |
| Affiliation 			| Will be set automatically. Format: University, Institute (e.g. University of Würzburg, Zoology III), or Institution (e.g. Nationalpark Bayerischer Wald).	| University of Würzburg, Zoology III |

### 3.7 Dates 

Important dates related to the (primary) data.

**Collected**: When was the (primary) data collected in the field?

**Created**: When was the (tabular) data created? 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🟣Date				| Date or date range. Use one of the following formats: YYYY, YYYY-MM-DD, YYYY-MM-DDThh:mm:ssTZD. Date ranges should be formatted like this: 2023-07-01/2023-07-31.  | 2023-06-12 |
| 🟣@Date type			| Select a date type from the drop-down list.   | Collected 	|


### 3.8 Alternate Identifiers

There are two different use cases for the element *Alternate Identifiers*:

1) Use the element *Alternate Identifiers* if your (primary) data is stored outside BEXIS (**NAS**, in case of large raw data; **Archivserver**).
   
| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🟣Alternate identifier		| Enter the storage location of the (primary) data here. | |
| 🟣@Alternate Identifier Type	| Fill in **External storage location**.	| External storage location |

2) Use the element *Alternate Identifiers* if your dataset has a **DOI**.

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🟣Alternate identifier	| Enter the DOI here. 		| 10.58160/88 	|
| 🟣@Alternate Identifier Type	| Fill in **DOI**.	| DOI |
   

### 3.9 Related Identifiers

The field *Related Identifiers* should be used if there are related datasets INSIDE BEXIS2. If you want to state a relationship to an EXTERNAL publication, use the *Related Items* field. 

To refer to the geographic information dataset (Title: BETA-FOR_SPZ_Patches_2022/2023; Dataset id: 9) use **IsSupplementedyBy** as @relationType.

Note: If you enter the field *Related Identifier*, a link is created in both directions, based on the current versions of the datasets.

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🟣Related identifier		| Use an entry from autocomplete list. Fill in the name of the related dataset. | BETA-FOR_SPZ_Patches_2022/2023 |
| 🟣@Related identifier type 	| Default is **URL**. 		| URL		|
| 🟣@Relation type			| Specifiy the type of relationship. The current dataset is the source, the related dataset the target. Example: If you want to specify the relationship to a dataset (B) from which the current dataset (A) was compiled, use (A) *Compiles* (B). For more information about the different relation types, visit: https://github.com/UB-LMU/DataCite_BestPracticeGuide/blob/4.4/bestpractice.md#relationtypes | IsSupplementedBy |

### 3.10 Formats

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🟣Format			| The file extension of your (primary) data. Select an entry from the drop-down list. | XLSX |


### 3.11 Rights List

Choose a ![Creative Commons](https://creativecommons.org/licenses/?lang=en) licence under which your dataset should be available after publication. If you want to use a licence that is not yet in the selection list, write an email to your data manager (betafor@uni-wuerzburg.de).

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Rights			| **!!! Leave this field empty !!!** | --- 	|
| 🟣@Rights identifier		| Select a Licence. Default is **CC BY-NC-SA**. | CC BY-NC-SA |


Here some information about the different Creative Commons licenses taken from the ![Creative Commons](https://creativecommons.org/licenses/?lang=en) website. 

| Licence	| Content			| Description   |
|---------------|-------------------------------|---------------|
| CC0		| No Rights Reserved		| This "license" allows licensors to waive all rights and place a work in the public domain. |
| CC BY		| Attribution   		| This license lets others distribute, remix, adapt, and build upon your work, even commercially, as long as they credit you for the original creation. |
| CC BY-SA	| Attribution-ShareAlike 	| This license lets others remix, adapt, and build upon your work even for commercial purposes, as long as they credit you and license their new creations under the identical terms. |
| CC BY-ND	| Attribution-NoDerivs		| This license lets others reuse the work for any purpose, including commercially; however, it cannot be shared with others in adapted form, and credit must be provided to you. |
| CC BY-NC	| Attribution-NonCommercial	| This license lets others remix, adapt, and build upon your work non-commercially, and although their new works must also acknowledge you and be non-commercial, they don’t have to license their derivative works on the same terms. |
| CC BY-NC-SA  	| Attribution-NonCommercial-ShareAlike 	| This license lets others remix, adapt, and build upon your work non-commercially, as long as they credit you and license their new creations under the identical terms.  |
| CC BY-NC-ND  	| Attribution-NonCommercial-NoDerivs  	| This license is the most restrictive of the six main licenses, only allowing others to download your works and share them with others as long as they credit you, but they can’t change them in any way or use them commercially. |


### 3.12 Descriptions

The field *Description* is repeatable. Please provide at least an **Abstract** (@DescriptionType="Abstract") and some information about the underlying **Methods** (@DescriptionType="Methods"). 

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🟣Description			| Enter some free text information. | This is my Abstract... (= Description Field No. 1) / These are my Methods... (= Description Field No. 2).|
| 🟣@Description type		| Select **Abstract** for your abstract and **Methods** for your description of your methods. | Abstract / Methods |


### 3.13 GeoLocations

The field *GeoLocation* is repeatable. Provide a spatial region or named place where the data was gathered or about which the data is focused.

There are 2 different options to provide geographic information:

* Geo Location **Place**: A name of a location.
* Geo Location **Point**: A single longitude-latitude pair.

You can select one option or combine them, e.g. provide a Place AND a Point. 

If your data covers all or a whole range of BETA-FOR patches, you can either enter some information on a higher level (e.g. GeoLocationPlace = Germany) or skip this field and ![refer to the geographic information dataset](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Manual.md#39-related-identifiers).

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| 🟣GeoLocationPlace		| Enter a location. Best practice is to use a term from a controlled vocabulary like ![GeoNames](https://www.geonames.org/). | Bavarian Forest |
| 🟣Geo Location Point / Point longitude | Enter the longitude in decimal degrees (-180 <= longitude <= 180). | 10.45047 |
| 🟣Geo Location Point / Point latitude | Enter the latitude in decimal degrees (-90 <= latitude <= 90). | 50.05453 |



### 3.14 Funding References 

The field *Funding Reference* is repeatable. Please enter both the **project** (BETA-FOR) **and** the **subproject** (e.g. SP9). 

**!!! Due to software issues, please select the "@Funder identifier type" (= ROR) first !!!**

| Element / @Attribute Name 	| How to fill it		| Example 	|
|-------------------------------|-------------------------------|---------------|
| Funder name 			| Will be set automatically. The name of the project funder. | Deutsche Forschungsgemeinschaft (DFG) |			
| Funder identifier		| Will be set automatically. An unique identifier for the funder. | https://ror.org/018mejw64 |
| 🟣@Funder identifier type 	| Select **ROR**. A scheme for identifying organizations. | ROR |
| Award number			| Will be set automatically. The number of the grant. | 459717468 |
| Award URI			| Will be set automatically. The URI of the grant. | https://gepris.dfg.de/gepris/projekt/459717468 |
| 🟣Award title 			| Use an entry from autocomplete list. Fill in the first letter(s) of the project name. | BETA-FOR: Enhancing the structural diversity between patches for improving multidiversity and multifunctionality in production forests. | 

### 3.15 Related Items

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

There are 2 ways to start the upload process:

1) Click the **Primary Data** tab in the dataset details view ...

![Tab_Primary_Data](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Tab_Primary_Data.PNG)

 ... and click on _Upload_.
 
 ![Tab_Primary_Data_2](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Tab_Primary_Data_2.PNG)


2) Or select **Upload Data** in the Collect menu ...

![upload_data](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/upload_data.png)

... and specify whether your (primary) data is structured (tabular data) or unstructured (file).

![Upload_Data_2](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Upload_Data_2.PNG)

### 4.1 Upload File 

Select a file from your local computer or pick a file that has already been uploaded to the server.

BEXIS2 supports the following file formats:

![select_file](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/select_file.png)

Note, that the maximum supported file size is: **1024 MB**. If your file is larger than that, store it at ... and refer to the external storage location in the metadata / ![Alternate identifiers](38-alternate-identifiers). 

If your file is **larger than 4 MB**, use the ![*Push Big File*](#42-push-big-file) function.

### 4.2 Push Big File

If you have a large file (> 4 MB), upload it to the server first. For this case, every user has a **personal folder** where files can be stored temporarily. 
Files that are stored here, can be selected via the ![upload wizard](#4-upload-data) and loaded into the BEXIS2 environment.

![push_big_file](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/push_big_file.png)

### 4.3. Upload Tabular Data

Note: Tabular data can only be uploaded to the system if there is a corresponding Data Structure which defines its variables. If you have not created a Data Structure for your (tabular) data yet, do it now (check the "Create a Data Structure"-Manual).

Tabular data - in terms of BEXIS2 - is *structured data*. BEXIS2 supports both Excel (.xlsm, .xlsx) and ASCII files (.csv, .txt, .tsv). 

It is recommended to use a **BEXIS2 Excel template** (.xslm). 

The optimal workflow would be as follows: 
1) ![Create a Data Structure](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Manual.md#21-create-a-data-structure) for your tabular data
2) Download the Data Structure as an ![Excel template](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Manual.md#24-download-an-excel-template)
3) ![Fill the template](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Manual.md#25-work-with-an-excel-template) with your data
4) Upload the filled template

#### 4.3.1 Select File

Select a file from your local computer or a file that you have uploaded to the server before you started the Upload Wizard. The latter option, called ![*Push Big File*](#42-push-big-file), is intended for files larger than 4 MB, which can take several minutes to transfer. 

Click the _Next_ button to proceed to the next step.

![select_file](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/select_file.png) 

#### 4.3.2 Get File Information

This step varies depending on the format of your file. 

##### 4.3.2.1 BEXIS2 Excel template

If you have selected a BEXIS2 Excel template, the data structure and format information will be automatically extracted and this step is omitted. 

##### 4.3.2.2 Excel file

If your data is a (normal) Excel file, you have to specify the Header and Data part of your table.  

![Get_File_Information_fresh](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Get_File_Information_fresh.PNG)

Select the header part and click on *Header*.
Do the same with the data part. If you have a large file with lots of rows, select only the first data row and click on *Expand Selection*.
You can reset your selection by clicking on *Reset*. 

![Get_File_Information](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Get_File_Information.PNG)

Finally click on the _Next_ button to proceed.

##### 4.3.2.3 ASCII file

If you want to upload an ASCII file, you need to provide some information about the formatting and structure of your file.

![grafik](https://user-images.githubusercontent.com/68608907/234531709-21182201-8131-4b33-b929-fc210198449a.png)

* **Separator**: Is your data separated by a tab, comma, semicolon, space, ... ?
* **Decimal**: Do you use a period (e.g. 3.12) or a comma (e.g. 3,12) for decimal data?
* **TextMarker**: Do you use quotes (') or double quotes (") as text markers?
* **Orientation**: Is your data oriented column-wise or row-wise? (s. screenshots below)
* **Offset**: How many empty rows (or columns) are there before the header/data section begins?
* **Variables**: Row (or column) containing the variable names (= header).
* **Data**: Row (or column) where the data part starts. 

![Offset.JPG](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/columnwise.jpg)![Variables.JPG](https://github.com/BEXIS2/Documents/raw/master/Manuals/DCM/Images/rowwise.jpg) 

#### 4.3.3 Specify Dataset

Select a dataset from the dropdown list (if it is not preselected). Click on _Next_.

![Specify_Dataset](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Specify_Dataset.PNG)

#### 4.3.4 Validation

By clicking on the _Validate_ button, the file will be validated against the selected data structure. 

![Validate](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Validate.PNG)

If you get an error message, fix the problem and try to upload the data again. 

![Validation_Error](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Validation_Error.PNG)

Finally you will get the message *Succesfully validated*.

![Validation_Succesful](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Validation_Succesful.PNG)

What will be checked?

* Data types
* Completeness and order of the variables
* Constraints (Range, Pattern, Domain)

![grafik](https://user-images.githubusercontent.com/68608907/234524007-5f993d90-116c-4911-a453-e3b8e6e5db5e.png)


#### 4.3.5 Summary

In this last step, a summary of the uploaded file is displayed. Please review the information and click the _Finish_ button to confirm and complete the upload.

![Summary](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Upload%20Data/Images/Summary.PNG)


[Go to top](#1-overview)

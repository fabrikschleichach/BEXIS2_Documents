# Create a Data Structure

<!-- TOC -->

- [1 Overview](#1-overview)

- [2 Data Structure](#2-data-structure)
	- [2.1 Create a Data Structure](#21-create-a-data-structure)
		- [2.1.1 Mandatory Variables in the context of BETA-FOR](#211-mandatory-variables-in-the-context-of-beta-for)
	- [2.2 Edit a Data Structure](#22-edit-a-data-structure)
	- [2.3 Create a copy of a Data Structure](#23-create-a-copy-of-a-data-structure)
	- [2.4 Download an Excel template](#24-download-an-excel-template)
	- [2.5 Work with an Excel template](25-work-with-an-excel-template)
- [3 Variable Templates](#3-variable-templates)
	- [3.1 Data Types](#31-data-types)
	- [3.2 Units](#32-units)
	- [3.3 Create a Variable Template](#33-create-a-variable-template)




<!-- /TOC -->

## 1 Overview

In BEXIS2, data is stored and managed as part of a **dataset**. You can think of a Dataset as a container for the (primary) data on the one hand, and the metadata on the other. 

![image](https://user-images.githubusercontent.com/68608907/232004312-0192043f-03be-4b11-b8bf-01e935f9f40b.png)

* **Metadata**: describing facts about the dataset, e.g. who created the dataset and when
* **(Primary) Data**: can be files or tabular data
* **File**: unstructured data, e.g. an audio file or image
* **Tabular Data**: structured data; supported formats are Excel and ASCII
* **Data Structure**: describes the structure of the data
 
The Data Structure of a File is its technical format. 

The Data Structure of Tabular Data are its **Variables**. Each Variable is a specific instance of a [variable template](#3-variable-templates), which is defined by its Data Type, Unit and unique name. 

If you want to upload tabular data to the system, there must be a corresponding data structure.

## 2 Data Structure

Data Structures contain Variables, which are specific instances of [Variable Templates](#3-variable-templates). A variable can have the same name as its underlying template or be more specific, e.g. *variable template*: species_detected, *variable*: Parus_major. For every column of your tabular data you have to define a variable. 

![image](https://user-images.githubusercontent.com/68608907/232013885-99b17aed-9d5d-4143-b3f4-921e7b86f240.png)

### 2.1 Create a Data Structure

Click on Create Data Structure from *Plan > Manage Data Structures*. 

![Plan](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Images/Plan.PNG)

![Create Data Structure](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Images/Create_Data_Structure.PNG)

Then select the Tabular option. Enter a name and a description and click on the Save button.

![Create Data Structure 2](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Images/Create_Data_Structure_2.PNG)

BEXIS2 will now refer you to the tool with which you can build your data structure by adding variables.

![Edit Data Structure new](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Images/Edit_Data_Structure_new.PNG)


Choose - if possible - a variable template starting with an uppercase letter. These have been defined especially for BETA-FOR. If there`s no variable template that fits to your data yet, you can [create a new one](#33-create-a-variable-template).

Always provide some date and time information (in ISO 8601 standard). 

When you click the arrow button next to a variable template, the variable will be displayed on the right side. You can keep its name or make it more specific.

![Change Name](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Images/Change_Name.PNG)

You can change the order of the variables by dragging and dropping them. 

A variable can be deleted from a structure by clicking on the trash button.

If the *Optional* checkbox is selected, the variable/column of your tabular data can have empty entries.

You can also define a placeholder for missing values. Their might be one by default, but you can adjust it and add more.Cancel changes

![Define variables](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/missing_values.png) 

### 2.1.1 Mandatory Variables in the context of BETA-FOR

Every BETA-FOR Dataset should contain these two Variables:

| Variable Name		| Possible Values	| Why mandatory?	| Example	|
|----------------------	|-----------------------|----------------------|---------------|
|**PatchLabel_BETAFOR**	| 			| Link to the detailed geographic information in a separate Dataset. | U03EAB003 |
|**Treatment_present**	| true, false		| Indicates if the treatment was already present when the data was collected. | true |

### 2.2 Edit a Data Structure

You can edit an existing Data Structure by clicking on the edit button.

![Edit Button](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Images/Edit_Button.PNG)

**BUT: A Data Structure cannot be changed anymore (or deleted) once it is linked to a dataset!!!**

### 2.3 Create a copy of a Data Structure

You can create a copy of a data structure, whether it is Tabular or File (structured or unstructured), in two ways:

1) On the page *Data Structure Search*, click on the _Copy_ button next to a Data Structure.
2) On the *Data Structure Edit* page, click the _Save as_ button. 

Just change the name of the copy.

![Copy Data Structure](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Images/Copy_Data_Structure.PNG)


### 2.4 Download an Excel template

You can download a Data Structure as Excel template in two ways:

1) On the page *Data Structure Search*, click on the _Download_ button next to a Data Structure.
2) On the *Data Structure Edit* page, click the _Download Excel Template_ button. BEXIS 2 creates an Excel Template from the current Data Structure.

![Download Excel Template](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Images/Download_Excel_Template.PNG)

Save the Excel Template to your preferred location on your computer.

### 2.5 Work with an Excel template
An Excel template is an Excel file that includes all the information about its underlying Data Structure. There are macros that check if your filled in data match the defined Data Types. For example: If you enter "one" into a variable/column with data type *integer*, you will get an error.

Usually, when you first open a template file, you get a security warning "macros have been disabled". In this case, choose the option "Enable content". 
Macro security settings are generally located in the Trust Center.

![Makros aktivieren](https://github.com/fabrikschleichach/BEXIS2_Documents/blob/master/Manuals/Create%20a%20Data%20Structure/Images/Makros_aktivieren.PNG)

## 3 Variable Templates

You can think of a Variable Template as a construction plan for a variable. It defines the data type and unit of a variable. 

The idea of Variable Templates is to **support reusability**: You don`t have to define the data type or unit of a variable each time you upload data. Instead, you can pick an existing variable template and modify its properties according to your needs. This way, you also **improve data quality**, since similar things are defined to be similar, and thus can be more easily related to each other.

To increase the compatibility of our project data with data from other biodiversity projects, the naming of our variable templates is mainly based on **Darwin Core**. [Darwin Core](https://dwc.tdwg.org/) "includes a glossary of terms (in other contexts these might be called properties, elements, fields, columns, attributes, or concepts) intended to facilitate the sharing of information about biological diversity by providing identifiers, labels, and definitions." 

### 3.1 Data Types

A data type is an attribute associated with a piece of data that tells a computer system how to interpret its value. 

You can choose one of the following data types:
	
Name	      	| Description 	| Example
------------- 	| ------------- | -----------
Boolean		| boolean value	| true, false, 0, 1
Date		| YYYY-MM-DD	| 2023-06-12
DateTime	| YYYY-MM-DDThh:mm:ss; stores an instant in time expressed as a calendar date and time of day; its precision can range from a year to a fraction of a second.	      | 2015-05-12T13:20:05, 2022-08-24
Decimal		| stores real numbers like Double, but with higher precision | 	7, 38.787, -24.666	|
Double		| stores real numbers | 12.6, 123.89999, -34.98, 9		|	
Integer		| stores whole numbers | -12, 0, 34567, 120		|
String		| sequence of characters | "one", "Turdus merula", "Horchbox", "13"
Time		| hh:mm:ss	| 12:39:46

### 3.2 Units

With the Unit Manager you are able to create, modify and delete Units. 

If the Unit you require is not yet part of the unit list, you can create it by clicking on the Create Unit button. Fill the fields, select a Measurement System and select or create a Dimension. To create a Dimension enter a Name in the Dimension Name field and edit the Dimension Specification pattern "L(0,0)M(0,0)T(0,0)I(0,0)Θ(0,0)N(0,0)J(0,0)". For more information about Dimension click [here](https://translate.google.de/translate?sl=de&tl=en&js=y&prev=_t&hl=de&ie=UTF-8&u=https%3A%2F%2Fde.wikipedia.org%2Fwiki%2FDimension_%28Gr%25C3%25B6%25C3%259Fensystem%29&edit-text=). For example, a Unit "meter per second" (m/s) would be represented as "L(1,0)M(0,0)T(0,1)I(0,0)Θ(0,0)N(0,0)J(0,0)".

Select at least one Data Type from the list.

Click on the Save button and the Unit is stored if all information is correct and it is not a duplicate.

Use ![img12](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/edit_button.png) to edit and ![img13](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/delete_button.png) to delete a Unit.

![Create Unit](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/create_unit.png) 


### 3.3 Create a Variable Template

If there is not yet a variable template, that fits to your data, you can email your data manager (betafor@uni-wuerzburg.de) or create one on your own. 

![Create Variable templates](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/create_variable.png) 

To create a Variable Template, click on the Create Variable Template button and fill in the fields:

**Name**

As most of our Variable Templates are based on Darwin Core Terms, it would be great, if you could search for a suitable name/term in the [Darwin Core Quick Reference Guide](https://dwc.tdwg.org/terms/). 

Otherwise ...

* Choose an English name
* Starting with a capital letter
* No spaces
* No special characters
* Avoid abbreviations
* If your Variable Template name consists of more than one word, combine it with CamelCase, e.g. Species detected -> "SpeciesDetected".

**Short Name**

Same entry as Name.

**Unit**

Select a Unit from the list or [create a new one](#32-units)

**Data Type**

Select a [Data Type](#31-data-types) from the list. 

**Description**

Please take some time to add a short description to ensure that others with similar data can reuse the variable template. 

**Constraints**

Define Constraints if you want to set limitations which will be checked during the validation process.

There are three types of constraints:

![grafik](https://user-images.githubusercontent.com/68608907/233010636-9ccf121e-e9ed-4fb0-8d46-c4d39a951b37.png)

* **Range**: If the input data is of type *Numeric*, this constraint checks whether the input value falls within the specified range. If the input data is of type *String*, the range check behaves like a length check, i.e. the length of the input string should fall within the range. The range has a lower and an upper limit. You can select the corresponding checkboxes if you want to include the limits in the range. If the "negate" checkbox is activated, the function checks whether the value is out of range!
* **Pattern**: Only for data of type String. The pattern constraint takes the value as input and matches it against the specified pattern. Please [test the regular expression](https://regexr.com/) before entering it here. If the "negate" checkbox is activated, the function will check if the input does not match the pattern!
* **Domain**: Takes the value as input and matches it against each item in the list. If there´s a match, the matching process stops and returns true. If no match is found, the function returns false. No duplicate item is allowed, although it does not affect the matching process. Domain items can be characters, strings, Booleans or numbers. Their data type is determined by the associated Variable Template. If the "negate" checkbox is activated, the function will return true if there`s no matching item!

Use ![Edit button](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/edit_button.png) to edit and ![Delete Button](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/delete_button.png) to delete a Variable Template.






[Go to top](#1-overview)

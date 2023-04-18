# Data Plannig / Description

<!-- TOC -->

- [1 Overview](#1-overview)

- [2 Data Structure](#2-data-structure)
	- [2.1 Create a Data Structure](#21-create-a-data-structure)
	- [2.2 Edit a Data Structure](#22-edit-a-data-structure)
	- [2.3 Create a copy of a Data Structure](#23-create-a-copy-of-a-data-structure)
	- [2.4 Download an Excel template](#24-download-an-excel-template)
	- [2.5 Work with an Excel template](25-work-with-an-excel-template)
- [3 Variable Templates](#3-variable-templates)
	- [3.1 Data Types](#31-data-types)
	- [3.2 Units](#32-units)
	- [3.2 Create a Variable Template](#33-create-a-variable-template)




<!-- /TOC -->

## 1 Overview

In BEXIS2, data is stored and managed as part of a **dataset**. You can think of a Dataset as a container for the (primary) data on the one hand, and the metadata on the other. 

![image](https://user-images.githubusercontent.com/68608907/232004312-0192043f-03be-4b11-b8bf-01e935f9f40b.png)

* **Metadata**: describes the dataset, e.g. who created the dataset and when
* **(Primary) Data**: can be files or tabular data
* **File**: unstructured data, e.g. an audio file or image
* **Tabular Data**: structured data; supported formats are Excel and ASCII
* **Data Structure**: describes the structure of the data
 
The Data Structure of a File is its technical format. 

The Data Structure of Tabular Data are its **Variables**. Each Variable is a specific instance of a variable template, which is defined by its Data Type, Unit and unique name. 

If you want to upload tabular data to the system, there must be a corresponding data structure.

## 2 Data Structure

Data Structures contain Variables, which are specific instances of Variable Templates. A variable can have the same name as its underlying template or be more specific, e.g. *variable template*: species_detected, *variable*: Parus_major. For every column of your tabular data you have to define a variable. 

![image](https://user-images.githubusercontent.com/68608907/232013885-99b17aed-9d5d-4143-b3f4-921e7b86f240.png)

### 2.1 Create a Data Structure

Click on Create Data Structure from *Plan > Manage Data Structures*, and then select the Tabular option. Enter a name and a description and click on the Save button. 

![Create Datastructure](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/create_data_structure.png) 

BEXIS2 will now refer you to the page where you can build your data structure by adding variables.

![Add Variables](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/add_variables.png)
Choose - if possible - a variable template starting with an uppercase letter. These have been defined especially for BETA-FOR.

When you click the arrow button next to a variable template, the variable will be displayed on the right side. You can keep its name or make it more specific. 

You can change the order of the variables by dragging and dropping them. 

A variable can be deleted from a structure by clicking on the trash button.

If the *Optional* checkbox is selected, the variable/column of your tabular data can have empty entries.

You can also define a placeholder for missing values. Their might be one by default, but you can adjust it and add more.

![Define variables](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/missing_values.png) 

### 2.2 Edit a Data Structure

**A Data Structure cannot be changed anymore (or deleted) once it is linked to a dataset!!!**

### 2.3 Create a copy of a Data Structure

You can create a copy of a data structure, whether it is Tabular or File (structured or unstructured), by clicking on the _Save as_ button. Just change the name of the copy.

![Copy Data Structure](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/copy_data_structure.png) 

### 2.4 Download an Excel template

You can download a Data Structure as Excel template in two ways:

1) On the page Data Structure management, click on the Download button next to a Data Structure.
2) On the Edit Data Structure page, click the Download Excel Template button. BEXIS 2 creates an Excel Template from the current Data Structure.

Save the Excel Template to your preferred location on your computer.

### 2.5 Work with an Excel template
An Excel template is an Excel file that includes all the information about its underlying Data Structure. There are macros that check if your filled in data match the defined Data Types. For example: If you enter "one" into a variable/column with data type *integer*, you will get an error.

Usually, when you first open a template file, you get a security warning "macros have been disabled". In this case, choose the option "Enable content". 
Macro security settings are generally located in the Trust Center.

![Enable Macro](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/Help_img6.png) 

## 3 Variable Templates

You can think of a Variable Template as a construction plan for a variable. It defines the data type and unit of a variable. 

The idea of Variable Templates is to **support reusability**: You don`t have to define the data type or unit of a variable every time you use it in your tabular data. Instead, you can pick an existing variable template and modify its properties according to your needs. This way, you also **improve data quality**, since similar things are defined to be similar, and thus can be more easily related to each other.





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

If there is not yet a variable template, that fits to your variable, you can create a new variable template.
With the Variable Template Manager you are able to create, modify and delete Variable Templates (called Data Attributes in older BEXIS2 versions). Variables are required to create Data Structures.

To create a Variable Template, click on the Create Variable Template button. Fill the fields. Select an associated Unit and Data Type and click on the Save button. The Variable Template is stored if all information are correct and it is not a duplicate.

Use ![Edit button](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/edit_button.png) for edit and ![Delete Button](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/delete_button.png) for delete a Variable Template.

![Create Variable templates](https://github.com/BEXIS2/Documents/raw/master/Manuals/RPM/Images/create_variable.png) 

It is possible to put constraints on Variable Templates, to add constraints click on the link Constrains. You can add a Range, a Pattern and a Domain Constraint to each Variable Template.

*   Range: If the input data is of numeric type, this constraint checks whether the input value falls in the specified range. If the input data is of type string, the range check behaves like a length check, which means the length of the input string should fall in the range. The range has a lower bound and an upper bound, plus two indicators to show whether the boundary values are included in the range. Negate function checks if the value is out of the range!
*   Pattern: takes the value as input and matches it against a pattern to see whether the pattern is found in the input. If so, it returns true; otherwise false. Pattern constraints apply to text values only, for more information on the format click [here](https://en.wikipedia.org/wiki/Regular_expression).
*   Domain: takes the value as input and matches it against each and every domain item in the list. If the value matches one, it stops matching and returns true, which means the value satisfies the constraint. If no match is found it returns false. No duplicate domain item is allowed, although it does not affect the matching procedure described. Domain items can be characters, strings, Booleans or numbers. Their data type is enforced by the associated Variable Template. Using the domain constraint as a tool to model acronyms and similar topics provided that some extra information such as description of each item is available, is supported.
*   Negation: The inversion of the chosen constraint will apply. In fact the result of the constraint is XORed with the negation field. For example, a negated Range Constraint of Min=1 and Max=100 will allow all values outside of this range.








[Go to top](#1-overview)

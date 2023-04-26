# Dataset Permissions

<!-- TOC -->
- [1 Overview](#1-overview)
- [2 Dataset permissions via metadata](#2-dataset-permissions-via-metadata)
- [3 Dataset permissions via menu](#3-dataset-permissions-via-menu)
- [4 Dataset Requests](#4-data-requests)
- [3 Dashboard](#3-dashboard)
		- [3.1 My Datasets](#31-my-datasets)
		- [3.2 My Requests](#32-my-requests)
		- [3.3 Decision](#33-decision)

	

<!-- /TOC -->

## 1 Overview

Who can see your data?

People logged into BEXIS2 can see the metadata of your dataset but not the (primary) data, unless you give them read permission. 

In BEXIS2 there are two ways to give permissions for a dataset:

* Implicitly, via the ![metadata form](#2-dataset-permissions-via-metadata)
* Explicitly, via the ![Dataset Permissions menu](#3-dataset-permissions-via-menu)

There are 4 different permission types:
* **Read** (see the primary data and download it)
* **Write** (edit the dataset)
* **Delete** (delete the dataset)
* **Grant** (give permissions to other users or groups)

## 2 Dataset permissions via metadata

You can give persons permissions on a dataset by considering them as creator (= owner) or contributor of a dataset. 

| Role 		| Permissions	|
|---------------|---------------|
|Creator	| Read, Write, Delete, Grant |
|Contributor	| Read		|	

## 3 Dataset permissions via menu

Select a Dataset and open the *Dataset Permissions* tab. 

![grafik](https://user-images.githubusercontent.com/68608907/234571603-d9f42d02-e111-4a12-b2a5-d3f522ffeb39.png)

Grant permissions on the dataset to another user by selecting the appropriate checkboxes.  
If you want to set permissions for all project members, it is best practice to set permissions for the corresponding Group (e.g. BETA-FOR) and not for each individual User. 

## 4 Dataset Requests




### 3 Dashboard
#### 3.1 My Datasets
Overview on all datasets the currently logged in user has access. Datasets are groups by permission: Own (full permission including granting permission), Edit, and download.
Datasets marked in red have incomplete metadata.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/dashboard.png)


#### 3.2 My Requests
List of all your pending and answered requests for data access permissions. Pending requests can be withdrawn/delete, if the request is not anymore valid.
![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/Requests.png)

 
#### 3.3 Decision
List of all answered and pending requests related to your datasets. You can accept (hook) or reject (minus) pending requests. The requesting person will be informed via email about your decision. 

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/decision.png)





[Go to top](#a-overview)

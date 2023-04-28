# Dataset Permissions

<!-- TOC -->
- [1 Overview](#1-overview)
- [2 Unpublished Datasets](#2-unpublished-datasets)
	- [2.1 Dataset permissions via metadata](#21-dataset-permissions-via-metadata)
	- [2.2 Dataset permissions via menu](#22-dataset-permissions-via-menu)
	- [2.3 Dataset Requests](#23-dataset-requests)
- [3 Published Datasets](#3-published-datasets)

<!-- /TOC -->

## 1 Overview

Who can see your data?

The answer to this question depends mainly on whether your dataset is published or not. **Published data** is freely available (under a licence that the owner(s) choose). **Unpublished data**, by default, can only be viewed by its owner(s) and by the contributors of the dataset. However, the owner(s) of the dataset can grant permissions to others. 

## 2 Unpublished Datasets

People logged into BEXIS2 can see the metadata of your dataset but not the (primary) data, unless you give them read permission. 

In BEXIS2 there are two ways to give permissions for a dataset:

* Implicitly, via the ![metadata form](#2-dataset-permissions-via-metadata)
* Explicitly, via the ![Dataset Permissions menu](#3-dataset-permissions-via-menu)

There are 4 different permission types:
* **Read** (see the primary data and download it)
* **Write** (edit the dataset)
* **Delete** (delete the dataset)
* **Grant** (give permissions to other users or groups)

### 2.1 Dataset permissions via metadata

You can give persons permissions on a dataset by considering them as creator (= owner) or contributor of a dataset. 

| Role 		| Permissions	|
|---------------|---------------|
|Creator	| Read, Write, Delete, Grant |
|Contributor	| Read		|	

### 2.2 Dataset permissions via menu

Select a Dataset and open the *Dataset Permissions* tab. 

![grafik](https://user-images.githubusercontent.com/68608907/234571603-d9f42d02-e111-4a12-b2a5-d3f522ffeb39.png)

You can grant permissions on the dataset to another user by selecting the appropriate checkboxes.  
If you want to set permissions for all project members, set permissions for the corresponding *Group* (e.g. BETA-FOR) and not for each individual *User*. 

### 2.3 Dataset Requests

If you select a Dataset for which you don`t have read permission, you can only see its Metadata and Data Structure. If you also want to see and download its Primary Data, you can send an **Access Request** to its Owner(s). 

![grafik](https://user-images.githubusercontent.com/68608907/234676764-729632fd-6615-4a70-a5e1-842962279f7f.png)

Please include the sequence number of the corresponding **Paper Proposal** if you wish to use the requested data for a publication.

In your **Dashboard** you will find a list of all your pending and answered data access requests. Pending requests can be withdrawn/deleted if the request is no longer valid.

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/Requests.png)

There is also a list of all answered and pending requests related to your datasets. You can accept (hook) or reject (minus) pending requests. The requesting person will be automatically informed about your decision via email. 

![image info](https://github.com/BEXIS2/Documents/raw/master/Manuals/DDM/Images/decision.png)

## 3 Published Datasets

The owners of a dataset decide when and under which licence it should be published. BETA-FOR datasets should be published not later than 3 years after the end of data collection/compilation. In exceptional cases, after 5 years (see Publication Policy).

Published datasets are freely available and can be viewed and downloaded by anyone (not just project members). 

If you want to know, which datasets have already been published, select the *public only* checkbox in the Search UI:

![grafik](https://user-images.githubusercontent.com/68608907/235094582-2446eda2-5977-4168-abd3-3caeec5fe6c7.png)



[Go to top](#1-overview)

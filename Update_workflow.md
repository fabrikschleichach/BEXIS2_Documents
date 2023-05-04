 # Updating BEXIS2 requires the following steps:

<!-- TOC -->
- [1 Preparations](#1-preparations)
- [2 Database](#2-database)
- [3 File system](#3-file-system)
- [4 Security settings](#4-security-settings)
- [5 Testing](#5-Testing)

<!-- /TOC -->

## 1 Preparations
* Download the newest BEXIS2 release from here: https://bexis2.github.io/software/releases
* Stop the current Site via IIS

## 2 Database
* **Backup** *current* (PostgreSQL) db
* Rename *current* (PostgreSQL) db: BEXIS_v--- 
* **Create** *new* (PostgreSQL) db: BEXIS
* **Restore** *new* db with backup
* Update *new* db with Update_Script:
	* Right-click on BEXIS and click on **CREATE Script**
 	* Open Update_Script_---to---.sql
 	* Click on Execute
		
![grafik](https://user-images.githubusercontent.com/68608907/236138033-6ca678b2-ac88-4328-85b6-9791cac5b282.png)
![grafik](https://user-images.githubusercontent.com/68608907/236138629-7a9fcea6-275b-42df-84c5-d5f9fc465653.png)


## 3 File system
* Create a new folder (BEXIS2_v---) in C:\inetpub\wwwroot and change to this directory
* Copy *new* **Site**  
* Take the *new* **Site/Web.config.sample** and fill in the following parameter:

	* ```<add name="ApplicationServices" connectionString="Server=wrzh088.uni-wuerzburg.eu;Port=5432;Database=BEXIS;Userid=postgres;Password=1;Pooling=true;MinPoolSize=2;MaxPoolSize=100;ConnectionIdleLifetime=3600;" />```
	* ```<add key="ApplicationName" value="BETA-FOR Data" />```
	* ```<add key="CreateDatabase" value="false" />```
	* ```<add key="WorkspacePath" value="{WORKSPACE}" />```
	* ```<add key="DataPath" value="{DATA}" />```
	* ```<add key="TenantId" value="betafor" />```
	* ```<add key="SystemEmail" value="betafor@uni-wuerzburg.de" />```
	* ```<add key="usePersonEmailAttributeName" value="true" />```
	
* Copy *current* **Data** 
* Copy *current* **Workspace**  
* Update Workspace (if it`s needed)

## 4 Security settings
* Set security settings (if it`s needed) for Data, Workspace and Site 

![grafik](https://user-images.githubusercontent.com/68608907/235126020-bb9dccc1-5815-4871-b136-863c203cf651.png)

## 5 Testing
* Start the Site
* Test functions

Finished!

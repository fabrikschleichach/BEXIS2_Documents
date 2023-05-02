 # Updating BEXIS2 requires the following steps:

<!-- TOC -->
- [1 Preparations](#1-preparations)
- [2 Database](#2-database)
- [3 File system](#3-file-system)
- [4 Security settings](#4-security-settings)
- [5 IIS](#5-IIS)
- [6 Testing](#6-Testing)

<!-- /TOC -->

## 1 Preparations
* Download the newest BEXIS2 release from here: https://bexis2.github.io/software/releases
* Stop the current Site via IIS

## 2 Database
* **Backup** *current* (PostgreSQL) db
* Rename *current* (PostgreSQL) db: BEXIS_v--- 
* Create *new* (PostgreSQL) db (BEXIS)
* **Restore** *new* db with backup
* **Refresh** *new* db

## 3 File system
* Create a new folder (BEXIS2_v---) in C:\inetpub\wwwroot and change to this directory
* Copy *new* **Site** 
* Copy *current* **Site\web.config**  
* Copy *current* **Data** 
* Copy *current* **Workspace** 
* Update Workspace (if it is needed)

## 4 Security settings
* Set security settings (if it is needed) for Data, Workspace and Site 
![grafik](https://user-images.githubusercontent.com/68608907/235126020-bb9dccc1-5815-4871-b136-863c203cf651.png)

## 5 IIS
* Create a new website (BEXIS2_v---) on a test port
* Open Application Settings:
  * **DataPath** = C:\inetpub\wwwroot\BEXIS2_v---\Data
  * **WorkspacePath** = C:\inetpub\wwwroot\BEXIS2_v---\Workspace
  * **CreateDatabase** = false 
 
![grafik](https://user-images.githubusercontent.com/68608907/235127702-c16a0be9-5b56-47ab-9a47-dd96da637d3b.png)

## 6 Testing
* Start the new Site
* Test functions on the server 
* Change the port to the correct one
* Test functions on normal browser out of server

Finished!

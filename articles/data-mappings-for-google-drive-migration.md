---
title: About the FLY User Guide
description: user guide.
ms.date: 11/02/2017
ms.prod: sharepoint
localization_priority: Priority
---

# Data Mappings for Google Drive Migration

 
## Site Data


|**Google Drive Data Type**  |**SharePoint/OneDrive For Business Data Type**   |
|---------|---------|
|My Drive |Library/Folder         |
|Shared Drive | Library/Folder        |
|Folder |  Library/Folder       |
|File         |     File    |
|File Version     |   File Version      |
|Google Docs     |    Microsoft Word     |
|Google Sheets     |    Microsoft Excel     |
|Google Slides     |     Microsoft PPT    |
|Google Forms     |    ZIP File     |
|Google Drawings     |   PNG File      |

 
## Metadata

|**Google Metadata Type**  |**SharePoint/OneDrive For Business Metadata**   |
|---------|---------|
|Owner/Created By|Created By **[1]**|
|Modified by|Last Modified By|
|Created Time|Created|
|Modified Time|Modified|
 
**[1]** The Owner and Created By metadata of Shared Drive is not supported being migrated because the metadata cannot be retrieved. This issue is due to API limitation.   

 > [!NOTE]
 > By default, FLY will map metadata from Google Drive to SharePoint based on the above mappings. Users can also configure property mappings in FLY to map metadata.  

## Permission Level

|Google Drive Permission Level|SharePoint/OneDrive For Business Permission Level|
|---------|---------|
|File Organizer|Full Control|
|Organizer|Full Control|
|Owner|Full Control|
|Writer|Contribute|
|Commenter|Read|
|Reader|Read|

 

 > [!NOTE]
> By default, FLY will map permissions from Google Drive to SharePoint based on the above mappings. Users can also configure permission mappings in FLY to map permissions.
 
---
title: Define and build the data model
description: After planning is complete, define and build the data model. Create one or more tables with fields, load the table with demo data, and verify access controls to the data.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Define and build the data model

After planning is complete, define and build the data model. Create one or more tables with fields, load the table with demo data, and verify access controls to the data.

## Create an application

Create or open an application record.

-   Create: If creating an application directly, use [Guided App Creator](https://developer.servicenow.com/dev.do#!/learn/courses/rome/app_store_learnv2_buildmyfirstapp_rome_build_my_first_application/app_store_learnv2_buildmyfirstapp_rome_guided_app_creator_and_servicenow_studio/app_store_learnv2_buildmyfirstapp_rome_guided_app_creator_and_servicenow_studio_objectives) to create the application. Guided App Creater allows you to create tables from spreadsheets, roles, and security rules. Design options are also available.
-   Open: If developers do not have the admin role, the ServiceNow System Administrator needs to create the application and grant developers a delegated development role. Developers then use Studio to open the application for editing.

**Note:** The application scope and table name are sometimes referred to as the internal names for these objects and cannot be changed once they are created. However, the application name and table label can be changed. Application users see the internal names in the URL only. If possible, internal names should always be consistent with what the user sees.

-   **[Build the data model](build-data-model.md)**  
Create tables and fields on the tables to support the application’s data model.
-   **[Secure data](secure-data.md)**  
Data security is one of the most important and overlooked aspects of creating an application. ServiceNow automatically configures access control for a new or selected role during the table creation process. Only users with the role can access the table to read, create, write, and delete.
-   **[Manage data](manage-data.md)**  
With the data model \(tables and fields\) created and security set up, add data into the application’s table\(s\).

**Parent Topic:**[Build your application](build-your-application.md)


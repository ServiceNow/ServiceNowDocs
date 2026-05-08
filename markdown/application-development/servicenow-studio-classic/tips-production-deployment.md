---
title: Legacy - Production deployment tips
description: When you develop customizations to applications on the ServiceNow platform, you deploy them via the application repository to a production instance. This topic examines and provides cautions for the tradeoffs between installing an application from the application repository versus Git repository with source control.
locale: en-US
release: australia
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Legacy - Source Control integration, Legacy - ServiceNow Studio, Building pro-code applications, Developing your application, Building applications]
---

# Legacy - Production deployment tips

When you develop customizations to applications on the ServiceNow® platform, you deploy them via the application repository to a production instance. This topic examines and provides cautions for the tradeoffs between installing an application from the application repository versus Git repository with source control.

**Important:** Starting with the Xanadu release, the legacy version of ServiceNow Studio is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

Try building and editing apps in the current version of ServiceNow Studio instead. For more information, see [ServiceNow Studio](../../servicenow-studio/concept/servicenow-studio-landing.md).

## Overview or deploying to production

Technically, you can still “deploy” an application from a Git repository to a production instance using source control. This can have unintended consequences.

## Glossary of terms

|Term|Definition|
|----|----------|
|[Metadata or application files](c_ApplicationFiles.md)|The sys\_metadata records that define configuration in ServiceNow and are packaged in an application. These records alter the behavior of the instance but do not contain data such as incident or CMDB records. \(See Note below\)|
|[Scoped applications](c_ApplicationScope.md)|ServiceNow applications that restrict allowing only updates and operations within the boundary of the scope. This mechanism is used for most new development.|
|[Global applications](c_ApplicationScope.md)|Global applications are developed in the legacy global scope. Work is often done in this scope to customize existing ServiceNow applications such as IT Service Management \(ITSM\).|
|[Application repository](app-repo.md)|Applications are typically published here for deployment in production instances. Although the application repository has separate entitlement rules, it operates similarly to the ServiceNow Store.|
|ServiceNow Store|Repository for third-party \(vendor\) applications as well as ServiceNow published applications. Most customers do not publish to the Store, but often install applications from it.|
|[Update sets](../../system-update-sets/concept/system-update-sets.md)|Standard method of packaging customizations for deployment in each successive instance. They contain the incremental collection of insertions, updates, and deletions.|
|[Legacy - Delta loading](delta-loading.md)|The most efficient method of loading because it changes only from source control rather than earlier uninstall/reinstall methods.|
|Schema|Definition of tables and columns in the tables.|
|Rollback|Administrators can roll back the last installation of a selected application. A rollback removes all code, table, and file updates from the initial installation.|

**Note:** The **sys\_metadata** table is the parent table of all application files in the ServiceNow platform using the table inheritance model. You can view summary information for metadata by visiting the parent table or tables that extend directly or indirectly as indicated by the Extends table\(super\_class\) field on the Table\(sys\_db\_object record\). You can also see the whole schema by visiting the Table\(sys\_db\_object\) form for the **sys\_metadata** table and selecting the **Show Schema Map** related link at the bottom of the form. The schema is large and so takes some time to render.

![Schema mapping](../image/tips-schema-map.png)

![Schema map table of contents](../image/tips-schema-map-link.png)

## Installation location

When you install source control, it facilitates the ongoing development of a custom application. Therefore, the application is managed as an “In development” application in the Custom Application \[sys\_app\] table rather than as an “Installed” application in the Store Application \[sys\_store\_app\] table. Both tables are extensions of sys\_scope so they both provide the same protections and restrictions as the scope. So when you search for the installation of a source control deployed application, refer to the System Application \[sys\_app\] table and the **in development** section of the Application Manager page.

You cannot have a sys\_app record on the instance while deploying that same application from the ServiceNow Store or application repository. The two deployment models are mutually exclusive. If at any point the deployment model changes, the sys\_app record must be converted to a sys\_store\_app record first. You can contact ServiceNow Support for help with performing that operation.

## Delta loading

Prior to the ServiceNow Paris release, application installation from source control always removed and reinstalled the entire application when triggered, including the Apply Remote Changes function. With [Legacy - Delta loading](delta-loading.md), now only the changes update, simplifying the process considerably.

The Delta loading process loads the changes from source control incrementally. When you apply remote changes, you don’t drop existing tables or columns unless they were removed from the repository. This preserves the data for tables and fields that continued to be present.

**Note:** The **glide.source\_control.allow\_delta\_loading\_in\_scopedapp** property allows you to disable Delta loading in Paris; however, this will revert to the more destructive behavior of removing and reinstalling the application. Global applications in Paris always use Delta loading.

Below is a table of the different expected outcomes in an instance using Delta loading.

|Application type|Install source|Schema present in package|Schema contains data|Claim by another app \(Global\)|Expected outcome for data and schema|
|----------------|--------------|-------------------------|--------------------|-------------------------------|------------------------------------|
|Scoped|Application repository or Store|Yes|Yes/No|N/A|Preserved|
|Scoped|Application repository or Store|No|Yes/No|N/A|Preserved|
|Scoped|Source control|Yes|Yes/No|N/A|Preserved|
|Scoped|Source control|No|Yes/No|N/A|Removed|
|Global|Source control, Application repository, or Store|Yes|Yes/No|Yes/No|Preserved|
|No|Yes|No|Preserved \(1\)|
|No|No|Yes|Preserved \(2\)|
|Source control|No|No|No|Removed \(3\)|
|Application repository|No|No|No|Preserved|

**Note:**

-   While the database schema and the data are preserved, they will be moved into the default global application.
-   While the database schema and the data are preserved, they will be moved into the global application which previously held claim to these files if installed. Otherwise, they will move into default global application.
-   Applicable only on custom columns with **u\_ prefix**. ServiceNow platform-authored columns are not dropped.

When switching branches in source control for a scoped application, use extreme caution in a production environment. If the target branch is missing schema elements found in the current branch, the related schema is dropped, destroying any data it contains. \(Global applications do not drop schema when data is present.\)

Just as with update sets, only a subset of the incremental changes needs to be applied with Delta loading. Unlike update sets, the application package represents the complete application. Files that are absent from the new package are deleted. This can alter functionality and delete data. Update sets and applications upgraded from the application repository or ServiceNow Store must have an explicit **DELETE** payload to remove a file or drop a schema.

If application files are being generated dynamically in any fashion, the next install/apply remote changes the operation of an application deletes those records. They are considered absent from the incoming application package. If you stash local changes, the application files may be recoverable by a stash commit, but if data is lost as a result of the changes, the data is not recovered.

**Note:** Removing or suppressing sys\_update\_xml records prevents them from being removed by Delta loading; however, this action can have other severe or undesirable results.

Direct edits to the repository, especially to remove files, can have significant ramifications, including loss of data and cascading deletes. Perform this action with care.

-   **[Legacy - Author elective and customer updates](tips-customer-updates.md)**  
When you install an application from the application repository or ServiceNow® store, you can set a series of properties to define the behavior of delete and choice processing. These kinds of choices are called an "author-elective" feature.
-   **[Legacy - Roll back, back out, and uninstall](tips-rollback-backout-uninstall.md)**  
The application installation from the application repository is recorded for rollback, which means as an administrator, you can roll back the last installation of a selected application. When you roll back an application, you remove all code, table, and file updates from the initial installation.
-   **[Legacy - Upgrade history](tips-upgrade-history.md)**  
Upgrade history records and history line dispositions are generated as part of the source control installation providing a record of the install.
-   **[Legacy - Development considerations](tips-dev-considerations.md)**  
When you are developing code, consider some of these suggestions for the most efficient performance.

**Parent Topic:**[Legacy - Source Control integration](c_SourceControlIntegration.md)


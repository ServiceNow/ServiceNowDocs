---
title: Create a data model for your application
description: Create a data model in App Engine Studio \(AES\) for your application by creating the tables that will house your application data. Create data tables that will be used in your application by creating the table from scratch, uploading a spreadsheet or PDF, or by using an existing table as a template. You can also create and schedule data imports by mapping a spreadsheet to an existing table in your application.
locale: en-US
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Enhance your app, Building apps in App Engine Studio, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Create a data model for your application

Create a data model in App Engine Studio \(AES\) for your application by creating the tables that will house your application data. Create data tables that will be used in your application by creating the table from scratch, uploading a spreadsheetor PDF, or by using an existing table as a template. You can also create and schedule data imports by mapping a spreadsheet to an existing table in your application.

Creating a data model and populating data into user interfaces are crucial starting points for any new application. Users may provide data, such as their name and phone number, when they fill in a form, and other users may refer to data as they fulfill a request.

In App Engine Studio, application data is stored in table format. When users update application data, they create a row or change an existing row in the table \(each row is also known as a data record\). You can create tables from existing ServiceNow AI Platform tables, from a spreadsheetor PDF, or customize a completely new table for your application to store records in.

The data records stored in your application may come from several sources. One table might store data records entered by users who are using your application, another might be populated via the import and mapping of data from a spreadsheet or through a script that updates data records with data from another ServiceNow AI Platform table.

## Application templates and data

Application templates automatically add data to your application. If you use a template to create your application, you can edit the tables that were added or add different tables.

## Forms

When you add data to your app, any associated form views display in the **Experience** section of your app. To edit the form, select it in the **Experience** section. Form views can be edited in the **Forms** tab of Table Builder. For more information, see [Forms in Table Builder](../../../administer/form-builder/concept/form-view-configuration.md).

## Table extension

There are several tables that your organization may already be using in other applications. For example, your organization may be using the Configuration item \[cmdb\_ci\] table for an application that houses configuration data. You can create a table for your application by extending any of these existing tables.

Table extension allows a table to share fields and records with a parent table. You might extend a table if you expect users to fill in similar fields across different form views in an application. For example, to create a ticketing type of table, you might extend the Task \[task\] table. The Task table includes fields that are standard for most work tickets, such as **Number** and **Assigned to**.

Many organizations create extensible standardized tables for their citizen developers to use when designing their apps. This enables the developers to standardize the way data is utilized across multiple applications within the organization.

To make a table in your application extensible, select **Make extensible** during table creation. After extending an existing table, you can further customize the new table by adding more columns.

The following table provides a list of commonly extended tables in the ServiceNow AI Platform. For more information on commonly extended tables and models for extension, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

<table id="table_o5c_hmf_25b"><thead><tr><th>

Table

</th><th>

Short Description

</th><th>

Description

</th></tr></thead><tbody><tr><td>

task

</td><td>

Task

</td><td>

Stores fields for the core applications such as Incident, Problem, and Change Management. It provides a series of standard fields used on each of the tables that extend it. Any table which extends the task table can take advantage of task-specific functionality for driving tasks.

</td></tr><tr><td>

cmdb\_ci

</td><td>

Configuration Item

</td><td>

Stores configuration items. This table can be extended for configuration items such as hardware, services, etc.

</td></tr><tr><td>

sn\_customerservice

 \_case

</td><td>

Customer Service Case

</td><td>

Stores customer service case records.

</td></tr><tr><td>

sm\_order

</td><td>

Service Order

</td><td>

Stores data that defines and manages work that needs to be performed.

</td></tr><tr><td>

sm\_task

</td><td>

Service Task

</td><td>

Stores units of work performed by one person in one session \(one location, one time\).

</td></tr><tr><td>

planned\_task

</td><td>

Planned Task

</td><td>

Stores additional fields for tasks pertaining to time and effort as part of a planned, multi-stage process.

</td></tr><tr><td>

cmn\_location

</td><td>

Location

</td><td>

Stores location information.

</td></tr><tr><td>

cmdb\_serviceorder

 \_product\_model

</td><td>

Service Order Model

</td><td>

Stores service order templates.

</td></tr><tr><td>

cmdb\_servicetask

 \_product\_mode

</td><td>

Service Task Model

</td><td>

Stores service task templates.

</td></tr><tr><td>

cmdb\_qb\_result

 \_base

</td><td>

Query Results

</td><td>

Stores query results created by the CMDB Query Builder.

</td></tr><tr><td>

alm\_asset

</td><td>

Asset

</td><td>

Stores general, financial, and contractual information about assets.

</td></tr><tr><td>

cmdb\_ci\_service

</td><td>

Business Service

</td><td>

Stores IT Services data that directly supports a business process.

</td></tr><tr><td>

sys\_user

</td><td>

User

</td><td>

Stores user data. The User table provides a list of all system users and their related department.

</td></tr><tr><td>

sys\_user\_group

</td><td>

User Group

</td><td>

Stores and groups a set of users who share a common purpose. Groups may perform tasks such as approving change requests, resolving incidents, receiving email notifications, or performing work order tasks.

</td></tr><tr><td>

core\_company

</td><td>

Company

</td><td>

Stores company information.

</td></tr><tr><td>

cmn\_schedule

</td><td>

Schedule

</td><td>

Stores records that specify a time zone and a type of schedule and use one or more schedule entries.

</td></tr><tr><td>

cmn\_department

</td><td>

Department

</td><td>

Stores a list of all departments and their related business unit.

</td></tr><tr><td>

cmn\_cost\_center

</td><td>

Cost Center

</td><td>

Stores cost center records. This is a reference between financial systems and IT. Cost center records represent business entities, and have a related list of CI Cost Center Relationships that measure the cost center's consumption of business services.

</td></tr><tr><td>

cmdb\_model

</td><td>

Product Model

</td><td>

Specific versions or various configurations of an asset. Models are used for managing and tracking assets through various ServiceNow platform asset applications, including Product Catalog, Asset Management, and Procurement.

</td></tr><tr><td>

life\_cycle\_stage

</td><td>

Life Cycle Stage

</td><td>

Stores standard fields and values for tracking life cycle stages for CIs. Using these standard values consistently across applications helps to effectively track assets through their life cycle transitions.

</td></tr><tr><td>

life\_cycle\_stage

 \_status

</td><td>

Life Cycle Status

</td><td>

Stores standard fields and values for tracking life cycle stage status for CIs. Using these standard values consistently across applications helps to effectively track assets through their life cycle transitions.

</td></tr><tr><td>

incident

</td><td>

Incident

</td><td>

Stores deviations from an expected standard of operation.

</td></tr><tr><td>

sysapproval

</td><td>

Approval

</td><td>

Stores data that allows you to require authorization on tasks before the work is done. You can define approvals for all tasks and associate users or groups to a task to approve or reject them.

</td></tr></tbody>
</table>Use the methods listed below to create a data model and add data to your application.

-   **[Create a blank table](../task/use-existing-table.md)**  
Add a data table to your application from an existing table that you or someone else previously created or from scratch.
-   **[Use a spreadsheet to add data](../task/upload-multi-sheets.md)**  
Add data tables and records to your application by uploading a Microsoft Excel spreadsheet.
-   **[Use a PDF to create data tables](pdf-extractor.md#)**  
Create tables from a PDF form using the PDF extractor tool in App Engine Studio.
-   **[Create a data integration](../task/import-map-data-existing-table.md)**  
Add new or updated information to your current data sets by importing it into existing tables in your application through the power of Integration Hub. Schedule future imports to add data at specific times.
-   **[Modify application data tables](edit-data.md)**  
Use Table Builder to modify data tables used in your application.

**Parent Topic:**[Enhance your app](customize-application.md)


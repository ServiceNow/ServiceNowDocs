---
title: Installed with Service Creator
description: Several types of components are installed with Service Creator.
locale: en-US
release: zurich
product: Service Creator
classification: service-creator
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Activate Service Creator, Service Creator, Build workflows]
---

# Installed with Service Creator

Several types of components are installed with Service Creator.

Demo data is available with Service Creator. The demo data provides the Departmental Services service catalog category.

Creating a new service category also creates [components for that service category](r_CompsCreatedWithNewSvcCategs.md).

The following components are added with [Service Creator](../concept/c_ServiceCreator.md):

## Tables

|Table|Description|
|-----|-----------|
|Service Category \[catalog\_category\_request\]|Stores all [service categories](../task/t_ManagingServices.md).|
|Service Category Request User \[catalog\_category\_request\_user\]|Tracks fulfillers for a service category. Use these records to grant or remove roles as needed.|
|Service \[sc\_cat\_item\_producer\_service\]|Stores all services.|
|Service Category App Menu \[service\_category\_app\_menu\]|Stores the application menus for each service category.|
|Service Category User Role \[service\_category\_user\_role\]|Tracks users who have been granted a role due to being an editor of a service category.|

## UI actions

|UI action|Description|
|---------|-----------|
|Create Category and Table|Approves a requested service category and creates system components for that category.|
|Request Category Publication|Lets a service creator request their category be published.|
|Create New Service|Creates a new service within the service category.|
|View Table Definition|Opens the task table definition \[sys\_db\_object\] for a service category.|
|View Task List|Opens the list of tasks associated with the service category.|

## UI policies

|UI policy|Description|
|---------|-----------|
|Hide Due Date|Hides the Due date field on the Service Category form if State is Requested or Due date is empty.|
|Hide Category If Empty|Hides the Category field, if empty, on the Service Category form.|
|Show Published|Shows the Published check box on the Service Category form if State is Created but Unpublished or Ready for Publication.|
|Hide Table name|Shows Table and hides Table name on the Service Category form if Table has a value.|
|Hide Category Name|Hides Name on the Service Category form if State is Requested or Rejected.|
|Table name read only|Makes Department and Table name read only on the Service Category form if State is not Requested.|
|Hide Editors|Hides the Editors field on the Service Category form if State is Requested or Rejected.|

## Properties

<table id="table_wy2_flx_3q"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

glide.citizen\_developer.category.auto\_publish

</td><td>

Automatically adds new service categories to the service catalog as subcategories of the Departmental Services category.-   Type: true\|false
-   Default value: true
-   Location: System Properties \[sys\_properties\] table

</td></tr><tr><td>

glide.citizen\_developer.set\_category\_roles

</td><td>

Comma-separated list of roles that can set the category for a new service.-   Type: String
-   Default value: admin, catalog\_admin
-   Location: System Properties \[sys\_properties\] table

</td></tr><tr><td>

glide.service\_creator.auto\_add\_to\_category

</td><td>

Automatically adds new services to the Departmental Services service catalog category, in addition to the department-specific category.-   Type: true\|false
-   Default value: true
-   Location: System Properties \[sys\_properties\] table

</td></tr></tbody>
</table>## Script includes

|Script include|Description|
|--------------|-----------|
|serviceCategoryIsUnpublished|Global function that returns true if the service category is unpublished.|
|getMyCatalogCategories|Global function that returns a list of categories for which the current user is the manager or an editor.|

## Client scripts

|Client script|Description|
|-------------|-----------|
|Duplicate Category Name Check|Displays a warning on the Service Category Request form when the requested service category has the same name as an existing service category.|
|Fix Table Name|Ensures a valid table name on the Service Category Request form.|
|Hide Draft Services|Hides the Draft Services related list on the Service Category Request form when appropriate.|
|Propose Table Name|Proposes a valid table name on the Service Category Request form for new service category requests.|
|Category Published|Displays a help message when Published is selected on the Service Category Request form.|
|Hide Fulfillers|Hides the Fulfillers related list on the Service Category Request form when appropriate.|
|Editors Message|Displays a help message for the Editors field when appropriate.|
|Other Tables Message|Provides information about existing service category tables for the selected Department.|
|State Message|Displays a help message for the State field.|

## Business rules

|Business rule|Description|
|-------------|-----------|
|Service Query|Restricts users without the catalog\_admin role to viewing service records within service categories they are the manager or editor of.|
|New Service|Provides a message when a new sc\_cat\_item\_producer\_service record is created.|
|Table Name Required|Ensures a service category request has a valid table name before approval.|
|Remove Fulfiller Role|Removes relevant role from service fulfillers when they are removed from a category.|
|Category Request query|Restricts users without the catalog\_admin role to viewing service category records they are a manager or editor of.|
|Editor Role|Adds and removes relevant roles from service category editors.|
|Delete User Role|Removes the relevant role from service category editors when appropriate.|
|Category Published|Sets State to Published to Catalog when the Published check box is selected on the Service Category Request form.|
|Populate Service Name if Empty|Populates a service name if none is provided.|
|Add Departmental Services Category|Adds a new service to the Departmental Services service catalog category.|
|Default Fulfillment User|Makes a category manager the assignee of service tasks if no assignee is specified.|
|Scratchpad Draft Services Count|Generates field help messages.|
|Catalog Category Request Approved|Creates components necessary to use of a new service category.|
|Manager Role|Grants relevant roles to category managers.|
|New Service Script|Populates the script of a new Service to set assignment group or user.|
|getDepartmentUsers|Returns the users of a department.|
|Draft Item Query|Restricts users without the catalog\_admin role to viewing draft service records they are a manager or editor of.|
|Grant Fulfiller Role|Grants relevant role to service fulfillers.|
|Scratchpad Department Name|Generates field help messages.|
|Scratchpad|Generates field help messages.|
|Other Tables For Department|Generates field help messages.|
|Set Single Catalog from Single Category|Populates a default Catalog for a new service.|

## Email notifications

|Name|Description|
|----|-----------|
|Service Category Published|Notifies the manager of a service category when the category request is approved.|
|Service Category Rejected|Notifies the manager of a service category when the category request is rejected.|
|Service Category Request Inserted|Notifies catalog administrators when a new category request is created.|
|Service Category Created|Notifies the manager of a service category when the category is created.|
|Service Category Publication Requested|Notifies catalog administrators when publication of a category has been requested.|
|Service Category Request Opened|Notifies the manager of a service category when a new category request is created on their behalf.|


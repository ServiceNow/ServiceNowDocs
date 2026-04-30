---
title: Create a record producer to log incidents
description: Create record producers to log incidents directly from Service Catalog.
locale: en-US
release: xanadu
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Incident templates and record producers, Configure, Incident Management, IT Service Management]
---

# Create a record producer to log incidents

Create record producers to log incidents directly from Service Catalog.

## Before you begin

Role required: catalog\_admin or admin

## About this task

Incident record producers provide users with an interface from which user can log an incident. For example, the default **Can We Help You?** category features record producers such as **Create Incident** to enable users to log incidents from the catalog.

The following example demonstrates how to create a record producer to request a wireless router reset.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Click **New** and complete the steps in [Create a record producer](https://www.servicenow.com/docs/access?context=t_DefRecProdInSCat&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) using the following information:

    |Field|Entry|
    |-----|-----|
    |Name|`Request to Reset Router`|
    |Table name|Incident \[incident\]|
    |What it will contain|
    |Short description|`Reset wireless router request`|
    |Description|`Please reset the building's router`|
    |Accessibility|
    |Catalogs|Service Catalog|
    |Category|Can We Help You?|

    ![Record producer](../image/record-producer.png)

3.  Right-click on the form header and from the context menu select **Save**.

    Several related lists appear at the end of the form, including Variables and Variable Sets.

4.  In the Variables related list, click **New**.

5.  On the form, fill in the fields.

    |Field|Entry|
    |-----|-----|
    |Type|Reference|
    |Question|
    |Question|`Which router needs to be reset?`|
    |Name|Router|
    |Type Specifications|
    |Reference|IP Router \[cmdb\_ci\_ip\_router\]|

    ![Variables related list](../image/record-producer2.png)

6.  Click **Submit**.

7.  To view the new record producer, click **Try It** in the form header.

    In Service Catalog, the new catalog item appears and any user can select it.


**Parent Topic:**[Incident templates and record producers](../concept/incident-templates-record-producers.md)

**Related topics**  


[Create incident template](t_CreateAnIncidentTemplate.md)

[Create a module that uses incident template](t_UseATemplateFromAModule.md)

[Create a record producer using a template](t_CreateRecProducWithTempl.md)


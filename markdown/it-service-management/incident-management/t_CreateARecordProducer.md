---
title: Create a record producer to log incidents
description: Create record producers to log incidents directly from Service Catalog.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-service-management/incident-management/t\_CreateARecordProducer.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Incident templates and record producers, Configuring Incident Management, Incident Management, IT Service Management]
---

# Create a record producer to log incidents

Create record producers to log incidents directly from Service Catalog.

## Before you begin

Role required: catalog\_admin or admin

## About this task

Incident record producers provide users with an interface from which users can log an incident. For example, the default **Can We Help You?** category features record producers such as **Create Incident** to enable users to log incidents from the catalog.

The following example demonstrates how to create a record producer to request a wireless router reset.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Select **New** and complete the steps in [Create a record producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/t_DefRecProdInSCat.md) using the following information:

    |Field|Value|
    |-----|-----|
    |Name|`Request to Reset Router`|
    |Table name|Incident \[incident\]|
    |What it will contain|
    |Short description|`Reset wireless router request`|
    |Description|`Please reset the building's router`|
    |Accessibility|
    |Catalogs|Service Catalog|
    |Category|Can We Help You?|

    \[Omitted image "record-producer.png"\] Alt text: Record Producer form filled in with the values for the router reset request

3.  Select the **Additional Action** \(\[Omitted image "additional-actions.png"\] Alt text: Additional Action Menu icon\) icon and then select **Save**.

    Several related lists appear at the end of the form, including Variables and Variable Sets.

4.  In the Variables related list, select **New**.

5.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Type|Reference|
    |Question|
    |Question|`Which router needs to be reset?`|
    |Name|Router|
    |Type Specifications|
    |Reference|IP Router \[cmdb\_ci\_ip\_router\]|

    \[Omitted image "record-producer2.png"\] Alt text: Variables related list

6.  Select **Submit**.

7.  To view the new record producer, select **Try It** in the form header.

    In Service Catalog, the new catalog item appears and any user can select it.


**Parent Topic:**[Incident templates and record producers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-service-management/incident-management/incident-templates-record-producers.md)

**Related topics**  


[Create an incident template]()

[Create a module that uses an incident template]()

[Create a record producer using a template]()


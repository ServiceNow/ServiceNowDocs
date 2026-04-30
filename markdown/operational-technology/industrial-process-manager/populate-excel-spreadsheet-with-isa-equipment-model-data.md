---
title: Populating your Microsoft Excel spreadsheet with equipment model data
description: Create and populate a Microsoft Excel spreadsheet with your existing ISA equipment model data. Positioning your existing data in the correct columns is crucial to the success of your upload.
locale: en-US
release: xanadu
product: Industrial Process Manager
classification: industrial-process-manager
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Importing equipment model data, Configure, Industrial Process Manager, Operational Technology]
---

# Populating your Microsoft Excel spreadsheet with equipment model data

Create and populate a Microsoft Excel spreadsheet with your existing ISA equipment model data. Positioning your existing data in the correct columns is crucial to the success of your upload.

To create a Microsoft Excel spreadsheet that properly populates the Configuration Management Database \(CMDB\) in the ServiceNow AI Platform, do the following actions:

1.  Prepare your spreadsheet for upload by using the Microsoft Excel spreadsheet that is attached to the data source record. To locate an empty template, do the following actions:

    1.  Navigate to **Equipment Model - ISA** &gt; **Import Equip. Model - Data Source**
    2.  Click **Import Equipment Model – Data Source - v2.xlsx**
    **Note:** Alternately, to download the **Import Equipment Model – Data Source - v2.xlsx** spreadsheet, see the [Microsoft Excel spreadsheets required for the ISA Equipment Model Excel Service Graph Connector \[KB0966600\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0966600) article in the Now Support Knowledge Base.

2.  Download the attached Import Equipment Model – Data Source - v2.xlsx spreadsheet to learn more about the template and its worksheets:

    **Note:** If you're an ISA SGC user upgrading from v1 to v2, see the section named **Upgrading from v1 to v2** below.

    |Worksheet name|Purpose|
    |--------------|-------|
    |Blank template for data import|Populates your Equipment Model data for import. You can view detailed examples in the remainder of this topic.|
    |Data Column Descriptions|Provides descriptions of the data columns on the spreadsheet, similar to the information found in this topic.|
    |Sample Data for Import|Provides an example of an equipment model for import in the spreadsheet. You can view these examples in the remainder of this topic.|

3.  After populating the Microsoft Excel spreadsheet, save it in a known location for easy access when you run the Integration Hub ETL function.

    **Note:** Column names cannot be changed. You can add additional columns to support additional fields to uniquely identify owners, as designated in the **sn\_isa\_model.user\_search\_matching\_attribute** system property.


## Populating the spreadsheet

You can import data from multiple sites in a single spreadsheet. The example image shows data for two sites: ATL and CTL.

![Sample Operational Technology data, columns A through J.](../image/aug-23-sample-import-equipment-model-data-source.png "Sample Operational Technology data, columns A through J")

<table id="table_mch_2cc_txb"><thead><tr><th>

Column

</th><th>

Name

</th><th>

Type

</th><th>

Description

</th><th>

Required

</th></tr></thead><tbody><tr><td>

A

</td><td>

Path

</td><td>

string

</td><td>

Concatenation of the short codes of this entity and all its parent entities. For example, `ATL-B42-MQSTOR-Z1` is the concatenation of these short codes: -   ATL short code for the Atlanta site.
-   B42 short code for Building B42.
-   MQSTORE short code for Model M and Q.
-   Z1 short code for the Zone 1 transfer storage zone for Model M and Q.

</td><td>

Yes

</td></tr><tr><td>

B

</td><td>

Short Code

</td><td>

string, alphanumeric only

</td><td>

Short description code for the entity. Refer to the previous Path column description for examples of short codes.The Short Code can be no longer than the maximum length that is designated in the **sn\_isa\_model.short\_code\_validation\_max\_length** system property.

</td><td>

No

</td></tr><tr><td>

C

</td><td>

Entity Name

</td><td>

string

</td><td>

Long name of the entity. For example, a city name, a building number, or a model number.

</td><td>

Yes

</td></tr><tr><td>

D

</td><td>

Location

</td><td>

string

</td><td>

Location of the entity. For example, you would list Atlanta Building 64 for each of the equipment models that are located there. The cmn-location value that is stored in the Configuration Management Database \(CMDB\) in the ServiceNow AI Platform, which uses it as a reference.

</td><td>

No

</td></tr><tr><td>

E

</td><td>

Assigned to

</td><td>

string

</td><td>

Email address of the assigned person who owns and manages this entity record. **Note:** You can use additional attributes, based on the settings designated in the **sn\_isa\_model.user\_search\_matching\_attribute** system property.

</td><td>

No

</td></tr><tr><td>

F

</td><td>

Support Group

</td><td>

string

</td><td>

Name of the group that supports the maintenance and management of this entity.

</td><td>

No

</td></tr><tr><td>

G

</td><td>

Description

</td><td>

string

</td><td>

Long description of this equipment model entity and its purpose.

</td><td>

No

</td></tr><tr><td>

H

</td><td>

Process criticality

</td><td>

string

</td><td>

Measure of how critical, or important, the entity is to the industrial process. Examples are as follows:-   1 - most critical.
-   2 - somewhat critical.

</td><td>

No

</td></tr><tr><td>

I

</td><td>

Company

</td><td>

string

</td><td>

Name of the company that the entity belongs to. The cmn-location value that is stored in the CMDB in the ServiceNow AI Platform, which uses it as a reference.

</td><td>

No

</td></tr><tr><td>

J

</td><td>

Template

</td><td>

string

</td><td>

The template used to import data. **Note:** After your import your data, you cannot set the template.

</td><td>

Yes

</td></tr></tbody>
</table>## Upgrading from v1 to v2

If you're an ISA SGC user upgrading from v1 to v2, you can import new ISA equipment model entities that have a unique path and update existing ISA equipment model entities that already have a path value with a fix script.

**Parent Topic:**[Importing equipment model data](importing-isa95-equipment-model-etl.md)


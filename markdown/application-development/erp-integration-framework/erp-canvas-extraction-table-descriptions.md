---
title: ERP Data Hub extraction table field descriptions
description: The Extraction table form in ERP Data Hub enables you to create and edit extraction tables in the ERP \(Enterprise Resource Planning\) model.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [ERP Data Hub field descriptions, ERP Data Hub reference, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# ERP Data Hub extraction table field descriptions

The Extraction table form in ERP Data Hub enables you to create and edit extraction tables in the ERP \(Enterprise Resource Planning\) model.

<table id="table_cv1_h3z_wxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the ERP extraction table.

</td></tr><tr><td>

ERP model

</td><td>

ERP model for the extraction table source, which must be configured for you to select.

</td></tr><tr><td>

Table transform map

</td><td>

Table that the extracted data is cached and stored in.The transform table is a temporary table that holds data during the data integration or transformation process. Transform tables are an intermediary step before data is further processed, cleaned, or loaded into the target destination.

The specified Glide table connects the source ERP extraction table and the target table for the extracted data.

If you use a custom transform table, you must first create the table on the ServiceNow AI Platform, and the table must be in the application scope. For more information on creating table transform maps, see [Create a transform map](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

ERP module

</td><td>

Name of the ERP module linked to the ERP extraction table, which is controlled by the ERP model.

</td></tr><tr><td>

Table transform map link

</td><td>

Link to the Glide table that the extracted ERP data is cached and stored in.After you save the extraction table, when you select the link, the ServiceNow AI Platform table opens in a new browser tab.

</td></tr><tr><td>

System

</td><td>

ERP system that the ETL \(extract, transform, and load\) process extracts data from on the system of record. The system must already be configured.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the ETL source.

</td></tr><tr><td>

Long text

</td><td>

Any additional text to describe the ERP extraction table.

</td></tr><tr><td>

Comments

</td><td>

Public comment that is visible to anyone working on the ERP extraction table.

</td></tr><tr><td>

Work notes

</td><td>

Private notes that only you can view.

</td></tr></tbody>
</table>**Parent Topic:**[ERP Data Hub field descriptions](erp-canvas-field-descriptions.md)


---
title: Zero Copy Connector for ERP extraction table field descriptions
description: The Extraction table form in Zero Copy Connector for ERP enables you to create and edit extraction tables in the ERP \(Enterprise Resource Planning\) model.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Zero Copy Connector for ERP field descriptions, Zero Copy Connector for ERP reference, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Zero Copy Connector for ERP extraction table field descriptions

The Extraction table form in Zero Copy Connector for ERP enables you to create and edit extraction tables in the ERP \(Enterprise Resource Planning\) model.

For process details, see [Add a new ERP extraction table in Zero Copy Connector for ERP](../task/erp-canvas-add-new-extraction-table.md).

<table id="table_cv1_h3z_wxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the ERP extraction table.

</td></tr><tr><td>

Table transform map

</td><td>

Table that the extracted data is cached and stored in.The transform table is a temporary table that holds data during the data integration or transformation process. Transform tables are an intermediary step before data is further processed, cleaned, or loaded into the target destination.

The specified Glide table connects the source ERP extraction table and the target table for the extracted data.

If you use a custom transform table, you must first create the table on the ServiceNow AI Platform, and the table must be in the application scope. For more information on creating table transform maps, see [Create a transform map](https://www.servicenow.com/docs/access?context=t_CreateATransformMap&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US).

</td></tr><tr><td>

Table transform map link

</td><td>

Link to the Glide table that the extracted ERP data is cached and stored in.After you save the extraction table, when you select the link, the ServiceNow AI Platform table opens in a new browser tab.

</td></tr><tr><td>

ERP model

</td><td>

ERP model for the extraction table source, which must be configured for you to select.

</td></tr><tr><td>

ERP module

</td><td>

Name of the ERP functional area in the system of record. For example, logistics, procurement, or sales.

</td></tr><tr><td>

Target table link

</td><td>

Link to the final table in which the extracted ERP data resides.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the ETL source.

</td></tr><tr><td>

Long text

</td><td>

Any additional text to describe the ERP extraction table.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)


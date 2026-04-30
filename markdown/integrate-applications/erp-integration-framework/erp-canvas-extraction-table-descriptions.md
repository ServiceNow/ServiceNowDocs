---
title: Zero Copy Connector for ERP extraction table field descriptions
description: The Extraction table form in Zero Copy Connector for ERP enables you to create and edit extraction tables in the ERP \(Enterprise Resource Planning\) model.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, extraction, table]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
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

Map specifying the data relationships between the import set and the target table.

</td></tr><tr><td>

Target table link

</td><td>

A link to the table in which you want the transformed data to be added.

</td></tr><tr><td>

Application

</td><td>

Application scope: global or per application.

</td></tr><tr><td>

ERP model

</td><td>

ERP model for the extraction table source, which must be configured for you to select.

</td></tr><tr><td>

ERP module

</td><td>

ERP module in the system of record, for example, sales orders or inventory. Select a module from the list. If the module you need isn't listed, contact [ServiceNow Technical Support](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547260).

 ERP modules represent a distinct set of features and functionalities tailored to address business processes or activities.

</td></tr><tr><td>

Page size

</td><td>

Amount of data to read from the ERP system at a time. The default is 1000. Increasing the size may impact MID Server memory space.

</td></tr><tr><td>

Table transform map link

</td><td>

Link to the Glide table that the extracted ERP data is cached and stored in.After you save the extraction table, when you select the link, the ServiceNow AI Platform table opens in a new browser tab.

</td></tr><tr><td>

Short description

</td><td>

Brief description of the extraction table.

</td></tr><tr><td>

Long text

</td><td>

A longer description or information about the extraction table.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)


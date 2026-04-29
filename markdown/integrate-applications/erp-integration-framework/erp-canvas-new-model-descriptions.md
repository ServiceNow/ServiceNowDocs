---
title: Zero Copy Connector for ERP new model field descriptions
description: The new model form in Zero Copy Connector for ERP contains details for the ERP \(Enterprise Resource Planning\) model.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, new]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP new model field descriptions

The new model form in Zero Copy Connector for ERP contains details for the ERP \(Enterprise Resource Planning\) model.

For process details, see [Create a new ERP model](../task/erpc-add-new-data-model.md).

<table id="table_vvj_5fy_v2c"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

Model name

</td><td>

Name of the ERP model.

</td></tr><tr><td>

ERP module

</td><td>

ERP module in the system of record, for example, sales orders or inventory. Select a module from the list. If the module you need isn't listed, contact [ServiceNow Technical Support](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547260).

 ERP modules represent a distinct set of features and functionalities tailored to address business processes or activities.

</td></tr><tr><td>

ERP system

</td><td>

ERP system the ERP model connects to.The connected ERP system enables access to information about fields and tables and interaction between the model and the connected ERP system. For more information, see [Create an ERP system in Zero Copy Connector for ERP](../task/create-an-erp-system.md) and [View a list of Zero Copy Connector for ERP systems](../task/view-and-monitor-erp-systems-health.md).

</td></tr><tr><td>

Application

</td><td>

Application scope the ERP model is linked to. For example, if you create a custom model, the model will be in that scope.

</td></tr><tr><td>

Model type

</td><td>

-   Platform model: Model with input and output fields mapped to an already existing platform table. These models standardize ERP data by mapping it to ServiceNow standardized platform tables.
-   ERP model: New, custom ERP model. These models follow the data structures defined by the connected, external ERP system. ERP models accommodate the unique formats of each ERP system.

</td></tr><tr><td>

Platform table \(only visible if Platform model is selected in **Model type**\)

</td><td>

Specify the table to use with this model.

</td></tr><tr><td>

Short description

</td><td>

Brief description of what the ERP model represents.

</td></tr><tr><td>

Long text

</td><td>

A longer description or information about the ERP data model.

</td></tr><tr><td>

ERP software

</td><td>

Supportability of the model. This field is required because it determines which models can be used with a system. When you create or update a model and specify an ERP system, the software linked to that system is automatically added to this field. You can select additional options from the list. The list contains major SAP versions and doesn't include patch versions. When a model is exported, the ERP software information specified here is included.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)


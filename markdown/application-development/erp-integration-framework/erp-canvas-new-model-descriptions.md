---
title: Zero Copy Connector for ERP new model field descriptions
description: The new model form in Zero Copy Connector for ERP contains details for the ERP \(Enterprise Resource Planning\) model.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Zero Copy Connector for ERP field descriptions, Zero Copy Connector for ERP reference, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Zero Copy Connector for ERP new model field descriptions

The new model form in Zero Copy Connector for ERP contains details for the ERP \(Enterprise Resource Planning\) model.

For process details, see [Add a new ERP model](../task/erpc-add-new-data-model.md).

<table id="table_vvj_5fy_v2c"><thead><tr><th>

Field

</th><th>

Definition

</th></tr></thead><tbody><tr><td>

ERP model name

</td><td>

Name of the ERP model.

</td></tr><tr><td>

ERP module

</td><td>

ERP module in the system of record, for example, sales orders or inventory. Select a module from the list. If the module you need is not listed, contact [ServiceNow Technical Support](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547260).

 ERP modules represent a distinct set of features and functionalities tailored to address business processes or activities.

</td></tr><tr><td>

ERP System

</td><td>

ERP system the ERP model connects to.The connected ERP system enables access to information about field and tables and interaction between the model and the connected ERP system. For more information, see [Create an ERP system in Zero Copy Connector for ERP](../task/create-an-erp-system.md) and [View a list of Zero Copy Connector for ERP systems](../task/view-and-monitor-erp-systems-health.md).

</td></tr><tr><td>

Application

</td><td>

Application scope the ERP model is linked to. For example, if you create a custom model, the model will be in that scope.

</td></tr><tr><td>

Short description

</td><td>

Brief description of what the ERP model represents.

</td></tr><tr><td>

Long text

</td><td>

A longer description or information about the ERP data model.

</td></tr><tr><td>

ERP softwares

</td><td>

Supportability of the model. This field is mandatory because it determines which models can be used with a system. When you create or update a model and specify an ERP system, the software linked to that system is automatically added to this field. You can select additional options from the list. The list contains SAP major versions and does not include patch versions. When a model is exported, the ERP software information specified here is included.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)


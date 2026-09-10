---
title: Zero Copy Connector for ERP new model field descriptions
description: The new model form in Zero Copy Connector for ERP contains details for the enterprise resource planning \(ERP\) model.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-new-model-descriptions.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 2
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, model, new]
breadcrumb: [Field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP new model field descriptions

The new model form in Zero Copy Connector for ERP contains details for the enterprise resource planning \(ERP\) model.

For process details, see [Create a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-add-new-data-model.md).

<table id="table_vvj_5fy_v2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model name

</td><td>

Name of the ERP model.

</td></tr><tr><td>

ERP module

</td><td>

ERP module in the ERP system, for example, sales orders or inventory. Select a module from the list. If the module you need is not listed, contact [ServiceNow Technical Support](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547260).

 Each ERP module represents a distinct set of features and functions tailored to address business processes or activities.

</td></tr><tr><td>

ERP system

</td><td>

ERP system the ERP model connects to.The connected ERP system provides access to field and table information, and enables interaction between the model and the ERP system. For more information, see [Create an ERP system in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/create-an-erp-system.md) and [View a list of Zero Copy Connector for ERP systems](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/view-and-monitor-erp-systems-health.md).

</td></tr><tr><td>

Keep mapped values the same as ERP field name

</td><td>

Select this option if you don't need suggested mapped values for this model. For more information, see [Edit input and output mapped value name in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-edit-mapped-value-name-in-model-manager.md).

</td></tr><tr><td>

Application

</td><td>

Application scope the ERP model is linked to. For example, if you create a custom model, the model is in that scope.

</td></tr><tr><td>

Model type

</td><td>

-   Platform model: Model with input and output fields mapped to an existing platform table. These models standardize ERP data by mapping it to ServiceNow AI Platform® standardized platform tables.
-   ERP model: New, custom ERP model. These models follow the data structures defined by the connected, external ERP system. ERP models accommodate the unique formats of each ERP system.

</td></tr><tr><td>

Platform table \(only visible if Platform model is selected in **Model type**\)

</td><td>

Table to use with this model.

</td></tr><tr><td>

Short description

</td><td>

Brief description of what the ERP model represents.

</td></tr><tr><td>

Long text

</td><td>

Longer description or more information about the ERP data model.

</td></tr><tr><td>

ERP software

</td><td>

Supportability of the model. This field determines which models can be used with a system. When you create or update a model and specify an ERP system, the software linked to that system is automatically added to this field. You can select additional options from the list. For SAP, the list contains major SAP versions and does not include patch versions. When a model is exported, the ERP software information specified here is included.

</td></tr></tbody>
</table>
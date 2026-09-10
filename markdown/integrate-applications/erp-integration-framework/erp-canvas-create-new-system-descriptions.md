---
title: Zero Copy Connector for ERP system details field descriptions
description: The system details tab in Zero Copy Connector for ERP \(Enterprise Resource Planning\) contains connection information for an ERP system.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-canvas-create-new-system-descriptions.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-08-06"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, system, oracle, ebs]
breadcrumb: [Field descriptions, Reference, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Zero Copy Connector for ERP system details field descriptions

The system details tab in Zero Copy Connector for ERP \(Enterprise Resource Planning\) contains connection information for an ERP system.

For process details, see [Create an ERP system in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/create-an-erp-system.md).

<table id="table_obh_qgd_5xb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP system

</td><td>

Name of the ERP system to help identify the business area.

</td></tr><tr><td>

Short description

</td><td>

Brief description of what the ERP system is for.

</td></tr><tr><td>

Connection

</td><td>

Alias of the connection credential that you configured to connect to the ERP system. You can select only from connections in the Zero Copy Connector for ERP scope.

</td></tr><tr><td>

ERP software

</td><td>

The supported ERP software on the system. Select one or more options from the list, for example, ECC 7.5 and SAP S/4HANA 2021. For SAP, the list contains major SAP versions and doesn't include patch versions.

 The list also contains Oracle E-Business Suite \(EBS\), version 12.2 or later. Oracle E-Business Suite systems support REST only. For more information, see [Oracle E-Business Suite support in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-overview.md).

</td></tr><tr><td>

Virtual schema name

</td><td>

Identifier for the ERP system that you use to run a model through the API. This value is generated when the system record is first saved and can't be edited.

</td></tr><tr><td>

KB link \(on heartbeat tabs after system record is first saved\)

</td><td>

Link to a relevant knowledge base article, when an error occurs and an article is available.

</td></tr><tr><td>

Status \(on heartbeat tabs after system record is first saved\)

</td><td>

State of the heartbeat: **Success**, **Failed**, or **Not connected**.

</td></tr><tr><td>

Error text \(on heartbeat tabs after system record is first saved\)

</td><td>

Details about any errors that have occurred.

</td></tr><tr><td>

Updated \(on heartbeat tabs after system record is first saved\)

</td><td>

Date and time when the heartbeat was last changed.

</td></tr></tbody>
</table>
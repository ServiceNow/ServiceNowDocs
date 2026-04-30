---
title: ERP Semantic Mining candidate scan results field descriptions
description: On a candidate record in ERP Semantic Mining the ERP scan results tab displays information about the latest scan of the ERP \(Enterprise Resource Planning\) system.
locale: en-US
release: zurich
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ERP Semantic Mining field descriptions, Reference, ERP Semantic Mining overview, Workflow Data Fabric]
---

# ERP Semantic Mining candidate scan results field descriptions

On a candidate record in ERP Semantic Mining the **ERP scan results** tab displays information about the latest scan of the ERP \(Enterprise Resource Planning\) system.

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

For process details, see [View and work with candidate details in ERP Semantic Mining](../task/erpcm-view-work-with-candidate-details.md).

<table id="table_oh5_w2p_jyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP model

</td><td>

Relevant ERP model that the candidate uses, which is configured in Zero Copy Connector for ERP.Select an ERP model to open the model in Zero Copy Connector for ERP.

</td></tr><tr><td>

Closest ERP model/Extensible model

</td><td>

The suggested closest matching ERP model that you can add the table to in Zero Copy Connector for ERP.This column is helpful for custom tables, which aren't part of a standard ERP model and therefore don't have a table listed in the **ERP model** column. Select an ERP model to open the model in Zero Copy Connector for ERP.

</td></tr><tr><td>

Technical cluster

</td><td>

If the field is empty, the table is an ordinary, non-technical table. If the field contains a value, the table belongs to a technical group and is disregarded in the candidate identification analysis.

</td></tr><tr><td>

ERP table name

</td><td>

Name of the table on the ERP system.

</td></tr><tr><td>

Table operation

</td><td>

Action that ERP Semantic Mining took on the scanned table: Create, Read, Update, or Delete.

</td></tr><tr><td>

Max number of rows \(DB\)

</td><td>

Maximum number of rows on the scanned table, which is useful for knowing candidate limitations.

</td></tr><tr><td>

Updated

</td><td>

Date and time the table was most recently scanned.

</td></tr></tbody>
</table>**Parent Topic:**[ERP Semantic Mining field descriptions](../concept/erpcm-field-description-reference-landing.md)


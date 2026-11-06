---
title: Product resolution skill - Triggers and inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/product-resolution-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Product resolution skill - Triggers and inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.

## Triggers for the Product resolution skill

The following table lists the trigger for the Product resolution skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|The skill runs automatically when more than one product passes Product Match Review for a single raw product. If only one product passes, the skill is not called.|

## Inputs for the Product resolution skill

The following table lists the input for the Product resolution skill.

<table id="table_inputs_stns"><thead><tr><th>

Input

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Software Raw Product \[samp\_raw\_product\]

 SAM Product \[samp\_sw\_product\]

</td><td>

The skill reads the raw product name as the source product, along with the name and description of each candidate SAM product that passed Product Match Review.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)


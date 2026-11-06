---
title: Software normalization skill - Triggers and Inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/software-normalization-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Software normalization skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.

## Triggers for the Software normalization skill

The following table lists the trigger for the Software normalization skill.

<table id="table_triggers_stns"><thead><tr><th>

Trigger

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Standard Excel import**Note:** Triggers only when the source entitlement import Excel file contains an unresolved error for a Publisher or Product value and the standard content match process has failed to resolve it.

</td><td>

The Product and Publisher data in the source Excel file don't match the Content Library data.

</td></tr></tbody>
</table>## Inputs for the Software normalization skill

The following table lists the input for the Software normalization skill.

|Input|Description|
|-----|-----------|
|Raw Publisher and Product value from source Excel file|Publisher and Product value given in standard Excel that are unresolved through standard Content Library match.|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)


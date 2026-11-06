---
title: Spend transaction software normalization skill - Triggers and Inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/spend-txn-normalization-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Spend transaction software normalization skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.

## Triggers for the Spend transaction software normalization skill

The following table lists the trigger for the Spend transaction software normalization skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|The skill normalizes the raw publisher and raw product after the Spend transaction software classification skill identifies a transaction as software. When a match is found in existing publisher and product records, the skill populates the Publisher and Product fields on the spend transaction record.|

## Inputs for the Spend transaction software normalization skill

The following table lists the input for the Spend transaction software normalization skill.

|Input|Description|
|-----|-----------|
|Extracted publisher and product values|Raw publisher and product produced by the Spend transaction software classification skill for transactions identified as software.|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)


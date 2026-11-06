---
title: Spend transaction software classification skill - Triggers and Inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to classify spend transactions. A trigger initiates an action, such as when the system classifies spend transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/spend-txn-classification-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Spend transaction software classification skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to classify spend transactions. A trigger initiates an action, such as when the system classifies spend transactions.

## Triggers for the Spend transaction software classification skill

The following table lists the trigger for the Spend transaction software classification skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|The skill classifies spend transactions as part of the spend transaction import pipeline through the SAM - Label Spend Transactions scheduled job. The job processes batches of transactions that haven't yet been classified.|

## Inputs for the Spend transaction software classification skill

The following table lists the input for the Spend transaction software classification skill.

|Input|Description|
|-----|-----------|
|Software Spend Transactions \[sam\_spend\_transaction\]|The skill reads the vendor name, transaction description, and GL account fields from imported spend transaction records.|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)


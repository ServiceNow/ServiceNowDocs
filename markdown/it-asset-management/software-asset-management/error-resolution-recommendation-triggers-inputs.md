---
title: Error resolution recommendation skill - Triggers and Inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate error resolution recommendations. A trigger initiates an action, such as when the system generates error resolution recommendations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/error-resolution-recommendation-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-11-06"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Error resolution recommendation skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to generate error resolution recommendations. A trigger initiates an action, such as when the system generates error resolution recommendations.

## Triggers for the Error resolution recommendation skill

The following table lists the trigger for the Error resolution recommendation skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Resolution recommendations are automatically generated after the Error log summarization skill produces an error summary.|

## Inputs for the Error resolution recommendation skill

The following table lists the inputs for the Error resolution recommendation skill.

|Input|Description|
|-----|-----------|
|Error summary|Consolidated error signature such as status codes, messages, failing action, and profile context that is produced by the Error log summarization skill.|
|Web search results|External guidance, vendor documentation, and API deprecation or known-issue references that are matched to the error signature.|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)


---
title: Publisher match review - Triggers and inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/publisher-match-review-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Publisher match review - Triggers and inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.

## Triggers for the Publisher match review skill

The following table lists the trigger for the Publisher match review skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Candidate publisher matches are reviewed automatically once the matching logic creates them in SAM Publisher Mapping Results table. The skill accepts or rejects each match.|

## Inputs for the Publisher match review skill

The following table lists the input for the Publisher match review skill.

|Input|Description|
|-----|-----------|
|SAM Publisher Mapping Result \[samp\_publisher\_mapping\_result\]|The skill reads each candidate match: the raw publisher name and its sample products, and the SAM publisher's name, webpage and sample products \[samp\_sw\_publisher\] and responds if its a match or not.|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)


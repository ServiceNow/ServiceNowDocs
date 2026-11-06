---
title: Product match review skill - Triggers and Inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/now-assist-for-software-asset-management-sam/product-match-review-triggers-inputs.html
release: zurich
product: Now Assist for Software Asset Management \(SAM\)
classification: now-assist-for-software-asset-management-sam
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 1
breadcrumb: [References, ServiceNow Otto for Software Asset Management \(SAM\), Software Asset Management, IT Asset Management]
---

# Product match review skill - Triggers and Inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.

## Triggers for the Product match review skill

The following table lists the trigger for the Product match review skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Candidate product matches are reviewed automatically once the matching logic creates them in SAM Product Mapping Results table. The skill accepts or rejects each match.|

## Inputs for the Product match review skill

The following table lists the input for the Product match review skill.

|Input|Description|
|-----|-----------|
|SAM Product Mapping Result \[samp\_product\_mapping\_result\]|The skill reads each candidate match: the raw product name, and the SAM product's name, description and publisher name \[samp\_sw\_product\] and responds if its a match or not.|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/references.md)


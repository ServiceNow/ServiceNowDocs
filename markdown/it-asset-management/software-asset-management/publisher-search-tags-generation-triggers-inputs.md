---
title: Publisher search tags generation skill - Triggers and inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/publisher-search-tags-generation-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Publisher search tags generation skill - Triggers and inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.

## Triggers for the Publisher search tags generation skill

The following table lists the trigger for the Publisher search tags generation skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Search tags are generated automatically for a raw publisher, as the first step when an entitlement import error with unresolved publisher error is created. For custom publishers \(samp\_custom\_sw\_publisher\) created, the daily SAM - Generate Search Tags for custom Publishers and Products job generates them for new or updated records.|

## Inputs for the Publisher search tags generation skill

The following table lists the input for the Publisher search tags generation skill.

|Input|Description|
|-----|-----------|
|Software Raw Publisher \[samp\_raw\_publisher\]|The skill reads the raw publisher name and a few sample product names taken from the publisher's raw products \[samp\_raw\_product\].|
|Custom Publisher \[samp\_custom\_sw\_publisher\]|For custom publishers, the skill reads the publisher name, webpage and sample product names from the publisher's custom products \[samp\_custom\_sw\_product\].|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)


---
title: Product search tags generation skill - Triggers and inputs
description: Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/product-search-tags-generation-triggers-inputs.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2026-10-29"
reading_time_minutes: 1
breadcrumb: [Software Asset Management references, Software Asset Management, IT Asset Management, Asset Management]
---

# Product search tags generation skill - Triggers and inputs

Configure the triggers and inputs to determine how and when a skill is used. An input identifies the data that is used for a skill, such as the table and fields that are used to normalize spend transactions. A trigger initiates an action, such as when the system normalizes spend transactions.

## Triggers for the Product search tags generation skill

The following table lists the trigger for the Product search tags generation skill.

|Trigger|Description|
|-------|-----------|
|Auto-triggered|Search tags are generated automatically for a raw products of a publisher once that publisher match passes Publisher Match Review or if publisher is already resolved. For custom products \(samp\_custom\_sw\_product\) created, the daily SAM - Generate Search Tags for custom Publishers and Products job generates them for new or updated records.|

## Inputs for the Product search tags generation skill

The following table lists the input for the Product search tags generation skill.

|Input|Description|
|-----|-----------|
|Software Raw Product \[samp\_raw\_product\]|The skill reads the raw product name along with the name of the publisher it belongs to.|
|Custom Product \[samp\_custom\_sw\_product\]|For custom products, the skill reads the product name along with the name of its publisher.|

**Parent Topic:**[Software Asset Management references](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/references.md)


---
title: Configure state bucket mapping for custom story states in EAP
description: Map custom story state choices to state buckets in the dictionary to keep story cards visible and correctly placed on the Planning board in Enterprise Agile Planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/enterprise-agile-planning/configure-state-buckets-for-custom-story-states-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-06-09"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Configure state bucket mapping for custom story states in EAP

Map custom story state choices to state buckets in the dictionary to keep story cards visible and correctly placed on the Planning board in Enterprise Agile Planning.

## Before you begin

Role required: admin

## About this task

The Planning board uses state bucket configurations in the dictionary to map story cards to columns. If a custom state choice is not mapped to a state bucket, the Planning board can't locate cards in that state after a page reload. Cards in unmapped states disappear. Complete this task after adding any custom state choice to the story work item type.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Open the `rm_story` table.

3.  In the **Columns** related list, open the **State** column record.

4.  In the **Dictionary Overrides** related list, open the `rm_story` record.

5.  In the **Attributes** field, add the custom state choice to the appropriate state bucket.

6.  Select **Save**.


**Related topics**  


[Story cards disappear from the planning board in Enterprise Agile Planning](https://www.servicenow.com/community/spm-articles/enterprise-agile-planning-story-cards-disappear-from-planning/ta-p/3520666)


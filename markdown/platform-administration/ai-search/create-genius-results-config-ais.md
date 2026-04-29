---
title: Create a Genius Result configuration
description: Create a Genius Result configuration, set its trigger condition, and configure the results displayed on its answer card.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Genius Results, Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a Genius Result configuration

Create a Genius Result configuration, set its trigger condition, and configure the results displayed on its answer card.

## Before you begin

Role required: ais\_admin

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to link the new Genius Result configuration to.

3.  In the Genius Results related list, select **Create and Link**.

4.  On the AI Search Genius Result Configuration form, fill in the fields.

    For a description of the field values, see [AI Search Genius Result Configuration form](../reference/genius-result-cfg-form-ais.md).

5.  Select **Submit**.

    The new Genius Result configuration appears in the Genius Results related list.

6.  Open the **Order** for the new Genius Result configuration to control its display order for the search profile.


## What to do next

Changes to Genius Result configurations take effect in search as soon as you save them. You don't need to publish the linked search profile to make the new configuration take effect.

If you selected an **NLU** trigger condition, you must link an NLU model and its intents to your Genius Result configuration. For instructions, see [Link an NLU model and intents to a Genius Result configuration](link-nlu-model-genius-result-ais.md).

**Parent Topic:**[Genius Results](../concept/genius-results-ais.md)


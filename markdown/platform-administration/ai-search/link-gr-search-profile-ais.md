---
title: Link a Genius Result configuration to a search profile
description: Link a Genius Result configuration to one or more search profiles.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Genius Results, Search profiles, Configuring AI Search, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Link a Genius Result configuration to a search profile

Link a Genius Result configuration to one or more search profiles.

## Before you begin

Role required: ais\_admin

## About this task

To use a Genius Result configuration, link it to a search profile. AI Search evaluates the Genius Result configuration for all searches made with the search profile.

You can link a single Genius Result configuration to multiple search profiles. A search profile can include multiple Genius Result configuration links.

AI Search evaluates active Genius Result configurations for a search profile in an order determined by their numeric **Order** field values, as defined in the search profile's Genius Results related list. Genius Result configurations with lower **Order** field values are evaluated before those with higher field values. As an example, a Genius Result configuration with **Order** 100 is evaluated before one with **Order** 200.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to link the Genius Result configuration to.

3.  In the Genius Results related list, select **Link Existing**.

4.  On the Search Profile - Genius Result Mapping form, fill in the fields.

    For a description of the field values, see [Search Profile - Genius Result Mapping form](../reference/search-prof-gr-mapping-form-ais.md).

5.  Select **Submit**.


## Result

The new Genius Result configuration link appears in the search profile's Genius Results related list.

**Parent Topic:**[Genius Results](../concept/genius-results-ais.md)


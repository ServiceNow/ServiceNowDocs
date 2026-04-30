---
title: Clone a search profile
description: Create a copy of an existing search profile. The cloned search profile retains search sources, stop word and synonym dictionaries, Genius Result configurations, and result improvement rules from the original search profile.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Clone a search profile

Create a copy of an existing search profile. The cloned search profile retains search sources, stop word and synonym dictionaries, Genius Result configurations, and result improvement rules from the original search profile.

## Before you begin

Role required: ais\_admin

## About this task

Multiple search applications can link to the same search profile. For example, in the base system, Service Portal and Virtual Agent both link to the **Service Portal search profile** record.

As a search administrator, you may wish to configure separate search profiles for two applications that share a search profile. Cloning the existing search profile enables you to create a new record with the same search sources, stop word and synonym dictionaries, Genius Result configurations, and result improvement rules. This approach saves time if you want the two applications to use similar or identical search experience settings.

**Note:** Cloning a search profile does not preserve its existing typo handling dictionary settings or blocked terms.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Select the record for the search profile that you want to clone.

    If the system prompts you to change the application scope so that you can edit the record, select the provided link.

3.  Select **Clone**.

4.  In the Set Profile Label dialog box, enter a label for your new search profile record, then select **OK**.

5.  Make changes to the cloned search profile's settings.

    For details on search profile settings, see [Create a search profile](create-search-profile-ais.md), [Synonyms](../concept/synonyms-ais.md), [Stop words](../concept/stop-words-ais.md), [Typo handling](../concept/typo-handling-ais.md), [Genius Results](../concept/genius-results-ais.md), and [Result improvement rules](../concept/result-improvement-rules-ais.md).

6.  Publish your cloned search profile by selecting **Publish**.

    For more information on the effects of publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).


## Result

Your cloned search profile record appears in the Search Profile table.

## What to do next

Edit the search application configuration record of your choice and link it to your cloned search profile. For details on search application configurations, see [Search application configurations](../concept/defining-search-app-cfgs-ais.md).

**Parent Topic:**[Search profiles in AI Search](../concept/defining-search-profiles-ais.md)


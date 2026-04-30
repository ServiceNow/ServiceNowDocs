---
title: Configure AI search profiles with Now Assist for PSDS
description: You can enable AI Search users to search content and metadata from documents in all or part of the knowledge bases, external repositories, and remote tables.Create a new search profile to store search experience settings for Now Assist for PSDS AI Search.Link search sources to a search profile to specify the content that a government service agent can search through that profile.Publish a search profile to make its settings, and any pending changes to its settings, active in search queries.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-16"
reading_time_minutes: 3
breadcrumb: [Enabling and configuring AI Search, Configure, Now Assist for PSDS, Public Sector Digital Services \(PSDS\)]
---

# Configure AI search profiles with Now Assist for PSDS

You can enable AI Search users to search content and metadata from documents in all or part of the knowledge bases, external repositories, and remote tables.

AI Search for Now Assist for Public Sector Digital Services \(PSDS\) stores search experience settings in search profiles. Define a search profile for each unique search experience that you want to offer users in a ServiceNow AI Platform application. Create and populate synonym and stop word dictionaries. Configure typo handling dictionary settings. Define Genius Results and result improvement rules.

A search profile contains settings that determine how AI Search generates search results for a given search. The search application's configuration specifies which search profile to use, and also determines how the generated results are displayed to users.

For more information on AI search profiles, see [Search profiles in AI Search](https://www.servicenow.com/docs/access?context=defining-search-profiles-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

## Create a search profile using Now Assist for PSDS

Create a new search profile to store search experience settings for Now Assist for PSDS AI Search.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Select **New**.

3.  On the Search Profile form, fill in the fields.

    For a description of the field values, see [Search Profile form](https://www.servicenow.com/docs/access?context=search-profile-form-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

4.  Select **Submit**.


### Result

The new search profile appears in the AI Search Search Profiles list with **State** set to **New**. An informational message and an alert triangle icon \(![Alert triangle icon.](../image/icon-alert-triangle.png)\) indicate that the new search profile has never been published.

### What to do next

Your new search profile includes sample synonym and stop word dictionaries and a default typo handling dictionary. For more details on configuring and populating these dictionaries, see [Synonyms](https://www.servicenow.com/docs/access?context=synonyms-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US), [Stop words](https://www.servicenow.com/docs/access?context=stop-words-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US), and [Typo handling](https://www.servicenow.com/docs/access?context=typo-handling-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

To make content searchable using your new search profile, link one or more search sources to it.

## Link a search source to a search profile in Now Assist for Public Sector Digital Services \(PSDS\)

Link search sources to a search profile to specify the content that a government service agent can search through that profile.

### Before you begin

Role required: admin

### About this task

Linking a search source to a search profile makes its filtered content available for searches using that search profile. AI Search only indexes and uses content from the search profile's linked search sources when finding and generating standard search results and Genius Result answers.

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the search profile that you want to link the search source to.

    To configure single-turn AI Search for use in the Now Assist Panel, select the **\[CSM AIS\] Configurable Workspace Search Config** search profile,

3.  In the Search Sources related list, select **Link Existing**.

    To configure single-turn AI Search, select the Genius Results related list, then select **Link Existing**.

4.  On the Search Profile-Search Source Mapping form, fill in the fields.

    To configure single-turn AI Search, enter **Now Assist Q&amp;A** in the Genius Result Configuration field, and set the order to **1**.

    For a description of the field values, see [Search Profile - Search Source Mapping form](https://www.servicenow.com/docs/access?context=search-prof-src-mapping-form-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

5.  Select **Submit**.

    ![Search profile related list showing linked Now Assist Q&A configuration](../image/search-profile-related-list-na-psds.png)


### Result

The new search source appears in the Search Sources or Genius Results related list. Search query results immediately reflect changes to the set of records searchable through the search profile.

### What to do next

To make a search profile's settings active in search queries, you must publish it.

## Publish a search profile in Now Assist for Public Sector Digital Services \(PSDS\)

Publish a search profile to make its settings, and any pending changes to its settings, active in search queries.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

    **Note:** Search profiles with the **New** state display an alert triangle icon \(![Alert triangle icon.](../image/icon-alert-triangle.png)\). An informational message notifies you to publish these search profiles.

2.  Open the search profile that you want to publish.

3.  Select **Publish**.


### Result

The search profile appears in the AI Search Search Profiles list with **State** set to **Published**, and can be used to filter what search sources are being indexed by the Now Assist for PSDS AI Search.


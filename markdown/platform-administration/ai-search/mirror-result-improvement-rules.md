---
title: Share result improvement rules between search profiles
description: Make your search experiences more consistent by configuring a search profile to mirror result improvement rules from other search profiles.
locale: en-US
release: zurich
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2025-10-03"
reading_time_minutes: 3
breadcrumb: [Result improvement rules, Search profiles, Configure, AI Search, Search administration, Configure core features, Administer]
---

# Share result improvement rules between search profiles

Make your search experiences more consistent by configuring a search profile to mirror result improvement rules from other search profiles.

## Before you begin

You must have [Now Assist in AI Search](../reference/now-assist-ais.md) installed.

Role required: ais\_admin

## About this task

Result improvement rules are specific to the search profile they're created in, and can't be copied between search profiles. As a search administrator, however, you can configure a search profile to use the set of result improvement rules defined in another search profile. This approach lets you define your result improvement rules in one place while making them available in multiple different search experiences.

This procedure is called mirroring, since your affected search profile reflects result improvement rules defined in another search profile. The search profile that includes your result improvement rules is called the mirror source, and the search profile that uses those rules is called the mirror target.

**Note:** You can link multiple mirror source search profiles to a single mirror target search profile. Similarly, you can link a single mirror source search profile to multiple mirror target search profiles.

When you modify result improvement rules in a mirror source search profile and then publish that search profile, AI Search checks all mirror target search profiles that link to that mirror source.

-   If the mirror target search profile is published, AI Search republishes it so that it reflects your result improvement rule changes.
-   If the mirror target search profile isn't published, an informational message reminds you to publish it so that it can reflect your result improvement rule changes.

This check keeps result improvement rule changes in sync across your search profiles.

## Procedure

1.  Navigate to **All** &gt; **AI Search** &gt; **Search Experience** &gt; **Search Profiles**.

2.  Open the record for the mirror target search profile.

    As an example, if you've defined result improvement rules in the Service Portal Default Search Profile and now want to mirror those rules in the ESC Portal Default Search Profile, open the ESC Portal Default Search Profile record.

3.  To add another search profile as a mirror source for result improvement rules, create a link to it.

    1.  In the Mirrored Result Improvement Rules related list, select **Link Search Profile**.

    2.  On the Mirrored Result Improvement Rule form, in the **Mirror Source** field, enter the name of the search profile that you want to mirror result improvement rules from, or use the Lookup using list icon ![](../image/icon-lookup-using-list.png) to populate the field.

    3.  Select **Submit**.

        The new mirror source search profile appears in the Mirrored Result Improvement Rules related list.

    4.  Repeat the linking procedure for each additional search profile you want to add as a mirror source.

4.  To remove one or more search profiles as mirror sources for result improvement rules, unlink them:

    1.  In the Mirrored Result Improvement Rules related list, select the row checkbox for each mirror source that you want to remove.

    2.  Select **Unlink Selected**.

        The selected mirror source search profiles are removed from the Mirrored Result Improvement Rules related list.

5.  To make your mirror source changes take effect, publish your modified mirror target search profile.

    For details on publishing a search profile, see [Publish an AI Search search profile](publish-search-profile-ais.md).


**Parent Topic:**[Result improvement rules](../concept/result-improvement-rules-ais.md)


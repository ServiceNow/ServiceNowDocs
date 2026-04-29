---
title: Search Preview admin tools
description: Learn about the output, controls, and fields provided by admin tools in the new Search Preview UI.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Search Preview UI, Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search Preview admin tools

Learn about the output, controls, and fields provided by admin tools in the new Search Preview UI.

In all of the admin tools, the active search profile is the search profile currently selected for previewed search queries.

-   If you select the **Full visual view** preview type, the active search profile is the one linked to the search application configuration selected in the **Search Application** field.
-   If you select the **Text only view** preview type, the active search profile is the one selected in the **Search Profile** field.

## Summary tool

The Summary tool ![](../image/search-preview-new-icon-summary.png) displays these sections:

-   **Search profile**

    In full visual view, this section provides links to the selected search application configuration and the active search profile that's linked to it. In text only view, it provides a link to the active search profile.

-   **Process data**

    This section provides an overview of how the previewed search query behaved, with details as given in the following table.

<table id="table_qh2_lyl_hhc"><thead><tr><th>

Entry

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Query Rules Triggered

</td><td>

Count and names of result improvement rules triggered by the search query.

</td></tr><tr><td>

Intents Matched

</td><td>

Count and names of NLU model intents detected in the search query.

</td></tr><tr><td>

Total time

</td><td>

Total time the AI Search back end spent processing the search query. This time includes the pre-processing time, search query time, Genius Result computation time, and security processing time values that are reported separately. It does not include time spent sending the search query results across the network to the user's browser.

</td></tr><tr><td>

Pre-processing time

</td><td>

Time spent preparing the search query for execution. Includes time spent looking up the user's access permissions for content security.

</td></tr><tr><td>

Search query time

</td><td>

Time spent retrieving records that match the search query and generating the result set.

</td></tr><tr><td>

Genius Result computation

</td><td>

Time spent computing Genius Result answers for the search query.

</td></tr><tr><td>

Security processing time

</td><td>

Time spent filtering inaccessible records out of the search query's result set based on the user's access permissions.

</td></tr></tbody>
</table>
## Genius Results tool

The Genius Results tool ![](../image/search-preview-new-icon-genius-results.png) displays these sections:

-   **Genius Result status**

    In full result view, this section shows a list of Genius Result configurations activated in the active search profile. A checkmark and status text indicate whether or not each Genius Result configuration generated an answer for the search query.

-   **LLM Context**

    This section shows a list of all the search results that were sent to the LLM for Genius Result answer generation, along with indicators of how well each sent result matched the context of the search query.


## Details tool

The Details tool ![](../image/search-preview-new-icon-details.png) displays these sections:

-   **Dictionary**

    This section shows how the stop word, typo handling, and synonym dictionaries defined in the active search profile affected the previewed search query.

    |Entry|Description|
    |-----|-----------|
    |Stopwords|Summary of stop word removal operations performed while processing the search query.|
    |Spellcheck|Summary of typo handling auto-correction operations performed while processing the search query.|
    |Synonyms|Summary of synonym expansion operations performed while processing the search query.|

-   **Query**

    List of fields and values from the search query object. Select **Filters** to refine this list by field category. You can select multiple categories at a time to view just the fields you're interested in.


## Profile tool

The Profile tool ![](../image/search-preview-new-icon-summary.png) displays these sections:

-   **User**

    This section provides fields you can use to search as a specific user or in a specific supported language. Use these fields to see how search results differ from user to user and language to language.

<table id="table_sc1_31m_hhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search as user

</td><td>

To submit search preview queries as another user, enter the user's name from the User \[sys\_users\] table. You must have the impersonator role.Use this control to see how content security affects search query results for specific user accounts.

Searches performed while impersonating another user don't affect the **Search users** metric, trend, and report on the AI Search Analytics dashboard.

**Note:** Changing the value of this field terminates elevated privileges for the ais\_high\_security\_admin role. To bypass filters after changing this field's value, you must re-elevate to the ais\_high\_security\_admin role.

</td></tr><tr><td>

Query locale

</td><td>

To submit search preview queries using a specific supported language, select the language from the list. Use this control to observe differences in search query results for different languages.

</td></tr></tbody>
</table>-   **Context settings**

    This section provides the following groups of user context fields you can use to specify user context values. Use these fields when testing user context triggers for your result improvement rules.

    -   **Location and language**

        |Field|Description|
        |-----|-----------|
        |User language|To set a language in the user context for search preview, select it from the list of supported languages.|
        |User groups|To set a user group in the user context for search preview, enter the name of a group from the Group \[sys\_user\_group\] table.|
        |User title|To set a title in the user context for search preview, select it from the list. This list includes all Title values found in the User \[sys\_user\] table.|
        |User department|To set a department in the user context for search preview, enter the name of a department from the Department \[cmn\_department\] table.|
        |User location|To set a location in the user context for search preview, enter the name of a location from the Location \[cmn\_location\] table.|
        |User country|To set a country in the user context for search preview, select it from the list. This list includes all countries found in user locations from the User \[sys\_user\] table.|
        |User office|To set an office in the user context for search preview, enter the name of a building from the Building \[cmn\_building\] table.|
        |User office city|To set an office city in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
        |User office state|To set an office state in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
        |User office country|To set an office country in the user context for search preview, select it from the list. This list includes all countries found in user locations from the User \[sys\_user\] table.|

    -   **User access**

<table id="table_n1y_z1m_hhc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User company

</td><td>

To set a company in the user context for search preview, enter the name of a company from the Company \[core\_company\] table.

</td></tr><tr><td>

User roles

</td><td>

To set a role in the user context for search preview, enter the name of a role from the Role \[sys\_user\_role\] table and press Enter. You can set multiple roles for a single search query. Each selected role appears as a pill. To remove a role, select the Remove icon ![](../image/search-preview-new-icon-pill-remove.png) for its pill.

</td></tr></tbody>
</table>    -   **Environment**

        |Field|Description|
        |-----|-----------|
        |User OS|To set an operating system in the user context for search preview, enter its name in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
        |User OS version|To set an operating system version in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
        |User agent|To set a web browser's user-agent string in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
        |User browser agent|To set a browser name in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
        |User device form|To set a device form in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
        |User device type|To set a user device type in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|


**Parent Topic:**[Search Preview UI for AI Search](../concept/search-preview-ui-new.md)


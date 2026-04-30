---
title: Search Preview admin tools
description: Understand the output, controls, and fields provided by admin tools in the new Search Preview UI.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2025-09-19"
reading_time_minutes: 6
breadcrumb: [Search Preview UI, Administer, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search Preview admin tools

Understand the output, controls, and fields provided by admin tools in the new Search Preview UI.

## Data tool

The Data tool ![](../image/search-preview-new-icon-process-data.png) displays summary information on the search query's triggered result improvement rules, matched NLU model intents, and processing time. These entries provide an overview of how the search query performed.

<table id="table_bz2_ln3_b4b"><thead><tr><th>

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

Total time the AI Search back end spent processing the search query.

 This time includes the pre-processing time, search query time, Genius Result computation time, and security processing time values that are reported separately. It does not include time spent sending the search query results across the network to the user's browser.

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
</table>## Alert tool

The Alert tool ![](../image/search-preview-new-icon-alerts.png) displays any alert feedback messages produced while processing the search query.

## Feedback tool

The Feedback tool ![](../image/search-preview-new-icon-feedback.png) displays any dictionary or query feedback messages or NLU model intent data produced while processing the search query.

|Entry|Description|
|-----|-----------|
|Stopwords|List of feedback messages relating to stop word removal for the search query.|
|Spellcheck|List of feedback messages relating to typo handling auto-correction for the search query.|
|Synonyms|List of feedback messages relating to synonym expansion for the search query.|

## Context tool

The Context tool ![](../image/search-preview-new-icon-context.png) provides fields you can use to specify user context values. Use these fields when testing user context triggers for your result improvement rules.

<table id="table_fgd_tp3_b4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

User Groups

</td><td>

To set a user group in the user context for search preview, enter the name of a group from the Group \[sys\_user\_group\] table.

</td></tr><tr><td>

User Company

</td><td>

To set a company in the user context for search preview, enter the name of a company from the Company \[core\_company\] table.

</td></tr><tr><td>

User Office

</td><td>

To set an office in the user context for search preview, enter the name of a building from the Building \[cmn\_building\] table.

</td></tr><tr><td>

User Department

</td><td>

To set a department in the user context for search preview, enter the name of a department from the Department \[cmn\_department\] table.

</td></tr><tr><td>

User Title

</td><td>

To set a title in the user context for search preview, select it from the list. This list includes all Title values found in the User \[sys\_user\] table.

</td></tr><tr><td>

User Location

</td><td>

To set a location in the user context for search preview, enter the name of a location from the Location \[cmn\_location\] table.

</td></tr><tr><td>

User Roles

</td><td>

To set a role in the user context for search preview, enter the name of a role from the Role \[sys\_user\_role\] table and press Enter.

 You can set multiple roles for a single search query. Each selected role appears as a pill. To remove a role, select the Remove icon ![](../image/search-preview-new-icon-pill-remove.png) for its pill.

</td></tr><tr><td>

User Country

</td><td>

To set a country in the user context for search preview, select it from the list. This list includes all countries found in user locations from the User \[sys\_user\] table.

</td></tr><tr><td>

User Language

</td><td>

To set a language in the user context for search preview, select it from the list of supported languages.

</td></tr><tr><td>

User Office Country

</td><td>

To set an office country in the user context for search preview, select it from the list. This list includes all countries found in user locations from the User \[sys\_user\] table.

</td></tr><tr><td>

User Office City

</td><td>

To set an office city in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.

</td></tr><tr><td>

User Office State

</td><td>

To set an office state in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.

</td></tr><tr><td>

User OS

</td><td>

To set an operating system in the user context for search preview, enter its name in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.

</td></tr><tr><td>

User Device Type

</td><td>

To set a user device type in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.

</td></tr><tr><td>

User OS Version

</td><td>

To set an operating system version in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.

</td></tr><tr><td>

User Agent

</td><td>

To set a web browser's user-agent string in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.

</td></tr><tr><td>

User Browser Agent

</td><td>

To set a browser name in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.

</td></tr><tr><td>

User Device Form

</td><td>

To set a device form in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../task/session-debugging-ais.md) to review values submitted for this user context field in user queries.

</td></tr></tbody>
</table>## User tool

The User tool ![](../image/search-preview-new-icon-user.png) provides fields you can use to search as a specific user or in a specific supported language. Use these fields to see how search results differ from user to user and language to language.

<table id="table_pxj_yq3_b4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search as User

</td><td>

To submit search preview queries as another user, enter the user's name from the User \[sys\_users\] table. You must have the impersonator role.

 Use this control to see how content security affects search query results for specific user accounts.

 Searches performed while impersonating another user don't affect the **Search users** metric, trend, and report on the AI Search Analytics dashboard.

 **Note:** Changing the value of this field terminates elevated privileges for the ais\_high\_security\_admin role. To bypass filters after changing this field's value, you must re-elevate to the ais\_high\_security\_admin role.

</td></tr><tr><td>

Query Locale

</td><td>

To submit search preview queries using a specific supported language, select the language from the list.

 Use this control to observe differences in search query results for different languages.

</td></tr></tbody>
</table>**Parent Topic:**[Search Preview UI for AI Search](../concept/search-preview-ui-new.md)


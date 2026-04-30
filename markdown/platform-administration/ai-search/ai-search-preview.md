---
title: Search Preview UI for AI Search
description: The Search Preview UI enables you to test AI Search queries using settings from a selected search profile. Administrator tools help you review search query performance data and feedback, debug queries, and override default query settings for testing purposes.Understand the output, controls, and fields provided by admin tools in the search preview UI.
locale: en-US
release: yokohama
product: AI Search
classification: ai-search
topic_type: concept
last_updated: "2025-09-12"
reading_time_minutes: 8
breadcrumb: [Advanced AI Search Management Tools, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search Preview UI for AI Search

The Search Preview UI enables you to test AI Search queries using settings from a selected search profile. Administrator tools help you review search query performance data and feedback, debug queries, and override default query settings for testing purposes.

Access the Search Preview UI by navigating to **AI Search** &gt; **Preview** &gt; **Search Preview**.

## Required ServiceNow AI Platform® roles

-   The ais\_admin role is required to view and use the Search Preview UI.
-   The impersonator role is required for some AI Search administrator tools.
-   The ais\_high\_security\_admin role is required to bypass search source and content security filtering. For details on this procedure, see [Diagnose search result access issues using the Search Preview UI](../../../administer/ai-search/task/diagnose-srch-result-access-ais.md).

## Search Preview UI components

![Sample Search Preview UI screen displaying sales laptop search query results.](../image/adv-ais-mgmt-search-preview.png "Search Preview UI")

<table id="table_f15_qb3_b4b"><thead><tr><th>

Component

</th><th>

Description

</th></tr></thead><tbody><tr><td>

1. Search profile list

</td><td>

Select the search profile to apply when previewing search queries. The list only includes published search profiles that have one or more linked search sources.

**Note:** If a search profile has unpublished changes, the list displays a warning icon ![](../image/icon-warning-circle.png) and shows `[DRAFT]` after the profile's name. Publish the search profile to see these changes reflected in the search query preview.

</td></tr><tr><td>

2. Search input field

</td><td>

Enter search query terms and operators in this field. To preview the query's results using settings from the selected search profile, select **Search**.

</td></tr><tr><td>

3. Table facet filter

</td><td>

View the distribution of search query results by source table. To filter the query results by table, select a table's name. To remove the table facet filter, select **All**.

</td></tr><tr><td>

4. Genius Result answers

</td><td>

Review the key-value pairs for each Genius Result answer the search query produces when executed with the selected search profile.**Note:** Genius Result answers may not appear for all search queries.

</td></tr><tr><td>

5. Search query results

</td><td>

Review the results the search query produces when executed with the selected search profile. To page through results, select **Next** or **Previous**.

</td></tr><tr><td>

6. AI Search administrator tools

</td><td>

Select the icon for the administrator tool that you want to use:-   Process data tool ![](../image/icon-help.png): View summary information on the search query's triggered result improvement rules, matched NLU model intents, and processing time.
-   Alerts tool ![](../image/icon-alert.png): Review alert feedback messages produced during processing of the search query.
-   Dictionary and query feedback tool ![](../image/icon-book-open.png): Review dictionary and query feedback messages and NLU model intent data for the search query. Enable debugging.
-   Context settings tool ![](../image/icon-boolean.png): Specify user context values for the search query to trigger result improvement rules.
-   User impersonation tool ![](../image/icon-user.png): Change the search query's user or locale to test access settings and view translated documents.

 For more detailed descriptions of each administrator tool's output, controls, and fields, see the following reference section.

</td></tr></tbody>
</table>## Search preview admin tools

Understand the output, controls, and fields provided by admin tools in the search preview UI.

### Process data tool

|Entry|Description|
|-----|-----------|
|Query Rules Triggered|Count of result improvement rules triggered by the search query.|
|Intents Matched|Count and names of NLU model intents detected in the search query.|
|Total time|Total time spent processing the search query. Includes pre-processing, search query, Genius Result computation, and security processing times.|
|Pre-processing time|Time spent preparing the search query for execution. Includes time spent looking up the user's access permissions for content security.|
|Search query time|Time spent retrieving records that match the search query and generating the result set.|
|Genius Result computation|Time spent computing Genius Result answers for the search query.|
|Security processing time|Time spent filtering inaccessible records out of the search query's result set based on the user's access permissions.|

### Alerts tool

This tool displays a list of alert feedback messages produced while processing the search query.

If the search query produced no alert feedback messages, the tool instead displays `No Alert Feedback`.

### Dictionary and query feedback tool

This tool displays separate panes for dictionary feedback entries and query feedback controls.

|Entry|Description|
|-----|-----------|
|Stop words|List of feedback messages relating to stop word removal for the search query.|
|Spellcheck|List of feedback messages relating to typo handling auto-correction for the search query.|
|Synonyms|List of feedback messages relating to synonym expansion for the search query.|

<table id="table_khg_z43_b4b"><thead><tr><th>

Control

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Show all feedback

</td><td>

Display a JSON array of feedback messages produced for the search query.

</td></tr><tr><td>

Show all intent data

</td><td>

Display a JSON array of NLU model intents detected in the search query.**Note:** To use this tool, you must have the impersonator role.

</td></tr><tr><td>

Debug

</td><td>

Enable this option to set **sysparm\_debug** to **true** when submitting search preview queries.**Note:** To use this tool, you must have the impersonator role.

</td></tr></tbody>
</table>### Context settings tool

With these tools, you can specify user context values to test user context triggers for result improvement rules.

|Field|Description|
|-----|-----------|
|User Domain|To set a domain in the user context for search preview, enter the name of a group from the Group \[sys\_user\_group\] table.|
|User Company|To set a company in the user context for search preview, enter the name of a company from the Company \[core\_company\] table.|
|User Office|To set an office in the user context for search preview, enter the name of a building from the Building \[cmn\_building\] table.|
|User Department|To set a department in the user context for search preview, enter the name of a department from the Department \[cmn\_department\] table.|
|User Title|To set a title in the user context for search preview, select it from the list. This list includes all Title values found in the User \[sys\_user\] table.|
|User Location|To set a location in the user context for search preview, enter the name of a location from the Location \[cmn\_location\] table.|
|User Role|To set a role in the user context for search preview, enter the name of a role from the Role \[sys\_user\_role\] table.|
|User Country|To set a country in the user context for search preview, select it from the list. This list includes all countries found in user locations from the User \[sys\_user\] table.|
|User Language|To set a language in the user context for search preview, select it from the list of supported languages.|
|User Office Country|To set an office country in the user context for search preview, select it from the list. This list includes all countries found in user locations from the User \[sys\_user\] table.|
|User Office City|To set an office city in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../../../administer/ai-search/task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
|User Office State|To set an office state in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../../../administer/ai-search/task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
|User OS|To set an operating system in the user context for search preview, enter its name in this field. You can enable [session debugging for AI Search](../../../administer/ai-search/task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
|User Device Type|To set a user device type in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../../../administer/ai-search/task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
|User OS Version Type|To set an operating system version type in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../../../administer/ai-search/task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
|User Browser Agent|To set a browser agent string in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../../../administer/ai-search/task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
|User Browser|To set a browser name in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../../../administer/ai-search/task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|
|User Device Form|To set a device form in the user context for search preview, enter it in this field. You can enable [session debugging for AI Search](../../../administer/ai-search/task/session-debugging-ais.md) to review values submitted for this user context field in user queries.|

### User impersonation tool

<table id="table_pxj_yq3_b4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search as

</td><td>

To submit search preview queries as another user, enter the user's name from the User \[sys\_users\] table. You must have the impersonator role. Use this control to see how content security affects search query results for specific user accounts.

 Searches performed while impersonating another user don't affect the **Search users** metric, trend, and report on the AI Search Analytics dashboard.

 **Note:** Changing the value of this field terminates elevated privileges for the ais\_high\_security\_admin role. To bypass filters after changing this field's value, you must re-elevate to the ais\_high\_security\_admin role.

</td></tr><tr><td>

Query Locale

</td><td>

To submit search preview queries using a specific supported language, select the language from the list. Use this control to observe differences in search query results for different languages.

</td></tr></tbody>
</table>
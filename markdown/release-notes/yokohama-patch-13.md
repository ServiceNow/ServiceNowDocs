---
title: Yokohama Patch 13
description: The Yokohama Patch 13 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/release-notes/yokohama-patch-13.html
release: yokohama
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 59
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 13

The Yokohama Patch 13 release contains important problem fixes.

-   **Yokohama Patch 13 was released on May 5, 2026.**
    -   Build date: 04-29-2026\_0346
    -   Build tag: glide-yokohama-12-18-2024\_\_patch13-04-21-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y13.00.xlsx).

## Overview

Yokohama Patch 13 includes 297 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-yp13.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Yokohama Patch 13 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 13, refer to [KB2962846](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2962846).

## Changes in Yokohama Patch 13

-   **[Associate a request header with a resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/associate-header-api-resource.md)**

    Define which request headers are expected for each resource within a scripted REST API.

-   **[Associate query parameters with a resource](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/AssocQueryParmResource.md)**

    Associate scripted REST API query parameters with a resource.

-   **[Automatically generate API request definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/autogenerate-api-request-definitions.md)**

    Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource.

-   **[Available system properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/platform-administration/r_AvailableSystemProperties.md)**
    -   **glide.rest.sampling.enabled**

        Enables request sampling from scripted REST API resources. REquest samples can be used to automatically generate definitions for request headers, query parameters, and schemas. General guidance to help limit performance problems is to only enable this property in non-production instances.

        -   Type: true \| false
        -   Default value: false
        -   Location: System Property \[sys\_properties\] table
-   **[Define a REST API response header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/define-scripted-api-response-header.md)**

    Define one or more REST API response headers in a REST API.

-   **[Define a REST API schema](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/define-scripted-rest-api-schema.md)**

    Specify the expected data structure for requests or responses within a REST API by defining a schema.

-   **[Define an API resource response structure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/add-schema-rest-api-response.md)**

    Add a schema and relevant response headers to a REST response to define the response's expected data structure.

-   **[Define an API resource request structure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/add-schema-rest-api-request.md)**

    Add a schema to a REST request record to define the request's expected data structure.

-   **[Define available query parameters](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/t_DefineAvailableQueryParameters.md)**

    Define available query parameters to control what values a requesting user can pass in the request URI.

-   **[Define a scripted REST API request header](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/t_DefineRESTServiceHeaders.md)**

    Define scripted REST API request headers to control which headers the API accepts.

-   **[Guarded script evaluator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/guarded-script.md)**

    The guarded script evaluator enhances instance security by supporting only a restricted scripting language and detecting or rejecting untrusted scripts that use unsupported JavaScript features.

-   **[JavaScript APIs supported by guarded script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/guarded-script-allowed-apis.md)**

    Review the JavaScript APIs that guarded script supports to help you analyze scripts in the Incompatible Guarded Scripts list and either rewrite them or create an exemption for them.

-   **[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md)**

    For Now Assist new features and changes, see [Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/now-assist-rn-landing.md).

-   **[Update scripts incompatible with guarded script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/incompatible-guarded-scripts.md)**
-   **[Script sandbox evaluator](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/script-sandbox.md)**

    The script sandbox evaluator helps prevent executing untrusted scripts on an instance by limiting the APIs available to scripts.

    Scripts that run in the script sandbox evaluator can use features supported by the JavaScript engine and the sandbox environment, except for certain restricted methods. Untrusted scripts are processed by the script sandbox evaluator under the following conditions:

    -   A script has been granted a guarded-script exemption \(manually or automatically\).
    -   When guarded script is in Phase 1: Detection, and a script is sent to the server by an authenticated user.
    For more information about guarded-script exemptions and enforcement phases, see .

-   **[Scripted REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/c_CustomWebServices.md)**

    Schemas define a structure that can be used for API requests and responses, including data type, expected fields, and formats. You can define multiple schemas within a scripted REST API, which can be used to specify request and response contents of the resources within that API.

    Schemas must be defined using [OpenAPI version 3.0.1 format](https://spec.openapis.org/oas/v3.0.1.html).

-   **[Script sandbox environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/api-reference/scripts/script-sandbox-environment.md)**

    The script sandbox environment is a restricted execution context in which untrusted, client-generated scripts run on the server using one of two evaluators: the guarded script evaluator or the script sandbox evaluator.


## Notable fixes

The following problems and their fixes are ordered by potential impact to customers, starting with the most significant fixes.

<table id="notable-fixes" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Application Manager

 PRB1889269

</td><td>

Progress worker state isn't set to complete after worker is finished

</td><td>

Installing plugins shows an error even when successfully completed. In the logs, it looks like the error comes from a script include. Previously, the code block was a part of a larger function that had appVersion and appID as parameters. The code was refactored into the forceSyncWithStore function, which doesn't have appVersion and appID as parameters. If the gs.info line is reached, it throws an error because those two fields were not passed into the function.

</td><td>

1.  Install the custom scoped app \(e.g., x\_conym\_atf\_sc\_req, x\_conym\_hrp\).
2.  Check 'sys\_upgrade\_history' to confirm the installation is marked as 'complete'.
3.  Check 'sys\_progress\_worker' list for the message 'Progress worker state is not set to complete after worker is finished.'
4.  Check 'syslog' for the error 'com.glide.script.RhinoEcmaError: 'appVersion' is not defined.'

</td></tr><tr><td>

Application Manager

 PRB1981044

 [KB2719949](https://hi.service-now.com/kb_view.do?sysparm_article=KB2719949)

</td><td>

The latest version in the sys\_store\_app table is updated to the installed version after an install, thereby causing the **Upgrade** button to be unavailable in App Manager

</td><td>

Two functions \(\_fixLatestVersionFor WithdrawnInstalledApps, \_fixLatestVersionFor WithdrawnInstalledCustomizations\) in Application Manager's UpdateChecker. checkAvailableUpdates API \(aka Sync in the UI\) were missing a required GlideRecord.addQuery constraint when the 'sn\_appclient.enable\_ app\_manager\_checksums\_cache' sys\_property was set to true \(default\). This issue led to the latest\_version being set to the incorrect values on Install/Sync.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence

 PRB1971863

</td><td>

Transaction canceled: 'Failed to get database connection due to exhaustion of connection pool on the node'

</td><td>

A spike in requests can produce a demand exceeding pool max capacity. Some connections are created, but the process is slow, causing various race conditions and delays and eventually causing a timeout in one operation.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1952527

 [KB2743221](https://hi.service-now.com/kb_view.do?sysparm_article=KB2743221)

</td><td>

An email template isn't applied when users select **Apply template** in the mini/full composer

</td><td>

The template isn't applied.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1969766

 [KB2664275](https://hi.service-now.com/kb_view.do?sysparm_article=KB2664275)

</td><td>

Missing MIDLogFileHandler MID Server properties cause MID servers to go into an infinite loop of restarting during start up

</td><td>

MID Servers repeatedly come up and then go back down for a few seconds before the MID Server comes back up again. This loop repeats continuously if certain MID Server Properties are missing from the ecc\_agent\_property table on the instance.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Multi-provider Single Sign-on \(SSO\)

 PRB1979071

 [KB2715489](https://hi.service-now.com/kb_view.do?sysparm_article=KB2715489)

</td><td>

SAML SP Keystore expiration

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1998771

 [KB2898934](https://hi.service-now.com/kb_view.do?sysparm_article=KB2898934)

</td><td>

Installing the com.glide.ai\_record\_activity plugin doesn't create the sys\_ai\_record\_activity table, causing NullPointerException errors

</td><td>

The user observes errors getting records for sys\_ai\_record\_activity: java.lang.NullPointerException.

</td><td>

1.  Install the GenAI Q4 feature or upgrade an existing instance.
2.  Ensure the plugin com.glide.ai\_record\_activity is installed.

 Observe the system logs or error output about an error getting a record for sys\_ai\_record\_activity: java.lang.NullPointerException.

</td></tr></tbody>
</table>## All other fixes

<table id="all-other-fixes" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Activity Stream

 PRB1996382

</td><td>

When setting glide.ui.escape\_text to 'false', forms break

</td><td>

 

</td><td>

1.  Open any Zurich instance.
2.  Upload the sys\_properties file for glide.ui.escape\_text.
3.  Run a /cache.do.
4.  Load any relevant record, such as 'Incident'.

 Expected behavior: The record should load normally with the glide.ui.escape\_text sys\_property activated.

 Actual behavior: A blank screen with a basic message at the top calls out the ampersand issue.

</td></tr><tr><td>

Activity Stream

 PRB1998124

</td><td>

Activity stream citations cause an increased page load time

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Open Service Operations Workspace.
3.  Open any incident record with a large amount of activity stream entries \(~2000 entries\).
4.  Open the browser's dev tools window.
5.  Select the 'Performance' tab.
6.  Select the **Record and reload** button.

 Expected behavior: The page load time shouldn't be affected by CitationHighlightBehavior.js and require less time.

 Actual behavior: The page takes about 6 seconds or more to fully load, and the 'Performance' tab displays that it is due to CitationHighlightBehavior.js.

</td></tr><tr><td>

Activity Stream

 PRB2004286

</td><td>

A user's filter is incorrectly keying the supplemental map with translated keys, leading to an empty activity stream after changing the language

</td><td>

A supplemental map is incorrectly keyed with a translated string. It's also not correctly handling the case where the key in the map doesn't exist, leading to an uncaught exception and the activity stream not loading.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2008384

</td><td>

The **Copy** button on journal entries doesn't always copy text or notify users correctly

</td><td>

This is reproducible in UI16 and Workspace.

</td><td>

1.  Navigate to any relevant workspace.
2.  Open any incident record.
3.  Turn on the 'Rich text editor' in activity stream's **Compose**.
4.  Add a work note or comment to the activity stream with some of the text set to bold.
5.  Select the **Copy to clipboard** button on the new journal entry.

 Expected behavior: When rich text is copied, a notification should display saying 'Copied to clipboard'. When pasted into a plain text editor, there shouldn't be \[code\] tags around the text.

 Actual behavior: When rich text is copied, a notification doesn't display. When pasted into a plain text editor, there shouldn't be \[code\] tags around the text.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1935541

</td><td>

Work item incorrectly moved to cancelled state instead of queued state

</td><td>

Without external routing, the rejected work item should move to the queued state. Instead, the work item moves to the cancelled state, and the interaction moves to closed\_abandoned.

</td><td>

1.  Change mweb sys\_cs\_channel to type 'Messaging'.
2.  Enable external routing for 'Chat - Asynchronous' Channel.
3.  Mark Chat Async Queue 'external' as true.
4.  Make two external agents available in workspace.
5.  As a system admin, start a chat in the SP/CSM portal.

Once routing to live agent starts, a new work item is created.

6.  Assign the work item to the first agent using manual assignment API via REST API explorer.
7.  Change the first agent presence to offline.
8.  Send a message from admin.

The conversation is reassigned, which moves the interaction state to New and creates a new work item.

9.  Assign the new work item to the second agent using manual assignment API via REST API explorer.
10. Reject the work item.

 Expected behavior: Without external routing, the work item is moved to the queued state, looking for new agent.

 Actual behavior: The new work item moves to the cancelled state, and the interaction moves to closed\_abandoned.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1938992

</td><td>

High AWA assignment cycle times for impact voice call routing

</td><td>

A user is uptaking in NVC and they are facing slow response times for call routing. It's taking ~12 seconds to route the call to agent. Each AWA assignment cycle is taking ~11 secs and out of which ~8 secs is being spent for Agent Map creation. Expected response times should be less than a second as there's no other load in the system.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1981019

</td><td>

AWA TransferToQueue shouldn't reassign a workItem to an AI Agent once rejected

</td><td>

If the interaction was previously transferred from the AI Agent, it shouldn't be transferred back to the AI Agent later \(even if the AI agent is available\).

</td><td>

1.  Make sure an AI agent \(sys\_user with identity\_type= 'ai\_agent'\) is part of the agent chat assignment group of the chat queue.
2.  Make it AI available.
3.  Create a workItem.
4.  Assign it to the AI agent.
5.  Use the 'Transfer to queue' API to transfer the interaction to the same chat queue where the first workItem was created.
6.  Make the agent 'Beth Anglin' available to receive the transferred workItem.
7.  Invoke the **Transfer To queue** quick action from Beth.
8.  Select the same chat queue.

 Observe that the interaction is transferred to the AI Agent.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1982818

</td><td>

After removing a service channel, the current universal capacity of the agent isn't decreased

</td><td>

After removing a service channel from the 'Available' presence state, the universal capacity for the existing documents related to that channel shouldn't be considered.

</td><td>

1.  Create a service channel \('Chat-test'\).
2.  Add it to the 'Available' presence state in awa\_presence\_state.
3.  Create related queues and assignment eligibility pools.
4.  Create a universal capacity record for the agent \('Beth Anglin'\).
5.  Make the agent 'Available'.
6.  Create documents for that and let those be assigned to the agent.

Observe that the current universal capacity of the agent is increased.

7.  Remove the service channel from the 'Available' presence state in awa\_presence\_state.

 Observe that the current universal capacity of the agent stays the same. In Xanadu and Zurich, the current universal capacity gets decreased.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1985807

</td><td>

Graphql calls related to snOpenframeWrapper happen in regular spikes across all nodes and cause large CPU spikes

</td><td>

After the upgrade to Australia, a specific graphql call happens every 10 \(or sometimes 5\) minutes on HI.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1975798

</td><td>

Glide fixes to JSON return type in AIAToolDataPillUtil

</td><td>

 

</td><td>

1.  Ensure that 'capability' text is within the **Value** field apart of the sn\_aia.supported\_tools sys prop.
2.  Create or find a skill tool that takes JSON as input.
3.  Apply that skill to a tool and then add to an agent.
4.  Run the agent in the playground.

Observe the execution log on the right hand side.


 Expected behavior: The user sees the actual JSON as an input for the skill tool.

 Actual behavior: The input is blank, causing the agent to fail.

</td></tr><tr><td>

AI Gateway - Security

 PRB1990717

</td><td>

AI Gateway Security Q1 Complete Feature Backport - Placeholder Story

</td><td>

 

</td><td>

This is a product update.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1934845

</td><td>

Make query boolean mode a first class parameter for search

</td><td>

When invoking AI search API, there should be a way to override the default query boolean mode. The goal is to first make NAVA default to OR mode.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1971388

</td><td>

IngestableDocument.getObjectSize isn't counting fEmbeddedDocuments

</td><td>

Indexing the document/table causes out of memory errors.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1972570

</td><td>

The display value in 'Location' gives the sysID rather than the country code

</td><td>

The issue occurs in the latest Zurich, Yokohama, and Now Assist instances. Sys\_user.country is working but sys\_user.location.country is not.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1990134

</td><td>

If all KBBs from one doc are removed from KB late binding, the post process stops and all following docs are returned

</td><td>

If ACL filtering removes all the embedded documents from a knowledge base article \(and there's no embedded match\), the code stops processing all subsequent documents.

</td><td>

1.  Ensure the KB is using ACL instead of UC 'glide.knowman.search.apply\_acls'=true.
2.  Create two KB articles:
    1.  For KB1, the user has ACL access, but cannot access any of the KBB.
    2.  For KB2, the user has no ACL access.
3.  As the user, search a query that matches KB1. \(Or use result improvement rule to boost KB1.\)

 Expected behavior: KB2 is not shown because the user has no ACL access.

 Actual behavior: KB2 is shown.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2006426

</td><td>

When a document with an attachment is removed by late binding, the next attachment where the user has access is also removed

</td><td>

When ds\_document\_version parent documents are filtered by an ACL and their children are skipped \(the continue at line 516–518 bypasses the recursive child processing\), the sys\_attachment sparse cursor falls out of sync. It was built assuming every child would be processed in order, but skipped parents leave gaps.

</td><td>

1.  Create 3 KBs with an attachment.
2.  Ensure that the KBs and attachments are relevant to a query. \(KB1 is most relevant. KB3 is least relevant but still matches a query.\)
3.  Add an ACL to block the second KB but allow the first and third.
4.  Force a late binding KB in ais\_datasource or the 'everything by' property.
5.  Query in a search preview as a user.

 Expected behavior: KB3 should be displayed with an attachment.

 Actual behavior: KB3 is displayed but with no attachment.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2008247

</td><td>

A negative offset isn't handled properly, which causes no results after moving to the next page

</td><td>

 

</td><td>

1.  Change the 'glide.ais.query.search\_operator' property to 'OR'.
2.  Perform a search on Service Portal which returns more than 12 results.
3.  Select the **Next Page** arrow button.

 Observe that there's no matches.

</td></tr><tr><td>

AI Search

 PRB1823355

 [KB2301356](https://hi.service-now.com/kb_view.do?sysparm_article=KB2301356)

</td><td>

When there is no scope or global for a scoped admin scoped app, an invalidate query is sent

</td><td>

AI Search doesn't work as expected and returns no results when searched with any query. On search preview, the message 'An error occurred. Check the logs for more details and contact Support if this issues continues' pops up before the query can even be triggered.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1838976

</td><td>

When Next Experience is off, searching for anything on the SOW/CSM workspace redirects the user to the homepage

</td><td>

This happens from Global Search. Instead of redirecting, it should display results using UI16.

</td><td>

1.  Open a Washington DC or Xanadu instance.
2.  Turn off the Next Experience by setting glide.ui.polaris.experience to 'false' from sys\_properties.
3.  Navigate to file navigator.
4.  Open Service Operations Workspace.
5.  Open the list from the left side panel.
6.  Select **All** under Incidents.
7.  Copy any incident number or search for any change/problem number.
8.  Search that number from the top-right search bar.

 Observe that it redirects to the homepage instead of displaying search results. If the user sets glide.ui.polaris.experience to 'true' from sys\_properties, then it displays search results inside SOW in a new tab.

</td></tr><tr><td>

AI Search

 PRB1841579

</td><td>

Sn-search-combobox-desktop's use of createGraphQLEffect dispatches errorActionType due to a 401 error for public GraphQL endpoints

</td><td>

The batch request fails due to 401 even though the GraphQL request in the batch was actually successful.

</td><td>

1.  Set the Service Portal home page to public.
2.  Set the Typeahead Search widget to public.
3.  Open Service Portal without logging in.
4.  Open Developer Tools.
5.  Select the Search Box.

 Observe in Seismic Dev Tools that the batch request failed due to 401. Then, observe in the Network tab that the GraphQL request in the batch was actually successful.

</td></tr><tr><td>

AI Search

 PRB1886370

</td><td>

AisHostnameProximityEstimator reads datacenter names from host names as case insensitive, but then compares them as case sensitive

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1896807

</td><td>

'Index All Table' from the list view of a datasource should trigger 'No block indexing' instead of 'Block reindexing'

</td><td>

This causes an event queue pile up when the user triggers multiple reindexing from the list view of the 'datasources' page.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1943058

</td><td>

There's a global search highlighting issue when using a Safari browser in Next Experience with Zing

</td><td>

There's a visual rendering issue affecting the search bar on the Support ServiceNow portal when accessed via Safari OS version 26. The text typed into the search bar isn't properly visible regarding the theme, making it difficult for users to interact with the search functionality.

</td><td>

1.  Log in to any instance.
2.  Select any available theme.
3.  Navigate to the support portal.
4.  Select the search bar and begin typing.

 Observe that the input text isn't rendered correctly, affecting visibility and usability.

</td></tr><tr><td>

AI Search UX

 PRB1980290

</td><td>

In the Service Portal with Now Assist enabled, when the tab focus is on the link and the 'Enter' key is pressed, the link doesn't open

</td><td>

 

</td><td>

1.  Navigate to **Conversational Interfaces** &gt; **Assistants**.
2.  Under Now Assist in Virtual Agent, select **Display Experiences** &gt; **Add service Portal** &gt; **Save**.
3.  Open any instance.
4.  Navigate to the Service Portal.
5.  Navigate to the search's **Edit** field.
6.  Type 'email' and search for it.
7.  Navigate to the **search results** &gt; **select a filter**.
8.  Navigate to **Any links** in the 'Results' section.
9.  Attempt to press the 'Enter' key to select.

 Observe that when the tab focus is on the link and the 'Enter' key is pressed, the link does not open.

</td></tr><tr><td>

AI Search UX

 PRB1981121

</td><td>

Global search isn't working with zoom in/zoom out

</td><td>

Global Search in the Native UI doesn't return results when the filter navigator is pinned and the browser zoom is set to 125% or 150%.

</td><td>

1.  Log in to an instance.
2.  Use the Native UI.
3.  Pin the filter navigator \(left navigation panel\).
4.  Set the browser zoom to 125% or 150%.
5.  Perform a global search for a known existing record.

Observe that the search returns 'No Record Found'.

6.  Change the zoom to 80% and repeat the same search.
7.  Verify that the results appear normally.

</td></tr><tr><td>

AI Search UX

 PRB2004210

</td><td>

A Zing component isn't loaded with an error on the console: '\_\_dyImp0\(...\).then is not a function'

</td><td>

Dynamic import fails as the component is already loaded by another module, in which case the dynamic import won't return a promise.

</td><td>

Navigate to an instance with Zing.

 On the home page, notice that the search bar doesn't load and an error appears in the console.

</td></tr><tr><td>

AI Search UX

 PRB2006200

</td><td>

Synthesized answer loading card status text isn't fully visible in a narrow viewport when non-English locale text exceeds container bounds

</td><td>

When a user performs an AI Search query in a narrow viewport \(reproducible via Chrome Responsive Design View on desktop\) on Service Portal without enhanced chat, and with the session language set to a non-English locale, the synthesized answer loading card clips overlap its content. The loading status text and any action elements within the loading card might overlap together rather than wrapping or expanding the container height. The synthesized answer and the underlying search results continue to function correctly; the issue is limited to the visual presentation of the loading card during the analysis phase. The behavior is triggered by the longer text strings used for loading status messages in non-English locales. For example, the German loading status text 'Ihre Anforderung wird analysiert' \(Analyzing your request\) is significantly longer than the English equivalent, and the loading card container does not wrap to accommodate it in a narrow viewport.

</td><td>

1.  Open an instance with ESC portal and Now Assist in AI Search with the session language set to German.
2.  Open Chrome and navigate to the AI Search page of ESC portal.
3.  Open Chrome Developer Tools and turn on 'Responsive Design' view \(toggle device toolbar\).
4.  Set the viewport to a narrow mobile width.
5.  Confirm that the instance language is set to German.
6.  Enter the search keyword 'übersicht fristen' in the search box.
7.  Submit.

Observe the synthesized answer loading card as it renders during the analysis phase.


 Expected behavior: The synthesized answer loading card displays the full loading status text without overlapping. The card container expands or wraps to accommodate the full text string regardless of locale or viewport width.

 Actual behavior: The synthesized answer loading card overlaps its content. The loading status text is not fully visible. The card does not expand to accommodate the longer German locale status text string in the narrow viewport.

</td></tr><tr><td>

Analytics Data API

 PRB1844011

</td><td>

Using 'trend by week' leads to incorrect record count when the new year starts

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1928857

</td><td>

The maximum number of groups on the heat map visualization in Platform Analytics resets to 10 when filtering

</td><td>

After saving and refreshing, the column count resets to 10. Instead, all selected groups should remain visible.

</td><td>

1.  Open an instance.
2.  Create a heatmap data visualization.
3.  Add a 'Group By' under Columns with more than 10 columns.
4.  Select **Apply.**

Observe that all columns display correctly at this point.

5.  Save and refresh the visualization or browser.

 Expected behavior: All selected groups remain visible after saving or refreshing.

 Actual behavior: The column count resets to 10 every time.

</td></tr><tr><td>

Analytics Data API

 PRB1931476

</td><td>

Issue with Incident SLA donut translation in Service Operations Workspace \(SOW\)

</td><td>

After changing the language in SOW, the Incident SLA widget appears as 'Breached'. After clearing the cache, it then appears as 'undefined'.

</td><td>

1.  Impersonate a user.
2.  Open SOW.

Notice that the Incident SLA widget label appears as 'Breached'.

3.  Change the language to any language.

Notice that the label still appears as 'Breached'.

4.  Clear the cache by cache.do.

 Notice that the label now appears as 'undefined' while the translation is already added in the sys\_ui\_message table.

</td></tr><tr><td>

Analytics Data API

 PRB1952604

</td><td>

The data label indicators show the same unit in Platform Analytics Data Visualization

</td><td>

After creating a data visualization that uses two indicators as data sources with different units, the data labels reflect the same unit.

</td><td>

1.  Create a data visualization \(line\).
2.  Add to the data sources with different units \(\# and % for example\).
3.  Show the data label.

 Expected behavior: The data label unit in each indicator reflects the unit of the indicator.

 Actual behavior: The data label units in both indicators are the same, and not respecting the configured unit of the indicators used as a base.

</td></tr><tr><td>

Analytics Data API

 PRB2001019

</td><td>

Accept 'group by' selection for all variable types

</td><td>

When comparing to classic reporting, many variable types are not available for selection in the 'group by' component in the Platform Analytics visualizations.

</td><td>

1.  Navigate to Platform Analytics Experience.
2.  Create a dashboard.
3.  Add a donut visualization:

    -   Datasource: sc\_req\_item
    -   Group by: variables
    -   Search for: Sample item
Notice only multi-choice and 'Select box' are available.

4.  Create the same visualization in classic reporting.

 Notice that there's a lot more options available.

</td></tr><tr><td>

Analytics Export API

 PRB1896576

 [KB2280342](https://hi.service-now.com/kb_view.do?sysparm_article=KB2280342)

</td><td>

Inconsistency in Platform Analytics scheduled export file types

</td><td>

While scheduling an export for List—Simple visualization, incorrect file types are shown when the property 'com.glide.par.unified\_analytics.enabled' is true and 'com.glide.par.v\_table\_join.enabled' is true or doesn't exist. The supported file types for List—Simple visualization export are PDF, Excel, and Embed List.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Analytics Export API

 PRB2001041

</td><td>

**Back** button and export functionality don't work with List

</td><td>

List component isn't compatible with Yokohama, so it should be backported. There are also List-related family changes.

</td><td>

 

</td></tr><tr><td>

Analytics Hub

 PRB1930155

</td><td>

'Comments created' date inside a widget displays the incorrect date

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1971605

</td><td>

The base version is grayed out in the new Application Manager

</td><td>

The base version is grayed out in the new Application Manager, which stops to install the custom version created on the base version 1.0.0. The new Application Manager allows to install the custom version only on the latest version.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1986694

 [KB2753355](https://hi.service-now.com/kb_view.do?sysparm_article=KB2753355)

</td><td>

App Manager and My Company Applications incorrectly show available updates after update checker

</td><td>

When publishing a new version of the app, it doesn't appear in 'My Company Application'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1992835

 [KB2804238](https://hi.service-now.com/kb_view.do?sysparm_article=KB2804238)

</td><td>

A deprecated Classic App Manager URL causes issues on some instances

</td><td>

Users have access to the Classic App Manager by navigating to the URI '/$allappsmgmt.do'. When they switched to new app manager later, and load the 'My company applications' page, that can corrupt the App Manager checksum cache, which causes the manual sync to fail.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Asset Management

 PRB1990771

</td><td>

Asset Analyst UI changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1990715

</td><td>

Token Exchange API for Voice Service Agent

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1977634

</td><td>

Change ATF test fails/flaps due to ATF steps timeout

</td><td>

 

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB1957741

</td><td>

On the CMDB Health Dashboard, a parent metric, like completeness, displays a total count of less than one of the sub-metric \(required or recommended\)

</td><td>

This causes totals to be incorrect.

</td><td>

 

</td></tr><tr><td>

Content Analytics

 PRB2002450

</td><td>

JavaScript sandbox replacement for app-content-automation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Content Experiences

 PRB2002443

</td><td>

JavaScript sandbox replacement for app-content-publishing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Content Governance

 PRB2002459

</td><td>

JavaScript sandbox replacement for app-content-governance

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Contextual Search

 PRB2010418

</td><td>

An admin user isn't able to add more additional resources to the search context \(cxs\_res\_context\_config\) table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Customer Operations for Customer Service Management

 PRB1879390

 [KB2052806](https://hi.service-now.com/kb_view.do?sysparm_article=KB2052806)

</td><td>

Viewing history for a csm\_consumer can trigger an update to the consumer record

</td><td>

This issue can occur when there's a difference between the address \(street, state, zip, country, or city values\) on the csm\_consumer record and its primary cmn\_location. It's caused by the client script 'Set type values' on csm\_consumer, which triggers on submit when the form view is 'case'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1999471

 [KB2820738](https://hi.service-now.com/kb_view.do?sysparm_article=KB2820738)

</td><td>

otherBlobsInChunkExist includes non-storage fields in coordinate comparison, causing premature S3 object deletion

</td><td>

The Archive Destroy job permanently removes archived records after they've aged past a configured retention period. It encounters a software defect that causes it to get stuck in a loop, repeatedly failing on the same set of records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1715251

</td><td>

There's a syntax error when adding a dot-walked column with the type 'fx\_currency' to a report

</td><td>

The user observes: Syntax - error or Access Rule Violation detected by database \(\(conne612968\) Unknown column 'task1 .amount' in held list'\).

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1968109

</td><td>

When glide.db.aggregate. groupby\_display\_optimize is true, group by reference fields display value is a sys\_id

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1939498

 [KB2814840](https://hi.service-now.com/kb_view.do?sysparm_article=KB2814840)

</td><td>

Migration to RaptorDB brings column length changes, which could impede archive table synchronization

</td><td>

The synchronization should run quickly, but this scenario can occur and slow down the process.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1970851

</td><td>

Glide enters 'Databaseless' mode after AHA failover is completed

</td><td>

This happens on an instance where the primary server is down.

</td><td>

1.  Open an instance where PG Fastaha is enabled and the primary server is down.
2.  Perform AHA failover.

 Observe that the failover is successful but app nodes aren't coming online. Glide entered 'Databaseless' mode.

</td></tr><tr><td>

Database Persistence

 PRB1965515

</td><td>

Minimize the impact of connection pool expansion throttling on scheduler jobs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1990231

</td><td>

Unable to install the Zero Copy Connectors plugin on production due to a conflict in the platform plugin ID

</td><td>

Users have a subscription and are entitled to the Zero Copy Connectors application, but can't install it due to a licensing issue.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB2005124

</td><td>

Plugin ID in LicenseUtil.java should be fixed

</td><td>

LicenseUtil.java checks whether a license for the Zero Copy Connector app exists on an instance using GlideLicenseAPI\(\). hasLicenseForFeature \(APP\_ID, ZCC\_LICENSE\_ID, false, true\). Currently, ZCC\_LICENSE\_ID is set to sn\_data\_fabric\_zcc. This should use the plugin ID instead of the scope name, so sn\_data\_fabric\_zcc needs to be changed to com.sn\_data\_fabric\_zcc.

</td><td>

On a Yokohama instance, try to create connection.

 Observe that it throws an error.

</td></tr><tr><td>

Declarative Actions

 PRB1975231

</td><td>

Field decorators for variable fields are cached in a way that causes issues, causing them to not show up sometimes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1937999

</td><td>

Discovery Schedule should support discovery of IPAM IPs and subnets

</td><td>

Currently Discovery Schedule only supports discovery IP address lists, IP Ranges and subnets configured in associated discovery\_range and discovery\_range\_item\_ip tables. This limits the ability to support integration of IPs from other sources such as IPAM.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1953520

 [KB2718488](https://hi.service-now.com/kb_view.do?sysparm_article=KB2718488)

</td><td>

ecc\_queue input records are stuck in IP jail, causing status cancellation

</td><td>

IPs are placed in a jail if it is suspected that multiple IPs on a schedule belong to the same device. IPs are supposed to be released from jail when the discovery of the device is complete. When this occurs, the IPs are never released from jail.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1981940

</td><td>

Add global scope support to allow application scope to delete cmdb\_file\_information records

</td><td>

The cmdb\_file\_information table is owned by the global scope and requires global-scope handling for controlled bulk deletions.

</td><td>

1.  Create or use an existing application scope.
2.  Implement logic in the application scope that requires deletion of records from the cmdb\_file\_information table using dynamic query conditions \(based on runtime parameters\).
3.  Attempt to perform the deletion directly from the application scope.

 Observe that the deletion can't be completed due to cross-scope access restrictions and/or the lack of a global-scope utility that supports dynamic, caller-defined queries.

</td></tr><tr><td>

Discovery

 PRB1996875

 [KB2801169](https://hi.service-now.com/kb_view.do?sysparm_article=KB2801169)

</td><td>

Cloud Infra Patterns are launched per datacenter, impacting GCP Discovery Schedules

</td><td>

GCP Discovery schedules take significantly longer to complete because the system launches one pattern execution per datacenter instead of one pattern per service account containing all datacenters. This results in a significant increase in probe executions.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB2003122

 [KB2896586](https://hi.service-now.com/kb_view.do?sysparm_article=KB2896586)

</td><td>

The Amazon Web Services \(AWS\) resource inventory box pattern stopped launching after Zurich for a non-US date format

</td><td>

It has a display value that is different from the instance.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery Probes and Sensors

 PRB1960340

 [KB2611107](https://hi.service-now.com/kb_view.do?sysparm_article=KB2611107)

</td><td>

Discovery's MID Server script files for Application Dependency Mapping are deleted during clones

</td><td>

The MID Server script file \(ecc\_agent\_script\_file\) records have attachments. These attachments may go missing after the instance is cloned, breaking Discovery probes. To retain the attachments of base instance code-related records in clones, the table\_name in the sys\_attachment table must be prefixed with ZZ\_YY. Discovery's names don't have that prefix, so the attachments may not be copied depending on the preserver/exclude settings for the clone.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1988914

</td><td>

Add functionality for Input Router to consider an entire document set

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Embedded Help

 PRB1912461

 [KB2774125](https://hi.service-now.com/kb_view.do?sysparm_article=KB2774125)

</td><td>

Default values for properties in an instance must change due to the docs' site URL change

</td><td>

Due to a change in website vendors and their inherent URL structuring, the URLs generated by the in-product help function are broken. Some system properties must be changed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Embedded Help

 PRB1975389

</td><td>

Add a check in Platform to control the access of foreign language content from Gumbo

</td><td>

Support has been extended to localized content in the Help Center framework. However, content in languages other than English isn't being published to Gumbo. There should be some control in the instance to avoid hitting the Gumbo to access the foreign language content.

</td><td>

 

</td></tr><tr><td>

Embedded Help

 PRB2008561

</td><td>

Update the list of allowed domains

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Employee Relations Case Management

 PRB2012556

</td><td>

Users can create more than one active Performance Improvement Plan \(PIP\) case for the same subject person

</td><td>

 

</td><td>

1.  Create an employee case for any user with the HR service as PIP.
2.  Move the case to the 'Ready' state.
3.  Create another case with same service and try to submit it.

 Expected behavior: The case shouldn't be created and an error should be thrown.

 Actual behavior: It gets submitted and a new case is created.

</td></tr><tr><td>

Encryption Support

 PRB1993181

</td><td>

Flow session cloning \(PFSessionClone\) needs to load all roles, including snc\_internal

</td><td>

GlideSecurityManager. get\(\).getRoles\(\) has side-effect of removing snc\_internal role when explicit roles plugin is enabled. Using GlideSecurityManager.get\(\).getRoles\(true\) will prevent this side-effect.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1902287

</td><td>

Users can't uninstall sn\_em\_ai\_overview and sn\_em\_ai\_action because they're part of core-ui-components/ 'Core UI Components'/ sn\_core\_ui\_ponents

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1990235

</td><td>

Add an entry point to sanitize an HTML field before insert

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1879472

</td><td>

Sub-flow context can't be opened after an upgrade to Yokohama

</td><td>

There's a deserialize error when viewing a flow context that has a static value assigned to the subflow output. The error stack can be located in the logs.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1944299

</td><td>

'Extension point not found' exception from com.glide.hub.action \_step.script plugin

</td><td>

The **Send\_notifications** action executed on a node with new code has no error. The **Send\_notifications** action executed on a node with old code errors out with an exception.

</td><td>

1.  Open a Yokohama or Zurich 2-nodes TD instance.
2.  Generate Now Assist Troubleshooting Notifications.
3.  Upgrade node 1 to a more recent release.

 Expected behavior: The **Send\_notifications** action is executed on both node 1 and node 2 without any error.

 Actual behavior: The **Send\_notifications** action executed on node 1 \(the new code\) has no error. The **Send\_notifications** action executed on node 2 \(the old code\) errors out with an exception.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1990495

 [KB2780048](https://hi.service-now.com/kb_view.do?sysparm_article=KB2780048)

</td><td>

The **Update record** action updates an invalid GlideRecord and triggers business rules when the reference record is deleted while a flow is in progress

</td><td>

When the record that is passed to a subflow is deleted while the flow is in progress, any **Update record** action in the subflow doesn't error out with 'Glide record is invalid' type errors. Instead, the **Update record** action in the subflow falls back and iterates on all records in the table, causing substantial data impact.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

GlideRecord

 PRB1990713

</td><td>

MID Server core logic for Collector Framework

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

GraphQL API

 PRB1971431

</td><td>

Extremely large tables are queried from GlideRecordSchema, causing out of memory errors

</td><td>

Out of memory exceptions are occurring in the GraphQL framework when GlideRecordSchema is invoked to query tables with extremely high record counts. The cause looks to be from GlideGraphQLQueryHolderImpl .getRowCount returning the rowCount of the GlideRecord when it should be providing the pagination limit size. The value from that method is used to initialize an ArrayList of the provided size in the graphql-java framework ExecutionStrategy.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB2004216

</td><td>

Update now-avatar properties to receive styling for AI avatars for AI Specialists

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HTML Field Type Editor

 PRB1990982

</td><td>

Predictive text assistance

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HTTP Client

 PRB1992475

</td><td>

Asynchronous HTTP client upgrade for complete feature change

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1775255

</td><td>

Increase the attachment limit in the SFTP step in Integration Hub

</td><td>

There's a hard-coded value of 100,000 KB for SFTP imports. When the user attempts to import more than the hard-coded limit, it fails. Even though it lets the user to set a limit, if it is higher than 100,000 KB, it isn't allowed.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1989692

</td><td>

Page details are missing from the execution details for Datastream Actions when run via FlowAPI

</td><td>

The 'Page Details' section is missing and the user is unable to view step-by-step execution data \(Pagination Setup, Integration Metadata, Step Configuration, API request/response\).

</td><td>

 

</td></tr><tr><td>

Internationalization Features

 PRB1892286

 [KB2277705](https://hi.service-now.com/kb_view.do?sysparm_article=KB2277705)

</td><td>

A non-admin user can't change a dashboard name by specific steps when the system language is set to Japanese

</td><td>

The dashboard name should be updated correctly and reflected in both the primary record and its translated fields, as it is in the Washington DC and Xanadu versions. In the Yokohama version, the update to the dashboard name fails silently when the Japanese language is enabled and the sys\_translated record exists.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

JVM at Scale

 PRB1967652

</td><td>

Expose microsecond level print of latency to DB into stats/xmlstats for easy bigdata ingestion

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1976775

</td><td>

A KB's article title is empty under the 'Event property values' column in the 'Article Title' report

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Navigate to the User Experience Analytics dashboard.
3.  Select **Employee Center** in the menu.
4.  Navigate to **Data Foundation** &gt; **Events section**.
5.  Open the 'View Knowledge Article' event.
6.  Under 'Event properties', navigate to the 'Article Title' and 'Article SysID' widgets.

Observe the '...' empty value on the report chart.

7.  Export the data to Excel.

 Observe the exported report contains an empty field under the first column labeled 'Event property values'.

</td></tr><tr><td>

Knowledge Management

 PRB1981407

</td><td>

After Zurich, the **Source task** field for knowledge articles isn't assigned

</td><td>

This issue occurs when a user creates a feedback task record for a knowledge article. The feedback task allows knowledge managers to either edit the existing article or create a new one. However, when users attempt to create an article from the feedback task, the new article doesn't reference the originating feedback task as it does in Yokohama. The **Source Task** field, which should contain this reference, appears in the article form view, but it is grayed out and empty.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1992747

</td><td>

Now Assist KB creation pop-up is unable to continue with the KB creation when no tasks are available for search

</td><td>

This issue occurs only in Native UI. Using the **Create knowledge** UI from Native UI during KB creation shows no options available to continue without selecting tasks. This blocks KB creation.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1894732

</td><td>

When a column is grouped, incorrect sys\_ids are returned

</td><td>

 

</td><td>

1.  Add a record list bundle to the UIB page with groupby Number.
2.  Create a declarative action.
3.  Preview the page.
4.  Select the record.
5.  Select the **Demo** button.
6.  Check the console.

 Observe that the returned sys\_ids are improper.

</td></tr><tr><td>

List Administration

 PRB1991341

 [KB2803013](https://hi.service-now.com/kb_view.do?sysparm_article=KB2803013)

</td><td>

Unable to update **User** field / other fields at Certification Task level

</td><td>

In the Certification Task record, under the inline level, the **User** field or other editable fields are not editable. When attempting to change the value by double-clicking \(or using the keyboard shortcut\) on the field, the field goes into a loading state and never allows selection of another.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Major Incident Management

 PRB1960650

</td><td>

There's a slow SQL query on multiple instances when executing the 'ContactManagementEngine .java\#L210'

</td><td>

.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1963685

 [KB2633251](https://hi.service-now.com/kb_view.do?sysparm_article=KB2633251)

</td><td>

MID Server File Sync doesn't sync attachments when the sys\_attachment table name is prefixed with ZZ\_YY to prevent clones deleting the attachments

</td><td>

Attachments of MID Server Synched File records, such as MID Server Script File \[ecc\_agent\_script\_file\] records, aren't synced to the MID Server when the sys\_attachment table name is prefixed with ZZ\_YY to prevent clones deleting the attachments. The MID Server platform should be expecting not only the actual table name, but also table name prefixed with ZZ\_YY when querying the instance for the attachment.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1966095

 [KB2659568](https://hi.service-now.com/kb_view.do?sysparm_article=KB2659568)

</td><td>

Auto MID selection causes excessive metrics to accumulate when connection issues occur

</td><td>

The MID server during auto-mid-selection can experience excessive memory allocation and CPU spikes due to agents connecting with network connectivity issues. As part of auto-mid-selection, agents make REST based calls to the MID server querying for the number of connected agents in order to perform load balancing and honor the maximum number of agents connections allowed. Part of this call will generate a metric instance for tracking which accumulates and can potentially block other thread calls to the MID web server hosting the REST calls. The result is the MID server experiences heavy CPU spikes and excessive memory retention while agents attempt to find the correct MID server to connect with. Coupled with network interruptions, this can result in the MID server running out of memory.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1971767

 [KB2678137](https://hi.service-now.com/kb_view.do?sysparm_article=KB2678137)

</td><td>

Agent Client Collector policies aren't synced to agents after MID restart and agent reconnection

</td><td>

The MID server currently has an issue where the policies and their check instances are not associated for tracking if the config\_publish ECC queue message has been processed by the MID server before the offline agents reconnect. The information will be present in the policy tracking mechanism, but the flow that processes the message sent to an agent during keep alive processing will not contain the up-to-date policies and their check instances due to the missing associations.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB2012665

 [KB2953193](https://hi.service-now.com/kb_view.do?sysparm_article=KB2953193)

</td><td>

MID Server upgrades fail because the mid.max.extract .file.size property default is too low

</td><td>

The MID Server property mid.max.extract .file.size property default of 500MB is too low for MID Server upgrades. Upgrades fail at the download/extract stage with the following errors, after the mid-core zip file has been successfully downloaded: '...Exceeds the maximum size \(500000000\). Unable to download package. The size of uncompressed files is too big or too many entries in the zip file'. This fails before the MID Server is shut down, avoiding outages, but causes repeated failed upgrades. The risks of running with an instance vs MID Server incompatibility, that generally has been known to break some features and cause data loss.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Experience for Field Service Management \(Glide Family\)

 PRB1978601

</td><td>

Offline Mode fails with an error due to FSM Data Item query fetching assets even if the **Location** field is empty

</td><td>

 

</td><td>

1.  Configure the Field Service Mobile plugin.
2.  Have many records in wm\_task where the 'Assigned to user' has their **Location** field empty, which will be returned by the 'DI\_my\_inventory\_remove\_parts' data item.
3.  Log in to Agent Mobile with FSM active.
4.  Enable Offline mode.
5.  Attempt to download cache.

 Notice that an error occurs.

</td></tr><tr><td>

Mobile Platform

 PRB2006346

</td><td>

The offline V2 sync API returns cumulative table snapshots in each execution result

</td><td>

This issue has been present since Yokohama or earlier and affects the Mobile Agent during offline-to-online sync. When a user performs multiple record edits in offline mode and then reconnects, the sync API processes each queued action and generates a RefreshedDocument per execution result. Due to the cumulative snapshot behavior, each execution result incorrectly includes the data of all previously synced records — not just the one modified in that action. This causes the response payload to grow at an N² rate: N offline edits produce N² total records across all execution results. The impact is significant. Users who perform hundreds of edits in offline mode can experience sync payloads exceeding 100MB+, leading to severe performance degradation, potential sync failures, and a poor user experience at the moment of reconnection.

</td><td>

1.  Provision an instance with Field Service Management with demo data installed.
2.  Log in to the agent app with a field agent user.
3.  Navigate to the offline settings.
4.  Download the offline cache.
5.  Go offline.
6.  Open a work order task form screen and make an edit.
7.  Open a separate work order task and make an edit.
8.  Navigate to settings.
9.  Sync online.

 Expected behavior: In the offline synchronize response, the **Document** &gt; **Data** &gt; **Tables** for each execution result should only contain the record that was edited.

 Actual behavior: The **Document** &gt; **Data** for each execution result contains the data for both records in each execution result.

</td></tr><tr><td>

Natural Language Query \(Family Release\)

 PRB1992648

 [KB2794876](https://hi.service-now.com/kb_view.do?sysparm_article=KB2794876)

</td><td>

com.snc.nlq.MetadataGenerator modifies GlideElement objects in TableDescriptorCache

</td><td>

This issue is observed in production.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Normalization Data Services

 PRB1931854

 [KB2664685](https://hi.service-now.com/kb_view.do?sysparm_article=KB2664685)

</td><td>

A core company isn't handled correctly for a domain-separated environment

</td><td>

In a domain-separated environments with Normalization Data services turned on, creating models or configuration items may fail or use an incorrect manufacturing \(publisher\) company. When selecting a manufacturer from a specific domain, the system incorrectly replaces it with a company record from the user's domain.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now Assist Panel

 PRB1985088

</td><td>

Link in NASS doesn't open in a new tab

</td><td>

 

</td><td>

1.  Navigate to full page.
2.  Search 'What is spam?'.
3.  Select the source link for the KB.

 Expected behavior: The KB link opens in a new tab.

 Actual behavior: The KB link doesn't open at all.

</td></tr><tr><td>

On-Call Scheduling

 PRB1981295

</td><td>

OnCallRotation. getPrimaryUser returns null when there's no members on a roster and only coverage present

</td><td>

.

</td><td>

1.  Log in to instance.
2.  Make sure an assignment group has the roaster with no members and has only the Primary Coverage.
3.  Execute the script.

 Expected behavior: The user id is returned.

 Actual behavior: The result is null.

</td></tr><tr><td>

OneExtend

 PRB1981515

</td><td>

Add enhanced debug logging around async client call

</td><td>

Debug logs need to be added when each streamed chunk is received, when the final callback is received \(VAStreamConsumer\), before enqueueing in the hybrid queue, and after enqueueing in the hybrid queue and the callback is complete.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1997461

</td><td>

NowLLMStreamReader.parse\(\) splits on 'data:' inside JSON content, corrupting LLM stream output

</td><td>

NowLLMStreamReader.parse\(\) uses data.split'data:' to split SSE \(Server-Sent Events\) frames. This splits on all occurrences of the literal 'data:' — including those embedded inside JSON string values in LLM output. When the LLM produces certain content, the split fragments the JSON into unparseable pieces. Jackson silently fails \(catches Exception in extractResults\), content is lost, and the feature invocation stays stuck in 'processing' with null output.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1998199

</td><td>

NAVA gets stuck intermittently

</td><td>

 

</td><td>

1.  Ensure Response Streaming is enabled.
2.  Open NAVA.
3.  Enter 'Creator.'

 Notice that NAVA will get stuck intermittently.

</td></tr><tr><td>

Performance Analytics

 PRB1948103

</td><td>

After upgrading from Xanadu to Yokohama, the line chart appearance changes for the 'current year vs. last year' comparison report using data sets

</td><td>

This fix requires manual change of a report property. Set 'Allow data label overlap' to true from sys\_report record. After having patch for this feature, the customer needs to update this property for each required report manually. This can be done from platform list by adding column 'Allow data label overlap'.

</td><td>

1.  Open any Xanadu instance.
2.  Create a Line report on sys\_trend with the following:
    1.  Trend on: Created
    2.  Condition \(Dataset A – Current Year\)
    3.  Add a second dataset with the same configuration but for last year.
    4.  Condition \(Dataset B – Last Year\)
3.  Save the report.

Observe the chart appearance in Xanadu.

4.  Upgrade the instance to Yokohama.
5.  Open the same report.

 Observe the chart appearance again.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1984668

</td><td>

There's a column filter issue in the Data Visualization library page, in which the 'Does Not contain' isn't working on the 'Owner' column

</td><td>

Applying the 'Does not contain' filter on the 'Owned by' column does not filter the records properly.

</td><td>

1.  Navigate to the Data visualization library page.
2.  Apply the 'Does not contain' filter on the 'Owned by' column.

 Expected behavior: All the records should be filtered by the applied filter value.

 Actual behavior: It is not filtered properly when there are multiple values.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1843154

</td><td>

Not able to save a dashboard after editing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1846141

</td><td>

Certain missing properties for a visualization can cause side effects

</td><td>

Some impacts include drilldowns in a dashboard not working, and the **Save** button being enabled without any edit.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1969752

</td><td>

Cached toolbox items cause options to remain in a previously selected language

</td><td>

While working on the Platform Analytics Dashboard and Data Visualization modules, users have observed that the language in the right-hand menu changes automatically without any user action. The issue occurs intermittently. Sometimes, it appears only in a single browser session, while at other times it affects multiple browsers simultaneously. No consistent trigger has been identified so far. Users report that refreshing the page or clearing the cache may temporarily resolve the issue, but it can recur unpredictably.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1983811

</td><td>

Unexpected response format for users without assigned roles

</td><td>

The API should return properly formatted JSON with error code, but instead it returns an invalid format.

</td><td>

Run GetMobileVisualizationIT \#verifyAsNoRoleUser.

 Expected behavior: The API returns properly formatted JSON with error code.

 Actual behavior: The API returns an invalid format.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2000628

</td><td>

DashboardWidgetDao.update\(\) does not persist **widget\_props** field

</td><td>

When updating a dashboard widget record via DashboardWidgetDao.update\(\), the **widget\_props** field is not written to the par\_dashboard\_widget table. The create\(\) method correctly calls gr.setValue\(WIDGET\_PROPS, widget.getWidgetProps\(\)\), but the update\(\) method is missing this call. This causes widget-level property overrides \(for example, followFilters, header color, header title\) to be saved on initial widget creation but silently lost on any subsequent dashboard save.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2003609

</td><td>

After migration, widget settings are lost

</td><td>

All of the widget related properties \(follow filter, header settings, etc\) should be migrated to the widget\_props of par\_dashboard\_widget table.

</td><td>

1.  Create a CoreUI dashboard.
2.  Add a report widget that's used in other dashboards and set the header alignment to be center.
3.  Migrate the dashboard.
4.  Verify that the par\_visualization record is created for the sys\_report.
5.  Open the dashboard in PAE.

 Expected behavior: The header alignment settings are migrated.

 Actual behavior: The header displays with the default settings.

</td></tr><tr><td>

Platform Runtime

 PRB2014434

</td><td>

The Granular Delegation API isn't returning any results

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1984620

</td><td>

Loading of sys\_pd\_process\_definition\_ c5142dddff37e21082a8ffffffffff2d taking two hours

</td><td>

This issue occurs when upgrading Yokohama and Zurich.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1991515

</td><td>

After a restart, the stage is still displayed even when the conditions aren't met

</td><td>

Remnants from the previous playbook lanes remain visible, although they appear in a 'PENDING' state. However, those lanes are reached, they update correctly.

</td><td>

1.  Navigate to **Configurable Workspace** &gt; **Lists** &gt; **AGR Connections** &gt; **All**.
2.  Create a record with subcategory 'WebEDI'.
3.  Proceed with Playbook.
4.  When asked for 'Fast Follower', select **True**.
5.  Proceed with Playbook until 'Packaging Data Exchange' \(lane 7\) is reached.
6.  Perform the complete Playbook restart.
7.  Proceed with Playbook to 'Validate Connection Type' \(activity 1.4\) activity.
8.  Change the subcategory to 'ClassicEDI'.
9.  When asked for Fast Follower, select **False** and proceed.
10. Proceed with Playbook until 'Testing' \(lane 9\) is reached.
11. Perform the complete Playbook restart again.
12. Proceed with Playbook to 'Validate Connection Type' activity.
13. Change the subcategory to 'WebEDI'.
14. When asked for Fast Follower, select **False** and proceed.

Observe that the 'Fast follower' phase is initiated even if the fast follower is not marked, which isn't correct. Also, observe that even if the subcategory is 'WebEDI' now, the phases / activities for 'ClassicEDI' are still initiated, which isn't correct.


 Expected behavior: If fast follower is set to true, then WebEDI and ClassicEDI don't appear on the playbook. If fast follower is set to false, then WebEDI or ClassicEDI appear on the playbook.

 Actual behavior: If fast follower is set to true, WebEDI and ClassicEDI appear on the playbook. If fast follower is set to false, then fast follower, WebEDI, and ClassicEDI appear on the playbook.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1992485

</td><td>

Remove sys\_ids from Playbook-fetched telemetry metrics

</td><td>

Process definition information isn't included as part of data that is captured.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1999600

</td><td>

Playbook with questionnaire activity is not activated by default in Yokohama instances

</td><td>

When apps are uploaded from Nexus or from a zip file, and they contain playbooks with questionnaire activities, those playbooks are missing trigger data. When a playbook has a questionnaire activity, a line gets added to the XML that causes everything after that line to fail to load.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization \(Glide Family Channel\)

 PRB1988877

</td><td>

Fix default skill level logic for Schedule Optimization 1.1

</td><td>

An additional validation is needed to ensure that the default skill level is returned correctly for skills.

</td><td>

 

</td></tr><tr><td>

Search Administration

 PRB1968215

</td><td>

Elements must only use supported ARIA attributes for the **Search catalog** field for Service Portal \(SP\)

</td><td>

 

</td><td>

1.  Ensure there are multiple requests raised in SP.
2.  Launch a base instance.
3.  Navigate to **Request** on the header menu and activate it.

Notice that multiple records are displayed.

4.  Choose any request.
5.  Open the Request summary.
6.  Navigate to **Search catalog**.

Notice that menu items are displayed.

7.  Run 'Evinced Flow Analyzer' and AXE devtool.

Observe the issue.


 Expected behavior: The ARIA attribute is not allowed as seen in 'aria-selected='false'' and an element's role supports its ARIA attributes.

 Actual behavior: Elements only use supported ARIA attributes, as seen in the element location: sn-search-combobox, sn-search-combobox-desktop,. -search-popover\_\_item--is-active.

</td></tr><tr><td>

Service Catalog Builder

 PRB1982503

</td><td>

In Yokohama, the **Continue** button doesn't work and the **Preview** button is missing in the canvas view of t2c- 6.0.7

</td><td>

 

</td><td>

1.  Open a Yokohama instance with NAFC 27.6.1.
2.  Enable the T2C skill.
3.  Navigate to **Catalog Builder**.
4.  Select **Build with Now Assist**.
5.  Enter any utterance.

 Observe that the **Preview** button is missing and the **Continue** button doesn't work.

</td></tr><tr><td>

Session Management

 PRB1962465

</td><td>

Performance degradation with build 1108

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB1975879

</td><td>

PPN lookup shouldn't be performed for empty PPNs

</td><td>

If there is a corrupted PPN record where the part number value is empty, it will be returned and set in the PPN reference value.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB1993170

</td><td>

Pass the auto-incremenator using the unique ID of the table rather than using the contract number

</td><td>

There should be automation for both scenarios: 1. Uploading the docs, finishing the flow, and importing another doc to the same contract. 2. The asset covered from both docs should be part of the same contract.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB2001908

</td><td>

Rename the **Ignore** button to 'Exclude'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB2001911

</td><td>

Update text on the content opt-in page

</td><td>

Software entitlement details are extracted from software contracts using AI. Opt-in to the content service to help improve the prediction for product, publisher, and edition values.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1936688

</td><td>

Add-On Publisher values are not populated properly

</td><td>

When Content is shipping Add-On Publisher life cycles, it gets defaulted to Publisher value instead of Add-On Publisher.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1975292

</td><td>

Contract start date parsing doesn't work as expected

</td><td>

The issue occurs when alphanumeric input is given. The **Organization ID** field should be set to read-only after successful validation.

</td><td>

1.  Open the docusign integration profile form.
2.  Set Integration type = Org Level.
3.  Set the contract renewal date to any number.

Observe that the contract renewal date is checking for integers, but the functionality is different in classic and workspace. In classic, any alphanumeric value is reduced to just integers. In workspace, the value stays as-is and a warning message appears.

4.  Open the DocuSign integration profile form again.
5.  Set Integration type = Org Level.
6.  Populate the fields.
7.  Save.
8.  Validate.
9.  Change the org ID.
10. Save again.

 Observe that the **Organization ID** field isn't set to read-only after successful connection validation.

</td></tr><tr><td>

Software Asset Management

 PRB2001199

</td><td>

Trigger flow and alternate flows

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Time Card Management

 PRB1988000

 [KB2760220](https://hi.service-now.com/kb_view.do?sysparm_article=KB2760220)

</td><td>

Managers are no longer able to add time cards for their direct reports and delegates in the Time Sheet Portal

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Field Administration

 PRB1962435

</td><td>

There's an incident form load issue due to the missing macro sn\_wwna\_nacm\_component, which causes a performance issue

</td><td>

When loading an incident form, the local host log is consistently flooded with the 'DBMacro WARNING \*\*\* WARNING \*\*\* Macro missing: sn\_wwna\_nacm\_component', and this is causing the form to load slowly.

</td><td>

1.  Open any incident record in the instance.
2.  Navigate to **System Diagnostics** &gt; **Session Debug** &gt; **Enable All**.

 Observe the error in the localhost log. The warning is called many times: 'DBMacro WARNING \*\*\* WARNING \*\*\* Macro missing: sn\_wwna\_nacm\_component'.

</td></tr><tr><td>

UI Field Administration

 PRB1990980

</td><td>

Add backend support for the multi-section configuration and fetch configurations in the UI to create the BE layer

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1990983

</td><td>

Support core IT use cases

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1920717

</td><td>

Hyperlinks in annotations on forms are not opening in a new window

</td><td>

Hyperlinks open in the same tab instead of opening in a new tab.

</td><td>

1.  Open a base instance.
2.  Open an incident table.
3.  Open any incident.
4.  Select and hold \(or right-click\) and navigate to **Configure** &gt; **Form builder**.
5.  Create an annotation with the code.
6.  Open the incident in SOW.
7.  Under 'Details,' select the link.

 Expected behavior: It opens the link in a new tab.

 Actual behavior: It opens the link in the same tab.

</td></tr><tr><td>

UI Form Administration

 PRB1959255

</td><td>

g\_form.clearValue shouldn't clear a choice field if the field is empty or has the default value

</td><td>

In Service Operations Workspace, the onChange client script only runs in the workspace if a reference isn't on the layout.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1971158

</td><td>

A blank screen displays when a user tries to access the ast\_contract record present in another domain

</td><td>

When the user doesn't have access to the record, globals are coming as undefined, and aren't adding the default value of \{\}. This causes a JS error later in the processing, which results in the blank screen.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1972511

</td><td>

Invalid payload event for CTRL\_RECORD\# MACROPONENT\_PROPERTY\_CHANGED

</td><td>

There are properties that are defined in the CTRL\_RECORD\# MACROPONENT\_PROPERTY\_CHANGED event definition. The properties are not stored in the cached payload due to a parsing error. getProperties returns no properties due to a parsing error.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1993929

 [KB2908761](https://hi.service-now.com/kb_view.do?sysparm_article=KB2908761)

</td><td>

RCAs are created with the source as 'sys\_ws\_operation.do? sys\_id=6986d96dff7322102 ae8ffffffffff48' for HR apps

</td><td>

An RCA is generated: 'RCA triggered - 'Read operation on table 'sn\_doc\_html\_template' from scope 'Global' was denied. The application 'Document Templates' must declare a Restricted Caller Access privilege. Please contact the application admin to update their access requests'. None should be generated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB2004264

</td><td>

Updates to support AI Specialist and draft note

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2011302

</td><td>

An API /api/now/ai\_agent/modified\_fields call on a form load increases the browser time

</td><td>

An API call has been added for every form operation as part of the platform engine feature '/api/now/ai\_agent/modified\_fields'.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB2002024

</td><td>

There's an inaccuracy in IH transactions DEFN ID

</td><td>

The 'IH Usage' table has an accrual month logic, where the same record is updated every single day for the rest of the month. The IH transactions fabric credits DEFN ID only fetches the first day reporting of usage on a record, and not the rest of the 29 days.

</td><td>

 

</td></tr><tr><td>

UXF Macroponent

 PRB1899084

</td><td>

The technical dashboard override isn't applied when switching domains in UI Builder \(UIB\)

</td><td>

 

</td><td>

1.  Open an instance with the 'Domain separation' plugin installed.
2.  Create a technical dashboard within the global domain.
3.  Add a data visualization to it.
4.  Switch to another domain.
5.  Create a page override.
6.  Add an additional data visualization to the overridden page.
7.  Preview the created dashboard pages from UIB by switching domains.

The page content changes as expected.

8.  Open the technical dashboard via the Platform Analytics experience.
9.  Switch domains to check the page content.

 Expected behavior: The overridden page variant should be displayed for the domain.

 Actual behavior: Only the global page variant is displayed in the domain.

</td></tr><tr><td>

UXF Macroponent

 PRB2009619

</td><td>

Multiple stuck threads cause semaphore exhaustion, requiring a node restart

</td><td>

There's a stuck semaphore transaction related to the function createCacheablePageFragmentFromShell in CacheablePageFragmentFactory.java. This can lead to multiple threads being stuck with no option but to restart the node to provide relief.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1947452

 [KB2601019](https://hi.service-now.com/kb_view.do?sysparm_article=KB2601019)

</td><td>

UX screen record allows the **Parent Macroponent** field to be set to the screen within the same screen collection as the current screen record

</td><td>

This results in an invalid screen configuration.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1966630

</td><td>

Workspace tabs aren't rendering screens

</td><td>

Loading a record page via select through \(hydrate\) is missing the audience applicability check \(present in direct load\), leading to incorrect screen variant resolution.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1990140

</td><td>

Framework support for the AI screen reader Store app

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Versatile Node and Cluster Configuration

 PRB1819117

</td><td>

Upper case datacenter name results in no triggers being executed

</td><td>

DNS PTR \(reverse-DNS\) records return hostnames with uppercase 'ABC123' instead of the expected lowercase 'abc123'. Comparison checks in HostnameProximityEstimator should be case insensitive.

</td><td>

 

</td></tr><tr><td>

Versatile Node and Cluster Configuration

 PRB2002618

</td><td>

There's an AHA check failure due to a node\_id mismatch from capitalizing the host name

</td><td>

Domain Name System \(DNS\) PTR \(reverse-DNS\) records can return host names with uppercase instead of the expected lowercase. The HostUtil.getHostname\(\) should return lowercase.

</td><td>

1.  Start a node with a set system\_id.
2.  Note the node\_id.
3.  Modify the system ID to have 'AMS' capitalized.
4.  Restart the instance.
5.  Observe that the node ID is now different.
6.  Modify the system ID back to the original value.
7.  Restart the instance.

 Observe that the node ID is now back to the original.

</td></tr><tr><td>

Virtual Agent

 PRB1916016

</td><td>

The **End Conversation** action does not end live agent interaction when the Post Chat survey is enabled

</td><td>

The interaction and conversation should be closed once the user responds to the survey.

</td><td>

1.  Start a conversation with a Live Agent using VA API.
2.  Make sure the Post Chat survey is enabled with the 'Requester Ended' flag.
3.  Exchange messages between the agent and user.
4.  Initiate the **END\_CONVERSATION** action from the user.

 Expected behavior: The interaction closes when the user ends the conversation, then the survey is presented to the user. This behavior can be verified from webclient as well.

 Actual behavior: The interaction is kept open and the survey is presented to the user.

</td></tr><tr><td>

Virtual Agent

 PRB1919055

</td><td>

Add a new property to turn off the 'shorten responses' feature by default

</td><td>

After upgrading Xanadu, shorten responses were added and set as 'on' by default. There is no method to set up shorten responses to 'false' as default. The user cannot see the full test display as default as before.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1960339

</td><td>

The **Use an AI agent** action moves to a 'Waiting' state when called inside a flow-logic component

</td><td>

In a use case where calling the agent multiple times in a single subflow/flow using the flow-logic, the agent is initially called, but the second call goes into 'Waiting' state and no other calls go through. In the second call to the same agent \(with a different objective\), the execution record's state is 'Ready' and the message 'Conversation data is not populated' occurs for the second record. This leads the action to be in 'Waiting' state. The sysevent record is also not created.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1973526

</td><td>

The business rule 'VA Phone Interaction - On Close' is not firing in the 'wrap\_up' state

</td><td>

The outcome of this issue end to end is this is causing an interaction that is intended to be closed by the agent \(so has entered wrap up\) resurfacing when the same caller makes consecutive calls before wrap up is finished.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1978979

</td><td>

The session should not get timed out during the execution of topic as a tool when run as an AI User

</td><td>

The user session is getting timed out after uploading the attachment.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1982735

</td><td>

Handle an unknown **document\_id** field in the sys\_cs\_provider\_application

</td><td>

 

</td><td>

1.  Set up Glide NLU or Now Assist.
2.  Set up the appropriate Teams version.
3.  Start a conversation from a bot.

 Logs have an unknown field **document\_id** in sys\_cs\_provider\_application exception for every Teams request.

</td></tr><tr><td>

Virtual Agent

 PRB1984195

</td><td>

Interactions are reused every time the startVoiceInteraction Voice API is invoked

</td><td>

The API should create an interaction, but instead it reuses the interaction if it's active. This used to work correctly in Yokohama, but is now failing.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1985280

</td><td>

Duplicate attachment is displayed in Virtual Agent after portal refresh

</td><td>

 

</td><td>

1.  Open an instance in two browsers.
2.  In browser one, impersonate the agent 'Fred Luddy'.
3.  Set the agent as available in Service Operations Workspace.
4.  Switch to browser two.
5.  Impersonate as admin.
6.  Initiate a chat from the portal or web-client.
7.  Connect to a live agent.
8.  In browser one, accept the chat as the agent.
9.  Send any image as end-user to agent.
10. Refresh the portal at end-user.

 Expected behavior: Nothing happens.

 Actual behavior: The duplicate attachment/image is displayed only in Virtual Agent.

</td></tr><tr><td>

Virtual Agent

 PRB1989732

</td><td>

The assistant\_personalization system property should handle default case properly for branding and personalization

</td><td>

When updating the sn\_nowassist\_va. assistant\_personalization system property to a random value, it doesn't behave the same as the default value.

</td><td>

1.  Open the sn\_nowassist\_va. assistant\_personalization system property.
2.  Update the value to a random value, different from the given three choices.
3.  Run a query in the Virtual Agent portal connected to the assistant that has personalization.
4.  Navigate to the **sys\_generative\_ai\_log** table.
5.  Locate the record for either AIA Unified Planner, AIA Unified Planner Quick, or AIA Planner.
6.  Review the record and verify that the configured persona is appearing in the prompt, in between &lt;persona&gt; and &lt;/persona&gt;.

 Expected behavior: It behaves the same as the default value, and should return only agent\_persona from the configuration attribute table.

 Actual behavior: It behaves as TONE\_RESPONSE\_LEN\_PERSONA and returns all the details.

</td></tr><tr><td>

Virtual Agent

 PRB1990179

</td><td>

Language Detection from French to English doesn't show the topic name in English

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1992132

</td><td>

The Virtual Agent \(VA\) link menu items are not displayed correctly

</td><td>

In Enhanced chat, VA link menu doesn't show the labels the way it shows on the standard chat. Instead it shows the label as plain text and shows the link below. If the link is longer, it increases the width of the 'Contact support window'. It should only show the label and shouldn't show the link.

</td><td>

1.  Open the Menu items from the branding.
2.  Add a long link.

 Notice that the width of the window increases beyond the chat window, and the label is shown in plain text and the link shows.

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1980510

</td><td>

Allow linking for AI agent user type from AI agents app

</td><td>

When the user triggers auto-linking from AI agent with an AI agent type, the linking fails.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1981024

</td><td>

Markdown link \[label\]\(url\) renders an incorrect URL when the URL contains a dollar sign \($\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1981038

</td><td>

There's an extra empty message added after the HTML output when messages arrive too quickly

</td><td>

This was added for scrolling. When the messages come too fast, this 'hidden' message stays in the chat.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1983355

</td><td>

Markdown to HTML parsing issues when there are special characters in the payload

</td><td>

 

</td><td>

1.  Create a topic in the designer with a text node with an response message containing a \` \(backtick\) character.
2.  Test the topic.

Notice the response shows unintended HTML.


 Expected behavior: Parsing is broken and links are highlighted.

 Actual behavior: The HTML output is broken.

</td></tr><tr><td>

Visual Task Boards

 PRB1994303

</td><td>

In a Visual Task Board \(VTB\), the 'Select lane' menu displays lane values from all the boards available irrespective of the board selected to move

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Word Document APIs

 PRB1967960

</td><td>

Custom fonts in Word documents throw an error

</td><td>

 

</td><td>

1.  Identify contract documents with custom fonts embedded into XML.
2.  Upload the contract into the contract request.

 Note that the upload fails and the file isn't visible in the contract request.

</td></tr><tr><td>

Word Document APIs

 PRB1987850

</td><td>

Issue with document sync when paragraph properties do not exist

</td><td>

An error occurs when attempting to sync the document. This issue occurs when the document was generated using ChatGPT or other AI tools, or when content controls are positioned on blank text.

</td><td>

1.  Make changes to the content control fields with 'Track Changes' on.

Observe that the selected paragraph should not have any styling.

2.  Attempt to replace the value.

 Notice that it will throw an error.

</td></tr><tr><td>

Work Order Management

 PRB1917452

</td><td>

Travel time and work time validation doesn't prevent the work order tasks from being updated, and the **Close incomplete** button has unexpected results

</td><td>

Modifying the Actual travel duration to be larger than the time between Actual travel start and Actual work start triggers a business rule to display 'Total travel time must be before actual work start' and abort the change. However the change is not aborted. Moreover, if the change is saved with the button **Close incomplete**, the task status will be updated to 'Closed complete'.

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB1984931

</td><td>

The WDF table throws exception when referencing glide tables with long logical table names that are greater than 30 characters

</td><td>

An error occurs when opening the WDF table and including the reference column in the list view.

</td><td>

1.  Create a glide table with more than 30 characters.
2.  Create a WDF table with a column that references a column in the glide table.
3.  Open the WDF table and include the reference column in the list view.

 Notice than an error shows on the page.

</td></tr><tr><td>

Zero Trust Access

 PRB1976242

</td><td>

There's a security constraints access prevention issue after enabling zero trust access when opening a VTB dashboard

</td><td>

 

</td><td>

1.  Provision an instance with the 'Zero trust access' plugin installed.
2.  Enable the ZTA property \(glide.authenticate. session\_access.enabled\).
3.  Navigate to vtb\_board.list.
4.  Open any dashboard having a condition with a date-time filter.
5.  Select **Show board** under related links.

 Expected behavior: The VTB board should load and the session should remain with the roles the user is entitled for that session.

 Actual behavior: Users observed a security constraints access 403 error for any subsequent action.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 12 Hotfix 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-12-hf-2-PO.md)
-   [Yokohama Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-12.md)
-   [Yokohama Patch 11 Hotfix 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11-hf-2-PO.md)
-   [Yokohama Patch 11 Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11-hf-1-PO.md)
-   [Yokohama Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-11.md)
-   [Yokohama Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-10.md)
-   [Yokohama Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-9.md)
-   [Yokohama Patch 8 Hotfix 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-8-hf-4-PO.md)
-   [Yokohama Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-8.md)
-   [Yokohama Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-7.md)
-   [Yokohama Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-6.md)
-   [Yokohama Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-5.md)
-   [Yokohama Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-4.md)
-   [Yokohama Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-3.md)
-   [Yokohama Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-2.md)
-   [Yokohama Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-patch-1.md)
-   [Yokohama security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-security-notables.md)
-   [All other Yokohama fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/release-notes/available-versions.md)


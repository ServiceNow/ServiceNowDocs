---
title: Zurich Patch 13
description: The Zurich Patch 13 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-13.html
release: zurich
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 126
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 13

The Zurich Patch 13 release contains important problem fixes.

-   **Zurich Patch 13 was released on October 08, 2026.**
    -   Build date: 10-06-2026\_0908
    -   Build tag: glide-zurich-07-01-2025\_\_patch13-09-17-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z013.00.xlsx).

Zurich Patch 13 includes 915 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-zp13.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Zurich Patch 13 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 13, refer to [KB3159341](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3159341).

## Changes in Zurich Patch 13

-   **[Agentic Usage Overview Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/agentic-usage-overview-dashboard.md)**

    Monitor usage from inbound agentic connections to MCP servers from the Agentic Usage Overview Dashboard.

-   **[Monitoring Now Assist usage in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/monitoring-now-assist-usage.md)**
    -   Track Now Assist usage, including Moveworks Assists, across your production and non-production instances.
    -   View Moveworks assists broken down by skill. Moveworks skill names are distinguished by the "MW" prefix.
-   **[Subscription Management release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/subscription-management-rn.md)**

    Starting in Zurich patch 13, Moveworks consumption can now be measured as part of your Assist meter, following the same subscription rules as other assist-based products. For more information about the timeline and required steps for integration, see [Moveworks Assist in Subscription Management: Rollout Timeline, Customer Actions &amp; FAQ \[KB3147691\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147691) on the Now Support Knowledge Base.


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

AI Search UX

 PRB2073716

 [KB3148324](https://hi.service-now.com/kb_view.do?sysparm_article=KB3148324)

</td><td>

For non-admin users, search results and suggestion navigation on portals are redirecting to platform view

</td><td>

After upgrading to Australia Patch 5 or Zurich Patch 12, non‑admin users performing a search on a portal \(for example, /esc\) experience incorrect navigation. Selecting a regular search result or a suggested search result opens the record in the platform view rather than within the portal.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Core UI Responsive Dashboards

 PRB2034505

 [KB3085059](https://hi.service-now.com/kb_view.do?sysparm_article=KB3085059)

</td><td>

A Platform Analytics \(PA\) dashboard overview can't load any dashboards

</td><td>

If all of the following conditions are met, the dashboard doesn't appear on the 'All' tab of PA dashboard 'Overview' page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB2009991

 [KB3090094](https://hi.service-now.com/kb_view.do?sysparm_article=KB3090094)

</td><td>

'Workflow'-type fields are displaying as 'Pending - has not started' for all values

</td><td>

This requires a single-line change that adds a defensive .clone\(\) call to deep-copy the choice list before WorkflowIcons.process\(\) mutates it. This prevents the shared cache from being poisoned by in-place label overwrites.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB2031478

 [KB3074807](https://hi.service-now.com/kb_view.do?sysparm_article=KB3074807)

</td><td>

The 'List edit' pop-up is not working in UI16 view with the Next Experience disabled view

</td><td>

The user is not able to edit values from the List view, and the 'List edit' pop-up is partially or not visible at all. The 'List edit' pop-up should be visible for every row and for every column.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Time Card Management

 PRB2051508

 [KB3139332](https://hi.service-now.com/kb_view.do?sysparm_article=KB3139332)

</td><td>

The **user.manager** field shows as empty when opening the 'Pending Approval' module for time sheets

</td><td>

The filter is empty for the **user.manager** field.

</td><td>

1.  Impersonate a user with submitted time sheets.
2.  Navigate to **Time Sheet** &gt; **Pending Approval**.

 Notice that the filter shows empty for **User.Manager**.

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

Activity Stream Compose Component

 PRB2032875

</td><td>

Highly threaded emails with multiple block quotes render as unreadable in the 'Conversation' tab

</td><td>

 

</td><td>

1.  Navigate to any workspace, such as Service Operations Workspace.
2.  Open any record from the list.
3.  Reply to that email from the inbox.

This reply should appear in the 'Conversation' section.

4.  Reply back to this new email.
5.  Repeat for 7-8 replies.

It reaches a point where users see one letter per row.


</td></tr><tr><td>

Activity Stream

 PRB1991852

</td><td>

Base64 coded attachments can't be loaded in the activity stream in the workspace

</td><td>

This likely has to do with processing large content.

</td><td>

1.  Navigate to any record page.
2.  Create an email with a base64 encoded image.
3.  Set the email to 'sent' status.
4.  Navigate to the record and select **Show more** for the email.

 Expected behavior: The full body of the email is displayed.

 Actual behavior: The email is loading for a long time and eventually crashes the page.

</td></tr><tr><td>

Activity Stream

 PRB2017633

</td><td>

ActivityDBListener fires too many AMB messages on bulk deletes

</td><td>

 

</td><td>

1.  Open an incident in a workspace.
2.  Create two emails.
3.  Open sys\_email\_list.do.
4.  Set both emails' type to 'sent' 5.

Notice that when returning back to the 'Incident' page, there should be two emails now.

5.  Open the Network panel in the DevTool's inspect window.
6.  Reload the page.
7.  Filter by 'amb'.
8.  Select the AMB message.
9.  Select the **Messages** tab.
10. Clear all of the messages.
11. In the sys\_email\_list.do, select one of the emails from step 4 and delete it.

Observe that in the 'Network tab', there should be an AMB message for the deleted email.

12. In /sys\_email\_list.do, delete multiple emails that are 'send-ready'.

Observe that in the 'Network' tab, there should be no messages for those deleted emails.

13. In /sys\_email\_list.do, delete multiple emails that are 'send-ready' and the other email from step 4.

 Observe that in the 'Network' tab, there should only be 1 message for the other email.

</td></tr><tr><td>

Activity Stream

 PRB2032224

</td><td>

Orphaned dependent fields in the initial audit event causes an exception in SysAuditRule

</td><td>

When the support audit is passed to findFirst, which filters out support audits, it finds an empty stream and throws 'IllegalStateException: Unreachable code reached.' The exception is caught, but it causes retrieveEvents to return zero events, leaving the workspace activity stream completely empty.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2060131

</td><td>

When table rotation is set up for sys\_audit\_relation, audit relationship events don't display in a workspace

</td><td>

 

</td><td>

1.  Navigate to **Table Rotations** \(sys\_table\_rotation\).
2.  Add a record for sys\_audit\_relation.
3.  Set the type to 'Extension' and the 'Duration' to 1 hour or less.
4.  Create audit relationship changes.

 Expected behavior: The audit relationship changes are displayed in the workspace activity stream.

 Actual behavior: The audit relationship changes are not displayed.

</td></tr><tr><td>

Activity Stream

 PRB2073311

</td><td>

Build backend graphQL endpoint for List Activity

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2073313

</td><td>

Provide supplemental data for returned records on the new back-end for list activity

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2073315

</td><td>

Review DT APIs for security

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB2060584

 [KB3143279](https://hi.service-now.com/kb_view.do?sysparm_article=KB3143279)

</td><td>

The 'Set logged out agent offline' script action shouldn't touch presence states when 'disable\_inactivity\_check' is set to true

</td><td>

A live human agent is made offline whenever they log out. However, the log out script action should bypass the agents in those presence states that have 'disable\_inactivity\_check' set to true.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Agent Chat

 PRB2053704

</td><td>

Confusing '\_​live\_​agent\_​support\_​offglide\_​' is triggered in non-off Glide LLM conversations

</td><td>

 

</td><td>

1.  Start an LLM conversation.
2.  Request a live agent transfer.
3.  Check the corresponding topic being triggered in the sys\_cs\_conversation record.

 Observe that the topic '\_​live\_​agent\_​support\_​offglide\_​' is triggered even though the conversation is not an off Glide conversation.

</td></tr><tr><td>

Agent Chat

 PRB2057904

</td><td>

When an agent's Async Message Bus \(AMB\) connection breaks, they silently stop receiving work-item events with no indication that anything is wrong

</td><td>

They appear available but never get offered work.

</td><td>

1.  Log in as an agent.
2.  Open Service Operations Workspace \(SOW\).
3.  Make the agent online.
4.  Log in as an admin in another window.
5.  Navigate to the 'sys\_amb\_channel\_presence' table and disconnect AMB.
6.  Navigate to SOW.

 Expected behavior: See a modal that AMB got disconnected. When users select**refresh**, it auto connects.

 Actual behavior: Users aren't seeing the modal that AMB got disconnected, so the agent never knows.

</td></tr><tr><td>

Agent Chat

 PRB2058031

</td><td>

Add a missing flag on 'Requires ACL authorization'

</td><td>

A fix has ensured that the 'Requires ACL authorization' flag on 'Conversation Server' graphQL schema is set to true. However, due to a discrepancy in syncing branches, only the ACL changes added are live and not the graphQL schema changes.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2063949

</td><td>

Some messages are hidden on the agent's side when hideControl is true and contains searchText

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2068933

</td><td>

A workspace error is observed when handling incoming messaging interactions in Agent Workspace

</td><td>

In both scenarios, the error modal occurs.

</td><td>

Scenario 1:

 1.  Open a messaging interaction in the CSM workspace.
2.  As a agent, navigate to any other tab than the ongoing interaction.
3.  Send one or more messages from the requester.
4.  Ensure that the ongoing messaging count is visible.
5.  Switch to the current interaction.

 Observe the error modal.

 Scenario 2:

 1.  Open a messaging interaction in CSM workspace.
2.  Send one or more messages from the agent/requester.
3.  Refresh the page.

 Observe the error modal.

</td></tr><tr><td>

Agent Chat

 PRB2077124

</td><td>

A tab subheading displays 'Call is in wrap-up' while a call is still active in an agent-initiated wrap-up scenario

</td><td>

When an agent selects **Open Wrap-Up** MID-call, the tab subheading immediately changes to 'Call is in wrap-up' even though the voice call is still ongoing. This is misleading. The label implies the interaction is in wrap-up state, but the call has not yet ended. UX has confirmed the label should be changed to 'Wrap-up initiated' — a generic label that works accurately for both MID-call and post-call scenarios.

</td><td>

1.  Configure an NVC/CCaaS integration with supportExternalWrapUp = true on the Wrap Up macroponent.
2.  Start a voice call as an agent.
3.  While the call is still active, select the **Open Wrap-Up** button.

 Observe the tab subheading. It immediately displays 'Call is in wrap-up' even though the call is still ongoing.

</td></tr><tr><td>

Agile Development

 PRB2057888

</td><td>

Add script include to gate PWS-CWM functionalities

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2059351

</td><td>

Record scope should override the user session scope

</td><td>

For AI Agents, when any record of a user instance is used, the record scope should override the user session scope of the MSP as per the domain separation policy. However, that's not happening. For example, when an AI Agent with a retriever tool is triggered by any record in a user instance \(like C1\), it fetches KBs/results from all the user instances under that MSP.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2059390

</td><td>

Role masking isn't unset when running a workflow

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2085529

</td><td>

AI Agent execution tool 'AIA RAG Retriever' returns faulty URLs for search result items in VA and ES

</td><td>

When the RAG/semantic-search result's URL omits the leading forward slash, the resulting link is corrupted and unusable.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2059453

</td><td>

True up version for the AIXF Store app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2061584

</td><td>

True-up the AI UX Builder Store app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2062421

</td><td>

The ACL 'Type' drop-down list does not include aiux\_page, aiux\_widget, or aiux\_dashboard options

</td><td>

None of these types are available when they should be included as selectable options.

</td><td>

1.  Navigate to sys\_security\_acl.list.
2.  Select **New** to create an ACL record.
3.  Open the 'Type' drop-down list.
4.  Search for aiux\_widget, aiux\_page.

 Expected behavior: The 'Type' drop-down list should include aiux\_page, aiux\_widget, and aiux\_dashboard as selectable options.

 Actual behavior: The AIUX types are not present in the 'Type' drop-down list.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2072025

</td><td>

sys\_ux\_theme\_asset records associated 'sys\_attachment' records have an incorrect state

</td><td>

It should be 'available' and not 'available\_conditionally'.

</td><td>

 

</td></tr><tr><td>

AI Gateway - Security

 PRB2041348

</td><td>

The auto-generated fake sys\_ids in AIG should be fixed

</td><td>

Fix the files sys\_id and corresponding ITs and UTs.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1859571

</td><td>

A search retrieval agent returns an incorrect catalog item URL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2033435

</td><td>

TSTranslationReference loads all sys\_translated rows for a field instead of filtering to the indexed record's value

</td><td>

When indexing a record that has a **Reference** field pointing to a table whose **Display** field is a translated\_field type, TSTranslationReference calls Translation​Util.​get​Translated​Field​Values\(\)​,​ which queries sys\_translated with only name=&amp;lt;table&amp;gt; and element=&amp;lt;field&amp;gt; — no VALUE filter. This loads all translations for every value of that field across all records.

</td><td>

1.  Have a large sys\_translated table with 50k+ rows for a single table/field combination.
2.  Enable a language plugin.
3.  Index a record that has a **Reference** field pointing to a table whose **Display** field is a translated\_field type. For example, a table referencing a question where the question\_text is translated\_field.

 Observe that index events take 5s to 8s each, and the message at occurs, 'QueryWarning: 'Large Table' on sys\_translated with query name=&lt;table&gt;^element=&lt;field&gt; \(no value filter\).'.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2052168

</td><td>

No\_answer Genius Result is streamed intermittently

</td><td>

A Genius Result rarely shows, but it should not show at all.

</td><td>

1.  Navigate to /sp.
2.  Search for something that gives a no\_answer result, like 'baseball world series'.

 Observe that a Genius Result rarely shows. It should not show at all.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2070763

</td><td>

Impersonation for RAGRetrivalAPI isn't required

</td><td>

This feature isn't required anymore. Going forward, it will be implemented in a different way. It is currently behind ais\_admin role but requires other impersonation checks which are missing currently.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2074141

</td><td>

Changing a retention policy on an indexed source doesn't enforce guard rail recalculation

</td><td>

 

</td><td>

1.  See that the retention policy for an 'Incident' indexed source is two years.
2.  Verify that Semantic Index configuration in enabled.
3.  Verify that there's an entry in the ais\_​guard\_​rail\_​limit\_​data\_​source table.
4.  Change the retention policy on the indexed source to three years.

 The entry isn't recalculated in ais\_​guard\_​rail\_​limit\_​data\_​source.​

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2084573

</td><td>

In the 'Live Search' API, if a userId passed in x-run-as doesn't exist, then it throws an error

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2084574

</td><td>

IncludeSources and ExcludeSources support for the 'Live Search' API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2084575

</td><td>

REST API policy configurations in Moveworks API V2

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2086827

</td><td>

Handle duplicates with version, embedding model gracefully in ServiceNow Security Center \(SSC\)

</td><td>

This is metadata, so business rules aren't guaranteed to run \(for example, when coming in through an update set\), which is why there should be graceful handling of duplicates.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2095212

</td><td>

SSC details override Next Wave request payload when both are present

</td><td>

When a Next Wave request is made with explicit parameters/details in the payload AND SSC \(Service Search Configuration\) details exist for the same context, the SSC details are taking precedence and overriding the values passed in the Next Wave request payload.

</td><td>

 

</td></tr><tr><td>

AI Search for Service Portal

 PRB1998368

</td><td>

AI Search in Enhanced Chat's full page experience throws a console error

</td><td>

The error, 'Uncaught TypeError: \(\(n.event.special\[g.origType\] \|\| \{\}\).handle \|\| g.handler\).apply is not a function : js\_includes\_sp\_libs.jsx at HTMLDivElement.dispatch' occurs in the console.

</td><td>

 

</td></tr><tr><td>

AI Search for Service Portal

 PRB2062818

</td><td>

The sparkle Otto icon in a portal search input has an incorrect color when Enhanced Chat is turned on

</td><td>

The sparkle Otto icon before the input placeholder is not visible because it is same color as the background.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1893398

</td><td>

Attempting to recreate a scenario where entries in the search term is empty in the sys\_search\_event table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB2064865

 [KB3151377](https://hi.service-now.com/kb_view.do?sysparm_article=KB3151377)

</td><td>

Now Assist search results overlap when keyboard tabbing is used

</td><td>

During keyboard navigation through the interactive elements in the AI component, overflowed content overlaps with other elements, making the response/answer difficult to read. This was identified as an accessibility finding during a recent audit by the Accessibility Center.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search UX

 PRB1939328

</td><td>

A 'No Answer Found' Genius Result response shouldn't cause 'Has Results' to be true

</td><td>

 

</td><td>

1.  Open Virtual Agent.
2.  Search for something that return a 'No Answer Found' \(NAF\) response.
3.  Open the sys\_cs\_fdih\_invocation table and find the recent entry that corresponds to the search.
4.  Copy the 'searchAnalyticsPayload' object from the outputs json.
5.  Send that payload as a SEARCH\_EVENT to the Signals API, either via Scriptable or the REST API.
6.  Open the sys\_search\_event table and inspect the record corresponding to the payload just submitted to Signals. In particular, look at the **Has Results** field.
7.  Open the sys\_search\_signal\_event table and find the corresponding record.
8.  Inspect the **Genius Results** field.

 Expected behavior: The**Genius Results** field on sys\_search\_signal\_event should be empty. **Has Results** should be false.

 Actual behavior: The**Genius Results** field indicates a synthesized response was displayed, and **Has Results** is true.

</td></tr><tr><td>

AI Search UX

 PRB1988057

 [KB3220629](https://hi.service-now.com/kb_view.do?sysparm_article=KB3220629)

</td><td>

Hyperlinks in synthesized responses don't open in a new tab

</td><td>

When the user attempts to open a hyperlink from the synthesized result, it fails to open.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search UX

 PRB2057349

</td><td>

Rename Now Assist to Otto for typeahead suggestions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2083562

</td><td>

Support right-click behavior for Service Portal search results

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1973007

</td><td>

The Platform Analytics 'pivot table' unit type doesn't persist

</td><td>

When creating a pivot table using two tables as the data sources, the 2nd and 3rd columns swap their values.

</td><td>

1.  Create a pivot table visualization within a dashboard.
2.  Add in two tables as data sources.
3.  Create four columns on the pivot table, with the first two column being a count of each respective table and the last two columns a sum of all the values with other columns.
4.  Save the visualization.
5.  Exit editing mode.
6.  Refresh the dashboard.

 When the order of the columns is the count of table 1, count of table 2, sum of table 1's column, sum of table 2's column, and when users refresh the dashboard, the 2nd and 3rd columns values swap, with the values from column 3 appearing in column 2 and vice versa.

</td></tr><tr><td>

Analytics Data API

 PRB1974104

</td><td>

The 'Sort by' value does not work in time series visualizations

</td><td>

The order changes, but in a pattern that is neither ascending or descending.

</td><td>

1.  Add a timeseries column chart.
2.  Add an incident table with the following:
    1.  Trend by: Year by Activity due
    2.  Group by: Assignment group
    3.  Sort data by value: ASC
3.  Hover on a chart.

Observe the values in the legend.

4.  Change sorting to 'DESC'.
5.  Hover on a chart.

Observe the values in the legend.

6.  Repeat the steps with 'Group by: State'.
7.  Change the group by aggregation to 'Hour of day by Opened'.
8.  Change DESC to ASC in all cases.

 Observe that the sorting by value is applied incorrectly – it's sorted, but in a strange order that is not ascending or descending. By changing the order, the values position changes, but the order is still not ASC or DESC.

</td></tr><tr><td>

Analytics Data API

 PRB2002190

</td><td>

The error log should be suppressed in a prefetch job

</td><td>

The user is getting the error log, 'com.​glide.​rest.​domain.​Service​Exception:​ Invalid configuration in their syslog daily at an interval of 15 minutes. This is a cause of concern as the error logs are frequent and does not give complete information to the user to stop them.

</td><td>

1.  Open any Zurich instance.
2.  Open the syslog table.

 Observe that there is a message containing 'com.​glide.​rest.​domain.​Service​Exception:​ Invalid configuration.'.

</td></tr><tr><td>

Analytics Data API

 PRB2008673

</td><td>

A single score reported on a **Time** field with an aggregation as a sum is calculated correctly in the Core/Responsive UI experience but incorrectly in the Platform Analytics Next Experience UI

</td><td>

When a field is created as a dictionary type as 'Integer' and has an attribute 'format=glide\_duration', then the aggregation of this field on a native report or a responsive/core dashboard is displaying the duration sum aggregate properly. But when migrated to the platform analytics dashboard, the same field aggregation sum does not render the result correctly.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2019716

</td><td>

Multiple elements from a single filter can't be applied to an 'COUNT DISTINCT' or 'AVERAGE' indicator with 'Show filter as separate series'

</td><td>

When multiple elements are selected and applied from a single filter to a visualization based on an automated indicator, the filter is not applied. The 'Network' tab in the developer console shows, 'Indicator does not support multi-element aggregation'. This should not occur for automated indicators. This issue only occurs if the 'facts' table is a database view.

</td><td>

1.  Create a PAR dashboard.
2.  Add a line visualization with the base instance indicator, 'Number of over-due incidents' as the data source.
3.  Add a filter with 'Indicators' as the filter source type, and 'Assignment Group' as the indicator breakdown.
4.  Under 'Data to filter,' add 'Indicators with Assignment Group breakdown'.
5.  Select two elements from the filter and apply it.

 Observe that the filter is not applied, in the 'Network' tab in the developer console, the following occurs:​\[\{'order':​0,​'response':​\{'filters':​\{'not​Applied​Filters':​\[\{'order':​0,​'reason':​'Indicator does not support multi-element aggregation'\}\]\}.

</td></tr><tr><td>

Analytics Export API

 PRB1971222

</td><td>

'Omit if no records' isn't honored for score visualizations

</td><td>

If the record count is zero for the visualization, the email with the exported data visualization PDF should not be generated when the 'Omit if no records' checkbox is checked.

</td><td>

1.  Create a data visualization of the type 'score', 'gauge', or 'dial'.
2.  Add a data source and conditions such that the record count is zero. For example, add a condition like 'active is true and active is false' which will make the record count zero.
3.  Save the data visualization.
4.  Schedule the export of data visualization to a PDF.
5.  Enable the **Omit if no records** checkbox.
6.  Select **Send now** from the 'Scheduled export' page.

 Expected behavior: The email shouldn't be generated when the record count is zero for the visualization.

 Actual behavior: The email gets generated even though the**Omit if no records** checkbox was selected.

</td></tr><tr><td>

Analytics Export API

 PRB2057980

</td><td>

The visualization creator is not able to select existing highlight value configurations

</td><td>

The visualization creator couldn't select a highlighted value configuration because the visaualization creator role doesn't have read access for the sys\_​ux\_​highlighted\_​value\_​config table.

</td><td>

1.  Create a highlight value configuration for an incident table as an admin user.
2.  Create a list visualization \(viz\_creator role\).
3.  Select the table as 'incident'.
4.  Enable the fetch highlighted value.
5.  Search for the highlight configuration created above.

 Observe that no result is returned in highlight value drop-down list, even though the visualization creator should be able to read and use existing highlight value configurations.

</td></tr><tr><td>

API Access Policies

 PRB2065453

</td><td>

The RESTAPIAccessScopeRepo map overwrite loses required authentication scopes when two sys\_api\_access\_scope records share the same API signature

</td><td>

A 403 'User Not Authorized' error occurs.

</td><td>

1.  Install and activate both ServiceNow Otto for Document Voice and Dynamic Guidance applications.
2.  Confirm both sys\_api\_access\_scope records are active for the SNGenerativeAI API path sn\_generative\_ai/extensions, with all apply-all flags \(apply\_all\_methods, apply\_all\_resources, apply\_all\_versions\) set to 'true'.
3.  Call GET /​api/​sn\_​generative\_​ai/​extensions/​live-​llm-​configuration?​solution​Capability=​smartdocs\_​voice\_​qna with the Document Voice token.

 Observe that if the Dynamic Guidance Authentication Scope record loads last into the RESTAPIAccessScopeRepo's map, the call returns the error, '403 User Not Authorized - Missing required API access scope: Dynamic Guidance Auth Scope'.

</td></tr><tr><td>

App Engine Pipelines

 PRB2068337

</td><td>

There's a Zboot error: 'fix\_cobalt\_raven\_store\_ app\_query\_acl\_customization\_\*.xml'

</td><td>

The failing fix files are placed directly under /update/ \(unconditional\), while every correctly working fix is placed under /if/com.glide. security.query\_acl/update/ \(conditional on the com.glide. security.query\_acl plugin\).

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB2033816

</td><td>

The Backfill Module Key ID in encrypted attachment ZIPs are polluting the syslog

</td><td>

It creates content that looks like a ZIP file \(by name/MIME\) but isn't a GZIP. It forces the platform to read it as GZIP, which triggers the identical ZipException and syslog error that the Backfill job produces at scale.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1975999

</td><td>

The user can not update the customized app's base version when no new customized versions are available

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1979149

</td><td>

Now Assist for Configuration Management Database \(CMDB\) 2.5.2 certification/installation fails with conflicting versions

</td><td>

There's an error message: 'Unable to successfully install batch package Suite install for Now Assist for Configuration Management Database \(CMDB\) 27.11.0:Batch install failed due to conflicting version or'.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB2022268

 [KB3156065](https://hi.service-now.com/kb_view.do?sysparm_article=KB3156065)

</td><td>

The application manager sys\_app\_version displays duplicate records for the same application and version, which is causing the app to be 'Installation blocked'

</td><td>

As part of the AI testing, it's been observed that the app installations are blocked. The sys\_app\_version displays duplicate records for the same application, which is causing the app installations to be blocked, despite the app versions being available as well as the license checks having successfully completed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB2056916

</td><td>

Skip a license-blocked status for all dependencies in DependencyProcessor

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB2057729

 [KB3140027](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140027)

</td><td>

Users can't publish custom-scoped applications after upgrading to Zurich or Australia

</td><td>

After upgrading to Zurich or Australia, there's an issue that prevents new application versions from being published for custom scoped apps in ServiceNow Studio. Selecting the **Publish** button for any custom application results in a publish failure with one of the following errors: 'Vendor information was not found, upload function is disabled for this instance' or 'Did not receive publishing information successfully. Cannot read properties of undefined \(reading 'toString'\)'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB2074238

</td><td>

Now Assist to Otto rename for Application Manager

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Appointment Booking

 PRB2074894

</td><td>

An appointment isn't working correctly after an upgrade

</td><td>

When the data format is set to dd-MM-yyyy, the appointment slots aren't retrieved correctly.

</td><td>

1.  Navigate to an instance.
2.  Set the date format to dd-MM-yyyy.
3.  Open any Record Producer in the Field Service Management \(FSM\) application.

There should be a calendar variable.

4.  Select the **calendar** icon to select an appointment.

 Observe that no available appointment time slots are displayed.

</td></tr><tr><td>

Authentication Factors

 PRB2037251

</td><td>

Update interactions post-identification and authentication

</td><td>

The 'Interactions' table has only 'Guest' resolved. It should have the user reference resolved post-identification and authentication.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB2037962

</td><td>

The MCP Server registration with the Client Credentials grant fails when created via AI Agent Studio

</td><td>

When registering an MCP Server in AI Agent Studio using the Client Credentials grant type \(manual registration\), the form doesn't get submitted. The same MCP server registration works correctly when the Connection &amp; Credential alias is created manually outside AI Studio on the same instance. It also works correctly when the flow is exercised via Postman/curl directly against the MCP server's '/token' endpoint. The Authorization Code grant type continues to work end-to-end through AI Studio.

</td><td>

1.  Log in to an instance.
2.  Navigate to **AI Agent Studio** &gt; **Settings**.
3.  Select **Manage MCP Servers**.
4.  Select **New** to add a new MCP server.
5.  Enter the MCP URL.
6.  Select **Manual Registration** for Client Registration Type.
7.  Select **Client Credentials** for Grant Type.
8.  Select **Client Secret Post** for Token Authentication Method.
9.  For Client ID, enter 'svc\_oodp\_dataaccess'.
10. For Client Secret, enter a valid secret.
11. For Auth Scopes, enter 'openid'.
12. Enter the token URL.
13. Select **Add**.

 Expected behavior: The MCP Server registers successfully, like it does for Authorization Code grants and for manually created Connection &amp; Credential aliases.

 Actual behavior: The form doesn't get submitted. The**Add** button is blocked until the authentication URL is provided, which ideally would not be required for the Client Credentials grant type.

</td></tr><tr><td>

Authentication

 PRB2084119

</td><td>

Ability to issue a correlation token that can be exchanged for access token

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB2084125

</td><td>

Workload identity federation support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2053799

</td><td>

Text and cosmetic changes for ServiceNow Otto

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2054701

 [KB3147951](https://hi.service-now.com/kb_view.do?sysparm_article=KB3147951)

</td><td>

A 'Host CPU Load Critical' alert is caused by ATF Scheduler jobs with a large amount of sys\_atf\_modified\_ record\_m2m records generated

</td><td>

ATF Tests that cause a large number of modified records \(stored in the sys\_atf\_modified\_record and sys\_atf\_modified\_record\_m2m tables\) cause cause high application server CPU usage as well as high memory usage. When users check to see if a test can run now, they attempt to first acquire exclusive access to all necessary records. If the list of modified records is very large, then users can spend a lot of time trying to determine if the test can run now, and this can cause high CPU usage on the application server and high memory usage in the application node.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Base Asset Management

 PRB1950847

</td><td>

Improve the performance of bulk updates of transfer order lines

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Base Asset Management

 PRB2055589

</td><td>

Make a serial number mandatory in Identification and Reconciliation Engine \(IRE\)

</td><td>

The follow list of model categories don't have IRE rules - thus there is no check on unique identifiers: Medical General, Facility General, HVAC, Fuel Tank, Structure, Fuel Tank, Transportation General, Aircraft, Ship, Train, Vehicle, and Retail General. If there is no IRE rule, it should fall back to either a serial number or asset tag as unique identifier for assets. Currently, there's no check on unique identifier.

</td><td>

 

</td></tr><tr><td>

Cache

 PRB1953827

</td><td>

There's errors in the system/error log since Zurich

</td><td>

The errors and messages in the syslog are coming from the source 'com.​glide.​ui.​Servlet​Error​Listener'.​

</td><td>

 

</td></tr><tr><td>

Canonicalization Data Services \(CDS\)

 PRB2053470

</td><td>

Data uploaded to cds\_server\_staging table is blocked within instances

</td><td>

This issue occurs in instances where the property 'glide.cmdb.canonical.URL' is set to https:​/​/​&lt;instance\_​name&gt;​.​service-​now.​com/​ and ends with '/'. Unfortunately, that is the base instance value, and it affects the upload portion of CDS.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2017688

</td><td>

RCAs from Knowledge script includes to HR are requesting entire scope access

</td><td>

The 'Advanced Knowledge Editor' page in HR Agent Workspace is being used, and contains Open Prompt, which is interactable and helps create an articles using Gen AI. For the Open Prompt to work without any issues, new RCAs are required.

</td><td>

1.  Activate the Knowledge Recommendation plugin and Article Optimization plugin.
2.  From the Knowledge Management properties, enable the ECE.
3.  Create an article from the related list of any HR case.
4.  Add a link in the article.

 Observe that there are RCAs from the Knowledge Center to HR Core.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2039604

</td><td>

The HR L1 Specialist is missing Restricted Caller Access \(RCA\) records from the installation

</td><td>

After installing the HR L1 Specialist on a zbooted Australia instance, RCA records were created from ZTSD and Now Assist AI Agents scopes to the HR Core scope, which prevent the specialist from completing its tasks.

</td><td>

1.  Create an instance or zboot an existing one.
2.  Upgrade the instance to Australia.
3.  Install the HR L1 Specialist along with all required dependencies for the HRSD product.
4.  Configure the HR L1 Specialist.
5.  Assign the specialist to a 'Ready' HR Case.

 Observe the Restricted Caller Access table to attempting to find the generated RCA records.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2070954

</td><td>

RCAs are required for predict and transfer use cases

</td><td>

There should be RCAs for the new tool call when the sys\_id isn't mentioned in the objective when invoking the 'Predict HR Service and Transfer' case workflow.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2071462

</td><td>

System logs have the error 'Scoped cache operation against catalog nowassist\_admin was skipped because of an invalid sysId: no thrown error'

</td><td>

There's the sys\_ws\_operation 'Get Complete State', owned by package Human Resources: Core \(sn\_hr\_core\), operation URI /​api/​sn\_​hr\_​core/​ hr\_​rest\_​api/ ​get\_​complete\_​state.​ configGr.skill\_config returns the raw GlideElement \(backed internally by com.​glide.​script. ​Field​Glide​Descriptor\)​,​ and is never converted with .toString\(\). That object is then handed straight into sn\_​nowassist\_​admin.​ Now​Assist​Skill​Config.​ get​Skill​Configuration\(\)​ — a call across a scope boundary \(sn\_hr\_core → sn\_nowassist\_admin\).

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2072634

</td><td>

HR cases no longer **Apply** fields set from a template when created from the 'Create New Case'/'Case Creation' page

</td><td>

Starting in the Australia release, when users have an HR template that sets the state to 'Ready' or any other state, the case still gets created with the state of 'Draft'.

</td><td>

1.  Navigate to the 'Create New Case' module.
2.  Select any user.
3.  Select **HR Service** where the template is set to the state to 'Ready'.
4.  Select the **Create Case** button.

 Expected behavior: The HR case is created in 'Ready' state.

 Actual behavior: The HR case is created in 'Draft' state.

</td></tr><tr><td>

Case Management

 PRB2057866

</td><td>

Target tables are missing required tracking fields for multi-case creation

</td><td>

For multi-case creation, the target records do not have the required tracking fields to capture Template Item and Template Execution. As a result, the created Case and Case Task records cannot be fully tracked with associated Template item and execution. To support multi-case creation, the fields **Template item** and **Template Execution** need to be added to the sn\_customerservice\_case and sn\_customerservice\_task tables.

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB2075237

</td><td>

Create an implementation to setWorkflow false for a table in the Case Management Core scope

</td><td>

Currently, the multi-case creation takes too much time. To solve the issue, setWorkflow should be set as false. setWorkflow can't be set as false to case management tables from the task plan template scope. Thus, an implementation should be added in the case management scope, which sets setWorkflow false for case and case task tables.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1893775

</td><td>

The sys\_db\_object query range ACL impacts IPC related records, CIs, and impacted business applications

</td><td>

 

</td><td>

1.  Log in as an itil user.
2.  Open any change request.
3.  Navigate to the 'Affected CIs' related list.
4.  Select **Add**.
5.  In the **Add Affected CIs** pop-up, locate the **Configuration Class** field.
6.  Select the lookup/search icon next to the field.

 Observe that no configuration class records are returned even if there's an error saying: 'Part of the query on sys\_db\_object has been ignored because of insufficient access for 'query\_range' operation on sys\_db\_object.super\_class'.

</td></tr><tr><td>

Client Scripts

 PRB1966873

</td><td>

Observations from the Highlighted Value Background

</td><td>

The two scenarios occur after installing the 'com.sn\_customerservice' plugin and configuring the UX Highlighted Value Configuration for the CSM workspace. In this case, the 'Enable Background Color' checkbox is checked, which is responsible for displaying the background color when highlighted values are present on supported fields. The following fields are added as read-only for the Case/Incident form: HTML, Translated HTML, and HTML Script. Highlighted values are also added to the Highlighted values to HTML, Translated HTML and **HTML Script** fields. In scenario 1, the highlighted value badge changes based on the values present on the drop-down list, and the corresponding color doesn't appear automatically. In scenario 2, the gray background color is not well-respected for the HTML type of fields when the highlighted value color is also enabled.

</td><td>

Scenario 1:

 1.  Log in to an instance.
2.  Navigate to the **CSM workspace**.
3.  Navigate to **List** &gt; **Cases**.
4.  Create a new case.

Observe that the **Priority** field starts seeing already pre-configured highlighted value badges. For example, the green colored background pis associated with the the priority value '4' - Low'.

5.  Change the Priority from '4 - Low' to '1 - Critical'.

Observe that the highlighted value badge changes accordingly without needing to save the form, and whether the background color changes or not.


 Expected behavior: The highlighted value background color should change per the highlighted value badge automatically. For example, the critical priority will highlight the background with critical color.

 Actual behavior: Only the badge changes with priority change. The background color is removed altogether and is not updated based on the badge change.

 Scenario 2:

 1.  Log in to an instance.
2.  Navigate to **CSM workspace**.
3.  Navigate to **List** &gt; **Cases**.
4.  Create a new case.

Observe that the **HTML**, **Translated HTML** and **HTML Script** fields should display highlighted value badge if they are supported, and the background colors of the fields.


 Expected behavior: The background for all the above fields should be gray as they have been set to read-only.

 Actual behavior: The**HTML** and **Translated HTML** fields appear with the grey background, however when the user interacts or double click on the field, background always changes from grey to that of corresponding highlighted value background. The **HTML Script** field constantly displays the highlighted value background in the read-only state.

</td></tr><tr><td>

Client Scripts

 PRB2078551

</td><td>

The base instance **Delete** UI action should be supported

</td><td>

The GlideModal logic for the **Delete** UI action needs to be converted into a widget and use g\_modal.showWidget instead.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB2082276

</td><td>

**Analyze Access** UI Action needs migration to work in UI26

</td><td>

When the user selects **Analyze Access**, it redirects to '/​sn\_​access\_​analysis\_​request.​do.​.​.​' because the Ajax request is broken. It should redirect to '/now/access-manager/...'.

</td><td>

1.  Navigate to '/aiux/ui/incident\_list.do'.
2.  Select an incident.
3.  Select and hold \(or right-click\) on the form header.
4.  Select **Analyze Access**.

 Expected behavior: It redirects to '/now/access-manager/...'.

 Actual behavior: It redirects to '/​sn\_​access\_​analysis\_​request.​do.​.​.​' because the Ajax request is broken.

</td></tr><tr><td>

Client Scripts

 PRB2083604

</td><td>

For g\_modal.showFrame, a mechanism is needed to prevent iframe modal autoclose and a way to programmatically close

</td><td>

The EMPTY\_BODY auto-close mode closes the iframe modal on any intermediate navigation with non-empty content, not just when reaching the final empty page \(blank.do\). This breaks multi-step workflows where users navigate through preview or intermediate pages.

</td><td>

1.  Open an iframe modal with autoCloseOn: FrameModalCloseOn.EMPTY\_BODY.
2.  Navigate the iframe to a page with content \(for example, the preview page\).

 Observe that the modal closes immediately as 'Cancelled'. The modal should remain open and wait for further navigation. Also, selecting **Create Excel Template** within the iframe modal does nothing.

</td></tr><tr><td>

Client Scripts

 PRB2084052

</td><td>

The list v2 scripting environment doesn't have access to form globals and angular globals \(NowAPI\)

</td><td>

The existing client script APIs \(for example, g\_modal and g\_ui\_scripts\) were only included in js\_include\_ui16\_form. They need to be extracted into a dedicated js\_include and included within the list page.

</td><td>

Access NowAPI on the list action page.

 Observe that NowAPI is undefined.

</td></tr><tr><td>

Client Scripts

 PRB2084579

</td><td>

Backend changes to the graphql schema to fetch additional data

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB2084581

</td><td>

Client side changes to handle runtime behavior

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB2084584

</td><td>

Port g\_list.refreshWithOrderBy

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB2084585

</td><td>

Port g\_list.refreshWithOrderBy

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Cloud Provisioning and Governance

 PRB1932710

</td><td>

'Operational status' and 'Install status' aren't in sync

</td><td>

In the CPG modules, the inactivation of the business rule 'Sync Ops Status for CMDB CI' has caused the install\_status to remain unsynchronized when operational\_status is updated.

</td><td>

 

</td></tr><tr><td>

CMDB CI Class Manager

 PRB2072350

</td><td>

Create additional fields and view for Dynamice IRE comparison enhancements

</td><td>

Currently the list and form view for the cmdb\_​ire\_​output\_​comparison\_​item table is too noisy and hides the important details. Additional columns should surface the important information in a meaningful manner that can be digested by the user.

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2077883

</td><td>

DynamicIRE cache build time is incorrectly reported in stats

</td><td>

The total time is tracked as build time, even when a cache miss occurs and the cache is flushed and rebuilt.

</td><td>

1.  Make sure the cache is warm.
2.  Request the model from cmdb\_ci\_hardware.
3.  Request something from the cache that doesn't exist, like the model for the cmdb\_ci class.

Observe that a cache miss occurs.

4.  Wait a few minutes, then flush the cache.
5.  Request something else from the cache.

Observe that the cache is rebuilt after being flushed.


 Expected behavior: The cache build time is accurately reported.

 Actual behavior: The total time between steps three and five is tracked as build time.

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2080716

</td><td>

A fix script is needed to turn on dynamic IRE for no-customizations users

</td><td>

Dynamic IRE should be enabled as long as there are no customizations to cmdb\_identifier, cmdb\_identifier\_entry, or ie\_active\_config.

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2080719

</td><td>

Class Manager's UI should be updated for a default-on dynamic IRE state

</td><td>

The existing UI flows should be preserved, but there's a new default-on state. Buttons, labels, and text need to align for the default-on state. When there are results and dynamic IRE is on, difference sampling shouldn't show the dashboard or have another action to load the dashboard.

</td><td>

 

</td></tr><tr><td>

CMDB Workspace

 PRB2085730

</td><td>

When Dynamic Identification and Reconciliation Engine \(IRE\) is turned on, there should be a banner added to the 'Products Highlight' section on the CMDB Workspace home page

</td><td>

 

</td><td>

1.  Turn on Dynamic IRE.
2.  Navigate to the CMDB workspace home page.

 There should be a banner in the 'Product Highlights' section with a **View details** button that links to the Dynamic IRE home page.

</td></tr><tr><td>

Column Level Encryption

 PRB2006384

</td><td>

Attachments from the sn\_si\_incident table are created with a different hash

</td><td>

There appears to be some sort of unique hashing algorithm applied only to the sn\_si\_incident table. Due to this hashing algorithm, attachments are being duplicated in the remote process sync feature.

</td><td>

1.  Attach an attachment to any table other than \[sn\_si\_incident\].
2.  Attach an attachment to the \[sn\_si\_incident\].

 Notice that when comparing the two hashes, two unique hashes are generated for the same file.

</td></tr><tr><td>

Communities

 PRB2003810

</td><td>

Views in Event Content are displaying as '2,147,483,648'

</td><td>

When the event is created through the platform, the events view count is showing high number in the community portal.

</td><td>

1.  Attempt to create an event from the platform \(sn\_communities\_event table\).
2.  Open the same event from the communities portal.
3.  Go back and open the same event again.

 Notice that the views are showing as 2,147,483,648.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1949356

 [KB2616435](https://hi.service-now.com/kb_view.do?sysparm_article=KB2616435)

</td><td>

The exact count match check results in an incorrect duplicate task creation

</td><td>

After upgrading to Zurich, de-duplication \(dedupe\) tasks are created incorrectly under certain scenarios. As a result, a large number of records are created in the duplicate\_audit\_result table, causing significant database growth. Instead of updating existing entries, new records are inserted during each subsequent run. In one scenario, the de-duplication tasks are created when they were previously working. In another scenario, users with many hosts that contain cmdb\_serial\_number records with the same serial\_number and serial\_number\_type notice that the number of duplicate\_audit\_result can grow to be tens of millions daily.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2040049

</td><td>

Life​Cycle​Util.​\_​validate​Combination aborts non-English lifecycle stage/status save from the Service Operations Workspace \(SOW\) standard record page

</td><td>

After upgrading to Zurich, saving a Life Cycle Stage + Stage Status combination from the SOW standard record page fails in non-English sessions \(for example, French, German\), even for a valid combination. The same save succeeds in an English session, and from the UI16 form and the CMDB Workspace CI record page. For example, on a cmdb\_ci\_server, when users set a valid stage/status pair in a French session via the SOW standard record page, the save is silently aborted by the 'Validate lifecycle combination' business rule. An undefined guard misses empty GlideElement.

</td><td>

1.  On a Zurich instance, navigate to **Service Operations Workspace** &gt; **List** &gt; **CMDB** &gt; **Server** &gt; **Open a server record**.
2.  Change session language to French \(or any language already installed\).
3.  Try to set **Life Cycle Stage** and **Life Cycle Stage Status** fields.
4.  Save.

 Observe the business rule error despite choosing valid fields in non-English language.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2086797

</td><td>

Auto-resolve de-duplication tasks using AI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2086798

</td><td>

Task creation, batch processing framework, staleness agent ledger-based task orchestration, and lifecycle automation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2086799

</td><td>

Retirement definition and staleness configurations

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Customer Service Core

 PRB2037285

</td><td>

There's slowness on every page/action for the account executive persona in a perf instance

</td><td>

When trying to perform any action in a perf environment with the account executive persona, the user observes slowness from one to two minutes.

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB2062954

</td><td>

Creating knowledge from a case doesn't populate the **kb\_issue** field

</td><td>

The kb\_issue field is mapped in the Advanced Field Mapping of the CSM Table Map 'Case KCS Article'. It is expected to populate the first comment from the case.

</td><td>

1.  Set the system property sn\_​customerservice. ​enable\_​knowledge\_​kcs to 'true'.
2.  Open a case that contains one or more comments.
3.  Select **Create Knowledge**.

 Expected behavior: The **kb\_issue** field of the newly created Knowledge article is populated with the first comment from the case.Actual behavior: The **kb\_issue** field of the newly created Knowledge article is left blank.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2051225

 [KB3141251](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141251)

</td><td>

GlideAggregate and Platform Analytics pivot fails with 'must appear in the GROUP BY clause' when grouping or sorting by a translatable field in a non-English language

</td><td>

The pivot shows 'No data available.'/'Aucune donnee disponible.' instead of the data. The node log shows com.glide.db. GlideSQLException with the PostgreSQL error, 'ERROR: column 'sc\_cat\_item3.name' must appear in the GROUP BY clause or be used in an aggregate function.'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1999432

</td><td>

The message 'Swarm64CapabilityCheck capability is not supported on Glide' shouldn't be logged and should be removed/stopped

</td><td>

It shouldn't be logged as an error. It should be logged as info, which is normal and valid. It's not an error. It's a note recorded during startup and completely expected when connecting to a non-RaptorDB database. However, if this is Oracle DB, the message is unnecessary. This message should not be logged at all.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2051763

</td><td>

The C2R error occurs for all the Workflow Data Fabric \(WDF\) queries

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2052676

</td><td>

Cache flushes are triggered, even when the cache is not used/populated

</td><td>

The number of cache flush messages for the table 'cmdb\_rel\_ci' is in the 80 million+ range every hour. In a way, it's making 80 million inserts into the sys\_cache\_flush table. 'cmdb\_rel\_ci' is paired with 'graph\_cmdb\_rel\_type\_cache'. The cache graph\_cmdb\_rel\_type\_cache isn't enabled, but the cache pairing is still in a static block and is active.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1962784

</td><td>

Property glide.​db.​alter\_​large\_​table\_​threshold can't be set large enough

</td><td>

When creating a table with greater than 2,147,483,647 rows, if glide.​db.​alter\_​large\_​table\_​threshold is set to 4B, it will not upgrade. The following error occurs on the upgrade: '2025-11-08 12:48:19 \(829\) worker.1 worker.1 txid=730511129301 DictionaryXMLParser \*\*\* WARNING \*\*\* Skipping table: cmdb\_rel\_ci \(too large to alter\)'.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB2052093

</td><td>

There's a three-way deadlock between Preferences, TableDescriptor, and TableRotationExtension, which causes node restarts in production

</td><td>

Preferences.get\(\) holds the Preferences.class monitor across a database query and table descriptor lookup, while the AMB cluster synchronizer thread holds a TableRotationExtension instance monitor across a field normalization engine call. The two lock-acquisition orders are inverted, producing a classic AB-BA deadlock that starves any thread attempting to call Preferences.get\(\) until one of the two owners is killed by the deadlock sweeper.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB1996837

</td><td>

The Data Management Console does not account for partitions while calculating table size when a table is partitioned

</td><td>

When sys\_attachment\_doc is partitioned, the Data Management Console for attachments reports only the size of the parent table, not the sum of all partitions. This causes the displayed table size to appear significantly smaller than the actual disk usage.

</td><td>

1.  Open a MariaDB Instance.
2.  Migrate it to Raptor with partitionining the sys\_attachment\_doc table.
3.  After the migration check the attachment table on the instance.

 Notice that the report for attachments only reports the size of the parent table, and not the entire sum of all partitions.

</td></tr><tr><td>

Data Management Console

 PRB2070406

</td><td>

Use the 'Audit' column in sys\_dictionary, which already exists, to skip sys\_audit peripheral stats computation

</td><td>

Stats gatherer times out after six hours. For certain instances, the time spent on sys\_audit stats is around four and a half hours. This can be significantly reduced by skipping tables for which sys\_audit is turned off.

</td><td>

Trigger 'Stats gatherer' in any Zurich instance.

 Observe that sys\_audit stats is called for every table.

</td></tr><tr><td>

Data Snapshots

 PRB1973364

</td><td>

The pa\_power\_user role cannot enable data snapshots from the 'Indicator' form even though it is possible to from the Indicators Library, which is inconsistent behavior

</td><td>

The 'Enable' option should appear consistently and enforce the rule that it only works when an existing source is available.

</td><td>

1.  Log in as a user with the pa\_power\_user role.
2.  Open the Indicators Library.
3.  Select an indicator eligible for data snapshots.
4.  Observe that the 'Enable' option is available.
5.  Open the same indicator in the Indicator Form.

 Observe that the 'Enable' option is missing.

</td></tr><tr><td>

Dependency Views

 PRB1882781

</td><td>

The relationship between nodes always shows up as 'Depends on::Used by' even though the relationship in cmdb\_rel\_ci is different for a dependency view

</td><td>

The relationship between nodes is not defined as it is in cmdb\_rel\_ci.

</td><td>

1.  Open the ngbsm\_script table.
2.  Create a record with the script.
3.  Navigate to **Dependency Views** &gt; **View Map**.
4.  Search for 'Blackberry'.
5.  On the filter panel, select the entry created in step 1 from the 'Dependency Type' drop-down list.

 Notice the loaded map, and that all the relationships show as 'Depends on::Used by' instead of the actual relationship between the nodes as defined in cmdb\_rel\_ci.

</td></tr><tr><td>

Developer Sandboxes

 PRB2054240

</td><td>

The scheduler claim mutex \(sys\_mutex\) isn't sandbox-aware and forces DSB nodes to contend for a cluster-wide lock, causing scheduled-job pickup delay

</td><td>

 

</td><td>

1.  On a multi-node instance \(50+ nodes\), turn on Developer Sandboxes.
2.  Create at least 20-30 sandboxes.
3.  Multiple isolated sys\_triggers should exist in the sandboxes.
4.  Pull stats.​do?​include=​otel.​scheduler\* on the sandbox's node.

Observe that claim\_lock\_time averages above one second \(expected ~13ms\), jobs\_lateness averaging 300+ seconds, and worker capacity used is very low.

5.  Compare against a controller node on the same instance.

 Observe that claim\_lock\_time is still elevated but jobs\_lateness stays within a few seconds, because base nodes don't pin an entire platform triggers on one node.

</td></tr><tr><td>

DirectSQL

 PRB2077815

</td><td>

Implicit joins should never be added for virtual fields

</td><td>

**Virtual** fields \(such as dbfunctions\) don't exist on the database and therefore never need implicit joins to a partition. The current code sends all column references through the addNeededJoinsForColumn path and incorectly adds a self join. This can happen when the dbfunction is on a child TPH or TPP table because the ED looks like it's on a different storage table than the base table.

</td><td>

 

</td></tr><tr><td>

Document Management Services

 PRB2033668

</td><td>

The 'Document Display' component displays different message button tooltips

</td><td>

The **Now Assist** button also displays the 'Download' tooltip. The **Download** button displays the 'Zoom in' tooltip. The **Zoom In** button has no tooltip.

</td><td>

 

</td></tr><tr><td>

Document Management Services

 PRB2039067

</td><td>

Smart redaction with redaction codes and notes for documents

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Management Services

 PRB2056919

</td><td>

SmartDocs enablement in UI16 and ServicePortals

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Viewer

 PRB2038307

</td><td>

The smart document skill doesn't invoke the agent and doesn't render anything on Now Assist Panel \(NAP\)

</td><td>

The 'Ask Now Assist' smart document button doesn't work as expected. When the user selects the button, it opens the NAP, but it just shows the topics and doesn't load the summarization of the document.

</td><td>

1.  Navigate to **Contract Workspace** &gt; **Default List** &gt; **List** &gt; **Contract Requests** &gt; **All**.
2.  Open any contract request.
3.  Select the **Contract Documents** tab.
4.  Select **Preview Document**.
5.  Select a document to preview, which opens it in a new tab.
6.  Select the **Ask Now Assist** button, which opens the NAP.

 Observe that the NAP loads for some time and then shows topics. Selecting the button again just loads the topics.

</td></tr><tr><td>

Document Viewer

 PRB2056915

</td><td>

Support in document viewer for the doc to voice agent

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Dynamic Schema

 PRB2054198

</td><td>

Users are unable to use OrderBy dynamic attributes

</td><td>

 

</td><td>

1.  On a Zurich+Oracle instance, attempt to issue a query that's ordered by a numerical dynamic attribute.
2.  Verify if it's ordered properly:
    1.  Ordering should happen \(the OrderBy isn't ignored\)
    2.  Ordering should happen numerically, not alphabetically.

</td></tr><tr><td>

Edge Encryption

 PRB1998926

</td><td>

The Edge command-line installation doesn't work on Java 21

</td><td>

 

</td><td>

1.  Ensure that Java 21 is running.
2.  Download the command-line install artifact.
3.  Run the command line install artifact to install Edge proxy.

 Expected behavior: Edge proxy installs successfully.

 Actual behavior: An error occurs indicating that Java 17 is required.

</td></tr><tr><td>

Edge Encryption

 PRB2051049

</td><td>

The edge decryption job doesn't decrypt audit records when an FE encryption configuration is active

</td><td>

During edge-to-cle migration, the user needs to run an edge decryption job while the CLE EFC is active. However, because it does not currently audit **CLE** fields, the check to see if the column is audited returns false. If the user has edge encrypted audit data, the migration \(decryption\) job will not migrate the audit data.

</td><td>

1.  Inactivate the edge configuration.
2.  Configure the field with an active EFC so that it will be field encrypted.
3.  Schedule the edge decryption job, ensuring that historical data will be processed.
4.  Run the job.

 Expected behavior: The execution records \(sys\_encryption\_job\_execution\) are created for the audit table's new/old value fields.

 Actual behavior: No execution records are created for audit table fields.

</td></tr><tr><td>

Email Notifications

 PRB1965886

</td><td>

The NACM Sparkle icon is not available in the email composer for the ERR skill

</td><td>

The Sparkle icon should be available when selecting the email composer body area.

</td><td>

1.  Install the latest email-client app and latest UXC generative AI app.
2.  Enable the ERR skill for ITSM.
3.  In Service Operations Workspace, open the email composer for any incident record.
4.  Select the composer body.

 Observe that **NACM sparkle** icon is not available for using ERR skill.

</td></tr><tr><td>

Email Notifications

 PRB2083210

</td><td>

Pass the reply ID and response type in a payload when performing pre-send validation

</td><td>

 

</td><td>

1.  Select **Reply** in an activity stream in a configurable send-enabled instance.
2.  Try to send.

 Before sending, the validation must catch the reply ID and response type so that further custom logic can be written to the reply ID.

</td></tr><tr><td>

Embedded Help

 PRB2056339

</td><td>

Replace all occurrences of 'Now Assist' text with 'AI' across the Help Center and embedded help

</td><td>

 

</td><td>

1.  Open Help Center or embedded help.
2.  Open a document that was created using AI-generated help.

 Observe that 'Now Assist' text is displayed for AI-generated help articles.

</td></tr><tr><td>

Embedded Help

 PRB2057373

</td><td>

Instance Observers have some http connections that breach Cryptography Standard

</td><td>

Cryptography Standard \(POL0020873\), section 2.4 Data in Transit Encryption, requires TLS for all connections. SysEng: Core is decommissioning CDN HTTP endpoints to support modern ServiceNow technologies. However, Instance Observers currently depend on HTTP for some connections and can't migrate until this dependency is removed.

</td><td>

 

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB2073966

</td><td>

Implement extension point for IKBViewAs in glide-taxnomy

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Encryption

 PRB1982641

 [KB2977274](https://hi.service-now.com/kb_view.do?sysparm_article=KB2977274)

</td><td>

Scan checks are missing null checks, causing the instance scan to fail

</td><td>

After running the 'Insecure GlideRecord Calls', if the getFunctionCallParamters\(\) function brings back an empty object, the instance scan fails.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Experimentation Platform

 PRB2088196

</td><td>

True-up of the Experimentation Framework store app from 1.1.14 to 1.1.20

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

External Content Connectors Glide

 PRB2088042

</td><td>

Scriptable API SearchExternalContentQueryApi doesn't work

</td><td>

The scriptable API that lets a non-maintenance user with the high-security-admin role verify the permissions of a given URL or item ID doesn't work. For such a user, the API is expected to return all metadata for the item except the text field \(the actual indexed content\), including the security fields ext\_groups\_read, ext\_users\_read, ext\_content\_all\_access, and ext\_content\_none\_access along with other fields - but this does not work.

</td><td>

1.  Sign in as a non-maintenance user with the high-security-admin role \(for example, ais\_high\_security\_admin\).
2.  Call the Index Inspector scriptable API for a given URL/item ID.
3.  Inspect the returned metadata, including ext\_groups\_read, ext\_users\_read, ext\_content\_all\_access, and ext\_content\_none\_access.

 Expected behavior: All metadata except the text field is returned, including the security fields.

 Actual behavior: It doesn't work.

</td></tr><tr><td>

Field Service Task Bundling

 PRB2079508

</td><td>

Changing the assignee of the child work order task \(WOT\) of a bundle task makes the bundle task disappear from Dispatcher Workspace

</td><td>

 

</td><td>

1.  Impersonate as a dispatcher.
2.  Create a work order from Customer Service Management workspace.
3.  Create two work order tasks in the work order record.
4.  Select **Ready for dispatch** for both WOTs.
5.  Open Dispatcher Workspace.
6.  Select the two WOTs and select **bundle**.
7.  Drag and drop the bundle task to some assignee.

 Changing the assignee of the child work order task \(WOT\) of a bundle task makes the bundle task disappear from Dispatcher Workspace.

</td></tr><tr><td>

Field Service Task Bundling

 PRB2080761

</td><td>

Dynamic bundling creates unassigned bundles

</td><td>

Set assignment\_group on bundles created through dynamic bundling. When a task is added to an existing bundle, the bundle's assignment group is now carried into the task update payload, and when a new bundle is created the assignment group of the selected agent \(resolved via the new \_getGroupIDForAgent helper\) is written to both the new bundle and the task update payload. For the territory model, FSMTaskBundleSNC.\_getTasks now rolls up the assignment group from a subtask when the bundle itself has none, so territory-based bundles are no longer left without an assignment group.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1937004

</td><td>

A script step reference input gives a string \(sys\_id\) instead of GRProxyStatic

</td><td>

A compilation should have the action's script input as a reference, but the action's script step input is resolved to a string on recompilation.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1943894

</td><td>

Looping over records using 'built in iterator' is significantly slower than the normal GlideRecord iteration

</td><td>

Flow engine should take a similar amount of time to iterate over records and script or Java when no quiescing occurs, but run times are 16.8x - 73.6x slower.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2059346

</td><td>

Flow context gets completed, but the event isn't relayed to playbook engine, so the activity context doesn't get completed

</td><td>

 

</td><td>

1.  Create a playbook with one normal activity \(say instruction\).
2.  Add one optional activity \(instruction\).
3.  In runtime, add six instances of the optional activity.
4.  Start marking the optional activity complete, from the last in the list to the top.

 Observe that the corresponding activity context is in progress, but the flow context gets completed.

</td></tr><tr><td>

Flow Engine

 PRB2062691

</td><td>

Action Fabric flow complexity is insufficient for pricing estimation exercises

</td><td>

The complexity\_bucket attribute contains values grouped into bucket\_0\_10, bucket\_11\_50, and likely no other buckets.

</td><td>

1.  Perform MCP requests on an instance with Action Fabric telemetry.
2.  View the Action Fabric telemetry via Clickhouse or logged data.

 Expected behavior: The exact complexity of the MCP flows are recorded.

 Actual behavior: The complexity\_bucket attribute contains values grouped into bucket\_0\_10, bucket\_11\_50, and likely no other buckets.

</td></tr><tr><td>

Flow Engine

 PRB2069407

</td><td>

Refer to the commons-glide servicetype instead of engine code

</td><td>

Currently, it's passing mcp-server as the service type for mcp, but it should use InboundServiceType to keep consistent.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2073167

</td><td>

Add new metric for flow runtime complexity called from non-mcp

</td><td>

The system currently tracks metrics for flow runtime complexity. There is a need to add a new metric specifically for flows called from non-mcp.

</td><td>

1.  Trigger a flow execution via a non-MCP channel \(Browser/UI, Integration channel, Mobile, or any execution path that is not MCP\).

Observe that flow runtime complexity metrics are not being recorded with the granularity/buckets defined for non-MCP execution.

2.  Compare against expected bucket definitions: Bucket 1 \(1-2\) through Bucket 24 \(1000+\).

 Expected behavior: For all non-MCP execution paths \(Browser/UI, Integration channels, Mobile, and any non-MCP path\), flow runtime complexity metrics are recorded using the new, more granular bucket set, without affecting existing metrics.

 Actual behavior: No dedicated metric/bucket set exists for non-MCP execution paths.

</td></tr><tr><td>

Flow Engine

 PRB2079986

</td><td>

Add 'custom/non-custom' for the non-mcp flow metric

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2019712

</td><td>

The 'See Related Flows' action in 'subflow' displays flows with no current reference to a subflow when stale sys\_hub\_sub\_flow\_instance records exist from old snapshots

</td><td>

The 'See Related Flows' action in 'subflow' displays that the subflow is referenced by other flows even though it is not.

</td><td>

1.  Open an exiting subflow that is referenced by another subflow/flow\(parent\).
2.  Create a copy of this subflow.
3.  Activate it.
4.  Edit the parent flow by adding a step calling the copied subflow.
5.  Save/activate the flow.
6.  Edit the parent flow again, and remove the step that calls the copied subflow.
7.  Save the flow.
8.  Open the copied subflow and from the 'Actions'.
9.  Choose **See related flows**.

 Notice that the flow is still shown referencing the parent flow.

</td></tr><tr><td>

Flows

 PRB2086973

</td><td>

The base instance version of Flow Designer uses the wrong property check for flow recommendations

</td><td>

The issue occurs in Zurich.

</td><td>

1.  Open a Zurich base instance with Flow Designer.
2.  Turn on flow recommendations.
3.  Navigate to a flow.
4.  Enter edit mode.

 Notice that the recommendations don't show up.

</td></tr><tr><td>

GlideAggregate API

 PRB2090884

</td><td>

For non-admin callers, a regression results in the **Aggregate/Stats API** field validation conflating 'field doesn't exist' with 'field exists but read-ACL denies it'

</td><td>

When a non-admin caller queries the Aggregate/Stats API \(/api/now/stats/\{table\}\) using sysparm\_min\_fields, sysparm\_max\_fields, sysparm\_avg\_fields, or sysparm\_sum\_fields, the API incorrectly rejects fields the caller is not allowed to read as if those fields did not exist. Any non-admin identity that has a field-level ACL restriction on one of the fields it requests receives a hard failure instead of the expected ACL behavior. This is a regression related to PRB2081870, which addressed reflected XSS issues.

</td><td>

1.  Pick any table \('T'\) with a field \('F'\) that has a field-level read ACL restricting a non-admin role.
2.  As the non-admin identity, get /​api/​now/​table/​T?​sysparm\_​fields=​F,​sys\_​id&amp;​sysparm\_​limit=​1 and confirm F is absent or blanked in the response.
3.  As the same non-admin identity, call: GET /​api/​now/​stats/​T?​sysparm\_​max\_​fields=​F.​

 Expected behavior: Either a normal aggregate result with F omitted/blank, or a proper ACL-style denial.

 Actual behavior: HTTP 400, 'Invalid sysparm\_max\_fields parameter' - reported identically to what a user would see for a field name that doesn't exist on T at all.

</td></tr><tr><td>

Global Ranking

 PRB2035527

</td><td>

Users aren't able to delete a scrum task from cross-scope

</td><td>

 

</td><td>

1.  Navigate to Collaborative Work Management \(CWM\) Workspace.
2.  Open any board.
3.  Turn on the 'Story &amp; Scrum' task.
4.  Add story &amp; scrum tasks records to the board.
5.  Try to delete the scrum task.

Observe that the shadow task is deleted but the actual scrum task isn't deleted.

6.  Refresh the board.

Observe that the deleted scrum task reappears.


</td></tr><tr><td>

GraphQL API

 PRB1971802

</td><td>

GraphQL has unhandled exceptions for unsupported tables, causing issues for introspection queries

</td><td>

When GlideRecord attempts to init an MIFVTable on an instance where no profile is defined, or the profile type is not supported, an exception is thrown and ends up breaking introspective GraphQL queries. When the tables are collected for an introspection query, it can catch exceptions thrown for an individual table, log the exception, and avoid breaking the entire query.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1960695

</td><td>

Don't run an external port test if hermes sys\_service doesn't exist

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB2075454

</td><td>

Voice evaluation’s Otto 'mic' icon is missing on the homepage in the latest skill kit

</td><td>

 

</td><td>

1.  On an instance running the Otto skill kit, navigate to the 'Agentic Evaluations' homepage.
2.  Select the **Select what you want to evaluate**modal.

 Observe that the chat agent or workflow icon renders correctly. The voice agent or assistant \(mic\) icon doesn't render.

</td></tr><tr><td>

Horizon iFrame Component

 PRB2074065

</td><td>

Users get an error when trying to access the iFrame related configurations

</td><td>

Users get the following error: 'Uncaught TypeError: Cannot read properties of null \(reading 'parent'\) at Object.&lt;anonymous&gt; \(now-iframe.js:48:16\) iframeWindow. parent. addEventListener \('message', function \(e\) \{ const \{data, origin\} = e;'.

</td><td>

 

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

 PRB2075799

</td><td>

Create definitions for cases created by external users in Portals and Engagement Messenger

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

 PRB2076022

</td><td>

'Customer history' keeps loading on a front-line case page

</td><td>

 

</td><td>

1.  Create a user with the frontline agent role, CSM manager role, and workspace user role.
2.  Navigate to CRM workspace.
3.  Create a case.
4.  Navigate to 'Customer history' on the contextual side panel.

 Expected behavior: 'Customer history' should load.

 Actual behavior: The 'Customer history' tab keeps loading.

</td></tr><tr><td>

HR Service Delivery

 PRB1998455

</td><td>

Choices of multi-row variable sets \(MRVS\) aren't translated in the rich description of an HR case created from a record producer

</td><td>

Stored values appear in English.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2057715

</td><td>

ZTSD dare RCAs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2059123

</td><td>

RCAs in the 'Requested' state for HR case assistant and HR Case Creation agent

</td><td>

 

</td><td>

1.  Open an instance.
2.  Ensure that there's no RCA for source as 'Tool: Add comment to HR case'.
3.  Call the Unified Orchestrator.
4.  Ask the voice agent to look up an HR case.

Notice that the agent asks for soft pin. After providing soft pin, the agent confirms that user is authenticated.

5.  Provide the number for HR case opened.

 Notice that when asked to add comments to case, there is an RCA, and another RCA is generated in the 'Requested' state the when user asks for case creation.

</td></tr><tr><td>

HR Service Delivery

 PRB2063926

</td><td>

Semantic index changes for HR Service and HR Case for predicting the HR Service

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HTTP Client

 PRB2031497

 [KB3137790](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137790)

</td><td>

A rest step sees Norwegian characters in the XML response body from an external API with incorrect encoding

</td><td>

The Norwegian characters are displayed as '�'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Identification and Reconciliation API

 PRB2004173

</td><td>

A certification audit produces incorrect failed results for first and last records when a template has reference-based related list conditions

</td><td>

This only impacts audits with reference-based related list conditions \(non-REL: join\_column in cert\_related\_list\_cond\). Attribute conditions, CI/User/Group relationship conditions, and REL:-based related list conditions are unaffected as they use different code paths.

</td><td>

 

</td></tr><tr><td>

IDR - Scheduled Replication

 PRB1937502

</td><td>

The scheduled replication 'Percent Complete' doesn't take updated records into account \(%\)

</td><td>

The percentage from the scheduled replication 'Percent Complete' is inaccurate. For example, it says '66.56%' for 'Percent Complete' despite the status being 'Completed'.

</td><td>

1.  Perform a scheduled replication test with inserts and updates.
2.  Update a third of the records inserted.

 Expected behavior: Scheduled seeding replication requests show the percentage 100% when complete.

 Actual behavior: Only the actual number of records sent over seems to be reflected in the percentage.

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB1988771

 [KB3082116](https://hi.service-now.com/kb_view.do?sysparm_article=KB3082116)

</td><td>

IPAccessListFilter handling for malformed IP addresses

</td><td>

Inbound REST API calls coming through proxy servers \(x-forwarded-for header with multiple IP's\) or malformed IP address can sometimes fail in Zurich and Australia instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB2055912

</td><td>

originatedFromFlow is always false in Integration​Usage​Transaction​Monitor,​ as flow-origin detection is broken for action fabric record-action metering

</td><td>

The originatedFromFlow dimension on action fabric record-action telemetry is never set to true. Integration​Usage​Transaction​Monitor decides flow origination once, at transaction start, by checking whether the transaction's usage-tracker context contains a UsageSource.FLOW event. That event doesn't exist yet at transaction start, is removed again before transaction completion, and for asynchronous/scheduled flows the monitor doesn't run at all \(background transactions are not a handled type\). As a result, record actions performed by flows are not attributed as flow-originated, degrading the accuracy of record-action metering.

</td><td>

 

</td></tr><tr><td>

Install Base Management Store

 PRB2059577

</td><td>

Install base items and sold products should support RAC fallback mechanism

</td><td>

The functions \_skipFetchEntities and getQRfallbackRoles should be overridden in CSMRelationshipServiceSNC in CSMRelationshipService \_InstallBaseRelatedParty to allow this fallback mechanism.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB2086800

</td><td>

True-up for Workflow Data Fabric credits

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB2058369

 [KB3140571](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140571)

</td><td>

Midserver is unable to fetch credentials after upgrading to Zurich or Australia

</td><td>

In certain versions, there's a Unified Secrets Gateway \(USG\) service for credential management. During the upgrade to those versions, a system trigger script is designed to automatically execute and populate the sys\_​secret\_​identity\_​group\_​member table with the MID Server identity group mappings required for USG authentication. However, this trigger fails to complete successfully, leaving the table incompletely populated. As a result, the MID Server can't authenticate with USG and fails to retrieve credentials.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Knowledge Center

 PRB2089021

</td><td>

Article Optimization's 'Auto-Fix' feature fails across multiple instances \(update errors, revert broken, or page unavailable\)

</td><td>

The Article Optimization 'Auto Fix' feature in Knowledge Center is broken across most instances. Auto-fix either fails with a critical error during an update, the revert doesn't work, or the Article Optimization page itself isn't available.

</td><td>

1.  Open the instance.
2.  Navigate to the 'Article Optimization' list page.
3.  Select the check/checkbox for the article to auto-fix.
4.  Trigger the **Auto-fix** action.
5.  Check the 'History' tab for the resulting revert-able batch entry.
6.  Select the batch from 'History'.
7.  Apply **Revert**.

 Expected behavior: The article should be checked out and a new article version should be published with the applied auto-fix changes. This should display in the 'History' tab for revert purposes. Selecting the batch from 'History' and applying**Revert** should return the article to its previous state, and it should become visible again for auto-fix.

 Actual behavior: An error displays: 'Update failed. Failed to update articles. Please try again or review the errors under 'History.'' \(Alert level: Critical\)'.

</td></tr><tr><td>

Knowledge Graph \(Family\)

 PRB2063201

</td><td>

Add support for dynamic table lists in the KG Affinity API for affinity data loading

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1997589

 [KB2970962](https://hi.service-now.com/kb_view.do?sysparm_article=KB2970962)

</td><td>

A published article displays a grey HTML body when ECE and the 'Minor edit' property are turned on

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Knowledge Management

 PRB2000452

</td><td>

The **Edit** button isn't visible in any of the previous versions of the articles in workspaces

</td><td>

After upgrading Zurich, the **Edit** button doesn't appear when users open an outdated Knowledge article in the kb\_view page of any workspace. The article is displayed in read‑only mode and authors, KB owners, or admins cannot switch to the full record view to make changes. This prevents necessary updates to legacy articles.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2058947

</td><td>

Update versions for the base instance Knowledge Management apps to include Australia and Zurich fixes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2060905

</td><td>

Updating versions for the base instance Knowledge Management apps to include Australia and Zurich fixes

</td><td>

There are fixes in app-knowledge-center, app-knowledge-gen-ai, app-kb-uib, and sn-enhanced-content-editor.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2076447

</td><td>

The Auto-fix plugin update blocks the Australia Patch 5m upgrade in loadsim release testing

</td><td>

The plugin upgrade thread handling becomes stuck in an error loop triggered by a null pointer. It never exits or advances, leaving the upgrade 'hung'. This happens when the upgrade plugin loader reaches the knowledge center update that adds in the auto-fix and auto-fix enable property.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2084586

</td><td>

True-up Store apps NAKM, KC, KCInWorkspaces and ECE versions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2084781

</td><td>

For markdown, the knowledge blocks addition shouldn't be allowed on the kb\_knowledge.do page

</td><td>

 

</td><td>

1.  Provision an instance with the plugin com.snc.knowledge\_blocks installed.
2.  Make sure the UI16 and workspace changes and the markdown changes are present.
3.  Create a knowledge article kb\_knowledge.do page with 'Knowledge' as Knowledge base
4.  Check if the **Add blocks** UI action is visible.

 Observe that the UI action isn't visible for wiki articles.

</td></tr><tr><td>

Knowledge Management

 PRB2085202

</td><td>

A page scroll bar isn't seen for long markdown articles, as in the case of HTML

</td><td>

The issue doesn't appear in Workspace.

</td><td>

1.  Log in to an instance.
2.  Create a markdown type article.
3.  Open the article.
4.  Navigate to the related list.
5.  Translate the article.

This opens kb\_create\_translations.do.

6.  Observe the page scroll.

 Expected behavior: The content on both side should be scrollable.

 Actual behavior: The content isn't scrollable.

</td></tr><tr><td>

Knowledge Management

 PRB2086922

</td><td>

The 'KB Health score config' column is missing from the kb\_knowledge\_base table

</td><td>

 

</td><td>

1.  Provision an Australia or Zurich instance with the NAKM plugin installed.
2.  Check the kb\_knowledge\_base table.

 Observe that it doesn't have the 'KB Health score config' column.

</td></tr><tr><td>

Knowledge Management

 PRB2090439

</td><td>

Due to Generative AI Controller \(GAIC\) layer issue, multi-KB generation is broken and Mosaic migration should be reverted

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Language and Translations

 PRB1945159

</td><td>

When adding an affected CI from the related list in Service Operations Workspace and native UI incident forms, the configuration class search doesn't function correctly when using the Finnish language

</td><td>

The Configuration Class search does not work correctly when adding affected CIs from the related list in Service Operations Workspace and native UI Incident forms while using the Finnish language. It works as expected with English words, but not with Finnish words.

</td><td>

1.  Open an instance where the language is Finnish \(Suomi\) or any language other than English.
2.  Navigate to **Service Operation Workspace**.
3.  Open any available incident.
4.  In the 'Related Records' tab, locate the 'Affected CI' section.
5.  Select the **Lisää" \(Add\)** button.
6.  In the **Konfiguraation luokka \(Configuration Class\)** field, search using '\*päätepiste'.

 Expected behavior: Matching Configuration Classes related to päätepiste should be returned.

 Actual behavior: No results are returned, even though a Configuration Class related to päätepiste exists in the system.

</td></tr><tr><td>

Language and Translations

 PRB2083978

</td><td>

Standard translation merge process

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB2013721

</td><td>

The **Resume Case** UI action doesn't work as expected for certain users

</td><td>

When a user with the admin role accesses an HR case but is restricted by a security policy, the **Resume Case** UI action does not restore the activity set to the 'Running' state. Instead, the activity remains in the awaiting\_trigger state, preventing the case workflow from continuing.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2024845

</td><td>

The ListHighlighted ValueService cache key is missing highlightedValueConfigId, and causes cache collisions between requests with different configuration IDs

</td><td>

The highlighted values in the Workspace list render intermittently. It works right after cache.do then stop after a few minutes, because ListHighlightedValueService's cache key omits highlightedValueConfigId. There are multiple requests for the table, workspace, and fields but different \(or null\) configuration IDs collide on the shared static cache. As a result, whichever request populates the cache first determines the result for all subsequent requests until the entry expires.

</td><td>

1.  Create a sys\_highlighted\_value for table=incident, field=state, with a simple condition where the state is not empty, color=blue, and status=positive.
2.  Create sys\_​ux\_​highlighted\_​value\_​config 'A' with M2M-linked to the highlighted value through sys\_​ux\_​m2m\_​highlighted\_​value\_​config.​
3.  Create sys\_​ux\_​highlighted\_​value\_​config 'B' with no M2M link to any highlighted value.
4.  Navigate to **cache.do** to flush the caches.
5.  Navigate to sys.scripts.do.
6.  Run the script.

 Expected behavior: It should be 'CONFIG\_B=0, CONFIG\_A=1'.

 Actual behavior: Notice that it is 'CONFIG\_B=0, CONFIG\_A=0,' and A reuses B's cached empty result.

</td></tr><tr><td>

List Administration

 PRB2027491

</td><td>

There's a null pointer exception in List​Layout.​ get​Grouped​Row​Layout​Query from a null integer auto-unbox on List​Layout​Builder.​ get​Record​Count​Limit\(\)​

</td><td>

Any workspace preset that calls getListLayout / getTinyListLayout with ignoreTotalRecordCount=true and a GROUPBY query, on a table not in the omit-count property, is facing this issue.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2084609

</td><td>

sysparm\_filter\_only parses a query but doesn't query data

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1989084

</td><td>

In Platform Analytics, a loading indicator appears in the MID-page of the scheduled export list after applying filters

</td><td>

In the Scheduled Export list, when applying any filter, the loading indicator is displayed in the middle of the web page rather than at the top. As a result, users must scroll down to notice that the page is loading, which can cause confusion.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1990422

</td><td>

A relative timestamp \(time ago\) in a workspace's 'List' view doesn't refresh unless the record itself is updated

</td><td>

In the Service Operations Workspace list view, the relative timestamp displayed under **datetime** fields, such as 'Updated' and 'Opened'\) does not refresh when the user selects the **Refresh** button, unless the underlying record has been updated. This results in a stale relative time value being continuously displayed, even though the actual absolute timestamp shown above it is correct. The issue was validated on a base instance, confirming that no customizations were involved. This behavior causes confusion for agents who rely on relative time indicators when monitoring active incident lists.

</td><td>

1.  Log in to a Zurich base instance with Service Operations Workspace enabled.
2.  Navigate to **Service Operations Workspace** &gt; **Incidents** &gt; **Open**.
3.  Identify any incident with visible **Updated** or **Opened** datetime fields.

Observe the relative timestamp directly under the datetime \(for example, '1m ago\).

4.  Wait several minutes without modifying the incident.
5.  Select the **Refresh** button on the Workspace list view.

Observe that the relative timestamp does not change, and it continues to show the original value \(1m ago\), even though more time has elapsed.

6.  Update the same incident record in the background by adding a comment.
7.  Return to the list.
8.  Select **Refresh** again.

 Observe that the relative timestamp updates to the correct value \(2m ago\).

</td></tr><tr><td>

List Filters

 PRB2031646

</td><td>

Mixed language text is displayed in the filter

</td><td>

When the session is in a language other than English, the pop-up invoked from the list filter controls displays text in English.

</td><td>

1.  Open a Zurich instance.
2.  Install the I18N: Brazilian Portuguese Translations plugin.
3.  Open the System Preferences.
4.  Switch the language to Portuguese.
5.  Open Service Operations Workspace.
6.  Select the **List** icon.
7.  Open any interaction.
8.  Select the filter control **x filtros**.

 Observe that there is English text content, such as 'Generate filters', when it should be in Portuguese, such as 'gerar filtros'.

</td></tr><tr><td>

Live Connect \(Server\)

 PRB2038719

</td><td>

Update all server side 'SQL API' references to 'Live Connect'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Live Connect \(Server\)

 PRB2062273

</td><td>

Allow user accounts to access Live Connect

</td><td>

Only service accounts were allowed to use Live Connect.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2040686

</td><td>

Linux MID Server pre-checks don't check that the service user would be able to run start.sh, before committing to an upgrade that would leave the MID Server Down

</td><td>

Linux MID Servers can end up stopped during the upgrade process if start.sh is prevented from starting the service again with 'Interactive authentication required' or 'Access denied' errors. This would also cause a Restart MID command from the instance, either from the MID Server's form, or when a plugin activation/upgrade triggers a restart, to leave the MID Server down. This problem is for error handling in this situation. That scenario should be checked for on startup, and as part of the pre-upgrade checks before committing to the upgrade. Breadcrumbs should be left before a restart, so that the MID Server can know a failed start happened, maybe read the relevant logs automatically, and clearly give the next steps to the user.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2063491

</td><td>

'LinkedHashMap$Entry' objects connected to the LRU take a couple MB

</td><td>

These objects are from 'ecc\_​queue\_​authorization\_​policy'.​

</td><td>

1.  Open a local instance.
2.  Connect to the MID Server.
3.  Create a heap dump.

 Notice that entries of 'LinkedHashMap$Entry' for ecc\_queue\_authorization\_policy have over 3MB for each entry.

</td></tr><tr><td>

MID Server

 PRB2078177

</td><td>

RDP client fails to fetch FQDN with the error 'Unknown tag 4'

</td><td>

The agent logs FQDN lookup falls back to DNS with an error. The last four bytes are the error code STATUS\_NOT\_SUPPORTED \(0xc00000bb\).

</td><td>

1.  Configure the target windows server with the following settings: **gpedit.msc** &gt; **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Credentials Delegation** &gt; **Encryption Oracle Remediation - Enabled \(Protection level - Forced Updated Client\)**.
2.  Run windows discovery with the following MID configuration: MID.​powershell\_​api.​wmi.​fqdn\_​method = RDP.

 Observe that the agent logs FQDN lookup falls back to DNS with the error: 'DEBUG \(Worker-​Expedited:​Multi​Probe-​e43cdafc3b6ecf 503886e28 e53e45aa0\)​ \[RdpClient:186\] Received NTLM response 30, 0D, A0, 03, 02, 01, 06, A4, 06, 02, 04, C0, 00, 00, BB.' The last four bytes are the error code STATUS\_NOT\_SUPPORTED \(0xc00000bb\).

</td></tr><tr><td>

Mobile Platform

 PRB2021795

</td><td>

The checklist string value ampersand is saved as '&amp;amp;'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB2033117

</td><td>

In Now Agent, the work order task questionnaire is truncated if the questionnaire is more than 100 characters

</td><td>

 

</td><td>

1.  Open the Now Agent App.
2.  Impersonate a user whose preferred language isn't English and a has work order task \(WOT\) questionnaire assigned to them.
3.  Select the **My work** option.
4.  Select the WOT.
5.  Take the questionnaire.
6.  Scroll through the queries.

 Observe that queries above 100 characters are truncated.

</td></tr><tr><td>

Mobile Platform

 PRB2070684

</td><td>

Check for SN-Client-Id in mobile request headers instead of always assuming that the user is on the lowest ordered native client

</td><td>

Mobile clients add SN-Client-Id to all request headers after the initial user\_client response. The backend should use this as the source of truth to know which experience \(native client\) the user is actively on.

</td><td>

1.  Log in to the Mobile app.
2.  Switch from the default experience to experience B.

 The backend should send responses based off of the SN-Client-Id in request headers instead of assuming the user is on the lowest ordered native client they have access to.

</td></tr><tr><td>

Mobile Platform

 PRB2084601

</td><td>

Add a logo configuration option to sys\_sg\_applet\_launcher

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB2084603

</td><td>

EmployeeWorks Mobile updates

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB2084604

</td><td>

Auto-routing AIUX links to Mobile apps

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multi-Instance Framework - Core

 PRB2063884

</td><td>

MIF Hermes doesn't refresh the cluster configuration when the local hermes\_cluster\_config has no primary or after a datacenter-rule change, causing stale/failed cluster resolution for remote owners

</td><td>

When instance A sends a MIF async message to instance B, it needs B's Hermes cluster details \(datacenter + Kafka bootstrap servers\). A keeps a saved copy in the hermes\_cluster\_config table and reads it in Hermes​Producer​Client.​get​Cluster​Info​Set.​ Today that method only calls B's live endpoint \(/api/now/hermes\_cluster\_info, tier-2\) when A has no saved rows for B. Two gaps result: 1. Saved rows but no primary — if A has rows for B where no one is is\_primary\_for\_service=true \(scenario like only a single non-primary cluster row\), the method does not refresh. And method ensure​Topic​Location​For​Instance\(String owningInstance\) then finds primaryCluster == null and the send fails with 'No primary cluster found'. 2. Stale rows after a datacenter change — if a MIMIR rule change moves B's cluster to a new DC, A's saved rows are outdated but still look complete \(they have a primary\), so tier-1 returns them and A never re-discovers → messages Navigate to the old cluster.

</td><td>

1.  Verify that Instance A has a saved Hermes cluster rows for instance B \(service MIF-Hermes\) pointing to B's old datacenter, or a single row that isn't marked primary.
2.  Send a MIF async message from A to B.

 Expected behavior: A resolves B's current cluster details and sends to the correct datacenter.

 Actual behavior: A uses the old/incomplete saved config and sends to the wrong datacenter, or fails with 'No primary cluster found'.

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2082821

</td><td>

Result and metadata attachments are written with no owning record

</td><td>

MMS writes its parsed-text and metadata result artifacts to sys\_attachment without a table\_name or table\_sys\_id, so those attachments have no owning record. Reference-image attachments are unaffected — they are correctly parented to sys\_mm\_reference\_image.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2084570

</td><td>

Enabling the 'Image' file type to be on by default for MMS for AI Search

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2084571

</td><td>

MMS Glide update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Next Experience All Menu

 PRB2074680

</td><td>

The Now Assist 'Launch Mode' menu label in Display Preferences is not updated to Otto

</td><td>

 

</td><td>

1.  Navigate to 'Home'.
2.  Select the user profile icon.
3.  Open 'Preferences'.
4.  Navigate to the 'Display' section.

 Observe the 'Now Assist Launch Mode' menu label.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2079464

 [KB3154841](https://hi.service-now.com/kb_view.do?sysparm_article=KB3154841)

</td><td>

Duplicate NextWave Client REST API definition causes a 403 error on session\_info for external users, disabling lbf-chat-client

</td><td>

Some users are unable to start a chat session in the assistant/chat widget. This is caused by a backend configuration issue and doesn't require any action.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2079773

</td><td>

Set token\_exchange\_allowed to 'true' on an OffGlide AIEX oauth entity record

</td><td>

Notice that token\_exchange\_allowed is 'false' which needs to be 'true', otherwise oauth will fail for guest users.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2081424

</td><td>

Set bff\_cookie\_exchange\_allowed to 'true' on OffGlide AIEX oauth entity records

</td><td>

bff\_cookie\_exchange\_allowed is set as 'false', which need to be 'true', otherwise oauth will fail for the guest user.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2085243

</td><td>

Page context updates aren't sending the backend the current URL

</td><td>

 

</td><td>

1.  Open an instance.
2.  Open AIEX.
3.  Perform any workspace navigation that triggers a page context update to the backend.

 Expected behavior: The URL is sent in the page context payload.

 Actual behavior: The URL is not sent in the page context payload.

</td></tr><tr><td>

Now Assist in Virtual Agent

 PRB2056609

</td><td>

Change the Knowledge Graph \(KG\) defaults in NAVA and Now Assist Portal

</td><td>

Today, the KG default is User NLQ graph. That should be changed so the defaults are: In Now Assist Virtual Agent for natural language query, change the graph to Enterprise Graph \(Small\) and select the tag as 'VIRTUAL AGENT DEFAULT TAG'. In Now Assist Panel for natural language query, change the graph to Enterprise Graph \(Small\) and select the tag as 'NOW ASSIST PANEL DEFAULT TAG'.

</td><td>

 

</td></tr><tr><td>

Now Assist Nextwave Experience

 PRB2059502

</td><td>

Add sys\_props for caching in sys\_og\_conversational \_cache\_configuration

</td><td>

If props are enabled on the instance, that should be reflected via cache service instantly.

</td><td>

 

</td></tr><tr><td>

Now Assist Nextwave Experience

 PRB2061245

</td><td>

SessionController shouldn't try to refresh AuthorizationInfoBundle, as this is done in the Glide handshake process

</td><td>

When a topic execution is initiated, the conversation ID isn't available in certain Glide log entries' context maps, which complicates troubleshooting across different trace IDs instead of a unified conversation ID. The conversation ID should be available in the cache and topic execution context map in the syslog table.

</td><td>

 

</td></tr><tr><td>

Now User Experience

 PRB1960854

</td><td>

JavaScriptCommentStripper doesn't work properly with the upgraded highchart bundle \(12.3.0\)

</td><td>

There's a runtime exception: 'org.​openqa.​selenium.​Javascript​Exception:​ Document was unloaded'.

</td><td>

Run IT test​Outage​Association​With​Case​IT .​check​Child​Case​Linked​To​Parent​Outage.​

 Observe that it fails on master.

</td></tr><tr><td>

OAuth

 PRB2018183

</td><td>

The not allowed system property glide.oauth. jwt.token\_request .honor\_claim\_keys is included in an upgrade payload, resulting in a misleading 'skipped' upgrade log entry

</td><td>

During a Zurich upgrade, the system property glide.oauth. jwt.token\_request .honor\_claim\_keys \(from com.​snc.​platform.​security.​oauth\)​ appears as a skipped entry. This property is not allowed by design and therefore never loaded into sys\_properties on user instances.

</td><td>

1.  Navigate to **All** &gt; **Upgrade Center** &gt; **Upgrade History**.
2.  Open the record of upgrading in Zurich.
3.  Select the **Skipped Changes to Review** tab.
4.  Select the skipped record for sys\_properties\_ 107762282 f223210 3698319 c003f9b2f.xml.

</td></tr><tr><td>

OneExtend

 PRB2056745

</td><td>

Guardian preprocess flow resolves getGeoRoutingDetails\(\) multiple times per request in NowLLMIntegration GuardianProvider

</td><td>

NowLLMIntegration GuardianProvider. shouldUseGatewayService\(\) and addLLMGatewayRoutingHeader\(\) each independently call through to GeoRoutingServiceImpl .getGeoRoutingDetails\(\) &gt; resolveGeoRoutingDetails\(\). ShouldUseGatewayService\(\) itself is invoked from multiple call sites across a single request's lifecycle \(transformRequest, generateTrustBuilderInputs, tryLogTrustBuilderResults, and twice within getUrl\(\)\). None of these calls are memoized, so resolveGeoRoutingDetails\(\) re-executes its full resolution logic \(potentially including the licensing entitlement API call\) on every invocation within the same request, even though the underlying geo-routing state can't change MID-request.

</td><td>

1.  Trigger a Guardian moderation request that routes through NowLLMIntegration GuardianProvider \(LLM\_GENERIC\_SMALL\_MODERATIONS model\).
2.  Trace/log calls into GeoRoutingServiceImpl .resolveGeoRoutingDetails\(\) \(or set a breakpoint\) during a single request's transformRequest\(\)/getUrl\(\) lifecycle.

 Observe that resolveGeoRoutingDetails\(\) executes repeatedly \(up to six times found via code trace\) instead of once per request. When the 0$ SKU entitlement isn't active, each of these calls re-invokes the expensive isEntitlementActive WithLicensingAPI\(\) licensing call, since resolveGeoRoutingDetails\(\) has no per-request memoization. Only the underlying getGeoRoutings\(\) /getGeoRoutingConfigs\(\) cache calls are cached via ADomainAwareCache.

</td></tr><tr><td>

OneExtend

 PRB2073758

</td><td>

AutoChat off-glide implementation changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2060938

</td><td>

An impersonated user sees the impersonator's bookmarked indicators, and the bookmark filter then returns no results

</td><td>

In an Indicator Scorecard, users can bookmark individual indicators \(the star on each row\) and then filter the list to 'show bookmarked only'. When an administrator impersonates another user, the scorecard incorrectly shows the admin's bookmarks as if they belonged to the impersonated user. If the bookmark filter is then applied it returns no results at all, and after turning the filter off again all bookmarks disappear from view. Impersonation is the normal way administrators and support staff verify what an end user can see. While this issue is present, that check gives the wrong answer for bookmarks, and the bookmark filter appears completely broken. Scope note: no user's bookmarks are visible to any other real user. The incorrect data is only ever shown to the administrator who is impersonating, and only within that one browser session. Logging out clears it. Verified: a different browser, or a private/incognito window, always shows the correct bookmarks.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2085934

</td><td>

AIDE **Explore** button is shown on all lists, including 'All Table Discovery' entities

</td><td>

The AIDE **Explore** button is shown on all entity lists, including entities that shouldn't have it. Only entities marked Active=true and population\_source=Table Config should display the **Explore** button. Entities with population\_source = 'All Table Discovery' \(or inactive entities\) shouldn't show the **Explore** button.

</td><td>

1.  Navigate to an entity list that is marked as 'All Table Discovery'.
2.  Check whether the **Explore** button is present.

 Expected behavior: Only entities with Active=true and population\_source=Table Config show the**Explore** button.

 Actual behavior: The**Explore** button is shown on 'All Table Discovery' entity lists.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1958926

</td><td>

Changing the Platform Analytics dashboard owner also changes the 'Created by' username

</td><td>

The **Created by** field should remain the same even when the Platform Analytics dashboard owner changes.

</td><td>

1.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Dashboards**.
2.  Create a dashboard.
3.  Enter 'Edit' mode.
4.  View the dashboard details.
5.  Change the **Owner** field value.
6.  Save the changes.
7.  Exit 'Edit' mode.
8.  Refresh the page.
9.  View the dashboard details again and observe the **Created by** field.

 Expected behavior: The**Created by** field should remain unchanged.

 Actual behavior: The**Created by** field is the same as the owner.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2035747

 [KB3120864](https://hi.service-now.com/kb_view.do?sysparm_article=KB3120864)

</td><td>

The **Create New** and **Duplicate** buttons in the Platform Analytics \(PA\) dashboard context menu are visible to users who don't have the pa\_admin or pa\_power\_user role

</td><td>

The user requests the ability to hide the **Create New** and 'Duplicate' options from the PA dashboard context menu \(⋮\) for regular users without removing broader role access.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2037900

</td><td>

A new dashboard widget is created for a sub-domain

</td><td>

In a user's instance, when the list-simple dashboard widgets migrated to list widget, the corresponding dashboard widgets were duplicated and new records were created in the user domain. This isn't the expected behavior, since nothing like this happens for par\_visualization record. The list-simple to analytics list migration is a background flow that executes as a system user, so when trying to do a dashboard widget update via a background script, this reproduced the same issue. This indicates that the root cause is updating a dashboard widget record while in another domain.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2053337

 [KB3152732](https://hi.service-now.com/kb_view.do?sysparm_article=KB3152732)

</td><td>

There's an increased response time of Core UI dashboards in Australia

</td><td>

The response times of Pa\_Dashboard transactions degraded by 2000ms compared. This comes from an increase in SQL time.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2058867

 [KB3152710](https://hi.service-now.com/kb_view.do?sysparm_article=KB3152710)

</td><td>

Reduce the call cost on calling isPaPremium for every dashboard get call

</td><td>

On instances with large dashboard counts \(thousands of dashboards\), this multiplies an expensive entitlement check across the full dataset, causing high memory usage, semaphore exhaustion, node failover, and an out of memory error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2059204

</td><td>

Non-admin users can't read a localized tab name on PAR dashboard in a scoped application

</td><td>

A non-admin or dashboard\_admin user can't change the localized tab name on the scoped application's dashboard.

</td><td>

1.  Create a dashboard in the application scope.
2.  Add tabs.
3.  Share it with a non-admin user as an editor.
4.  Impersonate to the user.
5.  Change language except for English.
6.  Change tab names.
7.  Save the dashboard.
8.  Reload.

 Expected behavior: The tab names have been changed.

 Actual behavior: The tab names were not changed.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2072270

</td><td>

Widgets, Permissions, and Canvas are created in the incorrect scope when a shared non-admin user edits a dashboard originally created in an application scope and leads to deletion

</td><td>

 

</td><td>

1.  Open an instance from the latest Zurich patch as an admin.
2.  Change the application scope to 'Knowledge Overview'.
3.  Duplicate the dashboard 'Knowledge Management Overview'.
4.  Validate that records created in all dashboard tables have the application scope set to 'Knowledge Overview'.
5.  Share the duplicated dashboard to the knowledge\_admin role with edit access.
6.  Switch back to the global scope.
7.  Create a user knowledge.admin with role knowledge\_admin.
8.  Impersonate as user knowledge.admin.
9.  Open the duplicated dashboard in **Edit** mode.
10. Add a single score widget to any of the existing tabs at the bottom of the tab.
11. Save the dashboard.

 Expected behavior: The new par\_dashboard\_widget entry should have the application scope as 'Knowledge Overview'.

 Actual behavior: The new par\_dashboard\_widget entry has the application scope as 'Global'.

</td></tr><tr><td>

Platform Analytics Filters

 PRB2031506

</td><td>

The 'Follow' filter toggle option is missing in a cascading filter

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1988855

</td><td>

Static content block in core UI after migration has HTML tags in the Next Experience rich text visualization

</td><td>

 

</td><td>

1.  Create a Core UI dashboard.
2.  Add a static content block.
3.  Add some contents within them, such as an embedded URL.
4.  Select the **Migrate to Next Experience** button to migrate the dashboard to Next Experience.

 Notice that in the migrated Next Experience dashboard, the rich text has HTML tags in them.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2022823

</td><td>

Allow users to configure the redirection of Core UI Performance Analytics widgets to the Analytics Hub instead of to 'KPI details'

</td><td>

Users that activated Next Experience after migrating or upgrading to Australia will be redirected to 'KPI details' when selecting a Performance Analytics widget, even if they keep using Core UI dashboards. This issue occurs because the unified\_analytics property forces the re-direction to 'KPI details'.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2037846

</td><td>

The Migration Center summary count doesn't match the list count for fully migrated dashboards

</td><td>

The Get Migration Summary Scripted API needs to be updated so that it calculates the total number of migrated dashboards in the same way as the Migrated List.

</td><td>

Scenario 1:

 1.  Create a few Core UI dashboards.
2.  Migrate them.
3.  Navigate to the PAR Dashboards table.
4.  Delete one or more migrated dashboards.

 Observe that the Migrated List count and the Summary count don't match.

 Scenario 2:

 1.  Create a Core UI dashboard containing a Dynamic Content widget.
2.  Migrate the dashboards.
3.  Navigate to the par\_coreui\_migration \_bridge\_dashboard table.
4.  Remove the record\(s\) associated with the dashboard that contains the Dynamic Content widget.

 Observe that the Migrated List count and the Summary count don't match.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2064612

</td><td>

Dashboard owner migration creates new pa\_dashboard records when triggered from a child domain

</td><td>

 

</td><td>

1.  Install the domain plugin with demo data.
2.  Create a core UI dashboard in TOP/MSP domain.
3.  Add a report in the global domain.
4.  Switch to the child domain TOP/MSP/MSP Technicians.
5.  Migrate it from the dashboard banner.
6.  Switch to the global domain.
7.  Open pa\_dashbaords.list and expand domains.

 Observe that there are two core UI dashboards.

</td></tr><tr><td>

Platform Runtime

 PRB1996636

</td><td>

An orbit dist-upgrade preserves the previous version of conf/tomcat-host.xml on node upgrades for self-hosted instances

</td><td>

The host configuration file conf/tomcat-host.xml on a ServiceNow application node isn't updated during node upgrades on self-hosted instances, as the Orbit dist-upgrade function is preserving this file from the original pre-upgrade version. This happens in the same manner glide.properties, glide.db.properties, and the contents of conf/overrides.d/ are preserved, by copying them from the existing node before the upgraded node files are copied to the original location. This is a potential issue, as the tomcat-host.xml config file is occasionally modified from time to time to fix or prevent certain issues. As the file is preserved during an upgrade on a self-hosted instance, that leaves self-hosted users running with outdated versions of tomcat-host.xml and thus vulnerable to issues.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2056633

</td><td>

A playbook activity start delay doesn't work if its less than 11 seconds

</td><td>

The 12 second start delay seems to be the minimum honored threshold.

</td><td>

1.  Create a simple playbook with 1 stage and 2 instruction acts.
2.  Configure activity 2 to have a start with delay for 11 seconds.
3.  Test the playbook.
4.  Notice that the activity is set in progress after activity 1 completed and there is no 11 second delay.
5.  Configure activity 2 with a 12 second start with delay.
6.  Test the playbook.

 Observe that after activity 1 is complete, the delay is honored, and activity 2 doesn't start until after 12 seconds.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2062029

</td><td>

Changes to the permission sets are not working as expected

</td><td>

The users should have the pd\_author role.

</td><td>

1.  Create a playbook that uses 'incident' as the parent table.
2.  Add two stages. Each stage should include at least on activity.
3.  Activate it.
4.  Open the 'Process properties' side panel.
5.  Select the **Runtime permissions** tab.
6.  Add a permission set of type users.
7.  Dot-walk to the **Assigned to** value of the parent record
8.  Activate the playbook.
9.  Test the playbook using the incident that involves the users set up with the permissions for it.
10. View it in 'Preview'.
11. Impersonate the caller of the incident.
12. Return to the playbook preview.
13. Refresh it.

 Expected behavior: The user should see nothing.

 Actual behavior: The user can see the playbook execution.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2086543

</td><td>

When resolving overrides for AI-experiences, the first matching overrides containing aixWidget should be returned

</td><td>

PlaybookActivityOverrideRepo .initializeByPlaybook ExperienceId\(\) only populates PlaybookActivityOverride .aixWidget from the override record's **aix\_widget.id** field. If the override record itself doesn't have an AIX widget configured, but the activity's linked activity UI record does \(activity\_ui.aix\_widget.id\), then the widget is never picked up. The override ends up with an empty/null AIX widget, so the AIX experience isn't rendered even though a widget is configured at the activity UI level.

</td><td>

1.  Create an activity UI.
2.  Populate the **AIX widget** field.
3.  Create an activity override using the above activity UI.
4.  Add conditions so that the above override is selected at runtime.

 Observe that the **AIX widget** field isn't picked from the activity UI in override at runtime. It's returned directly from the default activity UI.

</td></tr><tr><td>

Predictive Intelligence

 PRB2061744

</td><td>

Previous records of 'ml\_model\_artifact' are still present in the sys\_attachment table for the Data Analysis capability

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB2035128

</td><td>

Meter-based guardrails and controls

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB2037266

</td><td>

Process Mining Project Definition is stuck with 'Record Not Found'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB2068401

</td><td>

A Root Cause Analysis \(RCA\) fails on a child entity for all MDM projects

</td><td>

 

</td><td>

1.  Create any pair of MDM projects for the incident and problem entities, or the incident and SLA task entities.
2.  Select any eligible activity in the child entity.
3.  Run 'Key contributors RCA' from the 'Investigate' section.

 Observe that the RCA scheduled task fails for the selection. Note for the same entity without MDM setup, the RCA task is working correctly.

</td></tr><tr><td>

Process Mining Workspace

 PRB2069087

</td><td>

Update the Usage Metric Definition Id and guardrail changes for Meter Based

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1941521

</td><td>

Task type breakdowns have incorrect rolled-up actuals when the 'Budget allocation attribute' property is set to 'cost\_type'

</td><td>

The Program Actual Cost is not matching with the underlying Projects Actual Cost. There are duplicate task type breakdowns created for a program.

</td><td>

1.  Set the 'Budget allocation attribute' property to 'cost\_type'.
2.  Create a project.
3.  Create a cost plan 'CP-1' with 'Hardware Capex' for the project.
4.  Create a cost plan 'CP-2' with 'Software Capex' for the project.
5.  Create a expense line for CP-1 with 100 USD.
6.  Check the task type breakdowns \(TTB\) for the project.

Notice that there should be one 1 TTB with the 'Hardware Capex' cost type with 100 as the actuals.

7.  Create a expense line for CP-2 with 200 USD.
8.  Check the Task type breakdowns \(TTB\) for the project.
9.  Notice that there should be one 2 TTBS for 1 TTB with Hardware Capex with 100 as the actuals, and 1 TTB with the 'Software Capex' cost type with 300 as the actuals.

 Expected behavior: The TTB with the 'Software Capex' cost type has 200 as the actuals.

 Actual behavior: The TTB with the 'Software Capex' cost type has 300 as the actuals.

</td></tr><tr><td>

Project Management

 PRB1993708

</td><td>

When moving a story from one project to another, the actual effort doubles on the story

</td><td>

When assigning a story with actual hours more than 24 hours, suppose 40 hours, the story takes it as 1 day and 16 hours. However the project only adds the hours and not the days, therefore the project actual hours become just 16 hours.

</td><td>

1.  Navigate to an existing project with a story, or create one.
2.  Locate another project, or create one.
3.  Take one of the stories with logged 'Actual Hours' and move it to a different project.
4.  Navigate to the **Stories** \[rm\_story\] list view.
5.  Delete the existing **Project** field and change it from here.
6.  Choose a project.

 Observe the 'Actual effort' has doubled on the story.

</td></tr><tr><td>

Project Management

 PRB2036275

</td><td>

ProjectTemplate.java calls extension point outside null guard, so applyTemplate\(\) silently returns zero tasks within flow execution context

</td><td>

When PTGlobalAPI\(\).applyTemplate\(\) is called within a flow action \(for example, 'Implement SPM Oversight'\), the Customer Project record is created but zero project tasks are generated. The same applyTemplate\(\) call succeeds from Background Scripts on the same project record. The ProjectTemplate scripted extension point \(sys\_​script\_​include.​ 1e6e73619 f001200598 a5bb0657fcfc2,​ line 24\) performs a GlideRecord.get\(\) call where the table name resolves to null within the flow transaction context. This causes applyTemplate\(\) to silently return zero tasks. The PPM engine then attempts to recalculate the project, but the planned\_task record doesn't exist yet, producing the following error: 'com.​snc.​planned\_​task.​core.​ Planned​Task​API:​ PPM Unable to Recalculate Task : \[sys\_id\] Cannot invoke 'com.​snc.​planned\_​task.​core. ​Planned​Task.​get​Start​Date\(\)​' because 'task' is null'.

</td><td>

1.  Configure CSM Order Management project oversight with decision tables, field mappings, and project/task templates \(template tasks table = customer\_project\_task\).
2.  Submit a customer order via REST API that triggers a flow containing the 'Implement SPM Oversight' flow action.

Observe that the flow action calls Order​Line​Prj​Util​OOB. ​create​Project​For​Order​Line\(\)​,​ which calls PTGlobal​API\(\)​. ​apply​Template\(project​Sys​Id,​ templateId, actualStartDate\) at line 58 of OrderLinePrjUtilOOB.js. The Customer Project is created but zero Customer Project tasks are generated. The **Short Description** remains unchanged.

3.  Check the logs for the error 'com.​snc.​planned\_​task. ​core.​Planned​Task​API:​ PPM Unable to Recalculate Task : \[sys\_id\] Cannot invoke 'com.​snc.​planned\_​task.​core.​ Planned​Task.​get​Start​Date\(\)​' because 'task' is null'.
4.  Run the identical applyTemplate\(\) call from Background Scripts on the same project record.

Observe that tasks are created successfully.


 Expected behavior: ApplyTemplate\(\) creates Customer Project tasks from the template within the flow action.

 Actual behavior: Zero tasks are created. The ProjectTemplate extension point encounters a null table name because the project record isn't fully committed in the flow transaction.

</td></tr><tr><td>

Project Management

 PRB2050675

</td><td>

Allow the change of constraint date at the parent task level

</td><td>

Enure that the child task start date honors both the parent task and its constraint dates.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB2065386

</td><td>

'Show story' related list on non-agile phases

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB2066164

</td><td>

Certain users do not see all the drop-down list values within a grid cell in the 'RIDAC' tab

</td><td>

This issue occurs only in the grid view.

</td><td>

1.  Open the Project Workspace.
2.  Navigate to **RIDAC**.
3.  Open a project.
4.  Expand 'Risk'.

 Observe the drop-down list for the **Impact** field.

</td></tr><tr><td>

Project Management

 PRB2071094

</td><td>

Display a message if the parent change fails due to schedule conflicts

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ReleaseOps - Family

 PRB2030613

</td><td>

The **Promote Update Set** UI action is visible even when sn\_​releaseops.​deployment\_​controller property isn't set

</td><td>

The **Promote Update Set** UI action should be hidden when the sn\_​releaseops.​deployment\_​controller property isn't set. Currently it remains visible, which can confuse users who haven't configured ReleaseOps.

</td><td>

1.  Install ReleaseOps but don't set it up.
2.  On a complete local update, set the **Promote update set** button to display.

 Expected behavior:**The** button doesn't display if the property is not set/empty.

 Actual behavior: When the button is selected, an error message displays: 'Error MessageDeployment controller URL is not specified. Make sure that sn\_​releaseops.​deployment\_​controller is configured in system property'.

</td></tr><tr><td>

ReleaseOps - Family

 PRB2067737

</td><td>

ReleaseOps MIF handler bypasses the Instance Scan queue

</td><td>

InstanceScanHandler.java invokes the InstanceScanWorker directly. AScanWorker worker = InstanceScanWorker. generateFromSuites AndUpdateSets \(scanSuiteIds, updateSetIds\), bypassing the instance scan queue management. It should call the CICDInstance​Scan​Execution​Service as an entry point, to take advantage of queuing and possible future changes. In Zurich, the user can only execute one scan at a time. In Australia and onward, multiple scans are allowed using the current code but there are no checks on max number of scans that can be executed and the existing code could potentially overwhelm the instance with too many scans.

</td><td>

1.  Start a full instance scan.
2.  From the ReleaseOps controller, start moving a DR that needs to do an instance scan.

 Expected behavior: The Data Replication waits but then complete successfully.

 Actual behavior: The Data Replication fails the instance scan with an error: 'Failed to get scan result: Multiple scans cannot be run at the same time'.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB1950825

 [KB3148345](https://hi.service-now.com/kb_view.do?sysparm_article=KB3148345)

</td><td>

Remote Process Synchronization \(RPS\) sends more records to the target than that published into the transport queue

</td><td>

Remote Process Synchronization \(RPS\) is sending more records to the target than those published into the transport queue, resulting in discrepancies between outbound HTTP logs and transport queue data. The issue arises from a performance optimization feature that saves last positions for outbound jobs. When multiple capture definitions \(ih\_sync\_capture\_definition\) exceed the number of buckets, cursor backtracking occurs, leading to reprocessing of records and discrepancies in record counts. This can cause intermittent or unavailable connections between consumer applications with general usage of RPS. The issues manifest as slow response times, frequent disconnections, and periods where the connection appears down despite the RPS connection showing as **Active**. However, remote task records remain in the 'New' status and do not progress, creating a risk of transaction impact.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB2052613

</td><td>

Extremely slow processing of the RPS queue on Impact

</td><td>

With the number of connections increasing, slow processing occurs exponentially.

</td><td>

1.  Log in to Impact.
2.  Check the transaction time.
3.  Query the sn\_transport\_queue table to get the volume of the 'ready' transaction.
4.  On a subprod instance, onboard the instance via the impact onboarding process.
5.  Run the data migration.
6.  Verify the time it takes to migrate the data.

 Notice that with one or two connections, the transaction seems fast. But as the number of connections increase, performance issues happen exponentially.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB2055484

</td><td>

ProcessSyncReplicationTable's queryShard includes null labels

</td><td>

Both labeled and unlabeled entries are returned.

</td><td>

1.  Write an unlabeled entry into a cdc\_queue\_ih shard table.
2.  Write a second entry with a valid label.
3.  Trigger an RPS outbound poll for that valid label.

 Expected behavior: Only rows matching the requested label\(s\) should be returned, unlabeled entries should never match.

 Actual behavior: Query returns both the labeled entry and the unlabeled entry.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB2080234

</td><td>

Concurrent Remote Process Synchronization \(RPS\) can create too many sysevent records

</td><td>

When the main 'IB/OB' job runs, check to see the current queue size in sysevent. If it's greater than 2x the number of active remote systems, then log a 'WARN' message without creating any sysevent records.

</td><td>

1.  Enable concurrent RPS and ensure each the job takes time to run.
2.  Set the 'OB' job to run every 5 seconds.

 Observe that the sysevent queue creates records faster than they get processed.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB2080238

</td><td>

An outbound Remote Process Synchronization \(RPS\) job in Concurrent RPS is inefficient when it tries to filter the 'Capture Definition' map

</td><td>

This appears to be due to some inefficient coding in Outbound​Queue​Dao.​ get​Remote​System​ Capture​Defs​Map.​ It gets all CDs before trying to filter them with computations and comparisons. This would be more efficient if capture​Definitions.​ get​All​Capture​Definitions\(\)​ took an argument that would let users filter on a remote system before looping.

</td><td>

1.  Set up Concurrent RPS.
2.  Set up 1500 remote systems.

 See how long it takes to process a single job for a remote system without any records to process.

</td></tr><tr><td>

Reporting

 PRB2056087

</td><td>

Data labels are truncated when saving a report as a PNG

</td><td>

 

</td><td>

1.  In Core UI Reporting, create a report.
    -   Table: Incident
    -   Type: Bar Chart
    -   Group By: Short Description
    -   Aggregation: Count
2.  Save/Run the report.
3.  Observe that because **Short Description** can have long strings, the X axis labels are truncated.
4.  Change system property glide.​chart.​truncate.​ x\_​axis\_​labels = false.
5.  Run the report again.
6.  Observe that **Short Description** is no longer truncated.
7.  Export the chart to PNG using the context menu option **Export to PNG**.

 Expected behavior: The exported PNG looks like the chart, with the labels displayed.

 Actual behavior: The exported PNG has labels truncated.

</td></tr><tr><td>

Reporting

 PRB2067688

</td><td>

Reports shared with a user with the snc\_internal role aren't loading

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB2075931

</td><td>

Cart item hints do not get copied when ordering from a draft item

</td><td>

 

</td><td>

1.  Create a draft cart item.
2.  Add the hint to update the request parent to some incident.
3.  Checkout the cart item.

 Notice that the cart item hint doesn't gets populated to the request.

</td></tr><tr><td>

Roles

 PRB2023810

</td><td>

Instances without explicit roles throw an error when invoking agents with a 'Nobody' role mask

</td><td>

The following error appears in the logs: 'Role 'snc\_external' not found. Cannot be automatically created: no thrown error'.

</td><td>

1.  Open an instance that doesn't have the explicit roles plugin.
2.  Trigger an AI Agent that has a role mask on the **Nobody** field.

 Observe the error in the logs: 'Role 'snc\_external' not found. Cannot be automatically created: no thrown error'.

</td></tr><tr><td>

Schedule Optimization \(Glide Family Channel\)

 PRB2057489

</td><td>

SO conflict resolution is unassigning locked tasks

</td><td>

A conflict resolution fix was implemented to unassign tasks from the solution when the assignee has a conflict. However, it unassigns tasks even if they were locked after solution processing began. There should be a filter to skip the unassignment if the task has transitioned to a locked state.

</td><td>

 

</td></tr><tr><td>

Search Suggestions

 PRB2051556

</td><td>

The scheduled job deletes search suggestion and business rules, and should leave ones with the global namespace alone

</td><td>

The business rules created should not get deleted by the scheduled job.

</td><td>

1.  Create a business rule on some table.
2.  Set the business rule to run on the update and delete.
3.  Name it starting with 'Disable'.
4.  Set the script.
5.  Run the scheduled job, 'Remove obsolete search suggestion BRs' under sysauto\_script.

 Observe that the business rule created was deleted, and shows up in the sys\_update\_xml table.

</td></tr><tr><td>

Server-side scripts

 PRB2056793

 [KB3141731](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141731)

</td><td>

ESLatest sibling scopes shouldn't use scoped sandbox scopes

</td><td>

ESLatest sibling scopes are created when 'Ecmascript 2021' mode is turned on for global scripts. When they interact with something that requires sandbox script execution, they end up inadvertently creating an isolated scope for what essentially should be the global sandbox scope. There's a specific code path in KittyScriptEvaluator that attempts to reinitialise GlideElement in a scoped sandbox where it's not available leading to reinitialisation errors seen in the logs and triggering the causal chain that invokes this path.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Server-side scripts

 PRB2076586

 [KB3151029](https://hi.service-now.com/kb_view.do?sysparm_article=KB3151029)

</td><td>

Plugin scripts aren't registered in some app nodes

</td><td>

On some instances, a subset of nodes can experience the mega menu in Employee Center being broken. The following error appears on the screen when navigating to Employee Center, and users are unable to use the menu: 'ErrorServer JavaScript error 'sn\_taxonomy' is not defined.'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Builder

 PRB2028753

</td><td>

UI Policies in Catalog Builder are not captured within the catalog template's scope selected

</td><td>

The 'Option' UI policy introduced in Zurich isn't obeying to consider the scope of a template for Catalog UI policies. Rather, it's picking up the scope based on an application picker. Before, the option always used the scope of template for UI policies and items belonging to that catalog irrespective of what is selected in application picker.

</td><td>

1.  Log in to an Australia instance.
2.  Navigate to Catalog Builder.
3.  Select **Create a new catalog item**.
4.  Choose a template that's scoped and has the 'Use template scope for creating record' option checked.
5.  Fill in the details.
6.  When at the 'Questions' section, choose 'Dynamic behaviors' and provide the action and its condition.
7.  Submit the catalog.
8.  Navigate to 'Maintain items'.
9.  Look for the catalog just created.

 Observe the Catalog UI policies and its actions are created under the global scope instead of the template.

</td></tr><tr><td>

Service Catalog Builder

 PRB2033462

</td><td>

When creating a catalog item via Catalog Builder, UI policies configured in a previous step aren't visible on the 'Review and Submit' step

</td><td>

It appears that the GraphQL query is not being triggered for the catalog\_ui\_policy table.

</td><td>

1.  Open Catalog Builder.
2.  Create a catalog item.
3.  Configure a UI Policy, Client Script, and any other required details.
4.  Navigate to the **Review and Submit** step.

 Notice that the UI Policy is not displayed, even though one has been configured.

</td></tr><tr><td>

Service Catalog Builder

 PRB2033565

</td><td>

A UI policy action created from Catalog Builder can't be seen in the platform

</td><td>

 

</td><td>

1.  Log in to Catalog Builder.
2.  Create a question on a catalog item.
3.  Create a UI policy and associate an action from the 'UI Policy' tab.
4.  Open the item in 'Edit in Advanced View' to get the item in the platform.
5.  Open the UI policy from the related list.
6.  Open the UI policy action.

 Notice that the variable name is empty, and the valid options are not seen on the right side.

</td></tr><tr><td>

Service Catalog Builder

 PRB2063629

</td><td>

The UI Policy action field message fields re-appear after variable selection in Catalog Builder

</td><td>

 

</td><td>

1.  Open the catalog item in the CB wizard.
2.  Navigate to **UI Policy** &gt; **Add behavior** &gt; **Actions** &gt; **Add action**.
3.  Select the **Plain Label/Rich Text Label/Container Start** variable.
4.  Wait 3 seconds for onChange.

 Expected behavior: The field message should not be displayed in the UI policy.

 Actual behavior: The fields re-appear after the policy refresh.

</td></tr><tr><td>

Service Catalog

 PRB1972924

</td><td>

The **Generate sequence** UI action gives a missing start rule error on Playbook 28.2.1

</td><td>

This issue was observed in Playbook 28.2.1, but not in 28.0.8.

</td><td>

1.  Open any order guide.
2.  Generate the sequence.
3.  Open the playbook created.

 Observe the missing start rule errors.

</td></tr><tr><td>

Service Catalog

 PRB2033096

</td><td>

Catalog redirection throws a 404 error page when accessed from the chat responses

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2040266

</td><td>

g\_form.clearValue should clear the value of the Lookup Select Box, even when there are no reference qualifiers

</td><td>

When loading the XML files, this creates Lookup Select Boxes. One file creates an item option named 'user\_group' under the 'AWS account request' catalog item, which is a is a Lookup Select Box that references the sys\_user\_group table and its reference qualifier is 'javascript: 'manager=' + current.variables.user'. Another file creates an item option named **User** under the 'AWS account request' catalog item, which is a Lookup Select Box that references the sys\_user table. The next file is a catalog script for the 'AWS account request' catalog item, which logs the value of the user\_group field when there is a change to the user field.

</td><td>

1.  Load the XML files.

Notice that these XML files create a item options named 'user\_group' and **User** under the 'AWS account request' catalog item, and that Lookup Select Boxes are created.

2.  Navigate to the catalog item.
3.  Change the **User** field to any value.

 Expected behavior: The**User Group** field should be cleared, and the alert should show an empty value.

 Actual behavior: The**User Group** field is cleared in the UI, but the alert shows the previous value.

</td></tr><tr><td>

Service Catalog

 PRB2070973

</td><td>

Add Now Assist AI-usage tracking fields and options to the catalog\_builder\_analytics table

</td><td>

Extend the catalog\_builder\_analytics table to support tracking of Now Assist AI usage during catalog building.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2073331

</td><td>

Family changes for AIX STP

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2073333

</td><td>

Family changes for the AIX catalog item form

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2084606

</td><td>

Family changes to support widgets introduced to the Service Catalog LUX Widgets Store app

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2089751

 [KB3159281](https://hi.service-now.com/kb_view.do?sysparm_article=KB3159281)

</td><td>

Catalog client scripts and UI policies are blocked on requested item \(RITM\)/sc\_task forms for users who can read the record

</td><td>

The resolver throws 'User doesn't have access to the item' and returns no catalog client scripts / UI policies, so none execute on the RITM/sc\_task form, even though the user can fully read the record. Users expect catalog client scripts and UI policies load and execute for any user who has read access to the RITM / sc\_task record. The catalog item User-Criteria entitlement \(canView\) should only gate the catalog ordering context \(sc\_cat\_item / sc\_cart\_item\), not fulfillment records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Variables

 PRB2072938

</td><td>

The 'Lists and Platform Analytics' visualization shows encrypted responses for record producer variables

</td><td>

The variables in the incident list view should show decrypted values. The issue occurs because the form and the list view retrieve the variable's value in two different ways.

</td><td>

1.  Create an encrypted field configuration on the question\_answer table and **Value** field.
2.  Define a module access policy based on the crypto module of type 'Role'.
3.  Set the target role as snc\_internal and the result as track.
4.  Create a record producer on the incident with one variable.
5.  Create an incident via the record producer.
6.  Add the record producer variable to the incident list view.
7.  Load incident.list.

 Expected behavior: The variables in the list view show decrypted values.

 Actual behavior: The variables in the list view show encrypted values.

</td></tr><tr><td>

Service Mapping

 PRB2052536

</td><td>

In Service Map, additional related list tabs \(Changes-current/past, Incident, Problem\) are permanently stuck on 'Loading...'

</td><td>

 

</td><td>

1.  Open any Operational Service in the 'Event Management' view.
2.  Add indicators.
3.  Select on the added tabs for the indicator.

 Notice that it's permanently stuck on 'Loading...'.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB1831844

</td><td>

Users are unable to convert a sys\_app-based application due to a company key

</td><td>

The user is unable to convert an app from an instance with the error, 'Not allowed to download application x\_taniu\_tan\_core. Check that you either have User with elevated privileges access or have added your company key \(for example, sn for ServiceNow\) to the sn\_appauthor. all\_company\_keys system property.'.

</td><td>

1.  Load an open source app from a third party using Studio.
2.  Verify that it can be seen.
3.  Edit the sys\_app based scope in the instance.
4.  Open SDK.
5.  Attempt to convert it.

 Observe the error message.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2041355

</td><td>

The sys\_gen\_ai\_feature\_mapping and sys\_gen\_ai\_strategy\_mapping records are silently dropped during Now Assist skill installation via Studio and BuildAgent

</td><td>

All records including feature mappings and strategy mappings should be installed successfully.

</td><td>

1.  Log in as an admin user.
2.  Open Servicenow Studio and Build Agent.
3.  Provide a prompt to create a Now Assist skill for any use case.
4.  Provide the necessary answers to the Build Agent.

Notice that the Build Agent will build and install the skill.

5.  Open thesys\_gen\_ai\_feature\_mappin and sys\_gen\_ai\_strategy\_mappin tables.

 Observe whether any records are created or not.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2060181

</td><td>

ListElementLoader reinserts records if the child elements has the action attribute as 'INSERT\_OR\_UPDATE'

</td><td>

 

</td><td>

1.  Create an application on the instance with the table and list metadata.
2.  Remove the list metadata.
3.  Export the app.
4.  Reinstall the application.

 Expected behavior: The app should be installed and the list metadata should still remain deleted.

 Actual behavior: The list gets re-inserted again.

</td></tr><tr><td>

ServiceNow Studio \(Family Channel\)

 PRB2063560

</td><td>

True up the Glider Store app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal Core Widgets

 PRB1953795

 [KB3153830](https://hi.service-now.com/kb_view.do?sysparm_article=KB3153830)

</td><td>

The **Subscribe to update** button doesn't work for non- admin users after a Zurich upgrade

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB2058602

</td><td>

Typing indicator no longer works

</td><td>

 

</td><td>

1.  Open two browsers.
2.  Log in as two different users.
3.  Create a sidebar chat for the two users.
4.  Start typing.

 Observe that there is no typing indicator.

</td></tr><tr><td>

Software Asset Core Company

 PRB2005158

</td><td>

Improve NDS guided setup and proactively fix core company reference jobs by batching through local implementation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2018383

 [KB2986694](https://hi.service-now.com/kb_view.do?sysparm_article=KB2986694)

</td><td>

A Microsoft per‑core license metric isn't visible after a Zurich or Australia upgrade

</td><td>

The MS per core metric was moved from the apply\_once folder to the update folder. The fix script to set the metric group was overwritten, since the update folder file insert ran after. Thus, the MS per core uploaded with no metric group.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB2073947

</td><td>

Create samp\_software\_filter and samp\_software\_custom\_filter tables in app-itam-sam for software junk filtering

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2080316

</td><td>

Generate a summary for the 'New Reclamation Candidates' job

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Publisher Pack for Oracle

 PRB2062263

</td><td>

The Oracle option extension for Windows not working with Oracle Wallet changes for Windows

</td><td>

 

</td><td>

1.  Create applicative credentials for the CI type 'cmdb\_ci\_db\_ora\_instance' for the Oracle instance to the ServiceNow instance.
2.  Identify if the discovery process is utilizing the applicative credentials stored on the ServiceNow instance or external credential vault.
3.  Execute the command on the target server.

 Observe that the User/Credential combo printed in plain text in the Windows server shell log is utilizing the Oracle SQL\*Plus utility.

</td></tr><tr><td>

Software Asset Normalization

 PRB1703274

</td><td>

Slow queries identified during OKR 2.3 executions on reconciliation, de-duplication and normalization scenarios

</td><td>

During executions, certain slow queries take a total of at least 1 minute in the case of normalization.

</td><td>

1.  Have a discovery model \(DM\) \(cmdb\_sam\_sw\_discovery\_model\) with a non-empty **Publisher** field and a display\_name that matches an existing samp\_package\_map rule created for the publisher-less \(Add-Remove / Windows registry\) hash.
2.  Run NormalizationEngine. normalize​Discovery​Model​Record\(\)​ on that DM.

 Expected behavior: The DM with a non-empty discovered publisher shouldn't match Add-Remove rules. The status should remain 'missed' \(no match found\).

 Actual behavior: The engine falls back to the Add-Remove scenario \(blanks out the publisher\) in \_findAMatch\(\) and incorrectly matches a normalization rule intended only for publisher-less registry entries. The DM is incorrectly normalized against the wrong rule, leading to inflated/duplicate license counts for browser-hosted components \(PWAs, browser extensions\).

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2005145

</td><td>

Few software installations records have 'Install Requiring action' with the reason as 'Undetermined' for Esxi

</td><td>

During Software Asset Management \(SAM\) reconciliation, when a vCenter has a device allocation to an entitlement, the system discovers all ESXi hosts under that vCenter by traversing the CMDB relationship chain: vCenter → Datacenter → Cluster → ESXi Host. It then collects all installs from these hosts and licenses them using the allocated rights. When iterating over multiple clusters within a data center, the list of discovered ESXi hosts is overwritten on each cluster iteration instead of being accumulated. This causes only the hosts from the last-processed cluster per datacenter to be retained — hosts from all earlier clusters are silently dropped and never considered for licensing.

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2060697

</td><td>

Potential savings display incorrectly on the License Metric Result of a product for which a low usage reclamation candidate is created

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2074587

</td><td>

Reclamation code changes for app-itam-sam

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2084351

</td><td>

Domain separation doesn't work on the summary and entity table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2086017

</td><td>

Create an AI Agent for AI Worker \(app-itam-sam\)

</td><td>

A new AI Agent should be created for the AI Worker. The implementation should follow the same pattern as the existing AI Agent. The user handover stages must be specific to the AI Worker autonomous flow.

</td><td>

 

</td></tr><tr><td>

Software Installation Deduplication

 PRB2068830

</td><td>

Each dedup UPDATE should carry at most BATCHSIZE sys\_ids, bu it carries the sum of the sys\_ids from 100 \_markActive calls, with no upper bound

</td><td>

The 'SAM - Deduplicate Install Table' scheduled job issues UPDATE statements against cmdb\_sam\_sw\_install \(SET deduplicated='1', active='1', primary\_install=NULL\). Most executions complete in roughly 200 milliseconds, but intermittently a single execution takes over 40 minutes and causes database impact. The code that produces this statement was written to cap each UPDATE at a fixed batch size, but the cap doesn't take effect. Each UPDATE can therefore carry an unbounded number of sys\_ids, which produces the intermittent long-running statements.

</td><td>

 

</td></tr><tr><td>

Software Lifecycles

 PRB2002670

</td><td>

The 'Software Lifecycle Report' job fails when a child product in 'Software Product Parent-Child Relationships' isn't installed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Source Control Engine

 PRB2054438

</td><td>

A re-link of a customized Store app to git via Source Control fails with an error code '1030'

</td><td>

The application should link to the git repository without the error code 1030 occurring.

</td><td>

1.  Provision two instances \(DC/TD\) with apprepo setup and at least 1 instance with midserver.
2.  Create an application in the instance.
3.  Publish that application.
4.  Now the instance with midserver, install the published application.
5.  Make a change in that application.
6.  Source control this application to git using a MID server.
7.  Delete the sys\_repo\_config for this application this will un-link the application from git.
8.  Attempt to link to the source control again to the same repository using a MID server.

 Expected behavior: The application smoothly links to the git repository.

 Actual behavior: The error code 1030 occurs.

</td></tr><tr><td>

Stream Connect Core

 PRB2019118

</td><td>

Generative AI logs are missing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Subscription Management

 PRB2072670

</td><td>

Add sn\_entitlement scope in Glide properties to enable sending data from Glide to valk-gateway service

</td><td>

To send the metered usage data from the user and central instance to valk gateway via REST API, the valk gateway URL is accessed, which gets populated in the sys\_service table via DISH. To do so, a scope should be added in glide.properties glide.services. rest.allowed\_services to allow sys\_service to be accessed from sn\_entitlement and sn\_entitlement\_ctr scopes.

</td><td>

 

</td></tr><tr><td>

System Archiving

 PRB2059055

 [KB3143594](https://hi.service-now.com/kb_view.do?sysparm_article=KB3143594)

</td><td>

The S3DelegatingClient. isConnectivityException\(\) infinite loop on multi-level exception cause chains and hangs scheduler worker threads

</td><td>

Any S3 operation through S3DelegatingClient whose thrown exception has a cause chain 2+ levels deep permanently hangs the handling scheduler worker thread, effectively removing that worker from the pool and stalling S3 offload jobs over time.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Events

 PRB2080045

</td><td>

Post-clone event-processing cleanup scripts \(201-204\) fail to run when a user script ahead of them errors out

</td><td>

The post-clone cleanup scripts Delete Processing Framework Triggers \(201\), Deduplicate Queues Post Clone \(202\), Deduplicate Queue Params Post Clone \(203\), and Re Provision Queues Post Clone \(204\) are failing to run. This occurs when a cleanup script at a lower order value errors during the clone. Since the clone cleanup runner stops entirely on the first failure, scripts 201-204 never execute. Event queues are left unprovisioned, backing up hundreds of thousands of events until the missing scripts are run manually via emergency change.

</td><td>

1.  Configure a custom clone\_cleanup\_script record with an order value lower than 204 that will throw an error during execution.
2.  Perform an instance clone.

 Observe that the clone cleanup runner halts on the failing custom script and never executes scripts 201-204 \(Delete Processing Framework Triggers, Deduplicate Queues Post Clone, Deduplicate Queue Params Post Clone, Re Provision Queues Post Clone\). Also, observe that sysevent\_queue\_config and sys\_processing\_framework\_job remain unprovisioned for most queues, and events accumulate in the 'Ready' state with no active workers.

</td></tr><tr><td>

System Web Services

 PRB2037370

</td><td>

Reading of multiple records using the UI/API Call/Processor/Script/Flow fails to track multiple READs in the Record Action metric

</td><td>

Four GlideRecord operation methods are instrumented to call RecordActionRecorder.record\(\) at the point of each operation. This is the entry point for all telemetry, and every record operation on an allowlisted table flows through here. The instrumentation pattern follows Glide​Record​Protected​Data​Recorder,​ which already instruments the same methods: a single static call, no branching, no impact on the existing operation path. query\(\) is added for READ instrumentation so that data access by external agents and the NOW UI can be measured alongside writes.

</td><td>

1.  Navigate to the incident table.
2.  View the list of incidents in the ServiceNow UI.

Observe that all of the rows are visible in the UI with multiple read metrics.

3.  Execute a Query Service Query to validate that multiple metrics have been recorded in the 'sn.​glide.​action\_​fabric.​record\_​action' metric.

 Expected behavior: Multiple reads are recorded.

 Actual behavior: One read is recorded.

</td></tr><tr><td>

System Web Services

 PRB2088200

</td><td>

True-up Telemetry Data Connector

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2088201

</td><td>

Platform security changes in action fabric

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2088202

</td><td>

In action fabric billing, support the linear CRUD multiplier model for metering

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2088205

</td><td>

Action fabric billing

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2088207

</td><td>

True-up the Action Fabric Usage Dashboard app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB2071772

</td><td>

There's repeated 'skipping business rule' errors on work order tasks

</td><td>

The error looks similar to the following: 'Condition 'Condition: current.state != 3 &amp;&amp; current.state != 4 &amp;&amp; current.state != 7 &amp;&amp; \(current.location.changes\(\) \|\| current.territory.changes\(\) \|\| current.​consider\_​ potential\_​territories\_​for \_​schedule\_​optimization.​ changes\(\)​\)​' in business rule 'Update Potential Territories for Task' on wm\_task: WOT0010001 evaluated to null; skipping business rule, when Schedule optimization plugin is not installed and territory planning is installed.'.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2059215

</td><td>

Azure classic trace collector doesn't consider Credential IDs for AI and ML services

</td><td>

AzureTraceCollector ignores credential IDs supplied as config update parameters. It only considers credential alias names.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2074229

</td><td>

Trace collector MID code for Google Cloud custom agents

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2081553

</td><td>

Convert app-domain-util app as a hosted plugin

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2090151

</td><td>

Netty 1.2.10 is at end-of-life

</td><td>

As recommended, upgrade Netty to 1.2.17 or newer.

</td><td>

 

</td></tr><tr><td>

Transaction Logs

 PRB2073987

</td><td>

Enable MCP server user-facing logging via the sys\_log table

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB2036507

</td><td>

Hopped-in users are logged out every 5 minutes because glide.guest.session\_timeout = 5 minutes

</td><td>

This happens because hopped-in users follow the glide.guest.session\_timeout property. PRB1985070 changed glide.guest.session\_timeout to 5 minutes, the inactive.timeout for hopped-in users shows as 300 in /xmlstats.do?include=sessions. Regular users logged into the instance are not affected by the change in PRB1985070. A hopped-in user shouldn't use the same property as guest sessions for timeout.

</td><td>

1.  Navigate to an instance.
2.  Change the property 'glide.guest.session\_timeout' = 5.
3.  Log out and hop in again.
4.  Navigate to /xmlstats.do?include=sessions.
5.  Look up the hopped-in user name.

 Notice inactive.timeout is set to the value of the 'glide.guest.session\_timeout' property.

</td></tr><tr><td>

UI Actions

 PRB2074979

</td><td>

GraphQL list UI actions are pulling UI actions that are list V3 compatible

</td><td>

The graphQL endpoint is pulling list UI actions that are list v3 compatible, thus creating duplicate list UI actions in the choice menu.

</td><td>

1.  Enable the 'Lit' list component to fetch UI actions for the 'Incident' table.
2.  Open the choice/menu of actions in the top right corner of the list.

 Note the duplicated list UI actions such as **Repair SLAs,** &gt; **Add to Visual Task Board**, and so on.

</td></tr><tr><td>

UI Actions

 PRB2084588

</td><td>

Visibility and executability should be configurable for a UI action

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB2084589

</td><td>

Handle session notifications when a page redirect occurs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB2084591

</td><td>

UI action condition evaluation should leverage virtual URIs for improved parity

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB2084593

</td><td>

Correct the behavior of server-side UI actions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB2084596

</td><td>

Support handling of redirect-based processors

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2073309

</td><td>

Convert all UI16 Dev - Controls components to Lit

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2073310

</td><td>

Support the **Markdown** field type in UI16, Seismic, and LIT

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2082758

</td><td>

Advanced Qualifier Reference is skipped when doing a list edit operation for a reference field

</td><td>

Note that Advanced Qualifier Reference is working fine on a form.

</td><td>

1.  On an incident table, set up advanced reference qualifier for the **Assigned to** field.
2.  On Service Operations Workspace, navigate to the 'Incident' list.
3.  Try to list edit the **Assigned to** field.
4.  Select the **look up** icon.

 Expected behavior: The Advanced Qualifier Reference should be applied.

 Actual behavior: The Advanced Qualifier Reference is skipped.

</td></tr><tr><td>

UI Form Administration

 PRB2084578

</td><td>

Glide changes to support form URL parameters and formatter support in UI26

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2084598

</td><td>

Glide changes to support the form context menu and system parameters in UI26

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB2016580

</td><td>

After upgrading instances from Zurich to Australia, several records show up on the skipped list belonging to the sn\_glider or sn\_build\_agent with the error 'Unable to compare, unable to find a current record'

</td><td>

After upgrading a Zurich instance to Australia, the upgrade monitor has a list of skipped records. When trying to resolve issues and compare to current, users observe the error: 'Unable to compare, unable to find a current record'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Upgrade Center

 PRB2076321

</td><td>

Apply defaults on the loading of XML records with apply\_defaults=true attribute

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

User Criteria for Service Catalog

 PRB2087796

</td><td>

Scripted user criteria might return stale results via AI Search and aren't cached durably for the Moveworks Search API

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1996624

</td><td>

Add-on events aren't caught when a page is used as a subpage

</td><td>

There's a subpage 'announcements', where when users select the card in 'Grid' mode, it works. But when the same subpage is embedded in another page, it doesn't work. On investigation, it was found that in the chain of events, the add-on event mapping on the target event 'Announcement ECAM action' doesn't get triggered.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2054946

</td><td>

Keyboard shortcut remapping for admins and users

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2057267

</td><td>

The session expiry modal displays inside the workspace iFrame

</td><td>

 

</td><td>

1.  Navigate to the Service Operations Workspace \(SOW\) list page.
2.  Open a tab and do logout.do.
3.  Navigate back to the SOW list page and wait for the session expiry modal to show.

 Expected behavior: Session expiry handling should show the session expiry modal.

 Actual behavior: The session expiry modal shows up inside the iFrame.

</td></tr><tr><td>

UX Framework

 PRB2060350

</td><td>

Metric tracking for remapping suggestions is missing in Zurich

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2084577

</td><td>

Product lab and action triggers in Survey Center

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2005164

</td><td>

Dynamic Translation in Virtual Agent is translating already translated text in catalog items

</td><td>

Dynamic Translation is translating already translated catalog item text in the Virtual Agent, causing unexpected phrasing for text that users have specifically set for a specific language.

</td><td>

1.  Create a conversational catalog item.
2.  Define a translation for one of the questions in another language via the 'Translated Text' table.
3.  Open the catalog item via Virtual Agent.

 Notice that once the question translated is presented, the exact phrasing used in the Translated Text isn't presented. This is due to the Dynamic Translation translating an already translated question.

</td></tr><tr><td>

Virtual Agent

 PRB2025952

</td><td>

The value of the of the **Shorten response** field on text nodes in Virtual Agent Designer can't be set globally or per topic

</td><td>

It has to be set manually by opening every single text node and selecting the checkbox.

</td><td>

1.  In a Virtual Agent Designer, open any topic that contains one or more text nodes.
2.  Open any text node.

 Note that the default value for the 'Shorten response' checkbox is false.

</td></tr><tr><td>

Virtual Agent

 PRB2031991

</td><td>

'Get details of problem agent' returns additional duplicate closure messages along with the expected closing message

</td><td>

When the user enters a closing utterance, the agent returns multiple closure messages, and the last two messages are duplicated.

</td><td>

1.  Open NAP.
2.  Enter an utterance like 'Help me get details of a problem'.

Observe that the agent returns a response like 'Could you please provide the problem number you'd like details for?'.

3.  Enter an utterance like 'See you later'.

 Expected behavior: The agent returns a response like 'Understood. Feel free to return anytime if you need help.'

 Actual behavior: Additional closure messages show up, and the last two messages are duplicated. For example, the agent might return the following: 'Understood. Feel free to return anytime if you need help. Thanks for chatting! I'll go ahead and close this conversation now. I'm here if you need anything else. It looks like you're finished with this chat, so I'll go ahead and close it. It looks like you're finished with this chat, so I'll go ahead and close it.'.

</td></tr><tr><td>

Virtual Agent

 PRB2035888

</td><td>

A Guardian-triggered async\_search early-return leaves a stale task ID in the context

</td><td>

The second utterance result becomes dropped.

</td><td>

1.  Send a prompt that Guardian flags.

Observe that it's displayed correctly. Also, observe that the first request is still active but times out later.

2.  Send a second utterance that triggers skill Discovery immediately.
3.  Wait for a timeout from the first message to occur to display a 'sorry' message in the conversation.

 Expected behavior: The second utterance responds normally.

 Actual behavior: 'Sorry, there was a problem on my side' appears. The second utterance result is dropped.

</td></tr><tr><td>

Virtual Agent

 PRB2037636

 [KB3108272](https://hi.service-now.com/kb_view.do?sysparm_article=KB3108272)

</td><td>

Agent messages containing URLs aren't displaying correctly in the internal transcript

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2052769

</td><td>

There's a 'sorry' message after a user tries to enter a different topic after a survey message

</td><td>

Users receive a 'sorry' error message when attempting to continue a conversation after the survey prompt appears, such as by asking a new question or creating an incident. The issue occurs because the survey handling logic incorrectly classifies non‑feedback responses, causing the survey to be re‑triggered and the conversation to terminate unexpectedly. This prevents users from completing their intended actions and causes the chat session to end unexpectedly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2056495

</td><td>

Central cache doesn't return the correct entry if the cache is updated from a different cluster

</td><td>

In the central cache log, the following message appears: 'Negative cache hit — Glide previously returned null for this key'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2058703

</td><td>

Generating a KB article throws an error

</td><td>

The following error appears: 'Configured callback URL for the KB generation topic is invalid: https:​/​/​nextwave-​preview-​internal-​c003.​aus100.​service-​now.​com'.​

</td><td>

1.  Create an instance, following the documentation for setting up NextWave instances.
2.  Navigate to now-assist-admin.
3.  Make sure the KB Generation skill is active and the display for NAP\(OTTO\) channel is active.
4.  Give the prompt 'Create the KB for INCXXXXXXX' or 'Generate KB article'.

 Observe that there are three potential outcomes. First, the AI output could be: 'I wasn't able to generate the KB article because the configured callback URL for the KB generation topic is invalid'.

 Second, the AI output could be: 'I'll help you create a knowledge article. Let me first retrieve the incident details to understand what information should be included in the KB'. Then the execution stops. It doesn't collect any information nor create any article. The error code is 200102.

 Finally, it might not use the KB Generation skill. Instead, it uses knowledge graph or basic reasoning to form a draft article in the NAP window.

</td></tr><tr><td>

Virtual Agent

 PRB2058728

</td><td>

Chat summary isn't generated on instances with the Spanish translation plugin

</td><td>

After ending a chat between a requester and an agent, the summary doesn't generate. This occurs when one person is using Spanish and the other is using English.

</td><td>

1.  Provision an instance with the Spanish translation plugin installed.
2.  Set Spanish as the language for the requester.
3.  Set English as the language for the agent.
4.  Make sure DT is enabled.
5.  As the requester, initiate a chat and connect with the agent.
6.  Exchange around 20 messages.
7.  As the requester, end the chat.

 Observe that the chat summary doesn't generate.

</td></tr><tr><td>

Virtual Agent

 PRB2059089

</td><td>

The Otto session isn't aware of the logged-in user for 'assets managed by me' queries

</td><td>

The Otto/AICT chat session isn't aware of the logged-in user by default. When a user asks a question like 'Can you give me the assets managed by me?', the assistant returns the complete/unfiltered list of assets instead of applying a managed\_by = current user filter. The filter is only applied when the user explicitly names themselves in the query. The assistant should recognize 'me'/'my' references and automatically apply the logged-in session user's context without requiring explicit clarification.

</td><td>

1.  Log in as an AICT user.
2.  Ask Otto: 'Can you give me the assets managed by me?'.

Observe that the full/unfiltered asset list is returned instead of being filtered to the current user.

3.  Ask explicitly by name, for example: 'assets managed by &lt;username&gt;'.

 Observe that the managed\_by = current user filter is correctly applied.

</td></tr><tr><td>

Virtual Agent

 PRB2059128

</td><td>

In Language Detection, the loaded choices remain in the wrong language after switching from English to French via the Conversational catalog

</td><td>

When Language Detection is enabled, it automatically switches the conversation language from English to French after receiving 'Bonjour'. The user observes that the reference variable choices and loaded values appear in the wrong language \(English\) instead of French.

</td><td>

1.  Configure NextWave-Conversation-Server with Language Detection enabled.
2.  Set the Topic Block and Agent Execution priority, with Agent Execution higher priority.
3.  Use a conversational catalog item with a 'reference' variable type.
4.  Start the chat in the English profile/session language.
5.  Send the message 'Bonjour' to trigger Language Detection.
6.  Verify that the chat language switches to French.
7.  Wait for the French question to load \(with reference variable choices\).

 Observe the loaded choices for the reference variable.

</td></tr><tr><td>

Virtual Agent

 PRB2059632

</td><td>

BuildPolicyConfig should be aligned with sys\_​now\_​assist\_​va\_​persona\_​detail schema

</td><td>

No policy configs are returned because buildPolicyConfig doesn't target sys\_​now\_​assist\_​va\_​persona\_​detail and doesn't filter by persona\_detail\_type = Policy.

</td><td>

1.  Create an active record in sys\_​now\_​assist\_​va\_​persona\_​detail:​
    -   Deployment = a valid deployment sys\_id.
    -   Persona\_detail\_type = Policy.
    -   Name = Test Policy.
    -   Description = Test policy description.
    -   Prompt\_value = Test policy instruction.
2.  For the same deployment, create another active persona-detail record with persona\_detail\_type = Tone and prompt\_value = Friendly.
3.  Trigger the assistant-config handshake for that deployment via next wave.
4.  Inspect policyConfigs in the response.

 Expected behavior: One policy config entry is returned, containing the sys\_id, name, description, active, and instruction from the policy persona-detail record. Non-policy persona-detail records are excluded.

 Actual behavior: No policy configs are returned because buildPolicyConfig doesn't target sys\_​now\_​assist\_​va\_​persona\_​detail and doesn't filter by persona\_detail\_type = Policy.

</td></tr><tr><td>

Virtual Agent

 PRB2060897

</td><td>

The 'promoted-skills' API doesn't return non-discoverable skills

</td><td>

 

</td><td>

1.  Create a skill.
2.  Call the 'promoted-skills' API.

 Expected behavior: The skill should be returned.

 Actual behavior: The skill isn't returned.

</td></tr><tr><td>

Virtual Agent

 PRB2061042

</td><td>

Fixes are needed for guest user support for OffGlide

</td><td>

Additional rest endpoints need a public role. The NextWave token needs to be turned on for bff exchange.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2063396

</td><td>

Parallel tools execution aren't running in record domain

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2063992

</td><td>

The user is unable to add a portal to the Conversational AI Assistant

</td><td>

When the user attempts to add the ESC portal to domain one, it is successful. However, when the user attempts to set up the assistant to domain two with Service Portal, it fails and the portal is not set. Errors don't occur in the UI, but when it goes to the next step 'Branding', it fails saying the portal is not set. Errors occur in the logs.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2064355

</td><td>

Auto Chat executions are faulted

</td><td>

There is an intermittent failure in fetching the JWT token from CS, which is causing the faulted conversations.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2064833

</td><td>

A domain is set to null after user input

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2066077

</td><td>

Add the reduce\_items\_list\_polling toggle

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2066110

</td><td>

When ending the conversation, it moves the interaction to a 'Closed Abandoned' state without starting the conversation after creating it using CREATE\_CONVERSATION

</td><td>

The interaction moves to a 'Closed Abandoned' state instead of a 'Closed Complete' state.

</td><td>

1.  Create a conversation using the CREATE\_CONVERSATION action.
2.  Pass the context variables live\_agent only to 'true'.
3.  End the conversation using the END\_CONVERSATION action without starting the conversation

 Expected behavior: The interaction must move to 'Closed Complete' state.

 Actual behavior: It is moving to a 'Closed Abandoned' state.

</td></tr><tr><td>

Virtual Agent

 PRB2066290

</td><td>

Execution plans aren't moving to 'In Progress'

</td><td>

AI Agent auto-linking was previously restricted to the AIA Background channel only. To support the ZTSD use cases, AI Agent auto-linking also needs to work for Auto Chat providers \(autochat / autochatnava inbound IDs\), which weren't covered by the existing gating.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2068417

</td><td>

When Dynamic Translation \(DT\) is turned on, it causes incorrect translations with markdown link syntax

</td><td>

Dynamic Translation \(DT\) breaks markdown links and images in Virtual Agent messages when translating to languages that use non-ASCII punctuation \(for example, Chinese, Japanese, Korean\). DT converts all ASCII punctuation to localized equivalents during translation. For example, in Chinese, parentheses \(\) become full-width （）. This is correct for plain text, but DT does not distinguish plain text from markdown syntax.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2073250

</td><td>

A conversation from another domain doesn't work if the user default domain doesn't have access to the current session domain

</td><td>

Whenever there is a hybrid queue into play, the worker impersonates the user and updates the session, but doesn't touch the domain. When impersonated normally, the domain will be the default domain for the user. This might no have access to the conversation because its started in a different domain. So whenever we read some data that is not accessible like conversation, the flow fails.

</td><td>

1.  Enable domain seperation.
2.  Update any field on a user record.

Once updated, the default domain to the user moves to TOP/Default unless specified.

3.  Switch the domain to a different domain \(some sibling domain or a parent domain\).
4.  Start the conversation.

 Observe the responses would not be received for any query.

</td></tr><tr><td>

Virtual Agent

 PRB2076609

</td><td>

The 'Timeout conversations' job fails to close conversations on cross domains

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2078678

</td><td>

The dynamic loading 'Processing new information' progress message is not translated in localized Now Assist Virtual Agent \(NAVA\) conversations

</td><td>

Even though the values are translated in Spanish when the user opens 'Testing \(En pruebas\)' in the AI Agent Studio \(Estudio de agentes de IA\), the message 'Processing new information' remains in English and is not translated to Spanish.

</td><td>

1.  Set up Dynamic Translation.
2.  Change the language to Spanish.
3.  Navigate to **AI Agent Studio \(Estudio de agentes de IA\)** &gt; **Testing \(En pruebas\)**.
4.  Observe the following values that are translated:
    -   Choose a test type AI agent or workflow \(Elegir un tipo de prueba\): Agente de IA o Flujo de trabajo
    -   Name of the AI Agent or agentic workflow \(Nombre del agente de IA o flujo de trabajo agéntico\): Agente de IA de categorizar incidentes de ITSM
    -   Version: 1 - V1 \(activo\)
    -   Task: INC0009009
5.  Select **Continuar para probar la respuesta del chat**.
6.  Watch the dynamic loading messages.

 Expected behavior: The user sees 'Processing new information' translated in Spanish, 'Procesando nueva información'.

 Actual behavior: The English text 'Processing new information' displays and is not translated to Spanish.

</td></tr><tr><td>

Virtual Agent

 PRB2078683

</td><td>

The Topic execution is not working if the Nextwave user is in the TOP/Default scope

</td><td>

 

</td><td>

1.  Enable domain separation.
2.  Check the Nextwave service user domain.
3.  Make any update on the user if needed so that the domain gets changed to TOP/Default.
4.  Start a conversation and run a topic.

 Observe that it fails.

</td></tr><tr><td>

Virtual Agent

 PRB2084118

</td><td>

setCache is not honoring domain field

</td><td>

setCache is not honoring the domain field when impersonating the actual user.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2085859

</td><td>

The Prompt Library 'Topics' tab is empty because the visible skills API returns '404' for every deployment

</td><td>

When the Prompt Library is enabled on a Now Assist Panel deployment, the 'Topics' tab doesn't load any prompts. The other Prompt Library tabs are unaffected. Users expect that the 'Topics' tab lists the topics configured and marked visible for that deployment. However, the tab displays no content. The API that supplies visible skills for a deployment reports that no skills were found, even when topics and skills are configured and marked visible. Thus, the 'Topics' tab can't be used on any deployment, and there's no configuration change that corrects it.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2086482

</td><td>

Off Glide branding API returns the menu item with the type as null

</td><td>

The API returns the 'Contact Live Agent' item with the type as 'null', even though the actual type is 'chat'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2087473

</td><td>

Bring the tone/persona sys-prop at the assistant level and append the agent\_persona instruction to it

</td><td>

If the config attribute isn't 'agent persona', the system appends the agent persona to the prompt if it exists. If the attribute is 'agent persona', it uses the persona or a static fallback if empty.

</td><td>

1.  Bring the sys-prop 'sn\_​nowassist\_​va.​assistant\_​personalization' to the Now Assist deployment config table.
2.  Make the setting available at the assistant level.
3.  Append the **Agent\_persona** field in the Now Assist deployment config table to tone/persona prompt.

 Observe that, when the config attribute isn't 'agent persona', the system appends the agent persona to the prompt if it exists. If the attribute is 'agent persona', it uses the persona or a static fallback if empty.

</td></tr><tr><td>

Virtual Agent

 PRB2091490

</td><td>

Glide to OGCS requests should set X-Instance-URL header with canonical URL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2092748

</td><td>

Live agent availability doesn't work once the user selects the **Cancel** button

</td><td>

It shows that no agents are available, even after the user selects the **Cancel** button and the live agent availability should resume.

</td><td>

1.  Start a chat as requestor from the /esc portal.
2.  Have an agent online from another browser.
3.  Connect to a live agent.
4.  Select the **Cancel** button and do not accept the workitem.
5.  Try connecting to the agent again.

 Expected behavior: The live agent transfer should stop just for that interaction when**Cancel** is selected and the live agent availability should start resuming after.

 Actual behavior: Notice that even when the agent is available, it shows that no agents are available. This happens for all the new conversations.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2014619

</td><td>

Selecting an in-line citation link in output text control takes the user to live agent fallback

</td><td>

 

</td><td>

1.  Ensure that there's a result that has only one output \(topic\), so that it auto starts and has an inline citation link in the output text message.
2.  When the topic is auto-starting post-search, select the in-line link

 When topic auto starts, the link should be turned off, but it isn't.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2077685

</td><td>

Conversations are created in the user's default domain instead of the one they are working in

</td><td>

On an instance with domain separation enabled, starting a Now Assist conversation creates it in the user's default domain rather than the domain they are currently working in. A user who switches domains and starts a conversation can have it created against the wrong domain. Work done in that conversation then runs with the visibility of the wrong domain. This affects Now Assist across the Service Portal, the Unified Navigation panel, and the Agent workspace. Instances without domain separation are unaffected.

</td><td>

1.  Open an instance with the domain separation plugin installed for the workstream.
2.  Ensure the domain hierarchy has at least a parent and one child domain, and a user with domain picker access.
3.  Sign in and confirm the domain picker is available.
4.  Switch to a non-default domain.
5.  Open Now Assist.
6.  Start a new conversation
7.  Inspect the domain the conversation record was created in.

 Expected behavior: The correct domain is selected.

 Actual behavior: The user's default domain is selected.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2082757

</td><td>

After closing the authorization window, a success event is returned even though the user did not authorize

</td><td>

 

</td><td>

1.  Configure MCP/A2A agent.
2.  During the conversation, the authentication widget displays.
3.  Select **Authenticate**.
4.  Close the window without authenticating.

 Expected behavior: It sends a failure event.

 Actual behavior: It sends a success event, due to which it shows as successful.

</td></tr><tr><td>

Visual Task Boards

 PRB2059581

</td><td>

Users are unable to move a card from one visual task board \(VTB\) to another after an Australia upgrade

</td><td>

The 'Move' dialog does not display any swimlanes.

</td><td>

1.  Set the system property glide.​invalid\_​query.​returns\_​no\_​rows to 'true'.
2.  Create two Task Boards:
    -   Board A with at least one card
    -   Board B with two or more lanes
3.  Open a card on Board A and select **Move**.
4.  In the dialog, select **Board B** as the target Task Board.
5.  Select the **Lane** field and search.

 Observe that the drop-down list displays 'No matches found', even though Board B has valid lanes.

</td></tr><tr><td>

Window Manager

 PRB2071474

</td><td>

Pin/Unpin doesn't work when Now Assist chat is in auto-triggered in fullscreen mode \(13' / short-viewport displays\) and in the 'Enter' modal

</td><td>

 

</td><td>

Open the chat in full screen mode.

 In full screen mode, the pin/unpin doesn't work and won't dock the chat. When the 'Enter' modal and pinned, it goes back to full screen mode instead of docking the chat.

</td></tr><tr><td>

Work Order Management

 PRB2084523

</td><td>

The work order rollup fails because the agent doesn't close the sn\_doc\_task

</td><td>

FSMMobile​Util.​is​Workordertasks​Closed \(com.snc.work\_management\) passes the work order's GlideRecord object directly into the GlideAggregate parent query instead of its sys\_id. This causes the open-task check to always evaluate as 'No open tasks' and lets the **Preview** button create a doc task prematurely. The doc task is left open and blocks the work order rollup.

</td><td>

 

</td></tr><tr><td>

Zero Trust Access

 PRB2052933

</td><td>

Users are unable to maintain session roles when accessing the visual task board \(VTB\) dashboard

</td><td>

This issue occurs when an instance has Zero Trust Access \(ZTA\) policies configured with IDP Attributes filter condition used in the Adaptive Authentication policy condition, for any user who access the VTB dashboard with the filter, filter​LIKEjavascript^ORfilter​LIKEDYNAMIC',​ and if there is no channel responder record created for it yet. The flow receives an NPE \(NullPointerException\), and the roles in the session are not loaded properly. There are no roles for the user causing the user to see the 'Security Restricts Access Prevention' message on screen.

</td><td>

1.  Ensure the instance has ZTA configured with at least one active Adaptive Authentication policy.
2.  Log in to the instance as any non-admin user.
3.  Navigate to any VTB dashboard that contains a board filter matching.
4.  Confirm that no channel responder record exists for this filter combination.
5.  Load/open the VTB dashboard.

 Notice the 'Security Restricts Access Prevention' message occurs.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 12m W40](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3220899)
-   [Zurich Patch 12m W39](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3159455)
-   [Zurich Patch 12m W38](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3157848)
-   [Zurich Patch 12m W37](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3156077)
-   [Zurich Patch 12 W40](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3220898)
-   Zurich Patch 12 W39 Hotfix 1
-   [Zurich Patch 12 W39](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3159454)
-   [Zurich Patch 12 W38](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3157847)
-   [Zurich Patch 12 W37](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3156075)
-   [Zurich Patch 12 W36](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3154013)
-   [Zurich Patch 12 W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152171)
-   [Zurich Patch 12 W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150679)
-   [Zurich Patch 12 W33 Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12-W33-hf-1-PO.md)
-   [Zurich Patch 12 W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147948)
-   [Zurich Patch 12](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-12.md)
-   [Zurich Patch 11 Hotfix 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11-hf-6-PO.md)
-   [Zurich Patch 11 Hotfix 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11-hf-5-PO.md)
-   [Zurich Patch 11 Hotfix 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11-hf-4-PO.md)
-   [Zurich Patch 11 Hotfix 3 W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152175)
-   [Zurich Patch 11 Hotfix 3 W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150682)
-   [Zurich Patch 11 Hotfix 3 W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3148136)
-   [Zurich Patch 11 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146433)
-   [Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)
-   [Zurich Patch 10 Hotfix 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10-hf-8-PO.md)
-   [Zurich Patch 10 Hotfix 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10-hf-7-PO.md)
-   [Zurich Patch 10 Hotfix 5b W38](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10-hf-5b-w38-PO.md)
-   [Zurich Patch 10 Hotfix 5 W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152176)
-   [Zurich Patch 10 Hotfix 5 W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150683)
-   [Zurich Patch 10 Hotfix 5 W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147947)
-   [Zurich Patch 10 Hotfix 5 W32](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146427)
-   [Zurich Patch 10 Hotfix 4b W40](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3220901)
-   [Zurich Patch 10 Hotfix 4b W39](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3159456)
-   [Zurich Patch 10 Hotfix 4b W38](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3157849)
-   [Zurich Patch 10 Hotfix 4b W37](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3156079)
-   [Zurich Patch 10 Hotfix 4b W36](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3154016)
-   [Zurich Patch 10 Hotfix 4b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152184)
-   [Zurich Patch 10 Hotfix 4a W38](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3157850)
-   [Zurich Patch 10 Hotfix 4a W37](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3156078)
-   [Zurich Patch 10 Hotfix 4a W36](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3154017)
-   [Zurich Patch 10 Hotfix 4a W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152177)
-   [Zurich Patch 10 Hotfix 4a W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150684)
-   [Zurich Patch 10 Hotfix 4a W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147946)
-   [Zurich Patch 10 Hotfix 4a W32](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146429)
-   [Zurich Patch 10 Hotfix 3b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147883)
-   [Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)
-   [Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)
-   [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)
-   [Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)


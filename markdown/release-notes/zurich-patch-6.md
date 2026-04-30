---
title: Zurich Patch 6
description: The Zurich Patch 6 release contains important problem fixes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-02-05"
reading_time_minutes: 62
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 6

The Zurich Patch 6 release contains important problem fixes.

-   **Zurich Patch 6 was released on February 5, 2026.**
    -   Build date: 02-02-2026\_1554
    -   Build tag: glide-zurich-07-01-2025\_\_patch6-01-16-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z06.00.xlsx).

## Overview

Zurich Patch 6 includes 237 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-zp6.png "Top 10 problem categories")

## Security-related fixes

Zurich Patch 6 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 6, refer to [KB2713103](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2713103).

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

Analytics Export API

 PRB1950794

</td><td>

An admin is no longer able to edit fields from 'Scheduled Email of Reports' \(sysauto\_report\) in Zurich

</td><td>

An admin is no longer able to edit fields from 'Scheduled Email of Reports' \(sysauto\_report\) in Zurich, impacting sysauto\_report.address\_list, sysauto\_report.group\_list, and sysauto\_report.user\_list.

</td><td>

Open any sysauto\_report in Zurich as an admin.

 Observe that the following fields are read-only: **Users**, **Groups**, and **Email addresses**.

</td></tr><tr><td>

CMDB Query Builder

 PRB1952766

 [KB2634786](https://hi.service-now.com/kb_view.do?sysparm_article=KB2634786)

</td><td>

Calls to QueryBuilder from ServiceMapping return no results when executing in the new V2 mode

</td><td>

In Zurich, processes that call into Query Builder can have no results returned. There are two scenarios where this occurs. Firstly, a service CI populated via CMDB Group containing a saved query \(as constructed in Query Builder\) can have no 'svc\_ci\_assoc' records, even when rerunning the service population. However, the expected CIs will appear when viewing the CMDB Group or the saved query directly. Secondly, instances configured to use 'Zing' for Global Search don't return any CI records in the findings. These different methods both rely on the 'CMDBGroup' API, which may not return results of query execution when using the 'v2' execution mode introduced in Zurich. Instances are at risk if they use dynamic CI groups which are built using Query Builder, they're on an impacted Zurich Version, and the system property glide.cmdb. query.execution \_mode = 'v2'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Email Notifications

 PRB1951516

</td><td>

When using email client, drag and drop functionality isn't including an attachment on sending

</td><td>

In the current UI16 email client, users can add attachments using the paper-clip icon or by dragging and dropping files into the email body. However, drag-and-drop doesn't work outside the email body because a background field was not properly defined, which causes this limitation.

</td><td>

1.  Log in to a Zurich instance.
2.  Navigate to the incident.list.
3.  Open Email Client.
4.  Drag and drop an attachment.

 When an email is sent, see the attachment isn't included. When users manually add the attachment, it's being added in to the email and is being sent.

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

Key Management Framework \(KMF\)

 PRB1944097

 [KB2654904](https://hi.service-now.com/kb_view.do?sysparm_article=KB2654904)

</td><td>

Users are unable to upload push certificates into the sys\_certificate table

</td><td>

An error is thrown.

</td><td>

Refer to the listed KB article for details.

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

Access Control

 PRB1966968

</td><td>

ScriptingGovernanceUtils does not correctly create sys\_user\_has\_role records for the snc\_required \_script\_writer \_permission based on the legacy/V1 or V2 Role Management mechanisms

</td><td>

In Zurich, a 'Conditional Script Writer' group has been introduced and this group has the single role 'snc\_required \_script\_writer \_permission'. Users are added to this group automatically by a scheduled job during the Zurich upgrade. This is done by inserting records into sys\_user\_grmember and sys\_user\_has\_role to create this relationship. The ServiceNow platform has two currently different ways of tracking the roles in the sys\_user\_has\_role table: Legacy/V1 Role Management and Role Management V2. V2 introduced the concept of inheritance counts with the goal of reducing the overall size and complexity of the sys\_user\_has\_role table, with the benefit of reducing the amount of time performing large roles changes could take. With the legacy mechanism the three fields **granted\_by**, **included\_in\_role** and **included\_in\_role** instance record where a role was inherited from and need to be correctly set. If a user is a member of the 'Conditional Script Writer' group, and therefore they inherit the 'snc\_required\_script\_writer\_permission' role, then the sys\_user\_has\_role record must have the **granted\_by** field set to the sys\_id of the 'Conditional Script Writer' group. Without this, the 'Group Member Delete' business rule on sys\_user\_grmember is unable to delete the sys\_user\_has\_role record if the user is removed from the group.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1973866

</td><td>

When showEmailMiniCompose = ON\_EMAIL\_ACTION, users can't reply to an email more than once

</td><td>

 

</td><td>

1.  Select the **ALL** menu.
2.  Type 'sys\_aw\_master\_config.list'.
3.  Open the 'Agent Workspace' row.
4.  Check the 'Active' checkbox.
5.  In the browser URL bar, type '/workspace' after the instance URL.
6.  On the record page, use the declarative action to compose a new email and send it.
7.  On the instance, navigate to 'sys\_email.list' and find the email just sent to switch the status to 'Sent'.
8.  On the record page, select **Reply** on the activity stream tile for the email sent.
9.  An email tab appears in 'compose'; fill it out and send it.

Once it is sent, the 'Email' tab disappears.

10. Select reply on the same email tile as before.
11. The email tab should appear again; fill out the email and select **Send**.

 Expected behavior: Users should be able to send another reply if they already sent the previous one. If they have not sent it, then selecting the **Reply** in the tile doesn't do anything.

 Actual behavior: When selecting **Reply**, it is loading the previously sent reply draft. Selecting **Send** gets a error saying that the draft was previously sent.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1959522

</td><td>

Agents are able to send messages even after a conversation is closed

</td><td>

The chat summary includes details about a chat closure message that's not present in the transcript.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1978194

</td><td>

There's empty bubbles on Agent Workspace due to an empty payload in Agent Chat

</td><td>

 

</td><td>

1.  Navigate to OG requester.
2.  Have some conversation going on.
3.  Connect to a live agent.
4.  Log in as an agent in the instance mentioned.

Notice empty bubbles on Agent Workspace.

5.  Navigate to sys\_cs\_message.

Notice that there are empty payloads in the conversation.


</td></tr><tr><td>

Agile Development

 PRB1968771

</td><td>

/sn\_safe\_$ safe\_board.do\#/teamBacklog is broken

</td><td>

Loading different PIs in the SAFe team backlog board in Zurich isn't working. The data in the board doesn't always change and can take multiple tries to change the PI on the board.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1969245

</td><td>

sn\_aia\_tools \_execution displays an empty tools value but the value exists in the XML

</td><td>

sn\_aia\_tools \_execution tools column is referencing sn\_aia\_agent \_tool\_m2m but the value is set from the sn\_aia\_ agent\_tool table.

</td><td>

1.  Execute an agentic workflow.
2.  Navigate to the sn\_aia\_ execution\_plan.
3.  Navigate to the 'Tools' execution tab.

 Notice that all the tools records are empty. However, open one and show XML that there is a value.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1975174

</td><td>

Agentic Evaluation isn't working for the 'Support Renewals Expansion Agentic' workflow

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1975798

</td><td>

Glide fixes to JSON return type in AIAToolDataPillUtil

</td><td>

 

</td><td>

1.  Ensure that 'capability' text is within the value field apart of the sn\_aia. supported\_ tools sys prop.
2.  Create or find a skill tool that takes JSON as input.
3.  Apply that skill to a tool and then add to an agent.
4.  Run the agent in the playground and observe the execution log on the right hand side.

 Expected behavior: Users should see the actual JSON as an input for the skill tool.

 Actual behavior: The input is blank, causing the agent to fail.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1981261

</td><td>

Make agent and tool columns non-mandatory in sn\_aia\_agent \_tool\_m2m and fix the empty cacheconfig name issue

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB1982032

</td><td>

'Extend session' functionality issue

</td><td>

The 'Extend session' functionality should work the same as the platform.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1971388

</td><td>

IngestableDocument. getObjectSize isn't counting fEmbeddedDocuments

</td><td>

Indexing the document/table causes out of memory errors.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1975413

</td><td>

AI Search Dynamic filters extension point impl isn't triggered from a non-global scope

</td><td>

When an AI Search scriptable API provided is executed from both global and sn\_nb\_action scopes, the extension point implementation doesn't get triggered when the scope is not global \(sn\_nb\_action\).

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1980531

</td><td>

Issue in RAG response for external content \(connector-specific fields and missing chunk structure\)

</td><td>

The external document results should be grouped under 'ragResponse.external\_document' \(instead of using the connector table name as the top-level key\). Also, each external document must include a chunks list. Finally, the **table** field should identify the connector/schema name \(for example, 'sn\_ext\_conn \_spo\_external\_ search\_schema'\).

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1981323

</td><td>

Removing the m2m tool xml for RAG, Reranker, WebSearch for Perplexity that shall be migrated to the nowassist-ai-agent repo

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1982327

</td><td>

The RAG tool returns documents that shouldn't be included in a search source

</td><td>

Users get duplicate articles for some queries.

</td><td>

 

</td></tr><tr><td>

AI Search for Service Portal

 PRB1942272

 [KB2608116](https://hi.service-now.com/kb_view.do?sysparm_article=KB2608116)

</td><td>

Users are unable to select multiple facets even when 'multi select or' is selected in facet settings

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search for Service Portal

 PRB1956814

</td><td>

Pressing the 'Enter' key doesn't open the link

</td><td>

When the tab focus is on the link and the 'Enter' key is pressed, the link doesn't open. However, if the user presses the 'Tab' key, the focus moves to hidden and pressing 'Enter' opens the link.

</td><td>

1.  Open any base instance with AI search enabled.
2.  Navigate to the Service portal.
3.  Navigate to the **Search edit** field.
4.  Search for 'email'.
5.  Navigate to the search results.
6.  Select a filter.
7.  Navigate to any links in the 'Results' section.
8.  Press the 'Enter' key to select.
9.  Verify whether it opens.

 Expected behavior: The tab focus is on the link, and pressing the 'Enter' key opens it. Pressing the 'Tab' key moves the focus to the next interactive element.

 Actual behavior: When the tab focus is on the link and the 'Enter' key is pressed, the link doesn't open. However, if the user presses the 'Tab' key, the focus moves to hidden and pressing 'Enter' opens the link.

</td></tr><tr><td>

AI Search for Virtual Agent

 PRB1945491

</td><td>

Tags should be passed as 'Array of Strings' not 'String'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1962691

</td><td>

AI Search doesn't populate sys\_search\_ source\_event with sources that weren't returned

</td><td>

 

</td><td>

1.  Enable AI Search for a portal.
2.  Search for a query that doesn't return documents from a search source.

 Observe that only the tables from search results that were returned were added to sys\_search\_source\_event.

</td></tr><tr><td>

AI Search UX

 PRB1978161

</td><td>

Replace the sparkle icon with the lens icon and updated specs in the workspace search

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1982272

</td><td>

There's a missing configuration for RAG popular search suggestions

</td><td>

This limits the ability for the suggestion type to be used, as the sys\_suggestion\_reader entry would need to be shipped in a store app or created by background script, neither of which is ideal.

</td><td>

1.  On an AI Search enabled instance, open the list view for the sys\_suggestion\_reader table.
2.  Check for an entry for RAG Popular Queries \(e.g. Type = RAG\_POPULAR\_QUERY\).

 Expected behavior: There is an entry.

 Actual behavior: There isn't an entry, and no **New** button to create one.

</td></tr><tr><td>

Analytics Data API

 PRB1937286

</td><td>

When a visualization acts as filter, another visualization isn't filtered for the first time

</td><td>

 

</td><td>

1.  Create a dashboard.
2.  Add 2 visualizations:
    -   Horizontal bar on incident table, grouped by active, and acting as a filter.
    -   Single score on an incident table and follow filters.
3.  Save the dashboard.
4.  Exit the editing mode.
5.  Select on a bar \(true\) on the bar visualization.

Notice that the single score doesn't reflect with the changes.

6.  Select another bar \(false\).

 Notice that the single score reflects the changes.

</td></tr><tr><td>

Analytics Export API

 PRB1977069

</td><td>

Users are unable to schedule data visualizations

</td><td>

 

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

 PRB1981044

 [KB2719949](https://hi.service-now.com/kb_view.do?sysparm_article=KB2719949)

</td><td>

The latest version in the sys\_store\_app table is updated to the installed version after an install, thereby causing the **Upgrade** button to be unavailable in App Manager

</td><td>

Two functions \(\_fixLatestVersion ForWithdrawn InstalledApps, \_fixLatestVersion ForWithdrawn InstalledCustomizations\) in Application Manager's UpdateChecker.checkAvailableUpdates API \(aka Sync in the UI\) were missing a required GlideRecord.addQuery constraint when the 'sn\_appclient. enable\_app\_manager \_checksums\_cache' sys\_property was set to true \(default\). This regression led to the latest\_version being set to the incorrect values on Install/Sync.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Appointment Booking

 PRB1940645

</td><td>

If users load appointment booking on a portal home page and then use the Service Portal \(SP\) date picker in a different portal page, the datepicker won't be clickable until a page reload

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Appointment Booking

 PRB1973793

</td><td>

Blackout schedule isn't honored

</td><td>

Users are able to book an appointment during the blackout schedule period.

</td><td>

1.  Impersonate a user.
2.  Navigate to the 'Credentials' page.
3.  Select **Fingerprinting**.
4.  From the location drop-down list, select **San Diego - Linda Vista Campus**.
5.  Answer the question 'What is your reason for visiting?' with 'Fingerprinting'.
6.  Select the **calendar** icon next to Appointment.

 Notice that appointment slots are available during the blackout schedule \(for example, December 31st\).

</td></tr><tr><td>

Asset Management

 PRB1968544

</td><td>

Assets which were created aren't displaying in 'Create Asset' on the Agent Mobile app

</td><td>

 

</td><td>

1.  Navigate to the Agent Mobile app.
2.  Navigate to **Asset** &gt; **Create Asset**.
3.  Select **Submit**.
4.  Select the 3 dots menu on the list.
5.  Select the **Create Asset** function.
6.  Fill all the fields and submit.

The asset gets created.

7.  Select **Create Asset**.
8.  Enter the asset tag or serial number for the created Asset.

 Expected behavior: An asset which gets created should be visible.

 Actual behavior: An asset which gets created isn't displaying.

</td></tr><tr><td>

Authentication

 PRB1927594

 [KB2423799](https://hi.service-now.com/kb_view.do?sysparm_article=KB2423799)

</td><td>

Oauth token calls fail from an API authenticated sessions

</td><td>

As part of multi-factor authentication enforcement for local internal user logins, adaptive authentication is enabled and configured the MFA context policy. Once an API authenticated session is established, it's expected to make only API integration \(or non-interactive\) related calls, and the '/oauth\_token.do' call falls outside of integration calls.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1960277

</td><td>

An Supplier Lifecycle Operations \(SLO\) error displays when the SLO URL is empty in Identity Provider \(IdP\) configuration

</td><td>

When the SLO \(single logout\) URL field is left empty in the IdP configuration, the system redirects to external\_logout\_complete with an error code slo\_error. However, this behavior is incorrect. Since SLO is optional, the absence of an SLO URL shouldn't trigger an error. This issue also appears in mobile.

</td><td>

1.  Navigate to the 'IdP Configuration' page.
2.  Ensure that the SLO URL is left empty.
3.  Log in using the configured IdP.
4.  Log out.

 Expected behavior: The system should successfully log out and redirect to the external\_logout\_complete page without any error code, since SLO is optional.

 Actual behavior: The system redirects to external\_logout\_complete with error code slo\_error, implying a failure even though SLO wasn't configured.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1978271

</td><td>

Remove metadata tracing valid transaction filtering

</td><td>

In SpanJob, remove validTransaction filtering. Since tracing doesn't allow transactions not related to metadata tracing to be traced, this is a redundant functionality. This is causing Builder Agent not to work with Zurich Glide properly. Filtering should be removed and add a new one that filters out all metadata not containing testResultId. This line in code is misleading and might cause issues in metadata tracing entries persistence in future.

</td><td>

1.  Create sys\_trace\_config entry.
2.  Set atf\_context cookie.
3.  Navigate to incident\_list.do.
4.  In another browser, without the cookie set, confirm no trace records are produced in sys\_traced\_metadata.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1963168

</td><td>

The HRSD Knowledge Graph is unavailable after an upgrade

</td><td>

There's an issue with the Now Assist Knowledge graph. The user receives the error 'An unexpected error occurred. Please try again.'

</td><td>

1.  Impersonate a user who has access to the HR Portal.
2.  Navigate to the HR Portal: https://&lt;instance&gt;.service-now.com/hr.
3.  Initiate a Virtual Agent Chat.
4.  Enter the prompt: 'Show me my open HR cases'.

 Expected behavior: Information about the users's open HR Cases is displayed.

 Actual behavior: The user receives the error 'An unexpected error occurred. Please try again.'

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1965782

</td><td>

RCA created during case summarization / resolution notes generation

</td><td>

RCAs are generated when modifying any fields in an HR case and its child tables, which causes test failures.

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB1973038

</td><td>

Industry case count usage for TPSM, TMT, HCLS, MCO, FSO, Retail and CSM entitlements

</td><td>

Count of cases that are not extended from one of the industry base cases an have industry entitlements. The count needs to be as of yesterday and run daily. This need to per industry and count of cases should be grouped by case type.

</td><td>

 

</td></tr><tr><td>

CMDB Data Manager

 PRB1943938

</td><td>

The Data Manager policy jobs experience has increasing slowness creating tasks when processing large data sets

</td><td>

The CMDB Data Manager policy for running jobs keep running for a long time because the underlying SQL query has pattern of LIMIT and OFFSET on the CMDB table. The table has a lot of data, and thus those SQL queries start showing increased execution time, effectively slowing the job running them.

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

Configuration Management Database \(CMDB\)

 PRB1894727

</td><td>

Duplicate approvals are created for the same users for CMDB Data manager tasks while in the 'Requested' state

</td><td>

This issue shows up when there are multiple archive policies generating each at least one task. It might be applicable for retire or delete policies too.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1909893

</td><td>

The 'Run' filter can apply an old condition and not pick up the newly applied filter conditions

</td><td>

In the CMDB Relationship editor, the filter can apply old conditions and not pick up the newly applied filter conditions. This is issue isn't consistently reproducible but there's a problematic API call made.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1969483

</td><td>

The 'CMDB Group Health' dashboard displays incorrect totals for parent metrics

</td><td>

In the CMDB Health Dashboard, users can experience incorrect totals for parent metrics when they have different health inclusion rules on the submetrics, which can even show negative percentages.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1829096

</td><td>

There's an incorrect timeref display value for ISO week 53

</td><td>

It's cosmetic, as only the axis labels are affected and the real values are preserved.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1924708

</td><td>

'Show Matching' a list and ordering by **ref\_** fields throws a NPE

</td><td>

After the user orders the list, the records disappear.

</td><td>

1.  Navigate to task.list.
2.  Open **Configure** &gt; **List Layout**.
3.  Add the planned start date \[change request\] to the list of columns.
4.  Save.
5.  Add watch list to the view.
6.  Populate the watch list of some records.
7.  'Show Match' the watch list.
8.  Order by the planned start date \[change request\].

 Expected behavior: The records show.

 Actual behavior: The records disappear.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1968109

</td><td>

When glide.db.aggregate .groupby\_display \_optimize is true, the group by reference fields display value is a sys\_id

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1968921

</td><td>

Count\(\*\) throws an exception for Workflow Data Fabric tables

</td><td>

It works fine with Glide tables.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1889276

</td><td>

deleteMultiple fails for PG for IN conditions larger than 1000

</td><td>

A NullPointerException is thrown: 'Exception attempting to delete from: u\_cstask\_multiple\_delete: java.lang.NullPointerException: Cannot invoke 'java.util.List.addAll\(java.util.Collection\)' because 'this.fPlaceHolders' is null: com.glide.db.conditions. ASetCondition. formatFieldSet \(ASetCondition.java:265\) com.glide.db. conditions.ASetCondition. formatSet \(ASetCondition.java:157\)'.

</td><td>

1.  Create a table 'u\_cstask\_multiple\_delete'.
2.  Add a single string column 'end\_of\_life\_item'.
3.  Generate around 10,000 items.
4.  Try to delete them using Glide record and IN condition.
5.  Make sure to put more than 1,000 values into the addQuery IN values.

 Observe that a NullPointerException is thrown.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1945816

</td><td>

A connection pool should properly handle errors during expansion

</td><td>

This issue was observed in a user's production instance where the PRI database connection pool became exhausted. The exhaustion occurred because several threads were holding PRI DB connections while executing queries on the RR database. During this time the RR database went down \(due to a hardware failure\), and these threads remained blocked for approximately 10–15 minutes, resulting in pool exhaustion.

</td><td>

1.  Create an instance that has a read-replica DB.
2.  Execute repeated transactions that result in routing some, but not all, of the queries to the read replica.
3.  While these queries are running, the read-replica database needs to go down \(either kill -9 or unplug the box\).

 Observe that the system becomes unavailable for 10-15 minutes until the transactions begin to timeout.

</td></tr><tr><td>

Database Persistence - Graph

 PRB1974718

</td><td>

Null value optimization must handle a case where Genius Results are reused and null everything again

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1970223

</td><td>

The DBSqlParser query modifies the sys\_id ElementDescriptor storage table name, which breaks queries to the parent tables after

</td><td>

As a result, queries against parent tables are failing with an error similar to: 'Syntax Error or Access Rule Violation detected by database \(\(conn=31570\) Unknown column 'customer\_account0.sys\_id' in 'SELECT'\)'.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1881041

</td><td>

The **New** button displays on related lists where it isn't configured

</td><td>

 

</td><td>

1.  Provision an instance with the GRC: Advanced Risk and GRC: Risk Management Workspace plugins installed.
2.  Open the 'Lists' page in the Risk Workspace.
3.  Navigate to 'Risk assessment project' section.
4.  Select the **New** button visible at the top right on the list page.
5.  Fill all of the required fields.
6.  Make sure the impersonating user is set as the owner.
7.  Move the project to the 'Risk scoping stage'.

 Observe the **New** button that's visible on the 'Risks' related list.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1944655

</td><td>

The 'Data Privacy anonymization' job fails when resumed after an upgrade

</td><td>

 

</td><td>

1.  Create a data privacy job in a Yokohama instance.
2.  Pause the job and upgrade the instance to Zurich.
3.  Resume the job once an instance is upgraded.

 Notice that the anonymization job fails when resumed after an upgrade.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1975900

</td><td>

In Data Privacy's anonymization policies, 'Select child table filter \(Optional\)' values aren't saved

</td><td>

There's no logging.

</td><td>

 

</td></tr><tr><td>

Data Privacy

 PRB1978912

</td><td>

Data Privacy is incorrectly customizing the 'sys\_declarative\_ action\_assignment\_ 38b9d94373 12011071783 b1f3bf6a7e4' file

</td><td>

 

</td><td>

1.  Before installing Data Privacy, open the 'sys\_declarative\_ action\_assignment\_ 38b9d94373 12011071783 b1f3bf6a7e4' file.

Notice 'Experience Restricted' = true.

2.  Install Data Privacy.
3.  Open the file.

Notice 'Experience Restricted' = false


 The Data Privacy application installation shouldn't change the file data.

</td></tr><tr><td>

DevOps \(Family\)

 PRB1974768

</td><td>

Duplicate pull requests are created due to a concurrency problem

</td><td>

Database level uniqueness isn't present and, as a result, a duplicate record is created when a race condition happens.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1895238

 [KB2249032](https://hi.service-now.com/kb_view.do?sysparm_article=KB2249032)

</td><td>

Cloud Application Patterns are launched sequentially and contribute to the long discovery schedule

</td><td>

The launching time of a massive number of probes should be improved.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1903928

</td><td>

Slow query with primary\_hash=-865319141 runs 60k times per day, consuming reasonable time from the database

</td><td>

Users with a relatively high number of records on cmp\_discovery\_ldc\_config may be affected by query primary\_hash=-865319141. It can run thousand of times, reading the entire table.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1962473

</td><td>

The 'AWS Org Assume Role' fails when using wildcard ARN containing an IAM role path

</td><td>

Discovery using the 'AWS Organization Assume Role' fails when the access role name in cloud\_service\_account \_aws\_org\_assume \_role\_params contains both a wildcard \(\*\) and an IAM role path. During credential resolution, the MID Server truncates the ARN at the first path separator and attempts to assume arn:aws:iam::member-id:role/xa instead of the full path-qualified role name. This results in an access denied error from AWS STS, causing the Amazon AWS Datacenter pattern to fail for all member accounts. The issue does not occur when the same ARN is configured explicitly per a member account.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1969791

</td><td>

The Discovery Pattern logs say Warning CI Pattern is completed, even though the pattern failed completely

</td><td>

Even though the classification is successful, if the pattern fails to get the basic identification details such as name, serial number, etc., the pattern fails completely. However, the Discovery Pattern logs say the Warning CI Pattern was completed but failed some post-processing steps.

</td><td>

Run an SNMP Discovery.

 Observe that the pattern fails if it fails to get the basic identification details. However, the Discovery Pattern logs say the Warning CI Pattern was completed but failed some post-processing steps.

</td></tr><tr><td>

Discovery

 PRB1970237

 [KB2738206](https://hi.service-now.com/kb_view.do?sysparm_article=KB2738206)

</td><td>

Post-Zurich upgrade, pattern debug mode isn't working as expected

</td><td>

Post-upgrade, when users open the pattern step and try to debug, for troubleshooting, users aren't getting the options of selecting the Cloud Service Account and AWS datacenter information for which is needed to run the discovery in debug mode.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1974425

</td><td>

Make the **Discover Now** button primary in the workspace 'Form' view

</td><td>

Update the button style on the existing UI action record for **Discover Now** to mark it as primary.

</td><td>

1.  Navigate to **Discovery Admin Workspace** &gt; **Schedules**.
2.  Select any IP-based schedule.
3.  On the schedule 'Details' page, select the 'Schedule Details' section.

 Expected behavior: As one of the main UI actions on each schedule form is **Discover Now**, this should be displayed as a primary button.

 Actual behavior: Notice that the style of the **Discover Now** action button displayed isn't 'primary'.

</td></tr><tr><td>

Document Viewer

 PRB1947203

</td><td>

After upgrading to Yokohama, there's an issue during the generation of a PDF file for a custom audit process using the PDFGenerationAPI library

</td><td>

The URL of an image or some function of the style of the HTML text used as the basis for the PDF file isn't converted or supported.

</td><td>

1.  Take the **Corporate FSQ Audit engagement** field \(engagement\_type\) with the status \(state\) as 'Follow Up' \(5\).
2.  Verify that the **Report** field \(kb\_article\) is populated.
3.  Verify that the **Audit Report State** field \(u\_audit\_report\_state\) is 'Final Report Delivery' \(final\_review\).
4.  Select the **Preview Audit Report** UI action that appears.

 An attachment should automatically be generated and be attached to the engagement in question, but nothing happens.

</td></tr><tr><td>

Dynamic Schema

 PRB1972205

</td><td>

There's an incorrect index on the dynamic\_choice table

</td><td>

The existing index on dynamic\_choice prevents separate choice\_sets from having the same value.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1942395

</td><td>

The cursor moves to the end of an input field when the CPU throttling is 4\* slower and 6\* slower

</td><td>

 

</td><td>

1.  Log in as an admin user.
2.  Navigate to CSM Workspace.
3.  Open a case record.
4.  Navigate to **Compose email**.
5.  Change CPU throttling in the 'Network' tab to 4\*slower/6\*slower.
6.  Type continuously.

Observe that the cursor jumps to the end while typing.


 Expected behavior: Drafting an email shouldn't encounter unexpected cursor placement to the end.

 Actual behavior: The cursor moves to the end while typing.

</td></tr><tr><td>

Email Notifications

 PRB1964152

</td><td>

Email Client template behavior changed after upgrading to Zurich

</td><td>

After upgrading to Zurich, the behavior of Email Client template selection has changed. In Xanadu and Yokohama, the system always reverted to the default template when showing the 'Email' tab again. However, in Zurich, the system keeps the last used template \(template2\) instead of returning to the default.

</td><td>

1.  Log in to an instance.
2.  Open Service Operations Workspace.
3.  Open an incident record from the list.
4.  Select the **Detail** tab.
5.  Select the **More** menu on the right of 'Work notes', then select **Email** \(→ template1 is applied\).
6.  Confirm that template1 is currently applied.
7.  Select the **Email Template** icon on the right-side menu.
8.  Select **template2**, then select **Apply Template**.
9.  After template2 is applied, enter an email address in the **To** field and select **Send Email**.
10. Repeat Step 5.

 Expected behavior: Template1 is applied again \(returns to the initial status\).

 Actual behavior: Template2 remains applied \(the last used template is applied\).

</td></tr><tr><td>

Event Management

 PRB1975115

</td><td>

Slow processing of the 'Event Management - Maintenance Calculator' job when processing a large number of closed alerts

</td><td>

For users that have large number of closed alerts, this update can take about 20 minutes in case of the user with about 50k-100k closed alerts.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1971237

</td><td>

Unable to run 65M Load Test

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Under CISP Test suites, select **NMA\_Mock: 65M\_NMA\_MT\_Equip\_Data\_Update**.
3.  Select **Execute Tests**.
4.  Select **Execution Profile as Nested Payload**.
5.  Select **OK**.
6.  Check CISP executions for the results.

 Observe that certain executions didn't run.

</td></tr><tr><td>

Flow Engine

 PRB1984516

 [KB2741852](https://hi.service-now.com/kb_view.do?sysparm_article=KB2741852)

</td><td>

Flows with record triggers intermittently aren't triggering after a Zurich upgrade

</td><td>

The root cause of the issue lies in the record trigger cache preparation, which isn't thread safe. This may result in returning incomplete triggers that cause flows/playbooks not to trigger.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1948205

</td><td>

A user isn't able to delete 'Assign Subflow Output' flow logic's inputs

</td><td>

 

</td><td>

1.  Open any subflow with 'Assign Subflow Output' like 'Batch Rollback' or 'Batch Install'.
2.  Delete any of the outputs from the 'Assign Subflow Output' logic.
3.  Select **Done**.
4.  Reload.
5.  Expand 'Assign Subflow Output' again.

 Notice all the variables are still there.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1954202

</td><td>

Nested complex objects don't preserve dropped pills

</td><td>

When the user drops a complex object pill into a nested complex object, it does not save correctly \(with or without SAYG\). Dropping a pill on the root level works.

</td><td>

1.  Create an action that outputs a complex object.
2.  Create an action that has an input that is a complex object with a complex object nested within.
3.  Add action \#1 to a subflow.
4.  Add action \#2 to a subflow.
5.  Pass the output of action \#1 to action \#2's NESTED CO input \(not the top level CO itself\) by dropping a pill.
6.  Save the subflow \(skip if save-as-you-go is enabled. Note this bug occurs regardless of SAYG enabled/disabled\).
7.  Test the subflow.

Observe that the passed complex object works at runtime.

8.  Reload the subflow and observe that the pill is missing.
9.  Test the subflow.

 Observe that the passed complex object does not work at runtime.

</td></tr><tr><td>

Form Templates

 PRB1968784

</td><td>

Users aren't able to update certain fields using templates in Service Operations Workspace \(SOW\)

</td><td>

When a field depends on another field, if a user is attempting to clear the dependent field value via a template while the parent field is populated, the system validates if the new value exists within the parent field's reference. The validation fails, preventing the field from being cleared.

</td><td>

1.  Navigate to an instance.
2.  Impersonate any users who have roles to control incident along with SOW and to use a template.
3.  Navigate to **SOW** &gt; **incident record** to apply a template.
4.  Fill out values in an assignment group and 'assigned to' columns.
5.  Select the template icon in the far right panel and choose it to update a field for instance 'Assigned to'.

 Expected behavior: A warning message shouldn't appear. And the **Assigned to** field should be updated.

 Actual behavior: A warning 'unable to update field Assigned to' message appears and users are unable to update the **Assigned to** field.

</td></tr><tr><td>

GlideRecord

 PRB1981009

</td><td>

MID Server core logic for Collector Framework

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Horizon Design System

 PRB1973789

</td><td>

Agentic AI and GenAI color gradient implementation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HTML Field Type Editor

 PRB1953216

</td><td>

URL links added in HTML fields no longer change color when the **Toggle theme** button on the TinyMCE editor is clicked

</td><td>

The issue is observed in Zurich. It was tested in both light and dark themes, Next Experience, and coral.

</td><td>

1.  In a Zurich instance, navigate to kb\_knowledge.do.
2.  Copy and paste a URL link into the **Article body** HTML field.
3.  Select the **Toggle theme** button.

Observe no color changes.

4.  Repeat the same steps in a Yokohama instance.

Observe different behavior.


</td></tr><tr><td>

Identification and Reconciliation API

 PRB1972817

</td><td>

There's an NMA update exception

</td><td>

This results in various errors during the load test.

</td><td>

1.  Run OKR Mixed Load Test with CMDB Updates, Event Management, Discovery, and Order Management.
2.  Run the 10M NMA Update using CISP.
3.  Check for errors during the load test.

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB1972551

</td><td>

Protected data definitions sent to Clickhouse have invalid values for user names and application names

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB1974639

</td><td>

Track inbound API integration requests as GCF events for licensing

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Install Base Management Store

 PRB1972327

</td><td>

Instance performance issue due to no NULL checks in the InstallBaseUtilSNC base instance script include

</td><td>

'sn\_customerservice.unified\_consumer role' was added to a group, causing a cascading change to 27 child groups containing over 7000 users. Subsequently, users with this new role who didn't have a corresponding entry in the consumer table were caused to run a 'select \*' query on 'sn\_install\_base' tables. This results in queries of tables containing over 2 million records being continuously executed.

</td><td>

1.  Open a base instance.
2.  Try to assign 'sn\_customerservice .unified\_consumer role' to a high number of users \(or any group with a lot of members\).
3.  Try to open any case as any user from the above list.

 Observe the slowness. Global.CSManagementUtils .getConsumerID\(\) returns null for a user who doesn't have a record in csm\_consumer table and has a unified\_consumer role. This method is used in other methods, which are used in dynamic filters.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1821656

</td><td>

A carriage return character \(&amp;\#13;\) is added

</td><td>

A carriage return character is added when work notes or additional comments are synced to an instance.

</td><td>

1.  Navigate to a producer instance.
2.  Make a multi-line comment.
3.  Save.
4.  Navigate to a consumer instance.

 Observe that the carriage return character \(&amp;\#13;\) is added to the new line.

</td></tr><tr><td>

Internationalization Features

 PRB1892286

 [KB2277705](https://hi.service-now.com/kb_view.do?sysparm_article=KB2277705)

</td><td>

A non-admin user can't change a dashboard name by specific steps when the system language is set to Japanese

</td><td>

The dashboard name should be updated correctly and reflected in both the primary record and its translated fields, as it is in the Washington and Xanadu versions. In the Yokohama version, the update to the dashboard name fails silently when the Japanese language is enabled and the sys\_translated record exists.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Internationalization Features

 PRB1912273

</td><td>

After a Yokohama upgrade, catalog admins can't create new sys\_translated records

</td><td>

Since the upgrade to Yokohama, it's no longer possible for catalog\_admin users to create new records in table \[sys\_translated\], only update existing ones.

</td><td>

1.  Provision a Yokohama base instance with a language plugin installed.
2.  Create a testuser with the role catalog\_admin to access the catalog items and their variable sets and variables \(but not the sys\_translated table directly\).
3.  As sys\_admin, create two variables for any catalog item.
4.  Add a translation for one of the two variables.
5.  Switch to testuser.
6.  Open the catalog item.
7.  Change the preferred language to the one associated with the plugin \(make sure the translation exists\).
8.  Change the English value to a translation for the variable that wasn't translated yet.
9.  As sys\_admin, check on the sys\_translated table directly.
10. Observe that the change is instantly reverted after trying to save it and isn't saved.
11. As testuster, adjust the existing translation of the variable question text for the translation that already exists.

 Observe that the adjustment is saved correctly and can be found in the sys\_translated table, with 'updated' and 'updated by' correctly updated to the testuser.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1906571

</td><td>

Password2 system properties return an encrypted value after a node restart for on-prem instances

</td><td>

In on-premises environments, database \(DB\) properties aren't being correctly decrypted and remain encrypted in memory.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1906606

 [KB2601723](https://hi.service-now.com/kb_view.do?sysparm_article=KB2601723)

</td><td>

SEK rekey fails for records with undefined or invalid sys\_id or invalid table

</td><td>

Bagheera should handle undefined/null/empty sys\_id records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Knowledge Management

 PRB1929677

</td><td>

There's an issue with the dependent field values in Knowledge Management

</td><td>

When users create a KB Article from the list where the filter conditions are applied, the same values are populated on the new record.

</td><td>

1.  Navigate to knowledge list.
2.  Run a list filter with a mismatched combination of a knowledge base + a category defined under a different knowledge base.
3.  Select the **New** action.

 Observe that the form is populated with the mismatched values.

</td></tr><tr><td>

Lifecycle Events

 PRB1888762

</td><td>

LE/JD test failures

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1926700

</td><td>

Users are unable to select a custom component of a presentational list inside a modal

</td><td>

There's a presentational list inside a modal in UI Builder and the list has a custom component now button. When the modal is opened and the button **iconic** is selected, users see expected behavior. But, if users try to close the modal and reopen it again and then click on the button icon, the event 'NOW\_LIST\# CUSTOM\_COMPONENT \_ACTION\_DISPATCHED' doesn't get dispatched.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1964711

</td><td>

Reverse DNS lookup fails due to a mismatch between a fixed FQDN and a dynamically assigned IP address

</td><td>

Reverse DNS lookup in the users' environment fails because the host is configured with a fixed FQDN, while the IP address assigned to the system is dynamic. Since the PTR \(reverse DNS\) records in DNS aren't updated when the IP address changes, the reverse lookup returns either no hostname or an incorrect hostname for the current IP.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1979842

</td><td>

New function type for voice launcher

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB1972984

</td><td>

Build Multimodal Glide Service to support AIS multimodal document search

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multi-provider Single Sign-on \(SSO\)

 PRB1920554

</td><td>

The 'Check certificate expiration' job fails daily

</td><td>

If the user runs the job 'Check certificate expiration' on an instance with multiple certificates, the localhost\_log shows an issue for every certificate that got null.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1980286

</td><td>

The 'Preference' menu freezes when there's a circular dependency in the theme record

</td><td>

 

</td><td>

1.  Create a circular dependency in the Sys Ux theme of an active theme where the properties look like: '--property-1: --property 1'.
2.  Save the record.
3.  Reload the page.
4.  Open the preferences modal.

 Expected behavior: The preferences modal works as expected.

 Actual behavior: The page freezes and becomes unusable.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1981430

</td><td>

AIEL/X can't be loaded from the current endpoint

</td><td>

 

</td><td>

Load an instance configured with NextWave.

 Notice it doesn't work because the AIEL/X dependencies aren't reachable at the current endpoint.

</td></tr><tr><td>

Notify

 PRB1972166

</td><td>

Increase the transcript ID size in the 'Notify Transcript' table to accommodate bigger IDs

</td><td>

The newly added table 'Notify Transcript' has a field Transcript ID, which is of length 100. This needs to be increased to 500 as MS teams transcript ID is &gt; 300 and this size constraint is a blocker for the transcript feature to work.

</td><td>

Use MS teams integration over Notify with transcript support.

 Notice that the transcript ID stored is truncated as the limit is lower than the size.

</td></tr><tr><td>

Now Assist Panel

 PRB1982458

</td><td>

Instances with firewall issues or without ADC setup can't access AIEL assets through sk8s

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1984097

</td><td>

Increase the JWT expiration

</td><td>

Set the JWT expiration to a larger value and make it tied to a session.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1909337

</td><td>

No response after selecting On-Call Calendar if there's no shift in cmn\_rota

</td><td>

When the user tries to select On-Call Calendar, there's no response and no message, but a green border is displayed for an unknown reason. It seems related to the presence or absence of shift\(cmn\_rota\). Instead, the system should display a meaningful message on the page when no shifts are available.

</td><td>

1.  Execute cmn\_rota.list.
2.  Confirm there are no records.
3.  Navigate to On-Call Scheduling.
4.  Select **On-Call Calendar**.

 Observe that there's no response and no message, but a green border is displayed for an unknown reason.

</td></tr><tr><td>

On-Call Scheduling

 PRB1938628

</td><td>

When adding a coverage to a shift, the user is displayed two times on the 'day' view of the on-call schedule

</td><td>

 

</td><td>

1.  Create two or more shifts for a group.
2.  Ensure that one shift is using new schedule engine, and the other one with the old schedule engine.
3.  Add coverage to users in the new schedule engine.
4.  Select the shift in the classic calendar to view the on-call persons.

 Observe that users are displayed twice. The user should be displayed only once.

</td></tr><tr><td>

On-Call Scheduling

 PRB1967490

</td><td>

OnCallRotation.getPrimaryUser returns null for across day shift time while using 2024\_schedule\_engine

</td><td>

The script to get the primary on-call doesn't return valid data. Instead, it returns a null value.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1925002

</td><td>

Agentic Workflow's trigger sys\_user is taking precedence over run as 'AI User'

</td><td>

When trigger conditions are met, the workflow should be executed with workflow's 'Run As' user for the new incident. However, the workflow is actually executed with the trigger's sys\_user and the execution is terminated with the error 'Access Denied'.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1962281

</td><td>

Users are unable to uninstall a Store application that contains any tables which are restricted as a part of AccessHandler

</td><td>

When an admin user tries uninstalling the apps, uninstallation fails with an error: 'Deleted X,YZ metadata records, could not delete 2. The store application was deactivated, but not deleted'.

</td><td>

1.  Create a custom app or use a Store app.
2.  Add files under the sys\_gen\_ai\_ license\_metadata\_trial table.
3.  Try to uninstall the custom or Store app.

 Users with admin rights are unable to uninstall the app as the uninstall is unable to delete these tables data because of Access Handler.

</td></tr><tr><td>

OneExtend

 PRB1968937

</td><td>

Conversations aren't building correctly when users try with the aia\_artifact\_dataset table, even though identical queries work as expected with the qna\_dataset table

</td><td>

The conversations generated for both records are incorrect, and in some cases no conversation is generated at all. However, running the same queries using the qna\_dataset table or executing them manually produces the expected conversations. This suggests that Auto Chat isn't functioning correctly with the aia\_artifact\_dataset table.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1971589

</td><td>

cypher2Results API is broken with Glide record dynamic

</td><td>

A null pointer exception is coming from OneExtend: 'Couldn't decipher the stack trace resulting from the following JavaScriptException.'

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1978709

</td><td>

Now Assist Portal \(NAP\) and AI Agents fail because outbound URLs ignore the project ID of the connection URL \(sys\_alias\)

</td><td>

In the Gemini BYOK integration, outbound requests made by NAP and AI Agents fail because the generated outbound URLs don't include the project ID from the connection URL \(sys\_alias\). These features rely on the Java proxy to construct outbound URLs, but the proxy doesn't append the project ID. As a results, calls are sent to an incorrect or incomplete Gemini endpoint, and the user gets the error 'Invalid HTTP response 404: Not Found'. In contrast, Incident Summarization and Code Generation features work correctly because they use the Flow Designer, which properly constructs outbound URLs and includes the project ID as part of the request path. Since NAP and AI Agents bypass Flow Designer and instead use the Java proxy which omits the project ID, their outbound calls fail consistently.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1981515

</td><td>

Add enhanced debug logging around async client call

</td><td>

There needs to be debug logs added when each streamed chunk is received, when the final callback is received \(VAStreamConsumer\), before enqueueing in the hybrid queue, and after enqueueing in the hybrid queue and the callback is complete.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1981554

</td><td>

The 'One Extend' plugin needs the extension point for Hermes health checks

</td><td>

Without this health check endpoint in the extension points for Glide One Extend, alerts are sent to the SRE.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1981648

</td><td>

integration\_type metadata is missing in metadata sync, which is needed to support BYOK scenarios

</td><td>

Metadata sync from Glide to Mosaic is missing the provider's integration\_type related metadata. Without this metadata, Mosaic would not know whether customer has opted in for BYOK and so cannot support BYOK related use cases.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1986722

</td><td>

During Mosaic Log Sync, not all Generative AI metrics are persisted

</td><td>

 

</td><td>

 

</td></tr><tr><td>

PDF Generation

 PRB1829301

</td><td>

System Trigger-PDFReportExportJob causes nodes to go out of memory

</td><td>

One user had slowness in the instance when the trigger on PDFReportExportJobs was executed. This trigger was consuming a lot of memory which forced support to turn off the execution. This was observed multiple times in the instance.

</td><td>

 

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB1958610

</td><td>

'Perf Analytics Pack for Agile 2.0' doesn't have the necessary ACLs to view dashboards

</td><td>

There's an error message: 'Part of the query on sys\_portal\_preferences has been ignored because of insufficient access for 'query\_match' operation on sys\_portal\_ preferences.portal\_section'. Instances already have a query\_match ACL for \*.\* if the user has read access to the table. There's no read access has been provided to the sys\_portal\_preferences table other than the admin role, even though this dashboard is shared with the scrum\_user role.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1823066

</td><td>

Investigate and fix test failures in ams-analytics-business-calendar test project

</td><td>

Various tests started failing. These tests were related to BusinessCalendarAnalyticsHubIT, DeleteCalendarIT, DSTargetsCommentsIT, ListWidgetIT, PeriodsIntervalIT, SingleScoreWidgetIT, and TimeSeriesWidgetIT.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1936517

</td><td>

A user with minimal roles can't add a breakdown to an indicator

</td><td>

A new API must be created to get indicator breakdowns.

</td><td>

1.  Create an user with a minimal role.
2.  Log in to an instance using that user.
3.  Navigate to data viz center.
4.  Add an indicator scorecard as a viz type.
5.  Change the source definition to 'Manually Selected'.
6.  Add 'Number of open incidents'.

 Observe that the user isn't able to add any breakdown. A 'There is no valid breakdown' message is displayed.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1972888

 [KB2687484](https://hi.service-now.com/kb_view.do?sysparm_article=KB2687484)

</td><td>

Widgets are missing from dashboards in CAM, AO, and SCA Overview pages on the latest main and Zurich builds for CAM Application

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1977527

</td><td>

columnLimit has an invalid value, as it expected a value than can be converted to type 'Int' but it was a 'String'

</td><td>

On post-upgrade to Zurich, in list-type visualizations, if the **Number of columns displayed** field isn't specified, an error message is displayed: 'Variable 'columnLimit' has an invalid value: Expected a value that can be converted to type 'Int', but it was a 'String''.

</td><td>

1.  Create a dashboard with a list visualisation.
2.  Configure the number of columns to be displayed and leave it empty.

 Observe the error message.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1962944

</td><td>

Duplicate records are created in the analytics\_category\_m2m table when using UnloadDashboard before and after Platform Analytics migration

</td><td>

In the Zurich release, when a Core UI dashboard is exported from a source instance using UnloadDashboard before a Platform Analytics migration, and then the same dashboard is migrated to a Platform Analytics dashboard and exported again using UnloadDashboard after migration, duplicate category records are created in the analytics\_category\_m2m table upon importing to the target instance. This issue occurs when both the source and target instances perform the migration process and the migrated dashboard is re-imported through an update set. As a result, the migrated dashboard in the target instance displays two identical categories, with duplicate links in the analytics\_category\_m2m table.

</td><td>

1.  In the source instance, create a new update set and set it as current.
2.  Create a Core UI dashboard and assign it to a dashboard group.
3.  Use the UnloadDashboard functionality to record the dashboard into the current update set.
4.  Mark the update set as 'Complete' and export it to an XML file.
5.  In the target instance, upload, preview, and commit the update set XML file.
6.  In both the source and target instances, migrate the Core UI dashboard to a Platform Analytics dashboard using Migration Center.
7.  In the source instance, create an update set and set it as current again.
8.  Use UnloadDashboard again \(this time after the Platform Analytics migration\) to capture the Platform Analytics dashboard into the update set.
9.  In the target instance, upload, preview, and commit this new update set XML file.
10. In the target instance, open the migrated Platform Analytics dashboard and verify its category.

</td></tr><tr><td>

Platform Licensing

 PRB1980200

</td><td>

True-up of SM and LE 6.0.2

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Process Mining component for Platform Analytics

 PRB1949256

</td><td>

A filter on a promin component on Platform Analytics dashboard gives 'undefined' instead of displaying the task progress

</td><td>

 

</td><td>

1.  Navigate to Platform Analytics workspace.
2.  Enable the process mining component.
3.  Apply a filter on the graph.

 Observe that it says 'undefined' in the top right corner instead of showing a loading circle.

</td></tr><tr><td>

Process Mining Workspace

 PRB1914287

</td><td>

'The page you are looking for could not be found' error is thrown after selecting 'Generate report'

</td><td>

The issue has been observed on the 2.4.2 and the 2.4.8 version of Automation Discovery \(ml-automation-discovery\).

</td><td>

1.  Provision an instance with the Automation Discovery plugin installed \(for example, the base instance for Zurich\).
2.  Enable Automation Discovery for the entity say incident at process configuration level.
3.  Create a project on incident table and mine.
4.  Open the workspace.
5.  Navigate to 'Automation Opportunities' tab.
6.  Select **Generate Report**.

 Observe that the message 'The page you are looking for could not be found.' appears.

</td></tr><tr><td>

Process Mining Workspace

 PRB1916916

</td><td>

When datetime is selected as **Activity Definition**, the grouping of activities isn't working

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1916953

</td><td>

Capitalization error on project cards

</td><td>

 

</td><td>

1.  Navigate to the Process Mining Workspace.
2.  View a card.

 Notice that 'records' doesn't have a capital letter.

</td></tr><tr><td>

Process Mining Workspace

 PRB1921794

</td><td>

The number of variants is 0, and the average record duration and total accumulated record duration is 0 seconds

</td><td>

On the opportunity details page, the number of variants is shown as 0. Also, the average record duration and the total accumulated record duration is shown as 0 seconds. This issue is seen for the automated findings of MDM projects and rule-based findings on both single or MDM projects.

</td><td>

1.  Open the analyst workbench of any mined MDM project with findings added.
2.  Select any finding.
3.  Navigate to the 'Opportunity details' page.

 Observe that the number of variants is shown as 0. Also, the average record duration and total accumulated record duration is shown as 0 seconds. When the user hovers on the number of variants, the total inefficiency duration is shown.

</td></tr><tr><td>

Process Mining Workspace

 PRB1932901

</td><td>

The user can save and apply automated findings with empty configuration values, which causes mining to fail

</td><td>

Mining fails with the error 'Event extraction failure: Extraction encountered an unexpected issue. Contact your admin'.

</td><td>

1.  Create a new project from the 'Process Projects' page.
2.  On the 'Set improvement opportunities' page, create a new automated finding.
3.  On the Configure screen, remove the default values.
4.  Select **Save** and exit.
5.  Observe that finding gets added to project.
6.  Mine the project.

 Observe that mining fails with the error 'Event extraction failure: Extraction encountered an unexpected issue. Contact your admin'.

</td></tr><tr><td>

Process Mining Workspace

 PRB1949520

</td><td>

Users aren't able to view processes if they have access to only some of the records from that table

</td><td>

 

</td><td>

1.  Impersonate abel.tuter.
2.  Open the 'Process config' list from Process Mining Workspace.
3.  Select the wrench icon on the left sidebar.
4.  Select the kb\_knowledge record from the list.

 Observe that a 'You don't have required access to the Knowledge table for viewing this configuration' error displays even though the user has access to some records in the kb\_knowledge table.

</td></tr><tr><td>

Process Mining Workspace

 PRB1955632

</td><td>

The 'Top 5 opportunities type' graph isn't displaying the improvement opportunity type with the highest records

</td><td>

 

</td><td>

1.  Navigate to the 'Summary and insights' page after adding findings.
2.  View the 'Top 5 opportunities type' graph.

 Observe that the data is not sorted with highest record frequency.

</td></tr><tr><td>

Process Mining Workspace

 PRB1959708

</td><td>

Users are able to see the global search icon in the Process Mining Workspace, despite not having the needed roles defined in the system property 'glide.ui.can\_search'

</td><td>

 

</td><td>

1.  Access a Glide instance.
2.  Impersonate Abel Tuter.
3.  Navigate to the Process Mining Workspace.

 Observe that the global search is visible.

</td></tr><tr><td>

Procurement

 PRB1970134

</td><td>

'Receive by' isn't populated when receiving through the stockroom import flow

</td><td>

In a normal PO flow, 'Received by' is populated by the user who received the assets. However, in the import flow, it's shown as empty.

</td><td>

1.  Log in to the instance.
2.  Create a purchase order.
3.  Create a purchase order line with Apple Mac, with the quantity set to 3.
4.  Open the stockroom page.
5.  Complete the import flow for the above POL.
6.  Provide the details for 3 assets.
7.  Select **Receive**.

 Observe that 'Receive by' isn't populated on the receiving slip.

</td></tr><tr><td>

Request Management

 PRB1976593

</td><td>

A flow configuration for run as = system isn't honored and its being trigged as the session user, causing security errors in flow execution

</td><td>

 

</td><td>

1.  Impersonate an itil user.
2.  Navigate to the esc portal.
3.  Search for 'catalog item - Developer Laptop \(Mac\)'.
4.  Select the item fill the form and submit.
5.  End the impersonate the open request \(sc\_request\) table.
6.  In the related list users can see the approvers; open any one of them and select the **Approve** UI action.
7.  Similarly, open the attached requested item and approve for the available approvals.
8.  Select the **Flow context** action in the related links.

 Expected behavior: The flow should have been executed with the system user.

 Actual behavior: The flow is being executed using a logged-in session user.

</td></tr><tr><td>

Resource Management

 PRB1941447

 [KB2552237](https://hi.service-now.com/kb_view.do?sysparm_article=KB2552237)

</td><td>

The assignment FTE falls to an incorrect value due to lack of availability adjustment to 24 hours in the monthly view of RMWS

</td><td>

The issue is caused by not adjusting availability to 24 hours. It should adjust availability to 24 hours and redistribute hours evenly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Schedule Optimization

 PRB1976735

</td><td>

Re-true up Schedule Optimization and map integration apps for DM2 changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1977288

</td><td>

Skipped business rule issues during Schedule Optimization \(SO\) updates

</td><td>

Business rules are skipped or not skipped incorrectly during/after SO due to edge cases not being handled in the current logic to evaluate if SO is making the update, and due to workflows being turned off when locked tasks are updated.

</td><td>

 

</td></tr><tr><td>

Seismic Framework

 PRB1961091

</td><td>

The seismic placeholders 'nowPlaceholderHeight' and 'nowPlaceholderWidth' aren't rendering components

</td><td>

When both events in a starting position are visible on the screen, the templates render correctly. When the starting positions of both the events aren't visible on the screen but still they are in view port \(gets hidden due to the section header\), only one template renders and the other doesn't.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1955078

</td><td>

Singletons are broken by the inclusion of a module ID in URI

</td><td>

A change made in Zurich, as part of a fix, broke singleton behavior in modules.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1935624

</td><td>

'Hide filters' and 'Clear All' in a facet search aren't properly aligned

</td><td>

The 'Hide filters' and 'Clear All' options are showing, but they aren't aligned. There are a few pixel mismatches.

</td><td>

1.  Search for something in ESC portal.
2.  Observe the facets on the right side.
3.  Choose one of the sources so 'Clear All' shows up.

 Expected behavior: The 'Hide filters' and 'Clear All' options are aligned.

 Actual behavior: The 'Hide filters' and 'Clear All' options are showing, but they aren't aligned. There are a few pixel mismatches.

</td></tr><tr><td>

Service Portal

 PRB1980872

</td><td>

Provide a configuration for navigation from angular pages to Lit pages

</td><td>

In some portals, users have embedded angular experiences. Not all pages are moved to Lit in a single go, but in a phased manner. There are cases where an embedded angular experience has a navigation to a angular page, which has an equivalent experience in Lit. In such cases, users should be redirected to a Lit page.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1981788

</td><td>

A non-admin user can't view the notification on a portal and are getting the recordUpdateCount

</td><td>

 

</td><td>

Log in to a portal with some non-admin user.

 Expected behavior: A notification shall appear for the non-admin user.

 Actual behavior: Check for the notification and see that no notification is visible.

</td></tr><tr><td>

Service Portal

 PRB1981887

</td><td>

The tooltip and date picker don't render when a catalog item is embedded in Lit

</td><td>

 

</td><td>

1.  Embed a Service Catalog item inside a Lit-based page/component.
2.  Open the catalog item form.
3.  Trigger a tooltip \(hover/focus a tooltip element\).
4.  Select a **date/time** field to open the date picker.

 Observe that the tooltip and/or date picker UI doesn't appear \(isn't rendered\).

</td></tr><tr><td>

Service Portal

 PRB1982070

</td><td>

Address issues identified during catalog embed

</td><td>

Issues include the following. The dropdown isn't coming below the question. There's no way to select the file for attachments. For Retina icons, 'Save as Draft' and the 'Update Draft' icon isn't coming up. Error/info messages aren't coming when the angular widget is embedded. Upon submitting, the user isn't navigated anywhere. Options in a few dropdowns, list collectors, reference and requested for aren't populated. A date picker isn't opening. In the case of masked input, it should 'u\_show' instead of 'show'. Unable to test 'Not available for' as when logging into Sirius as an admin. For a catalog of type KB, on clicking the article, it's redirecting to /sirius?id=kb\_article&amp;sys\_id=. The instance options aren't correctly propagated to the angular widget. An HTML question in catalog isn't coming up properly. If a widget is rendered as a question in a catalog, the widget's styles aren't applied.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1982188

</td><td>

Users can't differentiate menu items in a sidebar to provide sections or groups

</td><td>

The sidebar currently can't support providing dividers between groups of items as shown in the figma.

</td><td>

1.  Open /aix/aix-portal/.
2.  Observe the sidebar.

 Expected behavior: There's a divider between different sections of items.

 Actual behavior: There's no way to provide a divider.

</td></tr><tr><td>

Service Portal

 PRB1982599

</td><td>

An object type in instance properties isn't working in widgetInstance

</td><td>

 

</td><td>

1.  Create a widget that accepts an object type property.
2.  Pass a object property via widget options.

 Expected behavior: The object type property value should be available in the server script.

 Actual behavior: The object type property isn't available in the options of the server script.

</td></tr><tr><td>

Service Portal

 PRB1982715

</td><td>

Widget metadata isn't cached on the client

</td><td>

Metadata is served via config API and not cacheable, but it should be.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1982935

</td><td>

AIX requires a full page chat experience

</td><td>

The chat requires a separate route and must be opened with 100% width.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1983135

</td><td>

Use the new aix\_icon type instead of the glyphIcon type

</td><td>

glyphicon is tied to Bootstrap's icon set and FontAwesome. The AI Experience now uses custom svg icons from the aiux-kit \(sn-aix-icon web component\).

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1983640

</td><td>

Multiple AIX dictionary tables have reference fields without reference\_cascade\_rule defined

</td><td>

This can lead to orphaned records or unexpected behavior when referenced records are deleted.

</td><td>

1.  Navigate to an AIX Experience record.
2.  Create related records \(e.g., experience properties, route maps, menu items\).
3.  Delete the parent experience record.

 Observe that child records \(properties, route maps\) may remain as orphans instead of being cascade deleted. Alternatively, delete a referenced widget and observe the app shell reference isn't properly cleared.

</td></tr><tr><td>

Service Portal

 PRB1984642

</td><td>

No current support for dashboard subtitles

</td><td>

 

</td><td>

Navigate to /aix/aix-portal/dashboard.

 Expected behavior: 'Here's your day at a glance' should be available as a subtitle.

 Actual behavior: 'Here's your day at a glance' is hardcoded.

</td></tr><tr><td>

Service Portal

 PRB1984694

</td><td>

Link color angular variable mapping must be updated

</td><td>

Change angular variable as per update design: $link-color to var\(--color-primary\) and $link-hover-color to var\(--primary-700\).

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1985141

</td><td>

Saving sys\_ux\_widget fails component validation

</td><td>

There's a component validation error: 'Could not save record because of a compile error: JavaScript parse error at line \(1\) column \(7\) problem = identifier "import" is a reserved word'.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1985562

</td><td>

Address issues identified during catalog embed

</td><td>

Issues include the following. The dropdown isn't coming below the question. There's no way to select the file for attachments. For Retina icons, 'Save as Draft' and the 'Update Draft' icon isn't coming up. Error/info messages aren't coming when the angular widget is embedded. Upon submitting, the user isn't navigated anywhere. Options in a few dropdowns, list collectors, reference and requested for aren't populated. A date picker isn't opening. In the case of masked input, it should 'u\_show' instead of 'show'. Unable to test 'Not available for' as when logging into Sirius as an admin. For a catalog of type KB, on clicking the article, it's redirecting to /sirius?id=kb\_article&amp;sys\_id=. The instance options aren't correctly propagated to the angular widget. An HTML question in catalog isn't coming up properly. If a widget is rendered as a question in a catalog, the widget's styles aren't applied.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1985806

</td><td>

Get widget.sys\_id from widgetInstance record and register it with AIEL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1985812

</td><td>

AI tool authors should be able to override widget action scripts

</td><td>

A tool author should be able to override the sys\_ux\_widget\_action their own custom script without copying the entire widget.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1985837

</td><td>

A record update on a child table doesn't trigger cache invalidation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1986152

</td><td>

Pinned widgets don't save

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  In the chat, type 'Show me my flight information'.
3.  Select the icon to pin the widget.
4.  Navigate to /aix/employee/canvas.

 Expected behavior: The widget should be pinned in the top left corner of the grid.

 Actual behavior: The widget isn't there.

</td></tr><tr><td>

Service Portal

 PRB1986754

</td><td>

Pinned widgets aren't returned from DashboardResolver

</td><td>

 

</td><td>

1.  Navigate to aixwashington/aix/employee/home.
2.  Ask the chat for a 'show me my flight details' widget.
3.  Pin the widget.
4.  Navigate to /aix/employee/canvas.

 Expected behavior: The pinned widget should show in the first slot of the dashboard.

 Actual behavior: The pinned widget is not shown.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1931636

</td><td>

Optimize member unread query

</td><td>

The CollabChatUnreadResponder has a long execution time.

</td><td>

1.  Create sidebar conversations using scripts.
2.  Send messages from each side of the conversation.

 Observe that the CollabChatUnreadResponder has a long execution time.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1971434

</td><td>

On SFS trueup, when users send a message, they get an exception saying that this.threadMembers is null and the message isn't sent

</td><td>

 

</td><td>

Send a collab message on trueup.

 The message doesn't send. On the debug, see the attached error.

</td></tr><tr><td>

Software Asset Management

 PRB1974875

</td><td>

Job failure troubleshooting for family releases

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Discovery

 PRB1967095

</td><td>

Software Asset Connections doesn't set the last scanned on cmdb\_sam\_sw\_install

</td><td>

Synch installed software pattern pre/post script should get the discovered date from cmdb\_ci\_appl.

</td><td>

 

</td></tr><tr><td>

Software Entitlements

 PRB1943125

 [KB2541050](https://hi.service-now.com/kb_view.do?sysparm_article=KB2541050)

</td><td>

Total cost calculation in software entitlements for workspace is different than on the form

</td><td>

The total cost displayed for software entitlements in the Software Asset Workspace \(SOW\) view is incorrect when compared to the form view of the same entitlement. The SOW is adding additional decimals on some occasions, which isn't consistent with the form view, which would have a rounded number. For example, Workspace: 10,441.5591 compared to Form: 10,440. This issue arises from the different outputs of the UI scripts CalculateTotalCostWS.getTimeSpan\(\) and CalculateTotalCost.getTimeSpan\(\), which should, but doesn't yield consistent results. This issue impacts the visibility of accurate cost information in Software Asset Workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Source-to-Pay Operations \(Glide\)

 PRB1978443

</td><td>

Integer to decimal changes, Java level changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

System Events and Jobs Dashboard

 PRB1917962

</td><td>

Charts in various tiles under the 'Current score' and 'Trends' sections aren't loading

</td><td>

In the System Events Dashboard, the charts under the 'Trends' section and the total error count under the 'Current score' section aren't loading.

</td><td>

1.  Log in as a user with elevated privileges.
2.  Navigate to **All** &gt; **System Diagnostics** &gt; **System Events and Jobs Monitoring** &gt; **System Events Dashboard**.
3.  Either keep the default filters or change any filters.
4.  Apply the filters.

 Observe that the charts under the 'Trends' section and the total error count under the 'Current score' section aren't loading.

</td></tr><tr><td>

System Events

 PRB1971488

</td><td>

Detect legacy jobs exist along with NowMQProcessingFrameworkJob and deletes the changes

</td><td>

In Zurich, when the flow\_queue migrates to processing framework, the legacy jobs are deleted and new NowMQ Processing jobs are created. But, if for any reason the legacy jobs aren't deleted or are created while users still have the 'NowMQ Processing' job, users detect it through a job running everyday and log it in the logs file \(and therefore it can be seen in the splunk logs\).

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB1974638

</td><td>

API Access Volume \(Data Egress\) exclusion for internal APIs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Table Administration and Data Management

 PRB1945120

</td><td>

Flow actions are deleted when they are reverted to older versions

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1965542

</td><td>

semaphore\_loans metric must have a sliding window

</td><td>

 

</td><td>

Execute xmlstats.do?include =semaphore\_loans,semaphores.

 The metrics for semaphore\_loans should have 1, 5, and 15-minute rollups like the ones for semaphores do.

</td></tr><tr><td>

UI Field Administration

 PRB1881510

</td><td>

The category under 'change request values' on the standard change template isn't reflected in Service Operations Workspace

</td><td>

This issue is present in the base instance as well. The category field is visible, but the value set for the category isn't visible under 'change template values'.

</td><td>

1.  In the application navigator, navigate to **Change** &gt; **Standard Change** &gt; **My Proposals** &gt; **New**.
2.  Create a new template with the change request values filled in.
3.  Request approval.
4.  In Service Operations Workspace, navigate to **List** &gt; **Tasks** &gt; **Assigned to you** \(remove the filter if required\).
5.  Open the standard change template.

 Observe that the category under 'change request values' isn't reflected.

</td></tr><tr><td>

Upgrade Center

 PRB1958321

</td><td>

Ensure schema changes occur before parallel plugin upgrades when Parallel Plugin Loading \(PPL\) is turned on

</td><td>

As a result, schema updates aren't completed before plugin upgrades begin when PPL is enabled. This can lead to multiple threads attempting to make schema modifications concurrently, causing potential conflicts and upgrade failures.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1963094

</td><td>

Users aren't able to interact with the Unified Navigation menu when the web sdk configuration becomes empty

</td><td>

Unified Navigation Menu interaction is stopped when the legacyConfig in sessionStorage is emptied by some scripts, causing errors related to trackingConsent and page freezing upon interaction. This restores smooth navigation between menu items.

</td><td>

1.  Load the home page.
2.  Open 'Inspect' mode in the browser.
3.  Navigate to the 'Application' tab.
4.  Delete the session storage.
5.  Try to interact with Unified Nav or other section of the page.
6.  Check that there's an error for tracking consent and the page is freezing.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1915787

</td><td>

There's a scope issue when using topic block as a tool in the AI agent

</td><td>

The AI agent internally calls the topic block 'Upload file 2', but it's not able to invoke the topic block and throws the error.

</td><td>

1.  Log in to an instance.
2.  Open the 'Testing' tab under AI agents.
3.  Test the AI agent: 'Upload attachment to the HR case'.

 Observe that it internally calls the topic block 'Upload file 2', which is used as a tool in the AI agent. It's not able to invoke the topic block and throws the error.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1961604

</td><td>

Implementing caching

</td><td>

 

</td><td>

1.  Set up GenAI and AI Search.
2.  Navigate to /esc.
3.  Open Virtual Agent.
4.  Type 'What is spam'.

 77 queries are issued over 7 separate transactions.

</td></tr><tr><td>

Virtual Agent

 PRB1962077

</td><td>

The Virtual Agent \(VA\) audio beep isn't heard for all chats in Zurich

</td><td>

 

</td><td>

1.  Log in to a Zurich instance.
2.  Navigate to /esc.
3.  Open Virtual Agent.

 Note that as the VA sends the messages, the chat audio alert isn't heard for each message \(sometimes it is heard at the end of the last message\). This was not the case prior to Zurich.

</td></tr><tr><td>

Virtual Agent

 PRB1973358

</td><td>

Support skillParams during execution

</td><td>

 

</td><td>

1.  Navigate to an instance with July Store apps installed.
2.  Turn on AIEL through guided setup.
3.  Turn on incident summarization skill.
4.  Navigate to the instance home page.
5.  Open the dev console.
6.  Inspect the element.
7.  Set the focus on sn-ai-engagement-experience.

 Excepted behavior: The skill gets executed without asking the user the record number.

 Actual behavior: The skill gets executed and asks the user for the record number.

</td></tr><tr><td>

Virtual Agent

 PRB1975277

</td><td>

The actual status of the additional chat features isn't reflected in the base instance NAVA assistant test window

</td><td>

In the test panel, the values of 'Allow web search', 'Allow response streaming', and 'Allow document uploads' are shown as 'Inactive'. This doesn't reflect the values set in the 'sys\_now\_assist\_ deployment\_config \_attributes' table.

</td><td>

1.  Navigate to **All** &gt; **Assistant Designer**.
2.  Ensure that you have active assistants 'Now Assist Panel - Platform \(default\)' and 'Now Assist in Virtual Agent \(default\)'.
3.  Navigate to the settings of 'Now Assist in Virtual Agent \(default\)'.
4.  In the 'Additional chat features' section, select the **Allow web search**, **Allow response streaming**, and **Allow document uploads** options.
5.  Save the assistant.
6.  Make sure the same options are selected for 'Now Assist Panel - Platform \(default\)'.
7.  Navigate to the table 'sys\_now\_assist\_deployment\_config\_attributes'.
8.  Search for 'doc\_qna', which is responsible for 'Allow document uploads'.
9.  Verify that it is set to 'true' for both assistants \(since it was selected in the steps above\).
10. In the same table, search for 'streaming\_enabled' and 'web\_search\_enabled'.
11. Verify that they're also set to 'true' for both assistants.
12. Navigate to **All** &gt; **Designer**.
13. From the 'Select assistant' drop-down list, select **Now Assist Panel - Platform \(default\) assistant**.
14. Select the **Test assistant** button.
15. Observe that the test panel opens, and the values of 'Allow web search', 'Allow response streaming', and 'Allow document uploads' are shown as 'Active'.
16. From the 'Select assistant' drop-down list, select **Now Assist in Virtual Agent \(default\) assistant**.
17. Select the **Test assistant** button.
18. Select one of the available chat options.

 Expected behavior: In the assistant test panel, the values of 'Allow web search', 'Allow response streaming', and 'Allow document uploads' are shown according to the actual values set in the 'sys\_now\_assist\_deployment\_config\_attributes' table.

 Actual behavior: The test panel opens, and the values of 'Allow web search', 'Allow response streaming', and 'Allow document uploads' are shown as 'Inactive'.

</td></tr><tr><td>

Virtual Agent

 PRB1975617

</td><td>

Failing to send an agent joined message

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1976846

</td><td>

SessionManager/ qlueSessionTo ChannelSessionMap caches rhino objects, contributing to higher heap memory usage

</td><td>

Even if it's using a cache of 100, each item takes between 8-10 MB, causing the overall memory consumption to spike to over 800 MB.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1979890

</td><td>

Handle an error in VoiceTranscriptServiceImpl

</td><td>

VoiceTranscriptMessage isn't setting the source, causing an error message: 'Exception occurred while adding the message: Cannot invoke "com.glide.cs.qlue. entities.MessageSource .name\(\)" because the return value of "com.glide.cs.qlue. entities.Message.getSource\(\)" is null'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1981015

</td><td>

Page context is not saved to Glide \(from off-Glide\)

</td><td>

Promoted skills should be sent to the client using a rest API.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1981262

</td><td>

Conversation cache invalidation from Glide

</td><td>

In cases of conversation state changes like abandoned conversation, faulted, or canceled, the cache should be flushed.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1982394

</td><td>

Topic block tool execution isn't running correctly

</td><td>

There's two problems. One, topic block rich control messages aren't sent back to OGCS. Two, the topic block's inputs aren't sent by AO/MCP.

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

 Logs have an unknown field document\_id in sys\_cs\_provider\_application exception for every Teams request.

</td></tr><tr><td>

Virtual Agent

 PRB1984139

</td><td>

Update permissions on the sys\_cs\_message\_last\_read and sys\_cs\_skill\_context tables

</td><td>

Cache writer operations fail with errors.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1984463

</td><td>

Client isn't loading during an upgrade

</td><td>

During an upgrade, the upgrade schema Web Client chat isn't loading.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1985779

</td><td>

Fallback option labels are missing in assistant configuration

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1986915

</td><td>

Attachment uploads fail for users without elevated privileges

</td><td>

 

</td><td>

 

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

 PRB1979942

</td><td>

Implement granular feedback functionality for NAVA

</td><td>

 

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

Walk-Up Experience

 PRB1965546

</td><td>

In Service Operations Workspace \(SOW\), navigating to location kiosks doesn't return any results

</td><td>

This is an issue with the Walk-up Experience.

</td><td>

1.  Provision a Yokohama instance with the latest version of the Walk-up plugin installed with demo data.
2.  Add two kiosks for walk-up location 'Santa Clara Tech Lounge'.
3.  Impersonate a user who is part of the group 'Santa Clara Tech Lounge'.
4.  Access either SOW or Platform.

 Expected behavior: Two kiosks are returned.

 Actual behavior: No results are returned.

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

 PRB1971900

</td><td>

If a document has modified content controls with track changes turned on, document generation fails when Sync Document is performed

</td><td>

 

</td><td>

1.  Do the required template setup.
2.  Generate an NDA request.
3.  Download the first version of the contract document generated.
4.  Turn on the track changes mode.
5.  Modify the content control like start date/company legal name.
6.  Save it.
7.  Create a new revision with this new document.
8.  Modify the same field \(start date/ company legal name\) in CMR.
9.  Select **sync document**.

 See that sync metadata and signatories fails with error: 'class org.docx4j.wml.RunIns cannot be cast to class org.docx4j.wml.ContentAccessor \(org.docx4j.wml.RunIns and org.docx4j.wml.ContentAccessor are in unnamed module of loader...\).

</td></tr><tr><td>

Work Order Management

 PRB1926871

</td><td>

When the task's location and agent doesn't have a timezone, the system timezone should be used

</td><td>

This would keep the Dispatcher Workspace behavior in sync with platform behavior. All places across the platform use the system timezone whenever there is no explicit timezone specified on the location record or agent record.

</td><td>

1.  Make sure the dispatcher is in the US/Eastern timezone.
2.  Make sure the system is in the US/Pacific timezone.
3.  As the dispatcher, view agents and tasks on DWS.

 Observe that the US/Eastern timezone is seen if the agent/task doesn't have a timezone. If the user opens that record on workspace or platform view, the default timezone is shown as US/Pacific, honoring the system timezone.

</td></tr><tr><td>

Work Order Management

 PRB1975195

</td><td>

Skipped business rule issues during Schedule Optimization \(SO\) updates

</td><td>

Business rules are skipped or not skipped incorrectly during/after SO due to edge cases not being handled in the current logic to evaluate if SO is making the update, and due to workflows being turned off when locked tasks are updated.

</td><td>

 

</td></tr><tr><td>

Zero Trust Access

 PRB1976242

</td><td>

There's a security constraints access prevention issue after enabling zero trust access when opening a VTB dashboard

</td><td>

 

</td><td>

1.  Provision an instance with the 'Zero trust access' plugin installed.
2.  Enable the ZTA property \(glide.authenticate. session\_access. enabled\).
3.  Navigate to vtb\_board.list.
4.  Open any dashboard having a condition with a date-time filter.
5.  Select **Show board** under related links.

 Expected behavior: The VTB board should load and the session should remain with the roles the user is entitled for that session.

 Actual behavior: Users observed a security constraints access 403 error for any subsequent action.

</td></tr><tr><td>

Zing Text Indexing and Search Engine

 PRB1972145

</td><td>

The query is slow from the TS Index Stats job from the getTableList method

</td><td>

The 'TS Index Stats' job executes some code to get a list of extension tables to index for a given base table. To do this, it executes an expensive aggregate query against the base table, grouping by the **sys\_class\_name** field. This doesn't scale well and can cause queries to run long, which impacts overall database and instance performance.

</td><td>

1.  Navigate to a large CMDB or SYS\_IMPORT\_SET\_ROW table.
2.  Run the TS Index Stats job.

 Expected behavior: The job runs quickly.

 Actual behavior: The job runs slowly as these extended tables grow in size.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 5](zurich-patch-5.md)
-   [Zurich Patch 4 Hotfix 5](zurich-patch-4-hf-5-PO.md)
-   [Zurich Patch 4 Hotfix 4a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2727535)
-   [Zurich Patch 4 Hotfix 4](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2706229)
-   [Zurich Patch 4 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2695190)
-   [Zurich Patch 4 Hotfix 1](zurich-patch-4-hf-1.md)
-   [Zurich Patch 4](zurich-patch-4.md)
-   [Zurich Patch 3 Hotfix 3](zurich-patch-3-hf-3-PO.md)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


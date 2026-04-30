---
title: Xanadu Patch 5
description: The Xanadu Patch 5 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-01-10"
reading_time_minutes: 46
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 5

The Xanadu Patch 5 release contains important problem fixes.

-   **Xanadu Patch 5 was released on January 10, 2025.**
    -   Build date: 12-31-2024\_0455
    -   Build tag: glide-xanadu-07-02-2024\_\_patch5-12-24-2024\_

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X05.00.xlsx).

## Overview

Xanadu Patch 5 includes 179 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp5.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 5 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 5, refer to [KB1724046](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1724046).

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

Code Signing

 PRB1783883

 [KB1710348](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710348)

</td><td>

LoggerConfiguration access privileges doesn't allow creation of a source record for Log Export Service

</td><td>

Despite an upgrade, when a user tries to create a LES source record, they get the message: 'Execute operation on script include 'LoggerConfiguration' from scope 'Log Export Service' was denied. The application 'Log Export Service' must declare a cross scope access privilege. Please contact the application admin to update their access requests. Error MessageSomething went wrong with the configuration setup. Please try again later by setting active to true and updating the record'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1813296

</td><td>

A subflow reference input comes in as a JSON instead of a reference

</td><td>

Whenever a group record is passed via flow to sub-flow, it displays an error as 'Skipping approvals due to invalid rule: ApprovesRejectsAnyG'. Passing a record to a subflow isn't constant and is coming through as a JSON. This isn't just isolated to ApprovalRules.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1813626

</td><td>

Remove the protection policy from the left navigation modules/menu

</td><td>

Since the left navigation module 'Process Mining' has a read-only policy applied, users aren't able to modify. The user wants to make the menu to be visible to only their admin users.

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB1804838

 [KB1705523](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705523)

</td><td>

New fields with double byte characters aren't created automatically on loading data

</td><td>

If the loading file or data source contains headers that don't match the fields in the import set table, when loading data, new fields are created. Since the Xanadu release, new fields aren't created when headers contain double byte characters, and a warning message is logged in the import log. This occurs even if com.glide.use\_column \_name\_optimizer property is 'true'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Time Card Management

 PRB1809013

</td><td>

The widget 'timesheet-week-breakdown' doesn't display hours on the Time Sheet portal

</td><td>

In the Time Sheet portal, the widget timesheet-week-breakdown doesn't display hours when a non-numbered task is added to a time sheet. This issue was noticed in Xanadu.

</td><td>

1.  Navigate to a base instance.
2.  Impersonate an admin user.
3.  Open the Time Sheet portal.
4.  Navigate to **Admin** &gt; **Other** &gt; **Add to Time Sheet**.
5.  Enter a number of hours for any day.
6.  View the number of hours daily breakdown.

Observe that there are no hours displayed.

7.  Add a numbered task to the time sheet.
8.  Add hours to the same day as a non-numbered task.

 Notice the number of hours in the daily breakdown, and that the hours are displaying correctly.

</td></tr><tr><td>

Visual Task Boards

 PRB1765065

</td><td>

ChecklistItemResponder is too slow to efficiently scale normal usage of the platform, resulting in backlog in the record watcher queue

</td><td>

ChecklistItemDAO has the functions canRead/canDelete that triggers base instance ACLs.

</td><td>

Trigger the ChecklistItemResponder with a check list that has 50+ items.

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

\[Deprecated\] Process Mining Guided Project Setup

 PRB1790547

</td><td>

When creating a project, added breakdowns aren't displayed

</td><td>

 

</td><td>

1.  Navigate to the 'Set objectives' page to create a project.
2.  Navigate to the 'Scope Your Analysis' page.
3.  Add breakdowns.

 Expected behavior: Breakdowns should be displayed.

 Actual behavior: Observe that the added breakdowns aren't displayed on the breakdowns page. It doesn't display even after refreshing from the breakdown page.

</td></tr><tr><td>

Adaptive Authentication

 PRB1657050

</td><td>

The 'Trusted Mobile Device' filter should also be used in the Post Authentication context

</td><td>

After creating a policy in the Post Authentication context with allowed IP ranges and Mobile App conditions, a user with a trusted, registered device should be able to log into the instance from the Now Mobile App. Currently, the login fails when the user uses a registered device with an IP that isn't allowed. The 'Trusted Mobile Device' filter can be used pre-authentication, but should also be supported post-authentication.

</td><td>

1.  Search for 'Post Authentication context' with the application navigator.
2.  Navigate to the **Post Authentication context** module.
3.  Create a policy in the Post Authentication context with allowed IP ranges and Trusted Mobile App conditions.
4.  Enable Adaptive Authentication and Device Trust on the instance.
5.  Select **User Profile.**
6.  Select **UI action.**
7.  Register a trusted mobile device.
8.  Notice that it displays a QR code to register the device.
9.  Open the NowMobile app.
10. Register the device by scanning the QR code.
11. Log into the instance from the Now Mobile app after registering the device.

 Expected behavior: The user should be able to login to the instance, as the user has registered the device, and post-authentication policies should pass and allow the user to log into the instance.

 Actual behavior: The user login fails from the registered device from an IP that is not allowed when the 'Trusted Mobile' filter is used in post-authentication.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1823277

</td><td>

Move external QueueID from the 'External Routing' plugin to the main AWA plugin

</td><td>

The **ExternalQueueID** field should be present in the main AWA plugin, but isn't.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1823284

 [KB1743632](https://hi.service-now.com/kb_view.do?sysparm_article=KB1743632)

</td><td>

There's 'Fix ErrorMessages' in UpdateSegment when 'confirmed on' is passed

</td><td>

Users see an error: 'Script execution error: Script Identifier: null.null.script, Error Description: undefined is not a function., Script ES Level: 0 Evaluator: com.glide.script.RhinoEcmaError: undefined is not a function.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1824092

</td><td>

Work items aren't counting towards the capacity recalculation total when they are matched with an agent but not yet offered

</td><td>

This can lead to an agent being assigned extra work during the next assignment round due to having an artificially low workload.

</td><td>

1.  On a multi-node instance, set up a scenario with an agent who is available on an AWA service channel and has a max capacity of 2.
2.  Create a large backlog of new interactions to route to this channel.
3.  Write a business rule to add a 10 second delay before awa\_work\_item updates that set the **assigned\_to** field.
4.  As the agent, go online and accept the 2 work items as they are offered.
5.  Close one interaction.
6.  Wait a few seconds, then close the other interaction.

 Expected behavior: Exactly 2 more work items appear in the inbox.

 Actual behavior: The agent may be offered 3 work items.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1831774

</td><td>

If the form is customized before the external routing plugin is enabled, an external field doesn't get added to a 'Queue' form

</td><td>

 

</td><td>

1.  Enable the 'Agent chat' plugin.
2.  Add the **external\_id** field to the queue.
3.  Now enable the 'External routing' plugin.

 The **External** field doesn't get added to the 'Queue' form.

</td></tr><tr><td>

Agent Chat

 PRB1802338

</td><td>

Auto-flush on the 'Conversation' table \(sys\_cs\_conversation\) causes issues with displaying the conversation history for agents in the chat window

</td><td>

The agent should still be able to view conversations that were not deleted or were created after the auto flush was run.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1831019

</td><td>

The API call to fetch the skill configuration of the WWNA component should be done if Now Assist is enabled

</td><td>

 

</td><td>

1.  Access an instance without Now Assist capabilities enabled.
2.  Open Agent Chat.

 Expected behavior: The extra call should not occur.

 Actual behavior: There is a network call to render the Now Assist Context Menu \(NACM\), formally known as WWNA, component that is not necessary.

</td></tr><tr><td>

AI Search

 PRB1766750

</td><td>

UX should respect timeouts on asynchronous Genius results

</td><td>

The UI doesn't short circuit and display 'request timed out' or something similar. This may cause issues if the asynchronous LLM request fails for some reason and doesn't send back a response. It causes the page to continuously display a loading effect.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1785906

</td><td>

The list value is not indexed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1792826

</td><td>

The search preview link doesn't take into account 'New Condition' from an indexed source

</td><td>

 

</td><td>

1.  Add two conditions in an indexed source \(new criteria\).
2.  Open a search source that uses that indexed source.
3.  Select the 'Preview' link.

 Observe that the search source conditions aren't combined correctly with the indexed source conditions.

</td></tr><tr><td>

AI Search

 PRB1794353

</td><td>

v\_search\_genius\_result becomes unreadable after opening a v\_search\_genius\_result ACL

</td><td>

AI Search stops rendering Genius Results after opening a v\_search\_genius\_result ACL record. A Null Pointer Exception \(NPE\) is observed in the system logs.

</td><td>

1.  Search with an AI Search search application and confirm the observation of Genius results.
2.  Open the 'Access Controls' table \(sys\_security\_acl\).
3.  Search for any v\_search\_genius\_result ACL and click into it.
4.  Search again.

 Observe that the Genius results are no longer rendering.

</td></tr><tr><td>

AI Search

 PRB1801325

</td><td>

Second tier feedback for negative feedback on Genius Results is not always presented

</td><td>

 

</td><td>

1.  Provision a Xanadu instance with AI Search enabled for /sp.
2.  Execute a search that triggers a Catalog Item Genius Result, preferably two in the carousel.
3.  As quickly as possible, select the thumbs down on the first Genius Result.
4.  Notice that it shows the thank you message without displaying the options to describe why the feedback is negative.
5.  Select the other result in the carousel, select the thumbs down, and notice that it works as expected.

</td></tr><tr><td>

AI Search

 PRB1802473

 [KB1704430](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704430)

</td><td>

Tab counts change for all the tabs when users select from 'All' to another tab

</td><td>

Tab counts also change on pagination.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1805031

</td><td>

The Global Search icon is incorrectly colored when a dark banner is used

</td><td>

 

</td><td>

1.  Provision an instance with Zing search enabled.
2.  Create a theme using Theme Builder.
3.  Change the primary color to black.
4.  Select **Experience Preview - Unified Navigation App**.
5.  Reduce the browser window width to display the search icon \(instead of the search bar\).

 Notice that the search icon isn't styled according to the other elements \(and isn't visible\).

</td></tr><tr><td>

AI Search

 PRB1820883

</td><td>

User context boost does not work for sys\_user.country and sys\_user.location.state

</td><td>

 

</td><td>

1.  Navigate to a search profile.
2.  Create a location boost rule.
3.  Add a positive boost action based on user context.
4.  Select **sys\_user.country**.
5.  Make sure that the sys\_user record has the proper fields set.
6.  Save the rule.
7.  Publish the profile.
8.  Search from any portal.

 Observe that the search result is not boosted as per user context.

</td></tr><tr><td>

AI Search

 PRB1830291

</td><td>

The 'AsyncEmbedding IngestionStatusHandler' connection is not updated when the AI Search connection URL is updated

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1832346

</td><td>

Selecting search results adds a parameter 'SearchTerm', which leads to a 404 error

</td><td>

With AI Search enabled, searching on the portal leads to a 404 page not found error. This happens when search results that happen to be external links are presented in the search results. When a search result is clicked, an additional parameter is added to the URL: '&amp;searchTerm='. This additional parameter causes the 404 error.

</td><td>

1.  Navigate to a Xanadu instance.
2.  Add an external link to the AI Search source.
3.  Navigate to /esc portal.
4.  Search for the external link term.
5.  Select the top search result.
6.  Observe that the external link is added to URL.

 Expected behavior: The user lands on the external link.

 Actual behavior: The user lands on a 404 page not found error.

</td></tr><tr><td>

AI Search

 PRB1835345

</td><td>

Users are unable to kick off ingestion when the index source has a semantic index configuration on one of its child tables

</td><td>

 

</td><td>

1.  Open a catalog index source.
2.  Create a semantic index configuration.
3.  Add a new component field mapping for the **Name** field with the source 'pc\_hardware\_cat\_item'.
4.  Start ingestion.

 Observe that ingestion does not start and there are errors in the log.

</td></tr><tr><td>

AI Search

 PRB1837962

</td><td>

When a query is performed in 'OR' mode, the pagination breaks

</td><td>

0 results are returned.

</td><td>

1.  Change the property 'glide.ais.query.search\_operator' to 'OR'.
2.  Perform a search on Service Portal that returns more than 12 results.
3.  Select the **Next page** arrow button.

 Observe that there's no matches.

</td></tr><tr><td>

Analytics Data API

 PRB1778742

</td><td>

Some breakdown elements filters aren't applied to the widget

</td><td>

 

</td><td>

1.  Install a PPM Standard plugin along with its demo data.
2.  Run the data collector jobs.
3.  Open Portfolio Analytics.
4.  Open the 'Summary' tab.
5.  Open the Portfolio Manager filter and apply a user.

 Expected behavior: The filter should be applied to all the widgets on the page.

 Actual behavior: The filter isn't applied for the first row widgets.

</td></tr><tr><td>

Analytics Export API

 PRB1813585

</td><td>

Add support for https/snowk8s in Highcharts and glide-whtp

</td><td>

 

</td><td>

 

</td></tr><tr><td>

API Usage Analytics Dashboard

 PRB1830743

</td><td>

There's a duplicate transfer-encoding header

</td><td>

The issue occurs for custom API/tables, with the x\_ in the URI. An error is listed in the logs.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1822879

</td><td>

In the case of a combination of hosted plugins with app customization, the existing higher version host app store plugin object isn't used

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1822973

</td><td>

Record watcher \(RW\) exceptions out when it encounters an invalid record and fails to execute responders, which can cause flows to stall

</td><td>

This is seen so far in case of indirect responders when trying to get indirectly watched records. During this, when the RW encounters an invalid sys\_id, IllegalArgumentException is thrown. This causes RW to not execute any responders matching that condition and can cause flows to be stuck in case there is a flow responder watching the same condition.

</td><td>

1.  Create an indirect responder on a task table with the condition ref\_problem.stateISNOTEMPTY.
2.  Set the sys\_id of a change\_request record to be –1.
3.  Update the state of a sc\_task record.

 Observe that the issue is triggered.

</td></tr><tr><td>

Audit History

 PRB1793551

</td><td>

A null object returned by HistoryChangeList Iterator should be handled

</td><td>

For an impersonated user, and only on certain records of a table, a calendar displays as empty. For other records of the same table, the calendar was populated as expected.

</td><td>

1.  In any audit-enabled table, add a custom column.
2.  Open any record.
3.  Update the custom column field value along with one or more other fields.
4.  Delete the column from the table.
5.  Impersonate a user and navigate to the record.
6.  Open **History** &gt; **Calendar**.

 Notice the calendar is empty.

</td></tr><tr><td>

Audit History

 PRB1837362

</td><td>

NoBroadcast\(\) logs are consumed by Log Export Service \(LES\) topics

</td><td>

In Xanadu, the persistence layer was updated to optimize database connection pool management, and new calls to Log.xxxNoBroadcast were introduced within the critical section. The expectation was that these calls would remain isolated and would not interact with the database. However, due to a downstream issue in the LogExportService Hermes API logic, database calls were inadvertently made during the same Log API calls, resulting in a deadlock.

</td><td>

1.  Install the LES application,
2.  Create a source with 'Table' as the node table.
3.  Verify that NoBroadcast\(\) logs are also consumed.

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1824649

</td><td>

Capacity metrics data is cleared when running the capacity scheduled job in the case of buckets

</td><td>

Additionally, appointment booking through the platform is creating duplicate capacity usage.

</td><td>

1.  Log in as admin and run the scheduled job 'Compute Capacity Demand Metrics Data'.
2.  Log in as an Field Service Management \(FSM\) territory planner.
3.  Navigate to CSM or FSM configurable workspace.

 On the homepage capacity dashboard, 'Field Service Territory Capacity Analytics' under the 'Capacity gap analysis' for territory, the assigned capacity data should be accurate and not all zeros.

</td></tr><tr><td>

Change Management

 PRB1801143

</td><td>

There's a URL truncation issue in change request copies

</td><td>

There's a URL truncation issue in change request copies due to large fields in the com.snc.change\_ request.copy.attributes property, leading to a missing **chg\_model** field if it is in the end of the list.

</td><td>

1.  Edit the change properties for 'com.snc.change\_request.copy.attributes'.
2.  Add 'justification,implementation\_plan' to the list.
3.  Move the **chg\_model** field to the end of the list.
4.  Create an emergency change.
5.  Populate the **Description**, **Justification** and **Implementation Plan** with lots of information.
6.  Save the record.

</td></tr><tr><td>

CMDB to CSDM Data Synchronization

 PRB1822499

 [KB1710540](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710540)

</td><td>

Life Cycle Control records are missing for a CMDB base table to allow the use of the 'End of Operation' stage

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Condition Builder

 PRB1776650

</td><td>

Unable to dot-walk into a reference field when configuring report conditions

</td><td>

Unable to dot-walk into a reference field when configuring report conditions since the Washington DC upgrade uses JAWS 2024 screen reading software.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1819137

</td><td>

Data Manager doesn't support dot-walk fields for task assignment

</td><td>

 

</td><td>

1.  Create a Data Manager policy.
2.  Try and set task\_management\_user or task\_management\_group to a dot-walked field.

 Notice that since it's a reference to sys\_dictionary, this isn't possible.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1828632

 [KB1710838](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710838)

</td><td>

The de-duplication task for lookup records isn't created with correct information

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1830256

</td><td>

If eligible records are more than batch size, certification audit results are duplicated for failed CIs

</td><td>

The checkTableAttributes AgainstTemplate method doesn't respect the current batch it is running in. It instead queries the entire CI class tables and logs the failed results.

</td><td>

1.  Create more than 1000 records in CI tables, like cmdb\_ci\_linux\_server or cmdb\_ci\_business\_app.
2.  Update any of the attributes, like cmdb\_ci\_linux\_server.os\_version or cmdb\_ci\_business\_app.active\_user\_count, to a particular value for half of the records
3.  Configure cert\_audit where certification attributes match half the records updated in step 2. Use only 1 attribute to certify.
4.  Run the audit.

 Expected behavior: The number of records in the cert\_audit\_results table shouldn't be more than one.

 Actual behavior: The total\_num\_records/1000 +1 times the results get duplicated for failed results.

</td></tr><tr><td>

Core Platform

 PRB1732676

 [KB1587782](https://hi.service-now.com/kb_view.do?sysparm_article=KB1587782)

</td><td>

The variable $\{comments\_and\_work\_notes\} isn't working for HR cases after an upgrade to Vancouver

</td><td>

After upgrading to Vancouver, email notifications with $\{comments\_and\_work\_notes\} are displaying as empty in the recipient's email. This works fine in Tokyo instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Crew Operations

 PRB1823861

</td><td>

Dynamic crew creation fails and the Dynamic Scheduling modal throws an error instead of identifying the proper filter

</td><td>

The same name for the variable and function was being used. As a result, the function call was overwritten by the variable in the extension point call. It fails and does not create the Dynamic Crew because it not able to get the function.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1765194

</td><td>

Database view's list query throws a syntax error when the language is set to Japanese

</td><td>

The error message is a syntax error or access rule violation detected by the database unknown column 'sys\_translated\_text2.name' in 'where clause'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1808839

</td><td>

Update related to PRB1762005, changing the column name octet\_length to below 63

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1765297

</td><td>

Enable extended tables for DMTableCleaner

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1800693

</td><td>

Create chunks based on the records eligible for deletion

</td><td>

Currently, hex cleaners create an enormous amount of chunks, even when a table has few records to delete. For example, on a clean up from a table with 70 million rows, the hex cleaner will create 65,000 chunks.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1721884

</td><td>

Tables without PK cause group replication errors in MySQL 8

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1749770

</td><td>

The size of tuple values received from the server should be limited

</td><td>

As a result of the size of these values, there's out of memory error restarts on surf far nodes.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1788274

 [KB1720975](https://hi.service-now.com/kb_view.do?sysparm_article=KB1720975)

</td><td>

There's incorrect results when a statement is closed while another statement is executing

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1793961

</td><td>

Use Log.infoNoBroadcast in RowList and RowBlock

</td><td>

Log.infoNoBroadcast is used in RowBlock, which could potentially trigger database queries. It is always executed as a nested query \(i.e., another query is still being executed and fetched\). This could potentially affect the enclosing query.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1773095

</td><td>

Links break in variable set records when the page is translated to a non-English language

</td><td>

The links in a variable set record don't work when the **Title** field isn't translated in a non-English language.

</td><td>

1.  Activate the Japanese language plugin \(com.snc.i18n.japanese\).
2.  Make sure the language is set to English.
3.  Navigate to sc\_cat\_item table.
4.  Create a catalog item.
5.  In the 'Variable Sets' related list, select **New**.
6.  Create a variable set \(for example, a single-row variable set\).
7.  Fill in the **Title** \(for example, Language test\) and other mandatory fields, then submit.
8.  Navigate back to the catalog item record.
9.  Scroll down to 'Variable Sets' related list.
10. Notice that the Variable Set 'Language test' link is working.
11. Switch the language to Japanese and check the variable set 'Language test' link again.

 Expected behavior: The link should work as same in English mode.

 Actual behavior: The link isn't working.

</td></tr><tr><td>

Database Persistence

 PRB1833850

</td><td>

Logging in critical sections of DBConnectionPool can cause deadlocks

</td><td>

This becomes a serious issue if a message is logged in a critical section while holding a lock.

</td><td>

 

</td></tr><tr><td>

Date Picker

 PRB1820680

</td><td>

Workspace date pickers are not respecting the language codes for pt-BR and fr-CA

</td><td>

When the user session language is either Portuguese Brazilian \(pt-BR\), or French Canadian \(fr-CA\), all date pickers in all workspaces in Xanadu are displaying in English.

</td><td>

1.  Set up a Xanadu environment.
2.  Install com.snc.i18n.brazilian\_portuguese and com.snc.i18n.portuguese.
3.  From the homepage, navigate to **Workspaces** &gt; **Service Operations Workspace**.
4.  Select the 'List' icon.
5.  Navigate to **Incidents** &gt; **All**.
6.  Select an open incident.
7.  Select the 'Details' tab.
8.  Change the language to Portuguese.
9.  Select any date picker.
10. Observe the date picker is displaying in Portuguese.
11. Change the language to Portuguese Brazilian.

 Observe the date picker is displaying in English.

</td></tr><tr><td>

Discovery

 PRB1833554

</td><td>

IP exclusion does not work as expected when the schedule contains an IP net-mask alone

</td><td>

If at least one IP list is added to the original schedule which had only subnet, exclusions work as expected.

</td><td>

1.  Create a discovery schedule.
2.  In quick ranges \(or otherwise\), add an IP using a subnet mask alone. Do not add any other type.
3.  Add IP exclusion records that are supposed to exclude the whole range above or partial \(that would exclude something from the above range\).
4.  Trigger discovery.

 Observe that the IP exclusion does not occur, despite the record types \(IP list, range, sub net masks - are used for exclusion\).

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1781359

</td><td>

Document Intelligence upgrade causes data migration to fail when the instance is in a non-English language

</td><td>

 

</td><td>

1.  Choose a different language in the preferences.
2.  Upgrade to Washington, Vancouver, or a release higher than Utah, where the Document Intelligence new table schema \(sys\_di\_ schema\) are used and tasks have to be migrated for every use case.

 The migration fails, and the model will not be trained. As a result, tasks, when processed, also fail.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1800115

</td><td>

If a migration task fails for a task definition failure, the upgrade of the task definition should not proceed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1828370

</td><td>

The **Show in Docintel** button is not visible for QnA tasks

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Dynamic Translation

 PRB1825179

</td><td>

Users get an error message when creating the setting as part of the localization framework

</td><td>

The error message: 'Translator version should be V3'.

</td><td>

1.  Install the localization framework installer.
2.  Navigate to the 'Settings' page.
3.  Create a setting by providing all the required fields.
4.  Provide the translator as any active translator.

 Expected behavior: The setting is created.

 Actual behavior: The setting isn't created and users get an error message: 'Translator name version should be V3'.

</td></tr><tr><td>

Dynamic Translation

 PRB1832033

</td><td>

When a translatorID is sent as null to an exclusion framework API, it's not returning the input texts in the output in Now Assist

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1824698

</td><td>

Notifications are sent to multiple users' personal email addresses

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Employee Relations Case Management

 PRB1830223

</td><td>

HR users are unable to add or view attachments on Employee Relations cases in HR Agent Workspace

</td><td>

When HR users try to add attachments to an Employee Relations case in HR Agent Workspace, the attachment disappears and they are unable to view all previous attached documents. If users view the same Employee Relations record in HR Agent Workspace as an admin, they can view all of the attachments that the HR user tried to add.

</td><td>

 

</td></tr><tr><td>

Field Normalization

 PRB1817181

</td><td>

The coalescer job reads an arbitrary number of sys\_ids into memory

</td><td>

Coalescer::getGoatReferences reads sys\_ids into memory with no limit. Meaning that for large enough tables, this job can easily bring down a node.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1814758

</td><td>

During Async HTTPClient initialization, there's reinitialization for every time in RESTStep

</td><td>

 

</td><td>

1.  Navigate to a Washington DC instance.
2.  Create an FDIH Action with a REST Step performing a POST on a Now LLM endpoint.
3.  Add some telemetry around this REST step.
4.  Run the action.
5.  Look in the node logs or outbound HTTP request log table and compare it to the telemetry.

 Expected behavior: There shouldn't be much of a difference between these numbers.

 Actual behavior: There's persistent 250ms-500ms delta between these numbers.

</td></tr><tr><td>

Flow Engine

 PRB1817474

</td><td>

An error message exists even after a retry is successful and the status code is 200

</td><td>

When an action is executed with a retry policy and the initial call/s failed, the rest step output has an error message. However, after certain attempts once it's successful, the status is 200. It also displays an error message.

</td><td>

1.  Create any rest action with the retry policy.
2.  Execute for failure for the initial 2 or 3 calls.

Observe that there's an error message.

3.  On runtime, do the appropriate changes so that action starts to work fine and returns 200.

 Even after updating to 200, the error message is still there.

</td></tr><tr><td>

Flow Engine

 PRB1832181

</td><td>

Password2 decryption fails in Engine V2 after returning from the MID server

</td><td>

The re-encryption for Password2 data when sending to MID aren't re-encrypted for Glide, which is causing the decryption to fail.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1784060

</td><td>

The 'System logs' table is flooded with the message 'Flow Designer: Credentials sys\_id'

</td><td>

The 'System logs' table is flooded with the log: 'Flow Designer: Credentials sys\_id: 41b53612c3fce5 d087d34f45df0131b6'.

</td><td>

1.  Navigate to the 'System logs' table.
2.  Check the logs.

</td></tr><tr><td>

Form Controller

 PRB1826786

</td><td>

Base input fields aren't displayed for Now Assist for Configure Management Database \(CMDB\)

</td><td>

The 'Choose Inputs' section is blank and throws an error when the user attempts to enable the CI summarization skill for CMDB.

</td><td>

Navigate to **Now Assist for Admin** &gt; **Features** &gt; **CMDB** &gt; **View details** &gt; **CI Summarization** &gt; **Close inputs.**

 Notice that base inputs are blank, and an error is thrown.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1807377

</td><td>

There's a canvas error on policy records in Compliance Workspace

</td><td>

When opening a policy text for a policy record in Compliance Workspace, it throws an error: 'Canvas Error'.

</td><td>

1.  Open Compliance Workspace.
2.  Navigate to 'List'.
3.  Select **All policies** under 'Compliance Library'.
4.  Create a policy record.
5.  Connect the policy with a document present in OneDrive.
6.  Select **Update link** from the 'Policy text' tab.
7.  Turn off the sync.

 Observe the 'Canvas error' when sync is toggled off in the 'Policy text' tab.

</td></tr><tr><td>

Group and Action Framework - Family

 PRB1834954

</td><td>

Support text as the similarity API input

</td><td>

The similarity API needs to support text similarity. Currently, it can provide similarity between incidents when two sysIDs, or free text and sysID of record is passed.

</td><td>

 

</td></tr><tr><td>

Guided Tours

 PRB1784409

</td><td>

The guided tours API returns java.lang.ArrayIndex OutOfBoundsException

</td><td>

It throws a 500 internal server error.

</td><td>

1.  Provision an instance with the Major Incident Management plugin with demo data installed.
2.  Navigate to Service Operations Workspace.
3.  Access one major incident from the list.
4.  Navigate to the 'Communicate' tab.
5.  Create a task with email as an option.
6.  Select **Compose**.

</td></tr><tr><td>

Guided Tours

 PRB1790101

</td><td>

A guided tour displays 'Undefined' when trying to stop auto-launching a tour in HR Agent Workspace

</td><td>

 

</td><td>

1.  Ensure that com.sn\_hr\_agent\_ws for Agent Workspace for HR Case Management is installed.
2.  Create a guided tour and provide the below information:
    1.  Name: provide-name
    2.  Tour Type: Workspace
    3.  Select **Manual Selection**
    4.  Starting page: now/hr/agent/home
    5.  Select **Create Tour**
3.  Open a browser.
4.  Ensure to close all the existing opened tabs first.
5.  Clear the entire cache and history of the browser.
6.  Log in to a Vancouver instance.
7.  Navigate to the HR Workspace home page.
8.  Wait for the tour to auto launch.
9.  After the tour pop-up displays, select the **x** button.

 Notice that it's displaying 'undefined'.

</td></tr><tr><td>

Haraka \(Glide\)

 PRB1824231

 [KB1709920](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709920)

</td><td>

sys\_kagami\_query\_engine has an error on the column decision\_last\_msg

</td><td>

Queries are not routing to postgreSQL after upgrading to Xanadu. Queries with 'group by' are attempting to route to Haraka, but are failing due to a syntax error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1827423

</td><td>

Elasticsearch \(ES\) data input \(DI\) has slow read throughput

</td><td>

Elasticsearch data input code isn't paralleling the scroll slice calls, which means there's no option for the user to increase the reading throughput. Increasing the scroll slice count won't have any effect.

</td><td>

1.  Create an ES DI.
2.  Read from an elasticsearch index that contains more than 20k events per second.
3.  Using the default slice scroll size of 1, users shouldn't be able to read 20k per second.
4.  Increase the number of slice scrolls to 3.

 Expected behavior: Users should be able to read as fast or faster then 20k per second.

 Actual behavior: No difference in read throughput.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1804125

</td><td>

Support change from Entrust to DigiCert

</td><td>

There's a need to update the certificate generator tool to support DigiCert as part of its truststore. Currently, it only supports Entrust.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1819119

</td><td>

Clones submitted using user profiles do not exclude Hermes tables by default

</td><td>

The default settings are used when users define a custom profile for cloning. When the default value is 'false' and custom profiles are used, the exclude/preserve rules are not honored and only get applied if the value is 'true.' Because it needs to be applied always for Hermes, the default value needs to be 'true'.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1821659

</td><td>

The full topic name for longer instance names and/or topic names are truncated in the **cluster\_topic\_name** field

</td><td>

 

</td><td>

1.  Install an application that requires Hermes \(StreamConnect as an example\).
2.  Navigate to sys\_kafka\_topic.
3.  Create a topic with a long name value.
4.  The **Name** field has a 100 character limit.
5.  View the **cluster\_topic\_name** field to confirm the truncation.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1821669

</td><td>

Stability improvement to non-default Hermes services

</td><td>

An instance upgrade is bringing the instance down

</td><td>

Create multiple HermesTopic objects for the same service.

 Notice that a DB call is made each time the HermesTopic object is constructed. This impacts compute speed in production.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1834407

</td><td>

Reduce DB calls during initialization for Hermes

</td><td>

 

</td><td>

1.  Create multiple HermesTopic objects for the same service
2.  Notice that a DB call is made each time the HermesTopic object is constructed, which impacts compute speed.

</td></tr><tr><td>

History Set

 PRB1826101

</td><td>

Enabling the property 'glide.history\_set.pull\_ journal\_entries\_from \_journal\_table ' has side effects

</td><td>

Enabling the property breaks HistoryWalker API and populates '0' as the update count for journal fields in the sys\_history\_line table.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1766824

</td><td>

Non-Integration Hub \(IH\) outbound calls are counted as IH usages if a flow is called earlier in the IH transaction, even if this flow doesn't cause the outbound request

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1784518

</td><td>

The 'Retry' policy doesn't retry for a connection timeout

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1821701

</td><td>

The 'Resolve SST for MID' property is not correctly honored when flows are set to run on v1 and the major engine version is v2

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1822660

</td><td>

IBM watsonx and Coupa spoke dependency issues in properties files

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1834092

</td><td>

An image size greater than 5MB isn't able to generate the playbook

</td><td>

At a spoke level, each image is converted into base64 before sending it to LLM. It uses the getcontentBase64 API, which puts a 5MB limit and couldn't generate its base64 encoding. It sends an empty payload for an image which results in invalid image data.

</td><td>

1.  Log in with the Now Assist creator role.
2.  Navigate to Process Automation Studio.
3.  Create a new playbook with Now Assist.
4.  Add a playbook name.
5.  Upload an image size greater than 5 MB.
6.  Select the **Generate playbook** button.

 Expected behavior: It should generate the playbook.

 Actual behavior: Users get a 'Couldn't generate the playbook' message.

</td></tr><tr><td>

Issue Auto Resolution for Virtual Agent

 PRB1819544

</td><td>

Agent are unable to submit feedbacks for KBs and catalog items

</td><td>

 

</td><td>

1.  Log in or impersonate as a user.
2.  In the esc portal, search for 'General Inquiry'.
3.  Create a case with the input 'Direct Deposit setup'.

The case is assigned to an HR bot and a few KBs/Catalogs are recommended.

4.  Opt-out of the IAR flow from esc portal.

The case is assigned to an HR agent.

5.  Log in as the agent and open the HR case created in the above steps.
6.  Select **View recommendation**.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1814067

</td><td>

Cross-region move with Bagheera-auto-config enabled fails sys\_property password2 record decryption

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1819238

</td><td>

Rekey only deactivates a private key for an asymmetric module key pair, causing a discrepancy when generating a new asymmetric key pair on the target

</td><td>

The rekey flow introduced in Xanadu only deactivates and claims ownership of the private key for an asymmetric module key pair. This causes an issue in generating a new key pair on the target because the public key is active, so only a private key is created and persisted. This leads to a mismatch between the active public key and the active private key. The logic that causes this issue is in KMFRekeyManager, as it only rekeys the private key and does not check for the peer key.

</td><td>

1.  Provision two instances with clone e2e enable.
2.  On instance A, create a crypto module with an asymmetric decryption crypto spec.
3.  Generate a new key pair for the module.
4.  Clone instance A to instance B.
5.  After the clone is successful, navigate to sys\_kmf\_module\_keys.
6.  Filter by the module created in step 3

 Expected behavior: Both the private key and public key are deactivated and owned by the target instance.

 Actual behavior: Only the private key is deactivated and owned by target instance. The public key is active and owned by the source instance.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1824187

</td><td>

Post cross-region move encryption fails for modules that don't have keys

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Legacy Agent Workspace

 PRB1830809

</td><td>

Users are unable to apply recommended response templates in an /r case

</td><td>

In a scenario when the /r-keyboard shortcut is used to browse response templates and Now Assist is enabled, users are not able to apply the templates by selecting a tab in the list. This works as expected in the search scenario.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1817332

</td><td>

Non-admin users are unable to remove tags from the list view for workspaces

</td><td>

This is working in the Native UI.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1826163

</td><td>

A list declarative action isn't working in the 'New List' page template

</td><td>

 

</td><td>

1.  Create a list declarative action:
    1.  Action label: Demo
    2.  Implemented: ClientScript
    3.  Table: Incident
    4.  Script condition: console.log\('Declarative Action method'\)
2.  Navigate to Service Operations Workspace.
3.  Select the 'List' tab.
4.  Open the browser console.
5.  Select the **trigger** button.

 Observe that the console log wasn't displayed in the browser console.

</td></tr><tr><td>

List Administration

 PRB1827799

</td><td>

A filter condition in a module is displaying additional filters when opened in new tab

</td><td>

The filter condition displays backend details.

</td><td>

1.  Create a module.
2.  On a table, select 'Incident'.
3.  Add any dot-walking fields.
4.  Create a user and a system level user preference record 'glide.ui.polaris.ui16\_tabs\_inside\_polaris' as a type string and set the value to true.
5.  Impersonate a user.
6.  Navigate to a module created incident.
7.  Open the module in a new tab.

 Expected behavior: When the module is clicked to open in a new tab, only the dot-walking filters should apply.

 Actual behavior: When the module is clicked to open in a new tab, additional backend filters are applied. Observe that some additional filters are applied. This issue only happens when opening the module in a new tab. If opened in the same tab, the issue doesn't happen. If the user preference value for the user is set as false, the issue isn't observed.

</td></tr><tr><td>

List Multi-Field Edit

 PRB1819121

</td><td>

The side panel form for the **Edit** UI action cannot be opened for a second time

</td><td>

 

</td><td>

1.  Navigate to any Xanadu instance and verify that it has Service Operations Workspace \(SOW\) available.
2.  Navigate to UI Builder, create a list variant under an existing '/list' route.
3.  From 'List page template,' make sure this new variant is the default for /list.
4.  Open SOW, then navigate to **List** &gt; **Incidents** &gt; **All**.
5.  Select any record and select the **Edit** UI action.

Notice that the side panel form opens properly.

6.  Close the form and deselect the record.
7.  Navigate to **List** &gt; **Problem** &gt; **All**.
8.  Select any record.
9.  Select the **Edit** UI action.

 Notice that this time, the side panel form opens but has no content.

</td></tr><tr><td>

List Search

 PRB1763145

</td><td>

Search behavior changed to 'Starts with' in Washington DC when adding columns to a list view in configurable workspaces

</td><td>

Search behavior used to be 'Contains' in pre-Washington DC.

</td><td>

1.  Open any Utah/Vancouver instance with CSM/Configurable Workspace installed.
2.  Open CSM/Configurable Workspace.
3.  Navigate to 'Open cases' from a list.
4.  Select the cogwheel icon.
5.  Select **Edit Columns**.
6.  Start searching for any column.
7.  Observe the search behavior, which is 'Contains'. If users type the second word in a column name, search results still appear.
8.  Take a Washington DC instance and repeat the above steps.
9.  Observe that search behavior is 'Starts with', where users can't search with a second word of a column name.

</td></tr><tr><td>

MID Server

 PRB1808948

</td><td>

MIDX509TrustManager doesn't handle expired cross-signing CA root certification

</td><td>

An exception appears in the logs.

</td><td>

 

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

 PRB1814364

</td><td>

Multi-factor authentication \(MFA\)'s flow is broken after cloning from Vancouver to Xanadu

</td><td>

 

</td><td>

1.  Log in into any instance on a Vancouver release.
2.  Enable MFA.
3.  Enroll any user into MFA on this instance.
4.  Log in into any other instance on the Xanadu release.
5.  Request a clone into the above Vancouver instance.
6.  After a clone is complete, try to login into the cloned instance which was earlier on Vancouver.

 Expected behavior: The user is able to log in successfully with MFA.

 Actual behavior: The user is unable log in into the instance after the clone.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1820116

</td><td>

Applications in a configured menu don't display after the user switches domains

</td><td>

 

</td><td>

1.  Create a configurable menu \(sys\_polaris\_menu\_config\) for a domain.
2.  Add an application to the configurable menu.
3.  Switch to the domain that contains the configurable menu.
4.  Refresh.
5.  Clear the browser local storage and refresh again.

 Expected behavior: The configurable menu displays.

 Actual behavior: If there are only applications in the configurable menu, the menu doesn't display in the header. If there are also modules, the menu displays but the applications doesn't. This also applies to the default domain, but only if the user switches their domain to another and then back to the default.

</td></tr><tr><td>

Now User Experience

 PRB1817203

</td><td>

Users are unable to open a module when the **sys\_app\_module .window\_name** field has a value

</td><td>

 

</td><td>

1.  Search for any module.
2.  Open that module in the sys\_app\_module table.
3.  Check if the **window name** field is filled. If it's not, put 'Approvals'.
4.  Save the change.
5.  Refresh the page.
6.  Navigate to the filter navigation.
7.  Search for the module that was changed previously.

 Expected behavior: The module should open even if the **window name** field is filled in like it does in Washington DC.

 Actual behavior: The module doesn't open when the **window name** field is filled in.

</td></tr><tr><td>

On-Call Scheduling

 PRB1805914

</td><td>

Daily, weekly or biweekly rotation is skipped in November

</td><td>

 

</td><td>

1.  Log in as an admin.
2.  Create a full day shift.
3.  Add primary -1 week, secondary- 1 daily.
4.  Publish the shift.
5.  Navigate to the calendar.
6.  Navigate to November.

 Expected behavior: A rotation shouldn't be skipped.

 Actual behavior: A rotation is skipped.

</td></tr><tr><td>

Password Reset

 PRB1807336

</td><td>

Missing translations for the pwd\_question on the password reset enrollment page for QA verification

</td><td>

Until Washington DC, users can see the translations of questions in the sys\_translated table. Xanadu onwards those records are missing from the sys\_translated table.

</td><td>

1.  Open to the pwd\_process list view.
2.  Navigate to the default self service process.
3.  In the related list, add question-answer verification to the process.
4.  Make sure that it is set to mandatory, the process is active, and 'Apply to all' is enabled.
5.  Impersonate abel.tuter.
6.  Search for the 'Enroll' in the left navigation menu to navigate to the password reset enrollment page.
7.  Install any language plugin.
8.  As Abel Tuter, switch the language and open the enrollment page.

 Expected behavior: The questions list should be in the user's current language.

 Actual behavior: The questions list is still in English.

</td></tr><tr><td>

Password Reset

 PRB1830139

</td><td>

SMS verification isn't working in 'Service Desk Password Reset' and enrollment modules after an Xanadu upgrade

</td><td>

After an Xanadu upgrade, when verifying an added device via SMS, E.164 compliant phone numbers throw an error: 'not an E.164 compliant phone number: no thrown error'.

</td><td>

Navigate to **Service Desk** &gt; **Enrollment** &gt; **SMS Verification** &gt; **Add device** &gt; **Verify**.

</td></tr><tr><td>

Performance Analytics

 PRB1784482

</td><td>

Users who have more then 40 characters in their username can't edit a dashboard

</td><td>

Users get a 403 forbidden error.

</td><td>

1.  Create a user with a username more then 40 characters.
2.  Impersonate a newly created user.
3.  Create a dashboard.
4.  Try to edit a dashboard.

</td></tr><tr><td>

Performance Analytics

 PRB1813754

</td><td>

The v\_table\_join property is installed for upgraded users when upgrading from Vancouver

</td><td>

This issue occurs because the unified analytics plugin did not exist in Vancouver, and the com.glide.par. v\_table\_join.enabled property was delivered under an unload folder so it will be installed with a false value for certain users only. When upgrading from Vancouver to Xanadu or later, the unified analytics plugin is installed the first time and therefore the property com.glide.par. v\_table\_join.enabled is installed, when it shouldn't.

</td><td>

1.  Access an instance on Vancouver.
2.  Upgrade the instance to Xanadu or later.

 Expected behavior: The com.glide.par. v\_table\_join.enabled property does not exist.

 Actual behavior: The com.glide.par. v\_table\_join.enabled property exists and is false.

</td></tr><tr><td>

Performance Analytics

 PRB1824024

</td><td>

Platform Analytics's 'Administration' menu is missing when upgraded from Vancouver to Xanadu

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1779614

</td><td>

The PAR dashboard search isn't giving the expected results when a non-English language is set on the instance

</td><td>

User gets 'Items removed from this page due to security constraints' or 'No data to display'. Messages are in a translated language, whichever exists at that time on the user session.

</td><td>

1.  Navigate to an instance with one of the language plugin installed.
2.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Dashboards**.
3.  On 'User Preferences', set the language to English.
4.  Navigate to 'All'.
5.  Search with a dashboard name like 'change' or 'incident'.
6.  On 'User Preferences', set the language to German, or any other installed non-English language.
7.  Search with a dashboard name like 'change' or 'incident'.

The same set of dashboards that were returned in step 5 do not appear. A few dashboards are displayed and a message exists that filters out other dashboards.


 Expected behavior: The dashboard search results should be consistent in all languages.

 Actual behavior: In the English language, there's expected results but in others, the result is inconsistent.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1797830

</td><td>

Dashboard visibility filtering isn't working

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1812468

</td><td>

Classification training capability doesn't return consistent results when doing batch predictions

</td><td>

Whenever users train a classification solution on Java, whenever they do single record predict, it by default returns 10 outputs per record and is filtered on the Glide side to return the one with highest confidence, which is more than the threshold. But when doing a batch predict, it returns only one output per record. If the confidence for that output is less than the threshold, then it doesn't return any output.

</td><td>

1.  Train a classification solution on Java.
2.  Select a record such that users get an inconsistent result for a single and a batch test.

</td></tr><tr><td>

Predictive Intelligence

 PRB1821890

</td><td>

The 'Cluster Concept' text isn't aligned/missing inside the 'Cluster Concept' tile

</td><td>

The 'Cluster Concept' text isn't aligned inside the 'Cluster Concept' tile. For some cluster concepts, the 'Cluster Concept' text is completely missing from 'Cluster Concept' visualization.

</td><td>

 

</td></tr><tr><td>

Problem Management

 PRB1816736

</td><td>

The **Problem** field isn't populated in a problem task

</td><td>

When a problem task is opened from a problem record, the **Problem** field in a problem task record displays as empty.

</td><td>

1.  Navigate to an instance.
2.  Open any active problem.
3.  Navigate to the 'Problem Task' related list.
4.  Select the **New** button to create a problem task.
5.  Choose any task type from the option 'Root Cause Analysis' or 'General'.

 Observe that it opens the 'Task' page, where the **Problem** field is empty, which isn't auto-populated.

</td></tr><tr><td>

Process Mining for External Data

 PRB1812761

</td><td>

The **Edit dataset** feature is broken

</td><td>

The **Edit dataset** action on an external dataset is taking the user to Step 3 \(Record data\) instead of Step 2 \(Import data\).

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1804947

</td><td>

Root cause analysis \(RCA\) fails on the HR case table \(sn\_hr\_core\_case\) in Process Mining

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1825682

</td><td>

Mining more records than the user has access to and a record mismatch on mining summary and workbench

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1778736

</td><td>

When viewing results for a root cause analysis \(RCA\), selecting any leading influencer and applying in the workbench isn't working as expected

</td><td>

 

</td><td>

Issue 1:

 1.  Open any mined model with findings.
2.  Select the 'Action' menu for any of the findings.
3.  Run RCA.
4.  Once completed, select **View results**.
5.  Select any of the leading influencers displayed on the RCA pop-up.
6.  Select **Apply in workbench**.

 Expected behavior: The condition selected on top of the insight should be applied.

 Actual behavior: Insight alone is applied in the workbench.

 Issue 2:

 1.  From the analyst workbench ST panel, view the result for the RCA.
2.  Select any of the leading influencers.
3.  Select **Apply**.

 Expected behavior: The ST created pop-up should appear once and the screen shouldn't flicker.

 Actual behavior: The screen flickers and the 'Scheduled tasks created' pop-up displays three times.

</td></tr><tr><td>

Process Mining Workspace

 PRB1793217

</td><td>

Certain RCA/clustering is not disabled on a graph \(node and arc\) and S&amp;I with more than 100 records

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1807084

</td><td>

For external data/archived data tables, the activities and breakdown fields shown are not same as those shown on Platform

</td><td>

 

</td><td>

1.  Create an external data model.
2.  Create a project for the external data table from the process projects page.

 On the 'Scope your analysis' page, observe that the activities shown do not match with activities shown on Platform \(some are missing like 'domain,' 'tags,' etc\). Breakdowns show only the **Updates** field, whereas in Platform, breakdown fields are shown. Also for archived data, **Process Perspectives** and **Breakdown** fields \(fields representing classification of records\) do not show all the fields when compared to those shown in Platform.

</td></tr><tr><td>

Process Mining Workspace

 PRB1818056

</td><td>

In the 'Summary and Insights Improvement Opportunities' list, actions items are stuck in a loading state

</td><td>

The issue may be related to a race condition on seismic or the 'now-list' component, because it doesn't happen when the viewport is narrow or when breakpoints are added.

</td><td>

1.  Navigate to an instance.
2.  Navigate to Process Mining.
3.  Select a project that has improvement opportunities.
4.  Try to open the 'Actions' menu on the list.

 Expected behavior: A set of options should display.

 Actual behavior: 'Loading items...'

</td></tr><tr><td>

Process Mining Workspace

 PRB1819728

</td><td>

Evaluation project should turn off 'Automation Discovery'

</td><td>

When users run their Evaluation Project with 3,600 records, the 'Automation Discovery' tab should be turned off by default.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1822950

</td><td>

Contextual filters are treating string fields as reference fields

</td><td>

Users are unable to use these fields with contextual conditions.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1823726

</td><td>

The repetition filter does not work as expected for nodes with high repetitions

</td><td>

Users observe an error message 'An error occurred: Max reps cannot be lesser than 0.'

</td><td>

1.  Import an external dataset.
2.  Mine the process model.
3.  Identify a node with a high number of repetitions.

 The 'An error occurred: Max reps cannot be lesser than 0' message appears.

</td></tr><tr><td>

Process Mining Workspace

 PRB1832584

</td><td>

The 'Top 3 KPIs by \# records &amp; opportunities' widget always displays one record even though there are many

</td><td>

 

</td><td>

1.  Mine a project with findings attached to more than one KPIs.
2.  Observe the third widget.

</td></tr><tr><td>

Process Mining Workspace

 PRB1833175

</td><td>

Users are able to update a filter on an evaluation project from Guided Setup

</td><td>

The filter shouldn't be visible.

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB1764936

 [KB1645365](https://hi.service-now.com/kb_view.do?sysparm_article=KB1645365)

</td><td>

Scheduled list export with many rows fails and is sent as a PDF with an error message

</td><td>

The attachment is exported as a PDF with an error message instead of an Excel file, even though the scheduled export was set as an Excel file.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Rollback Contexts

 PRB1774870

</td><td>

Rollback is recorded for tables without a sys\_id when using StatementBatcher

</td><td>

The RollbackDBListener.java is responsible for inserting records into rollback tables, including sys\_rollback\_sequence. However, when users insert records using StatementBatcher.java, it calls RollbackDBListener.onBatch which doesn't perform the same checks. As a result, they get cmdb\_ire\_partial \_payloads\_index inserts recorded in sys\_rollback\_sequence.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1807589

</td><td>

Prevent duplicate territories in overlapping qualifier sets

</td><td>

The logic to build qualifier sets wasn't checking for duplicate primary qualifiers, resulting in duplicate qualifiers being sent in multiple sets.

</td><td>

1.  Add two overlapping territories to the same scope.
2.  Run config data query for a batch with the above scope.

 Notice that duplicate territories are sent in multiple qualifier sets in configdata. This shouldn't happen.

</td></tr><tr><td>

Schedule Optimization

 PRB1823732

</td><td>

A personal event start date is later than end date, causing SO to fail

</td><td>

 

</td><td>

1.  Create personal events from platform/workspace view.
2.  Change the start date to go beyond the end date.
3.  Run schedule optimization.

</td></tr><tr><td>

Schedule Optimization

 PRB1825269

</td><td>

The 'Optimization Solution Processor' business rule trigger is to be changed

</td><td>

The 'Optimization Solution Processor' business rule was in AFTER mode, which delayed the file uploads from SO Engine to Glide.

</td><td>

1.  Run optimization.
2.  Observe the time taken for the results from engine in the sys\_attachments table.

 Files are taking longer to upload to a Glide instance.

</td></tr><tr><td>

Schedule Optimization

 PRB1829010

</td><td>

In Schedule Optimization, batch optimization fails when one of the scopes is turned off in a batch configuration

</td><td>

An error including 'Cannot read property "travel\_est\_provider" from null' is displayed.

</td><td>

1.  Open the Schedule Optimization batch configuration 'SO with Crews'.
2.  Mark one of the scopes as active = false.
3.  Start a Schedule Optimization run.

</td></tr><tr><td>

Service Mapping

 PRB1824257

</td><td>

ProcessToProcess LBAFPProviderEnhanced fails with cmdb\_tcp records containing source\_process=null

</td><td>

The log contains the following error: 'ProcessToProcess LBAFPProviderEnhanced: class org.json.JSONObject$Null cannot be cast to class java.lang.String ...no thrown error'.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1722817

 [KB1634661](https://hi.service-now.com/kb_view.do?sysparm_article=KB1634661)

</td><td>

'SAM - Deduplication Worker' has a long running query

</td><td>

The logs show the query is slow.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1775506

 [KB1648325](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648325)

</td><td>

The software lifecycle report in classic view is empty

</td><td>

The report for 'Software Lifecycle reports' table has empty records in the Washington DC release.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1807185

</td><td>

Forms break while creating new integration profiles

</td><td>

 

</td><td>

1.  Access a Xanadu instance.
2.  Navigate to the plugins page and install the 'samp\_master' and 'saas int' plugins.
3.  After installation, navigate to an integration profile page.

 The page breaks.

</td></tr><tr><td>

Software Asset Management Workspace

 PRB1833497

</td><td>

There's a workspace functionality issue where filtering products under license usage isn't working

</td><td>

There's an issue with filter products under license usage. All records are displayed if users select a record for any particular version for a product while entering the name of the product in the search field. All the products display again.

</td><td>

 

</td></tr><tr><td>

Software Models

 PRB1786414

 [KB1698556](https://hi.service-now.com/kb_view.do?sysparm_article=KB1698556)

</td><td>

The sam\_admin role failed to load the 'publish to software catalog' list when catalog records not readable by role

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Source Control Engine

 PRB1829444

</td><td>

sys\_ui\_message additional coalesce value can break an app customization install

</td><td>

An error displays: 'SEVERE \*\*\* ERROR \*\*\* Failed to auto install plugin and/or app customization sn\_hr\_sp with version 1.5.2 java.lang.NullPointerException: Cannot invoke "String.hashCode\(\)" because "this.fCompositeKey\[i\]" is null...'

</td><td>

1.  Create an app customization against either the sn\_hr\_sp or sn\_hr\_core scopes.
2.  Add a new sys\_ui\_message to the customization.
3.  Publish the version.
4.  Attempt to install the version

 Expected behavior: Customization installation completes, updating expected files.

 Actual behavior: Installation is interrupted with an error/stack trace.

</td></tr><tr><td>

System Export Sets

 PRB1836146

</td><td>

Log Export Service should top forwarding Log.xxxNoBroadcast\(\) events

</td><td>

More calls were added to the Log.xxxNobroadcast from the critical section code with the expectation that it doesn't make calls back to DB. However, the downstream code makes database calls on the same Log API calls, which created a deadlock situation.

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1822693

</td><td>

Added system properties to evenly distribute events for schedule optimization

</td><td>

Even though there are multiple queues, events are not distributed equally. As a result, the queues in use are overloading. New system properties include: com.glide.event\_ manager.territory \_overlapping\_ queue.claim\_limit, com.glide.event\_ manager.territory \_overlapping\_ queue.even. load.distribution.enabled, and com.glide.event\_manager .territory\_overlapping\_ queue.hard\_limit.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB1828008

 [KB1710085](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710085)

</td><td>

MFA-configured with SSO users are incorrectly redirected to a page that can't be found

</td><td>

Multi Factor Authentication \(MFA\) with single sign-on \(SSO\) redirection is broken and users are redirected to a 'not\_found.do' page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Builder \(Family Channel\)

 PRB1828407

</td><td>

Users are unable to add new data visualizations and set the data sources in Agent Workspace when opened in UI Builder

</td><td>

 

</td><td>

1.  Open any Xanadu-upgraded instance.
2.  Access the Agent Workspace sys\_aw\_master\_config record.
3.  From here, select the **Open in UI Builder** UI action.
4.  Create a page.
5.  Try to add/drag a data visualization from the components on the left.

 Expected behavior: Users are able to add a data source and save.

 Actual behavior: Users can't add a type of data visualization, and can't add the data source like how they can add on configurable workspaces opened from UI Builder.

</td></tr><tr><td>

UI Field Administration

 PRB1799424

</td><td>

There's a 'Recent selections' sorting issue on workspace

</td><td>

'Recent selections' on the **HR Service** reference field in workspace doesn't sort data as per the reference qualifier attribute ref\_ac\_order\_by.

</td><td>

1.  Log in to an instance.
2.  Navigate to HR Agent Workspace.
3.  Open any active HR case.
4.  Remove the **HR service** field's value.
5.  Select the **HR service** field.

 Expected behavior: The field should display the most recent selection with sorting.

 Actual behavior: The field displays the result as per recently selected reference data but they aren't sorted.

</td></tr><tr><td>

UI Field Administration

 PRB1805994

</td><td>

Reference fields are considering additional columns to sort auto-complete results in workspace

</td><td>

Reference fields are considering additional columns to sort auto-complete results in workspace in cases of a missing ref\_ac\_order\_by dictionary attribute.

</td><td>

1.  Navigate to an instance.
2.  Navigate to the 'Incident' table's **cmdb\_ci** field dictionary entry.
3.  Override the attributes.
4.  Remove ref\_ac\_order\_by=sys\_class\_name from the inherited attributes.
5.  Save.
6.  Impersonate as an itil user.
7.  Open a new 'Incident' form on workspace.
8.  Navigate to the **Configuration item** field.
9.  Open the reference picker list.
10. Sort by any column except name and close the reference picker.
11. Double-click on the **Configuration** item field.

 Expected behavior: There should be no modification in the auto-complete results sorting based on the column used to sort the reference picker list. It causes the performance issue.

 Actual behavior: The fired SQL query performs sorting on the sorted column name, 'Name'.

</td></tr><tr><td>

UX Framework

 PRB1766794

</td><td>

Closing multiple tabs quickly converts an existing workspace tab to a non-functional 'Details' workspace tab that can't be closed

</td><td>

A non-functional 'Details' tab appears when closing inactive tabs quickly.

</td><td>

1.  Open CWF or SOW Workspace.
2.  Open ten existing incident tabs.
3.  Click through the tabs to make them active, but keep switching and don't let them load all the way.
4.  Close an inactive tab before the new tab loads.
5.  Continue closing tabs this way until a non-functional tab is observed.

 Expected behavior: The subtab details is closed out.

 Actual behavior: The non-functional details tab appears when closing out inactive tabs quickly.

</td></tr><tr><td>

UX Framework

 PRB1822144

</td><td>

After upgrading to Xanadu, workspace date fields display an inaccurate date format error

</td><td>

Date format errors are present in date fields within workspace views.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

-   [Xanadu Patch 4 Hotfix 2](xanadu-patch-4-hf-2-PO.md)
-   [Xanadu Patch 4 Hotfix 1](xanadu-patch-4-hf-1-PO.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3 Hotfix 2](xanadu-patch-3-hf-2.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1 Hotfix 2b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1707176)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


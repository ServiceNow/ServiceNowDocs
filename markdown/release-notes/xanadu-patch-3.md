---
title: Xanadu Patch 3
description: The Xanadu Patch 3 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-12-05"
reading_time_minutes: 64
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 3

The Xanadu Patch 3 release contains important problem fixes.

-   **Xanadu Patch 3 was released on November 07, 2024.**
    -   Build date: 11-01-2024\_2230
    -   Build tag: glide-xanadu-07-02-2024\_\_patch3-10-23-2024

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X03.00.xlsx).

## Overview

Xanadu Patch 3 includes 298 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp3.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 3 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 3, refer to [KB1706274](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1706274).

## Changes in Xanadu Patch 3

-   **[Available system properties](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**
    -   **com.snc.pa.xmr.processes.limit**

        The maximum number of KPI Signals Configurations \(pa\_xmr\_processes\) that can be evaluated by the KPI Signals Insight Job. After this number of processes have been evaluated, the remaining processes are ignored.

        -   Type: Integer
        -   Default: 1000
        -   Maximum: 10,000

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

AI Search

 PRB1709322

 [KB1645499](https://hi.service-now.com/kb_view.do?sysparm_article=KB1645499)

</td><td>

Text seen when using AI Search can't be translated

</td><td>

The text '\[number\] results for \[keyword\]' can't be translated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1808466

 [KB1704590](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704590)

</td><td>

AI Search yields 'No results found' message on the Now Mobile app, but works as expected in the Service Portal

</td><td>

Using AI Search on the Now Mobile app does not render results and displays errors in the logs, but using AI Search in the Service Portal works as expected.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

History Set

 PRB1806563

</td><td>

Duplicate comments are observed intermittently even after enabling the fix for DEF0528864

</td><td>

With the fix for DEF0528864, the history set loader flow was modified to utilize the system property glide.history\_set.pull\_journal \_entries\_from\_journal\_table. However, there are new instances of intermittent duplication issues, even with this property enabled. In these cases, duplicate records in the sys\_history\_line table originate from the sys\_journal\_field table.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1797758

 [KB1705540](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705540)

</td><td>

When scrolling horizontally in any table in list view, field names do not scroll

</td><td>

When scrolling horizontally, the field names on the top are frozen in place but the values change.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1799023

</td><td>

Menu can show fewer items when a business rule is configured to restrict a query

</td><td>

The user observes that the Next Experience header is missing menus \(for example, 'All', 'Favorites', 'History'\). This can occur if there are business rules against the 'sys\_app\_application' or 'sys\_app\_module' tables with the type 'Query'. It can also result from bad domain-specific caching in relation to the menus.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1809948

 [KB1703663](https://hi.service-now.com/kb_view.do?sysparm_article=KB1703663)

</td><td>

Using the auto-fill function in an Edge browser triggers a search of all reference fields in the Service Portal catalog form

</td><td>

Starting from Edge browser 129.0.2792.52+, when the user fills the personal information with the auto-fill function on the service catalog form in the Service Portal, it triggers a search of all reference fields in the form. Sometimes this causes the form to freeze, and it must be reloaded to proceed.

</td><td>

1.  Enable the auto-fill function on Edge browser 129.0.2792.52+.
2.  Open a service catalog with multiple reference fields in Service Portal.
3.  Select one of the fields and fill the personal information by auto fill.

 Expected behavior: Only fields that are related to personal information are populated.

 Actual behavior: Fields related to personal information are populated, but all the reference fields on the form were in focus and triggered the searches of the fields.

</td></tr></tbody>
</table>## All other fixes

<table id="table_xl1_wyp_jdc" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Activity Stream

 PRB1773099

</td><td>

Components using the now-trigger-library for a keyboard shortcut are not deregistering

</td><td>

Components should deregister if using now-trigger-library so that the reference to the host and update state of the component is not kept. However, uxfTriggerLibrary continues to grow as certain components are not deregistering.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1803978

 [KB1704344](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704344)

</td><td>

The SysActivityRuleRepo should be share aware for event source tables

</td><td>

When the name of the rotated table does not match the root name, a new email event is not created. The SysActivityRuleRepo should allow emails to appear in both the Activity stream and in the Workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Advanced High Availability \(AHA\)

 PRB1816356

</td><td>

A rare deadlock occurs during Glide startup

</td><td>

The deadlock is caused by ScriptsMetricsPublisher.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1792465

</td><td>

Support for GlideRecordSecure in awa\_external\_event\_definition helper scripts

</td><td>

A helper script fetches record details for creating a WorkItem, Interaction and Queue Object details. However, GlideRecordSecure in the ExternalProviderHelper script is not being honored.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1798373

</td><td>

The **Reject** button should not be available on the inbox card during the queue transfer

</td><td>

The agent should only have the option to accept the chat or to let it time out. However, the agent has the option to reject or accept the chat.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1810926

</td><td>

A completed event is generated when the requester ends the conversation before an agent accepts chat

</td><td>

Cancelled and completed events are generated when the requester ends the conversation before an agent accepts the chat request. Only cancelled events should be triggered when a requested ends a conversation before an agent accepts the chat request.

</td><td>

1.  Start a conversation as a requester.
2.  Wait until the interaction gets routed to an agent.
3.  End conversation as a requester, before agent accepts chat request.

 Expected behavior: Only a cancelled event is triggered.

 Actual behavior: Cancelled and completed events are generated.

</td></tr><tr><td>

Agent Chat

 PRB1801904

</td><td>

The conversation panel appears for a closed interaction even after setting inactive.interaction.conversation .history.panel.enabled to 'false'

</td><td>

The conversation panel remains open in the list view of the Service Operations Workspace, even though the interaction is closed. This continues even after setting inactive.interaction.conversation .history.panel.enabled from 'true to 'false'.

</td><td>

1.  Set inactive.interaction.conversation .history.panel.enabled to **false**.
2.  Open two browsers.
3.  Impersonate an agent in the first browser.
4.  Open the Service Operations Workspace \(SOW\).
5.  Change the state to **Available.**
6.  Accept the incoming chat.
7.  End the chat.
8.  Close the workspace tab with the interaction.
9.  Open the same interaction from the list view in the second browser.
10. Open the portal that has the Virtual Agent.
11. Connect to an agent.

 Notice that the conversation panel appears.

</td></tr><tr><td>

Agent Chat

 PRB1813251

</td><td>

Now Assist context menu true-up

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Agent Workspace for HR Case Management

 PRB1749635

</td><td>

Scripted Template fields do not work in Workspace on the Case Creation Page

</td><td>

When setting up scripted values in an HR Case Template, the values don't work in the Case Creation Page on the workspace. However, when using the Case Creation Page in the classic view, the values do work.

</td><td>

1.  Set the scripted value in an HR case template for a field \(for example, set **Short description** to, javascript:'TEXT FROM TEMPLATE';\)
2.  Verify case creation from platform/classic view.

Observe that the **Short description** field is set to 'TEXT FROM TEMPLATE' as expected.

3.  Verify case creation from the workspace.

 Observe that the **Short description** field is not set to 'TEXT FROM TEMPLATE' as expected.

</td></tr><tr><td>

Agent Workspace for HR Case Management

 PRB1750634

</td><td>

Auto opening of knowledge creation records in Agent Workspace for HR

</td><td>

 

</td><td>

1.  Open any HR case on an instance with the Now Assist for HR plugin installed.
2.  Create an associated task record.
3.  Select **Save**.

 Notice that a new tab called Create Knowledge is opened.

</td></tr><tr><td>

Agent Workspace for HR Case Management

 PRB1758363

</td><td>

Timeline component icons are not rendered after event data changes

</td><td>

Child case event icons are not displayed on the timeline.

</td><td>

 

</td></tr><tr><td>

Agent Workspace for HR Case Management

 PRB1766214

</td><td>

The case form opened in Agent Workspace for HR case COE takes the default view instead of the Workspace UIB view

</td><td>

The default record view is displayed.

</td><td>

1.  Provision an instance with the 'Document templates' application installed.
2.  Open any sn\_hr\_core\_case case in HR Agent Workspace.

 Notice that the default record view is displayed.

</td></tr><tr><td>

Agent Workspace for HR Case Management

 PRB1768816

</td><td>

A knowledge creation record and resolution notes modal open automatically upon case creation

</td><td>

The resolution notes modal and KB creation page open automatically.

</td><td>

1.  Navigate to a declarative action \(sys\_declarative\_action\_assignment\).
2.  Search for a record: 'New' where table is 'sn\_hr\_core\_case'.
3.  Update the client script to 'Create New Record'.
4.  Activate the resolution notes skill.
5.  Navigate to HR Agent Workspace.
6.  Open any HR case.
7.  Navigate to the related item, 'Child Cases'.
8.  Create a new child case.

 Expected behavior: The resolution notes modal and KB creation page should not open.

 Actual behavior: The resolution notes modal and KB creation page open.

</td></tr><tr><td>

Agent Workspace for HR Case Management

 PRB1787727

</td><td>

Messages in the HR Agent Workspace are not translated to Japanese with the i18 Japanese plugin

</td><td>

Although most texts are translated to Japanese in the HR Agent Workspace with the i18 Japanese plugin, messages related to creating HR cases in the Agent Workspace for Case Management are not translated. Specifically, the text from the pop-up 'This case may already exist' and 'You can choose one of these cases or create a new one' are not translating to Japanese.

</td><td>

1.  Install the plugins i18 Japanese and sn\_hr\_agent\_ws \(Agent Workspace for HR Case Management\).
2.  Log in as an admin user or any user that can create HR case.
3.  Change the language setting to Japanese.
4.  Open the HR Agent Workspace.
5.  Create a new HR case.
    1.  Skip 'Verify the employee requesting this case'.
    2.  Provide the case details/ケースの詳細を入力. \(For example; COE：HRケース 　HRサービス：一般参照 　依頼者：admin 　対象者：admin 　作業メモ：test\)
6.  Select **Create case/ケースを作成**.
7.  Create a new HR case with the same details.

 Expected behavior: All texts are in Japanese.

 Actual behavior: Notice that the pop up 'This case may already exist' is not translated to Japanese, and the text 'You can choose one of these cases or create a new one' is not translated to Japanese.

</td></tr><tr><td>

Agent Workspace for HR Case Management

 PRB1809238

</td><td>

Some events are not displayed on the ER timeline

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1767776

</td><td>

Incorrect empty state \(no Genius results\)

</td><td>

Genius results do not appear on a query that should produce results.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1797747

 [KB1706071](https://hi.service-now.com/kb_view.do?sysparm_article=KB1706071)

</td><td>

The Genius Results Loading Spinner shows up despite unconfigured Genius Results

</td><td>

The top spinner is visible when Genius results are not linked and sometimes spins for a longer period of time. This occurs even if Genius results are not linked to a profile used in the application that is being searched. The loader causes the page to continue rendering even if genius results are not linked to a profile.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1799201

</td><td>

The suggested results page continuously loads when for guest user searches in the Service Portal

</td><td>

When users use the search bar in the home login page of an instance without logging in, they are redirected to the Search page. When users attempt to use the search bar in the Search page, the page will continuously load if no results are found.

</td><td>

1.  Enable AI Search.
2.  Enable the following public related base instance pages and widgets:
    1.  For the page, enable Title = Home Page\(ID=index\) and Title = Search\(ID=sp\_search\).
    2.  For widgets, enable Name = Homepage Search, Name = Typeahead Search, Name = Faceted Search, Name = breadcrumbs.
3.  Open the login page of an instance. Do not log in to the instance.
4.  Use the search bar on the login page to search for a keyword, for example 'email'.

Notice that the search will redirect to the Search page.

5.  Enter a keyword in the search bar on the Search page.

 Expected behavior: Suggested results will be generated, but if there are no results, no results will appear.

 Actual behavior: The Search page continuously loads even if there are no results found.

</td></tr><tr><td>

AI Search

 PRB1800899

</td><td>

Query Support for Multi Embedding model changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1805440

</td><td>

hasPendingIndex API returns true even though indexing is completed

</td><td>

If indexing is complete, the API should return false.

</td><td>

1.  Index any index source.
2.  In any table record in an index source, verify that indexing is complete with dumpDocument.
3.  Invoke hasPendingIndex for the table record and check the result.

 Expected behavior: Returns false as indexing is completed.

 Actual behavior: Returns true.

</td></tr><tr><td>

AI Search

 PRB1808465

</td><td>

The embedding stats state gets changed to 'Indexed' even though async embedding is enabled

</td><td>

The semantic ingestion state is indexing and the embedding stats state is in an indexed state.

</td><td>

1.  Enable async embedding by enabling system properties glide.ais.ingestion.embedding.async and glide.ais.ingestion.embedding .ais\_service\_async\_state.
2.  Index any data source and check the record after the value of Keyword Ingestion State changes to 'Indexed'.

 Expected behavior: The Semantic Ingestion State and each embedding stats state should be indexed, and these values should be updated by the scheduled job 'AIS Async Embedding Status Check'.

 Actual behavior: The semantic Ingestion State is indexing and the embedding stats state is in an indexed state.

</td></tr><tr><td>

AI Search

 PRB1812539

</td><td>

The AI Search 'Embedding Histories' tab shows an empty value in the End Time column

</td><td>

The AI Search 'Embedding Histories' tab shows an empty value in the End Time column when kb\_knowledge ingestion finishes.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1813387

</td><td>

A warning message should be shown when the user creates more than one semantic index source configuration for the same datasource

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1814811

</td><td>

AIS new datasource should not enable attachment by default

</td><td>

A new indexed source configuration should add advanced configuration for index\_attachement=false. However, nothing is added which enables attachment.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1815366

</td><td>

Show semantic ingestion status on index history default view on an indexed datasource

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1815524

</td><td>

AI Search embedding stats don't update after failover

</td><td>

Embedding stats doesn't get updated while async embedding is in progress. The semantic ingestion state stays 'Cancelled' after failover and doesn't update to indexing/indexed. The end time has a value set and embedding stats doesn't get updated while async embedding is in progress.

</td><td>

1.  Start 11k KB ingestion.
2.  Shutdown AIS node to create failover scenario.

 Observe that the keyword/semantic ingestion state updates to 'Cancelled'. Once failover is done, glide starts ingesting to a new active AIS and the keyword ingestion state changes to indexed once done.

</td></tr><tr><td>

AI Search

 PRB1817137

</td><td>

Rename 'Component field name' in semantic Index fields table to 'Field Name'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1818106

</td><td>

A negative value is shown for 'Percentage completed' on embedding stats

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1818925

</td><td>

Skill discovery doesn't work for Now Assist for HR skills

</td><td>

Skill discovery is not working for scoped apps where application administration is true.

</td><td>

1.  Provision an instance with Now Assist for HR 99.0.0 installed.
2.  Impersonate an admin
3.  Navigate to ESC portal.
4.  Open VA.
5.  Enter 'How to change my phone number.'

 Notice that the skill is in Now Assist for HR scope and the topic is not discovered.

</td></tr><tr><td>

AI Search

 PRB1820483

</td><td>

A regular DPR Search with scriptable API returns no passages

</td><td>

No results are returned.

</td><td>

1.  Provision an instance with AI Search 27.1 installed.
2.  Ingest a KB table with DPR field mappings.
3.  Attach a KB search source to a Service Portal profile.
4.  On Service Portal SAC, enable semantic search with semantic type 'DPR'.
5.  Perform a semantic search through a scriptable API.

 Notice that no results are returned.

</td></tr><tr><td>

App Generation \(Family Release\)

 PRB1808206

</td><td>

Ability to set color theme on input box in NAP for App Shell/ServiceNow Studio

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1788335

</td><td>

Remote app table entries are populated with 'undefined' in sys\_code column

</td><td>

There are 'undefined' entires in the sys\_code column of sys\_remote\_app entries.

</td><td>

 

</td></tr><tr><td>

Application Rationalization

 PRB1802489

</td><td>

There are issues in the 'Information object' related list

</td><td>

Managing and associating information objects in EA Workspace is broken and non-functional. The **Cancel** button isn't working for the **Add**, **Delete**, and **Edit** modals. There is some icon response time beside the **Cancel** button. There are spacing issues in the **Add** and **Edit** modals. Records aren't displayed after selecting the **i** icon and opening a record. When deleting a relationship, the browser is refreshed.

</td><td>

 

</td></tr><tr><td>

Application Rationalization

 PRB1809157

</td><td>

There are UI issues observed with the **Regenerate Indicator score** button

</td><td>

The modal UI has some issues. 'Fiscal period' isn't aligned to the title. There are issues with the **Cancel** button. There is a 'GlideWindow.locate: window not found' pop-up. Selecting the **Search** icon navigates to the 'Legacy' page when it should open in the workspace itself. When entering a value in the **Input** field, the 'Fiscal periods' list isn't properly visible. When adding a fiscal period, selecting the **i** icon and opening the record closes the modal. Indicator scores aren't generated.

</td><td>

 

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1817448

</td><td>

Fix Eslint errors in Xanadu

</td><td>

When trying to build a repo in Xanadu, the user observes eslint errors and the build fails.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1801811

</td><td>

Check the Ticket and Support status errors out when the HR plugins are installed

</td><td>

There are errors in the 'Check Ticket and Support' status in the Virtual Agent chat after the apps and plugins Now Assist in VA Human Resources, Human Resources: Core, the Human Resources Scoped App: Lifecycle Events, and the Human Resources Scoped App: Employee Relations are installed.

</td><td>

1.  Install the apps and plugins Now Assist in VA Human Resources, Human Resources: Core, the Human Resources Scoped App: Lifecycle Events, and the Human Resources Scoped App: Employee Relations.
2.  Navigate to **All** &gt; **Virtual Agent** &gt; **Designer.**
3.  Search for the topic 'Check Ticket and Support'.
4.  Select the test.

 Expected behavior: The list of pending items should be shown including HR items; the card includes: 'number', 'short\_description', and 'priority' of the selected HR case; and the user is able to add the additional comments on the case.

 Actual behavior: The error message, 'Sorry, there was a problem on my side trying to complete this request. Try asking again later'.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1803623

</td><td>

Missing RCAs from Manager Hub to HR Core

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1805956

</td><td>

Users are unable to create Knowledge Base \(KB\) Articles for HR Cases in UI16 and in the HR Agent Workspace

</td><td>

No error messages appear, yet draft KB articles are not created.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1811770

</td><td>

Restricted caller accesses \(RCA\) generate as part of healthcare HRSD

</td><td>

 

</td><td>

1.  Set up HRSD healthcare.
2.  Log in to the instance.
3.  Navigate to the application restricted caller access.

 Notice that the RCAs are coming as requested.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1812892

</td><td>

Multi-language support and Now Assist Context menu RCAs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1812953

</td><td>

RCAs to access \(create, read and write\) HR talent management case records from 'HRSDVAUtilsSNC' script include from Now Assist for HRSD

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1814233

</td><td>

The RCA should be shipped in the target scope \(source: OracleAdvancedUtilsSNC and target: hr\_Profile\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB1803076

</td><td>

The role gs.hasrole is missing on a base instance script include

</td><td>

The role is missing for the 'Consumer role' condition.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1797796

</td><td>

Incorrect configuration of audit fields causes slowness across features that use sys\_audit tables

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1805694

</td><td>

App Store contained signatures are not loading or validating in Xanadu

</td><td>

Each signature has an associated timestamp, and there was a change in how timestamps were generated in Xanadu. Prior to Xanadu the timestamp was computed from the plain text of the signature, whereas after Xanadu the timestamp is computed differently.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1809366

</td><td>

The Service Graph Connecter \(SGC\) Central menu link is missing in the Configuration Management Database \(CMDB\) Workspace after upgrading to Xanadu

</td><td>

After installing SGC V1.1, the user does not have a SGC Central menu link in the CMDB Workspace. Upgrading the CMDB Workspace to V6.2.0, a compatible version with the SGC Central, restores the SGC Central menu link. The CMDB Workspace is upgraded to V7.0.8 when upgrading to Xanadu, which is incompatible with the SGC Central, making the SGC Central menu link no longer available.

</td><td>

 

</td></tr><tr><td>

Contextual Security Manager

 PRB1769723

</td><td>

A query business rule prevents non-admin users commenting on SCTASK from copying over to RITM

</td><td>

Before Query Business rule preventing non-admin user comment on SCTASK from copying over to RITM.

</td><td>

 

</td></tr><tr><td>

Customer Service Management for Field Service Management

 PRB1817415

</td><td>

My Dispatch Map does not load

</td><td>

The map in the My Dispatch Map page doesn't load, with the error log 'TypeError: Cannot read property 'val' from undefined'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1804505

</td><td>

Add additional logging around sys\_db\_view \_table.where\_clause

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1814864

</td><td>

Platform Graph API to support Knowledge Graph

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1790711

</td><td>

Enable AHA Monitor on addition of secondary candidates without node restart

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1794580

</td><td>

DBAction.getListeners is slow

</td><td>

This is due to a synchronous block that needs to check for all active extension points for IDBListener and then merge and sort two array lists.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1739880

</td><td>

Ignore forcePrimaryKeyOrdering for 'TS' queries

</td><td>

Service Portal Search API returns an empty response.

</td><td>

 

</td></tr><tr><td>

Database Views

 PRB1764595

</td><td>

An amalgamated set of database view problems are encountered on migrated user instances

</td><td>

The issues include: Boolean values in where clauses; boolean operators in combination with '.' as the separator that need to be space-padded to convert to AND or OR; double-quoted strings with '.' as the separator are used as is and are interpreted as column names; duplicate order values.

</td><td>

 

</td></tr><tr><td>

Data Collection for Oracle Global Licensing and Advisory Services for Software Asset Management

 PRB1810089

</td><td>

Downloading the GLAS Report is running into blank page

</td><td>

The user is unable to download Oracle GLAS reports when there are over 10 million records in GLAS tables.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1726066

 [KB1645554](https://hi.service-now.com/kb_view.do?sysparm_article=KB1645554)

</td><td>

The vCenter Cloud probe is triggered every time the web server \(http.https\) is determined as open

</td><td>

A previous fix introduced a new 'VMWare - vCenter Cloud' probe which checks if vCenter is running on 443 port. If so, it triggers vCenter discovery. However, the 'VMWare - vCenter Cloud' probe gets triggered every time the Web Server \(http.https\) is determined to be open.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1788611

 [KB1703744](https://hi.service-now.com/kb_view.do?sysparm_article=KB1703744)

</td><td>

vCenter extension contexts fail to start

</td><td>

The vCenter collector MID Server Extensions do not start and events are not collected.

</td><td>

1.  Navigate to vCenter Event Collector Contexts.
2.  Create a new record.
3.  Specify the MID server and vcenter details.
4.  Save the record.
5.  Select **Start** to trigger the events.

 Observe that the events are not triggered upon selecting the **Start** button.

</td></tr><tr><td>

Discovery

 PRB1791352

</td><td>

ECC queue related list count mismatch for a discovery status

</td><td>

The ECC queue record count in the related list is lower than expected.

</td><td>

1.  Update the sys\_relationship record 897b216d0a0a0b 7300d9c0927455f8eb which controls how 'refined the query in current that will populate the related list'.
2.  Have the updated\_time.addSeconds in the script to a low value \(one or two minutes\).
3.  Run a discovery that takes at least five to ten minutes.
4.  Wait for discovery to execute beyond one minute.

 Observe that the ECC queue record count in the related list is lower than expected \(cross check against ECC\_QUEUE table directly using the agent correlator\).

</td></tr><tr><td>

Discovery Probes and Sensors

 PRB1790391

</td><td>

HP-UX Server OIDs try to launch switch/router patterns

</td><td>

Some OIDs will attempt to trigger network device discovery if SNMP is enabled for HP-UX servers.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1779605

</td><td>

Inactive keys are preventing STP because they return a prediction score as '0'

</td><td>

 

</td><td>

1.  Create a DE use case.
2.  Create required fields.
3.  Create a task.
4.  Upload documents to train a model.
5.  After training a couple of tasks, enable STP with STP Th=0.6.
6.  Create a task to go through STP.
7.  Deactivate any of the fields.
8.  Create another task.

 Since the field is required and thus makes it inactive, it causes the prediction score to be 0. STP doesn't pass since the required field that is now inactive has a 0 prediction score less than the STP threshold.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1800435

</td><td>

Use cases with date type fields are not autofilling the data, even though predictions are more than the threshold

</td><td>

Data is not autofilled for tasks, even after a use case with date fields was created with predictions of more than 50%.

</td><td>

1.  Create a use case, 'Nagesh\_DateUC\_MonthFirst\_NoAgentReview'.
2.  Create 20 date fields with the type 'Month First'.
3.  Create two field groups of the type 'fieldgroup'.
4.  Add five fields of type date under each field group, for a total of 30 fields.
5.  Create a task.
6.  Verify that the task was processed.
7.  Trained the task with 30 different date formats.
8.  Verify that prediction is more than 60% after some tasks.
9.  Enable autofill for the use case.
10. Set the threshold as 0.5.
11. Create a new task.

 Expected behavior: The task autofills the data if the predictions are more than 50%.

 Actual behavior: Autofill does not work for the task.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1802676

</td><td>

The **Edit** functionality does not appear for all reference fields

</td><td>

The **Edit** functionality does not appear at all times, and only appears after entering a proper value on. When adding two fields in a use case, the edit functionality only appears for one field and not the other.

</td><td>

Add two fields in a use case, one vendor reference field and one contract model reference field.

 Notice that the **Edit** functionality is not the same for both fields; the **Edit** functionality appears in the vendor reference field but does not appear in the contract model field.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1807379

</td><td>

Docintel OCR Triton config in Glide is incorrect

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1811973

</td><td>

Switch OCR and PDF to use DocReader

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1811982

</td><td>

Create form views to allow admin to create fields and field groups

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1811991

</td><td>

GenAI transaction not to be counted against 'Classic' transactions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1812780

</td><td>

Tasks are not processed for Doc Classifier use cases

</td><td>

Tasks are not processed for Doc Classifier use cases after training the use cases. Although the training job for use cases are triggered in ML solutions, the task is not processed and records are not created in the ML solutions table.

</td><td>

1.  Install the 5.2 App on an instance.
2.  Navigate to **Document Intelligence** &gt; **Document Classification** &gt; **Use cases**.
3.  Create the use case 'DC\_UC1'.
4.  Create two fields, 'k1' and 'k2'.
5.  Created a task.
    1.  Attached six files.
    2.  Submit the values in the DocIntel agent view.
6.  Select **Train use case**.

Notice that the training job has been triggered successfully in ML solutions.

7.  Created a new task 't2'.

Notice that the **Process task** button is available.

8.  Select **Process task**.

 Expected behavior: The task is processed.

 Actual behavior: The task is not processed and no record is created in the ML solutions table.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1814866

</td><td>

Add extension points/resolvers to hook prediction flow

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1814867

</td><td>

Add new column 'Prediction Method' to sys\_di\_key table and sys\_di\_key\_group table

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1814895

</td><td>

Modify Extension Point 'AttachmentPreProcessor' to add check for 'Prediction Method' Key

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1815770

</td><td>

The **Edit** fields in reference fields appear as Sys IDs for some tiebreaker fields

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1817986

</td><td>

Date fields with the month first type are not normalized correctly in plugin

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1818548

</td><td>

The user is unable to add new keys to a migrated use case

</td><td>

A new key has an empty name and fails.

</td><td>

1.  Create a task definition.
2.  Copy task definition with the DocIntel Admin app.
3.  Add a new key to the task definition.

 Notice that the name of the new key is empty. The backend expects it to be non-empty and fails. The user is unable to create subsequent keys because the name 'null' is already taken.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1818806

</td><td>

Implement the batching of attachments

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Dynamic Scheduling

 PRB1811377

</td><td>

Process failure when using the Workforce Optimization \(WFO\) feature to schedule a task under dynamic scheduling

</td><td>

If the window is not enough for the task work duration, the process fails and an error is reported. Also, when using the scheduled job 'Process Dynamic Schedule Auto Assignment', it won't proceed.

</td><td>

 

</td></tr><tr><td>

Dynamic Translation

 PRB1818919

</td><td>

The conversation gets stuck with language detection off

</td><td>

 

</td><td>

1.  Set up DT and keep the language detection off.
2.  Set up NAVA on any portal.
3.  Log in to the NAVA portal as a user with the language set to Spanish.
4.  Open the web client.
5.  Type 'I need to order a new hire'.

 Observe that the conversation gets stuck.

</td></tr><tr><td>

Dynamic Translation

 PRB1820033

</td><td>

Text is not fully matched for exclusion when there are overlapping exclusion rules in input

</td><td>

There are three issues: Text matching exclusion patterns that overlap with other matching text aren't marked correctly for exclusion. Match counts are undercounted for metrics - if a rule matches more than once in a block of text it will only be counted once. If the user creates a plain\_text exclusion pattern, the exclusion framework will fail to match \[rules\] if input is recognized as HTML.

</td><td>

 

</td></tr><tr><td>

Employee Center

 PRB1764971

</td><td>

An external link opens twice from the Favorites Content Card widget

</td><td>

This occurs because there are two redirections present on the anchor tag.

</td><td>

1.  Enable pop-up in the browser.
2.  Make a web application with an external link.
3.  Make a favorite with this web application.
4.  Open ESC and navigate to my favorite page.
5.  Open the external link.

 Notice that it opens twice.

</td></tr><tr><td>

Employee Center

 PRB1796462

</td><td>

'Sort by A-Z' doesn't work for non-English locale users

</td><td>

The 'Sort by A-Z' option shouldn't exist for non-English locale users, but it does exist and doesn't work.

</td><td>

1.  Log in as a non-English locale user.
2.  Navigate to the topic page.
3.  Sort by A-Z in the topic content widget.

 Expected behavior: A-Z sort option shouldn't exist for non-English locale users.

 Actual behavior: A-Z sort option exists and doesn't work.

</td></tr><tr><td>

Enterprise Architecture

 PRB1711624

</td><td>

An upload version isn't working for an architectural artifact to create an architectural artifact version

</td><td>

The **Save** button isn't working for the architectural artifact version new form.

</td><td>

1.  Log in to an instance with the latest or existing version \(2.1.0\) of EA Workspace installed.
2.  Navigate to **EA Workspace** &gt; **Portfolio** &gt; **Architectural Artifact** &gt; **All**.
3.  Open any existing architectural artifact.
4.  Navigate to the 'Architectural Artifact Versions' related list.
5.  Select the **Upload version** button.
6.  Select the file type as 'URL' and enter the URL.
7.  Select the **Save** button.

 Observe that no version is created.

</td></tr><tr><td>

Event Management

 PRB1796928

 [KB1701046](https://hi.service-now.com/kb_view.do?sysparm_article=KB1701046)

</td><td>

IT alerts are created or updated from anomaly events instead of anomaly alerts

</td><td>

Instead of anomaly alerts, IT alerts are created and updated when an anomaly event is created.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1797263

</td><td>

Express List suggestions appear on a Classic Incident Form

</td><td>

Express List suggestions unexpectedly appear on a Classic Incident Form on Xanadu and SOW 6.0 combination.

</td><td>

 

</td></tr><tr><td>

Fenix \(Family\)

 PRB1797963

</td><td>

Fenix manifest gets overridden when the app is upgraded

</td><td>

When a Fenix manifest is customized it breaks the ability to upgrade.

</td><td>

 

</td></tr><tr><td>

Fenix \(Family\)

 PRB1803849

</td><td>

A Fenix job isn't working when an instance has a vanity URL set up

</td><td>

The Fenix job starts with an incorrect instance\_url.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1780076

</td><td>

Approval state is set to 'Cancelled' when the Flow executes actions with the stage 'Requested Cancelled' in Vancouver and Washington

</td><td>

When the flow sets the RITM Stage to 'Request Cancelled', the RITM Approval is still 'Requested' which triggers the 'request item closure' business rule.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1796423

</td><td>

In Flow Designer, the input data disappears after the user saves the flow

</td><td>

The user builds an action with the structure 'Array.Object contains Array.Objects contains Objects of String'. When they try to set the value for the String variable, the value clears out after saving.

</td><td>

1.  Open a Xanadu release instance.
2.  Build an action with the structure 'Array.Object contains Array.Objects contains Objects of String'.
3.  Create a subflow and add the created action in the second step.
4.  Try to set the value for the String variable and save the subflow.

 Expected behavior: The value is saved.

 Actual behavior: The value is wiped out.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1796489

</td><td>

A flow variable assignment is reverted after saving a subflow

</td><td>

 

</td><td>

1.  Open Flow designer.
2.  Open the 'Test boolean assignment' subflow.
3.  Try to assign the **Active** field from the Subflow input \(Complaints Case\) record to the flow variable 'Case Active'.
4.  Save the subflow.
5.  Check the flow variable assignment.

 Notice that an assignment was reverted after saving the subflow.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1797470

</td><td>

Two way type doesn't work if used in multi-level subflows along with assign outputs

</td><td>

The password2 SSD \(Secure Storage Data\) records are deleted as soon as a flow completes/terminates.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1803100

</td><td>

Hints are not updated for actions and sub flows

</td><td>

Changing a **Hint** field value and saving doesn't update the value.

</td><td>

1.  Navigate to Flow Designer.
2.  Create an Action/Subflow.
3.  Add an input.
4.  Set a value for the **Hint** field on the input and save.
5.  Modify the hint and save.

 Expected behavior: The hint should get updated.

 Actual behavior: The hint is not getting updated.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814868

</td><td>

2.4 Flow Generation Data Pill for Subflow Component

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814869

</td><td>

3.7 Save Components inputs \(excludes additional UI data such as predicates\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814870

</td><td>

Input validation from LLM before display - Trigger Conditions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814871

</td><td>

2.2 Flow Generation Data Pill for flow logic Components

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814872

</td><td>

If the action does not exist after moving builder, the annotation should stay the same \(do not update it to the action label\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814873

</td><td>

Backend efforts to support input values in V1 and V2, data pill for trigger pills and without complex object fields

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814875

</td><td>

2.2 AI Search ACL Config Changes for tables and columns

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814877

</td><td>

Enable trigger to have non-existing inputs on createFlow operation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814879

</td><td>

2.3 Flow Generation Data Pill for the Action Components

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814881

</td><td>

Save trigger inputs \(excludes additional UI data such as predicates\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814883

</td><td>

Add required attribute/data in save trigger/component API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814885

</td><td>

Intermediate flow API version issue fix and top level try issue fix

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1814887

</td><td>

Flow generation validations back-end

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Form Controller

 PRB1789206

</td><td>

The banner is shown but AI Icons are missing

</td><td>

Only a banner is shown but AI Icons /predictions are missing. On form reload/refresh the AI Icons and predictions are shown.

</td><td>

1.  Open an instance with the following plugins installed:
    1.  Customer Service Management demo data
    2.  Task intelligence for August release \(25.1.2 and Task Intelligence for Admin 4.3.3\)
    3.  CSM Configurable workspace bundle - 4.1.1
2.  Deploy a Categorization Model with After Create predicting multiple output fields as Autofill.
3.  Create a case with short description and save.

Observe that AI Icons and Banner is shown properly.

4.  Close the case tab and open the case again from the list.

 Notice in the case form that only the banner is shown but AI Icons /predictions are missing. On form reload/refresh, the AI icons and predictions are shown.

</td></tr><tr><td>

Guided Application Creator

 PRB1800495

</td><td>

Non-ASCII characters should be prevented in the 'Application name' field in Guided Application Creator \(GAC\) when creating an application

</td><td>

Developers can't be managed for an application named entirely with non-ASCII characters.

</td><td>

1.  Open Studio.
2.  Create an application.
3.  Name the app 焼肉.
4.  Name the scope.
5.  Select **Create**.

 Expected behavior: The user shouldn't create an application with a non-ASCII character.

 Actual behavior: The user can create an application with a non-ASCII character.

</td></tr><tr><td>

Guided Tours

 PRB1793649

</td><td>

Tour is not triggered from portal and a console error is displayed

</td><td>

A tour is not triggered and following console error is displayed: 'TypeError: undefined is not an object \(evaluating '$scope.data.spInstanceId'\)'.

</td><td>

 

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1808558

</td><td>

Some Health Log Analytics \(HLA\) poller data inputs aren't using the proxy configured for MID

</td><td>

Some data inputs for HLA products don't respect the proxy configuration. The proxy can't be configured on the data input record either. This may exist for many data inputs but is confirmed in one.

</td><td>

1.  Set up a MID server in a network behind a firewall that requires a proxy for outbound access.
2.  Configure the proxy for outbound MID server connections.
3.  Add a rule to block all outbound connection and only allow connections to a potentially impacted URL.
4.  Try to configure a data input for the HLA test connection and/or try to start the data input with a potentially impacted data input.

 Notice that the connections time out or otherwise fail because they are ignoring the proxy configuration.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1809328

</td><td>

Upgrading an instance with certain plugins brings the instance down

</td><td>

 

</td><td>

1.  Set up LES in a Washington DC or Xanadu instance.
2.  Upgrade the instance to latest the track or datastreaming.

 Notice that the instance is down after the upgrade, and there is an error message in the nod log.

</td></tr><tr><td>

Horizon Component Library

 PRB1792830

</td><td>

The caret slot in now-textarea does not move when scrolling

</td><td>

The icon stays in the same place even though the caret position has been scrolled.

</td><td>

1.  Add enough text to enable scrolling in the Now Assist textarea.
2.  Select anywhere in the text and scroll.

 Expected behavior: The icon either disappears or stays with the caret position.

 Actual behavior: The icon stays in the same place even though the caret position has been scrolled.

</td></tr><tr><td>

Horizon Component Library

 PRB1804527

</td><td>

Extra popover panels are generated and not removed from the DOM when the cursor moves over menu triggers quickly

</td><td>

Many popover panels are generated and remain in the DOM even when the now-flyout-menu is closed.

</td><td>

1.  Open the now-flyout-menu demo and find the 'Mixture of children' example.
2.  Open the browser's inspector and navigate to the elements tab.
3.  Quickly mouse up and down repeatedly over the menu items in the 'Change Tone' section of the 'Mixture of children' example.
4.  Open the elements tab in the inspector.

 Expected behavior: Only two popovers at most should be present in the DOM - one for the root level menu and one for the nested menu.

 Actual behavior: Many popover panels are generated and remain in the DOM even when the now-flyout-menu is closed.

</td></tr><tr><td>

Horizon Component Library

 PRB1805211

</td><td>

The focus ring behavior breaks if the user switches between using the keyboard and mouse

</td><td>

There are several issues with the focus ring behavior.

</td><td>

Issue 1:

 1.  Navigate to the now-flyout-menu demo and open any flyout menu example by selecting the trigger.
2.  Press the down arrow.

 Observe that active item has an updated background color but no focus ring.

 Issue 2:

 1.  Navigate to the now-flyout-menu demo and open any flyout menu example via the keyboard.
2.  Use the keyboard to navigate to a flyout menu item that has nested items.
3.  Hover over the flyout menu item.

 Observe that there are two focus rings, one on the hovered item and one on the first item in the nested menu.

 Issue 3:

 1.  Navigate to the now-flyout-menu demo and open any flyout menu example by selecting the trigger.
2.  Press the key that corresponds to the first letter in one of the flyout menu item labels.

 Observe that the active item shifts to the flyout menu item that starts with that letter.

</td></tr><tr><td>

Horizon Component Library

 PRB1807498

</td><td>

Opening and closing the menu with the left and right arrow keys doesn't follow the documents direction

</td><td>

The direction of the arrows is reversed.

</td><td>

1.  In the design system repo, navigate to the example.js file within the directory components/flyout-menu/example.
2.  Add document.dir = 'rtl' before the render function.
3.  Run the demo and interact with one of the flyout menus using the keyboard.

 Expected behavior: When in RTL mode, the left arrow should open nested flyout menus and the right arrow should close nested flyout menus.

 Actual behavior: The right arrow opens the nested menus and the left arrow closes the nested menus.

</td></tr><tr><td>

Horizon Component Library

 PRB1808215

</td><td>

The **Now Assist Context Menu** \(WWNA\) floating button disappears while typing

</td><td>

This is a product update

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1814861

</td><td>

New component for the Horizon Component Library

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1814862

</td><td>

Flyout menu created for GenAI use cases

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1814892

</td><td>

Selection using CSS styles

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1814894

</td><td>

The GenAI **Now Assist Context Menu** \(WWNA\) now-modeless-dialog height can be resized

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Horizon Textarea Component

 PRB1813178

</td><td>

Portions of the selected text are not visibly highlighted

</td><td>

 

</td><td>

1.  Open an incident on SOW workspace and change the state to resolved or closed.

Notice that resolution notes are generated.

2.  Select the sparkle icon and generate the elaborated text, then replace it with the text available in the editor.
3.  Select the specific text to perform 'Elaborate' or 'Shorten'.

 Observe that portions of the selected text are not visibly highlighted.

</td></tr><tr><td>

HR Service Delivery integration with Adobe Sign

 PRB1784154

</td><td>

The 'Create And Send Adobe Sign Agreement' subflow uses a deprecated action

</td><td>

The subflow 'Create And Send Adobe Sign Agreement' uses a deprecated action from the 'Finalize Draft and Send Agreement' flow.

</td><td>

1.  Open the subflow **Create And Send Adobe Sign Agreement**.
2.  Navigate to **Finalize Draft and Send Agreement**.

 Notice that the subflow uses a deprecated version of the **Finalize Draft and Send Agreement** action.

</td></tr><tr><td>

HR Service Delivery

 PRB1760517

</td><td>

RCAs from EDG core to Employee Profile when HR Now Assist is installed

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1811082

</td><td>

Using email recommendations generates RCAs

</td><td>

When using email reply recommendation functionality, the user notices that RCAs generated.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1813441

</td><td>

Using email recommendations generates Restriced Caller Access \(RCA\)

</td><td>

RCAs are generated for reply email recommendations.

</td><td>

1.  Create a case of below types for the HRIT Operations Case, HR Total Rewards Case, HR Lifecycle Events Case, HR Payroll Case, and the HR Workforce Administration Case.
2.  Use the email reply recommendation functionality.

 Notice that RCAs generated.

</td></tr><tr><td>

Incident Management

 PRB1815219

</td><td>

Undo fix script changes done to add the email\_composer role to IPCR roles

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1785282

</td><td>

The sys\_ux\_lib\_component file is missing required translation keys

</td><td>

In Xanadu, the sys\_ux\_lib\_component file is missing required\_translation\_keys.

</td><td>

 

</td></tr><tr><td>

Internationalization Features

 PRB1809283

</td><td>

getDisplayValueLang\(\) isn't returning translated records from the sys\_choice table

</td><td>

 

</td><td>

Try to retrieve the translation records from sys\_choice table using getDisplayValueLang\(\).

 Expected behavior: It should return the choice record in Spanish.

 Actual behavior: It returns the choice record in English.

</td></tr><tr><td>

Knowledge Management

 PRB1791996

</td><td>

Fix for empty attributes in the TinyMCE Version 6 upgrade

</td><td>

There are dictionary entries with HTML types with empty attributes in TinyMCE Version 6.

</td><td>

1.  Upgrade to Xanadu.
2.  Run the fix script while upgrading dictionary attributes with empty values.

 Notice that it fails the execution and remaining dictionary entries are not upgraded.

</td></tr><tr><td>

Knowledge Management

 PRB1793247

</td><td>

Update toolbar/plugin value with V6 for the creation of article templates HTML type fields

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Legacy Application Creator

 PRB1800496

</td><td>

Non-ASCII characters should be prevented in the **Application name** field in Guided Application Creator \(GAC\) when creating an application

</td><td>

Developers can't be managed for an application named entirely with non-ASCII characters.

</td><td>

1.  Open Studio.
2.  Create an application.
3.  Name the app 焼肉.
4.  Name the scope.
5.  Select **Create**.

 Expected behavior: The user shouldn't create an application with a non-ASCII character.

 Actual behavior: The user can create an application with a non-ASCII character.

</td></tr><tr><td>

Major Incident Management

 PRB1815931

</td><td>

Impersonation logic in MIM script include causes events to fail post-upgrade

</td><td>

System events error out as a result of user impersonation logic in the 'ExecuteMIMTrigger RulesWithImpersonation' script include. When this script include is called during async processing, the system impersonates the logged in user, marking subsequent events as being processed or updated by an individual user instead of the 'System'. As a result, these events error out.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1699764

</td><td>

There's missing functionality for Amazon Web Services \(AWS\) credential resolution for some member accounts and regions

</td><td>

Resolving the default OrganizationAccountAccessRole for an AWS Member account discovery results in attempting using a Commercial ARN format.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1767562

</td><td>

The Mobile URL function with record context re-encodes the parameters of URLs

</td><td>

When a URL with encoded parameters is opened by the record context URL function in the Mobile app, the encoded parameter is encoded again, leading to incorrect parameters being passed to the server.

</td><td>

1.  Create a URL field for the incident table in a base instance.
2.  Create an incident record.
    1.  Assign the incident record to a user.
    2.  Enter the URL with encoded parameters.
    3.  Save the record.
3.  Open the URL in the incident record.
4.  Observe that the URL was opened with same encoded parameters.
5.  Configure the Mobile detail screen for the incident record.
6.  Configure a footer function that opens the URL field of the incident record \(for example, Type = URL, Context=Record\).
7.  Log in to the Mobile Agent app as the user assigned to the incident record.
8.  Open the incident record.
9.  Open the footer function.

 Observe that the URL is open, but the encoded parameters are encoded again.

</td></tr><tr><td>

Mobile Platform

 PRB1811273

</td><td>

Users can no longer view attached excel files and docx files on Work Order Tasks \(WOT\) from the Agent app

</td><td>

Users can no longer view excel sheets and docx files attached to work order tasks on the Agent app after upgrading to Xanadu. When users attempt to view the attached files from work order tasks on the Agent app, a modal with the message 'Unsupported file type' appears.

</td><td>

1.  Open a Xanadu instance.
2.  Open any work order task.
3.  Assign the work order task to a user.
4.  Add an excel file or and docx file to the work order task.
5.  Log in to the Agent app as a user.
6.  Open the work order task.
7.  Navigate to the **Activity Stream** tab.
8.  Open the attached files.

 Notice that a modal appears with the message, 'Unsupported file type'.

</td></tr><tr><td>

Natural Language Query \(Family Release\)

 PRB1789221

</td><td>

High processing times when rephrase utterance is invoked under load

</td><td>

The NowAssistVisualizationService TableGuesser takes a significant amount of time where invoked twice with the rephrase in place. Invocations hold the worker for a longer duration and cause latencies in the overall transaction response time.

</td><td>

1.  Set up an instance for Gen AI and Text2Analytics Feature.
2.  Execute 25 users test for the search query where it should invoke a rephrase utterance and describe the NLQ response.

 Notice the time taken to get the visualization to the end user.

</td></tr><tr><td>

Notification Preferences

 PRB1806559

</td><td>

A complete list of subscription notifications is not displayed in the list

</td><td>

 

</td><td>

1.  Log into the instance.
2.  Navigate to the Preference page.
3.  Create a custom notification.

 Expected behavior: All notifications appear in the list.

 Actual behavior: A complete list of notifications does not appear in the list.

</td></tr><tr><td>

Now Assist Panel

 PRB1820452

</td><td>

The **Skip** option on non-mandatory inputs in NAP is not available to the user

</td><td>

The **Skip** option on the input variable is not visible to the user.

</td><td>

Trigger any sys\_one\_extend\_capability skill with non mandatory inputs from NAP.

 Verify that skip option on the input variable is not visible to the user.

</td></tr><tr><td>

Now Assist Panel

 PRB1820783

</td><td>

A time out message is not displayed in NAP text box

</td><td>

When a conversation times out, the input box should be disabled and the 'Start a new conversation' message should appear. However, the message doesn't appear and a blank text box is displayed instead.

</td><td>

1.  Impersonate an Agent.
2.  Select **NAP** and start conversation.
3.  Change the timeout in sys\_cs\_channel.
4.  Let the conversation time out.

 Notice that the 'Start a new conversation' message is not present and a blank text box is displayed. Also, selecting the text box does not start a new conversation.

</td></tr><tr><td>

Now Assist Panel

 PRB1820940

</td><td>

Chat input box is enabled for closed conversations when MAC is enabled in NAP

</td><td>

Once a conversation times out with multi conversation support enabled, the input box should be disabled and 'Start a new conversation' message should not be present. However, the 'Start a new conversation' message is present and a blank text box is not displayed. Also, selecting the textbox starts a new conversation which shouldn't happen. Conversely, when multi conversation support is not enabled, the chat input box should be enabled and selecting it should start a new conversation.

</td><td>

1.  Enable multi conversation support in NAP.
2.  Impersonate an agent.
3.  Select NAP and start conversation.
4.  Change the timeout in sys\_cs\_channel.
5.  Let the conversation time out.

 Notice that the 'Start a new conversation' message is present and a blank text box is not displayed. Also, selecting the text box starts a new conversation which shouldn't happen.

</td></tr><tr><td>

On-Call Scheduling

 PRB1799388

</td><td>

Family changes for daylights savings time \(DST\) need a fix on the Service Operations Workplace calendar

</td><td>

From DST, end events aren't rendering properly on the calendar when the system time zone is PST.

</td><td>

 

</td></tr><tr><td>

Platform Runtime

 PRB1799122

</td><td>

There's false-positive notifications about memory pressure after switching to ParallelGC

</td><td>

High usage of OldGen doesn't necessarily indicate memory pressure, especially when no major GCs are happening.

</td><td>

1.  Start an instance with ParallelGC.
2.  Observe MemoryRemediator's behavior.

 Notice how many times nodes are in the 'DEGRADING/DEGRADED' states.

</td></tr><tr><td>

Playbook Experience Core

 PRB1799979

</td><td>

Opening playbook activities on the Process Automation Designer \(PAD\) throws errors

</td><td>

Upon opening some playbook activities on the PAD, the user observes the error, 'Alert level: critical. \[500 Internal Server Error\]: Exception while executing request: null'. This occurs in Xanadu Playbook Experience Components: 26.0.4, Playbook Experience: 26.0.6, and Process Automation Designer: 26.0.8.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1790392

</td><td>

Inactive fields still display in dotwalk data

</td><td>

 

</td><td>

1.  Navigate to sys\_dictionary.list.
2.  Turn off the **Transcript** field by unchecking the active checkbox.
3.  Create a process with **Record Create/Update** on the 'Interaction' table.
4.  Add a stage.
5.  Add an activity.
6.  Open the 'UI Layout' tab.
7.  Navigate to the **Tagline** field.
8.  Select the **Dotwalker** button and dotwalk into a trigger record.
9.  Scroll down on the list of fields available to dotwalk and notice that 'Transcript' is displaying.

 'Transcript' shouldn't be available in dotwalk fields because it's not an active field.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1801892

</td><td>

The modify condition list is empty in Playbooks

</td><td>

When trying to add or modify conditions for an activity in Playbooks, the condition builder is empty and does not show any values for choice type outputs.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1804027

</td><td>

Reduce base instance Process Automation Designer \(PAD\) jobs to two

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1806671

</td><td>

The cluster detail purge logic is deleting less records set by the MAX\_ML\_CLUSTER\_DETAIL\_PURGE\_COUNT

</td><td>

 

</td><td>

Trigger the cluster detail purge schedule job with more than 100k records.

 Observe that the amount of 'Total ML Cluster Detail records purged' is less than the amount set by MAX\_ML\_CLUSTER\_ DETAIL\_PURGE\_COUNT, which is set to 100k by default.

</td></tr><tr><td>

Predictive Intelligence

 PRB1814359

</td><td>

Clustering API isn't honoring minRowCount and fails to consume its value

</td><td>

The clustering job fails with an error: 'ERR059: Add operation failed on table ml\_capability\_definition\_clustering - reason: \['ERR011: Dataset for table promin\_processed\_work\_note should have minimum of 100 records'\]'.

</td><td>

Initiate clustering on a record with minRowCount set as '30' in the configuration.

 Expected behavior: The clustering job should be completed successfully with the number of records in minRowCount.

 Actual behavior: The clustering job fails with an error.

</td></tr><tr><td>

Proactive Analytics

 PRB1800161

</td><td>

Signal insights aren't generated for large data sets

</td><td>

The Fluent API has a default hardcoded limit of 500 records. This is causing an issue for a client where they have near 10k XMR processes \(KPI Signal Configurations\).

</td><td>

1.  Create an instance with more than 500 pa\_xmr\_processes \(KPI Signal Configurations\).
2.  Run the 'KPI Signals Insight' job.
3.  Verify that only the first 500 XMR processes are evaluated.

 Expected behavior: All KPI signals are generated at Insights.

 Actual behavior: Only the first 500 are processed.

</td></tr><tr><td>

Proactive Analytics

 PRB1812880

</td><td>

Multi chart support is broken when 'force\_table\_ grammar' is false

</td><td>

In the August release of Analytics Generation, when PA indicators are disabled \(which is controlled by the system property com.snc.analytics\_ generation.enable\_indicators, defaulting to false\), NLQ can sometimes return a multiple\_table response.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1798240

</td><td>

ACL restrictions on sys\_created\_on and sys\_updated\_on cause the mining job to fail with a null pointer exception

</td><td>

When reading value for the **Created on** field, GlideRecordSecure returns null and the process mining job fails. There is no helpful error message displayed.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1806458

</td><td>

Unable to save a finding with a relation constraint type as 'Same event'

</td><td>

The user observes the error 'Exception encountered processing path: /GlidePromin\_Mutation/saveFindingDefs - Finding Constraint 'same event' is not setup correctly. Please check the Start and End conditions'.

</td><td>

1.  Create a project from Process Projects page.
2.  Navigate to the Improvement Opportunities page and create a new rule based finding.
3.  Set the condition to 'State is anything', eventually followed by 'State is anything', eventually followed by another 'State is anything'.
4.  Add a constraint with a start condition of 1, end condition of 3, and a relation constraint type of 'Same event'.
5.  Save and exit.

 Observe the error.

</td></tr><tr><td>

Process Mining

 PRB1808695

</td><td>

The user cannot import reference fields in external data

</td><td>

When the user adds a reference field in the external dataset and generates case data, it appears empty. The reimport feature doesn't work.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1776967

</td><td>

The user can't link an existing CIM on analyst workbench

</td><td>

There are no results when the user selects **Link existing CIM**.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1779372

</td><td>

The 'Tables' list doesn't load on the Set Objectives page after upgrading from Washington DC to Xanadu

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1780059

</td><td>

Issues with the No Role User

</td><td>

Scheduled tasks are created and completed successfully, but no records are displayed upon selecting **View Result**. Additionally, some bins are missing from a histogram.

</td><td>

1.  Share a mined project with a No Role User.
2.  Impersonate a 'ProcessOpt No Role User'.
3.  Navigate to the Analyst Workbench of the shared project.
4.  Select any node or arc of the PO graph.

Observe that the bins are missing on the histogram.

5.  Under Investigate tab, select **Show Records**.

 Observe that Scheduled Tasks gets created and completes successfully, but when user selects **View Result**, no records are displayed. Scheduled task should not get created.

</td></tr><tr><td>

Process Mining Workspace

 PRB1780387

</td><td>

Selecting **Show records** after a completed job when RCA/Clustering is triggered throws an error

</td><td>

The error reads 'Exception encountered processing path: /GlidePromin\_Query/scheduleShowRecord - Name is null'.

</td><td>

1.  Open the Analyst Workbench of any mined model.
2.  Select any arc/node and trigger **Show records**.

Notice that the view result will open a new window with records.

3.  Select any arc/node and trigger RCA/Clustering.
4.  Once complete, select the same node/arc and view the results for **Show records**.

 Notice the error 'Exception encountered processing path: /GlidePromin\_Query/scheduleShowRecord - Name is null'.

</td></tr><tr><td>

Process Mining Workspace

 PRB1785040

</td><td>

Issues while configuring the Archived Data Table

</td><td>

Nodes are displayed on the PO graph

</td><td>

1.  Create a project with archived table.
2.  Create a new Activity Definition for State.
3.  Select the **List of Values** button.

Observe that the list shows 'No results found'.

4.  Mine the model.

 Expected behavior: The results for all fields should be shown.

 Actual behavior: On the PO graph, the nodes are displayed.

</td></tr><tr><td>

Process Mining Workspace

 PRB1785536

</td><td>

The 'Set objectives' page loads indefinitely

</td><td>

The 'Set objectives' page loads indefinitely upon creating a new project using Guided Setup.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1786987

</td><td>

Set Objectives is slow to load and sometimes doesn't load at all

</td><td>

 

</td><td>

1.  From the left navigation, select **Process mining** &gt; **Projects** &gt; **Create new**.

Observe that set objectives doesn't load and intermittently takes around one minute to load.

2.  Navigate to the 'Process Projects' page.
3.  Select **Create new project**.

 Notice that the project doesn't load the first time. If the user closes the tab and reopens it by selecting the **Create new project** button again, it opens instantly.

</td></tr><tr><td>

Process Mining Workspace

 PRB1788169

</td><td>

When there are activities including Activity of Interest \(AOI\) added to the project, only the **AOI** field is displayed in the contextual conditions field

</td><td>

Only the priority field \(AOI\) is displayed in contextual fields list.

</td><td>

1.  Create a new project.
2.  Add more than one default activity \(state, Assignment group, category\) and one AOI field \(priority\).
3.  Mine and open Analyst workbench.
4.  On Advanced transitions pop-up, add state as field for condition 1.
5.  Select **Add contextual condition**.

 Expected behavior: All fields should be displayed in addition to the AOI \(other than the field selected in the condition\).

 Actual behavior: Only the priority field \(AOI\) is displayed in the contextual fields list.

</td></tr><tr><td>

Process Mining Workspace

 PRB1788204

</td><td>

Add a new licensing SKU \(Source to Pay\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1792911

</td><td>

The clustering results pop-up doesn't appear on a Now Support instance

</td><td>

The **View cluster** button on a scheduled task list doesn't work as expected.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1794422

</td><td>

Advanced Transitions with Constraints doesn't give results even for valid conditions

</td><td>

No results are displayed.

</td><td>

1.  Open analyst workbench of any mined project with ADs say, 'State', 'Assignment group'.
2.  Select **Advanced transitions** and give it condition as 'Assignment group is anything' directly followed By 'Assignment group is anything'.

Observe that there are records with duration over one hour in the results.

3.  Add a Duration constraint to the condition above \(minimum duration one hour\).

 Expected behavior: Results should be displayed.

 Actual behavior: Results are not displayed.

</td></tr><tr><td>

Process Mining Workspace

 PRB1795220

</td><td>

Uptake ML change to add platform\_ml\_read role to read ACLs of worknotes table

</td><td>

Worknotes analysis fails for 'NSE0014:Failed to initialize pipeline : No columns to parse from file' when read ACL of promin\_processed\_work\_note is turned on.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1799617

</td><td>

Rule-based findings do not show all impacted KPIs

</td><td>

Upon opening the 'Define' step for a new or existing rule-based finding definition, the user observes that not all impacted KPIs are shown.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1803567

</td><td>

The 'Review and mine' page does not load for content pack projects in the Project Builder

</td><td>

After selecting the **Review and mine** step for content pack templates, the page remains blank as it continuously loads.

</td><td>

1.  Log in to the instance.
2.  Open the Process Mining Workspace.
3.  Select **Create new project**.
4.  Navigate to the **Set Objectives**.
5.  Select a content pack template link from the Quick Start section.
6.  Select **Review and mine**step.

 Expected behavior: The page loads and does not show any errors after selecting the **Review and mine** step.

 Actual behavior: The blank page continuously loads after selecting the **Review and mine** step.

</td></tr><tr><td>

Project Management

 PRB1797917

</td><td>

The user is unable to create a Project Template via the 'Save as New Template' Related link with the project\_manager role

</td><td>

Users with the project\_manager role should be able to create templates.

</td><td>

1.  Assign the project\_manager role to a User.
2.  Create a **New Project**.
3.  Add a Project Task via the Related List.
4.  On **Project**, select the related link **Save as New Template**.
5.  Fill out the Template Name and select **Save**/**OK**.

 Upon navigating to the project\_template table, notice no template is created.

</td></tr><tr><td>

Project Management

 PRB1816772

</td><td>

The EAC is not calculated while generating project insights

</td><td>

 

</td><td>

1.  Create a project.
2.  Set the email cadence for the project.
3.  Add a cost plan, expense lines, and a budget to the project.
4.  Generate the email insight.

 Notice that the EAC is always zero.

</td></tr><tr><td>

Scheduled Jobs

 PRB1746752

</td><td>

Removing a member from a group will add several more users

</td><td>

Removing a user from a group in a sub-domain through the background job does not remove the user, and the job creates users for the group in the Global domain. If domain separation is enabled, M2MSlushbucketSaveJob must recognize the domain.

</td><td>

1.  Log in to an instance.
2.  Ensure the system property glide.ui.schedule\_slushbucket \_save\_for\_group\_roles is set to 'true'.
3.  Impersonate a user.
4.  Switch the domain.
5.  Open a group.
6.  Navigate to the Group Members tab.

Take note of the number of members in the group and the domain they belong to.

7.  Select **Edit**.
8.  Select a user to remove.
9.  Select **Save**.

Observe the form message, 'Job to add or remove role\(s\) from user\(s\) from group has been queued'.

10. Refresh the group members list.

 Observed that the number of members in the group has increased, every member in the list is in both the current domain and the global domain, and the user that was removed from the group remains in the group.

</td></tr><tr><td>

Scheduled Jobs

 PRB1792821

</td><td>

Concurrent updates on sys\_trigger causes intermittent HLL spikes on instances with large node counts

</td><td>

Concurrent updates on sys\_trigger causes intermittent HLL spikes on few instances with large node counts that are already experiencing database pressure.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1811056

</td><td>

Multiple batches should be allowed to be scheduled to run at the same time

</td><td>

Currently, more than one batch can't run at the same time while there is a batch run in progress.

</td><td>

1.  Set up a batch to schedule to run at a specific hour.
2.  Set up another batch to schedule to run for the same hour as the first batch.

 Expected behavior: Up to three batches should run at the same time.

 Actual behavior: Only one job is triggered.

</td></tr><tr><td>

Script Includes

 PRB1805747

</td><td>

Restructure upgrade transition for sandbox\_callable script include schema change

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog API

 PRB1763520

</td><td>

Checkbox variables don't appear in a conversational catalog

</td><td>

When the user creates a catalog with a checkbox variable and a UI policy that shows/hides the checkbox variable based on some conditions, the checkbox variable doesn't appear in the conversational catalog.

</td><td>

1.  Create a test catalog.
2.  Add a variable of type 'Select box' with two to three options.
3.  Add another variable of type 'Checkbox'.
4.  Add a UI Policy with a condition that the variable created in step 2 is option 1.
5.  Run this catalog in Now Assist VA conversation.

 Notice that the checkbox variable doesn't get asked in conversation when one of the options is selected from the variable created in step 2.

</td></tr><tr><td>

Service Catalog

 PRB1785302

</td><td>

Catalog client scripts don't work properly for Multi-Turn Catalog Ordering experience when all the records are scoped

</td><td>

When populating a catalog item with a catalog client script, the model asks for a mobile number that was already populated by the script.

</td><td>

1.  Provision an instance with NowAssist set up in Virtual Agent.
2.  Create a scoped Catalog item with a variable set and a few variables in it.
3.  Have a catalog client script that applies to 'variable set' that populates data in the variables in the catalog item \(set the variables to mobile, email\).

Upon selecting the catalog item, notice that the catalog client script populates data on the catalog item form.

4.  Navigate to **Virtual Agent Designer** &gt; **Test active topics** &gt; **LLM assistant topic**.
5.  Enter the Catalog name created in step 1.

 Notice that the model asks 'What is the mobile number?'.

</td></tr><tr><td>

Service Catalog

 PRB1818118

</td><td>

Date comparison from an onChange client script doesn't work as expected

</td><td>

A field error message is not displayed as expected.

</td><td>

1.  Add a question \(for example, start\_date\) with a Date type to a catalog item.
2.  Import the client script and set the onChange to map to the above question.
3.  From the conversation catalog, when the above question is prompted, enter a past date to trigger the error condition.

 Expected behavior: There should be a field error message displayed in the topic block.

 Actual behavior: A field error message is not there.

</td></tr><tr><td>

Service Portfolio Management

 PRB1808035

 [KB1705403](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705403)

</td><td>

An error message occurs when submitting a service in the Service Builder for Service Portfolio Management

</td><td>

Submitting a service in Service Builder prompts the error message, 'Status can only move forward to retiring or retired or obsolete from operational'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1779646

 [KB1704566](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704566)

</td><td>

Subscription installs have preference rank of 999 and cause performance issues

</td><td>

The O365 F3 install appears in samp\_install \_license\_options as preference rank 999, which causes the calculator to run 999 times.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1799866

 [KB1704751](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704751)

</td><td>

The suite of suite is unable to process inefficient child suites in Software Asset Management

</td><td>

With suite engine in Software Asset Reconciliation, suite efficiency does not properly process suite of suites with inefficient children. When a suite parent has suite children that are not efficient, it will count the component as nonexistent. If the system property 'Use component license' is on, then it can be considered.

</td><td>

1.  Create a suite set up.
    1.  Create the suite set up so that Suite A has Suite B and Suite C as components.
    2.  Create the suite set up so that Suite B has component D and E as components.
        1.  Ensure Suite B has an inference number of 3, for three components.
        2.  Ensure Suite A has an inference number of 1, for one component.
2.  Create an entitlement on Suite A.
3.  Create the installation of component D.
4.  Run the reconciliation process.

 Expected behavior: Component D is not inferred.

 Actual behavior: Component D is inferred to Suite A.

</td></tr><tr><td>

Software Asset Management

 PRB1806176

</td><td>

Performance issue in setProductResultOnLeftover function in the Publisher calculator

</td><td>

When upgrading from Vancouver to Xanadu, the total recon time increases from three hours to 16 hours.

</td><td>

 

</td></tr><tr><td>

Software Entitlements

 PRB1802882

</td><td>

Potentially incorrect reconciliation outcomes due to legacy downgrade rights

</td><td>

Starting with the Xanadu family release, support was introduced for creation of downgrade rights across different products. In previous releases \(from Tokyo to Washington\), users were restricted from adding downgrades across different products. However, there might be a scenario where users have had the downgrade records even before Tokyo release. These legacy downgrade rights are picked up by the new Xanadu capability and potentially cause incorrect reconciliation outcomes.

</td><td>

 

</td></tr><tr><td>

Subscription Management

 PRB1807575

</td><td>

Properties are not defaulted correctly on a track/licensing instance

</td><td>

The properties 'glide.entitlement.surf.routing' and 'glide.entitlement.ems.data.available' should be switched to the correct state only if the glide.entitlement.datasource .propertyfix.enabled is true.

</td><td>

 

</td></tr><tr><td>

Syntax Editor API

 PRB1792891

</td><td>

The Completion API has a longer response time due to the inclusion of shadow tables

</td><td>

The Completion API is experiencing a longer response time on instances with many shadow tables.

</td><td>

1.  Create several shadow tables.
    1.  Set the table attribute to excludeFromRollback=false and
    2.  Delete the records.
2.  Navigate to a page with a script editor, such as sys.scripts.modern.
3.  Open Chrome Developer Tools \(F12\).
4.  Navigate to the **Network** tab.
5.  Select the Monaco editor to bring it into focus.

Observe the network requests when the editor is selected for the first time, triggering Completion API.


 Expected behavior: Completion API responds quickly.

 Actual behavior: Completion API takes a long time to complete.

</td></tr><tr><td>

System Archiving

 PRB1789660

</td><td>

Restoring records with multiple related rules for same table throws a NullPointerException if at least one rule points to an empty field

</td><td>

A NullPointerExcepton is thrown when an archive rule for a table contains multiple archive related rules for the same table, and if at least one of the related rules points to an empty field restoring the related records.

</td><td>

1.  Create a problem record.
2.  Create a problem\_task for the problem record.
3.  Create an archive rule to archive the problem.
4.  Create two rules for archiving the related records.
    1.  Create one rule that points to the problem\_task from the problem record.
    2.  Create another rule for other fields that is empty for the problem\_task.
5.  Simulate UI action, Restore Record and Related Records with the sys\_id ebe666370f1010108035430 4f6767edafrom, from background scripts.

 Observe there is a NullPointerException, and related records are not restored.

</td></tr><tr><td>

Table Builder \(Family Release Channel\)

 PRB1801044

</td><td>

The user observes an error when toggling on/off contextual side panel ribbon components

</td><td>

There is an unexpected error.

</td><td>

1.  Log in as an Admin and create a scoped app.
2.  Share an app with a DD User.
3.  Log in as a DD user.
4.  Change the instance scope to Global.
5.  Create a Workspace and open WB.
6.  Once WB opens, select Record pages and open a Record page.
7.  Once the page loads select **Record Details** and select **Activity Stream**.
8.  Select **Contextual side panel**.
9.  Toggle on Components and Ribbon components.

 Expected behavior: Activity Stream and Ribbon component should work fine.

 Actual behavior: An unexpected error appears.

</td></tr><tr><td>

Territory Planning

 PRB1797546

</td><td>

Relocated technicians should be visible on the date selected in the Dispatcher Workspace

</td><td>

 

</td><td>

1.  Load the Dispatcher Workspace.
2.  Move the agent to another territory with the membership flow.
3.  Change the date for when the agent should be visible under the territory.

 Notice that relocated technicians are not visible on the date selected.

</td></tr><tr><td>

Transaction Management

 PRB1808714

</td><td>

The DISHv2 scheduled job has no drift or randomization, making requests stampede the datacenter instance every five minutes

</td><td>

The DISHv2 scheduled job has no drift or randomization resulting in requests stampeding the datacenter instance every five minutes, causing severe semaphore saturation, and rejections.

</td><td>

Search the logs for the execution of the job 'Check Glide Service Status V2'.

 Notice that it runs exactly every five minutes.

</td></tr><tr><td>

UI Field Administration

 PRB1793495

</td><td>

Service Operations Workspace has poor performance on CI fields

</td><td>

Poor performance of the CI field and its reference qualifier within an Incident record in SOW.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1795835

</td><td>

The campaign date picker opens in a lower position than usual

</td><td>

The campaign date picker, which is the calendar with a date and time selection field, is positioned offset and lower than its usual correct position.

</td><td>

1.  Install the latest Content Publishing and Content Experiences app.
2.  Navigate to the Content Experience Builder.
3.  Select the date pickers **Start Time** and **End Time.**

 Expected behavior: The date picker opens in the correct position.

 Actual behavior: The date picker is opens in a lower position than usual in the campaign builder.

</td></tr><tr><td>

UI Field Administration

 PRB1802956

</td><td>

Setting the dictionary attribute ref\_search\_on\_click to 'false' on any reference field causes inconsistent behavior on Workspace

</td><td>

Recent selection suggestions don't appear when expected.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1790795

</td><td>

The modal box **Close** button can't be hidden

</td><td>

When creating a modal box on a page in UI builder, the **Close** button isn't hidden in modal box even though the **Hide Close Button** switch is on.

</td><td>

1.  Create/Open a page in workspace.
2.  Add a modal box component \(choose a custom one\).
3.  In the Configure tab, turn on **Hide Close Button** and save.

 Notice that the **Close** button is visible on the modal box.

</td></tr><tr><td>

Upgrade Center

 PRB1797126

 [KB1704373](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704373)

</td><td>

The **Save Merge** button throws 'GlideList is not defined' error for ACL records when trying to resolve conflicts in Xanadu

</td><td>

When resolving conflicts for skipped records from an upgrade, the **Save Merge** record throws an error for ACL records in Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UXF Components

 PRB1808093

</td><td>

The getCurrentExperienceUrl helper method returns an incorrect URL

</td><td>

 

</td><td>

1.  Provision an instance with Service Operations Workspace apps 6.1.0-snapshot installed.
2.  Open the home page /now/nav/ui.
3.  Select **Service Operations Workspace** from the Workspaces menu.
4.  Open list page.
5.  Open **Incidents** &gt; **All**.
6.  Select row action with three dots.
7.  Select the Copy URL row action.

 Expected behavior: &lt;instance URL&gt;/now/sow/record/incident/&lt;sys\_id&gt;.

 Actual behavior: &lt;instance URL&gt;/now/nav/ui/sow/record/incident/&lt;sys\_id&gt;.

</td></tr><tr><td>

UXF Macroponent

 PRB1802268

</td><td>

A modeless dialog component seems to hide behind the Activity Stream in Safari

</td><td>

When the user selects the **View chat transcript** button in the origin card on the contextual side panel, the dialog opens on top of the sidepanel but under the Activity Stream.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1764778

</td><td>

New IN\_PAGE\_INTERACTION LIST\_MENU\_NAVIGATION reports lower TotalUITime in comparison with WPT execution

</td><td>

WPT Visual Complete is 2.3s. Client-interaction is 0.2s.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1766817

</td><td>

Wrong interruptions are being logged in client interaction records

</td><td>

Interruptions are incorrectly logged in client interaction records when experience and tabs switches are performed.

</td><td>

1.  Add a UI Time 'Before' column to the list.
2.  Add a UI Time 'After' column to the list.
3.  Order the list by the UI Time 'Before' column.

 Notice that the Total UI Time reports negative numbers, which are incorrect results.

</td></tr><tr><td>

UX Framework

 PRB1773096

</td><td>

Components using the now-trigger-library for a keyboard shortcut are not deregistering

</td><td>

Components should deregister if using now-trigger-library so that the reference to the host and update state of the component is not kept. However, uxfTriggerLibrary continues to grow as certain components are not deregistering.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1791818

</td><td>

When page load and tab get switched immediately, client interaction does not log a PAGE\_FOCUS\_OUT interruption

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1795528

</td><td>

'Content Download Time' \(CDT\) is zero when the classic page is loaded directly

</td><td>

 

</td><td>

1.  Navigate to any classic page rendered inside Next Experience's layout's iFrame.
2.  Check the sys\_client\_interaction table.

 Observe that CDT is 0.

</td></tr><tr><td>

UX Framework

 PRB1806207

</td><td>

Enable now alert message to expand/collapse \(admin. config\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1813571

</td><td>

The user observes a paragraph tag on a UCM model

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Wait for UCM model.
3.  Close this UCM model and open any record in a new tab.

 The user observes a paragraph tag in UCM pop-up.

</td></tr><tr><td>

UX Framework

 PRB1816477

</td><td>

The sys\_user.country detail in the app log table is not available even when the sys\_properties is true

</td><td>

The log sys\_user.country detail in the app log table is not available even when the system property glide.uxf.lib.performanc e.monitoring.log .user.country.code to set to 'true'.

</td><td>

1.  Navigate to sys\_properties.
2.  Setting the system property glide.uxf.lib.performanc e.monitoring.log.user.country.code to **true**.
3.  Validate the sys\_user.country detail in the app log table.

 Expected behavior: The sys\_user.country detail is available.

 Actual behavior:The sys\_user.country detail is not available.

</td></tr><tr><td>

UX-Metrics

 PRB1781625

</td><td>

Users observe an error in ClientInteractionRepository when running an ATF test for HR Agent Workspace

</td><td>

The error: 'Unexpected error occurred while parsing the json params: org.json.JSONException: JSONObject\['table'\] not found.: org.json.JSONObject.get\(JSONObject.java:301\)...'.

</td><td>

1.  Create a user with roles given for an HR agent.
2.  Navigate to the HR Agent Workspace homepage.
3.  Navigate to **Create new HR Case**.
4.  Select **Skip verification**.

 On the next page, users observe the error. The error isn't coming on the console, but on the system logs only.

</td></tr><tr><td>

Virtual Agent

 PRB1813250

</td><td>

Gen AI family release feature

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1819265

</td><td>

Follow-up queries that are not in English intermittently hang

</td><td>

As soon as follow-up utterance is submitted, VA Input extraction fails, preventing anything else from happening after that. This includes the creation of a sys\_cs\_fdih\_invocation record.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1819708

</td><td>

The feature name in sys\_gen\_ai\_usage\_log when running FSM record summary use cases is shown as 'Case summarization'

</td><td>

 

</td><td>

1.  Open a Work Order Task \(WOT\).
2.  Select the **Summarize** button.
3.  Navigate to the sys\_gen\_ai\_usage\_log table and open latest record for the above action.

 Notice that the feature name is 'Case Summarization'

</td></tr><tr><td>

Virtual Agent

 PRB1819726

</td><td>

Invoke FDIH API in non-interactive mode if request coming from NASK

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1820812

</td><td>

Skill discovery with Now Assist creator does not work

</td><td>

 

</td><td>

1.  Provision an instance with Now Assist for Creator 26.2.0 installed.
2.  Enable 'Data visualization skill' from 'Now assist skill for creator' under Now Assist feature \(**All** &gt; **Now Assist admin** &gt; **Now Assist features** &gt; **Creator**\)
3.  Enable 'Now Assist Panel' under Settings \(**All** &gt; **Now Assist admin** &gt; **Settings** &gt; **Now Assist panel**\)
4.  Navigate to NAP and send an utterance \(for example, 'number of open incidents by category'\).

 Observe that skill discovery does not work.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1819654

</td><td>

Some catalogs on Surf are not rendered correctly and have broken images

</td><td>

Cards are stretched and have broken images.

</td><td>

1.  Navigate to Now Assist Virtual Agent on ESC portal.
2.  Type 'I want to buy a laptop'.

 Expected behavior: The cards in the synthesized response should be rendered correctly and have respective images.

 Actual behavior: The cards in the synthesized response are stretched and have broken images.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1820457

</td><td>

Now Assist Virtual Agent \(NAVA\) doesn't auto-scroll to the top of a message

</td><td>

Since vaLegacyScrollingEnabled is set to false, the page should be auto-scrolled to the top of a Virtual Agent message. Instead it is scrolled to the bottom.

</td><td>

1.  Provision an instance with NAVA enabled and vaLegacyScrollingEnabled set to false.
2.  Send an utterance that results in a longer response \(for example, 'How does ESPP work?'\).

 Observe that NAVA auto-scrolls to bottom instead of the top of the long response.

</td></tr><tr><td>

Work Order Management

 PRB1782808

</td><td>

Manual update does not update the travel time

</td><td>

Travel back to home doesn't show at the end of the day when the 'Show travel time' home indicator is turned on in the settings.

</td><td>

1.  In Dynamic scheduling Config, navigate to any task filter and modify it immediately assign the tasks if some task is unassigned in the system.
2.  Assign any task manually for an agent

Observe that travel time is populated correctly.

3.  Un-assign the task and save.

Dynamic scheduling picks up the task and assigns it to an agent.


 Notice that the travel time doesn't match the DS travel time, and it sets to default travel time.

</td></tr><tr><td>

Work Order Management

 PRB1806645

</td><td>

The user observes an error while training due to a missing ACL

</td><td>

There is a missing ACL that grants read access to the platform\_ml\_read role for wm\_task table.

</td><td>

1.  Log in as admin.
2.  Navigate **All** &gt; **Process Mining** &gt; **All Projects** and open an existing project.
3.  Create a copy of the project and select **Generate models**.

 Observe that model generation fails.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 2 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1705551)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1 Hotfix 3](xanadu-patch-1-hf-3-PO.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


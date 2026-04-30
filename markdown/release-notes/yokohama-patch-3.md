---
title: Yokohama Patch 3
description: The Yokohama Patch 3 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-05-01"
reading_time_minutes: 80
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 3

The Yokohama Patch 3 release contains important problem fixes.

-   **Yokohama Patch 3 was released on May 01, 2025.**
    -   Build date: 04-30-2025\_1345
    -   Build tag: glide-yokohama-12-18-2024\_\_patch3-04-17-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y03.00.xlsx).

## Overview

Yokohama Patch 3 includes 285 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp3.png "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 3 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 3, refer to [KB2060631](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2060631).

## Changes in Yokohama Patch 3

-   **[Activate indexing of catalog variable content on Catalog Item records](https://www.servicenow.com/docs/access?context=activate-catalog-variable-indexing&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Activate indexing of searchable content from variables on Catalog Item records. Configure the set of Catalog Items eligible for catalog variable indexing and the set of variables to index.

-   **[AI Search system properties](https://www.servicenow.com/docs/access?context=system-properties-ais&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    **glide.ais.ingestion.catalog\_variables\_filter\_query**: Encoded query string for a query that Catalog Item records must satisfy to be eligible for catalog variable content indexing.

    **glide.ais.ingestion.ignore\_catalog\_variables\_read\_roles**: Option to allow indexing of searchable content from role-restricted catalog variables on Catalog Item records.

    **glide.ais.ingestion.index\_catalog\_variables**: Option to allow indexing of searchable content from globally accessible catalog variables on Catalog Item records.

-   **[Field Service Management release notes](../field-service-management/field-service-management-rn.md)**

    : 







-   **[Variable types supported by AI Search indexing](https://www.servicenow.com/docs/access?context=variable-types-ais-index&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Service Catalog variable types indexed from Catalog Items.


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

Agent Chat

 PRB1862727

</td><td>

A 'Show audio' modal appears when an agent presence state is changed to 'Available' for Safari users

</td><td>

A user interaction is required on the page for the audio to work, especially in inactive tabs. This was enforced by a modal when the audioContext was detected to be suspended, which occurs when a new AudioContext is created in the page. Now, the modal appears for Safari whenever the presence changes in the inbox to 'Available' to avoid having users refresh the browser to see the modal.

</td><td>

 

</td></tr><tr><td>

Form Builder

 PRB1820975

</td><td>

A form isn't saved on a cross scope in ServiceNow studio

</td><td>

There's an error in the networking calls.

</td><td>

 

</td></tr><tr><td>

List Filters

 PRB1801767

</td><td>

Japanese names cannot be filtered by a Japanese term but can be filtered by an English term under the Japanese setting

</td><td>

Unable to filter lists by **Translated Text** fields in non-English languages when using the non-English translation

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1870465

 [KB2022624](https://hi.service-now.com/kb_view.do?sysparm_article=KB2022624)

</td><td>

ECCSender does not use the correct character set when reading XML queue files

</td><td>

ECCSender uses the default file encoding/character set when reading XML queue files from a disk. This results in incorrect characters in the response for some special characters. ECCSender should use UTF-8 when reading these files, as XML queue files on disk are always UTF-8.

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

 PRB1859273

</td><td>

A query that consumes significant time is invoked every minute by the UserHasRole Patcher sys\_trigger

</td><td>

It's an issue with CSM performance.

</td><td>

Prepare an instance with CSM with 5 times the data.

 Observe the time taken by the query executed as part of the UserHasRole Patcher scheduled job.

</td></tr><tr><td>

Activity Stream

 PRB1830587

</td><td>

Activity Stream doesn't limit the size of **Journal** fields

</td><td>

The maximum size of journal entry appears to be either 50Kb or 100Kb by default. UI16 has a 10MB limit on the total **Journal** field size. Once this limit was reached it truncates every journal entry to 50K. The entry cap is 250 by default. The entry cap is 30 for attachments. The size cap + entry cap is what ensured no out of memory errors in UI16.

</td><td>

1.  Create a script that creates a 10MB work note. This can be a 100 character string that is appended to the work note 100,000 times in a loop.
2.  Add 2-3 of these to a single incident.
3.  Request the incident in Service Operations Workspace \(SOW\).

 Expected behavior: The incident should load with these massive strings.

 Actual behavior: Chrome and Edge crash as the browser runs out of memory.

 1.  Add 100 of the 10MB work notes from \#1.
2.  Request the incident.

 Expected behavior: The incident should load in SOW.

 Actual behavior: The Glide server crashes with an out of memory error.

</td></tr><tr><td>

Activity Stream

 PRB1834000

</td><td>

Reaper query needs an index to perform optimally

</td><td>

When the reaper query runs, it does not use an index to find the expired records.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1867023

</td><td>

When a blind transfer work item is created from a work item with the consult state as 'transferred', it retains the consult state

</td><td>

The agent can accept only work items created in the 'requested' or empty state.

</td><td>

1.  Have Agent 1 get a call.
2.  Agent 1 consult transfers to Agent 2.
3.  Agent 1 leaves the call.
4.  Agent 2 blind transfers to Agent 1.
5.  Agent 1 gets the offer card in their inbox.
6.  Agent 1 accepts.

 Observe that the card stays, and the work item is also always in a 'pending accept' state.

</td></tr><tr><td>

Agent Chat

 PRB1868186

</td><td>

The conversation history in the Agent Chat only displays one previous interaction

</td><td>

All previous closed conversations should be displayed, but only one past closed conversation is shown.

</td><td>

1.  Enable conversation history in Agent Chat in **Conversational Settings** &gt; **Agent Chat** &gt; **Conversation History**.
2.  Log in as an agent in Safari.
3.  Log in as a non-guest user in any other browser.
4.  Start a conversation and accept as an agent.
5.  Close the conversation.
6.  Have a few more conversations \(about 2-3\) and close them.
7.  Start a new conversation and scroll up to see the past closed conversations in the chat panel in Agent Chat.

 Expected behavior: All previous closed conversations \(up to the amount configured in the conversation history settings\) are shown.

 Actual behavior: Only one past closed conversation is shown.

</td></tr><tr><td>

AI Search

 PRB1783862

</td><td>

The wrong search events get deleted due to incorrect sort logic

</td><td>

The method called via a scheduled job that runs weekly deletes signals that are both older than 90 days and are older than the 500K 'most recent' search events for the search application. When an end user closes a suggestion from their recently searched terms, it causes the **suggest\_to\_user** field on the sys\_search\_event record to be updated, which updates the **sys\_updated\_on** field in the process. This can lead to older search events that have suggest\_to\_user set to 'false' being preserved over newer ones that the user may still wants as a suggestion.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1824166

</td><td>

A translated reference field is indexed in a different language in a single record update vs a full table index

</td><td>

The peekahead is using the same value for different languages.

</td><td>

1.  Enable i18n Spanish.
2.  Insert a KB record kb\_knowledge\_base=knowledge, language=es.
3.  Wait for incremental index and dump the document.
4.  Verify that kb\_knowledge\_base is in Spanish.
5.  Re-index kb\_knowledge.
6.  Wait for incremental index and dump the document.

 Expected behavior: kb\_knowledge\_base is in Spanish.

 Actual behavior: kb\_knowledge\_base is in English.

</td></tr><tr><td>

AI Search

 PRB1841579

</td><td>

sn-search-combobox-desktop's use of createGraphQLEffect dispatches errorActionType due to a 401 error for public GraphQL endpoints

</td><td>

The batch request fails due to 401 even though the GraphQL request in the batch was actually successful.

</td><td>

1.  Set the Service Portal home page to public.
2.  Set the Typeahead Search widget to public.
3.  Open Service Portal without logging in.
4.  Open Developer Tools.
5.  Select the search box.

 Observe in Seismic Dev Tools that the batch request failed due to 401. Then, observe in the Network tab that the GraphQL request in the batch was actually successful.

</td></tr><tr><td>

AI Search

 PRB1847810

</td><td>

When multi-node ingestion is enabled on a production instance, all cloned instances from production enable multi-node ingestion

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1856064

</td><td>

Now Assist Panel \(NAP\) displays the error, 'Trouble processing your request' while promoted skills are working correctly

</td><td>

The skill is not being identified and indexing is not occurring automatically on the 'Skill' table. Skill discovery is not happening, and the following error message is displayed: 'We're having trouble processing your request right now due to a temporary system issue. Please try again later.' However, when the 'Skill' table is manually indexed, the skill gets discovered.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1860558

</td><td>

The indexing history of a quick test on an admin console does not show a link to the platform indexing history page

</td><td>

The start time column should be populated with a link to an indexing history record, but instead it is blank.

</td><td>

1.  Using admin console V5, select any indexed source.

Notice that it redirects to the indexing history page and the indexing history record is created after a couple seconds.

2.  Reload the list.

 Expected behavior: The start time column is populated with a link to an indexing history record on the platform.

 Actual behavior: The start time column is blank.

</td></tr><tr><td>

AI Search

 PRB1863971

</td><td>

RAGRertirval API throws an error if the searchSource given request is not present

</td><td>

When the user submits a RAGRetrieval API request with a search source that is not part of the search profile or is not an indexed source, RAGRetrievalAPI fails with no search results.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1869616

</td><td>

RAG capability isn't honoring return fields for child tables' columns

</td><td>

 

</td><td>

Try invoking Uber Rag or Retriever capability with child tables columns as return fields.

 Expected behavior: Child table fields should be returned in the response.

 Actual behavior: Child table fields aren't returned in the response.

</td></tr><tr><td>

AI Search

 PRB1870966

</td><td>

When topics are searched, the term logged to the suggested utterance table is unrelated to the topic

</td><td>

 

</td><td>

1.  Ensure that utterance readers are mapped to the search application.
2.  Search a topic on the portal.

It should return a synthesized Genius Results answer.

3.  Check that the utterance is logged to the sys\_suggested\_utterance table.

 Observe that the logged term is sometimes unrelated to the topic searched.

</td></tr><tr><td>

AI Search

 PRB1871798

</td><td>

Dynamic Window \(DW\) chat returns an error reading 'Sorry there was a problem on my side'

</td><td>

 

</td><td>

1.  Enable dynamic window on Service Portal
2.  Perform a search in chat.

 Notice an error that reads 'Sorry there was a problem on my side'.

</td></tr><tr><td>

AI Search

 PRB1878130

</td><td>

External content ingestion isn't sending a URL to AI Search's \(AIS\) backend

</td><td>

 

</td><td>

1.  Ingest a KB document.
2.  Observe AI Search \(AIS\) backend logs.
3.  Create external content setup.
4.  Start an external content ingestion, like web crawler.
5.  Observe AIS backend logs.

</td></tr><tr><td>

AI Search

 PRB1878248

</td><td>

Auto-correct is not turned off in search if it's triggered from the chat

</td><td>

Auto-correct should be turned off if a search is triggered from chat, and a rewritten query should be used.

</td><td>

1.  Navigate to search toggle in Full Page Experience.
2.  Search for 'Abel Tuter'.

 Expected behavior: It should search for Abel Tuter.

 Actual behavior: The search term gets auto-corrected to Abel Tuner and does not return any result.

</td></tr><tr><td>

AI Search

 PRB1881968

</td><td>

The full page responsive mobile is unusable

</td><td>

The pre-search box is cropped on both the left and right sides. The search results search box is cropped and buttons aren't accessible.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1882714

</td><td>

A KG response in streaming mode might stream 'kg\_information'

</td><td>

 

</td><td>

1.  Set up NA4S and NAVA on the instance.
2.  Set up KG.
3.  Ensure to enable streaming.
4.  Run a KG people search query.

 Expected behavior: 'kg\_information' shouldn't be part of streaming text.

 Actual behavior: Sometimes a streaming answer might contain the string 'kg\_information'.

</td></tr><tr><td>

AI Search

 PRB1882832

</td><td>

Fix tracer functionality end-to-end for search use cases

</td><td>

 

</td><td>

1.  Perform end-to-end searches.
2.  Collect search timings.

</td></tr><tr><td>

AI Search

 PRB1883872

</td><td>

A FPE new search isn't routed to the 'All' tab

</td><td>

 

</td><td>

1.  Open an instance with a May Store app.
2.  Ensure that FPE is enabled on the ESC portal.
3.  Search for the query 'what is cookie?'.
4.  Toggle the search.
5.  Perform the search again.
6.  Navigate to the 'Knowledge' tab.
7.  Perform a new search 'Apple iPhone' while still on the 'Knowledge' tab.

 Notice no results are found.

</td></tr><tr><td>

AI Search

 PRB1883953

</td><td>

Signals aren't being captured for a carousel on the Portal

</td><td>

This isn't working for synthesized Genius results either.

</td><td>

1.  Open an instance with May store apps.
2.  Enable Now Assist QnA and Now Assist Actions on portal.
3.  Perform search for queries 'Apple Iphone' and 'what is spam?'.
4.  Perform actions like 'Open source'.
5.  Trigger the 'Process Queued Signals' job.

 Expected behavior: Signals should be logged in the sys\_search\_genius \_result\_event\_action\_list table.

 Actual behavior: Notice no entries are found in the sys\_search\_genius \_result\_event\_action table.

</td></tr><tr><td>

AI Search

 PRB1884610

</td><td>

When a dynamic window is active, reloads on the search page result in double queries

</td><td>

 

</td><td>

1.  Navigate to the Portal.
2.  In the main search bar \(not the NAVA chatbot\), enter 'what is spam?'.

Portal Genius results return.

3.  Navigate to sys\_generative\_ai\_log and see there is one synthesized QnA response.
4.  Return to the page where the genius result is already displayed and reload the page.
5.  Navigate back to the sys\_generative\_ai\_log and observe there are two synth QnA capability calls. One has a conversationID of DefaultAISearch and one has a NAVA conversation ID.

 Observe that it acts as if the query was simultaneously entered from both the NAVA chatbot interface and also the Portal search bar.

</td></tr><tr><td>

AI Search

 PRB1887382

</td><td>

For Global search, subsequent searches can't be submitted

</td><td>

There is no issue on Service Portal.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1847323

</td><td>

The apply\_to object isn't parsing properly for custom data sources in a multivisdata API

</td><td>

 

</td><td>

1.  Add a custom data source.
2.  Create a resolution API for the data source.
3.  Add a filter to the inline dashboard with the data source and a visualization.
4.  Save the dashboard.
5.  Select something from the filter.
6.  Check the multivisdata API and see the filter configuration where apply\_to object has valid values.
7.  Once applied, check the data provider method defined in sys\_viz\_data\_source table.
8.  Check the request body passed to this method.

 See the apply\_to object is passed as an empty list.

</td></tr><tr><td>

Application Install Engine

 PRB1846815

</td><td>

Admins users aren't able to repair/install all dependencies when domain separation is enabled

</td><td>

An issue was observed where a parent application \(for example, Now Assist For CSM\) was installed successfully, even though its dependencies \(for example, sn\_genai\_platform\) weren't installed during the process. This behavior is unexpected.

</td><td>

1.  Open an instance where domain separation is enabled.
2.  Create an admin user in a different domain.
3.  Log in or impersonate as that admin user.
4.  Change the domain to global.
5.  Attempt to install a parent application with known dependencies.

New dependencies aren't installed and there's domain related errors in plugin logs.

6.  Try to repair the same plugin.
7.  Verify that the new dependencies are still not installed and the domain related errors in plugin logs are still present.

 All the dependencies should be installed with the parent app.

</td></tr><tr><td>

Appointment Booking

 PRB1874123

</td><td>

When a slot's end time is 'Arrive by', unavailable slots are displayed as available

</td><td>

In the case of 'Arrive by', when an appointment is being booked, it is only considering the exact slot's worth of block while making the booking. However, the slot may have been shown as available since the work could have been done between a time. After post-performance changes, it isn't adding the additional 30 min that is normally done when booking of the slot, which is leading to an available slot not being booked.

</td><td>

1.  In the appointment booking configuration, select the use slot end time as 'Arrive by'.
2.  Configure the slots from 5AM, the appointment window as 2 hours, and the work duration as 1 hour.
3.  Create a work schedule for an agent from 8-5.

 Observe that the first slot 5-7 should be unavailable but it is displayed as available. However, when an appointment is booked for that slot, it throws an error.

</td></tr><tr><td>

Authentication

 PRB1852202

</td><td>

A 'Tracking' status isn't changing to self-enrollment in a tracking table

</td><td>

 

</td><td>

1.  Log in via an admin.
2.  Enable MFA, AA and MFA context.
3.  Navigate to sys\_properties.list.
4.  Set SWP to 30 and MAX\_SWP to 90.
5.  Log in via a newly created user or any existing user.
6.  Navigate to a profile and configure MFA.
7.  Log in via an admin.
8.  Navigate to the sys\_user\_mfa\_enforcement\_info.list.

 Expected behavior: The status should change from 'Tracking' to 'Self Enrolled'.

 Actual behavior: The status doesn't change; it remains as 'Tracking' only.

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1868046

</td><td>

Event cells of capacity on a calendar aren't visible in the dark coral theme

</td><td>

 

</td><td>

1.  Enable the coral theme dark mode.
2.  Open capacity console using a user with elevated privileges.

 The user should be able to view the event cells without any issue.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1852603

</td><td>

A record handling agent is unable to fetch HR case details

</td><td>

The record handling agent gives an error: 'The system is unable to get the record information'.

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB1872131

</td><td>

Clustering isn't triggered because of a missing ACL

</td><td>

 

</td><td>

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Feature** &gt; **Now Assist Skills**.
2.  Select **suggested steps generation skills**.
3.  Select **clustering progress**.

 Observe that the clustering progress bar is stuck.

</td></tr><tr><td>

Change Advisory Board \(CAB\) Workbench

 PRB1870269

</td><td>

There's a 'Write operation against 'cab\_definition' from scope 'sn\_sow\_chg' has been refused due to the table's cross-scope access policy' alert present after selecting **Refresh CAB meetings** on SOW CAB Definition

</td><td>

**Refresh CAB meetings** actions in UI16 work without any issues, but returns an error in Service Operations Workspace.

</td><td>

1.  Log in.
2.  Navigate to **SOW** &gt; **Change Advisory Board** &gt; **All CAB Definitions**.
3.  Select **New**.
4.  Populate mandatory fields.
5.  Create scheduled entries from the 'Related records' tab via the **New** button.
6.  Populate mandatory fields.
7.  Select **Submit**.
8.  See a scheduled entry created for the CAB Definition.
9.  Select the 'Details' tab.
10. Select the **Refresh CAB Meetings** button.

 Expected behavior: CAB Meetings are generated without errors/alerts.

 Actual behavior: CAB Meetings generated with an error/alert: 'Write operation against 'cab\_definition' from scope 'sn\_sow\_chg' has been refused due to the table's cross-scope access policy" presents on the form'.

</td></tr><tr><td>

Change Management

 PRB1849821

</td><td>

The **Closed Change Count** field under the 'std\_change\_ record\_producer' table is calculated incorrectly when multiple template records are created with the same template name

</td><td>

This is caused because the 'group by' query defined in the script 'StdChangeUtilsSNC' inside the function 'calculateVersionAndTemplateStats' is attempting to group by on the name rather than the sysID, which is leading to the incorrect calculation of the closed change count.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1875123

</td><td>

CAB AMB controller is too strict on the number of parameters passed on registration, preventing enhancements for Store applications

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1880887

</td><td>

com.snc.change\_management .standard\_change\_catalog is activated on an upgrade

</td><td>

com.snc.change\_management. standard\_change\_flows is installed on an upgrade and zboot. This has a dependency on the standard change catalog. The dependency needs to be removed.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1854759

</td><td>

Frequent updates on the 'sn\_kmf\_record\_signature' table leads to excessive generation of text index events

</td><td>

Frequent updates on the 'sn\_kmf\_record\_signature' table leads to excessive generation of text index events, delaying the text index events processing on the instances.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1860810

</td><td>

Generate signatures for sys\_auto\_script table with wildcard mode

</td><td>

Generating signatures for sys\_suto\_script table records as they are invoking scripts writing to ecc\_queue directly from sys\_auto\_Script.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1869613

</td><td>

Guardrails should respect filter conditions on the signature configuration

</td><td>

Don't validate signatures for records not meeting filter conditions, and skip validating records that don't participate in MID.

</td><td>

Run guardrails.

 Observe that it validates all signatures and doesn't care about filters.

</td></tr><tr><td>

Column Level Encryption

 PRB1829680

</td><td>

Key Migration should succeed when EFCs and tables are in different scopes

</td><td>

When the EFC scope is different from the configured table scope, the key migration job will not modify it and fail the key migration. Key migration fails due to a scope mismatch between EFCs and the associated table during key migration.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1845617

</td><td>

A duration editor is modifying the typed in value and adding to it

</td><td>

 

</td><td>

1.  Navigate to a Yokohama instance.
2.  Navigate to now/SOW/list.
3.  Select the **Incidents** &gt; **All.**
4.  Open the PCB by selecting the **Filter** button.
5.  Select a duration value editor.
6.  Type the '1' character into the **Days** field.

 Expected behavior: It should set the value to what the user types in, but something is modifying the value before it goes to the editor.

 Actual behavior: The value for days jumps to 3079 with hours red and set to -1.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1868449

</td><td>

Fix family compatibility issues for the 'Reject task' feature

</td><td>

The Data Manager \(DM\) subflow does a double rejection process for rejected tasks in the Workspace, and the business rule 'Clean up TaskToCI records' fails to process records with a NullPointerException.

</td><td>

1.  Create a DM retire policy on the cmdb\_ci table where the condition name starts with 'SAP'.
2.  Assign the policy to user.
3.  Publish the policy.
4.  Run the scheduled job 'SNC.CMDBDataManager ScriptableApis. executeRetirePolicies\(\);'.
5.  Notice that a task is assigned to a user.
6.  Impersonate the user.
7.  Open the CMDB Workspace.
8.  Navigate to **Open my task** &gt; **Open the task** &gt; **Review task** &gt; **Reject**.
9.  Give a reason for the rejection.
10. Select **Save**.
11. Observe that the task is rejected successfully, and CIs should be available for any other DM policy to pick up.
12. Re-run the same scheduled job 'SNC.CMDBDataManager ScriptableApis. executeRetirePolicies\(\);' or any other policy process.

 Expected behavior: A new task should be created with the CIs with the matching condition because the task was rejected.

 Actual behavior: No task is created, and the cmdb\_data\_management\_task\_to\_ci table is not clearing the old CIs from the rejected task.

</td></tr><tr><td>

Content Management System

 PRB1880403

</td><td>

The CMS portal is corrupted after a Yokohama upgrade

</td><td>

It looks like there are CSS files for the portal that aren't loaded as expected.

</td><td>

 

</td></tr><tr><td>

Contextual Search

 PRB1872960

</td><td>

An external link can no longer be accessed in the cxs\_new\_window UI page

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Core Platform

 PRB1881092

</td><td>

In an activity stream, be able to determine actions performed by an AI Agent on behalf of a user

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB1848565

</td><td>

Creating a consumer user from a consumer form doesn't work

</td><td>

Creating a consumer user from a consumer form creates a sys\_user, not a csm\_consumer\_user. As a result, this user can't be linked with a consumer. This process should work according to documentation.

</td><td>

1.  Open any csm\_consumer record.
2.  Navigate to the 'Login Details' related list.
3.  Select the **User lookup** icon.
4.  Select **New** to create a user.

 Expected behavior: The user created should be csm\_consumer\_user, so this user can be linked with csm\_consumer.

 Actual behavior: The user created is sys\_user, so users can't select this user to link it with csm\_consumer.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1833232

</td><td>

There's an incomplete 'NULLS FIRST' clause in multi-column indexes on new \(non-migrated\) RaptorDB instances

</td><td>

This means that all multicolumn indexes can't leverage their natural sort order.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1881074

</td><td>

Provide introspection methods to get back the table/prefixes for views in the Genius Results returned from cypher2Results

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1861048

</td><td>

ServiceNow documentation is showing incorrect information for 'Clean peripheral' option

</td><td>

ServiceNow documentation needs to be updated regarding the 'Clean peripheral' option in the Table cleaner form. The default behavior when a parent record is deleted is that the system will automatically delete records from sys\_attachment table and not 'sys\_journal\_field' table.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1800841

</td><td>

JavaScriptMembers, ScriptableObject, and JavaMembers use a HashTable that causes a concurrency bottleneck

</td><td>

The 'get' method is synchronized. The HashTable is initialized and then not modified again. It's unnecessary to synchronize all 'get' access.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1846741

</td><td>

Adjust tuple size thresholds to avoid failing legitimate queries

</td><td>

Adjusting the threshold to a reasonable value to avoid failing some queries.

</td><td>

1.  Create a query pattern record with sizable executable SQL.
2.  Attempt to open the query pattern record.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1859279

</td><td>

StringCache causes a concurrency bottleneck due to SynchronizedLRU

</td><td>

Enhance StringCache to support a large volume of concurrent requests.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1823462

</td><td>

Document Q&amp;A should skip .docx processing once it started using Document Reader Processing API

</td><td>

 

</td><td>

Install the plugins 'Now Assist in Document Intelligence' and 'Generative AI Controller'.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1862011

</td><td>

Brief description shows a space in the 'General Details' page

</td><td>

Fields are showing empty when referred, as the display name is empty.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1862455

</td><td>

An extraction flow throws an error for a use case that has only a field group

</td><td>

Users get an error message: 'java.lang.IllegalArgumentException: objectToMap: invalid type class com.snc.process\_ flow.engine.serialization. GRProxy$1 for object property targetRecord \(sys\_script\_include. 4a035a2beb771110 f2549bf12a522841 .script; line 530'.

</td><td>

1.  Create a use case with a target table.
2.  Create fields that have a field group.
3.  Create integration flows and activate them.
4.  Create a record in the target table.
5.  Test the extraction flow with the created document task.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881095

</td><td>

Add 'description' and 'autogenerated\_summary' to a task definition

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881127

</td><td>

Turn off the embedded image extraction option for PDFs and Docx

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881128

</td><td>

Introduce the docx4j library to Glide env

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881129

</td><td>

Fix 'fileId' null issue in Glide Java

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881130

</td><td>

In 'Chat with doc', classify if it's a scanned or digital PDF

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881131

</td><td>

Move Docx4j to 8.3.13 in Xanadu and Yokohama Now Assist

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881132

</td><td>

In Docx4j, create a scriptable extractText Java function which takes a docx file and gives an attachment ID for a text file

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881133

</td><td>

Support the .txt file format

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881134

</td><td>

Adding a **PDF** &gt; **IMG** null pointer exception to Xanadu and Yokohama Now Assist

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881135

</td><td>

Extract text and embedded images using Docx4j for Docx and pdfbox for PDFs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881136

</td><td>

Glide API to convert a PDF to an image

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881137

</td><td>

Fix the Docx path for custom XML so extraction of the text is successful

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Dynamic Translation for Virtual Agent

 PRB1848023

</td><td>

Messages sent for DT are always using the system language property \(glide.sys.language\), which could result in LLM messages not being translated

</td><td>

This can cause LLM responses to go directly to the user without any translation taking place. This visible text is not hardcoded, but received from the LLM.

</td><td>

1.  Set glide.sys.language to a non-English language.
2.  Ensure the com.glide.cs.llm.default.Language is English/en.
3.  Ensure that native translations is turned off.
4.  Create a custom LLM topic in the same language as the system property language.
5.  Add some LLM components, such as an LLM enabled bot response.
6.  Publish the LLM topic.
7.  Set the session language to the same language as the glide.sys.language property.
8.  Start a Now Assist Virtual Agent \(VA\) conversation.
9.  Trigger the new topic.
10. Observe the results.
11. Set session language to the same language as the LLM default language.
12. Start a Now Assist VA conversation.
13. Trigger the new topic.
14. Observe the results.
15. Set session language to a language different than the LLM default language and the system property language.
16. Start a Now Assist VA conversation.
17. Trigger the new topic.
18. Observe the results.

 Expected behavior: VA responses are in same language as the session language.

 Actual behavior: VA responses may be mixed, with LLM responses in the default LLM language.

</td></tr><tr><td>

Dynamic Translation

 PRB1883401

</td><td>

The synthesized QnA capability fails for P3 languages when invoked from a Portal interface

</td><td>

 

</td><td>

1.  Navigate to a Service Portal page.
2.  Enter 'Vad är Sverige?' as a Swedish session user in the main portal page.
3.  Navigate to the generative AI log and observe 'Error occurred during Generative AI execution' for a synth QnA invocation.

 In the one\_api\_service\_plan \_feature\_invocation table, see that the error message is given: 'Cannot invoke 'com.glide.oneapi. entity.FeatureInput. getPayload\(\)" because the return value of 'com.glide.cs.qlue. module.oneextend. proxy.trackers. GenAIExecutionTracker .getOriginalRequest\(\)' is null'. If sn\_vad\_genai. com.glide.cs.one\_ extend.auto\_ proxy\_enabled is set to false, the E2E works successfully.

</td></tr><tr><td>

Embedded Help

 PRB1870178

</td><td>

The embedded help link redirects to the page 'not\_allowed.do' instead of the documentation site

</td><td>

The issue occurs in the Yokohama release.

</td><td>

1.  Open a Yokohama instance.
2.  Open the 'cmdb\_ci\_business\_app' or 'incident' table.
3.  In top right corner, select the **?** or the 'Show help' icon.
4.  Scroll down to link.
5.  Select it.

 Expected behavior: Users are redirected to the documentation.

 Actual behavior: Users are redirected to the 'not\_allowed.do' page.

</td></tr><tr><td>

Employee Center

 PRB1818417

</td><td>

JavaScript console errors on the Human Resource Management \(HRM\) ticket page

</td><td>

Navigating to the 'to-do' page displays console errors.

</td><td>

1.  Create a HR case - Employee Travel Visa Request for an employee with the manager 'Abel Tuter'.
2.  Let the case move to 'Awaiting approval'.The approval record is created for a user with no roles \(in this case - Abel\).
3.  Open the approval task in the 'to-do's' page.
4.  Select **HR Service**, which opens the 'HRM ticket' page.
5.  Select the approval to-do in the 'HRM ticket' page.

 Expected behavior: The user should be able to approve or reject the task from the 'HRM ticket' page.

 Actual behavior: The 'to-do' page has console errors.

</td></tr><tr><td>

Encryption

 PRB1854358

</td><td>

Protected script decryption fails for a cloned instance which is upgraded before the 'Protected Script Values Migration' job is executed

</td><td>

 

</td><td>

1.  Create a Xanadu/Yokohama instance.
2.  Create a 3des data.
3.  Clone the instance into other instance.
4.  After the clone is successful, verify the key exchange won't happen and the cm\_glide\_protected \_script\_encrypter module key isn't present in the instance.
5.  Upgrade the instance before the 'Protected Script Values Migration' job runs and keys are created.

 After an upgrade is successful, as the static key is removed and the key isn't available, protected scripts decryptions fail.

</td></tr><tr><td>

Field Service Quality Management

 PRB1860999

</td><td>

The dictionary override on wm\_task causes issues

</td><td>

In a Washington DC instance, there's no override attribute for the **State** field at the wm\_task. In the Xanadu, the override attribute is introduced for the **State** field at the wm\_task.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1751544

 [KB1710818](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710818)

</td><td>

There's a change in behavior from V1 to V2 in handling JS arrays

</td><td>

This change in behavior causes the failure of a following REST step in a Surf action where the 'If\_Matches' header who's value is 'etag' isn't matching.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1854665

</td><td>

Asynchronous business rules are not getting triggered on sys\_flow\_context when the condition has a 'change' operator

</td><td>

The business rule 'Testing flow rules' is not triggered even if it is changed after the update, and does not work on async.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1867133

</td><td>

The **Summarize** quick action gives a 'The current execution is in the waiting state' message

</td><td>

The flow caller is present. Async HTTP is used and that causes flows to go to a waiting state while waiting for the Async HTTP response. The 'The current execution is in the waiting state' exception is expected when Async HTTP is used.

</td><td>

1.  Log in to the instance as an admin.
2.  Navigate to ESC portal.
3.  Initiate a chat with LA.
4.  Log in as a user and accept the work item.
5.  Trigger the **Summarize** quick action.

 Expected behavior: The **Summarize** action should show the chat summary.

 Actual behavior: The quick action gives a 'The current execution is in the waiting state' message and an error in the sys\_log.

</td></tr><tr><td>

Flow Engine

 PRB1874438

</td><td>

There's a 'LLM Instruction Executor' error on flow execution

</td><td>

 

</td><td>

1.  Log in as a user with elevated privileges.
2.  Activate the plugin com.glide.utilities.capability\_step.
3.  Create an action.
4.  Add a LLM step to the action.
5.  Create a flow.
6.  Add the action created in step 3.
7.  Run the flow.
8.  Users see a 'LLM Instruction Executor' error when running the flow with LLM step.

</td></tr><tr><td>

Flow Engine

 PRB1874873

 [KB2042735](https://hi.service-now.com/kb_view.do?sysparm_article=KB2042735)

</td><td>

A deserialization issue occurs to flows when upgrading from Washington DC to Yokohama

</td><td>

Flows containing the 'Make a decision' logic don't resume and error out after upgrading to Yokohama. This is caused by a deserialization issue in Flow Engine V2, which prevents the flow from progressing.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1878005

</td><td>

The success status for the **Call Now Assist Skill** action step is displayed differently

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Enable Now Assist.
3.  Enable flow summarization.
4.  Enable a flow generation skill.
5.  Create a flow.

The install plugin ID: com.glide.utilities. now\_assist\_skill\_step.

6.  Create an action to the above flow and add the 'Call Now Assist Skill' step.
7.  Run the flow.
8.  Once the flow succeeds, check the status.

 Notice that the success status for the 'Call Now Assist Skill' action step is empty.

</td></tr><tr><td>

Flow Engine

 PRB1880998

</td><td>

Unable to deserialize a 'Make a decision' instruction after upgrading to Yokohama

</td><td>

When the flow is in a 'Waiting' state in the Washington DC release with Engine\_V2, the event opening the flow execution fails after upgrading to the Yokohama release.

</td><td>

1.  Create a flow with a 'Make a decision' flow logic.
2.  Ensure the flow has a waiting scenario so that flow\_context goes to a 'Waiting' state.
3.  Execute the flow.
4.  Ensure the flow is in a 'Waiting' state in the Washington DC release with Engine\_V2.
5.  Upgrade the instance to Yokohama.
6.  Notice that the event opening the flow execution in **Operation view** fails, and resuming the flow by satisfying the waiting condition fails.

 Expected behavior: The flow should resume on Yokohama without any errors.

 Actual behavior: The flow errors out in Yokohama.

</td></tr><tr><td>

Flow Engine

 PRB1881094

</td><td>

Create the ability to pass the context of the AI agent that triggered the flow

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flow Generation \(Family\)

 PRB1881140

</td><td>

Flow generation Glide changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1837338

</td><td>

Seeing log errors and warnings when creating flows

</td><td>

No functional breakdowns were seen, but the errors are consistent when creating flows.

</td><td>

1.  Impersonate a GenAI user with NAC, preferably an admin.
2.  Navigate to Workflow Studio.
3.  Create a flow.
4.  Use a build with Now Assist.
5.  Use any example and select **Generate preview**.
6.  While the flow is generated, select the 'Network' tab.
7.  Copy the transaction ID from the response payload.
8.  On the other tab, open **All** &gt; **System log** &gt; **Utilities** &gt; **Node Log File Browser**.
9.  Paste the transaction ID in the **Message** field.

 Observe the logs.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1839860

</td><td>

Trigger Designer role users face insufficient access errors and missing options in the 'Application' list for external triggers

</td><td>

When attempting to open the external trigger created using Github Spoke or Jira Spoke as a user with the trigger\_designer role, the error message appears, 'Insufficient level of access for eventsource'.

</td><td>

1.  Log in as a user with the admin role.
2.  Create an external trigger using GitHub Spoke or Jira Spoke.
3.  Log out.
4.  Create a new user with the trigger\_designer role.
5.  Log in as the user with the trigger\_designer role.
6.  Navigate to the Workflow Studio.
7.  Attempt to open the external trigger created.
8.  Observe the error banner that appears displaying the message, 'Insufficient level of access for eventsource'.
9.  Attempt to create a new external trigger.
10. Select the trigger type as **Event** on the trigger creation page.
11. Verify the Application list.

 Notice that the Application list no longer shows any options.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1865407

</td><td>

Mismatching data on an action instance can cause issues with flow execution

</td><td>

Actions don't perform as expected in various ways.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1869580

</td><td>

Subflow creation through image issues

</td><td>

Images are partially generated, or are returned with placeholders.

</td><td>

Attempt to create a subflow with attached images.Notice that they are partially generated or placeholders are returned for whole image.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1873141

</td><td>

CopyFlow doesn't set generationSource values as empty

</td><td>

 

</td><td>

1.  Create a flow with a trigger/action/subflow/flowlogic instances using Flow Generation.
2.  Copy the flow.
3.  View generationSource value on the flow and trigger/action/subflow/flowlogic instances on the copied flow.

 Expected behavior: All generationSource values are blank.

 Actual behavior: All generationSource values in trigger/action/subflow/flowlogic instances are 'text2Flow'.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1873639

</td><td>

The icon for 'Call Now Assist Skill' isn't correct

</td><td>

 

</td><td>

1.  Create an action.
2.  Add a LLM step to the action.
3.  Create a flow.
4.  Add the action created in step 1.
5.  Run the flow.

 Observe a 'LLM Instruction Executor' error.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1874240

</td><td>

Update the description of the flow family in **Now Assist Features** &gt; **Creator** &gt; **Flow in 'Now Assist Features**

</td><td>

It should read: 'Reduce flow creation time by building a multi-step flow with generative AI. Make editing flows easier by showing users recommendations for the next step of their flow. Learn about a flow by generating a summary.'

</td><td>

1.  Navigate to **Now Assist Features** &gt; **Creator** &gt; **Flow**.
2.  Check the description.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1874414

</td><td>

Changing the name of a step to 'Call Now Assist Skill'

</td><td>

The plugin isn't automatically enabled. It needs to be enabled by an admin. The name of the step should be changed to 'Call Now Assist Skill'. The name of the plugin should change accordingly to 'ServiceNow Call Now Assist Skill Step Plugin'.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1874640

</td><td>

There's a FlowSkeletonGlideRepository ::isAccessibleTable\(\) error if accessed in a background script

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1875963

</td><td>

There's a missing image attachment and prompt on Get Flow API

</td><td>

This issue occurs when using 'Build with Now Assist' in the Workflow Studio.

</td><td>

1.  Log in to a ServiceNow instance.
2.  Impersonate a delegated Gen AI user with NAC.
3.  Navigate to Workflow Studio.
4.  Create a flow.
5.  Use **Build with Now Assist**.
6.  Upload an image.
7.  Create a flow.
8.  Refresh the page once the flow is created.
9.  Observe the Get Flow API response.

 Expected behavior: The attachment ID and image prompt from the image generation can be seen.

 Actual behavior: There is no image prompt or attachment ID.

</td></tr><tr><td>

Flows

 PRB1868224

</td><td>

In Flow Designer, a dynamic choice isn't using a child alias

</td><td>

As a result, the first dynamic choice field value doesn't display as selected. This issue is happening in Xanadu and Yokohama versions.

</td><td>

1.  Create a connection alias with a parent and child alias.
2.  Consider the **Create issue** action, or anything that uses dynamic choices.

 In the flow override aliases, observe that the override to the child alias doesn't happen in the cases of dynamic choices.

</td></tr><tr><td>

Form Builder

 PRB1828559

</td><td>

Changing a field type doesn't surface errors on saving

</td><td>

 

</td><td>

1.  Navigate to the ServiceNow studio home page.
2.  Open a table in Table Builder.
3.  Select a field.
4.  Change the type of the field to reference from string when some data is in a record in that field.

 Expected behavior: An error message telling the user why the save failed.

 Actual behavior: The save silently fails.

</td></tr><tr><td>

Form Builder

 PRB1836580

</td><td>

Selecting **Edit in Original Scope** from the Form Builder banner enables the override properties of the field for editing

</td><td>

When a field is inherited from a parent table, it has the ability to override field properties. Previously, override properties were controlled by isFormReadOnly. However, with this PR update, the implementation has been refined how readability is determined.

</td><td>

 

</td></tr><tr><td>

Form Controller

 PRB1876936

</td><td>

GFORM\#ADD\_DECORATION isn't working in forms workspace like in they are in UI16 as g\_form.addDecoration

</td><td>

 

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

 PRB1833479

</td><td>

Upgrade a fix by removing previous sys\_choice records for the 'Application Id' list

</td><td>

In Washington DC, a release application ID was originally configured as a list that relied on sys\_choice list. In the later releases, this was changed to be a list that relied a new table that defined the configured applications which are associated to its respective Hermes service.

</td><td>

1.  Configure an instance on a Washington DC release.
2.  Note sys\_choice list entries for 'Application ID'.
3.  Upgrade the instance to.

 Note that the 'Application ID' list uses the reference table, but the sys\_choice\_list entries still exist on the instance, but they aren't used.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1846241

</td><td>

The Hermes metrics dashboard displays data off by 1

</td><td>

 

</td><td>

1.  Open an instance with data in the hermes\_usage\_metrics table.
2.  Switch the preference timezone to GMT in preference settings.
3.  Compare the data points on the graph vs the table.

 Expected behavior: It shows the same date as the table.

 Actual behavior: The date is one day behind.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1847005

</td><td>

The 'Hermes Metric Aggregation' job is joining dates together due to a job skew

</td><td>

The job should be moved further into the day with the GMT timezone to avoid a skew. Also, add limits so that the aggregation is only picking updates of the previous day's start and end and not have it depend on when the job is run. There should be similar limits for clean-up jobs and monthly aggregation.

</td><td>

1.  Have an instance with Hermes installed.
2.  Create a topic and produce and consume it.
3.  Verify usage metrics are logged every 1 hr.
4.  The next day, verify that all hourly metrics are aggregated to the daily metrics of the previous day and that hourly metrics are clear.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1856021

</td><td>

Data in throughput shown on hermes\_usage\_metrics when producing data in inconsistent patterns

</td><td>

Inaccuracies in 'Total MB Value Per Hour' when data flows in an inconsistent pattern. When producing data at a relatively constant rate, hermes\_usage\_metrics values closely matched the actual value, but when producing data in large spikes, the values in hermes\_usage\_metrics are significantly above or below the actual value.

</td><td>

1.  Set up Kafka producer on a local machine using Kafka Java APIs.
2.  Produce a large batch of messages.
3.  Wait until the hourly aggregation job runs to populate hermes\_usage\_metrics.
4.  Check the corresponding value in 'Total MB Value Per Hour'.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1876312

</td><td>

There's a missing call to refresh clients when clusters are removed

</td><td>

When clusters are removed during a 'Retire' request, the deletion should also refresh the clients. A recently added function was missing that refresh call.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1862345

</td><td>

A component needs to be deregistered on disconnect when using now-trigger-library's deregisterComponent

</td><td>

Not deregistering a component results in detached DOM nodes/memory leaks, as the registry object still retains a reference to the element even should it be removed from the DOM.

</td><td>

1.  Navigate to a page in a workspace that has the element in question on it \(now-alert-list\).
2.  Use the console to check the componentRegistry that exists in window.uxfTriggerLibrary.
3.  Navigate away from the tab in question or perform any action that removes the element from the DOM.

 Expected behavior: As the element no longer exists in the DOM, its entry in the componentRegistry should no longer be there.

 Actual behavior: The entry for the element in the componentRegistry persists, as it was not deregistered on COMPONENT\_DISCONNECT.

</td></tr><tr><td>

Horizon Component Library

 PRB1867018

</td><td>

Update Now Assist Panel \(NAP\) customization in the 'Tools and Admin' theme

</td><td>

NAP choice picker background colors don't allow for good color contrast.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1881075

</td><td>

HDS net new components: **Animated carousel** and **Animated** button

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1831301

</td><td>

Renaming an attachment isn't working for an agent

</td><td>

 

</td><td>

1.  Provision an instance with sn\_hr\_agent\_ws 3.3.1/4.0.0-SNAPSHOT installed.
2.  Log in as an agent.
3.  Open an HR case in HR Agent Workspace.
4.  Attach a document in the attachments side panel.
5.  Try to rename it.

 Observe that the attachment isn't renamed.

</td></tr><tr><td>

HR Service Delivery

 PRB1831691

 [KB2043348](https://hi.service-now.com/kb_view.do?sysparm_article=KB2043348)

</td><td>

HTML dynamic parameters on HR templates don't work as expected

</td><td>

There's an issue in Xanadu and Yokohama where HTML dynamic parameters aren't replaced with their actual values when used in links. The issue arises in the HTML-sanitizer enabled HTML and translated HTML fields during template replacement with HTML data.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery

 PRB1858070

</td><td>

There's an email client template visibility issue in HR Agent Workspace

</td><td>

A global ACL isn't working. sys\_email\_client\_template extends sys\_metadata \(application file\) so if the sys\_email\_client\_template record is created in ER scope, it runs the ACL in ER scope. If there's no ER scope ACL, it can inherit the global ACL by ACL inheritance, otherwise, access could be blocked. If there's no ER scope ACL on sys\_email\_client\_template, it might need to be added.

</td><td>

 

</td></tr><tr><td>

Incident Communications Management

 PRB1849039

</td><td>

Update the email client template from the mail script

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Incident Communications Management

 PRB1849469

</td><td>

Filter Major Incident Management \(MIM\) email templates in MIM Comm based on a template condition in Classic

</td><td>

MIM templates follow a reference qualifier and don't respect conditions set within the templates.

</td><td>

1.  Open major incident in Service Operations Workspace.
2.  Select the 'Communicate' tab.
3.  Select the **Compose** button on a communication plan.

 Expected behavior: A user can all see all templates

 Actual behavior: Based on a condition within the templates, filtering should be applied. It currently follows the reference qualifier.

</td></tr><tr><td>

Incident Communications Management

 PRB1860756

</td><td>

Resolving variables isn't working in UI16

</td><td>

 

</td><td>

1.  Install com.snc.incident.mim and sn\_itsm\_gen\_ai plugins.
2.  Open any major incident communication plan from UI16.
3.  Select **Compose**.

 Expected behavior: The email should display as per the variables defined under the email client template.

 Actual behavior: No email is displayed in UI16.

</td></tr><tr><td>

Integration Hub

 PRB1852454

</td><td>

com.service\_now.mid. connections.jdbc. JDBCConnection splits a property on equal signs

</td><td>

The '==' value is removed when the code saves to the property, which caused a save to an incorrect value string.

</td><td>

1.  Set up a JDBC data source.
2.  Add the string 'dGVzdCBzdHJpbmchIQ==' as a property.

 Notice that when it's processed, the '==' are stripped.

</td></tr><tr><td>

Integration Hub

 PRB1878255

</td><td>

Suggested actions are erroring out on the Yokohama Now Assist table

</td><td>

This issue appears to have been caused by an underlying script, including call adding to the scope stack, which exposed a problem in how the flow engine cleans up the scope stack after a flow execution.

</td><td>

1.  Create a flow that adds to the scope stack but does not clean it up.
2.  Execute the flow in the background.

 Expected behavior: Flow executes without exception.

 Actual behavior: An error is thrown when the flow completes.

</td></tr><tr><td>

Integration Hub Remote Process Sync

 PRB1874002

</td><td>

Remote Process Sync \(RPS\) is triggered by changes from non-captured fields

</td><td>

RPS captures changes to a record when any changes are made to the fields selected by the user as part of the CDC Definition \(change data capture\). Even though changes are being made to fields that are not part of the CDC Definition, RPS still captures these changes.

</td><td>

1.  Set up RPS.
2.  Create a record that syncs.
3.  Modify a field on that record that isn't part of the CDC definition.

 Observe that this creates an update record on cdc\_queue\_ih, which should not be created.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1854256

</td><td>

Legacy SEK rekey fails due to the **password2** field size not being large enough

</td><td>

Instance rekey use sys\_dictionary.max\_length for field size detection, leading to rekey failure.

</td><td>

1.  Provision an instance.
2.  Populate the oauth\_credential. token\_received with a large value.
3.  Clone the instance from step 1.

 Expected behavior: Legacy SEK rekey completes successfully.

 Actual behavior: Legacy SEK complains that the field isn't large enough.

</td></tr><tr><td>

Lifecycle Events

 PRB1848546

</td><td>

In Yokohama, when the property use\_flow is false, creating a LE case using the 'LE Testing' functionality causes the case to be reopened

</td><td>

This doesn't happen on Yokohama when the 'sn\_hr\_le.use\_flow' property is set to true, and it doesn't happen on Xanadu.

</td><td>

1.  On a Yokohama instance, as a user with elevated privileges, activate the 'HR Xanadu Deprecated Workflow' \[com.sn\_hr\_xanadu\_deprecated\_wf\] plugin.
2.  Set the 'sn\_hr\_le.use\_flow' property to false.
3.  Open any existing LE in the LE Builder.
4.  Select the **Test** functionality.
5.  Create a case.

 Actual behavior: In the case worknotes, there's a message 'Case reopened by...'. Review the case history and the user can see that the **Active** field is updated twice; once from empty to false, and then from empty to true.

 Expected behavior: The **Active** field should only be updated once, from empty to true, and therefore the worknote 'Case reopened by...' shouldn't be logged.

</td></tr><tr><td>

List Administration

 PRB1862344

</td><td>

Component needs to be deregistered on disconnect using now-trigger-library's deregisterComponent

</td><td>

This deregistering issue occurs for the component now-record-list-header.

</td><td>

1.  Navigate to a page in a workspace that has the element now-record-list-header.
2.  Use the console to check the componentRegistry that exists in window.uxfTriggerLibrary.
3.  Find an entry for the element.
4.  Navigate away from the page.

 Expected behavior: As the element no longer exists in the DOM, its entry in the componentRegistry should no longer be there.

 Actual behavior: The entry for the element in the componentRegistry persists, as it was not deregistered on COMPONENT\_DISCONNECT.

</td></tr><tr><td>

List Filters

 PRB1751177

</td><td>

Inconsistency in 'Presentational 'list filters

</td><td>

There's an inconsistency between the data displayed and the filter applied for empty values. In one scenario, there's inconsistency when applying filters on the string column and the number column. If the filter text value is empty, the **Apply** button is turned off for the string column, but still enabled for the number column. Selecting **Apply** still retains the older filter. In another scenario, there's also an inconsistency between the data shown and the filter applied for empty values. Fields, which are empty in a table, are displayed as 0 in the presentational list based on the data type. When they are filtered, they should be considered empty or should be considered as 0 if it is shown as zero.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1840424

 [KB1772428](https://hi.service-now.com/kb_view.do?sysparm_article=KB1772428)

</td><td>

MID Server ECCSender thread gives an 'Invalid byte 2 of 4-byte UTF-8 sequence' error, blocking sending of valid ecc\_queue inputs to an instance

</td><td>

This is most likely to be seen in LDAP user imports, or Import Set JDBC Data Sources, where large data is involved. Large data is likely to include extended unicode characters such as emojis. For LDAP probes, emojis have been seen in OU/CN group names and user details data. For REST integrations synching incidents, emojis have been seen in comments of cases. They could potentially appear anywhere, for any feature's probe result data.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Platform

 PRB1886492

</td><td>

\(MAB\) card generation with Now Assist is failing on Yokohama

</td><td>

Now Assist based card generation is currently failing on the Y track due to a missing required column. The 'Creation Method' column, needed for handling records created by Now Assist is missing, resulting in insertion failures during the card generation process. Now Assist-based card generation doesn't work for users.

</td><td>

1.  Provision a Yokohama instance with Now Assist for Creator installed.
2.  Enable mobile card generation skill.
3.  Open the web to mobile flow for a record screen.
4.  Select the **Generate with Now Assist** option.

 Observe an error message: 'unable to insert record into table sys\_sg\_view\_config - setValue called for unknown field **creation\_method** in table 'sys\_sg\_view\_config''.

</td></tr><tr><td>

Mobile Virtual Agent

 PRB1881114

</td><td>

Mobile NASS GenAI visual uplift

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

 PRB1862612

</td><td>

The 'More information' link on MFA registration has the old documentation link structure

</td><td>

There's an incorrect documentation link structure present in the page 'multi\_factor\_auth\_setup\_page'.

</td><td>

1.  Log in to an instance that has MFA setup but the user isn't enrolled into MFA yet.
2.  After logging in during MFA enrollment, users would see the 'More information' hyperlink.
3.  Verify that on selecting the link, it redirects to documentation home page.

</td></tr><tr><td>

Multi-Instance Framework - Core

 PRB1849745

</td><td>

Turn off collect\_metadata and recurring\_diagnostics in sn\_mif record on hermes\_app\_services

</td><td>

The collect\_metadata and recurring\_diagnostics flags aren't set in the hermes\_app\_services record. By default in the table dictionary, those flags are true. That means that the instance automatically connects to the Hermes configured in that record, creates metadata and diagnostics topics, and starts sending traffic. For some Hermes running, this data isn't needed or used and observations show that this activity puts significant load on the cluster.

</td><td>

1.  Check the sn\_mif record in hermes\_app\_services.
2.  Note that both collect cluster metadata and recurring diagnostics are checked.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1862338

</td><td>

A component must be deregistered on disconnect using now-trigger-library's deregisterComponent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1883320

</td><td>

KB search sometimes isn't working after upgrading from Xanadu to Yokohama

</td><td>

 

</td><td>

1.  Set up a Xanadu instance and ensure that the KB search is working.
2.  Upgrade to Yokohama.
3.  Select **NAP**.
4.  Enter: 'what is spam'.

 Expected behavior: The KB should display a result.

 Actual behavior: A 'No answer found' message is displayed.

</td></tr><tr><td>

Now Assist Panel

 PRB1885517

</td><td>

A user isn't able to add an attachment in playground and Now Assist Panel \(NAP\)

</td><td>

The icon to upload is missing.

</td><td>

1.  Create any agent with the catalog tool.
2.  Select the option to add an attachment after providing required details.

 Observe that the user is asked to add an attachment, but there's no icon to upload.

</td></tr><tr><td>

Performance Analytics

 PRB1857024

</td><td>

On some nodes, fields become read-only on after an upgrade

</td><td>

This issue is intermittent and depends on the load order. It can deny access with an error message.

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

 PRB1858849

</td><td>

An **empty row\_count** field in the ml\_solution table leads to an error message being logged while parsing an integer from empty string from the ml\_solution row\_count attribute

</td><td>

When the **row\_count** field is empty while training a solution, the following error message is logged: 'Exception caught while building data Description list: For input string: "": no thrown error'. This occurs only for Java-based solutions.

</td><td>

 

</td></tr><tr><td>

Procurement

 PRB1859220

</td><td>

Update 'Procurement Process Flow - Auto allocation enabled' workflow to skip auto allocation when Now Assist for Software Asset Management \(SAM\) is active

</td><td>

Agentic solution for true-up in Yokohama.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1850637

</td><td>

Duplicate resource\_aggregate\_weekly and resource\_aggregate\_monthly records are created intermittently

</td><td>

Code in the UpdateActualsFromTimeCard function of the ResourceActuals SI raises an event to update aggregates for each day when a time card is approved or recalled, causing duplicate resource\_aggregate\_weekly and resource\_aggregate\_monthly records to be created intermittently.

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB1853349

</td><td>

Visualizations in non-global domains aren't displayed in the list of visualizations

</td><td>

When trying to add some dashboard to a library, it's not saved in any sub domains. It's getting saved only in the global domain. In the sub domains, when they try to save the dashboard, it says it's saved but it's not.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1860079

</td><td>

Performance impact due to the 'Optimization' business rule

</td><td>

A 'Optimization Metadata processor' business rule is made in sys\_attachment async.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1875270

</td><td>

Prevent the fallback of retrieving the schedule from the sys\_user record when there's no schedule in the 'Agent schedule' table

</td><td>

Remove the 'Agent schedule' but add a schedule to the sys\_user record. The agent shouldn't be returned in the getQualifierData response. Add the 'Agent schedule' only, it should be returned in the getQualifierData response.

</td><td>

1.  Enable a territory model.
2.  For the qualifying agent, verify that no schedule is present in cmn\_schedule.
3.  Add a schedule at the agent level in the sys\_user record.
4.  Create SO batch with the 'Territory' qualifier.
5.  Perform Graph QL for agents.

 Expected behavior: No schedule should be returned.

 Actual behavior: A schedule from the sys\_user record is returned.

</td></tr><tr><td>

Security Incident Response integration with Splunk Enterprise Event Ingestion

 PRB1865568

</td><td>

CMDB\_CI mapping fails on the **Configuration Item** field

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1848232

</td><td>

TD instance gets hung up and unresponsive due to recursive calls while capturing Generic Collection Framework \(GCF\) metics

</td><td>

While publishing the GCF metrics for scripts, MInMaxPriorityQueue is used for collecting 20 longest executions. It attempts to access indices more than 20, causing ArrayIndexOutofBound exceptions.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1864630

</td><td>

A fetch process hangs in an infinite loop if the header is returned as a list

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1835397

</td><td>

Users are unable to clear a value on a date type question from a client script/UI Policy

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Level Management

 PRB1843470

 [KB1777517](https://hi.service-now.com/kb_view.do?sysparm_article=KB1777517)

</td><td>

SLA engine reset condition may fail in certain circumstances

</td><td>

SLA Engine reset condition fails if the advanced conditions changes, changesFrom or changesTo are used in conjunction with the table in com.snc.sla.get\_ task\_from\_db and the walker is CHECKPOINT.

</td><td>

1.  Create an SLA Definition on the table sc\_req\_item:
    1.  start condition active=true
    2.  stop condition active=false
    3.  reset condition due\_date changes \(advanced condition\)
2.  Check that the property com.snc.sla.get\_task\_from\_db contains sc\_req\_item.
3.  Check that property com.snc.walker.default=CHECKPOINT.
4.  Update any value on an existing sc\_req\_item or create one and verify task\_sla is created for SLA Definition created in \#1.
5.  Update the **due\_date** field to anything if it is empty or change it to any value if it has a value.

 Expected behavior: task\_sla is canceled and new task\_sla is created.

 Actual behavior: task\_sla isn't canceled. The error log contains 'CheckpointHistoryWalker does not support walk to update: \#'.

</td></tr><tr><td>

Service Level Management

 PRB1849627

</td><td>

Improve SLA Calculator's handling of very large sets of Task SLA records during trigger processing

</td><td>

Under certain circumstances, bulk SLA calculations can cause node memory issues if the set of Task SLAs being calculated is very large.

</td><td>

1.  Open the script include SLACalculatorNG.
2.  Look at the function SLACalculatorNG. calculateSLArange.

 Note that it first processes the list of Task SLA and adds them to an array. This is consumes memory unnecessarily.

</td></tr><tr><td>

ServiceNow IDE \(Family Release\)

 PRB1878166

</td><td>

Integrated development environment \(IDE\) source files should not be deleted using a business rule on sys\_app table

</td><td>

This business rule is triggered on every delete action for a sys\_app. All associated IDE source files could potentially be deleted unintentionally from the instance, which is irreversible.

</td><td>

1.  Create a ServiceNow instance.
2.  Install ServiceNow IDE 2.0.4.
3.  Bump IDE to 2.1.0.
4.  Create an app in Service Now IDE.
5.  Build and deploy the newly created app.
6.  Observe all the source files being shown in IDE.
7.  Navigate to the sys\_app record.
8.  Delete the sys\_app record.

 Expected: ServiceNow IDE should not show any source files when app is deleted.

 Actual: A purge occurs due to a business rule.

</td></tr><tr><td>

Service Portal

 PRB1839297

 [KB1925168](https://hi.service-now.com/kb_view.do?sysparm_article=KB1925168)

</td><td>

SPEntry page error 'Execute operation on script include 'SPEntryPage'' from scope occurs

</td><td>

Switching the scope and refreshing the page gives the error, 'Execute operation on script include 'SPEntryPage' from scope 'Knowledge Management - Service Portal' was denied'.

</td><td>

1.  Log in to a Xanadu instance.
2.  Create the glide.entry.first.page.script system property.
3.  Give it the value: new SPEntryPage\(\).getFirstPageURL\(\).
4.  Make 'Knowledge Management - Service Portal' as the current scope.
5.  Refresh the browser page.
6.  Notice the error, 'Execute operation on script include 'SPEntryPage' from scope 'Knowledge Management - Service Portal' was denied. The application 'Knowledge Management - Service Portal' must declare a cross scope access privilege. Please contact the application author to update their privilege requests.'
7.  Repeat step 2 and step 3 with the scopes 'CI Landing Experience' and 'Conversational Interfaces - Diagnostics'.

 Notice that the same error message occurs.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1849937

</td><td>

When sn\_hr\_core.impersonateCheck is set to 'true', users are unable to add users to the sidebar

</td><td>

When sn\_hr\_core.impersonateCheck is set to 'true', users can't add users to the sidebar discussion for sn\_hr\_core\_case\_payroll records. There's instead an error message: 'Participants can't join the discussion because they don't have access to this record.'

</td><td>

1.  Install the sn\_hr\_core plugin with demo data.
2.  Set the system property sn\_hr\_core.impersonateCheck to true.
3.  Navigate to any sn\_hr\_core\_case\_total\_rewards record.
4.  Select the **Discuss** UI action.
5.  Select **Add Participants**.
6.  Select any user \(such as Abel Tuter\) with access to the parent record.

 Notice the error message appears.

</td></tr><tr><td>

Software Asset Management

 PRB1878273

</td><td>

Databroker changes to call prompt

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Normalization

 PRB1840383

</td><td>

For a software product type other than the licensable normalization engine, it keeps the version empty and marks it as normalized using only the product map

</td><td>

For a software product type other than the licensable normalization engine, it doesn't pick a pattern rule that has a potential to stamp the version, and rather keeps the version empty and marks it as normalized using only the product map. When a discovery model undergoes normalization, in cases for software product types other than licensable, the normalization engine doesn't select a pattern rule that could assign a version. Instead, it leaves the **version** field empty and designates it as normalized using only the product map.

</td><td>

1.  Have a DM for a non licensable product. It should be product normalized.
2.  Have a pattern rule for the particular product.
3.  Run rormalization.

 Expected behavior: The product becomes pattern normalized, and the version is stamped in.

 Actual behavior: The product remains product normalized with no version stamped.

</td></tr><tr><td>

Syntax Editor

 PRB1533082

</td><td>

The fonts defined on the system property 'glide.ui.html.editor .v4.font.collection' aren't displayed on the font list of the HTML editor on Agent Workspace

</td><td>

The list should show only the fonts defined in the value of system property 'glide.ui.html.editor .v4.font.collection, but it shows all the fonts mentioned on the system property 'Description'. On the native UI HTML editor, it's working as expected.

</td><td>

 

</td></tr><tr><td>

Table Administration and Data Management

 PRB1852726

 [KB2068808](https://hi.service-now.com/kb_view.do?sysparm_article=KB2068808)

</td><td>

Users get an error: 'Syntax Error or Access Rule Violation detected by database \(\(conn=316832\) Unknown column 'ba.a\_ref\_10' in 'on clause'\)'

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Third-party Software

 PRB1793365

</td><td>

Commons-beanutils hits BEANUTILS-509, causing severe default thread contention, leading to 429s

</td><td>

In a few cases, this caused a node to completely hang indefinitely because all the threads were attempting to enter a synchronized block of a WeakHashMap that was being hogged by a thread stuck in an infinite loop.

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1866307

</td><td>

Sanitizing URLs in GlideElementURL

</td><td>

For performance, the sanitized URL can be cached rather than computing the same value repeatedly.

</td><td>

 

</td></tr><tr><td>

UI Builder \(Family Channel\)

 PRB1874490

</td><td>

PROXY\_DATA\_UPDATED is undefined

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1843602

</td><td>

There's an issue with the date picker position

</td><td>

The date picker position doesn't change when scrolling through the page.

</td><td>

1.  Open a form with a **Date** field.
2.  Select the date picker.
3.  Scroll the page.

 Notice that the date picker remains in the same position on the screen even when scrolling.

</td></tr><tr><td>

UI Form Administration

 PRB1847059

</td><td>

Formatting on the special handling notes header is aligned to the left in Xanadu

</td><td>

Special handling notes aren't aligned properly and are formatted completely to the left.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1859837

</td><td>

UX view rule configuration is not applied in the Workspace when a record is opened from a reference field

</td><td>

UX view rule configurations are not applied when a record is opened in a Workspace from a reference field on a form, but when opening the same record from a related list in a Workspace, the UX view rule configuration is applied.

</td><td>

1.  Open a cmdb\_ci\_computer table.
2.  Create a custom view.
3.  Create a workspace view rule on the sysrule\_view\_workspace table with the values:
    -   Table: cmdb\_ci\_computer
    -   View: Use the Custom View created
    -   Experience Restricted: Uncheck
    -   Workspace: Empty
    -   Execution Order: 1
4.  Create a UX view rule configuration on the sys\_ux\_view\_rules\_configuration table with the value: Active: True
5.  Navigate to **Workspace View Rules** &gt; **Related list**.
6.  Add the Workspace view rule created.
7.  Open the Service Operations Workspace.
8.  Create new incident where the **Configuration Item** field references a cmdb\_ci\_computer record.
9.  Save the new incident.
10. Navigate to **Incident** &gt; **Details** &gt; **Open Record** in the **Configuration Item** field.
11. Select **Open Record** on the modal that appears.

 Observe that the Custom View created in is not applied.

</td></tr><tr><td>

UI Form Administration

 PRB1868782

</td><td>

While composing an email in Vendor Operations, the cursor occasionally jumps, making it difficult to continue typing

</td><td>

When the user types rapidly, the position event is triggered multiple times, resulting in the cursor unexpectedly jumping to the end.

</td><td>

1.  On a base instance, enable email reply recommendations on any table.
2.  Add a line to the end of the email's last line.
3.  Start typing in the first line quickly.

 Observe that the cursor jumps to the end of the file.

</td></tr><tr><td>

UXF Components

 PRB1831642

</td><td>

Contents of UI Builder \(UIB\) components can't inherit the height of the container component it is placed into

</td><td>

Inside of the macroponent element used to render UIB components, two divs wrap internal contents - a plain div, and a div with display: contents; set on it. As a result child elements of the UIB component are unable to inherit the height of the container it is placed into.

</td><td>

1.  Create a component in UI Builder.
2.  Set the height and min-height to 100% on the component element.
3.  Add the resizable panes component inside.
4.  Populate it with any content in left and right panes.
5.  Set the height and min-height of a resizable component to 100%.
6.  Save the UIB component.
7.  In an experience built from Workspace App Shell, create a page.
8.  Add the previously created component to the page.
9.  Set the height and min-height of the body to 100%.
10. Set the height and min-height of component to 100%.

 Expected behavior: It is possible to set up a component built in UIB to take the full height of the container or page it is placed into.

 Actual behavior: The component doesn't stretch to the full height of the page.

</td></tr><tr><td>

UX Framework

 PRB1853498

</td><td>

Backslashes in UX Library's asset's source map URL causes an empty screen

</td><td>

It is possible to create custom components that have a source map URL path with backslashes. In the bundling logic, it looks for each asset source map URL line and remove it. That logic isn't full matching the strings that include backslashes and it leaves a partial string in the JavaScript content. This partial string is what's causing the empty screen, since the JavaScript content is malformed.

</td><td>

Modify the source map URL path with blackslashes instead of forward slashes in any UX library asset that is included in a core bundle.

 Expected behavior: The instance should display pages.

 Actual behavior: Empty screens are displayed.

</td></tr><tr><td>

UX Framework

 PRB1860878

</td><td>

sn-canvas-badge-connected fetches the count and then subscribes to the channel provided as part of a UX page property

</td><td>

Updates in between aren't captured by the badge.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1869757

</td><td>

There's a performance degradation when loading the home page on Xanadu

</td><td>

When the system property glide.ux.user\_ criteria\_enabled=true, there's a performance degradation between Washington DC and Xanadu when loading the home page.

</td><td>

1.  On a Washington DC instance, set glide.ux.user\_ criteria\_enabled to true.
2.  Navigate to the instance home page.
3.  Measure the page load times.

Notice that the average page load time is less than five seconds.

4.  On an Xanadu instance, set glide.ux.user\_ criteria\_enabled to true.
5.  Navigate to the instance home page.
6.  Measure the page load times.

Notice that the average page load time is between eight and ten seconds.


 Observe the performance degradation between the two versions when the system property glide.ux.user\_ criteria\_enabled is set to true.

</td></tr><tr><td>

Virtual Agent Actionable Notifications

 PRB1870525

</td><td>

Actions are not shown to the user if notification actions are passed in event parameters

</td><td>

Actions should be shown to the user, with the actions mapped to the content statically followed by the actions from the event parameters.

</td><td>

1.  Set up batch notification with the value of system property com.glide.cs. notification\_batch \_user\_size less than the number of recipients on notification.
2.  Setup an actionable notification with an event trigger.
3.  Add some actions, which may or may not be linked to the content.
4.  Select the checkbox to pass in actions as event parameters in **Link actions to content record**.
5.  Trigger the notification by passing in some actions as event parameters \(gs.eventQueue\(, , \)\) assuming the event parameters contain action sys IDs.

 Expected behavior: Actions should be shown, with the order being first the ones mapped to the content statically, followed by actions specified in the event parameters.

 Actual behavior: Actions are not shown along with the notification.

</td></tr><tr><td>

Virtual Agent Actionable Notifications

 PRB1881238

</td><td>

Non-actionable notifications aren't triggered

</td><td>

It isn't working with new or existing users. There's errors in the notification logs.

</td><td>

1.  Have 1 non-actionable notification setup or 1 non-actionable and 1 actionable.
2.  Create an incident for a user.
3.  Open Virtual Agent.

 Observe there's no notification.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1880139

</td><td>

L10n warning in Now Assist in Yokohama

</td><td>

Localization warning in Now Assist in Yokohama.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1847804

</td><td>

The script tool in skill-kit results is null and doesn't evaluate the script

</td><td>

A skill that calls a script tool to filter RAG results based on custom filtering does not process the script, causing the script to return null.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1853608

</td><td>

Now Assist Panel \(NAP\) isn't loading after 10+ cases notification have been triggered

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1854580

</td><td>

In the AutoEval Proxy2 skill, the grounded prompt is inserted incorrectly

</td><td>

The context is put into the hypothesis although the metric is mapped correctly.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1854684

</td><td>

Metric results override batch results when the batch run's run type is 'Auto Prompt Tuning'

</td><td>

Metric results aren't created in sys\_one\_extend\_eval\_metric\_result and override the batch results \(sys\_one\_extend\_batch\_result\).

</td><td>

1.  Create a skill.
2.  Trigger a prompt optimization run.

 Notice that the optimized evaluation run triggered by prompt assist \(of runType: Auto Prompt Tuning\) results are incorrect. Metric results aren't created in sys\_one\_extend\_ eval\_metric\_result and override the batch results.

</td></tr><tr><td>

Virtual Agent

 PRB1859774

</td><td>

Create sys\_auto\_flush records to auto delete one\_api\_variable\_store records

</td><td>

one\_api\_variable\_store is a run time record and that does not need to continue indefinitely. one\_api\_variable\_store records with sys\_created\_on with a specific timestamp need to be auto deleted by the instance.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1862370

</td><td>

Skill executions are stuck when Now Assist guardian settings \(prompt injection, offensiveness\) are enabled

</td><td>

Skill test runs aren't working from the skill kit, whereas executions outside of the skill kit \(for example: OneExtend.execute\(\) in async mode\) are working fine for the same settings. This is due an unsupported operation exception coming from EvaluationServiceImpl.java.

</td><td>

1.  Create a skill from the Now Assist Skill Kit.
2.  Enable prompt injection from the Now Assist Guardian settings \(use option as 'Block'\).
3.  Select **Run Test** on that skill.

 Expected behavior: **Run Test** should work irrespective of the guardian setting because users can execute the same One Extend capability outside of the skill kit.

 Actual behavior: **Run Test** is stuck due to an exception \(Error Execution of evaluation request failed for batch result: fbb3afc4c348 e2149e83d62 f0501312b due to error: null\).

</td></tr><tr><td>

Virtual Agent

 PRB1863302

</td><td>

Eval metric result records are not created when metric execution is skipped because of an applicability script condition

</td><td>

Eval metric result record should be created with status of 'Skipped'.

</td><td>

1.  Add a condition to a skill in an applicability script for any metric in an extended resource mapping record.
2.  Trigger an evaluation run by selecting the above changed metric.

 In the 'Eval metric result' table, notice that the records for the above metric is not created.

</td></tr><tr><td>

Virtual Agent

 PRB1864394

</td><td>

When a user selects the **None of these** option on the 'Submit Request \(Template\)' topic in Virtual Agent, it generates empty catalog item page

</td><td>

When the user selects the option **None of these** and selects the link, they are directed to an empty catalog item page. The user should not be asked to submit a request after selecting the option **None of these**.

</td><td>

1.  Hop into a base Xanadu instance.
2.  Ensure the plugin 'Customer Service Virtual Agent Conversations' is installed on the instance.
3.  Ensure the topic 'Submit Request \(Template\)' is published and visible in Virtual Agent.
4.  Navigate to the Customer Service Management \(CSM\) portal.
5.  Select **Show me everything** &gt; **Submit Request \(Template\)**.
6.  Enter **Create case**.
7.  Select **None of these**.
8.  Select **Yes** for the query 'Do you want to proceed with?'.
9.  Select the link.

 Expected behavior: The user selects the link and they are either directed to the correct catalog item page, a case is created, or for 'None of these' options they are not asked to submit a request.

 Actual behavior: The user is able to submit the 'None of these' option, and it gives an empty link for the catalog item.

</td></tr><tr><td>

Virtual Agent

 PRB1865096

</td><td>

There's a NotFoundExecption when a sys\_cs\_session record isn't available for a user

</td><td>

In the error log: 'Unable to find session in db. Script execution error: Script Identifier: null.null.script, Error Description: com.glide.rest.util. NotFoundException, Script ES Level: 0. Couldn't decipher the stack trace resulting from the following JavaScriptException: com.glide.rest.util. NotFoundException: org.mozilla.javascript. JavaScriptException: com.glide.rest.util .NotFoundException: org.mozilla.javascript. Context.makeJavaScript Exception\(Context.java:2626\)...'

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1866728

</td><td>

The user is not able to asynchronously process a dataset and trigger an eval run

</td><td>

A sys trigger can't process a dataset and an eval run at the same time.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1867769

</td><td>

Users can't activate a trigger for a Virtual Agent channel and profile

</td><td>

Instead of calling getChannelByName and hardcoding the channel, it should be grabbed by the channel ID. There's also a missing context profile.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1868677

</td><td>

Added a fix script for auto\_prompt\_tuning internal in sys\_one\_extend\_batch\_run

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1869860

</td><td>

System property 'proxy=false' with a carousel output does not return a Genius Response

</td><td>

Genius Response is stuck on 'Looking into your request' after updating the 'web client' output type to '= carousel' and updating the value of sn\_vad\_genai. com.glide.cs. one\_extend. auto\_proxy\_enabled to 'false'.

</td><td>

1.  Navigate to now\_assist\_va\_ search\_results\_output\_type table.
2.  Update the 'web client' output type to '= carousel'.
3.  Navigate to sys\_properties table.
4.  Update the value of sn\_vad\_genai. com.glide.cs.one\_ extend.auto\_ proxy\_enabled to 'false'.
5.  Start a new conversation with Now Assist Virtual Agent on an /ESC portal.
6.  Enter 'What is a cookie?'.

 Expected behavior: The response appears as a carousel.

 Actual behavior: The response is stuck on 'Looking into your request'.

</td></tr><tr><td>

Virtual Agent

 PRB1871270

</td><td>

Additional read of conversation in worker.lockAndProcess should be moved

</td><td>

A new call to retrieve the conversation and read values form the context before every lock and process operation in Worker for the AI Agents. This adds unnecessary overhead to any transaction that is not LLM or Agent AI related.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1872922

</td><td>

Domain separation issue when running AI Agents

</td><td>

When retrieving a record from a separate domain using an AI agent, no is data returned.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1872958

</td><td>

Virtual Agent search result showing issues after upgrade

</td><td>

Virtual Agent results returned were misaligned after upgrading to Yokohama.

</td><td>

1.  Log in to an Employee Service Center \(ESC\) portal.
2.  Impersonate a user.
3.  Initiate a Virtual Agent chat.
4.  Enter **bereavement policy**.

 Notice that the search results are shown in misaligned order.

</td></tr><tr><td>

Virtual Agent

 PRB1874300

</td><td>

A grammatically incorrect message is thrown by the API

</td><td>

Part of an error message from Now Assist skill capability is grammatically incorrect: 'Failed to execute the feature due to an error while executing it's depends on feature'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1876378

</td><td>

A KB article is not returned in NAVA during a Yokohama Now Assist upgrade

</td><td>

When a plugin stage user types 'what is spam' during an upgrade, the conversation gets stuck.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1877176

</td><td>

Enabling KG isn't making unified slot fill calls

</td><td>

This causes slot filling to not work.

</td><td>

1.  Ensure KG is enabled at the instance level as well as for a conversation catalog.
2.  Impersonate a user.
3.  Request the 'Employee Details' catalog item.

 Expected behavior: Slot fill should happen for most of the questions, and the unified slot fill call happens.

 Actual behavior: Slot fill doesn't happen for questions and the unified slot fill call didn't happen.

</td></tr><tr><td>

Virtual Agent

 PRB1877432

</td><td>

Dynamic loading message control \(on Virtual Agent chat client\) should contain non-agentic 'processing messages'

</td><td>

Non-agentic messages should appear in the chat client response.

</td><td>

1.  Set up Agentic.
2.  Perform a search, such as 'What is spam?'.

 Expected behavior: In the VA chat client, the 'View AI Agent Processing Steps' collapsible control should contain all update messages.

 Actual behavior: Only the first two messages \('Figuring out next steps', 'Executing agent Search QnA Agent'\) that were initiated from the Agentic frameworks are included inside the 'View AI Agent Processing Steps' collapsible control on the VA chat client. The next two status update messages \('Finding the needed info', 'Reviewing the details'\) appear as standalone messages.

</td></tr><tr><td>

Virtual Agent

 PRB1878226

</td><td>

When running AI Agent Studio on a non-English language instance, the stacked message renders until the conversation moves into the error topic

</td><td>

During the updateDynamicProgressMessage scriptable path, one of the progressMessages in the DynamicLoaderRichControl has a message of 'null'. This causes an exception.

</td><td>

1.  Provision and instance with a language plugin installed and enable DT for that language.
2.  Set up NowAssist and AI Agents.
3.  Ensure that the DT optimizer is on and the sys\_cs\_dynamic\_translation\_text table is cleared or that the optimizer is off.
4.  Change the user's language to a language other than English.
5.  Start a conversation in Agent Studio.

 Expected behavior: The stacked messages should all be translated/localized.

 Actual behavior: Conversation ends abruptly.

</td></tr><tr><td>

Virtual Agent

 PRB1880022

</td><td>

The skill applicability URL condition isn't working

</td><td>

The skill applicability is broken and doesn't apply correctly. The root cause is confirmed to be a URL query failing.

</td><td>

1.  Navigate to CMDB Workspace.
2.  Open the Now Assist Panel \(NAP\).

 Expected behavior: 'Diagnose a service graph connector' should be a recommended topic.

 Actual behavior: The **Diagnose a service graph connector** topic button doesn't appear.

</td></tr><tr><td>

Virtual Agent

 PRB1880277

</td><td>

Dynamic Translation \(DT\) in the full page experience does not translate all elements

</td><td>

Some elements are not translated in the user's language in the full page experience.

</td><td>

1.  Enable DT.
2.  Index sources for KB, Catalog, and skills.
3.  Impersonate a user.
4.  Change the language to Spanish.
5.  Search for KB, Catalog, or topics.
6.  Open the left panel.
7.  Check for the translation of elements.

 Expected behavior: All elements in full page should be translated to the user's language.

 Actual behavior: Some objects are not translated to the user's language.

</td></tr><tr><td>

Virtual Agent

 PRB1880594

</td><td>

The 'sys\_gen\_ai\_log\_metadata\_list' caller column is empty

</td><td>

The 'sys\_gen\_ai\_log\_metadata\_list' caller column is empty even if the caller column in 'sys\_generative\_ai\_log\_list' contains data.

</td><td>

1.  Run a dynamic capability.
2.  See if the caller is present on sys\_generative\_ai\_log but not on sys\_gen\_ai\_log\_metadata.

</td></tr><tr><td>

Virtual Agent

 PRB1881057

</td><td>

Java Proxy should use the LLM language as the source instead of the system language

</td><td>

Synthesized results should appear in the non-English language set by glide.sys.language when executing a search in Now Assist.

</td><td>

1.  Setup Now Assist Setup DT for VA Install language plugins.
2.  Set the LLM prop \(com.glide.cs.llm.default.Language\) to English.
3.  Set the NLU prop \(glide.sys.language\) to a non-English language as a user with their language preference set to same value as 'glide.sys.language'.
4.  Execute a search in Now Assist.

 Expected behavior: Synthesized results should appear in the user's language.

 Actual behavior: Synthesized results appear in English.

</td></tr><tr><td>

Virtual Agent

 PRB1881106

</td><td>

Global changes for auto chat in Glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881107

</td><td>

Enhance the async mode error response format in one API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881108

</td><td>

A capability should have a new type called 'Predictive Intelligence'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881109

</td><td>

Deep clone of some skills and multiple default prompt bug fixes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881110

</td><td>

Truncation support for tool outputs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881111

</td><td>

Support 'Cancel' for AutoEval Run

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881112

</td><td>

Enhance APIs to support for creating a dataset and processing a dataset to avoid creating dataset skill mapping

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881113

</td><td>

Auto-prompt tuning check due to a backend name change

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881115

</td><td>

Extend Metric Result's schema and API to persist results per group

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881116

</td><td>

Clone Agentic Eval Run

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881118

</td><td>

Support Agentic AI Eval execution without a proxy skill

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881121

</td><td>

API support for new schema changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881123

</td><td>

Adding to an update set should generate child update sets with a unique name

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881125

</td><td>

As an AI Practitioner, users should be able to select a solution, and be able to navigate to additional configurations sections

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881126

</td><td>

Create a new API for getTestDatasets for agentic-type datasets

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1882397

</td><td>

ReAct Search Agent stuck in a loop

</td><td>

This issue occurs with a search query and a meeting agent. Synthesized answers are returned in the logs, but are not displayed.

</td><td>

1.  Navigate to /ESC.
2.  Open the NASS query, 'Let's get info on password reset then set up meeting'.

 Notice that the search agent is stuck in a loop with the message, 'Sorry no agents are available', and a synthesized answer is returned in logs but is not displayed.

</td></tr><tr><td>

Virtual Agent

 PRB1882692

</td><td>

Assistant-based agents functionality is missing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1883231

</td><td>

Sync calls are happening every 5 seconds when creating a new chat

</td><td>

 

</td><td>

1.  Navigate to dynamic window/FPE.
2.  Open the browser console.
3.  Create a conversation.

 Expected behavior: '/sync' calls should be happening as often as the 'syncIntervalTime' is set. Ensure that 'syncIntervalTime' isn't displaying in the /sync calls response when initiating a new conversation.

 Actual behavior: that '/sync' calls are happening every 5 seconds.

</td></tr><tr><td>

Virtual Agent

 PRB1883338

</td><td>

Skill discovery for a non-agent topic \(caller's assets\) redirects to a AI Agent workflow in Now Assist Panel \(NAP\)

</td><td>

In NAP, skill discovery sometimes redirects to the default Virtual Agent workflow \(AI Agent\) instead of starting the caller assets skill.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1883376

</td><td>

Responses aren't coming when a user summarizes a record after providing an incident ID

</td><td>

An error happens in MessageBatchingSession.escapeList\(\), which escapes a list of strings before calling DT. The problem is the list is immutable, so it fails to update the list with the escaped values.

</td><td>

1.  Log in to the instance as Beth Anglin with the Spanish language
2.  Select the 'NAP' icon.
3.  Search for 'Resumir un registro'.
4.  Once the response comes back, provide the incident ID as INC0009009.

 Expected behavior: The incident summarization should come in Spanish.

 Actual behavior: There's no response in the chat, and an error in the log.

</td></tr><tr><td>

Virtual Agent

 PRB1883466

</td><td>

Parity with FD in NowLLM invocation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1883829

</td><td>

Verify 'Summarize a Record from Record View'

</td><td>

 

</td><td>

1.  Navigate to the 'Incident' table.
2.  Select any incident number.
3.  Navigate to the Now Assist Panel \(NAP\) panel by selecting the NAP icon in the top right corner of the unified navigation.
4.  Select the **Summarize a record skill** pill.

 Expected behavior: The summary should be displayed.

 Actual behavior: A 'What is the record number? 'question is displayed.

</td></tr><tr><td>

Virtual Agent

 PRB1884082

</td><td>

Input text messages from agents are displaying with a lower sequence number than they should

</td><td>

This affects the conversation history.

</td><td>

1.  Navigate to an instance with the 'Ticket status' agent.
2.  Type 'What is the status of my tickets?'.

 Expected behavior: The messages when sorted by sequence should reflect the actual flow of the conversation.

 Actual behavior: In the sys\_cs\_message table, if users sort the messages by the sequence number, they appear to be out of order.

</td></tr><tr><td>

Virtual Agent

 PRB1884615

</td><td>

Citations in NAVA and Now Assist Panel \(NAP\) for non-English conversation languages are displaying incorrectly

</td><td>

 

</td><td>

1.  Navigate to the SP portal.
2.  In the NAVA chatbot, enter 'Quels sont quelques monuments célèbres à Paris ?'.

 Observe that in the returned Genius Results, the citation at the end is displayed as just \[1\]. In the English session, users can type 'what is spam' to see expected response format.

</td></tr><tr><td>

Virtual Agent

 PRB1884694

</td><td>

Proactive triggers with topics don't launch in dynamic window \(DW\)

</td><td>

 

</td><td>

1.  Set up proactive triggers for the portals with topics that can be launched.
2.  Navigate to the portal on DW and wait for the proactive trigger.
3.  Launch the topic in proactive trigger.

 Expected behavior: The topic should launch in DW.

 Actual behavior: The topic doesn't launch and the user lands on a new chat in DW.

</td></tr><tr><td>

Virtual Agent

 PRB1887021

</td><td>

A conversation call is taking too long after an update

</td><td>

There's no 'IN' clause on a query on the sys\_cs\_message table.

</td><td>

1.  Load Now Assist Panel \(NAP\).
2.  Check the conversation call form network.

 Observe that the times are more than 1 second.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1820930

</td><td>

The **Show More** button isn't working consistently in iOS Safari

</td><td>

The **Show More** button in a NAVA synthesized response is shown despite not having more responses to display.

</td><td>

1.  Have NAVA enabled on an instance.
2.  Create a user to log in using a mobile browser.
3.  Enter 'What should I know about direct deposit?'.
4.  Select the **Show More** button on the response.

 Expected behavior: More of the SR should show without any issues.

 Actual behavior: SR is rendered incorrectly with the **Show Less** button showing behind the rest of the message.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1869818

</td><td>

Toggling between the search and Now Assist isn't retaining the search term

</td><td>

 

</td><td>

1.  Navigate to Service Portal.
2.  Enter 'what is spam' in the portal search test box.
3.  Select the **New chat** button in the 'NASS' page.
4.  Select the search toggle.

 Expected behavior: An empty search should be displayed.

 Actual behavior: The search term from step 2 is retained.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1871159

</td><td>

The 'DW' icon is visible and popups for citations aren't clickable

</td><td>

 

</td><td>

1.  Navigate to dynamic window \(DW\)/Full Page \(FP\).
2.  Open in floating mode.

 Expected behavior: The 'DW' icon shouldn't be available.

 Actual behavior: The 'DW' icon is available and clickable.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1871232

</td><td>

Chats aren't in sync when navigating multiple portal pages

</td><td>

 

</td><td>

1.  Enable full page \(FP\) for Service Portal.
2.  Navigate to dynamic window \(DW\).
3.  Run a few conversations such that there are a few chats in the 'Active' section.
4.  Perform another search in the search bar on FP.
5.  Switch to another chat on FP.
6.  Navigate to Knowledge, Catalogs, Requests, System Status, Tours and other pages on the portal.

 Expected behavior: The chat should remain in sync when the user opens DW in these pages.

 Actual behavior: The chat isn't in sync when the user goes through multiple pages and there's content from another chat on DW.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1877908

</td><td>

A document upload fails the first time

</td><td>

 

</td><td>

Try to upload an attachment to Virtual Agent.

 Notice that it gets stuck in loading. If the user refreshes and uploads again, it works.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1878155

</td><td>

Icons for different sources aren't visible in the 'Sources' section

</td><td>

 

</td><td>

1.  Navigate to NAVA.
2.  Search for a person and KB/catalog 'who is abel tuter and what is spam' / 'who is abel tuter and how can i order a laptop'.
3.  Expand the 'Sources' section to view citations.

 Expected behavior: Each source should have a corresponding icon beside the citation number.

 Actual behavior: No icons are visible except for the KB and the 'People' card. The current icon for the 'People' card is incorrect. It should be a generic icon instead of a user profile picture.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1879738

</td><td>

Chats are not in sync when navigating multiple portal pages

</td><td>

After enabling Full Page \(FP\), switching between multiple chats and navigating away to different Portal pages in the Dispatcher Workspace, the chats are not in sync when the user returns to them.

</td><td>

1.  Enable Full Page \(FP\) for Service Portal.
2.  Navigate to the Dispatcher Workspace.
3.  Run a few conversations so that there are a few chats in the Active section.
4.  Perform another search in the search bar on FP.
5.  Switch to another chat on FP.
6.  Navigate to other pages on Portal such as Knowledge, Catalogs, or Requests.

 Expected behavior: The chat should remain in sync when user opens dynamic window \(DW\) in these pages.

 Actual behavior: The chat is not in sync when user goes through multiple pages, and content from another chat on DW can be seen.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1880258

</td><td>

Focus isn't on the input box in dynamic window \(DW\)

</td><td>

 

</td><td>

1.  Navigate to SP portal in DW mode.
2.  Open DW.

 Expected behavior: The focus should be on an input text area where the user can start typing.

 Actual behavior: The focus isn't anywhere.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1880490

</td><td>

Loading a document with .doc ends document QnA with an error

</td><td>

Now Assist gives a message: 'Something went wrong. I'm not able to process the uploaded document right now. I will end this Document Q&amp;A. You can start a new session by uploading the document again, or you can try uploading something else.'

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1880493

</td><td>

The **Send** button isn't enabled after a document Q&amp;A topic exits with an error

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1880507

</td><td>

Input and output topics are not rendered properly in dynamic window \(DW\) and Full Page \(FP\)

</td><td>

Topics will have to be imported to VA Designer with a selected assistant.

</td><td>

1.  Import attached topics or create topics with all input/output controls
2.  Run both in DW and FP.

 Expected behavior: All topics should run correctly.

 Actual behavior: Input and output topics are not rendered correctly in both DW and FP, and an assistant must be selected to import them to VA Designer.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1880552

</td><td>

Agentic reasoning messages continue loading after topic completion

</td><td>

 

</td><td>

1.  Enable AI agents in NAVA/DW.
2.  Run the laptop ordering assistant.
3.  Complete all steps for a topic.

 Expected behavior: All agentic reasoning messages should have a checkmark showing completion.

 Actual behavior: Some messages are still loading after an AI agent topic is complete.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1880646

</td><td>

People card citations are grayed out and occasionally return duplicates

</td><td>

Searching for People cards in the Dispatcher Workspace returns a synthesized response that is grayed out, and with occasional duplicates.

</td><td>

1.  Setup Knowledge Graph and People card on the instance.
2.  Open Dispatcher Workspace.
3.  Enter 'who is Abel Tuter'.

 Expected behavior: Synthesized response with single citation people card for Abel Tuter is displayed and it is not grayed out.

 Actual behavior: Synthesized response with duplicate citation links are displayed sometimes and the citation is grayed out even before selecting it.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1881744

</td><td>

An attachment icon is enabled in the middle of a conversation on a page refresh

</td><td>

 

</td><td>

1.  Start a topic execution on a chat client.

Notice that the attachment icon no longer appears as expected.

2.  Refresh the browser page.

Notice that the attachment appears again.


 Expected behavior: The attachment icon should no longer appear on page refresh in the middle of the conversation.

 Actual behavior: The attachment icon shows up on a refresh.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1881830

</td><td>

Float mode of dynamic window \(DW\) is not resizable after minimizing from a pinned state

</td><td>

A resizing issue of DW occurs in float mode.

</td><td>

1.  Open DW.
2.  Notice it's resizable.
3.  Pin it and then minimize.
4.  Select the tab to display the DW again.

 Expected behavior: Float mode is always resizable irrespective of other state changes.

 Actual behavior: Observe it is not resizable anymore.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1881836

</td><td>

The UIs for chats are mixed up when switching between chats

</td><td>

Components are overlapping in the UI and dynamic window \(DW\) can't be minimized past 420px.

</td><td>

Components are overlapping in the UI:

 1.  Navigate to DW and run a few conversations.
2.  Do a search on Full Page.
3.  Return to DW's home.
4.  Try switching between the active chats.

 DW cannot be minimized past 420px:

 1.  Navigate to Service Portal with DW configured.
2.  Select the 'FAB' icon.
3.  Try to drag the side of DW to make it a smaller chat window.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1881936

</td><td>

Elements in dynamic window \(DW\)/Full Page \(FP\) aren't translated to the user selected language

</td><td>

Untranslated items: titles in the left panel, show/hide sources, the **Skip** button, tooltips, the **Live agent** button in support, toggles and titles in the settings of the left panel, topic descriptions, and the **Submit** button.

</td><td>

1.  Install a language.
2.  Switch the profile language to that language.
3.  Configure a full window/enhanced chat NAVA in a portal.
4.  Navigate to the chat location with the nowassistselfservice ID passed to see the full page experience.
5.  Select around the UI.
6.  Run a catalog/KB/topic by searching 'prestamista de ordenadores portatiles' 'que es el spam' 'pedir cafe'.

 Expected behavior: All elements on the page are translated to the user selected language.

 Actual behavior: All the elements aren't displayed in the user language.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1883412

</td><td>

'Show more' is removed after streaming is done, and for non-streaming, it's not displayed

</td><td>

 

</td><td>

1.  Navigate to Service Portal.
2.  Enter 'what is cookie and as follow how to set it in browser'.

 Expected behavior: 'Show more' shouldn't be displayed.

 Actual behavior: 'Show more' is displayed during streaming and then it's removed.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1883668

</td><td>

The **Attachment** button comes after a page refresh when in doc QnA mode

</td><td>

 

</td><td>

1.  Open the Virtual Agent chat.
2.  Attach a document to it.
3.  Ensure QnA mode is entered.
4.  Observe the **Attachment** button is turned off.
5.  Refresh the page.
6.  Observe that now the **Attachment** button is enabled.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1883927

</td><td>

Turned off text is unreadable

</td><td>

 

</td><td>

1.  Set up Now Assist for May.
2.  Set up a full page.
3.  Navigate to /esc.
4.  Type 'order laptop'.
5.  Start an execution.

The link displays as turned off text.


 Notice that it shows as unreadable.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1883963

</td><td>

Context data doesn't send start\_conversation \_immediately: true when going from the Portal to FPE

</td><td>

 

</td><td>

1.  Open a portal page with 'Enhanced Chat' setup.
2.  Enter a search term into a search combo box.

 Expected behavior: It should send 'start\_conversation\_immediately: true' so that the server knows to immediately start the conversation in the session call and not wait for a sync call to kick off the state machine.

 Actual behavior: The '/session' call doesn't contain 'start\_conversation\_immediately: true' in the contextData.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1884003

</td><td>

The 'People' icon is flashing when going from a streaming response to a final response

</td><td>

 

</td><td>

1.  Open a portal page with 'Enhanced Chat' setup.
2.  Enter a search term into the search combo box that results in a people search result, such as: 'who reports to Abel Tuter'.

 See that the 'People' icon gets shown, goes away, and comes back.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1884112

</td><td>

The dynamic window \(DW\) should occupy the entire screen for a browser window width less than 420px

</td><td>

 

</td><td>

1.  Open DW on a portal.
2.  Reduce the browser window width size to smaller than 421px.

 Expected behavior: DW should fill the entire screen for a width to smaller than or equal to 420px.

 Actual behavior: DW is cut off and not able to occupy the entire screen.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1884123

</td><td>

The 'Attachment' icon isn't appearing on refresh on a new chat in the middle of a topic

</td><td>

 

</td><td>

1.  Open a Virtual Agent chat.
2.  Start any topic.
3.  Select on a new chat.
4.  Refresh the page.

 Observe that the 'Attachment' icon isn't coming.

</td></tr><tr><td>

Walk-Up Experience

 PRB1873610

 [KB2046788](https://hi.service-now.com/kb_view.do?sysparm_article=KB2046788)

</td><td>

After an Yokohama upgrade, the walk-up queue isn't displaying any users who are checked in for any location

</td><td>

The issue occurs because the Rest API contains the snc\_internal role and as the user has snc\_external role, so it disqualifies the walkup user and doesn't render any users in the queue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Work Order Management

 PRB1853346

</td><td>

Upgrading to the 'New Places' API

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1855599

</td><td>

A work order task \(WOT\) isn't assigned to a vendor/contractor when assigning a WOT to a vendor/contractor group

</td><td>

A work order task \(WOT\) isn't assigned to a vendor/contractor when assigning a WOT to a vendor/contractor group, so the **Assigned to** field is empty in CSM/FSM Configurable Workspace.

</td><td>

1.  Navigate to **Dispatcher workspace****Workspace setting**.
2.  Check 'Enable task assignment modal' to ensure an assignment model opens when drag and dropping.
3.  Install the 'Field service territory planning' plugin.
4.  Navigate to a territory model module and set the territory model as true.
5.  Navigate to the **WOT Form page** &gt; **Form layout**.
6.  Add a **Territory** field in the 'DispatcherWorkspace' view if the it isn't already added.
7.  Create a WOT and assign it to some territory that manages at least one contractor group.
8.  Move it in a pending dispatch. Don't give values to **assignment group** or **assigned\_to** fields.
9.  Impersonate as a dispatcher that manages the territory where users assign a work order task.
10. Select the territory from the territory filter.
11. Drag and drop the WOT created in step 7 to the contractor group under 'Contractor Groups'.

 Expected behavior: The **Assigned\_to** field should be populated with the contractor manager.

 Actual behavior: The **Assigned\_to** field comes up as empty.

</td></tr><tr><td>

Work Order Management

 PRB1859719

</td><td>

Upgrade to the new Google Maps Places API for Platform and Portal

</td><td>

Using the new Places API to query and display suggestions on the NDS typeahead component.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1880140

</td><td>

Getting a pop-up error while opening the Work Order Task \(WOT\) on Portal

</td><td>

The error 'There is a JavaScript error in your browser console' pops up.

</td><td>

1.  Hop to any instance.
2.  Attempt to open any WOT on the portal.

 Notice that the error message pops up.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 2 Hotfix 2](yokohama-patch-2-hf-2.md)
-   [Yokohama Patch 2 Hotfix 1](yokohama-patch-2-hf-1-PO.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2056603)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


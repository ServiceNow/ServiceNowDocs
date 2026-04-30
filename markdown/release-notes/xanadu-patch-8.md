---
title: Xanadu Patch 8
description: The Xanadu Patch 8 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-04-10"
reading_time_minutes: 33
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 8

The Xanadu Patch 8 release contains important problem fixes.

-   **Xanadu Patch 8 was released on April 10, 2025.**
    -   Build date: 04-03-2025\_0833
    -   Build tag: glide-xanadu-07-02-2024\_\_patch8-03-26-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X08.00.xlsx).

## Overview

Xanadu Patch 8 includes 147 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp8.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 8 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 8, refer to [KB2045962](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2045962).

## Changes in Xanadu Patch 8

-   **[Create a marketplace engagement method](https://www.servicenow.com/docs/access?context=create-marketplace-eng-mthd&version=xanadu&pubname=xanadu-field-service-management&ft:locale=en-US)**

    Progressive push

    Using contractor ranking, incrementally pushes request to marketplace participants in numerical order based on specified wait duration.

    If the contractor does not respond or accept within a specified time frame, the request is shared automatically to the next ranked candidate. This process continues sequentially down the ranking list until it is shared with all contractors.

-   **[Add a contractor to Marketplace participants post-push](https://www.servicenow.com/docs/access?context=push-task-fsm-mktplc&version=xanadu&pubname=xanadu-field-service-management&section=managing-task-fsm-marketplace&ft:locale=en-US)**

    Use the Add Contractor button to add an eligible contractor to the list of marketplace participants once a work order task has already been pushed to Marketplace.


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

Database Persistence - Data Access

 PRB1649391

</td><td>

Database views using TPC with function fields generate errors

</td><td>

 

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

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1839341

 [KB1891818](https://hi.service-now.com/kb_view.do?sysparm_article=KB1891818)

</td><td>

Update Set with Playbook change failed to install

</td><td>

The invalid preview error, 'Could not find a record in sys\_pd\_snapshot for column snapshot referenced in this update' occurs when moving changes to related to Playbook via update set from one instance to another.

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

User Criteria for Service Catalog

 PRB1819841

 [KB1773413](https://hi.service-now.com/kb_view.do?sysparm_article=KB1773413)

</td><td>

Semaphore exhaustion is caused by the getAllUserCriteria function getting called in widgets

</td><td>

When a public page is accessed by a guest user or web crawler, this prompts a call to the getAllUserCriteria API, which causes semaphore exhaustion.

</td><td>

 

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

 PRB1744106

 [KB1992064](https://hi.service-now.com/kb_view.do?sysparm_article=KB1992064)

</td><td>

Concurrent updates to the group/role assignment results in an incorrect inheritance count

</td><td>

When role/group assignment/removal takes place concurrently for a user, it may result in an incorrect inheritance count. Thus the user may continue to have the role or may not have the required role.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Access Control

 PRB1833782

 [KB1721153](https://hi.service-now.com/kb_view.do?sysparm_article=KB1721153)

</td><td>

Slowness when loading forms with **TableChoice** fields related to the RecordFamilyResolver .archiveTableHasACLTerms code path

</td><td>

Accessing the any form with a **TableChoice** field where the instance has more than 250 archive tables can result in slowness due to RecordFamilyResolver .archiveTableHasACLTerms code path and a change to CACHE\_ARCHIVE\_TABLE\_HAS\_ACL\_TERMS in Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Access Control

 PRB1859273

</td><td>

Query consuming significant time is invoked every minute by the UserHasRole Patcher sys\_trigger

</td><td>

Issue with CSM performance.

</td><td>

Prepare an instance with CSM with five times the data.

 Observe the time taken by the query executed as part of the UserHasRole Patcher scheduled job.

</td></tr><tr><td>

Activity Stream

 PRB1807673

</td><td>

Activity stream size limits aren't applied to a response

</td><td>

During activity stream performance testing, the activity stream load time was tested with variable number of events: 250, 500, 1000, 2000, 5000, 10000, 20000. Each activity stream has even number of comments, emails, attachments, field changes and relations. Knowing that default limit is 2000 for each event type, the expectation was that response time and response size should grow till 10000 events \(2000 events for each of five event types\). Users expect to receive 10k events for activity stream with 20k events. However, all 20k events are returned, causing high response time. In a case with 20k events, the response time is ~13-14 seconds. Large users have even bigger response times, considering that response time grows linearly with increasing number of events.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1834000

</td><td>

Reaper query needs an index to perform optimally

</td><td>

When the reaper query runs, it does not use an index to find the expired records.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1858896

</td><td>

Posts generated by Agentic AI or Now Assist should be posted as an 'AI' user vs ServiceNow

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1836949

</td><td>

The **Send** button does not get enabled when new text is inserted in the chat input after stopping autopilot

</td><td>

 

</td><td>

1.  Start a conversation in agent chat.
2.  Start an autopilot topic by agent.
3.  Stop auto pilot by selecting the **Turn off autopilot** button.
4.  After autopilot is turned off, cut and paste text in the chat input or type some text in the chat input.
5.  Observe the **Send** button

 Expected behavior: The **Send** button should get enabled once text is inserted in the chat input

 Actual behavior: The **Send** button is not enabled once text is inserted. Refreshing the workspace and then inserting text enables the **Send** button.

</td></tr><tr><td>

Agent Chat

 PRB1862727

</td><td>

Show audio modal appears when an Agent presence state is changed to 'Available' for Safari users

</td><td>

User interaction is required on the page for audio to work, especially in inactive tabs. This was being enforced by a modal when the audioContext was detected to be suspended, which occurs when a new AudioContext is created in the page. Now, the modal appears for Safari whenever the presence changes in the inbox to 'Available' to avoid having users refresh the browser to see the modal.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1868186

</td><td>

Conversation history in Agent chat only shows one previous interaction

</td><td>

All previous closed conversations should be shown, but only one past closed conversation is shown.

</td><td>

1.  Enable conversation history in Agent chat in **Conversational Settings** &gt; **Agent Chat** &gt; **Conversation History**.
2.  Log in as an agent in Safari.
3.  Log in as a non-guest user in any other browser.
4.  Start a conversation and accept as agent.
5.  Close the conversation.
6.  Have a few more conversations \(about 2-3\) and close them.
7.  Start a new conversation and scroll up to see the past closed conversations in the chat panel in agent chat.

 Expected behavior: All previous closed conversations \(up to the amount configured in the conversation history settings\) are shown.

 Actual behavior: Only one past closed conversation is shown.

</td></tr><tr><td>

AI Search

 PRB1841579

</td><td>

sn-search-combobox-desktop's use of createGraphQLEffect dispatches errorActionType due to a 401 error for public GraphQL endpoints

</td><td>

The batch request fails due to 401 even though the GraphQL request in the batch was actually successful.

</td><td>

1.  Set the Service Portal Homepage to public.
2.  Set the Typeahead Search Widget to public.
3.  Open Service Portal without logging in.
4.  Open Developer Tools.
5.  Select the **Search Box**.

 Observe in Seismic Dev Tools that the batch request failed due to 401. Then, observe in the Network tab that the GraphQL request in the batch was actually successful.

</td></tr><tr><td>

AI Search

 PRB1847810

</td><td>

When multi-node ingestion is enabled on a production instance, all cloned instances from production will enable multi-node ingestion

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1850218

</td><td>

ais\_child\_table cache is not flushed when glide.ais.disable\_kbb property is changed

</td><td>

KBBs \(knowledge blocks\) should not be indexed as separate document. Instead, they are indexed with the KB document as embedded documents. When only KBB is enabled, the KBB table is removed from the tables.

</td><td>

1.  Enable the knowledge block \(KBB\) flag.
2.  Navigate to cache\_inspect.do.
3.  Check that CACHE\_AIS\_CHILD\_TABLE has kb\_knowledge\_block.
4.  Disable the flag.
5.  Index kb\_knowledge datasource.

 Observe that the KBB is indexed as separate documents.

</td></tr><tr><td>

AI Search

 PRB1851725

</td><td>

Typo Handling blocked terms state doesn't change from 'New' to 'Published' when publishing a search profile

</td><td>

Blocked terms are published, and the UI did not change the state from 'New' to 'Published'.

</td><td>

1.  Add a new blocked term to the Typo Handling dictionary.
2.  Publish the parent profile.

 Observe that the new term still has a 'New' state, the blocked term is actually published, but the UI did not change the state.

</td></tr><tr><td>

Analytics Data API

 PRB1794715

</td><td>

Breakdown elements are repeatedly queried when fetched with the PAR filter

</td><td>

In each API request, breakdown elements \(sites\) are fetched for more than 40 times.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1820588

</td><td>

Vendor Management Workspace Performance Reports show 'error'

</td><td>

After upgrading to Xanadu, Performance Reports show 'error' in Vendor Management Workspace.

</td><td>

1.  Create a time series visualization with a number of open incidents.
2.  In the data source, add the filter conditions:
    1.  Breakdown - Assignment Group.
    2.  Operator - Is \(Dynamic\), Element - Groups I manage.
3.  Make sure there are no incidents with the above filter condition.

 Expected behavior: Observe the message 'No data available. No content available for the selected criteria' and no error should be shown.

 Actual behavior: The Analytics data API is shows the error 'Unable to generate chart. Contact your ServiceNow administrator for more information.'

</td></tr><tr><td>

Cache

 PRB1860082

</td><td>

CacheMetricsManager causes a performance bottleneck at high workloads

</td><td>

Enhance the performance of the Cache Metrics API to accommodate a high volume of concurrent requests.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1815169

</td><td>

Standard Change template \(std\_change\_record\_producer\) does not display the 'Additional comments' column

</td><td>

The **Additional comments** field is not displayed when a change proposal is approved. Instead, another field is displayed.

</td><td>

1.  Create a new standard change proposal with 'Additional comments'.
2.  Request approval and approve it.
3.  Check the std\_change\_record\_producer created.

 Expected behavior: Additional comments should be visible.

 Actual behavior: The **Additional comments** field is not displayed. Instead, another field is displayed \(where the field name is the first in A-Z order of all fields\).

</td></tr><tr><td>

Code Signing

 PRB1857416

</td><td>

Signatures created by signing jobs have an empty **update\_name** field

</td><td>

The record field **update\_name** is empty for generated signatures to prevent records from being checked in to git and to be published to the App repo. Generated signatures should populate the **update\_name** field.

</td><td>

Run a signing job to generate a signature for the record field **update\_name**.

 Notice that the record field **update\_name** is empty

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
4.  Run the scheduled job 'SNC.CMDBDataManagerScriptableApis.executeRetirePolicies\(\);'
5.  Notice that a task is assigned to a user.
6.  Impersonate the user.
7.  Open the CMDB Workspace.
8.  Navigate to **Open my task** &gt; **Open the task** &gt; **Review task** &gt; **Reject**.
9.  Give a reason for the rejection.
10. Select **Save**.

Observe that the task is rejected successfully, and CIs should be available for any other DM policy to pick up.

11. Re-run the same scheduled job 'SNC.CMDBDataManagerScriptableApis.executeRetirePolicies\(\);' or any other policy process.

 Expected behavior: A new task should be created with the CIs with the matching condition because the task was rejected.

 Actual behavior: No task is created, and the cmdb\_data\_management\_task\_to\_ci table is not clearing the old CIs from the rejected task.

</td></tr><tr><td>

Core Platform

 PRB1762070

</td><td>

ServiceNow Performance Dashboards have errors for some graphs

</td><td>

When the user navigates to Service Now Performance Dashboards, some of the graphs are not shown and instead the following error message appears: 'Error:Invalid series data'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1857656

 [KB1935234](https://hi.service-now.com/kb_view.do?sysparm_article=KB1935234)

</td><td>

A Glide function with a substring function may return a 'negative substring length not allowed' error if the arguments are negative

</td><td>

A Glide function with a substring function may return a 'General Data Exception detected by database \(ERROR: negative substring length not allowed\)' error if the arguments are negative.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1844907

</td><td>

Orphan Archive Related Records \(sys\_archive\_related\) with empty Archive\_Map values are not ignored by the archive job

</td><td>

When instance has orphaned archive related records, the archive job does try to find orphan related records, and therefore archive them as a part of the archive run being processed by the archive job. Archive related records should not be created without an archive\_map defined, and every archive related record should be linked to an archive rule.

</td><td>

1.  Log in to the instance.
2.  Create a new archive rule on incident with any conditions.
3.  Add an archive related record for incident\_task.
    1.  Save the archive rule.
    2.  Delete the new archive rule.
    3.  Notice the archive related record becomes orphaned.
4.  Create a parent incident.
    1.  Create a new incident task for the incident.
    2.  Create a new incident with the parent incident created, where the relationship is incident.parent\_incident.
    3.  Create incident tasks for this new incident.
5.  Create a new archive rule on incident with conditions so that it archives the previously incident created, and if the parent incident is archived, the child incident will also be archived.
6.  Create an archive related record for the archive rule created with the metadata:
    1.  Action - archive.
    2.  Reference - incident.parent\_incident.
    3.  Reference table - Incident \[incident\].
    4.  Reference element - parent\_incident
    5.  Reference table rule - empty.
7.  Activate the new archive rule created.
8.  Run it.

 Expected behavior: The archive job should ignore invalid archive related records, and only linked archive related rules should be picked up and processed.

 Actual behavior: The archive job finds and processes orphaned archive related records for all the archive rules the job runs.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1850816

</td><td>

z\_tmp tables should not be eligible for compaction

</td><td>

Compaction is running on z\_tmp tables when they should not be.

</td><td>

Generate a z\_tmp table that is eligible for compaction.

 Notice that compaction is running on z\_tmp tables when they should not be.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1854621

</td><td>

Archive reparenting issue occurs when sys\_attachment is configured as a related record for an archive rule

</td><td>

The table name 'incident' remains instead of being renamed to 'incident\_task' after running the archive rule.

</td><td>

1.  Create an archive rule for the 'incident' table.
2.  Define archive the related records incident\_task and sys\_attachment.
3.  Set up test data.
    1.  Ensure incident\_task records references incident.
    2.  Ensure sys\_attachment records references incident and incident task.
4.  Run the archive rule.
5.  Verify that both incident and incident tasks are moved to ar\_incident and ar\_incident\_task.
6.  Check that the sys\_attachment records reference to the incident record are moved to ar\_system\_attachement.

 Notice that the table name is still 'incident' instead of 'incident\_task'.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1855929

</td><td>

Investigating sys\_attachment records that are not reparented correctly in Vancouver

</td><td>

Reparenting issue for records in sys\_attachment in the gateway DB.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1859358

 [KB1968830](https://hi.service-now.com/kb_view.do?sysparm_article=KB1968830)

</td><td>

The orphan cleaner does not check both the primary and archive tables to determine if a record is an orphan

</td><td>

Orphan cleaner is enabled by setting property 'glide.db.orphan\_cleaner.peripheral\_tables' to clean records from the peripheral tables sys\_attachment, sys\_attachment\_doc, and sys\_audit, sys\_journal\_field. It only checks if a record exists based on the document ID reference's tablename. When the document ID reference's tablename is not updated after archiving records during archive reparenting, the orphan cleaner deletes non-orphan records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1726762

</td><td>

SQLCancel does not end some queries that stream data

</td><td>

Cancellation takes five minutes and scales with the amount of inserted data because the close\(\) method is called and reads the rest of the data before ending the transaction. The database query isn't killed.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1793744

</td><td>

Change CorrelationAliasProvider to use ConcurrentLRUCache instead of SynchronizedLRUCache

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1795746

</td><td>

getRhinoFeatureSet causes contention when multiple threads ask for the current rhino feature set

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1800838

</td><td>

GLIDE\_ELEMENT\_EXTENSIONS cache access is slow due to CacheManager

</td><td>

There's no need for this to use CacheManager. Extensions don't need to be flushed when using extension point listeners.

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

 PRB1800843

</td><td>

Orbit class loader no longer uses ParallelWebappClassLoader

</td><td>

Orbit class loader no longer uses ParallelWebappClassLoader likely due to resource usage. This is noticeably one of the larger concurrency bottlenecks in glide. Glide runs with reloadable='false' flag to prevent reloading class files, therefore access to cache of class files don't need to synchronized.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1859279

</td><td>

StringCache causes a concurrency bottleneck due to SynchronizedLRU

</td><td>

Enhance StringCache to support a large volume of concurrent requests.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1840597

</td><td>

Admins are unable to see rollback record fields

</td><td>

After installing the data privacy application, security ACLs were installed for the sys\_rollback\_context table. The user is unable to see anything in the table even though they have admin access.

</td><td>

 

</td></tr><tr><td>

Declarative Actions

 PRB1824763

 [KB1754358](https://hi.service-now.com/kb_view.do?sysparm_article=KB1754358)

</td><td>

The **CSM/FSM Configurable Workspace** UI action overflow menu isn't working

</td><td>

After upgrading to Xanadu, there's a UI issue on the 'Record Default' page variant in the CSM/FSM Workspace. The overflow menu for UI actions doesn't work as expected, and the UI actions aren't stacked behind the three-dot menu item when the page is zoomed in.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1833735

 [KB1710860](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710860)

</td><td>

Azure Cloud Discovery schedules do not consider the member accounts that are selected when creating the discovery schedule via the discovery configuration page

</td><td>

When a cloud discovery schedule is created using the 'Cloud Discovery' option, member accounts are not included in the schedule, even if all member accounts are selected on the CDU page. Upon editing a previously created schedule in the Cloud Workspace, it shows that no member accounts are present in the schedule. However, if the accounts are added through the Cloud Workspace and the discovery is run, it works as expected, triggering patterns for the member accounts.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Employee Center

 PRB1818417

</td><td>

Javascript console errors on the Human Resource Management \(HRM\) ticket page

</td><td>

Navigating to the to-do page displays console errors.

</td><td>

1.  Create a HR case - Employee Travel Visa Request for an employee with the manager 'Abel Tuter'.
2.  Let the case move to 'Awaiting approval'.

The approval record is created for a user with no roles \(in this case, Abel Tuter\).

3.  Open the approval task in to-do's page.
4.  Select **HR Service** which opens the HRM ticket page.
5.  Select the approval to-do in the HRM ticket page.

 Expected behavior: User should be able to approve or reject the task from HRM ticket page.

 Actual behavior: The to-do page has console errors.

</td></tr><tr><td>

Employee Center Pro

 PRB1814341

 [KB1704519](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704519)

</td><td>

The 'Give Feedback' text in Experience Feedback Drawer widget is upside down for the Chinese/Japanese/Korean languages

</td><td>

All the vertical languages are considered and are read from top to bottom.

</td><td>

1.  Provision an instance with EC Pro installed with the Chinese, Japanese or Korean language.
2.  Switch to one of the above installed languages.
3.  Open /esc?id=hri\_user\_profile.

 Expected behavior: The 'Give feedback' text displays vertically.

 Actual behavior: The 'Give feedback' text displays upside down.

</td></tr><tr><td>

Event Management

 PRB1852761

</td><td>

NullPointerException \(NPE\) in Impact Calculation after topology change

</td><td>

NPE occurs after performing a topology change in Event Management.

</td><td>

1.  Navigate to Application Services.
2.  Navigate to ServiceNow Event Management.
3.  Select **View Map**.
4.  Add a Linux \(lnux100\) server under Alert Processing.
5.  Send a minor alert on lnux100.
6.  Select the Impact Tree.
7.  Navigate to **Impact Calculation** &gt; **Impact**.
8.  Change the influence for impact rule to 50 to perform a topology change.

 Observe the following NPE, 'Exception at executeImpactCalculation. Msg: Cannot invoke 'java.lang.Integer.toString\(\)' because 'this.fContributedSeverity' is nulllastImpactCalcDate: nullImpactSyncHandler'.

</td></tr><tr><td>

Flow Engine

 PRB1804504

</td><td>

Curly brackets within an inline script are parsed unexpectedly

</td><td>

The user observes the error 'Cannot invoke 'Object.toString\(\)' because the return value of 'com.snc.process\_flow.val.InVal.value\(\)' is null'.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1828174

 [KB1709903](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709903)

</td><td>

Do-In-Parellel branch remains on a 'Waiting' state after MID action

</td><td>

The flow should go to a 'Complete' state after it returns from MID, but it remains in a 'Waiting' state with only one of the parallel branches having been executed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1843595

</td><td>

The **Details** field is missing in Attestation Designer after Xanadu upgrade

</td><td>

The **Details** field is missing in the attestation designer after the upgrade to Xanadu from Washington DC.

</td><td>

1.  Navigate to attestation designer.
2.  Select the gear icon for any of the questions.

Observe that no **Details** field is present.

3.  View the same attestation designer in a Washington DC instance.

 Observe that the **Details** field is present.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1854275

</td><td>

Risk Assessment Designer doesn't launch or open a saved assessment

</td><td>

The session hangs and causes the browser to time out when using Risk Assessment Designer.

</td><td>

1.  Impersonate a user.
2.  Enter assessment types in the Filter Navigator.
3.  Navigate to **GRC Risk** &gt; **Administration** &gt; **Assessment Types**.
4.  Open an Assessment.
5.  Select **Risk Assessment Designer UI**.

Notice that the session hangs and eventually causes the browser to time out.

6.  Close the browser.
7.  Wait two minutes.
8.  Relaunch the browser.
9.  Impersonate the same user.
10. Enter assessment types in the Filter Navigator.
11. Navigate to **GRC Risk** &gt; **Administration** &gt; **Assessment Types**.
12. Select **Risk Assessment Designer UI** from the list.
13. Select **New Assessment New Assessment Load Assessment** &gt; **Load Assessment** when the designer opens.
14. Search for the assessment in the search modal.

 Notice that it hangs and eventually times out the session.

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1846612

</td><td>

MID server stops when it fails to format a log message

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1849037

</td><td>

Change to glide.graphql.gliderecord.maxResults.limit

</td><td>

The property ensures the GraphQL engine is not overconsuming resources for GlideRecord\_Query requests.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1857188

</td><td>

When DISH sends back an empty response for a Hermes Service \(for example, MIF-Hermes\) the preexisting hermes\_cluster\_config records are not cleared

</td><td>

Instances connected that have called the Hermes callback listener and set up the hermes\_cluster\_config table cannot be removed by returning an empty response to those instances from MIMIR.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1788794

 [KB1651068](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651068)

</td><td>

The 'Scratchpad: Show HR Service Fields' business rule causes errors in the system logs

</td><td>

A base instance business rule causes multiple errors in the system logs, including: 'com.glide.script.RhinoEcmaError: Cannot convert null to an object.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery

 PRB1831691

</td><td>

HTML dynamic parameters on HR templates do not work as expected

</td><td>

HTML dynamic parameters on HR templates are not replaced with the actual value when used in links.

</td><td>

 

</td></tr><tr><td>

Inbound Email Actions

 PRB1841147

</td><td>

Sensitive Data Redaction does not work for Inbound email actions if 'Stop processing' is enabled

</td><td>

This issue impacts inbound email actions even if 'Stop processing' is enabled.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1839006

 [KB1952753](https://hi.service-now.com/kb_view.do?sysparm_article=KB1952753)

</td><td>

OpenAPI Step with MID fails

</td><td>

When following the OpenAPI Step document to create an action to make an API to an OpenAPI Step, a Guice configuration error occurs.

</td><td>

Refer to the listed KB article for details.

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
3.  Modify a field on that record that isn't part of the CDC Definition.

 Observe that this creates an update record on cdc\_queue\_ih, which should not be created.

</td></tr><tr><td>

Issue Auto Resolution for Virtual Agent

 PRB1862157

</td><td>

IAR Simulation does not use the correct API

</td><td>

Custom intents are returned when the regular IAR flow is executed. Custom intents are not returned when simulation is used, because the API takes in a list of objects instead of a single object. The simulation feature is using the single prediction instead of the bulk one, so the custom IAR's are not being returned.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1827639

</td><td>

Selecting a knowledge base from 'Explore our Knowledge Bases' in a portal redirects to the wrong URL

</td><td>

A URL with incorrect search results is returned when selecting a knowledge base from /esc?id=kb\_home with AI Search enabled on the application 'Knowledge Management - Service Portal' version 1.0.0.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1849608

 [KB1906766](https://hi.service-now.com/kb_view.do?sysparm_article=KB1906766)

</td><td>

Knowledge Management \(KM\) notifications are unable to be triggered

</td><td>

Email notifications aren't triggered for Knowledge Articles because some KM artifact records in the Knowledge Advance plugin are overridden by the Activity Subscription plugin. This occurs in Xanadu and Yokohama.

</td><td>

1.  Select any Knowledge Base \(KB\) that is under subscription.
2.  Publish any Knowledge Article from the KB.

Notice that the published article is not triggered to the subscriber in the KM subscription.

3.  Attempt to trigger the published article by navigating to **Notification** &gt; **Related list** &gt; **Email log**.

 Notice that the notification is not getting triggered for 'KM Subscription: Article published'.

</td></tr><tr><td>

List Administration

 PRB1776103

</td><td>

Column personalization doesn't work

</td><td>

The issue is related to the list page template. List personalization works when using a record list bundle.

</td><td>

1.  Log in to any Xanadu instance.
2.  From UIB, create a Now list page using the List Menu Template.
3.  Save the page and open it in runtime.
4.  Edit columns to add columns to the list.
5.  Refresh the page using browser refresh.

 Expected behavior: New columns should be saved.

 Actual behavior: New columns added are not saved after refresh.

</td></tr><tr><td>

List Administration

 PRB1795127

</td><td>

Selecting an already selected item in the list menu causes the list to render incompletely

</td><td>

The list renders now-loader.

</td><td>

1.  Select an existing experience or create a new one.
2.  Add a new page from List Page Template.
3.  Once the **Preview** button in UIB is enabled, select the **Preview** button to open the page in a new tab.
4.  In the List menu, select a list item to open the list.
5.  Once the list finishes rendering, select the same list item again.

 Notice that this time, the list renders now-loader instead.

</td></tr><tr><td>

List Filters

 PRB1751177

</td><td>

Inconsistency in Presentational list filters

</td><td>

There is an inconsistency between the data shown and the filter applied for empty values. In one scenario, there is inconsistency while applying filters on the string column and the number column. If the filter text value is empty, the **Apply** button is disabled for the string column, but still enabled for the number column. Selecting **Apply** still retains the older filter. In another scenario, there is also an inconsistency between the data shown and the filter applied for empty values. Fields, which are empty in a table, are being shown as 0 in the presentational list based on the data type. When they are filtered, they should be considered empty or should be considered as 0 if it is shown as zero.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1840375

</td><td>

InputFormScreen doesn't work when the function containing the InputFormScreen comes from a list

</td><td>

An InputFormScreen with Fetch Type = Prefetch/OnDemand does not show the dependent parameter of level three \(parameter3 depends on parameter2 which depends on parameter1\).

</td><td>

1.  Open the mobile \(requestor\) app.
2.  Log in to an instance.
3.  Select **ALP List** &gt; **AppletList** &gt; **ListSegmentsWotInc** .
4.  Swipe left on item from the list.
5.  Choose 3LevelsParamsNotInline\_IFSPrefetch / 3LevelsParamsNotInline\_IFSOnDemand.

 Expected behavior: Choice three shows the option 'None', and when picking values in choice one and choice three, choice three shows the values configured to it.

 Actual behavior: Choice three doesn't show value at all, and when picking values in choice one and choice three, choice three does not show the values configured to it.

</td></tr><tr><td>

Oracle Reconciliation

 PRB1788175

</td><td>

Processor factor mapping is missing the Oracle core factor entry for some CPU names

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Filters

 PRB1812254

</td><td>

Migrated breakdown filters without indicators appear as 'Invalid Selection' on the filter source

</td><td>

When the user selects breakdowns in the source, they should be able to see all breakdowns regardless of whether they have at least one indicator or not. After the migration, the user should still be able to see only breakdowns with at least one indicator.

</td><td>

1.  Create a dashboard in classic.
2.  Add the following breakdown filters:
    1.  Groups
    2.  Incident.Category
    3.  Incident.Priority
    4.  Users.Active
3.  Add a few Platform Analytics widgets to the dashboard.
4.  Configure the widget using different indicators.
5.  Migrate the dashboard.
6.  Edit the User.Active filter after migrating the dashboard.

 Notice that the filter source shows an invalid selection.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1863262

</td><td>

Backend data load up for a fix for breakdown filters migrated incorrectly

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1857887

</td><td>

sys\_flow\_data\_definition is missing sys\_update\_name in sys\_update\_xml payload

</td><td>

This PR makes sys\_flow\_data\_definition use FlowDesignerSuppress which blanket returns 'true' for suppressNameAndUpdateName.

</td><td>

1.  Navigate to sys\_flow\_data\_definition.
2.  Create new record with just name.
3.  Navigate to sys\_update\_xml, sort by created.
4.  Open record for the data definition created.

 Expected behavior: The payload has non-empty sys\_update\_name and sys\_name and sys\_package.

 Actual behavior: The payload has empty sys\_update\_name and sys\_name and sys\_package.

</td></tr><tr><td>

Predictive Intelligence

 PRB1858849

</td><td>

Empty **row\_count** field in the ml\_solution table leads to an error message being logged while parsing an integer from empty string from the ml\_solution row\_count attribute

</td><td>

When the **row\_count** field is empty while training a solution, the following error message is logged, 'Exception caught while building data Description list: For input string: '': no thrown error'. This occurs only for Java-based solutions.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1847963

</td><td>

Mining data from either a record list or KPI doesn't create a process mining project properly

</td><td>

Several tables were tried in the risk space. sn\_grc\_issue and sn\_compliance\_control from either a KPI or list of records. From a KPI, there's an error that the instance isn't licensed for this KPI or table to produce a project. For a list of records, it presents an empty project with no definition, including the table the records are in.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1852247

</td><td>

Work Notes results shows HTML code in cluster concepts

</td><td>

Work notes are collected from sys\_journal\_field table which stores results with HTML tags.

</td><td>

1.  Initiate work notes analysis without LLM.
2.  Select **View Results**.

 Notice that HTML tags are present in cluster concepts.

</td></tr><tr><td>

Process Mining

 PRB1856986

</td><td>

In Xanadu, meter-based licenses block users from mining

</td><td>

 

</td><td>

1.  On a Xanadu instance, download a meter-based license.
2.  Execute a full mine.

 Observe that this triggers a licensing error.

</td></tr><tr><td>

Process Mining

 PRB1860897

</td><td>

Allow sample mining on an evaluation project from workbench

</td><td>

Sample mining an evaluation project works from a KPI but not from the workbench.

</td><td>

1.  Navigate to workbench.
2.  Attempt to sample mine.

 Notice that the user receives mining exception.

</td></tr><tr><td>

Project Management

 PRB1850637

</td><td>

Duplicate resource\_aggregate\_weekly and resource\_aggregate\_monthly records are created intermittently

</td><td>

Code in the UpdateActualsFromTimeCard function of the ResourceActuals SI raises an event to update aggregates for each day when a time card is approved or recalled, causing duplicate resource\_aggregate\_weekly and resource\_aggregate\_monthly records to be created intermittently.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1864892

</td><td>

The **Time Constraint** field dictionary default value does not work in Project Workspace while creating the Project Task

</td><td>

The default value for the **Time Constraint** field is set to 'ASAP' irrespective of Default value.

</td><td>

1.  Set the Default value for the **Time Constraint** field through dictionary from Project Task form.
2.  Open the Project Workspace.
3.  Open any project.
4.  Create a Project Task.

 Observe that the default value for the **Time Constraint** field is set to 'ASAP' irrespective of Default value.

</td></tr><tr><td>

Schedule Optimization

 PRB1860079

</td><td>

Performance impact due to the Optimization business rule

</td><td>

A 'Optimization Metadata processor' business rule is made in sys\_attachment async.

</td><td>

 

</td></tr><tr><td>

Seismic Framework

 PRB1859951

</td><td>

ClientInteraction aggregate transactions creates a performance bottleneck

</td><td>

Setting glide.client\_metrics. aggregation.enabled=true on a fully loaded system will cause performance to decrease significantly.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1782856

</td><td>

A business rule executes in the 'module' scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1841707

</td><td>

Turn on ECMAScript 2021 \(ES12\) mode is not toggled after upgrade/zboot

</td><td>

Turn on ECMAScript 2021 \(ES12\) mode is off.

</td><td>

1.  Unload a sys\_script\_include XML with Turn on ECMAScript 2021 \(ES12\) mode toggled.
2.  Make sure sys\_es\_latest\_script=true.
3.  Add the script include to the 'Update' folder in the com.glide.sg plugin.
4.  Zboot the instance.
5.  Spin the instance with Zboot.
6.  Check the record.

 Expected behavior: Turn on ECMAScript 2021 \(ES12\) mode is on.

 Actual behavior: Turn on ECMAScript 2021 \(ES12\) mode is off.

</td></tr><tr><td>

Service Catalog Variables

 PRB1863977

</td><td>

3DES Deprecation in Service Catalog Variables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1816637

</td><td>

In TB service connection, two CIs that are already part of a service and belong to the same CI type aren't added even if they match the traversal rule

</td><td>

When calculating a TB service, it starts from the tagged CIs, and then goes rule by rule to bring the next level according to the rule. When a rule is defined on the same class, if two CIs of that class have a connection that matches the rule between them, but those CIs are already part of a service, this connection isn't added to service.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1816925

</td><td>

Service Mapping \(SM\) Discovery state always remains 'Active' if entry points are not reachable

</td><td>

When SM scheduler is run, the Discovery status for SM Discovery and end point status is created. The host is not in CMDB, so the end point status runs 'Host detection'. Host detection creates a new prob with agent\_correlator with horizontal Discovery. When host detection is finished, it updates the end point and the state becomes 'Complete'. However, SM Discovery doesn't update, so the business rule was not triggered to set the Discovery status to 'Completed'.

</td><td>

1.  Created the service with two unreachable entry points.
2.  Create scheduled discovery that runs on this service by name attribute.
3.  Run a discovery scheduler.

 Notice that the discovery state will always remain 'Active'.

</td></tr><tr><td>

Service Portal

 PRB1834496

</td><td>

The user cannot input a value into a widget

</td><td>

The user cannot input a value into a widget \[KB knowledge base\].

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1854090

</td><td>

Cross product downgrade rights should exclude inactive downgrade relationships

</td><td>

There's no behavior change for the users on recon. This is intended to exclude inactive products in the backend.

</td><td>

1.  Create cross product downgrade rights in samp\_downgrade\_model.
2.  Set the Active column to **False**.
3.  Run reconciliation.

 Although the reconciliation result is as expected, it was found that inactive cross products downgrade rights been processed during recon logs, which is incorrect.

</td></tr><tr><td>

Software Asset Management

 PRB1865260

</td><td>

Unallocated installs should not infer unallocated installs to user-subscription-only entitlements

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB1842035

 [KB1833581](https://hi.service-now.com/kb_view.do?sysparm_article=KB1833581)

</td><td>

Replication lag due to slow updates on cmdb\_sam\_sw\_install table from jobs

</td><td>

An update in the SamPreferenceStageHandler script include causes replication lag.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Standard Change Catalog

 PRB1856886

 [KB1931818](https://hi.service-now.com/kb_view.do?sysparm_article=KB1931818)

</td><td>

Value is not populated from the template if a new text area field is added when creating or modifying a standard change proposal

</td><td>

The **template\_value** field contains 'STARTSWITH' instead of the '=' operator, which doesn't allow the field to be populated with the value when the template is applied to the change request record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Survey Management

 PRB1842390

 [KB1832412](https://hi.service-now.com/kb_view.do?sysparm_article=KB1832412)

</td><td>

The HR case number is not displayed completely on the survey card on the My surveys page

</td><td>

The HR case number is not displayed completely on the survey card rendered using the 'My surveys' widget on My surveys page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Transaction Management

 PRB1866307

</td><td>

Sanitizing URLs in GlideElementURL

</td><td>

For performance, the sanitized URL can be cached rather than computing the same value repeatedly.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1810910

 [KB2012523](https://hi.service-now.com/kb_view.do?sysparm_article=KB2012523)

</td><td>

In Xanadu, the onChange client script executes twice on the 'Record Default' UX screen of CSM Configurable Workspace

</td><td>

The onChange client script executes twice on the base instance 'Record Default' UX Screen.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1847059

</td><td>

Formatting on the special handling notes header is aligned to the left in Xanadu

</td><td>

Special Handling Notes is not aligned properly and is completely formatted to the left.

</td><td>

 

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

Virtual Agent

 PRB1819265

</td><td>

Follow-up queries that are not in English intermittently hang

</td><td>

As soon as follow-up utterance is submitted, VA Input extraction fails, preventing anything else from happening after that. This includes the creation of a sys\_cs\_fdih\_invocation record.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1852222

</td><td>

'Time Out Abandoned Virtual Agent \(VA\) Conversations' is not respecting the timeout configured for NAP in sys\_cs\_channel

</td><td>

VA conversations are not closed out according to the timeout configured for NAP.

</td><td>

1.  Set the timeout on NAP channel to four hours.
2.  Create a conversation.
3.  Don't update the conversation

 Expected behavior: Conversation should be closed after four hours.

 Actual behavior: Conversation is closed after two hours.

</td></tr><tr><td>

Virtual Agent

 PRB1859339

</td><td>

An attachment icon isn't aligning with the rest of the other icons in the chat box

</td><td>

 

</td><td>

1.  Navigate to a Xanadu instance.
2.  Log in as a user and then open Service Portal.
3.  Initiate a chat to see the attachment icon.

 Expected behavior: All the icons in the chat box should align.

 Actual behavior: The attachment icon is slightly above the other icons and doesn't align with the rest.

</td></tr><tr><td>

Virtual Agent

 PRB1862370

</td><td>

Skill executions are stuck when Now Assist guardian settings \(prompt injection, offensiveness\) are enabled

</td><td>

Skill test runs are not working from the skill kit, whereas executions outside of the skill kit \(for example, OneExtend.execute\(\) in async mode\) is working fine for the same settings. This is due to an unsupported operation exception coming from EvaluationServiceImpl.java.

</td><td>

1.  Create a skill from the Now Assist Skill Kit.
2.  Enable prompt injection from the Now Assist Guardian settings \(use option as Block\).
3.  Select **Run Test** on that skill.

 Expected behavior: **Run Test** should work irrespective of the guardian setting because users can execute the same One Extend capability outside of the skill kit.

 Actual behavior: **Run Test** is stuck due to an exception \(Error Execution of evaluation request failed for batch result: fbb3afc4c348e2149e83d62f0501312b due to error: null\).

</td></tr><tr><td>

Virtual Agent

 PRB1866633

</td><td>

In APAC data center instances, AI agents are not working even after accepting the Global Routing Consent information message

</td><td>

Global routing is not working even after consenting on the info message for data center instances in the Asia-Pacific region.

</td><td>

1.  Deploy a new instance from the APAC data center.
2.  In an APAC region instance, select **Agree on the Global Routing Consent info message**.

 Expected Behavior: The AI Orchestrator should be invoked.

 Actual Behavior: Even after accepting the consent, AI agents are not functioning, and the error message occurs: 'Sorry, there was a problem on my side trying to complete this request. Try asking again later'.

</td></tr><tr><td>

Virtual Agent

 PRB1866635

</td><td>

Trail Assists are incorrectly loaded for six or more tools triggered from Now Assist Panel \(NAP\) with skill Discovery

</td><td>

This problem doesn't occur with playground and NAP triggers.

</td><td>

1.  Have a use case with six or more tools.
2.  Navigate to NAP.
3.  Enter an utterance for the use case with six tools and skill Discovery.
4.  Invoke AI Agents use case:
    1.  Utterance: Get me the price of
    2.  Washing machine - 2
    3.  Refrigerator – 3
    4.  Monitor – 2
    5.  Toaster – 1
    6.  Vacuum cleaner – 2
    7.  Dishwasher – 2

 Expected behavior: Trail Assists should be 50.

 Actual behavior: Trail Assists are loaded as 25.

</td></tr><tr><td>

Web UX Runtime

 PRB1769964

</td><td>

In Agent Chat, intermittently the inbox icon won't disappear when the page is loaded

</td><td>

In Agent Chat, intermittently the inbox icon won't disappear when the page is loaded because sn-canvas-viewport doesn't handle includesFieldsAndParams in certain usecases.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1859719

</td><td>

Upgrade to the new Google Maps Places API for Platform and Portal

</td><td>

Using the new Places API to query and display suggestions on the NDS typeahead component.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 7 Hot Fix 1](https://downloads.docs.servicenow.com/enus/xanadu/rn/hotfix/xanadu-patch-7-hf-1.pdf)
-   [Xanadu Patch 7a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2038547)
-   [Xanadu Patch 7](xanadu-patch-7.md)
-   [Xanadu Patch 6](xanadu-patch-6.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


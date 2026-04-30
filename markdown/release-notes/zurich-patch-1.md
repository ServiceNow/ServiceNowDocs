---
title: Zurich Patch 1
description: The Zurich Patch 1 release contains important problem fixes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-09-10"
reading_time_minutes: 144
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 1

The Zurich Patch 1 release contains important problem fixes.

-   **Zurich Patch 1 was released on September 10, 2025.**
    -   Build date: 09-08-2025\_1328
    -   Build tag: glide-zurich-07-01-2025\_\_patch1-08-20-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z01.00.xlsx).

## Overview

Zurich Patch 1 includes 514 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-zp1.png "Top 10 problem categories")

## Security-related fixes

Zurich Patch 1 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 1, refer to [KB246342](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2463421).

## Changes in Zurich Patch 1

-   **[Create an endpoint for clients to access the instance](https://www.servicenow.com/docs/access?context=t_CreateEndpointforExternalClients&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Token FormatFormat of the token to generate. The format determines the structure of a token and the information it includes.

    Subject ClaimField in the User \(sys\_user\) table that's used to populate the value of the subject \(sub\) claim of a JWT token. The sub claim is a piece of information that identifies the subject, or user, of the JWT token. This field only applies if the **Token Format** is JWT.

-   **[Create an OAuth JWT API endpoint for external clients \(machine to machine integration\)](https://www.servicenow.com/docs/access?context=create-jwt-endpoint&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Token FormatFormat of the token to generate. The format determines the structure of a token and the information it includes.

    Subject ClaimField in the User \(sys\_user\) table that's used to populate the value of the subject \(sub\) claim of a JWT token. The sub claim is a piece of information that identifies the subject, or user, of the JWT token. This field only applies if the **Token Format** is JWT.

-   **QueryRangeACLAuditor**

    This patch includes the May Maintenance update script in the form of a script include \(QueryRangeACLAuditor\). This script is not triggered automatically and must be run after a patch upgrade. More details on running the QueryRangeACLAuditor and its functionality can be found in [KB2046494](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2046494).


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

 PRB1907408

</td><td>

A rollback blocking the install/upgrade for non-global scope users in a domain-separated instance

</td><td>

Non-global domain users have been blocked from being able to install/upgrade on domain-separated instances. There is now a fix to allow this behavior and hence this code change made on App Manager can now be rolled back.

</td><td>

 

</td></tr><tr><td>

CMDB Query Builder

 PRB1910646

</td><td>

A large query from Query Builder may lead to excessive memory utilization on a server

</td><td>

A large query from the Query Builder module \(involving &gt;200 union of cmdb and cmdb\_rel\_ci, or &gt;100 unions of large tables\) from an internal instance was seen to have caused a large spike in memory utilization on a database server, causing degradation/performance impact.

</td><td>

 

</td></tr><tr><td>

Database Indexes

 PRB1901971

 [KB2206973](https://hi.service-now.com/kb_view.do?sysparm_article=KB2206973)

</td><td>

A missing index on the 'sys\_id' column of the 'cmdb\_qb\_result \_base' table causes a replication lag when the table size is large

</td><td>

The index on the 'sys\_id' column of the 'cmdb\_qb\_result\_base' table is missing on 14000+ instances. Due to this missing index, when 'Table Cleanup on Query Status' \(qb\_query\_status\) table is triggered on such instances, it can lead to replication lag issues, especially when large volumes of records need to be deleted from the qb\_query\_status table. This can lead to memory exhaustion, and records are not properly cleaned up.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Internationa lization Features

 PRB1911538

 [KB2266945](https://hi.service-now.com/kb_view.do?sysparm_article=KB2266945)

</td><td>

The 'Translated Text Synchronize' business rule has an infinite loop against v\_plugin

</td><td>

The 'Translated Text Synchronize' business rule goes in an infinite loop. The virtual table v\_plugin \(or any virtual table\) can refresh \(delete and insert of records\) the table upon query. Since v\_plugin has translated fields, glideRecord insert tries to insert into the sys\_translated\_text table, which runs the 'Translated Text Synchronize' business rule. This business rule tries to query the owner table \(for example, v\_plugin again, which can trigger the refresh again and this goes on in an infinite loop\). This is causing performance impact against many instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Record Watcher

 PRB1894715

</td><td>

ChecklistItem Responder is too slow to effectively scale with normal usage of the platform, leading to the record watcher queue becoming backlogged

</td><td>

A performance issue has been identified related to checkLitsItem responders and ACL \(Access Control List\) checks while creating checkListItems in Visual Task Board's cards. These issues caused delays, especially when tasks had more than 50 checklist items. This is primarily because getItemsByChecklistId\(\) is invoked every time a checklist item is added or a card is moved between lanes. It loops through all items under a checklist and performs individual ACL evaluations \(read/delete access\). These checks result in: Repeated database lookups, redundant ACL checks for the same parent checklist, and slower response times, especially when checklist items exceed 50.

</td><td>

 

</td></tr><tr><td>

Service Operations Workspace

 PRB1875164

 [KB2179535](https://hi.service-now.com/kb_view.do?sysparm_article=KB2179535)

</td><td>

Users aren't able to dot walk to fields in a Service Operations Workspace list

</td><td>

.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1919041

</td><td>

An empty and read-only 'Template value' input field causes an error when saving a record: 'Cannot read properties of null \(reading 'hasChildNodes'\)'

</td><td>

To reproduce, users need a record with an input field of type 'Template Value', that is empty and also read-only. The error shows when saving the record.

</td><td>

1.  Log in as an admin.
2.  Navigate to **All** &gt; **incident.CONFIG**.
3.  Add a field called **Test Template**.
4.  Make it of the type 'Template Value' and save.
5.  Select the 'Advanced' view and the 'Dependent Field' tab.
6.  Select 'Use dependent field' and a field, such as 'Channel'.
7.  Save the changes.
8.  Navigate to **All** &gt; **incident.CONFIG**.
9.  Create a UI Policy that will always make the new template value field read-only.
10. Pick an existing incident.
11. Make a change to the **Short description** field and save.

 Expected behavior: The record should save without error.

 Actual behavior: There's an error: 'Cannot read properties of null \(reading 'hasChildNodes'\)'.

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

Access Control List \(ACL\) Rules

 PRB1910482

</td><td>

Ensures the QueryRange ACLAuditor doesn't generate Security Attribute with blank script

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1916144

</td><td>

gen\_ai\_ prefixed ACL types should use '\* ACLs' for their default rule name

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1918225

</td><td>

Ensures conditional\_table \_query\_range ACL customizations are honored with QueryRange ACLAuditor reruns

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1918943

</td><td>

Ensures QueryRange ACLAuditor rerun to preserve the timestamps of query ACLs created by previous audit run

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1917141

</td><td>

Ensures QueryRange ACLAuditor is re-run to preserve all the query ACLs created by the previous audit run, in case of query\_range ACL customizations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1923191

</td><td>

Prevent re-generating ACLs with a different sys\_id after upgrade when ACL schema changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1918613

</td><td>

Saving a form while comments and worknotes are in progress produces a warning pop-up that unsaved changes will be lost

</td><td>

A comment that should be posted is not posted and a warning dialog appears.

</td><td>

1.  Provision an instance with the CSM \(com.snc.customerservice.demo\) plugin installed.
2.  Log in as a user with elevated privileges.
3.  Navigate to **CSM** &gt; **All cases** and open any record.
4.  Select the **Compose** button and select **Compose Comments**.
5.  Copy and paste text and post the comments.
6.  Select the **Compose Comments** button again and type in comments.
7.  Minimize the comments window.
8.  Save the form.

 Expected behavior: The comment should post and a warning dialog should not appear.

 Actual behavior: A warning pop-up appears that says unsaved changes will be lost and the dialog is not closed.

</td></tr><tr><td>

Admin Center

 PRB1887565

</td><td>

The Core UI button group is missing from the left border

</td><td>

This issue is not coral-specific.

</td><td>

 

</td></tr><tr><td>

Admin Center

 PRB1887577

</td><td>

There is no appropriate error message displayed when leaving the required 'Send to' empty for Adoption Blueprints

</td><td>

This issue occurs when using a screen reader, such as JAWS, to announce the 'Send to' label. The error message shouldn't be generic.

</td><td>

1.  Launch an instance in a Chrome browser.
2.  Navigate to **Application navigator** &gt; **Admin center**.
3.  Navigate to **Adoption blueprints** &gt; **Adoption blueprints**.
4.  Select the **Share** button.
5.  Share the adoption blueprint page modal dialog.
6.  Turn the screen reader on.
7.  Check whether the label 'Send To' is announced when the focus is on respective form field.

 Expected behavior: An appropriate and specific error message is displayed when leaving the required **Send to** field empty, and the error message should be identifiable by the screen reader. The error message shouldn't be generic.

 Actual behavior: There isn't an appropriate error message displayed when leaving the required **Send to** empty, and the field label is highlighted in red.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1909214

</td><td>

Updating an agent's presence as an integration user via the Agent API fails

</td><td>

The gr.canWrite\(\) checks aren't working as expected when the API caller is an integration user. The integration user should be allowed to update the presence state. If the API caller has the awa\_integration\_user role, the request should go through. If the API caller doesn't have sufficient roles, the request should fail with a 500 error.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1908263

</td><td>

Safari audio issues in inactive tabs

</td><td>

Audio doesn't work properly when the user switches to an inactive tab.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1911696

</td><td>

Issues with displaying the list of 'Transfer to Agent' and 'Transfer to Queue' in third party chats

</td><td>

When an agent selects 'Transfer to Agent' and sets the searchTargetList payload for the first time, the target list doesn't show anything. It appears in second attempt. This issue also occurs for 'Transfer to Queue'.

</td><td>

1.  Set up third party chat interactions.
2.  Start a conversation with a live agent.

</td></tr><tr><td>

Agent Chat

 PRB1922878

</td><td>

The agent chat's audio alert for inbox should stop playing when the agent has responded even if the alert's mp3 has not finished playing

</td><td>

 

</td><td>

1.  Add a 20 or more seconds mp3 ring tone to the **System UI** &gt; **Audio Files**.
2.  Update the 'connect.notification.audio\_alert' to the new mp3 name.
3.  Sign in as an agent.
4.  Ensure that the 'Inbox Audio Alerts' is turned on.
5.  Have a customer request for a chat with a live agent.

On the Agent Workspace, the newly added alert is played.

6.  Accept the chat as the agent.

 Expected behavior: The alert should stop playing as the agent accepts the incoming chat.

 Actual behavior: The alert continues to play until the end of the ring tone file, regardless of if the agent has already picked up the call.

</td></tr><tr><td>

Agent Chat

 PRB1925414

</td><td>

There's issues with the 'Start Voice' API call in a domain-separated environment

</td><td>

There's issues with the 'Start Voice' API call in a domain-separated environment, both inbound and outbound calls and impersonation due to a guest user.

</td><td>

1.  Initiate an inbound or outbound call that triggers the 'Start Voice Interaction' API in a domain-separated environment.
2.  Observe that the API is logged under the user 'guest' \(see Splunk logs\) and an interaction record is created in the default domain instead of the user's domain.
3.  Attempt to retrieve interaction using getInteractionRecord.

 See that it fails due to a domain mismatch.

</td></tr><tr><td>

AI Agents

 PRB1913281

</td><td>

Script fix takes longer than usual as it runs through the whole table

</td><td>

The fix script update tools execution columns takes 15 minutes to run during the plugin upgrade in some instances.

</td><td>

1.  Install AI Agents v3 in Yokohama.
2.  Upgrade the instance to Zurich.

 Notice that the plugin installation is taking a long time, in which the fix script AI Agents v4 update tools execution columns takes 15 minutes.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1921084

</td><td>

HR Plugin's sys\_attachment ACL triggers AI Search late binding and performance delays

</td><td>

There's performance degradation of all AI search queries in the HR app due to unnecessary ACL evaluations for sys\_attachment on sources that don't use or index attachments.

</td><td>

1.  Enable force late binding for any data source.
2.  Hit RagRetriverAPI with a limit of 2000.

 Expected behavior: The limit for AI Search service backend should be capped to 5000.

 Actual behavior: The limit for AI search service backend is 6000.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1921138

</td><td>

Sys\_attachment ACLs shouldn't be evaluated when none of the indexed source attachments are turned on

</td><td>

 

</td><td>

1.  Ensure that none of the indexed source attachments are turned on.
2.  Observe if sys\_attachment ACLs are still being evaluated.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1927991

</td><td>

sn\_cs.VASystemObject. getAgentSkills ForAssistant took ~600 milliseconds to return

</td><td>

It shouldn't take that much time to return.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1928661

</td><td>

Advanced configuration needed for a performance improvement for Knowledge Graph \(KG\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1909140

</td><td>

An API endpoint which can delete users via a GlideQuery is required for XCC

</td><td>

The XCC Scoped App can't delete users one at a time. It needs a way to query a subset of users.

</td><td>

 

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1909142

</td><td>

When a user principal is written with the DirectUserImporter and one exists, the update fails

</td><td>

Stream is wrapped mistakenly during the serialization process from a list. Not all of the principal imports do a check for the DirectPrincipalImporter vs the ImportSetImporter. The streams should be closed effectively.

</td><td>

Attempt to send a new user principal that updates an existing user.

 Notice that updates to existing users fail, and removal of a user's group fails.

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1909146

</td><td>

The 'External Content Ingestion JS' API must do an undefined check on 'sourceId'

</td><td>

Use the newly qualified 'External Content Ingestion' APIs for ingesting principals with 'sourceId'. If 'sourceId' is undefined, see that the principals insert or updates fail.

</td><td>

 

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1909153

</td><td>

Change SOURCE\_ID\_FIELD to reference connector\_config uration\_id instead of connector\_config uration\_id\_s

</td><td>

The current licensing table process fails for some connectors because its querying the wrong field.

</td><td>

 

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1915715

</td><td>

Users get a 400 status code from calling a REST API: /api/now/v1/ais /external\_content /user\_mapping

</td><td>

Users get a 400 status code from calling a REST API, which should be 201. These following IT tests are failing: LegacyUserPrincipalImportRESTIT .multipleUsersWithAllFields \_successfully Inserted, LegacyUser PrincipalImport RESTIT. userWithOnly ExternalGroupField \_successfullyInserted, LegacyUser PrincipalImport RESTIT. userWithOnly ExternalUserField \_successfullyInserted.

</td><td>

 

</td></tr><tr><td>

AI Search for Next Experience

 PRB1857879

</td><td>

Regular catalog item results should use a 'Pencil' icon for consistency

</td><td>

 

</td><td>

1.  Open an AI Search \(AIS\)-enabled instance with AIS for global search.
2.  Search for a catalog item that doesn't have a picture, like 'laptop'.

 Notice that the Genius Results use the 'Pencil' icon, but the regular results use the 'Book' outline. Notice that in Portal, both regular and Genius results use the 'Pencil' icon. The icon should be consistent between regular and Genius results for the same record.

</td></tr><tr><td>

AI Search for Next Experience

 PRB1859890

</td><td>

There's improper use for current.update in a business rule

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search for Next Experience

 PRB1917747

</td><td>

Zing Migration Tool does not let users select unused SACs from base instance migration records

</td><td>

The tool only allows the user to select SACs currently used in a workspace. If one of the SACs from the base instance records is not being used in a workspace, it cannot be selected for migration in the tool.

</td><td>

 

</td></tr><tr><td>

AI Search for Next Experience

 PRB1920468

</td><td>

Upgrade issues on sn-search-facet and sn-search-result-wrapper component

</td><td>

This issue was observed in Zurich. The component loading state is being used inside the facet component because without the component loading flag, the facets still working fine. Another issue occurring in this problem is the appearance of the **Hide filters** button, which was not visible in the previous release.

</td><td>

1.  Hop in to the instance.
2.  Navigate to the **CSM/FSM Configurable Workspace**.
3.  Open a case record from the list.
4.  Navigate to the contextual side panel on the right hand side.
5.  Select on the magnifying glass icon at the top of the list.
6.  Search something in the search bar.
7.  Let the results generate.
8.  Select the **Full view** search icon shown in the video and landing on the full view search page.
9.  Notice that the facet component is in a loading state, when it should load as expected.
10. Return to the side panel.
11. Select on the filters below the search bar.

 Notice that it lands on a new page where the sn-search-facet component is rendered, and a **Hide filters** button appears on the top right which previously wasn't there.

</td></tr><tr><td>

AI Search

 PRB1861012

</td><td>

Sn-search-combobox sends exact match data broker execution

</td><td>

In Zurich, sn-search-combobox sends two databroker/exec calls to fetch if a search configuration has an exact match enabled. This occurs for 'SOW Incident' and 'HR Case' form direct loads.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1889815

</td><td>

KBB should filter out the none-embeddedMatch docs

</td><td>

The default of KKBs sent to LLM is one.

</td><td>

1.  Create KB with two KBBs.
2.  Search for the content that only exists in KBB1.

 Expected behavior: Only KBB1 content is sent to LLM.

 Actual behavior: Both KBB1 and KBB2 content are sent to LLM.

</td></tr><tr><td>

AI Search

 PRB1902960

</td><td>

Now Assist Q&amp;A Genius Results don't display when the Log Signals Server side is turned on through Search Application Configuration

</td><td>

SearchAnalyticsPayload is null when the Log Signals Server side is turned on.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1911804

</td><td>

There's a null point error for the index stats reporter

</td><td>

Note the JavaScript evaluation error on 'new sn\_ais. IndexStatsReporter\(\) .reportAllDataSource EmbeddingStats\(\);'.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1915070

</td><td>

The GENIUS\_RESULT\_ TRIGGERED event causes incorrect updates to the sys\_search\_event table when in async mode

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1921609

</td><td>

There's enlarged Now Assist loading icons in Portal with Dynamic Window \(DW\) turned on

</td><td>

 

</td><td>

1.  In znowassiststable, turn on DW in Portal.
2.  Open Portal.
3.  Perform a search.

 Observe the Now Assist Genius Results loading icons are enlarged.

</td></tr><tr><td>

AI Search UX

 PRB1921789

</td><td>

There's an initial loading issue on the facet component of the sn-search-result-wrapper component in the full-view-search page

</td><td>

The root cause of the issue is the componentProperty ChangedEffect isn't triggered post the componentBoot strappedEffect when, for the first time, the facet component is added in the DOM tree.

</td><td>

1.  Navigate to an instance.
2.  Navigate to CSM/FSM Configurable workspace.
3.  Open a case record from the list.
4.  Navigate to the contextual side-panel on the right hand side and select the magnifying-glass-icon at the top of the list.
5.  Search something in the search bar, then let the results generate.
6.  Select the full view search icon and land on the full view search page.

 Actual behavior: The facet component is in a loading state.

 Expected behavior: The facet component should load.

</td></tr><tr><td>

AI Search UX

 PRB1927351

</td><td>

On a 'Release Readiness' report, sn-search-genius-card-assist, an unapproved third party package impacts the merge to master

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1932120

</td><td>

Non-conversational catalogs shouldn't have an option to request in a chat

</td><td>

 

</td><td>

1.  Provision an instance with September GenAI apps.
2.  Turn on Dynamic Window \(DW\) on portal.
3.  Search for a non-conversational catalog, like an Apple iPhone.

 Notice there's a pop-up on the citation for an Apple iPhone 13 with an option to request in chat. A citation for a non-conversational catalog should open in a new tab automatically.

</td></tr><tr><td>

AI Service - Glide Interfaces

 PRB1919181

</td><td>

The 'Ml solution' table gets updated whenever a prediction is done because of the 'last accessed time' column

</td><td>

 

</td><td>

1.  Navigate to the ml\_solution table.
2.  Open a record with a successfully trained model.
3.  Run a prediction through the 'Test solution' page.

 See that the ml\_solution table gets updated.

</td></tr><tr><td>

Analyst Workbench

 PRB1914271

</td><td>

Workbench loads very slow

</td><td>

 

</td><td>

1.  Mine a project with Ideal time analysis.
2.  Open the Analyst Workbench.

 Expected behavior: Workbench should load within 10 seconds.

 Actual behavior: Workbench loads very slow.

</td></tr><tr><td>

Analytics Data API

 PRB1915499

</td><td>

The funnel is displayed incorrectly in the workload saving widget

</td><td>

In the workload saving widget, the funnel chart appears visually distorted or collapsed. It doesn't represent the values clearly or it's too narrow to distinguish the sections properly.

</td><td>

1.  Navigate to the AIOps 360° overview.
2.  Set the date filter to 'Last 3 months' or 'Last 6 months.'

 Expected behavior: The funnel chart renders proportional segments clearly showing auto-closed alerts, grouped alerts, events to significant alerts, and alert to incident compression.

 Actual behavior: The funnel chart appears visually incorrect \(collapsed or distorted\). It doesn't represent the values clearly or it's too narrow to distinguish the sections properly.

</td></tr><tr><td>

Analytics Export API

 PRB1916425

</td><td>

Selecting View All doesn't show the records in the Case Spot Light List Widget

</td><td>

Not all records are shown.

</td><td>

1.  Log in to the configurable workspace \(now/cwf/agent/home\).
2.  Select the home page.
3.  Create a New dashboard with the 'New List Bundle Widget'.
4.  Navigate to the List Widget in 'Case Spotlight' tab for Customer Service Manager Dashboard and apply the filter.

 Notice that not all records are shown.

</td></tr><tr><td>

Appointment Booking

 PRB1923326

</td><td>

There's insufficient server-side input validation for 'Reschedule Appointment' in FSM appointment booking

</td><td>

A user was using actualStartDate and actualEndDate \(display values\) for rescheduling, but the system only validates startDateUTC and endDateUTC. Also, a REST validation parameter was removed during refactoring, causing validation not to trigger.

</td><td>

 

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1934812

</td><td>

App Tier CPU increased during loadsim test executions

</td><td>

App tier CPU on a servers increased by 4 times of the baseline numbers.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1916164

</td><td>

Authentication Agentic AI Agent controls

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1917269

</td><td>

Authentication Agentic AI agent controls

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1918608

</td><td>

Low-level impersonated users don't capture front end metadata traces during ATF tests

</td><td>

sys\_traced\_metadata table does not have the sys\_ui\_action type associated.

</td><td>

1.  Create an ATF test on some form \(for example, the incident form\).
2.  For the first step, impersonate a user with a low-level role \(not the roles ATF test designer, ATF WS designer, or ATF test admin\).
3.  Add a test step that selects a UI action on the form \(for example, select **Resolve** on the incident form\).

 Expected behavior: sys\_traced\_metadata table has 1 transaction related to the Select UI action step \(needs to be the sys\_ui\_action metadata that was executed when the selection occurred\).

 Actual behavior: sys\_traced\_metadata table does not have the sys\_ui\_action type associated with Select UI action step.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1920825

</td><td>

ATF becomes less responsive if a large number of cloud runner tests are queued

</td><td>

A test can take over a minute before it starts. This problem becomes more noticeable the more mutually exclusive tests are involved.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1924154

</td><td>

Attempting to run a non-UI test in cloudrunner results in the individual tests being 'Pending' forever

</td><td>

This also occurs if running through the CICD Run ATF Suites API and setting 'run in cloud' to true.

</td><td>

1.  Create an on demand schedule with run in cloud = true.
2.  Add a non-UI test suite.
3.  Execute now.

 Expected behavior: The test suite runs.

 Actual behavior: The test suite is stuck in running, with the individual tests all pending.

</td></tr><tr><td>

Cache

 PRB1922845

</td><td>

File handlers are left open if a LazyInputStream is closed before being read by LargeContent DiskCache

</td><td>

If LazyInput\#close is called before the internal StreamSupplier is opened by LazyInputStream\#stream, the InputStream remains open until finalizers are calling during garbage collection. File handles are leaked when using LargeContentDiskCache and only call getMetadata\(\) or contentExists\(\). Because the supplier is never invoked and the stream is never opened, closing the LazyInputStream doesn't close the underlying FileInputStream. These leaked file handles are only released when the garbage collector runs finalizers.

</td><td>

1.  Start Glide.
2.  Run Java Process Status \(JPS\).
3.  Get the Process ID \(PID\) of the glide process.
4.  Run LSOF.
5.  Take note of the file descriptor entries.
6.  Flush the cache.
7.  Load the Service Operations Workspace home page.
8.  Repeat step 3 through step 6.

 Expected behavior: File descriptor entries is close to the original number.

 Actual behavior: Notice the 10's or 100's of additional file descriptor entries, indicating that the file handlers are left open.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1917146

</td><td>

Restricted caller access \(RCAs\) for Case look up Assistant

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1919807

</td><td>

Missing RCA permissions for the 'Create approval' subflow

</td><td>

This issue occurs in HR Service Delivery AI Agent Collection.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1928914

</td><td>

There's a RCA issue for email reply recommendation

</td><td>

The sparkle icon is missing because this RCA isn't in an allowed state.

</td><td>

 

</td></tr><tr><td>

Change Advisory Board for Service Operations Workspace

 PRB1882132

</td><td>

The user is redirected to the 'Current CAB Meeting Details' page after selecting the **Upcoming CAB Meetings** button

</td><td>

When the CAB meeting state is 'Canceled', the user is redirected to the 'Current CAB Meeting Details' page after selecting the **Go to Upcoming CAB Meetings** button.

</td><td>

1.  Create a CAB meeting.
2.  Impersonate the CAB meeting owner, then start the meeting.
3.  Change the CAB meeting state from **In Progress** to **Canceled** in the 'CAB Meeting Details' page.

Observe that the CAB meeting workbench shows 'Meeting is Cancelled.'

4.  Select **Go to Upcoming CAB Meetings.**

 Expected Behavior: The user is redirected to the 'Upcoming CAB Meetings' page.

 Actual Behavior: The user is redirected to the 'Current CAB Meeting Details' Page.

</td></tr><tr><td>

Change Advisory Board for Service Operations Workspace

 PRB1882187

</td><td>

Pagination controls are floating for CAB Workbench in SOW

</td><td>

Pagination controls are floating based on the number of agenda items per page.

</td><td>

1.  Create a CAB meeting with more than ten agenda items.
2.  Open the CAB workbench.

 Observe that the pagination controls are floating based on the number of agenda items per page.

</td></tr><tr><td>

Change Advisory Board for Service Operations Workspace

 PRB1898140

</td><td>

The 'Schedule Change' view in the Service Operations Workspace \(SOW\) executes the databroker 'a3bc9ca40b511110 c85e8a8db777 b278' too many times

</td><td>

 

</td><td>

1.  Create any Change.
2.  Open the Change in SOW.
3.  Use the Schedule calendar.
4.  Open the browser tools.
5.  Open the network tab.
6.  Reload the Schedule calendar.
7.  Search the requests made for 'a3bc9ca40b511110c85e8a8db777b278'.

 Notice the number of times it is executed, when it should be triggered once on load.

</td></tr><tr><td>

Cloud Provisioning and Governance

 PRB1923320

</td><td>

An ADO provision fails if a user has secret variables due to a bug fix on encrypted catalog variables

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Ensure that Azure Cloud Discovery is completed.
3.  Ensure that ADO Cloud Discovery is completed.
4.  Navigate to ESC portal and Launch CSC ADO Catalog.
5.  Fill all required parameters.
6.  Submit the catalog.

 Observe an error: '\#\#\[error\]InvalidParameter: The supplied password must be between 6-72 characters long and must satisfy at least 3 of password complexity requirements from the following...'

</td></tr><tr><td>

CMDB Data Manager

 PRB1864548

</td><td>

The 'Delete' policy only deletes half the records in 'delete policy task'

</td><td>

A delete policy was created to delete 50k cmdb\_ci records. After running the 'CMDB Data Manager Archive/Delete Policy Processor' job, five tasks were created, each targeting to delete 10k records \(50k records\). But, only 5k records were deleted per the task, leaving behind 5k records. 'Summary details from Task: Summary - Total CI Count:10000 Deleted CI Count:5000 Archived CI Count:0 Non-Retired CI Count:0'.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1921400

</td><td>

Update the signature timestamp on JIT-loading when the signature isn't present in the table, and compare the signature timestamp with the plugin upgrade timestamp before loading

</td><td>

During instance patch upgrades, many update events are generated for the sn\_kmf\_record\_signature table as the JIT loads many build-time signatures from the plugin to the table. The signature is considered stale, so the signature is loaded again into the table, after which its timestamp is updated. So, a signature which is not present in the table initially is loaded 2 times. The signature is already present in the table as its loaded 1 time.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1909506

</td><td>

Database performance is impacted due to the ASYNC: Script job

</td><td>

De-duplication template APIs fetch unnecessary data which slows down queries, impacting database performance.

</td><td>

1.  Create a de-duplication template for any class \(for example, Linux Server\).
2.  Select the default options for Main CI, Merge Attributes, Merge Relationships, Merge Related Items and Duplicate CI Actions.
3.  Save and publish the template.
4.  Manually add de-duplication tasks to the template \(if there are no matching tasks found\).
5.  Run the template.

 Observe slow queries during the template run.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1911028

</td><td>

The QB UI throws a 500 error on selecting columns for a node in QB Query construction

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1914626

</td><td>

Insufficient access that's caused by a 'run as' user specification causes fewer records than expected to be included in the generated task

</td><td>

This works fine if the 'run as' user is a system admin.

</td><td>

 

</td></tr><tr><td>

Content Library Portal

 PRB1903754

</td><td>

Fix scripts don't trigger the 'Historical Data Collection for Past Three Months' job

</td><td>

Fix scripts don't trigger 'Historical Data Collection for Past Three Months' job while installing the content library portal. Also, the job '\[Content Library\] Historical Data Collection for Past One Year' didn't pull any content.

</td><td>

 

</td></tr><tr><td>

Customer Service Management for Field Service Management

 PRB1913871

</td><td>

The 'sn\_som\_clm' app has an older version of the Contracts core app as a dependency in Zurich base instance apps

</td><td>

The correct app version is Contacts Core app version 2.4.8.

</td><td>

1.  Launch an instance on latest Zurich.
2.  Install the Contracts Core app.

 Observe that the app installation is not happening due to the unavailability of Contracts Core app version 2.3.0.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1886874

</td><td>

There's a CypherToResultNow LLMloadRow failure

</td><td>

While running the 'GraphQueryExecutor' API, the user gets a null pointer exception \(java.lang.NullPointerException\), but still gets a response.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1886876

</td><td>

Sys id isn't returned for the cypher2results API

</td><td>

The sys\_id doesn't appear from the cypher2results API for the user.

</td><td>

1.  Hop in to an AI test instance.
2.  Impersonate a user.
3.  Create or update any incident change short description, for example, something which contains 'kg test'.
4.  Observe that the info message added without impersonating the user works.

 Notice that the sys\_id doesn't appear from the cypher2results API for the impersonated user when using GlideRecordSecure.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1889657

</td><td>

The getForTables on Global Graph doesn't give the override data from the child graph

</td><td>

 

</td><td>

1.  Create a contribution graph to Global Graph.
2.  Update the description for the sys\_user node in child graph.

 Expected behavior: The object of sys\_user object is overridden.

 Actual behavior: The original object of sys\_user from global graph remains.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1890778

</td><td>

Missing properties of parent graph nodes in the child graph

</td><td>

The child graph has node definitions without any properties or empty property arrays, which is invalid.

</td><td>

1.  Create a parent graph with two nodes, 'sys\_user' and 'cmn\_location'.
2.  Keep 'all\_properties': false.
3.  Explicitly add a few properties in each node.
4.  Create a child graph of the parent graph with 1 node \(alm\_asset\).
5.  Get the child graph.
6.  View its JSON.

 Notice that it will not have properties of parent graph nodes, such as for 'sys\_user' and 'cmn\_location nodes' when they ideally they should have properties for all nodes.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1892362

</td><td>

getForTables isn't working on a few tables, such as sn\_nb\_action\_recom mended\_action

</td><td>

 

</td><td>

Invoke getForTables on Global graph with the sn\_nb\_action\_recommended\_action table.

 Notice that getForTables isn't working on a few tables.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1892396

</td><td>

The parent graph is able to select itself as the parent graph

</td><td>

 

</td><td>

1.  Create a graph.
2.  **Save** it.
3.  Select it as the parent graph.
4.  Select either **Extension** or **Contribution** as the model.
5.  Update the graph.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1896451

</td><td>

The saveNode/saveEdge functions don't update and cause a unique key violation

</td><td>

With the saveNode/saveEdge functions, the user can perform incremental saves on a graph. However, saving an existing node/edge causes a unique key violation. Also, saveNode returns 'false' instead of 'true' on a successful save.

</td><td>

1.  Create a graph.
2.  Get a node from returned graph JSON.
3.  Change the description, then pass to saveNode.

 Observe the unique key violation on the table or node\_type.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1898289

</td><td>

Excluded tables are included in getForTable method's output for node

</td><td>

 

</td><td>

Execute getForTables method for the graphtest\_standalone\_four table with depth.

 Notice that the output of the method contains a node for the sys\_package and sys\_scope tables, which are excluded tables.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1898627

</td><td>

Glide is not enforcing the 16MB limit on column values when inserting or updating records

</td><td>

It is observed that records are getting created with columns of bigger sizes, in some cases about 1G, when the max should be 16MB.

</td><td>

Create worknotes with size greater than 16MB.

 Observe the sys\_amb\_message created is greater than 16MB, and in splunk, there are records created with huge sizes via some background processes.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1898644

</td><td>

The update set is failing for graphs with extension and contribution models

</td><td>

In scenario one of this issue occurs when the parent graph, child graph \(extension model\), and contribution graph \(of parent graph\) are a part of same update set. While previewing the update set after importing it, the preview fails for the child graph and contribution graph. In scenario 2 this issue occurs when the parent graph exists in an instance, the child graph is imported, and the contribution graph of parent graph from an update set doesn't fail. When attempting to get the parent graph by the get\(\) method, it fails to get the nodes and edges of the contribution graph.

</td><td>

1.  Preview and commit the update set with the graphapi\_update\_set\_1.xml attachment in an instance.
2.  Skip any errors while previewing the update set.
3.  Preview the update set with the graphapi\_update\_set\_2.xml attachment in an instance.
4.  Execute the script in the background script of that instance.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1898886

</td><td>

The GraphQueryExecutor API fails at querying a cross-scope graph without specifying the scope name

</td><td>

Users get an exception when calling GraphQueryExecutor in a scoped application: 'Exception: Unable to find any graph definitions for labels: \[sys\_user\]'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1899248

</td><td>

getForTables on an extended graph of a global graph returns empty edges array

</td><td>

kg\_global\_graph extends Global Graph with no metadata defined. Global Graph has use\_dictionary defined, so there should be both nodes and edges returned from getForTables from the incident.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1902217

</td><td>

Missing edges when includeInboundEdges flag is 'false' for GetForTables

</td><td>

 

</td><td>

Check the output for getForTables method for global graph with following input: 1.  tables: incident
2.  depth: 0
3.  includeInboundEdges: false

 Observe that the output will have only seven edges, and it doesn't include multiple edges such as 'assigned\_to' and 'opened\_by'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1902272

</td><td>

Properties added in the Overridden node can't be queried

</td><td>

sys\_updated on should be queried as the child graph has all the properties for alm\_asset.

</td><td>

1.  Create a parent graph from userGraph.json.
2.  Notice that the sys\_user and alm\_asset nodes has a few properties defined.
3.  Create child graph \(extension model\) from userGraphChild1.json.
4.  Notice that the User and Asset nodes has all\_properties defined.
5.  Execute the cypher query on the child graph.

 Notice that the error 'sys\_updated\_on does not exist in graph node for table: alm\_asset' is thrown when executing the cypher. The properties of the overridden node alm\_asset are swapped by the base attributes \(parent node\) properties when using get\(\) on both the graphs.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1902348

</td><td>

Duplicate edges are generated in the contribution and extension model when the edge\_type name is the same, and the parent and child source nodes refer to the same table

</td><td>

One edge is expected for alm\_asset, but two are found.

</td><td>

1.  Create a graph with the following edges:
    1.  Edge in the parent graph with 'Asset' referring to the alm\_asset node and 'User' referring to the sys\_user node.
    2.  Edge in the child graph with 'Device' referring to the alm\_asset node and 'Employee' referring to the sys\_user node.
2.  Execute the cypher query on the child graph with 'synonymFlag' as 'true'.

 Notice that there's an error when executing the cypher.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1903772

</td><td>

There isn't an option to pass hops to getConnected TableList

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1904413

</td><td>

In the NLQ User graph, the 'install\_status' field from assets renders the choice value instead of the choice label in the bot

</td><td>

When the user initiates a conversation with 'What are my assets,' the bot's response includes something like 'Installation status is marked as \(1\).' However, the response should be 'Installation status is in use.'

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1904854

</td><td>

When migratedTo TableName is true, the getForTables method doesn't return the correct nodes

</td><td>

When migratedToTableName is true, the getForTables method doesn't return the correct nodes. The output contains only one node and is missing many nodes, including itself.

</td><td>

1.  Make sure ScopedGraphMetadata is configured for global graph.
2.  Make sure migratedToTableName is true.
3.  Execute getForTables with the following input: table=core\_company, depth=0, and includeInboundEdges=false.

 Notice that the output contains only one node and is missing many nodes, including itself.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1904883

</td><td>

The source\_graph for overridden nodes point to the incorrect sys\_id

</td><td>

The source\_graph for overridden nodes point to the parent graph sys\_id instead of the contribution graph sys\_id.

</td><td>

1.  Create a parent graph with the sys\_user and alm\_asset nodes.
2.  Create a contribution graph with the above graph as parent, and include the User \(sys\_user table\) and Asset \(alm\_asset table\) nodes.
3.  Make sure migratedToTableName is true.
4.  Execute the get\(\) method for the parent graph.
5.  Check the source\_graph for the sys\_user and alm\_asset nodes.

 Expected behavior: The overridden nodes point to the contribution graph sys\_id.

 Actual behavior: The overridden nodes point to the parent graph sys\_id.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1906058

</td><td>

getForTables on KG global graph doesn't give all synonyms of a node from child graphs

</td><td>

The **Synonym** field isn't set in the cached node when it is created from a JSON object.

</td><td>

1.  Update the incident node synonym in a contribution graph.
2.  Update the incident node synonym on a different contribution graph.
3.  Perform a new sn\_db.GraphMetadata\('sn\_kg.global\_graph', true\).getForTables\(\['incident'\], 1\).

 Expected behavior: The user receives all synonyms from the contribution graphs.

 Actual behavior: The user returns one synonym from a contribution graph.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1906309

</td><td>

The user is unable to add data conditions to the sys\_meta\_graph\_node and observes a pop-up that reads 'First select a table' where the table is already selected

</td><td>

Within the KG nodes there appears to be an option wherein users can add a data condition to further filter the returned results. However, when the user attempts to 'add filter condition', the browser throws a pop-up reading, 'First select a table' \(even after the 'table' is selected\) and prevents the user from adding a filter to the node.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1906408

</td><td>

Incorrect cypher query response when cypher query is generated \(GraphQueryBuilder\) by an encoded query which has ISEMPTY

</td><td>

 

</td><td>

1.  Create a cypher query by GraphQueryBuilder with the incident node and encoded query 'closed\_atISEMPTY'.
2.  Execute the cypher query and notice that the result count is 0.
3.  Execute the same encoded query with GlideRecord and notice that the result count is 33.

 Ideally both of the result counts should be matching.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1906482

</td><td>

passesAclCheck should precheck that a table is valid

</td><td>

Currently, if a user writes a query that references a non-existent table, it hits a null point error. This should precheck if the input Genius Results are valid first and immediately fail if that's the case.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1907396

</td><td>

Graph API needs to honor data filtration/data filter rules

</td><td>

 

</td><td>

1.  Create a data filter.
2.  Query against that table.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1907812

</td><td>

Cyphers of a certain form throw an error reading, 'Error: Node with types: \[incident\] is not an ID property'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1908179

</td><td>

The sysevent0001 table should be excluded from Graph API

</td><td>

sn\_db.GraphMetadata.is TableExcluded \('sysevent0001'\) returns false but should return true because sysevent is excluded and also a rotated table.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1909106

</td><td>

GraphQueryBuilder fails when encoded query contains javascript:gs.beginningOf NextYear\(\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1909182

</td><td>

A cypher query created by GraphQueryBuilder \(with encoded query having date condition\) is missing date condition

</td><td>

A cypher query is missing the date condition when created using GraphQueryBuilder for the 'Problem' node with the encoded query 'closed\_atONThis year@javascript:gs .beginningOfThisYear \(\)@javascript:gs.end OfThisYear\(\)^active=false'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1909639

</td><td>

Create a unique index on dynamic\_choice\_override of \(choice, namespace, category, attribute\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1911690

</td><td>

Users are getting a 'Property + entity exceed maximum length \(63\)' error

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1911868

</td><td>

GraphQueryBuilder throws a NullPointerException

</td><td>

The error is thrown, 'java.lang.NullPointerException: Cannot invoke 'com.glide.db.Element Descriptor.getType\(\)' because 'ed' is null.'

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1911870

</td><td>

GraphQueryBuilder throws a 'java.lang.Number FormatException: empty String' error

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1911877

</td><td>

GraphQueryBuilder throws StringIndex OutOfBounds Exception

</td><td>

The error is thrown with 'java.lang.StringIndex OutOfBounds Exception'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1911994

</td><td>

GetForTables isn't returning properties inside the payload for global graph for specific nodes

</td><td>

The property key is missing for the nodes 'incident' and 'sys\_user'.

</td><td>

1.  Log in to a Zurich instance.
2.  Run the snippet.
3.  Observe the payload returned.

 Notice that the property key is missing for the nodes 'incident' and 'sys\_user', and another key called 'allProperties' is added with a 'false' value, and the 'node-type' is coming as a string rather than array with slashes.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1912116

</td><td>

The 'CypherToResults' API is missing a table/sysid injection in the results

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1913010

</td><td>

GetForTables not returning related node for sys\_user table in KG global graph

</td><td>

All nodes should be returned, or at least the first 1000 nodes, instead of throwing an error.

</td><td>

1.  Log in to a znowassist instance.
2.  Run the snippet.

 Observe the exception error thrown, 'com.snc.db.graph.GraphException: Too many Nodes Requested for subgraph, total number of nodes allowed: 1000'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1914130

</td><td>

getForTables is throwing exception on few tables, such as wf\_workflow\_version

</td><td>

The exception error is thrown, 'Exception: Script execution error: Script Identifier: null.null.script, Error Description: org.mozilla.javascript. EvaluatorException: GlideRecord.set TableName - empty table name'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1914733

</td><td>

getForTables throws exceptions on a few tables

</td><td>

getEdgeList returns a response when it's called from global scope, but it gives an error when it's called from sn\_kg scope. Also, getEdgeList doesn't return all the edges between the two nodes.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1916615

</td><td>

GraphQueryExecutor is unable to find the metadata for Workflow Data Fabric \(WDF\) tables when joining to a Glide table using Global Graph

</td><td>

An exception is thrown.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1916672

</td><td>

Use a primary key rather than the sys\_id for the 'Target key' field when creating edges for subgraphs

</td><td>

The current code assumes its sys\_id, but with Workflow Data Fabric \(WDF\), that's no longer always the case.

</td><td>

1.  Create a WDF table with a primary key column that's name is something other than the sys\_id.
2.  Create a reference to that table from another table.
3.  Create a name subgraph with the tables in them.
4.  Try to traverse the edge for that reference.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1917979

</td><td>

Inbound edges don't appear in global graph APIs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1918749

</td><td>

A metadata update and Glide family changes to Knowledge Graph's Semantic Store

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1918934

</td><td>

No inbound edges are added in getForTables for a custom created graph

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1922241

</td><td>

Generate datetime literals in ANSI SQL formatter

</td><td>

Currently, the ISO format is used \(YYYY-MM-DDTHH:MM:SS\). Ansi SQL wants a space rather than a T \(YYYY-MM-DD HH:MM:SS\). This becomes relevant because Trino strictly only accepts ANSI format.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1922630

</td><td>

A graph query including a Workflow Data Fabric table isn't routed to Trino

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1924034

</td><td>

getForTables on KG Global Graph aren't returning the edges created via a saveEdge API call

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1924194

</td><td>

Don't strip a timestamp when converting to an ANSI date format

</td><td>

After the last changes, the TIMESTAMP was lost during the timestamp conversion.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1924601

</td><td>

Ignore date literals when converting ISO timestamps

</td><td>

Currently, JSQlParser converts both DATE and TIMESTAMP into DateTimeLiteral objects. It's necessary to ignore the DATE strings when doing conversions rather than flagging them as incompatible formats.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1926994

</td><td>

Data access for a parent epic in Workflow Data Fabric

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1929610

</td><td>

Cypher with a WDF and physical table isn't working

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Impersonate a user.
3.  Ask the query, 'last bonus and department of Abel Tuter'.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1867090

</td><td>

Tables available in the Unreferenced Table Cleaner \(URC\) rule creation form are unconstrained

</td><td>

Configure an inclusion list for available table names when creating new URC rule, and create a new glide property 'glide.db.unreferenced\_record\_cleaner.enabled\_tables'.

</td><td>

Attempt to create a URC rule.

 Expected behavior: Only a subset of tables should be available.

 Actual behavior: All tables are available.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1891527

</td><td>

Workflows aren't properly evaluating conditions to determine if tasks should fire

</td><td>

Filter conditions work differently between Xanadu and Yokohama instances.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1893555

</td><td>

The current implementation of the 'Physical Table Group Populate' job retrieves data only for the 'Day' sample period type, for the past 30 days

</td><td>

This job should also retrieve data for 'Month' and 'Year' sample period types.

</td><td>

1.  Log in to the instance.
2.  Navigate to sys\_trigger.LIST.
3.  Search with the 'Physical Table Group Populator' job.
4.  Select **Execute now**.

 Expected behavior: Data us collected for the sample period type 'Year' and 'Month' for the table sys\_physical\_table\_stats.

 Actual behavior: Data is created only for the sample period type 'Day' .

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1894152

</td><td>

The Data Management Console doesn't display the rotated tables

</td><td>

The Data Management Console should display the rotated tables to follow the TPC hierarchy. The rotated tables should be clubbed and the child tables' stats should be calculated for the TPC hierarchy.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1903967

</td><td>

Queries timing out interrupts the execution of StatsGatherer

</td><td>

If a long-running query times out during a StatsGatherer run, the execution is interrupted and StatsGatherer doesn't continue to the next table stats collection.

</td><td>

1.  Load an instance with rotation / sharded tables.
2.  Decrease the sys\_quota limit for queries to one second to force the queries to time out quickly.

 Expected behavior: Queries that time out are logged. StatsGatherer continues with the next table stats collection.

 Actual behavior: When queries time out, StatsGatherer doesn't continue to the next table stats collection.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1904961

 [KB2328103](https://hi.service-now.com/kb_view.do?sysparm_article=KB2328103)

</td><td>

DB compaction fails when there's a table with more than the MAX\_INT number of rows

</td><td>

A user has a sys\_audit table that has almost 8 billion rows. The query that fetches the size of tables parses out the number of rows as integer, which causes this error. There isn't a way to prevent it from reading the results for certain tables: '...worker.2 worker.2 txid=9f2eff89c30a CompactionQualificationJob SEVERE \*\*\* ERROR \*\*\* Compaction qualification failed java.sql.SQLException: Out of range value for column 'table\_rows' : value 7854795901 is not in class java.lang.Integer range...'.

</td><td>

1.  Insert more than the largest value of a Java integer number of rows into a table.
2.  Run the 'DB compaction' job.
3.  Check that the job completes.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1860663

</td><td>

An index is created without a size limit for some unbounded fields, which leads to errors while creating an index or adding data

</td><td>

The 'AWS Service Catalog Connector' \( x\_126749\_aws\_sc\) installation is left with an invalid index in the 'Task' table in RaptorDB. There's an error: 'SEVERE \*\*\* ERROR \*\*\* Exception executing deferred indexes for class: task...'

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1866261

</td><td>

DB utilization isn't updated if pool throttler isn't enabled

</td><td>

 

</td><td>

1.  Make sure that glide.db.pool.throttler.resource\_usage\_levels.glide is not specified in any property file and sys\_properties.
2.  Open stats.do.

 Observe that the 'DB Resource Usage' percentage for the Glide pool always shows zero.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1878859

</td><td>

The Muninn and Connectors image versions aren't shown

</td><td>

The Muninn version and the Connectors image version from reservation API aren't shown in xmlstats.do?include=database.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1888694

</td><td>

Send 'ClientTags' client info for each query execution

</td><td>

Glide sends information about a query so that Trino can assign the computing resources accordingly.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1891901

</td><td>

Log catalog names being requested during refresh/reservation

</td><td>

During a refresh, the catalogs requested can't be identified. When persistence refreshes the data fabric engine, the names of the catalogs being requested should be logged. For example, QE shows a 'Catalog not found' error during query, and there are no catalog initialization errors during reservation, so the user won't know whether the catalog was requested during the reservation.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1891911

</td><td>

Exclude data fabric-related tables from re-write and routing

</td><td>

Queries against the tables will be \_eligible\_to be routed to read-replica if dynamic routing is enabled and checkpoints are validated. If the query category is explicitly set and read-replica is within the threshold, the query will be \_eligible\_ to be routed to read-replica.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1891912

</td><td>

Use OAuth token and nonce only for queries that need the loopback connector

</td><td>

OAuth access token is only applied for trino queries that need the loopback connector \(for example, datafabric table joins with local Glide table\). Nonce is only applied for trino queries that need the loopback connector \(for example, datafabric table joins with local Glide table\).

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1891913

</td><td>

Reduce the number of 'SELECT 1' queries to trino

</td><td>

For any APIs that use DataFabricEngineManager\#getValidatedDBI, a 'SELECT 1' query is being executed to get a 'validated' DBI. For example, the DataFabricEngingService\#getSchemas API uses DataFabricEngineManager\#getValidatedDBI.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1904021

</td><td>

The oauth token isn't stored per transaction, resulting in increased DB operations

</td><td>

When the user loads a list view, it executes at least two trino queries \(count and data\). At least two DB operations are related to the token grant. Instead, there should be one insert and one update, and the update should extend the token's expiry.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1918929

</td><td>

A primary DB pool is initialized before the DB layer has completed all of its prechecks

</td><td>

There was a change introduced which changed the way to resolve table alias. This method is called during Glide init, where its doing prechecks for the DB. However, because of the change, it ends up initializing the primary pool, even before all the DB layer checks are completed.

</td><td>

Start Glide, as it happens with every Glide start up.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1919500

</td><td>

It takes a long time to recognize the 'DB is down' event

</td><td>

This applies to both PG and MariaDB when the primary database is brought down unexpectedly.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1921155

</td><td>

TableThrottler is broken

</td><td>

TableThrottler is broken due to the removal of lastLag and lastSleepFactor.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1924142

</td><td>

There's a log, 'WARN', based on the property in DBAction\#should UseGateway AwareDBI

</td><td>

The logs are flooded unnecessarily.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1925421

</td><td>

ServiceIdentity records are missing for RaptorDB

</td><td>

All services in the instance topology need to have ServiceIdentity records to turn on some authentication between services.

</td><td>

Zboot any instance.

 Observe there's no records in ServiceIdentity or ServiceOld tables for RaptorDB, unlike other DB services.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1929305

</td><td>

An acceptable table name for DB isn't used when fetching in-place updatable fields in Glide

</td><td>

There's an error. An example includes: 'com.glide.db.GlideSQLException: FAILED TRYING TO EXECUTE ON CONNECTION glide.2 \(connpid=10848\): SELECT attname, attoptions FROM pg\_attribute WHERE attrelid = 'proposed\_change\_verification\_ log'::regclass AND attoptions @&gt; ARRAY\[ 'in\_place\_update=true'\] /\* node-a, gs:glide.scheduler.worker.burst.0, tx:4ddaf200ff232 2109178ffffffffff6e \*/ Syntax Error or Access Rule Violation detected by database \(ERROR: relation 'proposed\_change\_ verification\_log' does not exist.'

</td><td>

Use the method DBInPlace UpdateUtils \#getEnabledInPlace UpdateFields with a table name that is longer than 30 characters.

 This results in an exception that indicates the table doesn't exist.

</td></tr><tr><td>

Database Persistence

 PRB1904837

</td><td>

'Group By' performance is &gt;30 seconds on foreign data connectors

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB1900435

</td><td>

An extra query to trino from worker occurs on the Core UI form opening in Windows Foundation Driver \(WDF\)

</td><td>

The query coming from schedule.worker is unusual and may cause huge data amounts received in some cases.

</td><td>

1.  Configure WDF connection.
2.  Map a table.
3.  Open the form view of the table.
4.  Open the Trino UI dashboard \(/datafabric\_dashboard/ui/index.html\).

 Observe the three calls that are happening; two as a part of the UI transaction, one from schedule.worker.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1929116

</td><td>

OAuth access token error occurs when data is fetched from a remote table to a physical table

</td><td>

The query tries to access a property from a remote table to physical table. The cypher is throws the error, 'OAuth access token is required for loopback connector type.'

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1903736

</td><td>

Column mapping page appears blank for some tables while using the local SN connector

</td><td>

This issue occurs only on certain tables.

</td><td>

1.  Navigate to **Windows Driver Foundation UI Hub** &gt; **Established Connections** **ServiceNow local instance**.
2.  Search for sn\_access\_analyzer\_request.
3.  Select **Create Data fabric table**.
4.  Add a label.
5.  Select **Continue**.

 Expected behavior: Column mapping should display.

 Actual behavior: A blank page is displayed.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1905781

</td><td>

The connection details page displays an 'invalid JSON parse error'

</td><td>

The connection details page displays an 'invalid JSON parse error' when the glide.ui.i18n\_test system property \(MSG: translations\) is enabled.

</td><td>

1.  Navigate to sys\_properties.list on a Zurich instance.
2.  Locate the glide.ui.i18n\_test property and set its value to true.
3.  Open an existing, established connection record.

 Expected behavior: The connection details page should load correctly without any JSON parse errors, regardless of the glide.ui.i18n\_test property's setting.

 Actual behavior: The connection details page displays an 'invalid JSON parse error.'

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1920491

</td><td>

df\_log entries for exceptions sometimes don't have any log category specified and an event isn't fired

</td><td>

There may be exceptions that are thrown in the normal operation of configuring or operating Workflow Data Fabric \(WDF\) tables and sources and these exceptions are expected to be logged into the 'df\_log' table. The WDF error logging framework is designed to translate these types of exceptions to some well-defined log category values. In some cases, this isn't happening. Additionally, when errors are thrown and a log category is known, a sysevent is fired so other components in WDF can react to the problems. This makes it harder for WDF admins to know what the problem is when they are looking at the 'df\_log' table and also prevents some actions where they would be able to solve the problem by themselves without support assistance.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1923285

</td><td>

Users can't create reference on columns of the type 'Int/BigInt' from DataBricks

</td><td>

DataBricks integer columns are mapped as 'BIGINT' in Trino and eventually 'Long' in ServiceNow tables. When users try to change one of the column mapping to a reference to another DataBricks DF Table reference key of type 'Long', it throws the error 'Reference column 'c\_nationkey' mapped to remote column 'c\_nationkey' is using type longint which is not supported for reference columns'.

</td><td>

1.  Create a DataBricks Connection and 2 DF tables \(Customers and Nations\).
2.  On a user's table, select 'nation key' columns as a reference.
3.  Try to select **Finish**.

 It throws an error: 'Reference column 'c\_nationkey' mapped to remote column 'c\_nationkey' is using type longint which is not supported for reference columns'.

</td></tr><tr><td>

Data Visualizations

 PRB1896818

</td><td>

The X-axis values of the 'Featured Metric' graphs display with seconds instead of numeric values

</td><td>

For all the metrics connectors, the X-axis values of the 'Featured Metric' graphs display with seconds instead of numeric values. This also occurs for ACC-M after an upgrade from Xanadu to Zurich.

</td><td>

1.  On a Xanadu instance, navigate to the 'Connector Instances List' page.
2.  Select **New**.
3.  Create connector instances of Zabbix metrics, Nagios metrics and Solarwinds metrics with the required details.
4.  Activate the connector instance.
5.  Navigate to 'Metric to CI' and verify that the Metric CI records of the particular source is created.
6.  Navigate to **SOW** &gt; **List** &gt; **CMDB** &gt; **Servers**.
7.  Open the relevant CI and check the featured metrics graph and the values.
8.  Upgrade to the latest Zurich version.
9.  Repeat steps five through seven.

 Observe that the X-axis values of the 'Featured Metric' graphs display with seconds instead of numeric values.

</td></tr><tr><td>

Declarative Actions

 PRB1908370

</td><td>

Form layout item UI updates aren't applied at runtime unless it's added to a specific layout

</td><td>

 

</td><td>

1.  Create a form action.
2.  Enable the action for all configurable experiences = true.
3.  Open the layout item that has been created.
4.  Update something.
5.  Open a 'Workspace' form.

Observe that none of the form layout item changes are applied or appearing.

6.  Add the form layout item to a form layout.

 Observe that the changes now appear.

</td></tr><tr><td>

Declarative Actions

 PRB1914488

</td><td>

The ai-sparkle-icon doesn't animate when 'animate icon' is set to 'true'

</td><td>

This issue also occurs when setting it on the **Split** button, Related list actions, field decorator, layout items, and m2m layout items.

</td><td>

1.  Navigate to a List Declarative Action.
2.  Set the **Icon** field to 'ai-sparkle-fill'.
3.  Notice the **Animate icon** checkbox appearing.
4.  Check the checkbox.
5.  Navigate to a list.

 Notice that the AI sparkle icon is present but doesn't animate.

</td></tr><tr><td>

Developer Sandboxes

 PRB1921161

</td><td>

Three tabs open after selecting a sandbox in the sandbox list

</td><td>

It looks like there were left over UI Builder generated events in the sandbox management home page macroponent that weren't cleaned. Those extra events should be deleted.

</td><td>

1.  Enable sandboxes.
2.  Navigate to the sandbox management home page.
3.  Create a sandbox if one does not already exist.
4.  Wait for the sandbox creation to finish.
5.  Select the sandbox name.

 Notice that three tabs open in the browser.

</td></tr><tr><td>

DevOps \(Family\)

 PRB1920798

</td><td>

Updating the sn\_devops.table\_ auto\_archive\_duration system property doesn't update all archive rules as there are some in other scopes

</td><td>

 

</td><td>

1.  Navigate to sys\_properties.
2.  Update sn\_devops.table\_ auto\_archive\_duration to another number \(something to test with\).

 Observe that only tables with the DevOps Data Model scope are available for archival.

</td></tr><tr><td>

Discovery

 PRB1901392

</td><td>

The error suggestions for some codes are insufficient or missing

</td><td>

Related errors: '2025-06-04 01:21:18: Exception occurred while executing operation Cloud REST Query. Custom operation Failed to run script due to the following error: JAVASCRIPT\_CODE \_FAILURE: com.snc.sw.exception. CommandFailureException: Cloud authorization failed.' 'Check access rights and proper permissions for requested resource...Status: 403 ErrorCode: PERMISSION\_DENIED Response: Permission 'resourcemanager .projects.get' denied on resource...'

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1909689

 [KB2411091](https://hi.service-now.com/kb_view.do?sysparm_article=KB2411091)

</td><td>

A pattern step fails intermittently due to the 'runCommand' being null

</td><td>

When running a Discovery schedule, the execution of the pattern 'Linux Server' sometimes fails on step '1.1 Get system info' where it runs 'uname -a'. The error generated is: 'Exception occurred. . Cannot invoke 'com.snc.sw. commands. RunCommand.exec \(com.snc.sw. context. ExecutionContext, boolean, String, com.snc.sw.kb. lang.commands. ExecutionMode, String\)' because 'runCommand' is null.' This results in the OS Version attribute on the Linux servers not being populated. The issue is only triggered intermittently and only on a Discovery schedule.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1915814

</td><td>

The user can't discover member accounts in SSM

</td><td>

The user can't discover the VMs associated with a member account via SSM. Instead, the user only discovers management account VMs.

</td><td>

1.  Add AWS credentials for a management account in the Credentials table.
2.  Make sure this account contains member accounts.
3.  Run the AWS SSM VM schedule associated with this management.

 Expected behavior: The user discovers the VMs associated with the member accounts via SSM.

 Actual behavior: The user only discovers management account VMs.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1876011

</td><td>

Conversation hangs after a topic is selected

</td><td>

In the syslogs related to DocIntel, scheduled job errors occur.

</td><td>

1.  Navigate to the Employee Service Center.
2.  Enter the prompt, 'I need to borrow a loaner laptop for work by tomorrow'.

 Notice that the topic will be selected, and 'Starting 'Loaner Laptop'...' is displayed, but then gets stuck.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1896682

</td><td>

Create a system property for max page and max field limits for GenAI use cases

</td><td>

Currently, the max page and max field limits are not customizable.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1898239

</td><td>

extractData fails to extract text from a CSV file due to an invalid character delimiter issue

</td><td>

Error: 'An unexpected error occurred while processing CSV file: IOException reading next record: java.io.IOException: \(line 1\) invalid char between encapsulated token and delimiter: java.lang.IllegalStateException: IOException reading next record: java.io.IOException: \(line 1\) invalid char between encapsulated token and delimiter...'.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1902104

</td><td>

Some of the documents aren't processed under GenAI Docintel

</td><td>

Some documents remain in the 'Setup' status and don't get processed. When attempting to create different extraction use cases, the messages 'There no fields defined for this task' or 'The document is being prepared for display' occur, and a recursive business rule is triggered. In some documents cases, the issue resolves upon refreshing the page, but this is not consistent.

</td><td>

1.  Open Skill under Now Assist.
2.  Navigate to **Platform** &gt; **Document Extraction**.
3.  Create a use case with 15 fields.
4.  Process the task with documents.

 Observe that some documents remain in the 'Setup' status and are not being processed, even after an extended period of time.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1905005

</td><td>

Use the system property max\_number\_of \_task\_images for QnA and extraction on Glide to filter documents

</td><td>

This is a product update

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1916124

</td><td>

Check for the 'Attachment' filter in callPredictionProcess

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1916127

</td><td>

Add text-only mode

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1916128

</td><td>

Extracting user edit fields for text-only mode and classifying as a scanned page for multimodal mode

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1916129

</td><td>

Implement functionality in the Glide/GenAI-App codebases

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1916130

</td><td>

Implementation optimizations

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1916132

</td><td>

Testing with all 3P models

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1916133

</td><td>

PPT document type support for text extraction

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1916136

</td><td>

Remove the OCR, PDF Nagini flow for Docintel GenAI use cases

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1916138

</td><td>

Add Excel/CSV file support for DocIntel GenAI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1919853

</td><td>

Issue with system properties not parsing numbers 0.1 vs 0,1

</td><td>

When an instance is set up with European formatting, such as the decimal being written 0,5 as opposed to the US format of 0.5, the system properties for the threshold values aren't parsed properly, returning an error.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1923569

</td><td>

A flow creates duplicate records in IT Asset Management \(ITAM\) target tables

</td><td>

An extracted table displays 3 rows but the flow ends up creating 6 rows in the ITAM table.

</td><td>

 

</td></tr><tr><td>

Dynamic Schema

 PRB1909876

</td><td>

The **DynamicAttribute Store** field must display and save JSON storage values in form and list views

</td><td>

When loading a record that contains a Dynamic Attribute Store column, the attribute values displayed in the list and form views must be 'Storage values'. By default, these are 'display values'.

</td><td>

 

</td></tr><tr><td>

Edge Encryption

 PRB1915259

</td><td>

Users are unable to attach a 10MB file to a record when logged in with an Edge URL

</td><td>

When logged in with the Edge URL and trying to attach an attachment of 10MB to any of the records in the instance, it keeps loading. But when users load attachments with less than 10MB, it works fine. However, with a normal instance URL, the user is able to attach the larger attachments without any issues.

</td><td>

 

</td></tr><tr><td>

Email Interaction for CSM

 PRB1915830

</td><td>

The inbound action 'Update work order' doesn't get triggered

</td><td>

When receiving mail, the inbound action 'Update work order' doesn't get triggered. The action 'Create an email interaction' gets triggered first, and it has the 'Stop processing' option enabled. As a result, the content of the mail sent from an external user isn't updated in the work order task.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1912370

</td><td>

A citation source link isn't working in the UI16 view

</td><td>

 

</td><td>

1.  Log in as an admin.
2.  Open the sn\_customerservice\_case list.
3.  Open CS0001006.
4.  Open an email client in UI16.
5.  Use the ERR skill.
6.  Select the KB citation link in sources/using the citation reference number.

 Observe that the citation source link isn't working. It's not redirecting to the source KB article.

</td></tr><tr><td>

Employee Center

 PRB1890562

</td><td>

Repetitive subtopics are appear in the Subtopic widget

</td><td>

This issue occurs in the Now Mobile app.

</td><td>

 

</td></tr><tr><td>

Employee Experience Framework

 PRB1918767

</td><td>

Update the Zurich file for Webviews

</td><td>

The window.snmCabrillo .isLoggedIn\(\) method is missing in the SP bundle for now-mobile-webiews, which is trued-up to Zurich. This can be verified using the console on chrome dev tools.

</td><td>

 

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB1894626

</td><td>

Repetitive subtopics display in a subtopic widget

</td><td>

 

</td><td>

1.  Log in as an admin.
2.  Configure more than 25 subtopics to any topic.
3.  Log in to the Now Mobile app.

 Observe that the subtopics are repetitive.

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB1909669

</td><td>

Uptake the AI Search EVAM bundle changes for Employee Centre Pro for Web Applications

</td><td>

With this change the following are expected: 1. The image duplication shouldn't be visible for search entries, so no image should be displayed on the left side as thumbnail. 2. Icons would be introduced for category results.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1891871

</td><td>

em\_events with the Resolution state 'Closing' aren't processed correctly during the CEST clock change window

</td><td>

em\_events with the Resolution state set to 'Closing' aren't processed correctly when their timestamp falls during the CEST clock change window. This results in the alert remaining open even though the closing event is received.

</td><td>

 

</td></tr><tr><td>

Experimentation Platform

 PRB1914754

</td><td>

The client captures data from the previous \(inactive\) experiment instead of the currently active one

</td><td>

The user can complete or cancel an experiment, then activate a new experiment with the same definition ID. However, the framework continues to collect telemetry from the associated usage metrics with the context of the inactive experiment. As a result, stale data is recorded and the exp\_variant bucket in the sample map reflects the inactive experiment's variant value. Instead, the client should reflect the latest active experiment linked to a definition, and it should record variant data accordingly after downloading the latest configuration.

</td><td>

 

</td></tr><tr><td>

Experimentation Platform

 PRB1921476

</td><td>

Notification for new experiments don't appear

</td><td>

Once experiments are downloaded to the instance, they begin executing without Admin awareness.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1855808

</td><td>

Callback is not invoked due to null pointer in FlowCallBack Executor

</td><td>

When an evaluation run from skill kit app is triggered, an attached error log occurred for a particular flow completion, and the run was not marked as complete.

</td><td>

Trigger an evaluation run from skill kit with many data set records.

 Notice that an attached error log occurs in the instance.

</td></tr><tr><td>

Flow Engine

 PRB1893452

</td><td>

AI Agent context isn't properly configured for quick flows

</td><td>

 

</td><td>

Update FlowUserAgentContextIT.java to accurately count the audit.

 Expected behavior: Quick flow tests in FlowUserAgentContextIT pass.

 Actual behavior: Quick flow tests in FlowUserAgentContextIT are failing.

</td></tr><tr><td>

Flow Engine

 PRB1903013

 [KB2218721](https://hi.service-now.com/kb_view.do?sysparm_article=KB2218721)

</td><td>

A flow execution step that calls a Now Assist skill kit is failing because it's sending back 'null' as the response from the skill kit

</td><td>

Now Assist's skill kit that calls flows using dynamic input fails to convert in the expected format in Flow Designer if special characters, like a carriage return, are part of the input.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1903784

</td><td>

process\_flow.engine related zboot errors in the database dump logs

</td><td>

Errors in the database dump logs from Now Assist.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1905152

</td><td>

The 'Make a decision' flow with invalid reference records in a 'Decision' table fails to execute

</td><td>

When a decision logic flow has no branches \(empty flowBlock\), it attempts to create a JumpInstruction with empty targets. During execution, this causes a runtime error in the CursorUpdater when it tries to split the cursor.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1910437

</td><td>

Add a script for GenAI app BUs to create flow and action ACLs

</td><td>

A script utility was removed from the Flow AI Access Control effort that would create the flow or flow\_action access control rule. That utility has been readded.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1916146

</td><td>

Callbacks invoked on the FD API in Async Quick and from an AI agent shouldn't run as 'system'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flow Generation \(Family\)

 PRB1877814

</td><td>

The short description isn't produced when users create a flow with Now Assist

</td><td>

 

</td><td>

1.  Open an instance.
2.  Impersonate a GenAI user with NAC.
3.  Navigate to Workflow Studio.
4.  Select **New** &gt; **Flow**.
5.  Select the 'Build with Now Assist' tab.
6.  Create a flow using the prompt 'Create a flow that is triggered everyday at 4 am and that creates an incident with a short description set to URGENT.'
7.  Navigate to the builder page.

 Observe that the short description is not set to 'URGENT.'

</td></tr><tr><td>

Flow Generation \(Family\)

 PRB1915407

</td><td>

The Now Assist flow builder bypasses system rules

</td><td>

It's not possible for the user to create a manual flow with a trigger on the 'sys\_update\_set' table. This is because of the system property 'glide.ui.permitted\_table.' However, the user can use the Now Assist flower builder to automate the creation of the flow without any challenges.

</td><td>

1.  Navigate to the Flow Designer.
2.  Create a flow.
3.  Use the Now Assist flow builder to generate a flow in which the trigger is the update of a record on the sys\_update\_set table and the state changes to complete.

 Observe that the AI generates the flow trigger on a table that should not be available.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1850039

</td><td>

Code-related text is appearing in the natural language summary for the 'Look up records' action

</td><td>

 

</td><td>

1.  Navigate to Workflow Studio with the latest changes.
2.  Navigate to **Create flow** &gt; **Build with Now Assist**.
3.  Use the prompt, 'Find all the logged issues yesterday, also if you find any \#Problem, report the same to manager through email'.
4.  Verify 'Look up records' while the response is being generated.

 Notice there is a text present saying, 'logged\_ON\_Yesterday@javascript::gs:beginning....'.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1871518

</td><td>

In the Natural language view, the table's internal name shows up for 'Create Task' \(table problem\_task\)

</td><td>

'Create Task' is displayed as 'Create problem\_task Task'.

</td><td>

1.  Create a flow with Now Assist.
2.  Use the prompt, 'Create a flow that runs every day at midnight, and then find all the newly created problem records for the past day'.
3.  Iterate over them.
    1.  If they are not assigned, assign the problem to the level 1 triage group.
        1.  Move the state to 'triaged'.
        2.  Send a notification to the group.
    2.  If they are assigned, assign multiple records to the level 2 triage group.
        1.  Create a task for each record.
        2.  Wait for the task to be assigned.
        3.  Ask for approval from the manager of the task assignee once the task is assigned.

 Notice that the flow is created in preview, and 'Create Task' is displayed as 'Create problem\_task Task'.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1898848

</td><td>

Duplicate entries of the same flow are populated in the flow versions table when flow generation stops

</td><td>

A flow history entry should be created when the flow is created using AI.

</td><td>

1.  Impersonate any user with Flow Designer and Now Assist creator.
2.  Navigate to the **Workflow studio**.
3.  Select **New Flow/Subflow**.
4.  Use any try example.
5.  Select **Generate Preview**.
6.  Select **Stop generation** after one or two components are populated while the flow is being generated.
7.  Select **Save and edit**.
8.  Navigate to **sys\_hub\_flow\_version** once the user is in **Flow Designer** button.

 Notice that there are two records with identical flow sysId names; one record with the 'Updated' as the flow type value, which is meant for base instance flows. There should be only one record with the 'Generated' value for the respective column.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1902025

</td><td>

The subflows are partially generated for the first two example prompts for the subflow

</td><td>

The populate subflow inputs and outputs fail with a code 500.

</td><td>

1.  Create a subflow using the first and second try example.
2.  Use the following prompts:
    1.  'Create a subflow to create a Flow launcher job using the given job configuration sys id and workload generator parameters. If the job sys id is not empty, assign it as the job exec id subflow output. Start the flow launcher for the created job sys id and assign subflow outputs.'
    2.  'Create a subflow that logs the name of the problem input, and then check if the last updated by person is the same as the assigned to. Output the result from the subflow output.'

 Observe that the skeleton is generated, but the first call for the populate subflow inputs and outputs fails.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1918469

</td><td>

There's error checking availability for a flow recommendations skill

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1921327

</td><td>

LLM one-extend secure changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1921403

</td><td>

Tools \(actions/subflow\) do not honor ACLs/Roles if the Agent ACL is successfully validated

</td><td>

When a tool inside AI agent is executed with certain roles and its internal\_name does not match the display name, it does not honor the ACL/role and proceeds with execution.

</td><td>

1.  Create an Agent.
2.  Add a tool, such as an action with an internal\_name that is different the display name.
3.  Create an ACL for that tool with an internal\_name and a dedicated role.
4.  Execute the agent for a user who does not have the required role.

 Notice that the tool works even though it shouldn't.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1922279

</td><td>

Glide changes for Text2flow

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1922818

</td><td>

Customer Service Spoke flows are missing an internal name

</td><td>

Most of the Customer Service Spoke flows don't have internal names.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1923788

</td><td>

Activating plugin and corrupted flow plugin converts to a corrupted flow when added to a flow

</td><td>

 

</td><td>

1.  Navigate to WorkFlow Studio.
2.  Create a new Flow/Subflow.
3.  Add the Activate Plugin and/or Rollback Plugin subflows.

 Expected behavior: Subflows are added successfully to the flow.

 Actual behavior: Subflows convert to a Corrupted Flow when added.

</td></tr><tr><td>

Form Controller

 PRB1905183

</td><td>

Add support for RELATED\_LIST \_FECTCH\_COMPLETED event from Form

</td><td>

The 'Related records' tab assumes that data is available and begins internal page processing while data is still being fetched, resulting in erroneous behavior.

</td><td>

1.  On a Zurich instance, open SOW in UI Builder and navigate to the SRP record page.
2.  Set 'Skiprelated list evaluation' to true in Form controller and make the appropriate changes to the client scripts.
3.  On Runtime of SOW, open any INC record.
4.  In the INC overview tab Impact section, select any Affected CI or Impacted Service card to bring up the **View All** button at the bottom of the section.
5.  Select **View all**
6.  Let focus shift to the Related Records tab.

 Expected behavior: The tab selected on related records should be the list from where the **View All** button was selected on INC overview tab.

 Actual behavior: The tab selected on related records is the first list.

</td></tr><tr><td>

Form Templates

 PRB1909599

 [KB2479828](https://hi.service-now.com/kb_view.do?sysparm_article=KB2479828)

</td><td>

Templates are not updated

</td><td>

The Additional comments section is not filled in even though the Work Notes are filled in. The use of special characters for 'greater than' or 'less than' in the template code, specifically in the resolution notes section, causes the template code to break and the resolution notes to not be displayed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Glide Server APIs

 PRB1921133

</td><td>

Users can't query guest voice agents due to a lack of impersonation ability in a scoped app

</td><td>

The AI Voice agent application makes a call to a platform API to retrieve guest or public voice agents. These are agents that return basic public data such as company hours, location, etc. These agents have an ACL for a guest user. However, the integration user can't impersonate a guest since the app isn't in a global scope.

</td><td>

Call into the voice agent app.

 Notice in the orchestrator that the public agents aren't queried correctly.

</td></tr><tr><td>

Health and Safety Core

 PRB1924486

</td><td>

There's an l10n warning against retrue-up

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Health and Safety Incident Management

 PRB1916809

 [KB2324070](https://hi.service-now.com/kb_view.do?sysparm_article=KB2324070)

</td><td>

The Injury illness 'Create' page is blank

</td><td>

This issue was observed in Zurich, but works in previous families.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Health and Safety Risk Management

 PRB1918530

</td><td>

The search function under Hazards in Health and Safety advanced in the Employee Service Center \(ESC\) is not working

</td><td>

This issue occurs for Health and Safety versions v10 and v11.

</td><td>

1.  Navigate to ESC.
2.  Create Health and Safety advanced.
3.  Select **Hazards**.
4.  Input a Hazard name under the search bar.

 Expected behavior: The search function should work as expected under 'Hazards'.

 Actual behavior: A server error appears.

</td></tr><tr><td>

Health and Safety Risk Management

 PRB1921969

</td><td>

Under the Health and Safety Inspection survey result, the question order is incorrectly displayed in the NowAgent app

</td><td>

The question order should be displayed the same as the original survey.

</td><td>

 

</td></tr><tr><td>

Help Center

 PRB1929400

</td><td>

Support dynamic guidance in help center

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1895321

</td><td>

RCAs are generated when triggering the **Generate Plan** button

</td><td>

The issue is applicable from both the platform and HR Agent Workspace.

</td><td>

1.  Provision an instance with the following plugins installed: sn\_hr\_core, sn\_hr\_gen\_ai - 11.0.0, sn\_generative\_ai - 11.1.0, sn\_genai\_platform - 9.1.0, sn\_skill\_builder - 6.0.0-snapshot, sn\_nowassist\_admin - 6.2.6, sn\_aia - 5.1.4 , and sn\_hr\_ai\_agents - 4.0.1-snapshot.
2.  Enable AI search.
3.  Move the HR case to a 'Ready' state.
4.  Verify that the **Generate Plan** button is available.
5.  Select the **Generate Plan** button.

 Expected behavior: RCAs shouldn't be created and the plan should get generated immediately without RCAs.

 Actual behavior: RCAs are generated for all the HR services.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1915169

</td><td>

A seeding topic doesn't disappear post-seeding despite not existing in the topic inspector

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1901076

</td><td>

Generative AI Controller \(GAIC\) fails to handle some streaming responses due to an unexpected format

</td><td>

Not all streaming responses are being returned by GAIC. Upon investigation, the issue was traced to a class in the flow processing code. This component currently supports only SSE or JSON data formats. However, some responses are returned in a different format, which causes the consumer to error out.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1922262

</td><td>

GEMINI tools break handleStream Message

</td><td>

Users see this issue when using GEMINI with the build agent and asking it to write code that contains an '\|\|' OR operator. Users see this error in the logs: 'Exception in GoogleGeminiResponseHandler while reading content from data chunk: Unterminated string at character 620 of...'

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1925160

</td><td>

Move WS Security signing capability to MID in SOAP step

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Investigation Framework

 PRB1909548

</td><td>

The change request 'Checking conflicts' screen loads indefinitely in remedial actions playbook

</td><td>

The 'Checking for conflicts' message appears indefinitely even though the remedial action is successful in the backend.

</td><td>

1.  Set up an investigation tab via ACCF/MECM.
2.  Select any service or process to restart or end from the investigation tab.

Observe that the playbook is loaded in the contextual side panel.

3.  Enter change details such as short description, assignment group, and assigned to.
4.  Select **Schedule**.

 Observe that the 'Checking for conflicts' message appears indefinitely.

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB1916372

</td><td>

A module key rekey job fails for asymmetric keys

</td><td>

 

</td><td>

1.  Navigate to the Crypto module.
2.  Open glide\_usage\_analytics\_token\_signing.
3.  Ensure that the key pair is generated in both instances with the same key alias.
4.  Perform a clone.

 Expected behavior: Users should be able to rekey and deactivate the asymmetric key pair and associated cert if it exists on the sys\_certificate table of the source instance

 Actual behavior: The module key rekey job fails for asymmetric keys.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1927390

</td><td>

An API to get a Public Key associated to the Private Key used for JWT token signing

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1913382

</td><td>

The 'Close' tooltip is hard-coded and untranslated

</td><td>

The 'Close' tool tip is translated on the GenAI Modal popup, however it remains hardcoded in Task Selector, Language Popup, and in the Drafting article dialog.

</td><td>

Scenario 1:

 1.  Create an article from Incident or Case using Agent Flow from UI16.
2.  Select **Create Knowledge**.
3.  Wait for the popup to display.
4.  Notice that the 'Close' tool tip is now translated.
5.  Select **Continue**.
6.  Wait for the language popup to display.
7.  Hover over the cross icon.
8.  Check the untranslated tool tip.
9.  Select **Continue**.
10. Hover over the cross icon on the drafting icon popup.

 Scenario 2:

 1.  Create an Article from Author flow from UI16.
2.  Wait for the popup to display.
3.  Notice that the 'Close' tool tip is now translated.
4.  Select **Continue**.
5.  Wait for the 'Task' selection to display.
6.  Hover over the cross icon.
7.  Check the untranslated tool tip.
8.  Select **Continue**.
9.  Wait for the language popup to display.
10. Hover over the cross icon.
11. Check the untranslated tool tip.
12. Select **Continue**.
13. Hover over the cross icon on drafting icon pop-up.

</td></tr><tr><td>

List Administration

 PRB1888913

</td><td>

The Query field \(filter\) is reset due to modifications of the state from the list, and the URL on the browser address bar is set incorrectly

</td><td>

 

</td><td>

1.  Side load UXR changes.
2.  Open a base instance list.
3.  Open console.
4.  Execute the line.
5.  Navigate to a URL with a custom filter.

</td></tr><tr><td>

List Administration

 PRB1911482

</td><td>

Unable to apply 'Nest by' for an external user for a hierarchical list

</td><td>

There are some plugin and Store app dependencies associated with this issue.

</td><td>

1.  Log in as an admin user.
2.  Navigate to a page.
3.  Configure the Portal Advanced List widget.
4.  Open the instance option for the widget.
5.  Apply the following instance options:
    1.  Table: sn\_install\_base\_sold\_product
    2.  Filter: parent\_sold\_productISEMPTY
    3.  Nest by: Parent Sold Product
6.  Check the Hierarchical for sold product record as an admin user.
7.  Impersonate a user.
8.  Check the widget data.

 Expected behavior: The record's hierarchical list is shown.

 Actual behavior: The record's data is shown as a flat list.

</td></tr><tr><td>

List Administration

 PRB1914557

</td><td>

Changes to filtered lists aren't saved

</td><td>

When the user edits a filtered list, the changes aren't saved temporarily and can't be accessed later from the 'Unified Nav.'

</td><td>

1.  Create a filtered list and make changes to it.
2.  Navigate away from the filtered list.
3.  Returned to the 'Unified Nav' and accesses the filtered list.

 Observe that the list is no longer filtered in the same way.

</td></tr><tr><td>

List Administration

 PRB1915162

</td><td>

List column values have different font sizes in NS-Sonic-Workspace

</td><td>

This slows down users as they have to zoom in on forms. There's difficulty reading, especially in the 'list' view.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1907127

</td><td>

Some related list DA model fields are not available in related list controller

</td><td>

Related list model fields should have their values populated, but they don't.

</td><td>

1.  Open **UI Builder** &gt; **Lists Demo** &gt; **Record list** bundle page.
2.  Configure the list controller as the following:
    1.  Type: Related
    2.  Table: CIs affected \(task\_ci\)
    3.  Related list parent table: Incident
3.  Open the page and inspect the action bar component, now-record-common-uiactionbar.
4.  In the console, type $0.daModel.

 Expected behavior: isParentNewRecord and isParentReadOnly are populated with boolean values.

 Actual behavior: isParentNewRecord and isParentReadOnly are null.

</td></tr><tr><td>

List Filters

 PRB1911228

</td><td>

Assignment group in the list filter not populating correctly

</td><td>

When applying a filter on a list, not all the groups are showing up in the filter condition in the assignment groups.

</td><td>

 

</td></tr><tr><td>

Metric Intelligence \(Family\)

 PRB1921270

</td><td>

Ignite does not support IPv6

</td><td>

Fixing the implementation to support IPv6.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1916650

 [KB2421892](https://hi.service-now.com/kb_view.do?sysparm_article=KB2421892)

</td><td>

Patterns on agent commands are randomly failing with allowlist errors

</td><td>

Collecting MSSQL DB details using ACC discovery fails to fetch DB details with an error message. The exception occurred when executing a command on Agent. The error occurs when processing the adhoc check request: 'command failed due to allow list exclusion: check command denied by the agent allow list. Context: Asset allow list empty, using agent config file allow list.'

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1904246

</td><td>

External content should be supported in standard search results

</td><td>

The user can't see the icon or select the URL without adding an admin.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1909655

</td><td>

External content in standard search results should be supported

</td><td>

The full URL is truncated.

</td><td>

1.  Log in to latest iOS/Android requestor 20.2 app.
2.  Search the home for a question.
3.  Check SharePoint search results.

 Expected behavior: It should redirect the user to a valid URL.

 Actual behavior: External content in standard search results redirects the user to an invalid URL.

</td></tr><tr><td>

Mobile Platform

 PRB1916140

</td><td>

Mobile Now Assist skill kit in product support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1916141

</td><td>

Attachment and external content for standard search results

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1916148

</td><td>

Mobile NASS entry point update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1919819

</td><td>

An error occurs when returning standard search results that don't have attachments associated with them

</td><td>

This problem occurs with iOS and Android requestor 20.2.

</td><td>

1.  Log in as an admin user.
2.  Search for standard search results that don't have attachments associated with them \(for example, iPhone\).

 Expected behavior: Standard search results should return.

 Actual behavior: Error returning standard search results that do not have attachments associated with them.

</td></tr><tr><td>

Model Context Protocol Server

 PRB1923168

</td><td>

Add the 'MCP' scope to glide.services. rest.allowed\_ services to allow the MCP Store app to use sys\_service

</td><td>

glide.services. rest.allowed\_ services is a static list of scopes that can use the sys\_service using ServiceRESTMessage. 'sn\_mcp\_server=mcp-server' should be added to this list. This allows the scope sn\_mcp\_server to access the sys\_service record mcp-server.

</td><td>

From a Store app, call var rm = new sn\_internal\_services.ServiceRESTMessage\('mcp-server'\) and use rm to call the mcp-server exposed REST APIs.

 Excepted behavior: Users are able to call MCP server APIs.

 Actual behavior: Users are unable to call MCP server APIs.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1926908

</td><td>

Both the polaris\_header\_logo theme asset and the coreUILogo image can be requested in a direct load due to a race condition

</td><td>

When getLogoSource is called initially for sn-polaris-header.view.js, the CoreUILogoSrc isn't defined. As a result, it falls back to get the logo from the theme asset. Later on, when the CoreUILogoSrc is defined, the request for loading the corresponding image is sent.

</td><td>

1.  Log in to an HR instance.
2.  Navigate to a record page or homepage.
3.  Notice the following requests:
    1.  theme asset: 0850a525073220105fca5d1aead30038.assetx
    2.  coreUILogo image: ccbd67c4408f4110f8775ad9518199da.iix

 When Next Experience is turned on, only the 2nd image should be requested.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1930430

</td><td>

An additional graphql request from nowAssistUtility has been observed to result in a 300ms slowdown during direct load scenarios

</td><td>

This occurs even when the plugin is not turned on.

</td><td>

 

</td></tr><tr><td>

Next Experience User Menu

 PRB1904194

</td><td>

Filter users of type AI Agents from the 'Impersonate user' list

</td><td>

Disable users from impersonating any user of the identity\_type 'ai\_agents'.

</td><td>

 

</td></tr><tr><td>

Next Experience User Menu

 PRB1926920

 [KB2442915](https://hi.service-now.com/kb_view.do?sysparm_article=KB2442915)

</td><td>

On instances with AI Agents, some users can't be found on the impersonation list

</td><td>

Currently, users with the 'Identity type' field set to 'AI Agent' are filtered out, but they must also be filtered by 'is empty'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Notify

 PRB1893788

</td><td>

The com.snc.notify plugin takes a long time during the Zurich upgrade

</td><td>

During the Yokohama to Zurich upgrade, the com.snc.notify plugin takes a long time \(around 31 minutes\).

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1909094

</td><td>

The **Show more** button isn't visible on NASS for Safari browsers

</td><td>

When using the Now Assist Panel \(NAP\), Now Assist for Virtual Agent \(NAVA\), or Now Assist for Request \(NASS\) on Safari, the **Show more** button isn't visible after truncation, so the user is unable to see the full message. This prevents users from accessing the complete content of responses.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1912777

</td><td>

Citations are not displayed in the Now Assist Panel \(NAP\)

</td><td>

Observe that the citations are not generated after the plan generation.

</td><td>

1.  Navigate to an instance.
2.  Navigate to sn\_aia\_property table.
3.  Create a record with the following details:
    1.  Name: show\_citation
    2.  Value: true
    3.  Target table: sn\_aia\_usecase or sn\_aia\_agent
    4.  Target record: Demo Steps for Incident Resolution or Demo Next Best Action Agent
4.  Execute the use case or the agent in NAP.

 Expected behavior: Citations should be displayed in NAP.

 Actual behavior: Citations are not displayed in NAP.

</td></tr><tr><td>

Now Assist Panel

 PRB1913113

</td><td>

External links on fullfiller Now Assist Panel \(NAP\) lead to 'No records found'

</td><td>

 

</td><td>

1.  Open NAP as user that owns a STRY.
2.  Enter 'what are the seven wonders of the world'.
3.  Open links for Sharepoint under 'Sources'.

 Expected behavior: The link should redirect to a new tab to log in to Sharepoint.

 Actual behavior: The links redirect to 'No records found'.

</td></tr><tr><td>

Now Assist Panel

 PRB1914236

</td><td>

Some channels aren't supported on enhanced chat

</td><td>

These controls aren't supported on all channels: Dynamic Choice, and Script Output.

</td><td>

1.  Configure enhanced chat in **All** &gt; **Conversational Interfaces** &gt; **Assistants**.
2.  Enable data visualization generation skill in **Now Assist Admin** &gt; **Platform**.
3.  Open Now Assist Portal.
4.  Select **Create a data visualization**.

 Expected behavior: Message asking for utterance appears.

 Actual behavior: Channel not supported appears.

</td></tr><tr><td>

Now Assist Panel

 PRB1914534

</td><td>

Other components should be able to request AIEL to execute a skill

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1916147

</td><td>

AI engagement layer initiative

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1929041

</td><td>

SKILL\_EXECUTION \_STARTED passes aiaExecutionPlanId as empty in its payload

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Select the sparkling icon to trigger AIEX.
3.  Keep the debugger at the SKILL\_EXECUTION\_STARTED' action handler.
4.  Trigger the 'Canvas flow' usecase.
5.  Observe that SKILL\_EXECUTION\_STARTED is passing 'aiaExecutionPlanId' as an empty value.

 Expected behavior: The aiaExecutionPlanId payload value should have execution planId of execution.

 Actual behavior: The aiaExecutionPlanId value is empty.

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1912755

</td><td>

Missing inline editing modal for existing ACLs for agentic workflows and agents

</td><td>

 

</td><td>

1.  Open any workflow or agent with an existing ACL from studio.
2.  Select **Role** pills in the 'Roles' column of the ACL listed in the 'Define who can access this agentic workflow' section.
3.  Edit roles in the appearing modal.
4.  Select **Save**.

 Expected behavior: The modal should appear, and roles can be updated and saved.

 Actual behavior: No editing modal appears.

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1913515

</td><td>

'Run As Triggers' at Agent level isn't initiating a conversation in sys\_cs\_conversation table

</td><td>

 

</td><td>

1.  Install AIA 5.1.SNAPSHOT to IT Ticket Status Agent.
2.  Add 'Run As' for any AI user with 'Admin' as a role.
3.  Configure triggers on incident table with Run AS AI User.
4.  Update the incident to initiate a trigger/conversation.

 Notice that 'Trigger Conversation' is not getting initiated.

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1919812

</td><td>

Uptake the security role masking changes on Virtual Agent

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1919813

</td><td>

Changes to accommodate new AIEL and Now Assist Panel configurations

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1919814

</td><td>

Changes to accommodate new AIEL and Now Assist Panel configurations

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1919815

</td><td>

Backend changes to align with sunsetted Now Assist Panel chat component and device type

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1919816

</td><td>

Capture invocation start to sn\_aia\_execution\_plan to determine if it ran from playground, trigger, or chat discovery

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OAuth

 PRB1903564

</td><td>

Unable to save JWT verifier map for CTT

</td><td>

 

</td><td>

1.  Impersonate an oauthadmin user.
2.  Navigate to **Inbound Integrations**.
3.  Create new record for the JWT bearer grant.
4.  Fill in the mandatory fields.
5.  **Save** the record.
6.  Reopen the record created.
7.  Add the JWT verifier map with all the fields filled in.
8.  Select **Save**.

 Observe that a success message shows that it saved, but the field was not updated.

</td></tr><tr><td>

OAuth

 PRB1927389

</td><td>

Support JWT Token format for OAuth access tokens

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1915941

</td><td>

Channels aren't shown in the escalation tracking modal

</td><td>

If the user gives more than ten numbers in custom escalation, the channels aren't shown in the escalation tracking modal.

</td><td>

1.  Log in as an admin user.
2.  Create a shift.
3.  Navigate to cmn\_rota.
4.  Select **Shift**.
5.  Select **Edit escalation and contact Pre**.
6.  Add more than twelve users in step one.
7.  Add one user and one group.
8.  Add 'Contact Pre' as Email, Teams, and Mobile Plus.
9.  Create a trigger rule for the subflow with 'On-Call: Assign by Acknowledgement.'
10. Create an incident.

 Observe that the channels aren't shown in the escalation tracking modal.

</td></tr><tr><td>

On-Call Scheduling

 PRB1917069

</td><td>

The property 'com.snc.notify.use \_subflow\_for\_conference \_escalation' set to true upon upgrading an instance when the user first installs notify and then upgrades

</td><td>

 

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1922005

</td><td>

Even after rejection, a voice call sends another reminder only with a voice device

</td><td>

 

</td><td>

1.  Log in as an admin.
2.  Create a shift.
3.  In a custom escalation, add the user and device in step 1 and the user and device in step 2.
4.  Add a contact pref as 'Email'.
5.  Create a trigger rule with on-call: assign by ack for workflow.
6.  Create an incident.
7.  Press 2 in call.

 It's also sending the second reminder.

</td></tr><tr><td>

On-Call Scheduling

 PRB1925331

</td><td>

In a custom escalation when a user rejects, the notifications for the next attempt for other users aren't waiting for the defined remainder time

</td><td>

 

</td><td>

1.  Log in as an admin.
2.  Create a custom escalation with more than one user at step 1 or either user + device.
3.  Reject via any one user by any channel.

 Issue 1: The other users are getting notifications for the next attempt and aren't waiting for the defined remainder time.

 Issue 2: The timer next to attempts in the tracking model is showing lesser time than the time defined when rejected in the previous step.

</td></tr><tr><td>

OneExtend

 PRB1920363

</td><td>

checkLLMModel Availability returns false when the user's preference language isn't English

</td><td>

Inside checkLLM ModelAvailability compares 'gr.getDisplayValue\('available'\) == 'true'', but gr.getDisplayValue\('available'\) would return a translated word of 'true'.

</td><td>

1.  Call 'checkLLMModelAvailability' in English and see if the result is true.
2.  Switch to a different language.
3.  Call 'checkLLMModelAvailability' again and see if the result is false.

</td></tr><tr><td>

OneExtend

 PRB1920515

</td><td>

LLM usage domain separation application properties aren't installed by default

</td><td>

 

</td><td>

1.  Install the latest OneExtend app.
2.  Add the domain separation plugin.
3.  Verify the sys\_application\_property table.
4.  Look for domain.llm. usage.entitled.

 Notice that the property is missing, even though it's part of the repository.

</td></tr><tr><td>

OneExtend

 PRB1920527

</td><td>

Elaborate or shortened responses load on form skills when the ACL is set to Now Assist Context Menu \(NACM\) skills

</td><td>

This issue was found in Washington DC. Responses that have been elaborated or shortened appear even though they are restricted to a particular role in the NACM ACL table. The NACM skill in the skill configuration table also becomes 'inactive' by default.

</td><td>

1.  Log in to a Washington DC instance.
2.  Ensure Gen AI is setup.
3.  Activate the Resolution Notes generation skill.
4.  Navigate to the ACL table.
5.  Add a role to the NACM ACL, such as workspace\_admin.
6.  Impersonate an ITIL user.
7.  Select the text on close\_notes.
8.  Elaborate or shorten the text on close\_notes.

 Observe that elaborate and shortened responses are loading even when it's restricted to only the workspace\_admin role, and the NACM skill in the skill configuration table is 'inactive' by default.

</td></tr><tr><td>

OneExtend

 PRB1923466

</td><td>

Search isn't working on the latest znowassiststable

</td><td>

There's exceptions: '\#35877 \[SEARCH API\] OrchestratorScriptUtil: Exception thrown when invoking sn\_ais\_assist.Conversation OrchestratorUtil script: org.mozilla.javascript .JavaScriptException: java.lang.NullPointer Exception...'

</td><td>

1.  Set up an instance with latest znowassiststable and store apps.
2.  Search with any utterance on both NAP and NAVA.

</td></tr><tr><td>

OneExtend

 PRB1923618

</td><td>

Heap OutOfMemory error and node restart in an ITSM use case for Agentic AI Benchmark

</td><td>

This issue may be caused by the Agentic AI workload transaction allocating heap memory of over 1G.

</td><td>

1.  Run ITSM Benchmark.
2.  Test the load with 500 users on Now Assist and 150 users on the Agentic AI workload.

</td></tr><tr><td>

OneExtend

 PRB1923685

</td><td>

When executing a couple of Zoom Agents, an IllegalAccess error is thrown

</td><td>

The same issue is observed for the 'Create Meeting' Agent.

</td><td>

1.  Log in to an instance.
2.  Navigate to Virtual Agent UI.
3.  Provide the prompt, 'Please create a user \[user's name\] having an email ID as \[user email address\]. The user should be a basic user only.'

 Expected behavior: A user should be created in Zoom.

 Actual behavior: The message appears, '\{'message':'Invalid inputs for tools execution: JavaException: java.lang.SecurityException: Illegal access to package\_private script include function AIAFdihDataTypeConstants: caller not in scope sn\_aia'\}'.

</td></tr><tr><td>

OneExtend

 PRB1923978

</td><td>

Metrics aren't observed and FSD isn't executed for ASYNC mode

</td><td>

Detector metrics aren't created in the sys\_generative\_ai\_metric\_list table. Also, FSD capabilities aren't executed and don't present in GenAI logs.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1924111

</td><td>

Incident Summarization keeps spinning indefinitely when Regex is detected

</td><td>

An error message should be displayed instead.

</td><td>

1.  Open an instance with the latest znowassiststable and GAIC 11.1.1-SNAPSHOT.
2.  Navigate to **Now Assist Settings** &gt; **Guardian** &gt; **Prompt Injection=Block and Log**.
3.  Add the sys\_prop com. glide.one\_ extend.security \_detector.enabled =true.
4.  Add a record in sys\_gen\_ai\_ detector\_text \_pattern with Type=Full Text match or Regex.
5.  Open an incident.
6.  Modify the content to trigger the regex in step 4.
7.  Summarize the incident.

 Notice that Incident Summarization keeps spinning indefinitely when Regex is detected.

</td></tr><tr><td>

OneExtend

 PRB1925075

</td><td>

Flow Designer retries aren't working with async non-quick mode capability executions

</td><td>

The OneExtend API returns an error without doing the retries.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1926131

</td><td>

Unable to store long-term memory, skill 'LTM Identify memories \(Azure OpenAI C\)' / AIA Identify Episodic Memories throws an error in the log

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1927150

</td><td>

User gets a script error for an execution request

</td><td>

The script execution error: 'Script Identifier: null.null.script, Error Description: java.lang.NullPointerException: Cannot invoke 'String.equalsIgnoreCase \(String\)' because the return value of 'com.glide.one \_extend.resource. dto.v2.MultiCapability ExecutionRequestDto .getMode\(\)' is null, Script ES Level: 0...'

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1928470

</td><td>

Abnormal GAIC async submission duration

</td><td>

When the user calls certain code with an async request, the response time should be around 0-200 milliseconds. However, the response time can be as high as five seconds because the Builder Entity cache frequently gets reclaimed.

</td><td>

1.  Enable logging sn\_ais\_assist. AISearchNA4S GeniusResultLogger .level=INFO.
2.  Run NAVA QnA flow.
3.  Look at the splunk log pattern 'AISearchNA4S GeniusResultLogger response received! duration'.

 Observe that the submission time can reach two to five seconds.

</td></tr><tr><td>

OneExtend

 PRB1929432

</td><td>

Improved accuracy of security detectors by leveraging attributes exclusion list

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1932671

</td><td>

OrchestratorUtil errors out during a platform upgrade

</td><td>

Observe errors: '\#3796 \[SEARCH API\] OrchestratorScriptUtil: Exception thrown when invoking sn\_ais\_assist. ConversationOrchestratorUtil script: org.mozilla. javascript. JavaScriptException: java.lang. NullPointerException: Cannot invoke...'

</td><td>

 

</td></tr><tr><td>

Oracle Reconciliation

 PRB1876511

</td><td>

An install shouldn't be deleted if there are applications pointing to it

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1893690

</td><td>

External users are unable to generate the bar and pie charts on any columns of a table for the first time

</td><td>

This issue occurs only for the first time the user attempts to generate bar and pie chats.

</td><td>

1.  Provision a new TD instance on the latest master.
2.  Log in as an admin.
3.  Install the OCS plugin.
4.  Log in as an external agent.
5.  Select **All** on the cases.
6.  Select the context on any column, such as 'contact'.
7.  Select **Bar chart** or **Pie chart**.

 Expected behavior: The user should be able to generate bar and pie charts.

 Actual behavior: The page keeps loading continuously.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1920884

</td><td>

CIO Dashboard duplication is resulting in failure by the users 'sn\_ciodashboard .ciodashboard\_admin' and 'sn\_ciodashboard. ciodashboard\_user'

</td><td>

Users get the following error in the logs: 'DASHBOARD\_API: Duplicate API - Widget Collision WidgetCollisionException - Colliding Widgets are: Widget....'

</td><td>

1.  Install the CIO app for the instance.
2.  Log in to the instance with either of these roles: sn\_ciodashboard.ciodashboard\_admin or sn\_ciodashboard.ciodashboard\_user.
3.  Try duplicating the dashboard.

 Observe that it is duplicating the dashboard error, but the dashboard is created in the backend with an incorrect UI.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1923076

</td><td>

The 'grouping' feature isn't turned on for all dashboards

</td><td>

The par.dashboard. widget.group. enabled.dashboards. list property should be updated to call CxO dashboard sysIDs, so that grouping is turned on for all CxO dashboards.

</td><td>

Open any CxO dashboard other than the CIO dashboard.

 The grouping feature isn't turned on by default for all dashboards.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1923080

</td><td>

A new dashboard category, C-suite, isn't available in the platform

</td><td>

 

</td><td>

Open the analytics\_category table in an instance.

 Observe that there's no C-suite category present.

</td></tr><tr><td>

Playbook Experience

 PRB1908664

</td><td>

Issues on Incident playbook on Zurich version

</td><td>

Records are replaced.

</td><td>

1.  Log in as OHS Manager and create a new incident on Health and Safety workspace.
2.  Navigate to 'People Involved' tab.
3.  Add a new record under 'People Involved' and select **Save**.
4.  Select another record under 'People Involved' and select **Save**.

 Observe that the section under 'Add persons involved' does not get refreshed after saving until the page is refreshed. Upon adding another person under 'People Involved' and saving, the first record gets replaced instead of adding a new person.

</td></tr><tr><td>

Playbook Experience

 PRB1916406

</td><td>

When a non-PO invoice is converted to a PO invoice, the PO confirmation pop-up is not closed and the user is stuck

</td><td>

 

</td><td>

1.  From the top menu, select **Workspace** &gt; **Source to pay workspace** &gt; **Invoices** &gt; **All invoices** &gt; **New**.
2.  Select.
3.  Select PO invoice from the Type drop-down list in the invoice form.
4.  Fill in all mandatory details and save.
5.  Select the **View Invoice Processing case** button.
6.  From the playbook tab, change the purchase order to something else.
7.  Scroll down and select **Continue**.

 Notice that a warning modal opens but none of the buttons work, including the default cross button.

</td></tr><tr><td>

Playbook Experience

 PRB1920761

</td><td>

The default value of inputForm ControllerFieldItem and inputForm ControllerSections is an '\[\]'

</td><td>

Activity UIs that are making a copy of the default and removing the form bundle get an '\[\]' and it breaks the runtime of the computeFormProperties behavior. This makes DAs not load and other issues could appear.

</td><td>

1.  Open the Playbook Activity UI Controller.
2.  Navigate to the properties for inputFormControllerFieldItem and inputFormControllerSections.

 Expected behavior: Both's defaultValue should be '\[\]' or an empty string.

 Actual behavior: Both are set to the string of '\[\]'.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1916240

</td><td>

Duplicating playbook with permissions referencing an activity does not copy over properly

</td><td>

 

</td><td>

1.  Create a playbook.
2.  Add a stage and create new record \(incident table\).
3.  Fill out a trigger and parent record.
4.  In the playbook permissions tab, reference the activity created.
5.  Duplicate the playbook.

 Observe that the pill errors out.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1917556

 [KB2461528](https://hi.service-now.com/kb_view.do?sysparm_article=KB2461528)

</td><td>

The user observes a 'No Playbook stages available' error in the Playbook tab

</td><td>

When creating an HR Lifecycle Events case with the Center of Excellence \(COE\): HR Lifecycle Events Case, and then moving the case to 'Ready' state, the Playbook tab displays 'No Playbook stages available' instead of showing the expected playbook cards in their respective lanes.

</td><td>

1.  Navigate to HR agent workspace.
2.  Create an LE case with COE: HR Lifecycle Events Case, HR service: New Hire Onboarding.
3.  Move the LE case state to Ready.

 Expected behavior: Playbook cards are to be visible under playbook tab.

 Actual behavior: In Playbook tab, the user is not able to see any playbook cards. It is displaying 'No Playbook stages available' instead of playbook card.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1918168

</td><td>

Record Generator does not enforce runtime permissions

</td><td>

An error should display saying that an action cannot occur, but the action occurs anyway,

</td><td>

1.  Provision an instance with the Playbook Experience Demo plugin installed.
2.  Open **Playbook Designer** &gt; **Playbook Experience Demo**.
3.  Auto-upgrade to schema version 3.
4.  Impersonate a user with access to Playbook Experience Demo workspace but not access to read/create on the interaction table.
5.  Open Workspace: Playbook Experience Demo.
6.  Create a new Interaction.

 Expected behavior: An error message displays saying that the playbook cannot be displayed.

 Actual behavior: Playbook Experience Demo opens.

</td></tr><tr><td>

Playbooks

 PRB1922985

</td><td>

A banner message to install the latest PAD should be displayed on a Playbook Designer page

</td><td>

To inform users to install the latest PAD when the new Now Assist for Platform version is available, there should be a banner message on a Playbook Designer page advising them to upgrade PAD for the Agentic Playbook feature.

</td><td>

1.  Navigate to any instance with the latest Glide build.
2.  Install Workflow Studio.
3.  Launch Workflow Studio.
4.  Open any particular playbook.

 Expected behavior: There's an info banner message to install the latest PAD to get the Agentic Playbook feature.

 Actual behavior: No banner is available.

</td></tr><tr><td>

Predictive Intelligence

 PRB1890514

</td><td>

A 'Feature Importance' tab displays for java classifications

</td><td>

 

</td><td>

1.  Train a classification solution with glide.platform\_ml. api.enable\_ workflow\_classification as 'false'.
2.  Observe that the 'Feature Importance' tab appears even though it's not trained with explainability.

 Expected behavior: The 'Feature Importance' tab shouldn't appear.

 Actual behavior: The 'Feature Importance' tab is appearing.

</td></tr><tr><td>

Predictive Intelligence

 PRB1892456

</td><td>

Workflow predictions fail when the attachment is missing for word vector corpus in the ml\_model\_artifact table

</td><td>

After deleting the attachment created in the word vector record in the ml\_model\_artifact table, the predictions fail with a bad URL and the word corpus artifact is referenced incorrectly.

</td><td>

1.  Set glide.platform\_ml.api.enable\_workflow\_similarity to 'false'.
2.  Create a word corpus record.
3.  Create a similarity definition.
4.  Select the word corpus created in step 2.
5.  Select **Submit and Train**.
6.  Notice that after successful training, the word vector record is created in ml\_model\_artifact table with an attachment.
7.  Perform the predictions.
8.  Ensure the predictions are successful.
9.  Set glide.platform\_ml.api.enable\_workflow\_similarity to 'true'.
10. Delete the attachment from the word vector created in step 5.
11. Re-trigger the training.
12. Perform the predictions after successful training.

 Notice that the predictions fail with a malformed URL, and the workflow predictions are incorrectly referencing the word corpus artifact.

</td></tr><tr><td>

Predictive Intelligence

 PRB1921497

</td><td>

For similarity, an empty column in the 'Test' table causes an error during predictions

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1905387

</td><td>

Addition of Query ACLs in Process Mining

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1912315

</td><td>

Filter set models are calculated on an incorrect number of cases when filter set conditions match more than 10k results

</td><td>

There's issues with filter sets' data upload: 1. Use the correct page size value for fetching filter set case IDs. 2. Add a header line to a filter set file upload for the second page onwards. 3. Avoid a case count query for filter sets' file names to avoid timeouts while the data file name generates for a full mine.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1920054

 [KB2423567](https://hi.service-now.com/kb_view.do?sysparm_article=KB2423567)

</td><td>

Condition with transitions are failing when viewing the 'Schedule task' results

</td><td>

This issue occurs when upgrading from Xanadu to Yokohama.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Process Mining Workspace

 PRB1918498

</td><td>

'Process Configuration' and 'External Data' lists don't show all configurations and external tables on Process Mining Workspace

</td><td>

 

</td><td>

1.  Navigate to the Process Mining Workspace.
2.  Open the 'Process configuration' tab.

 Expected behavior: The scroll must work correctly.

 Actual behavior: If there are many process configurations, notice that there's no pagination option to flip to the next page. Verify this by sorting the list.

</td></tr><tr><td>

Process Mining Workspace

 PRB1921809

</td><td>

Enable auditing on Process Mining config tables

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB1917740

</td><td>

Deprecated legacy workflows are installed on zbooted instances

</td><td>

Several base instance legacy workflows are installed in Zurich.

</td><td>

 

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

 PRB1925925

</td><td>

Users are unable to see the sparkle icon for an email recommendation

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Roles

 PRB1916157

</td><td>

Agent role controls for Identity type

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1916160

</td><td>

Agent role inheritance restriction

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Scheduled Jobs

 PRB1915686

</td><td>

The run\_dayofweek field isn't visible until the trigger type is changed

</td><td>

In the cds\_client\_schedule table, the run\_dayofweek field isn't visible for an entry with a 'Weekly' trigger type. The field only becomes visible when the trigger type is changed, then reverted back to 'Weekly.'

</td><td>

1.  Navigate to the cds\_client\_schedule UI.
2.  Create a schedule entry with the trigger type set to 'Weekly.'

Observe that the **run\_dayofweek** field isn't displayed.

3.  Change the trigger type to a different value \(for example, 'Daily'\).
4.  Change the trigger type back to 'Weekly.'

 Observe that the **run\_dayofweek** field now appears \(for example, 'Day: Monday'\).

</td></tr><tr><td>

Search Application Configurations

 PRB1912254

</td><td>

Performance test results for the E2E backend query show high response results

</td><td>

When the user runs a jmter test for a backend E2E query, the test results show a high response time, with an average of 1065 milliseconds.

</td><td>

 

</td></tr><tr><td>

Security Attributes

 PRB1916143

</td><td>

'Are you an Agent?' security attributes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Security Attributes

 PRB1916145

</td><td>

Default access posture security attribute

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB1897911

</td><td>

In ServiceNow Studio, when creating a catalog item using the AES Standard Items template, the catalog item preview fails to properly honor the dark themes for both Coral and Polaris

</td><td>

This issue also occurs when the user attempts to see the item preview after select 'Preview in new tab'.

</td><td>

1.  Ensure the AES plugin is installed.
2.  Navigate to **Navigation menu** &gt; **ServiceNow Studio** &gt; **Create app**.
3.  Fill in the details.
4.  Create the file.
5.  Enter **sc\_cat\_item** in the search bar.
6.  Select **Catalog item**.
7.  Select **AES Standard Items template**.
8.  Create a catalog item.
9.  Observe the various item previews available for the catalog item in portal, Mobile and Virtual Agent.

 Expected behavior: The item preview should honor the dark theme.

 Actual behavior: The item preview doesn't honor the dark theme for both Polaris and Coral theme.

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1910324

</td><td>

There's a dump error from the catalog in ynowassist

</td><td>

Notice the error: '...glide SYSTEM FailDMTUtil SEVERE \*\*\* ERROR \*\*\* File GLIDE INF/plugins/com. glideapp.servicecatalog .standard\_ticket/update/ sys\_ui\_list\_std\_ ticket\_action\_input\_ model.xml contains a record that will not correctly trigger collision detection. Expected the record to be in a file named sys\_ui\_list\_std\_ticket\_action \_input\_std\_ticket\_config\_ action\_null.xml'.

</td><td>

 

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1911973

</td><td>

Unable to display the 'show more/less' menu for the 'Incident ticket' form

</td><td>

 

</td><td>

1.  Navigate to the standard ticket configuration from the navigation menu.
2.  Open the incident table ticket configuration.
3.  Under 'Info region' tab, mark the **Show description** field as 'Always'.
4.  Mark the **Description** field as 'description/short description'.
5.  Save the changes.
6.  Launch Service Portal.
7.  Search for the 'Create incident' record producer.
8.  Fill in the variables and submit the form.
9.  Observe the ticket details.

 Expected behavior: The incident standard ticket form must show the description along with the 'show more/less' toggle.

 Actual behavior: Despite of the configurations, the 'show more/less' toggle isn't displaying.

</td></tr><tr><td>

Service Catalog

 PRB1916122

</td><td>

The ability for catalog authors to control prefill behavior \(KG, user personalization API, chat history\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

ServiceNow Voice \(Family\)

 PRB1894893

</td><td>

Add an AI Voice Agent service type to libkmf

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Operations Workspace Admin Center

 PRB1904917

</td><td>

Stale versions of SRM team governance files

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1877891

</td><td>

The summary section on the change overview page doesn't support dot-walked fields in read-only mode

</td><td>

 

</td><td>

1.  Modify the 'Summary' section of the 'SOW-Change-Overview' view.
2.  Add a dot-walked field into the view.
3.  Save the view.
4.  Open a change request in SOW.

 Observe that the dot-walked field is not displayed in the 'Summary' section. However, it's correctly displayed when the user edits the form.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1891866

</td><td>

The getRiskActions method of SOWChangeUtils throws an invalid table name exception

</td><td>

An invalid table name error occurs.

</td><td>

1.  Open Scripts - Background.
2.  Execute the code in the sn\_cow\_chg scope.

 Notice the error is displayed, 'Error Description: org.mozilla.javascript.EvaluatorException: GlideRecord.get\(\) - invalid table name'.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1896342

</td><td>

The **Restore** or **Make next agenda item** buttons overlap with the agenda description text

</td><td>

When the user opens a pending CAB meeting and selects an agenda card, the **Restore** or **Make next agenda item** buttons overlap with the agenda description text.

</td><td>

1.  Open a CAB Meeting that's in the pending state.
2.  Select any of the agenda cards.

 Observe that the **Restore** or **Make next agenda item** buttons overlap with the agenda description text.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1898517

</td><td>

Change Requests aren't documented when created from an Incident in Service Operations Workspace \(SOW\)

</td><td>

This issue is observed in Xanadu and in Yokohama.

</td><td>

1.  Impersonate a user.
2.  Select **Create New incident**.
3.  Create a Change \(CHG\) from the Incident \(INC\).
4.  Select **Create normal change**.
5.  Notice that the **RFC** field is updating in the Incident Related list.
6.  Return back to the INC.
7.  Notice that in the backend, the CHG is present in INC.
8.  Log in to SOW as a user without an ITIL role.
9.  Create a new INC.
10. Create a normal CHG from the INC.
11. **Save** it.

 Notice that the CHG Number is not listed in SOW.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1898965

</td><td>

When selecting 'Go to CAB Meeting' on the Service Operations Workspace \(SOW\) Change sidebar, this navigates to the UI16 CAB and not the SOW CAB if it's installed

</td><td>

The property 'com.snc.change.use\_sow \_meeting' should be set to 'true'.

</td><td>

1.  Load SOW and CAB Meeting.
2.  Navigate to a change request that is included in a CAB meeting.
3.  Select **Go to CAB meeting** on the Record Information sidebar.

 Expected behavior: The CAB meeting opens in a new tab within SOW if the property 'com.snc.change.use\_sow\_meeting' is set to 'true'.

 Actual behavior: The UI16 CAB meeting is opened in a new browser tab.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1900249

</td><td>

The **Copy Change** UI action on Service Operations Workspace \(SOW\) doesn't allow copying when a mandatory field is not populated

</td><td>

The **Copy Change** UI action on Service Operations Workspace is not allowing until mandatory fields are updated, when in Native UI, it copies without any blockers. When replicating the same on Native UI, the new change is created and no error message occurs.

</td><td>

1.  Open any change in SOW.
2.  Empty any mandatory field without saving.
3.  Select the **Copy Change** button.

 Expected behavior: A new change should be created.

 Actual behavior: A new change isn't created, and the error is displayed, 'The following mandatory fields are not filled in...'.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1900447

</td><td>

After upgrading to Yokohama and Service Operations Workspace version 7, when creating a CHG from a PRB via SOW, the user is no longer redirected to select a change mode

</td><td>

In a base instance that has SOW v7, and the functionality of a Normal Change Request being created is observed, and there is no option to select a different model.

</td><td>

1.  Open Service Operations Workspace.
2.  Navigate to **Lists** &gt; **Problems** &gt; **Create a new PRB**.
3.  Save the PRB.
4.  Navigate to the 'Fix Tasks' tab.
5.  Select **New**.

 Notice that a new 'normal' change request record is immediately opened.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1908670

 [KB2330510](https://hi.service-now.com/kb_view.do?sysparm_article=KB2330510)

</td><td>

If the 'Standard Change' plugin isn't installed, then the 'Create Change' page doesn't display cards in Software Operations Workspace

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Operations Workspace for Interaction Management

 PRB1906057

</td><td>

The chat session tab is purple in color

</td><td>

The chat session tab is purple when the page is refresh after an interaction ends

</td><td>

1.  Log in as an agent and navigate to SOW workspace.
2.  Log in as requestor and start a chat by navigating to /sp portal.
3.  Accept the chat and then end it.

 Notice that the chat session tab is purple in color.

</td></tr><tr><td>

Service Operations Workspace for On-Call Scheduling

 PRB1915351

</td><td>

Escalation tracking and escalation triggers don't load or save properly

</td><td>

On a zbooted Zurich instance, the live escalation doesn't load. Also, when the user creates and saves an escalation trigger, the record isn't shown in the left panel list.

</td><td>

1.  On a zbooted Zurich instance, log in as an admin user.
2.  Navigate to the Service Operations Workspace \(SOW\).
3.  Navigate to the teams record page of any group.
4.  Select the 'Escalation Triggers and Policies' tab.
5.  Select the **Create Trigger** button.
6.  Fill out the form.
7.  Select **Save.**

Observe that the record isn't shown in the left panel list.

8.  Create a trigger rule in UI 16 with some conditions, and make sure the flow is 'On-Call Assign by Acknowledgement.'
9.  Create a new incident in SOW.
10. In the side panel, select the escalation tracking icon.

 Observe that the live escalation doesn't load.

</td></tr><tr><td>

Service Operations Workspace for Walk-Up Experience

 PRB1900676

</td><td>

The **Check-in** button isn't visible on Service Operations Workspace \(SOW\) for Walk-up location kiosk records

</td><td>

This issue is caused because of the UI Action Visibility record being shipped, causing the UI action to be hidden from other workspaces.

</td><td>

1.  Impersonate an ITIL user.
2.  Navigate to **Service Operation Workspace** &gt; **List** &gt; **Walk-Up** &gt; **Location Kiosks**.
3.  Select any location kiosk record.

 Notice that on the top right side, the **Check-in** button isn't visible.

</td></tr><tr><td>

Service Operations Workspace

 PRB1888160

</td><td>

The 'Configure page' option is missing in the 'List 'page for the List Bundle SNC page variant

</td><td>

The 'Configure page' option is missing for the 'List' page when the page variant used is 'List Bundle SNC'.

</td><td>

1.  Hop in to a Xanadu or Yokohama instance.
2.  Navigate to any workspace.
3.  Navigate to Lists.
4.  Select on the User profile icon to see all the options.

 Expected behavior: The 'Configure page' is seen as an option.

 Actual behavior: The 'Configure page' option is not available as an option.

</td></tr><tr><td>

Service Portal

 PRB1900517

</td><td>

The Portal Search box is a rectangle instead of oval with white spaces surrounding it

</td><td>

This issue was found when upgrading from Yokohama to Zurich.

</td><td>

1.  Hop in to an instance.
2.  Select **Request**.

 Notice that the Search box is in the shape of an oval, and there is white space around it.

</td></tr><tr><td>

Service Portal

 PRB1919036

</td><td>

Faceted Search Widget/Genius Result card doesn't have a responsive design and disappears on a mobile browser or a small browser window

</td><td>

The issue can be reproduced on mobile and on a computer browser with developer tools.

</td><td>

1.  Log in to a Xanadu instance.
2.  Turn on AI Search.
3.  Turn on Genius Results for Portal.
4.  Turn on AI Search on Portal.
5.  Navigate to the Portal where this is turned on \(/sp or /esc\).
6.  Perform a search and view that the Genius Result show.
7.  Inspect the page to view the developer tools.
8.  Set the dimensions to a phone size.

 See that Genius Results disappear.

</td></tr><tr><td>

Service Portal

 PRB1921882

</td><td>

A session isn't reset on the portal enhance chat for Dynamic Window

</td><td>

The session context variables aren't reflecting the updated values after changes are made in the application. Either the server session should be updated or the existing session values should be cleared to ensure the context variables carry the latest information.

</td><td>

 

</td></tr><tr><td>

Session Management

 PRB1921793

</td><td>

Language preferences aren't getting saved

</td><td>

The changes to GlideSession.getLanguage\(\) and LanguageCookieHanlder are breaking how the platform saves the language info when the user logs out. Those changes may also be breaking other functionality inside the language support for non-authenticated users.

</td><td>

1.  Log in to an instance.
2.  Select a language or change the default language of a user.
3.  Once language changes, log out from the instances.

 Expected behavior: An instance should save the selected language.

 Actual behavior: An instance isn't saving the changes.

</td></tr><tr><td>

Software Asset Management Content Service

 PRB1893356

</td><td>

The com.snc.samp plugin fix script is takes long \(1 hour and 10 minutes\) during the Yokohama to Zurich upgrade

</td><td>

This issue occurs when upgrading from Yokohama to Zurich.

</td><td>

Upgrade a Yokohama instance to Zurich.

 Observed that the com.snc.samp plugin fix script takes long during the upgrade.

</td></tr><tr><td>

Software Asset Management

 PRB1899794

</td><td>

Create rotations as a fix script to ensure plugin/store app upgrade rotations are setup for the 'IBM License Compliance for Software Asset Management' application

</td><td>

Rotation schedules aren't created when the plugin is repaired.

</td><td>

1.  Provision an instance with the app-sam-ibm-licensing store app installed.
2.  Check the tables 'Public Cloud vCore' \(ibm\_public\_cloud\_vcore0000 to ibm\_public\_cloud\_vcore0006\), 'HMC Virtual Machine vCore' \(ibm\_vm\_hmc\_vcore0000 to ibm\_vm\_hmc\_vcore0006\), and 'VMware Virtual Machine vCore' \(ibm\_vm\_vcore0000 to ibm\_vm\_vcore0006\).

 Expected behavior: Rotation schedules are created for the plugin tables.

 Actual behavior: None of the tables have rotation schedules created.

</td></tr><tr><td>

Software Asset Management

 PRB1912731

</td><td>

The 'Software Procurement Workflow - Auto Allocation' flow creates allocations even if app-sam-now-assist is activated

</td><td>

The 'Software Procurement Workflow - Auto Allocation' flow allocates 1 license, but shouldn't allocate any if app-sam-now-assist is activated.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1913658

 [KB2290496](https://hi.service-now.com/kb_view.do?sysparm_article=KB2290496)

</td><td>

On an upgrade to Yokohama, new entitlements may get created from entitlement import errors

</td><td>

Users may observe the issue as duplicate entitlements found after an upgrade to Yokohama, or, after an upgrade to Yokohama, a number of entitlements were added that were created by 'system'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1920322

</td><td>

On Red Hat, an undetermined reason is caused by an incorrect 'Virtualized By' relationship

</td><td>

A virtual device should have a 'Virtualized By' relationship to a host, but if the 'Virtualized By' is connected to a virtual instance, it's considered as an incorrect relationship. When a virtual install of Red Hat is on a Virtual Machine with an incorrect virtualized by relationship, there's an undetermined reason created for the install. This is because the incorrect VM-host relationship prevented the install to be added in the 'samp\_vminstall\_on\_pinstall' view, so it can't be found when processing the installs in SamNewRedHat PerSocketPair LicenseCalculator. As a result, the install cannot be reconciled by the calculator and is stamped as 'undetermined'.

</td><td>

1.  Create a VM with 'virtualized by' set to a VMWare Virtual Machine instance.
2.  Create a Red Hat Enterprise Linux install and set 'installed on' to the VM created in step 1.
3.  Create an entitlement for a Red Hat Enterprise Linux \(license metric should be per socket pair\).
4.  Run recon.

 Observe the undetermined reason created for the install.

</td></tr><tr><td>

Software Asset Normalization

 PRB1904901

</td><td>

The enhancements for Norm product / publisher are not cleared / stamped on a few installs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Normalization

 PRB1916894

 [KB2397254](https://hi.service-now.com/kb_view.do?sysparm_article=KB2397254)

</td><td>

A 'Normalization' job isn't re-normalizing discovery models when incorrect content rules are deactivated

</td><td>

When a discovery model table is queried with an array containing more than a million sys\_id's in addquery, GlideRecord query silently fails with a QuerySizeToo LargeSQLException.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reclamation

 PRB1907403

</td><td>

Reclamation candidates and reclamation rule issues

</td><td>

For bulk reclamation, 'Auto generate name' and 'Populate install related fields' Business Rules don't run. Therefore, fields like name, description, product, publisher, cmdb\_ci, etc. are empty.

</td><td>

 

</td></tr><tr><td>

Software Asset Reclamation

 PRB1916098

</td><td>

SAMPReclama tionUtil throws an exception

</td><td>

The NewReclamation WorkflowForMultiple InstallsIT test fails because SAMPReclamationUtil throws an exception. The software installation doesn't have a providerNiceError.

</td><td>

 

</td></tr><tr><td>

Software Lifecycles \(Family Channel\)

 PRB1910582

</td><td>

There's a duplicate sys\_choice for current\_lifecycle \_phase in sam\_sw\_product\_ lifecycle\_report

</td><td>

The duplicate might be coming from the older field as they don't exist in that older field anymore.

</td><td>

 

</td></tr><tr><td>

Survey Management

 PRB1918779

</td><td>

Users can't access survey-related functionality from within the Localization Workspace due to the restricted visibility of a key script

</td><td>

The script include LFSurveyProcessorScript is defined with the default access \(private\) scope. Since it's not accessible publicly, it prevents runtime access from external or scoped applications.

</td><td>

 

</td></tr><tr><td>

System Scheduler

 PRB1920384

</td><td>

There's a missing sys\_scheduler\_me mory\_pressure \_job\_log table on an Oracle instance due to an SQLException in db-dumps

</td><td>

 

</td><td>

1.  Create an instance with an Oracle database.
2.  Open the list view for the sys\_scheduler\_memory \_pressure\_job\_log table.

 Expected behavior: The table should list the records.

 Actual behavior: The table displays a 'not found' error due to a zboot error.

</td></tr><tr><td>

Template Management for Field Service

 PRB1920388

</td><td>

When accessing a work order template, $sm\_templates can be slow and cause memory issues on the client-side \(browser\)

</td><td>

$sm\_templates can be slow when accessing Work Order Template and cause memory issue on the client-side \(browser\)

</td><td>

1.  Open https://\[instance\_name\].service-now.com/$sm\_templates.do ?sys\_id=\[template\_sysid\].

Notice it's slow if the templates have a relatively large number of the task templates.

2.  If it loads eventually, load it multiple times.

 Notice that the page timeouts and becomes blank.

</td></tr><tr><td>

Third-party Risk Management

 PRB1918672

</td><td>

A TPRM industry fix script looks up a non-existent column

</td><td>

After removing the column from the table definition, the same column is still used by the fix script: fix\_script\_adding\_tprm\_industry.xml. During the upgrading, the fix script is looking for the non-existing column 'industry'. It can take 20+ hours to run the fix script.

</td><td>

 

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1877226

</td><td>

Conflict on a field name when creating an offload rule

</td><td>

When configuring an offload rule, there's a conflict if a system field is set as an indexed field.

</td><td>

 

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1889818

</td><td>

The default retry period for failed offloads is too low

</td><td>

The default retry period should be 6 hours.

</td><td>

1.  Generate a record whose offload perpetually breaks.
2.  Make it fail on offload with a 60 minute retry period.
3.  Archive other records that would get offloaded by the same rule.

 Notice that the records never get offloaded.

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1893476

</td><td>

Tier 2 Index tables don't properly store DocumentID data

</td><td>

When creating a Tier 2 offload rule, the user is able to select DocumentID columns for indexing on the cidx\_ table created to store the indexed data. Columns of DocumentID type are missing the 'Dependent Field', which impacts the navigation and readability of index tables. This results in no previews or quick links to the record on cidx table.

</td><td>

1.  Create an archive and offload rule for sys\_email.
2.  Create or choose a sys\_email record which references some other record in its 'instance' column.
3.  Archive the record.
4.  Observe that on the archive table, the link to the referenced record is preserve on the column.
5.  Offload the record to tier 2.
6.  Observe that the link is missing on the cidx\_ar\_sys\_email table, and the data appears '\(empty\)'.
7.  View the XML for the record on the cidx\_ar\_incident.
8.  Observe that the sys\_id is in the instance column.
9.  Navigate to the **sys\_dictionary** table.
10. Open the 'instance' column for cidx\_ar\_sys\_email.
11. Select **Related links** &gt; **Advanced view**.
12. Navigate to the 'Dependent Field' tab.
13. Notice that the **Dependent** Field isn't selected.
14. Navigate to the **sys\_dictionary** table.
15. Open the 'instance' column for ar\_sys\_email.

 Notice that there is a **Dependent** field selected.

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1897660

</td><td>

Change the sys\_property glide. db.archive.offload. free\_storage\_max\_gb value from 100GB default to 36T

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1909722

</td><td>

Forked transactions close the async context immediately on an error

</td><td>

A few users have reported encountering a blank screen.

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1913194

</td><td>

Unhandled Exceptions in GlideTransaction Processor may leak HTTPTransaction objects, causing memory issues

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Universal Task

 PRB1912572

</td><td>

UT agent is unable to add/view checklist items

</td><td>

The UT is configured with task type 'Checklist' for UT agents.

</td><td>

1.  Log in to the instance as an agent.
2.  Open any HR case/Universal request.
3.  Select**Create a universal task** UI action.
4.  Fill the mandatory fields.
5.  Set the task type as 'Checklist'.
6.  **Save** the form.

 Expected behavior: The agent should be able to access the checklist items and can add/delete an item from the record.

 Actual behavior: The checklist items are not available to the agent.

</td></tr><tr><td>

Upgrade Center

 PRB1909309

</td><td>

Upgrading with parallel plugin loading causes Out of Memory \(OOM\) errors due to dense requests to flush caches

</td><td>

Plugins loaded during an upgrade may require the flushing of caches. The next time they are accessed, these caches are reloaded from a database. When combined with the parallel loading of plugin \(PPL\), the density of requests to flush the caches is much higher, which stresses the system.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1923117

</td><td>

Allow the MCP app to access query services

</td><td>

Enable the MCP app to securely query data from the Query Service for faster and more efficient insights.

</td><td>

1.  Navigate to any instance.
2.  Select any specific app scope or perf dashboard.
3.  Create a script and try fetching MCP data using new sn\_app\_analytics. SNAnalytics QueryService\(\).post.
4.  Verify that this script fails due to a scope restriction error.

 Excepted behavior: Users are able to fetch MCP data.

 Actual behavior: Users are unable to fetch MCP data due to a scope restriction error.

</td></tr><tr><td>

UX Framework

 PRB1888918

</td><td>

List with filters isn't rendering as expected when the Chrome extension \(Now link Manager\) posts the full URL

</td><td>

 

</td><td>

1.  Create a list with filters.
2.  Copy the shareable URL.
3.  Navigate to another list.
4.  Attempt to open the filtered list URL in a new Chrome tab.

 Notice that the new tab is closed and the URL is posted to the matching Chrome tab \(Workspace match\), and the filters aren't applied and the entire list is rendered.

</td></tr><tr><td>

UX Framework

 PRB1901587

</td><td>

Intent Library changes cause a SEND\_INTENT \_FEEDBACK error due to no meta.generator ForFeedback

</td><td>

The NAP window eventually displays a message that reads: 'An error occurred while saving your app. Please check with your admin.' The following error can be observed in the browser console: 'IntentTranslatorBehavior: LIBRARY-INTENT-CHANNEL\#SEND\_INTENT\_ FEEDBACK action is missing generatorForFeedback from meta'.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1903448

</td><td>

A UI Builder record page has a nodemap with 250 nodes which takes more than 15 seconds to load as per a WPT run

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1905564

</td><td>

Rendering of 'Incident overview' impact section cards and their content is delayed

</td><td>

Old layout values are persisted.

</td><td>

1.  For any existing macroponent, check its layout bound values in UX Layout Bounds table.
2.  Export that macroponent XML and make some changes to it.
3.  After making the changes, import the XML.
4.  Check the layout bound values again.

 Expected behavior: New layout bound values are reflected with respect to the changes made in the macroponent.

 Actual behavior: The Business Rule does not run when the user imports the XML/system upgrade/plugin upgrad, causing the old layout values to persist.

</td></tr><tr><td>

UX Framework

 PRB1909151

</td><td>

Bundle prefetched route icons

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1912438

</td><td>

Redundant render calculation of subtree if the node is in suspend mode

</td><td>

When a node is in suspend mode, it will not be stamped into the DOM tree, but still build childrenContent of the suspended node in the view function regardless the mode.

</td><td>

1.  Open Chrome dev tool.
2.  Open 'renderMacroponentNode.js' in the source tab.
3.  Add a conditional breakpoint.
4.  Check the 'childrenContent' variable.

 Observe that it's built regardless of the mode.

</td></tr><tr><td>

UX Framework

 PRB1915549

</td><td>

The ui-core-bundle may perform better if the sn-ui-logger and the ui-analytics-bundle are moved to another bundle

</td><td>

The ui-core-bundle is large, but its size can be reduced by moving the ui-analytics-bundle and the sn-ui-logger to another bundle. This may benefit the network load and the the CPU cycles for the repeat view \(because of the script evaluation and script parsing time\).

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1915794

</td><td>

Data doesn't display in the Teams module on the Zurich instance

</td><td>

Data doesn't display in the Teams module on the Zurich instance. For example, assignment groups may not appear.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1915996

</td><td>

The client script added on 'macroponent ready' and 'macroponent property changed events' doesn't trigger

</td><td>

When the user creates a controller and adds a client script on 'macroponent ready' and 'macroponent property changed events,' the client script isn't executed.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1916142

</td><td>

Intent library updates for Gen AI Canvas

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1918618

</td><td>

Session tabs above the maxCachedPage Count stay in DOM

</td><td>

 

</td><td>

1.  Open the Service Operations Workspace incident records list.
2.  Open at least 7 record tabs.
3.  Select one of the opened tabs.

 Expected behavior: There should be only 6 \(1 active + 5 chrome\_main.maxCachedPageCount\) session tab content in the DOM, the rest of tabs should have their sn-canvas-screen \#shadow-root nodes detached.

 Actual behavior: All 7 tabs are open and all their shadow-root nodes are stored in DOM.

</td></tr><tr><td>

UX Framework

 PRB1920715

</td><td>

UxExperienceURL Converter.convertURL ToRoutePayload doesn't support URLs that have '\_\_state\_\_'

</td><td>

When the URL points to a UXF page that also has an encoded persisted state \(\_\_state\_\_\), the generated route payload doesn't contain that state and hence is inaccurate to the URL. This is causing an issue with the history menu, where the route payload attached to history items only contains the list id and no persisted state, and selecting the history item is opening the list but not matching the description of the query conditions for that URL, because the route payload doesn't contain the persisted state.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1923265

</td><td>

Preload cacheable content for screen and shell

</td><td>

 

</td><td>

Open ITSM Workspace.

 Observe that partial requests aren't preloaded early in the document.

</td></tr><tr><td>

UX Framework

 PRB1923311

</td><td>

UX dependency tracing should use LargeContent DiskCache.get Metadata to avoid file touching

</td><td>

File descriptors should not increase when there is a cache hit.

</td><td>

1.  Access a workspace homepage \(for example: CSM, SOW, or Case Record\).
2.  Re-load the page multiple times.
3.  Monitor open file descriptors for LSOF.
4.  Notice the file descriptor entries.

 Notice that the file descriptors increase even when there's a cache hit.

</td></tr><tr><td>

UX Framework

 PRB1924691

</td><td>

Improve toolbar and session tabs rendering for direct load repeat view

</td><td>

 

</td><td>

1.  Navigate to any instance.
2.  Do a direct load for pages in workspace with UXR Workspace Appshell.

</td></tr><tr><td>

UX Framework

 PRB1925967

</td><td>

Engagement Messenger isn't loading chats after upgrading

</td><td>

The chat box in Engagement Messenger is blank, and loads no content. The errors occurs, 'SecurityError: Failed to read a named property 'uxfIntentLibrary' from 'Window'.

</td><td>

1.  Launch the Engagement Messenger.
2.  Select the chat box.
3.  Observe that the chat box is blank.
4.  Navigate to a Yokohama instance.
5.  Navigate to Agentic Portal in a separate browser tab, but don't attempt to log in.
6.  Open the dev console.
7.  Execute the script.
8.  Execute the code.
9.  Select the chat bubble that appears after the code finishes executing.

 Expected behavior: The chat loads with content.

 Actual behavior: The chat load is blank and a security error appears in console.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1891033

</td><td>

Marking the 'AI Agent'/ 'Agentic Workflows' as 'Promoted' from VA designer does not show up as a Promoted action in Virtual Agent

</td><td>

The user should be able to mark AI Agents / Agentic Workflows as 'Promoted' from VA Designer, but this does not appear as a promoted action.

</td><td>

1.  Ensure all Agentic Workflow and Now Assist Virtual Agent plugins are updated on the instance.
2.  Navigate to **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.
3.  Select the tab 'Agentic Workflow' and select an base instance workflow.
4.  Mark the workflow as 'promoted'.
5.  Ensure the Agentic Workflow is active, visible and discoverable.
6.  Navigate to the esc portal.

 Notice that no promoted Agentic Workflow / AI Agents appear as a button \(promoted action\).

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1891079

</td><td>

Validate NLU discoverable topics retrieved from cache when domain separation is turned on

</td><td>

Provide a scriptable function vaSystem. getNLUDiscoverableTopics \(String languageCode\) that returns the names of the active and discoverable topics given a language code. If no languageCode is given, it uses the session language. If NLU is turned off on the instance or com.glide.cs.cache.topic\_type.enabled is false, it should return an empty list and log why.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1917696

</td><td>

Virtual Agent Designer isn't displaying options for subflows if there are more than 100 spokes

</td><td>

.

</td><td>

1.  Log in to an instance with more than 100 spokes.
2.  Navigate to **Virtual agent designer** &gt; **Open a new topic**.
3.  Add the 'Action' component to the designer.
4.  Check the option 'subflows' for 'invoke flow designer object'.
5.  In the 'Spokes' menu, select a spoke which is at the end of the list in the 'Spokes' table.
6.  Select the 'subflow' menu.

 See that there isn't any options.

</td></tr><tr><td>

Virtual Agent

 PRB1879865

</td><td>

Now Assist doesn't generate Japanese answers properly

</td><td>

The results are mostly in English.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881959

</td><td>

The user doesn't receive small talk responses in WhatsApp LLM mode

</td><td>

When using Whatsapp in LLM mode, the user receives search-related responses instead of small talk responses.

</td><td>

1.  Navigate to Whatsapp in LLM mode.
2.  Try to say 'hello,' 'how are you,' or 'thanks.'

 Expected behavior: The user gets small talk responses.

 Actual behavior: The user gets search-related responses.

</td></tr><tr><td>

Virtual Agent

 PRB1887850

</td><td>

Setting com.glide.cs. task.transaction. enabled sysprop to true causes multiple issues

</td><td>

A sys\_generative\_ai\_log record with definition = 'Summary \(Now LLM Mixtral\)' has nothing recorded for prompt\_token\_count and response\_token\_count.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1890524

</td><td>

Increase in heap utilization due to expression cache for search

</td><td>

This issue occurs from a script include expression cache from platform.

</td><td>

1.  Set up Now Assist Virtual Agent \(NAVA\) on a Yokohama instance.
2.  Perform search actions from the chat window.
3.  Notice that the expression cache is filled due to this.

 Notice that the load of 25 users on a single node for one hour for the search action performed occupies more than 500MB.

</td></tr><tr><td>

Virtual Agent

 PRB1890944

 [KB2338484](https://hi.service-now.com/kb_view.do?sysparm_article=KB2338484)

</td><td>

Large /api/now/v1/cs/ consumerAccount /unreadMessage calls from Proactive Trigger exhausts instance API resources

</td><td>

Some users on Portal have over 1 million of /api/now/v1/cs/ consumerAccount /unreadMessage call observers in the node logs. This causes an issue as it exhausts the API rate limit and prevents people from submitting forms on the portal and other issues. The API call is constantly sent out even when the session is timed out.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1892135

</td><td>

A reference datatype gives multiple output cards instead of one card

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1892416

</td><td>

Incorrect column usage when updating the One API Service Plan Invocation record

</td><td>

A warning occurs in the logs.

</td><td>

1.  Execute any simple Now Assist Virtual Agent use case \(for example: small talk, what is spam\).
2.  Notice the warning in the logs: '2025-05-13 08:59:06 \(140\) glide.cs.worker.93 SYSTEM txid=c1dfd72c876d SSI\_ef76d022b7cf9a109d63827b5e11a913 WARNING \*\*\* WARNING \*\*\* getGlideElement called for unknown field 'startedAt' in table 'one\_api\_service\_plan\_feature\_invocation' 2025-05-13 08:59:06 \(140\) glide.cs.worker.93 SYSTEM txid=c1dfd72c876d SSI\_ef76d022b7cf9a109d63827b5e11a913 WARNING \*\*\* WARNING \*\*\* setValue called for unknown field 'startedAt' in table 'one\_api\_service\_plan\_feature\_invocation''.

</td></tr><tr><td>

Virtual Agent

 PRB1892510

</td><td>

Support 'Sync' mode for Java execution path

</td><td>

Currently, the Java execution path for OE system executor capabilities are limited to just the async mode. This is limiting the ability to execute troubleshooting tools via background scripts. The 'Sync' mode execution should be fully supported for the Java path as well.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1893137

</td><td>

Virtual Agent LLM Survey shows the question twice

</td><td>

There is LLM support for a survey, and the questions asked in the survey are populated twice.

</td><td>

1.  Access a Yokohama instance with Now Assist Virtual Agent.
2.  Navigate to **Designer**.
3.  Create a test topic.
4.  Add the topic block node.
5.  Add 'Survey-LLM' for the topic block.
6.  Pass any survey ID with at least five choices.
7.  Test the topic.

 Observe that each question populates twice.

</td></tr><tr><td>

Virtual Agent

 PRB1894001

</td><td>

Processing messages appear when using the AI Agent Studio

</td><td>

When the user creates a workflow or agent and runs the test in playground, the 'Planning the next steps' and 'undefined' messages appear.

</td><td>

1.  Create a workflow/agent. \(It can be very basic, like Hello world.\)
2.  Run the test in playground.

 Notice that the 'Planning the next steps' and 'undefined' messages appear.

</td></tr><tr><td>

Virtual Agent

 PRB1894063

</td><td>

The sendFeedback method throws an error: 'User is not authorized to update log record'

</td><td>

 

</td><td>

1.  Log in to an instance as an admin.
2.  Initiate a conversation with LA.
3.  Log in as a user.
4.  Carry out a conversation.
5.  End the chat.
6.  Modify the LLM generated short description.

 Expected behavior: An edited response field should be updated in the sys\_generative\_ai\_log table.

 Actual behavior: An edited response field isn't updated.

</td></tr><tr><td>

Virtual Agent

 PRB1894471

</td><td>

Virtual Agent push notifications aren't coming through on mobile

</td><td>

Noticed on Android.

</td><td>

1.  Set up a user with a push token and mobile client with NASS chat.
2.  Start a chat.
3.  Send a sequence of messages synchronously.
4.  Close the mobile client when they are sending.
5.  Wait.

 Expected behavior: Users should see a push notification.

 Actual behavior: There's no push notification in NASS.

</td></tr><tr><td>

Virtual Agent

 PRB1894545

</td><td>

LLM responses are not unmasked if streaming is enabled with java proxy enabled

</td><td>

 

</td><td>

1.  Enable NowAssist assistant with streaming.
2.  Use GPT4-0.
3.  Enable masking for email address and/or phone number types for the phrase 'what is my contact information'.

 Expected behavior: The unmasked email/phone numbers are displayed.

 Actual behavior: The email/phone numbers are displayed with masks.

</td></tr><tr><td>

Virtual Agent

 PRB1894930

</td><td>

The AI Agent gets stuck in the 'Ongoing' state when invoking the static method 'sendDynamic ProgressMessage'

</td><td>

The AI Agent gets stuck in the 'Ongoing' state when invoking the static method 'sendDynamicProgressMessage' from within the agent's tool. The syslog also shows lock version mismatch and conversation context mismatch errors.

</td><td>

1.  Set up Glide with the latest track/znowassist.
2.  Provision an instance with the latest sn-app-deploy node package globally installed.

3.  Clone the now-assist-deploy-plans repo and check out the main branch.
4.  Run the deploy plan to install the Now Assist AI Agents and all of the dependent apps. \(This process takes around 40 minutes.\)
5.  Set up the Azure GPT-4o connection and credential under the connection alias 'Azure OpenAI' on the sys\_alias table.
6.  Install the sample agent with the name 'Find User.'
7.  Navigate to the 'Create and Manage' module from the 'AI Agent Studio' application menu in the filter navigator.
8.  Select the 'Testing' tab, then select the **Find User** agent from the drop-down list.
9.  Paste the following into the **Task** field: 'Find user by email \[example email\].'
10. Select **Start test.**

 Observe that the agent gets stuck in ongoing state. The syslog also shows lock version mismatch and conversation context mismatch errors.

</td></tr><tr><td>

Virtual Agent

 PRB1895090

</td><td>

The dynamic loader doesn't display in NAVA on iOS

</td><td>

When the user launches NAVA and enters an utterance, the dynamic loader doesn't display. This occurs on iOS, but it works as expected on Android.

</td><td>

1.  Connect iOS requestor Version 20.1 \(.4061\) to mobiletrackznowassist.
2.  Log in as an admin user.
3.  Launch NAVA through the chat launcher.
4.  Enter the utterance 'Categorize INC0000025.'

 Observe that the dynamic loader doesn't display in NAVA. However, it works as expected on Android.

</td></tr><tr><td>

Virtual Agent

 PRB1896418

</td><td>

Gaic Timing on for App Generation on XP3 with NAFC NAFC26.4.0

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1896593

</td><td>

Shouldn't be relying on the 'Greetings' topic for portal's Virtual Agent hand off

</td><td>

Users can have custom 'Greetings' topics. For those users, the hand off is broken.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1896645

</td><td>

The header/title isn't updated until the agent tool execution completes

</td><td>

The header/title isn't updated until the agent tool execution completes when invoking the static method 'sendDynamicProgressMessage' from within the agent's tool.

</td><td>

1.  Set up Glide with the latest track/znowassist.
2.  Provision an instance with the latest sn-app-deploy node package globally installed.
3.  Clone the now-assist-deploy-plans repo and check out the main branch.
4.  Run the deploy plan to install the Now Assist AI Agents and all of the dependent apps. \(This process takes around 40 minutes.\)
5.  Set up the Azure GPT 4.1 connection and credential under the connection alias 'Azure OpenAI' on the sys\_alias table.
6.  Install the sample agent with the name 'Find User.'
7.  Delete any records in the 'sys\_gen\_ai\_feature\_mapping' table.
8.  Navigate to the 'Create and Manage' module from the 'AI Agent Studio' application menu in the filter navigator.
9.  Select the 'Testing' tab, then select the **Find User** agent from the drop-down list.
10. Paste the following into the **Task** field: 'Find user by email \[example email\].'

 Observe that the header/title isn't updated until the agent tool execution completes.

</td></tr><tr><td>

Virtual Agent

 PRB1898661

</td><td>

Non-LLM time has increased from 2544 to 3065 milliseconds \(ms\), leading to 500-900 ms in some NAVA use cases

</td><td>

In NAVA use cases, users observed 500–900 ms degradation from 2544 to 3065 ms in non-LLM async time. For a synthesized response, the non-LLM has degraded and it's spending additional 1.2 secs on that. Hence, the overall gain on the response stands at 5.3 seconds \(6.5-1.2\).

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1899360

</td><td>

Virtual Agent changes to publish message to AMBNodeDelivery MessageQueue also effects FDIH flows

</td><td>

These changes were only aimed to be used by Virtual Agent flows, not other FDIH flows.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1901579

</td><td>

When streaming is on, results aren't coming back

</td><td>

If streaming is turned off, results are coming back.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1902898

</td><td>

Attachments aren't deleted post-chat deletion

</td><td>

 

</td><td>

1.  Start a conversation from Dynamic Window \(DW\).
2.  Trigger a skill which includes a file upload.
3.  Post a skill execution.
4.  Navigate to sys\_cs\_conversation.
5.  Open the same active conversation and mark conversation the state as 'faulted'.
6.  In DW and under 'Chat', delete the same chat listed in the closed chat.
7.  Navigate to the sys\_attachment table and the 'Conversation task' table.

 Expected behavior: The file upload should be removed.

 Actual behavior: The file upload still exists in both places.

</td></tr><tr><td>

Virtual Agent

 PRB1903011

</td><td>

The error 'Cannot invoke 'org.apache.commons. httpclient.StatusLine. getStatusCode\(\)' because 'this.statusLine' is null' for LTM capabilities

</td><td>

The error is observed in the Gen AI logs for the conversation.

</td><td>

1.  Switch to any model.
2.  Try any utterances.

 Observe that in the Gen AI logs for that conversation, there's an error, 'Error: Cannot invoke 'org.apache.commons.httpclient.StatusLine.getStatusCode\(\)' because 'this.statusLine' is null Error Code: 200000'.

</td></tr><tr><td>

Virtual Agent

 PRB1903705

</td><td>

Chat type indicator and the message sender info is missing when a chat with a guest user and base instance guest user is deleted

</td><td>

Even though the Asynchronous Message Bus message is received, a new message isn't rendered.

</td><td>

1.  Install the Agent Chat plugin.
2.  Navigate to **CI settings**.
3.  Enable the public access for web client to allow the user to start a chat as a guest without logging in.
4.  Disable the business rule.
5.  Delete 'Guest' as an admin user.
6.  Open the sys\_user table.
7.  Delete the guest user record.
8.  Open another browser.
    1.  Log in as one of the agents.
    2.  Navigate to the Service Operations Workspace.
    3.  Mark the agent as 'available'.
9.  Start a chat as a guest through the $va-web-client-app.do.
10. Accept the chat as an agent.
11. Allow the guest requestor to type and send something.

 Expected behavior: Agent should see the type indicator when the guest is typing, and should see the message with the guest avatar when the message is sent.

 Actual behavior: A type indicator isn't shown and no new message is rendered until the screen re-rendered.

</td></tr><tr><td>

Virtual Agent

 PRB1905872

</td><td>

A new conversation with a skill created in sessionContext does not execute

</td><td>

A newly created conversation with a skill does not execute.

</td><td>

1.  Load an instance and open devtools.
2.  In the elements pane, find 'sn-polaris-layout'.
3.  In the console, type 'allow pasting'.
4.  Run a sys\_id from sys\_gen\_ai\_skill.

 Notice that the skills is not executed.

</td></tr><tr><td>

Virtual Agent

 PRB1906437

</td><td>

LTM Identify memories error out and conversation gets stuck

</td><td>

Conversation gets stuck in the GenAI logs. The user observes these errors: Cannot invoke 'java.util.Map.get\(Object\)' because 'originalResponse' is null for LTM Identify memories \(Azure OpenAI Chat Completions\).

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1907551

</td><td>

After invoking an abort action in an Agentic Virtual Agent Flow, the conversation breaks

</td><td>

The conversation gets stuck when the **Stop** button is selected during a query.

</td><td>

1.  Provision an instance with an agentic flow that is executable via Virtual Agent.
2.  Enter an utterance like 'help me resolve inc0000025' and select the **Stop** button while the flow is in progress.

 Observe that the conversation gets stuck.

</td></tr><tr><td>

Virtual Agent

 PRB1907682

</td><td>

Skill Discovery doesn't work after stopping Agentic Flow

</td><td>

An error message displays.

</td><td>

1.  Enable 'Generate Resolution Plan Use Case' for NAP.
2.  Execute 'Generate Resolution Plan Use Case' for NAP.
3.  Once the **Stop** button appears, select it.
4.  The user is prompted with: 'The current conversation has been stopped, but you can begin again. I'm an AI-powered virtual assistant that can handle work-related questions and requests.'
5.  Enter a 'Summarize a record' utterance.

 Observe that the skill is not discovered, and the following message is displayed: 'Unfortunately, there is not enough information available to address this query completely. Assistance can be provided on other topics such as reporting performance problems, creating incidents, booking meeting rooms, or learning about workstation security if needed.'

</td></tr><tr><td>

Virtual Agent

 PRB1908803

</td><td>

api.insertSkillACL BySkillId operation accepts role as String instead of Array of Strings

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1908805

</td><td>

API for authoring 'gen\_ai\_skill' acls from NASK UI

</td><td>

The goal of this ticket is to create a script include API in global scope \( shipped as part of OneExtend plugin\). This API should be restrictive with hard-coded values for the ACL of type: 'gen\_ai\_skill' and operation: 'execute'. It should take id as skillConfigId\_\[human\_readable\_name\] as the name and some roles from the user in NASK user experience. It should allow create, update and delete of the ACL given an id.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1910141

</td><td>

Duplicate messages are seen after receiving multiple notifications in NAVA

</td><td>

This issue is observed in the standard chat experience.

</td><td>

1.  Open a conversation in NAVA with the system admin.
2.  Impersonate another user \(Abraham Lincoln\).
3.  Update the HR case: HRC0001023 state multiple times with the Abraham Lincoln user.

This triggers multiple notifications in Virtual Agent.

4.  Impersonate the system admin user.
5.  Navigate to the ESC portal.

 Observe the same message appearing in NAVA after all notifications have been received.

</td></tr><tr><td>

Virtual Agent

 PRB1910766

</td><td>

One extend APIs aren't honoring a timeout with Virtual Agent \(VA\)

</td><td>

Even though timeout is set to 20 seconds, executions aren't exceeding that and completed at over 20 seconds. There are quite a lot of Gen AI calls with more than 20 seconds duration from the conversations. In the last 7 days, there have been a total of 5079 Gen AI log records from conversations that took more than 20 seconds.

</td><td>

1.  Set up Now Assist for platform and related apps.
2.  Make sure Knowledge Graph is installed and enabled for VA QnA.
3.  Ask a question involving a large amount of records to be returned like, 'give me all user details' or 'List all the incident details'.

 Expected behavior: VA conversations are shouldn't error out.

 Actual behavior: VA conversations are errored out.

</td></tr><tr><td>

Virtual Agent

 PRB1911623

</td><td>

Conversation doesn't continue when a guardrail is triggered in Now Assist Virtual Agent \(NAVA\)

</td><td>

After receiving the response from Guardian, the conversation should continue by providing options to the user 'dark roast' or 'medium roast' for the example scenario. When the user enters 'dark roast,' it kicks off the order coffee topic all over again.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1912380

</td><td>

Don't log agent skill execution licensing

</td><td>

It shouldn't create a licensing record when an agent skill is executed. The AIA framework does its own calculation/logging for agent execution based on the execution tasks created at runtime.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1912588

</td><td>

AiAgentSecurity Migration and AiAgentSecurity Helper script includes needs to be in the global scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1912822

</td><td>

No option to add an optional security attribute in the insert or update functions in the GenAiSkill SecurityUtils API

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1913154

</td><td>

Non-actionable notifications under regular cases create interaction records for channels and NASS

</td><td>

For channels and NASS, it creates a conversation and does a silent handshake for NASS/NAVA. This creates a conversation and an interaction internally, which is incorrect.

</td><td>

1.  Make sure that the user has had some conversation with NASS/Channel.
2.  Trigger a non-actionable notification.

 Expected behavior: A conversation associated with the notification shouldn't have an interaction record.

 Actual behavior: An interaction record is created.

</td></tr><tr><td>

Virtual Agent

 PRB1913835

</td><td>

Canvas isn't displaying the Show/Hide options when executing a skill

</td><td>

While Web Agent is executing the goal, the live 'Screenshot' view isn't loaded. After the execution, it's displaying the Show/Hide view, which is displaying all the screenshots.

</td><td>

1.  Create an Agent WF.
2.  Promote it.
3.  Navigate to Now Assist Portal.
4.  Switch to the 'Maximize' view.
5.  Select the skill and start it.
6.  Verify the live 'Screenshot' view isn't loaded.

</td></tr><tr><td>

Virtual Agent

 PRB1913892

</td><td>

Validation should be added for security attribute ID in global.GenAiSkill SecurityUtils\(\).insert SkillAclBySkillid\(...\) and global.GenAiSkill SecurityUtils\(\).update SkillAclByAclId\(...\)

</td><td>

While calling global.GenAiSkill SecurityUtils\(\).insert SkillAclBySkillid\(...\) and global.GenAiSkill SecurityUtils\(\).update SkillAclByAclId\(...\) with invalid sys id of security attribute, the security attribute is created with an empty condition. Since it is expected to used with Background script, the user should be informed of the invalid value used for the security attribute.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1914417

</td><td>

Stopping agentic conversation show an undefined message

</td><td>

 

</td><td>

1.  Start any agentic flow from Dispatcher Workspace, Now Assist Panel, NASS, or Playground.
2.  Select the **Stop** button once it's displayed.

 Observe the undefined message is displayed.

</td></tr><tr><td>

Virtual Agent

 PRB1914550

</td><td>

The Virtual Agent \(VA\) input box is disabled after page refresh

</td><td>

When the user refreshes a page in dynamic window \(DW\), the VA input box is disabled and VA is not useable.

</td><td>

1.  Navigate to the /ESC portal.
2.  Start DW.
3.  Start web search by selecting the globe icon.
4.  End web search by selecting **END** in the banner.
5.  Refresh the page.
6.  Open DW.

 Expected behavior: The input box is available so the user can continue to use VA.

 Actual behavior: The input box is disabled and VA is not useable.

</td></tr><tr><td>

Virtual Agent

 PRB1915170

</td><td>

Web search ends if the user sends the 'End' emoji in a standard chat

</td><td>

When the user sends the 'End' emoji, the Virtual Agent responds by ending web search. After a page refresh, the web search globe icon is still enabled. If the user selects the globe icon again, web search doesn't end.

</td><td>

1.  Navigate to **/SP**.
2.  Start a standard chat.
3.  Start web search mode.
4.  Send the 'End' emoji.

 Expected behavior: The emoji doesn't cause web search to end. The user retains normal functionality in the Virtual Agent.

 Actual: The Virtual Agent responds by ending web search. After a page refresh, the web search globe icon is still enabled. If the user selects the globe icon again, web search doesn't end.

</td></tr><tr><td>

Virtual Agent

 PRB1915460

</td><td>

gen\_ai\_agent and gen\_ai\_workflow advance is turned off in the ACL form16 UI

</td><td>

 

</td><td>

1.  Navigate to sys\_security\_acl.do.
2.  Select the type as gen\_ai\_agent or gen\_ai\_workflow.

 Observe that there's no option called 'advanced'.

</td></tr><tr><td>

Virtual Agent

 PRB1915751

</td><td>

Midtopic switch isn't switching to a new topic and runs into an error on the continuing existing topic

</td><td>

 

</td><td>

1.  Navigate to Dynamic Window.
2.  Type 'i want to order food'.
3.  Answer one of the prompts.
4.  Type 'i want to order coffee actually'.

 Expected behavior: The user should be given an option to switch to the 'Order coffee' topic and have an option to continue the request.

 Actual behavior: The user gets the order food topic started again and choosing 'continue' runs into an error as well.

</td></tr><tr><td>

Virtual Agent

 PRB1915793

</td><td>

There's an incorrect name for flows when creating 'invoke\_from\_ai' ACLs

</td><td>

 

</td><td>

Execute this API to create ACLs for flows used as tools: 'new global. AiAgentSecurityMigration\(\) .run\( true\)'.

 Observe that for the subflow ACLs, the ACL is created with 'name' instead of 'internal\_name', which is incorrect and it's missing ACL evaluations at run time. It's defaulting to global \* ACL due to the incorrect name of the flow.

</td></tr><tr><td>

Virtual Agent

 PRB1916057

</td><td>

Fall back options aren't displayed when 'Displeasure Small Talk' is triggered

</td><td>

When the user triggers 'Displeasure Small Talk,' the response 'Hmm, I don't understand this request' appears instead of the fall back options.

</td><td>

1.  Start a conversation from NAP.
2.  Enter 'Summarize a record.'
3.  Enter the record number when prompted.
4.  Once the summary is generated, enter 'Am not happy.'

 Observe that the response 'Hmm, I don't understand this request' appears. No fall back options are displayed.

</td></tr><tr><td>

Virtual Agent

 PRB1916762

</td><td>

An ACL restriction on sys\_one\_extend \_resource\_edge prevents websearch from being accessible to users

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1917121

</td><td>

Update the ACL name for OE skills to align with changes from the OE team

</td><td>

Update the ACL name format to use the '&lt;sys\_name.skillConfigId' format instead of the 'skillConfigId:&lt;sys\_name' format \(where skillConfigId is the sys\_id of the record, and sys\_name is the name of the record in sn\_nowassist\_skill\_config\). This is only applicable when the 'internal\_name' column in the sn\_nowassist\_skill \_config table is empty.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1917378

</td><td>

Agentic eval metric score standardization

</td><td>

It should incorporate the changes in NASK to display the label in the list view and the drill down view.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1918363

</td><td>

Canvas isn't working

</td><td>

The **Show** button doesn't appear at end of the execution.

</td><td>

1.  Set up Canvas
2.  Navigate to Now Assist Panel on the instance.
3.  Select **Canvas Flow**.
4.  Enter **Yes** to answer the question that it's ready to execute Canvas.

 Expect behavior: At end of the execution, users will see the **Show** button.

 Actual behavior: Nothing appears.

</td></tr><tr><td>

Virtual Agent

 PRB1918740

</td><td>

Querying on virtual column for retrieving skill metadata fails

</td><td>

 

</td><td>

1.  Navigate to AI Agent Studio.
2.  Choose an existing workflow or agent which has Now Assist Panel or Virtual Agent roles enabled.
3.  Create a new agent or workflow.
4.  Choose a role for those who can access the workflow or agent.
5.  Save and continue.

 Expected behavior: Previously associated skill applicability records should be deleted.

 Actual behavior: Previously associated skill applicability records still exists.

</td></tr><tr><td>

Virtual Agent

 PRB1920529

</td><td>

Skip define access in guided setup doesn't clone the NACM default ACL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1920729

</td><td>

Multiple conversations fail to maintain an 'adapter' state

</td><td>

consumerAccount and externalConversationId are missing sys\_cs\_adapter\_ conversation\_lookup for the first conversation.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1920790

</td><td>

A high query execution count contributes to performance degradation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1921188

</td><td>

Citations aren't returning in multilingual scenarios

</td><td>

Instead, 'null' is printed.

</td><td>

1.  Navigate to /esc.
2.  In the NAVA chatbot, enter '¿Qué son las legumbres?'.

 Observe that a Genius result comes back, but there's console errors flagging 'no citation' as well as no citations appearing in the UX. Observe that in output of AIA Planner 2 \(gpt\_large\), the document is cited in the **Response** field.

</td></tr><tr><td>

Virtual Agent

 PRB1921721

</td><td>

When topics are executed via Skill Discovery, topic script exceptions result in stuck conversations

</td><td>

The topic should fail and redirect to an error topic, but it 'sticks' instead.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1922067

</td><td>

A incorrect action is executed by a tool

</td><td>

Creating an action or a flow and changing its name before its first publish ends up with mismatch between the main snapshots internal\_name and the definitions internal\_name. The FlowActionProviders getMinimalMain ActionTypeSnapshot returns the internal name of the master\_snapshot and not the definition, which is incorrect and won't work when calling a flow by it internal name.

</td><td>

1.  Log in to an instance.
2.  From the playground and NAVA, select **Smartsheet user management AI agent**.
3.  Pass the utterance as 'get admin details'.

 Observe that it throws a 'Unexpected token: 'error. In the background execution, observe that wrong action is executed.'

</td></tr><tr><td>

Virtual Agent

 PRB1923131

</td><td>

sn-chat-choice-picker appears instead of text-picker for users that turned on the new sys prop

</td><td>

A choice picker with radio buttons appears for users that turned on the new sys prop, instead of the expected text picker with a list of topics.

</td><td>

1.  Turn on Now Assist Virtual Agent.
2.  Create a virtual agent topic.
3.  Select static/dynamic node and populate choices.
4.  Run the topic in NAVA.

 Expected behavior: If the user turned on the new sys prop, a text picker with a list of topics is displayed.

 Actual behavior: A choice picker with radio buttons is displayed.

</td></tr><tr><td>

Virtual Agent

 PRB1923271

</td><td>

With streaming turned on, a response gets stuck

</td><td>

Occurs when CEA agentic is off.

</td><td>

1.  Turn on streaming for CEA or bot.
2.  Navigate to CEA or bot.
3.  Type 'hi'.
4.  After getting a response, type something else.

 Expected behavior: The stream should complete without any issue.

 Actual behavior: The streaming is stuck and times out.

</td></tr><tr><td>

Virtual Agent

 PRB1923622

</td><td>

After selecting 'log in' and the user authenticating itself on the server, the conversation is refreshed but it's not resumed

</td><td>

In Agent Studio, after selecting 'log in' and the user authenticating itself on the server, the conversation is refreshed but it's not resumed. It's again asking to authenticate by displaying the same 'Log in' link in the conversation. In order to continue with the execution, the users has to restart the flow.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1923828

</td><td>

Fix choicepicker branding for NAVA

</td><td>

Choice picker shows default NAVA branding even though different branding was selected.

</td><td>

1.  Navigate to the 'Assistants' page.
2.  Create a new branding record in the sys\_cs\_branding\_setup table.
3.  Change the branding of the new record to 'Polaris-dark'.
4.  Navigate to /esc portal.
5.  Select a topic that uses the choice-picker.

 Expected behavior: The choice picker matches the selected branding.

 Actual behavior: The choice picker displays the default NAVA branding.

</td></tr><tr><td>

Virtual Agent

 PRB1924171

</td><td>

Fallback isn't working

</td><td>

 

</td><td>

1.  Navigate to /esc.
2.  Search for something that doesn't bring back any results, like 'which is better AMD vs Intel'.

 Expected behavior: Virtual Agent \(VA\) should go into fallback, and offer the user websearch, record producer, or live agent \(whatever is enabled for fallback\).

 Actual behavior: The users are getting an 'unfortunately' message and VA is having a technical issue.

</td></tr><tr><td>

Virtual Agent

 PRB1924923

</td><td>

Slow API queries for NowAssistConversation History\(\).\_getTranscript ForConversationHistory API

</td><td>

 

</td><td>

1.  Open an instance.
2.  Navigate to the ESC portal
3.  In the NASS chat, type an utterance like 'Hello!'
4.  Check the system logs for keywords starting with 'NowAssistConversationHistory: Time taken to retrieve transcripts for conversation history is.'

 For a new conversation, observe that the first hit to this API takes over 500 milliseconds.

</td></tr><tr><td>

Virtual Agent

 PRB1925496

</td><td>

SQL does a table scan on the sys\_cs\_session \_binding table for auxiliary subscripting, causing high SQL time

</td><td>

Auxiliary is the only subscription timing out, and the SQL processing time is more than 500ms.

</td><td>

Launch Now Assist Virtual Agent \(NAVA\).

 Notice the processing time for the subscription when launching the chat client.

</td></tr><tr><td>

Virtual Agent

 PRB1925600

</td><td>

Users are unable to remove prod bot integration from an instance

</td><td>

 

</td><td>

1.  Connect prod bot to an instance.
2.  Send a few messages in Teams.
3.  Try to remove the Teams integration for prod bot.

 Expected behavior: The integration is removed from an instance.

 Actual behavior: The user gets the error 'failed to remove integration...' and the integration isn't removed.

</td></tr><tr><td>

Virtual Agent

 PRB1926867

</td><td>

The skillParams in a session context isn't persisted

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1927087

</td><td>

Cold starts on Teams/CEA and LA handoffs are running into a fallback error

</td><td>

 

</td><td>

1.  Navigate CEA.
2.  Type 'hi'.
3.  Type 'i want to connect to a live agent'.
4.  After getting an LA card, select **Connect to agent** for handoff.

 Expected behavior: The handoff works without any error.

 Actual behavior: After handoff, the user runs into a fallback error.

</td></tr><tr><td>

Virtual Agent

 PRB1927417

</td><td>

Fallback in NAVA returns a technical error

</td><td>

 

</td><td>

1.  Navigate to NAVA.
2.  Send a gibberish message or anything that returns fallback as a user.

 Expected behavior: The user should get a fallback response.

 Actual behavior: The user gets a fallback response and then a technical error.

</td></tr><tr><td>

Virtual Agent

 PRB1930014

</td><td>

The true-up version in repo files needs to be updated with a hotfix version post-sign off

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1930434

</td><td>

Multilingual functionality is broken, and the complete flow is not working as expected

</td><td>

This issue was observed in Yokohama with RAG 3.0.4 after the ynowassist nightly build occurred.

</td><td>

1.  Impersonate as user with Japanese session language.
2.  Ensure 'glide.sys.language' system property is in Japanese with the system property value would be 'ja'.
3.  Create a skill.
4.  Add RAG as tool.
5.  Execute the skill.

 Expected behavior: The skill and RAG tool should execute successfully.

 Actual behavior: RAG is failing with attached error.

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1920178

</td><td>

Updating a message flow for a third-party message is sending a reply back to the requestor

</td><td>

 

</td><td>

1.  Initiate a chat between an agent and requestor using the Virtual Agent API.
2.  Add the 'third\_party\_chat' custom adapter property to true with reference to a provider application.
3.  Send a message from an agent.
4.  Update the message text using the **UPDATE\_MESSAGES** action.

 Expected behavior: An updated message must not be sent as a reply to a requestor when an API call is triggered.

 Actual behavior: Observe that an updated message is sent as a reply to a requestor when an API call is triggered.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1893104

</td><td>

In Now Assist Multi-Turn Catalog Ordering, the 'Data/Time' type variable isn't showing the current time, but as 00:00AM in Virtual Agent for non-English language mode

</td><td>

The 'Data/Time' type variable should be displayed as the current time across all language modes.

</td><td>

1.  Activate the following plugin/store apps to last version:
    1.  UXC Generative AI \(sn\_uxc\_gen\_ai\)
    2.  Now Assist for IT Service Management \(sn\_itsm\_gen\_ai\)
    3.  I18N: Japanese Translations \(com.snc.i18n.japanese\)
2.  Navigate to **Conversational Interfaces** &gt; **Assistants**.
3.  Enable Now Assist for Virtual Agent with 'Now Assist Multi-Turn Catalog Ordering' skill active in the Service Portal.
4.  Create a catalog item with one 'Data/Time' type variable.
5.  Navigate to **AI Search Index** &gt; **Indexed Sources**.
6.  Open 'Name='Catalog Item Table'.
7.  Select **Index All Tables** so that the newly created catalog item will be included in the Virtual Agent search via AI Search.
8.  Switch to the Japanese language mode after the reindex is done.
9.  Navigate to Service Portal.
10. Open Virtual Agent.
11. Search the newly create catalog item.
12. Start the request.
13. Check the 'Data/Time' type variable display.

 Expected behavior: The 'Data/Time' type variable should be displayed as the current time, which is the same in the English language mode.

 Actual behavior: The 'Data/Time' type variable displays as 00:00AM in the Japanese language mode.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1896390

</td><td>

Console errors for va\_web\_client API failures are displayed when launching a chat in the CSM portal and Engagement Messenger

</td><td>

Two console errors related to va\_web\_client are observed: '/api/now/ va\_web\_client\_settings /get\_va\_web\_ client\_settings' api results 403 error' and '\[SNAnalytics\] Invalid property name'. Console errors shouldn't be displayed and chat functionality should work as expected.

</td><td>

1.  Log in to an instance.
2.  Navigate to CSM portal or Engagement Messenger.
3.  Launch Virtual Agent chat/start a chat.
4.  Observe the browser console.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1896591

</td><td>

Emoji panel loading is slow in Windows OS

</td><td>

Chrome and Edge browsers freeze for one minute after the user selects an Emoji icon in the Virtual Agent Web Client.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1897932

</td><td>

NAVA isn't picking interaction context variables when enhanced chat is turned on

</td><td>

Account and contact fields aren't populated on an interaction record. Note that the issue isn't reproducible when enhanced chat is turned off in Virtual Agent.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1911025

</td><td>

The 'Chats' panel header title is empty for both requestor and fulfiller

</td><td>

In another scenario, the unread conversation count badge should be enabled by default for requestor clients.

</td><td>

1.  Open Dispatcher Workspace.
2.  Toggle to the 'Chats' panel by selecting the hamburger icon on the header.
3.  Notice that the 'Chats' panel header title is empty by default.
4.  Update the 'Left Panel Header Label' in the branding record to the correct value.

 Expected behavior: Even without updating the **Branding record** field, the 'Chats' panel header should have a default value.

 Actual behavior: The default value for chats header is empty.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1912866

</td><td>

Initiating a live agent in the same conversation right after canceling a live agent request doesn't work

</td><td>

 

</td><td>

1.  Navigate to Dispatcher Workspace \(DW\).
2.  Use 'Contact live agent' to connect to a live agent.
3.  Cancel the request.
4.  Request a live agent again.

 Expected behavior: The live agent should move to a 'Request' state.

 Actual behavior: Nothing happens.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1912902

</td><td>

The **Close** button on the People card in 'Sources' doesn't close the card

</td><td>

 

</td><td>

1.  Navigate to Now Assist Virtual Agent \(NAVA\).
2.  Enter the utterance, 'Who is Abel Tuter'.
3.  Select **Citation** after getting the response in 'Sources'.
4.  Select **X** to close the People card.

 Expected behavior: The People card should close.

 Actual behavior: The People card stays open.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1912919

</td><td>

New messages below the indicator exhibits old behavior and an outdated arrow

</td><td>

 

</td><td>

1.  Navigate to **sys\_cs\_branding\_setup.list**.
2.  Enable new messages below the indicator.
3.  Navigate to **Now Assist Virtual Agent \(NAVA\)**.
4.  Send an utterance with a long response.

 Expected behavior: The new message indicator is an arrow and shows text when hovering over it.

 Actual behavior: The new message indicator has the old behavior 'new message below' text with arrow.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1915596

</td><td>

Web search ends if the user sends the 'End' emoji in a standard chat

</td><td>

When the user sends the 'End' emoji, the Virtual Agent responds by ending web search. After a page refresh, the web search globe icon is still enabled. If the user selects the globe icon again, web search doesn't end.

</td><td>

1.  Navigate to **/SP**.
2.  Start a standard chat.
3.  Start web search mode.
4.  Send the 'End' emoji.

 Expected behavior: The emoji doesn't cause web search to end. The user retains normal functionality in the Virtual Agent.

 Actual: The Virtual Agent responds by ending web search. After a page refresh, the web search globe icon is still enabled. If the user selects the globe icon again, web search doesn't end.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1920026

</td><td>

Proactive trigger topics don't launch

</td><td>

 

</td><td>

1.  Set up proactive triggers on the instance so there are topics that launch when selected.
2.  Navigate to the portal where proactive trigger is configured.
3.  Launch the associated topic when proactive trigger is received.

 Expected behavior: The topic should launch in Dispatcher Workspace.

 Actual behavior: The topic doesn't launch, and the user just sees the welcome message.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1920035

</td><td>

The 'VTT' icon isn't available in previous model of Now Assist Portal \(NAP\)

</td><td>

The issue occurs when the user switches from the new model to the previous model with VTT turned on.

</td><td>

1.  Install any of the BU skills.
2.  Turn on NAP with VTT.
3.  Turn on the microphone from the browser preferences.
4.  Toggle 'on' accessibility settings.
5.  Select the **NAP icon**.
6.  Ensure the VTT icon is available in the new model.
7.  Change the model to old model \(Self service modal dialog\).
8.  Refresh the page.

 Expected behavior: The VTT icon should be available.

 Actual behavior: The VTT icon is not available in the old model of NAP when the user switches from the new model to old model with VTT enabled.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1921096

</td><td>

When an agent has a topic using the 'file upload' node, it triggers some odd UI in Web Client input

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Navigate to /esc portal.
3.  Enter: 'Summarize meeting into actionable items'.
4.  When it asks to upload a file, upload the attachment.

 Expected behavior: 'Executing Agent Meeting Action Item Agent' should be triggered by the utterance.

 Actual behavior: The input field displays 'Processing...' and the uploading icons.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1921129

</td><td>

Citations for skills are still available once skill execution starts on Now Assist Portal \(NAP\)

</td><td>

 

</td><td>

1.  Turn on Agentic for NAP.
2.  Navigate to NAP.
3.  Type 'summarize a record'.
4.  After skill execution starts, check the citation link.

 Expected behavior: The citation link is turned off and selecting it doesn't trigger any action.

 Actual behavior: The citation link is available to select and runs into an error if selected.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1922217

</td><td>

ServiceNow Chat.open isn't opening Portable Virtual Agent

</td><td>

 

</td><td>

1.  Implement the 'ServiceNowChat Third Party' API.
2.  Call serviceNowChat.open\(\).

 Notice that the chat never opens.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1922858

</td><td>

A new chat is created for the same search results when a user selects 'Go to Search Results'

</td><td>

It shouldn't create a new conversation when selecting the search icon from the feedback panel.

</td><td>

1.  Navigate to Dynamic Window \(DW\).
2.  Type 'I want dell XPS 13'.
3.  Navigate to the bottom of the results.
4.  Select the **Go to Search Results** icon.

 Expected behavior: A new chat shouldn't be created in DW.

 Actual behavior: A new chat is created for the same search.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1923459

</td><td>

Context variables aren't accessible in the enhanced chat

</td><td>

Context variables aren't accessible in the enhanced chat, whereas they are accessible in the standard chat using either 'vaContext.liveagent\_' or 'vaVars.liveagent\_'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1924539

</td><td>

Users get an empty message when asking for Abel Tuter's assets

</td><td>

 

</td><td>

1.  Open a znowassiststable instance with September apps.
2.  Navigate to /esc.
3.  Query: 'what are able tuter's assets'.

 Expected behavior: Virtual Agent should return a list of Abel Tuter's assets.

 Actual behavior: Users get an empty message in Virtual Agent.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1925994

</td><td>

Engagement Messenger isn't loading chats after upgrading Yokohama

</td><td>

The chat box in Engagement Messenger is blank, and loads no content. The errors occurs, 'SecurityError: Failed to read a named property 'uxfIntentLibrary' from 'Window'.

</td><td>

1.  Launch the Engagement Messenger.
2.  Select the chat box.
3.  Observe that the chat box is blank.
4.  Navigate to a Yokohama instance.
5.  Navigate to Agentic Portal in a separate browser tab, but don't attempt to log in.
6.  Open the dev console.
7.  Execute the script.
8.  Execute the code.
9.  Select the chat bubble that appears after the code finishes executing.

 Expected behavior: The chat loads with content.

 Actual behavior: The chat load is blank and a security error appears in console.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1927881

</td><td>

Virtual Agent topic options for dynamic choice input aren't displayed in Now Assist Portal \(NAP\)

</td><td>

For dynamic choice input, the options aren't appearing for the first time on NAP. If users enter a random string that isn't one of the expected options, it repeats the question and then displays the options on the second or third attempt.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1928501

</td><td>

Context variables are not accessible in the enhanced chat

</td><td>

The context variables are not accessible in enhanced chat, but they are accessible in standard chat using either 'vaContext.liveagent\_' or 'vaVars.liveagent\_'.

</td><td>

 

</td></tr><tr><td>

Workflow Studio

 PRB1844972

</td><td>

Files are missing from AI search indexes after installing NAFC 27.1.0

</td><td>

After installing NAFC 27.1.0 in Yokohama, files related to AI semantic search are skipped in the WFS plugin progress and the records don't appear in the tables.

</td><td>

 

</td></tr><tr><td>

Workflow Studio

 PRB1922333

</td><td>

A Workflow Studio upgrade message doesn't display for non-admins

</td><td>

 

</td><td>

1.  Log in to an instance without the latest Workflow Studio version.
2.  Navigate to Workflow Studio homepage.

 Expected behavior: The banner displays that a new version is available.

 Actual behavior: The banner doesn't display.

</td></tr><tr><td>

Workflow Studio

 PRB1922988

</td><td>

A banner message to install the latest PAD should be displayed on Workflow Studio

</td><td>

To inform users to install the latest PAD when the new Now Assist for Platform version is available, there should be a banner message in Workflow Studio advising them to upgrade PAD for the Agentic Playbook feature.

</td><td>

1.  Navigate to a Zurich instance.
2.  Install Workflow Studio.
3.  Launch Workflow Studio.

 Expected behavior: There's an info banner message to install the latest PAD to get an Agentic Playbook feature.

 Actual behavior: No banner is available.

</td></tr><tr><td>

Work Order Management

 PRB1912592

 [KB2266119](https://hi.service-now.com/kb_view.do?sysparm_article=KB2266119)

</td><td>

There's an incorrect info message for work order tasks

</td><td>

Currently, the displayed info message is 'Task WOTXXXXXXX Closed successfully. Work Order \(WOXXXXXXX\) is also closed'. This should be 'Task WOTXXXXXXX Closed successfully.' since there's still another task open for the work order.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1914183

</td><td>

Google Maps API doesn't work when calculating travel time in Field Service Management when changing the system date format

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1917364

</td><td>

Update the SMCoreConfig CacheManager. getSMConfig API to make it backward compatible with latest SMConfigurationHelper code

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1920024

</td><td>

Team Calendar isn't displaying events

</td><td>

 

</td><td>

1.  Impersonate as a manager.
2.  Create an event to make sure that an event is there.
3.  Check the Team Calendar for events.

 The created event isn't displaying.

</td></tr><tr><td>

Work Order Management

 PRB1921026

</td><td>

'Status' field choices differ from those on the 'Work Order' form view when setting up a Work Order Task \(WOT\) template

</td><td>

When setting up a WOT template, the choices that appear for the Status \[state\] field differ from the choices that appear on the WO form view. Also, when setting up a WO template, choices don't appear for the 'Service Request Type' field.

</td><td>

1.  Navigate to the list of Work Order Models \[cmdb\_workorder\_product\_model\].
2.  Select the **GE ULRICH ASSEMBLY** model.

 Notice that under 'Request Information', 'Service Request Type' doesn't provide selections. Also, notice that under 'Task information', the 'Status' choices differ from the choices that are available on the WOT form view.

</td></tr><tr><td>

Work Order Management

 PRB1925821

</td><td>

A Dispatcher Workspace group filter displays no results when a wm\_dispatcher persona accesses the workspace

</td><td>

Users with the 'wm\_dispatcher' role were unable to query the 'dispatch\_group' field on the 'sm\_m2m\_ group\_dependency' table due to a missing access.

</td><td>

1.  Impersonate a user.
2.  Log in to Dispatcher Workspace \(now/cwf/agent/dispatch\).
3.  Select the 'Assignment group' filter.
4.  Expected behavior: The 'Assignment group' filter should populate values correctly.
5.  Actual behavior: Observe that there are no results even when they have assignment groups configured.

</td></tr><tr><td>

Workplace Case Management

 PRB1921823

</td><td>

Moving bars aren't working in scenario planning

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Workplace Case Management

 PRB1927638

</td><td>

Moving bars aren't working in Scenario Planning

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Workplace Central

 PRB1914686

</td><td>

'Add/Change allocations from map-based administration' isn't working in Zurich instances

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Workplace Central

 PRB1919180

</td><td>

When selecting 'Create schedule', it takes more time open the 'Schedule' page and sometimes it doesn't open

</td><td>

When the user selects 'Create Schedule' it should open directly, and they should be able to view the schedule before publishing the plan. This issue occurs on new instances from Xanadu to Zurich, and has been observed in existing instances as well.

</td><td>

 

</td></tr><tr><td>

Workplace Maintenance Management

 PRB1919220

</td><td>

Unable to copy the schedule because the list appears empty when it's selected for Maintenance Plans

</td><td>

When a schedule is previously created for a Maintenance Plan, it can't be copied over to a new plan because the list appears empty and the previously created plan doesn't appear.

</td><td>

1.  Create a Maintenance Plan.
2.  Navigate to **Workspaces** &gt; **Workplace Central** &gt; **Preventive Maintenance icon**.
3.  Navigate to **All Plans** &gt; **New**.
4.  Give any plan name.
5.  Choose a start date in the future.
6.  Choose a end date in the future.
7.  Select the location.
8.  Select any building.
9.  Select **Next**.
10. Select one maintenance item.
11. Select **Next**.
12. Select **Create schedule**.
13. Create schedules with the following:
    1.  Schedule: 1
    2.  Name: Schedule 1
    3.  Trigger: Duration
    4.  Trigger type: Interval
    5.  Repeat: Days - 1
14. Select **Save**.
15. Select **Publish**.
16. Create Plan 2 with the previous the steps, up to the maintenance items selection.
17. Do not select **Create Schedule**.
18. Attempt to copy the schedule.

 Notice that the previously created schedule does not appear.

</td></tr><tr><td>

Workspace App Shells

 PRB1912366

</td><td>

Empty white space is showing for the interaction type 'Phone' for the Voice Interaction Page

</td><td>

 

</td><td>

1.  Navigate to the **CSM/FSM Configurable Workspace**.
2.  Create new interaction with the type 'Phone'

 Expected behavior: The white space shouldn't show up.

 Actual behavior: The empty white space shows up.

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB1891523

</td><td>

The databoard isn't working for prod and sub prod glide instances

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


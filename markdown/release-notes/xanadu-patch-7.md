---
title: Xanadu Patch 7
description: The Xanadu Patch 7 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-03-12"
reading_time_minutes: 49
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 7

The Xanadu Patch 7 release contains important problem fixes.

-   **Xanadu Patch 7 was released on March 12, 2025.**
    -   Build date: 03-06-2025\_0935
    -   Build tag: glide-xanadu-07-02-2024\_\_patch7-02-27-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X07.00.xlsx).

## Overview

Xanadu Patch 7 includes 164 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp7.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 7 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 7, refer to [KB1925102](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1925102).

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

Approvals

 PRB1845668

 [KB1810362](https://hi.service-now.com/kb_view.do?sysparm_article=KB1810362)

</td><td>

Multi-Level approval skips steps due to race conditions

</td><td>

Overlapping transactions on the sc\_req\_item table cause race conditions, allowing approval steps to be skipped.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1688076

 [KB1585842](https://hi.service-now.com/kb_view.do?sysparm_article=KB1585842)

</td><td>

In Vancouver, changing the rows per page in UI Builder results in security restraints messages

</td><td>

When a user changes the rows per page on Tokyo or Utah and refreshes, it resets to 20 per page and this error doesn't appear.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1804211

 [KB1710147](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710147)

</td><td>

A list is failing to load due to Access Control List \(ACL\) failures

</td><td>

Lists do not load, and a response is returned in the call for the record list composite data broker.

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

 PRB1850716

</td><td>

There should be a check for customization before the removal of the snc\_internal ACL role from a set of ACLs

</td><td>

If a snc\_internal acl role record has an entry in the sys\_update\_xml table, then the record shouldn't be deleted.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1843408

</td><td>

If a user deletes drafts after sending mail, the last sent email disappears in the filtered 'Activity Stream' section

</td><td>

 

</td><td>

1.  Open an email page record.
2.  Select the 'Email' tab.
3.  Compose an email with valid recipients.
4.  Select the **Send** button.
5.  Once the email history is updated, select the 'Email drafts' icon and delete all drafts.
6.  Close the dialog/modal.

 Expected behavior: Sent email logs should be displayed on the email's history.

 Actual behavior: The last sent email has disappeared from the email's history.

</td></tr><tr><td>

Activity Stream

 PRB1858894

</td><td>

Application Programming Interface \(API\), ServiceNow AI Platform, and GraphQL is slow due to the Table Cleaner being throttled, causing heavy replication lag

</td><td>

API, ServiceNow AI Platform, and GraphQL calls are slow specifically because of the Table Cleaner on sys\_activity shards. ​Using Instant Alter added an index, and as a result, all records were replicated with the load causing replication lag. When replication lag is detected, Table Cleaners are throttled, which can exacerbate the amount of data that is being replicated and cause timeouts. Timeouts are caused by the Table Cleaner running synchronously in the Activity Stream load request.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1857820

</td><td>

Agent Outside Workspaces that use OpenFrame soft phone are set to an 'Offline' presence state within a minute after the agent moves to an available state

</td><td>

If an agent isn't also on a workspace, the presence reverts to 'Offline' within about a minute. Since the agent is using OpenFrame to manage capacity, it shouldn't automatically revert to 'Offline'. The issue occurs after an Xanadu upgrade.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1846351

</td><td>

Audio notifications don't play intermittently when the browser has 'Allow All Auto-Play' configured

</td><td>

On a Safari browser, when the user doesn't allow the Auto-Play for the ServiceNow site, audio notifications intermittently don't play for an agent. This is applicable for inbox and conversation notifications. For example, if an agent doesn't hear an audio notification for an incoming inbox notification, it's possible the following conversation's audio alert to play or not play. Once audio notifications begin to play, proceeding audio notifications usually play. The audio state can be 'interrupted'.

</td><td>

1.  In a Safari browser, as an agent, open Service Operations Workspace.
2.  Change the status to 'Available'.
3.  Using a Chrome browser, impersonate a requester.
4.  Turn off audio notifications in the web client.
5.  Initiate a chat and attempt to connect to a live agent.
6.  In the Safari browser, as an agent, accept the incoming work item.

The audio notification plays.

7.  From the Chrome browser, as a requester, send a message to ensure an audio notification plays on the agent's side.
8.  In the same Safari browser, as an agent, open a new tab with a random URL. Keep this as the active tab and workspace tab in the background.
9.  In Chrome, as the requester, wait for the timeout reminder and observe if the audio notification plays.
10. In Chrome, as the requester, send a message.

Observe at this time, the audio notification stopped working, even though the console log says it successfully played audio.


</td></tr><tr><td>

Agile Development

 PRB1845010

</td><td>

Add the spm\_agile\_common\_user role to the plannedtask.\* ACL to view a rm\_story form

</td><td>

A spm\_agile\_common\_user should be able to have CURD access on the rm\_story table.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1827624

</td><td>

A search doesn't return any results

</td><td>

After configuring the search profiles and the user, the search results don't appear, but if the **location.state** field is changed for the user, search results appear.

</td><td>

1.  Download and import the search profiles.
2.  Ensure the search profiles were uploaded.
3.  Find the 'Location boost' risk intelligence report.
4.  Select the 'Location boost' risk intelligence report.
5.  Navigate to **positive**.
6.  Change the match field from 'location.city' to 'location.state'.
7.  Publish the profile.
8.  Set up a user.
9.  Assign the user the knowledge\_admin and ITIL roles.
10. Ensure the values in the **company** field are empty.
11. Change the **location** field to 'California'.
12. Select **Save**.
13. Select the value **California**.
14. Ensure that the column 'state' is 'California'.
15. Ensure that the 'name' is 'California'.
16. Run this query 'Employee benefits?' on Global, Service Portal, and Now Assist Virtual Agent.
17. Navigate to 'sys\_generative\_ai\_log.list'.
18. Check the response.

 Expected behavior: The Knowledge Base article, 'Employee Benefit - US' should be at the top.

 Actual behavior: The search results don't appear, but if the user changes the **location.state** field, the Knowledge Base article appears.

</td></tr><tr><td>

AI Search

 PRB1838451

</td><td>

AisJournalFieldPeekAhead throws a NullPointerException \(NPE\)

</td><td>

Leaving the value empty when adding a journal value column to kb\_knowledge throws an NPE.

</td><td>

1.  Add a journal value column to kb\_knowledge.
2.  Leave the value empty.
3.  Attempt to ingest the document.

 Observe the NPE.

</td></tr><tr><td>

AI Search

 PRB1852129

</td><td>

Selecting a search result in the Portal adds the parameter 'SearchTerm', leading to a 404 error

</td><td>

With AI Search enabled, searches in the Portal lead to a '404 page not found' error. This occurs when search results that are external links are presented in the search results. When a search result is selected, an additional parameter is added to the URL '&amp;searchTerm=', which causes the 404 error.

</td><td>

1.  Navigate to a Xanadu instance.
2.  Add an external link to the AI Search source.
3.  Navigate to the Employee Portal.
4.  Search for the external link.
5.  Select the top search result.
6.  Observe that 'searchTerm=' is added to the URL.

 Expected behavior: The user lands on the external link after selecting the search result.

 Actual behavior: The user lands on an page with the error message '404 Page not found'.

</td></tr><tr><td>

AI Search

 PRB1852402

 [KB1909618](https://hi.service-now.com/kb_view.do?sysparm_article=KB1909618)

</td><td>

SearchAnalyticsService. pruneSearchSignalEvents occasionally purges events with the wrong application ID

</td><td>

The sysauto\_script scheduled job, 'Prune Search Signal Events', may cause sys\_search\_events and its related tables to be incorrectly pruned.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1857237

</td><td>

Images aren't returned for Now Assist actions on Service Portal

</td><td>

 

</td><td>

1.  On a Yokohama instance with Now Assist for Search 10.0.14, navigate to Service Portal.
2.  Search for 'Apple' or 'Laptop'.

 Expected behavior: Images should be returned for the Now Assist actions Genius Results.

 Actual behavior: Notice that the images aren't coming back for Genius Results.

</td></tr><tr><td>

Application Install Engine

 PRB1836818

</td><td>

A parent application installs successfully despite missing dependencies

</td><td>

A parent application \(for example, Generative AI Controller 9.0.1-Snapshot\) is installed successfully even though its dependencies \(for example, Microsoft Azure AI Speech Spoke\) were not installed during the process

</td><td>

1.  Attempt to install a parent application with known dependencies.
2.  Simulate a scenario where the dependency \(for example, Microsoft Azure AI Speech Spoke\) fails to install.

 Observe that the parent application still installs, creating a record in the sys\_store\_app table, but dependencies remain missing.

</td></tr><tr><td>

Attachments to Records

 PRB1849752

 [KB1885864](https://hi.service-now.com/kb_view.do?sysparm_article=KB1885864)

</td><td>

There's an issue with archive table clean-up using the 'PurgeOrphanAttachments' job

</td><td>

There's an issue that may result in the unintentional removal of records from the sys\_attachment table under specific conditions. The issue may impact instances on Washington DC and later releases.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1827858

</td><td>

Ship RCA for a KB search in the target scope

</td><td>

 

</td><td>

1.  Set up Now Assist for HR.
2.  Enter a query in Virtual Agent: 'Tell me about parental leave policy' or any other KB related query.

 Expected behavior: The numbers should be visible and clickable.

 Actual behavior: The numbers aren't displayed in the KB result.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1850236

</td><td>

RCA issues with tuition reimbursement AI agents

</td><td>

There are RCA records that are needed in app-hr to let tuition reimbursement request AI agents to function.

</td><td>

 

</td></tr><tr><td>

Case Card Component for HRSD Agent Workspace

 PRB1828093

</td><td>

Tooltips aren't working

</td><td>

After upgrading to Xanadu, the tooltips stopped working on all the workspaces.

</td><td>

1.  Access any Xanadu instance that was upgraded from Utah or Washington DC.
2.  Navigate to sys\_ux\_lib\_asset\_list.
3.  Observe if the instance has the file sys\_ux\_lib\_asset\_ 4eca5b08258a2192915e9d083b0bf32e.xml.
4.  Open any workspace.
5.  Observe that there's no tooltip.
6.  Remove the file mentioned on step 3.

 Observe that the tooltips are working.

</td></tr><tr><td>

Client Scripts

 PRB1794520

</td><td>

Newly populated **on\_hold\_reason** field data doesn't display for a duplicate tab

</td><td>

The behavior is different from the native view and the Service Operations Workspace view.

</td><td>

1.  Log on to any instance.
2.  Navigate to 'change\_request.do' and populate the **assignment\_group** field.
3.  Save the form.
4.  Select the **Request Approval** UI action.
5.  Duplicate the tabs so users have the change request open on two tabs - Tab A and Tab B.
6.  In Tab A, select the 'on\_hold' checkbox.

Observe that the **on\_hold\_reason** field appears.

7.  Enter '123' in the **on\_hold\_reason** field.
8.  Save the form.
9.  Move to Tab B.

Observe that the 'on\_hold' checkbox is now ticked, but the **on\_hold\_reason** field doesn't have '123' populated.

10. Refresh Tab B.

Observe that '123' is now populated.


</td></tr><tr><td>

CMDB Query Builder

 PRB1830100

</td><td>

The 'Dynamic CI' group is missing a few CIs

</td><td>

The QueryBuilderOutput. getCISysIdsFromQBResults\(\) loop has an issue.

</td><td>

1.  Create a QB query \(can use only one node\) to qualify a few thousand CIs.
2.  Run the query entirely by selecting the **Load All Results** button.
3.  Note the count of CIs.
4.  Create a CMDB Group and use the QB query from step 1 into this group.
5.  Create a Dynamic CI Group and use the CMDB Group from step 4 to populate it.

Give it a minute or so to associate CIs with this DCG before going to the next step.

6.  On the 'Form' page of this Dynamic CI Group, select **View Service CIs**.
7.  Note the count of CIs.

 Expected behavior: The count of CIs from step 7 should match the count of CIs from step 3.

 Actual behavior: The count of CIs from step 7 doesn't match the count of CIs from step 3.

</td></tr><tr><td>

Code Signing

 PRB1857413

</td><td>

Signatures created by 'Signing' jobs have the **update\_name** field empty

</td><td>

 

</td><td>

Run the 'Signing' job to generate a signature for records.

 Excepted behavior: Generated signatures should populate the **update\_name** field

 Actual behavior: The **update\_name** field is empty for a generated signature. This prevents records from Git check-in and the 'Publish to App' repo.

</td></tr><tr><td>

COE Legacy Family Component

 PRB1850825

</td><td>

Moving the resizable panes handle quickly doesn't work on a configurable page with an iFrame component

</td><td>

If users add an iFrame component in the tab sidebar, then it causes an issue when trying to adjust the size of the panes in the workspace.

</td><td>

 

</td></tr><tr><td>

Conversational Interfaces

 PRB1810492

</td><td>

A module key isn't present in the ms\_teams\_crypto\_module, but the key is present in oauth\_entity, which is causing migration issues

</td><td>

 

</td><td>

Create a data migration from security jobs.

 The migration fails because a record from the oauth\_entity table is skipped. The oauth\_entity had a key but the respective crypto\_module module key doesn't exist.

</td></tr><tr><td>

Customer Service Management

 PRB1855041

</td><td>

Unable to create an email draft in an application scope

</td><td>

The sys\_email\_draft table has table-level access limitation. Only 'Can Read' is allowed in the application scope.

</td><td>

1.  **AI Agent** &gt; **Testing**.
2.  Select the AI agent 'CSM Response Handler'.
3.  Enter the task detail as:
    1.  record\_table = 'sn\_customerservice\_case'
    2.  record\_sysid = '5078cc9a2be71210f980f0aef291bf0b'
    3.  email\_reply\_content = 'We can't complete this case until missing fields and missing documents are added'

 Observe the email response tool 'Draft Email' returns an error message 'Email draft is failed created'.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1808866

</td><td>

Inefficient chunk production for a document ID type reference

</td><td>

For a document ID type reference, the 'Unreferenced Record Cleaner' producer first computes the list of unique table names and then produces the chunks. The SQL query to compute the list of unique table names can timeout leading to no chunks being produced.

</td><td>

1.  Create a large table with a document ID type reference.
2.  Have a large number of unique table names in the table **name** field.
3.  Set the SQL timeout \(sysrule\_quota\) to a small value.

 Observe that 'Unreferenced Record Cleaner' producer times out computing the list of unique table names, thus producing no chunks.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1820795

</td><td>

The DMJob allows the restarting of timed out DM runs

</td><td>

This issue was seen in an unreferenced record cleaner cleanup. Runs are left in a 'processing' state.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1840970

</td><td>

Monthly/Yearly scheduled jobs named 'Physical Table Stats Aggregator/Gatherer' causes slow CPU and instance responses

</td><td>

This problem manifested primarily on demo instances that have more than 300 DBIs, but it isn't necessarily isolated to demo hosts.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1777198

</td><td>

When upgrading, the fix script does not update records

</td><td>

 

</td><td>

Run an upgrade.

 Notice that records in sys\_query\_rewrite have the **Engine** field, but no value in it.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1807483

</td><td>

Track the number of total/dropped messages per SqlType

</td><td>

Currently, the number of dropped messages is already being tracked and the stats are exposed in xmlstats. When a capture is run, one can hit the xmlstats to get the state/health of the capture, which includes the number of dropped messages. However, the dropped messages are not tracked per SqlType, which makes it impossible to know the percentage of the dropped messages.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1834412

</td><td>

Make JDBC driver properties load dynamically from the DB so nodes don't need to be bounced

</td><td>

This property currently requires updating file properties and bouncing of nodes, which is hard on instances.

</td><td>

Update the sys\_properties table with glide.db.postgresql. jdbc.largeResult SetProtectionMethod = disk.

 Observe JDBC driver still uses stream mode.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1834816

</td><td>

Send txn-level SQL execution time in micros

</td><td>

Currently, TransactionMessage.sql\_time is being sent to indicate the total SQL time for the transaction. The value comes from Transaction\#getSQLTime and the unit is in milliseconds. The total transaction-level SQL time should be measured and sent in microseconds.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1763563

</td><td>

**SNCVARCHAR** fields are created as an unbounded length, but should be set to 16 MB

</td><td>

 

</td><td>

1.  Create a payload larger than 16MB.
2.  Insert into a text field set to more than string 255.

</td></tr><tr><td>

Developer Sandboxes

 PRB1788330

</td><td>

Standby nodes are incorrectly elected as controller/sandbox nodes over primary nodes

</td><td>

The available sandbox count should only count primary nodes \(seen from sys\_cluster\_state\). Only primary nodes should be assigned DSB nodes. If there are no more primary nodes left to assign sandboxes, then the available sandbox count should be 0 and a sandbox shouldn't be able to be created.

</td><td>

1.  Create a sandbox instance with many nodes, some as standby and others as primary.
2.  Increase the sandbox controller count.
3.  Check the expected behavior below, and repeat increasing the count as needed.

 Expected behavior: Each time the count is increased, an available primary node is chosen as the controller node.

 Actual behavior: Sometimes a standby node is chosen as the controller node over an available primary node.

</td></tr><tr><td>

Discovery

 PRB1804025

</td><td>

During Shazzam, updates should be batched to discovery\_status.started

</td><td>

A lot of updates in a short time causes a performance issue. In this case, batch means to change the started count only once for all probes that are to be launched.

</td><td>

1.  Run a discovery using RaptorDB.
2.  Observe the performance.

</td></tr><tr><td>

Discovery

 PRB1824650

</td><td>

Smart content for the November release should be true upped

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1843022

</td><td>

Simple Network Management Protocol \(SNMP\) GetTable commands during pattern execution no longer exit the pattern when errors occur that exceed the limit

</td><td>

SNMP GetTable commands no longer exit pattern when errors occur that exceed the limit, and the failure count continues to increase.

</td><td>

1.  Setup a Discovery.
2.  Run a Discovery against an SNMP device that returns errors running 'getTable' requests.

Ensure that this sets the MID properties 'mid.sa.snmp.allowable\_failures\_before\_success' and 'mid.sa.snmp.allowable\_failures\_after\_success' to 0.

3.  Check the logs after the Discovery.
4.  Observe messages such as, 'SNMP command failure count is 1 and allowable failures before success is 0. Exiting pattern execution'.

 Expected behavior: The pattern should exit after the first failure.

 Actual behavior: The pattern doesn't exit, and the failure count continues to increase on subsequent errors.

</td></tr><tr><td>

Discovery

 PRB1860779

</td><td>

True-up licensing app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Dynamic Translation for Virtual Agent

 PRB1853153

</td><td>

Virtual Agent responses are in English when Dynamic Translations are on

</td><td>

This impacts Brazilian Portuguese, French, German, Italian, Japanese, and Spanish.

</td><td>

1.  Ensure Dynamic Translation is enabled and Native LLM is turned off.
2.  Set the language session to Japanese.
3.  Navigate to 'https://&lt;instance name&gt;.service-now.com/sp'.
4.  Open the Virtual Agent chatbot.
5.  Request for '社内在庫管理' and, once the item is found, start the request.
6.  Begin entering Serial ID item inputs.
7.  Continue responding to any additional questions prompted by the chatbot.
8.  Observe the language of the chatbot's responses.

 Expected behavior: All chatbot responses, including those for Serial ID item inputs and other user-provided answers, should be entirely in Japanese.

 Actual behavior: The chatbot responds in English for every input provided by the user, including Serial ID item inputs and any other follow-up responses in the process.

</td></tr><tr><td>

Dynamic Translation

 PRB1847469

</td><td>

A Spanish user runs skills and gets a response in English

</td><td>

 

</td><td>

1.  Set up Dynamic Translation.
2.  Impersonate an agent.
3.  Change the language to Spanish.
4.  Type or select a skill pill.

 Expected behavior: The user gets the entire response in Spanish

 Actual behavior: The user gets a response in English and Spanish.

</td></tr><tr><td>

Edge Encryption

 PRB1844471

</td><td>

After a Vancouver upgrade, a scheduled upgrade is blocked from appearing on a Washington DC or Xanadu's instance for a Vancouver proxy

</td><td>

The **Schedule** button doesn't appear on the edge proxy page, so users are unable to schedule an upgrade.

</td><td>

 

</td></tr><tr><td>

Employee Center

 PRB1734350

</td><td>

Portal Utils prediction methods should respect missing or inactive HR AI configuration records

</td><td>

HR\_MLPortalUtilsSNC has two methods, 'getSimilarProfiles' and 'getRecommendedArticles' that retrieve HR AI configurations before trying to predict matches. getRecommendedArticles doesn't check for an HR AI configuration. It could be useful for a user to be able to turn off this functionality if they don't wish to train AI data and don't want to see the 'Solution GlideRecord does not exist, please train the solution definition' repeated in the system error logs.

</td><td>

1.  Log in to the instance.
2.  Check system logs for the message 'Solution GlideRecord does not exist, please train the solution definition' from the sn\_hr\_sp source.

</td></tr><tr><td>

Employee Center

 PRB1792636

</td><td>

Rich text content isn't translated on the ESC portal 'Get Support' widget

</td><td>

It still displays English content inside for rich text content.

</td><td>

 

</td></tr><tr><td>

Employee Center

 PRB1817222

</td><td>

Level 2 subcategories don't follow a tree form in the 'Categories' widget

</td><td>

The 'SC Categories' widget doesn't display the proper indentation for the Level 2 categories. The tree structure of the second level is the same as the parent and this creates confusion of where the categories end.

</td><td>

1.  Navigate to any Washington DC instance.
2.  Navigate to esc?id=sc\_category.
3.  Select the second level catalogs.

 Expected behavior: The second level content under the tree should get aligned similarly to the first level.

 Actual behavior: The content under the first level is properly aligned below the tree. The second level content isn't aligned properly under the tree.

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB1766037

</td><td>

The 'Search within Topic' page doesn't return results in the Employee Center when the topic name has special characters

</td><td>

The value of the **\_kb\_knowledge.topic \_level\_2\_s** field on documents under the 'Compensation \(Base/Incentive/Stock\)' topic is actually 'Compensation Base Incentive Stock'. The special characters were removed at indexing. The facetFilters added by the 'Topic Content' sp\_widget don't get the same treatment. The query has a filter looking for documents where the field's value is 'Compensation \(Base/Incentive/Stock\)' when the actual value is 'Compensation Base Incentive Stock'.

</td><td>

 

</td></tr><tr><td>

External Triggers

 PRB1848664

</td><td>

Change the spoke sys\_id to the spoke ID in the definition for external triggers telemetry

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Field Service Management

 PRB1827771

</td><td>

Sm\_config records are updated randomly with new versions

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1825217

 [KB1709497](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709497)

</td><td>

When applying inline scripting to pass the value in an input of a dynamic template, it's not working, and the field appears empty

</td><td>

When users create a new action from scratch with one input of a dynamic template and apply inline scripting to pass the value to this input in the flow, it doesn't work.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1843277

</td><td>

Users get an error when creating a flow from Table Builder or from logic and automation on a partially upgraded instance

</td><td>

An error is thrown: 'java.lang.NullPointerException: Cannot invoke "com.glide.db. PrimaryKey.addQuery \(com.glide.db. meta.Query, String\)...'

</td><td>

1.  Provision an instance having Washington DC installed.
2.  Partially upgrade it to Yokohama.
3.  Navigate to AES.
4.  Create an app or use existing an app.
5.  Create a table in it.
6.  Edit the table.
7.  Create a flow in it.

 Expected behavior: The user must be able to create the flow in it.

 Actual behavior: The user is getting an error.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1844406

</td><td>

The IntermediateFlow. processIntermediateFlow\(\) API doesn't work properly with the trigger type 'sla\_task'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1850367

</td><td>

Enable a generation\_source value other than 'text2flow' in Flow Generation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC Platform Plugins

 PRB1789050

</td><td>

When importing policy text, images don't render and there's misalignment

</td><td>

In Compliance Workspace with O365 Integration enabled, 'Import Policy Text - Images' don't render and there's misalignment.

</td><td>

1.  Impersonate a user.
2.  Open a policy in the Compliance Workspace​.
3.  Create a policy in 'Draft'.
4.  Navigate to 'Policy text'.
5.  Select **Import Policy** text.​
6.  Add a file in attachment.
7.  Select **Import**.
8.  Navigate back to the 'Policy text' tab.

 Observe the misalignment.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1842928

</td><td>

The **Revised by** field is empty when a policy is re-published in Policy and Compliance

</td><td>

Re-publishing a policy after moving it into a 'Draft' state displays an empty **Revised by** field.

</td><td>

1.  Navigate to an instance.
2.  Create a policy.
3.  Publish the policy.
4.  Move the policy into the 'Draft' state.
5.  Re-publish the policy.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1789573

</td><td>

The GCF metrics collector for certain internal topics is broken

</td><td>

Certain topic name patterns break GCF metrics' name parsing and selects the wrong value for the app ID.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1845208

</td><td>

Hermes tables aren't being audited

</td><td>

 

</td><td>

Modify hermes\_topics\_state or hermes\_app\_services.

 Notice that it's not being audited.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1845224

</td><td>

There's no warning that deleting sys\_kafka\_topic deletes the topic in a cluster

</td><td>

Deleting a topic in sys\_kafka\_topic deletes it in the cluster. Users should be warned about that.

</td><td>

Delete a sys\_kafka\_topic record in Xanadu or later.

 Notice that it's deleted in a cluster and no warning was given.

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

 PRB1827623

</td><td>

'\[Add to Wishlist\]' isn't displayed in the CSM portal after upgrading to Xanadu

</td><td>

It can be added in Service Portal, but in the CSM portal, the 'CSM SC Cat item' widget doesn't have \[**Show Add**/**Update Wish List** buttons\] as an instance option.

</td><td>

1.  Provision an instance with the Customer Service Management plugin to have a CSM portal.
2.  Find one sc\_cat\_item with 'Catalogs' and 'Category' defined and 'Catalog' enabled with Wishlist=true.
3.  Confirm it in the CSM portal.

 Expected behavior: It should be with the \[Add to Wishlist\] option, same as Vancouver.

 Actual behavior: \[Add to Wishlist\] isn't displayed in Washington and Xanadu.

</td></tr><tr><td>

HR Service Delivery

 PRB1819942

</td><td>

HTML tags are seen in the **Description\(description\)** field of an HR case

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HTML Field Type Editor

 PRB1841733

 [KB1813433](https://hi.service-now.com/kb_view.do?sysparm_article=KB1813433)

</td><td>

There's warnings seen in syslogs on visiting a classic form with an html-editor on it

</td><td>

'com.glide.script.RhinoEcmaError: null is not a function. : Line\(1\) column\(0\) ==&gt; 1: null\(\)' warnings are displayed in sys logs after upgrading to Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1853234

</td><td>

The 274 records related to TinyMCE 27.0.0 in the \[sys\_ux\_lib\_asset\] table shouldn't be presented

</td><td>

For example, when it comes to search, starting with 'sn-tinymce/27.0.0' in the 'Name' column.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1838458

</td><td>

Selected fields in 'Outbound Entry' aren't replicated to 'Inbound Entry' when a transformation is enabled \(specifically sys\_fields\)

</td><td>

When a user creates a 'Replication Entry' with transformation enabled, this freezes the selected/deselected sys\_ fields. Specifically, it freezes the ones that are gated by the 'Preserved Modified By' checkbox.

</td><td>

1.  On a 'Producer Replication' set, have sys\_ fields included and enable transformation on any table.
2.  Establish a 'Consumer' set.
3.  Ensure replication works.
4.  Remove/add a sys\_ field on a 'Producer Entry' set.
5.  Synchronize on the consumer side.

 Observe that the removal/addition isn't present on the 'Consumer Inbound Entry'.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1846711

</td><td>

If the legacy cluster is offline, the 'IDR Producer' job is in a 'doNothing' state

</td><td>

This prevents processing for Hermes sets too, even if the Hermes cluster is online.

</td><td>

Have the legacy cluster offline.

 Notice errors in the log and observe that the Hermes replication sets are also not processed.

</td></tr><tr><td>

Integration Hub

 PRB1836492

</td><td>

After upgrading to Xanadu, a 'No valid MID server' error is outputted by OAuthTokenRefreshJob

</td><td>

The error 'No valid MID server with REST capability available to obtain new access token' is outputted. The **use\_mid** field doesn't exist on the discovery\_credentials table until the 'com.snc.mid. enhanced\_security.oaut' plugin is installed.

</td><td>

1.  Prepare an instance which doesn't install the 'com.snc.mid. enhanced\_security.oauth' plugin.
2.  Allow OAuthTokenRefreshJob to run.
3.  Check the syslog to see if the error message is outputted.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1819713

</td><td>

A node is stuck in deadlock due to a LegacyPropertyEncrypter DB call in GlidePropertiesController.snapshot\(\)

</td><td>

This is a highly intermittent issue. This may take a significant number of node restarts to get this to occur due to the underlying race condition.

</td><td>

1.  Open a one node instance.
2.  Fire a full cache flush messages in a loop.
3.  Add 100 repeat jobs running every 1 second.
4.  Reduce the DB connection pool size as small as possible.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1839570

</td><td>

Upgrading to Xanadu causes module keys that are wrapped with a deactivated IKEK to be rekeyed with the active IKEK and then deactivated

</td><td>

This is an issue in KMF that causes module keys that are wrapped with a deactivated IKEK to be rekeyed with the active IKEK and then deactivated. The user is using a specific filter to find the correct module key to use for CLE, based on the sys\_id. However, because that key was deactivated, CLE failed.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1768407

</td><td>

The **Request Translation** UI action can be used multiple times for the same language on any knowledge article that has a version higher than 1

</td><td>

.

</td><td>

1.  Open a 'Knowledge Article' list.
2.  Find an article which has a version &gt; 1.
3.  Select the knowledge article in the list.
4.  Select the **Request Translation** action.
5.  Select a language to translate.
6.  Complete the process until a draft knowledge article version is created.

Notice that the draft knowledge article has a 'Parent' set to v1 of the knowledge article instead of the selected version.

7.  Select the **Request Translation** UI action.
8.  Select the same language as per the above step.
9.  Submit the request.

 See the translation request is still being created.

</td></tr><tr><td>

Language and Translations

 PRB1835314

</td><td>

Search is not working in the sc\_cat\_item table when a catalog item is created in a non-English language, and is then updated to an English language in an Oracle DB instance

</td><td>

When the user creates a catalog item in a non-English language, it can be searched by its name in the sc\_cat\_item table. However, when the name of the catalog item is updated to an English language, it cannot be searched in the sc\_cat\_item table in a non-English language.

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB1847452

</td><td>

The 'Check Activity closure - Flow' business rule \(BR\) may run and query more often than necessary

</td><td>

Notice that the 'Check Activity closure - Flow' business rule runs and queries for all sys\_flow\_context updates where 'state=COMPLETE'. This can lead to performance issues with an excessive number of sys\_trigger records created and unnecessary queries run by this BR.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1809729

</td><td>

When opening the database view record from a list, the view isn't the same as the list

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1821700

</td><td>

On an extensible list, users are unable to create an incident

</td><td>

The error message 'The page you are looking for could not be found' is displayed.

</td><td>

1.  Log in to the instance.
2.  Navigate to Service Operations Workspace.
3.  Navigate to the 'Incident' list.
4.  Refresh the page.
5.  Select the **New** button to create an incident.

 Users are unable to create an incident.

</td></tr><tr><td>

MID Server

 PRB1760614

</td><td>

SudoProcessor doesn't properly support commands with file paths

</td><td>

When configuring certain commands used by 'Parse File', they fail with 'Permission Denied' errors if configured in Sudo with a filepath specified, such as: /bin/cat /path/to/file.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1808137

</td><td>

Migrate 3DES ssh\_private\_key data to the new format of KMF encrypted data

</td><td>

Any ssh\_private\_key data must be encrypted in the password2 new KMF format. Any old\_format data must be migrated to the new format.

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

Mobile Experience for Field Service Management

 PRB1840564

</td><td>

A map doesn't load when users tap 'set location'

</td><td>

Users see a blank screen.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1843738

</td><td>

Field parameters for the URL button type that are used for the URL template are always encoded even when it's not needed

</td><td>

When selecting the options below on the Now Mobile app, the page doesn't navigate as expected. Instead, it is taken to a 'The page you are looking for could not be found' search screen. After selecting **Go**, the page is redirected correctly. Options: 'Open my Reservation » mesp?id=wsd\_reservations' and 'Create a new general reservation »mesp?id=wsd\_search'.

</td><td>

1.  Access the instance via Now Mobile.
2.  Open my Reservation » mesp?id=wsd\_reservations.
3.  Create a new general reservation »mesp?id=wsd\_search.
4.  Select **Go**.

 Notice that the page redirects correctly after selecting **Go**.

</td></tr><tr><td>

Mobile Platform

 PRB1844740

</td><td>

If a dot-walk field references a column in the parent table, document data isn't saved

</td><td>

Document data isn't displayed offline because it isn't saved in SQLite DB.

</td><td>

1.  Create a Table A extending task.
2.  Add a reference column.
3.  Create a child Table B extending from Table B.
4.  Add a few columns.
5.  Add a form screen to display the Table B record to show the reference field defined in Table A.
6.  Verify that the form screen is displayed correctly in the mobile app.
7.  Go offline.

 Notice that the form screen can't be displayed offline because the document data for Table B isn't saved in an SQLite database.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1792732

</td><td>

Next Experience's impersonate is much slower than UI16's impersonate

</td><td>

When users have a large number of sys\_user, the impersonate dialog can take a long time to open in Next Experience.

</td><td>

1.  Open an instance with at least 200k sys\_user records.
2.  Enable Next Experience.
3.  Connect as a user with admin rights in Next Experience.
4.  Notice the time it takes to open the impersonate dialog.
5.  Set the user preference to not use Next Experience.
6.  Reconnect and open the impersonate dialog.

 Observe that it takes a long time to open.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1814384

</td><td>

Adding a parent application and child module to the configurable menu breaks the menu API

</td><td>

 

</td><td>

1.  Create a configurable menu.
2.  Add the application 'Benchmark' to the configured items of the menu.
3.  Add a child module of 'Benchmark' to the configured menu.

 Expected behavior: The API should return the menu items' response.

 Actual behavior: The API returns 500.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1836091

</td><td>

There's a 'Session Expired 401' modal on public pages

</td><td>

The 'sn-banner-announcement-list' component emits an HTTP\_ERROR\_OCCURRED event causing a CANVAS\_GLOVAL\_ERROR event to open the 401 alert dialog.

</td><td>

1.  Create a page in UI Builder.
2.  Make it public.
3.  Log out.
4.  Open that public page.

 Notice a 'Session Expired \(401\)' dialog displays.

</td></tr><tr><td>

Now Assist Panel

 PRB1852531

</td><td>

The latency feedback messages are cut at the bottom

</td><td>

The problem likely stems from a height issue for the container.

</td><td>

1.  Navigate to NAP.
2.  Type 'summarize a record'.
3.  Check the latency feedback messages.

 Expected behavior: The message text is displayed whole in the container.

 Actual behavior: The bottom part of the messages are cut.

</td></tr><tr><td>

On-Call Scheduling

 PRB1814433

</td><td>

The 'Reminder Report' displays in an incorrect format

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1760775

</td><td>

There's an issue with reports on a workspace dashboard

</td><td>

Legends display duplicate values when translated into non-English language.

</td><td>

1.  Provision an instance with the 'Install Platform Analytics workspace' plugin installed.
2.  Create a Platform Analytics dashboard with a column report with 2 data sources.
3.  Change the language to Brazilian Portuguese.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1842669

</td><td>

Data definition synchronization slows down Playbook activation even when Playbook has no questionnaire activities

</td><td>

Activating Playbook can take over 1 hour to complete on a Xanadu instance. After setting a system property to turn off flow data variable sync, the activation time decreased to 40 minutes. When running a background script to activate, the process took 19 minutes. Previously, activation time took between 8 and 10 minutes.

</td><td>

1.  Create a Playbook with 100 activities but without any questionnaire activities, adding a trigger and filling all required fields.
2.  Activate the Playbook.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1847073

</td><td>

Questionnaire data definition and flow data variable \(questions\) are missing after duplicating a playbook

</td><td>

 

</td><td>

1.  Create a playbook.
2.  Add a lane and a questionnaire activity.
3.  Open the configuration panel and add a questionnaire \(data definition\).
4.  Add a question \(flow data var\).
5.  Save and close the configuration panel.
6.  Duplicate the playbook.

 Expected behavior: The questionnaire is duplicated.

 Actual behavior: The questionnaire isn't duplicated.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1848445

</td><td>

A PD update set generation takes a long time and/or timeouts for large playbooks with many conditions to run

</td><td>

This can happen with large processes. In extreme cases, update set generation takes 60+ minutes, where the entire process errors out.

</td><td>

1.  Create a large process \(e.g. 200 activities\), where all activities have a condition to run.
2.  Activate.

 Notice how long it takes to generate the update set, and if it fails.

</td></tr><tr><td>

Predictive Intelligence Similarity Solution

 PRB1826156

</td><td>

Untranslated annotations with the i18n language plugin

</td><td>

The annotation, 'STEP 1: Please select the table &amp; field\(s\) you want to use to retrieve your similarity results, and the table and fields you want compared' is left untranslated and in English.

</td><td>

1.  Set up a Xanadu testing environment.
2.  Install an i18n language plugin for French.
3.  Navigate to **now/nav/ui/classic/params/target /ml\_capability\_definition\_similarity.do**.

 Observe the hardcoded string, 'STEP 1: Please select the table &amp; field\(s\) you want to use to retrieve your similarity results, and the table and fields you want compared'.

</td></tr><tr><td>

Process Mining Workspace

 PRB1830418

</td><td>

Edit transitions aren't working

</td><td>

 

</td><td>

1.  Apply a transition.
2.  Select **Edit** from applied filters.

 Expected behavior: The transitions pop-up should be filled.

 Actual behavior: The transitions pop-up is empty.

</td></tr><tr><td>

Process Mining Workspace

 PRB1834704

</td><td>

When applying a transition filter and then an RCA, there's issues with flickering, the transitions, and filters

</td><td>

When applying a transition filter and then an RCA, after selecting any leading influencers and selecting 'Apply', there's multiple issues. Transitions aren't displayed properly. The screen flickers. Pop-ups are displayed multiple times. Applied filters and buttons aren't seen.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1839094

</td><td>

Full mining is enabled for a freemium project on the 'Project list' page

</td><td>

No users should be able to edit the evaluation project. No users should be able to delete the evaluation project\(s\). Users with a Process Mining role \(analyst, power or admin\) role can copy any project, including an evaluation project\(s\). The copied project is handled as a regular project and follows regular license check validation. No users should be able to do a full mine on evaluation project\(s\). The option shouldn't be available on UI16 and project card drop down menu.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1848238

</td><td>

Transitions freeze when max constrains are set to 0

</td><td>

The max duration in the constraints set is automatically handled as 0 when not filled in. This results in 0 matched records. Second, the UI freezes when the transition as 0 records, making it impossible to set a **max duration** field manually. This can also happen when a filter set has a transition with an activity from a previous version, which isn't present in the current version.

</td><td>

1.  Create a project with any AD.
2.  In the analyst workbench, open the **Transition** field.
3.  Configure 2 conditions/activity.
4.  Configure a constraint with:
    -   Start = step 1
    -   End = step 2
    -   Min duration = 1 min
    -   max duration: Keep empty

 Expected behavior: When the max duration is left empty, the max duration should be set to infinite \(so all records longer than the min duration should match\). Also, the user should be able to use the transition UI to add/remove fields and constraints.

 Actual behavior: When applying the transition, zero records match despite some matches. The **max duration** fields are set to 0 rather than kept empty. Also, when zero records match the condition, the user isn't able to change anything in the transition.

</td></tr><tr><td>

Project Management

 PRB1829307

</td><td>

A project actual isn't populated in the resource aggregated monthly for October, though it's populated for September and November

</td><td>

A category project actual isn't populated in table resource\_aggregate\_monthly for October. It does populate for September and November. There is one record for a project actual in October. If looking in resource\_aggregate\_weekly, all project actual records are there.

</td><td>

1.  Open the resource aggregate monthly \[resource\_aggregate\_monthly\] table.

Only 1 record displays under the monthly table and it excludes the month of October.

2.  Check in resource aggregate weekly \[resource\_aggregate\_weekly\].

Records are displayed as expected including the month of October.


</td></tr><tr><td>

Project Management

 PRB1829721

</td><td>

For a group-based ORA, if users update allocation dailies, it's rolling up to only immediate user-based allocation but not rolling up to group allocation without a user

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Related Lists

 PRB1780317

</td><td>

Inline cell edit options appear off-screen for related lists

</td><td>

The inline edit box should be right-justified when on the right side of the screen and should show all inline edit icons. Instead, the inline edit box is left justified when on the right side of the screen and disappears off the right edge of the screen.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1841076

</td><td>

After an Xanadu upgrade, there's a resource reports issue

</td><td>

Resource reports are broken after an Xanadu upgrade when the glide.sys.date\_format is dd-MM-yyyy.

</td><td>

1.  On Xanadu, set the date format to dd-MM-yyyy or dd/MM/yyyy.
2.  Navigate to **All** &gt; **Resource** &gt; **Resource Reports** &gt; **Resource Reports**.
    1.  Start date auto populates = today's date.
    2.  End date auto populates = 1 year from today's date - 1 day.
3.  Update the start date to 10/12/2024 and end date to 11/11/2025.
4.  Select **Run**.

 Observe the error message 'Report duration can't be more than 12 months'. The system considers the start date as being the 12th of October and not the 10th of December.

</td></tr><tr><td>

Rollback Contexts

 PRB1844400

 [KB1803428](https://hi.service-now.com/kb_view.do?sysparm_article=KB1803428)

</td><td>

The 'Clean Expired Rollback Contexts' job causes memory issues and node restarts

</td><td>

The job is streaming through large rowblocks of data and causing node restarts. The heap dump shows 1.2GB of memory taken by this job.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

SaaS integration with Adobe Cloud \(Glide\)

 PRB1843443

 [KB1913878](https://hi.service-now.com/kb_view.do?sysparm_article=KB1913878)

</td><td>

sn\_samp. UpdateReclamationCandidates &gt; getUserSubscriptionCost code issue

</td><td>

The **potential\_savings** field is only present on the samp\_sw\_ reclamation\_candidate table, and not in samp\_sw\_rc \_m2m\_subscription. This is causing the 'SAM - Updating Existing Reclamation Candidates' job to fail when updating the hybrid subscription cost.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Schedules

 PRB1831078

</td><td>

The 'Timeline' page isn't displaying properly with sub items after an Xanadu upgrade

</td><td>

When there is a \[cmn\_timeline\_sub\_item\] record attached, 'View Timeline' doesn't seem to work. The issue is only there when there's a timeline sub item in the 'Timeline' page. If there's no timeline, there's no issue.

</td><td>

1.  Navigate to **All** &gt; **Timeline Pages**.
2.  Select **ServiceNow Roadmap**.
3.  Select the **View Timeline** button.

</td></tr><tr><td>

Server-side scripts

 PRB1842183

</td><td>

Accessing ex.message throws an error in the 'try - catch' block when there's a RhinoException in the script

</td><td>

If there a RhinoException, there is an error: 'Allowing access to org.mozilla.javascript. RhinoException: getMessage:\(\) Ljava/lang/String;...'

</td><td>

1.  Write a server side script.
2.  Try to access ex.message in try-catch block.

</td></tr><tr><td>

Service Catalog

 PRB1835283

</td><td>

A UI policy script is running in Virtual Agent though the UI type is set to 'Desktop'

</td><td>

 

</td><td>

In Virtual Agent chat, request the item 'Seating Arrangement for Onboarding.' This has an onLoad UI Policy to make will\_this\_employee \_be\_seated\_flex\_or\_remote' read only.

 Expected behavior: The first question should be about a desk request.

 Actual behavior: The question 'Will this employee have a reserved desk, flexible desk, or work remotely?' is asked. This indicated that this isn't a read only question, and the onLoad UI Policy did run.

</td></tr><tr><td>

Service Mapping

 PRB1816637

</td><td>

In TB service connection, 2 CIs that are already part of a service and belong to the same CI type aren't added even if they match the traversal rule

</td><td>

When calculating a TB service, it starts from the tagged CIs, and then goes rule by rule to bring the next level according to the rule. When a rule is defined on the same class, if 2 CIs of that class have a connection that matches the rule between them, but those CIs are already part of a service, this connection isn't added to service.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1836767

</td><td>

When deleting a solution in the ml\_solution table, a cascade delete is triggered on ml\_cluster\_detail, but the records are not deleted

</td><td>

When deleting a solution in the ml\_solution table, a cascade delete is triggered on ml\_cluster\_detail, and it times out and does not delete all of the records because there are too many records in the table to handle a cascade delete.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1851972

</td><td>

Updating the same last\_mark in blob table during recomputation

</td><td>

During recomputation, the blob tables \(svc\_model\_obj\_relation for example\) are updated with today's date in the **last\_mark** field. The code is using 'date time' instead of the date to update the field.

</td><td>

1.  Open the SQL debug.
2.  Change a CI that connects to a service.

Users see an update to the **last\_mark** field with 'date time' instead of just the date.

3.  Repeat the process.

 Observe the same record updating with the same date.

</td></tr><tr><td>

ServiceNow Security Center \(Family Release\)

 PRB1843476

</td><td>

At an upgrade time with updated content, the completed steps of a customer action keeps the action status as 'ready', which turns off the action's **Complete** button

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1840878

</td><td>

The display of the Genius Results card using Now Assist and Knowledge Base articles are not aligned properly after resizing the browser

</td><td>

This issue also impacts the display in mobile devices.

</td><td>

1.  Navigate to a Xanadu instance with Now Assist configured.
2.  Ensure that the Portal has AI search enabled.
3.  Set the Genius search results limit to ten in the Search Application Configuration of the Portal Record.
4.  Ensure that the Search Profile has the Genius Results configuration 'Now Assist Q&amp;A' set in 'Related List'.
5.  Navigate to the Portal.
6.  Search for any keyword.

Notice that catalog items populate in Genius Results.

7.  Resize the browser.

Notice that the alignment of the Genius Results are not correct.

8.  Navigate to the Knowledge tab in the search results.

Notice that the alignment of the Knowledge Base results are also not properly aligned.


</td></tr><tr><td>

Session Validation

 PRB1846625

 [KB1812394](https://hi.service-now.com/kb_view.do?sysparm_article=KB1812394)

</td><td>

Deeplinks redirection failed with a node switch from an unauthenticated session to an authenticated session

</td><td>

On opening a deeplink URL, the user should authenticate and redirect to a specific resource.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management Licensing and Compliance

 PRB1807335

</td><td>

Daily subscription counts intermittently get zero counts

</td><td>

The 'SAM/CI populate data' job clears out resources counts but takes 7 minutes to repopulate. Since 'Usage Analytics definition' queries that for the daily count, if the definition query happens during the 7 minute window when the 'SAM/CI populate data job' is running, definition query doesn't get an accurate count.

</td><td>

1.  Run the 'SAM/CI populate data' job at 4AM.
2.  Run 'Usage Analytics for definition' counts at 4AM.

 Observe daily subscription counts gets zero counts.

</td></tr><tr><td>

Software Asset Management

 PRB1787960

 [KB1826337](https://hi.service-now.com/kb_view.do?sysparm_article=KB1826337)

</td><td>

There's a slow query caused by updateMultipleEntity in Suite Engine

</td><td>

The query causes a reconciliation performance issue, with slow updates due to chunking. There's significant performance degradation.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1790386

</td><td>

There's a replication lag caused by 'untagSoftwareModel ForUnlicensedInstall' in AutomaticSMRCreation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1853225

</td><td>

Remediation options buttons aren't triggering a scheduled job immediately if date\_format is different

</td><td>

A scheduled job should be scheduled to run immediately.

</td><td>

 

</td></tr><tr><td>

Software Asset Normalization

 PRB1808233

</td><td>

The 'SAM - Normalize discovery models using content library rules' scheduled job is not robust because a single corrupted samp\_package\_map record can make the job fail

</td><td>

The code should be robust to not fail the job because one record threw an exception. Also, this job triggers another job, 'SAM - Normalize discovery models using ML', which should be checked for being active before adding in a trigger.

</td><td>

1.  Create a discovery model.
2.  Create a matching version hash record in samp\_package\_map where the package reference is corrupted.
3.  Run the job.

 Observe that it fails.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB1791385

</td><td>

ignoreNonBYOLInstalls shouldn't insert a reason for 'Missing Cloud License Type'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Special Handling Notes

 PRB1836082

</td><td>

Simplify 'Refresh SHN' conditionals for readability and backportability

</td><td>

In Xanadu, if users set the Special Handling Notes \(SHN\) property 'Display special handling notes only once per session' to false, then the SHN pop-up window isn't displayed at all each time a user accesses a record. However, in Xanadu, once the property is set to false, the SHN pop-up window isn't displayed at all each time a user accesses a record. According to the documentation, the SHN pop-up window should be displayed each time a user accesses a record.

</td><td>

1.  Ensure that the plugin 'Special Handling Notes' \(com.sn\_shn\) is activated.
2.  Ensure to upgrade the Store apps to the latest versions.
3.  Create 'Special Handling Notes' \(sn\_shn\_notes\) for the 'Incident' table.
4.  Specify a condition, such as 'Short description', that contains something.
5.  Open the SHN 'Properties' page and set the property 'Display special handling notes only once per session' to false.
6.  Open an 'Incident' record which matches the condition in Service Operations Workspace or CSM Workspace.

 Notice that the 'Special Handling Notes' pop-up window isn't displayed at all each time a user accesses the record in either workspace.

</td></tr><tr><td>

Survey Management

 PRB1847800

</td><td>

Inactive metrics aren't displayed on the user response form

</td><td>

 

</td><td>

1.  Open any instance on or after Xanadu.
2.  Create a survey.
3.  Assign the survey to a user.
4.  Take the survey.
5.  Submit it.

After submitting, when users view a user response form, users are able to see all the questions along with their response.

6.  Mark a few questions as inactive.
7.  Open the view user response form.

 Expected behavior: Inactive metrics should also be shown in the response form.

 Actual behavior: Inactive metrics aren't displayed now even though the responses were there.

</td></tr><tr><td>

Syntax Editor

 PRB1533082

</td><td>

The fonts defined on the system property 'glide.ui.html.editor .v4.font.collection' aren't displayed on the font list of the HTML editor on Agent Workspace

</td><td>

The list should show only the fonts defined in the value of system property 'glide.ui.html.editor .v4.font.collection, but it shows all the fonts mentioned on the system property 'Description'. On the native UI HTML editor, it's working as expected.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB1818627

</td><td>

The 'Slow Delete DMLs' from the 'Text index events process' job is contributing towards a replication lag on the Standby DB

</td><td>

'Slow delete DMLs' originating from the 'Text index events process' job is contributing towards the lag when observed at any point of time during the lag increasing time. It can run past 3 hours.

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB1847486

</td><td>

Multiple concurrent import sets are created for one data source

</td><td>

 

</td><td>

1.  Install an AWS version with parallel loading.
2.  Configure AWS.
3.  Run import.
4.  Check the concurrent import set attached to the imports sets.

</td></tr><tr><td>

Table Administration and Data Management

 PRB1811830

</td><td>

Records with no translations for translated fields appear first when sorted a to z

</td><td>

 

</td><td>

1.  Provision an instance with a language plugin installed.
2.  Switch the user language from English to another language.
3.  Navigate to any table with a translated type field.
4.  Order the translated type columns.

 Expected behavior: The order should be correct.

 Actual behavior: The order isn't correct with 'a to z' or 'z to a'.

</td></tr><tr><td>

UI Field Administration

 PRB1696422

</td><td>

The **Toggle Domain Scope** UI action doesn't work in a workspace

</td><td>

The **Toggle Domain Scope in form** UI action isn't working when Next Experience is on. It works fine with Next Experience off on UI16 pages. This issue doesn't impact legacy Agent Workspace. It impacts configurable workspaces only.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1820922

</td><td>

The display business rule causes info messages to not display on quick-edit of records in the Service Operations Workspace \(SOW\)

</td><td>

An info message doesn't display the message when using the 'i' quick-edit feature in SOW or any other workspace. When selecting the 'i' icon to edit a record in quick edit from the list view in the workspace, the info message is not shown. However, the info message appears correctly when previewing a record using the 'i' icon in the Native UI.

</td><td>

1.  Open any Xanadu or Washington DC instance.
2.  Create a business rule for the incident table that executes on 'Display'.
3.  Add an info message in the script section of the business rule.
4.  Open the incident list in the Native UI.
5.  Select on the **i** preview of a record.

Observe that the business rule is executed and displays the info message.

6.  Open SOW or any workspace.
7.  Select the **i** icon for the quick view edit of a record in the list view.

 Expected behavior: The info message should be displayed upon triggering the business rule in the workspace.

 Actual behavior: The info message is not displayed in the quick-edit view in the workspace.

</td></tr><tr><td>

Upgrade Center

 PRB1812035

 [KB1831586](https://hi.service-now.com/kb_view.do?sysparm_article=KB1831586)

</td><td>

Records with &lt;sys\_es\_latest\_script action="INSERT\_OR\_UPDATE"&gt; in the XML are listed in the plugin update list as 'skipped' during the plugin upgrade

</td><td>

It seems that the entire XML file is diffed here, when users would expect only the contents of the record to matter.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Upgrade Center

 PRB1844300

</td><td>

sys\_claims customization protection behaves differently than sys\_update\_xml during upgrades when the sys\_policy of the file changes

</td><td>

The installer has no historic knowledge and can't tell if a record was previously unprotected and just became protected in a subsequent release version. This applies both to sys\_claims as well as sys\_update\_xml as a protection mechanism for changes.

</td><td>

1.  Open a Washington DC instance.
2.  Install the sn\_hr\_agent\_ws app.
3.  Customize the 'sys\_ux\_macroponent\_ 1d033475eb3011106eb96bf3a252287f' file.
4.  Publish to the app repo.
5.  Create a customization pack.
6.  Open another instance.
7.  Install the above app along with the app customization.
8.  Ensure the entry for that file is present in the sys\_claim table.
9.  Upgrade the instance to Xanadu's latest patch.
10. Check the upgrade history log for that file.

 Notice that it should be 'SKIPPED', but instead is 'UPDATED'.

</td></tr><tr><td>

Virtual Agent

 PRB1817023

</td><td>

A NAVA response is still loading when the conversation is closed

</td><td>

 

</td><td>

1.  On NAVA, start a conversation.
2.  Type 'show me some article'.

 Observe that the NAVA response is displaying as 'Looking into your request.

</td></tr><tr><td>

Virtual Agent

 PRB1849035

</td><td>

Skill discovery is failing because of a missing sn\_aia\_usecase table

</td><td>

 

</td><td>

1.  Install AI Agent Jan version to an instance with Now Assist.
2.  Create sn\_aia\_usecase.
3.  Upgrade the instance on to the latest build.
4.  Open NAP.

 Observe that topic discovery is failing.

</td></tr><tr><td>

Virtual Agent

 PRB1851004

</td><td>

Skill discovery and execution fails with the proxy sys\_prop enabled in Yokohama

</td><td>

Discovery and execution fails when the sysprop com.glide.cs.one\_extend. auto\_proxy\_enabled = false. This is enabled by default.

</td><td>

1.  Open a NAVA portal.
2.  Execute a topic.

The topic executes with error messages in each stage.

3.  Try to perform a topic discovery.

 Observe that discovery fails with a 'sorry' message.

</td></tr><tr><td>

Virtual Agent

 PRB1851248

</td><td>

In sync mode, skill execution involving RAG is failing

</td><td>

For the skill mentioned, the RAG tool is failing in 'sync' mode due to an empty query input. It looks like it's not able to fetch and resolve 'query' from the previous tool output.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1854061

</td><td>

OptimisticLockException when executing dynamic capability

</td><td>

The output refiner response is proper, but it fails to return a response to the dynamic capability node in the topic.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1854081

</td><td>

GAIC Licensing should charge assists instead of trial assists even when the 'Licensing' API returns that a feature isn't configured in pricing

</td><td>

When a GAIC capability is executed, as part of licensing, a call is made to the 'Licensing' API to get the assists configured for that capability. If it is not present in pricing, users get an empty response. In that case, trial assists are configured in GAIC \(sys\_gen\_ai\_license \_metadata\_trial\) and set as trial assists. This needs to be changed that the trial assists should still be charged as real assists when inserting into sys\_gen\_ai\_usage\_log.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1855393

</td><td>

User KnowledgeGraph data should be applied for search

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1856309

</td><td>

Create a metadata table for AI agents's skill discovery

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1856323

</td><td>

An NSA admin user is unable to switch LLMs

</td><td>

The issue exists during activating a skill.

</td><td>

1.  Impersonate with an NSA admin user.
2.  **Now Assist admin** &gt; **Settings** &gt; **Manage LLMs**.
3.  Switch the LLM from Azure to Now LLM.
4.  Verify the success modal.
5.  Verify the 'sys one extend capability' table.
6.  Observe that no capability is switched.

 Expected behavior: An NSA admin user is unable to switch the LLMs.

 Actual behavior: An NSA admin user should be able to switch the LLMs.

</td></tr><tr><td>

Virtual Agent

 PRB1856492

</td><td>

Chat bot errors out due to a mismatched lock version

</td><td>

The chat bot errors out and exits the chat.

</td><td>

1.  In a chat bot conversation, enter the query: 'General Request for a Storage VM' to request this catalog item.
2.  Go through the flow.

 Observe that bot throws the error, 'Syslog error: Lock version mismatch for conversationId 14c1dcb92b371a 1009f2f22ffe91bf1c - expected 13 and encountered 14'.

</td></tr><tr><td>

Virtual Agent

 PRB1857900

</td><td>

A deflection log table doesn't set a 'no response' state when AI Search returns 'no answer found'

</td><td>

 

</td><td>

1.  Navigate to NAVA.
2.  Type in a search term that has no synthesized result and no regular result.
3.  Navigate to the deflection log table \(sys\_cs\_deflection\_log\).
4.  Check the record corresponding to this search.

 Notice that the **State** field isn't set to 'no response'.

</td></tr><tr><td>

Virtual Agent

 PRB1858305

</td><td>

GAIC doesn't handle response max tokens of NULL for sys\_generative\_ai\_config

</td><td>

If sn\_vad\_genai.com. glide.cs.one\_extend .auto\_proxy\_enabled is set to false, the issue isn't reproducible.

</td><td>

1.  Provision an instance with Now Assist For Creator \(nowassist-creator\) plugin version 27.1.1 installed.
2.  As a user with elevated privileges, open Service Now Studio.
3.  Select **NAP** in ServiceNow Studio.
4.  Type anything as a prompt. For example, 'I want to create an app to track new employee hires'.

 Expected behavior: Users get a response from the LLM.

 Actual behavior: There's a GAIC error complaining about missing data.

</td></tr><tr><td>

Virtual Agent

 PRB1858954

</td><td>

Follow-up after a navigation skill isn't working

</td><td>

 

</td><td>

1.  Select **NAP**.
2.  Enter 'show me list of unassigned incidents'.
3.  Select **incident**.
4.  Enter 'show list of open incidents'.

 Observe that a processing message keeps loading and no response is displayed.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1861185

</td><td>

An animated icon isn't visible in NAVA when enabled

</td><td>

 

</td><td>

1.  Enable sn\_nowassist\_va.nass \_animated\_avatar\_enabled.
2.  Navigate to NAVA.
3.  Type an utterance like 'what is spam'.

 Expected behavior: An animated icon is visible next to the loading messages.

 Actual behavior: No icon loads next to loading messages.

</td></tr><tr><td>

Walk-Up Experience

 PRB1848443

</td><td>

A badge reader throws an error: 'Could not find location queue associated with badge reader'

</td><td>

Starting from Xanadu, users who have the badge reader configuration set up are facing the issue where it states 'Could not find location queue associated with badge reader', even though there is a location queue defined with the badge reader.

</td><td>

1.  Log in as an admin.
2.  Run the badgeReaderAPI.

 Expected behavior: The API should give a success message: 'User has been checked in'.

 Actual behavior: The API is throwing 'Could not find location queue associated with badge reader', even though there is a location available.

</td></tr><tr><td>

Workflow Contexts

 PRB1820829

</td><td>

A fix causes a query to be executed when module access is requested

</td><td>

A SQL query against sys\_kmf\_crypto\_module is run whenever access to a module is checked with CallerPolicyAccessManager .isModuleAccessible. For a field with a Column Level Encryption \(CLE\) configuration, this API is called one or more times for each canRead\|canWrite\|canCreate call that is made. When canRead is called multiple times for each form load, the query is run many times when loading a single record.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1838614

</td><td>

Logic fails to check for conflicts if the assignment group selected on the work order task \(WOT\) contains multiple group types

</td><td>

The business rule date checks for table sm\_task fails to correctly check for conflicts if the assignment group on the WOT contains multiple group types.

</td><td>

1.  Impersonate a dispatcher and assign a task to an agent in a group with multiple types.
2.  Assign a second task to the same agent at the same time.

The time-conflict that should be displayed isn't displayed.

3.  Unassign the task assigned in step 2.
4.  Remove one of the types from the agent's group.
5.  Execute step 2 again.

 The assignment fails because of the conflict.

</td></tr><tr><td>

Work Order Management

 PRB1853754

</td><td>

Schedule conflicts aren't displayed for wm\_manager when the contractor management plugin is installed

</td><td>

A conflict error message should be displayed when scheduled Work Order Tasks \(WOT\) conflict and are assigned to the same user with the wm\_manager role.

</td><td>

1.  Provision an instance with the Field Service Management Contractor Management plugin installed.
2.  Create a WOT.
3.  Assign the WOT to a wm\_manager.
4.  Create another task that conflicts with the previous task.
5.  Assign the WOT to a same wm\_manager.

 Expected behavior: The conflict error is displayed.

 Actual behavior: The conflict errors aren't displayed.

</td></tr></tbody>
</table>## Fixes included

-   [Xanadu Patch 6](xanadu-patch-6.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4b Hotfix 1](xanadu-patch-4b-hf-1-PO.md)
-   [Xanadu Patch 4b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1915138)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


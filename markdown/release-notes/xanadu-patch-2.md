---
title: Xanadu Patch 2
description: The Xanadu Patch 2 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-10-10"
reading_time_minutes: 43
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 2

The Xanadu Patch 2 release contains important problem fixes.

-   **Xanadu Patch 2 was released on October 10, 2024.**
    -   Build date: 10-06-2024\_2304
    -   Build tag: glide-xanadu-07-02-2024\_\_patch2-09-25-2024

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X02.00.xlsx).

## Overview

Xanadu Patch 2 includes 249 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp2.png "Top 10 problem categories")

If your organization is using FSM questionnaires, do not upgrade to Xanadu Patch 2. Plan your future upgrade for a release that includes the fix for PRB1811012.

## Security-related fixes

Xanadu Patch 2 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 2, refer to [KB1703800](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1703800).

## Changes in Xanadu Patch 2

-   **[Platform Analytics Migration Center](https://www.servicenow.com/docs/access?context=data-migration&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    You can disable the **Start Moving** and **Activate** Platform Analytics experience options. Create the system property `com.glide.par.coreui.migration.enabled` and set it to `False`. If you set the property to `False` before you migrate any content, both options are disabled. If you set the property to false after you migrate your content, only the **Activate** button is disabled.

    If you want to start the migration and view what artifacts are in compatibility mode, and resolve any issues, set the property to `False` after you run the migration to prevent activation of Platform Analytics experience. If you want to prevent the migration process, set the property to `False` first.

    For more information, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

-   **[System properties for Proactive analytics](https://www.servicenow.com/docs/access?context=system-props-proactive-analytics&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US)**

    The maximum number of KPI Signals Configurations \(pa\_xmr\_processes\) that can be evaluated by the KPI Signals Insight Job. After this number of processes have been evaluated, the remaining processes are ignored.


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

Activity Stream

 PRB1757236

 [KB1700513](https://hi.service-now.com/kb_view.do?sysparm_article=KB1700513)

</td><td>

The workspace activity stream displays the 'From' email as the actual user who has sent the email

</td><td>

The 'From' of the entry displays 'From: \[userId\]@snc'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1752255

</td><td>

Flow stage changes aren't updating after using the **Do the following in parallel** action

</td><td>

The issue is also confirmed in Washington DC.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1740666

</td><td>

Some certificates aren't regenerated when certificates are missing and keys are present

</td><td>

If an instance only has an active key pair \(for Instance Asymmetric Encryption Key \(IAEK\) and Instance Signature Key \(ISK\)\) but certificates corresponding to it don't exist, certificates corresponding to IAEK and ISK should be regenerated, but aren't.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1770231

</td><td>

A list doesn't load when a fixed filter is null and a live list is enabled

</td><td>

The 'List' screen hangs when applying a filter.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1791369

 [KB1703297](https://hi.service-now.com/kb_view.do?sysparm_article=KB1703297)

</td><td>

There's a MID server issue and a pop-up warning when two MID servers use the same username and password combination

</td><td>

The user observes a warning and a MID server issue.

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

Advanced Work Assignment

 PRB1793780

</td><td>

A post-chat survey related list is hidden for external queues

</td><td>

 

</td><td>

1.  Enable the related list chat survey on queues.
2.  Create an internal queue \(external boolean = false\).

The chat survey related list can be seen as a tab to setup post chat surveys.

3.  Create an external queue\(external boolean = true\).

 Expected behavior: The post chat survey should be available to setup for external queues as well.

 Actual behavior: The chat survey related list is hidden and post chat survey can't be setup.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1794843

</td><td>

Events are 'cancelled' instead of 'completed' when the requester ends the conversation with the Chat Agent

</td><td>

 

</td><td>

Scenario 1:

 1.  The requester starts a conversation.
2.  Agent 1 accepts the work item.
3.  The requester ends the conversation.

 Scenario 2:

 1.  The requester starts a conversation.
2.  Agent 1 accepts the work item.
3.  Agent 1 transfers the work item to Agent 2.
4.  The requester ends conversation before Agent 2 accepts the transferred work item.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1799796

</td><td>

Unable to transfer an interaction to an agent that doesn't belong to a group

</td><td>

 

</td><td>

1.  Add awa\_external\_user roles to Agent 1 and Agent 2.
2.  Add only Agent 1 to a user group.
3.  Start a conversation.
4.  Assign it to Agent 1.
5.  Transfer the interaction to Agent 2 from the Agent 1 workspace.

 Notice that Agent 2 does not appear in the list of agents eligible for transfer.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1800365

</td><td>

An external queue agent availability count displays '0'

</td><td>

The external queue agent count should be represented appropriately or the count parameter should be remove during the transfer initiation.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1792512

</td><td>

Translations are loaded repeatedly when loading conditional content for sn\_vul

</td><td>

 

</td><td>

Install or upgrade sn\_vul with customization.

</td></tr><tr><td>

Archive Rules

 PRB1789753

</td><td>

Table Cleaner rule for sys\_archive\_run impacts the restoration of records older than one year

</td><td>

The Table Cleaner rule for sys\_archive\_run impacts customers that have data archived more than one year ago, and have a need to restore some of those records.

</td><td>

1.  Provision an instance with records archived over one year ago where sys\_archive\_log is large \(10ths/100ths of millions records\).
2.  Restore a record that has related records and has been archived one year ago by selecting **Restore Record and Related Records**.

 Observe that the UI freezes and the transaction is canceled after five minutes. The parent record gets restored, the related record does not.

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1794574

</td><td>

Memory leak in the AMBSessionMessageQueue

</td><td>

A message from a removed session stays in the AMBSessionMessageQueue.

</td><td>

1.  Publish messages to a channel that has redelivery turned on.
2.  Turn off the redelivery.
3.  Disconnect the client.
4.  Reconnect the client.

 Notice that the redelivery continues.

</td></tr><tr><td>

Azure Active Directory User Mapping

 PRB1797579

</td><td>

EC in teams/unfurling flows are failing due to an authentication error

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1798836

</td><td>

The placeholder text 'Type your Work notes \(Private\) here' isn't generated in the resolution notes in UI16 after clearing AI generated notes

</td><td>

 

</td><td>

1.  Open an HR case that isn't closed on UI16.
2.  Change the state of the case from 'work in progress' to 'complete'.
3.  Verify that the pop up 'Add resolution notes' is displayed.
4.  Delete the AI-generated resolution notes.

 Expected behavior: The placeholder text 'Type your Work notes \(Private\) here' is visible upon deleting the AI generated notes.

 Actual behavior: The placeholder text 'Type your Work notes \(Private\) here' isn't generated upon clearing the AI generated notes.

</td></tr><tr><td>

Change Management

 PRB1788129

</td><td>

Opt-in mechanism for Change-HAM integration

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1797542

</td><td>

The **Proposed change** field becomes empty when a mass update CI Class is read-only

</td><td>

 

</td><td>

1.  Navigate to Service Operations Workspace \(SOW\).
2.  Create a normal change \(either with a change model or not\) with a configuration item and assignment group = 'Service Desk'.
3.  Save.
4.  Navigate to the 'Details' tab.
5.  Navigate to the 'Impact' section.
6.  Verify the mass update CI class is visible on the form.
7.  Enable the checkbox for mass update CI class.
8.  Populate the CI class and proposed change.
9.  Select **Request approval**.

 The **Proposed change** field becomes empty on SOW.

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB1791634

</td><td>

DbBatchProcessor doesn't handle resource cleanup properly, resulting in high memory contention on the node

</td><td>

When there are invalid SQL statements, DbBatchProcessor doesn't close the statement batcher. This results in high memory contention.

</td><td>

 

</td></tr><tr><td>

CMDB Query Builder

 PRB1796164

 [KB1701193](https://hi.service-now.com/kb_view.do?sysparm_article=KB1701193)

</td><td>

Query Builder queries with the 'AND' node have different result structures/the data is split over multiple result records

</td><td>

A fix was applied to the performance of QB queries with the 'AND' node by avoiding multiplexing data in the results of such queries. However, this might break the way users consume the results in their systems.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Condition Builder

 PRB1795084

</td><td>

Selecting 'AND' doesn't populate a catalog item when selecting variables/questions from a field's dot walk

</td><td>

On first load, the catalog item appears, but selecting 'AND' doesn't display the item name. Selecting 'OR' works. Expected behavior is that selecting 'AND' should populate the catalog item when selecting variables/question from a field.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1790374

 [KB1698757](https://hi.service-now.com/kb_view.do?sysparm_article=KB1698757)

</td><td>

The de-duplication template doesn't honor the 'Only allow updates from duplicate CIs when the main CI value is null' option

</td><td>

The main CI attributes are updated with the values of the duplicate CI.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Contracts Core

 PRB1798652

</td><td>

Files are deleted after a week due to a scheduler job

</td><td>

 

</td><td>

1.  Open any TPC or NDA contract.
2.  Try uploading a supporting file.

 After the upload, observe that a new record is created in sys\_attachment\_cleaner\_entry. The platform is providing a schedule job to run every weekend to fetch all the sys\_attachment\_cleaner\_entry records and delete the attachment referenced inside this record. Eventually, the uploaded attachment for the support document is deleted after 5 days \(since the scheduler only deletes the sys\_attachment\_cleaner\_entry records, which are of at least 5 days old\).

</td></tr><tr><td>

Core Platform

 PRB1761876

</td><td>

A QuotaManager null point exception is printed in the logs multiple times

</td><td>

If a caller requests active transactions, they might get one with a null sys\_ID. An error displays in the logs: 'QuotaManager: Exception during quota processing: : java.lang.NullPointerException:...'

</td><td>

1.  Navigate to syslog.list.
2.  Query on a message that contains QuotaManager.

 Expected behavior: There are no errors printed in the logs.

 Actual behavior: The logs contain multiple records with an error message.

</td></tr><tr><td>

Customer Service Management for Field Service Management

 PRB1798276

 [KB1700946](https://hi.service-now.com/kb_view.do?sysparm_article=KB1700946)

</td><td>

Field Service Management work order task map pages don't load for the latest Google Maps Javascript API versions

</td><td>

Map pages for 'View task location' fail to load due to an incompatibility between the latest Google Maps API versions and the Google Maps base instance integration plugin.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1756534

</td><td>

Enabling shadow tables for compaction

</td><td>

 

</td><td>

1.  Create a shadow table.
2.  Call the TableCompactor.compact\(tableName\) API.

Notice the message that appears, 'The compaction is not enabled for table:+ tableName'.

3.  Enable shadow tables for compaction.
4.  Create a shadow table.
5.  Call the TableCompactor.compact\(tableName\) API.

 Notice that the message 'Created sys\_trigger compaction qualification job with sys\_id:' appears, indicating the shadow table successfully qualified for compaction now.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1780248

</td><td>

The **Payload** field value isn't deleted for offload retry records

</td><td>

 

</td><td>

1.  Create 300 records.
2.  Update the batch\_size to 50 and update the offload retry to 5 minutes.
3.  Offload the records.
4.  Stop the facade instance while the first batch offload is in progress.
5.  Verify the entries created in the 'cidx' table.
6.  Verify the batch status in the 'sys\_archive\_tier2\_chunk' table is updated with 'Error'.
7.  Verify the 'sys\_archive\_log' table.

The 'Records' payload shouldn't be deleted.

8.  After 10 minutes, restart the facade and trigger offload.
9.  Verify the retry is happening for the failed batch.
10. Verify the retry is successful and verify the payload for the first failed batch 50 records is deleted.

 Expected behavior: The **Payload** field value should be deleted for the retry successful records in the sys\_archive\_log table.

 Actual behavior: The **Payload** field value isn't deleted for the retry successful records in the sys\_archive\_log table.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1794621

</td><td>

The user is unable to get data management update jobs to be applied when using 'Run at' time

</td><td>

 

</td><td>

1.  Create an incident with a short description of 'DM update test'.
2.  Create a sys\_dm\_update record.
3.  Set the table as 'Incident' and the conditions as 'Short Description contains 'DM update test''.
4.  In 'Field' and 'Values', set 'Assignment group' to 'Approvers'.
5.  Set the 'Run at' to a few minutes in the future \(the record may need to be saved first, before this field appears\).
6.  Wait the duration of the period that the sys\_dm\_update should take to run.
7.  Refresh the sys\_db\_update rule.

Observe that the state is 'New'.

8.  Refresh the incident created in step 1.

 Observe that the 'Assignment group' is unchanged.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1802795

</td><td>

Storage API can't record statistics for tables with names longer than 40 characters

</td><td>

The length of the **table\_name** field of the sys\_physical\_table\_disk\_usage table is set to 40.

</td><td>

1.  Create a table with a name longer than 40 characters in the database.
2.  Run the command 'snow -t storage\_disk\_usage db\_port'.
3.  Observe the logs.

 Expected behavior: There are no errors in the logs, and there's a record in sys\_physical\_table\_disk\_usage table for the table.

 Actual behavior: There are errors in the logs, and statistics for the table in sys\_physical\_table\_disk\_usage table aren't recorded.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1793059

</td><td>

ThresholdStopWatch is missing from the StringFormat arg for logNoBroadcast

</td><td>

 

</td><td>

1.  Query the GlideRecord in loop against the Configuration Management Database \(CMDB\) table.
2.  Profile the central processing unit \(CPU\).
3.  Review the before and after.

 Notice the string concatenation.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1796286

</td><td>

Remove usage of Cleaner from PreparedStatementWrapper

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1797887

</td><td>

A continuation of ThresholdStopWatch is missing from the StringFormat 'arg' for logNoBroadcast

</td><td>

 

</td><td>

1.  Replace getSimpleName\(\) to getName\(\).
2.  Notice that the debug property glide.db.listeners.slow\_listener\_debug.enable should not log messages when enabled.
3.  Ensure the default property value is 'false'.
4.  Ensure logging isn't enabled for standby nodes.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1798263

</td><td>

Allow a non-transactional use of StatementBatcher

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1795144

</td><td>

Introduction of PrimaryKey ordering \(PrimaryKeyOrderer\) in Xanadu increased application central processing unit \(CPU\) response greater than 5%

</td><td>

Excessive time spent on PrimaryKeyOrderer .adjustOrderBy / requireAdjustment when executing a script.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1796625

</td><td>

Adjust returned value of swarm64.get\_resource\_usage function

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Collection for Oracle Global Licensing and Advisory Services for Software Asset Management

 PRB1666406

 [KB1338595](https://hi.service-now.com/kb_view.do?sysparm_article=KB1338595)

</td><td>

Downloading Global License Advisory Services \(GLAS\) data results in a blank page

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1789497

</td><td>

Duplicate SNMP credential affinity records are created

</td><td>

When Discovery is run twice against an SNMP device using a SNMP v1/v2c credential, a duplicate affinity record is created.

</td><td>

1.  On an instance running Washington DC or later, run a Discovery against an SNMP device using a SNMP v1/v2c credential.
2.  After Discovery completes, check the dscy\_credentials\_affinity table for affinity for the device just discovered when linking the SNMP credential.
3.  Run another Discovery scan against the same device with the same MID and same credential.
4.  Check the dscy\_credentials\_affinity table after this scan.

 Observe that a duplicate affinity record should be created.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1794319

</td><td>

Using the DocIntel Admin application to copy use cases changes the name of key group keys, preventing a trained model from making predictions for the keys

</td><td>

 

</td><td>

1.  Take a use case that has key group keys.
2.  Copy the key group keys with the DocIntel Admin application.

 Notice that the key name of the key group keys are now prepended with the key group in the copied task definition.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1795579

</td><td>

Predictions are displaying as zero for new tasks for some trained usecases after an upgrade from Washington to Xanadu

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1796853

</td><td>

Tasks having the source table with restricted caller access \(RCA\) tracking fail during an ML backend job

</td><td>

This issue is because the RCA for the target record isn't added automatically. If a user creates a new RCA record, it works fine.

</td><td>

1.  Create a usecase.
2.  Have a task with source table restricted caller tracking.
3.  Run a task.

 Observe failure during ML tasks.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1798802

</td><td>

The date format takes the month as first in STP even when the day is first in the format

</td><td>

 

</td><td>

1.  Create date type fields where the day is first in the format.
2.  Process the task with a different date format.
3.  Enable STP.

</td></tr><tr><td>

Document Viewer

 PRB1734394

 [KB1647686](https://hi.service-now.com/kb_view.do?sysparm_article=KB1647686)

</td><td>

When viewing a knowledge article with an embedded PDF attachment, the preview of the attached PDF is low quality

</td><td>

While viewing the attached PDF in a knowledge article \('Published' or 'under review'\), the preview of the attached PDF is low quality. If the user views the attached PDF outside of the viewer \(in Adobe or in the browser\) the preview of the PDF is good quality. This issue occurs in platform document viewer.

</td><td>

1.  Log in to an instance.
2.  Open the application navigator and search **Incidents** &gt; **All**.
3.  Open any record.
4.  Attach the provided PDF.

 While viewing the attached PDF, notice that the preview of an attached PDF is in low quality.

</td></tr><tr><td>

Email Notifications

 PRB1777379

</td><td>

There's a potential memory leak in Email Client

</td><td>

Several elements are retained that shouldn't be by a reference held onto by Email Client.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1792310

</td><td>

Inbound emails that are signed and encrypted have an invalid signature with the S/MIME plugin

</td><td>

Emails received in the instance that are both signed and encrypted contain an invalid signature. Emails that are sent to the instance that are either encrypted or signed don't contain an invalid signature.

</td><td>

1.  Configure the S/MIME plugin to receive encrypted and signed emails in the instance.
2.  Send an email to the ServiceNow instances mailbox that is both signed and encrypted.
3.  Check the signature in the validity after the email is received.

 Observe that the email has an invalid signature.

</td></tr><tr><td>

Employee Center

 PRB1775296

</td><td>

After adding granular delegation, 'My Tasks' is slow in Employee Center

</td><td>

After adding Granular Delegation, 'My Tasks' is extremely slow in Employee Center.

</td><td>

 

</td></tr><tr><td>

Employee Center

 PRB1775510

</td><td>

'Article' isn't translated in the i18n Mobile App QA \(18.0.0\)

</td><td>

 

</td><td>

1.  Open the Now Mobile app.
2.  Enter the instance name.
3.  Log in as an administrator.
4.  Select the 'Support' tab at the bottom of the page.
5.  Observe the page.

 Expected behavior: 'Article' is translated.

 Actual behavior: 'Article' isn't translated.

</td></tr><tr><td>

Employee Center

 PRB1788890

</td><td>

The 'My active item' widget's request count loop isn't breaking even after counting 10 records

</td><td>

If the 'My request' filters \('request\_filter'\) table's request filter has more than 10 records, then getRequestsCount\(\) function's logic is looping over all records to get the count and isn't respecting the ITEM\_SUMMARY \_COUNT\_LIMIT variable.

</td><td>

 

</td></tr><tr><td>

Employee Center

 PRB1799296

 [KB1703119](https://hi.service-now.com/kb_view.do?sysparm_article=KB1703119)

</td><td>

Special characters aren't displayed correctly on the portal

</td><td>

Special characters aren't displayed correctly in 'My Tasks' or the 'HRM TODOs' page on the portal.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Employee Center Pro

 PRB1754194

 [KB1649141](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649141)

</td><td>

Opening a record from the 'Pages' tab opens an invalid URL, causing page errors on the esc portal

</td><td>

When selecting a topic 'Page' AI search result, it opens the expected topic page, but it displays the sys\_ID in the URL instead of the page ID. There's javascript errors once on the page. Errors include: 'Server JavaScript error The undefined value has no properties.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Encryption Support

 PRB1788684

</td><td>

The module key isn't generated after the import is uploaded for Column Level Encryption Bring Your Own Key \(CLE BYOK\)

</td><td>

The wrapped key material and import are deleted.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1688635

</td><td>

System Center Operations Manager \(SCOM\) limits the value of 'context' to 540 characters

</td><td>

When a SCOM event is inserted into the em\_event table, parts of the JSON string is missing from the **additional\_info** field. The MID log shows that the payload is fully intact and contains the full XML structure, but almost half the string is missing when it is written to the database. If the context is shorter than 540 characters, the SCOM alert is coming up correctly with no truncation occurring. The SCOM alert is truncated if the context if over 540 characters.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1790120

 [KB1652694](https://hi.service-now.com/kb_view.do?sysparm_article=KB1652694)

</td><td>

If the sys\_flow\_context table size is above 100 million during an upgrade from Vancouver, Flow Engine V2 new columns aren't added

</td><td>

New columns introduced by the Flow Engine V2 aren't added as expected when upgrading to Washington DC and beyond from a pre-Washington DC family, which can cause the symptom where new flows error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1792828

</td><td>

Possible data leak and race condition due to a mutation in the compiled flow

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1794986

</td><td>

The table cleaner rule on 'sys\_flow\_context\_inputs\_chunk' is not deleting records due to the 'disable table cleaner' dictionary attribute

</td><td>

A table cleaner rule and index was introduced in PRB1717537 for the Washington release to address excessive growth of the sys\_flow\_context\_inputs\_chunk table.

</td><td>

1.  Create records in the sys\_flow\_context\_inputs\_chunk table before 2,419,200 seconds ago in an instance on Washington DC.
2.  Ensure the fix from PRB1717537 is introduced.
3.  Ensure the table cleaner rule and the index 'sys\_created\_on' has been created for the sys\_flow\_context\_inputs\_chunk table.
4.  Run the table cleaner scheduled job.

 Expected behavior: Records from the sys\_flow\_context\_inputs\_chunk table are deleted.

 Current behavior: Notice the message in the logs 'Skipping cleanup of table sys\_flow\_context\_inputs\_chunk because it has the disableTableCleaner table attribute set'.

</td></tr><tr><td>

Flow Engine

 PRB1799845

</td><td>

The sys\_flow\_context schema attribute 'iterative delete' did not set to 'false' on an upgraded instance

</td><td>

 

</td><td>

1.  Request an earlier instance than Xanadu.
2.  Ensure the default value for sys\_flow\_context schema attribute 'iterative delete' is set to 'true'.
3.  Upgrade the instance to Xanadu.

 Expected: The sys\_flow\_context schema attribute 'iterative delete' is the value 'false'.

 Actual: The sys\_flow\_context schema attribute 'iterative delete' is the value 'true'.

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1798050

</td><td>

HLA SysLog Data Input isn't working upon start

</td><td>

The script include used by this data input doesn't exist in older versions and therefore the data input is broken.

</td><td>

1.  Navigate to the data input menu.
2.  Create a glide SysLog data input.
3.  Select **Start**.

 Notice that an error is presented and data input can not be started.

</td></tr><tr><td>

Horizon Component Library

 PRB1779573

</td><td>

now-content-tree height is fixed on drag-drop, making the expand operation odd

</td><td>

 

</td><td>

1.  Render now-content-tree with nested levels.
2.  Enable drag-drop.
3.  Keep items collapsed.
4.  Do any drag drop operation.
5.  Expand a few tree items.

 Expected behavior: The items should be expanded and visible with the height based on the size of the tree.

 Actual behavior: The height is fixed and on expand, a scroll bar appears and users must scroll to view the contents in the limited fixed height.

</td></tr><tr><td>

Horizon Component Library

 PRB1791908

</td><td>

Keyboard focus is misplaced on a banner notification pop-up, requiring multiple tab key taps to return focus to the **Close** button

</td><td>

Users with motor impairment often use only a keyboard and rely on quick and efficient navigation. This behavior doesn't allow the banner to be readily dismissed and forces to the user into extra tab stops. Additionally, the banner covers focusable content.

</td><td>

1.  Log in to any instance.
2.  Navigate to any list within any workspace, such as CSM.
3.  Select at least one record from the list \(select the checkbox\) to enable the **Export** button.
4.  Select **Export**.
5.  Select **Export** again on the modal.

Upon completion of the download, observe a notification banner at the top of the page.


 Expected behavior: Keyboard focus lands on the **X** or **Close** button of the notification banner.

 Actual behavior: Keyboard focus is behind the banner and the user needs to tab multiple times to bring focus back to the banner to dismiss it.

</td></tr><tr><td>

Horizon Popover Component

 PRB1802443

</td><td>

The now-popover repositions on a scroll of its ancestors only if it has a showroot and breaks when the scroll is defined on the window/document

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Incident Management

 PRB1786090

</td><td>

Plugins for com.snc.itsm.roles. problem\_management /incident\_management/ request\_management are experiencing longer upgrade times

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Incident Management

 PRB1788130

</td><td>

Opt-in mechanism for Change-Hardware Assest Management \(HAM\) integration

</td><td>

Users can opt-in for change request asset action validations. Users should be able to move the change request to 'review state' without an asset action even if the property is turned off.

</td><td>

 

</td></tr><tr><td>

Incident Management

 PRB1798497

</td><td>

A Glide aggregate query on the 'Impacted Services' table throws an error for sn\_incident\_read user

</td><td>

There's a 400 ms performance degradation because of the GlideRecord Collection query that is used to fetch the aggregate counts for the assets, impacted services, and affected CIs.

</td><td>

1.  Log in as an sn\_incident\_read user.
2.  Open **Service Operations Workspace** &gt; **List** &gt; **Incidents** &gt; **All**.
3.  Open any one of the incidents from the list.
4.  Check the single-score cards on the impact section for the assets, impacted services, and affected CIs.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1780273

</td><td>

There's a null point exception in the IDRProducerJob which prevents the cursor from advancing and halts all replication

</td><td>

An error displays: 'Stack Trace java.lang.NullPointerException: null, com.glide.idr.definition .ReplicationSetRegistry...'

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1799179

</td><td>

Action execution fails with 'No implementation for IExternalCredentialGCFCollector was bound'

</td><td>

This is happening because 'IntegrationConnection DataResolverOperation' is running on an instance for the subflow's first action. Therefore, it runs fine. For the second action, it seems to be running on MID. So, the issue occurs when two consecutive actions in a subflow use MID server. For the second one using MID, the environment seems to be shifting to MID.

</td><td>

1.  Create a Xanadu instance with MID Server.
2.  Create a connection and credential alias.
3.  Configure the connection to use MID server.
4.  Create an action with a REST step using the previous alias and publish it.
5.  Create a subflow and add the created action multiple times.
6.  Test the subflow.

 Observe that subflow's step 1 completes, but fails on step 2 with an error.

</td></tr><tr><td>

Internationalization Features

 PRB1787388

</td><td>

After upgrading to Washington DC, getDisplayValueLang\(\) doesn't return the expected results

</td><td>

Both the dollar symbol and the comma are dropped from a value in a currency field by getDisplayValueLang.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1771941

</td><td>

The existing script include in the Smart Operations application requires access to the Key Management Framework script include 'sn\_kmf.ScopedRevokeCertificate'

</td><td>

The existing script include 'sn\_smartops.SmartOpsCertificateSNC' in the Smart Operations application requires access to the 'revokeCertificateById' method in KMF script include 'sn\_kmf.ScopedRevokeCertificate'.

</td><td>

1.  Navigate to the 'sys\_restricted\_caller\_access' table on a Washington DC instance.
2.  Search for records with the source scope is 'Smart Operations' \(sn\_smartops\).

 Observe that no record is present to provide access for the 'sn\_kmf.ScopedRevokeCertificate' script include.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1781799

</td><td>

Provision instance email automation is completed, but email servers aren't created on the user instance for GovCommunityCloud \(GCC\)

</td><td>

The automation completes successfully with no errors in the logs, but the email servers aren't created or updated on the instance.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1794818

 [KB1699639](https://hi.service-now.com/kb_view.do?sysparm_article=KB1699639)

</td><td>

Vancouver instances with Washington DC data may fail to come online after being upgraded to Xanadu

</td><td>

This is an upgrade edge case.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1798919

</td><td>

A null pointer exception is observed when the input text for SYMMETRIC\_ENCRYPTION contains ':'

</td><td>

The issue can be reproduced only when the com.glide.encryption \(Column Level Encryption\) plugin is inactive.

</td><td>

 

</td></tr><tr><td>

Legal Simple Contracts

 PRB1798642

 [KB1700971](https://hi.service-now.com/kb_view.do?sysparm_article=KB1700971)

</td><td>

Attachments on contract document revision records are deleted

</td><td>

Attachments on contract document revision records stored in the ServiceNow-based storage are deleted. Finalized contracts aren't impacted by this defect.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1779205

</td><td>

The 'Asset refresh order' filter tooltip text doesn't receive focus

</td><td>

The tooltip text to the right of the **Assets** and **Filter** buttons on the 'Enterprise Asset Refresh Order' form doesn't receive screen reader focus. Users can navigate to the button but the text doesn't receive focus.

</td><td>

1.  Enable a screen reader.
2.  Navigate to an instance.
3.  Log in as an admin.
4.  From the 'All' menu, open the service catalog.
5.  Select 'Enterprise asset lifecycle'.
6.  Select the 'Enterprise Asset Refresh Order' catalog item.
7.  Select the location, replacement model, and assets.
8.  Move the screen reader focus to the assets/filters tooltip.

 Expected behavior: Screen reader users can access the tooltip text.

 Actual behavior: Screen reader users can't move focus to or access the tooltip text.

</td></tr><tr><td>

List Administration

 PRB1788744

</td><td>

An action configured through row actions in the 'Presentational' list isn't dispatched

</td><td>

 

</td><td>

1.  Log in to any instance.
2.  Navigate to url/now/lists-demo/presentational-list.
3.  Open the dev tools 'Actions' tab.
4.  Select the row action **ADD**.

 Expected behavior: It should show the ADD\_ACTION event in dev tools.

 Actual behavior: It doesn't dispatch any action.

</td></tr><tr><td>

List Administration

 PRB1789036

</td><td>

Uptake the enableFocus property for internal uses of now-alert/now-alert-list within the 'Lists' component

</td><td>

Include the enableFocus property to the message payload for any dispatches to the UXF notification handler where focus can safely be moved to the alert. Users with motor impairment often use only a keyboard and rely on quick and efficient navigation. This behavior doesn't let the banner be readily dismissed and forces to the user into extra tab stops. Additionally, the banner is covering focusable content.

</td><td>

1.  Log in to any instance.
2.  Navigate to any list within any workspace.
3.  Select at least one record from the list \(select the checkbox\) to enable the **Export** button.
4.  Select **Export**.
5.  Select **Export** again on the modal.
6.  Upon completion of the download, verify that there's a notification banner at the top of the page.

 Expected behavior: The keyboard focus lands on the **X** or **Close** button of the notification banner.

 Actual behavior: The keyboard focus is behind the banner. The user must tab multiple times to bring the focus back to the banner to dismiss it.

</td></tr><tr><td>

List Controller

 PRB1789532

</td><td>

The 'Open Panel' event doesn't allow for reusability outside of list-controller

</td><td>

 

</td><td>

1.  Open a record list bundle in UI Builder.
2.  Add a button to the page.
3.  Bind the event to 'Open Panel' list controller.
4.  In the event, add a field object of '\{sysId: &lt;sys id of first row&gt;'.
5.  In the event, add the route 'quick-edit'.
6.  Save.
7.  Open the app.
8.  Trigger the button.

 The pane doesn't open as expected.

</td></tr><tr><td>

Major Incident Management

 PRB1791586

</td><td>

A blank choice appears when adding a collaborative communication task in the Major Incident Workbench after upgrading the Service Operations Workspace \(SOW\)

</td><td>

After upgrading SOW to the latest version, on Major Incident Workbench, users are seeing a blank choice when adding a collaborative communication task.

</td><td>

1.  Open a major incident.
2.  Select **Workbench**.
3.  Navigate to **Collaborate** &gt; **Add** &gt; **Channel Dropdown**.

 Notice that the channel dropdown has a blank choice.

</td></tr><tr><td>

Microsoft Word Addin for ServiceNow Contracts

 PRB1798656

</td><td>

Files are deleted after a week due to a scheduled job in the Microsoft Word addin

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Natural Language Query \(Family Release\)

 PRB1770635

</td><td>

Group by queries don't work for CMDB\_WS or CMDB\_QB sources

</td><td>

When a script is executed in the Engineering Details in 'scripts - background', the results say '"errorMessage":"FAIL: type invalid for source of query","output\_source":"GAI","nlqQueryLog TableSysId":"cf207c fc43a20210a8fc3 9603ab8f2ac"\}'.

</td><td>

 

</td></tr><tr><td>

Now Assist for HRSD

 PRB1795282

</td><td>

Now Assist Virtual Agent triggers sensitivity detection for all utterances for upgrade customers

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist for HRSD

 PRB1797507

</td><td>

More utterances are giving false sensitivity

</td><td>

Normal questions are classified as sensitive under personal or health issues. When users phrase their utterances with certain conjunctions, it can lead to more false positive cases of sensitivity.

</td><td>

 

</td></tr><tr><td>

Now Mobile - Employee Experience

 PRB1744741

</td><td>

The 'Save a draft' function can only save some variables on a catalog item

</td><td>

Some fields are left blank when an incident is saved.

</td><td>

1.  Open Now Mobile 17.3.0 and log in \(Washington DC requires the latest mobile app version\).
2.  Select the **Request IT assistance** quick link.

The user is re-directed to the 'Create incident' catalog item.

3.  Input the urgency and description, then **Save a draft**.
4.  Navigate to 'My request'.
5.  Open the draft.

 Expected behavior: Both the urgency and description should be saved.

 Actual behavior: The description is saved as blank.

</td></tr><tr><td>

Now Mobile - Employee Experience

 PRB1785198

</td><td>

The 'Date' variable displays no default in languages other than English

</td><td>

When Record Producer is opened in Service Workspace Portal and Mobile Service Portal, the 'Date' variable is prefilled correctly. However, when it is opened again in both portals, the variable isn't prefilled correctly in Mobile Service Portal.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1780866

</td><td>

The on-call schedule reminder email doesn't have accurate information

</td><td>

The dates are incorrect.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1788633

</td><td>

Selecting the 'Primary user' icon opens multiple cards in on-call schedules

</td><td>

Selecting the 'Primary user' icon opens multiple cards shifts which have no members in the roster and are covered by coverages.

</td><td>

1.  Open an instance.
2.  Navigate to **All** &gt; **On-Call Scheduling** &gt; **On-Call Schedules**.
3.  Identify a rota.
4.  Select the 'Primary user' icon.

 Observe that the card expands.

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB1781569

</td><td>

pa\_tabs.name is changed after update set transfers

</td><td>

This is due to the update set's export/import mechanism stripping the separator between the sys\_id and the name of the tab.

</td><td>

1.  Install two instances with the com.snc.i18n.japanese plugin installed.
2.  Log in to the first instance as an admin.
3.  Display a dashboard.
4.  Select**Dashboard menu** &gt; **Create Tab**.
5.  Select the 'Edit tab' icon on the tab created in step 4.
6.  In the 'Rename tab', input Japanese text.
7.  Select **OK**.
8.  Select **Dashboard menu** &gt; **Dashboard properties**.

The record of pa\_dashboards is displayed. 'Tab name' is displayed normally in the **Tab** field of the 'Dashboard Tabs' related list.

9.  **Preferences** &gt; **Languages and Region**, change the language to Japanese.

 Observe that 'Tab name' is displayed with the sys\_id of pa\_tabs record in the **Tab** field of the 'Dashboard Tabs' related list.

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB1795213

</td><td>

A tab name is truncated in a Washington DC mainline instance

</td><td>

Tab names are truncated.

</td><td>

1.  Create a dashboard with two tabs.
2.  Make sure that the tab names are more than 32 characters long.
3.  Edit the tab records and delete the sys\_ID but keep the rest of the name.
4.  Load the dashboard again.

 Notice that the tab names are truncated.

</td></tr><tr><td>

Performance Analytics

 PRB1788449

</td><td>

NLQ isn't working as expected for GLOBAL\_NAVIGATION source

</td><td>

If two changes are made for the same files but are adding for different sources, the conflicts aren't handled properly.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1802121

</td><td>

com.glide.par.coreui .migration.enabled doesn't block migration activation

</td><td>

Migration can be activated via the API call.

</td><td>

1.  Select **Start moving** in Migration Center.
2.  Set com.glide.par.coreui .migration.enabled to false.

 Expected behavior: API call should fail.

 Actual behavior: Migration can still be activated via the API call.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1781302

</td><td>

Processes created in Paris and opened post-Paris have a lane order set to -1

</td><td>

 

</td><td>

1.  Create a process in Paris.
2.  Open the process in an instance post-Paris.

 Expected: The lane order is preserved.

 Actual: The lane order is set to -1.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1781451

</td><td>

Only the first activity is valid when a playbook definition run condition reference is duplicated

</td><td>

 

</td><td>

1.  Create a playbook definition with three or more activities.
2.  Add a run condition to the third activity.
3.  Reference the first two activities.
4.  Duplicate the playbook definition.

 Expected behavior: The duplicated playbook definition does not contain any invalid reference errors.

 Actual behavior: The second activity reference is invalid.

</td></tr><tr><td>

Portfolio Planning with PPM, Agile 2.0, and SAFe

 PRB1800163

 [KB1702516](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702516)

</td><td>

The **rm\_epic.portfolio** field created on instances has the same field on the sn\_safe\_epic child table

</td><td>

Portfolio Planning with PPM, Agile 2.0, and SAFe \[com.sn\_align\_cmn\_int\] application version 4.4.0 installs the **rm\_epic.portfolio** field. This can create an issue on instances where the Agile - Scaled Agile Framework - Portfolio SAFe \[com.snc.sdlc.portfolio\_safe\] plugin is active, because then the same field already exists on sn\_safe\_epic, child table of rm\_epic.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Predictive Intelligence

 PRB1793563

</td><td>

ML Solution events aren't fired when the clustering training request is scheduled by the system

</td><td>

In the process mining application, 2 ml\_solution events are used to know when the ml\_solution of clustering is completed. They are set via a business rule \(BR\) which checks the training scheduled request from the ml\_training\_request\_schedule table. Since the training request of the clustering is scheduled by the system, the BR never fires the event. Because of this, it doesn't say when clustering is completed.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1798054

</td><td>

An error reading 'Illegal parameter: null: no thrown error' is thrown when trying to fetch properties of active java solutions for clustering and similarity

</td><td>

JSON parsing on properties with null values results in this redundant error log to be thrown. This is a redundant error message without any impact on pipelines.

</td><td>

 

</td></tr><tr><td>

Proactive Analytics

 PRB1803059

</td><td>

Indicator Model Score generation failure

</td><td>

When a job runs, users observe null point exceptions in WidgetService and DashboardProvider. These are dependant services in the indicator model score generation and are unexpected errors.

</td><td>

 

</td></tr><tr><td>

Process Mining for Performance Analytics

 PRB1800156

</td><td>

The **Run process analysis** button on KPI details and Analytics Hub isn't visible

</td><td>

In Xanadu, there's a process mining evaluation project for incident management. Users can trigger the evaluation project from within Analytics Hub details by selecting the 'Process mining' icon. As part of Xanadu, the button was made bigger. This button isn't visible and the previous button still displays.

</td><td>

1.  Navigate to an instance not entitled from Program Management and where the entitlement check is turned on.
2.  Navigate to the KPI details/Analytics Hub of an incident-related KPI.

 Expected behavior: A new, big icon 'Run process analysis' is on the right side of the Analytics Hub/details.

 Actual behavior: A small 'Process mining' icon appears on the Analytics Hub \(no text\).

</td></tr><tr><td>

Process Mining

 PRB1785806

</td><td>

The sys\_ux\_lib\_component file is missing required translation keys

</td><td>

In Xanadu, the sys\_ux\_lib\_component file is missing the required\_translation\_keys for now-diagram. The issue isn't reproducible in Washington DC.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1792041

</td><td>

Work notes analysis isn't working on a support instance

</td><td>

 

</td><td>

1.  Install the Dynamic Translation plugin.
2.  In the left navigation, navigate to 'Translator Configuration'.
3.  Set any other provider to 'Active' and set it as default for detection.
4.  Initiate Work Notes Analysis.

 Expected behavior: Work Notes Analysis should be completed with any default translator.

 Actual behavior: Work Notes Analysis failed because the provider isn't active.

</td></tr><tr><td>

Process Mining

 PRB1793119

</td><td>

An error message occurs when the breakdown filter set with the 'Empty' category, and the filter doesn't get applied

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1711919

</td><td>

Values under 1000 don't copy into the 'Benefit Plan' grid in the Planning Console

</td><td>

Planning Console grid paste isn't working for values under 1000.

</td><td>

1.  Open any project.
2.  Open the planning console.
3.  Navigate to **Financials** &gt; **Monetary Benefit Plans**.
4.  Create a New Benefit Plan with '0' as the entered benefit.
5.  Open an Excel worksheet.
6.  Enter '10.11' into three columns.
7.  Copy all three columns.
8.  Paste the columns into the 'Benefit Plan' grid.
9.  Notice that the value 10.11 doesn't save into the 'Benefit Plan' grid.
10. Navigate back to Excel.
11. Enter '2000.11' in three columns.
12. Copy all three columns.
13. Paste the columns into the 'Benefit Plan' grid.

 Notice that the value 2000.11 is saved into the 'Benefit Plan' grid.

</td></tr><tr><td>

Project Management

 PRB1786998

</td><td>

Remove sn\_spm\_financial\_user to project\_manager and demand\_manager

</td><td>

Any teamspace project/demand manager can able to view other teamspace projects/demands as sn\_spm\_financial\_user is added to project\_manager and demand\_manager.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1792775

</td><td>

Cost values on task type breakdowns aren't populated

</td><td>

Cost values on task type breakdowns and investment and planning items on benefit plans aren't populated.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1797258

</td><td>

Required fixes for project insight snapshot fields in Project Portfolio Management \(PPM\) Standard

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Remote Tables

 PRB1772531

</td><td>

An aggregate query with a condition doesn't work for a remote table with enhanced capacity enabled

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Resizable Panes Component

 PRB1773094

</td><td>

Components that use now-trigger-library for keyboard shortcuts aren't deregistering

</td><td>

 

</td><td>

1.  Install the base agent workspace.
2.  Navigate to sys\_properties.list.
3.  Set the sn\_appclient.app.install.offline to 'true'.
4.  Clear the cache.
5.  Navigate to **Plugins** from the navigator.
6.  Select **Sync Store**.
7.  Refresh and clear the cache.
8.  Install sn\_app\_demo\_aw.
9.  Navigate to **Now** &gt; **Demo** &gt; **baseaw**.
10. Navigate to **All Incidents**.
11. Open any record.
12. Close the record.
13. Repeat step 2 and step 3.
14. Open Chrome DevTools.
15. Open up console.
16. Access the uxfTriggerLibrary.
17. Notice there are entries in the map with references to components that did not deregister.

 Expected behavior: Components that use now-trigger-library are deregistered, and the reference which hosts and updates the state of the component isn't kept.

 Actual behavior: The uxfTriggerLibrary continues to grow as components aren't deregistered.

</td></tr><tr><td>

Schedule Calendar

 PRB1794379

</td><td>

The Next UI Schedule Calendar doesn't save updates to the 'Repeat Until' date in the schedule entry

</td><td>

The 'Repeat Until' date does not save when it's updated in the schedule entry.

</td><td>

1.  Open a Washington DC instance.
2.  Navigate to **Show Schedule**.
3.  Open a schedule in the Next UI calendar view.
4.  Edit a repeating schedule entry where the **Repeat Until** field is empty.
5.  Set a date in the **Repeat Until** field.
6.  Save the changes.
7.  Observe the message 'Event updated successfully'.
8.  Open the schedule entry.
9.  Verify the date has been entered in the **Repeat Until** field.

 Expected behavior: The 'Repeat Until' date is in the schedule entry.

 Actual behavior: The **Repeat Until** field is blank in the schedule entry.

</td></tr><tr><td>

Schedule Optimization

 PRB1790119

</td><td>

Filter out locked tasks with an invalid location

</td><td>

Locked, or restricted, tasks with an invalid location \(no latitude, no longitude, no latitude and longitude\) cause the 'Schedule Optimization' job to error out.

</td><td>

1.  Set up a work order task with an invalid location \(remove latitude &amp; longitude for any address\).
2.  Assign the task and set schedule\_lock = true.
3.  Perform a Graph QL query for the batch/intraday.

 Expected behavior: The task should be filtered from locked\_tasks for an invalid location.

 Actual behavior: The task would be returned as part of locked\_tasks.

</td></tr><tr><td>

Seismic Framework

 PRB1792811

</td><td>

Service workers don't cache non-200 glide requests

</td><td>

 

</td><td>

1.  Spin up glide or a mock HTTP server.
2.  Respond with a 500 glide response.

 See that service workers responds to subsequent requests with a cached text or document.

</td></tr><tr><td>

Server-side scripts

 PRB1767574

</td><td>

Unable to use the require function in an ESLatest script include if invoked cross-scope from an ES5 scope

</td><td>

 

</td><td>

1.  Create an ES6 scope and an ES5 scope.
2.  Create a module in the ES6 scope.
3.  Create a script include in the ES6 scope that uses the module.
4.  Make the script include accessible from all application scopes.
5.  Invoke the script include from background scripts from the ES5 scope and ES6 scope.

</td></tr><tr><td>

Server-side scripts

 PRB1790567

</td><td>

Enabling ModuleSupport breaks on scopes with compiled scripts

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1793034

</td><td>

There's a performance degradation in builds between 07/19 and 07/30

</td><td>

Test results display a degradation in performance in multiple KPIa \(mostly in App CPU and transactions response time\).

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1777834

 [KB1648430](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648430)

</td><td>

The field message of the catalog UI policy actions aren't translated to a non-English language in Service Portal

</td><td>

In Service Portal, translation of field messages rendered from catalog UI policy actions aren't working as expected.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog

 PRB1797273

</td><td>

The Virtual Agent \(VA\) chat shows an error when g\_form.addOption is used in client script

</td><td>

 

</td><td>

1.  Created a record producer 'Create Magic' in Global Scope.
2.  Navigate to the Employee Center
3.  Open the Virtual Agent \(VA\) chat.
4.  Enter 'magic' in the chat.
5.  Select the catalog named 'magic'

 Expected: The VA chat asks a relevant question.

 Actual: The VA chat fails to ask a relevant question.

</td></tr><tr><td>

Service Catalog

 PRB1804801

</td><td>

There's an error on workspace catalog form when creating an incident request

</td><td>

There's an error that reads 'ReferenceError: g\_prevent\_access\_from\_console is not defined'.

</td><td>

1.  Provision the latest catalog builder or WDC-P8 build.
2.  Navigate to **Incident** &gt; **Create request** and open any item.

 Observe the error in the console: 'ReferenceError: g\_prevent\_access\_from\_console is not defined'.

</td></tr><tr><td>

Service Mapping

 PRB1794723

 [KB1699268](https://hi.service-now.com/kb_view.do?sysparm_article=KB1699268)

</td><td>

'Refresh processes and connections' marks all cmdb\_running\_process as absent true

</td><td>

The sensor 'Windows - ADM Multiple' was originally created by duplicating the 'Windows - ADM' sensor to run at a higher frequency. Changes made to the original sensor weren't automatically applied to our sensor, which led to an error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Mapping

 PRB1795155

</td><td>

The replication lag protection in recomputation doesn't support standby lag

</td><td>

RecomputationHandler. isReplicationLag AboveThreshold\(\) checks for read replica lag. If it's above the max allowed threshold \(30 min\), the job cancels. DBThrottlePoolsManager.get\(\) .getReplicationLags\(\) should do the same for the standby lag.

</td><td>

 

</td></tr><tr><td>

ServiceNow for Teams - Core

 PRB1783810

</td><td>

EC in teams/unfurling flows are failing due to an authentication error

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1781293

</td><td>

com.glide.encryption. enable\_attachment\_ key\_ui=TRUE has different behavior in Xanadu

</td><td>

When com.glide.encryption. enable\_attachment\_ key\_ui=FALSE there's no issue. In Washington DC, the property is set to true but the issue didn't occur.

</td><td>

1.  Log in to an instance.
2.  Navigate to any Catalog/Record Producer \(select **Request on Header**\).
3.  Select **Add attachment**.

 Expected behavior: The encryption dialog doesn't display when in platform or HR portal.

 Actual behavior: The encryption dialog displays.

</td></tr><tr><td>

Service Portal

 PRB1794691

</td><td>

The 'Business Services Status' widget displays different dates for Japanese and English modes

</td><td>

The issue is reproducible in Washington DC but not Vancouver.

</td><td>

1.  Provision an instance with the Japanese language plugin \(com.snc.i18n.japanese\) activated.
2.  Switch to English mode.
3.  Open the 'System Status' page in portal.
4.  Find the status history in the page and check the dates.

It should be last 5 days include today.

5.  Switch to Japanese mode.
6.  Repeat steps 3-4.

 Expected behavior: The dates should be the same as the English mode, with the last 5 days including today.

 Actual behavior: The dates are displaying the last 5 days except today.

</td></tr><tr><td>

Service Portal

 PRB1794718

</td><td>

A knowledge category displays as '\{\{::category.label\}\}' when the language is non-English

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reclamation

 PRB1792829

 [KB1698752](https://hi.service-now.com/kb_view.do?sysparm_article=KB1698752)

</td><td>

A 'Maximum JavaScript call depth of 1000 exceeded' error is thrown in the SAMPPreBuiltSuitesAPI. lookupSuiteComponents function call

</td><td>

If a suite parent has a suite child with the same product, there could be a case where the lookupSuiteComponents\(\) function calls addM2MSuiteComponentProducts\(\). This again calls lookupSuiteComponents\(\), and so leading to an infinite loop.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB1794331

</td><td>

Performance issue in clearing LMRs for entitlements

</td><td>

SamPublisherCalculator's cleanUpEntitlementsByPublisher\(\) gets stuck.

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB1794335

</td><td>

If there's many entitlements, there's a performance issue in SuiteEngine

</td><td>

A query per entitlement is fired to get its consumption rules. When there's many entitlements, the query takes forever. In general, there's far less consumption rules than entitlements.

</td><td>

 

</td></tr><tr><td>

Software Lifecycles

 PRB1756991

</td><td>

A lifecycle report should be able to handle empty lifecycle dates

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Survey Management

 PRB1797560

</td><td>

An error message appears when the date type field isn't updated when retaking survey

</td><td>

A required date type file has an error 'Some fields are incomplete' when the user is retaking the survey without updating that field. The symptom only happens on a date type question.

</td><td>

1.  Open an instance.
2.  Impersonate a system administrator user.
3.  Open a completed survey.
4.  Select **Get started** to retake the survey.
5.  Select **Submit** without changing the **new date** field.

 Expected behavior: The survey is submitted.

 Actual behavior: The error message 'ErrorSome fields are incomplete: New Date' appears and the survey can't be submitted.

</td></tr><tr><td>

Table Administration and Data Management

 PRB1796193

</td><td>

A sysauto\_script isn't present in a database

</td><td>

The script enables instant alter glide.db.instant\_alter.enabled.

</td><td>

 

</td></tr><tr><td>

Table Cleaner

 PRB1783267

</td><td>

There's uncontrolled growth of table sys\_cluster\_message

</td><td>

The table size increases infinitely.

</td><td>

1.  In background scripts, run the script new GlideTableCompactor\(\).cancel\(\).
2.  Check sys\_cluster\_message.list.

 Notice that there's one new entry per node every 15 seconds.

</td></tr><tr><td>

Table Cleaner

 PRB1785452

</td><td>

The sys\_dm\_run job is stuck in a processing state for &gt;8 days when multiple sys\_auto\_flush rules are triggered

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Table Cleaner

 PRB1791673

</td><td>

Hex Cleaner doesn't delete sys\_attachment\_doc when directly invoked on sys\_attachment

</td><td>

 

</td><td>

1.  Add some records to the sys\_attachment table.
2.  Create auto flush on sys\_attachment with conditions matching the above inserted records.
3.  Force Hex Cleaner by running the dmDMjob.

The Hex Cleaner threshold can be changed 'glide.db.tablecleaner.hex\_cleaner\_threshold' to a lower number to force the Hex Cleaner.


 Expected behavior: Both sys\_attachment and sys\_attachment\_doc should be removed.

 Actual behavior: Only sys\_attachment is removed.

</td></tr><tr><td>

Table Cleaner

 PRB1792483

</td><td>

Non-nibble table cleaners are cleaning data even when the child match field passes

</td><td>

 

</td><td>

1.  Create a TPH table with columns.
2.  Add 'short\_description'.
3.  Create a child table extending the above TPH table.
4.  Add a new column to the child table of the 'type glide\_date\_time'.
5.  Add 'child\_date\_time'.
6.  Add records to the the base table with the short\_description such as 'person\_1'.
7.  Add records to the child table with the short\_description starting with 'person\_1'.
8.  Add any date\_time to the child\_date\_time column.
9.  Create an auto flush on the parent TPH table with the condition 'short\_description starts with person\_1'.
10. Add the match\_field as 'child\_date\_time' and age so the record matches the date and time condition on the child table.
11. Run the table cleaner.
12. Notice that the records are deleted.

 Expected: Rows are not deleted because the match field only exists on the child table.

 Actual: All rows from both the parent and child tables with short\_description starting with 'person\_1' are deleted.

</td></tr><tr><td>

Table Cleaner

 PRB1797448

</td><td>

Turn on chunking for the hex cleaner

</td><td>

Hex cleaner is firing one pass queries to delete data when it should be firing two pass queries.

</td><td>

 

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

</td></tr><tr><td>

UI Field Administration

 PRB1799414

</td><td>

The decimal field doesn't register the user's country code and system language, and uses a period instead of a comma as a decimal separator in the legacy workspace

</td><td>

 

</td><td>

1.  Log in to a Vancouver or Washington DC instance.
2.  Install the com.snc.i18n.german plugin.
3.  Set the system property to glide.system.locale - en.
4.  Create a user with the country code 'Germany and Language - Deutsch'.
5.  Navigate to incident.LIST.
6.  Open any record.
7.  Add a decimal field to the form.
8.  Add '1,000.53' in the field.
9.  Save the changes.
10. Impersonate the user that was created.
11. Navigate to the incident record with the added field and value.

Notice that the decimal field is changed to 1.000,53.

12. Navigate to the legacy agent workspace and open the same incident record.

 Notice the decimal field isn't changed, and is displayed as 1,000.53.

</td></tr><tr><td>

UI Form Administration

 PRB1794967

</td><td>

Special handling notes overflow beyond the modal container

</td><td>

Reproducible in Washington DC and Xanadu.

</td><td>

 

</td></tr><tr><td>

UXF Components

 PRB1782803

</td><td>

Support for accessing current URLs in the UX client script

</td><td>

A URL should be accessible in the client script so that BU's can dynamically generate a URL based on their use case.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1780371

</td><td>

Context app bindings aren't working with nested macroponents on an initial load

</td><td>

The UI action **Save** on the table is visible only after a browser refresh with the record lookup component.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1788420

</td><td>

A tab set component now expects the initial value of an empty array causing a regression in builds that allow empty objects

</td><td>

The 'Success Portfolio' overview landing page are missing tabs: 'Active touchpoints', 'Active Success cases' , 'Active Risk Signals', and so on.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1793083

</td><td>

Having multiple scripted conditions on repeaters causes a collision and resolving in blank page

</td><td>

When multiple scripted conditions are added to a repeater for properties like 'repeatsWith' and 'isHidden' the page doesn't load at all and throws an 'Internal Server Error 500'.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1798658

</td><td>

The **To** recipient field isn't displayed because of the email header in Customer Service Management \(CSM\) Configurable Workspace

</td><td>

The **To** data pill is hidden in Now Email Client Viewer on the initial load of a workspace page.

</td><td>

1.  Open a base instance.
2.  Open the incident table attributes.
3.  Turn off the document viewer with the following steps:
    1.  Navigate to **System Definition** &gt; **Dictionary**.
    2.  Search for the table.
    3.  Open the record with the 'Collection' type field.
    4.  Enter 'Use Document Viewer' in the attribute field.
    5.  Enter 'false' in the value field.
    6.  Open incident email record in the email viewer.

 Observe that upon opening the email, recipients in the **To** field aren't displayed unless the 'Hide Email Header/Show Email Header' is selected.

</td></tr><tr><td>

Virtual Agent Designer

 PRB1788742

</td><td>

The Talent Development helper topic isn't discovered

</td><td>

The Talent Development topic should get discovered and it should go through the various talent flows, like getting skills, growth plans, and so on, based on the utterance.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1776622

</td><td>

The post-chat survey displays in the agent's language rather than the requester's language

</td><td>

There could be a live agent chat where the agent is conversing in a language other than English and the chat requester is in English. If the agent ends the chat via the **End chat** button, the post-chat survey is launched under the agent's user thread. If there's translations for the asmt\_metric\_definition records in sys\_translated\_text for those definitions, the agent's language preference is used to read the survey records and is displayed in the agent's language to the chat requester.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1793423

</td><td>

During an upgrade, skill search tracking throws an error when handling a skill search timeout

</td><td>

Conversation server worker transaction exception: 'java.lang.IllegalArgumentException: No enum constant...'

</td><td>

1.  Set up Now Assist for Virtual Agent.
2.  Perform skill searches and conversations during an upgrade.

 Observe that conversations move to the error topic when a skill search times out.

</td></tr><tr><td>

Virtual Agent

 PRB1800743

</td><td>

SensitiveDataHandling unmasking won't work if the value contains a '$' character

</td><td>

The replaceAll method is used to replace masked text with unmask text. Because the method is expression based, the appearance of a $ character causes unexpected behavior, such as the IndexOutOfBoundsException error.

</td><td>

 

</td></tr><tr><td>

Word Document APIs

 PRB1805330

</td><td>

There's test failures for the renderDocument API on Xanadu

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1784924

</td><td>

Updates made to the wm\_task.state label in the platform aren't reflected in 'My Map'

</td><td>

Changes in the wm\_task state labels aren't reflected in 'My Map' because state labels were hardcoded in Java.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 1 Hotfix 2a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1704810)
-   [Xanadu Patch 1 Hotfix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1703882)
-   [Xanadu Patch 1 Hotfix 1](xanadu-patch-1-hf-1.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


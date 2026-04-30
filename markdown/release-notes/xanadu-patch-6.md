---
title: Xanadu Patch 6
description: The Xanadu Patch 6 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-02-13"
reading_time_minutes: 36
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 6

The Xanadu Patch 6 release contains important problem fixes.

-   **Xanadu Patch 6 was released on February 13, 2025.**
    -   Build date: 02-11-2025\_1128
    -   Build tag: glide-xanadu-07-02-2024\_\_patch6-01-29-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X06.00.xlsx).

## Overview

Xanadu Patch 6 includes 151 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp6.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 6 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 6, refer to [KB1821996](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1821996).

## Changes in Xanadu Patch 6

-   **[Hyperautomation and low-code](https://www.servicenow.com/docs/access?context=hyperautomation-low-code-landing-page&version=xanadu&pubname=xanadu-hyperautomation-low-code&ft:locale=en-US)**

    The External Content Connectors ServiceNow® Store application enables AI Search applications to search content and metadata from supported external data repositories, such as Atlassian Confluence Cloud and Microsoft SharePoint Online


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

 PRB1825963

 [KB1763961](https://hi.service-now.com/kb_view.do?sysparm_article=KB1763961)

</td><td>

Index KBB throws an exception about journal peekahead

</td><td>

An error is thrown: 'IngestService: Unable to index Glide Record \[9b85baaa3bf 11a10c4589c 8c24e45a2b\] u\_kb\_template\_ topic\_category. fa8191f6fb059 e507863f46b5 eefdc1d : Cannot invoke "java.util.Map.get\(Object\)" because "journalElement ToValuesMap" is null java.lang. NullPointerException: Cannot invoke "java.util.Map. get\(Object\)" because "journalElement ToValuesMap" is null...'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1836358

 [KB1790348](https://hi.service-now.com/kb_view.do?sysparm_article=KB1790348)

</td><td>

A race condition causes an incorrect deleteMultiple\(\) query to be generated on the v\_search\_genius\_result and sys\_variable\_value tables

</td><td>

When the AI Search Genius Result is requested and processed in a multi-threaded, high-concurrency environment, such as when multiple users simultaneously perform search functions on a portal or virtual assistant \(VA\), a thread safety issue arises. This issue may cause an incorrect deleteMultiple\(\) query to be generated, potentially leading to the deletion of excessive records from the sys\_variable\_value table. As a result, various components, including the Integration Hub, Service Catalog items, and workflows, may malfunction due to the absence of these critical records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1814554

 [KB1715780](https://hi.service-now.com/kb_view.do?sysparm_article=KB1715780)

</td><td>

Issue found in Xanadu with **Submit Catalog Item Request**, and multi-row variable sets \(MRVS\) and multi-line text variables

</td><td>

A flow or subflow using **Submit Catalog Item Request** where the catalog item contains a MRVS and multi-line text field fails produces the error: 'com.snc.process \_flow.exception. OpException Caused by: Unexpected character \(\\\) at position 3942.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1402594

 [KB0956006](https://hi.service-now.com/kb_view.do?sysparm_article=KB0956006)

</td><td>

Unable to edit a field in the list view when it is dependent on another field that is read-only for the user

</td><td>

This issue has been observed since New York. Users are not able to edit a field on list view when it is dependent on another field that is read-only or has an ACL making it read-only.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1803497

</td><td>

attachment.upload.success event is triggered incorrectly, and can't be relied on to turn off the **Catalog - Order Now** button

</td><td>

When uploading multiple attachments consecutively, the 'attachment.upload.success' event is triggered immediately after the first batch of attachments finishes uploading instead of waiting for all batches to complete. The attachment modal is also hidden before the upload process is fully completed.

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

Activity Stream

 PRB1775777

</td><td>

g\_form.setValue\(\) doesn't work as expected on Workspace when applied to the **Comments** field

</td><td>

The g\_form.setValue can be used to update a field on an record form. Sometimes it is used to update a field with a value captured via the g\_form.getValue\(\). This behavior works without issue in the native UI. However, when trying to apply this same action to the Workspace view, it doesn't work under certain circumstances.

</td><td>

1.  Create a UI action on HR Workspace.
2.  Navigate to HR Workspace.
3.  Select any sn\_hr\_er\_case record from the HR workspace.
4.  Add text to the **Comments** field.
5.  Select **Add signature**.

 Expected behavior: The **Comment** field should be populated with both the current text and the message 'This is a test'.

 Actual behavior: The **Comment** field doesn't change.

</td></tr><tr><td>

Activity Stream

 PRB1832633

</td><td>

'Assignment group' changes are hidden in an activity stream on HR Agent Workspace, which is intermittently different to native

</td><td>

An activity stream in the workspace for the 'Case' table is intermittently missing the 'Assignment group' field change. Native has the change reflecting in 'Additional comments'.

</td><td>

1.  Open an incident.
2.  Set the 'Assignment groups' and **Assigned to** field.
3.  Save the record.
4.  Check the activity stream for the missing 'Assignment group' in the audit event.
5.  Repeat steps 2 through 4 several times.

 Expected behavior: The activity stream should be the same in both workspace and native.

 Actual behavior: The 'Assigned Group' field change is missing intermittently in the HR agent workspace activity.

</td></tr><tr><td>

Activity Stream

 PRB1834293

</td><td>

Activity stream activity events with empty **event\_created\_by** field values cause the activity stream screen on mobile to crash

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1837845

</td><td>

A 'File Attachment' type field isn't added in the activity log in Workspace

</td><td>

A 'File Attachment' type field isn't added in the activity log in Workspace when attaching from a field. It's a ZZ\_YY prefix problem.

</td><td>

1.  Create a new file attachment type field for some record type.
2.  Ensure that the field is visible in some view.
3.  Attach an image to an existing record via the **New file attachment** field.
4.  View the activity stream for the existing record in any workspace.

 Expected behavior: The image appears in the workspace activity stream.

 Actual behavior: The image doesn't appear in the workspace activity stream.

</td></tr><tr><td>

Activity Stream

 PRB1843720

</td><td>

The activity log captures changes but aren't displaying them as the newest entry in Workspace

</td><td>

For a field with name and label of length more than 40 characters, any changes made to the field aren't reflected in the activity stream as a new entry.

</td><td>

1.  Create a new field name and label of length of more than 40 characters.
2.  Add the newly created field in the Service Operations Workspace \(SOW\) view and configure the activity stream filter to display that field in SOW.
3.  Open SOW.
4.  Try updating the value in the field.
5.  **Save**.

 Expected Behavior: The field change should be added as a entry in activity stream.

 Actual Behavior: The change doesn't reflect in the workspace activity stream but reflects in the UI16 activity stream. Instead, the field change appears to overwrite the first initial field change record. If users follow the steps with a field name and label of less than 40 characters, the change would reflect in both workspace and UI16 activity stream.

</td></tr><tr><td>

Agile Development

 PRB1789584

</td><td>

DEFN1003811 calculates worker subscription roles differently for SMV1 versus SMV2

</td><td>

DEFN1003811 ends up producing different results if SMv1 vs SMv2 are installed. The root cause is that the filter to detect the worker subscriptions doesn't match the naming in production and thus misses the worker subscriptions in SMv2. It appears that the '-' in the subscription names is the problem as it doesn't exist in the product subscription names observed in production. The filters should be updated to consistently match the relevant subscriptions.

</td><td>

 

</td></tr><tr><td>

Agile Development

 PRB1797672

</td><td>

DEFN1003811 should clean user analytics files from app-itsm

</td><td>

DEFN1003811 ends up producing different results if SMv1 vs SMv2 are installed. The root cause is that the filter to detect the worker subscriptions doesn't match the naming in production and thus misses the worker subscriptions in SMv2. It appears that the '-' in the subscription names is the problem as it doesn't exist in the product subscription names observed in production. The filters should be updated to consistently match the relevant subscriptions.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1735195

</td><td>

The range facet and facet with compound table.column set in the facet fields is filtered out when one of the tables is late-binding

</td><td>

A fuction doesn't parse table.column correctly and results in a bucket match to zero. The facet is then filtered out.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1818529

</td><td>

A search results page is continuously loading when clicking the pagination in the search preview \(New\)

</td><td>

The issue exists in both xnowassist and ynowassist.

</td><td>

1.  Open a track/xnowassist or track/ynowassist instance.
2.  Navigate to 'Search preview \(New\)'.
3.  Navigate to /now/ais-preview-utility/preview.
4.  Select any search profile.
5.  Perform a search.
6.  Select a pagination.

 Expected behavior: Search results should load.

 Actual behavior: Search results are loading continuously.

</td></tr><tr><td>

AI Search

 PRB1832851

</td><td>

There's no hover over for a Q&amp;A source citation

</td><td>

 

</td><td>

1.  Get a Q&amp;A result.
2.  Hover over the source citation.

 There's no hover over of the source title.

</td></tr><tr><td>

AI Search

 PRB1835340

</td><td>

sys\_updated\_on for ais\_datasource isn't updated upon changes in Advanced Configuration, Field Configuration and Semantic Index Configurations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1837114

</td><td>

There's exceptions for the Search QnA Glide Signal processing

</td><td>

There's an exception in the logs: '\*\*\* Script: Failed to process signal event of type: 'SEARCH\_EVENT', priority: 'INFO', body: '\[object Object\]', created: '2024-12-17 01:44:04': null:...'

</td><td>

1.  Provision an instance on the latest main instance with all the latest store apps for GenAI.
2.  Make a **search** action.
3.  Check the logs for the exception.

</td></tr><tr><td>

AI Search

 PRB1843571

</td><td>

AI Search's NLQ Genius result 'None of the above' option doesn't work as expected

</td><td>

 

</td><td>

1.  Enable the NLQ Genius result for a search application.
2.  Search for an utterance that contains multiple table names.
3.  Select **None of the above** in one of the menus of the Genius result card.

 Observe that there's no result in the table. The NLQ query didn't properly remove the table which had **None of the above** selected for it. An error shouldn't display.

</td></tr><tr><td>

AI Search

 PRB1847092

</td><td>

A part of the query on sys \_generative \_ai \_config has been ignored because of insufficient access for 'query\_match operation on sys\_generative\_ai\_config definition

</td><td>

Results in warning message pop-ups.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1821588

</td><td>

sys\_report\_chart\_color and sys\_report\_color table cache creation is taking around 15 seconds

</td><td>

The creation of a cache for both tables becomes a lengthy operation when an instance has like 23000 and 1100 entries in the sys\_report\_chart\_color and sys\_report\_color tables, respectively.

</td><td>

1.  Navigate to any instance.
2.  Create a data visualization.
3.  Navigate to cache.do and clear the cache.
4.  Select the refresh context menu.
5.  Observe the network panel.

 Observe that it takes a long time to create.

</td></tr><tr><td>

Analytics Data API

 PRB1832760

</td><td>

Bar chart visualizations aren't loading on a BT1 clone

</td><td>

The following error is displayed in the console: '\{"error":\{"message":"Unable to generate chart","detail":"For input string: \\"gray\\" under radix 16","errorCode":100,"type":null\},"statusCode":400\}'.

</td><td>

1.  Navigate to **All** &gt; **Chart colors**.
2.  Select only 'incidents' colors.
3.  Select one color.
4.  Observe that the color in the 'Display' column is defined as red.
5.  Apply this color to the chart on a dashboard.
6.  On the 'Chart colors' page, change the color to 'gray'.
7.  Remove the existing color definition link.
8.  Refresh the visualization.

 See that the chart is displayed as a blank.

</td></tr><tr><td>

Antivirus Scanning

 PRB1835660

</td><td>

The antivirus job updates all columns instead of only the 'State' column

</td><td>

The antivirus job updates all columns in some scenarios. It should only update the state column when attachment.setState\(advice\) is called. However a forceUpdate occurs, which ultimately updates the entire row, including the state data. Additionally, when the old table name and table sys\_id are updated, the attached file is moved to the previous table.

</td><td>

1.  Log in to a Washington DC instance.
2.  Navigate to **All** &gt; **Self service** &gt; **Service catalog**
3.  Select **Mobiles** &gt; **Add to cart**
4.  Upload a 10MB file.
5.  Select **Order now.**.
6.  Navigate to sys\_attachment.list.

 Expected behavior: The table name should be sc\_req\_item on the available 'State'.

 Actual behavior: The antivirus job updates all columns instead of only the 'State' column.

</td></tr><tr><td>

Application Install Engine

 PRB1792128

</td><td>

There's a race condition when nodes try to download the same app package at the same time

</td><td>

During the cloning process, the list of nodes of clones are upgraded/downgraded. They restart at the same time and tend to download the app package at the same time. There is an existing logic which cleanups all the other attachments for the current app other that the download it made. Since the downloads are happening at the same time, nodes are deleting each other's downloads and nodes are failing to download the apps.

</td><td>

1.  Have multiple nodes \(&gt;=4\) in the clone.
2.  Reset the clone.

</td></tr><tr><td>

Approvals

 PRB1845668

</td><td>

Multi-Level approval skips steps due to race conditions

</td><td>

Overlapping transactions on the sc\_req\_item table cause race conditions allowing approval steps to be skipped.

</td><td>

 

</td></tr><tr><td>

Attachments to Records

 PRB1801182

</td><td>

The **Attach File** field Pencil/Edit icon disappears for an attachment after saving a record

</td><td>

 

</td><td>

1.  Create a table and name it 'cust\_attachment' with these columns:
    1.  Name , Type String
    2.  Approver , Type - Reference, Reference - sys\_user
    3.  Attachment, Type - File Attachments.
2.  Create an ACL, with the following parameter:
    1.  Type: Record
    2.  Operation: Read
    3.  Decision Type: Allow If
    4.  Table: cust\_attachment and leave field aline
    5.  Role: itil
3.  Create another ACL, with the following parameters:
    1.  Type: Record
    2.  Operation: write
    3.  Decision Type: Allow If
    4.  Table: cust\_attachment and leave field aline
    5.  Role: itil
    6.  In the data condition, add a condition with the approver is itil user.
4.  Create some records in the cust\_attachment table with some attachments and the approver as an itil user.
5.  Impersonate as an itil user.
6.  Add the cust\_attachment table to Service Operations Workspace from 'My Lists'.
7.  Add a new list.
8.  Select any record.

 Observe the 'Edit' icon is missing from the attachment.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1805778

</td><td>

'Validate Record Present in List' fails for a related list

</td><td>

Related list records are failing to run when the user preference 'Load related lists in classic forms' is set to 'On Demand'.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1844302

</td><td>

Ad hoc tasks generated from a flow aren't supported in the playbook on HR Agent Workspace

</td><td>

 

</td><td>

1.  Create a test LE event.
2.  Add several activity sets to it.
3.  Create a subflow in Flow Designer.
4.  Create activities in all of the activity sets of as many different activity types.
5.  For flow activities, make sure to define 'Activity Field Mappings'.
6.  Tie the LE event to HR service.
7.  Create a case of that HR service.

 Notice that LE activities can't be closed and closing all activities in an activity set triggers the next activity set \(if it is a dependent activity set\).

</td></tr><tr><td>

Case Management

 PRB1826618

</td><td>

An email with a recipient list of more than 1000 users isn't sent

</td><td>

When using a task communication recipient list with over 1000 users in a major incident, the resulting mail does not resolve the recipient list into its users and no mail is sent. The mail shows the error: 'Recipient items 3e6e6de1c3e 95a10b4081bddd 40131ef sn\_ publications\_recipients\_list failed to resolve with error: Cannot read property "length" from undefined'.

</td><td>

 

</td></tr><tr><td>

Communities

 PRB1793564

</td><td>

The video preview isn't displayed to users on 'Video' content type posts in the community activity feed

</td><td>

The video thumbnail should be displayed in the preview, similar to how it appears when the video URL is inserted during the posting.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1835043

</td><td>

The X true-up version for CMDB Workspace should be updated to add the domain\_master attribute for the cmdb\_dependent\_ci\_ledger table

</td><td>

The sn\_cmdb\_ws plugin and glidefix\_domain\_maste r\_cmdb\_dependent\_ ci\_ledger.xml fix script are taking 45 minutes during an X to Y upgrade.

</td><td>

 

</td></tr><tr><td>

Content Publishing

 PRB1837860

</td><td>

The Event Calendar widget 'Holiday Calendar' isn't generating the correct .ICS file

</td><td>

Users are unable to import all events from that .ICS file into Mac Calendar or MS Outlook.

</td><td>

This issue can be reproduced using either Mac Calendar or MS Outlook. Using Mac Calendar:

 1.  Navigate to /esc?id=esc\_dashboard.
2.  Find the Holiday Calendar.
3.  Select **Add all to Calendar**.
4.  Double click on the downloaded .ICS file.
5.  Open the file by double-clicking it.
6.  When adding a new event, select **New Calendar...**.
7.  Select **OK**.
8.  Verify that a new calendar named 'Holidays\_2025' has been added to the Mac Calendar.
9.  Browse through the months and observe that only one entry is present, while all other entries are missing.

 Expected behavior: The import for all events should work in the calendar.

 Actual behavior: Users can't import all events into the calendar. It only imports the first entry.

</td></tr><tr><td>

Data Archiving

 PRB1826830

</td><td>

Rearchiver runs for few days due to incorrect query logic when the archive rule has an 'OR' condition

</td><td>

Re-archiver can run for over 4 days without completion. In the localhost log, there can be a long query result set, such as 1409626 rows.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1842119

</td><td>

The ViewWhereClause PostgresSanitizer method isn't handling NOT LIKE correctly

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1842672

</td><td>

After renaming columns of a staging table to under 63 bytes for applicable ones, the staging table has syntax errors when accessing the list view

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1845539

</td><td>

Cypher datetime and property data types

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1801384

 [KB1790177](https://hi.service-now.com/kb_view.do?sysparm_article=KB1790177)

</td><td>

Orphan archive-related records \(Archive\_Map NULL\) aren't ignored by the archive job

</td><td>

When an instance has orphaned archive related records, the archive job tries to find orphan related records and archive them as part of the run being processed by the archive job.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1845280

</td><td>

Users see a null point error when turning on archive debugging

</td><td>

The error caused archive reparenting process to fail and the state to be in 'error'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1779767

</td><td>

Using 'Null' as a value in the '!= ALL' operator set fails

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1841215

</td><td>

Restrict primary key-ordering injection for Postgres only

</td><td>

Primary key ordering was dynamically added for certain kinds of queries \(for example, REST/BATCH\_REST, non-referred, non-interactive queries with windowing\). The change could adversely impact query performance for MySQL.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1849730

 [KB1901158](https://hi.service-now.com/kb_view.do?sysparm_article=KB1901158)

</td><td>

Oracle prepared statements leaked for sys\_attachment\_doc queries

</td><td>

When running Glide with an Oracle database, when loading an attachment, a PreparedStatement leaks. This leak eventually cleans up when its database connection is recycled. However, if enough attachments are loaded before the connection is recycled, an OutOfMemoryError can occur, resulting in the application node restarting.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

DevOps \(Family\)

 PRB1839002

</td><td>

A DevOps event isn't honoring load checks on the sys\_flow\_context table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1821160

</td><td>

A scripted deletion strategy is triggered for the keep strategy

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1833443

</td><td>

Files supported for the 'put file' operation should be extensible as a MID server property

</td><td>

Currently, the files supported for the 'put file' operation are hardcoded in Java. This needs to be more extensible moving forward to support more files added by content teams and users.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1835802

</td><td>

Discovery is incorrectly classifying Cisco routers as switches for OID 1.3.6.1.4.1.9.1.469

</td><td>

.

</td><td>

Run Discovery on any Cisco 2621XM router.

 Observe that it classifies as a switch instead of a router.

</td></tr><tr><td>

Discovery

 PRB1837810

</td><td>

vCenter Discovery doesn't go through IRE

</td><td>

As vCenter discover doesn't go through IRE, users can't leverage reconciliation rules. The actual source for a correlation ID is a third party integration. However, Discovery is overriding this field after integration updates the correlation ID. If not planning for IRE rules on vCenter Discovery, there should be configurable functionality to skip some fields.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1842227

</td><td>

True-up ITOM Licensing November release version for Xanadu and Washington DC

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Employee Center

 PRB1806589

 [KB1704673](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704673)

</td><td>

Employee Center autocomplete suggestions don't work in Xanadu

</td><td>

The autocomplete suggestions of a base instance ESC AI Search doesn't work in Xanadu.

</td><td>

1.  Open a base instance ESC Portal in Xanadu.
2.  In the Search box, type 'What is spam?'.

 Expected behavior: There are suggestions in the typeahead widget.

 Actual behavior: There are no suggestion results.

</td></tr><tr><td>

Employee Center

 PRB1820904

 [KB1705991](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705991)

</td><td>

A missing semi-colon in the EC Theme breaks the CSS resolution

</td><td>

A missing semi colon at the end of a new theme variable in EC Theme causes the CSS resolution to break.

</td><td>

1.  Log in to an instance with the latest EC apps.
2.  Create an incident using the 'Create Incident' catalog item on the ESC Portal.
3.  Navigate to 'My Requests'.
4.  Open the newly created incident.

 Observe that the 'Start' text isn't encircled in a green color.

</td></tr><tr><td>

Employee Center

 PRB1827901

</td><td>

On the EC homepage, the 'My items' widget displays 'You don't have any items yet', then loads

</td><td>

The text 'You don't have any items yet' shouldn't come up unless there aren't any active activity configurations on the instance.

</td><td>

 

</td></tr><tr><td>

Employee Relations Case Management

 PRB1827550

</td><td>

Requested RCA from Employee Center Core targeting Human Resources: Employee Relations about Widget: Standard Ticket Header

</td><td>

After installing the ER plugin, case creation isn't happening for those categories where it should be creating a sn\_hr\_er\_case. It is giving the 'Sorry, there was a problem on my side trying to ...' error.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1822392

</td><td>

After an upgrade to Xanadu, if automated grouping is turned off, \(sa\_analytics.aggregation\_enabled=false\) tag-based grouping isn't working

</td><td>

The sa\_analytics.aggregation \_enabled property should be responsible only for automated, CMDB and text grouping. In addition, there should be a feature flag property on the entire query job \(sa\_analytics.query \_job\_enabled\). When set to false, no logic inside the query job executes.

</td><td>

 

</td></tr><tr><td>

External Triggers

 PRB1810755

</td><td>

Updating an event source shouldn't update the domain and domain path

</td><td>

 

</td><td>

1.  Provision an instance with the Domain Separation plugin installed.
2.  From the global domain and any non global scope, navigate to sys\_ih\_external\_event\_source.
3.  Select the **New** button.
4.  Provide valid inputs.
5.  **Submit**.
6.  Navigate to sys\_api\_collection.list.
7.  Check the domain and domain\_path column values. It should be global.
8.  Navigate to sys\_api\_operation\_list.
9.  Check the domain and domain\_path column values. It should be global.
10. Switch the instance domain to the default domain.
11. Open Flow Designer.
12. Navigate to inbound connections.
13. Activate the event source created above.
14. Check the domain and domain path column values in sys\_api\_collection.list and sys\_api\_operation.list.

 Expected behavior: The domain and domain\_path column values should be global.

 Actual behavior: The domain and domain\_path column values display the default domain.

</td></tr><tr><td>

Flow Engine

 PRB1814015

</td><td>

A template isn't applied properly on the corresponding table fields through Flow Designer

</td><td>

In a subflow, the user uses the **Create Task** action to create a task and a template to fill the task field. When the subflow runs, the template populates one field with everything and leaves the other fields blank.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1822604

 [KB1709945](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709945)

</td><td>

**Flow action** field values are truncated when they contain the '=' symbol in one field and use inline scripts in another field

</td><td>

A flow action isn't updating fields properly when having the 'script' type column and inline scripts on the **Create Record** action.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1805189

</td><td>

Info logging in KafkaConsumerRegistry \(create/close\) is estimated to cost $20K/year in Splunk costs

</td><td>

Logging from KafkaConsumerRegistry should be lowered to debug or removed entirely to save Splunk costs.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1832870

</td><td>

'Potential infinite loop' errors in the 'MIF Consumer' job

</td><td>

The 'MIF Consumer' job fails when attempting to poll for new messages on the MIF topic.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1841698

 [KB1809311](https://hi.service-now.com/kb_view.do?sysparm_article=KB1809311)

</td><td>

There's duplicate entries in hermes\_cluster\_config

</td><td>

Duplicate entries in hermes\_cluster\_config table are causing dependent plugins to not work as expected, causing node failure during upgrades.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

 PRB1848928

</td><td>

There's an RCA error on creating LE and ER Cases for summarization

</td><td>

An error is thrown: 'Read operation on table 'sn\_hr\_le\_case' from scope 'Now Assist context menu' was denied. The application 'Now Assist context menu' must declare a cross scope access'.

</td><td>

1.  Log in to an instance.
2.  Create an LE case as an agent with the sn\_hr\_le.case\_writer role.

Observe that an RCA error is thrown.

</td></tr><tr><td>

HR Service Delivery

 PRB1830128

</td><td>

Quotes aren't correct in HTML in HR Workspace and Playbook after upgrading from Vancouver to Xanadu

</td><td>

Special characters are rendered in an encoded format: FIND

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1837460

</td><td>

Using the 'Email recommendations elaborate' functionality generates RCAs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HTML Field Type Editor

 PRB1796117

</td><td>

The copy and paste function isn't working as desired

</td><td>

When copying over formatted content from a Word document, a few formatting aspects like font sizes, link color, and table size aren't copied over properly.

</td><td>

 

</td></tr><tr><td>

Identity

 PRB1833655

</td><td>

A SCIM user who gets an endpoint has performance issues

</td><td>

A SCIM user who gets an endpoint has performance issues when fetching users with a page count of 500.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1795757

</td><td>

The IDR queue dashboard displays an incorrect value for the remaining messages that are to be processed for V2 sets

</td><td>

The queue dashboard displays the end offset of partition 1 as remaining messages, even though from the topic inspector it's evident that there are no new messages arriving there \(current and end offset same\). The logic for remaining messages should account for an active partition and then calculate the remaining messages based on the current and end offset values.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1835500

</td><td>

If the call chain contains a source with a null scope, OutboundUsage EventWatcher throws null pointer exceptions

</td><td>

Even if the call chain is corrupt, this class shouldn't throw a NPE.

</td><td>

Create an outbound HTTP Request with a call chain that has a null scope in one of the sources.

 Observe null pointer exceptions.

</td></tr><tr><td>

Integration Hub

 PRB1843074

</td><td>

The configurability of call chain debug logging for Integration Hub is insufficiently granular

</td><td>

There should be a couple more properties for if users only want to log certain scenarios.

</td><td>

1.  Enable glide.sys.client.call\_chain.debug=true on an instance.
2.  Run a REST step as well as a RMv2.

 See that users get logging statements for each of the following: Flow Engine starting, posting a usage to ua\_ih\_usage, and posting a transaction to outbound\_request\_usage\_metrics. If users only care about one of these scenarios, this is more logging than is needed if users want to leave the logging on for something that might only happen a few times per month.

</td></tr><tr><td>

Interactive Filters

 PRB1837354

</td><td>

Filters no longer support reference list types

</td><td>

It used to be possible \(up until Xanadu\) to select 'Incident."Watch List"' as the data to filter in the filter configuration. This seems to no longer be possible.

</td><td>

1.  Navigate to **Analytics Center** &gt; **Library** &gt; **Dashboards**.
2.  Create an in-line dashboard.
3.  Add a new single or multiselect filter:
    -   Filter Source: sys\_user table
    -   Data to Filter: Incident.Watch list

 Expected behavior: 'Watch List' should be a possible value to choose as a filter target.

 Actual behavior: 'Watch List' can't be chosen.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1847887

</td><td>

Support Bagheera-Phase2 enablement

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1830531

</td><td>

Post-Xanadu upgrade, changing a KB's article length makes the article unsearchable

</td><td>

The issue can be reproducible on any Xanadu instance.

</td><td>

1.  Open any Xanadu instance.
2.  Open a published KB article.
3.  Export the XML.
4.  Edit the number in the XML.
5.  Add an extra digit to the number.
6.  Import the article back.
7.  Search for it.

 A 'Knowledge Record not found' message is displayed.

</td></tr><tr><td>

Microsoft Reconciliation \(Family Release\)

 PRB1842128

</td><td>

Time consuming 'Select' queries on Cloud Installs views while fetching cloud installs for the 'markProviderHost TypeServiceType OnCloudInstalls' method due to complex joins

</td><td>

.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1825232

</td><td>

The reload\_credentials event triggers a flush and the close of all in-use connections in ConnectionCache

</td><td>

Whenever credentials are changed on an instance, the instance sends an event to the MID server, triggering a flush and close of all connections in ConnectionCache, even if some connections are actively in use. This is causing failures in workflows that are relying on cached connections at that time.

</td><td>

1.  Run Data Source \(DaaS - Supplier Data Full Load\).
2.  Verify that it intermittently fails with a 'Closed Connection' error.

</td></tr><tr><td>

Performance Analytics

 PRB1789424

</td><td>

Https \_request\_ decompression doesn't work correctly, as it doesn't strip the 'Content-Encoding' header after it unzips the body

</td><td>

The API returns a 'Not in GZIP format' error.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1836666

</td><td>

The family part of PRB1786205 to the Xanadu release

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics

 PRB1786205

</td><td>

The Migration Center application menu is still visible for zbooted users

</td><td>

 

</td><td>

1.  Provision a net new instance \(track/dataanalytics\).
2.  Notice that the Migration Center menu is visible under 'Platform Analytics Administration'.

 Expected behavior: It should be there only for upgraded instances.

 Actual behavior: It shouldn't be present for net new instances.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1831174

</td><td>

Adding a decision within an variant for base/parent variant activity doesn't work as expected

</td><td>

 

</td><td>

1.  Create a process definition with activity **A** &gt; **B** &gt; **C**.
2.  Add Variant X to the process definition.
3.  With Variant X selected, add Decision 1 after activity B.

Note that activity C is automatically associated with the else branch of Decision 1.

4.  With Variant X selected, add variant activities to other \(non-else\) branches of Decision 1.
5.  Test Playbook on a record that satisfies Variant X and one of the branch conditions of Decision 1.

 Expected behavior: Only activities on the satisfied branch of Decision 1 should appear in the running Playbook.

 Actual behavior: The base activities on the ELSE branch of Decision 1 always appear.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1834463

</td><td>

Process Automation Designer isn't able to pass a previous activity state as a subflow input

</td><td>

In Engine v1, it gives an error: 'Flow Designer: Failed to process event: sys\_flow\_context...'

</td><td>

 

</td></tr><tr><td>

Playbooks

 PRB1829699

</td><td>

Upgrade proof the deletion of the v\_pd\_activity\_start\_rule\_with\_condition table

</td><td>

CMDB's Data Certification feature has a script that queries all tables listed in sys\_db\_object. However, it has an error on a table and the script halts. The table and the ACLs associated with the table aren't deleted. The deleted ACLs should be brought back and have their action property changed to DELETE.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1843673

</td><td>

The 'ML Cluster Detail Purge' scheduled job causes out of memory issues

</td><td>

 

</td><td>

Trigger the 'ML Cluster Detail Purge' scheduled job with million scale data present in the 'ML Cluster Detail' table for a particular clustering solution.

 Observe that the query on the 'ML Cluster Detail' table in the MlClusterDetailPurgeUtil loads a lot of records that match the condition of the Solution ID and Active being true. This leads to an out of memory error in the node.

</td></tr><tr><td>

Process Mining

 PRB1829338

</td><td>

Full mining isn't triggered from platform when localization is enabled

</td><td>

A user with a non-English preferred language isn't able to mine a project.

</td><td>

1.  Enable localization.
2.  Complete a full mining, using platform

 Expected behavior: Mining should be successful.

 Actual behavior: Mining doesn't start the initial steps.

</td></tr><tr><td>

Project Management

 PRB1812212

</td><td>

The **Percentage completed** field doesn't load when exporting projects to MS project

</td><td>

When exporting projects, the '% Complete' column displays '0%' instead of the exported value.

</td><td>

1.  Open one of the projects in Project Workspace or Planning Console.
2.  Navigate to the 'Planning' tab.
3.  Select **More Options** &gt; **Export Planning Console** &gt; **MS Project**.
4.  Select **Ok** to download the XML.
5.  Import the downloaded XML file into MS Project.

 Expected behavior: The '% Complete' column displays the same exported value for each of the tasks in MS Project.

 Actual behavior: The '% Complete' column displays 0% instead of the exported value.

</td></tr><tr><td>

Reporting

 PRB1745543

</td><td>

An interactive report displays extra records in the report drill-down

</td><td>

The issue is seen only when ^NQ \(New criteria\) is used in the filters in the report and only in dashboard with interactive filters. It is working fine in Report Designer.

</td><td>

 

</td></tr><tr><td>

Seismic Framework

 PRB1838437

</td><td>

There's multiple react versions on a page at runtime

</td><td>

 

</td><td>

1.  Navigate to homepage /now/nav/ui.
2.  Open network tools.
3.  Search for ui-core.
4.  Navigate to the response.
5.  Search for React v16.14.0 and v16.2.0.

 Expected behavior: There is no match for v16.2.0.

 Actual behavior: React v16.2.0 appears.

</td></tr><tr><td>

Server-side scripts

 PRB1777353

</td><td>

There's an issue compiling a script using a map iterator or nested try/catch blocks

</td><td>

There's an error: 'Problem processing asynchronous servlet request java.lang.VerifyError: Stack map does not match the one at exception handler 2195...'

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1783385

</td><td>

Add rights for java.lang.NullPointer Exception.getMessage

</td><td>

If the user does not have elevated privileges, they see the message 'Attempted script access to inaccessible member denied'.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1837660

</td><td>

Calling hasOwnProperty on a wrapped string can sometimes fail

</td><td>

Calling hasOwnProperty on a Java string exposed to JavaScript can fail. In general, most strings in JavaScript are actual JS objects and work correctly. The problem only happens when a string is generated by a Java API and passed to some JS code. Note that the problem only affects the method 'hasOwnProperty' only on strings.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1834166

</td><td>

Catalog client scripts aren't working for the multi-turn catalog ordering experience when client scripts are exposed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1834958

</td><td>

The onLoad Mandatory and Visible UI policies aren't working

</td><td>

For the onLoad Mandatory policy, questions can be skipped. For the onLoad Visible UI policy, an incorrect question is prompted indicating that the policy didn't hide the correct variables.

</td><td>

 

</td></tr><tr><td>

Service Portal Core Widgets

 PRB1807235

</td><td>

There's accessibility issues for the keyboard and voice over in the 'Hiring' tab

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1823470

</td><td>

After an applied autofill, the cursor is moved to another field

</td><td>

The cursor focus moves to another field. Also, the **List collector** field is expanded and the focus is moved to a list field. An empty value is displayed in the list field.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1829670

</td><td>

Genius results shows both catalog items and knowledge articles even when the user is filtering with the navigation tabs

</td><td>

Searching in a portal displays Now Assist Genius results, including catalog items and knowledge search results. Selecting a catalog navigation pane or a knowledge navigation pane, the filtered results display both a catalog item and Now Assist QnA instead of displaying respective filtered results.

</td><td>

1.  Set up Now Assist in AI Search in the instance.
2.  Activate it for the portal /esc.
3.  Enable AI Search in portal.
4.  Map the Genius result configuration in the Genius result related list tab.
5.  Select the existing link.

A new form appears after entering a catalog item in a Genius result configuration.

6.  Navigate to /esc.
7.  Search in the search widget for **Password reset**.

It displays some Genius results, including a knowledge article summary and catalog item.

8.  Select on navigation's **Requests**.
9.  It displays the same Genius results, including the knowledge summary as well.

 Expected behavior: When selecting the **Requests** navigation pane, it should only display a catalog item Genius result and not knowledge. If users select the knowledge navigation pane, it should display only knowledge and not a catalog Genius result.

 Actual behavior: Irrespective of the navigation pane, the Genius result displays both a catalog item and a knowledge summary.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1821306

</td><td>

The **Discuss** button is missing on a domain-separated instance

</td><td>

The 'Admin' panel displaying the sidebar is activated. The user needs to deactivate and activate it again to see the **Discuss** button.

</td><td>

1.  Log in to Configurable Workspace.
2.  Impersonate as a parent user.
3.  In the list, navigate to 'Case'.
4.  Select **New**.
5.  Enter a domain as a parent.
6.  **Save**.

 Expected behavior: The **Discuss** button should display.

 Actual behavior: The **Discuss** button isn't displaying.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1833793

</td><td>

The sys\_cs\_collab\_settings record for new domains aren't created in the SFS scope

</td><td>

 

</td><td>

1.  Provision an instance with a domain separation plugin installed.
2.  Switch to the ACME domain.
3.  Stay in the global scope.
4.  Navigate to the sidebar settings page in the CI Admin Console.
5.  Observe that the emoji and records type toggles are enabled but the user can't save the record because they're not in the SFS scope.
6.  Switch to the SFS scope.
7.  Observe that the toggles are turned off but the user can save the record.

</td></tr><tr><td>

Software Asset Management

 PRB1840899

 [KB1801232](https://hi.service-now.com/kb_view.do?sysparm_article=KB1801232)

</td><td>

New License Metrics for CrowdStrike

</td><td>

This is a product update.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1842738

</td><td>

Auto-select a metric group based on the CrowdStrike software model

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Workspace

 PRB1774425

</td><td>

There's issues with currency conversion in Platform Analytics \(PA\) and the Publisher 'Results' page

</td><td>

PA widgets don't honor the user session's currency if a particular user has a different currency code than system locale default. Also, Publisher cards display values in the reference currency and not the user session currency.

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB1845639

</td><td>

Kafka Consumer stops consuming messages once it receives a 'null' message from Producer

</td><td>

When a 'null' message error is observed from the source, the Kafka stream no longer consumes the messages.

</td><td>

 

</td></tr><tr><td>

Table Cleaner

 PRB1836111

</td><td>

The dot walk in the **Match** field isn't working

</td><td>

There's no unintended data deletion. Table Cleaner thinks the **Match** field with dot walk isn't valid, and therefore doesn't clean anything for that invocation.

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1794454

</td><td>

Dynamic scheduling for crew isn't working as expected when the territory model is ON

</td><td>

 

</td><td>

1.  Log in as an admin.
2.  Navigate to SF territory.
3.  Add 'installation crew' to the territory as an adhoc crew.
4.  Create a work order task \(WOT\) for SF territory with the 'needs crew' property checked.
5.  Select **auto assign**.

 Expected behavior: The WOT should be assigned to the available crew.

 Actual behavior: The WOT isn't assigned.

</td></tr><tr><td>

Territory Planning

 PRB1808414

</td><td>

When are territory model is enabled and the 'Capacity reservations' plugin is just installed, the planned crew isn't assigned using dynamic scheduling

</td><td>

This issue is reproducible only when a territory model is on, the Capacity Plugin is installed, and definitions/assignments don't need to be created.

</td><td>

1.  Provision an instance with the FSM Territory plugin, Capacity Reservations, and Crew Operation plugins installed.
2.  Activate the FSM territory model.
3.  Have planned crews in place for a territory.
4.  Create a task for the same territory.
5.  Assign through DS auto assign.

 Expected behavior: A crew task should be assigned with the available panned crew.

 Actual behavior: Dynamic scheduling always looking for agents to create a new crew rather than assigning a planned crew.

</td></tr><tr><td>

UI Field Administration

 PRB1795149

</td><td>

Filtering on a dot-walked field incorrectly queries and results in no records being fetched

</td><td>

When filtering a custom table that includes a dot-walked **incident.state** field, the system incorrectly queries the **task.state** field instead. This causes the filter to return no records, despite valid entries in the 'incident.state' column. The expected behavior is for the filter to correctly query the **incident.state** field and return matching records.

</td><td>

1.  Log in to any instance where the issue needs to be replicated.
2.  Navigate to the appropriate module for creating tables.
3.  Create a table.
4.  Add a new field in the table that references the **number** field from the 'incident' table.
5.  Open the newly created table from the list view.
6.  Right-click the header and select **Configure** &gt; **List Layout**.
7.  In the list layout configuration, add the **number** field created earlier.
8.  Additionally, add a dot-walked column for 'incident.state'.
9.  Save the changes and verify that the fields are correctly displayed in the list layout.
10. Apply a filter on the new table using '\*New' or any state value displayed from the added records.
11. Observe the results after applying the filter.

 Expected behavior: The filter should fetch records where the 'incident.state' column matches the entered value.

 Actual behavior: No records are fetched.

</td></tr><tr><td>

UI Field Administration

 PRB1833651

</td><td>

The 'Sparkle' icon is displayed in the **Resolution notes** field without any user focus

</td><td>

 

</td><td>

1.  Enable the **Resolution notes** skill.
2.  Open an incident record in UI16.
3.  Navigate to the **Resolution notes** field.

 Observe that the 'Sparkle' icon is displayed to the user without any focus.

</td></tr><tr><td>

UI Form Administration

 PRB1787509

</td><td>

The glide.attachment. encrypt\_by\_default property value isn't honored by Agent Workspace

</td><td>

When glide.attachment. encrypt\_by\_default is set to true, the encryption isn't happening in HR Agent Workspace.

</td><td>

1.  Set up encryption.
2.  Log in to a Washington instance.
3.  Set the system property glide.attachment. encrypt\_by\_default to true.
4.  Set com.glide.encryption. enable\_attachment\_key\_ui to false.
5.  Open a record in Agent Workspace.
6.  Add an attachment.

 Expected behavior: The attachment should get encrypted by default when glide.attachment. encrypt\_by\_default is set to true.

 Actual behavior: When com.glide.encryption. enable\_attachment\_key\_ui is set to false, the encryption doesn't happen.

</td></tr><tr><td>

UI Form Administration

 PRB1836016

</td><td>

Fields in the Metric Data Task of the ESG Workspace are displayed in a single column

</td><td>

This issue occurs when the screen is opened at 100% zoom. If the screen is displayed at approximately 75% zoom, the fields are displayed in two columns according to the defined view. The affected view is as follows: Metric Data Task \[sn\_grc\_metric\_data\_task\] - View: Data task info. This issue doesn't occur in Vancouver, but it occurs after upgrading to Xanadu.

</td><td>

1.  Navigate to a Next Experience instance.
2.  Open the 'sys prop' table and set the value of the property glide.ui.form. breakpoints.enable as false.
3.  Open any configurable workspace.
4.  Open any form record.
5.  Select the 'Details' tab.
6.  Select the resizable panes divider handle and drag this on to left side

 Expected behavior: The form layout should display as a two column layout.

 Actual behavior: The form layout displaying as a single column layout.

</td></tr><tr><td>

UX Framework

 PRB1814114

</td><td>

An instance is significantly slower when zoomed in to 400% at a lower resolution

</td><td>

After zooming in, the instance gets slow and users can't open any list menus or open any records. After clicking around a few times, the page becomes unresponsive.

</td><td>

1.  Navigate to Service Operations Workspace/Customer Service Management Workspace and open an incident/case record, or use the list page.
2.  Set the display resolution to 1280x1024.
3.  Zoom in to 400%.

</td></tr><tr><td>

Virtual Agent

 PRB1844284

</td><td>

A multi-case KB GenAI call errors out for the agent persona

</td><td>

 

</td><td>

1.  Log in as a user.
2.  Create a KB.
3.  Draft an article with Now Assist.
4.  Enter a search term to search for HR cases.
5.  Select 2 or more cases and continue.

 Observe an error in the Generative AI log for the 'Multi-knowledge article generate' call.

</td></tr><tr><td>

Virtual Agent

 PRB1845506

</td><td>

The 'Status' column in the 'OneExtend Batch Run' table is missing the choice 'Archived'

</td><td>

 

</td><td>

1.  Navigate to the 'OneExtend Batch Run' table entry in the 'Tables' table.
2.  Look for the columns section.
3.  Select the 'Status' column.
4.  Under the choices section, check if there's an archived choice.

</td></tr><tr><td>

Visualization Designer

 PRB1784347

</td><td>

The 'Visualization Library' printer-friendly page is broken

</td><td>

When exporting and downloading a PDF, it contains different pages than expected.

</td><td>

 

</td></tr><tr><td>

Word Document APIs

 PRB1840050

</td><td>

The Docx4j version should be updated to support ServiceNow WordDocumentAPIs after a recent update of Microsoft Office Word 16.91

</td><td>

There's a new XML tag that is added in to docx format by Microsoft. The respective docx4j library has updated \(8.3.13\), which has to be updated in the WordDocumentAPIs services.

</td><td>

1.  Create a Word template document with MS Office Word with the 16.91.x version.
2.  Add it to the 'Contract' template.
3.  Parse it.
4.  Initiate a contract with this template document.

 Observe that the document is generated, but if it's downloaded and opened, it displays the document as corrupted.

</td></tr><tr><td>

Work Order Management

 PRB1839337

</td><td>

The time displayed in the 'Task' panel and CSP is in the UTC format

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Navigate to DWS.
3.  Select any work order task \(WOT\) from the 'Task' panel and verify the scheduled start date and time.
4.  Open the same WOT in a record page and verify the scheduled start date and time.
5.  Select a WOT from the 'Calendar' panel and hover over it to verify the scheduled start date and time displayed.
6.  Select the WOT and verify the scheduled start and time displayed in the CSP.

 Observe that the time displayed in 'Task' panel as well as the CSP is converted to UTC time instead of the user's timezone.

</td></tr><tr><td>

Zero Trust Access

 PRB1838694

</td><td>

Mobile users with SSO logins are logged out with Zero Trust Access \(ZTA\) mobile enabled

</td><td>

 

</td><td>

1.  Provision an instance with Zero Trust Access installed.
2.  Configure ZTA policy to relegate roles in a session and enable ZTA in a mobile entity record.
3.  Configure SAML IDP.
4.  On the Now Mobile app, perform a SAML based login from mobile app.

 Expected behavior: The user should not be logged out until the refresh token expires.

 Actual behavior: The user is logged out after ~30 minutes with a null pointer exception in the logs.

</td></tr></tbody>
</table>## Fixes included

-   [Xanadu Patch 5 Hotfix 1](xanadu-patch-5-hf-1-PO.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1774457)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


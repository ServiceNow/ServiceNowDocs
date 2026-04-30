---
title: Yokohama Patch 7
description: The Yokohama Patch 7 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-08-28"
reading_time_minutes: 67
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 7

The Yokohama Patch 7 release contains important problem fixes.

-   **Yokohama Patch 7 was released on August 28, 2025.**
    -   Build date: 08-22-2025\_1958
    -   Build tag: glide-yokohama-12-18-2024\_\_patch7-08-14-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y07.00.xlsx).

## Overview

Yokohama Patch 7 includes 220 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp7.png "Top 10 problem categories") ![Fixed issues grouped by problem categories bar chart]( "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 7 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 7, refer to [KB2399486](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2399486).

## Changes in Yokohama Patch 7

-   **[Create an endpoint for clients to access the instance](https://www.servicenow.com/docs/access?context=t_CreateEndpointforExternalClients&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**
    -   Token Format: Format of the token to generate. The format determines the structure of a token and the information it includes.
    -   Subject Claim: Field in the User \(sys\_user\) table that's used to populate the value of the subject \(sub\) claim of a JWT token. The sub claim is a piece of information that identifies the subject, or user, of the JWT token. This field only applies if the **Token Format** is JWT.
-   **[Create an OAuth JWT API endpoint for external clients \(machine to machine integration\)](https://www.servicenow.com/docs/access?context=create-jwt-endpoint&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US)**
    -   Token Format: Format of the token to generate. The format determines the structure of a token and the information it includes.
    -   Subject Claim: Field in the User \(sys\_user\) table that's used to populate the value of the subject \(sub\) claim of a JWT token. The sub claim is a piece of information that identifies the subject, or user, of the JWT token. This field only applies if the **Token Format** is JWT.
-   **[Create an HTTP classification](https://www.servicenow.com/docs/access?context=create-an-http-classifier&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

    Starting in YP7, the HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. To override this behavior, you can enable **mid.http\_classy.allow\_credentials\_over\_http**. However, enabling this setting can expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to **false** and use HTTPS whenever possible.

-   **[MID Server properties](https://www.servicenow.com/docs/access?context=r_MIDServerProperties&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**
    -   **mid.http\_classy.allow\_credentials\_over\_http**

        Enables the HTTP Classify probe to send credentials over the HTTP protocol during discovery.

        -   Type: true \| false
        -   Default value: false
        **Warning:** Enabling this setting can expose credentials to security risks, such as man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to **false** and use HTTPS whenever possible.

    -   **[Run discovery through an HTTP or HTTPS REST call](https://www.servicenow.com/docs/access?context=run-http-discovery&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US)**

        Starting in YP7, the HTTP Classify probe no longer attempts credentials over the HTTP protocol by default. To override this behavior, you can enable **mid.http\_classy.allow\_credentials\_over\_http**. However, enabling this setting can expose credentials to man-in-the-middle \(MitM\) attacks. Therefore, it’s strongly recommended to keep this property set to **false** and use HTTPS whenever possible.

    -   **[Virtual Agent release notes](../conversational-interfaces/virtual-agent-rn.md)**



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

 PRB1924202

 [KB2397128](https://hi.service-now.com/kb_view.do?sysparm_article=KB2397128)

</td><td>

The 'My Company Application' \($mycompany appsmgmt.do\) page isn't found

</td><td>

The 'My Company Application' page isn't found after upgrading Yokohama.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1905312

 [KB2415334](https://hi.service-now.com/kb_view.do?sysparm_article=KB2415334)

</td><td>

A 'Feedback definition' table doesn't display any feedback records

</td><td>

Feedback definitions aren't visible. Also, users can't create a feedback definition.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Indexes

 PRB1901971

 [KB2206973](https://hi.service-now.com/kb_view.do?sysparm_article=KB2206973)

</td><td>

A missing index on the 'sys\_id' column of the 'cmdb\_qb\_ result\_base' table causes a replication lag when the table size is large

</td><td>

The index on the 'sys\_id' column of the 'cmdb\_qb\_ result\_base' table is missing on 14000+ instances. Due to this missing index, when 'Table Cleanup on Query Status' \(qb\_query\_status\) table is triggered on such instances, it can lead to replication lag issues, especially when large volumes of records need to be deleted from the qb\_query\_status table. This can lead to memory exhaustion, and records are not properly cleaned up.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1840860

</td><td>

The scheduled job 'SAM - Apply latest content changes' fails

</td><td>

The scheduled job 'SAM - Apply latest content changes' fails with the exception 'SAM - Apply latest content changes job aborted as CDS pull has not happened for all tables'.

</td><td>

 

</td></tr><tr><td>

Software Asset Normalization

 PRB1847748

 [KB2020463](https://hi.service-now.com/kb_view.do?sysparm_article=KB2020463)

</td><td>

Sometimes Norm product/publisher isn't cleared/stamped on a few installs

</td><td>

 

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

Access Control List \(ACL\) Rules

 PRB1910480

</td><td>

Reduces ACLs generated by QueryACLAuditor for table and fields in hierarchies

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910482

</td><td>

Ensures the QueryRangeACLAuditor doesn't generate Security Attribute with blank script

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910491

</td><td>

Enables QueryACLAuditor to run for a specific list of tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910494

</td><td>

Fixes QueryACLAuditor ACL generation for specific read ACL combinations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910496

</td><td>

Fixes QueryACLAuditor ACL generation for some situations involving hierarchies of tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910499

</td><td>

Augments the description of ACLs, generated by QueryACLAuditor, to classify the field ACLs retained for their datatypes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910928

</td><td>

Adds Business Rule to keep query\_range ACLs synchronized with read ACLs in case of role modification

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1918225

</td><td>

Ensures conditional\_table\_query\_range ACL customizations are honored with QueryRangeACLAuditor reruns

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1918943

</td><td>

Ensures QueryRangeACLAuditor rerun to preserve the timestamps of query ACLs created by previous audit run

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1911812

</td><td>

Ensures retain fields get the right ACLs when in table hierarchies

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1917141

</td><td>

Ensures QueryRangeACLAuditor is re-run to preserve all the query ACLs created by the previous audit run, in case of query\_range ACL customizations

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

 PRB1923345

</td><td>

Activity Response Generation \(ARG\) updates for workspace are not included in Yokohama

</td><td>

ARG changes are missing in workspace.

</td><td>

1.  Set up Activity Response Generation.
2.  Enable the configuration.

</td></tr><tr><td>

Agent Assist

 PRB1910542

</td><td>

The window pane doesn't resize when composing an email in a configurable workspace

</td><td>

When the user composes an email in a configurable workspace, the window pane doesn't resize for the email body. The 'Email Templates' frame is expanded and not scrollable, and the **Send email** button isn't visible.

</td><td>

1.  In Yokohama, navigate to an instance.
2.  Open any workspace \(SOW/CSM/FSM\).
3.  Open any incident in the workspace.
4.  Compose an email.

Notice a new tab opens.

5.  Verify that the 'Email Templates' frame is opened.

 Expected behavior: The 'Email Templates' frame is collapsed and scrollable. The Email Client body is the same size as the window, and the **Send email** button is visible.

 Actual behavior: The 'Email Templates' frame is expanded and not scrollable. The Email Client body is the same height as the 'Email Templates' frame, and the **Send email** button only appears after scrolling down.

</td></tr><tr><td>

Agent Chat

 PRB1908263

</td><td>

Safari audio issues in inactive tabs

</td><td>

Audio doesn't work properly when the user switches to an inactive tab.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1926239

</td><td>

Clean up the AiSearchConversational CatalogHelpers script

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1848428

</td><td>

A blank screen is opened in a new tab when Now Assist generates an answer source from AI Search

</td><td>

'about:blank\#blocked' occurs with a blank screen when a Now Assist generated answer source \(from AI Search\) attempts to open in a new tab.

</td><td>

1.  Select any Washington/Xanadu instance having Now Assist in AI Search.
2.  Navigate to any Washington/Xanadu instance.
3.  Navigate to portal\(/sp\) having AI Search - Now Assist in AI Search configured.
4.  Navigate to /sp portal and search 'how to'.

Observe the Now Assist generated answer in the Genius result space. In the sources, see a link.

5.  Right-click on the source link and open in a new tab.

 See that 'about:blank\#blocked' with a blank screen appears.

</td></tr><tr><td>

AI Search

 PRB1888752

</td><td>

The KB sources number is cut off for Now Assist QnA Genius Results

</td><td>

This is observed on global and portal both.

</td><td>

1.  Open an instance with the latest znowassist version.
2.  Attach a Now Assist QnA to the search profile.
3.  Search for 'what is cookie?'.

 Notice that the KB number is cut off in sources and when a user hovers over the sources, it doesn't display the pop-up with the KB number and name.

</td></tr><tr><td>

AI Search

 PRB1889180

</td><td>

Action-type columns aren't registered on the sys\_search\_genius \_result\_event\_action table for NLQ Genius results

</td><td>

 

</td><td>

1.  Provision an instance with NLQ configured on the global search profile.
2.  Search for query-like incidents.
3.  Wait for NLQ Genius Results to load.
4.  Select **positive feedback** buttons.
5.  Navigate to the sys\_search\_genius\_ result\_event\_action table.

 The action type column should be 'Feedback' for thumbs up and down interactions and it's not being registered on the sys\_search\_genius\_ result\_event\_action table.

</td></tr><tr><td>

AI Search

 PRB1893450

</td><td>

When there's a search application without a name, the drop-down list appears empty

</td><td>

When the user creates a search application without a name, the drop-down list for selecting search applications appears empty and displays the message 'null'.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1921143

</td><td>

Define agent-specific 'additionalContext' keys

</td><td>

This is a product update.

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

The root cause of the issue is the componentPropertyChangedEffect isn't triggered post the componentBootstrappedEffect when, for the first time, the facet component is added in the DOM tree.

</td><td>

1.  Navigate to an instance.
2.  Navigate to the CSM/FSM configurable workspace.
3.  Open a case record from the list.
4.  Navigate to the contextual side-panel on the right hand side and select the magnifying-glass-icon at the top of the list.
5.  Search something in the search bar, then let the results generate.
6.  Post that click on the full view search icon and land on the full view search page.

 Actual behavior: The facet component is in a loading state.

 Expected behavior: The facet component should load.

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

Analytics Data API

 PRB1803606

</td><td>

The y-axis is skewed, causing data to look compressed for the time series column in Data Visualization

</td><td>

There are 2 related issues. One, both absolute and relative date range selections are visible at the same time. This is likely a UI policy issue. They shouldn't be visible at the same time. Two, when a user changes the range \(periods\), the scale on the Y axis doesn't get adjusted so it keeps displaying the chart as if the previously visible months are visible on the chart.

</td><td>

1.  Create a visualization with a daily indicator as a data source.
2.  In the metric, select **By Month SUM+** as the time aggregation.
3.  Update the 'Number of periods'.

 Observe that the chart y-axis range is being set by considering additional segment value that isn't displayed in the chart. On the visualization, when users input the **Number of periods** value as '1', the y-axis range is 30 but the max value in the data is '5'. The Y-axis range should have been less either 5 or 10 as per the data point. When users change the **Number of periods** value to '3', the y-axis range is 100, but the max data point value is 30, so the graph doesn't look right. The y-axis range should respect the data point value based on the selected period max data point value in the chart.

</td></tr><tr><td>

Analytics Data API

 PRB1845187

 [KB2238953](https://hi.service-now.com/kb_view.do?sysparm_article=KB2238953)

</td><td>

Drilling down on KPIs in a Performance Analytics dashboard produces an error 'no internet connection'

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Analytics Data API

 PRB1853319

</td><td>

A date range selection isn't applied correctly

</td><td>

The client sends new value in overrides.chartExtraConfig to the multivis API, but the backend returns the same data.

</td><td>

1.  Add a TS chart.
2.  Add an indicator.
3.  Navigate to a date range setting.
4.  Turn on 'show picker by default'.
5.  Select **7 days**.

 Observe that more than 7 days are displayed.

</td></tr><tr><td>

Analytics Data API

 PRB1879995

</td><td>

A chart displays an 'invalid configuration. Date format not valid' error when the date range is changed back to 'Default'

</td><td>

 

</td><td>

1.  Navigate to **All** &gt; **Library** &gt; **Dashboards**.
2.  Create a new dashboard.
3.  Add a new data visualization component on the dashboard.
4.  Specify the following settings to the data visualization:
    1.  Visualization type: Column.
    2.  Data source: 'Number of open incidents' indicator.
    3.  Date range &gt; 'Show maximum range' = true.
    4.  Date range &gt; 'Allow change date range' = true
    5.  Date range &gt; 'Show range picker by default' = true.
5.  Save the changes and exit from editing mode.
6.  Check that the column chart is rendered with 'Date Range' = Default.
7.  Change 'Date Range' = 7 days.
8.  Check that the chart is rendered.
9.  Change 'Date Range' back to 'Default'.
10. Check the chart.

 Expected result: The chart is rendered without errors.

 Actual result: The chart isn't rendered and an 'Invalid configuration. Date format not valid.' error displays.

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

 PRB1842663

</td><td>

Persisted responders rw\_cache aren't synchronized in a cluster

</td><td>

A persisted responder for a table is cleaned up only on 2 nodes. Remaining nodes still have it in memory. Any new registration for the table on remaining nodes won't be flushed to the cluster, as they already have it in memory.

</td><td>

1.  Use the rw\_amb\_demo.do page or use the logging responder.
2.  Have a 2 node cluster with all nodes restarted at same time.
3.  Change the property glide.record\_watcher. cleaner.orphaned\_ persisted\_responders .cleanup\_interval to 1 hour \(3600000 milliseconds\) for quick reproduction.
4.  Register a persisted responder for a custom table.
5.  Once the instance has been online for 30 minutes, then restart one node.
6.  Delete the persisted responder record from sys\_rw\_action or unregister the persisted responder to delete the record in sys\_rw\_action.

 In the next 30 minutes, observe that the cleanup runs on the other node that wasn't restarted and cleans-up the custom table persisted responder from the cache. The restarted node still has the custom table persisted responder in memory.

</td></tr><tr><td>

Authentication

 PRB1901316

</td><td>

The backend doesn't automatically generate the Requester ID in the OAuth JWT Grant Flow

</td><td>

Without a system property enabled, the backend doesn't automatically generate the Requester ID for JWT grant parameters. The client is required to explicitly provide the Requester ID in order to generate a unique access token.

</td><td>

 

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

Attempting to run a non-UI test in Cloud Runner results in the individual tests being 'Pending' forever

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

File handlers are left open if a LazyInputStream is closed before being read by LargeContentDiskCache

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

Restricted caller access \(RCAs\) for Case Look-up Assistant

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1919807

</td><td>

Missing restricted caller access \(RCAs\) permissions for the 'Create approval' subflow

</td><td>

This issue occurs in HR Service Delivery AI Agent Collection.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1928914

</td><td>

There's a restricted caller access \(RCAs\) issue for email reply recommendation

</td><td>

The sparkle icon is missing because this RCA isn't in an allowed state.

</td><td>

 

</td></tr><tr><td>

CMDB Data Manager

 PRB1864548

</td><td>

The 'Delete' policy only deletes half the records in 'delete policy task'

</td><td>

A delete policy was created to delete 50k cmdb\_ci records. After running the 'CMDB Data Manager Archive/Delete Policy Processor' job, five tasks were created, each targeting to delete 10k records \(50k records\). But, only 5k records were deleted per the task, leaving behind 5k records. 'Summary details from Task: Summary - Total CI Count:10000 Deleted CI Count:5000 Archived CI Count:0 Non-Retired CI Count:0'.

</td><td>

 

</td></tr><tr><td>

Column Level Encryption Enterprise

 PRB1848517

</td><td>

The migration process fails because of duplicate sys\_attachment\_doc records

</td><td>

The sys\_attachment records with duplicates aren't migrated successfully. The summaries include the sys\_ids for the attachments.

</td><td>

1.  Install com.glide.encryption.
2.  Reset the 'glide\_encryption.cle\_ replatforming\_with\_kmf' property to 'opt\_out.'
3.  Cache.do, log out, then log in.
4.  Verify that the 'Encryption Contexts' \(EC\) menu option is available.
5.  Cancel any 'Health Scan', 'Key Migration', or 'Data Migration' jobs. \(Delete the jobs if you aren't able to cancel them using a BG script.\)
6.  Create a new encryption context, create a new role, then assign the context to the role.
7.  Assign this role to a user.

You may have to disable a deny unless ACL which prevents creation of new ECs.

8.  Add an attachment to an incident record, then select the 'Encrypt' checkbox while uploading.
9.  Create an orphan record by deleting all the sys\_attachment\_doc records for the sys\_attachment uploaded in step seven.
10. Add another large attachment \(around 4 to 5 MB\) to the same incident record as above and encrypt the attachment.
11. Create duplicate sys\_attachment\_doc records.
12. Set the property glide\_encryption .cle\_replatforming \_with\_kmf to 'opt\_in.'
13. Cache.do, log out, then log in.
14. Create a Field Encryption module for the attachments in the incident table.
15. Create the MAP for the table.
16. Run the 'Migrate Key Context to Module' job.
17. Run the 'Migrate Attachment Context to Module' job.

 Observe that the sys\_attachment record that has duplicates is not migrated successfully and the summary includes the sys\_ids for the attachments.

</td></tr><tr><td>

Column Level Encryption

 PRB1858307

</td><td>

The 'Attachment migration' job doesn't update the job summary

</td><td>

The job summary is missing processing details \(for processed and unprocessed attachment\). The job summary should report job running details \(attachments that are processed and unprocessed\) as other migration jobs.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1895194

</td><td>

Multi-source doesn't set the domain path

</td><td>

If domain separation is turned on, multisource code sets the **sys\_domain** field explicitly using the logged in user's domain. However, the sys\_domain\_path is not set correctly \(default value "/" is set\). This happens because it calls setSystemFields\(\) on the corresponding DBAction before the sys\_domain is set.

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

Core Platform

 PRB1843825

</td><td>

CSRF token rotation isn't happening during login flows

</td><td>

This seems to be due to exceptions being thrown after asyncTransactions are instantiated but before they are ran. There's a small window where this can occur and the user has hundreds of connection resets and other network-related in their logs, which could be hitting this window.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1912116

</td><td>

The 'CypherToResults' API is missing a table/sysid injection in the results

</td><td>

 

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

Use a primary key rather than the sys\_id for the **Target key** field when creating edges for subgraphs

</td><td>

The current code assumes its sys\_id, but with Workflow Data Fabric \(WDF\), that's no longer always the case.

</td><td>

1.  Create a WDF table with a primary key column that's name is something other than the sys\_id.
2.  Create a reference to that table from another table.
3.  Create a name subgraph with the tables in them.
4.  Try to traverse the edge for that reference.

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

Database Persistence - Data Management

 PRB1891527

</td><td>

Workflows aren't properly evaluating conditions to determine if tasks should fire

</td><td>

Filter conditions work differently between Xanadu and Yokohama instances.

</td><td>

 

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

Database Persistence - Data Management

 PRB1908446

 [KB2256996](https://hi.service-now.com/kb_view.do?sysparm_article=KB2256996)

</td><td>

Turn off the 'Collect Reliability Metrics for Data Management' job

</td><td>

'Collect Reliability Metrics for Data Management' leads to long running queries when the TableStatsService API / Reliability metrics API is called on large tables with conditions. It causes performance issues.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1860663

</td><td>

An index is created without a size limit for some unbounded fields, which leads to errors while creating an index or adding data

</td><td>

The 'AWS Service Catalog Connector' \(x\_126749\_aws\_sc\) installation is left with an invalid index in the 'Task' table in RaptorDB. There's an error: 'SEVERE \*\*\* ERROR \*\*\* Exception executing deferred indexes for class: task...'

</td><td>

 

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

Data Privacy \(Classic\)

 PRB1768140

</td><td>

Anonymization of RTA for journal fields fails with a timeout exception for the first occurrence

</td><td>

There's also a instances of this issue on non-journal fields. Any subsequent insert/update works fine.

</td><td>

1.  Provision an instance with Privacy and Discovery apps.
2.  Add an incident to the target table.
3.  Add all patterns to active the 'Data pattern' table.
4.  Create an RTA policy with 'work\_notes' and 'comments' to anonymize.
5.  Add the string 'abc@example.com' to the work notes or comments of any incident.

 Expected behavior: The work notes should be anonymized.

 Actual behavior: Anonymization fails with a timeout exception.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1919038

</td><td>

dp\_cache\_refresh\_thread\_name Thread Deadlock scenarios

</td><td>

Note Preferences.get\(\) and DBConnectionPool are common themes in these stacktraces.

</td><td>

 

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

Developer Sandboxes

 PRB1921161

</td><td>

3 tabs open after clicking on a sandbox in the sandbox list

</td><td>

It looks like there were left over UI Builder generated events in the sandbox management home page macroponent that weren't cleaned. Those extra events should be deleted.

</td><td>

1.  Enable sandboxes.
2.  Navigate to the sandbox management home page.
3.  Create a sandbox if one does not already exist.
4.  Wait for the sandbox creation to finish.
5.  Select the sandbox name.

 Notice that 3 tabs open in your browser.

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

When running a Discovery schedule, the execution of the pattern 'Linux Server' sometimes fails on step '1.1 Get system info' where it runs 'uname -a'. The error generated is: 'Exception occurred. . Cannot invoke "com.snc.sw. commands. RunCommand.exec \(com.snc.sw. context. ExecutionContext, boolean, String, com.snc.sw.kb. lang.commands. ExecutionMode, String\)" because "runCommand" is null.' This results in the OS Version attribute on the Linux servers not being populated. The issue is only triggered intermittently and only on a Discovery schedule.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1848551

</td><td>

Restricting the user from adding more than 150 fields for Gen-AI tasks

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1896682

</td><td>

Create a system property for max page and max field limits for GenAI use cases

</td><td>

Currently, the max page and max field limits are not customizable.

</td><td>

 

</td></tr><tr><td>

Document Management

 PRB1884923

</td><td>

Users can't preview or publish to a case, and a null pointer exception \(NPE\) is thrown: 'Cannot invoke "java.io. ByteArray OutputStream .toByteArray\(\)" because "pdfOS" is null: HtmlToPdfConversionController'

</td><td>

In this process, if the HTML has images fetched from the db\_image table then shared service, it's unable to process it. In a few scenarios, it's throwing a NPE.

</td><td>

 

</td></tr><tr><td>

Document Management

 PRB1890501

</td><td>

With a scheduled email of a report, the 'Include detail' option breaks the PDF creation after a upgrade to Yokohama

</td><td>

This is happening to all scheduled reports where type is 'PDF' or 'PDF - landscape' and 'Include detail' = true. There's the same behavior on every instance, which was upgraded to Yokohama. These mails are sent with no text and no attachment. In logs, users see the error: 'EmailFormatter SEVERE \*\*\* ERROR \*\*\* error in substitution: java.lang. NullPointerException: Cannot invoke "com.glide.pdf. itext.components. Document.add \(com.glide.pdf. itext.components. Paragraph\)" because "this.fDocument" is null'.

</td><td>

1.  Open a scheduled report that's sending a report as a PDF.
2.  Try to execute it.
3.  Set the include\_detail to true.
4.  Check the email logs for this report.

 There's no attachment or text in the email sent.

</td></tr><tr><td>

Document Management Services

 PRB1892107

</td><td>

A visualization schedule in a PDF format seems to have incorrect columns

</td><td>

The issue doesn't occur on Excel report formats or when users export the report as a PDF and try to 'Send file via email'.

</td><td>

1.  Open a Yokohama instance.
2.  Navigate to 'Data Visualization'.
3.  Create a new report with type 'List - Simple'.
4.  Configure columns any way.
5.  Schedule the report with the following details:
    1.  Select 'File Type' as 'PDF'
    2.  'Reoccurance' = 'Once'
    3.  Populate the email address and subject of the report
6.  Select **Save** then **Send Now**.
7.  Navigate to sys\_email.LIST.
8.  Check for a sent email with a PDF report.
9.  Download the PDF report.

 The configured columns on the report aren't there. Instead, the downloaded report takes the columns that are configured in the default view on the platform.

</td></tr><tr><td>

Document Viewer

 PRB1902561

</td><td>

The background image inDocument HTML Templates is no longer visible in Yokohama

</td><td>

There's a difference in behavior with HR document template background images with Washington and Yokohama.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1898761

</td><td>

Email Client has a rendering issue in Next Experience due to '--now-accordion \_divider--color'

</td><td>

The issue doesn't happen in UI 16 or in Next Experience without Frame. The issue only happens in Next Experience with Frame.

</td><td>

1.  Provision an instance with sn\_csm\_gen\_ai installed.
2.  Set the email recommendation skill to active.
3.  Set the system property 'glide.ui.load\_ seismic\_email\_client' == true1.
4.  Navigate to an instance.
5.  Switch to Next Experience via personal settings.
6.  Navigate to any incident record.
7.  Select the 3 dots menu on the form header menu.
8.  Select **Email**.

 Expected behavior: The pop-up Email Client window should be rendered correctly.

 Actual behavior: The pop-up Email Client window is missing some CSS resources.

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

Event Management

 PRB1820659

</td><td>

sys\_trigger query is without an index

</td><td>

The Event Management job looks for sys\_trigger records by the **Name** field, which doesn't have an index. The performance can be improved with the same functionality by using the **job\_classification** field, which is indexed. The job classification is automatically applied to the sys\_trigger jobs.

</td><td>

1.  Capture an SQL statement used to look up EM jobs by name.
2.  Review the explain plan for the statement.

 Observe that the **Name** field doesn't have an index, so it displays using the full table scan.

</td></tr><tr><td>

Event Management

 PRB1830486

</td><td>

When deleting a ecc\_agent record, the self monitor service map isn't updated

</td><td>

The 'Update self health' business rule on the ecc\_agent table doesn't handle the delete case properly. The firing of the event evt\_mgmt.update \_self\_health when the record is deleted is with an invalid sys\_id.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1877169

 [KB2096192](https://hi.service-now.com/kb_view.do?sysparm_article=KB2096192)

</td><td>

Event Management Events in certain buckets are stuck in 'Ready' for hours after migrating

</td><td>

.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1891871

</td><td>

em\_events with the Resolution state 'Closing' aren't processed correctly during the CEST clock change window

</td><td>

em\_events with the Resolution state set to 'Closing' aren't processed correctly when their timestamp falls during the CEST clock change window. This results in the alert remaining open even though the closing event is received.

</td><td>

 

</td></tr><tr><td>

Field Service Management

 PRB1914183

</td><td>

Google Maps API doesn't work when calculating travel time in Field Service Management when changing the system date format

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1770528

</td><td>

A flow can start on another node before the flow inputs are persisted to the database

</td><td>

There are many conditions where NowMQ may not hold flow inputs in memory and they must be retrieved from the database: queue overflow, memory pressure, the node is shutting down, and so on. In these scenarios, flow inputs must be persisted to the database prior to queueing the event to the in-memory queue.

</td><td>

1.  Start a flow when the in-memory cache is full.
2.  Notice that if the node is under memory pressure, the current node may not cache the event and it may start on another node within a few seconds.

 Expected behavior: The flow starts with inputs properly persisted.

 Actual: The flow starts, but the inputs aren't available from the in-memory queue.

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

Flows \(Family Channel\)

 PRB1918469

</td><td>

There's error checking availability for a flow recommendations skill

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1921403

</td><td>

Tools \(actions/subflow\) do not honor ACLs/roles if the Agent ACL is successfully validated

</td><td>

When a tool inside AI agent is executed with certain roles and its internal\_name does not match the display name, it does not honor the ACL/role and proceeds with execution.

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

Glide Server APIs

 PRB1921133

</td><td>

Users can't query guest voice agents due to a lack of impersonation ability in a scoped app

</td><td>

The AI Voice agent application makes a call to a platform API to retrieve guest or public voice agents. These are agents that return basic public data such as company hours, location, etc. These agents have an ACL for a guest user. However, the integration user can't impersonate a guest since the app isn't in a global scope.

</td><td>

1.  Call into the voice agent app.
2.  Notice in the orchestrator that the public agents aren't queried correctly.

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

HR Service Delivery

 PRB1910181

</td><td>

Changes related to app-esm

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1915169

</td><td>

A seeding topic doesn't disappear post-seeding despite not existing in the Hermes topic inspector

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1922262

</td><td>

GEMINI tools break handleStreamMessage

</td><td>

Users see this issue when using GEMINI with the build agent and asking it to write code that contains an '\|\|' OR operator. Users see this error in the logs: 'Exception in GoogleGeminiResponseHandler while reading content from data chunk: Unterminated string at character 620 of...'

</td><td>

 

</td></tr><tr><td>

Internationalization Features

 PRB1911538

 [KB2266945](https://hi.service-now.com/kb_view.do?sysparm_article=KB2266945)

</td><td>

The 'Translated Text Synchronize' business rule has an infinite loop against v\_plugin

</td><td>

The 'Translated Text Synchronize' business rule goes in an infinite loop. The virtual table v\_plugin \(or any virtual table\) can refresh \(delete and insert of records\) the table upon query. Since v\_plugin has translated fields, glideRecord insert tries to insert into the sys\_translated\_text table, which runs the 'Translated Text Synchronize' business rule. This business rule tries to query the owner table i.e., v\_plugin again, which can trigger the refresh again and this goes on in an infinite loop. This is causing performance impact against many instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1927390

</td><td>

An API to get a Public Key associated to the Private Key used for JWT token signing

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

License Usage

 PRB1921586

</td><td>

Software Asset Workspace License Workbench's product search filter isn't filtering products from a list

</td><td>

This issue only affects Yokohama instances; Zurich and other versions aren't impacted.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1698906

 [KB1633481](https://hi.service-now.com/kb_view.do?sysparm_article=KB1633481)

</td><td>

The Workbench license consumption breakdown list view changes when the software product life cycle report changes

</td><td>

Editing columns in the Software Asset Workspace License Usage Report updates columns on the related lists.

</td><td>

1.  Log in to an instance.
2.  Navigate to the **Software Asset \(SAM\) Workspace**.
3.  Navigate to **License Usage** &gt; **Microsoft** &gt; **SQL Server** &gt; **Standard**.
4.  Select **License Metric Results**.
5.  Select the number link for the 'License required' column.
6.  Open the side view by selecting the number link for any 'License required' column.
7.  Select **Reports** &gt; **Software Product Lifecycle Report**.
8.  Change the column in the list view.
9.  Add some columns.
10. Refresh the License Consumption Details and Software Install Licensing.

 Notice that the details do not render in the table.

</td></tr><tr><td>

List Administration

 PRB1865572

</td><td>

Support fixed filters in the sys\_ux\_list configuration in the 'List' menu

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Configuration

 PRB1861671

</td><td>

List DAs with 'record selection required' aren't working when the list is grouped by a column

</td><td>

The format of the sys\_IDs passed to the daModel and then sent to the server don't seem correct.

</td><td>

1.  Navigate to a list for a given workspace that has a Server Script List DA with 'record selection required' set to true.
2.  Group the list by a column.
3.  Select a few rows.
4.  Select **Assign to me**.

 Notice the alert message telling the user they need to select records even though they just have selected records.

</td></tr><tr><td>

Major Incident Management

 PRB1858727

 [KB2399998](https://hi.service-now.com/kb_view.do?sysparm_article=KB2399998)

</td><td>

Modals in the workbench close when the user clicks out of the modal

</td><td>

 

</td><td>

Refer to the listed KB article for details.

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

 PRB1818637

</td><td>

HTTPClassyConnectionFactory throws AuthenticationFailedException when there's a connection error

</td><td>

Currently in AKeyConnectionFactory, the infrastructure only catches Automation AuthenticationException and iterates to the next credential. Other exceptions, such as AutomationIOException, if thrown, stop the loop and exit before moving onto the next credential. There should be a new, proper exception that the infrastructure can properly handle because it shouldn't throw an Authentication FailedException when there's a connection error in an http response.

</td><td>

1.  Create a dummy basic authentication credential.
2.  Run a Discovery on a host that has port 80/443 open, which isn't any devices that can be classified through HTTPClassifyProbe.
3.  Run Discovery.
4.  Verify that Authentication FailedException is thrown even though the error code of http response is 404.

</td></tr><tr><td>

MID Server

 PRB1885409

</td><td>

Discovery fails during the assumption from the US-East region due to internal restriction policies on AWS

</td><td>

This results in the error: 'AccessDenied: User is not authorized to perform sts:AssumeRole' when attempting to acquire temporary credentials.

</td><td>

 

</td></tr><tr><td>

Model Context Protocol Server

 PRB1923168

</td><td>

Add the 'MCP' scope to glide.services. rest.allowed\_ services to allow the MCP Store app to use sys\_service

</td><td>

glide.services. rest.allowed\_ services is a static list of scopes that can use the sys\_service using ServiceRESTMessage. 'sn\_mcp\_server=mcp-server' should be added to this list. This allows the scope sn\_mcp\_server to access the sys\_service record mcp-server.

</td><td>

From a Store app, call var rm = new sn\_internal\_services.ServiceRESTMessage\("mcp-server"\) and use rm to call the mcp-server exposed REST APIs.Excepted behavior: Users are able to call MCP server APIs.

Actual behavior: Users are unable to call MCP server APIs.

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

 PRB1868014

</td><td>

A conflict of recent factors and a multi-factor authentication \(MFA\) policy context leads to no MFA factor displaying in the log in flow

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Ensure that the MFA default email option is turned on.
3.  Create a user.
4.  Log in to an incognito browser.
5.  Ensure that it's redirected to a MFA setup page and that the mail option is displayed.
6.  Get the email OTP.
7.  Log in then log out of the instance.
8.  Check the 'Recent factors' table that an entry is added for that user.
9.  Enable MFA context.
10. Create an MFA factor policy to show an email factor for the itil role.
11. Re-log in with that user again.

 Expected behavior: The MFA factor policy returns false. The user should login directly/display other factors to log in.

 Actual behavior: As a policy is false and recent factors aren't taken as precedence over MFA context, the user isn't able to see any factor.

</td></tr><tr><td>

Next Experience User Menu

 PRB1926920

 [KB2442915](https://hi.service-now.com/kb_view.do?sysparm_article=KB2442915)

</td><td>

On instances with AI Agents, some users can't be found on the impersonation list

</td><td>

Currently, users with the **Identity type** field set to 'AI Agent' are filtered out, but they must also be filtered by 'is empty'.

</td><td>

Refer to the listed KB article for details.

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

 PRB1929041

</td><td>

SKILL\_EXECUTION\_STARTED passes aiaExecutionPlanId as empty in its payload

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

Now User Experience

 PRB1890272

</td><td>

A custom banner logo for an instance doesn't display for unauthenticated users

</td><td>

A broken image icon displays on the 'Log in' page.

</td><td>

 

</td></tr><tr><td>

OAuth

 PRB1927389

</td><td>

Support JWT Token format for OAuth access tokens

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1920363

</td><td>

checkLLMModelAvailability returns false when the user's preference language isn't English

</td><td>

Inside checkLLMModelAvailability compares 'gr.getDisplayValue\('available'\) == 'true'', but gr.getDisplayValue\('available'\) would return a translated word of 'true'.

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

There's exceptions: '\#35877 \[SEARCH API\] OrchestratorScriptUtil: Exception thrown when invoking sn\_ais\_assist.ConversationOrchestratorUtil script: org.mozilla.javascript.JavaScriptException: java.lang.NullPointerException...'

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
3.  Provide the prompt, 'Please create a user user's name having an email ID as user email address. The user should be a basic user only.'

 Expected behavior: A user should be created in Zoom.

 Actual behavior: The message appears, '\{'message':'Invalid inputs for tools execution: JavaException: java.lang.SecurityException: Illegal access to package\_private script include function AIAFdihDataTypeConstants: caller not in scope sn\_aia'\}'.

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

 PRB1925803

</td><td>

Model and language fields aren't present for the 'Sys GenAI Log' table

</td><td>

 

</td><td>

1.  Navigate to an instance with a user with elevated privileges.
2.  Open the sys\_generative\_ai\_log table.
3.  Verify and ensure that values for model\_name and model\_version are persisted in sys\_generative\_ ai\_log. model\_name and sys\_generative\_ ai\_log. model\_version for the NowLLM model.
4.  Verify that the **Target language** field is present.

 See that fields aren't present in the sys\_generative\_ai\_log table.

</td></tr><tr><td>

OneExtend

 PRB1926131

</td><td>

Unable to store long-term memory, skill 'LTM Identify memories \(Azure OpenAI C\)' / AIA Identify Episodic Memories throws an error in the log

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1926284

</td><td>

GAIC P0 Zero Day Attack Remediation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1926285

</td><td>

Integrate the regex, exact match, semantic and FSD detectors

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1927150

</td><td>

User gets a script error for an execution request

</td><td>

The script execution error: 'Script Identifier: null.null.script, Error Description: java.lang.NullPointerException: Cannot invoke "String.equalsIgnoreCase \(String\)" because the return value of "com.glide.one \_extend.resource. dto.v2.MultiCapability ExecutionRequestDto .getMode\(\)" is null, Script ES Level: 0...'

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

Oracle Reconciliation

 PRB1876511

</td><td>

An install shouldn't be deleted if there are applications pointing to it

</td><td>

 

</td><td>

 

</td></tr><tr><td>

PDF Generation

 PRB1890095

 [KB2184477](https://hi.service-now.com/kb_view.do?sysparm_article=KB2184477)

</td><td>

A PDF created from a view with dot-walked fields aren't displaying those fields or the exported PDF \(30B size\) is corrupted

</td><td>

When exporting a form, if the form contains dot-walking fields, then the value of those fields are empty in the exported PDF file. If the parent of the dot-walking field isn't present and dot-walking fields are present, then a corrupted PDF is generating with an error: 'Failed to load PDF document.'

</td><td>

1.  Navigate to a Yokohama instance.
2.  Find a record with dot-walked fields.
3.  Right-click the form header and export to PDF.

 Notice that the dot0walked fields **Model.model\_number** and **Model catergory.Name** aren't displaying. Also, if the parent of the dot-walking field is missing, then the corrupted PDF is generated with 30 bytes. The exported file \(30B size\) displays 'Failed to lad PDF attachment'.

</td></tr><tr><td>

PDF Generation

 PRB1893129

</td><td>

Aggregation functions \(Total, Min, Max, Avg\) aren't displayed in an exported PDF

</td><td>

When an aggregation function \(Total, Min, Max, Avg\) is applied on a column in list view, the result isn't displayed in the exported PDF.

</td><td>

1.  Navigate to a Yokohama instance.
2.  Navigate to any table.
3.  **Configure** &gt; **List Calculations** &gt; **** on a suitable column.
4.  Select an aggregation function \(Total, Max, Min, or Avg\).
5.  Select **OK**.

At the end of selected column, the aggregation function output is displayed.

6.  **Export** &gt; **PDF**.

 Expected behavior: In the exported PDF, an aggregation function output is displayed at the end of all rows under the column on which aggregation function is applied.

 Actual behavior: In the exported PDF, aggregation function output isn't displayed at the end of all rows.

</td></tr><tr><td>

Platform Analytics Filters

 PRB1838937

</td><td>

When a non-admin user creates a Platform Analytics 'Date' filter, 'Field' flashes briefly and is then cleared when selected, depending on the table chosen

</td><td>

Depending on the table chosen in the data to filter modal, entries selected in 'Field' flash briefly and are then cleared, and don't remain selected.

</td><td>

1.  Grant a non-admin user the analytics\_filter\_admin role.
2.  Impersonate the user.
3.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Filters**.
4.  Select **New**.
5.  Navigate to **Filter Type** &gt; **Date** &gt; **Data to filter** &gt; **Add**.
6.  Select **Task** in the field **Table** in the Data to filter modal.
7.  Select **Created** under **Field**.

 Observe that 'Created' flashes briefly and is then cleared, and the selection does not remain.

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

Record Watcher

 PRB1894715

</td><td>

ChecklistItemResponder is too slow to effectively scale with normal usage of the platform, leading to the record watcher queue becoming backlogged

</td><td>

A performance issue has been identified related to checkLitsItem responders and ACL \(Access Control List\) checks while creating checkListItems in Visual Task Board's cards. These issues caused delays, especially when tasks had more than 50 checklist items. This is primarily because getItemsByChecklistId\(\) is invoked every time a checklist item is added or a card is moved between lanes. It loops through all items under a checklist and performs individual ACL evaluations \(read/delete access\). These checks result in: Repeated database lookups, redundant ACL checks for the same parent checklist, and slower response times, especially when checklist items exceed 50.

</td><td>

 

</td></tr><tr><td>

Search Application Configurations

 PRB1912254

</td><td>

Performance test results for the E2E backend query show high response results

</td><td>

When the user runs a jmter test for a backend E2E query, the test results show a high response time, with an average of 1065 milliseconds.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1881845

</td><td>

globalThis isn't correctly shared between separate imports of the same module

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1886474

</td><td>

Users aren't able to turn off the ES toggle for an existing record

</td><td>

 

</td><td>

1.  Log in to a Yokohama or Zurich instance.
2.  Navigate to the 'Script include' table.
3.  Open any existing record which has ES toggle turned on.
4.  Turn off the ES toggle.
5.  Save the record.

 Expected behavior: The toggle should be turned off.

 Actual behavior: The toggle is still turned on.

</td></tr><tr><td>

Server-side scripts

 PRB1915039

</td><td>

Regex fails with 'Invalid quantifier ?: com.glide. rest.domain. ServiceException: Invalid quantifier ?'

</td><td>

The issue only affects Yokohama due to a missing polyfill in that version.

</td><td>

 

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

Service Portfolio Management

 PRB1897750

</td><td>

Lifecycle rules prevent certain actions

</td><td>

Lifecycle rules prevent users from adding an offering to a service that isn't operational. The user also can't move a service or offering from operational back to an earlier stage \(for example, ideation or design\).

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1857027

 [KB2214434](https://hi.service-now.com/kb_view.do?sysparm_article=KB2214434)

</td><td>

Performance enhancement for the 'Bookkeeping for dedup on delete' business rule

</td><td>

The number of records to update may be reduced if there's an additionally query on primary\_install is not null and deduplicated=true.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1865376

</td><td>

Unlicensed/actionable installs list are grouped by document ID by default, which turns off pagination

</td><td>

The unlicensed and actionable installs lists are grouped by the **m2m\_entity** field by default. Since they're grouped by a document ID, pagination is turned off and the user can't access more than 20 items.

</td><td>

1.  Run recon with demo data.
2.  Navigate to any software publisher result.
3.  Select **unlicensed install** or **installs requiring action with count &gt; 20**.

 Observe that the list view is grouped by the **m2m\_entity** field, which is a **Document id** field. The page only displays 20 items and pagination doesn't work.

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

 PRB1923069

</td><td>

In Software Asset Management \(SAM\) Workspace, users are unable to dot walk within a table in a Yokohama SAM Discovery model list

</td><td>

This is happening for other tables too in the License Operations module.

</td><td>

1.  Navigate to **SAM Workspace** &gt; **License Operations module**.
2.  Select any list.
3.  Select the 'Personalize list' icon.
4.  Try to add a referenced column.

 Observe that a reference dotwalk isn't available.

</td></tr><tr><td>

Software Asset Normalization

 PRB1916894

 [KB2397254](https://hi.service-now.com/kb_view.do?sysparm_article=KB2397254)

</td><td>

A 'Normalization' job isn't re-normalizing discovery models when incorrect content rules are deactivated

</td><td>

When a discovery model table is queried with an array containing more than a million sys\_id's in addquery, GlideRecord query silently failed with a QuerySizeToo LargeSQLException. The max limit for a SELECT query is 32MB and it hit 33.5MB for our 1.2M sys\_ids. With a recent increase in inactive content rules, this limit has been hit in the last 1 month.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reclamation

 PRB1882484

</td><td>

A business rule prevents duplicate reclamation candidates, causing bulk RC not to be created

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Software Asset Reclamation

 PRB1896341

 [KB2171072](https://hi.service-now.com/kb_view.do?sysparm_article=KB2171072)

</td><td>

There's reclamation candidate and reclamation rule issues

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Lifecycles \(Family Channel\)

 PRB1910582

</td><td>

There's a duplicate sys\_choice for current\_lifecycle\_phase in sam\_sw\_product\_ lifecycle\_report

</td><td>

The duplicate might be coming from the older field as they don't exist in that older field anymore.

</td><td>

 

</td></tr><tr><td>

Software Models

 PRB1828999

</td><td>

'Get install count for software model' job runs a large query when the software model is corrupted in Software Asset Management \(SAM\)

</td><td>

The 'Get install count for software model' job creates an encoded query for a software model to match the corresponding discovery model. The query generated is 'null' when the software model version/edition operator is corrupted. This causes all discovery models to be picked for matching, which creates a large query and results in the job running forever.

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

Template Management for Field Service

 PRB1920388

</td><td>

When accessing a work order template, $sm\_templates can be slow and cause memory issues on the client-side \(browser\)

</td><td>

.

</td><td>

1.  Open https://\[instance\_name\].service-now.com/$sm\_templates.do ?sys\_id=\[template\_sysid\].

Notice it's slow if the templates have a relatively large number of the task templates.

2.  If it loads eventually, load it multiple times.

Notice that the page timeouts and become blank.

3.  Monitor client-side memory.

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

 PRB1893476

</td><td>

Tier 2 Index tables don't properly store DocumentID data

</td><td>

When creating a Tier 2 offload rule, the user is able to select DocumentID columns for indexing on the cidx\_ table created to store the indexed data. Columns of DocumentID type are missing the **Dependent** field, which impacts the navigation and readability of index tables. This results in no previews or quick links to the record on cidx table.

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

UI Field Administration

 PRB1827405

</td><td>

A UI16 form loads slowly when the **Composite Name** type field is added and the instance has a lot of metadata

</td><td>

If a form has a **Composite Name** type field on it and there's much metadata present, the form can take upwards of 15-20 seconds to load.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1875982

</td><td>

Now Assist Context Menu \(NACM\) isn't rendered on a few form fields on an INC form

</td><td>

After creating and activating a new skill on an Incident form field, the NACM isn't rendered for some fields.

</td><td>

1.  Log in to a Washington DC instance.
2.  Ensure Gen AI is set up.
3.  Navigate to **Now Assist Admin \(NAA\)** &gt; **NACM experiences**.
4.  Create a new skill configuration on the **Incident form** field.
5.  Add **Record form** fields such as **Subcategory**, **Short description**, and **Service**.
6.  Activate the skill.
7.  Open an INC record.

 Observe that the NACM sparkle isn't rendered on the form for the fields **Subcategory** and **Short description**.

</td></tr><tr><td>

UI Form Administration

 PRB1880019

</td><td>

Field labels aren't displaying horizontally even though glide.ui.form.breakpoints.enable is true

</td><td>

If the form width is more than or equal to 800 pixels, then field labels should display horizontally. If glide.ui.form. breakpoints.enable is false, the form should be in a 2 column layout and field labels should display vertically after increasing the form layout.

</td><td>

1.  Log in to a Next Experience instance with an admin user.
2.  Open the sys\_properties table.
3.  Search for glide.ui.form.b reakpoints.enable and make it true.
4.  Open any configurable workspace.
5.  Open any of the record form.
6.  Increase the form layout by using the resizable pane.

 Expected behavior: Field labels should display horizontally beside the label after increasing the from layout.

 Actual behavior: Field labels aren't displaying horizontally after increasing the from layout.

</td></tr><tr><td>

UI Form Administration

 PRB1881995

</td><td>

Content on 'Special Handling Notes' isn't scrollable

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1900373

</td><td>

Form controller events are no longer prioritized after the Xanadu release

</td><td>

The root cause has been determined to be that the dispatch function being used by the Forms controller and client scripts \(api.emit\) has changed between Washington and Xanadu. In Xanadu, data fetching on component mounting was replaced with a GraphQL databroker. Databroker execution isn't prioritized, so all subsequent events from the form controller aren't prioritized.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1919041

</td><td>

An empty and read-only **Template value** input field causes an error when saving a record: 'Cannot read properties of null \(reading 'hasChildNodes'\)\)'

</td><td>

To reproduce, users need a record with an input field of type 'Template Value', that is empty and also read-only. The error shows when saving the record.

</td><td>

1.  Log in as an admin.
2.  Navigate to **All** &gt; **incident.CONFIG**.
3.  Add a field called **Test Template**.
4.  Make it of the type 'Template Value' and save.
5.  Select the 'Advanced' view and the 'Dependent Field' tab.
6.  Select 'Use dependent field' and a field, such as **Channel**.
7.  Save the changes.
8.  Navigate to **All** &gt; **incident.CONFIG**.
9.  Create a UI Policy that will always make the new template value field read-only.
10. Pick an existing incident.
11. Make a change to the **Short description** field and save.

 Expected behavior: The record should save without error.

 Actual behavior: There's an error: 'Cannot read properties of null \(reading 'hasChildNodes'\)'.

</td></tr><tr><td>

Usage Analytics

 PRB1923117

</td><td>

Allow the MCP app to access Clickhouse-based query services

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

 PRB1827900

</td><td>

The **New** button is missing in the 'Cases for Opened for User' related list

</td><td>

 

</td><td>

1.  Provision an instance with sn\_hr\_core sn\_hr\_agent\_ws 4.0.0-SNAPSHOT latest build installed.
2.  Open a HR case.
3.  Access cases for the opened 'For User' related list.
4.  Observe the list actions.

 See that the **New** button is missing.

</td></tr><tr><td>

UX Framework

 PRB1870378

</td><td>

Components fail to load in an instance after upgrading to Xanadu due to an asset bundling issue

</td><td>

In the asset 'string\_decoder', there's a regex which removes the source mapping URL in the bundle. This fails to identify the entire string.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1871297

</td><td>

UXF pages are broken due to the duplicate assets with different versions bundled in the nds-bundle

</td><td>

The new release of the sn-datagrid brings in new versions of side-channel-weak-map, side-channle and get-intrinsic which end up pulling in call-bind-apply-helpers 1.0.2 to the instance. When nds-bundle is built, it doesn't deduplicate assets with deep import paths, so both call-bind-apply-helpers/1.0.1/functionApply and call-bind-apply-helpers/1.0.2/functionApply are added to the nds-bundle. They share the same global variable name: \_\_TECTONIC\_\_ call\_bind\_apply \_helpers\_functionapply, so it ends up calling wrapTectonicVarIfNeeded\(\) twice for the same tectonic variable, which causes it to be double wrapped.

</td><td>

1.  Navigate to sn-datagrid.
2.  Build the zip of the component.
3.  Sideload the zip on to any instance.
4.  Navigate to the home page.

 Notice that the page is broken.

</td></tr><tr><td>

UX Framework

 PRB1923311

</td><td>

UX dependency tracing should use LargeContentDiskCache.getMetadata to avoid file touching

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
5.  Navigate to Agentic Portal in a separate browser tab.

Don't attempt to log in.

6.  Open up the dev console.
7.  Execute the script.
8.  Execute the code.
9.  Select the chat bubble that appears after the code finishes executing.

 Expected behavior: The chat loads with content.

 Actual behavior: The chat load is blank and a security error appears in console.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1917696

</td><td>

Virtual Agent Designer isn't displaying options for subflows if there are more than 100 spokes

</td><td>

 

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

 PRB1896418

</td><td>

Gaic Timing on for App Generation on XP3 with NAFC NAFC26.4.0

</td><td>

This is a product update.

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

 PRB1920712

</td><td>

FDIH isn't replaying if the last played node is a subflow

</td><td>

FDIH should replay both subflows and actions.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1920729

</td><td>

Multiple conversations fail to maintain an 'adapter' state

</td><td>

consumerAccount and externalConversationId are missing sys\_cs\_adapter\_conversation\_lookup for the first conversation.

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

 PRB1922176

</td><td>

For a guest user when a skill is promoted, that skill card shouldn't be seen in Virtual Agent

</td><td>

 

</td><td>

 

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

 Actual Results: A choice picker with radio buttons displays.

 Expected Results: A text picker with a list of topics displays if the user has turned on the new sys prop.

</td></tr><tr><td>

Virtual Agent

 PRB1923219

</td><td>

The live agent conversation banner stays on 'Cancel request' even after the user has canceled the request

</td><td>

On ending a live agent conversation, users get an empty skill picker topic and the client is able to understand that there's a new message coming in and ends the spinner display. However, no such message comes in and users are stuck in the routing to the live agent spinner.

</td><td>

1.  Navigate to Dynamic Window.
2.  Type and connect to a live agent.
3.  From the user side, select **Cancel**.

 Expected behavior: The chat is canceled and the banner changes to the requested query title.

 Actual behavior: When the requestor selects the **Cancel** button, the original created work item is canceled but 'routing to live agent' won't disappear from the chat window.

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

Slow API queries for NowAssist ConversationHistory\(\) .\_getTranscriptFor ConversationHistory API

</td><td>

 

</td><td>

1.  Open an instance.
2.  Go to the ESC portal
3.  In the NASS chat, type an utterance like 'Hello!'.
4.  Check the system logs for keywords starting with 'NowAssistConversationHistory: Time taken to retrieve transcripts for conversation history is.'

 For a new conversation, observe that the first hit to this API takes over 500 milliseconds.

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

Virtual Agent Web Client

 PRB1896390

</td><td>

Console errors for va\_web\_client API failures are displayed when launching a chat in the CSM portal and Engagement Messenger

</td><td>

Two console errors related to va\_web\_client are observed: '/api/now/ va\_web\_client\_settings /get\_va\_web\_ client\_settings' api results 403 error' and '\[SNAnalytics\] Invalid property name'. Console errors shouldn't be displayed and chat functionality should work as expected.

</td><td>

1.  Log in to an instance.
2.  Navigate to CSM portal or Engagement Messenger. Launch Virtual Agent chat/start a chat.
3.  Observe the browser console.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1896591

</td><td>

Emoji panel loading is slow in Windows OS

</td><td>

Chrome and Edge browsers freeze for one minute after the user clicks an Emoji icon in the Virtual Agent Web Client.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1920035

</td><td>

The 'VTT' icon isn't available in previous model of Now Assist Portal \(NAP\)

</td><td>

The issue occurs when the user switches from the new model to the previous model with VTT turned on.

</td><td>

1.  Install any of the BU skills.
2.  Turn on NAP with VTT turned on.
3.  Turn on the microphone from the browser preferences.
4.  Select the 'NAP' icon and ensure that the VTT icon is available in the new model.
5.  Change the model to the previous model from 'now/nav/ui /classic/params /target/sys\_now\_ assist\_deployment\_ channel\_list.do'.
6.  Refresh the page.

 Expected behavior: The 'VTT' icon should be available/

 Actual behavior: Observe that the 'VTT' icon isn't available in the previous model of NAP when the user switches from the new model to the previous model with VTT turned on.

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

 Expected behavior: The citation link is turned off and clicking on it doesn't trigger any action.

 Actual behavior: The citation link is available to click and runs into an error if clicked.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1922217

</td><td>

ServiceNowChat.open isn't opening Portable Virtual Agent

</td><td>

 

</td><td>

1.  Implement the 'ServiceNowChat Third Party' API.
2.  Call serviceNowChat.open\(\).

 Notice that the chat never opens.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1922825

</td><td>

The **New chat** button is in turned off mode after a live agent connection has ended when the chat history is turned off

</td><td>

 

</td><td>

1.  Navigate to Dynamic Window.
2.  Start a live chat.
3.  Accept the chat as an agent.
4.  End the chat from the requester end.

 Expected behavior: The **New Chat** button should be turned on and the requester should be able to click on it.

 Actual behavior: The **New chat** button is turned off and is turned on only on refresh.

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
4.  Select the 'Go to Search Results' icon.

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
5.  Navigate to Agentic Portal in a separate browser tab.

Don't attempt to log in.

6.  Open up the dev console.
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

Workforce Optimization for IT Service Management

 PRB1916888

</td><td>

There's an issue with the 'Work Scheduler' filter in Manager Workspace

</td><td>

A user isn't able to see the SCTask assigned to a group.

</td><td>

1.  Navigate to a Yokohama instance.
2.  Navigate to **Manager Workspace** &gt; **Work Scheduler**.
3.  Try assigning any unassigned SCTasks to a group.

 When users try to filter with 'Assignment group' from the right side filter panel, they aren't able to see the SCTask assigned to the group.

</td></tr><tr><td>

Work Order Management

 PRB1840169

</td><td>

When a multi-shift WOT status changes to 'WIP', its end time is displayed incorrectly without considering shifts on Dispatcher Workspace \(DWS\)

</td><td>

When the work duration covers multiple work ps of the assigned agent, the business rule for calculating the estimated end time is taking the agent work schedule into consideration and doesn't count their off-shift time. However, on DWS, when a task changes to 'WIP', the display end time is calculated by directly adding the work duration to the scheduled start time and doesn't consider the agent's off shift time. The behavior on platform and DWS is inconsistent.

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

 PRB1921026

</td><td>

**Status** field choices differ from those on the 'Work Order' form view when setting up a Work Order Task \(WOT\) template

</td><td>

When setting up a WOT template, the choices that appear for the **Status** \[state\] field differ from the choices that appear on the WO form view. Also, when setting up a WO template, choices don't appear for the **Service Request Type** field.

</td><td>

1.  Navigate to the list of Work Order Models \[cmdb\_workorder\_product\_model\].
2.  Select the **GE ULRICH ASSEMBLY** model.

 Notice that under 'Request Information', 'Service Request Type' doesn't provide selections. Also, notice that under 'Task information', the 'Status' choices differ from the choices that are available on the WOT form view.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 6 Hotfix 2](yokohama-patch-6-hf-2.md)
-   [Yokohama Patch 6 Hotfix 1](yokohama-patch-6-hf-1.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5 Hotfix 3](yokohama-patch-5-hf-3-PO.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2425802)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


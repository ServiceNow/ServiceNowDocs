---
title: Yokohama Patch 12
description: The Yokohama Patch 12 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2026-02-06"
reading_time_minutes: 38
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 12

The Yokohama Patch 12 release contains important problem fixes.

-   **Yokohama Patch 12 was released on February 06, 2026.**
    -   Build date: 02-03-2026\_1624
    -   Build tag: glide-yokohama-12-18-2024\_\_patch12-01-20-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y12.00.xlsx).

## Overview

Yokohama Patch 12 includes 139 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp12.png "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 12 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 12, refer to [KB2720387](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2720387).

## Changes in Yokohama Patch 12

-   **[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)**

    For Now Assist new features and changes, see [Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md).


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

 PRB1973244

</td><td>

Texts do not clear out from **Journal** fields, such as comments/work notes, after selecting **Save** in workspaces

</td><td>

When inserting a text in the **Journal** fields and going to save the records, the journal entry is created but the text remains in the box. This happens only when using the **Save** button, but works correctly when using the **Post** button.

</td><td>

1.  Open any active case, problem, incident in CSM/FSM or Service Operations Workspace \(SOW\).
2.  Insert text into the Internal Info \(work notes\) and Comments.
3.  Select **Save**.

 Expected behavior: The text disappears after the user saves it.

 Actual behavior: The text remains in text box after the user saves it.

</td></tr><tr><td>

Application Manager

 PRB1981044

 [KB2719949](https://hi.service-now.com/kb_view.do?sysparm_article=KB2719949)

</td><td>

The latest version in the sys\_store\_app table is updated to the installed version after an install, which causes the **Upgrade** button to be unavailable in App Manager

</td><td>

Two functions \(\_fixLatestVersionFor WithdrawnInstalledApps, \_fixLatestVersionFor WithdrawnInstalledCustomizations\) in Application Manager's UpdateChecker.checkAvailableUpdates API \(aka Sync in the UI\) were missing a required GlideRecord.addQuery constraint when the 'sn\_appclient.enable\_app\_ manager\_checksums\_cache' sys\_property was set to 'true' \(default\). This regression led to the 'latest\_version' being set to the incorrect values on Install/Sync.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1909893

</td><td>

The 'Run' filter can apply an old condition and not pick up the newly applied filter conditions

</td><td>

In the CMDB Relationship editor, the filter can apply old conditions and not pick up the newly applied filter conditions. This issue isn't consistently reproducible but there's a problematic API call made.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1829096

</td><td>

There's an incorrect timeref display value for ISO week 53

</td><td>

It's cosmetic as only the axis labels are affected and the real values are preserved.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1952527

</td><td>

An email template isn't applied when users select **Apply template** in the mini/full composer

</td><td>

The template isn't applied.

</td><td>

1.  Log in as an admin user.
2.  Navigate to CSM/SOW workspace and open an incident/case record.
3.  Navigate to the email tab in the activity stream.
4.  Select the **Apply templates** icon.
5.  Select a template.
6.  Select **Apply**.

 Expected behavior: The template should be applied.

 Actual behavior: The template isn't applied.

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

Server-side scripts

 PRB1972733

</td><td>

Field translations for security integrations are failing and return a null value

</td><td>

The field translations aren't working. On changing the field evaluator.withEnforcedSecurity\(false\), field translations work as expected.

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

Advanced Work Assignment

 PRB1982818

</td><td>

After removing a service channel, the current universal capacity of the agent isn't decreased

</td><td>

After removing a service channel from the 'Available' presence state, the universal capacity for the existing documents related to that channel shouldn't be considered.

</td><td>

1.  Create a service channel \('Chat-test'\).
2.  Add it to the 'Available' presence state in awa\_presence\_state.
3.  Create related queues and assignment eligibility pools.
4.  Create a universal capacity record for the agent \('Beth Anglin'\).
5.  Make the agent 'Available'.
6.  Create documents for that and let those be assigned to the agent.

Observe that the current universal capacity of the agent is increased.

7.  Remove the service channel from the 'Available" presence state in awa\_presence\_state.

 Observe that the current universal capacity of the agent stays the same. In Xanadu and Zurich, the current universal capacity gets decreased.

</td></tr><tr><td>

Agile Development

 PRB1968771

</td><td>

/sn\_safe\_$safe\_board.do \#/teamBacklog is broken

</td><td>

Loading different PIs in the SAFe team backlog board in Zurich isn't working. The data in the board doesn't always change and can take multiple tries to change the PI on the board.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1970081

</td><td>

Agent/Workflow Access not working for elevated roles

</td><td>

Although the user is shown to have the elevated roles, the user appears to be blocked from accessing the agent after testing the Agent Access.

</td><td>

1.  Create an instance with the latest track or znowassist.
2.  Run the December deployment plan.
3.  Create an agent.
4.  Restrict the access and roles to couple of elevated roles.
5.  Create a user.
6.  Assign these elevated roles to the user.
7.  Test the Agent Access from the Agent Studio against the user.

 Observe that the initial screen shows the user has these elevated roles. However, after running the test, the results show that the user is blocked from accessing the agent. However, the ACL check fails, but the role masking still passes.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1972747

</td><td>

Ten assists for catalog execution in the fully agentic should be charged

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1926964

</td><td>

E5 encoding does not work when a non-base instance English \(EN\) record is created in the sys\_language table

</td><td>

The issue occurs because E5 model config references sys\_language records for supported languages. It saves sys\_id of the record. However, if the user's instance has a non-base instance language record, it will not work with E5.

</td><td>

 

</td></tr><tr><td>

AI Search for Service Portal

 PRB1956814

</td><td>

Pressing the 'Enter' key doesn't open the link

</td><td>

When the tab focus is on the link and the 'Enter' key is pressed, the link doesn't open. However, if the user presses the Tab key, the focus moves to hidden and pressing Enter opens the link.

</td><td>

1.  Open any base instance with AI search enabled.
2.  Navigate to the Service portal.
3.  Navigate to the **Search edit** field.
4.  Search for 'email'.
5.  Navigate to the search results.
6.  Select a filter.
7.  Navigate to any links in the 'Results' section.
8.  Press the Enter key to select.
9.  Verify whether it opens.

 Expected behavior: The tab focus is on the link, and pressing the Enter key opens it. Pressing the Tab key moves the focus to the next interactive element.

 Actual behavior: When the tab focus is on the link and the 'Enter' key is pressed, the link doesn't open. However, if the user presses the Tab key, the focus moves to hidden and pressing Enter opens the link.

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

AI Search doesn't populate sys\_search\_source\_event with sources that weren't returned

</td><td>

 

</td><td>

1.  Enable AI Search for a portal.
2.  Search for a query that doesn't return documents from a search source.

 Observe that only the tables from search results that were returned were added to sys\_search\_source\_event.

</td></tr><tr><td>

AI Search UX

 PRB1973402

</td><td>

Genius results are stacked vertically instead of horizontally in Service Portal

</td><td>

This issue occurs in Yokohama and Washington DC.

</td><td>

 

</td></tr><tr><td>

Appointment Booking

 PRB1940645

</td><td>

If users load an appointment booking on a portal home page and then use the Service Portal \(SP\) date picker in a different portal page, the datepicker isn't selectable until a page reload

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

1.  Impersonate the user Ruaa Kuecken.
2.  Navigate to the Credentials page.
3.  Select **Fingerprinting**.
4.  From the location drop-down list, select **San Diego - Linda Vista Campus**.
5.  Answer the question 'What is your reason for visiting?' with 'Fingerprinting'.
6.  Select the **calendar** icon next to Appointment.

 Notice that appointment slots are available during the blackout schedule \(for example, December 31\).

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

 Expected behavior: Information about the user's open HR Cases is displayed.

 Actual behavior: The user receives the error 'An unexpected error occurred. Please try again.'

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1965782

</td><td>

RCA created during case summarization/resolution notes generation

</td><td>

RCAs are generated when modifying any fields in an HR case and its child tables, which causes test failures.

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB1821909

</td><td>

RecordReferenceConnected GQL query is seen on createCase flow, which wasn't the case in Xanadu

</td><td>

 

</td><td>

1.  Open any instance on main or track/perfintegrations where CSM is installed with demo data.
2.  Impersonate any user with the sn\_customerservice\_agent role.
3.  Navigate to the CSM workspace.
4.  Navigate to the case list view.
5.  Select **New** to create a case.
6.  Enter a random string in the short description.
7.  Set the value of the **Account** field.
8.  Set the **Short Description** field a random string.
9.  Select **Save**.

 Expected behavior: The user doesn't see the call to snRecordReferenceConnected.

 Actual result: The user sees a GQL call to snRecordReferenceConnected.

</td></tr><tr><td>

Change Management

 PRB1953175

 [KB2675721](https://hi.service-now.com/kb_view.do?sysparm_article=KB2675721)

</td><td>

The 'Notify assessment' user notification is triggered unnecessarily for change risk assessments

</td><td>

The email notification is triggered by the subflow 'Notify Assessment user' at the time when a risk assessment is opened \(where in theory the user completes the risk assessment\). By the time the email notification is received, this message becomes unnecessary.

</td><td>

1.  Navigate to a change request.
2.  Save the change request.
3.  Open a risk assessment and complete it.

 Observe a notification saying the user has been assigned an assessment \(event 'assessment.received' in the 'sysevent' table\).

</td></tr><tr><td>

CMDB Data Manager

 PRB1943938

</td><td>

The Data Manager policy jobs experience increasing slowness creating tasks when processing large data sets

</td><td>

The CMDB Data Manager policy for running jobs keep running for a long time because the underlying SQL query has pattern of LIMIT and OFFSET on the CMDB table. The table has a lot of data, and thus those SQL queries start showing increased execution time, effectively slowing the job running them.

</td><td>

 

</td></tr><tr><td>

Communities

 PRB1952833

</td><td>

Blog posts within Community forums have all been reformatted

</td><td>

The HTML code not showing properly on blog in community portal.

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

Data Archiving to Object Store

 PRB1890833

</td><td>

Corrupted attachments cause repeated offload failures, chunk starvation

</td><td>

 

</td><td>

1.  Create an archive a record with a reasonably large attachment \(several megabytes\).
2.  Delete one of the sys\_attachment\_doc records for this attachment.
3.  Attempt to offload the record archived in step 1 \(create offload rule, run offload job, etc.\).

 The offload errors out both now and on every subsequent reattempt. If enough attachments get corrupted, it can have broken chunks on every reattempt, preventing anything being offloaded for this rule.

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1893485

</td><td>

If a related record hasn't finished offloading, 'Restore from Tier 2' can cause unpredictable results

</td><td>

This is hard to reproduce without a large backlog to offload.

</td><td>

1.  Archive a record and its related record.
2.  Serialize the related record to a string and retain for now.
3.  Offload the record \(and the related record\).
4.  Simulate that the offloaded record is incomplete by changing its chunk status in sys\_archive\_tier2\_chunk to 'running'.
5.  De-serialize the string from step 2 back into the 'Archive' table.
6.  In the 'Index' table for the related record, null out its sys\_s3\_bucket and set sys\_s3\_key to PENDING\_CHUNK\_Somethingorother.

Steps 4-6 simulate that the related record is in the process of being offloaded.

7.  Restore the parent record to Tier 1.

 Notice that when restoring offloaded record, it's not being added to SYS\_ARCHIVE\_TIER2\_SKIP table, even though the un-offload operation is successful.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1924708

</td><td>

Show Matching a list and order by **ref\_** fields throws NPE

</td><td>

After the user orders the list, the records disappear.

</td><td>

1.  Navigate to task.list.
2.  Open**Configure** &gt; **List Layout**.
3.  Add the planned start date \[change request\] to the list of columns.
4.  Save.
5.  Add watch list to the view.
6.  Populate the watch list of some records.
7.  Show Match watch list.
8.  Order by the planned start date \[change request\].

 Expected behavior: The records show.

 Actual behavior: The records disappear.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1944597

</td><td>

Multiple applications under the same sys\_scope create an invalid GraphMetadata Object

</td><td>

An error occurs.

</td><td>

1.  Install CCOE-Global custom application or any application that is within a global scope.
2.  Create a new knowledge graph under CCOE-Global.
3.  Perform new sn\_db.GraphMetadata \('global.graph\_name'\).get\(\);.

 Notice the error, 'No graph named global.graph\_name was found.'

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1968109

</td><td>

When glide.db.aggregate. groupby\_display\_optimize is true, group by reference fields display value is a sys\_id

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1889276

</td><td>

deleteMultiple fails for PG for IN conditions larger than 1000

</td><td>

A NullPointerException is thrown: 'Exception attempting to delete from: u\_cstask\_multiple\_delete: java.lang.NullPointerException: Cannot invoke 'java.util.List.addAll\(java.util.Collection\)' because 'this.fPlaceHolders' is null: com.glide.db.conditions.ASetCondition .formatFieldSet\(ASetCondition.java:265\) com.glide.db.conditions.ASetCondition .formatSet\(ASetCondition.java:157\)'.

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

This issue was observed in a user's production instance where the PRI database connection pool became exhausted. The exhaustion occurred because several threads were holding PRI DB connections while executing queries on the RR database. During this time, the RR database went down \(due to a hardware failure\), and these threads remained blocked for approximately 10–15 minutes, resulting in pool exhaustion.

</td><td>

1.  Create an instance that has a read-replica DB.
2.  Execute repeated transactions that result in routing some, but not all, of the queries to the read replica.
3.  While these queries are running, the read-replica database must go down \(either kill -9 or unplug the box\).

 Observe that the system becomes unavailable for 10-15 minutes until the transactions begin to timeout.

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

The launching time of massive number of probes should be improved.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1903928

</td><td>

Slow query with primary\_hash= -865319141 runs 60k times per day, consuming reasonable time from the database

</td><td>

Users with a relatively high number of records on cmp\_discovery\_ldc\_config may be affected by query primary\_hash= -865319141. It can run thousands of times, reading the entire table.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1969791

</td><td>

The Discovery Pattern logs say Warning CI Pattern is completed, even though the pattern failed completely

</td><td>

Even though the classification is successful, if the pattern fails to get the basic identification details such as name, serial number, etc., the pattern fails completely. However, the Discovery Pattern logs say that the Warning CI Pattern was completed but failed some post-processing steps.

</td><td>

Run an SNMP Discovery.

 Observe that the pattern fails if it fails to get the basic identification details. However, the Discovery Pattern logs say the Warning CI Pattern was completed but failed some post-processing steps.

</td></tr><tr><td>

Discovery

 PRB1974425

</td><td>

Make the **Discover Now** button primary in the workspace 'Form' view

</td><td>

Update the button style on the existing UI action record for **Discover now** to mark it as primary.

</td><td>

1.  Navigate to **Discovery Admin Workspace** &gt; **Schedules**.
2.  Select any IP-based schedule.
3.  On the 'Schedule Details' page, select the 'Schedule Details' section.

 Expected behavior: As one of the main UI actions on each schedule form is **Discover Now**, it should be displayed as a primary button.

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

 Expected behavior: Drafting an email shouldn't encounter unexpected cursor placement to the end.

 Actual behavior: The cursor jumps to the end while typing.

</td></tr><tr><td>

Event Management

 PRB1953971

</td><td>

There are two columns named 'text' in the table sa\_agg\_alert\_filter, but one of them should be network\_traffic

</td><td>

The label is 'Network Traffic', but the column name is 'text', so there's no separated flag for network traffic.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1954172

 [KB2615509](https://hi.service-now.com/kb_view.do?sysparm_article=KB2615509)

</td><td>

Automated group is created even if some of the alerts don't match the aggregated alerts filter

</td><td>

Defined alert aggregation filter sa\_agg\_alert\_filter isn't working and alerts are still grouped.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1978591

</td><td>

PRC list contains new and outdated change requests that should be filtered out

</td><td>

 

</td><td>

1.  Set sa\_analytics.rca\_use \_legacy\_query to true.
2.  Create a change request on a CI and leave it in a 'new' state.
3.  Create another change request on the same CI with an implementation date set to one week ago.
4.  Generate an alert on the same CI.
5.  Verify the Probable Root Cause list.

 Expected behavior: Both CRs should be filtered out \(one for being in 'new' state, one for being outdated\).

 Actual behavior: Both CRs appear in the PRC list.

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

GRC Platform Plugins

 PRB1972072

</td><td>

The P95 response time for task page loading across all the workspaces exceeds SLA of 4 seconds

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Navigate to Risk/Audit/Compliance/ESG/Privacy WS.
3.  Select **Task Page Widget**.

 Observe that the P95 response time exceeds SLA of 4 seconds.

</td></tr><tr><td>

Horizon Image Component

 PRB1803287

</td><td>

The 'Fit' property doesn't work with max-width attribute

</td><td>

The now-image tag calculates to new resize events, but the 'img' tag remains the full width despite the values is in the 'Fit' property.

</td><td>

1.  Open a UI Builder page.
2.  Place a carousel component.
3.  Add 2 to 3 now-images components with some default photos within the carousel content slot.
4.  Navigate to**Navigation and interaction** &gt; **Carousel configuration**.
5.  Set 'Number of items in view' to 'Single content item'.
6.  Attempt to resize the window.

 Observe that the now-image tag has max-width dynamically calculated to new values on resize events, but the 'img' tag inside now-image still keeps the full width despite the options specified in now-image's 'Fit' property.

</td></tr><tr><td>

HTTP Client

 PRB1959206

</td><td>

Introduce Mechanism to Set Connection Pool Timeout on the Instance to Prevent Semaphore Exhaustion

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Install Base Management Store

 PRB1972327

</td><td>

Instance Performance issue due to No NULL checks in the InstallBaseUtilSNC base instance script include

</td><td>

'sn\_customerservice .unified\_consumer role' was added to a group, causing a cascading change to 27 child groups containing over 7000 users. Subsequently, users with this new role who didn't have a corresponding entry in the consumer table were caused to run a 'select \*' query on 'sn\_install\_base' tables. This results in queries of tables containing over 2 million records being continuously executed.

</td><td>

1.  Open a base instance.
2.  Try to assign 'sn\_customerservice .unified\_consumer role' to a high number of users \(or any group with a lot of members\).
3.  Try to open any case as any user from the above list.

 Observe the slowness. Global.CSManagementUtils.getConsumerID\(\) returns null for a user who doesn't have a record in csm\_consumer table and has a unified\_consumer role. This method is used in other methods, which are used in dynamic filters.

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

 PRB1912273

</td><td>

After a Yokohama upgrade, catalog admins can't create new sys\_translated records

</td><td>

Since the upgrade to Yokohama, it's no longer possible for catalog\_admin users to create records in table \[sys\_translated\], only update existing ones.

</td><td>

1.  Provision a Yokohama base instance with a language plugin installed.
2.  Create a testuser with the role catalog\_admin to access the catalog items and their variable sets and variables \(but not the sys\_translated table directly\).
3.  As sys\_admin, create two variables for any catalog item.
4.  Add a translation for one of the two variables.
5.  Switch to testuser.
6.  Open the catalog item.
7.  Change the preferred language to the one associated with the plugin \(make sure that the translation exists\).
8.  Change the English value to a translation for the variable that wasn't translated yet.
9.  As sys\_admin, check on the sys\_translated table directly.

Observe that the change is instantly reverted after trying to save it and isn't saved.

10. As testuster, adjust the existing translation of the variable question text for the translation that already exists.

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

Language and Translations

 PRB1978639

</td><td>

Translations merge for Yokohama to fix an issue introduced in a previous patch

</td><td>

This is a GenAI translation update.

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

 PRB1975305

</td><td>

AI Engagement Experience \(AIEX\) upgrade issue

</td><td>

When a user upgrade Yokohama, they won't get any of the new AIEL changes. This occurs when upgrading from version 27.0.29, which has UXR components, to version 27.0.28-aiex.13.

</td><td>

 

</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

 PRB1951872

</td><td>

The user resolution rule is created in a global domain instead specific domain

</td><td>

The user resolution rule is created in the global domain instead of the child domain 'A1'.

</td><td>

1.  Created a parent domain 'A'.
2.  Create child domains 'A1' and 'A2'.
3.  Create an integration profile in domain A1.
4.  Create a custom field as **Work Email** in the sys\_user table in domain A1.
5.  Run the scheduled job to pull the subscriptions in domain A1.

Notice that the user resolution rule creation schedule job is triggered, and rule is getting created.


 Expected behavior: The user resolution rule is created in domain A1.

 Actual behavior: The user resolution rule is created in the global domain.

</td></tr><tr><td>

Now Assist Panel

 PRB1985088

</td><td>

Link in NASS doesn't open in a new tab

</td><td>

 

</td><td>

1.  Navigate to full page.
2.  Search 'What is spam?'.
3.  Select the source link for the KB.

 Expected behavior: The KB link opens in a new tab.

 Actual behavior: The KB link doesn't open at all.

</td></tr><tr><td>

On-Call Scheduling

 PRB1909337

</td><td>

No response after selecting **On-Call Calendar** if there's no shift in cmn\_rota

</td><td>

When the user tries to select **On-Call Calendar**, there's no response and no message, but a green border is displayed for an unknown reason. It seems related to the presence or absence of shift\(cmn\_rota\). Instead, the system should display a meaningful message on the page when no shifts are available.

</td><td>

1.  Execute cmn\_rota.list.
2.  Confirm that there are no records.
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

 PRB1971589

</td><td>

cypher2Results API is broken with glide record dynamic

</td><td>

A Null Pointer Exception is coming from OneExtend: 'Couldn't decipher the stack trace resulting from the following JavaScriptException.'

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1973586

</td><td>

A newly changed LLM provider setting is reset after upgrading

</td><td>

After upgrading an instance to Zurich but not upgrading Generative AI Controller and Now Assist Admin apps to the compatible latest available versions, the LLM provider setting reverts to its pre-upgrade value within two hours or less after being changed through the 'Edit Model Provider' option in Now Assist Admin. This behavior may cause configuration instability after the upgrade.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1974084

</td><td>

Error during zboot due to a 'where' clause on sys\_db\_view\_table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1978709

</td><td>

Now Assist panel and AI Agents fail because outbound URLs ignore the project ID of the connection URL \(sys\_alias\)

</td><td>

In the Gemini BYOK integration, outbound requests made by Now Assist panel and AI Agents fail because the generated outbound URLs don't include the project ID from the connection URL \(sys\_alias\). These features rely on the Java proxy to construct outbound URLs, but the proxy doesn't append the project ID. As a result, calls are sent to an incorrect or incomplete Gemini endpoint, and the user gets the error 'Invalid HTTP response 404: Not Found'. In contrast, Incident Summarization and Code Generation features work correctly because they use the Flow Designer, which properly constructs outbound URLs and includes the project ID as part of the request path. Because Now Assist panel and AI Agents bypass Flow Designer and instead use the Java proxy that omits the project ID, their outbound calls fail consistently.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1981515

</td><td>

Add enhanced debug logging around async client call

</td><td>

Debug logs need to be added when each streamed chunk is received, when the final callback is received \(VAStreamConsumer\), before enqueueing in the hybrid queue, and after enqueueing in the hybrid queue and the callback is complete.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1797363

</td><td>

Scheduled reports are migrated even if they aren't active

</td><td>

 

</td><td>

1.  On track/dataanalytics, change the 'com.glide.par.unified\_analytics.enabled' property to false to trigger migration.
2.  Open a report.
3.  Schedule a report.
4.  Open the scheduled report.
5.  Set the active field to false so the scheduled report isn't sent automatically.
6.  Run migration from the migration center.
7.  After migration is complete, activate migration.
8.  Navigate to the 'Scheduled Export' library.

 Expected behavior: The scheduled report isn't migrated.

 Actual behavior: The inactive scheduled job is migrated as active.

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

 Observe that duplicate records are created in the analytics\_category\_m2m table.

</td></tr><tr><td>

Platform Licensing

 PRB1980200

</td><td>

True-up of SM and LE 6.0.2

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1916916

</td><td>

When datetime is selected as Activity Definition, the grouping of activities isn't working

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1949520

</td><td>

Users aren't able to view processes if they have access to only some of the records from that table

</td><td>

 

</td><td>

1.  Impersonate abel.tuter.
2.  Open the 'Process config' list from Process Mining Workspace.
3.  Select the **wrench** icon on the sidebar.
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

Procurement

 PRB1970134

</td><td>

'Receive by' isn't populated when receiving through the stockroom import flow

</td><td>

In a normal PO flow, 'Received by' is populated by the user who received the assets. However, in the import flow, it's shown as empty.

</td><td>

1.  Log in to the instance.
2.  Create a purchase order.
3.  Create a purchase order line with Apple Mac, with quantity set to 3.
4.  Open the stockroom page.
5.  Complete the import flow for the above POL.
6.  Provide the details for 3 assets.
7.  Select **Receive**.

 Observe that 'Receive by' isn't populated on the receiving slip.

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

Server-side scripts

 PRB1974676

</td><td>

Guest sandbox logging can potentially overwhelm system logs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1974683

</td><td>

Rules for static analysis feature are locked behind no\_db\_override

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB1982503

</td><td>

In Yokohama, the **Continue** button doesn't work and the **Preview** button is missing in the canvas view of t2c- 6.0.7

</td><td>

 

</td><td>

1.  Open a Yokohama instance with NAFC 27.6.1.
2.  Enable the T2C skill.
3.  Navigate to Catalog Builder.
4.  Select **Build with Now Assist**.
5.  Enter any utterance.

 Observe that the **Preview** button is missing and the **Continue** button doesn't work.

</td></tr><tr><td>

Service Portal

 PRB1935624

</td><td>

**Hide filters** and **Clear All** in a facet search aren't properly aligned

</td><td>

The **Hide filters** and **Clear All** options are showing, but they aren't aligned. There are a few pixel mismatches.

</td><td>

1.  Search for something in ESC portal.

Observe the facets on the right side.

2.  Choose one of the sources so **Clear All** shows up.

 Expected behavior: The **Hide filters** and **Clear All** options are aligned.

 Actual behavior: The **Hide filters** and **Clear All** options are showing, but they aren't aligned. There are a few pixel mismatches.

</td></tr><tr><td>

Software Asset Management

 PRB1968916

</td><td>

Fetch transactionId by failed job name and profile Sys ID

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1974875

</td><td>

Job failure troubleshooting for family releases

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Publisher Pack for Microsoft

 PRB1871730

</td><td>

The 'Collect CAL Info' extension section causes a huge payload for Windows discovery

</td><td>

When running Windows OS - Servers patterns, if the server has a large amount of records in the MsftUal\_DeviceAccess and MsftUal\_UserAccess through WMI queries, then the payload is substantial. Such large payloads may cause mutex locks and impact performance.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Publisher Pack for SAP

 PRB1887429

</td><td>

Automatic software model isn't created

</td><td>

An automatic software model isn't created for the Default Named User Type in the Default Price List as specified in the SAP connection.

</td><td>

1.  Set the 'com.snc.samp.automaticsmrcreation' system property to true.
2.  Create a SAP Connection and SAP Client.
3.  Create different types of SAP System Users.
4.  Verify that the discovered user records were created.
5.  Run recon.
6.  Verify that only SAP system users of user type 'Dialog' are reconciled.

 Observe that an automatic software model isn't created for the Default Named User Type in the Default Price List as specified in the SAP connection.

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

The total cost displayed for software entitlements in the Software Asset Workspace \(SOW\) view is incorrect when compared to the form view of the same entitlement. The SOW is adding additional decimals on some occasions, which isn't consistent with the form view, which would have a rounded number. For example, Workspace: 10,441.5591 compared to Form: 10,440. This issue arises from the different outputs of the UI scripts CalculateTotalCostWS .getTimeSpan\(\) and CalculateTotalCost .getTimeSpan\(\), which should, but doesn't yield consistent results. This issue impacts the visibility of accurate cost information in software asset workspace.

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

UI Field Administration

 PRB1881510

</td><td>

The category under 'change request values' on the standard change template isn't reflected in Service Operations Workspace

</td><td>

This issue is present in the base instance as well. The **Category** field is visible, but the value set for the category isn't visible under 'change template values'.

</td><td>

1.  In the application navigator, navigate to **Change** &gt; **Standard Change** &gt; **My Proposals** &gt; **New**.
2.  Create a new template with the change request values filled in.
3.  Request approval.
4.  In Service Operations Workspace, navigate to **List** &gt; **Tasks** &gt; **Assigned to you** \(remove the filter if required\).
5.  Open the standard change template.

 Observe that the category under 'change request values' isn't reflected.

</td></tr><tr><td>

UI Field Administration

 PRB1937530

</td><td>

Reference fields do not display correctly

</td><td>

When creating an incident using the **Create Incident** UI Action from a record page that uses UI Builder form components, reference fields may not display correctly.

</td><td>

1.  Navigate to Service operations workspace.
2.  Select the **plus** icon.

Notice that the interaction form page appears.

3.  Populate the below fields in the interaction form.
    1.  Caller: Select any caller.
    2.  Configuration item: Select any CI.
    3.  Service: Select any service.
4.  Select **Save**.
5.  In the interaction form view, populate the **Short description** field.
6.  Select **Create incident**.

 Notice in the incident workspace view under the assignment section that the **Configuration item** field and **Service** field are missing.

</td></tr><tr><td>

UI Field Administration

 PRB1945077

</td><td>

Click-to-call ignores the E.164 country code and defaults to +1

</td><td>

The 'Click-to-call' feature is incorrectly dialing US numbers instead of international numbers like the UK or India, regardless of the country code. Dialing from the contact card works correctly, but using the **Click-to-call** icon always defaults to US numbers.

</td><td>

1.  Navigate to the CSM Workspace
2.  Open a Case record.
3.  Select the **Information** icon of the **Contact** field.

The User account will open.

4.  Select the **Phone** icon of the **Business phone** field.

 An outbound call is placed, and an interaction record is created.

</td></tr><tr><td>

UI Form Administration

 PRB1953177

</td><td>

now-stylized-text is not supported in Yokohama so the tagline component is not rendered in workspace

</td><td>

This issue occurs in Yokohama.

</td><td>

1.  Log in to a ynowassist instance with GenAI setup.
2.  Open UI Builder.
3.  Select any of the configuration workspaces \(example: CSM/SOW\).
4.  Open an SRP record page.
5.  Add a tagline component.
6.  Generate a record with a GenAI agent or attached background script.
7.  Open the same record in the configuration workspace.

 Expected behavior: The tagline component is displayed in the workspace.

 Actual behavior: The now-stylized-text isn't supported in Yokohama so the tagline component isn't rendered in the workspace.

</td></tr><tr><td>

Usage Analytics

 PRB1963094

</td><td>

Users aren't able to interact with the Unified Navigation menu when the web SDK configuration becomes empty

</td><td>

Unified Navigation Menu interaction is stopped when the legacyConfig in sessionStorage is emptied by some scripts, causing errors related to trackingConsent and page freezing upon interaction. This restores smooth navigation between menu items.

</td><td>

1.  Load the home page.
2.  Open 'Inspect' mode in the browser.
3.  Navigate to the 'Application' tab.
4.  Delete the session storage.
5.  Try to interact with Unified Nav or other section of the page.

 Check that there's an error for tracking consent and the page is freezing.

</td></tr><tr><td>

Virtual Agent

 PRB1768573

</td><td>

Profanity filter keyword issues

</td><td>

Profanity filter keyword mode flags non-profane words that contain otherwise profane words.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1975277

</td><td>

The actual status of the additional chat features isn't reflected in the base instance NAVA assistant test window

</td><td>

In the test panel, the values of 'Allow web search', 'Allow response streaming', and 'Allow document uploads' are shown as 'Inactive'. This doesn't reflect the values set in the 'sys\_now\_assist\_deployment \_config\_attributes' table.

</td><td>

1.  Navigate to **All** &gt; **Assistant Designer**.
2.  Ensure that you have active assistants 'Now Assist Panel - Platform \(default\)' and 'Now Assist in Virtual Agent \(default\)'.
3.  Navigate to the settings of 'Now Assist in Virtual Agent \(default\)'.
4.  In the 'Additional chat features' section, select the **Allow web search**, **Allow response streaming**, and **Allow document uploads** options.
5.  Save the assistant.
6.  Make sure the same options are selected for 'Now Assist Panel - Platform \(default\)'.
7.  Navigate to the table 'sys\_now\_assist\_deployment \_config\_attributes'.
8.  Search for 'doc\_qna', which is responsible for 'Allow document uploads'.
9.  Verify that it is set to 'true' for both assistants \(since it was selected in the earlier steps\).
10. In the same table, search for 'streaming\_enabled' and 'web\_search\_enabled'.
11. Verify that they're also set to 'true' for both assistants.
12. Navigate to **All** &gt; **Designer**.
13. From the 'Select assistant' drop-down list, select **Now Assist Panel - Platform \(default\) assistant**.
14. Select the **Test assistant** button.

Observe that the test panel opens, and the values of 'Allow web search', 'Allow response streaming', and 'Allow document uploads' are shown as 'Active'.

15. From the 'Select assistant' drop-down list, select **Now Assist in Virtual Agent \(default\) assistant**.
16. Select the **Test assistant** button.
17. Select one of the available chat options.

 Expected behavior: In the assistant test panel, the values of 'Allow web search', 'Allow response streaming', and 'Allow document uploads' are shown according to the actual values set in the 'sys\_now\_assist\_deployment \_config\_attributes' table.

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

 PRB1982735

</td><td>

Handle an unknown document\_id field in the sys\_cs\_provider\_application

</td><td>

 

</td><td>

1.  Set up Glide NLU or Now Assist.
2.  Set up the appropriate Teams version.
3.  Start a conversation from a bot.

 Logs have an unknown field document\_id in sys\_cs\_provider\_application exception for every Teams request.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1927910

</td><td>

When initiating a chat with Enhanced Chat active in a portal, the **+** button to start a new chat remains disabled after the chat times out

</td><td>

Users must refresh the page to re-enable the **+** button.

</td><td>

1.  Ensure that the Enhanced Chat bot is added to the portal by navigating to **Conversational Interfaces** &gt; **Assistants** &gt; **Now Assist in Virtual Agent** &gt; **Display Experience**.
2.  Confirm that the portal \(for example, Employee Center\) has Enhanced Chat enabled.
3.  Navigate to **Employee Service Center**.
4.  Initiate a chat session.

Observe that the **+** button for starting a new chat is disabled.

5.  Leave the chat open until the abandon timeout occurs, or manually trigger the timeout.

After timeout, observe that the **+** button remains disabled.


 Expected behavior: The **+** button is enabled after a chat times out, allowing users to start a new conversation without refreshing the page.

 Actual behavior: The **+** button remains disabled after timeout, and users must refresh the page to initiate a new chat.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1974007

</td><td>

Synthesized responses disappear on Now Assist Virtual Agent \(NAVA\), Now Assist panel, Dynamic Window \(DW\)

</td><td>

Responses disappear after they're produced.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1981024

</td><td>

Markdown link \[label\]\(url\) renders an incorrect URL when the URL contains a dollar sign \($\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Walk-Up Experience

 PRB1965546

</td><td>

In SOW, navigating to location kiosks doesn't return any results

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

Web UX Runtime

 PRB1968992

</td><td>

There's a blank page in the custom workspace when users log in for the first time, or after they clear the cache

</td><td>

This issue occurs after upgrading Yokohama. The user notices that the Verify Guided Upgrade take a while to load when it's the first time logging in to the instance.

</td><td>

1.  Navigate to **Admin Menu** &gt; **Upgrade Management**.
2.  Select **Get started** from the Overview page.

 Notice that the Verify Guided Upgrade takes a long time to load when it's the user's first time logging into the instance.

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

Zing Text Indexing and Search Engine

 PRB1972145

</td><td>

The query is slow from the TS Index Stats job from the getTableList method

</td><td>

The TS Index Stats job executes some code to get a list of extension tables to index for a given base table. To do this, it executes an expensive aggregate query against the base table, grouping by the **sys\_class\_name** field. This doesn't scale well and can cause queries to run long, which impacts overall database and instance performance.

</td><td>

1.  Navigate to a large CMDB or SYS\_IMPORT\_SET\_ROW table.
2.  Run the TS Index Stats job.

 Expected behavior: The job runs quickly.

 Actual behavior: The job runs slowly as these extended tables grow in size.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 11](yokohama-patch-11.md)
-   [Yokohama Patch 10 Hotfix 1a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2711334)
-   [Yokohama Patch 10 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2695212)
-   [Yokohama Patch 10](yokohama-patch-10.md)
-   [Yokohama Patch 9](yokohama-patch-9.md)
-   [Yokohama Patch 8](yokohama-patch-8.md)
-   [Yokohama Patch 7 Hotfix 3b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2693894)
-   [Yokohama Patch 7](yokohama-patch-7.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


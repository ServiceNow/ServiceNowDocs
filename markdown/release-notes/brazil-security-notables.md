---
title: Brazil security and notable fixes
description: The Brazil release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/brazil-security-notables.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 106
breadcrumb: [Available patches and hotfixes, Learn about the Brazil release, Brazil release notes]
---

# Brazil security and notable fixes

The Brazil release contains important problem fixes.

-   **Brazil was released on September 24, 2026.**
    -   09-22-2026\_1636
    -   glide-brazil-08-25-2026\_\_patch0-08-26-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This version is being evaluated for use in the ServiceNow Government Community Cloud \(GCC\) environment.

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/brazil/rn/patches/PRBs-B00.00.xlsx).

## Security-related fixes

Brazil includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Brazil, refer to .

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

Access Analysis Instrumentation API

 PRB1984283

</td><td>

Analyze Access in any record's hamburger menu isn't working

</td><td>

Adding 'access-management' into the URL doesn't work either; it navigates to Access Analyzer's 'Analyze Permissions'.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1981898

</td><td>

Need properties for better control of the scope where a security attribute script gets evaluated

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1971849

</td><td>

The acronym 'AI' needs to be localized in some target languages

</td><td>

This issue was observed in instances using the languages Spanish, Portuguese Brazilian, or French.

</td><td>

1.  Switch the instance language to either Spanish, Portuguese Brazilian, or French.
2.  Navigate to the **Hardware Asset Workspace**.
3.  Open the Hardware Asset Workspace Overview.
4.  Select **Asset requests** under the 'Quick links' section.
5.  Open any Requested Item.

 Expected behavior: The acronym 'AI' should be localized in the target languages Spanish, Brazilian Portuguese, and French. This should also apply to the backend form of the Requested Item's 'Detailed Issue' description.

 Actual behavior: Observe that the 'AI' acronym still appears as 'AI' instead of 'IA'.

</td></tr><tr><td>

Activity Stream

 PRB1991852

</td><td>

Base64 coded attachments can't be loaded in the activity stream in the workspace

</td><td>

This likely has to do with processing large content.

</td><td>

1.  Navigate to any record page.
2.  Create an email with a base64 encoded image.
3.  Set the email to 'sent' status.
4.  Navigate to the record and select **Show more** for the email.

 Expected behavior: The full body of the email is displayed.

 Actual behavior: The email is loading for a long time and eventually crashes the page.

</td></tr><tr><td>

Activity Stream

 PRB2011631

 [KB2974503](https://hi.service-now.com/kb_view.do?sysparm_article=KB2974503)

</td><td>

The 'Additional comments' left side black indicator bar disappears after a page refresh

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB2016617

</td><td>

Unguarded Jelly expression in form.xml causes RhinoEcmaError warnings on every classic form load

</td><td>

On any classic UI16 form load, the platform Jelly template evaluator throws a RhinoEcmaError warning in the system log. The warning is present on every classic form, regardless of application scope or record type. There is no functional outage; forms load and save correctly, and all transactions return HTTP 200 with normal response times. The main impact is high-volume system log noise.

</td><td>

1.  Log in to a Zurich instance.
2.  Open any classic UI16 form record without a sysparam\_citation query parameter in the URL.
    -   Example without activity stream: Navigate to /sys\_dictionary.do and open any record.
    -   Example with activity stream: Navigate to /incident.do and open any record.
3.  After the form loads, open the system log.

 Expected behavior: No RhinoEcmaError warnings are generated during a standard form load.

 Actual behavior: On forms without an activity stream, one warning entry is generated per form load. On forms with an activity stream, two warning entries are generated per form load.

</td></tr><tr><td>

Activity Stream

 PRB2018914

</td><td>

In an activity stream, video controls become unusable after selecting an attached video

</td><td>

After a video file is uploaded as an attachment to a record and the page is refreshed, the video renders inside the activity stream with native HTML5 video controls \(play/pause, scrubber, volume, fullscreen\). However, on selecting the video element, the controls disappear and become unusable, preventing the user from playing back, scrubbing, or otherwise interacting with the video.

</td><td>

1.  Log in to a ServiceNow instance.
2.  Open any task record that supports an activity stream and an **Attachments** field.
3.  Attach a video file to the record.
4.  Save the record.
5.  Refresh the page so the attached video renders inside the activity stream.
6.  In the activity stream, locate the entry containing the attached video.

The video element appears with native video controls \(play/pause, scrubber, volume, fullscreen\).

7.  Select the video element in the activity stream to attempt playback or interact with the controls.

 Expected behavior: The native video controls remain visible and interactive; the user can play, pause, scrub, adjust volume, and enter fullscreen.

 Actual behavior: On selection, the video controls disappear and become unusable. The video element renders but no playback controls can be interacted with.

</td></tr><tr><td>

Activity Stream

 PRB2032224

</td><td>

**Orphaned Dependent** fields in the initial audit event causes an exception in SysAuditRule

</td><td>

When the support audit is passed to findFirst, which filters out support audits, it finds an empty stream and throws 'IllegalStateException: Unreachable code reached.' The exception is caught, but it causes retrieveEvents to return zero events, leaving the workspace activity stream completely empty.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2066570

</td><td>

Activity stream primary journal field ordering regression — work\_notes displayed before comments in UI16 and Service Portal

</td><td>

The activity stream on task records \(Incidents, Changes, etc.\) incorrectly defaults to the 'Work Notes' input instead of 'Comments' in both the platform UI and Service Portal. This affects user workflow as agents may inadvertently post internal work notes when intending to post customer-visible comments. Additionally, custom journal fields configured on tables do not appear in the Service Portal activity stream widget.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1969415

</td><td>

Javascript Error Logs on Advanced Work Assignment despite AWA not being in use

</td><td>

In sysevent\_​script\_​action\_​5054795a9f946210c89656effa0a1cda,​ if the user is not found in the instance, an error is thrown.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1683554

</td><td>

Conversation tab doesn't show up during an outbound call from Amazon Connect

</td><td>

The interaction pops open in agent workspace, but the conversation tab doesn't show. It only shows up on refresh or reload of the page.

</td><td>

1.  Make an outbound call from the agent workspace using the Amazon Connect.
2.  Select the **Set Up Real Time Transcription** checkbox in the instance setup step.

 Observe that the interaction pops open in agent workspace, but the conversation tab does not show. It only shows up on refresh or reload of the page.

</td></tr><tr><td>

Agent Chat

 PRB1928570

</td><td>

The Service Operation Workspace chat window malfunctions after dragging and dropping an image

</td><td>

The Service Operation Workspace chat window gets stuck after dragging and dropping an image from the chat window to the attachment section of the incident.

</td><td>

1.  Impersonate an agent and navigate to SOW and set state as available.
2.  In other browser intiate a chat.
3.  Once the chat is accepted from the agent side the interaction opens with chat window.
4.  Add an image in the chat window.
5.  Create an incident from the interaction using create incident.
6.  Drag the image from chat window to the add attachements on the incident.

 Notice that the Service Operation Workspace chat window gets stuck.

</td></tr><tr><td>

Agent Chat

 PRB2014178

</td><td>

Optimize the request to fetch previous interactions for a requester to show conversation history in Agent chat

</td><td>

If there are no custom filters, there is no need to create the list of interaction records by going through all the returned records from the DB query.

</td><td>

1.  Enable the 'Conversation history' feature in Agent chat settings.
2.  Set the limit to 10.
3.  Ensure that there's a large number of closed interactions \(more than 100\) for Abel Tuter.
4.  Check the server memory in /stats.do.
5.  Start a new conversation as Abel Tuter.
6.  Accept the work item as Beth Anglin.
7.  Ensure that the history shows in the agent chat.
8.  Check the server memory again in /stats.do.

 Observe that the server memory has gone up significantly.

</td></tr><tr><td>

Agent Chat

 PRB2030144

 [KB3133990](https://hi.service-now.com/kb_view.do?sysparm_article=KB3133990)

</td><td>

When a work item is in the queue but not yet accepted, the user can't update string fields on the open record

</td><td>

In the workspace, when a work item is in the queue but not yet accepted, the user is unable to update string fields on the open record. With these two circumstances satisfied, a focus-stealing issue occurs, where the blinking cursor is removed after a moment.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Agile Development

 PRB2026219

</td><td>

The **Group capacity** field is read only in sprint records

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Navigate to the table 'rm\_sprint.list'.
3.  Open any sprint record.

 Note that **Group capacity** \(points\) is read-only.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1994390

</td><td>

After a Zurich upgrade, hundreds of thousands of log entries are generated by CacheInvalidationEventHandler

</td><td>

The message is 'No endpoints available for cache invalidation'. The source is com.​glide.​ui.​Servlet​Error​Listener.​

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2025974

</td><td>

A user session is logged out when opening AI-generated interaction records

</td><td>

The user session is logged out when opening AI-generated interaction records that were created/updated by the incident\_intelligence\_agent. The interaction record remains in the work in progress state, even though the associated conversation has been marked as faulted. The issue is specific to the in Service Operations Workspace view, as opening the same record in platform view works without issue.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1913117

</td><td>

Searcingh on a reference field with an ACL on a reference table doesn't work even with dot\_walk\_field mapping

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search for Service Portal

 PRB2038055

 [KB3139447](https://hi.service-now.com/kb_view.do?sysparm_article=KB3139447)

</td><td>

The Now Assist Self Service widget breaks the full page experience search in portal

</td><td>

After upgrading to Zurich, when the user searches from the Employee Center portal, the full page experience fails and no results are displayed. Instead, the widget throws a server-side JavaScript error: '$sp is not defined'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search UX

 PRB1993482

</td><td>

Global Search is logging the error '\*\*\* Script: No EVAM Definition ID provided as input to Build Genius Result Templates transform.: no thrown error'

</td><td>

A 1000+ error is observed in the console and the syslog error occurs, '\*\*\* Script: No EVAM Definition ID provided as input to Build Genius Result Templates transform.: no thrown error.'.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2039564

 [KB3118078](https://hi.service-now.com/kb_view.do?sysparm_article=KB3118078)

</td><td>

Error while accessing catalog items from search after Australia upgrade

</td><td>

After upgrading to Australia, the typeahead widget for suggested results fails.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Analytics Data API

 PRB1844011

</td><td>

Using 'Trend by week' leads to an incorrect record count when the new year starts

</td><td>

When using 'Trend by' with the options 'Opened', 'Calendar', 'Standard Calendar' and 'per-week' and running the report, the record count is 3 but the List view record count is 5.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1973007

</td><td>

The Platform Analytics 'pivot table' unit type doesn't persist

</td><td>

When creating a pivot table using two tables as the data sources, the 2nd and 3rd columns swap their values.

</td><td>

1.  Create a pivot table visualization within a dashboard.
2.  Add in two tables as data sources.
3.  Create four columns on the pivot table, with the first two column being a count of each respective table and the last two columns a sum of all the values with other columns.
4.  Save the visualization.
5.  Exit editing mode.
6.  Refresh the dashboard.

 When the order of the columns is the count of table 1, count of table 2, sum of table 1's column, sum of table 2's column, and when users refresh the dashboard, the 2nd and 3rd columns values swap, with the values from column 3 appearing in column 2 and vice versa.

</td></tr><tr><td>

Analytics Data API

 PRB1974037

</td><td>

Platform Analytics - Visualization displays outddated dates when 'Use current date for period end' is selected

</td><td>

Even when the 'Use current date for period end' is selected on a time series visualization, the graph still displays older dates and not the latest dates.

</td><td>

1.  Create a time series visualization with an indicator \(daily frequency\) as a data source.
2.  Ensure that scores are collected for this indicator.
3.  In the configuration, under the date range section, select the **Set absolute period** and **Use current date for period end** options.
4.  Review the visualization on different days.

 Expected behavior: The visualization graph should consider the current date as the period end date and generate the graph.

 Actual behavior: The visualization graph is still generated with the older dates \(when the visualization is created\) as the period end date.

</td></tr><tr><td>

Analytics Data API

 PRB1986630

</td><td>

Domain isn't included while generating a key for the indicator data source

</td><td>

Visualizations that use the Analytics Cache currently omit the global key when generating cache entries. As a result, a visualization may behave inconsistently across domains, depending on which domain created the cache entry first.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2000611

</td><td>

Pivot tables for data visualizations cannot handle enough records to produce top ten charts, so the charts return no records in the Search Analyzer for Now Assist Analytics \(Performance\)

</td><td>

The error message reads, 'Unable to generate chart, maximum number of data points exceeded this visualization'.

</td><td>

1.  Navigate to Now Assist Admin module.
2.  Select the Performance tab.
3.  Select the User Search Analyzer.

 Observe that the two top charts do not have any data loaded in them.

</td></tr><tr><td>

Analytics Data API

 PRB2001019

</td><td>

Accept 'group by' selection for all variable types

</td><td>

When comparing to classic reporting, many variable types are not available for selection in the 'group by' component in the Platform Analytics visualizations.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2003111

</td><td>

Pivot table using multiple data sources shows 'No data' on the widget when one of the data sources returns no data

</td><td>

Even though data is available, the chart shows 'No data available'.

</td><td>

1.  Provision an instance with the com.snc.itsm\_pa.demo plugin installed to have more test data.
2.  Open the list with records of the problem table \(problem.LIST\).
3.  Filter records by Assigned to = Abel Tuter and State = Assess so that two records appear.
4.  Remove one of the records.
5.  Move the other record to the Fix in Progress state by selecting the **Fix** button.
6.  Navigate to **All** &gt; **Library** &gt; **Data visualizations**.
7.  Select **New**.
8.  Select **Visualization type: Pivot table**.
9.  Specify the following data sources:
    -   Incident table with the conditions Assigned to = Abel Tuter and State in \(New, On Hold, Resolved\).
    -   Problem table with the conditions Assigned to = Abel Tuter and State in \(New, Fix in Progress, Assess\).
10. Specify group by's:
    -   Columns: Assign to; Show all; Individual metric.
    -   Rows: State.
11. Set 'Show row total' and 'Show column total' to false.
12. Check the chart.

Observe that the chart renders and shows expected data.

13. Open the list with records of the problem table \(problem.LIST\).
14. Filter records by Assigned to = Abel Tuter and State = Fix in Progress so that one record appears.
15. Open that record.
16. Change the status to Re-Analyze.
17. Refresh the chart.

 Expected behavior: The chart is rendered and shows the expected data with zeros.

 Actual behavior: The chart shows 'No data available', despite data being available.

</td></tr><tr><td>

Analytics Export API

 PRB1987970

</td><td>

PDF Export of Inline Dashboard gives a blank page with Loading word in it

</td><td>

Export PDF for any of the Inline dashboards is blank and shows the loading symbol only in the PDF and not the actual report of the dashboard. Also, Exporting a Dashboard stays in the 'Export request in progress' state for a very long time even on a very simple one widget dashboard.

</td><td>

 

</td></tr><tr><td>

Analytics Export API

 PRB1995410

 [KB2810683](https://hi.service-now.com/kb_view.do?sysparm_article=KB2810683)

</td><td>

On demand list visualization export to .xlsx

</td><td>

An issue has been identified where on‑demand exports of list data visualizations intended for XLSX format are instead exported as XLS files in the Zurich environment. This behavior differs from the Yokohama environment, which previously exported successfully in XLSX format.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Analytics Export API

 PRB2007025

</td><td>

Dashboard PDF export doesn't apply dashboard filters on the list

</td><td>

Dashboard filters aren't applied to the list in the dashboard PDF exports. Only the filters configured in the list are honored.

</td><td>

1.  Export a dashboard to PDF with list visualization.
2.  Make sure the dashboard has dashboard filters and the list is following the filters.

 Observe that the filters are applied correctly on the dashboard to the list, but they aren't applied in the exported PDF.

</td></tr><tr><td>

Application Manager

 PRB1889269

</td><td>

Progress worker state isn't set to complete after worker is finished

</td><td>

Installing plugins shows an error even when successfully completed. In the logs, it looks like the error comes from a script include. Previously, the code block was a part of a larger function that had appVersion and appID as parameters. The code was refactored into the forceSyncWithStore function, which doesn't have appVersion and appID as parameters. If the gs.info line is reached, it throws an error because those two fields were not passed into the function.

</td><td>

1.  Install the custom scoped app \(for example, x\_conym\_atf\_sc\_req, x\_conym\_hrp\).
2.  Check 'sys\_upgrade\_history' to confirm the installation is marked as 'complete'.
3.  Check 'sys\_progress\_worker' list for the message 'Progress worker state is not set to complete after worker is finished.'
4.  Check 'syslog' for the error 'com.​glide.​script.​Rhino​Ecma​Error:​ 'appVersion' is not defined.'.

</td></tr><tr><td>

Application Manager

 PRB1971605

</td><td>

The base version is greyed out in the new Application Manager

</td><td>

The base version is greyed out in the new Application Manager, which stops to install the custom version created on the base version 1.0.0. The new Application Manager allows to install the custom version only on the latest version.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1971790

 [KB2827137](https://hi.service-now.com/kb_view.do?sysparm_article=KB2827137)

</td><td>

The size of the cache string is over 33.55MB, the GAAA response is too large to save as attachment

</td><td>

Post-release of killing entitlements, the large get\_all\_available\_apps \(GAAA\) response is breaking the checkAvailableUpdates call in the UpdateChecker. Until the get\_all\_available\_apps response size is reduced below the ~32MiB limit, the App Manager will continue to have cache issues.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1980407

 [KB2715943](https://hi.service-now.com/kb_view.do?sysparm_article=KB2715943)

</td><td>

In Application Manager, version details for intermediate versions don't refresh and are stuck loading

</td><td>

In Zurich instances, Application Manager fails to display version details when selecting any middle version between the installed and latest version for an app/plugin. The main details panel either shows no data or remains stuck loading and doesn't refresh.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1981044

 [KB2719949](https://hi.service-now.com/kb_view.do?sysparm_article=KB2719949)

</td><td>

The latest version in the sys\_store\_app table is updated to the installed version after an install, thereby causing the **Upgrade** button to be unavailable in App Manager

</td><td>

Two functions \(\_​fix​Latest​Version​For​Withdrawn​Installed​Apps,​ \_​fix​Latest​Version​For​Withdrawn​Installed​Customizations\)​ in Application Manager's Update​Checker.​check​Available​Updates API \(aka Sync in the UI\) were missing a required GlideRecord.addQuery constraint when the 'sn\_​appclient.​enable\_​app\_​manager\_​checksums\_​cache' sys\_property was set to true \(default\). This issue led to the latest\_version being set to the incorrect values on Install/Sync.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1988027

</td><td>

Application Manager fails to load Connected Workplace app info page with 'App info not found' error

</td><td>

In the Application Manager, the Connected Workplace app fails to load its information page when accessed from the Updates tab. The page spins for several minutes and then displays 'App info not found / Record not found', preventing the user from updating the app via the UI.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1992835

 [KB2804238](https://hi.service-now.com/kb_view.do?sysparm_article=KB2804238)

</td><td>

A deprecated Classic App Manager URL causes issues on some instances

</td><td>

Users have access to the Classic App Manager by navigating to the URI '/$allappsmgmt.do'. When they switched to new app manager later, and load the 'My company applications' page, that can corrupt the App Manager checksum cache, which causes the manual sync to fail.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB2057729

 [KB3140027](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140027)

</td><td>

Users can't publish custom-scoped applications after upgrading to Zurich or Australia

</td><td>

After upgrading to Zurich or Australia, there's an issue that prevents new application versions from being published for custom scoped apps in ServiceNow Studio. Selecting the **Publish** button for any custom application results in a publish failure with one of the following errors: 'Vendor information was not found, upload function is disabled for this instance' or 'Did not receive publishing information successfully. Cannot read properties of undefined \(reading 'toString'\)'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Navigator

 PRB2041444

 [KB3140871](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140871)

</td><td>

Tooltips persist and fail to dismiss on Chromium v149+ browsers

</td><td>

For users on UI16, there are recent updates to Chromium \(specifically version 149.x\) that trigger performance issues in UI16. This causes tooltips to remain stuck on the screen after a user hovers their cursor then moves away from elements. The tooltips should disappear once the user moves the cursor off the element.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Rationalization

 PRB1993865

</td><td>

Base instance business rule fails to exclude the current record during duplicate name validation due to incorrect property reference

</td><td>

The business rule on the cmdb\_ci\_business\_app table incorrectly blocks updates when changing the case of a Business Application name \(for example, 'abc' to 'ABC'\). This happens because it uses current.sysId instead of current.sys\_id, resulting in an undefined sys\_id comparison.

</td><td>

1.  Create a Business Application \(cmdb\_ci\_business\_app\) with the name 'abc'.
2.  Edit the same Business Application and change the name to 'ABC' \(only change the case\).
3.  Attempt to save the record.

 Expected behavior: The save is allowed because it's the same record, just with a different case.

 Actual behavior: The save is blocked with the error: 'A Business Application exists with the same name. Please verify.'.

</td></tr><tr><td>

App Shells

 PRB2005043

</td><td>

Some items are hidden behind the company logo in the Next Experience navigation bar

</td><td>

Sometimes the Next Experience navigation isn't rendered correctly. The 'All' and 'Favorites' items are displayed behind the ServiceNow logo. The issue is happening is randomly for some tests and does not have a fixed reproducible behavior. The menu items should always be rendered correctly and must be clickable.

</td><td>

 

</td></tr><tr><td>

Attachments to Records

 PRB2018059

</td><td>

GlideSysAttachment. writeContentStream\(\) fails in the Scripted REST API in Australia

</td><td>

GlideSysAttachment\(\). writeContentStream\(\) fails with 'Can't find method com.glide.ui. SysAttachment. writeContentStream \(object,string,string,com. glide.communications. GlideScriptableInputStream\)' when called from a Scripted REST API in the Australia release. The issue is not present in Zurich.

</td><td>

 

</td></tr><tr><td>

Audit History

 PRB2019035

</td><td>

The sysID of sn\_nowassist\_skill\_config is displayed in the username of the work notes

</td><td>

This issue is observed only in Workspace. In UI16, it's working fine.

</td><td>

1.  Make a GenAI Skill call.
2.  After the GenAI Skill call, update any record.

 Observe that the sysID of sn\_nowassist\_skill\_config is displayed in the username of the work notes, but it shouldn't be.

</td></tr><tr><td>

Authentication Factors

 PRB2006510

</td><td>

The 'Soft Pin Enrollment' option \(on the left panel menu and profile page\) shouldn't appear for all users by default

</td><td>

The 'Soft Pin Enroll' page is accessible by all users, with no role requirement. However, it should be displayed when AI Voice Agents are installed and controlled by a property.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1900411

</td><td>

Login page performance lag on Chrome browser \(Windows laptop\)

</td><td>

Performance lag on the new login page on a Windows laptop using the Chrome browser.

</td><td>

1.  Use a Windows laptop.
2.  Open Chrome browser \(137.0.7151.56 \(Official Build\) \(64-bit\)\).
3.  Navigate to the login page.

 Observe the lag in rendering or responsiveness compared to Microsoft Edge browser on the same machine, or a previous version \(Zurich\) vs current version \(Xanadu\).

</td></tr><tr><td>

Authentication

 PRB1969882

 [KB2718536](https://hi.service-now.com/kb_view.do?sysparm_article=KB2718536)

</td><td>

Login screen performance issues on iOS 26.2 RC and in Zurich instances

</td><td>

After upgrading to iOS 26.2, users are unable to log in to any instance using the Now Mobile app. The login page is extremely slow or unresponsive, and it can fail to load or accept credentials. The issue affects multiple users and device models. It's reproducible across different instances, and it also impacts the Agent app.

</td><td>

1.  On iOS, navigate to the Now Mobile app.

2.  Connect to a Zurich or later family release instance.


 Observe that the screen loads slowly and is non-responsive.

</td></tr><tr><td>

Authentication

 PRB2029440

 [KB3071161](https://hi.service-now.com/kb_view.do?sysparm_article=KB3071161)

</td><td>

side\_door.do changes are introduced after an Australia upgrade

</td><td>

Some users reported that after upgrading to Australia, when SSO is enabled, the side\_door.do page no longer works to allow local logins. Previously, in Zurich, even with auto-redirect enabled, accessing /side\_door.do still allowed users to access the local login page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1997825

 [KB2806020](https://hi.service-now.com/kb_view.do?sysparm_article=KB2806020)

</td><td>

When the 'glide.​script.​block.​client.​globals' property is set to false, running an ATF test throws a client error with code coverage enabled

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2038798

</td><td>

Cannot read the properties of the undefined \(reading 'message'\) after upgrading to Australia

</td><td>

The sys\_​processor\_​0af16f2d5363101034d1ddeeff7b12b6.​xml redirects requests to a new UI page, but this new UI page introduced in the Australia release is not supported by ATF's 'Navigate to module' step because it is relying on the gsft\_main to load the g\_form on the page. This breaks the custom logic to get the g\_form on the page, and errors occur in the console.

</td><td>

 

</td></tr><tr><td>

Benchmarks

 PRB1989154

</td><td>

Benchmark​Client​Util.​construct​Payload fails to fetch data for Global-scope PA Scorecards

</td><td>

Running the background script shows that the PAScorecard.query\(\) does not return results for Global-scope indicators, causing constructPayload to fail. For benchmarked indicators that exist in the Global scope, the constructPayload method fails to fetch PAScorecard details and returns 'null'. Because the PAScorecard records are not retrieved, the Global-scope indicators are not included in the upload payload, and scores are not uploaded to the central instance. As a result, instances do not receive benchmark scores for these indicators.

</td><td>

 

</td></tr><tr><td>

Build Agent \(Glide\)

 PRB2002763

</td><td>

Build Agent \(BA\) freemium install is blocked to due to hosted plugin, due to which NAFC install is incomplete

</td><td>

The BA trial version fails to install due to the missing hosted plugin.

</td><td>

 

</td></tr><tr><td>

Cache

 PRB1974175

</td><td>

Error messages appear in system logs when cache flush attempts to process records that have already been deleted

</td><td>

Error level messages are logged when the cache flush mechanism attempts to process records that no longer exist in the database. The error occurs in a race condition scenario where: A record is inserted into sys\_user\_grmember and a cache flush message is queued, the record is subsequently deleted before the cache flush message is processed, and when the cache flush processor attempts to handle the message. It can't find the record and logs an error.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2028299

 [KB3061412](https://hi.service-now.com/kb_view.do?sysparm_article=KB3061412)

</td><td>

In Platform Analytics, an ACL isn't letting an admin user modify or create data visualizations in dashboards or data visualizations

</td><td>

When editing any visualization in a dashboard with the sn\_hr\_er\_case table as a data source, the visualization can't access its data source. As a result, metrics are turned off and can't be edited, preventing updates or modifications to the visualization. There is error: 'You don't have access to the data source used in this visualization'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Change Management

 PRB2027139

</td><td>

The search bar and the divider overlap when 'Items per page' is set to 48

</td><td>

 

</td><td>

1.  Open the Create Change page.
2.  Set items per page to 48.

 Expected behavior: Heading, search bar, and divider render without overlap.

 Actual behavior: Search bar and divider overlap the heading.

</td></tr><tr><td>

Change Management

 PRB2029102

</td><td>

Manual approvers can't be added to the change and std\_change\_proposal due to newly enforced ACLs for related lists

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2035555

</td><td>

The 'All' filter on the 'Create Change' page doesn't display all standard change templates when a template has no category or catalog

</td><td>

When the 'All' filter is selected for standard change templates on the 'Create Change' page, not all templates are displayed. This is because one template has no category. The null category errors the 'can category be read by user' check.

</td><td>

 

</td></tr><tr><td>

Cloud Encryption

 PRB1980759

</td><td>

Prevent erroneous tampered DARE Properties notifications emails from being set to users

</td><td>

The error message, 'The tampering activities for Cloud Encryption properties have been found' is found in the logs.

</td><td>

 

</td></tr><tr><td>

Cloud Provisioning and Governance

 PRB1992234

</td><td>

​The catalog task **State** field is read-only

</td><td>

This is due to an ACL that looks for the 'sn\_request\_write' role. The user may not have this role installed.

</td><td>

1.  Log in to an instance.
2.  Disable any custom ACLs that were created in order to bypass this change.
3.  Impersonate a test user.
4.  Navigate to a catalog task in an **Open** state.

 Observe that the **State** field is read-only.

</td></tr><tr><td>

CMDB Health Dashboard

 PRB2037629

</td><td>

Certification audit OOMs node on large tables

</td><td>

On a fully-patched Zurich instance, a single CMDB data-certification audit job \('Audit for switchport'\) running on a glide.scheduler.worker thread retained 625 MB — over 50% of the 1.20 GB live heap — and tripped the GC-time heap-dump threshold \(node GC-thrashing toward OOM\). The audit loads the entire CI result set into memory in one pass instead of streaming it.

</td><td>

 

</td></tr><tr><td>

Column Level Encryption

 PRB1990541

</td><td>

Attachment upload defaults to 'None' encryption module in the workspace

</td><td>

Attachment upload defaults to 'None' encryption module in the workspace, where as in Classic View its working as expected.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1994536

</td><td>

Condition display value for 'Class is a &lt;ci class&gt;' isn't readable

</td><td>

There are applications that use condition builder, such as CMDB Data Manager, where data manager admins can create policies. They need to be able to read and interpret the conditions they select and save.

</td><td>

1.  Navigate to the cmdb\_ci list view.
2.  Choose **Class 'is a'** &gt; **Server**.
3.  Select **Run**.

 Observe that the display format of the condition is now 'Sys class path is a /!!/!2/!\(/!!%'. This is not readable.

</td></tr><tr><td>

Condition Builder

 PRB1997702

</td><td>

Limited number of values are shown in the 'Is one of' filter in Workspace

</td><td>

The filter is truncated and there's no way to check which values are configured. When the user wants to edit, it's also not possible to see all of the values.

</td><td>

1.  Navigate to the list view in CSM/FSM or SOW.
2.  Use the list filter settings and locate a operator which has the option to be 'is one of'.
3.  Add more than 10 values to the proper field.
4.  Select **Run**.
5.  After it's executed, check the filter again.

 Observe that the filter is truncated and there's no way to check which values are configured. When the user wants to edit, it's also not possible to see all of the values.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1994587

</td><td>

A race condition between IRE LazyWriter and Deletion Strategy causes the configuration item \(CI\) state to flip incorrectly

</td><td>

A CI's state is flipping from installed to stale during Discovery \(delete strategy execution\). A race condition occurred between IRE's asynchronous batch update of the **last\_discovered** field using 'db.executeLazy\(\)' and the execution of the Deletion Strategy. The LazyWriter delay caused the Deletion Strategy to process stale 'last\_discovered' values, marking valid CIs as retired despite their presence in the payload.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2020163

</td><td>

CMDB Data Manager archive tasks and retire tasks are not being processed correctly

</td><td>

Archive tasks and retire tasks fail with the message: 'Error: Failed to create archive chunk.' and the retire policy CIs already associated to these tasks are not being processed.

</td><td>

 

</td></tr><tr><td>

Core UI Responsive Dashboards

 PRB2013831

 [KB3143538](https://hi.service-now.com/kb_view.do?sysparm_article=KB3143538)

</td><td>

There's a dashboard layout issue after upgrading an instance to Australia

</td><td>

After an Australia upgrade, multiple users are reporting issues with alignments of reports in dashboards. While reports aren't missing, they are displayed vertically in dashboards. The issue is reproducible with core legacy dashboards.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Core UI Responsive Dashboards

 PRB2034505

 [KB3085059](https://hi.service-now.com/kb_view.do?sysparm_article=KB3085059)

</td><td>

A Platform Analytics \(PA\) dashboard overview can't load any dashboards

</td><td>

If all of the following conditions are met, the dashboard doesn't appear on the 'All' tab of PA dashboard 'Overview' page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Customer Service Management

 PRB2002976

 [KB3141009](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141009)

</td><td>

An advanced qualifier reference that uses 'current' isn't functioning as expected in CSM Workspace

</td><td>

Advanced reference qualifiers that rely on the 'current' object fail when templates are applied in Workspace. However, the same functionality works as expected in 'Classic UI \(UI16\)'. During template application in Workspace, the platform passes corrupted or incomplete serialized data to 'GlideRecordEncoder.decode\(\)'. As a result, the current GlideRecord is returned without field values.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Compaction

 PRB1816028

</td><td>

The 'Unexpected Compactor' job runs on the sys\_attachment\_doc table, causing an outage

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Compaction

 PRB1993126

 [KB3109620](https://hi.service-now.com/kb_view.do?sysparm_article=KB3109620)

</td><td>

'Compactor' on RaptorDB creates indexes without 'CONCURRENTLY', causing widespread locks

</td><td>

The DB 'Compactor' job creates direct indexes on temporary tables that are linked with source tables through triggers. Once 'insert' comes in for a source table, the trigger also tries to write on a TMP table, and are blocked by the 'Create index' command.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1636284

</td><td>

There's an inaccurate group count in a reference field with duplicate display values when results are pagenated

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1984070

 [KB2928335](https://hi.service-now.com/kb_view.do?sysparm_article=KB2928335)

</td><td>

Trend reports and dashboard show inaccurate data by week across the end of a year

</td><td>

On instances using a PostgreSQL database, an incorrect year reference \(yearref\) is returned for the non-ISO week functions sunday\_week and monday\_week. As a result, the column data displays trends for future dates where no actual record data exists. This issue affects reports and dashboards that group or summarize data by week across the end of a year. Reports may display an unexplained empty week in one year, a duplicated week in another, or records appearing in the incorrect annual bucket.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2007256

 [KB2925734](https://hi.service-now.com/kb_view.do?sysparm_article=KB2925734)

</td><td>

The text search doesn't return results in non-English languages

</td><td>

After downloading language plugins and switching the system language to a non-English language, results aren't returned when the property 'glide.​db\_​query.​replace\_​distinct\_​with\_​groupby' is set to 'false.' When the language is set to English, results are returned.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2051225

 [KB3141251](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141251)

</td><td>

GlideAggregate and Platform Analytics pivot fails with 'must appear in the GROUP BY clause' when grouping or sorting by a translatable field in a non-English language

</td><td>

The pivot shows 'No data available.'/'Aucune donnee disponible.' instead of the data. The node log shows com.glide.db.GlideSQLException with the PostgreSQL error, 'ERROR: column 'sc\_cat\_item3.name' must appear in the GROUP BY clause or be used in an aggregate function.'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1968227

</td><td>

DMLActionBatcher has some performance regressions comparing the StatementBatcher in MariaDB

</td><td>

The primary performance gap is driven by differences in how each batching mechanism manages transactional boundaries, especially during batch flush. An additional gap exists for mixed-mode statements.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1975852

</td><td>

MetricStatsCache causes the application node to run OutOfMemory

</td><td>

QueryMetricStatsListener has a cache limit of 10K entries \(from AbstractMetricStatsListener\), but as each entry contains a query which can be up to 2MB \(hardcode limit\), the user can easily spike the memory usage and run the node OOM.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1967193

</td><td>

CMDB Query Builder doesn't work when multiple OR conditions are used on location attribute

</td><td>

When multiple OR conditions are used on the location filter, the CMDB query builder doesn't return any results.

</td><td>

Scenario 1:

 1.  Navigate to the query builder.
2.  Open the configuration item query block.
3.  Select **Filter**.
4.  Run the builder with multiple OR conditions on the location filter.

Observe that no results are returned.

5.  Remove all the OR conditions for location \(or use one location filter\).
6.  Run it.

 Observe that once a second condition is added, the query builder fails.

 Scenario 2:

 1.  Navigate to the CMDB Query Builder.
2.  Add a server node to the canvas.
3.  Apply filters to the node with the following conditions:
    -   Location contains 'bock'
    -   Location contains 'via'
4.  Run the query.

Observe that no results are returned.

5.  Remove one of the conditions \(for example, 'Location Contains 'via''\).
6.  Rerun the query.

 Observe that results are now returned.

</td></tr><tr><td>

Database Persistence - Graph

 PRB1990632

</td><td>

Node/edge types should allow special characters for GraphMetadataAPI

</td><td>

Predefined filters fail in the Graph API version of the CMDB query builder. After a platform upgrade, CMDB query builder throws the 'Problem Running Query' error.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2005816

</td><td>

The choice field with 'none' doesn't appear intermittently

</td><td>

The choice field with 'none' doesn't appear in some cases for some users and sets the value of the next sequence number by default.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB2006319

</td><td>

ACL rules evaluated during twoPassQuery\(\) pull in mostly empty GlideRecords for context

</td><td>

During dot-walks, ACL rules evaluated during twoPassQuery\(\) often pull in mostly empty GlideRecords for context. This happens during script execution/condition evaluations.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB2075293

 [KB3150595](https://hi.service-now.com/kb_view.do?sysparm_article=KB3150595)

</td><td>

After the upgrade to Australia, auto-increment columns are failing inserts with the duplicate\_key error

</td><td>

Australia introduced a change to how certain database auto-increment sequences are managed. Under specific conditions, this change can cause the sequence used to generate new record identifiers to become invalid or out of sync with the database. When this occurs, attempts to create new records may fail. As a result, transient state records may not be created as expected in tables with the auto-increment field. This impacts many functional areas relying on the sequence record to track orders of states, logs or messages. This defect fix is included in the weekly patch due to its severe impact on multiple major functionalities across the platform.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1921715

</td><td>

Attempting to run an RLQuery condition on a database view removes all records unexpectedly from the view

</td><td>

Related List conditions aren't valid for database views, and they are blocked on the sys\_report condition builder. However, a user can run an encoded query containing a related list query \(just like any invalid query\) and get returned an invalid query error, which is correct. The problem is after specifically running a related list condition on a db-view \(valid or invalid\), all the records of the view disappear, leading to other problems.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2024733

 [KB3137449](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137449)

</td><td>

Reports containing reference-type catalog item variables \(lookup\) fail to render data after upgrading to the Australia release

</td><td>

After upgrading to the Australia release, reports that contain reference-type catalog item variable columns fail to render data correctly. The affected reference-type variables don't resolve their lookup values, and their presence in the report additionally causes all other columns — including native table fields such as Number, Created, and Closed — to render as empty across all rows.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Date Picker

 PRB2029576

 [KB3061444](https://hi.service-now.com/kb_view.do?sysparm_article=KB3061444)

</td><td>

There's an issue with GlideDateTime.setDisplayValue

</td><td>

Any script that calls setDisplayValue\(\) with an ISO-format string \(yyyy-MM-dd HH:mm:ss\) on an instance where glide.sys.date\_format is set to anything not in FORMAT\_LIST \(for example, dd-MM-yyyy, MM/dd/yyyy, etc.\) produces incorrect dates in Zurich.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Developer Sandboxes

 PRB2017438

</td><td>

DSB update sets aren't exported before clone

</td><td>

Because sandboxes are retired, update sets from a sandbox should be saved as remote update sets on the base instance on upgrade. However, due to this problem, they may not be saved correctly.

</td><td>

1.  Create a sandbox.
2.  Make changes in the sandbox.
3.  Upgrade the instance.

 Expected behavior: There is a way to recover the work.

 Actual behavior: . The work is gone. Logs show jsFunction\_exportUpdateSets is called.

</td></tr><tr><td>

Developer Sandboxes

 PRB2028151

 [KB3122033](https://hi.service-now.com/kb_view.do?sysparm_article=KB3122033)

</td><td>

Nodes are failing to upgrade during self-scheduled upgrades

</td><td>

After an upgrade, not all app nodes that were previously hosting a sandbox are upgraded. The nodes aren't in an error state and look okay. In Upgrade Monitor, users see that the node is actually not upgraded. This can happen on any upgrade and only impacts nodes that are hosting a sandbox. It can be seen in the logs that the upgrade process is checking the version of the instance and ignoring without updating the node. It's leaving a few of the nodes to fail to get upgrade. However, the change does not reflect that and it says it was successful.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1789882

 [KB1651489](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651489)

</td><td>

There's a large result set on the cmdb\_tcp table in DiscoveryReconciler from CookConnections

</td><td>

When the Application Dependency Mapping \(ADM\) probe returns a large number of references to 0.0.0.0, and IP Address count is limited by the 'sn.adm.ip\_expansion\_limit' system property value of 1000, large result sets can occur and cause instance outages.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1938058

 [KB2756546](https://hi.service-now.com/kb_view.do?sysparm_article=KB2756546)

</td><td>

Slow query from the status count optimizer impacts parallel launching of cloud app patterns

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1986211

</td><td>

Discovery.complete and discovery.canceled are triggered incorrectly

</td><td>

Discovery may trigger both discovery.complete and discovery.canceled events for the same status, and it may trigger discovery.canceled twice.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1989981

 [KB3057922](https://hi.service-now.com/kb_view.do?sysparm_article=KB3057922)

</td><td>

Issue with error handling for Test Credential if there's a KMF Issue

</td><td>

Either the Test Credential says that the credential worked \('Credential validated'\) or it will return this error: 'Cannot read properties of null \(reading 'indexOf'\)'. However, this is not the actual error that's occurring.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1996875

 [KB2801169](https://hi.service-now.com/kb_view.do?sysparm_article=KB2801169)

</td><td>

Cloud Infra Patterns are launched per datacenter, impacting GCP Discovery Schedules

</td><td>

GCP Discovery schedules take significantly longer to complete because the system launches one pattern execution per datacenter instead of one pattern per service account containing all datacenters. This results in a significant increase in probe executions.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1997816

 [KB2812138](https://hi.service-now.com/kb_view.do?sysparm_article=KB2812138)

</td><td>

Discovery status stops at phase one on a schedule with discovery behavior

</td><td>

When multiple phases exist on a behavior, discovery stops at the first phase.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB2005873

 [KB2958421](https://hi.service-now.com/kb_view.do?sysparm_article=KB2958421)

</td><td>

Daisy chain isn't working when a schedule is canceled

</td><td>

If one schedule in the daisy chain is canceled, none of the subsequent schedules in the chain are triggered.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB2016944

 [KB2997705](https://hi.service-now.com/kb_view.do?sysparm_article=KB2997705)

</td><td>

Classifier probes aren't firing if the 'First checked' probe has already been fired

</td><td>

Discovery should fire further probes, but instead completes prematurely.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB2037864

</td><td>

Scheduler Workers blocked by Cloud Discovery sensors waiting for discovery\_device\_history record locks

</td><td>

During Cloud Discovery, the Started and Completed counts on some Discovery Device records are updated many times. Many different sensors will be updating the same record, and be waiting for database locks for the record to clear before they can complete. With that causing extended runtime of these sensors, and given that there are lots of sensors running concurrently, updating the same record, this can lead to all scheduler worker threads being in use, blocking any other sys\_trigger scheduled jobs from starting.

</td><td>

 

</td></tr><tr><td>

Dynamic Translation for Agent Chat

 PRB1989609

</td><td>

When an instance has Now Assist installed, Dynamic Translation for Agent Chat \(DTAC\) doesn't honor the Dynamic Translation \(DT\) setting in Conversational Interfaces

</td><td>

 

</td><td>

1.  Provision an instance with Virtual Agent \(VA\) agent chat installed.
2.  Ensure that DT is set up with a provider.
3.  Ensure that Now Assist VA is installed.

 DTAC \(in either direction\) only displays the globe icon or is honored when DT in Now Assist Admin Console is turned on for that language.

</td></tr><tr><td>

Easy Import

 PRB1817119

</td><td>

Errors appear in logs when searching for the source table name in the transform map table

</td><td>

Easy import doesn't support Document ID type columns. Document ID type columns require the table name in addition to record details.

</td><td>

 

</td></tr><tr><td>

Edge Encryption

 PRB1945424

</td><td>

There's high memory utilization on proxy servers after the Yokohama upgrade

</td><td>

After upgrading and running Yokohama, the memory consumption is above the limit set in wrapper.conf. The user set the memory limit for 10G in the wrapper.conf, but the edge proxy doesn't respect this setting in the build. The memory goes to the physical limit and causes the proxy server to restart.

</td><td>

 

</td></tr><tr><td>

Encryption

 PRB1982641

 [KB2977274](https://hi.service-now.com/kb_view.do?sysparm_article=KB2977274)

</td><td>

Scan checks are missing null checks, causing the instance scan to fail

</td><td>

After running the 'Insecure GlideRecord Calls', if the getFunctionCallParamters\(\) function brings back an empty object, the instance scan fails.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Explicit Roles

 PRB2011506

</td><td>

The NullPointerException in ExplicitRoleCollisions .handleSysUserGrmember invalidates ATF rollback context during CreateUserStepRunner execution

</td><td>

During the scheduled nightly ATF test execution, a null pointer exception occurs in the explicit roles collision check logic, which propagates up and invalidates the ATF rollback context. This prevents automatic rollback of test-created records \(for example, Incidents, Users, Business Services\), leaving orphaned data in the environment.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1849568

</td><td>

Actions without an output are unable to proceed, but have a success status

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1909705

</td><td>

A transform script for JDBC DSAs isn't erroring out in engine major version v2

</td><td>

The issue can be reproduced when data stream actions are the same scope. The issue also occurs when the data stream actions are other than global and the script include is 'Global - Accessible to All Application Scopes'.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1937004

</td><td>

A script step reference input gives a string \(sys\_id\) instead of GRProxyStatic

</td><td>

A compilation should have the action's script input as a reference, but the action's script step input is resolved to a string on recompilation.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1967579

</td><td>

There's an issue with the **Debug** button on Flow Designer

</td><td>

When using the **Debug** button on Flow Designer in Zurich, these error message can show up: 'Cannot invoke 'com.snc.process\_flow .v2.model.DebugState .getBreakpoints\(\)' because 'debugState' is null' and 'Cannot invoke 'com.snc.process\_flow .v2.model.DebugState .​get​Source​Ui​Id​To​Breakpoint​Mapping\(\)​' because 'debugState' is null'.

</td><td>

1.  Provision a Zurich instance with the sn\_oracle\_hcm\_spk plugin installed.
2.  In Flow Designer, set up a flow that uses the flow action 'For Each Item in Look up Locations Stream'.
3.  Test it with the debug option.

 Notice the error messages.

</td></tr><tr><td>

Flow Engine

 PRB1989760

</td><td>

Execution details don't load during negative testing

</td><td>

The following error appears: 'There was an error loading the execution details for this flow context. Exception while executing request: Could not deserialize value from sys\_flow\_value with sys\_id 7fb6dcdbd9363a10919050c11e4ef686'.​

</td><td>

1.  Open an instance.
2.  Open the FD.
3.  Select the **Google Drive** application.
4.  Select **Look up file**.
5.  Provide a random file ID.
6.  Select the **Test** button

 Observe that FD execution doesn't load. The following error appears: 'There was an error loading the execution details for this flow context. Exception while executing request: Could not deserialize value from sys\_flow\_value with sys\_id 7fb6dcdbd9363a10919050c11e4ef686'.​

</td></tr><tr><td>

Flow Engine

 PRB2036311

 [KB3141836](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141836)

</td><td>

The SLA Percentage Timer flow action overwrites the paused task\_sla with stale GlideRecord state

</td><td>

The SLA Percentage Timer flow action \(Wait until N% of SLA Duration\) receives the task\_sla GlideRecord captured at flow-trigger time and passes it straight into SLACalculatorNG.calculateSLA. The pause guard inside calculateSLA reads pause\_time off that in-memory snapshot rather than re-checking the database. If another transaction pauses the task\_sla row between the flow trigger and the timer firing, the in-memory pause\_time is still nil, the guard is bypassed, and updateTaskSLAs overwrites duration/percentage/ time\_left/ business\_\* / has\_breached using running-state values. This silently corrupts the paused row. The same race also lets concurrent recalculations \(SLA engine business rules, Calc SLAs on Display, breakdown processor, SLA repair tool\) be overwritten by the stale flow GlideRecord. As a result, users see SLA timers that continue to accrue elapsed time while the underlying task is paused, and the breach state may flip incorrectly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1914472

</td><td>

The 'Retry policy' isn't accessible when a flow is executed by a non-admin

</td><td>

 

</td><td>

1.  Create a flow with a REST step, which has a retry policy specified inline.
2.  Invoke the flow in the background as a non-admin user.

 See messages saying 'Security constraints prevent displaying information' due to attempting to access the 'Retry' policy as a non-authorized user.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1990495

 [KB2780048](https://hi.service-now.com/kb_view.do?sysparm_article=KB2780048)

</td><td>

The 'Update record' action updates an invalid GlideRecord and triggers business rules when the reference record is deleted while a flow is in progress

</td><td>

When the record that is passed to a subflow is deleted while the flow is in progress, any 'Update record' action in the subflow doesn't error out with 'Glide record is invalid' type errors. Instead, the 'Update record' action in the subflow falls back and iterates on all records in the table, causing substantial data impact.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2003332

</td><td>

The user receives the message, 'Number of rows hidden by security constraints ' in Flow Designer related sub-flows

</td><td>

The user sees the security constraints message when opening 'See related flows' in sub-flows.

</td><td>

1.  Open Flow Designer.
2.  In the 'Subflows' tab, open a subflow.
3.  In the 'More' menu, select **See related flows**.

 Notice the security constraint message when it opens.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2019365

</td><td>

Domain trigger for agentic workflow only works if created by an admin of that domain and not another admin changing the picker

</td><td>

When a user with elevated privileges switches to a child domain \(for example, Oceanic\) via the domain picker and publishes a flow, the sys\_flow\_trigger\_plan record gets created in the wrong domain \(global instead of Oceanic\), while the sys\_hub\_flow record is correctly in the child domain.

</td><td>

 

</td></tr><tr><td>

GlideAggregate API

 PRB1922184

</td><td>

Data isn't visible in the dashboard when using time series visualization and using keywords as a filter

</td><td>

The following error appears: 'Error : No Data Available. There is no data available for the selected criteria.' The issue doesn't occur with other visualizations.

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1922298

</td><td>

Assessment Metrics \(asmt\_metric\) in a question bank disappear after they're used in a published survey

</td><td>

On an instance running on RaptorDB \(postresql\), the assessment metric in the question bank can disappear. The issue can't be reproduced on MariaDB.

</td><td>

 

</td></tr><tr><td>

Group and Action Framework - Family

 PRB2025623

</td><td>

The base instance business rule 'CSM NATT- Assign case to cluster' leads to OutofMemory heap space errors

</td><td>

Multiple 'ASYNC: CSM NATT- Assign case to cluster' jobs running on the nodes are causing OutOfMemoryError: heap space, leading to node restarts.

</td><td>

1.  Open an instance with attachment sizes on the ml\_model\_artifact table that are over 100 MB.
2.  Trigger multiple 'ASYNC: CSM NATT- Assign case to cluster' jobs to run on a single node.

 Notice the memory consumption by these jobs.

</td></tr><tr><td>

HR Service Delivery

 PRB2018687

</td><td>

The **Edit** button does not work for the Granular Delegation rule

</td><td>

The record edits are not reflected even though the Granular Delegation rule was created.

</td><td>

1.  Install the Granular Delegation Plugin.
2.  Create a Granular Delegation Rule.
3.  Save it.
4.  Use the **Edit** button to modify the user criteria to the delegate/delegator.

 Notice that after the edit, the record doesn't reflect the changes.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1667004

 [KB1348033](https://hi.service-now.com/kb_view.do?sysparm_article=KB1348033)

</td><td>

Paste formatting options from aren't honored in Service portal

</td><td>

A pop-up gets displayed in Service portal whereas in Platform it doesn't.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1768733

</td><td>

**The HTML** field shows as changed even though no changes occurred

</td><td>

**The HTML** field shows as changed without changes being made in 'History' &gt; 'Calendar'. There are no user updates to the **rich\_description** field, but a sys\_history\_set update record appears.

</td><td>

1.  Navigate to any open incident form view.
2.  Select **Configure** &gt; **Form Layout**.
3.  Add a new field \(for example, **Rich Description**\) with HTML type.
4.  Save.
5.  Create a sample record.
6.  Navigate to Scripts - Background.
7.  Run a test script.
8.  Navigate to the incident just created via the background script.
9.  Update some field \(for example, **Caller**, **Description**, etc.\).
10. Save.
11. Select **History** &gt; **Calendar**.

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB1988771

 [KB3082116](https://hi.service-now.com/kb_view.do?sysparm_article=KB3082116)

</td><td>

IPAccessListFilter handling for malformed IP addresses

</td><td>

Inbound REST API calls coming through proxy servers \(x-forwarded-for header with multiple IP's\) or malformed IP address can sometimes fail in Zurich and Australia instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Incident Communications Management

 PRB2028847

</td><td>

A skipped error occurs upon upgrading to Australia

</td><td>

After upgrading to Australia, a skipped error occurs because sys\_​gauge\_​4f1906b1bf3001003f07e2c1ac07393a record doesn't exist. Repairing the plugin doesn't resolve the issue.

</td><td>

1.  Before upgrading, check that the com.snc.iam plugin isn't installed and that it has three dependencies.
2.  Upgrade to Australia.
3.  Check if the com.snc.iam is installed upon the upgrade.
4.  Check if the skipped error occurred. If so, see if that a problematic record exists.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1721309

 [KB1584953](https://hi.service-now.com/kb_view.do?sysparm_article=KB1584953)

</td><td>

An app node is throwing a java.io.IOException: 'Too many open files due to IDR/Kafka issues'

</td><td>

The node is unresponsive or having odd behavior, such as the sidedoor displaying an empty page and intermittent xmlstats.do outputs.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Instance Scan

 PRB1992382

 [KB2901125](https://hi.service-now.com/kb_view.do?sysparm_article=KB2901125)

</td><td>

Instance scan jobs get stuck in a sleep loop for days, which causes the subsequent scans to fail

</td><td>

Instance scan findings are written to the database asynchronously and are tracked using a global counter. If any write fails, the counter doesn't decrement properly; it goes up but never comes back down. This causes all future scans to hang indefinitely, waiting for a counter that will never reach zero. There's no timeout or logging to flag this, so scans can get stuck silently.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Instance Scan

 PRB2017072

</td><td>

Instance scans detecting custom records instead of other records are modified from the baseline

</td><td>

Instance scan checks like 'Differs from baseline' are detecting custom records created by users. As per the script used, only the records which are modified should be detected.

</td><td>

 

</td></tr><tr><td>

Instance Security Center Session Management \(no longer supported\)

 PRB2024942

 [KB3071146](https://hi.service-now.com/kb_view.do?sysparm_article=KB3071146)

</td><td>

SessionDebug not deregistered from LogDispatcher on session expiry, causing unbounded heap growth and out of memory errors

</td><td>

When a user enables session-level debug logging \(via sys\_debug.do\), a SessionDebug instance registers itself as a LogListenerAdapter in the global LogDispatcher. If the owning GlideSession expires via timeout or is invalidated rather than through a clean logout, SessionDebug is not deregistered from LogDispatcher. The orphaned SessionDebug continues to receive every log event from the JVM across all threads. With verbose debug scopes \(for example, CacheSessionDebug\), individual OutputLine entries average 10–25 KB each. The output list is capped at ~10,001 entries, meaning a single orphaned SessionDebug can retain 200–300+ MB of heap indefinitely until the node restarts.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Integration Hub Data Stream Actions

 PRB1979273

</td><td>

Data stream flow report is not available due to orphaned context records

</td><td>

The issue occurs because Data Stream context records are populated with an incorrect source\_record sys\_id during execution. Since the referenced record does not exist in the sys\_flow\_context table, the context records are identified as orphan records and deleted by the Unreferenced Record Cleaner rule. Once deleted, the Flow Report cannot be generated, resulting in a null flowReport object and a runtime exception.

</td><td>

1.  Create a Data Stream action, or use an existing Data Stream action available via XML import.
2.  Trigger the Data Stream action and allow the execution to complete.
3.  Verify that context records are generated for the action, including child contexts \(for example: test\_with\_empty\_page.page$8\).
4.  Open one of the generated context records and inspect its XML.

Note the value populated in the source\_record field.

5.  Verify that the source\_record sys\_id does not match any record in the sys\_flow\_context table.
6.  Wait for the Unreferenced Record Cleaner scheduled job to run \(approximately one hour\).
7.  Attempt to open the Flow Report for the Data Stream execution.

 Expected behavior: Data Stream context records should reference a valid source record in the sys\_flow\_context table. Context records should not be treated as orphaned. Flow reports should remain available and load successfully.

 Actual behavior: Data Stream context records reference a non-existent source record in the sys\_flow\_context table. These records are treated as orphaned and removed by the Unreferenced Record Cleaner. Flow Report fails to load with an error.

</td></tr><tr><td>

Integration Hub

 PRB1870601

</td><td>

A PowerShell step error message is no longer populated

</td><td>

On flow engine V1, the user ran a flow execution and can observe 'Error Code' and 'Error Message' are outputed in the 'Output Data' section when the PowerShell script returns an error. However, if users switch to flow engine V2, the same error code and error message can not be rendered into the 'Output Data' section.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1975287

</td><td>

The 'Send Email' flow action adds unnecessary line breaks at the end of the email

</td><td>

Send Email Flow Action adds unnecessary line breaks at the end of the email. Please refer to the steps to reproduce and CSTASK1282991 Reproduced in Y, Z.

</td><td>

1.  Create a new flow with the **Send Email** action.
2.  Add test recipients and subject.
3.  In the rich text body, add the following: '

パスワード初期化依頼が正常に行われました。これから受付作業に入ります。完了連絡まで今しばらくお待ちください。申請状況はポータルトップ右下の「あなたのヘルプデスクへの問い合わせ」よりご確認いただけます。以下、申請内容となっております。【セルフパスワードリセットを実施しましたか？】：【リセットができなかった理由】：【初期化対象者氏名】：【初期化対象所属】：【初期化対象メールアドレス】：【対象IDの種類】：【連絡先電話番号】：【上司氏名】：【上司所属】：【上司メールアドレス】：【初期化理由】：【パスワード初期化に同意しますか？】：

'


 Observe that many line breaks are added at the end of the email.

</td></tr><tr><td>

Integration Hub

 PRB1983057

</td><td>

There are base instance Script Includes with duplicate names \(for example, RestStepMultipartUtil and RestStepFormUrlEncodedUtil\)

</td><td>

 

</td><td>

1.  Provision an instance with the IH starter plugin and SSE step \(com.​glide.​hub.​action\_​step.​sse\)​ installed.
2.  Navigate to the sys\_script\_include table.
3.  Search for 'name contains reststep'.

 Observe that duplicate names appear.

</td></tr><tr><td>

Integration Hub

 PRB2033476

</td><td>

After upgrading to Australia, password actions such as 'Change User Password' and 'Reset User Password' fail

</td><td>

The password actions 'Change User Password' and 'Reset User Password' are failing from Microsoft Active Directory v2 Spoke.

</td><td>

 

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

Issue Auto Resolution for Virtual Agent

 PRB1657388

 [KB1307989](https://hi.service-now.com/kb_view.do?sysparm_article=KB1307989)

</td><td>

Issue Auto Resolution \(IAR\) for HR isn't able to execute for users who remove HR roles from the 'admin' role due to internal data governance policies

</td><td>

Affects users using IT and HR products on the same instance. Due to the data internal visibility/governance policies, users have removed a number of HR roles \(for example, 'sn\_hr\_core.admin' role\) from the admin role, resulting in users in the IT business units not having access to the HR side of the platform. Removing the roles from the admin profile prevents the 'system' user from executing the AutoResolution scripts includes. The 'system' user no longer has access to the HR tables of the instance, hence it can't extract the necessary information for auto resolution ML Configuration Language solution, auto resolution context, or write to HR records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

IT Service Management Foundation License Control

 PRB2021441

 [KB3032668](https://hi.service-now.com/kb_view.do?sysparm_article=KB3032668)

</td><td>

Unable to rollback the plugin 'com.​snc.​itsm.​foundation.​license\_​control'

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

JVM at Scale

 PRB2032235

 [KB3078521](https://hi.service-now.com/kb_view.do?sysparm_article=KB3078521)

</td><td>

Memory watcher isn't logging active transactions in the Australia release

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB2058369

 [KB3140571](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140571)

</td><td>

Midserver is unable to fetch credentials after upgrading to Zurich or Australia

</td><td>

In certain versions, there's a Unified Secrets Gateway \(USG\) service for credential management. During the upgrade to those versions, a system trigger script is designed to automatically execute and populate the sys\_​secret\_​identity\_​group\_​member table with the MID Server identity group mappings required for USG authentication. However, this trigger fails to complete successfully, leaving the table incompletely populated. As a result, the MID Server can't authenticate with USG and fails to retrieve credentials.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Knowledge Blocks

 PRB2000541

</td><td>

There are formatting issues in the KB article view compared to the 'Details' tab view

</td><td>

There are differences in the formatting of the KB article between the 'Details' tab and the 'View article' view.

</td><td>

1.  Open the Compliance workspace.
2.  Navigate to **List modules** &gt; **All Policies**.
3.  Create any policy record with all the required fields completed.
4.  Switch to the 'Policy text' tab.
5.  Select **Import word document**.
6.  Import the word document.
7.  Select **Request review**.
8.  Select **Request approval**.
9.  Switch to the 'Approvals' tab.
10. Approve the record.
11. Switch back to the 'Details' tab.

Notice that there is a KB article generated in the **Published policy** field.


 Notice that the formatting in the KB article 'Details' tab and the 'View article' view are different.

</td></tr><tr><td>

Knowledge Management

 PRB1969145

</td><td>

The **Next** button doesn't respond when creating a Knowledge article from the Knowledge List view

</td><td>

When creating a Knowledge article from the Knowledge List view, selecting the **Next** button on the kb\_knowledge\_create wizard does nothing. The issue occurs when the referring URL includes a URL‑encoded sysparm\_query parameter \(for example, sysparm\_referring\_url =kb\_knowledge\_list.do %3Fsysparm\_query%3D…\). The client script attempts to split on 'sysparm\_query=', but the encoded value prevents a proper split, causing a TypeError and freezing the wizard. Users are unable to proceed to the article form, impacting article creation.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1975454

 [KB3151964](https://hi.service-now.com/kb_view.do?sysparm_article=KB3151964)

</td><td>

The 'View article' link in Manager Hub is not working as expected for employee users

</td><td>

After selecting the article as an employee from the results, the article is empty because it the fields from the template article are not rendering.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Knowledge Management

 PRB1997589

 [KB2970962](https://hi.service-now.com/kb_view.do?sysparm_article=KB2970962)

</td><td>

A published article displays a grey HTML body when ECE and the 'Minor edit' property are turned on

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2000521

</td><td>

Support for Knowledge blocks in ECE

</td><td>

Knowledge blocks are not supported in ECE. Ideally, blocks should be supported in ECE.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2002569

 [KB2930942](https://hi.service-now.com/kb_view.do?sysparm_article=KB2930942)

</td><td>

The user is no longer able to edit the workspace view of Knowledge Forms

</td><td>

When attempting to modify the Workspace configuration for Knowledge Base articles, the system prevents changes from being made. The related components appear to belong to a private application scope, which restricts editing. The user receives the message, 'The 'Knowledge' section is in the sn-​component-​workspace-​knowledge application and cannot be edited. The installed application 'sn-​component-​workspace-​knowledge' is private.' This blocks customization or adjustments to the Knowledge Form layout within Workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Knowledge Management

 PRB2071699

</td><td>

The knowledge search returns empty results for guests users on the CSP portal

</td><td>

No search results are displayed. However, when the user navigates from Knowledge Base, they can access the article as a guest.

</td><td>

1.  Navigate to the CSP portal as a guest user.
2.  Configure the Knowledge Base for guest users.
3.  Make widgets public.
4.  Navigate to the homepage.
5.  In the search bar, search for some text that's present in an article.

 Observe that no search results are displayed. However, when the user navigates from Knowledge Base, they can access the article as a guest.

</td></tr><tr><td>

Language and Translations

 PRB1931121

</td><td>

The set language doesn't stay consistent on the login page

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Language and Translations

 PRB1960166

</td><td>

The Japanese translation of 'No' for a Yes/No variable isn't correct

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1951502

</td><td>

When a user groups by any column and if it returns more than 20 rows, the list view only displays 20 rows even when the user selected to display 100

</td><td>

The maximum number of records displayed per group is the number of records per page in list view. If users select to show 100 rows in one list page, it shows 100 rows in the grouped list, but not the list view rows.

</td><td>

1.  Navigate to incident.LIST.
2.  Right-click on the 'Number' column.
3.  Group by 'number'.
4.  From the contextual menu options, select to show list 100 rows.

 Expected behavior: The list view should displays 100 records.

 Actual behavior: The list view still displays 20 records.

</td></tr><tr><td>

List Administration

 PRB1963197

</td><td>

**The Duration** field displays '0 seconds' in a Core UI list when the value is null

</td><td>

 

</td><td>

1.  In Zurich, navigate to any table list view that contains the **Duration** field.
2.  Filter by '&lt;DURATION\_TYPE\_FIELD&gt;' is 'Empty'.

 Review that records have '0 seconds' even if there's no value in the records \(empty\).

</td></tr><tr><td>

List Administration

 PRB1991341

 [KB2803013](https://hi.service-now.com/kb_view.do?sysparm_article=KB2803013)

</td><td>

Unable to update **User** field / other fields at Certification Task level

</td><td>

In the Certification Task record, under the inline level, the **User** field or other editable fields are not editable. When attempting to change the value by double‑selecting the field, the field goes into a loading state and never allows selection of another.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1994887

</td><td>

Issue with sharing a list from My List, users are only able to select 10 users

</td><td>

When the user creates a list in SOW under My List, they can share the list to the users. However, the drop-down list that shows both users and user groups shows only ten records.

</td><td>

1.  Open SOW.
2.  Create a new list under my list.
3.  Share the list to users.

 Notice there are only ten options available, and after selecting all the ten users it appears empty.

</td></tr><tr><td>

List Administration

 PRB2009991

 [KB3090094](https://hi.service-now.com/kb_view.do?sysparm_article=KB3090094)

</td><td>

'Workflow'-type fields are displaying as 'Pending - has not started' for all values

</td><td>

This requires a single-line change that adds a defensive .clone\(\) call to deep-copy the choice list before WorkflowIcons.process\(\) mutates it. This prevents the shared cache from being poisoned by in-place label overwrites.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB2012758

</td><td>

List fails to load due to a DataFetchingException from NowAssistSkillConfig

</td><td>

The list page in Service Operations Workspace doesn't load; it looks like the page is processing. NAA code is called and throws an exception, which results in list load error.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2020153

</td><td>

The tab view and list view aren't working correctly

</td><td>

Tab view and list view not working correctly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB2027491

</td><td>

NullPointerException in List​Layout.​get​Grouped​Row​Layout​Query from null Integer auto-unbox on List​Layout​Builder.​get​Record​Count​Limit\(\)​

</td><td>

\[ZP8 regression\] NullPointerException in List​Layout.​get​Grouped​Row​Layout​Query from null Integer auto-unbox on List​Layout​Builder.​get​Record​Count​Limit\(\)​ Caused By Task : DEF071991.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2030898

</td><td>

The 'Selected stage' icon isn't applied when WorkflowIcons has already assigned a default icon

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2031478

 [KB3074807](https://hi.service-now.com/kb_view.do?sysparm_article=KB3074807)

</td><td>

The 'List edit' pop-up is not working in UI16 view with Polaris disabled view

</td><td>

The user is not able to edit values from the List view, and the 'List edit' pop-up is partially or not visible at all. The 'List edit' pop-up should be visible for every row and for every column.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB2033285

</td><td>

There's an Australia update issue with roles not appearing in the 'Table/workspace' view

</td><td>

Having a dictionary entry with 'Use Dependent Field' turned on and pointing to a boolean dictionary entry on the same table causes the values on the list to not display.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2033991

</td><td>

The column filters are not applying as expected

</td><td>

When applying the column level filter, the select is empty for the Short description field, and the user observes that the list is not filtered.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2034071

</td><td>

The underline that sets links apart only appears on hover and keyboard focus

</td><td>

In HR Agent Workspace list view \(or in any workspace that uses the now-grid component to render lists\), links in the resting state are distinguished from the surrounding non-link text by color only. The link color computes to RGB =, which is about 2.7:1 against the adjacent text color, below the 3:1 needed for a luminance-based distinction.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2036908

 [KB3097895](https://hi.service-now.com/kb_view.do?sysparm_article=KB3097895)

</td><td>

An error occurs reading, 'Sorry, an error occurred or this page isn't available'

</td><td>

The page times out.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB2039348

</td><td>

In the List view, the first choice is shown and is not the selected choice for the lookup select box variable in the workspace

</td><td>

Irrespective of whatever option the user might have selected, it will show the first choice in the workspace List view.

</td><td>

 

</td></tr><tr><td>

List Editor

 PRB2001509

</td><td>

Inline list editing pop-up edit box UI is mispositioned when trying to edit a reference field by double clicking on it

</td><td>

The pop-up edit box UI is mispositioned when trying to edit any inline editable field by double clicking on it on a List Report added to a Dashboard. The dialog box that appears is positioned away from the actual field being edited and has an incorrect format: The cross is not red and the square around the magnifying glass is incomplete.

</td><td>

 

</td></tr><tr><td>

List Filters

 PRB1982205

</td><td>

Data visualizations don't translate to the selected language

</td><td>

The data visualization column is displayed in English instead of Swedish. Only the left sidebar is translated into Swedish.

</td><td>

1.  Provision an instance with the French language pack \(com.snc.i18n.swedish\) installed.
2.  Open Visualization Designer in Platform Analytics Workspace.
3.  Create a new visualization.
4.  Change the session language to Swedish.

 Observe that the column is displayed in English instead of Swedish. Only the left sidebar has been translated into Swedish.

</td></tr><tr><td>

List Filters

 PRB1994984

</td><td>

Column filters on date/time fields aren't working as expected on Data Visualizations when the time format is HH:mm

</td><td>

When filtering list visualizations by column filters, such as 'Actual end date', no data is filtered. Users customized the time format \(glide.sys.time\_format\) from HH:mm:ss to HH:mm.

</td><td>

1.  Set the glide.sys.time\_format to HH:mm.
2.  Create a data visualization.
3.  Add 'change\_request' as a data source.
4.  In columns and rows settings, set the following to enabled: 'Show option to personalize columns - Show column filtering'.
5.  Enter a date in the column filter for 'Actual start date'.

 Observe that nothing is filtered.

</td></tr><tr><td>

List Pagination

 PRB1980717

</td><td>

Grouping by dot-walked fields causes incorrect pagination and empty pages

</td><td>

When grouping a list by a dot-walked field in Configurable Workspace, pagination behaves incorrectly. The list shows a limited number of groups per page, but the system calculates pagination as if all rows were loaded, resulting in empty pages when navigating past the valid results. This issue doesn't occur when grouping by a field that exists directly on the table \(non dot-walked field\).

</td><td>

1.  Log in.
2.  Open Customer Service Management/Field Service Management Configurable Workspace or Service Operations Workspace.
3.  Navigate to the 'List' page.
4.  Open any list of records with more than 20 records per page \(50 or 100\).
5.  Select **Group by** to group by a field.
6.  Dot-walk to a nested field from one of the reference fields.
7.  After selecting **Run**, the list refreshes to show the list on records grouped by **Caller** &gt; **Location**.

 See that the list currently displays '1-20 of 23 groups'. Somehow, even if the list is only displaying 20 groups, the system considers that the page contains 50 records \(based on the 'Rows per group' parameters\). If users select the second page, it's blank.

</td></tr><tr><td>

MID Server

 PRB1898139

 [KB2398708](https://hi.service-now.com/kb_view.do?sysparm_article=KB2398708)

</td><td>

The MID server doesn't start due to a parenthesis in the home folder's path, leaving the MID Server down after upgrades

</td><td>

If there's a parenthesis in the MID server path, the upgrade from the Yokohama version fails. This problem is specific to the Set-FolderPermissions.ps1 script.

</td><td>

1.  Create a MID server with a parenthesis in the path.
2.  Run start.bat.

 Notice that it fails with this line: '\\ was unexpected at this time.' The upgrade log also includes a 'was unexpected at this time' syntax error specific to the Set-FolderPermissions.ps1 path.

</td></tr><tr><td>

MID Server

 PRB1965219

 [KB2636231](https://hi.service-now.com/kb_view.do?sysparm_article=KB2636231)

</td><td>

If pre-checks are turned off, or if the 2GB free check isn't enough, MID Servers can run out of disk space during upgrades: 'No space left on device'

</td><td>

This should always be checked for before committing to an upgrade. If this happens while downloading or extracting the ZIP files, the upgrade aborts before launching the upgrade process and shutting down the MID server. If this happens when running the upgrade process, during the backing up of files for rollback, or copying new files over old, then rollback should preserve the MID Server files as they were, and restart the MID Server service successfully on the previous version.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1970951

</td><td>

'Failed to Upgrade' banner and issues record are misleading when a MID Server has been down for years

</td><td>

When a MID server record's version value doesn't match the instance's version, it's assumed it failed while upgrading. The errors mention only the upgrade and warn that there may be integration outages. Users may assume that this is a new issue caused by the recent upgrade and that it's urgent, and will often open a support case. That is a valid issue if the MID Server had been recently up. However, if a MID Server hasn't been in communication with the instance, and it's been in down state since before the last instance upgrade, that message is misleading. The key point the user needs to understand and resolve is that it's been down for months or years, not that it hasn't upgraded recently.

</td><td>

1.  Install a MID Server.
2.  Retire it.
3.  Wait five years.
4.  Look at the MID server issues records.
5.  Open the MID server form.

 Expected behavior: The issue is that it is down. The next steps are to either get it up again \(if it's still needed and meant to be up\), or delete the orphan record to avoid more ignorable errors in future.

 Actual behavior: There are many errors about the recent failed upgrade, wrongly suggesting this might be affecting something right now, and the failed upgrade is the cause.

</td></tr><tr><td>

MID Server

 PRB1971530

 [KB2949602](https://hi.service-now.com/kb_view.do?sysparm_article=KB2949602)

</td><td>

On some hosts, MID Servers need more than five chances to start up the JVM within 30 seconds, leaving them down during restarts or upgrades

</td><td>

When a MID Server service starts, the Tanuki Wrapper process runs, which then has to start the Java JVM process \(java.exe\), which in turn runs the MID Server application. In the situation where apparently the 'Wrapper Process has not received any CPU time', the wrapper gives the JVM only 30 seconds to start. It will then only retry five times total, then give up, leaving the MID Server Down. A manual start of the MID Server service is then needed, which requires access to the Host server, often requiring several attempts to start the service before the JVM starts within the 30 second timeout. This is seen in 'soft' restarts, such as re-key, where only the JVM is restarted and also 'hard' restarts from the 'Restart MID' related link and where the service is stopped and started. This has been observed on VMware VMs, where the Windows OS is reporting plenty of free CPU at the time.

</td><td>

Restart a MID Server either from the service, from the MID Server form, during re-key, validate/invalidate, or upgrades.

 Expected behavior: The MID Server was up, and is expected to still be up afterwards.

 Actual behavior: The wrapper can't start the JVM and MID Server application and leaves the MID Server down. This results in an outage for any features using exclusively that MID Server, or performance issues if failover/load balancing is implemented.

</td></tr><tr><td>

MID Server

 PRB1986560

</td><td>

An MID Server Rate limit exceeded error is logged when it's actually working as designed

</td><td>

A rate limiting feature added in Washington DC throttles the execution of SystemCommands. When the invocation rate exceeds the maximum configured rate, a cooldown period will begin and additional invocations of the system command will be ignored until the cooldown period has expired. This causes an error in the agent log.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1998489

</td><td>

Root Cause Analysis \(RCA\)/Cross Scope Access changes are casuing the 'MAW' list and record declarative actions to be blocked from execution

</td><td>

Changes made in RCA/Cross Scope Access on the platform side have impacted the declarative list and record actions for MAW from working. When attempting to execute any of these actions which call the MIDManage API, users see an error that the RCA record isn't present for this script execution, despite the Cross Scope Access record being defined.

</td><td>

1.  Install MID Admin Workspace on any release on a fresh instance.
2.  Try to validate MID Server.

 Notice that this action is blocked and the corresponding error banner displayed to the user.

</td></tr><tr><td>

MID Server

 PRB2006438

</td><td>

MID Server shuts down unexpectedly during startup due to sorting/filtering logic mismatch in ECC queue record batching

</td><td>

During MID Server startup, the server retrieves ECC queue records in batches from the instance. A mismatch in the sorting and filtering logic causes some records to be missed, resulting in an empty response. This triggers a MIDServerInfoException: No 'sysIds' array is returned in the response error, causing the MID Server to shut down unexpectedly.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2012665

 [KB2953193](https://hi.service-now.com/kb_view.do?sysparm_article=KB2953193)

</td><td>

MID Server upgrades fail because the MID.max.extract .file.size property default is too low

</td><td>

The MID Server property MID.max.extract .file.size property default of 500MB is too low for MID Server upgrades. Upgrades fail at the download/extract stage with the following errors, after the MID-core zip file has been successfully downloaded: '...Exceeds the maximum size \(500000000\). Unable to download package The size of uncompressed files is too big or too many entries in the zip file'. This fails before the MID Server is shut down, avoiding outages, but causes repeated failed upgrades, and the risks of running with an instance vs MID Server incompatibility, that generally has been known to break some features and cause data loss.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB2038587

</td><td>

The MID upgrade fails after Australia with the error message, 'Entry doesn't have valid signer'

</td><td>

MIDs upgrading to Australia have MID upgrade failures with the error message, 'Signature verification failed: Entry doesn't have valid signer'.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2039307

</td><td>

MID Server not upgrading on Prod, dev1 and test2 ServiceNow Instance

</td><td>

If the existing upgrade zip files on the install server have to be mended and replaced, for whatever reason, for MID Server auto-upgrade to work, then the instance does not re-download them. MID servers that download through the instance will continue to download the non-working files from before they were mended.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2040686

 [KB3138403](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3138403)

</td><td>

Linux MID Server pre-checks don't check that the service user would be able to run start.sh, before committing to an upgrade that would leave the MID Server Down

</td><td>

Linux MID Servers can end up stopped during the upgrade process if start.sh is prevented from starting the service again with 'Interactive authentication required' or 'Access denied' errors. This would also cause a Restart MID command from the instance, either from the MID Server's form, or when a plugin activation/upgrade triggers a restart, to leave the MID Server down. This problem is for error handling in this situation. That scenario should be checked for on startup, and as part of the pre-upgrade checks before committing to the upgrade. Breadcrumbs should be left before a restart, so that the MID Server can know a failed start happened, maybe read the relevant logs automatically, and clearly give the next steps to the user.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1769455

</td><td>

Filter to sort doesn't work offline in Xanadu

</td><td>

For scripted data items, there is another flow of processing records in offline mode. Filter and sorting mechanisms were not implemented for this flow.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2010847

 [KB2981757](https://hi.service-now.com/kb_view.do?sysparm_article=KB2981757)

</td><td>

After upgrading an instance in Zurich, a skipped record error is consistently observed in the upgrade history

</td><td>

The issue is reproducible on a clean instance, indicating that it's not caused by customizations or data inconsistencies introduced post-deployment.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Multi-provider Single Sign-on \(SSO\)

 PRB2003491

 [KB3065130](https://hi.service-now.com/kb_view.do?sysparm_article=KB3065130)

</td><td>

An admin-only ACR user can't login via local log in as the sso\_config\_admin role check in ACRUtil.isACRUserByUserID\(\) ignores the admin role

</td><td>

When SSO Account Recovery \(ACR\) is turned on in an instance, an admin user registered as an ACR recovery account may be unable to log in via local login even when valid credentials are entered. The system doesn't recognize the user as a valid ACR recovery account and blocks the login attempt. The primary purpose of ACR is to provide a fallback login path during an SSO outage. Due to this issue, the designated recovery administrator loses access to the instance at the exact moment the fallback is needed. This issue was introduced in the Australia release.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Natural Language Query \(Family Release\)

 PRB1992648

 [KB2794876](https://hi.service-now.com/kb_view.do?sysparm_article=KB2794876)

</td><td>

com.snc.nlq.MetadataGenerator modifies GlideElement objects in TableDescriptorCache

</td><td>

This issue is observed in production.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2003211

</td><td>

/api/now/ui/polaris/menu is slow to build the cache on login

</td><td>

1000s of each of these queries are run to retrieve user preferences and screen accessibilities. It should be able to retrieve all of most of these items in 1 query.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2015985

 [KB3143862](https://hi.service-now.com/kb_view.do?sysparm_article=KB3143862)

</td><td>

Tags on task records aren't following background color hex codes after a Zurich upgrade

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2038994

</td><td>

Duplicate modules appear when an application is added to the custom menu

</td><td>

 

</td><td>

1.  Create a custom menu.
2.  Add an application to the custom menu through the related list.
3.  Refresh the menu request by selecting the **Refresh** button in the 'All' menu.

 Expected behavior: The custom menu has an application with correct modules.

 Actual behavior: The custom menu has an application with duplicate modules.

</td></tr><tr><td>

Now Assist in AI Search

 PRB1920760

</td><td>

GenAI log IDs are not returned for Now Assist Genius Results

</td><td>

This issue occurs in Virtual Agent, portal, Now Assist Actions, Now Assist Q&amp;A, Synthesized Response, or anywhere a Now Assist Genius Result \(GR\) can be returned. Feedback is not logged even though there should be a value after the user selects the Thumbs up icon or Thumbs down icon on the Genius Result \(GR\).

</td><td>

1.  Open Virtual Agent.
2.  Perform a search that returns at least one Now Assist Genius Result \(GR\).
3.  Select the **Thumbs up** icon or the **Thumbs down** icon on the GR.
4.  Run the background job to process queued signals.
5.  Open the sys\_generative\_ai\_log table.
6.  Inspect the **Feedback** field for the transactions relevant to the Genius Result the user provided feedback on.

 Expected behavior: There should be a value such as 'Rejected' for negative feedback or 'Accepted' for positive feedback.

 Actual behavior: The feedback is not logged.

</td></tr><tr><td>

Now Assist Panel

 PRB1965617

 [KB2768233](https://hi.service-now.com/kb_view.do?sysparm_article=KB2768233)

</td><td>

Legacy Now Assist Portal doesn't load upon upgrade

</td><td>

The Now Assist panel bubble opens when selected, but the panel doesn't fully load. The interface remains stuck in a loading state, and no content is displayed to the user.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now User Experience

 PRB2038702

 [KB3134148](https://hi.service-now.com/kb_view.do?sysparm_article=KB3134148)

</td><td>

A scoped public UI page isn't accessible without a login unless 'Name' is used vs a scoped endpoint in a sys\_public record

</td><td>

It should be accessible without a login, so a user can complete the authentication from Outlook.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OAuth

 PRB2018183

</td><td>

The deny listed system property glide.oauth. jwt.token\_request .honor\_claim\_keys is included in an upgrade payload, resulting in a misleading 'skipped' upgrade log entry

</td><td>

During a Zurich upgrade, the system property glide.oauth. jwt.token\_request .honor\_claim\_keys \(from com.​snc.​platform.​security.​oauth\)​ appears as a skipped entry. This property is deny listed by design and therefore never loaded into sys\_properties on user instances.

</td><td>

1.  Navigate to **All** &gt; **Upgrade Center** &gt; **Upgrade History**.
2.  Open the record of upgrading in Zurich.
3.  Select the **Skipped Changes to Review** tab.
4.  Select the the skipped record for sys\_properties\_ 107762282f223210 3698319c003f9b2f.xml.

</td></tr><tr><td>

OneExtend

 PRB1985682

</td><td>

The **User** field is blank in the 'Generative AI Usage Logs' table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1998199

</td><td>

NAVA gets stuck intermittently

</td><td>

 

</td><td>

1.  Ensure Response Streaming is enabled.
2.  Open NAVA.
3.  Enter 'Creator.'

 Notice that NAVA will get stuck intermittently.

</td></tr><tr><td>

OneExtend

 PRB2010146

</td><td>

AI Agent user context isn't cleared out after the GenAI Skill call is completed

</td><td>

Records may be incorrectly marked as 'Updated by Now Assist'.

</td><td>

1.  Run any GenAI Skill from background.
2.  Update/create any record immediately after the GenAI Skill call.

 Observe that the record is incorrectly marked as 'Updated by Now Assist'.

</td></tr><tr><td>

OneExtend

 PRB2011330

</td><td>

The **Add as Update Set** button creates invalid update sets with updates in the wrong application scope in Zurich

</td><td>

Attempting to commit retrieved update sets between versions may fail in Zurich with errors such as, 'Cannot commit Update Set 'X' because: Update scope id 'A' is different than update set scope id 'B'. Resolve the problem before committing.'.

</td><td>

1.  Navigate to **Now Assist Admin** &gt; **Now Assist skills**.
2.  Open 'ITSM.
3.  Find the 'Case summarization' skill.
4.  Select **...** \(three dots\).
5.  Select **Make a copy of skill**.
6.  Navigate to **Now Assist Skill Kit** &gt; **Homepage**.
7.  In the section called X, find the copied skill.
8.  In the Prompt editor, change the prompts for three or four prompts.
9.  Save the changes.
10. In the Prompt editor, change the maximum response tokens for three or four prompts.
11. Save the changes.
12. At the top right of the form, select the down error by **Publish** and select **Add as Update Set**.
13. Open the resulting update set.

Notice that some of the records will have different scopes than the update set to which they belong.

14. Export the update sets to XML.
15. Import them as 'Retrieved update sets'.
16. Run the preview on the retrieved update sets.

Notice that there are errors such as, 'Cannot commit Update Set 'X' because: Update scope id 'A' is different than update set scope id 'B'. Resolve the problem before committing.'


 Expected behavior: The user should be able to move the update sets between environments without errors.

 Actual behavior: The user cannot successfully move the update sets between environments due to errors.

</td></tr><tr><td>

Password2 Encryption

 PRB2015257

 [KB2978056](https://hi.service-now.com/kb_view.do?sysparm_article=KB2978056)

</td><td>

There's excessive growth on the sys\_rollback\_incremental table and higher binlog generation due to 'Mass Encryption Job'

</td><td>

This causes a large increase in the disk space on the database server.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Password Reset

 PRB2011602

</td><td>

There are localization and text alignment issues on the password reset pages

</td><td>

These issues occur on the password reset identify, verify, success, confirmation, and reset pages.

</td><td>

1.  Provision an instance with any language plugin installed.
2.  On the login page, switch to the foreign language.

 Observe that there are some text alignment and localization-related issues on the password reset identify, verify, success, confirmation, and reset pages.

</td></tr><tr><td>

PDF Generation

 PRB1967954

 [KB2685208](https://hi.service-now.com/kb_view.do?sysparm_article=KB2685208)

</td><td>

PDF export from workspace isn't working for some related lists

</td><td>

The approver data isn't in PDFs exported from a record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Performance Analytics

 PRB2050693

</td><td>

injectWidgetContent re-executes already-loaded scripts via document.body.appendChild, causing a widget regression

</td><td>

injectWidgetContent in canvasUtils.js strips all &lt;script src&gt; tags from the widget HTML and re-injects them via document.body.appendChild. For scripts already loaded at page render time via Jelly &lt;g:requires&gt;, this causes re-execution, which corrupts initialized state and breaks widget functionality.

</td><td>

 

</td></tr><tr><td>

Performance Telemetry

 PRB2003266

 [KB2897634](https://hi.service-now.com/kb_view.do?sysparm_article=KB2897634)

</td><td>

Upgrade from Australia RTP to a later Australia release fails

</td><td>

The instance becomes stuck when upgrading from an Australia release to another Australia release \(for example, RTP to EA\). However, instances can upgrade from outside of Australia into Australia successfully \(for example, Zurich to Australia\).

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1984668

</td><td>

There's a column filter issue in the Data Visualization library page, in which the 'Does Not contain' isn't working on the 'Owner' column

</td><td>

Applying the 'Does not contain' filter on the 'Owned by' column does not filter the records properly.

</td><td>

1.  Navigate to the Data visualization library page.
2.  Apply the 'Does not contain' filter on the 'Owned by' column.

 Expected behavior: All the records should be filtered by the applied filter value.

 Actual behavior: It is not filtered properly when there are multiple values.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1996045

</td><td>

The 'Dashboard' view count isn't updating for Core UI dashboards when the execution time is 0ms

</td><td>

The job report 'View events' process appears to failing due to an undefined string being passed to it. There are errors after upgrading to Zurich.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2021236

</td><td>

In an instance migrated to Australia, reports display Name = None for non-global domains

</td><td>

When a instance with core UI reports is migrated to Australia, any reports that aren't in the global domain don't have the name set.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2037528

</td><td>

In Australia, data visualizations created by non-admin users aren't visible by that user on the 'Overview' page under Quick Access &gt; Created by me

</td><td>

 

</td><td>

1.  On an Australia instance, impersonate a non-admin user.
2.  Navigate to **Platform Analytics** &gt; **Data Visualizations** &gt; **Library**.
3.  Select **Create data visualization** to create a data visualization \(any type, any data source\).
4.  Navigate to **Platform Analytics** &gt; **Data Visualizations** &gt; **Library** &gt; **Overview**.
5.  Under 'Quick Access', select **Created by Me**.

Observe that the data visualization doesn't appear.

6.  Repeat the same as an admin user.

Note that the visualization does appear.


</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1843154

</td><td>

Not able to save a dashboard after editing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1988004

</td><td>

Platform analytics displays an incorrect view for the most recently viewed dashboards

</td><td>

The Recent Dashboards list includes dashboards that were not previously accessed. While actively using the instance, the list appears to update as the user opens certain dashboards. However, after logging out and logging back in, the Recent Dashboards list resets and once again displays dashboards that haven't been used.

</td><td>

1.  Open a base instance.
2.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Dashboards**.
3.  Open any dashboard.
4.  Select the **arrow** to view the Recent Dashboards list.

If this is the first login of the day, observe that the list contains dashboards that may not have been previously accessed.

5.  Switch between several dashboards.

Observe that the Recent Dashboards list updates to reflect the dashboards opened during the session.

6.  Log out of the instance.
7.  Log back in using a new browser tab.

 Observe that the Recent Dashboards list resets and displays a different, seemingly random list of dashboards instead of the ones previously accessed.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1993476

 [KB2961192](https://hi.service-now.com/kb_view.do?sysparm_article=KB2961192)

</td><td>

sys\_translated records are deleted unexpectedly when updating a tab name on a dashboard in Japanese

</td><td>

sys\_translated records are deleted from the sys\_translated table unexpectedly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1998900

 [KB3060060](https://hi.service-now.com/kb_view.do?sysparm_article=KB3060060)

</td><td>

Tab name translations find an incorrect translation value

</td><td>

Tab names may not be translated correctly in the Next Experience dashboard.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2000628

</td><td>

DashboardWidgetDao.update\(\) does not persist widget\_props field

</td><td>

When updating a dashboard widget record via DashboardWidgetDao.update\(\), the widget\_props field is not written to the par\_dashboard\_widget table. The create\(\) method correctly calls gr.setValue\(WIDGET\_PROPS, widget.getWidgetProps\(\)\), but the update\(\) method is missing this call. This causes widget-level property overrides \(for example, followFilters, header color, header title\) to be saved on initial widget creation but silently lost on any subsequent dashboard save.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2014857

</td><td>

Navigation to home.do doesn't redirect to the last visited CoreUI dashboard

</td><td>

An empty 'com.​snc.​par.​dashboards.​ui.​preferences' user preference causes incorrect redirection to the CoreUI dashboard.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2018222

</td><td>

The last visited dashboard isn't restored when the user selects the homepage logo

</td><td>

When selecting the top-left logo to return to the homepage, users are consistently redirected to the ITOM Licensing Dashboard instead of the last visited dashboard.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2025067

 [KB3092785](https://hi.service-now.com/kb_view.do?sysparm_article=KB3092785)

</td><td>

The sys\_translated record for par\_dashboard\_tab is overwritten

</td><td>

This can cause translations to be lost.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2033980

 [KB3129184](https://hi.service-now.com/kb_view.do?sysparm_article=KB3129184)

</td><td>

Text index processing delay on analytics\_​visualization\(column=​type\)​ after upgrading to Australia

</td><td>

After upgrading to Australia, the user observed increased processing times related to text indexing events on the 'type' column of the analytics\_visualization table. This results in a backlog of index events.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2050123

 [KB3131331](https://hi.service-now.com/kb_view.do?sysparm_article=KB3131331)

</td><td>

GlideClearDashboardCache is undefined in Australia, causing 4 business rules \(BR\) to fail on every Platform Analytics \(PA\) dashboard save and widget loss and save failures

</td><td>

The Java class GlideClearDashboardCache \(com.snc.par. dashboards.glide.script. ClearDashboardCache, annotated @GlideScriptable\) isn't registered in the Rhino scripting scope. The class is present in the com.snc.par.dashboards OSGi bundle JAR, but isn't accessible as a Rhino scriptable — typeof GlideClearDashboardCache returns undefined. Four business rules in com.snc.par.dashboards call this class with no try/catch on every INSERT, UPDATE, and DELETE against par\_dashboard, par\_dashboard\_canvas, par\_dashboard\_widget, and par\_dashboard\_permission. When a user saves a PA dashboard, these BRs throw RhinoEcmaError: 'GlideClearDashboardCache' isn't defined \(logged as WARNING in the node log, firing 14+ times per transaction\). Two failure modes: \(1\) dashboard save fails with 'Your dashboard could not be saved', or \(2\) save succeeds but in-memory cache not flushed — stale canvas layouts cause widgets to disappear from tabs on subsequent loads.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1972851

</td><td>

Hide the info message if 'com.​glide.​par.​coreui\_​single\_​migration.​enabled' property is 'false'

</td><td>

 

</td><td>

1.  Create CoreUI dashboard \(pa\_dashboards\).
2.  Add Dynamic content block to it.
3.  Set 'com.​glide.​par.​coreui\_​single\_​migration.​enabled' system property to 'false.'

 Expected behavior: The info message should be hidden

 Actual behavior: The info message is shown.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2031469

</td><td>

The automatically triggered Core UI dashboard migration can cause an out of memory error and instance outages

</td><td>

After an Australia upgrade, the Core UI dashboard migration is triggered when a user loads the dashboard and the 'Do not migrate in bulk' \(no\_bulk\_migration\) field is set to false. **The** field default value is false, so any dashboard that isn't migrated is triggered to migrate when it's viewed.

</td><td>

 

</td></tr><tr><td>

Platform Runtime

 PRB1995562

</td><td>

Session lock leak when the SSL connection closes during async transaction processing

</td><td>

When an SSL/TLS connection closes while Tomcat is reading POST body parameters for an /xmlhttp.do request, Tomcat's Request.parseParameters\(\) silently catches the IOException. The transaction is created and queued with a dead connection. When worker threads attempt to claim the transaction, response.isCommitted\(\) throws IllegalStateException \(response recycled\), causing a cancellation. All subsequent transactions for the same session fail identically, leaving the session blocked until it times out \(for example, after 6 hours\). Instead, dead connections should be detected before transaction creation, or failed claims should invalidate the corrupt session to unblock subsequent transactions.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1999600

</td><td>

Playbook with questionnaire activity is not activated by default in Yokohama instances

</td><td>

When apps are uploaded from Nexus or from a zip file, and they contain playbooks with questionnaire activities, those playbooks are missing trigger data. When a playbook has a questionnaire activity, a line gets added to the XML that causes everything after that line to fail to load.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2009677

</td><td>

The complex object's format is different for playbook output/input

</td><td>

The flow gives an 'com.snc.process\_ flow.exception. ProcessAutomationException: Could not serialize value' error when running playbook.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1793351

</td><td>

Security restricted for the script include 'GlideEntitlementAPI' from the scope 'Predictive Intelligence for Flow Designer'

</td><td>

The user is utilizing Prediction Intelligence within a the flow 'Predictive Int. for INC - Service v2'. On testing the flow, the prediction message shows, '404: Prediction Failed with error: java.​lang.​Null​Pointer​Exception:​ Cannot invoke 'java.​lang.​Boolean.​boolean​Value\(\)​' because 'o' is null. Please contact Support for Additional Assistance.'.

</td><td>

 

</td></tr><tr><td>

Problem Management

 PRB2018009

 [KB2985638](https://hi.service-now.com/kb_view.do?sysparm_article=KB2985638)

</td><td>

An ACL is reverted to true after an upgrade

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Project Management

 PRB1980002

</td><td>

There's an report\_view ACL error for a few widgets

</td><td>

 

</td><td>

Open **Execution Dashboard** &gt; **Data Quality** tab in Strategic Planning workspace.

 Observe a report\_view ACL error for the 'No Planned Cost' and 'No Planned benefit' widgets.

</td></tr><tr><td>

Related Lists

 PRB2000158

 [KB2823064](https://hi.service-now.com/kb_view.do?sysparm_article=KB2823064)

</td><td>

Related lists do not show row data

</td><td>

Related lists do not show row data in list cells \[Core UI\].

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Related Lists

 PRB2025356

 [KB3032264](https://hi.service-now.com/kb_view.do?sysparm_article=KB3032264)

</td><td>

User can't add records in a related list because of the strict ACL check and missing ACLs for required roles

</td><td>

Users with missing ACLs are not able to add new records in the related list due to a strict ACL check.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Request Management

 PRB1973824

 [KB2815909](https://hi.service-now.com/kb_view.do?sysparm_article=KB2815909)

</td><td>

Added approvers names don't appear on the Approver list of Request and RITM

</td><td>

When adding approvers to a Request \(REQ\) or Requested Item \(RITM\) via the Multi-Row Add \(MRA\) component in the Related Records section of Service Operations Workspace \(SOW\), a success message is displayed confirming that the approvers have been added. However, the Approver list doesn't display the newly added approver names. Similarly, when attempting to add approvers from the UI16 related list, the approvers aren't added.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Resource Management

 PRB1925690

</td><td>

An influx of events are generated 'resource\_daily\_hours.changed'

</td><td>

Whenever updates are happening on the 'resource\_plan' table via any job, an influx of 'resource\_daily \_hours.changed' events are generated, and it's impacting the events processing in the default queue.

</td><td>

UPDATE the resource\_plan table.

 See an influx of 'resource\_daily \_hours.changed' events generated.

</td></tr><tr><td>

Resource Management

 PRB2003945

</td><td>

Cost plan breakdowns are duplicated

</td><td>

When the user changes the start date and end date from a resource plan, the business rule \(BR\) Update​Cost​Plan​Associated​To​Resource​Plan launches an event. The BR 'Recreate Requested Allocations' is also launched, updating the resource plan again and changing the planned cost. In summary, when the user updates the dates, the system updates the resource plan twice, one time for the dates and another for the planned cost, practically at the same time. Both changes trigger the BR Update​Cost​Plan​Associated​To​Resource​Plan and two events are created. Since there are two events in the system, they will try to perform the same action, and this could lead to problem concurrency. The two events are processed at the same time and the cost plan breakdowns are created twice.

</td><td>

1.  Navigate to pm\_project.list.
2.  Open the project where the duplicated cost plan breakdowns were created.

</td></tr><tr><td>

REST API Framework

 PRB2003629

 [KB2934340](https://hi.service-now.com/kb_view.do?sysparm_article=KB2934340)

</td><td>

The user is unable to accurately track response size \(egress data\) for inbound API calls made by integrations

</td><td>

This issue was observed in production instances on Yokohama or Zurich. The user cannot determine if their usage is accurate for API Access Volume and Workflow Data Fabric usage when using the Integration Hub Usage Dashboard and Workflow Data Fabric Usage Dashboard.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Roles

 PRB2001499

</td><td>

There's a role sys\_id mismatch as a masking configuration is using glide\_list

</td><td>

 

</td><td>

Create a masking configuration with the itil role.

 When the masking configuration is installed in a previous instance, there's a sys\_id mismatch of the itil role in the instance and the shipped configuration.

</td></tr><tr><td>

Roles

 PRB2023810

</td><td>

Instances without explicit roles throw an error when invoking agents with a 'Nobody' role mask

</td><td>

The following error appears in the logs: 'Role 'snc\_external' not found. Cannot be automatically created: no thrown error'.

</td><td>

1.  Open an instance that doesn't have the explicit roles plugin.
2.  Trigger an AI Agent that has a role mask on the **Nobody** field.

 Observe the error in the logs: 'Role 'snc\_external' not found. Cannot be automatically created: no thrown error'.

</td></tr><tr><td>

Scheduled Jobs

 PRB2031347

</td><td>

Scheduled templates loop an excessive amount of times on due to a UTC midnight boundary issue with 'Week in Month' scheduling in a UTC+ timezone

</td><td>

When the first Monday coincides with the first day of the month, the scheduler triggers the job multiple times until 12:00 AM GMT, resulting in duplicate executions.

</td><td>

 

</td></tr><tr><td>

Scripting Governance Tool

 PRB1967275

</td><td>

Unable to remove the 'snc\_​required\_​script\_​writer\_​permission' role from users in a domain separated instance

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Scripting Governance Tool

 PRB2013370

</td><td>

There's a unique constraint error when assigning roles/groups containing snc\_required\_ script\_writer\_permission

</td><td>

When assigning roles or groups that include the snc\_​required\_​script\_​writer\_​permission role \(directly or indirectly\), the system throws a unique constraint error. This occurs when auto-provisioning in Scripting Governance is turned on.

</td><td>

 

</td></tr><tr><td>

Security Data Filters

 PRB1967733

</td><td>

A security data filter \(SDF\) is applied redundantly via dotwalk paths, causing missing records in 'OR' queries

</td><td>

This has two distinct symptoms caused by the same underlying duplication. One, when querying a parent table with 'OR' conditions dotwalking into multiple child tables simultaneously, the parent SDF was applied three times — once directly and once per dotwalk CE path — producing conflicting conditions that returned 0 records instead of the expected results. Two, when querying a table with a field-based SDF, records where that field was empty/null were incorrectly excluded. This was caused by the same SDF being applied redundantly via a dotwalk CE, which caused the combined filter condition to exclude null matches.

</td><td>

 

</td></tr><tr><td>

Seismic Framework

 PRB1972265

</td><td>

Ancestor path retains the parent element using hard references and can make small memory leaks larger, depending on retention

</td><td>

In some cases, the retainer is the variable ANCESTOR\_PATH, as it holds on to hard references to the ancestor elements. Since elements in the ancestor path are retained, it may make a small leak larger if the elements themselves are large in nature \(lists, forms, client state data brokers, etc.\).

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1994381

 [KB3006010](https://hi.service-now.com/kb_view.do?sysparm_article=KB3006010)

</td><td>

Discovery has issues on some node after upgrading in Australia

</td><td>

After upgrading to Australia, JavaScript running in app nodes fails to call Java functions. The following warning appears: '\*\*\* WARNING \*\*\* Evaluator: com.​glide.​script.​Rhino​Ecma​Error:​ undefined is not a function.' This impacts various features, including Discovery and Event Management.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Server-side scripts

 PRB2022176

</td><td>

The script name should be logged when a page title is unavailable in the 'Guarded Scripts' list entry

</td><td>

The page title can be empty in some cases, such as a scheduled job and probably more. It should become the script name if there isn't a page name that makes sense.

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB2008409

 [KB3116170](https://hi.service-now.com/kb_view.do?sysparm_article=KB3116170)

</td><td>

Label-type variables aren't available for selection in a UI policy action within Catalog Builder

</td><td>

A label-type variable isn't available for selection in UI policy actions within Catalog Builder, whereas the same label variable is available in UI policy actions in 'Maintain Items'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Components

 PRB1999964

</td><td>

Null/No entries for some of the questions in selected items MRVS breaks the case record page \(platform and workplace central\)

</td><td>

A workplace case form \[UI16\] breaks when entries in sc\_multi\_row\_question\_answer are missing for one or more questions for selected items.

</td><td>

 

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB2018000

</td><td>

Performance issues with the Employee Center Standard Ticket Page Widget

</td><td>

This issue was observed in Australia, but the function works as expected in Zurich. This impacts the Service Portal 'Standard Ticket Header Widget.' The user observed that the RITM 'Show details' drop-down list alignment is off, and the REQ 'Show/Hide Details' drop-down list button option is shown even if there are no additional details to show.

</td><td>

1.  Open the Employee Center Portal \(ESC\).
2.  Submit a Request.

On the standard ticket page, observe that the **Show/Hide Details** button is shown even if there are no additional details to show.

3.  On the 'Requested items' tab, select on **RITM** number.

Notice that it will redirect to the standard ticket page for the RITM.


 Expected behavior: The RITM alignment is aligned without padding-left at 0px.

 Actual behavior: The RITM**Show details** button alignment is off, and the REQ **Show/Hide Details** drop-down list button option is shown even if there are no additional details to show.

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB2029227

</td><td>

Service Portal glide.​ui.​activity\_​stream.​style.​comments has a visual error after upgrading to Australia

</td><td>

When the sys\_property 'glide.​ui.​activity\_​stream.​style.​comments' is set to any color, the bar becomes taller than the parent element, making it overflow.

</td><td>

1.  Open an Australia instance.
2.  Change the sys\_property 'glide.​ui.​activity\_​stream.​style.​comments' from transparent to any color.
3.  Navigate to the Service Portal.
4.  Open any incident.

 Expected behavior: The comment section has a bar in the color that was chosen. It's the same size as the**Comment Input** field.

 Actual behavior: The comment section has a bar in the color that was chosen, but it's taller than the**Comment Input** field, making it overflow.

</td></tr><tr><td>

Service Catalog

 PRB1972924

</td><td>

The **Generate sequence** UI action gives a missing start rule error on Playbook 28.2.1

</td><td>

This issue was observed in Playbook 28.2.1, but not in 28.0.8.

</td><td>

1.  Open any order guide.
2.  Generate the sequence.
3.  Open the playbook created.

 Observe the missing start rule errors.

</td></tr><tr><td>

Service Mapping

 PRB1972871

</td><td>

There's a memory impact by the query in 'Service Mapping - Traffic Process to Process'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal Core Widgets

 PRB1819286

</td><td>

When updating the font-family in the EC theme, it doesn't update the font in the AI search results page

</td><td>

According to the 'Theming for AI Search in Service Portal' documentation, users can control the look and feel of AI search results. The user was attempting to update the default font family of the EC theme from Lato, Arial, sans-serif, to 'Segoe UI', sans-serif . When updating the EC theme CSS properties, this changed the font on the home page as expected, but failed to change font in the AI Search results page. Also, the faceted search widget doesn't change and was still using Lato, Arial, sans-serif.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1979009

 [KB2817350](https://hi.service-now.com/kb_view.do?sysparm_article=KB2817350)

</td><td>

Catalog items' M2M category user criteria aren't considered in late binding

</td><td>

The Service Catalog is split by company, with some items viewable for some companies, and some for more than one. One form that should be visible to two companies doesn't display in the Service Portal search. The form is available for both companies and is in two categories. It can be seen in 'Services' by some users, but it doesn't appear in search results for the other company's users.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1999839

 [KB2983856](https://hi.service-now.com/kb_view.do?sysparm_article=KB2983856)

</td><td>

When Multi-factor Authentication \(MFA\) and Password Needs Reset is true, the password reset workflow refreshes after selecting **Submit** on the initial login and redirects to the backend Platform UI

</td><td>

When MFA is configured on an instance and Password Needs Reset is set to true on a vendor contact record, they are presented with a screen to change their password on initial login. After changing the password on the initial screen and selecting submit, the page refreshes back to the same password reset screen. If they perform the same steps again and select submit, they are finally redirected but the redirect is incorrect and redirects the user to the backend UI.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB2006596

</td><td>

Tooltips of Cart and Tours are not hoverable

</td><td>

Pointer hover over the **Cart** button triggers the tooltip, but when the pointer is moved over the tooltip, the tooltip disappears.

</td><td>

 

</td></tr><tr><td>

Service Portfolio Management

 PRB2029361

</td><td>

The 'Outage calculation' business rule is not working when the date format is set to DD/MM/YYYY

</td><td>

**The Duration** field is not calculating correctly because the 'Outage Calculation' business rule does not work when the date format is set to DD/MM/YYYY.

</td><td>

 

</td></tr><tr><td>

Session Management

 PRB1950133

</td><td>

The guest user's language isn't displayed on the log in page in Zurich

</td><td>

After setting the 'guest' user language to Japanese, the log in page should be displayed in Japanese but is displayed in English.

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1996759

</td><td>

Null check for threadMember is incomplete for CollabMessageDto

</td><td>

The user can send a message but it's greyed out in the chat window until the user refreshes. The last sent message in a collab chat record doesn't update, so the discussion card in the utility menu never updates.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Plugin Framework

 PRB1788390

</td><td>

Software Asset Management \(SAM\) Discovery Model to Software Model matching fails when Discovery Models are corrupted

</td><td>

The job should not fail because of the few corrupted discovery records, and should handle the corrupted records and finish processing other software models and discovery models.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2018383

 [KB2986694](https://hi.service-now.com/kb_view.do?sysparm_article=KB2986694)

</td><td>

A Microsoft per‑core license metric isn't visible after a Zurich or Australia upgrade

</td><td>

The MS per core metric was moved from the apply\_once folder to the update folder. The fix script to set the metric group was overwritten, since the update folder file insert ran after. Thus, the MS per core uploaded with no metric group.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Standard Ticket Page

 PRB2000629

 [KB3153782](https://hi.service-now.com/kb_view.do?sysparm_article=KB3153782)

</td><td>

There's issues when sending a reply to a ticket from Service Portal

</td><td>

When the user sends a reply in the Service Portal via widget, the text field isn't cleared after the user selects the **Post** option.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Archiving

 PRB1890304

</td><td>

Users can't uninstall a custom or store application with archive records \(sys\_archive\)

</td><td>

A user with admin rights can't uninstall the custom or store app because the uninstall can't delete the sys\_archive records.

</td><td>

1.  Create a custom app \(or use a store app\).
2.  Enable data archiving for a table in the app.
3.  Ensure that there are multiple archive runs moving data from the table to the archive table ar\_table.
4.  Try to uninstall the custom or store app.

 Observe that a user with admin rights can't uninstall the app. The uninstall can't delete the sys\_archive records until a workaround is applied.

</td></tr><tr><td>

System Events

 PRB1969068

</td><td>

The 'Events process 0' job yields to memory pressure, causing event processing delays

</td><td>

When node memory pressure is high \(live set ≥ ~91%\), the JobYieldCheck mechanism triggers a yield on events process 0 despite it being a priority 25 \(high priority\) job. High-priority jobs should not be subject to automatic yield throttling, as this directly delays critical event processing and can result in P1 incidents. The memory pressure itself may be transient or difficult to diagnose quickly — heap dumps often show no obvious culprit, and identifying the root cause of elevated memory usage takes time. During that window, events process 0 is repeatedly yielded, stalling event processing pipelines that users depend on for time-sensitive operations. JobYieldCheck WARNING Job=events process 0 yields due to memory pressure logged on affected nodes. Node memory is sustained at 91–93% of max, with live set at ~91.44% \(~1.28GB\). glide.memory.watcher logs no active transaction warnings alongside persistent memory pressure status = true. There's only a single job visible in the queue during the yield window, yet throttling still triggers. However, users expect priority 25 jobs \(events process 0\) should not be yielded under memory pressure conditions. Yield throttling should be restricted to lower-priority workloads.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2003217

</td><td>

Fix behavior of event processing tables during the clone operation and clean up invalid records/jobs during the clean up script

</td><td>

During cloning on Zurich instances, events processing framework tables' configuration aren't preserved, causing errors in transaction logs due to orphan records for events jobs. An orphan record occurs when a sys\_trigger record exists for an event processing job, but the corresponding entry in the sys\_processing\_framework\_job table is missing. This causes the ProcessingFrameworkJob to fail when attempting to retrieve the scheduled job context. Log example: 'ProcessingFrameworkJob SEVERE ProcessingFramework &gt; Failed to get the schedule job context'.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2003586

</td><td>

A database \(DB\) CPU spikes to 76% due to a slow sysevent 'UNION ALL' query on flow.fire events triggered by an SLA breach processing at 14k incidents/hr

</td><td>

During a combined load test generating 14,000 incidents/hr \(7k/hr via Event Management + 7k/hr via ITSM SOW\), the DB host CPU spiked sharply to 76% at approximately 00:30–00:45 UTC on 2026-03-17. The spike is correlated with a high-frequency, slow-executing SQL query scanning all sysevent partition tables \(sysevent0000–sysevent0006\) via a 7-way 'UNION ALL', issued by the Flow Engine's MonitorOperation while polling for SLA breach flow events.

</td><td>

 

</td></tr><tr><td>

System Export Sets

 PRB1835154

</td><td>

Improve retry logic in POST API from MID server LES Consumer to Customer REST endpoint

</td><td>

Currently, the infinite retry doesn't work for different status codes. This needs to be modified \(for example, to support 201 and 204\).

</td><td>

 

</td></tr><tr><td>

Table Administration and Data Management

 PRB2032949

</td><td>

Shadow table alter failing and retrying in loop

</td><td>

'Fix Shadow Table Schema' job triggers alter on shadow tables fail and retry in a loop.

</td><td>

 

</td></tr><tr><td>

Table Cleaner

 PRB1821147

 [KB2480543](https://hi.service-now.com/kb_view.do?sysparm_article=KB2480543)

</td><td>

Archive Destroy Log\[sys\_archive\_destroy\_log\] table cleanup doesn't work as the table cleaner rule is disabled by default

</td><td>

The table cleaner rule for sys\_archive\_destroy\_log table is disabled by default in an instance. For instances that have entries in sys\_archive\_destroy\_log, cleanup doesn't work as this table cleaner is disabled.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Table Cleaner

 PRB2001569

</td><td>

Long running queries from com.​glide.​dm\_​job.​table\_​cleaner.​Table​Cleaner​Producer cause significant DB CPU spikes on Raptor DB Pro instances

</td><td>

The HexCleanerProducerValidator lacks a guard against dot-walk conditions. Combined with recursive count-estimation logic and unbounded MIN\(sys\_id\) aggregates, this leads to the creation of aggregate queries on massive tables.

</td><td>

 

</td></tr><tr><td>

Table Rotation

 PRB1954428

 [KB2590667](https://hi.service-now.com/kb_view.do?sysparm_article=KB2590667)

</td><td>

Table rotation creates too many 'Online Alter Truncate Delayed Drop Table' entires in sys\_trigger to be executed in a short span of time

</td><td>

The syslog and extended tables are supposed to be rotated weekly, which means it switches to the next rotation in the schedule and also truncates future rotation to make it available for the next week.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Tables and Columns Data Dictionary

 PRB1773296

</td><td>

For a DocumentID type field, there's no option to specify reference\_cascade\_rule

</td><td>

Cascade delete doesn't work for DocumentID type fields the same way it works for the reference fields.

</td><td>

 

</td></tr><tr><td>

Tags

 PRB2039548

</td><td>

In Australia, tags aren't saved for 'active = false' records for non-admin users

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Time Card Management

 PRB1988000

 [KB2760220](https://hi.service-now.com/kb_view.do?sysparm_article=KB2760220)

</td><td>

Managers are no longer able to add time cards for their direct reports and delegates in the Time Sheet Portal

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Time Card Management

 PRB2051508

 [KB3139332](https://hi.service-now.com/kb_view.do?sysparm_article=KB3139332)

</td><td>

The user.manager field shows as empty when opening the 'Pending Approval' module for Time sheets

</td><td>

The filter is emplty for the user.manager field.

</td><td>

1.  Impersonate a user with submitted time sheets.
2.  Navigate to **Time Sheet** &gt; **Pending Approval**.

 Notice that the filter shows empty for **User.Manager**.

</td></tr><tr><td>

Time-Limited User Roles

 PRB1972197

</td><td>

When a user is logged in, updating an existing record with a new end time in the 'Time limited user roles' table causes never ending information messages on all pages

</td><td>

 

</td><td>

1.  Open a Zurich instance.
2.  In a separate browser or incognito window, log in with a user that has an 'itil' role.
3.  In another window, log in with a user who has an 'admin' role.
4.  With the admin user, navigate to **All** &gt; **User administration** &gt; **Time-limited roles**.
5.  Create a record that grants an 'admin' role to the user.
6.  With the user that had only an 'itil' role but received the 'Time limited admin' role, open an incident list and then a record.

 Expected behavior: Users see an information message once.

 Actual behavior: Users see a message about roles that are granted or removed, but closing them isn't helping.

</td></tr><tr><td>

Transaction Management

 PRB2031636

 [KB3141646](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141646)

</td><td>

When a semaphore is loaded via plugin extension point, the queue depth limit is set wrong and the semaphore's load\_stats saturation value will always report 1 instead of the correct value

</td><td>

The saturation value should not always be one because saturation should reflect the amount of work queued in CsHybridQueue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Actions

 PRB1995906

</td><td>

The dependent field is updated by a flow that appears blank in workspace

</td><td>

Confirmation on the task - CSTASK1336675 This issue could be intermittent, needs to be replicated thoroughly.

</td><td>

1.  Create a UI Action in a table which has a dependent field \(for example, **State** and **Sub State**\).
2.  Make sure the UI Action sets the 'State' and 'Sub State' values when selected.
3.  Create two flows that trigger when the record is updated.
    -   Flow one is triggered when the 'State' value is changed by the UI Action. It also changes the state.
    -   Flow two is triggered when the 'State' value is changed by flow one.
4.  Open the record on which the UI Action and flows are created.
5.  Select the UI Action.

 Observe that the **Sub State** field is empty in workspace.

</td></tr><tr><td>

UI Field Administration

 PRB1926469

</td><td>

The contrast ratio of the focus indicator on the search suggestion item of the combo box is less than 3:1

</td><td>

 

</td><td>

1.  Open any instance.
2.  Navigate to **All** &gt; **Incident** &gt; **All** &gt; **New**.
3.  Navigate to the 'Caller' combo box and type in it.
4.  When the search results appear, navigate to them.
5.  Verify the contrast ratio of the focus indicator.

 Expected behavior: The contrast ratio of the focus indicator on the search suggestion item of the combo box should be equal to or greater than 3:1.

 Actual behavior: The contrast ratio of the focus indicator on the search suggestion item of the combo box is less than 3:1.

</td></tr><tr><td>

UI Field Administration

 PRB1962435

</td><td>

There's an incident form load issue due to the missing macro sn\_wwna\_nacm\_component, which causes a performance issue

</td><td>

When loading an incident form, the local host log is consistently flooded with the 'DBMacro WARNING \*\*\* WARNING \*\*\* Macro missing: sn\_wwna\_nacm\_component', and this is causing the form to load slowly.

</td><td>

1.  Open any incident record in the instance.
2.  Navigate to **System Diagnostics** &gt; **Session Debug** &gt; **Enable All**.

 Observe the error in the localhost log, users notice the warning called many times: 'DBMacro WARNING \*\*\* WARNING \*\*\* Macro missing: sn\_wwna\_nacm\_component'.

</td></tr><tr><td>

UI Field Administration

 PRB1969665

</td><td>

Currency values change automatically in workspaces

</td><td>

The currency value changes automatically when selecting in and out of the **Currency** field, without actually changing the value.

</td><td>

1.  Open any record from incident.list.
2.  Select **View - Service Operations Workspace**.
3.  Create a field type 'price'.
4.  Give it any name and any value.
5.  Save the record.
6.  Open sys\_user table for the name 'Beth Anglin' who has 'ITIL' role.
7.  Add a **County Code** field with the value set to 'system\(US\)'.
8.  Impersonate the user Beth Anglin.
9.  Open Service Operations Workspace.
10. Select into the **Price** field under the 'Details' tab.
11. Without changing anything, select out of the field.

Notice that the value doesn't change.

12. End the impersonation.
13. Update the **County Code** field to 'Germany' or any other country for the user Beth Anglin.
14. Impersonate the user Beth Anglin again.
15. Open Service Operations Workspace.
16. Select into the **Price** field under the 'Details' tab.
17. Without changing anything, select out of the field again.

 Observe that the value changes.

</td></tr><tr><td>

UI Field Administration

 PRB1998819

</td><td>

WWNAglobal utils should be removed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1825264

</td><td>

A cursor jumps in the subject line when composing an email in Workspace

</td><td>

There's an issue with the cursor jumping to the end of the line while writing/editing the subject line when composing an email in an Workspace. The cursor jumps when editing the subject line and not the the body of the email.

</td><td>

1.  Log in to any instance.
2.  Navigate to Customer Service Management \(CSM\) Configurable Workspace.
3.  Open any case.
4.  Select **Compose Email**.
5.  Select the **Subject** field.

 See that the cursor jumps randomly to the end of the subject field.

</td></tr><tr><td>

UI Form Administration

 PRB1971299

</td><td>

When leaving an unsaved task, the pop-up modal shows the incorrect component name

</td><td>

When the user access a UI16 form from a dashboard page, then leaves the form without saving changes, a confirmation modal is displayed. The first letter of the 'component or element' is trimmed in the modal.

</td><td>

1.  Log in to an instance.
2.  Navigate to a dashboard that has a data visualization component.
3.  Access the component.
4.  Navigate to the form record.
5.  Make some changes in the form, but don't save it.
6.  Select the **B** &gt; **ack**button on the form \(not the browser **Back** button\).

 Expected behavior: A confirmation modal is displayed with the text: 'Do you want to save changes to Critical Task assigned before leaving this page? Your changes will be lost if you leave now.'

 Actual behavior: A confirmation modal is displayed with the text: 'Do you want to save changes to ritical Task assigned before leaving this page? Your changes will be lost if you leave now.'.

</td></tr><tr><td>

UI Form Administration

 PRB1993929

 [KB2908761](https://hi.service-now.com/kb_view.do?sysparm_article=KB2908761)

</td><td>

RCAs are created with the source as 'sys\_ws\_operation.do? sys\_​id=​6986d96dff7322102ae8ffffffffff48' for HR apps

</td><td>

An RCA is generated: 'RCA triggered - 'Read operation on table 'sn\_doc\_html\_template' from scope 'Global' was denied. The application 'Document Templates' must declare a Restricted Caller Access privilege. Please contact the application admin to update their access requests'. None should be generated.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1998771

 [KB2898934](https://hi.service-now.com/kb_view.do?sysparm_article=KB2898934)

</td><td>

Installing the com.glide.ai\_record\_activity plugin doesn't create the sys\_ai\_record\_activity table, causing NullPointerException errors

</td><td>

The user observes errors getting records for sys\_ai\_record\_activity: java.​lang.​Null​Pointer​Exception.​

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB2006958

</td><td>

Introduce system property to hide form level TI banner

</td><td>

The alert appears when the form is loaded. There's no way to avoid seeing the alert if not required.

</td><td>

1.  Open a SOW record with **Task Intelligence** field level recommendations.

Notice that the form level banner appears with deep links to fields that have recommendations.

2.  Cancel the alert.
3.  Load the form.

 Observe that the alert appears again.

</td></tr><tr><td>

UI Form Administration

 PRB2019275

</td><td>

There's layout and scrollbar flickering when entering info, internal and external, in HTML **Journal** fields

</td><td>

There's layout and scrollbar flickering when entering info, internal and external, in HTML **Journal** fields, caused by automatic browser window resizing. The issue occurs randomly and is not related to a specific case or text size.

</td><td>

1.  Change the glide.ui.journal.use\_html system property to true.
2.  Open any incident in any workspace.
3.  Type multiple lines in internal info or copy/paste some text until the scroll bar appears.
4.  Remove enough lines so that it's one new line away from displaying the scroll bar.
5.  Type some words randomly to add enough words to create a new line.

 Observe the flickering issue.

</td></tr><tr><td>

UI Form Administration

 PRB2020457

</td><td>

There's a false error for a strict read-only 'Currency' column when the numeric value is 1000 or larger

</td><td>

Additional formatting like commas or decimals are added to **Currency** fields on the client side form initialization, which makes the field appear as modified on update. This issue is present when: 1. a field of type currency is visible on a form, 2. **The** field has a read\_​only\_​option=​strict\_​read\_​only,​ and 3. The numeric value of a field is 4 digits or greater.

</td><td>

1.  On any table, create a field of the type **Currency**.
2.  Create an on insert business rule to set the value of the field to USD: 1000.
3.  Save the record.
4.  Modify a different field on the form and save.

 Expected behavior: The record is updated without any error messages.

 Actual behavior: An error message stating updates to columns 'depreciated\_amount' and 'residual' were ignored.

</td></tr><tr><td>

UI Form Administration

 PRB2023067

</td><td>

The UI Section doesn't show the mandatory asterisk in UI16

</td><td>

Sections that contain a mandatory field \(set by the UI policy\) should have an asterisk.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2033143

 [KB3139369](https://hi.service-now.com/kb_view.do?sysparm_article=KB3139369)

</td><td>

The 'Preview this record' icon isn't working in the Safari browser

</td><td>

Selects on the button components and controls aren't working in Safari for UI16. This issue is only reproducible in the Safari browser. Non-Safari browsers aren't impacted and they don't face this issue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Upgrade Center

 PRB1889947

</td><td>

Instance nodes do not appear and this error appears: javax.​crypto.​AEADBad​Tag​Exception:​ Error finalising cipher data: mac check in GCM failed

</td><td>

Instance JVMs won't start after the error, ' java.io.IOException: javax.​crypto.​AEADBad​Tag​Exception:​ Error finalising cipher data: mac check in GCM failed'.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB1950446

</td><td>

The 'Flow Designer' module directs to 'Page Not Found' after an instance upgrade on some nodes

</td><td>

The Process Automation &gt; Flow Designer module redirects to 'Page Not Found' on some nodes after an instance upgrade. The main issue is that nodes tried to download app packages from Store, but Store responded with a 400 error because the platform version for the instance isn't updated on the Store end yet, and the request is considered incompatible. However, during an upgrade, it shouldn't request app packages from Store.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB2016580

</td><td>

After upgrading instances from Zurich to Australia, several records show up on the skipped list belonging to the sn\_glider or sn\_build\_agent with error 'Unable to compare, unable to find a current record'

</td><td>

After upgrading a Zurich instance to Australia the upgrade monitor will have a list of skipped records. But when trying to resolved issue, users observe the error: 'Unable to compare, unable to find a current record' when trying to compare to current.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Upgrade Center

 PRB2023239

 [KB3015307](https://hi.service-now.com/kb_view.do?sysparm_article=KB3015307)

</td><td>

There is a mismatch in the Glide version between the app node and the database following an upgrade

</td><td>

A new code path introduced the MariaDBI18NSQLFormatter class. When the sys\_properties record of the 'com.glide.db.session \_language\_collation\_feature' property is set to true, it takes a code path upon upgrade or restart where an instance will not come up. When 'com.glide.db.session \_language\_collation\_feature' is false, the code path exits early and doesn't cause this issue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UXF Macroponent

 PRB2009619

</td><td>

Multiple stuck threads cause semaphore exhaustion, requiring a node restart

</td><td>

There's a stuck semaphore transaction related to the function create​Cacheable​Page​Fragment​From​Shell in Cacheable​Page​Fragment​Factory.​java.​ This can lead to multiple threads being stuck with no option but to restart the node to provide relief.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1966018

</td><td>

On a slow network, sometimes the record details appear in the 'List' tab

</td><td>

The issue occurs if the user opens a record and quickly switches back to the list tab in CSM Configurable Workspace.

</td><td>

1.  Open any Zurich base instance.
2.  Open CSM Configurable Workspace.
3.  On a Google Chrome browser, select F12.
4.  Navigate to **Network tab** &gt; **3G Throttling**to simulate a slower network.
5.  Navigate to 'Lists'.
6.  Open any list, such as 'Problem records'.
7.  Open a problem record so a new tab opens.
8.  Quickly switch back to the 'Lists' tab.

 Observe that the problem record details load in the 'Lists' tab.

</td></tr><tr><td>

UX Framework

 PRB1969085

</td><td>

GraphQL schema changes for client-interaction.graphl in ux-metrics

</td><td>

The user sees error logs from the ClientMetricsRestService.java file. The error logs are logged to the syslog table.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1986291

 [KB2956365](https://hi.service-now.com/kb_view.do?sysparm_article=KB2956365)

</td><td>

List dynamic routing shouldn't be applied when creating a record from a related list

</td><td>

Dynamic routing is handled within the recordRoutesMapping Client Script Include. Kb\_knowledge mapping uses source\_component: 'list' to route article selects to kb\_view. When the **New** button is selected on a related list, the kb\_view route is incorrectly applied. Since kb\_view can't handle new records, the page breaks.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB2002003

 [KB2901692](https://hi.service-now.com/kb_view.do?sysparm_article=KB2901692)

</td><td>

Stuck semaphore due to the call Glide​Ux​Interoperable​Routes​Provider.​get​Interoperable​Routes​By​Ids\(\)​

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB2027095

 [KB3102030](https://hi.service-now.com/kb_view.do?sysparm_article=KB3102030)

</td><td>

The latest component asset isn't selected when multiple asset associations exist in sys\_​ux\_​lib\_​component\_​m2m\_​asset,​ which impacts AI summary cards on UI Builder workspaces

</td><td>

When the AI summary card component was upgraded, its asset name changed from now-ai-summary-card/index to uxc-generative-ai/index. The upgrade doesn't clean up the old asset association, so the sys\_ux\_lib\_component\_m2m\_asset table ends up with two associations for the same component \(old and new asset\). The component-to-asset selection query in Glide​Ux​Component​Def​Provider.​get​Asset​Names​By​Component​Sys​Ids\(\)​ had no ordering and relied on default DB ordering. When duplicate associations exist, this could return the stale now-ai-summary-card/index asset, which is incompatible with the latest Platform AI Agents and Skills app. As a result the AI summary card fails to load on UI Builder workspaces. Classic UI uses a different rendering path, so it is unaffected.

</td><td>

Refer to the listed KB article for details.

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
6.  Select the **subflow** menu.

 Observe that there aren't any options.

</td></tr><tr><td>

Virtual Agent

 PRB1963467

</td><td>

Variable is slot filled with SYSTEM\_FILTERED

</td><td>

This issue occurs in any catalog item for a reference type question. When a user types an option that isn't present in the reference table, the variable is slot filled with SYSTEM\_FILTERED in the summary card.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1975617

</td><td>

Failing to send an agent joined message

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1994599

</td><td>

Off Glide code introduced an issue for DTAC when the agent sends a message to the requester

</td><td>

The dynamic translation for messages doesn't work when the agent sends messages to the requester. It throws NPE.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1997460

</td><td>

For Now Assist conversations, interaction.transcript contains all the smartlinks rather than just the sources shown to the chat requester

</td><td>

 

</td><td>

1.  Set up an instance with Now Assist and AI Search.
2.  Perform a search that returns multiple sources.
3.  Close the conversation.

 Expected behavior: Interaction.transcript should show the sources that are displayed to the chat request.

 Actual behavior: Interaction.transcript shows all sources in the smartLinksData regardless of whether or not they are shown to the user.

</td></tr><tr><td>

Virtual Agent

 PRB1999010

 [KB2817637](https://hi.service-now.com/kb_view.do?sysparm_article=KB2817637)

</td><td>

The scheduled job, 'Time out abandoned Virtual Agent \(VA\) conversation' closes the conversation

</td><td>

'Time out abandoned VA conversation' should not close the conversation if the idle timeout is not completed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2006856

 [KB3003358](https://hi.service-now.com/kb_view.do?sysparm_article=KB3003358)

</td><td>

Serial number when conversation moves across nodes

</td><td>

Virtual Agent gets stuck. New messages are sent but the client doesn't render them until the page is reloaded.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2007255

 [KB3045151](https://hi.service-now.com/kb_view.do?sysparm_article=KB3045151)

</td><td>

There's memory pressure on nodes due to high memory for the cache 'com.​glide.​cs.​qlue.​module.​coma.​Message​Batching​Session'

</td><td>

Users with 2GB nodes may encounter memory issues that can cause the events process jobs to yield.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1923955

</td><td>

In an enhanced chat, the user can't view the RITM form in small screen

</td><td>

When the enhanced chat is in 90% modal and the user selects a link inside a card, the link opens in a new tab, but the VA remains in 90% modal. The enhanced chat should switch to floating mode when a link opens in a new tab. When the enhanced chat is in full-screen mode and a user selects any link inside the VA, the link also opens in a new tab. However, due to limited browser space, the enhanced chat remains in full-screen mode.

</td><td>

1.  Enable Enhanced Chat on portal.
2.  Log in to a Yokohama instance.
3.  Initiate a chat.
4.  Submit a request.
5.  Minimize the window so that only the chat window is visible on the screen.
6.  Select the RITM number.

 Expected behavior: Once RITM is selected, the RITM details are visible.

 Actual behavior: The RITM details aren't visible. Only the chat window is visible.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1972561

 [KB2787591](https://hi.service-now.com/kb_view.do?sysparm_article=KB2787591)

</td><td>

Enhanced chat does not pick up custom tokens in portal

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1988834

</td><td>

Custom icon on a menu item isn't displayed in the Conversational Panel \(Enhanced Chat\)

</td><td>

The icon configured for a menu item is not visible. This functionality previously worked in the standard chat experience, but it's no longer working in the enhanced chat.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2067082

</td><td>

Enhanced Chat colors don't change when theming CSS variables are set as documented

</td><td>

The variables in the 'Theming for Now Assist in Virtual Agent enhanced chat' documentation should be followed.

</td><td>

 

</td></tr><tr><td>

Visual Task Boards

 PRB1994303

</td><td>

In a Visual Task Board \(VTB\), the 'Select lane' menu displays lane values from all the boards available irrespective of the board selected to move

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Walk-Up Experience

 PRB2039555

</td><td>

The walk-up queue is not refreshing automatically after interaction closure

</td><td>

The walk-up 'Now Serving' queue does not automatically refresh when an interaction is moved to the 'Closed/Complete' state. The queue continues to display the user until the page is manually refreshed.

</td><td>

 

</td></tr><tr><td>

Window Manager

 PRB2019525

</td><td>

When the Now Assist panel is activated, the left side navigation is hidden and the margin remains applied, leaving an empty space

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1960028

</td><td>

AgentScheduleUtil script causes an 'Out of memory' issue for /​api/​now/​sg/​applet\_​launcher/​feed

</td><td>

While processing the API 'api/​now/​sg/​applet\_​launcher/​feed',​ there was an 'Out of memory' issue due to the script AgentScheduleUtil, leading to node restart. Based on the node logs, it seems to be a sudden spike that resulted in a restart. The issue is caused by an array holding more than 1Gb of data.

</td><td>

 

</td></tr></tbody>
</table>## All Other Fixes

To view a list of all other PRBs fixed in Brazil, refer to [All other Brazil fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/brazil-all-other-fixes.md).

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/available-versions.md)


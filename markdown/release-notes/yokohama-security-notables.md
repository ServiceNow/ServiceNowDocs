---
title: Yokohama security and notable fixes
description: The Yokohama release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 69
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama security and notable fixes

The Yokohama release contains important problem fixes.

-   **Yokohama was released on January 30, 2025.**
    -   Build date: 01-22-2025\_0439
    -   Build tag: glide-yokohama-12-18-2024\_\_patch0-01-14-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y00.00.xlsx).

## Security-related fixes

Yokohama includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama, refer to [KB1710869](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1710869).

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

Access Control

 PRB1833782

 [KB1721153](https://hi.service-now.com/kb_view.do?sysparm_article=KB1721153)

</td><td>

Slowness when loading forms with **Table Choice** fields related to the RecordFamilyResolver .archiveTableHasACLTerms code path

</td><td>

Accessing the any form with a **TableChoice** field where the instance has more than 250 archive tables can result in slowness due to RecordFamilyResolver .archiveTableHasACLTerms code path and a change to CACHE\_ARCHIVE\_TABLE \_HAS\_ACL\_TERMS in Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

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

Activity Stream

 PRB1778011

</td><td>

Audit and Journal events don't need to sanitize in the backend

</td><td>

SysAudit:218 and SysJournalRule don't need to sanitize, just getHtmlValue.

</td><td>

1.  Post the following comment: \[code\]&lt;IMG SRC=\# onmouseover="alert\('xxs'\)"&gt;\[/code\].

A broken image icon should appear in the comment for the activity stream.

2.  Hover over the icon.

No alert dialog should display.

3.  Open the Developer Inspector on the image element.

 The element should only have: 'img src="\#"&gt;'.

</td></tr><tr><td>

Activity Stream

 PRB1780340

 [KB1649222](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649222)

</td><td>

Post-Washington DC upgrade, GlideRecord for \[sys\_email\] updates all fields

</td><td>

The transaction should display that only the relevant information on the sys\_email record was updated, but extraneous fields are also updated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1781721

 [KB1705519](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705519)

</td><td>

Embedded images, such as images that are copied and pasted in the Workspace activity stream, aren't displayed in the Customer Portal

</td><td>

When an agent copies and pastes an image in the activity stream of the CSM Workspace, the image isn't visible to the user who accesses the case via the CSM portal.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1803978

 [KB1704344](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704344)

</td><td>

The SysActivityRuleRepo should be share aware for event source tables

</td><td>

When the name of the rotated table does not match the root name, a new email event was not created. The SysActivityRuleRepo should allow emails to appear in both the activity stream and in the workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1811273

</td><td>

Users can no longer view attached Excel files and DOCX files on Work Order Tasks \(WOT\) from the Agent app

</td><td>

Users can no longer view Excel sheets and docx files attached to work order tasks on the Agent app after upgrading to Xanadu. When users attempt to view the attached files from work order tasks on the Agent app, a modal with the message 'Unsupported file type' appears.

</td><td>

1.  Open a Xanadu instance.
2.  Open any work order task.
3.  Assign the work order task to a user.
4.  Add an Excel file or and docx file to the work order task.
5.  Log in to the Agent app as a user.
6.  Open the work order task.
7.  Navigate to the 'Activity Stream' tab.
8.  Open the attached files.

 Notice that a modal appears with the message, 'Unsupported file type'.

</td></tr><tr><td>

Activity Stream

 PRB1816292

</td><td>

An attachment isn't visible in the activity stream in workspaces

</td><td>

When an attachment is added to Record Producer, it can't be found in the activity stream.

</td><td>

1.  Add a variable with Type = 'Attachment' to Record Producer \(for example, create a case for CSM Outlook\).
2.  Open Record Producer in Service Portal.
3.  Attach a file to the field created in step 1 and submit.
4.  Navigate to CSM and FSM Configurable workspace and search for the item created after submitting.
5.  Check the activity stream.

 Expected behavior: The attachment should be visible in the activity stream in workspace.

 Actual behavior: The attachment isn't visible in activity stream in workspace.

</td></tr><tr><td>

Activity Stream

 PRB1832633

</td><td>

'Assignment group' changes are hidden in an activity stream on HR Agent Workspace, which is intermittently different to native

</td><td>

An activity stream in the workspace for the 'Case' table is intermittently missing the **Assignment Group** field change. Native has the change reflecting in 'Additional comments'.

</td><td>

1.  Open an incident.
2.  Set the assignment groups and **Assigned to** field.
3.  Save the record.
4.  Check the activity stream for the missing assignment group in the audit event.
5.  Repeat steps 2 through 4 several times.

 Expected behavior: The activity stream should be the same in both workspace and native.

 Actual behavior: The **Assigned Group** field change is missing intermittently in the HR agent workspace activity.

</td></tr><tr><td>

Adaptive Authentication

 PRB1657050

</td><td>

The 'Trusted Mobile Device' filter should also be used in the Post Authentication context

</td><td>

After creating a policy in the Post Authentication context with allowed IP ranges and Mobile App conditions, a user with a trusted, registered device should be able to log into the instance from the Now Mobile app. Currently, the login fails when the user uses a registered device with an IP that is not allowed. The Trusted Mobile device filter can be used pre-authentication, but should also be supported post-authentication.

</td><td>

1.  Search for 'Post Authentication context' with the application navigator.
2.  Navigate to the **Post Authentication context** module.
3.  Create a policy in the Post Authentication context with allowed IP ranges and Trusted Mobile App conditions.
4.  Enable Adaptive Authentication and Device Trust on the instance.
5.  Select **User Profile.**
    1.  Select **UI action**
    2.  Register a trusted mobile device.

Notice that it displays a QR code to register the device.

6.  Open the NowMobile app.

Register the device by scanning the QR code.

7.  Log into the instance from the Now Mobile app after registering the device.

 Expected behavior: The user should be able to login to the instance, as the user has registered the device, and post-authentication policies should pass and allow the user to log into the instance.

 Actual behavior: The user login fails from the registered device from an IP that is not allowed when the Trusted Mobile Filter is used in post-authentication.

</td></tr><tr><td>

Advanced High Availability \(AHA\)

 PRB1816356

</td><td>

A rare deadlock occurs during Glide start up

</td><td>

The deadlock is caused by ScriptsMetricsPublisher.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1792311

</td><td>

Advanced Work Assignment \(AWA\) causes significant memory pressure when used in the UI16 environments

</td><td>

When AWA is configured on an instance, but the agents primarily use UI16 to work tasks, unopened items build up in the users AWA inbox. This leads to very large AMB messages \(i.e. 3Mb +\) and significant memory pressure when the user opens a workspace.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1823284

 [KB1743632](https://hi.service-now.com/kb_view.do?sysparm_article=KB1743632)

</td><td>

There's 'Fix ErrorMessages' in UpdateSegment when 'confirmed on' is passed

</td><td>

Users see an error: 'Script execution error: Script Identifier: null.null.script, Error Description: undefined is not a function., Script ES Level: 0 Evaluator: com.glide.script.RhinoEcmaError: undefined is not a function.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Agent Chat

 PRB1823530

</td><td>

Input text is occasionally truncated in 'now-textarea'

</td><td>

Characters are truncated when typing quickly as an agent.

</td><td>

1.  Set up Agent Chat and accept a chat as an agent in Agent Chat.
2.  Type fast in the input text area.

 Observe that characters are truncated.

</td></tr><tr><td>

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

 PRB1745648

</td><td>

Some of the CSS variables for theming AI Search in Service Portal no longer work

</td><td>

$now-sp-tabs--selected--color and $now-sp-button--primary--color no longer work. They used to work in Tokyo.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1750999

</td><td>

The 'More' tab label displays 'More\_menu'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1767776

</td><td>

Incorrect empty state \(no Genius results\)

</td><td>

Genius results aren't appearing on a query that should produce results.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1778235

</td><td>

There's an 'Invalid or unexpected token' error message on a browser console when accessing any page on a portal after upgrading to a Washington DC version

</td><td>

The issue can be seen on any portal, like 'sp' or 'esc', as well as an empty testing page. There shouldn't be an error message on the browser console.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1779636

 [KB1651332](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651332)

</td><td>

Carousel and regular search results do not appear, and are stuck in a loading state

</td><td>

The carousel gets stuck in a loading state when a search query is performed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1794353

</td><td>

v\_search\_genius\_result becomes unreadable after opening a v\_search\_genius\_result ACL

</td><td>

AI Search stops rendering Genius Results after opening a v\_search\_genius\_result ACL record. A Null Pointer Exception \(NPE\) is observed in the system logs.

</td><td>

1.  Search with an AI Search search application and confirm the observation of Genius results.
2.  Open the Access Controls table \(sys\_security\_acl\).
3.  Search for any v\_search\_genius\_result ACL and click into it.
4.  Search again.

 Observe that the Genius results are no longer rendering.

</td></tr><tr><td>

AI Search

 PRB1794674

</td><td>

The top results carousel gets stuck in a loading state when the EVAM bundle doesn't have any view configuration for Genius results

</td><td>

Typically, regardless of if a search returns Genius results or not, geniusResultsTemplates is a JSON object with an 'items' property that is an array. If there are no Genius results for that query, items are just an empty array. However, if the EVAM definition doesn't have any view configurations for Genius results in any of its bundles, EVAM instead returns an empty response, which causes it to ultimately return 'null' for geniusResultsTemplates. While this doesn't impact the 'stacked' view of Genius results, it does break the logic in our top results component, and so the state is never updated to stop loading.

</td><td>

1.  Open ESC on a AIS-enabled instance.
2.  Search for '\*\*\*'.
3.  Verify that there's no Genius results.
4.  Open the EVAM definition for ESC, 'ESC Portal Search'.
5.  On the 'EVAM View Config Bundle M2Ms' related list, unlink 'Taxonomy Portal Search Bundle'.
6.  Refresh the portal page.
7.  Search for '\*\*\*' again.

 Expected behavior: There's no Genius results and the top results component hides itself.

 Actual behavior: The top-results component gets stuck in a loading state.

</td></tr><tr><td>

AI Search

 PRB1797747

 [KB1706071](https://hi.service-now.com/kb_view.do?sysparm_article=KB1706071)

</td><td>

The Genius results' loading spinner shows up despite unconfigured Genius results

</td><td>

The top spinner is visible when Genius results aren't linked and sometimes spins for a longer period of time. This occurs even if Genius results aren't linked to a profile used in the application that is being searched. The loader causes the page to continue rendering even if Genius results aren't linked to a profile.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1802473

 [KB1704430](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704430)

</td><td>

Tab counts change for all the tabs when users select from 'All' to another tab

</td><td>

Tab counts also change on pagination.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Analytics Hub

 PRB1798071

</td><td>

Analytics Hub throws an error when multiple breakdowns are applied

</td><td>

An error message appears: 'Expected ',' or '\]' after array element in JSON at position 951652 \(line 1 column 951653\)'.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1786797

</td><td>

Batch Install doesn't handle circular dependencies for non-app V2 apps

</td><td>

The BatchInstallDependencyMap.java class doesn't handle circular dependencies when the app being installed isn't a V2 app. The shouldEvaluateDependencies method incorrectly returns true when a circular dependency is encountered. When loading a non-V2 app and there's a dependency pair that's already seen, shouldEvaluateDependencies returns true because it checks the list of V2 plugins visited, which is empty because it's not a V2 app.

</td><td>

1.  Open a Washington DC instance.
2.  Attempt to batch install App Engine Studio.

 Observe that the progress bar doesn't go beyond 0%, and eventually a StackOverflow message appears.

</td></tr><tr><td>

Application Install Engine

 PRB1792128

</td><td>

There's a race condition when nodes try to download the same app package at the same time

</td><td>

During the cloning process, the list of nodes of clones are upgraded/downgraded. They restart at the same time and tend to download the app package at the same time. There is an existing logic which cleanups all the other attachments for the current app other that the download it made. Since the downloads are happening at the same time, nodes are deleting each other's downloads and nodes are failing to download the apps.

</td><td>

1.  Have multiple nodes \(&gt;=4\) in clone.
2.  Reset the clone.

</td></tr><tr><td>

Application Manager

 PRB1781787

 [KB1695712](https://hi.service-now.com/kb_view.do?sysparm_article=KB1695712)

</td><td>

Dependencies are not loading on Now Assist for Creator

</td><td>

The dependency processor repeatedly adds the same dependency for further processing, causing the list to grow continuously in an infinite loop.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Attachments to Records

 PRB1823698

 [KB1709552](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709552)

</td><td>

Out Of Memory \(OOM\) caused by the misuse of BufferedInputStream when creating attachments

</td><td>

Attachments created from previously prepared TMP files are read with BufferedInputStream and have an internal buffer of 512M.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1767180

 [KB1700280](https://hi.service-now.com/kb_view.do?sysparm_article=KB1700280)

</td><td>

A global policy shouldn't apply to internal APIs

</td><td>

Global policies shouldn't block internal APIs, but users get a 401 error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1768642

 [KB1649654](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649654)

</td><td>

OAuth Client \(consumer\) refresh token expiry should not get updated

</td><td>

The token receiver cannot determine the exact expiration date of the refresh token.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1793151

</td><td>

Screenshots are blank when certain characters appear in Service Portal HTML

</td><td>

context.drawImage\(\) is unable to properly parse the end of a comment that goes for multiple lines and includes extra dashes. Standalone commas in an element's attributes also prevent rendering of the document image.

</td><td>

1.  Create a Service Portal widget \(sp\_widget\).
2.  Add ca omment to the body HTML template with extra dashes and new lines, or add a comma character inside an element's attributes.
3.  Add the widget to an sp\_instance in an sp\_column, and add that column to an sp\_page.
4.  Create an ATF test with the 'Open Service Portal Page' step that opens the sp\_page from step 3 in any portal.
5.  Run the test with GlideScreenshot capturing the full page.

 Expected behavior: A screenshot is captured successfully.

 Actual behavior: A screenshot is blank and a client test runner console error appears.

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

 PRB1785629

 [KB1698772](https://hi.service-now.com/kb_view.do?sysparm_article=KB1698772)

</td><td>

The 'Manage Human Resource' catalog page isn't loading

</td><td>

An error displays in the console: 'Uncaught SyntaxError: Unexpected token '\)...'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1815083

 [KB1704517](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704517)

</td><td>

The banner image and production description are missing in UI16 if the plugin 'Human Resources Application: Core \(com.snc.hr.core\)' is activated

</td><td>

This issue only happens on Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Case Management

 PRB1803076

</td><td>

The role gs.hasrole is missing on a base instance script include

</td><td>

The role is missing for the 'Consumer role' condition.

</td><td>

 

</td></tr><tr><td>

CMDB Data Manager

 PRB1811393

</td><td>

The 'CMDB DependentCI Policy Processor' scheduled job consumes excessive memory with long execution times

</td><td>

 

</td><td>

1.  Find or create an instance with a large number of CIs.
2.  Add ledger \(cmdb\_dependent\_ci\_ledger\) entries, such that over 10k applies to a single policy.
3.  Run a scheduled job 'CMDB DependentCI Policy Processor'.

 Note the execution time and memory consumption.

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

CMDB Query Builder

 PRB1831836

 [KB1710849](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710849)

</td><td>

Users are unable to add columns in the query to be displayed in the query results

</td><td>

This issue might not display on all instances because the problematic tables might be coming from various plugins.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Code Signing

 PRB1783883

 [KB1710348](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710348)

</td><td>

LoggerConfiguration access privileges doesn't allow creation of a source record for Log Export Service \(LES\)

</td><td>

Despite an upgrade, when a user tries to create a LES source record, they get the message: 'Execute operation on script include 'LoggerConfiguration' from scope 'Log Export Service' was denied. The application 'Log Export Service' must declare a cross scope access privilege. Please contact the application admin to update their access requests. Error MessageSomething went wrong with the configuration setup. Please try again later by setting active to true and updating the record'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Column Level Encryption

 PRB1781726

 [KB1648610](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648610)

</td><td>

Duplicate 'Encryption Configuration' field records for tables in the CMDB hierarchy cause errors when the tables are queried

</td><td>

Duplicate 'Encryption Configuration' field records for tables in the CMDB hierarchy can lead to new tables not having the correct number of clone descendant records, causing errors when the tables are queried.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Column Level Encryption

 PRB1798601

</td><td>

Encrypted field configuration \(EFC\) records in the global scope for tables that are in a non-global scope can't be edited

</td><td>

When this happens, the global scope EFCs were all created by 'system' around the same time.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1777164

 [KB1650812](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650812)

</td><td>

Change Advisory Board \(CAB\) workbench displays an extra backslash in the **Planned start date** field

</td><td>

CAB workbench displays an extra backslash in the **Planned start date** field every time the CAB meeting is saved and refreshed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1332966

</td><td>

The 'Reset Unknown Discovery Source State' business rule \(BR\) calls current.setWorkflow\(false\) and thus cancels all the BRs that should have run after it

</td><td>

The **Convert to application service** action inserts/updates the cmdb\_ci\_service\_discovered table. But because the service had a discovery source set to 'Unknown', the 'Reset Unknown Discovery Source State' ran and the model update BR that should have been executed didn't. Thus, the service model wasn't created.

</td><td>

1.  Add a BR with an order higher than the order of 'Reset Unknown Discovery Source State' \(1010\) to the cmdb\_ci table.
2.  Update the table.
3.  Check if the new BR has ran.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1672625

 [KB1364738](https://hi.service-now.com/kb_view.do?sysparm_article=KB1364738)

</td><td>

Choices for the **Life Cycle Stage** and **Life Cycle Stage Status** fields are not translated

</td><td>

In the list view, both translations do not work. In the form view, **Life Cycle Stage** translations do not work.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1696232

</td><td>

The 'CMDB Query Builder suggested relationship' job executes a long running and expensive query, causing DB performance issues

</td><td>

Slow query ran for close to 2 hours.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1739806

</td><td>

Discovery jobs are causing an influx of queries to the ire\_mutex table, causing DB congestion

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1781459

</td><td>

The job 'CMDB Health Dashboard - Completeness Score Calculation' runs a slow query, which causes performance issues

</td><td>

The slow query causes a high DB CPU and increases history list length \(HLL\).

</td><td>

Run the job "CMDB Health Dashboard - Completeness Score Calculation".

 Observe the long running query.

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

Contextual Security Manager

 PRB1769723

</td><td>

A query business rule prevents non-admin users commenting on a Service Catalog task \(SCTASK\) from copying over to a requested item \(RITM\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Continuous Integration/Continuous Delivery \(CI/CD\) API

 PRB1774672

</td><td>

Continuous Integration/Continuous Delivery \(CICD\) publishing fails with a ScriptEvaluator error but appears successful on the tracker

</td><td>

The error reads: 'ScriptEvaluator SEVERE \*\*\* ERROR \*\*\* Evaluator.evaluateString\(\) problem'.

</td><td>

1.  Update the sn\_appauthor.ScopedAppUploader to throw a script evaluator error \(for example, clear the entire script field so that when a function is called it triggers an error due to the function not existing.\)
2.  Using a REST API explorer, publish an application by ID.

 Expected behavior: The tracker shows failure.

 Actual behavior: The tracker shows success.

</td></tr><tr><td>

Core Platform

 PRB1732676

 [KB1587782](https://hi.service-now.com/kb_view.do?sysparm_article=KB1587782)

</td><td>

The variable $\{comments\_and\_work\_notes\} isn't working for HR cases after an upgrade to Vancouver

</td><td>

After upgrading to Vancouver, email notifications with $\{comments\_and\_work\_notes\} are displaying as empty in the recipient's email. This works fine in Tokyo instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Core Platform

 PRB1762070

</td><td>

ServiceNow Performance Dashboards have errors for some graphs

</td><td>

Graphs have the error message, 'Error: Invalid series data'.

</td><td>

 

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

Database Persistence - Data Access

 PRB1649391

</td><td>

Database views using TPC with function fields generate errors

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1717895

 [KB1629327](https://hi.service-now.com/kb_view.do?sysparm_article=KB1629327)

</td><td>

The 'OR' logical operator in a related list condition query behaves as the 'AND' operator

</td><td>

When reporting over a table, using a related list condition with the 'OR' logical operator, it seems to have the same effect as using 'AND'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1759083

 [KB1641694](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641694)

</td><td>

DBOnlineAlter loops infinitely when reading data from the staging table

</td><td>

Online alters can loop infinitely from the staging table which impacts performance and causes upgrade issues.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1765194

</td><td>

A database view 'List' query throws a syntax error when the language is set to Japanese

</td><td>

The error message is a syntax error or access rule violation detected by the database unknown column 'sys\_translated\_text2.name' in 'where clause'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1818225

 [KB1705517](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705517)

</td><td>

Using 'order by' on a single field with a limit clause produces error messages in Xanadu

</td><td>

Users are experiencing 'Syntax Error' or 'Access Rule Violation' messages when they use an 'order by' function on a single field with a limit clause. This error occurs in the within the CMDB workspaces and CMDB hierarchy when viewing tables in the list view. This also occurs if the ordered list displays no data yet indicates a valid, non-zero row count.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1826425

</td><td>

An Application Menu Module \[sys\_app\_module\] with a space character causes a display failure in the filter navigator

</td><td>

An application menu module \(sys\_app\_module\) may not be visible in the filter navigator if there is a whitespace character \(non-null value\) in the **Query** field.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1771921

</td><td>

If a physical table name is different from the logical, the daily scheduled compaction job isn't working

</td><td>

 

</td><td>

1.  Make the sys\_report\_flow\_doc\_a5e table compaction eligible by setting up data and compaction criteria.
2.  Run compaction.

 Observe that it prints 'The compaction is not enabled for table: sys\_flow\_report\_doc\_chunk\_a5e. skipping..'.

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

Database Persistence - Data Scale

 PRB1784967

 [KB1706117](https://hi.service-now.com/kb_view.do?sysparm_article=KB1706117)

</td><td>

A NullPointException \(NPE\) was thrown while invoking the getAvailableConnection

</td><td>

An NPE occasionally occurs during the AHA 3.0 switchover. The failure to load the scripts database is because the return value of com.glide.db.pool. DBConnectionPool. getDBConnection\(int\) is null.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1788274

 [KB1720975](https://hi.service-now.com/kb_view.do?sysparm_article=KB1720975)

</td><td>

There's incorrect results when a statement is closed while another statement is executing

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence

 PRB1266075

 [KB0728469](https://hi.service-now.com/kb_view.do?sysparm_article=KB0728469)

</td><td>

If all tables that are part of a database view are on the same gateway database, Glide should be able to redirect the query to the gateway

</td><td>

Database views that are connecting to tables that are sharded aren't working. They aren't honoring the gateway configuration and still look in the base database.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence

 PRB1592883

</td><td>

There are unexpected results when QueryTermParser evaluates a query that contains 'STARTSWITH' and 'ON'

</td><td>

QueryTermParser returns ON for a query such as 'short\_description STARTSWITHSNOWMON' rather than 'STARTSWITH'.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1739880

</td><td>

Ignore forcePrimaryKeyOrdering for 'TS' queries

</td><td>

The Service Portal Search API returns an empty response. The UI looks like it hangs and no results appear.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1773095

</td><td>

Links break in 'Variable Set' records when the page is translated to a non-English language

</td><td>

The links in a 'Variable Set' record don't work when the **Title** field is not translated in a non-English language.

</td><td>

1.  Activate the Japanese language plugin \(com.snc.i18n.japanese\).
2.  Make sure the language is set to English.
3.  Navigate to the sc\_cat\_item table.
4.  Create a new catalog item.
5.  In the 'Variable Sets' related list, select **New**.
6.  Create a variable set \(for example, a single-row variable set\).
7.  Fill in the 'Title' name and other mandatory fields.
8.  Submit.
9.  Navigate back to the catalog item record and scroll down to the 'Variable Sets' related list.

Notice that the variable set 'Language test' link is working.

10. Switch the language to Japanese and check the variable set **Language test** link again.

 Expected behavior: The link should work as same in English mode.

 Actual behavior: The link is not working.

</td></tr><tr><td>

Data Collection for Oracle Global Licensing and Advisory Services for Software Asset Management

 PRB1810089

</td><td>

Downloading the GLAS report causes a blank page

</td><td>

The user is unable to download Oracle GLAS reports when there are over 10 million records in GLAS tables.

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

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1613464

 [KB1444661](https://hi.service-now.com/kb_view.do?sysparm_article=KB1444661)

</td><td>

The cmdb\_sam\_sw\_install table is duplicated after running discovery even after the extra records are deleted

</td><td>

Duplicate records are created in the cmdb\_sam\_sw\_install table even after deleting duplicate records and running discovery.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1619143

</td><td>

Specific MID selection for Cloud Discovery doesn't work due to an existing business rule implemented for MID cluster selection

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1726066

 [KB1645554](https://hi.service-now.com/kb_view.do?sysparm_article=KB1645554)

</td><td>

The vCenter Cloud probe is triggered every time the web server \(http.https\) is determined as open

</td><td>

A previous fix introduced a new 'VMWare - vCenter Cloud' probe which checks if vCenter is running on 443 port. If so, it triggers vCenter discovery. However the 'VMWare - vCenter Cloud' probe gets triggered every time the Web Server \(http.https\) is determined as open.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1742335

</td><td>

Discovering a large cloud environment causes issues with discovery\_temp\_results

</td><td>

The discovery status is marked as completed but the transaction is still processing because of the long running query on discovery\_could \_temp\_results. This occurs because of the business rule 'Update Cloud Resources Counts'.

</td><td>

Run Discovery on a large number AWS accounts where it retrieves an excess of 2 million records.

</td></tr><tr><td>

Discovery

 PRB1788611

 [KB1703744](https://hi.service-now.com/kb_view.do?sysparm_article=KB1703744)

</td><td>

vCenter extension contexts fail to start

</td><td>

The vCenter collector MID Server Extensions don't start and events aren't collected.

</td><td>

1.  Navigate to vCenter Event Collector Contexts.
2.  Create a record.
3.  Specify the MID server and vCenter details.
4.  Save the record.
5.  Select **Start** to trigger the events.

 Observe that the events aren't triggered upon selecting the **Start** button.

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

Discovery

 PRB1804276

 [KB1702685](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702685)

</td><td>

Discovery Application Dependency Mapping \(ADM\) process classifiers put incorrect configuration items \(CI\) in the probe ecc\_queue outputs, leading to data from the application only to be updated in the computer CI

</td><td>

When the ADM probe runs, matching process classifiers trigger probes specific to applications. The code involved in specifying the CI to put in the probe output is in the script include ApplicationDependencyMapping, which puts the parent computer CI in instead of the application CI. As a result, the computer CI is updated and overwritten rather than the application CI, and the application CI is not updated.

</td><td>

1.  Open NGINX on a Linux server to use as an example.
2.  Open a Vancouver instance.
3.  Discover a host to create a NGINX CI is created.
4.  Upgrade the instance to Washington DC.
5.  Clear out the version value from the existing application CI.
6.  Discover the Linux host.

 Notice that the example version is not repopulated in the NGINX CI.

</td></tr><tr><td>

Discovery Probes and Sensors

 PRB1769606

 [KB1645469](https://hi.service-now.com/kb_view.do?sysparm_article=KB1645469)

</td><td>

Non-Windows devices do not create software installs for the Operating System \(OS\)

</td><td>

On non-Windows servers, software install records are not created for the OS.

</td><td>

1.  Run discovery on a Windows device with SAMP activated.

Notice that software install records are created for Windows OS.

2.  Perform the same step for Linux/Solaris.

 Notice that OS install records are not created.

</td></tr><tr><td>

Document Management

 PRB1754517

</td><td>

The image saved inside of a table on a document section is distorted and truncated

</td><td>

When adding an image file into a table cell in a BCP record from the 'Documentation' related list, the image file is truncated and distorted after generating the PDF.

</td><td>

 

</td></tr><tr><td>

Document Management Services

 PRB1710424

</td><td>

PDF generation isn't working correctly when Hungarian characters are used

</td><td>

Ú and Ű characters are causing formatting errors in the generated document.

</td><td>

1.  Provision an instance with sn\_bcm, sn\_bcp, sn\_bia and sn\_bcm\_components plugins installed.
2.  Open the sn\_bia\_analysis record in the BCM workspace.
3.  In the **Description** and **Name** add one \(or both\) of the Ú and Ű characters. Ensure that the string is present after the characters.
4.  Save the record.
5.  Select the **Generate PDF** button.
6.  Open the generated document.

 Observe that the formatting breaks after the Ú and Ű characters.

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

Dynamic Translation

 PRB1832033

</td><td>

When a translatorID is sent as null to an exclusion framework API, it's not returning the input texts in the output in Now Assist

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Edge Encryption

 PRB1773542

</td><td>

A scheduled upgrade fails for a proxy running on Windows

</td><td>

It appears that the upgrade mostly completes. There's no errors in any of the logs, but the new Edge proxy service isn't started.

</td><td>

 

</td></tr><tr><td>

Elasticsearch Integration

 PRB1711742

</td><td>

Elastic index creation fails when clining from an instance with HA elastic search to non-HA

</td><td>

The user observes the error 'Failed to create surrounding logs' and all index creation fails.

</td><td>

1.  Request two instances with HLA \(one with HA Elastic and the other non-HA\).
2.  On startup, the surrounding logs index should be created.
3.  Clone the HA instance to a non-HA instance.

 On startup, observe the error 'Failed to create surrounding logs'. In general, all index creation fails.

</td></tr><tr><td>

Email Notifications

 PRB1763775

 [KB1699112](https://hi.service-now.com/kb_view.do?sysparm_article=KB1699112)

</td><td>

When composing an email in Service Operations Workspace \(SOW\) and copy/pasting the 'Caller' name to the **To** or **CC** field, the auto-complete for the reference field isn't appearing

</td><td>

For example, when the user copies and pastes the name 'Abraham Lincoln', it displays the error 'Local address contains control or whitespace. Characters in format \[a-z\]\[A-Z\]\[0-9\] \{-\} are accepted'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Email Notifications

 PRB1783999

</td><td>

The 'Instance Email Reader' job stalls when only deleting \(not retrieving\) messages from POP3

</td><td>

When an instance is collecting mail, it retrieves messages at a significant rate under normal operations. When choosing only to delete messages \(and not retrieve them\), each mail reader job processes only 20 messages and then exits, forcing the instance to wait for the next scheduled email reader job 2 minutes later. This cycle repeats until the instance finds messages it chooses to retrieve, instead of just delete.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1828578

</td><td>

Slow performance loading Major Issue Management \(MIM\) workbench email client

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Employee Relations Case Management

 PRB1830223

</td><td>

HR users are unable to add or view attachments on Employee Relations cases in HR Agent Workspace

</td><td>

When HR users try to add attachments to an Employee Relations case in HR Agent Workspace, the attachment disappears and they are unable to view all previous attached documents. If users view the same Employee Relations record in HR Agent Workspace as an admin, they can view all of the attachments that the HR user tried to add.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1760429

</td><td>

A race condition in tag-based clustering engine when multi job/node event processing is enabled is causing multiple tag clusters to be created

</td><td>

This causes multiple tag cluster groups to be created for the same alerts.

</td><td>

1.  Set 'not for correlation' from the query job \(set the property as false\).
2.  Enable multi-job \(4\)/node event processing.
3.  Create a TBAC definition.
4.  Send several events at the same time with different message keys.

 Observe that multiple tag cluster groups containing the same alerts are created.

</td></tr><tr><td>

Event Management

 PRB1815229

 [KB1704522](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704522)

</td><td>

AnomalyScoreProcessor has 'Debug logging' turned on by default

</td><td>

Having 'Debug logging' turned on by default results in thousands of unnecessary records appearing in the syslog.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1821550

</td><td>

An info message of 'Have you tried express list...' appears also for non em\_alert tables \(but for em\_alert as a related list in the page\)

</td><td>

The blue message of 'Have you tried express list...' appears, though it shouldn't for the related list of the 'Alerts' page.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1752255

 [KB1705325](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705325)

</td><td>

Flow stage changes aren't working after using the **Do the following in parallel** action with engine v2

</td><td>

The issue is also confirmed in Washington DC.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1813296

</td><td>

A subflow reference input comes in as a JSON instead of a reference

</td><td>

Whenever a group record is passed via flow to sub-flow, it displays an error as 'Skipping approvals due to invalid rule: ApprovesRejectsAnyG'. Passing a record to a subflow isn't constant and is coming through as a JSON. This isn't just isolated to ApprovalRules.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1814554

 [KB1715780](https://hi.service-now.com/kb_view.do?sysparm_article=KB1715780)

</td><td>

Issue found in Xanadu with 'Submit Catalog Item Request', and multi-row variable sets \(MRVS\) and multi-line text variables

</td><td>

A flow or subflow using 'Submit Catalog Item Request' where the catalog item contains a MRVS and multi-line text field fails produces the error: 'com.snc.process \_flow.exception. OpException Caused by: Unexpected character \(\\\) at position 3942.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1648314

</td><td>

There's a 'LookUpRecord' error log when it gives no results

</td><td>

When 'Look up record' returns null, the sys log records an error log even if 'don't fail on error' is true.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1740676

</td><td>

Users are receiving a 'Number of rows hidden by security constraints' message in Flow Designer related flows

</td><td>

There's related flows logic when the main flows/subflows snapshots with different names use a given subflow A. For subflow A, the related flows logic counts each snapshot with a different name as a single flow, which is incorrect. Due to this, in Flow Designer, for a subflow/action in a related flow, a 'Number of rows hidden by security constraints' error message displays.

</td><td>

1.  Navigate to Flow Designer.
2.  Create a subflow and publish.
3.  Add a subflow to a flow and save.
4.  Change the name of the flow and publish.
5.  Navigate back to the subflow.
6.  Select **Show related fields**.
7.  Select the **More Actions Menu** in the top right corner.
8.  Select **See Related Flows**.

 Observe that one flow is visible while it shows the message at the bottom 'Number of rows hidden by security constraints: 2'.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1755867

</td><td>

Saving flow stages is throwing an internal server error

</td><td>

An error message 'Internal server issue due to insufficient access' appears when saving flow stages.

</td><td>

1.  Log in to the most recent iPaaS instance.
2.  Impersonate as a user who has the 'flow\_designer and action\_designer' role only.
3.  Create a new flow.
4.  Navigate to the **More actions** menu.
5.  Add stages.
6.  Select **Save**.

 Notice that error message, 'Internal server issue due to insufficient access' appears.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1780076

</td><td>

**Approval** &gt; **State** is set to 'Canceled' when the flow executes actions with the stage 'Requested Canceled' in Vancouver and Washington

</td><td>

When the flow sets the requested item \(RITM\) stage to 'Request Canceled', the RITM approval is still 'Requested', which triggers the 'request item closure' business rule.

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
3.  Create a subflow.
4.  Add the created action in the second step.
5.  Try to set the value for the String variable and save the subflow.

 Expected behavior: The value is saved.

 Actual behavior: The value is wiped out.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1796489

</td><td>

A flow variable assignment is reverted after saving a subflow

</td><td>

 

</td><td>

1.  Open Flow Designer.
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

 PRB1817432

 [KB1710616](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710616)

</td><td>

Error Evaluation isn't functioning as expected for new flows in Washington DC where Flow Engine V2 was introduced

</td><td>

In an action, the REST step is used, and Error Evaluation is configured. The Error Evaluation is set to assign an action status code of 2 and set the action status Message to the REST step's response body when the REST step's status code isn't 200. However, in the execution result, even though the REST step's status code is 200, the action status code is 2, and the action status message is null.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1822604

 [KB1709945](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709945)

</td><td>

Flow action field values are truncated when they contain the '=' symbol in one field and use inline scripts in another field

</td><td>

A flow action isn't updating fields properly when having the 'script' type column and inline scripts on the 'Create Record' action.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Form Controller

 PRB1826786

</td><td>

Base input fields aren't displayed for Now Assist for Configure Management Database \(CMDB\)

</td><td>

The 'Choose Inputs' section is blank and throws an error when the user attempts to enable the CI summarization skill for CMDB.

</td><td>

Navigate to **Now Assist for Admin** &gt; **Features** &gt; **CMDB** &gt; **View details** &gt; **CI Summarization** &gt; **Close inputs.**

 Notice that base inputs are blank, and an error is thrown.

</td></tr><tr><td>

GlideRecord

 PRB1786468

</td><td>

A transaction runs in an infinite loop when the user evaluates the condition that has 'Contains'

</td><td>

As a result of this issue, the entire session becomes unusable.

</td><td>

 

</td></tr><tr><td>

Guided Tours

 PRB1784409

</td><td>

The guided tours API returns java.lang.ArrayIndex OutOfBoundsException

</td><td>

It throws a 500 internal server error.

</td><td>

1.  Provision an instance with the Major Incident Management plugin with demo data installed.
2.  Navigate to Service Operations Workspace.
3.  Access one major incident from the list.
4.  Navigate to the 'Communicate' tab.
5.  Create a task with email as an option.
6.  Select **Compose**.

</td></tr><tr><td>

Guided Tours

 PRB1790101

</td><td>

A guided tour displays 'Undefined' when trying to stop auto-launching a tour in HR Agent Workspace

</td><td>

 

</td><td>

1.  Ensure that com.sn\_hr\_agent\_ws for Agent Workspace for HR Case Management is installed.
2.  Create a guided tour and provide the below information:
    1.  Name:provide-name
    2.  Tour Type:Workspace
    3.  Select 'Manual Selection'
    4.  Starting page: now/hr/agent/home
    5.  Select on **Create Tour**.
3.  Open a browser.
4.  Ensure to close all the existing opened tabs first.
5.  Clear the entire cache and history of the browser.
6.  Log in to a Vancouver instance.
7.  Navigate to HR Workspace home page.
8.  Wait for the tour to auto launch.
9.  After the tour pop-up displays, select the **x** button.

 Notice that it's displaying 'undefined'.

</td></tr><tr><td>

Haraka \(Glide\)

 PRB1824231

 [KB1709920](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709920)

</td><td>

sys\_kagami\_query\_engine has an error on the column decision\_last\_msg

</td><td>

Queries are not routing to postgreSQL after upgrading to Xanadu. Queries with 'group by' are attempting to route to Haraka, but are failing due to a syntax error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1825365

 [KB1709665](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709665)

</td><td>

Health Log Analytics breaks after upgrading to Xanadu

</td><td>

MID Server distribution is missing a bundled dependency \(mid-loom.jar\).

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

History Set

 PRB1826101

</td><td>

Enabling the property 'glide.history\_set.pull\_ journal\_entries\_from \_journal\_table ' has side effects

</td><td>

Enabling the property breaks HistoryWalker API and populates '0' as the update count for journal fields in the sys\_history\_line table.

</td><td>

 

</td></tr><tr><td>

HTML Field Type Editor

 PRB1782444

</td><td>

When the 'close unordered list' tag is used in a template, a non-breaking space element gets added to the HTML field

</td><td>

When a template is created on an HTML field and '&lt;/ul&gt;' tag is included, the issue occurs. Applying the template adds '&amp;nbsp;' to the HTML field. The value is seen as; &lt;/ul&gt; &amp;nbsp;

</td><td>

 

</td></tr><tr><td>

HTML Field Type Editor

 PRB1799918

</td><td>

Selecting the 'Preview form' icon opens the TinyMCE editor

</td><td>

The UXC Generative AI plugin adds a UI Macro to a form containing TinyMCE. When a form is previewed from a list, the UI Macro is rendered and TinyMCE is initialized around the list. The selector it is using isn't compatible with a 'Lists' page.

</td><td>

1.  Provision an instance with the latest version of UXC Generative AI \(6.0.1\).
2.  Set the glide.ui.html.editor.use\_v4 property to true.
3.  Open any list.
4.  Select the 'Preview form' icon for any record.

 Expected behavior: The 'Read only' form pop-up is opened.

 Actual behavior: The TinyMCE editor is opened.

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB1774663

</td><td>

The user observes the alert 'General Data Exception detected by Database \(No value specified for parameter 1.\)' after submitting a clone on the 'clone\_instance' page

</td><td>

This isn't impacting clone progress, but it gives false alarm.

</td><td>

Submit a clone via the 'Legacy clone request' page.

 An error warning displays on the top of the page.

</td></tr><tr><td>

Instance Scan

 PRB1797550

 [KB1704250](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704250)

</td><td>

Deprecated APIs scheduled scan has an invalid combo reference

</td><td>

Users may see an error because scans are run periodically: 'Error log com.glide.instance\_ scan.ScanEngine: java.lang. IllegalArgumentException: No such scan\_combo record...'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Integration Hub

 PRB1766824

</td><td>

Non-Integration Hub \(IH\) outbound calls are counted as IH usages if a flow is called earlier in the IH transaction, even if this flow doesn't cause the outbound request

</td><td>

 

</td><td>

 

</td></tr><tr><td>

JVM at Scale

 PRB1783992

 [KB1698970](https://hi.service-now.com/kb_view.do?sysparm_article=KB1698970)

</td><td>

Nodes are unresponsive after Java Virtual Machine \(JVM\) hangs or crashes

</td><td>

A change in the Washington DC upgrade causes the JVM nodes to become unresponsive, leading the Java Service Wrapper to determine the JVM node is hung. The nodes do not appear to restart, and out of memory \(OOM\) errors are not posted in the logs. This causes the node to stay down and causes performance impact for instances that are affected.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1740666

</td><td>

Publickeywrap and Publicsigver certificates aren't regenerated when certificates are missing and keys are present

</td><td>

If an instance only has an active key pair \(for Instance Asymmetric Encryption Key \(IAEK\) and Instance Signature Key \(ISK\)\) but certificates corresponding to it don't exist, certificates corresponding to IAEK and ISK should be regenerated, but aren't.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1783762

 [KB1695361](https://hi.service-now.com/kb_view.do?sysparm_article=KB1695361)

</td><td>

Authors that are not a member of the ownership group can no longer edit a Knowledge Base article, even if the glide.knowman.ownership \_group.override property is set to true

</td><td>

The relevant condition does not check if the user is the author of the KB article, and if the glide.knowman.ownership \_group.override property is set to true, causing the ACL to fail.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Language and Translations

 PRB1766013

</td><td>

For Japanese, the dirty update dialog isn't translated correctly in U16

</td><td>

\{HTML:displayValue\} is displayed without a value from sys\_ui\_message. \# is missing in the Japanese translation.

</td><td>

1.  Provision an instance with the Japanese translations plugin installed.
2.  Change the system property glide.ui.polaris.experience to false to enable U16.
3.  Open an incident record.
4.  Change the description without saving.
5.  Select the **Back** button to trigger the dirty update dialog.

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

 PRB1770231

</td><td>

A list doesn't load when a fixed filter is null and a live list is enabled

</td><td>

The 'List' screen hangs when applying a filter.

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

List Administration

 PRB1798031

</td><td>

The **Edit columns** functionality isn't working as expected in Configurable Workspace

</td><td>

If a user opens the workspace the first time and do the re-column options, the user preference is saved in a format: workspace.list. columnOrder.xyz. If users then open a new tab in Chrome, and change it again, the preference is saved with a different suffix: workspace.list. columnOrder.abc. If users then go back to the first tab in Chrome and update the user preference, it updates back to: workspace.list. columnOrder.xyz. The workspace latches onto one of these user preference suffixes, and ignores the others.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1804211

</td><td>

A list is failing to load due to ACL failures

</td><td>

Lists do not load, and a response is returned in the call for the record list composite data broker.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1827799

</td><td>

A filter condition in a module is displaying additional filters when opened in new tab

</td><td>

The filter condition displays backend details.

</td><td>

1.  Create a module.
2.  On a table, select **Incident**.
3.  Add any dot-walking fields.
4.  Create a user and a system level user preference record 'glide.ui.polaris. ui16\_tabs\_inside\_polaris' as a type string and set the value to true.
5.  Impersonate a user.
6.  Navigate to a module created incident.
7.  Open the module in a new tab.

 Expected behavior: When the module is clicked to open in a new tab, only the dot-walking filters should apply.

 Actual behavior: When the module is clicked to open in a new tab, additional backend filters are applied. Observe that some additional filters are applied. This issue only happens when opening the module in a new tab. If opened in the same tab, the issue doesn't happen. If the user preference value for the user is set as false, the issue isn't observed.

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
4.  In the event, add a field object of 'sysId: &lt;sys id of first row&gt;'.
5.  In the event, add the route 'quick-edit'.
6.  Save.
7.  Open the app.
8.  Trigger the button.

 The pane doesn't open as expected.

</td></tr><tr><td>

Major Incident Management

 PRB1815931

 [KB1709324](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709324)

</td><td>

Impersonation logic in the Major Incident Management \(MIM\) script include causes events to fail post-upgrade

</td><td>

System events error out as a result of user impersonation logic in the 'ExecuteMIMTrigger RulesWithImpersonation' script include. When this script include is called during async processing, the system impersonates the logged in user, marking subsequent events as processed or updated by an individual user instead of the 'System'. As a result, these events error out.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1773302

 [KB1646558](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646558)

</td><td>

Start and stop permissions for MID Server Windows service users triggers security alerts by enumerating all local administrator users

</td><td>

Security monitoring tools flag the execution of 'net localgroup administrators' due to user enumeration of SAM-R queries going to the Active Directory server. The group 'net localgroup administrators' is used for all users.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1779476

 [KB1648678](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648678)

</td><td>

The MID Server Dashboard doesn't show CPU usage for some MID Servers, but does show memory

</td><td>

Windows MID Servers can fail to fetch CPU Usage metrics from the host, resulting in blank or zero graphs in the MID Server Dashboard. The StatusMonitor thread in the MID Server is unable or stops being able to get CPU usage information from the Windows OS. It does not end up in the queue.stats/MID Server XMLStats error correction code input, which then does not put it in the table ecc\_agent\_scal ar\_metric in which the graphs derive from. Errors should be seen in the agent log for the StatusMonitor thread if the data cannot be retrieved. With this issue, no errors are seen in agent log, and the data is missing.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1788294

 [KB1704349](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704349)

</td><td>

MID server issue warning, 'No mapping between account names and security IDs was done'

</td><td>

When trying to grant permission using all possible fully qualified representations of a user without verifying if that representation is valid as per the environment configuration, when a given representation isn't valid, users receive the warning: 'No mapping between account names and security IDs was done'.

</td><td>

Refer to the listed KB article for details.

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

</td></tr><tr><td>

MID Server

 PRB1792071

 [KB1695722](https://hi.service-now.com/kb_view.do?sysparm_article=KB1695722)

</td><td>

MID server ECCsender fails to process XML files and continuously retries if the file is truncated or contains invalid characters

</td><td>

MID server ECCsender fails to process XML files and continuously retries if the file is truncated, or if the file contains invalid, control, or unparsable characters such as '\#31;'. As soon as the files begin to be renamed, they continue to fail to be sent to the instance. Because the instance fails to read the files, it constantly retries, and moves the records to output\_error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1797811

 [KB1702039](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702039)

</td><td>

There's misleading FileNameCompliance InSync attachment file errors when ecc\_agent\_script\_file attachments are missing

</td><td>

Xanadu added a filename check for synched files. It generates MID Server issues records, but these can be misleading false positives that would be difficult to figure out if the record has use attachments but doesn't have the referenced attachment present.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1819817

</td><td>

Reduce default SFTP read/write buffer to 32768 from 32868

</td><td>

There were few cases of import/export where there environment had some issues in handling the SFTP buffer size of 32868. Since import/export has not exposed any SSH configuration, users aren't able to reduce the buffer size.

</td><td>

 

</td></tr><tr><td>

ML Normalization for SAM

 PRB1663147

 [KB1634642](https://hi.service-now.com/kb_view.do?sysparm_article=KB1634642)

</td><td>

The job 'SAM - Normalize discovery models using machine learning' fails for unavailable or mismatched content

</td><td>

'SAM - Normalize discovery models using machine learning' fails intermittently for mismatched / unavailable content even though other models are normalized with no issues.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

 PRB1827237

</td><td>

The '\[ICenter Analytics\] Daily Data Collection' job throws an error

</td><td>

The '\[ICenter Analytics\] Daily Data Collection' job throws an error: 'Error Invalid facts table for indicator source IntegrationUsers WithoutWSAOFlag Enabled DataCollector'.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1787356

 [KB1652699](https://hi.service-now.com/kb_view.do?sysparm_article=KB1652699)

</td><td>

Some pages don't load when the property 'glide.ui.next\_experience. instance\_tools\_disabled' is set it to false and Next Experience is turned off

</td><td>

Pages such as 'Plugins', 'NLU Workbench models', 'Service Operations Workspace', and 'CSM-Configurable Workspace' don't load when the property 'glide.ui.next\_experience. instance\_tools\_disabled' is set it to false and Next Experience is turned off. Admin role users are unable to access these modules: Plugins \(now/app-manager/home\), NLU Workbench models, Service Operations Workspace, CSM-Configurable Workspace. ITIL role users are unable to access Service Operations Workspace and CSM-Configurable Workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1799023

</td><td>

A menu can show fewer items when a business rule is configured to restrict a query

</td><td>

The user observes that the Next Experience header is missing menus \(for example, 'All', 'Favorites', and 'History'\). This can occur if there are business rules against the 'sys\_app\_application' or 'sys\_app\_module' tables with the type 'Query'. It can also result from bad domain-specific caching in relation to the menus.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1805368

 [KB1703778](https://hi.service-now.com/kb_view.do?sysparm_article=KB1703778)

</td><td>

Use of home keyboard cursor navigation is broken in the Next Experience navigation filter input and end keyboard buttons in Xanadu

</td><td>

Left, Right, Home, End, Shift+Home, Shift+End, Shift-Left, and Shift-Right don't move the cursor or select text.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1806148

</td><td>

A long contextual pill pushes the search, help, notification, and user menu out of the viewport

</td><td>

Extra long text in the contextual menu is not truncated and causes spillover of the search and other icons.

</td><td>

1.  Log in to any instance.
2.  Navigate to any page that has a long title.

 Notice that the extra long text in the contextual menu is not truncated and causes spillover of the search and other icons.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1806521

 [KB1705141](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705141)

</td><td>

Next Experience menus are blurred/unreadable in Safari v18

</td><td>

It's related to the CSS style 'webkit-backdrop-filter' being applied incorrectly to the pages. Instead of applying the blur to the background of the menus, it's applying to the entire menu, including the text.

</td><td>

1.  Open the instance using Safari 18.0 \(20619.1.26.31.6\).
2.  Navigate to the top menus.

 Expected behavior: The navigation is readable.

 Actual behavior: The menu is blurred and unreadable.

</td></tr><tr><td>

On-Call Scheduling

 PRB1819083

</td><td>

The 'On-call schedules' \(all on-call schedules\) tab isn't loading

</td><td>

The 'All on-call schedules' tab gets stuck at 'loading'. The following error message displays in the console: 'TypeError: Cannot read properties of undefined \(reading 'name'\)...'

</td><td>

1.  Navigate to on-call schedules.

The 'All on-call schedules' tab is stuck at 'loading'.

2.  Select 'my on-call schedules'.

Verify that it works.


 If a user selects the 'all on-call schedules' tab, the display doesn't change and still displays 'my on-call schedules' tiles.

</td></tr><tr><td>

Performance Analytics

 PRB1789424

</td><td>

Https \_request\_ decompression doesn't work correctly, as it doesn't strip the 'Content-Encoding' header after it unzips the body

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1779614

</td><td>

The PAR dashboard search isn't giving the expected results when a non-English language is set on the instance

</td><td>

User gets 'Items removed from this page due to security constraints' or 'No data to display'. Messages are in a translated language, whichever exists at that time on the user session.

</td><td>

1.  Navigate to an instance with one of the language plugin installed.
2.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Dashboards**.
3.  On 'User Preferences', set the language to English.
4.  Navigate to 'All'.
5.  Search with a dashboard name like 'change' or 'incident'.
6.  On 'User Preferences', set the language to German, or any other installed non-English language.
7.  Search with a dashboard name like 'change' or 'incident'.

The same set of dashboards that were returned in step 5 do not appear. A few dashboards are displayed and a message exists that filters out other dashboards.


 Expected behavior: The dashboard search results should be consistent in all languages.

 Actual behavior: In the English language, there's expected results but in others, the result is inconsistent.

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

Predictive Intelligence

 PRB1759824

</td><td>

HTML fields include HTML tags in the prediction result, which adds noise and reduces the prediction scores

</td><td>

HTML-type input fields contain HTML tags that add noise to the dataset for machine learning. Machine learning doesn't remove these HTML tags during the pre-processing stage, and so when making predictions, the HTML fields include the HTML tags in the prediction result.

</td><td>

1.  Add an HTML field as an input field to any type of solution definition.
2.  Train the solution.
3.  When making predictions, make HTML fields include the HTML tags that add noise to the dataset for machine learning.

</td></tr><tr><td>

Predictive Intelligence

 PRB1777777

 [KB1702121](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702121)

</td><td>

Similarity calculation from Predictive Intelligence slows down the instance

</td><td>

An issue with Predictive Intelligence similarity calculation slows down alert record loading.

</td><td>

1.  Change the property evt\_mgmt.similarity\_use\_ml to true.
2.  Open an alert record through Express List Records.

Notice that it takes a few minutes to open.

3.  Change the property evt\_mgmt.similarity\_use\_ml to false.
4.  Refresh the alert record.

 Notice that the similar alerts query takes an average of 35,655 milliseconds.

</td></tr><tr><td>

Problem Management

 PRB1762651

</td><td>

PMMU \(Physical Memory Management Unit\) issues found during London to Xanadu upgrade testing

</td><td>

There are several issues. There's incorrect code and problem models for customizations. The demo data needs to be remapped. There's an outdated info message. The **Next** button doesn't appear until reloading when requesting to activate a plugin. Some of the problems and problem tasks failed to migrate. The 'Problem overview' dashboard should not be deleted on upgrading.

</td><td>

 

</td></tr><tr><td>

Problem Management

 PRB1816736

</td><td>

The **Problem** field isn't populated in a problem task

</td><td>

When a problem task is opened from a problem record, the **Problem** field in a problem task record displays as empty.

</td><td>

1.  Navigate to an instance.
2.  Open any active problem.
3.  Navigate to the 'Problem Task' related list.
4.  Select the **New** button to create a problem task.
5.  Choose any task type from the option 'Root Cause Analysis' or 'General'.

 Observe that it opens the 'Task' page, where the **Problem** field is empty, which isn't auto-populated.

</td></tr><tr><td>

Project Management

 PRB1789648

</td><td>

**Save as new template** fails at creating a template

</td><td>

In a domain separation instance, there's an ACL to restrict the user from creating a project template in the global domain \(add condition 'domain is not global'\). When a non-admin user is trying to create a template from a project by selecting the 'save as new template' related link, the template was not created because the ACL is failing. The user and project aren't in the global domain.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1810601

</td><td>

'Page not found' displayed when selecting the **Check it out** button from a 'Project' form in Project Workspace

</td><td>

 

</td><td>

1.  Log in to the application.
2.  Navigate to pm\_project.list.
3.  Open a record.
4.  Select **checkitout**.

 'Page not found' is displaying.

</td></tr><tr><td>

Project Management

 PRB1814537

</td><td>

The 'Planning Console' related link on the project record gets stuck after clicking the link

</td><td>

The user is not redirected to a console.

</td><td>

1.  Open any project.
2.  Under related links, select **Planning Console**.

 Notice that the user is not redirected to any console and the page is stuck.

</td></tr><tr><td>

Related Lists

 PRB1720250

 [KB1639073](https://hi.service-now.com/kb_view.do?sysparm_article=KB1639073)

</td><td>

Default filters on relationship-related lists aren't applied in a workspace

</td><td>

.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Related Lists

 PRB1780317

</td><td>

Inline cell edit options appears off-screen for related lists

</td><td>

The inline edit box should be right justified when on the right of the screen and show all inline edit icons. Instead, the inline edit box is left justified when on the right of the screen and disappearing off the right edge of the screen.

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB1715615

</td><td>

In a calendar report, the linked dataset has quarters that are not in sequence

</td><td>

If a dataset has missing data for the quarters VS report the report does not bring back details for 0 data so because of missing data. The report is designed not to return 0 results - 'dataset' graphs align per data availability and ignore the sequence of quarters.

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB1764936

 [KB1645365](https://hi.service-now.com/kb_view.do?sysparm_article=KB1645365)

</td><td>

Scheduled list export with many rows fails and is sent as a PDF with an error message

</td><td>

The attachment is exported as a PDF with an error message instead of an excel file, even though the scheduled export was set as an excel file.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Reporting

 PRB1815240

</td><td>

Multi-pivot in Service Portal throws 'ERROR: An error occurred while generating chart'

</td><td>

There's also an error in the logs: 'Uncaught Error: TypeError: leftMostRowValue\[key\].escapeHTML is not a function'.

</td><td>

1.  Navigate to the classic reporting module.
2.  Create a report:
    -   Table: incident
    -   Type: Multi-level pivot table
    -   Selected columns: Assignment Group
    -   Selected rows: Short description, Number
3.  Navigate to **Service Portal** &gt; **Service Portal Configuration**.
4.  Select **Designer**.
5.  Add a page.
6.  Select any container.
7.  Under 'widgets', select **Report** and drag it into the container.
8.  Select the recently created multi-pivot chart.

 Expected behavior: The chart renders.

 Actual behavior: 'ERROR: An error occurred while generating chart' displays.

</td></tr><tr><td>

Request Management

 PRB1793466

</td><td>

A business rule throws an 'Unparseable date' exception

</td><td>

The error reads: 'java.lang.RuntimeException: could not be parsed using format string yyyy-MM-dd HH:mm:ss'.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1784311

</td><td>

When trying to select the **Request Extension** button on a resource plan from the project workbench, the 'Extend resource plan' pop-up appears empty

</td><td>

A blank pop-up screen appears.

</td><td>

1.  Navigate to the project module and open any project.
2.  Under the related links, select something in the project workbench.
3.  Under the 'Resource' tab, select any resource plan.
4.  Select the **Request** button.

 Observe that a blank screen appears.

</td></tr><tr><td>

Rollback Contexts

 PRB1772992

 [KB1648911](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648911)

</td><td>

The 'Shadow' table chunk delete has performance issues

</td><td>

The time taken for deleting shadow records can be derived from the logs. When users delete data from the 'Shadow and snapshot' table, a log statement is printed. First, 'Shadow' table records are deleted, then the 'Snapshot' table. Time between log statements would be the time taken to delete shadow records. It takes more than 1 minute to delete records from a 'Shadow' table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Script Includes

 PRB1805747

 [KB1704606](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704606)

</td><td>

Restructure upgrade transition for the sandbox\_callable script to include the schema change

</td><td>

There's been issues with different upgrade scenarios when separating the sandbox callable functionality of client callable in pre-Y releases.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Server-side scripts

 PRB1786423

 [KB1650937](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650937)

</td><td>

Transpiler doesn't respect the custom per-thread memory limit, causing an error

</td><td>

Some threads in the transpiler do not respect the value of the system property, com.glide.script.swc .memory\_threshold\_in\_kb, and instead throw an exception when memory usage exceeds the default per-thread limit of 16MB. The error is logged repeatedly and prevents a portion \(up to 1/4\) of the server-side scripts executed on the node to fail.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Server-side scripts

 PRB1796259

</td><td>

Failure to instantiate a GlideElement during a sandboxed script execution can take down a node

</td><td>

It should obtain the global scope to reinitialize GlideController instead of trying to traverse to global from the current GlideElement and, potentially, grabbing the sandbox scope instead.

</td><td>

Trigger GlideElement.specialReinitialize using the sandbox scope.

</td></tr><tr><td>

Server-side scripts

 PRB1809279

 [KB1703678](https://hi.service-now.com/kb_view.do?sysparm_article=KB1703678)

</td><td>

The SWC version in Xanadu leaks memory

</td><td>

The transpiler leaks a small amount of memory, on the order of 50 bytes, with each script that it processes. Eventually, enough memory is leaked that attempts to execute additional scripts on the node cause the transpiler to exceed the memory usage limit, specified by the com.glide.script.swc. global\_memory\_threshold\_in\_kb system property. Once this limit is exceeded, a 'Transpilation global memory limit exceeded' error is logged and the node is unable to process server-side scripts normally until it is restarted.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Builder

 PRB1794710

</td><td>

A catalog filter isn't functioning in Xanadu

</td><td>

When users select 'Need to Request Something?', the catalog filter widget is displayed on the left side of the page. It should display the 15 categories and when users select the 'Show More Catalog' filters, it's expected to display another 15 categories. Currently, categories aren't displaying on the 'Catalog filters' widgets.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1734166

</td><td>

Localization framework publishes translations in the global scope although the artifact record is created in a different scope

</td><td>

Users see the following error: 'Cannot commit update set since scope ID is different'.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1808592

</td><td>

The 'Popular items' widget doesn't display legal catalog items

</td><td>

The 'Popular items' widget doesn't display relevant catalog items specific to the category chosen. When changing the category, users can find that catalog filters display related items but not the 'Catalog item' widget.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1781293

 [KB1710481](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710481)

</td><td>

com.glide.encryption. enable\_attachment\_ key\_ui=TRUE has different behavior in Xanadu

</td><td>

When com.glide.encryption. enable\_attachment\_ key\_ui=FALSE there's no issue. In Washington DC, the property is set to true but the issue didn't occur.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1794718

</td><td>

A knowledge category displays as '\{\{::category.label\}\}' when the language is non-English

</td><td>

Build information: Xanadu EA Issue Description: \[Xanadu EA\]: Knowledge category is shown as \{\{::category.label\}\} when language is non-English

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1803497

</td><td>

attachment.upload.success event is triggered incorrectly, and cannot be relied on to disable the **Catalog - Order Now** button

</td><td>

When uploading multiple attachments consecutively, the 'attachment.upload.success' event is triggered immediately after the first batch of attachments finishes uploading instead of waiting for all batches to complete. The attachment modal is also hidden before the upload process is fully completed.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1809948

 [KB1703663](https://hi.service-now.com/kb_view.do?sysparm_article=KB1703663)

</td><td>

Using the auto-fill function in an Edge browser triggers a search of all reference fields in the Service Portal catalog form

</td><td>

Starting from Edge browser 129.0.2792.52+, when the user fills the personal information with the auto-fill function on the Service Catalog form in the Service Portal, it triggers a search of all reference fields in the form. Sometimes this causes the form to freeze, and it must be reloaded to proceed.

</td><td>

1.  Enable the auto-fill function on Edge browser 129.0.2792.52+.
2.  Open a service catalog with multiple reference fields in Service Portal.
3.  Select one of the fields and fill the personal information by auto fill.

 Expected behavior: Only fields that are related to personal information are populated.

 Actual behavior: Fields related to personal information are populated, but all the reference fields on the form were in focus and triggered the searches of the fields.

</td></tr><tr><td>

Service Portal

 PRB1823470

</td><td>

After an applied autofill, the cursor is moved to another field

</td><td>

The cursor focus moves to another field. Also, the **List collector** field is expanded and the focus is moved to a dropdown field. An empty value is displayed in the dropdown field.

</td><td>

 

</td></tr><tr><td>

Service Portfolio Management

 PRB1808035

 [KB1705403](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705403)

</td><td>

An error message occurs when submitting a service in the Service Builder

</td><td>

Submitting a service in Service Builder prompts the error message, 'Status can only move forward to retiring or retired or obsolete from operational'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1665612

 [KB1641524](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641524)

</td><td>

Purchased rights in alm\_license are limited by an integer field type

</td><td>

A user can have a value that can only be contained by a long field type, causing issues due to the limitation.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1731774

</td><td>

The 'Software Asset Connections' job is creating install records on retired configuration items

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1775506

 [KB1648325](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648325)

</td><td>

The software lifecycle report in classic view is empty

</td><td>

The report for 'Software Lifecycle reports' table has empty records in the Washington DC Release.

</td><td>

Refer to the listed KB article for details.

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

Software Asset Reclamation

 PRB1795844

 [KB1702053](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702053)

</td><td>

The incorrect user is assigned to a single install per user-based reclamation candidates

</td><td>

Usage/Installs used to create RC belongs to the previous user and aren't current or changed to the user. User aggregate isn't ordered by the user.

</td><td>

1.  Create a single install/low usage for the same user on a device.
2.  Create an install for a few users on other devices.
3.  License all installs by the 'per user' metric.
4.  Run the RC job.

 Notice that RC is stamped by the incorrect user.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB1790386

</td><td>

There's a replication lag caused by 'untagSoftwareModelForUnlicensedInstall' in AutomaticSMRCreation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Entitlements

 PRB1787017

 [KB1650157](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650157)

</td><td>

In Software Asset Workspace, the 'Total cost' is generated incorrectly when the glide.sys.date\_format property value is set to anything other than the default format 'yyyy-MM-dd'

</td><td>

In Software Asset Workspace, the 'Total cost' is generated incorrectly when the glide.sys.date\_format property value is set to dd-MM-yyyy. The Entitlement Total Cost functions properly in the classic view of the alm\_license table, but not in the workspace view. When the default format is used \(yyyy-MM-dd\), the Total Cost calculation is correct on both Software Asset Workspace and the alm\_license table. The root cause of this issue is the base instance client script 'Update total cost onChange subscription', which does not recognize date formats other than 'yyyy-MM-dd' for the start date and end date of the software entitlement in the workspace view.

</td><td>

1.  Set the 'glide.sys.date\_format' property value to dd-MM-yyyy.
2.  Navigate to **Software Asset Workspace** &gt; **License Operations**.
3.  Open any entitlement with the license type as 'Subscription'.
4.  Attempt to change the subscription period to something other than 'Entire Subscription Period'.

 Notice that the 'Total cost' is generated incorrectly due to the new date format preference.

</td></tr><tr><td>

Software Lifecycles

 PRB1759420

</td><td>

Changing the 'phase' data type from the 'string' to a 'choice' value for better reporting

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Models

 PRB1786414

</td><td>

The sam\_admin role failed to load the 'publish to software catalog' list when catalog records aren't readable by role

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Source Control Engine

 PRB1789863

 [KB1652375](https://hi.service-now.com/kb_view.do?sysparm_article=KB1652375)

</td><td>

There's failure to install an app with a dependency that was converted to 'application repository' mode

</td><td>

Trying to install an app with a dependency on another app that was converted from a Store app into a developer app with 'application repository mode' results in failure.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Source Control Engine

 PRB1795465

</td><td>

getRemoteTags doesn't have a timeout specified

</td><td>

If the git server can't be reached, the job can seem to stall indefinitely. The job can run for days.

</td><td>

1.  Create an app in Studio.
2.  Link to Source Control successfully.
3.  Set a breakpoint in AGitRepository.getRemoteTags\(\).
4.  Refresh the repository \(perhaps via sys\_repo\_config\).
5.  Make the git server unresponsive when the breakpoint from step 3 gets reached.
6.  Resume the breakpoint.

</td></tr><tr><td>

Subscription Management

 PRB831241

</td><td>

A unique key violation is detected by the database \(Duplicate entry\) on the ua\_app\_usage table

</td><td>

When Usage Analytics is used, the following error generates intermittently: 'FAILED TRYING TO EXECUTE ON CONNECTION'.

</td><td>

 

</td></tr><tr><td>

Survey Management

 PRB1817570

 [KB1704997](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704997)

</td><td>

HTML formatting and line breaks are no longer working on the 'Assessment' page

</td><td>

The HTML formatting and line breaks in the Document Titles \(sys\_ui\_title\) are not functioning correctly. As a result, the descriptions and other instructions are rendered as raw HTML code instead of plain text on the 'Assessment' instance pages.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Import Sets

 PRB1796959

</td><td>

JDBC data source errors are generic messages starting in Washington DC, such as 'Cannot invoke 'java.util.Map.keySet\(\) because 'this.fImportSourceFields is null'

</td><td>

Since the Washington DC upgrade, it appears that users aren't directly seeing the JDBC Data Sources SQL errors in progress workers or when doing a 20 records load on the UI. It is replaced by a generic message 'Cannot invoke "java.util.Map.keySet\(\) ...this.fImportSourceFields" is null'. When checking the agent log file of the MID Server, the JDBC SQL error that should be present isn't in the progress worker log. Before Washington DC, these kind of SQL errors were retrieved directly in the instance and it wasn't needed to retrieve the MID Server logs.

</td><td>

1.  Set up a JDBC data source with incorrect credentials.
2.  Test load 20 records for the data source.

 An error message is noticed in the UI 'Cannot invoke "java.util.Map.keySet\(\)" because "this.fImportSourceFields" is null'.

</td></tr><tr><td>

System Import Sets

 PRB1804838

 [KB1705523](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705523)

</td><td>

New fields with double byte characters are not created automatically upon loading data

</td><td>

When loading data, new fields are created if the loading file or data source contains headers that don't match the fields in the import set table. Since the Xanadu release, new fields are not created when headers contain double byte characters, and a warning message is logged in the import log. This occurs even if com.glide.use\_column \_name\_optimizer property is 'true'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Table Administration and Data Management

 PRB1527645

 [KB1225737](https://hi.service-now.com/kb_view.do?sysparm_article=KB1225737)

</td><td>

A null pointer exception is thrown by the database view where the driving table is a TPC child of the task table, which has off-rowed fields on task\_offrow

</td><td>

The error occurs if the following conditions exist: 1. A table which is a direct child of task has TPC as its extension model. 2. At some point in the past ServiceNow has executed a change to off-row one or more columns from the task table to workaround a dynamic row size error. 3. A database view is created with just the TPC table as a view table, with no other view table to join. 4. The view table has the default of no view fields being defined.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Table Administration and Data Management

 PRB1735107

</td><td>

The 'Data Management' job state doesn't update correctly when the node stops abruptly

</td><td>

A 'Data Management' job state in 'sys\_dm\_delete' doesn't update correctly when the node processing the DM job stops/restarts abruptly.

</td><td>

 

</td></tr><tr><td>

Table Administration and Data Management

 PRB1743783

</td><td>

setAllowCascadeDelete method of GlideMultipleDelete is not scriptable

</td><td>

Users are referred to use GlideMultipleDelete when cleaning up their data. Large amounts of data cleanup is a requirement for users with the recent change in data footprint policies. Enabling platform features for users to better manage their data footprint is essential.

</td><td>

 

</td></tr><tr><td>

Table Administration and Data Management

 PRB1792808

</td><td>

Running an instance health scan table check throws a null pointer expection error if a sys\_storage\_alias record has an empty storage\_table\_name

</td><td>

Table check fails with the error message 'Rhino error: java.lang.NullPointerException'.

</td><td>

 

</td></tr><tr><td>

Table Rotation

 PRB1726430

</td><td>

Rotations for sys\_scheduler\_job\_history\_node and sys\_scheduler\_job\_history were incorrectly created in the Vancouver release

</td><td>

The sys\_s7r\_job\_history\_node0000 table is missing the primary key.

</td><td>

 

</td></tr><tr><td>

Third-party Software

 PRB1793365

</td><td>

Commons-beanutils hits BEANUTILS-509, causing severe default thread contention, leading to 429s

</td><td>

In a few cases, this caused a node to completely hang indefinitely because all the threads were attempting to enter a synchronized block of a WeakHashMap that was being hogged by a thread stuck in an infinite loop.

</td><td>

 

</td></tr><tr><td>

Time Card Management

 PRB1785263

</td><td>

Managers are unable to copy timecards

</td><td>

When a manager attempts to copy time cards for one of their reports, the system returns \{0\} time cards created.

</td><td>

1.  Impersonate a manager in an instance.
2.  Select a user from the user dropdown.
3.  Select the **Copy time card** button.
4.  Select the date for the time sheet.
5.  Select **Okay**.

 Observe the error message.

</td></tr><tr><td>

UI Field Administration

 PRB1779043

</td><td>

There's an error inputting a decimal value into a decimal field when glide.system.locale has a value set

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Navigate to Agent Workspace.
3.  Open any incident.
4.  Enter '123456789.09' on the **Test** field and select out of the field

 Notice that the below message is seen: 'Could not parse 123.456.789,6 as a number'. This issue is reproducible on any workspace and when the system property glide.system.locale isn't empty.

</td></tr><tr><td>

UI Field Administration

 PRB1793495

</td><td>

Service Operations Workspace \(SOW\) has poor performance on **CI** fields

</td><td>

Poor performance of the **CI** field and its reference qualifier within an incident record in SOW. The issue is only seen in workspace and not in the platform/native view.

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

UI Form Administration

 PRB1767288

 [KB1710682](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710682)

</td><td>

Adding the **Sort** button on sys\_ux\_list opens new record instead of allowing edits

</td><td>

When a filter has a sort condition and the filter tries to load or add a new condition, there's an error thrown that causes the filter to not load or to not add a new sort row.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1783850

 [KB1651462](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651462)

</td><td>

High memory usage by viewrule\_all\_cache \(Workspace View Rules\)

</td><td>

The viewrule\_all\_cache can consume excessive memory on application nodes. This can cause memory contention/increased garbage collection/application node performance degradation.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Policies

 PRB1725664

</td><td>

Date validation isn't working as expected when the user timezone is set to the 'other' region

</td><td>

The platform considers the system \(actual machine which user uses\) timezone to calculate the time calculation rather than the instance timezone which the user is in. An error message displays.

</td><td>

 

</td></tr><tr><td>

UI Scripts

 PRB1784983

 [KB1649352](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649352)

</td><td>

Duplicate UI scripts that have the same exact name prevent a workspace page from loading

</td><td>

Workspace pages fail to load if there are duplicate UI scripts with the same API name in the sys\_ui\_script table. This is caused by a functional change to how the workspace UI scripts are called.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Upgrade Center

 PRB1797126

 [KB1704373](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704373)

</td><td>

The **Save Merge** button throws a 'GlideList is not defined' error for ACL records when trying to resolve conflicts in Xanadu

</td><td>

When resolving conflicts for skipped records from an upgrade, the 'Save Merge' record throws an error for ACL records in Xanadu. The error message reads, 'Error MessageonSubmit script error: ReferenceError: GlideList2 is not defined:' and the record is not updated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Upgrade Center

 PRB1812035

</td><td>

Records with &lt;sys\_es\_latest\_script action="INSERT\_OR\_UPDATE"&gt; in the XML are listed in the plugin update list as 'skipped' during the plugin upgrade

</td><td>

It seems that the entire XML file is diffed here, when users would expect only the contents of the record to matter.

</td><td>

1.  Choose any application that has records with &lt;sys\_es\_latest\_script action="INSERT\_OR\_UPDATE"&gt; in the xml.
2.  Side-load the application via 'install application' from either the file or Nexus.
3.  Navigate to sys\_upgrade\_history.
4.  Select the recent record.
5.  Check records with &lt;sys\_es\_latest\_script action="INSERT\_OR\_UPDATE"&gt; in the XML are in the 'Changes Applied' tab.
6.  Repair the application.
7.  Navigate to sys\_upgrade\_history.
8.  Select the recent record.
9.  Check records with &lt;sys\_es\_latest\_script action="INSERT\_OR\_UPDATE"&gt; in the XML are marked as 'Skipped'.
10. Check logs to confirm the record is skipped because of sys\_es\_latest\_script action.

</td></tr><tr><td>

UX Framework

 PRB1754230

</td><td>

A data resource doesn't pick up default values when input values are missing

</td><td>

The 'Data Visualization API for table data source' defines 'useDataCache' as a query parameter in the URL. Sending this value as null marks the URL as invalid and the data resource throws an invalid URL error.

</td><td>

1.  Add 'Data Visualization API for table data source' to any page in UI Builder \(UIB\).

Observe that the output value returns a valid JSON.

2.  Save the page.
3.  Navigate to 'Page definition'.
4.  Remove the 'useDataCache' input value from the data resource JSON in the **Data** field.
5.  Open the page again in UIB.
6.  Open the 'Data resource' configuration.

 Expected behavior: The output is the same as in step 1.

 Actual behavior: An invalid URL error is shown.

</td></tr><tr><td>

UX Framework

 PRB1766794

</td><td>

Closing multiple tabs quickly converts an existing workspace tab to a non-functional 'Details' workspace tab that can't be closed

</td><td>

A non-functional 'Details' tab appears when closing inactive tabs quickly.

</td><td>

1.  Open CWF or SOW workspace.
2.  Open ten existing 'incident' tabs.
3.  Click through the tabs to make them active, but keep switching and do not let them load all the way.
4.  Close an inactive tab before the new tab loads.
5.  Continue closing tabs this way until a non-functional tab is observed.

 Expected behavior: The subtab details get closed out.

 Actual behavior: The non-functional details tab appears when closing out inactive tabs quickly.

</td></tr><tr><td>

Virtual Agent

 PRB1763848

</td><td>

Manual account linking fails non-admin users

</td><td>

There's errors in the logs.

</td><td>

1.  Navigate to an instance.
2.  Log in as a non-admin user.
3.  Start a conversation on Teams.
4.  Select **Link to servicenow**.

 The chat fails after choosing any topic. The channel user profile isn't created for the user.

</td></tr><tr><td>

Virtual Agent

 PRB1784826

</td><td>

A JavaScript console error appears when the Virtual Agent chat is open in the Service Portal UI

</td><td>

A JavaScript console error appears in the Service Portal UI as a result of a keyboard shortcut API returning with a code in the 400-500 range.

</td><td>

1.  Select **Track your Tickets**.
2.  Open any case.
3.  Select the chat option to launch the Virtual Assistant in the Engagement Messenger.

 Notice that the console error appears on your browser and in JavaScript.

</td></tr><tr><td>

Virtual Agent

 PRB1789855

</td><td>

In Virtual Agent after a Washington DC upgrade, every input that matches more than one keyword throws an error

</td><td>

Virtual Agent should display all topics that match a keyword, but it displays a technical error message or occasionally hangs.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1814179

</td><td>

Selecting links causes the link to be opened inside Web Client

</td><td>

Selecting **T&amp;E Card Request** breaks the Now Assist Virtual Agent \(NAVA\) experience.

</td><td>

 

</td></tr><tr><td>

Visual Task Boards

 PRB1765065

</td><td>

ChecklistItemResponder is too slow to efficiently scale normal usage of the platform, resulting in a backlog in the record watcher queue

</td><td>

ChecklistItemDAO has the functions canRead/canDelete that triggers an ACL.

</td><td>

Trigger the ChecklistItemResponder with a check list has 50+ items.

</td></tr><tr><td>

Web UX Runtime

 PRB1776097

 [KB1709413](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709413)

</td><td>

Chats close automatically on the workspace after they are opened within a few seconds

</td><td>

This issue was introduced in Washington DC. Chats are closed automatically in the workspace after they are opened within a few seconds. Shortly after the chat window is opened, it is then closed, and the chat state is set to 'Closed Complete'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Work Order Management

 PRB1823305

</td><td>

Work order template assignment groups are not honored

</td><td>

When using work order templates and setting a specific assignment group, the group isn't set and a different group is assigned. Additional fields that are configured on the work order templates can't be processed properly. As a result, fields like 'assignment\_group' that are defined in the WOT of the work order template aren't applied properly.

</td><td>

 

</td></tr><tr><td>

Zing Text Indexing and Search Engine

 PRB1759390

 [KB1649571](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649571)

</td><td>

Global search no longer auto-opens the result record when the **Short description** field is empty

</td><td>

There's an error in the browser console: 'Uncaught TypeError: Cannot read properties of undefined \(reading 'title'\)...'

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>## All Other Fixes

To view a list of all other PRBs fixed in Yokohama, refer to [All other Yokohama fixes](yokohama-all-other-fixes.md).

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


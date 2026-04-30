---
title: Yokohama Patch 9
description: The Yokohama Patch 9 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-11-06"
reading_time_minutes: 64
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 9

The Yokohama Patch 9 release contains important problem fixes.

-   **Yokohama Patch 9 was released on November 6, 2025.**
    -   Build date: 11-02-2025\_1032
    -   Build tag: glide-yokohama-12-18-2024\_\_patch9-10-22-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y09.00.xlsx).

## Overview

Yokohama Patch 9 includes 208 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp9.png "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 9 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 9, refer to [KB2587878](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2587878).

## Changes in Yokohama Patch 9

-   **[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)**

    For Now Assist new features and changes, see [Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md).


-   **[Show borders between search result cards in portal search](https://www.servicenow.com/docs/access?context=show-borders-search-result-cards-portal-search&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Display borders between search result cards on the search results page for portal search applications.

-   **[Show borders between search result cards in global search](https://www.servicenow.com/docs/access?context=show-borders-search-result-cards-global-search&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Display borders between search result cards on the global search results page.


-   **[Show borders between search result cards in portal search](https://www.servicenow.com/docs/access?context=show-borders-search-result-cards-portal-search&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Display borders between search result cards on the search results page for portal search applications.

-   **[Show borders between search result cards in global search](https://www.servicenow.com/docs/access?context=show-borders-search-result-cards-global-search&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Display borders between search result cards on the global search results page.


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

 PRB1893600

 [KB2178333](https://hi.service-now.com/kb_view.do?sysparm_article=KB2178333)

</td><td>

RecordFamilyResolver.archiveTableHasACLTerms needs more optimization

</td><td>

Performance issues with reports on instances with a big number of archive tables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Access Control

 PRB1915184

 [KB2400619](https://hi.service-now.com/kb_view.do?sysparm_article=KB2400619)

</td><td>

Security constraints prevent access to a requested page when visiting task.list

</td><td>

Failing a Deny ACL from anywhere in the hierarchy prevents table access to the list of a parent table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1878917

</td><td>

Text doesn't persist if the user navigates away from the email composer when drafting a reply

</td><td>

Text in the email composer disappears when the user navigates to a different tab. This only occurs when replying via the activity stream tile, not when composing a new email.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1930654

</td><td>

The legacy health dashboard doesn't tell the user that the dashboard is deprecated/no longer supported

</td><td>

Users have bookmarked, saved, or edited links to the legacy health dashboard, meaning they can still access it. There's a lot of confusion on why the dashboard is no longer working as intended. There should be a message to tell the user this dashboard has been migrated to CMDB Workspace.

</td><td>

1.  Check out a Washington DC instance.
2.  Make a favorite for Health Dashboard - CMDB view.
3.  Upgrade your instance to Xanadu or beyond.
4.  Select the bookmark for the CMDB view.

 Expected behavior: When users navigate to the legacy dashboard, they should be able to see a message telling them to use the new health dashboard and that the legacy dashboard is no longer supported.

 Actual behavior: See that the legacy health dashboard has some broken widgets, no colors, etc. but there is no indication that this dashboard is retired or has been migrated.

</td></tr><tr><td>

UI Field Administration

 PRB1877769

 [KB2182152](https://hi.service-now.com/kb_view.do?sysparm_article=KB2182152)

</td><td>

The **info \(i\)** icon for reference catalog variables is missing on requested items and the 'SCTASK' form under Service Operations Workspace

</td><td>

The issue is seen with all the workspaces since Yokohama.

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

Activity Stream

 PRB1928872

</td><td>

The CanReadRepo class encounters a ConcurrentModificationException

</td><td>

This concurrency issue arises because the class uses a HashMap, which is not thread-safe. The HashMap should be replaced with a ConcurrentHashMap to ensure thread-safe operations and prevent the exception.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment for Case Service channel

 PRB1946390

</td><td>

The case task isn't working properly for CCaaS external routing

</td><td>

The assignment isn't happening since there's no mapping field available for CCaaS partners to use and store their external ID onto the 'Case task' table.

</td><td>

1.  Configure the instance to route the case tasks through external CCaaS.
2.  Create a case task in the instance.

 Expected behavior: The case task should be routed to the agent using the external routing mechanism. The case task should be picked up by the CCaaS events and assigned to the identified agent. Further events should also be triggered for this task.

 Actual behavior: Currently the case task doesn't get assigned to the agent.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1933671

</td><td>

AWA \(Advanced Work Assignment\) uses the system locale timezone when writing to logs

</td><td>

The AWAEventUtil code changes the global locale setting, causing the 'localhost log' to be written in UTC rather than PST \(standard\).

</td><td>

1.  Log in to an instance.
2.  Install the Advanced Work Assignment \(AWA\) plugin.
3.  Navigate to **Advanced Work Assignment** &gt; **Service Channels** &gt; **New**.
4.  Enter the following values:
    1.  Name: test
    2.  Index order: 100
    3.  Table: Incident
    4.  Utilization condition: Short Description is not empty
5.  Submit it.
6.  Ensure that the channel is active.
7.  Create a new queue.
8.  Open the record created in step 3.
9.  Choose the 'Queue' related list.
10. Create a new 'Queue' record.
11. Enter in all the mandatory fields.
12. Submit it.
13. Enable Logging.
14. Open the record created in step 3.
15. Select **Queues** and **New**.
16. Name it 'test-queue'.
17. Submit it.
18. Check the localhost log.
19. Have the terminal open for all the nodes.
20. Tail the localhost log.
21. Navigate to **Incident** &gt; **Create New**.
22. Enter in something.
23. Submit it.

 Observe that the timestamp zone has changed, and some lines are in the previous timezone and others are in UTC.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1938992

</td><td>

High AWA assignment cycle times for impact voice call routing

</td><td>

A user is uptaking in NVC and they are facing slow response times for call routing. It's taking ~12 seconds to route the call to agent. Each AWA assignment cycle is taking ~11 secs and out of which ~8 secs is being spent for Agent Map creation. Expected response times should be less than a second as there's no other load in the system.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1942061

</td><td>

Lack of ability to track end-to-end AWA Assignment times

</td><td>

There's currently a gap in performance measurement of the AWA offer work API and manual assignment API, where there is no way to accurately determine the time difference between when an external AWA assignment API call was made and when the work item assigned\_to would be updated to the assigned agent. The admin lacks context as to when the request actually gets processed and the work item gets assigned \(and by extension, the inbox card shows up in the agent's inbox\). Another limitation with the current design is that it only persists the offered\_on for the final API invocation, which led to work item acceptance. If there were multiple agents which were offered the work item via these APIs, this context is lost.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1944387

</td><td>

The 'Create Segment On WorkItem Accept' business rule runs unnecessarily when a previous accepted work item exists

</td><td>

 

</td><td>

1.  Call the 'Offer work' API on an interaction.
2.  Accept the work item.
3.  Clear out the assigned\_to on the interaction.
4.  Call the offer work API on the same interaction.

 Expected behavior: The 'Create Segment On WorkItem Accept' business rule shouldn't be triggered for the old work item.

 Actual behavior: The 'Create Segment On WorkItem Accept' business rule is triggered for the old work item.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1950558

</td><td>

Advanced Work Assignment \(AWA\) should be able to determine if the work item is rejected due to time out or Asynchronous Message Bus \(AMB\) disconnection

</td><td>

When the work item times out, the work item reason on the awa\_work\_item\_rejection table is 'Timed out' instead of 'AMB connection lost'.

</td><td>

1.  Install the Agent Chat plugin with the demo data.
2.  Open the AWA assignment rule.
3.  Update the timeout time to 15 seconds.
4.  Open a browser \(browser 1\).
5.  Log in to the workspace as an agent in browser 1.
6.  Open another browser \(browser 2\).
7.  Log in to the instance as a requestor.
8.  Open the URL /sn-va-web-client-app.do in browser 2.
9.  In browser 1, close the workspace tab completely as an agent.
10. Notice that the agent presence will not be set to offline immediately because the default idle check gives a 5 min buffer, and the agent is still available to receive work item at the moment.
11. In browser 2, start the live agent handoff.
12. Wait for 15 seconds so the work item will be timed out.
13. As an admin, navigate to the awa\_work\_item\_rejection table.
14. Check the rejection record for the previous interaction.

 Expected behavior: The reason should be 'AMB connection lost'.

 Actual behavior: The rejection reason is 'Timed out'.

</td></tr><tr><td>

Agent Chat

 PRB1839064

</td><td>

Refreshing the page causes the active chat shell to disappear, but refocusing on the live agent in a separate window restores the chat shell

</td><td>

This issue is observed in version 24.4.2 of Workspace App Shell TD.

</td><td>

1.  Ensure the Agent Chat plugin is installed.
2.  Open Service Operation Workspace as an admin in a window.
3.  Set the admin as available as a chat agent.
4.  Attempt to log in to Service Operations Workspace as Abel Tuter in an incognito window.
5.  Attempt to connect to a live agent.
6.  Accept the chat as an admin.
7.  End the chat.
8.  Keep the tab open.
9.  Initiate the chat again as Abel Tuter.
10. Accept the chat as an admin.
11. Refresh the admin page

 Observe that the active chat shell window isn't opening unless the live agent is not in focused by Abel Tuter.

</td></tr><tr><td>

Agent Chat

 PRB1846962

</td><td>

Chat disappears if the user refreshes the page when a list is in the open tabs of Service Operations Workspace \(SOW\)

</td><td>

Refreshing the page causes the chat to disappear until the tab with the simple list is opened.

</td><td>

1.  Create a single score related to a simple list on the home page.
2.  Open the instance in a browser.
3.  Impersonate a system administrator.
4.  Open SOW.
5.  Navigate to **Inbox** &gt; **Available**.
6.  Open a new browser in incognito mode.
7.  Open the instance in the incognito browser window.
8.  Impersonate another user.
9.  Open /esc.
10. Select **Open chat Window.**
11. Select **Contact Live Agent**, if necessary.
12. Return back to the first opened.
13. Accept the chat.

 Observe that in the chat window opened in first browser, unexpected behaviors occur when the simple list is open in the SOW tabs.

</td></tr><tr><td>

Agent Chat

 PRB1943902

</td><td>

Create a new exclusive channel to receive work items on Agent Chat

</td><td>

The inbox component should subscribe to a new Asynchronous Message Bus \(AMB\) channel other than the existing AWA/work\_item channel to reduce the chance of being interfered with by other components subscribing to the same channel. The AMB publish function used in the workItemResponder should be updated to take the trace id.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1921724

</td><td>

Improve ResponsePostProcessor time when the table is early binding

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1930534

</td><td>

When used on service portals, 'Exact Match' should honor search sources

</td><td>

When using the 'Exact Match' feature on a service portal, the results of the exact match lookups should be limited to the sources which are included in the search profile, and honor the filters set on the search sources.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1942680

</td><td>

Web search isn't working in Zurich and recent store apps

</td><td>

 

</td><td>

1.  Navigate to **/esc**.
2.  Start the web search by selecting the **Globe** icon.
3.  Query, 'Who is the president of the US.'

 Expected behavior: The web search query goes through.

 Actual behavior: The user receives a 'Sorry there was a problem' message.

</td></tr><tr><td>

AI Search

 PRB1799463

</td><td>

The 'Clone' functionality fails for search applications

</td><td>

A clone isn't created when using the Clone UI Action, even though it asks for the name of the cloned profile.

</td><td>

1.  Navigate to **All** &gt; **Search Applications**.
2.  Select any search application.
3.  Select the **Clone** UI Action.
4.  Observe that it re-routes to another form that asks for name of the cloned profile again.

 Notice that no clone is created.

</td></tr><tr><td>

AI Search

 PRB1859870

</td><td>

Removing two business rules and a dictionary attribute

</td><td>

This issue was observed in Xanadu and Yokohama.

</td><td>

1.  Provision an instance using an older glide version.
2.  Apply the fix in PRB1836358 by using the script.
3.  Observe that two business rules and a dictionary attribute were added.
4.  Upgrade the instance to latest Xanadu or Yokohama build.

 Expected behavior: The business rules and dictionary attributed added were removed.

 Actual behavior: The business rules and dictionary attribute remain on the instance.

</td></tr><tr><td>

AI Search

 PRB1940661

</td><td>

The hasPendingIndex API is broken

</td><td>

The sn\_ais.AisUtil.hasPendingIndex\(tableName, recordSysId, embeddingModelName, semanticIndexName\); call fails.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1917701

</td><td>

Empty suggestions are stored when the user query is '\*\*\*'

</td><td>

 

</td><td>

1.  Enable Dynamic Window.
2.  Search '\*\*\*'.

 Observe that empty suggestions are stored as queries are normalized and punctuations are stripped.

</td></tr><tr><td>

AI Search UX

 PRB1917704

</td><td>

Punctuation isn't removed for languages other than English

</td><td>

 

</td><td>

1.  Turn on Spanish language.
2.  Enable DW/FPE.
3.  Search for '¿Qué es el spam?'

 Observe that '¿' isn't removed in the suggestion utterances table.

</td></tr><tr><td>

AI Search UX

 PRB1930672

</td><td>

Service Portal Genius Result \(GR\) synthesized response flashes and changes text size

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1935078

</td><td>

Make the border for the Search Result card configurable

</td><td>

There are no borders for the Search Result card.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1936251

</td><td>

KG citation list view is empty

</td><td>

A message says 'Found no records' when a query should produce results.

</td><td>

1.  Navigate to **/sp**.
2.  Query 'What asset does Abel Tuter have' in the portal search box.
3.  View the assets info and multiple assets citations.
4.  Select **View Records**.

 Expected behavior: The user is direct to KG citation list view and assets show up in the list.

 Actual behavior. A message says, 'Found no records'.

</td></tr><tr><td>

AI Search UX

 PRB1937984

</td><td>

The caller is not in the scope rhino.global when called from Now Assist in Virtual Agent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1941065

</td><td>

Response loads even after a 15 second timeout on the portal

</td><td>

The portal stops the loading sign, which means it's reached the 15 second timeout. The response to the user's query loads after that.

</td><td>

1.  Navigate to a portal with DW enabled.
2.  Search for any query, such as 'How to create a new user'.

 Expected behavior: Once the portal times out, it doesn't load the response.

 Actual behavior: The portal stops the loading sign, which means it's reached the 15 second timeout, but the response loads after that.

</td></tr><tr><td>

AI Search UX

 PRB1942589

</td><td>

Increased timeout from 15s to resolve frequent no Genius Results on Portal

</td><td>

This issue occurs on Dynamic Window \(DW\) enabled on Portal with Model GPT OSS, and takes longer for a response to return than in any other models.

</td><td>

 

</td></tr><tr><td>

AI Service - Glide Interfaces

 PRB1900176

</td><td>

ExtractItems\(\) pops the solutionIds from the original array

</td><td>

On an instance with more than 40\(JOB\_REQUEST\_COUNT\_LIMIT\) solutions in 'Waiting For Training' state at present, once the sys\_trigger is triggered, all these solutions will be moved to the 'Training is Cancelled' state and new solutions will be created and retried again.

</td><td>

 

</td></tr><tr><td>

AI Service - Glide Interfaces

 PRB1902435

</td><td>

In handleWaitingForTrainingState, there is a missing second argument in isJobSubmitted\(\)

</td><td>

In handleWaitingForTrainingState, a solution ID is not passed to the isJobSubmitted\(\) function, resulting in an execution of the 'if' condition. Even if the job is submitted, the solution is cancelled and retried until it reaches its last retry.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1894963

</td><td>

Data Visualization drilldown doesn't follow previous filters

</td><td>

On Data Visualization, only the first-level drilldown honors the selected filters. This issue was observed in Xanadu and Yokohama.

</td><td>

1.  Navigate to an instance.
2.  Open a Data Visualization.
3.  Select a column.
4.  Notice that it contains a drilldown.
5.  Select another column.
6.  Notice that it contains a drilldown with a daily view.

 Observe that only the first-level drilldown honors the selected filters, and that subsequent drilldowns \(level 2 and beyond\) reset to the original selection context, rather than chaining the filters from the intermediate drilldown.

</td></tr><tr><td>

Analytics Data API

 PRB1921406

</td><td>

POST /api/now/charts/data returns 500 status code when the table is not valid

</td><td>

POST /api/now/charts/data should return the 400 HTTP status code, with the error message 'Table is not valid: null.' Instead, it returns the 500 HTTP status code.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1926918

</td><td>

The 'Process analytics cache pre-fetch queue' job leads to OutOfMemoryError and the node restarts

</td><td>

When the user runs the 'Process analytics cache pre-fetch queue' job, it loops in ChangeCheckConflictsSNC script include.

</td><td>

1.  Create a test\_breakdown table.
2.  Add a field:
    1.  Name: Name.
    2.  Type: String.
    3.  Length: 50.
3.  Populate two million records in the table with names such as Name1, Name2, etc.
4.  Create a breakdown source on test\_breakdown without any condition.
5.  Create a breakdown of the above breakdown source.
6.  Create a test\_indicator table.
7.  Add a field:
    1.  Name: ref\_breakdown.
    2.  Type: Reference.
    3.  Reference: test\_breakdown.
8.  Populate two million records in test\_indicator with reference to all the records in test\_breakdown, respectively.
9.  Create an indicator source based on test\_indicator, without any condition.
10. Create an indicator based on the above indicator source.
11. Navigate to the breakdown created in step five.
12. Add a breakdown mapping on the **test\_incident** and **ref\_breakdown** field.
13. Navigate back to the indicator.
14. Add the breakdown.
15. Change the system properties:
    1.  com.snc.pa.dc.hsql.max\_row\_count\_indicator\_source = &gt; 10000000.
    2.  com.snc.pa.dc.max\_breakdown\_elements\_limit = &gt; 10000000.
16. Collect 1-day score for the indicator.
17. Create a new dashboard.
18. Add a visualization:
    1.  Type: Single score.
    2.  Source: Indicator created in step 10.
19. Add a filter:
    1.  Type: Single select.
    2.  Source: Breakdown created in step five.
20. Open any memory inspection tool and check the current memory footprint.
21. Open the filter and select a value.

 Notice that the memory footprint steadily increases by about 800 million until the score is displayed.

</td></tr><tr><td>

Analytics Data API

 PRB1945218

</td><td>

Memory leak of JSON serializer in multivis API

</td><td>

Each time a data request is processed, a new serializer is created and not released unless a GC is performed, which causes a memory leak.

</td><td>

1.  Create a dashboard.
2.  Add a tab and add 50 identical single score vis:
    1.  Source: incident.
    2.  Condition: sys\_id is empty.
3.  Duplicate the tab 9 times so there are 500 visualizations in total.
4.  Disable the property 'com.snc.dashboard.streaming.enabled'.
5.  Stop the instance and start again, but don't access the instance in the browser.
6.  Use VisualVM to capture the heapdump.
7.  Search for 'IntegerDateSerializer' in the object list.
8.  Observe that there are 0 results.
9.  Access the dashboard created in step 1.
10. Go over all 10 tabs.
11. Use VisualVM to capture the heapdump.
12. Search for 'IntegerDateSerializer'.
13. Observe that there are ~500 results.
14. Repeat steps 8 through 11 \(get the heapdump and search\).

 Observe that there are ~1000 results. Each time a data request is processed, a new serializer is created and not released unless a GC is performed, which causes a memory leak.

</td></tr><tr><td>

App Engine Studio - Family Channel

 PRB1923756

</td><td>

The Record Producer remains as the original template's one in a newly created app

</td><td>

When using the AES Template, the Record Producer remains as the original template's one, but it should be the one in the new app.

</td><td>

1.  Create an app \(App1\).
2.  Create a new table in App1.
3.  Create a Record Producer with the table.
4.  Create a flow with the action 'Get Catalog Variables'.
5.  Set the Record Producer in it.
6.  Save.
7.  Create a template with App1.
8.  Create a new app \(App2\) with the template.
9.  Check the Record Producer that was set in the action 'Get Catalog Variables'.

 Expected behavior: The Record Producer is the one in the new app \(App2\).

 Actual behavior: The Record Producer is the one in the original app \(App1\).

</td></tr><tr><td>

Application Install Engine

 PRB1936285

</td><td>

During node re-start, the system downloads version expects a higher store version

</td><td>

After a node restarts, the user sees the soft dependencies in the dependency manager are populated by the versions. The root cause is the artifacts are loaded from a file during node restart, and that is overwriting the active plugins information in Dependency Manager.

</td><td>

1.  Open a multi-node instance that has 15.0.5 as a version.
2.  Install 15.0.5 and other optional plugins.
3.  Upgrade to 15.0.17.

 After the node restarts, soft dependencies in the dependency manager are being populated by the base instance versions.

</td></tr><tr><td>

Async HTTP Client

 PRB1937994

</td><td>

Async HTTP client connection pool isn't optimized

</td><td>

Connection pooling is limited to 60 per host and 180 total, when it should host 300-900.

</td><td>

1.  Log in to an instance.
2.  Navigate to **/sp endpoint**.
3.  Enter 'What is spam'.
4.  Select **New conversation** after 35s.
5.  Enter 'What is spam' again.

 Notice that second set of requests don't benefit from connection pooling, and limits it to 60 per host and 180 total.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1874569

</td><td>

Opening a form with 'view' can fail in Automated Test Framework \(ATF\) due to case sensitivity

</td><td>

This issue was observed with a new ATF test in the Performance Analytics application.

</td><td>

1.  Create a new ATF test.
2.  Add a 'Navigate to Module' step to navigate to 'Automated Indicators' in the Performance Analytics application.
3.  Add an 'Open a Record in List' step to open any record in that list.
4.  Run the test.
5.  Wait until the test completes.
6.  View the result.

 Expected behavior: The test passes.

 Actual behavior: Test fails with the output 'Expected to open the 'Automated' view of the form, but actually opened to the 'automated' view.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1922654

</td><td>

**Automated Test Framework test** UI action fails due to a timeout error

</td><td>

There appears to be a race condition introduced in Yokohama. Tests that previously passed in Xanadu are now failing some of time when waiting for a response from the intent channel.

</td><td>

1.  Navigate to **Automated Test Framework \(ATF\)** &gt; **Tests**.
2.  Create a test.
3.  Add test step by opening an existing record with values:
    -   Form: SOW Workspace
    -   Table: sc\_task
    -   Record: Select any record
4.  Add test step by:
    1.  Select a UI action or UI action visibility.
    2.  Select **Save** for the UI action.
5.  Clear the instance cache and browser cache.
6.  Using an incognito browser session.
7.  Log in.
8.  Navigate to the test.
9.  Run the test.

 Expected behavior: The test should pass every time.

 Actual behavior: The tests fails intermittently due to an 'Timed out waiting for intent feedback' error.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1880009

</td><td>

Attachments aren't uploaded in the 'Agent Chat' window from HR Agent Workspace

</td><td>

This is happening for HR Core.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1933236

</td><td>

Add RCA to support 'Ask a question' with enhanced chat

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB1889628

</td><td>

List declarative actions aren't working

</td><td>

 

</td><td>

1.  Create a list declarative action.
2.  Implement as a client script.
3.  Set the client script to 'console.log\(''Test''\)'.
4.  Set the table as 'incident'.
5.  Navigate to the incident list.
6.  Select the declarative action.

 Notice that no console logs are outputted.

</td></tr><tr><td>

CMDB Data Manager

 PRB1892066

 [KB2217546](https://hi.service-now.com/kb_view.do?sysparm_article=KB2217546)

</td><td>

Policy form doesn't honor retirement definitions correctly in enforced conditions when multiple retirement definitions are enabled

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Condition Builder

 PRB1927599

</td><td>

The condition builder on the presentational list displays all the options instead of the one that was searched

</td><td>

When the user searches for an option, the condition builder displays all the options in a list and highlights the one that was searched. Instead, only the option that was searched should be displayed.

</td><td>

1.  Create a UI Builder page.
2.  Configure the presentational list component.
3.  Open the page in run time.
4.  Select the **Filter** icon.
5.  In one of the fields, search for an option.

 Expected behavior: The list displays only the option that was searched.

 Actual behavior: The list displays multiple options and highlights the one that was searched.

</td></tr><tr><td>

Condition Builder

 PRB1943552

</td><td>

dotWalkConnectedDataBehavior cannot be imported in version 27.0.4

</td><td>

The behavior source files aren't where exports exists after the import.

</td><td>

1.  Open a project where now-dot-walk 27.0.4 is a dependency.
2.  Attempt to import dotWalkConnectedDataBehavior from/now-dot-walk.

 Expected: The import provides the consuming application with the behavior.

 Actual: The import doesn't provide the behavior source files where exports exist.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1846249

</td><td>

Identification and Reconciliation Engine \(IRE\) throws a NullPointerException \(NPE\) when there is a cache flush during IRE processing

</td><td>

 

</td><td>

1.  Run the payload with a break point after'setIndependentQueryFromPayload' method locally.
2.  Create a new break point after the 'setIndependentQueryFromPayload' to stop the thread.
3.  Open another window.
4.  Log in to /cache.do.
5.  Perform the cache flush.
6.  Resume the execution of thread stopped in step 2.

 Observe NPE.

</td></tr><tr><td>

Contract Management

 PRB1913448

 [KB2310704](https://hi.service-now.com/kb_view.do?sysparm_article=KB2310704)

</td><td>

The payment amount and total amount are incorrectly displayed in the local currency value under USD currency

</td><td>

When the user sets a payment amount using a local currency \(for example, NOK\) when selecting **Adjust** on the Contract, the payment amount gets saved on the XML. When re-opening the record in Form view, it defaults to USD, but shows the amount that originally belonged to NOK. This behavior applies to both **payment\_amount** and **total\_cost** fields.

</td><td>

1.  Open a contract from the ast\_contract table.
2.  Select **Adjust**.
3.  Enter a new payment amount and currency, for example, NOK 966.00.
4.  Search and view the same Contract on List view.
5.  Notice that payment amount and total amount are both reflected as \(NOK\)966.00 and \(USD\)96.7669 when selecting **Toggle currencies**.
6.  Open the record in Form view.

 Notice that the payment amount is USD 966.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1792470

</td><td>

Some alters to increase max length are running twice during an upgrade

</td><td>

Multiple updates happen because a sys\_dictionary record has an incorrect field length after finishing the bootstrap batcher.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1923704

</td><td>

Due to an ordering change on Raptor post migration, certificate authentications for API calls may fail and cause '500' errors

</td><td>

When mutual authentication is configured using both protocol profile and system properties, the system property takes precedence. This causes the SSL exchange to utilize the socket factory for client certificate provisioning, bypassing the keystore defined in the protocol profile. Additionally, when mutual authentication is enabled via property configuration, all certificates from the sys\_certificate table are loaded. This can lead to intermittent outbound call failures if expired certificates are cached and used for mutual authentication, resulting in HTTP 500 responses.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1930031

</td><td>

The user doesn't get results from a Child table \(sn\_lg\_cnt\_repository\) of Parent \(ast\_contract\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1934684

</td><td>

getForTables on KG Global Graph isn't returning all the edges from contribution graphs

</td><td>

WDF tables that do not have a primary key when included in a knowledge graph schema causes query failures, even for queries that are only referencing to other glide tables present in that schema. The presence of this table can block all query execution within the graph.

</td><td>

1.  Create a contribution graph 'cont1' having sys\_user and cmn\_schedule nodes.
2.  Save the edge by using the script.

 Notice the error that occurred while getting cypher to result, 'com.snc.db.graph.GraphToGtopSerializationException: No element descriptor found for column on table u\_df\_wdf\_without\_pk: no thrown error.'

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1936199

</td><td>

Apostrophe in the cypher query causes an error

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1944376

</td><td>

Order tables in the view deterministically

</td><td>

Currently, when constructing the view to return from a cypher call, it creates the view from the set of the tables being requested based on enumerating the keyset. This has a non-deterministic order that depends on the underlying structure and the table prefixes. While that wouldn't be an issue at some layers, it means the ACL evaluation differs based on the ordering, which is hard for debugging and also hard to configure around. Instead, it should sort the order of the tables in the view alphabetically by the table name.

</td><td>

1.  Do a cypher query with more than one return node.
2.  Examine the view definition to see which table comes first.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1944805

 [KB2552260](https://hi.service-now.com/kb_view.do?sysparm_article=KB2552260)

</td><td>

getDisplayValue\(\) throws NullPointerException on many types of catalog variable

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1946286

</td><td>

Failing Workflow Data Fabric \(WDF\) queries when trying to execute on connection for trino\_primary

</td><td>

When trying to get specific column instead of the entire record, the error occurs in the response.

</td><td>

1.  Log in to the instance.
2.  Impersonate a user.
3.  Run the script.

 Notice the error which includes, 'FAILED TRYING TO EXECUTE ON CONNECTION trino\_primary'.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1938101

</td><td>

The 'Database' view for Workflow Data Fabric \(WDF\) incorrectly assumes the sys\_id when caching underlying glide records

</td><td>

add/getCache in the 'Database' view has a hardcoded assumption that there's a sys\_id element in the source and doesn't check for a null result. The copyValue code calls into GlideElement, which short circuits due to the WDF table being a foreign table. This needs to skip the cross scope check but still copy the value.

</td><td>

 

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

 PRB1843863

 [KB2061931](https://hi.service-now.com/kb_view.do?sysparm_article=KB2061931)

</td><td>

Shazzam Insights doesn't display any data in Discovery Admin Workspace

</td><td>

Shazzam Insights information isn't populated in the table 'Shazzam\_Insights' and an error appears in the system logs related to 'com.glide.util' usage.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1862106

 [KB2436326](https://hi.service-now.com/kb_view.do?sysparm_article=KB2436326)

</td><td>

Global IP exclusion isn't working for a cloud VM schedule

</td><td>

Not all the global exclusions are working for a cloud discovery.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1902780

</td><td>

The log pattern cloud errors only once

</td><td>

Currently, the cloud pattern errors are incorrectly being logged twice. It ends with two separate errors for the same pattern, one for the exception in the log and one for the 'Pattern Failed'.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1930200

 [KB2474013](https://hi.service-now.com/kb_view.do?sysparm_article=KB2474013)

</td><td>

Protected Tables Plugin will block DiscoverySensorJob logging, and cause warnings about syslog inserts from ProtectedTableAccessHandler instead

</td><td>

When the Protected Tables Plugin is active, which is recommended, the source= DiscoverySensorJob GlideRecord inserts made directly to the syslog table by Discovery's 'DiscoverySensorJob' script include are blocked, and flood the syslog table with logs from source=ProtectedTableAccessHandler instead.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1933785

</td><td>

A Cloud Discovery schedule incorrectly maps all related service accounts even when the 'Discover all Related accounts' toggle is unchecked

</td><td>

When creating a Cloud Discovery schedule for a project and un-checking the 'Discover all Related accounts listed below' toggle, the schedule still maps to all service accounts under that folder level. This behavior is intermittent and has been reproduced on multiple environments. The UI script logic doesn't correctly handle timing between setAllSubAccSelected and getSubAccountsOfMasterAccount. As a result, subAccountsList is reset incorrectly, leading to unintended account mappings.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1937992

</td><td>

Discovery Schedule doesn't support the discovery of more than 5000 IPv6 addresses

</td><td>

If the user creates a Discovery Schedule with over 5000 IPv6 addresses, the Discovery Status is instantly canceled and an error message appears.

</td><td>

1.  Create a Discovery Schedule with over 5000 \(X\) IPv6 addresses to disocvery\_range\_item\_ip.
2.  Select **Discover Now**.

 Observe that the Discovery Status is created and instantly canceled with the following error message under the Discovery logs related list: 'IP lists with IPv6 addresses can only contain 5,000 IPs but have X'.

</td></tr><tr><td>

Dynamic Translation for Agent Chat

 PRB1942231

</td><td>

The agent\_translated\_msg column is overwritten with empty value when the agent is in English and the chat requester is non-English

</td><td>

 

</td><td>

1.  Enable and configure Dynamic Translation for Agent Chat \(DTAC\).
2.  Log in to Service Operations Workspace as an English speaking agent.
3.  In another browser, log in as chat request in non-English language.
4.  Initiate an agent chat.
5.  Type an English phrase as an agent.

 Expected behavior: The agent\_translated\_msg on outbound message should be populated with English text.

 Actual behavior: The agent\_translated\_msg gets overwritten with empty values.

</td></tr><tr><td>

Event Management

 PRB1639714

</td><td>

Alerts on an Application Service have empty PRCs

</td><td>

Alerts on an Application Service appear in the list of 'Impacted Services/CIs' of some change requests. These alerts have empty PRCs and they have only one change request instead of two.

</td><td>

1.  Define the Manual Application Service.
2.  Define the Change Request for the Application Service.
3.  Send the event to some CI of the Application Service.
4.  Open the generated alert.
5.  Navigate to the PRC.
6.  Observe that the alert has the PRC 'Change on Application Service.'
7.  Send the event to the Application Service.
8.  Open the generated alert.
9.  Navigate to the PRC.
10. Observe that the alert has the PRC 'Change on Application Service.'
11. Create another change request on a different CI.
12. Add the defined Application Service to the list of Impacted CIs of the change request.
13. Send the event to the Application Service.
14. Open the generated alert.
15. Navigate to the PRC.

 Observe that the alert has only one change request, but it should have two.

</td></tr><tr><td>

Event Management

 PRB1934096

</td><td>

There's a regex preview mismatch in Enrich due to Java vs JavaScript engine differences

</td><td>

In the 'Enrich' page, the regex preview incorrectly shows no match even when the regex is valid and works correctly on actual events. This discrepancy, caused by differences between Java and JavaScript regex engines, has been observed by multiple users and leads to confusion when building enrichment rules.

</td><td>

 

</td></tr><tr><td>

File-based Discovery

 PRB1936524

</td><td>

File-based Discovery doesn't capture the content when the filename contains spaces

</td><td>

Discovery throws an below error in the Discovery logs for a filename that contains spaces: 'Error\(s\) during file based discovery: base64: extra operand '/usr/share/.../IOP' Try 'base64 --help' for more information'.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1925181

 [KB2407160](https://hi.service-now.com/kb_view.do?sysparm_article=KB2407160)

</td><td>

The Script API inForeground run a subflow that calls another subflow that has mid action step throws an exception before the outputs are ready with a message

</td><td>

The flow should complete and the outputs displayed in Scripts - Background. However, the flow executes, but an exception is thrown: 'The current execution is in the waiting state and the subflow outputs are not available'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1941990

</td><td>

Trigger inputs aren't accessible after a do-until loop execution

</td><td>

This issue is caused by the changes to GlideFlowStages Updater.java \(older name GlideStage UpdateListener.java\). It's observed that, in this specific flow structure, the 'in.request\_item' flow input isn't passed to the 'Create Catalog Task' action. Querying the sys\_flow\_value table, there are 2 entries for 'in.request\_item' one for the flow input and another with the parent loop associated. As the same key 'in.request\_item' is now associated with parent loops, it can only be accessed in the loop body \(and for the specific iteration\), and all other references to it out side the loop aren't available.

</td><td>

1.  Import the flow XML.
2.  Open Service Portal.
3.  Place a request for 'iPad Pro' with the color set to 'Silver'.
4.  Retrieve the RITM. Open Flow Designer.
5.  Test run the flow XML with the copied RITM as the input.
6.  Open the RITM when the flow waits at the AFA.
7.  Approve the request created for Abel Tuter.

 Expected behavior: The flow resumes, exits the loop, and reached the 'Create Catalog Task' and will be in the 'Waiting' state.

 Actual behavior: After exiting the loop, it is errored at 'Create Catalog Task' with an error executing the instruction.

</td></tr><tr><td>

Form Controller

 PRB1812174

</td><td>

The glide form saves the previous date

</td><td>

The report generates for the previous day.

</td><td>

 

</td></tr><tr><td>

GRC Platform Plugins

 PRB1941250

</td><td>

In Yokohama and Zurich, assessment reporting views aren't displayed

</td><td>

 

</td><td>

1.  Create and publish a RAM.
2.  Select the **View reporting** button.

 Observe that the reporting view is not displayed.

</td></tr><tr><td>

HR Service Delivery

 PRB1880661

</td><td>

The task\_sla records aren't visible to the user for the records created in the 'Employee relations' table

</td><td>

After upgrading to Yokohama, a script is added which fails for 'Employee Relations' table records.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1920738

 [KB2525534](https://hi.service-now.com/kb_view.do?sysparm_article=KB2525534)

</td><td>

HR Case description **\(rich\_description\)** doesn't copy over data, and the rich description is left empty

</td><td>

Rich Description appears as null in List View but displays correctly in the case record. The reverse works as expected when updating the **rich\_description** field in the HR case form, the value will appear in the **rich\_description** field in the list view.

</td><td>

1.  Log in to the instance.
2.  Create an HR case.
3.  Navigate to **sn\_hr\_core\_case.LIST**.
4.  Open the newly created case.
5.  Select the **Hamburger** icon.
6.  Configure the form layout.
7.  Add the **Description** field.
8.  Save the changes.
9.  Return to the HR case form.
10. Enter a message in the **Description** field, but don't enter anything in the **rich\_description** field.
11. Save the changes.
12. Observe that the same value is automatically updated in the **rich\_description** field due to a business rule that syncs values between the two fields.
13. Open the list view.
14. Add the Description and rich\_description columns.

 Notice that the **rich\_description** field doesn't contain a value.

</td></tr><tr><td>

HR Service Delivery

 PRB1943958

 [KB2570781](https://hi.service-now.com/kb_view.do?sysparm_article=KB2570781)

</td><td>

There's a 'You do not have permission to read the created record' error when creating an HR Case

</td><td>

A race condition in the UI happens when a form is submitted before the GUID is created and an empty sys\_is is passed. The server-side code was not handling this. It happens intermittently.

</td><td>

1.  Open **Create New** via Agent Workspace.
2.  Select the **Benefits Management** HR service.
3.  Select **Create case**.

 Notice the error, but the case gets created in backend with an empty case number.

</td></tr><tr><td>

Integration Hub

 PRB1931168

</td><td>

SSE step does not run on MID

</td><td>

 

</td><td>

1.  Create an action with an SSE step and check the run on the MID checkbox.
2.  Test the action.

 Notice the error 'SSE is only available on instance'. Individual chunks are not processed by the handler.

</td></tr><tr><td>

Investment Portal

 PRB1920188

</td><td>

Can't open or filter users/groups when there are a lot of records in the sys\_user table

</td><td>

In the Investment Portal, when the user opens 'Users/Groups' and add a new user, it takes about 30 seconds to load. Search doesn't work.

</td><td>

1.  Navigate to **Filter Navigator** &gt; **Investment Portal**.
2.  Open any of the bookmarked records.
3.  Select the **User** icon to open 'Users/Groups'.
4.  Select **Add users**.
5.  Wait for it to load, about 30 seconds.
6.  Try to add some letters in input.

 Observe that it doesn't work and doesn't search anything.

</td></tr><tr><td>

Language and Translations

 PRB1910767

</td><td>

The **question\_choice** field is displaying 'um' instead of 'A' for Brazilian Portuguese language

</td><td>

This issue was observed when upgrading to Xanadu.

</td><td>

1.  Navigate to a base Xanadu or Yokohama instance.
2.  Install the I18N Brazilian Portuguese Translations plugin.
3.  Navigate to **sys\_translated.LIST**.
4.  Filter the table as 'question\_choice' is value 'a'.

 Observe in Brazilian Portuguese language Label \(translate\) is displaying as 'um'.

</td></tr><tr><td>

Lifecycle Events

 PRB1926997

</td><td>

Lifecycle events \(LE\) aren't getting if the activity set isn't created in an LE scope, and the LE uses a flow to launch activity sets

</td><td>

This issue occurs when Lifecycle Event and its associated activity sets are configured within an HR scope other than Human Resources: Lifecycle Events. Additionally, the sn\_hr\_le.use\_flow property is set to true. When an HR case is submitted and fulfilled by a Lifecycle Event created outside the standard LE scope, the activity set fails to launch. The related subflow, HR Activity Launcher, ends with a status of 'Completed \(error caught\)'. The failure occurs in the first flow action, 'Look Up Record', which attempts to retrieve the sn\_hr\_le\_activity\_set defined in the Lifecycle Event. However, because no ACLs are defined for this table outside the scopes 'Human Resources: Lifecycle Events' or 'Human Resources: Lifecycle Enterprise', the lookup fails with an error.

</td><td>

1.  Create a Lifecycle Event and its activity sets in a non-LE scope. For example,'Human Resources: Employee Relations'.
2.  Create an HR Service in sn\_hr\_er\_case Centers of Excellence \(COE\).
3.  Set the fulfillment type to 'Lifecycle Event'.
4.  Use the Lifecycle Event created in step 1.
5.  Complete the other HR Service setup.
6.  Submit a new HR case from the new HR Service.
7.  Notice there are no Activity Sets attached.
8.  Open the Flow Designer.
9.  Check the operations of the 'HR Activity Launcher' subflow related to the test.

 Notice that the error 'Look Up Record action, 'The requested flow operation was prohibited by security rules'' occurs in the first step.

</td></tr><tr><td>

Lifecycle Events

 PRB1945674

</td><td>

Improve logging and validation in glidefix\_deprecate\_le\_workflow for when the 'sn\_hr\_le.use\_flow' property fails to update

</td><td>

The logs for the fix script doesn't re-validate the property.

</td><td>

1.  Install the following on a WDC instance:
    -   HR Core
    -   HR Lifecycle Event \(HR LE\)
    -   HR Lifecycle Event for enterprise \(HR LE Ent\)
2.  Upgrade the instance to Yokohama.
3.  Examine the logs for the glidefix\_deprecate\_le\_workflow fix script.

 Notice that it doesn't re-validate that the property was successfully updated.

</td></tr><tr><td>

List Administration

 PRB1847244

</td><td>

Fixed filters in the Condition Builder \(CB\) aren't displayed after refreshing the page with the updated URL

</td><td>

After refreshing the page with the updated URL, the fixed filters don't appear in the CB.

</td><td>

1.  Log into any Yokohama instance.
2.  Navigate to **Service Operations Workspace \(SOW\)**.
3.  Open a page with a predefined filter.
4.  Select **Incidents** &gt; **Open**.
5.  Open the Condition Builder \(CB\).
6.  Notice that the CB should appear with the fixed filter as expected.
7.  Copy the URL up until the listID.
8.  Append the URL to the end of the instance's address bar.
9.  Select **Enter** to refresh the page.
10. Open the CB again.
11. Check the filter conditions.

 Expected behavior: The fixed filters should be visible in the Condition Builder.

 Actual behavior: The fixed filters don' appear in the Condition Builder.

</td></tr><tr><td>

List Administration

 PRB1932703

 [KB2543882](https://hi.service-now.com/kb_view.do?sysparm_article=KB2543882)

</td><td>

Display values aren't showing for reference fields within the 'List' component

</td><td>

When including a table on the 'List' component that contains reference fields, it's showing empty. Where as in platform, it shows a value.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1944139

</td><td>

Uptake allowExtended fields property on the lists side for the sn-field-select component

</td><td>

Tracking the changes for PRB1935534.

</td><td>

1.  Create a system property 'glide.ui.list.allow\_extended\_fields'.
2.  Set it to 'true'.
3.  Create a UI Builder page with a list component configured.
4.  Set the table property 'task'.
5.  Open the runtime page.
6.  Select the **Personalize columns** button in the header.

 Expected behavior: The fields from all tables extending from the task are displayed.

 Actual behavior: Only fields from the task table are displayed.

</td></tr><tr><td>

List Controller

 PRB1937947

</td><td>

Additional logging for Splunk to build more context around legitimate use cases

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Views

 PRB1886477

</td><td>

Selecting a 'Presentational' list component in a UI Builder \(UIB\) panel causes some issues

</td><td>

This issue was observed in Xanadu.

</td><td>

1.  Log in to any instance.
2.  Navigate to the UIB page.
3.  Create an experience with the List Page template.
4.  Select **Save**.
5.  Open in runtime.
6.  Notice that the **Select** checkboxes are shown as expected.
7.  Select **Presentational list component** on the UIB page configured.

 Notice that the **Select** checkbox disappears and the **Save** button is enabled, even when there have been no changes. When selecting **Save** and **Open the page**, the **Select** checkbox aren't present.

</td></tr><tr><td>

Memory: Heap Space

 PRB1636231

</td><td>

Memory exhausted by the Archiver Job Consumer due to syslog records stored in memory, and syslog\_awa is not configured as a rotated table

</td><td>

Memory exhausted by the Archiver Job Consumer reparenting records from syslog table due to a problem observed when syslog\_awa, which is a child table of syslog, is created without table rotation. The archiver job reparents records for the archive rules it triggers for, and will reparent a table that's not rotated. When syslog\_awa isn't configured as a rotated table, the reparenting process will execute on it and its parent table syslog. Query to syslog shards are then observed, and memory is consumed as the records on these shards are stored into memory. Due to the size of it, it will cause memory to become depleted. When the archiver job is running, the localhost logs will have a large query to a syslog shard where the function reparentDocumentIDRecords is running.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1923497

</td><td>

Deadlock occurred due to two threads

</td><td>

The issue is caused by a conflict between two internal processes that manage and refresh OAuth credentials and MID Server connections. The platform periodically checks and refreshes expired OAuth tokens using a scheduled job. When this happens, the system reloads the credentials and resets all related connection data to ensure security and consistency. At the same time, if a Discovery probe or integration is trying to establish a new connection, it might attempt to access the same shared connection resources. This overlap can lead to both processes waiting for each other to finish, resulting in a temporary deadlock where neither process can proceed.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1951413

</td><td>

Search cards based on external content can't be configured on fields created on the external content table

</td><td>

Creating a search card based on an external connector based table allows only certain fields to be visible. After the configuration of the mobile search card, find that the created field for mobile\_url can't be used in the card for navigation.

</td><td>

1.  Navigate to the instance.
2.  Impersonate a user.
3.  Navigate to the portal.
4.  In the global search, search for the keyword 'lays'.
5.  Notice that the results are displayed.
6.  Navigate to the 'News' tab to view the results.
7.  Open the Now mobile app.
8.  Log into the mobile app.
9.  Impersonate Abel Tuter in Now mobile.
10. Search for 'lays' in global search.

 Notice that no results are seen under the 'News' tab.

</td></tr><tr><td>

Now Assist Panel

 PRB1867538

</td><td>

Copy for synthesized responses \(auto start\) on Now Assist panel \(NAP\) doesn't work and copies 'undefined'

</td><td>

When using the Now Assist panel \(NAP\) and entering 'Summarize a record', the **Copy icon** on the auto-started synthesized response does not copy the content, and instead, 'undefined' is copied. When 'Undefined' is copied instead of the content and the synthesized response is not auto-started, there is no **Copy icon** and a **Like/dislike** button is shown instead.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1938963

</td><td>

Text is cut off in Now Assist panel \(NAP\) in the text area in Spanish

</td><td>

 

</td><td>

1.  Impersonate a user.
2.  Set the language as Spanish.
3.  Select the **NAP** icon.

 Notice that the message in the text area is cut off.

</td></tr><tr><td>

Now Assist Panel

 PRB1941558

</td><td>

Now Assist panel \(NAP\) Assistant Information sources changes aren't saved in the guided setup

</td><td>

The NAP assistant default schema is set to 'None'.

</td><td>

1.  Navigate to **Conversational interface** &gt; **Assistants** &gt; **NAP assistant** &gt; **Information Sources**.
2.  Change the KG schema to an NLQ user graph.
3.  Select **Save and continue**.
4.  Return back to the tab to ensure the changes are saved.

 Expected behavior: The changes made in Information Sources saved.

 Actual behavior: The KG schema returns to 'None'.

</td></tr><tr><td>

Now Assist Panel

 PRB1942697

</td><td>

The Now Assist Panel \(NAP\)/NASS window can't be found after closing and not pinning it

</td><td>

On the header, the NAP icon should be visible, but there's no option for opening it.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1938158

</td><td>

Providers are restored to the default when plugins are repaired or when a new version is updated

</td><td>

After updating the provider to another, it gets set to the default again.

</td><td>

1.  Log in to the instance as an admin.
2.  Navigate to **Now Assist admin** &gt; **Settings** &gt; **Manage Model Providers**.
3.  Select **Edit Model Provider** &gt; **Customize** &gt; **Edit provider for skill**.
4.  Select a skill such as 'Incident summarization'.
5.  Update the provider to any other provider, such as Google or Amazon, except for the default one.
6.  Verify that the provider has been updated for the record summarization to Google in sys\_one\_extend\_capability.
7.  Repair the UXC plugin or install the latest version.

 Notice that the provider is set to the default again.

</td></tr><tr><td>

OneExtend

 PRB1938406

</td><td>

QnA Planner2 call failing with the path /v2/models/ llm\_generic\_large\_v2/infer

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1938474

</td><td>

Entitlement\_active isn't activated in the sys\_geo\_routing table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1938540

</td><td>

Strange JSON format sources displayed in Now Assist Virtual Agent \(NAVA\) chatbot for certain queries

</td><td>

Issue is intermittent.

</td><td>

1.  Navigate to**/sp**.
2.  Enter the utterance **Create incident** in the NAVA chatbot.

 Observe the Planner 2 response displayed but with unexpected JSON style sources output at the bottom.

</td></tr><tr><td>

OneExtend

 PRB1939640

</td><td>

Incident summarization doesn't work if the user enables Guardian in znowassiststable

</td><td>

 

</td><td>

1.  Enable offensiveness, block and log.
2.  Enable Prompt Inject Block and log.
3.  Navigate to any incident and update the short description as 'Lets kill all.'
4.  Select the **Summarize** button.
5.  Verify that it should get blocked with the error code in generative AI log table.

 Observe that summarizing the record in the incident is stuck and works fine if disabled.

</td></tr><tr><td>

OneExtend

 PRB1940891

</td><td>

The **Prompt** field in the 'Generative AI Log' table has extra escaped characters when using Java subflow implementation

</td><td>

In Java, a **Prompt** is converted to a string even though it's already a string before inserting it into the Generative AI Log table. There's extra escaped characters in the **Prompt** field.

</td><td>

1.  Run a capability.
2.  Navigate to the sys\_generative\_ai\_log table.
3.  Check the **Prompt** fields.

 Expected behavior: Users shouldn't see extra escaped characters in the prompt.

 Actual behavior: Valid escaped sequences are escaped unnecessarily.

</td></tr><tr><td>

OneExtend

 PRB1941124

</td><td>

Claude and streaming yields significantly malformed the output

</td><td>

When the user enters the query in French for the first time, the streamed output has words stuck together. For example, 'basede' should be 'base de' and 'vousavez' should be 'vous avez'. When the user runs the query again, the issue doesn't persist.

</td><td>

1.  Ensure the instance has Claude, has streaming on, and has Dynamic Translation off.
2.  Navigate to **/sp**.
3.  Open the Now Assist Virtual Agent \(NAVA\) chatbot.
4.  Enter the utterance, **Quelles sont les options pour créer une base de connaissances?**.
5.  Observe that the streamed output has several words mashed together.
6.  Observe that in the sys\_generative\_ai\_log planner 2 output, the response from LLM itself is this way
7.  Disable streaming.
8.  Repeat the query.

 Notice that there is no issue with the words being stuck together in the output.

</td></tr><tr><td>

OneExtend

 PRB1942490

</td><td>

KB generation isn't working when requested from Now Assist panel \(NAP\)

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Activate all FSM skills.
3.  Ensure the credentials for Now LLM are updated with proxy.
4.  Navigate to **NAP**.
5.  Select **Generate KB Article**.

 Expected behavior: KB generation happens successfully.

 Actual behavior: Notice the error message, 'Sorry, there was a problem on my side trying to complete this request. Try asking again later' and that there's an error in the sys\_generative\_ai\_log.

</td></tr><tr><td>

OneExtend

 PRB1942618

</td><td>

Script include-based capabilities aren't executed as a subflow though the required sys property is enabled

</td><td>

 

</td><td>

1.  Create a Gen AI capability with it's definition pointing to script include.
2.  Ensure the sys prop 'com.glide.oneapi.run\_ script\_include\_on\_fdih \_engine' is set to 'True'.
3.  Ensure flow debugging is turned on for the subflow.
4.  Run the script include as a FDIH subflow.
5.  Execute the capability from 1 using OneExtendUtil.execute API.

 Expected behavior: The script include is executed as a subflow and subflow executions should execute.

 Actual behavior: The subflow 'Run script include as FDIH subflow' won't show any executions.

</td></tr><tr><td>

OneExtend

 PRB1944861

 [KB2566151](https://hi.service-now.com/kb_view.do?sysparm_article=KB2566151)

</td><td>

Assists Consumption for Custom Skills created in Now Assist Skill Kit

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Filters

 PRB1832303

</td><td>

The option to select a one-day range on the calendar grid is blocked for the NextGen Dashboard

</td><td>

There is no option to select a one-day range on the calendar grid. The grid allows a minimum range of two days. However, if the user manually enters the end date, the filter applies without any restrictions.

</td><td>

1.  Log in to the UXA dashboard.
2.  Select a custom range.
3.  Select **November 29** as the start date.
4.  Attempt to select **November 29** as the end date.

 Expected behavior: A one-day range is available to the user when using the calendar grid and when entering it manually.

 Actual behavior: A one-day range selection is blocked on the calendar grid, but the user can manually enter **November 29** as the end date and the **Apply** button becomes active so the user can apply a one-day range to the filter.

</td></tr><tr><td>

Playbook Experience Core

 PRB1929896

</td><td>

The playbook lane isn't translated to Italian

</td><td>

This is an issue with record generator. It can also be reproduced by going to 'Playbook Preview' and selecting the record generator for the record.

</td><td>

1.  Log in to any instance.
2.  Switch the language to Italian from the menu preference.
3.  Open **Workspaces** &gt; **Risk workspace**.
4.  Select the **List** icon.
5.  Select **Risk assessment planning** &gt; **Scheduled assessment**.
6.  Select **New**.
7.  Observe that the playbook lane is still coming in the English language.

 Expected behavior: The playbook lane should be translated to Italian.

 Actual behavior: The playbook lane isn't translated to Italian.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1934746

 [KB2592048](https://hi.service-now.com/kb_view.do?sysparm_article=KB2592048)

</td><td>

Playbooks archived in Xanadu don't work in newer releases

</td><td>

New fields that get added to the deserializer need to handle the keys not existing, which, as of now, is snapshot\_id and variant\_id.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Predictive Intelligence

 PRB1936441

</td><td>

Prediction fails when a new advanced parameter is used during training

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1905989

</td><td>

The **Create Expenseline** button from the new **Costplan split** button doesn't create a system generated costplan

</td><td>

The widget is updated, but no new system generated costplan is created.

</td><td>

1.  Create any planning item.
2.  Add a costplan intially.
3.  Select **New Expenseline** on the**Costplan split** button.
4.  Add the details but don't associate it with any costplan.
5.  Save the expenseline side panel.

 Notice that the actuals widget is updated, but no new system generated costplan is created.

</td></tr><tr><td>

Project Management

 PRB1918462

 [KB2532380](https://hi.service-now.com/kb_view.do?sysparm_article=KB2532380)

</td><td>

The system throws an error and a Resource Allocation record is not created upon creation of a Resource Assignment record on a Project Task

</td><td>

The user observes an error while generating a resource allocation record during the creation of a resource assignment record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Reporting

 PRB1892170

</td><td>

A table isn't able to select from the sys\_report\_source form

</td><td>

The table doesn't show in the list.

</td><td>

 

</td></tr><tr><td>

Security Customer Actions

 PRB1922115

 [KB2414937](https://hi.service-now.com/kb_view.do?sysparm_article=KB2414937)

</td><td>

A completed user action with a canceled playbook is set to 'open' after upgrading

</td><td>

The user action is reset to 'Open' and the latest playbook snapshot is canceled. The action should remain in a 'Complete' state when there's no active playbook snapshot to work on.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Seismic Framework

 PRB1836265

</td><td>

Seismic P2 Scheduler remains in an infinite loop

</td><td>

Performance issues on the 'Schedule' page. When switching from daily to weekly to monthly, it takes more time. After creating the schedule, sometimes the user can't see the created schedule before publishing the plan.

</td><td>

1.  Navigate to **Workspaces** &gt; **Workplace Central**.
2.  Select the **Preventive Maintenance** icon on the side bar.
3.  Navigate to **All Plans**.
4.  Select **New**.
5.  Select the start date and future end date.
6.  Select any building.
7.  Select **Next**.
8.  Select one or more maintenance items.
9.  Select **Next**.
10. Select **Create schedule.**

 Observe it will take more time to open the 'Schedule page' and sometimes it doesn't open.

</td></tr><tr><td>

Seismic Framework

 PRB1919027

</td><td>

Document requests end up using outstanding child prefetch promise

</td><td>

In certain scenarios, the Service Worker incorrectly fulfills a main page request using a pending iframe request. This occurs when the Service Worker matches the main page request to an existing pending iframe request, resulting in the main page loading the iframe's content instead of its own. This leads to incorrect rendering and potential functional issues on the main page.

</td><td>

1.  Open any UI16 page on a Next Experience enabled instance.
2.  Wait for the page to load.
3.  Reload the same page several times \(5+\).

 Expected behavior: The navigation bar and shell to show up with UI16 content all the time.

 Actual behavior: Only UI16 content is shown on the page. The navigation bar and shell are missing.

</td></tr><tr><td>

Service Catalog

 PRB1831404

</td><td>

Multiple dynamic behavior records are generated for a regenerate action

</td><td>

The ability for dynamic behavior enables the creation of AI-generated properties for questions. The design should include a clear indication when these properties are generated by AI.

</td><td>

 

</td></tr><tr><td>

ServiceNow Studio \(Legacy\)

 PRB1831690

</td><td>

Progress keeps displaying 'In progress' while publishing the app

</td><td>

The 'In progress' state at 0% progress keeps showing when publishing the app, when the actual progress should be displayed. Once the app has finished publishing, the 'In progress' state should close out. This issue occurs on a Yokohama instance with MFA enabled and connected to pipeline.

</td><td>

1.  Log in as an admin user.
2.  Navigate to **Legacy Service Studio**.
3.  Create an app.
4.  Publish the app.

 Expected behavior: Progress should display the progress and close once the deployment is finished.

 Actual behavior: It keeps showing 'In progress' with 0% progress.

</td></tr><tr><td>

Service Portal

 PRB1839297

 [KB1925168](https://hi.service-now.com/kb_view.do?sysparm_article=KB1925168)

</td><td>

A SPEntry page error 'Execute operation on script include 'SPEntryPage'' from scope occurs

</td><td>

Switching the scope and refreshing the page gives the error, 'Execute operation on script include 'SPEntryPage' from scope 'Knowledge Management - Service Portal' was denied'.

</td><td>

1.  Log in to a Xanadu instance.
2.  Create the glide.entry.first.page.script system property.
3.  Give it the value: new SPEntryPage\(\).getFirstPageURL\(\).
4.  Make'Knowledge Management - Service Portal' as the current scope.
5.  Refresh the browser page.
6.  Notice the error, 'Execute operation on script include 'SPEntryPage' from scope'Knowledge Management - Service Portal' was denied. The application ' Knowledge Management - Service Portal' must declare a cross scope access privilege. Please contact the application author to update their privilege requests.'
7.  Repeat step 2 and step 3 with the scopes 'CI Landing Experience' and 'Conversational Interfaces - Diagnostics'.

 Notice that the same error message occurs.

</td></tr><tr><td>

Service Portal

 PRB1935238

</td><td>

Portal page shifts occasionally when 'Ask a follow-up' is selected

</td><td>

 

</td><td>

1.  Ensure Agentic AI is set up on the instance.
2.  Enable Dispatcher Workspace \(DW\) on portal.
3.  Search for 'Loaner Laptop'.
4.  Wait for the response to load.
5.  Select the **Loaner laptop** citation.
6.  Select **Request in chat**.
7.  Wait for the chat to open.

 Notice that the Portal page shifts occasionally.

</td></tr><tr><td>

Software Asset Management

 PRB1771094

</td><td>

A default value isn't set for some of the content tables

</td><td>

The default value isn't set in the dictionary for some content tables, causing it not to push the content data from stage columns to actual columns if the 'SAM - Apply latest content' job isn't run.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Workspace \(Glide\)

 PRB1939252

</td><td>

Backport UI changes for Software Assest Management \(SAM\) AI agent

</td><td>

Multiple UI fixes from Zurich to Yokohama. This includes message displays, navigation, and changes to the activity center.

</td><td>

 

</td></tr><tr><td>

Software Discovery

 PRB1579663

</td><td>

File-based discovery populates the version only on the first software install record for a DM

</td><td>

 

</td><td>

Run file based discovery.

 Notice the software install record \(cmdb\_sam\_sw\_install\) only has **Publisher** and **Product** \(display names\) populated. It would be good to also populate version with the normalized version if available. Some users have use cases that require a version on the install records.

</td></tr><tr><td>

Standard Change Catalog

 PRB1850616

</td><td>

On Service Operations Workspace \(SOW\), change request template values aren't auto-populated when they are modified or retired

</td><td>

This issue also occurs when 'Retire an existing template' is selected.

</td><td>

1.  Open any instance with SOW.
2.  Open SOW.
3.  Select **Create new change request**.
4.  Select **Propose a new template**on the right top corner.
5.  Change the field **Proposal type** to **Modify an existing template**.
6.  Fill any template to modify/retire.

 Notice that the change request values will be still empty.

</td></tr><tr><td>

Telemetry Glide Infrastructure

 PRB1920545

</td><td>

CDC replication disables batch DB update operations on replicated tables causing increased upgrade time on instances

</td><td>

 

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

UI Field Administration

 PRB1833290

</td><td>

Performance issues with **List** field type referencing an attachment table in Workspace

</td><td>

A **List** type field that is based on the sys\_attachment table shows selected attachments that have already been attached to the parent record, but there is a difference in behavior between the backend and Workspace when adding records to the field. This results in a performance issue in Workspace that is dependent on the number of records present in the sys\_attachment table, which is not seen in the backend.

</td><td>

1.  Open a Xanadu base instance.
2.  Add the **List** type field on incident.for for default view and workspace.
3.  Configure it so that it displays only attachments associated with the parent record.
4.  Enable 'Detailed SQL debugging'.
5.  View an active Incident record in the backend.
6.  Associate some attachments to it.
7.  Select an attachment in the new **List** field.
8.  Review the generated SQL
9.  Observe the query for the sys\_attachment record.
10. Repeat step 5 through step 9 using CSM/FSM Configurable Workspace.

 Expected behavior: The user sees the query for the sys\_attachment record.

 Actual behavior: The same querying approach for the sys\_attachment record is seen, there's an additional query on sys\_attachment on the **File name** field using the record's SysId as the value. This results in a whole table scan that returns no records.

</td></tr><tr><td>

UI Field Administration

 PRB1877769

 [KB2182152](https://hi.service-now.com/kb_view.do?sysparm_article=KB2182152)

</td><td>

The **info \(i\)** icon for reference catalog variables is missing on requested items and the 'SCTASK' form under Service Operations Workspace

</td><td>

The issue is seen with all the workspaces since Yokohama.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Field Administration

 PRB1942077

</td><td>

The **field\_list** field type in workspaces should support extending child table columns

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1847354

</td><td>

There's no facility for setting the default encryption of attachments to 'None' in the configurable workspace

</td><td>

With CLE attachment encryption enabled, if a user adds an attachment, there isn't a way to configure the UI to use 'None' as the default. If the user has access to an encryption module, it will always be the default option in the workspace UI. It's possible to customize the platform UI for this, but the workspace doesn't have this adaptability.

</td><td>

1.  Install CLE Enterprise.
2.  Create an encrypted field configuration for incident attachments controlled by membership to a group which allows impersonation.
3.  Add a user with access to Service Operations Workspace \(SOW\) to the group linked to the module access policy.
4.  Impersonate that user.
5.  Open an incident in the workspace.
6.  Add an attachment.

 Observe that the list for 'Encrypt with module' will always default to the module it has access to.

</td></tr><tr><td>

UI Form Administration

 PRB1870603

</td><td>

A read-only HTML field displays a horizontal and vertical scroll

</td><td>

The field shouldn't have a scroll bar.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB1933942

</td><td>

Skipped error after upgrading

</td><td>

The user gets a skipped error after upgrading the instance from Xanadu to Yokohama. The reason is 'Skipping unavailable system property glide.db.df\_engine.enabled. Customers cannot configure this property.' It's included in the plugin 'com.snc.db.df\_engine'.

</td><td>

 

</td></tr><tr><td>

UXF Components

 PRB1919730

 [KB2505771](https://hi.service-now.com/kb_view.do?sysparm_article=KB2505771)

</td><td>

UXF page components aren't loading properly post-upgrade due to a page fragment not updating during the upgrade

</td><td>

When users upgrade minor patches, if there are no changes to the metadata related to macroponents, page fragment caches won't be flushed. During the upgrade process, if any user accesses pages that have asset bundles, a problem occurs. During the upgrade, asset bundling is turned off, so the macroponent page fragment doesn't have assetsInBundle, but once the upgrade is completed, asset bundling will be turned on. However, the backend is serving the old page fragment without the asset bundle context, and the macroponent asset bundle is not loaded, so components in the page won't load.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1892094

</td><td>

An **ATF test** UI action fails due to a timeout error

</td><td>

The intent library delivers context on generator registration for translators that don't exist on the page.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1918913

</td><td>

The js\_atf\_instrumentation.js script is missing when asset bundling is turned on

</td><td>

js\_atf\_instrumentation.js script, which instruments pages for component load detection and rollback during Automated Test Framework \(ATF\) testing, is missing when asset bundling is turned on.

</td><td>

1.  Navigate to **Menu** &gt; **Automated Test Framework** &gt; **Tests**.
2.  Select **Create your own new test** &gt; **Give a name** &gt; **Save**.
3.  Add a test step to open a form in the workspace **sc\_task** &gt; **Form** &gt; **Open a new form**.
4.  Choose **Form UI** &gt; **SOW workspace**.
5.  Choose **Table** &gt; **sc\_task** &gt; **Save the test step**.
6.  Add **Test step** &gt; **Form** &gt; **UI action visibility**.
7.  Choose **Visible close task** &gt; **Save the test step**.
8.  Navigate to the test page where it lists the 2 steps.
9.  Right click on the display name of the UI action visibility display name and select **Add breakpoint**.
10. Select **Debug Test**.
11. Notice that this opens the test runner in a new window.
12. Wait for the test to stop at the break point and inspect the DOM to notice the script tag for js\_atf\_instrumentation.js is missing.
13. Turn off asset bundling using glide property glide.uxf.lib.asset\_bundle\_enabled.

 Notice js\_atf\_instrumentation.js is available.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1928396

</td><td>

Date time input when used in a topic block returns null on output parameters

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Create a topic block \(nlu/keywords\) with data time input.
3.  Add date time input to the output parameters.
4.  Run the topic block and the data time returned in the output parameters in \{\}.

</td></tr><tr><td>

Virtual Agent

 PRB1911010

</td><td>

With DTAC enabled and an agent name showing in the Virtual Agent Header, VA uses an incorrect name

</td><td>

From the end-user perspective, an Agent's full name is displayed.

</td><td>

1.  Modify the 'Name' column for an Agent \(for example, Abel Tuter\) in the live\_profile table.
2.  Verify that the Live Profile name is changed to something like 'abel@example'.
3.  With the Agent user, navigate to CSM/FSM or SOW.
4.  Make the agent 'Available for chat' with the agent's language set to English.
5.  Connect with another user in another window with the language preference set to a language other than English.
6.  Navigate to /sp.
7.  Open Virtual Agent.
8.  Start a Live Agent conversation.
9.  Check the title on the chat window.
10. Accept the chat as the agent.

 Observe the chat title is changed from 'Abel@example' to 'ABEL TUTER'.

</td></tr><tr><td>

Virtual Agent

 PRB1915544

</td><td>

The Virtual Agent \(VA\) topic execution returns a tool response instead of a main skill

</td><td>

The VA topic execution should return a main skill response or provide a way for the user to configure the topic to return a main skill response. Instead, the VA topic execution returns RAG response.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1936820

</td><td>

Lock exceptions are noticed for Now Assist Portal \(NAP\) and Now Assist Virtual Agent \(NAVA\)

</td><td>

 

</td><td>

1.  Set up the latest ynowassiststable instance for NAP/NAVA.
2.  Execute load tests for any use case of Virtual Agent.

 Notice the exceptions are logged in the log.

</td></tr><tr><td>

Virtual Agent

 PRB1937290

</td><td>

The **New conversation** button disappears when using certain custom branding colors

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1937589

</td><td>

Abnormal Generative AI Controller \(GAIC\) Async submission duration

</td><td>

SkillDetailsCache is reclaimed and cache building can be as high as 3.5s.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1938022

</td><td>

AI Agent \(AIA\) Unified Planner 1 is taking up to 1.5 to 2 seconds in the Gen AI log with a single user.

</td><td>

The Hybrid queue take up to 500 ms.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1938273

</td><td>

Multi-intent utterances are not working in Now Assist panel \(NAP\)

</td><td>

This issue was observed when using Azure and Gemini. Workflows are available for example both utterances, and individually both utterances are work as expected.

</td><td>

Enter the utterance 'Book a flight and order coffee.'

 Notice that the first workflow completed for both Azure and Gemini, but general react responses occur instead of triggering the next flow in Azure, and a message occurs that the workflow can't proceed in Gemini.

</td></tr><tr><td>

Virtual Agent

 PRB1938620

</td><td>

The **Go to search results** button isn't visible in Dynamic Window \(DW\)

</td><td>

The **Go to search results** button isn't visible for chat-to-search transition. It should be visible, as this functionality worked in the previous release.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1938658

</td><td>

Second intent is not going to planner 1 in continuous conversations

</td><td>

 

</td><td>

1.  Navigate to the**/esc** portal.
2.  Open Virtual Agent \(VA\).
3.  Enter utterance which can match multiple agents.
4.  Instead of selecting an agent, enter the next utterance that can give fallback options such as 'What is ServiceNow stock price'.
5.  Select **Web search** in the fallback option.

 Observe that web search gives an answer for incident resolution, and not for ServiceNow stock price.

</td></tr><tr><td>

Virtual Agent

 PRB1941025

</td><td>

Conversation doesn't end after catalog execution completes on standard chat

</td><td>

 

</td><td>

1.  Execute the Miro access catalog item in standard chat.
2.  Finish the flow.

 Expected behavior:The conversation ends after the execution completes.

 Actual behavior: The conversation doesn't ended.

</td></tr><tr><td>

Virtual Agent

 PRB1941206

</td><td>

Cloned metrics aren't appearing in the list after creation

</td><td>

The metric appears to be created successfully, but the cloned metric doesn't appear up in the list in the home page.

</td><td>

1.  Create a custom metric.
2.  Open the created custom metric.
3.  Select **Copy** on the top right corner to clone the metric.
4.  Select **Finish setup**.
5.  Navigate to the home page.

 Observe that the metric is not available.

</td></tr><tr><td>

Virtual Agent

 PRB1941593

</td><td>

Using vaSystem.executeSkillWithResumeBehavior in a topic causes resume conversation to fail

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1941618

</td><td>

The same workflow is displayed twice in Now Assist panel \(NAP\)

</td><td>

There is only one workflow with the 'Order items' name.

</td><td>

Enter the utterance, 'I want to order below list of items: Coffee, Laptop, Book a flight, Pizza.'

 Notice that the coffee agent is completed and the same workflow is displayed twice as the following, 'To place your laptop request, use either of the available ordering workflows: it Order items – order a laptop for you and Order items – order a laptop for you.'

</td></tr><tr><td>

Virtual Agent

 PRB1942159

</td><td>

Conversations that already have diverted to Live Agent are timing out

</td><td>

 

</td><td>

1.  Start a NAVA chat with a search phrase.
2.  While waiting for the result, select the **Contact Live Agent** \(Contextual Action\) button.
3.  Conduct a live agent chat.
4.  Within 30-60 seconds, the conversation times out.

</td></tr><tr><td>

Virtual Agent

 PRB1943087

</td><td>

AI Search for semantic filters shouldn't be executed if no filters are returned

</td><td>

With semantic filters enabled, no filters are configured for the assistant. AI Search is getting executed for semantic filters.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1943466

</td><td>

Now Assist Skill executing twice when running in sync mode

</td><td>

The main skill should execute only once. The main skill is executing twice. Please check the GenAI log and find two execution records.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1943976

</td><td>

Need to add expensive caches as hard reference caches to avoid GC

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1947698

</td><td>

Only one agentic workflow executes successfully when the same trigger fires simultaneously

</td><td>

When a workflow trigger fires simultaneously multiple times, only one of the resulting agentic workflows executes successfully. The other workflows terminate immediately with an error indicating that no session ID could be found. Each trigger correctly creates a new execution plan and a new conversation record, but only one conversation proceeds, while the others fail at the start.

</td><td>

1.  Create the agentic workflow named 'Test multiple case executions'.
2.  Select three or more case records and update them simultaneously so that the trigger fires for all at once.
3.  Notice that the three execution plans \(sn\_aia\_execution\_plan\) and three conversation records are created. Only one conversation and execution plan executes successfully. The other conversations don't continue after the first task with the error ''No session ID found'.

 Expected behavior: Each triggered workflow should independently create or resolve its own valid session so that all conversations execute successfully, even under concurrent trigger conditions.

 Actual behavior: Only one conversation executes successfully. The other conversations either terminate immediately or don't continue after the first task with 'No session ID found' error.

</td></tr><tr><td>

Virtual Agent

 PRB1948321

</td><td>

The send history is not returning the sequence field for the Virtual Agent \(VA\) API

</td><td>

The script should return the sequence field in response.

</td><td>

1.  Send history messages using the VA API.
2.  Start the conversation.
3.  Retrieve the history messages using the script.

 Observe that the sequence field isn't returned.

</td></tr><tr><td>

Virtual Agent

 PRB1948603

</td><td>

The DateTimePicker component breaks for the Japanese language

</td><td>

 

</td><td>

1.  Change language to Japanese.
2.  Open an instance.
3.  Open the /esc portal.
4.  Select the date time picker demo topic.

 Notice that the time fields are showing 00:00.

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1941102

</td><td>

Typing a response before a previous response has completed can lead to a 'technical error' in the conversation

</td><td>

 

</td><td>

 

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
4.  Create a catalog item with one'Data/Time' type variable.
5.  Navigate to **AI Search Index** &gt; **Indexed Sources**.
6.  Open 'Catalog Item Table'.
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

 PRB1936255

</td><td>

Turn off audio notifications by default in Now Assist Portal and Virtual Agent

</td><td>

As processing execution occurs, there's continuous beeps. The audio should be turned off by default.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1937016

</td><td>

Fixing VX spacing issues

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1937432

</td><td>

Fixing VX spacing issues

</td><td>

Issues with spacing observed Assist Virtual Agent \(NAVA\) and Dispatcher Workspace \(DW\). In issue 1, there's an extra space under 'Generating a response' for NAVA while it seems to be fixed for DW. In issue 2, spacing between the processing message container and the Sparkle icon should be 24px but it's 12px in NAVA and 24px in DW. In issue 3, processing step spacing should be 8px at the top and bottom in both NAVA and DW.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1940018

</td><td>

Spacing not matching Figma for Conversational UX enhancements

</td><td>

Spacing issues in Now Assist Virtual Agent \(NAVA\), Dispatcher Workspace \(DW\), and Now Assist panel \(NAP\).

</td><td>

1.  Enter **Hello**.
2.  Notice that the space between 'Hello' and the sparkle icon should be 12px, and is currently 24px in both NAVA, DW and NAP.
3.  Notice the space between 'Let me look up for information'.
4.  Hover the **Copy** icon to next **Sparkle** icon.
5.  Notice that it should be 12px, has a 4px margin in DW and NAP.
6.  Select **Show Sources**.

 Notice that the space between the Synthesized results and the links should be 8px, and that it's 4px in DW and NAP.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1940975

</td><td>

Support more markdown for text messages and synthesized responses

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1941763

</td><td>

The **New chat** button is turned off after a flow execution is complete

</td><td>

 

</td><td>

1.  Call one of the HR flows that results in successful case creation which is the end of the flow.
2.  Try to start a new conversation.

 The **New chat** \(plus button\) is turned off.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1941773

</td><td>

Portal page shifts occasionally when **Ask a follow-up** is selected

</td><td>

The portal page shifts to the left then returns back to its original place when the user dismisses the popup.

</td><td>

1.  Ensure Dynamic Window \(DW\) is enabled for Service Portal \(SP\) from the 'Assistants page'
2.  Navigate to **SP portal**.
3.  Enter **What is spam** in portal search.
4.  Select **Ask for follow up** once the Results page displays.

 Notice that DW opens with the pop-up 'Your previous chat was saved' and the portal page shifts to the left, but when the user when the user dismisses the **Your previous chat was saved** button, the page returns to its original place.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1948623

</td><td>

Uptake new versions of Unified Experience Framework \(UXF\)

</td><td>

UXF intent library changes to Zurich and Yokohama chat-components to uptake these versions.

</td><td>

 

</td></tr><tr><td>

Web UX Runtime

 PRB1879187

</td><td>

In Upgrade Console, the 'Guided Upgrade' page is blank for a long time when users log in for the first time

</td><td>

Opening 'Guided Upgrade' for the first time takes a long time to load the page.

</td><td>

1.  Navigate to **Admin Menu** &gt; **Upgrade Management**.
2.  Select **Get started** from the Overview page.

 Notice that the 'Verify Guided Upgrade' loads forever when it's the first time to log in to the instance.

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

 PRB1935240

</td><td>

Duplicate events appear when the schedule of a personal event changes

</td><td>

When using the flat table for personal events, duplicate events appear when the schedule of a personal event changes. The old user still has the personal event displayed on DW.

</td><td>

1.  Make sure the flat table is turned on.
2.  Open the cmn\_schedule\_p table.
3.  Add the **Schedule** field on the form \(if needed\).
4.  Open DW.
5.  Create a personal event for the user.
6.  Double-click \(or use the keyboard shortcut\) on the event.
7.  Observe that the cmn\_schedule\_p record opens in a new tab.
8.  Change the schedule to a user's personal schedule.
9.  Navigate to DW.
10. Select the **Refresh** button.

 Expected behavior: The personal event is only shown for the user based on the update.

 Actual behavior: Two personal events are shown. After the schedule changes to a different user, the old user still has the personal event displayed on DW.

</td></tr><tr><td>

Zing Text Indexing and Search Engine

 PRB1943229

</td><td>

Exact match always returns the same KB on Service Portal

</td><td>

Exact match should only show KBs that pass certain conditions, but queries always lead to one specific KB number.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 8 Hotfix 1](yokohama-patch-8-hf-1-PO.md)
-   [Yokohama Patch 8](yokohama-patch-8.md)
-   [Yokohama Patch 7 Hotfix 4](yokohama-patch-7-hf-4-PO.md)
-   [Yokohama Patch 7 Hotfix 2a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2556027)
-   [Yokohama Patch 7](yokohama-patch-7.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3 Hotfix 5](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2579293)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


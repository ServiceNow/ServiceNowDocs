---
title: Yokohama Patch 5
description: The Yokohama Patch 5 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-06-27"
reading_time_minutes: 98
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 5

The Yokohama Patch 5 release contains important problem fixes.

-   **Yokohama Patch 5 was released on June 27, 2025.**
    -   Build date: 06-25-2025\_1836
    -   Build tag: glide-yokohama-12-18-2024\_\_patch5-06-11-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y05.00.xlsx).

## Overview

Yokohama Patch 5 includes 329 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp5.png "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 5 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 5, refer to [KB2192702](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2192702).

## Changes in Yokohama Patch 5

-   **QueryRangeACLAuditor**

    This patch includes the May Maintenance update script in the form of a script include \(QueryRangeACLAuditor\). This script is not triggered automatically and must be run after a patch upgrade. More details on running the QueryRangeACLAuditor and its functionality can be found in [KB2046494](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2046494).

-   **[Workflow Data Fabric Hub](https://www.servicenow.com/docs/access?context=workflow-data-fabric&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US)**




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

Agent Chat

 PRB1900981

 [KB2226265](https://hi.service-now.com/kb_view.do?sysparm_article=KB2226265)

</td><td>

Inbox audio is delayed when the 'Workspace' tab is inactive or out of focus before receiving the first work item

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1840823

</td><td>

Temporary files are left by PG-JDBC driver

</td><td>

There must be obsolete .trs files in /glide/nodes/&lt;node port&gt;/tmp directory. Obsolete files are created 1 hour ago or before and not touched.

</td><td>

 

</td></tr><tr><td>

History Set

 PRB1844946

 [KB1923828](https://hi.service-now.com/kb_view.do?sysparm_article=KB1923828)

</td><td>

There's intermittent duplicate comments in an Activity Stream due to sys\_email records

</td><td>

Some comments are duplicated due to the presence of sys\_email records. This duplication occurs when a comment is added in a way that causes the incident's sys\_updated\_on timestamp to be one second earlier than the corresponding sys\_journal\_field record. If emails are triggered by the incident update, the loading of sys\_email records within the related sys\_history\_set interferes with the **last\_update\_recorded** field in sys\_history\_set. This disruption ultimately results in the duplication of the comment whenever the next update to the incident occurs.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Internal Platform Security Services

 PRB1813597

 [KB1790767](https://hi.service-now.com/kb_view.do?sysparm_article=KB1790767)

</td><td>

There's a MIME type check error when attaching a txt \(sjis code\) file after upgrading to Xanadu

</td><td>

MIME Type check error: '\[File type not permitted or mime type does not match the file content\]'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Controller

 PRB1847141

</td><td>

Lists in Service Operations Workspace \(SOW\) aren't automatically refreshing

</td><td>

When users enable the glide.lists.live\_list\_enabled property and make any changes in any record of the list, then the list refreshes in SOW version 5.0.1 but not in version 6.1.1.

</td><td>

1.  Navigate to an instance.
2.  Open Service Operations Workspace version 6.1.1.
3.  Navigate to any list in the SOW.
4.  Select the record number, and make some change to the record that should be visible on the list.
5.  Save and close the record.
6.  Observe that the record still displays in the list without the changes that were just made.
7.  Open a new browser session in a different browser.
8.  Navigate to the same list and make a change.
9.  Save.

 Observe that the list on the first browser session doesn't change. Eventually, a number appears on the **refresh** button at the top of the list. Select the button, and the data refreshes.

</td></tr><tr><td>

UI Form Administration

 PRB1866407

</td><td>

Activity Stream attachment tile actions don't work when a page has been set up to use the multi-controller template

</td><td>

Attachments aren't downloadable from the Activity Stream.

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

 PRB1889272

</td><td>

GlideSearch\_Query/suggestions user context gathering triggers role creation

</td><td>

When gathering user context, the platform triggers role creation.

</td><td>

 

</td></tr><tr><td>

Action Bar Component

 PRB1840507

</td><td>

An incorrect action bar intermittently displays

</td><td>

 

</td><td>

1.  Navigate to /now/cwf/agent/home.
2.  Impersonate a user.
3.  In the list, select **My cases** &gt; **New**.
4.  Select **Accept** UI action.

 Expected behavior: The action bar shouldn't change.

 Actual behavior: The action bar changes in a few seconds after the case is accepted.

</td></tr><tr><td>

Activity Stream Compose Component

 PRB1897434

</td><td>

The 'Email' tab in the Activity Stream in the CSM Configurable Workspace doesn't resize when the text is larger than the vertical limit

</td><td>

This issue is found in Yokohama, but works as expected in Xanadu.

</td><td>

1.  Navigate to a Yokohama instance as an admin user.
2.  Navigate to the **Activity Stream** &gt; **More** &gt; **Email**.
3.  Select **Return past vertical limit**.

 Expected behavior: The email text box auto-resizes vertically.

 Actual behavior: The email text box doesn't auto-resize.

</td></tr><tr><td>

Activity Stream

 PRB1881272

</td><td>

'Multiple delete' should check the condition list for archive tables

</td><td>

The 'Archive destroy' task uses multiple delete to remove sys\_journal\_field data. Users have to query the table to find which records specifically are deleted so that it can create a delete message for them. ActivityDBListener. removeMultipleEvents\(\) has to check the dbDeleteQuery. getQueryConditions\(\) for the rule's documentTable and ignore it if it isn't a table they care about.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1888279

</td><td>

The **Translation** button isn't turned on in a legacy Agent Workspace when dynamic translations are turned on

</td><td>

 

</td><td>

1.  Apply an update set to install, configure, and turn on dynamic translations, legacy Agent Workspace, and CSM/FSM Workspace.
2.  Open an incident in either legacy Agent Workspace \(/now/workspace/agent\) or CSM/FSM workspace \(/now/cwf/agent\).
3.  Add a comment in another language.

 Expected behavior: When hovering over the journal tile for the newly added comment, a **Translation** button should be visible and clickable.

 Actual behavior: When hovering over the journal tile for the newly added comment, there's no **Translation** button.

</td></tr><tr><td>

Activity Stream

 PRB1888552

</td><td>

Attachments aren't removed from an activity stream when stored on a secondary DBI

</td><td>

In a multiple delete scenario, when the activity stream DB listener creates a DBQuery to select all Activity Stream records to remove, it uses the default DBQuery constructor, which selects the primary DBI by default. The DB listener needs to pass the same DBI that's used by the DB action to ensure that the correct DBI is utilized in a multiple DBI situation.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1893483

</td><td>

No activity displays in UI16 when a blank journal event is added to the Activity Stream

</td><td>

After upgrading to Yokohama, some records display 'No Activity' on the platform view. A null pointer exception displays.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1894361

</td><td>

Timeago elements \(sn-time-ago\) should display a tooltip when accessed via the keyboard

</td><td>

 

</td><td>

1.  Navigate to any instance.
2.  Launch the Employee Service Center \(ESC\) portal by appending '/esc' to the URL.
3.  Navigate to the 'My Requests' menu item in the header and select.

The 'My Requests' page opens.

4.  Using the keyboard, navigate through the list of requests. Select 'tab' until the time focus goes on a sn-time-ago element.

 Expected behavior: If the focus should move to the non-interactive elements for sighted users who use the keyboard, then the tooltip should appear without hovering over it.

 Actual behavior: The tooltip isn't visible when the focus moves to the 'created/updated' elements using the tab key.

</td></tr><tr><td>

Advanced Risk

 PRB1896933

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in Advanced Risk

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1887118

</td><td>

The 'new message' sound and desktop notification aren't working in legacy workspace

</td><td>

 

</td><td>

1.  As an agent, navigate to the legacy workspace with the url /workspace/agent.
2.  As a requestor, start a chat.
3.  After an agent accepts the work item, as a requestor, start sending some messages.

 Expected behavior: When desktop and sound notifications are turned on, an agent should hear the sound for a new message and receive desktop notifications for the new message.

 Actual behavior: There's no sound or desktop notification.

</td></tr><tr><td>

AI Search

 PRB1850255

</td><td>

ScriptableSearchAdminQuery throws a NullPointException \(NPE\)

</td><td>

There's several areas where NPEs in AI Searches should be better handled.

</td><td>

1.  Create a search profile with no search sources.
2.  Search using that profile.

 Observe the NPE in the log.

</td></tr><tr><td>

AI Search

 PRB1875255

</td><td>

Glide sends an 'admin' value in the **Date** field

</td><td>

There's an error in the logs.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1885792

</td><td>

AI Search only logs sources that match a search in the sys\_search\_source\_event

</td><td>

 

</td><td>

Search with a query term that returns no results.

 Observe that no sources are logged in sys\_search\_source\_event. The entry for each source that was searched and has\_results=false.

</td></tr><tr><td>

AI Search

 PRB1892363

</td><td>

Citations in Genius Results, after selecting 'Ask in Chat', don't automatically close the pop-up, causing overlay

</td><td>

The Virtual Agent open page refresh pop-up appears if not permanently dismissed.

</td><td>

1.  Search 'Request laptop'.
2.  In the synthesized response, select **Citations** &gt; **Ask in chat**.

 Virtual Agent opens, but the citations pop-up is still open and doesn't close automatically.

</td></tr><tr><td>

AI Search

 PRB1893376

</td><td>

Need to support filters on KBBs in AI Search sources

</td><td>

Users currently lack the ability to exclude specific KBBs from the search sources. There should be a way to define and apply filters on KBBs within the search configuration—filters that are respected when retrieving results from AI Search.

</td><td>

1.  Create a KB containing a KBB.
2.  Index the 'Knowledge' table.
3.  Create a search profile with a search source containing that KB.
4.  Publish the search profile.
5.  Execute a query against that search profile, which only matches the content of the KBB \(and not the parent KB\).

See that the corresponding KB displays in the results.

6.  Add a KBB filter by adding sys property 'glide.ais.kbb\_filters'.

Only KBBs that match the encoded query are returned.

7.  Execute the same query as step 5.

 The same KB shouldn't appear on the results if the KBB doesn't pass the filter condition.

</td></tr><tr><td>

AI Search

 PRB1900322

</td><td>

A synthesized response isn't displaying on Portal when Dynamic Window \(DW\) is turned on

</td><td>

A response is present in the sys\_generative\_ai\_log. It's working fine in the chat.

</td><td>

1.  Open a Yokohama instance with recent Store apps.
2.  Enable DW on Portal.
3.  Perform a search for any query.

 Notice there's no synthesized response.

</td></tr><tr><td>

Analytics Data API

 PRB1839577

</td><td>

A chart is rendered with a default group by option when the 'None' group by option is selected

</td><td>

 

</td><td>

1.  Navigate to **All** &gt; **Library** &gt; **Dashboards**.
2.  Create a dashboard.
3.  Add a data visualization component to the dashboard.
4.  Select:
    -   Visualization type: Line
    -   Data source: Asset table \(alm\_asset\)
    -   Add Group by: Assigned to
    -   Add several 'Alternative group by' values
5.  Save the changes and exit from the editing mode.
6.  Check that the line chart is rendered according to the default 'group by - Assigned to'.
7.  On the line chart, select the three dots in the right top corner.
8.  Select **Show change group by**.
9.  Select the **None** option in the 'group by' menu.
10. Check the re-rendered line chart.

 Expected behavior: When the **None** option is selected, the line chart should be rendered as there's no group by.

 Actual behavior: The line chart is rendered with the 'Assigned to' group by.

</td></tr><tr><td>

Application Install Engine

 PRB1869500

</td><td>

The user is unable to upgrade a base app version when a batch install hosts a customized app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1894443

</td><td>

Integrate sn\_app\_deploy JSON functionality into Glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1886735

</td><td>

The 'Switch to Virtual Agent Web Client' link isn't receiving the keyboard tab focus

</td><td>

This impacts keyboard users who navigate documents sequentially and expect the focus order to be consistent with the sequential reading order.

</td><td>

1.  Navigate to any instance.
2.  Append sys\_store\_app\_list.do to the instance URL.
3.  Search for any Store plugin app, such as 'Virtual Agent Web Client'.
4.  Change the application scope to 'global'.
5.  Open the form.
6.  Tab to the 'Switch to Virtual Agent Web Client' link.

 Expected behavior: The 'Switch to Virtual Agent Web Client' link should be receiving the keyboard tab focus.

 Actual behavior: The 'Switch to Virtual Agent Web Client' link isn't receiving the keyboard tab focus.

</td></tr><tr><td>

Application Manager

 PRB1891971

</td><td>

The 'How Search works' info icon tooltip details are not announced by the screen reader

</td><td>

The JAWS screen reader doesn't read the tooltip content.

</td><td>

1.  Start JAWS.
2.  Navigate to the Home screen.
3.  Navigate to **Dashboard** &gt; **Entitled ServiceNow apps** &gt; **View all Applications**.
4.  Tab to the 'How Search works' info icon.

 Notice that JAWS does not read the tooltip content.

</td></tr><tr><td>

Application Manager

 PRB1891976

</td><td>

The Application Manager pop-up title is incorrectly described as 'Activity Log' by screen readers

</td><td>

 

</td><td>

1.  Start JAWS.
2.  Navigate to the home screen.
3.  Navigate to **Dashboard** &gt; **Entitled ServiceNow apps panel** &gt; **View all Applications link**.
4.  Press **enter** on the **Activity log** button.

Note that the screen reader dialog title announced is nothing like the visible modal dialog title.


 Expected behavior: It says 'Activity Log'.

 Actual behavior: It says 'Application Manager'.

</td></tr><tr><td>

Application Manager

 PRB1892000

</td><td>

There's a focus management issue on selecting **View More**

</td><td>

On selecting **View More**, more content is loaded. When pressing the tab key, the focus is going to the 'Skip to Main Content' link and not to the newly loaded items.

</td><td>

1.  Launch an instance in a Chrome browser.
2.  Navigate to **Filter** &gt; **All**.
3.  Navigate to **Admin center** &gt; **Application manager** &gt; **View all Applications link.**
4.  Scroll down and press **Enter** on the 'View more' link.
5.  Check where the keyboard focus is placed when the view more link is activated.

 Once more options are loaded and the user presses the tab key, the keyboard focus should go to the updated content and not to the 'Skip' link. However, when pressing the tab key, the focus is going to the 'Skip to Main Content' link and not to the newly loaded items.

</td></tr><tr><td>

Application Manager

 PRB1892002

</td><td>

The 'Sync in progress' and 'Sync completed' details aren't announced to screen reader users

</td><td>

On selecting 'Enter' on the **Sync Now** button, the sync starts progressing. That isn't communicated to the screen reader users.

</td><td>

1.  Launch an instance in a Chrome browser.
2.  Navigate to **Filter** &gt; **All**.
3.  Navigate to **Admin center** &gt; **Application manager**.
4.  Turn the screen reader on.
5.  Press enter on the **Sync** button.
6.  Check whether the screen reader communicates the sync in progress/complete state.

 Expected behavior: The 'Sync in progress' and 'Sync completed' details should be announced to screen reader users.

 Actual behavior: The 'Sync in progress' and 'Sync completed' details aren't announced to screen reader users.

</td></tr><tr><td>

Application Scoping

 PRB1889050

</td><td>

Apply cross-scope restrictions when querying locally mapped data fabric \(DF\) tables

</td><td>

 

</td><td>

1.  Create a Glide table in scope-A.
2.  Set its RCA property to 'Restricted'.
3.  Create a DF table in another scope \(Scope-B\).
4.  Map it to the Glide table.
5.  Query the DF table.

 RCA records should be created from Scope-B to Scope-A, in Scope-A, with source type = Data Fabric Table, with the correct source and target tables.

</td></tr><tr><td>

Appointment Booking

 PRB1894193

</td><td>

The scope of the Appointment Booking service's configuration was changed in Yokohama, which leads to a scope access issue

</td><td>

After upgrading to Yokohama from Washington, the value of the 'Availability' table changed from wu\_appointment to empty in some Appointment Booking service configuration records.

</td><td>

 

</td></tr><tr><td>

Audit Management

 PRB1896927

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in Audit Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1860702

</td><td>

The Vendor Portal 'Take-questionnaire' page stops working when the HR application is installed

</td><td>

Users observe an error on the page.

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB1892871

</td><td>

Cases RL on PI isn't accessible to a customer contact on the Business Portal due to query match and query range ACLs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change Management Collision Detector

 PRB1868251

</td><td>

The 'Conflict Detection' job, especially the ChangeCheckConflictsSNC script include, can lead to an OutOfMemoryError and node restarts

</td><td>

This seems to happen when the Affected CIs \[task\_ci\] table has a large amount of records on it. In one of the cases, there were 93,685,849 records.

</td><td>

Run the 'Conflict Detection' job and notice it loops in the ChangeCheckConflictsSNC script include.

</td></tr><tr><td>

Change Management

 PRB1862569

</td><td>

Change CheckConflict can cause stale reads and updates, which causes unexpected other behaviors

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1895395

</td><td>

A standard change template record producer condition builder filter operator is broken when the variable type 'List Collector' is used in conjunction with a standard change template field

</td><td>

On the 'Sample change requests' filter, after selecting a field, notice that all the operators are empty except for 'is'.

</td><td>

 

</td></tr><tr><td>

CMDB Query Builder

 PRB1791382

</td><td>

CMDB Query Builder results' count isn't consistent

</td><td>

There's a missing result from the CMDB Query Builder query. This causes missing some records in the result with a default batchsize \(100\) without the user knowing they are missing the records.

</td><td>

 

</td></tr><tr><td>

Communities

 PRB1865845

</td><td>

Some characters are displayed as unicode in blog titles

</td><td>

When a blog article in posted in the Community portal, some characters are encoded in unicode and then are displayed without being decoded.

</td><td>

1.  With the Communities plugin installed, set up a forum and put 'blog' in the 'Content type' related list.
2.  Navigate the Community portal.
3.  Navigate to **Community** &gt; **All forums**.
4.  Select the created forum.
5.  On the right-hand side menu, select **Post Content** &gt; **Blog**.
6.  In the blog title, input something like 'test漢字テストﾃｽﾄ７7'.
7.  Input a description.
8.  Select **Save as draft** or **Publish**.

 Observe that the title is now 'test漢字テスト&amp;\#xff83;&amp;\#xff7d;&amp;\#xff84;&amp;\#xff17;7'.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1893434

</td><td>

A11y bug fixes on CMDB Workspace

</td><td>

Info tooltips are identified by screen readers as 'Search Button' and there's multiple H1 elements on a page.

</td><td>

Issue 1: Info tooltips are identified by screen readers as 'Search Button'.

 1.  Start JAWS.
2.  Navigate to **Home** &gt; **All** &gt; **CMDB Workspace** &gt; **Management tab**.
3.  Move the input focus to the info icon in excluded CIs.

 Note that the info tooltip is described as 'Search button'.

 Issue 2: Multiple H1 elements on the page.

 1.  Navigate to **Home** &gt; **All** &gt; **CMDB Workspace**.
2.  Start NVDA.
3.  Display the speech viewer in NVDA.
4.  Navigate through the page's headings.

 Note that there are two H1s when there should only be one.

</td></tr><tr><td>

Content Analytics

 PRB1895477

</td><td>

The **agg\_period\_in\_tz** field causes a zero action\_count

</td><td>

Although sn\_cd\_analytics\_stat aggregation records for Content Analytics now populate both agg\_period \(date-only\) and agg\_period\_in\_tz \(full timestamp\), the \_calculateNumEvents method still does an exact match on agg\_period\_in\_tz using a date‐only string. Because the query value omits the time portion, no records qualify and every non-impression count is recalculated to zero.

</td><td>

1.  Follow the Content Analytics KB to activate and set a tracking profile to default.
2.  Using the 'Schedule Content' module, publish content on all tracked widgets.
3.  Using SCA and content templates, publish content on all tracked widgets.
4.  Follow the Content Analytics KB to publish a tracked campaign.
5.  Verify that the new dashboard 'Content Overview' appears as expected.

 Expected behavior: Audience, views, and clicks are recorded.

 Actual behavior: Only audience and views are recorded.

</td></tr><tr><td>

Content Experiences

 PRB1895089

</td><td>

Welcome Banner \(CD\) carousel dots are moving in reverse when pressing previous/next arrows

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Content Experiences

 PRB1895347

</td><td>

Topic header banner images aren't displaying for users without elevated privileges

</td><td>

This happens when 'Schedule Content' records reference pointers for a widget instance \(sp\_instance\) are broken, such as when the widget instance was deleted on the instance. With these schedules in this state, the topic header widget is somehow matching to the blank **sp\_instance** field and triggering the altered UI instead of the banner.

</td><td>

1.  Create a 'Schedule Content' \[sn\_cd\_content\_visibility\] record.
2.  Select a widget instance \[sp\_instance\].
3.  Save the 'Schedule Content' record.
4.  Delete the widget instance.
5.  Open a Employee Center page \(topic\) with a banner image.

 Expected behavior: A banner image displays for all users.

 Actual behavior: A banner image doesn't display for users without elevated privileges.

</td></tr><tr><td>

Content Experiences

 PRB1897513

</td><td>

New update/repair of a plugin causes the mass deletion of sys\_translated\_text records

</td><td>

After repairing and updating the plugin, the records in sys\_translated\_text table are completely erased.

</td><td>

 

</td></tr><tr><td>

Core Platform

 PRB1775831

 [KB1818197](https://hi.service-now.com/kb_view.do?sysparm_article=KB1818197)

</td><td>

When the user accesses a CTI record URL before SSO or a local login, they are redirected to an incident.do record

</td><td>

When the user is logged in to an instance, a CTI link takes them to the correct record. However, when they are logged out, they are directed to the incident.do page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Data Archiving

 PRB1865429

</td><td>

Infinite recursion is possible in the 'Archive Reparent Retry' job

</td><td>

In the 'Archive Reparent Retry' job \(though not in the reparenting code in the archive job itself\), a cycle in the sys\_archive\_related records causes infinite recursion. This can obstruct reparenting of other rules.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1855719

</td><td>

The cmn\_skill table isn't available to select as a node in the Knowledge Graph \(KG\) UI

</td><td>

In Project Management, there's a 'Resource Assignment' table that specifies which user/resource is working on which task. Also, a project manager can request for resources either by group or role or skill. Users are able to add a group or role via the KG UI. But currently, users are unable to add Skill \(cmn\_skill\) as a node.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1885744

</td><td>

List view for a Glide table joined with an external table returns SQL syntax error if filtered with conditions based on the external table

</td><td>

An SQL syntax error occurs when the user tries to run the list view of the Glide table with a filter that uses fields from the data fabric table.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1886440

</td><td>

When glide.db.trino.collate \_ci.references is turned on, 'lower\(\)' isn't used on 'JOIN' statements

</td><td>

The lower\(\) function is used in the 'WHERE' clause, but not in the 'JOIN' statement.

</td><td>

1.  Open an instance.
2.  Open the 'List' view.
3.  Set glide.db.trino.collate\_ci.references to '=TRUE'.
4.  Set glide.db.trino.collate\_ci to '=TRUE.
5.  Turn on SQL Debug.

 Notice that the lower\(\) function isn't used in 'JOINS', but is used in the 'WHERE' clause.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1886577

</td><td>

Because of incorrect datatype mapping, users are unable to map float\_type to Glide

</td><td>

Users aren't able to use the 'Float' and 'Long' data types, as they are inconsistent in usage.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1889900

</td><td>

CMDB list view never loads when grouped by 'Location' after a reference to a data fabric table is added

</td><td>

'Group by' never completes and times out.

</td><td>

1.  Navigate to an instance.
2.  Impersonate a system administrator user.
3.  Open the sys\_db\_object record for incident table.
4.  Add a new field that refers to a data fabric table.
5.  Save the sys\_db\_object record.
6.  Add the field to the list layout.
7.  Open the cmdb\_ci list view.

 Notice that when attempting to group by 'Location' the CMDB list never loads.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1890265

</td><td>

Users are unable to build a report due to the inability to run aggregate methods avg/sum for the **Long Integer String** field brought in by BigQuery and Databricks

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1894406

</td><td>

SQL error messages can't be enabled

</td><td>

If glide.db.loguser is set to 'false' by running the background scripts 'gs.setProperty\("glide.db.loguser", false\)', then only one error message appears. If glide.db.loguser is set to 'true', two error messages appear.

</td><td>

1.  Run the background script 'gs.setProperty\("glide.db.loguser", true\)'.
2.  Create a table by creating a record in the sys\_db\_object table.
3.  Navigate to the sys\_db\_object record in that table.
4.  Create a column with the type 'Auto Increment' in the 'Columns' section.
5.  Create a new record on the table, for example put the value '1' in the new column.
6.  Create a new record with the same value.

 Expected behavior: Two error messages appear when the user should only receive one; 'Unique Key violation detected by database \(\(conn=493\) Duplicate entry '1' for key 'PRIMARY'\)' and 'Invalid insert'.

 Actual behavior: Only one error message is shown, 'Invalid insert'.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1864182

</td><td>

An unreferenced record cleaner doesn't handle parent tables that are sharded and archived

</td><td>

 

</td><td>

1.  Create a parent table that is sharded or extension.
2.  Create an attachment that points to a record in this table.
3.  Create an archive rule for that table.
4.  Get the record archived.
5.  Create a table rotation for sys\_email with type 'extension'.
6.  Set up an archive rule for incident.
7.  Configure an archive related record with sys\_email that references the incident table.
8.  Run archive.

The incident is moved to ar\_incident, and related sys\_email is moved to ar\_sys\_email0000.


 Expected behavior: This record shouldn't be considered unreferenced and eligible for deletion.

 Actual behavior: This record could be deleted by the unreferenced record cleaner.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1865408

</td><td>

An unreferenced record cleaner can potentially cause unintentional deletion when a reference table is an archive table

</td><td>

In case of document ID type references, if a table **name** field has a table which is an archive table \(ar\_x\), currently the unreferenced record cleaner consumer doesn't check the corresponding base table\(x\) for existence. This can lead to data loss. This is because it is possible that the record is restored from ar\_x to x but the document ID reparenting process didn't update the table **name** field back to x.

</td><td>

1.  Create a document ID column table doc\_id\_tab.
2.  Create a table test\_tab.
3.  Archive records from the table test\_tab to ar\_test\_tab.
4.  Restore records from ar\_test\_tab.
5.  Insert a record in the table doc\_id\_tab with the table name as ar\_test\_tab and table\_sys\_id as sys\_id of one of the restored records.
6.  Create and run the unreferenced record cleaner rule for doc\_id\_tab.

 See the record from doc\_id\_tab being deleted equals data loss.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1866360

</td><td>

An unreferenced record cleaner is incorrectly applying GlideRecord.canDelete\(\) logic

</td><td>

 

</td><td>

1.  Create an unreferenced record cleaner rule for sys\_attachment/sys\_attachment\_doc.
2.  Run the unreferenced 'Record Cleaner' job on the rule.

 Observe orphans in sys\_attachment/sys\_attachment\_doc aren't deleted.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1869761

</td><td>

An unreferenced record cleaner \(URC\) doesn't handle parent tables that are sharded and archived

</td><td>

Currently, URC checks for a base reference table and an archive reference table. But if the base reference table is part of a hierarchy, when the reference record gets archived, it doesn't go to ar\_base\_table, it goes to ar\_child\_table. Archiving flattens the table hierarchy. The URC can delete such records as unreferenced but they are actually not orphaned.

</td><td>

1.  Create a table tab\_parent.
2.  Create a table tab\_child extending tab\_parent.
3.  Create table ref\_test with a 'Reference' type column referencing tab\_parent.
4.  Add records to the ref\_test referencing records in tab\_parent and tab\_child.
5.  Create an archive rule for tab\_parent which archives tab\_parent and tab\_child records to ar\_tab\_parent and ar\_tab\_child.
6.  Create a URC rule for ref\_test.
7.  Preview a sample of unreferenced records/run the 'URC' job.

 Expected behavior: No records are deleted.

 Actual behavior: Records belonging to ar\_tab\_child are deleted.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1871043

</td><td>

The unreferenced record cleaner \(URC\) rule using JoinUnreferencedRecordFinder can delete data that it shouldn't

</td><td>

JoinUnreferencedRecordFinder deletes data that shouldn't be deleted, and can return less than the chunk limit even if there is more data to be deleted.

</td><td>

1.  Create a test\_table with a reference to the test\_reference table.
2.  Insert data into test\_table with null references.
3.  Set the glide property glide.db.unreferenced \_record\_cleaner. verify\_before\_delete to '=false' when the default is '=true'.
4.  Verify that the glide property glide.db.unreferenced \_record\_cleaner.consider \_nulls\_unreferenced is set to the default '= false'.
5.  Run the unreferenced record cleaner for the rule.

 Expected behavior: Records with null references shouldn't be deleted.

 Actual behavior: Records with null references are deleted.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1884643

</td><td>

Unreferenced record cleaner \(URC\) doesn't handle parent tables which are sharded and archived

</td><td>

The archived record that is orphaned by the sharded parent table can be deleted by the URC, even though it should be considered unreferenced and shouldn't be deleted.

</td><td>

1.  Create a parent table that is sharded.
2.  Create an attachment which points to a record in this table.
3.  Create an archive rule for that table, for example, so that a child table such as ar\_sys\_email\_001 is created.
4.  Archive the record, so that it's in the example child table ar\_sys\_email\_001.

 Expected behavior: This record should not be considered unreferenced and ineligible for deletion.

 Actual behavior: This record could be deleted by the unreferenced record cleaner.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1888624

</td><td>

Archiving on data fabric \(DF\) tables results in multiple archive runs, but no records were archived

</td><td>

These process all create chunks which the framework later tries to execute on.

</td><td>

1.  Create an archive rule on a DF table to archive less than ten records.
2.  Wait for the hourly job.

It won't produce any runs if users try to execute **Archive now** or manually from sys\_trigger.


 Notice that over 3000 archive runs were created but no records were archived, and DF tables are read-only tables.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1881044

</td><td>

User session context needs to be identified appropriately during a Trino loop back call

</td><td>

When creating a HTTP session using OAuthToken in a loopback case, some context about the original session is lost. A nonce table needs to be set up that can be used to persist the original session ID, transaction ID, and the session type \(interactive/non-interactive\) along with user sys\_id using OAuthToken as nonce.

</td><td>

1.  Create a reference field on an incident table to a data fabric table.
2.  Log in as an interactive user.
3.  Look up an incident list with the reference field in the view.

 Observe the loopback session created is non-interactive.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1881949

</td><td>

Fast lock aren't released if a Tx is cancelled

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1884709

</td><td>

The user session context needs to be identified appropriately during the data fabric loop back call

</td><td>

 

</td><td>

1.  Create a reference field on an incident table to a data fabric table.
2.  Log in as interactive user.
3.  Look up an incident list with a reference field in the view.

 Observe that the loopback session created is non-interactive.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1887442

</td><td>

Don't shut down the Trino connection pool upon an InternalErrorException

</td><td>

Currently, when a Trino query fails execution and the translated exception is of 'InternalErrorException', the Trino connection pool shuts down. With the introduction of the ServiceNow Connector, any authentication error is translated as 'InternalErrorException', which causes the Trino connection pool to be retried and recreated. This is unnecessary and can make things slower as the cluster is really intact and has no issues.

</td><td>

1.  Establish a Trino connection.
2.  Load a data fabric table list view.
3.  Set the 'glide.db.df\_engine .sn\_connector. loopback. oauth\_access\_token. enabled' property to false.
4.  Load the same data fabric table list view.

It should complain in the UI about not having the oauth token in the request.


 Observe in the log that the trino\_primary pool was actually shut down and re-created. It would have 'unpooled: trino\_primary' in the log after the oauth token exception.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1888243

</td><td>

Loading the 'List' view for a Glide table that has an element referencing a data fabric table on a reference key is almost impossible

</td><td>

The list loads slowly and the 'Form' view doesn't open.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1890184

</td><td>

Users are unable to open the 'Incident Form' view when it references a Workflow Data Fabric \(WDF\) table

</td><td>

This also happens on an 'Incident' table in a SURF clone. It displays 'Record not found' or users see no records.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1891598

</td><td>

Exponential backoff upon refresh failure

</td><td>

This is to improve the resilience around cluster reservation.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1891600

</td><td>

Better handle pool shutdown during pool configuration

</td><td>

An error occurs when trino\_primary pool is shutdown \(by another thread\) during pool configuration.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1893025

</td><td>

A potential deadlock can occur if the loopback query lands on the same box

</td><td>

A semaphore isn't released if all of the transactions are executing Trino queries are waiting, and a 'deadlock' can potentially occur if the loopback request happens to come back to the same box.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1893055

</td><td>

Workflow data fabric for parent Epics

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1898714

</td><td>

A connection becomes vulnerable to sharing when it's marked for recycle

</td><td>

When a connection is marked for recycle, it's returned to the pool and can be picked up for allocation, where it's marked as 'Assigned'. The connection is checked for recycling and a new physical connection is established. Glide marks the connection as 'Available', which allows it to serve other requestors in the pool, causing connection sharing.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1857963

</td><td>

A string containing an underscore doesn't work in an encoded query with StartsWITH, LIKE, ENDSWith etc. on data fabric \(DF\) tables

</td><td>

 

</td><td>

1.  Load any DF table list view.
2.  Filter a column with phrase that contains an underscore character.
3.  Turn on Debug SQL \(detailed\).
4.  Reload the list view.

 Notice an 'ESCAPE' clause in the SQL running for 'trino\_primary' DBI.

</td></tr><tr><td>

Database Persistence

 PRB1861792

</td><td>

A Glide query with a **date/time** field throws an error

</td><td>

'Enable debug SQL detailed' throws this error after 25 seconds: 'Error executing query: Cannot invoke "io.trino.jdbc. $internal.client. QueryResults. getNextUri\(\)" because the return value of "java.util. concurrent.atomic. AtomicReference.get\(\)" is null'.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1862601

</td><td>

DatePart functions and 'Trend By' aren't working

</td><td>

Error: 'Query failed \(\#20250307\_002425\_02173\_asrt2\): line 1:1610: Function 'dayofweek' not registered'.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1864019

</td><td>

A boolean field in Snowflake isn't mapped to any data type in a data fabric table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1864033

</td><td>

From the 'Form' view, exporting a PDF exports an empty PDF document

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1864034

</td><td>

From the 'Form' view, 'Export as XML' doesn't work

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1869557

</td><td>

Running any GlideScript errors out when run after around 10 minutes of inactivity

</td><td>

The error executing query: 'Cannot invoke "io.trino. jdbc.$internal. client.QueryResults. getNextUri\(\)" because the return value of "java.util. concurrent.atomic. AtomicReference.get\(\)" is null'.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1870521

</td><td>

Upsert to reservation tables throws an exception

</td><td>

A unique key violation is detected by a database. Upsert throws an exception for duplicate entries.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1872092

</td><td>

LOWER\(\) usage in query predicate turns off predicate push down from Trino to an external data source

</td><td>

This means that when the SQL is executed, partial SQL is sent to an external data source: SELECT col1, col2, and col3 from sample\_table. This leads to bad query performance as PUSHDOWN of predicate doesn't happen, and that the entire table is downloaded from an external data source leading to \(a\) excessive data download, \(b\) bad query performance, and \(c\) high resource usage at Trino layer. Functionally, this bloats the 'data downloaded from external source' licensing metric.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1872106

</td><td>

'Show matching' in list view doesn't work for truncated data

</td><td>

In the 'List' view, if the user selects a field that displays a truncated value and selects 'Show matching', no value is returned.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1872607

</td><td>

Loading data fabric \(DF\) tables coming out of 'Idle time' for Trino throws a 500 error

</td><td>

A first time query hits an error: 'Error executing query: Error starting query...'

</td><td>

1.  Let 'Idle time' trigger for Trino.
2.  Stop queries for remote tables.
3.  After 10 minutes, query remote tables.

</td></tr><tr><td>

Database Persistence

 PRB1872718

</td><td>

There's an incorrect data type in the source table on the mapping screen

</td><td>

The data types of source columns doesn't match the data types on external databases.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1873237

</td><td>

Importing a BigQuery table is getting an error on the table name and blocking the import

</td><td>

Error: 'Failed to create remote table with error: Data Fabric Hub: Unable to create a remote table. com.glide. datafabric.model. DataFabricException: Expecting a prefix of "u\_df\_" for table name "df\_u\_supplier\_bg" Cause: null'.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1873825

</td><td>

countRemoteTable throws an error 'failed to get remote schemas' on a deactivated connection

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Create a Snowflake connection.
3.  Deactivate that connection.

 The screen refreshes and displays an error and the connection detail doesn't get loaded.

</td></tr><tr><td>

Database Persistence

 PRB1874006

</td><td>

Running any GlideScript errors out after 10 minutes of inactivity

</td><td>

The table list view was able to load before upgrading.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1876398

</td><td>

A join between cmdb$par1 or any table with special characters and a data fabric table would fail when the query gets to Trino

</td><td>

This issue only occurs with a base instance SNC connector.

</td><td>

1.  Create a join between a CMDB table \(for an element on $par1\) and a data fabric table.
2.  Execute a list or a glide record query.

 Observe the error.

</td></tr><tr><td>

Database Persistence

 PRB1877079

</td><td>

When a field is mapped and the field's Glide type is identified as UNKNOWN or DB\_UNKNOWN, this field shouldn't be available for mapping

</td><td>

There's an error querying a data fabric table.

</td><td>

1.  Log in to an instance that has data fabric setup.
2.  Import a table with a boolean field.
3.  Load a list view of the table.

 Users are getting an error: 'Query failed \(\#20250404\_164711\_05824\_egbw8\): line 1:853: Unexpected parameters \(boolean\) for function lower'.

</td></tr><tr><td>

Database Persistence

 PRB1882958

</td><td>

From Glide UI, the column type returned is displayed as glide\_date for minimum viable product \(MVP\) connectors

</td><td>

 

</td><td>

1.  Navigate to Workflow Data Fabric \(WDF\).
2.  Create a connection.
3.  Create a DF table.

 See the column type for 'Date'. The date is coming as glide\_date.

</td></tr><tr><td>

Database Persistence

 PRB1883871

</td><td>

Create an API for that returns a selective list of elements for a glide table that are allowed to have a reference key assigned

</td><td>

Relaxing requirements for glide tables and having 'persistence' control those requirements to provide an API. Currently, when a reference is created to a glide table from a data fabric table, a sys\_id is provided as the only option unless there is a unique key.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1883877

</td><td>

GlideRecord.query\(\) should limit the max number of rows returned when used in conjunction with a data fabric table

</td><td>

 

</td><td>

Execute GlideRecord.query\(\) on a data fabric table that has large result set \(for example, more than 100k\).

 Observe the rb\_\*.tmp files grow in size and count based on the number of row blocks created.

</td></tr><tr><td>

Database Persistence

 PRB1885159

</td><td>

Add support/capability for a guardrail or killswitch for an instance with Workflow Data Fabric \(WDF\) turned on

</td><td>

The guardrail or switch should be available to turn off the DF-specific processing and the transaction or operation should work as if no DF table exists. Glide Table elements should still continue to work without interruption.

</td><td>

1.  Introduce a field on a glide table that joins a data fabric table.
2.  Ensure 1,000 rows are loaded on the list.

 Observe amount of time it takes to load the list.

</td></tr><tr><td>

Database Persistence

 PRB1887082

</td><td>

'Catalog not found' exceptions are thrown when de-activating a connection

</td><td>

 

</td><td>

1.  Navigate to the Data Fabric Hub.
2.  Deactivate a connection.

 Notice that this triggers the ScriptableConnectionManager. jsFunction\_deactivateConnection\(\), updateConnectionStatus AndRefreshRemoteDB\(\), getDataFabricEngine Service\(\).invalidateTablesForCatalog \(connectionName\). This throws the following exception 'com.snc.db.df\_engine. DataFabricEngineException: failed to get remote schemas at com.snc.db.df\_ engine.DataFabricCatalog. getSchemas\(DataFabric Catalog.java:29\) at com.snc.db.df\_engine. DataFabricCatalog. getSchemaToMappedTables\( DataFabricCatalog.java:40\) at com.snc.db.df\_engine. DataFabricCatalog. invalidateAllTables \(DataFabricCatalog.java:85\) at com.snc.db.df\_engine. service.DataFabricEngineService. invalidateTablesForCatalog \(DataFabricEngineService.java:260\) at com.glide.datafabric. connection.ScriptableConnectionManager. updateConnectionStatus AndRefreshRemoteDB\( ScriptableConnection Manager.java:631\) at com.glide.datafabric. connection.ScriptableConnection Manager.jsFunction \_deactivateConnection \(ScriptableConnectionManager.java:463\)'.

</td></tr><tr><td>

Database Persistence

 PRB1887434

</td><td>

Ensure sys\_df\_data\_dictionary inherits ClientScripts and UIPolicies from sys\_dictionary

</td><td>

The script and UI policy changes should apply for sys\_dictionary table, however not for var\_dictionary table which is another child of sys\_dictionary.

</td><td>

1.  Navigate to a data fabric table dictionary column record.
2.  Attempt to make any changes on the data fabric dictionary record.

 Expected behavior: The user should be able to make changes such as string length edit without the formula being mandatory, and calculated and function types are not supported.

 Actual behavior: The calculated value section, **Formula** field is mandatory and doesn't allow the user to make changes.

</td></tr><tr><td>

Database Persistence

 PRB1891532

</td><td>

Add a guard rail to not allow certain Glide tables from having a reference field set out to reference data fabric table

</td><td>

Currently, users are able to add a field on central tables such as sys\_user and reference to data fabric tables. Guard rails are being added to ensure no outgoing references that refer to a data fabric table are allowed from a Glide table.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1897768

</td><td>

Running a GlideRecord query via a script on a large data fabric \(DF\) table results in a large amount of records queried

</td><td>

A large amount of records are queried even though results are truncated to 10,000.

</td><td>

1.  Have a large Workflow DF table with much more than 10,000 rows.
2.  Run GlideRecord.query\(\) in a script on that table without a limit set.

 Expected behavior: Some limit should have been applied on the remote data store.

 Actual behavior: Only 10,000 records are returned. On the remote data store, many more rows than 10,000 were queried.

</td></tr><tr><td>

Database Persistence

 PRB1898737

</td><td>

API returns a selective list of elements for a data fabric table that are allowed to have a reference key assigned

</td><td>

Currently DataFabricReferencableGenerator only returns referenceable columns for a Glide tables, and a similiar API is needed for data fabric tables.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1866372

</td><td>

The read ACL for sys\_df\_connection \_metadata doesn't work for data steward roles with upper cases

</td><td>

 

</td><td>

1.  Create a data steward role using at least one upper case letter.
2.  Assign this role to some connection.

 See that the data steward user can't see that connection.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1868977

</td><td>

The createRemoteTable method should allow a data steward to call it if they have read access to the connection

</td><td>

The access needs to be checked for the APIs created.

</td><td>

1.  Create a user with a data steward role for some connection.
2.  Impersonate the data steward user.
3.  Navigate to the 'Workflow Data Steward' UI.
4.  Try mapping a table using the connection.

 Notice that this should be allowed, but it's not.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1871926

</td><td>

Connection admin users need appropriate ACL access for table reads and services

</td><td>

Currently, there's no special permissions or roles bundled under our provided df\_connection\_admin role. Connection admin users must be able to assign user and data steward roles, which is currently breaking due to security constraints, preventing users from accessing/reading these tables.

</td><td>

1.  Log in to an instance as a user with elevated privileges.
2.  Navigate to the sys\_user\_role table to assign roles, accessing Workflow Data Fabric \(WDF\) app pages, etc.
3.  Navigate to the sys\_user table and assign any user with the df\_connection\_admin role.
4.  Impersonate or log in as this connection admin user.
5.  Navigate to the sys\_user\_role and related tables, and see a security constraint preventing access message.
6.  Check the WDF app.

 See that the connection admin users are now returned with no results when trying to access sys\_user\_role, or other impacted tables. Similarly, on connection creation and setting scope, they run into the issue with access constraints to sys\_scope records.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1874586

</td><td>

Users without the 'admin' or 'delegated\_developer' role can create tables via Workflow Data Fabric

</td><td>

Currently, only users with the 'admin' or a user that has a 'delegated\_developer' roles and when added as as a delegated developer to an application by an Admin/Application Admin can create tables.

</td><td>

1.  Assign a user with only the 'df\_data\_steward' role.
2.  Navigate to **WorkFlow Data Fabric** &gt; **Established Connection** &gt; **Create Remote Table**.
3.  Navigate to Sys\_db\_object to confirm the table is created.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1878836

</td><td>

A system administrator attempting to navigate to the 'Data Assets' page for an established connection encounters an error

</td><td>

A system administrator should have the necessary permissions to access the 'Data Assets' page for established connections and be able to create, edit, and delete tables without encountering an error.

</td><td>

1.  Navigate to the 'WDF overview' page.
2.  Select an existing established connection.

 Note that an error message is displayed: 'Data Fabric Hub: Unable to retrieve connection fields. com.glide.processors. json.ACLException: getSavedConnection is only authorized for role df\_connection\_admin'.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1878928

</td><td>

Error messages from the remote system aren't bubbled up on the UX

</td><td>

With a bad username or key, all it says is 'Encountered an unexpected exception. Please try again later', instead of bubbling up the right error message.

</td><td>

1.  Navigate to Workflow Data Fabric \(WDF\).
2.  Create a new Snowflake connection.
3.  Enter a bad username.

 Note the error: 'Encountered an unexpected exception. Please try again later'.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1881090

</td><td>

listAllMappedTables fails when connections mapped to tables are missing

</td><td>

If a table mapped to a connection/catalog is missing in the sys\_df\_connection\_metadata table, the listAllMappedTables API fails with an error: 'Cannot invoke "com.glide.datafabric. schemamapping. SchemaCaches $ConnectionInfo. getConnectionSysId\(\)" because "connectionInfo" is null'.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1881218

</td><td>

Update handleConnectorError to read from parm2

</td><td>

Connection/catalog details are now provided as part of 'parm2' when a warn/error event is generated.

</td><td>

1.  Create a ConnectorErrorException.
2.  Verify that this generates an event 'data\_fabric.error.connector\_error'.

 Notice connection details are available in parm2.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1881820

</td><td>

A system admin isn't able to create a connection

</td><td>

 

</td><td>

1.  Impersonate a system admin.
2.  Navigate to any connection form on Workflow Data Fabric \(WDF\) UI Hub.
3.  Fill the form with correct credentials.
4.  Select the **Connect** button.

 Expected behavior: The connection is established.

 Actual behavior: The connection isn't established.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1884525

</td><td>

Users can't delete columns from a data fabric \(DF\) application table

</td><td>

In the create \(or update\) DF application table flow, it calls the persistence loadSchema\(\) API before dropping the columns. This order is incorrect because the loadSchema API updates the TableDescriptor, and in case of when the column was deleted, the TableDescriptor doesn't contain that column. When dropColumn is called, an error displays.

</td><td>

1.  Create a Glide table with 3 columns.
2.  Call the createAppTable API to create a data fabric table based on this Glide table.
3.  Delete 1 column from the Glide table.
4.  Call the createAppTable again.

 Expected behavior: This column should get deleted from the data fabric table as well.

 Actual behavior: There's an error.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1884668

</td><td>

listAllMappedTables doesn't return glideTableLabel

</td><td>

 

</td><td>

1.  Create a data fabric \(DF\) table.
2.  Using 'Scripts Background', call SchemaMapping. listAllMappedTables.

 See that the response doesn't include any table's label.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1884675

</td><td>

Unable to connect to Oracle connector

</td><td>

Error: 'GlideElementPassword2 SEVERE \* ERROR \* GlideElementPassword2 couldn't encrypt the column: snc.oracle.wallet-pem-content from table...java.lang.Exception: Action abort: Password value is too long and could be truncated after encryption. Please either reduce password length or increase field size'.

</td><td>

1.  Navigate to an instance.
2.  Try to connect to Oracle.

 Notice the error message from the attachment.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1885160

</td><td>

Users are unable to update the connection details in 'Edit' mode

</td><td>

 

</td><td>

1.  Navigate to Workflow Data Fabric \(WDF\).
2.  Create a connection.
3.  Try to edit the connection and update the connection details.

 Notice that this doesn't work and the connection attributes remain as is.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1885246

</td><td>

Data Steward is unable to delete a Workflow Data Fabric \(WDF\) table from a scoped app

</td><td>

 

</td><td>

1.  Navigate to an WDF UI Hub.
2.  Create a new connection in any scoped app.
3.  Navigate to the 'Access Controls' tab.
4.  Add a Data Steward/Connection Admin role.
5.  Save it.
6.  This assigns the user with a Data Steward role to have access to the 'Data Assets' page of the established connection.
7.  Additionally, provide the Delegated Developer role to the same user so that they are able to create tables in the same scoped app.
8.  Impersonate the user having the Data Steward role.
9.  Create a WDF table.
10. Attempt to delete the table.

 Expected behavior: The table gets deleted and there's a success message on the WDF UI.

 Actual behavior: The table doesn't get deleted and an error is displayed: 'Failed to delete table. Please try again'.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1887047

</td><td>

Updating UI messages based on product review feedback

</td><td>

No functional issue exists. The changes are related to improving clarity, tone, or consistency of UI text messages as per the latest product expectations.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1888231

</td><td>

The 'Glide Internal Connection' isn't displaying in the established connections if the Workflow Data Fabric \(WDF\) license check fails

</td><td>

'Glide Internal Connection' should be available in the established connection by default, regardless of the instances licensed to WDF or not.

</td><td>

1.  Check for an instance that isn't licensed to WDF.
2.  Navigate to WDF Hub.

 See that the 'Established Connection' section has no connections.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1888349

</td><td>

Schema mapping API responses should return as a NativeObject

</td><td>

When the table doesn't exist, it throws an exception. The jsFunction\_listColumnsInTable doesn't catch it and lets the exception pass through, resulting in an error message that doesn't make sense.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1888617

</td><td>

Users can't drop a locally mapped data fabric \(DF\) table without a Workflow DF \(WDF\) license

</td><td>

There's an error: 'Failed to establish connection. Check your credentials or try again later. If the issue persists, contact your administrator. Additional Details: Instance is not licensed for Zero Copy Connectors cannot execute dropDataFabricRemoteTable.'

</td><td>

1.  Navigate to an instance that doesn't have Trino configured, and which doesn't have the WDF license.
2.  Create a locally mapped DF table.
3.  Try to delete this new table.

 Notice that dropping a locally mapped DF table should be possible without a WDF license.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1888676

</td><td>

A data steward can't create a data fabric \(DF\) table in a scoped app for a local instance connection

</td><td>

When a data steward connects a application table, it can connect it to local tables. During selecting columns, the column that isn't supported should be grayed out and not selectable from the menu. This scenario occurs for developed applications that have a space in the name\(" "\).

</td><td>

1.  Log in as a user having the delegated\_developer role and data steward role for any scoped app.
2.  Navigate to Workflow Data Fabric Hub.
3.  Select **Servicenow Local Instance** connection.
4.  Select any table belonging to the sn\_admin\_center scope from the schema list.
5.  Make the column selection for the DF table to be created.
6.  Select **Continue**.

 Expected behavior: The table gets created.

 Actual behavior: The table doesn't get created and throws the following error: 'Alert level: critical. Failed to create data fabric table with error: Data Fabric Hub: Unable to create a data fabric table. Failed to create data fabric table. You must have delegated development roles in this application scope to create a data fabric table'.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1889059

</td><td>

An upgrade resets to an 'open' instance status workaround on production test instances

</td><td>

Data fabric tables and zero copy connectors require a product to operate due to their additional Trino infrastructure. The zero copy connector metadata has been moved into a licensed store application sn\_data\_fabric\_ connector\_metadata. The Trino code is part of a core plugin, and the ability to reserve a Trino cluster should be limited to instances that are entitled to the zero copy connector application.

</td><td>

1.  On a production instance, set the instance status to 'Open'.
2.  Upgrade the instance to an updated track version.

 Note that the status is reset to 'Closed'.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1889097

</td><td>

Users encounter an error when attempting to map a 'char' column from an application table to a data fabric table

</td><td>

Additionally, users are unable to add a new column with the 'char' data type when creating a data fabric table from scratch.

</td><td>

1.  Navigate to the 'Data Assets' page.
2.  Select an existing schema and table.
3.  Select **Create Table**.
4.  Provide a name for the new data fabric table.
5.  Select **Continue**.
6.  In the column definition section, attempt to add a new column with the data type set to 'char'. Alternatively, if editing an existing data fabric table, try to change the data type of a column to 'char'.

 Observe that the option to select or add a 'char' column is unavailable.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1889647

</td><td>

'Ship First Party App to a new instance' and 'Edit connection' doesn't handle the TD cache properly

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1890695

</td><td>

Ensure that empty non-mandatory connection fields passed to the backend are handled correctly for all connectors

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1892019

</td><td>

Integrate with the 'Persistence' API for to check the referenceable columns from a table during data fabric \(DF\) table creation

</td><td>

Today, if users try to create a reference to a Glide table from a DF table, it provides the sys\_id as the only option unless there's a unique key.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1892093

</td><td>

Address decryption issues with **password2** fields

</td><td>

Users are getting an error when trying to establish connections: 'Alert level: critical. Failed to establish connection. Check your credentials or try again later. If the issue persists, contact your administrator. Additional Details: data fabric engine connection test failed'.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1893391

</td><td>

Users are able to make a reference from-to any type when creating a data fabric table

</td><td>

As part of this, references aren't allowed if the remote column type is integer. Only strings are supported.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1893437

</td><td>

Data fabric \(DF\) table default ACLs aren't consistent with a regular table's

</td><td>

DF tables should have default ACLs and table access policies set correctly.

</td><td>

Create a DF table in a private scope or in the global scope.

 Expected behavior: Default ACLs match to that of regular platform table's.

 Actual behavior: All the table access policies are set true except delete. No ACLs are created by default.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1893502

</td><td>

Deactivated connection tables are missing from the data fabric 'Tables' page

</td><td>

 

</td><td>

1.  Navigate to the 'Established Connections' page.
2.  Open an existing connection with associated tables.
3.  Deactivate the connection.
4.  Navigate to the data fabric 'Tables' page.
5.  Observe the displayed tables.

 Expected behavior: The deactivated tables should be available under the 'other' section within the data fabric 'Tables' page. The user should be able to change the connection of the tables under the deactivated connection.

 Actual behavior: Tables associated with a deactivated connection aren't on the data fabric 'Tables' page.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1894742

</td><td>

Adding a mapping level checks to check if the source table has RCAs

</td><td>

Currently, when a data fabric \(DF\) table is created from a Glide local table as the source, there are no checks in place to enforce if the source Glide table needs RCAs to access the table.

</td><td>

1.  Create a DF table using the Glide\_internal connection.
2.  Select a Glide local as source, which needs RCAs to access the table.
3.  Select columns to be mapped and complete the mapping.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1895491

</td><td>

There's an ACL exception as part of the exception translation service

</td><td>

When a user tries to delete a data fabric \(DF\) table when not authorized, it can throw an ACL exception. This exception must be handled in the exception translation class.

</td><td>

1.  Log in as an non-admin user.
2.  Try to delete a table created in the global scope.

 Observe that this throws an ACL exception: 'Failed to establish connection. Check your credentials or try again later. If the issue persists, contact your administrator. Additional Details: You must have the admin role to create or delete a data fabric table in the global scope'. The error message is misleading. The expected message is 'Failed to delete data fabric table. You must be authorized to create or delete a data fabric table in the global scope'.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1896064

</td><td>

A Snowflake established connection is broken after PEM key expiry and new key replacement

</td><td>

After updating the new key in established connections, in some instances the connection is successful, but the page goes blank.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1897712

</td><td>

Query errors from connectors change the connection status to NOT\_CONNECTED

</td><td>

When there was a query error from a connector, the connection status was changed to NOT\_CONNECTED. The connection status is supposed to change to not connected only when there's a real connection level error.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1812384

 [KB2234218](https://hi.service-now.com/kb_view.do?sysparm_article=KB2234218)

</td><td>

Inclusion pattern discovery fails with a NullPointerException if one of the identifications fails for a parent pattern

</td><td>

When the main pattern identification a fails, a NullPointerException exception is thrown: 'com.snc.sw.exception. PatternDebuggerException: Debug task failed to initialize parent CI for entry point: null.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1843083

</td><td>

The Discovery monitoring job to search for future jobs before deciding to terminate a status

</td><td>

The monitoring job cancels the status even though the instance has a job for it but hasn't pick it up yet.

</td><td>

1.  Have a status that is 'stuck' - input ECC queue in 'ready' state for more than 20 minutes.
2.  Have a record for that ECC queue in sys\_trigger table that is for the future.

 The job should cancel the status even though the instance has a job for it but didn't pick it up yet.

</td></tr><tr><td>

Discovery

 PRB1884527

 [KB2078932](https://hi.service-now.com/kb_view.do?sysparm_article=KB2078932)

</td><td>

A pattern on Agent Client Collector \(ACC\) requires MID specific configurations to the target device

</td><td>

When running a pattern on ACC, it requires the MID server to have discovery-specific port connectivity to the target instead of only using the ACC specific port.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1802663

</td><td>

A reference qualifier isn't applied for reference fields in the Agent Viewer experience

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1897412

</td><td>

Enable field group name update using Glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Dynamic Scheduling

 PRB1851315

</td><td>

When a dispatcher from an Australian timezone creates a personal event, the tasks overlapping the events aren't unassigned

</td><td>

 

</td><td>

1.  In Dispatcher Workspace, set the timezone of the dispatcher to be an Australian timezone.
2.  Create a task on one agent.
3.  With the same dispatcher, create a personal event that overlaps the tasks.

 Expect behavior: The overlapping task would be unassigned.

 Actual behavior: The overlapping task isn't unassigned and still overlaps the event.

</td></tr><tr><td>

Dynamic Scheduling

 PRB1894500

</td><td>

A work order task \(WOT\) isn't assigned to the selected user when using assignment assistance when there's no associated assignment group

</td><td>

This issue occurs in Yokohama.

</td><td>

1.  Create a WOT in a 'pending' dispatch state with no assignment group associated with it.
2.  Log in to Dispatcher Workspace.
3.  Select any WOT that doesn't have an assignment group associated with it.
4.  From the 'Task' panel, select **Overflow action** &gt; **Assignment assistance**.
5.  Select any agent that has been recommended.
6.  Select **Save**.

 Expected result: Either a proper message should be displayed that no agents should be recommended or the proper assignment group should be selected and the WOT should be assigned to the selected agent.

 Actual behavior: The following message is displayed and the WOT isn't assigned: 'This agent is busy during this time. Choose another agent.'

</td></tr><tr><td>

Edit List Columns

 PRB1855487

</td><td>

Changing an operator to 'is' reverts the reference list to a normal list and causes the **Caller** field to display as '\(Empty\)'

</td><td>

 

</td><td>

1.  Log in to any instance.
2.  Open any NRLC Workspace.
3.  Navigate to **Incidents** &gt; **All/Open**.
4.  Double-click a cell in the 'Caller' column to enable inline editing, then select the magnifying glass icon.
5.  Select the three-dot filter next to the 'Email' column and change the operator to 'is'.

 Expected behavior: The operator should be changed to 'is'.

 Actual behavior: Changing the operator to 'is' reverts the reference list to a normal list and makes the **Caller** field '\(Empty\)'.

</td></tr><tr><td>

Email Notifications

 PRB1887279

</td><td>

After a Yokohama upgrade, notifications broke because of an email script update

</td><td>

After an Yokohama upgrade, the email notification content broke. On analysis, it was found it might be caused by a change in one of the email scripts during the upgrade.

</td><td>

 

</td></tr><tr><td>

Employee Profile

 PRB1895942

</td><td>

There's encryption of attachments by users with the 'sn\_employee.admin' role after upgrading to Xanadu

</td><td>

The user is creating attachment records via a table API through a MID server script include. The attachments were previously not coming in as encrypted. After upgrading to Xanadu, they are being encrypted due to the 'sys\_kmf\_crypto\_ caller\_policy\_ 0b3419d867 323110fc90a2 aeb8f922c0' policy.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1842971

</td><td>

Service Dashboard doesn't load due to a slow API

</td><td>

When there are many services \(~2 million\) on cmdb\_ci\_serice\_auto and cmdb\_ci\_service\_auto\_cache is empty, Service Dashboard doesn't load.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1867782

</td><td>

Slow EM Events processing due to the default value for 'evt\_mgmt.max \_characters\_in \_additional\_info' is too low

</td><td>

When there are many events with addional\_info length &gt; 600,000 characters, events processing becomes slower.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1872971

 [KB2060302](https://hi.service-now.com/kb_view.do?sysparm_article=KB2060302)

</td><td>

Tag-based groups can include alerts which don't match the rule's filter

</td><td>

In the Xanadu release, a new tag-based alert correlation mechanism was introduced using the 'Query' job \(via the Service Analytics RCA/Alert Aggregation job\). There's an issue where alerts matching different tag-based definitions may not be grouped correctly if they arrive close together in time.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1884824

 [KB2082291](https://hi.service-now.com/kb_view.do?sysparm_article=KB2082291)

</td><td>

Tag-based groups can include alerts which don't match the tag-based alert clustering definitions tags

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1884862

</td><td>

If there's an automatic group filter for automated groups, tag-based groups aren't created

</td><td>

The alerts that are supposed to be grouped aren't grouped.

</td><td>

1.  Create a TAG definition or use a base instance definition.
2.  Create an automatic group filter for automated groups with something illogical so that the automated groups won't be created.
3.  Send at least two events that fit the definition.
4.  Wait for grouping job to run.
5.  Verify that alert exists in sa\_agg\_group\_alert\_staging table.

 Notice that alerts that should be grouped aren't grouped.

</td></tr><tr><td>

Event Management

 PRB1886771

</td><td>

Alerts with the same CI metric name aren't grouped together in the CMDB group if automated alert grouping is turned off

</td><td>

When Automated \(ML based grouping\) is turned off, the CMDB group isn't created for alerts with the same CI metric name.

</td><td>

1.  Turn off automated \(ML based\) alert grouping.
2.  Send two events with same CI metric name to create two alerts.

 Observe that CMDB group isn't created.

</td></tr><tr><td>

Event Management

 PRB1889397

</td><td>

If there's an alert with its initial event generated time in the future, an alert isn't added to tag-based group or alerts are split into a different group

</td><td>

 

</td><td>

1.  Create a tag definition.
2.  Create several events, whose alerts may be grouped by tag according to the definition above.
3.  Create another event.
4.  Change via script the initial event generated time \(initial\_remote\_time\) to the future of the relevant alert.
5.  Create one more event and don't change the time. It should be added to the exiting group.

 All events should be in the staging table, but aren't.

</td></tr><tr><td>

External Triggers

 PRB1878365

</td><td>

Change sys IDs to readable values in GCF definitions of external triggers

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Field Service Marketplace

 PRB1874290

</td><td>

The 'Add Contractor' action is still active in lane 2 of the playbook even after moving it to lane 3

</td><td>

The issue is reproducible in Yokohama and Xanadu.

</td><td>

1.  Provision an instance with the Contractor Management and Marketplace Plugins installed.
2.  Log in as wm\_dispatcher.
3.  Create a work order task \(WOT\) in Workspace.
4.  Push to marketplace.

 The user lands on playbook experience where in the lane 1 request is created. In lane 2, after selecting contractors and moving to lane 3, if the user navigates back to lane 2, the **Add Contractor** action is still active. But when selected, it throws an error.

</td></tr><tr><td>

Field Service Marketplace

 PRB1895775

</td><td>

'Add contractor' isn't turned off in playbook lane 2 and lane 3 after the status is complete for that lane until the page is refreshed

</td><td>

 

</td><td>

1.  Create a task.
2.  Push to MP.
3.  In lane 2, select **Contractors**.
4.  Push the request.

It redirects to lane 3.


 Notice in lane 2, **Add Contractor** is still enabled until the page is manually refreshed. Similarly on lane 3, **Add contractor** is enabled even after selecting the **Close response** window.

</td></tr><tr><td>

Field Service Task Bundling

 PRB1888651

</td><td>

'Add to Bundle' fails on the latest 28.x DWS

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1811796

</td><td>

Nodes went offline and won't rejoin a node pool after a restart due to stack overflow in EventHandlerJobPool

</td><td>

Self hosted instance few nodes crashed due to the 'com.glide.event\_ manager.process\_ automation.event\_ handler.workers' system property with the value -1.

</td><td>

1.  Navigate to /sys\_trigger\_list.do.
2.  Add filter Name=Process Automation Event Handler.

By default, there should be 2 per node.

3.  Change the system property 'com.glide.event\_ manager.process\_ automation.event\_ handler.workers' to -1.
4.  Navigate back to check the same page/filter as step 1.

There should now be 0 Process Automation Event Handler records.

5.  Navigate to **All** &gt; **Node Logs File Download**.
6.  Download the localhost\_log.current\_date.txt.

 Observe that the logs contain a retry attempt message multiple times and afterwards throws a StackOverflowError.

</td></tr><tr><td>

Flow Engine

 PRB1853618

</td><td>

High priority \(P0-P4\) flow events should be queued on the current node for lower latencies

</td><td>

High priority events aren't cached to the current node. This results in longer latencies \(30+ seconds\), which shouldn't exist for high priority flows.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1860060

</td><td>

sys\_flow\_context\_inputs\_chunk record was removed by the table cleaner before the SLA timer resumed

</td><td>

Currently, the table cleaner of sys\_flow\_context\_inputs\_chunk has the condition matchfield=sys\_created\_on with age = 3,628,800 sec \(42 days\) and the original inputs is false. The original inputs field is set to false right after the flow starts. If the SLA definition has a long duration, the table cleaner may remove the sys\_flow\_context\_inputs\_chunk record before the SLA timer resumes.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1816646

</td><td>

The update number on the record remains the same when it is updated by the subflow and parent flow in sequence, causing inconsistencies in SLA executions

</td><td>

When the subflow updates the trigger record, and parent flow updates the same trigger record, the update number on the trigger record remains the same. This impacts respective SLA executions on the record.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1891084

</td><td>

Alias override mappings for V2 action instances aren't captured in flow update XML

</td><td>

This issue was caused by the introduction of JSON save on action instances. The FlowDesignerSychnronizer isn't syncing related records for V2 action instances.

</td><td>

1.  Ensure glide.flow.version != '1'.
2.  Provision an instance with the ID com.glide.hub. integrations.enterprise plugin installed.
3.  Add an outbound connection for the spoke being used.
4.  Create a flow.
5.  Add either the **Create a Container** action or some other action with a 'connection' action property.
6.  Pick the connection from step \#1 as the 'Docker Connection' on the 'Create a Container' action instance just added.
7.  Save the flow.
8.  Look for the most recent sys\_update\_xml for the flow.
9.  Open the XML viewer for the **sys\_update\_xml** payload field.

 Observe that the sys\_hub\_alias\_mapping is missing.

</td></tr><tr><td>

FX Currency Conversion

 PRB1861950

 [KB1962510](https://hi.service-now.com/kb_view.do?sysparm_article=KB1962510)

</td><td>

Daily currency rates retrieval from European Central Bank \(ECB\) may fail due to a lack of response from an Online Certificate Status Protocol \(OCSP\) endpoint

</td><td>

The 'Retrieve System Rates' and the 'ECB Exchange Rate Load' jobs, which are used to capture currency exchange rates using the ECB endpoint, are failing intermittently across multiple instances because the OCSP endpoint for ecb.europa.eu isn't answering validity questions during certain times.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

GlideRecord

 PRB1864786

</td><td>

When creating a reservation with an incorrect warehouse, the connection is set up but the Glide Table UI fails to log, and errors display

</td><td>

Sometime when loading the UI page, the first page displays data but the data is invalid. The next page is empty with no errors. There's an error in the log: '\*\*\* ERROR \*\*\* Encountered Exception while loading Table from ResultSet, closing java.sql. SQLException: Query failed \(\#20250312\_ 222003\_00046 \_c99gn\): No active warehouse selected in the current session. Select an active warehouse with the 'use warehouse' command.'

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1865565

</td><td>

The data fabric \(DF\) Logger and error event handling mechanisms are missing the catalog, details, and queue

</td><td>

The current implementation of the logger and error event handling mechanisms has three issues. The logger doesn't automatically include the catalog when it is missing in the logger builder, even though it is available in the exception details. The generated error events lack essential details such as table, schema, and catalog information, making it difficult to trace the source of issues. Error events are currently handled in the generic queue.

</td><td>

Trigger a ConnectorErrorException where the catalog is available in the exception details but not explicitly set in the logger builder for an inactive connection/catalog.

 Observe that the df\_log table log records display up without the catalog name, the first parameter field of the generated event doesn't include the catalog/table/schema name as a **key/value** field, and events are not part of any queue.

</td></tr><tr><td>

GlideRecord

 PRB1865622

</td><td>

GlideRecord queries are processed even though the connection status is 'INACTIVE'

</td><td>

Currently, the connection status to 'INACTIVE' is ignored, and the queries are processed. Users expect query requests to be blocked when the connection status is 'INACTIVE' to prevent unnecessary processing and failures. An error message should be displayed.

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1869620

</td><td>

'Data Fabric Logger' and 'Error Event Handling' are missing catalog, details, and queue

</td><td>

'Data Fabric Logger' was using 'Map.of', which throws an error when any values are null. Some of the values for catalog, schema, table, dfTable, logcategory could be null, so this shouldn't have thrown an error.

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1871360

</td><td>

Review the RecordCache API in relation to the data fabric \(DF\) table

</td><td>

The SQL query is executed 9 times on the workspace form view load. Extra queries occupy the cluster as well as semaphores which may impact non only Workflow Data Fabric \(WDF\) related traffic on the instance, but non-WDF as well, by exhausting semaphores.

</td><td>

1.  Navigate to /now/sow/list.
2.  Create 'My list' using a WDF table.
3.  Open the created list.
4.  Open the form from the list.

</td></tr><tr><td>

GlideRecord

 PRB1871916

</td><td>

If **PK** fields are defined where values are null, there should be an alert on lists, forms, and Genius Results stating that platform functionality is limited

</td><td>

 

</td><td>

1.  Define a Workflow Data Fabric \(WDF\) table.
2.  Set the PK to 1 or more fields that have null values.

 Platform behavior related to the sys\_id is strange because it's difficult to identify that record uniquely and reliably. An alert should be present and a warning log message in 'df\_log' should be present stating that platform functionality is limited. There should be an error message in the 'df\_log' table. There should also be a sysevent starting with the name 'data\_fabric.error.PrimaryKeyProblem'.

</td></tr><tr><td>

GlideRecord

 PRB1871950

</td><td>

If **PK** fields are defined where values are null, there should be an alert on 'List', 'Form', and Genius Results stating that platform functionality is to be limited

</td><td>

If a Genius Results \(GR\) query includes query params on all the **PK** fields, and the database returns 0 or more than 1 record, GR should set LastErrorMessage and lastException stating that the primary key isn't unique. The list and/or form view should display the error message.

</td><td>

1.  Define a Workflow Data Fabric \(WDF\) table.
2.  Set the **PK** to 1 or more fields where the fields don't uniquely identify each record.

 Expected behavior: The platform lists display a list of records when selecting a record to open the form view. There should be an alert stating that there is a problem with how the PK is defined. This doesn't fix the form or list operation, but it tells the user that something is not right.

 Actual behavior: The platform list displays a list of records when selecting on a record to open the form view. The expected record isn't selected. There should be a warning/info message on the list and/or form page if the GlideRecord query on a WDF table where the primary key isn't defined to have actual unique records. There should be an error message in the 'df\_log' table. There should also be a sysevent starting with the name data\_fabric.error.PrimaryKeyProblem.

</td></tr><tr><td>

GlideRecord

 PRB1872592

</td><td>

A sys-event record non-translatable exception is created with the **Name** field having 'data\_fabric' appearing twice

</td><td>

The **Name** field of the record contains the text 'data\_fabric .error.data \_fabric.operation. unsupported'. All teams write to that log.

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1874644

</td><td>

A 'PK Problems' warning displays in cases when it shouldn't

</td><td>

If **PK** fields are defined, and the query condition is on **PK** fields but it's not an equals condition, there's a warning that 1 or more record was found. The warning should only display if the condition is on an equals operator. Also, if a query is on **PK** fields, but the query also has an exception that results in zero records returned the PK warning that zero records were found displays. Warnings about PK problems shouldn't display if there was a separate exception preventing the query for executing properly.

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1881668

</td><td>

Every message logs as an error in the df\_log table

</td><td>

For example, 'Error WDF\_CONNECTION\_MANAGER Successfully refreshed remote connection DataFabric'.

</td><td>

1.  Navigate to any instance.
2.  Connect to Big Query.
3.  Map a table.
4.  Navigate to the df\_log table.

 Notice every log is recorded as an error.

</td></tr><tr><td>

GlideRecord

 PRB1884480

</td><td>

GlideTrinoStatsListener log update

</td><td>

The log level should be changed to 'DEBUG' on GlideTrinoStatsListener of the processStats.

</td><td>

Trigger a Trino Query.

 See that GlideTrinoStatsListener logs TrinoStats at the 'INFO' level.

</td></tr><tr><td>

GlideRecord

 PRB1887896

</td><td>

Unsanitized cache TTL attribute read causes NumberFormatException

</td><td>

The 'Data Fabric Cache' table is created during the first query execution. This approach introduces unnecessary query latency for the user's first access to the cache.

</td><td>

1.  Enable caching.
2.  Add or modify a cache TTL configuration with a non-numeric value \(for example, '30s' instead of '30'\).

 Observe that the log throws a NumberFormatException.

</td></tr><tr><td>

GlideRecord

 PRB1888657

</td><td>

Add indexes on the 'Data Fabric Cache' table

</td><td>

The 'Data Fabric Cache' table lacks necessary indexes on two critical fields: **cache\_key** and **cache\_expires\_at**. This absence can cause performance degradation when querying the table, particularly in high-volume transactions and during cache cleanup operations.

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1889243

</td><td>

There's a 'NamedMessage.getMessage \(L10N\_CODE, errorMsg, map\)' variable warning

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1889865

</td><td>

Getting an error for a standard record page template in runtime when using a test value table as 'incident' in UI Builder

</td><td>

Error: 'Platform behavior may be limited because of problem detected with primary key definition, zero records were returned for table...'

</td><td>

1.  Navigate to UI Builder.
2.  Create a page from the 'Standard Record Page' template.
3.  Update the table test value.
4.  Select **incident**.
5.  Save the page.
6.  Select the preview menu and select 'Open URL path'.

 Expected behavior: The page loads in runtime without any error.

 Actual behavior: The page loads fine but the user is alerted about the error.

</td></tr><tr><td>

GlideRecord

 PRB1894453

</td><td>

Create a scripted definition for usage metrics

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1895699

</td><td>

A cache table creation message is displayed for data fabric \(DF\) tables

</td><td>

 

</td><td>

Create a DF table.

 A message for cache table creation is displayed when the user visits the list page of the newly created DF table.

</td></tr><tr><td>

GlideRecord

 PRB1897719

</td><td>

Optimizations for data fabric caching

</td><td>

Introduced strict validation and logging for 'IQueryCondition' types. Only allow caching for queries using fully supported conditions. Added support for longer than 74 characters table names by using a new format for the cache table name when the table name length is between 74 and 80 characters. Flushing the data fabric cache every time the TTL attribute gets changed to prevent serving stale data. Changed the log category for the 'Data Fabric Cache' table to 'WDF\_CACHE\_TABLE' to improve log filtering and analysis. A new scriptable API method 'DataFabricCacheManager. flushCache\(df\_table\_name\)' is available and accessible via scoped application scripts.

</td><td>

 

</td></tr><tr><td>

GRC: Business Continuity Planning

 PRB1894009

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Business Continuity Planning

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Business Continuity Planning

 PRB1897810

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Business Continuity Planning

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Continuous Authorization and Monitoring

 PRB1893692

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Continuous Authorization and Monitoring

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Metrics

 PRB1894403

</td><td>

When EBA is enabled, a query range isn't working on the 'Threshold' table due to a 'deny unless' ACL

</td><td>

It throws an error, but it should be able to query the records if the user has access.

</td><td>

1.  Log in as a ESG user to the latest main instance.
2.  Open the 'Threshold table list' view.
3.  Try searching thresholds by query range.

</td></tr><tr><td>

GRC: Operational Resillience

 PRB1896635

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Operational Resillience

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Privacy Management

 PRB1900172

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Privacy Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Profiles

 PRB1894767

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Profiles

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Regulatory Change Management

 PRB1890993

</td><td>

Addition of Query ACLs in GRC: Regulatory Change Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Risk Shared Common Components

 PRB1897619

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Risk Shared Common Components

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Vendor Portal

 PRB1889689

</td><td>

Addition of Query ACLs in GRC: Vendor Portal

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1874464

</td><td>

The 'Suspended Reason' is overwritten with its previous value when the case moves from 'Draft' to 'Suspended state'

</td><td>

The issue is only reproducible when: the state moves directly from 'Draft' to 'Suspended', on HR Agent Workspace and not on UI16, and when the **Suspended reason \[sla\_suspended\_reason\]** field is on the form.

</td><td>

1.  Log into an instance.
2.  Impersonate a system administrator.
3.  If the **Suspended reason** \[sla\_suspended\_reason\] field isn't on the HR Case 'Workspace UIB' view, add it to the form.
4.  Open HR Agent Workspace.
5.  Create an HR Case with the HR service 'General Inquiry'.

Notice how the **Suspended reason** field displays as 'User' but it's empty.

6.  Manually set the **State** field from 'Draft' to 'Suspended'.

A pop-up window displays.

7.  On the modal, set the reason to 'Group', add work notes.
8.  Select **ok.**

 Expected behavior: The 'Suspended Reason' should be 'Group'.

 Actual behavior: The 'Suspended Reason' is set to 'User'.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1897036

</td><td>

NACM auto-grow functionality doesn't work correctly for Hebrew language content

</td><td>

Selected text is incorrect and elaborate/shorten is done on empty text. When the default preset action is present along with preset actions, the user doesn't see a preset menu and instead sees a default preset action.

</td><td>

 

</td></tr><tr><td>

Identification and Reconciliation API

 PRB1898162

</td><td>

Dynamic IRE key enhancement and validation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Install Base Management Store

 PRB1890911

</td><td>

Due to query match and query range ACLs, related list cases on product inventorie \(PI\) aren't accessible to a contact on Business Portal

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1884096

</td><td>

When a consumer replication set is created, the replication entry should have 'Preserve Modified By' set to true

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1893073

</td><td>

Implement a not-allow list for data fabric \(DF\) tables in Instance Data Replication

</td><td>

Users shouldn't be able to create replication entries against DF tables.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1882852

</td><td>

A source field isn't attached with the GlideRecordSecure insert operation

</td><td>

There's a field-level ACL kb\_knowledge.source with the role 'nobody' on the write operation, which prevents populating the source field for the 'create' operation.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1808314

</td><td>

The user is unable to personalize list columns for Oracle DB instances

</td><td>

A related list renders with old columns.

</td><td>

1.  Log in to an Oracle DB instance as an admin user.
2.  Open an incident on Service Operations Workspace.
3.  Select **Related records**.
4.  Select any of the related lists \(for example, Task SLAs\).
5.  Select the gear icon and **Edit Column**.
6.  Select some new columns and select **Ok**.

 Expected behavior: The related list should render with new columns.

 Actual behavior: The related list renders with old columns.

</td></tr><tr><td>

List Administration

 PRB1847198

</td><td>

featureFlags of sys\_ux\_list isn't working when switching between list menu lists in a 'New list' template

</td><td>

The default values of controller props are used on the cases, other than the first load.

</td><td>

1.  Create a UI Builder page with a 'New list' template page.
2.  Update some feature flags in one of the sys\_ux\_list items.
3.  Navigate to the 'Realtime' page of the newly created list template page.
4.  Select the list menu list where the feature flags are modified.
5.  Switch to some other list in the same menu.
6.  Switch back to the previous list.

 Expected behavior: quickEdit should be hidden by honoring the sys\_ux\_list config.

 Actual behavior: quickEdit is visible.

</td></tr><tr><td>

List Administration

 PRB1861358

</td><td>

The rich description appears as NULL in the 'List' view but displays correctly in the case record

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Create an HR case.
3.  Navigate to sn\_hr\_core\_case.LIST.
4.  Open the newly created case.
5.  Select the hamburger icon and configure the form layout.
6.  Add the **Description** field.
7.  Save the changes.
8.  Return to the HR case form.
9.  Enter a message in the **Description** field.
10. Save the changes.

 Observe that the same value is automatically updated in the **rich\_description** field. This behavior is due to the 'Sync Description with rich\_description' business rule that synchronizes the values of the **Description** and **rich\_description** fields. When users go to the list view and add the 'Description' and 'rich\_description' columns, notice that the rich\_description field doesn't contain any value. The reverse works as expected; when users update the **rich\_description** field in the HR case form, the value appears in the **rich\_description** field in the list view.

</td></tr><tr><td>

List Administration

 PRB1887929

</td><td>

A list type field isn't displaying the choice label on a list and instead displays its choice value

</td><td>

If choices are created on a task it works as expected. If choices are created on an incident only, there's a behavior difference between Xanadu and Yokohama. If choices exist for both tasks and incidents, the incident list in Yokohama incorrect displays task choice labels.

</td><td>

1.  Navigate to a Yokohama instance.
2.  Navigate to a dictionary.
3.  Create a list type field on a 'Task' table.
4.  In the choices related list on a dictionary, create some choices for an 'Incident' table where the label differs from the value.
5.  Navigate to an incident form.
6.  Configure the form.
7.  Add the created list type field on the form.
8.  For the list type field, add some value in the form.
9.  Navigate to incident.list.

 Notice the list type field is displaying the choice value instead of the choice label. Repeat the same step in a Xanadu instance and observe it is working fine.

</td></tr><tr><td>

List Controller

 PRB1872717

</td><td>

When the user creates a new 'My List' and edits the columns, the list doesn't display personalized columns until the page is refreshed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1892485

</td><td>

Reference fields in a 'Workspace' list cause slowness, as each reference triggers an additional SQL call

</td><td>

In workspace, every reference in the list is requested separately. In contrast, in UI16, a single query with a JOIN is executed for the whole list representation. While for the primary database it doesn't have a significant impact, for Workflow Data Fabric tables \(WDF\), where each query takes &gt;1s, even with small tables loading a list with 20 records can cause significant performance degradation.

</td><td>

1.  Create a table with a reference to the WDF table.
2.  Open /now/sow/list.
3.  Create 'My list' using the newly created table.
4.  Open the list.

 All references are requested from the external data source one by one for each record, even if there's duplicates.

</td></tr><tr><td>

Major Incident Management

 PRB1891876

</td><td>

The **View Workbench** UI action is redirecting to a broken 'Activity' section when opening it for a second time on a major incident form on the classic UI

</td><td>

After upgrading in Yokohama, when managing a major incident \(MI\) in the classic UI and moving to the 'Workbench' view, it's not loading properly. It's redirecting to a MI management broken activity view.

</td><td>

1.  Open any major incident.
2.  Select **View workbench**.

MI workbench loads.

3.  Select **View form**.
4.  Once the form is loaded, select **View workbench** again and wait.

 See that a different form view is loaded instead of workbench. It seems to be that the redirection URL is changing to this form view.

</td></tr><tr><td>

MID Server

 PRB1864193

</td><td>

Upgrading a Linux MID Server to Xanadu reverts mid.shconf\_override to the default setting

</td><td>

mid.shconf\_override has an empty setting. It's reverted to default setting after upgrading.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1883251

</td><td>

The 'Block Mobile Attachment Sharing' property for Mobile doesn't support exemption based on user roles

</td><td>

Changing the property glide.sg.block\_ mobile\_attachment \_sharing from 'false' to 'true' should exempt some users based on their roles for the security property.

</td><td>

1.  Navigate to **sys\_properties.list**.
2.  Change the property glide.sg.block \_mobile\_attachment \_sharing from 'false' to 'true'.

 Notice that this applies to all users, when only some users require the ability to download or view attachments on Mobile based on their role.

</td></tr><tr><td>

Next Experience Notifications Menu

 PRB1851718

</td><td>

A URL isn't updated when navigating from the migrated dashboard by clicking the notifications

</td><td>

There's an issue on the unified navigation side that is causing this for several releases.

</td><td>

1.  Navigate to pa\_dashboards.LIST.
2.  Select a dashboard.
3.  Choose **Migrate Dashboard** from the 'Actions' menu.
4.  Open the migrated dashboard from the message displayed on the top of the page.
5.  Search for the migrated dashboard and open it.
6.  Have a notification in the notification bell at the top-right hand corner of the Next Experience UI.
7.  Select the bell.
8.  Select the incident record in the notification list.

 Observe that while the record displays in the main window, the URL bar isn't successfully updated and the tab name is wrong.

</td></tr><tr><td>

On-Call Scheduling

 PRB1868011

</td><td>

The 'Show Schedule' link doesn't work for a non-admin user

</td><td>

After upgrading to Xanadu, non-admin users aren't able to access the on-call schedule.

</td><td>

1.  Impersonate a non-admin user.
2.  Open any on-call schedule for the group.
3.  Select the 'Schedule' column for any schedule.
4.  Select the UI Action **Show Schedule**.

 Observe that an error is thrown.

</td></tr><tr><td>

On-Call Scheduling

 PRB1893263

</td><td>

A query range error displays when the Automated Certificate Management Environment \(ACME\) rota\_admin is accessing cmn\_rota\_member record filters

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1864500

 [KB2216882](https://hi.service-now.com/kb_view.do?sysparm_article=KB2216882)

</td><td>

Activating Now Assist skills creates unnecessary \[sys\_update\_xml\] records which shouldn't be transferred between instances

</td><td>

Unexpected customer updates are being automatically generated for one\_api\_\* tables extending \[sys\_metadata\]. This causes confusion among users as they are unaware of how the updates are generated and these records aren't intended to be transferred via an update set.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB1900147

</td><td>

Users are unable to open responsive CoreUI dashboards

</td><td>

An error message appears: 'Sorry! The requested dashboard has not been shared with you.'

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1783660

</td><td>

A search isn't giving the expected results when the user language is set to non-English

</td><td>

The localization of the title of 'Visualisations' is also not working.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Filters

 PRB1841953

</td><td>

A filter is unexpectedly dispatching the 'reference' type

</td><td>

A filter is used to return 'choice' in the filter configuration type, but it was changed it so that it may return 'reference' when the field isn't 'choice'. This isn't fully correct, and it may also cause issues to other BUs and users. The filter should always return 'choice' for single and multi-select filters.

</td><td>

1.  Create a dashboard.
2.  Add a filter component to it.
3.  Select as it as a 'data source incident' table and the 'field assignment' group.
4.  Add a data visualization to the dashboard.
5.  Select a 'single score' type and an 'Incident' data source table.
6.  Save the changes.
7.  Apply any value from the filter.
8.  Open the Webinspector to look at the network calls.
9.  Refresh the visualization and look at the payload of the network call for the multivis API call.

 Expected behavior: The existing filterConfigurations has a type 'choice' for single or multi-select filters.

 Actual behavior: The existing filterConfigurations has the type 'reference'.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1882396

 [KB2072479](https://hi.service-now.com/kb_view.do?sysparm_article=KB2072479)

</td><td>

**Recipient Users** and **Recipient Groups** fields don't populate on migrated scheduled export records after the Platform Analytics migration

</td><td>

After the Platform Analytics migration on Yokohama, the **Recipient Users** and **Recipient Groups** fields from scheduled reports records don't populate to the **Recipient Users** and **Groups** fields for the migrated scheduled export records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1894148

 [KB2173216](https://hi.service-now.com/kb_view.do?sysparm_article=KB2173216)

</td><td>

Bulk migration rewrites the scope of all Core UI dashboards

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Licensing

 PRB1894922

</td><td>

Apps update to true-up a newer version of LE and SM in Yokohama

</td><td>

'Delete auditing' is on by default for all tables. In one of the tables, there's logic that's deleting all records and re-creating them, which is flooding user audit records. By adding the no\_audit\_delete flag for the table, it avoids creating these audit records.

</td><td>

1.  On an instance with SM 4.1, create a test record in the unconfirmed\_user\_role table.
2.  Navigate to a sys\_audit record.
3.  Filter the table by unconfirmed\_user\_role.

 Observe that there's delete audit records.

</td></tr><tr><td>

Platform Runtime

 PRB1900474

</td><td>

There's a difference in the number of sys\_journal\_field records created when running GR.setDisplayValue\(\) before GR.insert\(\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1820635

</td><td>

Users see a 500 internal server error when doing a prediction from the Rest API explorer

</td><td>

Error: 'error: ava.lang.IllegalArgumentException: Invalid input format...'

</td><td>

1.  Create a classification solution and train.
2.  Open the Rest API explorer.
3.  Select the API name as 'predictive intelligence'.
4.  Select for multiple records.
5.  Add all the queries.

 Expected behavior: The status code should be 200.

 Actual behavior: User see a 500 error.

</td></tr><tr><td>

Predictive Intelligence

 PRB1832015

</td><td>

The training failed because the solution has a table as an input field, but the platform\_ml\_read role is missing from the input table

</td><td>

This issue occurs because the scheduler worker is logged in with a user that has the platform\_ml\_read role. If this role is missing from the table, the scheduler worker is unable to read the table data, causing the training to fail.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1887194

</td><td>

A root cause analysis \(RCA\) fails when an invalid field is present in a content pack shipped by a process configuration

</td><td>

There's an issue when an ITSM content pack was installed on an instance and it had an **RCA** field 'hold\_reason', which was not present in the 'Incident' table of that instance. Since there was an invalid field, RCA was failing and in guided setup and this process configuration record wasn't opening.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1903878

 [KB2229304](https://hi.service-now.com/kb_view.do?sysparm_article=KB2229304)

</td><td>

After upgrading from Xanadu to Yokohama release, process mining filtersets and scheduled tasks are being deleted

</td><td>

During the upgrade from Xanadu to Yokohama, the process mining filter set conditions and scheduled tasks are being deleted. Due to a backend issue, the upgrade script execution unintentionally deletes saved filter sets and scheduled tasks of Process Mining Projects. This particularly affects configurations with "transition filters" linked to scheduled tasks. Although no other customer data was affected, this issue may disrupt functionality where the deleted filter sets or scheduled tasks were actively used.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Project Management

 PRB1859066

</td><td>

A Resource Assignment \(RA\) is associated to a new Resource Plan upon migration

</td><td>

The resource plan associated with an RA is in the 'Completed' state. When the effort value is updated, a new resource place is created and attaches the RA to the new resource plan. A new plan shouldn't be created, and the resource assignment should be pointing to the initial completed resource plan.

</td><td>

1.  Create a resource plan.
2.  Allocate it.
3.  Complete the plan.
4.  Migrate the plan to resource assignment.

 Notice that upon migrating the plan, the newly created resource assignment will be linked to the completed resource plan; when attempting to change the effort type on the resource assignment record, a new resource plan with an allocated state is created.

</td></tr><tr><td>

Project Management

 PRB1889859

</td><td>

Actuals for planning item are not rolled up to the task type breakdown

</td><td>

Enable actual costs from expense lines to rollup to the 'Actual cost' on associated cost plans related to planning items without the core table integration. When user creates a new expense line for a planning item in the 'New financials' page for a planning item, the actual cost value on the cost plan breakdown should add up to the total amount from processed expense lines.

</td><td>

1.  Create a planning item without integrations.
2.  Add cost plans and expense lines.
3.  Validate the actual roll up to task type breakdown.
4.  Validate the roll up to investment entity.

</td></tr><tr><td>

Remote Tables

 PRB1885282

</td><td>

There's an out of memory exception when there's JavaScript and ^NQ in the encoded query string

</td><td>

Encoded strings are saved by calling setEncodedString on the query condition. This is done per row bases. As it is checking query conditions for each row, a saved encoded query is appended to the previous one. Eventually, it eats up the memory.

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB1874881

</td><td>

A calendar report doesn't display Japanese characters correctly

</td><td>

The issue is reproducible in Yokohama.

</td><td>

1.  Create a record on the vtb\_task table with short description '保守：YokohamaへVerUpリグレ開始'.
2.  Create a CoreUI Calendar report based on the vtb\_task table and the **Updated** field.
3.  On the 'Calendar' report, Japanese characters aren't displayed correctly.

 Expected behavior: '保守：YokohamaへVerUpリグレ開始'.

 Actual behavior: '20:36 保守&amp;\#xff1a;YokohamaへVerUpリグレ開始 - 保守&amp;\#xff1a;YokohamaへVerUpリグレ開始'.

</td></tr><tr><td>

Resource Management

 PRB1860646

</td><td>

A top task isn't updated for existing resource assignments when a project is made or removed from being a child of another project

</td><td>

When a project that has an existing resource assignment is added to another project as a child project the top task of the resource assignment isn't being updated. Additionally, when a project with an existing resource is removed from being a child of another project, the top task of the resource assignment isn't being updated.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1877603

</td><td>

In Resource Management Workspace, there's a NullPointer exception

</td><td>

In Resource Management Workspace, users get nullpointer exception when changing resource status for an allocation.

</td><td>

1.  Open Resource Management Workspace.
2.  Open a card.
3.  Change the status of the assignments for a user.

</td></tr><tr><td>

Rollback and Recovery

 PRB1809473

</td><td>

When truncating a logical non-root table in TPH or TPP, all records are stored for ancestors and siblings in a shadow table

</td><td>

 

</td><td>

1.  Create 2 tables using the 'Table Per Hierarchy' extension model \(u\_table1 and u\_table2 extending the former\).
2.  Seed some test data on each tables.
3.  Invoke 'DBI.tableDrop\(\)' for u\_table2 with rollback enabled.
4.  Confirm that records from u\_table1 were recorded in the shadow table 'sh$u\_table1'.

 That shadow table should only have records for u\_table2 since those are the ones that were deleted and therefore the only ones that could be restored by rolling back the truncate of the logical table 'u\_table2'. This can become a costly, unnecessary operation if the parent table is large.

</td></tr><tr><td>

Schedule Optimization

 PRB1891169

</td><td>

On Demand Intraday, selecting multiple territories displays an 'Optimizing' icon even when there's no optimization running

</td><td>

 

</td><td>

1.  Create an Intraday configuration for multiple territories, and ensure that those are overlapping territories.
2.  In the config, set the 'On Demand' boolean to true.
3.  As a dispatcher, navigate to Dispatcher Workspace \(DWS\).
4.  From DWS settings, turn off the 'Territory single select' toggle.
5.  From the territory selection on top left, select those same territories that are present in the intradat config.

 Expected behavior: We shouldn't see the 'Optimizing' icon when there's no optimization running.

 Actual behavior: Users are seeing the 'Optimizing' icon on the calendar for those territories even if there's no optimization running.

</td></tr><tr><td>

Schedule Optimization

 PRB1898555

</td><td>

When one of overlapping territories has 0 tasks, double booking happens

</td><td>

 

</td><td>

1.  Create overlapping territories.
2.  Ensure that one or more overlapping territories have 0 tasks.
3.  Run optimization.

 Actual behavior: None of the existing assignments for that territory are sent as locked, so it double books.

 Expected behavior: Double booking shouldn't happen.

</td></tr><tr><td>

Server-side scripts

 PRB1883239

</td><td>

ESLatestScriptLoader returns a warning message

</td><td>

The message reads, 'Version loading was stopped by ESLatestScriptLoader for sys\_es\_latest\_script...'.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1883153

</td><td>

Blob reaper alerts for jobs that are running for less than 48 hours

</td><td>

 

</td><td>

1.  Navigate to sys\_status.
2.  Look for records with the name 'glide.service.modeling.startSweep, glide.service.modeling.lastSweep'.
3.  Change one of them so that the value in lastSweep is 25 hours after the value in startSweep.
4.  From the browser URL, type 'https://&lt;InstanceName&gt;.service-now.com/xmlstats.do'.
5.  Look for blob\_reaper\_job\_stuck and see its value is 'true'.

</td></tr><tr><td>

ServiceNow Voice \(Family\)

 PRB1894893

</td><td>

Add an AI Voice Agent service type to libkmf

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1625349

</td><td>

The 'Ideas' tablist widget breaks accessibility requirements

</td><td>

The 'Ideas' tablist widget isn't screen reader accessible because it doesn't conform to the WCAG 4.1.2 Name, Role, Value \(Level A\) rule. Specifically, it's missing the tabpanel role and also missing various states, properties, and values required for screen readers to be able to parse the markup and make sense of it for people with low or no vision. Right now, the screen reader isn't able to tell users when focus lands on the first tab that it is 'One of two' or 'Two of two' when focus moves to the second tab. It doesn't indicate what tab is currently selected, meaning which content is currently visible. Focus doesn't automatically move into what should be the tabpanel area, so nothing is read when the selected tab changes.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1875043

</td><td>

In the 'Canada - French' language, submitting a date in 'dd-MM-yy' format causes an error

</td><td>

When a user sets their language to 'Canada - French' and attempts to submit a date in the format 'dd-MM-yy', the date doesn't apply correctly, resulting in an error.

</td><td>

1.  Install the plugin com.snc.i18n.french-canada \(French - Canada\).
2.  In the instance, navigate to **All** &gt; **Basic Config** &gt; **Date Format**.
3.  Set the system date format to 'dd-MMM-yy'.
4.  Mark the 'Sample Item' catalog item as active.
5.  Assign it a category so it displays in the service catalog for users.
6.  Set the date variable to 'mandatory'.
7.  Navigate to the /sp \(Service Portal\).
8.  Search for 'Sample Item'.
9.  Ensure that the language is set to French - Canada.
10. Fill in the date variable.
11. Submit.

 Observe that there's an error, and the date doesn't apply to the field.

</td></tr><tr><td>

Service Portal

 PRB1891178

</td><td>

The scroll doesn't work on the Portal when it is 400+ zoom

</td><td>

 

</td><td>

1.  Navigate to Service Portal.
2.  Zoom the size to 400%.
3.  Scroll from the top to the bottom.

 Expected behavior: The scroll should happen at 400% zoom.

 Actual behavior: The scroll doesn't work.

</td></tr><tr><td>

Service Portal

 PRB1894604

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for widget-data-table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Smart Assessment Engine

 PRB1900594

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in Smart Assessment Engine

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1830073

 [KB2120852](https://hi.service-now.com/kb_view.do?sysparm_article=KB2120852)

</td><td>

The 'Software Asset Connections' job fails when a cmdb\_rel\_ci record doesn't have a child

</td><td>

The job fails with the error: 'Script: SAMPDataSource lntegrationUtils: \[2024-11-22T23:32:26.885Z\]: Unable to match value 'undefined' with field 'sys\_id' in table 'cmdb\_ci. Expecting type 'GUID''.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1845794

 [KB2186255](https://hi.service-now.com/kb_view.do?sysparm_article=KB2186255)

</td><td>

The 'ITAM License Report' module isn't displaying in upgraded instances from Washington DC/Xanadu to Yokohama releases

</td><td>

The module is missing.

</td><td>

1.  Install HAMP.
2.  Log in to the instance and check for the 'ITAM License Report' module under the 'ITAM Licensing' menu.
3.  Note that the module isn't available.

 Expected behavior: The 'ITAM License Report' module should be visible under the 'ITAM Licensing' menu.

 Actual behavior: The 'ITAM License Report' module is not visible under the 'ITAM Licensing' menu.

</td></tr><tr><td>

Software Asset Management

 PRB1878871

</td><td>

The 'Publisher Overview' page doesn't load after a user clicks on the publisher card after recon is completed

</td><td>

The 'Publisher Overview' page should be loaded completely, but only loads after selecting the **Refresh** button.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1883407

</td><td>

The default value for month in the samp\_sw\_usage table remains in the dictionary after upgrading to Xanadu

</td><td>

 

</td><td>

1.  Provision a Washington DC instance with samp plugins.
2.  Upgrade the instance to Xanadu.
3.  Observe the default value of **month** in the samp\_sw\_usage table.

 Actual behavior: The default value is 'January'.

 Expected behavior: The default value should be empty.

</td></tr><tr><td>

Software Asset Management

 PRB1892609

</td><td>

The install date isn't in the expected format when the date format is changed

</td><td>

 

</td><td>

1.  Open the 'Download GLAS' report page.
2.  Update the data and time format of the user or system.
3.  Download the vCenter VM Report.

 Observe that the 'Install date' column isn't in the expected format.

</td></tr><tr><td>

Software Asset Management

 PRB1893997

</td><td>

Install consumption journey nodes aren't displaying the correct number of installs

</td><td>

The issue is the redundant query on the software install model.

</td><td>

1.  Create some software installs for SQL Server.
2.  Make a few installs inactive \(active=false\).
3.  Run recon and wait until the recon is complete.
4.  Navigate to install consumption analysis.
5.  Select the SQL Server root node to see the installs modal.

 Expected behavior: The number of installs on the node should match the number of installs displayed on the modal.

 Actual behavior: In the modal, the inactive installs are missing.

</td></tr><tr><td>

SSH MID Server Communication Protocol

 PRB1887914

</td><td>

SSHProtocolEngine thread is overwhelmed when SSH server starts dumping instead of sending a protocol version string

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Store IRM GRC Core Case Management

 PRB1892851

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in Store IRM GRC Core Case Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Store IRM Privacy Case Management

 PRB1894359

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in Store IRM Privacy Case Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB1892411

</td><td>

If users get an exception during assignPartitions\(\), GlideHermesConsumer isn't closed in MessagePollSubscription

</td><td>

The root cause appears to be an instance of GlideHermesConsumer that is created but not closed in the case of exceptions.

</td><td>

1.  Create a topic, consumer, and subscription.
2.  Shut down the Hermes cluster or do something to cause exceptions when trying to read from the topic in Hermes.

 This creates a situation where Glide picks up a subscription and tries to read from the underlying topic but can't because it is missing. This produces some stack traces in the logs.

</td></tr><tr><td>

Stream Connect Core

 PRB1900417

</td><td>

A kafka\_admin doesn't have report view access to the sys\_sc\_alerts table

</td><td>

 

</td><td>

1.  Create a user.
2.  Add the kafka\_admin role to the user.
3.  Impersonate as the user.
4.  Navigate to the Store app.

 In the 'Overview' page, users aren't able to view the alerts in the 'Active alerts' section.

</td></tr><tr><td>

System Update Sets

 PRB1834468

</td><td>

A sys\_db\_object record was created when the **Function** field was loaded through update, set, and commit

</td><td>

When creating a database view and **Function** fields on the instance through UI, a sys\_db\_object isn't created for the database view table. If a commit or update contains certain actions, it will create a sys\_db\_object for the database view table.

</td><td>

1.  Import the update set that contains sys\_update\_xmls for the **Function** field for a database view.
2.  Preview it.
3.  Commit it.

 Expected behavior: The sys\_db\_object record was not created for the database view.

 Actual behavior: The sys\_db\_object record was created.

</td></tr><tr><td>

Table Administration and Data Management

 PRB1771107

</td><td>

Creating a list type field on cmdb\_ci from the Configure &gt; Form Layout page breaks the cmdb table due to the field being created with an incorrect storage alias entry

</td><td>

After the field is created with its storage alias mapped to cmdb but the actual column in the backend being created on cmdb$par1, there's the following error when accessing cmdb\_ci.list: 'Syntax Error or Access Rule Violation detected by database \(\(conn=218714\) Unknown column 'cmdb0.list\_field\_name' in 'field list'\)'. The list displays all empty rows.

</td><td>

1.  Confirm that sys\_table\_partition.i s\_current\_target is true for cmdb$par1 or any of the other partitions other than the base partition.
2.  Navigate to sys\_db\_object.list.
3.  Open the 'cmdb\_ci' table.
4.  From the related links on the form, select the **Show Form** link.
5.  Right-click on the form header and select **Configure** &gt; **Form Layout**.
6.  Enter any name for the field and select:
    1.  **Type** &gt; **List**
    2.  **Table to Reference** &gt; **cmdb\_ci\_service\_discovered** OR **task.**

 Notice that the field in the database gets created on the current partition like cmdb$par1 but if users look at sys\_storage\_alias for the new field it is pointing the storage table name as cmdb. Navigate to cmdb\_ci.list to notice the syntax error message.

</td></tr><tr><td>

Table Administration and Data Management

 PRB1888056

</td><td>

DMTSchedulerUtils. scheduleDM expects a global Genius Results \(GR\) parameter

</td><td>

DMTSchedulerUtils\(\).scheduleDM results in an error: ''gr' is not defined'. There's a bug in the script that expects 'gr' as a defined global variable.

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1899540

</td><td>

Field Service Management data filters are restricting access for RSO/CSM personas

</td><td>

Both wm\_location\_agent and wm\_location\_assignment\_manager roles should be able to see all the wm\_order and wm\_task.

</td><td>

 

</td></tr><tr><td>

Third-party Risk Management

 PRB1889679

</td><td>

Addition of Query ACLs in Third-party Risk Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Transform Maps

 PRB1847878

</td><td>

Slow loading of related lists for particular transform maps

</td><td>

It takes several minutes to load a related list from a sys\_transform\_map record.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1891838

</td><td>

The TinyMCE editor is missing on the 'Share to work notes' model

</td><td>

An error message is displayed on the console: 'TypeError: Cannot read properties of undefined \(reading 'themeOptions'\)'.

</td><td>

1.  Open any active incident record.
2.  Select the **Summary** button.
3.  Find if that summary is generated.
4.  Select the **Share** button.
5.  Observe that the TinyMCE editor is missing on the 'Share to work notes' model.

</td></tr><tr><td>

UI Field Administration

 PRB1892439

</td><td>

When a preset action is selected and autogrow is false, there's infinite loading

</td><td>

 

</td><td>

1.  Have a quickAction with autogrow as false.
2.  Have this quickAction configured on a **Form** field as a default or normal preset action.

 See that when this quick action is selected, the modeless dialogue opens but nothing happens.

</td></tr><tr><td>

UI Form Administration

 PRB1860501

</td><td>

A form's cache key doesn't account for roles with external and internal users

</td><td>

A generated cache key doesn't contain roles.

</td><td>

1.  Enable the 'Explicit Roles' plugin.
2.  Modify ACLs to incident to allow read access to the snc\_external role.
3.  As an external user, navigate to any given incident.
4.  As an admin, navigate to the sys\_db\_cache table.

 Expected behavior: The cache entry created by the external user, should include the users roles in the cache key.

 Actual behavior: The cache key generated doesn't contain roles.

</td></tr><tr><td>

UI Form Administration

 PRB1863573

</td><td>

A 'Scope tag not permitted' error is thrown when the UXC Generative AI plugin is active

</td><td>

The scoped UI macros are added to the UI16 form by the 'UXC Generative AI' plugin clash with scoping rules, causing a 'Scope tag not permitted' error to be thrown. Visually, users notice related lists and others macros not loading on the form.

</td><td>

1.  Navigate to sysapproval\_approver.list.
2.  Open any record still in the 'Requested' state.
3.  Right-click on the header and configure the form layout.
4.  Add the 'Test Formatter Approval Scoped' formatter to the layout after the 'Approval Summary' formatter.
5.  Configure the form.
6.  Add 1 related list to better see a broken page when reproducing.
7.  Clear the cache using cache.do.
8.  Open the record.

 Observe that the form is in a broken state. The approval \_summary form renders on the page, but everything else is missing. Related lists won't display. Users aren't able to right-click on the header or see the scoped UI macro rendered.

</td></tr><tr><td>

Usage Analytics

 PRB1879227

</td><td>

Users aren't able to filter UX Analytics Data on 'User Properties' as User Property Sync Service fails due to inbound mTLS not being turned on

</td><td>

Users can't filter their user experience analytics data by user roles, departments, and related user properties.

</td><td>

1.  Log in to the instance where an inbound mTLS isn't turned on.
2.  Configure the user properties in the sys\_analytics\_user\_property\_config table.
3.  Run the scheduled job 'User Property Config Change Sync Job'.

 Expected behavior: The user properties data should be synced from the instance to ClickHouse. The user shouldn't see the warning message when the sys\_analytics\_user\_property\_config table is opened.

 Actual behavior: The user properties data isn't synced to ClickHouse.

</td></tr><tr><td>

User Presence

 PRB1767417

</td><td>

Multiple threads can unnecessarily race to build the user presence cache, adding a load to the primary database

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1834547

</td><td>

An additional HR case creation form opens when selecting the 'View All' details of 'Cases for Subjected Person', 'Cases for Opened For', or 'Interactions' in a some scenarios

</td><td>

Occurs on the HR Agent Workspace 'HR Case creation' page.

</td><td>

1.  Log in as an HR Agent.
2.  Navigate to the HR Agent workspace.
3.  Select the **New HR Case** creation button.
4.  Search for and select an employee.
5.  Select the **Next** button.
6.  Refresh the page.
7.  Enter the employee name again.
8.  Once the 'Create a New Case' page loads, select **View All** for 'Cases for Subjected Person', 'Cases for Opened For', or 'Interactions'.

 Observe the issue where an additional HR case creation form appears.

</td></tr><tr><td>

UX Framework

 PRB1884471

</td><td>

Incorrect page variant is displayed when the variant audience is mapped to user criteria and glide.ux.user\_ criteria\_enabled=true

</td><td>

There is performance degradation between the two versions when the system property glide.ux.user\_ criteria\_enabled is to 'true'. The incorrect page variant is displayed when the variant audience is mapped to user criteria.

</td><td>

Scenario 1:

 1.  Open a Washington DC instance.
2.  Set glide.ux.user\_criteria\_enabled to 'true'.
3.  Navigate to a list in the Service Operations Workspace.
4.  Measure the page load times.

 Notice that the average page load time is less than 5 seconds.

 Scenario 2:

 1.  Open a Xanadu instance.
2.  Set glide.ux.user\_ criteria\_enabled to 'true'.
3.  Navigate to a list in the Service Operations Workspace.
4.  Measure the page load times.

 Scenario 3:

 1.  Create two page variants which have two respective audience records, which are mapped to two distinct user criteria.
2.  In the user criteria, use two different groups to map two different users.
3.  Open the SOW landing page.

 Expected behavior: The user should see the variant, 'Variant Landing Page Demo Level 2'. Actual behavior: The user should see the variant, 'Variant Landing Page Demo Level 1'.

</td></tr><tr><td>

UX Framework

 PRB1898329

</td><td>

Service Worker fails to cache shell-bundle.jsdbx which causes a blank page on the page load

</td><td>

The page that's loaded is blank, and an error message appears in the console. This issue occurs on Chronium browsers.

</td><td>

Log in to a Xanadu or Yokohama instance.

 Notice that the page loaded is blank, and in the console an error shows, 'Cannot cache the response UnknownError: Failed to execute 'put' on 'Cache'.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1891033

</td><td>

Marking the AI Agent/Agentic Workflows as 'Promoted' from Virtual Agent \(VA\) designer does not show up as a **Promoted** action in Virtual Agent

</td><td>

The user should be able to mark AI Agents/Agentic Workflows as 'Promoted' from VA Designer, but this doesn't appear as a **Promoted** action.

</td><td>

1.  Ensure all Agentic Workflow and Now Assist Virtual Agent plugins are updated on the instance.
2.  Navigate to **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.
3.  Select the tab 'Agentic Workflow' and select an base instance workflow.
4.  Mark the workflow as 'promoted'.
5.  Ensure the Agentic Workflow is active, visible and discoverable.
6.  Navigate to the esc portal.

 Notice that no promoted Agentic Workflow/AI Agents appear as a button \(promoted action\).

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1891079

</td><td>

Validate NLU discoverable topics retrieved from cache when domain separation is turned on

</td><td>

Provide a scriptable function vaSystem. getNLUDiscoverableTopics \(String languageCode\) that returns the names of the active and discoverable topics given a language code. If no languageCode is given, it uses the session language. If NLU is turned off on the instance or com.glide.cs.cach e.topic\_type.enabled is false, it should return an empty list and log why.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1821950

</td><td>

Now Assist Virtual Agent \(NAVA\) web client unread message appears on Natural Language Understanding \(NLU\) web client

</td><td>

Unread messages from the Employee Service Center \(ESC\) web client appear on the NLU web client in the Service Portal when it is open in another tab in the browser.

</td><td>

1.  Set up NAVA on an ESC portal.
2.  Keep open NLU AI Search in the Service Portal \(SP\).
3.  Open an ESC portal in one tab of the browser.
4.  Log in.
5.  Open SP in another tab.
6.  Open the ESC portal webclient.
7.  Start any LLM topic.
8.  Complete the topic flow.
9.  Wait for the summary card to appear.
10. Select **Submit**.
11. Open the SP tab.

 Notice that all the unread messages applicable only to the ESC web client appears on the NLU based web client.

</td></tr><tr><td>

Virtual Agent

 PRB1878360

 [KB2092161](https://hi.service-now.com/kb_view.do?sysparm_article=KB2092161)

</td><td>

'Show more' links are displayed, even for a topic which doesn't have any additional lines in an Edge browser

</td><td>

.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1880242

</td><td>

'interaction\_context' is overwritten with new conversation variables

</td><td>

When a requester is starting a conversation via sn\_va\_web\_client\_app with sysparm\_skip\_ load\_history=true and other parameters, the 'interaction\_context' takes the params as we'd expect. But if the requester has an ongoing chat, but starts a new conversation with different params, the initial chat's interaction\_context is overwritten with the new interaction\_context values.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881387

</td><td>

In Virtual Agent, dynamic translation isn't working when an agent sends a message to the end-user

</td><td>

 

</td><td>

1.  Provision an instance with Now Assist in Virtual Agent and the profanity filter for Agent Chat plugins installed on any Washington DC or Xanadu instances.
2.  Verify the record has the value 'OneExtend Profanity Filter' in the **Type document** field.
3.  Upgrade the instance to Yokohama.
4.  Verify that the **Type document** field has an empty value, due to which the dynamic translation is failing with below error: 'com.glide.oneapi.exception. OneApiRequestException: Error calling One API for feature Profanity Filtering : service invocation Id'.

 Expected behavior: For the profanity filter on the one\_api\_feature\_provider record, the **Type document** field shouldn't be empty.

 Actual behavior: For the profanity filter the one\_api\_feature\_provider record, the **Type document** field is empty.

</td></tr><tr><td>

Virtual Agent

 PRB1881393

</td><td>

An Agent Chat new message desktop notification should be clickable and redirect to the 'Calling' tab

</td><td>

When there's an agent in the workspace doing a live chat with a user, if users move the focus to another tab, with desktop notifications turned on, they receive a notification. The need is for the notification to be clickable and redirect to the 'Chat' tab.

</td><td>

1.  Navigate to an instance.
2.  Impersonate a system admin.
3.  Open Service Operations Workspace.
4.  Navigate to the inbox and set yourself to 'available'.
5.  Ensure that the desktop notifications are set up with the gear icon.
6.  Open an incognito window.
7.  Impersonate Beth Anglin.
8.  Open the Service Portal.
9.  Open the chat.
10. Ask for a live agent.
11. Wait for the connection with the agent.
12. From the system admin window, open a new tab and stay on that tab.
13. From the Beth window, send a message.

 Users should receive a desktop notification, but it's not clickable and doesn't redirect.

</td></tr><tr><td>

Virtual Agent

 PRB1896976

</td><td>

The 'Start a new conversation' pop-up box in Virtual Agent is out of the screen

</td><td>

In the instance, the padding is cut off, and the popover should be contained in the Web Client window.

</td><td>

1.  Navigate to Virtual Agent on an instance.
2.  Start a new conversation with the Now Assist' pop-up.

 Observe that when hovering over the **+** button, it's cut off on the right side.

</td></tr><tr><td>

Virtual Agent

 PRB1901626

</td><td>

'Notification' errors out if users trigger it for a user who has not had any interaction with Virtual Agent for more than 60 days

</td><td>

 

</td><td>

1.  Verify that the user doesn't have any interactions with web-client/channels for more than 60 days.
2.  Set up and trigger a non-actionable/actionable notification.

 Expected behavior: A new sys\_cs\_notification record should be created for the user.

 Actual behavior: There's an error in the notification log on the lines of 'sessionResponseV2Dto is null'.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1869054

</td><td>

Adding the ability to customize/update the default 'FAB' icon

</td><td>

The custom 'FAB' icon is configurable by defining this variable: $now-sp-nass-FAB-icon.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1881938

</td><td>

Boolean choice pickers aren't translated to the user's language in Dynamic Window

</td><td>

 

</td><td>

1.  Install a language.
2.  Switch the profile language to that language.
3.  Ensure that Dynamic Translation and Native Translation are turned on in Now Assist.
4.  Create a topic with the user input using the input selector.
5.  Navigate to Dynamic Window.
6.  Run the topic from step 4 until completion.

 Expected behavior: Boolean topic choice pickers are translated to the user's selected language \(Yes/No input\).

 Actual behavior: Boolean topic choice pickers are still in English \(Yes/No input\).

</td></tr><tr><td>

Work Order Management

 PRB1853297

</td><td>

Users are seeing an error message on a work order task whose state is '&gt;= Assigned' in the CSM Portal

</td><td>

An error message displays for querying the 'Map integration usage' table when getting a work order task as a user out of the scope of map integration ACLs.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1882671

</td><td>

Ignore sys\_user schedule when assigning tasks in the background

</td><td>

In the case where the 'com.snc.dynamic.scheduling. useWorkScheduleOnly' system property is true, the work schedule for an agent is absent. sys\_user.schedule isn't empty. Dynamic scheduling uses sys\_user.schedule to identify work blocks.

</td><td>

1.  Set 'com.snc.dynamic.scheduling. useWorkScheduleOnly' to true.
2.  Add sys\_user.schedule.
3.  Don't define any work schedule for an agent.

 Expected behavior: The task shouldn't assign to the agent. Check the DS log, and there should be no workblock for the agent.

 Actual behavior: The task could still assign to the agent. Check the DS log, there's a workblock based on sys\_user.schecdule for the agent.

</td></tr><tr><td>

Work Order Management

 PRB1889505

</td><td>

A fix script isn't executed while upgrading

</td><td>

A fix script isn't executed when upgrading from Washington DC to Yokohama.

</td><td>

1.  Create an instance in Washington DC
2.  Upgrade the instance from Washington DC to Yokohama.
3.  Check for the logs for execution of fix script: sys\_script\_fix\_ 6e154ec7c3d13010 a0cd587c1f40ddd1

 Expected behavior: The sys\_script\_fix\_ 6e154ec7c3d13010 a0cd587c1f40ddd1 must be executed.

 Actual behavior: The sys\_script\_fix\_ 6e154ec7c3d13010 a0cd587c1f40ddd1 isn't executed.

</td></tr><tr><td>

Work Order Management

 PRB1890343

</td><td>

In the CSM portal, the user is unable to see the Worker Order Task \(WOT\) details in the fsm\_ticket page

</td><td>

The WOT details aren't displayed and an error message on the **wm\_task.parent** field appears.

</td><td>

1.  Create a Work Order \(WO\) with a user as a contact.
2.  Select **Ready for qualification**.

Notice that the WOT gets created for the WO in the RL.

3.  Impersonate the user set as the contact in the WO.
4.  Access the CSM portal.
5.  Select the WO from the Work Orders list.

 Expected behavior: The user should be able to see the WOT details on WO page.

 Actual behavior: The WOT details aren't displayed and a query\_match error message on the **wm\_task.parent** field is appearing.

</td></tr><tr><td>

Work Order Management

 PRB1893187

</td><td>

The location contributor staff lost access to the work order tasks associated to the work orders on the portal

</td><td>

Error message: 'org.openqa. selenium. TimeoutException: Expected condition failed: waiting for visibility of element located by By.xpath: //\*\[@id="related-wot"\]//table/tbody/tr/td\[1\]/a \(tried for 20 second\(s\) with 500 milliseconds interval\)'.

</td><td>

1.  Log in with the location contributor associated with a location having work order tasks associated with work orders.
2.  Navigate to the cases associated to the work order on the BLSP Portal.
3.  Select work orders RL.
4.  Select the work order task.

 Expected behavior: The user should get access to the work order tasks.

 Actual behavior: The user is getting a query\_range error.

</td></tr><tr><td>

Work Order Management

 PRB1895750

</td><td>

A work order task template doesn't display the skill associated/linked to it

</td><td>

Users aren't able to associate the task skills with levels to a work order task template and display the value to the UI. Also, the **Task skills** field isn't available from the field picker of the work order task template, even though the form layout includes the field.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1895909

</td><td>

Add the mktplace\_requestor role for wm\_task.parent

</td><td>

 

</td><td>

1.  Log in with the location contributor associated with a location, and having work order tasks associated with work orders.
2.  Navigate to the cases associated with the work order on the BLSP portal.
3.  Select **work orders RL**.
4.  Select **work order task**.

 Expected behavior: The user should get access to the work order tasks.

 Actual behavior: The user is getting a query\_range error.

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB1877371

</td><td>

An established connection with the state 'Needs Configuration' throws an exception on the 'Connection details' tab

</td><td>

Error: 'Data Fabric Hub: Unable to retrieve connection fields. Error: Connection details not found, connection ID...'.

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB1879783

</td><td>

Move muninn controller sys\_service endpoints to data-fabric-connector-metadata project

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB1888130

</td><td>

A reservation request in Glide should send whether an instance is a production instance or not

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB1900907

</td><td>

Requests using shortname URLs for a controller don't get routed

</td><td>

This may be caused by the HTTP Client not setting the SNI.

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB1906629

</td><td>

Scope name change for the 'Connectors metadata' app

</td><td>

The previous scope name is 'sn\_data\_fabric \_connector\_metadata'. The new one is 'sn\_data\_fabric\_zcc'. With the previous scope name, users get an error: 'Encountered an error on Technology Partner Portal: Scope name should be max 18 characters'.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3 Hotfix 3](yokohama-patch-3-hf-3-PO.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2 Hotfix 3](yokohama-patch-2-hf-3-PO.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


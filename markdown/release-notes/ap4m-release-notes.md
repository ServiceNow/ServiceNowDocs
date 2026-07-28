---
title: Australia Patch 4m
description: The Australia Patch 4m release contains important problem fixes via Australia Patch 4 and updates to compatible ServiceNow Store applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/ap4m-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-07-27"
reading_time_minutes: 324
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 4m

The Australia Patch 4m release contains important problem fixes via Australia Patch 4 and updates to compatible ServiceNow Store applications.

-   **Australia Patch 4m was released on July 23, 2026.**
    -   Build date: 07-22-2026\_0427
    -   Build tag: glide-australia-02-11-2026\_\_patch4m-07-09-2026

## Monthly "m" releases

Monthly "m" releases are now available for your ServiceNow AI Platform® instances. These releases, which are identified by an "m" in the release name, contain everything from the base family patches, the latest version of all AI applications, and those apps' supporting non-AI application dependencies.

**Important:** This ServiceNow® release is not available for ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in the Australia Patch 4 release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A04.00.xlsx).

## Overview

Australia Patch 4 includes 420 problem fixes in various categories.

\[Omitted image "prb-chart-ap4.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Australia Patch 4 includes fixes for security-related problems that affected certain ServiceNow applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 4m, refer to [KB3141166](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3141166).

## Changes in Australia Patch 4m

See the following Now Support Knowledge Base articles for more information about upgrading to Australia Patch 4m:

-   [KB3140377](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3140377)
-   [KB3141683](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3141683)
-   [KB3141830](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3141830)

-   ****

    Archive, clear, or delete related records when an archive rule runs.

-   ****

    Define a rule for archiving records.

-   ****

    Define a rule for deleting records from a primary table on a recurring basis.

-   ****

    Define a rule for deleting records now or at a later date.

-   ****

    Define one or more conditions that identify the records to be archived.

-   ****

    Define one or more conditions that identify the records to be deleted.

-   ****

    Define one or more conditions that identify the records to be deleted.

-   ****

    Delete archived records after a specified amount of time by configuring optional destroy rule conditions.

-   ****

    Delete older, expired, or unwanted records from tables automatically.

-   ****

    Encryption at rest for Hermes topics protects message data stored on broker disks from unauthorized access. Hermes supports both ServiceNow-managed keys and keys you provide using the Bring Your Own Key \(BYOK\) model.

-   **[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md)**

    For Now Assist new features and changes, see [Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-assist-rn-landing.md).

-   **[Properties for Identification and Reconciliation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/properties-id-reconciliation.md)**

    glide.identification\_engine.non\_dependency\_relation.duplicate\_detection

    Set IRE behavior when the payload contains duplicate non-dependent relationships \(identical parent/child relationship type\).

    When set to **true**, IRE detects duplicate non-dependent relationships in a payload.

    When set to **false**, IRE doesn't detect duplicate non-dependent relationships in a payload.

    -   Type: true \| false
    -   Default: false
    -   Learn more: 
    -   Location: [Add to System Properties \[sys\_properties\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md) table.
-   ****

    Manage table size growth and improve query performance by archiving records.

-   ****

    Manage the growth and storage of data on your instance by creating data management rules in the Data Management Console.

-   ****

    Restore one or more archive records and any related records back into the primary table.

-   ****

    Safely delete records from a table without using scripts and without deleting the table by creating one-time delete rules.

-   ****

    Schedule a date and time to execute a one-time delete rule or execute it after you finish creating it.

-   ****

    Specify which associated records to delete when the cleanup rule runs.

-   ****

    Specify which associated records to delete when the one-time delete rule runs.

-   ****

    View a summary of your archive rule and decide whether to activate it.

-   ****

    View a summary of your cleanup rule and decide whether to activate it.

-   ****

    View a summary of your one-time delete rule and acknowledge the deletion.


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

Next Experience Unified Navigation

 PRB2015985

 [KB3018348](https://hi.service-now.com/kb_view.do?sysparm_article=KB3018348)

</td><td>

Tags on task records don't conform to background color hex codes after a Zurich upgrade

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2014857

</td><td>

Navigation to home.do doesn't redirect to the last visited CoreUI dashboard

</td><td>

An empty 'com.​snc.​par.​dashboards.​ui.​preferences' user preference causes erroneous redirection to the CoreUI dashboard.

</td><td>

1.  Have the 'com.​glide.​par.​unified\_​analytics.​enabled' system property set to true.
2.  Create a user with the dashboard\_admin role.
3.  Create a CoreUI dashboard.
4.  Share it with the created user.
5.  Impersonate the user.
6.  Open the shared CoreUI dashboard.

This should create a user preference record: 'com.​snc.​pa.​ui.​preferences\_​dashboards',​ storing the sys\_id of the last visited CoreUI dashboard.

7.  Navigate to: /nav\_to.do?uri=%2Fhome.do%3F.

 Expected behavior: The user is redirected to the last visited CoreUI dashboard.

 Actual behavior: The user is redirected to the Platform Analytics dashboard overview page.

</td></tr><tr><td>

Server-side scripts

 PRB1994381

 [KB3006010](https://hi.service-now.com/kb_view.do?sysparm_article=KB3006010)

</td><td>

Discovery node issues after upgrading to Australia

</td><td>

After upgrading to Australia, JavaScript that is running in app nodes fails to call Java functions. The following warning appears: '\*\*\* WARNING \*\*\* Evaluator: com.​glide.​script.​Rhino​Ecma​Error:​ undefined is not a function.' This impacts various features, including Discovery and Event Management.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Events

 PRB2003217

</td><td>

Fix behavior of event processing tables during the clone operation and clean up invalid records/jobs during the clean up script

</td><td>

During cloning on Zurich instances, events processing framework tables' configurations aren't preserved, causing errors in transaction logs due to orphan records for events jobs. An orphan record occurs when a sys\_trigger record exists for an event processing job, but the corresponding entry in the sys\_processing\_framework\_job table is missing. This causes the ProcessingFrameworkJob to fail when attempting to retrieve the scheduled job context. Log example: 'ProcessingFrameworkJob SEVERE ProcessingFramework &gt; Failed to get the schedule job context'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2007255

 [KB3045151](https://hi.service-now.com/kb_view.do?sysparm_article=KB3045151)

</td><td>

There is memory pressure on nodes due to high memory for the cache 'com.​glide.​cs.​qlue.​module.​coma.​Message​Batching​Session'

</td><td>

Users with 2GB nodes may encounter memory issues that can cause the events process jobs to yield.

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

 PRB2003313

</td><td>

The @mention in the journal input does not appropriately respond to assistive technologies in workspaces

</td><td>

When using '@' in the **Comments** field to invoke the list for user selection, the screen reader does not identify it.

</td><td>

1.  Create an account on Assistiv Labs to use NVDA and JAWS.
2.  Open a base instance.
3.  Navigate to a workspace such as Service Operations Workspace \(SOW\).
4.  Open any incident.
5.  Open a screen reader, such as VoiceOver and Safari or JAWS/NVDA and Chrome.
6.  Navigate to the **Comments** field.
7.  Enter '@' and a character or two for a user to invoke the drop-down list for user selection.

 Notice that neither screen reader identifies the pop-up, nor is there any identification of the members of the list as the user navigates it.

</td></tr><tr><td>

Activity Stream

 PRB2010203

</td><td>

SysUserRepo should add setWorkflow\(false\) when querying the sys\_user table

</td><td>

 

</td><td>

1.  Add a before business rule query rule to the sys\_user table where 'active=true'.
2.  Impersonate the user, Abraham Lincoln.
3.  Create a work note/comment from Abraham.
4.  End the impersonation.
5.  Mark Abraham as 'inactive'.
6.  Flush the Activity stream's user cache.
7.  Reload the Activity stream with Abraham's comment.

 Notice that the author is now Abraham's username.

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

 PRB2022330

</td><td>

Custom **journal\_input** field values are not displayed on Service Portal Ticket Conversational widget after Australia upgrade

</td><td>

After the Australia Upgrade, custom journal\_input field values added to records are not displayed on the Service Portal Ticket Conversational widget.

</td><td>

1.  Create a custom **Comment** Field , Type - journal\_input.
2.  Make sure the user does not have read access to other base instance journal fields \(comments/work\_notes\).
3.  Navigate to any incident, open any record.
4.  Add some comments in the **journal\_input** field.
5.  Navigate to the service portal.
6.  Impersonate any non-admin user.

 Observe that comments are not visible.

</td></tr><tr><td>

Activity Stream

 PRB2029963

</td><td>

The **Copy** button for Journal entries does not work in List Activity Stream view

</td><td>

Content does not get copied to the clipboard and subsequently cannot get pasted.

</td><td>

1.  Navigate to /incident\_list.do.
2.  Select the **Show activity stream in a flyout window** button \(heartbeat icon at the top-right of the table\).
3.  Find a journal tile in the activity stream, and select the **Copy journal content** button.
4.  Try pasting the copied content anywhere.

 Expected behavior: The content should get copied to the clipboard, and a notification saying, 'Copied to clipboard' should appear.

 Actual behavior: The content does not get copied to the clipboard and subsequently cannot get pasted.

</td></tr><tr><td>

Activity Stream

 PRB2033885

</td><td>

A new activity comment has the type as 'Field changes' instead of 'Comments'

</td><td>

 

</td><td>

1.  Open any incident in UI16.
2.  Post a comment.

 Note that the comment type \(top right of tile\) is 'Field changes \[dot timestamp\]' instead of 'Comments \[dot timestamp\]'.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1996219

</td><td>

The END\_WRAP\_UP event is published twice when wrap-up is timed out

</td><td>

This behavior causes 'openframe\_wrap\_up\_submitted' to trigger twice, which isn't expected while users are using OpenFrame to handle wrap up with external systems.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB2007529

</td><td>

Alert audio continues playing after rejecting a work item

</td><td>

When an audio with a length of two minutes is mapped with Genesys and a call is initiated from an 'Available' agent, the call the audio continues to play after the user ends the call.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB2010201

</td><td>

The script action 'Set logged out agent offline' creates an offline Advanced Work Assignment \(AWA\) presence record for non-agent users

</td><td>

The script action will insert records to awa\_agent\_presence and awa\_agent\_channel\_availability when a user without awa\_agent role logs out.

</td><td>

1.  Log in to the latest Zurich instance.
2.  Impersonate a user without the awa\_agent role.
3.  Log out.
4.  Check awa\_agent\_presence and awa\_​agent\_​channel\_​availability.​

 Notice that a record associated with the impersonated user was inserted.

</td></tr><tr><td>

Advanced Work Assignment

 PRB2025053

</td><td>

Missing validation allows AWA queue save with floating schedule

</td><td>

The queue is successfully saved even when the schedule has Timezone = Floating.

</td><td>

Navigate to **AWA** &gt; **Queues**.

 Open an existing queue or create a new AWA Queue.

 In the **Schedule** field, select a schedule configured with Timezone = Floating.

 Select **Save**.

 Expected behavior: System should prevent saving the queue when the selected schedule has Timezone = Floating or show a validation error/warning indicating that floating schedules are not supported for AWA queues.

 Actual behavior: The queue is successfully saved even when the schedule has Timezone = Floating.

</td></tr><tr><td>

Advanced Work Assignment

 PRB2026914

</td><td>

Duplicate work items when the service channel's work\_item\_table is a parent class of the routed record

</td><td>

Duplicate work items are created.

</td><td>

1.  Configure service channel against the parent table \(task\).
2.  In service channel condition, the user can restrict the task type to only incident \(optional\).
3.  Have a live agent online with good capacity \(&gt;500\).
4.  Make sure auto acceptance is on.
5.  Create 200 incidents together via BG script.

 Expected behavior: 200 work items created.

 Actual behavior: 200+ work items created \(have duplicates\).

</td></tr><tr><td>

Advanced Work Assignment

 PRB2033767

</td><td>

Enhanced updateSegment API \(Wrap-up\) to support Agent Initiated Wrap-up

</td><td>

When CCaaS sends updateSegment with only configuration \(no wrapUpCode, notes, or confirmedOn\), the backend treats it as a full submission and closes the segment. The correct behavior is to update the wrap-up configuration reference on the open segment and return without closing it.

</td><td>

1.  Create an active phone interaction with an assigned agent.
2.  Create a wrap-up segment via createSegment \(external=true\).
3.  Call updateSegment with only configuration: \{ duration: '120', show\_timer: true \} — no wrap\_up\_code, notes, or confirmed\_on.
4.  Notice the segment state in interaction\_wrap\_up\_segment.

 Expected behavior: Agent should be able to submit the wrap upSegment.

 Actual behavior: Agent is not able to submit the wrap up.

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

 PRB2030144

</td><td>

In the workspace, when a work item is in the queue but not yet accepted, the user is unable to update string fields on the open record

</td><td>

In the workspace, when a work item is in the queue but not yet accepted, the user is unable to update string fields on the open record. With these two circumstances satisfied, a focus-stealing issue removing the blinking cursor after a moment begins to occur.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2033778

</td><td>

Dynamic wrap-up timer update on UI when call ended

</td><td>

Wrap-up dialog does not close in other tabs when submitted in one tab. The timer does not reset on config refresh.

</td><td>

1.  Open the same active phone interaction in two browser tabs \(Tab A and Tab B\).
2.  Wait for the wrap-up dialog to appear in both tabs.
3.  Submit wrap-up in Tab A \(fill in notes/code and select **Submit**\).
4.  Observe Tab B.

 Expected behavior: Wrap-up dialog in Tab B closes automatically.

 Actual behavior: Tab B continues showing the open wrap-up dialog.

</td></tr><tr><td>

Agent Chat

 PRB2033973

</td><td>

Agents can close audio warning pop-ups without changing browser settings

</td><td>

If the agent's browser Audio/Sound settings are set to 'Automatic\(default\) in chrome' and 'Automatic' in Edge, they observe an 'Audio Warning' pop-up reading as follows: 'Browser settings may block notifications in some cases. To avoid missing alerts in the future, please verify notifications are working for your browser.'.

</td><td>

1.  Have agent chat installed.
2.  On a browser session, impersonate an agent and open SOW workspace.

 Notice the 'Audio Warning' pop-up.

 Observe that the agent can close the 'Audio Warning' pop-up and continue to work without changing the intended settings.

</td></tr><tr><td>

Agent Chat

 PRB2033982

</td><td>

Duplicate entries in ui\_notification\_inbox for workspace notifications when agent has multiple subscriptions

</td><td>

Multiple entries are created in ui\_notification\_inbox table.

</td><td>

1.  In Agent Chat, set sys\_prop 'glide.​awa.​work\_​item.​notifications.​enabled' to true.
2.  On one browser session, impersonate an agent and open SOW workspace.
3.  Set workspace notifications to True from the settings gear icon next to presence state.
4.  Duplicate the workspace tab to open two workspace tabs.
5.  In another session, as Abel Tuter, initiate a live agent conversation from ESC.

 Expected behavior: Only one entry should be created in ui\_notification\_inbox table for workspace notification.

 Actual behavior: Multiple entries are created in ui\_notification\_inbox table.

</td></tr><tr><td>

Agent Chat

 PRB2034807

</td><td>

UXF changes for inbox DOM

</td><td>

Assist UXF with the changes being implemented to remove inbox from the DOM when navigating away from workspace.

</td><td>

1.  Open ServiceNow Workspace with Agent Inbox loaded.
2.  Navigate away from the workspace to another page/module.
3.  Inspect the DOM.

 Observe that the inbox component remains in the DOM instead of being removed on navigation.

</td></tr><tr><td>

Agent Chat

 PRB2050363

</td><td>

Incorrect and inconsistent heading hierarchy in ServiceNow flow

</td><td>

Users who rely on screen readers to navigate via headings are unable to get an overview of the Inbox section. The lack of a clear hierarchy makes the content feel disconnected from the rest of the page, leading to confusion and increased cognitive load when trying to locate specific information.

</td><td>

1.  Open the SOW home page.
2.  Navigate to the Inbox section using the tab key.
3.  Enable VoiceOver on macOS and use the rotor or heading shortcut to navigate.

Observe that it only identifies H4 and H5.

4.  Enable ChromeVox on ChromeOS and try to navigate by heading using the 'H' key.

 Observe that ChromeVox fails to identify any headings in this section.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2025221

</td><td>

Cache service intermittently fails and gets calls across different keys

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2025859

</td><td>

The Off​Glide​Script​Object.​generate​Authorization​Info API creates JSON Web Tokens \(JWT\) with current session users

</td><td>

The API sn\_​cs\_​offglide.​Off​Glide​Script​Object.​generate​Authorization​Info\(\)​ creates JWT with current user sessions, even though the userID value is passed in the request.

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

AI Agents \(Glide Family\)

 PRB2030410

</td><td>

An instance isn't invoking DARE calls due to new properties not being allow-listed in the cache configuration's invalidation script

</td><td>

 

</td><td>

1.  Turn on the DARE sysprop.
2.  Open Now Assist Portal.
3.  Run the utterance 'List my incidents'.

 Expected behavior: The response should be received from DARE.

 Actual behavior: The response is coming from NextWave.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2030948

</td><td>

Tools using data stream actions aren't able to retrieve data in NAVA

</td><td>

 

</td><td>

1.  Log in to an instance with user credentials.
2.  In Service Portal, give the utterance, such as 'using smartsheet agents, look up groups stream'.

 Observe that the tool isn't able to retrieve data.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2032030

</td><td>

Add impersonate role to NextWave Service User and append cache/ to offglide service path

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2033732

</td><td>

Whenever the batch set script execution is failing on Glide, it's surfaced as a success to the central cache

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2034452

</td><td>

Batch Set Glide Script execution failure is surfaced as success to central cache

</td><td>

Whenever the Set Script execution fails on glide, it is surfaced as success to central cache.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2039170

</td><td>

Evict the cache client for cache invalidation after TTL expiry

</td><td>

Add Impersonate role to NextWave Service User to impersonate the actual call for glide backed set operations.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2015095

</td><td>

Changes for rich\_control\_type are not invalidating sys\_ux\_widget used by the agent orchestrator \(AO\)

</td><td>

Modifying the sys\_ux\_widget or any of its extension tables should invalidate the sys\_ux\_widget cache, otherwise a duplicate cache configuration will have to be created for each child table.

</td><td>

1.  Open an instance.
2.  Use the chat for Now Assist panel \(NAP\) or Janus.
3.  Enter, 'Show me a date time widget'.
4.  Select an agent in the list of agents.

Observe that the DateTimeSelect widget rendered does not contain the latest changes from the rich\_control\_type record.


 Expected behavior: Editing the rich\_control\_type record should change the widget rendered in the chat client.

 Actual behavior: The rich\_control\_type widget is pulled from a stale cache.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2024769

</td><td>

Chat gate service uses a GlideRecord query with ACL evaluation, blocking non-admin users from reading the 'Deployment channel' table

</td><td>

In chat-gate-service.js \(line 13\), the chatEnabled check uses glideRecord\_query to query the 'Deployment channel' table. This evaluates all ACLs for the current user, so only admin users have the necessary read access to that table. Non-admin users are blocked from fetching chatEnabled, which prevents the chat from functioning for them.

</td><td>

1.  Log in as a non-admin user.
2.  Navigate to an AI Control Tower \(AICT\) page where the chat is expected to load.

Observe that the chat doesn't initialize because chatEnabled can't be fetched.

3.  Log in as an admin user and repeat.

The chat works correctly.


 Expected behavior: ChatEnabled is fetched successfully regardless of the user role.

 Actual behavior: GlideRecord\_query evaluates ACLs and denies non-admin users read access to the deployment channel table.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2027770

</td><td>

Remove the 'Applicability' table \(sys\_aix\_applicability\) and move the fields **Applicable for** and **Not applicable for** glide\_list \(user\_criteria\) into a multi-theme table

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2030274

</td><td>

Users without elevated privileges cannot query widgets that are category=internal

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2036766

</td><td>

Experience cache population only emits the default theme

</td><td>

Multi-theme \(user-criteria\) themes are missing from the edge cache, so targeted users get the wrong theme.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2039292

</td><td>

Move component and source\_browser\_code fields from sys\_ux\_widget to sys\_aix\_widget dictionary

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1976935

</td><td>

The user context's country in search request is a displayed value instead of an internal value

</td><td>

This is because the **Country** field in user context uses Display Value instead of the actual Internal Value.

</td><td>

1.  Navigate to sys\_user, search for User ID = abel.tuter, and open the record.
2.  Update **Country Code \(country\)** field to 'United States'.
3.  Open ESC Default Search Profile and create a new RIR.
    1.  Trigger: User Context - Country \(sys\_user.country\) is United States.
    2.  Set the appropriate Start and End Date so the RIR is valid.
    3.  Select the **Promote Document** action and promote Apple Watch \(sc\_cat\_item\).
    4.  Save and Republish the search profile.
4.  Open Search Preview, search 'spam' with the matching search application \(base instance is ESC Default Search App\) and user Abel Tuter.

 Expected behavior: 'Apple Watch' is promoted and can be seen in result list.

 Actual behavior: 'Apple Watch' is not promoted. Under 'Summary' tab, RIR is not applied.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2020989

</td><td>

Performance and EVAM-related debug messages no longer appear in sys log for async GRs and Virtual Agent searches

</td><td>

When the system properties 'glide.​search.​performance.​logger.​enabled' or 'glide.​search.​evam.​logger.​enabled' are set to true, messages should appear in the sys log prefaced with '\[SEARCH PERFORMANCE\]' or '\[SEARCH EVAM\]' respectively. However, these messages no longe appear in the syslog when a conversation is part of the logging context.

</td><td>

1.  On an instance that returned synth response in portal \(for example, Dynamic Window setup\):
2.  Create and set glide.​search.​evam.​logger.​enabled to true.
3.  Perform a search that returns a synthesized response in portal.
4.  Open the sys log and search for recent messages containing 'for Genius Result with table'.

 Expected behavior: Log entry in sys log specifying the ID of the view config that was used for each genius result.

 Actual behavior: No log entries for GR EVAM View Config selection.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2028353

</td><td>

Deprecate 'ServiceNow RAG \(Deprecated\)' resource options from NASK Tool UI drop-down list

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2035235

</td><td>

Glide changes required for expanding MC-synthesized responses to other indexed sources

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1787984

</td><td>

The search preview has the Service Portal Entity View Action Mapper \(EVAM\) configuration hardcoded

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1991431

</td><td>

The right-hand side panel in Zing search is not scrollable

</td><td>

The user cannot reach for sources below the screen height because the panel is not scrollable.

</td><td>

1.  Find an instance with zing search enabled.
2.  Search for a term that returns results from many sources.
3.  Attempt to reach for sources available below the screen height.

 Expected behavior: The panel is scrollable and sources are reachable.

 Actual behavior: The right-hand side panel is not scrollable and the sources are not reachable.

</td></tr><tr><td>

AI Search UX

 PRB1998976

</td><td>

Search event records don't indicate the search mode \(keyword, hybrid, or semantic\)

</td><td>

When a search is executed in an AIS-enabled portal with Hybrid Search enabled on the corresponding search application, the resulting sys\_search\_event and sys\_search\_signal\_event records don't capture the search mode \(keyword, hybrid, or semantic\) that was used to execute the query. This makes it impossible to distinguish query types in search analytics and signal data.

</td><td>

1.  Turn on Hybrid Search on a Search Autocomplete Configuration \(SAC\).
2.  Navigate to a Dynamic Window-enabled portal that uses the configured SAC.
3.  Perform a search in the portal.
4.  Open the corresponding sys\_search\_event and sys\_search\_signal\_event records generated by the query.

 Observe that neither record contains any field or indicator specifying the search mode used \(keyword, hybrid, or semantic\).

</td></tr><tr><td>

AI Search UX

 PRB2026614

</td><td>

Auto-Enable Hybrid Search on Now Assist for Search Installation

</td><td>

When a new users installs the 'Now Assist for Search' plugin, the system should automatically enable Hybrid Search for all search applications configured in the instance. This ensures new users benefit from Hybrid Search by default without requiring manual configuration. The behavior applies to all new user installations going forward and shouldn't retroactively affect existing users who have already installed Now Assist for Search.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2031624

</td><td>

Enhanced Chat's search bar appears on portals with NextWave

</td><td>

Note that the NextWave omni-bar displays on the homepage as expected. However, the search bar from Enhanced Chat is also appearing on other pages unexpectedly.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2038703

</td><td>

Instance creation failure for com.​glide.​search.​graphql.​query.​Suggestions from service portal's typeahead AIS Suggestions API

</td><td>

When soemthing is searched for in the portal's typeahead, no suggestions appear and AIS Suggestions API calls in the network tab return 'Instance creation failure for: com.​glide.​search.​graphql.​query.​Suggestions',​ and 'DataFetchException'.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2039564

</td><td>

Error while accessing catalog items from search after Australia upgrade

</td><td>

After upgrading to Australia, the typeahead widget for suggested results fails.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1974037

</td><td>

Visualization displays outdated dates when 'Use current date for period end' is selected

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

 PRB2030053

</td><td>

Add a feature flag for auto cache of PA indicators

</td><td>

Indicators are cached automatically, leading to data discrepancies between different users.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2050449

</td><td>

Next Experience Widgets load with an 'Unable to generate chart' error

</td><td>

The error reads: 'Error Unable to generate chart. Cannot invoke 'com.glide.glideobject.GlideDateTime.after\(com.glide.glideobject.GlideDateTime\)' because 'scoresModifiedAt' is null.'

</td><td>

 

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

 PRB2019161

</td><td>

The export option is not working for sub domain dashboards

</td><td>

This issue was also observed in Australia. An error occurs when attempting to export the dashboard, and an error also occurs in the logs.

</td><td>

1.  Open an instance.
2.  Navigate to **Platform Analytics** &gt; **Dashboards**.
3.  Create a new inline dashboard.
4.  Select **Add component**.
5.  Select **Data visualization**.
6.  Select any visualization type, such as column or bar, and configure it to show the visualizations.
7.  Navigate back to the dashboard created.
8.  Select **Export** on the dashboard.
9.  Select **Export to PowerPoint or PDF** .

 Notice the error, 'Export failed. Please contact your system administrator.' There is also an error is displayed in the error logs, 'ExportJobExecutor \*\*\* ERROR \*\*\* EXPORT\_JOB\_EXECUTOR: PEJ0001007 AttachmentID is null, attachment was not saved properly.'.

</td></tr><tr><td>

Application Manager

 PRB2020279

</td><td>

Users can't uninstall the 'Universal Request' application

</td><td>

After installing the 'Universal Request' plugin, it isn't possible to uninstall it. There is a message stating that it can't be uninstalled because of the dependent plugin 'Universal Request: Reporting'. When attempting to uninstall 'Universal Request: Reporting', we are not able to because 'Universal Request' needs to be uninstalled first: 'This application cannot be uninstalled because one or more applications are dependent on it. In order to uninstall this application, please uninstall the below dependent applications first'.

</td><td>

1.  Provision an instance with the 'Universal Request' plugin installed.
2.  Navigate to the record on sys\_store\_app.
3.  Attempt to uninstall.

 See that it isn't possible.

</td></tr><tr><td>

Application Manager

 PRB2057729

 [KB3140027](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3140027)

</td><td>

Users can't publish custom-scoped applications after upgrading to Zurich or Australia

</td><td>

After upgrading to Zurich or Australia, users can't publish new application versions to scoped apps. Selecting the 'Publish' button on any custom applications in ServiceNow studio results in a pop-up with the error 'Alert level: Critical. Vendor information was not found, upload function is disabled for this instance'.

</td><td>

Refer to the listed KB article for details.

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

 PRB2035326

</td><td>

Enable an audit to clearly attribute every field level data change to either a human user or an AI capability

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2026060

</td><td>

The kba\_session\_context value is not in JSON format

</td><td>

The kba\_session\_context value is logged in this format: '\{q1\_keyword=q1\_user\_input, q2\_keyword=q2\_user\_input\}'.

</td><td>

1.  Create three scriptable authentication type answers.
2.  Attach them to three different questions.
3.  Log kba\_session\_context in these three answers, along with kba\_auth\_result=true.
4.  Navigate to a voice deployment.
5.  Select the three questions as a KBA auth factor.
6.  Call the voice agent.
7.  Authenticate a user.
8.  Navigate to the syslog table.

 Observe that the kba\_session\_context value for the third question is logged in this format: '\{q1\_keyword=q1\_user\_input, q2\_keyword=q2\_user\_input\}'. It should be logged in a standard json format.

</td></tr><tr><td>

Authentication Factors

 PRB2030597

</td><td>

Fall back to secondary identification when the primary resolves a non-sys\_user

</td><td>

In cases when the identification questions are configured to a non-sys user, then it should ask fallback questions. This isn't happening in v2 and the call is ended since the userID isn't resolved. It should fallback to the secondary identification to get the userID. In cases where both the questions lead to a non-sys\_user, then it should fail.

</td><td>

1.  Log in to the instance.
2.  Navigate to **All** &gt; **Authentication Factors** &gt; **Knowledge Based Factor** &gt; **Questions**.
3.  Select any question with the type, 'Identification/​Authentication'.​
4.  For the question, create service mapping with the type set to 'Authentication'.
5.  Return to the selected question.
6.  Update the type to 'Identification only'

 Expected behavior: 'Identification' should not be allowed because the question is mapped to service an 'Authentication' question, which creates inconsistency.

 Actual behavior: The operation is successful.

</td></tr><tr><td>

Authentication Factors

 PRB2037631

</td><td>

Identification Retry does not occur after plugin upgrade

</td><td>

If the identification step fails \(first PIN entry is incorrect\), the voice agent directly transfers to live agent which is the fallback on the assistant. It doesn't ask the user to re-enter the identification PIN again.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB2009727

</td><td>

A base instance doesn't have the tokenbased\_auth plugin

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB2033124

</td><td>

Case-sensitive comparison is applied during knowledge-based authentication \(KBA\) answer matching

</td><td>

Case sensitiveness of KBA answer matching is controlled by the system property 'glide.auth\_factors. kba.case\_insensitive \_validation'. It is by default case insensitive in previous patches, but seems to have the incorrect default value in recent tracks.

</td><td>

1.  Set up knowledge\_based\_answer for a KBA Service.
2.  As an end user, try to pass answers and validate identification/authentication.

 Expected behavior: The user-given input should be matched case insensitively.

 Actual behavior: Answers are matched case sensitively.

</td></tr><tr><td>

Authentication

 PRB2037225

</td><td>

Third-party access token authentication fails

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2031396

</td><td>

ATF tests fail when code coverage is enabled due to onChange client scripts in a scoped app failing to execute

</td><td>

The onChange client script in the scoped app does not execute.

</td><td>

1.  Navigate to **Automated Test Framework \(ATF\)** &gt; **Tests**.
2.  In the list filter, search for the test named **Scoped coverage test** and select it to open the test record.
3.  Select **Run Test**, choose a browser or open a new one, and select **Run Test** again.
4.  Let the test run to completion, then navigate back to the test.

 Expected behavior: The test runs to completion, and the status reads 'Success'.

 Actual behavior: The test fails. The onChange client script in the scoped app does not execute, and the following client error is reported: 'Script: MyScriptInclude not found in scope: global, and HTTP Processor class not found: com.​glide.​processors.​xmlhttp.​My​Script​Include:​ no thrown error'.

</td></tr><tr><td>

Cache

 PRB2001257

</td><td>

Tiered Caching Journal files are deleted by a file maintenance scheduled job leading to resurrection failures for tiered caching

</td><td>

syscache\_realform entries fail to be resurrected from the tiered\_cache\_journal.dat file because the file has been deleted.

</td><td>

1.  Modify the sys\_trigger: sys\_​trigger\_​c10d485e0a0a0b170060611b99ccd00c.​xml \(Clean Temp Files\) to call the FileMaintenance.cleanTempDir API with the current node name as a prefix \(the first argument in the API call\).
2.  Ensure that entries have been serialized to the journal files by navigating to any list form, closing it, and waiting to create and serialize a syscache\_realform entry.
3.  Find the location of the journal files for the node and run: touch -mt YYYYMMDDhhmm \(replacing the date format with a timestamp at least a day in the past\).
4.  Run the scheduled job: Clean Temp Files \(sys\_​trigger\_​c10d485e0a0a0b170060611b99ccd00c.​xml\)​.​

 Observe that the tiered caching journal file is deleted.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2015442

</td><td>

Semantic configuration for HR case indexed sources are in the wrong path

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2018011

</td><td>

Multiple requested RCAs from Employee Slate Core targeting 'Human Resources: Core' about the script include 'ActivityHubUtilSNC'

</td><td>

When selecting a widget, an RCA error is thrown.

</td><td>

1.  Open the instance.
2.  Impersonate as a user.
3.  Navigate to **/aiux/employeeslate/home**.
4.  Select a widgets, such as 'Our Company'.

 Notice that it throws the RCA error, 'Read operation on table 'sn\_hr\_core\_case\_operations' from scope 'Employee Slate Core' was denied. The application 'Human Resources: Core' must declare a Restricted Caller Access privilege. Please contact the application admin to update their access requests.'.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2024293

 [KB3031345](https://hi.service-now.com/kb_view.do?sysparm_article=KB3031345)

</td><td>

The HR ACL script hasHRApprovalAccess fails to resolve a source table for non-task approvals

</td><td>

This blocks HR agent read access on sysapproval\_approver records for KB articles in HR knowledge bases.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2027153

</td><td>

HR Templates not applying as expected from Flows

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2031869

</td><td>

Missing RCAs for HR ZTSD flow

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2026001

</td><td>

An AI-driven question and answer completer that populates both change risk assessments and dynamic schema questions with context-based, accurate answers

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2029102

</td><td>

Manual approvers can't be added to the change and std\_change\_proposal due to newly enforced ACLs for related lists

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB2023188

</td><td>

Signature verification triggers for records with no signature configuration defined

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB2033953

</td><td>

LES behavior for missing client transaction fields in the syslog\_transaction payload

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Communities

 PRB1487727

</td><td>

'Moderation Banned Keyword Filter' isn't working for keywords in other language

</td><td>

The user is allowed to post content with the banned keyword if the keyword is not in English.

</td><td>

1.  Provision an instance with the following plugins installed: customer communities, communities demo data, and I18N: Japanese Translations.
2.  As community admin, log in to the platform.
3.  Navigate to **Community** &gt; **Moderation** &gt; **Moderation filters**.
4.  Create a new moderation filer/use the existing filter.
5.  Add any Japanese keyword \(こんにちは\) in the filter.
6.  Add any English keyword \(hello\) in the filter.
7.  Save it.
8.  Log in to community portal as any community user1 with the preferred language set to Japanese.
9.  Try to post content with the keyword used in step 5.
10. Log in to community portal as any community user1 with the preferred language set to English.
11. Try to post content with the keyword used in step 6.

 Expected behavior: The user is prevented from using banned keywords during content posting. The appropriate message appears.

 Actual behavior: 'Moderation Banned Keyword Filter' doesn't work for characters in other languages. The user is allowed to post content with the banned keyword if the keyword is not in English.

</td></tr><tr><td>

Condition Builder in Workspace

 PRB2001225

</td><td>

The messaging for deleting saved filters is misleading

</td><td>

The confirmation dialog says 'Active will no longer be available in your saved filters. This action can't be undone.' Instead, it should be more explicit that the filter may be deleted for everyone.

</td><td>

1.  Navigate to a list in Service Operations Workspace.
2.  Open the condition builder.
3.  Add some filters to the condition builder.
4.  In the 'Saved Filters' list, select **Save Filter**.
5.  Select **Save**.
6.  Open the 'Saved Filters' list.
7.  Select the **Trash Can** icon next to the saved filter that was just created.

 Expected behavior: The confirmation explicitly says that when a filter is deleted—especially one that has been shared to a group or globally—it is deleted for everyone.

 Actual behavior: The confirmation dialog opens and shows: 'Active will no longer be available in your saved filters. This action can't be undone'.

</td></tr><tr><td>

Condition Builder in Workspace

 PRB2011310

</td><td>

The **SLA** field is read-only in a related condition when creating a list in Workspace

</td><td>

**The SLA** field and the operator should not become ready-only.

</td><td>

1.  Log in to a base instance.
2.  Select **Workspaces** from the Banner/Header Menu.
3.  Search for 'Service Operations Workspace'
4.  Select **Service Operations Workspace**.
5.  Once the workspace is open, navigate to **Lists**.
6.  Navigate to **My Lists**.
7.  Select the **Create new list** button.
8.  Navigate to **Create your own**.
9.  Provide the list name, such as 'Testing'.
10. Select **Source - HR Case \[sn\_hr\_core\_case\]**.
11. Navigate to **Add Filters** &gt; **Condition**.
12. Select the field, **SLA\(sla\)**.

Observe that the field and operator become read-only.


 Expected behavior: The**SLA** field should not become read-only.Actual behavior: The **SLA** field is read-only.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2017461

</td><td>

There's MULTI\_MATCH errors when duplicate rows exist in cmdb\_rel\_ci for non-dependency relationships

</td><td>

After upgrading to the Australia release, Discovery logs may show errors when processing CI relationships if there are pre-existing duplicate rows in the cmdb\_rel\_ci table for the same parent-child-type combination. These errors are harmless and do not affect data integrity. The duplicate relations in cmdb\_rel\_ci should be handled gracefully without generating errors in Discovery logs.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2017567

</td><td>

There is an infinite loop in PartialPayloadProcessor when the payload size limit is exceeded on the first record of a batch

</td><td>

Re-running the payload after changing the property 'glide.​identification\_​engine.​partial\_​processing\_​max\_​fetch\_​memory\_​mb' to zero causes the thread to be in an infinite loop.

</td><td>

1.  Run the payload to create a partial payload: var payload = \{ 'items': \[ \{ 'className': 'cmdb\_ci\_computer', 'values': \{ 'ram': 'q111211' \}, 'sys\_object\_source\_info': \{ 'source\_native\_key': 'IRE\_TOI\_PARTIAL\_1', 'source\_name': 'SERVICENOW', 'source\_feed': 'DISK\_FEED', 'source\_recency\_timestamp': '2019-08-26 13:00:00' \} \}, \{ 'className': 'cmdb\_ci\_disk', 'values': \{ 'name': 'disk1' \} \} \], 'relations': \[ \{ 'parent': 0, 'child': 1, 'type': 'Contains::Contained by' \} \] \}; var input = new JSON\(\).encode\(payload\); var output = SNC.​Identification​Engine​Scriptable​Api.​create​Or​Update​CIEnhanced\('SERVICENOW',​ input, \{\}\); gs.print\(output\);.
2.  Change the property to 'glide.​identification\_​engine.​partial\_​processing\_​max\_​fetch\_​memory\_​mb' to 0.
3.  Re-run the payload.

 Observe the thread is now in infinite loop.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2018505

</td><td>

The multiSource **last\_discovered** field is not updated even when the CI is updated

</td><td>

The multi-source last\_discovered timestamp is not updated when CI is rediscovered from the same source.

</td><td>

1.  Run the following script to create a multi-source record: var payload = \{ 'items': \[\{ 'className': 'cmdb\_ci\_linux\_server', 'values': \{ 'short\_description': 'Linux server description', 'name': 'Linux Server 1' \} \}\] \}; var input = new JSON\(\).encode\(payload\); var output = SNC.​Identification​Engine​Scriptable​Api.​create​Or​Update​CIEnhanced\('Service​Now',​ input, \{\}\); gs.​print\(JSON.​stringify\(JSON.​parse\(output\)​,​ null, '\\t'\)\);.
2.  Manually add the last\_discovered value to col51 in the cmdb\_multisource\_data table for this record.
3.  Rerun the same payload with the same CI with updated short\_description.

 Observe that col51 is not updated with the latest time stamp.

</td></tr><tr><td>

Connections and Credentials

 PRB2007222

</td><td>

AuthMetadataProvider .getAliasInfoList\(\) performs unfiltered full-table scan on sys\_alias \(29,000+ rows\)

</td><td>

This causes QueryWarning and excessive DB load. The same behavior occurs via any code path that calls PersonalAuthClient .​get​Auth​Credential​Info\(credential​Id\)​.​

</td><td>

1.  Open an instance with a large number of aliases in sys\_alias \(for example, 29,000+ records\).
2.  Trigger a flow that invokes sn\_cc.PersonalAuthAPI\(\) .getInitiatorURL\(aliasId\) with a valid alias ID.

 Observe that the following warning appears in the system logs: 'QueryWarning \*\*\* WARNING \*\*\* Large Table: Table handling an extremely large result set: 29180'. Additionally, observe that the info-level log for orphaned credential aliases contains 'Cannot find a credential with the given alias sys\_id...'.

</td></tr><tr><td>

Content Library Portal

 PRB2005753

</td><td>

Content lookup historical data triggers unintended deduplication for pa\_manual\_breakdowns records

</td><td>

The fix script runs with the 'isHistorical' parameter set to true, then it calls the deduplicateByValueField function. The duplication logic doesn't query for the breakdown; it only looks for duplicated value to identify duplicate records. In theory, there could be duplicated value across different breakdowns, causing unwanted data loss.

</td><td>

 

</td></tr><tr><td>

Content Library Portal

 PRB2010143

</td><td>

Multiple ais\_index events are triggered for sam\_sw\_product\_lifecycle during content updates

</td><td>

During content updates in the ITAM Content Library, a large number of ais\_index events are generated for the sam\_sw\_product\_lifecycle \(SAM software lifecycle\) and sn\_hamp\_lifecycle\_definition \(HAM hardware lifecycle\) tables. These events appear in the event log. The excessive events are triggered because system metadata columns on the AI Search datasources for these two tables are missing the no\_text\_index field attribute. Without this attribute, the AI Search indexing engine includes these columns in the vector index.

</td><td>

 

</td></tr><tr><td>

Core UI Responsive Dashboards

 PRB2019649

</td><td>

Exclude legacy dashboards from the 'PA Indicator Recommendation Calculator Job'

</td><td>

The 'PA Indicator Recommendation Calculator Job' takes a long time to run \(10+ hours\).

</td><td>

 

</td></tr><tr><td>

Customer Operations for Customer Service Management

 PRB2017754

</td><td>

Query rules show an error with Security Constraints and remove records

</td><td>

Query rules show an error and also pull more data than the Territory member assignment

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB2028756

</td><td>

While upgrading from Yokohama to Zurich, a skipped error occurs

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

Database Indexes

 PRB1975183

</td><td>

Creating an index on a few columns with an already existing column causes a drop of the redundant index and a 'AccessExclusiveLock' on a table

</td><td>

 

</td><td>

1.  Ensure that an index already exists on an instance for the ColA.
2.  Create an index on: ColA, ColB, ColC, ColD.
3.  Verify that the redundant index check is dropping the index, causing 'AccessExclusiveLock' and slowness on the instance.

 Expected behavior: It should have been dropped concurrently so that there's no instance wide issue while dropping the index.

 Actual behavior: There's an instance wide issue due to the 'AccessExclusiveLock'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2021451

</td><td>

MariaDB/Oracle UUID values with hyphens need to be normalized in query time

</td><td>

When query a UUID column has hyphens, the returned results won't be correct as UUID values are stored without the hyphens. It's okay for Postgres because it accepts UUID values with or without values, but this breaks on MariaDB and Oracle.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2027220

</td><td>

ColumnName.resurrect\(\) re-shortens long names, corrupting external store column names on deserialization

</td><td>

ColumnName.resurrect\(\) reconstructs a ColumnName from its serialized form using new ColumnName\(name\), which re-applies the preFujiShortColumnName\(\) 30-character shortening algorithm. However, serialize\(\) writes the already-resolved fName directly. For external-store columns \(Snowflake, BigQuery, Trino\) whose physical names exceed 30 characters, the name is corrupted on deserialization — the resurrected ColumnName points to a shortened name that doesn't exist in the external store.

</td><td>

1.  Create a ColumnName with shortening turned off: new Column​Name\('external\_​column\_​with\_​a\_​very\_​long\_​name',​ false\) \(37 chars, exceeds MAX\_LENGTH of 30\).
2.  Serialize via ColumnName.serialize\(writer, cn\).
3.  Deserialize via ColumnName.resurrect\(reader\).

 Observe the resurrected name is the 30 character shortened form, not the original 37 character name — a round-trip corruption.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2036434

</td><td>

Adding unique identifier \(UUID\) support for Workflow Data Fabric-Trino

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2036436

</td><td>

Add a unique identifier \(UUID\) Glide type

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Dictionaries

 PRB2021884

</td><td>

DictionaryXMLParser check for other numeric types

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1989714

</td><td>

The 'WITH' clause requires all variables to be explicitly aliased

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1991033

</td><td>

The user is not getting the expected response for the query, 'Give me active users created in Q3 in 2025' in Gemini

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1991929

</td><td>

Add a guardrail to prevent unbounded/extremely large queries from the LLM

</td><td>

A 184M SQL query was produced and attempting to parse it brought the node down with OOM.

</td><td>

Execute cypher2Results with the cypher query.

 Observe that OOM is parsing the massive generated SQL.

</td></tr><tr><td>

Database Persistence - Graph

 PRB2025391

</td><td>

Encoded query is not supporting variable length edges

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2026584

</td><td>

Aggregate and Function types are not accepted in Function Using\(\)

</td><td>

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferrable serialization of the query.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2026592

</td><td>

Inline node properties via withProperties\(\) are dropped on round-trip

</td><td>

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferrable serialization of the query.

</td><td>

 

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

 PRB1931656

</td><td>

A data fabric \(DF\) table should be blocked when creating a 'shard' type rotation table

</td><td>

 

</td><td>

1.  Create a DF table.
2.  Assign unique string columns with type 'GUID'.
3.  Navigate to sys\_table\_rotation.
4.  Create a record.
5.  Add the name of the mapped table to the **Name** field.
6.  Choose a shard.
7.  Select the column with type 'GUID'.

 Expected behavior: The DF table should be blocked when it's being used as base rotation table for extension, rotation, and shard.

 Actual behavior: A rotation record is created with the DF table as a base rotation table.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1978280

</td><td>

Missing/Incorrect Date Part Implementations

</td><td>

Analysis of TrinoDatePartFormatter.java revealed eight implementation issues affecting date/time extraction functions.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2019390

</td><td>

Update sets do not capture interface specific metadata

</td><td>

When the user creates a field mapping and interface to implementation relationship record in the m2m, only the table and columns are captured, but no interface specific metadata is captured.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2019509

</td><td>

Materializing virtual table when max\_insert\_size is reached fails

</td><td>

When the user hits the max\_insert\_size and executes the query, the DBExtendedInsert DBI is nulled.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2030176

</td><td>

Add DBI methods to abstract create/delete temporary tables

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2030390

</td><td>

A java.lang.SecurityException occurs

</td><td>

The error reads, 'Illegal access to method close\(\) in class com.glide.db.DBQuery'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2032178

</td><td>

Ensure Glide UUID time based generation is sortable

</td><td>

Currently Glide UUID time based generation is not always sortable, if multiple UUIDs are generated in the same millisecond.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2036451

</td><td>

Enable data interface tables to work with remote and virtual tables

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2036455

</td><td>

Column mapping capability

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2036458

</td><td>

Basic field-level transform support on interfaces

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB1949587

</td><td>

Archive conditions are deleted when users edit the destroy rule conditions

</td><td>

When predicate builder is used, the user observes many fields in a drop-down list for a dot walked field when compared to the fields observed in UI16.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB1976888

</td><td>

StatsGatherer isn't collecting stats when it runs in parallel with a SNC provision job

</td><td>

 

</td><td>

1.  Navigate to sys\_sdu\_collection\_job.
2.  Change the 'Collection' job record status to 'running'.
3.  Run StatsGatherer.

 See that StatsGatherer should collect stats, but isn't.

</td></tr><tr><td>

Data Management Console

 PRB1978885

</td><td>

Enable Data Destroy checkbox gets unchecked when a pop-up is closed using the **Close** button

</td><td>

When the Enable Data Destroy checkbox is checked and the user unchecks it, a confirmation pop-up appears with **Yes**, **Cancel**, and **Close \(X\)** options. Selecting **Close \(X\)** closes the pop-up and reverts the checkbox back to its previously checked state — no change is applied. Selecting **Cancel** closes the pop-up and reverts the checkbox back to its previously checked state — no change is applied. Selecting **Yes** closes the pop-up and applies the change — checkbox remains unchecked. The same revert behavior applies in reverse — if unchecked and user checks it, then dismisses via **Close \(X\)** or **Cancel**, it reverts back to unchecked.

</td><td>

1.  Navigate to the Edit Archive Rule page.
2.  Ensure the Enable Data Destroy checkbox is checked.
3.  Uncheck the checkbox.

Observe that a confirmation pop-up appears with **Yes**, **Cancel**, and **Close \(X\)** options.

4.  Select the **Close \(X\)** button on the pop-up.

 Expected behavior: The pop-up closes. Enable Data Destroy checkbox reverts to its previous checked state. No change is applied unless the user explicitly selects**Yes**.

 Actual behavior: The pop-up closes. Enable Data Destroy checkbox becomes unchecked even though the action was not confirmed.

</td></tr><tr><td>

Data Management Console

 PRB2013603

</td><td>

StatsGatherer early death

</td><td>

Stats Gatherer stops with the error 'Zero records found in sys\_audit'.

</td><td>

1.  Create sys\_audit SPTS with 0 row count.
2.  Trigger Stats gatherer.

 Observe Stats Gatherer stops with error 'Zero records found in sys\_audit'.

</td></tr><tr><td>

Data Management Console

 PRB2013605

</td><td>

The Statsgatherer job is finished with incomplete data

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB2015722

</td><td>

Loading conditions don't appear in rule details page

</td><td>

Conditions do not appear where they should.

</td><td>

1.  Log in to the instance.
2.  Navigate to the DMC.
3.  Select a table with an archive rule and navigate to Rule Details page.
4.  Edit any field on the page and select **Update**, then switch the tabs.
5.  Observe the table associated with the rule.

 Expected behavior: The conditions should be displayed for the rule.

 Actual behavior: The conditions are not appearing.

</td></tr><tr><td>

Data Management Console

 PRB2019127

</td><td>

Persistence Failures \(Missing Parent Stats ID\) for ALIAS/Normal

</td><td>

Peripheral stats are not stored.

</td><td>

1.  Create a table with long table name.
2.  Enable the sys\_audit stats for this in Audit management console.
3.  Change any field in this table.
4.  Audits will be added with tablename = ALIAS:\{shortTableName\}.
5.  Now run stats gatherer.

 Observe that peripheral stats are not stored for this table and the error is logged.

</td></tr><tr><td>

Data Management Console

 PRB2025271

</td><td>

Change the status column label for tables on primary/gateway to **Active** from 'Live'

</td><td>

With the new naming convention for Data archiving solution to object storage, the label for status column value displayed is renamed so that it is not confusing.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB2030039

</td><td>

'Physical Table Stats Gatherer' is triggered, which does 'UNION ALL' for rotated tables

</td><td>

There's a repeated slow query \#-1454801932 from the daily 'Physical Table Stats Gatherer' job, which is triggered 6 times. This causes spikes in SQL response times.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB2032534

</td><td>

When 'Age in seconds' is less than 3600, it's resolved as 0 in the Data Management Console \(DMC\) rule screen

</td><td>

The 'Age in seconds' property set on an auto flush rule is translated into years, days and hours for the rule management page. Seconds &lt; 3600 doesn't make up an hour, so it has resolved as 0 in hours.

</td><td>

1.  Create an auto flush rule with age in seconds = 3599.
2.  Open the created rule from DMC by navigating to the table details view and then picking the concerned rule from the 'Rules' tab.
3.  Verify that the matchfield inputs for years, days and hours show 0.

</td></tr><tr><td>

Data Management Console

 PRB2034974

</td><td>

An age of less than 3600 seconds is resolved as 0 in the DMC rule screen

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2022419

</td><td>

Unable to generate granular findings for **Journal** fields in Data Discovery job

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Create data discovery policy with different type of columns.
3.  While running a data discovery job, select track granular discovery, run the job.
4.  Open the granular findings.
5.  Verify the age pattern from any records.

 Observe that there is no age mentioned, yet its still its detected as sensitive data.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2024478

</td><td>

**Currency** field types are not anonymized properly

</td><td>

The **Currency** field type is not recognized by the Data Privacy discovery engine or processed by anonymization rules.

</td><td>

 

</td></tr><tr><td>

Data Product Backend Services

 PRB2027662

</td><td>

**Resolving** field mapping discrepancies between interfaces and implementers

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Snapshots

 PRB2028735

</td><td>

On non-eligible instances for Data Snapshots, Data Snapshots functionalities are accesible

</td><td>

The following data snapshots functionalities are accessible in non eligible instances for data snapshots: Data Snaphshots Hierarchy, Data Snapshots Exclusions, Data Snapshots Jobs , Data Snapshots Jobs Logs, and Bucket Group Mapping for Data Snapshots.

</td><td>

 

</td></tr><tr><td>

Demand Management

 PRB2020276

</td><td>

The **Create Epic** UI action doesn't work in Australia

</td><td>

 

</td><td>

1.  Navigate to a 'Demand' record.
2.  Select the **Create Epic** related link on the 'Demand' form.

 Observe that the action doesn't work/is missing.

</td></tr><tr><td>

Developer Sandboxes

 PRB2016067

</td><td>

ServiceNow Studio shows 'Recently opened' across controller and sandboxes

</td><td>

'Recently opened' does show the project and file from sandbox.

</td><td>

1.  Choose an instance that has multiple sandboxes.
2.  Log in to one sandbox \(1\) and open SNS, then create a new project.
3.  Add a new file \(for example, a business rule\).
4.  Log into another sandbox \(or base\) and open SNS.

 Expected behavior: 'Recently opened' shouldn't show new project or file from sandbox \(1\)

 Actual behavior: 'Recently opened' does show the project and file from sandbox \(1\). Choosing them results in 'Not found' error.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB2029867

</td><td>

Users can configure more than 50 fields per use case, which does not match the product and pricing based limitations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Management

 PRB2032863

</td><td>

SmartDocs default skill enablement for all tables

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Management Services

 PRB2032865

</td><td>

Smart redaction with redaction codes and notes for documents

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Viewer

 PRB2021741

</td><td>

When printing a PDF from the $viewer.do UI page, an extra page is appended to the end of the PDF in the print dialog

</td><td>

When printing a PDF with Document Viewer \($viewer.do\) UI page using CTRL + P, an extra page is appended to the end of the PDF in the print dialog.

</td><td>

1.  Open a PDF attachment in $viewer.do.
2.  Press 'Ctrl + P'.
3.  Scroll down.

 Observe an empty page appended to the PDF.

</td></tr><tr><td>

Dynamic Guidance

 PRB2050926

</td><td>

Unintended Dynamic Guidance steps in Unified Navigation Onboarding modal

</td><td>

The onboarding modal contains Dynamic Guidance steps.

</td><td>

1.  Open a Zurich/Australia instance with Now Assist enabled.
2.  Log in as a user with Now Assist enabled.
3.  On first-time login, notice the onboarding modal.

 Expected behavior: The onboarding modal shouldn't contain the steps of Dynamic Guidance.

 Actual behavior: The onboarding modal contains the steps of Dynamic Guidance.

</td></tr><tr><td>

Dynamic Translation for Agent Chat

 PRB2030959

</td><td>

When using the live agent in Now Assist Virtual Agent \(NAVA\), the disclaimer message at the bottom is dynamically translated based on the agent's session language

</td><td>

The disclaimer message should be displayed in the end user's session language preference instead of the agent's session language.

</td><td>

1.  As an agent, impersonate a system administrator user.
2.  Switch the agent language to French under 'Preferences'.
3.  Navigate to **Service Operations Workspace**.
4.  Make the agent available.
5.  As the end user, set the session language to English.
6.  Navigate to the **Employee Service Center** portal.
7.  Initiate NAVA.

Observe the disclaimer message is in English.

8.  Connect to a live agent.
9.  Once the work item is offered to agent, accept the work item.

Observe that the disclaimer message is translated to French for the end user.


 Expected behavior: The disclaimer message should honor the end user's session language.

 Actual behavior: When connected to a live agent, the disclaimer message is changed based on the agent's session language.

</td></tr><tr><td>

Edge Encryption

 PRB2012969

</td><td>

Edge Encryption mass jobs do not support sys\_audit table rotation

</td><td>

Edge Encryption mass jobs \(such as mass-encrypt, mass-decrypt, key-rotation\) that process the audited journal field history do not correctly handle instances where the 'sys\_audit' table has been rotated. When sys\_audit is rotated, the historical audit records no longer reside in sys\_audit itself but in one or more physical rotation tables \(for example, sys\_audit0 or sys\_audit1\). Because the job execution infrastructure previously hard-coded sys\_audit as the target table, all direct updates issued during job processing targeted the base sys\_audit table and found no matching records. This results in zero rows being updated for any encrypted field that lives exclusively in a rotated partition.

</td><td>

1.  Configure an Edge Encryption mass job on a table/field whose **Journal** field is audited \(for example, incident.work\_notes with auditing enabled\).
2.  Rotate the sys\_audit table to create physical tables such as sys\_audit0 and sys\_audit1 that contain the actual audit records, and so that the sys\_audit base table is empty.
3.  Run the Edge Encryption mass job, such as mass-encrypt, mass-decrypt, or key-rotation.

 Observe that no audit records are updated, and the job reports zero rows processed for the AUDITED\_NEW\_VALUE and AUDITED\_OLD\_VALUE chunk types. When verifying in the database that encrypted values in sys\_audit0 / sys\_audit1 are unchanged, this confirms updates targeted the empty sys\_audit base table.

</td></tr><tr><td>

Edge Encryption

 PRB2016789

</td><td>

Edge Encryption mass decryption job doesn't support tables with edge encrypted data inside a field value

</td><td>

There are several tables that end up with edge encrypted data stored inside a field, but where the entire field is not edge encrypted. The user has no way to migrate this data from being edge encrypted. To allow sys\_archive\_log to be used in an edge encryption configuration, the user must add the 'edge\_table\_whitelist=true' attribute to the table in sys\_dictionary. Adding this attribute allows the sys\_archive\_log table to show up in the table list on the edge configuration page.

</td><td>

1.  Create an edge encryption configuration on the **incident.short\_description** field.
2.  Run a mass encryption job to encrypt the data on that field.
3.  Create an archive rule for the incident table to archive one or more of the records with an encrypted **short\_description** field.
4.  Verify that sys\_archive\_log records are created for the archived incidents, and that the **Payload** field has edge encrypted data.
5.  Create an edge encryption rule on **sys\_archive\_log.payload**.
6.  Create an edge decryption job on the sys\_archive\_log table.
7.  Run the job.

 Expected behavior: Edge encrypted data inside the**sys\_archive\_log.payload** field is decrypted by the job.

 Actual behavior: The scheduled encryption job does not have any execution records nor chunks, as it did not find any data to be decrypted.

</td></tr><tr><td>

Email Accounts

 PRB2022999

</td><td>

Add the capability to capture mailbox as part of headers

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB2017829

</td><td>

A fix script incorrectly marks event rules as UI16 incompatible

</td><td>

During an Australia upgrade, the fix script EM - Event​Rule​UI16​Compatibility​Updater runs to populate the **is\_ui16\_compatible** field on all existing em\_match\_rule records. The method \_countRegexInFields counts field name occurrences across rawFields and additionalInfoFields to detect multiple regex patterns on the same field. However, it doesn't check whether the field actually has a regex value defined before incrementing the counter.

</td><td>

1.  Open a Zurich instance.
2.  Create and save an event rule where the same field name appears in both rawFields and additionalInfoFields.
3.  Upgrade the instance to an Australia version.

 Observe that in the event rule record is\_ui16\_compatible is set to false, and it can't be opened it from previous UI.

</td></tr><tr><td>

Event Management

 PRB2022546

</td><td>

Tag based group is created with single Alerts where em\_agg\_group points at two alerts

</td><td>

A new TBAC group is created with a recent corresponding alert only.

</td><td>

1.  Create TBAC rule.
2.  Send two events matching this TBAC rule.
3.  Wait for the TBAC group to be created with the corresponding two alerts.
4.  Create a new matching event but do not submit yet.
5.  Close on of the group secondaries.
6.  Immediately send the prepared Event from step 4.

 Notice that a new TBAC group is created with a recent corresponding alert only.

</td></tr><tr><td>

Experimentation Framework Core

 PRB2033548

</td><td>

Before activating any feature, an admin must accept the new feature preview terms in the modal

</td><td>

 

</td><td>

 

</td></tr><tr><td>

External Content Connectors Glide

 PRB2027151

</td><td>

After deleting the SPO connector, results can still be found

</td><td>

The AIS query engine requires the qlang=advanced parameter to correctly interpret and match documents. Without it, queries silently fail to match any documents, causing operations like deleteByAISQuery to delete zero records.

</td><td>

 

</td></tr><tr><td>

Financial Management

 PRB2032487

</td><td>

Role available in the ACL is not actually available in the Role table, so there are orphan records available in the sys\_security\_acl\_role table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Financial Services Operations

 PRB2038662

</td><td>

A query range error appears when querying on the filter present under 'Claim transaction' &amp; 'Receiving transaction'

</td><td>

Part of the query on sn\_bom\_transaction is ignored because of insufficient access for the 'query\_range' operation on sn\_bom\_transaction.details.

</td><td>

1.  Impersonate the sn\_bom\_payment.claim\_agent role.
2.  Navigate to **Workspaces** &gt; **Financial services workspace** &gt; **Claims** &gt; **All** &gt; **New** &gt; **Internal claim**.
3.  Fill in all the details and add multiple transactions into the fields **Claim transactions** &amp; **Receiving transactions**.
4.  Save the form.
5.  Navigate to the related lists of 'Claim Transactions' and 'Receiving Transactions'.
6.  Select the filter icon and start querying on 'Sender transaction' &amp; 'receiving transaction' respectively on both the related lists.

 Observe the error as mentioned above.

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

 PRB2013989

</td><td>

AI agent execution fails when source of record has been created by the virtual agent on portal

</td><td>

This issue occurs when the impersonates user doesn't have the 'admin' role.

</td><td>

1.  Install the following:
    -   Playbook Experience \(playbook-experience:29.1.0\)
    -   Playbook Experience Components \(servicenow-​now-​playbook-​experience:​29.​2.​2-​SNAPSHOT\)​
    -   Process Automation Designer \(sn-​process-​automation-​designer:​29.​3.​1-​SNAPSHOT\)​
    -   Customer Service Management Demo Data' \(Plugin id: com.snc.customerservice.demo\)
    -   Playbooks for Customer Service Management \(app-​csm-​playbook:​6.​4.​0-​SNAPSHOT\)​
    -   app-​csm-​complaint-​case:​8.​0.​2-​SNAPSHOT
    -   app-​csm-​complaint-​case-​ai-​agents:​1.​1.​2-​SNAPSHOT
    -   app-​csm-​complaint-​gen-​ai:​2.​1.​2-​SNAPSHOT
2.  Impersonate the user 'Abel Tuter'.
3.  Navigate to **/csm**.
4.  Select the **Sparkle** icon to launch the virtual agent.
5.  Paste this prompt to the virtual agent to go through record creation: 'I want to log a complaint. My KNS-ULTRA1100 is over heating. The product becomes uncomfortably hot during normal operation, even with light usage. My colleague had also experienced the same issue with the product on their machine. It started happening 2 days ago'.
6.  Once the record has been created, impersonate the user 'Abraham Lincoln' on the platform.
7.  Find the created record.
8.  Keep selecting the **Continue** button to advance to the 'Research' stage.
9.  Select the **Use an AI agent** button.

 Notice that an error is shown to the user, and the execution plan is terminated with the message, 'You don't have the required access to complete this request. Try another request.'.

</td></tr><tr><td>

Flow Engine

 PRB2026000

</td><td>

Engines support for conditional 'go back to' in Playbooks

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1975298

</td><td>

After moving a flow from one instance to another using an update set, the flow variable label changes to match the variable name

</td><td>

In the payload of the custom update that captured the flow, the variable correctly displays its label in the update set payload. However, when viewed in Flow Designer, the label appears to have been updated to match the variable name.

</td><td>

1.  Prepare two Zurich instances.
2.  Navigate to the first Zurich instance.
3.  Create an update set and make it current.
4.  Create a simple flow and create a variable with a long name with a space.
5.  Ensure that those creations are captured in the update set and complete the update set.
6.  Deploy this update set to the second Zurich instance.
7.  **Navigator** &gt; **Remote instance** &gt; **Retrieved completed update set** &gt; **Commit**.
8.  Open the flow and verify that the flow variable label is automatically updated to match the variable name.

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

 PRB2014125

</td><td>

Remove use of javascript: prefixed reference qualifiers

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Generative AI Controller

 PRB2026284

</td><td>

Agents aren't working in Zurich nightly with the latest snapshot

</td><td>

 

</td><td>

1.  Navigate to agents playground.
2.  Trigger any agent.

 See that the agent is stuck in starting and no context is passed to it.

</td></tr><tr><td>

GRC: Crisis Management

 PRB2039145

</td><td>

Adding similar tasks to a task group doesn't show the correct filters

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC Platform Plugins

 PRB2019351

</td><td>

On final approval of policy, a generated KB article is not published

</td><td>

The KB article is not published and throws the error, 'Failed to publish knowledge article'. The associated article is created by this user but is not moved to the 'Published' state.

</td><td>

1.  Navigate to sn\_compliance\_policy.
2.  Select **New** to open new policy form.
3.  Fill in the necessary fields.
4.  Add policy text, uncheck the **Require Review Approval checkbox**, and **Submit**.
5.  Select **Request Review**.

Notice that the system moves the record to the 'Review' state.

6.  Select **Request Content Approval**.

Notice that the system moves the record to the 'Approval' state.


 Observe that although the Final Approver approves the policy and the policy is published, the associated article is still in a 'Draft' state.

</td></tr><tr><td>

Hermes \(Family\)

 PRB2018415

</td><td>

Implement retry mechanism for publishing encryption metadata

</td><td>

The new cluster won't have the encryption key since there is no change detected in the dare\_key\_metadata table.

</td><td>

1.  Insert a key in the dare\_key\_metadata table that currently gets published to the inbox of a cluster \(Cluster A\).
2.  Change the Hermes clusters to point to another cluster \(Cluster B\).

 Observe that the new cluster won't have the encryption key since there is no change detected in the dare\_key\_metadata table.

</td></tr><tr><td>

Hermes \(Family\)

 PRB2028058

</td><td>

Identify and collect metrics for XML stats

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB2028059

</td><td>

Set up an observer on the dare\_key\_metadata table to observe and transmit key changes to the Broker's inbox topic

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB2028061

</td><td>

Hermes Topic Manager should have a configurable setting for a topic retention period

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB2028063

</td><td>

Topic Manager support for bring your own key \(BYOK\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Hiring Core

 PRB2025492

</td><td>

Only one Job Request is visible in 'Active Requisitions' on the home page of Recruitment Workspace

</td><td>

On the home page of Recruitment Workspace, only one Job Request is visible in the Active Requisition portion even if multiple Job Requests are present in the backend.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2023321

 [KB3025105](https://hi.service-now.com/kb_view.do?sysparm_article=KB3025105)

</td><td>

In HR Agent Workspace, an HR case can be cancelled without adding a work note, causing 'undefined' to be automatically logged in the conversation section

</td><td>

With the **Cancel** UI action \(sys\_ui\_action sys\_id 325370019f22120047a2d126c42e701d\)​,​ the workspace client\_script\_v2 unconditionally forwards the modal's **Work note** field to the server. When the field is left empty during case cancellation, GlideAjax.addParam stringifies undefined to the string 'undefined' and forwards it to the server, which then persists it to work\_notes.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HTML Field Type Editor

 PRB2008555

</td><td>

The @mention and response template in HTML Editor does not appropriately respond to assistive technologies

</td><td>

The screen reader does not identify the drop-down list or the members of the list.

</td><td>

1.  Create an account on Assistiv Labs to use NVDA and JAWS.
2.  Open a base instance.
3.  Create or set the system property 'glide.ui.journal.use\_html' to 'true'.
4.  Navigate to **Service Operations Workspace**.
5.  Open any incident.
6.  Open a screen reader, such as VoiceOver and Safari or JAWS/NVDA and Chrome.
7.  Navigate to the **Comments/Work Notes** field.
8.  Enter '@' and a character or two for the user to invoke the drop-down list for user selection.

 Notice that neither screen reader identifies the pop-up, nor is there any identification of the members of the list as the user navigates it.

</td></tr><tr><td>

HTTP Client

 PRB1914462

 [KB2813624](https://hi.service-now.com/kb_view.do?sysparm_article=KB2813624)

</td><td>

There's a warning log 'Invalid cluster size -1, will return'

</td><td>

This is caused by stricter hostname validation logic introduced in Glide's HTTP client layer. The change impacts RESTMessageV2 calls made from scheduled jobs within the HLA \(Health Log Analytics\) application. Although the target and source instance hostnames are identical, the platform incorrectly treats them as mismatched, resulting in a java.lang.SecurityException and blocking HLA workflows that rely on fetching /​xmlstats.​do?​include=​services\_​status.​ It breaks the HLA flow responsible for retrieving elastic endpoints and other service status information.

</td><td>

 

</td></tr><tr><td>

Identification and Reconciliation API

 PRB2031317

</td><td>

Apply fix script for base instance dynamic IRE properties

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Identity

 PRB1988754

</td><td>

NHIUserTrackerDAO has a cache \(sys\_mi\_user\_cache \) which is storing GlideDateTime objects

</td><td>

This issue was noticed in heap dumps.

</td><td>

 

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB2016072

</td><td>

Exclude Moveworks integration traffic

</td><td>

Moveworks requests to ServiceNow APIs \(such as Table API\) are being counted as integration traffic. They should be excluded.

</td><td>

 

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
3.  Check if the com.snc.iam is installed on upgrade.
4.  Check if the skipped error occurred. If so, see if that a problematic record exists.

</td></tr><tr><td>

Install Base Management Store

 PRB2027486

</td><td>

Errors in CanRead path from ACL

</td><td>

Failures observed in Service Portal with latest changes in responsibility framework.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1986252

</td><td>

Auto-heal when symmetric keys are deleted doesn't work as expected

</td><td>

The consumer replication gets stuck in a 'Request Producer Approval' state where Status=Active Replication and Consumer Approval Status=Approval Pending.

</td><td>

1.  Create an Hermes producer and consumer replication set on the incident table.
2.  Create and activate producer replication set for incident table.
3.  Create and activate consumer replication set.
4.  On the consumer, Navigate to the idr\_replication\_shared\_key table &amp; delete the record in the table.
5.  Replicate a single record from the producer to the consumer.
6.  Create a test record on the producer.

 Expected behavior: The consumer replication should self-heal &amp; be active. Replication should resume as expected with the shared\_key recovery.

 Actual behavior: The consumer replication gets stuck in a 'Request Producer Approval' state where Status=Active Replication and Consumer Approval Status=Approval Pending - manual intervention is required \(by selecting the**Request Producer Approval** button\).

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB2004240

</td><td>

Instance Data Replication \(IDR\) issues with batched seeding with CDATA-embedded declarations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB2014054

</td><td>

Cannot read the array length because 'bytes' is null

</td><td>

 

</td><td>

See above.

</td></tr><tr><td>

Instance Scan

 PRB2017072

</td><td>

Instance scans detecting custom records instead of other records are modified from the baseline

</td><td>

Instance scan checks like 'Differs from baseline' are detecting custom records created by users. As per the script used, only the records which are modified should be detected.

</td><td>

 

</td></tr><tr><td>

Instance Scan

 PRB2022691

</td><td>

Instance Scan Linter Check fails on sys\_module with an error: 'Rhino error: missing ; before statement'

</td><td>

 

</td><td>

1.  Create an app in ServiceNow IDE.
2.  Create at least one file \(for example, business rule\) that stores code in a sys\_module application file.
3.  Build and deploy the app.
4.  Create an Instance Scan Linter Check.
5.  Scan the resulting app \(or the individual sys\_module record\) using the linter check.
6.  In the scan result record on the 'Failures' related list.
7.  Validate that one or more errors are logged: 'Rhino error: missing ; before statement'.

</td></tr><tr><td>

Integration Authentication

 PRB2038657

</td><td>

Clone preservers are missing for IPKI Auth Policy tables

</td><td>

Target instance records are not preserved and the target has an exact replica of the source. This breaks integration from MID to the target as the MID servers are preserved but not the IPKI policy and user mappings.

</td><td>

1.  Configure two instances - source and target with IPKI Auth policies and map users to the policy.
2.  Add sys\_user to preservers list.
3.  Clone source over target.
4.  Post-clone, navigate to the sys\_ipki\_auth\_policy and sys\_ipki\_auth\_user\_policy table on the target instance.

 Observe that the target instance records are not preserved and the target has an exact replica of the source.

</td></tr><tr><td>

Integration Hub

 PRB2006931

</td><td>

The error message is not cleared out when the retry is successful and the retry status code is 200

</td><td>

When the retry is enabled in an action, if the first try fails with a 429 and the retry is successful, the **Error message** field does not get cleared out.

</td><td>

1.  Create any rest action with the retry policy.
2.  Execute for failure for the initial 2 or 3 calls.

Notice that there is an error message to the rest step output.

3.  At runtime, perform the appropriate changes so that the action starts to work fine and returns 200.

 Notice that this updates the status code to 200 and updates the success response body, however, the error message remains.

</td></tr><tr><td>

Integration Hub

 PRB2027484

</td><td>

wdf\_operator &gt; sn\_mcp\_client.viewer should be under the condition 'if plugin'

</td><td>

There's an error traced to an incorrect role inheritance in the base platform. The platform role wdf\_operator inherits sn\_mcp\_client.viewer as part of its shipped configuration. sn\_mcp\_client.viewer isn't a platform-native role; it belongs to the MCP application, which is a separately licensed, paid plugin. This inheritance wasn't conditionally guarded, so it is applied unconditionally on all instances, including those where the MCP plugin isn't installed. On instances without the MCP application, this dangling role reference triggers the error.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB2034438

</td><td>

Terminal attachment is processed before non-terminal attachments

</td><td>

This causes partial data processing in the JDBC data stream action during race condition.

</td><td>

1.  Create a JDBC DataStream action.
2.  Run it.

 Observe that the terminal attachment \(small in size\) is processed before non-terminal attachments \(large in size\). In the execution results, it shows less data.

</td></tr><tr><td>

IT Asset Management for Financial Services

 PRB2000282

</td><td>

The 'Read Only' option needs to be set on missing app-itam-asset-audit-response tables

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

IT Asset Management for Financial Services

 PRB2026876

</td><td>

Update 3P default models to the latest available

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB2058369

 [KB3140571](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3140571)

</td><td>

MID server is unable to fetch credentials after upgrading to Zurich or Australia

</td><td>

In certain versions, there's a Unified Secrets Gateway \(USG\) service for credential management. During the upgrade to those versions, a system trigger script is designed to automatically execute and populate the sys\_secret\_identity\_group\_member table with the MID Server identity group mappings required for USG authentication. However, this trigger fails to complete successfully, leaving the table incompletely populated. As a result, the MID Server can't authenticate with USG and fails to retrieve credentials.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1986102

</td><td>

Fix/disable IPKI KMF diagnostics job to reduce the performance impact on downstream services

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB2007037

</td><td>

A duplicate Instance Key Encryption Key \(IKEK\) is active in the instance after a future rotation date

</td><td>

Although it is observed the current IKEK gets deactivated and a new IKEK is generated, it later actives back the deactivated one. This causes multiple IKEK to be in an active status.

</td><td>

Set/Check the active IKEK future rotation date.

 Notice that after the rotation check, there are two active IKEK.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB2014313

</td><td>

Nodes taking long time to load CrytpoCore initialization during startup

</td><td>

It is observed that some nodes are taking an unusually long time during CryptoCore initialization at startup. A few nodes are taking anywhere between 15 minutes to up to 4 hours to complete CryptoCore initialization. Due to the large volume of logs, performing a full-day analysis in splunk places additional load on the indexers. A subset of nodes were identified consistently exhibiting this behavior.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB2035774

</td><td>

SecretAPI Core

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB2035775

</td><td>

Generic secrets wrapper API and Glide-independent interfaces

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1997589

 [KB2970962](https://hi.service-now.com/kb_view.do?sysparm_article=KB2970962)

</td><td>

A published article displays a gray HTML body when ECE and the 'Minor edit' property are turned on

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2027236

</td><td>

True-up for KC and NAKM, ECE, and KC in UI Builder

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

KPI Details

 PRB2017652

</td><td>

Selecting KPI 'Details' records in Platform Analytics redirects to a blank page when glide.ui.polaris.experience is set to false

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB2026077

</td><td>

Dependent activity sets are not getting triggered when completing activities after upgrade to Zurich

</td><td>

This occurs when upgrading from Yokohama to Zurich.

</td><td>

1.  Setup an instance in Yokohama
2.  Create multiple LE cases and move them to ready state. Ensure sn\_hr\_le.use\_flow property is set to true.
3.  Upgrade to Zurich.
4.  Complete Pre hire activity set.

 Expected behavior: Pre-boarding activities should have created.

 Actual behavior: Pre-boarding activities are still in awaiting trigger.

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

 PRB2034695

</td><td>

Unexpected 's' character appears in a related list filter when using an operator in UI16 after Australia upgrade

</td><td>

When Accessibility is enabled in UI16 \(Preferences &gt; Accessibility\) and a related list is filtered using operators such as 'is one of', an extra 's' character appears in the breadcrumb.

</td><td>

1.  In UI16, Navigate to **Profile Picture** &gt; **Preferences** &gt; **Accessibility** and enable 'Enable accessibility in classic'.
2.  Navigate to a record with related lists \(for example, Problem\).
3.  Open any related list \(for example, Problem Tasks\).
4.  Apply a filter such as State is one of \[values\].

 Observe the filter above the related list has an extra 's' before State.

</td></tr><tr><td>

Live Archive

 PRB1987487

</td><td>

Improve Attachment migration to Columnar performance

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Live Archive

 PRB1989270

</td><td>

Mismatch between number of records succesfully in DM run and sys\_attachment table

</td><td>

There is a mismatch in the number of records migrated.

</td><td>

1.  Navigate to sys\_dm\_run for attachment migration run and filter by ar\_incident in run details.

This queries 471,353 number of records successfully processed.

2.  Navigate to sys\_attachment table and filter by tablename 'ar\_incident and column type equal to 'COLUMNSTORE'.

This queries 547,901 number of records.


 Expected behavior: The number of records should match in DM run and attachment table.

 Actual behavior: There is a mismatch in the actual number of records migrated.

</td></tr><tr><td>

Major Incident Management

 PRB2030990

</td><td>

The Major Incident Management \(MIM\) plugin is installed automatically after upgrading in Australia

</td><td>

The MIM family plugin is added as a dependency on the Service Operations Workspace MIM application. The dependency of the MIM plugin should be removed from the sn\_sow\_mim plugin.

</td><td>

Upgrade an instance to Australia.

 Expected behavior: The MIM family plugin shouldn't be installed on the upgrade.

 Actual behavior: The MIM family plugin is installed on upgrading to Australia.

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

 PRB2034352

</td><td>

MID doesn't sync ECC firewall message audit data on shutdown, leading to audit data loss

</td><td>

If using the default 1 hour reporting interval, up to 1 hour of data could be lost if MID is restarted between reporting intervals.

</td><td>

1.  Start a MID Server - if desired, set the MID.​ecc.​queue.​audit.​report\_​interval to the minimum value of 900 seconds \(15 minutes\).
2.  Kick off a large Discovery to ensure a steady flow of ECC messages to the MID Server.
3.  Wait for ECC firewall message audit data to be reported for the first time
4.  After ten minutes, stop the MID.

 Notice that there are no audit data updates since the first reporting interval.

</td></tr><tr><td>

MID Server

 PRB2035227

</td><td>

ECC queue firewall in MID hardening and MID control

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035228

</td><td>

MID Server Security 2026

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035229

</td><td>

Application authorization for MID server execution in MID hardening authorization

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035230

</td><td>

MID hardening in the authorization track

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035231

</td><td>

Adopting USG for credentials in MID hardening

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035232

</td><td>

MID hardening in the logging/telemetry track

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035233

</td><td>

MID hardening and authentication JWT using iPKI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035234

</td><td>

Uniquely identifying a MID server in MID hardening authorization

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2039554

</td><td>

Issues with download page on new UI and misc others

</td><td>

The download page does not open with the new UI, there are zboot errors due to a missing version, and there are issues with migration page auto refresh.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2040231

</td><td>

MID users are missing the MID Server role

</td><td>

Only MID users with the MID server role can load credentials for discovery use cases.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1984781

</td><td>

Incremental offline caching does not sync related records for newly created Work Order Tasks \(WOT\) after the initial offline payload is downloaded

</td><td>

Related records are missing in offline mode for the WOT.

</td><td>

1.  Provision an instance with the following plugins:
    -   com.snc.work\_management
    -   com.snc.work\_management.demo
    -   com.sn\_fsm\_mobile
2.  Ensure incremental offline is configured and working, so that the offline payload download works and incremental jobs are being processed.
3.  Using the Agent mobile app, trigger the incremental offline process by downloading the offline payload.
4.  Create a new work order task \(WOT\) using the instance configuration.
5.  Create part requirements related to the WOT using instance configuration.
6.  Using the Agent mobile app, navigate to **Offline mode**.
7.  Check if the newly created WOT exists.
8.  Open the WOT.
9.  Navigate to the corresponding section that contains information about part requirements.
10. Validate that the parts associated with the WOT are viewable.

 Expected behavior: The new WOT appears in offline mode, and the related records created are present in the corresponding section and visible offline. Additionally, an incremental payload is generated for the new task and its related records \(entries in sys\_sg\_incremental\_result\).

 Actual behavior: The new WOT presents, but related records are missing in offline mode. For the newly created WOT, no new watcher record is created in sys\_rw\_action, so subsequent related record inserts are not tracked. Since no watcher exists for this WOT, no incremental payload parts are generated for its related records, so they never arrive in the device's offline cache.

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2029152

</td><td>

Update vision agent AIA records to consume new multimodal service-backed video Q&amp;A subflows

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2029156

</td><td>

Move MMS to GA

</td><td>

The MMS plugin name displays 'USER WITH ELEVATED PRIVILEGES ONLY', and should be updated.

</td><td>

 

</td></tr><tr><td>

Multi-provider Single Sign-on \(SSO\)

 PRB2003491

 [KB3065130](https://hi.service-now.com/kb_view.do?sysparm_article=KB3065130)

</td><td>

An admin-only ACR user can't log in via local log in as the sso\_config\_admin role check in ACRUtil.isACRUserByUserID\(\) ignores the admin role

</td><td>

When SSO Account Recovery \(ACR\) is turned on in an instance, an admin user registered as an ACR recovery account may be unable to log in via local login even when valid credentials are entered. The system doesn't recognize the user as a valid ACR recovery account and blocks the login attempt. The primary purpose of ACR is to provide a fallback login path during an SSO outage. Due to this issue, the designated recovery administrator loses access to the instance at the exact moment the fallback is needed. This issue was introduced in the Australia release.

</td><td>

Refer to the listed KB article for details.

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

 PRB2033990

</td><td>

Desktop navigation selection redirects to the wrong window instead of SOW workspace

</td><td>

When the user selects a desktop notification, the wrong browser window gets activated instead of the one with SOW where a new interaction is 'ringing in'.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2034454

</td><td>

Record Summarization isn't using the page context

</td><td>

In Now Assist Portal \(NAP\), when standing on an incident record and if the user type is 'summarize this record', NAP should pick up the incident from the page context.

</td><td>

1.  Open an incident on Service Workspace.
2.  Open NAP.
3.  Type 'summarize this record' in NAP.

 Expected behavior: NAP should summarize the incident the user is seeing.

 Actual behavior: NAP asks the user to enter the incident record number.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2036738

</td><td>

Duplicate desktop notifications are created for a single assignment to an agent

</td><td>

A desktop notification for a new chat shouldn't appear second time for the same assignment. It should re-appear only on reassignment.

</td><td>

1.  As Agent Beth Anglin, enable desktop notifications from the settings **Gear** icon next to the presence drop-down list and enable browser level notifications.
2.  As agent Beth Anglin, open SOW workspace and set the presence to 'Available'.
3.  Open another window pointing to the home page.
4.  As requester Abel Tuter, open the ESC portal, start a chat, and transfer it to a live agent.

In an Agent session, there is a desktop notification pop up that appears for the new chat.

5.  Select the notification to navigate to the workspace page.
6.  Within few sec, refresh the second window that has a home page.

 Expected behavior: A desktop notification for a new chat shouldn't appear second time for the same assignment. It should re-appear only on reassignment.

 Actual behavior: A desktop notification appears for the second time for the same assignment.

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

Now Assist in Document Intelligence

 PRB2030125

</td><td>

Support attachments where the file names doesn't contain '.type' at the end

</td><td>

There's an error: '\{'attachment':​\{\}​,​'task':​\{'708a54b23b810f50141a0e0f23e45a0b':​\{'error\_​msg':​'Prediction server is not able to process the attachments: begin 0, end -1, length 9'\}\}\}'.

</td><td>

1.  Have a PNG image file with no errors.
2.  Rename it to have a file name with '.png'.
3.  Upload it to an instance.
4.  Test the attachment summarization.

 Observe an error.

</td></tr><tr><td>

Now Assist Nextwave Experience

 PRB2015459

</td><td>

Now Assist Portal's unread conversation count disappears after the execution is started via AI Agent triggers or Runtime APIs

</td><td>

The unread conversation count over the NAP icon on the menu bar disappears.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB2003390

</td><td>

**The New Chat** button is disabled on Now Assist panel \(NAP\) when launched through AI Engagement Experience Layer \(AIEL\)

</td><td>

When an agentic workflow is triggered by a UI action in a workspace using AIEL with forceNewConversation set to 'true', NAP launches successfully with a new conversation session. However, the **New Chat** button remains persistently disabled throughout the session, preventing users from initiating additional conversations. Additionally, the name of the workflow at the top of NAP is not displayed and the conversation does not show up in the list of prior conversations.

</td><td>

1.  Trigger an agentic workflow using a UI action in a workspace to auto-launch NAP with forceNewConversation set to 'true'.
2.  Ensure NAP launches with the workflow triggered in a new conversation session.

Observe the state of the **New Chat** button in the NAP header.


 Expected behavior: The**New Chat** button is enabled, allowing users to start a new conversation.

 Actual behavior: The**New Chat** button is always disabled when NAP is launched through AIEL.

</td></tr><tr><td>

OAuth 2.0 integration

 PRB2032073

</td><td>

Chat-Input is available to requester when conversation ends

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Onboarding Experience

 PRB2050925

</td><td>

Unintended Dynamic Guidance steps in Unified Navigation Onboarding modal

</td><td>

The onboarding modal contains Dynamic Guidance steps.

</td><td>

1.  Open a Zurich/Australia instance with Now Assist enabled.
2.  Log in as a user with Now Assist enabled.
3.  On first-time login, notice the onboarding modal.

 Expected behavior: The onboarding modal shouldn't contain the steps of Dynamic Guidance.

 Actual behavior: The onboarding modal contains the steps of Dynamic Guidance.

</td></tr><tr><td>

On-Call Scheduling

 PRB2030480

</td><td>

Wrapper global APIs for on call bulk upload utility

</td><td>

 

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB2030962

</td><td>

The On-Call Scheduling family plugin is installed on upgrading to Australia

</td><td>

The On-call plugin has been added as a dependency for the sn\_sow\_on\_call plugin as part of core IT changes. This is causing issues for some users. On-call is automatically installed for new users via zboot. However, upgrade users need to install it manually. Due to the new dependency on the Store app, On-call is installed for some users when the commons bundle is upgraded. The dependency of the On-Call Scheduling plugin should be removed.

</td><td>

1.  Open any pre-Madrid instance where the On-call plugin isn't installed.
2.  Upgrade to Australia.

 Expected behavior: The On-Call Scheduling family plugin shouldn't be installed on upgrading to Australia.

 Actual behavior: The On-Call Scheduling family plugin is installed on upgrading to Australia.

</td></tr><tr><td>

OneExtend

 PRB2028533

</td><td>

Java scriptable methods aren't working in some instance nodes

</td><td>

The script should return a proper response in all nodes.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2038858

</td><td>

Mosaic/NowAssist jobs run for extended periods, slowing down processing

</td><td>

The Mosaic Off-Glide Kafka log-sync flow has no recovery path when subscription activation lands in a bad state.

</td><td>

 

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

 PRB2015951

</td><td>

The indicator **Sparkle** icon shows on data visualizations saved to the library

</td><td>

The **Sparkle** icon on data visualizations based on indicators should not show for data visualizations that are not saved to the library. This is a caching issue.

</td><td>

Disable the following properties:

 -   sn\_​query\_​gen.​indicator.​feature.​enabled
-   sn\_​pa\_​ai\_​canvas.​indicator.​feature.​enabled
-   sn\_​pa\_​ai\_​canvas.​entry.​visualization.​enabled

 Expected behavior: The**Sparkle** icon should not show on any data visualization, and whether it's saved to the library or not is based on an indicator source.

 Actual behavior: Notice that the**Sparkle** icon on data visualizations based on indicators still show for data visualizations saved to the library. This is caused by analytics\_cache, which clears out every 24 hours.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2032319

 [KB3083846](https://hi.service-now.com/kb_view.do?sysparm_article=KB3083846)

</td><td>

Localized names on the Performance Analytics and Reporting \(PAR\) dashboard are no longer displayed

</td><td>

The names of PAR dashboards localized for the Zurich environment are lost when upgrading to the Australia version.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2000095

</td><td>

The Guided Tour does not populate route parameters for 'default' dashboards, which breaks the functionality

</td><td>

By default, when navigating to 'now/​platform-​analytics-​workspace/​dashboards' and selecting a dashboard, the system will set the last dashboard that was viewed as the default' dashboard. This dashboard will always be displayed when navigating to the same page until the user views a different dashboard, at which point, that dashboard will then become the 'default'. In addition to this, when creating a new guided tour using a URL, the system auto-creates a sys\_embedded\_tour\_guide record and uses the values from the URL to populate the 'Context' and **Route parameters** fields. However, when a tour is created using the URL for a 'default' dashboard, no URL parameters are needed, and the system sets the 'Route parameters' value to empty \(\{\}\). If a user visits another dashboard, which will automatically set that dashboard as the 'default', the system attempts to run the same guided tour created for the previous default dashboard, and fails.

</td><td>

1.  Set a 'default' dashboard.
2.  Navigate to the URL: **now/​platform-​analytics-​workspace/​dashboards**.
3.  Navigate to any dashboard from the drop-down list menu, such as 'AI Agent Analytics'.
4.  Navigate back to the URL: **now/​platform-​analytics-​workspace/​dashboards**.
5.  Confirm the the last dashboard viewed is the dashboard that is displayed on the page.
6.  Copy the URL to the dashboard that is displayed.
7.  Created a guided tour for the default dashboard.
8.  Confirm it works as expected.
9.  Navigate to **Guided Tour Designer** &gt; **Create Tour**.
10. Set the following values:
    -   Name: Any
    -   Tour Type: Workspaces \(select **Paste URL**\)
    -   Roles: All
11. Create and publish the tour with example steps.
12. Navigate to **sys\_embedded\_tour\_guide.list**.
13. Open the record for the tour that was created.
14. Confirm that the context is 'now/​platform-​analytics-​workspace/​dashboards' and the 'Route Parameters' value is empty \(\{\}\).
15. Navigate to **now/​platform-​analytics-​workspace/​dashboards**.
16. Confirm the default dashboard displays.
17. In the header, select the **Show help** icon.
18. Confirm the tour runs as expected.

Notice the issue.

19. Set a new 'default' dashboard, such as IT Agent Dashboard'.
20. Navigate to **now/​platform-​analytics-​workspace/​dashboards**.
21. Ensure it loads the new default dashboard.
22. In the header, select the **Show help**.
23. Confirm the tour launches.

 Notice the tour fails, or crashes. This is due to the tour targets elements on the previous default dashboard. Since no URL parameters were saved as it was the default, the system cannot locate those elements on the new default dashboard, causing the failures.

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

 PRB2019318

</td><td>

The 'hide​New​Migrated​Dashboard​Modal' boolean is ignored in the 'Preference' **JSON** field of the dashboard API whenever there is a broken filter component in the migrated dashboard

</td><td>

The 'Welcome to PAE' pop-up occurs every time the user launches the dashboard.

</td><td>

1.  Set the system property 'com.​glide.​par\_​dashboards.​hide\_​new\_​migrated\_​dashboard\_​modal' to '=true' for boolean true/false.
2.  Migrate a classic dashboard with a filter on the incident priority.
3.  After migration, edit the par\_dashboard\_widget record of that filter element to have a broken stored component entry which doesn't exist in the par\_component\_filter table.
4.  Open the migrated dashboard.

 Expected behavior: The user should not see the 'Welcome to PAE' pop-up.

 Actual behavior: The user sees it every time they launch this dashboard.

</td></tr><tr><td>

Platform Analytics Filters

 PRB2018497

</td><td>

When using a date/time filter, the 'Today' predefined range incorrectly starts from the current hour instead of all of today

</td><td>

When setting up a date filter in Platform Analytics, if the predefined range of 'Today' is added and 'Allow time selection' is set, it will default to the start time of Current Date + Current time, and the end time of Current Date + 23:59. This means it is not showing the whole day, and instead just starting from the current moment and going into the future \(and therefore is unlikely to show any records\).

</td><td>

1.  Create a Dashboard in Platform Analytics.
2.  Add a date filter.
3.  Add the '**Today**' predefined range. Add any other predefined range for easy testing.
4.  Set the default value to '**Custom Range**'
5.  Enable '**Allow time selections**'.
6.  Save changes and Navigate to the date filter.
7.  Select any predefined range other than **Today**.
8.  Select **Today**.

 Notice that the date will update correctly, but the start time will update to the current time.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2009064

</td><td>

The calendar report event displays fields that are not migrated correctly for all tables

</td><td>

By default, the calendar report uses Number and short\_description, and the migration only supports this configuration. If the user creates custom calendar\_elements, it is not migrated.

</td><td>

1.  Navigate to the **sys\_dictionary** list.
2.  Find the Incident table in 'Attributes'.
3.  Add the new attribute calendar elements value, 'category; description'
4.  Create a calendar report on the Incident table.

Observe that events contain both the category and description instead of the number and short\_description.

5.  Migrate the report to visualization.

 Observe that the migrated visualization contains **Number** and **Short description** as event display fields.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2013849

</td><td>

The scheduled report recipient user list might contain email addresses

</td><td>

 

</td><td>

1.  Create a report schedule report.
2.  Use email addresses to insert recipients.

 Observe that the migrated report scheduled export does not have these recipients.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2016359

</td><td>

After the full migration, Core UI reports are not automatically redirecting to their newly migrated versions

</td><td>

After the full migration, the report menu links or favorite links are still redirecting to the Core UI version instead of the migrated version \(Data Visualization\). Non-admin users selecting bookmarks, favorites, or links are automatically redirected to migrated content after full migration.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2031469

</td><td>

The automatically triggered Core UI dashboard migration can cause an out of memory error and instance outages

</td><td>

After an Australia upgrade, the Core UI dashboard migration is triggered when a user loads the dashboard and the **Do not migrate in bulk \(no\_bulk\_migration\)** field is set to false. The field default value is false, so any dashboard that isn't migrated is triggered to migrate when it's viewed.

</td><td>

 

</td></tr><tr><td>

Platform Licensing

 PRB2036351

</td><td>

True-up of SM and LE 6.4.3

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Playbook Experience Core

 PRB2032183

</td><td>

Create record form not rendering when show\_create\_record\_form value is missing on record generator

</td><td>

The 'Create record' form fails to render on a playbook card when the record generator does not have a value populated for 'show\_create\_record\_form'. The expected behavior is that the form should render by default \(treating an absent value as true\), with the form only being hidden when 'show\_​create\_​record\_​form.​value' is explicitly set to '0'. Today, configurations that pre-date the 'show\_create\_record\_form' property or that omit it for any reason end up with no form rendered, which is a regression from the original always-show behavior.

</td><td>

1.  Provision an instance with Process Automation Experience Demo installed.
2.  Open up the Playbook Experience Demo.
3.  Open the playbook card for that activity in the runtime.

 Expected behavior: The form should render by default when 'show\_create\_record\_form' has no value. Only an explicit value of '0' should suppress it.

 Actual behavior: The form does not render when no value is present.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2023726

</td><td>

Validation rules for conditional restarts in playbooks

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2026890

</td><td>

Playbook translations are broken if messages cost more than 255 tokens and some changes are made to them

</td><td>

Key size is capped to 255. The key is formed by truncating the message which can be more than 255 tokens, the message is changed after the 255th token, the newly generated key would have no change.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2039142

</td><td>

Playbooks' AI native authoring experience

</td><td>

This is a product update.

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

 PRB2014422

</td><td>

Copying a Partial Project in Project Workspace not working as expected after upgrading to Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ReleaseOps - Family

 PRB2000140

</td><td>

The Deployment Analyzer rule fails for common catalog edits

</td><td>

The default 'Catalog Only Deployment Analyzer' rule \(DA\) is so restrictive it does not actually work, causing users to think that the DA is not working and not viable.

</td><td>

1.  Log in to the instance.
2.  Open Catalog Builder.
3.  Create a new catalog item.
4.  Add questions.
5.  Create a new UI Policy.
6.  Finish creating new catalog item.
7.  Publish it.
8.  Promote the catalog change update set that is autogenerated to utilize the 'Sample On-Demand Pipeline'.
9.  Progress the DR to 'Ready to Assess'.

 Notice that when Deployment Analyzer runs, it does not pass when it should. This is due to the missing metadata options. Instead, an error occurs, 'Deployment request moved to draft because it failed on demand criteria: must not contain non-catalog item changes'.

</td></tr><tr><td>

ReleaseOps - Family

 PRB2008798

</td><td>

Improve the logging of RemoteOperationUpdateHandler

</td><td>

 

</td><td>

1.  Create a DR.
2.  Mark it ready for assessing
3.  Check the logs.

 Expected behavior: The message reads, 'Starting RemoteOperationUpdateHandler for event with correlation id'.

 Actual behavior: The message reads, 'Starting RemoteOperationUpdateHandler for '.

</td></tr><tr><td>

ReleaseOps - Family

 PRB2030220

</td><td>

Add MIF Sync messaging support to ReleaseOps deployment operations to reduce multi-instance communication latency

</td><td>

In ReleaseOps, the product is leveraging asynchronous message handling for multi-instance deployment actions.

</td><td>

1.  Create a new release on Production Instance.
2.  Create a new Deployment Request.
3.  On Dev \(source\) instance create a new UpdateSet and make a change like create a new script include.
4.  Complete UpdateSet and save changes.
5.  Open the update set record completed from the step above and promote the update set, choose the DR record from step two.
6.  Select **Ready to assess**.

 Expected behavior: Deployment occurs under 2.5 mins.

 Actual behavior: Deployment takes 10.5 mins.

</td></tr><tr><td>

Resource Management

 PRB2032582

</td><td>

After changing the schedule, and performing edit, allocation dailies are not deleted on traditional resource plan

</td><td>

Bulk Extend using the using the **Extend** UI Action from the list context menu is not working. The date input is not getting updated on the resource plans.

</td><td>

1.  Create a resource plan for a user with a default schedule.
2.  Update the user schedule to MWF schedule.
3.  Edit the allocation records.

 Notice that the Tue, Thu hours are not being deleted.

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

 PRB2029429

</td><td>

There's a Zboot error due to a syntax error

</td><td>

There's an error: 'Error : \*\*\* ERROR \*\*\* invalid return \(&lt;refname&gt;; line 7\)'.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB2007579

</td><td>

User.hasPreciseRole\(\) incorrectly assumes User object represents the current session, causing role checks to fail in pre-login and non-session contexts

</td><td>

Any caller invoking user.hasRole\(\) or user.hasPreciseRole\(\) on a non-session User object receives an incorrect false result, silently failing role checks and causing access to be incorrectly denied or granted depending on how the result is consumed.

</td><td>

Pre-requisites:

 1.  A User record exists with role X assigned.
2.  The code under test calls user.hasRole\('X'\) on that User object.
3.  The call occurs in a pre-login context \(for example, login flow or ACR authentication\) where no GlideSession exists for that user.

 Steps to reproduce:

 1.  Trigger the ACR local login flow for a user who has the admin role but does NOT have sso\_config\_admin explicitly assigned.
2.  Execution reaches ACRUtil.isACRUserByUserID\(\) before session is established.
3.  Internally, call user.hasRole\(&lt;any\_role&gt;\) on the User object retrieved for the login candidate.

 Expected behavior: HasRole\(\) returns true, reflecting actual DB role membership.

 Actual behavior: HasRole\(\) returns false due to GlideSession short-circuit at User.java:3130 , session is not yet established at this point in the login flow.

</td></tr><tr><td>

Roles

 PRB2027465

</td><td>

Excessive user queries during 'role contains' insert/delete can cause increased upgrade times

</td><td>

There is also audit done in sys\_audit\_role table if glide.​role\_​management.​v2.​audit\_​roles is true which can also increase upgrade time significantly.

</td><td>

1.  Include a sys\_user\_role\_contains XML in a plugin where the child role has 40-50 contained roles.
2.  Have an instance where there are 16k users have the parent role.
3.  Upgrade the instance to a build with the stipulations in step one.

 Notice that the sys\_user\_role\_contains record will create 800k sys\_user\_has\_role records. There will be close to 1.6M read queries on sys\_user table made for 16k users.

</td></tr><tr><td>

Roles

 PRB2030872

</td><td>

Role mgmt v2 audit should be skipped during plugin and app install/upgrade

</td><td>

 

</td><td>

Create 5k users and assign a parent role, such as Admin.

 In sys\_audit\_role table, notice 30k audit records created for above sys\_user\_role\_contains which also adds more time for the plugin install to complete.

</td></tr><tr><td>

Scan Engine

 PRB2030265

</td><td>

Create a global family release plugin with prerequisite and setup track/impact

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Scan Engine

 PRB2030266

</td><td>

Update the global family release plugin

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1987001

</td><td>

Javascript globals are not available in the **Apply to** script field for advanced scripted relationships \(sys\_relationship\)

</td><td>

After creating a new sys\_relationship record, an error message occurs in the logs stating that the 'table\_name' is not defined.

</td><td>

1.  Create a new scope and a new table.
2.  Create a new relationship \(sys\_relationship\) record with the following configuration:
    1.  Name: Created by
    2.  Advanced: true
    3.  Applies to table: New Scoped Table
    4.  Apply to: gs.debug\('Table Name: ' + table\_name\);
3.  Open the New Scoped Table form.
4.  Right click and navigate to **Configure** &gt; **Related Lists**.

 Notice that when checking the system logs, the following error message occurs: 'com.​glide.​script.​Rhino​Ecma​Error:​ 'table\_name' is not defined. : Line\(1\) column\(0\) ==&gt; 1: gs.debug\('Table Name: ' + table\_name\); Stack trace: at :1.'.

</td></tr><tr><td>

Server-side scripts

 PRB1996400

</td><td>

Update ACLs for the sys\_es\_latest\_script table

</td><td>

 

</td><td>

1.  Navigate to the 'sys\_es\_latest\_script' table record.
2.  Ensure that all ACLs have the new ACL role attached to them: 'sys\_es\_latest\_script\_admin'.

 Expected behavior: There are 5 ACL roles that should be present in the related tables of the table record.

 Actual behavior: There are no ACL roles in the related tables of the table record.

</td></tr><tr><td>

Server-side scripts

 PRB2022324

</td><td>

Logging for all sandbox scripts is broken

</td><td>

 

</td><td>

Execute a script in the sandbox.

 Observe that it should be logged, but isn't.

</td></tr><tr><td>

Server-side scripts

 PRB2033661

 [KB3094262](https://hi.service-now.com/kb_view.do?sysparm_article=KB3094262)

</td><td>

There's different behavior of 'instanceof Array' between Zurich and Australia

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Server-side scripts

 PRB2034671

</td><td>

Static methods of String such as String.trim are broken in Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB2035844

</td><td>

An apparent scope stack corruption leads to global code running under an app scope

</td><td>

 

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

ServiceNow MCP Server Security

 PRB2050682

</td><td>

The token claim and metadata endpoints reflect a static instance URL instead of instance host

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2016794

</td><td>

Skip delete issue for 'Coalsce' tables

</td><td>

When a Fluent app defines a role, the SDK generates a new sys\_id. The existing ScopeConflictDetector keys off sys\_update\_name \(which encodes the sys\_id\), and finds nothing in sys\_metadata, so no conflict is flagged. The installer then coalesces onto the real global admin role by matching the name field and silently overwrites its sys\_scope, stealing a system-owned record into the app's scope.

</td><td>

1.  Navigate to IDE.
2.  Create a fscoped Fluent app.
3.  Create a role with the name as 'admin'.
4.  Build and install.

 Expected behavior: The Global role shouldn't be overridden.

 Actual behavior: The Global role is overridden.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2023227

</td><td>

FluentXMLLoader does not process the uploaded XML files according to their dependency order

</td><td>

Duplicate sys\_update\_xml getting create for views when uploaded via FluentXMLLoader.

</td><td>

1.  Create a fluent configuration project.
2.  Create a new form with a couple sections and a custom view.
3.  Install the configuration project.

 Observe that the sys\_update\_xml for view is duplicated.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2027930

</td><td>

Installing SDK-built app with ChoiceSet deletes existing instance choices not included in the app payload

</td><td>

When installing a ServiceNow SDK application that defines choices for a field using the ChoiceSet API, existing choices on the target instance that are not explicitly included in the application payload may be removed during installation. This can result in unintended loss of choice values that were previously configured on the instance.

</td><td>

1.  On a target instance, confirm that the task.priority field has base system choices \(for example, 1 - Critical, 2 - High, 3 - Moderate, 4 - Low, 5 - Planning\)
2.  Using the ServiceNow SDK, create a scoped app that defines a ChoiceSet for task.priority with only a subset of choices \(for example, only values 1, 2, and 3\).
3.  Build the app using now-sdk build.
4.  Install the built app on the target instance.
5.  After installation, inspect the choices for task.priority

 Expected behavior: Only the three choices defined in the app are added or updated. All other existing instance choices \(4 - Low, 5 - Planning\) remain untouched.

 Actual behavior: All existing choices for task.priority are deleted and replaced with only the three from the app. Choices 4 and 5 are lost.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2032877

</td><td>

The loader should save DB serialized XML in an update set instead of the original XML payload

</td><td>

The original XML payload is retained.

</td><td>

1.  Create a config project.
2.  Customize and upload the changes.

 Expected behavior: Updateset to contain DB serialized XML.

 Actual behavior: Retain the original XML payload.

</td></tr><tr><td>

Software Asset Management Content Service

 PRB2021862

</td><td>

Minor changes to styles on the UI page for content set up to match latest UI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Foundation plugin

 PRB2021740

</td><td>

New property categories

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2010303

</td><td>

Unable to Add software products in the Software Asset Management \(SAM\) workspace in published products list

</td><td>

The issue is caused by the maximum allowed size for a gzipped scripted REST request body, which is default set to 1MB.

</td><td>

1.  Navigate to **All** &gt; **Software Asset Management Workspace** &gt; **License operations**.
2.  From the SAM Implementation list, select **Published products**.
3.  Select **Add**.
4.  In the Add to published products dialog box, select the desired licensable software products.
5.  Select **Add** to publish them.

 Expected behavior: The selected products should be successfully added to the Published products list.

 Actual behavior: The products do not publish. The list remains unchanged after selecting Add, even after multiple attempts.

</td></tr><tr><td>

Software Asset Management

 PRB2017405

</td><td>

There's a missing fix script to update the label of cmdb\_model\_lifecycle

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2017767

</td><td>

Uptake of the setValueWithIdentify platform fix to update AI highlighted values

</td><td>

Identify AI updated fields and differentiate them from a non-AI user update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Publisher Pack for Oracle

 PRB2026881

</td><td>

Wallet authentication support for discovery patterns for Oracle on the Unix part of Software Asset Management plugin

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reclamation

 PRB2008233

</td><td>

Potential savings on reclamation candidates should be set regardless of licensing status

</td><td>

It should be set for both licensed and unlicensed subscriptions/installs.

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2015647

</td><td>

There's a null point error \(NPE\) in SamMSInfraLicReportGenerator

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2021614

</td><td>

Potential savings on reclamation candidates should be set regardless of licensing status

</td><td>

It should be set for both licensed and unlicensed subscriptions/installs. A software's license status doesn't impact the potential savings for removing that software. The reclamation candidate should reflect the cost of having that software installed.

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2024886

 [KB3043462](https://hi.service-now.com/kb_view.do?sysparm_article=KB3043462)

</td><td>

Recon for subscriptions fails with: 'TypeError: Cannot read property 'unlicensedSubscriptionCnt' from undefined''

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Entitlements

 PRB2023513

</td><td>

Add an asset tag, agreement number, and location to entitlement duplicate check attributes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Lifecycles

 PRB2014527

 [KB3018548](https://hi.service-now.com/kb_view.do?sysparm_article=KB3018548)

</td><td>

Custom lifecycle phases cause errors in Software Asset Management \(SAM\)

</td><td>

The 'SAM - Generate Software Lifecycle Report' job may show as 'Failed' for Zurich users who have added custom choices to the phase column on the 'sam\_sw\_product\_lifecycle' table. Supported phases are: pre\_release, availability, upgrade, end\_of\_support, end\_of\_extended\_support, end\_of\_life. Any added phases may cause errors.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

SQL API \(Server\)

 PRB1966907

</td><td>

DBSQL Parser changes are not working properly for ODBC/JDBC applications

</td><td>

 

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2007066

</td><td>

Check to correct Legacy and Delegated Flow Engine jobs that are created during Upgrade

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2030366

</td><td>

Thread pool for fast lane – flow event processing

</td><td>

This is a product update.

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

System Export Sets

 PRB2002031

</td><td>

Export to Excel from the UI with glide.​excel.​use\_​user\_​date\_​format set to true does not export in UTC date time

</td><td>

When exporting to Excel/XLSX from the UI with 'Export using raw values' enabled, Date/**Time** fields are not exported in UTC as documented.

</td><td>

1.  In a Zurich instance, set the property glide.​excel.​use\_​user\_​date\_​format to true and set the user to a timezone different than PST.
2.  List a table from the UI and include a column of type date time.
3.  Export to Excel.

 Observe that the date time field does not show the expected UTC0.

</td></tr><tr><td>

System Export Sets

 PRB2014333

</td><td>

ACL rules with JavaScript referencing non-displayed dot-walked data during twoPassQuery\(\) can result in partially constructed GlideRecords that lack the needed data

</td><td>

When users run an ordered two-pass query and then subsequently next\(\) through the records, the code today if users request a dot-walked field with an ACL on resolve the dot walk to mostly empty \(not read from the database\) GlideRecords to represent the data in the dot-walks. Typically, the sys\_id of the GlideRecord is present, but not much else.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2034836

</td><td>

Telemetry for Action Fabric

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Tables and Columns Data Dictionary

 PRB2015281

 [KB3035672](https://hi.service-now.com/kb_view.do?sysparm_article=KB3035672)

</td><td>

Dependent choices filter on a session domain instead of a record domain

</td><td>

When glide.​sys.​domain.​use\_​record\_​domain\_​for\_​choice\_​list is true, the choice list resolution through GlideElement.getChoices\(\) is expected to filter choices based on the record's domain instead of the session domain. This works correctly for non-dependent choice fields. However, dependent choice fields \(for example, subcategory, which depends on category\) filter based on the session domain, ignoring the record's domain — even when the property is enabled. This means when a global user accesses choices on a record belonging to a child domain, the category returns the correct domain-specific choices, but the subcategory returns global choices or nothing.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2019038

</td><td>

Credentials containing org level projects.list role cause total interval failure

</td><td>

When the GCP Trace Collector uses a service account with org-level project listing permission but trace/log access only for some projects, the collector fails the entire pipeline on the first unauthorized project. This causes the circuit breaker to trigger and results in data loss, even for projects where access is valid.

</td><td>

1.  Create a GCP service account.
2.  Grant an org/folder-level role that includes resourcemanager.projects.list \(for example, roles/browser\).
3.  Grant Cloud Trace / Logs permissions to only one project.
4.  Configure and run the GCP Trace Collector with this service account.

 Expected behavior: Skip only the projects where trace access is missing. Continue fetching traces from projects with valid permissions. Do not fail the entire pipeline due to partial access.

 Actual behavior: Projects are listed successfully and trace fetch starts, but on the first unauthorized project a PERMISSION\_DENIED error occurs. Circuit breaker triggers and the interval is skipped.

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2030648

</td><td>

The Azure Application Insight throws an error

</td><td>

During testing of the Application Insight feature, users are intermittently seeing an error: 'Unable to find app\_insights\_config.json'.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2035153

</td><td>

Support AWS CloudWatch traces for a custom agent running on any ADK and OpenTelemetry instrumentation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2039605

</td><td>

GCP spans are not correctly formatted to receive trace scoped evaluator metrics from Traceloop

</td><td>

For Azure, the gen\_ai.provider.name span attribute does not exist which prevents Traceloop from scoring the spans.

</td><td>

Send traces from a GCP agent.

 Observe the scores in sn\_ai\_observe\_ai\_span are missing metrics from trace-scoped evaluators \(agent-goal-deviation, agent-system-prompt-leakage, privileged-access-detector, observed-access-detector\).

</td></tr><tr><td>

Transaction Management

 PRB2031636

</td><td>

When a semaphore is loaded via plugin extension point, the queue depth limit is set wrong and the semaphore's load\_stats saturation value will always report 1 instead of the correct value

</td><td>

The saturation value should not always be one because saturation should reflect the amount of work queued in CsHybridQueue.

</td><td>

1.  Navigate to any A+ instance that has the CsHybridQueue sys\_semaphore\_set records.
2.  Navigate to instanceUrlHere/load\_stats.do.

 Observe that the saturation value of CsHybridQueue is always one.

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

 PRB1962677

</td><td>

Text in string fields in a modal window are cut off under certain conditions in Safari

</td><td>

When using the Safari web browser, there are certain conditions that result in text in a string field being cut off from displaying. These include the amount of text in the string field and the size of the web browser window. The result is a string field where the user has to select their cursor in and move down with the arrow keys to read all of the text in the string field.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2009135

</td><td>

There is a filter anomaly on Affected CIs

</td><td>

The filter is applied on the initial load, but not when the configuration class is changed.

</td><td>

1.  In a base Zurich instance, replace line 49 of the script include.

Notice the number of records for the configuration class 'software', along with the above filter in the platform list view.

2.  Navigate to **Service Operations Workspace \(SOW\)**.
3.  Open any active incident.
4.  Navigate to **Related Records** &gt; **Affected CIs** &gt; **Add**.
5.  Change the configuration class to 'Software'.

 Expected behavior: The records are returned along with the additional filter added in the script include.

 Actual behavior: The user will see all the records with the class 'software' are returned without the additional filters on the install status, and manufacturer is added in the script include.

</td></tr><tr><td>

UI Field Administration

 PRB2035410

</td><td>

Reduce DB load on sys\_ai\_record\_activity \( Perf\)

</td><td>

Tracking should impose a negligible background DB load.

</td><td>

1.  Enable AI Record Activity tracking \(glide.​ai.​field\_​indicators.​enabled\)​ on an instance with active AI Agent traffic.
2.  Drive normal insert/update/delete volume on non-system tables \(and AI writes to AI logging tables\).

 Observe sys\_query\_pattern / Splunk over a ~10h window.

</td></tr><tr><td>

UI Field Administration

 PRB2037047

</td><td>

AI indicators for a skill update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2020457

</td><td>

There's a false error for a strict read-only 'Currency' column when the numeric value is 1000 or larger

</td><td>

Additional formatting like commas or decimals are added to **Currency** fields on the client side form initialization, which makes the field appear as modified on update.

</td><td>

1.  On any table, create a field of the type **Currency**.
2.  Create an on insert business rule to set the value of the field to USD: 1000.
3.  Save the record.
4.  Modify a different field on the form and save.

 Expected behavior: The record is updated without any error messages.

 Actual behavior: An error message stating updates to columns 'depreciated\_amount' and 'residual' were ignored.

</td></tr><tr><td>

Upgrade Center

 PRB2040287

</td><td>

AutoUpgrade sn-managed applications on customer instances using periodic batch installs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB2040289

</td><td>

AutoUpgrade sn-managed applications changes on glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1893217

</td><td>

The way workspace tabs and their **Remove** buttons are grouped into lists is not clear

</td><td>

 

</td><td>

1.  Open any workspace like Service Operations Workspace or HR Agent Workspace from 'Workspaces' menu.
2.  Navigate to a list from the left tab panel.
3.  Select a few items to open a number of workspace tabs.
4.  Turn on the screen reader.
5.  Navigate on these tabs with forward \(tab key\) and backward \(shift +tab key\) navigation.
6.  Notice what the screen reader reads at workspace tab items and their **Remove** buttons.

 Expected behavior: The way workspace tabs and their**Remove** buttons are grouped into lists should be clear for screen reader users.

 Actual behavior: The way workspace tabs and their**Remove** buttons are grouped into lists is not clear for screen reader users.

</td></tr><tr><td>

UX Framework

 PRB1981765

</td><td>

'Max Tab Reached' dialog card is not closing on select of **Close dialog** button \(**X** button\)

</td><td>

On selecting the **Close dialog** button \(**X** button\) the 'Max Tab Reached' dialog card doesn't close.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1990613

</td><td>

A stale Interaction Record sysID is passed for the help request modal component

</td><td>

This issue is caused when a modal is opened from the utility panel. The utility panel gets hoisted from the screen to the appshell and loses the context of the screen. When the first utility panel gets hoisted, there's no issue because the modal logic falls back to the first matching element with the modal component ID. When an additional screen with a utility panel is opened, and an action is taken to open a new modal, the context of the screen is lost and the modal fallback logic is executed.

</td><td>

1.  Create 2–3 interactions of type Phone and refresh the workspace page so the Active Call component loads in the utility panel.
2.  Open **Developer Tools** &gt; **Console**.
3.  Select the iframe hosting the workspace and execute the Active Call payload to simulate the call context \(replace SYSID with the interaction sys\_id\).
4.  Open Interaction A in Tab 1 and select **Request Help**.
5.  Open Interaction B in a new tab and select **Request Help** again.
6.  Navigate to the interaction\_help\_request table and verify the record.

 Observe that the Help Request is created/updated for Interaction A \(previous tab\) instead of the active interaction \(Interaction B\).

</td></tr><tr><td>

UX Framework

 PRB2012962

</td><td>

GET\_ACTION\_STATE intent silently fails when no action bars are found

</td><td>

In getTranslatorBehavior.js, the INTENT\_RECEIVED handler for GET\_ACTION\_STATE operations retrieves action bars via getActionbarsForTranslator. If the result is an empty array, the forEach loop never executes and no intent feedback is sent. This leaves the intent sender waiting indefinitely with no indication of success or failure.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2018044

 [KB2993927](https://hi.service-now.com/kb_view.do?sysparm_article=KB2993927)

</td><td>

If sys\_attachments is excluded during cloning, UXF pages aren't loading correctly after cloning

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB2019867

</td><td>

Cleanup UXR event listeners

</td><td>

UXR event listeners persist in detached elements after DOM removal, bloating JS heap and Blink GC oil pan heap, eventually leading to memory issues, compounded with other component issues.

</td><td>

1.  Navigate to SOW.
2.  Open 10 incidents.
3.  Close the incidents.
4.  Repeat this three times.
5.  Open the browser dev tools.
6.  Retrieve a heap snapshot.

 Notice the detached elements.

</td></tr><tr><td>

UX Framework

 PRB2020890

</td><td>

Properly disconnect sn-canvas components to prevent memory leaks

</td><td>

Multiple module-scoped resources in the canvas framework were not being cleaned up when components disconnected, causing memory and listener counts to grow across navigation/tab-close cycles.

</td><td>

1.  Navigate to Service Operations Workspace.
2.  Open 10 tabs.
3.  Close 10 tabs.
4.  Get a JS heap dump.
5.  Inspect the detached elements.

 Notice the screen action transformers and other UXR components have a large retained size.

</td></tr><tr><td>

UX Framework

 PRB2020895

</td><td>

Cleanup viewports and now-trigger-library memory leaks

</td><td>

Four memory leaks in library-uxf and now-trigger-library: duplicate/orphaned popstate+locationchange listeners, unpruned ComponentRegistry entries, retained per-nowId cache buffers, and a strong lastClickedElement reference holding a detached DOM node alive.

</td><td>

1.  Navigate to SOW \(base instance instance\)
2.  Open 10 incident tabs close the 10 tabs

 Observe that memory usage is high. Take a JSheap dump and inspect the retainers of detached elements.

</td></tr><tr><td>

UX Framework

 PRB2026005

</td><td>

UXF should let the inbox know when the workspace is not the active experience

</td><td>

Currently, when the agent navigates from workspace to home, the Inbox is still present in the DOM. Because of this, agents are still assigned work items even when they are not in the workspace.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2029831

</td><td>

June release survey doesn't match the design

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2030213

</td><td>

When a user navigates between two pages that both have IPS surveys configured, the survey triggered on the first page isn't dismissed upon navigation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2032793

</td><td>

Network Inventory AppBU Survey Configuration is incorrect

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2033952

</td><td>

GLOBAL\_NAVIGATION\_REQUESTED is not routing to feature on select after hard refresh of the page apart from home page

</td><td>

The GLOBAL\_NAVIGATION\_REQUESTED payload feature is undefined. Without a feature defined in the payload, no navigation will occur.

</td><td>

1.  Navigate to SOW and Enable Desktop Notifications in the Agent Chat.
2.  Make an agent self available.
3.  From a different, incognito browser window, log in to the instance in question and navigate to instance/esc.
4.  Select the chat icon in the bottom right, start a new chat, and select **Live agent support**. Do not select the global navigation notification yet.

From the original browser tab, observes an incoming chat \(don't select it\).

5.  In the filter navigator, select **All** &gt; **Incidents**.
6.  On the incidents page, perform a hard reload \(must be a hard reload\).
7.  Select the Desktop Notification for global navigation.

 Expected behavior: The user is navigated back to the workspace screen where the notification originated from \(in this case, SOW chat\).

 Actual behavior: The user is not navigated back to the workspace.

</td></tr><tr><td>

UX Framework

 PRB2035481

</td><td>

Two extra loading tabs are visible after selecting a desktop notification

</td><td>

Two extra loading tabs are visible in workspace after selecting a desktop notification.

</td><td>

1.  Navigate to SOW and Enable Desktop Notifications in the Agent Chat.
2.  Make an agent self available and trigger a chat with the agent.
3.  Select the home page.
4.  Refresh the home page.
5.  When incoming work item appears for the agent, select the desktop notification.

 Expected behavior: The user is navigated back to the workspace screen where the notification originated from, and workspace should not have extra loading tabs.

 Actual behavior: Two extra loading tabs visible in workspace after selecting a desktop notification.

</td></tr><tr><td>

Virtual Agent

 PRB1980327

</td><td>

A chat dynamic greeting isn't localized correctly

</td><td>

Because the message doesn't go down the correct API path to resolve to sys\_ui\_message, and it can't honor the dynamic greeting.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1999511

</td><td>

Message preview and unread badge count don't work upon page refresh

</td><td>

When the user refreshes the page, the message preview doesn't show up. On standard chat, there's also no unread badge count.

</td><td>

1.  Navigate to /sp.
2.  Query 'What is spam'.
3.  While standard or enhanced chat is processing, close the VA.

Observe that there is an unread badge count \(1\) and the message preview pops up.

4.  Refresh the page.

 Expected behavior: There is still an unread badge count and the message preview shows up.

 Actual behavior: The message preview doesn't show up. On standard chat, there's also no unread badge count.

</td></tr><tr><td>

Virtual Agent

 PRB2007156

 [KB2928656](https://hi.service-now.com/kb_view.do?sysparm_article=KB2928656)

</td><td>

An Asynchronous Message Bus \(AMB\) subscription to 'after guest elevates to consumer account' returns a 403 error to the chat session

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2013952

</td><td>

Remove the deprecate system property 'com.​glide.​cs.​conversation.​entity.​cache.​enabled'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2014676

</td><td>

Honor hideShowControl for text inbound controls

</td><td>

 

</td><td>

Trigger text inbound.

 See an empty card instead of text inbound control.

</td></tr><tr><td>

Virtual Agent

 PRB2015460

</td><td>

Now Assist Portal's unread conversation count disappears after the execution is started via AI Agent triggers or Runtime APIs

</td><td>

The unread conversation count over the NAP icon on the menu bar disappears.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2019099

</td><td>

Starting '\{0\}' sys\_cs\_context\_profile\_message isn't translated per user session language

</td><td>

The message should be translated using SysMessage.getMessageLang before it's sent.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2020334

</td><td>

glide-cs unit test failures in Yokohama

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2021983

</td><td>

Null GlideRecord in conversation context causes IllegalArgumentException during deserialization in TypedValueDeserializationUtil

</td><td>

Typed​Value​Deserialization​Util.​get\(\)​ crashes with IllegalArgumentException when deserializing a null GlideRecord value stored in conversation context by the AI Search fallback topic.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2022716

</td><td>

NextWave Premium Chat doesn't work for external users \(snc\_external\) on CSM portal

</td><td>

The console error '403 FORBIDDEN' appears on ais\_auth\_token\_refresh API. The external user can't use the chat experience.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2024316

</td><td>

Stuck Virtual Agent conversations from FDIH async\_search race condition cause infinite retry loop consuming worker threads

</td><td>

When Virtual Agent invokes an AI search via FDIH \(global.async\_search\), a race condition in the callback handler can silently drop the search result if another thread updates the same conversation simultaneously. This leaves the conversation's task data in an incomplete state — the FDIH invocation started but never completed.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2024809

</td><td>

Handshake process does not end impersonation, which could cause session issues

</td><td>

Impersonation should not continue if the user is locked out.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2025956

</td><td>

Resolved issues after introducing four tables for Virtual Agent \(VA\) analytics

</td><td>

The search-related analytics can be written to the four tables instead of sys\_ci\_analytics as event entries.

</td><td>

1.  Make sure sn\_​nowassist\_​va.​analytics.​persistence\_​strategy = 'table'.
2.  Launch VA client.
3.  Type anything in the search.

 Observe that all the expected entries are in the new tables and view.

</td></tr><tr><td>

Virtual Agent

 PRB2026053

</td><td>

sys\_cs\_context\_profile\_topics should be sent to the offGlide cache for Authorizing Official \(AO\) to read

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2028137

</td><td>

Glide-cs-test failures in Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2029447

</td><td>

Knowledge article links are broken in the sources citation when the article has an attachment

</td><td>

There is an issue with the link formation in the source citations for the KB article if there is an attachment. The link generated by Now Assist uses the sys\_id of the PDF attachment instead of the KB article sys\_id in the URL.

</td><td>

1.  Navigate to **/esc**.
2.  Impersonate a user.
3.  Initiate a conversation in Now Assist with the query, 'Are there any KB articles about job abandonment, when an employee stops showing up for work?'.

Observe that the generated content is sourced from the 'Missing Persons Standard Operating Procedure' attachment in KB0083268.

4.  Open 'Sources and More', then hover over the source related to POL0021842-2.0 'Missing Persons Standard Operating Procedure.pdf'.

 Observe the link formation.

</td></tr><tr><td>

Virtual Agent

 PRB2031672

</td><td>

Non-topic skills dropped from skill picker when all applicable topic skills have a visible design category

</td><td>

Conversation insights attempts to perform a lookup against sys\_cs\_message with sequence which fails due to a sequence change.

</td><td>

1.  Configure the Virtual Agent topic to use GroupedPartsOutputControl.
2.  Have conversations using this topic, and then have inferred-csat generated for the conversation.

 Observe that during this process, transcript generation fails with an error.

</td></tr><tr><td>

Virtual Agent

 PRB2031950

</td><td>

AI-user fetch issue

</td><td>

The conversation user for the ZTSD flow is AI L1 Service Desk Specialist, which is the identity type ai\_agent. The cache configuration get\_​user\|table:​\{table\}​\|field:​\{field\}​\|value:​\{value\}​ explicitly ignores users of type 'ai\_agent'.

</td><td>

Perform a cache fetch call for the cache key 'get\_​user\|table:​\{table\}​\|field:​\{field\}​\|value:​\{value\}​' for any user of the identity type 'ai\_agent'.

 See that it doesn't return the **User** field value.

</td></tr><tr><td>

Virtual Agent

 PRB2032726

</td><td>

Topic execution fails intermittently during automation

</td><td>

Nextwave playwright test automation runs several conversational tests on NAP. The topic execution fails intermittently during the execution.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2033217

</td><td>

A topic template navigates to a different page where there is no premium chat visible

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2033400

</td><td>

vaSystem.getTranscript\(\) returns empty when Dynamic Translation is turned on and messages are in the 'Pending' or 'Translating' status

</td><td>

The issue is in ConversationTranscriber.java lines 383-388: when Dynamic Translation for Virtual Agent is turned on and a single message has a 'Pending' or 'Translating' status, the entire transcript is discarded \(returns empty list\) because forceTranscript is hardcoded to false all the way from jsFunction\_getTranscript\(\). The chat summary topic script then sends an empty transcript to the LLM, which hallucinates a description.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2033535

</td><td>

CSP Pre-Chat Survey not displayed in Premium Chat \(NextWave\) experience on CSP portal

</td><td>

The Pre-Chat Survey should be displayed at the start of the chat session in the Premium chat experience, consistent with the Enhanced chat experience. However, the Pre-Chat Survey is skipped entirely in the Premium chat experience. The chat starts with a generic greeting and the user is expected to type their request, with no pre-classification flow.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2033881

</td><td>

Executing a catalog item or a skill from searched results fails silently after canceling the live agent request

</td><td>

Canceling the live agent before the agent accepts results in the catalog item execution silently failing, and the user is left with at \_empty\_skill\_picker\_ topic. This issue was found in Service Operations Workspace \(SOW\).

</td><td>

1.  In one browser, sign on as live agent.
2.  Make the live agent available for agent chats in SOW.
3.  In another browser or in an incognito window, start a chat as a different user \(for example, System Admin\).
4.  Select **Contact an agent** from the menu or type 'live agent'.
5.  As the chat requester, cancel the live agent transfer before the agent accepts.
6.  Perform a search that will result in conversational catalog results \(for example, 'order a laptop'\).
7.  Select **Start Request** on one of the catalog items.

 Expected behavior: The catalog item starts and is completed successfully.

 Actual behavior: The catalog item execution fails silently, leaving the user with the at \_empty\_skill\_picker\_ topic.

</td></tr><tr><td>

Virtual Agent

 PRB2034790

</td><td>

The user is able to discover agents even though the sys property value is 'false'

</td><td>

 

</td><td>

1.  Set sn\_​aia.​enable\_​aiagents\_​discovery to 'false'.
2.  Open Now Assist panel \(NAP\).
3.  Enter, 'Show me list of agents.'

 Notice that no agents are discovered or executable on NAP.

</td></tr><tr><td>

Virtual Agent

 PRB2036293

</td><td>

AI closing messages are not supported in chat experiences

</td><td>

Chat experience can't display AI-generated closing messages when configured.

</td><td>

1.  Install the latest Now Assist VA plugin.
2.  As an admin, navigate to the chat experience configuration screen.
3.  Attempt to configure an AI closing message and select **Save**.

 Expected behavior: The user can save ai\_closing message configuration successfully.

 Actual behavior: The user can't save because ai\_closing type is not recognized by the backend.

</td></tr><tr><td>

Virtual Agent

 PRB2037059

</td><td>

Guest user conversation history is not visible after logging in as an authenticated user

</td><td>

When a guest user chats with the Virtual Agent on the ESC portal and then logs in, their conversation history is not transferred to their authenticated account. Instead, a new empty conversation is created for the logged-in user and the guest conversation history is lost from their view. The expected behavior \(per design\) is that the guest conversations appear in the authenticated user's Active chat history immediately after login.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2037309

</td><td>

All auto chat conversations share the same conversation because the channel user profile reuse ignores channelUserId

</td><td>

All auto chat records reference the same conversation.

</td><td>

1.  Configure a channel with a provider application that supports bot-to-bot / auto chat conversations.
2.  Trigger multiple auto chat conversations for the same user on that channel, each with a unique channelUserId passed in the AI agent context.
3.  Wait for all auto chat executions to complete.
4.  Open the auto chat records and inspect the conversation field on each record.

 Expected behavior: Each auto chat record has a unique conversation.

 Actual behavior: All auto chat records reference the same conversation — the one tied to the first channel user profile found for that user on that channel.

</td></tr><tr><td>

Virtual Agent

 PRB2038004

</td><td>

AMB subscription to after guest elevates to consumer account returns 403 to chat session

</td><td>

Conversation messages appear to be delayed. This is because the sync API is being used instead of AMB subscription.

</td><td>

1.  Enable a guest for NAVA Enhanced Chat on /esc.
2.  Open NAVA as guest with the 'Network' tab open.
3.  Log in and resume conversation.

 Expected behavior: AMB subscription should occur to /cs/auxiliary and /cs/messages. Messages to and from VA should occur on the AMB subscription.

 Actual behavior: AMB subscription fails with 403 to /cs/auxiliary and /cs/messages. Conversation continues using cs\_message API instead of AMB subscription.

</td></tr><tr><td>

Virtual Agent

 PRB2038142

</td><td>

In order for users to adopt NAVA, OGCS should do parity with an onglide version of va​System.​send​Skill​Picker​Control

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2038143

</td><td>

In order for users to adopt NAVA, OGCS should do parity with an onglide version of va​System.​send​Skill​Picker​Control

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2039532

</td><td>

getInstanceKeys scriptable method is missing from glide-plugins-members.xml

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2039580

</td><td>

vaContext object isn't available in the **Applicability** field of a Virtual Agent topic

</td><td>

The user observes the error 'Script evaluation error at \[topic\_Generate epics from capability\_applicability\]'.

</td><td>

1.  Open a record from the table 'x\_snc\_pm\_product\_feature' and create a new chat in NASS.
2.  Confirm that the topic 'Generate epics from capability', which should be conditionally available for this table, is not present.

 Observe the error 'Script evaluation error at \[topic\_Generate epics from capability\_applicability\]'.

</td></tr><tr><td>

Virtual Agent

 PRB2040084

</td><td>

Current action payload sends conversational and is\_conversational which is redundant

</td><td>

 

</td><td>

1.  Create an enhanced chat Employee Center experience in an instance.
2.  Navigate to esc portal.
3.  Use the assistant to 'Order an iphone'.
4.  In the instance Navigate to 'sys\_generative\_ai\_log.list' table and sort be recently created.
5.  Look for Unified planner response.

 The response should include is\_conversational as a param and no other param like 'conversational' should be included.

</td></tr><tr><td>

Virtual Agent

 PRB2041409

</td><td>

The vaContext object isn't available in the **Applicability** field of the Virtual Agent topic

</td><td>

An error occurs in the logs and the topic is not present, even though it should be conditionally available for the table.

</td><td>

1.  Log in to the instance.
2.  Open a record from the table 'x\_snc\_pm\_product\_feature'.
3.  Create a new chat in Now Assist for Request \(NASS\).
4.  Confirm that the topic 'Generate epics from capability', which should be conditionally available for this table, is not present.

 Notice the error in the logs, 'Script evaluation error at \[topic\_Generate epics from capability\_applicability\] ReferenceError: 'vaContext' is not defined. \(sys\_​cs\_​topic.​6db146b993f6f610b2f9f60f2603d678;​ line 9\)'.

</td></tr><tr><td>

Virtual Agent

 PRB2050001

</td><td>

Capture 'Sorry, there was a problem' error count on on-glide server

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2050011

</td><td>

NextWave Premium Chat doesn't work for external users \(snc\_external\) on CSM portal

</td><td>

The user observes, '403 FORBIDDEN' on ais\_auth\_token\_refresh API.

</td><td>

1.  Invoke the OGCS chat kit from the Virtual Agent API.
2.  Pass the Primary Bot History in the payload.

 Observe that the Primary Bot History column is empty in the sys\_cs\_message table for the conversation.

</td></tr><tr><td>

Virtual Agent

 PRB2051507

</td><td>

Capturing the 'Sorry, there was a problem' error count on the on-glide server

</td><td>

A baseline measurement of the error frequency on the glide surface is needed.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2032099

</td><td>

New Chat contains messages from the old chat

</td><td>

If the user is on a chat and selects the **+** button, it starts a new chat and shows the content of the previous chat as well.

</td><td>

1.  Start a new chat from NAVA.
2.  Transfer to a live agent.
3.  When the chat ends, immediately select the **+** button.

 The new chat shows messages from the previous closed chat.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2033755

</td><td>

SEARCH\_FALLBACK\_EVENT is missing in sys\_ci\_analytics

</td><td>

SEARCH\_FALLBACK\_EVENT records are no longer created in sys\_ci\_analytics in Australia.

</td><td>

1.  Navigate to Dynamic Window.
2.  Create a conversation.
3.  Start a conversation.
4.  Search for 'iPhone'.
5.  Select **See more of iPhone**.
6.  Navigate through the conversation without starting a catalog request.
7.  End the iPhone search conversation with 'nothing else'.

</td></tr><tr><td>

Word Document APIs

 PRB2029404

</td><td>

Table data is lost in the Word document after sending for signature

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Enter Word doc API with the wrong URL.

 Observe that fallback doesn't occur in a 404 case.

</td></tr><tr><td>

Work Order Management

 PRB2027565

</td><td>

DWS 'Sort by' skills degraded in Australia

</td><td>

The 'Sort by' skill runs slowly.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included in Australia Patch 4m

These prior versions contain PRB fixes that are also included with Australia Patch 4. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 3 Hot Fix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3104013)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)
-   [Australia Patch 2 Hot Fix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3101088)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

## Store app versions included in Australia Patch 4m

<table id="table_zfc_nvb_zjc"><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

@servicenow/sn-ai-engagement-experience

</td><td>

3.4.7

</td><td>

AI In-Product Experience \(AIIPEX\) - Key Deliverables

 Led modernization of the AI In-Product Experience platform by migrating core Agentic AI experiences from legacy implementations to the Lit/AIX Widget architecture, including Agent Status Cards, Agentic Presence, Agentic Processes, Supervision, Review Cards, and Conversation Transcript components.

 Established the Lit development foundation through local development tooling, Fluent widget compilation pipelines, and standardized migration patterns, enabling faster future modernization efforts. Improved accessibility compliance and responsive design support across all Lit-based widgets to deliver a consistent enterprise experience across device sizes.

 Enhanced Agentic AI workflows by introducing persona-aware input validation, workflow supervision improvements, contextual follow-up support, visibility into previous agent outputs, and user feedback collection capabilities. Delivered rich interaction features including planner controls, file uploads, copy-to-clipboard actions, notifications for input-required workflows, and enhanced review/output experiences with markdown rendering and improved content presentation.

 Completed a strategic modernization initiative aligned with the Lit and Fluent design system architecture, improving scalability, maintainability, performance, and future development velocity.

 Quality, Stability, and Security Improvements

 Delivered critical fixes across AI Engagement Experience and AI In-Product Experience, resolving issues related to link rendering, conversation context conflicts, input-required workflows, output review functionality, agent sidebar interactions, and multi-conversation session management.

 Improved Agentic AI workflow reliability by correcting incident context detection, workflow restart behavior, process visibility permissions, and UI Builder component exposure. Enhanced conversational continuity across AI Engagement Launcher, Now Assist Search, and Agentic AI experiences.

 Strengthened platform security through dependency upgrades, vulnerability remediation, and role inheritance corrections. Improved localization and internationalization support through standardized translation handling and message management.

 Resolved API and data presentation issues including date/time localization inconsistencies, customer configuration challenges, workflow visibility problems, chat header customization defects, and integration issues across LitJS, Seismic, NextWave, and AI Engagement Experience components.

 Enhanced platform stability, upgrade readiness, and customer adoption by addressing workflow automation defects, Canvas fix script issues, Agentic Process execution problems, and numerous customer-reported issues across Agentic AI, Now Assist, and AI-powered workflow experiences.

</td></tr><tr><td>

@servicenow/sn-enhanced-content-editor

</td><td>

31.24.0

</td><td>

Defect for the editor fixed.

</td></tr><tr><td>

Admin Center

</td><td>

6.1.3

</td><td>

New

 PoCs to explore LitJS and AIUX \(Horizon 2.0\) for Admin Home redesign/uplifts.

 Fixed

 GA defect fixes.

</td></tr><tr><td>

Agentic Contact Center for Insurance

</td><td>

1.2.2

</td><td>

Changed

 Agentic Contact Center for Insurance has been modernized for ServiceNow's Now SDK \(Fluent\), updating how the app is packaged and built. Existing functionality is unchanged.

</td></tr><tr><td>

AI Agent Advisor

</td><td>

1.2.2

</td><td>

New

 -   Enhanced error detection and pre-execution data validation. AI Agent Advisor verifies that required data is present before running, with clearer error reporting when it is not.
-   Updated out-of-the-box agent catalog improves matching recommendations for automation opportunities.

 Changed

 Nothing changed in this release.

 Fixed

 -   Resolved an issue where POV extraction failures could halt the mining pipeline. Records without an extracted root cause are now included in clustering, improving resilience.
-   Resolved a platform issue where mining runs were overloading the LLM backend leading to reduced throughput. Pipeline scheduling now staggers executions to improve LLM call batching and load distribution.

 Removed

 Nothing removed in this release.

</td></tr><tr><td>

AI agents and skills for Quote Management

</td><td>

3.0.1

</td><td>

Initial version of Quote AI agent.

</td></tr><tr><td>

AI Agents for AIOps

</td><td>

1.10.0

</td><td>

New

 Implemented secure-by-default configurations for the 5 new agentic ACLs.

 Fixed

 The autonomous workflow has been updated to support AWS Claude as an AI agent provider, resolving compatibility issues and enabling seamless integration.

</td></tr><tr><td>

AI Agents for Discovery

</td><td>

3.2.1

</td><td>

Multi-Rule Firewall Tasks.

 You can now add multiple rule configurations to a single firewall task, eliminating the need to create separate tasks for each rule. Available through both the AI agent and service catalog, this enhancement reduces administrative overhead and accelerates firewall rule deployment. Rules are automatically verified and created together as part of the same task, ensuring consistency across your firewall management process and improving operational efficiency.

</td></tr><tr><td>

AI Agents for Health and Safety

</td><td>

1.3.4

</td><td>

-   Resolved issue where the Health and Safety agentic workflow was not triggered after an incident was assigned to a user.
-   Eliminated repeated responses in the Health and Safety Incident Pattern Detector AI agent.

</td></tr><tr><td>

AI Agents for ITAM

</td><td>

4.4.0

</td><td>

Starting this version, the Asset Summary displays each linked change request once, eliminating duplicate entries.

</td></tr><tr><td>

AI agents for Observability

</td><td>

6.1.4

</td><td>

Changed

 Improved system performance.

</td></tr><tr><td>

AI Agents for Service Exchange Provider

</td><td>

1.1.4

</td><td>

Connections tab in the Service Exchange Center.

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding.

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities.

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements.

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting.

 Group-based persona assignments for Remote Catalog.

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

</td></tr><tr><td>

AI agents for Synthetic Monitoring

</td><td>

1.4.4

</td><td>

-   Safer batch monitor creation: Batch operations now handle failures more gracefully. If an error occurs during bulk creation, the system recovers automatically and rolls back failed items-so you don't lose work.
-   Better validation upfront: Input validation now catches issues before they cause problems, reducing failed operations and rework.
-   More dependable recommendations: Recommendation tracking is now more reliable. State updates complete successfully even when errors occur, and orphaned records are automatically cleaned up during bulk deletions.
-   Faster monitor queries: Query performance improvements reduce lag when selecting monitor locations, even in large CMDB environments.
-   Improved security: Access controls for the Synthetic Creator agent have been tightened to follow security best practices-limiting permissions to only what's needed.

</td></tr><tr><td>

AI Asset Management

</td><td>

5.0.3

</td><td>

In this version, the following enhancements have been made:

 -   Asset type selection now requires explicit user input when creating a new AI System Intake, giving you greater control over asset classification.
-   Modal messages in the change request flow have been optimized for improved clarity.
-   Translations for string literals have been enhanced to provide better support for global users.
-   The Next button on the intake form is now always visible, providing consistent navigation even when the sidebar is pinned.
-   The 'Managed by' field now preserves user input throughout the intake form completion, ensuring data consistency and reducing re-entry.

</td></tr><tr><td>

AI Case Management

</td><td>

22.4.2

</td><td>

New

 Generate responses to assessment questions based on past assessments and reference documentation on AI Case Management.

</td></tr><tr><td>

AI Control Tower

</td><td>

6.0.0

</td><td>

New

 -   Assign unique asset IDs for each asset.
-   Opt-in to model preview program.

 Changed

 -   Post-upgrade fix: Auto-flag existing active assets as 'Managed' for AICT Enterprise SKU customers upgrading from pre-March release.
-   Simplified asset state and status values - replaces lifecycle states.

</td></tr><tr><td>

AI Control Tower Core

</td><td>

7.6.4

</td><td>

New

 -   Assign unique asset IDs for each asset.
-   Opt-in to model preview program.

 Changed

 -   Post-upgrade fix: Auto-flag existing active assets as 'Managed' for AICT Enterprise SKU customers upgrading from pre-March release.
-   Simplified asset state and status values - replaces lifecycle states.

</td></tr><tr><td>

AI Control Tower for Enterprise AI Foundation

</td><td>

1.2.1

</td><td>

New

 Now Assist powers new agentic and Gen AI capabilities in AI Risk and Compliance, providing built-in regulatory alignment and ethical AI governance for responsible deployment.

 Changed

 All Now Assist skills are now integrated with the latest third-party models for Claude, Gemini, and ChatGPT. This enables better performance and broader compatibility across your AI workflows.

</td></tr><tr><td>

AI Control Tower for Now Assist

</td><td>

5.0.2

</td><td>

New

 -   Assign unique asset IDs for each asset.
-   Opt-in to model preview program.

 Changed

 -   Post-upgrade fix: Auto-flag existing active assets as 'Managed' for AICT Enterprise SKU customers upgrading from pre-March release.
-   Simplified asset state and status values - replaces lifecycle states.

</td></tr><tr><td>

AI Dashboard Insights

</td><td>

1.2.3

</td><td>

New

 -   Improved Summary generation accuracy and performance.
-   Improved error messages displayed to the users.

 Fixed

 -   The NACM components embedded inside tabs fails, when no Experience is associated.
-   Component title is not reflecting in grid component.
-   Missing ACL for Dashboard Summary Skill.
-   What Changed summary logic is comparing the facts even when metadata is changes.

</td></tr><tr><td>

AI Data Explorer

</td><td>

5.1.6

</td><td>

New: Delivered support for automated indicators in AI Data Explorer. You can ask questions or add to AI Data Explorer any data visualization based on an automated indicator.

</td></tr><tr><td>

AI Desktop Actions

</td><td>

5.0.1

</td><td>

New

 Unified automation workflow - Create automations seamlessly across Task Mining, Automation Center, AI Agent Studio, and AI Desktop Actions in a single integrated journey, eliminating context switching and streamlining automation development.

</td></tr><tr><td>

AI Desktop Actions Core

</td><td>

5.0.1

</td><td>

New

 Unified automation workflow - Create automations seamlessly across Task Mining, Automation Center, AI Agent Studio, and AI Desktop Actions in a single integrated journey, eliminating context switching and streamlining automation development.

</td></tr><tr><td>

AI Enhanced Recommended Actions

</td><td>

1.0.3

</td><td>

New

 Switches the default LLM provider to AWS Claude for the Now Assist skills.

</td></tr><tr><td>

AI Experience Framework Builder

</td><td>

1.2.2

</td><td>

New

 Widget editor

 Support for new karuna runtime.

 Dashboard editor

 Preview the canvas by user / role.

 Fixed

 Widget editor

 Defect fixes.

 Dashboard editor

</td></tr><tr><td>

AI Experience Framework Components

</td><td>

1.2.2

</td><td>

Fixed translation issues.

 Defect fixes

 -   Fixed unused icon import in knowledge\_article component.
-   Fixed greeting component rendering when aiux-chat-wrapper is present.
-   Fixed padding issue in Knowledge and Catalog item pages.
-   Resolved activity-stream component 400% zoom display issue.
-   Scoped empty-state-message and state-illustration widgets in sn\_aiux\_components for better component isolation.
-   Enhanced ai-response-card to properly handle HTML content as summary.
-   Readied the app for fluent enablement.

</td></tr><tr><td>

AI Experience Framework Components for Now Assist Setup

</td><td>

1.2.1

</td><td>

Fixed

 -   Fixed translation issues.
-   Fixed styling issues on the Additional theme page.
-   Fixed an issue where assets are not loaded in the Additional page when an existing theme record is selected.
-   Readied the app for fluent enablement.

</td></tr><tr><td>

AI Experience Framework Skills

</td><td>

1.2.0

</td><td>

Fixed

 -   Fixed translation issues.
-   Ready the app for fluent enablement.

</td></tr><tr><td>

AI Help Framework

</td><td>

1.0.6

</td><td>

New

 -   Native integration with AI experiences.
-   AI-powered help generation engine.

</td></tr><tr><td>

AIOps Agentic Workforce

</td><td>

2.1.0

</td><td>

Fixed

 -   The autonomous workflow has been updated to support AWS Claude as an AI agent provider, resolving previous compatibility issues.
-   Alert Investigation insight prompt limitation on length is extended.
-   Improving results for the Impact Agent search for related issues.

</td></tr><tr><td>

AIOps Experience

</td><td>

27.2.7

</td><td>

Changed

 -   Express List accessibility improvements. The Express List is now fully accessible to users with low vision, expanding the user base and ensuring compliance with international accessibility standards and regulations.
-   Consolidated ACLs for access control management. Access control lists have been consolidated to better follow security best practices, reducing risks and simplifying management.
-   Link View topology visualization accessibility. Link View topology visualization now meets accessibility standards while maintaining usability and performance.

 Fixed

 -   The Express List layout has been corrected to properly adapt for narrow viewports and no longer breaks at certain screen sizes.
-   Unintended double scrollbars in accessibility reflow mode have been eliminated.
-   The Express List columns now display correctly in Japanese and CJK languages, resolving translation and layout issues.
-   The Express List live list functionality now properly triggers and updates in real time.
-   The 'update available' banner no longer appears incorrectly when resuming the live list.
-   Saving an Alert Management Rule with 'Create Incident Advanced' now works in all scenarios.
-   Operators with more than five assignment groups can now see their created Enrich automations in the Enrich module.
-   Alerts manually removed from a group are no longer automatically re-added.
-   A broken documentation link in the alert automation configuration has been fixed.
-   Dynatrace Monitor setup instructions in the Launchpad have been updated to match the current Dynatrace console.
-   The 'Tags' label in the Launchpad is now correctly translated across contexts.
-   Concatenated strings causing grammatical issues in certain languages have been separated for correct localization.
-   Launchpad forms now match the approved design at 400% zoom.
-   Dotted connection lines in Link View now appear when connected CIs are returned from the backend.
-   The Simulation UI now displays 'This automation' or the saved automation name instead of 'MIXED' or 'CMDB' labels for Mixed or CMDB group types.
-   The 'All Time \(Last 180 days\)' option now shows as selected in the time range picker and is correctly translated.
-   Service health percentages now display correctly in locales using a comma as the decimal separator.
-   Ellipsis menu items in the Log Viewer now display in the user's language setting.
-   Backspace behavior in Extended mode is now correct.
-   The evt\_mgmt\_admin role now has write access to Express List properties.

</td></tr><tr><td>

AI Risk and Compliance Integration with Control Tower

</td><td>

22.4.2

</td><td>

New

 -   Create and document governance, risk, and compliance issues with guided assistance from the employee center.
-   Generate concise summaries of complex GRC issues for faster review and decision-making.
-   Generate summaries of risk assessments to communicate insights to stakeholders.
-   Generate responses to assessment questions based on past assessments and reference documentation.
-   Identify related control objectives from your controls library to reduce duplication.

</td></tr><tr><td>

AI Risk and Compliance Management

</td><td>

22.4.1

</td><td>

New

 -   Create and document governance, risk, and compliance issues with guided assistance from the employee center.
-   Generate concise summaries of complex GRC issues for faster review and decision-making.
-   Create executive summaries of risk assessments to communicate findings to stakeholders.
-   Generate responses to assessment questions based on past assessments and reference documentation.
-   Identify related control objectives from your controls library to reduce duplication.

</td></tr><tr><td>

AI Specialists for Security Incident Response

</td><td>

1.0.5

</td><td>

This is the Restricted Access release of the T2 SOC AI Specialist within the AI Specialists for Security Incident Response app. The specialist is now ready for SOC teams looking to augment Tier 2 analyst capacity with autonomous AI-driven investigation and response.

 What's included in this release:

 -   Full T2 SOC AI Specialist capability set.
-   Configurable onboarding and handover workflows.
-   Analyst summary and evidence generation.

</td></tr><tr><td>

Alert Assist

</td><td>

3.10.0

</td><td>

Changed

 -   Azure OpenAI is now the default model provider for AI skills and agents. Now LLM is no longer the default. Customers can choose the default and choose their own third-party providers.
-   Implemented secure-by-default configurations for the 5 new agentic ACLs.

 Fixed

 -   A formatting issue in alert analysis responses caused by the \` character has been resolved. HTML formatting in NAP now displays correctly.
-   The autonomous workflow has been updated to support AWS Claude as an AI agent provider, resolving compatibility issues and enabling seamless integration.

</td></tr><tr><td>

Analytics Generation

</td><td>

4.1.15

</td><td>

Fixed: Navigational bugs.

</td></tr><tr><td>

Analytics Toolkit

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

App AutoUpgrade Client

</td><td>

1.0.0

</td><td>

Initial release.

</td></tr><tr><td>

App Generation

</td><td>

28.3.12

</td><td>

Fixed

 Issue with support in Regulated Markets.

</td></tr><tr><td>

Applicant Center

</td><td>

8.0.2

</td><td>

No functional changes.

</td></tr><tr><td>

App Studio Commons

</td><td>

29.2.7

</td><td>

This app is a dependency of ServiceNow Studio + ServiceNow IDE. See the ServiceNow Studio + ServiceNow IDE listing for release notes.

</td></tr><tr><td>

App Summary

</td><td>

29.4.0

</td><td>

Fixed

 Disabled the existing Now LLM model and enabled the Google Cloud Vertex AI model.

</td></tr><tr><td>

Asset Audit Response

</td><td>

2.0.3

</td><td>

-   Track and manage impacted records that are associated with your remediation tasks.
-   Gain insight into the citations that are associated with your evidence requests.

</td></tr><tr><td>

ATF Test Generator and Cloud Runner

</td><td>

3.1.1

</td><td>

-   Added the role sn\_atf\_tg.cloud\_runner\_admin which allows users to set the cloud user and start test generations without needing the admin role themselves.
-   Added asynchronous option to Test Runner Rest API which returns the root tracker id and does not wait for the Browser Orchestration Queue record to be inserted.
-   Improved consistency of HTTP response codes to Cloud Runner Rest APIs.
-   Improved consistency of progress percentage for test runs in the Browser Orchestration Queue table.

</td></tr><tr><td>

Automation Center

</td><td>

15.0.1

</td><td>

Automate Task Mining tasks in Automation Center.

 Automation Center transforms task recordings from Task Mining, decomposes them into discrete automations, and generates an AI agent in AI Agent Studio that executes those automations using AI Desktop Actions.

 Automation Center analyzes Task Mining recordings and identifies discrete tasks-on-screen actions and background actions-eliminating manual analysis and reducing time-to-automation from hours to minutes.

 This multi-tool solution ensures that any repetitive task in Task Mining can be automated to be run as desktop actions.This feature currently supports only Excel-to-browser interactions, where data is copied from a Microsoft Excel file and is entered into a form in a browser.

 You must have the User Task Summarization skill and Now Assist AI Agents skill activated to use this feature.

 Task Mining recording and AI Desktop Actions agent execution require a Windows machine.For detailed information, see the Automation Center documentation.

 Kanban Board Enhancements.

 Create tasks from the Request board in Kanban board. Earlier, you could create tasks only from the Task Board in Kanban board. Also, there's a contextual panel to the right of the Kanban board that helps you create a task.

</td></tr><tr><td>

Build Agent \(Trial\)

</td><td>

2.4.5

</td><td>

New

 -   A new web search tool capability enabled Build Agent to find answers from the public internet when its internal knowledge sources don't have them. This tool needs to be toggled on from the settings screen of the Build Agent chat panel.
-   Consolidated update sets enable you to track changes generated by Build Agent and manual edits in consolidated update sets. All changes to your application are captured in the same scope, making it easier to review what was modified and merge updates to other environments.
-   Work with more metadata types in Build Agent, which now supports connection and credential alias, data lookup, rest message/HTTP method, and user criteria.

 Changed

 -   Developers can now see the complete history of changes in Build Agent conversations, including both automatic Build Agent updates and manual edits made in Studio. The system automatically creates separate 'manual-edit' update sets for manual changes between Build Agent installs, making it easy to distinguish which changes were automated versus hand-crafted. Restore to any point in your workflow, including manual edits between Build Agent prompts, and the system intelligently manages update set reconciliation to keep your change history clean and traceable.
-   Build Agent handles checkpoints and update sets differently: checkpoint 0 no longer creates an update set, checkpoint 1 is the base update set for all subsequent changes, and update sets use human-readable naming.
-   An updated semantic metadata search tool improves performance replaces the previous semantic search tool.

</td></tr><tr><td>

Build Agent Premium

</td><td>

1.4.1

</td><td>

New

 -   A new web search tool capability enabled Build Agent to find answers from the public internet when its internal knowledge sources don't have them. This tool needs to be toggled on from the settings screen of the Build Agent chat panel.
-   Consolidated update sets enable you to track changes generated by Build Agent and manual edits in consolidated update sets. All changes to your application are captured in the same scope, making it easier to review what was modified and merge updates to other environments.
-   Work with more metadata types in Build Agent, which now supports connection and credential alias, data lookup, rest message/HTTP method, and user criteria.

 Changed

 -   Developers can now see the complete history of changes in Build Agent conversations, including both automatic Build Agent updates and manual edits made in Studio. The system automatically creates separate 'manual-edit' update sets for manual changes between Build Agent installs, making it easy to distinguish which changes were automated versus hand-crafted. Restore to any point in your workflow, including manual edits between Build Agent prompts, and the system intelligently manages update set reconciliation to keep your change history clean and traceable.
-   Build Agent handles checkpoints and update sets differently: checkpoint 0 no longer creates an update set, checkpoint 1 is the base update set for all subsequent changes, and update sets use human-readable naming.
-   An updated semantic metadata search tool improves performance replaces the previous semantic search tool.

</td></tr><tr><td>

Case Playbook for Complaints

</td><td>

9.1.1

</td><td>

Changed

 -   Agentic activity Enhancements to support Research AI agent.
-   The show/hide the complaint case research agent activity is based on the research agent availability.

</td></tr><tr><td>

Chat Recommendation

</td><td>

1.8.3

</td><td>

Changed the default model to Azure.

 Fixed Truncation bugs.

</td></tr><tr><td>

Chat Summarization for Virtual Agent

</td><td>

1.11.4

</td><td>

Support 'Google Gemini' as the default model for Chat Summarization.

</td></tr><tr><td>

CMDB MCP Server

</td><td>

1.0.1

</td><td>

Initial release of ServiceNow CMDB MCP Server.

</td></tr><tr><td>

Coaching

</td><td>

9.9.0

</td><td>

1. New: These are new tables that will be in the coaching application:

 -   Quality metric type.
-   Quality metric category.
-   Quality metric category m2m.
-   Quality metric.
-   Quality metric results.

 2. Changed: .

 -   Updated coaching opportunity form.
-   Updated coaching assessment form.

 3. Fixed: N/A.

 4. Removed: N/A.

</td></tr><tr><td>

Collaborative Work Management - Advanced

</td><td>

2.0.5

</td><td>

Minor fixes.

 Removed

</td></tr><tr><td>

Complaint Case AI Agents collection

</td><td>

1.4.3

</td><td>

Fixed: VA Channel for Intake Agents are now opt-in instead of enabled by default, allowing customers to configure them only when needed.

</td></tr><tr><td>

Content library portal

</td><td>

4.1.1

</td><td>

Minor fixes around the product lifecycle during Content updates and content lookup historical data.

</td></tr><tr><td>

Content Pack for CMDB

</td><td>

2.0.1

</td><td>

Fixed

 Fix applied to the 'latest' field for base-system records in kb\_knowledge.

</td></tr><tr><td>

Contract Management Pro - Prime

</td><td>

1.0.11

</td><td>

New

 -   Signature workflows on the Docusign envelope now support adding signatories with different roles.
-   Resolution time for contract requests is now calculated automatically based on calendar duration and terminal state.

 Changed

 -   View the complete contract family hierarchy - including parent, sibling, and child contract requests - from the Related contract requests tab of the contract request.
-   Upload multiple supporting documents in a single action from your computer, activity stream, or external storage.
-   Upload supporting documents across any contract request state rather than a restricted subset of states.

 Fixed

 The contract administrator on a contract repository records is correctly assigned based on configured mapping rules.

</td></tr><tr><td>

Conversational Studio

</td><td>

10.0.3

</td><td>

RELEASE NOTES - Conversational Studio v10.0

 New

 -   Auto-Eval - Compare results across runs. Admins can now view and compare evaluation metrics across 2 to 5 runs \(table view, with an optional line graph\).
-   Auto-Eval - New metrics. Admins can now select and view Response Faithfulness and Response Fluency on the evaluation setup page.
-   LLM Topics and rarr; AI Agents migration tool. A new tool to convert LLM Topics into AI Agents \(spike work\), including building a dataset and running evaluations on the original Topic vs. the migrated Agent.

 Changed

 Asset accessibility - color contrast. Improved color contrast on Assets for better accessibility.

 Fixed

 -   Voice Assistant test button no longer fails to open the popup in the Assistant Designer cards view.
-   Migrated Topics on a non-global scope no longer cause Topic Block calls to be undiscoverable.
-   'Clone' auto-evaluation now works correctly.
-   Findability fields in conversational settings now save correctly.
-   Auto-Eval summary page no longer shows a false '0 completed' error when all scenarios actually ran.
-   Japanese translation on the Assistant Designer Home page no longer breaks due to text concatenation.
-   Untranslated timestamp / concatenation issue on the Assistant Designer Home page fixed.
-   Delete Assistant modal button order corrected.
-   Release build failure \(ERR\_PNPM\_GIT\_UNKNOWN\_BRANCH after the snc-app-parent 6.5.2.21 migration\) fixed.

 Removed

 None in this release.

</td></tr><tr><td>

Core Business Suite

</td><td>

3.2.7

</td><td>

 

</td></tr><tr><td>

Core Business Suite Advanced

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Advanced for Finance

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Advanced for Health and Safety

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Advanced for Human Resources

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Advanced for Legal

</td><td>

3.0.7

</td><td>

Updated to support the latest versions of the dependent apps.

</td></tr><tr><td>

Core Business Suite Advanced for Source to Pay

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Advanced for Workplace Services

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite AI Agent

</td><td>

3.2.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite for Finance

</td><td>

3.2.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite for Health and Safety

</td><td>

3.2.7

</td><td>

Removed the 'Assigned to Health and amp; Safety team' message that appears after a Health and Safety request is created on the Employee Center portal.

</td></tr><tr><td>

Core Business Suite for Human Resources

</td><td>

3.2.7

</td><td>

Defect Fix:

 Fixed the Now Assist skill mismatch on the product configuration console for Human Resources.

</td></tr><tr><td>

Core Business Suite for Legal

</td><td>

3.2.7

</td><td>

Updated to support the latest versions of the dependent apps.

</td></tr><tr><td>

Core Business Suite For Source To Pay

</td><td>

3.2.7

</td><td>

Fixed Now Assist skill mismatch the on the product configuration console for Source To Pay.

 Fixed supplier management breadcrumb and added the cancel button for Add Suppliers and Upload supplier page.

 Changed redirections after an invoice case is created to request detail page instead of category page on the Supplier Collaboration Portal.

</td></tr><tr><td>

Core Business Suite For Workplace Service Delivery

</td><td>

3.2.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Foundation

</td><td>

3.0.7

</td><td>

 

</td></tr><tr><td>

Core Business Suite Foundation for Finance

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Foundation for Health and Safety

</td><td>

3.0.7

</td><td>

Removed the 'Assigned to Health and amp; Safety team' message that appeared even without any assignment after a Health and Safety request is created on the Employee Center portal.

</td></tr><tr><td>

Core Business Suite Foundation for Human Resources

</td><td>

3.0.7

</td><td>

Defect Fix:

 Fixed the Now Assist skill mismatch on the product configuration console for Human Resources.

</td></tr><tr><td>

Core Business Suite Foundation for Legal

</td><td>

3.0.7

</td><td>

Updated to support the latest versions of the dependent apps.

</td></tr><tr><td>

Core Business Suite Foundation for Source to Pay

</td><td>

3.0.7

</td><td>

 

</td></tr><tr><td>

Core Business Suite Foundation for Workplace Services

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Prime

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Prime for Finance

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Prime for Health and Safety

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Prime for Human Resources

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Prime for Legal

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Prime for Source to Pay

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Prime for Workplace Services

</td><td>

3.0.7

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Cornerstone Spoke

</td><td>

1.6.0

</td><td>

Changed

 Migrated DEAPI \(Data Exporter API\) datastreams to OData Change Tracking for the Cornerstone HRSD integration, improving the reliability and efficiency of incremental data retrieval.

 Fixed

 -   Resolved an HTTP 415 error in the 'Create Assignment' action caused by a missing Content-Type header on the request.
-   Corrected the data type of the is\_latest\_reg\_num attribute in the 'Look up Transcripts From Data Exporter Data Stream' output, which now returns a Boolean value to match the Cornerstone API specification \(previously returned as an integer\).

</td></tr><tr><td>

CPQ for Manufacturing Advanced

</td><td>

1.2.0

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

CPQ for Manufacturing Foundation

</td><td>

1.2.0

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Critical Event Management

</td><td>

1.2.5

</td><td>

Fixed

 -   Hardcoded strings in the Critical Event Management dashboard within the Health and Safety Workspace were not displaying correctly in non-English locales.
-   A 'Do not show again' checkbox was missing from the 'Need Help' popup.
-   A duplicate Properties option appeared in the application properties configuration.
-   The Total Impacted list and loading bar intermittently became stuck.
-   Child critical events could be added to closed Critical Event Management records.

</td></tr><tr><td>

CRM Touchpoint

</td><td>

1.4.0

</td><td>

Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.

</td></tr><tr><td>

CSM - Advanced

</td><td>

2.0.1

</td><td>

Internal code updates with no impact to existing functionality or user-facing behavior.

</td></tr><tr><td>

CSM - Foundation

</td><td>

2.0.1

</td><td>

Internal code updates with no impact to existing functionality or user-facing behavior.

</td></tr><tr><td>

CSM MCP Server

</td><td>

1.0.4

</td><td>

Exposed gen AI capabilities through MCP server tools.

</td></tr><tr><td>

CSM - Prime

</td><td>

2.0.1

</td><td>

Internal code updates with no impact to existing functionality or user-facing behavior.

</td></tr><tr><td>

Customer Service Management AI agent collection

</td><td>

6.1.0

</td><td>

Optimized query routing for customer 360.

</td></tr><tr><td>

Data Foundation Model

</td><td>

1.11.0

</td><td>

New AI digital assets are now automatically assigned a unique, human-readable asset tag. Each tag follows the format of a type prefix followed by a hash value, where the prefix identifies the kind of asset, as listed here. Records that don't belong to one of these asset types are skipped and receive no tag.

 -   AIS - AI Systems.
-   AIM - AI Models.
-   AIP - AI Prompts.
-   AID - AI Datasets.
-   MCP - MCP assets.

 Tags are generated deterministically so that the same asset always produces the same tag. The value is derived from a stable identifier on the record, using the ServiceNow reference ID first, falling back to the external reference ID, and finally the record's own sys\_id if neither is present. That identifier is hashed using a 64-bit FNV-1a algorithm and rendered as a zero-padded 20-digit number, which is then combined with the type prefix. The tag is written back to the record without altering audit fields or re-triggering workflows, avoiding unnecessary updates and recursion.

 Tagging happens in two ways:

 -   New assets are tagged automatically by a business rule that fires immediately after the record is inserted.
-   Existing untagged assets are handled by an on-demand scheduled job that finds records with an empty asset tag and backfills them, logging its progress along the way.

</td></tr><tr><td>

Data Model for Order Management

</td><td>

16.4.0

</td><td>

New

 Supporting billing account on order line.

 Fixed

 Minor defects fixes.

</td></tr><tr><td>

DCNAM - Advanced

</td><td>

2.0.2

</td><td>

Agentic data center infrastructure allocation.

 AI interpretation of free-text change requests into structured parameters; autonomous policy- and capacity-aware allocation agent with full audit trail; policy management UI for DC planners \(6 policy types, dry-run mode\); three validators \(power, RU space, temperature\) that block bad allocations; rack visualization with clickable change-request traceability; a dedicated 4-stage 'DC Infrastructure Allocation' change model; and AIEL integration surfacing the agent in the NI workspace.

</td></tr><tr><td>

Document Intelligence for Contract Management Content Pack

</td><td>

1.5.0

</td><td>

Changed

 The default model provider for contract metadata extraction, contract analysis, and contract obligation extraction is Azure OpenAI.

</td></tr><tr><td>

Document Processor

</td><td>

1.8.6

</td><td>

New

 A new 'Specify document type' field has been added to the Document Verification Task, letting users indicate the type of document being verified.

</td></tr><tr><td>

Document Templates

</td><td>

29.0.1

</td><td>

Fixed: Bugs and Defects.

</td></tr><tr><td>

Employee Center

</td><td>

44.1.1

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Employee Profile

</td><td>

14.0.2

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Employee Slate Core

</td><td>

2.1.0

</td><td>

This release provides the following features and enhancements:

 -   Enhanced Org chart and profile with visual updates and profile image edits.
-   Introduced an option to configure a custom AI insights skill.
-   Introduced Home page widget configuration from the admin console, starting with Quick links.
-   Improved performance and accessibility support.
-   Updated the approval checklist skill default settings to on-demand to support upgrades.

</td></tr><tr><td>

Employee Slate for Now Assist

</td><td>

1.2.0

</td><td>

This release provides the following updates and enhancements:

 -   Enhanced Org chart and profile with visual updates and profile image edits.
-   Introduced an option to configure a custom AI insights skill.
-   Introduced Home page widget configuration from the admin console, starting with Quick links.
-   Improved performance and accessibility support.
-   Updated the approval checklist skill default settings to on demand to support upgrades.

</td></tr><tr><td>

Enhanced Features for IRM Enterprise

</td><td>

22.4.1

</td><td>

Changed

 Updated dependent plug-in versions to incorporate the default LLM model updates.

</td></tr><tr><td>

Enhanced Features for IRM Professional

</td><td>

22.4.1

</td><td>

Changed

 Updated dependent plug-in versions to incorporate the default LLM model updates.

</td></tr><tr><td>

Experimentation Framework Core

</td><td>

1.1.14

</td><td>

Internal app, external customers only have an Opt Out of the Framework button available to use and a read only view of live experiments on the instance.

</td></tr><tr><td>

External content connectors - Now assist agent

</td><td>

1.1.2

</td><td>

Fixed

 Dependency on Now Assist for Platform latest version.

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

4.2.1

</td><td>

Fixed

 Resolved an issue where the AI-generated recommendation was not set correctly.

</td></tr><tr><td>

Financial Services Operations Core

</td><td>

12.3.0

</td><td>

New

 A new field has been added to the Financial transaction table to capture additional transaction details.

 Fixed

 Tightened access security on financial transaction detail records by correcting query-range access controls, addressing identified security \(MSI\) issues.

</td></tr><tr><td>

Form data collector

</td><td>

2.2.1

</td><td>

Changed

 Form data collector has been modernized for ServiceNow's Now SDK \(Fluent\), updating how the app is packaged and built. Existing functionality is unchanged.

</td></tr><tr><td>

Generative AI Controller

</td><td>

14.1.2

</td><td>

New

 -   Extended support for new versions of third-party LLM provider models.
-   Introduced the Model Preview Program, giving customers early access to third-party model versions ahead of general availability for evaluation and testing.

 Removed

 Support for Long Term Stability\(LTS\) SKU.

</td></tr><tr><td>

GRC Common GenAI

</td><td>

22.4.0

</td><td>

Replaced Now LLM with Azure Open AI 5.4 mini model as the default model for all AI capability configurations.

</td></tr><tr><td>

GRC Shared GenAI

</td><td>

22.4.0

</td><td>

Now Assist skills now support the latest Claude, Gemini, and ChatGPT models, improving performance and compatibility across your AI workflows.

</td></tr><tr><td>

Group-Action Framework

</td><td>

7.1.1

</td><td>

New

 Enabling support Off-glide migration for GAF skills.

 Changed

 Updates to GAF clustering duration query to provide exact timestamp.

</td></tr><tr><td>

Hardware Asset Management - Advanced

</td><td>

1.0.2

</td><td>

This app is a subscription layer on Now Assist for HAM. This release updates Now Assist for HAM only; the Hardware Asset Management - Advanced app version remains unchanged.

</td></tr><tr><td>

Health and Safety - Advanced

</td><td>

1.0.6

</td><td>

Changed

 Version increment.

</td></tr><tr><td>

Health and Safety Case Management

</td><td>

6.2.2

</td><td>

Fixed

 Resolved a cross-scope access violation in the Attach HS Case Primary Ticket to UR Business Rule that prevented the Transfer and Create Associated Ticket buttons from appearing.

</td></tr><tr><td>

Health and Safety Components

</td><td>

12.1.2

</td><td>

Changed

 Version increment.

</td></tr><tr><td>

Health and Safety Contractor Management

</td><td>

5.2.2

</td><td>

Changed

 Version increment.

</td></tr><tr><td>

Health and Safety Core

</td><td>

13.2.2

</td><td>

Fixed

 -   Corrected hardcoded strings and date/time formats in the Health and Safety Workspace that did not adapt to non-English locales.
-   Resolved an issue where 'Link Documents' and 'Select Documents' action labels appeared untranslated on initial page load.
-   Prevented users from creating and linking Health and Safety actions to a restricted incident without the required access permissions.
-   Fixed an intermittent issue that prevented incident playbook triggers from firing.

</td></tr><tr><td>

Health and Safety - Foundation

</td><td>

1.0.6

</td><td>

Changed

 Version increment.

</td></tr><tr><td>

Health and Safety Incident Management

</td><td>

13.2.2

</td><td>

-   Resolved a scrolling issue in the Injury Details section that prevented the delete option for the last added injury from being reachable.
-   Restricted work notes on Health and Safety incidents from being visible to end users.
-   Prevented Risk Management ACLs from overriding involved party access.
-   Corrected the body part picker so that clicking the back of the hand now selects the correct body part instead of the palm of the hand.
-   Corrected Date of birth and Date of hire fields to populate correctly on exported OSHA 301 PDF form.
-   Resolved a cross-scope access violation in the Attach Health and Safety Case primary record to universal request business rule that prevented the Transfer and Create Associated Ticket buttons from appearing.
-   Enforced ACL checks on Health and Safety incident records for all applicable extension points.

</td></tr><tr><td>

Health and Safety Incident Management PA Content Pack

</td><td>

10.1.1

</td><td>

Changed

 Version increment.

</td></tr><tr><td>

Health and Safety - Prime

</td><td>

1.0.6

</td><td>

Changed

 Version increment.

</td></tr><tr><td>

Health and Safety Risk Management

</td><td>

9.2.2

</td><td>

-   Resolved an issue where the Approval Task Creator tool failed to read manager details when the application was installed.
-   Corrected the Health and Safety Ask attachment field to render as mandatory when configured as required on a Smart Assessment template question.
-   Resolved a timezone issue that caused the Inspection Schedule flow to run incorrectly for daily frequency schedules.
-   Resolved a 'Component not configured' dialog box error that appeared when scheduling audits.

</td></tr><tr><td>

Hiring Core

</td><td>

5.4.1

</td><td>

Minor updates to the data model supporting Hiring functionalities.

</td></tr><tr><td>

Hiring tab

</td><td>

8.0.1

</td><td>

No Functional updates.

</td></tr><tr><td>

HRSD - Advanced

</td><td>

2.1.0

</td><td>

Changed

 Plugin and content bundling has been updated for licensing.

</td></tr><tr><td>

HRSD - Foundation

</td><td>

2.1.0

</td><td>

Changed

 Plugin and content bundling has been updated for licensing.

</td></tr><tr><td>

HRSD - Prime

</td><td>

2.1.0

</td><td>

Changed

 Plugin and content bundling has been updated for licensing.

</td></tr><tr><td>

HR Service Delivery AI agent collection

</td><td>

7.1.1

</td><td>

Changed

 Agent permissions have been updated with revised access levels and new role-based restrictions to enhance security compliance and align with platform updates and regulatory requirements.

</td></tr><tr><td>

HR Talent AI Agent Collection

</td><td>

5.0.4

</td><td>

No Functional updates.

</td></tr><tr><td>

Human Resources: Service Portal

</td><td>

44.1.1

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Industrial Cyber Security Suite Prime

</td><td>

1.0.3

</td><td>

Fixed

 Fixed package.json dependency.

</td></tr><tr><td>

Insights Clustering Utils

</td><td>

3.2.2

</td><td>

New

 Nothing new in this release.

 Changed

 Internal improvements to clustering quality and reliability.

 Fixed

 Resolved an issue where missing group errors could occur during cluster prediction.

 Removed

 Nothing removed in this release.

</td></tr><tr><td>

Integrated Risk Management Advanced

</td><td>

22.4.0

</td><td>

Changed

 Updated dependent plug-in versions to incorporate the default LLM model updates.

</td></tr><tr><td>

Integrated Risk Management Foundation

</td><td>

22.4.0

</td><td>

Changed

 Updated dependent plug-in versions to incorporate the default LLM model updates.

</td></tr><tr><td>

Integrated Risk Management Prime

</td><td>

22.4.0

</td><td>

Changed

 Updated dependent plug-in versions to incorporate the default LLM model updates.

</td></tr><tr><td>

Interview management

</td><td>

4.0.2

</td><td>

No Functional updates.

</td></tr><tr><td>

IRM Compliance GenAI

</td><td>

22.4.0

</td><td>

Changed

 All Now Assist skills are now integrated with the latest third-party models for Claude, Gemini, and ChatGPT. This enables better performance and broader compatibility across your AI workflows.

</td></tr><tr><td>

IRM Risk GenAI

</td><td>

22.4.0

</td><td>

\[New\].

 Expanded Risk Event Summarization skill to support latest third-party AI models, including GPT‑5.4 mini, GPT‑5.1, and Gemini 3.5 Flash.

 \[Changed\].

 Updated Risk Event Summarization skill to use GPT‑5.4 mini as the default model, delivering enhanced AI capabilities and model improvements.

</td></tr><tr><td>

ITOM - Advanced

</td><td>

1.1.0

</td><td>

-   AI agent for Agent Client Collector \(ACC\) - Autonomously monitors ACC deployments across endpoints, ensuring agent health, version compliance, and seamless data collection without manual intervention, and provides guided troubleshooting experience.
-   AI agent for Discovery - Proactively tracks and renews digital certificates enterprise-wide, eliminating outages by auto-detecting expirations and creating firewall rules.
-   MID Guardian agent - Continuously monitors MID Server health and connectivity, providing guided troubleshooting of MID Server issues to resolve them seamlessly.
-   ITOM AI agent for Service Mapping - Intelligently discovers application dependencies and maps services to infrastructure, autonomously resolving gaps to keep service maps accurate and business-ready.
-   AI agent Topology Mapping - Discovery, classifies, and syncs AI agents deployed in cloud including the AI model metadata the agent deployed.
-   AIOps Learning Enhanced Automation Playbooks - Amplifies efficiency by mining historical incident data to generate dynamic resolution playbooks, automate workflows, and reduce MTTR.
-   ITOM URL Discovery - Discover URLs and SaaS applications from ITOM Browser Plugin .

</td></tr><tr><td>

ITOM AI Agents For Service Mapping

</td><td>

1.4.0

</td><td>

New

 Tag-Based Service Mapping AI Agent transforms cloud tags into validated, business-ready application services. This AI agent reads cloud tags and validates that tagged resources belong together. It improves the CMDB quality with built-in guardrails to catch noisy, inconsistent, or overly broad tagging schemes.

 Removed

 The MCP Server Service Mapping tools have been moved out of Service Mapping and now reside within the Now Assist CMDB MCP Server store app-though Service Mapping is still needed to use this capability.

</td></tr><tr><td>

ITOM Infra Services Workspace

</td><td>

2.0.3

</td><td>

New MID Server Onboarding Experience.

 New onboarding page in the ITOM Infra Services Workspace provides guidance through initial MID Server setup. The previous downloads page can be accessed via 'mid\_server\_download\_ui.do' if required.

 Command Line Installer for Windows and Linux \(for JWT Authentication\).

 -   The workspace now offers an automated command line installer that pre-configures your instance name, authentication, proxy, and other settings during installation.
-   The service account that will run on the MID Server needs to be specified on the MID Server host during installation.
-   Applications and capabilities must be assigned after the MID Server comes online and validates.

 Private Key JWT Authentication.

 -   Each MID Server gets authenticates with a unique certificate that automatically rotates every 45 days.
-   Migration from basic authentication to private key JWT can be done from the Auth-type migration tab on the MID Admin Workspace.
-   New MIDs can be setup to authenticate with JWTs through the above command line installer or manually via registration key in ITOM Infrastructure Services Workspace.
-   Currently available for standard cloud and on-prem instances. Regulated cloud and on-prem instances are not yet supported.

</td></tr><tr><td>

ITOM - Prime

</td><td>

1.1.0

</td><td>

ITOM - Prime provides the following capabilities:

 -   AI agents for AIOps - Automate alert triage, impact analysis, and root cause investigation with an AI-driven agentic workflow that transforms manual operator processes, typically 30+ clicks and 15+ minutes, into a streamlined, autonomous flow. The workflow processes incoming IT alerts end-to-end, correlating observability data, analyzing affected services, and identifying probable root causes before an operator touches the alert. Consolidated insights are surfaced through the Express List interface, giving operators immediate visibility into what happened, what's affected, and recommended next steps, enabling faster resolution while keeping humans in control of final decisions.
-   AI agents for Observability - Helps IT operators assess business and application service impact, formulate probable cause theories, and prioritize investigations by analyzing data from ServiceNow and seamlessly collaborating with third-party AI agents from leading APM and observability vendors, including New Relic, Dynatrace, and Kentik. Using natural language, IT operators can understand the blast radius of an alert, pinpoint affected services, assess business impact, formulate probable cause theories, and help track down the right teams to drive towards problem resolution.
-   AIOps Learning Enhanced Automation Playbooks - Leverages AI-driven insights to mine historical incident data, dynamically prioritize tasks, and generate actionable resolution playbooks. By automating workflows and enhancing knowledge sharing, AIOps Learning Enhanced Automation Playbooks empowers teams to address issues proactively and efficiently. It reduces mean time to resolution \(MTTR\), increases automation coverage, streamlines processes like certificate renewals, and improves team productivity. This ultimately leads to measurable cost savings and operational excellence.
-   AI agents for HLA - Automate the most complex and time-consuming steps in setting up and operating HLA - mapping business context, classifying log fields, and investigating alerts. Powered by Now Assist, these agents bring AI-driven recommendations directly into HLA workflows, reducing the expertise required to configure the system and helping operators respond to alerts faster and more confidently.
-   AI agents for SLO - Automates the creation of service level objectives \(SLOs\) based on operational data for services and configuration items \(CIs\), helping teams adopt SLOs faster and improve service reliability.

</td></tr><tr><td>

ITOM UI internal components

</td><td>

27.4.16

</td><td>

Fixed: Avatar presence on the Specialist onboarding flow.

</td></tr><tr><td>

IT Service Management

</td><td>

3.1.1

</td><td>

New

 -   Admin experience for Gmail inbound email configuration. The Product Configuration Console supports inbound email setup for Google alongside the ServiceNow account option.
-   Admin experience to manage and switch over to Employee Slate as primary engagement experience for Incident and Request Management notifications.
-   AI-assisted incident reassignment: routing logic that helps L1 agents pick the right L2 group to escalate to.

 Changed

 Admin experience Categorization and Routing agent enhancements. Minor functional refinements such as improving the accuracy of suggested categories, subcategories, and routing rules and the ease of configuring them.

 Fixed

 For fulfiller experience:

 -   Chat Reply Recommendation skill now includes the portal selection step during activation, closing the parity gap with Chat Summarization.
-   The Service Operations Workspace interaction record now shows both Transcript and Internal Transcript fields when both are added to the view.
-   The Related Records tab now shows Change and Problem fields for Prime and Advanced AI-Native IT Service Desk SKUs, and UI Action drop-downs are SKU-aware.
-   The VIP icon for the caller field now appears in the Record Information tab of the Service Operations Workspace side panel for custom Highlighted Value conditions.

</td></tr><tr><td>

IT Service Management Advanced

</td><td>

3.1.1

</td><td>

No changes.

</td></tr><tr><td>

IT Service Management AI agent collection

</td><td>

10.0.1

</td><td>

New

 -   AI Quality Assessment for the L1 AI Specialist - Automatically scores the AI Specialist's incident resolutions inside the Coaching application, so teams can measure resolution quality at enterprise volume and catch regressions instead of manually sampling.
-   Routing mode selector for Reassign tasks - A new out-of-the-box selector lets AI Admins choose Router \(recommended\) or Script for the AI Specialist without editing worker-template configuration.
-   In-form ticket deflection in Service Portal - An AI pipeline embedded in the ticket-creation form classifies intent, enriches context, retrieves knowledge, and suggests a resolution before a ticket is submitted.
-   Device remediation from ITSM workflows \(Intune and amp; Jamf\) - Agents can trigger endpoint remediation directly from Incident, Task, and Change without switching to external MDM consoles.
-   Toggle to enable/disable KFT creation - A new on/off control on the AI Specialist worker template governs whether a Knowledge Fulfillment Task is created when a resolution cites no knowledge article \(enabled by default\).
-   Specialized Resolutions onboarding in L1 Specialist Configuration - A new section where admins can discover every available SME AI Agent, view prerequisites and setup readiness, and enable or disable each one for the ZTS L1 Specialist flow.

 Changed

 -   Slow Computer SME AI Agents honor L1 Specialist Configuration - Agents now check enable, consent, and approval settings and read action details from the Remedial Action Framework before acting.
-   Zscaler and amp; SharePoint SME AI Agents honor L1 Specialist Configuration - The same configuration-aware behavior extended to these agents.
-   Routing-criteria analytics on the AIS Performance Dashboard - A new reassignment reason and per-criteria counts show when the AI Specialist reassigned an incident due to a routing-criteria match.
-   Remedial Action Framework extended to non-device actions - RAF now registers non-device actions \(e.g., SharePoint access, fulfillment flows, catalog items\) alongside device actions as the single action registry.
-   DEX performance tab extended to all ZTS AI Agent actions - Now reports both device and non-device action performance, with drill-down.
-   Richer AI Specialist work notes - Investigation and resolution work notes get consolidated formatting and clickable links to cited KB articles, similar incidents, and related records.

 Fixed

 Nothing was removed in this release.

 Removed

 Nothing was removed in this release.

</td></tr><tr><td>

ITSM Admin Experience

</td><td>

3.1.0

</td><td>

New

 -   Inbound email configuration for Gmail: The Product Configuration Console supports inbound email setup for Google \(Gmail\) alongside the existing ServiceNow account option. An admin can select a provider, complete the provider-specific configuration, and see the connected accounts in the inbound email accounts list with the correct source label.
-   Employee Slate notifications for Incident and Request Management.

 Changed

 -   Categorization and Routing agent enhancements: Minor functional refinements to the Categorization and Routing agents based on post-GA customer feedback, improving usability and accuracy without changing the core agent architecture.
-   For For XCC \(External Content Connector\), improvements to the AI Agent to support a NextWave-compatible experience.

 Fixed

 For XCC \(External Content Connector\):

 -   Agent prompt quality improvements.
-   Hallucination issues affecting AI Agent performance.

 Removed

 For XCC \(External Content Connector\), removed implicit dependency on the External Content Connector web crawler. The web crawler now needs to be installed explicitly as a soft dependency.

</td></tr><tr><td>

ITSM - Advanced

</td><td>

2.2.2

</td><td>

New

 In-form ticket deflection in Service Portal - An AI pipeline embedded in the ticket-creation form classifies intent, enriches context, retrieves knowledge, and suggests a resolution before a ticket is submitted.

 Changed

 -   Conversational Analytics dashboard \(Phase 2\) - Adds a topic detail page, Now Assist Data Explorer integration, standardized visualizations, and improved topics tables.
-   Default model change - Now LLM is no longer the default model for ITSM skills and agents; each now defaults to an optimal small third-party model \(large third-party models require approval\).

 Fixed

 Nothing was removed in this release.

 Removed

 Nothing was removed in this release.

</td></tr><tr><td>

ITSM Advanced Admin Experience

</td><td>

3.1.0

</td><td>

No changes.

</td></tr><tr><td>

ITSM Change Admin Experience

</td><td>

1.1.1

</td><td>

Fixed

 Enhanced the user interface for the Change models and Risk configuration pages.

</td></tr><tr><td>

ITSM Common Catalog Content

</td><td>

3.1.0

</td><td>

No changes.

</td></tr><tr><td>

ITSM Employee Experience

</td><td>

3.1.0

</td><td>

No changes.

</td></tr><tr><td>

ITSM - Foundation

</td><td>

2.2.3

</td><td>

New

 In-form ticket deflection in Service Portal - An AI pipeline embedded in the ticket-creation form classifies intent, enriches context, retrieves knowledge, and suggests a resolution before a ticket is submitted.

 Changed

 -   Conversational Analytics dashboard \(Phase 2\) - Adds a topic detail page, Now Assist Data Explorer integration, standardized visualizations, and improved topics tables.
-   Default model change - Now LLM is no longer the default model for ITSM skills and agents; each now defaults to an optimal small third-party model \(large third-party models require approval\).

 Fixed

 Nothing was removed in this release.

 Removed

 Nothing was removed in this release.

</td></tr><tr><td>

ITSM Fulfiller Experience

</td><td>

3.1.0

</td><td>

Changed

 AI-assisted incident reassignment: New routing logic helps L1 agents identify, reassign, and escalate an incident to the right L2 group or individual.

 Fixed

 -   Chat Reply Recommendation skill now includes the portal selection step during activation, closing the parity gap with Chat Summarization.
-   The Service Operations Workspace interaction record now shows both Transcript and Internal Transcript fields when both are added to the view.
-   The Related Records tab now shows Change and Problem fields for Prime and Advanced AI-Native IT Service Desk SKUs, and UI Action dropdowns are SKU-aware.
-   The VIP icon for the caller field now appears in the Record Information tab of the Service Operations Workspace side panel for custom Highlighted Value conditions.

</td></tr><tr><td>

ITSM - Prime

</td><td>

2.2.2

</td><td>

New

 -   AI Quality Assessment for the L1 AI Specialist - Automatically scores the AI Specialist's incident resolutions inside the Coaching application, so teams can measure resolution quality at enterprise volume and catch regressions instead of manually sampling.
-   Routing mode selector for Reassign tasks - A new out-of-the-box selector lets AI Admins choose Router \(recommended\) or Script for the AI Specialist without editing worker-template configuration.
-   In-form ticket deflection in Service Portal - An AI pipeline embedded in the ticket-creation form classifies intent, enriches context, retrieves knowledge, and suggests a resolution before a ticket is submitted.
-   Device remediation from ITSM workflows \(Intune and amp; Jamf\) - Agents can trigger endpoint remediation directly from Incident, Task, and Change without switching to external MDM consoles.
-   Toggle to enable/disable KFT creation - A new on/off control on the AI Specialist worker template governs whether a Knowledge Fulfillment Task is created when a resolution cites no knowledge article \(enabled by default\).
-   Specialized Resolutions onboarding in L1 Specialist Configuration - A new section where admins can discover every available SME AI Agent, view prerequisites and setup readiness, and enable or disable each one for the ZTS L1 Specialist flow.

 Changed

 -   Conversational Analytics dashboard \(Phase 2\) - Adds a topic detail page, Now Assist Data Explorer integration, standardized visualizations, and improved topics tables.
-   Default model change - Now LLM is no longer the default model for ITSM skills and agents; each now defaults to an optimal small third-party model \(large third-party models require approval\).
-   Slow Computer SME AI Agents honor L1 Specialist Configuration - Agents now check enable, consent, and approval settings and read action details from the Remedial Action Framework before acting.
-   Zscaler and amp; SharePoint SME AI Agents honor L1 Specialist Configuration - The same configuration-aware behavior extended to these agents.
-   Routing-criteria analytics on the AIS Performance Dashboard - A new reassignment reason and per-criteria counts show when the AI Specialist reassigned an incident due to a routing-criteria match.
-   Remedial Action Framework extended to non-device actions - RAF now registers non-device actions \(e.g., SharePoint access, fulfillment flows, catalog items\) alongside device actions as the single action registry.
-   DEX performance tab extended to all ZTS AI Agent actions - Now reports both device and non-device action performance, with drill-down.
-   Richer AI Specialist work notes - Investigation and resolution work notes get consolidated formatting and clickable links to cited KB articles, similar incidents, and related records.

 Fixed

 Nothing was removed in this release.

 Removed

 Nothing was removed in this release.

</td></tr><tr><td>

Journey designer

</td><td>

7.5.0

</td><td>

Switched default model from nowLLM to optimal small 3P model for HRSD skills.

</td></tr><tr><td>

Knowledge Capabilities in UI Builder

</td><td>

30.4.1

</td><td>

Defect - Service Operations Workspace 'More Actions' missing labels KB article Zurich patch 7.

</td></tr><tr><td>

Knowledge Center

</td><td>

31.11.3

</td><td>

No feature release, ECE defect.

</td></tr><tr><td>

Knowledge Graph

</td><td>

8.1.0

</td><td>

- Added support for glide list type support in Knowledge graph.

</td></tr><tr><td>

LEAP

</td><td>

4.1.0

</td><td>

New

 -   Autonomous AI Agent that scans incident clusters and automatically generates draft knowledge base articles and problem records based on configurable incident count and severity thresholds.
-   Agent-generated artifacts display with an AI icons on LEAP home page with hover cards linking to related records for visibility. The Action Insights panel on the automation opportunity details page of agent-generated artifact uses gradient styling.
-   Ansible Connector integration now available on LEAP Home page with dedicated help section.
-   Three new generative AI models now supported: Gemini 3.5 Flash, GPT 5.4 mini, and GPT 5.1.

 Changed

 Now LLM Service is no longer the default model provider for new or inactive AI assets. Third-party LLM is selected by default, while existing configurations using Now LLM service continue to remain unchanged and are available for manual selection.

</td></tr><tr><td>

Legal Counsel Center

</td><td>

2.3.3

</td><td>

Fixed

 -   Selecting 'Assign to me' button on legal requests displays error message when a request is already assigned.
-   The 'Start work' button on the request list on Legal Counsel Center home page now functions correctly.

</td></tr><tr><td>

Legal Request Management

</td><td>

10.2.0

</td><td>

New

 Resolution time for legal requests is now calculated automatically based on calendar duration and terminal state.

 Fixed

 -   Security fixes.
-   OneDrive permission issues fixed.
-   The milestone overdue message no longer appears when the associated due date is still in the future.
-   The Approvals tab in the ServiceNow Portal is visible to appropriate users.

</td></tr><tr><td>

Major Issue Management

</td><td>

4.1.0

</td><td>

Changed: Internal code updates with no impact to existing functionality or user-facing behavior.

 Fixed: Defect fix - When a Major Case is accepted via the 'Approve Major Case Candidate' UI action, the suggested child cases \(SMCs - cases whose suggested\_major\_case points at the candidate\) were not being promoted \(linked as children\) to the major case.

</td></tr><tr><td>

Manage Invoice Operations

</td><td>

1.1.2

</td><td>

Fixed

 -   The Invoice case voice agent helper subflow now runs as the user who initiates the session.
-   The subflow has been assigned the interaction\_Agent and sn\_csm\_invoice.writer roles to maintain its ability to update work notes and create interaction-related records.

</td></tr><tr><td>

Manufacturing Commercial Operations Advanced

</td><td>

1.2.0

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Manufacturing Commercial Operations AI agents collection

</td><td>

2.3.0

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Manufacturing Commercial Operations Foundation

</td><td>

1.2.0

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Manufacturing Commercial Operations Prime

</td><td>

1.2.0

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

MCP Client

</td><td>

1.0.2

</td><td>

- Scriptable MCP Client.

 - Performance optimization for getServers API.

 - Security defects fixed.

</td></tr><tr><td>

Metadata Search

</td><td>

1.0.12

</td><td>

Fixed

 Some bugs related to the Metadata Search Tool.

</td></tr><tr><td>

Microsoft Azure OpenAI Generative AI Spoke

</td><td>

3.12.2

</td><td>

-   New: Added support for sending additional headers in OEM actions.
-   Fixed: invalid content type validation that prevented OEM actions from processing PDF and file payloads.
-   Fixed: function call response handling for GPT models to properly send additional headers in OEM actions.

</td></tr><tr><td>

Microsoft Graph Security API Alert Ingestion Integration For Security Operations

</td><td>

10.5.5

</td><td>

Restored the buildInputValue function in the Graph Security API transform, fixing SIR fields being mapped as empty when a referenced source field is missing from the alert response.

</td></tr><tr><td>

MID Admin Workspace

</td><td>

2.0.1

</td><td>

New MID Server Onboarding Experience.

 New onboarding page in the ITOM Infra Services Workspace provides guidance through initial MID Server setup. The previous downloads page can be accessed via 'mid\_server\_download\_ui.do' if required.

 Command Line Installer for Windows and Linux \(for JWT Authentication\).

 -   The workspace now offers an automated command line installer that pre-configures your instance name, authentication, proxy, and other settings during installation.
-   The service account that will run on the MID Server needs to be specified on the MID Server host during installation.
-   Applications and capabilities must be assigned after the MID Server comes online and validates.

 Private Key JWT Authentication.

 -   Each MID Server gets authenticates with a unique certificate that automatically rotates every 45 days,.
-   Migration from basic authentication to private key JWT can be done from the Auth-type migration tab on the MID Admin Workspace.
-   New MIDs can be setup to authenticate with JWTs through the above command line installer or manually via registration key in ITOM Infrastructure Services Workspace.
-   Currently available for standard cloud and on-prem instances. Regulated cloud and on-prem instances are not yet supported.

</td></tr><tr><td>

MID Server Infrastructure

</td><td>

2.0.1

</td><td>

-   Added new tables and to support IPKI certificate lifecycle for MID Servers.
-   Added support for initial authentication of new MIDs using registration keys.

</td></tr><tr><td>

Mobile Builder AI

</td><td>

27.6.0

</td><td>

New

 Modified default model provider for card generation skill to gpt-5.4-mini.

</td></tr><tr><td>

Model Context Protocol Server

</td><td>

1.6.1

</td><td>

Performance Improvements, Third-Party IDP Support.

</td></tr><tr><td>

Notifications Email Agents

</td><td>

2.2.0

</td><td>

- Enhanced support for extracting inputs for subflow execution from inbound emails.

 Fixed

 - Improved similarity checks in the Notification agent.

</td></tr><tr><td>

Now Assist Admin Console

</td><td>

10.1.5

</td><td>

1.The Now LLM LTS \(Long-Term Stable\) model provider has been decommissioned and is no longer available in Now Assist Admin. This change affects the model provider selection surface, skill compliance messaging, and the model provider settings page.

 What has Changed: .

 -   Model provider selection - Now LLM LTS is no longer available as a selectable model provider when configuring skills or setting instance-level defaults. Administrators will no longer see Now LLM LTS in the provider dropdown.
-   Skill compliance messaging - Skills will no longer display out-of-compliance warnings related to Now LLM LTS. Any skill previously flagged as non-compliant due to Now LLM LTS provider assignment will no longer surface this alert.
-   Model provider banner Removed: The informational banner previously displayed on the Manage Model Providers page referencing Now LLM LTS compatibility and upgrade guidance has been removed.

 2.Deprecated Skills Section.

 Administrators can now view all deprecated Now Assist skills across products like ITSM,CSM and others in a dedicated section within the Now Assist Admin Console. This change provides full transparency into the skill lifecycle - including skills removed across products, skills replaced by newer versions, and skills that were available in a previous quarter but are no longer available in the current one.

 3.Common Skills Product Visibility.

 Administrators can now see all products associated with a Common skill directly on the Skills page in Now Assist Admin. Common skills - those that apply across multiple Now Assist products simultaneously - are now clearly identified and display the full list of products they support, giving administrators complete visibility before activation or configuration.

 A common skill will be mapped across multiple products,however its activation and deactivation can be done from any one individual product only.

</td></tr><tr><td>

Now Assist Agents for requestor

</td><td>

3.6.1

</td><td>

Approval checklist generation skill now supports passing the request body in place of the Approval ID.

</td></tr><tr><td>

Now Assist AI Agents

</td><td>

8.1.7

</td><td>

This release includes new capabilities and improvements across AI Agent Studio, including extensibility enhancements, memory improvements and security updates.

 Key features include:

 Security Improvements:

 Multiple updates to strengthen the security posture of agentic AI, including deny-by-default access controls and explicit ACL enforcement on new instances.

 Agent to Agent \(A2A\) 1.1 Upgrade:

 Agent-to-agent interactions upgraded from v0.3 to v1.1, with migration scripts and backward compatibility to improve multi-agent onboarding and reliability.

 Semantic Memory Redesign:

 Long-term memory no longer relies on predefined categories, reducing memory loss and improving the relevancy of memories surfaced during agent interactions.

</td></tr><tr><td>

Now Assist Analytics

</td><td>

5.1.2

</td><td>

New

 -   Conversational analytics agent for KPI exploration and explanation. Users can now interact with a conversational agent to retrieve, explain, and compare analytics KPIs, including metric definitions, data sources, retention periods, and custom calculations. The agent supports natural language queries, provides actionable recommendations, and maintains conversation context within sessions.
-   AI Analytics Q and amp;A skill integration and knowledge source expansion. The AI Analytics Q and amp;A skill now integrates a dedicated knowledge source covering domain configuration, release-wise major changes, and frequently asked case task resolutions. You can receive accurate answers to common questions and recent product changes directly from the skill.
-   The Overview, Business Value, and Executions pages \(Assistant and AI Agent tabs\) have been redesigned.
-   Business Value tab and benchmark creation modal have been redesigned for improved navigation and dynamic presentation lists.
-   The Assistants and AI Agent tabs in the Executions page have been redesigned to include pill-based filters, split-screen side panels, and agent-specific fields for tool calls and replay links.
-   Analytics Q and amp;A agent and workflow are now available for answering user questions about analytics metrics and dashboard data latency.
-   Skill for agent-based analytics Q and amp;A has been introduced: The skill can efficiently respond to analytics-related queries.
-   Automatic evaluation of AI Analytics Q and amp;A skill across providers: The system performs automated evaluations of the Q and amp;A skill using AWS Claude, Azure OpenAI, and Now LLM Service, with results available per provider.
-   Descriptions added to all formula indicators. All formula indicators in Now Assist Analytics now include descriptions detectable by the Q and amp;A skill, improving interpretability.

</td></tr><tr><td>

Now Assist Center

</td><td>

5.0.5

</td><td>

Minor enhancements and fixes.

</td></tr><tr><td>

Now Assist context menu

</td><td>

3.7.1

</td><td>

-   Update model provider default from Now LLM to OpenAI.
-   Some defect fixes.

</td></tr><tr><td>

Now Assist Data Kit

</td><td>

8.1.6

</td><td>

-   Data Creation updates - Data Kit Admins can now create a dataset with as few as 1 record \(reduced from 10\) and dataset names now support up to 200 characters.
-   Push to Table - Data Kit Admins can now push generated synthetic data directly to the respective target tables for Multi-table Data Generator requests \(advised for Sub Prod Environment\), using script assistance available within the Data Kit screen.

</td></tr><tr><td>

Now Assist for AIRC

</td><td>

22.4.0

</td><td>

New

 -   Users can now create and document governance, risk, and compliance issues with guided assistance from the Employee Center. Now Assist helps structure the issue and recommends relevant controls, entities, and policies based on the input provided. This ensures that the issue is well-defined and enriched with contextual information before it is submitted.
-   Use Now Assist to analyze the issue records, including the description, activity log, and remediation tasks, and generate a concise summary that captures the essential information needed.
-   Use Now Assist to identify redundant or overlapping control objectives and rationalize control objectives.
-   Use Now Assist to create a common control objective by summarizing duplicate control objectives from the rationalization process.
-   Use the Now LLM Service to generate risk assessment summaries from inherent, residual, and target risks and control effectiveness data. These summaries highlight key factors and relevant comments, helping assessors and approvers gain actionable insights.

</td></tr><tr><td>

Now Assist for Automation Center

</td><td>

1.2.4

</td><td>

Automate Task Mining tasks in Automation Center.

 Automation Center transforms task recordings from Task Mining, decomposes them into discrete automations, and generates an AI agent in AI Agent Studio that executes those automations using AI Desktop Actions.

 Automation Center analyzes Task Mining recordings and identifies discrete tasks-on-screen actions and background actions-eliminating manual analysis and reducing time-to-automation from hours to minutes.

 This multi-tool solution ensures that any repetitive task in Task Mining can be automated to be run as desktop actions.This feature currently supports only Excel-to-browser interactions, where data is copied from a Microsoft Excel file and is entered into a form in a browser.

 You must have the User Task Summarization skill and Now Assist AI Agents skill activated to use this feature.

 Task Mining recording and AI Desktop Actions agent execution require a Windows machine.For detailed information, see the Automation Center documentation.

</td></tr><tr><td>

Now Assist for Collaborative Work Management \(CWM\)

</td><td>

6.1.2

</td><td>

Now LLM is no longer set as the default provider for AI skills in CWM.

</td></tr><tr><td>

Now Assist for Complaint Case \(CSM\)

</td><td>

2.1.6

</td><td>

Changed: No changes to features, version update only.

</td></tr><tr><td>

Now Assist for Configuration Management Database \(CMDB\)

</td><td>

4.0.0

</td><td>

New

 -   AI-powered HAM advisor dashboard summarization: Leverage the summary section in HAM advisor dashboard to get precise recommendations and insights on what actions to take to get your CMDB ready to drive HAM business outcomes.
-   Impact Analysis: Get qualitative impact analysis for change and incident records associated with CIs. This capability looks at the dependencies of a CI, takes the semantics of the topology into account, and provides details on severity of the impact on connected CIs.

 Fixed

 -   The broken 'click here' link in the Search CMDB AI Agent panel has been resolved. The link now provides correct results.
-   Security fixes.

 Removed

 CMDB MCP server is no longer available via this plugin and has been deprecated. All registry records are now marked as inactive. The ServiceNow CMDB MCP and Visibility Server is now available as a separate application.

</td></tr><tr><td>

Now Assist for Contract Analysis

</td><td>

1.0.11

</td><td>

Updated the generic prompts for publisher part number and changes to list view, handle subscription period for review entitlement.

</td></tr><tr><td>

Now Assist For Core Business Suite

</td><td>

3.2.7

</td><td>

Fixed Now Assist skill mismatch on the product configuration console for Human Resources, Workplace services and Source-to-Pay.

</td></tr><tr><td>

Now Assist for CPQ

</td><td>

1.0.5

</td><td>

Plugin names under Now Assist for CPQ were changed, but the parent container app \(app-now-assist-for-cpq\) was not re-released to reflect them. The name change was introduced in the parent app by Prankur. Without a release cut of the parent, the updated names will not reach the Store, and customers installing or upgrading the parent app will hit issues from the mismatch.

</td></tr><tr><td>

Now Assist for Creator

</td><td>

29.4.1

</td><td>

Please click on the individual dependent apps included with this package for detailed release note information.

</td></tr><tr><td>

Now Assist for CSM Major Issue Management

</td><td>

1.1.0

</td><td>

Changed

 -   Major Case/Major Case Candidate worknotes - Display the similar case numbers or suggested case numbers with hyperlinks.
-   Internal code updates with no impact to existing functionality or user-facing behavior.

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

14.1.1

</td><td>

Changed

 -   New AI assets now default to third-party LLM providers with model version updates. Existing configurations using Now LLM Service stay unchanged, and the service remains available for manual selection.
-   Admins can view detailed information about each Now Assist skill to make faster and more informed decisions about enabling skill capabilities.

</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

7.4.1

</td><td>

New

 -   Default AI model provider for the Now Assist for Enterprise Architecture skills changed from Now LLM to Azure Open AI.
-   Added support for third-party AI models: GPT-5.4 mini and Gemini 3.5 Flash.

 Changed

 The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

</td></tr><tr><td>

Now Assist for Financial Services Operations \(FSO\)

</td><td>

3.3.1

</td><td>

New

 Added AI model options across Now Assist for FSO summarization skills, including Claude 4.5 Sonnet, Claude Haiku 4.5, Gemini 3.5 Flash, and GPT-5.4 mini - giving more provider and model choices.

 Changed

 -   Updated the default AI models for Claim, Dispute, Banking Customer Profile, Insurance Customer Profile, and Insurance Interaction Context summarization to newer model versions.
-   Set default model versions and tuned per-model token limits for more consistent summarization output.

</td></tr><tr><td>

Now Assist for Hardware Asset Management

</td><td>

4.4.0

</td><td>

Asset Summary Text Formatting - Fixed text display issues in asset summaries on on-premises instances to ensure consistent, readable formatting across all deployment types.

 Change Request Visibility - Resolved an issue where change requests were not appearing in asset summaries, giving you complete visibility into all asset-related changes.

</td></tr><tr><td>

Now Assist for HR Service Delivery \(HRSD\)

</td><td>

13.3.2

</td><td>

Changed

 Skills have been migrated to use 3P models by default.

</td></tr><tr><td>

Now Assist for IRM

</td><td>

22.4.0

</td><td>

Now Assist for IRM is now managed as a platform dependency. The application is delivered as an installed-as-dependency plugin, hidden from the main user interface and no longer appears as a standalone application tile in the ServiceNow App Store. AI-driven IRM functionality remains available and operates as before.

 Changed

 AI features are now accessed through IRM Native SKU applications. Users interact with AI capabilities via the IRM Native SKU apps; the AI dependency loads transparently, requiring no customer action to maintain existing functionality.

 Removed

 The Now Assist for IRM standalone application is no longer available. The application tile has been removed from the ServiceNow App Store and is not visible in the main user interface. Customers now use IRM Native SKU applications for AI features.

</td></tr><tr><td>

Now Assist for IT Operations Management \(ITOM\)

</td><td>

2.8.0

</td><td>

Changed

 -   Azure OpenAI is now the default model provider for AI skills and agents. Now LLM is no longer the default. Customers can choose the default and choose their own third-party providers.
-   Implemented secure-by-default configurations for the 5 new agentic ACLs.

 Fixed

 -   A formatting issue in alert analysis responses caused by the \` character has been resolved. HTML formatting in NAP now displays correctly.
-   The autonomous workflow has been updated to support AWS Claude as an AI agent provider, resolving compatibility issues and enabling seamless integration.

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

</td><td>

16.0.3

</td><td>

New

 -   Routing mode selector for Reassign tasks - A new out-of-the-box selector lets AI Admins choose Router \(recommended\) or Script for the AI Specialist without editing worker-template configuration.
-   In-form ticket deflection in Service Portal - An AI pipeline embedded in the ticket-creation form classifies intent, enriches context, retrieves knowledge, and suggests a resolution before a ticket is submitted.
-   Device remediation from ITSM workflows \(Intune and amp; Jamf\) - Agents can trigger endpoint remediation directly from Incident, Task, and Change without switching to external MDM consoles.
-   Toggle to enable/disable KFT creation - A new on/off control on the AI Specialist worker template governs whether a Knowledge Fulfillment Task is created when a resolution cites no knowledge article \(enabled by default\).

 Changed

 -   Conversational Analytics dashboard - Adds a topic detail page, Now Assist Data Explorer integration, standardized visualizations, and improved topics tables.
-   Default model change - Now LLM is no longer the default model for ITSM skills and agents; each now defaults to an optimal small third-party model \(large third-party models require approval\).
-   Routing-criteria analytics on the AIS Performance Dashboard - A new reassignment reason and per-criteria counts show when the AI Specialist reassigned an incident due to a routing-criteria match.
-   Remedial Action Framework extended to non-device actions - RAF now registers non-device actions \(e.g., SharePoint access, fulfillment flows, catalog items\) alongside device actions as the single action registry.
-   Richer AI Specialist work notes - Investigation and resolution work notes get consolidated formatting and clickable links to cited KB articles, similar incidents, and related records.

 Fixed

 Nothing was removed in this release.

 Removed

 Nothing was removed in this release.

</td></tr><tr><td>

Now Assist for Manufacturing Commercial Operations \(MCO\)

</td><td>

2.3.0

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Now Assist for Order Management

</td><td>

2.2.2

</td><td>

Changed

 -   The Manage Invoice Operations subflow now runs as the user who initiates the session.
-   The subflow has been assigned the interaction\_Agent and sn\_csm\_invoice.writer roles to maintain its ability to update work notes and create interaction-related records.

</td></tr><tr><td>

Now Assist for Platform

</td><td>

12.1.1

</td><td>

Application to capture the dependencies.

</td></tr><tr><td>

Now Assist for Platform Advanced

</td><td>

2.1.0

</td><td>

Application is used to capture dependencies.

</td></tr><tr><td>

Now Assist for Platform Foundation

</td><td>

2.1.0

</td><td>

Application is used to capture dependencies.

</td></tr><tr><td>

Now Assist for Platform Prime

</td><td>

2.1.0

</td><td>

Application is used to capture dependencies.

</td></tr><tr><td>

Now Assist for Privacy Management

</td><td>

22.4.0

</td><td>

Changed

 All Now Assist skills are now integrated with the latest third-party models for Claude, Gemini, and ChatGPT. This enables better performance and broader compatibility across your AI workflows.

</td></tr><tr><td>

Now Assist for Process Mining

</td><td>

3.1.2

</td><td>

- Migrate all process mining skills to Mosaic \(off Glide\).

</td></tr><tr><td>

Now Assist for Prompt Assistance

</td><td>

5.1.4

</td><td>

New

 Added new metric 'Response Time' for Voice Agents - this enables users to validate the time taken by voice agents to perform their assigned tasks.

 Changed

 -   Modified the default model to Claude.
-   Added improvements for candidate generation for AIO.

</td></tr><tr><td>

Now Assist for Sales and Order Management for Telecommunications

</td><td>

4.1.2

</td><td>

Fixed

 App Dependency was added for smooth installation.

</td></tr><tr><td>

Now Assist for Sales Force Automation \(SFA\)

</td><td>

1.1.5

</td><td>

Changed: Some details related to the dependency for this plugin.

</td></tr><tr><td>

Now Assist for Security Incident Response \(SIR\)

</td><td>

6.3.4

</td><td>

Changed

 Default models for all skills updated from Now LLM to 3P model.

</td></tr><tr><td>

Now Assist for Service Exchange

</td><td>

1.1.4

</td><td>

Connections tab in the Service Exchange Center.

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding.

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities.

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements.

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting.

 Group-based persona assignments for Remote Catalog.

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

</td></tr><tr><td>

Now Assist for Setup

</td><td>

3.1.4

</td><td>

New

 -   PoCs to explore LitJS and AIUX \(Horizon 2.0\) for Product Hub and Admin Home redesign/UIs.
-   Continue defining and tracking the U2 metrics framework.
-   Explore Golden Config and App Manager Suite Installation APIs for installs.
-   Address GA defect fixes and defects; explore AINPX for the console.
-   HA: Fix security defects, stabilize HA and agent responses across LLM providers, and improve UX and content.

</td></tr><tr><td>

Now Assist for Setup Core

</td><td>

2.1.5

</td><td>

New

 -   PoCs to explore LitJS and AIUX \(Horizon 2.0\) for Product Hub and Admin Home redesign/uplifts.
-   Continue defining and tracking the U2 metrics framework.
-   Explore Golden Config and App Manager Suite Installation APIs for installs.

 Fixed

 -   Address GA defect fixes and defects; explore AINPX for the console.
-   HA: Fix security defects, stabilize HA and agent responses across LLM providers, and improve UX and content.

</td></tr><tr><td>

Now Assist for Smart Assessment Engine

</td><td>

22.4.1

</td><td>

Changed

 -   Updated LLM provider model versions for Smart Assessment Response Assist skill for Google Gemini \(Chat Completions\) to gemini-3.5-flash, Azure OpenAI \(Chat Completions\) to gpt-5.4, and AWS Claude \(Amazon Bedrock Chat Completions\) to claude-sonnet-4-6.
-   Changed the default LLM provider for Smart Assessment Response Assist skill from Now LLM Service \(Now LLM Generic\) to Google Gemini \(Chat Completions\).

</td></tr><tr><td>

Now Assist for Software Asset Management \(SAM\)

</td><td>

9.0.0

</td><td>

Changed

 Now Assist for SAM no longer defaults to the Now LLM. It now selects from alternate third-party LLMs based on which model performs best for each individual use case.

</td></tr><tr><td>

Now Assist for Strategic Portfolio Management \(SPM\)

</td><td>

9.7.1

</td><td>

Fixed

 -   AI forecasted status and AI rationale fields from goal insights are updated on the grid in realtime without grid refresh.
-   Portfolio Insights button is visible faded out when Portfolio Insights panel is open.
-   Project Answers \(Ask Now Assist\) now deliver improved formatting and more enhanced query parsing for complex questions.

 Changed

 Experience a more streamlined RIDAC with three dedicated views: AI-Identified Risks \(Project Risk Detection\), RIDAC by Type with separate tabs for each RIDAC type, and the complete All RIDAC overview. The new presentation list layout replaces the flat grid, making records easier to browse, organize, and manage.

</td></tr><tr><td>

Now Assist for Talent

</td><td>

1.8.3

</td><td>

Default Model for 'Generate Talking Points' skill has been updated from NowLLM to Amazon Bedrock.

</td></tr><tr><td>

Now Assist for Third-Party Risk Management

</td><td>

22.3.4

</td><td>

New

 Added support for Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini models.

 Changes

 Updated Azure OpenAI gpt-5.4-mini as default model for issue recommendation skill.

</td></tr><tr><td>

Now Assist for Threat Intelligence Security Center

</td><td>

2.2.0

</td><td>

New

 Introduced Report Authoring capability with customizable styling options. Analysts can now generate AI-powered threat intelligence reports directly from threat case data with simple instructions to guide content, focus, and formatting.

 Fixed

 Enhanced case summarization with improved performance and faster response times while maintaining summary quality.

</td></tr><tr><td>

Now Assist for Voice

</td><td>

5.1.1

</td><td>

New

 -   Multi-Language Support: Callers can select their preferred language at the start of a call; added support for Irish English, Swedish, Norwegian, Australian English, and Polish voices.
-   SIP Telephony Integration: Transfer calls to live agents via SIP protocol for NiCE-enabled contact center.

 Changed

 -   Context Persistence Control: New flag to enable/disable conversation context storage for compliance.
-   SIP Metadata Tracking: Transfer method and target now captured in interaction records.
-   Language Config Table: Dynamically generates language selection prompts from trigger phrases.
-   TTS Config Updates: Added trigger phrases for secondary language selection.
-   Cross-Scope Deletion: Language configuration records can now be deleted from cross scope.

</td></tr><tr><td>

Now Assist for Vulnerability Response

</td><td>

5.1.0

</td><td>

Changed

 Updated the default LLM provider for Now Assist for Vulnerability Response skills to 3P \(Third-Party\) models where required for consistency across all supported skills.

 Added support for the following models for all AI features:

 -   Google Gemini 3.5.
-   FlashOpenAI GPT 5.1.
-   OpenAI GPT 5.4 Mini.

</td></tr><tr><td>

Now Assist for WDF

</td><td>

2.1.4

</td><td>

-   Enabled Now Assist Panel in WDF Home Page.
-   Configured NextWave for faster and better AI Conversational Assist within WDF.

</td></tr><tr><td>

Now Assist in AI Search

</td><td>

17.1.4

</td><td>

New

 AI Search Admins can now configure any search source \(including non-out-of-box tables such as incidents and custom tables\) to the Now Assist multi-content synthesized answers. Results from additional sources are dispatched per source group, merged into a ranked top-K list, and delivered to the synthesizer with citation metadata and origin information intact. New system properties control the maximum documents requested per group and the top-K document count used in the final merged response.

 Changed

 Search and VA profile handling has been separated for the Enhanced Chat dynamic window experience.

 Fixed

 -   MarkdownToHtml incorrectly truncated URLs containing balanced parentheses. For example, SharePoint URLs containing \(SRM FORM\) caused the href attribute to cut off at the first closing parenthesis and left the remainder of the URL as plain text in Now Assist synthesized answer rendering.
-   The Now Assist Multi-Content Response Genius Model returned an inconsistent output structure \(one synthesized result plus separate citation entries\) rather than consolidating citations within the synthesized result as an internal array. This caused multiple Genius Guidance Cards to render instead of a single unified card.

</td></tr><tr><td>

Now Assist in Catalog Builder

</td><td>

7.3.0

</td><td>

Now Assist for Catalog Generation now incorporates catalog item creation best practices directly into the catalog item building experience. As catalog item creators build catalog items, the system detects deviations from established standards and surfaces proactive recommendations - including optimal variable types, streamlined form designs, and structures suited for conversational requests. A new administrator property controls whether best practice enforcement is active, supported by a dedicated knowledge base of catalog standards.

</td></tr><tr><td>

Now Assist in Catalog item forms

</td><td>

1.4.2

</td><td>

Made some enhancements.

</td></tr><tr><td>

Now Assist in Contract Management

</td><td>

2.3.2

</td><td>

Changed

 The default model provider for Now Assist features in Contract Management is Azure OpenAI.

</td></tr><tr><td>

Now Assist in Conversational Catalog Request

</td><td>

7.1.1

</td><td>

Catalog agent for Premium chat experiences.

 -   Extended conversational coverage with support for additional question types, including Lookup Multiple Choice, Lookup Select Box, and Requested For \(Single\).
-   Maintained compatibility with the existing Conversational Catalog solution \(LLM topic block\) on Premium chat within portals and the Now Assist panel. Catalog items continue to be accessible through conversational interfaces; when agentic AI cannot process catalog item requests, the system reverts to the established solution.
-   Implemented validation checks to ensure catalog item questions with prefilled values meet requirements.
-   Applied performance optimizations.

</td></tr><tr><td>

Now Assist in Document Intelligence

</td><td>

6.2.0

</td><td>

Changed

 -   Updated default model configuration per ServiceNow platform guidance.
-   Default OOB model provider to Azure OpenAI.
-   Increase token limit to 8192.

 Fixed

 Task status should be set to failed if the LLM throws an error.

</td></tr><tr><td>

Now Assist in Document Management

</td><td>

3.0.1

</td><td>

In July release we are enabling the smart documents skill configuration as active by default and the smart documents feature would be available on all tables if no table is specified.

</td></tr><tr><td>

Now Assist in Knowledge Management

</td><td>

30.11.3

</td><td>

Defect fix.

</td></tr><tr><td>

Now Assist in Standard Ticket Page

</td><td>

1.3.0

</td><td>

Made some enhancements.

</td></tr><tr><td>

Now Assist in Virtual Agent

</td><td>

20.0.8

</td><td>

New

 -   Prompt library for premium chat: View default prompts \(read-only filters\) and manage your own prompts.
-   Post-chat survey for premium chat: Configure survey and closing topics \(premium chat\) and closing topics \(enhanced chat\). Existing topics migrate automatically.
-   Additional semantic search sources for synthesized response: Added via the dropdown.
-   Search-profile override for the enhanced chat with dynamic movable, resizable window: Toggle per assistant via a new agentic orchestration attribute.
-   Premium chat for mobile custom apps: Custom apps on mobile can be set to enhanced chat or premium chat.

 Changed

 -   Citations for additional search source types are now shown in the user experience.
-   AI Agent Studio assistant is no longer shown in the assistant list.

 Fixed

 -   PRB2024249: Repeated non-conversational catalog term no longer drop URLs.
-   PRB2039583: Corrected prompt library text in Assistant Designer.
-   PRB2038815: Prompt library toggle now auto-saves.
-   PRB2038884: Restored tooltip for conversational catalog Items.
-   PRB2038480: Promoted assets no longer mis-map Agentic Workflow to AI agent type.
-   PRB2038346: Default prompts now show 'ServiceNow' as creator.
-   PRB2030411/PRB2030421: Fixed UI issues in display experience portal and amp; channel.
-   PRB2032277: Review page in create flow no longer omits configuration.
-   PRB2032733: Custom greeting/live-agent topics no longer lost on June 2026 upgrade.
-   PRB2030773: Fixed localization warning from parameterized static greeting.
-   PRB2032989: Chat tabs no longer mislabeled when premium chat is unavailable.
-   PRB2024688: Fixed long-string layout on small windows and non-English icons.
-   PRB2035197: Premium display experience now defaults to 'Otto'.
-   PRB2033795: Granular feedback options now translate correctly.
-   PRB2034709: Inactivated the Search Q and amp;A agent for Now Assist in Virtual Agent.
-   PRB2029072: Fixed Now Assist panel Developer assistant in add from library.
-   PRB1998145: Voice calls in testing UI now connect on first attempt.
-   PRB2030310: Fixed copy/font-size issues in enable chat features.
-   PRB2029063: Add from library now shows correct count.
-   PRB2033251: Default Now Assist for Virtual Agent and Now Assist panel greeting topics convert to tools on load.
-   PRB2029106: Fixed header UI on Promoted asset tab.
-   PRB2030701: Fixed secondary-language support when phonemes change.
-   PRB2027372/PRB2027179/PRB2027171: Fixed RTL layout under Voice Deployment designer and Assistant tab in Assistant Designer.
-   PRB2027159: Translated strings under Voice Deployment.
-   PRB2022882: Disambiguated 'min' in the Voice Deployment designer.
-   PRB2026588: Corrected tooltip for field labels.
-   PRB2013063: Assistant test panel refreshes across sequential tests.
-   PRB2027467: Options disabled until type selected in add chat experience.
-   PRB2032643: Org chart widget loads on mobile.
-   PRB2032268: Labels populate correctly on 'chat' type premium chat branding modal.

</td></tr><tr><td>

Now Assist Readiness Evaluation

</td><td>

1.4.2

</td><td>

Agentic AI Assessment dashboard tab correctly displays finding cards only by default \(Assessment Findings, Findings by Category, Finding Trends\), consistent with the Now Assist Assessment tab behavior. Previously, the Agentic AI Assessment tab incorrectly displayed effort-related cards when the sn\_assess.effort\_visibility system property was set to its default value of false.

</td></tr><tr><td>

Now Assist Service Quality

</td><td>

2.0.2

</td><td>

Changed

 -   Admins can sort data, manage filters, and easily organise cases on the dashboard with the new sorting, visibility, and skill management capabilities.
-   The Now Assist Admin experience enhancements include filtering of scoring parameters and the option to separate out availability across dashboards and record pages.
-   The enhanced quality assurance dashboard enables managers to sort agents and case lists and also enables managers to open agent evaluations in a separate tab.

</td></tr><tr><td>

Now Assist Skill Discovery and Execution

</td><td>

10.2.3

</td><td>

Fixed

 -   Slot fill error fixed when KG results are large by adding a result limit.
-   Resolved incorrect confirmation of fields from unrelated input collectors.
-   Fixed slot fill failure during second topic discovery in the same conversation.
-   Corrected handling of 'trying\_to\_skip' due to wrong property reference.
-   Fixed intermittent empty response issue in VA input response generation prompt.

</td></tr><tr><td>

Now Assist Skill Kit

</td><td>

9.1.1

</td><td>

Voice Assistant/Agent Evaluations

 -   Background Noise Injection for Voice Assistant/Agent Simulations - Simulate real-world acoustic environments by injecting background noise during evaluations, helping ensure results better reflect production conditions.
-   Response Time Metric - Gain deeper visibility into voice agent/assistant performance with a new latency-focused metric that measures response time.

 Now Assist Skill Kit

 -   Model Preview Program for Skill Kit - Get Day 0 access to the latest frontier models through the Model Preview Program, enabling early testing and innovation.
-   Skill Archiving - Archive Skills to keep your workspace organized while preserving access to historical configurations and assets.

 Agentic Evaluations.

 Framework Enhancements to Agentic Evaluations.

</td></tr><tr><td>

Opportunity Management AI Features

</td><td>

1.0.9

</td><td>

New: Manage opportunity line items conversationally via a conversational interface through the MCP server.

 Fixed: Manage competitor details, and touchpoint information conversationaly via a conversational interface through the MCP server. Fields like work notes and other fields in the competitor object could not be managed in the previous release.

</td></tr><tr><td>

Opportunity Management Application

</td><td>

12.1.0

</td><td>

New: Create a guided selling framework to enforce stage exit governance, and manage all deal-related actions from a uniﬁed opportunity workspace.

</td></tr><tr><td>

Opportunity Management Data Model

</td><td>

12.1.0

</td><td>

New: Introduced default OOB sales types and sales cycle stage values.

</td></tr><tr><td>

Order Management

</td><td>

17.2.0

</td><td>

New

 Supporting billing account on order line.

 Fixed

 Minor defects fixes.

</td></tr><tr><td>

Payment Card

</td><td>

1.4.0

</td><td>

Changed

 Updated internal application components to support ongoing platform enhancements.

</td></tr><tr><td>

Platform AI Agents and Skills

</td><td>

13.1.9

</td><td>

New

 Generate resolution plan Agentic workflow

 -   Information from related tables is now included while generating resolution notes.
-   Display predicted field values and amp; allow edits on the output before record creation.

 Process images for tasks Agentic workflow

 Existing UI validations honored while record creation.

 Help optimize team productivity Agentic workflow

 Consider similar records for work allocation.

 Activity Response Generation capability

 Detect user intent and proactively propose work notes/ comments.

 Analyse task trends Agentic workflow

 Improve quality of GAF records being fetched.

 Identify escalation signals Agentic workflow

 Support manager utterances like 'show me likely escalations for John Doe \(agent name\)'.

 Generate my work plan Agentic workflow

 Suggest actions for prioritized list of tasks.

 Changed

 Default model provider changed from existing NowLLM models.

 Fixed

 Investigate IT problems Agentic workflow

 Token limit issue is now resolved.

</td></tr><tr><td>

Platform Analytics

</td><td>

8.4.1

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

Portfolio Planning

</td><td>

8.15.3

</td><td>

Fixed

 -   Resolved an issue where the Create Demand modal in Portfolio Planning did not work.
-   Resolved an issue that prevented creating a portfolio plan with the Planning Item lens when only standard Portfolio Planning was installed.
-   Resolved an issue where targets added to a portfolio plan did not reflect correctly in the Financials tab.
-   Resolved an issue where status values were incorrectly copied when duplicating planning items.
-   Resolved an issue where the Documents tab displayed a blank page in Spanish in Enterprise Agile Planning.
-   Resolved a text concatenation issue affecting translated strings in SPM Prioritization.
-   Resolved unclear empty-state messaging in the Manage Access modal.

</td></tr><tr><td>

Portfolio Planning Core

</td><td>

5.13.1

</td><td>

Fixed

 Resolved an issue that allowed a lens to be deactivated while portfolio plans were still associated with it.

</td></tr><tr><td>

Privacy Management Advanced

</td><td>

22.4.0

</td><td>

Changed

 All Now Assist skills are now integrated with the latest third-party models for Claude, Gemini, and ChatGPT. This enables better performance and broader compatibility across your AI workflows.

</td></tr><tr><td>

Product Catalog Management Core

</td><td>

19.1.0

</td><td>

-   Support domain separation on product offering tables, product specification tables, specification-to-specification relationships and product offering-to-product offering relationships.
-   Support REST API on product catalog to support custom portals.

</td></tr><tr><td>

Project Workspace

</td><td>

7.4.1

</td><td>

New RIDAC List view: Experience a more streamlined RIDAC with three dedicated views: AI-Identified Risks \(Project Risk Detection\), RIDAC by Type with separate tabs for each RIDAC type, and the complete All RIDAC overview. The new presentation list layout replaces the flat grid, making records easier to browse, organize, and manage.

</td></tr><tr><td>

prompt-management

</td><td>

2.0.6

</td><td>

 

</td></tr><tr><td>

Query Generation

</td><td>

6.1.1

</td><td>

New

 Support for Automated Indicators.

</td></tr><tr><td>

Query Orchestrator

</td><td>

1.2.1

</td><td>

-   Updated the query orchestrator's generative AI configuration to use specific, versioned model IDs with higher reasoning effort and larger token limits, improving the quality and reliability of query decomposition.
-   Set AWS Claude as the default model.

</td></tr><tr><td>

Recommendation template

</td><td>

22.4.0

</td><td>

Changed

 All Now Assist skills are now integrated with the latest third-party models for Claude, Gemini, and ChatGPT. This enables better performance and broader compatibility across your AI workflows.

</td></tr><tr><td>

Recommended Actions for Security Operations

</td><td>

2.2.4

</td><td>

Changed

 Default model for the skill updated from Now LLM to 3P model.

</td></tr><tr><td>

Recruiter Workspace

</td><td>

8.0.1

</td><td>

No Functional updates.

</td></tr><tr><td>

Reporting UI Component for Workspace

</td><td>

2.5.0

</td><td>

New

 Enhanced reporting infrastructure to support Now Assist for Threat Intelligence Security Center with AI-powered authoring and customizable styling capabilities.

</td></tr><tr><td>

Resource Management Workspace

</td><td>

5.9.1

</td><td>

New

 Using common schedule for group resource assignments.

 Fixed

 -   Resolved error when dragging and dropping resource assignments to other users.
-   Preserved custom field values when unassigning resources.
-   Fixed filtering by Parent Item and Owner in Resource Management Workspace.
-   Resolved error when displaying custom date fields as workspace columns.
-   Hidden inactive skills from the Skills display in Resource Management Workspace.
-   Improved performance when loading resource cards in the workspace.
-   Fixed error when editing text and dropdown fields in the Unassigned Work tab.
-   Fixed filtering for integer-based dropdown fields in workspace columns.

</td></tr><tr><td>

Roadmap UI Builder Component

</td><td>

22.13.2

</td><td>

Fixed

 -   Resolved an issue where the milestone tab on the roadmap rendered project details instead of actual milestone data.
-   Resolved an issue where the left arrow key did not return focus to the milestone from the group-by expand indicator.
-   Resolved an issue where the milestone status was not announced to screen reader users.
-   Resolved an issue where the current date line was not accessible to screen readers.

</td></tr><tr><td>

Sales and Order Management for Telecommunications - Advanced

</td><td>

2.1.2

</td><td>

Fixed

 App Dependency was added for smooth installation.

</td></tr><tr><td>

Sales and Order Management for Telecommunications - Prime

</td><td>

2.1.2

</td><td>

Fixed

 App Dependency was added for smooth installation.

</td></tr><tr><td>

Sales Common

</td><td>

7.0.1

</td><td>

Fixed: Minor defects for term calculations.

</td></tr><tr><td>

Screen Summarization

</td><td>

1.1.18

</td><td>

Maintenance fixes.

</td></tr><tr><td>

Security Incident Response

</td><td>

14.1.2

</td><td>

External users couldn't open a security incident from a response task due to a GlideRecordSecure access-control restriction.

</td></tr><tr><td>

Security Incident Response Workspace

</td><td>

1.9.2

</td><td>

Fixed

 Fixed an issue with 'Allow access for external user' option to access assigned response tasks of a parent security incident.

</td></tr><tr><td>

Service Exchange - Advanced

</td><td>

1.1.4

</td><td>

Connections tab in the Service Exchange Center.

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding.

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities.

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements.

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting.

 Group-based persona assignments for Remote Catalog.

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

</td></tr><tr><td>

Service Exchange - Foundation

</td><td>

1.1.4

</td><td>

New

 -   Added a new Knowledge Assist experience: admins and agents can now ask questions about Service Exchange directly from the Now Assist panel and get answers grounded in official documentation and support content, with source links included.
-   Answers are scoped to your currently installed app version and limited to information you're permitted to access in your instance, the assistant never fabricates information outside of what's documented.

</td></tr><tr><td>

Service Exchange - Prime

</td><td>

1.1.4

</td><td>

Connections tab in the Service Exchange Center.

 Create, view, request, and offboard provider and consumer connections from a single location in the Service Exchange Center. Search and filter connections without navigating across multiple screens.

 Improved consumer registration and onboarding.

 Onboard consumers faster with a guided, step-by-step registration experience. Upgraded consumers are automatically redirected to this experience to receive clearer progress indicators during onboarding, and actionable messaging for failure and delay scenarios, minimizing onboarding friction and support dependency.

 Improved FDS capabilities.

 -   Improve your connection experience, by syncing Knowledge Base articles between provider and consumer instances.
-   Reduce data inconsistencies by maintaining sys IDs for CMDB data and dependent relationships through transform maps.
-   Ensure CI functionality is preserved on the destination instance by choosing to automatically create CI dependency relationships when relationship data is received from the source.
-   Improved compliance through restricted data sync from non production instances to production instances for CMDB tables.

 Journal Field Framework enhancements.

 -   Increase flexibility in journal data synchronization between provider and consumer instances by mapping multiple source fields to a single target journal field.
-   Configure journal fields such of type journal\_input fields alongside journal type, ensuring all journal entries are preserved during synchronization without requiring custom scripting.

 Group-based persona assignments for Remote Catalog.

 Assign Remote Catalog personas to user groups so existing group-based access management practices extend to Remote Catalog, reducing administrative effort by managing access at the group level instead of individual users.

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

7.0.2

</td><td>

New

 Use ServiceNow AI Lens from your browser to capture and analyze screens and auto-fill catalog item forms in Service Portal - no installation required.

</td></tr><tr><td>

ServiceNow AI Lens Core

</td><td>

7.0.1

</td><td>

New

 Use ServiceNow AI Lens from your browser to capture and analyze screens and auto-fill catalog item forms in Service Portal - no installation required.

</td></tr><tr><td>

ServiceNow IDE

</td><td>

4.4.2

</td><td>

New

 Expanded end-to-end automation coverage for ServiceNow Studio workflows.

</td></tr><tr><td>

Service Operations Workspace Alert Automation

</td><td>

25.16.0

</td><td>

Fixed

 Team operators can open response automations with an OR condition.

</td></tr><tr><td>

Service Operations Workspace Alert Automation API

</td><td>

25.16.0

</td><td>

Fixed

 Team operators can open response automations with an OR condition.

</td></tr><tr><td>

Service Operations Workspace Alert Automation UI

</td><td>

25.16.0

</td><td>

Fixed

 Team operators can open response automations with an OR condition.

</td></tr><tr><td>

Service Operations Workspace Alert Mngmt

</td><td>

27.2.1

</td><td>

Changed

 -   Express List accessibility improvements. The Express List is now fully accessible to users with low vision, expanding the user base and ensuring compliance with international accessibility standards and regulations.
-   Consolidated ACLs for access control management. Access control lists have been consolidated to better follow security best practices, reducing risks and simplifying management.
-   Link View topology visualization accessibility. Link View topology visualization now meets accessibility standards while maintaining usability and performance.

 Fixed

 -   The Express List layout has been corrected to properly adapt for narrow viewports and no longer breaks at certain screen sizes.
-   Unintended double scrollbars in accessibility reflow mode have been eliminated.
-   The Express List columns now display correctly in Japanese and CJK languages, resolving translation and layout issues.
-   The Express List live list functionality now properly triggers and updates in real time.
-   The 'update available' banner no longer appears incorrectly when resuming the live list.
-   Saving an Alert Management Rule with 'Create Incident Advanced' now works in all scenarios.
-   Operators with more than five assignment groups can now see their created Enrich automations in the Enrich module.
-   Alerts manually removed from a group are no longer automatically re-added.
-   A broken documentation link in the alert automation configuration has been fixed.
-   Dynatrace Monitor setup instructions in the Launchpad have been updated to match the current Dynatrace console.
-   The 'Tags' label in the Launchpad is now correctly translated across contexts.
-   Concatenated strings causing grammatical issues in certain languages have been separated for correct localization.
-   Launchpad forms now match the approved design at 400% zoom.
-   Dotted connection lines in Link View now appear when connected CIs are returned from the backend.
-   The Simulation UI now displays 'This automation' or the saved automation name instead of 'MIXED' or 'CMDB' labels for Mixed or CMDB group types.
-   The 'All Time \(Last 180 days\)' option now shows as selected in the time range picker and is correctly translated.
-   Service health percentages now display correctly in locales using a comma as the decimal separator.
-   Ellipsis menu items in the Log Viewer now display in the user's language setting.
-   Backspace behavior in Extended mode is now correct.
-   The evt\_mgmt\_admin role now has write access to Express List properties.

</td></tr><tr><td>

Service Operations Workspace Express List

</td><td>

27.3.2

</td><td>

Changed

 -   Express List accessibility improvements. The Express List is now fully accessible to users with low vision, expanding the user base and ensuring compliance with international accessibility standards and regulations.
-   Consolidated ACLs for access control management. Access control lists have been consolidated to better follow security best practices, reducing risks and simplifying management.
-   Link View topology visualization accessibility. Link View topology visualization now meets accessibility standards while maintaining usability and performance.

 Fixed

 -   The Express List layout has been corrected to properly adapt for narrow viewports and no longer breaks at certain screen sizes.
-   Unintended double scrollbars in accessibility reflow mode have been eliminated.
-   The Express List columns now display correctly in Japanese and CJK languages, resolving translation and layout issues.
-   The Express List live list functionality now properly triggers and updates in real time.
-   The 'update available' banner no longer appears incorrectly when resuming the live list.
-   Saving an Alert Management Rule with 'Create Incident Advanced' now works in all scenarios.
-   Operators with more than five assignment groups can now see their created Enrich automations in the Enrich module.
-   Alerts manually removed from a group are no longer automatically re-added.
-   A broken documentation link in the alert automation configuration has been fixed.
-   Dynatrace Monitor setup instructions in the Launchpad have been updated to match the current Dynatrace console.
-   The 'Tags' label in the Launchpad is now correctly translated across contexts.
-   Concatenated strings causing grammatical issues in certain languages have been separated for correct localization.
-   Launchpad forms now match the approved design at 400% zoom.
-   Dotted connection lines in Link View now appear when connected CIs are returned from the backend.
-   The Simulation UI now displays 'This automation' or the saved automation name instead of 'MIXED' or 'CMDB' labels for Mixed or CMDB group types.
-   The 'All Time \(Last 180 days\)' option now shows as selected in the time range picker and is correctly translated.
-   Service health percentages now display correctly in locales using a comma as the decimal separator.
-   Ellipsis menu items in the Log Viewer now display in the user's language setting.
-   Backspace behavior in Extended mode is now correct.
-   The evt\_mgmt\_admin role now has write access to Express List properties.

</td></tr><tr><td>

Service Operations Workspace ITOM Apps

</td><td>

27.2.6

</td><td>

Changed

 -   Express List accessibility improvements. The Express List is now fully accessible to users with low vision, expanding the user base and ensuring compliance with international accessibility standards and regulations.
-   Consolidated ACLs for access control management. Access control lists have been consolidated to better follow security best practices, reducing risks and simplifying management.
-   Link View topology visualization accessibility. Link View topology visualization now meets accessibility standards while maintaining usability and performance.

 Fixed

 -   The Express List layout has been corrected to properly adapt for narrow viewports and no longer breaks at certain screen sizes.
-   Unintended double scrollbars in accessibility reflow mode have been eliminated.
-   The Express List columns now display correctly in Japanese and CJK languages, resolving translation and layout issues.
-   The Express List live list functionality now properly triggers and updates in real time.
-   The 'update available' banner no longer appears incorrectly when resuming the live list.
-   Saving an Alert Management Rule with 'Create Incident Advanced' now works in all scenarios.
-   Operators with more than five assignment groups can now see their created Enrich automations in the Enrich module.
-   Alerts manually removed from a group are no longer automatically re-added.
-   A broken documentation link in the alert automation configuration has been fixed.
-   Dynatrace Monitor setup instructions in the Launchpad have been updated to match the current Dynatrace console.
-   The 'Tags' label in the Launchpad is now correctly translated across contexts.
-   Concatenated strings causing grammatical issues in certain languages have been separated for correct localization.
-   Launchpad forms now match the approved design at 400% zoom.
-   Dotted connection lines in Link View now appear when connected CIs are returned from the backend.
-   The Simulation UI now displays 'This automation' or the saved automation name instead of 'MIXED' or 'CMDB' labels for Mixed or CMDB group types.
-   The 'All Time \(Last 180 days\)' option now shows as selected in the time range picker and is correctly translated.
-   Service health percentages now display correctly in locales using a comma as the decimal separator.
-   Ellipsis menu items in the Log Viewer now display in the user's language setting.
-   Backspace behavior in Extended mode is now correct.
-   The evt\_mgmt\_admin role now has write access to Express List properties.

</td></tr><tr><td>

Service Operations Workspace Service Dashboard

</td><td>

27.3.1

</td><td>

Changed

 -   Express List accessibility improvements. The Express List is now fully accessible to users with low vision, expanding the user base and ensuring compliance with international accessibility standards and regulations.
-   Consolidated ACLs for access control management. Access control lists have been consolidated to better follow security best practices, reducing risks and simplifying management.
-   Link View topology visualization accessibility. Link View topology visualization now meets accessibility standards while maintaining usability and performance.

 Fixed

 -   The Express List layout has been corrected to properly adapt for narrow viewports and no longer breaks at certain screen sizes.
-   Unintended double scrollbars in accessibility reflow mode have been eliminated.
-   The Express List columns now display correctly in Japanese and CJK languages, resolving translation and layout issues.
-   The Express List live list functionality now properly triggers and updates in real time.
-   The 'update available' banner no longer appears incorrectly when resuming the live list.
-   Saving an Alert Management Rule with 'Create Incident Advanced' now works in all scenarios.
-   Operators with more than five assignment groups can now see their created Enrich automations in the Enrich module.
-   Alerts manually removed from a group are no longer automatically re-added.
-   A broken documentation link in the alert automation configuration has been fixed.
-   Dynatrace Monitor setup instructions in the Launchpad have been updated to match the current Dynatrace console.
-   The 'Tags' label in the Launchpad is now correctly translated across contexts.
-   Concatenated strings causing grammatical issues in certain languages have been separated for correct localization.
-   Launchpad forms now match the approved design at 400% zoom.
-   Dotted connection lines in Link View now appear when connected CIs are returned from the backend.
-   The Simulation UI now displays 'This automation' or the saved automation name instead of 'MIXED' or 'CMDB' labels for Mixed or CMDB group types.
-   The 'All Time \(Last 180 days\)' option now shows as selected in the time range picker and is correctly translated.
-   Service health percentages now display correctly in locales using a comma as the decimal separator.
-   Ellipsis menu items in the Log Viewer now display in the user's language setting.
-   Backspace behavior in Extended mode is now correct.
-   The evt\_mgmt\_admin role now has write access to Express List properties.

</td></tr><tr><td>

Service Operations Workspace Supervisor Dashboard

</td><td>

1.1.0

</td><td>

Changed

 -   Express List accessibility improvements. The Express List is now fully accessible to users with low vision, expanding the user base and ensuring compliance with international accessibility standards and regulations.
-   Consolidated ACLs for access control management. Access control lists have been consolidated to better follow security best practices, reducing risks and simplifying management.
-   Link View topology visualization accessibility. Link View topology visualization now meets accessibility standards while maintaining usability and performance.

 Fixed

 -   The Express List layout has been corrected to properly adapt for narrow viewports and no longer breaks at certain screen sizes.
-   Unintended double scrollbars in accessibility reflow mode have been eliminated.
-   The Express List columns now display correctly in Japanese and CJK languages, resolving translation and layout issues.
-   The Express List live list functionality now properly triggers and updates in real time.
-   The 'update available' banner no longer appears incorrectly when resuming the live list.
-   Saving an Alert Management Rule with 'Create Incident Advanced' now works in all scenarios.
-   Operators with more than five assignment groups can now see their created Enrich automations in the Enrich module.
-   Alerts manually removed from a group are no longer automatically re-added.
-   A broken documentation link in the alert automation configuration has been fixed.
-   Dynatrace Monitor setup instructions in the Launchpad have been updated to match the current Dynatrace console.
-   The 'Tags' label in the Launchpad is now correctly translated across contexts.
-   Concatenated strings causing grammatical issues in certain languages have been separated for correct localization.
-   Launchpad forms now match the approved design at 400% zoom.
-   Dotted connection lines in Link View now appear when connected CIs are returned from the backend.
-   The Simulation UI now displays 'This automation' or the saved automation name instead of 'MIXED' or 'CMDB' labels for Mixed or CMDB group types.
-   The 'All Time \(Last 180 days\)' option now shows as selected in the time range picker and is correctly translated.
-   Service health percentages now display correctly in locales using a comma as the decimal separator.
-   Ellipsis menu items in the Log Viewer now display in the user's language setting.
-   Backspace behavior in Extended mode is now correct.
-   The evt\_mgmt\_admin role now has write access to Express List properties.

</td></tr><tr><td>

Service Operations Workspace UI Components

</td><td>

27.2.4

</td><td>

Changed

 -   Express List accessibility improvements. The Express List is now fully accessible to users with low vision, expanding the user base and ensuring compliance with international accessibility standards and regulations.
-   Consolidated ACLs for access control management. Access control lists have been consolidated to better follow security best practices, reducing risks and simplifying management.
-   Link View topology visualization accessibility. Link View topology visualization now meets accessibility standards while maintaining usability and performance.

 Fixed

 -   The Express List layout has been corrected to properly adapt for narrow viewports and no longer breaks at certain screen sizes.
-   Unintended double scrollbars in accessibility reflow mode have been eliminated.
-   The Express List columns now display correctly in Japanese and CJK languages, resolving translation and layout issues.
-   The Express List live list functionality now properly triggers and updates in real time.
-   The 'update available' banner no longer appears incorrectly when resuming the live list.
-   Saving an Alert Management Rule with 'Create Incident Advanced' now works in all scenarios.
-   Operators with more than five assignment groups can now see their created Enrich automations in the Enrich module.
-   Alerts manually removed from a group are no longer automatically re-added.
-   A broken documentation link in the alert automation configuration has been fixed.
-   Dynatrace Monitor setup instructions in the Launchpad have been updated to match the current Dynatrace console.
-   The 'Tags' label in the Launchpad is now correctly translated across contexts.
-   Concatenated strings causing grammatical issues in certain languages have been separated for correct localization.
-   Launchpad forms now match the approved design at 400% zoom.
-   Dotted connection lines in Link View now appear when connected CIs are returned from the backend.
-   The Simulation UI now displays 'This automation' or the saved automation name instead of 'MIXED' or 'CMDB' labels for Mixed or CMDB group types.
-   The 'All Time \(Last 180 days\)' option now shows as selected in the time range picker and is correctly translated.
-   Service health percentages now display correctly in locales using a comma as the decimal separator.
-   Ellipsis menu items in the Log Viewer now display in the user's language setting.
-   Backspace behavior in Extended mode is now correct.
-   The evt\_mgmt\_admin role now has write access to Express List properties.

</td></tr><tr><td>

Setup Hub

</td><td>

1.1.2

</td><td>

New

 -   PoCs to explore LitJS and AIUX \(Horizon 2.0\) for Product Hub and Admin Home redesign/uplifts.
-   Continue defining and tracking the U2 metrics framework.
-   Explore Golden Config and App Manager Suite Installation APIs for installs.

 Fixed

 GA defect fixes.

</td></tr><tr><td>

Setup Hub Common

</td><td>

3.1.1

</td><td>

New

 -   PoCs to explore LitJS and AIUX \(Horizon 2.0\) for Product Hub and Admin Home redesign/uplifts.
-   Continue defining and tracking the U2 metrics framework.
-   Explore Golden Config and App Manager Suite Installation APIs for installs.

 Fixed

 GA defect fixes.

</td></tr><tr><td>

Setup Hub Config

</td><td>

3.1.2

</td><td>

New

 -   PoCs to explore LitJS and AIUX \(Horizon 2.0\) for Product Hub and Admin Home redesign/uplifts.
-   Continue defining and tracking the U2 metrics framework.
-   Explore Golden Config and App Manager Suite Installation APIs for installs.

 Fixed

 GA defect fixes.

</td></tr><tr><td>

Setup Hub Content

</td><td>

3.1.2

</td><td>

New

 -   PoCs to explore LitJS and AIUX \(Horizon 2.0\) for Product Hub and Admin Home redesign/uplifts.
-   Continue defining and tracking the U2 metrics framework.
-   Explore Golden Config and App Manager Suite Installation APIs for installs.

 Fixed

 GA defect fixes.

</td></tr><tr><td>

Smart Assessment Core

</td><td>

22.4.0

</td><td>

Fixed: A minor defect regarding the Activity formatter.

</td></tr><tr><td>

sn-app-analytics-center

</td><td>

8.4.1

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-chart-drilldown-configuration

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-component-builder

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-config-panel

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-create-dashboard-modal

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-create-indicator-modal

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-dashboard-categories

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-data-visualization-wrapper

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-divider

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-dynamic-renderer

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-export-email-composer

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-export-modal

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-info-content

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-info-panel

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-insights-panel

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-saved-data-visualization

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-scheduled-export

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-share-dialog

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-components-share-info

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-app-par-nacm-component

</td><td>

8.4.3

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

sn-experiment-ui

</td><td>

1.1.14

</td><td>

Changed: The consent agreement language has been modified to broader terms in order to reflect the inputs provided by the Legal Team.

</td></tr><tr><td>

sn-task-planner

</td><td>

22.12.0

</td><td>

New

 Added a configuration slot to support the AI Specialist use case.

</td></tr><tr><td>

sn-viz-designer

</td><td>

8.4.1

</td><td>

Fixed

 Dashboards and Visualizations

 -   Strategy Execution Dashboard: Resolved permission error \('You do not have permission to access this page'\) when clicking widgets.
-   Dashboard Data Integrity: Fixed issue where visualizations on dashboard tabs were unexpectedly overwritten with data from other sources.
-   Widget Interactions: Restored drag-and-resize functionality for widgets in Platform Analytics Experience Bundle.
-   Visualization Rendering: Resolved delay when adding visualizations to dashboards from Explorer with the 'Show data for selected period as = Avg' option.
-   Chart Display: Fixed column chart bars widening unexpectedly when hiding a data source on Business Calendar monthly charts.

 Filters and Date Handling

 -   'Today' Predefined Range: Corrected 'Today' filter to display the full calendar day instead of starting from the current hour.
-   Date Field Filters: Fixed timezone handling for 'ON' and 'NOT ON' operators, and resolved date field filters \(Created, Updated, Viewed\) returning records from previous dates.
-   Dashboard Drilldown: Fixed full page refresh during drilldown actions in Service Operations Workspace that caused loss of unsaved work notes.

 Exports and Scheduled Reports

 -   Scheduled Exports: Improved validation messaging when attempting to save without completing mandatory fields.
-   Migrated Scheduled Reports: Resolved case sensitivity issue preventing report owners from editing or deleting migrated scheduled reports.
-   Export Visibility: Updated export button display to respect dashboard and visualization designer export properties.

 Navigation and Accessibility

 -   Cross-tab Navigation: Enabled CTRL + Click to open dashboards and visualizations in new tabs or windows from Platform Analytics on Windows.
-   Visualization Properties: Improved clarity between widget-level and visualization-level properties in the config panel.

 Internationalization

 -   Text Localization: Fixed hardcoded 'activate,' 'deactivate,' and 'delete' text in analytics overview to support translation.
-   RTL Support: Corrected dashboard title order and close button orientation for right-to-left languages \(Arabic, Hebrew\) in Service Operations Workspace.

</td></tr><tr><td>

Software Asset Management

</td><td>

4.1.4

</td><td>

Minor defect fixes related to reconciliation flow performance and lifecycle report.

</td></tr><tr><td>

Software Asset Management AI Advanced

</td><td>

2.1.0

</td><td>

Starting this version, features that rely on Now Assist for SAM use alternate third-party LLMs selected per use case, rather than the default Now LLM.

</td></tr><tr><td>

Software Asset Management AI Prime

</td><td>

2.1.1

</td><td>

Starting this version, features that rely on Now Assist for SAM use alternate third-party LLMs selected per use case, rather than the default Now LLM.

</td></tr><tr><td>

Software Asset Workspace

</td><td>

11.0.15

</td><td>

In this version, the Software Asset Workspace includes the following fixes:

 -   Security fix for Multi Record Associator pop-up page.
-   Fixed incompatible script in 'SAM - Software Estate Weekly Job' PA Job.

</td></tr><tr><td>

SOM for Manufacturing Advanced

</td><td>

1.2.0

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

SOM for Manufacturing Prime

</td><td>

1.2.0

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

SPM Enterprise-Wide Deployment

</td><td>

1.0.1

</td><td>

Fixed

 Resolved a dependency issue affecting system stability.

</td></tr><tr><td>

SPM Planning Attributes Core

</td><td>

1.16.1

</td><td>

New

 Using common schedule for group resource assignments.

 Fixed

 -   Optimized resource sync API and schedule fetch performance.
-   Admin config roles check for resource finder.
-   Fixed Resource Assignment creation to correctly populate plan start and end dates in Strategic Planning Workspace.
-   Fixed decimal field behavior to properly handle comma and dot separators in Resource Management workspace.
-   Fixed effort editing on child resource assignments with actuals to retain actual values.
-   Fixed attribute updates on unassigned assignments to properly recreate daily records.
-   Fixed end date calculation in Recalculate Resource Cost to respect MM-DD-YYYY format correctly.

</td></tr><tr><td>

Supplier Case Management

</td><td>

11.0.4

</td><td>

Fixed

 -   Requests raised by a supplier contact from the Supplier Collaboration Portal now correctly transition to the 'New' state.
-   Contact invitation for a supplier from workspace and Supplier collaboration portal is fixed.
-   Default supplier catalog item shows list of suppliers.
-   Supplier filtering conditions accepted in document configs validated.
-   Resolved catalog item visibility issue while creating supplier task of action type- 'Complete a form'.

</td></tr><tr><td>

Supplier Common Architecture

</td><td>

11.0.6

</td><td>

Fixed

 -   Requests raised by a supplier contact from the Supplier Collaboration Portal now correctly transition to the 'New' state.
-   Contact invitation for a supplier from workspace and Supplier collaboration portal is fixed.
-   Default supplier catalog item shows list of suppliers.
-   Supplier filtering conditions accepted in document configs validated.
-   Resolved catalog item visibility issue while creating a supplier task of action type- 'Complete a form'.

</td></tr><tr><td>

Talent profile

</td><td>

7.0.1

</td><td>

No Functional updates.

</td></tr><tr><td>

Third-party Risk Management Advanced

</td><td>

22.3.4

</td><td>

New

 Added support for Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini models.

 Changes

 Updated Azure OpenAI gpt-5.4-mini as default model for issue recommendation skill.

</td></tr><tr><td>

Third-party Risk Management Professional Plus

</td><td>

22.3.4

</td><td>

New

 Added support for Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini models.

 Changes

 Updated Azure OpenAI gpt-5.4-mini as default model for issue recommendation skill.

</td></tr><tr><td>

Threat Intelligence Security Center - Advanced

</td><td>

3.0.1

</td><td>

New

 Introduced Report Authoring capability with customizable styling options. Analysts can now generate AI-powered threat intelligence reports directly from threat case data with simple instructions to guide content, focus, and formatting.

 Fixed

 Enhanced case summarization with improved performance and faster response times while maintaining summary quality.

</td></tr><tr><td>

Threat Intelligence Security Center for Security Operations

</td><td>

4.7.0

</td><td>

Fixed

 -   Resolved modal loading issues when fetching related records in Investigation Canvas.
-   Fixed the issue with Affected Services retrieval while fetching vulnerability related data in Internal Intelligence.
-   Improved observable correlation logic to prevent valid relationships from being skipped when existing self-relations are present.
-   Fixed the Done button in Scoping Hunt task stage to properly advance the workflow to completion.

</td></tr><tr><td>

TNI - Advanced

</td><td>

2.0.2

</td><td>

Same NI/DCN GenAI content as DCNAM - Advanced \(shared app-nidcn-gen-ai app\): agentic data center infrastructure allocation - free-text request interpretation, autonomous policy/capacity-aware allocation agent, DC-planner policy UI, power/space/temperature validators, rack visualization with traceability, the 'DC Infrastructure Allocation' change model, and AIEL workspace integration.

</td></tr><tr><td>

TNI and DCNAM AI Content Collection

</td><td>

2.0.1

</td><td>

Updated content collection bundling the latest TNI and DCNAM GenAI and Agentic AI capabilities, including the agentic data center infrastructure-allocation agent \(free-text request interpretation, autonomous policy/capacity-aware allocation, validators, rack visualization, and workspace integration\). See the individual app release notes for detail.

</td></tr><tr><td>

TSOM - Advanced

</td><td>

2.0.2

</td><td>

Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

TSOM - Prime

</td><td>

2.0.1

</td><td>

Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

Unified Developer Core

</td><td>

29.2.7

</td><td>

This app is a dependency of ServiceNow Studio + ServiceNow IDE. See the ServiceNow Studio + ServiceNow IDE listing for release notes.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Advanced

</td><td>

2.1.0

</td><td>

New

 Added support for Azure OpenAI and Google Gemini models across all Now Assist AI features, giving you more flexibility in LLM provider selection.

 Changed

 Now Assist skills now use third-party LLM providers as the default for the following capabilities: Remediation Assistance, Vulnerable Item Deduplication, Approver Recommendation, Security Exposure Management \(SEM\) Important Insights, and SPC Setup Connector.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Foundation

</td><td>

2.1.0

</td><td>

New

 Added support for Azure OpenAI and Google Gemini models across all Now Assist AI features, giving you more flexibility in LLM provider selection.

 Changed

 Now Assist skills now use third-party LLM providers as the default for the following capabilities: Vulnerable Item Deduplication, Security Exposure Management \(SEM\) Important Insights.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Prime

</td><td>

2.1.0

</td><td>

New

 Added support for Azure OpenAI and Google Gemini models across all Now Assist AI features, giving you more flexibility in LLM provider selection.

 Changed

 Now Assist skills now use third-party LLM providers as the default for the following capabilities: Remediation Assistance, Vulnerable Item Deduplication, Approver Recommendation, Security Exposure Management \(SEM\) Important Insights, and SPC Setup Connector.

</td></tr><tr><td>

Usage Insights Application

</td><td>

6.3.9

</td><td>

What's new?.

 -   Conversations - A dedicated view of chat activity from chat assistants like Now asisst virtual agent, including total chat users, live agent transfers, and the full sequence of chat events from conversation start to response. Analyze trends over time and drill into any individual conversation.
-   Cross-application conversion funnels - Build funnels where each step can belong to a different application, so you can follow a user journey as it spans multiple workspaces and portals.
-   Session-based and user-based funnels - Choose whether steps must complete within one session \(time-to-value\) or across multiple sessions over time \(overall task completion\).
-   Previous period comparison in conversion funnel - Compare completion rate, step conversion, and transition timing against a prior period. Each metric shows its delta, and a step comparison table breaks down engaged users, sessions, and conversion time side by side - turning a snapshot into an adoption trend.

</td></tr><tr><td>

Usage Insights Commons

</td><td>

6.3.9

</td><td>

Internal app.

</td></tr><tr><td>

Usage Insights Commons Connected

</td><td>

6.3.9

</td><td>

Internal app.

</td></tr><tr><td>

Usage Insights Funnel Core

</td><td>

6.3.9

</td><td>

Internal app.

</td></tr><tr><td>

Usage Insights in Data Visualizations

</td><td>

6.3.9

</td><td>

Graphically represent funnels as part of data visualizations.

</td></tr><tr><td>

Usage Insights Pages

</td><td>

6.3.9

</td><td>

Internal app.

</td></tr><tr><td>

Usage Insights Query Builder

</td><td>

6.3.9

</td><td>

Internal app.

</td></tr><tr><td>

Usage Insights Query Builder Core

</td><td>

6.3.9

</td><td>

Internal App.

</td></tr><tr><td>

Usage Insights Request Manager

</td><td>

6.3.9

</td><td>

Not visible on UI, internal app.

</td></tr><tr><td>

Value dashboard for AI Control Tower

</td><td>

5.2.1

</td><td>

Fixed

 -   Resolved incorrect sorting of creator skill names in the metrics dashboard. Non-numeric skill columns now sort alphabetically by name for easier identification and analysis.
-   Fixed error handling in the AI Value API. The system now properly reports errors when retrieving value lists instead of returning incomplete data silently.
-   Improved reliability of asset metrics retrieval. The API now accurately indicates when requested metric streams are unavailable, preventing false success reports.
-   Corrected retry logic in background job processing. Job status manager now properly retries failed metric calculation jobs, improving scheduling reliability for cost and value analysis.

</td></tr><tr><td>

Value Engine

</td><td>

5.2.1

</td><td>

Fixed

 -   Resolved incorrect sorting of creator skill names in the metrics dashboard. Non-numeric skill columns now sort alphabetically by name for easier identification and analysis.
-   Fixed error handling in the AI Value API. The system now properly reports errors when retrieving value lists instead of returning incomplete data silently.
-   Improved reliability of asset metrics retrieval. The API now accurately indicates when requested metric streams are unavailable, preventing false success reports.
-   Corrected retry logic in background job processing. Job status manager now properly retries failed metric calculation jobs, improving scheduling reliability for cost and value analysis.

</td></tr><tr><td>

Voice input for Now Assist

</td><td>

1.5.0

</td><td>

Maintenance fixes.

</td></tr><tr><td>

WDF Unified Hub

</td><td>

1.1.0

</td><td>

The Now Assist Panel is now enabled on the Workflow Data Fabric home page, providing real-time AI guidance for navigation, configuration, and troubleshooting without leaving the app.

</td></tr><tr><td>

Workplace Case Management

</td><td>

1.28.8

</td><td>

New

 No items in this release.

 Changed

 No items in this release.

 Fixed

 -   JSON payloads sent through case utilities are now correctly formatted, preventing processing errors in downstream integrations.
-   Workplace cases now appear correctly on the My Requests page, ensuring employees can track all their submitted requests in one place.
-   Access control for Move and Maintenance cases is now consistent with Workplace cases, closing a gap in permission enforcement.
-   Lead Time unavailable state now applies reliably in all scenarios, eliminating intermittent failures in availability calculations.

 Removed

 No items in this release.

</td></tr><tr><td>

Workplace Central

</td><td>

1.16.5

</td><td>

New

 No items in this release.

 Changed

 No items in this release.

 Fixed

 -   Security fixes.
-   UI actions on the Reservation record page now display correctly - the Record Page action script no longer incorrectly filters out valid UI action types.
-   The Close button and related UI text are now properly right-to-left \(RTL\) aligned for languages such as Arabic.
-   The Workplace Central landing page workspace layout now renders correctly for RTL languages.

 Removed

 No items in this release.

</td></tr><tr><td>

Workplace Concierge

</td><td>

1.7.11

</td><td>

New

 Changed

 Fixed

 Building timezone was not returned when retrieving the presence exceptions in conversational experiences.

 Removed

</td></tr><tr><td>

Workplace Core

</td><td>

2.28.5

</td><td>

New

 No items in this release.

 Changed

 No items in this release.

 Fixed

 -   The clear \( and times;\) button on the Building field is now reachable as a distinct focus stop for VoiceOver users, improving accessibility for screen reader navigation.
-   The location directory legend now displays a color swatch next to every neighborhood, even when more than approximately 145 neighborhoods are configured.
-   Users in the Reservation Portal can now only see neighborhoods they are assigned to in the dropdown menu.

 Removed

 No items in this release.

</td></tr><tr><td>

Workplace Indoor Mapping

</td><td>

1.18.6

</td><td>

New

 Changed

 Fixed

 -   Added the favorite icon to Location Directory space cards in card view.
-   Improved hover behavior for neighborhood, campus, building, and floor information on Location Directory space cards.
-   Corrected neighborhood information displayed on Location Directory space cards when neighborhoods are disabled.
-   Improved configuration of the record producer and catalog category used by the 'Raise a Request' action in Location Directory.
-   Added support for redirection to configurable pages from Location Directory space cards.
-   Improved map display in Kiosk portrait mode.

 Removed

</td></tr><tr><td>

Workplace Lease Administration

</td><td>

1.8.5

</td><td>

New

 Changed

 Fixed

 -   Certain UI actions were not showing up in Workplace central if Asset management workspace plugin was not installed.
-   Filters for the location related lists after creating a lease contract could change.

 Removed

</td></tr><tr><td>

Workplace Maintenance Management

</td><td>

1.11.5

</td><td>

New

 No items in this release.

 Changed

 No items in this release.

 Fixed

 Date formats in Workplace Maintenance Management are now localized correctly, respecting regional formatting preferences instead of displaying a hardcoded format.

 Removed

 No items in this release.

</td></tr><tr><td>

Workplace Move Management

</td><td>

1.14.5

</td><td>

New

 No items in this release.

 Changed

 No items in this release.

 Fixed

 -   Security fixes.
-   Bulk upload in Move Management now processes files correctly, resolving multiple issues that caused uploads to fail or produce incorrect results.

 Removed

 No items in this release.

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

3.5.0

</td><td>

New

 Changed

 Improve performance of reservation search page.

 Fixed

 -   Reservations created through Outlook and conflicted with an existing reservation could be indicated as cancelled.
-   The reservation search could show the previously selected floor when switching between reservable modules.
-   Past reservations now display consistently in a user's reservation history.
-   Extra services configured with a record producer now retain the values entered before the reservation is submitted.
-   Changing reservable modules with different max days in the future could result in employees who cannot select a day in the future.
-   In some cases, the recurring score was not calculated correctly when a conflict exists in the middle of a planned series.
-   Previously selected date was displayed when reloading the page, while the map was loading.
-   It was not possible to reserve space on the Workplace Kiosk using certain date and time formats.
-   A conflicted reservation could move to a confirmed state after updating the reservation without any changes.
-   Extra-services handling in the Outlook add-in behaved inconsistently when changing date, time, location, or the all-day setting.
-   The 'To Time' field would not reflect the correct timing when all day is required for a reservable module.
-   Search result counts were displayed incorrectly after changing the floor.
-   Push notifications were not sent to attendees when a group reservation got cancelled.
-   Microsoft Exchange login prompt was not displayed, as required, when using the NowMobile application while reserving spaces.
-   Min and max duration were not always correctly available within conversational experiences.
-   Availability checks on department, neighborhood, and more were not always available within conversational experiences.
-   Employees with Australia/Melbourne timezone and specific date formats could book spaces for future dates via the location directory on NowMobile.
-   Blocker reservations could get stuck in awaiting approval when approvals were required.
-   Several design enhancements for recurring reservations, using the Outlook add-in, filter button alignment, and more.
-   Quick actions and the status badge on the Waitlist Summary page now align correctly on mobile for Confirmed and Queued states.
-   The right-hand chevron is now visible in the Schedule view of Make a Reservation on mobile browsers.
-   The reservation page schedule view displayed the date and time in the correct format.
-   General accessibility improvements for screen readers and other areas.
-   Improvements to translations when adding attendees, creating a recurring series, selecting the reservable module, and more.
-   Improvements to translations to the Event Planner in Workplace Central.
-   Improvements to support ATF tests.

 Removed

</td></tr><tr><td>

Workplace Space Management

</td><td>

1.20.5

</td><td>

New

 No items in this release.

 Changed

 No items in this release.

 Fixed

 -   Security fixes.
-   Space selection and allocation interactions in the space assignment flow now work correctly, resolving multiple UI interaction issues.
-   Translation strings and UI labels in Space Management now display accurately across supported languages.
-   Visual padding and spacing in the Space selection panel and Neighborhood panel are now consistent and properly aligned.
-   Scenario planning views now accurately reflect space groups when grouped by workplace entity or neighborhood, eliminating display gaps.
-   The floor styles REST API now returns a proper 400 error response when required query parameters are missing, instead of an unhelpful 500 error.
-   Padding and spacing are now consistent throughout the Space Management application.
-   The Assign Users modal in space selection now functions correctly.
-   Removing a neighborhood space no longer incorrectly deletes the associated Space Details record in Space Optimization.
-   The scenario list view now refreshes correctly, and the processing state filter in View Scenarios works as expected.
-   Scenario readers can now access query results correctly - an access control issue affecting read-only scenario roles has been resolved.

 Removed

 No items in this release.

</td></tr><tr><td>

Workplace Visitor Management

</td><td>

2.0.11

</td><td>

This release introduces breaking changes. Please review the impact on your current configuration and user experience before upgrading.

 New

 -   Added a Receptionist page to manage the full visitor flow from a single place.
-   Introduced a Host page for employees to view, update, or cancel visits.
-   Launched a secure Visitor portal to complete pre-visit steps and access visit details.
-   Enabled dynamic, condition-based visitor check-in flows.
-   Introduced the Workplace Concierge AI agent to automate visit creation and management from email, calendar invites, and Now Assist.

 Changed

 -   Migrated the product to use Workplace locations instead of CMN locations.
-   Replaced the record producer in the 'Register a guest' page with the new requirements configuration.
-   Centralized the check-in configuration flow into the Visit Requirements model, enabling dynamic, condition-based configurations.
-   Replaced the record producer in the kiosk self-registration with the new requirements configuration.
-   Updated kiosk self-registration to display forms instead of one question per page.

 Fixed

 -   Removed an issue affecting the phone number self check-in option.
-   Enabled support for phone numbers formatted with dashes during kiosk check-in and check-out.
-   Fixed an issue where visitor QR codes did not display correctly on Windows devices.
-   Resolved several badge printing issues.
-   Resolved multiple issues affecting the Register a Guest experience, including validation, draft saving, mobile display, and email formatting.
-   Applied security fixes.
-   Improved support for overnight and multi-day visits.
-   Applied translation improvements.
-   Corrected recurring invitations creating visits beyond the configured end date.
-   Improved the Visitor Portal mobile experience.
-   Reduced excessive logging in Visitor Management.
-   Corrected duplicate or blank policy acknowledgments during kiosk check-in.

 Removed

</td></tr><tr><td>

Zero Touch Service Desk

</td><td>

2.3.5

</td><td>

This release focused on improving the quality and accuracy of AI Specialists responses as well as consolidating feedback management.

 Key features:

 Memory bank to give AI Specialists context of resolutions that lead to positive outcomes

 AI Specialists now have an updated memory type that enables them to reference past resolutions that led to a positive outcome on assigned records.

 This is disabled by default for this release, but can be enabled by administrators via system properties.

 Consolidated feedback visibility

 Feedback given on records that an AI Specialist is assigned to will now appear in the AI Specialist activity tab. Admins and managers now have a consolidated view of all feedback given to the AI Specialist.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@devsnc/behavior-form-intent-translator|29.0.9|2026-03-12|
|@devsnc/behavior-list-intent-translator|29.0.9|2026-03-12|
|@devsnc/behavior-uibtk-media|29.1.71|2026-03-12|
|@devsnc/behavior-uibtk-supporting-records|29.1.71|2026-03-12|
|@devsnc/behavior-ui-interaction|29.1.14|2026-03-12|
|@devsnc/library-uibtk-caching|29.1.71|2026-03-12|
|@devsnc/library-uibtk-commons|29.1.71|2026-03-12|
|@devsnc/library-uibtk-macroponent|29.1.71|2026-03-12|
|@devsnc/library-uibtk-screen|29.1.71|2026-03-12|
|@devsnc/library-uibtk-undo-redo|29.1.71|2026-03-12|
|@devsnc/library-uibtk-uxvalue|29.1.71|2026-03-12|
|@devsnc/library-uibtk-ux-value-resolver|29.1.71|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-devops-pipeline|21.0.5|2022-08-04|
|@devsnc/sn-feedback|2.0.0|2025-12-11|
|@devsnc/sn-help-setup|29.0.0|2026-03-12|
|@devsnc/sn-interaction-builder|29.1.37|2026-03-12|
|@devsnc/sn-list-selector|26.1.3|2026-03-12|
|@devsnc/sn-par-calendar-connected|29.0.8|2026-04-09|
|@devsnc/sn-uibtk-actionable-list-item|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-builder-in-builder|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-client-state-config-panel|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-conditional-renderer|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-content-tree-picker|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-create-page|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-data-navigator|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-diff-renderer|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-domain-picker|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-draggable-dialog|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-draggable-list|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-editor-header|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-element-context-menu|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-element-navigator|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-element-properties-configuration-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-events-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-experience-assistant|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-extension-point-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-features-catalog-modal|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-form-factor-controls|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-formula-builder|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-icon|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-instance-config-editor|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-is-hidden-property-input|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-json-navigator|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-loader|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-mcp-event-definitions-config-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-mcp-props-config-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-menu-elements|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-minimized-dialogs-dropdown|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-modal|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-param-row|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-placeholder|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-preset-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-props-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-replace-component|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-scope-picker|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-script-config-panel|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-shelf-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-site-map|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-stage-preview|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-stage-scale-controls|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-style-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-style-provider|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-style-select|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-tabs|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-test-values-editor|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-text-link|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-toolbox|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-transaction-alert|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-viewport-config-panel|29.1.71|2026-03-12|
|@devsnc/sn-ui-interaction-modals|29.1.14|2026-03-12|
|@devsnc/sn-vtb|26.0.0|2025-12-11|
|@devsnc/uibtk-api|29.1.71|2026-03-12|
|@devsnc/uibtk-uxf-assets|29.1.71|2026-03-12|
|@now-par-components/macroponent-provider|29.0.8|2026-04-09|
|@now-par-components/sn-par-additional-group-by|29.0.8|2026-04-09|
|@now-par-components/sn-par-breakdowns|29.0.8|2026-04-09|
|@now-par-components/sn-par-chart-size|29.0.8|2026-04-09|
|@now-par-components/sn-par-colors|29.0.8|2026-04-09|
|@now-par-components/sn-par-color-selector|29.0.8|2026-04-09|
|@now-par-components/sn-par-data-sources|29.0.8|2026-04-09|
|@now-par-components/sn-par-date-input|29.0.8|2026-04-09|
|@now-par-components/sn-par-dot-walk|29.0.8|2026-04-09|
|@now-par-components/sn-par-draggable-list|29.0.8|2026-04-09|
|@now-par-components/sn-par-duration-format|29.0.8|2026-04-09|
|@now-par-components/sn-par-filter-per-metric|29.0.8|2026-04-09|
|@now-par-components/sn-par-group-by|29.0.8|2026-04-09|
|@now-par-components/sn-par-metricbase|29.0.8|2026-04-09|
|@now-par-components/sn-par-metrics|29.0.8|2026-04-09|
|@now-par-components/sn-par-number-format|29.0.8|2026-04-09|
|@now-par-components/sn-par-pillar|29.0.8|2026-04-09|
|@now-par-components/sn-par-popover|29.0.8|2026-04-09|
|@now-par-components/sn-par-ranges|29.0.8|2026-04-09|
|@now-par-components/sn-par-refresh-frequency|29.0.8|2026-04-09|
|@now-par-components/sn-par-scorecard-aggregates|29.0.8|2026-04-09|
|@now-par-components/sn-par-scorecard-metrics|29.0.8|2026-04-09|
|@now-par-components/sn-par-toggle|29.0.8|2026-04-09|
|@now-par-components/sn-par-trend-by|29.0.8|2026-04-09|
|@now-par-components/sn-par-visualization-controls-section|29.0.8|2026-04-09|
|@now-par-components/sn-par-visualization-header|29.0.8|2026-04-09|
|@now-par-components/sn-par-widget-header|29.0.8|2026-04-09|
|@servicenow/now-score|29.0.8|2026-04-09|
|@servicenow/now-vis-bar|29.0.8|2026-04-09|
|@servicenow/now-vis-boxplot|29.0.8|2026-04-09|
|@servicenow/now-vis-dial|29.0.8|2026-04-09|
|@servicenow/now-vis-gauge|29.0.8|2026-04-09|
|@servicenow/now-vis-navigator|29.0.8|2026-04-09|
|@servicenow/now-vis-pie|29.0.8|2026-04-09|
|@servicenow/now-vis-sparkline|29.0.8|2026-04-09|
|@servicenow/now-vis-timeseries|29.0.8|2026-04-09|
|@servicenow/sn-builder-core|29.1.59|2026-03-12|
|@servicenow/sn-cb-api|27.2.29|2025-05-01|
|@servicenow/sn-cb-asset-picker|27.2.29|2025-05-01|
|@servicenow/sn-cb-commons|27.2.29|2025-05-01|
|@servicenow/sn-cb-events-navigator|27.2.29|2025-05-01|
|@servicenow/sn-cb-experiences|27.2.29|2025-05-01|
|@servicenow/sn-cb-presets|27.2.29|2025-05-01|
|@servicenow/sn-cb-property-navigator|27.2.29|2025-05-01|
|@servicenow/sn-cb-property-pane|27.2.29|2025-05-01|
|@servicenow/sn-cb-slide-modal|27.2.29|2025-05-01|
|@servicenow/sn-cb-theme-picker|27.2.29|2025-05-01|
|@servicenow/sn-cb-usage|27.2.29|2025-05-01|
|@servicenow/sn-component-builder|29.1.32|2026-03-12|
|@servicenow/sn-controller-builder|29.1.30|2026-03-12|
|@servicenow/sn-next-experience-all-menu-editor|29.1.81|2026-03-12|
|@servicenow/sn-preset-builder|29.1.28|2026-03-12|
|360 degree relationship visualization|22.3.0|2026-06-16|
|ACC Admin Workspace|1.0.0|2025-12-11|
|Access Analyzer|6.0.6|2026-05-21|
|Access Management Automation|2.1.0|2023-12-07|
|Access Management Flow Wizards|1.0.1|2021-09-16|
|Accounts Payable Invoice Processing|13.0.1|2026-06-16|
|Accounts Payable Operations integration with Document Intelligence|13.0.1|2026-06-16|
|ACL Assessment for Reports|3.1.2|2025-01-30|
|Action Status Automation|2.0.0|2026-03-12|
|Activity Timer|1.0.2|2026-03-12|
|Admin Experience Framework|5.3.0|2026-03-12|
|Administration for Security Exposure Management|30.1.4|2026-01-20|
|Admin Workspace for Service Providers \(SPs\)|1.1.4|2025-07-31|
|Adobe Experience Platform Spoke|2.2.0|2025-01-02|
|Adobe Sign Spoke|2.7.2|2025-10-16|
|Advanced AI Search Management Tools|8.0.1|2025-12-11|
|Advanced Appointment Booking|30.0.1|2026-03-12|
|Advanced Promotion Engine|4.2.1|2025-12-11|
|Advanced Recommended actions for ITSM|8.1.0|2025-09-10|
|Advanced Response Automation for Smart assessments|22.3.0|2026-06-16|
|Advanced Response Automation for Smart assessments|22.3.0|2026-06-16|
|Advanced Work Assignment for CSM|1.0.4|2026-03-12|
|Advanced Work Assignment for Legal Service Delivery|1.1.1|2025-06-05|
|Advanced Work Assignment for Source-to-Pay Operations|3.1.1|2025-12-11|
|Advanced Work Assignment for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|Advanced Work Assignment for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|Advanced Work Assignment for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|Advanced Work Assignment for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|AES Application Object Templates|29.2.1|2026-06-16|
|AES Application Object Wizard Components|29.2.1|2026-06-16|
|AES Catalog Builder|28.2.1|2025-12-11|
|AES Catalog Builder Wizard|28.2.1|2025-12-11|
|AES Decision Table Builder Templates|4.0.0|2023-02-02|
|AES Decision Table Builder Wizard|4.0.0|2023-02-02|
|AES Flow Templates|28.2.1|2025-12-11|
|AES Flow Wizards|28.2.1|2025-12-11|
|AES Mobile Templates|28.2.1|2025-12-11|
|AES Mobile Wizards|28.2.1|2025-12-11|
|AES Notification Builder Component|28.2.1|2025-12-11|
|AES Portal UI Template|28.2.1|2025-12-11|
|AES Role Builder|28.2.1|2025-12-11|
|AES Role Builder Component|28.2.1|2025-12-11|
|AES Table Builder Wizard|28.2.1|2025-12-11|
|AES UI Template Wizards|28.2.1|2025-12-11|
|AES Workspace UI Template|28.2.1|2025-12-11|
|Agency Support Model|3.0.0|2026-06-16|
|Agent Client Collector for Investigation|9.2.0|2026-06-16|
|Agent Client Collector for Security Incident Response|20.2.0|2023-05-04|
|Agent Client Collector for Visibility Content|1.9.0|2026-06-16|
|Agent Client Collector Framework|6.5.1|2026-06-18|
|Agent Client Collector Log Analytics|3.9.1|2025-12-11|
|Agent Client Collector Monitoring|3.16.1|2026-01-20|
|Agent Client Collector Spoke|1.1.5|2024-01-04|
|Agent Forecast|5.7.1|2026-03-12|
|Agentic Contact Center for Banking|1.3.0|2026-06-16|
|Agentic Contact Center for Banking|1.3.0|2026-06-16|
|Agent-Initiated Messaging Interface|1.0.22|2026-03-12|
|Agent Messaging Component|3.0.17|2026-03-12|
|Agent Workspace for HR Case Management|4.6.0|2026-06-16|
|Agile Development v2|1.1.0|2023-02-02|
|Agile Integrations Common|1.4.0|2025-12-11|
|Aha! Spoke|1.7.2|2026-01-20|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for Customer Success Management|2.7.4|2026-06-16|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.1|2026-06-16|
|AI agents for SLO|2.0.3|2026-06-16|
|AI Agents for Workplace Service Delivery|3.3.1|2026-06-16|
|AI Agents Platform Usecase|1.0.5|2025-03-12|
|AI Discovery|2.0.6|2026-04-09|
|AI for document designer|22.3.4|2026-06-16|
|AIOps Dashboards|26.3.1|2026-06-16|
|AI Risk and Compliance Content|21.1.1|2025-12-11|
|AI Search Admin Console|9.0.5|2026-06-16|
|AI Search for Customer Portals|1.1.0|2025-12-11|
|AI Search For Next Experience|5.0.2|2026-02-05|
|AI Search RAG|6.1.0|2026-06-16|
|AI Search Spoke|2.0.3|2023-09-20|
|AI Security and Privacy|4.1.3|2026-05-06|
|AI Service Graph Connector for Amazon|1.0.4|2026-03-12|
|AI Service Graph Connector for Databricks|1.0.2|2026-04-09|
|AI Service Graph Connector for GCP Vertex AI|1.0.4|2026-03-12|
|AI Service Graph Connector for LangGraph|1.1.0|2026-03-12|
|AI Service Graph Connector for Microsoft|2.0.0|2026-03-12|
|AI Service Graph Connector for n8n|1.0.2|2026-04-09|
|AI Service Graph Connector for Salesforce|1.0.2|2026-03-12|
|AI SGC Discovery|1.0.0|2026-04-09|
|AI Websearch|4.1.0|2026-06-16|
|Aleph Alpha Spoke|1.0.2|2025-01-30|
|Alert Rules Management|18.15.9|2026-06-16|
|Alumni Center|4.0.2|2025-12-11|
|Amazon Alexa Spoke|1.1.0|2024-11-07|
|Amazon Bedrock Spoke|1.5.0|2026-06-16|
|Amazon CloudWatch Spoke|1.0.2|2022-12-01|
|Amazon Connect Spoke|1.2.0|2025-03-12|
|Amazon DynamoDB Spoke|1.0.1|2022-09-01|
|Amazon EBS Spoke|1.0.2|2023-09-20|
|Amazon EC2 Spoke|1.4.0|2025-09-10|
|Amazon Elastic Container Service Spoke|1.0.2|2023-09-07|
|Amazon RDS Spoke|1.0.5|2025-06-05|
|Amazon Route 53 Spoke|1.0.2|2022-12-01|
|Amazon S3 Spoke|1.2.1|2024-09-10|
|Amazon SNS Spoke|1.1.0|2023-09-07|
|Amazon SQS Spoke|1.0.1|2025-01-02|
|Amazon VPC Spoke|1.0.3|2023-09-07|
|Analytics Pack for Contract Management Pro|1.2.0|2025-05-01|
|Ansible Spoke|2.2.9|2024-12-05|
|API Insights|2.2.1|2025-12-11|
|API Notification Management|4.0.1|2025-12-11|
|API Service Graph Connector for Apigee X|2.2.2|2025-10-16|
|API Service Graph Connector for AWS API Gateway|2.2.0|2025-09-10|
|API Service Graph Connector for Azure API Management|2.2.0|2025-07-31|
|API Service Graph Connector for Kong Gateway|2.1.0|2025-10-16|
|API Service Graph Connector for Kong Konnect|1.0.0|2025-10-16|
|APO - Foundation|1.2.0|2026-06-16|
|APO - Prime|1.2.0|2026-06-16|
|App Best Practices Shared|29.2.0|2026-06-16|
|App Collaboration Component|28.2.1|2025-12-11|
|App Engine Management Center|29.2.1|2026-06-16|
|App Engine Notifications|29.2.1|2026-06-16|
|App Engine - Prime|29.1.5|2026-06-16|
|App Engine Studio|28.2.1|2025-12-11|
|Application Common Configuration|29.0.8|2026-03-12|
|Application Insights|2.0.3|2021-11-18|
|Application Intake|29.2.1|2026-06-16|
|Application Portfolio Management integration with Policy and Compliance|1.0.3|2023-05-04|
|Application Portfolio Management integration with Risk Management|1.0.2|2023-05-04|
|Application Service Extensions|1.1.7|2024-11-07|
|Application spoke selector|1.5.0|2026-03-12|
|App Life Cycle AI Agents|29.3.1|2026-06-16|
|Appointment calendar component|28.1.1|2025-12-11|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|App Shell Utils|29.0.0|2026-03-12|
|ArcSight ESM Event Ingestion for Security Operations|10.5.0|2025-12-11|
|ArcSight Logger Integration for Security Operations|10.4.1|2024-11-07|
|Aria Systems Spoke|2.1.2|2023-04-06|
|Asana Spoke|1.0.3|2024-08-01|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Asset Audits|1.0.0|2026-03-12|
|Asset Management Common|15.1.2|2026-06-16|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management - Procurement Integration|1.0.1|2024-11-07|
|Asset Security Posture Management|5.5.1|2025-12-11|
|Asset Shipments|1.0.0|2026-03-12|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Atlassian Administration Spoke|1.0.1|2025-01-30|
|Atlassian Jira Integration for Agile Development|2.3.2|2025-12-23|
|Atlassian Jira Integrations Common|2.4.2|2025-12-23|
|Attribute Pack|5.0.0|2025-07-31|
|Attribute Pack|5.0.0|2025-07-31|
|Attribute Pack|5.0.0|2025-07-31|
|Attribute propagation|9.4.0|2026-06-16|
|Attribute propagation|9.4.0|2026-06-16|
|Audio player component|27.3.1|2026-03-12|
|Authentication for conversational channels|1.1.0|2026-03-12|
|Automation Anywhere Spoke|1.2.1|2025-05-01|
|AWH for AI Control Tower|2.0.9|2026-05-05|
|AWS Certificate Manager Spoke|1.0.1|2022-09-21|
|AWS CloudFormation Spoke|1.1.4|2024-03-20|
|AWS Elastic Beanstalk Spoke|1.0.3|2024-06-06|
|AWS Elastic Load Balancing Spoke|1.0.1|2022-09-01|
|AWS IAM Spoke|1.1.0|2023-07-06|
|AWS Lambda Spoke|1.1.3|2023-09-07|
|AWS OpsWorks Spoke|1.0.2|2023-09-20|
|AWS Translate Spoke|1.0.0|2022-11-03|
|Azure Active Directory User Mapping|1.11.0|2025-12-11|
|Basic Scoring for Smart Assessments|22.3.0|2026-06-16|
|Basic Scoring for Smart Assessments|22.3.0|2026-06-16|
|BCM mobile app|9.1.3|2025-12-11|
|Beans.ai Spoke|29.0.7|2026-03-12|
|BigFix Inventory Spoke|1.5.4|2023-09-07|
|Blue Prism Spoke|1.0.2|2022-09-21|
|BMC Remedy Spoke|1.4.1|2024-10-03|
|Bot Interconnect|1.7.0|2025-07-31|
|Box Spoke|3.5.1|2026-01-20|
|Breadcrumb navigation demo|27.0.0|2025-06-05|
|Breakdown Data Grid UI Component|1.4.0|2023-05-04|
|Broadcom Rally Integration with DevOps|7.0.0|2026-06-16|
|Browser Extension for Employee Center|1.1.1|2025-12-11|
|Bubble trend|1.0.0|2025-05-01|
|Build Agent Glide Tools|1.0.10|2026-03-12|
|Business Continuity Management Advanced|1.1.3|2026-06-16|
|Business Continuity Management Foundation|1.1.3|2026-06-16|
|Business domain|22.3.1|2026-06-16|
|Business Location|5.0.2|2026-03-12|
|Business Object Core|2.1.0|2025-12-11|
|Business Object Core|2.1.0|2025-12-11|
|Business Portal|2.3.0|2026-03-12|
|Calendar component|26.0.2|2026-03-12|
|Calendly Spoke|1.2.0|2023-08-03|
|Capacity Management|4.1.0|2025-12-11|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Career Assessment|3.3.0|2026-06-16|
|Career Conversations|3.10.0|2026-06-16|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Care Team Portal|2.2.0|2026-03-12|
|Care Team Portal|2.2.0|2026-03-12|
|Care Team Portal|2.2.0|2026-03-12|
|Carousel component|28.0.1|2026-03-12|
|Case Digests|2.0.0|2026-03-12|
|Case lines and workflows|4.3.0|2026-03-12|
|Case Management for Invoice Operations|1.8.0|2026-05-05|
|Case Playbook for Onboarding|8.1.0|2025-12-11|
|Case Playbook for Product Support|6.0.1|2025-07-31|
|Catalog Conversational Coverage|6.0.2|2026-05-05|
|CCG Content Pack|1.3.12|2024-11-07|
|CCO Dashboard|2.0.8|2025-12-11|
|CDM File Uploader|1.0.1|2023-11-02|
|CDO Dashboard|2.0.5|2025-12-11|
|Certificate Inventory and Management|3.14.0|2025-12-11|
|CFO Dashboard|2.0.1|2025-12-11|
|Change Management for Field Service|1.1.2|2025-01-02|
|Change Management for Service Operations Workspace|9.2.0|2026-06-16|
|Change Password Custom Component|1.3.0|2025-12-11|
|Channel Management|7.1.1|2026-03-12|
|Chat integration with Security Incident Management|1.2.10|2025-07-31|
|Chat Zoom Connector|1.0.6|2023-01-12|
|Checklist component|26.0.0|2025-12-11|
|Check Point Integration for Security Operations|10.4.10|2025-07-31|
|CHRO Dashboard|2.0.4|2025-12-11|
|CIO Dashboard|2.1.1|2025-12-11|
|Cisco Webex Meetings Spoke|2.3.3|2024-08-01|
|Cisco Webex Teams Spoke|2.3.6|2025-12-11|
|CISO Dashboard|2.0.5|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Claims for reporting|21.1.0|2025-12-11|
|Client Software Distribution 2.0|1.4.0|2025-12-11|
|CLI Metadata|1.1.2|2021-04-15|
|Clone Admin Console|2.1.7|2026-03-12|
|Cloud Access Interface|1.0.8|2024-11-07|
|Cloud Action Library|1.4.0|2024-11-07|
|Cloud Configuration Governance|1.6.0|2025-12-11|
|Cloud Deployment Automation|1.0.3|2024-12-05|
|Cloud Discovery Workspace|1.7.1|2025-05-01|
|Cloud Flow Wizards|1.2.1|2022-08-24|
|Cloudify Spoke|2.1.1|2023-04-06|
|Cloud Insights Billing|6.0.1|2024-04-04|
|Cloud Insights Billing|6.0.1|2024-04-04|
|Cloud Migration Assessment|1.4.0|2024-11-07|
|Cloud Security Posture Management|2.5.0|2024-02-01|
|Cloud Services Catalog|1.5.1|2025-12-11|
|Cloud Services Catalog Terraform Connector|1.9.1|2025-12-11|
|Cloud Spend Dashboard|1.0.3|2022-06-02|
|Cloud Storage|6.1.0|2026-03-12|
|Cloud Workspace|2.2.0|2025-12-11|
|CMDB and CSDM Data Foundations Dashboards|4.2.0|2025-12-11|
|CMDB Application for APIs and CLI|1.0.1|2021-07-22|
|CMDB CI Class Models|1.86.2|2026-06-16|
|CMDB Page Templates|3.2.6|2026-06-16|
|CMDB Workspace|9.2.0|2026-06-16|
|Coaching With Learning|5.4.2|2026-03-12|
|Coaching with Learning Migration Utility|1.0.1|2021-09-16|
|Collaboration applications - common|1.1.0|2025-12-11|
|Collaboration Request|28.2.1|2025-12-11|
|Collaboration Services|3.12.2|2025-12-11|
|Collaboration Services for Service Operations Workspace|9.2.0|2026-06-16|
|Collaboration UI Component for Major Security Incident Management Workspace|1.2.1|2024-11-07|
|Collaborative Work Management|10.0.2|2026-06-16|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Common AI Framework|1.0.1|2026-06-16|
|Common Guidances|14.0.0|2026-06-16|
|Common Service Delivery|14.0.0|2026-06-16|
|Common UIB Wrapper Components|1.5.1|2025-12-11|
|Common Vendor Core|4.5.0|2026-06-16|
|Compatibility Management|6.6.0|2026-06-16|
|Compatibility Management|6.6.0|2026-06-16|
|Configurable Workspace for Order Management|15.2.0|2026-06-16|
|Configurable Workspace for Order Management|15.2.0|2026-06-16|
|Configuration Compliance|15.5.3|2025-12-11|
|Configuration Data Management|5.0.2|2024-03-20|
|Configuration Hub|1.0.9|2025-12-11|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Confluence Cloud Spoke|1.2.6|2026-01-20|
|Confluent Kafka REST Proxy Spoke|1.0.0|2021-03-11|
|Consumer Service Portal|23.12.0|2025-12-11|
|Contact card component|26.0.0|2025-12-11|
|Contact Center Integration Core|1.4.4|2025-12-11|
|Contact Tracing|1.30.0|2025-07-31|
|Content Engagement for Employee Center Pro|1.4.1|2026-03-12|
|Content Experiences|33.0.0|2026-06-16|
|Content Publishing|37.0.1|2026-06-16|
|Context Menu Component for Configuration Data Management UI|1.2.1|2023-05-04|
|Context Rule Management|10.6.0|2026-06-16|
|Contract Management for Sales and Order Management|1.1.0|2025-12-11|
|Contract Management Pro|1.7.6|2026-06-16|
|Contract Management Pro for Legal Service Delivery|3.0.2|2025-12-11|
|Contractor Service Center|1.0.7|2025-12-11|
|Contracts and Entitlement Workflows|13.0.0|2025-12-11|
|Contracts Core|3.2.4|2026-06-16|
|Contracts Core components|1.5.1|2026-03-12|
|Contract Workspace|1.9.0|2026-06-16|
|Conversational Analytics|9.1.3|2026-03-12|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Appointment Booking|1.4.1|2026-03-12|
|Conversational Appointment Booking Components|2.0.5|2023-09-07|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Integration with Alexa|1.5.5|2024-08-01|
|Conversational Integration with Apple Messages for Business|1.3.0|2026-03-12|
|Conversational Integration with Facebook Messenger|3.0.8|2025-12-11|
|Conversational Integration with Google Business Messages|1.1.1|2024-02-01|
|Conversational Integration with Google Chat|2.0.4|2025-12-11|
|Conversational Integration with LINE|2.0.7|2025-01-30|
|Conversational Integration with Microsoft Teams|10.3.1|2026-03-12|
|Conversational Integration with Slack|6.0.6|2026-03-12|
|Conversational Integration with WhatsApp \(powered by Twilio\)|2.0.11|2025-12-11|
|Conversational Integration with Workplace from Facebook|5.0.1|2025-01-30|
|Conversational Interfaces - Diagnostics|2.2.1|2024-11-07|
|Conversational IVR with Amazon Connect|1.6.3|2025-07-31|
|Conversational SMS Integration with AWS End User Messaging|1.0.2|2025-01-30|
|Conversational SMS Integration with Twilio|4.2.4|2025-12-11|
|Conversational SMS Service Channel|2.0.23|2026-03-12|
|Conversational subflows and actions|29.2.2|2026-04-09|
|Conversation Evaluator|3.0.4|2026-06-16|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.1.0|2026-06-16|
|Core Business Suite Analytics|3.1.0|2026-06-16|
|Coupa Spoke|4.14.0|2025-10-16|
|COVID-19 Global Health Data Set|1.20.3|2024-05-09|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ Configurator|1.2.5|2025-10-14|
|CPQ Configurator|1.2.5|2025-10-14|
|CPQ - Foundation|1.0.1|2026-04-09|
|CPQ Integration|2.1.0|2025-12-11|
|CPRO Dashboard|2.0.5|2025-12-11|
|Craft.co Integration for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|Craft.co Integration for Supplier Lifecycle Operations|5.0.0|2026-06-16|
|Craft.co Integration for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|Craft.co Integration for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|Craft.co Integration for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|Craft Spoke|1.0.0|2024-11-07|
|Creator Studio|28.2.1|2025-12-11|
|Creator Studio Configurations|28.2.1|2025-12-11|
|Creator Studio Configurations|28.2.1|2025-12-11|
|Credentials Core|1.2.0|2026-06-16|
|Credly Spoke|1.1.0|2026-06-16|
|CRM Flow Wizards|1.0.1|2023-04-06|
|CRM Territory Extensions|2.0.3|2026-03-12|
|CRO Dashboard|2.0.10|2025-12-11|
|CrowdStrike Falcon EDR Integration for Threat Intelligence Security Center|3.0.0|2024-11-07|
|CrowdStrike Falcon Host for Security Operations|10.4.5|2024-11-07|
|CrowdStrike Falcon Insight Integration for Security Operations|1.4.1|2026-01-20|
|CrowdStrike Falcon Sandbox Integration for Security Operations|11.0.10|2024-09-10|
|CrowdStrike Spoke|1.1.0|2025-01-30|
|CSC Content Pack|1.7.0|2025-12-11|
|CSM Account Hierarchy|30.0.3|2026-03-12|
|CSM Account Hierarchy|30.0.3|2026-03-12|
|CSM and FSM Configurable Workspace Foundation|26.0.8|2026-03-12|
|CSM and FSM Configurable Workspace Integrations|26.0.0|2026-03-12|
|CSM Configurable Workspace|26.0.2|2026-03-12|
|CSM Configurable Workspace Lookup and Verify|26.0.0|2026-03-12|
|CSM Contributor User|2.4.0|2026-06-16|
|CSM Data Classification|1.0.0|2025-07-31|
|CSM Extension for Proxy Contacts|2.0.0|2026-03-12|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|Custom App Record Summarization|29.2.2|2026-06-16|
|Customer Contracts and Entitlements|13.1.0|2026-02-05|
|Customer Data Models for B2B2C|2.1.0|2025-07-31|
|Customer Engagement Sequences|2.0.1|2025-12-11|
|Customer Household Data Model|2.0.6|2026-03-12|
|Customer Life Cycle Management Self Service|2.1.1|2025-12-11|
|Customer Life Cycle Management Workflows|5.1.1|2025-12-11|
|Customer Project Management|2.0.0|2026-03-12|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Service Case Action Status|2.0.0|2026-03-12|
|Customer Service Case Types|4.3.1|2026-05-05|
|Customer Service Document Template|2.0.0|2026-03-12|
|Customer Service Install Base Characteristics|2.3.0|2026-03-12|
|Customer Service Install Base Management|4.8.1|2026-06-16|
|Customer Service integration with Social Media Store|1.0.2|2026-03-12|
|Customer Service NLU Model for Virtual Agent Conversations|1.0.5|2026-03-12|
|Customer Service Portal|25.3.0|2026-03-12|
|Customer Service Problem Management|5.0.2|2025-12-11|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Customer Service Virtual Agent Conversations|1.0.4|2026-03-12|
|Customer Service with Request Management|2.1.0|2026-04-09|
|Customer Service with Service Management|2.0.1|2026-03-12|
|Customer Service with Service Portfolio Management \(SPM\)|2.0.1|2025-01-30|
|Cybersecurity Executive Dashboard|2.4.3|2025-05-01|
|Dashboard and visualization export|1.3.5|2026-01-20|
|Data Collection for Oracle Global Licensing and Advisory Services|1.11.0|2025-12-11|
|Data Discovery|8.1.0|2026-03-12|
|Data Grid UI Component|26.0.7|2026-06-16|
|Data Loss Prevention Incident Response|2.2.2|2026-02-05|
|Data Model for SBOM|4.2.1|2025-12-11|
|Data Privacy|8.1.1|2026-03-12|
|Data registry|22.3.1|2026-06-16|
|Data Relationships Framework|11.0.0|2026-06-16|
|Data visualizations|29.0.8|2026-04-09|
|Decision Builder|29.1.4|2026-04-09|
|Decision Table Builder|29.1.6|2026-04-09|
|Deployment Pipeline|29.2.1|2026-06-16|
|DevOps Change Health Scan Content Pack|6.2.0|2025-12-11|
|DevOps Change Velocity|7.0.0|2026-06-16|
|DevOps Config|5.2.0|2024-11-07|
|DevOps Config Exporter Content Pack|2.3.0|2023-08-03|
|DevOps Config Policy Content Pack|1.6.0|2023-11-02|
|DevOps Data Model|7.0.0|2026-06-16|
|DevOps Feature Flag Integrations|7.0.0|2026-06-16|
|DevOps Flow Wizards|1.1.1|2022-09-21|
|DevOps Insights|7.0.0|2026-06-16|
|DevOps Integrations|7.0.0|2026-06-16|
|DevOps Integration with Argo CD|7.0.0|2026-06-16|
|DevOps Vulnerability Integrations|7.0.0|2026-06-16|
|DevOps Workspace|7.0.0|2026-06-16|
|DEX Application and Device Health|4.3.0|2026-06-16|
|DEX Content Playbook|4.3.0|2026-06-16|
|DEX Desktop Assistant|4.3.0|2026-06-16|
|DEX Desktop Assistant|4.3.0|2026-06-16|
|DEX Desktop Assistant|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Zoom|4.0.0|2026-03-12|
|DEX for Zoom|4.0.0|2026-03-12|
|DEX for Zoom|4.0.0|2026-03-12|
|DEX for Zoom|4.0.0|2026-03-12|
|DEX Self Service|4.3.0|2026-06-16|
|Diagram Builder|29.1.0|2026-03-12|
|Digital Experience Feedback Survey|4.3.0|2026-06-16|
|Digital Experience Score|4.3.0|2026-06-16|
|Digital Integration Management|1.6.1|2026-06-16|
|Digital Operational Resilience Management|21.1.1|2025-12-11|
|Digital Portfolio Management|7.4.1|2026-01-20|
|Digital Product Release|2.3.2|2025-12-11|
|Digital Product Release Data Model|2.4.0|2026-03-12|
|Digital Product Release Policy Content Pack|2.2.0|2025-07-31|
|Digital Product Release Workspace|2.3.0|2025-12-11|
|Digital Resilience Incident Reporting|21.1.1|2025-12-11|
|Digital Resilience Third-party Information Register|21.1.7|2025-12-11|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital signature component|27.1.0|2025-07-31|
|Discovery Admin Workspace|1.12.0|2025-12-11|
|Discovery and Service Mapping Patterns|1.29.0|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|DLP Incident Response integration with ICAP|1.1.1|2026-01-20|
|DLP Incident Response integration with Microsoft|1.3.1|2026-01-20|
|DLP Incident Response integration with Netskope|1.2.1|2026-01-20|
|DLP Incident Response integration with Proofpoint|1.1.0|2025-12-11|
|DLP Incident Response integration with Symantec|1.3.1|2026-01-20|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Docker Spoke|2.3.4|2025-07-10|
|Document Approval App Template|28.2.1|2025-12-11|
|Document display component|27.0.0|2025-05-01|
|Document Flow Wizards|2.0.2|2022-09-21|
|Document Intelligence|8.0.6|2026-06-16|
|Document Intelligence Admin|4.1.0|2025-12-11|
|Document Intelligence for Accounts Payable Operations Content Pack|2.0.0|2025-12-11|
|Document Service Framework for Google Drive|3.0.0|2025-07-31|
|Document Service Framework for OneDrive|3.0.0|2025-07-31|
|Document Template Integration with AdobeSign|1.7.0|2025-12-11|
|Document Template integration with DocuSign|1.7.1|2026-03-12|
|DocuSign Activities for PAD|1.1.3|2023-01-12|
|Docusign eSignature Spoke|4.2.2|2026-02-05|
|Dropbox Business Spoke|1.0.5|2024-03-07|
|Dun and Bradstreet DirectPlus Spoke|1.0.0|2025-01-30|
|Dynamic Guidance|28.3.2|2026-06-16|
|Dynamic Related Records for Configurable Workspace|25.7.0|2026-06-16|
|Elasticsearch Integration for Security Operations|10.3.4|2024-11-07|
|Email Interaction Core|1.0.3|2025-12-11|
|Email Interaction for CSM|1.5.0|2025-12-11|
|Emergency Alert App Template|28.2.1|2025-12-11|
|Emergency Exposure Management|1.27.0|2025-07-31|
|Emergency Outreach|1.34.0|2025-07-31|
|Emergency Self Report|1.21.0|2025-07-31|
|Employee Center for Microsoft Viva Connections|2.0.8|2025-07-31|
|Employee Center integration with Zoom|2.0.16|2025-12-11|
|Employee Center Pro|42.0.2|2026-06-16|
|Employee Center Pro Kiosk|2.3.4|2025-12-11|
|Employee Experience Foundation|30.0.3|2025-12-11|
|Employee experience taxonomy|28.2.5|2025-12-11|
|Employee Experience VA Components|1.0.0|2023-08-03|
|Employee Experience VA topics and topic blocks|1.1.2|2023-05-04|
|Employee Goals|1.3.0|2026-06-16|
|Employee Health Screening|1.28.0|2025-07-31|
|Employee Readiness Core|1.42.0|2025-12-11|
|Employee Readiness Surveys|1.5.3|2025-07-31|
|Employee Travel Safety|1.22.0|2025-12-11|
|Engagement dashboard for AI Control Tower|3.0.11|2025-12-12|
|Engagement Messenger|5.12.1|2026-01-20|
|Enterprise Architecture - Advanced|1.0.1|2026-06-16|
|Enterprise Architecture Cloud Assessment|1.0.1|2025-01-30|
|Enterprise Architecture - Prime|1.0.1|2026-06-16|
|Enterprise Architecture Workspace|9.1.1|2026-06-16|
|Enterprise Asset Management Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for DCNAM|1.0.0|2025-12-11|
|Enterprise Asset Management for DCNAM Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for Facilities|1.0.0|2024-08-01|
|Enterprise Asset Management for Healthcare|1.1.2|2026-03-12|
|Enterprise Asset Management for Healthcare Advanced|1.0.0|2026-04-09|
|Enterprise Asset Management for Providers|1.0.0|2025-12-11|
|Enterprise Modeling and Visualization|6.2.2|2026-06-16|
|Enterprise Modeling Common|3.8.0|2026-06-16|
|Enterprise Portfolio|1.3.0|2025-12-11|
|Enterprise Service Management Integrations Framework|3.8.2|2025-07-31|
|Entitlements Verification|6.0.0|2025-12-11|
|Equifax Spoke|1.0.0|2023-08-03|
|ER integration with NAVEX|1.1.1|2024-02-01|
|ERP Customization Mining|7.0.5|2025-05-01|
|ERP Integration Framework|19.0.3|2026-06-16|
|ESG integration with DEX|21.1.0|2025-12-11|
|ESG Risk Management|21.0.1|2025-12-11|
|Ethoca Spoke|3.0.1|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Management Connectors|2.19.4|2026-06-16|
|Event Management Core|23.16.0|2026-06-16|
|Event Registration App Template|28.2.1|2025-12-11|
|Exception Management for Unified Security Exposure Management|30.2.1|2026-01-20|
|Expanded Model and Asset Classes|2.16.1|2026-05-05|
|Expense Pre-Approval Template|28.2.1|2025-12-11|
|Export entities|3.3.1|2026-06-16|
|Export entities|3.3.1|2026-06-16|
|Export to PowerPoint|2.3.0|2025-12-11|
|Export to PowerPoint for Application Portfolio Management|1.0.1|2024-02-01|
|Export to PowerPoint for Strategic Portfolio Management|1.4.2|2025-12-11|
|External Agent Management Util Pack|1.2.0|2025-07-31|
|External Content Connectors|7.0.7|2026-05-28|
|External Content Connectors Admin|7.0.7|2026-05-28|
|External Content Connectors Adobe Acrobat Sign|7.0.7|2026-05-28|
|External Content Connectors Adobe AEM|7.0.7|2026-05-28|
|External Content Connectors Aha Roadmaps|7.0.7|2026-05-28|
|External Content Connectors Amazon S3|7.0.7|2026-05-28|
|External Content Connectors Application Suite|7.0.7|2026-05-28|
|External Content Connectors Asana|7.0.7|2026-05-28|
|External Content Connectors Box|7.0.7|2026-05-28|
|External Content Connectors Confluence Cloud|7.0.7|2026-05-28|
|External Content Connectors Cornerstone|7.0.7|2026-05-28|
|External Content Connectors Docusign|7.0.7|2026-05-28|
|External Content Connectors Dropbox|7.0.7|2026-05-28|
|External Content Connectors FluidTopics|7.0.7|2026-05-28|
|External Content Connectors GitHub Enterprise Cloud|7.0.7|2026-05-28|
|External Content Connectors Gitlab|7.0.7|2026-05-28|
|External Content Connectors Google Drive|7.0.7|2026-05-28|
|External Content Connectors Hubspot|7.0.7|2026-05-28|
|External Content Connectors Jira Cloud|7.0.7|2026-05-28|
|External Content Connectors Lucid|7.0.7|2026-05-28|
|External Content Connectors Microsoft OneDrive|7.0.7|2026-05-28|
|External Content Connectors Microsoft Teams|7.0.7|2026-05-28|
|External Content Connectors Miro|7.0.7|2026-05-28|
|External Content Connectors Monday.com|7.0.7|2026-05-28|
|External Content Connectors Notion|7.0.7|2026-05-28|
|External Content Connectors SAP Document Management System|7.0.7|2026-05-28|
|External Content Connectors ServiceNow Instance|7.0.7|2026-05-28|
|External Content Connectors Sharepoint Online|7.0.7|2026-05-28|
|External Content Connectors Slack|7.0.7|2026-05-28|
|External Content Connectors Smartsheet|7.0.7|2026-05-28|
|External Content Connectors SN Docs|7.0.7|2026-05-28|
|External Content Connectors Trello|7.0.7|2026-05-28|
|External Content Connectors Viva Engage|7.0.7|2026-05-28|
|External Content Connectors Web Crawler|7.0.5|2026-04-09|
|External Content Connectors Wordpress|7.0.7|2026-05-28|
|External Content Connectors Workday|7.0.7|2026-05-28|
|External Content Connectors Workvivo|7.0.7|2026-05-28|
|External Content Connectors Zendesk|7.0.7|2026-05-28|
|External Content Connectors Zoom|7.0.7|2026-05-28|
|External Credential Storage and Management Application|1.3.1|2025-12-11|
|External Legal Service Center|1.2.0|2025-12-11|
|External Trigger Builder|1.1.0|2026-03-12|
|F5 BIG-IP Spoke|1.3.0|2025-09-10|
|Fallout management|7.8.0|2026-06-16|
|Fallout management|7.8.0|2026-06-16|
|FDIH Dashboard|25.0.5|2024-11-07|
|Field Service Advanced Capacity and Reservations Management|30.0.3|2026-03-12|
|Field Service Capacity and Reservations Management|30.0.3|2026-03-12|
|Field Service Contractor for mobile|4.8.3|2026-03-12|
|Field Service Contractor Management|30.0.2|2026-03-12|
|Field Service Management AI agent collection|3.0.1|2026-06-16|
|Field Service Management for Telecommunications|3.0.2|2025-12-11|
|Field Service Management Intelligent Task Recommendations|29.0.6|2026-03-12|
|Field Service Management Scheduling Automations|29.0.6|2026-03-12|
|Field Service Management Virtual Conferencing Integration|30.0.0|2026-03-12|
|Field Service Manager Mobile|1.1.0|2026-04-09|
|Field Service Manager Workforce|1.1.0|2026-04-09|
|Field Service Marketplace|30.0.1|2026-03-12|
|Field Service Mobile|29.1.5|2026-04-09|
|Field Service NLU Model for Virtual Agent Conversations|1.3.0|2025-07-31|
|Field Service Quality Management|29.1.1|2026-03-12|
|Field Service Territory Planning|30.0.3|2026-03-12|
|Field Service Virtual Agent Conversations|1.7.0|2025-07-31|
|Field Service with Service Locations support|30.0.3|2026-03-12|
|File Explorer Component for Security Operations|1.2.13|2025-08-22|
|File Explorer for Security Incident Response|1.3.0|2025-12-11|
|Finance Case Management|1.5.1|2026-06-16|
|Finance Common Architecture|12.0.1|2026-06-16|
|Finance Operations Workspace|1.5.1|2026-06-16|
|Financials Core|6.2.0|2026-06-16|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Firewall Audits and Reporting|1.8.0|2025-12-11|
|First Advantage Spoke|1.8.0|2025-11-06|
|Flow Designer - Designer|29.1.0|2026-04-09|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Diagramming|29.0.1|2026-03-12|
|Flow Execution Analysis|29.2.8|2026-06-16|
|Flow Generation|29.1.2|2026-04-09|
|Flow Summarization|29.1.2|2026-04-09|
|Flow Template Builder|1.0.9|2023-05-04|
|Flow Templates for Access Management|1.0.4|2023-04-06|
|Flow Templates for Cloud Services|1.2.3|2023-01-12|
|Flow Templates for CRM|1.0.3|2023-04-06|
|Flow Templates for DevOps|1.1.3|2023-04-06|
|Flow Templates for Document Management|1.1.10|2023-04-06|
|Flow Templates for HR Management|1.4.4|2023-04-06|
|Flow Templates for IntegrationHub Enterprise|1.0.2|2023-04-06|
|Flow Templates for Notifications|1.2.4|2024-06-06|
|Flow Templates for Service Desk|1.0.3|2023-04-06|
|Forecast planning analysis|21.1.0|2025-12-11|
|Formula Builder|29.1.1|2026-03-12|
|Formula builder connected|22.3.1|2026-06-16|
|Fortify Application Vulnerability Integration|2.7.1|2025-09-10|
|FRISS Spoke|1.1.1|2026-03-12|
|FSC Common - Foundation|1.2.0|2026-06-16|
|FSC Common - Prime|1.2.0|2026-06-16|
|FSM - Advanced|2.0.1|2026-06-16|
|FSM Configurable Dispatcher Workspace|29.0.11|2026-03-12|
|FSM Configurable Workspace|29.0.4|2026-03-12|
|FSM - Foundation|2.0.1|2026-06-16|
|FSM Scheduling AI Agent Collection|1.0.7|2026-06-16|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Gantt UI Builder Component|26.1.1|2026-06-16|
|GC Dashboard|2.0.5|2025-12-11|
|Geo Map component|1.2.0|2025-07-31|
|Gifts and Entertainment Compliance|1.3.0|2025-12-11|
|Github Application Vulnerability Integration|2.3.1|2025-12-11|
|GitHub Spoke|3.5.1|2026-01-20|
|GitLab Spoke|2.4.0|2025-11-06|
|Gmail Spoke|1.3.3|2025-12-11|
|Goal Framework|4.12.1|2026-04-09|
|Goal Framework for SPM|2.7.0|2026-03-12|
|Google Calendar Spoke|2.6.0|2025-09-10|
|Google Chat Spoke|1.2.0|2025-09-10|
|Google Cloud Datastore Spoke|1.0.3|2023-09-07|
|Google Cloud DNS Spoke|1.0.2|2022-09-01|
|Google Cloud Functions Spoke|1.0.3|2025-06-05|
|Google Cloud Load Balancer Spoke|1.0.2|2023-09-07|
|Google Cloud Pub Sub Spoke|1.0.4|2024-09-10|
|Google Cloud SQL Spoke|1.0.2|2023-09-07|
|Google Cloud Storage Spoke|1.1.1|2025-12-11|
|Google Cloud Translator Service Spoke|3.2.6|2025-05-01|
|Google Cloud Virtual Network Spoke|1.0.5|2023-09-07|
|Google Cloud VPC Access Spoke|1.0.1|2022-09-01|
|Google Compute Engine Spoke|1.0.5|2024-09-10|
|Google Directory Spoke|1.5.2|2024-10-03|
|Google Docs Spoke|1.3.0|2025-09-10|
|Google Drive Spoke|2.3.0|2025-09-10|
|Google Gemini Spoke|1.6.0|2026-03-12|
|Google Identity And Access Spoke|1.1.1|2022-09-01|
|Google Meet Spoke|1.2.1|2025-11-06|
|Google Persistent Disk Spoke|1.0.2|2022-09-01|
|Google Sheets Spoke|1.0.7|2023-09-20|
|Google Tasks Spoke|1.4.0|2025-09-10|
|GoTo Spoke|2.0.1|2021-08-19|
|GovNotify Spoke|1.2.0|2025-09-10|
|GRC: Advanced Audit|21.1.2|2025-12-11|
|GRC: Advanced Core|22.0.1|2026-03-12|
|GRC: Advanced Dashboards|21.1.1|2025-12-11|
|GRC: Advanced Risk|22.3.2|2026-06-16|
|GRC: Advanced Risk Assessment|22.3.2|2026-06-16|
|GRC: Approver Configurator|22.3.0|2026-06-16|
|GRC: Audit Management|22.0.1|2026-03-12|
|GRC: Audit Management Workspace|22.0.1|2026-03-12|
|GRC: Business Continuity Management - Core|11.0.1|2026-06-16|
|GRC: Business Continuity Management User - Lite|5.0.1|2023-08-03|
|GRC: Business Continuity Planning|11.0.2|2026-06-16|
|GRC: Business Impact Analysis|11.0.2|2026-06-16|
|GRC: Business User - Lite|18.0.0|2024-02-01|
|GRC: Common Dashboard Elements|18.1.4|2024-06-06|
|GRC: Common Workspace Elements|22.3.6|2026-06-16|
|GRC: Compliance Assessment|22.3.2|2026-06-16|
|GRC: Compliance Case Management|21.1.0|2025-12-11|
|GRC: Compliance Management Workspace|21.1.3|2025-12-11|
|GRC: Compliance UCF|21.1.0|2025-12-11|
|GRC: Composite Entity|21.1.1|2025-12-11|
|GRC: Continuous Authorization and Monitoring|21.1.1|2025-12-11|
|GRC: Continuous Authorization and Monitoring Advanced|21.1.1|2025-12-11|
|GRC: Continuous Authorization and Monitoring Workspace|21.1.1|2025-12-11|
|GRC: Crisis Management|11.0.2|2026-06-16|
|GRC: Crisis Management integration with Everbridge Notifications|9.1.1|2025-12-11|
|GRC: Crisis Map|11.0.1|2026-06-16|
|GRC: Cyber Risk Institute \(CRI\) Profile Accelerator|21.1.0|2025-12-11|
|GRC: Cybersecurity Controls Accelerator|18.1.0|2024-06-06|
|GRC: Entity Based Access|21.1.4|2025-12-11|
|GRC: Financial Services Controls Accelerator|22.0.1|2026-03-12|
|GRC: integrations with third-party content|18.1.0|2024-06-06|
|GRC: Management Reporting|18.1.0|2024-06-06|
|GRC: Metrics|22.3.1|2026-06-16|
|GRC: Mobile|18.0.0|2024-02-01|
|GRC: Model Risk Management|21.1.3|2025-12-11|
|GRC: NIST CSF Use Case Accelerator|21.1.0|2025-12-11|
|GRC: Operational Resilience|21.1.3|2025-12-11|
|GRC: Performance Analytics Premium Integration|19.1.0|2024-11-07|
|GRC: Policy and Compliance integrator|21.1.0|2025-12-11|
|GRC: Policy and Compliance Management|22.3.2|2026-06-16|
|GRC: Predictive Intelligence|21.1.0|2025-12-11|
|GRC: Privacy Case Management|21.1.0|2025-12-11|
|GRC: Privacy Lite User|19.0.0|2024-08-01|
|GRC: Privacy Management|21.1.4|2025-12-11|
|GRC: Profiles|22.3.3|2026-06-16|
|GRC: Regulatory Change Management|21.1.1|2025-12-11|
|GRC: Regulatory Change Management integration with RSS Feeds|21.1.0|2025-12-11|
|GRC: Risk Heatmap|22.3.2|2026-06-16|
|GRC: Risk Management|22.3.3|2026-06-16|
|GRC: Risk Management Workspace|21.1.1|2025-12-11|
|GRC: Risk Shared Common Components|22.3.2|2026-06-16|
|GRC: SIG Questionnaire Integration|21.1.0|2025-12-11|
|GRC: SOX Content Pack|21.1.0|2025-12-11|
|GRC: taxonomy management|22.3.0|2026-06-16|
|GRC: Technology Controls Monitoring Accelerator|21.1.0|2025-12-11|
|GRC: Vendor Portal|22.3.2|2026-06-16|
|GRC: Vendor Risk Management Workspace|22.3.2|2026-06-16|
|GRC: Virtual Agent|19.1.0|2024-11-07|
|GRC: Workbench|21.1.0|2025-12-11|
|GRC Case Management Core|22.3.3|2026-06-16|
|GRC Compliance Case Management Advanced|18.1.1|2024-06-06|
|GRC Compliance Case Management Full Access|18.1.1|2024-06-06|
|GRC Employee User|19.0.1|2024-08-01|
|GRC Feature roles|22.3.0|2026-06-16|
|GRC integration with Thomson Reuters Regulatory Intelligence|21.1.0|2025-12-11|
|GRC Personal Data Rights|21.1.3|2025-12-11|
|GRC Privacy Case Management Integration with RadarFirst|21.1.0|2025-12-11|
|Group Life Servicing|2.5.0|2026-03-12|
|Group Life Servicing|2.5.0|2026-03-12|
|Group Life Servicing|2.5.0|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|Guest Walk-up Experience for Customer Service|2.0.1|2026-03-12|
|Guidance|43.0.0|2026-06-16|
|Guided Decisions|38.0.2|2025-12-11|
|Guided Decisions|38.0.2|2025-12-11|
|Guided Decisions|38.0.2|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Guided Self-Service in Employee Center|3.2.2|2025-12-11|
|Guided Setup|6.0.2|2026-03-12|
|Guidewire Spoke|1.3.0|2026-03-12|
|Hardware Asset Management|15.0.2|2026-06-16|
|Hardware Asset Management for DaaS|12.1.1|2026-03-12|
|Hardware Asset Management for TNI|13.0.0|2025-11-06|
|Hardware Asset Management for Zero Touch Mobility|12.0.0|2025-01-30|
|HCLS - Advanced|2.0.1|2026-05-05|
|HCLS - Foundation|2.0.1|2026-05-05|
|HCLS - Foundation|2.0.1|2026-05-05|
|HCLS - Prime|2.0.1|2026-05-05|
|HCLS - Prime|2.0.1|2026-05-05|
|Header App Shell|23.0.0|2023-06-01|
|Health and Safety Incident Management OSHA Content Pack|11.0.0|2025-12-11|
|Health and Safety Incident Management OSHA Content Pack|11.0.0|2025-12-11|
|Health and Safety Testing|1.27.0|2025-07-31|
|Healthcare and Life Sciences Service Management Core|11.3.0|2026-03-12|
|Healthcare and Life Sciences Service Management Core|11.3.0|2026-03-12|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Operations Core|2.3.0|2026-03-12|
|Healthcare Operations Core|2.3.0|2026-03-12|
|Healthcare Professional Data Model|1.3.0|2025-12-11|
|Health dashboard for AI Control Tower|3.0.11|2025-12-12|
|Health Log Analytics|38.0.17|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Homepage deprecation help tool|2.0.2|2024-11-07|
|HR Flow Wizards|1.1.0|2022-05-05|
|HR License meter|1.1.6|2026-06-16|
|HR Multi Instance Integration Base|2.0.0|2025-07-31|
|HR Multi Instance Integration for Consumer|2.0.0|2025-07-31|
|HR Multi Instance Integration for Provider|2.0.0|2025-07-31|
|HRSD Process Mining Content Pack|6.0.3|2026-03-12|
|HR Service Delivery Advanced Integration with Oracle HCM|1.3.0|2025-12-11|
|HR Service Delivery Advanced Integration with Workday|2.2.6|2025-12-11|
|HR Service Delivery for Healthcare|1.0.4|2025-05-01|
|HR Service Delivery for Microsoft 365|3.8.0|2025-12-11|
|HR Service Delivery for mobile|21.2.9|2025-12-11|
|HR Service Delivery Integration with Cornerstone OnDemand|1.2.0|2025-12-11|
|HR Service Delivery integration with Oracle HCM|1.0.10|2024-11-07|
|HR Service Delivery Integration with Ultimate Kronos Group|2.0.6|2024-06-06|
|HR Service Delivery Integration with Workday|3.4.11|2025-12-11|
|HR Service Delivery NLU Model for Virtual Agent Conversations|22.2.0|2023-11-02|
|HR Service Delivery Portal UI Components|1.0.5|2024-05-09|
|HR Service Delivery Virtual Agent Conversations|24.2.8|2025-05-01|
|HR Success Dashboard indicators|1.0.15|2025-05-01|
|HR taxonomy|1.2.1|2022-12-01|
|HR Voice AI Agents|2.3.6|2026-06-16|
|HR Voice AI Agents|2.3.6|2026-06-16|
|Human Resources Service Delivery Integration with Workday Learning|1.4.0|2025-07-31|
|IBM License Compliance for Software Asset Management|6.0.7|2026-03-12|
|IBM QRadar Integration for Security Operations|10.3.7|2024-11-07|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|ICW Core|1.0.4|2026-05-05|
|ICW - Foundation|1.0.3|2026-05-05|
|Idea Manager Dashboard|2.2.0|2025-12-11|
|iManage Spoke|1.1.6|2026-01-20|
|Impact|8.0.10|2026-06-16|
|Impact Common|8.0.7|2026-06-16|
|Impact Content|8.0.5|2026-06-16|
|Impact Health Content|3.0.3|2026-06-16|
|Impact Value Management - APM|2.1.0|2025-01-30|
|Impact Value Management - APM|2.1.0|2025-01-30|
|Impact Value Management - APM|2.1.0|2025-01-30|
|Impact Value Management - APM|2.1.0|2025-01-30|
|Impact Value Management - App Engine|2.1.0|2025-01-30|
|Impact Value Management - App Engine|2.1.0|2025-01-30|
|Impact Value Management - App Engine|2.1.0|2025-01-30|
|Impact Value Management - App Engine|2.1.0|2025-01-30|
|Impact Value Management - CSM|2.1.0|2025-01-30|
|Impact Value Management - CSM|2.1.0|2025-01-30|
|Impact Value Management - CSM|2.1.0|2025-01-30|
|Impact Value Management - CSM|2.1.0|2025-01-30|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HR|4.0.0|2026-06-16|
|Impact Value Management - IRM|3.0.3|2025-12-11|
|Impact Value Management - IRM|3.0.3|2025-12-11|
|Impact Value Management - ITOM|3.0.1|2025-12-11|
|Impact Value Management - ITOM|3.0.1|2025-12-11|
|Impact Value Management - ITSM|3.0.1|2025-12-11|
|Impact Value Management - ITSM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SECOPS|3.0.3|2025-12-11|
|Impact Value Management - SECOPS|3.0.3|2025-12-11|
|Impact Value Management - SPM|3.0.1|2025-12-11|
|Impact Value Management - SPM|3.0.1|2025-12-11|
|Inbound API Integration Usage|1.1.9|2026-03-12|
|Incident Communications Management for Service Operations Workspace|9.2.0|2026-06-16|
|Incident Management for Field Service|1.1.1|2025-01-02|
|Incident Management for Service Operations Workspace|9.2.0|2026-06-16|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Servicing|2.5.0|2026-03-12|
|Individual Life Servicing|2.5.0|2026-03-12|
|Individual Life Servicing|2.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Indoor Mapping|1.16.8|2026-06-16|
|Indoor Mapping Component|1.6.1|2026-06-16|
|Indoor Mapping for Assets|1.0.2|2025-10-16|
|Indoor Mapping Service|1.0.8|2025-12-11|
|Industrial Control Tower Advanced|1.0.0|2026-06-16|
|Industrial Control Tower Foundation|1.0.0|2026-06-16|
|Industrial Control Tower Prime|1.0.0|2026-06-16|
|Industrial Core|4.0.0|2026-06-16|
|Industrial Core|4.0.0|2026-06-16|
|Industrial Cyber Security Suite Advanced|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Advanced|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Foundation|1.0.1|2026-04-09|
|Industrial Cyber Security Suite Foundation|1.0.1|2026-04-09|
|Industrial Operations Suite Advanced|1.0.1|2026-04-09|
|Industrial Operations Suite Advanced|1.0.1|2026-04-09|
|Industrial Operations Suite Foundation|1.0.1|2026-04-09|
|Industrial Operations Suite Foundation|1.0.1|2026-04-09|
|Industrial Operations Suite Prime|1.0.1|2026-04-09|
|Industrial Operations Suite Prime|1.0.1|2026-04-09|
|Industrial Process Manager|3.1.0|2026-03-12|
|Industrial Process Manager|3.1.0|2026-03-12|
|Industrial Workspace Common|4.1.0|2026-06-16|
|Industry Core|1.0.9|2022-12-01|
|Infoblox Spoke|2.0.4|2024-03-20|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Insurance claims|1.2.2|2026-03-12|
|Insurance claims|1.2.2|2026-03-12|
|Insurance claims|1.2.2|2026-03-12|
|Insurance Claims Core|3.5.0|2026-06-16|
|Insurance Claims Core|3.5.0|2026-06-16|
|Insurance Claims Core|3.5.0|2026-06-16|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Integrated Risk Management Enterprise|22.3.0|2026-06-16|
|Integrated Risk Management Professional|22.3.0|2026-06-16|
|Integrated Risk Management Standard|22.1.1|2026-04-09|
|Integration Commons for CMDB|2.25.0|2026-06-16|
|IntegrationHub Enterprise Flow Wizards|1.0.0|2021-08-19|
|IntegrationHub ETL|3.3.6|2025-12-11|
|Integration Hub Usage Dashboards|3.0.0|2025-07-31|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Intelligent Task Recommendations|29.0.7|2026-03-12|
|Intent Discovery|3.3.8|2026-05-05|
|Interaction Management for Service Operations Workspace|9.2.0|2026-06-16|
|Interceptor UI for Service Operations Workspace|9.2.0|2026-06-16|
|Inventory Number Management|5.0.0|2025-07-31|
|Inventory Number Management|5.0.0|2025-07-31|
|Inventory Number Management|5.0.0|2025-07-31|
|Inventory Tracker App Template|28.2.1|2025-12-11|
|Investigation Framework|9.2.0|2026-06-16|
|Investment Funding|1.1.1|2024-05-09|
|Invicti Application Vulnerability Integration|1.2.1|2024-11-07|
|Invoice Case Management|13.0.1|2026-06-16|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|Invoice Self-Service|1.0.0|2026-03-12|
|Invoice Self-Service|1.0.0|2026-03-12|
|Invoice Self-Service|1.0.0|2026-03-12|
|Invoice Self-Service|1.0.0|2026-03-12|
|Invoice Self-Service|1.0.0|2026-03-12|
|Invoice Self-Service|1.0.0|2026-03-12|
|ISA Equipment Model|4.0.0|2026-06-16|
|ISA Equipment Model|4.0.0|2026-06-16|
|ISA Equipment Model|4.0.0|2026-06-16|
|Issue Auto Resolution for HR|4.0.3|2024-06-06|
|ITAM Common for DaaS|11.2.1|2026-03-12|
|ITAM common hub|1.1.0|2025-12-11|
|ITAM Health Check application|3.0.5|2026-03-12|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|ITOM AIOPS Config Center|27.3.5|2026-06-16|
|ITOM Cloud Services Core|4.1.15|2026-06-16|
|ITOM Configuration Console|28.1.1|2026-06-16|
|ITOM Guided Setup - New|27.3.1|2026-06-16|
|ITOM Line chart|27.1.1|2026-03-12|
|ITOM Mobile Agent|1.0.0|2025-05-01|
|ITOM Telemetry Ingest|1.0.0|2025-12-11|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|IT Service Management for Microsoft 365|2.11.1|2025-12-11|
|ITSM Admin Experience Components|2.1.0|2026-05-05|
|ITSM Enterprise UI Components|3.5.0|2025-12-11|
|ITSM Mobile Agent|10.2.0|2025-12-11|
|ITSM NLU Model for Virtual Agent Conversations|8.2.0|2025-05-01|
|ITSM Process Mining Content Pack|2.0.0|2026-03-12|
|ITSM Virtual Agent Conversations|9.3.2|2026-03-12|
|Jack Henry jXchange Spoke|2.1.0|2025-07-31|
|Jamf Spoke|1.2.1|2025-12-11|
|Jenkins Spoke|2.3.0|2025-09-10|
|Jenkins v2 Spoke|1.2.0|2023-02-02|
|Jira Service Management Spoke|1.2.0|2025-10-16|
|Jira Spoke|6.0.1|2026-04-09|
|Journey Accelerator|6.10.0|2026-06-16|
|Kanban board component|26.0.1|2026-02-05|
|Kanban Components|1.2.0|2026-03-12|
|KnowBe4 Integration for SecOps|2.3.3|2024-12-05|
|Knowledge API|29.0.1|2026-03-12|
|KPI Composer|4.3.1|2025-12-11|
|KPI Framework|6.1.0|2026-06-16|
|Kubernetes Spoke|1.3.0|2025-09-10|
|Kubernetes Visibility Agent|3.13.0|2025-12-11|
|Leader Hub|1.5.0|2026-03-12|
|Lead Management Application|5.0.0|2025-12-11|
|Lead Management Data Model|5.0.1|2025-12-11|
|Lead to Cash Core|1.9.0|2026-06-16|
|Lead-to-Cash Process Management|2.2.2|2025-12-11|
|Learning|5.7.0|2026-06-16|
|Learning Core|9.10.0|2026-06-16|
|Legal and Contracts Common Utilities|1.1.1|2026-06-16|
|Legal Conflict of Interest|4.7.0|2025-12-11|
|Legal Content Review|1.3.0|2025-12-11|
|Legal Hold Notification|1.1.0|2025-12-11|
|Legal Mobile|5.6.0|2025-12-11|
|Legal Practice Apps Core|1.0.2|2023-02-02|
|Legal Service Delivery - Prime|1.0.9|2026-06-16|
|Legal Simple Compliance|1.1.0|2025-12-11|
|Legal Simple Intellectual Property|1.6.0|2025-12-11|
|Legal Simple Privacy|1.2.5|2025-12-11|
|Legal Stock Preclearance|4.9.0|2025-12-11|
|Legal Tracker Spoke|1.0.4|2025-01-30|
|Legal Virtual Agent Conversations|1.3.2|2023-05-04|
|Licensing Engine|6.4.3|2026-06-16|
|List AI Experience|3.0.0|2026-06-16|
|Live CI View|19.1.2|2023-05-04|
|Localization Workspace|1.0.6|2025-05-01|
|Log Export Service|3.2.0|2025-05-01|
|Looker Spoke|1.0.2|2025-01-30|
|Lucidchart Diagramming Spoke|1.1.1|2024-01-04|
|Lucidchart Integration|2.4.1|2025-01-30|
|Magnit Spoke|1.2.1|2023-09-07|
|Major Incident Management for Service Operations Workspace|9.2.0|2026-06-16|
|Major Security Incident Management|3.5.1|2026-01-20|
|Manage Order Operations|2.0.3|2026-06-16|
|Manager Hub|4.9.1|2026-06-16|
|Manage Skills Configurable Page|1.1.12|2025-01-30|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Map Integrations for Field Service|29.0.8|2026-03-12|
|Marketplace Core|30.0.1|2026-03-12|
|Mastercard Spoke|4.0.1|2025-12-11|
|Matrix report|21.0.1|2025-07-31|
|McAfee ePO Integration for Security Operations|10.6.0|2025-12-11|
|MCP for Strategic Portfolio Management|1.0.2|2026-06-16|
|Meeting CAB|9.2.0|2026-06-16|
|Meeting Extensions for Microsoft Teams|1.8.0|2025-12-11|
|Meeting Watcher - UI Builder Data Resource|9.2.0|2026-06-16|
|Mentoring|2.3.0|2026-06-16|
|Metric data table|22.0.0|2026-03-12|
|Metric Intelligence|2.7.11|2025-12-11|
|Metric Rules|1.1.4|2024-06-06|
|Metrics and CI Actions Framework|9.2.0|2026-06-16|
|Microsoft 365 for ServiceNow Reporting|22.3.1|2026-06-16|
|Microsoft Active Directory v2 Spoke|2.5.1|2025-10-16|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure Application Insights Spoke|2.0.0|2024-11-07|
|Microsoft Azure Artifacts Spoke|1.1.0|2024-11-07|
|Microsoft Azure Automation Spoke|2.0.0|2024-11-07|
|Microsoft Azure Blob Storage Spoke|2.0.0|2024-11-07|
|Microsoft Azure Cosmos DB Spoke|2.0.0|2024-11-07|
|Microsoft Azure DevOps Boards Spoke|3.1.0|2025-09-10|
|Microsoft Azure DevOps Integration for Agile Development|1.7.0|2025-12-11|
|Microsoft Azure DevOps Integrations Common|1.9.0|2025-12-11|
|Microsoft Azure DevOps Pipelines Spoke|1.0.0|2023-08-03|
|Microsoft Azure Managed Storage Spoke|2.0.1|2024-11-07|
|Microsoft Azure Notification Hub Spoke|2.0.0|2024-11-07|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure RBAC Spoke|1.0.2|2025-09-10|
|Microsoft Azure Resource Management Spoke|2.0.0|2024-11-07|
|Microsoft Azure Sentinel Incident Ingestion Integration For Security Operations|11.2.3|2026-05-05|
|Microsoft Azure SQL Database Spoke|2.0.0|2024-11-07|
|Microsoft Azure Traffic Manager Spoke|2.0.0|2024-11-07|
|Microsoft Azure Virtual Machine Spoke|2.0.0|2024-11-07|
|Microsoft Azure Virtual Network Spoke|2.0.0|2024-11-07|
|Microsoft Defender for Cloud Integration for Security Operations|2.8.0|2025-12-11|
|Microsoft Defender for Office365 Integration for SecOps|2.3.4|2024-12-05|
|Microsoft Dynamics 365 for Finance and Operations Spoke|2.4.3|2026-01-20|
|Microsoft Dynamics 365 Spoke|1.1.0|2025-07-31|
|Microsoft Dynamics CRM Spoke|1.9.0|2025-11-06|
|Microsoft Endpoint Configuration Manager for Investigation|9.2.0|2026-06-16|
|Microsoft Endpoint Configuration Manager Spoke|1.8.1|2025-06-05|
|Microsoft Entra ID Integration for Password Reset|3.0.3|2025-01-30|
|Microsoft Entra ID Spoke|4.7.3|2025-12-11|
|Microsoft Exchange Online for Security Operations|10.7.2|2026-01-20|
|Microsoft Exchange Online Spoke|3.13.0|2026-03-12|
|Microsoft Exchange Server Spoke|2.5.1|2025-11-06|
|Microsoft Integrations - Core|5.8.1|2025-12-11|
|Microsoft Intune Spoke|1.2.0|2025-11-06|
|Microsoft Office add-in|22.3.0|2026-06-16|
|Microsoft OneDrive Spoke|2.8.1|2025-11-06|
|Microsoft Outlook Add-In for Legal Service Delivery|1.5.0|2025-12-11|
|Microsoft Security Response Center Spoke|1.3.0|2025-09-10|
|Microsoft SharePoint File Explorer Connector for Security Incident Response integration|1.3.0|2025-12-11|
|Microsoft SharePoint Online Spoke|2.10.0|2025-09-10|
|Microsoft Teams Chat Connector for Security Incident Management|1.2.30|2025-10-16|
|Microsoft Teams Communications Spoke|1.5.0|2025-12-11|
|Microsoft Teams Graph Spoke|4.4.1|2026-02-05|
|Microsoft Word Add-in for ServiceNow Contracts|1.8.0|2026-06-16|
|MID Guardian|1.0.4|2025-12-11|
|MIF Customer Instance|4.0.4|2026-03-12|
|Migration Utility for Service Operations Workspace|2.3.1|2025-05-01|
|Milestones|2.9.0|2026-06-16|
|Miro Spoke|3.3.1|2025-12-11|
|MISP integration for Security Operations|1.4.4|2026-02-05|
|Mitigation Controls Monitoring|4.1.4|2025-12-11|
|Mobile App Builder|27.11.0|2025-07-31|
|Mobile App Builder API|27.11.0|2025-07-31|
|Mobile Card Builder|26.12.0|2025-07-31|
|Mobile Publishing|24.0.0|2025-12-11|
|Mobile SDK|2.2.0|2025-03-12|
|Mobile Time Sheets|2.3.0|2025-12-11|
|Model Context Protocol Client|2.2.0|2026-06-16|
|monday.com Spoke|1.1.5|2025-06-05|
|MSIM VTB Task Card|1.0.|2024-02-01|
|MS Teams Activities for PAD|1.0.3|2023-01-12|
|Multi-case creation framework|2.1.0|2025-07-31|
|Natural Language Understanding Models for Sourcing and Procurement Operations|2.0.5|2023-05-04|
|Navex EthicsPoint Spoke|1.0.3|2025-12-11|
|News Integration for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|News Integration for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|News Integration for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|News Integration for Supplier Lifecycle Operations|4.0.0|2025-12-11|
|NLU Workbench - Advanced Features|7.0.22|2025-07-10|
|Node map Experience Component|27.3.0|2025-12-11|
|Notification Flow Wizards|2.0.1|2022-09-21|
|Notifications for Employee Center|2.0.9|2025-12-11|
|Notify Connector for Microsoft Teams|2.10.0|2025-12-11|
|Notify UI Components for Configurable Workspaces|9.2.0|2026-06-16|
|Notify Webex Connector|1.4.0|2025-12-11|
|Notify Zoom Connector|1.9.0|2025-07-31|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|31.0.5|2026-06-16|
|Now Assist for Accounts Payable Operations \(APO\)|8.0.0|2026-06-16|
|Now Assist for Advanced Work Assignment \(AWA\)|1.0.3|2026-06-16|
|Now Assist for App Engine|29.2.3|2026-06-16|
|Now Assist for Care Team Operations|2.0.1|2026-05-05|
|Now Assist for code generation|28.5.23|2026-06-16|
|Now Assist for Digital End-user Experience \(DEX\)|4.3.0|2026-06-16|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.3.2|2026-06-16|
|Now Assist for Enterprise Asset Management|1.0.1|2026-04-09|
|Now Assist for Error Framework|1.0.3|2026-06-16|
|Now Assist for Field Service Management \(FSM\)|10.0.1|2026-06-16|
|Now Assist for FSC Common|7.0.0|2026-06-16|
|Now Assist for Health and Safety|1.4.1|2026-06-16|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for ICW|1.0.0|2026-05-05|
|Now Assist for Impact|4.0.5|2026-06-16|
|Now Assist for Integration Hub|2.2.1|2025-11-06|
|Now Assist for Legal Service Delivery|1.8.1|2026-06-16|
|Now Assist for Operational Sustainability|22.3.2|2026-06-16|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.2.2|2026-06-16|
|Now Assist for Purchase Order Management \(POM\)|1.2.0|2026-06-16|
|Now Assist for RPA Hub|5.0.2|2025-12-11|
|Now Assist for RSM|1.4.0|2026-04-09|
|Now Assist for Security Incident Response integrations|1.2.1|2026-06-16|
|Now Assist for Service Graph Connectors|1.1.0|2025-01-30|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|10.0.0|2026-06-16|
|Now Assist for Spoke Generation|1.6.1|2026-06-16|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|8.0.0|2026-06-16|
|Now Assist for Telecommunications|2.0.1|2026-06-16|
|Now Assist for Telecommunications|2.0.1|2026-06-16|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.7|2026-06-16|
|Now Assist for Vault|2.1.1|2026-06-16|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.13|2026-06-16|
|Now Assist for Zero Copy Connector|2.0.0|2026-05-05|
|Now Assist in Conversational Spokes|1.0.0|2024-11-07|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Platform Skills|3.0.3|2026-06-16|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|Now Learning Integration|1.0.3|2024-02-01|
|Now Mobile|30.1.2|2026-03-12|
|Now Mobile|30.1.2|2026-03-12|
|now-visualization-extensions|29.0.8|2026-04-09|
|Obligation Management|1.7.0|2026-06-16|
|Observability Commons for CMDB|1.1.0|2023-11-02|
|Okta Spoke|4.7.1|2025-11-06|
|Omnichannel Callback|2.0.7|2026-03-12|
|Omnichannel Callback for Customer Service Management|1.5.1|2025-12-11|
|Omni-Experience Standard Feature Set|8.1.6|2026-04-09|
|On Call Scheduling for Service Operations Workspace|9.2.0|2026-06-16|
|On-Call UI Components for Configurable Workspaces|9.2.0|2026-06-16|
|OneLogin Spoke|1.0.2|2023-09-07|
|One-time Password Generator|1.1.0|2025-12-11|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management|22.3.1|2026-06-16|
|Operational Sustainability Management Advanced|22.3.1|2026-06-16|
|Operational Technology Change Management|3.1.0|2026-03-12|
|Operational Technology Change Management|3.1.0|2026-03-12|
|Operational Technology Hardware Vulnerability Assessment|3.1.0|2026-03-12|
|Operational Technology Hardware Vulnerability Assessment|3.1.0|2026-03-12|
|Operational Technology Health|3.1.0|2026-03-12|
|Operational Technology Health|3.1.0|2026-03-12|
|Operational Technology Incident Management|3.1.0|2026-03-12|
|Operational Technology Incident Management|3.1.0|2026-03-12|
|Operational Technology Manager|4.0.0|2026-06-16|
|Operational Technology Manager|4.0.0|2026-06-16|
|Operational Technology Manager|4.0.0|2026-06-16|
|Operational Technology Vulnerability Response|30.0.3|2026-03-12|
|Opportunity Management for Business Locations|2.0.0|2026-03-12|
|Opportunity Marketplace|2.7.0|2026-06-16|
|Oracle Autonomous DB Spoke|1.0.6|2022-12-01|
|Oracle Block Storage Spoke|1.0.4|2022-12-01|
|Oracle Boot Volume Spoke|1.0.6|2022-12-01|
|Oracle Cloud IAM Spoke|1.1.3|2022-09-21|
|Oracle Compute Engine Spoke|1.0.4|2022-12-01|
|Oracle EBS Spoke|1.13.2|2025-07-10|
|Oracle Financial Cloud Spoke|1.2.0|2025-11-06|
|Oracle HCM Cloud Spoke|4.3.0|2025-12-11|
|Oracle Netsuite Spoke|1.0.3|2025-09-10|
|Oracle Object Storage Management Spoke|1.0.3|2022-09-21|
|Oracle Peoplesoft Financial Spoke|1.1.0|2024-03-07|
|Oracle Virtual Cloud Network Spoke|1.0.4|2022-12-01|
|Order Case Playbook|1.4.1|2025-12-11|
|Order Case Playbook|1.4.1|2025-12-11|
|Order Case Self Service|1.4.3|2026-06-16|
|Order Case Self Service|1.4.3|2026-06-16|
|Order Management|5.0.0|2023-02-02|
|Order Management for Business Locations|2.0.0|2026-03-12|
|Order Management for Telecom, Media and Tech|13.1.2|2025-12-11|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Operations Case Management|2.8.0|2026-06-16|
|Order Operations Case Management|2.8.0|2026-06-16|
|Order Qualification Management|4.5.0|2026-06-16|
|Order Qualification Management|4.5.0|2026-06-16|
|Order to cash common architecture|1.5.0|2026-03-12|
|OT Asset Management|2.2.0|2025-12-11|
|OT Asset Management Advanced|1.0.0|2026-04-09|
|OT Manager Foundation|3.3.3|2026-06-16|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|Outlook Actionable Messages|4.7.0|2026-06-16|
|Outsourced Customer Service|2.1.2|2026-03-12|
|PagerDuty Spoke|1.5.1|2026-01-20|
|Palo Alto Networks NGFW for Security Operations|10.5.2|2025-12-11|
|Parallel Review and Feedback|21.1.0|2025-12-11|
|PAR CoreUI Migration Scripts|4.0.3|2026-03-12|
|Participant Suggestions|2.0.1|2024-08-01|
|Password Reset for Service Operations Workspace|9.2.0|2026-06-16|
|Password Reset for Virtual Agent|5.0.6|2025-07-31|
|Password Reset integration for Microsoft Active Directory|4.0.0|2025-07-31|
|Password Reset integration with Google Directory|1.0.3|2023-06-01|
|Password Reset integration with Okta|1.1.2|2023-04-06|
|Password Reset UI components for Configurable Workspaces|9.2.0|2026-06-16|
|Patch Management Data Model|1.0.4|2025-05-01|
|Pattern Designer Enhancements|3.9.0|2025-12-11|
|Payment framework for conversational channels|1.1.0|2026-03-12|
|PDF Extractor|28.2.1|2025-12-11|
|PDF Extractor|28.2.1|2025-12-11|
|PDF Extractor|28.2.1|2025-12-11|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics Content Pack for Agile 2.0|1.4.6|2025-12-11|
|Performance Analytics Content Pack for Cloud Resources|1.5.0|2024-11-07|
|Performance Analytics Content Pack for Essential SAFe|1.4.2|2023-09-20|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Legal Service Delivery|2.7.0|2025-12-11|
|Performance Analytics Content Pack for Public Sector Digital Services|2.0.3|2024-09-10|
|Performance Analytics - Content Pack - Guided Tours|1.4.0|2026-03-12|
|Performance Analytics for Configuration Compliance|1.5.2|2025-12-11|
|Performance Analytics for Security Incident Response|10.5.2|2025-05-01|
|Performance Analytics for Sourcing and Procurement Operations|3.0.9|2024-08-01|
|Performance Analytics for Vulnerability Response|12.16.1|2025-12-11|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Appraisal App Template|28.2.1|2025-12-11|
|Personal Lines Claims|4.4.0|2026-03-12|
|Personal Lines Claims|4.4.0|2026-03-12|
|Personal Lines Claims|4.4.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Physical Assets|2.3.0|2026-03-12|
|Pipeline|29.2.1|2026-06-16|
|Planned Maintenance Management|2.14.0|2026-06-16|
|Planned Task Common|1.1.0|2025-12-11|
|Planned Work Management|2.11.0|2025-12-11|
|Playbook Experience|29.2.1|2026-04-09|
|Playbook Experience Components|29.2.1|2026-04-09|
|Playbooks for Customer Service Management|6.5.1|2026-06-16|
|Plivo Spoke|1.2.0|2025-11-06|
|Pluralsight Spoke|1.2.1|2025-05-01|
|Policy as Code Engine|3.2.1|2025-12-11|
|policy-as-code-engine-ui|3.1.1|2025-07-31|
|POM - Foundation|1.1.2|2026-06-16|
|POM - Prime|1.1.1|2026-06-16|
|Portal navigation demo|27.0.0|2025-06-05|
|Portal Next Experience Theme|24.2.2|2026-03-12|
|Portfolio Planning integrations for Shared Infrastructure|3.12.0|2026-06-16|
|Portfolio Planning with PPM, Agile 2.0, and SAFe|4.7.0|2026-06-16|
|Post Assessment Actions for Smart Assessments|22.3.2|2026-06-16|
|Post Assessment Actions for Smart Assessments|22.3.2|2026-06-16|
|PPM Collaboration|2.1.0|2024-11-07|
|Predictive Intelligence for Legal Service Delivery|1.2.0|2025-12-11|
|Predictive Intelligence for User Reported Phishing|10.3.7|2024-09-10|
|Predictive Intelligence Store App|1.0.3|2025-12-11|
|Preferred tables|29.1.1|2026-03-12|
|Price Management|17.0.1|2026-06-16|
|Privacy Employee User|19.0.1|2024-08-01|
|Private cloud orchestration|1.0.0|2025-12-11|
|Proactive Customer Service Operations|25.0.1|2026-03-12|
|Proactive Customer Service Operations with Event Management|25.0.2|2026-03-12|
|Proactive Engagement|4.0.0|2026-03-12|
|Proactive Engagement|4.0.0|2026-03-12|
|Proactive Engagement|4.0.0|2026-03-12|
|Proactive Engagement|4.0.0|2026-03-12|
|Proactive Prompts|3.5.1|2026-06-16|
|Proactive Triggers|3.0.10|2025-12-11|
|Problem Management for Service Operations Workspace|9.2.0|2026-06-16|
|Problem Management Migration Utility|2.3.0|2026-03-12|
|Process Automation Content|28.1.4|2025-09-10|
|Process Automation Designer|29.2.1|2026-04-09|
|Process Automation Experience Demo|24.1.4|2024-10-03|
|Process Mining|29.7.9|2026-05-05|
|Process Mining Content Pack for CSM|23.2.0|2025-07-31|
|Process Mining Content Pack for FSM|1.5.0|2026-03-12|
|Process Mining Content Pack for SPM|1.0.2|2026-03-12|
|Process Mining for external data|29.5.0|2026-03-12|
|Process Mining for external data|29.5.0|2026-03-12|
|Process Mining for external data|29.5.0|2026-03-12|
|Process Mining for Source-to-Pay Operations|1.0.1|2024-08-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining Workspace Components|29.7.9|2026-05-05|
|Procurement Case Management|19.0.3|2026-06-16|
|Procurement File Transfer Framework|2.2.2|2023-05-04|
|Procurement for Field Service|3.0.0|2026-03-12|
|Product and pricing rules|9.0.0|2025-12-11|
|Product Capability Core|1.6.6|2026-03-12|
|Product Capability Core|1.6.6|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Conditions Core|4.6.0|2026-06-16|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Inventory Advanced|14.0.1|2026-06-16|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Profanity filter for agent chat|3.0.12|2024-11-07|
|Professional Data Model|1.1.0|2025-12-11|
|Project Status Report|1.1.0|2023-02-02|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|Public Sector Digital Services AI Agent Collection|1.3.1|2026-06-16|
|Public Sector Digital Services Core|14.0.1|2026-06-16|
|Purchase Order Management|2.2.2|2026-06-16|
|Qualtrics Spoke|1.3.0|2025-11-06|
|Qualys Integration for Security Operations|12.19.6|2025-12-11|
|Quick filter component|27.1.4|2025-07-31|
|Quick links component for Service Operations Workspace|9.2.0|2026-06-16|
|Quote Management Application|9.1.0|2025-12-11|
|Quote Management Data Model|9.0.0|2025-12-11|
|Quote Management for Business Locations|2.0.0|2026-03-12|
|RAG for code generation|1.1.8|2026-03-12|
|Rally Spoke|1.0.3|2023-05-04|
|Rapid7 Integration for Security Operations|13.16.4|2025-12-11|
|Recommended Actions|42.0.0|2026-06-16|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions for Customer Service|30.0.1|2025-07-31|
|Recommended Actions for ITSM|3.3.0|2026-03-12|
|Recommended Actions for OTSM|3.1.0|2026-03-12|
|Record lookup connected component|28.0.1|2025-12-11|
|Record Page for Service Operations Workspace|9.2.0|2026-06-16|
|Record Related Items Connected|2.2.0|2025-12-11|
|Record - vertical|22.3.1|2026-06-16|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Regulatory Agency Library|22.3.0|2026-06-16|
|Related party|1.0.6|2023-02-02|
|Related party|1.0.6|2023-02-02|
|ReleaseOps|1.2.3|2026-02-05|
|Release Timeline Component|1.4.0|2025-12-11|
|Remedial Actions Framework|9.2.0|2026-06-16|
|Remediation for Security Exposure Management|30.2.0|2026-01-20|
|Remediation Playbooks|1.1.0|2022-11-03|
|Requester Experience Templates|1.0.0|2024-11-07|
|Request Management for Service Operations Workspace|9.2.0|2026-06-16|
|Requirement Intake Diagram|1.0.1|2024-12-05|
|Resizable panes component|28.0.3|2025-12-11|
|Resolution Shaper|29.0.10|2026-03-12|
|Resolution Shaper|29.0.10|2026-03-12|
|Retail Core|7.0.0|2026-03-12|
|Retail Core|7.0.0|2026-03-12|
|Retry Handler Framework|1.0.2|2022-09-21|
|Rich Text Editor Component for Security Operations|2.0.1|2026-06-16|
|Risk Assessments for Supplier Lifecycle Operations|4.0.0|2026-06-16|
|Risk Assessments for Supplier Lifecycle Operations|3.0.0|2025-12-11|
|Risk Assessments for Supplier Lifecycle Operations|3.0.0|2025-12-11|
|Risk Assessments for Supplier Lifecycle Operations|3.0.0|2025-12-11|
|Risk Assessments for Supplier Lifecycle Operations|3.0.0|2025-12-11|
|Risk Scoring for Security Exposure Management|30.1.3|2026-01-20|
|RMA Case Management|2.1.0|2026-03-12|
|Roadmunk Spoke|1.6.5|2024-07-11|
|RPA Hub|17.0.0|2026-03-12|
|RPA Plugin Bundle|17.0.0|2026-03-12|
|RSM - Advanced|1.0.0|2026-04-09|
|RSM AI agent collection|1.4.0|2026-04-09|
|RSM - Foundation|1.0.0|2026-04-09|
|RSM - Prime|1.0.0|2026-04-09|
|Saba Spoke|1.2.2|2026-06-16|
|Safe Workplace Dashboard|1.41.0|2025-07-31|
|Safe Workplace for mobile|2.10.3|2025-07-31|
|Safe Workplace suite|1.34.2|2025-07-31|
|Safe Workplace suite Professional|1.25.2|2025-07-31|
|Sales Agreement Data Model|8.0.0|2025-12-11|
|Sales Agreement Management|8.0.0|2025-12-11|
|Sales and Order Management for Technology Provider - Advanced|1.0.3|2026-06-16|
|Sales and Order Management for Technology Provider - Prime|1.0.3|2026-06-16|
|Sales and Order Management for Telecommunications, Media and Technology - Advanced|1.0.3|2026-06-16|
|Sales and Order Management for Telecommunications, Media and Technology - Prime|1.0.4|2026-06-16|
|Sales and Order Management Mobile Common|29.1.2|2026-03-12|
|Sales and Service API Core|7.3.0|2026-06-16|
|Sales Cart|2.1.0|2025-12-11|
|Sales Cart|2.1.0|2025-12-11|
|Sales Development AI Agents|1.0.9|2026-05-05|
|Salesforce Marketing Cloud Spoke|1.5.1|2025-03-12|
|Salesforce Spoke|2.3.4|2025-11-06|
|Sales Forecasting|2.0.1|2025-12-11|
|Sales Quota Application|1.1.0|2025-12-11|
|Sales Quota Data Model|1.1.0|2025-12-11|
|Sales Territory Management|2.0.0|2026-03-12|
|SBOM Core|6.2.2|2025-12-11|
|SBOM Response|6.4.1|2025-12-11|
|Scan Engine|3.0.4|2026-06-16|
|SCCM Usage Metering Spoke|1.0.2|2023-09-07|
|Scenario Planning for PPM|2.4.0|2025-12-11|
|Schedule Optimization|29.0.13|2026-03-12|
|Scope 3 emissions management|21.1.1|2025-12-11|
|Scrum Common|1.4.5|2025-01-30|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Secops Health Analytics|30.1.0|2025-12-11|
|Secureworks CTP Spoke|1.0.3|2022-09-21|
|Secureworks Ticket Ingestion Integration for Security Operations|11.1.2|2026-02-05|
|Security Case Management common PAD artefacts|1.1.12|2026-01-20|
|Security Case Management common workspace components|2.1.0|2026-06-16|
|Security Center|3.2.5|2026-06-16|
|Security Exposure Management Workspace|30.2.2|2026-01-20|
|Security Incident Response - Advanced|1.0.7|2026-06-16|
|Security Incident Response - Foundation|1.0.7|2026-06-16|
|Security Incident Response integration with AWS SecurityHub|1.1.0|2025-12-11|
|Security Incident Response Integration with CrowdStrike Next-Gen SIEM|2.3.1|2025-12-11|
|Security Incident Response integration with FireEye HX|1.1.0|2025-12-11|
|Security Incident Response integration with Microsoft Defender for Endpoint|1.2.1|2026-02-05|
|Security Incident Response Integration with Palo Alto Networks XSIAM|3.0.2|2026-01-20|
|Security Incident Response integration with Proofpoint|1.1.0|2025-12-11|
|Security Incident Response Integration with Zscaler|11.2.3|2026-02-05|
|Security Incident Response Mobile|10.4.0|2024-11-07|
|Security Incident Response - Prime|1.0.7|2026-06-16|
|Security Incident Response Process Mining Content Pack|1.0.3|2026-03-12|
|Security Incident UI Card Component|1.0.1|2023-12-07|
|Security Integration Framework|13.12.1|2025-12-11|
|Security Operations 'Have I been pwned?' Integration|10.5.1|2025-03-12|
|Security Operations CrowdStrike Intelligence Integration|10.8.0|2025-12-11|
|Security Operations Hybrid Analysis Integration|10.7.0|2026-02-05|
|Security Operations LogRhythm Integration|11.2.1|2025-12-11|
|Security Operations Metadefender Integration|10.5.0|2024-08-01|
|Security Operations Palo Alto Networks - AutoFocus|10.4.0|2025-01-30|
|Security Operations Palo Alto Networks - WildFire|10.4.0|2025-01-30|
|Security Operations PhishTank Integration|10.5.0|2024-08-01|
|Security Operations Reverse WHOIS Integration|10.5.0|2025-12-11|
|Security Operations RiskIQ Integration|10.4.1|2024-08-01|
|Security Operations Setup Assistant|10.4.41|2026-06-16|
|Security Operations Shodan Integration|10.4.1|2024-08-01|
|Security Operations Spoke|10.6.7|2025-06-05|
|Security Operations VirusTotal Integration|10.4.1|2025-12-11|
|Security Posture Control Core|7.0.1|2025-12-11|
|Security Simulation and Training Integration for SecOps|2.1.3|2024-05-09|
|Security Support Common|30.4.1|2026-06-16|
|Security Support Orchestration|12.13.4|2025-01-30|
|Service Bridge for Public Sector Digital Services \(PSDS\)|1.0.2|2025-05-01|
|Service Builder|3.6.1|2025-12-11|
|Service Builder Components|2.2.0|2025-12-11|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Contractor Base|2.0.0|2026-03-12|
|Service Exchange Base|2.3.10|2026-03-19|
|Service Exchange for Consumers|2.3.10|2026-03-19|
|Service Exchange Health|2.3.10|2026-03-19|
|Service Exchange Remote Process Sync Transport|2.3.10|2026-03-19|
|Service Graph Connector Dependencies|1.0.0|2021-01-21|
|Service Graph Connector for Akamai API Security|1.0.0|2025-10-16|
|Service Graph Connector for AWS|2.12.1|2025-10-16|
|Service Graph Connector for ExtraHop|2.0.3|2020-09-16|
|Service Graph Connector for GCP|1.11.0|2025-10-16|
|Service Graph Connector for Google Console|1.0.0|2024-08-01|
|Service Graph Connector for Infoblox|1.4.0|2025-07-31|
|Service Graph Connector for Jamf|2.14.4|2025-09-10|
|Service Graph Connector for Microsoft Azure|1.15.0|2025-12-11|
|Service Graph Connector for Microsoft Defender Endpoint|1.2.0|2025-05-01|
|Service Graph Connector for Microsoft Defender for IoT \(Azure\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Excel|4.0.0|2026-06-16|
|Service Graph Connector for Microsoft Excel|4.0.0|2026-06-16|
|Service Graph Connector for Microsoft Excel|4.0.0|2026-06-16|
|Service Graph Connector for Microsoft Intune|2.7.1|2025-10-16|
|Service Graph Connector for Microsoft SCCM|3.8.0|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Service Graph Connector for Observability - AppDynamics|1.6.0|2025-12-11|
|Service Graph Connector for Observability - Datadog|1.4.0|2025-12-11|
|Service Graph Connector for Observability - Dynatrace|1.13.1|2025-09-10|
|Service Graph Connector for Observability - New Relic|1.4.0|2025-12-11|
|Service Graph Connector for OpenTelemetry|1.4.1|2024-05-09|
|Service Graph Connector for SolarWinds|2.6.0|2025-07-31|
|Service Graph Connector for Tanium|1.8.2|2025-11-06|
|Service Graph Connector for Trellix|1.0.0|2025-06-05|
|Service Graph Connector for VMware Workspace ONE UEM|1.8.0|2025-07-31|
|Service Graph Connector for Wiz|1.4.0|2025-11-06|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Licensing|1.0.0|2022-05-05|
|Service Graph Connector Support Tools|1.0.0|2024-02-01|
|Service Level Management Experience for Workspace|9.2.0|2026-06-16|
|Service Level Objective Management for Service Operations Workspace|1.5.1|2025-12-11|
|Service Mapping Plus|1.17.2|2026-01-20|
|ServiceNow Add-Ins for Microsoft Office|7.4.3|2026-03-12|
|ServiceNow Document Designer with Word|22.3.2|2026-06-16|
|ServiceNow Enterprise Asset Management|10.0.0|2026-03-12|
|ServiceNow ITOM/OT SU Licensing|3.11.0|2025-12-11|
|ServiceNow Kafka Consumer|1.0.1|2023-04-06|
|ServiceNow Remote Instance Spoke|2.2.9|2025-11-06|
|ServiceNow Studio|29.2.6|2026-06-16|
|ServiceNow Studio for App Engine|28.2.1|2025-12-11|
|ServiceNow Voice|5.0.1|2026-02-05|
|ServiceNow Voice for CSM|3.10.0|2026-02-05|
|ServiceNow Voice for HR Service Delivery \(HRSD\)|1.0.5|2025-12-11|
|ServiceNow Voice for ITSM|4.1.1|2025-12-11|
|ServiceNow Voice UI components|3.8.0|2026-02-05|
|ServiceNow Voice with Amazon Connect|4.9.1|2026-03-12|
|service-observability-app|1.10.12|2025-12-11|
|Service Observability UI|1.10.12|2025-12-11|
|Service Operations Workspace Admin Center|9.2.0|2026-06-16|
|Service Operations Workspace Core|9.2.0|2026-06-16|
|Service Operations Workspace Express List App|27.1.2|2026-06-16|
|Service Operations Workspace Integrations launchpad|27.1.5|2026-06-16|
|Service Operations Workspace Integrations launchpad UI|27.1.1|2026-06-16|
|Service Operations Workspace ITSM Admin Center|9.2.0|2026-06-16|
|Service Operations Workspace ITSM Advanced Applications|9.2.1|2026-06-16|
|Service Operations Workspace ITSM Applications|9.2.0|2026-06-16|
|Service Operations Workspace ITSM Common|9.2.0|2026-06-16|
|Service Operations Workspace Link View|27.1.1|2026-06-16|
|Service Operations Workspace Log Analytics|26.6.1|2026-06-16|
|Service Operations Workspace Metric Explorer|27.1.1|2026-06-16|
|Service Operations Workspace Metric Explorer APIs|23.4.0|2025-07-31|
|Service Operations Workspace Service Map Monitoring|26.5.0|2025-07-31|
|Service Operations Workspace Service Reliability Management \(SRM\) Common|6.5.3|2025-12-11|
|Service Organization|2.3.1|2026-03-12|
|Service Reliability Management|6.5.1|2025-12-11|
|Service Request Criteria|3.1.0|2026-06-16|
|Service Request Management App Template|28.2.1|2025-12-11|
|Service Test Management|5.0.1|2025-12-11|
|SGC Central|2.4.0|2026-03-12|
|Shared Library for Talent Development|2.5.0|2026-06-16|
|SharePoint Online Search Connector|6.1.2|2024-11-07|
|Shift Handover Application|1.8.0|2026-06-16|
|Shift Planning|7.0.0|2026-03-12|
|Shift Planning for Configurable Workspace|3.8.0|2026-03-12|
|Shodan Exploit Integration for Security Operations|10.8.0|2024-11-07|
|Shopping Hub|11.1.1|2026-06-16|
|Shopping Hub Mobile|7.6.24|2025-07-31|
|Sitemap Generator|1.2.0|2025-07-31|
|Site Mapping for Field Service Management|2.1.1|2026-03-12|
|Site Reliability Metrics|2.1.7|2023-11-02|
|Site Reliability Metrics UX|2.1.7|2023-11-02|
|Site Reliability Operations|14.2.3|2024-05-09|
|Skill Review Management|1.6.1|2025-12-11|
|Skill Rule|1.0.3|2026-03-12|
|Skills foundation|10.1.0|2026-06-16|
|Skills Industry Data|2.2.0|2026-06-16|
|Skills Workspace|6.1.0|2025-12-11|
|Slack Activities for PAD|1.0.3|2023-01-12|
|Slack Chat Connector for Security Incident Management|1.0.1|2025-05-01|
|Slack Spoke|1.8.0|2025-09-10|
|SLO - Foundation|1.2.0|2026-06-16|
|SLO - Prime|1.2.0|2026-06-16|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Smart Assessment for Field Service Questionnaire|3.0.2|2026-03-12|
|Smart Assessment for Mobile|3.0.1|2026-03-12|
|Smart Assessment Migration tools|22.3.1|2026-06-16|
|Smart Assessment Migration tools|22.3.1|2026-06-16|
|SmartRecruiters Spoke|1.0.0|2021-11-18|
|Smartsheet Spoke|2.6.1|2026-01-20|
|sn-4q-bubble|23.2.3|2026-06-16|
|sn-actionable-insights|1.1.1|2026-06-16|
|sn-apm-diagram-builder|3.7.0|2026-06-16|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-par-coreui-migration-center|4.0.3|2026-03-12|
|sn-app-par-coreui-migration-legacy-widget|4.0.3|2026-03-12|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|sn-chart-renderer|29.0.8|2026-04-09|
|sn-circuit-map|5.0.0|2025-07-31|
|sn-circuit-map|5.0.0|2025-07-31|
|sn-circuit-map|5.0.0|2025-07-31|
|sn-cmdb-nlq-search|2.3.3|2024-11-07|
|sn-component-account-hierarchy|29.0.7|2026-03-12|
|sn-component-account-hierarchy|29.0.7|2026-03-12|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|sn-component-workspace-ribbon|30.0.0|2026-03-12|
|sn-component-workspace-ribbon|30.0.0|2026-03-12|
|sn-component-workspace-shn|29.0.7|2026-03-12|
|sn-component-workspace-shn|29.0.7|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|sn-cwm-agile|2.1.0|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-docintel-iframe|1.0.4|2024-02-01|
|sn-docs|7.6.0|2026-06-16|
|sn-formula-kit|1.0.1|2026-06-16|
|sn-fsm-components|29.0.5|2026-03-12|
|sn-guided-action-experience|39.0.1|2025-12-11|
|sn-guided-action-experience|39.0.1|2025-12-11|
|sn-guided-action-experience|39.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-hla-admin-experience|1.0.2|2026-01-20|
|sn-hr-casecard|1.3.2|2025-12-11|
|sn-ia-summary-card|1.0.1|2025-05-01|
|sn-multipivot|29.0.8|2026-04-09|
|sn-next-best-action-list|39.0.0|2026-06-16|
|sn-next-best-action-list|39.0.0|2026-06-16|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Snowflake Spoke|1.0.3|2025-09-10|
|sn-par-analytics-list|29.0.8|2026-04-09|
|sn-par-forecast-config|29.0.8|2026-04-09|
|sn-par-multipivot-extension|29.0.8|2026-04-09|
|sn-quick-filter-popover|24.3.1|2026-05-05|
|sn-rack|4.0.0|2025-07-31|
|sn-rack|4.0.0|2025-07-31|
|sn-rack|4.0.0|2025-07-31|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|sn-scorecard-list|29.0.8|2026-04-09|
|sn-smart-assessment-connected|22.3.3|2026-06-16|
|sn-smart-assessment-connected|22.3.3|2026-06-16|
|sn-smart-assessment-designer|22.3.1|2026-06-16|
|sn-smart-assessment-designer|22.3.1|2026-06-16|
|sn-timer|2.0.1|2026-03-12|
|sn-topology-map|4.0.0|2025-07-31|
|sn-topology-map|4.0.0|2025-07-31|
|sn-topology-map|4.0.0|2025-07-31|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-uxf-formula-parser|29.1.0|2026-03-12|
|Socure Spoke|1.2.2|2026-03-12|
|Software Asset Management for CPE support|1.0.0|2022-08-04|
|Software Asset Management Guided Experiences|7.0.1|2026-03-12|
|Software Asset Management integration with Salesforce CRM|2.0.1|2025-12-11|
|Software Asset Management integration with Salesforce Marketing Cloud|1.2.7|2025-03-12|
|Software Asset Management integration with Tableau|1.0.1|2024-08-01|
|Software Asset Management integration with Workday|1.0.12|2025-01-30|
|Software Asset Management Professional for Engineering Applications|1.0.3|2026-03-12|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM - Prime|1.0.1|2026-04-09|
|Source-to-Pay Common Architecture|24.0.0|2026-06-16|
|Source-to-Pay Integration Framework|14.0.2|2026-06-16|
|Source-to-Pay Operations with Contract Management Pro|2.0.1|2025-05-01|
|Source-to-Pay Workspace|20.0.1|2026-06-16|
|Sourcing and Purchasing Automation|11.4.1|2026-06-16|
|SOW Funnel Highchart Component|28.3.1|2026-03-12|
|Special Handling Instruction|26.0.3|2026-05-05|
|Spend and Savings Management|5.0.2|2026-06-16|
|Splunk Search Integration for Security Operations|10.5.0|2025-07-31|
|SPM Benchmarking|1.0.0|2022-11-03|
|SPM Common UI Component|4.1.0|2026-03-12|
|SPM Team Member|1.0.0|2026-04-09|
|SPO - Foundation|1.2.0|2026-06-16|
|Spoke Generator|4.2.4|2026-03-12|
|SPO - Prime|1.2.0|2026-06-16|
|SPW Jira Integrations|1.0.0|2025-12-11|
|Status Report UI Component for MSIM Workspace|1.0.2|2024-11-07|
|Strategic Planning|4.13.0|2026-04-09|
|Strategic Portfolio Management - Advanced|1.0.2|2026-04-09|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management - Prime|1.0.4|2026-04-09|
|Strategic Spend Tracking for PPM|1.2.0|2025-12-11|
|Stream Connect Designer|5.0.1|2026-03-12|
|Subscription Management v2|6.4.3|2026-06-16|
|SuccessFactors Learning Spoke|1.0.0|2025-01-30|
|Summarization for Order Management|2.1.0|2026-05-05|
|Summarization for Quote Management|1.1.0|2026-04-09|
|SumTotal Spoke|1.1.0|2023-03-02|
|Supplier Collaboration Portal|11.0.0|2026-06-16|
|Supplier Collaboration Portal|11.0.0|2026-06-16|
|Supplier Operations|7.0.0|2026-06-16|
|Supplier Operations|7.0.0|2026-06-16|
|Supplier Payment Optimization|6.0.0|2026-06-16|
|Supplier Payment Optimization|6.0.0|2026-06-16|
|Supplier Relationship and Performance Management|10.0.0|2026-06-16|
|Supplier Relationship and Performance Management|10.0.0|2026-06-16|
|SurveyMonkey Spoke|2.0.6|2024-08-01|
|Surveys for mobile|1.0.2|2021-09-16|
|Sustainable IT|21.1.0|2025-12-11|
|Synthetic Monitoring|1.4.4|2025-12-11|
|System Events and Jobs Dashboard|3.1.5|2026-03-12|
|Tableau Spoke|1.0.2|2024-08-01|
|Table Builder|29.1.1|2026-03-12|
|Tag Based Alert Clustering Engine|18.24.0|2026-06-16|
|Tag Governance|1.8.0|2025-12-11|
|Talent Development Core|5.5.0|2026-06-16|
|Talent feedback|1.3.0|2026-06-16|
|Targeted Communications|30.0.0|2026-03-12|
|Task activity timeline|25.4.0|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Task Communications Management UI Components for Configurable Workspaces|9.2.0|2026-06-16|
|Task Intelligence Admin Console|5.2.1|2025-12-11|
|Task Intelligence for Customer Service|25.4.0|2025-12-11|
|Task Intelligence for ITSM|8.2.1|2025-12-11|
|Task Plan Template AI Agents|1.0.0|2026-06-16|
|Task Plan Templates|4.0.0|2026-06-16|
|Task Quality Review Management|29.1.1|2026-03-12|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Task SLA cards|26.0.0|2026-03-12|
|Task SLA cards|26.0.0|2026-03-12|
|Team Contacts App Template|28.2.1|2025-12-11|
|Team Performance|202603.0.0|2026-03-12|
|Technician driven sales with Field Service|29.1.2|2026-03-12|
|Technology Advanced|1.0.4|2026-06-16|
|Technology Foundation|1.0.4|2026-06-16|
|Technology Portfolio Management|1.10.0|2026-06-16|
|Technology Prime|1.0.4|2026-06-16|
|Telecom Discovery Patterns|1.0.2|2025-12-11|
|Telecommunication Open APIs|6.0.9|2025-12-11|
|Telecommunications, Media and Technology - Advanced|1.0.3|2026-06-16|
|Telecommunications, Media and Technology - Foundation|1.0.4|2026-06-16|
|Telecommunications, Media and Technology - Prime|1.0.3|2026-06-16|
|Telecommunications Advanced|2.0.1|2026-06-16|
|Telecommunications Advanced|2.0.1|2026-06-16|
|Telecommunications Alarm Management Open API|7.0.1|2025-12-11|
|Telecommunications Foundation|2.0.1|2026-06-16|
|Telecommunications Foundation|2.0.1|2026-06-16|
|Telecommunications Media and Technology AI agent collection|6.0.1|2026-06-16|
|Telecommunications Media and Technology AI agent collection|6.0.1|2026-06-16|
|Telecommunications Prime|2.0.1|2026-06-16|
|Telecommunications Prime|2.0.1|2026-06-16|
|Telecom Service Operations Core|1.2.1|2025-12-11|
|telemetry-data-connector|1.2.1|2026-05-05|
|Territory Planning|30.0.3|2026-03-12|
|Test Generation|4.0.11|2025-12-11|
|Theme Builder|6.1.5|2026-01-22|
|Theme Builder AI|1.1.0|2026-05-05|
|Third-party Risk Due Diligence|22.3.1|2026-06-16|
|Third-party Risk Management|22.3.3|2026-06-16|
|Threat and alert data feeds for Crisis Management|11.0.1|2026-06-16|
|Threat Intelligence|13.4.4|2026-02-05|
|Threat Intelligence Security Center integration with CrowdStrike Intelligence|3.0.4|2025-03-12|
|Threat Intelligence Security Center integration with Elasticsearch|3.0.4|2025-05-01|
|Threat Intelligence Security Center integration with Microsoft Defender for Endpoint|1.0.4|2025-06-05|
|Threat Intelligence Security Center Integration with Palo Alto Networks NGFW|2.0.1|2025-03-12|
|Threat Intelligence Security Center integration with Shodan|1.0.7|2025-05-01|
|Threat Intelligence Security Center integration with Splunk Search|3.0.5|2025-03-12|
|Threat Intelligence Security Center integration with VirusTotal|3.0.3|2025-03-12|
|Threat Intelligence Security Center integration with WHOIS|5.0.4|2025-03-12|
|Threat Intelligence Support Common|13.6.4|2026-06-16|
|Threat Intelligence Support Common UI Components|1.1.4|2025-12-11|
|Timeline component|29.0.0|2026-03-12|
|Time Off Request App Template|28.2.1|2025-12-11|
|Total Cost of Ownership|1.1.0|2026-06-16|
|Touchpoint Meeting|2.7.0|2026-06-16|
|Transporter|2.3.10|2026-03-19|
|Trello Spoke|1.4.0|2025-11-06|
|Triggers|29.0.2|2026-03-12|
|Twilio Spoke|1.2.0|2023-02-02|
|UCF Spoke|1.1.0|2023-05-04|
|Udemy Spoke|1.0.2|2022-12-01|
|UI Builder|29.1.52|2026-03-12|
|UI Components for Customer Portals|4.0.0|2026-02-05|
|UI Components of Collaboration for Configurable Workspaces|9.2.0|2026-06-16|
|UI Generation|29.2.5|2026-05-05|
|UiPath Spoke|2.5.1|2025-11-06|
|UI shared library|1.6.2|2026-06-16|
|UKG Spoke|3.5.0|2025-12-11|
|Unified Content Management|22.3.1|2026-06-16|
|Unified Security Exposure Management|30.2.7|2026-01-20|
|Universal Request AI agent collection|1.0.9|2026-06-16|
|Universal Request for Source-to-Pay Operations|1.2.2|2026-06-16|
|Universal Request integration with Microsoft Teams|1.0.2|2022-12-01|
|Universal Task|2.8.0|2026-06-16|
|Urjanet ESG integration|21.1.1|2025-12-11|
|Usage Insights Funnel|6.1.12|2026-03-12|
|User Experience Analytics API|3.1.2|2024-02-01|
|User Experience Redirection|1.0.1|2026-03-12|
|User Sense|1.1.13|2025-12-11|
|User Surveys|1.5.4|2025-12-11|
|Utility Actions Spoke|1.3.0|2024-10-03|
|UX Commons|27.0.2|2025-07-31|
|Vaccination Status|1.25.0|2025-12-11|
|Value stream artifacts|2.3.0|2026-06-16|
|Vault Console|2.1.0|2026-06-16|
|Vendor Manager Workspace|3.5.0|2024-11-07|
|Vendor Risk Management integration with EcoVadis|21.1.1|2025-12-11|
|Verifi Spoke|1.0.0|2024-08-01|
|Virtual Agent Adapter Common|6.2.3|2026-03-12|
|Virtual Agent API|4.3.0|2026-04-09|
|Virtual Agent for PPM|1.0.1|2023-05-04|
|Virtual Agent for Source-to-Pay Operations|3.11.0|2025-07-31|
|Virtual Agent Topic Recommendations|4.5.5|2024-08-01|
|Virtual Machine Management for Virtual Agent|3.0.11|2023-08-03|
|Visa Spoke|2.2.2|2025-12-11|
|Visibility Content|6.30.2|2026-04-23|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Vonage Spoke|1.2.0|2025-12-11|
|Vulnerability Crisis Management|1.0.1|2024-08-01|
|Vulnerability Exposure Assessment|30.2.1|2026-01-20|
|Vulnerability Response|30.2.5|2026-01-20|
|Vulnerability Response Common|30.2.8|2026-01-20|
|Vulnerability Response Common Workspace|30.2.7|2026-01-20|
|Vulnerability Response Integration Framework|1.3.0|2026-01-20|
|Vulnerability Response Integration with Agile Management|1.2.2|2025-07-31|
|Vulnerability Response Integration with Atlassian Jira|1.0.4|2024-05-09|
|Vulnerability Response Integration with Black Duck|1.1.1|2025-12-11|
|Vulnerability Response Integration with CISA|1.5.1|2025-07-31|
|Vulnerability Response Integration with Microsoft Defender for IoT \(Azure\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Threat and Vulnerability Management|2.8.1|2025-12-11|
|Vulnerability Response Integration with NVD|1.7.2|2025-07-31|
|Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute|3.5.0|2025-12-11|
|Vulnerability Response Integration with Palo Alto Prisma Cloud|2.8.0|2025-12-11|
|Vulnerability Response Integration with Tenable|5.2.1|2025-12-11|
|Vulnerability Response Integration with Veracode|4.7.3|2025-12-11|
|Vulnerability Response Licensing and Usage|2.9.1|2026-01-20|
|Vulnerability Response Mobile|11.1.1|2023-05-04|
|Vulnerability Response Patch Orchestration|2.2.5|2025-05-01|
|Vulnerability Response Patch Orchestration with HCL Bigfix|1.3.0|2025-05-01|
|Vulnerability Response Patch Orchestration with Microsoft SCCM|2.3.1|2025-05-01|
|Vulnerability Solution Management|10.4.3|2022-12-01|
|Walk-up Experience for Service Operations Workspace|9.2.0|2026-06-16|
|Walk-Up for CSM|2.0.1|2026-03-12|
|Watershed integration for ESG|16.0.1|2023-02-02|
|WDF Tokenization|2.0.2|2025-12-11|
|Whats New Framework Core|1.3.1|2026-03-12|
|WHOIS Integration for Security Operations|10.4.0|2024-08-01|
|Word Document Templates|1.10.0|2026-06-16|
|Workday ESG integration|21.1.1|2025-12-11|
|Workday Financials Spoke|2.1.0|2025-07-31|
|Workday HR Spoke|2.7.0|2025-12-11|
|Workday Learning Spoke|1.1.4|2024-04-04|
|Workflow Studio|29.1.1|2026-04-09|
|Workforce Optimization Common|1.7.0|2025-12-11|
|Workforce Optimization Configurable Workspace Core|1.11.0|2025-12-11|
|Workforce Optimization Configurable Workspace UI Components|4.4.1|2025-12-11|
|Workforce Optimization for CSM Configurable Workspace|5.0.0|2026-03-12|
|Workforce Optimization for HR|1.1.2|2025-07-31|
|Workforce Optimization for ITSM Configurable Workspace|2.9.0|2026-05-05|
|Workforce Optimization integration with Microsoft Outlook|1.4.0|2026-03-12|
|Workfront Spoke|1.3.0|2025-11-06|
|Work Item Integrations Common|1.15.0|2026-06-16|
|Workplace Agent for mobile|1.4.5|2026-03-12|
|Workplace Calendar Synchronization|3.3.0|2025-12-11|
|Workplace Connectors|2.3.1|2026-06-16|
|Workplace from Facebook Spoke|4.2.1|2025-11-06|
|Workplace Indoor Map Component|1.1.1|2024-08-01|
|Workplace PPE Inventory Management|1.18.0|2025-07-31|
|Workplace Reservations for Microsoft Outlook Add-in|1.12.2|2025-07-31|
|Workplace Service Delivery Enterprise|1.6.0|2025-12-11|
|Workplace Service Delivery for Mobile|1.16.2|2025-12-11|
|Workplace Service Delivery integration with Microsoft Places|1.2.5|2025-12-11|
|Workplace Service Delivery Professional|1.4.0|2025-12-11|
|Workplace Service Delivery Suite|2.17.2|2025-12-11|
|Workplace Services Kiosk|1.5.2|2025-12-11|
|Workplace Space Mapping|1.20.5|2026-06-16|
|Workplace Stack Plan|1.5.12|2026-06-16|
|Work Progress Status for Agile Teams|1.0.4|2025-06-05|
|Work Progress Status for SAFe|1.0.4|2025-06-05|
|Work Scheduler for Workforce Optimization|3.3.2|2026-03-12|
|Workspace App Shell|29.1.1|2026-03-12|
|Workspace Builder for App Engine|28.2.0|2025-12-11|
|Workspace Inspector|20.1.1|2025-05-01|
|Workspace navigation and experience demo|27.1.1|2026-03-12|
|Wrike Spoke|1.3.0|2025-09-10|
|WSD - Advanced|1.0.2|2026-06-16|
|WSD - Foundation|1.0.2|2026-06-16|
|WSD - Prime|1.0.2|2026-06-16|
|X Spoke|2.3.0|2025-09-10|
|YouTube Spoke|1.0.5|2025-07-10|
|Zendesk Spoke|1.8.0|2025-11-06|
|Zero Copy Connector for ERP|10.0.9|2026-05-05|
|Zero Copy Connector Hub|3.0.1|2026-03-12|
|Zoom extension for Omnichannel Callback|1.3.6|2025-07-31|
|Zoom Spoke|4.6.2|2026-01-20|

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/available-versions.md)


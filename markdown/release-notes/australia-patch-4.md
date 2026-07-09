---
title: Australia Patch 4
description: The Australia Patch 4 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/australia-patch-4.html
release: australia
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 112
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 4

The Australia Patch 4 release contains important problem fixes.

-   **Australia Patch 4 was released on July 09, 2026.**
    -   Build date: 07-05-2026\_0129
    -   Build tag: glide-australia-02-11-2026\_\_patch4-06-22-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A04.00.xlsx).

## Overview

Australia Patch 4 includes 420 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-ap4.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Australia Patch 4 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 4, refer to [KB3126028](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3126028).

## Changes in Australia Patch 4

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
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 3 Hot Fix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3104013)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)
-   [Australia Patch 2 Hot Fix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3101088)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/available-versions.md)


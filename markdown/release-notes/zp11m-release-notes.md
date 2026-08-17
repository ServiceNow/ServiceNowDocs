---
title: Zurich Patch 11m
description: The Zurich Patch 11m release contains important problem fixes via Zurich Patch 11 and updates to compatible ServiceNow Store applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zp11m-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-07-27"
reading_time_minutes: 242
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 11m

The Zurich Patch 11m release contains important problem fixes via Zurich Patch 11 and updates to compatible ServiceNow Store applications.

-   **Zurich Patch 11m was released on July 23, 2026.**
    -   Build date: 07-22-2026\_0426
    -   Build tag: glide-zurich-07-01-2025\_\_patch11m-07-09-2026

## Monthly "m" releases

Monthly "m" releases are now available for your ServiceNow AI Platform® instances. These releases, which are identified by an "m" in the release name, contain everything from the base family patches, the latest version of all AI applications, and those apps' supporting non-AI application dependencies.

**Important:**

This ServiceNow AI Platform® release is not available for ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z11.00.xlsx).

## Overview

Zurich Patch 11 includes 355 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-zp11.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Zurich Patch 11m includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 11m, refer to [KB3141209](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3141209).

## Changes in Zurich Patch 11m

See the following Now Support Knowledge Base articles for more information about upgrading to Zurich Patch 11m:

-   [KB3140377](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3140377)
-   [KB3141683](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3141683)
-   [KB3141830](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3141830)

-   **[Activate a pre-release feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/activate-prerelease-feature.md)**

    Activate a pre-release feature on the instance so your users can try it out and provide feedback to the product team.

-   **[Auto-upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/um-auto-upgrade.md)**

    The auto-upgrade mechanism automatically upgrades ServiceNow-managed applications across your instances on a regular schedule without requiring manual intervention. Auto-upgrade applies exclusively to ServiceNow-managed applications; customer-customized or third-party applications aren't included in automatic upgrades.

-   **[Deactivate a pre-release feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/deactivate-prerelease-feature.md)**

    Deactivate a pre-release feature if it is not working as expected or if you no longer need the feature.

-   **[Feature Preview Program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/feature-preview-program.md)**

    The Feature Preview Program provides access to pre-release capabilities on your instance. You can activate, test, and provide feedback on individual features before they are generally available.

-   **[Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md)**

    For Now Assist new features and changes, see [Now Assist and agentic AI release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/now-assist-rn-landing.md).


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

AI Search UX

 PRB2039564

</td><td>

Error while accessing catalog items from search after Australia upgrade

</td><td>

After upgrading to Australia, the typeahead widget for suggested results fails.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1994381

 [KB3006010](https://hi.service-now.com/kb_view.do?sysparm_article=KB3006010)

</td><td>

Discovery has issues on some node after upgrading in Australia

</td><td>

After upgrading to Australia, JavaScript running in app nodes fails to call Java functions. The following warning appears: '\*\*\* WARNING \*\*\* Evaluator: com.glide.script.RhinoEcmaError: undefined is not a function.' This impacts various features, including Discovery and Event Management.

</td><td>

Refer to the listed KB article for details.

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

Service Portal

 PRB1978655

 [KB3094451](https://hi.service-now.com/kb_view.do?sysparm_article=KB3094451)

</td><td>

Menu values for a **Reference** field in Record Producer aren't displayed when the language isn't English

</td><td>

In Service Portal, when users access a catalog item with a variable that references the user table and the logged-in user doesn't pass the query\_range ACL, then the menu of users is empty when the user language is non-English. However, the menu has values when the language is English. This is because there's a difference in the query string that is generated for English and non-English sessions.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2007255

 [KB3045151](https://hi.service-now.com/kb_view.do?sysparm_article=KB3045151)

</td><td>

There's memory pressure on nodes due to high memory for the cache 'com.glide.cs.qlue.module.coma.MessageBatchingSession'

</td><td>

Users with 2GB nodes may encounter memory issues that can cause the events process jobs to yield.

</td><td>

Run a heap dump.

 Observe that MacMessageBatchingSession or MessageBatchingSession uses over 50 MB of memory.

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
7.  Enter '@' and a character or two for a user to invoke the dropdown list for user selection.

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

After a video file is uploaded as an attachment to a record and the page is refreshed, the video renders inside the activity stream with native HTML5 video controls \(play/pause, scrubber, volume, full screen\). However, on selecting the video element, the controls disappear and become unusable, preventing the user from playing back, scrubbing, or otherwise interacting with the video.

</td><td>

1.  Log in to a ServiceNow instance.
2.  Open any task record that supports an activity stream and an **Attachments** field.
3.  Attach a video file to the record.
4.  Save the record.
5.  Refresh the page so the attached video renders inside the activity stream.
6.  In the activity stream, locate the entry containing the attached video.

The video element appears with native video controls \(play/pause, scrubber, volume, full screen\).

7.  Select the video element in the activity stream to attempt playback or interact with the controls.

 Expected behavior: The native video controls remain visible and interactive; the user can play, pause, scrub, adjust volume, and enter full screen.

 Actual behavior: On selection, the video controls disappear and become unusable. The video element renders but no playback controls can be interacted with.

</td></tr><tr><td>

Activity Stream

 PRB2023624

</td><td>

For the Core UI only, update the **Activity Stream** icon for AI specialist vs Agentic Workflow

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2029963

</td><td>

The **Copy** button for Journal entries does not work in List Activity Stream view

</td><td>

Content does not get copied to the clipboard and subsequently cannot get pasted.

</td><td>

1.  Navigate to **/incident\_list.do**.
2.  Select the **Show activity stream in a flyout window** button \(the **Heartbeat** icon at the top-right of the table\).
3.  Find a journal tile in the Activity Stream, and select the **Copy journal content** button.
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

 PRB2010201

</td><td>

The script action 'Set logged out agent offline' creates an offline Advanced Work Assignment \(AWA\) presence record for non-agent users

</td><td>

The script action will insert records to awa\_agent\_presence and awa\_agent\_channel\_availability when a user without awa\_agent role logs out.

</td><td>

1.  Log in to the latest Zurich instance.
2.  Impersonate a user without the awa\_agent role.
3.  Log out.
4.  Check awa\_agent\_presence and awa\_agent\_channel\_availability.

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

 PRB2026676

</td><td>

Enhanced updateSegment API \(wrap-up\) to support agent-initiated wrap-up

</td><td>

As a CCaaS Developer, the updateSegment API should be able to be used in the CCaaS plugin. This API should allow users to update a wrap-up segment at the same time as closing/updating the segment without requiring a separate API call. This allows the voice plugin to support agent-initiated wrap-up. Agents should have the ability to initiate a wrap-up before the call ends. If the system has wrap-up with a timer, they should get a timer on the wrap-up modal to provide the count down timer until the wrap-up is submitted.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB2026914

</td><td>

Duplicate work items when the service channel's work\_item\_table is a parent class of the routed record

</td><td>

Duplicate work items are created.

</td><td>

1.  Configure service channel against the parent table \(task\).
2.  In service channel condition, you can restrict the task type to only incident \(optional\).
3.  Have a live agent online with good capacity \(&gt;500\).
4.  Make sure auto acceptance is on.
5.  Create 200 incidents together via BG script.

 Expected behavior: 200 work items created.

 Actual behavior: 200&amp;\#43; work items created \(have duplicates\).

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
3.  Call updateSegment with only configuration: \{ duration: '120', show\_timer: true \} &amp;\#8212; no wrap\_up\_code, notes, or confirmed\_on.
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

 PRB2026678

</td><td>

Dynamic wrap-up timer update on the UI when a call has ended

</td><td>

Agents should have the wrap-up timer updated automatically when CCaaS provides the wrap-up context after a call has ended. The wrap-up modal should be refreshed automatically without intervention. The wrap-up modal shouldn't require users to close or open to have the timer count down.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2030602

</td><td>

The error 'TypeError: Cannot read properties of undefined \(reading 'output'\)' occurs in the Console Browser

</td><td>

 

</td><td>

1.  Navigate to Service Operations Workspace.
2.  Open an Incident record from the List menu.

 Observe error message, TypeError: Cannot read properties of undefined \(reading 'output'\) in Browser Console,' on the initial load of record.

</td></tr><tr><td>

Agent Chat

 PRB2033778

</td><td>

Dynamic wrap-up timer update on UI when call ended

</td><td>

Wrap-up dialog does not close in other tabs when submitted in one tab. The timer does not reset on configuration refresh.

</td><td>

1.  Open the same active phone interaction in two browser tabs \(Tab A and Tab B\).
2.  Wait for the wrap-up dialog to appear in both tabs.
3.  Submit wrap-up in Tab A \(fill in notes/code and select **Submit**\).
4.  Observe Tab B.

 Expected behavior: Wrap-up dialog in Tab B closes automatically.

 Actual behavior: Tab B continues showing the open wrap-up dialog.

</td></tr><tr><td>

Agent Chat

 PRB2050363

</td><td>

Incorrect and inconsistent heading hierarchy in ServiceNow flow

</td><td>

Users who rely on screen readers to navigate via headings are unable to get an overview of the 'Inbox' section. The lack of a clear hierarchy makes the content feel disconnected from the rest of the page, leading to confusion and increased cognitive load when trying to locate specific information.

</td><td>

1.  Open the SOW home page.
2.  Navigate to the 'Inbox' section using the tab key.
3.  Enable VoiceOver on macOS and use the rotor or heading shortcut to navigate.

Observe that it only identifies H4 and H5.

4.  Enable ChromeVox on ChromeOS and try to navigate by heading using the 'H' key.

 Observe that ChromeVox fails to identify any headings in this section.

</td></tr><tr><td>

Agile Development

 PRB2022589

</td><td>

Add 'None' as a choice to the **rm\_epic.status** field and make it the default for new epics

</td><td>

The **Epic Status \(rm\_epic.status\)** field currently doesn't include a 'No status' option, which prevents epics from having an unset/neutral status. This causes ambiguity in reporting and makes it difficult to distinguish between epics that have not yet been assigned a status versus those intentionally marked as green, yellow, or red.

</td><td>

1.  Navigate to **Agile Development** &gt; **Epics** \(or open an Epic from a board/backlog\).
2.  Open any active Epic record
3.  Select the **Status** field.

 Expected behavior: 'No status' is available as a selectable option to represent epics with no status assigned, enabling accurate status transition tracking for usage analytics.

 Actual behavior: 'No status' isn't available as an option in the **Status** field choice list. Available options are limited to green, yellow, and red.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2011068

</td><td>

Data to Glide from offGlide isn't getting logged with the actual user

</td><td>

Any record update or creation doesn't have the created\_by or updated\_by set as the actual user.

</td><td>

Make a set cache call to Glide from offGlide.

 Observe that any record update or creation doesn't have the created\_by or updated\_by set as the actual user.

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

The OffGlideScriptObject.generateAuthorizationInfo API creates JSON Web Tokens \(JWT\) with current session users

</td><td>

The API sn\_cs\_offglide.OffGlideScriptObject.generateAuthorizationInfo\(\) creates JWT with current user sessions, even though the userID value is passed in the request.

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

An instance isn't invoking DARE calls due to new properties not being allow listed in the cache configuration's invalidation script

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

 PRB2024169

</td><td>

widget\_translations REST endpoint case-sensitive lookup misses lowercase-stored translations

</td><td>

The widget\_translations REST endpoint performs a case-sensitive match between widget required\_translations keys and sys\_ui\_message records. When a translation exists in sys\_ui\_message but is stored with different casing \(for example, lowercase message column vs mixed-case required\_translations key, or vice versa\), the aggregator returns no translation for that key and the widget renders the source string instead of the translated value.

</td><td>

1.  Create a sys\_ui\_message record with a lowercase message key \('submit'\).
2.  Reference the same key with different casing \('Submit'\) in a widget's **required\_translations** field.
3.  Call the widget\_translations REST endpoint with pageID and lang.

 Expected behavior: Lookup should be case-insensitive \(or normalization should be applied consistently on both sides\) so that the translation is returned.

 Actual behavior: The response is missing the entry for 'Submit' even though a translation exists in sys\_ui\_message under 'submit'.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2024430

</td><td>

AIX widgets POST to /api/now/aix\_kit/widget/id on every mount even when sys\_aix\_widget.script is the default empty IIFE

</td><td>

Every widget extending AIUXWidgetElement unconditionally calls this.server.update\(\) in connectedCallback. The default value of sys\_aix\_widget.script is an empty IIFE. Even when the user never modified that field, the client still fires a POST to /api/now/aix\_kit/widget/widgetId, which lands in WidgetRestService.handleUpdatesFromWidget and runs the no-op script through Rhino via WidgetScriptEngine.execute. This results in one wasted network round-trip and one wasted script-engine evaluation per widget mount, scaling with the number of widgets on a page. Widgets with no-op server scripts should not trigger the on-mount POST.

</td><td>

1.  Load any AIX experience page containing widgets whose server script has not been customized \(for example, shipped widgets in com.snc.ai\_experience\_components\).
2.  Open the 'DevTools Network' tab.
3.  Filter for aix\_kit/widget.

 Observe one POST per widget mount, each returning \{ 'result': \{ 'data': \{\} \} \}.

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

Observe that the chat works correctly.


 Expected behavior: chatEnabled is fetched successfully regardless of the user role.

 Actual behavior: glideRecord\_query evaluates ACLs and denies non-admin users read access to the deployment channel table.

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

 PRB2034740

</td><td>

aiux\_service/chat\_check\_access should work with the default experience name to query the deployment document id

</td><td>

There should be a way to query by experience name so that there is no need to force pass a sys\_id each time.

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

Move the **Component** and **source\_browser\_code** fields from sys\_ux\_widget to sys\_aix\_widget dictionary

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2020989

</td><td>

Performance and EVAM-related debug messages no longer appear in sys log for asynchronous GRs and Virtual Agent searches

</td><td>

When the system properties 'glide.search.performance.logger.enabled' or 'glide.search.evam.logger.enabled' are set to true, messages should appear in the sys log prefaced with '\[SEARCH PERFORMANCE\]' or '\[SEARCH EVAM\]' respectively. However, these messages no longer appear in the syslog when a conversation is part of the logging context.

</td><td>

1.  Open an instance that returned a synthesized response in portal \(for example, Dynamic Window setup\).
2.  Create and set glide.search.evam.logger.enabled to true.
3.  Perform a search that returns a synthesized response in portal.
4.  Open the sys log and search for recent messages containing 'for Genius Result with table'.

 Expected behavior: Log entry in sys log specifying the ID of the view configuration that was used for each genius result.

 Actual behavior: No log entries for GR EVAM View configuration selection.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2028353

</td><td>

Deprecate 'ServiceNow RAG \(Deprecated\)' resource options from NASK Tool UI dropdown list

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1935844

</td><td>

Asynchronous Framework should hold GRs until client is ready to receive them

</td><td>

The asynchronous GR payload can be missed depending on generation time.

</td><td>

1.  Open an AIS-enabled instance with asynchronous GRs set up.
2.  Navigate to the asynchronous GR amb processor.
3.  In 'Channel Subscribe Advanced Authorization', add the following at the top of the function: gs.sleep\(12000\); // 12 seconds.
4.  In portal, open the 'Network' tab.
5.  Filter by 'amb'.
6.  Search something that would bring up an asynchronous GR.

 Notice that the AMB subscription eventually succeeds, but the asynchronous GR payload can be missed if it takes less than 10 seconds to generate.

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

Analytics Data API

 PRB1974037

</td><td>

Visualization displays outdated dates when 'Use current date for period end' is selected for Platform Analytics

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

The PDF export of the inline dashboard gives a blank page with only the word 'Loading' in it

</td><td>

The exported PDF for any of the 0iInline dashboards is blank and shows the loading symbol only in the PDF, and not in the actual report of the dashboard. Also, exporting a dashboard stays in the 'Export request in progress' state for a very long time even on a very simple one-widget dashboard.

</td><td>

 

</td></tr><tr><td>

Analytics Export API

 PRB2019161

</td><td>

The **Export** option is not working for sub domain dashboards

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
9.  Select **Export to Powerpoint or pdf** .

 Notice the error, 'Export failed. Please contact your system administrator.' There is also an error is displayed in the error logs, 'ExportJobExecutor \*\*\* ERROR \*\*\* EXPORT\_JOB\_EXECUTOR: PEJ0001007 AttachmentID is null, attachment was not saved properly.'

</td></tr><tr><td>

Application Manager

 PRB2057729

 [KB3140027](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3140027)

</td><td>

Users can't publish custom-scoped applications after upgrading to Zurich or Australia

</td><td>

After upgrading to Zurich or Australia, users can't publish new application versions to scoped apps. Selecting the **Publish** button on any custom applications in ServiceNow studio results in a pop-up with the error 'Alert level: Critical. Vendor information was not found, upload function is disabled for this instance'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

App Shells

 PRB2005043

</td><td>

Some items are hidden behind the company logo in the Next Experience navigation bar

</td><td>

Sometimes the Next Experience navigation isn't rendered correctly. The 'All' and 'Favorites' items are displayed behind the ServiceNow logo. The issue is happening is randomly for some tests and does not have a fixed reproducible behavior. The menu items should always be rendered correctly and must be selectable.

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
5.  Select the three questions as a KBA authentication factor.
6.  Call the voice agent.
7.  Authenticate a user.
8.  Navigate to the syslog table.

 Observe that the kba\_session\_context value for the third question is logged in this format: '\{q1\_keyword=q1\_user\_input, q2\_keyword=q2\_user\_input\}'. It should be logged in a standard JSON format.

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
3.  Select any question with the type, 'Identification/Authentication'.
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

Canonicalization Data Services \(CDS\)

 PRB2036615

</td><td>

Implement server side filtering to improve experiment targeting of user instances

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1937698

</td><td>

The user gets a RCA error when trying to create ds\_document and a version with an attachment

</td><td>

The status is wrong for the RCA privilege.

</td><td>

 

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

 Notice that it throws the RCA error, 'Read operation on table 'sn\_hr\_core\_case\_operations' from scope 'Employee Slate Core' was denied. The application 'Human Resources: Core' must declare a Restricted Caller Access privilege. Please contact the application admin to update their access requests.'

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

CMDB Identification and Reconciliation

 PRB1952085

</td><td>

Dependent items are inserted regardless of the parent or the main CI insertion failure

</td><td>

Configuration items and their relationships should not be created.

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
4.  Create a new moderation filter or use the existing filter.
5.  Add any Japanese keyword in the filter.
6.  Add any English keyword in the filter.
7.  Save it.
8.  Log in to community portal as any community user1 with the preferred language set to Japanese.
9.  Try to post content with the keyword used in step 5.
10. Log in to community portal as any community user1 with the preferred language set to English.
11. Try to post content with the keyword used in step 6.

 Expected behavior: The user is prevented from using banned keywords during content posting. The appropriate message appears.

 Actual behavior: 'Moderation Banned Keyword Filter' doesn't work for characters in other languages. The user is allowed to post content with the banned keyword if the keyword is not in English.

</td></tr><tr><td>

Condition Builder in Workspace

 PRB2011310

</td><td>

The **SLA** field is read-only in a related condition when creating a list in Workspace

</td><td>

The **SLA** field and the operator should not become read-only.

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


 Expected behavior: The **SLA** field should not become read-only.

 Actual behavior: The **SLA** field is read-only.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1926784

</td><td>

Skip invalid tables from health score calculation of CMDB health group

</td><td>

The group score calculation errors out for invalid tables.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1956449

</td><td>

A CMDB data certification task in the 'Data Certification' dashboard displays inconsistent data on the 'Review not completed' tab

</td><td>

In the CMDB 'Data Certification' dashboard, the 'Review not completed' tab displays a count of pending records, but no records appear in the list. Users also can't submit the certification task, even after completing the review.

</td><td>

1.  Navigate to CMDB Workspace.
2.  Create a Data Certification policy on any table.
3.  Execute it.
4.  Open a Data Certification task.
5.  Navigate to the 'Review Records' page.
6.  Create an archive.
7.  Archive one or more records associated with that Data Certification task.
8.  Navigate back to the 'Review Records' page.

 Observe that the 'Review not completed' tab still includes the count of the records that were archived. Also, the user can't submit the task, even though all the records available are reviewed.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1992684

 [KB3005930](https://hi.service-now.com/kb_view.do?sysparm_article=KB3005930)

</td><td>

CMDB Query Builder with the system language set as Japanese displays empty results

</td><td>

There are missing values in queries when using Japanese. The French language can lead to errors.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2017567

 [KB3137554](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137554)

</td><td>

There is an infinite loop in PartialPayloadProcessor when the payload size limit is exceeded on the first record of a batch

</td><td>

Re-running the payload after changing the property 'glide.identification\_engine.partial\_processing\_max\_fetch\_memory\_mb' to zero causes the thread to be in an infinite loop.

</td><td>

1.  Run the payload to create a partial payload.
2.  Change the property to 'glide.identification\_engine.partial\_processing\_max\_fetch\_memory\_mb' to 0.
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

1.  Run the script to create a multi-source record.
2.  Manually add the **last\_discovered** value to col51 in the cmdb\_multisource\_data table for this record.
3.  Rerun the same payload with the same CI with updated short\_description.

 Observe that col51 is not updated with the latest time stamp.

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

During content updates in the ITAM Content Library, a large number of ais\_index events are generated for the sam\_sw\_product\_lifecycle \(SAM software lifecycle\) and sn\_hamp\_lifecycle\_definition \(HAM hardware lifecycle\) tables. These events appear in the event log. The excessive events are triggered because system metadata columns on the AI Search data sources for these two tables are missing the **no\_text\_index** field attribute. Without this attribute, the AI Search indexing engine includes these columns in the vector index.

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

.

</td><td>

1.  Ensure that an index already exists on an instance for the ColA.
2.  Create an index on: ColA, ColB, ColC, ColD.
3.  Verify that the redundant index check is dropping the index, causing 'AccessExclusiveLock' and slowness on the instance.

 Expected behavior: It should have been dropped concurrently so that there's no instance wide issue while dropping the index.

 Actual behavior: There's an instance wide issue due to the 'AccessExclusiveLock'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2031369

</td><td>

Quoted CTE identifiers cause 'com.glide.db.GlideSQLException: Invalid table name'

</td><td>

DBSqlParser.withItem \(line 1224\) stores CTE names with quotes. Everywhere else that checks for it uses unquoted names. The mismatch causes the parser to not recognize valid CTE names. The quoted CTE identifier throws 'com.glide.db.GlideSQLException: Invalid table name: cte\_name'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1974343

</td><td>

A query hint isn't including the change number and is causing the hint to be ignored

</td><td>

 

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

 PRB2022040

</td><td>

Knowledge Graph support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2023371

</td><td>

The 'NOT IN' operator isn't supported

</td><td>

 

</td><td>

 

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

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferable serialization of the query.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2026592

</td><td>

Inline node properties via withProperties\(\) are dropped on round-trip

</td><td>

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferable serialization of the query.

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

 Observe that StatsGatherer should collect stats, but isn't.

</td></tr><tr><td>

Data Management Console

 PRB2013605

</td><td>

The Statsgatherer job is finished with incomplete data

</td><td>

 

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

DirectSQL

 PRB2019852

</td><td>

SELECT \* must exclude columns that don't exist in the database

</td><td>

Select \* from a table that has a **Function** field, like cmdb\_data\_management\_policy, won't work because it's trying to find the function fields on the database. A filter should be added to exclude these fields.

</td><td>

 

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

Dynamic Guidance

 PRB2050926

</td><td>

There are unintended Dynamic Guidance steps in Unified Navigation Onboarding modal

</td><td>

The onboarding modal contains Dynamic Guidance steps.

</td><td>

1.  Open a Zurich or Australia instance with Now Assist enabled.
2.  Log in as a user with Now Assist enabled.
3.  On first-time log in, notice the onboarding modal.

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

Edge Encryption mass jobs \(such as mass-encrypt, mass-decrypt, key-rotation\) that process the audited **Journal** field history do not correctly handle instances where the 'sys\_audit' table has been rotated. When sys\_audit is rotated, the historical audit records no longer reside in sys\_audit itself but in one or more physical rotation tables \(for example, sys\_audit0 or sys\_audit1\). Because the job execution infrastructure previously hard-coded sys\_audit as the target table, all direct updates issued during job processing targeted the base sys\_audit table and found no matching records. This results in zero rows being updated for any encrypted field that lives exclusively in a rotated partition.

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

 Expected behavior: Edge encrypted data inside the **sys\_archive\_log.payload** field is decrypted by the job.

 Actual behavior: The scheduled encryption job does not have any execution records nor chunks, as it did not find any data to be decrypted.

</td></tr><tr><td>

Enhanced Content Editor \(ECE\)

 PRB2039917

</td><td>

Enhanced Content Editor \(ECE\) has an incorrect TinyMCE version as a dependency, impacting now-record-html-editor

</td><td>

This issue occurs in Zurich.

</td><td>

1.  Create any latest Zurich instance.
2.  Open Service Operations Workspace \(SOW\).
3.  Open any 'Incident' page.
4.  Check the Activity Stream.
5.  Open the 'Email' tab.
6.  Let the email body load.
7.  Once it is loaded, open the dev tools.
8.  Search for 'sn\_mentions'.
9.  Open the file with the source path, '/uxasset/externals/sn-tinymce/28.11.0/js/tinymce/plugins/sn\_mentions/plugin.min.js.jsdbx'.
10. Check that the content of the file is actually fetched from the file path.
11. Verify this by changing the content in the sys\_ux\_lib\_asset record.
12. Perform a hard reload.
13. Check the source code in the dev tools again.

 Notice that this console log is showing up in the file with path:' /uxasset/externals/sn-tinymce/28.11.0/js/tinymce/plugins/sn\_mentions/plugin.min.js.jsdbx.'

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

Experimentation Platform

 PRB2036613

</td><td>

Glide changes to support feature toggling and user criteria-based roll out in Experimentation Framework

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Experimentation Platform

 PRB2036614

</td><td>

Feature flagging under the feature preview program

</td><td>

This is a product update.

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

Field Service Capacity and Reservations Management \(Glide Family Channel\)

 PRB2028443

</td><td>

Capacity usage frequency is incorrect on the Daylight Savings day

</td><td>

This issue occurs for Daylight Savings Time \(DST\) timezones. The usage record shows two days, when it should only show one day.

</td><td>

1.  Create a Capacity Definition with 'Frequency: Daily'.
2.  Create a Capacity Assignment with the following:
    -   Capacity Definition: \(above definition\)
    -   Timezone: A DST-observing timezone \(for example, US/Eastern\)
    -   Effective dates for a DST transition \(for example, 2027-03-13 to 2027-03-17\)
3.  Create a Work Order Task \(WOT\).
4.  Assign it to an agent on the day immediately following the DST start \(2027-03-15\).
5.  Navigate to the **Capacity Usage** \(wm\_capacity\_usage\) table.

Observe the **start\_date\_time** and **end\_date\_time** fields for the newly created usage record.


 Expected behavior: The usage record should show exactly 1 day.

 Actual behavior: The usage record shows 2 days.

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

A query range error appears when querying on the filter present under '**Claim transactions** and **Receiving transactions**

</td><td>

Part of the query on sn\_bom\_transaction is ignored because of insufficient access for the 'query\_range' operation on sn\_bom\_transaction.details.

</td><td>

1.  Impersonate the sn\_bom\_payment.claim\_agent role.
2.  Navigate to **Workspaces** &gt; **Financial services workspace** &gt; **Claims** &gt; **All** &gt; **New** &gt; **Internal claim**.
3.  Fill in all the details and add multiple transactions into the fields **Claim transactions** and **Receiving transactions**.
4.  Save the form.
5.  Navigate to the related lists of 'Claim Transactions' and 'Receiving Transactions'.
6.  Select the **Filter** icon.
7.  Start querying on 'Sender transaction' &amp; 'Receiving transaction' respectively on both the related lists.

 Observe the error as mentioned above.

</td></tr><tr><td>

Flow Engine

 PRB1909705

</td><td>

A transform script for JDBC DSAs doesn't error out in engine major version v2

</td><td>

The issue can be reproduced when data stream actions are the same scope. The issue also occurs when the data stream actions are other than global and the script include is 'Global - Accessible to All Application Scopes'.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1967018

</td><td>

Instance outage and default semaphore exhaustion is caused by a long-running database query from the GlideElementWorkflow.queryStageState\(\) function

</td><td>

Querying the 'Stage' state of a workflow element causes a long-running query when an invalid ID is passed. There's a slow query executed against the database. This causes a lot of unnecessary data streaming across the network from the database to the application server. The application server may encounter an increase in garbage collection activities as it compacts/expands large RowBlock objects from memory to disk. The application server needs to do a lot of I/O to read and write and otherwise maintain the rowblock file on disk. The transaction response time is slower due to the large table handling. This can increase semaphore time and lead to contention and even semaphore exhaustion. In addition to all of the performance issues, this undoubtedly fetches incorrect results and potentially causes corruption.

</td><td>

Query the 'Stage' state of a workflow element which hasn't yet been saved.

 Expected behavior: The stage state should return null, quickly.

 Actual behavior: A large table handling warning is raised as it queries an excessive number of irrelevant stage\_state records and then returns an incorrect value.

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
    -   Playbook Experience Components \(servicenow-now-playbook-experience:29.2.2-SNAPSHOT\)
    -   Process Automation Designer \(sn-process-automation-designer:29.3.1-SNAPSHOT\)
    -   Customer Service Management Demo Data' \(Plugin id: com.snc.customerservice.demo\)
    -   Playbooks for Customer Service Management \(app-csm-playbook:6.4.0-SNAPSHOT\)
    -   app-csm-complaint-case:8.0.2-SNAPSHOT
    -   app-csm-complaint-case-ai-agents:1.1.2-SNAPSHOT
    -   app-csm-complaint-gen-ai:2.1.2-SNAPSHOT
2.  Impersonate the user 'Abel Tuter'.
3.  Navigate to **/csm**.
4.  Select the **Sparkle** icon to launch the virtual agent.
5.  Paste this prompt to the virtual agent to go through record creation: 'I want to log a complaint. My KNS-ULTRA1100 is over heating. The product becomes uncomfortably hot during normal operation, even with light usage. My colleague had also experienced the same issue with the product on their machine. It started happening 2 days ago'.
6.  Once the record has been created, impersonate the user 'Abraham Lincoln' on the platform.
7.  Find the created record.
8.  Keep selecting the **Continue** button to advance to the 'Research' stage.
9.  Select the **Use an AI agent** button.

 Notice that an error is shown to the user, and the execution plan is terminated with the message, 'You don't have the required access to complete this request. Try another request.'

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
7.  Navigate to **Navigator** &gt; **Remote instance** &gt; **Retrieved completed update set** &gt; **Commit**.
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

Remove the use of javascript prefixed reference qualifiers

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

Horizon Icon Component

 PRB2026750

</td><td>

A request for an icon in Zurich

</td><td>

Playbook Summarization features need the **document-template-ai-sparkle** icon in the Zurich release.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2023321

 [KB3025105](https://hi.service-now.com/kb_view.do?sysparm_article=KB3025105)

</td><td>

In HR Agent Workspace, an HR case can be cancelled without adding a work note, causing 'undefined' to be automatically logged in the conversation section

</td><td>

With the **Cancel** UI action \(sys\_ui\_action sys\_id 325370019f22120047a2d126c42e701d\), the workspace client\_script\_v2 unconditionally forwards the modal's **Work note** field to the server. When the field is left empty during case cancellation, GlideAjax.addparameter stringifies undefined to the string 'undefined' and forwards it to the server, which then persists it to work\_notes.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HTML Field Type Editor

 PRB2008555

</td><td>

The @mention and response template in HTML Editor does not appropriately respond to assistive technologies

</td><td>

The screen reader does not identify the dropdown list or the members of the list.

</td><td>

1.  Create an account on Assistiv Labs to use NVDA and JAWS.
2.  Open a base instance.
3.  Create or set the system property 'glide.ui.journal.use\_html' to 'true'.
4.  Navigate to **Service Operations Workspace**.
5.  Open any incident.
6.  Open a screen reader, such as VoiceOver and Safari or JAWS/NVDA and Chrome.
7.  Navigate to the **Comments/Work Notes** field.
8.  Enter '@' and a character or two for the user to invoke the dropdown list for user selection.

 Notice that neither screen reader identifies the pop-up, nor is there any identification of the members of the list as the user navigates it.

</td></tr><tr><td>

Identification and Reconciliation API

 PRB2029121

</td><td>

Help users determine whether dynamic Identification and Reconciliation Engine \(IRE\) should be turned on

</td><td>

This is a product update.

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

This issue was noticed in heap dumps

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

Install Base Management Store

 PRB2027486

</td><td>

Errors in CanRead path from ACL

</td><td>

Failures observed in Service Portal with latest changes in responsibility framework.

</td><td>

 

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

Key Management Framework \(KMF\) for Platform Encryption

 PRB2058369

 [KB3140571](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3140571)

</td><td>

Midserver is unable to fetch credentials after upgrading to Zurich or Australia

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

Nodes taking long time to load CryptoCore initialization during startup

</td><td>

It is observed that some nodes are taking an unusually long time during CryptoCore initialization at startup. A few nodes are taking anywhere between 15 minutes to up to 4 hours to complete CryptoCore initialization. Due to the large volume of logs, performing a full-day analysis in Splunk places additional load on the indexers. A subset of nodes were identified consistently exhibiting this behavior.

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

 PRB2027236

</td><td>

True-up for KC and NAKM, ECE, and KC in UI Builder

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2031464

</td><td>

The Knowledge Base Article \(KBA\) text is not visible in the workspace

</td><td>

This issue occurs with custom templates that contain fields of mixed data types like HTML, string, date.

</td><td>

1.  Create such a template with mixed data types.
2.  Create an article fill, and fill non-HTML fields as well.
3.  Insert a block in one of the fields.
4.  Save this article.
5.  Attempt to searching this article on 'SOW/CSM/KC'.
6.  Select the article

 Notice that it will open the kb\_view page of the article, and renders the article content as empty.

</td></tr><tr><td>

Knowledge Management

 PRB2038003

</td><td>

Updating versions for the base instance Knowledge Management apps to include Australia fixes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB1942195

</td><td>

HR Lifecycle Events resume cases are failing

</td><td>

The resume cases fail when trying to cancel and retrigger the HR activities.

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB2026077

</td><td>

Dependent activity sets are not getting triggered when completing activities after upgrade to Zurich

</td><td>

This occurs when upgrading from Yokohama to Zurich.

</td><td>

1.  Set up an instance in Yokohama.
2.  Create multiple LE cases and move them to ready state.
3.  Ensure sn\_hr\_le.use\_flow property is set to true.
4.  Upgrade to Zurich.
5.  Complete 'Pre-hire' activity set.

 Expected behavior: Pre-boarding activities should have created.

 Actual behavior: Pre-boarding activities are still in awaiting trigger.

</td></tr><tr><td>

List Administration

 PRB2003558

</td><td>

Users are unable to select 'presentational' variables when using the list selector to build out list configurations

</td><td>

 

</td><td>

1.  Verify that sn-list-selector has been updated to Version 26.0.0.
2.  Create a list visualization against the incident table.
3.  Select **Edit**.
4.  In the configuration panel in the 'Columns and rows' section, next to 'Columns', select **Add**.
5.  Scroll to 'Questions' and expand it.
6.  Scroll on the list of variables and look for 'Legal Section'.

 Observe that it can't be found. Users would like to be able to choose presentational variables as well, even if they don't contain any values.

</td></tr><tr><td>

MID Infrastructure

 PRB2039652

</td><td>

Issues with the migration UI

</td><td>

There is an issue with the 'Migration' page auto-refresh.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1978666

</td><td>

Users are unable to reset MID authentication from mutual authentication to basic authentication

</td><td>

When setting mutual authentication back to basic authentication using the same file, it results in an error: 'Error: The system cannot find the batch label specified - turnOffMutualAuth'.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1998489

</td><td>

Root Cause Analysis \(RCA\)/Cross Scope Access changes are causing the 'MAW' list and record declarative actions to be blocked from execution

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

MID Server shuts down unexpectedly during start up due to sorting/filtering logic mismatch in ECC queue record batching

</td><td>

During MID Server start up, the server retrieves ECC queue records in batches from the instance. A mismatch in the sorting and filtering logic causes some records to be missed, resulting in an empty response. This triggers a MIDServerInfoException: No 'sysIds' array is returned in the response error, causing the MID Server to shut down unexpectedly.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2034352

</td><td>

MID doesn't sync ECC firewall message audit data on shutdown, leading to audit data loss

</td><td>

If using the default 1 hour reporting interval, up to 1 hour of data could be lost if MID is restarted between reporting intervals.

</td><td>

1.  Start a MID Server - if desired, set the mid.ecc.queue.audit.report\_interval to the minimum value of 900 seconds \(15 minutes\).
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

 PRB2035293

</td><td>

Implement retries for signing endpoint on MID

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035295

</td><td>

Add new MID configuration parameters to support IPKI flow

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035298

</td><td>

Implement a IPKI certificate provisioning flow on MID

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035301

</td><td>

Validate a IPKI certificate chain on MID

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035302

</td><td>

Create an empty hosted plugin for the MID infrastructure app

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2035304

</td><td>

Add more validation to the KeystoreInstall API

</td><td>

This is a product update.

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
10. Validate that you see the parts associated with the WOT.

 Expected behavior: The new WOT appears in offline mode, and the related records created are present in the corresponding section and visible offline. Additionally, an incremental payload is generated for the new task and its related records \(entries in sys\_sg\_incremental\_result\).

 Actual behavior: The new WOT presents, but related records are missing in offline mode. For the newly created WOT, no new watcher record is created in sys\_rw\_action, so subsequent related record inserts are not tracked. Since no watcher exists for this WOT, no incremental payload parts are generated for its related records, so they never arrive in the device's offline cache.

</td></tr><tr><td>

Multi-Instance Framework

 PRB2032862

</td><td>

Multi-instance Framework \(MIF\) synchronous messaging

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2029156

</td><td>

Move MMS to GA

</td><td>

The MMS plugin name displays 'MAINT ONLY', and should be updated.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2039537

</td><td>

The 'Options' parameter is missing, causing the Vision agent pipeline to fail

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2039538

</td><td>

The sync service record is missing, causing an error in Mosaic

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2039539

</td><td>

The billing feature is not working

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1905386

</td><td>

When a custom Unified Navigation menu is created, the menu items added in the menu are duplicated in 'All'

</td><td>

The menu items are duplicated in 'All', and one appears as an application and the other appears as a favorite.

</td><td>

1.  Open an instance.
2.  Open the Unified Navigation menu.
3.  Create a new menu.
4.  Add menu items from the related list, such as 'Access Analyzer'.
5.  Refresh the page.
6.  Open 'All'.
7.  Search for Access Analyzer.

 Notice that it appears twice, and one is an application and the other is added as a favorite.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1971847

</td><td>

The default ServiceNow logo appears briefly in Next Experience before switching to the user's logo

</td><td>

The issue is happening only when users access one of the workspaces. It doesn't happen when accessing the Next Experience homepage URL. It also only occurs on a machine that is slow, with a poor performance/network.

</td><td>

1.  Update glide.product.image and glide.produce.image.light to a new iix image.
2.  Cache.do.
3.  Open Developer tools.
4.  Under network, turn off cache.
5.  Access /now/sow/home.

 Expected behavior: The custom logo should be loaded.

 Actual behavior: The default Next Experience logo is visible first and later updated to the custom logo.

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

Now Assist Panel

 PRB2003390

</td><td>

The **New Chat** button is disabled on Now Assist panel \(NAP\) when launched through AI Engagement Experience Layer \(AIEL\)

</td><td>

When an agentic workflow is triggered by a UI action in a workspace using AIEL with forceNewConversation set to 'true', NAP launches successfully with a new conversation session. However, the **New Chat** button remains persistently disabled throughout the session, preventing users from initiating additional conversations. Additionally, the name of the workflow at the top of NAP is not displayed and the conversation does not show up in the list of prior conversations.

</td><td>

1.  Trigger an agentic workflow using a UI action in a workspace to auto-launch NAP with forceNewConversation set to 'true'.
2.  Ensure NAP launches with the workflow triggered in a new conversation session.

Observe the state of the **New Chat** button in the NAP header.


 Expected behavior: The **New Chat** button is enabled, allowing users to start a new conversation.

 Actual behavior: The **New Chat** button is always disabled when NAP is launched through AIEL.

</td></tr><tr><td>

On-Call Scheduling

 PRB2030480

</td><td>

Wrapper global APIs for on call bulk upload utility

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2026081

</td><td>

There's a 100501 error with an asynchronous call

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2027496

</td><td>

The metric batch\_result.status is stuck at in\_progress and isSkillEvaluationRun\(\) doesn't recognize the conversational\_ai evaluation type

</td><td>

For conversational\_ai evaluation runs, metric-level batch\_result records are never updated to status=completed. This causes the evaluation dashboard to display zero scores for all the metrics, even though valid evaluation data exists in the sys\_one\_extend\_eval\_metric\_result and sys\_generative\_ai\_metric tables.

</td><td>

1.  Create a Conversational AI evaluation run \(AutoChat\) with metrics like conversation success, skill selection accuracy, and turn count.
2.  Wait for the evaluation to complete \(batch\_run\_task status = processed\).
3.  Query the metric-level batch\_result records.

Observe that all the metric batch\_result records have status=in\_progress instead of completed.

4.  Navigate to the evaluation dashboard.

 Observe that all the metric scores show as 0 because the Java API getCustomMetricScoresPerPrompt filters batch\_result.status!=in\_progress.

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

 PRB2036182

</td><td>

Avoid early exit for the guardian error and add a response in the GenAI log even if content is flagged

</td><td>

 

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

Performance Analytics

 PRB1963190

</td><td>

Drilldowns from Single Score visualizations with monthly aggregation redirect to the current month instead of the month that the data represents

</td><td>

Single Score data visualizations based on an indicator and that are configured with a metric using a monthly aggregation are displaying an incorrect month after drilling down into the indicator details. For example, after selecting the Single Score card configured with the indicator, the user is redirected to the 'KPI Details' page. This page displays the current month \(for example, November\) in the title, but the data shown in the score card corresponds to October, explicitly labeled as 'Data from October'.

</td><td>

1.  Create a Single Score data visualization.
2.  Add an indicator as the source.
3.  Add the visualization to a dashboard.
4.  Enter 'Editing' mode on the dashboard.
5.  Navigate to the 'Metric' section.
6.  Set 'Time Aggregation' to 'By Month \(AVG\)'.
7.  Select the **Single Score card** to drilldown into the 'Indicator Details' page.

 Notice that even though the Single Score card displays a title such as 'Data from October', the drilldown redirects the user to the current month, not the month for which the data was collected.

</td></tr><tr><td>

Performance Analytics

 PRB2015951

</td><td>

The indicator **Sparkle** icon shows on data visualizations saved to the library

</td><td>

The **Sparkle** icon on data visualizations based on indicators should not show for data visualizations that are not saved to the library. This is a caching issue.

</td><td>

Disable the following properties:

-   sn\_query\_gen.indicator.feature.enabled
-   sn\_pa\_ai\_canvas.indicator.feature.enabled
-   sn\_pa\_ai\_canvas.entry.visualization.enabled

 Expected behavior: The **Sparkle** icon should not show on any data visualization, and whether it's saved to the library or not is based on an indicator source.

 Actual behavior: Notice that the **Sparkle** icon on data visualizations based on indicators still show for data visualizations saved to the library. This is caused by analytics\_cache, which clears out every 24 hours.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1981675

</td><td>

The 'Calendar Data' API's changes aren't reflecting

</td><td>

 

</td><td>

Call ScriptableCalendarDataAPI from the script background.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2031905

</td><td>

Update the indicator scorecard support to Zurich

</td><td>

The dashboard should include the indicator scorecard widget in the AI dashboard summary.

</td><td>

1.  Log in to a Zurich instance.
2.  Validate AI dashboard summary preference in 'Dashboard settings' is not persisting after saving.

 Expected behavior: It should save.

 Actual behavior: It is not saving.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2056500

</td><td>

There is a Zboot error for an unresolved dependency for sn\_app\_analytics\_w

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1948555

</td><td>

Sys\_scripts have references to old fields, which throws errors when the dashboard is updated

</td><td>

The following error appears: 'GlideLogLogger Invalid query detected, stack trace below \[Unknown field time\_unit in table par\_dashboard\_user\_metadata\]'.

</td><td>

Update a dashboard.

 Observe the error in the business rule.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2000095

</td><td>

The Guided Tour does not populate route parameters for 'default' dashboards, which breaks the functionality

</td><td>

By default, when navigating to 'now/platform-analytics-workspace/dashboards' and selecting a dashboard, the system will set the last dashboard that was viewed as the default' dashboard. This dashboard will always be displayed when navigating to the same page until the user views a different dashboard, at which point, that dashboard will then become the 'default'. In addition to this, when creating a new guided tour using a URL, the system auto-creates a sys\_embedded\_tour\_guide record and uses the values from the URL to populate the **Context** and **Route parameters** fields. However, when a tour is created using the URL for a 'default' dashboard, no URL parameters are needed, and the system sets the 'Route parameter' value to empty \(\{\}\). If a user visits another dashboard, which will automatically set that dashboard as the 'default', the system attempts to run the same guided tour created for the previous default dashboard, and fails.

</td><td>

1.  Set a 'default' dashboard.
2.  Navigate to the URL: **now/platform-analytics-workspace/dashboards**.
3.  Navigate to any dashboard from the dropdown list menu, such as 'AI Agent Analytics'.
4.  Navigate back to the URL: **now/platform-analytics-workspace/dashboards**.
5.  Confirm the last dashboard viewed is the dashboard that is displayed on the page.
6.  Copy the URL to the dashboard that is displayed.
7.  Created a guided tour for the default dashboard.
8.  Confirm it works as expected.
9.  Navigate to **Guided Tour Designer** &gt; **Create Tour**.
10. Set the following values:
    -   Name: Any
    -   Tour Type: Workspaces \(select 'Paste URL'\)
    -   Roles: All
11. Create and publish the tour with example steps.
12. Navigate to **sys\_embedded\_tour\_guide.list**.
13. Open the record for the tour that was created.
14. Confirm that the context is 'now/platform-analytics-workspace/dashboards' and the 'Route parameters' value is empty \(\{\}\).
15. Navigate to **now/platform-analytics-workspace/dashboards**.
16. Confirm the default dashboard displays.
17. In the header, select the **Show help** icon.
18. Confirm the tour runs as expected.

Notice the issue.

19. Set a new 'default' dashboard, such as IT Agent Dashboard'.
20. Navigate to **now/platform-analytics-workspace/dashboards**.
21. Ensure it loads the new default dashboard.
22. In the header, select the **Show help**.
23. Confirm the tour launches.

 Notice the tour fails, or crashes. This is due to the tour targets elements on the previous default dashboard. Since no URL parameters were saved as it was the default, the system cannot locate those elements on the new default dashboard, causing the failures.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2019318

</td><td>

The 'hideNewMigratedDashboardModal' boolean is ignored in the **Preference** JSON field of the dashboard API whenever there is a broken filter component in the migrated dashboard

</td><td>

The 'Welcome to PAE' pop-up occurs every time the user launches the dashboard.

</td><td>

1.  Set the system property 'com.glide.par\_dashboards.hide\_new\_migrated\_dashboard\_modal' to '=true' for boolean true/false.
2.  Migrate a classic dashboard with a filter on the incident priority.
3.  After migration, edit the par\_dashboard\_widget record of that filter element to have a broken stored component entry which doesn't exist in the par\_component\_filter table.
4.  Open the migrated dashboard.

 Expected behavior: The user should not see the 'Welcome to PAE' pop-up.

 Actual behavior: The user sees it every time they launch this dashboard.

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

 PRB2031476

</td><td>

User can't configure filters on a **Table** field which is of type 'String'

</td><td>

The **short\_description** \(a string field\) can't be enabled.

</td><td>

1.  Create a filter.
2.  Select the source as 'Table' and the table name as 'Incident'.
3.  Try to enable **Short\_description** as the field.

 Expected behavior: **Short\_description** \(a string field\) is enabled for configuration.

 Actual behavior: It's not enabled.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2031858

</td><td>

Add the AI dashboard summary preference saving capability to Zurich

</td><td>

 

</td><td>

1.  Log in to a Zurich instance.
2.  Validate that the AI dashboard summary preference in the dashboard settings isn't persisting after saving.

 Observe that it should save.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1941846

</td><td>

The CoreUI reports are migrated without the bulk migration being triggered and activated

</td><td>

Once the report is opened from CoreUI, it's automatically migrated to the PAE pages. The CoreUI reports shouldn't be migrated if no migration was triggered.

</td><td>

1.  Open an upgraded instance.
2.  Open any CoreUI report.

 Observe that the report is automatically migrated to the PAE pages. The CoreUI reports shouldn't be migrated if no migration was triggered.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2009064

</td><td>

The calendar report event displays fields that are not migrated correctly for all tables

</td><td>

By default, the calendar report uses **Number** and **short\_description**, and the migration only supports this configuration. If the user creates custom **calendar\_elements**, it is not migrated.

</td><td>

1.  Navigate to the **sys\_dictionary** list.
2.  Find the Incident table in 'Attributes'.
3.  Add the new attribute calendar elements value, 'category; description'
4.  Create a calendar report on the Incident table.

Observe that events contain both the category and description instead of **Number** and **short\_description**.

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

Platform Licensing

 PRB2036351

</td><td>

True-up of SM and LE 6.4.3

</td><td>

This is a product update.

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

 PRB1972438

</td><td>

There's an incorrect roll up of costs in demand currency to demand and task breakdown levels

</td><td>

.

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
8.  Promote the catalog change update set that is auto-generated to utilize the 'Sample On-Demand Pipeline'.
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

 Expected behavior: Deployment occurs under 2.5 minutes.

 Actual behavior: Deployment takes 10.5 minutes.

</td></tr><tr><td>

Resource Management

 PRB2032582

</td><td>

After changing the schedule, and we perform edit, allocation dailies are not deleted on traditional resource plan

</td><td>

Bulk Extend using the using the **Extend** UI action from the list context menu is not working. The date input is not getting updated on the resource plans.

</td><td>

1.  Create a resource plan for a user with a default schedule.
2.  Update the user schedule to a 'MWF' schedule.
3.  Edit the allocation records.

 Notice that the 'Tue, Thu' hours are not being deleted.

</td></tr><tr><td>

Roles

 PRB2027465

</td><td>

Excessive user queries during 'role contains' insert/delete can cause increased upgrade times

</td><td>

There is also audit done in sys\_audit\_role table if glide.role\_management.v2.audit\_roles is true which can also increase upgrade time significantly.

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

Create a global family release plugin with pre-requisite and setup track/impact

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

Schedules

 PRB1868862

</td><td>

Changing glide.sys.time\_format from HH:MM:SS to HH:MM affects tasks with an end time of 23:59

</td><td>

An issue occurs in the blackout schedule when the ending hour is set to 23:59 and the glide.sys.time\_format is changed from HH:MM:SS to HH:MM.

</td><td>

1.  Make sure glide.sys.time\_format has the HH:MM format.
2.  Navigate to **All** &gt; **Blackout Schedules**.
3.  Create a new 'Blackout Schedule'.
4.  Create a new entry that's a few days long.
5.  Set the end time to 23:59.
6.  In the Blackout Schedule, locate the related link.
7.  Open **Show Schedule**.
8.  Open the calendar view.

 Observe that an additional day has been added.

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

 PRB2022176

</td><td>

The script name should be logged when a page title is unavailable in the 'Guarded Scripts' list entry

</td><td>

The page title can be empty in some cases, such as a scheduled job and probably more. It should become the script name if there isn't a page name that makes sense.

</td><td>

 

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

 PRB2035844

</td><td>

An apparent scope stack corruption leads to global code running under an app scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1931472

</td><td>

Memory usage is high with many tag-based services due to createSubLogger

</td><td>

The 'Populate Calculated Services' scheduled job causes high memory consumption. There's unbounded memory growth from com.snc.cmdb .logging.LoggerFactory. Loggers aren't cached and per-logger change-listeners are never de-registered.

</td><td>

 

</td></tr><tr><td>

ServiceNow MCP Server Security

 PRB2050682

</td><td>

The token claim and metadata endpoints reflect a static instance URL instead of instance host

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow Otto for Code

 PRB2056970

</td><td>

The sn\_now\_assist\_code app fails to autoUpgrade when upgrading Zurich

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2016794

</td><td>

Skip delete issue for 'Coalesce' tables

</td><td>

When a Fluent app defines a role, the SDK generates a new sys\_id. The existing ScopeConflictDetector keys off sys\_update\_name \(which encodes the sys\_id\), and finds nothing in sys\_metadata, so no conflict is flagged. The installer then coalesces onto the real global admin role by matching the **Name** field and silently overwrites its sys\_scope, stealing a system-owned record into the app's scope.

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

Duplicate sys\_update\_xml is created for views when uploaded via FluentXMLLoader.

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

1.  On a target instance, confirm that the **task.priority** field has base system choices \(for example, 1 - Critical, 2 - High, 3 - Moderate, 4 - Low, 5 - Planning\)
2.  Using the ServiceNow SDK, create a scoped app that defines a ChoiceSet for **task.priority** with only a subset of choices \(for example, only values 1, 2, and 3\).
3.  Build the app using now-sdk build.
4.  Install the built app on the target instance.
5.  After installation, inspect the choices for **task.priority**.

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

1.  Create a configuration project.
2.  Customize and upload the changes.

 Expected behavior: the updateset contains DB serialized XML.

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

The issue is caused by the maximum allowed size for a zipped scripted REST request body, which is default set to 1MB.

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

 PRB2021450

</td><td>

The **Add Lifecycle Data** table UI action for the lifecycle playbook is incorrectly available in Zurich

</td><td>

The **Add Lifecycle Data** button is available for Zurich users, despite it being an Australia feature. When the user selects the button, nothing happens.

</td><td>

1.  Provision an instance with version 10.0.1 or 10.0.2 of the app-sam-workspace store app.
2.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **Software asset analytics**.
3.  Select the 'Lifecycle Management' tab.
4.  Select a report result to drill down into any report.
5.  Select the **Add Lifecycle Data** button.

 Observe that nothing happens.

</td></tr><tr><td>

Software Asset Management Publisher Pack for Microsoft

 PRB1908686

 [KB2243700](https://hi.service-now.com/kb_view.do?sysparm_article=KB2243700)

</td><td>

Windows Os Server Pattern is failing at the extension section 'collect CAL info' with duplicate DUPLICATE\_RELATED\_PAYLOAD errors for samp\_user\_device\_license\_consumption

</td><td>

Windows Os Server Pattern did not update or populate the IP address for the host. In the payload, duplicate related items for the table 'msft\_ual\_user' in 'Collect CAL info' causes IRE issues.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management Publisher Pack for Oracle

 PRB2026881

</td><td>

Wallet authentication support for discovery patterns for Oracle on the Unix part of Software Asset Management plugin

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Entitlements

 PRB1937440

 [KB2514736](https://hi.service-now.com/kb_view.do?sysparm_article=KB2514736)

</td><td>

The **Agreement type** is not available for the license metric group

</td><td>

When using an import set for entitlements, the **Agreement Type**' field becomes mandatory. However, for the license metric group, an import errors occur because there is no agreement type available. As a result, the errors can't be resolved and the records can't be moved to the alm\_license table.

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

Suite Engine

 PRB2026124

</td><td>

Software License Reconciliation is slow on Zurich, and there are SamSubscriptionSuiteEngine static nodes cache leaks across publishers, which inflate processAllocations per publisher

</td><td>

This is a performance issues. After upgrading to Zurich, scheduled Software License Reconciliation runs significantly longer than on the prior release, despite no material change in data volume. The slowdown to the 'Processing suites for the publisher' stage increased from 3 seconds to 73 seconds per publisher on average.

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

System Web Services

 PRB2034836

</td><td>

Telemetry for Action Fabric

</td><td>

This is a product update.

</td><td>

 

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

GCP 'p' attributes are not correctly formatted to receive trace scoped evaluator metrics from Traceloop

</td><td>

For Azure, the gen\_ai.provider.name 'p' attribute does not exist which prevents Traceloop from scoring the 'p' attributes.

</td><td>

Send traces from a GCP agent.

 Observe the scores in sn\_ai\_observe\_ai\_p are missing metrics from trace-scoped evaluators \(agent-goal-deviation, agent-system-prompt-leakage, privileged-access-detector, observed-access-detector\).

</td></tr><tr><td>

UI Field Administration

 PRB1916843

</td><td>

@mentions shortcuts don't work properly on the form's section

</td><td>

The issue occurs on Forms, but not on Activity Stream. It worked correctly in Yokohama.

</td><td>

 

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

When using the Safari web browser, there are certain conditions that result in text in a string field being cut off from displaying. These include the amount of text in the string field and the size of the web browser window. The result is a string field where the user has to click their cursor in and move down with the arrow keys to read all of the text in the string field.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2005816

</td><td>

The **Choice** field with 'none' doesn't appear intermittently

</td><td>

The **Choice** field with 'none' doesn't appear in some cases for some users and sets the value of the next sequence number by default.

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

Reduce DB load on sys\_ai\_record\_activity

</td><td>

 

</td><td>

1.  Enable AI Record Activity tracking \(glide.ai.field\_indicators.enabled\) on an instance with active AI Agent traffic.
2.  Drive normal insert/update/delete volume on non-system tables \(and AI writes to AI logging tables\).
3.  Observe sys\_query\_pattern / Splunk over a ~10h window.

 Expected behavior: Tracking imposes negligible background DB load.

 Actual behavior: ~288M queries/10h \(~8,000/sec\) against sys\_ai\_record\_activity and its 16 shards &amp;\#8212; \#3&amp;\#8211;4 DB load source on BT1. The queries are fast \(~0.31ms, indexed point lookups\) but the volume continuously consumes ~one full core.

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

 PRB1888357

</td><td>

Cannot invoke 'com.glide.sys.cache.CompactCacheEntry.getBytes\(\)' because 'entry' is null

</td><td>

A client-side error appears when the user loads or submits a large, complex form: 'form generation: java.lang.NullPointerException: Cannot invoke 'com.glide.sys.cache.CompactCacheEntry.getBytes\(\)' because 'entry' is null...'

</td><td>

1.  Log in to an instance.
2.  Open a large, complex form where the compressed \(LZ4\) HTML representation exceeds about 12.5 MB.
3.  To ensure the instance's form is not already in the DB-backed cache, clear the cache by navigating to **Cache Management** &gt; **Flush caches**.
4.  Load \(or submit\) the form from a browser or via an ATF test step.

Observe that GlideForm.putInCache\(\) is invoked, triggering DBCache.put\(\) for that form entry.


 Observe the client-side error on form load/submit: 'form generation: java.lang.NullPointerException: Cannot invoke 'com.glide.sys.cache.CompactCacheEntry.getBytes\(\)' because 'entry' is null...'

</td></tr><tr><td>

UI Form Administration

 PRB1971033

</td><td>

JavaScript's heapsize increases on the form page during an endurance test on ConfigWS

</td><td>

 

</td><td>

1.  Provision an instance with base Agent Workspace.
2.  Select the list.
3.  Select **All**.
4.  Open 5 incidents.
5.  Select each tab for each incident.
6.  Close all tabs.
7.  Repeat 2-4 for until test duration is complete \(250 mins\).

</td></tr><tr><td>

Upgrade Center

 PRB2040287

</td><td>

Auto-upgrade sn-managed applications on instances using periodic batch installs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB2040289

</td><td>

Auto-upgrade sn-managed applications changes on glide

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

1.  Open any workspace like Service Operations Workspace or HR Agent Workspace from the 'Workspaces' menu.
2.  Navigate to a list from the left tab panel.
3.  Select a few items to open a number of workspace tabs.
4.  Turn on the screen reader.
5.  Navigate on these tabs with forward \(tab key\) and backward \(shift + tab key\) navigation.
6.  Notice what the screen reader reads at workspace tab items and their **Remove** buttons.

 Expected behavior: The way workspace tabs and their **Remove** buttons are grouped into lists should be clear for screen reader users.

 Actual behavior: The way workspace tabs and their **Remove** buttons are grouped into lists is not clear for screen reader users.

</td></tr><tr><td>

UX Framework

 PRB2004013

</td><td>

Filters are not appearing in the dashboard

</td><td>

Filters are not appearing in the dashboard during the initial dashboard load.

</td><td>

1.  In cache.do, select **Clear Cache** and **Clear All Browser Caches**.
2.  Open a dashboard presenting multiple filters.

 Observe the filters are not loading.

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

1.  Navigate to **SOW**.
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

1.  Navigate to **Service Operations Workspace**.
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

1.  Navigate to a SOW base instance.
2.  Open 10 incident tabs.
3.  Close the 10 tabs.

 Observe that memory usage is high.

</td></tr><tr><td>

UX Framework

 PRB2029831

</td><td>

Release survey doesn't match the design

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

 PRB2039563

</td><td>

The workspace integration in the synchronization layer is missing in Zurich when aiux.experience is enabled

</td><td>

 

</td><td>

1.  Enable the 'aixu.experience' system property.
2.  Visit '/aiux/ui/workspace/now/sow/home'.

 Notice that the workspace should render in iFrame without L1, and the Polaris header navigation should work and be synchronized.

</td></tr><tr><td>

Virtual Agent

 PRB1999511

</td><td>

Message preview and unread badge count don't work upon page refresh

</td><td>

When the user refreshes the page, the message preview doesn't show up. On standard chat, there's also no unread badge count.

</td><td>

1.  Navigate to **/sp**.
2.  Query 'What is spam'.
3.  While standard or enhanced chat is processing, close the VA.

Observe that there is an unread badge count \(1\) and the message preview pops up.

4.  Refresh the page.

 Expected behavior: There is still an unread badge count and the message preview shows up.

 Actual behavior: The message preview doesn't show up. On standard chat, there's also no unread badge count.

</td></tr><tr><td>

Virtual Agent

 PRB2003424

</td><td>

External users are unable to delete closed chats from the Virtual Agent chat history

</td><td>

External users are unable to delete closed chats from the Virtual Agent chat history and encounter the error message: 'Failed to delete conversation. Please try again'.

</td><td>

1.  Impersonate an external user.
2.  Navigate to the ESC portal.
3.  Open the Virtual Agent chat history.
4.  Select the **Bin** icon to delete a closed chat.

 Notice that the error message appears: 'Failed to delete conversation. Please try again'.

</td></tr><tr><td>

Virtual Agent

 PRB2010886

</td><td>

A session expires in the middle of a conversation with the agent

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Impersonate an admin.
3.  Open Now Assist Portal.
4.  In the search bar, type 'Configure Internal AI search for Request for agent'.

Observe that an AI agent 'AI search Configuration agent' is invoked.

5.  Follow the agent.
6.  When asked to select the table name, scroll and select **Show more** 2-3 times.
7.  Try to select the table.

 Observe that the session is expired as the user tries to select the table and then is unable to log in and continue the conversation.

</td></tr><tr><td>

Virtual Agent

 PRB2013952

</td><td>

Remove the deprecate system property 'com.glide.cs.conversation.entity.cache.enabled'

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

 PRB2019099

</td><td>

Starting '\{0\}' sys\_cs\_context\_profile\_message isn't translated per user session language

</td><td>

The message should be translated using SysMessage.getMessageLang before it's sent.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2021983

</td><td>

Null GlideRecord in conversation context causes IllegalArgumentException during deserialization in TypedValueDeserializationUtil

</td><td>

TypedValueDeserializationUtil.get\(\) crashes with IllegalArgumentException when deserializing a null GlideRecord value stored in conversation context by the AI Search fallback topic.

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

When Virtual Agent invokes an AI search via FDIH \(global.async\_search\), a race condition in the callback handler can silently drop the search result if another thread updates the same conversation simultaneously. This leaves the conversation's task data in an incomplete state and the FDIH invocation started but never completed.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2024715

</td><td>

Asynchronous tool executions are stuck in processing

</td><td>

There's an error when getting tool execution context.

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

Observe that the generated content is sourced from the 'Missing Persons Standard Operating Procedure' attachment in the KB article.

4.  Open 'Sources and More', then hover over the source related to POL0021842-2.0 'Missing Persons Standard Operating Procedure.pdf'.

 Observe the link formation.

</td></tr><tr><td>

Virtual Agent

 PRB2031950

</td><td>

AI-user fetch issue

</td><td>

The conversation user for the ZTSD flow is AI L1 Service Desk Specialist, which is the identity type ai\_agent. The cache configuration get\_user\|table:\{table\}\|field:\{field\}\|value:\{value\} explicitly ignores users of type 'ai\_agent'.

</td><td>

Perform a cache fetch call for the cache key 'get\_user\|table:\{table\}\|field:\{field\}\|value:\{value\}' for any user of the identity type 'ai\_agent'.

 Notice that it doesn't return the **User** field value.

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

 PRB2034975

</td><td>

Interactions are throwing an error of 'technical issues' intermittently

</td><td>

A few interactions intermittently throw 'I'm having technical issues and won't be able to continue this conversation'.

</td><td>

1.  Ensure the following is installed:
    -   Now Assist in Virtual Agent Plugin: 15.0.8
    -   Now Assist in Virtual Agent Configurations: 8.0.8
    -   Generative AI Controller: 12.1.2
2.  Open a Zurich instance.
3.  In Now Assist Virtual Agent \(NAVA\), initiate a conversation.
4.  Impersonate an agent who is made available to take interactions.
5.  Initiate a live agent configuration.

 Observe the message, 'I'm having technical issues and won't be able to continue this conversation' occurs intermittently.

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

 PRB2037309

</td><td>

All auto chat conversations share the same conversation because the channel user profile reuse ignores channelUserId

</td><td>

All auto chat records reference the same conversation.

</td><td>

1.  Configure a channel with a provider application that supports bot-to-bot / auto chat conversations.
2.  Trigger multiple auto chat conversations for the same user on that channel, each with a unique channelUserId passed in the AI agent context.
3.  Wait for all auto chat executions to complete.
4.  Open the auto chat records and inspect the **Conversation** field on each record.

 Expected behavior: Each auto chat record has a unique conversation.

 Actual behavior: All auto chat records reference the same conversation, the one tied to the first channel user profile found for that user on that channel.

</td></tr><tr><td>

Virtual Agent

 PRB2038143

</td><td>

In order for users to adopt NAVA, OGCS should do parity with an onglide version of vaSystem.sendSkillPickerControl

</td><td>

This is a product update.

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
2.  Navigate to the /esc portal.
3.  Use the assistant to 'Order an iphone'.
4.  In the instance go to 'sys\_generative\_ai\_log.list' table and sort be recently created.
5.  Look for Unified planner response.

 The response should include is\_conversational as a parameter and no other parameter like 'conversational' should be included.

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

 Notice the error in the logs, 'Script evaluation error at \[topic\_Generate epics from capability\_applicability\] ReferenceError: 'vaContext' is not defined. \(sys\_cs\_topic.6db146b993f6f610b2f9f60f2603d678; line 9\)'.

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

 PRB2022914

</td><td>

A model is not displayed to the guest user informing them of the timeout or 403 failure

</td><td>

guest user session if timed out/ failing with a 403, no model is displayed to end user informing timeout

</td><td>

1.  Open a Zurich instance.
2.  Attempt to access Virtual Agent web client as guest user.
3.  Leave the chat open.

 Notice that after some time of inactivity, the logs display 'sync' calls failing with a 403, but a 'Session expire' message or any other timeout message is not displayed to the user. This results in Virtual Agent getting stuck.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2030686

</td><td>

The **Stop Flow** button is incorrectly displayed in the Virtual Agent **Input** field during file upload

</td><td>

The **Stop Flow** button should only be visible when a dynamic loader control is active, and it should not appear for normal file upload controls.

</td><td>

1.  Create a NLU topic with file upload.
2.  Open the topic in standard Virtual Agent chat.

 Observe the **Stop Flow** button in the bottom text **Input** field when the file upload control appears.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2032099

</td><td>

New chat contains messages from the old chat

</td><td>

If the user is on a chat and selects the **Plus \(+\)**button, it starts a new chat and shows the content of the previous chat as well.

</td><td>

1.  Start a new chat from NAVA.
2.  Transfer to a live agent.
3.  When the chat ends, immediately select the **+**button.

 Notice that the new chat shows messages from the previous closed chat.

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

Zero Copy Connectors \(Glide\)

 PRB2026100

</td><td>

There's a reverse tunnel solution for Trino private connectivity

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Zing Text Indexing and Search Engine

 PRB1982399

</td><td>

The **Choice** field is not indexed if there is no language configured for Zing

</td><td>

 

</td><td>

1.  Pick any table \(for example: ts\_index\_group\) that does not have any language configurations.
2.  Ensure the table has no text\_index\_translations attribute if the table has ts\_configuration record.
3.  Ensure the table or its parent table's columns doesn't have the attribute 'Text Search Index Language'.
4.  Add a **Choice** field to the table.
5.  Populate it with some choices and a default value.
6.  Re-index one record of the table.
7.  Dump the document.

 Expected behavior: The **Choice** field should be indexed.

 Actual behavior: The **Choice** field doesn't get indexed.

</td></tr></tbody>
</table>## Fixes included in Zurich Patch 11

These prior versions contain PRB fixes that are also included with Zurich Patch 11. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 10 Hotfix 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10-hf-2.md)
-   [Zurich Patch 10 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3104098)
-   [Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)
-   [Zurich Patch 9 Hotfix 4](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3108427)
-   [Zurich Patch 9 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3101238)
-   [Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)
-   [Zurich Patch 8 Hotfix 4](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3101281)
-   [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)
-   [Zurich Patch 7b Hotfix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3101108)
-   [Zurich Patch 7 Hotfix 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7-hf-3-PO.md)
-   [Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4 Hotfix 5b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3108431)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

## Store app versions included in Zurich Patch 11m

<table id="table_fh1_1gr_zjc"><thead><tr><th>

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

31.11.0

</td><td>

Defect with editor fix.

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

App Studio Commons

</td><td>

29.2.7

</td><td>

This app is a dependency of ServiceNow Studio + ServiceNow IDE. See the ServiceNow Studio + ServiceNow IDE listing for release notes.

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

Complaint Case AI Agents collection

</td><td>

1.4.3

</td><td>

Fixed: VA Channel for Intake Agents are now opt-in instead of enabled by default, allowing customers to configure them only when needed.

</td></tr><tr><td>

Content library portal

</td><td>

4.0.4

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

CRM Touchpoint

</td><td>

1.4.0

</td><td>

Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.

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

Document Intelligence for Contract Management Content Pack

</td><td>

1.5.0

</td><td>

Changed

 The default model provider for contract metadata extraction, contract analysis, and contract obligation extraction is Azure OpenAI.

</td></tr><tr><td>

Employee Center

</td><td>

41.0.3

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Employee Profile

</td><td>

13.6.9

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Employee Slate Core

</td><td>

2.0.5

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

1.1.5

</td><td>

This release provides the following features and enhancements:

 -   Enhanced Org chart and profile with visual updates and profile image edits.
-   Introduced an option to configure a custom AI insights skill.
-   Introduced Home page widget configuration from the admin console, starting with Quick links.
-   Improved performance and accessibility support.
-   Updated the approval checklist skill default settings to on-demand to support upgrades.

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

Group-Action Framework

</td><td>

7.1.1

</td><td>

New

 Enabling support Off-glide migration for GAF skills.

 Changed

 Updates to GAF clustering duration query to provide exact timestamp.

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

41.0.2

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Incident Management for Service Operations Workspace

</td><td>

7.1.5

</td><td>

Fixed

 Fixed an issue while adding interactions to incident by using GlideRecordSecure instead of GlideRecord.

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

ITOM UI internal components

</td><td>

27.4.16

</td><td>

Fixed: Avatar presence on the Specialist onboarding flow.

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

Knowledge Capabilities in UI Builder

</td><td>

29.11.2

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

Manage Invoice Operations

</td><td>

1.1.2

</td><td>

Fixed

 -   The Invoice case voice agent helper subflow now runs as the user who initiates the session.
-   The subflow has been assigned the interaction\_Agent and sn\_csm\_invoice.writer roles to maintain its ability to update work notes and create interaction-related records.

</td></tr><tr><td>

Manufacturing Commercial Operations AI agents collection

</td><td>

2.3.0

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

1.0.6

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

Now Assist for CPQ

</td><td>

1.0.5

</td><td>

Plugin names under Now Assist for CPQ were changed, but the parent container app \(app-now-assist-for-cpq\) was not re-released to reflect them. The name change was introduced in the parent app by Prankur. Without a release cut of the parent, the updated names will not reach the Store, and customers installing or upgrading the parent app will hit issues from the mismatch.

</td></tr><tr><td>

Now Assist for Creator

</td><td>

28.9.4

</td><td>

Please click on the individual dependent apps included with this package for detailed release note information.

</td></tr><tr><td>

Now Assist for Customer Service Management \(CSM\)

</td><td>

13.1.1

</td><td>

Changed

 -   New AI assets now default to third-party LLM providers with model version updates. Existing configurations using Now LLM Service stay unchanged, and the service remains available for manual selection.
-   Admins can view detailed information about each Now Assist skill to make faster and more informed decisions about enabling skill capabilities.

</td></tr><tr><td>

Now Assist for Enterprise Architecture \(EA\)

</td><td>

7.4.0

</td><td>

New

 -   Default AI model provider for the Now Assist for Enterprise Architecture skills changed from Now LLM to Azure Open AI.
-   Added support for third-party AI models: GPT-5.4 mini and Gemini 3.5 Flash.
-   Use the Enterprise Architecture query agent to ask natural language questions about your enterprise architecture portfolio. The agent supports multi-condition queries, quarterly trend comparisons, and impact analysis for scenarios such as application decommissioning, and suggests related questions after answering.
-   Generate a business process map \(BPM\) diagram in the Enterprise Modeling and amp; Visualization by uploading an image of an existing process diagram.

 Changed

 The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

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

12.0.1

</td><td>

New: Create a guided selling framework to enforce stage exit governance, and manage all deal-related actions from a uniﬁed opportunity workspace.

</td></tr><tr><td>

Opportunity Management Data Model

</td><td>

12.0.0

</td><td>

New: Introduced default OOB sales types and sales cycle stage values.

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

7.4.3

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

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

Recommended Actions for Security Operations

</td><td>

2.2.4

</td><td>

Changed

 Default model for the skill updated from Now LLM to 3P model.

</td></tr><tr><td>

Request Management for Service Operations Workspace

</td><td>

7.1.4

</td><td>

Fixed

 Fixed an issue while adding approvers to a request item by changing from GlideRecord to GlideRecordSecure.

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

Service Operations Workspace ITSM Applications

</td><td>

7.1.7

</td><td>

Fixed

 Fixed issues while adding interactions to incident and approvers to Request Item in respective related lists.

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

sn-app-analytics-center

</td><td>

7.4.3

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-chart-drilldown-configuration

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-component-builder

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-config-panel

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-create-dashboard-modal

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-dashboard-categories

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-data-visualization-wrapper

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-divider

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-dynamic-renderer

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-export-email-composer

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-export-modal

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-info-content

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-info-panel

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-insights-panel

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-saved-data-visualization

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-scheduled-export

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-share-dialog

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-app-par-components-share-info

</td><td>

7.4.5

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

sn-dashboard

</td><td>

7.4.4

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

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

7.4.2

</td><td>

Fixed

 -   Visualization configuration panel not opening in Dashboard edit mode.
-   Dragging and resizing widgets does not work in Platform Analytics plugin- v7.4.1.
-   Platform Analytics dashboard drilldown causes full page refresh in Service Operations Workspace, resulting in loss of unsaved work note.
-   Distinguish widget level properties from visualization level properties for saved visualizations in config panel.
-   Scheduled Export: Users receive an irrelevant error message \('Failed to save scheduled export. Please contact administrator'\) when clicking Save without entering mandatory fields.
-   Recent dashboard is not showing the recently used dashboard if its landed other than dropdown.
-   Migrated scheduled reports cannot be edited/deleted by the owner due to case sensitivity issue.
-   Dashboard library page - Card numbers are not visible in dark theme.
-   Dashboard/Data Visualization filters on date fields \(Created, Updated, Viewed\) are returning records from previous dates.
-   Hide Export button based on the export properties - Dashboard and Visualization Designer.
-   CTRL + Click does not open dashboards or visualizations in a new tab/window from Platform Analytics Dashboard or Visualization Library on Windows machines.
-   Content block shows up as following filter post migration.

</td></tr><tr><td>

Software Asset Management

</td><td>

3.2.8

</td><td>

Minor defect fixes related to reconciliation flow performance and lifecycle report.

</td></tr><tr><td>

Software Asset Workspace

</td><td>

10.0.16

</td><td>

In this version, the Software Asset Workspace includes the following fixes:

 -   Security fix for Multi Record Associator pop-up page.
-   Fixed incompatible script in 'SAM - Software Estate Weekly Job' PA Job.

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

8.0.4

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

8.0.6

</td><td>

Fixed

 -   Requests raised by a supplier contact from the Supplier Collaboration Portal now correctly transition to the 'New' state.
-   Contact invitation for a supplier from workspace and Supplier collaboration portal is fixed.
-   Default supplier catalog item shows list of suppliers.
-   Supplier filtering conditions accepted in document configs validated.
-   Resolved catalog item visibility issue while creating supplier task of action type- 'Complete a form'.

</td></tr><tr><td>

Unified Developer Core

</td><td>

29.2.7

</td><td>

This app is a dependency of ServiceNow Studio + ServiceNow IDE. See the ServiceNow Studio + ServiceNow IDE listing for release notes.

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
|@devsnc/behavior-uibtk-media|28.2.84|2025-12-11|
|@devsnc/behavior-uibtk-supporting-records|28.2.84|2025-12-11|
|@devsnc/library-uibtk-caching|28.2.84|2025-12-11|
|@devsnc/library-uibtk-commons|28.2.84|2025-12-11|
|@devsnc/library-uibtk-macroponent|28.2.84|2025-12-11|
|@devsnc/library-uibtk-screen|28.2.84|2025-12-11|
|@devsnc/library-uibtk-uxvalue|28.2.84|2025-12-11|
|@devsnc/library-uibtk-ux-value-resolver|28.2.84|2025-12-11|
|@devsnc/sn-customer-activity|28.0.5|2025-10-16|
|@devsnc/sn-customer-information|23.0.2|2025-05-01|
|@devsnc/sn-customer-information|23.0.2|2025-05-01|
|@devsnc/sn-customer-information|23.0.2|2025-05-01|
|@devsnc/sn-customer-information|23.0.2|2025-05-01|
|@devsnc/sn-devops-pipeline|21.0.5|2022-08-04|
|@devsnc/sn-feedback|2.0.0|2025-12-11|
|@devsnc/sn-help-setup|28.0.3|2025-07-31|
|@devsnc/sn-list-selector|26.1.3|2026-03-12|
|@devsnc/sn-par-calendar-connected|28.4.5|2026-05-05|
|@devsnc/sn-uibtk-actionable-list-item|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-builder-in-builder|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-client-state-config-panel|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-conditional-renderer|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-content-tree-picker|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-create-page|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-data-navigator|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-diff-renderer|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-domain-picker|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-draggable-dialog|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-draggable-list|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-editor-header|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-element-context-menu|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-element-navigator|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-element-properties-configuration-pane|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-events-pane|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-experience-assistant|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-extension-point-pane|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-features-catalog-modal|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-form-factor-controls|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-formula-builder|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-icon|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-instance-config-editor|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-is-hidden-property-input|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-json-navigator|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-loader|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-mcp-event-definitions-config-pane|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-mcp-props-config-pane|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-menu-elements|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-minimized-dialogs-dropdown|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-modal|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-param-row|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-placeholder|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-preset-pane|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-props-pane|28.2.86|2026-02-05|
|@devsnc/sn-uibtk-replace-component|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-scope-picker|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-script-config-panel|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-shelf-pane|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-site-map|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-stage-preview|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-stage-scale-controls|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-style-pane|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-style-provider|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-style-select|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-tabs|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-test-values-editor|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-text-link|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-toolbox|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-transaction-alert|28.2.84|2025-12-11|
|@devsnc/sn-uibtk-viewport-config-panel|28.2.84|2025-12-11|
|@devsnc/sn-vtb|25.6.2|2025-07-31|
|@devsnc/uibtk-api|28.2.85|2026-01-20|
|@devsnc/uibtk-uxf-assets|28.2.84|2025-12-11|
|@now-par-components/macroponent-provider|28.4.5|2026-05-05|
|@now-par-components/sn-par-additional-group-by|28.4.5|2026-05-05|
|@now-par-components/sn-par-breakdowns|28.4.5|2026-05-05|
|@now-par-components/sn-par-chart-size|28.4.5|2026-05-05|
|@now-par-components/sn-par-colors|28.4.5|2026-05-05|
|@now-par-components/sn-par-color-selector|28.4.5|2026-05-05|
|@now-par-components/sn-par-data-sources|28.4.5|2026-05-05|
|@now-par-components/sn-par-date-input|28.4.5|2026-05-05|
|@now-par-components/sn-par-dot-walk|28.4.5|2026-05-05|
|@now-par-components/sn-par-draggable-list|28.4.5|2026-05-05|
|@now-par-components/sn-par-duration-format|28.4.5|2026-05-05|
|@now-par-components/sn-par-filter-per-metric|28.4.5|2026-05-05|
|@now-par-components/sn-par-group-by|28.4.5|2026-05-05|
|@now-par-components/sn-par-metricbase|28.4.5|2026-05-05|
|@now-par-components/sn-par-metrics|28.4.5|2026-05-05|
|@now-par-components/sn-par-number-format|28.4.5|2026-05-05|
|@now-par-components/sn-par-pillar|28.4.5|2026-05-05|
|@now-par-components/sn-par-popover|28.4.5|2026-05-05|
|@now-par-components/sn-par-ranges|28.4.5|2026-05-05|
|@now-par-components/sn-par-refresh-frequency|28.4.5|2026-05-05|
|@now-par-components/sn-par-scorecard-aggregates|28.4.5|2026-05-05|
|@now-par-components/sn-par-scorecard-metrics|28.4.5|2026-05-05|
|@now-par-components/sn-par-toggle|28.4.5|2026-05-05|
|@now-par-components/sn-par-trend-by|28.4.5|2026-05-05|
|@now-par-components/sn-par-visualization-controls-section|28.4.5|2026-05-05|
|@now-par-components/sn-par-visualization-header|28.4.5|2026-05-05|
|@now-par-components/sn-par-widget-header|28.4.5|2026-05-05|
|@servicenow/now-score|28.4.5|2026-05-05|
|@servicenow/now-vis-bar|28.4.5|2026-05-05|
|@servicenow/now-vis-boxplot|28.4.5|2026-05-05|
|@servicenow/now-vis-dial|28.4.5|2026-05-05|
|@servicenow/now-vis-gauge|28.4.5|2026-05-05|
|@servicenow/now-vis-navigator|28.4.5|2026-05-05|
|@servicenow/now-vis-pie|28.4.5|2026-05-05|
|@servicenow/now-vis-sparkline|28.4.5|2026-05-05|
|@servicenow/now-vis-timeseries|28.4.5|2026-05-05|
|@servicenow/sn-builder-core|28.2.49|2026-01-20|
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
|@servicenow/sn-component-builder|28.2.43|2025-12-11|
|@servicenow/sn-controller-builder|28.2.15|2025-12-11|
|@servicenow/sn-preset-builder|28.2.12|2025-12-11|
|360 degree relationship visualization|22.0.0|2026-03-12|
|Access Analyzer|4.0.1|2025-01-30|
|Access Management Automation|2.1.0|2023-12-07|
|Access Management Flow Wizards|1.0.1|2021-09-16|
|Accounts Payable Invoice Processing|9.0.5|2025-05-01|
|Accounts Payable Invoice Processing|9.0.5|2025-05-01|
|Accounts Payable Invoice Processing|9.0.5|2025-05-01|
|Accounts Payable Operations integration with Document Intelligence|9.0.0|2025-05-01|
|Accounts Payable Operations integration with Document Intelligence|9.0.0|2025-05-01|
|Accounts Payable Operations integration with Document Intelligence|9.0.0|2025-05-01|
|ACL Assessment for Reports|3.1.2|2025-01-30|
|Admin Experience Framework|5.2.0|2025-12-11|
|Admin Workspace for Service Providers \(SPs\)|1.1.2|2025-05-01|
|Adobe Experience Platform Spoke|2.2.0|2025-01-02|
|Adobe Sign Activities for PAD|1.0.3|2023-01-12|
|Adobe Sign Spoke|2.6.0|2025-05-01|
|Advanced AI Search Management Tools|6.0.10|2025-01-30|
|Advanced Promotion Engine|4.2.0|2025-05-01|
|Advanced Recommended actions for ITSM|8.0.1|2025-05-01|
|Advanced Response Automation for Smart assessments|21.1.1|2025-12-11|
|Advanced Response Automation for Smart assessments|21.1.1|2025-12-11|
|Advanced Work Assignment for Legal Service Delivery|1.1.1|2025-06-05|
|Advanced Work Assignment for Source-to-Pay Operations|3.0.0|2025-05-01|
|Advanced Work Assignment for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Advanced Work Assignment for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Advanced Work Assignment for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Advanced Work Assignment for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Advanced Work Assignment for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Advanced Work Assignment for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Advanced Work Assignment for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Advanced Work Assignment for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|AES Application Object Templates|29.2.1|2026-06-16|
|AES Application Object Wizard Components|29.2.1|2026-06-16|
|AES Catalog Builder|27.2.3|2025-05-01|
|AES Catalog Builder|27.2.3|2025-05-01|
|AES Catalog Builder Wizard|27.2.3|2025-05-01|
|AES Catalog Builder Wizard|27.2.3|2025-05-01|
|AES Decision Table Builder Templates|4.0.0|2023-02-02|
|AES Decision Table Builder Wizard|4.0.0|2023-02-02|
|AES Flow Templates|27.2.3|2025-05-01|
|AES Flow Templates|27.2.3|2025-05-01|
|AES Flow Wizards|27.2.3|2025-05-01|
|AES Flow Wizards|27.2.3|2025-05-01|
|AES Mobile Templates|27.2.3|2025-05-01|
|AES Mobile Templates|27.2.3|2025-05-01|
|AES Mobile Wizards|27.2.3|2025-05-01|
|AES Mobile Wizards|27.2.3|2025-05-01|
|AES Notification Builder Component|27.2.3|2025-05-01|
|AES Notification Builder Component|27.2.3|2025-05-01|
|AES Portal UI Template|27.2.3|2025-05-01|
|AES Portal UI Template|27.2.3|2025-05-01|
|AES Role Builder|27.2.3|2025-05-01|
|AES Role Builder|27.2.3|2025-05-01|
|AES Role Builder Component|27.2.3|2025-05-01|
|AES Role Builder Component|27.2.3|2025-05-01|
|AES Table Builder Wizard|27.2.3|2025-05-01|
|AES Table Builder Wizard|27.2.3|2025-05-01|
|AES UI Template Wizards|27.2.3|2025-05-01|
|AES UI Template Wizards|27.2.3|2025-05-01|
|AES Workspace UI Template|27.2.3|2025-05-01|
|AES Workspace UI Template|27.2.3|2025-05-01|
|Agency Support Model|3.0.0|2026-06-16|
|Agent Client Collector for Investigation|7.1.0|2025-05-01|
|Agent Client Collector for Security Incident Response|20.2.0|2023-05-04|
|Agent Client Collector for Visibility Content|1.9.0|2026-06-16|
|Agent Client Collector Framework|6.5.1|2026-06-18|
|Agent Client Collector Log Analytics|3.8.9|2025-03-12|
|Agent Client Collector Monitoring|3.13.0|2025-01-30|
|Agent Client Collector Spoke|1.1.5|2024-01-04|
|Agent Forecast|5.7.1|2026-03-12|
|Agent-Initiated Messaging Interface|1.0.20|2025-12-11|
|Agent Messaging Component|3.0.12|2025-12-11|
|Agent Workspace for HR Case Management|4.0.2|2025-06-05|
|Agile Development v2|1.1.0|2023-02-02|
|Agile Integrations Common|1.2.3|2023-05-04|
|Aha! Spoke|1.7.0|2024-11-07|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for Customer Success Management|2.7.4|2026-06-16|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.1|2026-06-16|
|AI agents for SLO|2.0.3|2026-06-16|
|AI Agents for Workplace Service Delivery|3.3.1|2026-06-16|
|AI Agents Platform Usecase|1.0.5|2025-03-12|
|AI Asset Management|1.0.0|2025-05-01|
|AI Case Management|20.2.0|2025-06-05|
|AI Control Tower|1.0.1|2025-05-01|
|AI Discovery|2.0.4|2025-12-11|
|AIOps Dashboards|26.3.1|2026-06-16|
|AI Risk and Compliance Content|20.1.2|2025-05-01|
|AI Risk and Compliance Integration with Control Tower|20.1.2|2025-05-01|
|AI Risk and Compliance Management|20.2.0|2025-06-05|
|AI Search Admin Console|9.0.5|2026-06-16|
|AI Search for Customer Portals|1.0.5|2023-05-04|
|AI Search For Next Experience|4.1.1|2025-09-10|
|AI Search For Next Experience|4.1.1|2025-09-10|
|AI Search RAG|6.1.0|2026-06-16|
|AI Search Spoke|2.0.3|2023-09-20|
|AI Security and Privacy|4.1.3|2026-05-06|
|AI Websearch|4.1.0|2026-06-16|
|Aleph Alpha Spoke|1.0.2|2025-01-30|
|Alert Rules Management|18.15.9|2026-06-16|
|Amazon Alexa Spoke|1.1.0|2024-11-07|
|Amazon Bedrock Spoke|1.5.0|2026-06-16|
|Amazon CloudWatch Spoke|1.0.2|2022-12-01|
|Amazon Connect Spoke|1.2.0|2025-03-12|
|Amazon DynamoDB Spoke|1.0.1|2022-09-01|
|Amazon EBS Spoke|1.0.2|2023-09-20|
|Amazon EC2 Spoke|1.3.0|2025-03-12|
|Amazon Elastic Container Service Spoke|1.0.2|2023-09-07|
|Amazon RDS Spoke|1.0.5|2025-06-05|
|Amazon Route 53 Spoke|1.0.2|2022-12-01|
|Amazon S3 Spoke|1.2.1|2024-09-10|
|Amazon SNS Spoke|1.1.0|2023-09-07|
|Amazon SQS Spoke|1.0.1|2025-01-02|
|Amazon VPC Spoke|1.0.3|2023-09-07|
|Analytics Pack for Contract Management Pro|1.2.0|2025-05-01|
|Ansible Spoke|2.2.9|2024-12-05|
|API Insights|2.0.2|2025-06-05|
|API Service Graph Connector for Apigee X|2.0.1|2025-05-01|
|API Service Graph Connector for AWS API Gateway|2.0.0|2025-03-12|
|API Service Graph Connector for Azure API Management|2.1.0|2025-05-01|
|API Service Graph Connector for Kong Gateway|2.0.0|2025-04-03|
|App Best Practices Shared|27.2.1|2025-05-01|
|App Collaboration Component|27.2.3|2025-05-01|
|App Collaboration Component|27.2.3|2025-05-01|
|App Engine Management Center|27.2.1|2025-05-01|
|App Engine Notifications|29.2.1|2026-06-16|
|Application Insights|2.0.3|2021-11-18|
|Application Intake|27.2.3|2025-05-01|
|Application Intake|27.2.3|2025-05-01|
|Application Portfolio Management integration with Policy and Compliance|1.0.3|2023-05-04|
|Application Portfolio Management integration with Risk Management|1.0.2|2023-05-04|
|Application Service Extensions|1.1.7|2024-11-07|
|Application spoke selector|1.3.1|2025-12-11|
|Appointment calendar component|28.0.2|2025-07-31|
|Approvals Hub integration with Workday|1.0.9|2024-05-09|
|Approvals Hub integration with Workday|1.0.9|2024-05-09|
|Approvals Hub integration with Workday|1.0.9|2024-05-09|
|Approvals Hub integration with Workday|1.0.9|2024-05-09|
|Approvals Hub integration with Workday|1.0.9|2024-05-09|
|Approvals Hub integration with Workday|1.0.9|2024-05-09|
|Approvals Hub integration with Workday|1.0.9|2024-05-09|
|Approvals Hub integration with Workday|1.0.9|2024-05-09|
|App Summary|28.2.6|2025-12-11|
|ArcSight ESM Event Ingestion for Security Operations|10.4.17|2025-04-03|
|ArcSight Logger Integration for Security Operations|10.4.1|2024-11-07|
|Aria Systems Spoke|2.1.2|2023-04-06|
|Asana Spoke|1.0.3|2024-08-01|
|Asset Audits|1.0.0|2026-03-12|
|Asset Management Common|15.1.2|2026-06-16|
|Asset Management for mobile|26.4.1|2024-11-07|
|Asset Management for mobile|26.4.1|2024-11-07|
|Asset Management for mobile|26.4.1|2024-11-07|
|Asset Management for mobile|26.4.1|2024-11-07|
|Asset Management - Procurement Integration|1.0.1|2024-11-07|
|Asset Security Posture Management|5.3.4|2025-05-01|
|Asset Shipments|1.0.0|2026-03-12|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Atlassian Administration Spoke|1.0.1|2025-01-30|
|Atlassian Jira Integration for Agile Development|2.2.0|2024-11-07|
|Atlassian Jira Integrations Common|2.2.5|2025-01-30|
|Attribute Pack|4.0.1|2025-01-30|
|Attribute Pack|4.0.1|2025-01-30|
|Attribute propagation|9.4.0|2026-06-16|
|Attribute propagation|9.4.0|2026-06-16|
|Audio player component|23.0.0|2024-08-01|
|Authentication for conversational channels|1.0.2|2025-07-31|
|Automation Anywhere Spoke|1.2.1|2025-05-01|
|Automation Discovery|2.4.2|2024-01-04|
|AWH for AI Control Tower|2.0.9|2026-05-05|
|AWS Certificate Manager Spoke|1.0.1|2022-09-21|
|AWS CloudFormation Spoke|1.1.4|2024-03-20|
|AWS Elastic Beanstalk Spoke|1.0.3|2024-06-06|
|AWS Elastic Load Balancing Spoke|1.0.1|2022-09-01|
|AWS IAM Spoke|1.1.0|2023-07-06|
|AWS Lambda Spoke|1.1.3|2023-09-07|
|AWS OpsWorks Spoke|1.0.2|2023-09-20|
|AWS Translate Spoke|1.0.0|2022-11-03|
|Azure Active Directory User Mapping|1.10.5|2025-07-31|
|Basic Scoring for Smart Assessments|22.0.3|2026-03-12|
|BigFix Inventory Spoke|1.5.4|2023-09-07|
|Blue Prism Spoke|1.0.2|2022-09-21|
|BMC Remedy Spoke|1.4.1|2024-10-03|
|Bot Interconnect|1.4.1|2024-03-20|
|Box Spoke|3.3.0|2025-05-01|
|Breadcrumb navigation demo|27.0.0|2025-06-05|
|Breakdown Data Grid UI Component|1.4.0|2023-05-04|
|Broadcom Rally Integration with DevOps|7.0.0|2026-06-16|
|Bubble trend|1.0.0|2025-05-01|
|Business domain|21.1.0|2025-12-11|
|Business Location|4.2.0|2025-12-11|
|Business Location|4.2.0|2025-12-11|
|Business Portal|2.3.0|2026-03-12|
|Calendar component|26.0.1|2025-12-11|
|Calendly Spoke|1.2.0|2023-08-03|
|Capacity Management|3.0.0|2025-01-30|
|Capacity Management|3.0.0|2025-01-30|
|Career Assessment|3.1.0|2025-05-01|
|Career Conversations|3.5.3|2025-07-31|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Care Team Operations AI agent collection|2.0.1|2026-05-05|
|Care Team Portal|2.0.0|2025-07-31|
|Carousel component|27.0.2|2025-05-01|
|Case lines and workflows|4.3.0|2026-03-12|
|Case Management for Invoice Operations|1.8.0|2026-05-05|
|Case Playbook for Onboarding|8.0.1|2025-07-31|
|Case Playbook for Product Support|5.1.0|2023-11-02|
|Catalog Conversational Coverage|6.0.2|2026-05-05|
|CCG Content Pack|1.3.12|2024-11-07|
|CDM File Uploader|1.0.1|2023-11-02|
|Certificate Inventory and Management|3.6.3|2025-07-10|
|Change Management for Field Service|1.1.2|2025-01-02|
|Change Management for Service Operations Workspace|7.1.6|2025-12-11|
|Change Password Custom Component|1.2.0|2023-08-03|
|Channel Management|7.1.1|2026-03-12|
|Chat integration with Security Incident Management|1.2.5|2025-05-01|
|Chat Zoom Connector|1.0.6|2023-01-12|
|Checklist component|24.2.2|2025-03-12|
|Check Point Integration for Security Operations|10.4.3|2024-11-07|
|Cisco Webex Meetings Spoke|2.3.3|2024-08-01|
|Cisco Webex Teams Spoke|2.3.5|2024-11-07|
|Claim Common|1.0.0|2025-05-01|
|Client Software Distribution 2.0|1.2.3|2024-07-11|
|CLI Metadata|1.1.2|2021-04-15|
|Clone Admin Console|2.0.2|2025-09-10|
|Cloud Access Interface|1.0.8|2024-11-07|
|Cloud Action Library|1.4.0|2024-11-07|
|Cloud Configuration Governance|1.5.0|2024-11-07|
|Cloud Cost Management Infra Stack|8.2.2|2025-06-05|
|Cloud Deployment Automation|1.0.3|2024-12-05|
|Cloud Discovery Workspace|1.7.1|2025-05-01|
|Cloud Flow Wizards|1.2.1|2022-08-24|
|Cloudify Spoke|2.1.1|2023-04-06|
|Cloud Insights Billing|6.0.1|2024-04-04|
|Cloud Insights Billing|6.0.1|2024-04-04|
|Cloud Migration Assessment|1.4.0|2024-11-07|
|Cloud Security Posture Management|2.5.0|2024-02-01|
|Cloud Services Catalog|1.4.1|2025-07-10|
|Cloud Services Catalog Terraform Connector|1.8.0|2025-05-01|
|Cloud Spend Dashboard|1.0.3|2022-06-02|
|Cloud Storage|6.1.0|2026-03-12|
|Cloud Workspace|2.0.1|2025-05-01|
|CMDB and CSDM Data Foundations Dashboards|4.2.0|2025-12-11|
|CMDB Application for APIs and CLI|1.0.1|2021-07-22|
|CMDB CI Class Models|1.86.2|2026-06-16|
|CMDB Page Templates|3.2.6|2026-06-16|
|CMDB Workspace|9.2.0|2026-06-16|
|Coaching With Learning|5.4.2|2026-03-12|
|Coaching with Learning Migration Utility|1.0.1|2021-09-16|
|Collaboration applications - common|1.0.1|2023-05-04|
|Collaboration Request|27.2.3|2025-05-01|
|Collaboration Request|27.2.3|2025-05-01|
|Collaboration Services|3.11.1|2025-05-01|
|Collaboration Services for Service Operations Workspace|7.1.3|2025-12-11|
|Collaboration UI Component for Major Security Incident Management Workspace|1.2.1|2024-11-07|
|Collaborative Work Management|10.0.2|2026-06-16|
|Common AI Framework|1.0.1|2026-06-16|
|Common Guidances|14.0.0|2026-06-16|
|Common Service Delivery|11.6.1|2026-06-16|
|Common UIB Wrapper Components|1.5.1|2025-12-11|
|Common Vendor Core|4.4.0|2026-03-12|
|Compatibility Management|6.6.0|2026-06-16|
|Compatibility Management|6.6.0|2026-06-16|
|Configurable Workspace for Order Management|15.2.0|2026-06-16|
|Configurable Workspace for Order Management|15.2.0|2026-06-16|
|Configuration Compliance|15.3.4|2025-06-05|
|Configuration Data Management|5.0.2|2024-03-20|
|Configuration Hub|1.0.9|2025-12-11|
|Confluence Cloud Spoke|1.2.3|2025-03-12|
|Confluent Kafka REST Proxy Spoke|1.0.0|2021-03-11|
|Contact card component|25.2.4|2025-06-05|
|Contact Center Integration Core|1.1.0|2025-01-30|
|Contact Tracing|1.29.5|2024-11-07|
|Content Engagement for Employee Center Pro|1.4.0|2025-12-11|
|Content Experiences|32.2.1|2025-12-11|
|Content Publishing|36.1.6|2025-12-11|
|Context Menu Component for Configuration Data Management UI|1.2.1|2023-05-04|
|Context Rule Management|10.6.0|2026-06-16|
|Contract Management for Sales and Order Management|1.0.4|2025-01-30|
|Contract Management Pro|1.7.6|2026-06-16|
|Contract Management Pro for Legal Service Delivery|1.8.1|2025-07-10|
|Contracts and Entitlement Workflows|9.0.0|2025-05-01|
|Contracts Core|3.2.4|2026-06-16|
|Contracts Core components|1.5.1|2026-03-12|
|Conversational Analytics|9.1.2|2025-12-11|
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
|Conversational Appointment Booking|1.3.1|2024-05-09|
|Conversational Appointment Booking Components|2.0.5|2023-09-07|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Integration with Alexa|1.5.5|2024-08-01|
|Conversational Integration with Apple Messages for Business|1.1.7|2025-07-31|
|Conversational Integration with Facebook Messenger|3.0.8|2025-12-11|
|Conversational Integration with Google Business Messages|1.1.1|2024-02-01|
|Conversational Integration with LINE|2.0.7|2025-01-30|
|Conversational Integration with Microsoft Teams|10.3.0|2025-12-11|
|Conversational Integration with Slack|6.0.5|2025-12-11|
|Conversational Integration with WhatsApp \(powered by Twilio\)|2.0.10|2025-05-01|
|Conversational Integration with Workplace from Facebook|5.0.1|2025-01-30|
|Conversational Interfaces - Diagnostics|2.2.1|2024-11-07|
|Conversational IVR with Amazon Connect|1.6.0|2024-11-07|
|Conversational SMS Integration with AWS End User Messaging|1.0.2|2025-01-30|
|Conversational SMS Integration with Twilio|4.2.4|2025-12-11|
|Conversational SMS Service Channel|2.0.22|2025-12-11|
|Conversational subflows and actions|29.2.2|2026-04-09|
|Conversation Evaluator|3.0.4|2026-06-16|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.1.0|2026-06-16|
|Cornerstone Spoke|1.3.1|2024-09-10|
|Coupa Spoke|4.10.0|2025-05-01|
|COVID-19 Global Health Data Set|1.20.3|2024-05-09|
|Craft.co Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Craft.co Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Craft.co Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Craft.co Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Craft.co Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Craft.co Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Craft.co Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|Craft.co Integration for Supplier Lifecycle Operations|5.0.0|2026-06-16|
|Craft Spoke|1.0.0|2024-11-07|
|Creator Studio|27.2.3|2025-07-31|
|Credentials Core|1.1.0|2025-05-01|
|Credly Spoke|1.0.0|2025-01-30|
|CRM Flow Wizards|1.0.1|2023-04-06|
|CrowdStrike Falcon EDR Integration for Threat Intelligence Security Center|3.0.0|2024-11-07|
|CrowdStrike Falcon Host for Security Operations|10.4.5|2024-11-07|
|CrowdStrike Falcon Insight Integration for Security Operations|1.3.1|2025-05-01|
|CrowdStrike Falcon Sandbox Integration for Security Operations|11.0.10|2024-09-10|
|CrowdStrike Spoke|1.1.0|2025-01-30|
|CSC Content Pack|1.6.0|2025-05-01|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|CTO Voice AI Agents|2.0.1|2026-05-05|
|Custom App Record Summarization|29.2.2|2026-06-16|
|Customer Central|28.0.9|2025-10-16|
|Customer Contracts and Entitlements|13.0.0|2025-12-11|
|Customer Data Models for B2B2C|2.0.0|2025-01-30|
|Customer Life Cycle Management Self Service|1.0.0|2025-05-01|
|Customer Life Cycle Management Workflows|4.2.0|2025-05-01|
|Customer Service Case Types|3.0.2|2025-12-11|
|Customer Service Install Base Characteristics|2.3.0|2026-03-12|
|Customer Service Install Base Management|4.5.0|2026-03-12|
|Customer Service Portal|25.3.0|2026-03-12|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Customer Service with Service Portfolio Management \(SPM\)|2.0.1|2025-01-30|
|Cybersecurity Executive Dashboard|2.4.3|2025-05-01|
|Dashboard and visualization export|1.3.5|2026-01-20|
|Data Discovery|7.1.1|2025-12-11|
|Data Grid UI Component|26.0.7|2026-06-16|
|Data Loss Prevention Incident Response|2.1.21|2025-07-10|
|Data Model for Order Management|16.3.1|2026-06-16|
|Data Model for SBOM|4.0.0|2025-01-30|
|Data Privacy|7.0.0|2025-07-31|
|Data registry|21.1.0|2025-12-11|
|Data Relationships Framework|8.1.0|2025-05-01|
|Data visualizations|28.4.5|2026-05-05|
|Decision Builder|28.0.0|2025-07-31|
|Decision Table Builder|28.0.0|2025-07-31|
|Deployment Pipeline|29.2.1|2026-06-16|
|DevOps Change Health Scan Content Pack|6.0.1|2025-05-01|
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
|Diagram Builder|29.0.6|2025-12-11|
|Digital Experience Feedback Survey|4.3.0|2026-06-16|
|Digital Experience Score|4.3.0|2026-06-16|
|Digital Integration Management|1.6.0|2026-06-16|
|Digital Operational Resilience Management|20.1.1|2025-05-01|
|Digital Product Release|2.1.0|2025-05-01|
|Digital Product Release Data Model|2.1.0|2025-05-01|
|Digital Product Release Policy Content Pack|2.1.0|2025-05-01|
|Digital Product Release Workspace|2.1.0|2025-05-01|
|Digital Resilience Incident Reporting|20.2.0|2025-06-05|
|Digital Resilience Third-party Information Register|20.1.2|2025-05-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital signature component|27.0.3|2025-05-01|
|Discovery Admin Workspace|1.8.0|2025-05-01|
|Discovery and Service Mapping Patterns|1.27.0|2025-05-01|
|Dispute Content Pack for US Regulations|1.1.0|2025-03-12|
|Dispute Content Pack for US Regulations|1.1.0|2025-03-12|
|Dispute Content Pack for US Regulations|1.1.0|2025-03-12|
|Dispute Content Pack for US Regulations|1.1.0|2025-03-12|
|Dispute Content Pack for US Regulations|1.1.0|2025-03-12|
|Dispute Content Pack for US Regulations|1.1.0|2025-03-12|
|Dispute Rules Content Pack for Mastercard|2.3.0|2025-07-31|
|Dispute Rules Content Pack for Mastercard|2.3.0|2025-07-31|
|Dispute Rules Content Pack for Mastercard|2.3.0|2025-07-31|
|Dispute Rules Content Pack for Mastercard|2.3.0|2025-07-31|
|Dispute Rules Content Pack for Visa|5.3.0|2025-04-03|
|Dispute Rules Content Pack for Visa|5.3.0|2025-04-03|
|Dispute Rules Content Pack for Visa|5.3.0|2025-04-03|
|Dispute Rules Content Pack for Visa|5.3.0|2025-04-03|
|Dispute Rules Content Pack for Visa|5.3.0|2025-04-03|
|Dispute Rules Content Pack for Visa|5.3.0|2025-04-03|
|Dispute Rules Content Pack for Visa|5.3.0|2025-04-03|
|DLP Incident Response integration with ICAP|1.0.11|2025-06-05|
|DLP Incident Response integration with Microsoft|1.1.2|2025-07-10|
|DLP Incident Response integration with Netskope|1.0.18|2025-07-10|
|DLP Incident Response integration with Proofpoint|1.0.15|2025-05-01|
|DLP Incident Response integration with Symantec|1.1.21|2025-06-05|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Docker Spoke|2.3.3|2023-07-06|
|Document Approval App Template|27.2.3|2025-05-01|
|Document Approval App Template|27.2.3|2025-05-01|
|Document display component|27.0.0|2025-05-01|
|Document Flow Wizards|2.0.2|2022-09-21|
|Document Intelligence|8.0.6|2026-06-16|
|Document Intelligence Admin|4.0.3|2025-05-01|
|Document Intelligence for Accounts Payable Operations Content Pack|1.0.1|2025-05-01|
|Document Processor|1.6.0|2025-12-11|
|Document Service Framework for Google Drive|2.0.0|2025-05-01|
|Document Service Framework for OneDrive|2.1.1|2024-10-03|
|Document Template Integration with AdobeSign|1.6.6|2025-01-30|
|Document Template integration with DocuSign|1.6.3|2025-01-30|
|Document Templates|27.2.0|2026-06-16|
|DocuSign Activities for PAD|1.1.3|2023-01-12|
|Docusign eSignature Spoke|4.0.3|2025-07-10|
|Dropbox Business Spoke|1.0.5|2024-03-07|
|Dun and Bradstreet DirectPlus Spoke|1.0.0|2025-01-30|
|Dynamic Guidance|28.3.2|2026-06-16|
|Dynamic Related Records for Configurable Workspace|25.7.0|2026-06-16|
|Elasticsearch Integration for Security Operations|10.3.4|2024-11-07|
|Email Interaction Core|1.0.1|2025-05-01|
|Email Interaction for CSM|1.1.2|2025-09-12|
|Emergency Alert App Template|27.2.3|2025-05-01|
|Emergency Alert App Template|27.2.3|2025-05-01|
|Emergency Exposure Management|1.26.0|2024-11-07|
|Emergency Self Report|1.20.5|2024-05-09|
|Employee Center integration with Zoom|2.0.10|2024-05-09|
|Employee Center Pro|37.0.3|2025-12-11|
|Employee Experience Foundation|30.0.3|2025-12-11|
|Employee experience taxonomy|28.2.5|2025-12-11|
|Employee Experience VA Components|1.0.0|2023-08-03|
|Employee Goals|1.1.0|2025-05-01|
|Employee Health Screening|1.27.2|2024-11-07|
|Employee Readiness Core|1.40.3|2025-01-30|
|Employee Readiness Surveys|1.5.2|2022-11-03|
|Employee Travel Safety|1.20.2|2024-05-09|
|Engagement dashboard for AI Control Tower|3.0.11|2025-12-12|
|Engagement Messenger|5.10.1|2025-09-10|
|Enterprise Architecture Cloud Assessment|1.0.1|2025-01-30|
|Enterprise Architecture Workspace|9.1.0|2026-06-16|
|Enterprise Asset Management for Facilities|1.0.0|2024-08-01|
|Enterprise Asset Management for Healthcare|1.1.1|2025-01-30|
|Enterprise Modeling and Visualization|4.0.1|2025-06-05|
|Enterprise Modeling Common|3.3.2|2025-06-05|
|Enterprise Portfolio|1.2.1|2025-01-30|
|Enterprise Service Management Integrations Framework|3.8.2|2025-07-31|
|Entitlements Verification|6.0.0|2025-12-11|
|Equifax Spoke|1.0.0|2023-08-03|
|ER integration with NAVEX|1.1.1|2024-02-01|
|ERP Customization Mining|7.0.5|2025-05-01|
|ERP Integration Framework|15.16.7|2025-06-05|
|ESG integration with Concur|20.1.0|2025-05-01|
|ESG Risk Management|19.1.1|2024-11-07|
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
|Event Registration App Template|27.2.3|2025-05-01|
|Event Registration App Template|27.2.3|2025-05-01|
|Expanded Model and Asset Classes|2.16.0|2026-03-12|
|Expense Pre-Approval Template|27.2.3|2025-05-01|
|Expense Pre-Approval Template|27.2.3|2025-05-01|
|Export entities|3.3.1|2026-06-16|
|Export entities|3.3.1|2026-06-16|
|Export to PowerPoint|2.2.0|2024-08-01|
|Export to PowerPoint for Application Portfolio Management|1.0.1|2024-02-01|
|Export to PowerPoint for Strategic Portfolio Management|1.4.0|2024-08-01|
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
|External Content Connectors Web Crawler|3.0.26|2025-05-15|
|External Content Connectors Wordpress|7.0.7|2026-05-28|
|External Content Connectors Workday|7.0.7|2026-05-28|
|External Content Connectors Workvivo|7.0.7|2026-05-28|
|External Content Connectors Zendesk|7.0.7|2026-05-28|
|External Content Connectors Zoom|7.0.7|2026-05-28|
|External Credential Storage and Management Application|1.1.1|2025-05-01|
|External Legal Service Center|1.1.5|2025-07-31|
|F5 BIG-IP Spoke|1.2.0|2025-03-12|
|Fallout management|7.8.0|2026-06-16|
|Fallout management|7.8.0|2026-06-16|
|FDIH Dashboard|25.0.5|2024-11-07|
|Field Service Contractor for mobile|4.6.0|2025-07-31|
|Field Service Management AI agent collection|3.0.1|2026-06-16|
|Field Service Management for Telecommunications|1.1.0|2024-11-07|
|Field Service Management for Telecommunications|1.1.0|2024-11-07|
|Field Service Management Virtual Conferencing Integration|2.2.1|2025-01-02|
|Field Service Mobile Sidebar|1.0.3|2024-08-01|
|Field Service NLU Model for Virtual Agent Conversations|1.3.0|2025-07-31|
|Field Service Virtual Agent Conversations|1.7.0|2025-07-31|
|File Explorer Component for Security Operations|1.2.4|2024-11-07|
|File Explorer for Security Incident Response|1.2.3|2024-05-09|
|Finance Case Management|1.0.0|2025-05-01|
|Finance Common Architecture|12.0.1|2026-06-16|
|Finance Operations Workspace|1.0.0|2025-05-01|
|Financials Core|6.2.0|2026-06-16|
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
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Financial Services Operations AI agent collection|3.0.3|2025-12-11|
|Financial Services Operations Core|11.0.0|2025-12-11|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
|Financial Services Operations Integration with FRISS|1.2.1|2025-07-31|
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
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Operations Integration with Socure|1.1.3|2023-05-04|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Financial Services Remote Tables|1.4.0|2025-07-31|
|Firewall Audits and Reporting|1.7.0|2024-11-07|
|First Advantage Spoke|1.7.0|2024-11-07|
|Flow Designer - Designer|28.2.1|2025-12-19|
|Flow Designer GenAI|29.1.3|2026-03-12|
|Flow Diagramming|28.2.0|2025-12-11|
|Flow Generation|28.3.3|2026-03-12|
|Flow Summarization|28.3.4|2026-03-12|
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
|Forecast planning analysis|20.0.3|2025-01-30|
|Form data collector|2.0.0|2025-12-11|
|Form data collector|2.0.0|2025-12-11|
|Formula Builder|27.2.1|2025-05-01|
|Formula builder connected|21.1.0|2025-12-11|
|Fortify Application Vulnerability Integration|2.6.0|2025-05-01|
|FRISS Spoke|1.0.1|2025-07-31|
|FSM Configurable Dispatcher Workspace|28.1.1|2025-07-31|
|FSM Configurable Workspace|28.1.1|2025-07-31|
|FSM Scheduling AI Agent Collection|1.0.7|2026-06-16|
|Gantt UI Builder Component|26.1.1|2026-06-16|
|Geo Map component|1.2.0|2025-07-31|
|Gifts and Entertainment Compliance|1.2.1|2025-05-01|
|Github Application Vulnerability Integration|2.2.0|2025-06-05|
|GitHub Spoke|3.2.1|2025-07-10|
|GitLab Spoke|2.2.0|2024-11-07|
|Gmail Spoke|1.3.2|2024-09-10|
|Goal Framework|4.12.1|2026-04-09|
|Goal Framework for SPM|2.4.1|2025-05-01|
|Google Calendar Spoke|2.5.1|2025-06-05|
|Google Chat Spoke|1.1.1|2025-03-12|
|Google Cloud Datastore Spoke|1.0.3|2023-09-07|
|Google Cloud DNS Spoke|1.0.2|2022-09-01|
|Google Cloud Functions Spoke|1.0.3|2025-06-05|
|Google Cloud Load Balancer Spoke|1.0.2|2023-09-07|
|Google Cloud Pub Sub Spoke|1.0.4|2024-09-10|
|Google Cloud SQL Spoke|1.0.2|2023-09-07|
|Google Cloud Storage Spoke|1.0.4|2024-09-10|
|Google Cloud Translator Service Spoke|3.2.6|2025-05-01|
|Google Cloud Virtual Network Spoke|1.0.5|2023-09-07|
|Google Cloud VPC Access Spoke|1.0.1|2022-09-01|
|Google Compute Engine Spoke|1.0.5|2024-09-10|
|Google Directory Spoke|1.5.2|2024-10-03|
|Google Docs Spoke|1.2.0|2025-03-12|
|Google Drive Spoke|2.2.0|2025-05-01|
|Google Gemini Spoke|1.6.0|2026-03-12|
|Google Identity And Access Spoke|1.1.1|2022-09-01|
|Google Meet Spoke|1.0.0|2025-01-30|
|Google Persistent Disk Spoke|1.0.2|2022-09-01|
|Google Sheets Spoke|1.0.7|2023-09-20|
|Google Tasks Spoke|1.3.0|2025-05-01|
|GoTo Spoke|2.0.1|2021-08-19|
|GovNotify Spoke|1.1.0|2025-03-12|
|Grants Management Playbook|1.0.6|2025-07-31|
|GRC: Advanced Audit|20.2.0|2025-06-05|
|GRC: Advanced Core|20.2.0|2025-06-05|
|GRC: Advanced Dashboards|20.0.0|2025-01-30|
|GRC: Advanced Risk|20.2.1|2025-07-10|
|GRC: Approver Configurator|22.0.0|2026-03-12|
|GRC: Audit Management|20.2.0|2025-07-10|
|GRC: Audit Management Workspace|20.1.0|2025-05-01|
|GRC: Business Continuity Management - Components|7.1.0|2024-11-07|
|GRC: Business Continuity Management - Core|8.1.1|2025-05-01|
|GRC: Business Continuity Management User - Lite|5.0.1|2023-08-03|
|GRC: Business Continuity Planning|8.1.4|2025-07-10|
|GRC: Business Impact Analysis|8.1.2|2025-06-05|
|GRC: Business User - Lite|18.0.0|2024-02-01|
|GRC: Common Dashboard Elements|18.1.4|2024-06-06|
|GRC: Common Workspace Elements|22.0.4|2026-03-12|
|GRC: Compliance Assessment|21.1.0|2025-12-11|
|GRC: Compliance Case Management|20.2.0|2025-06-05|
|GRC: Compliance Management Workspace|20.1.2|2025-05-01|
|GRC: Compliance UCF|20.1.0|2025-05-01|
|GRC: Composite Entity|19.1.1|2024-11-07|
|GRC: Continuous Authorization and Monitoring|20.2.1|2025-07-10|
|GRC: Continuous Authorization and Monitoring Workspace|20.1.1|2025-05-01|
|GRC: Crisis Management|8.1.2|2025-06-05|
|GRC: Crisis Management integration with Everbridge Notifications|8.1.0|2025-06-05|
|GRC: Crisis Map|8.1.1|2025-05-01|
|GRC: Cyber Risk Institute|19.1.0|2024-11-07|
|GRC: Cybersecurity Controls Accelerator|18.1.0|2024-06-06|
|GRC: Entity Based Access|20.1.4|2025-05-01|
|GRC: integrations with third-party content|18.1.0|2024-06-06|
|GRC: Management Reporting|18.1.0|2024-06-06|
|GRC: Metrics|22.0.1|2026-03-12|
|GRC: Mobile|18.0.0|2024-02-01|
|GRC: NIST CSF Use Case Accelerator|20.1.1|2025-05-01|
|GRC: Operational Resilience|20.2.1|2025-07-10|
|GRC: Performance Analytics Premium Integration|19.1.0|2024-11-07|
|GRC: Policy and Compliance integrator|19.1.1|2024-11-07|
|GRC: Policy and Compliance Management|22.0.2|2026-03-12|
|GRC: Predictive Intelligence|20.1.0|2025-05-01|
|GRC: Privacy Case Management|20.2.2|2025-07-10|
|GRC: Privacy Lite User|19.0.0|2024-08-01|
|GRC: Privacy Management|20.2.1|2025-07-10|
|GRC: Profiles|22.0.2|2026-03-12|
|GRC: Regulatory Change Management|20.2.2|2025-06-05|
|GRC: Regulatory Change Management integration with RSS Feeds|20.1.1|2025-05-01|
|GRC: Risk Heatmap|21.1.1|2025-12-11|
|GRC: Risk Management|20.1.1|2025-05-01|
|GRC: Risk Management Workspace|20.1.1|2025-05-01|
|GRC: Risk Shared Common Components|22.0.1|2026-03-12|
|GRC: SIG Questionnaire Integration|20.1.1|2025-05-01|
|GRC: SOX Content Pack|16.0.2|2023-05-04|
|GRC: taxonomy management|21.1.0|2025-12-11|
|GRC: Technology Controls Monitoring Accelerator|18.1.0|2024-06-06|
|GRC: Vendor Portal|22.0.1|2026-03-12|
|GRC: Vendor Risk Management Workspace|22.0.3|2026-03-12|
|GRC: Virtual Agent|19.1.0|2024-11-07|
|GRC: Workbench|20.1.0|2025-05-01|
|GRC Case Management Core|20.2.2|2025-07-10|
|GRC Common GenAI|22.0.3|2026-03-12|
|GRC Compliance Case Management Advanced|18.1.1|2024-06-06|
|GRC Compliance Case Management Full Access|18.1.1|2024-06-06|
|GRC Employee User|19.0.1|2024-08-01|
|GRC Feature roles|22.0.1|2026-03-12|
|GRC integration with Thomson Reuters Regulatory Intelligence|20.1.1|2025-05-01|
|GRC Personal Data Rights|20.2.0|2025-06-05|
|GRC Privacy Case Management Integration with RadarFirst|20.1.1|2025-05-01|
|GRC Shared GenAI|22.2.0|2026-05-05|
|Guest Walk-up Experience for Customer Service|1.2.0|2025-05-01|
|Guidance|43.0.0|2026-06-16|
|Guided Decisions|35.0.1|2025-05-06|
|Guided Decisions Experience|36.0.1|2025-05-06|
|Guided Setup|5.0.4|2025-07-31|
|Guidewire Spoke|1.2.1|2025-07-31|
|Hardware Asset Management|15.0.2|2026-06-16|
|Hardware Asset Management for DaaS|12.0.0|2025-01-30|
|Hardware Asset Management for TNI|12.0.0|2025-01-30|
|Hardware Asset Management for Zero Touch Mobility|12.0.0|2025-01-30|
|Header App Shell|23.0.0|2023-06-01|
|Health and Safety Components|12.1.0|2026-06-16|
|Health and Safety Core|13.2.0|2026-06-16|
|Health and Safety Incident Management|13.2.0|2026-06-16|
|Health and Safety Incident Management OSHA Content Pack|9.0.0|2025-05-01|
|Health and Safety Incident Management OSHA Content Pack|9.0.0|2025-05-01|
|Health and Safety Incident Management OSHA Content Pack|9.0.0|2025-05-01|
|Health and Safety Incident Management PA Content Pack|10.1.0|2026-06-16|
|Health and Safety Testing|1.26.4|2024-05-09|
|Healthcare and Life Sciences Service Management Core|11.0.0|2025-07-31|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Operations Core|2.0.0|2025-07-31|
|Healthcare Professional Data Model|1.0.2|2025-05-01|
|Health dashboard for AI Control Tower|3.0.11|2025-12-12|
|Health Log Analytics|36.1.11|2025-07-10|
|Hiring Core|4.0.1|2025-05-01|
|Homepage deprecation help tool|2.0.2|2024-11-07|
|HR Flow Wizards|1.1.0|2022-05-05|
|HR License meter|1.0.3|2025-07-31|
|HR Multi Instance Integration Base|1.0.0|2025-01-30|
|HR Multi Instance Integration for Consumer|1.0.0|2025-01-30|
|HR Multi Instance Integration for Provider|1.0.0|2025-01-30|
|HRSD Process Mining Content Pack|6.0.0|2025-01-30|
|HR Service Delivery Advanced Integration with Oracle HCM|1.2.2|2025-05-01|
|HR Service Delivery Advanced Integration with Workday|2.2.2|2025-05-01|
|HR Service Delivery for Healthcare|1.0.4|2025-05-01|
|HR Service Delivery for Microsoft 365|3.5.0|2025-05-01|
|HR Service Delivery for mobile|21.2.7|2025-05-01|
|HR Service Delivery Integration with Cornerstone OnDemand|1.1.6|2025-05-01|
|HR Service Delivery integration with Oracle HCM|1.0.10|2024-11-07|
|HR Service Delivery Integration with Ultimate Kronos Group|2.0.6|2024-06-06|
|HR Service Delivery Integration with Workday|3.4.0|2025-05-01|
|HR Service Delivery NLU Model for Virtual Agent Conversations|22.2.0|2023-11-02|
|HR Service Delivery Portal UI Components|1.0.5|2024-05-09|
|HR Service Delivery Virtual Agent Conversations|24.2.8|2025-05-01|
|HR Success Dashboard indicators|1.0.15|2025-05-01|
|HR taxonomy|1.2.1|2022-12-01|
|HR Voice AI Agents|2.3.6|2026-06-16|
|HR Voice AI Agents|2.3.6|2026-06-16|
|Human Resources Service Delivery Integration with Workday Learning|1.3.0|2025-01-30|
|IBM License Compliance for Software Asset Management|6.0.3|2025-07-31|
|IBM QRadar Integration for Security Operations|10.3.7|2024-11-07|
|IBM QRadar Offense Ingestion for Security Operations|10.4.14|2024-11-07|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Idea Manager Dashboard|2.1.0|2024-08-01|
|iManage Spoke|1.1.3|2024-07-11|
|Impact|8.0.10|2026-06-16|
|Impact Common|8.0.7|2026-06-16|
|Impact Content|8.0.5|2026-06-16|
|Impact Health|1.1.1|2025-03-12|
|Impact Health|1.1.1|2025-03-12|
|Impact Health|1.1.1|2025-03-12|
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
|Incident Communications Management for Service Operations Workspace|7.1.3|2025-12-11|
|Incident Management for Field Service|1.1.1|2025-01-02|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Individual Life Claims|1.1.1|2025-01-30|
|Indoor Mapping for Assets|1.0.1|2025-01-30|
|Industrial Core|4.0.0|2026-06-16|
|Industrial Core|4.0.0|2026-06-16|
|Industrial Core|4.0.0|2026-06-16|
|Industrial Process Health|1.0.0|2025-01-30|
|Industrial Process Health|1.0.0|2025-01-30|
|Industrial Process Health|1.0.0|2025-01-30|
|Industrial Process Manager|3.1.0|2026-03-12|
|Industrial Process Manager|3.1.0|2026-03-12|
|Industrial Workspace Common|4.1.0|2026-06-16|
|Industry Core|1.0.9|2022-12-01|
|Infoblox Spoke|2.0.4|2024-03-20|
|Information Request Playbook|2.0.0|2025-01-30|
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
|Insurance claims|1.0.4|2025-07-31|
|Insurance claims|1.0.4|2025-07-31|
|Insurance claims|1.0.4|2025-07-31|
|Insurance claims|1.0.4|2025-07-31|
|Insurance claims|1.0.4|2025-07-31|
|Insurance Claims Core|3.2.1|2025-07-31|
|Insurance Claims Core|3.2.1|2025-07-31|
|Insurance Claims Core|3.2.1|2025-07-31|
|Insurance Claims Core|3.2.1|2025-07-31|
|Insurance Claims Core|3.2.1|2025-07-31|
|Insurance Claims Core|3.2.1|2025-07-31|
|Insurance Claims Core|3.2.1|2025-07-31|
|Insurance Claims Core|3.2.1|2025-07-31|
|Integration Commons for CMDB|2.25.0|2026-06-16|
|IntegrationHub Enterprise Flow Wizards|1.0.0|2021-08-19|
|Integration Hub Usage Dashboards|2.1.0|2025-05-01|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intelligent Servicing for Fraud|2.4.0|2025-07-31|
|Intent Discovery|3.3.8|2026-05-05|
|Interaction Control Component|2.2.0|2025-05-01|
|Interaction Management for Service Operations Workspace|7.1.3|2025-12-11|
|Interceptor UI for Service Operations Workspace|7.1.0|2025-05-01|
|Inventory Number Management|4.0.0|2025-01-30|
|Inventory Number Management|4.0.0|2025-01-30|
|Inventory Tracker App Template|27.2.3|2025-05-01|
|Inventory Tracker App Template|27.2.3|2025-05-01|
|Investigation Framework|7.1.0|2025-05-01|
|Investment Funding|1.1.1|2024-05-09|
|Invicti Application Vulnerability Integration|1.2.1|2024-11-07|
|Invoice Case Management|11.2.1|2026-06-16|
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
|IRM Compliance GenAI|22.2.0|2026-05-05|
|IRM Risk GenAI|22.2.0|2026-05-05|
|ISA Equipment Model|4.0.0|2026-06-16|
|ISA Equipment Model|4.0.0|2026-06-16|
|ISA Equipment Model|4.0.0|2026-06-16|
|Issue Auto Resolution for HR|4.0.3|2024-06-06|
|ITAM Common for DaaS|11.0.0|2024-08-01|
|ITAM common hub|1.1.0|2025-12-11|
|ITAM Health Check application|3.0.1|2025-07-31|
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
|ITOM Content Service|1.5.1|2025-05-01|
|ITOM Guided Setup - New|27.3.1|2026-06-16|
|ITOM Line chart|27.1.1|2026-03-12|
|ITOM Mobile Agent|1.0.0|2025-05-01|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|IT Service Management for Microsoft 365|2.8.0|2025-05-01|
|ITSM Analytics|3.1.0|2025-05-01|
|ITSM Enterprise UI Components|3.5.0|2025-12-11|
|ITSM Mobile Agent|10.0.0|2025-01-30|
|ITSM Process Mining Content Pack|1.9.0|2025-04-03|
|ITSM Success Dashboard indicators|8.1.0|2025-05-01|
|Jack Henry jXchange Spoke|2.1.0|2025-07-31|
|Jamf Spoke|1.0.8|2024-07-11|
|Jenkins Spoke|2.2.0|2025-03-12|
|Jenkins v2 Spoke|1.2.0|2023-02-02|
|Jira Service Management Spoke|1.1.1|2024-12-05|
|Jira Spoke|6.0.1|2026-04-09|
|Journey Accelerator|6.5.7|2025-05-01|
|Kanban board component|25.5.0|2025-07-31|
|Kanban Components|1.2.0|2026-03-12|
|KnowBe4 Integration for SecOps|2.3.3|2024-12-05|
|KPI Composer|4.2.11|2025-06-05|
|KPI Framework|3.0.0|2025-05-01|
|Kubernetes Spoke|1.2.0|2025-03-12|
|Kubernetes Visibility Agent|3.10.2|2025-03-12|
|Leader Hub|1.2.0|2025-05-01|
|Lead Management Application|4.0.1|2025-06-05|
|Lead Management Data Model|4.0.0|2025-05-01|
|Lead Management Data Model|4.0.0|2025-05-01|
|Lead to Cash Core|1.9.0|2026-06-16|
|Learning|5.4.0|2025-05-01|
|Learning Core|9.9.1|2026-03-12|
|Legal and Contracts Common Utilities|1.1.1|2026-06-16|
|Legal Conflict of Interest|4.6.0|2025-05-01|
|Legal Content Review|1.2.0|2025-05-01|
|Legal Counsel Center|2.2.0|2026-06-16|
|Legal Mobile|5.5.0|2023-08-03|
|Legal Practice Apps Core|1.0.2|2023-02-02|
|Legal Request Management|10.1.4|2026-06-16|
|Legal Simple Compliance|1.0.3|2025-05-01|
|Legal Simple Intellectual Property|1.5.3|2025-05-01|
|Legal Simple Privacy|1.2.1|2025-06-05|
|Legal Stock Preclearance|4.8.0|2025-05-01|
|Legal Tracker Spoke|1.0.4|2025-01-30|
|Legal Virtual Agent Conversations|1.3.2|2023-05-04|
|License and Permit Playbook|3.0.5|2025-07-31|
|Licensing Engine|6.4.3|2026-06-16|
|List AI Experience|3.0.0|2026-06-16|
|Live CI View|19.1.2|2023-05-04|
|Localization Workspace|1.0.6|2025-05-01|
|Log Export Service|3.2.0|2025-05-01|
|Looker Spoke|1.0.2|2025-01-30|
|Lucidchart Diagramming Spoke|1.1.1|2024-01-04|
|Lucidchart Integration|2.4.1|2025-01-30|
|Magnit Spoke|1.2.1|2023-09-07|
|Major Incident Management for Service Operations Workspace|7.1.3|2025-12-11|
|Major Security Incident Management|3.4.3|2025-06-05|
|Manage Order Operations|2.0.3|2026-06-16|
|Manage Skills Configurable Page|1.1.12|2025-01-30|
|Manufacturing Core|1.0.0|2025-05-01|
|Manufacturing Dealer Management|1.0.0|2025-05-01|
|Manufacturing Sales Promotion Claim Management|1.0.1|2025-05-01|
|Manufacturing Sales Promotion Management|1.0.0|2025-05-01|
|Mastercard Spoke|3.0.0|2025-05-01|
|Matrix report|20.1.1|2025-05-01|
|McAfee ePO Integration for Security Operations|10.5.1|2025-01-30|
|MCP for Strategic Portfolio Management|1.0.2|2026-06-16|
|Meeting CAB|1.0.7|2025-07-31|
|Meeting Extensions for Microsoft Teams|1.7.0|2025-05-01|
|Meeting Watcher - UI Builder Data Resource|1.0.9|2025-05-01|
|Mentoring|1.4.0|2025-05-01|
|Metric data table|22.0.0|2026-03-12|
|Metric Intelligence|2.6.3|2025-05-01|
|Metric Rules|1.1.4|2024-06-06|
|Metrics and CI Actions Framework|7.1.0|2025-05-01|
|Metrikus Spoke|1.0.5|2025-01-30|
|Microsoft 365 for ServiceNow Reporting|22.0.1|2026-03-12|
|Microsoft Active Directory v2 Spoke|2.4.0|2025-03-12|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure Application Insights Spoke|2.0.0|2024-11-07|
|Microsoft Azure Artifacts Spoke|1.1.0|2024-11-07|
|Microsoft Azure Automation Spoke|2.0.0|2024-11-07|
|Microsoft Azure Blob Storage Spoke|2.0.0|2024-11-07|
|Microsoft Azure Cosmos DB Spoke|2.0.0|2024-11-07|
|Microsoft Azure DevOps Boards Spoke|3.0.1|2025-07-10|
|Microsoft Azure DevOps Integration for Agile Development|1.6.0|2024-11-07|
|Microsoft Azure DevOps Integrations Common|1.8.1|2024-02-01|
|Microsoft Azure DevOps Pipelines Spoke|1.0.0|2023-08-03|
|Microsoft Azure Managed Storage Spoke|2.0.1|2024-11-07|
|Microsoft Azure Notification Hub Spoke|2.0.0|2024-11-07|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure Resource Management Spoke|2.0.0|2024-11-07|
|Microsoft Azure SQL Database Spoke|2.0.0|2024-11-07|
|Microsoft Azure Traffic Manager Spoke|2.0.0|2024-11-07|
|Microsoft Azure Virtual Machine Spoke|2.0.0|2024-11-07|
|Microsoft Azure Virtual Network Spoke|2.0.0|2024-11-07|
|Microsoft Defender for Cloud Integration for Security Operations|2.7.3|2025-06-05|
|Microsoft Defender for Office365 Integration for SecOps|2.3.4|2024-12-05|
|Microsoft Dynamics 365 for Finance and Operations Spoke|2.2.0|2024-11-07|
|Microsoft Dynamics CRM Spoke|1.6.0|2025-03-12|
|Microsoft Endpoint Configuration Manager for Investigation|7.1.0|2025-05-01|
|Microsoft Endpoint Configuration Manager Spoke|1.8.1|2025-06-05|
|Microsoft Entra ID Integration for Password Reset|3.0.3|2025-01-30|
|Microsoft Entra ID Spoke|4.5.0|2025-03-12|
|Microsoft Exchange Online for Security Operations|10.6.5|2025-05-01|
|Microsoft Exchange Online Spoke|3.13.0|2026-03-12|
|Microsoft Exchange Server Spoke|2.5.0|2023-08-03|
|Microsoft Graph Security API Alert Ingestion Integration For Security Operations|10.4.5|2022-09-21|
|Microsoft Integrations - Core|5.5.0|2025-05-01|
|Microsoft Intune Spoke|1.1.8|2025-01-02|
|Microsoft Office add-in|20.0.0|2025-01-30|
|Microsoft OneDrive Spoke|2.5.0|2025-03-12|
|Microsoft Outlook Add-In for Legal Service Delivery|1.4.1|2025-07-31|
|Microsoft Security Response Center Spoke|1.2.1|2025-03-12|
|Microsoft SharePoint File Explorer Connector for Security Incident Response integration|1.2.6|2025-05-01|
|Microsoft SharePoint Online Spoke|2.9.0|2025-05-01|
|Microsoft Teams Chat Connector for Security Incident Management|1.2.12|2024-11-07|
|Microsoft Teams Communications Spoke|1.4.2|2025-02-19|
|Microsoft Teams Graph Spoke|4.4.1|2026-02-05|
|Microsoft Word Add-in for ServiceNow Contracts|1.8.0|2026-06-16|
|MID Guardian|1.0.4|2025-12-11|
|Migration Utility for Service Operations Workspace|2.3.1|2025-05-01|
|Milestones|2.9.0|2026-06-16|
|Miro Spoke|3.2.0|2025-05-01|
|MISP integration for Security Operations|1.2.1|2025-06-05|
|Mitigation Controls Monitoring|4.0.2|2025-05-01|
|Mobile App Builder|27.10.1|2025-05-01|
|Mobile App Builder API|27.10.0|2025-05-01|
|Mobile Card Builder|26.11.2|2025-06-05|
|Mobile Publishing|23.2.0|2024-11-07|
|Mobile SDK|2.2.0|2025-03-12|
|Mobile Time Sheets|2.1.1|2023-02-02|
|Model Context Protocol Client|2.2.0|2026-06-16|
|monday.com Spoke|1.1.5|2025-06-05|
|MSIM VTB Task Card|1.0.1|2024-02-01|
|MS Teams Activities for PAD|1.0.3|2023-01-12|
|Multi-case creation framework|2.1.0|2025-07-31|
|Natural Language Understanding Models for Sourcing and Procurement Operations|2.0.5|2023-05-04|
|Navex EthicsPoint Spoke|1.0.2|2024-02-01|
|Network Inventory Advanced|4.1.0|2025-07-31|
|Network Inventory Core|4.1.0|2025-07-31|
|Network Inventory Workspace|4.1.0|2025-07-31|
|News Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|News Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|News Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|News Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|News Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|News Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|News Integration for Supplier Lifecycle Operations|2.5.0|2025-01-30|
|News Integration for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|NLU Workbench - Advanced Features|7.0.22|2025-07-10|
|Node map Experience Component|27.3.0|2025-12-11|
|Notification Flow Wizards|2.0.1|2022-09-21|
|Notify Connector for Microsoft Teams|2.8.0|2025-05-01|
|Notify UI Components for Configurable Workspaces|7.1.0|2025-05-01|
|Notify Webex Connector|1.3.0|2025-05-01|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Now Assist AI web agent|31.0.5|2026-06-16|
|Now Assist for Accounts Payable Operations \(APO\)|8.0.0|2026-06-16|
|Now Assist for App Engine|29.2.3|2026-06-16|
|Now Assist for Care Team Operations|2.0.1|2026-05-05|
|Now Assist for code generation|28.5.23|2026-06-16|
|Now Assist for Digital End-user Experience \(DEX\)|4.3.0|2026-06-16|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Employee Experience|4.3.2|2026-06-16|
|Now Assist for Error Framework|1.0.3|2026-06-16|
|Now Assist for Field Service Management \(FSM\)|10.0.1|2026-06-16|
|Now Assist for Financial Services Operations \(FSO\)|2.0.5|2026-01-20|
|Now Assist for FSC Common|7.0.0|2026-06-16|
|Now Assist for Health and Safety|1.4.1|2026-06-16|
|Now Assist for HLA|1.0.1|2026-03-12|
|Now Assist for Impact|4.0.5|2026-06-16|
|Now Assist for Integration Hub|2.2.1|2025-11-06|
|Now Assist for IRM|22.2.0|2026-05-05|
|Now Assist for Legal Service Delivery|1.8.1|2026-06-16|
|Now Assist for Operational Sustainability|22.0.2|2026-03-12|
|Now Assist for OTSM|3.1.2|2026-03-12|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Privacy Management|22.2.0|2026-05-05|
|Now Assist for Process Mining|2.6.8|2026-05-05|
|Now Assist for Public Sector Digital Services \(PSDS\)|2.2.2|2026-06-16|
|Now Assist for Purchase Order Management \(POM\)|1.2.0|2026-06-16|
|Now Assist for RPA Hub|5.0.4|2026-03-12|
|Now Assist for RSM|1.3.0|2026-03-12|
|Now Assist for Security Incident Response integrations|1.1.1|2026-01-20|
|Now Assist for Service Graph Connectors|1.1.0|2025-01-30|
|Now Assist for Sourcing and Procurement Operations \(SPO\)|10.0.0|2026-06-16|
|Now Assist for Spoke Generation|1.5.10|2025-12-11|
|Now Assist for Supplier Lifecycle Operations \(SLO\)|8.0.0|2026-06-16|
|Now Assist for Telecommunications|2.0.1|2026-06-16|
|Now Assist for Telecommunications|2.0.1|2026-06-16|
|Now Assist for Telecommunications, Media and Technology \(TMT\)|6.0.7|2026-06-16|
|Now Assist for Third-Party Risk Management|22.0.9|2026-04-09|
|Now Assist for Vault|1.0.4|2026-03-12|
|Now Assist for Workplace Service Delivery \(WSD\)|1.1.13|2026-06-16|
|Now Assist for Zero Copy Connector|2.0.0|2026-05-05|
|Now Assist in Conversational Spokes|1.0.0|2024-11-07|
|Now Assist in Virtual Agent Configurations|12.0.2|2026-04-09|
|Now Assist Platform Skills|3.0.3|2026-06-16|
|Now Assist Troubleshooting|4.0.2|2025-07-31|
|Now Learning Integration|1.0.3|2024-02-01|
|now-visualization-extensions|28.4.5|2026-05-05|
|Obligation Management|1.7.0|2026-06-16|
|Observability Commons for CMDB|1.1.0|2023-11-02|
|Okta Spoke|4.3.0|2025-05-01|
|Omnichannel Callback|2.0.5|2025-12-11|
|Omnichannel Callback for Customer Service Management|1.3.2|2025-01-30|
|Omni-Experience Standard Feature Set|7.4.0|2026-04-09|
|On Call Scheduling for Service Operations Workspace|7.1.2|2025-09-10|
|On-Call UI Components for Configurable Workspaces|7.1.5|2025-09-10|
|OneLogin Spoke|1.0.2|2023-09-07|
|One-time Password Generator|1.0.7|2024-07-11|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management|22.0.2|2026-03-12|
|Operational Technology Change Management|2.0.6|2025-01-30|
|Operational Technology Change Management|2.0.6|2025-01-30|
|Operational Technology Change Management|2.0.6|2025-01-30|
|Operational Technology Hardware Vulnerability Assessment|1.0.2|2025-03-12|
|Operational Technology Hardware Vulnerability Assessment|1.0.2|2025-03-12|
|Operational Technology Incident Management|3.1.0|2026-03-12|
|Operational Technology Incident Management|3.1.0|2026-03-12|
|Operational Technology Manager|4.0.0|2026-06-16|
|Operational Technology Manager|4.0.0|2026-06-16|
|Operational Technology Manager|4.0.0|2026-06-16|
|Operational Technology Vulnerability Response|2.0.4|2025-01-30|
|Operational Technology Vulnerability Response|2.0.4|2025-01-30|
|Operational Technology Vulnerability Response|2.0.4|2025-01-30|
|Opportunity Marketplace|2.3.1|2025-05-01|
|Oracle Autonomous DB Spoke|1.0.6|2022-12-01|
|Oracle Block Storage Spoke|1.0.4|2022-12-01|
|Oracle Boot Volume Spoke|1.0.6|2022-12-01|
|Oracle Cloud IAM Spoke|1.1.3|2022-09-21|
|Oracle Compute Engine Spoke|1.0.4|2022-12-01|
|Oracle EBS Spoke|1.13.0|2024-11-07|
|Oracle Financial Cloud Spoke|1.1.0|2023-09-20|
|Oracle HCM Cloud Spoke|4.1.1|2025-01-02|
|Oracle Object Storage Management Spoke|1.0.3|2022-09-21|
|Oracle Peoplesoft Financial Spoke|1.1.0|2024-03-07|
|Oracle Virtual Cloud Network Spoke|1.0.4|2022-12-01|
|Order Case Playbook|1.3.0|2025-07-10|
|Order Case Playbook|1.3.0|2025-07-10|
|Order Case Playbook|1.3.0|2025-07-10|
|Order Case Playbook|1.3.0|2025-07-10|
|Order Case Playbook|1.3.0|2025-07-10|
|Order Case Self Service|1.4.3|2026-06-16|
|Order Case Self Service|1.4.3|2026-06-16|
|Order Management|17.0.2|2026-06-16|
|Order Management|5.0.0|2023-02-02|
|Order Management for Telecom, Media and Tech|11.2.2|2025-07-31|
|Order Management Portal|1.4.0|2025-07-10|
|Order Operations Case Management|2.8.0|2026-06-16|
|Order Operations Case Management|2.8.0|2026-06-16|
|Order Qualification Management|4.5.0|2026-06-16|
|Order Qualification Management|4.5.0|2026-06-16|
|Order to cash common architecture|1.5.0|2026-03-12|
|OT Asset Management|2.1.1|2025-06-05|
|OT Manager Foundation|3.3.3|2026-06-16|
|Outlook Actionable Messages|4.6.1|2025-12-11|
|PagerDuty Spoke|1.4.1|2025-06-05|
|Palo Alto Networks NGFW for Security Operations|10.4.7|2025-05-01|
|Parallel Review and Feedback|20.0.0|2025-01-30|
|Participant Suggestions|2.0.1|2024-08-01|
|Password Reset for Service Operations Workspace|7.1.0|2025-05-01|
|Password Reset integration for Microsoft Active Directory|3.0.0|2024-11-07|
|Password Reset integration with Google Directory|1.0.3|2023-06-01|
|Password Reset integration with Okta|1.1.2|2023-04-06|
|Password Reset UI components for Configurable Workspaces|7.1.0|2025-05-01|
|Patch Management Data Model|1.0.4|2025-05-01|
|Pattern Designer Enhancements|3.7.0|2025-05-01|
|Payment Card|1.0.1|2025-07-31|
|Payment Card|1.0.1|2025-07-31|
|Payment Card|1.0.1|2025-07-31|
|Payment Card|1.0.1|2025-07-31|
|Payment Card|1.0.1|2025-07-31|
|Payment Card|1.0.1|2025-07-31|
|Payment Card|1.0.1|2025-07-31|
|Payment Card|1.0.1|2025-07-31|
|Payment framework for conversational channels|1.0.1|2025-07-31|
|PDF Extractor|27.2.1|2025-05-01|
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
|Performance Analytics Content Pack for Agile 2.0|1.4.5|2025-06-05|
|Performance Analytics Content Pack for Cloud Resources|1.5.0|2024-11-07|
|Performance Analytics Content Pack for Essential SAFe|1.4.2|2023-09-20|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Legal Service Delivery|2.6.0|2025-01-30|
|Performance Analytics Content Pack for Public Sector Digital Services|2.0.3|2024-09-10|
|Performance Analytics - Content Pack - Guided Tours|1.3.0|2025-01-30|
|Performance Analytics Content Pack - Vendor Management Workspace|2.0.1|2024-11-07|
|Performance Analytics for Configuration Compliance|1.5.1|2025-05-01|
|Performance Analytics for Security Incident Response|10.5.2|2025-05-01|
|Performance Analytics for Sourcing and Procurement Operations|3.0.9|2024-08-01|
|Performance Analytics for Vulnerability Response|12.15.9|2025-05-01|
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
|Performance Analyzer Page|2.1.0|2025-10-16|
|Performance Appraisal App Template|27.2.3|2025-05-01|
|Performance Appraisal App Template|27.2.3|2025-05-01|
|Physical Assets|2.3.0|2026-03-12|
|Pipeline|29.2.1|2026-06-16|
|Planned Maintenance Management|2.9.0|2025-07-31|
|Planned Task Common|1.0.4|2023-05-04|
|Planned Work Management|2.9.0|2025-07-31|
|Playbook Experience|28.5.2|2026-05-05|
|Playbook Experience Components|28.5.1|2026-05-05|
|Playbooks for Customer Service Management|6.5.1|2026-06-16|
|Plivo Spoke|1.1.0|2024-02-01|
|Pluralsight Spoke|1.2.1|2025-05-01|
|Policy as Code Engine|3.1.0|2025-05-01|
|policy-as-code-engine-ui|3.1.0|2025-05-01|
|Portal navigation demo|27.0.0|2025-06-05|
|Portal Next Experience Theme|24.2.2|2026-03-12|
|Portfolio Planning integrations for Shared Infrastructure|3.12.0|2026-06-16|
|Portfolio Planning with PPM, Agile 2.0, and SAFe|4.7.0|2026-06-16|
|Post Assessment Actions for Smart Assessments|22.0.2|2026-03-12|
|PPM Collaboration|2.1.0|2024-11-07|
|Predictive Intelligence for Legal Service Delivery|1.1.2|2024-11-07|
|Predictive Intelligence for User Reported Phishing|10.3.7|2024-09-10|
|Predictive Intelligence Store App|1.0.3|2025-12-11|
|Preferred tables|27.2.1|2025-05-01|
|Pre-Visit Management|9.1.2|2025-01-30|
|Pre-Visit Management|9.1.2|2025-01-30|
|Pre-Visit Management|9.1.2|2025-01-30|
|Pre-Visit Management|9.1.2|2025-01-30|
|Pre-Visit Management|9.1.2|2025-01-30|
|Price Management|17.0.1|2026-06-16|
|Privacy Employee User|19.0.1|2024-08-01|
|Proactive Customer Service Operations|24.0.1|2025-07-31|
|Proactive Customer Service Operations with Event Management|24.0.1|2025-07-31|
|Proactive Engagement|4.0.0|2026-03-12|
|Proactive Engagement|4.0.0|2026-03-12|
|Proactive Engagement|4.0.0|2026-03-12|
|Proactive Engagement|4.0.0|2026-03-12|
|Proactive Prompts|3.3.2|2024-11-07|
|Proactive Triggers|3.0.10|2025-12-11|
|Problem Management for Service Operations Workspace|7.1.3|2025-12-11|
|Problem Management Migration Utility|2.2.0|2025-05-01|
|Process Automation Content|27.0.3|2025-03-12|
|Process Automation Designer|28.4.8|2026-04-09|
|Process Automation Experience Demo|24.1.4|2024-10-03|
|Process Mining|28.9.9|2026-05-05|
|Process Mining Content Pack for CSM|23.1.0|2025-01-30|
|Process Mining Content Pack for FSM|1.4.0|2025-01-30|
|Process Mining Content Pack for SPM|1.0.0|2023-08-03|
|Process Mining for external data|28.8.4|2025-09-10|
|Process Mining for external data|28.8.4|2025-09-10|
|Process Mining for external data|28.8.4|2025-09-10|
|Process Mining for external data|28.8.4|2025-09-10|
|Process Mining for external data|28.8.4|2025-09-10|
|Process Mining for Source-to-Pay Operations|1.0.1|2024-08-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining Workspace Components|28.9.9|2026-05-05|
|Procurement Case Management|16.0.2|2026-06-16|
|Procurement File Transfer Framework|2.2.2|2023-05-04|
|Procurement for Field Service|2.0.0|2025-01-30|
|Product and pricing rules|6.0.0|2025-05-01|
|Product and pricing rules|6.0.0|2025-05-01|
|Product Capability Core|1.6.4|2026-03-12|
|Product Capability Core|1.6.4|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Advanced|10.3.0|2026-03-12|
|Product Catalog Management Portal|1.1.0|2025-05-01|
|Product Catalog Management Portal|1.1.0|2025-05-01|
|Product Conditions Core|4.6.0|2026-06-16|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Inventory Advanced|13.0.1|2026-06-16|
|Product Offering Recommendations|1.1.0|2025-05-01|
|Product Offering Recommendations|1.1.0|2025-05-01|
|Product Offering Recommendations|1.1.0|2025-05-01|
|Product Offering Recommendations|1.1.0|2025-05-01|
|Profanity filter for agent chat|3.0.12|2024-11-07|
|Professional Data Model|1.0.3|2025-05-01|
|Project Costing for Sourcing and Procurement Operations|2.10.0|2025-05-01|
|Project Status Report|1.1.0|2023-02-02|
|Public Sector Digital Services AI Agent Collection|1.3.1|2026-06-16|
|Public Sector Digital Services Core|14.0.1|2026-06-16|
|Purchase Order Management|2.2.2|2026-06-16|
|Qualys Integration for Security Operations|12.17.1|2025-05-01|
|Quick filter component|27.1.4|2025-07-31|
|Quick links component for Service Operations Workspace|7.1.0|2025-05-01|
|Quote Management Application|6.0.1|2025-07-31|
|Quote Management Data Model|6.0.0|2025-05-01|
|Quote Management Data Model|6.0.0|2025-05-01|
|RAG for code generation|1.1.8|2026-03-12|
|Rally Spoke|1.0.3|2023-05-04|
|Rapid7 Integration for Security Operations|13.15.1|2025-05-01|
|Recommendation template|22.0.1|2026-03-12|
|Recommended Actions|42.0.0|2026-06-16|
|Recommended Actions - Advanced|10.0.2|2025-05-01|
|Recommended Actions - Advanced|10.0.2|2025-05-01|
|Recommended Actions for Customer Service|29.0.1|2025-05-01|
|Recommended Actions for ITSM|3.3.0|2026-03-12|
|Record lookup connected component|27.1.3|2025-05-01|
|Record Page for Service Operations Workspace|7.1.0|2025-05-01|
|Record Related Items Connected|2.0.4|2025-01-02|
|Record - vertical|22.0.0|2026-03-12|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Regulatory Agency Library|20.1.0|2025-05-01|
|Related party|1.0.6|2023-02-02|
|Related party|1.0.6|2023-02-02|
|Release Timeline Component|1.3.0|2025-05-01|
|Remedial Actions Framework|7.1.0|2025-05-01|
|Remediation Playbooks|1.1.0|2022-11-03|
|Reporting UI Component for Workspace|2.4.0|2026-06-16|
|Requester Experience Templates|1.0.0|2024-11-07|
|Requirement Intake Diagram|1.0.1|2024-12-05|
|Retail Core|5.4.0|2025-12-11|
|Retail Task Management Core|2.2.0|2025-07-31|
|Retail Task Management Core|2.2.0|2025-07-31|
|Retail Task Management Core|2.2.0|2025-07-31|
|Retry Handler Framework|1.0.2|2022-09-21|
|Rich Text Editor Component for Security Operations|2.0.1|2026-06-16|
|Risk Assessments for Supplier Lifecycle Operations|1.4.0|2025-01-30|
|Risk Assessments for Supplier Lifecycle Operations|1.4.0|2025-01-30|
|Risk Assessments for Supplier Lifecycle Operations|1.4.0|2025-01-30|
|Risk Assessments for Supplier Lifecycle Operations|1.4.0|2025-01-30|
|Risk Assessments for Supplier Lifecycle Operations|1.4.0|2025-01-30|
|Risk Assessments for Supplier Lifecycle Operations|1.4.0|2025-01-30|
|Risk Assessments for Supplier Lifecycle Operations|1.4.0|2025-01-30|
|Risk Assessments for Supplier Lifecycle Operations|4.0.0|2026-06-16|
|Risk Assessments Integration for Sourcing and Procurement Operations|1.5.4|2023-11-02|
|RMA Case Management|2.1.0|2026-03-12|
|Roadmap Planning|3.2.0|2022-05-05|
|Roadmunk Spoke|1.6.5|2024-07-11|
|RPA Hub|17.0.0|2026-03-12|
|RPA Plugin Bundle|17.0.0|2026-03-12|
|RSM AI agent collection|1.3.0|2026-03-12|
|Saba Spoke|1.0.4|2022-12-01|
|Safe Workplace Dashboard|1.40.2|2024-11-07|
|Safe Workplace for mobile|2.10.1|2024-01-04|
|Safe Workplace suite|1.34.0|2022-11-03|
|Safe Workplace suite Professional|1.25.0|2022-11-03|
|Sales Agreement Data Model|7.0.0|2025-05-01|
|Sales Agreement Management|7.0.0|2025-05-01|
|Sales and Service API Core|7.3.0|2026-06-16|
|Sales Development AI Agents|1.0.9|2026-05-05|
|Salesforce Marketing Cloud Spoke|1.5.1|2025-03-12|
|Salesforce Spoke|2.3.3|2025-03-12|
|Sales Forecasting|1.0.0|2025-05-01|
|Sales Quota Application|1.0.0|2025-05-01|
|Sales Quota Data Model|1.0.0|2025-05-01|
|SBOM Core|6.0.6|2025-05-01|
|SBOM Response|6.2.2|2025-06-05|
|Scan Engine|3.0.4|2026-06-16|
|SCCM Usage Metering Spoke|1.0.2|2023-09-07|
|Scenario Planning for PPM|2.3.6|2025-01-30|
|Scope 3 emissions management|20.1.0|2025-05-01|
|Scrum Common|1.4.5|2025-01-30|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Secops Health Analytics|2.4.3|2025-12-11|
|Secureworks CTP Spoke|1.0.3|2022-09-21|
|Security Case Management common PAD artefacts|1.1.12|2026-01-20|
|Security Case Management common workspace components|2.1.0|2026-06-16|
|Security Center|3.1.4|2025-12-11|
|Security Incident Response integration with AWS SecurityHub|1.0.2|2025-03-12|
|Security Incident Response integration with FireEye HX|1.0.14|2024-11-07|
|Security Incident Response integration with Microsoft Defender for Endpoint|1.0.12|2025-06-05|
|Security Incident Response integration with Proofpoint|1.0.4|2025-07-10|
|Security Incident Response Integration with Zscaler|11.1.3|2025-01-30|
|Security Incident Response Mobile|10.4.0|2024-11-07|
|Security Incident Response Process Mining Content Pack|1.0.1|2025-05-01|
|Security Incident UI Card Component|1.0.1|2023-12-07|
|Security Integration Framework|13.12.1|2025-12-11|
|Security Operations 'Have I been pwned?' Integration|10.5.1|2025-03-12|
|Security Operations CrowdStrike Intelligence Integration|10.7.0|2024-08-01|
|Security Operations Hybrid Analysis Integration|10.6.0|2024-08-01|
|Security Operations LogRhythm Integration|11.1.10|2025-04-03|
|Security Operations Metadefender Integration|10.5.0|2024-08-01|
|Security Operations Palo Alto Networks - AutoFocus|10.4.0|2025-01-30|
|Security Operations Palo Alto Networks - WildFire|10.4.0|2025-01-30|
|Security Operations PhishTank Integration|10.5.0|2024-08-01|
|Security Operations Reverse WHOIS Integration|10.4.0|2024-08-01|
|Security Operations RiskIQ Integration|10.4.1|2024-08-01|
|Security Operations Setup Assistant|10.4.41|2026-06-16|
|Security Operations Shodan Integration|10.4.1|2024-08-01|
|Security Operations Spoke|10.6.7|2025-06-05|
|Security Operations VirusTotal Integration|10.4.0|2024-08-01|
|Security Posture Control Core|6.1.2|2025-05-01|
|Security Simulation and Training Integration for SecOps|2.1.3|2024-05-09|
|Security Support Common|30.4.1|2026-06-16|
|Security Support Orchestration|12.13.4|2025-01-30|
|Service Applicant Information|2.2.0|2025-07-31|
|Service Applicant Program Management|1.0.3|2025-07-31|
|Service Bridge for Public Sector Digital Services \(PSDS\)|1.0.2|2025-05-01|
|Service Builder|3.5.0|2025-05-01|
|Service Builder Components|2.1.2|2024-03-07|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Exchange Base|2.3.10|2026-03-19|
|Service Exchange for Consumers|2.3.10|2026-03-19|
|Service Exchange for Providers|2.1.36|2026-04-09|
|Service Exchange Health|2.3.10|2026-03-19|
|Service Exchange Order Management for Providers|2.1.36|2026-04-09|
|Service Exchange Remote Process Sync Transport|2.3.10|2026-03-19|
|Service Graph Connector Dependencies|1.0.0|2021-01-21|
|Service Graph Connector for AWS|2.10.1|2025-05-01|
|Service Graph Connector for ExtraHop|2.0.3|2020-09-16|
|Service Graph Connector for GCP|1.9.0|2025-05-01|
|Service Graph Connector for Google Console|1.0.0|2024-08-01|
|Service Graph Connector for Infoblox|1.1.1|2024-03-20|
|Service Graph Connector for Jamf|2.14.1|2025-01-30|
|Service Graph Connector for Microsoft Azure|1.12.1|2025-05-30|
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
|Service Graph Connector for Microsoft SCCM|3.6.0|2024-11-07|
|Service Graph Connector for NOKIA Altiplano|1.0.1|2025-01-30|
|Service Graph Connector for Observability - AppDynamics|1.4.0|2024-11-07|
|Service Graph Connector for Observability - Datadog|1.2.1|2023-03-22|
|Service Graph Connector for Observability - Dynatrace|1.12.0|2025-05-01|
|Service Graph Connector for Observability - New Relic|1.2.1|2023-03-22|
|Service Graph Connector for OpenTelemetry|1.4.1|2024-05-09|
|Service Graph Connector for SolarWinds|2.5.0|2025-03-12|
|Service Graph Connector for Tanium|1.8.0|2025-05-01|
|Service Graph Connector for VMware Workspace ONE UEM|1.7.0|2024-12-05|
|Service Graph Connector for Wiz|1.3.0|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Licensing|1.0.0|2022-05-05|
|Service Graph Connector Support Tools|1.0.0|2024-02-01|
|Service Level Management Experience for Workspace|7.1.0|2025-05-01|
|Service Level Objective Management for Service Operations Workspace|1.3.0|2025-05-01|
|Service Mapping Plus|1.15.2|2025-05-01|
|ServiceNow Add-Ins for Microsoft Office|7.4.3|2026-03-12|
|ServiceNow Benchmarks|4.1.0|2025-05-01|
|ServiceNow Document Designer with Word|20.0.1|2025-01-30|
|ServiceNow Enterprise Asset Management|8.1.3|2025-06-05|
|ServiceNow ITOM/OT SU Licensing|3.10.2|2025-07-10|
|ServiceNow Kafka Consumer|1.0.1|2023-04-06|
|ServiceNow Remote Instance Spoke|2.2.7|2024-12-05|
|ServiceNow Studio|29.2.6|2026-06-16|
|ServiceNow Voice|4.8.3|2025-07-31|
|ServiceNow Voice for CSM|3.8.1|2025-01-30|
|ServiceNow Voice for HR Service Delivery \(HRSD\)|1.0.2|2024-02-01|
|ServiceNow Voice for ITSM|4.1.0|2025-08-07|
|ServiceNow Voice UI components|3.7.3|2025-05-01|
|service-observability-app|1.7.3|2025-06-05|
|Service Observability UI|1.7.3|2025-06-05|
|Service Operations Workspace Admin Center|7.1.0|2025-05-01|
|Service Operations Workspace Core|7.1.4|2025-09-10|
|Service Operations Workspace Express List App|27.1.2|2026-06-16|
|Service Operations Workspace Integrations launchpad|27.1.5|2026-06-16|
|Service Operations Workspace Integrations launchpad UI|27.1.1|2026-06-16|
|Service Operations Workspace ITSM Admin Center|7.1.1|2025-07-31|
|Service Operations Workspace ITSM Common|7.1.5|2025-12-11|
|Service Operations Workspace Link View|27.1.1|2026-06-16|
|Service Operations Workspace Log Analytics|26.6.1|2026-06-16|
|Service Operations Workspace Metric Explorer|27.1.1|2026-06-16|
|Service Operations Workspace Metric Explorer APIs|23.4.0|2025-07-31|
|Service Operations Workspace Service Map Monitoring|26.4.0|2025-05-01|
|Service Operations Workspace Service Reliability Management \(SRM\) Common|6.3.3|2025-06-05|
|Service Reliability Management|6.3.2|2025-06-05|
|Service Request Criteria|3.0.1|2025-12-11|
|Service Request Management App Template|27.2.3|2025-05-01|
|Service Request Management App Template|27.2.3|2025-05-01|
|Service Request Playbook|3.0.0|2025-01-30|
|Service Test Management|2.1.0|2025-01-30|
|Service Test Management|2.1.0|2025-01-30|
|Service Test Management|2.1.0|2025-01-30|
|Service Test Management|2.1.0|2025-01-30|
|Service Test Management|2.1.0|2025-01-30|
|SGC Central|2.1.0|2025-05-01|
|Shared Library for Talent Development|2.3.1|2025-05-01|
|SharePoint Online Search Connector|6.1.2|2024-11-07|
|Shift Handover Application|1.8.0|2026-06-16|
|Shift Planning|7.0.0|2026-03-12|
|Shift Planning for Configurable Workspace|3.8.0|2026-03-12|
|Shift Scheduling for Field Service|6.0.4|2025-07-31|
|Shodan Exploit Integration for Security Operations|10.8.0|2024-11-07|
|Shopping Hub Mobile|7.6.20|2025-05-01|
|Sitemap Generator|1.1.4|2024-05-09|
|Site Mapping for Field Service Management|2.0.6|2025-07-31|
|Site Reliability Metrics|2.1.7|2023-11-02|
|Site Reliability Metrics UX|2.1.7|2023-11-02|
|Site Reliability Operations|14.2.3|2024-05-09|
|Skill Review Management|1.6.1|2025-12-11|
|Skills Industry Data|1.2.0|2024-11-07|
|Skills Intelligence|8.0.0|2025-05-01|
|Skills Intelligence Workspace|5.0.1|2025-06-05|
|Slack Activities for PAD|1.0.3|2023-01-12|
|Slack Chat Connector for Security Incident Management|1.0.1|2025-05-01|
|Slack Spoke|1.7.0|2025-03-12|
|Smart Assessment Collaboration|22.0.1|2026-03-12|
|Smart Assessment Core|22.0.4|2026-03-12|
|Smart Assessment for Mobile|1.0.0|2025-01-30|
|Smart Assessment Migration tools|22.0.0|2026-03-12|
|SmartRecruiters Spoke|1.0.0|2021-11-18|
|Smartsheet Spoke|2.4.0|2025-05-01|
|sn-4q-bubble|23.2.2|2026-06-16|
|sn-actionable-insights|1.1.1|2026-06-16|
|sn-apm-diagram-builder|3.2.2|2025-06-05|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-kpi|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-analytics-workflow-source|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-app-kpi-details|7.0.1|2025-07-31|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|sn-chart-renderer|28.4.5|2026-05-05|
|sn-circuit-map|4.0.0|2025-01-30|
|sn-circuit-map|4.0.0|2025-01-30|
|sn-cmdb-nlq-search|2.3.3|2024-11-07|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|sn-csm-custom-activity-tile|3.0.1|2025-07-31|
|sn-cwm-agile|2.1.0|2026-03-12|
|sn-docintel-iframe|1.0.4|2024-02-01|
|sn-docs|7.6.0|2026-06-16|
|sn-formula-kit|1.0.1|2026-06-16|
|sn-fsm-components|28.1.1|2025-07-31|
|sn-guided-action-experience|36.0.1|2025-05-01|
|sn-guided-action-experience|36.0.1|2025-05-01|
|sn-guided-action-playbook-card|31.0.1|2025-05-01|
|sn-guided-action-playbook-card|31.0.1|2025-05-01|
|sn-hr-casecard|1.3.1|2025-01-02|
|sn-ia-summary-card|1.0.1|2025-05-01|
|sn-multipivot|28.4.5|2026-05-05|
|sn-next-best-action-list|39.0.0|2026-06-16|
|sn-next-best-action-list|39.0.0|2026-06-16|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-analytics|28.0.1|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|sn-nlq-query-input|28.0.3|2025-07-31|
|Snowflake Spoke|1.0.2|2025-01-30|
|sn-par-analytics-list|28.4.5|2026-05-05|
|sn-par-forecast-config|28.4.5|2026-05-05|
|sn-par-multipivot-extension|28.4.5|2026-05-05|
|sn-quick-filter-popover|24.3.1|2026-05-05|
|sn-rack|3.0.0|2025-01-30|
|sn-rack|3.0.0|2025-01-30|
|sn-reusable-impact-framework|22.0.0|2026-03-12|
|sn-risk-assessment|20.1.1|2025-05-01|
|sn-scorecard-list|28.4.5|2026-05-05|
|sn-smart-assessment-connected|22.0.3|2026-03-12|
|sn-smart-assessment-designer|22.0.1|2026-03-12|
|sn-timer|1.0.0|2025-01-30|
|sn-topology-map|3.0.0|2025-01-30|
|sn-topology-map|3.0.0|2025-01-30|
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
|sn-uxf-formula-parser|28.2.0|2025-12-11|
|Social Benefits Playbook|2.0.2|2025-07-31|
|Socure Spoke|1.1.1|2022-11-03|
|Software Asset Management for CPE support|1.0.0|2022-08-04|
|Software Asset Management Guided Experiences|6.0.3|2025-07-31|
|Software Asset Management integration with Salesforce CRM|2.0.0|2025-07-31|
|Software Asset Management integration with Salesforce Marketing Cloud|1.2.7|2025-03-12|
|Software Asset Management integration with Tableau|1.0.1|2024-08-01|
|Software Asset Management integration with Workday|1.0.12|2025-01-30|
|Software Asset Management - SaaS License Connections|4.0.1|2023-02-02|
|Software Asset Management - SaaS License Management Foundation|12.0.4|2025-07-31|
|Source-to-Pay Common Architecture|21.2.1|2026-06-16|
|Source-to-Pay Operations with Contract Management Pro|2.0.1|2025-05-01|
|Source-to-Pay Workspace|17.0.1|2026-06-16|
|Sourcing and Purchasing Automation|11.2.6|2026-06-16|
|SOW Funnel Highchart Component|28.3.1|2026-03-12|
|Spend and Savings Management|1.0.1|2025-05-01|
|Splunk Search Integration for Security Operations|10.4.11|2025-03-12|
|SPM Benchmarking|1.0.0|2022-11-03|
|SPM Common UI Component|4.1.0|2026-03-12|
|SPM Team Member|1.0.0|2026-04-09|
|Spoke Generator|4.2.0|2025-09-10|
|Status Report UI Component for MSIM Workspace|1.0.2|2024-11-07|
|Store app certification|Version|Market launch date|
|Strategic Planning|4.7.0|2025-05-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Portfolio Management for Telecom Project Templates|1.0.1|2024-08-01|
|Strategic Spend Tracking for PPM|1.1.0|2024-05-09|
|Stream Connect Designer|3.0.1|2025-05-01|
|Subscription Management v2|6.4.3|2026-06-16|
|Success Dashboard Common|4.1.0|2025-05-01|
|Success Dashboard Core|8.1.0|2025-05-01|
|SuccessFactors Learning Spoke|1.0.0|2025-01-30|
|Summarization for Order Management|2.1.0|2026-05-05|
|Summarization for Quote Management|1.1.0|2026-04-09|
|SumTotal Spoke|1.1.0|2023-03-02|
|Supplier Collaboration Portal|8.0.0|2026-06-16|
|Supplier Collaboration Portal|8.0.0|2026-06-16|
|Supplier Operations|4.0.0|2026-06-16|
|Supplier Payment Optimization|3.0.0|2026-06-16|
|Supplier Relationship and Performance Management|3.0.0|2025-05-01|
|Supplier Relationship and Performance Management|7.0.0|2026-06-16|
|SurveyMonkey Spoke|2.0.6|2024-08-01|
|Surveys for mobile|1.0.2|2021-09-16|
|Sustainable IT|20.1.0|2025-05-01|
|Synthetic Monitoring|1.2.4|2025-06-05|
|System Events and Jobs Dashboard|3.0.7|2026-01-20|
|Tableau Spoke|1.0.2|2024-08-01|
|Table Builder|27.2.2|2025-05-01|
|Tag Based Alert Clustering Engine|18.24.0|2026-06-16|
|Tag Governance|1.5.0|2024-11-07|
|Talent Development Core|5.1.4|2025-06-05|
|Talent feedback|1.0.1|2025-05-01|
|Task Communications Management UI Components for Configurable Workspaces|7.1.2|2025-05-01|
|Task Intelligence Admin Console|5.0.6|2025-06-05|
|Task Intelligence for Customer Service|25.2.1|2024-11-07|
|Task Intelligence for ITSM|8.0.0|2025-05-01|
|Task Plan Template AI Agents|1.0.0|2026-06-16|
|Task Plan Templates|4.0.0|2026-06-16|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Team Contacts App Template|27.2.3|2025-05-01|
|Team Contacts App Template|27.2.3|2025-05-01|
|Team Management for Field Service|6.0.3|2025-07-31|
|Team Performance|202603.0.0|2026-03-12|
|Technology Portfolio Management|1.7.2|2025-05-01|
|Telecom Discovery Patterns|1.0.1|2025-01-30|
|Telecommunication Open APIs|4.1.0|2025-05-01|
|Telecommunication Open APIs|4.1.0|2025-05-01|
|Telecommunications Media and Technology AI agent collection|6.0.1|2026-06-16|
|Telecommunications Media and Technology AI agent collection|6.0.1|2026-06-16|
|Telecom Service Operations Core|1.0.1|2025-01-30|
|telemetry-data-connector|1.2.1|2026-05-05|
|Test Generation|5.0.2|2026-03-12|
|Theme Builder AI|1.1.0|2026-05-05|
|Third-party Risk Due Diligence|22.0.1|2026-03-12|
|Third-party Risk Management|22.0.2|2026-03-12|
|Threat Intelligence|13.3.2|2025-06-05|
|Threat Intelligence Security Center for Security Operations|3.12.0|2025-05-01|
|Threat Intelligence Security Center integration with CrowdStrike Intelligence|3.0.4|2025-03-12|
|Threat Intelligence Security Center integration with Elasticsearch|3.0.4|2025-05-01|
|Threat Intelligence Security Center integration with Microsoft Defender for Endpoint|1.0.4|2025-06-05|
|Threat Intelligence Security Center Integration with Palo Alto Networks NGFW|2.0.1|2025-03-12|
|Threat Intelligence Security Center integration with Shodan|1.0.7|2025-05-01|
|Threat Intelligence Security Center integration with Splunk Search|3.0.5|2025-03-12|
|Threat Intelligence Security Center integration with VirusTotal|3.0.3|2025-03-12|
|Threat Intelligence Security Center integration with WHOIS|5.0.4|2025-03-12|
|Threat Intelligence Support Common|13.6.4|2026-06-16|
|Threat Intelligence Support Common UI Components|1.1.3|2025-05-01|
|Timeline component|28.0.1|2025-12-11|
|Time Off Request App Template|27.2.3|2025-05-01|
|Time Off Request App Template|27.2.3|2025-05-01|
|Total Cost of Ownership|1.1.0|2026-06-16|
|Touchpoint Meeting|2.7.0|2026-06-16|
|Transporter|2.3.10|2026-03-19|
|Trello Spoke|1.3.0|2024-11-07|
|Triggers|28.1.4|2026-05-05|
|Twilio Spoke|1.2.0|2023-02-02|
|UCF Spoke|1.1.0|2023-05-04|
|Udemy Spoke|1.0.2|2022-12-01|
|UI Builder|28.2.75|2026-02-05|
|UI Components for Customer Portals|4.0.0|2026-02-05|
|UI Generation|28.2.14|2026-01-23|
|UiPath Spoke|2.3.0|2024-10-03|
|UI shared library|1.3.1|2025-05-01|
|UKG Spoke|3.4.0|2024-11-07|
|Unified Content Management|22.0.1|2026-03-12|
|Universal Request AI agent collection|1.0.9|2026-06-16|
|Universal Request for Source-to-Pay Operations|1.2.2|2026-06-16|
|Universal Request integration with Microsoft Teams|1.0.2|2022-12-01|
|Universal Task|2.6.2|2025-07-31|
|Urjanet ESG integration|20.1.0|2025-05-01|
|User Experience Analytics API|3.1.2|2024-02-01|
|User Experience Analytics Funnel|5.0.8|2025-07-31|
|User Sense|1.1.13|2025-12-11|
|User Surveys|1.5.4|2025-12-11|
|Utility Actions Spoke|1.3.0|2024-10-03|
|UX Commons|27.0.2|2025-07-31|
|Vaccination Status|1.23.4|2024-05-09|
|Value stream artifacts|2.3.0|2026-06-16|
|Vault Console|1.1.0|2025-12-11|
|Vendor Management Mobile|1.3.0|2023-08-03|
|Vendor Manager Workspace|3.5.0|2024-11-07|
|Vendor Risk Management integration with EcoVadis|20.1.1|2025-05-01|
|Verifi Spoke|1.0.0|2024-08-01|
|Virtual Agent Adapter Common|6.2.2|2025-12-11|
|Virtual Agent API|4.2.0|2026-04-09|
|Virtual Agent for PPM|1.0.1|2023-05-04|
|Virtual Agent for Sourcing and Procurement Operations|3.8.0|2025-05-01|
|Virtual Agent Topic Recommendations|4.5.5|2024-08-01|
|Visa Spoke|2.0.0|2025-05-01|
|Visibility Content|6.26.0|2025-05-01|
|Vonage Spoke|1.1.4|2024-10-03|
|Vulnerability Crisis Management|1.0.1|2024-08-01|
|Vulnerability Exposure Assessment|5.1.2|2025-06-05|
|Vulnerability Response|26.5.3|2026-01-20|
|Vulnerability Response and Configuration Compliance for Containers|2.13.5|2025-06-05|
|Vulnerability Response Common|2.15.0|2026-01-20|
|Vulnerability Response Common Workspace|1.9.0|2026-01-20|
|Vulnerability Response Integration Framework|1.3.0|2026-01-20|
|Vulnerability Response Integration with Agile Management|1.1.2|2024-11-07|
|Vulnerability Response Integration with Atlassian Jira|1.0.4|2024-05-09|
|Vulnerability Response Integration with Black Duck|1.0.5|2024-05-09|
|Vulnerability Response Integration with CISA|1.5.1|2025-07-31|
|Vulnerability Response Integration with Microsoft Defender for IoT \(Azure\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Threat and Vulnerability Management|2.6.3|2025-05-01|
|Vulnerability Response Integration with NVD|1.7.2|2025-07-31|
|Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute|3.2.2|2025-05-01|
|Vulnerability Response Integration with Palo Alto Prisma Cloud|2.7.0|2025-05-01|
|Vulnerability Response Integration with Tenable|5.0.3|2025-05-01|
|Vulnerability Response Integration with Veracode|4.6.2|2025-03-12|
|Vulnerability Response Licensing and Usage|2.9.1|2026-01-20|
|Vulnerability Response Mobile|11.1.1|2023-05-04|
|Vulnerability Response Patch Orchestration|2.2.5|2025-05-01|
|Vulnerability Response Patch Orchestration with HCL Bigfix|1.3.0|2025-05-01|
|Vulnerability Response Patch Orchestration with Microsoft SCCM|2.3.1|2025-05-01|
|Vulnerability Solution Management|10.4.3|2022-12-01|
|Walk-up Experience for Service Operations Workspace|7.1.5|2025-12-11|
|Watershed integration for ESG|16.0.1|2023-02-02|
|WDF Tokenization|2.0.2|2025-12-11|
|Web Components for Customer Service|4.0.1|2025-07-31|
|Whats New Framework Core|1.2.3|2025-07-31|
|WHOIS Integration for Security Operations|10.4.0|2024-08-01|
|Word Document Templates|1.10.0|2026-06-16|
|Workday ESG integration|16.0.3|2023-02-02|
|Workday Financials Spoke|2.0.2|2023-09-20|
|Workday HR Spoke|2.6.0|2025-03-12|
|Workday Learning Spoke|1.1.4|2024-04-04|
|Workflow Data Fabric Hub|2.2.1|2026-01-20|
|Workflow Studio|28.4.1|2026-05-05|
|Workforce Optimization Common|1.8.0|2026-03-12|
|Workforce Optimization Configurable Workspace Core|1.11.2|2026-03-12|
|Workforce Optimization Configurable Workspace UI Components|4.5.0|2026-03-12|
|Workforce Optimization for CSM Configurable Workspace|4.3.3|2025-05-01|
|Workforce Optimization for Field Service|6.0.3|2025-07-31|
|Workforce Optimization for HR|1.1.0|2024-08-01|
|Workforce Optimization for ITSM Configurable Workspace|2.9.0|2026-05-05|
|Workforce Optimization integration with Microsoft Outlook|1.4.0|2026-03-12|
|Workfront Spoke|1.2.0|2024-11-07|
|Work Item Integrations Common|1.15.0|2026-06-16|
|Workplace Core|2.28.1|2026-06-16|
|Workplace from Facebook Spoke|4.1.2|2023-09-07|
|Workplace Indoor Map Component|1.1.1|2024-08-01|
|Workplace PPE Inventory Management|1.17.0|2024-11-07|
|Workplace Service Delivery Integration with Mappedin|1.11.3|2024-11-07|
|Work Progress Status for Agile Teams|1.0.2|2023-05-04|
|Work Progress Status for SAFe|1.0.2|2023-05-04|
|Work Scheduler for Workforce Optimization|3.3.2|2026-03-12|
|Workspace App Shell|28.0.10|2026-05-05|
|Workspace Builder for App Engine|27.2.2|2025-05-01|
|Workspace Inspector|20.1.1|2025-05-01|
|Workspace navigation and experience demo|27.0.1|2025-07-31|
|Wrike Spoke|1.2.0|2025-05-01|
|X Spoke|2.2.1|2025-03-12|
|YouTube Spoke|1.0.4|2023-08-03|
|Zendesk Spoke|1.7.1|2025-06-05|
|Zero Copy Connector for ERP|10.0.9|2026-05-05|
|Zoom extension for Omnichannel Callback|1.3.5|2025-05-01|
|Zoom Spoke|4.2.0|2025-03-12|

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)


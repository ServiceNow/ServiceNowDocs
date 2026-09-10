---
title: Zurich Patch 11
description: The Zurich Patch 11 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-11.html
release: zurich
topic_type: reference
last_updated: "2026-07-09"
reading_time_minutes: 89
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 11

The Zurich Patch 11 release contains important problem fixes.

-   **Zurich Patch 11 was released on July 09, 2026.**
    -   Build date: 07-03-2026\_2048
    -   Build tag: glide-zurich-07-01-2025\_\_patch11-06-18-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z11.00.xlsx).

## Overview

Zurich Patch 11 includes 355 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-zp11.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Zurich Patch 11 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 11, refer to [KB3091782](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3094782).

## Changes in Zurich Patch 11

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
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

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

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)


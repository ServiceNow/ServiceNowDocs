---
title: Zurich Patch 10
description: The Zurich Patch 10 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-10.html
release: zurich
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 106
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 10

The Zurich Patch 10 release contains important problem fixes.

-   **Zurich Patch 10 was released on June 16, 2026.**
    -   Build date: 06-12-2026\_2311
    -   Build tag: glide-zurich-07-01-2025\_\_patch10-05-22-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z10.00.xlsx).

## Overview

Zurich Patch 10 includes 357 problem fixes in various categories. The chart previous shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-zp10.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Zurich Patch 10 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 10, refer to [KB3046592](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3046592).

## Changes in Zurich Patch 10

-   **[Authentication factors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/authentication-factors.md)**

    Authentication factors help identify and verify callers, allowing only authorized users to access AI voice agents on the ServiceNow AI Platform.

-   **[Explore authentication factors for AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/explore-authentication-factors.md)**

    Email OTP delivers a temporary numeric code to the caller’s registered email address. It is easy to deploy and familiar to most users. Callers can enter the code via keypad or by speaking the digits. Email OTP is susceptible to email account compromise and phishing, and should not be used as a standalone factor for sensitive operations.

-   **[Configure authentication factors for AI voice agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/authentication/configuring-authentication-factors-for-ai-voice-agents.md)**

    To secure voice agent environments, configure authentication factors that first identify the caller, then authenticate them before granting access.

-   **[Theming for AI Search in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/service-portal/ais-sp-css-vars.md)**

    The default value for the background color for title highlights in search results is transparent.


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

Database Persistence - Data Access

 PRB2007256

 [KB2925734](https://hi.service-now.com/kb_view.do?sysparm_article=KB2925734)

</td><td>

The text search doesn't return results in non-English languages

</td><td>

After downloading language plugins and switching the system language to a non-English language, results aren't returned when the property 'glide.db\_query.replace \_distinct\_with\_groupby' is set to 'false.' When the language is set to English, results are returned.

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

Related Lists

 PRB2025356

 [KB3032264](https://hi.service-now.com/kb_view.do?sysparm_article=KB3032264)

</td><td>

User can't add records in a related list because of the strict ACL check and missing ACLs for required roles

</td><td>

Users with missing ACLs aren't able to add new records in the related list due to a strict ACL check.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Request Management

 PRB1973824

 [KB2815909](https://hi.service-now.com/kb_view.do?sysparm_article=KB2815909)

</td><td>

Added approvers names don't appear on the Approver list of Request and RITM

</td><td>

When adding approvers to a Request \(REQ\) or Requested Item \(RITM\) via the Multi-Row Add \(MRA\) component in the 'Related Records' section of Service Operations Workspace \(SOW\), a success message is displayed confirming that the approvers have been added. However, the Approver list doesn't display the newly added approver names. Similarly, when attempting to add approvers from the UI16 related list, the approvers aren't added.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2007255

 [KB3045151](https://hi.service-now.com/kb_view.do?sysparm_article=KB3045151)

</td><td>

There's memory pressure on nodes due to high memory for the cache 'com.glide.cs.qlue.module. coma.MessageBatchingSession'

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

Access Control

 PRB1892720

</td><td>

'Applies to' in the Deny Unless Read ACL doesn't work for users with elevated privileges

</td><td>

It always returns true for any record for users with elevated privileges.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2005727

</td><td>

Navigation fails for sources beyond sliding windows in an activity stream

</td><td>

When selecting a citation source in an incident summary response, navigation doesn't work properly if the cited activity \(comment or email\) is more than three pages away or before the current activity stream view. The user receives a message stating 'The source may be hidden in your current view', even though the source exists and isn't filtered.

</td><td>

1.  Navigate to any instance on track/anowassist.
2.  Open Service Operations Workspace.
3.  Open a record with 200+ activity stream entries.
4.  Scroll to a recent AI-generated response containing citation references.
5.  Select **Show sources**. The cited source \(comment/email\) should be an older entry — at least 3+ pages before the current viewport.
6.  Select the citation link with worknotes/comments.

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

 PRB2018487

</td><td>

A citation URL is retained and fields are highlighted when a user logs in to an instance again

</td><td>

 

</td><td>

1.  Navigate to any instance with the 'Record Summarization' skill activated.
2.  Open any incident in Workspace.
3.  Ensure that the activity stream has several entries for the 'Record Summarization' skill to pick up.
4.  Run the 'Record Summarization' skill.
5.  Select a citation source that points to an activity stream entry.
6.  Log out of the instance.
7.  Log back in to the instance and return to the same record.

 Expected behavior: The citation URL shouldn't be preserved after triggering the citation source flow.

 Actual behavior: The URL that is created after selecting a citation source is preserved, and causes the citation scroll and highlight to trigger.

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

 PRB2033885

</td><td>

A new activity comment has the type as 'Field changes' instead of 'Comments'

</td><td>

 

</td><td>

1.  Open any incident in UI16.
2.  Post a comment.

 Note that the comment type \(top right of tile\) is 'Field changes \[dot timestamp\]' instead of 'Comments \[dot timestamp\]'.

</td></tr><tr><td>

Agent Chat

 PRB1943203

</td><td>

When hovering through the response templates, the preview is obstructed/hidden behind the case form

</td><td>

The response templates are obstructed in the header.

</td><td>

1.  Open an instance on a Safari browser.
2.  Open the same instance in the incognito window of Safari or in a new window on a Chrome browser.
3.  Request a live agent chat from a virtual agent \(for example, through the ESC portal\).
4.  Accept the chat as an agent in the SOW/HR Agent Workspace \(keep the plugins on the latest version for workspace\).
5.  Resize the browser window to be small.
6.  Type /r to open the response template.
7.  Hover through the response templates.

 Observe that the preview is obstructed/hidden behind the case form.

</td></tr><tr><td>

Agent Chat

 PRB2000390

</td><td>

The date format is incorrect in the Active Chat window

</td><td>

The date/time format is displayed as 'MMM DD, YYYY HH:MM a.m.' instead of 'DD-MM-YYYY HH:MM:SS' in the Active Chat window.

</td><td>

1.  Enable the conversation history by navigating to **Conversational Interface** &gt; **Agent chat settings**.
2.  Set the value for 'Number of conversations to display'.
3.  Navigate to an instance where Advanced Work Assignment \(AWA\) is configured in two browsers.
4.  Log in as Abel Tuter.
5.  Set the date/time preference to 'DD-MM-YYYY HH:MM:SS'.
6.  Initiate a chat from the portal.
7.  Connect to a live agent.
8.  Log in as an agent.
9.  Accept the chat.
10. Close the conversation.
11. Initiate a new chat.
12. Connect to a live agent.
13. Accept the chat as an agent.

Observe that the previous chat conversation is visible in the Active Chat window.


 Expected behavior: The date/time format should display as 'DD-MM-YYYY HH:MM:SS' at the top of the Active Chat window.

 Actual behavior: The date/time format is displayed as 'MMM DD, YYYY HH:MM a.m.' in the Active Chat window.

</td></tr><tr><td>

Agent Chat

 PRB2012130

</td><td>

There's a misleading VA Message while agent connection is still in progress

</td><td>

Before the agent accepts the workItem, there's a VA Message that says 'Live Agent Engaged'.

</td><td>

Connect to LA.

 Observe that the VA Message says 'Live Agent Engaged' before the agent accepts the workItem.

</td></tr><tr><td>

Agent Chat

 PRB2013475

</td><td>

LA conversation ends when sys\_prop is set to empty

</td><td>

When sys\_prop is deleted, the off-Glide LA topic is still called for LA transfer.

</td><td>

Scenario 1:

 1.  Create the sys\_prop, but leave the value as empty.
2.  Connect to LA.

 Observe that the conversation ends.

 Scenario 2:

 1.  Delete the sys\_prop.
2.  Start a LA topic.

 Observe that the off-Glide LA topic is still called for LA transfer, even when sys\_prop is deleted.

</td></tr><tr><td>

Agent Chat

 PRB2013947

</td><td>

Inbox Advanced Work Assignment \(AWA\) interactions aren't presented according to the **Configuration** field and order for the walkup experience

</td><td>

When an agent receives multiple chats in Service Operations Workspace \(SOW\), they are initially displayed in descending order, with the most recent chat at the top. However, after a refresh, the chat order appears to change and seemingly displays in a different order.

</td><td>

1.  Open an instance.
2.  Impersonate an agent with the role 'system\_administrator'.
3.  Open SOW.
4.  Set the agent status as 'available'.
5.  Open the instance again in new incognito tab, or in any another browser.
6.  Initiate 4-5 live agent chats by impersonating the end users from service portal.
7.  Check the order of the chats the agent received.

Notice that it would be in descending order, with the most recent chat appearing first.

8.  Refresh the page as an agent.

 Notice that the chat order is jumbled in a different order.

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
3.  Ensure that there's many closed interactions \(more than 100\) for Abel Tuter.
4.  Check the server memory in /stats.do.
5.  Start a new conversation as Abel Tuter.
6.  Accept the work item as Beth Anglin.
7.  Ensure that the history shows in the agent chat.
8.  Check the server memory again in /stats.do.

 Observe that the server memory has gone up significantly.

</td></tr><tr><td>

Agent Chat

 PRB2021490

</td><td>

Enhance the chat desktop notification

</td><td>

When the user selects the new chat message desktop notification, they should get focused back on the workspace tab. The workspace tab that the new chat message belongs to should also be focused and opened.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2022900

</td><td>

AWA workItem responder changes

</td><td>

Update WorkItemResponder's onEnter and OnExit to add and remove notifications in the ui\_notification\_inbox table. Also, create a system property \(glide.awa.work\_ item.notifications.enabled\) to determine whether to show or hide user preference at the agent level.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2022906

</td><td>

Add user preference for app shell notifications

</td><td>

Add support to display a new user preference 'Inbox Workspace Notifications' based on the system property glide.awa.work\_ item.notifications.enabled.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2022911

</td><td>

Polaris app shell changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2023682

</td><td>

Add the interaction number to desktop notifications to differentiate between interactions

</td><td>

The desktop notification should contain the IMS number to indicate which chat the notification is for.

</td><td>

1.  Enable desktop notifications in the agent workspace.
2.  Start a live agent chat so that a new desktop notification is rendered.

 Expected behavior: The desktop notification contains the IMS number to indicate which chat the notification is for.

 Actual behavior: The desktop notification only says that a new chat arrived.

</td></tr><tr><td>

Agile Development

 PRB2022589

</td><td>

Add 'None' choice to the **rm\_epic.status** field and make it the default for new epics

</td><td>

The **Epic Status** field \(rm\_epic.status\) currently doesn't include a 'No status' option, which prevents epics from having an unset/neutral status. This causes ambiguity in reporting and makes it difficult to distinguish between epics that have not yet been assigned a status vs. those intentionally marked as green, yellow, or red.

</td><td>

1.  Navigate to **Agile Development** &gt; **Epics** \(or open an Epic from a board/backlog\).
2.  Open any active Epic record
3.  Select the **Status** field.

 Expected behavior: 'No status' is available as a selectable option to represent epics with no status assigned, enabling accurate status transition tracking for usage analytics.

 Actual behavior: 'No status' isn't available as an option in the **Status** field list. Available options are limited to green, yellow, and red.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1997916

</td><td>

There's an extra 'response' layer in the JSON input passed by the agent to a scripted tool, causing performance issues

</td><td>

The final tool of creating the regulatory change tasks expects the input to be in the format - \{ 'finalPlan\_json': \{...\}, 'finalPlan\_html': '...' \}. But with the latest code, one 'response' layer is added, which causes performance issues.

</td><td>

Scenario 1:

 1.  Log in to an instance.
2.  Navigate to **/now/risk/compliance/record/sn\_grc\_reg\_change\_regulatory\_feed**.
3.  Open a record.
4.  Navigate to **AskNowAssist** &gt; **Get action oplan**.
5.  Select **Yes** after the action plan is displayed.

 Notice that number of regulatory tasks in the related list doesn't change. Tasks aren't being created.

 Scenario 2:

 1.  Create a skill tool that outputs a JSON object.
2.  Create a script tool that takes the skill output JSON as input.
3.  Return that input as is for displaying in VA.

 Expected behavior: The JSON object returned by the skill tool should display in VA.

 Actual behavior: The JSON object will be wrapped/contained in a format like this: \{ response: \{ model\_output: 'actual JSON object' \}\}.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2011068

</td><td>

Data to Glide from off-Glide isn't getting logged with the actual user

</td><td>

Any record update or creation doesn't have the created\_by or updated\_by set as the actual user.

</td><td>

Make a set cache call to Glide from off-Glide.

 Observe that any record update or creation doesn't have the created\_by or updated\_by set as the actual user.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2018916

</td><td>

AI Agent execution fails with 'Tool access denied' for triggering user after the update set migration

</td><td>

After migrating AI Agents \(built in Agent Studio\) from a development environment to a client test environment via update set, the agents fail to execute. The triggering user receives an error indicating that they don't have access to the agent's tools, and the agent never starts.

</td><td>

1.  In a source instance, build an AI Agent in Agent Studio with one or more tools \(for example, a subflow tool\).
2.  Configure the agent's ACL to allow any authenticated user to trigger.
3.  Configure the agent's dynamic user with the snc\_internal role.
4.  Verify the agent runs successfully end-to-end in the source instance.
5.  Capture the agent, its tools, ACLs, and dynamic-user configuration in an update set.
6.  Move the update set to the target instance.
7.  Commit it.
8.  As any authenticated user on the target instance \(admin or otherwise\), trigger the agent.

 Observe that the agent fails to start. An error states that the triggering user doesn't have access to the agent's tools.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2022336

</td><td>

Caching improvements for NextWave architecture

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2022344

</td><td>

Java changes for conversation history support for a Knowledge Graph tool in AI Agent Studio

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2022649

</td><td>

AI Agents are stuck indefinitely and the facts response is empty

</td><td>

When running AutoEval for the Enterprise Architecture Explorer – Query Agent, the evaluation run gets stuck indefinitely while processing certain questions and datasets. During execution, AutoEval doesn't progress to completion, progress keeps retrying without advancing, and the run never completes successfully. GenAI logs repeatedly show: 'JSON\{ 'facts': \[\]\}Show more lines'. Despite retries, no new facts are generated and the evaluation pipeline makes no forward progress.

</td><td>

1.  Navigate to **Now Assist Skill Kit** &gt; **Evaluation Results Dashboard**.
2.  Start an AutoEval run for:
    -   Agent: Enterprise Architecture Explorer – Query Agent
    -   Dataset containing multiple evaluation questions
3.  Allow the run to process.

 Observe that the evaluation stalls on certain questions, AutoEval keeps retrying internally, and the run never completes.

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

The OffGlideScriptObject. generateAuthorizationInfo API creates JSON Web Tokens \(JWT\) with current session users

</td><td>

The API sn\_cs\_offglide.OffGlideScriptObject .generateAuthorizationInfo\(\) creates JWT with current user sessions, even though the userID value is passed in the request.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2025974

</td><td>

User session is logged out when opening AI-generated interaction records

</td><td>

The user session is logged out when opening AI-generated interaction records that were created/updated by the incident\_intelligence\_agent. The interaction record remains in the WIP state, even though the associated conversation has been marked as faulted. The issue is specific to the in Service Operations Workspace view, as opening the same record in platform view works without issue.

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

AI Experience Framework - Glide

 PRB2015131

</td><td>

Turn on UI validation for 'Record Update' and 'Create Agent'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2018366

</td><td>

/api/now/aiux\_service/sysprops doesn't enforce an allowlist

</td><td>

 

</td><td>

 

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

 PRB2027126

</td><td>

AIX Webserver Glide integration

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2027128

</td><td>

Migration in Glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Gateway - Security

 PRB2024062

</td><td>

AI Gateway security Q2 complete feature update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2001677

</td><td>

A Knowledge Graph \(KG\) NLQ call should pass the caller ID in the **Caller** field, not meta

</td><td>

 

</td><td>

In an instance with KG, navigate to 'Make a kgnlq query'.

 Observe one\_api\_service\_ plan\_feature invocation. It doesn't match the design with respect to the **Caller** field.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2002346

</td><td>

When a KB only has an embedded KBB with embedded\_match = false, the KB should send itself instead of the KBB

</td><td>

The KBB content is sent to the LLM instead of KB.

</td><td>

1.  Create a KB titled 'abc' with some text content and an embedded KBB 'defhi'.
2.  Perform a search for 'abc' in the search preview with the 'Now Assist in VA' profile in sys\_generative\_ai\_log.

Observe the KB sent to LLM.


 Expected behavior: The content of the KB is sent to LLM.

 Actual behavior: Only the KBB content \(defhi\) is sent to the LLM.

</td></tr><tr><td>

AI Search for Service Portal

 PRB2023882

</td><td>

The 'View all results' option isn't available in the chat response shared by assistant

</td><td>

 

</td><td>

1.  Open an instance.
2.  Impersonate the system admin.
3.  Navigate to /csm portal.
4.  Input 'How to repair fan fuse'.

 Expected behavior: The 'View all results' option is visible.

 Actual behavior: There is no 'View all results' option in the side panel bottom.

</td></tr><tr><td>

AI Search UX

 PRB1989246

</td><td>

When records are searched in global search, it isn't opening the form directly

</td><td>

When a user tries to search the incident number in the global search when the zoom size is 150% and left navigator is pinned, then the incident record isn't opening directly. It instead displays a search result page. However, when the zoom size is 100%, then the incident record is opening directly in a form page.

</td><td>

1.  Navigate to an instance where AI Search is turned on.
2.  Update the browser zoom to 150%.
3.  Pin the 'All' option in the filter navigator.
4.  Copy any incident number.
5.  Search with the incident number in the global search and press enter.
6.  See the search results page.

 Expected behavior: Users should see the incident form record directly.

 Actual behavior: Users are seeing the search results page.

</td></tr><tr><td>

AI Search UX

 PRB1991340

</td><td>

Search input intermittently skips characters

</td><td>

The search input intermittently drops characters when users type quickly, especially under a heavy event load.

</td><td>

1.  Open any workspace/heavy loaded page.
2.  In the global search, type quickly.

 Observe intermittent character loss.

</td></tr><tr><td>

AI Search UX

 PRB1994212

</td><td>

The hidden description in the source code is visible in the chatbot for 'Order guide' and not for 'Catalog item' in Now Assist Virtual Agent \(NAVA\)

</td><td>

On the catalog item, it's possible to hide the description using the following in the code source: '&lt;div style=''display: none;''&gt; TEXT TO HIDE.' When attempting to do the same in the order guide, it's not working properly in the chatbot, and both texts are visible. This issue occurs only on the chatbot preview of the order guide, and not when consulting it directly from portal.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1998976

</td><td>

Search event records don't indicate the search mode \(keyword, hybrid, or semantic\)

</td><td>

When a search is executed in an AIS-enabled portal with Hybrid Search enabled on the corresponding search application, the resulting sys\_search\_event and sys\_search\_signal\_event records don't capture the search mode \(keyword, hybrid, or semantic\) that was used to execute the query. This makes it impossible to distinguish query types in search analytics and signal data.

</td><td>

1.  Turn on Hybrid Search on a Search auto-complete Configuration \(SAC\).
2.  Navigate to a Dynamic Window-enabled portal that uses the configured SAC.
3.  Perform a search in the portal.
4.  Open the corresponding sys\_search\_event and sys\_search\_signal\_event records generated by the query.

 Observe that neither record contains any field or indicator specifying the search mode used \(keyword, hybrid, or semantic\).

</td></tr><tr><td>

AI Search UX

 PRB2005193

</td><td>

Exact Match, when configured to honor conditions of search sources, should be configurable for a single application and not the entire instance

</td><td>

A system property called glide.search.exact\_match \_use\_search\_source\_filter enables all applications on the instance with exact match limited to those tables included in a search source and honors the conditions set within them. Users don't expect this feature to be enabled at the instance level, but require it to be enabled at the application level.

</td><td>

Set the system property glide.search.exact\_match\_use\_search\_source\_filter to true.

 Notice how setting this property to true applies to all search applications. Instead, it should be enabled/inactive for a single application.

</td></tr><tr><td>

AI Search UX

 PRB2006060

</td><td>

Now Assist AI Search summary links \(catalog item references\) are non-functional, but appear active due to the text styling

</td><td>

When a user performs an AI Search on Employee Center/Employee Service Center, the generated summary contains functional reference links to catalog items. When the user selects **Ask a follow-up**, the AI Search summary is copied into the Virtual Agent \(VA\) chat window. The catalog item reference links within a copied summary in VA are non-functional, which is expected. However, they still appear active due to the text styling. Instead, they should appear faded and the link pop-up shouldn't be displayed.

</td><td>

1.  Log in to an ESC/EC portal.
2.  In the search bar, enter a query that triggers an AI Search summary with catalog item links \(for example, 'I would like to order hardware' or 'reset password'\).

In the AI Search generated summary, observe that the reference links to catalog items are functional.

3.  Select **Ask a follow-up**.

Observe that the AI Search summary is copied into the Virtual Agent \(VA\) chat window.

4.  In the VA chat window, select any of the catalog item reference links.

 Observe that the links are non-functional, but they appear active due to the text styling. A pop-up is also displayed.

</td></tr><tr><td>

AI Search UX

 PRB2011697

</td><td>

RAG popular search suggestion reader doesn't consider sys\_rag\_search \_suggestion.active

</td><td>

The sys\_rag\_search\_suggestion records with active=false are still returned.

</td><td>

1.  Generate sys\_rag\_search\_suggestion entries.
2.  Query the Suggestion API.

 Observe that the sys\_rag\_search\_suggestion records with active=false are still returned.

</td></tr><tr><td>

AI Search UX

 PRB2014138

</td><td>

$sp-search-result-title- highlight--background-color in sp-variables.scss

</td><td>

There is no default assigned for variabl '$sp-search-result-title- highlight--background-color'.

</td><td>

1.  Log in to Portal with AI search enabled.
2.  Search for 'laptop' and navigate to the AI search page.

 Notice that the variable '--search-result-title- highlight--background-color: $sp-search-result-title- highlight--background-color;' is not resolved.

</td></tr><tr><td>

AI Search UX

 PRB2016024

</td><td>

Synthesized responses on a mobile sized screen don't show 'Show full answer' after truncation in Zurich on Safari

</td><td>

The answer is truncated without the option to expand: 'Show full answer'.

</td><td>

1.  Find a Zurich instance with Multi Content Synthesized GRs working in Portal that can work on Safari mobile browser.
2.  Search for a term that would yield a Synthesized GR.

 Observe that the answer is truncated without the option to expand: 'Show full answer'.

</td></tr><tr><td>

AI Search UX

 PRB2021873

</td><td>

Facets aren't rendered as the sensitivity filter fails quietly

</td><td>

Facets aren't returned because of a failure to fetch hasMatch.

</td><td>

1.  Make sure the Now Assist setup isn't done.
2.  Make sure the sensitivity filter is null.

 Observe that facets aren't returned as a result of before line failing to fetch hasMatch.

</td></tr><tr><td>

AI Search UX

 PRB2024551

</td><td>

New/different experience in the search when AI Search is turned on in the portal level

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Impersonate as system admin.
3.  Navigate to /csm portal.
4.  In search bar, search 'Controllers and applications'.

 Observe that there's no follow up and articles displayed are shown previously in the enhanced chat.

</td></tr><tr><td>

AI Search UX

 PRB2024704

</td><td>

RAG search signals aren't getting logged

</td><td>

After certain searches, the sys\_search\_event and sys\_search\_signal\_event records should be created. The response from the REST API call should have a signalsCorrelationData object on it. Instead, no records get created and no signalsCorrelationData is returned.

</td><td>

 

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

 PRB1844011

</td><td>

Using 'Trend by week' leads to an incorrect record count when the new year starts

</td><td>

When using 'Trend by' with the options 'Opened', 'Calendar', 'Standard Calendar' and 'per-week' and running the report, the record count is 3 but the List view record count is 5.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1919741

</td><td>

Calendar API doesn't accept requests from external users

</td><td>

The following message appears: 'message': 'External User Not Authorized'.

</td><td>

1.  Provision an instance with the plugin 'com.glide.explicit\_roles' installed.
2.  Open a record for the user 'Abel.tuter'.
3.  Replace Abel.tuter's current role with 'snc\_external'.
4.  Set a new password for Abel.tuter.
5.  Using Postman or any other tool, make a request using the credentials from step 4.

 Expected behavior: The user is able to make the request.

 Actual behavior: The following message appears: 'message': 'External User Not Authorized'.

</td></tr><tr><td>

Analytics Data API

 PRB1928857

</td><td>

The maximum number of groups on the heat map visualization in Platform Analytics resets to 10 when filtering

</td><td>

After saving and refreshing, the column count resets to 10. Instead, all selected groups should remain visible.

</td><td>

1.  Open an instance.
2.  Create a heatmap data visualization.
3.  Add a 'Group By' under Columns with more than 10 columns.
4.  Select **Apply.**

Observe that all columns display correctly at this point.

5.  Save and refresh the visualization or browser.

 Expected behavior: All selected groups remain visible after saving or refreshing.

 Actual behavior: The column count resets to 10 every time.

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

Analytics Data API

 PRB2005078

</td><td>

When using dynamic date ranges, appliedFilters returns incorrect dates

</td><td>

 

</td><td>

1.  Open UI Builder.
2.  Create a page.
3.  Add a data visualization component.
4.  Use the type, 'Line'
5.  Check the **Define Data Manually** toggle under 'Under data sources'.
6.  Copy and paste the 'defect response.txt' in the 'Data' section.

Notice that the chart is rendered, though no information from March is present.

7.  Edit the 'Data' section.
8.  Update the 'end' information in appliedFilters, from ''end':'2026-02-28' to ''end':'2026-03-31'.

 Notice that the data for March is now visible.

</td></tr><tr><td>

Analytics Data API

 PRB2006926

</td><td>

Geomap doesn't fetch locationData correctly when the incorrect query gets applied

</td><td>

Locations which have valid data in cmn\_location table aren't getting plotted. Every valid location should get plotted correctly.

</td><td>

1.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Dashboards**.
2.  Create a dashboard.
3.  Add a Geomap widget based on the \[sys\_user\] table with the following configuration:
    -   Metric: Count
    -   Group by: 'Location'
4.  Save the dashboard.
5.  Exit 'Edit' mode.

 Observe that the created Geomap widget doesn't render all the data points and shows an error: 'Some of the data you selected can't be visualized on the map due to latitude/longitude mapping errors'.

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

Analytics Export API

 PRB2019202

</td><td>

Show the total row count in the analytics list

</td><td>

The list-simple property 'hideTitleRowCount' should migrate to showRecordCount in the new analytics list.

</td><td>

1.  In Yokohama, create a list-simple visualization.
2.  Change the **Hide total number of records** toggle switch in the configuration.
3.  Save the visualization.
4.  Upgrade the instance.
5.  Open the same visualization.

 Observe that it doesn't migrate to the new list visualization and have the corresponding property set for showing count.

</td></tr><tr><td>

Analytics Export API

 PRB2023200

</td><td>

Hide the export option when it's inactive or the roles list is empty

</td><td>

The system provides export on demand functionality at dashboard and data visualization level \(server-side\) for the Next Experience. There is a need to control the availability of the export option based on system properties and user roles.

</td><td>

1.  As the system administrator, configure a system property to enable or disable the export feature.
2.  Make sure the export feature is enabled.
3.  Configure a second system property with a comma-separated list of roles that are allowed to use the export feature when it is enabled.

 Observe the system checks if the user's role is included in the configured list of roles \(if the list is not empty\). If the second system property \(roles list\) is empty, the export feature is available to all users when enabled. If the second system property \(roles list\) is populated, only users with roles in the list can access the export feature.

</td></tr><tr><td>

Application Manager

 PRB1995859

</td><td>

KMF key isn't copied to the target instance during the clone, causing encrypted app attachment decryption failure and store re-download fallback

</td><td>

After cloning an instance, the target instance fails to decrypt the encrypted app ZIP attachments. This happens because the KMF key used on the source instance isn't copied to the target during the clone. The target instance falls back to re-downloading and re-encrypting every installed app from the ServiceNow App Store, causing extended startup times, node timeouts, and degraded instance availability.

</td><td>

1.  Provision a source instance \(sub-prod\) with one or more apps installed, so that the encrypted app ZIP attachments exist in sys\_attachment.
2.  Clone the source instance to a target instance.
3.  Start the target instance after the clone completes.
4.  Check the instance startup logs.

 Observe that there are repeated re-download attempts for apps already installed on the source. Also, the decryption of app ZIP attachments fails on the target \(KMF key from source is not present on target\). Finally, enroll\_module\_for \_resource\_exchange is false on the com\_glide\_snc\_app\_client KMF crypto spec.

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

 Actual behavior: The save is blocked with the error: 'A Business Application exists with the same name. Please verify.'

</td></tr><tr><td>

Appointment Booking

 PRB1961234

</td><td>

Future maximum bookable days are inconsistent when the time is 8:58AM in JST and 9:00AM in JST

</td><td>

The issue is caused by the internal time zone conversion logic. JST 19th Aug 08:58 a.m. converts to GMT 18th Aug 11:58 p.m.. Since GMT is behind JST, slots for September 18th aren't shown \(the future maximum only reaches September 17th\). However, JST 19th Aug 08:00 a.m. converts to GMT 19th Aug 12:00 a.m.. Future maximum days are added on GMT, and slots for September 18th appear.

</td><td>

 

</td></tr><tr><td>

Asset Management

 PRB2018791

</td><td>

The navigation filter isn't applied correctly

</td><td>

The relevant filter should be automatically applied after navigation.

</td><td>

1.  Navigate to Software Asset Workspace.
2.  Open the 'Software Asset Overview' page.
3.  In the 'Activity Center' section, select the **Asset Request** link.

Observe the navigation to the target page.

4.  Verify whether the expected navigation filter is applied.

 Expected behavior: The relevant filter is automatically applied after navigation.

 Actual behavior: The filter isn't applied.

</td></tr><tr><td>

Authentication Factors

 PRB2026011

</td><td>

Introduce a new MFA factor, Email OTP

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2026012

</td><td>

KBA improvements of Platform capabilities

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2026014

</td><td>

KBA session context persistence

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2026015

</td><td>

NextWave AI authentication migration to a new authentication service

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

Automated Test Framework \(ATF\)

 PRB2022891

</td><td>

MVP - UI test script \(Testing Library\) test step in ATF for UI testing

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1983139

</td><td>

Approval records aren't created when creating a HR case

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Assign some manager \(for example, system admin\) to Abel Tuter.
3.  If the HR service is inactive, activate it.
4.  Create a HR case for the 'Request Personal Information Report' service.

 Observe that the approval record isn't created.

</td></tr><tr><td>

Change Management

 PRB1994240

</td><td>

Translation issues in the Conflict Checker Progress modal window

</td><td>

Translation issues were observed after upgrading from Yokohama to Zurich. The 'conflict\_detection' header appears to be missing the message completely when it previously read 'Conflict Detection'. The message 'The conflict check is complete' is translated into Finnish, even when the user's language is in English. This issue also occurs when the instance language is set to French, and the label is translated in English.

</td><td>

1.  Open a Zurich instance.
2.  Ensure the instance is set to the English language.
3.  Open a Change record.
4.  Select the **Check Conflicts** button in the 'Conflicts' tab.

 Notice that the progress bar title displays as 'conflict\_detection' and the value is shown rather than the label, 'The conflict check is complete'. The label is translated in Finnish even though the user's instance language is set to English.

</td></tr><tr><td>

Code Signing

 PRB2014768

</td><td>

Increase the code signing validity window maximum from 60 minutes to 4 hours

</td><td>

In the 'Scan Signatures' module, the **Data source** field is incorrectly set to false for records that have valid, successfully created signatures. These signatures return true when validated via a background script. The issue occurs because the effective maximum of com.snc.kmf.signature .validity\_window is 60 minutes, which prevents users from configuring longer validity windows, especially when the consecutive signature generation takes time.

</td><td>

1.  Open an instance.
2.  Navigate to 'Update Set: Test Code Signing Updates'.
3.  Validate that the signature is created for the **Data source** field.
4.  Select **Scan Signature**.

 Observe that the signature state for the **Data source** field still reflects as false.

</td></tr><tr><td>

Code Signing

 PRB2014831

</td><td>

Scheduled scripts incorrectly appear in 'Update Set Signature States'

</td><td>

Currently, users are required to hold the security\_admin role to perform code signing operations on update sets. This creates several operational and security challenges. Instead, there should be a separate role that grants the ability to perform code signing operations on update sets and related artifacts within the Code Signing framework. It shouldn't grant access to security policies, ACLs, encryption contexts, or other security administration functions.

</td><td>

1.  Open an instance.
2.  Navigate to 'Update Set: Code Signing Scheduled Jobs'.
3.  Navigate to the tab 'Update Set Signature States'.

 Observe that there's no option to run signing jobs unless elevated to the 'security\_admin' role.

</td></tr><tr><td>

Code Signing

 PRB2014833

</td><td>

Enable digest creation for users with the code signing role

</td><td>

For users with the code\_signing\_user role, the 'Create Digest' functionality should be enabled for Flow Designer flows and actions. The current dependency on the security\_admin role should be removed.

</td><td>

1.  Open an instance.
2.  Navigate to 'Update Set: Code Signing Scheduled Jobs'.
3.  Navigate to the tab 'Update Set Signature States'.

 Observe that the user can't generate digest for flows unless they have the 'security\_admin' role.

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

Configuration Management Database \(CMDB\)

 PRB1923632

</td><td>

CMDB Health Correctness group score doesn't consider inclusion rules when computing health score

</td><td>

The CMDB Health correctness group score is incorrect because the parent metric doesn't consider the inclusion rules. The code in the correctness manager that would return the health inclusion rule for the class is missing. It works correctly for other metrics \(for example, completeness and conformance\).

</td><td>

 

</td></tr><tr><td>

Connections and Credentials

 PRB2007222

</td><td>

AuthMetadataProvider .getAliasInfoList\(\) performs unfiltered full-table scan on sys\_alias \(29,000+ rows\)

</td><td>

This causes QueryWarning and excessive DB load. The same behavior occurs via any code path that calls PersonalAuthClient .getAuthCredentialInfo \(credentialId\).

</td><td>

1.  Open an instance with many aliases in sys\_alias \(for example, 29,000+ records\).
2.  Trigger a flow that invokes sn\_cc.PersonalAuthAPI\(\) .getInitiatorURL\(aliasId\) with a valid alias ID.

 Observe that the following warning appears in the system logs: 'QueryWarning \*\*\* WARNING \*\*\* Large Table: Table handling an extremely large result set: 29180'. Additionally, observe that the info-level log for orphaned credential aliases contains 'can't find a credential with the given alias sys\_id...'

</td></tr><tr><td>

Connections and Credentials

 PRB2015199

</td><td>

An initiator URL isn't returned when the AT has expired and the record is present in oauth\_credential\_list

</td><td>

 

</td><td>

 

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

During content updates in the ITAM Content Library, many ais\_index events are generated for the sam\_sw\_product\_lifecycle \(SAM software lifecycle\) and sn\_hamp\_lifecycle\_definition \(HAM hardware lifecycle\) tables. These events appear in the event log. The excessive events are triggered because system metadata columns on the AI Search datasources for these two tables are missing the no\_text\_index field attribute. Without this attribute, the AI Search indexing engine includes these columns in the vector index.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1919872

</td><td>

There's duplicate edges in the output of jsFunction\_getEdgeList for custom created graphs and when includeEdgesForTables OutsideGraph is true

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1930279

</td><td>

Users can create a cyclic relation through graph hierarchy

</td><td>

 

</td><td>

1.  Create a graph.
2.  Name it test1.
3.  Create another graph with the parent as test1 \(with extension model\) and name it test2.
4.  Edit test1 to have a parent as test2 \(with extension model\).

 Notice that it creates a cyclic relation in graphs test2-parent-test1 and test1-parent-test2.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1946286

</td><td>

Workflow Data Fabric \(WDF\) queries fail when trying to execute on connection for trino\_primary

</td><td>

When trying to get a specific column instead of the entire record, the error occurs in the response: 'FAILED TRYING TO EXECUTE ON CONNECTION trino\_primary'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1962536

</td><td>

The prefix is missing in some places for the Knowledge Graph UI

</td><td>

 

</td><td>

1.  Navigate to **All** &gt; **Knowledge Graph Designer**.
2.  Select the **Open global graph** button.
3.  Select **Start with user table** &gt; **Any node**.

Note that the prefix is missing for some of the columns.

4.  Expend any node on canvas.

Note that the prefix is missing for expended nodes.

5.  Open the contribution graph.

 Note that the prefix is missing for all the nodes, columns, and relations.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1969193

</td><td>

SELECT isn't generated correctly for a script when a business rule is active with ORDER BY for Postgres

</td><td>

There's an error message: 'FAILED TRYING TO EXECUTE ON CONNECTION glide.1 \(connpid=3758451\): SELECT...'

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

Database Persistence - Graph

 PRB1923336

</td><td>

The isTableExcluded API should exclude text search tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1938573

</td><td>

A 'WHERE' clause appends all query node conditions with an 'AND' operator, even when there are 'OPTIONAL MATCH 'statements

</td><td>

When trying to a build cypher query for the following use case, 'Identify all CIs which are connected to Database catalog or Application', in the final built cypher query the 'WHERE' clause is using all 'AND' conditions to append all node filters to the query. When using 'OPTIONAL MATCH' statements, an 'OR' logic is expected.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1944327

</td><td>

Global graph should be the default and all other graphs should be non-default when the instance is upgraded from Yokohama to Zurich

</td><td>

Default graphs and Global graphs are all set to non-default.

</td><td>

1.  Create two default graphs on a Yokohama instance.
2.  Upgrade the instance to Zurich.
3.  Check the graphs on sys\_meta\_graph.

 Expected behavior: Global graph should have default = true and the other two graphs that were created in step one should have default = false.

 Actual behavior: Both of the created default graphs and the Global graph are default = false.

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

5.  Remove one of the conditions \(for example, Location Contains 'via'\).
6.  Rerun the query.

 Observe that results are now returned.

</td></tr><tr><td>

Database Persistence - Graph

 PRB1975732

</td><td>

There's a repeated query execution in GraphUtils \#getGraphByQualifiedName for a metadata child table \[sys\_meta\_graph\] for every iteration/execution

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1988516

</td><td>

Weeks, milliseconds, and microseconds aren't supported in a DURATION map

</td><td>

There's an error: 'com.glide.db. DBGraphApiException: Error executing cypher: FAILED TRYING TO EXECUTE ON CONNECTION...Syntax Error or Access Rule Violation detected by database \(ERROR: function duration\_between\(date, date\) does not exist tooltip: No function matches the given name and argument types. You might need to add explicit type casts. Position: 294\)'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1988520

</td><td>

TimeKeyExpression isn't supported as a DURATION function parameter in DBSqlParser

</td><td>

There's an error: 'Error: com.glide.db. DBGraphApiException: Error executing cypher: FAILED TRYING TO EXECUTE ON CONNECTION...Syntax Error or Access Rule Violation detected by database \(ERROR: function duration\_between\(timestamp with time zone, date\) does not exist Hint: No function matches the given name and argument types. You might need to add explicit type casts. Position: 307\)'.

</td><td>

 

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

 PRB1995712

</td><td>

Weeks, milliseconds, and microseconds aren't supported in the Duration map

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1996879

</td><td>

Guardrail for maximum number of edges returned from getForTables

</td><td>

The number of nodes returned from getForTables is capped to 1000, but there's no such limitation for the number of edges. When inbound edges are specified and the number of nodes is at maximum, the number of edges can be quite large.

</td><td>

Run getForTables for sys\_user with inbound edge flag = true.

</td></tr><tr><td>

Database Persistence - Graph

 PRB1997409

</td><td>

L2 query displays non-empty edge values

</td><td>

 

</td><td>

1.  Navigate to Query Builder.
2.  Drag the 'Database and Computer' class into the canvas.
3.  Connect them with the L2 relationship edge.

 Expected behavior: With the data, there should be two L1 relationships and three L2 relationships with the edge shown as '\(empty\)'.

 Actual behavior: The three L2 relationships have unexpected edge values.

</td></tr><tr><td>

Database Persistence - Graph

 PRB2007566

</td><td>

com.glide.db. DBGraphApiException has an error executing cypher

</td><td>

There's an error: 'This user \(admin\) is not allowed access to table: sys\_user\_has\_role'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2008809

</td><td>

Rename the ScopedGraphQueryBuilder .createNode method

</td><td>

To avoid potential confusion with createNode as a write operation, rename the 'createNode\(\)' method to 'node\(\)'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2020140

</td><td>

Union queries aren't supported

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2021889

</td><td>

GlideRecord.setCategory\(\) is used in a way that prevents routing to read-replica databases

</td><td>

The query is categorized as 'graphqueryexecutor' instead of 'cmdb\_queries', and therefore doesn't get routed to the read replica because the category isn't a second database category.

</td><td>

1.  Ensure the instance is set up with a read replica database.
2.  Ensure the CMDB Queries \(or all Secondary Database Categories\) are enabled and are mapped to the read replica.
3.  Execute a KG query from the CMDB Query Builder app.

 Expected behavior: The query is categorized as 'cmdb\_queries' and is routed to the read replica.

 Actual behavior: The query is categorized as 'graphqueryexecutor', and since that category isn't a secondary database category, is not routed to the read replica.

</td></tr><tr><td>

Database Persistence

 PRB1866305

</td><td>

DictionaryXMLParser rejects large table alters for Postgresql db based on MariaDB logic

</td><td>

 

</td><td>

1.  Create an instance on Postgresql with any table that has over 150M records \(for example, a table like sys\_journal\_field\).
2.  Update the sys\_journal\_field.xml to have a new string column.
3.  Upgrade the instance.

 Observe that the alter is rejected.

</td></tr><tr><td>

Data Management Console

 PRB1974031

</td><td>

A repeated query with the hash -423529530 comes up when running stats gatherer

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Snapshots

 PRB1999238

</td><td>

There's a node outage due to an out-of-memory error as a result of a memory bloat in ScriptableCDCDataCollector .jsFunction\_mineAllChanges\(\)

</td><td>

During the investigation, it was noticed via heapdumps that the com.snc.db.cdc. implementation. ReplicationTableReader object held an array list of size 500. Each entry in this array list held up to a max of 800 Glide record objects. The size of each of these 500 entries was ~21 MB. The Glide record objects were from the cmdb\_ci\_vm\_instance table. These were particularly heavy in terms of row size \(reaching ~400 KB\). The existing sizing must be revisited to take into account this outlier. In particular, in addition to a limit on number of rows to be polled from cdc\_queue\_par, it should also include a limit to cap the memory size.

</td><td>

1.  Create an 'All activity data snapshots' source on the em\_alert table.
2.  Run the 'Incremental all activity' job.
3.  Run the first snapshot job and let the first mining complete.
4.  Run the 'Incremental all activity' job.

 Notice the memory bloat in the worker thread running for the 'All changes' job.

</td></tr><tr><td>

Developer Sandboxes

 PRB1995018

</td><td>

NowMQ messages can be claimed by an unexpected recipient

</td><td>

If the user sets the App Operation Queue Health Monitor job to inactive, it should prevent the sandbox from claiming any application operation queue messages in sys\_nowmq\_message. On an instance without sandboxes, any messages that were left unclaimed or any newly added messages should still be claimable when the job is re-enabled.

</td><td>

1.  Make sure one controller and one sandbox are running.
2.  On the sandbox, set the App Operation Queue Health Monitor job to inactive.
3.  Enqueue an operation on the sandbox by initiating an app install from app manager or via /sn\_cicd/update\_set/commit.
4.  Navigate to sys\_nowmq\_message.

 Observe that the corresponding message from step 3 is unexpectedly gone. It should still be present but unclaimed as a result of step 2.

</td></tr><tr><td>

Developer Sandboxes

 PRB2011753

</td><td>

Sys\_flow\_trigger\_plan\_chunk is currently shared and causing updated flows to error out

</td><td>

If the user updates the base flow, the sandbox flow errors out with 'Compiled flow not found for snapshotId'.

</td><td>

1.  On a base instance, create a flow that is scheduled to run every minute.
2.  Navigate to **Flow Designer** &gt; **Operations** &gt; **Flow** &gt; **Today's execution**.

Observe that the flow is running successfully.

3.  Create a sandbox.
4.  In the sandbox, navigate to **Flow Designer** &gt; **Operations** &gt; **Flow** &gt; **Today's execution**.

Observe that the flow is running successfully.

5.  In the sandbox, update the flow.
6.  Select **Activate**.
7.  Navigate to the base instance.

 Observe that, under 'Today's execution', the flow starts erroring out with 'Compiled flow not found for snapshotId'.

</td></tr><tr><td>

Developer Sandboxes

 PRB2015080

</td><td>

The scheduled flow inherited from the main instance does not run automatically on the sandbox instance

</td><td>

The flow runs in main instance at the scheduled interval, but the flow doesn't run in the sandbox instance even though it exists.

</td><td>

1.  Open the main instance.
2.  Navigate to **All** &gt; **Flow Designer**.
3.  Create a flow.
4.  Schedule that flow to run at a certain interval, for example, 'Repeat every minute'.
5.  Activate the flow.
6.  Navigate to **All** &gt; **Flow Designer** &gt; **Operations** &gt; **Flows** &gt; **Today's executions**.

Notice that the flow is running every minute.

7.  Create a sandbox instance.
8.  Navigate to **All** &gt; **Flow Designer**.

Notice that the flow exists.

9.  Navigate to **All** &gt; **Flow Designer** &gt; **Operations** &gt; **Flows** &gt; **Today's executions**.

 Notice that the flow is not running.

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

 Actual behavior. The work is gone. Logs show jsFunction\_exportUpdateSets is called.

</td></tr><tr><td>

Developer Sandboxes

 PRB2018545

</td><td>

BA conversations are shared between sandboxes/base instance

</td><td>

The base instance conversation contains messages from the sandbox, and vice versa.

</td><td>

1.  Provision an instance with BA installed.
2.  Create a sandbox.
3.  From the base instance, open IDE or Studio.
4.  Start a conversation \(for example, 'What's 1+1'\).
5.  Visit the sandbox.
6.  Open IDE or Studio again.

Observe that the conversation already contains the messages from the base instance, even though it should be empty.

7.  Add another prompt in the sandbox.
8.  Refresh the base instance.

 Expected behavior: The conversation doesn't contain what was typed in the sandbox.

 Actual behavior: The conversation contains messages from the sandbox.

</td></tr><tr><td>

Discovery

 PRB1986211

</td><td>

Discovery.complete and discovery.canceled are triggered incorrectly

</td><td>

Discovery may trigger both discovery.complete and discovery.canceled events for the same status, and it may trigger discovery.canceled twice.

</td><td>

1.  Create or pick a cloud-resource discovery schedule configured to use a specific MID Server \(midSelMethod = 'specific\_mid'\).
2.  Ensure that the MID Server is in a state where validateMIDCondition\(\) returns false \(typically because the MID is down / not validated\).
3.  Run the schedule \(or trigger it via the Discover Now action\).

 Observe that discovery.canceled fires twice for the same status record. The StartDiscovery error log for 'Discovery canceled on previously started schedule ... due to mid not available' appears twice. Instead, there should be a single discovery.canceled event and a single error log entry per cancelled run.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB2018937

</td><td>

Local naively checks for empty text rather than 'empty' when classifying PDF pages for DocReader

</td><td>

The PDF page is classified as 'digital' instead of 'scanned' because it checks for empty text instead of a empty PDF page.

</td><td>

Call DocReader Local with a scanned PDF containing empty text, for example, '\\n\\n\\n'.

 Notice that the page is classified as 'digital' rather than 'scanned'.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB2029867

</td><td>

Users can configure more than 50 fields per use case, which does not match the product and pricing based limitations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Edge Encryption

 PRB1945424

</td><td>

There's high memory utilization on proxy servers after the Yokohama upgrade

</td><td>

After upgrading and running Yokohama, the memory consumption is over the limit set in wrapper.conf. The user set the memory limit for 10G in the wrapper.conf, but the edge proxy doesn't respect this setting in the build. The memory goes to the physical limit and causes the proxy server to restart.

</td><td>

 

</td></tr><tr><td>

Email Accounts

 PRB2022999

</td><td>

Add the capability to capture mailbox as part of headers

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB2006670

</td><td>

Push Notifications aren't sending the badge count

</td><td>

This issue occurs on mobile instances.

</td><td>

1.  Log in to a mobile instance.
2.  Fire a notification.

 Observe that the badge count isn't sent in the push payload.

</td></tr><tr><td>

Email Notifications

 PRB2022602

</td><td>

Client script include should be created to make client scripts modular and reusable

</td><td>

In Zurich, the wiring's not implemented for mini composer in CSM when activity stream compose isn't present.

</td><td>

1.  Update the 'glide.email\_client. configurable\_send\_enabled' value to 'sn\_customerservice\_case'.
2.  Make sure configuration is done.
3.  Log in as a user with elevated privileges.
4.  Navigate to CSM workspace.
5.  Open a case record.
6.  Ensure activity stream isn't present.
7.  Select **Compose Email** to open a modeless dialog.
8.  Add \[private\] in the **Subject** field.
9.  Add 'unknown user' in the **To** field.
10. Select the **Send** button.

 Expected behavior: The pop-up is displayed based on the configuration.

 Actual behavior: The pop-up isn't displayed when the user selects the **Send** button.

</td></tr><tr><td>

Event Management

 PRB1980951

 [KB2738069](https://hi.service-now.com/kb_view.do?sysparm_article=KB2738069)

</td><td>

When text-based grouping is turned on, tag-based grouping doesn't work consistently

</td><td>

When text-based grouping is turned on, the related tag-based alerts aren't always grouped. This behavior isn't consistently reproducible and occurs at random. If text-based grouping is turned off, the related alerts are grouped by tags.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1982324

</td><td>

Group type appears automated, but the group was created according to the tag-based definition

</td><td>

The issue occurs when there is a pattern \(same metric, different node\), and tag-based is enabled but with the wrong one turned on \(same metric, same node\). The user gets an automated group, but worknotes are received from tag-based.

</td><td>

1.  Define the pattern attribute node and metric.
2.  Set the following properties:
    -   sa\_analytics.enable\_no\_ci\_grouping=true
    -   sa\_analytics.agg.query. group\_logic\_order= MIXED,PATTERN,GENERALIZED \_PATTERNS,NETWORK\_ TRAFFIC,TEXTBASE \(default\)
    -   sa\_analytics.agg.mi\_graph\_min\_freq\_threshold=2
3.  Deactivate all tag-based definitions except the base instance definition \(group by exact match of node\).
4.  Create two events with the same node N1, empty CI, and different metrics M1 and M2.
5.  Wait at least 10 minutes.
6.  Create the same pair of events again.
7.  Run the job 'Service Analytics Alert Aggregation Learner'.
8.  Verify that the pattern with features N1&amp;&amp;&amp;M1 and N1&amp;&amp;&amp;M3 is created.
9.  Close all alerts.
10. Create one event with N1 and M1.
11. Wait for the grouping job to handle it.

Observe that the relevant alert appears in the staging table as an isolated alert with no parent.

12. Create one event with N1 and M2.

 Observe that an automated group with two alerts is created in the next cycle of the grouping job. The group alert should have the proper worknotes.

</td></tr><tr><td>

Event Management

 PRB1999707

</td><td>

An app node crash occurs due to OutOfMemory \(OOM\), and GroupingDebugLogger accumulates log messages even if logging is disabled

</td><td>

After stimulating alerts for Metric rule/Event rule and checking the tables for node restarts and active transactions, the queue in the sys\_trigger table is huge.

</td><td>

1.  Provision an instance with the following installed:
    -   sn-dex-4.0.0-SNAPSHOT
    -   agent-client-collector-framework-6.0.1
    -   com.snc.samp
    -   com.sn\_sam\_saas\_int
2.  Load 400k agents with E2E data simulation using SIM Version: 3.2.45.
3.  Simulate alerts for Metric rule/Event rule at 300k-600k per 5 minute rate, so that it runs at 1-2k per second.
4.  Check the node restarts from the v\_cluster\_nodes table.
5.  Check the active transactions from the v\_cluster\_transaction table.

Notice that there are slow 'Event Management – process events' jobs.

6.  Check queue in the sys\_trigger table.

 Notice that there is a huge queue found in the sys\_trigger table.

</td></tr><tr><td>

Explicit Roles

 PRB2011506

</td><td>

The NullPointerException in ExplicitRoleCollisions .handleSysUserGrmember invalidates ATF rollback context during CreateUserStepRunner execution

</td><td>

During the scheduled nightly ATF test execution, a null pointer exception occurs in the explicit roles collision check logic, which propagates up and invalidates the ATF rollback context. This prevents automatic rollback of test-created records \(for example, Incidents, Users, Business Services\), leaving orphaned data in the environment.

</td><td>

1.  Activate the explicit roles plugin.
2.  Create a test user.
3.  Assign the user the snc\_internal role only.
4.  Create a group with any one role.
5.  Add the test user to the created group.

 Expected behavior: There is no null pointer exception in the node log.

 Actual behavior: There is the following null pointer exception in the node log: 'Error: java.lang.NullPointerException: can't invoke 'com.glide.explicit\_roles. MutuallyExclusiveRoleCheckResult $MutualExclusionResultType .ordinal\(\)' because the return value of 'com.glide.explicit\_roles. MutuallyExclusiveRoleCheckResult .getResultType\(\)' is null'.

</td></tr><tr><td>

Field Service Capacity and Reservations Management \(Glide Family Channel\)

 PRB2017642

</td><td>

The hours/tasks capacity definition doesn't consider the assignment time zone when computing demand metrics and calculating capacity usage

</td><td>

The metrics table records \(from\_date, to\_date\) are based on the system time zone, not the assignment time zone.

</td><td>

1.  Create a capacity assignment with the capacity definition as hours/tasks.
2.  Give any time zone other than system time zone.

 Observe that the metrics table records \(from\_date, to\_date\) are based on the system time zone, not the assignment time zone.

</td></tr><tr><td>

Field Service Capacity and Reservations Management \(Glide Family Channel\)

 PRB2020554

</td><td>

All capacity console event values should be displayed based on the capacity assignment time zone

</td><td>

The events should be displayed according to the assignment time zone, not the system time zone.

</td><td>

1.  Navigate to the Capacity Console.
2.  Create a capacity assignment for any territory.
3.  Open CSP.
4.  Check the dates of the event.

 Observe that the events aren't displayed according to the assignment time zone.

</td></tr><tr><td>

Flow Engine

 PRB1992819

</td><td>

Impact handling of Scripting Governance disable switch

</td><td>

A disable switch for the Scripting Governance feature is being added. Any ACL or Java code dependent on the scripting role/group will break if a user flips the disable switch.

</td><td>

1.  Check the ACL and Java code for usage of the snc\_required\_script\_writer\_permission role and conditional script writer group.
2.  verify that the feature doesn't break when the switch is turned off/on.

</td></tr><tr><td>

Flow Engine

 PRB2014479

</td><td>

Add the roles 'taas writer' and 'taas reader' with API access only, and not with table ownership

</td><td>

Adding the role trigger\_designer directly to policy\_manager was evaluated and ruled out, as the 'policy manager' role should not have access to trigger the 'designer' role.

</td><td>

 

</td></tr><tr><td>

Form Templates

 PRB1963747

 [KB2962231](https://hi.service-now.com/kb_view.do?sysparm_article=KB2962231)

</td><td>

A template sometimes can't populate both the 'Assigned to' and 'Assignment' group

</td><td>

Following the upgrade to Zurich, the user can't update 'Assigned to' through templates, but they can perform the update manually. In workspace, if a template sets both 'Assigned To' and 'Assignment Group', the template application may fail. Assignment group validation determines if the 'Assigned To' user belongs to the assignment group when a template is applied. However, there's an issue where the validation only uses the record value's assignment group and the assignment group in the template is ignored. This behavior doesn't occur when templates are applied using UI16.

</td><td>

Refer to the listed KB article for details.

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

GlideAggregate API

 PRB1951351

</td><td>

GlideAggregate returns incorrect results for the business calendar with a condition on **Date** field

</td><td>

The issue occurs on both MariaDB and RaptorDB.

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

GlideRecord

 PRB1958518

 [KB2942052](https://hi.service-now.com/kb_view.do?sysparm_article=KB2942052)

</td><td>

A Null Pointer Exception is thrown if a table has a **GlideElement WikiText type** field and queries at start up before extension points are loaded

</td><td>

Adding a **GlideElement Wikitext type** field to the user table can cause an outage. The page is empty and errors are seen. On a local instance, the instance throws servlet exceptions and doesn't start.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Hardware Asset Management

 PRB2023284

</td><td>

The stockrooms missing distribution channel yields empty records in list view

</td><td>

 

</td><td>

1.  Provision a Zurich instance with HAM 12.1.2 installed.
2.  Navigate to **Hardware Asset Workspace** &gt; **Inventory**.
3.  Select the **View** button on stockrooms missing distribution channel \(important action\).

 Observe that no records are visible.

</td></tr><tr><td>

Horizon Avatar Component

 PRB2010763

</td><td>

The gradient border is missing for AI Specialist avatars in the activity stream for Seismic interfaces

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1910095

</td><td>

The **VA Chat** icon disappears in responsive view

</td><td>

 

</td><td>

1.  Log in to the ESC Portal.
2.  Configure NAVA.
3.  Enable pinning behavior.
4.  Pin the chat window.
5.  Change the view to the responsive view.
6.  Unpin the chat window.

 Observe that the **VA Chat** icon disappears.

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

 PRB2010425

</td><td>

Additional comments added via the CSM Portal are duplicated

</td><td>

This happens if the state is set to Awaiting Info.

</td><td>

1.  Impersonate a CSM agent.
2.  Open a case.
3.  Add an additional comment and request info.

Observe that the state of the case is set to Awaiting Info.

4.  Impersonate an external customer account.
5.  Open the case.
6.  Add a comment.

Observe that the comment appears twice in the case activity log.

7.  With the state of the case set to open, add a second comment.

 Observe that the second comment is not duplicated.

</td></tr><tr><td>

HR Service Delivery

 PRB2016516

</td><td>

RCA is generated for 'Populate Manager Reportee Count Using Eligible Users' and 'EmployeeHubOrgChart ReporteeUtilSNC'

</td><td>

The following two RCA's are generated for the new scripts, causing test failures: sys\_script\_include\_ a302f8807873f250f877079523d275e1 and sysauto\_script\_ 33a5e72453f7b210f2ebffc230e5e69d.

</td><td>

 

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB2023467

</td><td>

Incorrect values are shown on the clone summary page

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Interactive Filters

 PRB2007031

</td><td>

Applying the filter in the Dashboard shows 'Some applied options are currently unavailable' when the filter options have a comma ',' in the value

</td><td>

While trying to apply an indicator filter with the 'Filter' option in the breakdown, the messages 'Some applied options are currently unavailable' and 'Unavailable option' appear.

</td><td>

1.  Create a filter with a data source as an indicator.
2.  Create a breakdown on any table.
3.  Ensure the field has a comma in the field value.
4.  Add the filter to a dashboard.
5.  Apply the filter.

 Notice the message, 'Some applied options are currently unavailable.'

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

Key Management Framework \(KMF\)

 PRB1964424

</td><td>

WebServices Mutual Auth connections fail if the instances are in FIPS mode

</td><td>

If an instance is using FIPS mode, REST Web Services connections fail if the authentication type is 'Mutual Auth'. The following error is thrown: 'org.bouncycastle.tls.TlsFatalAlert: unsupported\_extension\(110\)'.

</td><td>

1.  Turn on FIPS mode on an instance.
2.  Set up an outbound REST call to a third-party API.
3.  Make sure the authentication type is 'Mutual Auth'.
4.  Set up a protocol profile record to associate with the REST connection.
5.  Apply the API's endpoint .bsfks keystore certificate to the Protocol Profile Keystore record.
6.  Run a test connection to the endpoint.

 See that it fails with an error: 'org.bouncycastle.tls.TlsFatalAlert: unsupported\_extension\(110\)'.

</td></tr><tr><td>

Knowledge Graph \(Family\)

 PRB2021133

</td><td>

Knowledge Graph \(KG\) description deactivator triggers long-running queries, causing HLL spikes

</td><td>

Post Version Upgrade Job : KG Description Deactivator triggers Long running queries and causes HLL spike

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2000521

</td><td>

Support for Knowledge blocks in ECE

</td><td>

Knowledge blocks aren't supported in ECE. Ideally, blocks should be supported in ECE.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2005195

</td><td>

KM Import Article conversion utility should be exposed as a callable API for external consumption by the GRC/IRM policy flow

</td><td>

The KM Import Article feature uses Apache Tika and Apache POI libraries for DOCX-to-HTML conversion and produces flexible, translation-safe HTML output. On the other hand, the GRC policy flow's current GroupDocs-based conversion applies static absolute positioning. To resolve the translation formatting issue in GRC's policy flow, the KM conversion utility needs to be exposed as a standalone API that GRC/IRM can consume directly—without requiring an existing Knowledge Article upfront and without deleting the source attachment document during processing.

</td><td>

1.  Navigate to **Knowledge Management** &gt; **Import Article**.
2.  Import a Word document.
3.  Open the created Knowledge Article.
4.  View the source HTML.

 Observe that the output contains flexible/relative styling and there's no static absolute positioning. Compare against a Knowledge Article created via the GRC/IRM policy flow and note the static positioning difference.

</td></tr><tr><td>

Knowledge Management

 PRB2010029

</td><td>

Knowledge blocks aren't honoring KC redirection properties

</td><td>

 

</td><td>

1.  Turn on redirection properties for KC: sn\_km\_center.glide.knowman.redirect.enable.
2.  Navigate to 'Knowledge Blocks' in Navigator in UI16.
3.  Select **Create**.

 Expected behavior: Knowledge blocks should honor KC redirection properties.

 Actual behavior: Creating or editing a from UI16 doesn't redirect to KC.

</td></tr><tr><td>

Knowledge Management

 PRB2014078

</td><td>

Turn on the Apriel 2.0 model and set the new 3P model as the default

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

List Administration

 PRB1933683

</td><td>

List column widths aren't persistent when columns are personalized

</td><td>

The user can adjust the list column width. However, when the list columns are personalized \(either by adding or removing columns\), the adjusted width doesn't persist and resets to the default width.

</td><td>

1.  Navigate to CSM/FSM Configurable Workspace.
2.  Open any list from the List Page.
3.  Adjust the width of any column.
4.  Select the **Personalize** action.
5.  Add or remove columns.
6.  Select **Apply**.

 Notice that the adjusted width is reset to some default width.

</td></tr><tr><td>

List Administration

 PRB1970036

</td><td>

List type data visualization doesn't show new lines \(multi-lines\)

</td><td>

The data visualization doesn't add new lines \(multi-lines\) in Zurich, but it does in Yokohama.

</td><td>

1.  Open an incident record.
2.  Enter the following strings in the **Description** field:
    -   改行1
    -   改行1
    -   改行1
    -   改行1
    -   改行1
    -   改行1
3.  Create a dashboard.
4.  Add a list data visualization based on the incident table.
5.  Show the description column on the data visualization.

 Observe that the data visualization doesn't add new lines \(multi-lines\).

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

 PRB2015114

</td><td>

The user is unable to load the results table frame on the same page

</td><td>

This issue was found in Query Builder for Yokohama and Zurich.

</td><td>

1.  Navigate to the **CMDB Query Builder**.
2.  Create a simple one node query.
3.  Select the **Settings** icon on top right.
4.  Turn off 'Display Results in New Tab' so that the results are displayed on the current page.
5.  Run the query without saving.

 Expected behavior: Even when there are no results for this query, the result table frame is shown with headers and columns.

 Actual behavior: The result table frame does not show up, and only a blank popover appears.

</td></tr><tr><td>

List Administration

 PRB2023617

</td><td>

Grouping and summarization for telemetry for Multi-Record Actions \(MRA\) - List AI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2023634

</td><td>

Implement add/remove an AI indicator for the rows created/modified by an AI agent and clear an AI indicator when inline edits are made

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1773052

</td><td>

The check box in presentational list can't be both inactive and selected

</td><td>

When the user sets the row as selected and inactive, the check box is only inactive.

</td><td>

1.  Add a presentational list on UIB.
2.  Use a script to set a row as selected and inactive.

 Expected behavior: The check box in presentational list is both inactive and selected.

 Actual behavior: The check box in presentational list is inactive, but not selected.

</td></tr><tr><td>

MetricBase

 PRB2008126

</td><td>

The rollup scheduling script has a race condition that allows duplicate event queuing in MetricRaptor

</td><td>

When no classic shards are configured and the mb\_shard\_mapping table is either empty or has no rows with stores\_classic\_data = true, there is excessive logging for ClothoClientManager and ClothoRrdWriter. The error '\*\*\* ERROR \*\*\* No endpoints available' occurs for ClothoClientManager, and '\*\*\* WARNING \*\*\* No Classic Clotho Shard Configured' occurs for ClothoRrdWriter.

</td><td>

1.  Have an active mb\_raptor\_table with the rollup spec configured.
2.  Wait for the scheduled script to queue an mb\_rollup event.
3.  While the event is in 'processing' state, trigger or wait for the next scheduled run.
4.  Wait for a one minute interval.

 Observe that a duplicate mb\_rollup event is queued because the state = 'ready' check misses the processing event.

</td></tr><tr><td>

Mobile Platform

 PRB1999865

</td><td>

Support onSubmit UI Rule

</td><td>

Configure and execute UI Rules at the time when the input form screen is submitted both online and offline.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2022350

</td><td>

Vision Agent MMS Glide changes

</td><td>

This is a product update

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2022351

</td><td>

Implement improvements to the MMService plugin

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

Next Experience Unified Navigation

 PRB2003211

</td><td>

/api/now/ui/polaris/menu is slow to build the cache on login

</td><td>

1000s of each of these queries are run to retrieve user preferences and screen accessibilities. It should be able to retrieve all of most of these items in 1 query.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2022500

</td><td>

If a work item is assigned to the same agent repeatedly, the Desktop Notification stops appearing entirely

</td><td>

A new desktop notification should appear on every work item assignment.

</td><td>

 

</td></tr><tr><td>

Now Assist in AI Search

 PRB1920760

</td><td>

GenAI log IDs are not returned for Now Assist Genius Results

</td><td>

This issue occurs in Virtual Agent, portal, Now Assist Actions, Now Assist Q&amp;A, Synthesized Response, or anywhere a Now Assist Genius Result \(GR\) can be returned. Feedback is not logged even though there should be a value after the user selects the **Thumbs up** icon or **Thumbs down** icon on the Genius Result \(GR\).

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

Now Assist in Document Intelligence

 PRB2030125

</td><td>

Support attachments where the file names doesn't contain '.type' at the end

</td><td>

There's an error: '\{'attachment':\{\}, 'task':\{'708a54b23b810f50141 a0e0f23e45a0b': \{'error\_msg':'Prediction server is not able to process the attachments: begin 0, end -1, length 9'\}\}\}'.

</td><td>

1.  Have a png image file with no errors.
2.  Rename it to have a file name with '.png'.
3.  Upload it to an instance.
4.  Test the attachment summarization.

 Observe an error.

</td></tr><tr><td>

Now Assist Nextwave Experience

 PRB2010718

</td><td>

Portal URL resolver mapping is broken in NextWave conversations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB2009288

</td><td>

Feedback isn't updated in the Gen AI log table

</td><td>

 

</td><td>

1.  Type 'what is spam?'.
2.  Select any feedback **Thumbs Up/Down** icon immediately.

Observe that feedback is successfully stored in the Gen AI log table.

3.  Unselect submitted feedback or submit different feedback.

 Expected behavior: Feedback should be updated in the Gen AI log table.

 Actual behavior: Feedback isn't updated in Gen AI log table.

</td></tr><tr><td>

Now Assist Panel

 PRB2025041

</td><td>

A mic enabled for NAVA Premium Chat is incorrectly surfaced on Enhanced Chat

</td><td>

 

</td><td>

1.  Use the latest version of NAVA.
2.  Enable a mic from NAVA assistant designer.
3.  Change the experience to Enhanced Chat.

 Expected behavior: The **Send** button appears in the input bar.

 Actual behavior: On-Glide mic appears in the input bar.

</td></tr><tr><td>

OneExtend

 PRB2001785

</td><td>

Accuracy choice should be added for the **Group** field in the eval suggestion table

</td><td>

 

</td><td>

1.  Navigate to the sys\_one\_extend\_eval\_suggestion table.
2.  Open any record.
3.  Select the **Group choice** list.

 Observe that accuracy choice isn't present.

</td></tr><tr><td>

OneExtend

 PRB2013928

</td><td>

JSON Web Token \(JWT\) and metadata are missing domain visibility information

</td><td>

The JWT API only contains a claim for the domain, and is missing the list of domains visible to the user.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2017386

</td><td>

Now Assist jobs are running for extended periods and slowing processing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2025105

</td><td>

Responses fix for Java flow

</td><td>

Validate all the Java flow from NAVA, NAP and Skill Kit.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2025250

</td><td>

Correlation Insights skill is stuck on the progress bar when off-Glide is enabled

</td><td>

Insights should be generated and displayed. Instead, the progress bar spins indefinitely and no generative AI logs are produced. The issue occurs because the app prepares a bulk request with three payloads and invokes it in async mode with a callback handler. When off-Glide is enabled for the capability, the async callback flow \('NowAssistforSIR CorrelationInsightsCallback'\) appears to break silently. No generative AI logs are generated, indicating the LLM call never completes or the response isn't handled correctly.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2025268

</td><td>

Refactor the logic to update the URL and status in GeoRoutingDaoImpl

</td><td>

On repairing the GAIC plugin, if the Geo-Licensed record is not available, the http\_connection records are randomly updating.

</td><td>

1.  Log in to an instance as an admin user.
2.  Navigate to **Connection &amp; Credential aliases**.
3.  Filter Now LLM.
4.  Open the record.
5.  Verify that the Now LLM and Geo-Licensed record exists in http\_connection.
6.  Delete only the Geo-Licensed record.
7.  Repair the GAIC plugin.
8.  Once the repair is complete, navigate to the http\_connection record.
9.  Filter by latest updated.

 Observe that it's randomly updating any of the http\_connection.

</td></tr><tr><td>

OneExtend

 PRB2025367

</td><td>

A cloning instance should preserve mosaic functionality in the target instance

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2025540

</td><td>

Off-glide Mosaic pipeline ignores the per-request timeout and every call falls back to the platform default, regardless of caller intent or service-plan configuration

</td><td>

All Mosaic calls fall back to the platform default; caller / control-setting / service-plan values are ignored. There's no phase-boundary timeout enforcement and requests run well past their stated SLA. DT translation always uses 0L.

</td><td>

1.  Enable off-Glide execution.
2.  Ensure the Mosaic endpoint is reachable.
3.  Submit an off-Glide execution request with an explicit short timeout \(for example, 5 seconds\) that targets a capability with a slow model/heavy prompt so that the Mosaic call takes around 10–20 seconds.

Observe that the request doesn't abort at 5 seconds. It runs until the platform default \(around 60 seconds\) or the upstream gateway times out.

4.  In the Mosaic-client logs, confirm timeoutMs=0 \(or the default\) on the outgoing HTTP call, regardless of the caller-supplied value.
5.  Update the sys\_generative\_ai control setting \(Mosaic timeout\) to a small value.
6.  Send a request with no explicit timeout.

Observe that the control setting is also ignored.

7.  Update one\_api\_service\_plan.timeout\_ms for the plan backing the capability.
8.  Send a request.

Observe that the service-plan value is not applied either.

9.  Pick a capability whose postprocessor emits a \_dtRequest \(DT reverse translation\).
10. Send a request with timeout=5 seconds where the primary Mosaic call returns at around 4 seconds.
11. Confirm the subsequent DT-translation call still fires with timeoutMs=0 \(platform default\), so the total elapsed time exceeds 5 seconds.
12. Repeat steps 9-11, driving the budget to exhaustion before postprocess.
13. Confirm the DT call still fires instead of being skipped, and there is no 400001 / timeout response.
14. Send a request via the routed-from-Mosaic &gt; OneExtend callback path \(validateOffGlideConfig\) that triggers DT translation.
15. Confirm that no timeout is honored there either.

 Expected behavior: The caller-supplied timeout is the strongest signal and is honored by every Mosaic HTTP call in the pipeline \(preprocess gate, primary execute, postprocess DT translation\). In its absence, the control-setting, service-plan, and 60 second default apply \(in that order\). Exhausting the budget at any phase returns a timeout response \(status=error, errorCode=400001\). Override values are persisted to one\_api\_service\_plan.timeout\_ms and cascade.

 Actual behavior: All Mosaic calls fall back to the platform default; caller / control-setting / service-plan values are ignored. There's no phase-boundary timeout enforcement and requests run well past their stated SLA. DT translation always uses 0L.

</td></tr><tr><td>

OneExtend

 PRB2025975

</td><td>

Do not log prompts or responses to Splunk for in-country routing users

</td><td>

Prompt and response information is removed from logs for users with in-country routing SKU.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2026081

</td><td>

There's a 100501 error with an async call

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2026173

</td><td>

Glide-cs unit test fails in Zurich mainline

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2027496

</td><td>

The metric batch\_result.status is stuck at in\_progress and isSkillEvaluationRun\(\) doesn't recognize the conversational\_ai evaluation type

</td><td>

For conversational\_ai evaluation runs, metric-level batch\_result records are never updated to status=completed. This causes the evaluation dashboard to display zero scores for all the metrics, even though valid evaluation data exists in the sys\_one\_extend \_eval\_metric\_result and sys\_generative\_ai\_metric tables.

</td><td>

1.  Create a Conversational AI evaluation run \(AutoChat\) with metrics like conversation success, skill selection accuracy, and turn count.
2.  Wait for the evaluation to complete \(batch\_run\_task status = processed\).
3.  Query the metric-level batch\_result records.

Observe that all the metric batch\_result records have status=in\_progress instead of completed.

4.  Navigate to the evaluation dashboard.

 Observe that all the metric scores show as 0 because the Java API getCustomMetric ScoresPerPrompt filters batch\_result.status! =in\_progress.

</td></tr><tr><td>

OneExtend

 PRB2028533

</td><td>

Java scriptable methods aren't working in some instance nodes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB1993682

</td><td>

'This report has been migrated to a visualization' banner is shown when the unified property is false

</td><td>

The banner message appears: 'This report has been migrated to a visualization. Migrated visualization is here.' The link redirects to a random visualization.

</td><td>

1.  Open an instance with sys\_ui\_context menus.
2.  Navigate to Migration Center \(/now/platform-analytics-workspace/migration-center\).
3.  Perform a bulk migration.
4.  Activate all content.
5.  Navigate to System Properties.
6.  Set the property 'com.glide.par.unified\_analytics.enabled' to false.
7.  Navigate to any record list \(for example, /incident\_list.do\).
8.  Create a bar or pie chart report from any column to open the Report Designer.

 Expected behavior: The banner isn't shown, as no report was migrated.

 Actual behavior: The banner message appears: 'This report has been migrated to a visualization. Migrated visualization is here.' The link redirects to a random visualization.

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB2005720

</td><td>

The CoreUI dashboard selector triggers excessive ACL checks

</td><td>

The ACL is evaluated with a different access path and context for each check, so it is re‑executed repeatedly. When there are thousands of dashboards, this results in excessive ACL evaluations and causes the instance to hang.

</td><td>

1.  Open any CoreUI dashboard.
2.  Open the dashboard selector.
3.  Select **All Dashboards**.

 Expected behavior: The dashboard selector avoids excessive ACL checks and runs one check per dashboard.

 Actual behavior: It triggers permission evaluation for every dashboard the user has access to, including an ACL check per dashboard and multiple field‑level ACL checks.

</td></tr><tr><td>

Performance Analytics

 PRB1990900

</td><td>

The system property com.snc.pa.dm.enable.mlb is set to true on non-Raptor DB Pro instances

</td><td>

Users can install a plugin with Raptor DB \(pro or standard\). With a schedule job, they can disable the feature by disabling the global property com.snc.pa.dm.enable.mlb.

</td><td>

1.  Open an instance with raptor standard.
2.  Validate the system property: com.snc.pa.dm.enable.mlb.

 Expected behavior: The property is set to false. The user shouldn't be able to control it and set its values.

 Actual behavior: The property is set to true. The user can control it and set its values.

</td></tr><tr><td>

Performance Analytics

 PRB1995131

</td><td>

There are Query Builder \(QB\) and Workspace UI error pop-up clips in the surrounding UI if a query fails for CMDB NLQ

</td><td>

Turning off the NLQ Prediction server results in an error message in both QB and in the CMDB Workspace, and the UI doesn't render as expected in CMDB Workspace.

</td><td>

1.  Turn off the NLQ Prediction server from sys\_properties by deleting the URL value 'glide.prediction\_service.url'.
2.  Navigate to **Query Builder**.
3.  Create an NLQ query, which adds nodes to the canvas.

Notice that this results in the 'Oops...' error.

4.  Navigate to **CMDB Workspace**.
5.  Create an NLQ query, which should open a new tab.

 Notice that this results in the 'Oops...' error, and the UI is incorrect.

</td></tr><tr><td>

Performance Analytics

 PRB1999245

</td><td>

Discrepancies with Core UI on change and change percentage

</td><td>

The change and change percentage may be displayed on the widget but not on the data visualization.

</td><td>

1.  Create an indicator \(an indicator source isn't necessary\).
2.  Enable **Render continuous lines** under the 'Other' tab.
3.  Open the scoresheet to edit the scores of the before indicator:
    1.  Feb 28th: 200
    2.  Jan 31st: 100
4.  Create a single score visualization using this indicator.
5.  Enable change and change percentage.

Notice that the change and change percentage aren't displayed.

6.  Disable the system property 'com.glide.par.unified\_analytics.enabled'.
7.  Create a single score PA widget on the before indicator, with Visualization: Latest Score.
8.  Leave all other fields as the default value.
9.  Add the before widget to a Core UI dashboard.

 Notice that the widget displays the change \(100\) and change percentage \(100%\).

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
4.  Select the **Arrow** to view the Recent Dashboards list.

If this is the first login of the day, observe that the list contains dashboards that may not have been previously accessed.

5.  Switch between several dashboards.

Observe that the Recent Dashboards list updates to reflect the dashboards opened during the session.

6.  Log out of the instance.
7.  Log back in using a new browser tab.

 Observe that the Recent Dashboards list resets and displays a different, seemingly random list of dashboards instead of the ones previously accessed.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1992984

</td><td>

Can't share a dashboard to all internal users \(users with at least one role\)

</td><td>

When the itil user opens the dashboard, the dashboard isn't found.

</td><td>

1.  Create a dashboard.
2.  Share the dashboard to the role 'dashboard\_user' with view mode.
3.  Impersonate an itil user.
4.  Open the dashboard.

 Expected behavior: The dashboard is visible to the itil user.

 Actual behavior: The dashboard isn't found.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1998865

</td><td>

Sys ID is automatically populated for the value in sys\_translated

</td><td>

This happens when the user changes the value of a tab when using a non-English language.

</td><td>

1.  Navigate to Dashboards.
2.  Create a dashboard.
3.  Add a tab.
4.  Switch to a non-English language.
5.  Change the value of the tab.
6.  Save.

 Notice that the value in sys\_translated contains sys ID.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2002552

</td><td>

Due to VCS update set collision, a dashboard save fails with a generic error: 'Your dashboard could not be saved'

</td><td>

This problem only happens in scopes with VCS-controlled apps, no matter where users create the dashboard. The important factor is whether the scope has a repo configuration set.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2007784

</td><td>

DomainService uses DomainSupport.hasAccess instead of DomainHierarchy for validation

</td><td>

When the user tries to access the dashboard, an error appears: 'Error while getting domain for dashboard'.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2025067

</td><td>

The sys\_translated record for par\_dashboard\_tab is overwritten

</td><td>

This can cause translations to be lost.

</td><td>

1.  In English, create a sys\_translated record as follows:
    1.  Label: あいう
    2.  Table: par\_dashboard\_tab
    3.  Element: name
    4.  Language: ja
    5.  Value: TabName
2.  Create a PAE Dashboard.
3.  Add a tab with the same name as the sys\_translated value \(TabName\).
4.  Save the dashboard.
5.  Create another dashboard.
6.  Add a tab with the same name as the sys\_translated value again.
7.  Save the dashboard.
8.  Switch the language to Japanese.
9.  Return to one of the dashboards.
10. Rename the tab あいう to さしす.
11. Check the other dashboard tab.

 Observe that the translation is lost because the sys\_translated record is overwritten.

</td></tr><tr><td>

Platform Analytics Filters

 PRB2013316

</td><td>

Additional controls for single and multi select

</td><td>

For both radio buttons and check boxes, there should be a way to clear the selection instead of using the 'Clear all filters' capability on the dashboard level.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Filters

 PRB2014365

</td><td>

JavaScript-based sys\_choice labels are rendered as raw text in dashboard filters

</td><td>

A sys\_choice record uses JavaScript to dynamically populate the country label when the value is null. However, when this field is used in Platform Analytics dashboards \(via indicator breakdown with sys\_choice as the facts table\), the JavaScript isn't evaluated and is instead displayed as raw text in the filter.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1998821

</td><td>

The Platform Analytics Migration Center summary window isn't counting all domain dashboards when doing migration in the global domain

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics

 PRB1933496

 [KB2599826](https://hi.service-now.com/kb_view.do?sysparm_article=KB2599826)

</td><td>

The main **Refresh** icon in the dashboard doesn't work with the list component added to the dashboard

</td><td>

In Zurich, the main **Refresh** icon in dashboards doesn't refresh list components when they are added to a dashboard. While other widgets \(such as single score visualizations\) refresh correctly, the list component remains static. This issue occurs because the dashboard refresh event isn't mapped to the list component.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2009677

</td><td>

The complex object's format is different for playbook output/input

</td><td>

The flow gives an 'com.snc.process\_ flow.exception. ProcessAutomationException: Could not serialize value' error when running playbook.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2023731

</td><td>

Child agent changes in playbook snapshot for hybrid agent configuration

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1980574

</td><td>

The Process Mining app should be free on the store

</td><td>

Process Mining is shown as a licensed app on the store. However, it's auto-installed on many instances, which causes confusion when users aren't able to upgrade.

</td><td>

Scenario 1:

 1.  Navigate to the store.
2.  Search for the Process Mining app.
3.  Check the pricing.

 Scenario 2:

 1.  Navigate to the plugin list.
2.  Search for the Process Mining \(sn\_po\) app.
3.  Make sure there are some app updates available.

 Expected behavior: Users can update the app to the latest version.

 Actual behavior: Users get a license error, so they can't proceed with the app update.

</td></tr><tr><td>

Process Mining Workspace

 PRB2011383

</td><td>

Update the Appsee event

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1908085

</td><td>

Error on 'Manage View'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB2009176

</td><td>

Opening the Project Status Report in the Project Workspace triggers an update to the **Overall Health** field on the corresponding project record

</td><td>

Opening the Project Status Report within the Project Workspace updates the **Overall Health** field on the corresponding project record to match the value from the status report.

</td><td>

1.  Open a project in the Project Workspace \(PW\).
2.  Navigate to the 'Status Report' tab.
3.  Create a status report.
4.  Navigate to the 'Details' tab.
5.  Locate the **Status** field.
6.  Ensure the **Status** field is different from the **Overall Health** field in the status report.
7.  If both values are the same, manually update the **Status** field on the project.
8.  Open the 'Status Report' tab from the left panel.
9.  Navigate back to the 'Details' tab.

 Notice that the **Status** field is automatically reverted to match the Overall Health value from the status report.

</td></tr><tr><td>

Project Management

 PRB2021806

</td><td>

Add a 'No status' option to the **Project Status** field

</td><td>

The **Project Status** field \(pm\_project.status\) currently doesn't include a 'No status' option, which prevents projects from having an unset/neutral status state. This causes ambiguity in reporting and makes it difficult to distinguish between projects that have not yet been assigned a status vs. those intentionally marked as 'On Track' or 'At Risk'. A 'No status' option should be added to the **Status** field list. This verifies that status transitions — including from an unset state to a defined status — can be accurately captured and reflected in usage analytics.

</td><td>

1.  Navigate to **Project Management** &gt; **Projects** &gt; **All Projects**.
2.  Open any active project.
3.  Select the **Status** field.

 Observe that a 'No status' option isn't available.

</td></tr><tr><td>

Record Hierarchy

 PRB2013585

</td><td>

Reconciliation of record hierarchy with missing path field skipped

</td><td>

If the user deletes the rh.hierarchy.create event, there is no 'Reconcile Hierarchy' link under Related Links. If the user executes SNC.RecordHierarchyAPI.get \(\).reconcilePaths\(sysId\), no event is posted to resume creation of the hierarchy.

</td><td>

1.  Create a sys\_record\_hierarchy.
2.  Immediately delete the associated rh.hierarchy.create event that's generated in sysevent.

Observe that the sys\_record\_hierarchy is in a PENDING\_CREATE state with no event to progress it to the next step.

3.  Visit the sys\_record\_hierarchy record.

Notice that there is no 'Reconcile Hierarchy' link under Related Links.

4.  Copy the sysId of the sys\_record\_hierarchy record.
5.  Navigate to **Scripts - background**.
6.  Execute SNC.RecordHierarchyAPI. get\(\).reconcilePaths\(sysId\).

 Observe that nothing happens. No event is posted to resume creation of the hierarchy.

</td></tr><tr><td>

Record Hierarchy

 PRB2014979

</td><td>

Allow RecordHierarchies to always be usable optionally unless it is inactive

</td><td>

The current behavior shows that after a record hierarchy is defined, any query operations that use the hierarchy will explicitly return 'false' until every record in the hierarchy has been assigned a path. After paths have been assigned, the hierarchy is said to be 'usable' as its fully initialized and ready for queries. A GP was added to optionally allow the hierarchy to be usable while records are being assigned paths. The results for queries may be incomplete or partially stale depending on how long the initialization takes place, but should otherwise be accurate.

 Users are beginning to use IN\_HIERARCHY conditions for all sorts of features ranging in criticality, up to and including ACLs. If the record hierarchy runs into some sort of issue, such as it can render the record hierarchy unusable and all queries would begin to fail. However, the paths assigned to all records are still valid as long as changes are minimal, and can continue to return mostly accurate results while any issues with the record hierarchy feature are addressed.

 This fix is to address usability; as long as the record hierarchy isn't explicitly deactivated, it can be made 'usable' and queries will return results based on whatever paths may be assigned at the time.

</td><td>

 

</td></tr><tr><td>

Related Lists

 PRB2000158

 [KB2823064](https://hi.service-now.com/kb_view.do?sysparm_article=KB2823064)

</td><td>

Related lists don't show row data

</td><td>

Related lists don't show row data in list cells \[Core UI\].

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

ReleaseOps - Family

 PRB2009639

</td><td>

Instance scan failure doesn't return the correct message

</td><td>

The scan failure doesn't mention a reason for the failure in the work notes.

</td><td>

1.  Open a Zurich instance.
2.  In development, start a full instance scan.
3.  In production, mark a DR as ready for assessment.

 Expected behavior: The scan failure shows the reason for the failure in the work notes.

 Actual behavior: The scan failure doesn't mention a reason in the work notes.

</td></tr><tr><td>

Resource Management

 PRB2003945

</td><td>

Cost plan breakdowns are duplicated

</td><td>

When the user changes the start date and end date from a resource plan, the business rule \(BR\) UpdateCostPlan AssociatedToResourcePlan launches an event. The BR 'Recreate Requested Allocations' is also launched, updating the resource plan again and changing the planned cost. In summary, when the user updates the dates, the system updates the resource plan twice, one time for the dates and another for the planned cost, practically at the same time.

 Both changes trigger the BR UpdateCostPlan AssociatedToResourcePlan and two events are created. Since there are two events in the system, they will try to perform the same action, and this could lead to problem concurrency. The two events are processed at the same time and the cost plan breakdowns are created twice.

</td><td>

1.  Navigate to pm\_project.list.
2.  Open the project where the duplicated cost plan breakdowns were created.

</td></tr><tr><td>

Resource Management

 PRB2020809

</td><td>

Updating dates in the assignment should update the resource availability

</td><td>

Dependent choice config should also be supported in the project workspace bottom grid.

</td><td>

1.  Open the project workspace.
2.  Navigate to the project.
3.  Create an unassigned assignment from the bottom grid.
4.  Check any resource.

Notice its availability.

5.  Update the assignment dates.
6.  Check the resource availability again.

Observe that it's still the same, even though the availability should be updated as soon as the dates are updated.

7.  Create any field on the resource assignment table which is dependent on any other reference field.

 Observe that the dependent config isn't supported in bottom grid choices. It should be supported.

</td></tr><tr><td>

Resource Management

 PRB2024520

</td><td>

Fetching choices with their dependent field values to prepare criteria

</td><td>

The field doesn't show the choices according to the dependent config defined.

</td><td>

1.  Create any field on the resource assignment table which is dependent on any other reference field.
2.  Add that field in the resource assignment bottom grid in PWS.
3.  Open the project workspace.
4.  Navigate to the project.
5.  Create an unassigned assignment from the bottom grid.

 Observe that the field doesn't show the choices according to the dependent config defined.

</td></tr><tr><td>

Server-side scripts

 PRB1994381

</td><td>

Discovery has issues on some node after upgrading in Australia

</td><td>

After upgrading to Australia, JavaScript running in app nodes fails to call Java functions. The following warning appears: '\*\*\* WARNING \*\*\* Evaluator: com.glide.script.RhinoEcmaError: undefined is not a function.' This impacts various features, including Discovery and Event Management.

</td><td>

 

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

Service Catalog

 PRB1976031

</td><td>

Lookup select box variables with 'Choices depend on' store a choice value instead of a label

</td><td>

When a lookup select box variable on a record producer is configured to depend on another variable, the system saves the underlying choice value rather than the human‑readable label in the created record. This behavior occurs only for lookup select box variables with the 'Choices depend on' setting; standard select box variables work correctly. As a result, the **Subcategory** field of the incident shows the internal value \(for example, '1023'\) instead of the expected label \(for example, 'Internal Application'\), which can cause confusion for users reviewing incident data. This is observed in portal pages like the ESC standard ticket page, where the value is shown in the variable summarizer.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2014228

</td><td>

Update the copy in the alert banner

</td><td>

Catalog item forms should be automatically pre-filled using the context from the conversation. The user shouldn't have to re-enter information they've already shared in the chat.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2020118

</td><td>

Ensure that a search term is a minimum of 3 words before triggering the slot fill

</td><td>

.

</td><td>

 

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2016794

</td><td>

Skip delete issue for 'Coalsce' tables

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

 PRB2021468

</td><td>

Dictionary updates aren't propagated when installed via FluentXMLUploader

</td><td>

When the user deploys changes, the dictionary updates get skipped.

</td><td>

1.  Create a fluent configuration project.
2.  Update the table column maxLength value on the instance in the UI.
3.  Update it again in the fluent configuration project.
4.  Deploy the changes.

 Expected behavior: The maxLength of the column is updated.

 Actual behavior: The dictionary updates get skipped.

</td></tr><tr><td>

Service Portal

 PRB2014571

</td><td>

Alignment of the Now Assist search results gets overflow

</td><td>

This happens on the portal while loading on browser resolution size 360 x 640.

</td><td>

1.  Make sure the Now Assist genius result is enabled on the portal.
2.  Navigate to a base instance.
3.  Change the session language to Deutsch.
4.  Navigate to the /esc portal.
5.  Open the developer tool of the browser.
6.  Set the resolution as 360 x 640.
7.  Search for any keyword \(for example, people manager\).

 Observe that the filter text 'Am relevantesten' gets overflow.

</td></tr><tr><td>

Session Management

 PRB2024286

</td><td>

Make application nodes more resilient to DDoS attacks from unauthenticated traffic

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB2019090

</td><td>

The cached RecordCard is returned without checking if the user has access to record

</td><td>

This is a caching issue, and occurs for both with incident and HR records. When the code checks if the Record Card is in the cache, it does not re-check if the user can access the record or not. When clearing the cache, the record access check is calculated correctly.

</td><td>

1.  Create an incident \(INC1\) as the user Abel Tuter.
2.  Create a discussion on it.
3.  Paste INC1 in the chat.

Notice that it renders a record card, and the user Abraham Lincoln can't access INC1 in the sidebar chat.

4.  As the user Abraham Lincoln, attempt to paste the INC1 number in the chat.

Notice that Abraham Lincoln can see the INC1 record card and its details, when Abraham Lincoln should not be able to because they have no access.

5.  Create another incident \(INC2\) as the user Abel Tuter.
6.  Create a discussion on it.
7.  Paste INC2 in the chat.

 Notice that it renders a record card, and the user Abraham Lincoln can't access INC2 in the sidebar chat. The INC2 record card is not in the cache.

</td></tr><tr><td>

Software Asset Management

 PRB1959756

</td><td>

The 'Connection Setup' section is missing on the Custom Integration view for the Workday Integration Profile after upgrading sn\_sam\_saas\_int

</td><td>

When trying to integrate with Workday \(SaaS License Management\), some tabs are missing \(for example, the 'Connection Setup' section and related list\). This makes the user unable to validate the connection and publish the profile. The 'Connection Setup' section should be visible and accessible on the custom integration view after the upgrade.

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

Software Asset Management

 PRB2021450

</td><td>

The **Add Lifecycle Data** table UI action for lifecycle playbook is incorrectly available in Zurich

</td><td>

The **Add Lifecycle Data** button is available for Zurich users, despite it being an Australia feature. When the user selects the button, nothing happens.

</td><td>

1.  Download version 10.0.1 or 10.0.2 of the app-sam-workspace store app.
2.  Navigate to **Workspaces** &gt; **Software Asset Workspace** &gt; **Software asset analytics**.
3.  Select the 'Lifecycle Management' tab.
4.  Select a report result to drill down into any report.
5.  Select the **Add Lifecycle Data** button.

 Observe that nothing happens.

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

 PRB2021614

</td><td>

Potential savings on reclamation candidates should be set regardless of licensing status

</td><td>

It should be set for both licensed and unlicensed subscriptions/installs. A software's license status doesn't impact the potential savings for removing that software. The reclamation candidate should reflect the cost of having that software installed.

</td><td>

 

</td></tr><tr><td>

Software Entitlements

 PRB2023511

</td><td>

Add an asset tag, agreement number, and location to entitlement duplicate check attributes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Standard Ticket Page

 PRB2023619

</td><td>

Family changes to fetch **Summary** fields from the m2m table

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Suite Engine

 PRB1966133

</td><td>

Assigned software should handle suite of suite

</td><td>

The reconciliation logic for licensing subscriptions should license corresponding installations for the same user.

</td><td>

 

</td></tr><tr><td>

System Archiving

 PRB1938103

</td><td>

Reparenting of sys\_attachment doesn't work when the table name is longer than 37 characters

</td><td>

.

</td><td>

 

</td></tr><tr><td>

System Archiving

 PRB1988156

</td><td>

Archive reparenting doesn't work with peripherals and large table names

</td><td>

The records for sys\_audit and sys\_journal\_field don't reparent, and an error is found in the logs.

</td><td>

1.  Create a table with sys\_audit and sys\_journal records with a length that is over 60 characters. For example, 'u\_supercalifragilisticexpiextralongname\_restore\_destroy\_test'.
2.  Attempt to archive it.

 Notice that the sys\_audit and sys\_journal\_field records don't reparent. Instead, the log shows this error, 'Found in current data management track'.

</td></tr><tr><td>

System Events

 PRB1939688

</td><td>

Inputs aren't getting processed for subflows with inputs

</td><td>

Implement thread pool with the configurations/design. The scope excludes any changes related to autoscaling or processing framework \(which means it co-exists with the jobs that are already there for flow\_engine\).

</td><td>

1.  Create a subflow with inputs.
2.  Trigger it.

 Expected behavior: All flows are completed without any errors.

 Actual behavior: A couple flows move to the completed state with an error log for not processing inputs.

</td></tr><tr><td>

Table Administration and Data Management

 PRB2025009

</td><td>

Ordering a query by a **Function** field that wraps a translated\_text column returns empty values for that list

</td><td>

 

</td><td>

1.  Create a table.
2.  Add a translated\_text column.
3.  Add **Function** field on that column.
4.  Navigate to v\_plugin.LIST.
5.  Activate the plugin 'com.snc.i18n.swedish'.
6.  Insert records \(New Name=Alice and New Name=Bob\).
7.  Submit.
8.  Add the Swedish translations \(Älice\_sv for Alice and Bob\_sv for Bob\).
9.  Submit.
10. Switch the session to Swedish.
11. Open u\_repro\_translated\_function.LIST.
12. Personalize the columns to show 'Name' and 'Name Function'.
13. Select the **Name Function** header to sort by ascending.

 Expected behavior: The 'Name Function' column shows Älice\_sv and Bob\_sv \(or the English fallback\).

 Actual behavior: The 'Name Function' column is empty for both rows.

</td></tr><tr><td>

Territory Planning

 PRB2016459

</td><td>

Unused form field mappings in the 'Suggested Agents' and 'Relocate Agents' pages cause performance issues

</td><td>

This happens in the CSM/FSM Configurable Workspace. There are two UX screen conditions where not all form field mappings are used.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2023730

</td><td>

Trace collector Epic

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

UI Builder \(Family Channel\)

 PRB2023628

</td><td>

Configuration table, APIs and ACLs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1917016

</td><td>

TinyMCE Editor is not dark theme compatible in the builder screen

</td><td>

The **Description** field and the 'Preview' and 'Default Value' sections don't honor the dark theme.

</td><td>

1.  Log in to an instance as an admin.
2.  Navigate to **Catalog Builder**.
3.  Select the **Admin Profile** icon.
4.  Set the theme as dark.
5.  Select **Build From Scratch** \(the create catalog item flow\).
6.  Select **Standard**.
7.  Continue the flow from the pop-up.
8.  Scroll a bit.

 Observe that the **Description** field doesn't honor the dark theme. The same issue is also seen in the 'Preview' and 'Default Value' sections.

</td></tr><tr><td>

UI Field Administration

 PRB1919959

</td><td>

An exception displays in a syslog when adding/removing a property in full-screen

</td><td>

TableName is returned as an empty string in a function, which causes tabledescriptor to throw an error in the log during initialization.

</td><td>

1.  Log in to a Zurich or Australia instance as an admin.
2.  Navigate to kb\_knowledge\_base.list or sys\_user.list.
3.  Select any record or user.
4.  Open the related list.
5.  Edit any properties.
6.  Select **Save**.
7.  View syslog.list.
8.  Order it by 'Created by most recent' first.

 Notice the following exception: 'Table name can't be null: java.lang.IllegalStateException: Table name can't be null: com.glide.db.TableDescriptor.init\(TableDescriptor.java:98\)...'

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
3.  Create a field type 'Price'.
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

 PRB1982868

</td><td>

The pop-up related to the Comment/Work Note web link only displays in the boundary of the 'Compose' tab

</td><td>

The message, 'The URL you entered seems to be an external link. Do you want to add the required http:// prefix' is confined to the 'Compose' section and not overlaying the page. This occurs in the CSM workspace, Service Operations Worspace \(SOW\), and the HR workspace. This issue occurs in Safari browsers, but has been resolved in Chrome browsers.

</td><td>

1.  Open a Safari browser.
2.  Log in to a Xanadu instance.
3.  Open the CSM workspace.
4.  Open any non-closed incident.
5.  Navigate to the Activity Stream.
6.  Navigate to the 'Compose' section.
7.  Under 'Subject', select the **3 dots \(...\)** if formatting options aren't available.
8.  Select the **Link** button.
9.  In the URL field, enter 'www.servicenow.com'.
10. Select the **Save** button.

 Observe the message, 'The URL you entered seems to be an external link. Do you want to add the required http:// prefix'. The message is confined to the 'Compose' section, and not overlaying the entire page.

</td></tr><tr><td>

UI Field Administration

 PRB1985085

</td><td>

Quick action visibility script is executed in global scope, preventing access to scoped script includes

</td><td>

The quick action runs into an error: 'Evaluator.evaluateString\(\) problem: java.lang.SecurityException: Illegal access to package\_private script include...'

</td><td>

1.  Create a quick action in a scoped app.
2.  From the visibility script, call a script include that is accessible only from the same scope.

 Notice the quick action runs into an error: 'Evaluator.evaluateString\(\) problem: java.lang.SecurityException: Illegal access to package\_private script include CMDBGenAICIFormContextualHelp: caller not in scope sn\_cmdb\_gen\_ai: com.glide.script. RhinoEnvironment. checkScriptableAccess \(RhinoEnvironment.java:723\) com.glide.script. ARhinoScope. checkScriptableAccess \(ARhinoScope.java:134\)'. This happens because the visibility script is evaluated in the global scope.

</td></tr><tr><td>

UI Field Administration

 PRB1998819

</td><td>

WWNAglobal utils should be removed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2025633

</td><td>

AI Agent modified fields API returns aiCreated instead of isAiCreated in JSON response

</td><td>

The Boolean field is named incorrectly.

</td><td>

1.  Provision an instance with Gen AI installed.
2.  Open any existing record page \(for example, an incident in Ui16\).

Observe the **AI Agent modified** field API response.

3.  Inspect the JSON response body.

 Expected behavior: The Boolean field is named 'isAiCreated'.

 Actual behavior: The Boolean field is named 'aiCreated'.

</td></tr><tr><td>

UI Form Administration

 PRB1999196

</td><td>

The citation URL is retained and fields are highlighted when the user logs in to an instance again

</td><td>

The highlight should happen only if the user selects links in a summary or the email outputs.

</td><td>

 

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

Upgrade Center

 PRB1889947

</td><td>

Instance nodes don't appear and an error appears: 'javax.crypto.AEADBadTagException: Error finalizing cipher data: mac check in GCM failed'.

</td><td>

Instance JVMs won't start after the error, 'java.io.IOException: javax.crypto.AEADBadTagException: Error finalizing cipher data: mac check in GCM failed'.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB1992027

</td><td>

'Add node' automation times out too quickly

</td><td>

The 'Add node' automation times out before the node is online. PluginManager takes a long time to complete initialization.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB2023239

 [KB3015307](https://hi.service-now.com/kb_view.do?sysparm_article=KB3015307)

</td><td>

There is a mismatch in the Glide version between the app node and the database following an upgrade

</td><td>

A new code path introduced the MariaDBI18NSQLFormatter class. When the sys\_properties record of the 'com.glide.db.session \_language\_collation\_feature' property is set to true, it takes a code path on upgrade or restart where an instance will not come up. When 'com.glide.db.session \_language\_collation\_feature' is false, the code path exits early and doesn't cause this issue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Usage Analytics

 PRB2021289

</td><td>

Long session durations are observed for few Usage Insights Sessions, causing inaccurate session duration metrics

</td><td>

A fix for long session duration in some Usage Insights sessions.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1969085

 [KB2677276](https://hi.service-now.com/kb_view.do?sysparm_article=KB2677276)

</td><td>

GraphQL schema changes for client-interaction.graphl in ux-metrics

</td><td>

The user sees error logs from the ClientMetricsRestService.java file. The error logs are logged to the syslog table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1986291

</td><td>

List dynamic routing shouldn't be applied when creating a record from a related list

</td><td>

Dynamic routing is handled within the recordRoutesMapping Client Script Include. Kb\_knowledge mapping uses source\_component: 'list' to route article clicks to kb\_view. When the **New** button is selected on a related list, the kb\_view route is incorrectly applied. Since kb\_view can't handle new records, the page breaks.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1987200

</td><td>

GLOBAL\_NAVIGATION\_REQUESTED isn't routing to the feature on select after a hard refresh of the page

</td><td>

When the user selects the desktop notification, it doesn't navigate back to the workspace.

</td><td>

1.  Enable desktop notifications in the Agent Chat.
2.  Make an agent self available.
3.  When an incoming work item appears for the agent, select the desktop notification.

 Observe that it doesn't navigate back to the workspace.

</td></tr><tr><td>

UX Framework

 PRB2002772

</td><td>

Preset for the presentational list \(nested inside the record list bundle\) wasn't discovered during pre-population

</td><td>

The list is completely broken.

</td><td>

1.  On a base instance, build a custom UIB page where the record list component is nested deeply under a tabs viewport.
2.  Perform cache.do.
3.  Visit the UIB page.

Observe that the list component is empty and broken. No data is rendered.

4.  Visit the SOW list page: /now/sow/list.

 Observe that the SOW list page is also broken and empty.

</td></tr><tr><td>

UX Framework

 PRB2018001

</td><td>

An blank page issue on some nodes during upgrade

</td><td>

This issue occurs in Australia instances.

</td><td>

1.  Upgrade the instance.
2.  Navigate to the node.

 Observe that an empty page is displayed with a spinning wheel.

</td></tr><tr><td>

UX Framework

 PRB2023614

</td><td>

In-product surveys MVP

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2030213

</td><td>

When a user navigates between two pages that both have IPS surveys configured, the survey triggered on the first page isn't dismissed on navigation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1752802

</td><td>

The virtual agent designer page isn't accessible on Safari

</td><td>

All seismic and Core UI pages should work on Safari 17.1+ for Washington and 17.3+ for Xanadu.

</td><td>

1.  Open a Safari browser.
2.  Navigate to **All** &gt; **Virtual Agent** &gt; **Designer**.

 Observe the following error: 'Safari and older versions of internet Explorer are unsupported browsers, please switch to a different or newer browser.'

</td></tr><tr><td>

Virtual Agent

 PRB1977665

</td><td>

The 'Pagination' API doesn't reset totalSearchResultsCount if a search term is removed

</td><td>

 

</td><td>

1.  Execute a topic with dynamic input.
2.  Scroll through the input list.

Note that the totalSearchResultsCount is 0 in the response for /options, during scrolling.

3.  Enter a search text in the input.

Note that totalSearchResultsCount has some valid integer values in the response for /options.

4.  Remove the search text in the input.

 Note that totalSearchResultsCount still has the same value from step three in the response for /options and isn't reset to 0.

</td></tr><tr><td>

Virtual Agent

 PRB1985280

</td><td>

Duplicate attachment is displayed in Virtual Agent after portal refresh

</td><td>

 

</td><td>

1.  Open an instance in two browsers.
2.  In browser one, impersonate the agent 'Fred Luddy'.
3.  Set the agent as available in Service Operations Workspace.
4.  Switch to browser two.
5.  Impersonate an admin.
6.  Initiate a chat from the portal or web-client.
7.  Connect to a live agent.
8.  In browser one, accept the chat as the agent.
9.  Send any image as end-user to agent.
10. Refresh the portal at end-user.

 Expected behavior: Nothing happens.

 Actual behavior: The duplicate attachment/image is displayed only in Virtual Agent.

</td></tr><tr><td>

Virtual Agent

 PRB1999511

</td><td>

Message preview and unread badge count don't work on page refresh

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

 PRB2004944

</td><td>

Teams conversations can pull in context from NAP if not using a NAP channel

</td><td>

When the user executes a skill, it should prompt for more context if needed instead of using NAP context.

</td><td>

1.  Set up an instance using NAP with the standard chat widget \(not enhanced chat\).
2.  Make sure the instance has Teams integration installed for NAVA.
3.  In SOW, navigate to an incident as a user.
4.  In Teams, as the same user, start a conversation.
5.  Execute the 'Summarize Record' skill.

 Expected behavior: The skill prompts for the record to summarize.

 Actual behavior: The skill uses the incident from NAP context.

</td></tr><tr><td>

Virtual Agent

 PRB2006240

</td><td>

The Virtual Agent server doesn't process pre-chat surveys for bot 2 bot

</td><td>

Users aren't routed to a live agent in bot to bot conversations. This was due to a misconfiguration where pre-chat survey was enabled and the user wasn't able to provide a response. Interactions aren't assigned to the queue or an agent in Agent Workspace. It was working when the user first upgraded, but recently has stopped.

</td><td>

1.  Start a conversation in crescendo using the ServiceNow Virtual Agen API.
2.  Send a request to transfer to a live agent using endpoint /api/sn\_va\_as\_service/bot/integration.

 Notice that the conversation doesn't get routed to the live agent.

</td></tr><tr><td>

Virtual Agent

 PRB2012889

</td><td>

vaSystem.getSearchText isn't working with off-Glide

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2013847

</td><td>

Create a scriptable API for endChatSummarization

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2013993

</td><td>

The deployment channel for a conversation isn't populated in context variables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2015140

</td><td>

Multiple interactions are created during live agent execution

</td><td>

This only happens when a conversation is reset or abandoned.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2015460

</td><td>

Now Assist Portal's unread conversation count disappears after the execution is started via AI Agent triggers or Runtime APIs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2015866

</td><td>

Handshake fails when it fails to load an in-progress conversation

</td><td>

The same error impacts async tool execution intermittently.

</td><td>

1.  Impersonate any user who has existing open conversations.
2.  Open Now Assist Portal.

 Expected behavior: It should load the chat client successfully with a new or older conversation.

 Actual behavior: It keeps loading and throws an error.

</td></tr><tr><td>

Virtual Agent

 PRB2017392

</td><td>

Add topic, agent execution to the sys\_cs\_now\_ assist\_execution table for NextWave

</td><td>

When a topic/agent is run, the sys\_cs\_now\_assist\_execution doesn't populate.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2018098

</td><td>

AI agents are incorrectly displayed on the Virtual Agent's topics list

</td><td>

On Virtual Agent, users see AI agents in the 'View All Topics' section under the 'Others' category. But none of those agents are marked to be visible on that section.

</td><td>

1.  Open Virtual Agent.
2.  Navigate to the 'View All Topics' section.
3.  Scroll to the 'Others' section.

 Observe that multiple AI Agents are visible there.

</td></tr><tr><td>

Virtual Agent

 PRB2018878

</td><td>

Employeeslate gets a 404 error for promoted-skills

</td><td>

 

</td><td>

Navigate to Employeeslate's home.

 Observe the 404 error.

</td></tr><tr><td>

Virtual Agent

 PRB2021412

</td><td>

Send flag to AIEL to identify new vs. existing catalog pages

</td><td>

When a catalog item is opened in the NextWave interactive view, AIEL needs to be able to distinguish whether the catalog page being rendered is a new \(modern/interactive\) catalog page or an existing \(legacy\) catalog page. Currently, no flag is sent to AIEL to make this distinction, which can cause incorrect rendering behavior or routing decisions. A flag should be passed to AIEL at the time of catalog page load so it can apply the appropriate logic based on the page type.

</td><td>

1.  Open Now Assist NextWave chat experience.
2.  Trigger a catalog item via conversational flow.

 Observe that AIEL doesn't receive any flag to differentiate between a new catalog page and an existing/legacy catalog page. This can result in incorrect behavior when AIEL applies logic without awareness of the page type.

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

 PRB2024076

</td><td>

Pickers aren't honoring pre-selected options

</td><td>

This works in the web version and is considered a feature gap.

</td><td>

1.  Set up a topic that has pre-selected options.
2.  Execute a topic in MS Teams.

 Expected behavior: The pre-selected options defined in the topic should be presented to the user as selected.

 Actual behavior: An empty picker is presented with nothing selected.

</td></tr><tr><td>

Virtual Agent

 PRB2024849

</td><td>

Simplified handshake for NextWave needs fixes for session creation, channels, and context

</td><td>

The existing session needs to be looked up by conversation before creating a new one. Also, if the consumer account context name is provided, it needs to be stamped and associated with the consumer account when created. Finally, the channel user profile needs to be properly resolved for channels.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2025027

</td><td>

Create a custom fallback message for AI Control Tower \(AICT\) Assistant

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2025311

</td><td>

Add an ai\_greeting type mapping in getContextProfile MessagesNoDomain to support a Premium Chat greeting message feature

</td><td>

The Now Assist Virtual Agent \(VA\) admin UI saves static AI greeting messages as sys\_cs\_context \_profile\_message records with type=ai\_greeting. For these to load correctly, getContextProfile MessagesNoDomain in NowAssistIn VAadmin ConsoleUtil needs an explicit branch mapping ai\_greeting → aiGreetingMessage. Without this Glide-services change, the greeting message isn't populated for multi-domain instances when the feature ships.

</td><td>

1.  On a multi-domain instance, navigate to **Now Assist VA admin UI** &gt; **Chat Experience** &gt; **Premium Messages tab**.
2.  Configure a static greeting message.
3.  Save.
4.  Refresh the page.
5.  Navigate back to the chat.

 Observe that the custom greeting message isn't populated even though the message was saved earlier.

</td></tr><tr><td>

Virtual Agent

 PRB2025956

</td><td>

Resolved issues after introducing four tables for Virtual Agent \(VA\) analytics

</td><td>

The search-related analytics can be written to the four tables instead of sys\_ci\_analytics as event entries.

</td><td>

1.  Make sure sn\_nowassist\_va.analytics .persistence\_strategy = 'table'.
2.  Launch VA client.
3.  Type anything in the search.

 Observe that all the expected entries are in the new tables and view.

</td></tr><tr><td>

Virtual Agent

 PRB2026053

</td><td>

sys\_cs\_context\_profile\_topics should be sent to the off-Glide cache for Authorizing Official \(AO\) to read

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2026723

</td><td>

In OGChannels, there should be a picker search update

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2026804

</td><td>

getBrandingConfig\(\) doesn't provide the correct response in NextWave

</td><td>

api/sn\_nowassist\_va/ og\_branding\_configs/ \{deploymentId\} doesn't provide the correct response for branding configuration. It's missing a **Value** field and the type is null for the first item.

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

 

</td></tr><tr><td>

Virtual Agent

 PRB2030245

</td><td>

External users can't upload files

</td><td>

There's an HTTP 422 error and the file fails to upload.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2031950

</td><td>

AI-user fetch issue

</td><td>

The conversation user for the ZTSD flow is AI L1 Service Desk Specialist, which is the identity type ai\_agent. The cache configuration get\_user\|table:\{table\} \|field:\{field\}\|value:\{value\} explicitly ignores users of type 'ai\_agent'.

</td><td>

Perform a cache fetch call for the cache key 'get\_user\|table:\{table\} \|field:\{field\}\|value:\{value\}' for any user of the identity type 'ai\_agent'.

 See that it doesn't return the **User** field value.

</td></tr><tr><td>

Virtual Agent

 PRB2032108

</td><td>

Glide-side changes for the NextWave release

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1993741

</td><td>

When live\_agent\_only is set to true, the agent chat triggers the greetings topic instead of going to the live agent

</td><td>

The /esc portal agent chat is configured to only trigger the live agent. However, when the user selects the **Virtual Agent** icon, it triggers the greetings topic and doesn't go to the live agent. When the user ends the first conversation and creates another conversation, it then goes straight to the live agent. The issue only occurs the first time the user selects the **Virtual Agent** icon in the session. It also only happens for Now Assist virtual agent sessions.

</td><td>

1.  Enable Now Assist in Virtual Agent.
2.  Configure the agent chat config for the /esc portal.
3.  Disable all the other agent chat configs, only keeping one active.
4.  Navigate to /esc.
5.  Select the **Virtual Agent** icon.

 Expected behavior: It triggers the live agent support topic.

 Actual behavior: It triggers the greetings topic. However, if the user ends the conversation and creates a new conversation, it goes straight to the live agent.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2030686

</td><td>

The **Stop Flow** button is incorrectly displayed in the Virtual Agent input field during file upload

</td><td>

The **Stop Flow** button should only be visible when a dynamic loader control is active, and it should not appear for normal file upload controls.

</td><td>

1.  Create a NLU topic with file upload.
2.  Open the topic in standard Virtual Agent chat.

 Observe the **Stop Flow** button in the bottom text input field when the file upload control appears.

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

 PRB1973625

</td><td>

Support unzipped font size up to 20 MB in Word Doc API

</td><td>

The property com.snc.word\_doc\_api .unzip\_word\_size\_limit\_mb supports only up to 10 MB file size. This is an enhancement request to support up to 20 MB.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 9 Hotfix 2](https://downloads.docs.servicenow.com/enus/zurich/rn/hotfix/zurich-patch-9-hf-2.pdf)
-   [Zurich Patch 9 Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9-hf-1.md)
-   [Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)
-   [Zurich Patch 8 Hotifx 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3055427)
-   [Zurich Patch 8 Hotfix 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8-hf-2-PO.md)
-   [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)
-   [Zurich Patch 7b Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7b-hf-1.md)
-   [Zurich Patch 7b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3006227)
-   [Zurich Patch 7a Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7a-hf-1-PO.md)
-   [Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)


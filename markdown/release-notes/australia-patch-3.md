---
title: Australia Patch 3
description: The Australia Patch 3 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/australia-patch-3.html
release: australia
topic_type: reference
last_updated: "2026-06-16"
reading_time_minutes: 157
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 3

The Australia Patch 3 release contains important problem fixes.

-   **Australia Patch 3 was released on June 16, 2026.**
    -   Build date: 06-12-2026\_1106
    -   Build tag: glide-australia-02-11-2026\_\_patch3-05-25-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A03.00.xlsx).

## Overview

Australia Patch 3 includes 502 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-ap3.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Australia Patch 3 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 3, refer to [Australia Patch 3 security fixes](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3035030).

## Changes in Australia Patch 3

-   **[Activate a pre-release feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/activate-prerelease-feature.md)**

    Activate a pre-release feature on the instance so your users can try it out and provide feedback to the product team.

-   **[Activate Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/activate-unlimited-breakdowns.md)**
    -   Starting with Australia Patch 3, if the instance is eligible, this plugin is installed automatically.
    -   Activate Data snapshots for each eligible indicator, either one-at-a-time or in bulk.
-   **[Authentication release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/authentication-rn.md)**
    -   Email OTP as an authentication factor for AI voice service: Use Email OTP as a standalone factor, a primary factor, or a secondary factor in AI voice agent authentication flows. When a caller reaches the voice agent, a one-time password is sent to their registered email address. The caller provides the password to complete authentication.
    -   KBA for AI voice service: Use the KBA setup to configure Knowledge-Based Authentication \(KBA\) for the voice channel. Choose from base system questions at both the identification level and the authentication level. AI voice service mappings are populated automatically from your Assistant Designer selection, so manually mapping voice services is no longer a mandatory step in the KBA setup.
    -   Authenticate callers at the start of every call: Prompt callers for authentication or identification details at the start of every call, before the voice-only assistant responds to any request, using the Authenticate at the start of the call option on the Assistant Designer's Caller verification page.
-   **[Clone Admin Console release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/clone-admin-console-rn.md)**

    The ServiceNow® Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances. Clone Admin Console was enhanced and updated in the Australia release.

-   **[Code Signing actions and required roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/cs-actions-roles.md)**

    Reference table of Code Signing actions, their descriptions, and the roles required to perform them.

-   **[Create a Universal Request from the Supplier Collaboration Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/create-universal-request.md)**

    Create a Universal Request \(UR\) in Employee Center when your request involves multiple departments or the right department to contact is unclear.

-   **[Data snapshots and multiple breakdowns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/multi-level-breakdowns.md)**

    If you have Australia Patch 3 or later, the plugin is installed automatically on qualified instances.

-   **[Data snapshots jobs and tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/ds-jobs-tables.md)**

    Instance Eligibility Check Job for Data Snapshots and Instance readiness for Data snapshots Scheduled jobs installed.

-   **[Deactivate a pre-release feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/deactivate-prerelease-feature.md)**

    Deactivate a pre-release feature if it is not working as expected or if you no longer need the feature.

-   **[Feature Preview Program](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/feature-preview-program.md)**

    The Feature Preview Program provides access to pre-release capabilities on your instance. You can activate, test, and provide feedback on individual features before they are generally available.

-   **[Hermes background jobs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/hermes-settings-background-jobs.md)**

    These background jobs are associated with Hermes settings. The table lists their default run frequencies and descriptions.

-   **[Hermes Settings page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/c-hermes-settings.md)**

    The Hermes Settings page is a centralized interface that enables Hermes administrators and maintenance users to monitor and control the configuration properties that govern the Hermes Messaging Service.

-   **[Install Universal Request for Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/install-universal-request-spo.md)**

    Install the Universal Request for Source-to-Pay Operations \[sn\_fsc\_ur\_common\] plugin to enable the Universal Request in Sourcing and Procurement Operations.

-   **[Limitations and requirements for Data snapshots](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/limitations-mlb.md)**

    If you have Australia Patch 3 or later, the Data Snapshots \(com.snc.pa.mlb\) plugin is installed automatically on eligible instances. This includes instances with domain separation, but on such instances the Data snapshots feature is disabled when the first job runs.

-   **[Manage a background job in Hermes Messaging Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/manage-a-background-job.md)**

    Manage background jobs in Hermes Messaging Service to control when and how often scheduled tasks run. You can make a job inactive, re-enable it, or adjust its interval from the Hermes Settings page.

-   **[Managing Hermes settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/manage-hermes-settings.md)**

    View, modify, and manage configuration properties that control the behavior of Hermes Messaging Service. You can update property values, manage background job states, or adjust settings where automated detection is unavailable.

-   **[Performance Analytics release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/performance-analytics-rn.md)**

    If you have Australia Patch 3 or later, the Data snapshots plugin is installed automatically if you have RaptorDB Professional. If your instance is also domain separated, the Data snapshots feature is installed but disabled.

-   **[Reviewing prediction errors with the Observability Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/prediction-errors-observability-dashboard.md)**

    View this table's records directly by entering `ml_predictor_error_logs.list` in the navigator.

-   **[ServiceNow AI Platform core feature release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/core-platform-rn.md)**
    -   The Feature Preview Program provides a centralized location to discover, activate, and test pre-release capabilities on your instance. When a pre-release feature is added to your instance, you receive a notification and can access the Feature Preview Program to review feature details, activate features for testing, and provide feedback.
    -   Use the Feature Preview Program to choose which pre-release capabilities to activate and test on your instance.
-   **[Theming for AI Search in Service Portal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/ais-sp-css-vars.md)**

    `transparent`

-   **[Update Hermes messaging settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/view-and-modify-a-hermes-property-value.md)**

    Review and modify the current the Hermes configuration properties to control Apache Kafka integration, topic management, and other messaging behavior.


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

Change Management

 PRB2021441

 [KB3032668](https://hi.service-now.com/kb_view.do?sysparm_article=KB3032668)

</td><td>

Unable to rollback the plugin 'com.snc.itsm. foundation.license \_control'

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2007256

 [KB2925734](https://hi.service-now.com/kb_view.do?sysparm_article=KB2925734)

</td><td>

The text search doesn't return results in non-English languages

</td><td>

After downloading language plugins and switching the system language to a non-English language, results aren't returned when the property 'glide.db\_ query.replace\_ distinct\_with\_ groupby' is set to 'false.' When the language is set to English, results are returned.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Password2 Encryption

 PRB2015257

 [KB2978056](https://hi.service-now.com/kb_view.do?sysparm_article=KB2978056)

</td><td>

There's excessive growth on the sys\_rollback \_incremental table and higher binlog generation due to the 'Mass Encryption' job

</td><td>

This causes a large increase in the disk space on the database server.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Related Lists

 PRB2025356

 [KB3032264](https://hi.service-now.com/kb_view.do?sysparm_article=KB3032264)

</td><td>

A user can't add records in a related list because of the strict ACL check and missing ACLs for required roles

</td><td>

Users with missing ACLs are not able to add new records in the related list due to a strict ACL check.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Server-side scripts

 PRB1994381

 [KB3006010](https://hi.service-now.com/kb_view.do?sysparm_article=KB3006010)

</td><td>

Discovery has issues on some node after upgrading in Australia

</td><td>

After upgrading to Australia, JavaScript running in app nodes fails to call Java functions. The following warning appears: '\*\*\* WARNING \*\*\* Evaluator: com.glide.script. RhinoEcmaError: undefined is not a function.' This impacts various features, including Discovery and Event Management.

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

Access Analysis Instrumentation API

 PRB1984283

</td><td>

Analyze Access in any record's hamburger menu isn't working

</td><td>

Adding 'access-management' into the URL doesn't work either; it navigates to Access Analyzer's 'Analyze Permissions'.

</td><td>

1.  Navigate to any record in any table.
2.  Right-click the header or select the hamburger menu.
3.  Select **Analyze Access**.

 Expected behavior: The page redirects to Access Analyzer to analyze that record.

 Actual behavior: 'The page you are looking for cannot be found'. It navigates using the previous URL.

</td></tr><tr><td>

Access Analyzer

 PRB1993028

 [KB2820230](https://hi.service-now.com/kb_view.do?sysparm_article=KB2820230)

</td><td>

\(Access Analyzer\) Instance scan jobs can hang and are not terminated due to checks not being optimized

</td><td>

Instance scan jobs triggered by the Access Auditor Suite, which is a part of the Access Analyzer \(sn\_access\_analyzer\) store application, may hang or fail to terminate. This may cause multiple jobs to accumulate over several days, consuming multiple workers and preventing other jobs from running. This may cause performance issues on the instance. This issue affects Access Analyzer \(sn\_access\_analyzer\) versions 6.0.0 through 6.0.5, as well as version 6.1.0.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

ACL Engine

 PRB1998171

</td><td>

The store\_app\_write\_audit\_acl table was created in a Store app scope instead of the global scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2005727

</td><td>

Navigation fails for sources beyond sliding windows in an activity stream

</td><td>

When selecting a citation source in an incident summary response, navigation doesn't work properly if the cited activity \(comment or email\) is more than three pages away or above the current activity stream view. The user receives a message stating 'The source may be hidden in your current view', even though the source exists and isn't filtered.

</td><td>

1.  Navigate to any instance on track/anowassist.
2.  Open Service Operations Workspace.
3.  Open a record with 200+ activity stream entries.
4.  Scroll to a recent AI-generated response containing citation references.
5.  Select **Show sources**.

The cited source \(comment/email\) should be an older entry — at least 3+ pages above the current viewport.

6.  Select the citation link with work notes/comments.

</td></tr><tr><td>

Activity Stream

 PRB2008384

</td><td>

The **Copy** button on journal entries doesn't always copy text or notify users correctly

</td><td>

This is reproducible in UI16 and Workspace.

</td><td>

1.  Navigate to any relevant workspace.
2.  Open any incident record.
3.  Turn on the 'Rich text editor' in activity stream's **Compose**.
4.  Add a work note or comment to the activity stream with some of the text set to bold.
5.  Select the **Copy to clipboard** button on the new journal entry.

 Expected behavior: When rich text is copied, a notification should display saying 'Copied to clipboard'. When pasted into a plain text editor, there shouldn't be \[code\] tags around the text.

 Actual behavior: When rich text is copied, a notification doesn't display, and when pasted into a plain text editor, there shouldn't be \[code\] tags around the text.

</td></tr><tr><td>

Activity Stream

 PRB2011415

</td><td>

AI skill attribution issue in an activity stream

</td><td>

Activity stream entry grouping logic should account for AI skills registered via setValueWithAuditIdentity. The grouping currently does not use sys\_updated\_by as the grouping key when UserAgentContext isn't set, so field-level audit entries attributed to distinct AI skill sys IDs along with the session user involved are not getting shown as expected.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2013162

</td><td>

Add filter a configuration, such as a slushbucket

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2013164

</td><td>

Integrate translations into the Java REST API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2013167

</td><td>

Dynamic translations in the activity stream convert to Lit

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2013171

</td><td>

Create a Java REST API

</td><td>

This is a product update.

</td><td>

 

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

Example without activity stream: Navigate to /sys\_dictionary.do and open any record.

Example with activity stream: Navigate to /incident.do and open any record.

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

For the Core UI only, update the activity stream icon for AI specialist vs Agentic Workflow

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

Advanced Work Assignment

 PRB1996219

</td><td>

The END\_WRAP\_UP event is published twice when wrap-up is timed out

</td><td>

This behavior causes 'openframe\_wrap\_up\_submitted' to trigger twice, which isn't expected while users are using OpenFrame to handle wrap up with external systems.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB2026676

</td><td>

Enhanced updateSegment API \(wrap-up\) to support agent-initiated wrap-up

</td><td>

As a CCaaS Developer, the updateSegment API should be able to be used in the CCaaS plugin. This API should allow users to update a wrap-up segment at the same time as closing/updating the segment without requiring a separate API call. This allows the voice plugin to support agent-initiated wrap-up. Agents should have the ability to initiate a wrap-up before the call ends. If the system has wrap-up with a timer, they should get a timer on the wrap-up modal to provide the count down timer until the wrap-up is submitted.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1992614

</td><td>

Dirty screens in Document Object Model \(DOM\) experience data loss if one of the middle tabs are closed, triggering a screen reorder and refresh

</td><td>

Screens between deleted screens lose edited data due to incorrect DOM detachment/reattachment. When incident is closed, screens 2 and 4 are removed. The updateChildren algorithm uses two-pointer comparison \(from both ends\). Elements at the ends that match are patched in place, but elements in the middle that need repositioning are moved via insertBefore. This movement triggers a re-render of sn-canvas-screen, and due to vnode-DOM desynchronization \(the view renders a p but loadScreen manually replaces it with the macroponent\), the section element is destroyed and recreated. This causes hook-insert to fire, which calls loadScreen again, recreating the macroponent and losing all unsaved data.

</td><td>

1.  Open the Service Operations Workspace list URL.
2.  Navigate to an incident list.
3.  Open any incident.
4.  Select the **+** menu.
5.  Select **Create Interaction**.
6.  Edit the new interaction record fields.
7.  Navigate to an incident record.
8.  Open any reference field in a sub tab.
9.  Close the incident record.

 See that the focus shifts to an interaction record and the edited field values are lost.

</td></tr><tr><td>

Agent Chat

 PRB1993857

</td><td>

Agent chat inbox notifications appear in HTML

</td><td>

The incident card on the agent chat appears as HTML on a desktop notification.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2000390

</td><td>

The date format is incorrect in the Active Chat window

</td><td>

The date/time format is displayed as 'MMM DD, YYYY HH:MM AM' instead of 'DD-MM-YYYY HH:MM:SS' in the Active Chat window.

</td><td>

1.  Enable the conversation history by navigating to **Conversational Interface** &gt; **Agent chat settings**.
2.  Set the value for 'Number of conversations to display'.
3.  Hop to an instance where Advanced Work Assignment \(AWA\) is configured in two browsers.
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

 Actual behavior: The date/time format is displayed as 'MMM DD, YYYY HH:MM AM' in the Active Chat window.

</td></tr><tr><td>

Agent Chat

 PRB2013947

</td><td>

Inbox Advanced Work Assignment \(AWA\) interactions are not presented according to the **Configuration** field and order for the walkup experience

</td><td>

When an agent receives multiple chats in Service Operations Workspace \(SOW\), they are initially displayed in descending order, with the most recent chat at the top. However, after a refresh, the chat order appears to change and seeimingly displays in a different order.

</td><td>

1.  Open an instance.
2.  Impersonate an agent with the role 'system\_administrator'.
3.  Open SOW.
4.  Set the agent status as 'available'.
5.  Open the instance again in a new incognito tab, or in any another browser.
6.  Initiate 4-5 live agent chats by impersonating the end users from Service Portal.
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

1.  Enable the 'Conversation history' feature in Agent Chat settings.
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

Update WorkItemResponder's onEnter and OnExit to add and remove notifications in the ui\_notification\_inbox table. Also, create a system property \(glide.awa.work\_item.notifications.enabled\) to determine whether to show or hide user preference at the agent level.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2022906

</td><td>

Add user preference for app shell notifications

</td><td>

Add support to display a new user preference 'Inbox Workspace Notifications' based on the system property glide.awa.work \_item.notifications .enabled.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2022911

</td><td>

Next Experience app shell changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2022913

</td><td>

Component inbox logger changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2023682

</td><td>

Add the interaction number to desktop notifications to differentiate between interactions

</td><td>

The desktop notification should contain the IMS number to indicate which chat the notification is for.

</td><td>

1.  Enable desktop notifications in the Agent Workspace.
2.  Start a live agent chat so that a new desktop notification is rendered.

 Expected behavior: The desktop notification contains the IMS number to indicate which chat the notification is for.

 Actual behavior: The desktop notification only says that a new chat arrived.

</td></tr><tr><td>

Agent Chat

 PRB2026678

</td><td>

Dynamic wrap-up timer update on the UI when a call has ended

</td><td>

Agents should have the wrap-up timer updated automatically when CCaaS provides the wrap-up context after a call has ended. The wrap-up modal should be refreshed automatically without intervention. The wrap-up modal shouldn't require users to close or open to have the timer count down.

</td><td>

 

</td></tr><tr><td>

Agile Development

 PRB2022589

</td><td>

Add 'None' choice to the **rm\_epic.status** field and make it the default for new epics

</td><td>

The **Epic Status** field \(rm\_epic.status\) currently doesn't include a 'No status' option, which prevents epics from having an unset/neutral status. This causes ambiguity in reporting and makes it difficult to distinguish between epics that have not yet been assigned a status versus those intentionally marked as green, yellow, or red.

</td><td>

1.  Navigate to **Agile Development** &gt; **Epics** \(or open an Epic from a board/backlog\).
2.  Open any active Epic record.
3.  Select the **Status** field.

 Expected behavior: 'No status' is available as a selectable option to represent epics with no status assigned, enabling accurate status transition tracking for usage analytics.

 Observed: 'No status' isn't available as an option in the **Status** field list. Available options are limited to green, yellow, and red.

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

 PRB2018916

</td><td>

AI Agent execution fails with 'Tool access denied' for triggering user after the update set migration

</td><td>

After migrating AI Agents \(built in Agent Studio\) from a development environment to a client test environment via update set, the agents fail to execute. The triggering user receives an error indicating that they don't have access to the agent's tools, and the agent never starts.

</td><td>

1.  In a source instance, build an AI Agent in Agent Studio with one or more tools \(e.g. a subflow tool\).
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

When running AutoEval for the Enterprise Architecture Explorer – Query Agent, the evaluation run gets stuck indefinitely while processing certain questions and datasets. During execution, AutoEval doesn't progress to completion, progress keeps retrying without advancing, and the run never completes successfully. GenAI logs repeatedly show: 'JSON\{ "facts": \[\]\}Show more lines'. Despite retries, no new facts are generated and the evaluation pipeline makes no forward progress.

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

The API sn\_cs\_offglide. OffGlideScriptObject. generateAuthorizationInfo\(\) creates JWT with current user sessions, even though the userID value is passed in the request.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2025974

</td><td>

A user session is logged out when opening AI-generated interaction records

</td><td>

The user session is logged out when opening AI-generated interaction records that were created/updated by the incident\_intelligence\_agent. The interaction record remains in the WIP state, even though the associated conversation has been marked as faulted. The issue is specific to the in Service Operations Workspace \(SOW\) workspace view, as opening the same record in platform view works without issue.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2030410

</td><td>

An instance isn't invoking DARE calls due to new properties not being allowed in the cache configuration's invalidation script

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
2.  In Service Portal, give an utterance, such as 'using smartsheet agents, look up groups stream'.

 Observe that the tool isn't able to retrieve data.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB1980207

</td><td>

Implement the logic of 'Mark as read' in the notification

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB1986457

</td><td>

The icon color on notifications uses a hard-coded hash value

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB1994093

</td><td>

'Mark all as read' isn't working due to GlideRecordSecure and updateMultiple methods being used

</td><td>

 

</td><td>

1.  Trigger notifications to any non-admin user.
2.  Log in.
3.  Navigate to a portal.
4.  Open a notification tray.
5.  Select **Mark all as read**.

 Notice that it's not marking as read in the background.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2010223

</td><td>

Glide assets release

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2011879

</td><td>

Allow the 'Notification content' table to have separate records per experience

</td><td>

Currently, users can only map a single experience for the portal. Allow the 'Notification content' table to have separate records per experience and also allow content configuration to map multiple experiences.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2012479

</td><td>

AIX Webserver Glide integration

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

The chat works correctly.


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

AI Experience Framework - Glide

 PRB2027770

</td><td>

Remove the 'Applicability' table \(sys\_aix\_applicability\) and move the fields **applicable for** and **not applicable for** glide\_list \(user\_criteria\) into a multi-theme table

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Gateway

 PRB2010156

</td><td>

A scheduled job overwhelms a clickhouse service in sk8s with queries

</td><td>

An app has a scheduled job that runs daily that uses a query service to query AI Gateway data for the previous day. There's a large number of instances querying at the same time \(around 12,000\), causing every clickhouse node in the cluster to hit its max concurrent query limit and start rejecting incoming requests.

</td><td>

 

</td></tr><tr><td>

AI Gateway - Security

 PRB2024062

</td><td>

AI Gateway security Q2 complete feature backport

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1951236

</td><td>

In DirectUserImport, a multiple user match isn't reported

</td><td>

The connectors create user mapping for the first matched user, but not for the second user without reporting an error for the second user.

</td><td>

1.  For a known user ID, create two users in sys\_user with the 'First name' column containing the same user ID as the value.
2.  Configure the 'first\_name' column as a mapping field in the connector configuration.
3.  Run user mapping crawl.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1986147

</td><td>

Extend branding properties to support the update to the dynamic landing page 'Search My Servicenow' placeholder

</td><td>

 

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

Observe the KB is sent to the LLM.


 Expected behavior: The content of the KB is sent to the LLM.

 Actual behavior: Only the KBB content \(defhi\) is sent to the LLM.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2006426

</td><td>

When a document with an attachment is removed by late binding, the next attachment where the user has access is also removed

</td><td>

When ds\_document\_version parent documents are filtered by an ACL and their children are skipped \(the continue at line 516–518 bypasses the recursive child processing\), the sys\_attachment sparse cursor falls out of sync. It was built assuming every child would be processed in order, but skipped parents leave gaps.

</td><td>

1.  Create 3 KBs with an attachment.
2.  Ensure that the KBs and attachments are relevant to a query \(KB1 is most relevant. KB3 is least relevant but still matches a query\).
3.  Add an ACL to block the second KB but allow the first and third.
4.  Force a late binding KB in ais\_datasource or the 'everything by' property.
5.  Query in a search preview as a user.

 Expected behavior: KB3 should be displayed with an attachment.

 Actual behavior: KB3 is displayed but with no attachment.

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

On the catalog item, it's possible to hide the description using the following in the code source: 'div style=''display: none;'' TEXT TO HIDE &lt;p&gt;.' When attempting to do the same in the order guide, it's not working properly in the chatbot, and both texts are visible. This issue occurs only on the chatbot preview of the order guide, and not when consulting it directly from portal.

</td><td>

1.  Open an instance.
2.  Navigate to /esc.
3.  Enter the utterance, 'Standard Laptop'.

Notice that the preview does not show the utterance since the description of the catalog item has the following: '&lt;div style="display: none;"&gt; TEXT TO HIDE &lt;p&gt;'.

4.  Enter the utterance "Request Developer Project Equipment".

The preview does show the utterance even though the description of the catalog item has the &lt;div style="display: none;"&gt; TEXT TO HIDE &lt;p&gt;.


</td></tr><tr><td>

AI Search UX

 PRB1998976

</td><td>

Search event records don't indicate the search mode \(keyword, hybrid, or semantic\)

</td><td>

When a search is executed in an AIS-enabled portal with Hybrid Search enabled on the corresponding search application, the resulting sys\_search\_event and sys\_search\_signal\_event records don't capture the search mode \(keyword, hybrid, or semantic\) that was used to execute the query. This makes it impossible to distinguish query types in search analytics and signal data.

</td><td>

1.  Turn on Hybrid Search on a Search Auto-complete Configuration \(SAC\).
2.  Navigate to a Dynamic Window-enabled portal that uses the configured SAC.
3.  Perform a search in the portal.
4.  Open the corresponding sys\_search\_event and sys\_search\_signal\_event records generated by the query.

 Observe that neither record contains any field or indicator specifying the search mode used \(keyword, hybrid, or semantic\).

</td></tr><tr><td>

AI Search UX

 PRB2000828

</td><td>

The 'Async Genius Result Processor' Asynchronous Message Bus \(AMB\) channel subscription is delayed by session sync contention

</td><td>

The 'Async Genius Result Processor' sys\_amb\_processor record doesn't have dedicated\_session\_sync enabled. Without this flag, AMB subscribe transactions for this channel share the same global per-session lock as HTTP transactions. When long-running HTTP transactions are active in the same user session, subscribing to the Genius Result AMB channel is blocked waiting for the session lock, causing delayed delivery of Now Assist results.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2011697

</td><td>

RAG popular search suggestion reader doesn't consider sys\_rag\_search \_suggestion.active

</td><td>

The sys\_rag\_ search\_suggestion records with active=false are still returned.

</td><td>

1.  Generate sys\_rag\_ search\_suggestion entries.
2.  Query the Suggestion API.

 Observe that the sys\_rag\_ search\_suggestion records with active=false are still returned.

</td></tr><tr><td>

AI Search UX

 PRB2012802

</td><td>

Indexed source types shouldn't be hardcoded in the API

</td><td>

The AISIndexSourceAPI.fetchIndexingState\(\) method only returns for internal type indexed sources. It should include all indexed sources.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2014138

</td><td>

$sp-search- result-title-highlight --background-color in sp-variables.scss

</td><td>

There is no default assigned for variable '$sp-search- result-title-highlight --background-color'.

</td><td>

1.  Log in to Portal with AI Search enabled.
2.  Search for 'laptop'.
3.  Navigate to the AI Search page.

 Notice that the variable '--search-result -title-highlight --background-color: $sp-search-result- title-highlight --background-color;' isn't resolved.

</td></tr><tr><td>

AI Search UX

 PRB2016024

</td><td>

Synthesized responses on a mobile sized screen don't display 'Show full answer' after truncation in Zurich on Safari

</td><td>

The answer is truncated without the option to expand: 'Show full answer'.

</td><td>

1.  Find a Zurich instance with multi-content synthesized Genius Results \(GR\) working in Portal that can work on the Safari mobile browser.
2.  Search for a term that would yield a synthesized GR.

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

 Observe that facets aren't returned as a result of above line failing to fetch hasMatch.

</td></tr><tr><td>

AI Search UX

 PRB2024551

</td><td>

New/Different experience in the search when AI Search is turned on in the portal level

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Impersonate as system admin.
3.  Navigate to /csm portal.
4.  In search bar, search 'Controllers and applications'.

 Observe that there's no follow up and articles displayed are shown previously in the enhanced chat.

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

AI Service - Glide Interfaces

 PRB1970597

 [KB2977679](https://hi.service-now.com/kb_view.do?sysparm_article=KB2977679)

</td><td>

Machine Learning \(ML\) trainings fail with a 401 error due to ACL errors, unless the 'Predictive Intelligence' plugin is explicitly repaired

</td><td>

When the ML trainer attempts to fetch data from the instance, it receives an HTTP 401 unauthorized error for gml\_service, which is resolved after explicitly repairing the 'Predictive Intelligence' plugin.

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

 PRB1998034

</td><td>

Single score data visualization ignores the 'Apply time series to result' indicator configuration

</td><td>

Starting in the Zurich release, the Single Score Data Visualization with AVG \(or SUM\) aggregation does not respect the 'Apply time series to result' configuration on formula indicators. When this option is unchecked, the Single Score continues to display the time-series-based result instead of updating accordingly.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2003111

</td><td>

Pivot table using multiple data sources shows 'No data' on the widget when one of the data sources returns no data

</td><td>

Even though data is available, the chart shows 'No data available'.

</td><td>

1.  Provision an instance with the com.snc.itsm \_pa.demo plugin installed to have more test data.
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

 Notice that data for March is now visible.

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

 Observe that the created Geomap widget doesn't render all the data points and shows an error: 'Some of the data you selected cannot be visualized on the map due to latitude/longitude mapping errors'.

</td></tr><tr><td>

Analytics Data API

 PRB2020263

</td><td>

Remove PowerMock to fix broken tests

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Analytics Export API

 PRB1977076

</td><td>

There's a blank page when exporting Boxplot data visualizations

</td><td>

Boxplot emits 2 SN\_PAR\_VISUALIZATION\#RENDERED events, but it sends expectedRenderEvents = 1 in the export payload. That's why this fails intermittently when the chart isn't loaded completely.

</td><td>

1.  Navigate to Boxplot.
2.  Select **Export**.
3.  Pick JPEG as the file type.
4.  Download the JPEG file.

 Observe that a blank page is displayed. The same issue occurs with an embedded PNG and with PowerPoint files in a dashboard.

</td></tr><tr><td>

Analytics Export API

 PRB1996615

</td><td>

Scheduled export with omit if no records enabled, no attaching the exported file in Email log

</td><td>

 

</td><td>

1.  Create any visualization with some data.
2.  Schedule that visualization and while scheduling, turn on 'omit' if no records toggle.
3.  Select the export type of **other** &gt; **ppt** &gt; **embed png**.
4.  Save the scheduled export.
5.  Select **Send Now**.
6.  Navigate to email logs to find the email record of the scheduled export.
7.  Open that email record.
8.  Select the 'Email attachment' tab at the bottom.

 Expected behavior: The exported visualization should be attached there.

 Actual behavior: Nothing is attached.

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

Show the total row count in the 'Analytics' list

</td><td>

The list-simple property 'hideTitleRowCount' should migrate to showRecordCount in the new 'Analytics' list.

</td><td>

1.  In Yokohama, create a list-simple visualization.
2.  Change the **Hide total number of records** toggle in the configuration.
3.  Save the visualization.
4.  Upgrade the instance.
5.  Open the same visualization.

 Observe that it doesn't migrate to the new list visualization and have the corresponding property set for showing count.

</td></tr><tr><td>

Analytics Export API

 PRB2023200

</td><td>

Hide the export option when its disabled or the roles list is empty

</td><td>

The system provides export on demand functionality at dashboard and data visualization level \(server-side\) for the Next Experience. There is a need to control the availability of the export option based on system properties and user roles.

</td><td>

1.  As the system administrator, configure a system property to enable or disable the export feature.
2.  Make sure the export feature is enabled.
3.  Configure a second system property with a comma-separated list of roles that are allowed to use the export feature when it is enabled.

 Observe the system checks if the user's role is included in the configured list of roles \(if the list is not empty\). If the second system property \(roles list\) is empty, the export feature is available to all users when enabled. If the second system property \(roles list\) is populated, only users with roles in the list can access the export feature.

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

Application Rationalization

 PRB1990668

</td><td>

Malformed sn-lucid-chart-intg.properties

</td><td>

There's a missing comma in a dependency list.

</td><td>

1.  Open oob-apm-apps/ src/main/oob\_apps /sn-lucid-chart-intg.properties.
2.  Locate the 2.4.1-dependencies= block.
3.  Find the line containing sn\_lucdchart\_spoke:1.1.1\\.

 Confirm that there's no comma before the backslash continuation.

</td></tr><tr><td>

Application Rationalization

 PRB1993865

</td><td>

Base instance business rule fails to exclude the current record during duplicate name validation due to incorrect property reference

</td><td>

The business rule on the cmdb\_ci\_business\_app table incorrectly blocks updates when changing the case of a Business Application name \(e.g., 'abc' to 'ABC'\). This happens because it uses current.sysId instead of current.sys\_id, resulting in an undefined sys\_id comparison.

</td><td>

1.  Create a Business Application \(cmdb\_ci\_business\_app\) with the name 'abc'.
2.  Edit the same Business Application and change the name to 'ABC' \(only change the case\).
3.  Attempt to save the record.

 Expected behavior: The save is allowed because it's the same record, just with a different case.

 Actual behavior: The save is blocked with the error: 'A Business Application exists with the same name. Please verify.'

</td></tr><tr><td>

Appointment Booking

 PRB2026901

</td><td>

Appointment Booking's scripted mode doesn't consider the territory resource demand feature

</td><td>

 

</td><td>

1.  Create a 'Records in Territory Resource Demand' table.
2.  Turn on this feature in the configuration.

 Appointment Booking in scripted mode should consider agent availability based on the territory demand channel association.

</td></tr><tr><td>

Approvals

 PRB2012477

</td><td>

Glide changes to Intelligent Approvals

</td><td>

This is a product update.

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

 Expected Result: The relevant filter is automatically applied after navigation.

 Actual Result: On navigation, the filter isn't applied.

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

 Observe that the kba\_session\_context value for the third question is logged in this format: '\{q1\_keyword= q1\_user\_input, q2\_keyword= q2\_user\_input\}'. It should be logged in a standard json format.

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

 PRB1969882

 [KB2718536](https://hi.service-now.com/kb_view.do?sysparm_article=KB2718536)

</td><td>

Log in screen performance issues on iOS 26.2 RC and in Zurich instances

</td><td>

After upgrading to iOS 26.2, users are unable to log in to any instance using the Now Mobile app. The login page is extremely slow or unresponsive, and it can fail to load or accept credentials. The issue affects multiple users and device models. It's reproducible across different instances, and it also impacts the Agent app.

</td><td>

1.  On iOS, navigate to the Now Mobile app.
2.  Connect to a Zurich or later family release instance.

 Observe that the screen loads slowly and is non-responsive.

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

 PRB2015508

</td><td>

Workspace load time performance fixes in Automated Test Framework \(ATF\) cache

</td><td>

 

</td><td>

1.  Navigate to an Australia instance.
2.  Create a test to open **SOW Workspace** &gt; **Incident Form** &gt; **UI action visibility** &gt; **Save**.
3.  Run the test.

 Observe the test takes up to 40 seconds to complete successfully. Sometimes intent timeout errors are seen.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2022891

</td><td>

MVP - UI test script \(Testing Library\) test step in ATF for UI testing

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Cache

 PRB1947736

</td><td>

DBVideoProvider shouldn't use a synchronized LRU

</td><td>

This lock displays contended in most p90+ UI transactions.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2015420

</td><td>

RCAs for Now Assist Agents for requestor

</td><td>

 

</td><td>

1.  Open NAVA.
2.  Give the utterance: 'I need to verify the status of my tickets' to invoke 'Request Status AI Agent'.

 See an error and see the requested RCAs.

</td></tr><tr><td>

Change Management

 PRB1994240

</td><td>

Translation issues in the Conflict Checker Progress modal window

</td><td>

Translation issues were observed after upgrading from Yokohama to Zurich. The 'conflict\_detection' header appears to be missing the message completely when it previously read 'Conflict Detection'. The message 'The conflict check is complete' is translated into Finnish, even when the user's language is in English. This issue also occurs when the instance language is set to French, and the label is translated in English.

</td><td>

1.  Open a Zurich instance.
2.  Ensure that the instance is set to the English language.
3.  Open a change record.
4.  Select the **Check Conflicts** button in the 'Conflicts' tab.

 Notice that the progress bar title displays as 'conflict\_detection' and the value is shown rather than the label, 'The conflict check is complete'. The label is translated in Finnish even though the user's instance language is set to English.

</td></tr><tr><td>

Change Management

 PRB2011052

</td><td>

Users are unable to add a change model state attribute for a major model from a scoped app

</td><td>

Application access settings don't allow writes to the sttrm\_state\_attribute table. The ACL is restricting to set the **State** field on sttrm\_state\_attribute record.

</td><td>

1.  Create a change model with a set of states from a scoped app.
2.  Try to add an existing change model attribute to one of the states.

 Observe that the record isn't generated properly.

</td></tr><tr><td>

Change Management

 PRB2011527

</td><td>

Applying a template can lead to URL size issues and invalid encoding

</td><td>

This appears to be potentially two issues. The template being added to the URL to apply it on the new form causes URL size and encoding issues. Observe that there's an error message in the developer console. A 500 error is returned from the instance: 'URLDecoder: Illegal hex characters in escape \(%\) pattern - Error at index 0 in: \|",%\\'''.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2021436

</td><td>

Instances should not get license restriction ACLs

</td><td>

This issue was observed in Australia. Licensing controls are enforced when there are entries in subscription\_entitlement.

</td><td>

Log in to any Australia non-prod instance.

 Notice that the licensing controls are enforced when there are entries in subscription\_entitlement, even if the instance is open.

</td></tr><tr><td>

Change Management

 PRB2024681

</td><td>

Add a missing entry for an advanced/change admin experience for Auto Install Framework

</td><td>

Auto Install Framework was shipped to Australia users. The missing entry record related to advanced admin experience should be added so that the framework installs this experience as well for net-new users.

</td><td>

 

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

Column Level Encryption

 PRB1978716

</td><td>

Encryption isn't applied correctly for comma separated list values in a Glide record query for IN and NOT\_IN clauses

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Condition Builder in Workspace

 PRB2011310

</td><td>

The **SLA** field is read-only in a related condition when creating a list in Workspace

</td><td>

 

</td><td>

 

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

Customer Service Portal Base

 PRB1966219

</td><td>

Additional comments are duplicated in the Customer Service Management \(CSM\) Portal if the state is 'Awaiting Info'

</td><td>

Duplicate comments are occurring due to two identical network calls being made with the same journalEntry content. This duplication specifically happens when the spUtil.recordWatch method \(part of the client-side script\) triggers these service calls under slower network conditions \(3G speed simulation\).

</td><td>

1.  Impersonate a CSM agent.
2.  Open a case.
3.  Add an additional comment and request information.

The state of the case is set to 'Awaiting Info'.

4.  Impersonate a user account \(external\).
5.  Open the case.
6.  Add a comment.

Note that the comment appears twice in the case activity log.

7.  Add a second comment \(the state of the case is now open\).

Note that the comment isn't duplicated.


</td></tr><tr><td>

Database Persistence - Data Access

 PRB1919872

</td><td>

There's duplicate edges in the output of jsFunction\_getEdgeList for custom created graphs and when includeEdgesForTablesOutsideGraph is true

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1930279

</td><td>

Users are able to create a cyclic relation through graph hierarchy

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

When trying to get a specific column instead of the entire record, the error occurs in the response: ''FAILED TRYING TO EXECUTE ON CONNECTION trino\_primary'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1962536

</td><td>

The prefix is missing on some places for the Knowledge Graph UI

</td><td>

 

</td><td>

1.  **All** &gt; **Knowledge Graph Designer**.
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

 [KB2747470](https://hi.service-now.com/kb_view.do?sysparm_article=KB2747470)

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

Database Persistence - Data Access

 PRB1986459

</td><td>

The 'Add OR Clause' with multiple filters is not working as expected

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1998050

</td><td>

Glide-side changes for label population in picker tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2027220

</td><td>

ColumnName.resurrect\(\) re-shortens long names, corrupting external store column names on deserialization

</td><td>

ColumnName.resurrect\(\) reconstructs a ColumnName from its serialized form using new ColumnName\(name\), which re-applies the preFujiShortColumnName\(\) 30-character shortening algorithm. However, serialize\(\) writes the already-resolved fName directly. For external-store columns \(Snowflake, BigQuery, Trino\) whose physical names exceed 30 characters, the name is corrupted on deserialization — the resurrected ColumnName points to a shortened name that doesn't exist in the external store.

</td><td>

1.  Create a ColumnName with shortening turned off: new ColumnName \("external\_column\_ with\_a\_very\_ long\_name", false\) \(37 chars, exceeds MAX\_LENGTH of 30\).
2.  Serialize via ColumnName.serialize\(writer, cn\).
3.  Deserialize via ColumnName.resurrect\(reader\).

 Observe the resurrected name is the 30 character shortened form, not the original 37 character name — a round-trip corruption.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1999855

</td><td>

The 'One Time Archive Max Length Sync' job widens the max length of reference fields incorrectly

</td><td>

 

</td><td>

1.  Create an archive table with retain reference enabled:new GlideArchiveTable\(\) .create \(&lt;primaryTableName&gt;, true\);.

This operation creates an archive rule and corresponding reference fields on the archive table.

2.  Run the one-time job.
3.  Since no explicit archive rule exists on the table at runtime, verify that the one-time job recalculates the maximum length of reference fields based on the reference display element length, resulting in those fields being widened.

 Expected behavior: The one-time job should not widen reference fields when they are already reference types created with retainReference = true. In this scenario, the reference fields are already correctly defined, and recalculating their length based on display values is unnecessary and incorrect.

 Actual behavior: The one-time job widens the max length of reference fields, even though the fields are already of reference type and were created with retainReference = true.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2004780

</td><td>

Use batch deletion for the 'Columnar' archive table during bulk archive restore

</td><td>

Deleting records one by one is not efficient for a 'Columnar' archive table because it requires scanning the same bucket multiple times. Batch deletion would only scan each bucket once.

</td><td>

1.  Migrate some archive tables to columnar.
2.  Attempt to run archive bulk restore.

 Expected behavior: Archive restore should be performed.

 Actual behavior: Archive restore isn't performed.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2005218

</td><td>

Archive-Tier2-Bulk-Restore handle has silent exceptions when missing an archive log or bucket

</td><td>

If there's no archive log for the relevant cidx\_record during restoration to the ar\_\* table, the process fails silently and also moves the cidx\_\* record to the cidx\_\*\_backup table. If the sys\_s3\_bucket value is missing in the cidx\_\* record, which shouldn't occur, it loses the key value needed to restore the record. In this case, the chunk is processed, but the cidx\_\* record remains unchanged, making it appear as though the record was not processed. sys\_s3\_bucket value is missing for any cidx\_\* records which are still pending to be offloaded. The pending cudx\_\* records needs to be ignored.

</td><td>

1.  Offload a bunch of records to tier2 \(using the 'Offload' job\).
2.  For a couple of records, remove the value from the **sys\_s3\_bucket** field.
3.  For another couple records, find its sys\_archvie\_log record and delete it.
4.  Turn on the tier2 bulk restore.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2015142

</td><td>

There's a slow query during archiving records to the 'columnar archive' table

</td><td>

The archived incident has a reference field whose referenced record has already been archived; it no longer exists in the live incident table, only in ar\_incident. When copyFields tries to get the display value of that reference, live table lookup fails \(record already moved to archive\), GlideElementReference falls back to ArchiveResolver, and ArchiveResolver confirms it's in ar\_incident via sys\_archive\_log, then queries ar\_incident to fetch the display value.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2016927

</td><td>

Avoid reparenting the 'Columnar' archive table with a documentID reference after restoring a record

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2022327

</td><td>

Data Management Console fails to load live archive object storage data

</td><td>

Data Management \(DM\) Console fails to load live archive object storage data on instances using the new Live Archive / Tier 2 archive feature \(com.glide.db.columnar.archive\). This is because S3StorageInfoEligibilityChecker.isEligible\(\) calls ArchiveEntitlementAPI. passedEntitlementCheck\(\), which only validates the legacy plugin com.snc.tier2\_data\_offload via isBaseTermsAndConditionsAccepted\(\). Users on the new columnar archive plugin fail eligibility and the S3StorageInfo daily job aborts.

</td><td>

1.  Provision an instance with the Live Archive feature.
2.  Turn on the Live Archive feature.
3.  Offload a lot of data.
4.  Browse to the 'DM Console' page.
5.  Look for the 'Object Storage' widget.
6.  Verify that the data isn't visible.

 Expected behavior: The S3StorageInfo job should run for eligible users.

 Actual behavior: The S3StorageInfo job isn't running for eligible users.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1974343

</td><td>

A query hint isn't including the change number and is causing the hint to be ignored

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB2002323

</td><td>

When dry run mode is false, a successful external transfer causes TM to lock itself in a failed state and prevents any automatic failover during that window

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1923336

</td><td>

The isTableExcluded API should exclude text search tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1932536

</td><td>

An error should show 'Display Name' instead of the table name

</td><td>

 

</td><td>

1.  Create a graph.
2.  Add nodes - 'User' and 'Location'.
3.  Save the graph.

 Observe an error: 'No properties found for node sys\_user'.

</td></tr><tr><td>

Database Persistence - Graph

 PRB1938573

</td><td>

A 'WHERE' clause appends all query node conditions with an 'AND' operator, even when there are 'OPTIONAL MATCH 'statements

</td><td>

When trying to a build cypher query for the following use case, 'Identify all CI's which are connected to Database catalog or Application', in the final built cypher query the 'WHERE' clause is using all 'AND' conditions to append all node filters to the query. When using 'OPTIONAL MATCH' statements, an 'OR' logic is expected.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1944327

</td><td>

Global graph should be the default and all other graphs should be non-default when the instance is upgraded from Yokohama to Zurich

</td><td>

Default graphs and global graphs are all set to non-default.

</td><td>

1.  Create two default graphs on a Yokohama instance.
2.  Upgrade the instance to Zurich.
3.  Check the graphs on sys\_meta\_graph.

 Expected behavior: Global graph should have default = true and the other two graphs that were created in step one should have default = false.

 Actual behavior: Both of the created default graphs and the global graph are default = false.

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

5.  Remove one of the conditions \(e.g., 'Location Contains 'via''\).
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

There's an error: 'com.glide.db. DBGraphApiException: Error executing cypher: FAILED TRYING TO EXECUTE ON CONNECTION...Syntax Error or Access Rule Violation detected by database \(ERROR: function duration\_between\(date, date\) does not exist Hint: No function matches the given name and argument types. You might need to add explicit type casts. Position: 294\)'.

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

Weeks, milliseconds, and microseconds aren't supported in the 'Duration' map

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

 Expected behavior: Observe with the data, there should be two L1 relationships and three L2 relationships with edge shown as '\(empty\)'.

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

GlideRecord. setCategory\(\) is used in a way that prevents routing to read-replica databases

</td><td>

The query is categorized as 'graphqueryexecutor' instead of 'cmdb\_queries', and therefore doesn't get routed to the read replica because the category isn't a second database category.

</td><td>

1.  Ensure that the instance is set up with a read replica database.
2.  Ensure that the CMDB Queries \(or all Secondary Database Categories\) are enabled and are mapped to the read replica.
3.  Execute a KG query from the CMDB Query Builder app.

 Expected behavior: The query is categorized as 'cmdb\_queries' and is routed to the read replica.

 Actual behavior: The query is categorized as 'graphqueryexecutor', and since that category isn't a secondary database category, is not routed to the read replica.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1975615

</td><td>

GlideAggregate. getDisplayValue issues a separate query per each returned record for GlideAggregate

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Views

 PRB2004420

</td><td>

Data fabric \(DF\) tables in DBViews uses an old connection even after doing a change connection/remap flow on DF tables

</td><td>

 

</td><td>

1.  Create two DF tables on any two tables from an existing established connection on Snowflake Zero Copy Connector.
2.  Create DBView on these two tables, joining them on any field.
3.  Navigate back to the DF tables and change connection on that existing DFtable that was initially created.
4.  Query DBView.

 Observe that the underlying DF tables in DBView still looks for an old connection.

</td></tr><tr><td>

Data Management Console

 PRB1974031

</td><td>

A repeated query with the hash -423529530 comes up when running stats gatherer

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB1976295

</td><td>

The confirmation checkbox is missing on the 'Summary' page when scheduling a rule

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB1979259

</td><td>

The data on Data Management Console \(DMC\) is inconsistent when the 'Stats gatherer' job runs

</td><td>

The data on DMC is inconsistent when the 'Stats gatherer' job runs because the latest available data is chosen, even when the data isn't completely generated.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB1980674

</td><td>

There's a potential of orphan sys\_peripheral \_table\_stats records for a duration of 1 year with the existing Data Management Console \(DMC\) table's table cleaners

</td><td>

Revisiting the table cleaners for sys\_peripheral \_table\_stats and sys\_physical \_table\_stats in order to accommodate a new data model. Cascade delete should be turned on so that orphan records are cleaned up regularly.

</td><td>

1.  Check the 4 table cleaners for sys\_physical\_table\_stats.
2.  Observe that cascade delete isn't enabled.

 Expected behavior: Cascade delete should be enabled and in the sys\_dictionary. The reference column's reference\_cascade\_rule should be 'delete'.

 Actual behavior: Cascade delete isn't enabled.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2001965

</td><td>

'Run once' Data Privacy jobs take a long time to complete on large tables

</td><td>

As part of Zurich, Data Privacy jobs were enhanced to support incremental and recurring anonymization. As part of this, 'sys\_updated\_on &lt; jobStartTime' was added to the query condition while creating segments and querying a batch of records for processing. Generally, sys\_updated\_on column isn't indexed. As a result, the jobs take lot of time to create segments, which require querying boundary records involving filtering on sys\_updated\_on and ordering by sys\_id. While the sys\_updated\_on filter condition is necessary to support incremental, this dependency can be removed on 'Run once' jobs, where all records in a table are expected to be anonymized.

</td><td>

1.  Provision an instance with the Data Privacy plugin installed on a large clone.
2.  Set up a privacy configuration on a table with large number of records.
3.  Configure and run a 'Run once' dp\_job.

 Expected behavior: Segment creations \(dp\_work\_item\) should happen within few a minutes.

 Actual behavior: It takes hours to create segments \(dp\_work\_item\).

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2002556

</td><td>

Data Privacy Clone \(federated\) jobs can't handle pause/resume scenarios

</td><td>

During a clone job execution, if the node on which the clone job is executing is restarted, scheduler reschedules the job on a different node. When the job is restarted on a different node, it fails due to inability to deserialize and restore the state items \(that dictate where the job should resume from\).

</td><td>

1.  Provision an instance with Data Privacy installed.
2.  Create a data class with classified fields of table - cmn\_location.
3.  Create a clone Data Privacy policy.
4.  Schedule the clone policy by creating a clone.
5.  Notice a clone job is created in the dp\_federated\_job table and the job is running.

 Expected behavior: The job should be completed.

 Actual behavior: The job errored out with 'Error creating job handler for type null from serialized state : \[Interfaces can't be instantiated! Register an InstanceCreator or a TypeAdapter for this type. Interface name: com.glide.data\_privacy.jobs.stateitem.StateItem\]'.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2006453

</td><td>

The Data Privacy job's policy child table filtering isn't working as expected if the parent table is selected as a child table filter

</td><td>

If a task table is selected as child table for any of its dictionary selected tasks as the child table, then it's expected to anonymize records that belong to sys\_class\_name = task, and the rest of the records, the incident or problem, are expected not to be anonymized. It's anonymizing the entire task table.

</td><td>

1.  Create a Data Privacy policy using the task table, short description, description columns.
2.  Select the child table filter for any of the columns.
3.  Add a task.
4.  Save and publish the policy.
5.  Schedule a Data Privacy job.

 After the job completion, notice that the entire task table is anonymized, but it's expected to only anonymize the task records, not any others.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2017470

</td><td>

Job conditions aren't applied by additional jobs during parallel execution

</td><td>

This is caused because of dp\_additional\_job not applying the condition setup for the job. Since, the conditions in dp\_job\_condition is tied to parent job, querying from additional job won't find them unless it uses the parent job ID to query.

</td><td>

1.  Create a privacy policy for a task table.
2.  Set up sys\_properties to com.glide.data\_ privacy.max\_ parallel\_workers=2.
3.  Configure a job with conditions.
4.  Ensure sufficient data to create at least 2 segments.
5.  Run the job.

 Expected behavior: Only records matching the setup condition should be anonymized.

 Actual behavior: Record not matching the condition are also anonymized.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2017592

</td><td>

A minimum segment size of 100K characters restricts parallelization and lacks work item table cleanup

</td><td>

The current minimum segment size is hardcoded at 100K characters, which artificially caps the number of segments that can be generated for a given dataset. As a result, the number of worker threads that can be utilized for parallel processing is also restricted — even when additional infrastructure capacity \(CPU, memory, available workers\) is available to be consumed. If the minimum segment size is reduced to improve parallelization, the number of work items inserted into dp\_workitem grows significantly, accelerating the rate at which this table accumulates rows. Without a corresponding cleanup mechanism, this will lead to unbounded table growth, increased storage consumption, and potential degradation of query performance over time.

</td><td>

1.  Create/update the sys\_property 'com.glide. data\_privacy. max\_records\_ per\_work\_item' to 10000
2.  Create a data class Data Privacy job on a table containing at least 20K records.
3.  Run the job.
4.  Examine dp\_work\_items.

 Expected behavior: There should be at least 2 work items.

 Actual behavior: There's 1 work item.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2017660

</td><td>

Users aren't able to switch to a GPU-based Named Entity Recognition \(NER\) service from CPU-based services for privacy jobs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Product Backend Services

 PRB2017091

</td><td>

Users are unable to remove a source table from Data Interface

</td><td>

syncDataInterfaceM2MTable DAO method wasn't removing M2M rows for sources absent from the new list. Delete path lacked compensating-action registration, leaving stale rows on partial failure.

</td><td>

1.  Navigate to Data Workbench.
2.  Create a Data Interface.
3.  Try to add a new source to the interface.

 Observe that the user isn't able to add/remove a source from the interface.

</td></tr><tr><td>

Data Product Backend Services

 PRB2017092

</td><td>

Users are unable to add a new source to Data Interface

</td><td>

The syncDataInterfaceM2MTable DAO method isn't inserting rows for sources present in the new list but that are absent from the database. Insert path lacked compensating-action registration, leaving the interface with no implementors on partial failure.

</td><td>

1.  Navigate to Data Workbench.
2.  Create a Data Interface.
3.  Try to add a new source to the interface.

 Observe that the user isn't able to add a new source to the interface.

</td></tr><tr><td>

Data Product Backend Services

 PRB2017094

</td><td>

Users are unable to roll back if the creation or editing of a data interface fails in the middle

</td><td>

DataProductDAO edit methods had no rollback mechanism. A failure mid-transaction left the interface partially mutated with no way to restore prior state.

</td><td>

1.  Navigate to Data Workbench.
2.  Create a Data Interface.

 Observe that the data interface creation failed in the process, a few artifacts were created, and a few are missing.

</td></tr><tr><td>

Data Product Backend Services

 PRB2017095

</td><td>

Once an interface is created, the metadata JSON for existing interface tables is missing

</td><td>

DataProductDAO didn't call TableManager.invalidateTable for existing source tables after interface creation. Users received stale cached metadata JSON rather than the newly registered interface state.

</td><td>

1.  Navigate to Data Workbench.
2.  Create a Data Interface
3.  Add a new source to the interface.

 Observe that the metadata is missing, causing the UI to break.

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

Data Snapshots

 PRB2018876

</td><td>

Turn on automatic installation of the plugin com.snc.pa.mlb on eligible instances

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Developer Sandboxes

 PRB1995018

</td><td>

NowMQ messages can be claimed by an unexpected recipient

</td><td>

If the user sets the App Operation Queue Health Monitor job to disabled, it should prevent the sandbox from claiming any application operation queue messages in sys\_nowmq\_message. On an instance without sandboxes, any messages that were left unclaimed or any newly added messages should still be claimable when the job is re-enabled.

</td><td>

1.  Make sure one controller and one sandbox are running.
2.  On the sandbox, set the App Operation Queue Health Monitor job to disabled.
3.  Enqueue an operation on the sandbox by initiating an app install from app manager or via /sn\_cicd/update\_set/commit.
4.  Navigate to sys\_nowmq\_message.

 Observe that the corresponding message from step 3 is unexpectedly gone. It should still be present but unclaimed as a result of step 2.

</td></tr><tr><td>

Developer Sandboxes

 PRB2011753

</td><td>

Sys\_flow\_trigger\_plan\_chunk is currently shared and causing updated flows to error out

</td><td>

If you update the base flow, the sandbox flow errors out with 'Compiled flow not found for snapshotId'.

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
5.  Activate the flow
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

DirectSQL

 PRB2000506

</td><td>

A correlated sub query loses outer table references

</td><td>

The correlated condition is translated incorrectly, resulting in incorrect results.

</td><td>

Run the following query: SELECT number, \(SELECT COUNT\(\*\) FROM incident AS x WHERE x.priority &lt; incident.priority\) AS lower\_pri\_count FROM incident ORDER BY number.

 Expected behavior: The query returns each incident with a count of how many other incidents have a strictly lower priority value. Incidents with priority &gt; 1 should have a non-zero count.

 Actual behavior: Every row returns lower\_pri\_count = 0, because the correlated condition is translated as x.priority &lt; x.priority \(always false\).

</td></tr><tr><td>

DirectSQL

 PRB2014682

</td><td>

DirectSQL extract epoch support is broken

</td><td>

Users can't extract epoch and must use unix\_timestamp instead. Also, the cypher-related code may be breaking the postgres implementation.

</td><td>

 

</td></tr><tr><td>

DirectSQL

 PRB2016811

</td><td>

Disallow queries that use an inaccessible offrow array in non-select items

</td><td>

For example, select \* from sys\_user where roles is not null. If users don't have access to sys\_userroles for the roles offrow array, then this query should error out indicating that is the case. Currently, null is substituted into the 'where' clause instead, which is confusing.

</td><td>

 

</td></tr><tr><td>

DirectSQL

 PRB2019852

</td><td>

SELECT \* must exclude columns that don't exist in the database

</td><td>

Select \* from a table that has a function field, like cmdb\_data\_management\_policy, won't work because it's trying to find the function fields on the database. A filter should be added to exclude these fields.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1986211

</td><td>

Discovery.complete and discovery.canceled are triggered incorrectly

</td><td>

Discovery may trigger both discovery.complete and discovery.canceled events for the same status, and it may trigger discovery.canceled twice.

</td><td>

1.  Create or pick a cloud-resource Discovery schedule configured to use a specific MID server \(midSelMethod = 'specific\_mid'\).
2.  Ensure that the MID server is in a state where validateMIDCondition\(\) returns false \(typically because the MID is down / not validated\).
3.  Run the schedule \(or trigger it via the Discover Now action\).

 Observe that discovery.canceled fires twice for the same status record. The StartDiscovery error log for 'Discovery canceled on previously started schedule ... due to mid not available' appears twice. Instead, there should be a single discovery.canceled event and a single error log entry per cancelled run.

</td></tr><tr><td>

Discovery

 PRB2014076

</td><td>

Update Discovery references to the new error framework from a scoped app to zboot

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB2016944

</td><td>

Classifier probes aren't firing if the 'First checked' probe has already been fired

</td><td>

Discovery should fire further probes, but instead completes prematurely.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB2018937

</td><td>

Local naively checks for empty text rather than 'blank' when classifying PDF pages for DocReader

</td><td>

The PDF page is classified as 'digital' instead of 'scanned' because it checks for empty text instead of a blank PDF page.

</td><td>

Call DocReader Local with a scanned PDF containing blank text, for example, '"\\n\\n\\n"'.

 Notice that the page is classified as 'digital' rather than 'scanned'.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB2029867

</td><td>

Users can configure more than 50 fields per use case, which does not match the product and pricing based limitations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Dynamic Scheduling

 PRB2021720

</td><td>

Capacity console isn't loading after changing the default date format

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Change the default date format from sys properties.
3.  Create a capacity assignment for any territory.
4.  Try to load the capacity console.

 Expected behavior: Events display for the territory.

 Actual behavior: No events display as demand metrics data aren't created.

</td></tr><tr><td>

Dynamic Scheduling

 PRB2025038

</td><td>

Dynamic Scheduling isn't considering recurrence if more then 1 record for same resource is present in the 'Territory resource demand' table

</td><td>

For example, if 2 records for the same date range with da ifferent recurrence are created for same territory and demand channel, such as: May 1st to May 30th - Monday Recurrence and May 1st to May 30th - Tuesday Recurrence, then Dynamic scheduling isn't considering the Tuesday recurrence.

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

Email Notifications

 PRB1970107

</td><td>

There's an issue with adding an email template in Zurich

</td><td>

 

</td><td>

1.  If no record exists, create a record for a sys\_email\_template for sn\_customerservicecase.
2.  Navigate to CSM/FSM Configurable Workspace.
3.  Select the 'Lists' icon on the left navigation pane.
4.  Navigate to **Cases** &gt; **All**.
5.  Open case CS0001001.
6.  Stay on the 'Comments' tab in the right-side pane.
7.  From the right navigation, select **Email Templates**.
8.  Apply any template.
9.  Do this repeatedly until an error displays.

</td></tr><tr><td>

Email Notifications

 PRB2003711

</td><td>

There's inconsistent behavior on bringing the /r response template in the email body

</td><td>

 

</td><td>

1.  Create a response template with the channel type as 'email'.
2.  Navigate to Customer Service Management/Field Service Management configurable workspace and impersonate as a frontline agent.
3.  Create a case with 'email' as the channel type.
4.  In the 'Email' section, type '/r'.
5.  Look for the created response template.

 See that the response template isn't displaying.

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

1.  Update the 'glide.email\_ client.configurable \_send\_enabled' value to 'sn\_customerservice\_case'.
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

Employee Relations Case Management

 PRB2009979

</td><td>

Moving an RCA from the Employee Relations scope to the Evidence scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Error Framework

 PRB2014079

</td><td>

Migrate the error framework from a scoped app to Glide universe/zboot

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Error Framework

 PRB2014080

</td><td>

Log analysis and error refinement

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Error Framework

 PRB2014081

</td><td>

Error framework backlog for UI Builder unit tests and QoL

</td><td>

This is a product update.

</td><td>

 

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

 PRB1999707

</td><td>

An app node crash occurs due to OutOfMemory \(OOM\), and GroupingDebugLogger accumulaties log messages even if logging is disabled

</td><td>

After stimulating alerts for Metric rule/Event rule and checking the tables for node restarts and active transactions, the queue in the sys\_trigger table is huge.

</td><td>

1.  Install the following in the instance:
    1.  sn-dex-4.0.0-SNAPSHOT
    2.  agent-client-collector-framework-6.0.1
    3.  com.snc.samp
    4.  com.sn\_sam\_saas\_int.
2.  Load 400k agents with E2E data simulation using SIM Version: 3.2.45.
3.  Simulate alerts for Metric rule/Event rule at 300k-600k per 5 minute rate, so that it runs at 1-2k per second.
4.  Check the node restarts from the v\_cluster\_nodes table.
5.  Check the active transactions from the v\_cluster\_transaction table.

Notice that there are slow 'Event Management – process events' jobs.

6.  Check queue in the sys\_trigger table.

 Notice that there is a huge queue found in the sys\_trigger table.

</td></tr><tr><td>

Experimentation Platform

 PRB2027972

</td><td>

Feature flagging under the feature preview program

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Explicit Roles

 PRB2011506

</td><td>

The NullPointerException in ExplicitRoleCollisions .handleSysUserGrmember invalidates ATF rollback context during CreateUserStepRunner execution

</td><td>

During the scheduled nightly ATF test execution, a null pointer exception occurs in the explicit roles collision check logic, which propagates up and invalidates the ATF rollback context. This prevents automatic rollback of test-created records \(e.g. Incidents, Users, Business Services\), leaving orphaned data in the environment.

</td><td>

1.  Activate the explicit roles plugin.
2.  Create a test user.
3.  Assign the user the snc\_internal role only.
4.  Create a group with any one role.
5.  Add the test user to the created group.

 Expected behavior: There is no null pointer exception in the node log.

 Actual behavior: There is the following null pointer exception in the node log: 'Error: java.lang.NullPointerException: Cannot invoke 'com.glide.explicit\_roles. MutuallyExclusive RoleCheckResult $MutualExclusion ResultType .ordinal\(\)' because the return value of 'com.glide.explicit\_roles. MutuallyExclusive RoleCheckResult .getResultType\(\)' is null'.

</td></tr><tr><td>

Flow Engine

 PRB1992819

</td><td>

Impact handling of Scripting Governance disable switch

</td><td>

A disable switch for the Scripting Governance feature is being backported. Any ACL or Java code dependent on the scripting role/group will break if a user flips the disable switch.

</td><td>

1.  Check the ACL and Java code for usage of the snc\_required\_ script\_writer\_ permission role and conditional script writer group.
2.  Ensure that the feature doesn't break when the switch is turned off/on.

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

 PRB1833484

</td><td>

A workspace template with a currency-type field fails to apply

</td><td>

A workspace template fails to apply if it contains a currency-type field. However, a template created from the platform applies in workspace as expected, even with a currency-type field.

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

A Null Pointer Exception is thrown if a table has a GlideElement WikiText type field and queries at startup before extension points are loaded

</td><td>

Adding a GlideElement Wikitext type field to the user table can cause an outage. The page is blank and errors are seen. On a local instance, the instance throws servlet exceptions and doesn't start.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Global Ranking

 PRB2005044

</td><td>

Remove 'defect' and 'enhancement' as options from the 'Demand' type

</td><td>

Removing 'defect' and 'enhancement' as drop down options in the 'Demand' type from the SPM\_agile\_commons plugin repository that are c entries to appear in 'Demand'. Removing these files from the repository prevent these demands from being created.

</td><td>

 

</td></tr><tr><td>

Hardware Asset Management

 PRB2023375

</td><td>

Stockrooms missing a distribution channel yield empty records in the 'list' view

</td><td>

The following exception is thrown when navigating to the 'list' view: 'com.snc.kittyscript.SecurityCallbackException: Scope objects cannot be passed as function arguments'.

</td><td>

1.  Log in to a Zurich instance with HAM 12.1.2 installed.
2.  Navigate to **Hardware Asset Workspace** &gt; **Inventory**.
3.  Select the **View** button on the Stockrooms missing distribution channel.

 See that no records are visible.

</td></tr><tr><td>

HR Service Delivery

 PRB2016516

</td><td>

RCA is generated for 'Populate Manager Reportee Count Using Eligible Users' and 'EmployeeHubOrg ChartReporteeUtilSNC'

</td><td>

The following two RCA's are generated for the new scripts, causing test failures: sys\_script\_include\_ a302f8807873f250 f877079523d275e1 and sysauto\_script\_ 33a5e72453f7 b210f2ebffc 230e5e69d.

</td><td>

 

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB2023467

</td><td>

Incorrect values are shown on the clone summary page

</td><td>

 

</td><td>

 

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

Instance Scan

 PRB2022691

</td><td>

Instance Scan Linter Check fails on sys\_module with an error: 'Rhino error: missing ; before statement'

</td><td>

 

</td><td>

1.  Create an app in ServiceNow IDE.
2.  Create at least one file \(e.g. business rule\) that stores code in a sys\_module application file.
3.  Build and deploy the app.
4.  Create an Instance Scan Linter Check.
5.  Scan the resulting app \(or the individual sys\_module record\) using the linter check.
6.  In the scan result record on the 'Failures' related list.
7.  Validate that one or more errors are logged: 'Rhino error: missing ; before statement'.

</td></tr><tr><td>

Integration Hub

 PRB1870601

</td><td>

A PowerShell step error message is no longer populated

</td><td>

On flow engine V1, the user ran a flow execution and can observe 'Error Code' and 'Error Message' are outputed in the 'Output Data' section when the PowerShell script returns an error. However, if users switch to flow engine V2, the same error code and error message can not be rendered into the 'Output Data' section.

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

Issue Auto Resolution for Virtual Agent

 PRB1657388

 [KB1307989](https://hi.service-now.com/kb_view.do?sysparm_article=KB1307989)

</td><td>

Issue Auto Resolution \(IAR\) for HR isn't able to execute for users who remove HR roles from the 'admin' role due to internal data governance policies

</td><td>

Affects users using IT and HR products on the same instance. Due to the data internal visibility/governance policies, users have removed a number of HR roles \(i.e. 'sn\_hr\_core.admin' role\) from the admin role, resulting in users in the IT business units not having access to the HR side of the platform. Removing the roles from the admin profile prevents the 'system' user from executing the AutoResolution scripts includes. The 'system' user no longer has access to the HR tables of the instance, hence it can't extract the necessary information for auto resolution ML Configuration Language solution, auto resolution context, or write to HR records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1964424

</td><td>

WebServices Mutual Auth connections fail if the instances are in FIPS mode

</td><td>

If an instance is using FIPS mode, REST Web Services connections fail if the authentication type is 'Mutual Auth'. The following error is thrown: org.bouncycastle.tls.TlsFatalAlert: unsupported\_extension\(110\).

</td><td>

1.  Turn on FIPS mode on an instance.
2.  Set up an outbound REST call to a third-party API.
3.  Make sure the authentication type is 'Mutual Auth'.
4.  Set up a protocol profile record to associate to the REST connection.
5.  Apply the API's endpoint .bsfks keystore certificate to the Protocol Profile Keystore record.
6.  Run a test connection to the endpoint.

 See that it fails with an error: 'org.bouncycastle.tls.TlsFatalAlert: unsupported\_extension\(110\)'.

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

Knowledge Graph \(Family\)

 PRB2021133

</td><td>

Knowledge Graph \(KG\) description deactivator triggers long-running queries, causing HLL spikes

</td><td>

Post Version Upgrade Job : KG Description Deactivator triggers Long running queries and causes HLL spike

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1976775

</td><td>

A KB's article title is empty under the 'Event property values' column in the 'Article Title' report

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Navigate to the User Experience Analytics dashboard.
3.  Select **Employee Center** in the menu.
4.  Navigate to **Data Foundation** &gt; **Events section**.
5.  Open the 'View Knowledge Article' event.
6.  Under 'Event properties', navigate to the 'Article Title' and 'Article SysID' widgets.
7.  Observe the '...' empty value on the report chart.
8.  Export the data to Excel.

 Observe the exported report contains an empty field under the first column labeled 'Event property values'.

</td></tr><tr><td>

Knowledge Management

 PRB2009818

</td><td>

The **Recall** button isn't displayed for the author of the article in Service Operations Workspace

</td><td>

The **Recall** button in a workspace is nested behind the **Edit** button, which is intentionally hidden from the author while the article is in review. However, authors are blocked from editing content that is currently under review. The **Recall** button only appears after selecting **Edit**, but since the **Edit** button isn't visible to the author in this state, the **Recall** button is unreachable.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2010029

</td><td>

Knowledge blocks aren't honoring Knowledge Center \(KC\) redirection properties

</td><td>

 

</td><td>

1.  Turn on redirection properties for KC: sn\_km\_center. glide.knowman. redirect.enable.
2.  Navigate to 'Knowledge Blocks' in Navigator in UI16.
3.  Select **Create**.

 Expected behavior: Knowledge blocks should honor KC redirection properties.

 Actual behavior: Creating or editing a from UI16 doesn't redirect to KC.

</td></tr><tr><td>

Knowledge Management

 PRB2010576

</td><td>

kb\_translate page padding and alignment must be revisited

</td><td>

There's no padding at all and the page content and buttons are near to the borders and not what users see in other workspaces. The kb\_translate page should be properly padded as in other workspaces for a consistent experience.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2014935

</td><td>

KB Portal's image dimensions don't match with the Native UI

</td><td>

The image dimensions displayed in the KB Portal don't match with the dimensions configured in the article body within the Native UI, although they should.

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

 PRB1989840

</td><td>

There's unintended creation of temporary list copies when refreshing a default list via address bar

</td><td>

When a user refreshes a default list by selecting the browser address bar and pressing Enter, the system creates a new temporary copy of the list and stores it under 'My Lists' &gt; 'Opened by link'. When the page reloads, that view is opened. This happens without any explicit user action or intent to create or save a new list, and the newly created list is not shared with anyone by default. This behavior creates large volumes of unnecessary list views, leads to user confusion, and pollutes My Lists governance and storage with artifacts.

</td><td>

1.  Open any default list in the workspace.
2.  Select the browser address bar \(don't modify the URL\).
3.  Press **Enter** to reload/refresh the page.

Observe that once the page reloads, it automatically navigates to **My Lists** &gt; **Opened by link**.


 Expected Behavior: Refreshing a default list via the browser address bar doesn't create a list artifact.

 Actual Behavior: A new temporary copy of the default list is automatically created. The list appears in **My Lists** &gt; **Opened by link**, even though the user never requested a copy. The list is not shared with anyone by default.

</td></tr><tr><td>

List Administration

 PRB1999574

</td><td>

The user has no information about who shared a list with them

</td><td>

 

</td><td>

1.  Open Customer Service Management or Field Service Management Configuration Workspace.
2.  Navigate to the 'List' page as an admin user.
3.  Create a few lists in the 'My Lists' tab.
4.  Share one list with another user, like Fred Luddy.
5.  Impersonate Fred Luddy.

Observe the shared list in the 'Shared with me' section inside the 'My List' tab.


 Expected behavior: There's some info or indication on who shared the list.

 Actual behavior: The Fred Luddy user has no information regarding who shared this list.

</td></tr><tr><td>

List Administration

 PRB1999583

</td><td>

The user can't re-order the lists 'Shared with me' lists or 'Opened by Link' to keep the important lists at the top and move less important lists to the bottom

</td><td>

Lists can't be re-ordered in the 'Shared with me' section in the 'My List' tab.

</td><td>

1.  Open Customer Service Management or Field Service Management Configuration Workspace.
2.  Open the 'List' page as an admin user.
3.  Create a few lists for as an admin user in the 'My Lists' tab.
4.  Share all these lists with the user, Fred Luddy.
5.  Impersonate the user, Fred Luddy.

Notice that there is a shared list in the 'Shared with me' section inside the 'My List' tab.

6.  Attempt to reorder the lists by using the drag and drop function.

 Expected behavior: There should be a re-ordering capability to arrange the shared lists when there are many lists in 'Shared with me' section. This should also apply to the 'Opened by Link' list.

 Actual behavior: The user Fred Luddy can't reorder the lists in the 'Shared with me' section.

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

List Administration

 PRB2009991

</td><td>

'Workflow'-type fields are displaying as 'Pending - has not started' for all values

</td><td>

This requires a single-line change that adds a defensive .clone\(\) call to deep-copy the choice list before WorkflowIcons.process\(\) mutates it. This prevents the shared cache from being poisoned by in-place label overwrites.

</td><td>

1.  Navigate to the table schema for the 'Incident' table.
2.  Create a custom field named 'Test column' with the field type set to 'Workflow'.
3.  Configure 2-3 choice options for the newly created custom field.
4.  Select 2-3 incident records and set values for the **Test column** field using any of the available options.
5.  Open UI Builder.
6.  Create an experience and page by using the 'List Page' template.
7.  Once the page is created, navigate to it on the instance.
8.  From the sidebar navigation, navigate to **Incidents** &gt; **All**.
9.  Select the **Personalize fields** button on the list page.
10. Add the **Test column** custom field to the visible columns.

Observe that the workflow stages for the custom workflow type field appear empty.

11. Open any incident record that has a value set for this field \(can be opened in classic view as well\). If the field is not visible, add it to the 'Form' view.
12. Observe that the field displays 'Pending - has not started'. Note that even when the field value is changed via background script, it continues to display 'Pending - has not started'.

 Expected behavior: The display value should be as per available choices.

 Actual behavior: It displays 'Pending - has not started' even after changing value. 'Pending - has not started' is not even available as a choice option for a field.

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

 PRB2014997

</td><td>

In Service Operations Workspace, live updates of Alert Express List displays en 'Invalid Row Data, Duplicate Row Keys' error on auto-refresh

</td><td>

handleLiveListChange\(\) \(~line 448\) dispatches LIVE\_LIST\_FETCH\_ROW\_LAYOUT\_REQUESTED for every AMB event with no in-flight deduplication. When multiple AMB events arrive for the same sys\_id before the first GraphQL fetch completes, findRowByFullKey\(\) \(parentChildBehaviorUtils.js:95\) returns null for each event and each event triggers its own fetch. Each fetch response then adds the row via addEnteredRowToRowDefinitions\(\) \(~line 676\), resulting in duplicate row keys. hasDuplicateRowKeys\(\) \(rowBehavior.js\) detects duplicates and triggers the error overlay.

</td><td>

 

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

Live Archive

 PRB1976776

</td><td>

There's an error when restoring to long table name aliased tables

</td><td>

This happens with both chunking and hex based approaches. It happens in both related records and payload parsing. Also, the state in sys\_archive\_restore\_request is set to 'complete' instead of 'Error' in this case.

</td><td>

1.  Create a long table name aliased table in sys\_db\_object.
2.  Add records to the table in step one.
3.  Create and run an archive rule for the table.
4.  Create a bulk restore request for the ar\_ aliased table.
5.  Run a bulk restore or wait on an hourly trigger.

 Expected behavior: All records matching the restore request conditions should be restored.

 Actual behavior: The chunks error out and an error is seen in the logs.

</td></tr><tr><td>

Live Archive

 PRB1980314

</td><td>

After archiving, bulk restoring, and killing a node, checkpoint rows aren't populated in sys\_archive\_restore\_checkpoint

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Live Archive

 PRB1982265

</td><td>

There's an error in the logs after running the DMscheduler daily trigger

</td><td>

There's an error: 'ERROR \*\*\* \#808133feature= AttachmentMigration AttachmentMigrationService: Error migrating attachment sys\_id: 73dec36dcc623210 f877c28b1770b27b from: ROWSTORE to: COLUMNSTORE'.

</td><td>

1.  Migrate ar\_incident with 10k attachment records to columnstore.
2.  Trigger the 'Attachment Storage Migration' job using DMscheduler daily in sys\_trigger.
3.  While the chunks are processing, shut down the app node that the job is working on.
4.  Start the appnode.

 Once job resumes, notice there's a chunk stuck in a 'processing' state and an error in the logs after running DMscheduler daily trigger.

</td></tr><tr><td>

Live Archive

 PRB2007788

</td><td>

Data Management Console isn't reporting Tier 2 data correctly

</td><td>

Recently, data was offloaded to the new 'Columnar' solution for multiple tables to S3 storage. The Data Management Console displays a negative value, which is incorrect, and also doesn't match with the PG stats.

</td><td>

1.  Offload data from 'Columnar' tables.
2.  Log in to the instance to check the data for Tier 2 on Data Management Console.

 Expected behavior: 'Tier 2 Storage Used' should match the actual amount of data offloaded.

 Actual behavior: 'Tier 2 Storage Used' is negative.

</td></tr><tr><td>

Live Archive

 PRB2010081

</td><td>

Tier 2 archive plugins \(com.glide.columnar.archive &amp; com.glide.data\_management. columnar\_attachment\) and the legacy archive plugin \(com.glide.auxdb\) need to be renamed

</td><td>

The plugin ID should remain the same.

</td><td>

1.  Browse to the 'Plugins' page.
2.  Search for the archiving plugin shipping with Australia and the legacy plugins.

 Expected behavior: Marketing has changed the plugin names:

 -   com.glide.data\_ management.columnar \_attachments: New Name = Live Archive Attachments
-   com.glide. columnar.archive: New name = Live Archive
-   com.glide.auxdb: New name = System Archive

 Actual behavior: The incorrect plugin names are displayed.

</td></tr><tr><td>

Live Archive

 PRB2017269

</td><td>

Archive Destroy operations against archive tables that have attachments aren't performed

</td><td>

The 'Destroy' job deletes attachment data from sys\_attachment\_ doc\_columnar one attachment at a time, with each attachment requiring two SQL operations. Each attachment pair takes ~2.7 seconds. The ColumnarDeleteService is cleaning up related/peripheral records \(attachments, journals\) but the actual archive table row deletion either happens in a separate phase, was skipped, or happened in a subsequent chunk.

</td><td>

1.  Set up Tier 2 Live Archive.
2.  Archive a lot of records that have attachments.
3.  Configure an archive destroy rule that deletes these archived records.

 Expected behavior: The archive destroy operation should be performed.

 Actual behavior: Archive destroy is taking 1hr 40mins to delete 2,000 records.

</td></tr><tr><td>

Live Archive

 PRB2022367

</td><td>

In AttachmentMigrationService, copy-then-delete causes silent data loss through cascade delete on sys\_attachment\_attribute, dp\_attachment\_protection\_history, and sys\_attachment\_migration\_status

</td><td>

AttachmentMigrationService migrates attachments between the storage backends 'ROWSTORE' and 'COLUMNSTORE' by creating a new sys\_attachment row with a new sys\_id, and then deleting the old one. Deleting the old sys\_attachment triggers reference\_cascade\_rule='delete' on every child table that references it, which silently destroys records that reference the old sys\_id, even though a valid replacement exists. The cascade engine has no knowledge of the new sys\_id, so the new sys\_attachment ends up with no associated child rows. The following child tables suffer silent data loss on every migrated attachment: sys\_attachment\_attribute \(per-attachment metadata\), sys\_attachment\_migration\_status \(migration tracking history\), and dp\_attachment\_protection\_history \(data-privacy / compliance audit trail\).

</td><td>

1.  Open an instance with the columnar attachments plugin, 'com.glide.data\_ management.columnar \_attachments,' enabled.
2.  Create a sys\_attachment row for any storage type, such as 'ROWSTORE', and note that the sys\_id equals 'X'.
3.  Insert child rows referencing 'X' with the following:
    1.  sys\_attachment \_attribute: row with the sys\_attachment = X
    2.  sys\_attachment \_migration\_status: row with the attachment = X
    3.  dp\_attachment \_protection\_history: row with the attachment = X
4.  Trigger the migration via AttachmentMigration Service.migrate Attachments\(\[X\], AttachmentStorageType .ROWSTORE, AttachmentStorageType .COLUMNSTORE\).
5.  Query each of the three child tables for the original sys\_id 'X' after the call returns.

 Expected behavior: All three child tables still contain rows for the migrated attachment, either against the same sys\_id, or under copy-then-delete which is re-pointed to the new sys\_id.

 Actual behavior: All three child tables contain zero rows for the original sys\_id 'X'. The new sys\_attachment record, the new sys\_id 'Y', exists with the migrated chunk data, but contains no rows in any of these three child tables. The data is silently lost and no error is logged. This occurs in any instance running on a build that includes AttachmentMigrationService for track, datamanagement, and downstream.

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
4.  Wait for one minute interval.

 Observe that a duplicate mb\_rollup event is queued because the state = 'ready' check misses the processing event.

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

 PRB2024310

</td><td>

MID Admin Workspace isn't auto-installed with ITOM Infra Services Workspace app

</td><td>

In an Australia instance, the ITOM Infra Services Workspace is installed but the MID Admin Workspace is not, though it should be.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1984253

</td><td>

When in offline mode for external uses, cost and currency display inaccurately

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1999865

</td><td>

Support onSubmit UI Rule

</td><td>

Configure and execute UI Rules at the time when the input form screen is submitted both online and offline.

</td><td>

 

</td></tr><tr><td>

Multi-Instance Framework

 PRB2019094

</td><td>

Async messages from a JavaScript layer aren't signed so they aren't validated on a receipt

</td><td>

MIF async messages sent from the script layer aren't signed because the two argument 'MessageSender.createTrusted \(scopeName, messageProducer\)' factory method uses a no-op identity augmentor instead of 'EnvelopeTrustAugmenter'. However, the Hermes receiver still expects and validates ISK signatures on all incoming messages, causing a failure when attempting to decode the null Base64 signature field.

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

The MMS plugin name displays 'MAINT ONLY', and should be updated.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2022500

</td><td>

If a work item is assigned to the same agent repeatedly, the desktop notification stops appearing entirely

</td><td>

A new desktop notification should appear on every work item assignment.

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

Now Assist in Document Intelligence

 PRB2030125

</td><td>

Support attachments where the file names doesn't contain '.type' at the end

</td><td>

There's an error: '\{"attachment":\{\},"task":\{"708a54b23b 810f50141a0 e0f23e45a0b":\{"error\_msg":"Prediction server is not able to process the attachments: begin 0, end -1, length 9"\}\}\}'.

</td><td>

1.  Have a png image file with no errors.
2.  Rename it to have a file name with '.png'.
3.  Upload it to an instance.
4.  Test the attachment summarization.

 Observe an error.

</td></tr><tr><td>

Now Assist Nextwave Experience

 PRB2009794

</td><td>

Synthesized response generation isn't considering custom sources

</td><td>

 

</td><td>

 

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

 Actual behavior: On-Glide mic seen in input bar.

</td></tr><tr><td>

On-Call Scheduling

 PRB2030962

</td><td>

The On-Call Scheduling family plugin is installed on upgrading to Australia.

</td><td>

The On-call plugin has been added as a dependency for the sn\_sow\_on\_call plugin as part of core IT changes. This is causing issues for some users. On-call is automatically installed for new users via zboot. However, upgrade users need to install it manually. Due to the new dependency on the Store app, On-call is installed for some users when the commons bundle is upgraded. The dependency of the On-Call Scheduling plugin should be removed.

</td><td>

1.  Open any pre-Madrid instance where the On-call plugin isn't installed.
2.  Upgrade to Australia.

 Expected behavior: The On-Call Scheduling family plugin shouldn't be installed on upgrading to Australia.

 Actual behavior: The On-Call Scheduling family plugin is installed on upgrading to Australia.

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

Insights should be generated and displayed. Instead, the progress bar spins indefinitely and no generative AI logs are produced. The issue occurs because the app prepares a bulk request with three payloads and invokes it in async mode with a callback handler. When off-glide is enabled for the capability, the async callback flow \('NowAssistforSIR CorrelationInsights Callback'\) appears to break silently. No generative AI logs are generated, indicating the LLM call never completes or the response isn't handled correctly.

</td><td>

 

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
3.  Submit an off-Glide execution request with an explicit short timeout \(e.g., 5 seconds\) that targets a capability with a slow model/heavy prompt so that the Mosaic call takes around 10–20 seconds.

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

 Expected behavior: The caller-supplied timeout is the strongest signal and is honored by every Mosaic HTTP call in the pipeline \(preprocess gate, primary execute, postprocess DT translation\). In its absence, the control-setting, service-plan, and 60 second default apply \(in that order\). Exhausting the budget at any phase returns a timeout response \(status=error, errorCode=400001\). Override values are persisted to one\_api\_service\_ plan.timeout\_ms and cascade.

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
6.  Set the property 'com.glide.par. unified\_analytics .enabled' to false.
7.  Navigate to any record list \(e.g., /incident\_list.do\).
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

Performance Analytics Dashboards

 PRB2013831

 [KB2959423](https://hi.service-now.com/kb_view.do?sysparm_article=KB2959423)

</td><td>

There's a dashboard layout issue after upgrading an instance to Australia

</td><td>

After an Australia upgrade, multiple users are reporting issues with alignments of reports in dashboards. While reports aren't missing, they are displayed vertically in dashboards. The issue is reproducible with core legacy dashboards.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Performance Analytics

 PRB1990900

</td><td>

The system property com.snc.pa.dm.enable.mlb is set to true on non-Raptor DB Pro instances

</td><td>

Users can install a plugin with Raptor DB \(pro or standard\). With a schedule job, they can disable the feature by disabling the global property com.snc.pa.dm.enable.mlb.

</td><td>

1.  Open an instance with raptor standard.
2.  Validate the system property: com.snc.pa. dm.enable.mlb.

 Expected behavior: The property is set to false. The user shouldn't be able to control it and set its values.

 Actual behavior: The property is set to true. The user can control it and set its values.

</td></tr><tr><td>

Performance Analytics

 PRB1995131

</td><td>

There are Query Builder \(QB\) and Workspace UI error popup clips in the surrounding UI if a query fails for CMDB NLQ

</td><td>

Turning off the NLQ Prediction server results in an error message in both QB and in the CMDB Workspace, and the UI doesn't render as expected in CMDB Workspace.

</td><td>

1.  Turn off the NLQ Prediction server from sys\_properties by deleting the URL value 'glide.prediction \_service.url'.
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
3.  Open the scoresheet to edit the scores of the above indicator:
    1.  Feb 28th: 200
    2.  Jan 31st: 100
4.  Create a single score visualization using this indicator.
5.  Enable change and change percentage.

Notice that the change and change percentage aren't displayed.

6.  Disable the system property 'com.glide.par .unified\_analytics. enabled'.
7.  Create a single score PA widget on the above indicator, with Visualization: Latest Score.
8.  Leave all other fields as the default value.
9.  Add the above widget to a Core UI dashboard.

 Notice that the widget displays the change \(100\) and change percentage \(100%\).

</td></tr><tr><td>

Performance Analytics

 PRB2009359

</td><td>

Turn off/delete the 'Populate Indicator Source Row Count' job, as the guardrails are deprecated in Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB2014881

 [KB2977667](https://hi.service-now.com/kb_view.do?sysparm_article=KB2977667)

</td><td>

Core UI widget date settings aren't retained on dashboards

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2016214

</td><td>

oob-pa-cxo-apps are missing from the Glide distribution due to an app packaging issue

</td><td>

These apps have an incorrect scope and aren't included in the ZIP or DIST packaging. As a result, users aren't able to auto-upgrade to the latest versions of these apps through the monthly release pipeline.

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
4.  Select the **arrow** to view the 'Recent Dashboards' list.

If this is the first login of the day, observe that the list contains dashboards that may not have been previously accessed.

5.  Switch between several dashboards.

Observe that the 'Recent Dashboards' list updates to reflect the dashboards opened during the session.

6.  Log out of the instance.
7.  Log back in using a new browser tab.

 Observe that the 'Recent Dashboards' list resets and displays a different, seemingly random list of dashboards instead of the ones previously accessed.

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

 PRB2005188

</td><td>

Override the scope of any par\_dashboard\_\* record with the scope received from the dashboard

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2006097

</td><td>

Allow the user to turn on/off the AI summary generation in a dashboard

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Open any dashboard.

The Now Assist context menu \(NACM\) component appears above the grid.

3.  Open the 'Settings' panel.
4.  Toggle off the AI summary generation.
5.  Save and reload the dashboard.

 Expected behavior: The NACM shouldn't appear.

 Actual behavior: The NACM appears again.

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

 PRB2014426

</td><td>

A duplicated dashboard doesn't persist an AI summary generation value

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Open any Platform Analytics dashboard.
3.  Verify the dashboard summary component is visible on top.
4.  Verify the 'Setting' panel AI summary generation toggle is on.
5.  Duplicate the dashboard.

 Expected behavior: The dashboard summary should be visible in the duplicated dashboard.

 Actual behavior: The dashboard summary isn't visible in the duplicated dashboard.

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

Addtional controls for single and multi select

</td><td>

For both radio buttons and checkboxes, there should be a way to clear the selection instead of using the 'Clear all filters' capability on the dashboard level.

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

 PRB1989820

</td><td>

Users with the itil role are shown reports in read-only mode

</td><td>

If a user has the itil role, there should be no read-only mode. It should display in 'Edit' mode.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1998821

</td><td>

The Platform Analytics Migration Center summary window isn't counting all domain dashboards when doing migration in the global domain

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2003834

</td><td>

AppTier CPU increases by 4 points \(~18%\) when background jobs are turned on

</td><td>

AppTier CPU increased in Australia compared to the Zurich baseline when background jobs are turned on during loadsim performance testing. The primary driver is the 'events\_process\_0' background job, which regressed +254% in average execution time. The 'Script Action: Refresh ready\_to\_migrate after XML load' runs every time there is an XML load on tables pa\_m2m\_ dashboard\_tabs, pa\_tabs, sys\_portal, and sys\_portal\_preferences. The event action runs a script that looks at all dashboards' related artifacts, makes an assessment, and fills out the 'ready\_to\_migrate' column on each dashboard. This action is unnecessarily long-running because it attempts to update all dashboards, most of which aren't needed.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2010427

</td><td>

Turn off auto-conversion of homepages to CoreUI dashboards after upgrades

</td><td>

1000 homepages are migrated every day, and it triggers a business rule that migrates CoreUI automatically.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2022823

</td><td>

Allow users to configure the redirection of Core UI Performance Analytics widgets to the Analytics Hub instead of to 'KPI details'

</td><td>

Users that activated Next Experience after migrating or upgrading to Australia will be redirected to 'KPI details' when selecting a Performance Analytics widget, even if they keep using Core UI dashboards. This issue occurs because the unified\_analytics property forces the re-direction to 'KPI details'.

</td><td>

 

</td></tr><tr><td>

Playbook Experience

 PRB2007586

 [KB2994368](https://hi.service-now.com/kb_view.do?sysparm_article=KB2994368)

</td><td>

Declarative Action marks playbook activity as complete despite throwing an error from the UI action

</td><td>

When a custom declarative action is configured with the action model set to 'Playbook Card' in order to display a button on a playbook activity, the expected behavior after displaying an error is as follows: if the UI action invoked by the declarative action displayed an error message, the error was displayed to the user, and the underlying activity was not marked as complete. This allowed the user to address the issue before proceeding. As of the Zurich release, this behavior has changed. When the UI action returns an error message, the error is displayed to the user; however, the activity is also marked as complete. This represents a change in the expected workflow, as the activity now progresses regardless of whether the error condition has been resolved.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2012190

</td><td>

When any one pill value is null, it returns null for the value of the whole input field

</td><td>

This happens for any multi pill-text inputs.

</td><td>

1.  Create action1, which takes in 1 input and 1 output of type 'String'.
2.  Create action2, which has 3 inputs of type 'String' and can be used as dynamic input action.
3.  Create a new subflow1, which has 3 inputs.
4.  Make 1 input a dynamic input.
5.  Assign the previously created action as the dynamic input action.
6.  Publish both of them.
7.  Create a playbook.
8.  Add a stage.
9.  In activity picker, enable 'Include all automation assets'.
10. Select action1 and subflow1.
11. Set the dynamic input to output of action1 and the other 2 dynamic inputs with some static value.
12. Leave the value of that pill empty.

 Expected behavior: The dynamic input value returns for the other 2 dynamic inputs set.

 Actual behavior: The whole dynamic input value is set to empty.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2021433

</td><td>

Dot-walkers aren't working on the 'Recommended actions' table for playbook inputs

</td><td>

 

</td><td>

1.  Provision an instance with the 'Customer Service' plugin installed.
2.  Navigate to **All** &gt; **Recommended Actions** &gt; **Contexts**.
3.  Open any existing context.
4.  Under the 'Rules' related list, create a rule with the **Name** and **Condition** fields filled out.
5.  Under the 'Recommended actions' related list, select **New** with the action type as 'Playbook'.
6.  Set action as any playbook with inputs and save the record.

 Expected behavior: The playbook inputs dotwalker should have content inside, and it's the case table meta fields.

 Actual behavior: The dotwalker opens to have empty content.

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

 PRB1972729

</td><td>

On the 'Opportunity details' page, when applying views on the process map, the progress tracker isn't displayed and the user has to hard refresh the page to apply views

</td><td>

 

</td><td>

1.  Mine a project with findings with more than 1 activity definition.
2.  From the S&amp;I page, select any of the rule based improvement opportunities to open the 'Opportunity details' page.
3.  On the map, select the gear icon.
4.  Select a view and apply.

 See that the progress tracker isn't updating and the user has to hard refresh the page to apply the view. The 'Scheduled task completed' alert is displayed but the scheduled task isn't displayed in the 'Scheduled tasks' panel of the page.

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

 PRB1984137

</td><td>

The 'Project' card gives an incorrect average duration

</td><td>

 

</td><td>

Mine a playbook project.

 Observe the average duration on the project card and the average duration in the project itself. Notice that they are not the same. They should match.

</td></tr><tr><td>

Process Mining Workspace

 PRB1990953

</td><td>

Change the default number of records per cluster in a request to '50'

</td><td>

Currently, it sends 200 records per cluster to create the intent and activities. Since there are 5 clusters in each request, it takes more processing time. By reducing the number to 50, the request should be processed in about 10 minutes.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1994902

</td><td>

When clustering on intermodal arcs, 'show records' redirects to a child table with 'No records to display'

</td><td>

 

</td><td>

1.  Mine a MDM project on incident and Task\_SLA.
2.  Open Analyst Workbench.
3.  Select any intermodal arc.
4.  Once it's completed, select **View result**.
5.  Select **Show records**.

 Expected behavior: The user should be shown the incidents belonging to the cluster.

 Actual behavior: Observe that the user is redirected to the 'Task SLA' list page with a 'No records to display' message.

</td></tr><tr><td>

Process Mining Workspace

 PRB2003893

</td><td>

Duplicate results display when 'Intent and activity analysis' is applied on a filtered model

</td><td>

 

</td><td>

1.  Initiate 'Intent and activity analysis' on any node.
2.  Apply breakdowns that should have a WIP node.
3.  Select the WIP node.
4.  Observe the results already generated on WIP node and select **View**.

 Expected behavior: The 'View results' card shouldn't be displayed on a breakdown applied model. It's a new task altogether.

 Actual behavior: It triggers and 'Intent and activity analysis' and generates the duplicate results.

</td></tr><tr><td>

Process Mining Workspace

 PRB2005530

</td><td>

Users can't submit an automated finding def when the left navigation search panel is opened

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Keep the left navigation panel open.
3.  Try adding a new automated finding def.

 Observe that the buttons are not visible/accessible.

</td></tr><tr><td>

Process Mining Workspace

 PRB2008088

</td><td>

Project setup data fetch fails when a user with no role opens the shared project configuration

</td><td>

 

</td><td>

1.  Share a project with a user that has 0 roles.
2.  Open a shared project configuration as the shared user.

 Notice that data on project setup fails to load.

</td></tr><tr><td>

Process Mining Workspace

 PRB2011383

</td><td>

Backport the Appsee event

</td><td>

 

</td><td>

 

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

Project Management

 PRB2009176

</td><td>

Opening the Project Status Report in the Project Workspace triggers an update to the **Overall Health** field on the corresponding project record

</td><td>

Opening the Project Status Report within the Project Workspace updates the **Overall Health** field on the corresponding project record to match the value from the status report.

</td><td>

1.  Open a project in the Project Workspace \(PW\).
2.  Navigate to the **Status Report** tab.
3.  Create a status report.
4.  Navigate to the **Details** tab.
5.  Locate the **Status** field.
6.  Ensure the **Status** field is different from the **Overall Health** field in the status report. If both values are the same, manually update the **Status** field on the project.
7.  Open the 'Status Report' tab from the left panel.
8.  Navigate back to the **Details** tab.

 Notice that the **Status** field is automatically reverted to match the **Overall Health** value from the status report.

</td></tr><tr><td>

Project Management

 PRB2021806

</td><td>

Add a 'No status' option to the **Project status** field

</td><td>

The **Project status** field \(pm\_project.status\) currently doesn't include a 'No status' option, which prevents projects from having an unset/neutral status state. This causes ambiguity in reporting and makes it difficult to distinguish between projects that have not yet been assigned a status versus those intentionally marked as 'On Track' or 'At Risk'. A 'No status' option should be added to the **Status** field choice list. This ensures that status transitions — including from an unset state to a defined status — can be accurately captured and reflected in usage analytics.

</td><td>

1.  Navigate to **Project Management** &gt; **Projects** &gt; **All Projects**.
2.  Open any active project.
3.  Select the **Status** field.

 See that a 'No status' option should be available.

</td></tr><tr><td>

Record Hierarchy

 PRB2013585

</td><td>

Reconciliation of record hierarchy with missing path field skipped

</td><td>

If the user deletes the rh.hierarchy.create event, there is no 'Reconcile Hierarchy' link under Related Links. If the user executes SNC.RecordHierarchyAPI.get\(\).reconcilePaths\(sysId\), no event is posted to resume creation of the hierarchy.

</td><td>

1.  Create a sys\_record\_hierarchy.
2.  Immediately delete the associated rh.hierarchy.create event that's generated in sysevent.

Observe that the sys\_record\_hierarchy is in a PENDING\_CREATE state with no event to progress it to the next step.

3.  Visit the sys\_record\_hierarchy record.

Notice that there is no 'Reconcile Hierarchy' link under 'Related Links'.

4.  Copy the sysId of the sys\_record\_hierarchy record.
5.  Navigate to **Scripts - background**.
6.  Execute SNC.RecordHierarchy API.get\(\). reconcilePaths\(sysId\).

 Observe that nothing happens. No event is posted to resume creation of the hierarchy.

</td></tr><tr><td>

Record Hierarchy

 PRB2014979

</td><td>

Allow RecordHierarchies to always be usable optionally unless it is disabled

</td><td>

The current behavior shows that after a record hierarchy is defined, any query operations that use the hierarchy will explicitly return 'false' until every record in the hierarchy has been assigned a path. After paths have been assigned, the hierarchy is said to be 'usable' as its fully initialized and ready for queries. A GP was added to optionally allow the hierarchy to be usable while records are being assigned paths. The results for queries may be incomplete or partially stale depending on how long the initialization takes place, but should otherwise be accurate. Users are beginning to use IN\_HIERARCHY conditions for all sorts of features ranging in criticality, up to and including ACLs. If the record hierarchy runs into some sort of issue, such as it can render the record hierarchy unusable and all queries would begin to fail. However, the paths assigned to all records are still valid as long as changes are minimal, and can continue to return mostly accurate results while any issues with the record hierarchy feature are addressed. This fix is to address usability; as long as the record hierarchy isn't explicitly deactivated, it can be made 'usable' and queries will return results based on whatever paths may be assigned at the time.

</td><td>

 

</td></tr><tr><td>

Record Watcher

 PRB2016869

</td><td>

IndirectRecordCollector. setPreviousValueFrom PreviousRecord throws an error on a null ElementDescriptor in a dotwalked path, aborting Record Watcher enqueue and stalling flows

</td><td>

When a sys\_rw\_indirect\_query is configured with a dotwalked condition path that contains a field segment which does not exist on the traversed table \(returns null from getElement\(\)\), IndirectRecordCollector. setPreviousValueFrom PreviousRecord at line 304 calls fieldEd.getReference\(\) on a null ElementDescriptor and throws an error. This exception propagates up through RecordWatcherService.enqueue, aborting the entire enqueue and silently preventing all flow responders from executing for that record update. Flows waiting on a catalog task or incident completion stall permanently — the sys\_flow\_rw\_action record is created but never processed, and DeferredResponderHandler does not recover this class of failure.

</td><td>

1.  Create a sys\_rw\_indirect\_query on the task table \(or any table\) with a dot-walked condition path that traverses a field not present on all subtype records.
2.  Trigger a record update \(GlideRecord.update\(\)\) on a record of that table.

 Observe in the transaction log: 'RecordWatcherService SEVERE \*\*\* ERROR \*\*\* record-watcher: Caught error attempting to enqueue change \[table.sys\_id\] followed by java.lang. NullPointerException: Cannot invoke "com.glide.db.ElementDescriptor.getReference\(\)" because "fieldEd" is null at IndirectRecordCollector. setPreviousValue FromPreviousRecord \(IndirectRecordCollector.java:304\). Observe that any flow responder waiting on that table/record never executes — sys\_flow\_rw\_action record is created but state never advances.

</td></tr><tr><td>

ReleaseOps - Family

 PRB1966100

 [KB2733370](https://hi.service-now.com/kb_view.do?sysparm_article=KB2733370)

</td><td>

Deployment Analyzer forms are broken

</td><td>

Deployment Analyzer forms are empty, breaking reports. Users are unable to fix it because when they go to form layout, no fields are listed.

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

When the user changes the start date and end date from a resource plan, the business rule \(BR\) UpdateCostPlanAssociatedToResourcePlan launches an event. The BR 'Recreate Requested Allocations' is also launched, updating the resource plan again and changing the planned cost. In summary, when the user updates the dates, the system updates the resource plan twice, one time for the dates and another for the planned cost, practically at the same time. Both changes trigger the BR UpdateCostPlanAssociatedToResourcePlan and two events are created. Since there are two events in the system, they will try to perform the same action, and this could lead to problem concurrency. The two events are processed at the same time and the cost plan breakdowns are created twice.

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

7.  Create any field on the resource assignment table which is dependent on any other **Reference** field.

 Observe that the dependent config isn't supported in bottom grid choices. It should be supported.

</td></tr><tr><td>

Resource Management

 PRB2024520

</td><td>

Fetching choices with their dependent field values to prepare criteria

</td><td>

The created field doesn't show the choices as per the dependent config defined.

</td><td>

1.  Create any field on the resource assignment table which is dependent on any other reference field.
2.  Add that field in the resource assignment bottom grid in PWS.
3.  Open the project workspace.
4.  Navigate to the project.
5.  Create an unassigned assignment from the bottom grid.

 Observe that the created field doesn't show the choices as per the dependent config defined.

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

 PRB2029429

</td><td>

There's a Zboot error due to a syntax error

</td><td>

There's an error: 'Error : \*\*\* ERROR \*\*\* invalid return \(refname; line 7\)'.

</td><td>

 

</td></tr><tr><td>

Security Incident Response Explorer

 PRB2013795

</td><td>

The sub-project oob-secops-npm-apps in oob-apps isn't picked up in a Glide build

</td><td>

The apps are missing in Glide's distribution.

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

 See that it should be logged, but isn't.

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1966196

</td><td>

There's an issue with 'Also Request for'

</td><td>

Duplicate requested items \(RITM\) are generated when the same user is selected in both the **Requested For** and **Also Request For** fields. When the **Requested For** user is selected first, it automatically removes that user from the **Also Request For** list, preventing duplication. However, when a user is selected first in **Also Request For** and then again in **Requested For**, the platform allows the same user to be selected in both fields. This results in multiple RITMs being generated for the same user.

</td><td>

1.  Log in to an instance.
2.  Navigate to the Service Catalog.
3.  Open a catalog item.
4.  On the catalog item form, ensure that the **Requested For** field is empty.
5.  Select the **Also Request For** \(multi-user\) icon or selector and select a user \(e.g., User A\).
6.  After selecting the user in **Also Request For**, attempt to select the same user in the **Requested For** field.
7.  Fill in all mandatory fields.
8.  Submit the request.
9.  Open the associated REQ record and review the generated RITMs.

 Actual behavior: Duplicate RITMs are created for the same user.

 Expected behavior: The system should prevent selecting the same user in both fields.

</td></tr><tr><td>

Service Catalog

 PRB2014228

</td><td>

Update the copy in the alert banner

</td><td>

Catalog item forms should be automatically pre-filled using the context from the conversation. The user shouldn't have to to re-enter information they've already shared in the chat.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2020118

</td><td>

Ensure that a search term is a minimum of 3 words before triggering the slot fill

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1998724

</td><td>

'Create Layer 2' connections causes Out of Memory \(OOM\) errors if the device has many router interfaces

</td><td>

The creation of 'Layer 2 Connections ' can cause excessive memory and multi-node events.

</td><td>

1.  Create server with 30,000 router interfaces.
2.  Run the script in background scripts.

 Notice that all the records will be used for calculation.

</td></tr><tr><td>

Service Mapping

 PRB2006053

</td><td>

There's a missing conditional\_table\_ query\_range ACL for the cmdb\_ci\_service\_discovered in the plugin com.snc.cmdb.it\_service

</td><td>

Calls can fail at runtime, causing range query operations to be denied.

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

Service Operations Workspace for Change Management

 PRB1921763

</td><td>

A reference qual isn't working for a dependency field on the Service Operations Workspace \(SOW\) 'Overview' page

</td><td>

A dependency field on the SOW 'Overview' page isn't working, as the 'Assigned to' field won't only return the available users from the assignment group value, but rather the whole itil user list.

</td><td>

1.  Navigate to the 'Change Models' module.
2.  Open the 'Normal' change model.
3.  Set the assignment group to 'Application Development' in the **Record preset** field.
4.  Save.
5.  Navigate to the 'Change Request' form in Core UI.
6.  Switch to the 'SOW-Overview-Change' form view.
7.  Right-click the form header.
8.  **Configure** &gt; **Form Layout**.
9.  Modify the 'Summary' form section.
10. Add **Assignment group** and **Assigned to** fields.
11. Save.
12. Navigate to **Service Operations Workspace** &gt; **Changes list** &gt; **New** &gt; **Normal card** &gt; **Continue**.
13. On the 'Change' form, the Application Development is pre-populated. Search the **Assigned to** field for a list of available users.

 Expected behavior: See only users in the 'Application Development' group.

 Actual behavior: More users are shown that aren't in the 'Application Development' group.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1977258

</td><td>

In Service Operations Workspace \(SOW\), there's a JavaScript \(JS\) error 'Assess risk', and the modal doesn't open

</td><td>

 

</td><td>

1.  Provision an instance with the Change Risk Assessment v2 plugin installed.
2.  Navigate to a change request \(normal or emergency\) in SOW.
3.  Select the 'Risk assessment' related link.
4.  Complete the assessment.
5.  Submit from the 'Overview' page.
6.  After it reloads, on the right-hand side \(record information\), there should be card titled 'Risk'.
7.  Select the 3 dots to open a contextual menu.
8.  Select **Assess risk**.

 This should open a modal with the assessment and its answers to allow changes, but nothing happens. Also, there's a JS error in the browser's console.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1981820

 [KB2755016](https://hi.service-now.com/kb_view.do?sysparm_article=KB2755016)

</td><td>

Service Operations Workspace action bar buttons aren't displayed even if 'Display action' is set to true for a change state

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1983773

</td><td>

Overview tab sections are refreshed on an update

</td><td>

When working in the Service Operations Workspace \(SOW\) change request overview, the sections are refreshed whenever any field in the 'Scope and Impact/Schedule/Summary' section is updated. This problem occurs only when the fields in the 'Assignment' section, specifically 'Assignment group' or 'Assigned to', are filled in. If these fields are left blank, the issue doesn't occur.

</td><td>

1.  Open or create a change request in SOW.
2.  Verify that the **Assignment Group** field is updated.
3.  In the 'Overview' tab, update a field in the 'Scope and Impact' section and move the control outside the field.

 See that the 'Overview' section begins to refresh, which shouldn't occur. This same issue arises when updating fields in other sections.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1987932

 [KB2807996](https://hi.service-now.com/kb_view.do?sysparm_article=KB2807996)

</td><td>

In 'Change Management' in Service Operations Workspace \(SOW\), the **Assess Risk** button isn't working

</td><td>

When a user attempts to complete a risk assessment for a change request in SOW, the modal appears briefly and then immediately closes.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Operations Workspace for On-Call Scheduling

 PRB1993717

</td><td>

On Service Operations Workspace \(SOW\), there's no place to set the rotation start time for the roster

</td><td>

When users create the shifts on SOW, the rotation is automatically happening at midnight.

</td><td>

1.  Navigate to SOW.
2.  Navigate to schedules.
3.  Open one of the groups.
4.  Open a shift on the side panel.
5.  Navigate to the 'Members' tab.

 See no place to set the rotation start time.

</td></tr><tr><td>

Service Operations Workspace

 PRB1982622

</td><td>

The declarative action 'Copy Link' introduced in Service Operations Workspace \(SOW\) throws an error: 'Declarative Action scripted client condition expression evaluation failed'

</td><td>

The declarative action 'Copy URL' was updated to include values in the scripted client condition in the latest upgrade of SOW. The scripted client condition was empty earlier. While this declarative action is in the SOW application scope, 'Enable for all Experience' is checked, so it's rendered for Project Workspace/other configurable workspaces as well. The error is thrown because it can't be evaluated for Project Workspace.

</td><td>

 

</td></tr><tr><td>

Service Operations Workspace

 PRB2013463

</td><td>

Customer Service Management workspace experience is not opening in UI Builder

</td><td>

 

</td><td>

1.  Navigate to UI Builder.
2.  Navigate to Customer Service Management workspace experience.

 Observe that it's opening with a 500 internal server error.

</td></tr><tr><td>

Service Portal

 PRB1981788

</td><td>

A non-admin user can't view the notification on a portal and are getting the recordUpdateCount

</td><td>

 

</td><td>

Log in to a portal with some non-admin user.

 Expected behavior: A notification shall appear for the non-admin user.

 Actual behavior: Check for the notification and see that no notification is visible.

</td></tr><tr><td>

Service Portal

 PRB1999839

 [KB2983856](https://hi.service-now.com/kb_view.do?sysparm_article=KB2983856)

</td><td>

When Multi-factor Authentication \(MFA\) and Password Needs Reset is true, the password reset workflow refreshes after selecting 'Submit' on the initial login and redirects to the backend Platform UI

</td><td>

When MFA is configured on an instance and Password Needs Reset is set to true on a vendor contact record, they are presented with a screen to change their password on initial login. After changing the password on the initial screen and clicking submit, the page refreshes back to the same password reset screen. If they perform the same steps again and click submit, they are finally redirected but the redirect is incorrect and redirects the user to the backend UI.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB2013342

 [KB2974430](https://hi.service-now.com/kb_view.do?sysparm_article=KB2974430)

</td><td>

In Australia, the Mission Control \(/mc\) portal fails to load the Bootstrap CSS \(sp-bootstrap-rem.scss\), while the same configuration works correctly in Zurich

</td><td>

In Australia, the Mission Control \(/mc\) portal no longer auto-loads the Bootstrap CSS \(sp-bootstrap-rem.scss\), resulting in whole portal not loading correctly. The same portal, theme, and configuration work correctly on the Zurich instance, indicating a release-specific behavior change.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB2014571

</td><td>

Alignment of the Now Assist search results gets overflow

</td><td>

This happens on the portal while loading on browser resolution size 360 x 640.

</td><td>

1.  Make sure the Now Assist Genius Result \(GR\) is enabled on the portal.
2.  Navigate to a base instance.
3.  Change the session language to Deutsch.
4.  Navigate to the /esc portal.
5.  Open the developer tool of the browser.
6.  Set the resolution as 360 x 640.
7.  Search for any keyword \(for example, people manager\).

 Observe that the filter text 'Am relevantesten' gets overflow.

</td></tr><tr><td>

Service Portal

 PRB2020265

</td><td>

The 'Homepage Search' section isn't available at higher zoom levels

</td><td>

 

</td><td>

1.  Open any instance in a Chrome browser.
2.  Append the url using /sp to open Service Portal.
3.  On the homepage, notice the 'How can we help? text search box.
4.  Open inspect.
5.  Expand the three dots menu to select the first option of 'Dock side', so that the DevTools window opens in a new tab.
6.  Change the page width to 1280px by dragging the edge of the browser window.
7.  Select the browser menu using the three dots button in the top right corner of the browser window.
8.  Zoom the page to 400% and note if the 'How can we help?' text search box that was visible at 100% \(without zooming\) is still visible at 400% zoom.
9.  Decrease the zoom.

Notice that this section starts disappearing at the 175% zoom level.


 Actual behavior: The 'My Saved Bundles' section isn't available on a catalog page at higher zoom levels.

 Expected behavior: The 'My Saved Bundles' section is should be available on a catalog page at higher zoom levels.

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

the cached RecordCard is returned without checking if the user has access to record

</td><td>

This is a caching issue, and occurs for both with Incident and HR records. When the code checks if the Record Card is in the cache, it does not re-check if the user can access the record or not. When clearing the cache, the record access check is calculated correctly.

</td><td>

1.  Create an incident \(INC1\) as the user Abel Tuter.
2.  Create a discussion on it.
3.  Paste INC1 in the chat.

Notice that it renders a record card, and the user Abraham Lincoln cannot access INC1 in the sidebar chat.

4.  As the user Abraham Lincoln, attempt to paste the INC1 number in the chat.

Notice that Abraham Lincoln can see the the INC1 record card and its details, when Abraham Lincoln should not be able to because they have no access.

5.  Create another incident \(INC2\) as the user Abel Tuter.
6.  Create a discussion on it.
7.  Paste INC2 in the chat.

 Notice that it renders a record card, and the user Abraham Lincoln cannot access INC2 in the sidebar chat. The INC2 record card is not in the cache.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB2023462

</td><td>

Turn off the sidebar collab chat scope main enablement

</td><td>

 

</td><td>

1.  Provision an instance with the plugin com.sn\_hr\_core \(Human Resources Scoped App: Core\) installed.
2.  Create an HR case for Abel Tuter.
3.  Create a discussion with Abel.
4.  Try to upload an attachment.
5.  Ensure that it works with no errors.

 Expected behavior: The file should get attached to the discussion.

 Actual behavior: The error message 'User is not authorized' appears.

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

Software Asset Management Workspace \(Glide\)

 PRB1992196

</td><td>

In Software Asset Management workspace, the 'Assets Covered' tab is in English

</td><td>

It should be translated.

</td><td>

1.  Log in to Software Asset Management workspace.
2.  Select the **Licensing Operations** module on the left pane.
3.  Under the standard list, select **Software contracts** in 'Contracts'.
4.  Select a contract.

 Note that the 'Assets Covered' tab isn't converted to German.

</td></tr><tr><td>

Software Asset Normalization

 PRB1991265

</td><td>

Regex normalization suggestions are incorrectly excluded when the product map sets suggested\_rule\_table on the Discovery model

</td><td>

\_createSuggestionsForRegexDMs\(\) in NormalizationEngine has a 'NOT IN' filter that excludes DMs with suggested\_rule\_table in \[PACKAGE\_MAP\_TABLE, PRODUCT\_MAP\_TABLE, PATTERN\_RULES\_TABLE, WIDE\_NET\_MAP\_TABLE\]. PRODUCT\_MAP\_TABLE shouldn't be in this exclusion list because product map rules don't create their own suggestions — they are only a stepping stone for wide-net suggestions.

</td><td>

1.  Manually normalize a Discovery model.
2.  Ensure that there's an active product map rule and an active Regex normalization rule that both match this Discovery model \(DM\).
3.  Ensure that there's no active package map rule, pattern rule, or wide-net rule for this DM.
4.  Run the 'SAM - Find Normalization Suggestions' job.

 Expected behavior: A Regex suggestion should be created, because product map rules don't generate suggestions themselves — they only serve as an entry point for wide-net processing. Regex should be evaluated for DMs where product map is the only suggested rule table.

 Actual behavior: No Regex suggestion is created. The DM's suggested\_rule\_table is set to samp\_product\_map \(by the product map suggestion path\), which causes \_createSuggestionsForRegexDMs\(\) to exclude this DM from regex processing via the NOT IN filter.

</td></tr><tr><td>

Software Asset Normalization

 PRB2013453

</td><td>

The 'Find Normalization Suggestions' job fails to create suggestions for Regex rules due to accessing the private closure variable \_regexMap

</td><td>

NormalizationEngine.\_createSuggestionsForRegexDMs\(\) accesses regexEngine.regexMap, but \_regexMap is a private variable inside RegexNormalizationEngine's IIFE closure. It is not exposed as a public property. The code also called getDM\(\) and applyRegexRuleToDiscoveryModel\(\) in a loop over this inaccessible map, so the entire regex suggestion path was non-functional.

</td><td>

1.  Ensure that the Regex normalization feature is active \(com.sn\_itam\_samp plugin\).
2.  Have at least one Regex normalization rule in the samp\_regex\_normalization\_rule table.
3.  Create or have a manually normalized discovery model that would match a Regex rule.
4.  Run the 'SAM - Find Normalization Suggestions' scheduled job.

 Expected behavior: A normalization suggestion should be created linking the discovery model to the matching Regex rule.

 Actual behavior: No normalization suggestion is created for Regex rules. The job silently fails for the Regex code path.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2015480

</td><td>

Regex normalization discards edition\_map \(including versionMap\) when edition\_index is null on the rule

</td><td>

In \_buildRuleObject\(\), the edition\_map is guarded by 'gr.edition\_index &amp;&amp; gr.getValue\('edition\_map'\)'. When edition\_index is null/empty, the entire edition\_map \(including its versionMap\) is replaced with an empty object.

</td><td>

1.  Create a Regex normalization rule with:
    -   edition\_index = null \(no edition capture group\)
    -   edition\_map populated with a versionMap.
2.  Create a Discovery model whose display\_name matches the Regex pattern.
3.  Run the 'SAM - Normalize Discovery Models Using Content Rules' job.

 Expected behavior: The edition\_map should be parsed regardless of edition\_index, so that versionMap entries are applied to remap version values.

 Actual behavior: The versionMap isn't applied. The version value is not remapped because edition\_map is discarded when edition\_index is null.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2018394

</td><td>

Regex normalization ignores product license exception rules, as it stamps the product type directly from samp\_sw\_product instead of consulting the exception map

</td><td>

Both setDiscoveryModelNormalizedValues\(\) and findSuggestedValues\(\) used ruleObj.productType directly \(which comes from samp\_sw\_product.product\_type\) bypass product license exception rules. Other normalization paths \(pattern, package map\) already consult these exception rules via NormalizationEngine.\_getProductTypeFromRule\(\).

</td><td>

1.  Create a product in samp\_sw\_product with the product\_type=licensable.
2.  Create a product license exception rule for that product with a specific edition mapped to 'not licensable'.
3.  Create a regex normalization rule pointing to that product.
4.  Create a discovery model whose display\_name matches the Regex pattern with the exception edition.
5.  Run the 'SAM - Normalize Discovery Models Using Content Rules' job.

 Expected behavior: The discovery model's norm\_type should be 'not licensable' \(honoring the Product License Exception Rule\), consistent with how pattern and package map normalization paths behave via \_getProductTypeFromRule\(\).

 Actual behavior: The discovery model's norm\_type is set to 'licensable' \(taken directly from samp\_sw\_product.product\_type\). The same issue affects the suggestions path — findSuggestedValues\(\) also returns the wrong productType, causing incorrect suggested values.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2020394

</td><td>

The 'Apply latest content changes' job fails for Regex normalization rules due to calling a private function as an instance method

</td><td>

SampRegexNormalization RuleContentUpdate Handler.reEvaluate DiscoveryModels\(\) calls this.regexEngine. buildRuleObject\(ruleGr\), but buildRuleObject is a closure-private function inside RegexNormalizationEngine's IIFE — it isn't exposed as an instance method. This causes every content update for Regex rules to crash.

</td><td>

1.  Ensure the Regex normalization feature is active \(com.sn\_itam\_samp plugin\).
2.  Have at least one Regex normalization rule record in the samp\_regex\_ normalization\_rule table.
3.  Trigger the 'Apply latest content changes' scheduled job, or invoke SampRegexNormalization RuleContentUpdate Handler.processRecord\(\) on a Regex rule record.

 See that the job fails with an error: 'Cannot find function buildRuleObject in object \[object Object\]'.

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

Family changes to fetch summary fields from the m2m table

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Archiving

 PRB1988156

</td><td>

Archive reparenting doesn't work with peripherals and large table names

</td><td>

The records for sys\_audit and sys\_journal\_field don't reparent, and an error is found in the logs.

</td><td>

1.  Create a table with sys\_audit and sys\_journal records with a length that is over 60 characters. For example, 'u\_supercalifragilistic expiextralongname\_restore\_destroy\_test'.
2.  Attempt to archive it.

 Notice that the sys\_audit and sys\_journal\_field records don't reparent. Instead, the log shows this error, 'Found in current data management track'.

</td></tr><tr><td>

Table Administration and Data Management

 PRB2025009

</td><td>

Ordering a query by a **Function** field that wraps a translated\_text column returns blank values for that list

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

 Actual behavior: The 'Name Function' column is blank for both rows.

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

UI Actions

 PRB2013168

</td><td>

Support actions in AINPX

</td><td>

This is a product update.

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

 PRB1982868

</td><td>

The pop-up related to the Comment/Work Note web link only displays in the boundary of the 'Compose' tab

</td><td>

The message, 'The URL you entered seems to be an external link. Do you want to add the required http:// prefix' is confined to the 'Compose' section and not overlaying the page. This occurs in the CSM workspace, Service Operations Workspace \(SOW\), and the HR workspace. This issue occurs in Safari browsers, but has been resolved in Chrome browsers.

</td><td>

1.  Open a Safari browser.
2.  Log in to a Xanadu instance.
3.  Open the CSM workspace.
4.  Open any non-closed incident.
5.  Navigate to the **Activity Stream**.
6.  Navigate to the **Compose** section.
7.  Under 'Subject, select the 3 dots \(**...**\) if formatting options are not available.
8.  Select the **Link** button.
9.  In the **URL** field, enter 'servicenow.com'.
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

 Notice the quick action runs into an error: 'Evaluator.evaluateString\(\) problem: java.lang.SecurityException: Illegal access to package\_private script include CMDBGenAICIFormContextualHelp: caller not in scope sn\_cmdb\_gen\_ai: com.glide.script. RhinoEnvironment.checkScriptableAccess \(RhinoEnvironment.java:723\) com.glide.script. ARhinoScope.checkScriptableAccess \(ARhinoScope.java:134\)'. This happens because the visibility script is evaluated in the global scope.

</td></tr><tr><td>

UI Field Administration

 PRB1998819

</td><td>

WWNAglobal utils should be removed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2017755

</td><td>

The text command shortcut behavior is confusing

</td><td>

 

</td><td>

1.  Open the email composer on any incident record in Service Operations Workspace.
2.  Press /r.

Nothing happens.

3.  Press /.

It displays the text commands dropdown.

4.  Press esc.
5.  Press /r.

It activates the response template command.


 The user finds this confusing and would rather that the text commands always have to be selected from the list instead of being triggered directly via the keyboard.

</td></tr><tr><td>

UI Field Administration

 PRB2025633

</td><td>

AI Agent modified fields API returns aiCreated instead of isAiCreated in JSON response

</td><td>

The boolean field is named incorrectly.

</td><td>

1.  Provision an instance with Gen AI installed.
2.  Open any existing record page \(for example, an incident in Ui16\).

Observe the **AI Agent modified** field API response.

3.  Inspect the JSON response body.

 Expected behavior: The boolean field is named 'isAiCreated'.

 Actual behavior: The boolean field is named 'aiCreated'.

</td></tr><tr><td>

UI Form Administration

 PRB1988524

</td><td>

The copy/paste functionality is not working in the 'Email' section of the workspace.

</td><td>

This issue occurs after upgrading to Zurich.

</td><td>

1.  Log in to a Zurich instance.
2.  Open any workspace, such as Service Operations Workspace or HR workspace.
3.  Open any record.
4.  Navigate to the **Compose email** section.
5.  Enter the email addresses.
6.  Select any email address.
7.  Perform Copy \(ctrl+c\) or Cut \(ctrl+x\) on the email address.
8.  Paste it in the 'To' or 'cc' or 'bcc' section.
9.  Notice that the email address is not copied.

 Expected behavior: The user is able to copy and paste.

 Actual behavior: The user is not able to copy and paste.

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

UI Form Administration

 PRB2010217

</td><td>

UI Policy date comparisons are stale after waiting on the page in Workspace

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2013158

</td><td>

Form and client scripting work for Lit components

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2013160

</td><td>

Handle a graphql error for a boolean choice field

</td><td>

This is a product update.

</td><td>

 

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

 PRB1995434

</td><td>

Modeless dialog with dynamic content fails to render repeater-driven lists on subsequent opens

</td><td>

Users experience a broken user interface when reopening modeless dialog windows that contain dynamically loaded content. On second and subsequent opens, repeater-driven lists fail to appear, preventing users from interacting with required dialog data. This impacts workflows that rely on repeatedly opening dialogs and creates a confusing, non-deterministic user experience. The failure is silent and no visible error is shown.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2002772

</td><td>

Preset for the presentational list \(nested inside the record list bundle\) wasn't discovered during pre-population

</td><td>

The list is completely broken.

</td><td>

1.  On a base instance, build a custom UI Builder \(UIB\) page where the record list component is nested deeply under a tabs viewport.
2.  Perform cache.do.
3.  Visit the UIB page.

Observe that the list component is empty and broken. No data is rendered.

4.  Visit the Service Operations Workspace \(SOW\) list page: /now/sow/list.

 Observe that the SOW list page is also broken and empty.

</td></tr><tr><td>

UX Framework

 PRB2018001

</td><td>

A blank page issue on some nodes during upgrade

</td><td>

This issue occurs in Australia instances.

</td><td>

1.  Upgrade the instance.
2.  Navigate to the node.

 Observe that there is a empty page is displayed with a spinning wheel.

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

When a user navigates between two pages that both have IPS surveys configured, the survey triggered on the first page isn't dismissed upon navigation

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

 Observe the following error: 'Safari and older versions of Internet Explorer are unsupported browsers, please switch to a different or newer browser.'

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
5.  Impersonate as admin.
6.  Initiate a chat from the portal or web-client.
7.  Connect to a live agent.
8.  In browser one, accept the chat as the agent.
9.  Send any image as end-user to agent.
10. Refresh the portal at end-user.

 Expected behavior: Nothing happens.

 Actual behavior: The duplicate attachment/image is displayed only in Virtual Agent.

</td></tr><tr><td>

Virtual Agent

 PRB1989524

</td><td>

Consecutive chat interactions from Customer Service Management \(CSM\) portal have anempty 'Account' and 'Contact' field

</td><td>

 

</td><td>

1.  Log in as a contact/contact as a consumer.
2.  Navigate to the CSM Portal.
3.  Open Virtual Agent chat.
4.  Select the **Live Agent Support** topic.
5.  Close the conversation.
6.  Select **Live Agent Support** topic again in the new conversation.
7.  As an admin, open Interaction list\(interaction\_list\).

 The 'Assigned to = Virtual Agent' has the first interaction has **Account** and **Contact** fields filled, but the next interaction records are missing the **Account** and **Contact** fields.

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
3.  While standard or enhanced chat is processing, close the Virtual Agent.

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

 PRB2003812

</td><td>

Sonar test coverage should be 80% for the Data Collector module

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2006240

</td><td>

The Virtual Agent server doesn't process pre-chat surveys for bot 2 bot

</td><td>

Users aren't routed to a live agent in bot to bot conversations. This was due to a misconfiguration where pre-chat survey was enabled and the user wasn't able to provide a response. Interactions aren't assigned to the queue or an agent in Agent Workspace. It was working when the user first upgraded, but recently has stopped.

</td><td>

1.  Start a conversation in crescendo using the ServiceNow Virtual Agent API.
2.  Send a request to transfer to a live agent using endpoint /api/sn\_va\_as\_service/bot/integration.

 Notice that the conversation doesn't get routed to the live agent.

</td></tr><tr><td>

Virtual Agent

 PRB2007255

 [KB3045151](https://hi.service-now.com/kb_view.do?sysparm_article=KB3045151)

</td><td>

There's memory pressure on nodes due to high memory for the cache 'com.glide.cs.qlue. module.coma. MessageBatchingSession'

</td><td>

Users with 2GB nodes may encounter memory issues that can cause the events process jobs to yield.

</td><td>

Run a heap dump.

 Observe that MacMessageBatchingSession or MessageBatchingSession uses over 50 MB of memory.

</td></tr><tr><td>

Virtual Agent

 PRB2012889

</td><td>

vaSystem.getSearchText isn't working with offGlide

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2013847

</td><td>

Create a new scriptable API for endChatSummarization

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

When a topic/agent is run, the sys\_cs\_now\_ assist\_execution doesn't populate.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2017869

</td><td>

A custom navigation URL isn't working

</td><td>

Users expect that custom URL mappings under sys\_cs\_portal\_url\_ mapping\_list should only impact the portal/mobile device for which it was configured. Also, pages opened on Mobile NextWave should be read as iOS/Android, not mweb. However, custom URL mapping configured for Mobile impacts Portals or vice versa, and pages opened on Mobile NextWave are read as mweb.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2018098

</td><td>

AI agents incorrect are displayed on the Virtual Agent's topics list

</td><td>

On Virtual Agent, users see AI Agent in the 'View All Topics' section under the 'Others' category. But none of those agents are marked to be visible on that section.

</td><td>

1.  Open Virtual Agent.
2.  Navigate to the 'View All Topics' section.
3.  Scroll to the 'Others' section.

 See that multiple AI Agents are visible there.

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

 PRB2019099

</td><td>

Starting '\{0\}' sys\_cs\_context\_ profile\_message isn't translated per user session language

</td><td>

The message should be translated using SysMessage. getMessageLang before it's sent.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2020252

</td><td>

The Virtual Agent goes into a loop after selecting the feedback survey

</td><td>

In Zurich, the Now Assist Virtual Agent in enhanced chat intermittently gets stuck in a loop selecting the feedback survey topic.

</td><td>

1.  Open the NAVA bot from the portal.
2.  Ensure that the survey topic is added in fallback.
3.  Search for a query that has no related knowledge articles and triggers the fallback topic \(for example, 'What is quantum physics?'\).

 Observe that after the fallback is triggered, a form link is provided and a feedback message is triggered. After the feedback message is triggered, the Virtual Agent continues to return the same feedback message as the response.

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

 PRB2025311

</td><td>

Add an ai\_greeting type mapping in getContextProfile MessagesNoDomain to support a Premium Chat greeting message feature

</td><td>

The Now Assist Virtual Agent \(VA\) admin UI saves static AI greeting messages as sys\_cs\_context\_profile\_message records with type=ai\_greeting. For these to load correctly, getContextProfile MessagesNoDomain in NowAssistIn VAAdmin ConsoleUtil needs an explicit branch mapping ai\_greeting → aiGreetingMessage. Without this Glide-services change, the greeting message isn't populated for multi-domain instances when the feature ships.

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

1.  Make sure sn\_nowassist\_ va.analytics. persistence\_strategy = 'table'.
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

api/sn\_nowassist\_va /og\_branding\_configs/ \{deploymentId\} doesn't provide the correct response for branding configuration. It's missing a value field and the type is null for the first item.

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

The conversation user for the ZTSD flow is AI L1 Service Desk Specialist, which is the identity type ai\_agent. The cache configuration get\_user\|table:\{table\} \|field:\{field\}\| value:\{value\} explicitly ignores users of type 'ai\_agent'.

</td><td>

Perform a cache fetch call for the cache key 'get\_user\|table:\{table\}\|field:\{field\}\|value:\{value\}' for any user of the identity type 'ai\_agent'.

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

The /esc portal agent chat is configured to only trigger the live agent. However, when the user selects the 'Virtual Agent' icon, it triggers the greetings topic and doesn't go to the live agent. When the user ends the first conversation and creates another conversation, it then goes straight to the live agent. The issue only occurs the first time the user selects the 'Virtual Agent' icon in the session. It also only happens for Now Assist virtual agent sessions.

</td><td>

1.  Enable Now Assist in Virtual Agent.
2.  Configure the agent chat configuration for the /esc portal.
3.  Turn off all the other agent chat configurations, only keeping one active.
4.  Navigate to /esc.
5.  Select the **Virtual Agent** icon.

 Expected behavior: It triggers the live agent support topic.

 Actual behavior: It triggers the greetings topic. However, if you end the conversation and create a conversation, it goes straight to the live agent.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2021136

</td><td>

Selecting the **Stop** button during synthesized results streaming causes an error

</td><td>

This issue occurs when the **Stop** button is selected in the small time interval between the receipt of the last chunk and the full synthesized response.

</td><td>

1.  Navigate to the esc portal.
2.  Select the **Now Assist** chat icon.
3.  Type the utterance: 'Adobe access'.
4.  Wait for the response to be streamed.
5.  Select the **Stop** button immediately after the response is streamed.

 Observe that there's an error.

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

Visibility Content

 PRB2008571

 [KB2946711](https://hi.service-now.com/kb_view.do?sysparm_article=KB2946711)

</td><td>

Sybase Discovery failed due to an issue in the step 8 condition, causing instances to be created in the wrong class

</td><td>

The Sybase Discovery pattern fails during execution, which results in database instances created in the parent table instead of the expected Sybase-specific class. Even after retrieving the instance name in step 7, the Sybase database pattern is failing in step 8.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Visual Task Boards

 PRB1994303

</td><td>

In a Visual Task Board \(VTB\), the 'Select lane' menu displays lane values from all the boards available irrespective of the board selected to move

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Window Manager

 PRB2019525

</td><td>

When the Now Assist panel is activated, the left side navigation is hidden and the margin remains applied, leaving an empty space

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Word Document APIs

 PRB1973625

</td><td>

Support unzipped font size up to 20 MB in Word Doc API

</td><td>

The property com.snc.word\_doc\_api .unzip\_word\_size\_limit\_mb supports only up to 10 MB file size. This is an enhancement request to support up to 20 MB.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB2015160

</td><td>

'Sort by distance' is degraded in Australia

</td><td>

The 'Sort by distance' operation in the FSM Dispatcher Workspace is significantly slower in Australia than Zurich. The transaction response time increased from 2.2 seconds to 8.9 seconds — 6.5 seconds slower.

</td><td>

1.  Log in to an instance with dispatcher0400.
2.  Select the **Dispatcher workspace** button.
3.  Select a task from the left side pane.
4.  Select the **Sort by distance** button.

</td></tr><tr><td>

Work Order Management

 PRB2017308

</td><td>

Flat table records aren't invalidated when location attributes are inserted to Workforce Operations \(WFO\) events

</td><td>

In Australia, when a location attribute \(sn\_shift\_planning \_sched\_attr\) record was inserted into or deleted from a WFO event, the related schedule flat-table records weren't invalidated. As a result, outdated event entries continued to exist on the agent's flat table instead of being re-inserted with the updated sn\_shift\_planning\_ sched\_attr sys\_id. The issue was present in the 'Update schedule flat table' business rule in the Field Service Management \(com.snc.work\_management\) plugin.

</td><td>

1.  Enable WFO.
2.  Insert a location attribute \(sn\_shift\_planning\_sched\_attr\) record to a WFO event.
3.  Navigate to a flat table.

 See the outdated events record still exist for the agent. When sn\_shift\_planning\_sched\_attr record is inserted or deleted, related flat table records should also be invalidated as they have to be inserted with an updated sn\_shift\_planning\_sched\_attr sysID into the table.

</td></tr><tr><td>

Work Order Management

 PRB2023961

</td><td>

The switch 'Enable/disable association of territory resources with demand channels' can be turned on even when FSM shift scheduling is turned off

</td><td>

 

</td><td>

1.  Provision an instance with FSM Territory Planning, Advanced Capacity, and WFO installed.
2.  Activate a territory model.
3.  Navigate to the 'Field Service Configuration Assignment' tab.

 Expected behavior: Enabling/disabling the association of territory resources with demand channels can't be turned on unless the 'Enable FSM shift scheduling' toggle is enabled.

 Actual behavior: The toggle 'Enable/disable association of territory resources with demand channels' can be set to enabled without setting 'Shift Scheduling' to true.

</td></tr><tr><td>

Work Order Management

 PRB2026498

</td><td>

Work order tasks \(WOT\) are unassigned after flexible breaks are updated by Schedule Optimization \(SO\)

</td><td>

When a flexible break is optimized by the SO engine, it inserts/updates records in the sn\_shift\_planning\_agent\_schedule table to update the original break start and end time. This operation is triggering the business rule 'Re-assignment on shift deletion', which causes all of the tasks in the shift to be unassigned, even if they don't overlap with the break event.

</td><td>

1.  Set up a Workforce Optimization \(WFO\) schedule with flexible breaks.
2.  Set up an optimization batch or intraday configuration for the same group/territory.
3.  Run optimization.

 Observe that the tasks are assigned by SO, but then immediately unassigned after the flexible breaks are updated.

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

 PRB2018016

</td><td>

The 'TS Index Stats' job shouldn't check a table that's not indexed

</td><td>

The 'TS Index Stats' job is pulling 45 million records from syslog and caused an out of memory error on the node.

</td><td>

1.  Run the 'TS Index Stats' job.
2.  Turn on the syslog\(collection\) text index attribute in sys\_dictionary.
3.  Create a record in ts\_index\_name for syslog.
4.  In the background, run the new GlideTSIndexStatistician\(\).allStats\(\);.

 Expected behavior: It shouldn't load all records for the table.

 Actual behavior: There's a warning for syslog large table: 'Table handling an extremely large result set'.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 2 Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2-hf-1.md)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/available-versions.md)


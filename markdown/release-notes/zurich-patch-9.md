---
title: Zurich Patch 9
description: The Zurich Patch 9 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-9.html
release: zurich
product: Release Notes
classification: release-notes
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 78
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 9

The Zurich Patch 9 release contains important problem fixes.

-   **Zurich Patch 9 was released on May 5, 2026.**
    -   Build date: 04-30-2026\_1910
    -   Build tag: glide-zurich-07-01-2025\_\_patch9-04-20-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z09.00.xlsx).

## Overview

Zurich Patch 9 includes 292 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-zp9.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Zurich Patch 9 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 9, refer to [KB2956830](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2956830).

## Changes in Zurich Patch 9

-   ****

    The guarded script evaluator enhances instance security by supporting only a restricted scripting language and detecting or rejecting untrusted scripts that use unsupported JavaScript features.

-   ****

    Review the JavaScript APIs that guarded script supports to help you analyze scripts in the Incompatible Guarded Scripts list and either rewrite them or create an exemption for them.

-   ****

    Create zero copy connections and data fabric tables in Workflow Data Fabric Hub after requesting the Zero Copy Connectors app through the Now Support Service Catalog. If it isn't already installed, the app installs Workflow Data Fabric Hub.

-   ****
-   ****

    The script sandbox environment is a restricted execution context in which untrusted, client-generated scripts run on the server using one of two evaluators: the guarded script evaluator or the script sandbox evaluator.

-   ****

    The evaluator:

    The script sandbox evaluator helps prevent executing untrusted scripts on an instance by limiting the APIs available to scripts.

    Scripts that run in the script sandbox evaluator can use features supported by the JavaScript engine and the sandbox environment, except for certain restricted methods. Untrusted scripts are processed by the script sandbox evaluator under the following conditions:

    -   A script has been granted a guarded-script exemption \(manually or automatically\).
    -   When guarded script is in Phase 1: Detection, and a script is sent to the server by an authenticated user.
    For more information about guarded-script exemptions and enforcement phases, see .


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

Database Persistence

 PRB2006319

</td><td>

ACL rules evaluated during twoPassQuery\(\) pull in mostly empty GlideRecords for context

</td><td>

During dot-walks, ACL rules evaluated during twoPassQuery\(\) often pull in mostly empty GlideRecords for context. This happens during script execution/condition evaluations.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB1949832

</td><td>

The 'Physical Table Stats Gatherer' job runs long due to an influx of a query with the hash 943940198

</td><td>

This occurs after the user upgrades to Zurich. Due to the slow query, the job ran more than two days.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2008600

</td><td>

Platform Analytics Experience \(PaE\) tab translations don't work in non-English instances

</td><td>

The tab names should be preserved and not overridden.

</td><td>

1.  Provision an Australia or Zurich instance with a language plugin installed.
2.  Switch the language to the installed one.
3.  Create a dashboard.
4.  Add two new tabs.
5.  Give a name to both.
6.  Save the dashboard.
7.  Switch to English.
8.  Rename both tabs.
9.  Save the dashboard.
10. Switch back to the initial language.

 Expected behavior: The tab names should be preserved and not overridden.

 Actual behavior: The tabs now contain English names instead of the ones for the specific language.

</td></tr><tr><td>

Server-side scripts

 PRB1989147

 [KB2771034](https://hi.service-now.com/kb_view.do?sysparm_article=KB2771034)

</td><td>

Unauthenticated URLs that include invalid URL encoding may redirect to an empty page

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1886667

</td><td>

Korean consonants and vowels are separately returned when the user types into a variable using a keyboard in a portal page

</td><td>

.

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

Activity Stream

 PRB1890722

</td><td>

Attachment details are displayed incorrectly in the workspace activity stream when attaching a duplicate attachment to an email

</td><td>

If an identical attachment is included on an e-mail, the sys\_email\_attachment record reports: Action: Filtered from Target Record and Action Reason: An identical attachment already exists on the target record. Additionally, the attachment is added to the sys\_attachment table with the following document reference: Table Name: sys\_email and Table Sys ID: Email Sys ID. As such, the attachment isn't returned in the activity stream event list. That means that the assumption that all e-mail attachments are also included in the activity stream is false.

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
2.  Navigate to Hardware Asset Workspace.
3.  Open the Hardware Asset Workspace Overview.
4.  Select **Asset requests** under the 'Quick links' section.
5.  Open any requested item.

 Expected behavior: The acronym 'AI' should be localized in the target languages Spanish, Brazilian Portuguese, and French. This should also apply to the backend form of the requested item's 'Detailed Issue' description.

 Actual behavior: Observe that the 'AI' acronym still appears as 'AI' instead of 'IA'.

</td></tr><tr><td>

Activity Stream

 PRB2004286

</td><td>

A user's filter is incorrectly keying the supplemental map with translated keys, leading to an empty activity stream after changing the language

</td><td>

A supplemental map is incorrectly keyed with a translated string. It's also not correctly handling the case where the key in the map doesn't exist, leading to an uncaught exception and the activity stream not loading.

</td><td>

 

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

 PRB2009281

</td><td>

AI Specialist 'reviewed by' subtitle is always shown on journal entries

</td><td>

 

</td><td>

1.  Navigate to any relevant workspace that contains an activity stream.
2.  Open a record that contains a comment or work note posted by an AI Specialist.

 Expected behavior: The 'reviewed by' subtitle isn't displayed on AI Specialist posts.

 Actual behavior: The 'reviewed by' subtitle is displayed on all AI Specialist posts \(for example, 'Work note reviewed by Abel Tuter'\).

</td></tr><tr><td>

Activity Stream

 PRB2009316

</td><td>

Gradient borders are missing for AI Specialist avatars

</td><td>

 

</td><td>

1.  Navigate to any relevant workspace that contains an activity stream.
2.  Open a record that contains a comment or work note that an AI Specialist posted.

 Expected behavior: There should be a gradient border ring on AI Specialist avatars.

 Actual behavior: The gradient border ring is missing from AI Specialist avatars.

</td></tr><tr><td>

Activity Stream

 PRB2009317

</td><td>

GlideActivity methods for supplemental data should be publicly available

</td><td>

A notification should be displayed with the text 'Test Success!'.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2010277

</td><td>

Text is removed when typing fast in Robust Transform Engine \(RTE\) in Service Operations Workspace \(SOW\)

</td><td>

There is an issue with the timing of the post-button render.

</td><td>

1.  Open any instance with RTE turned on \(glide.ui.journal.use\_html=true\).
2.  Navigate to SOW.
3.  Open any incident.
4.  Open DevTools and throttle CPU to 6x slowdown.
5.  Navigate to **Work Notes**.
6.  Begin typing very rapidly.

 Expected behavior: All keystrokes should be recorded in RTE.

 Actual behavior: The cursor backups to a previous spot and users lose text.

</td></tr><tr><td>

Activity Stream

 PRB2011239

</td><td>

Notify Seismic application users when an activity entry has been flagged for review

</td><td>

If the following conditions are true, on a page load, a page level user notification should be displayed indicating that there is a journal entry requiring review: 1. The instance is configured for participation in AI specialist workflow / notification \(sn\_aia.enable\_ai\_workers = true\). 2. 'journalUnderReview' is set to a non-empty string. 3. 'journalUnderReview' is a valid sys\_id that corresponds to a journal entry associated with the current document. 4. The URL doesn't contain a citation.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2012881

</td><td>

Notify UI16 application users when an activity entry has been flagged for review

</td><td>

The page level notification should be displayed: '\[User\] has updated fields and work notes. Please review the work notes and fields for accuracy.' The notification should also contain a link titled 'Review work notes'.

</td><td>

1.  Log in as admin.
2.  To configure the instance for participation in an AI specialist workflow, set the system property sn\_aia.enable\_ai\_workers to true.
3.  Create a user account with the display name = AI Specialist.
4.  Impersonate AI Specialist.
5.  Add a incident record.
6.  Copy the sys\_id for the record \(INCIDENT\_SYS\_ID\).
7.  Add two work notes for the incident record.
8.  End the impersonation \(go back to admin\).
9.  Look up the sys\_id of the first work note \(WORK\_NOTE\_SYS\_ID\) in the sys\_journal\_field table.
10. Copy that sys\_id.
11. Run a background script to flag the work note for review.
12. Impersonate an ITIL user.
13. Open the incident record in UI16.

 Expected behavior: Page level notification is displayed: 'AI Specialist has updated fields and work notes. Please review the work notes and fields for accuracy.' The notification also contains a link titled 'Review work notes'. When this link is selected, configured work note \(WORK\_NOTE\_SYS\_ID\) is highlighted in the activity stream using citation highlight snake animation.

 Actual behavior: No notification is displayed.

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

Agent Chat

 PRB1960915

</td><td>

Live chat messages from agents aren't appearing in the end user UI

</td><td>

The indexedDB connection can be lost if the app background refresh is turned off and the app gets backgrounded/foregrounded. When this issue happens, Seismic code should be robust enough to error out properly without breaking the rendering mechanism.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1989186

</td><td>

TaskUtilsSNC creates millions of sys\_cs\_collab\_chat when Collaborative Chat is not enabled

</td><td>

The sys prop com.glide.cs.collab.enabled is false on the instance, meaning Collaborative Chat is not enabled on the instance. Despite this, there are millions of sys\_cs\_collab\_chat records created.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2006599

</td><td>

Locked out AI agents are also included during Zero Touch Service Desk \(ZTSD\) assignments

</td><td>

Only active agents who aren't locked out should be included for ZTSD assignment.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2010436

</td><td>

Move **Include AI agents** related fields out of the 'Auto-assign handling' section

</td><td>

 

</td><td>

1.  Provision a Zurich instance with the sn\_aia and interaction.awa plugins installed.
2.  Navigate to the awa\_assignment\_rule table.
3.  Open or create a entry.

 Observe that the **Include AI agents** related fields are available in the 'Auto-assign handling' section.

</td></tr><tr><td>

Agent Chat

 PRB2011112

</td><td>

Requesting a live agent doesn't create a work item in the NLU \(Natural Language Understanding\) flow in track/swarm

</td><td>

 

</td><td>

1.  Provision an instance with Agent Chat installed.
2.  Log in as both an agent and a requester.
3.  Make the agent available.
4.  Navigate to Service Portal.
5.  Request a live agent.

 Observe that the conversation ends without a work item sent to the agent.

</td></tr><tr><td>

Agent Inbox

 PRB1998675

</td><td>

Dispatch notifications even when the service channel name is missing to avoid skipping notifications

</td><td>

dispatchNotification previously required serviceChannel.name to be true before playing any notification. If this field was missing \(partial GraphQL result, timing issue, channel configuration gap\), the function returned silently — no audio, no desktop notification, no log entry.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2001449

</td><td>

i18n cache configuration is missing cache invalidation metadata

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2013602

</td><td>

When creating a copy of the L1 AI Service Desk specialist, the minimum roles aren't copied over

</td><td>

When adding it to a team, the newly created AI specialist doesn't get the required roles, which happens because of ACL restrictions.

</td><td>

1.  Navigate to SOW.
2.  Impersonate a service desk manager, i.e. a user with the role sn\_sow\_itsm\_ common.sn\_service\_ desk\_manager.
3.  Make a copy of the AI Service Desk specialist.

 Observe that the default roles needed for the AI worker to perform any action aren't copied over. The user only takes the roles from the assignment group.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2001757

</td><td>

Cachebuster isn't added to page\_bundle request

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2005399

</td><td>

An AI Experience virtual host path conflicts with another path

</td><td>

 

</td><td>

Navigate to the Employee Hub home page.

 Observe a 404 not found error. It should load, but there's no way to configure the AI Experience virtual host site name. It's hard-coded.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2012305

</td><td>

AIUXKit oauth\_entity has the scope\_restriction\_status as 'unrestricted', but it should be 'useraccount' with M2M scope mapping

</td><td>

The oauth\_entity record for 'AIUXKit' has the scope\_restriction\_status set to 'unrestricted'. This should be set to 'useraccount', and a corresponding record in the oauth\_entity\_auth\_scope\_mapping M2M table linking the oauth entity to the 'useraccount' scope should be created. Without this fix, JWT tokens created using this oauth entity may cause session mismatch issues because the scope isn't properly set.

</td><td>

1.  Inspect the oauth\_entity record for 'AIUXKit' in the instance.
2.  Observe that scope\_restriction\_status is set to 'unrestricted'.
3.  Verify that no corresponding 'oauth\_entity\_auth\_scope\_mapping' record exists linking this entity to the 'useraccount' scope.
4.  Use a JWT token created via the AIUXKit oauth entity in a flow that relies on session matching.

Observe session mismatch errors due to the unrestricted scope.


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

/api/now/aiux\_service/sysprops does not enforce an allowlist

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1972570

</td><td>

The display value in 'Location' gives the sysID rather than the country code

</td><td>

The issue occurs in the latest Zurich, Yokohama, and Now Assist instances. sys\_user.country is working but sys\_user.location.country is not.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1991218

</td><td>

Any portal should be able to enable hybrid search

</td><td>

When the user tries to enable hybrid search on global search, enablement is blocked.

</td><td>

Try to enable hybrid search on global search.

 Observe that enablement is blocked.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1999484

</td><td>

KBB \(Knowledge Block\) checks break incremental indexing for some catalog child tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2006426

</td><td>

When a document with an attachment is removed by late binding, the next attachment where the user has access is also removed

</td><td>

When ds\_document\_version parent documents are filtered by an ACL and their children are skipped \(the continue at line 516–518 bypasses the recursive child processing\), the sys\_attachment sparse cursor falls out of sync. It was built assuming every child would be processed in order, but skipped parents leave gaps.

</td><td>

1.  Create 3 KBs with an attachment.
2.  Confirm that the KBs and attachments are relevant to a query \(KB1 is most relevant. KB3 is least relevant but still matches a query\).
3.  Add an ACL to block the second KB but allow the first and third.
4.  Force a late binding KB in ais\_datasource or the 'everything by' property.
5.  Query in a search preview as a user.

 Expected behavior: KB3 should be displayed with an attachment.

 Actual behavior: KB3 is displayed but with no attachment.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2008247

</td><td>

A negative offset isn't handled properly, which causes no results after moving to the next page

</td><td>

 

</td><td>

1.  Change the 'glide.ais.query.search\_operator' property to 'OR'.
2.  Perform a search on Service Portal which returns more than 12 results.
3.  Select the **Next page** arrow button.

 Observe that there's no matches.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2013447

</td><td>

Glide side configurations for context graph

</td><td>

The following Glide-side system properties are required for the Context Graph Reranker feature in AI Search. If these configurations are absent, the reranker doesn't function correctly or may fail silently. Ensure the following 3 system properties exist and are correctly configured: glide.ais.query.context\_ graph\_reranker \_enabled \(default: false\), glide.ais.query. context\_graph\_reranker \_max\_rerank \(default: empty\), glide.ais.query. context\_graph\_reranker \_scalar \(default: empty\). In SearchRequestConverter. toAISObject\(\), when converting an internal search request to an AIS query: If context\_graph\_reranker\_enabled is true and the parameter is not already set via REST params or additional params, it adds contextgraph. reranker.enabled =true to the query. Only when the reranker is enabled, it conditionally passes max\_rerank and scalar values \(if non-empty\) as additional REST parameters to the AIS engine. Without these properties, the Context Graph Reranker cannot be toggled on or configured, and overrides via REST parameters will not work as expected.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1886370

</td><td>

AisHostnameProximityEstimator reads datacenter names from host names as case insensitive, but then compares them as case sensitive

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1887375

</td><td>

'OR' conditions aren't correctly evaluated in Entity View Action Mapper \(EVAM\) lite

</td><td>

In SearchResultTemplateGenerator, there's logic to revert to legacy EVAM template engine if the condition is complex, but it doesn't currently catch 'OR' conditions.

</td><td>

1.  Set active=false to the Service Portal default view configuration.
2.  Search for 'IPV6' in Service Portal.

Observe users get 1 result \(expected\).

3.  Modify the Service Portal 'Knowledge Search Results' view configuration to add 'knowledge\_base is Known Error'.
4.  Search for 'IPV6' in Service Portal.

Observe users still get 1 result \(expected\).

5.  Add an 'OR' condition to the 'Knowledge Search Results' view configuration for 'knowledge\_base is IT'.
6.  Search for 'IPV6' in Service Portal.

Observe users no longer get the result \(not expected\).


</td></tr><tr><td>

AI Search UX

 PRB1981121

</td><td>

Global search isn't working with zoom in/zoom out

</td><td>

Global Search in the Native UI doesn't return results when the filter navigator is pinned and the browser zoom is set to 125% or 150%.

</td><td>

1.  Log in to an instance.
2.  Use the Native UI.
3.  Pin the filter navigator \(left navigation panel\).
4.  Set the browser zoom to 125% or 150%.
5.  Perform a global search for a known existing record.
6.  Observe that the search returns 'No Record Found'.
7.  Change the zoom to 80% and repeat the same search.
8.  Verify that the results appear normally.

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

 PRB1993790

</td><td>

The typeahead search results panel doesn't close and the search state becomes inconsistent after selecting a catalog item

</td><td>

In a portal, the typeahead search widget dropdown list doesn't properly reset or close after selecting a catalog item using a mouse interaction. After performing multiple searches and selecting catalog items from the search dropdown list: 1. The search results panel remains visible instead of closing. 2. Previous search result list remains rendered in the background. 3. In some cases, the search string becomes empty unexpectedly after navigation to the catalog item form. 4. The catalog item form loads, but the search state is inconsistent.

</td><td>

1.  Log in to a Zurich instance as a portal admin.
2.  Navigate to Employee Center: /esc.
3.  Search for 'outlook' or 'email'.
4.  From the typeahead results dropdown list, select the catalog item using the mouse.
5.  When the results load, observe that the previously listed dropdown list/suggested results still display.

 Expected behavior: The dropdown list should close on selection. The search state should reset or behave consistently. No residual search results should remain visible.

 Actual behavior: The search results dropdown list remains visible after selection. The previous search list remains rendered.

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

 PRB2002354

</td><td>

Conversational-agentic catalog results for NextWave should display a chat icon

</td><td>

In a regular search result for regular search terms, users should be able to see the chat icon.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2004210

</td><td>

A Zing component isn't loaded with an error on the console: '\_\_dyImp0\(...\).then is not a function'

</td><td>

Dynamic import fails as the component is already loaded by another module, in which case the dynamic import won't return a promise.

</td><td>

Navigate to an instance with Zing.

 On the home page, notice that the search bar doesn't load and an error appears in the console.

</td></tr><tr><td>

AI Search UX

 PRB2005193

</td><td>

Exact Match, when configured to honor conditions of search sources, should be configurable for a single application and not the entire instance

</td><td>

A system property called glide.search.exact\_ match\_use\_search \_source\_filter enables all applications on the instance with exact match limited to those tables included in a search source and honors the conditions set within them. Users do not expect this feature to be enabled at the instance level, but require it to be enabled at the application level.

</td><td>

Set the system property glide.search.exact\_ match\_use\_search\_ source\_filter to true.Notice how setting this property to true applies to all search applications. Instead, it should be enabled/disabled for a single application.

</td></tr><tr><td>

AI Search UX

 PRB2006200

</td><td>

Synthesized answer loading card status text isn't fully visible in a narrow viewport when non-English locale text exceeds container bounds

</td><td>

When a user performs an AI Search query in a narrow viewport \(reproducible via Chrome Responsive Design View on desktop\) on Service Portal without enhanced chat, and with the session language set to a non-English locale, the synthesized answer loading card clips overlap its content. The loading status text and any action elements within the loading card might overlap together rather than wrapping or expanding the container height. The synthesized answer and the underlying search results continue to function correctly; the issue is limited to the visual presentation of the loading card during the analysis phase. The behavior is triggered by the longer text strings used for loading status messages in non-English locales. For example, the German loading status text 'Ihre Anforderung wird analysiert' \(Analyzing your request\) is significantly longer than the English equivalent, and the loading card container does not wrap to accommodate it in a narrow viewport.

</td><td>

1.  Open an instance with ESC portal and Now Assist in AI Search with the session language set to German.
2.  Open Chrome and navigate to the AI Search page of ESC portal.
3.  Open Chrome Developer Tools and turn on 'Responsive Design' view \(toggle device toolbar\).
4.  Set the viewport to a narrow mobile width.
5.  Confirm that the instance language is set to German.
6.  Enter the search keyword 'übersicht fristen' in the search box.
7.  Submit.
8.  Observe the synthesized answer loading card as it renders during the analysis phase.

 Expected behavior: The synthesized answer loading card displays the full loading status text without overlapping. The card container expands or wraps to accommodate the full text string regardless of locale or viewport width.

 Actual behavior: The synthesized answer loading card overlaps its content. The loading status text is not fully visible. The card does not expand to accommodate the longer German locale status text string in the narrow viewport.

</td></tr><tr><td>

AI Search UX

 PRB2012802

</td><td>

Indexed source types shouldn't be hard-coded in the API

</td><td>

The AISIndexSourceAPI.fetchIndexingState\(\) method only returns for internal type indexed sources. It should include all indexed sources.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2001019

</td><td>

Accept 'group by' selection for all variable types

</td><td>

When comparing to classic reporting, many variable types are not available for selection in the 'group by' component in the Platform Analytics visualizations.

</td><td>

1.  Navigate to Platform Analytics Experience.
2.  Create a dashboard.
3.  Add a donut visualization:
    1.  Datasource: sc\_req\_item
    2.  Group by: variables
    3.  Search for: Sample item
4.  Notice only multi-choice and 'Select box' are available.
5.  Create the same visualization in classic reporting.

 Notice that there's a lot more options available.

</td></tr><tr><td>

Approvals

 PRB2012477

</td><td>

Glide changes to Intelligent Approvals

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Approval with E-signature

 PRB1955867

</td><td>

The **Approval Reason** field should be empty when no reason is provided

</td><td>

The field displays the message 'No approval reason provided' instead of being left empty.

</td><td>

1.  Provision an instance with the 'Approval with E-Signature' plugin installed.
2.  Create a flow that includes the 'Ask for Approval' action operating on a table registered in the E-Signature Registry. \(For example, when an incident is triggered, ask ml.admin for approval.\)
3.  Leave the **Approval Reason** field empty.
4.  Trigger the flow so that an approval record is created.
5.  Approve the record using the appropriate user.
6.  Navigate to the record requiring approval.
7.  Open the approved record from the related lists.
8.  Inspect the activity stream comments.

 Observe that the **Reason** field displays the message 'No approval reason provided' instead of being left empty. This is a mismatch with the read-only **Approval Reason** field.

</td></tr><tr><td>

Attachments to Records

 PRB1954868

</td><td>

The 'Delete' option is visible in the 'Attachment' section in workspace even after restricting the access to delete attachments in the Zurich version

</td><td>

The multi-attachment delete option \(introduced in the Zurich version\) still appears, and it displays the message 'Attachment deleted: The attachment attachment\_name.type has been deleted from this record' even though the attachment isn't actually deleted.

</td><td>

1.  Navigate to any Zurich instance.
2.  Restrict the delete ACLs on the sys\_attachment table.
3.  Turn off the ACLs.
4.  Create a delete ACL on the sys\_attachment table.
5.  Give a role as an admin.
6.  Impersonate a non-admin user.
7.  Navigate to any workspace.
8.  Open a record that has attachments.
9.  Select the attachment.
10. Select the **Delete** option.

 Observe that the attachment isn't deleted but there's a message coming up as deleted.

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

 PRB1964259

</td><td>

When OpenID Connect \(OIDC\) authentication fails, users are redirected to /not\_allowed.do

</td><td>

 

</td><td>

1.  Provision an instance with Engagement Messenger \(EM\) version 5.12.0 installed.
2.  Set up OIDC.
3.  Embed EM on a third-party site.
4.  Try to log in to the site.

 Observe that authentication fails \(as expected\) and the user is redirected to \[servicenow\_instance\_url\]/not\_allowed.do.

</td></tr><tr><td>

Authentication

 PRB2013580

</td><td>

The Kaa-JWT custom URL audience support is broken

</td><td>

This field is auto-populated based on the failed test result. Any user that is inputted before saving is not retained. An error message occurs, 'Error Message = Execution = platform-authentication-mutual-auth-test@2026-04-13 02:05:52 Glide Version = 28.0.0.596.'

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2012205

</td><td>

Verify the Automated Test Framework \(ATF\) environment in business applications \(BA\) for Glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2012206

</td><td>

Capture server logs along with client logs and turn on grep for both

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2012207

</td><td>

Track initiator for Automated Test Framework \(ATF\) test executions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2012208

</td><td>

Support running a single Automated Test Framework \(ATF\) test \(vs. a suite\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2004389

</td><td>

The TableChoiceList cache is susceptible to corruption

</td><td>

Cached TableChoiceList items that are generated and returned by the ChoiceListGenerator can be mutated with the removeNone API. This leads to cache corruption when a user of TableChoiceList modifies the object.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1771020

</td><td>

The **Questions** field does not properly scale in the UI for medium and large layouts in the between editor

</td><td>

The **Questions** field scales properly in the UI width for the size small, but is crunched when in the sizes medium and large.

</td><td>

1.  Create a predicate builder in the UI Builder, or leverage one of the demo pages.
2.  Select questions and select values that have a between editor. For example, use 'Question' and 'Ask a Question' and select **Short description** then **Between**.
3.  Scale the UI width in small, medium, and large layouts.

 Notice that the layout is crunched only with the 'Between' operator.

</td></tr><tr><td>

Condition Builder

 PRB1899557

</td><td>

Dot-walked **Tags** fields in Platform Analytics revert back to the original table

</td><td>

Dot-walked tags in the dashboard condition builder don't display the reference field. For example, they display 'Tags' or 'Caller Tags'.

</td><td>

 

</td></tr><tr><td>

Connections and Credentials

 PRB1980233

</td><td>

Refreshing invalid tokens via MID Server fails when using threshold-based token refresh strategy

</td><td>

There are errors with NumberFormatException in the MID Server's agent logs.

</td><td>

1.  Make sure the MID Server is validated.
2.  Setup OAuth 2.0 on an instance.
3.  Fetch the token using the **Get OAuth Token** UI action.

Observe the MID Server's agent logs. There shouldn't be any error.

4.  Manually expire the token.

 Observe that there are errors with NumberFormatException in the MID Server's agent logs.

</td></tr><tr><td>

Connections and Credentials

 PRB2015199

</td><td>

An initiator URL isn't returned when the AT has expired and the record is present in oauth\_credential\_list

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Content Analytics

 PRB2002450

</td><td>

JavaScript sandbox replacement for app-content-automation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Content Experiences

 PRB2002443

</td><td>

JavaScript sandbox replacement of app-content-publishing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Content Governance

 PRB2002459

</td><td>

JavaScript sandbox replacement for app-content-governance

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Contextual Search

 PRB2010418

</td><td>

An admin user isn't able to add more additional resources to the search context \(cxs\_res\_context\_config\) table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB1967302

</td><td>

Inactive CSM knowledge bases were reactivated unexpectedly during the upgrade of an instance to Zurich

</td><td>

The user had inactivated CSM knowledge bases such as 'Consumer Service' and 'Customer Service', but noticed that the inactive CSM knowledge bases were reactivated during the upgrade of the instance to Zurich.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1983237

</td><td>

Multiple filters execution doesn't use the 'AND' operator as expected

</td><td>

When certain filters are called together, they should return empty results, but they don't.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1985999

</td><td>

'Add Sort' doesn't work as expected

</td><td>

The records aren't sorted. Queries like 'Give me name of user' or 'Give me email ids of users' work as expected, but if one more tag with any other filter is added, then those queries stop working as well.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1991710

</td><td>

In DirectSQL, the alias in ORDER BY isn't supported

</td><td>

This error limits significantly the use cases that the API can support, specifically around function fields/bucketing.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1995482

</td><td>

Filters aren't applied on some cyphers

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1910342

</td><td>

Handing RR candidates present in glide.db.properties

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Dictionaries

 PRB2008800

</td><td>

Support locale aware text searching sensitive columns and provide toggles to turn on/off UI and background transactions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1994994

</td><td>

'Add OR Clause' filter1 doesn't work as expected with 'filter2'

</td><td>

The filter returns records for 'A AND \(B OR C\)'. Instead, it should return records for 'A AND B OR C'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1999440

</td><td>

The before-query rule glide list conditions aren't resolved correctly when the field only exists on partition

</td><td>

An error is thrown, such as 'ERROR: column \_\_src140\_cmdb0.u\_access\_groups does not exist'. This happens with DBSqlParser/ForCypher.

</td><td>

1.  Create a glide\_list **access\_groups** field on cmdb\_ci.
2.  Verify that it is on the partition; if not, migrate it.
3.  Create a before-query business rule on cmdb\_ci\_server.
4.  Add an encoded query on glide list that uses the dynamic filter option 'one of my groups': 'current.addEncodedQuery \('access\_groupsDYNAMIC &lt;sys\_id\_for\_dynamic\_ filter\_option\_record&gt;'\);'.
5.  Execute DBSqlParser query: 'select access\_group from cmdb\_ci\_server'.

 Observe that an error is thrown, such as 'ERROR: column \_\_src140\_cmdb0.u\_access\_groups does not exist'. It should use the partition instead of the root.

</td></tr><tr><td>

Database Persistence - Graph

 PRB2011934

</td><td>

GraphQueryExecutor is returning an error

</td><td>

This is observed only when a filter is used when executing GraphQueryExecutor: 'FAILED: com.glide.db.DBGraphApiException: Error executing cypher: FAILED TRYING TO EXECUTE ON CONNECTION glide.6...'.

</td><td>

 

</td></tr><tr><td>

Database Views

 PRB1981902

</td><td>

The Raptor DB view has a mixed case prefix and a '.' combination errors out

</td><td>

 

</td><td>

1.  Create a DB view between task\_sla and incident, and DB view table records with a prefix with a mixed case \(for example, the prefix 'inC' for incident\).
2.  Have the 'where' clause as 'task\_sla.task = inC.sys\_id'.

 Notice that the execution errors out.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB2002718

</td><td>

Handle the entitlement check of the new ZCC App

</td><td>

The new ZCC app \(sn\_zcc\_primary / sn\_data\_fabric\_zcc\) is not correctly handling the plugin ID after the ZCC app split.

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

 PRB1995608

</td><td>

The 'Attachment' table size is not shown, or is shown incorrectly, in the top 10 largest tables

</td><td>

The 'Attachment' tables are not showing in the top 10 table grid, even if it has large size. The sys\_attachment\_doc stores attachments in binaries, which can be larger in size, but the size will be reported under the sys\_attachment group. Both sys\_attachment and sys\_attachment\_doc are reported under the sys\_attachment table.

</td><td>

 

</td></tr><tr><td>

Delegated Development and Deployment

 PRB1992821

</td><td>

Impact handling of the Scripting Governance on/off switch

</td><td>

The feature may break when the switch is turned on or off.

</td><td>

1.  Check the ACL and Java code for usage of the snc\_required\_script\_writer\_permission role and conditional script writer group.
2.  Turn the switch on or off.

 Observe that the feature may break.

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

 PRB2006752

</td><td>

Incorrect handling of quoted table aliases in DirectSQL

</td><td>

SELECT 'alias'.'bar' from 'foo' 'alias' fails because some unquoting logic in getColumnTable is missing.

</td><td>

 

</td></tr><tr><td>

DirectSQL

 PRB2006863

</td><td>

There's an error in 'LIKE' expression processing when an expression is missing an ASTNode

</td><td>

While generally JSQLParser should have an ASTNode for every expression, there's a case in a query where that's not true. The IHS of the expression is irregular.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1857955

</td><td>

Discovery jobs on Mutual Auth MID servers have a big increase in duration

</td><td>

Running Discovery using the mTLS MID Server can be a lot slower than using the Basic Auth MID Server.

</td><td>

1.  Configure mTLS for MID Server.
2.  For MID Server certificates, use one that is privately signed with a private OCSP.
3.  Run a Discovery schedule on a large subnet.
4.  Compare the Discovery run time on this schedule when using Basic Auth MID vs mTLS MID.
5.  Take thread dumps and verify that mTLS MID Server threads are competing for monitor entries in StandardCredentialsProvider.

</td></tr><tr><td>

Discovery

 PRB1935593

</td><td>

Get pattern temporary variables and add it to allowlist temporary variables

</td><td>

For the patterns allowlist, users may need temporary variables to generate the content. After the pattern executes, it can fetch the temporary variables and add them to the allowlist temporary variables table. When the allowlist is generated, this content is used to replace the temporary variables with the actual value.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1953520

 [KB2718488](https://hi.service-now.com/kb_view.do?sysparm_article=KB2718488)

</td><td>

ecc\_queue input records are stuck in IP jail, causing status cancellation

</td><td>

IPs are placed in a jail if it is suspected that multiple IPs on a schedule belong to the same device. IPs are supposed to be released from jail when the discovery of the device is complete. When this occurs, the IPs are never released from jail.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1972668

</td><td>

Systems Manager \(SSM\) starved all MID threads

</td><td>

SSM starved all MID threads on one user's MID Server, resulting in the MID becoming unusable due to all of the threads being stuck. All the threads are waiting on join\(\) for the completion of a REST API call. The user was trying to discover 300 Linux Server machines.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1988150

 [KB2833085](https://hi.service-now.com/kb_view.do?sysparm_article=KB2833085)

</td><td>

The IP duplicate/jail mechanism interferes with the new counting mechanism

</td><td>

Discovery is completed prematurely when using the new counting jobs. discovery\_probes\_tracker displays records as 'In Progress' for that status, which are stopped from being updated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB2003122

 [KB2896586](https://hi.service-now.com/kb_view.do?sysparm_article=KB2896586)

</td><td>

The Amazon Web Services \(AWS\) resource inventory box pattern stopped launching after Zurich for a non-US date format

</td><td>

It has a display value that is different from the instance.

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

 PRB2012126

</td><td>

The Applicative Credentials call is removed from AWSPowershellProvider

</td><td>

When the user runs a Systems Manager \(SSM\) Discovery on pattern that would use applicative credentials, the applicative credentials aren't being used as expected.

</td><td>

 

</td></tr><tr><td>

Document Management Services

 PRB2012474

</td><td>

Document led AI approvals for some experiences

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Dynamic Translation for Agent Chat

 PRB1989609

</td><td>

When an instance has Now Assist installed, Dynamic Translation for Agent Chat \(DTAC\) doesn't honor the Dynamic Translation \(DT\) setting in Conversational Interfaces

</td><td>

 

</td><td>

1.  Provision an instance with Virtual Agent \(VA\) agent chat installed.
2.  Verify that DT is set up with a provider.
3.  Verify that Now Assist VA is installed.

 DTAC \(in either direction\) only displays the globe icon or is honored when DT in Now Assist Admin Console is turned on for that language.

</td></tr><tr><td>

Email Notifications

 PRB1997659

</td><td>

There's duplicate recipients in email notifications in HR Records

</td><td>

When navigating to the workspace and accessing any HR record, under the 'Emails' related tab, users observe that the notification displays duplicate recipients for the same email.

</td><td>

1.  Configure the 'Email' related tab on the Workspace UI Builder view of sn\_hr\_core\_case\_workforce\_admin.
2.  Navigate to the HR Agent Workspace.
3.  Open any HR record by impersonating an HR Admin.
4.  Send an email using **Compose Email**.
5.  Select a user who has two user profiles \(under To:\) \(one active and one inactive\).
6.  Navigate to the 'Emails' related tab.
7.  Open any email record.
8.  Observe that duplicate recipients are displayed in the notification.

 Expected behavior: Each recipient should be displayed only once in the notification, without any duplication.

 Actual behavior: Duplicate recipients are displayed in the notification for the same email under the 'Emails' related tab.

</td></tr><tr><td>

Embedded Help

 PRB1912461

 [KB2774125](https://hi.service-now.com/kb_view.do?sysparm_article=KB2774125)

</td><td>

Default values for properties in an instance must change due to the docs' site URL change

</td><td>

Due to a change in website vendors and their inherent URL structuring, the URLs generated by the in-product help function are broken. Some system properties must be changed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Embedded Help

 PRB2008561

</td><td>

Update the list of allowed domains

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Employee Relations Case Management

 PRB2012556

</td><td>

Users can create more than one active Performance Improvement Plan \(PIP\) case for the same subject person

</td><td>

 

</td><td>

1.  Create an employee case for any user with the HR service as PIP.
2.  Move the case to the 'ready' state.
3.  Create another case with same service and try to submit it.

 Expected behavior: The case shouldn't be created and an error should be thrown.

 Actual behavior: It gets submitted and a new case is created.

</td></tr><tr><td>

Event Management

 PRB1902287

</td><td>

Users can't uninstall sn\_em\_ai\_overview and sn\_em\_ai\_action because they're part of core-ui-components/'Core UI Components'/sn\_core\_ui\_ponents

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1930730

</td><td>

The graph reuse mechanism in CMDB grouping saves graphs that can contain CIs of more than 4 hops distance

</td><td>

 

</td><td>

1.  Create topology.
2.  Stop the 'Grouping' job.
3.  Send alerts on CI1 and CI8.
4.  Run the 'Grouping' job.

Observe that in em\_ci\_graph\_reuse, the graph of CI1 also contains CI6, CI7, Ci12, etc.

5.  Close the group.
6.  Send alert on CI6.
7.  Run the 'Grouping' job.

Observe that the alert is added to the staging table but no group is created.

8.  Send alert on CI8.
9.  Run the 'Grouping' job.

 Observe that CI8 and CI6 create a CMDB group. However, alerts should not be grouped.

</td></tr><tr><td>

Event Management

 PRB1994838

</td><td>

The EIF Listener **Source** field isn't correctly set for incoming events, and the extParam variable is inaccessible in JavaScript

</td><td>

After setting up an EIF listener, there's an issue with the **Source** field in the incoming events. Instead of displaying the EIF listener's name, the **Source** field shows either host names or IP addresses. This causes problems because users are unable to create accurate event rules. The reason is that the host names change frequently, and IP addresses can also vary over time. As a result, the user can't easily filter or group the events based on the listener's name, which is critical for event management and rule creation. In summary, the inconsistency in the **Source** field makes it difficult for the user to effectively manage their events, as the changing nature of host names and IP addresses creates complications when setting up filters and event rules.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB2006672

</td><td>

Service Analytics group alerts using RCA/Alert Aggregation can get stuck due to the usage of parallelStream\(\)

</td><td>

There's a stuck thread due to AlertStreamClassifierGroupStats.updateStats. Only a node restart frees up the thread.

</td><td>

1.  Open a Zurich instance.
2.  Run Service Analytics group alerts using RCA/Alert Aggregation.

 Observe that it can get stuck under concurrent load.

</td></tr><tr><td>

Event Management

 PRB2008110

</td><td>

MID Server isn't processing V1 traps

</td><td>

Users are sending both SNMP v1 and SNMP v2 traps from a target device. The SNMP v2 traps are consistently received and processed, while SNMP v1 traps are received with an empty node.

</td><td>

1.  Send a SNMP V1 trap.
2.  Navigate to the em\_event table.

 See that there are no events with a node.

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

 PRB1988355

</td><td>

The base instance Unreferenced Record Cleaner rules on the 'sys\_flow\_\*' tables have settings that can cause data loss

</td><td>

The rules have the following settings which could cause orphan records in other tables within the instance: 'Exclude archive: Checked/True Cascade delete: Unchecked/false', 'Clean audits: Unchecked/false', and 'Clean journals: Unchecked/false'.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2014479

</td><td>

Add the roles 'taas writer' and 'taas reader' with API access only, and not with table ownership

</td><td>

Adding the role trigger\_designer directly to policy\_manager was evaluated and ruled out, as the 'policy manager' role should not have access to trigger the 'designer' role.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2012618

</td><td>

Publish flows and actions scriptable API failure

</td><td>

The existing 'sn\_fd.FlowAPI.publish\(sysId\)' fails with the following error: 'Could not publish flow as Action Instance: 'name' is not published'. This happens when a flow contains action instances that point at draft/unpublished action type references. The UI endpoint \(/api/now/processflow/flow/\{sysId\}/snapshot\) works fine for the same flows.

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1940425

</td><td>

Users are unable to install the Security Incident Response app due to an exception

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Hardware Asset Management

 PRB2011466

</td><td>

Failures in app-ham-atf-test and app-ham-eam-atf-test ITs

</td><td>

The reason for their failure is that they do some date arithmetics using multiple statements and variables, which are not allowed in the stricter execution model.

</td><td>

 

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1979839

</td><td>

EventHubs DI automatically specifies servicebus.windows.net as the domain name

</td><td>

 

</td><td>

Set up an Azure Hubs data input.

 Observe that within the 'setNamespaceName' method, the FQDN is set to end in servicebus.windows.net.

</td></tr><tr><td>

Horizon Avatar Component

 PRB2010763

</td><td>

The gradient border is missing for AI Specialist avatars in the activity stream for Seismic interfaces

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Horizon Image Component

 PRB1910414

</td><td>

The 'Image component' configuration panel is missing the **Upload** button and flow in the Platform Analytics dashboard

</td><td>

 

</td><td>

1.  Add an image component to the Platform Analytics dashboard.
2.  Select **Configure**.
3.  Look for a method to upload an image in the configuration panel.

</td></tr><tr><td>

HR Service Delivery

 PRB2004808

 [KB2950289](https://hi.service-now.com/kb_view.do?sysparm_article=KB2950289)

</td><td>

checkForActiveActivitySets\(\) doesn't treat skipped dependencies as complete in combination and trigger, and there's a permanent journey stall after a Zurich upgrade

</td><td>

After refactoring checkForActiveActivitySets\(\) in hr\_ActivitySetTrigger from workflow\_context.state to the activity set context state \(Yokohama+\), the method only checks state !== 'finished' and doesn't treat state = 'skipped' as a satisfied dependency. This causes combination and triggers with audience-filtered \(skipped\) dependencies to permanently stall; the AND condition can never be satisfied because skipped sets are treated as incomplete. This is an inconsistency within the same script include.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery

 PRB2007007

</td><td>

The **Copy to Interview Summary** button isn't visible on Employee Relations \(ER\) Interview Summarization

</td><td>

 

</td><td>

1.  Log in to any Zurich instance.
2.  Activate the ER Interview Summarization Skill.
3.  Open any ER Interview.
4.  Select **Summarize**.

 Observe that the '**Copy to Interview Summary**' button isn't visible after the summary is generated.

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB2000833

</td><td>

Integration metering tables are not synced with the Content Data Service \(CDS\) instance

</td><td>

In Zurich, the intergration metering tables, such as sys\_protected\_data\_ telemetry\_inclusion and sys\_integration\_ metering\_resource\_ exclusion, are not connected to the CDS server for regular updates to the records in the tables. Instead, they must be manually updated by an admin user or a user with elevated privileges. When the Zurich instance is not connected to the CDS instance, no jobs exist in the cds\_client\_schedule with the name 'Integration Metering Protected Table' and 'Integration Metering Resource Exclusion.'

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1994487

</td><td>

There's log message flooding: 'java.net.UnknownHostException'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integrated Email Client

 PRB1998008

</td><td>

Pre-send email client side validation checks

</td><td>

There have been multiple feature requests related to email handling within the Seismic client, including redaction of sensitive information and support for sensitivity labels before sending emails.

</td><td>

 

</td></tr><tr><td>

Interactive Filters

 PRB1996683

</td><td>

Support of dependent fields in cascading filters for both reference and choice type-fields

</td><td>

When using choice fields \(not reference/M2M fields\) as cascading filters in a Platform Analytics workspace, selecting a value in a parent filter doesn't narrow down the available values in child filters.

</td><td>

 

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

 PRB1950812

</td><td>

The SEK rekey job fails if the data is double-encrypted

</td><td>

 

</td><td>

1.  Enable glide.skip\_ storage\_encryption \_for\_kmf\_encrypted to false, which makes the data double-encrypted \(KMF+SEK\).
2.  Insert records for the pwd2 columns.

 Expected behavior: The SEK rekey job processes all records, including the KMF + SEK encrypted records.

 Actual behavior: The SEK rekey job fails because the data is double-encrypted.

</td></tr><tr><td>

Knowledge Blocks

 PRB2000541

</td><td>

There are formatting issues in the KB article view compared to the 'Details' tab view

</td><td>

There are differences in the formatting of the KB article between the 'Details' tab and the 'View article' view.

</td><td>

1.  Open Compliance Workspace.
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

Knowledge Graph

 PRB1992934

 [KB2800544](https://hi.service-now.com/kb_view.do?sysparm_article=KB2800544)

</td><td>

knowledge-graph has two screens with circular dependencies

</td><td>

UI Builder \(UIB\) has login and performance issues due to erroneous creation of uxf records. The root cause has been identified due to the circular dependencies between the parent and child screen records part of same screen collection, causing the UIB duplicate variant logic to run endlessly.

</td><td>

Refer to the listed KB article for details.

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

 PRB1988136

</td><td>

Users can associate the same article as a related article from kb\_knowledge

</td><td>

Add an 'abort' action business rule when the related article matches the knowledge article on the kb\_2\_kb table.

</td><td>

1.  Open an published KB article.
2.  Navigate to the related list.
3.  Find the 'Related articles' tab.
4.  Select the **Edit** button.
5.  Add another KB article as a related list.

This works as expected.


 Observe that from the related list 'mapping record' achieved on step 4, users can edit the mapping record to and add the same record as the related article.

</td></tr><tr><td>

Knowledge Management

 PRB1994772

</td><td>

Navigating to 'Create Knowledge' displays the interceptor page

</td><td>

This occurs when the KCS plugin is enabled and the CSM table map is turned off.

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

 PRB2005195

</td><td>

The **KM Import Article conversion** utility should be exposed as a callable API for external consumption by the GRC/IRM policy flow

</td><td>

The **KM Import Article** feature uses Apache Tika and Apache POI libraries for DOCX-to-HTML conversion and produces flexible, translation-safe HTML output. On the other hand, the GRC policy flow's current GroupDocs-based conversion, which applies static absolute positioning. To resolve the translation formatting issue in GRC's policy flow, the KM conversion utility needs to be exposed as a standalone API that GRC/IRM can consume directly--without requiring an existing Knowledge Article upfront and without deleting the source attachment document during processing.

</td><td>

1.  Navigate to **Knowledge Management** &gt; **Import Article**.
2.  Import a Word document.
3.  Open the created Knowledge Article.
4.  View the source HTML.

 Observe that the output contains flexible/relative styling and there's no static absolute positioning. Compare against a Knowledge Article created via the GRC/IRM policy flow and note the static positioning difference

</td></tr><tr><td>

Knowledge Management

 PRB2014078

</td><td>

Turn on the Apriel 2.0 model and set the new 3P model as the default

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

KPI Details

 PRB1997302

</td><td>

Dates are unlocalized in French in now-date-time-input

</td><td>

 

</td><td>

1.  Provision a Zurich instance with the French language pack installed.
2.  Navigate to **Workspaces** &gt; **CMDB Workspace**.
3.  Change the session language to French.
4.  Select **Visualization** under 'Nouveaux CI'.

 Observe that the dates are in English in the now-date-time-input section.

</td></tr><tr><td>

List Administration

 PRB1963950

</td><td>

There's an undefined table name when opening a record in the task table list after a live update

</td><td>

When a new record is created in Service Operations Workspace \(SOW\) that differs in type from the last record in the custom 'Tasks' list, opening the newly created after live updates displays the message, 'The page you are looking for could not be found.' In the URL, the table parameter appears as 'undefined'. In the CSM/FSM Configurable workspace, the table name is reflected properly, but shows 'No record found'.

</td><td>

1.  Ensure that the property 'glide.lists.live\_list\_enabled' is set to 'true' on the instance for live updates.
2.  Navigate to **SOW**.
3.  Open the Custom List, which is created on the 'Task' table.
4.  Sort the list by 'Created \(Z to A\)'.
5.  Take note of the last record.
6.  Create a record with different type than the last record. Verify that the filter criteria is satisfied.
7.  Return to the list after creating the new record.

Notice that the new record will appear without refreshing the list for the live update.

8.  Open the record.

Notice that the message, 'The page you are looking for could not be found' appears, and the table name in the URL will be 'undefined'.

9.  Refresh the list.
10. Open the record again.

 Notice that it opens correctly.

</td></tr><tr><td>

List Administration

 PRB1967492

</td><td>

An export fails when the filter is too long in Service Operations Workspace

</td><td>

 

</td><td>

1.  Open **SOW** &gt; **Incident** &gt; **All**.
2.  Add the following filter: 'Short description contains \{5000+ character random string\}'.
3.  Select **Export**.

 Observe that the export fails.

</td></tr><tr><td>

List Administration

 PRB1989840

</td><td>

There's unintended creation of temporary list copies when refreshing a default list via address bar

</td><td>

When a user refreshes a default list by selecting the browser address bar and pressing **Enter**, the system creates a new temporary copy of the list and stores it under **My Lists** &gt; **Opened by link**. When the page reloads, that view is opened. This happens without any explicit user action or intent to create or save a new list, and the newly created list is not shared with anyone by default. This behavior creates large volumes of unnecessary list views, leads to user confusion, and pollutes My Lists governance and storage with artifacts.

</td><td>

1.  Open any default list in the workspace.
2.  Select the browser address bar \(don't modify the URL\).
3.  Press **Enter** to reload/refresh the page.

Observe that once the page reloads, it automatically navigates to **My Lists** &gt; **Opened by link**.


 Expected behavior: Refreshing a default list via the browser address bar doesn't create a list artifact.

 Actual behavior: A new temporary copy of the default list is automatically created. The list appears in **My Lists** &gt; **Opened by link**, even though the user never requested a copy. The list is not shared with anyone by default.

</td></tr><tr><td>

List Administration

 PRB1999574

</td><td>

The user has no information about who shared a list with them

</td><td>

 

</td><td>

1.  Open CSM/FSM configuration workspace.
2.  Navigate to the List page as an admin user.
3.  Create a few lists in the 'My Lists' tab.
4.  Share one list with another user, like Fred Luddy.
5.  Impersonate Fred Luddy.

Observe the shared list in the 'Shared with me' section inside the My List tab.


 Expected behavior: There is some info or indication who shared the list.

 Actual behavior: The Fred Luddy user has no information regarding who shared this list.

</td></tr><tr><td>

List Administration

 PRB1999583

</td><td>

The user can't re-order the lists 'Shared with me' lists or 'Opened by Link' to keep the important lists at the top and move less important lists to the bottom

</td><td>

Lists can't be re-ordered in the 'Shared with me' section in the 'My List' tab.

</td><td>

1.  Open the CSM/FSM Configuration workspace.
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

 PRB2009056

</td><td>

The **Back** button after grouping isn't working

</td><td>

 

</td><td>

1.  Open any record list in a Zurich instance.
2.  Perform grouping on any field.
3.  Select the **Show all** group header action.
4.  Select the **Back** button.

 Observe a JS exception in the console, preventing the **Back** button action.

</td></tr><tr><td>

MetricBase

 PRB1983655

</td><td>

Clotho XMLStats reports 'ONLINE' even when Clotho HA pair isn't replicating

</td><td>

 

</td><td>

1.  Set up a Zurich+ Glide instance with a pair of Clothos in a single-sharded setup.
2.  Turn off replication between the Clothos.
3.  Confirm that the HTTP GET request to /xmlstats.do?include=clotho.

 Observe 'ONLINE'.

</td></tr><tr><td>

MID Server

 PRB2012665

 [KB2953193](https://hi.service-now.com/kb_view.do?sysparm_article=KB2953193)

</td><td>

MID Server upgrades fail because the mid.max.extract .file.size property default is too low

</td><td>

The MID Server property mid.max.extract .file.size property default of 500MB is too low for MID Server upgrades. Upgrades fail at the download/extract stage with the following errors, after the mid-core zip file has been successfully downloaded: '...Exceeds the maximum size \(500000000\). Unable to download package The size of uncompressed files is too big or too many entries in the zip file'. This fails before the MID Server is shut down, avoiding outages, but causes repeated failed upgrades, and the risks of running with an instance vs MID Server incompatibility, that generally has been known to break some features and cause data loss.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Experience for Field Service Management \(Glide Family\)

 PRB2007516

</td><td>

The 'My Schedule' calendar screen causes memory issues when it is enabled in offline in Mobile

</td><td>

The memory issues occur in offline because there is a record created for each event every day.

</td><td>

1.  Enable the 'My schedule' calendar screen in offline.
2.  Enter a repeating personal event for an agent.
3.  Log in as an agent into the Mobile app.
4.  Attempt to download the cache.

 Notice that the instance is stuck and the nodes goes down.

</td></tr><tr><td>

Mobile Platform

 PRB1989348

</td><td>

Filtering with a date range doesn't work in offline

</td><td>

All the tasks are still displayed after applying the filter.

</td><td>

1.  In any instance, activate the Field Service Management Demo plugin.
2.  As admin, double check that the list screen 'My tasks' has the default filter.
3.  Sign in as a user from the Agent app.
4.  Edit a task or pick a task that has an expected start date that is easy to filter.
5.  Select **My tasks** &gt; **See all**.
6.  Check that online filtering on 'Expected start' works correctly and one task is picked.
7.  Download offline.
8.  Go offline.
9.  Perform the same filtering in offline mode.

 Expected behavior: One task is picked and displayed after filtering on 'Expected start'.

 Actual behavior: All tasks are displayed after applying the filter.

</td></tr><tr><td>

Mobile Platform

 PRB2006346

</td><td>

The offline V2 sync API returns cumulative table snapshots in each execution result

</td><td>

This issue has been present since Yokohama or earlier and affects the Mobile Agent during offline-to-online sync. When a user performs multiple record edits in offline mode and then reconnects, the sync API processes each queued action and generates a RefreshedDocument per execution result. Due to the cumulative snapshot behavior, each execution result incorrectly includes the data of all previously synced records — not just the one modified in that action. This causes the response payload to grow at an N² rate: N offline edits produce N² total records across all execution results. The impact is significant. Users who perform hundreds of edits in offline mode can experience sync payloads exceeding 100MB+, leading to severe performance degradation, potential sync failures, and a poor user experience at the moment of reconnection.

</td><td>

1.  Provision an instance with Field Service Management with demo data installed.
2.  Log in to the agent app with a field agent user.
3.  Navigate to the offline settings.
4.  Download the offline cache.
5.  Go offline.
6.  Open a work order task form screen and make an edit.
7.  Open a separate work order task and make an edit.
8.  Navigate to settings.
9.  Sync online.

 Expected behavior: In the offline synchronize response, the **Document** &gt; **Data** &gt; **Tables** for each execution result should only contain the record that was edited.

 Actual behavior: The **Document** &gt; **Data** for each execution result contains the data for both records in each execution result.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2003211

</td><td>

/api/now/ui/polaris/menu is slow to build the cache on login

</td><td>

1000s of each of these queries are run to retrieve user preferences and screen accessibilities. It should be able to retrieve all of most of these items in 1 query.

</td><td>

 

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
2.  Select any feedback thumbs up/down icon immediately.
3.  Observe that feedback is successfully stored in the Gen AI log table.
4.  Unselect submitted feedback or submit different feedback.

 Expected behavior: Feedback should be updated in the Gen AI log table.

 Actual behavior: Feedback isn't updated in Gen AI log table.

</td></tr><tr><td>

On-Call Scheduling

 PRB1976318

</td><td>

Duplicate incorrect records on the 'v\_st\_on\_call\_shifts \_and\_coverages\_my\_team' table for an on-call group

</td><td>

The issue is that it's rounding off 23:59 of the previous day as 00:00 of the current day, so there's an extra entry for 00:00 to 00:00.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1982308

</td><td>

On-call message number records aren't deleted when a user responds

</td><td>

On‑call message records are expected to be removed after acknowledgment. But this isn't happening, and they aren't deleted even after the user responds.

</td><td>

1.  Create an on-call incident.
2.  Have the user respond to that incident.

 See that records are created in on-call messages and in the 'Notify' table. But when the user responds, they aren't deleted.

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

 PRB2013928

</td><td>

JSON Web Token \(JWT\) and metadata are missing domain visibility information

</td><td>

The JWT API only contains a claim for the domain, and is missing the list of domains visible to the user.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2014491

</td><td>

Predictive Intelligence \(PI\) fails due to an API restriction by the PI team

</td><td>

An error is returned.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2017386

</td><td>

Now Assist jobs are running for extended periods and slowing processing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Outbound REST Web Service

 PRB2001231

</td><td>

REST Message V2 doesn't support sending nor receiving OAuth credentials via MID Server

</td><td>

The MID Server can't be selected and OAuth credentials can't be sent as an authorization header via MID.

</td><td>

1.  Create an OAuth integration with any flow \(for example, auth code or client credentials\).
2.  Create a REST Message V2 record.
3.  Set 'Authentication type' to 'OAuth 2.0'.
4.  Set 'OAuth profile' to the OAuth entity profile created in the first step.
5.  Attempt to set the MID Server.

 Expected behavior: The MID Server can be selected, enabling the OAuth credential to be sent as an authorization header via MID.

 Actual behavior: The MID Server can't be selected. OAuth credentials can't be sent as an authorization header via MID.

</td></tr><tr><td>

Performance Analytics

 PRB1979962

</td><td>

Slow execution of the 'Indicator Data snapshot status update' scheduled job

</td><td>

 

</td><td>

1.  Run the 'Indicator Data snapshot status update' job.
2.  Observe that all the row counts are added to the pa\_cdc\_indicator\_table\_row\_count table.
3.  Run the 'Indicator Data snapshot status update' job again.
4.  Observe that run time is low as the row counts are already cached.
5.  Clear the cache \(cache.do\).
6.  Run the 'Indicator Data snapshot status update' job.

 Expected behavior: Since these are already captured in the table, it shouldn't take much time to run.

 Actual behavior: The DB call GlideAggregate is made again to get the row count.

</td></tr><tr><td>

Performance Analytics

 PRB2000268

</td><td>

The wrong formula score is shown when filtered on multiple elements

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1907336

</td><td>

The 'Created By' column values truncates after 10 characters in the Data Visualization library for Platform Analytics

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1979509

</td><td>

API changes to support date filtering for 'ON' and 'NOT ON' operators in **Date** fields on the list visualizations of Platform Analytics

</td><td>

There's an issue where date filtering doesn't work for 'ON' operator in **Date** fields on the list visualizations of Platform Analytics. This happens because the 'ON' operator also has a time selection option along with the date picker. For the 'ON' operator, it should only be the date selector, the time selector shouldn't exist there and API should support it.

</td><td>

1.  Open the Platform Analytics library: now/platform-analytics-workspace/dashboard-library.
2.  Notice the list visualization named 'Count'.
3.  Select the small filter icon which can be seen in the header line of the fields.
4.  Under the **Viewed** field \(or any date type field\), select the operator as 'on'.
5.  Select the calendar picker.
6.  Select any date to view any PAR dashboard.

 See that the filter isn't applied and the results aren't filtered.

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

 PRB2005345

</td><td>

Enable grouping on the Glide list field type

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2005346

</td><td>

Calendar improvement of color highlighting based on field styling

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2005359

</td><td>

Breakdown relations support for the 'Indicator Scorecard' API

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1846141

</td><td>

Certain missing properties for a visualization can cause side effects

</td><td>

Some impacts include drilldowns in a dashboard not working, and the **Save** button being enabled without any edit.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1974613

</td><td>

Color cache for mobile visualizations doesn't evict when there is a database update

</td><td>

The DB update isn't reflected in the API response as the cache still has the old color code value.

</td><td>

1.  Create a pie chart grouped by state from Visualization Designer.
2.  Invoke /api/now/sg/visualization.
3.  Make sure that the color code is returned for incident state 8 in the response.
4.  Navigate to the sys\_report\_chart\_color table.
5.  Filter table:incident and element:state.
6.  Update the color code for incident state 8.
    1.  Color name: Use the search box and choose alert--info-1.
    2.  Color: Open the alert--info-1 record using the **i preview** icon and copy the color code from there \(\#5EABDF\).
7.  Save the record.
8.  Invoke /api/now/sg/visualization again.
9.  Check the color code returned for incident state 8.

 Expected behavior: The color code should be returned as \#5EABDF for incident state 8.

 Actual behavior: The DB update isn't reflected in the API response as the cache still has the old color code value.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1993476

 [KB2961192](https://hi.service-now.com/kb_view.do?sysparm_article=KB2961192)

</td><td>

sys\_translated records are deleted unexpectedly when updating a tab name on a dashboard in Japanese

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1998900

</td><td>

Tab name translations find an incorrect translation value

</td><td>

 

</td><td>

 

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

Platform Analytics Migration API

 PRB1956520

</td><td>

Support the migration of a tab name and dashboard name translations

</td><td>

 

</td><td>

1.  Create a Core UI dashboard.
2.  Add tabs to change the user language to German.
3.  Update the dashboard tab names.

 After migration, users with the German language should see translated tab names.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1997683

</td><td>

Partial dashboard migration and rollback from a non-global domain creates duplicate records inside the domain

</td><td>

 

</td><td>

1.  Create a Core UI dashboard in the global domain.
2.  Migrate the dashboard partially in the global domain.
3.  Switch to the ACME domain open-migrated Next Experience dashboard.
4.  Rollback the dashboard inside the ACME domain.
5.  After rollback, it creates a Core UI dashboard in the ACME domain with an overrides value to the original dashboard.

 Observe that the Core UI dashboard isn't accessible from the ACME domain after rollback. Also, when users migrate a global Core UI dashboard inside a domain, then duplicate bridge records are generated.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2003609

</td><td>

After migration, widget settings are lost

</td><td>

All of the widget related properties \(follow filter, header settings, etc\) should be migrated to the widget\_props of par\_dashboard\_widget table.

</td><td>

1.  Create a CoreUI dashboard.
2.  Add a report widget that's used in other dashboards and set the header alignment to be center.
3.  Migrate the dashboard.
4.  Verify that the par\_visualization record is created for the sys\_report.
5.  Open the dashboard in Platform Analytics Experience.

 Expected behavior: The header alignment settings are migrated.

 Actual behavior: The header displays with the default settings.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2010427

</td><td>

Turn off auto-conversion of homepages to CoreUI dashboards after upgrades

</td><td>

1000 homepages are migrated every day, and it triggers a business rule that migrates CoreUI automatically.

</td><td>

 

</td></tr><tr><td>

Platform Runtime

 PRB2014434

</td><td>

The Granular Delegation API isn't returning any results

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1992485

</td><td>

Remove sys\_ids from Playbook-fetched telemetry metrics

</td><td>

Process definition information isn't included as part of data that is captured.

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

Playbooks \(Family Channel\)

 PRB2012190

</td><td>

When any one pill value is null, it returns null for the value of the whole input field

</td><td>

This happens for any multi pill-text inputs.

</td><td>

1.  Create action1, which takes in 1 input and 1 output of type 'String'.
2.  Create action2, which has 3 inputs of type 'String' and can be used as dynamic input action.
3.  Create a subflow1, which has 3 inputs.
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

Project Management

 PRB2007616

</td><td>

Duplicate investments are created

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Record Hierarchy

 PRB2011614

</td><td>

When a record hierarchy status record is deleted, performing reconciliation should correct it

</td><td>

A message appears saying that reconciliation has been scheduled, but no sys\_record\_hierarchy\_status record is created and no event is posted to sysevent.

</td><td>

1.  Open any record hierarchy \(for example, manager hierarchy on sys\_user\).
2.  Wait for the associated sys\_record\_hierarchy\_status record to reach a READY state.
3.  Delete the associated sys\_record\_hierarchy\_status record.
4.  Clear the cache by visiting /cache.do.
5.  Visit the associated sys\_record\_hierarchy record.
6.  Attempt to perform a reconciliation.

 Notice that a message appears saying that reconciliation has been scheduled, but no sys\_record\_hierarchy\_status record is created and no event is posted to sysevent.

</td></tr><tr><td>

ReleaseOps - Family

 PRB1953573

</td><td>

The 'Integrate DR' subflow should fail on an unexpectedly already-committed update set

</td><td>

The deployment request doesn't fail and the update set gets committed twice.

</td><td>

1.  Create an update set on dev.
2.  Export as XML.
3.  Import, preview, and commit the update set on test without using ReleaseOps.

Observe that the update set is committed without an info record and the controller isn't aware of the commit.

4.  Promote the update set to test using ReleaseOps.

 Expected behavior: The deployment request fails.

 Actual behavior: The deployment request doesn't fail and the update set gets committed twice.

</td></tr><tr><td>

ReleaseOps - Family

 PRB1960603

</td><td>

Deployment Request \(DR\) is not the catching preview conflict in 'Test', and moves to 'Ready for Deployment'

</td><td>

Batch update sets show a preview problem that is not caught in 'Test,' but then moves to 'Ready to Deploy' even though the update set is still in 'Preview'.

</td><td>

 

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

 PRB2009674

</td><td>

A final operation tracker response may occasionally be overwritten in Zurich

</td><td>

When the user creates a record in sn\_releaseopsbe\_operation\_tracker and creates certain sysevents, the operation tracker isn't updated.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB2011087

</td><td>

Add the ability to turn off/deactivate the Scripting Governance Tool \(SGT\) with a kill switch

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Scripting Governance Tool

 PRB1967275

</td><td>

Unable to remove the 'snc\_required\_script\_writer\_permission' role from users in a domain separated instance

</td><td>

 

</td><td>

1.  Provision an instance with the 'Domain Separation' plugin and demo data installed.
2.  Create a user in a subdomain.
3.  Assign a few roles \(snc\_internal and another role\) to the user.
4.  Check the sys\_user\_has\_role records.

Notice that a new record with the 'snc\_required\_script\_writer\_permission' role is created with an empty domain path. Make sure you open as a standalone list, because the records aren't visible in the related list.

5.  Open the sys\_user\_grmember table in the list view.

Notice that the user is added to the 'Conditional Script Writer' user group. Again, it's not visible under the 'Groups' related list because the domain path is empty.

6.  Disable the user \(active=false\).
7.  Re-enable the user \(active=true\).
8.  Check the sys\_user\_has\_role list.

 Observe that a new record with the snc\_required\_script\_writer\_permission role is created. The domain path is again empty/incorrect.

</td></tr><tr><td>

Service Catalog Components

 PRB1977677

 [KB2710223](https://hi.service-now.com/kb_view.do?sysparm_article=KB2710223)

</td><td>

The event 'Request generated' isn't triggered after using the catalog item in the Mobile variant

</td><td>

A new property called 'mode' was introduced on the catalog item component and defined in the now-ui.json file, which is responsible for exposing properties from the Seismic component to the UI Builder component. No default value was provided for this property in now-ui.json. As a result, when a new page is created and the component is dragged onto it, the mode property remains null by default. If 'mode' is standalone, the system proceeds with the submission and dispatches the request generated event. For any other value \(or null\), the submission doesn't proceed. The bug occurs because the code relies on JavaScript destructuring to set the default value for 'mode' as standalone which fails when 'mode' is explicitly present but set to null, as destructuring doesn't override null values. Therefore, the event isn't dispatched, and the request submission doesn't occur.

</td><td>

1.  Navigate to the UI Builder experience.
2.  Create a page.
3.  Drag the catalog item component onto the page.
4.  Don't configure any properties other than the default society of the item.
5.  Preview the page.
6.  Select **Order** on the component.

 Expected behavior: The system should submit the request and dispatch the request generated event.

 Actual behavior: The system doesn't proceed with request submission, and no request generated event is dispatched.

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1991914

</td><td>

Opening a TinyMCE PDF link in a new tab is blocked by Chrome when users click from a catalog item in a workspace where a Service Portal page is rendered in an iFrame

</td><td>

When PDF links are embedded into catalog items, clicking on the link directly from a workspace does not open the PDFs.

</td><td>

1.  Open a Chrome browser.
2.  Open any catalog item from the sc\_cat\_item table.
3.  Edit it.
4.  In the description, embed a link to a pdf and set it to open in a new window.
5.  Select **Try it** to confirm that the links are working properly.
6.  Open the same catalog item in Service Operations Workspace: now/sow/record/sc\_cat\_item/&lt;sys\_id&gt;.
7.  Select the link directly.

Observe that it doesn't open and says 'blocked by Chrome'.

8.  Right click on the link to open it in a new tab.

Observe that it works fine.


</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB2014263

</td><td>

Support view details and close in the interactive 'View status' page

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB2014265

</td><td>

New widget option for prefill for Catalog forms to support chat history

</td><td>

This is a product update.

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

 PRB1998727

</td><td>

In the case of duplicate relation records in CMDB, not all CIs are populated in Manual Service

</td><td>

The issue is related to duplicate records in cmdb\_rel\_ci. When one of the duplicate records are removed, the services were populated properly.

</td><td>

1.  Create Manual Service.
2.  Add relations to CMDB where the parent is 'service' and the child is some CIs.
3.  Add duplicated records of one relation using the BG script to the cmdb\_rel\_ci table.
4.  Add one more relation \(not duplicated\) for the service.
5.  Select **Update with changes from CMDB**.

 The entry point for the latest added CIs won't be added to the map.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2008680

</td><td>

Form metadata isn't fully unloaded in incremental download

</td><td>

All data from the last updated timestamp shown in sys\_update\_xml should get downloaded. Instead, form sections aren't downloaded.

</td><td>

Scenario 1:

 1.  Make sure an app exists on the instance with Form metadata containing a couple sections and elements.
2.  Add or update elements in the UI section.

Notice that the sys\_update\_xml table updates with changes.

3.  Perform download using FluentDownloader.
4.  Provide the last updated timestamp.

 Expected behavior: All data from the last updated timestamp shown in sys\_update\_xml gets downloaded.

 Actual behavior: Form sections are not downloaded.

 Scenario 2:

 1.  Make sure an app exists on the instance with Form metadata containing a couple sections and elements.
2.  Add or move existing sections in Form.

Notice that sys\_update\_xml updates with changes.

3.  Perform download using FluentDownloader.
4.  Provide the last updated timestamp.

 Expected behavior: All data from the last updated timestamp shown in sys\_update\_xml gets downloaded.

 Actual behavior: Form isn't downloaded. Only the UI section gets downloaded.

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

 PRB2002719

</td><td>

Field decorations no longer appear in Service Portal

</td><td>

The usage of g\_form.addDecoration no longer works in Service Portal.

</td><td>

1.  On the latest base instance version, create a client script on the incident table with the UI type 'Mobile/Service Portal'.
2.  Set the type to onLoad.
3.  In the script, add a line with g\_form.addDecoration, such as: g\_form.addDecoration\('description', 'icon-star', 'Please provide steps to reproduce the error.'\);.
4.  Navigate to https://\(YOUR INSTANCE\).service-now.com/sp?id=form&amp;t=incident.

 Expected behavior: Field decorations display a star symbol on the **Description** field.

 Actual behavior: Field decorations don't appear.

</td></tr><tr><td>

Service Portal

 PRB2005660

</td><td>

Tooltips on **Date** fields aren't shown when one of the fields in the record producer isn't visible on the form

</td><td>

There's an issue with the tooltip on date variables of the record producer in the Service Portal. When there are multiple **Date** fields and one \(or more\) of the fields is rendered based on some condition, or it's hidden, then the tool tip isn't shown for other **Date** fields on the form.

</td><td>

1.  Create a record producer.
2.  Create 3 date variables.
3.  Make one of the variable 'hidden'.
4.  Open the record producer in the portal.
5.  Hover over the **Date** field.

 Expected behavior: A tooltip is visible.

 Actual behavior: A tooltip isn't visible.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1908427

</td><td>

The 'Util' menu keeps loading if there are no conversations yet

</td><td>

 

</td><td>

1.  Navigate to a Washington DC instance.
2.  Select the sidebar **Discussion** button on the top of the page.

 Observe that when there are no discussions that the user is a part of or started by, the 'Util' menu keeps loading for that user.

</td></tr><tr><td>

Software Asset Management

 PRB1975702

</td><td>

Total\_spend/true\_up\_cost/over\_licensed\_amount/potential\_savings values at the publisher level are set to 0

</td><td>

This happens even though Product\_results have those values. The issue is due to missing code when creating the product results that don't have the SM.

</td><td>

1.  Pick a publisher where some products don't have the software model and some products have the total\_spend/true\_up\_cost /over\_licensed\_amount/ potential\_savings values.
2.  Run the reconciliation.

 Observe that the potential saving value is set to 0, even though some products have the potential saving value.

</td></tr><tr><td>

SSH MID Server Communication Protocol

 PRB1999773

</td><td>

The SSH connection fails with an error: 'Protocol version ID is too long'

</td><td>

This issue is happening because the SSH protocol version string and a different packet arrived at the same time. The buffer limit on the version string applied the limit on both packets, which caused a failure even though the version string size was within the buffer limit.

</td><td>

 

</td></tr><tr><td>

Standard Ticket Page

 PRB1969370

</td><td>

There's a random language translation on a request in Portal

</td><td>

When users change the system language from non-English to English, the 'Activity' and 'Attachment' tabs in the service portal ticket page remain in non-English.

</td><td>

 

</td></tr><tr><td>

Tables and Columns Data Dictionary

 PRB2002096

</td><td>

A null pointer exception \(NPE\) occurs in ChoiceList\#addNoCheck when the cache contains a null value, causing a 500 error on service portals

</td><td>

An NPE in ChoiceList\#addNoCheck causes a 500 error on the Employee Centre portal \(/esc\) when the sys\_choice\_compiled cache contains a null entry for a user with a non-null country code. The issue was reproduced synthetically via cache injection.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2010222

</td><td>

Trace collector for Zurich

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Triggers \(Family\)

 PRB2012475

</td><td>

TAAS improvements for AI Approval

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Triggers \(Family\)

 PRB2014592

</td><td>

Trigger as a service

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB2013168

</td><td>

Support Actions in AINPX

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1575910

</td><td>

When an activity stream pop-up is opened using a mouse, the user can interact with other interactive elements in the main content

</td><td>

 

</td><td>

1.  Open an instance on any form view.
2.  Remove the activities filter from the form section.

This enables the activity stream option on the right side of the form.

3.  Open any form, like incident or user profile, etc.
4.  Using the keyboard controls, navigate to and select **Activity Stream**.

The activity stream is opened on the right side of the form.

5.  Move focus to the activity stream.

 Notice that tabbing only moves between the **Close Activity Stream** button, **Additional Comments** field, **Work Notes** checkbox and the **Post** button.

</td></tr><tr><td>

UI Form Administration

 PRB1889844

</td><td>

Base instance incident caller location auto-population doesn't work

</td><td>

There is a restriction on the **sys\_user.sys\_id** field which causes the issue, but that isn't relevant on the Native UI.

</td><td>

1.  Open an instance.
2.  Impersonate a user.
3.  Navigate to SOW.
4.  Select **+**.
5.  Create an incident.
6.  Fill the **Caller** field with the impersonated user.

 Expected behavior: The **Location** field fills up automatically, as it does in the Native UI.

 Actual behavior: The **Location** field doesn't fill up automatically, even though it works fine in the Native UI with the same ACLs.

</td></tr><tr><td>

UI Form Administration

 PRB1939423

</td><td>

Workspace record context isn't updating Now Assist Panel \(NAP\) on the initial load of the record

</td><td>

On the first load of the record, 'action.payload.context' doesn't have the table and sys\_id of the opened record. When the workspace tab for the record is closed and reopened, it updates properly. On a Yokohama instance, it's correctly updated on the initial load.

</td><td>

1.  Log in to a znowassist instance with GenAI enabled.
2.  Open NAP \(**sparkle** icon\).
3.  Open dev tools.
4.  Set a breakpoint in the file called 'intent-behavior.js' at line 297 in the CONTEXT\_RECEIVED action handler.
5.  Open SOW workspace.
6.  Navigate to a list.
7.  Open any record.

 Expected behavior: 'Action.payload.context' has the table and sys\_id of the opened record.

 Actual behavior: On the first load of the record, 'action.payload.context' doesn't have the table and sys\_id of the opened record. When the workspace tab for the record is closed and reopened, it updates properly.

</td></tr><tr><td>

UI Form Administration

 PRB1959255

</td><td>

g\_form.clearValue shouldn't clear a choice field if the field is empty or has the default value

</td><td>

In Service Operations Workspace, the onChange client script only runs in the workspace if a reference isn't on the layout.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1988524

</td><td>

The copy/paste functionality is not working in the 'Email' section of the workspace.

</td><td>

This issue occurs after upgrading to Zurich.

</td><td>

1.  Log in to a Zurich instance.
2.  Open any workspace, such as Service Operations Workspace or HR Workspace.
3.  Open any record.
4.  Navigate to the **Compose email** section.
5.  Enter the email addresses.
6.  Select any email address.
7.  Perform Copy \(ctrl+c\) or Cut \(ctrl+X\) on the email address.
8.  Paste it in the 'To' or 'cc' or 'bcc' section.
9.  Notice that the email address is not copied.

 Expected behavior: The user is able to copy and paste.

 Actual behavior: The user is not able to copy and paste.

</td></tr><tr><td>

UI Form Administration

 PRB2011302

</td><td>

An API /api/now/ai\_agent/modified\_fields call on a form load increases the browser time

</td><td>

An API call has been added for every form operation as part of the platform engine feature '/api/now/ai\_agent/modified\_fields'.

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

 PRB1991306

</td><td>

On upgrade from Xanadu or Yokohama to Zurich, a 'Before' fix script runs even though it's not supposed to

</td><td>

The syslog contains relevant log messages.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1966686

</td><td>

There is a heap memory issue due to the queuedevents array growing uncontrollably

</td><td>

Unified Navigation breaks when legacyConfig becomes empty in the sessionStorage. This fix is for performance issues that occur when navigating between Next Experience pages.

</td><td>

1.  Load the home page.
2.  Open inspect mode in the browser.
3.  Navigate to the 'Application' tab.
4.  Delete session storage.
5.  Attempt to interact with the Unified Navigation or any other section of the page.

 Notice that there is an error for trackingConsent and for the page freezing.

</td></tr><tr><td>

Usage Analytics

 PRB2002024

</td><td>

There's an inaccuracy in IH transactions DEFN ID

</td><td>

The 'IH Usage' table has an accrual month logic, where the same record is updated every single day for the rest of the month. The IH transactions fabric credits DEFN ID only fetches the first day reporting of usage on a record, and not the rest of the 29 days.

</td><td>

 

</td></tr><tr><td>

UXF Macroponent

 PRB1899084

</td><td>

The technical dashboard override isn't applied when switching domains in UI Builder \(UIB\)

</td><td>

 

</td><td>

1.  Open an instance with the 'Domain separation' plugin installed.
2.  Create a technical dashboard within the global domain.
3.  Add a data visualization to it.
4.  Switch to another domain.
5.  Create a page override.
6.  Add an additional data visualization to the overridden page.
7.  Preview the created dashboard pages from UIB by switching domains.

The page content changes as expected.

8.  Open the technical dashboard via the Platform Analytics experience and switch domains to check the page content.

 Expected behavior: The overridden page variant should be displayed for the domain.

 Actual behavior: Only the global page variant is displayed in the domain.

</td></tr><tr><td>

UXF Macroponent

 PRB2009619

</td><td>

Multiple stuck threads cause semaphore exhaustion, requiring a node restart

</td><td>

There's a stuck semaphore transaction related to the function createCacheablePageFragmentFromShell in CacheablePageFragmentFactory.java. This can lead to multiple threads being stuck with no option but to restart the node to provide relief.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1957790

</td><td>

An error page displays when adding parameters to a page variant after a Zurich upgrade

</td><td>

'The page you are looking for could not be found' is displayed when setting a parameter condition to a page variant.

</td><td>

 

</td></tr><tr><td>

Versatile Node and Cluster Configuration

 PRB2002618

</td><td>

There's an AHA check failure due to a node\_id mismatch from capitalizing the host name

</td><td>

Domain Name System \(DNS\) PTR \(reverse-DNS\) records can return host names with uppercase instead of the expected lowercase. The HostUtil.getHostname\(\) should return lowercase.

</td><td>

1.  Start a node with a set system\_id.
2.  Note the node\_id.
3.  Modify the system ID to have 'AMS' capitalized.
4.  Restart the instance.
5.  Observe that the node ID is now different.
6.  Modify the system ID back to the original value.
7.  Restart the instance.
8.  Observe that the node ID is now back to the original.

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

 Expected behavior: interaction.transcript should show the sources that are displayed to the chat request.

 Actual behavior: interaction.transcript shows all sources in the smartLinksData regardless of whether or not they are shown to the user.

</td></tr><tr><td>

Virtual Agent

 PRB2004184

</td><td>

Update proxy URL from https://\[proxy\].servicenowlab.com to https://\[proxy\].service-now.com

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2004856

</td><td>

A premium chat upgrade should only apply to Zurich, not Australia

</td><td>

When a user is upgrading to NAVA April \(17.0.x\) version, if they are on Australia then they shouldn't get premium chat experience for Now Assist Portal \(NAP\). If they are on a Zurich version, they should get the premium chat experience for NAP.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2013144

</td><td>

A portal name is to be persisted in an interaction context

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2013145

</td><td>

Support AI\_NATIVE\_CHAT renderType on a full-page-wrapper-app

</td><td>

This is a product update.

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

 PRB2014827

</td><td>

Customize the NextWave search placeholder for AI Control Tower \(AICT\) assistant

</td><td>

 

</td><td>

1.  Navigate to any instance that has NextWave.
2.  On the NextWave home page, verify it displays the main search bar page.

 The search placeholder should be 'Ask Otto or search anything' for the AICT assistant.

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

 PRB2016737

</td><td>

OnGlide Search Pipeline fails

</td><td>

The search pipeline is failing due to a hard-coded major version check.

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

Virtual Agent Web Client

 PRB1976753

</td><td>

Messages sent in the new chat are some times getting merged with messages in the previous chat

</td><td>

The new input is merged in the previous conversation.

</td><td>

1.  Start a new chat.
2.  Give some input.
3.  Start another chat before the response comes in.
4.  Give a new input in the new chat.

 Notice the response from the previous chat sometimes show up in the new chat, and when refreshing the page, it's all in the same conversation, and the new input entered is merged in the previous conversation.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1994795

</td><td>

On changing non-English languages, links are translating from 'password' to 'lösenord', breaking the link

</td><td>

In the Swedish language the, 'password' should be displayed as is. Currently, the link is broken due to it translating as 'lösenord'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1998643

</td><td>

While requesting a catalog item in Now Assist Virtual Agent \(NAVA\), selecting the **Skip** button for a date/time question does not clear the date/time value in the **Input** field

</td><td>

While requesting a catalog item in NAVA, selecting 'Skip for a date/time question does not clear the automatically populated value in the **Input** field, which is generated based on the selected value of the date/time picker. The date/time value remains in the 'Input' field when the next question is presented, requiring the user to manually clear it before entering the answer for the current question.

</td><td>

1.  Open an instance.
2.  Create a record producer or catalog item with a date/time variable that has 'Mandatory' set to 'false'.
3.  Request the catalog item in NAVA in the Employee Service Center.
4.  Select **Skip** when the question based on this date/time variable is presented.

 Expected behavior: The date/time value populated in the text **Input** field is cleared for the next question.

 Actual behavior: The date/time value stays in the text **Input** field.

</td></tr><tr><td>

Visual Task Boards

 PRB1994303

</td><td>

In a Visual Task Board \(VTB\), the 'Select lane' menu displays lane values from all the boards available irrespective of the board selected to move

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB2010868

</td><td>

Attachments added through questionnaires aren't reflected/updated on the corresponding Work Order Task records

</td><td>

 

</td><td>

1.  Create an attachment-type question in a questionnaire.
2.  Assign the questionnaire to a user.
3.  Log in to the Mobile Agent application.
4.  Start work on the work order task \(WOT\).
5.  Select **Take Questionnaire**.
6.  Complete the questionnaire, including adding attachments.
7.  Check the platform record for the WOT.

 Observe that the attachments aren't reflected or updated.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 8 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2968809)
-   [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)
-   [Zurich Patch 7a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2935961)
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


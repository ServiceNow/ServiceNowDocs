---
title: Australia Patch 2
description: The Australia Patch 2 release contains important problem fixes.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-05-05"
reading_time_minutes: 86
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 2

The Australia Patch 2 release contains important problem fixes.

-   **Australia Patch 2 was released on May 05, 2026.**
    -   Build date: 04-29-2026\_2044
    -   Build tag: glide-australia-02-11-2026\_\_patch2-04-17-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A02.00.xlsx).

## Overview

Australia Patch 2 includes 332 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-ap2.png "Top 10 problem categories")

## Security-related fixes

Australia Patch 2 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 2, refer to [KB2977251](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2977251).

## Changes in Australia Patch 2

-   **Add the Now Assist context menu**

    Use the NACM to enable viewers of a dashboard to generate a summary of the contents of a dashboard or dashboard tab.

-   **Altering tables and fields using dictionary attributes**

    If true, enables case and accent \(diacritic\) sensitivity for text search of the column. If false, text search of the column is case and accent insensitive. The default behavior is false. This attribute can't be set to true when i18n\_session\_language\_sortable is true on the same column. To learn more see Set case and accent sensitivity on a per-column basis.

-   **Guarded script evaluator**

    The guarded script evaluator enhances instance security by supporting only a restricted scripting language and detecting or rejecting untrusted scripts that use unsupported JavaScript features.

-   **Install Live Archive**

    Install Live Archive to archive data in object storage.

-   **JavaScript APIs supported by guarded script**

    Review the JavaScript APIs that guarded script supports to help you analyze scripts in the Incompatible Guarded Scripts list and either rewrite them or create an exemption for them.

-   **Live Archive with RaptorDB Professional V2**

    Live Archive \(formerly Data Archiving\) moves records and attachments to object storage, freeing up space in the primary database while keeping data accessible for compliance and reporting. This capability improves query performance and provides scalable storage for large archives.

-   **Review and update scripts incompatible with guarded script**

    Review scripts that are incompatible with guarded script and either rewrite them to use supported features or create an exemption for scripts that can't be rewritten.

-   **[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)**

    For Now Assist new features and changes, see [Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md).

-   **Script sandbox environment**

    The script sandbox environment is a restricted execution context in which untrusted, client-generated scripts run on the server using one of two evaluators: the guarded script evaluator or the script sandbox evaluator.

-   **Script sandbox evaluator**

    The script sandbox evaluator helps prevent executing untrusted scripts on an instance by limiting the APIs available to scripts.

    Scripts that run in the script sandbox evaluator can use features supported by the JavaScript engine and the sandbox environment, except for certain restricted methods.

-   **Set case and accent sensitivity on a per-column basis**

    Set locale text match to provide case and accent sensitivity when searching the text of table columns. The default behavior for text searching in table columns is insensitive to case and accent \(diacritic\) variations, but you can enforce sensitivity using locale text match.

-   **System Archive**

    System Archive enables you to manage table growth by moving inactive records out of primary tables into dedicated archive tables within the same instance.

-   **Viewing all tables**

    By default, the list of live tables and live archive tables is filtered to show tables over 100 MB in size.

    Review storage breakdowns across tables in a unified view. Use this data to identify which tables contain the most archived data to adjust rule conditions or schedules.

    Estimate future object storage requirements by accounting for the compression in columnar storage. Base your storage forecasts on actual object storage growth rates rather than primary database removal rates, as these metrics don't correlate directly.


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

Application Manager

 PRB1988027

</td><td>

The Application Manager fails to load the Connected Workplace app info page with 'App info not found' error

</td><td>

In the Application Manager, the Connected Workplace app fails to load its information page when accessed from the Updates tab. The page spins for several minutes and then displays 'App info not found / Record not found', preventing the user from updating the app via the UI.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB2006319

</td><td>

ACL rules evaluated during twoPassQuery\(\) pull in mostly empty GlideRecords for context

</td><td>

During dot-walks, ACL rules evaluated during twoPassQuery\(\) often pull in mostly empty GlideRecords for context. This happens during script execution/condition evaluations.

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB1973824

 [KB2815909](https://hi.service-now.com/kb_view.do?sysparm_article=KB2815909)

</td><td>

Added approvers names don't appear on the Approver list of Request and RITM

</td><td>

When adding approvers to a Request \(REQ\) or Requested Item \(RITM\) via the Multi-Row Add \(MRA\) component in the Related Records section of Service Operations Workspace \(SOW\), a success message is displayed confirming that the approvers have been added. However, the Approver list does not display the newly added approver names. Similarly, when attempting to add approvers from the UI16 related list, the approvers are not added.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Server-side scripts

 PRB1994381

</td><td>

Discovery has issues on some node after upgrading to Australia RP2

</td><td>

After upgrading to Australia RP2 or later, Javascript running in app nodes fails to call Java functions. The following warning appears: '\*\*\* WARNING \*\*\* Evaluator: com.glide.script.RhinoEcmaError: undefined is not a function.' This impacts various features, including Discovery and Event Management.

</td><td>

1.  Open a Zurich instance with multiple nodes.
2.  Upgrade the instance from Zurich to Australia RP2.
3.  Run a quick Discovery or discover a few IPs.

 Notice that the Shazzam probe creation or Shazzam sensors processing has an error. The Shazzam probe isn't created with a name \(likely skipping some business rules\), and Shazzam sensor processing doesn't create the further probes in the chain. This results in discovery not running effectively.

</td></tr><tr><td>

UX Framework

 PRB2002003

 [KB2901692](https://hi.service-now.com/kb_view.do?sysparm_article=KB2901692)

</td><td>

Stuck semaphore due to the call GlideUxInteroperableRoutesProvider.getInteroperableRoutesByIds\(\)

</td><td>

 

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

 PRB2004286

</td><td>

A user's filter is incorrectly keying the supplemental map with translated keys, leading to an empty activity stream after changing the language

</td><td>

A supplemental map is incorrectly keyed with a translated string. It's also not correctly handling the case where the key in the map doesn't exist, leading to an uncaught exception and the activity stream not loading.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2009281

</td><td>

AI Specialist 'reviewed by' subtitle is shown on journal entries

</td><td>

 

</td><td>

1.  Navigate to any relevant workspace \(for example, SOW or CSM\) that contains an Activity Stream.
2.  Open a record \(for example, Incident\) that contains a comment or work note posted by an AI Specialist.

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

If the following conditions are true, on a page load, a page level user notification should be displayed indicating that there is a journal entry requiring review: The instance is configured for participation in AI specialist workflow / notification \(sn\_aia.enable\_ai\_workers = true\). 'journalUnderReview' is set to a non-empty string. 'journalUnderReview' is a valid sys\_id that corresponds to a journal entry associated with the current document. The URL doesn't contain a citation.

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
5.  Add a new incident record.
6.  Copy the sys\_id for the record \(INCIDENT\_SYS\_ID\).
7.  Add two work notes for the incident record.
8.  End the impersonation \(go back to admin\).
9.  Look up the sys\_id of the first work note \(WORK\_NOTE\_SYS\_ID\) in the sys\_journal\_field table.
10. Copy that sys\_id.
11. Run a background script to flag the work note for review.
12. Impersonate an ITIL user.
13. Open the incident record in UI16.

 Expected behavior: Page level notification is displayed: 'AI Specialist has updated fields and work notes. Please review the work notes and fields for accuracy.' The notification also contains a link titled **Review work notes**. When this link is selected, configured work note \(WORK\_NOTE\_SYS\_ID\) is highlighted in the activity stream using citation highlight snake animation.

 Actual behavior: No notification is displayed.

</td></tr><tr><td>

Agent Chat

 PRB1993351

</td><td>

Glide tries to send multiple unnecessary invisible messages to the requester when the live agent transfer is initiated

</td><td>

Several error logs are printed, including 'Failed to get client for base url'. The errors are related to unneeded messages being attempted to an incorrect URL.

</td><td>

1.  Set up an off-glide conversation server with a lab instance.
2.  Start a chat.
3.  Request a live agent.
4.  Check the node logs for the instance.

 Observe that several error logs are printed, including 'Failed to get client for base url'. The errors are related to unneeded messages being attempted to an incorrect URL.

</td></tr><tr><td>

Agent Chat

 PRB2002696

</td><td>

Different time zones on client and Agent workspace

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2004301

</td><td>

AI agent prioritization is not functioning correctly when the 'Include AI Agents' option is enabled

</td><td>

 

</td><td>

1.  Provision an instance with glide.awa and nowassist-ai-agents plugins on a Z or A instance.
2.  Enable 'Include AI Agents' for a assignment rule which has both AI agent and manual agents.
3.  Start a incident.

 Observe that incident is not assigned to an AI agent as preference even though it is available.

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

 PRB2007792

</td><td>

Date format is incorrect in the Active chat window

</td><td>

When the user starts a regular chat interaction and refreshes Agent workspace multiple times, the Agent chant window disappears.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2010436

</td><td>

Move **Include AI agents** related fields out of the 'Auto-assign handling' section

</td><td>

 

</td><td>

1.  Provision a Zurich instance with sn\_aia and interaction.awa plugins installed.
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
2.  Log in as both an agent and requester.
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

 PRB1999384

</td><td>

The Value\_overrides property is not working

</td><td>

The script tool returns undefined, and the agent fails.

</td><td>

1.  Navigate to sn\_aia\_property table and set the 'Enable value overrides' property to true.
2.  Create a basic agent with two tools.
    1.  Create a skill tool.
    2.  Create a script tool \(a tool to use the skill tools output as input\).
3.  Set value overrides on the script tool.
4.  Create an input, use the value override field to set it to the skills response. The script can be very minimal.
5.  Save and run agent in playground.

 Expected behavior: The script return the expected skill output that was passed to it.

 Actual behavior: The script tool returns undefined, and the agent fails.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2000110

</td><td>

Add post processor logic to get cardData info for FA based genAISkill execution

</td><td>

This is a product update.

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

 PRB2001595

</td><td>

Add support for web automation and desktop automation tools

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2002151

</td><td>

Role masking is not applied for AI agents when run through A2A

</td><td>

The issue is reproducible only with A2A secondary flow sync mode.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2003366

</td><td>

Data to glide from offglide is not logged with the actual user

</td><td>

Add Impersonate role to NextWave Service User to impersonate the actual call for glide backed set operations.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2004770

</td><td>

The worker\_manager should be able to create/update AI User records

</td><td>

This is a product update.

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
2.  Impersonate a service desk manager. For example, a user with the role sn\_sow\_itsm\_common.sn\_service\_desk\_manager.
3.  Make a copy of the AI Service Desk specialist.

 Observe that the default roles needed for the AI worker to perform any action aren't copied over. The user only takes the roles from the assignment group.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2015131

</td><td>

Turn on UI validation for **Record Update** and **Create Agent**

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1999484

</td><td>

KBB \(Knowledge Block\) checks break incremental indexing for some catalog child tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2001921

</td><td>

Indexed data gets wiped immediately after ingestion

</td><td>

Indexed data gets wiped immediately after ingestion for a specific table.

</td><td>

 

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

 PRB2015520

</td><td>

Synthesized Response generation does not consider custom sources

</td><td>

Results for the Synthesized Response come from articles and catalogs, and not from custom sources.

</td><td>

1.  Navigate to the 'Search' page in the /esc portal.
2.  Enter the search keyword, 'Camtasia for beginners'.

 Notice that the results come from articles or catalogs instead of custom sources, and the result should be from the Learning Course table.

</td></tr><tr><td>

AI Search

 PRB1753423

</td><td>

The table 'ais\_rule\_action' contains an empty field caused by an exception thrown when publishing the profile

</td><td>

An error occurs when publishing the profile, even though an error doesn't initially occur when saving the rule with an empty **Contains** field.

</td><td>

1.  Open any profile.
2.  In the Related List, create a new 'Result Improvement Rule'.
3.  Create the rule with a label.
4.  Check the **Activate on all queries** checkbox.
5.  Select **Create boost action** after the rule is created.
6.  Select the type **Boost with field match\(static\)**.
7.  Leave the **Contains** field empty.
8.  Select **Save**.

Notice that no errors occur.

9.  Return back to the profile in step 1.
10. Select the **Publish** button.

 Notice the error when publishing the profile.

</td></tr><tr><td>

AI Search

 PRB1886370

</td><td>

AisHostnameProximityEstimator reads datacenter names from host names as case insensitive, but then compares them as case sensitive

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1912337

</td><td>

The **Sort by** fields in the List View of Facet Filters display blank values

</td><td>

The **Sort by** column is completely blank in the Facet Filters, even though the field has a count when a record is open.

</td><td>

1.  Open any search application configuration, such as Service Portal.

Observe that in the Related list Facets table, the 'Sort by' column is completely blank.

2.  Open a record.

Observe that the **Sort by** field has a count or some other field selected, similarly in the AI Search Admin Console.

3.  Open any application.
4.  Navigate to **Facet filters**.

 Observe that the **Sort by** column is completely blank.

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

Observe that the search returns 'No Record Found'.

6.  Change the zoom to 80% and repeat the same search.

 Observe that Global Search in the Native UI doesn't return results.

</td></tr><tr><td>

AI Search UX

 PRB1993790

</td><td>

The typeahead search results panel doesn't close and the search state becomes inconsistent after selecting a catalog item

</td><td>

In a portal, the typeahead search widget drop-down list doesn't properly reset or close after selecting a catalog item using a mouse interaction. After performing multiple searches and selecting catalog items from the search drop-down list, issues occur.

</td><td>

1.  Log in to a Zurich instance as a portal admin.
2.  Navigate to Employee Center: /esc.
3.  Search for 'outlook' or 'email'.
4.  From the typeahead results drop-down list, select the catalog item using the mouse.
5.  When the results load, observe that the previously listed drop-down list/suggested results still display.

 Expected behavior: The drop-down list should close on selection. The search state should reset or behave consistently. No residual search results should remain visible.

 Actual behavior: The search results drop-down list remains visible after selection. The previous search list remains rendered.

</td></tr><tr><td>

AI Search UX

 PRB2002354

</td><td>

Conversational-agentic catalog results for NextWave should display a **Chat icon**

</td><td>

In a regular search result for regular search terms, users should be able to see the **Chat icon**.

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

Exact Match, when configured to honor conditions of search sources should be configurable for a single application, not entire instance

</td><td>

A system property called glide.search.exact\_match\_use\_search\_source\_filter enables all applications on the instance with exact match limited to those tables included in a search source and honors the conditions set within them. Users do not expect this feature to be enabled at the instance level, but require it to be enabled at the application level.

</td><td>

 

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

 Expected behavior: The synthesized answer loading card displays the full loading status text without overlapping. The card container expands or wraps to accommodate the full text string regardless of locale or viewport width.

 Actual behavior: The synthesized answer loading card overlaps its content. The loading status text is not fully visible. The card does not expand to accommodate the longer German locale status text string in the narrow viewport.

</td></tr><tr><td>

AI Search UX

 PRB2007702

</td><td>

Ask a follow up handoff

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2015147

</td><td>

The asyncGeniusResultTimerExpired flag is not reset after timeout, causing permanent render failure on subsequent searches

</td><td>

Results fail to render.

</td><td>

1.  Navigate to an experience using the sn-search-top-results Seismic component \(for example, Now Assist–enabled portal or Employee Center with AI Search configured\).
2.  Perform a search query that triggers a RAG/Genius Result response.
3.  Simulate or wait for a timeout condition in the RAG response \(for example, slow network, high latency instance, or LLM response delay exceeding the configured threshold\).

Observe that the search results fail to render after the timeout.

4.  Without reloading the page, perform a second search query.

 Expected behavior: Results render normally as the second request completes in time.

 Actual behavior: Results still fail to render — asyncGeniusResultTimerExpired remains true and is never reset, blocking all subsequent renders.

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
Notice that only multi-choice and 'Select box' are available.

4.  Create the same visualization in classic reporting.

 Notice that there's a lot more options available.

</td></tr><tr><td>

Application Manager

 PRB1971790

 [KB2827137](https://hi.service-now.com/kb_view.do?sysparm_article=KB2827137)

</td><td>

The size of the cache string is over 33.55MB, the GAAA response is too large to save as attachment.

</td><td>

Post-release of killing entitlements, the large get\_all\_available\_apps \(GAAA\) response is breaking the checkAvailableUpdates call in the UpdateChecker. Until the get\_all\_available\_apps response size is reduced below the ~32MiB limit, the App Manager will continue to have cache issues.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1992033

</td><td>

Incorrect Dependencies showing up for an app with customizations on Install Modal

</td><td>

An intermittent UI issue occurs in the Application Manager when viewing the Install Modal for apps with customizations. The issue arises when the initially selected base version is the latest version \(4.0.0\), but the default customized version is built on an older base version \(1.0.0\). If the older base version \(1.0.0\) is available in the base version drop-down list, the base version is automatically updated, causing dependencies for the newer version \(4.0.0\) to display instead of the expected dependencies for the customized version \(1.0.0\). This affects the display of dependencies but does not impact functionality. The issue is triggered by a specific edge case involving version linking.

</td><td>

 

</td></tr><tr><td>

Asset Management Common

 PRB2003545

</td><td>

The **Save** UI action is missing in HAM workspace when creating new Stockrooms if the plugin Problem Management for Service Operations workspace is not installed

</td><td>

Users that do not have the Problem Management for Service Operations workspace plugin installed do not see a **Save** UI action button when creating a new stockroom in HAM workspace.

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory** &gt; **All Stockrooms**.
2.  Select **New** to create a new stockroom.

 Observe that the UI action to save the stockroom is not visible.

</td></tr><tr><td>

Asset Management

 PRB2003556

</td><td>

The **Save** UI action is missing in HAM workspace when creating new Stockrooms if the plugin Problem Management for Service Operations workspace is not installed

</td><td>

Users that do not have the Problem Management for Service Operations workspace plugin installed do not see a **Save** UI action button when creating a new stockroom in HAM workspace.

</td><td>

1.  Navigate to **Workspaces** &gt; **Hardware Asset Workspace** &gt; **Inventory** &gt; **All Stockrooms**.
2.  Select **New** to create a new stockroom.

 Observe that the UI action to save the stockroom is not visible.

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB2012100

</td><td>

AMBSessionMessageQueues incorrectly gets becomes full.

</td><td>

Over time, the AMBSessionMessageQueues becomes full for a node and processing of messages get impacted.

</td><td>

 

</td></tr><tr><td>

Attachments to Records

 PRB1986352

</td><td>

Certificate attachments are deleted or becoming null, preventing User Experience Analytics collection from instances

</td><td>

Instances experience failures when platform components attempt to create certificate attachments on sys\_certificate records programatically.

</td><td>

 

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

 PRB2007236

</td><td>

Agentic workflow execution is stuck at 'Ready' and does not execute

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2002662

</td><td>

All SAM ATF tests failing with error - JS error 'SyntaxError: unexpected token: identifier' found during Step 'null'

</td><td>

 

</td><td>

1.  Request an instance on Australia build.
2.  Install com.sn\_samp\_master plugin.
3.  Run any of the tests in app-sam-atf-test or app-sam-atf-recon-test or app-sam-atf-demodata-recon-test.

 Observe that they all fail with the same error.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2006231

</td><td>

Metadata Persistence cause DB connections pool exhaust with a parallel tests execution

</td><td>

This occurs upon receiving a big number of metadata trace records.

</td><td>

1.  Create a test suite and add all active ATF tests to it.
2.  Copy test suite to a new one.
3.  Create separate user with admin roles.
4.  Run two test suites in parallel browser sessions.
5.  Monitor /stats.do?view=node Open Connections section with Utilization numbers.

 Notice that ATF tests start to fail because they are not able to acquire DB connection.

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

Build Agent \(Glide\)

 PRB1997824

</td><td>

Base instance app issue blocks NAFC installation

</td><td>

Now Assist for Creator \(NAFC\) can't be installed because the BA app is not included as part of distribution.

</td><td>

1.  License NAFC for an Australia instance.
2.  Attempt to install.

 Observe that it can't be installed because the BA app is not included as part of distribution.

</td></tr><tr><td>

Cache

 PRB1991677

</td><td>

The support for bulk loaded caches and unused entries cache should be removed

</td><td>

This is to disable the bulk-loaded caches from CacheReplication, which causes large amounts of traffic.

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

Case Management

 PRB1956961

</td><td>

Multiple **Create Case** buttons appear in a interaction record in Workspace

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2005309

</td><td>

Declarative way to choose model used for ITIL Normal/Standard/Emergency processes

</td><td>

This is a product update.

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

Content Analytics

 PRB2002450

</td><td>

JavaScript sandbox replacement for app-content-automation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Content Experiences

 PRB1991920

 [KB2836214](https://hi.service-now.com/kb_view.do?sysparm_article=KB2836214)

</td><td>

When editing homepage banner carousel content, the image disappears from the editor

</td><td>

Editing the homepage banner carousel content causes the background image to disappear from the editor preview after checking out and modifying the content name or header, though the image remains visible on the live portal.

</td><td>

 

</td></tr><tr><td>

Content Experiences

 PRB2002443

</td><td>

JavaScript sandbox replacement for app-content-publishing

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

CSM Workspace Components

 PRB2001110

</td><td>

After Australia RTP upgrade, all special handling notes are displayed with HTML tags

</td><td>

After Australia RTP upgrade, the message inside special handling notes is displayed with HTML tags.

</td><td>

 

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1983498

</td><td>

Migration fails with ava.util.ArrayList.iterator\(\)

</td><td>

During migration, tables fail with error message 'Cannot invoke 'java.util.ArrayList.iterator\(\)' because 'tables' is null'.

</td><td>

 

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1986928

</td><td>

chunk\_max\_row\_count and chunk\_max\_data\_size\_mb raptor input parameters modified

</td><td>

When the user attempts to create a columnar table using chunk\_max\_row\_count or chunk\_max\_data\_size\_mb parameters, Raptor doesn't honor the input parameters.

</td><td>

 

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1993175

</td><td>

Using the transactional statement batcher with columnar archive tables

</td><td>

After inserting into the archive table, a point lookup is performed to verify records before deleting them from the live table. The point lookup by sys\_id is slow when executed against the columnar table.

</td><td>

 

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1993184

</td><td>

Avoid reparenting columnar archive table with documentID reference

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1993185

</td><td>

Update Archive-Based Destroy Job to Support Column Store Tables

</td><td>

The destroy job uses a two‑pass delete query, which is extremely slow on columnar archive tables.

</td><td>

 

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1995269

</td><td>

Handle archive restore from columnar archive table

</td><td>

When an archive record is restored, it is deleted from the archive table.

</td><td>

 

</td></tr><tr><td>

Data Archiving to Object Store

 PRB2000230

</td><td>

Columnar table migration fails with OOM when collision detection on large tables and

</td><td>

Migration fails.

</td><td>

1.  Initiate columnar migration for a large table \(72 millions+ rows\).
2.  Navigate to Columnar Store Migration UI or DMJob.
3.  Update the script to only run migration for this large table.
4.  Start migration job.

 Expected behavior: Migration should succeed.

 Actual behavior: Migration fails for this table and subsequent retries fail as well.

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

 PRB1988680

</td><td>

While initializing a RecordHierarchy, path update events should not be recorded for processing

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1989461

</td><td>

Attempts to reconcile a RH in pending\_create or pending\_initialize states should repost those events

</td><td>

A hierarchy can get stuck in a PENDING\_CREATE or PENDING\_INITIALIZE state due to a lost, failed or missing event to allow them to progress to the next state. Attempts to reconcile the hierarchies are also ignored because the user can't reconcile un-initialized hierarchies.

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

1.  Create a glide\_list **access\_groups** field on cmdb\_ci \(or tpp\).
2.  Ensure that it is on the partition. If not, migrate it.
3.  Create a before-query business rule on cmdb\_ci\_server.
4.  Add an encoded query on glide list that uses the dynamic filter option 'One of my groups'.
5.  Execute DBSqlParser query: 'Select access\_group from cmdb\_ci\_server'.

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

Database Persistence

 PRB1885188

</td><td>

The JSON datatype is not supported in glide

</td><td>

An unknown column type appears for JSON and it becomes unavailable to map to. This issue is also observed for the 'Float' datatype.

</td><td>

1.  Ensure the user has a table in the MySQL remote database with a column of the type 'JSON', and that a connection is established with MySQL connector.
2.  Navigate to **Workflow Data Fabric** \(WDF\).
3.  Select a connection.
4.  Create data fabric table for a table that has a JSON column.
5.  Map the columns.

 Observe that there is an unknown column type selected for JSON, and it is unavailable to map to.

</td></tr><tr><td>

Database Persistence

 PRB1920865

</td><td>

The user observes the error 'decimal digits not present' when opening list view

</td><td>

The error occurs when one of the Date/Time columns has list calculations enabled.

</td><td>

1.  Navigate to **All** &gt; **Manager Analytics** &gt; **Voice Survey Mg2 DF**.When opening the list view, observe the error message 'Decimal digits not present'.
2.  In the list view, navigate to the column 'Last bonus Date' and select the three dots.
3.  Navigate to **Configure** &gt; **List Calculations** and deselect everything.
4.  Reload the list view.

 Notice that see the error disappears. Then, observe the error again upon re-selecting the list calculations.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1988910

</td><td>

Integer columns from external database systems are treated as decimal fields during WDF table creation, which prevents them from being used as reference fields

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2002769

</td><td>

The default security model for loopback data fabric queries is overly strict and will prevent user adoption

</td><td>

The default behavior of data fabric should allow users to access tables with remote tables if they already have access to that table using read ACLs. Currently, the default behavior is to block all access.

</td><td>

Attempt to query an SN table via Trino.

 Expected behavior: By default, the user should have access if they have read access to the table.

 Actual behavior: The user must have specific data\_fabric access granted to that table to run the query.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1887922

</td><td>

Binary data types are not mappable when creating DF table

</td><td>

Binary data type columns are greyed out and cannot be mapped.

</td><td>

1.  Provision a table with a binary datatype in the mySQL database.
2.  Create a DF table.

 Notice that the column with type binary is greyed out and cannot be mapped.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1987462

</td><td>

Editing connection refers to old trino primary

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB2005520

</td><td>

Fix DataFabricStatsAccumulator to support new plugin sn\_zcc\_primary

</td><td>

 

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

Data Management Console

 PRB1963627

</td><td>

A warning message is missing when an active archive rule becomes inactive after a condition changes

</td><td>

The **Active** button in 'Create flow' should be inactive when the rule is changed.

</td><td>

1.  Navigate to DMC and select any table with rules in archive rule active.
2.  Select the table and navigate to a 'Rule detail' page, change the conditions and select **Update**.

 Expected behavior: The rule should change to an inactive state, and a message should be displayed indicating that the rule was made inactive due to condition changes.

 Actual behavior: Active button in create flow should be inactive when the rule is changed.

</td></tr><tr><td>

Data Management Console

 PRB1977994

</td><td>

Remove unnecessary debug and warn logs in Stats Gatherer

</td><td>

The logs print many times in prod even though they're debug logs. The record count estimate for the table 'Optimal sys\_id prefix length' is fetched from the transaction cache for the table.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB1978032

</td><td>

'Edit rule' page takes excessive time to load conditions or fails to load them

</td><td>

The 'Edit rule' page takes around ten minutes to load the conditions.

</td><td>

1.  Navigate to the Create Rule module.
2.  Create a rule with conditions and save it successfully.
3.  From the rules list, select the **Edit** option for the created rule.
4.  Wait for the 'Edit rule' page to load.
5.  Observe the loading behavior of the conditions section.

 Expected behavior: The rule edit page should load within a few seconds. All configured conditions should be displayed correctly and consistently every time. Add a loading indicator so the user is aware before taking any action or updating an incomplete record.

 Actual behavior: The 'Edit rule' page takes around ten minutes to load the conditions. In some cases, the conditions do not load at all, leaving the edit page incomplete or blank.

</td></tr><tr><td>

Data Management Console

 PRB1992769

</td><td>

Migration to Strict Read-Only Fields for DMC tables

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB2010867

</td><td>

Label changes for the Tier 2 storage visualization on DMC

</td><td>

The label for Tier 2 storage visualization needs to be changed to 'Object storage used \(GB\)'.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB2012032

</td><td>

DMC does not show up in the s3 information tile if offloading is enabled

</td><td>

 

</td><td>

Activate com.glide.db.columnar.archive to enable offloading.

 Expected behavior: DMC should show up for the tier2 storage tile.

 Actual behavior: DMC does not show up for the tier2 storage tile.

</td></tr><tr><td>

Data Snapshots

 PRB1998307

</td><td>

Targets 'Too Early to track' is not implemented as per classic PA

</td><td>

Classic PA shows 'Too Early to track' status but DS indicator shows an empty status and also doesn't show its status on graphql single score.

</td><td>

 

</td></tr><tr><td>

Data Snapshots

 PRB2005229

</td><td>

Telemetry column indicator\_sysid is not supported

</td><td>

All columns should have finite data instead of infinite. The Indicator\_sysid column contains infinite values and should replace the name of the source table.

</td><td>

 

</td></tr><tr><td>

Data Snapshots

 PRB2009990

</td><td>

'Show records' shows scores one day ahead for a daily source

</td><td>

 

</td><td>

1.  Create a analytics source that collects data 'Daily' on Problem table with timezone America/Los\_Angeles and create DS indicator on it with no conditions.
2.  Run the collection jobs.
3.  Navigate to Source state table\(pa\_dm\_source\_state\) and set start\_date\_time as 30 days ago from current date and set last\_delta\_time as current date.
4.  Navigate to pa\_cdc\_fact\_problem and Change start\_date\_time to ten days of current date, so that scores before that day is 0.
5.  Navigate to KPI details for the newly created indicator, select the 11th day from current day where the zero score starts and select **Show Records**.

 Notice that **Show records** shows scores one day ahead.

</td></tr><tr><td>

Declarative Actions

 PRB1995366

</td><td>

AI gradient support in Declarative Actions \(DA\) and UI actions in Workspace and Core UI

</td><td>

This is a product update.

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

Demand Management

 PRB2008508

</td><td>

Missing conditional\_table\_query\_range ACL for dmn\_demand

</td><td>

The CTQR ACL is not present for the table dmn\_demand on base instance.

</td><td>

 

</td></tr><tr><td>

Developer Sandboxes

 PRB1978622

</td><td>

Post clone DSB recovery fails to start

</td><td>

DSBs are not rebuilt properly.

</td><td>

1.  Provision an instance with com.glide.dsb.cc installed on the source instance.
2.  Install and setup DSBs on the target instance.
3.  Trigger a clone from the source to target.
4.  Wait for the clone to finish.
5.  Run 'gs.info\(new sn\_dsb.API\(\).isEnabled\(\)\)' on the target instance

Notice that DSBs are disabled.

6.  Check the list of DSBs on the target instance

 Notice that none of the DSBs have been rebuilt.

</td></tr><tr><td>

Developer Sandboxes

 PRB2006165

</td><td>

DSB queue processing fails to start after upgrade from Zurich to Australia

</td><td>

The 'Process Sandbox Operation Queue' is only added during node transition to/from controller.

</td><td>

1.  Create a Zurich instance.
2.  Enable sandboxes.
3.  Create sandboxes.
4.  Upgrade instance to Australia.
5.  After upgrade has completed, check the sandbox states.

Notice that they're all stuck in 'Queued'.

6.  Verify that events are stuck in a 'Ready' state in a sysevent \(filter by name = dsb.create\).

 Check sys\_trigger for 'Process Sandbox Operation Queue' - there should be one per controller, but there are none.

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

While generally JSQLParser should have an ASTNode for every expression, there's a case in a query where that's not true. The lhs of the expression is irregular.

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

Dynamic Schema

 PRB1971762

</td><td>

DynamicSchema Integration Tests should not clear unassociated DynamicSchema metadata on the instance

</td><td>

When running DynamicSchema ITs in db-dynamic-schema-it, many of the tests start out by clearing all dynamic schema metadata on the instance in order to start with a clean slate.

</td><td>

 

</td></tr><tr><td>

Dynamic Schema

 PRB1976934

</td><td>

Attributes missing in the JSON should return null/undefined rather than NIL values

</td><td>

 

</td><td>

 

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
5.  Select a user who has two user profiles \(under 'To:'\). One active and one inactive.
6.  Navigate to the 'Emails' related tab.
7.  Open any email record.

 Expected behavior: Each recipient should be displayed only once in the notification, without any duplication.

 Actual behavior: Duplicate recipients are displayed in the notification for the same email under the 'Emails' related tab.

</td></tr><tr><td>

Email Notifications

 PRB2003482

</td><td>

Email client templates and quick messages are not visible in the side panel of the full composer when CreateDraftOnLoad is set to false

</td><td>

Email client templates and quick messages which are configured are not visible in the side panel.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB2006136

</td><td>

Push notifications for Android apps is not working when configured using Google Authentication Type - HTTP V1

</td><td>

In the Australia and Brazil instances, Android push notifications are not working when the push application is set to send notifications directly using an OAuth token.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB2010959

</td><td>

Missing conditional\_table\_query\_range ACL for sysevent\_email\_action

</td><td>

The user observes the error 'Part of the query on sysevent\_email\_action has been ignored because of insufficient access for 'query\_range' operation on sysevent\_email\_action.weight'.

</td><td>

1.  Assign 'notification\_admin' role to 'abel.tuter'.
2.  Impersonate 'abel.tuter' and navigate to 'sysevent\_email\_action\_list.do'.
3.  Add 'Weight' column to the list view.
4.  Add a filter 'weight&gt;10'.

 Expected behavior: The user should be able to perform query\_range operation and view the results.

 Actual behavior: The user observes the error 'Part of the query on sysevent\_email\_action has been ignored because of insufficient access for 'query\_range' operation on sysevent\_email\_action.weight'.

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

Encryption Support

 PRB1993181

</td><td>

Flow session cloning \(PFSessionClone\) needs to load all roles, including snc\_internal

</td><td>

GlideSecurityManager.get\(\).getRoles\(\) has side-effect of removing snc\_internal role when explicit roles plugin is enabled. Using GlideSecurityManager.get\(\).getRoles\(true\) will prevent this side-effect.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1930730

</td><td>

The graph reuse mechanism in CMDB grouping saves graphs that can contain CIs of more than four hops distance

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

 Observe that CI8 and CI6 create a new CMDB group. However, alerts should not be grouped.

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

 PRB1988355

</td><td>

The base instance Unreferenced Record Cleaner rules on the 'sys\_flow\_\*' tables have settings that can cause data loss

</td><td>

The rules have the following settings which could cause orphan records in other tables within the instance: 'Exclude archive: Checked/True Cascade delete: Unchecked/false', 'Clean audits: Unchecked/false', and 'Clean journals: Unchecked/false'.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2003199

</td><td>

Flow execution reporting level reverts to BASIC on sub-production instances

</td><td>

On the Australia release, the system property com.snc.process\_flow.reporting.level cannot be set to FULL on sub-production instances. After changing the value to FULL, the system automatically reverts it back to BASIC.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2006418

</td><td>

Query\_range operations failed on sys\_flow\_log due to missing conditional\_table\_query\_range ACLs in split-ownership scenarios

</td><td>

The root cause is the split-ownership scenarios where table Read ACL plugin differs from table definition plugin.

</td><td>

1.  Log in to any Australia instance and assign abel.tuter role 'flow\_admin'.
2.  Impersonate abel.tuter and navigate to sys\_flow\_log.
3.  Perform any range query operation \('contains'\) on the field **Context**.

 Expected behavior: abel.tuter with role 'flow\_admin' should be able to perform query\_range operation and view the results.

 Actual behavior: Part of the query on sys\_flow\_log has been ignored because of insufficient access for 'query\_range' operation on sys\_flow\_log.context.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2011637

</td><td>

Query\_range operations failed on sys\_hub\_flow internal\_name due to new global security rule

</td><td>

Query\_range operations failed on sys\_hub\_flow due to missing conditional\_table\_query\_range ACLs. The root cause is the split-ownership scenarios where table Read ACL plugin differs from table definition plugin.

</td><td>

1.  Give a user flow\_admin.
2.  Navigate to the list for sys\_hub\_flow.
3.  Try to query internal\_name Starts With.

 Notice that the list blocks that query.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2012618

</td><td>

Publish flows and actions scriptable API failure

</td><td>

The existing 'sn\_fd.FlowAPI.publish\(sysId\)' fails with the following error: 'Could not publish flow as Action Instance: 'name' is not published'. This happens when a flow contains action instances that point at draft/unpublished action type references. The UI endpoint \(/api/now/processflow/flow/\{sysId\}/snapshot\) works fine for the same flows.

</td><td>

 

</td></tr><tr><td>

Hardware Asset Management

 PRB2011465

</td><td>

Failures in app-ham-atf-test and app-ham-eam-atf-test ITs after enabling KittyScript DSL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB2008135

</td><td>

The user is unable to create a topic with the sn\_logstoanalytics application ID for log export service as admin

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Horizon Avatar Component

 PRB2010763

</td><td>

The gradient border is missing for AI Specialist avatars in the activity stream for Seismic interfaces

</td><td>

 

</td><td>

 

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

 Observe that the **Copy to Interview Summary** button isn't visible after the summary is generated.

</td></tr><tr><td>

Incident Management

 PRB2007117

</td><td>

Auto install applications based on license once instance is provisioned

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Incident Management

 PRB2011427

</td><td>

Remove IA and Now Assist for ITSM foundation entries from the auto-install list

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Indicator Management

 PRB1989726

</td><td>

The filter on list component is not concatenated when a card is selected

</td><td>

As part of library recommendation, when the user selects **View details** the list is filtered. When user selects a card it is not concatenated, but if the user manually adds a filter on list and selects a card it concatenates.

</td><td>

 

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB1905909

</td><td>

When setting a script in clone\_cleanup\_script table to active=false, the same script remains active=true in the clone\_profile\_cleanup\_scripts\_list table

</td><td>

Instance Clone : When setting a script in clone\_cleanup\_script table to acitve=false, the same script remains active=true in clone\_profile\_cleanup\_scripts\_list table

</td><td>

 

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB2002095

</td><td>

Creating a new Clone Profile or duplicating an existing profile pulls in all existing custom P/E/Scripts

</td><td>

Creating a new Clone Profile pulls in all existing P/E/Scripts. Duplicating a Profile via Clone App pulls in all existing P/E/Scripts.

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

Integration Hub

 PRB2005536

</td><td>

Lockpad missing for URL in SOAP step

</td><td>

When the user opens Flow Designer and adds a SOAP step, the lockpad is missing for URL input.

</td><td>

 

</td></tr><tr><td>

Integration Hub Steps for Action Designer

 PRB2003311

</td><td>

Duplicate target fields cause partial save and inconsistent database state during Map/Data Transfer Action save

</td><td>

When a user adds duplicate target fields and attempts to save a Map and Data Transfer Action, the system behaves inconsistently.

</td><td>

1.  Create or open a Map / Data Transfer Action.
2.  Add duplicate target fields in the target section.
3.  Attempt to save or publish the record.

Observe that an error is shown.

4.  Check the database tables.

Observe that partial target data is saved in sys\_rte\_eb\_entity in JSON and no corresponding record is created in sys\_rte\_eb\_definition.

5.  Fix the duplicate target field name to make it unique.
6.  Attempt to save or publish again.

 Observe that the record is still not inserted properly.

</td></tr><tr><td>

Integration Hub Steps for Action Designer

 PRB2005869

</td><td>

Fix scripted fields issues and drag and drop

</td><td>

When a pill is dropped for the first time it doesn't render the source tree. Additionally, when the user tries to edit a scripted field that is created, if new source fields are selected they are not persisted.

</td><td>

Add the data mapper step and create a step input and then map some source fields to target fields.

 Notice that when the pill is dropped for the first time it doesn't render the source tree.

</td></tr><tr><td>

Integration Hub Steps for Action Designer

 PRB2010179

</td><td>

Map and Transform step RTE fails to transform data when source field label contains spaces

</td><td>

When a Flow Designer action is created with a Map and Transform step, the RTE \(Runtime Transform Engine\) fails to correctly transform data if any input field label contains spaces \(for example, **First Name**\).

</td><td>

1.  Open Flow Designer and create a new action.
2.  Add an Input variable with a label containing a space. For example, 'First Name' \(internal name auto-set to 'first\_name'\).
3.  Add a Map and Transform step to the action.
4.  Configure the Map and Transform step to map the **First Name** input field to an output or target field.
5.  Save and publish the action.
6.  Trigger the action with a test value for **First Name**.
7.  Observe the output.

 Expected behavior: The RTE correctly identifies the source field by its internal name \(with underscores\) and transforms the data as configured.

 Actual behavior: The RTE skips source fields whose labels contain spaces, resulting in empty/null output for those fields.

</td></tr><tr><td>

Interactive Filters

 PRB1996683

</td><td>

Support of dependent fields in cascading filters for both reference and choice type-fields

</td><td>

When using choice fields \(not reference/M2M fields\) as cascading filters in a Platform Analytics workspace, selecting a value in a parent filter doesn't narrow down the available values in child filters.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1965036

</td><td>

Instances sys\_kmf\_external\_key table end up in an unclean state with multiple IRK's post clone/move

</td><td>

A grant rule is not revoked.

</td><td>

1.  Perform a cross region Move or Clone on Washington DC instances \(with or without EKMS, seeing same behavior\).
2.  The Rekey is complete but the source IRK record is still present in the target sys\_kmf\_external\_key table.

 Expected behavior: The source IRK should be deleted and Grant rule is revoked.

 Actual behavior: Observe that the grant rule is not revoked.

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

 PRB1988136

</td><td>

Users can associate the same article as a related article from kb\_knowledge

</td><td>

Add an **Abort** action business rule when the related article matches the knowledge article on the kb\_2\_kb table.

</td><td>

1.  Open an published KB article.
2.  Navigate to the related list.
3.  Find the 'Related articles' tab.
4.  Select the **Edit** button.
5.  Add another KB article as a related list.

 Observe that from the related list 'mapping record' achieved on step 4, users can edit the mapping record to and add the same record as the related article.

</td></tr><tr><td>

Knowledge Management

 PRB2005195

</td><td>

KM Import Article conversion utility should be exposed as a callable API for external consumption by the GRC/IRM policy flow

</td><td>

The KM Import Article feature uses Apache Tika and Apache POI libraries for DOCX-to-HTML conversion and produces flexible, translation-safe HTML output. On the other hand, the GRC policy flow's current GroupDocs-based conversion, which applies static absolute positioning. To resolve the translation formatting issue in GRC's policy flow, the KM conversion utility needs to be exposed as a standalone API that GRC/IRM can consume directly--without requiring an existing Knowledge Article upfront and without deleting the source attachment document during processing.

</td><td>

1.  Navigate to **Knowledge Management** &gt; **Import Article**
2.  Import a Word document.
3.  Open the created Knowledge Article.
4.  View the source HTML.

 Observe that the output contains flexible/relative styling and there's no static absolute positioning. Compare against a Knowledge Article created via the GRC/IRM policy flow and note the static positioning difference

</td></tr><tr><td>

Knowledge Management

 PRB2006452

</td><td>

Launch AI Native SKUs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2014078

</td><td>

Turn on the Apriel 2.0 model and set the new 3P model as the default

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1989782

</td><td>

Inconsistent naming of the three-dot menu on 'My Lists' \(Show Options vs. Menu Item Actions\)

</td><td>

Inconsistent tooltip naming of the three-dot menu on 'My Lists' \(Show Options vs. Menu Item Actions\) - Zurich in workspace

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1997156

</td><td>

List sections under My Lists tab of Workspace do not keep their expand / collapse state

</td><td>

With the 'List Bundle SNC' screen variant, the list sections under the 'My Lists' tab, such as 'Created by me', 'Shared with me' and 'Opened by link', do not keep their expand / collapse state after reloading the browser \(or a new browser session\) while the the list sections under Default list keep their expand / collapse state.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1997159

</td><td>

Lists created under 'My Lists' of Workspace requires explicitly provide the permission

</td><td>

With 'List Bundle SNC' screen variant enabled in Workspace, lists created under 'My Lists' now requires explicitly provide the permission. In the previous list screen variant 'List SNC', such premission is not required.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1998065

</td><td>

The 'Share' icon isn't visible after copying a list and sharing it

</td><td>

In the Zurich release, an issue has been identified in My Lists. Lists created using the 'Save a copy' option don't display the 'Share' icon after being shared. The icon only becomes visible after performing a manual page refresh. However, the share action completes successfully and the recipients receive access to the list. This creates a misleading user experience, since the UI doesn't reflect the actual shared state of the list.

</td><td>

1.  Open CSM/FSM Workspace.
2.  Navigate to My Lists.
3.  Open a list from either 'Created by me' or 'Shared with me'.
4.  Select **Save a copy**.
5.  Open the new copy.
6.  Share the copied list with a user or group.

 Expected behavior: After sharing the copied list, the **Share** icon appears immediately without requiring a page refresh.

 Actual behavior: After sharing the copied list, the **Share** icon doesn't appear immediately in the 'My Lists' overview page. It only becomes visible after refreshing/reloading the page.

</td></tr><tr><td>

List Administration

 PRB2008294

</td><td>

When using the filter search with wildcard \(\*\) for contains it instead filters it with 'is one of' rule.

</td><td>

Transform maps filters do not behave as expected when using the asterisk wildcard \(\*\) for the 'Contains' filter. Instead, the filters updates to 'is one of' after pressing 'Enter'.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2009056

</td><td>

The **Back** button after grouping isn't working

</td><td>

 

</td><td>

1.  Open any record list in a Zurich instance.
2.  Perform grouping on any field.
3.  Selec the **Show all** group header action.
4.  Select the **Back** button.

 Observe a JS exception in the console, preventing the **Back** button action.

</td></tr><tr><td>

List Editor

 PRB2001509

</td><td>

Inline list editing pop-up edit box UI is mispositioned when trying to edit a reference field by double clicking on it

</td><td>

The pop-up edit box UI is mispositioned when trying to edit any inline editable field by double clicking on it on a List Report added to a Dashboard. The dialog box that appears is positioned away from the actual field being edited and has an incorrect format: The cross is not red and the square around the magnifying glass is incomplete.

</td><td>

 

</td></tr><tr><td>

MetricBase

 PRB1659850

</td><td>

Fix failing tests that look for legacy trigger tables

</td><td>

Two errors messages occur. The error message, 'Application installation error message Table 'sys\_metric\_trigger\_level' does not exist' occurs in one scenario, and the error message, 'Application installation error message Table 'sys\_metric\_trigger' does not exist' occurs in another scenario.

</td><td>

 

</td></tr><tr><td>

MetricBase

 PRB2000747

</td><td>

Boolean literals are not parsed correctly in the 'where' clause, preventing queries

</td><td>

An execution error occurs.

</td><td>

1.  Create a Boolean Data Type metric.
2.  Run the script in scripts background.

 Expected behavior: Valid query result.

 Actual behavior: An error occurs, 'Script execution error: Script Identifier: null.null.script, Error Description: com.snc.clotho.ClothoException: com.glide.db.GlideSQLException: Element doesn't exist. Table: mb\_dex\_installed\_app\_metrics col: false.'

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

Mobile Platform

 PRB1989348

</td><td>

Filtering with a date range doesn't work in offline

</td><td>

All the tasks are still displayed after applying the filter.

</td><td>

1.  In any instance, activate the Field Service Management Demo plugin.
2.  As admin, double check that the List screen 'My tasks' has the default filter.
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

 PRB1995706

</td><td>

Zing Search Grouping Behavior does not work as expected

</td><td>

In mobile, when Zing search is enabled and the mobile search configuration for a launcher screen has the 'Interleave Result' flag set to false, duplicate results are being displayed in the grouped results.

</td><td>

 

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

Mobile Platform

 PRB2007847

</td><td>

Missing conditional\_table\_query\_range ACL for sys\_sg\_async\_service\_request in Australia

</td><td>

For a user with conditional read access, querying a table fails.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1979347

</td><td>

Interactive view is not launching for the map component even though the event is fired from LBF client

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1997600

</td><td>

Now Assist Panel performance issue

</td><td>

In Zurich or the latest instance with Now Assist enabled, when an ITIL or sn\_hr\_core.admin user opens an active record in a workspace \(such as SOW or HR Agent Workspace\), changes the **Assigned to** field to another user, pins the Now Assist panel, and then selects **Assign to me**, selecting **View Plan** under 'Now Assist has a plan for solving \(record\)' message does not display the generated resolution plan. Instead of showing the plan in the Now Assist Panel \(NAP\) as expected, the panel appears blank.

</td><td>

1.  Log in into any Zurich instance with Now Assist capabilities enabled.
2.  Impersonate any 'ITIL' or 'sn\_hr\_core.admin' user.
3.  Open any workspace \(for example, SOW or HR agent workspace\) and open an active Incident or HR record.
4.  Change the **Assigned to** field to a different user.
5.  Open now assist panel and 'pin' it.
6.  Select the **Assign to me** button.
7.  Select **View Plan**.

 Expected behavior: Plan is displayed on the NAP.

 Actual behavior: The NAP is blank.

</td></tr><tr><td>

Now Assist in Document Intelligence

 PRB1973445

</td><td>

sn\_docintel\_gen\_ai plugin takes an excessive amount of time during Zurich to Australia upgrade

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB2009288

</td><td>

Feedback isn't updated in the Gen AI log table

</td><td>

 

</td><td>

1.  Type 'What is spam?'.
2.  Select any feedback thumbs up/down icon immediately.

Observe that feedback is successfully stored in the Gen AI log table.

3.  Deselect submitted feedback or submit different feedback.

 Expected behavior: Feedback should be updated in the Gen AI log table.

 Actual behavior: Feedback isn't updated in Gen AI log table.

</td></tr><tr><td>

Now Mobile - Employee Experience

 PRB1993072

</td><td>

SP Cabrillo bundle isMethodAvailable should be called isAvailable

</td><td>

Cabrillo methods launchChat and performSearch throw an error on Service Portal.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2004938

</td><td>

Metadata changes to support Data Separation

</td><td>

Mosaic currently doesn't send the domain hierarchy to mosaic as a part of the metadata sync.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2008013

</td><td>

Log Sync Service isn't activated if sys\_service\_endpoint business rules and AI Native Chat Experience activation events are missed

</td><td>

 

</td><td>

 

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

 PRB2013877

</td><td>

Synchronous reseed calls fail silently with 404 when the originating Glide instance does not have the 'reseed-delta' endpoint

</td><td>

Execute request fails with capability hierarchy not found. No actionable error indicates the root cause is a missing Glide endpoint.

</td><td>

 

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

 PRB2000268

</td><td>

The wrong formula score is shown when filtered on multiple elements

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1975833

</td><td>

Report drillown records are inserted to report\_stats table

</td><td>

When the user logs in as Admin, opens Sys\_report table, and views any report with a class of sys\_report\_drillown the record is created in report\_stats table.

</td><td>

 

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

Enable grouping on the **Glide list** field type

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
3.  Make sure that the color code is returned for incident state eight in the response.
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

.

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

 PRB1999703

</td><td>

A dashboard can't be shared to all internal users, or with users with at least one role

</td><td>

The dashboard is not found when shared with the 'dashboard\_user' role.

</td><td>

1.  Create a dashboard.
2.  Share the dashboard to the role 'dashboard\_user' with view mode.
3.  Impersonate an ITIL user.
4.  Open the dashboard.

 Expected behavior: The dashboard should be visible to the ITIL user.

 Actual behavior: The dashboard is not found.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2004023

</td><td>

When non-existing visualization ID is being processed by Visualization,Java in the method getType, it will result in serialization error

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2005163

</td><td>

Rich text styles defined using style tags are not retained in Next Experience dashboards.

</td><td>

When rich text content containing CSS styles \(defined via style tags and class selectors\) undergoes via translation logic, the styles are not reflected in the final rendered output.

</td><td>

1.  Create a dashboard in Next Experience.
2.  Add a Rich Text component.
3.  Add content with embedded styles.
4.  Save the dashboard.
5.  Reload the dashboard.

 Observe that text is displayed without styling.

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

Platform Analytics Filters

 PRB1998380

</td><td>

Configured values are not respected for string field filters

</td><td>

All values are loaded and available for selection.

</td><td>

1.  Create a new PA dashboard.
2.  Add a multi-select filter with source **User** &gt; **Name**.
3.  Select **Configure values for filter source** and uncheck all names starting with A, B and C and save.
4.  Save and exit edit mode.
5.  Select the filter.

 Expected behavior: Unchecked values should be filtered out for filter values.

 Actual behavior: All values for User.Name \(including the ones starting with A, B and C\) are loaded and available for selection.

</td></tr><tr><td>

Platform Analytics Libraries

 PRB1992776

</td><td>

Allow users to create Core UI reports and dashboards

</td><td>

From Australia, users cannot create Core UI reports and dashboards.

</td><td>

 

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
3.  Migrate the dashbooard.
4.  Verify that the par\_visualization record is created for the sys\_report.
5.  Open the dashboard in PAE.

 Expected behavior: The header alignment settings are migrated.

 Actual behavior: The header displays with the default settings.

</td></tr><tr><td>

Playbook Experience

 PRB2000221

 [KB2917064](https://hi.service-now.com/kb_view.do?sysparm_article=KB2917064)

</td><td>

Saving the form without changing anything on the form caused the loading icon displayed until refreshing

</td><td>

When a Playbook activity uses a custom Declarative Action with the client action set to 'Playbook Form Submit,' selecting the **Save** button without modifying any form fields leaves the loading spinner active indefinitely. The activity appears stuck, preventing further interaction until the page is refreshed. This behavior affects users using the Australia or Zurich family releases and occurs only when the form is submitted unchanged.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Playbook Experience

 PRB2004436

</td><td>

The form section heading is incorrectly shown when an activity has only one form section

</td><td>

When displaying an activity that contains only one form section, and that section has a form heading defined, the heading is incorrectly rendered. When there is only one form section, no heading should be displayed. This is most visible with questionnaire activities, where the single section heading shows as 'Variables' when it should not be shown at all.

</td><td>

1.  Open a Playbook with a questionnaire activity \(or any activity with only one form section that has a heading defined\).
2.  Execute the Playbook to reach the questionnaire activity.

 Observe that the form section heading \(for example, 'Variables'\) is displayed.

</td></tr><tr><td>

Playbook Experience

 PRB2005336

</td><td>

Work notes added to Work note component after submission of Form in Playbook

</td><td>

When a Playbook activity contains a form with a **Work notes** field, submitting the form via 'Update' or 'Mark Complete' incorrectly adds the work notes entry to the Work Note component on the parent record.

</td><td>

1.  Have a parent record on a workspace with a work notes field.
2.  Have a playbook activity with a form that contains the **Work notes** field.
3.  Submit the form via Update or Mark Complete.

 Expected behavior: The work notes component does not get the work note data from the playbook form.

 Actual behavior: The work notes component gets the submitted work note data.

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

 PRB1999317

</td><td>

Playbook actions do not refresh the card

</td><td>

A button should either be hidden after selecting, or the button associated to next state \(start work/close complete\) should show up. Instead, the button persists despite taking the action on the playbook card.

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

Process Mining

 PRB2002953

</td><td>

The back-end sends a minimum duration value instead of the mean duration for a Project card's average duration

</td><td>

 

</td><td>

1.  Navigate to process models.
2.  Take any playbook project and note the average duration on the project card.
3.  Navigate to Workbench and note the average duration shown in the header.
4.  Open Global Metrics and note the average duration.

 Expected behavior: On the project card, average duration should retrieve the mean duration values which has been fixed and is being called from the front-end side.

 Actual behavior: On the project card, the minimum duration value is sent for average duration. Therefor, there is a discrepancy in the stats shown for average duration.

</td></tr><tr><td>

Project Management

 PRB2007616

</td><td>

Duplicate investments are created

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB2010566

</td><td>

Missing conditional\_table\_query\_range ACL for cost\_plan and cost\_plan\_breakdown

</td><td>

The CTQR ACL is not present for the table cost\_plan and cost\_plan\_breakdown on base instance.

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

Related Lists

 PRB2000158

 [KB2823064](https://hi.service-now.com/kb_view.do?sysparm_article=KB2823064)

</td><td>

Related lists do not show row data

</td><td>

 

</td><td>

Refer to the listed KB article for details.

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

Reporting

 PRB2005733

</td><td>

Issue with drilldown Map in Reporting on Australia release

</td><td>

The map type does not work as expected after an instance upgrade to Australia. It shows the data on the map, but when any of the data points are selected it drills down to another country, which shows the value as 'Map' but displays something different on the Map Key.

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

Scripted REST APIs

 PRB1996583

</td><td>

There's high latency of the REST API scriptable

</td><td>

The existing scriptable methods jsFunction\_getDetailedServices and jsFunction\_getDetailedServicesWithOAuthPolicy had the withSchemaContent flag hardcoded to true, forcing retrieval of schema information for every API resource, which the MCP team doesn't need in the first step. This fix exposes withSchemaContent as an explicit parameter, letting the caller decide based on their use case.

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

Notice that a new record with the 'snc\_required\_script\_writer\_permission' role is created with an empty domain path. Make sure to open as a standalone list, because the records aren't visible in the related list.

5.  Open the sys\_user\_grmember table in the list view.

Notice that the user is added to the 'Conditional Script Writer' user group. Again, it's not visible under the Groups related list because the domain path is empty.

6.  Disable the user \(active=false\).
7.  Reenable the user \(active=true\).
8.  Check the sys\_user\_has\_role list.

 Observe that a new record with the snc\_required\_script\_writer\_permission role is created. The domain path is again empty/incorrect.

</td></tr><tr><td>

Server-side scripts

 PRB1977307

</td><td>

Module implementation adds a requirement to global and causes an increase in SecurityException being thrown

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

1.  Create a scope and a new table.
2.  Create a relationship \(sys\_relationship\) record with the following configuration:
    1.  Name: Created by
    2.  Advanced: true
    3.  Applies to table: New Scoped Table
    4.  Apply to: gs.debug\('Table Name: ' + table\_name\);
3.  Open the New Scoped Table form.
4.  Right-click and navigate to **Configure** &gt; **Related Lists**.

 Notice that when checking the system logs, the following error message occurs: 'com.glide.script.RhinoEcmaError: 'table\_name' is not defined. : Line\(1\) column\(0\) ==&gt; 1: gs.debug\('Table Name: ' + table\_name\); Stack trace: at :1.'

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

Service Catalog

 PRB2010774

 [KB2943324](https://hi.service-now.com/kb_view.do?sysparm_article=KB2943324)

</td><td>

In the service portal, selecting categories does not do anything

</td><td>

When selecting Catalog Categories in SP Portal, nothing happens.

</td><td>

1.  Navigate to SP portal.
2.  Select **Catalog**.
3.  Select any of the categories on the left.

 Observe that the catalog items don't appear. The URL keeps changing but stays on the same page.

</td></tr><tr><td>

Service Exchange for Consumers

 PRB2007859

 [KB2956938](https://hi.service-now.com/kb_view.do?sysparm_article=KB2956938)

</td><td>

Inbound transforms for Service Exchange do not execute as expected

</td><td>

Inbound transforms for Service Exchange are not applied unless the integration user has the role sb\_admin.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Mapping

 PRB1998727

</td><td>

In the case of duplicate relation records in CMDB, not all CIs are populated in Manual Service

</td><td>

The issue is related to duplicate records in cmdb\_rel\_ci. When one of the duplicate records are removed, the services were populated properly.

</td><td>

1.  Create Manual Service.
2.  Add relations to CMDB where the parent is 'Service' and the child is some CIs.
3.  Add duplicated records of one relation using the BG script to the cmdb\_rel\_ci table.
4.  Add one more relation \(not duplicated\) for the service.
5.  Select **Update with changes from CMDB**.

 The entry point for the latest added CIs won't be added to the map.

</td></tr><tr><td>

ServiceNow Data Catalog \(Glide\)

 PRB2005266

</td><td>

IllegalStateException in tableAccessCheck\(\) when executing Glide RDF queries

</td><td>

The RdfGraphStoreJSIT.writeMaxSizeTriple test is failing in the eco tests for the 'dcg-rdf-api-test' project.

</td><td>

 

</td></tr><tr><td>

ServiceNow Data Catalog \(Glide\)

 PRB2010122

</td><td>

A collector exception with no message is reported as a success, not a failure

</td><td>

com.snc.process\_flow.operation.collector.CollectorExecutor relies on all error messages have non-null results from 'Throwable.getMessage\(\)'.

</td><td>

 

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2005272

</td><td>

The app download from now-sdk fails when there are unpublished wf\_workflow\_version records in the app

</td><td>

The command 'now-sdk download/transform' fails with an error.

</td><td>

1.  Take any fluent app that has unpublished wf\_workflow\_version records.
2.  Run now-sdk download/transform.

 Notice that the command fails with the 'Unexpected error' log, and there is an exception logged on the instance log.

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

 Actual behavior: Form sections are not downloaded. Scenario 2:

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

</td><td>

Catalog items' M2M category user criteria aren't considered in late binding

</td><td>

The Service Catalog is split by company, with some items viewable for some companies, and some for more than one. One form that should be visible to two companies doesn't display in the Service Portal search. The form is available for both companies and is in two categories. It can be seen in 'Services' by some users, but it doesn't appear in search results for the other company's users.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1985812

</td><td>

AI tool authors should be able to override widget action scripts

</td><td>

A tool author should be able to override the sys\_ux\_widget\_action their own custom script without copying the entire widget.

</td><td>

 

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

 Expected behavior: Field decorations display a star symbol on the **Description** field.

 Actual behavior: Field decorations don't appear.

</td></tr><tr><td>

Service Portal

 PRB2005660

</td><td>

Tooltips on **Date** fields aren't shown when one of the fields in the record producer isn't visible on the form

</td><td>

There's an issue with the tooltip on date variables of the record producer in the Service Portal. When there are multiple **Date** fields and one \(or more\) of the fields is rendered based on some condition, or it's hidden, then the tool tip isn't shown for other 'Date' fields on the form.

</td><td>

1.  Create a record producer.
2.  Create three date variables.
3.  Make one of the variable 'hidden'.
4.  Open the record producer in the portal.
5.  Hover over the **Date** field.

 Expected behavior: A tooltip is visible.

 Actual behavior: A tooltip isn't visible.

</td></tr><tr><td>

Service Portal

 PRB2005800

</td><td>

The attachment window continues to load when dragging / dropping an opened One Drive file

</td><td>

The getMessage used here causes the test AspirationCreationIT.verifyTrapFocus from egd-store-aspirations-test to fail.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2000639

</td><td>

Workspace changes to Job Failure Troubleshooting for Australia

</td><td>

This is a product update

</td><td>

 

</td></tr><tr><td>

SSH MID Server Communication Protocol

 PRB1999773

</td><td>

The SSH connection fails with an error: 'Protocol version ID is too long'

</td><td>

This issue is happening because the SSH protocol version string and a different packet arrived at the same time. The buffer limit on the version string applied the limit on both packets, which caused a failure even though the version string size was within the buffer limit.

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB1988698

</td><td>

A zboot error on anowassist regarding sys\_kafka\_topic\_m2m\_sys\_sc\_topic\_alias

</td><td>

The error occurs: 'glide SysLog \*\*\* ERROR \*\*\* STREAM\_CONNECT: SCUpgradeZToA: Got exception while executing fix script: Required table sys\_kafka\_topic\_m2m\_sys\_sc\_topic\_alias not found on instance.'

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB1997412

</td><td>

Fix the SCRAM auth issue that enables glide to connect to Amazon MSK cluster

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB2005282

</td><td>

Track Direct Kafka Consumer Usage Metrics

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB2011230

</td><td>

Error messages appear in a flow engine log when a message is produced to a Kafka Flow Trigger

</td><td>

This hinders any possibility of debugging issues with a flow.

</td><td>

1.  Set up a direct Kafka cluster.
2.  Create a Kafka Flow Trigger Consumer with a topic alias, publish it.
3.  Make sure the flow reporting setting is set to 'Full' or 'Basic'.
4.  Push a message on Kafka so this flow consumes it.

 Notice the error in execution log.

</td></tr><tr><td>

System Events

 PRB2001375

</td><td>

The next discovery in the daisy chain is not triggered when the current discovery is cancelled

</td><td>

When discovery is cancelled, it generates two events, discovery.canceled and discovery.complete. Whenever discovery.cancelled is picked up first, triggers the next discovery. When discovery.complete is picked up first, it does not trigger the discovery as the script action 'Discovery Run Next'. With that, discovery.complete exits on the condition 'current.state == 'Canceled' or canceledEventExists. When discovery.cancelled is picked after this, 'Discovery Run Next' exits on the condition that there is already a processed discovery.complete event for this status record.

</td><td>

1.  Make a daisy chain of discovery schedules to trigger one after another.
2.  Set 'Even if canceled' to 'true'.
3.  Run discovery and cancel it.

 Notice that even though the next discovery should be triggered, it does not always happen.

</td></tr><tr><td>

System Export Sets

 PRB2005111

</td><td>

Parallel delta export updates last\_export\_run independently in each job, so the cursor advances too early and skips records in the next run

</td><td>

Parallel delta export updates last\_export\_run in each parallel job as they start at different times, causing delta cursor to advance before all jobs are complete. This results in skipped records in the next run.

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

Transaction Logs

 PRB1997038

</td><td>

The **http\_response\_code** field in the syslog\_transaction table should be read-only

</td><td>

 

</td><td>

Open a syslog\_transaction record in form view.

 Observe that the **http\_response\_code** field may be editable.

</td></tr><tr><td>

Transaction Management

 PRB1996223

</td><td>

Modify parameters for TimeBasedStatusSampler for better memory state tracking

</td><td>

The parameters for TimeBasedStatusSampler are used for Memory Health Checks by Loanable Semaphore. The NodeHealthChecker takes too long to identify the high memory pressure, so the parameters should be modified for better memory state tracking.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1986121

</td><td>

Phone number from Côte d'Ivoire invalid

</td><td>

The entered number does not pass the validations defined in the Sys Phone Territory configuration for that territory.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2005816

</td><td>

A **Choice** field with None does not appear intermittently

</td><td>

A **Choice** field with None does not appear in some cases for some users and sets the value of the next sequence number by default.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1789457

</td><td>

The Advanced Reference Qualifier for reference fields is not working

</td><td>

The reference qualifier on a reference catalog variable does not work if it uses 'contains' \('LIKE'\) operand on dot-walked **glide\_list** field in combination with any other condition.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2004264

</td><td>

Updates to support AI Specialist and draft note

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2011302

</td><td>

An API /api/now/ai\_agent/modified\_fields call on a form load increases the browser time

</td><td>

An API call has been added for every form operation as part of the platform engine feature '/api/now/ai\_agent/modified\_fields'.

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

Upgrade Center

 PRB1992027

</td><td>

'Add node' automation times out too quickly

</td><td>

'Add node' automation times out before the node is online.

</td><td>

 

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

 PRB1970316

</td><td>

JAWS/NVDA does not announce the tab built using sn-canvas-menu component on page load

</td><td>

When navigating into the certificate management dashboard, the selected status of the selected tab does not have its selected status reported by JAWS on first page load. After the same tab or another tab is selected, the status is correctly reported.

</td><td>

1.  Launch JAWS.
2.  Impersonate Beth Anglin.
3.  From the 'All' menu, navigate to the certificate management page.
4.  Navigate the page to find tabs like 'Tasks', 'Records', and 'Download'.

Note that the currently selected tab does not have a selected status reported by JAWS.

5.  Select a tab.

Note that tab now reports its selected status.

6.  Reload the page, and note the lack of selected status.

 Expected behavior: The selected status of currently selected tab is always reported.

 Actual behavior: The selected status of the tab is not reported on first page load.

</td></tr><tr><td>

UX Framework

 PRB1977362

</td><td>

At 400% zoom the screen shifts to the right and requires horizontal scroll when opening the tabs container

</td><td>

On expanding the More drop-down list, the screen shifts right. Horizontal scrolling at the page level is required to view the main UI and the items in the drop-down list

</td><td>

1.  Navigate to a base instance with Hardware Asset Workspace \(plugin: sn\_hamp\).
2.  Navigate to **All** &gt; **Hardware Asset Workspace**.
3.  Open at least one other record.
4.  Set window size to 1280x1024.
5.  Zoom the window in to 400%.

The second tab in the tab container is now in a **More** drop-down list.

6.  Expand the tab.

 Expected Behavior: Content does not require scrolling in two dimensions \(both vertically and horizontally\).

 Actual Behavior: Content requires scrolling in two dimensions \(both vertically and horizontally\).

</td></tr><tr><td>

UX Framework

 PRB1988996

</td><td>

Model-less dialog is not opening over a model in Australia

</td><td>

There is a modeless dialog over a model that is opened when the field decorator in the **Condition** field is triggered.

</td><td>

 

</td></tr><tr><td>

Vault Console

 PRB2011312

</td><td>

Deny Unless Vault console ACL blocks access to dp\_configuration\_domain separated table.=

</td><td>

 

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

 Observe that the node ID is now back to the original.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB2006402

</td><td>

AI Connector node should hide custom skills based on foundation, advanced and prime plugins

</td><td>

In scenario 1, the custom skill in the skill type should only be available when there are no platform type installations on the instance or when the installation type is prime. It should be hidden in the skill type of ai connector node for advanced and foundation. In scenario 2, when there is no custom skill in the skill type, the AI agent should be selected on default for ai connector node. In scenario 3, the AI agents that are specific to list of subscription profiles sn\_ai\_plat\_fdn, sn\_ai\_plat\_adv or sn\_ai\_plat\_prm in sys\_gen\_ai\_asset\_subscription table should also be specifc in the AI agents drop-down list of the AI connector node. AI agents that are not accessible for certain subscription profile should also be restricted to select from AI connector node.

</td><td>

 

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

 PRB1999948

</td><td>

Make conversation cache glide backed

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2002220

</td><td>

Topics that are 'interrupted' put the conversation in a bad state

</td><td>

 

</td><td>

1.  Invoke an Agent that invokes a topic-as-a-tool.
2.  Ensure that the topic has a Boolean/yes/no question, such as 'Do you like Fridays?'.
3.  When the runs and asks if the user likes Fridays, answer with 'What is spam'?
4.  Verify that the topic stops and there's an LLM answer about spam.
5.  Perform a Q&amp;A about spam.
6.  Type another phrase that would trigger an agent, where the 2nd agent is configured with a tool that is-a topic.

 Notice that the second topic doesn't run correctly. The conversation is stuck at this point.

</td></tr><tr><td>

Virtual Agent

 PRB2003145

</td><td>

Add session\_key claim to tokens generated for nextwave calls

</td><td>

NW tokens generated by conversation service in current flavor does not have session\_key session\_key holds the glide session id which connects session-bound tokens with the OBO session routing path in GlideHttpRequestContext, which extracts session\_key from the inner token to route requests to the correct user session. The initial token which is used to generate new tokens JWT\(NW\) will now have this extra claim session\_key.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2003370

</td><td>

Use 'Common Logging' framework

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2003443

</td><td>

Sort promoted skills based on order

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2004044

</td><td>

vaContext.url is undefined in NextWave

</td><td>

 

</td><td>

1.  Create a LLM topic.
2.  use vaContext.url in the script.
3.  Call the LLM topic through the nextWave NAP.

 Notice that the vaContext.url is undefined.

</td></tr><tr><td>

Virtual Agent

 PRB2004184

</td><td>

Update proxy URL from https://\[proxy\].servicenowlab.com to https://\[proxy\].service-now.com

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2004408

</td><td>

getNearestInternalEndpoint\(\) compares endpoint names instead of URLs for DC proximity, making selection order-dependent

</td><td>

In NextwaveEndpointService.getNearestInternalEndpoint\(\), the HostnameProximityEstimator compares endpoint names \(for example, 'nextwave-fqsn-0', 'nextwave-fqsn-1'\) instead of endpoint URLs. Since the endpoint names have no datacenter segment, the proximity estimator computes identical distances for all endpoints, and min\(\) simply returns whichever endpoint appears first in stream order — not the one in the same datacenter as the Glide node.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2004906

</td><td>

After upgrading from Zurich, NAP does not work

</td><td>

An error message appears.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2005501

</td><td>

Make Next Wave client auto-suggest debounce configurable

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2005783

</td><td>

Dynamic Translation doesn't work on topic execution and live agent messages in the nextwave code path due to missing code

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2006124

</td><td>

A topic doesn't resume from where it left

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Open AI agent playground.
3.  Select the **Demo Next Best Action Agent** agent and run it.

Observe that the execution gets stuck right after the first tool call.

4.  Check the sys\_generative\_ai\_log for the above conversation.

 Observe that there are two LLM calls.

</td></tr><tr><td>

Virtual Agent

 PRB2006256

</td><td>

After upgrading from Zurich, NAP is not working

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2008646

</td><td>

The Virtual Agent API that adds processing messages for web automation tools is not working in OFFGlide exeperience

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2010355

</td><td>

A thinking process doesn't display in Now Assist Portal for web agents

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2012889

</td><td>

vaSystem.getSearchText isn't working with offglide

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2013143

</td><td>

Portal name to be persisted in interaction context

</td><td>

This is a product update.

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

 PRB2015636

</td><td>

NAP premium chat should not be supported

</td><td>

Premium chat should not be an option for NAP.

</td><td>

1.  Navigate to Assistant Designer for NAP Platform assistant
2.  Navigate to 'Display experiences' page

 Notice that display experience is set to 'Enhanced' but if instance has nextwave setup, an **Edit** button will be available next to it allowing user to change display experience to 'Premium'.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1930368

</td><td>

Linguistic errors for Japanese were found during a Virtual Agent \(VA\) conversation

</td><td>

A number appears in the wrong place in the text, '1 選択済み'.

</td><td>

1.  Navigate to /esc and open the chat bot.
2.  Type 'Presentation device' manually and start the conversation.
3.  Select options or enter the asked information and proceed with the flow.

 Observe the incorrect highlighted message/strings: '1 選択済み' and '送信 1' - ' 1 Selected' and 'Send 1'.

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

Work Order Management

 PRB2010868

</td><td>

Attachments added through questionnaires aren't reflected/updated on the corresponding Work Order Task records

</td><td>

 

</td><td>

1.  Create a new attachment-type question in a questionnaire.
2.  Assign the questionnaire to a user.
3.  Log in to the Mobile Agent application.
4.  Start work on the Work Order Task.
5.  Select **Take Questionnaire**.
6.  Complete the questionnaire, including adding attachments.
7.  Check the platform record for the Work Order Task.

 Observe that the attachments aren't reflected or updated.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 1](australia-patch-1.md)
-   [Australia EA Hotfix 1](https://www.servicenow.com/docs/r/release-notes/australia-patch-0-hf-1-PO.html)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


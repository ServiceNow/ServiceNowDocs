---
title: Zurich Patch 12m
description: The Zurich Patch 12m release contains important problem fixes via Zurich Patch 12 and updates to compatible ServiceNow Store applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zp12m-release-notes.html
release: zurich
topic_type: reference
last_updated: "2026-09-03"
reading_time_minutes: 291
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 12m

The Zurich Patch 12m release contains important problem fixes via Zurich Patch 12 and updates to compatible ServiceNow Store applications.

-   **Zurich Patch 12m was released on September 03, 2026.**
    -   Build date: 09-01-2026\_1221
    -   Build tag: glide-zurich-07-01-2025\_\_patch12m-08-07-2026

## Monthly "m" releases

Monthly "m" releases are now available for your ServiceNow AI Platform® instances. These releases, which are identified by an "m" in the release name, contain everything from the base family patches, the latest version of all AI applications, and those apps' supporting non-AI application dependencies.

**Important:**

This ServiceNow AI Platform® release is not available for ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in the Zurich Patch 12m release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z12m.00.xlsx).

## Overview

Zurich Patch 12m includes 394 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-zp12.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Zurich Patch 12m includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 12m, refer to [KB3151401](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3151401).

## Changes in Zurich Patch 12

-   **[Configure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure.md)**

    Configure Dynamic Guidance to be available in the Help Center and Now Assist panel. When sn\_dyn\_guidance\_user role is assigned, it also includes the genai\_admin role.

    **Note:** The genai\_admin role does not grant administrative privileges.

-   **[Using Dynamic Guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/using-dynamic-guidance.md)**

    Learn how to invoke Dynamic Guidance and use it effectively to enhance your experience. Starting with Dynamic Guidance version 28.4.3, the genai\_admin role is automatically included when the sn\_dyn\_guidance\_user role is assigned. The genai\_admin role does not grant administrative privileges.


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

AI Search for Service Portal

 PRB2038055

 [KB3139447](https://hi.service-now.com/kb_view.do?sysparm_article=KB3139447)

</td><td>

The Now Assist Self Service widget breaks the full page experience search in portal

</td><td>

After upgrading to Zurich, when the user searches from the Employee Center portal, the full page experience fails and no results are displayed. Instead, the widget throws a server-side JavaScript error: '$sp is not defined'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB2058369

 [KB3140571](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140571)

</td><td>

Midserver is unable to fetch credentials after upgrading to Zurich or Australia

</td><td>

In certain versions, there's a Unified Secrets Gateway \(USG\) service for credential management. During the upgrade to those versions, a system trigger script is designed to automatically execute and populate the sys\_​secret\_​identity \_​group\_​member table with the MID Server identity group mappings required for USG authentication. However, this trigger fails to complete successfully, leaving the table incompletely populated. As a result, the MID Server can't authenticate with USG and fails to retrieve credentials.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now User Experience

 PRB2038702

 [KB3134148](https://hi.service-now.com/kb_view.do?sysparm_article=KB3134148)

</td><td>

A scoped public UI page isn't accessible without a login unless 'Name' is used vs a scoped endpoint in a sys\_public record

</td><td>

It should be accessible without a log in, so a user can complete the authentication from Outlook.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Events

 PRB1969068

</td><td>

The 'Events process 0' job yields to memory pressure, causing event processing delays

</td><td>

When node memory pressure is high \(live set ≥ ~91%\), the JobYieldCheck mechanism triggers a yield on events process 0 despite it being a priority 25 \(high priority\) job. High-priority jobs should not be subject to automatic yield throttling, as this directly delays critical event processing and can result in P1 incidents. The memory pressure itself may be transient or difficult to diagnose quickly — heap dumps often show no obvious culprit, and identifying the root cause of elevated memory usage takes time. During that window, events process 0 is repeatedly yielded, stalling event processing pipelines that users depend on for time-sensitive operations. JobYieldCheck WARNING Job=events process 0 yields due to memory pressure logged on affected nodes. Node memory is sustained at 91–93% of max, with live set at ~91.44% \(~1.28GB\). Glide.memory.watcher logs no active transaction warnings alongside persistent memory pressure status = true. There's only a single job visible in the queue during the yield window, yet throttling still triggers. However, users expect priority 25 jobs \(events process 0\) should not be yielded under memory pressure conditions. Yield throttling should be restricted to lower-priority workloads.

</td><td>

 

</td></tr><tr><td>

Table Rotation

 PRB1959672

 [KB3071677](https://hi.service-now.com/kb_view.do?sysparm_article=KB3071677)

</td><td>

Shard tables aren't created on an initial plugin install

</td><td>

When a plugin is manually installed, shard tables aren't created automatically.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB2027095

 [KB3102030](https://hi.service-now.com/kb_view.do?sysparm_article=KB3102030)

</td><td>

The latest component asset isn't selected when multiple asset associations exist in sys\_​ux\_​lib\_​ component\_​m2m\_​asset,​ which impacts AI summary cards on UI Builder workspaces

</td><td>

When the AI summary card component was upgraded, its asset name changed from now-ai-summary-card/index to uxc-generative-ai/index. The upgrade doesn't clean up the old asset association, so the sys\_ux\_lib\_ component\_m2m\_asset table ends up with two associations for the same component \(old and new asset\). The component-to-asset selection query in Glide​Ux​Component​Def​Provider .​get​Asset​Names​By​Component​Sys​Ids\(\)​ had no ordering and relied on default DB ordering. When duplicate associations exist, this could return the stale now-ai-summary-card/index asset, which is incompatible with the latest Platform AI Agents and Skills app. As a result the AI summary card fails to load on UI Builder workspaces. Classic UI uses a different rendering path, so it is unaffected.

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

 PRB1991852

</td><td>

Base64 coded attachments can't be loaded in the activity stream in the workspace

</td><td>

This likely has to do with processing large content.

</td><td>

1.  Navigate to any record page.
2.  Create an email with a base64 encoded image.
3.  Set the email to 'sent' status.
4.  Navigate to the record and select **Show more** for the email.

 Expected behavior: The full body of the email is displayed.

 Actual behavior: The email is loading for a long time and eventually crashes the page.

</td></tr><tr><td>

Activity Stream

 PRB2040417

</td><td>

The **Copy** button on the VTB view can't access copyJournalContent or GlideUIDefault

</td><td>

The content doesn't get copied to the clipboard API and doesn't show the 'Copied to clipboard' notification.

</td><td>

1.  On any instance, navigate to **All** &gt; **Visual Task Boards**.
2.  Create a Freeform Board.
3.  Add a card on the newly-created board.
4.  Open the card and add a work note or comment.
5.  Select the **Copy journal content** button.

 Expected behavior: The content is copied to the clipboard API and shows a 'Copied to clipboard' toast.

 Actual behavior: The content doesn't get copied to the clipboard API and doesn't show the 'Copied to clipboard' notification.

</td></tr><tr><td>

Agent Chat

 PRB2021594

</td><td>

An agent chat box isn't enabled when work is offer re-routed post blind queue transfer

</td><td>

In most recent Australia release, the CSM Workspace agent isn't able to type messages in the chat input box after they are re-routed an interaction that was rejected by a previous agent. The chat box should be enabled after re-routing acceptance.

</td><td>

 

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

 PRB2051353

</td><td>

Agent presence indicator should be shown in the 'Transfer to Agent' list for third party

</td><td>

When searchTargetList is set, a list of agents is shown, but there's no presence indicator.

</td><td>

1.  Create and offer a third-party messaging interaction to a CSM Agent.
2.  Select the **Transfer to Agent** quick action.

 Expected behavior: It shows a list of agents along with presence indicator when searchTargetList is set.

 Actual behavior: It shows a list of agents with no presence indicator when searchTargetList is set.

</td></tr><tr><td>

Agent Chat

 PRB2052028

</td><td>

Integration users can't read sys\_cs\_conversation\_member for creating wrap-up segment

</td><td>

The wrap-up segment creation fails with a 400 status and the error message: 'Failed to create wrap-up segment. Segment not found in implementations for extension point: interactionSegment'.

</td><td>

1.  Create a third-party messaging interaction.
2.  Offer to a CSM Agent.
3.  Call REST API to create a wrap-up segment for that interaction and agent.

 Expected behavior: The wrap-up segment is created and the API returns success.

 Actual behavior: The wrap-up segment creation fails with a 400 status and the error message: 'Failed to create wrap-up segment. Segment not found in implementations for extension point: interactionSegment'.

</td></tr><tr><td>

Agent Chat

 PRB2055561

</td><td>

Rename Now Assist, Moveworks and AI experience to ServiceNow Otto

</td><td>

The **Sparkle** button for CRR should be replaced with the new **Otto** button. **CRR** button's tooltip 'Write with Now Assist' should be replaced with 'Write with AI'. Finally, the **Sparkle** icon and its label in the recommendation modal should be replaced with the **Otto** icon.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2058031

</td><td>

Add a missing flag on 'Requires ACL authorization'

</td><td>

A fix has ensured that the 'Requires ACL authorization' flag on 'Conversation Server' graphQL schema is set to true. However, due to a discrepancy in syncing branches, only the ACL changes added are live and not the graphQL schema changes.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2063949

</td><td>

Some messages are hidden on the agent's side when hideControl is true and contains searchText

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2034699

</td><td>

GenAIMetadataM2MDaoImpl createAIAGenAIMetadataM2M doesn't assert that the genAILogId parameter is not NULL

</td><td>

This causes a full table scan of the sys\_gen\_ai\_log\_metadata table. This code is invoked by the AsyncMessageProcessor.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2037758

</td><td>

AI Agents randomly throw a tool execution error: 'Failed to execute async FDIH tool'

</td><td>

At any random tool call, the AI Agent throws: 'Sorry, there was a problem on my side trying to complete this request. Try asking again later'. In logs, it shows 'FDIH async tool call exception'.

</td><td>

1.  Log in to an instance.
2.  Invoke the Quote AI agent.
3.  Input a multi-paragraph, conversational prompt.

 Observe that, at any random tool call, it throws: 'Sorry, there was a problem on my side trying to complete this request. Try asking again later'. In logs, it shows 'FDIH async tool call exception'.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2051367

</td><td>

TTL isn't honored in sys\_​og\_​conversational \_​cache\_​configuration in the absence of any other invalidation rule

</td><td>

The persona section doesn't show the new memories immediately, but they're visible after 24 hours.

</td><td>

1.  Set up LTM extraction on Glide \(enable sys\_prop use\_new\_ltm\).
2.  Set up DARE with memory enabled \(in pipeline.yaml, set enable\_user\_persona\).
3.  Create a conversation with some details that are a candidate for LTM extraction \(for example, 'I like cycling'\).
4.  Verify that memories are extracted \(the ltm job runs every hour\).
5.  After new memories have been extracted, check the persona section.

 Observe that it doesn't show the new memories. However, they will be visible after 24 hours.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2059351

</td><td>

Record scope should override the user session scope

</td><td>

For AI Agents, when any record of a user instance is used, the record scope should override the user session scope of the MSP as per the domain separation policy. However, that's not happening. For example, when an AI Agent with a retriever tool is triggered by any record in a user instance \(like C1\), it fetches KBs/results from all the user instances under that MSP.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2059390

</td><td>

Role masking isn't unset when running a workflow

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2061584

</td><td>

True-up the AI UX Builder Store app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Gateway - Security

 PRB2052119

</td><td>

As part of the name change, update error strings in MCPOAuthConstants.java that reference 'Now Assist' to 'ServiceNow Otto'

</td><td>

The changes will be made in Zurich and Australia. Also, an additional change is needed for the description in glide/glide-ai-security-scan.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2052168

</td><td>

No\_answer Genius Result is streamed intermittently

</td><td>

A Genius Result rarely shows, but it should not show at all.

</td><td>

1.  Navigate to /sp.
2.  Search for something that gives a no\_answer result, like 'baseball world series'.

 Observe that a Genius Result rarely shows. It should not show at all.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2054276

</td><td>

The fix script shouldn't backfill non-default sources

</td><td>

When the user upgrades to an instance with additional sources in the multi-content feature, the additional sources are marked as 'Included'.

</td><td>

Upgrade an instance without additional sources in the multi-content feature to a version with the feature.

 Observe that the additional sources are marked as 'Included'.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2054932

</td><td>

In Moveworks API V2, support linking ServiceNow Security Center \(SSC\) to a search profile

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2054938

</td><td>

For the Moveworks API V2, return chunks when passing an additional flag

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2058047

</td><td>

Indexing with multiple semantic indexing configurations with the same name on different models isn't working

</td><td>

When multiple semantic index configurations are created on the same datasource with the same semantic field name but different embedding models, only the first configuration is loaded into the active semantic index field cache. Subsequent configurations are silently ignored, so ingestion and search only use one embedding model for that field. Only one embedding model is used for indexing and search when multiple semantic index configurations share the same semantic field name. Additional configurations with the same semantic field name aren't visible in get​Semantic​Index​Field​Mapping\(\)​.​ No error or warning is logged when the duplicate-name configurations are skipped. Thus, multi-embedding model support for a single semantic field is broken. Configurations are silently lost during cache population. This affects ingestion, search, and any callers that rely on get​Semantic​Index​Field​Mapping\(\)​.​

</td><td>

1.  Create two active ais\_​semantic\_​index\_​configuration records on the same datasource with the same semantic\_field\_name but different embedding\_models values.
2.  Add valid component fields via ais\_semantic\_component\_field for each record.
3.  Set a valid semantic\_​snippetization\_​configuration.​
4.  Flush the datasource object cache \(Ais​Configuration​Cache​Manager .​flush​Datasource​Object​Cache\(\)​\)​.​
5.  Call Ais​Configuration.​get\(\)​.​ get​Semantic​Index​Field​Mapping \('kb\_​knowledge',​'kb\_​knowledge'\)​.​

 Observe that only one SemanticFieldConfiguration is returned for semantic\_search and the other is silently dropped.

</td></tr><tr><td>

AI Search

 PRB1875924

 [KB3137872](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137872)

</td><td>

AI search ingestion sticks when the 'Size in Bytes' column has an empty value in sys\_attachment for an attachment that has a size more than 25MB

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1902419

</td><td>

The conversation ID isn't logged to the sys\_search\_event table

</td><td>

 

</td><td>

1.  On an AI Search-enabled instance, start a new chat with Virtual Agent \(VA\).
2.  Enter 'what is spam'.
3.  Flush queued signals.
4.  Open the sys\_search\_event table, and if necessary, add the **Conversation ID** field to the list/form.

 Expected behavior: Since it was from VA, there should be a conversation.

 Actual behavior: The conversation ID is empty.

</td></tr><tr><td>

AI Search UX

 PRB2004411

</td><td>

Refactor the synthesized Genius Result presence filter from Data Broker into the Java layer

</td><td>

Currently, the logic to conditionally execute the synthesized Genius Result — specifically, the filter that checks whether a Genius Result is present before execution — lives in the Data Broker transform layer \(UX layer\). This means the filter isn't automatically applied across all clients and must be manually maintained per-client in the Data Broker. This logic must be moved into the Java layer so that it is applied universally and automatically for all users, reducing duplication and the risk of inconsistent behavior across different consumers of the Search API.

</td><td>

1.  Review the Data Broker transform at sys\_ux\_data\_ broker\_transform\_ 0c735fb4530422104 accddeeff7b12dd.xml\#L44.
2.  Check the conditional filter that gates execution of the synthesized Genius Result on its presence.
3.  .

 Notice that this filter only applies to clients using this specific Data Broker transform; it isn't enforced at the Java/API layer. A user that bypasses or doesn't use this Data Broker transform doesn't have the filter applied, resulting in potentially inconsistent or unintended behavior around synthesized Genius Result execution.

</td></tr><tr><td>

AI Search UX

 PRB2014714

</td><td>

Ignore Genius Result's limit for citations in sync mode

</td><td>

 

</td><td>

1.  On an AI Search enabled instance with synthesized response configured for portal, navigate to a portal.
2.  Complete a query that yields a synthesized response.
3.  Set the system property 'glide.​ais.​query.​disable\_​async\_​mode' to true.
4.  Do same search in portal.

The user should still get a synthesized response.

5.  Open the search application \(presumably NAVA\) and set the Genius Result limit to one.
6.  Do the same search in portal.

 Expected behavior: Users still get a synthesized response.

 Actual behavior: No Genius Result renders because of no citations.

</td></tr><tr><td>

AI Search UX

 PRB2038703

</td><td>

Instance creation failure for com.​glide.​search.​ graphql.​query.​Suggestions from service portal's typeahead AIS Suggestions API

</td><td>

When something is searched for in the portal's typeahead, no suggestions appear and AIS Suggestions API calls in the network tab return 'Instance creation failure for: com.​glide.​search.​ graphql.​query.​Suggestions',​ and 'DataFetchException'.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2054213

</td><td>

URLs with special characters like $ break streaming for non-VA clients

</td><td>

Streaming starts successfully, but it stops partway through and the full answer is never rendered.

</td><td>

1.  Open an AIS-enabled instance.
2.  Make sure 'Synthesized Response' is enabled in portal.
3.  Navigate to the portal with Now Assist enabled.
4.  Search for 'How can I reset my password?'.

 Expected behavior: The full answer streams successfully.

 Actual behavior: Streaming starts successfully, but it stops partway through and the full answer is never rendered.

</td></tr><tr><td>

AI Search UX

 PRB2054952

</td><td>

Rename Now Assist to Otto within AI Search components

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2056856

</td><td>

Replace the **Sparkle** icon animation with the Otto animation for synthesized genius results \(GR\)

</td><td>

 

</td><td>

1.  Open an instance with multi-content GR configured.
2.  Navigate to portal/global search.
3.  Search for a query that returns a synthesized GR.
4.  Check the loader in the GR component when the loading state is showing.

 Expected behavior: The loader state shows the Otto animation.

 Actual behavior: The loader state shows the **Sparkle** icon animation.

</td></tr><tr><td>

AI Search UX

 PRB2057349

</td><td>

Rename Now Assist to Otto for typeahead suggestions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2073716

 [KB3148324](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3148324)

</td><td>

For non-admin users, search results and suggestion navigation on portals are redirecting to platform view

</td><td>

After upgrading to Australia Patch 5 or Zurich Patch 12, non‑admin users performing a search on a portal \(for example, /esc\) experience incorrect navigation. Selecting a regular search result or a suggested search result opens the record in the platform view rather than within the portal.

</td><td>

Scenario 1:

 1.  Upgrade an instance to Australia Patch 5 or Zurich Patch 12.
2.  Log in as a non‑admin user.
3.  Perform a search on a portal, such as /esc or /sp.
4.  Select the regular search result that is returned.

 Observe that the record opens in platform view instead of the portal.

 Scenario 2:

1.  Upgrade an instance to Australia Patch 5 or Zurich Patch 12.
2.  Log in as a non‑admin user.
3.  Enter a search term on a portal, such as /esc or /sp, without submitting the search.
4.  Select a suggested search result in the typeahead drop-down list.

 Observe that the record opens in platform view instead of the portal.

</td></tr><tr><td>

Analytics Data API

 PRB2039649

</td><td>

The Platform Analytics dashboard ignores the data source filter

</td><td>

The 'Is one of' operator doesn't function as expected on the source. The issue is reproducible in Australia with the Data Visualization plugin version 29.1.0 and in Zurich with version 28.5.0. However, the functionality works as expected in Yokohama with version 28.0.29 and in Zurich with version 28.4.5.

</td><td>

1.  Open an instance.
2.  Create an indicator scorecard visualization.
3.  Select **Number of Incidents** as the data source.
4.  Apply a source condition using the 'Is one of' operator.
5.  Select the required priority values.

 Expected behavior: Only the selected priority is reflected.

 Actual behavior: All priorities are reflected in the indicator scorecard visualization.

</td></tr><tr><td>

Analytics Export API

 PRB2021342

</td><td>

The email layout in an Platform Analytics scheduled export doesn't match the received email format

</td><td>

Platform Analytics scheduled reports aren't honoring the email body configured when the field **omit\_if\_no\_records** is true.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB2056922

</td><td>

Install engine reads the dependencies from package.json with a fall back to the previous way when not available

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB2022268

</td><td>

The application manager sys\_app\_version displays duplicate records for the same application and version, which is causing the app to be 'Installation blocked'

</td><td>

As part of the AI testing, it's been observed that the app installations are blocked. The sys\_app\_version displays duplicate records for the same application, which is causing the app installations to be blocked, despite the app versions being available as well as the license checks having successfully completed.

</td><td>

1.  Navigate to an instance.
2.  Navigate to App Manager.
3.  Open any app \(for example, sn\_ai\_itsm\_cont\) which is licensed and validated on CI \(usageanalytics\) prod, but has yet showed 'Not Licensed'.
4.  Select **Install**.
5.  It just fails with 'Installation blocked' on that app itself.
6.  Open sys\_app\_version table.
7.  Check the app/scope id.

 Expected behavior: It should have only one record for that app and a specific app version.

 Actual behavior: It has multiple records for the same app and app version.

</td></tr><tr><td>

Application Manager

 PRB2057729

 [KB3140027](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140027)

</td><td>

Users can't publish custom-scoped applications after upgrading to Zurich or Australia

</td><td>

After upgrading to Zurich or Australia, there's an issue that prevents new application versions from being published for custom scoped apps in ServiceNow Studio. Selecting the **Publish** button for any custom application results in a publish failure with one of the following errors: 'Vendor information was not found, upload function is disabled for this instance' or 'Did not receive publishing information successfully. Cannot read properties of undefined \(reading 'toString'\)'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Rationalization

 PRB1977007

</td><td>

Generate Assessment takes too long to load because of excessive sys\_user\_group records

</td><td>

The issue occurs when there are a lot of records in the sys\_user\_group table. The sn\_apm.Assessment AjaxProcessor script include calls the getInitData method, which contains some code that queries all sys\_user\_group records. There is no limit, so instances with many sys\_user\_group records may encounter the following issues: first, excessive memory usage by the userGroupRecords object, causing node performance issues and even a node restart. Second, excessive payload returned by the function to the application node and eventually to the client browser, causing slowness.

</td><td>

 

</td></tr><tr><td>

Asset Management Common

 PRB1982019

</td><td>

Service locations on stockroom aren't added through the MRA pop-up

</td><td>

The success message is shown, but records aren't added under the related list.

</td><td>

1.  Log in to an instance.
2.  Navigate to the stockroom record in workspace.
3.  Select the **Service Locations** related list.
4.  Select the **Add** button.
5.  Select two locations in the MRA pop-up.
6.  Select **Add**.

 Expected behavior: Locations are added under Service Locations.

 Actual behavior: Locations aren't added under Service Locations.

</td></tr><tr><td>

Authentication Factors

 PRB2037251

</td><td>

Update interactions post-identification and authentication

</td><td>

The 'Interactions' table has only 'Guest' resolved. It should have the user reference resolved post-identification and authentication.

</td><td>

 

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

 PRB1942035

</td><td>

sn\_cicd API for test run doesn't start the test in cloud runner when run\_in\_cloud is set to true

</td><td>

The test remains in the waiting state until a scheduled client runner is opened. It fails after waiting for ten minutes due to timeout. No record is found in sn\_atf\_tg\_sn\_boq for the test run submitted.

</td><td>

1.  Open an instance with ATF Cloud runner enabled.
2.  Log in as admin.
3.  Navigate to REST API Explorer.
4.  Navigate to namespace: sn\_cicd and API name: CICD ATF Test Execution API.
5.  Select **Start a ATF, given a test ID** to open the API to run a test
6.  Enter the test\_sys\_id of any UI based test.
7.  Enter run\_in\_cloud = true.
8.  Leave is\_performance\_run as blank.
9.  Submit the request.
10. Navigate to the test page for the sysID.
11. Check the 'Test Results' tab.
12. Open Browser Orchestration Queue \(sn\_atf\_tg\_sn\_boq\).
13. Look for the record created for the test run.

 Expected behavior: The test run should be queued in sn\_atf\_tg\_sn\_boq. The test should run in cloud and complete.

 Actual behavior: The test result shows 'Waiting'. The test remains in the waiting state until a scheduled client runner is opened. It fails after waiting for ten minutes due to timeout. It's also not queued in Browser Orchestration Queue. No record is found in sn\_atf\_tg\_sn\_boq for the test run submitted.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2017949

</td><td>

There's stuck execution trackers due to Automated Test Framework \(ATF\)'s new feature metadata tracing

</td><td>

For invalid metadata table names in sys\_traced\_metadata records, the generateMissingPayloadHashes throws an error and causes the final payload hash calculation execution trackers to be stuck.

</td><td>

1.  Ensure that metadata tracing is on.
2.  Run a test on a table with a long name \(such as 'sys\_og\_conversational \_cache\_configuration', more than 40 characters\).

 Observe that the sys\_traced\_metadata records truncate the long table name \(sys\_traced\_metadata records save table names up to 40 characters whereas metadata table names can be up to 80 characters in length\). Observe at the end of the test, there's stuck sys\_execution\_trackers while generating payload hashes for the sys\_traced\_metadata records because the truncated metadata table name is invalid. It thus throws an error.

</td></tr><tr><td>

Canonicalization Data Services \(CDS\)

 PRB2053470

</td><td>

Data uploaded to cds\_server\_staging table is blocked within instances

</td><td>

This issue occurs in instances where the property 'glide.cmdb.canonical.URL' is set to https:​/​/​&lt;instance\_​name&gt;​.​service-​now.​com/​ and ends with '/'. Unfortunately, that is the base instance value, and it affects the upload portion of CDS.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2035924

 [KB3093597](https://hi.service-now.com/kb_view.do?sysparm_article=KB3093597)

</td><td>

Standard changes created from a problem aren't linked to the parent task

</td><td>

The issue is reproducible if users clear the 'Two step' checkbox under **Change** &gt; **Administration** &gt; **Standard Change Properties** and then perform **cache.do** &gt; **Clear Cache**. A standard change created from a task \(incident/problem\) aren't linked to a parent task. If users check conflicts before saving a child change from a project requested item, it won't attach the change to the parent item.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2053039

</td><td>

In the 'Change risk assessment' answer generator skill flow, replace the Now Assist terminology with Otto rebranding

</td><td>

The suggestion message should contain 'Check answers generated by AI for accuracy'.

</td><td>

1.  Navigate to **SOW** &gt; **Change Request**.
2.  Select **Assess Risk** in the 'Overview' tab.
3.  Select **Generate Answers**.
4.  Wait until risk assessment completes answer generation.
5.  Open risk assessment.

 Observe that the suggestion message doesn't contain 'Check answers generated by AI for accuracy'.

</td></tr><tr><td>

Client Scripts

 PRB1956934

</td><td>

g\_form.getActionName returns 'none' when adding a file in a **File Attachment** field

</td><td>

 

</td><td>

1.  Create an OnSubmit client script for incident table.
2.  Add a **File Attachment** field in the incident form.
3.  Select **Click to add...** in the **File** **Attachment** field.

 Observe that g\_form.getActionName returns 'none'.

</td></tr><tr><td>

Condition Builder

 PRB2054935

</td><td>

Create a sys property to determine the Glide version for condition builder

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1994587

</td><td>

A race condition between IRE LazyWriter and Deletion Strategy causes the configuration item \(CI\) state to flip incorrectly

</td><td>

A CI's state is flipping from installed to stale during Discovery \(delete strategy execution\). A race condition occurred between IRE's asynchronous batch update of the **last\_discovered** field using 'db.executeLazy\(\)' and the execution of the Deletion Strategy. The LazyWriter delay caused the Deletion Strategy to process stale 'last\_discovered' values, marking valid CIs as retired despite their presence in the payload.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2017559

</td><td>

The health configuration cache is ineffective due to a shared cache eviction

</td><td>

The getHealthConfiguration\(\) method in HealthConfigManager.java is not getting effective cache hits. The current implementation caches per \(metricSysId + className + domainId\) key, creating a few hundred cache entries. Since this is a shared cache, entries get evicted before they can be reused, resulting in repeated DB queries for records that never change during processing.

</td><td>

1.  Create health configuration rules and observe the cache entry through cache\_inspect.do.
2.  Create a pressure on the system to cause cache eviction.

 Observe in the code path that the cache is rebuilt every time there is an eviction. The caching path is controlled via sys\_property and only applies to the non-domain path.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2020295

</td><td>

INSERT\_NOT\_ALLOWED\_FOR\_SOURCE incorrectly classified as a partial error causes the cmdb\_ire\_partial\_payloads table to bloat and an out of memory \(OOM\) error

</td><td>

When an IRE data source rule blocks inserts for a class and data source, affected records are incorrectly saved as partial payloads. Since the block is permanent, these partial payloads can never complete — each retry creates a new entry, causing the cmdb\_ire\_partial\_payloads table to grow unboundedly. If the partial payload contains a large number of related or lookup items, this can also lead to OOM on app nodes.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2021367

</td><td>

Implement totals calculation for the group view when applying a class filter qualifier configuration

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2030304

</td><td>

OrphanProcessor skips CIs and reprocesses records after batch timeouts due to unordered HashMap iteration

</td><td>

When the CMDB Health orphan metric job times out MID-run on large datasets, it saves an incorrect resume position and silently skips CIs on the next run. As a result, orphan CIs appear healthy in the dashboard even though they are actual orphans, leading to inaccurate health scores.

</td><td>

1.  Set up a class with a large enough population of orphan CIs such that processing exceeds five minutes.
2.  Trigger the CMDB Health orphan batch job.
3.  Allow the job to run until the five-minute batch timeout fires MID-loop.

 Observe the checkpoint value stored in MetricProcessorStatus for that class — it's an arbitrary sys\_id, not the lexicographically highest one processed. On the next scheduled run, observe that orphan CIs with sys\_ids smaller than the stored checkpoint aren't evaluated and not reported as failures.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2052583

</td><td>

References to 'Now Assist' for the duplicate CI remediator should be renamed to Otto

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2055214

</td><td>

AI should be used to suggest options for de-duplication task/template remediation

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2055216

</td><td>

Related items handling for de-duplication process should be improved

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Contract Management

 PRB2040201

 [KB3140742](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140742)

</td><td>

Assets covered on a contract aren't added through an Multiple Record Associator \(MRA\) pop-up

</td><td>

In the 'add action' over MRA pop-up, there's a slight change by the platform. It is now performing a GlideRecordSecure insert instead of GlideRecord. It is validating for create and write ACLs on **clm\_m2m\_contract\_asset.asset** and **clm\_​m2m\_​contract \_​asset.​contract fields**. There's ACLs where it allows the respective operations only if they are blank. This is clearing out the **Contract** and **Asset** field values during creation. So, records which are created don't have these fields and aren't displaying in the related list.

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB2002976

 [KB3141009](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141009)

</td><td>

An advanced qualifier reference that uses 'current' isn't functioning as expected in CSM Workspace

</td><td>

Advanced reference qualifiers that rely on the 'current' object fail when templates are applied in Workspace. However, the same functionality works as expected in 'Classic UI \(UI16\)'. During template application in Workspace, the platform passes corrupted or incomplete serialized data to 'GlideRecordEncoder.decode\(\)'. As a result, the current GlideRecord is returned without field values.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1884666

</td><td>

TableCleaner. deleteAttachments\(\) has an infinite loop and is unable to delete encrypted records

</td><td>

 

</td><td>

1.  Insert an encrypted attribute into sys\_attachment.
2.  Invoke TableCleaner. deleteAttachments\(\) via a script.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1942731

</td><td>

If sequences exist to reduce redundant queries, SequenceAtomicCounter.get could cache

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2026586

</td><td>

toLower\(\) and toUpper\(\) functions aren't supported in WHERE and RETURN

</td><td>

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferable serialization of the query. Cypher's toLower\(\) and toUpper\(\) functions aren't supported anywhere in the builder — neither in WHERE predicates nor in RETURN projections.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2026589

</td><td>

COUNT\(DISTINCT x\) can't be represented with GraphQueryBuilder API

</td><td>

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferable serialization of the query. Aggregate\('COUNT', x\) only ever emits COUNT\(x\). There's no way to express COUNT\(DISTINCT x\), which is the only correct answer when multiple paths can reach the same node.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2026590

</td><td>

ORDER BY isn't stored in Encoded QueryModel

</td><td>

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferable serialization of the query. RETURN alias — the AS clause is dropped when using buildEncodedQuery\(\), so any consumer of the encoded query has no way to know what column name the user asked for. ORDER BY / LIMIT / SKIP — these have no representation in QueryModel at all, so they're dropped whole on round-trip.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2040734

</td><td>

Sys\_class\_name doesn't come as property from getForTables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2051205

</td><td>

Inline node properties in the cypher are dropped in the encoded query when using with useCypher\(\)

</td><td>

If there are inline properties in the cypher passed to useCypher, the returned encoded query doesn't contain that query.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2052676

</td><td>

Cache flushes are triggered, even when the cache is not used/populated

</td><td>

The number of cache flush messages for the table 'cmdb\_rel\_ci' is in the 80 million+ range every hour. In a way, it's making 80 million inserts into the sys\_cache\_flush table. 'cmdb\_rel\_ci' is paired with 'graph\_cmdb\_rel\_type\_cache'. The cache graph\_cmdb\_rel\_type\_cache isn't enabled, but the cache pairing is still in a static block and is active.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2053774

</td><td>

Support initializing GraphQueryBuilder with a cypher query string via the JavaScript API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Views

 PRB1881428

 [KB2062907](https://hi.service-now.com/kb_view.do?sysparm_article=KB2062907)

</td><td>

A MariaDB database view using INSTR could result in a syntax error when the function is rewritten and executed on RaptorDB

</td><td>

This happens because of a related &gt; 0 or != 0 comparison. When executed on MariaDB, INSTR\(\) returns an integer and the comparison is to an integer. However, on RaptorDB, the rewrite results in a function which returns a boolean. Due to RaptorDB's strong typing semantics, a boolean can't be compared to an integer, resulting in the syntax error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2031271

</td><td>

Rollback of a scheduled anonymization job doesn't refresh the activity stream UI for **Journal** fields \(work\_notes, comments\)

</td><td>

When a scheduled Data Privacy anonymization job is rolled back, the **Journal** field values \(work\_notes and comments\) are correctly restored in the sys\_journal\_field table. However, the activity stream UI continues to display the anonymized values because sys\_activity table \(used by Service Operations Workspace\) and sys\_​history\_​set/​sys\_​history\_​line \(used by UI16 List and Form views\) aren't refreshed upon rollback. The **Description** field doesn't exhibit this issue. This is inconsistent behavior introduced when journal type anonymization support was added.

</td><td>

1.  Open an instance with Data Privacy enabled.
2.  Configure a scheduled anonymization job targeting **Journal** fields \(**work\_notes**, **comments**\) on the Incident table.
3.  Run the anonymization job.
4.  Confirm the fields are masked in both the database and the UI.
5.  Execute a rollback of the anonymization job.
6.  Verify in sys\_journal\_field that the original values have been restored.
7.  Navigate to the affected Incident record in both UI16 and Service Operations Workspace.

 Observe that the activity stream still displays the anonymized values even though the database was reverted.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2039332

</td><td>

Increase the maximum size limit of the incoming request to Data Privacy APIs from 1M to 10M

</td><td>

The Data Privacy API only supports up to 1M character long prompts. However, a simple prompt on Virtual Agent may result in prompts larger than 1M characters, which causes the prompt's response to get stuck. Prompts of extra large size should be processed by the Data Privacy API.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2040595

</td><td>

Post-clone anonymization of child workers is incorrectly cancelled due to parent job type mismatch

</td><td>

The post-clone data privacy anonymization job uses a parent-child architecture; one parent job distributes work to multiple child worker jobs that process tables in parallel. The issue is in how the child workers look up their parent job record. In the post-clone flow, the parent job is stored in a different table type than the child workers' lookup code expects. Because the lookup fails with 'data protection job is not valid,' each child worker is cancelled immediately.

</td><td>

 

</td></tr><tr><td>

Date Picker

 PRB2029576

 [KB3061444](https://hi.service-now.com/kb_view.do?sysparm_article=KB3061444)

</td><td>

There's an issue with GlideDateTime.setDisplayValue

</td><td>

Any script that calls setDisplayValue\(\) with an ISO-format string \(yyyy-MM-dd HH:mm:ss\) on an instance where glide.sys.date\_format is set to anything not in FORMAT\_LIST \(for example, dd-MM-yyyy, MM/dd/yyyy, etc.\) produces incorrect dates in Zurich.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Decision Graph for Context Engine \(Family\)

 PRB2056900

</td><td>

Glide changes for machine learning integration needed for Distinguished Encoding Rules \(DER\) mining

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Decision Graph for Context Engine \(Family\)

 PRB2056902

</td><td>

Instrument 'Ask For' approval action Instance Observer \(IO\) during flow execution for context graph tracing

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Decision Graph for Context Engine \(Family\)

 PRB2056905

</td><td>

Rate-limited flow trace eligibility evaluation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Decision Graph for Context Engine \(Family\)

 PRB2056908

</td><td>

Scaffolding for the decision-graph module

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Decision Graph for Context Engine \(Family\)

 PRB2056910

</td><td>

Cache decision weightage for a low-latency runtime lookup

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Decision Graph for Context Engine \(Family\)

 PRB2056912

</td><td>

Adding or deleting a feature dictionary should make mined patterns inactive

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Declarative Actions

 PRB2055766

</td><td>

The related list UI actions to update rows are failing on m2m if the field being updated is read-only

</td><td>

The UI action calls AssetAutomationAPI. completeAssetDisposalTask. This has current.update, which fails. If the read-only flag is removed from the **Stage** field in the sn\_hamp\_m2m\_ hw \_asset\_disposal table, then it works.

</td><td>

1.  Navigate to **Hardware Asset Workspace** &gt; **Inventory** &gt; **Disposal order**.
2.  Create a disposal order.
3.  Navigate to the related list.
4.  Add an asset to the disposal order.
5.  Open **Verify task** from the related list.
6.  Select the row.
7.  Select **Verify**.

 Observe that the action fails to update.

</td></tr><tr><td>

Developer Sandboxes

 PRB2054240

</td><td>

The scheduler claim mutex \(sys\_mutex\) isn't sandbox-aware and forces DSB nodes to contend for a cluster-wide lock, causing scheduled-job pickup delay

</td><td>

 

</td><td>

1.  On a multi-node instance \(50+ nodes\), turn on Developer Sandboxes.
2.  Create at least 20-30 sandboxes.
3.  Make sure multiple isolated sys\_triggers exist in the sandboxes.
4.  Pull stats.​do?​include=​otel.​scheduler\* on the sandbox's node.

Observe that claim\_lock\_time averages above one second \(expected ~13ms\), jobs\_lateness averaging 300+ seconds, and worker capacity used is very low.

5.  Compare against a controller node on the same instance.

 Observe that claim\_lock\_time is still elevated but jobs\_lateness stays within a few seconds, because base nodes don't pin an entire platform triggers on one node.

</td></tr><tr><td>

Document Management

 PRB2056202

</td><td>

Replace 'Now Assist' and 'Sparkle' with 'ServiceNow Otto' in screenshots, images, and icon assets

</td><td>

All UI visual elements should be updated across SmartDocs, Doc to Voice, and SmartRedact to reflect the ServiceNow Otto branding changes. This includes both images/screenshots and icon assets.

</td><td>

 

</td></tr><tr><td>

Document Management Services

 PRB2039067

</td><td>

Smart redaction with redaction codes and notes for documents

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Management Services

 PRB2056919

</td><td>

SmartDocs enablement in UI16 and ServicePortals

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Viewer

 PRB2056915

</td><td>

Support in document viewer for the doc to voice agent

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB2036855

</td><td>

Agent workspace case emails display multiple 'To' names if the email recipient has multiple contact records

</td><td>

If a contact has more than one contact record in the system \(same email address\), the system displays the names of all the contacts when viewing an email sent to that person on a case.

</td><td>

1.  Navigate to customer\_contact table.
2.  Create multiple contact records with the same name and email address, but a different user ID.
3.  Navigate to CSM workspace.
4.  Create a case.
5.  Add one of the contacts created above as the case contact.
6.  Send an email to that contact.
7.  Open the sent email.

 Expected behavior: Only one contact is displayed in the **To** field.

 Actual behavior: The **To** field lists all the contacts with the same name and email address.

</td></tr><tr><td>

Email Notifications

 PRB2050616

</td><td>

Email client APIs shouldn't be public

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Embedded Help

 PRB2056339

</td><td>

Replace all occurrences of 'Now Assist' text with 'AI' across the Help Center and embedded help

</td><td>

 

</td><td>

1.  Open Help Center or embedded help.
2.  Open a document that was created using AI-generated help.

 Observe that 'Now Assist' text is displayed for AI-generated help articles.

</td></tr><tr><td>

Event Management

 PRB2052731

</td><td>

Remove the step in mixed grouping that allows alerts to join existing groups before the grouping definitions are run in order

</td><td>

The mixed grouping engine handles alerts in two steps. First, it checks whether an alert can join a group that already exists—without following the order the definitions are set up in. After, it goes through all the definitions in their proper order, where it's also allowed to create new groups. The first step disregards the configured definitions order; as a result, an alert can end up in a group created by a lower-priority rule instead of a higher-priority definition. The definition order exists specifically to control which definition gets to group an alert first, so skipping it defeats the purpose of the order. In conclusion, the two-step process should be removed. The mixed grouping engine should go through the definitions once, in order. For each definition, it should allow alerts to either join an existing group or create a new one.

</td><td>

1.  Create two grouping definitions, Definition A and Definition B, with Definition A placed ahead of Definition B in the rule order.
2.  Send alerts A1 and A2 that fit Definition B.
3.  Wait for the grouping job to run.
4.  Create Group B.
5.  Send alerts A3 and A4 that fit both Definition A and Definition B.
6.  Wait for the grouping job to run.
7.  Check which group A3 and A4 end up in.

 Expected behavior: A3 and A4 form a new group created under Definition A, because Definition A comes first in the rule order.

 Actual behavior: A3 and A4 are added to the existing Group B.

</td></tr><tr><td>

Event Management

 PRB2053524

</td><td>

Azure monitor for 'Issue' integration, and UI enhancements in Express List and alert record

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2059346

</td><td>

Flow context gets completed, but the event isn't relayed to playbook engine, so the activity context doesn't get completed

</td><td>

 

</td><td>

1.  Create a playbook with one normal activity \(say instruction\).
2.  Add one optional activity \(instruction\).
3.  In runtime, add six instances of the optional activity.
4.  Start marking the optional activity complete, from the last in the list to the top.

 Observe that the corresponding activity context is in progress, but the flow context gets completed.

</td></tr><tr><td>

Flow Engine

 PRB2062691

</td><td>

Action Fabric flow complexity is insufficient for pricing estimation exercises

</td><td>

The complexity\_bucket attribute contains values grouped into bucket\_0\_10, bucket\_11\_50, and likely no other buckets.

</td><td>

1.  Perform MCP requests on an instance with Action Fabric telemetry.
2.  View the Action Fabric telemetry via Clickhouse or logged data.

 Expected behavior: The exact complexity of the MCP flows are recorded.

 Actual behavior: The complexity\_bucket attribute contains values grouped into bucket\_0\_10, bucket\_11\_50, and likely no other buckets.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2054449

</td><td>

Refactor all occurrences of 'Now Assist' in Flow Designer, Action Designer, and Flow Diagram to 'ServiceNow Otto'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2056022

</td><td>

Otto directive renaming for the call skill step plugin

</td><td>

The plugin name is being changed from 'Now Assist Skill' to 'AI Skill' \(or 'AI Skill Step'\). The step name is being changed from 'Call Now Skill Step' to 'Call AI Skill Step'. Also, the plugin and step description should be updated where applicable.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB2026691

</td><td>

TCP connection establishment and SSL handshake occur every minute

</td><td>

TCP connection establishment and SSL handshake occur every minute even when the health check is skipped under the 150-second threshold. The unnecessary overhead should be remediated.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB2026695

</td><td>

Identify and eliminate duplicate health checks where two Hermes services point to the same Hermes cluster

</td><td>

Normally, it'd be expected that Glide apps would use different bootstraps. Given the special condition, when the Kafka bootstraps are the same, it should avoid the duplicate connections/healthchecks between the two services.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB2052114

</td><td>

Replace the **Sparkle** icon with the Otto Lottie animation in AI and loader experiences

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB2052172

</td><td>

Suppress console statements so browser tools aren't flooded

</td><td>

 

</td><td>

View the 'Theme behavior' console output.

 The console output should only be logged when env = development.

</td></tr><tr><td>

Horizon Empty State Component

 PRB2050333

</td><td>

Update ai-general illustration

</td><td>

The sparkle illustration should use the new Otto logo instead.

</td><td>

1.  Open an instance.
2.  Create an experience in UIB.
3.  Add an empty state component to the stage.
4.  In the config panel, locate the illustration property.
5.  Select **AI general** from the drop-down list.

 Expected behavior: The empty state shows the Otto logo.

 Actual behavior: The empty state shows sparkles.

</td></tr><tr><td>

Horizon Icon Component

 PRB2032851

</td><td>

Add the **Otto** icon to the library

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Create a experience in UI Builder.
3.  Add a now-button-iconic component to the stage.
4.  In the configuration panel, locate the drop-down list for the icon property.
5.  Search for 'sn-sparkmoji-logo'.

 Expected behavior: The new Otto logo is visible.

 Actual behavior: The icon is missing.

</td></tr><tr><td>

Horizon Icon Component

 PRB2050318

</td><td>

Update all **Sparkle** icons

</td><td>

Icons with the Otto logo should be shown instead.

</td><td>

1.  Open an instance.
2.  Create an experience in UIB.
3.  Add a now-button-iconic component to the stage
4.  In the config panel, locate the icon property.
5.  Search for an icon.

 Expected behavior: Icons with the Otto logo are shown.

 Actual behavior: Icons with sparkles are shown.

</td></tr><tr><td>

HR Service Delivery

 PRB1958041

</td><td>

After a Zurich upgrade, LE tasks aren't getting created

</td><td>

During case creation, the system needs to evaluate audience, which includes the creation of lifecycleEventLogger. Inside lifecycleEventLogger, the flow checks whether there is a valid HR case. Due to the restricted query business rules, the system is blocked from accessing the target records and stops when the error is thrown. This causes the 'Evaluate Audience' result to be false and the flow skips that activity creation.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2014389

</td><td>

RCAs are generated for 'Populate Manager Reportee Count Using Eligible Users' and 'Employee​Hub​Org​Chart​ Reportee​Util​SNC'

</td><td>

During nightly test case execution, two RCAs are generated for the new scripts: - sys\_script\_include \_a302f8807873 f250f877079523d275e1 and - sysauto\_script\_ 33a5e72453f7 b210f2ebff c230e5e69d. It is causing test failures.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2021314

</td><td>

The **Cancel** UI action in an HR case checks for 'mandatory' after the case is canceled

</td><td>

The **Cancel** UI action is invoking hr\_CaseAjax.cancelAction\(\). In this function, state and work notes are updated from the server script. Inside the callback function, there's g\_form.save\(\), which checks the mandatory and saves the form. If the data is already saved from the server script, the system shouldn't check the mandatory.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2052205

</td><td>

In Australia and Zurich, RCAs generated in HR Core and HR Employee Relations need to be added back to track/HR

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2052632

</td><td>

The **header\_config\_\*** fields are missing from the sn\_hr\_core\_service table in Zurich and Australia

</td><td>

 

</td><td>

Open a Zurich or Australia instance with the sn\_hr\_core and EC Core plugins installed.

 Observe that the **header\_config\_\*** fields are missing from the sn\_hr\_core\_service table.

</td></tr><tr><td>

Identification and Reconciliation API

 PRB2028002

</td><td>

Fix three dynamic IRE UI messaging and wording issues and the system properties in the update folder

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Identification and Reconciliation API

 PRB2034883

</td><td>

Users can add or edit identification rules for hardware's child classes while dynamic IRE is enabled

</td><td>

If dynamic IRE is enabled, users shouldn't be able to see or edit identification rules on the hardware hierarchy.

</td><td>

1.  Enable dynamic IRE.
2.  Navigate to hardware or any of the child classes.

 Observe that static rules are displayed and editable, even though dynamic IRE is enabled.

</td></tr><tr><td>

Identity

 PRB1964703

</td><td>

A federated ID isn't generated for all the users in the instance

</td><td>

There's also instances where a federated ID isn't generated for some users even when they have a unique user\_name and email.

</td><td>

 

</td></tr><tr><td>

Install Base Management Store

 PRB2059577

</td><td>

Install base items and sold products should support RAC fallback mechanism

</td><td>

The functions \_skipFetchEntities and getQRfallbackRoles should be overridden in CSMRelationshipServiceSNC in CSMRelationshipService \_InstallBaseRelatedParty to allow this fallback mechanism.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1940978

</td><td>

There's many IDR-DCTComparisonJobs on an instance

</td><td>

This is likely only a cosmetic issue and not hurting performance. Instances have at least one IDRDCTComparisonJob per node, which seems excessive. For instances with many nodes, this ends up being the majority of IDR jobs. There's only a few consumer jobs per instance \(not per node\).

</td><td>

1.  On an instance running a version lower than Australia and configured with multiple nodes, open the sys\_trigger table.
2.  Check if there's multiple IDRDCTComparisonJob records present.

</td></tr><tr><td>

Integrated Email Client

 PRB2051938

</td><td>

A Now Assist reference in Email Client must be changed to Otto

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB2056938

</td><td>

Rename the 'Now Assist for Spoke Generation API Support' Glide plugin

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub Spokes

 PRB2053392

</td><td>

Users can recover box webhook HMAC signing keys via timing oracle on JavaScript == comparison and forge events to trigger arbitrary subflows

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Center

 PRB2076447

</td><td>

The Auto-fix plugin update blocks the Australia Patch 5m upgrade in loadsim release testing

</td><td>

The plugin upgrade thread handling becomes stuck in an error loop triggered by a null pointer. It never exits or advances, leaving the upgrade 'hung'. This happens when the upgrade plugin loader reaches the knowledge center update that adds in the auto-fix and auto-fix enable property.

</td><td>

 

</td></tr><tr><td>

Knowledge Graph \(Family\)

 PRB2016914

</td><td>

Update the structure to keep the Knowledge Graph configuration file in the same folder as the released description version and dynamic configuration for the Install Server URL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Graph \(Family\)

 PRB2052948

</td><td>

Implement batch insert logic for affinity jobs to improve insert latency

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2054012

</td><td>

Rename app-common 'Now Assist' to Otto

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2054937

</td><td>

True up Store apps NAKM, KC, KCInWorkspaces and ECE

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2058947

</td><td>

Update versions for the base instance Knowledge Management apps to include Australia and Zurich fixes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2060905

</td><td>

Updating versions for the base instance Knowledge Management apps to include Australia and Zurich fixes

</td><td>

There are fixes in app-knowledge-center, app-knowledge-gen-ai, app-kb-uib, and sn-enhanced-content-editor.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1963197

</td><td>

The **Duration** field displays '0 seconds' in a Core UI list when the value is null

</td><td>

 

</td><td>

1.  In Zurich, navigate to any table list view that contains the **Duration** field.
2.  Filter by '&lt;DURATION\_TYPE\_FIELD&gt;' is 'Empty'.

 Review that records have '0 seconds' even if there's no value in the records \(empty\).

</td></tr><tr><td>

List Administration

 PRB2044745

</td><td>

Now-record-list-connected sends encodedRecord as \{\} instead of ''

</td><td>

The variables contain 'encodedRecord': \{\} \(empty object\). It's treated as a non-empty, non-nil value, so the advanced qual is evaluated against an empty 'current' and wrong/empty results are returned. This is reproducible across base instances, but works correctly in Classic UI16.

</td><td>

1.  In a workspace \(for example, CSM/incident\), open an incident record.
2.  From the right sidebar, select **Create Template**.
3.  Select **+** to add a field.
4.  Add a reference field that uses an advanced/dynamic reference qualifier referencing the 'current' object.
5.  Open the picker \('Search for Record'\).
6.  Inspect the getReferenceListLayout / now​Record​List​Connected​Reference GraphQL call.

 Expected behavior: EncodedRecord is '', so the advanced/dynamic qualifier is correctly skipped when no 'current' is available. This matches the UI16 template behavior.

 Actual behavior: The variables contain 'encodedRecord': \{\} \(empty object\). It's treated as a non-empty, non-nil value, so the advanced qual is evaluated against an empty 'current' and wrong/empty results are returned.

</td></tr><tr><td>

List Administration

 PRB2053781

</td><td>

The new AI list badge in UI16 breaks list cell content wrapping

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2054941

</td><td>

Additional tags features should be supported

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

List AI Indicators

 PRB2051786

</td><td>

The horizontal scroll for AI-tagged items in the groupedBy list is broken

</td><td>

When the user scrolls to the right, the field isn't visible.

</td><td>

 

</td></tr><tr><td>

List AI Indicators

 PRB2055051

</td><td>

Update the Otto indicators in seismic workspace lists

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List AI Indicators

 PRB2055052

</td><td>

Update the Otto indicators in UI16 lists

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2063491

</td><td>

'LinkedHashMap$Entry' objects connected to the LRU take a couple MB

</td><td>

These objects are from 'ecc\_​queue\_​authorization\_​policy'.​

</td><td>

1.  Open a local instance.
2.  Connect to the MID Server.
3.  Create a heap dump.

 Notice that entries of 'LinkedHashMap$Entry' for ecc\_queue\_authorization\_policy have over 3MB for each entry.

</td></tr><tr><td>

Mobile Platform

 PRB1965358

</td><td>

Scripted screen questionnaire dependencies between fields stop working because of irrelevant evaluations using toString\(\)

</td><td>

In the Now Agent app, the mandatory questionnaire doesn't honor dependency settings after an instance upgrade.

</td><td>

1.  Open an instance.
2.  Impersonate 'Persona field service officer'.
3.  Navigate to the 'My work' navigation tab at the bottom.
4.  Select a work order task.
5.  Select **Visit Report**.
6.  Scroll down, then select **Visit Report Install**.

 Expected behavior: 'Age of responsible adult' and 'Responsible adult relationship' should be visible when 'Is the subject a child' is set to 'Yes' and 'Parent, guardian and other P/G/O' is set to 'Other'.

 Actual behavior: The fields show 'Age of responsible adult' and 'Responsible adult relationship' on load.

</td></tr><tr><td>

Multi-Instance Framework - Core

 PRB2062210

</td><td>

Implement Glide family changes to support discovering Hermes across data centers

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multi-Instance Framework - Core

 PRB2063884

</td><td>

MIF Hermes doesn't refresh the cluster configuration when the local hermes\_cluster\_config has no primary or after a datacenter-rule change, causing stale/failed cluster resolution for remote owners

</td><td>

When instance A sends a MIF async message to instance B, it needs B's Hermes cluster details \(datacenter + Kafka bootstrap servers\). A keeps a saved copy in the hermes\_cluster\_config table and reads it in Hermes​Producer​Client .​get​Cluster​Info​Set.​ That method only calls B's live endpoint \(/api/now/hermes\_cluster\_info, tier-2\) when A has no saved rows for B. Two gaps result: First, saved rows but no primary — if A has rows for B where no one is is\_primary\_for\_service=true \(scenario like only a single non-primary cluster row\), the method does not refresh. And method ensure​Topic​Location​For​Instance\(String owningInstance\) then finds primaryCluster == null and the send fails with 'No primary cluster found'. Second, stale rows after a datacenter change — if a MIMIR rule change moves B's cluster to a new DC, A's saved rows are outdated but still look complete \(they have a primary\), so tier-1 returns them and A never re-discovers → messages Navigate to the old cluster.

</td><td>

1.  Verify that Instance A has a saved Hermes cluster rows for instance B \(service MIF-Hermes\) pointing to B's old datacenter, or a single row that isn't marked primary.
2.  Send a MIF async message from A to B.

 Expected behavior: A resolves B's current cluster details and sends to the correct datacenter.

 Actual behavior: A uses the old/incomplete saved config and sends to the wrong datacenter, or fails with 'No primary cluster found'.

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2051440

</td><td>

On-demand MMS submission fails

</td><td>

The issue occurs on instances where the multimodal service URL is configured via sys\_service\_endpoint instead of the system property.

</td><td>

1.  Open an instance with the MMS plugin active.
2.  Leave glide.​platform\_​mm\_​service.​service\_​url empty.
3.  Configure the Multimodal service endpoint via an active sys\_service\_endpoint record.
4.  Confirm that the batch/scheduled MMS job reaches the service.

Observe that it resolves the URL from sys\_service\_endpoint.

5.  Call new MultimodalServiceUtil\(\) .​submit​On​Demand \(attachment​Sys​Id,​ query\).

 Observe that the on-demand MMS submission fails.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2053821

</td><td>

Update to Otto branding in Next Experience

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Now Assist for IT Service Management \(ITSM\)

 PRB2075918

</td><td>

'GlideRecordCache is not allowed' error message appears in incident records

</td><td>

After the 'ServiceNow Otto for IT Service Management' \(v17.0.5\) plugin update on Zurich Patch 12, users see duplicate error messages stating 'GlideRecordCache is not allowed in scoped applications' when viewing incident records.

</td><td>

1.  Provision a Zurich Patch 12 instance with the 'ServiceNow Otto for IT Service Management' plugin installed with version 17.0.5.
2.  Open any incident form.

 Observe that the following error message is displayed: 'GlideRecordCache is not allowed in scoped applications'.

</td></tr><tr><td>

Now Assist in Virtual Agent

 PRB2056609

</td><td>

Change the Knowledge Graph \(KG\) defaults in NAVA and Now Assist Portal

</td><td>

Today, the KG default is User NLQ graph. That should be changed so the defaults are: In Now Assist Virtual Agent for natural language query, change the graph to Enterprise Graph \(Small\) and select the tag as 'VIRTUAL AGENT DEFAULT TAG'. In Now Assist Panel for natural language query, change the graph to Enterprise Graph \(Small\) and select the tag as 'NOW ASSIST PANEL DEFAULT TAG'.

</td><td>

 

</td></tr><tr><td>

Now Assist Nextwave Experience

 PRB2059502

</td><td>

Add sys\_props for caching in sys\_og\_conversational \_cache\_configuration

</td><td>

If props are enabled on the instance, that should be reflected via cache service instantly.

</td><td>

 

</td></tr><tr><td>

Now Assist Nextwave Experience

 PRB2061245

</td><td>

SessionController shouldn't try to refresh AuthorizationInfoBundle, as this is done in the Glide handshake process

</td><td>

When a topic execution is initiated, the conversation ID isn't available in certain Glide log entries' context maps, which complicates troubleshooting across different trace IDs instead of a unified conversation ID. The conversation ID should be available in the cache and topic execution context map in the syslog table.

</td><td>

 

</td></tr><tr><td>

Now User Experience

 PRB1960854

</td><td>

JavaScriptCommentStripper doesn't work properly with the upgraded highchart bundle \(12.3.0\)

</td><td>

There's a runtime exception: 'org.​openqa.​selenium. ​Javascript​Exception:​ Document was unloaded'.

</td><td>

Run IT test​Outage​Association​With​Case​IT .​check​Child​Case​Linked​To​Parent​Outage.​

 Observe that it fails on main.

</td></tr><tr><td>

OAuth 2.0 integration

 PRB2032073

</td><td>

Chat-Input is available to requester when conversation ends

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OAuth

 PRB2052671

</td><td>

Support to create an OAuth entity record within the caller scope

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1975559

</td><td>

On-call contact information isn't visible for some users for some attempts

</td><td>

This issue only occurs when logged in as a user.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB2034496

</td><td>

In a SMS action in the subflow 'On-Call', the 'Check Assignment Response' doesn't use Notify

</td><td>

The 'On‑Call: Check Assignment Response' flow uses the legacy SMS send action instead of the Notify‑based SMS action.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB2039960

</td><td>

The NotifyUtils check for notification devices should return empty when the ACL check is successful

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2041342

</td><td>

AI Summary card stays in perpetual loading state

</td><td>

This issue occurs for some Business Application records using the Record Summarization capability. There are no LLM calls and no errors.

</td><td>

1.  Navigate to APM Workspace.
2.  Open a Business Application record.

Observe that the AI Summary card stays in perpetual loading.

3.  Check sys\_generative\_ai\_log.

Observe that there's no LLM call logged for this request.

4.  Check syslog.

Observe that there's no errors; the full pipeline completes with cache HIT.

5.  To compare with a working BA record, navigate to service-​now.​com/​now/​apm/​application-​rationalization.​
6.  Select the **Now Assist** icon on business apps.

 Observe that the summary is generated. It generates LLM calls and renders correctly.

</td></tr><tr><td>

OneExtend

 PRB2056745

</td><td>

Guardian preprocess flow resolves getGeoRoutingDetails\(\) multiple times per request in NowLLMIntegration GuardianProvider

</td><td>

NowLLMIntegration GuardianProvider. shouldUseGatewayService\(\) and addLLMGatewayRoutingHeader\(\) each independently call through to GeoRoutingServiceImpl .getGeoRoutingDetails\(\) &gt; resolveGeoRoutingDetails\(\). ShouldUseGatewayService\(\) itself is invoked from multiple call sites across a single request's lifecycle \(transformRequest, generateTrustBuilderInputs, tryLogTrustBuilderResults, and twice within getUrl\(\)\). None of these calls are memoized, so resolveGeoRoutingDetails\(\) re-executes its full resolution logic \(potentially including the licensing entitlement API call\) on every invocation within the same request, even though the underlying geo-routing state can't change MID-request.

</td><td>

1.  Trigger a Guardian moderation request that routes through NowLLMIntegration GuardianProvider \(LLM\_GENERIC\_ SMALL\_MODERATIONS model\).
2.  Trace/log calls into GeoRoutingServiceImpl .resolveGeoRoutingDetails\(\) \(or set a breakpoint\) during a single request's transformRequest\(\)/getUrl\(\) lifecycle.

 Observe that resolveGeoRoutingDetails\(\) executes repeatedly \(up to six times found via code trace\) instead of once per request. When the 0$ SKU entitlement isn't active, each of these calls re-invokes the expensive isEntitlementActive WithLicensingAPI\(\) licensing call, since resolveGeoRoutingDetails\(\) has no per-request memoization. Only the underlying getGeoRoutings\(\) /getGeoRoutingConfigs\(\) cache calls are cached via ADomainAwareCache.

</td></tr><tr><td>

OneExtend

 PRB2057127

</td><td>

Multiple GenAI logs are created in skill chaining execution

</td><td>

OneExtend Execute and ExecuteSecure are missing the offGlideChainingEnabled flag.

</td><td>

Execute a skill chaining.

 Observe that the Generative AI logs are created two times.

</td></tr><tr><td>

OneExtend

 PRB2059503

 [KB3142021](https://hi.service-now.com/kb_view.do?sysparm_article=KB3142021)

</td><td>

Summarization records aren't displaying a proper response

</td><td>

Incident, Change, and Case summarizations are failing with errors when users select the **Summarize** button: 'Summarization could not be completed because access to the base table Case was unsuccessful'. Error logs: 'Error sending to unified\_​short\_​url\_​active\_​ 1.​.​.​Status 500 - \[Internal Server Error\] \[\{'success':​false,​'status​Code':​429,​'message':​'Too many concurrent data insert operations in progress - additional rebuild request being ignored',​'timestamp':​'2026-​07-​17​T07:​00:​17.​752637494​Z',​'results':​\{\}​\}​\]​'.​

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OneExtend

 PRB2079397

</td><td>

The 'Incident Summarization' skill intermittently isn't returning the correct response after an upgrade

</td><td>

​

</td><td>

​

</td></tr><tr><td>

Performance Analytics

 PRB1899019

</td><td>

PA scores aren't retrieved immediately after enabling data snapshots

</td><td>

The 'No scores available' message is displayed. It remains the same until mining is complete, which shouldn't happen.

</td><td>

1.  Provision an instance with the com.snc.pa.premium and com.snc.pa.mlb plugins installed.
2.  Navigate to the number of open incidents.
3.  Make sure there isn't a data snapshot already created for the incident table.
4.  Remove the age breakdown.
5.  Run the classic Historic PA Job to view scores.
6.  Enable data snapshots for this indicator.
7.  View the scores.

 Observe that the 'No scores available' message is displayed.

</td></tr><tr><td>

Performance Analytics

 PRB2032037

</td><td>

The Platform Analytics dashboard filters ignore Element Security Lists and display 'Nothing is available'

</td><td>

If the user sets up an Element Security List for a breakdown source that's used as a filter in a Platform Analytics dashboard, the filter shows 'Nothing is available'. This happens even though the user has valid access to the dashboard and the underlying data.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2037426

</td><td>

scoreType is forced to 'latest' for non-aggregate indicators due to an undefined aggregateIndicator check

</td><td>

When a visualization widget uses a classic indicator \(sourceType: 'indicator'\) with applyDateRange enabled, the scoreType property is incorrectly forced to 'latest' even when the metric is not an aggregate indicator. This happens because the aggregateIndicator check in the scripted policy evaluates 'undefined !== ''' as 'true', even though the metric object doesn't have an 'aggregateIndicator' property at all. The user loses the ability to select other score types \(sum, average, etc.\) for non-aggregate indicators, and any previously configured scoreType value \(for example, 'sum'\) is overwritten to 'latest'.

</td><td>

1.  Add a single-score \(or any visualization that uses the shared date-range policy\) widget to a dashboard.
2.  Configure it with a classic PA indicator data source \(sourceType: 'indicator'\) that isn't an aggregate indicator \(for example, 'Number of new requested items'\).
3.  Enable 'Apply date range' \(applyDateRange: true\).
4.  Set scoreType to 'sum' \(or any value other than 'latest'\).
5.  Open the widget configuration again.

 Expected behavior: The scoreType remains 'sum' and all score type options are available in the drop-down list.

 Actual behavior: The scoreType is forced to 'latest' and the drop-down list is inactive.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2038900

</td><td>

Platform Analytics Release \(PAR\) dashboard's saved filters drop on 'GET' \(200, empty filters\) when a referenced saved/library filter is unresolvable \(deleted or cross-domain\)

</td><td>

Filters​Service.​remove​Invalid​Filter \(inline path\) had a guard that returned '' whenever availableFilters.size\(\) didn't match the layout's filter-component count. getAvailableFilters can't resolve a stored\_component whose par\_component\_filter record is deleted or domain-invisible, so a single unresolvable reference caused all of the dashboard's saved filters to be discarded for every user. The PUT path does no validation and saves correctly; only the GET-time validation drops them. On domain-separated \(MSP\) instances, this is easily hit because dashboards in user sub-domains reference global saved filters.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2039418

</td><td>

List migration logic should be added for the highlighted values config

</td><td>

When the user upgrades, the corresponding properties should be migrated to the new list visualization.

</td><td>

1.  On a Yokohama instance, create a list-simple visualization.
2.  Enable fetchHighlightedValues.
3.  Add some highlightedvalueconfigid to the list-simple visualization.
4.  Upgrade to Zurich, Australia, or Brazil.

 Observe that the corresponding properties are migrated to the new list visualization.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2050660

</td><td>

Par\_dashboard\_tab records are created unintentionally when a non-admin user accesses an inactive dashboard

</td><td>

When a non-admin user accesses an inactive \(deactivated\) Platform Analytics dashboard through the workspace URL, one or two new par\_dashboard\_tab records are created unintentionally.

</td><td>

1.  Impersonate a user.
2.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Dashboards**.
3.  Create a dashboard without any dashboard tabs.
4.  Open the dashboard record using a URL like 'https:​/​/​&lt;instance-​id&gt;​.​service-​now.​com/​ par\_​dashboard.​do?​sys\_​id=​&lt;sys\_​id&gt;​'.​
5.  Clear the **Active** option.
6.  Update the record.
7.  As the same user as step 1, access the dashboard via a URL like 'https:​/​/​&lt;instance-​id&gt;​.​service-​now.​com/​ now/​platform-​analytics-​workspace/​dashboards/ ​sys-​id/​&lt;sys\_​id&gt;​'.​
8.  Check par\_dashboard\_tab.

 Expected behavior: The par\_dashboard\_tab doesn't have a record for the test dashboard.

 Actual behavior: Once the user accesses the inactive dashboard, one or two new par\_dashboard\_tab records are created unintentionally.

</td></tr><tr><td>

Platform Analytics Filters

 PRB1968556

</td><td>

Users are unable to filter on the sys\_class\_name column of the kb\_knowledge table in a new Platform Analytics dashboard

</td><td>

The column 'Class' isn't present.

</td><td>

1.  Navigate to self-service dashboards \(also known as Core UI dashboards\).
2.  Create a dashboard.
3.  Add an interactive filter to the dashboard that filters on table 'kb\_knowledge' and column 'Class'.

Observe that it works.

4.  Save the dashboard.
5.  Migrate it to Platform Analytics.

Observe that the filter works.

6.  Create a Platform Analytics dashboard.
7.  Add a filter.
8.  Select table 'kb\_knowledge' as the source.
9.  Try to select column 'Class'.

 Expected behavior: The user can choose the column 'Class'.

 Actual behavior: The column 'Class' isn't present.

</td></tr><tr><td>

Platform Analytics Filters

 PRB1993721

</td><td>

A dashboard's Year to Date \(YTD\) filter fails to apply on a list unless it's reset

</td><td>

A dashboard's YTD filter doesn't consistently apply the correct date range to list widgets, resulting in incorrect list results until the YTD filter is manually cleared or reset.

</td><td>

 

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
3.  Add the 'Today' predefined range.
4.  Add any other predefined range for easy testing.
5.  Set the default value to 'Custom Range'.
6.  Enable **Allow time selections**.
7.  Save changes and Navigate to the date filter.
8.  Select any predefined range other than 'Today'.
9.  Select **Today**.

 Notice that the date will update correctly, but the start time will update to the current time.

</td></tr><tr><td>

Platform Analytics Filters

 PRB2021606

</td><td>

An interactive filter can be cleared via a double-click even when the 'Allow User to Clear Filter' option is turned off

</td><td>

Users are able to clear the applied interactive filter by double-clicking the selected filter value even when the 'Allow user to clear filter' option is turned off in the filter configuration and clear filter option isn't appearing. Additionally, when multiple interactive filters are configured with filter interactions/dependencies, the dependent filters still display the option to clear the filter. This behavior creates inconsistency with the expected functionality of the 'Allow user to clear filter' setting, as users are still able to clear filters through alternate interactions.

</td><td>

1.  Create a dashboard.
2.  Add a visualization with an interactive filter.
3.  Configure the interactive filter to turn off the option 'Allow user to clear filter'.
4.  Apply/select a filter value on the dashboard.

Observe that there's no 'Clear filter' option.

5.  Double-click the selected filter value.

Observe that the filter is cleared even though the clear option is turned off.

6.  Configure another interactive/dependent filter.

Observe that the dependent filter still displays the option to clear the filter.


 Expected behavior: When the 'Allow user to clear filter' option is turned off, users shouldn't be able to clear filters through any UI interaction, including double-click actions or dependent filter interactions.

 Actual behavior: Filters can still be cleared through double-click interaction and dependent filters display clear filter options despite the setting being turned off.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2034116

</td><td>

Upgrading from Yokohama to Zurich causes all pa\_widgets to be migrated after upgrade

</td><td>

The pa\_widgets table doesn't have an active field.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2037846

</td><td>

The Migration Center summary count doesn't match the list count for fully migrated dashboards

</td><td>

The Get Migration Summary Scripted API needs to be updated so that it calculates the total number of migrated dashboards in the same way as the Migrated List.

</td><td>

Scenario 1:

 1.  Create a few Core UI dashboards.
2.  Migrate them.
3.  Navigate to the PAR Dashboards table.
4.  Delete one or more migrated dashboards.

 Observe that the Migrated List count and the Summary count don't match.

 Scenario 2:

 1.  Create a Core UI dashboard containing a Dynamic Content widget.
2.  Migrate the dashboards.
3.  Navigate to the par\_coreui\_migration \_bridge\_dashboard table.
4.  Remove the record\(s\) associated with the dashboard that contains the Dynamic Content widget.

 Observe that the Migrated List count and the Summary count don't match.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2025987

</td><td>

A user can't view a playbook without record create access

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2052473

</td><td>

The getPlaybookContextParentRecord API should be exposed as scriptable

</td><td>

The Playbook MCP tool code doesn't use the existing API get​Playbook​Contexts​By​Parent​Record to launch and continue playbook execution. This API internally handles all validation and permission access, which results in duplicate logic. The current java API should be exposed as a scriptable API to use at Playbook MCP tool.

</td><td>

1.  Add any compatible playbook as MCP tool.
2.  Try to launch playbook through the Claude client.

 Observe that it launches playbook, but it uses custom logic to validate access and permission.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2052670

</td><td>

'Completed By' and 'Completed On' for Activity Contexts

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

PPM Standard

 PRB2037975

</td><td>

Relax RIDAC table business rules

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1957306

</td><td>

Scheduled tasks are shown in the 'Pending' state after the execution tracker is deleted

</td><td>

The scheduled task shows up on workbench with the 'Pending' state and no actions can be taken on it.

</td><td>

1.  Create a scheduled task.
2.  Delete the execution tracker associated with the task.

 Observe that the scheduled task shows up on workbench with the 'Pending' state. No actions can be taken on it.

</td></tr><tr><td>

Process Mining

 PRB2022864

</td><td>

Users are unable to edit access for Now Assist creator's 'Work Notes Analysis' skill

</td><td>

 

</td><td>

1.  Navigate to a Zurich instance.
2.  Impersonate any admin user.
3.  Navigate to Now Assist Admin.
4.  Open **Creator** &gt; **Skill** &gt; **Work Notes Analysis**.
5.  Try to add an extra role beside the given role.

 Expected behavior: The user should have edit permission to edit.

 Actual behavior: The user is unable to edit permissions.

</td></tr><tr><td>

Process Mining

 PRB2035128

</td><td>

Meter-based guardrails and controls

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB2022151

</td><td>

The record count for child tables shows the total records and ignores any applied filter

</td><td>

Since this is expensive to calculate, the recommendation is to hide that counter for child tables altogether.

</td><td>

1.  Create a project.
2.  Add a child entity.
3.  Add a filter to the child entity.
4.  Select the button to show total number of records for that child entity.

 Expected behavior: Only the records in scope are shown.

 Actual behavior: The total number of records in the table are shown.

</td></tr><tr><td>

Process Mining Workspace

 PRB2023836

</td><td>

The Process Mining usage table \(promin\_metered\_usage\_data\) must be preserved across clones

</td><td>

The Process Mining usage table \(promin\_metered\_usage\_data\) is overwritten during instance clone operations, causing mined record counts to be duplicated and incorrectly reported when users mine on non-production after cloning from production. Process Mining licensing counts unique mined records per instance \(not across instances\).

</td><td>

1.  Mine records in production.
2.  Clone production into a non-production instance.
3.  Mine again in non-production

 Expected behavior: After any clone operation, the Process Mining usage table on the target \(cloned\) instance is reset to its original \(empty/baseline\) state, so usage counting starts fresh/continues per instance. The configuration that enforces this should be mandatory on every clone and read-only / protected.

 Actual behavior: The cloned non-prod instance inherits production's usage history, but subsequent mining activity overwrites or duplicates entries. This breaks per-instance usage reporting and creates a double-charging risk.

</td></tr><tr><td>

Process Mining Workspace

 PRB2024798

</td><td>

Summary top banner metrics isn't displaying until the project is reopened or the page is refreshed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB2034613

</td><td>

Users can't edit access for the Now Assist creator 'Work Notes Analysis' skill

</td><td>

 

</td><td>

1.  Open a Zurich instance.
2.  Impersonate any admin user.
3.  Navigate to Now Assist Admin.
4.  Open **Creator** &gt; **Skill - Work Notes Analysis**.
5.  Try to add an extra role besides the given role.

 Expected behavior: The user has permission to edit the field. Also, the workbench should respect the permission set at skill level.

 Actual behavior: The user is unable to edit permissions.

</td></tr><tr><td>

Process Mining Workspace

 PRB2038768

</td><td>

Scheduled tasks are shown in the 'Queued' state after the execution tracker is deleted

</td><td>

Scheduled tasks show up on workbench with the 'Queued' state, and no actions can be taken on them.

</td><td>

1.  Create a scheduled task.
2.  Delete the execution tracker associated with the task.

 Observe that the scheduled task shows up on workbench with the 'Queued' state and no actions can be taken on it.

</td></tr><tr><td>

Process Mining Workspace

 PRB2050830

</td><td>

Wipe out promin\_metered\_usage\_data across non-prod and rely on the Glide non-prod/prod property, not on the Open/Closed property

</td><td>

When users clone production to a non-prod instance, the non-prod promin\_metered\_usage\_data table is wiped and replaced with prod's data, so non-prod reflects a copy of prod rather than real usage. When users clone prod to several non-prods at once, each carries prod's usage table. Subscription Management's flat aggregation then counts the same prod records once per instance, so reported usage scales linearly with the number of non-prods a user maintains, independent of actual mining behavior.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB2052878

</td><td>

Otto directive for process mining

</td><td>

The Otto rebrand should be completed for work notes analysis, intent and activity analysis, process highlights, generate process config with AI, and playbook mining.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB2055568

</td><td>

In Zurich, a false 'access denied' error appears when saving table/filter changes on an existing project

</td><td>

Process Mining table-access validation incorrectly denies save actions for users who have genuine read access to the table via a conditional ACL. The system throws: 'You do not have access to \{table\} table'. This happens because it checks permissions against an empty test record instead of real data. The error is a false negative in the platform's own pre-save validation, not an actual permissions gap. Users with access via an unconditional ACL don't receive the error.

</td><td>

1.  Create a dedicated test role \(for example, test\_incident\_reader\).
2.  On the incident table, add a new read ACL.
3.  Set the role to the new test role.
4.  Add a data condition \(for example, assignment group is &lt;specific group&gt;\).
5.  Create a test user with only that new role \(make sure there's no other role tied to an existing unconditional ACL on incident, like itil or sn\_incident\_read\).
6.  Create an incident record matching the condition \(for example, the same assignment group\).
7.  Impersonate the test user.
8.  Confirm via the incident list view that the user sees only that one matching record.
9.  As that user, open Process Mining.
10. Create or open a project with a table configuration on incident.
11. In the 'Scope your analysis' step, edit a filter.
12. Save.

 Expected behavior: The save succeeds.

 Actual behavior: The message 'You do not have access to incident table' appears, despite step 8 confirming real access.

</td></tr><tr><td>

Project Management

 PRB2006929

</td><td>

Deleting a project task with MS Project creates an orphaned resource request

</td><td>

 

</td><td>

1.  Log in to any instance.
2.  Open the new Project Workspace.
3.  Select the **New** button to create a project.
4.  Select the **Menu button \(...\)** &gt; **Import from MS project**.
5.  Upload a MS Project schedule.
6.  Create a resource request for Project Tasking.
7.  Navigate to the resource module as the resource manager and approve the task.
8.  As the project manager, delete the task in the MS Project schedule.
9.  Return to the project record.
10. Re-upload the updated MS Project.

 Expected behavior: The re-upload of the schedule isn't permitted because of the related record. If it does allow the re-upload, it should cascade the delete to the related records.

 Actual behavior: The resource manager can still see the resource request, but the task name is blank.

</td></tr><tr><td>

Project Management

 PRB2023802

</td><td>

The PowerPoint export service loses the connection

</td><td>

The export functionality is broken. When using the export feature, it displays 'Unable to complete request'. There are no log entries available for this error message. In order to exclude issues with the built-up service, there are regular pings every 15 minutes from the instance to the backend service, but those pings stop at the end of the day. After manually updating the entry in sys\_service\_endpoint, the pings start and exporting to PowerPoint is available.

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB2040639

</td><td>

Require authentication on a scripted rest API reporting\_alias

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Roles

 PRB2052882

</td><td>

Inherited roles aren't added back when patcher is on and the state of 'User has role' is changed from pending\_approval to active

</td><td>

When the user updates the state of the 'User has role' record to active, no records are created for inherited roles.

</td><td>

1.  Enable the glide.​security.​inh\_​count \_​patcher.​enabled property to true.
2.  Assign a user with an admin role and with the state as pending approval.

No 'User has role' records should be created for inherited roles.

3.  Update the state of the 'User has role' record to active.

 Expected behavior: 'User has role' records are created for inherited roles with the state as active.

 Current behavior: No 'User has role' records are created for inherited roles.

</td></tr><tr><td>

Scheduled Jobs

 PRB2015240

</td><td>

Create a guard rail to protect the scheduler against misconfigured nodes to avoid impact to critical jobs

</td><td>

Misconfigured nodes can severely impact the job scheduler, causing business critical jobs to not get executed.

</td><td>

1.  On a two \(or more\) node cluster, configure one of the nodes to have schedulers=any and participation=standby.
2.  Create 1000 pinned jobs with priority=100 and pin to that node.
3.  Wait a few minutes.

 Observe that both this node's and other nodes' pinned jobs with priority&gt;=100 no longer execute.

</td></tr><tr><td>

Schedule Optimization \(Glide Family Channel\)

 PRB2034899

</td><td>

Intraday optimization is stuck in 'In progress'

</td><td>

Intraday optimization jobs may become permanently stuck in the 'In Progress' status due to a timing issue in how solution metadata is processed internally, which can result in job status updates being lost.

</td><td>

1.  Configure Schedule Optimization with intraday optimization enabled with territory model.
2.  Set up an intraday optimization schedule with multiple overlapping territories.
3.  Trigger an intraday optimization run.
4.  Check wm\_intraday\_job\_m2m\_qualifier.

 Observe that some of the records remain stuck in in\_progress status indefinitely, even after all the solutions are processed or the records show no processed task counts, total task counts, and/or progress bar. During normal intraday runs with concurrent solution processing, the race condition between SolutionMetadataProcessor and SolutionProcessorSNC can cause lost updates on ml\_solution.solution\_metadata, also resulting in stuck in\_progress records.

</td></tr><tr><td>

Schedule Optimization \(Glide Family Channel\)

 PRB2035210

</td><td>

When work schedules aren't created in WFO, GraphQL fails a few times

</td><td>

 

</td><td>

1.  Create an empty work schedule in WFO.
2.  Send a QualifierData GraphQL call.

 Observe that GraphQL fails a few times.

</td></tr><tr><td>

Schedule Optimization \(Glide Family Channel\)

 PRB2041460

</td><td>

In Zurich, an intraday job takes around 12 minutes to be submitted to ML Scheduler

</td><td>

 

</td><td>

1.  Log in to a Zurich instance.
2.  Run an intraday job with 200 qualifiers.

 Observe that it takes around 12 minutes to be submitted to ML Scheduler.

</td></tr><tr><td>

Schedule Optimization \(Glide Family Channel\)

 PRB2051159

</td><td>

Intraday optimization is stuck in 'In progress'

</td><td>

The race condition is in solution processing. Glide mutex API needs to be added in global scope.

</td><td>

1.  Configure Schedule Optimization with intraday optimization enabled with territory model.
2.  Set up an intraday optimization schedule with multiple overlapping territories.
3.  Trigger an intraday optimization run.
4.  Check wm\_intraday\_job\_m2m\_qualifier.

 Observe that some of the records remain stuck in the in\_progress status indefinitely, even after all the solutions are processed or the records show no processed task counts, total task counts, and/or the progress bar. During normal intraday runs with concurrent solution processing, the race condition between SolutionMetadataProcessor and SolutionProcessorSNC can cause lost updates on ml\_solution.solution\_metadata, also resulting in stuck in\_progress records.

</td></tr><tr><td>

Schedule Optimization \(Glide Family Channel\)

 PRB2056649

</td><td>

There's a double booking issue in conflict resolution

</td><td>

 

</td><td>

1.  Configure Schedule Optimization with intraday optimization enabled with territory model/assignment group.
2.  Set up an intraday optimization schedule with multiple overlapping territories/assignment groups.
3.  Trigger an intraday optimization run.
4.  Open dispatcher workspace.

 Observe that a few work order tasks are double booked.

</td></tr><tr><td>

Schedule Optimization \(Glide Family Channel\)

 PRB2057489

</td><td>

SO conflict resolution is unassigning locked tasks

</td><td>

A conflict resolution fix was implemented to unassign tasks from the solution when the assignee has a conflict. However, it unassigns tasks even if they were locked after solution processing began. There should be a filter to skip the unassignment if the task has transitioned to a locked state.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB2051345

 [KB3128196](https://hi.service-now.com/kb_view.do?sysparm_article=KB3128196)

</td><td>

Automatically created KittyScript exemptions are incorrect when using 'new GlideRecord'

</td><td>

When GuardedScript/KittyScript checks scripts in the exemption table, it does by checking a \_normalized\_ version of the script, where all literals are removed to ensure that it deduplicates similar scripts where the only difference is \(say\) a 'sys\_id'. This normalization does \_not\_ apply to the constructor of 'GlideRecord' where it doesn't want a blanket exception for \_all\_ tables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB2054951

</td><td>

ServiceNow Otto rebranding for catalog item slot-fill

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2054931

</td><td>

ServiceNow Otto rebranding for catalog item generation with Text2Catalog family support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Level Management

 PRB2001036

 [KB3137219](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137219)

</td><td>

In SLACalculatorNG, an unbounded schedule/DurationCalculator cache causes memory growth during bulk SLA recalculation

</td><td>

During bulk SLA recalculation, SLACalculatorNG accumulates one GlideSchedule and one DurationCalculator instance per unique schedule+time zone combination into unbounded object maps \(this.schedules and this.durationCalculators\). These maps are never evicted and grow proportionally to the number of distinct schedule/time zone pairs encountered across all task\_sla records in the query. In instances with many SLA definitions backed by different schedules, this results in unbounded heap growth for the lifetime of the bulk calculation, degrading instance performance and potentially causing out-of-memory conditions under load.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Mapping

 PRB2036299

</td><td>

After upgrading to Australia, parent.process.pid fails to resolve, which causes the 'Get Process' operation to return the full process list instead of the targeted parent process

</td><td>

The user can run a customized Tomcat WAR pattern for Service Mapping discovery. Following the Australia upgrade, step two of the 'Identification' section stops working during Service Mapping discovery. The step uses a 'Get Process' operation with process\_id = get\_attr \{'parent.process.pid'\} to locate the parent Windchill Java process. This expression fails to resolve, causing the step to run with no PID filter and return the entire process list on the host instead of the targeted parent process.

</td><td>

1.  Upgrade to the Australia release.
2.  Run discovery on the service map with Tomcat CI.

 Observe that the 'Get Process' operation returns the full process list from the host instead of the targeted parent process.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2013533

</td><td>

There's an unhelpful error when installing an app with an invalid scope prefix

</td><td>

Error: '\[now-sdk\] ERROR: Exception occurred while installing application/Unable to install application as application was null. Error: Exception occurred while installing application/nUnable to install application as application was null'.

</td><td>

Create an app with now-sdk init without a valid auth saved.

 The resulting app has an x\_ prefix and gives an error when trying to install on an instance.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2033218

</td><td>

Fluent App metadata deletions aren't propagated when installing from the app repo

</td><td>

The issue occurs because of missing sysmetadatadelete records.

</td><td>

1.  Delete metadata from Fluent App.
2.  Build and deploy to the instance.
3.  Publish to the app repo from the instance.
4.  Install it on a different instance that doesn't contain the delete from app-repo.

 Expected behavior: The delete is applied and the metadata is removed.

 Actual behavior: The metadata is not removed.

</td></tr><tr><td>

ServiceNow Studio \(Family Channel\)

 PRB2063560

</td><td>

True up the Glider Store app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB2056735

</td><td>

Update the accessibility voice-input toggle label in Service Portal for the Otto rename

</td><td>

As part of the 'Now Assist to Otto' rename, the accessibility toggle label must be updated in Service Portal. It's currently 'Enable voice input for Now Assist in Virtual Agent'. The new value will be similar to 'Enable voice input for ServiceNow Otto'.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB2056737

</td><td>

Portal-core widget UI and theming for new Otto onboarding modal in the Service Portal

</td><td>

The modal introduces users to the ServiceNow Otto experience on first login. Because Lit-based workspace components can't be embedded in angular portals, a dedicated Service Portal implementation is required. The widget lives in the platform layer and is shared across all portals. No per-portal or user uptake is required.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB2056743

</td><td>

Eligibility and admin control for new Otto onboarding modal

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB2058602

</td><td>

Typing indicator no longer works

</td><td>

 

</td><td>

1.  Open two browsers.
2.  Log in as two different users.
3.  Create a sidebar chat for the two users.
4.  Start typing.

 Observe that there is no typing indicator.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2000893

</td><td>

Recon updates are dropped by a database, causing license metric results \(LMR\) and product results to not update

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Lifecycles

 PRB2004396

</td><td>

A calculated lifecycle should consider other phase start dates before creation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Lifecycles

 PRB2010294

</td><td>

Matching a common platform enumeration \(CPE\) to DMs should ignore CPEs that are version less

</td><td>

sn\_itam\_samp. MatchVulnerableSoftware ToDiscoveryModels should ignore CPEs that are a version less. Vulnerabilities are reported against versions of a product, but due to National Vulnerability Database \(NVD\) data or corrupted NVD data, CPEs may be a version less.

</td><td>

 

</td></tr><tr><td>

Software Lifecycles

 PRB2012476

</td><td>

Matching a common platform enumeration \(CPE\) to DMs should ignore CPEs edition and software edition

</td><td>

There are two **Edition** fields on CPE, 'Edition' and 'Software Edition'. It queries against both, but 'Edition' is a legacy and deprecated field from the old 2.2 standard. 'Software Edition' was introduced in 2.3.

</td><td>

 

</td></tr><tr><td>

Standard Ticket Page

 PRB2054934

</td><td>

ServiceNow Otto rebranding for Now Assist in 'Standard Ticket' page family

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB2019118

</td><td>

Generative AI logs are missing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2003217

</td><td>

Fix behavior of event processing tables during the clone operation and clean up invalid records/jobs during the clean up script

</td><td>

During cloning on Zurich instances, events processing framework tables' configuration aren't preserved, causing errors in transaction logs due to orphan records for events jobs. An orphan record occurs when a sys\_trigger record exists for an event processing job, but the corresponding entry in the sys\_processing\_framework\_job table is missing. This causes the ProcessingFrameworkJob to fail when attempting to retrieve the scheduled job context. Log example: 'ProcessingFrameworkJob SEVERE ProcessingFramework &gt; Failed to get the schedule job context'.

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

System Import Sets

 PRB2038233

</td><td>

JDBC connections are left dangling and unclosed

</td><td>

Every time the user issues a change credential signal to MID during a JDBC import, the number of open connections grows.

</td><td>

1.  Set up a MID server with a long running JDBC import that can be run through it.
2.  Start an import.
3.  While it's running, issue a change credentials signal to MID using the 'Refresh Credentials' related link on the MID server record.
4.  Repeat.
5.  Check the database for open connections from MID.

 Observe that the number of open connections grows each time.

</td></tr><tr><td>

System Web Services

 PRB2029605

</td><td>

There's hourly recurring OAuth authentication failures on an outbound REST from ST ServiceNow to CG ServiceNow: 'User is not authenticated. OAuth token has expired or has not been retrieved'

</td><td>

The reported issue affects the outbound integration between ServiceNow and the external ServiceNow instance through the iPaaS layer using OAuth 2.0 Client Credentials authentication. The integration fails specifically during the final one-minute window before the OAuth access token expiration. During normal token validity, the integration works successfully. Starting one minute before token expiration, outbound calls from ServiceNow fail. Failures occur in: REST Message, REST API Step, Flow Designer executions, and custom scripts. Once the token fully expires, ServiceNow successfully retrieves a new token and the integration resumes functioning normally.

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB2039182

</td><td>

Updating potential territories for a task doesn't work as expected

</td><td>

The Business Rule that updates the potential territories is currently triggered only when the location changes. It doesn't consider the **consider\_​potential\_​territories \_for\_schedule\_optimization** boolean field.

</td><td>

1.  Create a work order task.
2.  Change the location to see the eligible territories as per the new changed location.

 Expected behavior: The Business Rule that updates the potential territories should consider the **consider\_potential\_territories \_for\_schedule\_optimization** boolean field.

 Actual behavior: The Business Rule that updates the potential territories is currently triggered only when the location changes and doesn't consider the **consider\_potential\_territories \_for\_schedule\_optimization** boolean field.

</td></tr><tr><td>

Time-Limited User Roles

 PRB1972197

</td><td>

When a user is logged in, updating an existing record with a new end time in the 'Time limited user roles' table causes never ending information messages on all pages

</td><td>

 

</td><td>

1.  Open a Zurich instance.
2.  In a separate browser or incognito window, log in with a user that has an 'itil' role.
3.  In another window, log in with a user who has an 'admin' role.
4.  With the admin user, navigate to **All** &gt; **User administration** &gt; **Time-limited roles**.
5.  Create a record that grants an 'admin' role to the user.
6.  With the user that had only an 'itil' role but received the 'Time limited admin' role, open an incident list and then a record.

 Expected behavior: Users see an information message once.

 Actual behavior: Users see a message about roles that are granted or removed, but closing them isn't helping.

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2056896

</td><td>

Trace collector MID code

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2059215

</td><td>

Azure classic trace collector doesn't consider Credential IDs for AI and ML services

</td><td>

AzureTraceCollector ignores credential IDs supplied as config update parameters. It only considers credential alias names.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB2051051

</td><td>

The field error message isn't shown when the error comes from the backend via business rule abortAction

</td><td>

The error message isn't shown for the **short\_description** field in Australia. However, it's visible in Faster or PAXE Integration.

</td><td>

1.  Create an Insert/Update business rule with abortAction \(for example, current.​short\_​description.​set​Error\('Error!'\)​;​ current.​set​Abort​Action\(true\)​;​\)​.​
2.  Create an incident.
3.  Fill in the mandatory fields.
4.  Attempt to save it.

 Observe that the error message isn't shown for the **short\_description** field.

</td></tr><tr><td>

UI Field Administration

 PRB2054948

</td><td>

ServiceNow Otto rebranding for AI indicators, AI indicator pop-overs, and Task intelligence prediction

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2054949

</td><td>

IndexName GraphQL component and choice fallback

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2054953

</td><td>

Inject '\*' options into composite\_name table and field picker choice lists

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2019275

</td><td>

There's layout and scrollbar flickering when entering info, internal and external, in HTML **Journal** fields

</td><td>

There's layout and scrollbar flickering when entering info, internal and external, in HTML **Journal** fields, caused by automatic browser window resizing. The issue occurs randomly and is not related to a specific case or text size.

</td><td>

1.  Change the glide.ui.journal.use\_html system property to true.
2.  Open any incident in any workspace.
3.  Type multiple lines in internal info or copy/paste some text until the scroll bar appears.
4.  Remove enough lines so that it's one new line away from displaying the scroll bar.
5.  Type some words randomly to add enough words to create a new line.

 Observe the flickering issue.

</td></tr><tr><td>

UI Form Administration

 PRB2033143

 [KB3139369](https://hi.service-now.com/kb_view.do?sysparm_article=KB3139369)

</td><td>

The 'Preview this record' icon isn't working in the Safari browser

</td><td>

Selects on the button components and controls aren't working in Safari for UI16. This issue is only reproducible in the Safari browser. Non-Safari browsers aren't impacted and they don't face this issue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB2054945

</td><td>

Otto brand change in form notification messages

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2056498

</td><td>

The parentRecordSysId is missing from ORM Workspace payload template, so the getFilterQuery API breaks

</td><td>

The getFilterQuery REST API \(/api/now/ related\_list\_item\_filter/ getFilterQuery\) is being updated to require four mandatory parameters: tableName, parentFieldName, parentRecordSysId, and referencedFieldName. The Configurable Workspace for Order Management \(sn\_app\_orm\_wksp\) payload definition doesn't include parentRecordSysId in its payload template. Once the change occurs, any UI action using the payload receives a 400 error from the API.

</td><td>

1.  Provision an instance with the plugin com.sn\_app\_orm\_wksp installed.
2.  Activate the plugin.
3.  Trigger any UI action that uses the payload definition for event mappings.

 Observe that the call to /api/now/ related\_list\_item\_filter/ getFilterQuery returns \{'error': 'Invalid inputs'\}.

</td></tr><tr><td>

Upgrade Center

 PRB1950446

</td><td>

The 'Flow Designer' module directs to 'Page Not Found' after an instance upgrade on some nodes

</td><td>

The **Process Automation** &gt; **Flow Designer** module redirects to 'Page Not Found' on some nodes after an instance upgrade. The main issue is that nodes tried to download app packages from Store, but Store responded with a 400 error because the platform version for the instance isn't updated on the Store end yet, and the request is considered incompatible. However, during an upgrade, it shouldn't request app packages from Store.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2026005

</td><td>

UXF should let the inbox know when the workspace is not the active experience

</td><td>

Currently, when the agent navigates from workspace to home, the inbox is still present in the DOM. Because of this, agents are still assigned work items even when they aren't in the workspace.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2035397

</td><td>

After typing in an input field on record page load, the focus shifts intermittently

</td><td>

After a few words, the focus shifts to the 'Tags' section and it continues to write in that section.

</td><td>

1.  Navigate to CSM/FSM workspace.
2.  Open the list module.
3.  Navigate to 'All Cases'.
4.  Open any case form with tags displayed on it.
5.  Start typing in an input field \(for example, **Compose comments**\).

 Expected behavior: The user continues to type and the focus remains in the typing area.

 Actual behavior: After a few words, the focus shifts to the 'Tags' section and it continues to write in that section.

</td></tr><tr><td>

UX Framework

 PRB2054946

</td><td>

Keyboard shortcut remapping for admins and users

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1980327

</td><td>

A chat dynamic greeting isn't localized correctly

</td><td>

The message doesn't go down the correct API path to resolve to sys\_ui\_message, so it can't honor the dynamic greeting.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2009200

</td><td>

For the 'Resume' flow, work notes are added as the guest user

</td><td>

 

</td><td>

1.  Trigger the ZTSD flow with a query that has a valid KB resolution available.
2.  Impersonate as the subject person.
3.  Ask a query that can be answered by an existing KB article.

The 'Resume' flow is triggered.

4.  Open the corresponding case and check the 'Work Notes' section.

 Expected behavior: Work notes should be added under the impersonated HR L1 worker.

 Actual behavior: Work notes are added under the guest user.

</td></tr><tr><td>

Virtual Agent

 PRB2026682

</td><td>

Conversation history of language detection confirmation disrupts a user response

</td><td>

According to Search QnA, the prompt isn't structured to support the intermediate language selection turn. That should be removed from the conversation history.

</td><td>

1.  Configure language detection.
2.  Start a conversation in any standard chat.
3.  Type an utterance in a different language.
4.  When presented with 'You are typing in xyz language, do you want to switch', select **Yes**.

 Expected behavior: The language should switch and the synthesized response should be displayed.

 Actual behavior: The language switches but the response is 'How can I help you with your laptop'.

</td></tr><tr><td>

Virtual Agent

 PRB2031232

</td><td>

The 'Litjs' widget isn't displaying on the Now Assist panel

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2031583

</td><td>

Non-topic skills are dropped from the skill picker when all applicable topic skills have a visible design category

</td><td>

The picker shows the topic skills grouped under their design categories, but the non-topic skills are absent. No 'Others' category is created and the non-topic skills aren't rendered.

</td><td>

1.  Configure a VA/NowAssist conversation with:
    -   At least one non-TOPIC skill that is applicable and visible \(optionally, mark it as promoted in the context profile\).
    -   At least one TOPIC-type skill that is applicable and visible.
2.  Ensure every applicable topic skill has at least one visible design category \(sys\_cb\_topic\_category with visible = true\).
3.  Trigger the skill picker \(for example, via SystemScriptObject.jsFunction \_sendSkillPickerControl → VASkill​Service.​send​Skill​Picker\)​.​

 Expected behavior: Non-topic skills appear in the picker regardless of whether the applicable topic skills all carry visible design categories. For example, they could appear under 'Others'.

 Actual behavior: Non-topic skills are omitted whenever there is more than one applicable topic skill and all applicable topic skills have a visible design category.

</td></tr><tr><td>

Virtual Agent

 PRB2031991

</td><td>

'Get details of problem agent' returns additional duplicate closure messages along with the expected closing message

</td><td>

When the user enters a closing utterance, the agent returns multiple closure messages, and the last two messages are duplicated.

</td><td>

1.  Open NAP.
2.  Enter an utterance like 'Help me get details of a problem'.

Observe that the agent returns a response like 'Could you please provide the problem number you'd like details for?'.

3.  Enter an utterance like 'See you later'.

 Expected behavior: The agent returns a response like 'Understood. Feel free to return anytime if you need help.'

 Actual behavior: Additional closure messages show up, and the last two messages are duplicated. For example, the agent might return the following: 'Understood. Feel free to return anytime if you need help. Thanks for chatting! I'll go ahead and close this conversation now. I'm here if you need anything else. It looks like you're finished with this chat, so I'll go ahead and close it. It looks like you're finished with this chat, so I'll go ahead and close it.'.

</td></tr><tr><td>

Virtual Agent

 PRB2035888

</td><td>

A Guardian-triggered async\_search early-return leaves a stale task ID in the context

</td><td>

 

</td><td>

1.  Send a prompt that Guardian flags.

Observe that it's displayed correctly. Also, observe that the first request is still active but times out later.

2.  Send a second utterance that triggers skill Discovery immediately.
3.  Wait for a timeout from the first message to occur to display a 'sorry' message in the conversation.

 Expected behavior: The second utterance responds normally.

 Actual behavior: 'Sorry, there was a problem on my side' appears. The second utterance result is dropped.

</td></tr><tr><td>

Virtual Agent

 PRB2037636

 [KB3108272](https://hi.service-now.com/kb_view.do?sysparm_article=KB3108272)

</td><td>

Agent messages containing URLs aren't displaying correctly in the internal transcript

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB2054519

</td><td>

Rename five assistant names from 'Now Assist' to 'Otto'

</td><td>

The old assistant names should be renamed as following: 'Now Assist in Virtual Agent' &gt; 'ServiceNow Otto for Virtual Agent', 'Now Assist Panel – Platform' &gt; 'ServiceNow Otto panel – Platform', 'Now Assist Panel – Developer' &gt; 'ServiceNow Otto panel – Developer', 'Now Assist Voice Deployment' &gt; 'ServiceNow Otto voice', 'Now Assist in Virtual Agent - N' &gt; 'New chat assistant - 1', and 'Now Assist Voice Development - N' &gt; 'New voice assistant - N'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2055706

</td><td>

Snc\_internal role is missing on sys\_cs\_conversation write ACL when the 'Explicit Roles' plugin is also active

</td><td>

Since the snc\_internal role is never associated to the ACL, any users with snc\_internal role can't upload files from NextWave conversation experience. The /api/now/upload/attachment API checks for write access on the actual record itself before allowing file upload, so the upload API is failing.

</td><td>

1.  Provision a Zurich instance with the 'Explicit Roles' plugin \(com.glide.explicit\_roles\) and the Conversation Server plugin \(com.glide.cs\) installed.
2.  Navigate to an ACL on sys\_cs\_conversation table with write operation on record.

 Observe that only the snc\_external role is added. The snc\_internal role is never associated to this ACL.

</td></tr><tr><td>

Virtual Agent

 PRB2056495

</td><td>

Central cache doesn't return the correct entry if the cache is updated from a different cluster

</td><td>

In the central cache log, the following message appears: 'Negative cache hit — Glide previously returned null for this key'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2057596

</td><td>

Rename 'Now Assist Virtual Agent' to Otto for topics in Glide

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2058703

</td><td>

Generating a KB article throws an error

</td><td>

The following error appears: 'Configured callback URL for the KB generation topic is invalid: https:​/​/​nextwave-​preview-​internal- ​c003.​aus100.​service-​now.​com'.​

</td><td>

1.  Create an instance, following the documentation for setting up NextWave instances.
2.  Navigate to now-assist-admin.
3.  Make sure the KB Generation skill is active and the display for NAP\(OTTO\) channel is active.
4.  Give the prompt 'Create the KB for INCXXXXXXX' or 'Generate KB article'.

 Observe that there are three potential outcomes. First, the AI output could be: 'I wasn't able to generate the KB article because the configured callback URL for the KB generation topic is invalid'.

 Second, the AI output could be: 'I'll help you create a knowledge article. Let me first retrieve the incident details to understand what information should be included in the KB'. Then the execution stops. It doesn't collect any information nor create any article. The error code is 200102.

 Finally, it might not use the KB Generation skill. Instead, it uses knowledge graph or basic reasoning to form a draft article in the NAP window.

</td></tr><tr><td>

Virtual Agent

 PRB2058728

</td><td>

Chat summary isn't generated on instances with the Spanish translation plugin

</td><td>

After ending a chat between a requester and an agent, the summary doesn't generate. This occurs when one person is using Spanish and the other is using English.

</td><td>

1.  Provision an instance with the Spanish translation plugin installed.
2.  Set Spanish as the language for the requester.
3.  Set English as the language for the agent.
4.  Make sure DT is enabled.
5.  As the requester, initiate a chat and connect with the agent.
6.  Exchange around 20 messages.
7.  As the requester, end the chat.

 Observe that the chat summary doesn't generate.

</td></tr><tr><td>

Virtual Agent

 PRB2059089

</td><td>

The Otto session isn't aware of the logged-in user for 'assets managed by me' queries

</td><td>

The Otto/AICT chat session isn't aware of the logged-in user by default. When a user asks a question like 'Can you give me the assets managed by me?', the assistant returns the complete/unfiltered list of assets instead of applying a managed\_by = current user filter. The filter is only applied when the user explicitly names themselves in the query. The assistant should recognize 'me'/'my' references and automatically apply the logged-in session user's context without requiring explicit clarification.

</td><td>

1.  Log in as an AICT user.
2.  Ask Otto: 'Can you give me the assets managed by me?'.

Observe that the full/unfiltered asset list is returned instead of being filtered to the current user.

3.  Ask explicitly by name, for example: 'assets managed by &lt;username&gt;'.

 Observe that the managed\_by = current user filter is correctly applied.

</td></tr><tr><td>

Virtual Agent

 PRB2059632

</td><td>

BuildPolicyConfig should be aligned with sys\_​now\_​assist \_​va\_​persona\_​detail schema

</td><td>

No policy configs are returned because buildPolicyConfig doesn't target sys\_​now\_​assist \_​va\_​persona\_​detail and doesn't filter by persona\_detail\_type = Policy.

</td><td>

1.  Create an active record in sys\_​now\_​assist\_​va\_​persona\_​detail:​
    -   Deployment = a valid deployment sys\_id.
    -   Persona\_detail\_type = Policy.
    -   Name = Test Policy.
    -   Description = Test policy description.
    -   Prompt\_value = Test policy instruction.
2.  For the same deployment, create another active persona-detail record with persona\_detail\_type = Tone and prompt\_value = Friendly.
3.  Trigger the assistant-config handshake for that deployment via next wave.
4.  Inspect policyConfigs in the response.

 Expected behavior: One policy config entry is returned, containing the sys\_id, name, description, active, and instruction from the policy persona-detail record. Non-policy persona-detail records are excluded.

 Actual behavior: No policy configs are returned because buildPolicyConfig doesn't target sys\_​now\_​assist\_​va\_​persona\_​detail and doesn't filter by persona\_detail\_type = Policy.

</td></tr><tr><td>

Virtual Agent

 PRB2060897

</td><td>

The 'promoted-skills' API doesn't return non-discoverable skills

</td><td>

 

</td><td>

1.  Create a skill.
2.  Call the 'promoted-skills' API.

 Expected behavior: The skill should be returned.

 Actual behavior: The skill isn't returned.

</td></tr><tr><td>

Virtual Agent

 PRB2061042

</td><td>

Fixes are needed for guest user support for OffGlide

</td><td>

Additional rest endpoints need a public role. The NextWave token needs to be turned on for bff exchange.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2061520

</td><td>

Calling the 'Bg channel' API with the same session ID isn't resuming the conversation

</td><td>

 

</td><td>

1.  Create a incident and assign it to the ZTSD worker.
2.  Once solution is proposed, reply with new comments.

 Expected behavior: The conversation, which is waiting for input, should resume back.

 Actual behavior: Creating a conversation and execution plan with the workflow as 'Default VA Workflow'.

</td></tr><tr><td>

Virtual Agent

 PRB2063396

</td><td>

Parallel tools execution aren't running in record domain

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2064355

</td><td>

Auto Chat executions are faulted

</td><td>

There is an intermittent failure in fetching the JWT token from CS, which is causing the faulted conversations.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2064833

</td><td>

A domain is set to null after user input

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2066077

</td><td>

Add the reduce\_items\_list\_polling toggle

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Window Manager

 PRB2052078

</td><td>

Resize doesn't work at run time, only on creation time

</td><td>

The talk modal needs to be a fixed size. The user dragging it smaller breaks the layout, so the grip should be disabled at runtime.

</td><td>

Try \{canResize: false\}.

 Expected behavior: The gripper disappears.

 Actual behavior: There's no change.

</td></tr><tr><td>

Window Manager

 PRB2052105

</td><td>

SetWindowProperties ignores empty headingLabel and it can't clear a window's title at runtime

</td><td>

The previous title stays. '' and null are silent no-ops.

</td><td>

1.  Open a window with a heading \(for example, the canvas window with any headingLabel\).
2.  Call setWindowProperties\(windowId, \{ headingLabel: '' \}\).

 Expected behavior: The heading clears, resulting in a blank title.

 Actual behavior: The previous title stays. '' and null are silent no-ops.

</td></tr><tr><td>

Work Order Management

 PRB2035667

</td><td>

Intraday optimization is stuck in 'In progress'

</td><td>

During normal intraday runs with concurrent solution processing, the race condition between SolutionMetadataProcessor and SolutionProcessorSNC can cause lost updates on ml\_solution.solution\_metadata. This results in stuck in\_progress records.

</td><td>

1.  Configure Schedule Optimization with intraday optimization enabled with territory model.
2.  Set up an intraday optimization schedule with multiple overlapping territories.
3.  Trigger an intraday optimization run.
4.  Check wm\_intraday\_job\_m2m\_qualifier.

 Observe that some of the records remain stuck in the in\_progress status indefinitely, even after all the solutions are processed or the records show no processed task counts, total task counts, and/or progress bar.

</td></tr></tbody>
</table>## Fixes included in Zurich Patch 12

These prior versions contain PRB fixes that are also included with Zurich Patch 12. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich patch 11 Hotfix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3143608)
-   [Zurich Patch 11 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3140570)
-   [Zurich Patch 11](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-11.md)
-   [Zurich Patch 10 Hotfix 5](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3142080)
-   [Zurich Patch 10 Hotfix 4a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3143606)
-   [Zurich Patch 10 Hotfix 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10-hf-4-PO.md)
-   [Zurich Patch 10 Hotfix 3a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3138481)
-   [Zurich Patch 10 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3135835)
-   [Zurich Patch 10](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-10.md)
-   [Zurich Patch 9 Hotfix 6](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3137633)
-   [Zurich Patch 9 Hotfix 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9-hf-5-PO.md)
-   [Zurich Patch 9](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-9.md)
-   [Zurich Patch 8 Hotfix 5](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3137636)
-   [Zurich Patch 8](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-8.md)
-   [Zurich Patch 7b Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3137129)
-   [Zurich Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-7.md)
-   [Zurich Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-6.md)
-   [Zurich Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-5.md)
-   [Zurich Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-4.md)
-   [Zurich Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-3.md)
-   [Zurich Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-2.md)
-   [Zurich Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-patch-1.md)
-   [Zurich security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-security-notables.md)
-   [All other Zurich fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/zurich-all-other-fixes.md)

## Store app versions included in Zurich Patch 12m

<table><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

@servicenow/sn-enhanced-content-editor

</td><td>

2026-08-07 00:00:00

</td><td>

OTTO Rebranding.

</td></tr><tr><td>

Impact

</td><td>

2026-08-07 00:00:00

</td><td>

Impact Store App - August Release.

 1. Scan Engine Definition Enhancements - Restored sys\_properties Scanning.

 Customers can once again add sys\_properties directly as an Applicable Table target in Scan Engine Definitions, using any conditions they choose.

 This capability was temporarily removed one release ago, which required customers to use a dedicated 'Sys Property' definition type \(system property name + condition\) to check properties. Based on customer feedback, the August release restores the original free-form scanning approach for sys\_properties - customers now have both options available:

 -   Direct table scanning of sys\_properties with custom conditions \(restored\).
-   The 'Sys Property' definition type \(system property name + condition\).

 2. On-Demand Accelerators - Defects and Enhancements.

 This release includes a set of defect fixes and enhancements for On-Demand Accelerators, improving reliability and overall performance of the accelerator experience.

</td></tr><tr><td>

ServiceNow Otto for Manufacturing Commercial Operations \(MCO\)

</td><td>

2026-08-07 00:00:00

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Impact Common

</td><td>

2026-08-07 00:00:00

</td><td>

Impact Store App - August Release.

 1. Scan Engine Definition Enhancements - Restored sys\_properties Scanning.

 Customers can once again add sys\_properties directly as an Applicable Table target in Scan Engine Definitions, using any conditions they choose.

 This capability was temporarily removed one release ago, which required customers to use a dedicated 'Sys Property' definition type \(system property name + condition\) to check properties. Based on customer feedback, the August release restores the original free-form scanning approach for sys\_properties - customers now have both options available:

 -   Direct table scanning of sys\_properties with custom conditions \(restored\).
-   The 'Sys Property' definition type \(system property name + condition\).

 2. On-Demand Accelerators - Defects and Enhancements.

 This release includes a set of defect fixes and enhancements for On-Demand Accelerators, improving reliability and overall performance of the accelerator experience.

</td></tr><tr><td>

Impact Content

</td><td>

2026-08-07 00:00:00

</td><td>

Impact Store App - August Release.

 1. Scan Engine Definition Enhancements - Restored sys\_properties Scanning.

 Customers can once again add sys\_properties directly as an Applicable Table target in Scan Engine Definitions, using any conditions they choose.

 This capability was temporarily removed one release ago, which required customers to use a dedicated 'Sys Property' definition type \(system property name + condition\) to check properties. Based on customer feedback, the August release restores the original free-form scanning approach for sys\_properties - customers now have both options available:

 -   Direct table scanning of sys\_properties with custom conditions \(restored\).
-   The 'Sys Property' definition type \(system property name + condition\).

 2. On-Demand Accelerators - Defects and Enhancements.

 This release includes a set of defect fixes and enhancements for On-Demand Accelerators, improving reliability and overall performance of the accelerator experience.

</td></tr><tr><td>

Impact Value Management - ITSM

</td><td>

2026-08-07 00:00:00

</td><td>

This release upgrades the Data Collection App for ITSM with an expanded set of value-measurement metrics.

 All existing metrics remain unchanged. No modifications have been made to current functionality. This release only adds net-new metrics that extend value-measurement capabilities across the supported products.

 For the complete list of new metrics, please refer to the Supporting Document.

 Enhanced Metrics.

 Any new metric introduced with this release is classified as an Enhanced Metric. Enhanced Metrics can be collected, and their data will be visible on the data dashboard included with the Data Collection App.

 Important: Automatic data transfer of Enhanced Metrics to ServiceNow's centralized Impact Delivery Instance is not supported.

 To make Enhanced Metric data available on the Impact Delivery Instance, customers must:

 -   Install the Impact In-Platform App, and.
-   Enable ServiceBridge.

 Both steps are mandatory for Enhanced Metric data to appear on the Impact Delivery Instance.

</td></tr><tr><td>

Scan Engine

</td><td>

2026-08-07 00:00:00

</td><td>

-   Scan-time completion warnings - Added warnings during scan execution when the selected Suite Scan may not meet the requirements needed to complete an Update Set or application workflow.
-   New: statistical rule detection type - Added support for a new statistic detection type for Scan Engine statistical rules, including schema validation and compile/decompile support.

 Clearer Suite Scan messaging - Improved labels, descriptions, and enforcement messaging for Update Set and Application Suite Scan settings. Users now receive clearer guidance when Suite Scan is unavailable, including restricted actions and recommended next steps.

 -   Full-table custom definition scanning restored - Restored support for custom Scan Engine definitions that scan entire tables. Additional warning guidance is now provided when targeting the System Properties table.
-   Improved Platform Health Analytics dashboard performance to reduce load times.
-   Corrected findings count inconsistencies in Platform Owner dashboard views.
-   Fixed: Update Set enforcement issues when complex AND/OR conditions are configured.
-   Resolved exception-handling issues affecting findings during rescans.
-   Corrected clone behaviour for resolved finding history records.
-   Fixed: localisation issues in My Resolved Findings.
-   Resolved UI branding and consistency issues across Health Findings, and AI Code Review pages.

</td></tr><tr><td>

Manufacturing Commercial Operations AI agents collection

</td><td>

2026-08-07 00:00:00

</td><td>

Https://docs-preview.corp.service-now.com/bundle/australia-release-notes/page/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

SOM for Manufacturing Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Https://www.servicenow.com/docs/r/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Certificate Inventory and Management

</td><td>

2026-08-07 00:00:00

</td><td>

Fixed: Refined the access control list \(ACL\) role permissions required to access certificate inventory and management records.

</td></tr><tr><td>

Manufacturing Commercial Operations Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Https://www.servicenow.com/docs/r/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Alert Rules Management

</td><td>

2026-08-07 00:00:00

</td><td>

--- AI Generated Release Notes ---.

 All references to 'Now Assist' have been updated to 'ServiceNow Otto' across IT Operations Management \(ITOM\) features. UI labels, flow descriptions, action descriptions, and rule labels now consistently use the 'ServiceNow Otto' name, replacing the previous 'Now Assist' terminology.

</td></tr><tr><td>

Knowledge Capabilities in UI Builder

</td><td>

2026-08-07 00:00:00

</td><td>

Auto-update, auto-merge and otto branding updates.

</td></tr><tr><td>

ServiceNow Otto for Voice Agents

</td><td>

2026-08-07 00:00:00

</td><td>

-   STT Key Term Dictionary - Administrators can now configure custom key terms within language settings to improve speech-to-text recognition accuracy for domain-specific vocabulary.
-   Conversational Quality Controls - Voice pacing and readability settings are now configurable via the Agents API, enabling more natural and controlled interactions.
-   Expanded Language and amp; Voice Support - Added support for the following languages: Finnish, Czech, Slovakian, and Ukrainian.
-   Resolved an issue where the Test Assistant UI displayed empty message bubbles when a secondary language was enabled.
-   Fixed: a plan handler error that prevented incoming plan IDs from being accepted correctly.
-   Updated default values on out-of-box deployments to reflect current configuration requirements.

 Rebranding to ServiceNow Otto - ServiceNow Otto is the AI experience brand going forward. All product references to Now Assist have been updated to the ServiceNow Otto naming convention.

</td></tr><tr><td>

Remedial Actions Framework

</td><td>

2026-08-07 00:00:00

</td><td>

-   Admins can now configure remedial actions for both device and non-device scenarios. The system supports defining remedial actions with an action type \(device or non-device\), consent requirements, and applicability for specific roles such as AI Specialist.
-   API consumers can now retrieve remedial actions by applicability. An API endpoint is available to fetch a list of remedial actions relevant to a specified applicability, including action identifiers, names, and consent requirements.

</td></tr><tr><td>

SOM for Manufacturing Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Https://www.servicenow.com/docs/r/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Service Operations Workspace Alert Automation

</td><td>

2026-08-07 00:00:00

</td><td>

Added.

 -   Support multi-line text in enrich automation compose actions using a and lt;br and gt; tag.
-   When creating incidents in response automations, you can now set an incident field to a static value.

 Now Assist has been renamed to ServiceNow Otto.

</td></tr><tr><td>

Service Operations Workspace Alert Automation UI

</td><td>

2026-08-07 00:00:00

</td><td>

Added.

 -   Support multi-line text in enrich automation compose actions using a and lt;br and gt; tag.
-   When creating incidents in response automations, you can now set an incident field to a static value.

 Now Assist has been renamed to ServiceNow Otto.

</td></tr><tr><td>

Process Automation Designer

</td><td>

2026-08-07 00:00:00

</td><td>

-   Playbooks as MCP tools: Access and run your Playbooks directly from your favorite MCP client.
-   New 'run as' option: The Hybrid Agentic Activity and Use an AI Agent activity now support running as the user who completed the previous activity.
-   Expanded autonomous mode: Hybrid Agentic Activity autonomous mode now supports custom form-based activities, with operations configurable in the activity definition.

 Updated default model: Playbook generation skills now default to Azure OpenAI instead of NowLLM.

</td></tr><tr><td>

Manufacturing Commercial Operations Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Https://www.servicenow.com/docs/r/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Human Resources: Service Portal

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Impact Health Content

</td><td>

2026-08-07 00:00:00

</td><td>

 

</td></tr><tr><td>

Event Management Connectors

</td><td>

2026-08-07 00:00:00

</td><td>

-   Changed: Enhanced Dynatrace Event Connector to support Dynatrace Grail 3rd Gen APIs.
-   Enhanced Azure Event connector to support Azure issues from Azure monitor.

</td></tr><tr><td>

CPQ for Manufacturing Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Https://www.servicenow.com/docs/r/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

ServiceNow Otto for Contract Management Pro

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: ServiceNow Otto is the new AI experience brand. Now Assist in Contract Management is now ServiceNow Otto for Contract Management Pro.

</td></tr><tr><td>

CPQ for Manufacturing Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Https://www.servicenow.com/docs/r/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Service Operations Workspace Alert Automation API

</td><td>

2026-08-07 00:00:00

</td><td>

Added.

 -   Support multi-line text in enrich automation compose actions using a and lt;br and gt; tag.
-   When creating incidents in response automations, you can now set an incident field to a static value.

 Now Assist has been renamed to ServiceNow Otto.

</td></tr><tr><td>

Manufacturing Commercial Operations Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Https://www.servicenow.com/docs/r/release-notes/manufacturing-commercial-operations-rn.html.

</td></tr><tr><td>

Build Agent \(Trial\)

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: New Build Agent model integrations, including GPT-5.5, Gemini 3.5 Flash, and Opus 4.8.
-   Ability to select model versions directly from the Build Agent chat panel within ServiceNow Studio.
-   Ability to create new custom skills and rules at instance-wide, application, and user levels to tailor Build Agent's behavior.
-   Run background scripts securely within app-build flows, with rollback, scope-restriction, and dry-run containment paths.
-   Ability to handoff ServiceNow Otto conversations to Build Agent in ServiceNow Studio.
-   Ability to run Build Agent in Developer Sandboxes, allowing for better collaboration and isolation.
-   Automatically keep all the ATF tests in sync as your Build Agent written code evolves over time, toggled on via the 'Sync ATF tests with app' setting for Build Agent.
-   Automatically keep all the UI tests in sync as your Build Agent written code evolves over time, toggled via the 'Run UI ATF Tests' setting for Build Agent.
-   Get prompted to generate ATF tests anytime you invoke Build Agent, enabled via Build Agent settings.
-   Execute and troubleshoot ATF tests directly from the ServiceNow SDK.
-   Support for new knowledge base access metadata type.
-   More granular overview of tools per connected MCP server in Build Agent settings.
-   Expanded MCP Server support, including AWS DevOps, Box, Postman, and Sentry.
-   Context compaction enhancements.
-   Sub Agent memory improvements.

</td></tr><tr><td>

Employee Center

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Playbook Experience

</td><td>

2026-08-07 00:00:00

</td><td>

Rebranding: Updated branding in Hybrid agentic activity and Use an AI agent from NowAssist to ServiceNow Otto.

</td></tr><tr><td>

Playbook Experience Components

</td><td>

2026-08-07 00:00:00

</td><td>

Rebranding: Updated branding in Hybrid agentic activity and Use an AI agent from NowAssist to ServiceNow Otto.

</td></tr><tr><td>

AI Agents for Retail Service Management

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: the plugin name \(AI Agents for Retail Service Management\).

</td></tr><tr><td>

AI Data Kit

</td><td>

2026-08-07 00:00:00

</td><td>

-   Added validations to ensure Dataset and Data Collection names are unique.
-   All in-product UI strings, labels, tooltips, banners, and documentation that mention 'Now Assist' were retranslated and repackaged in line with the Otto naming guidelines.
-   Discovery Experience - DataKit Admins and analysts can search for datasets by either name or description.

</td></tr><tr><td>

Field Service Management AI agent collection

</td><td>

2026-08-07 00:00:00

</td><td>

Fluent based development support added.

 ServiceNow Otto is the new Al experience brand. This change is reflected in the name of ServiceNow products, including Field Service Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

RSM - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist is becoming ServiceNow Otto. Otto is the unified AI experience through which people interact with ServiceNow's intelligence in natural language to get work done.

</td></tr><tr><td>

Spend and Savings Management

</td><td>

2026-08-07 00:00:00

</td><td>

Applied security hardening to address CVE-2025-3648.

</td></tr><tr><td>

SLO - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, references to Now Assist have been replaced with ServiceNow Otto.

</td></tr><tr><td>

Now Assist for Digital End-user Experience \(DEX\)

</td><td>

2026-08-07 00:00:00

</td><td>

A new AI agent can diagnose and resolve slow computer issues reported through an incident or self-service, checking live device health across disk, CPU, memory, and network, and automatically applying the right fix - from killing resource-heavy processes to freeing up disk space.This change integrates with ZTS so will not be published until ZTS is GA.

</td></tr><tr><td>

ServiceNow Otto for AI Search

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist in AI Search has been renamed to ServiceNow Otto for AI Search, reflecting ServiceNow's broader AI product branding. References throughout the product experience have been updated accordingly.

 -   Synthesized Answer consistency for Gemini and Anthropic models. Addressed inconsistent prompt instructions that resulted in and lt;response and gt; field to sometimes appear under and lt;thinking and gt; and sometimes be missing altogether, causing streaming issues.
-   Added sys\_property gate to skip catalog price field in GR citation builder to avoid performance degradation.

</td></tr><tr><td>

RSM - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist is becoming ServiceNow Otto. Otto is the unified AI experience through which people interact with ServiceNow's intelligence in natural language to get work done.

</td></tr><tr><td>

Service Operations Workspace Alert Mngmt

</td><td>

2026-08-07 00:00:00

</td><td>

-   Admins can set static values for incident fields in Event Management response automations. When creating incidents via advanced response automation, users can now assign fixed values or map alert fields to incident fields, restoring and extending previous functionality.
-   Admins can enter free text in the Create Incident Advanced subflow. The UI now supports free text input for incident field customization during incident creation in response automations.
-   Migration script updates the JSON formats for custom fields used in incident creation automations. A fix script migrates legacy data in incident field mapping to the new JSON format, ensuring compatibility and data integrity.
-   Compose actions now support multiline text. Users can enter, view, and edit structured, multi-line content in Alert Automation compose fields, with line breaks preserved and bidirectional compatibility with UI16.

 Alert automation in the Service Operations Workspace no longer hangs when changing the language to Portuguese.

</td></tr><tr><td>

Health and Safety Incident Management

</td><td>

2026-08-07 00:00:00

</td><td>

Role-based access to Safety Knowledge Base articles. Health and Safety managers and agents can now contribute to knowledge articles in the Safety Knowledge Base, while case requestors have read-only access.

 The active status of Health and Safety incident records now updates correctly when the state changes from Closed to Work in Progress.

</td></tr><tr><td>

ServiceNow Otto for Financial Services Operations \(FSO\)

</td><td>

2026-08-07 00:00:00

</td><td>

-   Changed: Updated internal application components to support ongoing platform enhancements.
-   Updated 'ServiceNow Otto' branding for ServiceNow Otto for Financial Services Operations \(FSO\).

</td></tr><tr><td>

Service Operations Workspace UI Components

</td><td>

2026-08-07 00:00:00

</td><td>

Otto rebranding changes.

</td></tr><tr><td>

DEX Content Playbook

</td><td>

2026-08-07 00:00:00

</td><td>

See DEX Application and Device Health product for release notes. This app is a dependency of DEX Application and Device Health.

</td></tr><tr><td>

Recommended Actions for ITSM

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Now Assist Multi-Content Response Genius Results support.

</td></tr><tr><td>

Core Business Suite Advanced for Legal

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Software Asset Management

</td><td>

2026-08-07 00:00:00

</td><td>

In this version, minor defects affecting reconciliation flow performance and lifecycle report have been resolved. System behavior is now consistent and reliable in these areas.

</td></tr><tr><td>

Service Operations Workspace ITSM Common

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

Health and Safety Contractor Management

</td><td>

2026-08-07 00:00:00

</td><td>

Version bump only, because the hs-core version was updated. No new features delivered. Fixed one defect related to adding a worker in Brazil.

</td></tr><tr><td>

Service Operations Workspace Integrations launchpad

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated ServiceNow Otto branding for HLA data inputs integrations.

</td></tr><tr><td>

Problem Management for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

Build Agent Premium

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: New Build Agent model integrations, including GPT-5.5, Gemini 3.5 Flash, and Opus 4.8.
-   Ability to select model versions directly from the Build Agent chat panel within ServiceNow Studio.
-   Ability to create new custom skills and rules at instance-wide, application, and user levels to tailor Build Agent's behavior.
-   Run background scripts securely within app-build flows, with rollback, scope-restriction, and dry-run containment paths.
-   Ability to handoff ServiceNow Otto conversations to Build Agent in Studio.
-   Ability to run Build Agent in Developer Sandboxes, allowing for better collaboration and isolation.
-   Automatically keep all the ATF tests in sync as your Build Agent written code evolves over time, toggled via the 'Sync ATF tests with app' setting for Build Agent.
-   Automatically keep all the UI tests in sync as your Build Agent written code evolves over time, toggled via the 'Run UI ATF Tests' setting for Build Agent.
-   Get prompted to generate ATF tests anytime you invoke Build Agent, enabled via Build Agent settings.
-   Execute and troubleshoot ATF tests directly from the ServiceNow SDK.
-   Support for new knowledge base access metadata type.
-   More granular overview of tools per connected MCP server in Build Agent settings.
-   Expanded MCP Server support, including AWS DevOps, Box, Postman, and Sentry.
-   Context compaction enhancements.
-   Sub Agent memory improvements.

</td></tr><tr><td>

ServiceNow Otto for Retail Service Management

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist is becoming ServiceNow Otto. Otto is the unified AI experience through which people interact with ServiceNow's intelligence in natural language to get work done.

</td></tr><tr><td>

Portfolio Planning with PPM, Agile 2.0, and SAFe

</td><td>

2026-08-07 00:00:00

</td><td>

Fixed: an L10 Warning and can now read property 'isValid' from undefined from 'Sync Data from execution to alignment' flow.

</td></tr><tr><td>

AIOps Dashboards

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: AIOps 360 view dashboard now quantifies AI-driven operational value. The dashboard introduces a widget that displays the time saved by AI, counting the alerts AI closed as insignificant or analyzed and provided insights or next-step recommendations, contributing to time savings \(Note that Admins can adjust the time-saving definitions for this calculation\).
-   Adding a new resolution type for alerts closed as insignificant, 'Closed by AI'. This info is added to the AIops 360 view dashboard heatmap chart for improved visibility of AI-driven outcomes.

</td></tr><tr><td>

AI Agents for Core Business Suite

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

ServiceNow Otto for Field Service Management

</td><td>

2026-08-07 00:00:00

</td><td>

Fluent based development support added.

 ServiceNow Otto is the new Al experience brand. This change is reflected in the name of ServiceNow products, including Field Service Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

Enhanced Features for IRM Enterprise

</td><td>

2026-08-07 00:00:00

</td><td>

 

</td></tr><tr><td>

Content Pack for CMDB

</td><td>

2026-08-07 00:00:00

</td><td>

-   Allow specific CI Classes to be excluded from Service Graph Connector recommendations. For example cmdb\_ci\_ot to be excluded for Hardware Asset Management use cases.
-   Updated logic to retrieve Service Graph Connector recommendations only if mappings exist to the specific CI Class, not to its base classes.

</td></tr><tr><td>

ServiceNow Otto for Virtual Agent Configurations

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Otto renaming changes.

</td></tr><tr><td>

RSM - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist is becoming ServiceNow Otto. Otto is the unified AI experience through which people interact with ServiceNow's intelligence in natural language to get work done.

</td></tr><tr><td>

Core Business Suite Foundation for Workplace Services

</td><td>

2026-08-07 00:00:00

</td><td>

Shipped out-of-the-box Workplace Services knowledge base.

 Owners and managers can be defined by the admin for the knowledge base in the Core Business Suite configuration console to ensure proper governance and content tracking.

 Shipped Now Assist search sources for Workplace Services for Knowledge article generation from workplace case table on the Knowledge center.

 Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

Form data collector

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated internal config properties.

</td></tr><tr><td>

Sales Common

</td><td>

2026-08-07 00:00:00

</td><td>

Minor performance improvements and defect fixes.

</td></tr><tr><td>

ERP Rapid Deployment Packs

</td><td>

2026-08-07 00:00:00

</td><td>

-   Manage the full life cycle of data records across business domains through the MDM Orchestrator.
-   Review and act on transactions, data records, and month-end journal entries from a single location through the centralized Approvals Hub.
-   Validate and authorize manual journal entries before they post to the general ledger through the Journal Entry Approval Portal.

</td></tr><tr><td>

Core Business Suite Advanced for Health and Safety

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, Now Assist for Sourcing and Procurement Operations is now ServiceNow Otto for Sourcing and Procurement Operations.

</td></tr><tr><td>

Service Operations Workspace ITSM Admin Center

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

ITOM Cloud Services Core

</td><td>

2026-08-07 00:00:00

</td><td>

-   Detect and automatically remediate common ICS configuration issues directly from the Diagnostics page.
-   Added ADCv2 and mTLS prerequisite checks to the System Property card, flagged in red when either is missing.
-   Improved alerting reliability for CnC keepalive REST request error monitoring.
-   Corrected ICS integration user setup so service accounts are provisioned with the right access by default.
-   Updated underlying platform components for improved stability and forward compatibility.

</td></tr><tr><td>

Screen Summarization

</td><td>

2026-08-07 00:00:00

</td><td>

Updated icon and wording to align with ServiceNow's latest AI visual experience.

</td></tr><tr><td>

Service Operations Workspace Log Analytics

</td><td>

2026-08-07 00:00:00

</td><td>

Hidden app.

</td></tr><tr><td>

AI Authoring for Catalog Builder

</td><td>

2026-08-07 00:00:00

</td><td>

Rebranding: The 'Now Assist' branding in conversational Catalog Builder has been replaced with 'ServiceNow Otto', backed by new automated test coverage.

</td></tr><tr><td>

AI Agents for Talent

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

</td></tr><tr><td>

GRC Common GenAI

</td><td>

2026-08-07 00:00:00

</td><td>

\*\*New\*\* None \*\*Changed\*\* ServiceNow Otto for Integrated Risk Management branding is now applied across relevant products.All references to 'Now Assist for IRM' have been updated to 'ServiceNow Otto for Integrated Risk Management' in the Australia Patch5 and Zurich latest patch releases. \*\*Fixed\*\* None \*\*Removed\*\* None.

</td></tr><tr><td>

SPO - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, references to Now Assist have been replaced with ServiceNow Otto.

</td></tr><tr><td>

ServiceNow Otto for Error Framework

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: AMB Insights introduced.

</td></tr><tr><td>

Workflow Studio

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Branding changes from Now Assist to Otto, the new ServiceNow AI companion.

</td></tr><tr><td>

Portfolio Planning

</td><td>

2026-08-07 00:00:00

</td><td>

-   View the demand summary card on the AI Overview tab of the demand record page when the demand summarization skill is active and accessible.
-   View and filter demand data using the Overview, Financials, and Data Quality tabs in Demands Dashboard.
-   View and manage cost plans, benefit plans, and baselines from the Financials grid in Demands.
-   Switch between the Dashboard and List views in Demands using the breadcrumb navigation.
-   View a related list of similar demands on the demand record page for quick access to system-identified matches.
-   Explore detailed data directly from the Demands Dashboard widgets using the widget drill-down capability.
-   Track Risks, Issues, Decisions, Actions, and Changes \(RIDAC\) for planning items directly within the workspace using related lists and configurable views on record pages, with role-based access for viewing and editing.
-   Use the L2 RIDAC menu to view all RIDAC items, project-specific RIDAC, portfolio risks, and program risks. Note that certain fields are read-only during and after creation.

 The portfolio financials page now displays a budget value of 0 for planning items without an approved budget, ensuring accurate variance calculations and eliminating blank values.

 -   Resolved an accessibility issue where the screen reader announced the value of the Rows Per Page dropdown more than once in Portfolio Planning.
-   Resolved an accessibility issue where roadmap keyboard shortcuts appeared as a one-time popup when tabbing through the interface. Shortcuts are now persistently accessible from the side panel.
-   Removed: the % Complete label from demand bars in the Roadmap tab, demand cards in the Kanban tab, and the % Complete column for demand rows in grid and list views, as demands do not support percent complete calculations.
-   Removed: the standalone demand summarization component from the demand record page in Next Experience for Demand Management. The summary now appears only within the AI Overview tab.

</td></tr><tr><td>

IT Service Management AI agent collection

</td><td>

2026-08-07 00:00:00

</td><td>

-   AI can now automatically complete Change Risk Assessment and Dynamic Schema questions based on the change record's context, showing its reasoning for each answer so admins and change managers can verify or correct it. Answers that identify compliance exposure \(for example SOX, PCI-DSS, or HIPAA\) automatically populate the matching Dynamic Schema fields.
-   A new AI agent can diagnose and resolve common Okta account lockouts and MFA failures reported through an incident or self-service, checking live account status and submitting the correct unlock or reset request automatically.
-   A new Teams-native AI agent lets shift agents manage on-call coverage directly in chat - requesting coverage or leave, and asking questions like 'who is on call' or 'when is my next shift.'.

 The DEX Diagnosis AI agent now factors in event monitoring logs and statistical anomaly signals alongside existing telemetry for more accurate root-cause diagnoses, and now surfaces the specific evidence behind each conclusion.

 -   Fixed: an issue where several AI agents \(including Zscaler, Installed Apps, and Modern Change agents\) had read-only configuration, preventing customers from disabling them.
-   Fixed: an issue where the Zscaler and Installed Apps agents' action engagement tools showed an empty timeout field.
-   Fixed: a date-formatting issue in the Change Outage Assistant AI agent.
-   Fixed: a security issue that allowed any authenticated user, regardless of role, to invoke ITSM AI agents and skills that should have been role-restricted.
-   Fixed: an issue where the incident investigation and resolution workflow could fail with an 'incident search/read service unavailable' error.
-   Fixed: an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
-   Reduced processing time for the Generate Change Request Plans AI flow, which had been taking an unusually long time to complete.
-   Fixed: an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform.
-   Fixed: an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users.
-   Fixed: an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own.

 No items removed in this release.

</td></tr><tr><td>

ServiceNow Studio

</td><td>

2026-08-07 00:00:00

</td><td>

This app is a dependency of ServiceNow Studio + ServiceNow IDE. Please see release notes for parent app.

</td></tr><tr><td>

Finance and Procurement - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Updated the plugin name and details to Finance and Procurement - Foundation.

</td></tr><tr><td>

Employee Profile

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

AI Dashboard Insights

</td><td>

2026-08-07 00:00:00

</td><td>

-   Personalized dashboard summary output.
-   Improved summary for multi-page lists.
-   Configurable default active skills in AI Admin Hub.
-   Support for updated third-party models.

 Renamed Otto context menu labels.

</td></tr><tr><td>

GRC: Vendor Risk Management Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

-   Rebranded to ServiceNow Otto, replacing Now Assist references for a consistent AI experience.
-   Enhanced MRA authorization validation to ensure access checks are consistently enforced during record association.

</td></tr><tr><td>

Portfolio Planning Core

</td><td>

2026-08-07 00:00:00

</td><td>

Resolved an issue where execution URL and demand menu links from the portfolio plan grid, Kanban, and roadmap were broken due to a URL change introduced with the new L2 navigation.

</td></tr><tr><td>

POM - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, references to Now Assist have been replaced with ServiceNow Otto.

</td></tr><tr><td>

ServiceNow Otto for AIRC

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: ServiceNow OTTO Branding Updates Updated the application to reflect the new ServiceNow OTTO branding, replacing Now Assist references and providing a more consistent AI experience across the platform.

</td></tr><tr><td>

Employee Slate \(built for Now Assist\)

</td><td>

2026-08-07 00:00:00

</td><td>

-   Introduced topic-based content discovery with category-based navigation in Employee Slate, updating the browse experience.
-   Enhanced org charts with responsive layouts, profile cards redesign, and team visualization.
-   Provided field visibility controls on knowledge articles.
-   Introduced configuration scope controls so task configs and Lit-based action widgets can independently target Employee Center or Employee Slate, enabling teams to ship new configs with existing mappings.
-   Introduced task record preprocessing for skills to fetch context, enrich records, and format output before skill invocation.
-   Rebranded Now Assist, Moveworks, and AI Experience to Otto for consistency.

</td></tr><tr><td>

Digital Experience Score

</td><td>

2026-08-07 00:00:00

</td><td>

See DEX Application and Device Health product for release notes. This app is a dependency of DEX Application and Device Health.

</td></tr><tr><td>

ServiceNow Otto for IT Operations Management \(ITOM\)

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: AIOps AI Specialist: Operator-reopened alerts get full AI investigation automatically. When a human operator reopens an alert that the AI previously closed as noise, the system bypasses noise classification for the rest of that alert's lifecycle and runs a complete investigation - ensuring human overrides are respected and learned from.
-   AI-handled alerts are automatically returned to the original operator. After the AIOps AI Specialist completes its analysis or remediation, the alert is reassigned back to the human who originally owned it, preserving all AI-generated context and notes.
-   AWS Claude is now supported as an AI agent provider, expanding the choice of underlying AI models for automated workflows.
-   All Now Assist references changed to ServiceNow Otto.
-   AIOps AI Specialist: AIOps AI Specialist auto-assignment no longer overrides human ownership. The AIOps AI Specialist will not automatically take over alerts already assigned to a human operator, reducing unwanted reassignments and keeping accountability clear.
-   When the AIOps AI Specialist is manually triggered on a human-assigned alert, the alert returns to its original owner after AI processing - with configuration options to control behavior for noisy or previously assigned alerts.

 AIOps AI Specialist Fixes and improvements.

</td></tr><tr><td>

Major Incident Management for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

Employee Goals

</td><td>

2026-08-07 00:00:00

</td><td>

No customer facing changes were shipped in this version.

</td></tr><tr><td>

ServiceNow AI Lens Core

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: Use ServiceNow AI Lens from your browser to upload one or more files for AI Lens to analyze and auto-fill form fields - no installation required.
-   Use Lens as a Service to map the data from multiple related Excel column headers and values to a single ServiceNow table field.
-   Use Lens as a Service to auto-map an Excel column header and its values from a single Excel sheet to multiple ServiceNow table fields simultaneously.
-   Choose how AI Lens opens when you start a session - from your browser or the desktop application. You can update this preference at any time.

 Updated the AI experience branding in AI Lens to align with ServiceNow Otto naming and visual guidelines.

</td></tr><tr><td>

Flow Summarization

</td><td>

2026-08-07 00:00:00

</td><td>

Flow Summarization now defaults to optimal small third-party models for skills and agents. All skills and agents previously using Now LLM have been updated to use Google Gemini 3.5 Flash, OpenAI GPT 5.1, or OpenAI GPT 5.4 mini as the default model provider. These models have been tested and validated for the AP5/Australia release.

 ServiceNow Otto branding is now applied throughout Flow Summarization. All UI strings, labels, and icons referencing 'Now Assist' have been replaced with ServiceNow Otto naming and marks per Otto Naming Guidelines. Interactive surfaces now display the Otto mark, and background AI processes use the black Otto mark. Loading animations and field-level sparkles are flagged for PM review before updating. UX review has been completed prior to merge.

 Prompt Analyzer findings for Flow Summarization prompts have been reviewed and addressed. All prompt standards and best practice issues identified by Prompt Analyzer have been triaged or resolved for skills within Flow Summarization.

</td></tr><tr><td>

ServiceNow Otto for Platform Prime

</td><td>

2026-08-07 00:00:00

</td><td>

The application captures dependencies, updated the plugin dependencies for this release.

</td></tr><tr><td>

Request Management for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

Purchase Order Management

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, references to Now Assist have been replaced with ServiceNow Otto.

</td></tr><tr><td>

Service Operations Workspace ITSM Applications

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

Recommendation template

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: ServiceNow OTTO Branding Updates Updated the application to reflect ServiceNow's new OTTO branding, replacing Now Assist references for a consistent AI experience across the platform.

</td></tr><tr><td>

Query Generation

</td><td>

2026-08-07 00:00:00

</td><td>

Indicator Configuration - Allows users to promote indicators manually in AI Search results.

</td></tr><tr><td>

Service Operations Workspace Express List

</td><td>

2026-08-07 00:00:00

</td><td>

-   Express list now supports color-coded visual cues to highlight values \(based on existing definitions in sys\_highlighted\_value\). Admins can configure conditional formatting rules on alert columns \(e.g., severity, priority\) so that critical items are immediately visible through colored indicators and icons - no more scanning through uniform rows.
-   Azure Monitor Issues now surface related alerts in context. A new 'Related Records' tab appears directly in the alert view for Azure Monitor Issues, letting operators drill into associated alerts without leaving their current workflow.
-   Express List now fully supports right-to-left languages, including Arabic and Hebrew, with correct mirroring of layout, icons, and spacing.
-   All 'Now Assist' references across Service Operations Workspace, Express List, etc. have been rebranded to ServiceNow Otto.
-   The 'Probable Cause' tab in the Alerts Preview panel is now called 'Related Records' and includes Azure Monitor Issues.

 Express List no longer fails to load when a system property record has a missing type value.

</td></tr><tr><td>

ITSM Admin Experience Components

</td><td>

2026-08-07 00:00:00

</td><td>

No changes.

</td></tr><tr><td>

ITSM Employee Experience

</td><td>

2026-08-07 00:00:00

</td><td>

-   Simplified request experience for order guides on Employee Center: For requests submitted through order guides, employees see the parent Request \(REQ\) as the primary entity in the order confirmation page, My Requests list, and activity filtering. Approval workflows for these order guide requests and email notifications operate at the REQ level, providing a unified view of multi-item requests.
-   Simplified Request on Employee Slate: Initial support for the simplified request experience on Employee Slate, enabling request simplification for both new and upgrade customer paths.
-   The Configuration Console now honours ITSM granular roles on a per-step basis for the Employee Experience and ITSM Fulfiller Experience steps. The Console evaluates the invoking user's granular role for each step, gates visibility and actions accordingly, and surfaces consistent messaging on which role to request. To delegate Incident Management setup tasks, provide sn\_incident\_admin role.
-   To delegate Request Management setup tasks, provide sn\_request\_admin role.

</td></tr><tr><td>

AI Agents for Employee Experience

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

ServiceNow Otto for Security Incident Response Integration Toolkit

</td><td>

2026-08-07 00:00:00

</td><td>

Rebranded 'Now Assist' to 'ServiceNow Otto' across the application.

</td></tr><tr><td>

Interaction Management for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

AI Data Explorer

</td><td>

2026-08-07 00:00:00

</td><td>

-   UI improvements for data source view information.
-   Otto rebranding for AI Data Explorer experience.
-   AI Data Explorer skills made compatible with Default activation of Out-of-box skills in Now Assist Admin Console.

</td></tr><tr><td>

AIOps Experience

</td><td>

2026-08-07 00:00:00

</td><td>

-   AI value is now visible on the AIOps 360 dashboard. A new widget shows estimated time saved based on how many alerts were resolved and analyzed by AI, giving operations teams a real-time view of AI's impact on their workload.
-   Express lists now support color-coded visual cues to highlight values \(based on existing definitions in sys\_highlighted\_value\). Admins can configure conditional formatting rules on alert columns \(e.g., severity, priority\) so that critical items are immediately visible through colored indicators and icons - no more scanning through uniform rows.
-   Azure Monitor Issues now surface related alerts in context. A new 'Related Records' tab appears directly in the alert view for Azure Monitor Issues, letting operators drill into associated alerts without leaving their current workflow. Azure Monitor Issues are now bi-directionally synchronized with ServiceNow. The integration supports real-time ingestion of Azure Monitor Issues via webhook and polling, with two-way synchronization of status, severity, title, description, and AI-generated insights. OAuth 2.0 and multi-tenant Azure environments are supported.

 Dynatrace Gen3 event payloads are now supported in the event push connector, alongside legacy formats - no migration required.

 -   Express List now fully supports right-to-left languages, including Arabic and Hebrew, with correct mirroring of layout, icons, and spacing.
-   All 'Now Assist' references across Service Operations Workspace, Express List, Integration Launchpad, and the AIOps AI Specialist onboarding have been rebranded to ServiceNow Otto.
-   The Probable Cause tab in the Alerts Preview panel is now called 'Related Records' and includes Azure Monitor Issues.
-   The Dynatrace Gen3 payload processor now handles both workflow-wrapped and raw Davis Gen3 payloads consistently, with improved severity mapping and entity tag preservation.
-   Alert automation no longer hangs when the interface language is set to Portuguese.
-   The AIOps Supervisor Homepage remains responsive when managing a large number of teammates.
-   Express List no longer fails to load when a system property record has a missing type value.

</td></tr><tr><td>

ServiceNow Otto for Spoke Generation

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Servicenow Otto rename changes.

</td></tr><tr><td>

Incident Communications Management for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

ServiceNow Otto for Public Sector Digital Services \(PSDS\)

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto Rebranding.

</td></tr><tr><td>

Core Business Suite Foundation for Finance

</td><td>

2026-08-07 00:00:00

</td><td>

Shipped Now Assist search sources for Finance for Knowledge article generation from finance case table on Knowledge center.

 Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

SLO - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, references to Now Assist have been replaced with ServiceNow Otto.

</td></tr><tr><td>

ServiceNow Otto for WDF

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist for Workflow Data Fabrics \(WDF\) has been renamed to ServiceNow Otto for Workflow Data Fabrics \(WDF\).

</td></tr><tr><td>

App Engine Notifications

</td><td>

2026-08-07 00:00:00

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

Group-Action Framework

</td><td>

2026-08-07 00:00:00

</td><td>

--- AI Generated Release Notes ---.

 -   Admins can now grant report-view access to additional data tables for users with the data report viewer role, enabling broader visibility in dashboard visualizations.
-   Incremental clustering capabilities have been introduced for apps like Agent Advisor, Suggested steps allowing the system to process and group data as they come in.
-   GPT SMALL will now be the default model for GAF skills, enabling enhanced skill processing and evaluation.

 Incremental clustering handler logic has been updated to improve prediction accuracy and workflow processing for Agent Advisor features.

</td></tr><tr><td>

Common AI Framework

</td><td>

2026-08-07 00:00:00

</td><td>

Enhancements to support the ServiceNow Otto brand.

</td></tr><tr><td>

Service Operations Workspace Supervisor Dashboard

</td><td>

2026-08-07 00:00:00

</td><td>

AIOps Supervisor Homepage updated for Otto branding. All text and icon references to 'Now Assist' are replaced with 'Otto' for brand consistency. No functional changes are introduced.

 The AIOps Supervisor Homepage now remains responsive even with a large number of teammates.

</td></tr><tr><td>

HCLS - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Dependency version fixes and branding fixes.

</td></tr><tr><td>

ServiceNow Otto for Third-Party Risk Management

</td><td>

2026-08-07 00:00:00

</td><td>

Updated.

 -   Rebranded to ServiceNow Otto, replacing Now Assist references for a consistent AI experience.
-   Enhanced MRA authorization validation to ensure access checks are consistently enforced during record association.

</td></tr><tr><td>

Sourcing and Purchasing Automation

</td><td>

2026-08-07 00:00:00

</td><td>

-   Resolved a scoping issue that could allow cross-record access under specific configurations.
-   Applied security hardening to address CVE-2025-3648.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Enhancements to support the ServiceNow Otto brand.

</td></tr><tr><td>

Change Management for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

AES Application Object Templates

</td><td>

2026-08-07 00:00:00

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

Model Context Protocol Server

</td><td>

2026-08-07 00:00:00

</td><td>

New: OAuth Client Registration wizard: register an inbound OAuth client for your MCP server using a guided setup \(name and redirect URL\) instead of configuring it manually.- In-console tool testing: list and run any tool directly from the MCP Server Console to validate it before making it available to clients.- Tool visibility controls: choose which tools are visible in the console and to connected MCP clients.- Tool annotations: tools now indicate whether they are read-only, destructive, or display a friendly title, so AI clients like Claude can skip confirmation prompts for safe, read-only actions.- Improved separation between production and sub-production traffic, so testing and development activity no longer competes with production usage.

 Changed: Expanded request tracing, so administrators can follow a single tool call from start to finish.- Improved throughput and scaling, supporting significantly more concurrent users without performance degradation.- Enhanced monitoring for rate limits and platform guardrails to help administrators stay ahead of usage issues.

 Fixed: Performance and scaling fixes that address slowdowns under higher concurrent usage.

</td></tr><tr><td>

RPA Plugin Bundle

</td><td>

2026-08-07 00:00:00

</td><td>

-   Changed: Improved the ability to map credential records to automation processes, enhancing configuration flexibility for RPA administrators.
-   Enhanced the functionality for organizing and grouping robots to improve automation distribution and workload management.
-   Security enhancements to strengthen authorization controls and data protection across the application.

</td></tr><tr><td>

Walk-up Experience for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

Employee Slate Core

</td><td>

2026-08-07 00:00:00

</td><td>

-   Introduced topic-based content discovery with category-based navigation in Employee Slate, updating the browse experience.
-   Enhanced org charts with responsive layouts, profile cards redesign, and team visualization.
-   Provided field visibility controls on knowledge articles.
-   Introduced configuration scope controls so task configs and Lit-based action widgets can independently target Employee Center or Employee Slate, enabling teams to ship new configs with existing mappings.
-   Introduced task record preprocessing for skills to fetch context, enrich records, and format output before skill invocation.
-   Rebranded Now Assist, Moveworks, and AI Experience to Otto for consistency.

</td></tr><tr><td>

Proactive Engagement

</td><td>

2026-08-07 00:00:00

</td><td>

See DEX Application and Device Health product for release notes. This app is a dependency of DEX Application and Device Health.

</td></tr><tr><td>

AES Application Object Wizard Components

</td><td>

2026-08-07 00:00:00

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

Finance Common Architecture

</td><td>

2026-08-07 00:00:00

</td><td>

Introduced the Jurisdiction table to store jurisdiction names, codes, types, and associated tax authority.

 -   Enhanced the Tax Type table to associate tax types with jurisdictions.
-   Updated the Tax Type list view to display jurisdiction type and tax authority.
-   When adding a tax line, jurisdiction type and tax authority now populate automatically based on the selected tax type. These fields are hidden by default and can be enabled as needed.

</td></tr><tr><td>

Unified Developer Core

</td><td>

2026-08-07 00:00:00

</td><td>

Maintenance release.

</td></tr><tr><td>

Legal Service Delivery - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: ServiceNow Otto is the new AI experience brand. Now Assist for Legal Service Delivery is ServiceNow Otto for Legal Service Delivery.

</td></tr><tr><td>

Lead to Cash Core

</td><td>

2026-08-07 00:00:00

</td><td>

Release Notes \*\*New\*\* None \*\*Changed\*\* Enhanced support to provide custom mapping in DeltaService API. \*\*Fixed\*\* None \*\*Removed\*\* None.

</td></tr><tr><td>

ServiceNow Otto for Purchase Order Management \(POM\)

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, references to Now Assist have been replaced with ServiceNow Otto.

</td></tr><tr><td>

ServiceNow Otto for Service Quality

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: ServiceNow Otto is the new AI Experience brand. This change is reflected in the name of ServiceNow products, including Now Assist for Service Quality. Your product entitlements remain unchanged.
-   Changed: The engine that evaluates a case when it's closed now runs as a single streamlined step instead of a longer chain of internal steps to minimize failures points.- The loading time of the Automated Quality Assurance dashboard is optimized to handle large number for records.

</td></tr><tr><td>

Telecommunications, Media and Technology - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

SKU plugin.

</td></tr><tr><td>

Third-party Risk Management Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

-   Rebranded to ServiceNow Otto, replacing Now Assist references for a consistent AI experience.
-   Enhanced MRA authorization validation to ensure access checks are consistently enforced during record association.

</td></tr><tr><td>

Tag Based Alert Clustering Engine

</td><td>

2026-08-07 00:00:00

</td><td>

--- AI Generated Release Notes ---.

 Query range issues on session alerts have been resolved. Session alert queries now return accurate results without errors.

</td></tr><tr><td>

@servicenow/sn-ai-engagement-experience

</td><td>

2026-08-07 00:00:00

</td><td>

Updated branding of Now Assist to ServiceNow Otto to align with the new branding guidelines.

 -   Resolved Core IT installation override of agenticWorkflowsRoute property.
-   Updated the access control to ensure ITIL users do not have unintended access.
-   Fixed: ServiceNow Otto panel in portal to render when web embeddables is enabled.

</td></tr><tr><td>

Sales and Order Management for Telecommunications, Media and Technology - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

SKU plugin.

</td></tr><tr><td>

ITSM Admin Experience

</td><td>

2026-08-07 00:00:00

</td><td>

-   The Configuration Console honours ITSM granular roles on a per-step basis for the Employee Experience and ITSM Fulfiller Experience steps. The Console evaluates the invoking user's granular role for each step, gates visibility and actions accordingly, and surfaces consistent messaging on which role to request. To delegate Incident Management setup tasks, provide sn\_incident\_admin role.
-   To delegate Request Management setup tasks, provide sn\_request\_admin role.

</td></tr><tr><td>

CTO Voice AI Agents

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Dependency version fixes and branding fixes.

</td></tr><tr><td>

ITSM Change Admin Experience

</td><td>

2026-08-07 00:00:00

</td><td>

Forms module in Configuration Console.

 Review and configure change forms that IT fulfiller staff use to create and manage changes. Use the Form Builder to customize form layouts, fields, and sections to match your organization's change processes.

 Lists module in Configuration Console Configure which columns appear in the change lists for your IT fulfiller staff.

 Enhanced AI agents Use a document upload flow as an alternative to the traditional form-based approach to configure team roles and the Change Advisory Board \(CAB\) using AI agents, with support for PDF, DOCX, XLSX, and CSV file formats.

</td></tr><tr><td>

SPO - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, Now Assist references have been replaced with ServiceNow Otto.

</td></tr><tr><td>

IT Service Management

</td><td>

2026-08-07 00:00:00

</td><td>

-   Simplified request experience for order guides on Employee Center: For requests submitted through order guides, employees see the parent Request \(REQ\) as the primary entity in the order confirmation page, My Requests list, and activity filtering. Approval workflows for these order guide requests and email notifications operate at the REQ level, providing a unified view of multi-item requests.
-   Simplified Request on Employee Slate: Initial support for the simplified request experience on Employee Slate, enabling request simplification for both new and upgrade customer paths.

</td></tr><tr><td>

ServiceNow Otto for Workplace Service Delivery \(WSD\)

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

DEX Self Service

</td><td>

2026-08-07 00:00:00

</td><td>

See DEX Application and Device Health product for release notes. This app is a dependency of DEX Application and Device Health.

</td></tr><tr><td>

ServiceNow Otto for Threat Intelligence Security Center

</td><td>

2026-08-07 00:00:00

</td><td>

Added support for Google Gemini 3.5 Flash and OpenAI GPT 5.4 mini models for Case summarization.

 Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand.

</td></tr><tr><td>

Hardware Asset Management - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

This app extends ServiceNow Otto capabilities for Hardware Asset Management through a subscription model. This release updates app dependencies to the latest versions while maintaining compatibility with the Hardware Asset Management - Advanced app.

</td></tr><tr><td>

Incident Management for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

Recommended Actions for Security Operations

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been rebranded as ServiceNow Otto.

</td></tr><tr><td>

observ-ai-agents-app

</td><td>

2026-08-07 00:00:00

</td><td>

-   Added the following agents to the Analyze alert impact agentic workflow: Gemini Cloud Assist A2A Investigation Agent.
-   Azure Monitor MCP Agent.

 ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI Agents for Observability. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Enhancements to the Security Exposure 360 feature:

 -   Clickable Links to Records: Counts and findings in the Security Exposure 360 output are now directly clickable, linking you to the underlying vulnerable item \(VITs\)/records in your ServiceNow AI Platform instance.
-   Suggested follow-up questions: Suggested follow-up questions are provided that help you drill down.

 Enhancements to support the ServiceNow Otto brand.

</td></tr><tr><td>

ITSM Advanced Admin Experience

</td><td>

2026-08-07 00:00:00

</td><td>

No changes.

</td></tr><tr><td>

DEX Application and Device Health

</td><td>

2026-08-07 00:00:00

</td><td>

-   Offline Monitoring: Continue collecting endpoint telemetry during network outages and automatically sync queued metrics when connectivity is restored.
-   Incident Work Notes Integration: Automatically add DEX work note to incident with deep links to DEX device health, DEX application health, when any of the following fields are updated \(Configuration Item, Service, Service Offering\).
-   CMDB population with enhanced discovery: Running processes are now reconciled directly into the cmdb\_running\_process table without creating unnecessary Application CIs. Running process data no longer creates Application Shell CIs in cmdb\_ci\_appl, and the system uses targeted reconciliation instead of the full ADM pipeline to keep your application inventory focused on actual software installations. This results in a cleaner CMDB with less clutter, better performance for instances with high process activity, and clearer separation between process telemetry and installed software inventory.
-   Updated remedial action: Perform disk clean up remedial action has been renamed to Disk cleanup for low disk space on device health page.
-   DEX policies for Windows and mac OS: These DEX policies are now split into multiple policies to optimise the performance of the device or the application that is monitored.

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto Rebranding.

</td></tr><tr><td>

CRM Touchpoint

</td><td>

2026-08-07 00:00:00

</td><td>

Admins can now assign granular read and write roles for CRM Touchpoints. The new roles provide fine-grained access control to CRM Touchpoint records, enabling separate assignment of read and write permissions through the Responsibility Framework. Access Control Lists \(ACLs\) have been updated to enforce these granular permissions.

</td></tr><tr><td>

Clone Admin Console

</td><td>

2026-08-07 00:00:00

</td><td>

-   Enhanced authentication: Clone Admin Console now uses OAuth-based authentication. When you place your next clone, a guided experience automatically prompts you to set up the new mechanism between your instances.
-   Cleanup Script status: You can now view the status of your cleanup scripts. With Multi-Instance View enabled, the status appears on the clone status page of the source instance.

 Clone Request page: The page now warns you if a clone profile overrides the target instance selection.

</td></tr><tr><td>

Conversation Evaluator

</td><td>

2026-08-07 00:00:00

</td><td>

As part of our evolving model strategy, the default model for all skills is being migrated from NowLLM to a 3rd-party \(3P\) model. This change aligns with our ongoing efforts to enhance model capabilities, performance, and scalability across the platform.

 What's changing?.

 -   The default model for all skills will transition from NowLLM to a 3P model.
-   Existing skills that rely on the default model will automatically use the new default unless explicitly configured otherwise.

</td></tr><tr><td>

ServiceNow Otto for Integrated Risk Management

</td><td>

2026-08-07 00:00:00

</td><td>

\*\*New\*\*.

 \*\*Changed\*\*All references to 'Now Assist for IRM' have been renamed to 'ServiceNow Otto for Integrated Risk Management' in the Australia Patch4 and Zurich latest patch versions.

 \*\*Fixed\*\*.

 -   The display properties for ServiceNow Otto for Integrated Risk Management plug-in updated, so that System Admins can install this plug-in.
-   Install-as-dependency settings also have been updated to ensure correct application visibility and dependency management.

 \*\*Removed\*\*.

</td></tr><tr><td>

ServiceNow Otto for Document Voice

</td><td>

2026-08-07 00:00:00

</td><td>

Enhanced the voice Q and amp;A experience.

 Fixed: a few UI issues that occurred when closing voice Q and amp;A sessions.

</td></tr><tr><td>

Portfolio Planning integrations for Shared Infrastructure

</td><td>

2026-08-07 00:00:00

</td><td>

Fixed: Resolved an issue where execution URL and demand menu links from the portfolio plan grid, Kanban, and roadmap were broken due to a URL change introduced with the new L2 navigation.

</td></tr><tr><td>

Agent Client Collector Framework

</td><td>

2026-08-07 00:00:00

</td><td>

Fixes:

 1. Clean up of .pem and .bin files in the upgrade directory during upgrades of the ACC RPM agent on Linux hosts.

 2. Upgraded OpenSSL version to 3.4.6 and net-imap to 0.5.15 that will resolve the security vulnerabilities.

 4. Fixed Windows instllation for acc version greater than 6.5.1 due to servicenow user creation error.

</td></tr><tr><td>

Data Discovery

</td><td>

2026-08-07 00:00:00

</td><td>

Service now Otto Directive Changes.

</td></tr><tr><td>

AI Agents for Universal Request

</td><td>

2026-08-07 00:00:00

</td><td>

-   Changed: Renamed the app to 'AI Agents for Universal Request' as per Otto rebranding.
-   Fixed: When the UR Agentic workflow kicks in and creates a HR case, Case is getting created but the HR Service field is empty and not getting populated.

</td></tr><tr><td>

Roadmap UI Builder Component

</td><td>

2026-08-07 00:00:00

</td><td>

Access the Roadmap Component shortcuts modal from the side panel for a more consistent experience when viewing and managing roadmap shortcuts.

 -   Resolved an accessibility issue where the close button on roadmap item popovers incorrectly included the aria-pressed attribute and was presented as a toggle button.
-   Resolved an accessibility issue where the No Roadmap Milestones tooltip help button was not included in the tab order and did not respond to the Enter key.

</td></tr><tr><td>

Microsoft Azure OpenAI Generative AI Spoke

</td><td>

2026-08-07 00:00:00

</td><td>

Fixed: an issue in Azure OpenAI Spoke where multi-turn GPT conversations failed due to message input not being passed as JSON type.

 Fixed: an issue in Azure OpenAI Spoke where Tool Calling was not supported in Streaming \(SSE\) mode for GPT-5.4 in GAIC.

</td></tr><tr><td>

DEX Desktop Assistant

</td><td>

2026-08-07 00:00:00

</td><td>

See DEX Application and Device Health product for release notes. This app is a dependency of DEX Application and Device Health.

</td></tr><tr><td>

Health and Safety Risk Management

</td><td>

2026-08-07 00:00:00

</td><td>

-   Date of birth and Date of hire fields now populate correctly in the exported OSHA 301 PDF forms.
-   Work notes on Health and Safety incidents are now restricted from being visible to end users.
-   Risk Management ACLs no longer override involved party access to Health and Safety incidents.
-   The body part picker now correctly selects the back of the hand instead of the palm when clicked.
-   ACL checks are now enforced on Health and Safety incident records for all applicable extension points.
-   Hardcoded strings and date and time formats in the Health and Safety Workspace now adapt to non-English locales.
-   'Link Documents' and 'Select Documents' action labels appear translated on initial page load.
-   Users are prevented from creating and linking Health and Safety actions to restricted incidents without the required access permissions.
-   An intermittent issue that prevented incident playbook triggers from firing has been resolved.
-   A scrolling issue in the Injury Details section that prevented the delete option for the last added injury from being reachable has been fixed.
-   A cross-scope access violation in the Attach Health and Safety Case primary record to universal request business rule that prevented the Transfer and Create Associated Ticket buttons from appearing has been resolved.
-   The Approval Task Creator tool now reads manager details correctly when the application is installed.
-   The Health and Safety Ask attachment field now renders as mandatory when configured as required on a Smart Assessment template question.
-   A time zone issue that caused the Inspection Schedule flow to run incorrectly for daily frequency schedules has been resolved.
-   Scheduling an audit no longer returns a 'Component not configured' error.

</td></tr><tr><td>

Health and Safety Case Management

</td><td>

2026-08-07 00:00:00

</td><td>

Safety Knowledge Base access controls for managers and requestors. Health and amp; Safety managers and agents can now contribute to Safety Knowledge Base articles, while case requestors have read-only access to articles within the Knowledge Base.

</td></tr><tr><td>

Health and Safety Core

</td><td>

2026-08-07 00:00:00

</td><td>

The Assets involved list on the Incident Overview tab now displays correctly when the system property for invalid queries is set to return no rows. The previous hardcoded filter requiring an 'active' field has been corrected to support tables without an 'active' field.

</td></tr><tr><td>

Security Incident Response

</td><td>

2026-08-07 00:00:00

</td><td>

-   Fixed: an issue where analysts could not interact with Overview tab widgets or closure modal links in the Security Incident Response Workspace.
-   Fixed: an issue where the Configure button on the Post Incident Review Assessments Setup page did not respond due to a client-script error.
-   Improved accessibility by ensuring screen reader users are notified when a quick link is added on the Security Incident Response Workspace home page \(WCAG 3.2.2 compliance\).
-   Fixed: an issue in the Security Operations Integration - Publish to Watchlist V1 integration flow where a single Capability Implementation input incorrectly triggered execution of all active implementations.

</td></tr><tr><td>

Metric data table

</td><td>

2026-08-07 00:00:00

</td><td>

All subgroup sections are now displayed in the Metric Data Grid, allowing users to view and select metric data tasks across multiple subgroups.

</td></tr><tr><td>

Core Business Suite for Finance

</td><td>

2026-08-07 00:00:00

</td><td>

Shipped Now Assist search sources for Finance for Knowledge article generation from finance case table on Knowledge center.

 Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, references to Now Assist have been replaced with ServiceNow Otto.

</td></tr><tr><td>

ServiceNow Otto for CSM Complaint Case

</td><td>

2026-08-07 00:00:00

</td><td>

App renamed to ServiceNow Otto for CSM Complaint Case.

</td></tr><tr><td>

ServiceNow Otto for Platform Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

The application captures dependencies, updated the plugin dependencies for this release.

</td></tr><tr><td>

ITOM Configuration Console

</td><td>

2026-08-07 00:00:00

</td><td>

-   Best practices for Discovery setup.
-   Assign a NOC Manager.
-   Remediation Actions - show response automations that do not contain 'incident'.
-   Change the 'Assign Event Management Admin' item from direct assignment to group assignment \(similar to the operator item\).
-   Update the operator training step to link to ServiceNow University.

</td></tr><tr><td>

Workplace Connectors

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

Flow Generation

</td><td>

2026-08-07 00:00:00

</td><td>

Flow Generation skills and agents now default to optimal small third-party models. All skills and agents previously using Now LLM have been updated to use Google Gemini 3.5 Flash, OpenAI GPT 5.1, or OpenAI GPT 5.4 mini as default model providers. Large model selections require documented exception approval.

 ServiceNow Otto branding is now applied throughout Flow Generation interfaces. All UI strings, labels, and icons referencing 'Now Assist' have been replaced with ServiceNow Otto naming and marks according to Otto Naming Guidelines. Interactive and background surfaces display the correct Otto mark variant. UX review has been completed prior to merge.

 Prompt Analyzer findings for Flow Generation prompts have been reviewed and addressed. All prompt standards and best practices have been validated for skills, and any issues have been triaged or resolved.

</td></tr><tr><td>

Technology Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

SKU plugin.

</td></tr><tr><td>

Core Business Suite Advanced for Source to Pay

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Core Business Suite Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

ServiceNow Otto for Wrap Up

</td><td>

2026-08-07 00:00:00

</td><td>

Name updated to ServiceNow Otto for Wrap Up.

</td></tr><tr><td>

ServiceNow Otto for Security Incident Response \(SIR\)

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand.

 Correlation Insight skill now supports optional security incident ID for MCP.

</td></tr><tr><td>

Enhanced Features for IRM Professional

</td><td>

2026-08-07 00:00:00

</td><td>

 

</td></tr><tr><td>

Core Business Suite Prime for Workplace Services

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

AI Agents for CSM - Complaint Case

</td><td>

2026-08-07 00:00:00

</td><td>

App renamed to Complaint Case AI Agent Collection.

</td></tr><tr><td>

Resource Management Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

-   Filtering for unassigned tasks in Resource Management Workspace no longer creates blank resource cards; the filter now shows only relevant cards.
-   The Resource Management Workspace tooltip now correctly shows 'Pending' status instead of a null value after updates.
-   Resource Management Workspace no longer generates additional assignments with zero person days; assignments are created only when resources are available and effort is sufficient.
-   The Unassigned Assignment Requests dashboard in Resource Management Workspace now filters correctly by unassigned task start date.
-   The new resource assignment modal in Resource Management Workspace now loads correctly when domain determination is enabled.
-   Notes no longer duplicate when you assign an unassigned assignment from Resource Management Workspace.
-   Expand All now calculates correctly when grouping by primary resource group.
-   Resource realign calls and realign buttons now disable correctly when the auto-realign property is configured.
-   Color coding now displays correctly when grouping by owner using resource manager impersonation.

</td></tr><tr><td>

Collaborative Work Management

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: SPM's Project Workspace now has an integration with Collaborative Work Management Team Members can create new CWM tasks/stories under an assigned project task.
-   Users can move or break a CWM task's connection to a different project task.
-   Project Managers will see CWM tasks/stories connected to their project tasks directly inline in the Planning page of the Project in Project Workspace.
-   Team Members in CWM see their connected project and project tasks as columns in CWM list view, and in 'My Work'.

 Relationships for any task types can added now using Task number/id instead of just Task description.

</td></tr><tr><td>

Legal Request Management

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: ServiceNow Otto is the new AI experience brand. Now Assist for Legal Service Delivery is ServiceNow Otto for Legal Service Delivery.

 Security fixes.

</td></tr><tr><td>

Sales and Order Management for Telecommunications, Media and Technology - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

SKU Application Container.

</td></tr><tr><td>

Data Foundation Model

</td><td>

2026-08-07 00:00:00

</td><td>

Added the 'Agentic Client' model category to the cmdb\_model\_category table. The category groups AI client software such as Arc ServiceNow clients, Claude Coworker clients, and so on.

</td></tr><tr><td>

Workplace Core

</td><td>

2026-08-07 00:00:00

</td><td>

Security fixes.

</td></tr><tr><td>

Event Management Core

</td><td>

2026-08-07 00:00:00

</td><td>

--- AI Generated Release Notes ---.

 All references to 'Now Assist' have been updated to 'ServiceNow Otto' across the em-scoped-app and em-arm modules. UI labels, flow descriptions, hint texts, and rule labels now consistently use the new product name to align with branding changes. Commit: Renaming of now assist to ServiceNow Otto - em-scoped-app; Updates according to the revised guideline.

</td></tr><tr><td>

Accounts Payable Invoice Processing

</td><td>

2026-08-07 00:00:00

</td><td>

-   A new Jurisdiction table included to capture tax jurisdiction, type, and authority information. Tax types are enhanced to capture and auto-populate tax jurisdiction details when users add tax lines to invoices.
-   This release includes fixes for reported defects to improve product stability. Fixed an issue that could cause auto-reject to fail during invoice exception processing.
-   Fixed: an issue on invoice processing case where user is unable to update when requested by is empty.

</td></tr><tr><td>

Core Business Suite Foundation for Source to Pay

</td><td>

2026-08-07 00:00:00

</td><td>

-   Shipped out-of-the-box Procurement and Supplier knowledge bases.
-   Owners and managers can be defined by the admin for the knowledge base in the Core Business Suite configuration console to ensure proper governance and content tracking.
-   Shipped Now Assist search sources for Source to Pay for Knowledge article generation from invoice, supplier and procurement case table on the Knowledge center.
-   Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

HRSD - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Otto skills and a refreshed user interface for Otto.

</td></tr><tr><td>

Sales and Order Management for Technology Provider - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Underline application released.

</td></tr><tr><td>

ServiceNow Otto AI web agent

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: Preserve context across long-running sessions by summarizing older step history instead of discarding it. When history exceeds the configured window, older steps are automatically summarized instead of being discarded. They preserve context about earlier actions, failed approaches, and application state.
-   Three new system properties let you configure how adaptive desktop actions step history is compacted:
    -   sn\_naa.web\_agent.compaction\_enabled.
    -   Sn\_naa.web\_agent.compaction\_history\_limit.
    -   Sn\_naa.web\_agent.summarization\_batch\_size.
-   Adaptive desktop actions are now batched for better performance. Multiple actions execute per LLM call instead of one call per action that reduces the round-trip latency that previously limited production readiness.
-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI Desktop Actions. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

Sales and Order Management for Technology Provider - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

SKU plugin.

</td></tr><tr><td>

Software Asset Management AI Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Starting with v2.4.3, Now Assist for Software Asset Management is now ServiceNow Otto for Software Asset Management.

</td></tr><tr><td>

SPM Planning Attributes Core

</td><td>

2026-08-07 00:00:00

</td><td>

System administrators and developers can now access Financial Management Attributes without restriction. Access is now public, enabling integration with additional applications.

 -   Assignment realignment for demand now functions correctly.
-   Assignment date updates and realignment now work correctly when actuals are present. The system checks assignment alignment before proceeding.
-   UI actions for epic and planning items have been updated to support this alignment check.
-   Rate override and resource rate columns on the resource board now display and function correctly.
-   Task reassignments now correctly update associated dates.

</td></tr><tr><td>

Knowledge Center

</td><td>

2026-08-07 00:00:00

</td><td>

Auto-update, auto-merge and otto branding updates.

</td></tr><tr><td>

AI Desktop Actions

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated the AI experience branding in AI Desktop Actions to align with ServiceNow Otto naming and visual guidelines.

</td></tr><tr><td>

AI Agents for Meetings

</td><td>

2026-08-07 00:00:00

</td><td>

This release introduces AI Agents for Meetings \(sn\_meeting\_ai\_ag\), a new standalone plugin that delivers AI-driven meeting creation. The AI Agent monitors risk records and proposes complete meeting drafts automatically, with additional entry points available via a 'Create Meeting' action on Engagement and Touchpoint forms and through the Now Assist conversational panel.

</td></tr><tr><td>

Technology Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

SKU plaugin.

</td></tr><tr><td>

Technology Prime

</td><td>

2026-08-07 00:00:00

</td><td>

SKU plugin.

</td></tr><tr><td>

Core Business Suite Foundation for Health and Safety

</td><td>

2026-08-07 00:00:00

</td><td>

-   Shipped out-of-the-box Safety knowledge base.
-   Owners and managers can be defined by the admin for the knowledge base in the Core Business Suite configuration console to ensure proper governance and content tracking.
-   Shipped user criteria for Health and amp; Safety knowlegde base.
-   Shipped Now Assist search sources for Health and amp; Safety for Knowledge article generation from health and safety case table on the Knowledge center.
-   Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

ServiceNow Otto for Configuration Management Database \(CMDB\)

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: Added summarization to the CMDB success advisor for HAM dashboard.
-   Added summarization to the CMDB success advisor for Data Foundations dashboard.

 Fixed: Security fixes.

</td></tr><tr><td>

AI Control Tower Core

</td><td>

2026-08-07 00:00:00

</td><td>

Discovery &amp;amp; Inventory.

 Multi-tenant credential support for hyperscaler connectors.

 -   Enhanced asset enrichment with cloud-native metadata and AI system relationship mapping.
-   Relationship mapping with Business applications \(requires EA entitlement\).
-   Simplified asset states and status which replaces lifecycle phase and lifecycle status in asset record view.

 Legacy single-tenant discovery connectors.

</td></tr><tr><td>

AI Agents for Customer Success Management

</td><td>

2026-08-07 00:00:00

</td><td>

Meeting related fixes.

</td></tr><tr><td>

Core Business Suite

</td><td>

2026-08-07 00:00:00

</td><td>

-   Shipped out-of-the-box knowledge bases defined at two levels: individual business unit knowledge bases \(Human Resources, Legal, Source to Pay, Workplace Services, and Health and amp; Safety\) and a CBS aggregate knowledge base.
-   Owners and managers can be defined by the admin in the Knowledge module for each knowledge base to ensure proper governance and content tracking.
-   Shipped new AI skills module under the Platform module on Configuration console enables admins to activate knowledge-specific skills from simplified setup.
-   Improve article optimization in terms of content quality, identification, and merging of duplicate articles to eliminate redundant content.
-   Shipped Now Assist search sources for all the business unit for Knowledge article generation from case tables on the Knowledge center.
-   Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

 Admins can now manage access to the Core Business Suite analytics dashboard through the new Groups module under Core Business Suite module. Define which users have view and edit access by adding them to groups, providing fine-grained control over who can access reporting and metrics across your Core Business Suite implementation.

</td></tr><tr><td>

ServiceNow Otto for Telecommunications, Media and Technology \(TMT\)

</td><td>

2026-08-07 00:00:00

</td><td>

Meeting V2 Agent is getting shipped.

</td></tr><tr><td>

ServiceNow Otto for Creator

</td><td>

2026-08-07 00:00:00

</td><td>

-   Changed: ServiceNow Otto branding.
-   Please click on the individual dependent apps included with this package for detailed release note information.

</td></tr><tr><td>

IRM Risk GenAI

</td><td>

2026-08-07 00:00:00

</td><td>

-   Updated the application to reflect the new ServiceNow OTTO branding, replacing Now Assist references and providing a more consistent AI experience across the platform.
-   Note: These branding updates are fully supported on AP5. Customers using AP4 will continue to see legacy branding elements and could notice missing icons on a few buttons until they upgrade to AP5.

</td></tr><tr><td>

Content Publishing

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Security Support Common

</td><td>

2026-08-07 00:00:00

</td><td>

-   Security tags are now correctly applied to Security Incident Response records when hierarchical conditions are used in filter groups.
-   URLs are now correctly recognized as observable data types.
-   Resolved an issue where duplicate assignment records were being loaded.

</td></tr><tr><td>

ServiceNow Otto for Code

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Name change from Now assist to ServiceNow Otto.

 General fixes and enhancements.

</td></tr><tr><td>

Core Business Suite Prime for Health and Safety

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Telecommunications, Media and Technology - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

SKU related changes.

</td></tr><tr><td>

Query Orchestrator

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated internal application components to support ongoing platform enhancements.

</td></tr><tr><td>

GRC: Policy and Compliance Management

</td><td>

2026-08-07 00:00:00

</td><td>

Changes.

 Multiple record association \(MRA\) security enhancements: Authorization validation has been strengthened within MRA workflows to consistently enforce access checks during record association operations.

</td></tr><tr><td>

Telecommunications, Media and Technology - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

SKU plugin.

</td></tr><tr><td>

Automation Center

</td><td>

2026-08-07 00:00:00

</td><td>

Sn\_ac.auto\_onboarding\_catalog\_items - Use this system property to control how catalog items are onboarded as automations. Users with the sn\_ac.automation\_admin role can edit the system property.

 -   True \(default\): New catalog items are onboarded automatically and appear on the automation dashboard immediately, without time and cost savings for each catalog item.
-   False: New catalog items are onboarded manually. Generating this data takes longer, but the dashboard shows an expanded summary with time and cost savings for each catalog item.

</td></tr><tr><td>

Advanced Approval Management AI

</td><td>

2026-08-07 00:00:00

</td><td>

-   Enable sales agents and approvers to add ad-hoc approvers from Claude Desktop.
-   Enable sales agents to recall approval requests from Claude Desktop.

</td></tr><tr><td>

Pluralsight Spoke

</td><td>

2026-08-07 00:00:00

</td><td>

Resolved an issue where Pluralsight Spoke actions and datastreams stopped working as expected following Pluralsight's 2025 API deprecations. The spoke has been updated to use Pluralsight's current API endpoints, restoring end-to-end functionality for course and content synchronization, user activity ingestion, and the associated spoke actions used in HR learning workflows.

</td></tr><tr><td>

ServiceNow Otto for Health and Safety

</td><td>

2026-08-07 00:00:00

</td><td>

Unified AI branding across Health and Safety interfaces. All customer-facing references to 'Now Assist,' 'Moveworks,' and 'AI Experience' have been replaced with 'ServiceNow Otto' in Health and Safety. Design review has confirmed consistency across UI elements, tooltips, images, and documentation.

 GenAI capabilities now default to third-party model providers. Four Health and Safety GenAI features have updated their default model provider from Now LLM to the best-performing third-party provider \(Azure OpenAI, Google Gemini, or AWS Claude\) per capability. No Now LLM defaults remain in GenAI workflows.

</td></tr><tr><td>

GRC: Common Workspace Elements

</td><td>

2026-08-07 00:00:00

</td><td>

 

</td></tr><tr><td>

Accounts Payable Operations integration with Document Intelligence

</td><td>

2026-08-07 00:00:00

</td><td>

This release includes fixes for reported defects to improve product stability.

</td></tr><tr><td>

Asset Management Common

</td><td>

2026-08-07 00:00:00

</td><td>

Related-list visibility is restored in Hardware Asset Management, Agentic Process sidebar availability is improved, and security hardening strengthens access-control enforcement across asset management workflows.

 -   Stockroom-related lists are now visible in Hardware Asset Workspace.
-   The Agentic Process sidebar availability has been improved.
-   Security enhancements strengthen access-control enforcement within asset management workflows.

</td></tr><tr><td>

Procurement Case Management

</td><td>

2026-08-07 00:00:00

</td><td>

-   Restricted purchase modification request access to a user's own records.
-   Applied security hardening to address CVE-2025-3648.

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

2026-08-07 00:00:00

</td><td>

- Added description field to the MCP server for a better discovery.

 - Pre-work for supporting MCP servers to assistants.

</td></tr><tr><td>

GRC: Approver Configurator

</td><td>

2026-08-07 00:00:00

</td><td>

 

</td></tr><tr><td>

Core Business Suite Prime for Source to Pay

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

ServiceNow Otto for OT Service Management

</td><td>

2026-08-07 00:00:00

</td><td>

New: Updated to support the ServiceNow Otto brand.

</td></tr><tr><td>

ServiceNow Otto for Operational Sustainability

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto Branding Updates Updated the application to reflect the new ServiceNow Otto branding, replacing Now Assist references and providing a more consistent AI experience across the platform.

</td></tr><tr><td>

Customer Service Management AI agent collection

</td><td>

2026-08-07 00:00:00

</td><td>

Customer 360 query routing to improve performance for lookups and KB-related queries.

</td></tr><tr><td>

Document Intelligence

</td><td>

2026-08-07 00:00:00

</td><td>

Minor UI content updates.

</td></tr><tr><td>

Mentoring

</td><td>

2026-08-07 00:00:00

</td><td>

Addressed UI Defects \(Hide the Now Assist FAB when Mentoring modals/flyouts open to prevent it from overlapping the UI\).

</td></tr><tr><td>

ServiceNow Otto Agents for requestor

</td><td>

2026-08-07 00:00:00

</td><td>

Approval checklist generation skill now supports passing the request body in place of the Approval ID.

 Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

</td></tr><tr><td>

AI Control Tower for ServiceNow Otto

</td><td>

2026-08-07 00:00:00

</td><td>

Auto-installed app for all ServiceNow AI products.

</td></tr><tr><td>

HCLS - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Minor typo correction.

</td></tr><tr><td>

Core Business Suite Analytics

</td><td>

2026-08-07 00:00:00

</td><td>

-   Introduced Goups under the Core Business Suite module in the Configuration Console.
-   Admins can now manage access to the Core Business Suite analytics dashboard through the new Groups module under Core Business Suite module.
-   Define which users have view and edit access by adding them to the groups, providing granular control over who can access reporting and metrics across your Core Business Suite implementation.

</td></tr><tr><td>

Core Business Suite Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

ServiceNow Otto for Core Business Suite

</td><td>

2026-08-07 00:00:00

</td><td>

-   Added new AI skills module under the Platform module on Configuration console. It enables admins to activate knowledge-specific skills from simplified setup.
-   Improve article optimization in terms of content quality, identification, and merging duplicate articles to eliminate redundant content.
-   Shipped Now Assist search sources for all the business units to generate knowledge article from the BU case tables on the Knowledge center.
-   Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

Amazon Bedrock Spoke

</td><td>

2026-08-07 00:00:00

</td><td>

Fixed: an issue in Amazon Bedrock Spoke OEM actions where additional headers were not being sent correctly.

 Fixed: an issue in Amazon Bedrock Spoke where the Generative AI Controller streaming done-chunk double-encoded non-ASCII model output \(em dash, curly quotes, accents\) as ISO-8859-1, causing garbled thinking and tool\_use inputs due to VAStreamConsumer not enforcing UTF-8.

</td></tr><tr><td>

Insurance Claims Core

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated internal application components to support ongoing platform enhancements.

</td></tr><tr><td>

Core Business Suite Advanced for Finance

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Record Page for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

Flow Designer GenAI

</td><td>

2026-08-07 00:00:00

</td><td>

-   All references to Now Assist, Moveworks, and AI Experience have been renamed to ServiceNow Otto. Applications, features, plugins, packages, in-product strings, images, and documentation now consistently use ServiceNow Otto branding.
-   Admins can now configure Flow Designer GenAI skills and agents to use optimal small third-party models as the default. Google Gemini 3.5 Flash, OpenAI GPT 5.1, and OpenAI GPT 5.4 mini are validated and available for use.
-   Context Memory input is now available in the Use an AI Agent action. Users can provide context memory to enhance agent interactions.
-   TinyMCE editor library has been upgraded to version 8 across Flow Designer GenAI products. Editor functionality, including hashtag and prompt editing, has been validated with no regressions.
-   Default model provider for Flow Designer GenAI skills and agents is now a third-party model. Now LLM is no longer the default; optimal small models are set as default, with exception handling for large models.
-   Prompt Analyzer findings for Flow Generation prompts have been reviewed and addressed. All active prompts now comply with prompt standards and best practices.
-   Call Now Assist Skill step now supports a data pill value. Data pill values can be used directly in skill calls.
-   Invalid roles in ACL definitions have been audited and remediated across Flow Designer GenAI products. Access control behavior is validated and confirmed compliant.
-   Implementation Agent integration for AI Approvals has been updated and validated. End-to-end sanity testing confirms no regressions in MCP and Decision Tables.
-   GetRefRecord scoping bypass fix has been validated. No direct references found and sanity testing confirms no scoping bypass issues.
-   Project Greenlight test automation and stabilization improvements delivered. Manual test backlog analyzed, prioritized automation plan executed, pre-merge automation expectations defined, and test stability improved for MCP, Decision Tables, and AI Approvals.
-   Java 21 compile upgrade validated across Flow Designer GenAI products. MCP, Decision Tables, and AI Approvals tested with no regressions.
-   Non-Glide Cobalt Raven ACLs merged and validated in product code. Sanity testing confirms no regressions in ACL behavior.
-   User-supplied JavaScript execution is now disabled in the Guest Sandbox environment. Flow Generation, Flow Summarization, MCP, Decision Tables, and AI Approvals are unaffected and validated for correct operation.
-   CSRF remediation implemented and validated across platform APIs. MCP, Decision Tables, and AI Approvals API endpoints confirmed compliant with CSRF protection.

</td></tr><tr><td>

ServiceNow Otto context menu

</td><td>

2026-08-07 00:00:00

</td><td>

-   \[Otto Directive\]: Renaming of Now assist to ServiceNow Otto.
-   Defect fixes and minor performance enhancements.

</td></tr><tr><td>

AI Platform skills

</td><td>

2026-08-07 00:00:00

</td><td>

Changes made as part of Otto rebranding.

 Plugin name changes and source display updates.

</td></tr><tr><td>

App Life Cycle AI Agents

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated to support the ServiceNow Otto brand.

</td></tr><tr><td>

Integrated Risk Management Prime

</td><td>

2026-08-07 00:00:00

</td><td>

 

</td></tr><tr><td>

External content connectors - ServiceNow Otto agent

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Name of AI agent to configure External Content Connector has been updated to External content connectors - ServiceNow Otto agent.

</td></tr><tr><td>

ServiceNow Otto for Unified Security Exposure Management

</td><td>

2026-08-07 00:00:00

</td><td>

Enhancements to the Security Exposure 360 feature:

 -   Clickable Links to Records: Counts and findings in the Security Exposure 360 output are now directly clickable, linking you to the underlying vulnerable item \(VITs\)/records in your ServiceNow AI Platform instance.
-   Suggested follow-up questions: Suggested follow-up questions are provided that help you drill down.

 Enhancements to support the ServiceNow Otto brand.

</td></tr><tr><td>

ServiceNow Otto for Platform

</td><td>

2026-08-07 00:00:00

</td><td>

The application captures dependencies, updated the plugin dependencies for this release.

</td></tr><tr><td>

Core Business Suite Advanced for Workplace Services

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Career Conversations

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.Growth Conversation Preparation AI agent has been updated to follow the Otto guidelines.

</td></tr><tr><td>

Core Business Suite Prime for Finance

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Integrated Risk Management Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

 

</td></tr><tr><td>

AI Enhanced Recommended Actions

</td><td>

2026-08-07 00:00:00

</td><td>

New: Updated to support the ServiceNow Otto brand.

</td></tr><tr><td>

Source-to-Pay Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated the in-app assistant branding and messaging from Now Assist to Otto.

 Implemented general platform security improvements.

</td></tr><tr><td>

Summarization for Order Management

</td><td>

2026-08-07 00:00:00

</td><td>

Converted the Summarization for Order Management Application into Fluent.

</td></tr><tr><td>

AI Agents for Health Log Analytics

</td><td>

2026-08-07 00:00:00

</td><td>

Internal naming conventions.

</td></tr><tr><td>

ServiceNow Otto for Customer Service Management \(CSM\)

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto is the new Al experience brand. This change is reflected in the name of ServiceNow products, including Customer Service Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

ServiceNow Otto for Impact

</td><td>

2026-08-07 00:00:00

</td><td>

What's changing.

 As part of ServiceNow's broader move to unify its AI capabilities under one brand, ServiceNow Otto, several Now Assist-powered skills within Impact have been renamed. This is a branding update only - the underlying functionality, workflows, and outputs you rely on today are unchanged.

 What this means for you.

 -   Any menu labels, skill names, or references to 'Now Assist' for these two capabilities will now show as 'Otto' across the Impact UI.
-   How you invoke these skills, the outputs they generate, or your entitlements/licensing remains the same.

</td></tr><tr><td>

Common Service Delivery

</td><td>

2026-08-07 00:00:00

</td><td>

Added indexed finance case data as a search source for Finance Knowledge article generation in Knowledge Center.

</td></tr><tr><td>

Google Gemini Spoke

</td><td>

2026-08-07 00:00:00

</td><td>

Fixed: an issue in Google Gemini Spoke OEM actions where additional headers were not being sent correctly.

</td></tr><tr><td>

Agent Workspace for HR Case Management

</td><td>

2026-08-07 00:00:00

</td><td>

Critical Functionality Fixes: Resolved critical issues preventing core case management workflows from functioning properly.

 -   Fixed: the 'Create HR Case' action bar button that was bypassing mandatory field validation on Interaction records, allowing incomplete cases to be created.
-   Restored the functionality of the Close Complete button that had been unresponsive, preventing agents from transitioning cases to the 'Awaiting Acceptance' or 'Closed Complete' states.
-   Re-enabled Approve and Reject buttons on approval sub-record forms that were missing in Agent Workspace.
-   Fixed: drag-and-drop Transfer Case functionality in the Triaging Dashboard that was not responding to user actions.

 Form and amp; Field Handling: Improved form rendering and field behaviour to provide a smoother user experience.

 -   Resolved intermittent read-only field issues on Move Attachments where the Topic Details and Document Type fields were locked despite selection, blocking attachment workflows.
-   Eliminated misleading validation error messages on the Transfer Case modal COE field that appeared even when the field was correctly auto-populated.
-   Corrected information message alignment in the Preview Document modal during document template generation.
-   Enhanced the case creation form to clarify why the Next button is disabled when the search field is empty and how Skip Verification relates to the primary form flow.

 Data Filtering and amp; Logic: Fixed how data is filtered and displayed across HR Agent Workspace lists.

 -   Corrected HR Service filtering on the Case Creation page to consistently use the Subject Person field instead of following whichever field \(Subject Person or Opened for\) was changed last, ensuring eligible services always appear.
-   Resolved the Delegated HR Cases and Delegated HR Tasks lists that showed no records.

 Performance and amp; UI Optimization: Enhanced performance and resolved display issues to ensure smooth operation at scale.

 -   Optimized attachment loading to eliminate page hangs and unresponsiveness when the system contains a large number of attachments in the Move Attachments feature.
-   Removed: console errors that were being flooded when loading the Move Attachments page in UI Builder, improving debuggability and development experience.
-   Fixed: file access permission handling for users with limited roles who received 'File Does Not Exist' errors when accessing Summary Report attachments, even though attachments were properly created.

 Localization and amp; Internationalization: Enhanced support for international users by fixing date format hardcoding in HR Agent Workspace. Date formats now properly respect locale settings and language plugins, ensuring correct date display for users with non-English language settings \(e.g., Japanese date formats for Japanese language plugin users\) and supporting localized deployments globally.

</td></tr><tr><td>

Core Business Suite For Workplace Service Delivery

</td><td>

2026-08-07 00:00:00

</td><td>

-   Shipped out-of-the-box Workplace Services knowledge base.
-   Owners and managers can be defined by the admin for the knowledge base in the Core Business Suite configuration console to ensure proper governance and content tracking.
-   Shipped Now Assist search sources for Workplace Services for Knowledge article generation from workplace case table on the Knowledge center.
-   Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

AI Desktop Actions Core

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated the AI experience branding in AI Desktop Actions to align with ServiceNow Otto naming and visual guidelines.

</td></tr><tr><td>

Core Business Suite For Source To Pay

</td><td>

2026-08-07 00:00:00

</td><td>

-   Shipped out-of-the-box Procurement and Supplier knowledge bases.
-   Owners and managers can be defined by the admin for the knowledge base in the Core Business Suite configuration console to ensure proper governance and content tracking.
-   Shipped Now Assist search sources for Source to Pay for Knowledge article generation from invoice, supplier and procurement case table on the Knowledge center.
-   Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

ServiceNow Otto for Sales Automation

</td><td>

2026-08-07 00:00:00

</td><td>

Fluent-based development support has been added.

 The app has been renamed from 'Now Assist for Sales Force Automation \(SFA\)' to 'ServiceNow Otto for Sales Automation'.

</td></tr><tr><td>

Touchpoint Meeting

</td><td>

2026-08-07 00:00:00

</td><td>

This application is included in the August 2026 A bundle as part of the coordinated TMT Service Management Bundle release. All existing functionality remains fully operational and consistent with the prior release.

</td></tr><tr><td>

App Engine - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated to support the ServiceNow Otto brand.

</td></tr><tr><td>

AI Agents for Workplace Service Delivery

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

List AI Experience

</td><td>

2026-08-07 00:00:00

</td><td>

-   Updated logos to new Otto logos and removed any references to Now Assist for AI filter assist, Track record list change, and multi record actions.
-   Replaced NowLLM with Gemini for Track record list changes.

</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

2026-08-07 00:00:00

</td><td>

--- AI Generated Release Notes ---.

 Admins can now configure document upload at the assistant level. Admins can enable or disable document upload for each assistant, ensuring consistent behavior across all user interactions.

 Admins can create and assign MCP Server connections to assistants. Admins can set up MCP Server connections in AI Agent Studio, assign them to assistants, and configure role-based access for premium chat experiences.

 Admins can enable or disable estimated wait time display for Live Agent in Chat menu items. The option to show or hide estimated wait time is now available for Chat menu items of type 'Chat.'.

 System prevents creation of duplicate Chat menu items of type 'Chat' within an assistant. Only one Chat menu item of type 'Chat' can exist per assistant.

 Playbook skills are now supported in AI search sources for premium chat. The system returns playbook skills in applicable searches, enhancing Playbook visibility for ServiceNow Otto panel assistants.

 Admins can define custom persona policies, including parametric memory settings. A new Policy persona detail type is available, allowing admins to specify custom instructions such as disabling parametric memory.

 Admins can disable the test assistant button when prerequisites are not met. The test assistant button is disabled unless the assistant is active and required configurations are complete.

 Product branding and assistant names updated from 'Now Assist' to 'ServiceNow Otto.' All UI components, pages, and customer-facing materials now reference 'ServiceNow Otto' instead of 'Now Assist,' including Assistant Designer, chat headers, and default assistant names.

 Search source names and topic names updated to be more customer-friendly. Multiple search sources and topics have been renamed to descriptive, user-focused labels.

 Enhanced Chat branding UI now clarifies dependency on selected branding profile. The branding configuration page clearly indicates that Enhanced Chat's branding relies on the selected profile.

 Basic details tab and AI agents tab enhancements. UI improvements include updated naming conventions, optional description fields, and clearer organization of assistant details.

 Welcome message management and AI prompt guidance improved for admins. Admins can select and manage localized welcome messages, update Voice AI agent content, and access in-product guidance for crafting effective AI prompts.

 Keyterm and pronunciation dictionaries added to the UI. Admins can manage keyterm and pronunciation dictionaries directly from the interface.

 Primary language configuration moved into the language config table. The system now inserts primary language records into the language table during deployment creation and updates logic for secondary language handling.

 Inactivity default timeout updated to 30 seconds. The system now uses a 30-second timeout for inactivity, replacing the previous 60-second default.

 Analysis tab now displays latency for all bot responses in voice mode. Latency values are shown next to timestamps for voice responses; chat mode displays a text flag.

 Secondary language edit functionality removed from the UI. The option to edit secondary language has been eliminated.

 Branding preview and disclaimers updated to reflect ServiceNow Otto branding. UI elements now show ServiceNow Otto branding in previews and disclaimers.

 Noise cancellation content updated for low, medium, and high categories. UI content for noise cancellation settings is revised for clarity and consistency.

 Error in setting the Assistant nickname and specialization through the Personalization page has been resolved. Assistant personalization now works as expected.

</td></tr><tr><td>

ServiceNow Otto Conversational Data Collection

</td><td>

2026-08-07 00:00:00

</td><td>

-   Custom skills display line breaks incorrectly in Now Assist Panel.
-   Data Collector doesn't trigger search after 3 retries.
-   Skill name is incorrectly extracted during slot filling.
-   User responses aren't translated back during dynamic translation.

</td></tr><tr><td>

Configuration Hub

</td><td>

2026-08-07 00:00:00

</td><td>

- Internal Code Fixes.

</td></tr><tr><td>

Core Business Suite Advanced for Human Resources

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

AI Agents for HR Service Delivery

</td><td>

2026-08-07 00:00:00

</td><td>

--- AI Generated Release Notes ---.

 -   AI Specialist now communicates ticket reassignment to users. When a ticket is reassigned from the AI Specialist to a human HR Agent, users receive a clear notification outlining next steps and expectations.
-   MCP server repository established for multi-tool development. The MCP server repository is now structured to support parallel tool development, with a baseline Hello World implementation and initial CI pipeline in place.
-   AI workers migrated to DARE architecture. AI workers now operate on the DARE architecture, with all previous off-glide workflows tested to ensure uninterrupted functionality.
-   ZTSD L1 worker template compared and validated against OOB HR L1 worker template. All new, changed, or removed properties introduced by the ZTSD platform team have been identified and tested for correctness. Documentation of differences is complete.

 HR Policy and HR Benefits removed from profile capabilities. Profile capabilities no longer display HR Policy and HR Benefits, leaving only relevant HR options for editing.

</td></tr><tr><td>

Admin Center

</td><td>

2026-08-07 00:00:00

</td><td>

Admin Home MVP redesign: Initial AIUX-based redesign and user experience refresh.

</td></tr><tr><td>

AI slot-filling for catalog items

</td><td>

2026-08-07 00:00:00

</td><td>

New: Minor enhancements.

 Fixed: Minor defects.

</td></tr><tr><td>

Workplace Reservation Management

</td><td>

2026-08-07 00:00:00

</td><td>

Only building or system time zones will be used when synchronizing reservations with external systems. The UTC time zone is used when no timezone can be determined.

 -   Unable to update the visitor parking option while editing an existing reservation.
-   Unable to edit the recurring pattern after initially setting it to custom when there was no 'Max days in future' limit configured.
-   Reservation creation could fail when using abbreviated time zone formats.
-   As an admin, clicking 'View all' in the reservation email preview did not correctly display the reservation details page with all recurring reservation occurrences.
-   Fixes to support translations.

</td></tr><tr><td>

Keyboard Shortcuts AI Skills

</td><td>

2026-08-07 00:00:00

</td><td>

Generally Available Compatibility: Support for Next Experience interfaces where keyboard shortcuts are configurable.

</td></tr><tr><td>

Workplace Visitor Management

</td><td>

2026-08-07 00:00:00

</td><td>

New: The introduction of new API end points to support artificial intelligence platforms.

</td></tr><tr><td>

ServiceNow Otto for Platform Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

The application captures dependencies, updated the plugin dependencies for this release.

</td></tr><tr><td>

Invoice Case Management

</td><td>

2026-08-07 00:00:00

</td><td>

This release includes fixes for reported defects to improve product stability.

</td></tr><tr><td>

Talent feedback

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

 As part of this version, the Now Assist Icon in the 'Request feedback' button on the employee feedback page in Manager Hub was updated.

</td></tr><tr><td>

AI Analytics

</td><td>

2026-08-07 00:00:00

</td><td>

-   Granular analytics for AI asset evaluations and performance - Users can now access detailed evaluation KPIs for deployed AI assets, including manual and automated evaluations, asset consumption metrics, and trendlines with benchmarks. The analytics dashboard supports custom date range filters and provides granular feedback indicators for conversation interactions, negative feedback reasons, and free-text comment usage.
-   Auto Evaluation dashboard with KPI cards and asset type filtering - The Auto Eval dashboard now displays KPI cards for asset health, evaluation status, and monthly assists, with filtering by asset type \(agent, skill, assistant\).
-   Detailed asset evaluation pages and asset lists - Users can view individual asset evaluation details, including latest scores, evaluation run history, and benchmark trendlines. Asset lists are available for auto evaluation, supporting drill-down and comparison.
-   Performance Explorer Skills tab with skill detail panel - The Performance Explorer now includes a Skills tab showing skill usage, feedback quality, unique users, and allows drill-down to detailed metrics for each skill, including Guardian safety indicators.
-   Custom date range filter for analytics dashboards - Users can select custom start and end dates for dashboard data, with selections persisting during sessions.

 Now Assist rebranding - All analytics screens, dashboard titles, and icons have been updated to reflect ServiceNow Otto for interactive surfaces and AI for background metrics.

</td></tr><tr><td>

Chat Summarization for Virtual Agent

</td><td>

2026-08-07 00:00:00

</td><td>

Changes related to Otto Rebranding Directive.

</td></tr><tr><td>

AI for document designer

</td><td>

2026-08-07 00:00:00

</td><td>

AI-powered Word content generation now supports advanced third-party models. Users can generate and manage Microsoft Word report content using new AI models, including Gemini 3.5 Flash \(with fallback to 2.5 Pro\), GPT-5.4-mini, and Claude 4.5 Haiku, improving content accuracy and performance.

 ServiceNow Otto Branding Updates: Updated the application to reflect the new ServiceNow Otto branding, replacing Now Assist references and providing a more consistent AI experience across the platform.

</td></tr><tr><td>

AI Experience Framework

</td><td>

2026-08-07 00:00:00

</td><td>

This app contains the core AIUX framework that powers the next generation of AI Native Experiences by providing a unified platform for designing, deploying, and managing intelligent user interfaces. This store app specifically contains the key metadata tables for managing key entities such as pages, widgets, experiences, and page routes, which power the new experiences. The plugin ensures that customers can leverage AI native experiences such as Employeeworks, build new experiences, and develop custom widgets, all while maintaining compliance with industry standards and scalability requirements.

 Key Note: This is a free plugin and does not have any AI licensing requirements.

</td></tr><tr><td>

GRC Shared GenAI

</td><td>

2026-08-07 00:00:00

</td><td>

Changes.

 -   Multiple record association \(MRA\) security enhancements: Authorization validation has been strengthened within MRA workflows to consistently enforce access checks during record association operations.
-   Query Range ACL enhancements: Improved application security by adding query range access controls and strengthening authorization checks across supported data models. This helps ensure users can access only the data they are authorized to view.

</td></tr><tr><td>

ServiceNow Otto for Employee Experience

</td><td>

2026-08-07 00:00:00

</td><td>

Otto rebranding: All references to AIA, Moveworks, or Now Assist are replaced with Otto throughout. You can see Otto as the assistant in all relevant interfaces and documentation.

</td></tr><tr><td>

AI Security and Privacy

</td><td>

2026-08-07 00:00:00

</td><td>

This is a major release of the AI Control Tower Security pillar, delivering the following capabilities.

 -   AI agent containment with kill switch protocol \(phase 1\): Revoke AI agent session tokens through Okta, deactivate and reinstate AI agents running in AWS Bedrock, AWS Bedrock AgentCore, GCP Vertex AI \(limited support\), and ServiceNow agents.
-   Extended agent map schema: On the map, you can see nodes for LLMs and MCP servers for complete resource visibility across your enterprise. Previously, the map only showed agentic workflows, AI agents, tools, and providers.
-   System prompt leakage, threat monitoring, and sensitive data disclosure post-runtime metrics are now configured and active by default. Previously, you had to enable them manually.
-   Veza access intelligence usability: Improved messaging in Access Intelligence tab of AI assets in agent map.
-   Overview and Runtime metric quality: Improved accuracy of AI threat metrics and evaluation datasets that use Traceloop for continuous monitoring.
-   Now Assist was renamed to ServiceNow Otto.
-   Number of clients connecting to MCP servers metrics in Overview metrics.
-   Ability to create security incidents from dormant agents using conversational prompts.

</td></tr><tr><td>

Financial Services Operations Core

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Centralized currency rounding precision logic into a shared utility, ensuring consistent handling of the platform's currency fraction digits setting across all consumers.

</td></tr><tr><td>

ServiceNow Otto for RPA Hub

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated the AI experience branding in RPA Desktop Design Studio to align with ServiceNow Otto naming and visual guidelines.

</td></tr><tr><td>

MIF Customer Instance

</td><td>

2026-08-07 00:00:00

</td><td>

-   A new column, retirement date, is now available in the sn\_mif\_instance table for licensing to consume and use to manage entitlements.
-   Clone exclusion and preserver are available in the sn\_mif\_vtable\_operation\_context table.

</td></tr><tr><td>

Agentic Contact Center for Banking

</td><td>

2026-08-07 00:00:00

</td><td>

-   Changed: Updated internal application components to support ongoing platform enhancements.
-   Updated 'ServiceNow Otto' branding for Agentic Contact Center for Banking.

</td></tr><tr><td>

Schedule Optimization

</td><td>

2026-08-07 00:00:00

</td><td>

Made Security enhancements on Schedule Optimization store app compatible to Australia release.

 No Actions needed from customer while upgrading to this version.

</td></tr><tr><td>

Platform AI Agents and Skills

</td><td>

2026-08-07 00:00:00

</td><td>

New: Identify Escalation Signals agentic workflow now includes suggested actions, to help fulfillers take action on potential escalations.

 -   Updated the Generate my work plan agentic workflow summary and reasoning to make it more understandable and relevant to end users.
-   Enabled citations for resolution notes. Users can directly reference which work note/comment/KB section the resolution note came from and navigate there.
-   Agentic workflows can now be triggered using survey record number in the utterance.
-   Updated branding of Now Assist to Otto, inline with the Otto directive.
-   Performance improvements to the Analyze task trends agentic workflow.
-   Added 'Show Citations' toggle in the NAA guided-setup wizard for Record Resolution Notes.
-   Fixed: greetings appearing in the Branded Email response generated by LLM.
-   Added 3P model support for replan skill as part of Generate my work plan agentic workflow.

</td></tr><tr><td>

Core Business Suite Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

-   Shipped out-of-the-box knowledge bases defined at two levels: individual business unit knowledge bases \(Human Resources, Legal, Source to Pay, Workplace Services, and Health and amp; Safety\) and a CBS aggregate knowledge base.
-   Owners and managers can be defined by the admin in the Knowledge module for each knowledge base to ensure proper governance and content tracking.
-   Added new AI skills module under the Platform module on Configuration console enables admins to activate knowledge-specific skills from simplified setup.
-   Improve article optimization in terms of content quality, identification, and merging of duplicate articles to eliminate redundant content.
-   Shipped Now Assist search sources for all the business unit for Knowledge article generation from case tables on Knowledge center.
-   Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

 Admins can now manage access to the Core Business Suite analytics dashboard through the new Groups module under Core Business Suite module. Define which users have view and edit access by adding them to groups, providing fine-grained control over who can access reporting and metrics across your Core Business Suite implementation.

</td></tr><tr><td>

Core Business Suite Foundation for Human Resources

</td><td>

2026-08-07 00:00:00

</td><td>

Shipped out-of-the-box Human Resources knowledge base.

 Owners and managers can be defined by the admin for the knowledge base in the Core Business Suite configuration console to ensure proper governance and content tracking.

 Shipped Now Assist search sources for Human Resources for Knowledge article generation from legal case table on Knowledge center.

 Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

Generative AI Controller

</td><td>

2026-08-07 00:00:00

</td><td>

New: Added support for capabilities provided by newest AI models \(Latest Azure OpenAI, Gemini, and Claude models\).

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Enhancements to the Security Exposure 360 feature:

 -   Clickable Links to Records: Counts and findings in the Security Exposure 360 output are now directly clickable, linking you to the underlying vulnerable item \(VITs\)/records in your ServiceNow AI Platform instance.
-   Suggested follow-up questions: Suggested follow-up questions are provided that help you drill down.

 Enhancements to support the ServiceNow Otto brand.

</td></tr><tr><td>

CSM - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Updated with the latest version of ServiceNow Otto Customer Service Management \(CSM\).

</td></tr><tr><td>

Core Business Suite for Human Resources

</td><td>

2026-08-07 00:00:00

</td><td>

-   Shipped out-of-the-box Human Resources knowledge base.
-   Owners and managers can be defined by the admin for the knowledge bases in the Core Business Suite configuration console to ensure proper governance and content tracking.
-   Shipped Now Assist search sources for Human Resources for Knowledge article generation from legal case table on the Knowledge center.
-   Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

Alert Assist

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: All 'Now Assist' references across the application have been updated to ServiceNow Otto.

</td></tr><tr><td>

Catalog Conversational Coverage

</td><td>

2026-08-07 00:00:00

</td><td>

Minor enhancements.

</td></tr><tr><td>

Financials Core

</td><td>

2026-08-07 00:00:00

</td><td>

-   Fixed: an issue where financial plans didn't support negative budget values.
-   Fixed: an issue where a script naming conflict caused actuals to aggregate incorrectly after upgrade.
-   Fixed: an issue where customized access control rules on cost plan breakdowns weren't applied on the Financials tab of Project Workspace.
-   Fixed: an issue where long text strings caused overflow in Financial Dashboard widgets.

</td></tr><tr><td>

Third-party Risk Management Professional Plus

</td><td>

2026-08-07 00:00:00

</td><td>

Updated.

 -   Rebranded to ServiceNow OTTO, replacing Now Assist references for a consistent AI experience.
-   Enhanced MRA authorization validation to ensure access checks are consistently enforced during record association.

</td></tr><tr><td>

Custom App Record Summarization

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated to support the ServiceNow Otto brand.

</td></tr><tr><td>

ServiceNow Otto for Conversational Spokes

</td><td>

2026-08-07 00:00:00

</td><td>

Rebranding from Now Assist to ServiceNow Otto.

</td></tr><tr><td>

AI Experience Framework Skills

</td><td>

2026-08-07 00:00:00

</td><td>

- Introduce support for creating widgets in the new format, ensuring compatibility with the pro-code developer experience.

</td></tr><tr><td>

Conversational Studio

</td><td>

2026-08-07 00:00:00

</td><td>

-   Bulk migration of Topics to AI Agents is now supported. Admins can select and migrate batches of 100+ Topics to AI Agents at once using the Topics-to-AI Agents tool.
-   Auto Evaluation integration for migrated AI Agents. The Topics-to-AI Agents tool now integrates with Auto Evaluation, allowing users to review the quality of migrated AI Agents.
-   Dataset creation and evaluation for migrated Topics. Users can create datasets and run automated evaluations comparing migrated Topics and AI Agents, with comparison metrics displayed upon completion.
-   NLU deprecation banner in Asset Library. A legal-approved banner now displays in the Assistant Designer Asset Library when NLU assets are present or the NLU/Keyword filter is active. The banner includes a 'Learn More' link to deprecation documentation and is dismissible per user session.
-   Assignment of active Assets to inactive Assistants. Users can assign active Assets-including Topics, Subflows, Actions, AI Agents, Agentic Workflows, and Custom Skills-to inactive Assistants via Asset and gt; Conversational Settings, with clear differentiation between active and inactive Assistants in the UI.
-   Test assistant button availability. The 'Test assistant' button in Assistant Designer is now disabled when the Voice assistant is not active or prerequisites are incomplete.
-   Asset pages and Asset Library updates. The Asset pages and Asset Library have been updated to reflect new design standards and improved usability.

 Migrated Topics now correctly display their migration status. The system accurately discerns the 'isMigrated' state for NLU topics, resolving previous inconsistencies.

</td></tr><tr><td>

sn-ia-summary-card

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand.

</td></tr><tr><td>

APO - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

The application captures dependencies, updated the plugin dependencies for this release.

</td></tr><tr><td>

Legal Counsel Center

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: ServiceNow Otto is the new AI experience brand. Now Assist for Legal Service Delivery is ServiceNow Otto for Legal Service Delivery.

 -   Cancelling an edit to a Quick Link on Legal Counsel Center Home page now correctly restores the original display name and URL instead of retaining the unsaved changes.
-   Security fixes.

</td></tr><tr><td>

Agentic Contact Center for Insurance

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated 'ServiceNow Otto' branding for Agentic Contact Center for Insurance.

</td></tr><tr><td>

ServiceNow Otto for Care Team Operations

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist for Care Team Operations has been renamed to ServiceNow Otto for Care Team Operations.

</td></tr><tr><td>

sn-actionable-insights

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand.

</td></tr><tr><td>

IT Service Management Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

No changes.

</td></tr><tr><td>

ServiceNow Otto for Vault

</td><td>

2026-08-07 00:00:00

</td><td>

-   Starting with Australia Patch 5, Now Assist for Vault is now ServiceNow Otto for Vault. This name change reflects the evolution of AI assistance on the platform into a conversational, agentic AI experience. All existing functionality, configurations, and AI-powered security capabilities are unchanged.
-   Azure OpenAI is now the default model for all AI assets in ServiceNow Otto for Vault, including the Discovery data pattern grouping skill and the Data Discovery Job Summarization skill. Existing configurations that use the Now LLM Service continue to work as before, and you can still select the Now LLM Service manually.

</td></tr><tr><td>

Agent Client Collector for Visibility Content

</td><td>

2026-08-07 00:00:00

</td><td>

ACC is now certified on below list of Operating Systems - Red Hat Enterprise Linux \(RHEL\) 10 - x86\_64Rocky Linux 10 - x86\_64Oracle Linux 10 - x86\_64Ubuntu Linux - ARM64 \(aarch64\).

 Improved Oracle Java Discovery using process based detection - complementing the FBD solution for a more accurate solution.

</td></tr><tr><td>

Conversational subflows and actions

</td><td>

2026-08-07 00:00:00

</td><td>

-   Discontinued Now LLM to use third-party model for CSA Skills.
-   Renamed Now Assistant to ServiceNow Otto in CSA Side Panel.
-   Created the required Query\_range ACLs as per Cobalt raven directive.

</td></tr><tr><td>

Financial Services Operations AI agent collection

</td><td>

2026-08-07 00:00:00

</td><td>

Fixed: Fixed multilingual output in Friendly fraud AI Agent.

</td></tr><tr><td>

Opportunity Management Data Model

</td><td>

2026-08-07 00:00:00

</td><td>

-   Added support for Opportunity records in global search.
-   UI refinements on the Opportunity page - padding fixes and rebranding updates.
-   Quote tasks for primary quotes now appear in the To-Do section of the Opportunity Overview page.
-   Added configurable dependency between Won/Lost stage and Won/Lost reason fields, controlled via system properties.
-   Resolved UX defects on the Opportunity Overview page and Guided Selling experience.
-   Fixed: semantic search results for Opportunity records.
-   Corrected inconsistencies in Contract End Date and Term \(months\) calculations within Opportunity Management.
-   Price list on Opportunity now updates correctly when currency is changed.
-   Resolved intermittent 'One or more property values are invalid' error in Manage Allocations when saving allocation splits.
-   Addressed performance issues on the Opportunity page.

</td></tr><tr><td>

Workplace Space Management

</td><td>

2026-08-07 00:00:00

</td><td>

Security fixes.

</td></tr><tr><td>

ITSM Fulfiller Experience

</td><td>

2026-08-07 00:00:00

</td><td>

No changes.

</td></tr><tr><td>

On Call Scheduling for Service Operations Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

AI Skill Kit

</td><td>

2026-08-07 00:00:00

</td><td>

-   Now Assist Skill Kit is now renamed to AI Skill Kit.
-   The default model provider for skills is now Azure \(from NowLLM\). Newly created skills will use Azure as the default provider unless explicitly changed.

</td></tr><tr><td>

Collaborative Work Management - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: SPM's Project Workspace now has an integration with Collaborative Work Management Team Members can create new CWM tasks/stories under an assigned project task.
-   Users can move or break a CWM task's connection to a different project task.
-   Project Managers will see CWM tasks/stories connected to their project tasks directly inline in the Planning page of the Project in Project Workspace.
-   Team Members in CWM see their connected project and project tasks as columns in CWM list view, and in 'My Work'.
-   Relationships for any task types can added now using Task number/id instead of just Task description.
-   Now Assist is now ServiceNow Otto.

</td></tr><tr><td>

HRSD - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Otto skills and a refreshed user interface for Otto.

</td></tr><tr><td>

HCLS - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

New: Dependency version fixes and branding fixes.

</td></tr><tr><td>

Source-to-Pay Common Architecture

</td><td>

2026-08-07 00:00:00

</td><td>

-   Added the Jurisdiction field to Invoice Tax Line to capture the jurisdiction associated with a tax line.
-   Added Jurisdiction Type and Tax Authority fields to Invoice Tax Line. These fields populate automatically based on the selected jurisdiction or tax type.
-   Enhanced the Invoice Tax Line form and list view to display jurisdiction, jurisdiction type, and tax authority.
-   Updated duplicate tax line detection to use the combination of tax type, jurisdiction, and jurisdiction type instead of tax type alone.
-   When adding or editing a tax line, jurisdiction type and tax authority now populate automatically based on the selected jurisdiction or tax type.

</td></tr><tr><td>

ServiceNow Otto for Talent

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

 In this version, Now Assist for Talent app has been renamed to ServiceNow Otto for Talent.

</td></tr><tr><td>

AIOps Agentic Workforce

</td><td>

2026-08-07 00:00:00

</td><td>

-   The autonomous workflow now supports AWS Claude as an AI agent provider, improving compatibility with additional AI services.
-   The alert investigation insight prompt now accepts longer input, allowing for more detailed queries.
-   The Impact Agent search has been improved to return more relevant related issues.

</td></tr><tr><td>

CSM MCP Server

</td><td>

2026-08-07 00:00:00

</td><td>

New: Sentiment Analysis and amp; Activity Response Generation.

 Two new GenAI skills for CSM MCP Server, with full enterprise security and intelligent plugin gating. Tools deploy only on instances where the com.sn.csm.gen.ai plugin is active-no setup errors, no unnecessary dependencies.

</td></tr><tr><td>

Operational Sustainability Management Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto Branding Updates Updated the application to reflect the new ServiceNow Otto branding, replacing Now Assist references and providing a more consistent AI experience across the platform.

</td></tr><tr><td>

Core Business Suite for Health and Safety

</td><td>

2026-08-07 00:00:00

</td><td>

-   Shipped out-of-the-box Safety knowledge base.
-   Owners and managers can be defined by the admin for the knowledge base in the Core Business Suite configuration console to ensure proper governance and content tracking.
-   Shipped user criteria for Health and amp; Safety knowlegde base.
-   Shipped Now Assist search sources for Health and amp; Safety for Knowledge article generation from health and safety case table on the Knowledge center.
-   Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

GRC: Profiles

</td><td>

2026-08-07 00:00:00

</td><td>

\*\*New\*\* None \*\*Changed\*\* None \*\*Fixed\*\* Fixed Cobalt Pegasus vulnerability by enforcing Glide Record Secure while querying/saving data through MRA components. \*\*Removed\*\* None.

</td></tr><tr><td>

Record - vertical

</td><td>

2026-08-07 00:00:00

</td><td>

-   Changed: Updated the application to reflect the new ServiceNow Otto branding, replacing Now Assist references and providing a more consistent AI experience across the platform.
-   The record page on Operational Sustainability management workspace for Campaigns now shows a tick mark when the actions in its related lists are completed.
-   It also groups the records within the related list based on the group field configured.

</td></tr><tr><td>

HRSD - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Otto skills and a refreshed user interface for Otto.

</td></tr><tr><td>

ServiceNow Otto for Collaborative Work Management \(CWM\)

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: SPM's Project Workspace now has an integration with Collaborative Work Management Team Members can create new CWM tasks/stories under an assigned project task.
-   Users can move or break a CWM task's connection to a different project task.
-   Project Managers will see CWM tasks/stories connected to their project tasks directly inline in the Planning page of the Project in Project Workspace.
-   Team Members in CWM see their connected project and project tasks as columns in CWM list view, and in 'My Work'.
-   Relationships for any task types can added now using Task number/id instead of just Task description.
-   Now Assist is now rebranded as ServiceNow Otto.

</td></tr><tr><td>

Sales Development AI Agents

</td><td>

2026-08-07 00:00:00

</td><td>

Fluent based development support added.

</td></tr><tr><td>

ServiceNow Otto for IT Service Management \(ITSM\)

</td><td>

2026-08-07 00:00:00

</td><td>

-   AI can now automatically complete Change Risk Assessment and Dynamic Schema questions based on the change record's context, showing its reasoning for each answer so admins and change managers can verify or correct it. Answers that identify compliance exposure \(for example SOX, PCI-DSS, or HIPAA\) automatically populate the matching Dynamic Schema fields.
-   A new AI agent can diagnose and resolve common Okta account lockouts and MFA failures reported through an incident or self-service, checking live account status and submitting the correct unlock or reset request automatically.
-   A new Teams-native AI agent lets shift agents manage on-call coverage directly in chat - requesting coverage or leave, and asking questions like 'who is on call' or 'when is my next shift.'.
-   Employees creating a ticket in Service Portal now see an AI-generated suggestion - drawn from relevant knowledge articles and catalog items - before they submit, based on the ticket description and their hardware, location, and department.
-   Now Assist, Moveworks, and 'AI Experience' branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
-   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
-   A new dashboard section shows how closely AI-proposed solutions in Copilot \(supervised\) mode matched what human agents ultimately implemented.
-   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
-   The DEX Diagnosis AI agent now factors in event monitoring logs and statistical anomaly signals alongside existing telemetry for more accurate root-cause diagnoses, and now surfaces the specific evidence behind each conclusion.
-   Fixed: an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
-   Fixed: an issue where several AI agents \(including Zscaler, Installed Apps, and Modern Change agents\) had read-only configuration, preventing customers from disabling them.
-   Fixed: an issue where the Zscaler and Installed Apps agents' action engagement tools showed an empty timeout field.
-   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
-   Fixed: an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
-   Fixed: a date-formatting issue in the Change Outage Assistant AI agent.
-   Fixed: a security issue that allowed any authenticated user, regardless of role, to invoke ITSM AI agents and skills that should have been role-restricted.
-   Fixed: an issue where the incident investigation and resolution workflow could fail with an 'incident search/read service unavailable' error.
-   Fixed: an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
-   Reordered the metrics on the Copilot Performance dashboard so the '80% or higher similarity' metric appears first.
-   Improved the error message shown for the Resolution Notes generation skill when the 'display in product desktop' setting is turned off.
-   Reduced processing time for the Generate Change Request Plans AI flow, which had been taking an unusually long time to complete.
-   Fixed: an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform.
-   Fixed: an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users.
-   Fixed: an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own.

 No items removed in this release.

</td></tr><tr><td>

Threat Intelligence Support Common

</td><td>

2026-08-07 00:00:00

</td><td>

-   Fixed: the observable identification logic while adding an observable.
-   Fixed: the translation issues for UI messages.

</td></tr><tr><td>

ServiceNow Otto for ICW

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: in this release: ServiceNow Otto for Industrial Connected Workforce is the new name for Now Assist for ICW.

</td></tr><tr><td>

Core Business Suite Prime for Human Resources

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Threat Intelligence Security Center - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Added support for Google Gemini 3.5 Flash and OpenAI GPT 5.4 mini models for Case summarization.

 Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand.

</td></tr><tr><td>

Data Privacy

</td><td>

2026-08-07 00:00:00

</td><td>

\*RTA not supporting selection of child tables from different scopes other than the scope of the policy\*All columns selected from parent automatically apply to children \(Need to add support for handling inherited child table field separately\).

</td></tr><tr><td>

ServiceNow Otto for Contract Analysis

</td><td>

2026-08-07 00:00:00

</td><td>

Starting with v1.0.15, Now Assist for Software Asset Management is now ServiceNow Otto for Software Asset Management.

</td></tr><tr><td>

RPA Hub

</td><td>

2026-08-07 00:00:00

</td><td>

-   Changed: Improved the ability to map credential records to automation processes, enhancing configuration flexibility for RPA administrators.
-   Enhanced the functionality for organizing and grouping robots to improve automation distribution and workload management.
-   Security enhancements to strengthen authorization controls and data protection across the application.

</td></tr><tr><td>

Service Operations Workspace Core

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

Enterprise Architecture Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

-   Added four new entity types - Business Actor, Business Role, Stakeholder, and Driver to the Business Architecture section of the Portfolio page.
-   Added business capabilities and business process as related lists on the Goals page in the Business Architecture section of the Portfolio page.
-   Added business capabilities and business process as related list on the Business Unit page in the Business Architecture section of the Portfolio page.
-   Added goals as related list on the Business Processes and Business Capabilities page in the Business Architecture section of the Portfolio page.
-   Added business units as related list on the Business Processes and Business Capabilities page in the Business Architecture section of the Portfolio page.

 Renamed Now Assist to ServiceNow Otto. All Enterprise Architecture Workspace screens, icons, and generative AI skill names now reflect the ServiceNow Otto brand.

 -   Corrected the French translation of Retire in the bubble chart labels and captions.
-   Out-of-the-box business application certification policies now ship inactive by default, preventing unintended task creation.
-   Sorting by hierarchy ID in the Business Portfolio now uses natural numeric ordering, so capabilities sequence correctly \(1.1 and rarr; 1.2 and rarr; ... and rarr; 1.9 and rarr; 1.10 and rarr; 1.11\) instead of being sorted as text.
-   The Save button now displays for Business Applications in CMDB Workspace, matching the classic UI.

</td></tr><tr><td>

Insights Clustering Utils

</td><td>

2026-08-07 00:00:00

</td><td>

No major changes.

</td></tr><tr><td>

Vault Console

</td><td>

2026-08-07 00:00:00

</td><td>

-   The security\_admin role has been removed from the roles required to elevate to and administer Vault Console. All administrative tasks including that of viewing tools metrics across the dashboard is now available to the sn\_vault\_console.vault\_console\_admin. This change was made to conform with the principle of least privilege, ensuring administrators only elevate to roles they actually need.
-   UI fixes to ensure interface elements are displayed according to entitlement settings.

</td></tr><tr><td>

Integrated Risk Management Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

 

</td></tr><tr><td>

ServiceNow Otto for Enterprise Asset Management

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: All visible references to 'Now Assist' have been updated to 'ServiceNow Otto' to ensure consistent branding.

</td></tr><tr><td>

ServiceNow Otto for Integration Hub

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Name change from Now assist to ServiceNow Otto.

</td></tr><tr><td>

Contract Management Pro - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

New: Conversational search results can be exported in multiple file formats.

 ServiceNow Otto is the new AI experience brand. Now Assist in Contract Management is now ServiceNow Otto for Contract Management Pro.

 Contract fulfillers can trigger AI review for contracts stored in external storage.

</td></tr><tr><td>

ServiceNow Otto for HR Service Delivery \(HRSD\)

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

 New: Skills released:Activity Response Generation skill:

 -   Actions surface in case record: Suggest response, Post response, Refine.
-   'Suggest a response' generates a relevant, non-empty AI response for an HR case with sufficient activity context.

</td></tr><tr><td>

sn-formula-kit

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: System administrators can decide the list of functions that display in the Formula columns.

</td></tr><tr><td>

Project Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

-   Users can now customize L2 menu items in Project Workspace. Users are able to personalize the L2 menu without system issues, and their customization settings persist across sessions. When enabled by an administrator, the legacy RIDAC page is hidden to streamline navigation. Customization applies consistently for all users with appropriate permissions.
-   Project managers can view connected tasks and stories inline in the Planner tab. Connected CWM tasks and stories now display as child rows under each project task in the Planner, with standard columns shown and collapsible rows. Inline editing is disabled for these child tasks; edits can be made in the form view as permitted.
-   A toggle button is now available in Project Workspace settings to show or hide connected tasks. By default, the toggle is turned on, displaying all CWM and Project Workspace tasks. Turning it off hides connected tasks from view.
-   Performance improvements have been made to AI-generated status reports. Status report generation now runs asynchronously, resulting in faster performance for the health widget and executive summary widget in In-App insights.
-   All customer-facing SPM product documentation now uses the 'ServiceNow Otto' name. References to 'Now Assist,' 'Moveworks,' and 'AI Experience' have been updated to 'ServiceNow Otto' in documentation, following the Otto Naming Guidelines.
-   Changes made in the Project Workspace Planning tab are now retained after refreshing the page. Previously, updates could be lost due to errors in handling planning attributes; this has been resolved.
-   The Status Report UI Action now opens the correct page without errors. The routing logic has been updated to ensure the status report page loads as expected.
-   Export logs from the Project Workspace now correctly indicate whether the export was performed from the Planning or Financials page, improving traceability.

</td></tr><tr><td>

Software Asset Management AI Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Starting with v2.4.2, Now Assist for Software Asset Management is now ServiceNow Otto for Software Asset Management.

</td></tr><tr><td>

ITOM AI Agents For Service Mapping

</td><td>

2026-08-07 00:00:00

</td><td>

-   ServiceNow Otto is the new AI experience brand. This name change is reflected in ServiceNow products, including ITOM AI Agents For Service Mapping. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

</td></tr><tr><td>

ServiceNow Otto for Software Asset Management \(SAM\)

</td><td>

2026-08-07 00:00:00

</td><td>

Starting with v10.4.0, Now Assist for Software Asset Management is now ServiceNow Otto for Software Asset Management.

</td></tr><tr><td>

App Studio Commons

</td><td>

2026-08-07 00:00:00

</td><td>

Maintenance release.

</td></tr><tr><td>

Flow Diagramming

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Rebranded UI for ServiceNow Otto.

</td></tr><tr><td>

Journey designer

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

 -   Updated agentic workflows in Journey Designer to align with the Otto rebranding initiative.
-   Replaced legacy product terminology, labels, visual references and user-facing text with Otto branding.

</td></tr><tr><td>

Telecommunications Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Otto rebranding changes.

</td></tr><tr><td>

Telecommunications Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Otto Rebranding.

</td></tr><tr><td>

Deployment Pipeline

</td><td>

2026-08-07 00:00:00

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

2026-08-07 00:00:00

</td><td>

-   Product roles and functional domain separation. Product roles have been restructured with updated role inheritance and licensing exclusions, enabling clearer role management and functional domain separation in ESG.
-   Unified Document Designer add-in. The Office 365 reporting and Document Designer add-ins have been consolidated into a single unified Document Designer plugin with updated manifest and business domain support.
-   Read access to emission calculation guidelines is now restricted to the cmdagentuser role only.
-   The read access of the GRC confidentiality user role on the Portfolio Management Goal Framework table has been reviewed and updated.
-   Business domain references for uptaking teams are now updated automatically via a new script.
-   Demo data has been corrected to align with updated role and domain separation changes.
-   The metric picker now loads quickly when adding Metric to Target relationships via related lists.
-   Metric data task values are no longer set to null when edited with multibyte characters.
-   Related list UX form values sourced from the main form are now retained when reloading in the ESG workspace.
-   The Document ID field is now read-only and is populated automatically.
-   Accessibility issues across the application have been resolved.
-   List type data visualization is now available for selection in Reporting configuration.
-   The record-vertical child page now correctly sets values when using the Form controller.

</td></tr><tr><td>

GRC: Metrics

</td><td>

2026-08-07 00:00:00

</td><td>

-   Campaigns support metric bundling and unified workflow management: Metric Campaigns bundles metrics by group, entity, frequency, and calendar into a single coordinated workflow, ensuring all metric types move through data collection, submission, and approval together as one transaction. Campaign cycles are automatically generated periodically based on the frequency configured at the campaign level.
-   Streamlined campaign UI and bulk actions: The campaign workspace provides a scalable interface for managing up to 30 metrics across 17 entities, with dropdown filters and minimized scrolling. Users can bulk submit and approve metric data tasks, and tick marks indicate completion status for campaign setup steps.
-   Configurable data owner and approval workflows: Admins can assign data owners and configure single-level or multi-level approval workflows for campaigns, with validation to prevent conflicts between data owners and approvers.
-   Enhanced metric data task \(MDT\) lifecycle and UI: Metric data tasks now support campaign-driven scheduling, custom due dates, and read-only data fields for calculated metrics. The MDT UI includes new filters for project and task, project details on the ribbon, and approval page updates for bulk actions.
-   Threshold variance calculation and configuration: Metric definitions now support configurable variance base values and improved variance calculation logic, including handling of missing or overridden data and immediate client-side updates.
-   Support for calculated metric definition \(CMD\) task creation and approval: Tasks are now generated for calculated metrics, enabling review and approval before data is used in disclosures or reporting. CMD recalculation occurs in real time when source data changes, and approval flows are fully supported.
-   Naming conventions for campaign cycles: Campaign cycles are named according to frequency \(daily, weekly, monthly, quarterly, semi-annually, annually\) for clarity and consistency.
-   Campaign and metric data task logic updated for campaign-driven scheduling: When a metric is part of an active, published campaign, its data collection schedule, due date, and lifecycle are governed by the campaign rather than the individual metric definition. Updates to campaign cycles or due dates are reflected across all associated tasks.
-   Bulk state updates for campaign cycles: Campaign cycles automatically transition to 'Approval' or 'Closed' states based on the status of underlying tasks, eliminating manual intervention.
-   Validation and filtering improvements for campaign setup: Entity selection now prevents duplicates, and the system shows an error message when a user attempts to add an entity already present in another campaign with matching group, frequency, and calendar. Bulk submission is disabled by default for new campaigns.
-   Metric data logic refined for task state and value propagation: Metric data values populate immediately when child tasks complete, but the state remains 'in-progress' if tasks are enabled. CMD recalculation and approval flows are updated so task states and value propagation stay correct.
-   Approval configuration UI updated: The data owner and approval configuration page now supports adding multiple approval levels, error handling for empty or conflicting values, and automatic clearing of multi-level settings when switching to single-level approval.
-   Field-level access controls and UI policies updated: Data owner and approver fields are now managed at the campaign level, with updated ACLs and UI policies to enforce correct permissions and field behaviors.

</td></tr><tr><td>

UI Components for Customer Portals

</td><td>

2026-08-07 00:00:00

</td><td>

Defect fixes.

</td></tr><tr><td>

ServiceNow Otto for Knowledge Management

</td><td>

2026-08-07 00:00:00

</td><td>

Auto-update, auto-merge and otto branding updates.

</td></tr><tr><td>

Opportunity Management Application

</td><td>

2026-08-07 00:00:00

</td><td>

-   Added support for Opportunity records in global search.
-   UI refinements on the Opportunity page - padding fixes and rebranding updates.
-   Quote tasks for primary quotes now appear in the To-Do section of the Opportunity Overview page.
-   Added configurable dependency between Won/Lost stage and Won/Lost reason fields, controlled via system properties.
-   Resolved UX defects on the Opportunity Overview page and Guided Selling experience.
-   Fixed: semantic search results for Opportunity records.
-   Corrected inconsistencies in Contract End Date and Term \(months\) calculations within Opportunity Management.
-   Price list on Opportunity now updates correctly when currency is changed.
-   Resolved intermittent 'One or more property values are invalid' error in Manage Allocations when saving allocation splits.
-   Addressed performance issues on the Opportunity page.

</td></tr><tr><td>

ServiceNow Otto for Accounts Payable Operations \(APO\)

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, references to Now Assist have been replaced with ServiceNow Otto.

</td></tr><tr><td>

ServiceNow Otto for Strategic Portfolio Management

</td><td>

2026-08-07 00:00:00

</td><td>

-   Use the Budget Overrun insight card in Portfolio AI Insights to view real-time analysis of planning items with forecasts over budget, including impact assessment, root cause analysis, and recommended next steps to proactively manage budget overruns and allocation decisions.
-   Updated all customer-facing references from 'Now Assist' to 'ServiceNow Otto' across SPM products and UI components.
-   Access a dedicated AI Overview tab for demand summarization on the demand record page.
-   Project Q and amp;A now supports questions about work notes and dependencies on a project.
-   Improved the performance of AI project status report generation to create draft reports faster.
-   Improved the output quality and performance of goal insights generation.
-   Improved AI-identified risk generation with minor functional enhancements.

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2026-08-07 00:00:00

</td><td>

-   Fixed: issue retrieving expenses for Zoho agent fails.
-   Fixed: issue with HR case creation agent needing an HR role.

</td></tr><tr><td>

ServiceNow Otto for Opportunity Management

</td><td>

2026-08-07 00:00:00

</td><td>

Renamed the plugin from Opportunity management AI feature' to 'ServiceNow Otto for Opportunity Management.

 Provides more clear Error messages on Claude for a few scenarios.

</td></tr><tr><td>

APO - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

The application captures dependencies, updated the plugin dependencies for this release.

</td></tr><tr><td>

Product Catalog Management Core

</td><td>

2026-08-07 00:00:00

</td><td>

Enable external integrations and in-platform applications to retrieve the eligible catalog-category tree hierarchy by using a REST endpoint.

</td></tr><tr><td>

Advanced Approval Management

</td><td>

2026-08-07 00:00:00

</td><td>

Show amount of time that has passed since an approval action was taken by approval users/groups in the approval card.

</td></tr><tr><td>

Flow Designer - Designer

</td><td>

2026-08-07 00:00:00

</td><td>

Rebranded UI for ServiceNow Otto.

</td></tr><tr><td>

ServiceNow Otto for CSM Major Issue Management

</td><td>

2026-08-07 00:00:00

</td><td>

Rename the app to Now Assist for CSM Major Issue Management.

</td></tr><tr><td>

IRM Compliance GenAI

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow OTTO Branding Updates: The IRM Compliance GenAI user interface now reflects ServiceNow's OTTO branding. All references to 'Now Assist' have been updated to 'OTTO' in UI labels, navigation, and help text.

</td></tr><tr><td>

Care Team Operations AI agent collection

</td><td>

2026-08-07 00:00:00

</td><td>

Fixed: Dependency and branding fixes.

</td></tr><tr><td>

Sales and Order Management for Telecommunications - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

ServiceNow Otto for Employee Center Pro

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

SPM Enterprise-Wide Deployment

</td><td>

2026-08-07 00:00:00

</td><td>

Resolved security vulnerabilities and minor defects.

</td></tr><tr><td>

ServiceNow Otto for Smart Assessment Engine

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto branding is now implemented across the Smart Assessment Engine \(SAE\) AI user interface. All customer-facing references to 'Now Assist' in SAE AI UI elements, labels, tooltips and images have been replaced with 'ServiceNow Otto'.

</td></tr><tr><td>

ServiceNow Otto for Enterprise Architecture \(EA\)

</td><td>

2026-08-07 00:00:00

</td><td>

Added support for linked text in Enterprise Architecture query agent responses. Selecting a linked record opens that record directly in Enterprise Architecture Workspace.

 Rebranded Now Assist to ServiceNow Otto. The product name Now Assist for Enterprise Architecture is updated to ServiceNow Otto for Enterprise Architecture as part of the rebranding initiative.

</td></tr><tr><td>

CMDB Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: Welcome to ServiceNow Otto, the new name for Now Assist!.
-   Support for 400% zoom in web browsers.

 Show dependency maps in Unified Map for specific Service Instance CI classes, instead of using service maps.

 -   Various CMDB Data Manager performance and quality issues.
-   Various Data Certification quality issues.
-   CMDB Workspace and CI Form quality issues.
-   Various internationalization issues.

</td></tr><tr><td>

Product Catalog Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Support multilanguage filtering for TMF-620 API.

</td></tr><tr><td>

Privacy Management Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: ServiceNow OTTO Branding Updates Updated the application to reflect ServiceNow's new OTTO branding, replacing Now Assist references for a consistent AI experience across the platform.

</td></tr><tr><td>

CSM - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Updated with the latest version of ServiceNow Otto Customer Service Management \(CSM\).

</td></tr><tr><td>

sn-itom-ui-internal

</td><td>

2026-08-07 00:00:00

</td><td>

Otto rebranding changes.

</td></tr><tr><td>

Hardware Asset Management

</td><td>

2026-08-07 00:00:00

</td><td>

Fixed: an issue with PLANNED\_ASSETS\_EXTENSION\_POINT API to ensure ACL rules are respected during planned asset candidate filtering on disposal orders.

</td></tr><tr><td>

Sales and Service API Core

</td><td>

2026-08-07 00:00:00

</td><td>

New: Not applicable.

 Change: Performance improvements.

</td></tr><tr><td>

Digital Integration Management

</td><td>

2026-08-07 00:00:00

</td><td>

Removed: a hardcoded platform\_host system ID from the EA credential-field UI policy condition. Credential fields on sn\_apm\_di\_credential now enforce read-only consistently across all customer instances, regardless of platform host.

</td></tr><tr><td>

AI Troubleshooting

</td><td>

2026-08-07 00:00:00

</td><td>

-   Troubleshoot setup issues for Now Assist in Virtual Agent, AI Search, and Now Assist skills in the Now Assist Admin console.
-   Set up proactive error monitoring to automate checks for execution errors and alert when acceptable threshold is crossed.
-   View actionable list of identified underlying issues for quick problem resolution.

</td></tr><tr><td>

AI Admin Center

</td><td>

2026-08-07 00:00:00

</td><td>

Generally available.

 New: public API \(script include\) exposes automation-opportunity data globally.

 New: Lit.JS user experience only \(selected users\).

 -   AI readiness: Single hub for all activation-ready skills and AI agents; filter by type, metrics with change indicators, activate, expand for details, re-run assessment.
-   Monitor tab: Cross-repo analytics in a new sidebar entry \(Overview, Performance Explorer, Business Value widgets\).
-   System property registry: Browse/search/filter AI properties by domain and editability; view details; edit eligible single-value and boolean properties in-UI with audit logging \(masked, multi-value excluded\).
-   Upgrade readiness pre-check: AI-specific impact report vs target releases - at-risk customizations, changed behaviors, deprecated features, new config options, with remediation and exports.
-   AI Agent Advisor: Create/edit custom data sets, define cost profiles, new views for OOTB agents and clusters, including step pages.
-   AI Search integrated into the discover flow.
-   Self-healing AI agent skill support added to AI Agent Advisor.
-   Automation opportunity backend wired into shared AI Readiness and Asset Inventory components for ready-to-activate.

 Otto rebranding: all Now Assist Center references updated to AI Admin Center.

 Lit.JS only \(selected users\).

 -   AI Optimization renamed to AI Readiness, with updated filters, components, and design across Health, Ready-to-Activate, Data Quality tabs.
-   Ready-to-Activate table refactored with snow-list.
-   Plan Upgrade adopts snow-list and August UI tweaks; category filter pills removed, sub-filter pills retained.
-   Customizations tab \(Upgrade Pre-Check\): Action-button nav to file details, more filters, breadcrumb mapping, better consistency.
-   Instance Health stream shows all inactive agents and OOTB skills ready to activate.
-   Data Quality tab adds an Estimated Effort column.
-   Localization standardized via aiux-services i18n.
-   Accessibility verified and fixed across all pages.
-   Typography tokens and rules established.
-   Snow-design-system components made Horizon 2.0-compliant on Home, Agent Advisor, Opportunity Detail.
-   Now Assist Admin refactored for Lit.JS/Horizon 2.0 - Model Mgmt/Versions, Experiences, Edit Model Providers, DT Languages.
-   Sidebar adopts latest karuna side-nav and top header \(navigation, logout, impersonate, scope-picker\).
-   'New version available' indicator added to the AI Readiness page.
-   Agent Advisor resolution steps and modal updates for OOTB agents.
-   AI Agent Advisor settings/list pages show updated timestamps, cost-profile fields, cluster mapping.
-   AI Readiness Overview tab adds graph components for Health, Data Quality, Ready-to-Activate metrics.
-   System Property Registry supports cross-scope edits with scope-aware, role-accurate UI.
-   Upgrade Pre-Check supports async run orchestration and per-file review.

 NAA KAA Auth dependency removed; Skills config now uses SkillConfig instead of the REST API.

 -   UI/stability: Blank-page loads, broken AI Solution page, dark theme, missing nav loaders, Otto Panel images, 'Loading Now Assist...' hang.
-   Navigation: Failing menu/workspace redirection and a broken Home 'View All' control.
-   AI Readiness/Instance Health: disabled Re-Run Assessment button, missing AI Solution count, skill-activation and rapid-action-card display issues.
-   Agent Advisor/Agent-Miner/Automation Opportunity: Page-load latency, missing Activate button for inactive configs, savings-projection count error, minor list/resolution defects.
-   Asset Inventory: Asset details not displaying and skill-type asset-page rendering.
-   Localization: Translation gaps and 5.1 localization warnings across Lit and UI Builder.
-   Access/roles: Updated nac\_user access on settings sub-pages; Agent-miner role scoping.

 Platform-app dependencies eliminated; platform apps now function independently.

 Pre-built automation workflows no longer accessible or visible.

</td></tr><tr><td>

Retail Core

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Added a plugin-gated 'In-Store Ops Tasks' tab to the RSM portal Home page and Cases and amp; Tasks page.

</td></tr><tr><td>

Standard ticket page summarization

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the ServiceNow Otto brand.

</td></tr><tr><td>

Sales and Order Management for Telecommunications - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

sn-task-planner

</td><td>

2026-08-07 00:00:00

</td><td>

-   View and manage connected tasks and stories inline in the Planner tab. Connected CWM tasks and stories display as child rows under each project task with standard fields, and are collapsible per project task. Inline editing is disabled for child tasks - edits can be made in the form view based on user permissions.
-   Use the toggle in PWS settings to show or hide connected tasks. The toggle is enabled by default, displaying all CWM and PWS tasks. Disable the toggle to hide connected tasks.

 A red indicator now appears on a project task row when a connected CWM child task's start or end date falls outside the parent task's date range, with a tooltip explaining the conflict. The indicator clears automatically when the dates are corrected.

</td></tr><tr><td>

Telecommunications Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Otto rebranding changes.

</td></tr><tr><td>

Knowledge Graph

</td><td>

2026-08-07 00:00:00

</td><td>

Graph query builder to traverse through Knowledge Graph.

</td></tr><tr><td>

ServiceNow Otto for Sales and Order Management for Telecommunications

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

Pipeline

</td><td>

2026-08-07 00:00:00

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

TSOM - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

sn-docs

</td><td>

2026-08-07 00:00:00

</td><td>

-   All references to Now Assist, Moveworks, and AI Experience in Docs have been renamed to ServiceNow Otto. The full name, ServiceNow Otto, is used in all customer-facing contexts except where UX character limits require shortening.
-   Artifact versions now render all content correctly, without requiring users to download or zoom out to view the full content.
-   Project Status Report in Project Workspace now maintains table width as expected.
-   Exported PDF documents in Project Workspace no longer truncate issues in portrait orientation.

</td></tr><tr><td>

Cryptographic Asset Compliance

</td><td>

2026-08-07 00:00:00

</td><td>

-   Centralized cryptographic asset visibility: Assess the quantum safety of your certificates and cloud keys \(AWS KMS and Azure Key Vault\) discovered across on-premises and cloud environments from a centralized inventory, giving you a unified view of your organization's quantum safety posture.
-   Policy-based risk indicators: Identify at-risk cryptographic assets, including risks like outdated algorithms, untrusted certificate authorities, and expiring certificates, helping you focus remediation efforts where they matter most.
-   Post-quantum cryptography \(PQC\) compliance and quantum vulnerability dashboards: Track PQC compliance status and quantum vulnerability through purpose-built dashboards. For example, certificates using RSA are automatically tagged as quantum-vulnerable, enabling data-driven migration planning toward quantum-resistant algorithms.
-   Dependency graph for impact analysis: Visualize where each cryptographic asset is used across your environment with an interactive dependency graph and assess downstream impact before initiating migration, reducing the risk of service disruption.
-   AI-driven analysis and recommendations: Get AI-generated insights for each identified cryptographic asset, including recommended next steps to guide remediation and migration planning.

</td></tr><tr><td>

Security Incident Response Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Users can now preview attachments in a configurable upload modal before completing the upload process.

 -   Translations now display correctly on Quick filters in Security Incident Workspace.
-   Heading levels in Security Incident Response are now sequential, improving accessibility and screen reader compatibility.
-   The relationship graph in Security Incident Workspace now supports localization and displays translated content.
-   Users can now close security incidents from the closure modal, even when the active tab is not the details tab.

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: Use ServiceNow AI Lens from your browser to upload one or more files for AI Lens to analyze and auto-fill form fields - no installation required.
-   Use Lens as a Service to map the data from multiple related Excel column headers and values to a single ServiceNow table field.
-   Use Lens as a Service to auto-map an Excel column header and its values from a single Excel sheet to multiple ServiceNow table fields simultaneously.
-   Choose how AI Lens opens when you start a session - from your browser or the desktop application. You can update this preference at any time.

 Updated the AI experience branding in AI Lens to align with ServiceNow Otto naming and visual guidelines.

</td></tr><tr><td>

ServiceNow Otto for Process Mining

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: the default NowLLM provider to a 3p model provider\(Amazon bedrock\)- Unable to Edit without creator role issue- Made GenAI Skill access rules customizable- Move GenAI skills to platform.

</td></tr><tr><td>

TSOM - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

ServiceNow Otto for Telecommunications Service Management

</td><td>

2026-08-07 00:00:00

</td><td>

Otto Rebranding.

</td></tr><tr><td>

AI Agents for AIOps

</td><td>

2026-08-07 00:00:00

</td><td>

--- AI Generated Release Notes ---.

 -   Operator-reopened alerts get full AI investigation automatically. When a human operator reopens an alert that the AI previously closed as noise, the system bypasses noise classification for the rest of that alert's lifecycle and runs a complete investigation - ensuring human overrides are respected and learned from.
-   ServiceNow Otto for ITOM branding is now applied. The Now Assist for ITOM app has been renamed to ServiceNow Otto for ITOM throughout the application.
-   AI Specialist alert reassignment behavior has been enhanced. When the AI Specialist completes investigation or remediation on an alert originally assigned to a human operator, the alert is automatically reassigned back to the original owner, unless the alert was closed as noise or manually reassigned during AI processing. Audit trails and work notes reflect the reassignment, and configuration options allow admins to enable or disable this behavior.
-   Automatic triggering of AI Specialist on assigned alerts is now configurable. By default, the AI Specialist does not take over alerts already assigned to a human operator. This condition can be edited by admins if needed.
-   Manual triggering of AI Specialist now preserves alert ownership. When the AI Specialist is manually triggered on an alert assigned to a human operator, the alert is reassigned back to the operator at the end of execution. Feature flags control whether noisy alerts or previously assigned alerts are reassigned.
-   Alert closure by AI now records closure reason for downstream processing. When the AI auto-closes an alert, a durable marker is recorded indicating the closure was AI-driven, enabling correct handling on future reopen events.
-   Operator override flag and additional alert lifecycle data are now stored durably. A new JSON field on the AI session record captures operator overrides and other lifecycle facts, supporting robust reopen and investigation workflows.

 The Alert Investigation 'Related Changes' flow no longer causes excessive memory usage or out-of-memory errors that could lead to node restarts. The system now handles related changes efficiently during alert investigation.

</td></tr><tr><td>

DCNAM - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

AI Agents for Telecommunications, Media and Technology

</td><td>

2026-08-07 00:00:00

</td><td>

Otto Rebranding Changes.

</td></tr><tr><td>

TNI - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

ITSM - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

-   AI can now automatically complete Change Risk Assessment and Dynamic Schema questions based on the change record's context, showing its reasoning for each answer so admins and change managers can verify or correct it. Answers that identify compliance exposure \(for example SOX, PCI-DSS, or HIPAA\) automatically populate the matching Dynamic Schema fields.
-   A new Teams-native AI agent lets shift agents manage on-call coverage directly in chat - requesting coverage or leave, and asking questions like 'who is on call' or 'when is my next shift.'.
-   Employees creating a ticket in Service Portal now see an AI-generated suggestion - drawn from relevant knowledge articles and catalog items - before they submit, based on the ticket description and their hardware, location, and department.
-   Now Assist, Moveworks, and 'AI Experience' branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
-   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
-   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
-   The DEX Diagnosis AI agent now factors in event monitoring logs and statistical anomaly signals alongside existing telemetry for more accurate root-cause diagnoses, and now surfaces the specific evidence behind each conclusion.
-   Fixed: an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
-   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
-   Fixed: an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
-   Fixed: a date-formatting issue in the Change Outage Assistant AI agent.
-   Fixed: an issue where the incident investigation and resolution workflow could fail with an 'incident search/read service unavailable' error.
-   Fixed: an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
-   Improved the error message shown for the Resolution Notes generation skill when the 'display in product desktop' setting is turned off.
-   Reduced processing time for the Generate Change Request Plans AI flow, which had been taking an unusually long time to complete.
-   Fixed: an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform.
-   Fixed: an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users.
-   Fixed: an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own.

 No items removed in this release.

</td></tr><tr><td>

FSM - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Fluent based development support added.

 ServiceNow Otto is the new Al experience brand. This change is reflected in the name of ServiceNow products, including Field Service Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

TNI and DCNAM AI Content Collection

</td><td>

2026-08-07 00:00:00

</td><td>

Maintenance release - dependency updates only; no new customer-facing functionality in this version.

</td></tr><tr><td>

ITSM - Foundation

</td><td>

2026-08-07 00:00:00

</td><td>

Employees creating a ticket in Service Portal now see an AI-generated suggestion - drawn from relevant knowledge articles and catalog items - before they submit, based on the ticket description and their hardware, location, and department.

 -   Now Assist, Moveworks, and 'AI Experience' branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
-   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
-   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
-   Fixed: an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
-   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
-   Fixed: an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
-   Fixed: an issue where the incident investigation and resolution workflow could fail with an 'incident search/read service unavailable' error.
-   Fixed: an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
-   Improved the error message shown for the Resolution Notes generation skill when the 'display in product desktop' setting is turned off.
-   Fixed: an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform.
-   Fixed: an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users.
-   Fixed: an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own.

 No items removed in this release.

</td></tr><tr><td>

ServiceNow Otto for Privacy Management

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: ServiceNow OTTO Branding Updates Updated the application to reflect ServiceNow's new OTTO branding, replacing Now Assist references for a consistent AI experience across the platform.

</td></tr><tr><td>

Conversational Catalog Requests

</td><td>

2026-08-07 00:00:00

</td><td>

New: Minor enhancements.

 Fixed: Minor defects.

</td></tr><tr><td>

ITSM - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

-   AI can now automatically complete Change Risk Assessment and Dynamic Schema questions based on the change record's context, showing its reasoning for each answer so admins and change managers can verify or correct it. Answers that identify compliance exposure \(for example SOX, PCI-DSS, or HIPAA\) automatically populate the matching Dynamic Schema fields.
-   A new AI agent can diagnose and resolve common Okta account lockouts and MFA failures reported through an incident or self-service, checking live account status and submitting the correct unlock or reset request automatically.
-   A new Teams-native AI agent lets shift agents manage on-call coverage directly in chat - requesting coverage or leave, and asking questions like 'who is on call' or 'when is my next shift.'.
-   Employees creating a ticket in Service Portal now see an AI-generated suggestion - drawn from relevant knowledge articles and catalog items - before they submit, based on the ticket description and their hardware, location, and department.
-   Now Assist, Moveworks, and 'AI Experience' branding has been renamed to ServiceNow Otto across in-product labels, icons, tooltips, and documentation.
-   Incident Managers can now drill from any indicator on the Insights and Opportunities dashboard directly into the underlying incident records without losing their place on the dashboard.
-   A new dashboard section shows how closely AI-proposed solutions in Copilot \(supervised\) mode matched what human agents ultimately implemented.
-   The employee consent experience for remedial actions is more consistent and accurate: duplicate requests are no longer triggered for already-approved or declined actions, and messaging now notes when a device needs to stay online.
-   The DEX Diagnosis AI agent now factors in event monitoring logs and statistical anomaly signals alongside existing telemetry for more accurate root-cause diagnoses, and now surfaces the specific evidence behind each conclusion.
-   Fixed: an issue where the summarize capability could produce an irrelevant summary on requested items with many related records.
-   Fixed: an issue where several AI agents \(including Zscaler, Installed Apps, and Modern Change agents\) had read-only configuration, preventing customers from disabling them.
-   Fixed: an issue where the Zscaler and Installed Apps agents' action engagement tools showed an empty timeout field.
-   Corrected a remaining reference to the previous Now Assist branding that had been missed during the ServiceNow Otto rename.
-   Fixed: an issue on the Insights and Opportunities dashboard where assigning an incident to a cluster could fail and prevent clustering from completing.
-   Fixed: a date-formatting issue in the Change Outage Assistant AI agent.
-   Fixed: an issue where the incident investigation and resolution workflow could fail with an 'incident search/read service unavailable' error.
-   Fixed: an issue where the knowledge-article search filters used by the Create Incident AI agent were not being applied correctly.
-   Reordered the metrics on the Copilot Performance dashboard so the '80% or higher similarity' metric appears first.
-   Improved the error message shown for the Resolution Notes generation skill when the 'display in product desktop' setting is turned off.
-   Reduced processing time for the Generate Change Request Plans AI flow, which had been taking an unusually long time to complete.
-   Fixed: an issue where built-in ITSM AI agents were unintentionally discoverable and visible within the Now Assist Platform.
-   Fixed: an issue where a required role was missing from the Link Major Incident agent's flow, which could prevent the agent from working as expected for some users.
-   Fixed: an issue where the Triage and Categorize AI agent could assign an irrelevant, caller-owned device as the configuration item when the matched service offering had no related configuration items of its own.

 No items removed in this release.

</td></tr><tr><td>

AI Agents for ITAM

</td><td>

2026-08-07 00:00:00

</td><td>

Hardware Asset Workspace and Software Asset Workspace now feature ServiceNow Otto, replacing all previous references to Now Assist.

</td></tr><tr><td>

ServiceNow Otto for Automation Center

</td><td>

2026-08-07 00:00:00

</td><td>

-   ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Automation Center. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   The Now Assist for Automation Center plugin is now renamed to ServiceNow Otto for Automation Center.

</td></tr><tr><td>

FSM - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Fluent based development support added.

 ServiceNow Otto is the new Al experience brand. This change is reflected in the name of ServiceNow products, including Field Service Management. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

ServiceNow Otto for CPQ

</td><td>

2026-08-07 00:00:00

</td><td>

1. App dependency for sn\_cpq\_cfg\_ai\_a2a2. Support enforced for min glide version of Australia Patch 2 and Zurich Patch 10 respectively.

</td></tr><tr><td>

ITOM Guided Setup - New

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist and gt; ServiceNow Otto announcement.

 Now Assist introduced AI on the platform. As that experience has evolved, there's a new name for the experience. ServiceNow Otto is the conversational AI platform integrated into ServiceNow workflows. It provides agentic capabilities, supports multimodal interactions across web, mobile, and messaging channels, and enables autonomous orchestration for cross-system workflows.

</td></tr><tr><td>

ServiceNow IDE

</td><td>

2026-08-07 00:00:00

</td><td>

-   New: Use ServiceNow IDE capabilities within ServiceNow Studio to create apps in source code. Use the new Explorer tab to open Fluent files and see underlying Fluent source code.
-   Upgrade to the new version of source control in ServiceNow Studio to access more features, such as additional Git commands.

 ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including ServiceNow Studio. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

</td></tr><tr><td>

Service Operations Workspace Integrations launchpad UI

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated ServiceNow Otto branding for HLA data inputs integrations.

</td></tr><tr><td>

Service Operations Workspace Express List App

</td><td>

2026-08-07 00:00:00

</td><td>

-   Express list now supports color-coded visual cues to highlight values \(based on existing definitions in sys\_highlighted\_value\). Admins can configure conditional formatting rules on alert columns \(e.g., severity, priority\) so that critical items are immediately visible through colored indicators and icons - no more scanning through uniform rows.
-   Azure Monitor Issues now surface related alerts in context. A new 'Related Records' tab appears directly in the alert view for Azure Monitor Issues, letting operators drill into associated alerts without leaving their current workflow.
-   Express List now fully supports right-to-left languages, including Arabic and Hebrew, with correct mirroring of layout, icons, and spacing.
-   All 'Now Assist' references across Service Operations Workspace, Express List, etc. have been rebranded to ServiceNow Otto.
-   The 'Probable Cause' tab in the Alerts Preview panel is now called 'Related Records' and includes Azure Monitor Issues.

 Express List no longer fails to load when a system property record has a missing type value.

</td></tr><tr><td>

ServiceNow Otto for Hardware Asset Management

</td><td>

2026-08-07 00:00:00

</td><td>

This release rebrands Now Assist to ServiceNow Otto. Previous references to Now Assist inside Hardware Asset Workspace have been replaced with new verbiage.

</td></tr><tr><td>

Core Business Suite for Legal

</td><td>

2026-08-07 00:00:00

</td><td>

Shipped out-of-the-box Legal knowledge base.

 Owners and managers can be defined by the admin for the knowledge base in the Core Business Suite configuration console to ensure proper governance and content tracking.

 Shipped Now Assist search sources for Legal for Knowledge article generation from legal case table on Knowledge center.

 Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

Service Level Management Experience for Workspace

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

AI Agent Advisor

</td><td>

2026-08-07 00:00:00

</td><td>

New: Recommend out-of-the-box agents alongside top problems - AI Agent Advisor now surfaces recommended ServiceNow AI Agents directly alongside discovered opportunities in the same view.

-   Pre-generate agents for recommendations in AI Agent Studio and AI Admin Center \(formerly Now Assist Center\) - Agents are pre-generated for matched recommendations, reducing time to creation from Agent Studio and AI Admin Center.
-   Surface AI Agent Advisor recommendations as insights in AI Control Tower - Automation opportunities discovered by AI Agent Advisor are now visible as insights within AI Control Tower.
-   Mining custom tables and fields - AI Agent Advisor can now analyze custom tables and fields, expanding opportunity discovery beyond standard incident and case data.Changed
-   Minor updates to UI - Removed the summary bar on list view, updated the list view columns and list view filtering.

 Fixed: No major defect fixes.

 Removed: Nothing major removed in this release.

</td></tr><tr><td>

ServiceNow Otto for Legal Service Delivery

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: ServiceNow Otto is the new AI experience brand. Now Assist for Legal Service Delivery is ServiceNow Otto for Legal Service Delivery.

 The ServiceNow Otto panel now starts a single chat session for a legal request record instead of opening multiple concurrent sessions.

</td></tr><tr><td>

Core Business Suite Prime for Legal

</td><td>

2026-08-07 00:00:00

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Service Operations Workspace ITSM Advanced Applications

</td><td>

2026-08-07 00:00:00

</td><td>

Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.

</td></tr><tr><td>

ServiceNow Otto for App Engine

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated to support the ServiceNow Otto brand.

</td></tr><tr><td>

ServiceNow Otto for Order Management

</td><td>

2026-08-07 00:00:00

</td><td>

ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including Now Assist for Order Management. Your product entitlements remain unchanged. There is no change to functionality or existing customer configurations.

</td></tr><tr><td>

Field Service Mobile

</td><td>

2026-08-07 00:00:00

</td><td>

Security patch.

</td></tr><tr><td>

LEAP

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Now Assist is renamed to 'ServiceNow Otto'.

</td></tr><tr><td>

Dynamic Guidance

</td><td>

2026-08-07 00:00:00

</td><td>

-   Integrated oneextend-gen-ai APIs to handle transcript storage, knowledge base retrieval, and connection initialization.
-   This update ensures all three core operations now use the consolidated API layer for consistency and maintainability.

</td></tr><tr><td>

Payment Card

</td><td>

2026-08-07 00:00:00

</td><td>

Changed: Updated internal application components to support ongoing platform enhancements.

</td></tr><tr><td>

Core Business Suite Foundation for Legal

</td><td>

2026-08-07 00:00:00

</td><td>

Shipped out-of-the-box Legal knowledge base.

 Owners and managers can be defined by the admin for the knowledge base in the Core Business Suite configuration console to ensure proper governance and content tracking.

 Shipped Now Assist search sources for Legal for Knowledge article generation from legal case table on Knowledge center.

 Create contextually relevant articles from case tables and drive better AI-assisted content creation by enabling Knowledge Content Recommendation skill from AI skills module.

</td></tr><tr><td>

Finance and Procurement - Prime

</td><td>

2026-08-07 00:00:00

</td><td>

Updated the plugin name and details to Finance and Procurement - Prime.

</td></tr><tr><td>

ServiceNow Otto for Zero Copy Connector

</td><td>

2026-08-07 00:00:00

</td><td>

Name changes from Now Assist to Otto for Zero Copy Connector.

 Defect fixing.

</td></tr><tr><td>

ITOM - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

-   Cryptographic Asset Compliance Centralized cryptographic asset visibility: Assess the quantum safety of your certificates and cloud keys \(AWS KMS and Azure Key Vault\) discovered across on-premises and cloud environments from a centralized inventory, giving you a unified view of your organization's quantum safety posture.
-   Policy-based risk indicators: Identify at-risk cryptographic assets, including risks like outdated algorithms, untrusted certificate authorities, and expiring certificates, helping you focus remediation efforts where they matter most.
-   Post-quantum cryptography \(PQC\) compliance and quantum vulnerability dashboards: Track PQC compliance status and quantum vulnerability through purpose-built dashboards. For example, certificates using RSA are automatically tagged as quantum-vulnerable, enabling data-driven migration planning toward quantum-resistant algorithms.
-   Dependency graph for impact analysis: Visualize where each cryptographic asset is used across your environment with an interactive dependency graph and assess downstream impact before initiating migration, reducing the risk of service disruption.
-   AI-driven analysis and recommendations: Get AI-generated insights for each identified cryptographic asset, including recommended next steps to guide remediation and migration planning.

 Extend alert analysis capabilities with the Azure Monitor MCP Agent and Gemini Cloud Assist A2A Investigation Agent in the analyze alert impact agentic workflow.

 AI Agents for Service Level Objective ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI agents for SLO. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 -   ServiceNow Otto is the new AI experience brand. This name change is reflected in ServiceNow products, including ITOM AI Agents For Service Mapping. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.
-   The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.

 ServiceNow Otto is the new AI experience brand. This change is reflected in the name of ServiceNow products, including AI agents for Observability. Your product entitlements remain unchanged. Check your entitlements to determine your access to specific features.

 Now Assist is renamed to ServiceNow Otto. All references to Now Assist are renamed and relevant images updated.

 ITOM URL Discovery: You can now add one or more URLs to targeted discovery from the Other URLs tab and the domain details page in the ITOM URL Discovery for SAM dashboard without receiving an error.

</td></tr><tr><td>

Service Operations Workspace ITOM Apps

</td><td>

2026-08-07 00:00:00

</td><td>

-   AI value is now visible on the AIOps 360 dashboard. A new widget shows estimated time saved based on how many alerts were resolved and analyzed by AI, giving operations teams a real-time view of AI's impact on their workload.
-   Alerts Express List now supports color-coded visual cues to highlight values \(based on existing definitions in sys\_highlighted\_value\). Admins can configure conditional formatting rules on alert columns \(e.g., severity, priority\) so that critical items are immediately visible through colored indicators and icons - no more scanning through uniform rows.
-   Azure Monitor Issues now surface related alerts in context. A new 'Related Records' tab appears directly in the alert view for Azure Monitor Issues, letting operators drill into associated alerts without leaving their current workflow. Azure Monitor Issues are now bi-directionally synchronized with ServiceNow. The integration supports real-time ingestion of Azure Monitor Issues via webhook and polling, with two-way synchronization of status, severity, title, description, and AI-generated insights. OAuth 2.0 and multi-tenant Azure environments are supported.

 Dynatrace Gen3 event payloads are now supported in the event push connector, alongside legacy formats - no migration required.

 -   Express List now fully supports right-to-left languages, including Arabic and Hebrew, with correct mirroring of layout, icons, and spacing.
-   All 'Now Assist' references across Service Operations Workspace, Express List, Integration Launchpad, and the AIOps AI Specialist onboarding have been rebranded to ServiceNow Otto.
-   The Probable Cause tab in the Alerts Preview panel is now called 'Related Records' and includes Azure Monitor Issues.
-   The Dynatrace Gen3 payload processor now handles both workflow-wrapped and raw Davis Gen3 payloads consistently, with improved severity mapping and entity tag preservation.
-   Alert automation no longer hangs when the interface language is set to Portuguese.
-   The AIOps Supervisor Homepage remains responsive when managing a large number of teammates.
-   Express List no longer fails to load when a system property record has a missing type value.

</td></tr><tr><td>

AI agents for SLO

</td><td>

2026-08-07 00:00:00

</td><td>

All customer-facing references to 'Now Assist' have been updated to 'ServiceNow Otto' throughout the interface, documentation, and support materials. The product functionality remains the same, but you will see the ServiceNow Otto name and branding everywhere you interact with your AI agent.

</td></tr><tr><td>

ServiceNow Otto for Finance and Procurement

</td><td>

2026-08-07 00:00:00

</td><td>

Now Assist has been renamed to ServiceNow Otto, ServiceNow's AI experience brand. As a result, Now Assist for FSC Common is now ServiceNow Otto for Finance and Procurement.

</td></tr><tr><td>

CSM - Advanced

</td><td>

2026-08-07 00:00:00

</td><td>

Updated with the latest version of ServiceNow Otto Customer Service Management \(CSM\).

</td></tr><tr><td>

Third-party Risk Due Diligence

</td><td>

2026-08-07 00:00:00

</td><td>

-   Rebranded to ServiceNow Otto, replacing Now Assist references for a consistent AI experience.
-   Enhanced MRA authorization validation to ensure access checks are consistently enforced during record association.

</td></tr><tr><td>

Third-party Risk Management

</td><td>

2026-08-07 00:00:00

</td><td>

Rebranded to ServiceNow Otto, replacing Now Assist references for a consistent AI experience.

 Addressed Arbitrary GlideRecord read in VendorRiskAsmtAjax security issue \[PRB1997560\].

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|Financial Services Document Management|1.3.1|2022-02-03|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Zoom extension for Omnichannel Callback|1.3.6|2025-07-31|
|HR Service Delivery Portal UI Components|1.0.5|2024-05-09|
|ITOM Line chart|27.1.1|2026-03-12|
|Impact Value Management - CSM|2.1.0|2025-01-30|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|HR Service Delivery Integration with Ultimate Kronos Group|2.0.6|2024-06-06|
|Cisco Webex Meetings Spoke|2.3.3|2024-08-01|
|Vulnerability Response Integration with NVD|1.7.2|2025-07-31|
|Document Template integration with DocuSign|1.7.1|2026-03-12|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Impact Value Management - HR|4.0.0|2026-06-16|
|Financial Services Document Management|1.3.1|2022-02-03|
|Impact Value Management - APM|2.1.0|2025-01-30|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|COVID-19 Global Health Data Set|1.20.3|2024-05-09|
|Vulnerability Response Integration with Agile Management|1.2.2|2025-07-31|
|Vulnerability Response Integration with CISA|1.5.1|2025-07-31|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Zendesk Spoke|1.8.0|2025-11-06|
|Investment Funding|1.1.1|2024-05-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|CCO Dashboard|2.0.8|2025-12-11|
|Jira Spoke|6.0.1|2026-04-09|
|Impact Value Management - App Engine|2.1.0|2025-01-30|
|Impact Value Management - SECOPS|3.0.3|2025-12-11|
|ServiceNow Otto in Document Management|4.0.8|2026-08-13|
|Bubble trend|1.0.0|2025-05-01|
|Order Management Portal|2.1.0|2025-07-31|
|sn-nlq-analytics|29.0.1|2026-03-12|
|Qualtrics Spoke|1.3.0|2025-11-06|
|Infoblox Spoke|2.0.4|2024-03-20|
|Digital Product Release Workspace|2.3.0|2025-12-11|
|Microsoft Dynamics 365 Spoke|1.1.0|2025-07-31|
|FSO - Advanced|1.0.0|2026-04-09|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Lucidchart Diagramming Spoke|1.1.1|2024-01-04|
|Enterprise Asset Management for Facilities|1.0.0|2024-08-01|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Export to PowerPoint for Application Portfolio Management|1.0.1|2024-02-01|
|Service Graph Connector Support Tools|1.0.0|2024-02-01|
|SurveyMonkey Spoke|2.0.6|2024-08-01|
|Issue Auto Resolution for HR|4.0.3|2024-06-06|
|CRO Dashboard|2.0.10|2025-12-11|
|Impact Value Management - IRM|3.0.3|2025-12-11|
|Adobe Sign Spoke|2.7.2|2025-10-16|
|Impact Value Management - SPM|3.0.1|2025-12-11|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Workplace from Facebook Spoke|4.2.1|2025-11-06|
|Dropbox Business Spoke|1.0.5|2024-03-07|
|Financial Services Document Management|1.3.1|2022-02-03|
|User Experience Analytics API|3.1.2|2024-02-01|
|Document Service Framework for Google Drive|3.0.0|2025-07-31|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|Oracle Peoplesoft Financial Spoke|1.1.0|2024-03-07|
|Agent Client Collector Spoke|1.1.5|2024-01-04|
|Employee Center for Microsoft Viva Connections|2.0.8|2025-07-31|
|Customer Request for Quote|1.0.0|2025-12-11|
|Workfront Spoke|1.3.0|2025-11-06|
|Impact Value Management - ITOM|3.0.1|2025-12-11|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Field Service Virtual Agent Conversations|1.7.0|2025-07-31|
|Roadmunk Spoke|1.6.5|2024-07-11|
|Microsoft Azure Sentinel Incident Ingestion Integration For Security Operations|11.2.3|2026-05-05|
|Access Management Automation|2.1.0|2023-12-07|
|Product Capability Core|2.2.2|2026-07-09|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|sn-dashboards-view|29.0.1|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Engagement dashboard for AI Control Tower|3.0.11|2025-12-12|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Incident Management for Field Service|1.1.1|2025-01-02|
|GRC Compliance Case Management Advanced|18.1.1|2024-06-06|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Google Meet Spoke|1.2.1|2025-11-06|
|Log Export Service|3.2.0|2025-05-01|
|Microsoft Azure DevOps Pipelines Spoke|1.0.0|2023-08-03|
|Microsoft Integrations - Core|5.8.1|2025-12-11|
|Customer Service Case Action Status|2.0.2|2026-06-16|
|Operational Technology Incident Management|4.0.0|2026-06-16|
|Attribute Pack|5.0.0|2025-07-31|
|sn-app-par-components-create-indicator-modal|8.4.3|2026-07-09|
|sn-viz-designer|8.4.1|2026-07-09|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Strategic Spend Tracking for PPM|1.2.0|2025-12-11|
|AES Mobile Wizards|28.2.1|2025-12-11|
|Advanced Work Assignment for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|DevOps Insights|7.0.0|2026-06-16|
|@devsnc/sn-feedback|2.0.0|2025-12-11|
|ER integration with NAVEX|1.1.1|2024-02-01|
|Threat Intelligence Security Center integration with WHOIS|5.0.4|2025-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|ServiceNow ITOM/OT SU Licensing|3.13.1|2026-07-09|
|Supplier Case Management|11.0.4|2026-07-09|
|Hiring Connector|7.0.0|2025-12-11|
|Parallel Review and Feedback|21.1.0|2025-12-11|
|External Legal Service Center|1.2.0|2025-12-11|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|AES Flow Templates|28.2.1|2025-12-11|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Browser Extension for Employee Center|1.1.1|2025-12-11|
|Planned Task Common|1.1.0|2025-12-11|
|Legal Simple Compliance|1.1.0|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Application Common Configuration|29.0.8|2026-03-12|
|Enterprise Asset Management Advanced|1.0.0|2026-04-09|
|Trello Spoke|1.4.0|2025-11-06|
|Workplace Agent for mobile|1.4.5|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|Health and Safety Incident Management PA Content Pack|10.1.1|2026-07-09|
|Performance Analytics Content Pack for Essential SAFe|1.4.2|2023-09-20|
|Health dashboard for AI Control Tower|3.0.11|2025-12-12|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Impact Value Management - APM|2.1.0|2025-01-30|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|sn-app-par-components-config-panel|8.4.3|2026-07-09|
|Workday Financials Spoke|2.1.0|2025-07-31|
|Talent profile|7.0.1|2026-07-09|
|Basic Scoring for Smart Assessments|22.3.0|2026-06-16|
|Group Life Underwriting|2.5.0|2026-03-12|
|GRC: Mobile|18.0.0|2024-02-01|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|DevOps Workspace|7.0.0|2026-06-16|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Enterprise Portfolio|1.3.0|2025-12-11|
|Work Progress Status for Agile Teams|1.0.4|2025-06-05|
|Jack Henry jXchange Spoke|2.1.0|2025-07-31|
|Healthcare Operations Core|2.3.0|2026-03-12|
|Hiring tab|8.0.1|2026-07-09|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|App Summary|29.4.0|2026-07-09|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|Vulnerability Response Licensing and Usage|2.9.1|2026-01-20|
|sn-dashboards-view|29.0.1|2026-03-12|
|CPQ - Foundation|1.0.1|2026-04-09|
|Customer Success Advanced|2.4.10|2026-07-09|
|Now Assist for Playbook|28.0.1|2025-12-11|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|Process Automation Content|28.1.4|2025-09-10|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Oracle Autonomous DB Spoke|1.0.6|2022-12-01|
|sn-app-par-components-share-info|8.4.3|2026-07-09|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Microsoft Intune Spoke|1.2.0|2025-11-06|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Credentials Core|1.2.0|2026-06-16|
|Workforce Optimization Configurable Workspace UI Components|4.4.1|2025-12-11|
|Insurance claims|1.2.2|2026-03-12|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|On-Call UI Components for Configurable Workspaces|9.2.0|2026-06-16|
|GitHub Spoke|3.5.1|2026-01-20|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|AWS Lambda Spoke|1.1.3|2023-09-07|
|sn-app-par-components-export-email-composer|8.4.3|2026-07-09|
|Credly Spoke|1.1.0|2026-06-16|
|sn-nlq-analytics|29.0.1|2026-03-12|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Metric Intelligence|2.7.11|2025-12-11|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Group Life Underwriting|2.5.0|2026-03-12|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Planned Maintenance Management|2.14.0|2026-06-16|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|ArcSight ESM Event Ingestion for Security Operations|10.5.0|2025-12-11|
|Event Inquiry|1.4.0|2025-07-31|
|@devsnc/library-uibtk-ux-value-resolver|29.1.71|2026-03-12|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|GC Dashboard|2.0.5|2025-12-11|
|Gmail Spoke|1.3.3|2025-12-11|
|sn-nlq-analytics|29.0.1|2026-03-12|
|Personal Lines Claims|4.4.0|2026-03-12|
|UKG Spoke|3.5.0|2025-12-11|
|Workplace Service Delivery integration with Microsoft Places|1.2.5|2025-12-11|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Technician driven sales with Field Service|29.1.2|2026-03-12|
|Admin Experience Framework|5.3.0|2026-03-12|
|Microsoft SharePoint File Explorer Connector for Security Incident Response integration|1.3.0|2025-12-11|
|AI Agents Platform Usecase|1.0.5|2025-03-12|
|External Content Connectors GitHub Enterprise Cloud|7.0.7|2026-05-28|
|Basic Scoring for Smart Assessments|22.3.0|2026-06-16|
|Product Inventory Advanced|14.0.1|2026-06-16|
|Service Operations Workspace Service Reliability Management \(SRM\) Common|7.0.0|2026-06-16|
|Data Context Engine|3.3.2|2026-06-16|
|Compatibility Management|6.6.0|2026-06-16|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|sn-uxf-formula-parser|29.1.0|2026-03-12|
|sn-app-par-nacm-component|8.4.3|2026-07-09|
|Google Cloud DNS Spoke|1.0.2|2022-09-01|
|@servicenow/sn-cb-events-navigator|27.2.29|2025-05-01|
|MS Teams Activities for PAD|1.0.3|2023-01-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Operational Technology Incident Management|4.0.0|2026-06-16|
|Slack Spoke|1.8.0|2025-09-10|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Amazon EBS Spoke|1.0.2|2023-09-20|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|@devsnc/sn-uibtk-site-map|29.1.71|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Work Progress Status for SAFe|1.0.4|2025-06-05|
|Customer Service Case Types|4.4.2|2026-07-20|
|Telecom Core|6.6.2|2026-07-09|
|Individual Life Servicing|2.5.0|2026-03-12|
|GRC: Risk Management Workspace|21.1.1|2025-12-11|
|Card data security|1.0.1|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Password Reset UI components for Configurable Workspaces|9.2.0|2026-06-16|
|sn-app-kpi-details|8.0.1|2026-03-12|
|Health and Safety Components|12.1.2|2026-07-09|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|AI agents for Synthetic Monitoring|1.4.4|2026-07-09|
|SPM Benchmarking|1.0.0|2022-11-03|
|Threat Intelligence Security Center integration with Splunk Search|3.0.5|2025-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Vulnerability Response Integration Framework|1.3.0|2026-01-20|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|@devsnc/sn-devops-pipeline|21.0.5|2022-08-04|
|Oracle HCM Cloud Spoke|4.3.0|2025-12-11|
|Digital Signature API|26.0.0|2024-08-01|
|Order Management Portal|2.1.0|2025-07-31|
|Atlassian Jira Integration for Agile Development|2.3.2|2025-12-23|
|Email Interaction for CSM|1.5.0|2025-12-11|
|Procurement File Transfer Framework|2.2.2|2023-05-04|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Guided Decisions|38.0.2|2025-12-11|
|Recruiter Workspace|8.0.1|2026-07-09|
|Supplier Relationship and Performance Management|10.0.0|2026-06-16|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Advanced Recommended actions for ITSM|8.1.0|2025-09-10|
|HR Service Delivery for Healthcare|1.0.4|2025-05-01|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|Human Resources Service Delivery Integration with Workday Learning|1.4.0|2025-07-31|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Document Management|1.3.1|2022-02-03|
|Performance Analytics for Configuration Compliance|1.5.2|2025-12-11|
|Procurement for Field Service|3.0.0|2026-03-12|
|SmartRecruiters Spoke|1.0.0|2021-11-18|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Service Graph Connector Dependencies|1.0.0|2021-01-21|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Conversational IVR with Amazon Connect|1.6.3|2025-07-31|
|GRC: Entity Based Access|21.1.4|2025-12-11|
|Access Management Flow Wizards|1.0.1|2021-09-16|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|Subscription Management v2|6.4.3|2026-06-16|
|Ansible Spoke|2.2.9|2024-12-05|
|sn-app-par-components-dashboard-categories|8.4.3|2026-07-09|
|sn-nlq-analytics|29.0.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Financial Services Document Management|1.3.1|2022-02-03|
|Individual Life Servicing|2.5.0|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|@devsnc/sn-interaction-builder|29.1.37|2026-03-12|
|Product Configurator|1.0.1|2024-11-07|
|@devsnc/sn-uibtk-diff-renderer|29.1.71|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|F5 BIG-IP Spoke|1.3.0|2025-09-10|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|sn-nlq-analytics|29.0.1|2026-03-12|
|Insurance claims|1.2.2|2026-03-12|
|Customer Contracts and Entitlements|13.1.0|2026-02-05|
|Data Relationships Framework|11.0.0|2026-06-16|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Financial Services Document Management|1.3.1|2022-02-03|
|@servicenow/sn-cb-property-navigator|27.2.29|2025-05-01|
|Related party|1.0.6|2023-02-02|
|GRC Case Management Core|22.3.3|2026-06-16|
|CrowdStrike Spoke|1.1.0|2025-01-30|
|@devsnc/sn-uibtk-element-navigator|29.1.71|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Impact Value Management - IRM|3.0.3|2025-12-11|
|Miro Spoke|3.3.1|2025-12-11|
|Visibility Content|6.32.2|2026-07-09|
|prompt-management|2.0.6|2026-07-09|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Microsoft Teams Communications Spoke|1.5.0|2025-12-11|
|Guided Self-Service in Employee Center|3.2.2|2025-12-11|
|Analytics Pack for Contract Management Pro|1.2.0|2025-05-01|
|GRC: Business User - Lite|18.0.0|2024-02-01|
|GRC: Management Reporting|18.1.0|2024-06-06|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Financial Services Document Management|1.3.1|2022-02-03|
|@devsnc/sn-uibtk-placeholder|29.1.71|2026-03-12|
|Password Reset integration with Google Directory|1.0.3|2023-06-01|
|YouTube Spoke|1.0.5|2025-07-10|
|Cybersecurity Executive Dashboard|2.4.3|2025-05-01|
|Order Management Portal|2.1.0|2025-07-31|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Professional Data Model|1.1.0|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|HR Service Delivery for mobile|21.2.9|2025-12-11|
|Security Incident Response integration with Proofpoint|1.1.0|2025-12-11|
|AES Decision Table Builder Wizard|4.0.0|2023-02-02|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|DevOps Flow Wizards|1.1.1|2022-09-21|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Financial Services Document Management|1.3.1|2022-02-03|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|FSO - Foundation|1.0.0|2026-04-09|
|CrowdStrike Falcon EDR Integration for Threat Intelligence Security Center|3.0.0|2024-11-07|
|Idea Manager Dashboard|2.2.0|2025-12-11|
|Digital Portfolio Management|7.4.1|2026-01-20|
|Field Service Quality Management|29.1.1|2026-03-12|
|Flow Templates for HR Management|1.4.4|2023-04-06|
|sn-4q-bubble|23.2.3|2026-06-16|
|AWH for AI Control Tower|2.0.9|2026-05-05|
|Experimentation Framework Core|1.1.14|2026-07-09|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|FSO - Prime|1.0.0|2026-04-09|
|Notify Zoom Connector|1.9.0|2025-07-31|
|Personal Lines Claims|4.4.0|2026-03-12|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|HR Multi Instance Integration Base|2.0.0|2025-07-31|
|DEX for Zoom|5.0.0|2026-07-09|
|Card data security|1.0.1|2025-07-31|
|Claim Common|2.3.3|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Field Service Capacity and Reservations Management|30.0.3|2026-03-12|
|Conversational Integration with Apple Messages for Business|1.3.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|sn-cwm-agile|2.1.0|2026-03-12|
|sn-quick-filter-popover|24.3.1|2026-05-05|
|Common Guidances|14.1.0|2026-07-09|
|User Surveys|1.5.4|2025-12-11|
|@devsnc/behavior-uibtk-supporting-records|29.1.71|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Performance Appraisal App Template|28.2.1|2025-12-11|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Collaboration Services|3.12.2|2025-12-11|
|Intelligent Task Recommendations|29.0.7|2026-03-12|
|Customer Service RMA AI Agents|1.0.2|2026-03-12|
|Zero Copy Connector for ERP|10.0.9|2026-05-05|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|Craft.co Integration for Supplier Lifecycle Operations|5.0.0|2026-06-16|
|Reporting UI Component for Workspace|2.5.0|2026-07-09|
|Workplace Lease Administration|1.8.5|2026-07-09|
|Customer Request for Quote|1.0.0|2025-12-11|
|Fortify Application Vulnerability Integration|2.7.1|2025-09-10|
|DEX for Zoom|5.0.0|2026-07-09|
|@devsnc/sn-list-selector|26.1.3|2026-03-12|
|Performance Analytics Content Pack for Legal Service Delivery|2.7.0|2025-12-11|
|ServiceNow Enterprise Asset Management|10.0.0|2026-03-12|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|Security Center|3.2.3|2026-02-05|
|Legal Practice Apps Core|1.0.2|2023-02-02|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Microsoft Azure Virtual Network Spoke|2.0.0|2024-11-07|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Price Management|17.0.1|2026-06-16|
|WDF Unified Hub|1.1.0|2026-07-09|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Telecom Discovery Patterns|1.0.2|2025-12-11|
|Sitemap Generator|1.2.0|2025-07-31|
|Field Service Management Intelligent Task Recommendations|29.0.6|2026-03-12|
|Formula Builder|29.1.1|2026-03-12|
|ICW - Foundation|1.0.3|2026-05-05|
|SPM Common UI Component|4.1.0|2026-03-12|
|Group Life Servicing|2.5.0|2026-03-12|
|Financial Services Document Management|1.3.1|2022-02-03|
|Legal Virtual Agent Conversations|1.3.2|2023-05-04|
|Context Menu Component for Configuration Data Management UI|1.2.1|2023-05-04|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Sales Quota Application|1.1.0|2025-12-11|
|OTSM Foundation|1.0.1|2026-04-09|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Field Service Advanced Capacity and Reservations Management|30.0.3|2026-03-12|
|Map Integrations for Field Service|29.0.8|2026-03-12|
|Healthcare and Life Sciences Service Management Core|11.3.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|Service Graph Connector for Akamai API Security|1.0.0|2025-10-16|
|HR Multi Instance Integration for Consumer|2.0.0|2025-07-31|
|Business Location|5.5.0|2026-06-16|
|Business domain|22.3.1|2026-06-16|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Salesforce Marketing Cloud Spoke|1.5.1|2025-03-12|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Finance Case Management|1.5.1|2026-06-16|
|Cloud Insights Billing|6.0.1|2024-04-04|
|ITOM Infra Services Workspace|2.0.3|2026-07-09|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Service Observability UI|1.10.12|2025-12-11|
|Service Graph Connector for Trellix|1.0.0|2025-06-05|
|@devsnc/sn-uibtk-features-catalog-modal|29.1.71|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Microsoft Defender for Office365 Integration for SecOps|2.3.4|2024-12-05|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|CSC Content Pack|1.7.0|2025-12-11|
|Tag Governance|1.8.0|2025-12-11|
|Sales Quota Data Model|1.1.0|2025-12-11|
|Digital Product Release Policy Content Pack|2.2.0|2025-07-31|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Safe Workplace for mobile|2.10.3|2025-07-31|
|Setup Hub Config|4.0.8|2026-08-13|
|Event Inquiry|1.4.0|2025-07-31|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|sn-app-par-components-export-modal|8.4.3|2026-07-09|
|sn-app-analytics-center|8.4.1|2026-07-09|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Impact Value Management - SECOPS|3.0.3|2025-12-11|
|Vulnerability Response Mobile|11.1.1|2023-05-04|
|Software Asset Management integration with Tableau|1.0.1|2024-08-01|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Microsoft Word Add-in for ServiceNow Contracts|1.6.7|2025-12-11|
|sn-app-par-components-component-builder|8.4.3|2026-07-09|
|@servicenow/sn-cb-asset-picker|27.2.29|2025-05-01|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Task Communications Management UI Components for Configurable Workspaces|9.2.0|2026-06-16|
|Asset Management for mobile|27.0.2|2025-07-31|
|Care Team Portal|2.2.0|2026-03-12|
|AI Experience Framework Components for Now Assist Setup|1.2.1|2026-07-09|
|Saba Spoke|1.2.2|2026-06-16|
|Legal Mobile|5.6.0|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|Impact Value Management - APM|2.1.0|2025-01-30|
|Field Service Manager Workforce|1.1.0|2026-04-09|
|SOW Funnel Highchart Component|28.3.1|2026-03-12|
|SumTotal Spoke|1.1.0|2023-03-02|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Asset Management for mobile|27.0.2|2025-07-31|
|External Content Connectors SAP Document Management System|7.0.7|2026-05-28|
|Guidance|43.1.0|2026-07-09|
|Supplier Relationship and Performance Management|10.0.0|2026-06-16|
|CMDB Page Templates|3.2.6|2026-06-16|
|Security Simulation and Training Integration for SecOps|2.1.3|2024-05-09|
|ESG integration with DEX|21.1.0|2025-12-11|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|sn-app-par-components-export-email-composer|8.4.3|2026-07-09|
|@devsnc/sn-uibtk-stage-scale-controls|29.1.71|2026-03-12|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|sn-app-par-components-dynamic-renderer|8.4.3|2026-07-09|
|Financial Services Document Management|1.3.1|2022-02-03|
|Service Exchange Health|2.3.26|2026-07-17|
|Advanced Work Assignment for Legal Service Delivery|1.1.1|2025-06-05|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Task Intelligence for Customer Service|25.4.0|2025-12-11|
|Service Builder|3.6.1|2025-12-11|
|Workday ESG integration|21.1.1|2025-12-11|
|SBOM Core|6.2.2|2025-12-11|
|Impact Value Management - IRM|3.0.3|2025-12-11|
|Data Model Navigator|1.0.3|2026-03-12|
|Conversational Integration with LINE|2.0.7|2025-01-30|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|Technology Portfolio Management|1.10.0|2026-06-16|
|Security Incident Response integration with FireEye HX|1.1.0|2025-12-11|
|Content Experiences|33.1.0|2026-07-09|
|Analytics Toolkit|8.4.3|2026-07-09|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Creator Studio Configurations|28.2.1|2025-12-11|
|Order Case Playbook|1.4.1|2025-12-11|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Agency Support Model|3.1.0|2026-07-09|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|SBOM Response|6.4.1|2025-12-11|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Email Interaction Core|1.0.3|2025-12-11|
|Microsoft Defender for Cloud Integration for Security Operations|2.8.0|2025-12-11|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|CLI Metadata|1.1.2|2021-04-15|
|Google Cloud VPC Access Spoke|1.0.1|2022-09-01|
|Udemy Spoke|1.0.2|2022-12-01|
|Cloud Flow Wizards|1.2.1|2022-08-24|
|Oracle Cloud IAM Spoke|1.1.3|2022-09-21|
|Sales Cart|2.1.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|AES UI Template Wizards|28.2.1|2025-12-11|
|sn-app-par-components-create-dashboard-modal|8.4.3|2026-07-09|
|Zero Touch Service Desk|2.3.19|2026-07-30|
|Commercial Lines Claims|4.4.0|2026-03-12|
|PDF Extractor|28.2.1|2025-12-11|
|Care Team Mobile|1.2.0|2026-03-12|
|API Service Graph Connector for Kong Konnect|1.0.0|2025-10-16|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Event Inquiry|1.4.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Service Graph Connector for VMware Workspace ONE UEM|1.8.0|2025-07-31|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Card data security|1.0.1|2025-07-31|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Service Graph Connector for Infoblox|1.4.0|2025-07-31|
|sn-app-par-components-share-dialog|8.4.3|2026-07-09|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Performance Analytics Content Pack for Public Sector Digital Services|2.0.3|2024-09-10|
|Threat Intelligence Security Center integration with Elasticsearch|3.0.4|2025-05-01|
|Conversational SMS Service Channel|2.0.23|2026-03-12|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Node map Experience Component|27.3.0|2025-12-11|
|Contract Management Pro for Legal Service Delivery|3.0.2|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Predictive Intelligence for Legal Service Delivery|1.2.0|2025-12-11|
|GRC: Continuous Authorization and Monitoring Advanced|21.1.1|2025-12-11|
|ITSM NLU Model for Virtual Agent Conversations|8.2.0|2025-05-01|
|Software Asset Management for CPE support|1.0.0|2022-08-04|
|sn-dashboards-view|29.0.1|2026-03-12|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Threat Intelligence Security Center integration with VirusTotal|3.0.3|2025-03-12|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Enterprise Architecture Cloud Assessment|1.0.1|2025-01-30|
|Financial Services Document Management|1.3.1|2022-02-03|
|Usage Insights Query Builder|6.3.9|2026-07-09|
|Notify Webex Connector|1.4.0|2025-12-11|
|Export to PowerPoint for Strategic Portfolio Management|1.4.2|2025-12-11|
|Impact Value Management - SPM|3.0.1|2025-12-11|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Security Operations Palo Alto Networks - WildFire|10.4.0|2025-01-30|
|DevOps Change Velocity|7.0.0|2026-06-16|
|Visa Spoke|2.2.2|2025-12-11|
|Service Graph Connector for Microsoft Defender Endpoint|1.2.0|2025-05-01|
|@devsnc/sn-uibtk-editor-header|29.1.71|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Requester Experience Templates|1.0.0|2024-11-07|
|Agent Messaging Component|3.0.17|2026-03-12|
|Appointment calendar component|28.1.1|2025-12-11|
|Google Docs Spoke|1.3.0|2025-09-10|
|Cloud Insights Billing|6.0.1|2024-04-04|
|Coupa Spoke|4.14.0|2025-10-16|
|Tableau Spoke|1.0.2|2024-08-01|
|AES Portal UI Template|28.2.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Vendor Risk Management integration with EcoVadis|21.1.1|2025-12-11|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Impact Value Management - CSM|2.1.0|2025-01-30|
|Mobile SDK|2.2.0|2025-03-12|
|Google Calendar Spoke|2.6.0|2025-09-10|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|Industrial Workspace Common|4.2.2|2026-08-13|
|sn-app-par-components-config-panel|8.4.3|2026-07-09|
|Flow Templates for Access Management|1.0.4|2023-04-06|
|Flow Templates for IntegrationHub Enterprise|1.0.2|2023-04-06|
|CMDB Application for APIs and CLI|1.0.1|2021-07-22|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Financial Services Document Management|1.3.1|2022-02-03|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Surveys for mobile|1.0.2|2021-09-16|
|Twilio Spoke|1.2.0|2023-02-02|
|sn-nlq-analytics|29.0.1|2026-03-12|
|Health and Safety Components|12.1.2|2026-07-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|ITSM Mobile Agent|10.2.0|2025-12-11|
|Impact Value Management - App Engine|2.1.0|2025-01-30|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|sn-docintel-iframe|1.0.4|2024-02-01|
|Agency Support Model|3.1.0|2026-07-09|
|AI Case Management|22.4.2|2026-07-09|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Microsoft Dynamics 365 for Finance and Operations Spoke|2.4.3|2026-01-20|
|Notifications for Employee Center|2.2.0|2026-07-09|
|Employee Travel Safety|1.22.0|2025-12-11|
|AI Risk and Compliance Content|21.1.1|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Tasks for mobile|27.1.0|2024-11-07|
|sn-app-par-components-chart-drilldown-configuration|8.4.3|2026-07-09|
|Service Exchange Remote Process Sync Transport|2.3.26|2026-07-17|
|FSM Scheduling AI Agent Collection|1.0.7|2026-06-16|
|PDF Extractor|28.2.1|2025-12-11|
|AES Role Builder Component|28.2.1|2025-12-11|
|Event Inquiry|1.4.0|2025-07-31|
|Employee Center Pro Kiosk|2.3.4|2025-12-11|
|sn-app-par-components-insights-panel|8.4.3|2026-07-09|
|Transporter|2.3.26|2026-07-17|
|Vulnerability Solution Management|10.4.3|2022-12-01|
|Omni-Experience Standard Feature Set|8.1.6|2026-04-09|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|CMDB and CSDM Data Foundations Dashboards|4.2.0|2025-12-11|
|AI Search for Customer Portals|1.1.0|2025-12-11|
|Legal Content Review|1.3.0|2025-12-11|
|Impact Value Management - ITOM|3.0.1|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-app-par-components-data-visualization-wrapper|8.4.3|2026-07-09|
|Application Service Extensions|1.1.7|2024-11-07|
|Notify Connector for Microsoft Teams|2.10.0|2025-12-11|
|Matrix report|21.0.1|2025-07-31|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Security Operations VirusTotal Integration|10.4.1|2025-12-11|
|Security Posture Control Core|7.0.1|2025-12-11|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Asset Management for mobile|27.0.2|2025-07-31|
|Smartsheet Spoke|2.6.1|2026-01-20|
|Service Exchange for Consumers|2.3.26|2026-07-17|
|Virtual Agent for Source-to-Pay Operations|3.11.0|2025-07-31|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Amazon Connect Spoke|1.2.0|2025-03-12|
|Card data security|1.0.1|2025-07-31|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Broadcom Rally Integration with DevOps|7.0.0|2026-06-16|
|Order Management Portal|2.1.0|2025-07-31|
|Team Contacts App Template|28.2.1|2025-12-11|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Customer Life Cycle Management Self Service|2.1.1|2025-12-11|
|GRC: Predictive Intelligence|21.1.0|2025-12-11|
|Qualys Integration for Security Operations|12.19.6|2025-12-11|
|Security Case Management common PAD artefacts|1.1.12|2026-01-20|
|Conversational Integration with WhatsApp \(powered by Twilio\)|2.0.11|2025-12-11|
|Sales and Order Management Mobile Common|29.1.2|2026-03-12|
|CPRO Dashboard|2.0.5|2025-12-11|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Financial Services Document Management|1.3.1|2022-02-03|
|Sales Agreement Management|8.0.0|2025-12-11|
|DLP Incident Response integration with Netskope|1.2.1|2026-01-20|
|sn-app-par-nacm-component|8.4.3|2026-07-09|
|Source-to-Pay Operations with Contract Management Pro|2.0.1|2025-05-01|
|Google Tasks Spoke|1.4.0|2025-09-10|
|CDO Dashboard|2.0.5|2025-12-11|
|sn-guided-action-experience|39.0.1|2025-12-11|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|DLP Incident Response integration with Symantec|1.3.1|2026-01-20|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Service Contractor Base|2.0.0|2026-03-12|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|sn-nlq-analytics|29.0.1|2026-03-12|
|External Content Connectors Slack|7.0.7|2026-05-28|
|Recommended Actions|42.1.0|2026-07-09|
|Contracts Core components|1.4.1|2025-07-31|
|Content Experiences|33.1.0|2026-07-09|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Google Directory Spoke|1.5.2|2024-10-03|
|One-time Password Generator|1.1.0|2025-12-11|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Talent Development Core|5.5.0|2026-06-16|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Metric Rules|1.1.4|2024-06-06|
|sn-viz-designer|8.4.1|2026-07-09|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Employee Readiness Surveys|1.5.3|2025-07-31|
|PPM Collaboration|2.1.0|2024-11-07|
|Adobe Experience Platform Spoke|2.2.0|2025-01-02|
|Microsoft Azure DevOps Integration for Agile Development|1.7.0|2025-12-11|
|ATF troubleshooting agent|1.0.3|2025-12-11|
|Chat Zoom Connector|1.0.6|2023-01-12|
|Case lines and workflows|4.3.0|2026-03-12|
|Customer Project Management|2.0.0|2026-03-12|
|Work Item Integrations Common|1.15.0|2026-06-16|
|ServiceNow Voice UI components|3.8.0|2026-02-05|
|AES Catalog Builder|28.2.1|2025-12-11|
|Document Processor|1.8.6|2026-07-09|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Service Organization|2.7.0|2026-06-16|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Document Flow Wizards|2.0.2|2022-09-21|
|Patch Management Data Model|1.0.4|2025-05-01|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|sn-app-par-components-scheduled-export|8.4.3|2026-07-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Microsoft Azure Cosmos DB Spoke|2.0.0|2024-11-07|
|Service Operations Workspace Service Map Monitoring|26.5.0|2025-07-31|
|Legal Tracker Spoke|1.0.4|2025-01-30|
|Indoor Mapping Component|1.6.1|2026-06-16|
|Journey Accelerator|6.10.0|2026-06-16|
|Vaccination Status|1.25.0|2025-12-11|
|Omnichannel Callback for Customer Service Management|1.5.1|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Problem Management Migration Utility|2.3.0|2026-03-12|
|Aria Systems Spoke|2.1.2|2023-04-06|
|Tasks for mobile|27.1.0|2024-11-07|
|Financial Services Document Management|1.3.1|2022-02-03|
|Security Operations Palo Alto Networks - AutoFocus|10.4.0|2025-01-30|
|Oracle Block Storage Spoke|1.0.4|2022-12-01|
|SOM - Prime|1.0.1|2026-04-09|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Financial Services Document Management|1.3.1|2022-02-03|
|Security Support Orchestration|12.13.4|2025-01-30|
|FSO - Advanced|1.0.0|2026-04-09|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|Task Intelligence for ITSM|8.2.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Territory Planning|30.0.3|2026-03-12|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Order Management Portal|2.1.0|2025-07-31|
|External Content Connectors Monday.com|7.0.7|2026-05-28|
|External Content Connectors SN Docs|7.0.7|2026-05-28|
|Event Inquiry|1.4.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|GRC: Risk Management|22.3.3|2026-06-16|
|Asset Management for mobile|27.0.2|2025-07-31|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|Workforce Optimization for ITSM Configurable Workspace|2.9.0|2026-05-05|
|Flow Templates for Cloud Services|1.2.3|2023-01-12|
|Watershed integration for ESG|16.0.1|2023-02-02|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Microsoft Azure DevOps Boards Spoke|3.1.0|2025-09-10|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Service Request Management App Template|28.2.1|2025-12-11|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Usage Insights Request Manager|6.3.9|2026-07-09|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|GRC: SOX Content Pack|21.1.0|2025-12-11|
|Tasks for mobile|27.1.0|2024-11-07|
|Employee Center integration with Zoom|2.0.16|2025-12-11|
|Field Service Management Scheduling Automations|29.0.6|2026-03-12|
|Search Configurations for mobile|29.0.7|2025-05-01|
|@devsnc/sn-uibtk-modal|29.1.71|2026-03-12|
|Cloud Deployment Automation|1.0.3|2024-12-05|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Amazon Alexa Spoke|1.1.0|2024-11-07|
|Industrial Control Tower Advanced|1.0.0|2026-06-16|
|Group Life Servicing|2.5.0|2026-03-12|
|Inventory Tracker App Template|28.2.1|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Order Qualification Management|4.5.0|2026-06-16|
|Contracts and Entitlement Workflows|13.0.0|2025-12-11|
|Forecast planning analysis|21.1.0|2025-12-11|
|Software Asset Management integration with Salesforce CRM|2.0.1|2025-12-11|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Financial Services Document Management|1.3.1|2022-02-03|
|Cloudify Spoke|2.1.1|2023-04-06|
|@devsnc/sn-uibtk-content-tree-picker|29.1.71|2026-03-12|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Common Vendor Core|4.5.0|2026-06-16|
|Export to PowerPoint|2.3.0|2025-12-11|
|MID Guardian|1.0.4|2025-12-11|
|AI Search Admin Console|9.1.2|2026-07-09|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Oracle Boot Volume Spoke|1.0.6|2022-12-01|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Contract Workspace|1.7.2|2025-12-11|
|Legal Conflict of Interest|4.7.0|2025-12-11|
|Kanban board component|26.0.1|2026-02-05|
|sn-component-workspace-ribbon|30.0.0|2026-03-12|
|Vulnerability Response Common|2.15.0|2026-01-20|
|sn-next-best-action-list|39.0.0|2026-06-16|
|Hiring Connector|7.0.0|2025-12-11|
|News Integration for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|Smart Assessment Migration tools|22.3.1|2026-06-16|
|Card data security|1.0.1|2025-07-31|
|Manage Skills Configurable Page|1.1.12|2025-01-30|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Lucidchart Integration|2.4.1|2025-01-30|
|Data Loss Prevention Incident Response|2.2.2|2026-02-05|
|Individual Life Claims|1.4.0|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Document Management|1.3.1|2022-02-03|
|Change Management for Field Service|1.1.2|2025-01-02|
|AWS Certificate Manager Spoke|1.0.1|2022-09-21|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Decision Builder|29.1.4|2026-04-09|
|Impact Value Management - APM|2.1.0|2025-01-30|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Microsoft Teams Chat Connector for Security Incident Management|1.2.30|2025-10-16|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|GRC: Cyber Risk Institute \(CRI\) Profile Accelerator|21.1.0|2025-12-11|
|Contact Center Integration Core|1.4.4|2025-12-11|
|Virtual Agent for PPM|1.0.1|2023-05-04|
|Flow Template Builder|1.0.9|2023-05-04|
|Impact Value Management - App Engine|2.1.0|2025-01-30|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Inventory Number Management|5.0.0|2025-07-31|
|sn-rack|4.0.0|2025-07-31|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|ServiceNow Otto for Setup|4.0.5|2026-08-13|
|Post Assessment Actions for Smart Assessments|22.3.2|2026-06-16|
|sn-dashboards-view|29.0.1|2026-03-12|
|Gifts and Entertainment Compliance|1.3.0|2025-12-11|
|ITAM common hub|1.1.0|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|AI Service Graph Connector for Amazon|1.0.4|2026-03-12|
|Word Document Templates|1.9.7|2026-01-20|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Triggers|29.0.2|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Personal Lines Claims|4.4.0|2026-03-12|
|sn-guided-action-experience|39.0.1|2025-12-11|
|Enterprise Asset Management for Providers|1.0.0|2025-12-11|
|App Generation|28.3.12|2026-07-09|
|Theme Builder|6.1.5|2026-01-22|
|Site Mapping for Field Service Management|2.1.1|2026-03-12|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Supplier Collaboration Portal|11.0.0|2026-06-16|
|GRC: NIST CSF Use Case Accelerator|21.1.0|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Google Drive Spoke|2.3.0|2025-09-10|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Entitlements Verification|6.0.0|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|GRC: Compliance Management Workspace|21.1.3|2025-12-11|
|Team Performance|202603.0.0|2026-03-12|
|Table Builder|29.1.1|2026-03-12|
|Security Incident Response Mobile|10.4.0|2024-11-07|
|Value dashboard for AI Control Tower|6.0.10|2026-08-10|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Conversational Integration with Slack|6.0.6|2026-03-12|
|Financial Services Document Management|1.3.1|2022-02-03|
|Microsoft Exchange Online for Security Operations|10.7.2|2026-01-20|
|AI Asset Management|5.0.3|2026-07-09|
|Vulnerability Response Integration with Veracode|4.7.3|2025-12-11|
|@devsnc/sn-uibtk-scope-picker|29.1.71|2026-03-12|
|@devsnc/library-uibtk-screen|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-element-context-menu|29.1.71|2026-03-12|
|Threat Intelligence Security Center integration with CrowdStrike Intelligence|3.0.4|2025-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|Employee Health Screening|1.28.0|2025-07-31|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|FSO - Advanced|1.0.0|2026-04-09|
|Source-to-Pay Integration Framework|14.0.2|2026-06-16|
|Advanced Promotion Engine|4.2.1|2025-12-11|
|Firewall Audits and Reporting|1.8.0|2025-12-11|
|Task Intelligence Admin Console|5.2.1|2025-12-11|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Special Handling Instruction|26.0.3|2026-05-05|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Vulnerability Response Common Workspace|1.9.0|2026-01-20|
|Security Operations Metadefender Integration|10.5.0|2024-08-01|
|Emergency Self Report|1.21.0|2025-07-31|
|Microsoft Azure Artifacts Spoke|1.1.0|2024-11-07|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|HR Service Delivery NLU Model for Virtual Agent Conversations|22.2.0|2023-11-02|
|MID Server Infrastructure|2.0.1|2026-07-09|
|ServiceNow Remote Instance Spoke|2.2.9|2025-11-06|
|sn-dashboards-view|29.0.1|2026-03-12|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Career Assessment|3.3.0|2026-06-16|
|Client Software Distribution 2.0|1.4.0|2025-12-11|
|Integrated Risk Management Standard|22.1.1|2026-04-09|
|AI SGC Discovery|1.0.0|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Discovery and Service Mapping Patterns|1.31.2|2026-07-09|
|Google Cloud Load Balancer Spoke|1.0.2|2023-09-07|
|sn-circuit-map|5.0.0|2025-07-31|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Risk Assessments for Supplier Lifecycle Operations|4.0.0|2026-06-16|
|Check Point Integration for Security Operations|10.4.10|2025-07-31|
|Ethoca Spoke|3.0.1|2025-07-31|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Conversational Integration with Workplace from Facebook|5.0.1|2025-01-30|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Github Application Vulnerability Integration|2.3.1|2025-12-11|
|Document Intelligence for Accounts Payable Operations Content Pack|2.0.0|2025-12-11|
|Service Graph Connector for Observability - Datadog|1.4.0|2025-12-11|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|sn-app-par-coreui-migration-center|4.0.3|2026-03-12|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Task activity timeline|25.4.0|2025-12-11|
|Vulnerability Response Integration with Black Duck|1.1.1|2025-12-11|
|ServiceNow Voice for ITSM|4.1.1|2025-12-11|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|Zoom Spoke|4.6.2|2026-01-20|
|Jenkins Spoke|2.3.0|2025-09-10|
|Setup Hub|2.0.8|2026-08-13|
|Virtual Agent Topic Recommendations|4.5.5|2024-08-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Service Graph Connector for Observability - AppDynamics|1.6.0|2025-12-11|
|Contract Management Pro|1.6.0|2025-12-11|
|Order Management Portal|2.1.0|2025-07-31|
|Service Level Objective Management for Service Operations Workspace|2.0.0|2026-06-16|
|Strategic Portfolio Management - Prime|1.0.4|2026-04-09|
|Workspace navigation and experience demo|27.1.1|2026-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Manage Invoice Operations|1.1.2|2026-07-09|
|@devsnc/sn-uibtk-form-factor-controls|29.1.71|2026-03-12|
|Google Chat Spoke|1.2.0|2025-09-10|
|HR Multi Instance Integration for Provider|2.0.0|2025-07-31|
|Meeting CAB|9.2.0|2026-06-16|
|Workday Learning Spoke|1.1.4|2024-04-04|
|Threat Intelligence Security Center Integration with Palo Alto Networks NGFW|2.0.1|2025-03-12|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|Service Exchange - Foundation|1.1.13|2026-08-13|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|AES Flow Wizards|28.2.1|2025-12-11|
|ITOM - Prime|1.2.1|2026-08-13|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Product and pricing rules|9.0.0|2025-12-11|
|Lead-to-Cash Process Management|2.2.2|2025-12-11|
|AI Service Graph Connector for Databricks|1.0.2|2026-04-09|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Digital Product Release|2.3.2|2025-12-11|
|Agile Integrations Common|1.4.0|2025-12-11|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Case Digests|2.0.0|2026-03-12|
|Timeline component|29.0.0|2026-03-12|
|Field Service Territory Planning|30.0.3|2026-03-12|
|Customer Service NLU Model for Virtual Agent Conversations|1.0.5|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|External Content Connectors Admin|7.0.7|2026-05-28|
|External Content Connectors Workday|7.0.7|2026-05-28|
|Conversational Appointment Booking Components|2.0.5|2023-09-07|
|@servicenow/sn-cb-commons|27.2.29|2025-05-01|
|Universal Request integration with Microsoft Teams|1.0.2|2022-12-01|
|Synthetic Monitoring|1.4.4|2025-12-11|
|Microsoft Azure RBAC Spoke|1.0.2|2025-09-10|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Project Status Report|1.1.0|2023-02-02|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|GRC: Composite Entity|21.1.1|2025-12-11|
|Healthcare Professional Data Model|1.3.0|2025-12-11|
|Vulnerability Response Integration with Palo Alto Prisma Cloud|2.8.0|2025-12-11|
|Virtual Machine Management for Virtual Agent|3.0.11|2023-08-03|
|DLP Incident Response integration with ICAP|1.1.1|2026-01-20|
|Sales Territory Management|2.0.0|2026-03-12|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|@devsnc/sn-uibtk-menu-elements|29.1.71|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Google Cloud Pub Sub Spoke|1.0.4|2024-09-10|
|Industrial Operations Suite Advanced|1.0.3|2026-08-13|
|Attribute Pack|5.0.0|2025-07-31|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|Financial Services Document Management|1.3.1|2022-02-03|
|Cloud Configuration Governance|1.6.0|2025-12-11|
|AI Service Graph Connector for LangGraph|1.1.0|2026-03-12|
|Customer Service Document Template|2.0.0|2026-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|@devsnc/library-uibtk-uxvalue|29.1.71|2026-03-12|
|@servicenow/sn-component-builder|29.1.32|2026-03-12|
|sn-app-par-components-export-modal|8.4.3|2026-07-09|
|Microsoft OneDrive Spoke|2.8.1|2025-11-06|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Security Incident Response integration with Microsoft Defender for Endpoint|1.2.1|2026-02-05|
|sn-nlq-query-input|30.0.1|2026-03-12|
|App Engine Studio|28.2.1|2025-12-11|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Craft.co Integration for Supplier Lifecycle Operations|5.0.0|2026-06-16|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|IT Service Management for Microsoft 365|2.11.1|2025-12-11|
|GRC integration with Thomson Reuters Regulatory Intelligence|21.1.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Service Graph Connector for Microsoft Azure|1.15.0|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|GRC: Regulatory Change Management integration with RSS Feeds|21.1.0|2025-12-11|
|IntegrationHub ETL|3.3.6|2025-12-11|
|Data registry|22.3.1|2026-06-16|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Order Management Portal|2.1.0|2025-07-31|
|Customer Service integration with Social Media Store|1.0.2|2026-03-12|
|File Explorer for Security Incident Response|1.3.0|2025-12-11|
|Industrial Process Manager|4.2.2|2026-08-13|
|Skill Review Management|1.6.1|2025-12-11|
|Value Engine|6.0.10|2026-08-10|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Amazon CloudWatch Spoke|1.0.2|2022-12-01|
|@devsnc/sn-uibtk-element-properties-configuration-pane|29.1.71|2026-03-12|
|Customer Service with Request Management|2.1.0|2026-04-09|
|Service Graph Connector for AWS|2.12.1|2025-10-16|
|Threat Intelligence Security Center integration with Shodan|1.0.7|2025-05-01|
|AES Table Builder Wizard|28.2.1|2025-12-11|
|Password Reset integration with Okta|1.1.2|2023-04-06|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Service Graph Connector for Observability - New Relic|1.4.0|2025-12-11|
|Configuration Compliance|15.5.3|2025-12-11|
|Microsoft Teams Graph Spoke|4.4.1|2026-02-05|
|Guidewire Spoke|1.3.0|2026-03-12|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Enterprise Asset Management for DCNAM Advanced|1.0.0|2026-04-09|
|sn-component-workspace-shn|29.0.7|2026-03-12|
|Test Generation|4.0.11|2025-12-11|
|Customer Service Install Base Characteristics|2.3.0|2026-03-12|
|Workplace Indoor Map Component|1.1.1|2024-08-01|
|Asset Shipments|1.0.0|2026-03-12|
|@servicenow/sn-cb-api|27.2.29|2025-05-01|
|@devsnc/sn-uibtk-icon|29.1.71|2026-03-12|
|sn-topology-map|4.0.0|2025-07-31|
|Digital Signature API|26.0.0|2024-08-01|
|Health and Safety Incident Management PA Content Pack|10.1.1|2026-07-09|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|Manufacturing Core|2.3.3|2025-12-11|
|Meeting Extensions for Microsoft Teams|1.8.0|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|Activity Timer|1.0.2|2026-03-12|
|Cloud Storage|6.1.0|2026-03-12|
|Resolution Shaper|29.0.10|2026-03-12|
|Order Management|5.0.0|2023-02-02|
|Admin Workspace for Service Providers \(SPs\)|1.1.4|2025-07-31|
|sn-app-par-components-info-panel|8.4.3|2026-07-09|
|Insurance claims|1.2.2|2026-03-12|
|AES Role Builder|28.2.1|2025-12-11|
|AI agents and skills for Quote Management|3.0.1|2026-07-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Product Conditions Core|4.6.0|2026-06-16|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|SPW Jira Integrations|1.0.0|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Action Status Automation|2.0.0|2026-03-12|
|Document Templates|29.0.1|2026-07-09|
|@devsnc/uibtk-uxf-assets|29.1.71|2026-03-12|
|Microsoft Security Response Center Spoke|1.3.0|2025-09-10|
|Microsoft SharePoint Online Spoke|2.10.0|2025-09-10|
|Flow Templates for Notifications|1.2.4|2024-06-06|
|@devsnc/sn-uibtk-props-pane|29.1.71|2026-03-12|
|@servicenow/sn-cb-property-pane|27.2.29|2025-05-01|
|Breadcrumb navigation demo|27.0.0|2025-06-05|
|@devsnc/sn-uibtk-style-select|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-style-provider|29.1.71|2026-03-12|
|Service Graph Connector for SolarWinds|2.6.0|2025-07-31|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Skills Workspace|6.1.0|2025-12-11|
|ITSM Virtual Agent Conversations|9.3.2|2026-03-12|
|Service Request Criteria|3.1.0|2026-06-16|
|PSDS - Advanced|1.0.1|2026-04-09|
|Digital Product Release Data Model|2.4.0|2026-03-12|
|policy-as-code-engine-ui|3.3.0|2026-06-16|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|Equifax Spoke|1.0.0|2023-08-03|
|Fallout management|7.8.0|2026-06-16|
|Security Operations LogRhythm Integration|11.2.1|2025-12-11|
|Healthcare and Life Sciences Service Management Core|11.3.0|2026-03-12|
|Playbooks for Customer Service Management|6.5.1|2026-06-16|
|Order Operations Case Management|2.8.0|2026-06-16|
|Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute|3.5.0|2025-12-11|
|GRC: Advanced Dashboards|21.1.1|2025-12-11|
|Private cloud orchestration|1.0.0|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Flow Templates for Document Management|1.1.10|2023-04-06|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|Participant Suggestions|2.0.1|2024-08-01|
|Application Insights|2.0.3|2021-11-18|
|@devsnc/sn-uibtk-param-row|29.1.71|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Indoor Mapping Service|1.0.8|2025-12-11|
|Status Report UI Component for MSIM Workspace|1.0.2|2024-11-07|
|Impact Value Management - APM|2.1.0|2025-01-30|
|Task Plan Templates|4.0.0|2026-06-16|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Goal Framework for SPM|2.7.0|2026-03-12|
|Vulnerability Response|26.5.3|2026-01-20|
|External Content Connectors Docusign|7.0.7|2026-05-28|
|Industrial Control Tower Advanced|1.0.0|2026-06-16|
|Workplace Case Management|1.28.8|2026-07-09|
|@servicenow/sn-cb-experiences|27.2.29|2025-05-01|
|Security Integration Framework|13.13.0|2026-07-09|
|Security Incident Response integration with AWS SecurityHub|1.1.0|2025-12-11|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|@devsnc/sn-uibtk-minimized-dialogs-dropdown|29.1.71|2026-03-12|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Mobile App Builder API|27.11.0|2025-07-31|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Now Assist for Prompt Assistance|5.1.4|2026-07-09|
|ITAM Common for DaaS|11.2.1|2026-03-12|
|Mobile Builder AI|27.6.0|2026-07-09|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|@devsnc/sn-uibtk-formula-builder|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-client-state-config-panel|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-instance-config-editor|29.1.71|2026-03-12|
|@devsnc/library-uibtk-undo-redo|29.1.71|2026-03-12|
|Contact Tracing|1.30.0|2025-07-31|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|@devsnc/sn-uibtk-loader|29.1.71|2026-03-12|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Microsoft Entra ID Integration for Password Reset|3.0.3|2025-01-30|
|Service Graph Connector for Microsoft Intune|2.7.1|2025-10-16|
|BMC Remedy Spoke|1.4.1|2024-10-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Oracle Compute Engine Spoke|1.0.4|2022-12-01|
|Creator Studio|28.2.1|2025-12-11|
|Flow Templates for CRM|1.0.3|2023-04-06|
|Enterprise Architecture - Prime|1.0.1|2026-06-16|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|HR Service Delivery for Microsoft 365|3.8.0|2025-12-11|
|GRC: taxonomy management|22.3.0|2026-06-16|
|Mobile App Builder|27.11.0|2025-07-31|
|Beans.ai Spoke|29.0.7|2026-03-12|
|Task SLA cards|26.0.0|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|CSM Account Hierarchy|30.0.3|2026-03-12|
|Tasks for mobile|27.1.0|2024-11-07|
|@devsnc/sn-uibtk-draggable-list|29.1.71|2026-03-12|
|ArcSight Logger Integration for Security Operations|10.4.1|2024-11-07|
|Security Incident Response Integration with Zscaler|11.2.3|2026-02-05|
|Elasticsearch Integration for Security Operations|10.3.4|2024-11-07|
|KnowBe4 Integration for SecOps|2.3.3|2024-12-05|
|HR Service Delivery integration with Oracle HCM|1.0.10|2024-11-07|
|Vendor Manager Workspace|3.5.0|2024-11-07|
|Impact Value Management - App Engine|2.1.0|2025-01-30|
|ServiceNow Voice for HR Service Delivery \(HRSD\)|1.0.5|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Content Engagement for Employee Center Pro|1.4.1|2026-03-12|
|Quote Management for Business Locations|2.0.0|2026-03-12|
|Opportunity Management for Business Locations|2.0.0|2026-03-12|
|@devsnc/sn-uibtk-data-navigator|29.1.71|2026-03-12|
|Interview management|4.0.2|2026-07-09|
|Event Inquiry|1.4.0|2025-07-31|
|Dashboard and visualization export|1.3.5|2026-01-20|
|Tasks for mobile|27.1.0|2024-11-07|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|OT Asset Management Advanced|1.0.0|2026-04-09|
|Preferred tables|29.1.1|2026-03-12|
|Physical Assets|2.3.0|2026-03-12|
|@devsnc/sn-uibtk-events-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-stage-preview|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-draggable-dialog|29.1.71|2026-03-12|
|@servicenow/sn-controller-builder|29.1.30|2026-03-12|
|@devsnc/sn-uibtk-builder-in-builder|29.1.71|2026-03-12|
|@devsnc/library-uibtk-caching|29.1.71|2026-03-12|
|@devsnc/sn-ui-interaction-modals|29.1.14|2026-03-12|
|WSD - Foundation|1.0.2|2026-06-16|
|@devsnc/behavior-uibtk-media|29.1.71|2026-03-12|
|@devsnc/library-uibtk-commons|29.1.71|2026-03-12|
|Knowledge API|29.0.1|2026-03-12|
|PDF Extractor|28.2.1|2025-12-11|
|Industrial Control Tower Foundation|1.0.0|2026-06-16|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|ITSM Common Catalog Content|3.1.0|2026-07-09|
|Technology Core|3.8.4|2026-06-16|
|Sales Agreement Data Model|8.0.0|2025-12-11|
|Business Object Core|2.1.0|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|ITSM Process Mining Content Pack|2.0.0|2026-03-12|
|Advanced Work Assignment for CSM|1.0.4|2026-03-12|
|Universal Request for Source-to-Pay Operations|1.2.2|2026-06-16|
|WDF Tokenization|2.0.2|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Decision Table Builder|29.1.6|2026-04-09|
|ServiceNow Add-Ins for Microsoft Office|7.4.0|2025-12-11|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Content library portal|4.1.1|2026-07-09|
|External Content Connectors Aha Roadmaps|7.0.7|2026-05-28|
|External Content Connectors Zoom|7.0.7|2026-05-28|
|Process Mining for external data|29.5.0|2026-03-12|
|Skills foundation|10.1.0|2026-06-16|
|Care Team Mobile|1.2.0|2026-03-12|
|@devsnc/sn-uibtk-viewport-config-panel|29.1.71|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|AI Admin Hub|10.2.6|2026-08-13|
|@devsnc/uibtk-api|29.1.71|2026-03-12|
|Business Object Core|2.1.0|2025-12-11|
|GoTo Spoke|2.0.1|2021-08-19|
|Header App Shell|23.0.0|2023-06-01|
|Order Case Self Service|1.4.3|2026-06-16|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|FSO - Foundation|1.0.0|2026-04-09|
|Collaboration Services for Service Operations Workspace|9.2.0|2026-06-16|
|Impact Value Management - HR|4.0.0|2026-06-16|
|Microsoft Outlook Add-In for Legal Service Delivery|1.5.0|2025-12-11|
|Workplace Service Delivery Suite|2.17.2|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Field Service Marketplace|30.0.1|2026-03-12|
|sn-component-account-hierarchy|29.0.7|2026-03-12|
|Customer Service Portal|25.3.0|2026-03-12|
|SPM Team Member|1.0.0|2026-04-09|
|Major Security Incident Management|3.5.1|2026-01-20|
|External Content Connectors Zendesk|7.0.7|2026-05-28|
|Work Scheduler for Workforce Optimization|3.3.2|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|MID Admin Workspace|2.0.1|2026-07-09|
|@devsnc/sn-uibtk-transaction-alert|29.1.71|2026-03-12|
|Secureworks Ticket Ingestion Integration for Security Operations|11.1.2|2026-02-05|
|Order Management Portal|2.1.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Workplace Service Delivery Enterprise|1.6.0|2025-12-11|
|AI Search For Next Experience|5.0.2|2026-02-05|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Advanced Appointment Booking|30.0.1|2026-03-12|
|@devsnc/sn-uibtk-replace-component|29.1.71|2026-03-12|
|Flow Templates for DevOps|1.1.3|2023-04-06|
|Order Case Self Service|1.4.3|2026-06-16|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|GRC: Policy and Compliance integrator|21.1.0|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|@devsnc/sn-help-setup|29.0.0|2026-03-12|
|PAR CoreUI Migration Scripts|4.0.3|2026-03-12|
|Financial Services Document Management|1.3.1|2022-02-03|
|ServiceNow Voice|5.0.1|2026-02-05|
|@servicenow/sn-preset-builder|29.1.28|2026-03-12|
|Financial Services Document Management|1.3.1|2022-02-03|
|Microsoft Azure Virtual Machine Spoke|2.0.0|2024-11-07|
|Microsoft Azure Resource Management Spoke|2.0.0|2024-11-07|
|@devsnc/sn-uibtk-tabs|29.1.71|2026-03-12|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Asana Spoke|1.0.3|2024-08-01|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Performance Analytics Content Pack for Cloud Resources|1.5.0|2024-11-07|
|Amazon RDS Spoke|1.0.5|2025-06-05|
|Order Management Portal|2.1.0|2025-07-31|
|Usage Insights Application|6.3.9|2026-07-09|
|GRC: Vendor Portal|22.3.2|2026-06-16|
|Customer Life Cycle Management Workflows|5.1.1|2025-12-11|
|Service Catalog for mobile|29.0.7|2025-05-01|
|GRC: Continuous Authorization and Monitoring Workspace|21.1.1|2025-12-11|
|Kubernetes Visibility Agent|3.13.0|2025-12-11|
|Summarization for Quote Management|1.1.0|2026-04-09|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|ITAM Health Check application|3.0.5|2026-03-12|
|@devsnc/sn-uibtk-script-config-panel|29.1.71|2026-03-12|
|Performance Analytics for Security Incident Response|10.5.2|2025-05-01|
|Microsoft Azure Application Insights Spoke|2.0.0|2024-11-07|
|Event Registration App Template|28.2.1|2025-12-11|
|@servicenow/sn-cb-presets|27.2.29|2025-05-01|
|Digital signature component|27.1.0|2025-07-31|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Customer Service with Service Portfolio Management \(SPM\)|2.0.1|2025-01-30|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Cloud Migration Assessment|1.4.0|2024-11-07|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Atlassian Administration Spoke|1.0.1|2025-01-30|
|@devsnc/sn-uibtk-extension-point-pane|29.1.71|2026-03-12|
|Event Inquiry|1.4.0|2025-07-31|
|Utility Actions Spoke|1.3.0|2024-10-03|
|Order Operations Case Management|2.8.0|2026-06-16|
|Finance Operations Workspace|1.5.1|2026-06-16|
|Microsoft Office add-in|22.3.0|2026-06-16|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Socure Spoke|1.2.2|2026-03-12|
|Regulatory Agency Library|22.3.0|2026-06-16|
|Enterprise Asset Management for Healthcare|1.1.2|2026-03-12|
|Operational Technology Health|4.1.2|2026-08-13|
|External Content Connectors Smartsheet|7.0.7|2026-05-28|
|FSO - Advanced|1.0.0|2026-04-09|
|@devsnc/sn-uibtk-preset-pane|29.1.71|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Health and Safety Incident Management PA Content Pack|10.1.1|2026-07-09|
|Workspace Inspector|20.1.1|2025-05-01|
|Microsoft Azure Blob Storage Spoke|2.0.0|2024-11-07|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Document Approval App Template|28.2.1|2025-12-11|
|Investigation Framework|9.2.0|2026-06-16|
|Impact Value Management - SPM|3.0.1|2025-12-11|
|Card data security|1.0.1|2025-07-31|
|AES Catalog Builder Wizard|28.2.1|2025-12-11|
|FSO - Prime|1.0.0|2026-04-09|
|Fallout management|7.8.0|2026-06-16|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Document Template Integration with AdobeSign|1.7.0|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|CSM Account Hierarchy|30.0.3|2026-03-12|
|@servicenow/sn-cb-slide-modal|27.2.29|2025-05-01|
|Workforce Optimization for HR|1.1.2|2025-07-31|
|Requirement Intake Diagram|1.0.1|2024-12-05|
|API Service Graph Connector for Kong Gateway|2.1.0|2025-10-16|
|Order Qualification Management|4.5.0|2026-06-16|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|User Experience Redirection|1.0.1|2026-03-12|
|GRC: Business Impact Analysis|11.0.2|2026-06-16|
|RMA Case Management|2.1.0|2026-03-12|
|Shift Planning|7.0.0|2026-03-12|
|Industrial Core|4.1.3|2026-08-13|
|Supplier Payment Optimization|6.0.0|2026-06-16|
|sn-next-best-action-list|39.0.0|2026-06-16|
|Configurable Workspace for Order Management|15.2.0|2026-06-16|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Document Management|1.3.1|2022-02-03|
|GRC: Advanced Core|22.0.1|2026-03-12|
|@devsnc/behavior-list-intent-translator|29.0.9|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Event Inquiry|1.4.0|2025-07-31|
|ITOM AIOPS Config Center|27.3.5|2026-06-16|
|Impact Value Management - SECOPS|3.0.3|2025-12-11|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|GRC: Continuous Authorization and Monitoring|21.1.1|2025-12-11|
|SGC Central|2.4.0|2026-03-12|
|Payment framework for conversational channels|1.1.0|2026-03-12|
|sn-component-workspace-ribbon|30.0.0|2026-03-12|
|Enterprise Architecture - Advanced|1.0.1|2026-06-16|
|Cornerstone Spoke|1.6.0|2026-07-09|
|Service Graph Connector for Microsoft Excel|4.1.2|2026-08-13|
|External Content Connectors Dropbox|7.0.7|2026-05-28|
|@devsnc/sn-uibtk-test-values-editor|29.1.71|2026-03-12|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Security Operations Hybrid Analysis Integration|10.7.0|2026-02-05|
|Verifi Spoke|1.0.0|2024-08-01|
|Emergency Alert App Template|28.2.1|2025-12-11|
|Financial Services Document Management|1.3.1|2022-02-03|
|Workforce Optimization Common|1.7.0|2025-12-11|
|POM - Foundation|1.1.2|2026-06-16|
|Scope 3 emissions management|21.1.1|2025-12-11|
|Performance Analytics for Vulnerability Response|12.16.1|2025-12-11|
|GRC: Compliance Case Management|21.1.0|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|Order Management Portal|2.1.0|2025-07-31|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Service Graph Connector for Google Console|1.0.0|2024-08-01|
|ServiceNow Otto AI Agents|8.2.13|2026-08-13|
|Content Understanding|7.0.5|2026-08-13|
|Collaboration Request|28.2.1|2025-12-11|
|CPQ Config Agent A2A|1.1.0|2026-07-09|
|Service Test Management|5.0.1|2025-12-11|
|Rapid7 Integration for Security Operations|13.16.4|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Business Continuity Management Advanced|1.1.3|2026-06-16|
|Field Service with Service Locations support|30.0.3|2026-03-12|
|Site Reliability Metrics UX|2.1.7|2023-11-02|
|Agent Forecast|5.7.1|2026-03-12|
|Portal Next Experience Theme|24.2.2|2026-03-12|
|App Collaboration Component|28.2.1|2025-12-11|
|Quick filter component|27.2.3|2026-06-16|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Workplace Service Delivery for Mobile|1.16.2|2025-12-11|
|@servicenow/sn-cb-usage|27.2.29|2025-05-01|
|Financial Services Document Management|1.3.1|2022-02-03|
|Service Graph Connector for Tanium|1.8.2|2025-11-06|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Service Operations Workspace Metric Explorer APIs|23.4.0|2025-07-31|
|@devsnc/sn-uibtk-json-navigator|29.1.71|2026-03-12|
|Customer Service Virtual Agent Conversations|1.0.5|2026-04-09|
|Redox Inbound Integration|6.0.0|2024-08-01|
|AES Workspace UI Template|28.2.1|2025-12-11|
|FSO - Advanced|1.0.0|2026-04-09|
|Chat Recommendation|1.8.3|2026-07-09|
|AI Agents for Discovery|3.2.1|2026-07-09|
|Agent Client Collector Log Analytics|3.9.1|2025-12-11|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Walk-Up for CSM|2.0.1|2026-03-12|
|Shift Planning for Configurable Workspace|3.8.0|2026-03-12|
|Product Configurator|1.0.1|2024-11-07|
|Process Mining for Source-to-Pay Operations|1.0.1|2024-08-01|
|sn-experiment-ui|1.1.14|2026-07-09|
|Industrial Control Tower Prime|1.0.0|2026-06-16|
|AES Notification Builder Component|28.2.1|2025-12-11|
|FSO - Prime|1.0.0|2026-04-09|
|Safe Workplace Dashboard|1.41.0|2025-07-31|
|@devsnc/sn-uibtk-is-hidden-property-input|29.1.71|2026-03-12|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Card data security|1.0.1|2025-07-31|
|FSO - Prime|1.0.0|2026-04-09|
|Usage Insights in Data Visualizations|6.3.9|2026-07-09|
|Customer Service Problem Management|5.0.2|2025-12-11|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|System Events and Jobs Dashboard|3.1.5|2026-03-12|
|External Content Connectors Microsoft Teams|7.0.7|2026-05-28|
|Service Operations Workspace Metric Explorer|27.1.1|2026-06-16|
|Customer Service Install Base Management|4.8.1|2026-06-16|
|KPI Framework|6.1.0|2026-06-16|
|Enterprise Modeling and Visualization|6.2.2|2026-06-16|
|Unified Content Management|22.4.0|2026-07-09|
|Gantt UI Builder Component|26.1.1|2026-06-16|
|HR License meter|1.1.6|2026-06-16|
|AES Mobile Templates|28.2.1|2025-12-11|
|Order Management|17.2.0|2026-07-09|
|Order Management for Telecom, Media and Tech|13.1.2|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Security Incident Response - Foundation|1.0.7|2026-06-16|
|Channel Management|7.1.1|2026-03-12|
|ICW Core|1.0.4|2026-05-05|
|ERP Integration Framework|19.0.3|2026-06-16|
|DevOps Config Policy Content Pack|1.6.0|2023-11-02|
|External Content Connectors Workvivo|7.0.7|2026-05-28|
|Supplier Operations|7.0.0|2026-06-16|
|Workplace Maintenance Management|1.11.5|2026-07-09|
|Advanced Response Automation for Smart assessments|22.3.0|2026-06-16|
|Licensing Engine|6.4.3|2026-06-16|
|Asset Management for mobile|27.0.2|2025-07-31|
|Security Incident Response - Advanced|1.0.7|2026-06-16|
|Time Off Request App Template|28.2.1|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|Craft.co Integration for Supplier Lifecycle Operations|5.0.0|2026-06-16|
|Field Service Management for Telecommunications|3.0.2|2025-12-11|
|Contract Management for Sales and Order Management|1.1.0|2025-12-11|
|Build Agent Glide Tools|1.0.10|2026-03-12|
|SOM - Advanced|1.0.1|2026-04-09|
|Bot Interconnect|1.7.0|2025-07-31|
|Proactive Customer Service Operations with Event Management|25.0.2|2026-03-12|
|CRM Territory Extensions|2.0.3|2026-03-12|
|Major Issue Management|4.1.7|2026-07-31|
|External Content Connectors FluidTopics|7.0.7|2026-05-28|
|Risk Assessments for Supplier Lifecycle Operations|4.0.0|2026-06-16|
|Learning Core|9.10.0|2026-06-16|
|@servicenow/sn-cb-theme-picker|27.2.29|2025-05-01|
|AWS Elastic Load Balancing Spoke|1.0.1|2022-09-01|
|CRM Flow Wizards|1.0.1|2023-04-06|
|Notify UI Components for Configurable Workspaces|9.2.0|2026-06-16|
|@devsnc/sn-uibtk-create-page|29.1.71|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|Microsoft Exchange Server Spoke|2.5.1|2025-11-06|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Data Model for Order Management|16.4.0|2026-07-09|
|sn-hr-casecard|1.3.2|2025-12-11|
|Workplace Services Kiosk|1.5.2|2025-12-11|
|GRC Privacy Case Management Integration with RadarFirst|21.1.0|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|CSM Extension for Proxy Contacts|2.0.0|2026-03-12|
|Workforce Optimization integration with Microsoft Outlook|1.4.0|2026-03-12|
|External Content Connectors Gitlab|7.0.7|2026-05-28|
|External Content Connectors Confluence Cloud|7.0.7|2026-05-28|
|Supplier Collaboration Portal|11.0.0|2026-06-16|
|Advanced Work Assignment for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|Integration Commons for CMDB|2.25.0|2026-06-16|
|Task Plan Template AI Agents|1.0.0|2026-06-16|
|Shift Handover Application|1.8.0|2026-06-16|
|Microsoft Graph Security API Alert Ingestion Integration For Security Operations|10.5.5|2026-07-09|
|Context Rule Management|10.6.0|2026-06-16|
|Service Graph Connector for Wiz|1.4.0|2025-11-06|
|Vulnerability Crisis Management|1.0.1|2024-08-01|
|monday.com Spoke|1.1.5|2025-06-05|
|Expense Pre-Approval Template|28.2.1|2025-12-11|
|Workforce Optimization Configurable Workspace Core|1.11.0|2025-12-11|
|Contact card component|26.0.0|2025-12-11|
|Scenario Planning for PPM|2.4.0|2025-12-11|
|Aleph Alpha Spoke|1.0.2|2025-01-30|
|@devsnc/sn-uibtk-style-pane|29.1.71|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Creator Studio Configurations|28.2.1|2025-12-11|
|Common UIB Wrapper Components|1.5.1|2025-12-11|
|Inventory Number Management|5.0.0|2025-07-31|
|Document Intelligence Admin|4.1.0|2025-12-11|
|Cloud Security Posture Management|2.5.0|2024-02-01|
|Zero Copy Connector Hub|3.0.1|2026-03-12|
|Proactive Customer Service Operations|25.0.1|2026-03-12|
|sn-app-par-components-dynamic-renderer|8.4.3|2026-07-09|
|Remediation Playbooks|1.1.0|2022-11-03|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Capacity Management|4.1.0|2025-12-11|
|Security Incident Response Integration with CrowdStrike Next-Gen SIEM|2.3.1|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Field Service Management Virtual Conferencing Integration|30.0.0|2026-03-12|
|Outsourced Customer Service|2.1.2|2026-03-12|
|Field Service Contractor Management|30.0.2|2026-03-12|
|Coaching|9.9.0|2026-07-09|
|Document Intelligence for Contract Management Content Pack|1.5.0|2026-07-09|
|FSO - Foundation|1.0.0|2026-04-09|
|Invoice Case Self-Service|1.0.3|2026-05-05|
|Technology Core|3.8.4|2026-06-16|
|sn-app-par-components-info-content|8.4.3|2026-07-09|
|Field Service Manager Mobile|1.1.0|2026-04-09|
|Microsoft Endpoint Configuration Manager Spoke|1.8.1|2025-06-05|
|Cloud Spend Dashboard|1.0.3|2022-06-02|
|UI Components of Collaboration for Configurable Workspaces|9.2.0|2026-06-16|
|Interceptor UI for Service Operations Workspace|9.2.0|2026-06-16|
|OT Manager Foundation|3.3.3|2026-06-16|
|GRC: Advanced Risk|22.3.2|2026-06-16|
|sn-circuit-map|5.0.0|2025-07-31|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|Recommended Actions for OTSM|3.1.0|2026-03-12|
|External Agent Management Util Pack|1.2.0|2025-07-31|
|FSO - Foundation|1.0.0|2026-04-09|
|Service Graph Connector for Microsoft Defender for IoT \(Azure\)|2.0.2|2024-11-07|
|Spoke Generator|4.2.4|2026-03-12|
|Indoor Mapping for Assets|1.0.2|2025-10-16|
|Predictive Intelligence for User Reported Phishing|10.3.7|2024-09-10|
|Service Operations Workspace Admin Center|9.2.0|2026-06-16|
|sn-app-par-components-saved-data-visualization|8.4.3|2026-07-09|
|Azure Active Directory User Mapping|1.11.0|2025-12-11|
|Google Compute Engine Spoke|1.0.5|2024-09-10|
|Related party|1.0.6|2023-02-02|
|Digital Resilience Third-party Information Register|21.1.7|2025-12-11|
|HR Service Delivery Integration with Cornerstone OnDemand|1.2.0|2025-12-11|
|Password Reset for Service Operations Workspace|9.2.0|2026-06-16|
|GRC: Risk Heatmap|22.3.2|2026-06-16|
|Group Life Servicing|2.5.0|2026-03-12|
|Navex EthicsPoint Spoke|1.0.3|2025-12-11|
|OTSM Prime|1.0.1|2026-04-09|
|Workspace App Shell|29.1.1|2026-03-12|
|Task Quality Review Management|29.1.1|2026-03-12|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Hardware Asset Management for Zero Touch Mobility|12.0.0|2025-01-30|
|HR Flow Wizards|1.1.0|2022-05-05|
|Agent Client Collector for Investigation|9.2.0|2026-06-16|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|CISO Dashboard|2.0.5|2025-12-11|
|GRC: Compliance UCF|21.1.0|2025-12-11|
|Password Reset for Virtual Agent|5.0.6|2025-07-31|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Usage Insights Funnel|6.1.12|2026-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|CSM Data Classification|1.0.0|2025-07-31|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|CrowdStrike Falcon Host for Security Operations|10.4.5|2024-11-07|
|Shopping Hub Mobile|7.6.24|2025-07-31|
|Metrics and CI Actions Framework|9.2.0|2026-06-16|
|Now Assist Readiness Evaluation|1.4.2|2026-07-09|
|Analytics Generation|4.1.15|2026-07-09|
|Product Configurator|1.0.1|2024-11-07|
|Order Management Portal|2.1.0|2025-07-31|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Strategic Planning|4.13.0|2026-04-09|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Health Log Analytics|38.0.17|2025-12-11|
|ITSM Enterprise UI Components|3.5.0|2025-12-11|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|Care Team Portal|2.2.0|2026-03-12|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Cloud Action Library|1.4.0|2024-11-07|
|sn-app-kpi-details|8.0.1|2026-03-12|
|Microsoft Endpoint Configuration Manager for Investigation|9.2.0|2026-06-16|
|Indoor Mapping|1.16.8|2026-06-16|
|Usage Insights Commons Connected|6.3.9|2026-07-09|
|Card data security|1.0.1|2025-07-31|
|Industrial Cyber Security Suite Prime|1.0.5|2026-08-13|
|Service Exchange - Prime|1.1.13|2026-08-13|
|sn-app-par-components-scheduled-export|8.4.3|2026-07-09|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|ERP Customization Mining|7.0.5|2025-05-01|
|Compatibility Management|6.6.0|2026-06-16|
|Export entities|3.3.1|2026-06-16|
|Universal Task|2.8.0|2026-06-16|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Meeting Watcher - UI Builder Data Resource|9.2.0|2026-06-16|
|Dynamic Related Records for Configurable Workspace|25.7.0|2026-06-16|
|360 degree relationship visualization|22.3.0|2026-06-16|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Threat Intelligence Support Common UI Components|1.1.4|2025-12-11|
|AI Discovery|2.0.6|2026-04-09|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Whats New Framework Core|1.3.1|2026-03-12|
|Marketplace Core|30.0.1|2026-03-12|
|Operational Technology Manager|4.1.3|2026-08-13|
|External Content Connectors Asana|7.0.7|2026-05-28|
|Industrial Control Tower Foundation|1.0.0|2026-06-16|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Security Operations Setup Assistant|10.4.41|2026-06-16|
|CPQ Configurator|1.4.0|2026-06-16|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Export entities|3.3.1|2026-06-16|
|Critical Event Management|1.2.5|2026-07-09|
|Usage Insights Pages|6.3.9|2026-07-09|
|Conversation Insights|3.1.0|2026-06-16|
|Analytics Toolkit|8.4.3|2026-07-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Usage Insights Commons|6.3.9|2026-07-09|
|service-observability-app|1.10.12|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Customer Service with Service Management|2.0.1|2026-03-12|
|Case Management for Invoice Operations|1.8.0|2026-05-05|
|External Content Connectors Microsoft OneDrive|7.0.7|2026-05-28|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Smart Assessment Core|22.4.0|2026-07-09|
|AI Control Tower for Enterprise AI Foundation|1.2.1|2026-07-09|
|GRC: Business Continuity Planning|11.0.2|2026-06-16|
|Shared Library for Talent Development|2.5.0|2026-06-16|
|Application Intake|29.2.1|2026-06-16|
|Workplace Central|1.16.5|2026-07-09|
|sn-app-par-components-share-info|8.4.3|2026-07-09|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Privacy Employee User|19.0.1|2024-08-01|
|AI Specialists for Security Incident Response|1.0.5|2026-07-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Workplace Service Delivery Professional|1.4.0|2025-12-11|
|Threat Intelligence|13.4.4|2026-02-05|
|Industry Core|1.0.9|2022-12-01|
|Remedial Actions Framework|9.2.0|2026-06-16|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Calendly Spoke|1.2.0|2023-08-03|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Atlassian Jira Integrations Common|2.4.2|2025-12-23|
|Security Operations Reverse WHOIS Integration|10.5.0|2025-12-11|
|Data Model for SBOM|4.2.1|2025-12-11|
|sn-app-par-components-chart-drilldown-configuration|8.4.3|2026-07-09|
|Financial Services Document Management|1.3.1|2022-02-03|
|AWS IAM Spoke|1.1.0|2023-07-06|
|Discovery Admin Workspace|1.17.0|2026-06-16|
|Employee Readiness Core|1.42.0|2025-12-11|
|sn-topology-map|4.0.0|2025-07-31|
|Leader Hub|1.5.0|2026-03-12|
|Process Mining for external data|29.5.0|2026-03-12|
|Order Management for Business Locations|2.0.0|2026-03-12|
|Authentication for conversational channels|1.1.0|2026-03-12|
|Skill Rule|1.0.3|2026-03-12|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|App AutoUpgrade Client|1.0.0|2026-07-09|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|External Content Connectors Wordpress|7.0.7|2026-05-28|
|AI Risk and Compliance Management|22.4.1|2026-07-09|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Value stream artifacts|2.3.0|2026-06-16|
|Shopping Hub|11.1.1|2026-06-16|
|App Best Practices Shared|29.2.0|2026-06-16|
|GRC Feature roles|22.3.0|2026-06-16|
|Attribute propagation|9.4.0|2026-06-16|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Record lookup connected component|28.0.1|2025-12-11|
|Blue Prism Spoke|1.0.2|2022-09-21|
|Slack Activities for PAD|1.0.3|2023-01-12|
|X Spoke|2.3.0|2025-09-10|
|Wrike Spoke|1.3.0|2025-09-10|
|GRC: Common Dashboard Elements|18.1.4|2024-06-06|
|Usage Insights Query Builder Core|6.3.9|2026-07-09|
|Data Collection for Oracle Global Licensing and Advisory Services|1.11.0|2025-12-11|
|Employee Experience VA topics and topic blocks|1.1.2|2023-05-04|
|Financial Services Document Management|1.3.1|2022-02-03|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Healthcare Operations Core|2.3.0|2026-03-12|
|External Content Connectors Sharepoint Online|7.0.7|2026-05-28|
|External Content Connectors Adobe AEM|7.0.7|2026-05-28|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|AI Experience Framework Components|1.2.2|2026-07-09|
|Legal Simple Privacy|1.2.5|2025-12-11|
|DevOps Change Health Scan Content Pack|6.2.0|2025-12-11|
|OTSM Advanced|1.0.1|2026-04-09|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|sn-app-par-components-create-indicator-modal|8.4.3|2026-07-09|
|Application Portfolio Management integration with Risk Management|1.0.2|2023-05-04|
|Industrial Cyber Security Suite Foundation|1.0.3|2026-08-13|
|Employee Experience VA Components|1.0.0|2023-08-03|
|Docusign eSignature Spoke|4.2.2|2026-02-05|
|Digital Signature API|26.0.0|2024-08-01|
|Microsoft Exchange Online Spoke|3.13.0|2026-03-12|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|AI Service Graph Connector for Microsoft|2.0.0|2026-03-12|
|Care Team Portal|2.2.0|2026-03-12|
|Service Catalog for mobile|29.0.7|2025-05-01|
|External Content Connectors Lucid|7.0.7|2026-05-28|
|External Content Connectors|7.0.7|2026-05-28|
|Enterprise Modeling Common|3.8.0|2026-06-16|
|Hiring Core|5.4.1|2026-07-09|
|MSIM VTB Task Card|1.0.1|2024-02-01|
|AI Control Tower|6.0.0|2026-07-09|
|McAfee ePO Integration for Security Operations|10.6.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Conversational Integration with Google Chat|2.0.4|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Invicti Application Vulnerability Integration|1.2.1|2024-11-07|
|Setup Hub Common|4.0.8|2026-08-13|
|Proactive Triggers|3.0.10|2025-12-11|
|Quick links component for Service Operations Workspace|9.2.0|2026-06-16|
|Jamf Spoke|1.2.1|2025-12-11|
|KPI Composer|4.3.1|2025-12-11|
|ITOM Telemetry Ingest|1.0.0|2025-12-11|
|Cloud Workspace|2.2.0|2025-12-11|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Amazon S3 Spoke|1.2.1|2024-09-10|
|Product Offering Recommendations|1.2.0|2025-12-11|
|sn-app-kpi-details|8.0.1|2026-03-12|
|Planned Work Management|2.11.0|2025-12-11|
|sn-app-par-components-insights-panel|8.4.3|2026-07-09|
|Industrial Cyber Security Suite Advanced|1.0.3|2026-08-13|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|GRC: Crisis Management|11.0.2|2026-06-16|
|GRC: Crisis Map|11.0.1|2026-06-16|
|sn-rack|4.0.0|2025-07-31|
|NLU Workbench - Advanced Features|7.0.22|2025-07-10|
|HRSD Process Mining Content Pack|6.0.3|2026-03-12|
|Intent Discovery|3.3.8|2026-05-05|
|External Content Connectors Cornerstone|7.0.7|2026-05-28|
|AI Help Framework|1.0.6|2026-07-09|
|sn-apm-diagram-builder|3.7.0|2026-06-16|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Data Grid UI Component|26.0.7|2026-06-16|
|Workplace Stack Plan|1.5.12|2026-06-16|
|Financial Services Document Management|1.3.1|2022-02-03|
|Business Continuity Management Foundation|1.1.3|2026-06-16|
|Workplace Move Management|1.14.5|2026-07-09|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|sn-app-analytics-center|8.4.1|2026-07-09|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|GRC: Performance Analytics Premium Integration|19.1.0|2024-11-07|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|ServiceNow Studio for App Engine|28.2.1|2025-12-11|
|Microsoft Azure SQL Database Spoke|2.0.0|2024-11-07|
|Platform Analytics|8.4.1|2026-07-09|
|Homepage deprecation help tool|2.0.2|2024-11-07|
|Snowflake Spoke|1.0.3|2025-09-10|
|GRC: Risk Shared Common Components|22.3.2|2026-06-16|
|Risk Assessments for Supplier Lifecycle Operations|4.0.0|2026-06-16|
|Tasks for mobile|27.1.0|2024-11-07|
|Vulnerability Exposure Assessment|5.2.3|2025-12-11|
|Jenkins v2 Spoke|1.2.0|2023-02-02|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|External Trigger Builder|1.1.0|2026-03-12|
|sn-app-par-components-create-dashboard-modal|8.4.3|2026-07-09|
|FDIH Dashboard|25.0.5|2024-11-07|
|Notification Flow Wizards|2.0.1|2022-09-21|
|Software Asset Workspace|11.0.15|2026-07-09|
|Supplier Operations|7.0.0|2026-06-16|
|Collaboration applications - common|1.1.0|2025-12-11|
|Performance Analytics - Content Pack - Guided Tours|1.4.0|2026-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Financial Services Document Management|1.3.1|2022-02-03|
|Product Configurator|1.0.1|2024-11-07|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Software Asset Management integration with Workday|1.0.12|2025-01-30|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Bridge for Public Sector Digital Services \(PSDS\)|1.0.2|2025-05-01|
|Scrum Common|1.4.5|2025-01-30|
|Multi-case creation framework|2.1.0|2025-07-31|
|UiPath Spoke|2.5.1|2025-11-06|
|Field Service NLU Model for Virtual Agent Conversations|1.3.0|2025-07-31|
|Microsoft Dynamics CRM Spoke|1.9.0|2025-11-06|
|AI Agents for Service Exchange Provider|1.1.12|2026-08-13|
|Service Exchange - Advanced|1.1.13|2026-08-13|
|UX Commons|27.0.2|2025-07-31|
|Amazon SQS Spoke|1.0.1|2025-01-02|
|Google Cloud SQL Spoke|1.0.2|2023-09-07|
|Google Cloud Virtual Network Spoke|1.0.5|2023-09-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Slack Chat Connector for Security Incident Management|1.0.1|2025-05-01|
|Observability Commons for CMDB|1.1.0|2023-11-02|
|Learning|5.7.0|2026-06-16|
|Google Identity And Access Spoke|1.1.1|2022-09-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Financial Services Document Management|1.3.1|2022-02-03|
|Digital Signature API|26.0.0|2024-08-01|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|GovNotify Spoke|1.2.0|2025-09-10|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Google Cloud Functions Spoke|1.0.3|2025-06-05|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Product Configurator|1.0.1|2024-11-07|
|Enterprise Service Management Integrations Framework|3.8.2|2025-07-31|
|CMDB CI Class Models|1.87.0|2026-07-09|
|Cloud Services Catalog|1.5.1|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|ATF Test Generator and Cloud Runner|3.1.1|2026-07-09|
|Advanced Work Assignment for Source-to-Pay Operations|3.1.1|2025-12-11|
|Application Portfolio Management integration with Policy and Compliance|1.0.3|2023-05-04|
|FRISS Spoke|1.1.1|2026-03-12|
|Workforce Optimization for CSM Configurable Workspace|5.0.0|2026-03-12|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|External Content Connectors Viva Engage|7.0.7|2026-05-28|
|External Content Connectors Adobe Acrobat Sign|7.0.7|2026-05-28|
|Event Inquiry|1.4.0|2025-07-31|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Customer Success Management|6.6.3|2026-07-09|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Guided Setup|6.0.2|2026-03-12|
|Record Related Items Connected|2.2.0|2025-12-11|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Expanded Model and Asset Classes|2.16.1|2026-05-05|
|Notifications Email Agents|2.2.0|2026-07-09|
|External Content Connectors Notion|7.0.7|2026-05-28|
|External Content Connectors Application Suite|7.0.7|2026-05-28|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Flow Templates for Service Desk|1.0.3|2023-04-06|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Security Operations 'Have I been pwned?' Integration|10.5.1|2025-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Conversational SMS Integration with AWS End User Messaging|1.0.2|2025-01-30|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|DocuSign Activities for PAD|1.1.3|2023-01-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Dun and Bradstreet DirectPlus Spoke|1.0.0|2025-01-30|
|Vulnerability Response Patch Orchestration|2.2.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|@devsnc/behavior-form-intent-translator|29.0.9|2026-03-12|
|Process Mining for external data|29.5.0|2026-03-12|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Docker Spoke|2.3.4|2025-07-10|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|Portal navigation demo|27.0.0|2025-06-05|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|GRC: Business Continuity Management - Core|11.0.1|2026-06-16|
|Vulnerability Response Integration with Tenable|5.2.1|2025-12-11|
|GRC: Workbench|21.1.0|2025-12-11|
|AI Service Graph Connector for GCP Vertex AI|1.0.4|2026-03-12|
|iManage Spoke|1.1.6|2026-01-20|
|Mobile Card Builder|26.12.0|2025-07-31|
|Goal Framework|4.13.0|2026-06-16|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|@devsnc/sn-uibtk-actionable-list-item|29.1.71|2026-03-12|
|UCF Spoke|1.1.0|2023-05-04|
|Compatibility Management|6.6.0|2026-06-16|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|@devsnc/sn-uibtk-mcp-event-definitions-config-pane|29.1.71|2026-03-12|
|AWS OpsWorks Spoke|1.0.2|2023-09-20|
|Amazon DynamoDB Spoke|1.0.1|2022-09-01|
|Task activity timeline|25.4.0|2025-12-11|
|OT Asset Management|2.2.0|2025-12-11|
|@servicenow/sn-next-experience-all-menu-editor|29.1.81|2026-03-12|
|Order to cash common architecture|1.5.0|2026-03-12|
|RAG for code generation|1.1.8|2026-03-12|
|Policy as Code Engine|3.3.0|2026-06-16|
|UI Generation|29.2.5|2026-05-05|
|Chat integration with Security Incident Management|1.2.10|2025-07-31|
|External Content Connectors Jira Cloud|7.0.7|2026-05-28|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|sn-smart-assessment-connected|22.3.3|2026-06-16|
|AI Websearch|4.1.0|2026-06-16|
|Post Assessment Actions for Smart Assessments|22.3.2|2026-06-16|
|CrowdStrike Falcon Sandbox Integration for Security Operations|11.0.10|2024-09-10|
|Google Sheets Spoke|1.0.7|2023-09-20|
|Security Operations RiskIQ Integration|10.4.1|2024-08-01|
|OneLogin Spoke|1.0.2|2023-09-07|
|Vulnerability Response Patch Orchestration with Microsoft SCCM|2.3.1|2025-05-01|
|SCCM Usage Metering Spoke|1.0.2|2023-09-07|
|Rally Spoke|1.0.3|2023-05-04|
|Event Inquiry|1.4.0|2025-07-31|
|Individual Life Claims|1.4.0|2026-03-12|
|Document Processor|1.8.6|2026-07-09|
|Splunk Search Integration for Security Operations|10.5.0|2025-07-31|
|Conversational Integration with Microsoft Teams|10.3.1|2026-03-12|
|Formula builder connected|22.3.1|2026-06-16|
|Digital Signature API|26.0.0|2024-08-01|
|Lead Management Application|5.0.0|2025-12-11|
|Calendar component|26.0.2|2026-03-12|
|Field Service Contractor for mobile|4.8.3|2026-03-12|
|Employee Center Pro|42.0.4|2026-07-09|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Amazon Elastic Container Service Spoke|1.0.2|2023-09-07|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Process Mining Workspace Components|29.7.9|2026-05-05|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|@devsnc/sn-uibtk-toolbox|29.1.71|2026-03-12|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Financial Services Document Management|1.3.1|2022-02-03|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Amazon Route 53 Spoke|1.0.2|2022-12-01|
|GRC: integrations with third-party content|18.1.0|2024-06-06|
|sn-app-par-components-saved-data-visualization|8.4.3|2026-07-09|
|Performance Analytics Content Pack for Agile 2.0|1.4.6|2025-12-11|
|HR Service Delivery Virtual Agent Conversations|24.2.8|2025-05-01|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Industrial Control Tower Prime|1.0.0|2026-06-16|
|Oracle Object Storage Management Spoke|1.0.3|2022-09-21|
|Conversational Analytics|9.1.3|2026-03-12|
|Conversational Integration with Facebook Messenger|3.0.8|2025-12-11|
|GRC: Business Continuity Management User - Lite|5.0.1|2023-08-03|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|ServiceNow Voice for CSM|3.10.0|2026-02-05|
|Emergency Outreach|1.34.0|2025-07-31|
|ServiceNow Otto for Service Exchange|1.1.12|2026-08-13|
|Natural Language Understanding Models for Sourcing and Procurement Operations|2.0.5|2023-05-04|
|Amazon SNS Spoke|1.1.0|2023-09-07|
|Process Mining|29.7.9|2026-05-05|
|Financial Services Document Management|1.3.1|2022-02-03|
|Process Mining Content Pack for CSM|23.2.0|2025-07-31|
|Vulnerability Response Integration with Atlassian Jira|1.0.4|2024-05-09|
|App Engine Management Center|29.2.1|2026-06-16|
|DevOps Vulnerability Integrations|7.0.0|2026-06-16|
|Legal Stock Preclearance|4.9.0|2025-12-11|
|Vulnerability Response Integration with Microsoft Threat and Vulnerability Management|2.8.1|2025-12-11|
|Shodan Exploit Integration for Security Operations|10.8.0|2024-11-07|
|Application spoke selector|1.5.0|2026-03-12|
|sn-component-workspace-shn|29.0.7|2026-03-12|
|Public Sector Digital Services Core|14.1.0|2026-07-09|
|External Content Connectors Miro|7.0.7|2026-05-28|
|Workplace Indoor Mapping|1.18.6|2026-07-09|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Now Assist for Service Graph Connectors|1.1.0|2025-01-30|
|Attribute propagation|9.4.0|2026-06-16|
|API Service Graph Connector for Azure API Management|2.2.0|2025-07-31|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|News Integration for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|External Credential Storage and Management Application|1.3.1|2025-12-11|
|Strategic Portfolio Management - Advanced|1.0.2|2026-04-09|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-app-par-components-share-dialog|8.4.3|2026-07-09|
|Mobile Time Sheets|2.3.0|2025-12-11|
|Product Configurator|1.0.1|2024-11-07|
|Secureworks CTP Spoke|1.0.3|2022-09-21|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Attribute Pack|5.0.0|2025-07-31|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Resolution Shaper|29.0.10|2026-03-12|
|Asset Audits|1.0.0|2026-03-12|
|External Content Connectors Box|7.0.7|2026-05-28|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Rich Text Editor Component for Security Operations|2.0.1|2026-06-16|
|Order Management Portal|2.1.0|2025-07-31|
|Proactive Prompts|3.5.1|2026-06-16|
|GRC: Compliance Assessment|22.3.2|2026-06-16|
|WHOIS Integration for Security Operations|10.4.0|2024-08-01|
|sn-app-kpi-details|8.0.1|2026-03-12|
|@devsnc/sn-uibtk-experience-assistant|29.1.71|2026-03-12|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Enterprise Asset Management for DCNAM|1.0.0|2025-12-11|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|Audio player component|27.3.1|2026-03-12|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Business Portal|2.3.0|2026-03-12|
|Conversation Improvement themes|1.0.8|2026-05-05|
|sn-app-kpi-details|8.0.1|2026-03-12|
|Operational Technology Vulnerability Response|3.2.4|2026-08-13|
|Vulnerability Response Patch Orchestration with HCL Bigfix|1.3.0|2025-05-01|
|@servicenow/sn-builder-core|29.1.59|2026-03-12|
|@devsnc/sn-uibtk-shelf-pane|29.1.71|2026-03-12|
|sn-app-par-components-component-builder|8.4.3|2026-07-09|
|Export entities|3.3.1|2026-06-16|
|AWS Translate Spoke|1.0.0|2022-11-03|
|Google Persistent Disk Spoke|1.0.2|2022-09-01|
|Craft.co Integration for Supplier Lifecycle Operations|5.0.0|2026-06-16|
|Google Cloud Storage Spoke|1.1.1|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Security Case Management common workspace components|2.1.0|2026-06-16|
|External Content Connectors Google Drive|7.0.7|2026-05-28|
|External Content Connectors Amazon S3|7.0.7|2026-05-28|
|External Content Connectors Trello|7.0.7|2026-05-28|
|GRC: Cybersecurity Controls Accelerator|18.1.0|2024-06-06|
|Health and Safety Testing|1.27.0|2025-07-31|
|Confluent Kafka REST Proxy Spoke|1.0.0|2021-03-11|
|Kubernetes Spoke|1.3.0|2025-09-10|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Safe Workplace suite Professional|1.25.2|2025-07-31|
|Skills Industry Data|2.2.0|2026-06-16|
|Mitigation Controls Monitoring|4.1.4|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|App Shell Utils|29.0.0|2026-03-12|
|AI Service Graph Connector for Salesforce|1.0.2|2026-03-12|
|GRC: Audit Management Workspace|22.0.1|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Case Playbook for Onboarding|8.1.0|2025-12-11|
|Carousel component|28.0.1|2026-03-12|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|ReleaseOps|1.2.3|2026-02-05|
|AI Risk and Compliance Integration with Control Tower|22.4.2|2026-07-09|
|BigFix Inventory Spoke|1.5.4|2023-09-07|
|Service Exchange Base|2.3.26|2026-07-17|
|MISP integration for Security Operations|1.4.4|2026-02-05|
|Customer Data Models for B2B2C|2.1.0|2025-07-31|
|CMDB MCP Server|1.0.1|2026-07-09|
|Guided Decisions|38.0.2|2025-12-11|
|Vonage Spoke|1.2.0|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|IntegrationHub Enterprise Flow Wizards|1.0.0|2021-08-19|
|Conversational Help|2.0.3|2026-03-12|
|Asset Management for mobile|27.0.2|2025-07-31|
|Google Cloud Translator Service Spoke|3.2.6|2025-05-01|
|Outlook Actionable Messages|4.7.0|2026-06-16|
|Now Learning Integration|1.0.3|2024-02-01|
|Aha! Spoke|1.7.2|2026-01-20|
|Workspace Builder for App Engine|28.2.0|2025-12-11|
|Security Operations PhishTank Integration|10.5.0|2024-08-01|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|sn-hla-admin-experience|1.0.2|2026-01-20|
|@devsnc/sn-vtb|26.0.0|2025-12-11|
|Resizable panes component|28.0.3|2025-12-11|
|Order Management Portal|2.1.0|2025-07-31|
|Cloud Discovery Workspace|1.7.1|2025-05-01|
|Password Reset integration for Microsoft Active Directory|4.0.0|2025-07-31|
|Case Playbook for Product Support|6.0.1|2025-07-31|
|WSD - Advanced|1.0.2|2026-06-16|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|HR Service Delivery Advanced Integration with Oracle HCM|1.3.0|2025-12-11|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Contractor Service Center|1.0.10|2026-06-16|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|Risk Assessments for Supplier Lifecycle Operations|4.0.0|2026-06-16|
|DLP Incident Response integration with Proofpoint|1.1.0|2025-12-11|
|Secops Health Analytics|2.4.3|2025-12-11|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Order Management Portal|2.1.0|2025-07-31|
|AI Search RAG|6.1.0|2026-06-16|
|MCP Client|1.0.2|2026-07-09|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|ACC Admin Workspace|1.0.0|2025-12-11|
|GRC: Audit Management|22.0.1|2026-03-12|
|Security Operations Spoke|10.6.7|2025-06-05|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Service Graph Connector for OpenTelemetry|1.4.1|2024-05-09|
|ITOM Mobile Agent|1.0.0|2025-05-01|
|Advanced AI Search Management Tools|8.0.1|2025-12-11|
|Threat Intelligence Security Center integration with Microsoft Defender for Endpoint|1.0.4|2025-06-05|
|CPQ - Advanced|1.0.1|2026-04-09|
|Safe Workplace suite|1.34.2|2025-07-31|
|HR taxonomy|1.2.1|2022-12-01|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Performance Analytics for Sourcing and Procurement Operations|3.0.9|2024-08-01|
|Microsoft Azure Notification Hub Spoke|2.0.0|2024-11-07|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Service Graph Connector for Microsoft SCCM|3.8.0|2025-12-11|
|MCP for Strategic Portfolio Management|1.0.2|2026-06-16|
|Conversational Integration with Google Business Messages|1.1.1|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|GRC: Privacy Lite User|19.0.0|2024-08-01|
|Security Incident Response Integration with Palo Alto Networks XSIAM|3.0.2|2026-01-20|
|External Content Connectors ServiceNow Instance|7.0.7|2026-05-28|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|Amazon VPC Spoke|1.0.3|2023-09-07|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|UI Builder|29.1.52|2026-03-12|
|@devsnc/sn-uibtk-mcp-props-config-pane|29.1.71|2026-03-12|
|Configuration Data Management|5.0.2|2024-03-20|
|@devsnc/sn-uibtk-text-link|29.1.71|2026-03-12|
|sn-app-par-components-divider|8.4.3|2026-07-09|
|Security Operations Shodan Integration|10.4.1|2024-08-01|
|Card data security|1.0.1|2025-07-31|
|Individual Life Servicing|2.5.0|2026-03-12|
|Amazon EC2 Spoke|1.4.0|2025-09-10|
|Financial Services Document Management|1.3.1|2022-02-03|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|CDM File Uploader|1.0.1|2023-11-02|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|AES Decision Table Builder Templates|4.0.0|2023-02-02|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|CCG Content Pack|1.3.12|2024-11-07|
|Microsoft Azure Traffic Manager Spoke|2.0.0|2024-11-07|
|Service Graph Connector for Jamf|2.14.4|2025-09-10|
|Oracle Netsuite Spoke|1.0.3|2025-09-10|
|Conversational Interfaces - Diagnostics|2.2.1|2024-11-07|
|Profanity filter for agent chat|3.0.12|2024-11-07|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|API Service Graph Connector for Apigee X|2.2.2|2025-10-16|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Agile Development v2|1.1.0|2023-02-02|
|Virtual Agent API|4.3.0|2026-04-09|
|Virtual Agent Adapter Common|6.2.3|2026-03-12|
|Smart Assessment Migration tools|22.3.1|2026-06-16|
|BCM mobile app|9.1.3|2025-12-11|
|Tasks for mobile|27.1.0|2024-11-07|
|Lead Management Data Model|5.0.1|2025-12-11|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Software Asset Management Guided Experiences|7.0.1|2026-03-12|
|IBM License Compliance for Software Asset Management|6.0.7|2026-03-12|
|Magnit Spoke|1.2.1|2023-09-07|
|@devsnc/sn-uibtk-domain-picker|29.1.71|2026-03-12|
|Okta Spoke|4.7.1|2025-11-06|
|Plivo Spoke|1.2.0|2025-11-06|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Google Cloud Datastore Spoke|1.0.3|2023-09-07|
|Microsoft Azure Automation Spoke|2.0.0|2024-11-07|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|sn-smart-assessment-connected|22.3.3|2026-06-16|
|HR Service Delivery Integration with Workday|3.4.11|2025-12-11|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|Site Reliability Metrics|2.1.7|2023-11-02|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|sn-nlq-analytics|29.0.1|2026-03-12|
|Access Analyzer|6.0.6|2026-05-21|
|Care Team Mobile|1.2.0|2026-03-12|
|DevOps Feature Flag Integrations|7.0.0|2026-06-16|
|DevOps Integrations|7.0.0|2026-06-16|
|ServiceNow Document Designer with Word|22.3.2|2026-06-16|
|CPQ Integration|3.3.0|2026-07-09|
|Legal Simple Intellectual Property|1.6.0|2025-12-11|
|Urjanet ESG integration|21.1.1|2025-12-11|
|GRC: Technology Controls Monitoring Accelerator|21.1.0|2025-12-11|
|GRC: Crisis Management integration with Everbridge Notifications|9.1.1|2025-12-11|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Observability - Dynatrace|1.13.1|2025-09-10|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Theme Builder AI|1.1.0|2026-05-05|
|Live CI View|19.1.2|2023-05-04|
|ACL Assessment for Reports|3.1.2|2025-01-30|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|API Service Graph Connector for AWS API Gateway|2.2.0|2025-09-10|
|Product Configurator|1.0.1|2024-11-07|
|Impact Value Management - CSM|2.1.0|2025-01-30|
|Voice input for Now Assist|1.5.0|2026-07-09|
|Financial Services Document Management|1.3.1|2022-02-03|
|Proactive Service Experience Workflows|8.6.2|2026-07-09|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Hardware Asset Management for TNI|13.0.0|2025-11-06|
|@devsnc/sn-uibtk-conditional-renderer|29.1.71|2026-03-12|
|Recommended Actions for Customer Service|30.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Automation Anywhere Spoke|1.2.1|2025-05-01|
|Retry Handler Framework|1.0.2|2022-09-21|
|Integration Hub Usage Dashboards|3.0.0|2025-07-31|
|Advanced Work Assignment for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|sn-app-kpi-details|8.0.1|2026-03-12|
|Usage Insights Funnel Core|6.3.9|2026-07-09|
|Metadata Search|1.0.12|2026-07-09|
|sn-nlq-analytics|29.0.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|API Insights|2.2.1|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Coaching with Learning Migration Utility|1.0.1|2021-09-16|
|sn-topology-map|4.0.0|2025-07-31|
|Inventory Number Management|5.0.0|2025-07-31|
|Change Password Custom Component|1.3.0|2025-12-11|
|Event Inquiry|1.4.0|2025-07-31|
|Software Asset Management integration with Salesforce Marketing Cloud|1.2.7|2025-03-12|
|sn-circuit-map|5.0.0|2025-07-31|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Document Management|1.3.1|2022-02-03|
|Card data security|1.0.1|2025-07-31|
|Service Mapping Plus|1.17.2|2026-01-20|
|Advanced Response Automation for Smart assessments|22.3.0|2026-06-16|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Sales Forecasting|2.0.1|2025-12-11|
|sn-timer|2.0.1|2026-03-12|
|Task SLA cards|26.0.0|2026-03-12|
|Microsoft Entra ID Spoke|4.7.3|2025-12-11|
|Site Reliability Operations|14.2.3|2024-05-09|
|Milestones|2.9.0|2026-06-16|
|Operational Technology Hardware Vulnerability Assessment|4.1.4|2026-08-13|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Migration Utility for Service Operations Workspace|2.3.1|2025-05-01|
|Agent Client Collector for Security Incident Response|20.2.0|2023-05-04|
|Service Operations Workspace Service Dashboard|27.3.1|2026-07-09|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Data Context Engine|3.3.2|2026-06-16|
|Cisco Webex Teams Spoke|2.3.6|2025-12-11|
|Pattern Designer Enhancements|3.9.0|2025-12-11|
|Stream Connect Designer|5.0.1|2026-03-12|
|sn-app-par-coreui-migration-legacy-widget|4.0.3|2026-03-12|
|GRC Employee User|19.0.1|2024-08-01|
|Oracle Virtual Cloud Network Spoke|1.0.4|2022-12-01|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|ISA Equipment Model|4.1.0|2026-08-13|
|Digital Signature API|26.0.0|2024-08-01|
|File Explorer Component for Security Operations|1.2.13|2025-08-22|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|Guided Decisions|38.0.2|2025-12-11|
|sn-guided-action-experience|39.0.1|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|HR Success Dashboard indicators|1.0.15|2025-05-01|
|Workplace PPE Inventory Management|1.18.0|2025-07-31|
|CrowdStrike Falcon Insight Integration for Security Operations|1.4.1|2026-01-20|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Cloud Access Interface|1.1.3|2026-06-23|
|Industrial Operations Suite Foundation|1.0.3|2026-08-13|
|ServiceNow Kafka Consumer|1.0.1|2023-04-06|
|Employee experience taxonomy|28.2.5|2025-12-11|
|DevOps Data Model|7.0.0|2026-06-16|
|News Integration for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|User Sense|1.1.13|2025-12-11|
|@devsnc/behavior-ui-interaction|29.1.14|2026-03-12|
|sn-app-par-components-data-visualization-wrapper|8.4.3|2026-07-09|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Emergency Exposure Management|1.27.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Microsoft Azure Managed Storage Spoke|2.0.1|2024-11-07|
|Setup Hub Content|4.0.8|2026-08-13|
|Service Graph Connector for GCP|1.11.0|2025-10-16|
|ServiceNow Otto for Setup Core|3.0.7|2026-08-13|
|Total Cost of Ownership|1.1.0|2026-06-16|
|sn-smart-assessment-designer|22.3.1|2026-06-16|
|Supplier Payment Optimization|6.0.0|2026-06-16|
|Release Timeline Component|1.4.0|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|DLP Incident Response integration with Microsoft|1.3.1|2026-01-20|
|Configurable Workspace for Order Management|15.2.0|2026-06-16|
|Operational Technology Incident Management|4.0.0|2026-06-16|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Supplier Common Architecture|11.0.6|2026-07-09|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|Oracle EBS Spoke|1.13.2|2025-07-10|
|GitLab Spoke|2.4.0|2025-11-06|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Order Management Portal|2.1.0|2025-07-31|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|sn-app-par-components-info-panel|8.4.3|2026-07-09|
|CFO Dashboard|2.0.1|2025-12-11|
|Conversational SMS Integration with Twilio|4.2.4|2025-12-11|
|First Advantage Spoke|1.8.0|2025-11-06|
|News Integration for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Cloud Services Catalog Terraform Connector|1.9.1|2025-12-11|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Microsoft Azure DevOps Integrations Common|1.9.0|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|GRC: Financial Services Controls Accelerator|22.0.1|2026-03-12|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Hardware Asset Management for DaaS|12.1.1|2026-03-12|
|AI Search Spoke|2.0.3|2023-09-20|
|AWS Elastic Beanstalk Spoke|1.0.3|2024-06-06|
|Kanban Components|1.2.0|2026-03-12|
|sn-attach-article-guidance|31.0.0|2026-06-16|
|Health and Safety - Advanced|1.0.6|2026-07-09|
|Coaching With Learning|5.4.2|2026-03-12|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Workplace Reservations for Microsoft Outlook Add-in|1.12.2|2025-07-31|
|sn-app-par-components-divider|8.4.3|2026-07-09|
|Security Incident UI Card Component|1.0.1|2023-12-07|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Looker Spoke|1.0.2|2025-01-30|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|GRC Compliance Case Management Full Access|18.1.1|2024-06-06|
|Applicant Center|8.0.2|2026-07-09|
|Event Inquiry|1.4.0|2025-07-31|
|DEX for Zoom|5.0.0|2026-07-09|
|Security Incident Response - Prime|1.0.7|2026-06-16|
|CIO Dashboard|2.1.1|2025-12-11|
|HR Service Delivery Advanced Integration with Workday|2.2.6|2025-12-11|
|ESG Risk Management|21.0.1|2025-12-11|
|Mastercard Spoke|4.0.1|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Engagement Messenger|5.12.1|2026-01-20|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Breakdown Data Grid UI Component|1.4.0|2023-05-04|
|PagerDuty Spoke|1.5.1|2026-01-20|
|Impact Value Management - CSM|2.1.0|2025-01-30|
|Document Service Framework for OneDrive|3.0.0|2025-07-31|
|Agent-Initiated Messaging Interface|1.0.22|2026-03-12|
|Conversational Integration with Alexa|1.5.5|2024-08-01|
|Product Support for Technology|4.3.6|2026-07-09|
|Telecom Service Operations Core|1.2.1|2025-12-11|
|GRC: SIG Questionnaire Integration|21.1.0|2025-12-11|
|Software Asset Management Professional for Engineering Applications|1.0.3|2026-03-12|
|Geo Map component|1.2.0|2025-07-31|
|Process Mining Content Pack for SPM|1.0.2|2026-03-12|
|Document display component|27.0.0|2025-05-01|
|@devsnc/library-uibtk-macroponent|29.1.71|2026-03-12|
|Workday HR Spoke|2.7.0|2025-12-11|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Microsoft Active Directory v2 Spoke|2.5.1|2025-10-16|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Oracle Financial Cloud Spoke|1.2.0|2025-11-06|
|SharePoint Online Search Connector|6.1.2|2024-11-07|
|AI Agents for ACC|1.0.3|2026-04-09|
|Predictive Intelligence Store App|1.0.3|2025-12-11|
|Tasks for mobile|27.1.0|2024-11-07|
|Salesforce Spoke|2.3.4|2025-11-06|
|Agent Client Collector Monitoring|3.16.1|2026-01-20|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Employee Experience Foundation|30.0.3|2025-12-11|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|Customer Household Data Model|2.0.6|2026-03-12|
|Diagram Builder|30.0.0|2026-05-05|
|Impact Value Management - App Engine|2.1.0|2025-01-30|
|Checklist component|26.0.0|2025-12-11|
|Impact Value Management - CSM|2.1.0|2025-01-30|
|Confluence Cloud Spoke|1.2.6|2026-01-20|
|sn-app-par-components-info-content|8.4.3|2026-07-09|
|DevOps Integration with Argo CD|7.0.0|2026-06-16|
|GRC: Advanced Risk Assessment|22.3.2|2026-06-16|
|Financial Services Document Management|1.3.1|2022-02-03|
|Asset Security Posture Management|5.5.1|2025-12-11|
|Service Builder Components|2.2.0|2025-12-11|
|sn-rack|4.0.0|2025-07-31|
|Assist Order Management AI Agent|1.0.1|2026-03-12|
|Opportunity Marketplace|2.7.0|2026-06-16|
|Service Operations Workspace Link View|27.1.1|2026-06-16|
|Impact Value Management - ITOM|3.0.1|2025-12-11|
|Threat and alert data feeds for Crisis Management|11.0.1|2026-06-16|
|Customer Discovery Hub|1.2.2|2026-07-09|
|Customer Engagement Sequences|2.0.1|2025-12-11|
|Process Mining Content Pack for FSM|1.5.0|2026-03-12|
|Enterprise Asset Management for Healthcare Advanced|1.0.0|2026-04-09|
|sn-component-account-hierarchy|29.0.7|2026-03-12|
|telemetry-data-connector|1.2.1|2026-05-05|
|Operational Technology Change Management|4.1.4|2026-08-13|
|sn-component-guidance-experience|41.0.0|2026-06-16|
|sn-smart-assessment-designer|22.3.1|2026-06-16|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|sn-app-par-components-dashboard-categories|8.4.3|2026-07-09|
|Jira Service Management Spoke|1.2.0|2025-10-16|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|AWS CloudFormation Spoke|1.1.4|2024-03-20|
|Industrial Operations Suite Prime|1.0.3|2026-08-13|
|Omnichannel Callback|2.0.7|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Service Graph Connector Licensing|1.0.0|2022-05-05|
|Attribute propagation|9.4.0|2026-06-16|
|Advanced Work Assignment for Supplier Lifecycle Operations|6.0.0|2026-06-16|
|CHRO Dashboard|2.0.4|2025-12-11|
|Security Operations CrowdStrike Intelligence Integration|10.8.0|2025-12-11|
|Obligation Management|1.5.5|2025-12-11|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Reliability Management|7.0.0|2026-06-16|
|External Content Connectors Hubspot|7.0.7|2026-05-28|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|AI Agents for Health and Safety|1.3.4|2026-07-09|
|GRC: Virtual Agent|19.1.0|2024-11-07|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Event Inquiry|1.4.0|2025-07-31|
|Integrated Risk Management Professional|22.3.0|2026-06-16|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Health and Safety - Foundation|1.0.6|2026-07-09|
|Microsoft 365 for ServiceNow Reporting|22.3.1|2026-06-16|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Integrated Risk Management Enterprise|22.3.0|2026-06-16|
|Workplace Concierge|1.7.11|2026-07-09|
|Case Playbook for Complaints|9.1.1|2026-07-09|
|UI shared library|1.6.2|2026-06-16|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Asset Audit Response|2.0.3|2026-07-09|
|Localization Workspace|1.0.6|2025-05-01|
|Sales Cart|2.1.0|2025-12-11|
|Service Graph Connector for ExtraHop|2.0.3|2020-09-16|
|Order Case Playbook|1.4.1|2025-12-11|
|Order Management Portal|2.1.0|2025-07-31|
|Craft Spoke|1.0.0|2024-11-07|
|sn-app-kpi-details|8.0.1|2026-03-12|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|WSD - Prime|1.0.2|2026-06-16|
|CSM Contributor User|2.4.0|2026-06-16|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Telecommunication Open APIs|6.0.9|2025-12-11|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Mobile Publishing|24.0.0|2025-12-11|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Quote Management Data Model|9.0.0|2025-12-11|
|Workplace Space Mapping|1.20.5|2026-06-16|
|Palo Alto Networks NGFW for Security Operations|10.5.2|2025-12-11|
|Now Assist AI Helper - Galileo Inside|2.1.2|2025-10-16|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Manager Hub|4.9.1|2026-06-16|
|Threat Intelligence Security Center for Security Operations|4.7.0|2026-07-09|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Flow Execution Analysis|29.2.8|2026-06-16|
|Manage Order Operations|2.0.3|2026-06-16|
|Sustainable IT|21.1.0|2025-12-11|
|Process Automation Experience Demo|24.1.4|2024-10-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|IBM QRadar Integration for Security Operations|10.3.7|2024-11-07|
|Financial Services Document Management|1.3.1|2022-02-03|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Collaboration UI Component for Major Security Incident Management Workspace|1.2.1|2024-11-07|
|API Notification Management|4.0.1|2025-12-11|
|PSDS - Prime|1.0.1|2026-04-09|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|Quote Management Application|9.1.0|2025-12-11|
|Box Spoke|3.7.1|2026-06-26|
|Redox Inbound Integration|6.0.0|2024-08-01|
|sn-nlq-analytics|29.0.1|2026-03-12|
|Telecommunications Alarm Management Open API|7.0.1|2025-12-11|
|Asset Management - Procurement Integration|1.0.1|2024-11-07|
|AI Service Graph Connector for n8n|1.0.2|2026-04-09|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|sn-nlq-query-input|30.0.1|2026-03-12|
|DevOps Config Exporter Content Pack|2.3.0|2023-08-03|
|Health and Safety - Prime|1.0.6|2026-07-09|
|sn-cmdb-nlq-search|2.3.3|2024-11-07|
|DevOps Config|5.2.0|2024-11-07|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|SuccessFactors Learning Spoke|1.0.0|2025-01-30|
|Customer Request for Quote|1.0.0|2025-12-11|

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)


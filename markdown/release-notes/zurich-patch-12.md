---
title: Zurich Patch 12
description: The Zurich Patch 12 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/release-notes/zurich-patch-12.html
release: zurich
topic_type: reference
last_updated: "2026-08-07"
reading_time_minutes: 85
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 12

The Zurich Patch 12 release contains important problem fixes.

-   **Zurich Patch 12 was released on August 07, 2026.**
    -   Build date: 07-31-2026\_1556
    -   Build tag: glide-zurich-07-01-2025\_\_patch12-07-16-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z12.00.xlsx).

## Overview

Zurich Patch 12 includes 381 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-zp12.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Zurich Patch 12 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 12, refer to [KB3140941](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3140941).

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
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

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

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/available-versions.md)


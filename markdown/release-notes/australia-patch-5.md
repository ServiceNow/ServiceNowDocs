---
title: Australia Patch 5
description: The Australia Patch 5 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/australia-patch-5.html
release: australia
topic_type: reference
last_updated: "2026-08-07"
reading_time_minutes: 118
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 5

The Australia Patch 5 release contains important problem fixes.

-   **Australia Patch 5 was released on August 7, 2026.**
    -   Build date: 08-03-2026\_1111
    -   Build tag: glide-australia-02-11-2026\_\_patch5-07-20-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A05.00.xlsx).

Australia Patch 5 includes 539 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-ap5.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Australia Patch 5 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 5, refer to [KB3138411](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3138411).

## Changes in Australia Patch 5

-   **[Adoption Services release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/adoption-services-rn.md)**

    genai\_admin role in Dynamic Guidance

    The sn\_dyn\_guidance\_user role now includes the role. When you assign sn\_dyn\_guidance\_user to a user, the genai\_admin role is automatically granted.

-   **[Configure](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure.md)**

    When sn\_dyn\_guidance\_user role is assigned, it also includes the genai\_admin role.

    **Note:** The genai\_admin role does not grant administrative privileges.

-   **[Integration Hub release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/integration-hub-rn.md)**

    [OAUTHBEARER authentication for Stream Connect message replication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/hla-data-input-kafka-credentials.md)

    Authenticate using OAUTHBEARER as part of the SASL credential framework for Stream Connect message replication. OAUTHBEARER authentication lets Stream Connect administrators meet customer requirements, improve security, and align with existing OAuth capabilities on the platform, enabling seamless integration with Kafka environments that require advanced authentication.

-   **[Integration Hub Usage Dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integrationhub-usage-dashboard.md)**

    The Integration Hub Usage Dashboard provides reports of usage by protocol. For more information about the service accounts contributing to each protocol, see [Monitor inbound API integration usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/inbound-api-integration-usage-dashboard.md).

-   **[Kafka SSL credentials fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/hla-data-input-kafka-credentials.md)**

    Updates to OAUTHBEARER, Token endpoint URL, Client ID, Client Secret, Scope, and OAUTH extensions.

-   **[Monitor inbound API integration usage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/inbound-api-integration-usage-dashboard.md)**

    Monitor inbound integration usage requests, data egress, and domain-level usage through the Inbound API Integration Usage dashboard.

-   **[Predictive Intelligence release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/predictive-intelligence-rn.md)**

    The sys property ML Trainer - Glide communication KAA \(glide.platform\_ml.kaa\_auth\_enabled\) implements KAA validation when mTLS is enabled.

    Sys property: [ML Trainer - Glide communication KAA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/predictive-intelligence-properties.md)

    A sys property \(glide.platform\_ml.kaa\_auth\_enabled\) implements KAA validation to the ML Trainer server. KAA validation occurs only if mTLS is enabled on the instance. If this property is enabled but mTLS isn't enabled, the KAA validation is skipped. Default value is true \(from the Australia release\).

-   **[Properties for Identification and Reconciliation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/properties-id-reconciliation.md)**

    glide.identification\_engine.batch\_update\_last\_discovered.use\_execute\_lazy

    Sets IRE mode for processing batch updates of the discovery timestamp fields **first\_discovered** and **last\_discovered**.

    For optimized performance, when IRE processes CI records, it updates discovery timestamp fields in batches. This property controls when these batch updates are executed.

    -   **true**

        IRE defers database updates and uses batched operations, which improves performance.

        Usage:

        -   For standard production operations
        -   When performance is critical
        -   When no race conditions are observed
    -   **false**

        IRE processes updates synchronously without delay, ensuring immediate database consistency.

        Usage:

        -   When race conditions between discovery and CI deletion exist
        -   A deletion strategy is aggressively removing recently discovered CIs
        -   If immediate timestamp consistency is required
    General details:

    -   Type: true \| false
    -   Default: true
    -   Learn more: 
    -   Location: [Add to System Properties \[sys\_properties\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md) table.
-   **[Properties for Identification and Reconciliation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/properties-id-reconciliation.md)**

    glide.identification\_engine.batch\_update\_last\_discovered.use\_execute\_lazy

    Sets IRE mode for processing batch updates of the discovery timestamp fields **first\_discovered** and **last\_discovered**.

    For optimized performance, when IRE processes CI records, it updates discovery timestamp fields in batches. This property controls when these batch updates are executed.

    -   **true**

        IRE defers database updates and uses batched operations, which improves performance.

        Usage:

        -   For standard production operations
        -   When performance is critical
        -   When no race conditions are observed
    -   **false**

        IRE processes updates synchronously without delay, ensuring immediate database consistency.

        Usage:

        -   When race conditions between discovery and CI deletion exist
        -   A deletion strategy is aggressively removing recently discovered CIs
        -   If immediate timestamp consistency is required
    General details:

    -   Type: true \| false
    -   Default: true
    -   Learn more: 
    -   Location: [Add to System Properties \[sys\_properties\]](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AddAPropertyUsingSysPropsList.md) table.
-   **ServiceNow AI Platform core feature release notes**

    [Data Egress and Usage by Domain tabs added to the Inbound API Integration Usage dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/inbound-api-integration-usage-dashboard.md)

    View data volumes returned in integration responses and monitor domain-level usage.

-   **[ServiceNow Vault roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/vault-roles.md)**

    Learn and set up the roles necessary to use ServiceNow Vault.

-   **[Using Dynamic Guidance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/using-dynamic-guidance.md)**

    Starting with Dynamic Guidance version 28.4.3, the genai\_admin role is automatically included when the sn\_dyn\_guidance\_user role is assigned. The genai\_admin role does not grant administrative privileges.

-   **[View Inbound API Integration Usage dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/web-services/view-inbound-api-integration-usage-dashboard.md)**

    View integration request counts, data egress volume, and domain-level usage.


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

Database Persistence - WDF

 PRB2024733

 [KB3137449](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137449)

</td><td>

Reports containing reference-type catalog item variables \(lookup\) fail to render data after upgrading to the Australia release

</td><td>

After upgrading to the Australia release, reports that contain reference-type catalog item variable columns fail to render data correctly. The affected reference-type variables don't resolve their lookup values, and their presence in the report additionally causes all other columns — including native table fields such as **Number**, **Created**, and **Closed** — to render as empty across all rows.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB2058369

 [KB3140571](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140571)

</td><td>

MID Server is unable to fetch credentials after upgrading to Zurich or Australia

</td><td>

In certain versions, there's a Unified Secrets Gateway \(USG\) service for credential management. During the upgrade to those versions, a system trigger script is designed to automatically execute and populate the sys\_​secret\_​identity \_​group\_​member table with the MID Server identity group mappings required for USG authentication. However, this trigger fails to complete successfully, leaving the table incompletely populated. As a result, the MID Server can't authenticate with USG and fails to retrieve credentials.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Multi-Instance Framework

 PRB2040054

 [KB3119447](https://hi.service-now.com/kb_view.do?sysparm_article=KB3119447)

</td><td>

There's a flood of 'Unable to find vtable operation for operation id \{\}' messages that's generating millions of records in an instance for every Flow Designer execution

</td><td>

In a cloned instance, the root cause of the flood of errors messages 'Unable to find vtable operation for operation id \{\}' in the syslog is sn\_mif\_vtable\_ operation\_context.vtable \_operation is empty.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now User Experience

 PRB2038702

 [KB3134148](https://hi.service-now.com/kb_view.do?sysparm_article=KB3134148)

</td><td>

A scoped public UI page isn't accessible without a login unless 'Name' is used vs a scoped endpoint in a sys\_public record

</td><td>

It should be accessible without a login, so a user can complete the authentication from Outlook.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Events

 PRB1969068

</td><td>

The 'Events process 0' job yields to memory pressure, causing event processing delays

</td><td>

When node memory pressure is high \(live set ≥ ~91%\), the JobYieldCheck mechanism triggers a yield on events process 0 despite it being a priority 25 \(high priority\) job. High-priority jobs should not be subject to automatic yield throttling, as this directly delays critical event processing and can result in P1 incidents. The memory pressure itself may be transient or difficult to diagnose quickly — heap dumps often show no obvious culprit, and identifying the root cause of elevated memory usage takes time. During that window, events process 0 is repeatedly yielded, stalling event processing pipelines that users depend on for time-sensitive operations. JobYieldCheck WARNING Job=events process 0 yields due to memory pressure logged on affected nodes. Node memory is sustained at 91–93% of max, with live set at ~91.44% \(~1.28GB\). glide.memory.watcher logs no active transaction warnings alongside persistent memory pressure status = true. There's only a single job visible in the queue during the yield window, yet throttling still triggers. However, users expect priority 25 jobs \(events process 0\) should not be yielded under memory pressure conditions. Yield throttling should be restricted to lower-priority workloads.

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

The latest component asset isn't selected when multiple asset associations exist in sys\_​ux\_​lib\_​ component\_​ m2m\_​asset,​ which impacts AI summary cards on UI Builder workspaces

</td><td>

When the AI summary card component was upgraded, its asset name changed from now-ai-summary-card/index to uxc-generative-ai/index. The upgrade doesn't clean up the old asset association, so the sys\_ux\_lib\_component\_m2m\_asset table ends up with two associations for the same component \(old and new asset\). The component-to-asset selection query in Glide​Ux​Component​ Def​Provider.​ get​Asset​Names ​By​Component​Sys​Ids\(\)​ had no ordering and relied on default DB ordering. When duplicate associations exist, this could return the stale now-ai- summary-card/index asset, which is incompatible with the latest Platform AI Agents and Skills app. As a result the AI summary card fails to load on UI Builder workspaces. Classic UI uses a different rendering path, so it is unaffected.

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>## All other fixes

<table id="AllOtherFixes" class="custom-rows"><thead><tr><th class="filter">

Problem

</th><th>

Short description

</th><th>

Description

</th><th>

Steps to reproduce

</th></tr></thead><tbody><tr><td>

Activity Stream

 PRB2027954

</td><td>

An activity filter's field's slushbucket initially has every field selected when the glide.​ui.​\{table\}​\_​activity.​fields property doesn't exist

</td><td>

For non-task tables with an empty 'glide.​ui.​&lt;table&gt;​\_​activity.​fields' property, 'Filter​Field​Repo.​get​Table​Property​Filters\(' returned a hardcoded 'DEFAULT\_FIELDS' constant. This default set was designed for task tables and didn't reflect the actual fields on the table, causing incorrect or missing fields in the activity stream.

</td><td>

1.  Verify that the record is a non-task table record.
2.  Verify that the glide.​ui.​\{table\}​\_​activity.​field isn't set.
3.  On an instance, in UI16, create a interaction record.
4.  Select the **Filter Activity** button, all of the fields should be selected.
5.  Select the **Configure fields** to bring up that the slushbucket now aligns with the fields in the 'Filter Activity'.

</td></tr><tr><td>

Activity Stream

 PRB2040417

</td><td>

The **Copy** button on the VTB view can't access copyJournalContent or GlideUIDefault

</td><td>

The content doesn't get copied to the clipboard API and doesn't show the 'Copied to clipboard' notification.

</td><td>

1.  On any instance, navigate to **All** &gt; **Visual Task Boards**.
2.  Create a freeform board.
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

In most recent Australia release, ServiceNow CSM Workspace agent isn't able to type messages in the chat input box after they are re-routed an interaction that was rejected by a previous agent. The chat box should be enabled after re-routing acceptance.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2031080

</td><td>

Setting 'Disable agent inactivity check for API' to true makes the presence states disappear from the presence state picker in workspace's inbox

</td><td>

The presence state picker should display all available states, even when 'Disable agent inactivity check for API' is set to true.

</td><td>

1.  Log in to an instance.
2.  Navigate to the awa\_presence\_state table.
3.  Select **Update Personalized List** using the gear icon.
4.  Add the 'Disable agent inactivity check for API' column to the list view.
5.  Set the value of 'Disable agent inactivity check for API' to true for the 'Available' presence state.
6.  Navigate to Service Operations Workspace \(SOW\).
7.  Select the inbox icon.

The 'Available' option isn't displayed.

8.  Set the value of 'Disable agent inactivity check for API' back to false for the 'Available' presence state.

 See that the 'Available' option is displayed in the SOW presence state picker.

</td></tr><tr><td>

Agent Chat

 PRB2033499

</td><td>

Improve the presence state picker in workspace's inbox based on the new flag 'show\_in\_workspace' instead of 'Disable agent inactivity check for API'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2051353

</td><td>

Agent presence indicator should be shown in the 'Transfer to Agent' list for third party

</td><td>

When searchTargetList is set, a list of agents is shown, but there's no presence indicator.

</td><td>

1.  Create and offer a third party messaging interaction to a CSM Agent.
2.  Select the **Transfer to Agent** quick action.

 Expected behavior: It shows a list of agents along with presence indicator when searchTargetList is set.

 Actual behavior: It shows a list of agents with no presence indicator when searchTargetList is set.

</td></tr><tr><td>

Agent Chat

 PRB2052028

</td><td>

Integration users can't read sys\_cs\_conversation\_member for creating wrap up segment

</td><td>

The wrap up segment creation fails with a 400 status and the error message: 'Failed to create wrap-up segment. Segment not found in implementations for extension point: interactionSegment'.

</td><td>

1.  Create a third party messaging interaction.
2.  Offer to a CSM Agent.
3.  Call REST API to create a wrap up segment for that interaction and agent.

 Expected behavior: The wrap up segment is created and the API returns success.

 Actual behavior: The wrap up segment creation fails with a 400 status and the error message: 'Failed to create wrap-up segment. Segment not found in implementations for extension point: interactionSegment'.

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

 PRB2055562

</td><td>

Rename of Now Assist, Moveworks and AI experience to ServiceNow Otto

</td><td>

 

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

Agile Development

 PRB2026219

</td><td>

The **Group capacity** field is read only in sprint records

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Navigate to the table 'rm\_sprint.list'.
3.  Open any sprint record.

 Note that **Group capacity** \(points\) is read-only.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2034699

</td><td>

GenAIMetadata M2MDaoImpl createAIAGenAI MetadataM2M doesn't assert that the genAILogId parameter is not NULL

</td><td>

This causes a full table scan of the sys\_gen\_ai\_ log\_metadata table. This code is invoked by the AsyncMessageProcessor.

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

 PRB2034740

</td><td>

aiux\_service/ chat\_check\_access should work with the default experience name to query the deployment document ID

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

 PRB1859571

</td><td>

A search retrieval agent returns an incorrect catalog item URL

</td><td>

 

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

When multiple semantic index configurations are created on the same datasource with the same semantic field name but different embedding models, only the first configuration is loaded into the active semantic index field cache. Subsequent configurations are silently ignored, so ingestion and search only use one embedding model for that field. Only one embedding model is used for indexing and search when multiple semantic index configurations share the same semantic field name. Additional configurations with the same semantic field name are not visible in get​Semantic​Index​Field​Mapping\(\)​.​ No error or warning is logged when the duplicate-name configurations are skipped. Thus, multi-embedding model support for a single semantic field is broken. Configurations are silently lost during cache population. This affects ingestion, search, and any callers that rely on get​Semantic​Index​Field​Mapping\(\)​.​

</td><td>

1.  Create two active ais\_​semantic\_ ​index\_​configuration records on the same datasource with the same semantic\_field\_name but different embedding\_models values.
2.  Add valid component fields via ais\_semantic\_ component\_field for each record and set a valid semantic\_​ snippetization\_​configuration.​
3.  Flush the datasource object cache \(Ais​Configuration​ Cache​Manager.​ flush​Datasource​ Object​Cache\(\)​\)​.​
4.  Call Ais​Configuration.​ get\(\)​.​get​Semantic​ Index​Field​Mapping\('kb\_​knowledge',​'kb\_​knowledge'\)​.​

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
2.  Observe that the conditional filter that gates execution of the synthesized Genius Result on its presence.
3.  Note that this filter only applies to clients using this specific Data Broker transform; it isn't enforced at the Java/API layer.

 A user that bypasses or doesn't use this Data Broker transform doesn't have the filter applied, resulting in potentially inconsistent or unintended behavior around synthesized Genius Result execution.

</td></tr><tr><td>

AI Search UX

 PRB2014714

</td><td>

Ignore Genius Result's limit for citations in sync mode

</td><td>

 

</td><td>

1.  On an AI Search enabled instance with synthesized response configured for portal, navigate to a portal and complete a query that yields a synthesized response.
2.  Set the system property 'glide.​ais.​query.​ disable\_​async\_​mode' to true.
3.  Do same search in portal.

The user should still get a synthesized response.

4.  Open the search application \(presumably NAVA\) and set the Genius Result limit to 1.
5.  Do the same search in portal.

 Expected behavior: Users still get a synthesized response.

 Actual behavior: No Genius Result renders because of no citations.

</td></tr><tr><td>

AI Search UX

 PRB2038703

</td><td>

Instance creation failure for com.​glide.​search.​ graphql.​query.​ Suggestions from service portal's typeahead AIS Suggestions API

</td><td>

When something is searched for in the portal's typeahead, no suggestions appear and AIS Suggestions API calls in the network tab return 'Instance creation failure for: com.​glide.​search.​ graphql.​query.​ Suggestions',​ and 'DataFetchException'.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2054213

</td><td>

URLs with special characters like $ break streaming for non-Virtual Agent clients

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

Replace the sparkle icon animation with the Otto animation for synthesized Genius Results \(GR\)

</td><td>

 

</td><td>

1.  Open an instance with multi-content GR configured.
2.  Navigate to portal/global search.
3.  Search for a query that returns a synthesized GR.
4.  Check the loader in the GR component when the loading state is showing.

 Expected behavior: The loader state shows the Otto animation.

 Actual behavior: The loader state shows the sparkle icon animation.

</td></tr><tr><td>

AI Search UX

 PRB2057349

</td><td>

Rename Now Assist to Otto for typeahead suggestions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Alumni Center

 PRB2054850

</td><td>

Add a null check when using getRefRecord\(\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1973007

</td><td>

The Platform Analytics 'pivot table' unit type doesn't persist

</td><td>

When creating a pivot table using two tables as the data sources, the 2nd and 3rd columns swap their values.

</td><td>

1.  Create a pivot table visualization within a dashboard.
2.  Add in two tables as data sources.
3.  Create four columns on the pivot table, with the first two column being a count of each respective table and the last two columns a sum of all the values with other columns.
4.  Save the visualization.
5.  Exit editing mode.
6.  Refresh the dashboard.

 When the order of the columns is the count of table 1, count of table 2, sum of table 1's column, sum of table 2's column, and when users refresh the dashboard, the 2nd and 3rd columns values swap, with the values from column 3 appearing in column 2 and vice versa.

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

Analytics Data API

 PRB2050449

</td><td>

Next Experience Widgets load with an 'Unable to generate chart' error

</td><td>

The error reads: 'Error Unable to generate chart. Cannot invoke 'com.glide. glideobject. GlideDateTime.after \(com.​glide.​ glideobject. ​Glide​Date​Time\)​' because 'scoresModifiedAt' is null.'.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2053974

</td><td>

Bubble chart bubbles render horizontally in Platform Analytics Workspace \(PAW\) instead of distributed across both X and Y axes

</td><td>

After upgrading to Australia, bubble charts in PAW now render bubbles horizontally \(all on Y = -1\) instead of being distributed diagonally across both X and Y axes as expected. The same configuration in the Classic Reporting module \(sys\_report.LIST\) correctly displays bubbles distributed across both axes. The bubbles are rendering and not stacking, but the axis distribution logic differs between PAW and Classic Reporting. In Classic Reporting, bubbles are positioned diagonally across both X and Y axes. Each rating value \(Dissatisfied, N/A, Satisfied, Very Satisfied\) appears at a distinct \(X, Y\) coordinate pair. In PAW, all bubbles are rendered on the same horizontal line \(Y = -1\), with X-axis variation only. There's no Y-axis differentiation.

</td><td>

1.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**.
2.  Select **Create data visualization**.
3.  Choose **Bubble** as the data visualization type.
4.  Add the asmt\_metric\_result table as the data source.
5.  Add a custom condition: Metric is 'How likely is it that you would recommend this service to others?'.
6.  Select **Run** and then add this source.
7.  In the 'Dimensions' section, set the **Group by** to 'Metric definition' and apply.
8.  Select **Run**.

 Expected behavior: Bubbles should be distributed across both X and Y axes, matching the Classic Reporting output. Each unique combination of Row \(Actual Value\) and Column \(Actual Value\) should result in a distinct \(X, Y\) coordinate pair on the visualization.

 Actual behavior: All bubbles are aligned horizontally at Y = -1, with X-axis values varying. The chart is unreadable and does not match the intended visualization.

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

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Asset Management Common

 PRB2024372

</td><td>

Related lists aren't rendered in Hardware Asset Workspace despite existing in an configuration

</td><td>

Certain related lists such as 'Hardware', 'Software licenses', 'Bundles', and 'Other' assets aren't displayed in Hardware Asset Workspace even though they are present in the Workspace configuration. Analysis confirmed that the related lists exist in the latest configuration \(physical\_asset\_workspace view\) and are conditionally loaded. The issue results in only a subset of related lists being visible in Hardware Asset Workspace while others remain hidden.

</td><td>

 

</td></tr><tr><td>

Asset Management

 PRB2025075

 [KB3052414](https://hi.service-now.com/kb_view.do?sysparm_article=KB3052414)

</td><td>

A catalog task isn't created in Hardware Asset's refresh flow

</td><td>

There's similar issues with the other flows as well, like transfer order, transfer order line, and contract approval.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB2040279

</td><td>

Add bearer token authentication support to Asynchronous Message Bus \(AMB\) client library

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2037251

</td><td>

Update interactions post-identification and authentication

</td><td>

The 'Interactions' table has only 'Guest' resolved. It should have the user reference resolved post-identification and authentication.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2066684

</td><td>

Match KB identification phone numbers are ignoring special characters

</td><td>

Questions with the category 'phone number' aren't matched against formatted stored phone numbers during voice agent identification flow.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2012913

</td><td>

Tests fail with an error: 'Timed out waiting for intent feedback &lt;Intermittent, slow loading forms, SAP&gt;'

</td><td>

When Automated Test Framework \(ATF\) sends an intent to the UXF framework, the intent is received by UXF but is silently terminated/consumed without any feedback being returned to the caller. There's no success response, failure response, error message, or 'action not available' status sent back. Because of this, ATF can't determine whether the request failed due to unsupported actions, missing configuration, processing errors, or temporary issues. This prevents ATF from performing retries, fallback handling, or proper error recovery.

</td><td>

 

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

Business Calendar Filter Options

 PRB1977276

</td><td>

Filter values included with the 'Fiscal Calendar' \(com.snc.fiscal\_calendar\) plugin aren't translated

</td><td>

Filter values included with the 'Fiscal Calendar' \(com.snc.fiscal\_calendar\) plugin aren't translated when users change their language preferences. If a user switches to French \(Canada\), the filter value 'Next 3 fiscal months' should be translated as 'es 3 prochains mois fiscaux'. However, if a user switches to French \(Canada\), the filter value 'Next 3 fiscal months' is actually translated as '3 Fiscal Months suivant'. There are multiple other filter values included with the plugin that are affected.

</td><td>

1.  Provision an instance with a language other than English and the 'Fiscal Calendar' \(com.snc.fiscal\_calendar\) plugin installed.
2.  In English, open any list that can use 'Fiscal Calendar' list filters for a date range.
3.  Set the language to anything other than English.
4.  Refresh the page.

 Notice that the filter value still displays some of the text in English.

</td></tr><tr><td>

Canonicalization Data Services \(CDS\)

 PRB2053470

</td><td>

Data uploaded to cds\_server\_staging table is blocked within instances

</td><td>

This issue occurs in instances where the property 'glide.cmdb.canonical.URL' is set to https:​/​/​&lt;instance\_​name&gt;​.​service-​now.​com/​ and ends with '/'. Unfortunately, that is the base instance value, and it affects the upload portion of CDS.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2023216

</td><td>

Ship the required RCAs per the analysis result

</td><td>

Also, analyze those RCAs for which the analysis result said not to ship. Trigger automation and verify the result if there are any failures.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2023219

</td><td>

Ship the required RCAs as per the analysis result

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2025681

</td><td>

Due to 'getRefRecord', a RCA is generated in the Oracle HCM job execution that should be marked as 'Allowed'

</td><td>

Due to the use of 'getRefRecord' in the script include, a RCA record is generated with the source scope as: 'HR Service Delivery integration with Oracle HCM'. the target scope as 'Human Resources: Core', the target as: 'Table: HR Profile', and the operation as 'Read' after running the Oracle HCM job. This RCA should be marked as 'Allowed' and pushed to the repo.

</td><td>

1.  Provision an instance with Oracle HCM related plugins installed.
2.  Navigate to the Oracle HCM Cloud Integration Source record.
3.  Ensure that on the Integration Service record, **Workers** is active.
4.  Select the **Run Job** button.

 After some time, the RCA record is generated when 'Job Transform Map' starts running. This RCA is created by the source 'Script Include: OracleHCMJob TransformHelperSNC' where 'getRefRecord' is used.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2028299

 [KB3061412](https://hi.service-now.com/kb_view.do?sysparm_article=KB3061412)

</td><td>

In Platform Analytics, an ACL isn't letting an admin user modify or create data visualizations in dashboards or data visualizations

</td><td>

When editing any visualization in a dashboard with the sn\_hr\_er\_case table as a data source, the visualization can't access its data source. As a result, metrics are turned off and can't be edited, preventing updates or modifications to the visualization. There is error: 'You don't have access to the data source used in this visualization'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2055197

</td><td>

In Alumni Center, update RCAs in HR Core for the getRefRecord\(\) for Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2035555

</td><td>

The 'All' filter on the 'Create Change' page doesn't display all standard change templates when a template has no category or catalog

</td><td>

When the 'All' filter is selected for standard change templates on the 'Create Change' page, not all templates are displayed. This is because one template has no category. The null category errors the 'can category be read by user' check.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2035924

 [KB3093597](https://hi.service-now.com/kb_view.do?sysparm_article=KB3093597)

</td><td>

Standard changes created from a problem aren't linked to the parent task

</td><td>

The issue is reproducible if users untick the 'Two step' checkbox under **Change** &gt; **Administration** &gt; **Standard Change Properties** and then perform **cache.do** &gt; **Clear Cache**. A standard change created from a task \(incident/problem\) aren't linked to a parent task. If users **Check Conflicts** before saving a child change from a project requested item, it won't attach the change to the parent item.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2052987

</td><td>

NewChangeRedirectProcessor only checks the system-wide glide.ui.polaris.experience property and ignores per-user glide.ui.polaris.use preference when deciding Next Experience redirect for Create Change

</td><td>

The file app-itsm/glide-service-mgt/ src/main/plugins/ com.snc.change\_request/ update/sys\_processor\_ 0af16f2d53631010 34d1ddeeff7b12b6.xml \(NewChangeRedirectProcessor, path new\_change\_redirect\), line 76: var polarisEnabled = 'gs.​get​Property\('glide.​ui.​polaris.​experience',​ false\) === 'true';' — only reads instance-wide sys\_property, ignores per-user preference glide.ui.polaris.use \(sys\_user\_preference table\), the documented mechanism for per-user Next Experience toggle. The user opted out at a user level, but still was redirected into Next Experience's create-change flow when the system property is on. polarisEnabled check should account for both glide.ui.polaris.experience \(system\) and glide.ui.polaris.use \(user preference\) — not the system property alone.

</td><td>

1.  Turn on the system property glide.ui.polaris.experience = true and com.​snc.​change\_​ request.​next\_​ create\_​page = true.
2.  Set the sys\_user\_ preference glide.ui.polaris.use = false for a specific test user \(system unchecked, User = test user\).
3.  Log in as that user.
4.  Trigger **Create New Change** \(module or UI action\) so the request hits the new\_change\_redirect processor.
5.  Observe the redirect.

 Expected behavior: The redirect respects the user-level opt-out and goes to sn\_chg\_model \_ui\_landing.do \(UI16\).

 Actual behavior: The redirect goes to now/​change-​management/​create-​change/​ \(Next Experience\), ignoring the user preference.

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

CMDB Identification and Reconciliation

 PRB2021886

</td><td>

Null dbquery results must be preserved as null instead of wrapped

</td><td>

 

</td><td>

Run a payload for a non-existing table that has a sys\_id in the payload.

 Where encryption wrappers are constructed, dbq.execute\(\) would normally return null when querying this non-existent table. Now, code is wrapping the null.

</td></tr><tr><td>

Column Level Encryption

 PRB2005360

</td><td>

On an encrypted **HTML** field, getElement\(fieldName\) returns a GlideElement with a value of 'null' instead of an empty string \(''\), causing the condition ge == null to evaluate as true

</td><td>

The field value conversion logic checks for encryption before validating whether the value exists. When encryption is enabled on an empty field, the system attempts to process a null value through the encryption path, which returns the literal string 'null' instead of handling it as an empty value.

</td><td>

 

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

 PRB2026628

</td><td>

getRefRecord\(\) scoping bypass due to directive changes

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
3.  Allow the job to run until the five minute batch timeout fires MID-loop.
4.  Observe the checkpoint value stored in MetricProcessorStatus for that class — it's an arbitrary sys\_id, not the lexicographically highest one processed.
5.  On the next scheduled run, observe that orphan CIs with sys\_ids smaller than the stored checkpoint are not evaluated and not reported as failures.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2037178

</td><td>

A relationship editor \(child\) entry incorrectly displays a '\*' suggested marker when only the parent direction is configured in cmdb\_rel\_type\_suggest

</td><td>

After upgrading from Yokohama to Australia, the CI relationship editor's 'Suggested relationship types' list displays both the parent and child directions of a configured suggested relationship with the '\*' suggested marker, even when only one direction was configured in the cmdb\_rel\_type\_suggest table. For example, a cmdb\_rel\_type\_suggest record is created with base\_class = Windows Server, dependent\_class = Business Service, and direction Connects to \(parent\). When the relationship editor is opened for a Windows Server CI, the list shows two entries instead of one: \* Connects to::Connected by \(Parent\) and \* Connects to::Connected by \(Child\). Both entries appear with the leading \*, suggesting both directions are configured. Only the \(parent\) direction was actually configured. Users selecting from the suggested list can't distinguish which direction was the configured one. Because the list is sorted alphabetically and the \(Child\) entry sorts before \(Parent\), the misleading default selection can result in CI relationships being created in the inverse direction of the customer's intent — silently introducing incorrect CMDB data. The \* suggested marker should only appear on the direction that is actually configured in cmdb\_rel\_type\_suggest. The \(Child\) entry for a parent-only suggested relationship should either not appear in the suggested-marker group, or appear without the \* prefix.

</td><td>

1.  Navigate to the 'Suggested Relationships' module.
2.  Insert a record using an unused relationship.
3.  Open the relationship editor from the relationships formatter on a Windows server CI.

 Expected behavior: Only the added suggested relationship from one direction is expected.

 Actual behavior: Observe two relationship choices for the relationship.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2052583

</td><td>

References to 'Now Assist' for the duplicate CI remediator should be renamed to Otto

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Connections and Credentials

 PRB2034770

</td><td>

A scoped app is unable to update the http\_connection record

</td><td>

Scoped applications need to update http\_connection records that they themselves created and own. Because the table-level ACL blocks all cross-scope writes, there's currently no supported path for a scoped app to modify its own connection records. The http\_connection table is a platform \(global\) table whose cross-scope access policy grants only read access to all application scopes. In the earlier ServiceNow-managed scoped app flow, Claroty CTD via Service Graph Connector relied on the existing platform-owned Connection and Credential creation path to create http\_connection and related credential records. The available scriptable sn\_cc.ConnectionBuilder APIs cover create scenarios such as createConnectionAlias and createConnectionAndCredential, so the absence of a scoped update path didn't surface when the use case was limited to creation.

</td><td>

1.  Navigate to Service Graph Connector for Claroty CTD.
2.  Create a connection with the provided connection\_url.

 Expected behavior: It should be able to update the connection record for the child sys\_alias's http\_connection record.

 Actual behavior: Updating on http\_connection isn't allowed from any scoped app due to tables's cross-scope access policy.

</td></tr><tr><td>

Content Experiences

 PRB2036902

</td><td>

A change in HRApprovalAccessUtilsSNC causes schedule content approvals to fail without a new RCA

</td><td>

 

</td><td>

1.  Provision an instance with HR Core installed.
2.  Create a schedule with approvers such that one rejection rejects the whole schedule.
3.  Approve any number of the requests, saving at least one \(0:X-1\).
4.  Reject one.

 Expected behavior: The schedule is rejected as normal.

 Actual behavior: An RCA error occurs.

</td></tr><tr><td>

Content Experiences

 PRB2054955

</td><td>

RCA for app-ex-ai-agents in Content Publishing for the getRefRecord directive

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Contract Management

 PRB2040201

 [KB3140742](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140742)

</td><td>

Assets covered on a contract aren't added through an Multiple Record Associator \(MRA\) pop-up

</td><td>

In the 'add action' over MRA pop-up, there's a slight change by the platform. It is now performing a GlideRecordSecure insert instead of GlideRecord. It is validating for create and write ACLs on clm\_m2m\_contract\_asset.asset and clm\_​m2m\_​contract\_​asset.​contract fields. There's ACLs where it allows the respective operations only if they are blank. This is clearing out the **Contract** and **Asset** field values during creation. So, records which are created don't have these fields and aren't displaying in the related list.

</td><td>

 

</td></tr><tr><td>

Contracts Core

 PRB2036700

</td><td>

Add the needed RCA as part of the getRefRecord\(\) scoping bypass directive changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Conversational Appointment Booking

 PRB2054247

</td><td>

True-up Conversation Appointment Booking for GetRefRecord directive changes

</td><td>

After making the required changes as part of the directive, all the three flows \(schedule an appointment, reschedule an appointment and cancel an appointment\) should work when the caller scope access is restricted.

</td><td>

 

</td></tr><tr><td>

Customer Operations for Customer Service Management

 PRB2035611

</td><td>

Fix GetRefRecord scoping bypass

</td><td>

On CSManagementUtils, guard the getRefRecord\(\) result before calling getLabel\(\) to prevent an error when a reference field has no associated record. Also, on CSQueryBRUtil, add a null check on entityGR before calling isValid\(\) to prevent an error during dot-walked field validation.

</td><td>

 

</td></tr><tr><td>

Customer Service Case Action Status

 PRB2011771

</td><td>

Keep the 'Major Case' related list consistent in app-csm-action-status and app-major-issue-management

</td><td>

If users reinstall or upgrade app-csm-action-status again after Major Case is installed, the related list on Major Case is different. The newly added-in app-major-issue-management is gone.

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

Database Persistence - Data Access

 PRB2013282

</td><td>

Columns are created with a 'u\_' prefix

</td><td>

After Table​Schema​Manager .​alter\(\)​.​execute\(\)​ adds a column, TableDescriptor returns the new column but the column name is different from what was supplied. The new column was created with a 'u\_' prefix in the column name. This behavior is different from table creation, where columns are created with exactly the same name supplied for column\_name.

</td><td>

1.  Alter a table using the 'Table Management' API.
2.  Add a column.

 Expected behavior: Create a column exactly as specified.

 Actual behavior: It adds a 'u\_' prefix to the column.

</td></tr><tr><td>

Database Persistence - Data Dictionaries

 PRB2050936

</td><td>

Let the 'Table Management' Java API create a table/column in a scope without a scope prefix

</td><td>

MetricBase must create tables in the DEX scope without applying the scope prefix, as it applies the mb\_ prefix to metricbase table. The API should be changed and require a scope object by default.

</td><td>

Use the TableManagement Java API to create a table in any custom scope.

 Observe that a scope prefix is added to the table.

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

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferrable serialization of the query. Cypher's toLower\(\) and toUpper\(\) functions aren't supported anywhere in the builder — neither in WHERE predicates nor in RETURN projections.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2026589

</td><td>

COUNT\(DISTINCT x\) can't be represented with GraphQueryBuilder API

</td><td>

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferrable serialization of the query. Aggregate\('COUNT', x\) only ever emits COUNT\(x\). There's no way to express COUNT\(DISTINCT x\), which is the only correct answer when multiple paths can reach the same node.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2026590

</td><td>

ORDER BY isn't stored in Encoded QueryModel

</td><td>

After creating a query with GraphQueryBuilder, users of GraphQueryBuilder API should be able to get the encoded query representation as a transferrable serialization of the query. RETURN alias — the AS clause is dropped when using buildEncodedQuery\(\), so any consumer of the encoded query has no way to know what column name the user asked for. ORDER BY / LIMIT / SKIP — these have no representation in QueryModel at all, so they're dropped whole on round-trip.

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

Database Persistence

 PRB2029202

 [KB3092221](https://hi.service-now.com/kb_view.do?sysparm_article=KB3092221)

</td><td>

RaptorDB has an auto-increment column reset with a '0' value

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1931544

</td><td>

Users should be warned/blocked from setting up a reference field that is ineligible

</td><td>

As of Australia, it currently enforces the reference key assignment only in the WDF Hub mapping page and not on sys\_dictionary or sys\_db\_object. When creating/editing the remote table through the hub, there's a method called 'com.glide.datafabric. schemamapping. Remote​Table​Def\#validate​Reference'.​ This method verifies that the reference table and the reference key are valid. If the reference table table doesn't exist/cannot be accessed, or if the reference key's data type is not in the list of allowed types, it blocks the table from being created/updated and throws an error message to the user in the UI. Following this approach, it can add the null value check in this method and throw the appropriate error message to the user.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2038399

</td><td>

There's a pagination issue

</td><td>

 

</td><td>

1.  Open the 'List' view of a data interface.
2.  Order by one column.
3.  Navigate to the next page.
4.  Check the data.

The same page is displayed.


 See that the limit isn't applied to the query.

</td></tr><tr><td>

Database Persistence - WDF

 PRB2040034

</td><td>

In Australia, all database columns that start with a number have 'yy\_' added to the start of the name, causing a syntax error

</td><td>

When querying a table in the Australia release and the DB column starts with a number, it adds a 'yy\_' to the SQL query, breaking the collection of data and making a list view show nothing. Error: 'Syntax Error or Access Rule Violation detected by database \(ERROR: column x\_​snc\_​potatofarm \_​0\_​farmers0.​yy \_​1stname does not exist. Hint: Perhaps you meant to reference the column 'x\_​snc\_​potatofarm \_​0\_​farmers0.​1stname'.​ Position: 259\)'.

</td><td>

1.  Create a scoped app.
2.  Create a table.
3.  Create some data on that table.
4.  Add a column that name starts with a number.
5.  Navigate back to the list view.

 See that its blank, but the count displays that there's records.

</td></tr><tr><td>

Database Persistence - WDF

 PRB2050923

</td><td>

Provide unified server-side API's fetch primary key details for Data Fabric and standard ServiceNow tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2052538

</td><td>

Data interface tables are unable to fetch data with remote table as the implementation

</td><td>

Current remote table support requires that the vtable is provider backed.

</td><td>

1.  Open a remote table.
2.  Create a data interface table with the fields matching with the remote table.
3.  Navigate to 'Interface M2M'.
4.  Configure the m2m mappings.
5.  Navigate to the &lt;new\_table&gt;\_list.do.

 Expected behavior: The table displays the data.

 Actual behavior: No data is displayed.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB2018015

</td><td>

The Zero Copy Connector \(ZCC\) Hub UI becomes unresponsive/times out if a large number of schemas and tables are retrieved

</td><td>

When large amounts of schemas and tables \(~20k\) are retrieved in an API call, the function 'refreshSchemasAndTables\(\)' takes a long time to execute compared to the underlying persistence API 'GlideDataFabric EngineService. getInstance\(\). getAllTablesForCatalo'. This is on the magnitude of 2.25 seconds vs 40 seconds.

</td><td>

1.  Navigate to ZCC Hub on an instance.
2.  Create a connection with large number of schemas and tables \(~20k schemas and tables\).

 Expected behavior: The 'Data Assets' page loads schemas and table and is responsive.

 Actual behavior: The 'Data Assets' page times out during loading.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2031050

</td><td>

The 'Run Once Data Privacy' job takes days to complete after segment creation on large tables \(300M+ records\)

</td><td>

 

</td><td>

1.  Provision an instance with the Data Privacy plugin installed on a large clone.
2.  Set up a privacy configuration on a table with a large number of records \(300M+\).
3.  Configure a 'Run Once' dp\_job and trigger it.

 Expected behavior: The job should complete within a few hours after segment creation \(dp\_work\_item\).

 Actual behavior: The job takes days to complete.

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

 PRB2032551

 [KB3140437](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140437)

</td><td>

LLM prompt creation takes ~800 ms, though it used to be 200-300 ms

</td><td>

The root cause was determined as the introduction of 'Sensitive Data Trail system processors', which had a large default timeout \(20 seconds\). The processors were scanning all 32 data patterns on an prompt of ~130K characters, taking an additional ~400 ms in latency.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2039058

</td><td>

Real time anonymization \(RTA\) for child tables separate from parent tables

</td><td>

This is a product update.

</td><td>

 

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

Data Product Backend Services

 PRB2027724

</td><td>

Users are unable to edit reference type details on DTT when editing a data interface

</td><td>

There's no error, but it doesn't work.

</td><td>

 

</td></tr><tr><td>

Data Snapshots

 PRB1995292

</td><td>

A data snapshot indicator timeseries API returns empty data instead of the expected single-span score when the request startTime and endTime are the same date

</td><td>

 

</td><td>

1.  Configure a data snapshot indicator \(pa\_datasnapshot\_indicator\) with a boolean condition.
2.  Send a POST request to /api/now/analytics/data with a timeseries data configuration where:
    1.  The startTime and endTime are set to the same date/time
    2.  A business calendar is used
    3.  The date falls within a valid span for that calendar period
3.  Observe the API response data array.

 Expected behavior: The API returns the single-span score for the calendar period that covers the requested date.

 Actual behavior: The API returns an empty data array — the single span covering the requested date is silently truncated/ignored.

</td></tr><tr><td>

Date Picker

 PRB2029576

 [KB3061444](https://hi.service-now.com/kb_view.do?sysparm_article=KB3061444)

</td><td>

There's a regression on GlideDateTime.setDisplayValue

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

The UI action calls AssetAutomationAPI. completeAssetDisposalTask. This has current.update, which fails. If the read-only flag is removed from the **Stage** field in the sn\_hamp\_m2m\_hw \_asset\_disposal table, then it works.

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

Developer App Shell

 PRB2052364

</td><td>

Fix GetRefRecord scoping bypass

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Developer Sandboxes

 PRB2054240

</td><td>

The scheduler claim mutex \(sys\_mutex\) isn't sandbox-aware and forces DSB nodes to contend for a cluster-wide lock, causing scheduled-job pickup delay

</td><td>

 

</td><td>

1.  On a multi-node instance \(50+ nodes\), turn on Developer Sandboxes.
2.  Create at least 20-30 sandboxes.
3.  Multiple isolated sys\_triggers should exist in the sandboxes.
4.  Pull stats.​do?​include=​otel.​scheduler\* on the sandbox's node.

Observe that claim\_lock\_time averages above one second \(expected ~13ms\), jobs\_lateness averaging 300+ seconds, and worker capacity used is very low.

5.  Compare against a controller node on the same instance.

Claim\_lock\_time is still elevated but jobs\_lateness stays within a few seconds, because base nodes don't pin an entire platform triggers on one node.


</td></tr><tr><td>

DevOps Change Velocity

 PRB2052626

</td><td>

GetRefRecord scoping bypass for the 6.2.1 release

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB2015204

</td><td>

Update the IP address to retired when the network interface card's \(NIC\) is updated to 'Retired'

</td><td>

In the IP-Based Discovery plugin, the business rule \(BR\) 'Discovery - Set IP Address to Absent' only sets the IP address to absent. When the NIC is retired, it doesn't set the IP address to 'Retired', leaving orphaned or outdated IP addresses. The BR should handle the retired scenario as well.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB2023232

</td><td>

Some Sybase processes running on Linux don't meet the classifier conditions to trigger the sybase pattern, resulting in an incomplete Discovery

</td><td>

The Sybase Process classifier has these conditions: Command contains 'dataserver', parameters contains 'sqlsrvr', and parameters matches regex '-\[Dd\]\\s+'. The regex breaks down as follows: -\[Dd\]\\s+ matches a literal hyphen, \[Dd\] matches either uppercase D or lowercase d, and \\s+ matches one or more whitespace characters \(space, tab, etc.\). It matches a hyphen, followed by D or d, followed by at least one space. If a process running returns a parameters string starting with \['parameters':​'-​d/​data/​master.​dat\]​ this doesn't meet the condition for this regex and the pattern doesn't trigger, despite the process being a valid Sybase process.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB2029641

</td><td>

Update Store app true-up for ITOM Licensing Store app 3.13.0

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB2059465

</td><td>

Discovery patterns fail to launch for sub-accounts/datacenters when glide.​discovery.​ retire\_​stale\_​accounts is turned on

</td><td>

In Cloud Discovery, schedules configured to discover all sub-accounts under a master account, with enabling glide.​discovery.​retire\_​stale\_​accounts and glide.​discovery.​cdu.​ auto\_​refresh\_​sub\_​accounts \_​and\_​ldcs , Discovery patterns fail to launch for sub-accounts/datacenters \(only the service account discovery launches\).

</td><td>

 

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

Dynamic Schema

 PRB2037531

</td><td>

There's failing DynamicSchema aggregate ITs

</td><td>

In Australia, in the db-dynamic-schema-test package, the following ITs are failing: DynamicSchemaAggregatesIT and DynSchQueryAggregates\*IT. The expression added to the GROUP BY isn't listed in the SELECT clause.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1948259

</td><td>

SelectAll and **Delete** buttons aren't working in Email Viewer

</td><td>

 

</td><td>

1.  Log in as an admin user.
2.  Navigate to CSM Workspace and open a case record.
3.  From mini composer, send an email with some documents attached.
4.  Update the email status to 'sent' from send-ready in the sys\_email.list table.
5.  Open the email from the 'Emails' tab in the case record.

The email opens in the Email Viewer view


 Expected behavior:**SelectAll** should select all the attachments. The **Delete** button should delete the selected attachments.

 Actual behavior:**SelectAll** isn't selecting all the attachments. The **Delete** button isn't functioning properly.

</td></tr><tr><td>

Email Notifications

 PRB2001946

</td><td>

The **RemoveAll** button shouldn't be present in the email viewer

</td><td>

 

</td><td>

1.  Log in as an admin user.
2.  Navigate to Customer Service Management workspace.
3.  Open a case record.
4.  From the mini composer, send a email with some documents attached.
5.  Update the email status to 'sent' from send-ready in the sys\_email.list table.
6.  Open the email from the 'Emails' tab in the case record.
7.  Select **Select All**.
8.  Select the **3 dots** and verify.

 Expected behavior: The **RemoveAll** button shouldn't be present in the email viewer.

 Actual behavior: The **RemoveAll** button is visible in the email viewer.

</td></tr><tr><td>

Email Notifications

 PRB2019162

</td><td>

Introduce batch support for subscriptions in NotificationRecipientBuilder

</td><td>

Notification events are taking a longer time to process \(5-7 seconds\).

</td><td>

1.  Log in to an instance.
2.  Create a subscribable notification record.
3.  Create 1800+ subscriptions.
4.  Trigger a notification.

 Expected behavior: The notification should be sent to all recipients without much delays.

 Actual behavior: The notification is generated but its processing consumed a significant amount of time.

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
5.  Add one of the contacts created as the case contact.
6.  Send an email to that contact.
7.  Open the sent email.

 Expected behavior: Only one contact is displayed in the**To** field.

 Actual behavior: The**To** field lists all the contacts with the same name and email address.

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

Employee Profile

 PRB2011497

</td><td>

There's a dot-walking RCA error when moving from the 'Learning' scope to the 'Employee profile' scope

</td><td>

An attempt to dot-walk to table sn\_employee\_profile present in the 'Employee profile' scope from the 'Learning' scope was blocked. The reference field employee belongs to the sn\_lep\_challenge table. The operation type was: GET\_REF\_RECORD.

</td><td>

 

</td></tr><tr><td>

Employee Profile

 PRB2021875

</td><td>

getRefRecord\(\) changes for Opportunity Marketplace \(OPM\) and TD Core in Employee Profile

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB2034593

</td><td>

An event field mapping rule from the type 'Map field' using regex causes an error in event processing

</td><td>

When having an event field mapping rule from type 'Map field' using regex and a matching event is processed, if the **Additional info** field contains the source field JSON as the value, the event finishes in an error state.

</td><td>

1.  Create some event field mapping rule from the type 'Map field' using regex.
2.  Create an event with **Additional info** containing nested JSON, where one of the keys matches the regex and its value is a JSON object.

 Expected behavior: Event processing should complete successfully without errors and an alert should created.

 Actual behavior: Event processing fails, and the event is moved to the error state.

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

Field Service Task Bundling

 PRB2064856

</td><td>

Dynamic bundling creates unassigned bundles

</td><td>

 

</td><td>

1.  Verify that Dynamic Scheduling, Task Bundling, and Task Grouping plugins are active.
2.  Enable the sys\_property 'com.snc.dynamic. scheduling.bundle\_ before\_scheduling'.
3.  Set the Task Grouping rules \(Same Location\) and policy.
4.  Create two work order tasks \(WOT\) in the draft.
5.  Once the WOTs are moved to the 'Qualified \(Pending Dispatch\)' state, the tasks should be bundled using Dynamic Bundling and Dynamic Schedule the tasks automatically.

</td></tr><tr><td>

Flow Engine

 PRB1943894

</td><td>

Looping over records using 'built in iterator' is significantly slower than the normal GlideRecord iteration

</td><td>

Flow engine should take a similar amount of time to iterate over records and script or Java when no quiescing occurs, but run times are 16.8x - 73.6x slower.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2001686

</td><td>

There's multiple queries to fetch a flow plan record

</td><td>

When the plan isn't cached, it takes two queries. When run again with the plan already cached, it takes only one query.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2001694

</td><td>

Reduce multiple sys\_flow\_context select queries

</td><td>

In GlideRecord, before updating, it queries to get the DB state of the record to populate the 'previous' object for business rules. This can be avoided if 'fPopulatePrevious FromMemory' is set to true. It can be set by calling Glide​Record:​:​ set​Populate​Previous​ From​Memory.​

</td><td>

1.  Create any simple flow.
2.  Execute it in background scripts.

 Observe that there is 'select query' before every update.

</td></tr><tr><td>

Flow Engine

 PRB2029887

</td><td>

Flow engine is ~200x slower than the equivalent script on 1000 elements, as eager Val.displayValue dominates input wrapping for large collections

</td><td>

A flow that takes a large ComplexObjectCollection as input executes ~200x slower than the equivalent Rhino background script doing the same work. For a 1000-element ForEach input, per-invocation wall-clock is ~143 ms \(vs ~0.7 ms for the equivalent script\). The slowdown scales with the input collection size; small inputs are affected less, but flows that pass large lists as input are heavily impacted even on the user-default execution path \(reporting off, trace off\). There's no functional break as the flow produces correct output, but the per-invocation cost is dominated by work that the engine never reads on the default path.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2034134

</td><td>

'Require' statements throw a JavaScript exception error in Australia's Flow Designer

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2038121

</td><td>

Restore the Flow Engine FlowObjectDef cache

</td><td>

This removes redundant sys\_hub\_action \_type\_definition read per quick-action execution.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2054195

</td><td>

The 'ForEach' iteration on GlideRecord does eager canRead checks on all the records

</td><td>

 

</td><td>

1.  Create a subflow.
2.  Add a **lookuprecords** action on the sys\_user table with active = true and a max count of 10.
3.  Add ForEach flow logic with the input as lookuprecords output.
4.  Add a log inside ForEach.

 In GRProxy, before starting the loop it internally loops over all the records in GlideRecord and collects sys\_ids and skipped counts by doing a canRead check.

</td></tr><tr><td>

Flow Engine

 PRB2054201

</td><td>

Introduce a cache in FlowRecompileChecker

</td><td>

The eviction policy is too broad for execution settings in ProcessPlanCache. Any change to any execution setting evicts all plans but should only effect one. Instead, it should evict a process plan directly when its execution settings change.

</td><td>

 

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

Global Ranking

 PRB2035527

</td><td>

Users aren't able to delete a scrum task from cross-scope

</td><td>

 

</td><td>

1.  Navigate to Collaborative Work Management \(CWM\) Workspace.
2.  Open any board.
3.  Turn on the 'Story &amp; Scrum' task.
4.  Add story &amp; scrum tasks records to the board.
5.  Try to delete the scrum task.

Observe that the shadow task is deleted but the actual scrum task isn't deleted.

6.  Refresh the board.

Observe that the deleted scrum task reappears.


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

Normally, it'd be expected that Glide apps would use different bootstraps. Given the special condition, when the Kafka bootstraps are the same, it should avoid the duplicate connections/healthchecks between the 2 services.

</td><td>

 

</td></tr><tr><td>

Hiring Experiences

 PRB2031986

</td><td>

The 'Last Month' option under 'My job requests' in the hiring portal displays data of requisitions created in the current month

</td><td>

For the 'Last Month' filter in the hiring portal, the UI displays the current month record because it's using &gt;= beginningOfLastMonth\(\), which pulls in June \(this month\) records too. The platform's native filter uses sys\_created\_onONLast month, which is properly bounded to just the previous month.

</td><td>

 

</td></tr><tr><td>

Hiring Experiences

 PRB2057166

</td><td>

GetRefRecord scoping bypass fix

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB2052114

</td><td>

Replace the 'Sparkle' icon with the Otto Lottie animation in AI and loader experiences

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
2.  Create a experience in UI Builder.
3.  Add an empty state component to the stage.
4.  In the config panel, locate the illustration property.
5.  Select **AI general** from the drop-down list.

 Expected behavior: The empty state shows the Otto logo.

 Actual behavior: The empty state shows sparkles.

</td></tr><tr><td>

Horizon Icon Component

 PRB2032851

</td><td>

Add the Otto icon to the library

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Create a experience in UI Builder.
3.  Add a now-button-iconic component to the stage.
4.  In the configuration panel, locate the drop-down list for the icon property .
5.  Search for 'sn-sparkmoji-logo'.

 Expected behavior: See the new Otto logo.

 Actual behavior: The icon is missing.

</td></tr><tr><td>

Horizon Icon Component

 PRB2050318

</td><td>

Update all 'Sparkle' icons

</td><td>

Icons with the Otto logo should be shown instead.

</td><td>

1.  Open an instance.
2.  Create an experience in UI Builder.
3.  Add a now-button-iconic component to the stage
4.  In the config panel, locate the icon property.
5.  Search for an icon.

 Expected behavior: Icons with the Otto logo are shown.

 Actual behavior: Icons with sparkles are shown.

</td></tr><tr><td>

HR e-signature

 PRB2035247

</td><td>

RCA for Content Experience

</td><td>

Specifically, eesign for getRefRecord directive.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2014389

</td><td>

RCAs are generated for 'Populate Manager Reportee Count Using Eligible Users' and 'Employee​Hub​Org​ Chart​Reportee​Util​SNC'

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

 PRB2035482

</td><td>

getRefRecord updates to Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2052205

</td><td>

In Australia and Zurich, RCAs generated in HR Core and HR Employee Relations must be added back to track/HR

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2052632

</td><td>

The **header\_config\_\*** fields are missing from the sn\_hr\_core\_service table in Zurich and Australia

</td><td>

**header\_config\_\*** fields missing from sn\_hr\_core\_service table in Zurich and Australia.

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

Inbound API Integration Usage Framework

 PRB1988771

 [KB3082116](https://hi.service-now.com/kb_view.do?sysparm_article=KB3082116)

</td><td>

IPAccessListFilter handling for malformed IP addresses

</td><td>

Inbound REST API calls coming through proxy servers \(x-forwarded-for header with multiple IP's\) or malformed IP address can sometimes fail in Zurich and Australia instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB2034837

</td><td>

Record data egress usage for integration requests

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB2034838

</td><td>

Domain separation support for Inbound API Integration Framework

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Innovation Management

 PRB2055588

</td><td>

GetRefRecord scoping bypass for app-ppm

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Innovation Management

 PRB2055611

</td><td>

GetRefRecord scoping bypass for app-common

</td><td>

 

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

Instance Clone \(Family\)

 PRB2032595

</td><td>

Deactivate the 'Target Instance Validate' business rule \(BR\) on an instance table to support OAuth-based authentication of clone targets from the Clone Admin Console

</td><td>

 

</td><td>

On any Australia instance, add a target instance through the Clone Admin Console.

 The instance is inserted into the table post-successful authentication, but there's an unnecessary BR that runs the authentication again to validate it. This BR was used in the legacy version of the clone and isn't required with the Store app.

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB2051479

</td><td>

Clone cleanup script fixes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB2051483

</td><td>

In Clone Admin Console, declare v.2.2.4 to ensure that OAuth is used

</td><td>

 

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
2.  See if there's multiple IDRDCTComparisonJob records present.

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

JVM at Scale

 PRB2032235

 [KB3078521](https://hi.service-now.com/kb_view.do?sysparm_article=KB3078521)

</td><td>

Memory watcher isn't logging active transactions in the Australia release

</td><td>

 

</td><td>

Refer to the listed KB article for details.

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

 PRB2022138

</td><td>

getRefRecord\(\) scoping bypass update

</td><td>

It must ship an RCA for HR tables for the knowledge scope sn\_km\_gen\_ai.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2031464

</td><td>

The Knowledge Base Article \(KBA\) is text not visible in the workspace

</td><td>

This issue occurs with custom templates that contain fields of mixed data types like HTML, string, date.

</td><td>

1.  Create such a template with mixed data types.
2.  Create an article fill, and fill non-**HTML** field as well.
3.  Insert a block in one of the fields.
4.  Save this article.
5.  Attempt to searching this article on 'SOW/CSM/KC'.
6.  Select the article

 Notice that it will open the kb\_view page of the article, and renders the article content as empty.

</td></tr><tr><td>

Knowledge Management

 PRB2033473

 [KB3144003](https://hi.service-now.com/kb_view.do?sysparm_article=KB3144003)

</td><td>

An article title isn't displayed in the Knowledge Article print view \(sysparm\_media=print\) from Service Portal on the Australia release

</td><td>

An article title isn't displayed in the Knowledge Article print view \(sysparm\_media=print\) from Service Portal on the Australia release due to a JavaScript error in KBViewArticle.jsdbx, while it works as expected in Zurich.

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

Legal Digital Forensics

 PRB2036701

</td><td>

Add the needed RCA as part of the getRefRecord\(\) scoping bypass directive changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Legal Hold Notification

 PRB2055600

</td><td>

Add the needed RCA as part of the getRefRecord\(\) scoping bypass directive changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Legal Matter Management

 PRB2036702

</td><td>

Add the needed RCA as part of the getRefRecord\(\) scoping bypass directive changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Legal Request Management

 PRB2036703

</td><td>

Add the needed RCA as part of the getRefRecord\(\) scoping bypass directive changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2030898

</td><td>

The 'Selected stage' icon isn't applied when WorkflowIcons has already assigned a default icon

</td><td>

 

</td><td>

1.  Open the latest Australia instance.
2.  Open an articles list in Knowledge Center.

 See that workflow states are displaying as 'No workflow stages available'.

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

List AI Indicators

 PRB2051786

</td><td>

The horizontal scroll for AI-tagged items in the groupedBy list is broken

</td><td>

When the user scroll to the right, the field isn't visible.

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

Manager Hub

 PRB2054008

</td><td>

In Manager Hub, add a null check when using getRefRecord\(\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mentoring

 PRB2056277

</td><td>

getRefRecord\(\) scoping bypass for mentoring

</td><td>

 

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

Mobile Experience for Field Service Management

 PRB2053984

</td><td>

Backport getRef changes to Field Service Management \(FSM\) Mobile

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB2033559

</td><td>

Add a null check for using getRefRecord\(\) in the script include

</td><td>

Enforce cross scope access restrictions when using Glide​Element​Reference.​ js​Function\_​get​Ref​Record\(\)​.​

</td><td>

1.  Create two scoped apps: App A and App B.
2.  In App B, create Table B with caller restriction turned on.
3.  In App A, create Table A with a reference field pointing to Table B.
4.  Don't grant RCA access from App A to Table B.
5.  Insert a record in Table A referencing a record in Table B.
6.  From the App A script, call current.​ref\_​to\_​b.​get​Ref​Record\(\)​.​

 Expected behavior: Access is denied, null is returned, and a violation is logged.

 Actual behavior: The call returns a valid record instead of null.

</td></tr><tr><td>

Mobile Platform

 PRB2039101

</td><td>

A device pin on mobile devices can't be turned off for Government Community Cloud \(GCC\) users

</td><td>

 

</td><td>

1.  Log in to a mobile device for a GCC instance.
2.  Note that the device pin is turned on.

 See that changing the device encryption enabled property doesn't turn off the pin.

</td></tr><tr><td>

Mobile Studio

 PRB2034896

 [KB3085639](https://hi.service-now.com/kb_view.do?sysparm_article=KB3085639)

</td><td>

sn\_maib app fails to auto-upgrade when installed

</td><td>

This is due to an incorrect app\_id declaration in the oob-app properties file.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Multi-Instance Framework - Core

 PRB2063884

</td><td>

MIF Hermes doesn't refresh the cluster configuration when the local hermes\_cluster\_config has no primary or after a datacenter-rule change, causing stale/failed cluster resolution for remote owners

</td><td>

When instance A sends a MIF async message to instance B, it needs B's Hermes cluster details \(datacenter + Kafka bootstrap servers\). A keeps a saved copy in the hermes\_cluster\_config table and reads it in Hermes​Producer​Client.​get​Cluster​Info​Set.​ Today that method only calls B's live endpoint \(/api/now/hermes \_cluster\_info, tier-2\) when A has no saved rows for B. Two gaps result: 1. Saved rows but no primary — if A has rows for B where no one is is\_primary\_for\_service=true \(scenario like only a single non-primary cluster row\), the method does not refresh. And method ensure​Topic​Location​For​Instance\(String owningInstance\) then finds primaryCluster == null and the send fails with 'No primary cluster found'. 2. Stale rows after a datacenter change — if a MIMIR rule change moves B's cluster to a new DC, A's saved rows are outdated but still look complete \(they have a primary\), so tier-1 returns them and A never re-discovers → messages Navigate to the old cluster.

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

5.  Call new MultimodalServiceUtil\(\) .​submit​On​Demand\(attachment​Sys​Id,​ query\).

 Observe that the on-demand MMS submission fails.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2019091

</td><td>

If beyond the 5MB limit, a localStorage limit blocks headerMenuItems from being cached

</td><td>

 

</td><td>

1.  Open an instance with thousands of apps and tens of thousands of modules, enough to make the menu payload be over 5MB.
2.  Clear the caches and refresh the page.

 Notice that the menu request is made on each load because the object isn't cached due to being too large.

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

Today, the KG default is User NLQ graph. That should be changed so the defaults are: In Now Assist Virtual Agent for natural language query, change the graph to Enterprise Graph \(Small\) and select the tag as 'VIRTUAL AGENT DEFAULT TAG'. In Now Assist Panel for natuaral language query, change the graph to Enterprise Graph \(Small\) and select the tag as 'NOW ASSIST PANEL DEFAULT TAG'.

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

OAuth

 PRB2018183

</td><td>

The unallowed system property glide.oauth. jwt.token\_request .honor\_claim\_keys is included in an upgrade payload, resulting in a misleading 'skipped' upgrade log entry

</td><td>

During a Zurich upgrade, the system property glide.oauth. jwt.token\_request .honor\_claim\_keys \(from com.​snc.​platform.​security.​oauth\)​ appears as a skipped entry. This property is not allowed by design and therefore never loaded into sys\_properties on user instances.

</td><td>

1.  Navigate to **All** &gt; **Upgrade Center** &gt; **Upgrade History**.
2.  Open the record of upgrading in Zurich.
3.  Select the **Skipped Changes to Review** tab.
4.  Select the skipped record for sys\_properties\_ 107762282f223210 3698319c003f9b2f.xml.

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

In a SMS action in a the subflow 'On-Call', the 'Check Assignment Response' doesn't use Notify

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
6.  Select the **Now Asisst** icon on business apps.

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

 PRB2056991

</td><td>

Log reasoning tokens for 3P providers and Now LLM

</td><td>

A new field, reasoning\_token\_count, naming is aligned to existing token fields. The field is added to the GenAI log table. The field is populated for reasoning-capable models across all supported providers. For non-reasoning models, or when a provider returns no reasoning count, the field defaults to zero \(documented\) rather than null-ambiguous. A single, documented convention is applied to stored token values: store the provider's raw output\_tokens and reasoning\_tokens separately such that reasoning\_tokens ≤ output\_tokens, allowing it to derive answer-only tokens as output − reasoning. Existing consumers of the log are unaffected, and total-token reconciliation still holds.

</td><td>

 

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

Incident, Change, Case summarizations are failing with errors when users select the **Summarize** button: 'Summarization could not be completed because access to the base table Case was unsuccessful'. Error logs: 'Error sending to unified\_short\_url\_active\_1...Status 500 - \[Internal Server Error\] \[\{'success':​false,​'status​Code':​429,​'message':​'Too many concurrent data insert operations in progress - additional rebuild request being ignored',​'timestamp':​'2026-​07-​17​T07:​00:​17.​752637494​Z',​'results':​\{\}​\}​\]​'.​

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Operational Technology Visibility

 PRB2031853

</td><td>

getRefRecord\(\) scoping bypass for Operational Technology \(OT\) core and OT Service Management

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1802682

</td><td>

The score for average duration of a DB view is incorrect when compared with the list view for both data snapshots and classic Platform Analytics \(PA\)

</td><td>

A Glide record sets a default value of '0' for null values. Classic PA uses the Glide record.

</td><td>

1.  Turn on data snapshots for the indicator in incident SLA DB view.
2.  Ensure to remove any scripted breakdowns.
3.  Add 'AVG of Business Duration' with units as 'Time'.
4.  Run data collection for both data snapshots and classic PA.
5.  Compare scores.

 See that classic PA shows 11 hours 28 minutes, data snapshots shows 8 hours 35 minutes, and list view shows 20 hours 40 minutes.

</td></tr><tr><td>

Performance Analytics

 PRB1949829

</td><td>

Breakdown elements aren't displaying consistently on the 'workbench' widget

</td><td>

On the 'workbench' widget, all the elements are displaying for a breakdown when the **Timeseries** field has a value and the value of the property 'com.snc.pa. scorecard.breakdown. chart.max\_rows' hasn't been changed.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB2032037

</td><td>

The Platform Analytics dashboard filters ignore Element Security Lists and display 'Nothing is available'

</td><td>

If the user sets up an Element Security List for a breakdown source that's used as a filter in a Platform Analytics dashboard, the filter shows 'Nothing is available'. This happens even though the user has valid access to the dashboard and the underlying data.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB2035061

</td><td>

Core UI widgets render blank data for fiscal and business calendar indicators

</td><td>

Highcharts has been upgraded from version 10.3.3 to 12.3.0. As part of this upgrade, some legacy Highcharts utility methods used by the Core UI dashboards \(legacy pa\_dashbaord\) and widgets have been deprecated or replaced in the newer version. Any usage of older Highcharts APIs or utility methods should be reviewed and updated to use the latest supported alternatives available in Highcharts 12.3.0.

</td><td>

1.  On any instance in \(or after\) Australia's build, create any indicator source with:

**Standard calendar** &gt; **fiscal quarter or fiscal year**

2.  Create the indicators with these sources and run data collection jobs to populate scores.
3.  Navigate to KPI Details/Analytics Hub with these indicators and make sure that the charts are visible.
4.  Create core UI widgets and link the with the newly created indicators.
5.  Create a core UI Dashboard and add the widgets.

 Expected behavior: The same data as shown in the Analytics Hub is to be rendered.

 Actual behavior: All the business calendar or fiscal calendar indicator widgets render blank data.

</td></tr><tr><td>

Performance Analytics

 PRB2050693

</td><td>

injectWidgetContent re-executes already-loaded scripts via document.body.appendChild, causing a widget regression

</td><td>

injectWidgetContent in canvasUtils.js strips all &lt;script src&gt; tags from the widget HTML and re-injects them via document.body.appendChild. For scripts already loaded at page render time via Jelly &lt;g:requires&gt;, this causes re-execution, which corrupts initialized state and breaks widget functionality.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB2054497

</td><td>

Data snapshot indicator charts fail to render

</td><td>

It can't encode an object during JSON serialization.

</td><td>

On an Australia instance, open any dashboard with a data snapshot indicator chart.

 Observe that the chart fails to render. Check the server logs for: ''Cannot encode object' / JsonMappingException through reference chain: LinkedList\[0\] -&gt; Data​Snapshots ​Data​Service$1\['response'\]​'.​

</td></tr><tr><td>

Platform Analytics Component API

 PRB1961798

</td><td>

Records aren't deleted from report stats or the 'Visualization metadata' table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2021236

</td><td>

In an instance migrated to Australia, reports display Name = None for non-global domains

</td><td>

When a instance with core UI reports is migrated to Australia, any reports that aren't in the global domain don't have the name set.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2031447

</td><td>

A data visualization type is duplicated post-Australia upgrade

</td><td>

When in the **Platform Analytics** &gt; **Library** &gt; **Data Visualization** &gt; **Landing** page under the 'Count' section, and putting a filter with the condition type as 'single score', there are duplicate values in the total.

</td><td>

1.  **All** &gt; **Platform Analytics** &gt; **Data visualization**.
2.  Try adding a filter on the **Type** fiel.
3.  While adding a filter condition, observe it has more than one single score.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2037528

</td><td>

In Australia, data visualizations created by non-admin users aren't visible by that user on the 'Overview' page under **Quick Access** &gt; **Created by me**

</td><td>

 

</td><td>

1.  On an Australia instance, impersonate a non-admin user.
2.  Navigate to **Platform Analytics** &gt; **Data Visualizations** &gt; **Library**.
3.  Select **Create data visualization** to create a data visualization \(any type, any data source\).
4.  Navigate to **Platform Analytics** &gt; **Data Visualizations** &gt; **Library** &gt; **Overview**.
5.  Under 'Quick Access', select **Created by Me**.

Observe that the data visualization doesn't appear.

6.  Repeat the same as an admin user.

Note that the visualization does appear.


</td></tr><tr><td>

Platform Analytics Component API

 PRB2039912

</td><td>

'vertical\_bar' is displayed in the value format on the data visualization library page

</td><td>

 

</td><td>

1.  Turn on the v\_table property to see Core UI reports in the data visualization library.
2.  Search for 'Top 15 most helpful articles'.
3.  Check the type of the report.

 Expected behavior: The type should be 'Vertical bar'.

 Actual behavior: The type is 'vertical\_bar'.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2040129

</td><td>

Optimize the reparenting script

</td><td>

 

</td><td>

1.  Upgrade a Zurich instance to Australia.
2.  Navigate to the dashboard/data visualization library page.

 Expected behavior: Dashboards/data visualization are there in the library page list.

 Actual behavior: Dashboards/data visualization aren't shown in the library page list.

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

 PRB2050123

 [KB3131331](https://hi.service-now.com/kb_view.do?sysparm_article=KB3131331)

</td><td>

GlideClearDashboardCache is undefined in Australia, causing four business rules \(BR\) to fail on every Platform Analytics \(PA\) dashboard save and widget loss and save failures

</td><td>

The Java class GlideClearDashboardCache \(com.snc.par. dashboards.glide.script. ClearDashboardCache, annotated @GlideScriptable\) isn't registered in the Rhino scripting scope. The class is present in the com.snc.par.dashboards OSGi bundle JAR, but isn't accessible as a Rhino scriptable — typeof GlideClearDashboardCache returns undefined. Four business rules in com.snc.par.dashboards call this class with no try/catch on every INSERT, UPDATE, and DELETE against par\_dashboard, par\_dashboard\_canvas, par\_dashboard\_widget, and par\_dashboard\_permission. When a user saves a PA dashboard, these BRs throw RhinoEcmaError: 'GlideClearDashboardCache' isn't defined \(logged as WARNING in the node log, firing 14+ times per transaction\). Two failure modes: \(1\) dashboard save fails with 'Your dashboard could not be saved', or \(2\) save succeeds but in-memory cache not flushed — stale canvas layouts cause widgets to disappear from tabs on subsequent loads.

</td><td>

 

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
4.  Open the dashboard record using a URL like 'https:​/​/​&lt;instance-​id&gt;​.​service-​now.​com/​par\_​dashboard.​do?​sys\_​id=​&lt;sys\_​id&gt;​'.​
5.  Clear the **Active** option.
6.  Update the record.
7.  As the same user as step 1, access the dashboard via a URL like 'https:​/​/​&lt;instance-​id&gt;​.​service-​now.​com/​now/​platform-​analytics-​workspace/​dashboards/​sys-​id/​&lt;sys\_​id&gt;​'.​
8.  Check par\_dashboard\_tab.

 Expected behavior: The par\_dashboard\_tab doesn't have a record for the test dashboard.

 Actual behavior: Once the user accesses the inactive dashboard, one or two new par\_dashboard\_tab records are created unintentionally.

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

 PRB2021606

</td><td>

An interactive filter can be cleared via a double click even when the 'Allow User to Clear Filter' option is turned off

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

Platform Analytics Filters

 PRB2031107

</td><td>

The 'Allow user to clear filter' option isn't auto-checked in the filter designer

</td><td>

 

</td><td>

1.  Configure one single select, one multi select, and one date filter type separately from filter designer.
2.  Add a source if needed, based on the filter type.
3.  Save the filter.
4.  Open each filter.
5.  Check the 'Advanced' option.

 Expected behavior: The 'Allow user to clear filter' option should be auto-checked.

 Actual behavior: The 'Allow user to clear filter' option isn't auto-checked.

</td></tr><tr><td>

Platform Analytics Filters

 PRB2031506

</td><td>

The 'Follow' filter toggle option is missing in a cascading filter

</td><td>

 

</td><td>

1.  Create a Next Experience dashboard.
2.  Add two filters, one on sys\_user\_group and another on sys\_user.
3.  In the configuration panel of the filter on sys\_user, check the 'Follow other' filter section.

 Expected behavior: The filter on sys\_user has the option to follow the sys\_user\_group filter.

 Actual behavior: No available option is displayed.

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

Platform Analytics Migration API

 PRB2057808

</td><td>

Remove unified User with elevated privileges only

</td><td>

Removing the write for User with elevated privileges only for the com.glide.par.unified \_analytics.enabled property.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2025987

</td><td>

A user can't view a playbook without record create access

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2034002

</td><td>

There's canLaunchPlaybook and launchPlaybook inconsistency for run strategy

</td><td>

can​Launch​Playbook\(enforce​Run​Strategy=​true\)​ returns true but the subsequent launchPlaybook call throws PlaybookInvalidInputException: 'The playbook specified can't be launched because of its run strategy for the same playbook and parent record'.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2052473

</td><td>

The getPlaybookContextParentRecord API should be exposed as scriptable

</td><td>

The Playbook MCP tool code doesn't use the existing API get​Playbook​Contexts​ By​Parent​Record to launch and continue playbook execution. This API internally handles all validation and permission access, which results in duplicate logic. The current java API should be exposed as a scriptable API to use at Playbook MCP tool.

</td><td>

1.  Add any compatible playbook as MCP tool.
2.  Try to launch playbook through the Claude client.

 Observe that it launches playbook, but it uses custom logic to validate access and permission.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2052669

</td><td>

'Completed By'/'Completed On' for activity contexts

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Portfolio Planning with PPM, Agile 2.0, and SAFe

 PRB2055648

</td><td>

GetRefRecord scoping bypass for app-apw-internal-int

</td><td>

 

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

Process Mining Workspace

 PRB2007466

</td><td>

When feedback given by user is changed and navigates to another UI, on a revisit, the **Feedback** button switches from the previous state to new

</td><td>

 

</td><td>

1.  Generate highlights for any of the findings on a mined project.
2.  Submit feedback via the icon.
3.  Navigate to any other page or open any other finding.
4.  Navigate back to the same highlights and make a thumbs down.

 Expected behavior: Feedback shouldn't be switched back and forth. The new state should be preserved even if the user navigates to other screens.

 Actual behavior: When the user comes back to the finding where feedback is given, the feedback is switched from the previous state to the new state.

</td></tr><tr><td>

Process Mining Workspace

 PRB2024798

</td><td>

Summary top banner metrics isn't displaying until the project is reopened or the page is refreshed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB2029472

</td><td>

The **Intent and activity analysis** button is enabled on findings without process configuration

</td><td>

 

</td><td>

1.  Don't configure intent and activity analysis on process configuration.
2.  Navigate to the 'Summary and insights' page of the mined project.
3.  Open the findings in the 'Opportunity details' page.
4.  Select the **Investigate** tab.

 Observe that intent and activity analysis is turned on. It should be turn off without the proper configuration.

</td></tr><tr><td>

Process Mining Workspace

 PRB2030093

</td><td>

Re-triggering 'Generate highlights' after an error displays no loading indicator or feedback that a process is running

</td><td>

 

</td><td>

1.  Navigate to an improvement opportunity with a high number of records \(~30k\).
2.  Attempt to generate highlights.

Observe that an error is displayed.

3.  After the error, select **Generate highlights** again.

 Expected behavior: The UI should go into 'progress' mode, before displaying the result/error.

 Actual behavior: No loading indicator, spinner, or any visual feedback is displayed to the user to indicate that a process is running.

</td></tr><tr><td>

Process Mining Workspace

 PRB2030109

</td><td>

An errored scheduled task leaves the component stuck at 'Loading contents...' indefinitely

</td><td>

 

</td><td>

1.  Navigate to an improvement opportunity with a high number of records \(~30k\).
2.  Attempt to generate highlights.

 Observe that the scheduled task errors out, and that the highlights component remains stuck displaying 'Loading contents..' indefinitely and never surfaces the error state to the user. The loading message should be replaced with an error message.

</td></tr><tr><td>

Process Mining Workspace

 PRB2050830

</td><td>

Wipe out promin\_metered \_usage\_data across non-prod and rely on the Glide non-prod/prod property, not on the Open/Closed property

</td><td>

When users clone production to a sub-prod instance, the sub-prod promin\_metered \_usage\_data table is wiped and replaced with prod's data, so sub-prod reflects a copy of prod rather than real usage. When users clone prod to several sub-prods at once, each carries prod's usage table. Subscription Management's flat aggregation then counts the same prod records once per instance, so reported usage scales linearly with the number of sub-prods a customer maintains, independent of actual mining behavior.

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

Project Management

 PRB2006929

</td><td>

Deleting a project task with MS Project creates an orphaned resource request

</td><td>

 

</td><td>

1.  Log in to any instance.
2.  Open the new Project Workspace.
3.  Select the **New** button to create a project.
4.  Select the menu button **\(...\)** &gt; **Import from MS project**.
5.  Upload a MS Project schedule.
6.  Create a resource request for Project Tasking.
7.  Navigate to the resource module as the resource manager and approve the task.
8.  As the project manager, delete the task in the MS Project schedule.
9.  Return to the project record.
10. Re-upload the updated MS Project.

 Expected behavior: The reupload of the schedule isn't permitted because of the related record or if it does allow the reupload, it should cascade the delete to the related records.

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

ReleaseOps - Family

 PRB1951541

</td><td>

update\_set\_admin needs access to 'Promote Update Set'

</td><td>

The UI action condition currently requires the admin role, but should allow for both 'admin' and 'update\_set\_admin'.

</td><td>

As a user with role update\_set\_admin \(and not admin\), complete an update set.

 Expected behavior: The**Promote Update Set** UI action is available.

 Actual behavior: It isn't available.

</td></tr><tr><td>

Reporting

 PRB2040639

</td><td>

Require authentication on a scripted rest API reporting\_alias

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB2058918

</td><td>

Logging when there's an RVACL exception doesn't work for visualizations and only for Core reports

</td><td>

Glide.rest.debug = true can't be set on instances, so it needs a dedicated sys property to allow RVACL exception logging for the failed path. Only Core UI reports are tracked in the code and not visualizations.

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB2050782

</td><td>

An approval summary displays the incorrect attachment

</td><td>

In Service Operations Workspace \(SOW\), attachment records displayed on approval records are inconsistent with the actual request item. When multiple request items contain attachments with the same file name, SOW resolves and displays the attachment from a different record \(incorrect sys\_id\). The attachment file name appears correct, but the underlying file content belongs to a different request item. This behavior isn't reproducible in Classic UI, where attachments are always correctly associated with the respective record. The issue doesn't occur when the attachment file names are unique.

</td><td>

 

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

Schedule Optimization

 PRB2022407

</td><td>

getRefRecord\(\) scoping bypass for the 1.0.1 release

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Security Data Filters

 PRB1967733

</td><td>

A security data filter \(SDF\) is applied redundantly via dotwalk paths, causing missing records in 'OR' queries

</td><td>

This has two distinct symptoms caused by the same underlying duplication. One, when querying a parent table with 'OR' conditions dotwalking into multiple child tables simultaneously, the parent SDF was applied three times — once directly and once per dotwalk CE path — producing conflicting conditions that returned zero records instead of the expected results. Two, when querying a table with a field-based SDF, records where that field was empty/null were incorrectly excluded. This was caused by the same SDF being applied redundantly via a dotwalk CE, which caused the combined filter condition to exclude null matches.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB2051345

 [KB3128196](https://hi.service-now.com/kb_view.do?sysparm_article=KB3128196)

</td><td>

Automatically created KittyScript exemptions are incorrect when using 'new GlideRecord'

</td><td>

When GuardedScript/KittyScript checks scripts in the exemption table, it does by checking a \_normalized\_ version of the script, where all literals are removed to ensure that it deduplicates similar scripts where the only difference is \(say\) a 'sys\_id'. This normalization does \_not\_ apply to the constructor of 'GlideRecord' where it doesn't want a blanket execption for \_all\_ tables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Builder

 PRB2030878

</td><td>

'Mode' defaults incorrectly when not specified in the catalog item configuration, blocking item submission from Builder

</td><td>

The root cause is a missing default value for the 'mode' property in the catalog-item component configuration \(now-ui.json\).

</td><td>

1.  Navigate to UI Builder.
2.  Create an experience and a page.
3.  Add the catalog item component to the page and provide the sys\_id.
4.  Preview the page and submit the item.

 Expected behavior: The item should get submitted.

 Actual behavior: The item isn't submitted.

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

During bulk SLA recalculation, SLACalculatorNG accumulates one GlideSchedule and one DurationCalculator instance per unique schedule+timezone combination into unbounded object maps \(this.schedules and this.durationCalculators\). These maps are never evicted and grow proportionally to the number of distinct schedule/timezone pairs encountered across all task\_sla records in the query. In instances with many SLA definitions backed by different schedules, this results in unbounded heap growth for the lifetime of the bulk calculation, degrading instance performance and potentially causing out-of-memory conditions under load.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Mapping

 PRB1971609

</td><td>

Service Mapping Discovery runs an instance out of memory during the rediscovery process in case there are 100K discovered services in Operational Status

</td><td>

The code queries for all cmdb\_ci\_service\_discovered records with operational\_status=1 without any limit. If a user has enough cmdb\_ci\_service\_discovered records with operational\_status=1, then the instance can immediately be run out of memory while building an array of the results. 0 means no limit: get​All​Discovered​Business​Services\(conditions,​ null, 0\).

</td><td>

1.  Create 100K discovered services in Operational Status.
2.  Run 'All Application' Discovery.

</td></tr><tr><td>

Service Mapping

 PRB2036299

</td><td>

After upgrading to Australia, parent.process.pid fails to resolve, which causes the 'Get Process' operation to return the full process list instead of the targeted parent process

</td><td>

The user can run a customised Tomcat WAR pattern for Service Mapping discovery. Following the Australia upgrade, step two of the 'Identification' section stops working during Service Mapping discovery. The step uses a 'Get Process' operation with process\_id = get\_attr \{'parent.process.pid'\} to locate the parent Windchill Java process. This expression fails to resolve, causing the step to run with no PID filter and return the entire process list on the host instead of the targeted parent process.

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

Error: '\[now-sdk\] ERROR: Exception occurred while installing application/nUnable to install application as application was null. Error: Exception occurred while installing application/nUnable to install application as application was null'.

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

 Actual behavior: The metadata not removed.

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

Smart Assessments for Field Service

 PRB2054418

</td><td>

Backport getRef changes to app-smart-assessment-mobile

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Smart Assessments Mobile

 PRB2054417

</td><td>

Backport getRef changes to app-smart-assessment-mobile

</td><td>

 

</td><td>

 

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

Source-to-Pay Operations \(Glide\)

 PRB2057105

</td><td>

getRefRecord\(\) scoping bypass directive changes

</td><td>

 

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

Stream Connect Core

 PRB2036772

</td><td>

Stream Connect fails to authenticate with Kafka brokers requiring OAUTHBEARER as the SASL mechanism, blocking connectivity

</td><td>

When a broker is configured to require OAUTHBEARER, the Kafka client initiates a SASL handshake and signals the OAUTHBEARER mechanism. Without a registered token callback handler, the client cannot respond with a valid bearer token, causing the handshake to fail. The connection is dropped and no meaningful error is surfaced to the administrator beyond a generic authentication failure.

</td><td>

1.  Configure an external Kafka broker with the SASL mechanism set to OAUTHBEARER and a valid OAuth 2.0 token endpoint.
2.  In Stream Connect, navigate to the credential configuration for Message Replication and attempt to select OAUTHBEARER as the SASL mechanism.

 Observe that OAUTHBEARER isn't available as a selectable mechanism in the credential configuration UI.

</td></tr><tr><td>

System Import Sets

 PRB2033737

 [KB3070753](https://hi.service-now.com/kb_view.do?sysparm_article=KB3070753)

</td><td>

role mis\_server can't read database credentials for a JDBC data source when it uses an alias

</td><td>

 

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

There's hourly reoccuring OAuth authentication failures on an outbound REST from ST ServiceNow to CG ServiceNow: 'User is not authenticated. OAuth token has expired or has not been retrieved'

</td><td>

The reported issue affects the outbound integration between ServiceNow and the external ServiceNow instance through the iPaaS layer using OAuth 2.0 Client Credentials authentication. The integration fails specifically during the final one-minute window before the OAuth access token expiration. During normal token validity, the integration works successfully. Starting one minute before token expiration, outbound calls from ServiceNow fail. Failures occur in: REST Message, REST API Step, Flow Designer executions, and custom scripts. Once the token fully expires, ServiceNow successfully retrieves a new token and the integration resumes functioning normally.

</td><td>

 

</td></tr><tr><td>

Table Builder

 PRB2052385

</td><td>

Backport GetRefRecord scoping bypass changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Tags

 PRB2039548

</td><td>

In Australia, tags aren't saved for 'active = false' records for non-admin users

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Talent Feedback

 PRB2056254

</td><td>

getRefRecord\(\) scoping bypass for talent feedback

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Task Plan Templates

 PRB1978400

</td><td>

Auto-populating the value of a task plan **Feature** field in a task plan template document isn't dymanic

</td><td>

The domain separations script needs an additional check for the global domain.

</td><td>

1.  Navigate to the sn\_task\_plan\_ template\_document table.
2.  Select the **New** button.

The task plan **Feature** field is auto-populated.

3.  Navigate to the sn\_task\_ plan\_feature table and delete the document feature.
4.  Create a record with the sn\_task\_plan\_ template\_document feature table with the name 'Document'.
5.  Navigate to the sn\_task\_plan\_ template\_document table.
6.  Select the **New** button.

The task plan **Feature** field isn't auto-populated now.


</td></tr><tr><td>

Territory Planning

 PRB2039182

</td><td>

Updating potential territories for a task doesn't work as expected

</td><td>

The business rule that updates the potential territories is currently triggered only when the location changes. It doesn't consider the **consider\_​potential\_​territories \_for\_schedule\_optimization** boolean field.

</td><td>

1.  Create a work order task.
2.  Change the location to see the eligible territories as per the new changed location.

 Expected behavior: The Business Rule that updates the potential territories should consider the**consider\_potential\_territories \_for\_schedule\_optimization** boolean field.

 Actual behavior: The Business Rule that updates the potential territories is currently triggered only when the location changes and doesn't consider the **consider\_potential\_territories \_for\_schedule\_optimization** boolean field.

</td></tr><tr><td>

Third-party Software

 PRB2032449

</td><td>

The Kitty script changes should be reverted

</td><td>

The changes to the Kitty script are no longer required. Everything works fine; the dashboard loads and there's no exception in the syslog table.

</td><td>

 

</td></tr><tr><td>

Time-Limited User Roles

 PRB1972197

</td><td>

When a user is logged in, updating an existing record with a new end time in the 'Time limited user roles' tablec causes never ending information messages on all pages

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
2.  Create a incident.
3.  Fill in the mandatory fields.
4.  Attempt to save it.

 Observe that the error message isn't shown for the **short\_description** field.

</td></tr><tr><td>

UI Field Administration

 PRB2054948

</td><td>

ServiceNow Otto rebranding for AI indicators, AI indicator pop-overs, and Task intelligence predicition

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

1.  Change the glide.ui. journal.use\_html system property to true.
2.  Open any incident in any workspace.
3.  Type multiple lines in internal info or copy/paste some text until the scroll bar appears.
4.  Remove enough lines so that it's one new line away from displaying the scroll bar.
5.  Type some words randomly to add enough words to create a line.

 Observe the flickering issue.

</td></tr><tr><td>

UI Form Administration

 PRB2033143

 [KB3139369](https://hi.service-now.com/kb_view.do?sysparm_article=KB3139369)

</td><td>

The 'Preview this record' icon isn't working in the Safari browser

</td><td>

Selects on the button components and controls isn't working in Safari for UI16. This issue is only reproducible in the Safari browser. Non-Safari browsers aren't impacted and they don't face this issue.

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

Upgrade Center

 PRB2056920

</td><td>

Bulk app updates feature Glide changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2004013

</td><td>

Filters aren't appearing in the dashboard

</td><td>

Filters aren't appearing in dashboard in an initial dashboard load.

</td><td>

1.  In cache.do, select **Clear Cache** and **Clear All Browser Caches**.
2.  Open a dashboard presenting multiple filters.

 Observe that the filters aren't loading.

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

 PRB2039881

</td><td>

GLOBAL\_NAVIGATION\_REQUESTED isn't routing to a feature after selecting a hard refresh of the page

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2054946

</td><td>

Keyboard shortcut remapping for admins and users

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent for Customer Service \(Store\)

 PRB1998239

</td><td>

An outdated file in the Virtual Agent store plugin causes integration tests to fail

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1895195

</td><td>

When the user enters an invalid/partial utterance, an error appears and the conversation is closed

</td><td>

Dynamic capability executor can trigger multiple capabilities with different payloads. However, dynamic capability executor fails when duplicate capability IDs are passed.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1914417

</td><td>

Stopping agentic conversation shows an undefined message

</td><td>

 

</td><td>

1.  Start any agentic flow from Dispatcher Workspace, Now Assist Panel, NASS, or Playground.
2.  Select the **Stop** button once it's displayed.

 Observe the undefined message is displayed.

</td></tr><tr><td>

Virtual Agent

 PRB1952103

</td><td>

Remove showNoSkillsConfigured options passed when requesting the skill picker control in Now Assist Portal \(NAP\)

</td><td>

Previously, a message was displayed to the end user if no applicable skills were configured for the logged-in user in NAP. Now that NAP also supports QnA, users will still be able to search knowledge articles, so this message is no longer required.

</td><td>

1.  Make sure no skills are configured for the current user.
2.  Launch NAP.

 Observe a message reading: 'Looks like no skills are configured' and the conversation ends.

</td></tr><tr><td>

Virtual Agent

 PRB1960129

</td><td>

A conversation abruptly ends after a cold start conversation with a pre-chat survey enabled

</td><td>

The conversation ends after the survey is complete.

</td><td>

1.  Enable pre-chat survey.
2.  Navigate to Teams.
3.  Type 'what is spam'.
4.  Complete the pre-chat survey.

 Expected behavior: The user should get a response related to the query from step 3.

 Actual behavior: The conversation ends after the survey is complete.

</td></tr><tr><td>

Virtual Agent

 PRB1962876

</td><td>

An interaction record form doesn't always pop up when receiving an inbound call

</td><td>

An interaction record form doesn't always pop up when receiving an inbound call from multiple sources in short time.

</td><td>

 

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

According to Search QnA, the prompt isn't structured to support the intermediate language selection turn. That should be removed from the conversation history.\`.

</td><td>

1.  Configure language detection.
2.  Start a conversation in any standard chat.
3.  Type an utterance in a different language.
4.  The user is presented with 'You are typing in xyz language, do you want to switch' - select **Yes**.

 Expected behavior: The language should switch and the synthesized response should be displayed.

 Actual behavior: The langue switches but the response is 'How can I help you with your laptop'.

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

1.  Open Now Assist Portal.
2.  Enter an utterance like 'Help me get details of a problem'.

Observe that the agent returns a response like 'Could you please provide the problem number you'd like details for?'.

3.  Enter an utterance like 'See you later'.

 Expected behavior: The agent returns a response like 'Understood. Feel free to return anytime if you need help.'

 Actual behavior: Additional closure messages show up, and the last two messages are duplicated. For example, the agent might return the following: 'Understood. Feel free to return anytime if you need help. Thanks for chatting! I will go ahead and close this conversation now. I'm here if you need anything else. It looks like you're finished with this chat, so I will go ahead and close it. It looks like you're finished with this chat, so I will go ahead and close it.'.

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

 PRB2035888

</td><td>

A Guardian-triggered async\_search early-return leaves a stale task ID in the context

</td><td>

 

</td><td>

1.  Send a prompt that Guardian flags and see that it's displayed correctly.
2.  See that the first request is still active but times out later.
3.  Send a second utterance that triggers skill Discovery immediately.
4.  Wait for a timeout from the first message to occur to display a 'sorry' message in the conversation.

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

 Observe that that only the snc\_external role is added. The snc\_internal role is never associated to this ACL.

</td></tr><tr><td>

Virtual Agent

 PRB2056495

</td><td>

Central cache doesn't return the correct entry if the cache is updated from a different cluster

</td><td>

In the central cache log, the following message apepars: 'Negative cache hit — Glide previously returned null for this key'.

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

No policy configs are returned because buildPolicyConfig doesn't target sys\_​now\_​assist\_​ va\_​persona\_​detail and doesn't filter by persona\_detail\_type = Policy.

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

Virtual Agent Web Client

 PRB1933088

</td><td>

Processing loader is displayed even after getting a response

</td><td>

 

</td><td>

1.  Select **Now Assist Portal**.
2.  Enter 'Summarize a record/conversation'.
3.  Select the discovered skill.

 Observe that the loader is still displayed, even after getting the record number question.

</td></tr><tr><td>

Vulnerability Response Integration with Microsoft Defender for IoT \(Azure\)

 PRB2031861

</td><td>

getRefRecord\(\) scoping bypass for AzureVR

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Window Manager

 PRB2041392

 [KB3142333](https://hi.service-now.com/kb_view.do?sysparm_article=KB3142333)

</td><td>

There's a UI bug when opening the Now Assist panel

</td><td>

When a user has a menu pinned \(whether it's the All menu, Favorites, History, etc.\) and they open the Now Assist panel, the pinned menu turns into a blank white pane. The menu that was pinned also then reappear in the list of other unpinned menus, although the name of the pinned menu still also appears next to the ServiceNow logo with a blank pane beneath it. The blank menu can generally be recovered by opening it from the list of unpinned menus \(where it has reappeared\) and re-pinning it , refreshing the page, or resizing the window. However, there is some inconsistency in whether refreshing or resizing the window always fixes it. If users refresh with the blank menu pinned and the Now Assist panel still open, the Now Assist panel then becomes blank and can only be dismissed/recovered by pinning something else, like sidebar discussions, to the right of the screen to get rid of it. This behavior happens most consistently when a user with a pinned menu logs in and opens the Now Assist panel for the first time after their start screen loads. However, it does also happen MID-session sporadically if users unpin/re-pin different menus and open/close the Now Assist panel frequently.

</td><td>

Refer to the listed KB article for details.

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

 PRB2034992

</td><td>

Backport changes for getRefRecord\(\) changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB2053534

</td><td>

The 'Location update when PSO is populated' business rule isn't needed anymore

</td><td>

The business rule sets and syncs the **Location** field on the work order from the provider organization, and the same location is applied to the work order task. This seems confusing, since the provider org and location don't necessarily have to be the same. The provider org refers to who is responsible for the work, while the location refers to where the work happens.

</td><td>

1.  Create a work order.
2.  Update the provider organization.

 Expected behavior: The location remains unchanged.

 Actual behavior: The location changes to the provider organization location.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 4 Hotfix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3143885)
-   [Australia Patch 4 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3140560)
-   [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md)
-   [Australia Patch 3 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3143614)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)
-   [Australia Patch 2 Hotfix 5a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3142075)
-   [Australia Patch 2 Hotfix 4b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3143888)
-   [Australia Patch 2 Hotfix 3b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3138484)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/available-versions.md)


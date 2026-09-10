---
title: Australia Patch 6
description: The Australia Patch 6 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/australia-patch-6.html
release: australia
topic_type: reference
last_updated: "2026-09-20"
reading_time_minutes: 134
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 6

The Australia Patch 6 release contains important problem fixes.

-   **Australia Patch 6 was released on September 10, 2026.**
    -   Build date: 09-04-2026\_1352
    -   Build tag: glide-australia-02-11-2026\_\_patch6-08-21-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A06.00.xlsx).

## Overview

Australia Patch 6 includes 675 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-ap6.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Australia Patch 6 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 6, refer to [KB3152248](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152248).

## Changes in Australia Patch 6

-   ****

    Live Connect provides read-only access to your ServiceNow tables, allowing you to write SQL queries, create reports, and perform analysis while maintaining your existing security controls. This eliminates the need for data synchronization and ensures you work with current ServiceNow data.

-   ****

    Activate a Stream Producer configuration to begin capturing and streaming table changes to your Kafka topic. You can deactivate it at any time to stop streaming changes. When you deactivate a producer, any unprocessed messages in the CDC queue are discarded.

-   ****
-   ****
-   ****
-   **[Connect a private relay to the Reverse Tunnel gateway](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/connect-customer-relay.md)**

    In the relay record, select **Recreate** gateways to recreate a gateway instance.

-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   ****
-   **[Integration Hub plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/ih-plugins.md)**

    ServiceNow Stream Producer \[com.glide.hub.stream\_connect.stream\_producer\]: Enables Stream Producer to automatically stream changes from ServiceNow tables to Kafka topics.

-   **[Using Stream Connect for Apache Kafka](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/stream-connect-apache-kafka.md)**

    Automatically stream changes from ServiceNow tables to Kafka topics with Stream Producer.

-   ****

    Stream Producer enables you to automatically stream changes from ServiceNow tables to Kafka topics using change data capture \(CDC\), eliminating the need for custom scripts or business rules.

-   ****

    Create a Stream Producer configuration to automatically stream table changes to a Kafka topic. You can specify which table to monitor, which change events to capture, which fields to include, and configure keys and headers for routing and tracking.

-   ****

    Monitor Stream Producer performance metrics and change data capture \(CDC\) queue health to identify bottlenecks and optimize for your deployment scale and throughput requirements.

-   **[Schema management in Stream Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/schema-management.md)**

    When you create or update a Stream Producer record with the serialization format set to Avro, ServiceNow automatically generates and maintains an Avro schema for the associated table.

    Stream Producer schemas are stored across two tables in the ServiceNow IntegrationHub Stream Connect Schema \[`com.glide.hub.stream_connect.schema`\] plugin. These tables are read-only for all users. No one has create, update, or delete access.

    You can also configure a Stream Producer to send messages in an Avro format. When the serialization format is set to Avro, the Stream Producer uses the auto-generated schema for the selected table to convert CDC payloads to Avro before sending them to Kafka.

    The Schema Registry REST API exposes your Stream Producer Avro schemas to external systems and consumers. External applications can use the API to retrieve schemas and decode Avro-encoded messages received from Kafka topics.

    Stream Producer schema evolution features.

-   ****

    Human-assisted SMS OTP lets a human agent verify an end user's identity by sending a one-time passcode via SMS during a live interaction. The agent initiates OTP generation and validation through the platform's scriptable APIs, and the consuming application \(for example, CSM or FSO workspace\) handles the agent-facing workflow and user interface.


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

 PRB2073716

 [KB3148324](https://hi.service-now.com/kb_view.do?sysparm_article=KB3148324)

</td><td>

For non-admin users, search results and suggestion navigation on portals are redirecting to platform view

</td><td>

After upgrading to Australia Patch 5 or Zurich Patch 12, non-admin users performing a search on a portal \(for example, /esc\) experience incorrect navigation. Selecting a regular search result or a suggested search result opens the record in the platform view rather than within the portal.

</td><td>

Scenario 1:

 1.  Upgrade an instance to Australia Patch 5 or Zurich Patch 12.
2.  Log in as a non-admin user.
3.  Perform a search on a portal, such as /esc or /sp.
4.  Select the regular search result that is returned.

 Observe that the record opens in platform view instead of the portal.

 Scenario 2:

 1.  Upgrade an instance to Australia Patch 5 or Zurich Patch 12.
2.  Log in as a non-admin user.
3.  Enter a search term on a portal, such as /esc or /sp, without submitting the search.
4.  Select a suggested search result in the typeahead drop-down list.

 Observe that the record opens in platform view instead of the portal.

</td></tr><tr><td>

Core UI Responsive Dashboards

 PRB2034505

 [KB3085059](https://hi.service-now.com/kb_view.do?sysparm_article=KB3085059)

</td><td>

A Platform Analytics \(PA\) dashboard overview can't load any dashboards

</td><td>

If all of the following conditions are met, the dashboard doesn't appear on the 'All' tab of PA dashboard 'Overview' page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence

 PRB2075293

 [KB3150595](https://hi.service-now.com/kb_view.do?sysparm_article=KB3150595)

</td><td>

After the upgrade to Australia Patch 5, auto-increment columns are failing inserts with the duplicate\_key error

</td><td>

Australia Patch 5 \(AP5\) introduced a change to how certain database auto-increment sequences are managed. Under specific conditions, this change can cause the sequence used to generate new record identifiers to become invalid or out of sync with the database. When this occurs, attempts to create new records may fail. As a result, transient state records may not be created as expected in tables with the auto-increment field. This impacts many functional areas relying on the sequence record to track orders of states, logs or messages. This defect fix is included in the weekly patch due to its severe impact on multiple major functionalities across the platform.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2036311

 [KB3141836](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141836)

</td><td>

The SLA Percentage Timer flow action overwrites the paused task\_sla with stale GlideRecord state

</td><td>

The SLA Percentage Timer flow action \(Wait until N% of SLA Duration\) receives the task\_sla GlideRecord captured at flow-trigger time and passes it straight into SLACalculatorNG.calculateSLA. The pause guard inside calculateSLA reads pause\_time off that in-memory snapshot rather than re-checking the database. If another transaction pauses the task\_sla row between the flow trigger and the timer firing, the in-memory pause\_time is still nil, the guard is bypassed, and updateTaskSLAs overwrites duration/percentage/ time\_left/ business\_\* / has\_breached using running-state values. This silently corrupts the paused row. The same race also lets concurrent recalculations \(SLA engine business rules, Calc SLAs on Display, breakdown processor, SLA repair tool\) be overwritten by the stale flow GlideRecord. As a result, users see SLA timers that continue to accrue elapsed time while the underlying task is paused, and the breach state may flip incorrectly.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB2058369

 [KB3140571](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140571)

</td><td>

Midserver is unable to fetch credentials after upgrading to Zurich or Australia

</td><td>

In certain versions, there's a Unified Secrets Gateway \(USG\) service for credential management. During the upgrade to those versions, a system trigger script is designed to automatically execute and populate the sys\_secret\_identity\_group\_member table with the MID Server identity group mappings required for USG authentication. However, this trigger fails to complete successfully, leaving the table incompletely populated. As a result, the MID Server can't authenticate with USG and fails to retrieve credentials.

</td><td>

1.  Upgrade an instance from a version where USG doesn't exist to a Zurich or Australia version where USG exists.
2.  Check if sys\_secrets\_identity\_group\_member is populated with all entries from ecc\_agent.

 Expected behavior: All entries from ecc\_agent are present in sys\_secret\_identity\_group\_member.

 Actual behavior: There are no entries in sys\_secret\_identity\_group\_member.

</td></tr><tr><td>

Multi-Instance Framework

 PRB2040054

 [KB3146783](https://hi.service-now.com/kb_view.do?sysparm_article=KB3146783)

</td><td>

There's a flood of 'Unable to find vtable operation for operation id \{\}' messages that's generating millions of records in an instance for every Flow Designer execution

</td><td>

In a cloned instance, the root cause of the flood of errors messages 'Unable to find vtable operation for operation id \{\}' in the syslog is sn\_mif\_vtable\_ operation\_context.vtable \_operation is empty.

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

Activity and Subscriptions

 PRB2069585

 [KB3148451](https://hi.service-now.com/kb_view.do?sysparm_article=KB3148451)

</td><td>

The 'Customer history' tab keeps loading on the front-line case page

</td><td>

The tab never loads.

</td><td>

 

</td></tr><tr><td>

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

 PRB2017633

</td><td>

ActivityDBListener fires too many AMB messages on bulk deletes

</td><td>

 

</td><td>

1.  Open an incident in a workspace.
2.  Create two emails.
3.  Open sys\_email\_list.do.
4.  Set both emails' type to 'sent' 5.
5.  Notice that when returning back to the 'Incident' page, there should be two emails now.
6.  Open the Network panel in the DevTool's inspect window.
7.  Reload the page.
8.  Filter by 'amb'.
9.  Select the AMB message.
10. Select the 'Messages' tab.
11. Clear all of the messages.
12. In the sys\_email\_list.do, select one of the emails from step 4 and delete it.

Observe that in the 'Network tab', there should be an AMB message for the deleted email.

13. In /sys\_email\_list.do, delete multiple emails that are 'send-ready'.Observe that in the 'Network' tab, there should be no messages for those deleted emails.
14. In /sys\_email\_list.do, delete multiple emails that are 'send-ready' and the other email from step 4.

 Observe that in the 'Network' tab, there should only be 1 message for the other email.

</td></tr><tr><td>

Activity Stream

 PRB2032224

</td><td>

Orphaned Dependent fields in the initial audit event causes an exception in SysAuditRule

</td><td>

When the support audit is passed to findFirst, which filters out support audits, it finds an empty stream and throws 'IllegalStateException: Unreachable code reached.' The exception is caught, but it causes retrieveEvents to return zero events, leaving the workspace activity stream completely empty.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2060131

</td><td>

When table rotation is set up for sys\_audit\_relation, audit relationship events don't display in a workspace

</td><td>

 

</td><td>

1.  Navigate to **Table Rotations** \(sys\_table\_rotation\).
2.  Add a record for sys\_audit\_relation.
3.  Set the type to 'Extension' and the 'Duration' to 1 hour or less.
4.  Create new audit relationship changes.

 Expected behavior: The audit relationship changes are displayed in the workspace Activity Stream.Actual behavior: The audit relationship changes are not displayed.

</td></tr><tr><td>

Activity Stream

 PRB2066570

</td><td>

In Activity stream primary Journal **field** ordering, work\_notes are displayed before comments in UI16 and Service Portal

</td><td>

The activity stream on task records \(Incidents, Changes, etc.\) incorrectly defaults to the 'Work Notes' input instead of 'Comments' in both the platform UI and Service Portal. This affects user workflow as agents may inadvertently post internal work notes when intending to post user-visible comments. Additionally, custom **Journal** fields configured on tables don't appear in the Service Portal activity stream widget.

</td><td>

1.  Open any task-extended record \(for example, Incident\) in UI16 or Service Portal.
2.  Observe the activity stream input area.

 Expected behavior: 'Comments' is the default selected journal input field.

 Actual behavior: 'Work Notes' is the default selected journal input field.

</td></tr><tr><td>

Activity Stream

 PRB2073311

</td><td>

Build backend graphQL endpoint for List Activity

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2073313

</td><td>

Provide supplemental data for returned records on the new back-end for list activity

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2073315

</td><td>

Review DT APIs for security

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB2060584

 [KB3143279](https://hi.service-now.com/kb_view.do?sysparm_article=KB3143279)

</td><td>

The 'Set logged out agent offline' script action shouldn't touch presence states when 'disable\_inactivity\_check' is set to true

</td><td>

A live human agent is made offline whenever they log out. However, the log out script action should bypass the agents in those presence states that have 'disable\_inactivity\_check' set to true.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2063949

</td><td>

Some messages are hidden on the agent's side when hideControl is true and contains searchText

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2068933

</td><td>

A workspace error is observed when handling incomingmessaging interactions in Agent Workspace

</td><td>

In both scenarios, the error modal occurs.

</td><td>

Scenario 1:

 1.  Open a messaging interaction in the CSM workspace.
2.  As a agent, go to any other tab than the ongoing interaction.
3.  Send one or more messages from the requester.
4.  Ensure sure the ongoing messaging count is visible.
5.  Switch to the current interaction

 Observe the error modal.

 Scenario 2:

 1.  Open a messaging interaction in CSM workspace.
2.  Send one or more messages from the agent/requester.
3.  Refresh the page.

 Observe the error modal.

</td></tr><tr><td>

Agile Development

 PRB2057888

</td><td>

Add script include to gate PWS-CWM functionalities

</td><td>

 

</td><td>

 

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

AI Agents \(Glide Family\)

 PRB2061451

</td><td>

The topic tool execution status is 'success to completed' before the tool completes

</td><td>

 

</td><td>

1.  Create a topic tool with input nodes in it.
2.  End the topic execution if the user replies back.
3.  Add it to the agent as a tool.

 Observe that the sn\_aia\_tools\_execution record execution status should be marked as 'Success' only when topic completes.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2069685

</td><td>

EG mini doesn't work in the KG tool in AIA Agent

</td><td>

 

</td><td>

1.  Create an AIA agent with the KG tool.
2.  Select **EG mini schema** and a tag with it.
3.  Try to run the agent which calls the tool.

Observe that the tool call fails.

4.  Select **EG as schema**.

 Observe that it works as expected.

</td></tr><tr><td>

AI Agents \(Glide Family\)

PRB2070503

</td><td>

Generic tool for mutate operations for agent-orchestrator-v2

</td><td>

 

</td><td>

1.  Enable domain separation.
2.  Start conversations from different domains.
3.  Ensure records are not available cross the domain.
4.  Run the abandoned conversation job.

 Notice that the conversations do not get properly faulted and throws an exception.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2074132

</td><td>

meta.agentId is 'null' for assistant-wired tools, breaking agentic\_context in OGScriptToolExecutor

</td><td>

Tools that are wired directly to assistants a not to an agent have always had an empty **Agent** field on their tool M2M record. Previously this was masked because DARE resolved the default root agent \('Otto'\) regardless, so meta.agentId was always populated in the tool's input request. Now that the default-agent resolution is gone, meta.agentId comes through as null for these assistant-wired tools. The OGScriptToolExecutor depends on meta.agentId to populate the **agentic\_context** field on the tool execution. With meta.agentId as 'null', the agentic\_contex is no longer populated for any tool wired directly to an assistant.

</td><td>

1.  Take a tool whose M2M record is wired to an assistant directly.
2.  Ensure the **Agent** field on that M2M record is empty.
3.  Invoke the tool through that assistant.
4.  Inspect the tool's input request.

 Observe that 'meta.agentId' is null, and OGScriptToolExecuto does not populate the agentic\_context.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2074803

</td><td>

Implement a scriptable method for channels instead of restmessagev2

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2074876

</td><td>

Process A2A primary asynchronous responses to offglide via Hybrid Queue

</td><td>

Currently, external agent \(A2A\) primary async responses land in sn\_aia\_external\_agent\_primary\_async\_responses and are forwarded to offglide via a synchronous, in-transaction path \(A2aPrimaryAsyncEventHandler\) guarded by a raw Mutex. This blocks the event-delegator thread for the duration of the DB read and offglide POST + mark-processed sequence, and doesn't benefit from the platform's existing overflow/shutdown safety net.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2074920

</td><td>

Enable the passing of the assistant context from AI Agents to GAIC

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2078415

</td><td>

Add sys\_og\_conversational\_cache\_http\_log with request-ID dedup for setCache

</td><td>

CCS adds a retry to its glide calls, and a re-tried SET\_CACHE re-executes the configuration row's set\_script with no record that the original attempt already applied.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2059453

</td><td>

True up version for the AIXF Store app

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

AI Experience Framework - Glide

 PRB2062421

</td><td>

The ACL 'Type' dropdown list does not include aiux\_page, aiux\_widget, or aiux\_dashboard options

</td><td>

None of these types are available when they should be included as selectable options.

</td><td>

1.  Navigate to sys\_security\_acl.list.
2.  Select **New** to create a new ACL record.
3.  Open the 'Type' dropdown list.
4.  Search for aiux\_widget, aiux\_page.

 Expected behavior: The 'Type' dropdown list should include aiux\_page, aiux\_widget, and aiux\_dashboard as selectable options.

 Actual behavior: The AIUX types are not present in the 'Type' dropdown list.

</td></tr><tr><td>

AI Gateway - Security

 PRB2041348

</td><td>

The autogenerated fake sys\_ids in AIG should be fixed

</td><td>

Fix the files sys\_id and corresponding ITs and UTs.

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

 PRB1918638

</td><td>

Indexing fails for the batch due to a corrupted GZIP trailer error

</td><td>

Two errors occur in the system log, resulting in some of the KBs in the batch to not be indexed.

</td><td>

1.  Attach the problematic attachment of one KB article.
2.  Index the Knowledge indexed source.
3.  Check the system log.

 Notice that there are two notable errors, 'Corrupt GZIP trailer' and 'Internal Server Error.' As a result, some KBs in the same batch are not indexed due to the exception.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1925971

</td><td>

The 'Category' and 'Catalog' facets for catalog items are not using the translated values

</td><td>

The facet filters remain untranslated, even though the facet filters under 'Categories' and 'Catalogs' have translated values provided.

</td><td>

1.  Set up AIS in the /esc portal with the default esc search application and profile.
2.  Ensure the search application has these two facets configured:
    -   sc\_cat\_item.sc\_catalogs
    -   sc\_cat\_item.category
3.  Activate another language plugin, such as Italian.
4.  Find an sc\_cat\_item that is searchable.
5.  Navigate to the **category.sc\_catalog** field.
6.  For that catalog, ensure there is an entry in the sys\_translated\_text table with the following:
    -   Document: Catalog sys id
    -   Field name: **Title**
    -   Language: Italian
    -   Table name: 'sc\_catalog'
    -   Value: A translated value
7.  For that category, make sure there is an entry in the sys\_translated\_text table with the following:
    -   Document: Category sys id
    -   Field name: **Title**
    -   Language: Italian
    -   Table name: 'sc\_category'
    -   Value: A translated value
8.  Switch to the Italian session.
9.  Open to the /esc portal.
10. Search for the catalog item from before.

 Expected behavior: The corresponding facet filters under 'Categories' and 'Catalogs' should be translated into the Italian values provided.

 Actual behavior: The facet filters are still in English.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2029415

</td><td>

When creating a record, recordClassName becomes the parent class

</td><td>

As a result, selecting the search result in the Service portal re-directs users to a malicious form.

</td><td>

1.  Open sc\_cat\_item\_guide list /sc\_cat\_item\_guide\_list.do%3Fsysparm\_clear\_stack%3Dtrue.
2.  Create a new record with the following:
    1.  Catalogs: Technical Catalog
    2.  Category: Services
3.  Ensure the 'Category' is selected from 'Recent selections'.
4.  Open the AI Search Preview with the following:
    1.  Search Application: 'ESC Portal Default Search Application
    2.  Card View: Raw
    3.  Output search words: the word you input on 2.
5.  Notice the result is 'searchResults': ... 'recordClassName': 'sc\_cat\_item', when it should be 'sc\_cat\_item\_guide'.
6.  Update the record created in step 2.
7.  Search in AI Search Preview again.

 Observe that the values have been updated correctly: 'searchResults': ... 'recordClassName': 'sc\_cat\_item\_guide'.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2033435

</td><td>

TSTranslationReference loads all sys\_translated rows for a field instead of filtering to the indexed record's value

</td><td>

When indexing a record that has a **Reference** field pointing to a table whose **Display** field is a translated\_field type, TSTranslationReference calls TranslationUtil.getTranslatedFieldValues\(\), which queries sys\_translated with only name= table and element= field – no VALUE filter. This loads all translations for every value of that field across all records.

</td><td>

1.  Have a large sys\_translated table with 50k+ rows for a single table/field combination.
2.  Enable a language plugin.
3.  Index a record that has a **Reference** field pointing to a table whose **Display** field is a translated\_field type. For example, a table referencing a question where the question\_text is translated\_field.

 Observe that index events take 5s to 8s each, and the message at occurs, 'QueryWarning: 'Large Table' on sys\_translated with query name=&amp;lt;table&amp;gt;^element=&amp;lt;field&amp;gt; \(no value filter\).'

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2050402

</td><td>

Improve search relevancy for the Hybrid search on portal for 'OR' mode with a matching threshold of 80%

</td><td>

By default, the search is performed in 'AND' mode for Hybrid search on portal, which is ignoring the q.threshold parameter completely.

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

 PRB2058047

</td><td>

Indexing with multiple semantic indexing configurations with the same name on different models isn't working

</td><td>

When multiple semantic index configurations are created on the same datasource with the same **Semantic** field name but different embedding models, only the first configuration is loaded into the active **Semantic index** field cache. Subsequent configurations are silently ignored, so ingestion and search only use one embedding model for that field. Only one embedding model is used for indexing and search when multiple semantic index configurations share the same **Semantic** field name. Additional configurations with the same **Semantic** field name are not visible in getSemanticIndexFieldMapping\(\). No error or warning is logged when the duplicate-name configurations are skipped. Thus, multi-embedding model support for a single **Semantic** field is broken. Configurations are silently lost during cache population. This affects ingestion, search, and any callers that rely on getSemanticIndexFieldMapping\(\).

</td><td>

1.  Create two active ais\_semantic\_index\_configuration records on the same datasource with the same semantic\_field\_name but different embedding\_models values.
2.  Add valid component fields via ais\_semantic\_component\_field for each record and set a valid semantic\_snippetization\_configuration.
3.  Flush the datasource object cache \(AisConfigurationCacheManager.flushDatasourceObjectCache\(\)\).
4.  Call AisConfiguration.get\(\).getSemanticIndexFieldMapping\('kb\_knowledge','kb\_knowledge'\).

 Observe that only one SemanticFieldConfiguration is returned for semantic\_search and the other is silently dropped.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2070763

</td><td>

Impersonation for RAGRetrivalAPI isn't required

</td><td>

This feature isn't required anymore. Going forward, it will be implemented in a different way. It is currently behind ais\_admin role but requires other impersonation checks which are missing currently.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2073296

</td><td>

Add handlers to convert labels for the field types 'Table Name' and 'Field Name'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2073297

</td><td>

Searchability Tracer for detailed ACL and User Criteria diagnostics API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2073298

</td><td>

Search Evaluation application

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2073301

</td><td>

Diagnostics API for searchability

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2073303

</td><td>

Catalog enrichment for Glide AIS

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2073307

</td><td>

Expanding the **Search signal** fields logged in glide AIS

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2073308

</td><td>

Catalog enrichment for glide AIS

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2076604

</td><td>

Expose glide.ais.query.server\_side\_reranker\_enabled in BP0 for reranker to be enabled by default

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search for Service Portal

 PRB1998368

</td><td>

AI Search in Enhanced Chat's full page experience throws a console error

</td><td>

The error, 'Uncaught TypeError: \(\(n.event.special\[g.origType\] \|\| \{\}\).handle \|\| g.handler\).apply is not a function : js\_includes\_sp\_libs.jsx at HTMLDivElement.dispatch' occurs in the console.

</td><td>

1.  Open the 'Assistant Designer' page for Now Assist in Virtual Agent.
2.  Enable Enhanced Chat.
3.  Open the full page experience for Employee Center portal.
4.  Open the /esc portal.
5.  Select the **Search box** or search anything in the typeahead search widget.

 Observe console error, 'Uncaught TypeError: \(\(n.event.special\[g.origType\] \|\| \{\}\).handle \|\| g.handler\).apply is not a function : js\_includes\_sp\_libs.jsxat HTMLDivElement.dispatch.'

</td></tr><tr><td>

AI Search for Service Portal

 PRB2062818

</td><td>

The sparkle Otto icon in a portal search input has an incorrect color when Enhanced Chat is turned on

</td><td>

The sparkle Otto icon before the input placeholder is not visible because it is same color as the background.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1893398

</td><td>

Attempting to recreate a scenario where entries in the search term is empty in the sys\_search\_event table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2072005

</td><td>

The fix for PRB1935844 was overwritten during a merge

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB2073716

 [KB3148324](https://hi.service-now.com/kb_view.do?sysparm_article=KB3148324)

</td><td>

For non-admin users, search results and suggestion navigation on portals are redirecting to platform view

</td><td>

After upgrading to Australia Patch 5 or Zurich Patch 12, non-admin users performing a search on a portal \(for example, /esc\) experience incorrect navigation. Selecting a regular search result or a suggested search result opens the record in the platform view rather than within the portal.

</td><td>

Scenario 1:

 1.  Upgrade an instance to Australia Patch 5 or Zurich Patch 12.
2.  Log in as a non-admin user.
3.  Perform a search on a portal, such as /esc or /sp.
4.  Select the regular search result that is returned.

 Observe that the record opens in platform view instead of the portal.

 Scenario 2:

 1.  Upgrade an instance to Australia Patch 5 or Zurich Patch 12.
2.  Log in as a non-admin user.
3.  Enter a search term on a portal, such as /esc or /sp, without submitting the search.
4.  Select a suggested search result in the typeahead drop-down list.

 Observe that the record opens in platform view instead of the portal.

</td></tr><tr><td>

Analytics Data API

 PRB2002190

</td><td>

The error log should be suppressed in a prefetch job

</td><td>

The user is getting the error log, 'com.glide.rest.domain.ServiceException: Invalid configuration in their syslog daily at an interval of 15 minutes. This is a cause of concern as the error logs are frequent and does not give complete information to the user to stop them.

</td><td>

1.  Open any Zurich instance.
2.  Open the syslog table.

 Observe that there is a message containing 'com.glide.rest.domain.ServiceException: Invalid configuration.'

</td></tr><tr><td>

Analytics Data API

 PRB2019716

</td><td>

Multiple elements from a single filter can't be applied to an 'COUNT DISTINCT' or 'AVERAGE' indicator with 'Show filter as separate series'

</td><td>

When multiple elements are selected and applied from a single filter to a visualization based on an automated indicator, the filter is not applied. The 'Network' tab in the developer console shows, 'Indicator does not support multi-element aggregation'. This should not occur for automated indicators. This issue only occurs if the 'facts' table is a database view.

</td><td>

1.  Create a PAR dashboard.
2.  Add a line visualization with the base instance indicator, 'Number of over-due incidents' as the data source.
3.  Add a filter with 'Indicators' as the filter source type, and 'Assignment Group' as the indicator breakdown.
4.  Under 'Data to filter,' add 'Indicators with Assignment Group breakdown'.
5.  Select two elements from the filter and apply it.

 Observe that the filter is not applied, in the 'Network' tab in the developer console, and an error occurs.

</td></tr><tr><td>

Analytics Data API

 PRB2029673

</td><td>

Data Visualization Library quick-access cards return '0' under the 'Bookmarked' scope when the grid sees bookmarks correctly

</td><td>

On the Data Visualizations Library page, the quick-access cards display 0 when the Bookmarked type-choice filter is applied, even when the grid below correctly shows the bookmarked vizes. The same card filter without the Bookmarked scope returns the correct count.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2050497

</td><td>

The report.view events are generated with the wrong sys\_id and are erroring out in Australia

</td><td>

These events seems to be created from the Platform Analytics Dashboard home page.

</td><td>

1.  Open an instance.
2.  Navigate to the sysevent table
3.  Use the filter conditions, 'Queue is report\_view'.
4.  Notice the state is 'error'.
5.  Check the instance column.

 Notice that the sys\_id's are not 32 characters, and from the 'Report' view, events process jobs logging the event have an error due to an invalid reference.

</td></tr><tr><td>

Analytics Export API

 PRB1971222

</td><td>

'Omit if no records' isn't honored for score visualizations

</td><td>

If the record count is zero for the visualization, the email with the exported data visualization PDF should not be generated when the **Omit if no records** checkbox is checked.

</td><td>

1.  Create a data visualization of the type 'score', 'gauge', or 'dial'.
2.  Add a data source and conditions such that the record count is zero. For example, add a condition like 'active is true and active is false' which will make the record count zero.
3.  Save the data visualization.
4.  Schedule the export of data visualization to a PDF.
5.  Enable the **Omit if no records** checkbox.
6.  Select **Send now** from the 'Scheduled export' page.

 Expected behavior: The email shouldn't be generated when the record count is zero for the visualization.

 Actual behavior: The email gets generated even though the **Omit if no records** checkbox was selected.

</td></tr><tr><td>

Analytics Export API

 PRB2057980

</td><td>

The visualization creator is not able to select existing highlight value configurations

</td><td>

The visualization creator couldn't select a highlighted value configuration because the visaualization creator role doesn't have read access for the sys\_ux\_highlighted\_value\_config table.

</td><td>

1.  Create a highlight value configuration for an incident table as an admin user.
2.  Create a list visualization \(viz\_creator role\).
3.  Select the table as 'incident'.
4.  Enable the fetch highlighted value.
5.  Search for the highlight configuration created above.

 Observe that no result is returned in highlight value dropdown list, even though the the visualization creator should be able to read and use existing highlight value configurations.

</td></tr><tr><td>

API Access Policies

 PRB2065453

</td><td>

The RESTAPIAccessScopeRepo map overwrite loses required authentication scopes when two sys\_api\_access\_scope records share the same API signature

</td><td>

A 403 'User Not Authorized' error occurs.

</td><td>

1.  Install and activate both ServiceNow Otto for Document Voice and Dynamic Guidance applications.
2.  Confirm both sys\_api\_access\_scope records are active for the SNGenerativeAI API path sn\_generative\_ai/extensions, with all apply-all flags \(apply\_all\_methods, apply\_all\_resources, apply\_all\_versions\) set to 'true'.
3.  Call GET /api/sn\_generative\_ai/extensions/live-llm-configuration?solutionCapability=smartdocs\_voice\_qna with the Document Voice token.

 Observe that if the Dynamic Guidance Authentication Scope record loads last into the RESTAPIAccessScopeRepo's map, the call returns the error, '403 User Not Authorized - Missing required api access scope: Dynamic Guidance Auth Scope'.

</td></tr><tr><td>

Application Manager

 PRB2022268

 [KB3156065](https://hi.service-now.com/kb_view.do?sysparm_article=KB3156065)

</td><td>

The application manager sys\_app\_version displays duplicate records for the same application and version, which is causing the app to be 'Installation blocked'

</td><td>

As part of the AI testing, it's been observed that the app installations are blocked. The sys\_app\_version displays duplicate records for the same application. This causes the app installations to be blocked, despite the app versions being available as well as the license checks having successfully completed.

</td><td>

1.  Navigate to an instance.
2.  Navigate to App Manager.
3.  Open any app \(e.g. sn\_ai\_itsm\_cont\) which is licensed and validated on CI \(usageanalytics\) prod, but has yet showed 'Not Licensed'.
4.  Select **Install**.
5.  It just fails with 'Installation blocked' on that app itself.
6.  Open sys\_app\_version table.
7.  Check the app/scope id.

 Expected behavior: It should have only 1 record for that app and a specific app version.

 Actual behavior: It has multiple records for the same app and app version.

</td></tr><tr><td>

Application Manager

 PRB2056916

</td><td>

Skip a license-blocked status for all dependencies in DependencyProcessor

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB2074238

</td><td>

Now Assist to Otto Rename for Application Manager

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Appointment Booking

 PRB1992532

</td><td>

The 'Appointment Booking Select' widget fails to load for the French language \(i18n\) due to an AngularJS Lexer error

</td><td>

When the system language is set to French, the appointment booking slot selection widget does not load. The sn-appointment-booking-select widget fails to render, and console errors are observed. As a result, booking slots are not displayed.

</td><td>

1.  Impersonate as system administrator.
2.  Change the language to normal French.
3.  Open the page '/esc?id=appointment\_booking'.
4.  Select any reason and appointment type..

 Notice that the appointment booking slot selection widget is not loading.

</td></tr><tr><td>

Asset Management

 PRB2069476

</td><td>

Let asset managers review and confirm extracted contract metadata in a 'Playbook' tab so that they can ensure accuracy before saving to the contract record

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

Authentication Factors

 PRB2072957

</td><td>

Enhance telemetry for Authentication Factors

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2074233

</td><td>

SMS OTP Authentication for human-assisted voice interactions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB2037962

</td><td>

The MCP Server registration with the Client Credentials grant fails when created via AI Agent Studio

</td><td>

When registering an MCP Server in AI Agent Studio using the Client Credentials grant type \(manual registration\), the form doesn't get submitted. The same MCP server registration works correctly when the Connection &amp; Credential alias is created manually outside AI Studio on the same instance. It also works correctly when the flow is exercised via Postman/curl directly against the MCP server's '/token' endpoint. The Authorization Code grant type continues to work end-to-end through AI Studio.

</td><td>

1.  Log in to an instance.
2.  Navigate to **AI Agent Studio** &gt; **Settings**.
3.  Select **Manage MCP Servers**.
4.  Select **New** to add a new MCP server.
5.  Enter the MCP URL.
6.  Select **Manual Registration**for Client Registration Type.
7.  Select **Client Credentials**for Grant Type.
8.  Select **Client Secret Post**for Token Authentication Method.
9.  For Client ID, enter 'svc\_oodp\_dataaccess'.
10. For Client Secret, enter a valid secret.
11. For Auth Scopes, enter 'openid'.
12. Enter the token URL.
13. Select **Add**.

 Expected behavior: The MCP Server registers successfully, like it does for Authorization Code grants and for manually created Connection &amp; Credential aliases.

 Actual behavior: The form doesn't get submitted. The **Add** button is blocked until the authentication URL is provided, which ideally would not be required for the Client Credentials grant type.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2038798

</td><td>

Cannot read the properties of the undefined \(reading 'message'\) after upgrading to Australia

</td><td>

The sys\_processor\_0af16f2d5363101034d1ddeeff7b12b6.xml redirects requests to a new UI page. However, this new UI page introduced in the Australia release is not supported by ATF's 'Navigate to module' step. It is relying on the gsft\_main to load the g\_form on the page. This breaks the custom logic to get the g\_form on the page, and errors occur in the console.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2053799

</td><td>

Text and cosmetic changes for ServiceNow Otto

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB2054701

 [KB3147951](https://hi.service-now.com/kb_view.do?sysparm_article=KB3147951)

</td><td>

A 'Host CPU Load Critical' alert is caused by ATF Scheduler jobs with a large amount of sys\_atf\_modified\_record\_m2m records generated

</td><td>

ATF Tests that cause a large number of modified records \(stored in the sys\_atf\_modified\_record and sys\_atf\_modified\_record\_m2m tables\) cause high application server CPU usage as well as high memory usage. When users check to see if a test can run now, they attempt to first acquire exclusive access to all necessary records. If the list of modified records is very large, then users can spend a lot of time trying to determine if the test can run now, and this can cause high CPU usage on the application server and high memory usage in the application node.

</td><td>

 

</td></tr><tr><td>

Benchmarks

 PRB1989154

</td><td>

BenchmarkClientUtil.constructPayload fails to fetch data for Global-scope PA Scorecards

</td><td>

Running the background script shows that the PAScorecard.query\(\) does not return results for Global-scope indicators, causing constructPayload to fail. For benchmarked indicators that exist in the Global scope, the constructPayload method fails to fetch PAScorecard details and returns 'null'. Because the PAScorecard records are not retrieved, the Global-scope indicators are not included in the upload payload, and scores are not uploaded to the central instance. As a result, instances do not receive benchmark scores for these indicators.

</td><td>

 

</td></tr><tr><td>

Cache

 PRB2025917

</td><td>

Query Cache metrics aggregator do not delete data older than 14 days

</td><td>

The property 'glide.query\_cache.aggregate\_metrics.retention\_days' controls how many days old data should be deleted from the 'qc\_instance\_metric' table when the job runs.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2017688

</td><td>

New RCAs from the Knowledge Center to HR Core to use Open Prompt

</td><td>

The Advanced Knowledge Editor page in HR Agent Workspace is being used, and contains Open Prompt, which is interactable and helps create an articles using Gen AI. For the Open Prompt to work without any issues, new RCAs are required.

</td><td>

1.  Activate the Knowledge Recommendation plugin and Article Optimization plugin.
2.  From the Knowledge Management properties, enable the ECE.
3.  Create an article from the related list of any HR case.
4.  Add a link in the article.

 Observe that there are RCAs from the Knowledge Center to HR Core.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2039604

</td><td>

The HR L1 Specialist is missing Restricted Caller Access records from the installation

</td><td>

After installing the HR L1 Specialist on a zbooted Australia instance, Restricted Caller Access records were created from ZTSD and Now Assist AI Agents scopes to the HR Core scope which that prevent the specialist from completing its tasks.

</td><td>

1.  Create a new instance or zboot an existing one.
2.  Upgrade the instance to Australia.
3.  Install the HR L1 Specialist along with all required dependencies for the HRSD product.
4.  Configure the HR L1 Specialist.
5.  Assign the specialist to a 'Ready' HR Case.

 Observe the Restricted Caller Access table to attempting to find the generated RCA records.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2070954

</td><td>

RCAs are required for predict and transfer usecases

</td><td>

There should be RCAs for the new tool call when the sys\_id isn't mentioned in the objective when invoking the 'Predict HR Service and Transfer' case workflow.

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB2057866

</td><td>

Target tables are missing required tracking fields for multi-case creation

</td><td>

For multi-case creation, the target records do not have the required tracking fields to capture **Template Item** and **Template Execution**. As a result, the created Case and Case Task records cannot be fully tracked with associated Template item and execution. To support multi-case creation, the fields **Template item** and **Template Execution** need to be added to the sn\_customerservice\_case and sn\_customerservice\_task tables.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2061984

</td><td>

On insert, if a template writable value is modified, the modification is overwritten by the template value

</td><td>

 

</td><td>

1.  Create a template for the normal mode which sets the **Short Description** field to **Test value from template**.
2.  Run the scripts background.

 Observe that the **Short description** is set to the template value, not the value set during the creation.

</td></tr><tr><td>

Column Level Encryption

 PRB2006384

</td><td>

Attachments from the sn\_si\_incident table are created with a different hash

</td><td>

There appears to be some sort of unique hashing algorithm applied only to the sn\_si\_incident table. Due to this hashing algorithm, attachments are being duplicated in the remote process sync feature.

</td><td>

1.  Attach an attachment to any table other than \[sn\_si\_incident\].
2.  Attach an attachment to the \[sn\_si\_incident\].

 Notice that when comparing the two hashes, two unique hashes are generated for the same file.

</td></tr><tr><td>

Communities

 PRB2003810

</td><td>

Views in Event Content are displaying as '2,147,483,648'

</td><td>

When the event is created through the platform, the events view count is showing high number in the community portal.

</td><td>

1.  Attempt to create an event from the platform \(sn\_communities\_event table\).
2.  Open the same event from the communities portal.
3.  Go back and open the same event again.

 Notice that the views are showing as 2,147,483,648.

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

Core UI Interactive Filters

 PRB2073810

 [KB3154499](https://hi.service-now.com/kb_view.do?sysparm_article=KB3154499)

</td><td>

Selecting the pie chart legend/label does not filter visualizations correctly

</td><td>

The pie visualization acting as an interactive filter does not apply the filter correctly when the legend items are selected.

</td><td>

1.  Navigate to the classic reporting module.
2.  Create a new visualization with the following:
    -   Table: Incident
    -   Type: Pie
    -   Group by: Assignment group
3.  Save it.
4.  Navigate to the classic dashboard module.
5.  Create a new dashboard.
6.  Add the '\{Debug\}' interactive filter.
7.  Add the visualization created in step 2.
8.  Edit the visualization widget.
9.  Select **Act as interactive filter**.
10. Select any legend item.

 Expected behavior: It should show a filter condition being applied.

 Actual behavior: The 'Debug' homepage filters shows no filters applied.

</td></tr><tr><td>

Core UI Responsive Dashboards

 PRB2034505

 [KB3085059](https://hi.service-now.com/kb_view.do?sysparm_article=KB3085059)

</td><td>

A Platform Analytics \(PA\) dashboard overview can't load any dashboards

</td><td>

If all of the following conditions are met, the dashboard doesn't appear on the 'All' tab of PA dashboard 'Overview' page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Customer Service Case Action Status

 PRB2011771

</td><td>

Keep the 'Major Case' related list consistent in app-csm-action-status and app-major-issue-management

</td><td>

If users reinstall or upgrade app-csm-action-status again after Major Case is installed, the related list on Major Case is different. The newly added-in app-major-issue-management is gone.

</td><td>

 

</td></tr><tr><td>

Customer Service Core

 PRB2037285

</td><td>

There's slowness on every page/action for the account executive persona in a perf instance

</td><td>

When trying to perform any action in a perf environment with the account executive persona, the user observes slowness from one to two minutes.

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB2062954

</td><td>

Creating knowledge from a case doesn't populate the **kb\_issue** field

</td><td>

The **kb\_issue** field is mapped in the Advanced Field Mapping of the CSM Table Map 'Case KCS Article'. It is expected to populate the first comment from the case.

</td><td>

1.  Set the system property sn\_customerservice.enable\_knowledge\_kcs to 'true'.
2.  Open a case that contains one or more comments.
3.  Select **Create Knowledge**.

 Expected behavior: The **kb\_issue** field of the newly created Knowledge article is populated with the first comment from the case.Actual behavior: The **kb\_issue** field of the newly created Knowledge article is left blank.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2051225

 [KB3141251](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141251)

</td><td>

GlideAggregate and Platform Analytics pivot fails with 'must appear in the GROUP BY clause' when grouping or sorting by a translatable field in a non-English language

</td><td>

The pivot shows 'No data available.'/'Aucune donnee disponible.' instead of the data. The node log shows com.glide.db.GlideSQLException with the PostgreSQL error, 'ERROR: column 'sc\_cat\_item3.name' must appear in the GROUP BY clause or be used in an aggregate function.'

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1971093

</td><td>

One-time update/delete job conditions shouldn't contain Javascript

</td><td>

From PRB1866906, if the query brought over from the table view includes javascript, the query must be removed entirely. Potential for data loss may occur.

</td><td>

1.  Log in as user with the admin role.
2.  Browse to /incident\_list.do?sysparm\_query=caller\_id=javascript:gs.getUserID\(\).
3.  Hover over the 'Opened' column.
4.  Select the **Column Options** \(3 vertical dots/hamburger menu\).
5.  Select **Data Management** &gt; **Delete all with preview**.

Notice that the user is navigated to a screen showing the sys\_dm\_delete record.


 Expected behavior: The condition is retained, but the javascript/dynamic content in the conditions should not be stored. It should be 'caller\_id=the current user's id&gt;'.

 Actual behavior: The condition is removed since it includes javascript, as it is in PRB1866906.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2015145

</td><td>

The bulk archive restore performs poorly with the columnar archive table

</td><td>

 

</td><td>

1.  Test the bulk archive restore with a clone instance.
2.  Migrate ar\_incident to the columnar storage.
3.  Run bulk restore with a list of ar\_incident records.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2015146

</td><td>

DocumentIDTableFixer queries perform poorly against the columnar archive tables

</td><td>

 

</td><td>

1.  Migrate ar\_incident to the columnar storage.
2.  Run the DocumentIDTableFixer job.

 Observe the check query performance.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2017978

</td><td>

The RefCopy job experiences performance issues for columnar archive tables

</td><td>

The slow query table shows the average SQL execution time.

</td><td>

Enable the 'Retain reference' option for the incident table's archive rule.

 Notice that when checking the slow query table, the user can find the average SQL execution time.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2025948

</td><td>

Exclude raptordb columnar tables from the clone

</td><td>

 

</td><td>

Clone from the source to the target with the columnar table plugin active.

 Expected behavior: Archive tables are not cloned.

 Actual behavior: Archive tables are cloned.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2036545

</td><td>

Archive table mutability causes performance problems

</td><td>

The data should be immutable other than archive destroy. However, certain operations cause mutability, such as cascade delete or reparenting.

</td><td>

Archive some data into an archive table, like ar\_u\_table1.

 Expected behavior: The data is immutable other than archive destroy.

 Actual behavior: Certain operations, such as cascade delete or reparenting, cause mutability.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2039000

</td><td>

ArchiveResolver doesn't work with the columnar archive table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2039435

</td><td>

The URC could run slowly when executing the row count estimation on the columnar table

</td><td>

 

</td><td>

1.  Install Live Archive on an instance.
2.  Offload a large amount of data.
3.  Create a URC rule like for sys\_flow\_plan\_context\_binding which has a document table reference.

 Expected behavior: The URC runs as expected.

 Actual behavior: The row count estimation query is very slow.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2039436

</td><td>

The URC could run slowly when executing row count estimation on the columnar table

</td><td>

 

</td><td>

1.  Install Live Archive on an instance.
2.  Offload a large amount of data.
3.  Create a URC rule for sys\_flow\_plan\_context\_binding which has a document table reference.

 Observe the time it takes for the URC to run.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2039845

</td><td>

The sys\_attachment\_doc\_columnar table is not created in the gateway DB when the sys\_attachment group is on a gateway

</td><td>

The sys\_attachment\_doc\_columnar table is created in the primary DB instead of the gateway DB, and the list view shows no records.

</td><td>

1.  Set up an instance with a gateway database configured for the sys\_attachment table group \(for example, sys\_attachment, sys\_attachment\_doc, and sys\_attachment\_doc\_v2 are routed to the gateway DB\).
2.  Activate the com.glide.data\_management.columnar\_attachments plugin on the instance..
3.  Verify that the sys\_attachment\_doc\_columnar table gets created in the gateway DB.

 Expected behavior: The sys\_attachment\_doc\_columnar table is created in the gateway DB, the same as sys\_attachment and sys\_attachment\_doc, and the list view displays the migrated records.

 Actual behavior: The sys\_attachment\_doc\_columnar table is created in the primary DB instead of the gateway DB. However, the list view shows 0 records because the platform queries the gateway DB where the sys\_attachment group is routed, but the data resides in the primary DB.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2051706

</td><td>

The sys\_service\_endpoint\_attribute exclusion rule is in the incorrect package

</td><td>

The sys\_service\_endpoint\_attribute clone exclusion record is in the s3\_standard package.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2054270

</td><td>

Table cleaner performance issues on columnar archive tables

</td><td>

 

</td><td>

1.  Create a table cleaner rule targeting a columnar archive table.
2.  Execute the table cleaner job.

 Observe whether the rule is deactivated or not, and if no records are cleaned.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2055841

</td><td>

The archive DDL sync default-value back-fill times out on columnar archive tables

</td><td>

The archive table default-value back-fill does not complete.

</td><td>

1.  Have a source table \(for example, sn\_customerservice\_case\) with a columnar archive table \(ar\_sn\_customerservice\_case\) that contains a meaningful number of rows.
2.  Add a new column with a non-null default to the source table such as, auto\_created\_case \(boolean, default '0'\).

Notice that ArchiveDDLChangeListener fires and synchronizes the schema change onto the archive table. Because the column has a default, DBUtil.updateDefaultValues back-fills existing rows via the chunk-copy path.

3.  Observe the per-chunk statement.

 Expected behavior: Adding a defaulted column to a source table with a columnar archive table should complete the archive schema sync without timing out. The back-fill should either avoid the sys\_id-range chunked UPDATE strategy on columnar archive tables or use a columnar-appropriate approach.

 Actual behavior: Each chunk UPDATE runs a full column-segment scan \(no sys\_id index on the columnar archive table\), executes serially one chunk at a time, and times out. The archive table default-value back-fill does not complete.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2057672

</td><td>

Global search performance issue with columnar archive tables

</td><td>

 

</td><td>

1.  Install Live Archive on an instance.
2.  Offload a large amount of data, including some task or problem tables.
3.  Ensure glide.ui.text\_search.enable\_archive\_fallback\_number\_search is set to the base instance value \(true\).
4.  Search for a task or problem number in the global search box.

 Expected behavior: The result should come back quickly.

 Actual behavior: There could be a long delay when the record has been offloaded due to point lookup with columnar/offloaded tables.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2059007

</td><td>

Prevent Data Management jobs from operating on columnar archive tables

</td><td>

In both scenarios, the DM Delete Job is attempting to run, but it's too slow

</td><td>

Scenario 1:

 1.  Create a Data Management Delete Job targeting a columnar archive table.
2.  Execute the job.

 Expected behavior: The DM Delete Job should not run on columnar archive tables, it should be skipped.

 Actual behavior: The DM Delete Job is attempting to run and it's too slow.

 Scenario 2:

 1.  Create a Data Management Update Job targeting a columnar archive table.
2.  Execute the job.

 Expected behavior: The DM Update Job should not run on columnar archive tables, it should be skipped.

 Actual behavior: The DM Update Job is attempting to run and it's too slow.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2059138

</td><td>

Increase columnar table migration thesholds

</td><td>

 

</td><td>

1.  Set up an Australia instance with Live Archive.
2.  Let the migration start and monitor the archive tables being migrated to columnar.

 Expected behavior: Only large archive tables \(&gt;10 GB\) should migrate, reducing the amount of columnar queries in the future.

 Actual behavior: Tables as small as 100 MB are being migratedl, which leads to a lot of columnar queries with minimal space benefits.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2061236

</td><td>

Leverage local tables to locate archive records in Global Search

</td><td>

 

</td><td>

1.  Install the Live Archive on an instance.
2.  Offload a large amount of data, including some task or problem tables.
3.  Search for a task or problem number which has been offloaded in the global search box.

 Expected behavior: The result should come back.

 Actual behavior: The result doesn't come back.

</td></tr><tr><td>

Database Persistence - Graph

 PRB2017435

</td><td>

The cypher graph query generates an invalid SQL JOIN ordering when the 'Before Query' rule injects dot-walk conditions on extended tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2051763

</td><td>

The C2R error occurs for all the WDF queries

</td><td>

 

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

 PRB2064975

</td><td>

The sub graph time increased ~200ms

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1962784

</td><td>

Property glide.db.alter\_large\_table\_threshold can't be set large enough

</td><td>

When creating a table with greater than 2,147,483,647 rows, if glide.db.alter\_large\_table\_threshold is set to 4B, it will not upgrade. The following error occurs on the upgrade: 2025-11-08 12:48:19 \(829\) worker.1 worker.1 txid=730511129301 DictionaryXMLParser \*\*\* WARNING \*\*\* Skipping table: cmdb\_rel\_ci \(too large to alter\).

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB2052093

</td><td>

There's a three-way deadlock between Preferences, TableDescriptor, and TableRotationExtension, which causes node restarts in production

</td><td>

Preferences.get\(\) holds the Preferences.class monitor across a database query and table descriptor lookup, while the AMB cluster synchronizer thread holds a TableRotationExtension instance monitor across a field normalization engine call. The two lock-acquisition orders are inverted, producing a classic AB-BA deadlock that starves any thread attempting to call Preferences.get\(\) until one of the two owners is killed by the deadlock sweeper.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB2075293

 [KB3150595](https://hi.service-now.com/kb_view.do?sysparm_article=KB3150595)

</td><td>

After the upgrade to Australia Patch 5, auto-increment columns are failing inserts with the duplicate\_key error

</td><td>

Australia Patch 5 \(AP5\) introduced a change to how certain database auto-increment sequences are managed. Under specific conditions, this change can cause the sequence used to generate new record identifiers to become invalid or out of sync with the database. When this occurs, attempts to create new records may fail. As a result, transient state records may not be created as expected in tables with the auto-increment field. This impacts many functional areas relying on the sequence record to track orders of states, logs or messages. This defect fix is included in the weekly patch due to its severe impact on multiple major functionalities across the platform.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2038995

</td><td>

Unable able to join the DF table with the native UUID to other tables that use string and native UUID as a reference key

</td><td>

This problem address the two failing reference scenarios for 'DF table with native UUID PK &gt; DF table with varchar\(32\) UUID PK' and 'DF table with native UUID &gt; Glide table with native UUID'.

</td><td>

Scenario 1:

 1.  On a instance with postgres as primary db, create a glide table.
2.  Add a column with the the type 'UUID'.
3.  Add the attribute df\_reference=true for the column to be used as reference key.
4.  Create multiple records for the table.
5.  Generate UUID values on the column.
6.  Open an external database that has UUID as a native datatype, such as postgres.
7.  Create a table that has the type 'UUID'.
8.  Add UUID values created in the glide table to here.

Notice that in the WDF hub map, the remote table is defined in the external database. The UUID column is marked as a reference to the glide table with the UUID column as primary key.

9.  Open the list view as an admin user.

 Expected behavior: The reference column should have links available for the user to access the records of the reference table.

 Actual behavior: The links to the glide table are not available.

 Scenario 2:

 1.  Create two tables in a remote postgres database.

Notice that the first table \(the reference table\) should have a column with varchar\(32\).

2.  Generates UUID values without the hyphens.

Notice that the second table \(the driving table\) should have a column with type 'UUID'.

3.  Copy the same values from the previous table with hyphens.
4.  In the WDF hub create the reference table and assign the varchar uuid column as primary key.
5.  Create the driving table and have the native uuid column as type reference.
6.  Open the driving table's list view.

 Expected behavior: The list view should load and references should work with no issues

 Actual behavior: The list view fails to load and fails in trino with the error 'Cannot apply operator: uuid = varchar\(32\)'.

</td></tr><tr><td>

Database Persistence - WDF

 PRB2040034

</td><td>

In Australia, all database columns that start with a number have 'yy\_' added to the start of the name, causing a syntax error

</td><td>

When querying a table in the Australia release and the DB column starts with a number, it adds a 'yy\_' to the SQL query. This break the collection of data and making a list view show nothing. Error: 'Syntax Error or Access Rule Violation detected by database \(ERROR: column x\_snc\_potatofarm\_0\_farmers0.yy\_1stname does not exist. Hint: Perhaps you meant to reference the column 'x\_snc\_potatofarm\_0\_farmers0.1stname'. Position: 259\)'.

</td><td>

1.  Create a scoped app.
2.  Create a table.
3.  Create some data on that table.
4.  Add a column that name starts with a number.
5.  Navigate back to the list view.

 See that its blank, but the count displays that there's records.

</td></tr><tr><td>

Database Persistence - WDF

 PRB2076449

</td><td>

A node can't start if there's a 'Formula' field on sys\_user

</td><td>

The instance node will fail to restart if there is a formula‑calculated field on the User \[sys\_user\] table. When the issue occurs, the node does not restart and logs a stack overflow error. The failure occurs during the platform's schema loading phase, preventing the instance from coming online and impacting all users.

</td><td>

1.  Create a custom field on the sys\_user table with similar customized configuration:
    -   Name: u\_test\_field
    -   Type: String
    -   Max length: 40 Select Advanced View
2.  In the 'Related lists' tab under 'Calculated Value', set the following:
    -   Calculated: true
    -   Calculation Type: Formula
    -   Formula: if\(name&gt;'''', ''Not empty'',''Empty''\)
3.  Select Submit.
4.  Restart the node.

 Expected behavior: The node restarts without issue.

 Actual behavior: The node is not able to restart and throws a stack overflow error.

</td></tr><tr><td>

Database Persistence - WDF

 PRB2080099

</td><td>

LeadingDigitLegacyColumnIT fails on Australia

</td><td>

On an Australia patch, running against Oracle, any column rename involving a column whose logical name begins with a digit fails with: 'ORA-00957: duplicate column name'. This is because the generated statement collapses the source and target names into the same identifier.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB2051005

</td><td>

Disable catalog caching as the default for ZCC

</td><td>

This data gets cached to the sys\_dcg\_ext\_meta table.

</td><td>

Create a new connection in the ZCC hub and view tables.

 Expected behavior: There should be no data in the sys\_dcg\_ext\_meta table since catalog caching should not be on by default.

 Actual behavior: There is data.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB2073262

</td><td>

Implement Personal Authentication support for Zero Copy Connectors \(ZCC\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Management Console

 PRB1996837

</td><td>

The Data Management Console does not account for partitions while calculating table size when a table is partitioned

</td><td>

When sys\_attachment\_doc is partitioned, the Data Management Console for attachments reports only the size of the parent table, not the sum of all partitions. This causes the displayed table size to appear significantly smaller than the actual disk usage.

</td><td>

1.  Open a MariaDB Instance.
2.  Migrate it to Raptor with partitioning the sys\_attachment\_doc table.
3.  After the migration check the attachment table on the instance.

 Notice that the report for attachments only reports the size of the parent table, and not the entire sum of all partitions.

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

 PRB2063909

</td><td>

Auto-install applications are based on a user license once the instance is provisioned

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2072955

</td><td>

Bring Your Own \(BYO\) PII Anonymization Service Integration \(for ServiceNow Otto\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Product Backend Services

 PRB2054113

</td><td>

Add the Java plugin for semantic search and clustering of texts

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Product Backend Services

 PRB2064387

</td><td>

Implement sys\_data\_product and sys\_data\_product\_content writes as a native Java scriptable API instead of a self-HTTP REST bridge

</td><td>

Both 'sys\_data\_product' and sys\_data\_product\_content' are global tables owned by the com.glide.dataproduct Java plugin, not by sn\_data\_product. The platform's cross-scope GlideRecord write wall blocks direct writes to these tables from our scope.

</td><td>

In the sn\_data\_product scope, attempt to write to sys\_data\_product or sys\_data\_product\_content via direct GlideRecordSecure insert/update.

 Observe the platform refuses the write with the message, 'Security restricted: Create operation against 'sys\_data\_product' from scope 'sn\_data\_product' has been refused due to the table's cross-scope access policy.'

</td></tr><tr><td>

Dependency Views

 PRB1882781

</td><td>

The relationship between nodes always shows up as 'Depends on::Used by' even though the relationship in cmdb\_rel\_ci is different for Dependency View

</td><td>

The relationship between nodes is not defined as it is in cmdb\_rel\_ci.

</td><td>

1.  Open the ngbsm\_script table.
2.  Create a new record with the script.
3.  Navigate to **Dependency Views** &gt; **View Map**.
4.  Search for 'Blackberry'.
5.  On the filter panel, select the entry created in step 1 from the 'Dependency Type' dropdown list.

 Notice the loaded map, and that all the relationships show as 'Depends on::Used by' instead of the actual relationship between the nodes as defined in cmdb\_rel\_ci.

</td></tr><tr><td>

Dev-API Authentication

 Dev-API Authentication

</td><td>

Ability to issue a correlation token that can be exchanged for access token

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Developer Sandboxes

 PRB2028151

 [KB3122033](https://hi.service-now.com/kb_view.do?sysparm_article=KB3122033)

</td><td>

Nodes are failing to upgrade during self-scheduled upgrades

</td><td>

After an upgrade, not all app nodes that were previously hosting a sandbox are upgraded. The nodes aren't in an error state and look okay. In Upgrade Monitor, users see that the node is actually not upgraded. This can happen on any upgrade and only impacts nodes that are hosting a sandbox. It can be seen in the logs that the upgrade process is checking the version of the instance and ignoring without updating the node. It's leaving a few of the nodes to fail to get upgrade. However, the change does not reflect that and it says it was successful.

</td><td>

Refer to the listed KB article for details.

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
4.  Pull stats.do?include=otel.scheduler\* on the sandbox's node.

Observe that claim\_lock\_time averages above one second \(expected ~13ms\), jobs\_lateness averaging 300+ seconds, and worker capacity used is very low.

5.  Compare against a controller node on the same instance.

 Observe that claim\_lock\_time is still elevated but jobs\_lateness stays within a few seconds, because base nodes don't pin an entire platform triggers on one node.

</td></tr><tr><td>

DevOps Change Velocity

 PRB2052626

</td><td>

GetRefRecord scoping bypass for the 6.2.1 release

</td><td>

 

</td><td>

 

</td></tr><tr><td>

DirectSQL

 PRB2031660

</td><td>

There's missing DBView support for Data Interfaces and DirectSQL

</td><td>

The initial code was done in a branch that didn't have the dbview baseline code. This finishes it in dataaccess, which now has both needed components dbviews in directsql and data interface.

</td><td>

 

</td></tr><tr><td>

DirectSQL

 PRB2073934

</td><td>

Support data interfaces with function fields in Direct SQL

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB2009621

</td><td>

Sub account \(LP\) deletion strategy is retiring logical datacenter CIs

</td><td>

The deletion strategy 'Mark as Retired' on the 'cmdb\_ci\_cloud\_service\_account' table for the pattern 'Azure - Sub Account \(LP\)' is updating the cmdb\_ci\_azure\_datacenter records to the 'Retired' status. This update on the cmdb\_ci\_logical\_datacenter record is triggering the business rule 'Cascade Update LDCs Resource State' which is updating the child resources contained in this datacenter to the 'Retired' status.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB2056121

</td><td>

There are incorrect or missing SNMP OID classifications, which result in SAN / fibre switches being classified as 'IP Switch'

</td><td>

Incorrect/ missing SNMP OID Classifications which result SAN / Fibre switches classified as IP Switch

</td><td>

Discover SAN / Fibre switches.

 Observe that these are classified as 'IP switch'.

</td></tr><tr><td>

Discovery

 PRB2058910

 [KB3156347](https://hi.service-now.com/kb_view.do?sysparm_article=KB3156347)

</td><td>

Typo in the script in Sensor SNMP

</td><td>

Classify 'his' instead of 'this.'

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB2059465

</td><td>

Discovery patterns fail to launch for sub-accounts/datacenters when glide.discovery.retire\_stale\_accounts is turned on

</td><td>

In Cloud Discovery, schedules configured to discover all sub-accounts under a main account, with enabling glide.discovery.retire\_stale\_accounts and glide.discovery.cdu.auto\_refresh\_sub\_accounts\_and\_ldcs , Discovery patterns fail to launch for sub-accounts/datacenters \(only the service account discovery launches\).

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB2073306

</td><td>

DocIntel glide support

</td><td>

This is a product update.

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

 PRB2038307

</td><td>

The smart document skill doesn't invoke the agent and doesn't render anything on Now Assist Panel

</td><td>

The **Ask Now Assist** smart document button doesn't work as expected. When the user selects the button, it opens the NAP, but it just shows the topics and doesn't load the summarization of the document.

</td><td>

1.  Navigate to **Contract Workspace** &gt; **Default List** &gt; **List** &gt; **Contract Requests** &gt; **All**.
2.  Open any contract request.
3.  Select the 'Contract Documents' tab.
4.  Select **Preview Document**.
5.  Select a document to preview, which opens it in a new tab.
6.  Select the **Ask Now Assist** button, which opens the NAP.

 Observe that the NAP loads for some time and then shows topics. Selecting the button again just loads the topics.

</td></tr><tr><td>

Document Viewer

 PRB2056915

</td><td>

Support in document viewer for the doc to voice agent

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Edge Encryption

 PRB1998926

</td><td>

The Edge command-line installation doesn't work on java 21

</td><td>

 

</td><td>

1.  Ensure java 21 is running.
2.  Download the command-line install artifact.
3.  Run the command line install artifact to install edge proxy.

 Expected behavior: Edge proxy installs successfully.

 Actual behavior: An error occurs indicating java 17 is required.

</td></tr><tr><td>

Edge Encryption

 PRB2051049

</td><td>

The edge decryption job doesn't decrypt audit records when an FE encryption configuration is active

</td><td>

During edge-to-cle migration, the user needs to run an edge decryption job while the CLE EFC is active. However, because it does not currently audit CLE fields, the check to see if the column is audited returns false. If the user has edge encrypted audit data, the migration \(decryption\) job will not migrate the audit data.

</td><td>

1.  Inactivate the edge configuration.
2.  Configure the field with an active EFC so that it will be field encrypted.
3.  Schedule the edge decryption job, ensuring that historical data will be processed.
4.  Run the job.

 Expected behavior: The execution records \(sys\_encryption\_job\_execution\) are created for the audit table's new/old value fields.

 Actual behavior: No execution records are created for audit table fields.

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

Employee Taxonomy Framework

 PRB2073966

</td><td>

Implement extension point for IKBViewAs in glide-taxnomy

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Encryption

 PRB1982641

 [KB2977274](https://hi.service-now.com/kb_view.do?sysparm_article=KB2977274)

</td><td>

Scan checks are missing null checks, causing the instance scan to fail

</td><td>

After running the 'Insecure GlideRecord Calls', if the getFunctionCallParamters\(\) function brings back an empty object, the instance scan fails.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Error Framework

 PRB2035967

</td><td>

The **Reset** button doesn't work and the 'Refined Codes' section displays error codes with error\_count=0

</td><td>

The **Reset** button on the error card list component doesn't work. When the user selects the button, the filters should be reset and the same errors should be displayed. Instead, 'No actions needed' appears and no error cards are visible. Additionally, in the Discovery Admin Workspace, the 'Refined Codes' section displays error codes that have an error\_count of 0. These zero-occurrence entries represent errors that have been fully ignored \(captured in error\_ignored\_count only\) and carry no actionable significance for the user. Showing these entries pollutes the list with noise, making it harder for users to focus on error codes that actually require attention.

</td><td>

Scenario1:

 1.  Provision an instance with:
    -   The 'Error Framework' plugin \(com.glide.error\_framework\) installed.
    -   At least one source application registered in sys\_error\_appl.
    -   Errors ingested and aggregation run \(so sys\_error\_code\_stats has records with error\_count &gt; 0\).
2.  Add the error card list component to a new workspace on the 'Error Stats' page.
3.  Verify that errors are displayed.
4.  Apply a filter to enable the **Reset** button.
5.  Select the **Reset** button.

 Expected behavior: The filters are reset to defaults. The same errors are displayed.

 Actual behavior: 'No actions needed' appears. An empty state is shown, and no error cards are visible.

 Scenario 2:

 1.  Navigate to **Discovery Admin Workspace** &gt; **Diagnostics** &gt; **Errors**.
2.  Check the Refined Codes list.

 Expected behavior: Only refined codes with error\_count &gt; 0 are displayed in the Refined Codes list.

 Actual behavior: Refined codes with error\_count = 0 are displayed in the list.

</td></tr><tr><td>

Error Framework

 PRB2058704

</td><td>

Allow apps to define key labels for UI Builder components \(configurable fieldLabels/columnList/sort-by\)

</td><td>

Consuming applications should be able to define UI Builder component field labels as domain-specific terms rather than generic ones. For example, if a component has a 'key' or 'source' field, a user should be able to define the field label as 'IP Address' or 'Discovery Schedule' for clarity in their implementation. Additionally, column reordering should be allowed, and so should the action for dropdown list subsections and ordering.

</td><td>

 

</td></tr><tr><td>

Error Framework

 PRB2069719

</td><td>

Separate the 'Error' and 'Context' actions in EF UI Builder \(UIB\) components

</td><td>

The EF UIB error detail panel had a single combined 'Actions' dropdown list for both error-level and context-level actions. This splits them into two distinct split-buttons aligned with the redesign: 'Mark error as ' in the properties pane for error actions, and 'Actions' in the agent context pane for context actions. App teams can configure and order actions independently for each section.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB2053994

</td><td>

There's a null pointer exception in AlertWorkNotesHandler .updateWorkNotesAnd SilentSaveOfClosedAlert

</td><td>

The race condition causes the Null Pointer Exception in AlertWorkNotesHandler.updateWorkNotesAndSilentSaveOfClosedAlert.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB2060447

</td><td>

Intermittent JDBC error 'The column index is out of range' is caused by concurrent reuse of the shared QueryCondition instance

</td><td>

This issue occurred because of the race condition.

</td><td>

 

</td></tr><tr><td>

External Content Connectors Glide

 PRB2068960

</td><td>

'Item\_label\_rid' field is dropped for ais\_high\_security\_admin users in SearchExternalContentQueryApi

</td><td>

The field is absent from the response. If 'item\_label\_rid' is the only field requested, the response is empty entirely. The query to AIS is skipped because no fields survive the allow list intersection.

</td><td>

1.  Log in as a user with the ais\_high\_security\_admin role.
2.  Call SearchExternalContentQueryApi.search\(\) against an external content table, requesting the field **item\_label\_rid**.

 Observe that the field is absent from the response. If **item\_label\_rid** is the only field requested, the response is empty entirely. The query to AIS is skipped because no fields survive the allow list intersection.

</td></tr><tr><td>

External Content Connectors Glide

 PRB2073292

</td><td>

Execute the Direct AI Search query and display the raw result

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

External Content Connectors Glide

 PRB2073293

</td><td>

Extend scriptable API work to non-maintenance users

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

External Content Connectors Glide

 PRB2073294

</td><td>

The filtered list of XCC are linked to a specific search profile, such as Janus

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

 Notice that once the WOTs are moved to the 'Qualified \(Pending Dispatch\)' state, the tasks should be bundled using Dynamic Bundling and Dynamic Schedule the tasks automatically.

</td></tr><tr><td>

Flow Engine

 PRB2055858

</td><td>

Add flow benchmarking tests to Australia code base to monitor flow engine performance improvements

</td><td>

The user is unable to run standardized micro benchmarks in Australia.

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

Flow Engine

 PRB2073167

</td><td>

Add new metric for flow runtime complexity called from non-mcp

</td><td>

The system currently tracks metrics for flow runtime complexity. There is a need to add a new metric specifically for flows called from non-mcp.

</td><td>

1.  Trigger a flow execution via a non-MCP channel \(Browser/UI, Integration channel, Mobile, or any execution path that is not MCP\).

Observe that flow runtime complexity metrics are not being recorded with the granularity/buckets defined for non-MCP execution.

2.  Compare against expected bucket definitions: Bucket 1 \(1-2\) through Bucket 24 \(1000+\).

 Expected behavior: For all non-MCP execution paths \(Browser/UI, Integration channels, Mobile, and any non-MCP path\), flow runtime complexity metrics are recorded using the new, more granular bucket set, without affecting existing metrics.

 Actual behavior: No dedicated metric/bucket set exists for non-MCP execution paths.

</td></tr><tr><td>

Flow Engine

 PRB2073745

 [KB3154012](https://hi.service-now.com/kb_view.do?sysparm_article=KB3154012)

</td><td>

Revert the change to sys-property so users can enable full reporting for flow executions in production

</td><td>

Users see a yellow message stating that action details have been removed according to the report retention policy, and cannot view the detailed flow execution information in production instances. This occurs after the platform change that forces the system property com.snc.process\_flow.reporting.level to 'BASIC' on production, automatically reverting any attempt to set it to 'FULL'. As a result, new records in sys\_flow\_context ;are stored at the 'BASIC' level, limiting visibility of inputs, outputs, and step-by-step details.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2067258

</td><td>

Feature filtering fixes for new the Flow Designer

</td><td>

Read only/stop editing and Undo/Redo is supported.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2074948

</td><td>

APIs for skills and agents are missing from Australia and are needed for the lit rework

</td><td>

Two API's were made, one for skills and one for agents, they return an error message when the tables for those items don't exist.

</td><td>

1.  Verify the availability of APIs for skills and agents.
2.  Confirm the correctness of the APIs for skills and agents.
3.  Select a skill name.
4.  Check if the **Workflow**, **Product**, and **Feature** fields are auto-populated in the 'Execute skill' actions.
5.  Verify that each skill and agent has a description available.

 Observe that the APIs for skills and agents are available and functioning correctly.

</td></tr><tr><td>

Hermes \(Family\)

 PRB2051477

 [KB3152907](https://hi.service-now.com/kb_view.do?sysparm_article=KB3152907)

</td><td>

The Hermes topic inspector falsely displays the 'unreadable messages' pop up

</td><td>

A modal alert was introduced in the Hermes Topic Inspector to handle unreadable messages – conditions such as unsupported compression types that cause a page crash. An issue has been identified where this modal triggers incorrectly due to the improper evaluation of the unreadable\_messages flag, preventing users from inspecting topics even when no unreadable messages are present. As a result, users are unable to inspect Hermes topics despite no actionable error condition existing, resulting in unnecessary disruption to monitoring and troubleshooting workflows.

</td><td>

1.  Open the Topic Inspector.
2.  View a topic with a large amount of messages.
3.  Set the timestamp to the maximum, such as 2 days prior to the current time.

 Observe that the 'unreadable messages' popup appears.

</td></tr><tr><td>

Hermes \(Family\)

 PRB2057996

</td><td>

Setting 'hermes.kafka.disabled' to 'true' does not help to disable Hermes jobs such as 'Hermes Failover State Refresh Job'

</td><td>

This issue causes huge loads of logs.

</td><td>

 

</td></tr><tr><td>

Horizon iFrame Component

 PRB2074065

</td><td>

Users get an error when trying to access the iFrame related configurations

</td><td>

Users get the following error: 'Uncaught TypeError: Cannot read properties of null \(reading 'parent'\) at Object.

</td><td>

 

</td></tr><tr><td>

HR e-signature

 PRB2035247

</td><td>

RCA for Content Experience

</td><td>

Specifically, EEsign for getRefRecord directive.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1970902

</td><td>

'Mark When Complete' is hardcoded in the Agent Workspace for HR Case Management for i18n

</td><td>

 

</td><td>

1.  Set up a testing environment.
2.  Install the French language pack \(com.snc.i18n.french\).
3.  Install sn\_hr\_agent\_ws with demo data.
4.  Install sn\_jny with demo data.
5.  Install com.sn\_hr\_lifecycle\_events with demo data.
6.  Enable 'Playbook' in sn\_hr\_le\_case records in the HR Agent Workspace.
7.  Create a sn\_hr\_le\_case record.
8.  Navigate through the playbook until the user sees the 'Dispatch the Onboarding Swag' lane.

 Observe the string 'Mark When Complete' is hardcoded.

</td></tr><tr><td>

HR Service Delivery

 PRB2018687

</td><td>

The 'Edit' button does not work for the Granular Delegation rule

</td><td>

The record edits are not reflected even though the Granular Delegation rule was created.

</td><td>

1.  Install the Granular Delegation Plugin.
2.  Create a Granular Delegation Rule.
3.  Save it.
4.  Use the **Edit** button to modify the user criteria to the delegate/delegator.

 Notice that after the edit, the record doesn't reflect the changes.

</td></tr><tr><td>

HR Service Delivery

 PRB2057715

</td><td>

ZTSD dare RCAs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2059123

</td><td>

RCAs in the 'Requested' state for HR case assistant and HR Case Creation agent

</td><td>

 

</td><td>

1.  Open an instance.
2.  Ensure there is no RCA for Source as 'Tool: Add comment to HR case'.
3.  Call the Unified Orchestrator.
4.  Ask the voice agent to look up an HR case.

Notice that the agent asks for soft pin. After providing soft pin, the agent confirms that user is authenticated.

5.  Provide the number for HR case opened.

 Notice that when asked to add comments to case, there is an RCA. Another RCA is generated in the 'Requested' state the when user asks for case creation.

</td></tr><tr><td>

HR Service Delivery

 PRB2063926

</td><td>

Semantic index changes for HR Service and HR Case for predicting the HR Service

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2067282

</td><td>

GlideHTMLSanitizer is not callable from HR scoped applications

</td><td>

 

</td><td>

1.  From any scoped application \(for example, sn\_hrbp\_hub\), run it in a background script.

Observe it fails because 'GlideHTMLSanitizer' is not defined.

2.  Retry it with global.GlideHTMLSanitizer.sanitize\(...\).

Observe it also fails with SNC.GlideHTMLSanitizer.sanitize\(...\).

3.  Run the same call from the global scope.

 Observe that it succeeds and returns the correctly sanitized HTML.

</td></tr><tr><td>

HR Service Delivery

 PRB2071645

</td><td>

Add required RCAs for CBS AINPX in HR Scope

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

IDR - Scheduled Replication

 PRB1937502

</td><td>

The Scheduled Replication 'Percent Complete' doesn't take updated records into account \(%\)

</td><td>

The percentage from the Scheduled Replication 'Percent Complete' is inaccurate. For example, it says '66.56%' for 'Percent Complete' despite the status being 'Completed'.

</td><td>

1.  Perform a scheduled replication test with inserts and updates.
2.  Update a third of the records inserted.

 Expected behavior: Scheduled Seeding Replication Requests show the percentage 100% when complete.

 Actual behavior: Only the actual number of records sent over seems to be reflected in the percentage.

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

Indicator Management

 PRB2052998

</td><td>

When the indicator library name ='None' with no data, sometimes data displays intermittently on some columns and rows

</td><td>

The Indicator Library shows the indicators name as 'None' and shows no other data.

</td><td>

1.  Impersonate ITIL user.
2.  Navigate to **Platform Analytics** &gt; **Indicators**.

 Observe that all rows show as 'None'

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

 PRB2074591

</td><td>

Update for glide version and Clone Admin Console store app

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1994565

</td><td>

If the shared key is expired before activating the consumer set, consumer set cannot be activated

</td><td>

The message, 'Shared key corresponding to shared key id %s is not found.' is triggered when the shared key expires before activating the consumer set.

</td><td>

1.  Set idr.shared.key.expiration to 300,000 on the producer side \(5 minutes\).
2.  Create a producer replication set,.
3.  Activate it.
4.  Create a consumer replication set.
5.  Approve the subscription from the producer side.
6.  Let the shared key expire from the producer side.
7.  Attempt to activate the consumer.

 Expected behavior: There is a mechanism to detect when shared key has expired, similar to auto-shared key recovery when the consumer shared key is missing.

 Actual behavior: The producer is not able to send the CONSUMER\_ACTIVATION payload due to mismatched shared keys between the producer and consumer.

</td></tr><tr><td>

Integration Hub

 PRB2033476

</td><td>

After upgrading to Australia, password actions such as 'Change User Password' and 'Reset User Password' fail

</td><td>

The password actions 'Change User Password' and 'Reset User Password' are failing from Microsoft Active Directory v2 Spoke.

</td><td>

 

</td></tr><tr><td>

Internationalization Features

 PRB2027846

</td><td>

Changing the country in the user preferences doesn't check the user's permission

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Create an ACL removing write access to sys\_user.country for users without the 'admin' role.
3.  Impersonate a user without the admin role.
4.  Open the 'User Preference panel'.
5.  Change the country preference.
6.  Stop the impersonation.

 Observe whether the value for sys\_user.country was changed for the user.

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB2058369

 [KB3140571](https://hi.service-now.com/kb_view.do?sysparm_article=KB3140571)

</td><td>

Midserver is unable to fetch credentials after upgrading to Zurich or Australia

</td><td>

In certain versions, there's a Unified Secrets Gateway \(USG\) service for credential management. During the upgrade to those versions, a system trigger script is designed to automatically execute and populate the sys\_secret\_identity\_group\_member table with the MID Server identity group mappings required for USG authentication. However, this trigger fails to complete successfully, leaving the table incompletely populated. As a result, the MID Server can't authenticate with USG and fails to retrieve credentials.

</td><td>

1.  Upgrade an instance from a version where USG doesn't exist to a Zurich or Australia version where USG exists.
2.  Check if sys\_secrets\_identity\_group\_member is populated with all entries from ecc\_agent.

 Expected behavior: All entries from ecc\_agent are present in sys\_secret\_identity\_group\_member.

 Actual behavior: There are no entries in sys\_secret\_identity\_group\_member.

</td></tr><tr><td>

Knowledge Graph \(Family\)

 PRB2063201

</td><td>

Add support for dynamic table lists in the KG Affinity API for affinity data loading

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1975454

 [KB3151964](https://hi.service-now.com/kb_view.do?sysparm_article=KB3151964)

</td><td>

The 'View article' link in Manager Hub is not working as expected for employee users

</td><td>

After selecting the article as an employee from the results, the article is empty because it the fields from the template article are not rendering.

</td><td>

1.  Install the com.sn\_ex\_employee\_center\_pro plugin.
2.  Set the property 'glide.knowman.enable\_view\_as\_user' to 'true'.
3.  Create a manager user.
4.  Add the 'knowledge\_view\_as' role to the manager user.
5.  Create an employee user.
6.  Add the 'knowledge' role to the employee user.
7.  Link the manager user as a manager to the employee user.
8.  Create a new knowledge base.
9.  Add the 'user with knowledge role' user criteria to both 'canRead' and 'canContribute'.
10. Create a new template article \(template article, kb\_template\_what\_is etc\) under that new KB.
11. Link that article to any topic from the 'Connected content' related list.
12. Create a password for the manager.
13. Log in with the userid and password.
14. Open /esc?id=ec\_view\_as\_results.
15. Select the employee user.
16. Search for that newly created article.
17. Open the article from the results.

 Notice that the article content is empty, as it is not rendering any fields of the template article.

</td></tr><tr><td>

Knowledge Management

 PRB1989283

</td><td>

m2m\_kb\_to\_ block\_history\_list displays the state of article as 'outdated' instead of 'published'

</td><td>

The state should be 'Published' and not 'Outdated'.

</td><td>

1.  Create an article which has a block in it.
2.  Checkout the article, create a new version and publish the article.
3.  Check the state of the latest article.

 Notice that it says 'Outdated' instead of published in m2m\_kb\_to\_block\_history\_list.

</td></tr><tr><td>

Knowledge Management

 PRB2000452

</td><td>

The 'Edit' button isn't visible in any of the previous versions of the articles in workspaces

</td><td>

After upgrading Zurich, the **Edit** button does not appear when users open an outdated Knowledge article in the kb\_view page of any workspace. The article is displayed in read-only mode and authors, KB owners, or admins cannot switch to the full record view to make changes. This prevents necessary updates to legacy articles.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2034151

</td><td>

Back link on Portal \(Widget: HRM Back Button\) doesn't work in certain situations

</td><td>

Irregular execution of events triggered while typing search inputs.

</td><td>

1.  Apply the update set.
2.  Navigate to **Knowledge search**.
3.  Type a name in the client search.

Notice that the results are displayed.

4.  Clear the results.
5.  Wait 1 second.
6.  Type in another result.

</td></tr><tr><td>

Knowledge Management

 PRB2037824

</td><td>

The pop-up to select relevant tasks doesn't appear after selecting 'Yes, draft with Now Assist' from the knowledge base

</td><td>

When creating a new article from a knowledge base, the base instance Now Assist Skill 'Generate Knowledge Article' / 'KB generation' doesn't show the pop-up to select incidents.

</td><td>

1.  Make all article templates inactive.
2.  2. Navigate to **Knowledge** &gt; **Administration** &gt; **Knowledge Bases**.
3.  Open any knowledge base record from the list view.
4.  Scroll down to the 'Knowledge' related list.
5.  Select **New** from the related list to create a new knowledge article.

Observe that it redirects to the knowledge article form. A pop-up appears, asking if the user would like to use AI to draft the article.

6.  Select **Yes, draft with Now Assist**.

If any language plugin is available, observe that a pop-up appears with the title 'Select options - language options are configured in Now Assist admin'. Otherwise, it shows 'Draft with Now Assist momentarily'.

7.  Select **Continue**.

 Observe that it returns the user to the form. There's no pop-up to select relevant tasks, and no article is drafted.

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

Knowledge Management

 PRB2061644

</td><td>

Support KB creation through the import feature processAttachment\(\) API

</td><td>

It returns JSONObject and causes the error, 'Error: Evaluator.evaluateString\(\) problem: java.lang.SecurityException: Method returned an object of type JSONObject which is not allowed in scope sn\_ia\_config. JSONObject parsing is not possible in scoped app.'

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2073317

</td><td>

Create a new article type in the UI16 flow

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2073319

</td><td>

Upgrading NAKM, KC, KCInWorkspaces and ECE to Brazil

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2076447

</td><td>

The Auto-fix plugin update blocks the Australia Patch 5m upgrade in loadsim release testing

</td><td>

The plugin upgrade thread handling becomes stuck in an error loop triggered by a null pointer. It never exits or advances, leaving the upgrade 'hung'. This happens when the upgrade plugin loader reaches the knowledge center update that adds in the auto-fix and auto-fix enable property.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2077445

</td><td>

Updating versions for the base instance Knowledge Management apps to include Australia and Brazil fixes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2083241

</td><td>

True up for Australia and Brazil

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB2013721

</td><td>

The **Resume Case** UI Action doesn't work as expected for certain users

</td><td>

When a user with the admin role accesses an HR case but is restricted by a COE Security Policy, the **Resume Case** UI action does not restore the activity set to the 'Running' state. Instead, the activity remains in the awaiting\_trigger state, preventing the case workflow from continuing.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2024845

</td><td>

The ListHighlighted ValueService cache key is missing highlightedValueConfigId, and causes cache collisions between requests with different configuration IDs

</td><td>

The highlighted values in the Workspace list render intermittently. It works right after cache.do then stop after a few minutes, because ListHighlightedValueService's cache key omits highlightedValueConfigId. There are multiple requests for the table, workspace, and fields but different \(or null\) configuration IDs collide on the shared static cache. As a result, whichever request populates the cache first determines the result for all subsequent requests until the entry expires.

</td><td>

1.  Create a sys\_highlighted\_value for table=incident, field=state, with a simple condition where the state is not empty, color=blue, and status=positive.
2.  Create sys\_ux\_highlighted\_value\_config 'A' with M2M-linked to the highlighted value through sys\_ux\_m2m\_highlighted\_value\_config.
3.  Create sys\_ux\_highlighted\_value\_config 'B' with no M2M link to any highlighted value.
4.  Navigate to **cache.do** to flush the caches.2. Navigate to sys.scripts.do.
5.  Run the script.

 Expected behavior: It should be 'CONFIG\_B=0, CONFIG\_A=1'.Actual: Notice that it is 'CONFIG\_B=0, CONFIG\_A=0,' and A reuses B's cached empty result.

</td></tr><tr><td>

List Administration

 PRB2033285

</td><td>

There's an Australia update issue with roles not appearing in the 'Table/workspace' view

</td><td>

Having a dictionary entry with 'Use Dependent Field' turned on and pointing to a boolean dictionary entry on the same table causes the values on the list to not display.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2036908

 [KB3097895](https://hi.service-now.com/kb_view.do?sysparm_article=KB3097895)

</td><td>

A list fails to load when a catalog variable with a reference qualifier on a large table is added as a column

</td><td>

The page times out. An error occurs reading, 'Sorry, an error occurred or this page isn't available'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB2039348

</td><td>

In the List view, the first choice is shown and is not the selected choice for the lookup select box variable in the workspace

</td><td>

Irrespective of whatever option the user might have selected, it will show the first choice in the workspace List view.

</td><td>

 

</td></tr><tr><td>

List Column Menu

 PRB2077157

</td><td>

Grouping by any field displays a '$c66360ca901b4a5387c58a30a4270909\[ListProperties.getGrandTotalRows\(\)\] total $c66360ca901b4a5387c58a30a4270909\[ListProperties.getTitle\(\)\]' on the list view

</td><td>

This issue was observed in an Australia instance.

</td><td>

1.  On an Australia instance, open sc\_cat\_item.list.
2.  On the 'Short description' column, right click on the 3 dots.
3.  Use 'Group By Short description.'

 Notice on the top banner, there is a $c66360ca901b4a5387c58a30a4270909\[ListProperties.getGrandTotalRows\(\)\] total $c66360ca901b4a5387c58a30a4270909\[ListProperties.getTitle\(\)\] getting displayed at the top.

</td></tr><tr><td>

List Controller

 PRB1989084

</td><td>

In Platform Analytics, a loading indicator appears in the mid-page of the scheduled export list after applying filters

</td><td>

In the Scheduled Export List, when applying any filter, the loading indicator is displayed in the middle of the web page rather than at the top. As a result, users must scroll down to notice that the page is loading, which can cause confusion.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1990422

</td><td>

A relative timestamp \(time ago\) in a workspace's 'List' view doesn't refresh unless the record itself is updated

</td><td>

In the Service Operations Workspace list view, the relative timestamp displayed under **datetime** fields, such as **Updated** and **Opened**\) does not refresh when the user selects the **Refresh** button, unless the underlying record has been updated. This results in a stale relative time value being continuously displayed, even though the actual absolute timestamp shown above it is correct. The issue was validated on a base instance, confirming that no customizations were involved. This behavior causes confusion for agents who rely on relative time indicators when monitoring active incident lists.

</td><td>

1.  Log in to a Zurich base instance with Service Operations Workspace enabled.
2.  Navigate to **Service Operations Workspace** &gt; **Incidents** &gt; **Open**.
3.  Identify any incident with visible **Updated** or **Opened** datetime fields.

Observe the relative timestamp directly under the **datetime** \(for example, '1m ago\).

4.  Wait several minutes without modifying the incident.
5.  Select the **Refresh** button on the Workspace list view.

Observe that the relative timestamp does not change, and it continues to show the original value \(1m ago\), even though more time has elapsed.

6.  Update the same incident record in the background by adding a comment.
7.  Return to the list.
8.  Select **Refresh** again.

 Observe that the relative timestamp updates to the correct value \(2m ago\).

</td></tr><tr><td>

List Filters

 PRB1982205

</td><td>

Data visualizations don't translate to the selected language

</td><td>

The data visualization column is displayed in English instead of Swedish. Only the left sidebar is translated into Swedish.

</td><td>

1.  Provision an instance with the French language pack \(com.snc.i18n.swedish\) installed.
2.  Open Visualization Designer in Platform Analytics Workspace.
3.  Create a new visualization.
4.  Change the session language to Swedish.

 Observe that the column is displayed in English instead of Swedish. Only the left sidebar has been translated into Swedish.

</td></tr><tr><td>

Live Archive

 PRB2022491

</td><td>

The count of records is missing before and after the columnar migration

</td><td>

The log message is missing.

</td><td>

1.  Open an Australia instance with the latest RaptorDB.
2.  Install Tier 2 Live Archive.
3.  Offload data to include attachments.
4.  Inspect the node queries.

 Expected behavior: There is a log message detailing the number of records in each table, and sys\_attachment\_doc\_columnar before and after migration.

 Actual behavior: This is missing from logs.

</td></tr><tr><td>

Live Archive

 PRB2056631

</td><td>

The two-pass sparse fetch on sys\_attachment\_doc\_columnar forces a sequential scan, and not an indexed lookup. Pass 2 filters by sys\_id even though the table is physically ordered by sys\_attachment

</td><td>

During attachment downloads, the chunk row resolution against sys\_attachment\_doc\_columnar performs a sequential scan instead of an indexed lookup. This adds latency to attachment reads that use the columnar \(RaptorDB/S3-offloaded\) attachment storage backend.

</td><td>

1.  Ensure an attachment's chunks are stored in sys\_attachment\_doc\_columnar with columnar/RaptorDB storage enabled.
2.  Download that attachment so that loadPrefix\(\)/chunk iteration resolves a sparse row on sys\_attachment\_doc\_columnar.
3.  Capture DB query stats/timing for the resulting 'WHERE sys\_id = ?' pass-2 query.

 Expected behavior: The pass-2 row fetch performs comparably to the same fetch against sys\_attachment\_doc \(indexed lookup\).

 Actual behavior: The pass-2 fetch against sys\_attachment\_doc\_columnar performs a sequential scan because sys\_id is not the table's primary\_ordering column, causing measurable added latency, especially as the table/segment grows.

</td></tr><tr><td>

Live Connect \(Server\)

 PRB2038719

</td><td>

Update all server side 'SQL API' references to 'Live Connect'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Live Connect \(Server\)

 PRB2062273

</td><td>

Allow user accounts to access Live Connect

</td><td>

Only service accounts were allowed to use Live Connect.

</td><td>

 

</td></tr><tr><td>

Microsoft Reconciliation

 PRB1980380

</td><td>

An incorrect 'Bring your own license' \(BYOL\) unlicensed reason is provided when the setup does not have any relation to BYOL

</td><td>

 

</td><td>

1.  Create CIS Suite with different components, with the entitlement per processor.
2.  Create installs without any **Cloud** fields.
3.  Notice that there should not be any BYOL tags in the key value table.
4.  Run recon.

 Notice that the unlicensed reason is 'BYOL Not Supported for Per Processor Licensing on This Installation.'

</td></tr><tr><td>

Microsoft Reconciliation

 PRB2039492

</td><td>

Resource value for bug bash observations

</td><td>

The PO line needs license metric changes on UI 16 same as alm\_license. The description is missing for volume based LM configurations, and the license metric tier related list should not have a license metric configuration column.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2063491

</td><td>

'LinkedHashMap$Entry' objects connected to the LRU take a couple MB

</td><td>

These objects are from 'ecc\_queue\_authorization\_policy'.

</td><td>

1.  Open a local instance.
2.  Connect to the MID Server.
3.  Create a heap dump.

 Notice that entries of 'LinkedHashMap$Entry' for ecc\_queue\_authorization\_policy have over 3MB for each entry.

</td></tr><tr><td>

MID Server

 PRB2067544

</td><td>

ScopedProcessFlowScriptSource.getSourceName\(\) returns display label 'Process Automation' instead of a valid table name, causing the invalid ScriptRecordDescriptor on the transaction

</td><td>

 

</td><td>

1.  Navigate to **Process Automation** &gt; **Flow Designer**.
2.  Create a new Action \(for example, 'Test Process Automation Table Name'\).
3.  Add a script step.
4.  Save and publish the action.
5.  Select **Test**.
6.  Navigate to ecc\_queue\_authorization\_policy.list.

 Expected behavior: The policy record has a valid initiator\_table \(sys\_hub\_step\_instance\) and the populated initiator sys\_id.

 Actual behavior: The policy record has initiator\_table = 'Process Automation' \(which is invalid and not a real table\), initiator = empty and scope = NA.

</td></tr><tr><td>

Mobile Platform

 PRB2021795

</td><td>

The checklist string value ampersand is saved as '&amp;'

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB2033117

</td><td>

In Now Agent, the work order task questionnaire is truncated if the questionnaire is more than 100 characters

</td><td>

.

</td><td>

1.  Open the Now Agent App.
2.  Impersonate a user whose preferred language isn't English and a has work order task \(WOT\) questionnaire assigned to them.
3.  Select the **My work** option.
4.  Select the WOT.
5.  Take the questionnaire.
6.  Scroll through the queries.

 Observe that queries above 100 characters are truncated.

</td></tr><tr><td>

Multi-Instance Framework - Core

 PRB2063884

</td><td>

MIF Hermes doesn't refresh the cluster configuration when the local hermes\_cluster\_config has no primary or after a datacenter-rule change, causing stale/failed cluster resolution for remote owners

</td><td>

When instance A sends a MIF async message to instance B, it needs B's Hermes cluster details from datacenter and Kafka bootstrap servers. Instance A keeps a saved copy in the hermes\_cluster\_config table and reads it in HermesProducerClient.getClusterInfoSet. Today that method only calls B's live endpoint \(/api/now/hermes\_cluster\_info, tier-2\) when A has no saved rows for B.

</td><td>

1.  Verify that Instance A has a saved Hermes cluster rows for instance B \(service MIF-Hermes\) pointing to B's old datacenter, or a single row that isn't marked primary.
2.  Send a MIF async message from A to B.

 Expected behavior: A resolves B's current cluster details and sends to the correct datacenter.

 Actual behavior: A uses the old/incomplete saved config and sends to the wrong datacenter, or fails with 'No primary cluster found'.

</td></tr><tr><td>

Multi-Instance Framework

 PRB2040054

 [KB3146783](https://hi.service-now.com/kb_view.do?sysparm_article=KB3146783)

</td><td>

There's a flood of 'Unable to find vtable operation for operation id \{\}' messages that's generating millions of records in an instance for every Flow Designer execution

</td><td>

In a cloned instance, the root cause of the flood of errors messages 'Unable to find vtable operation for operation id \{\}' in the syslog is that sn\_mif\_vtable\_ operation\_context.vtable \_operation is empty.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Multi-Instance Framework

 PRB2066107

</td><td>

DB listener MIFVTableListener fails with IAE before/after DB actions and breaks the normal upgrade flow

</td><td>

During an upgrade, a database listener throws an IllegalArgumentException at two points in the plugin-install lifecycle - both before and after DB actions run. This prevents the normal upgrade flow from completing for a number of plugins, resulting in files not being properly installed/loaded.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2073299

</td><td>

MMS Glide update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2073300

</td><td>

Vision Agent and MMS Glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2076357

</td><td>

Update system properties default values for MMS

</td><td>

MMS is not queuing enough records. The system propertyies 'glide.platform\_mm\_service.job.batch\_size' should be set to '10' and 'glide.platform\_mm\_service.async\_http\_max\_outstanding\_requests' should be set to '20'

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1720952

</td><td>

The 'Not Found' tab on workspace

</td><td>

After opening the workspace, the user will notice a 'Not Found' tab.

</td><td>

1.  Import xmls attached.
2.  Open console.
3.  Select the **iframe**scope.
4.  Provide the script 'openFrameAPI.openCustomURL\('interaction\_list.do'\);'.

Notice that the Interaction list will open in the platform view.

5.  Open the workspace.

 Notice the 'Not Found' tab.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2034126

</td><td>

A collapsible menu \(for example, 'Self Service' or similar\) text color does not change when the user hovers over it in the navigation filter menu

</td><td>

It remains black when other entries turn white when the user hovers.

</td><td>

1.  Open a theme where the top-level collapsible menu is set to black.
2.  Navigate to the **All** menu.
3.  Hover the mouse over different menu items.

Observe that most menu items change text color from black to white on hover.

4.  Hover over 'Self Service'.

 Notice that the text remains black instead of changing to white.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2054933

</td><td>

Glide custom menu updates

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2079773

</td><td>

Set token\_exchange\_allowed to 'true' on an OffGlide AIEX oauth entity record

</td><td>

Notice that token\_exchange\_allowed is 'false' which needs to be 'true', otherwise oauth will fail for guest users.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2081424

</td><td>

Set bff\_cookie\_exchange\_allowed to 'true' on OffGlide AIEX oauth entity records

</td><td>

bff\_cookie\_exchange\_allowed is set as 'false', which need to be 'true', otherwise oauth will fail for the guest user.

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

When a topic execution is initiated, the conversation ID isn't available in certain Glide log entries' context maps This complicates troubleshooting across different trace IDs instead of a unified conversation ID. The conversation ID should be available in the cache and topic execution context map in the syslog table.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2056745

</td><td>

Guardian pre-process flow resolves getGeoRoutingDetails\(\) multiple times per request in NowLLMIntegration GuardianProvider

</td><td>

NowLLMIntegration GuardianProvider. shouldUseGatewayService\(\) and addLLMGatewayRoutingHeader\(\) each independently call through to GeoRoutingServiceImpl .getGeoRoutingDetails\(\) &gt; resolveGeoRoutingDetails\(\). ShouldUseGatewayService\(\) itself is invoked from multiple call sites across a single request's lifecycle. None of these calls are memorized, so resolveGeoRoutingDetails\(\) re-executes its full resolution logic \(potentially including the licensing entitlement API call\) on every invocation within the same request, even though the underlying geo-routing state can't change mid-request.

</td><td>

1.  Trigger a Guardian moderation request that routes through NowLLMIntegration GuardianProvider \(LLM\_GENERIC\_SMALL\_MODERATIONS model\).
2.  Trace/log calls into GeoRoutingServiceImpl .resolveGeoRoutingDetails\(\) \(or set a breakpoint\) during a single request's transformRequest\(\)/getUrl\(\) lifecycle.

 Observe that resolveGeoRoutingDetails\(\) executes repeatedly \(up to six times found via code trace\) instead of once per request. When the 0$ SKU entitlement isn't active, each of these calls re-invokes the expensive isEntitlementActive WithLicensingAPI\(\) licensing call, since resolveGeoRoutingDetails\(\) has no per-request memorization. Only the underlying getGeoRoutings\(\) /getGeoRoutingConfigs\(\) cache calls are cached via ADomainAwareCache.

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

Incident, Change, and Case summarizations are failing with errors when users select the 'Summarize' button: 'Summarization could not be completed because access to the base table Case was unsuccessful'. Error logs: 'Error sending to unified\_short\_url\_active\_1...Status 500 - \[Internal Server Error\] \[\{'success':false,'statusCode':429,'message':'Too many concurrent data insert operations in progress - additional rebuild request being ignored','timestamp':'2026-07-17T07:00:17.752637494Z','results':\{\}\}\]'.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2064726

</td><td>

The Mosaic response translation to the user's preferred language is failing

</td><td>

 

</td><td>

1.  Set the user's preferred language to a non-default language.
2.  Generate a Mosaic token for the given userId.
3.  Run the Mosaic capability.

 Expected behavior: The Mosaic response should be translated and returned in the user's preferred language.

 Actual behavior: The Mosaic response is not translated to the user's preferred language and is returned in the default language.

</td></tr><tr><td>

OneExtend

 PRB2073758

</td><td>

AutoChat off-glide implementation changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2076738

</td><td>

Update the model display names in the Gen AI model configuration table

</td><td>

 

</td><td>

1.  Update the model display names.
2.  Make the Gemini pro model as 'active=false' and the 'lifecycle' state as 'deprecated'.
3.  Make the Gemini 3 flash as the action 'delete'.

</td></tr><tr><td>

OneExtend

 PRB2078604

</td><td>

Add caching for BYO PII

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB2014301

</td><td>

In the Classic Formula indicator form, the elements list is not visible when configuring breakdowns of contributing indicators in the formula

</td><td>

A null table appears and an error is thrown without showing the elements list.

</td><td>

1.  Open WDF enabled instance.
2.  Navigate to Formula Indicators list through the 'All' menu navigation.
3.  Open any existing indicator or create a new formula indicator.
4.  Select on **Browse** for an indicator.

Notice that under the 'Formula' tab, a modal with **Indicator**, **Breakdown** and **Element** fields opens up.

5.  Select any indicator and breakdown.

 Expected behavior: The list of elements for the selected breakdown from the respective target table are shown.

 Actual behavior: When selecting the **Search** icon on the **Elements** field, the popup opens with a null table, and throws an error without showing the actual elements list.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2035261

</td><td>

Advanced Filter doesn't work as expected for certain filters in the Data Visualization dashboard in Platform Analytics

</td><td>

Advanced filters in data visualizations aren't honored for both date range \('Between'\) and keyword conditions, resulting in all the records being returned regardless of the configured filter criteria.

</td><td>

Scenario 1:

 1.  Log in to an Australia base instance.
2.  Navigate to **All** &gt; **Data Visualizations**.
3.  Open any visualization.
4.  Select the **Advanced Filter** button.
5.  Select the **Created** field.
6.  Choose the 'Between' operator.
7.  Specify a valid start date and end date.
8.  Apply the filter.

 Expected behavior: Only records with a created date within the specified date range are returned.

 Actual behavior: The visualization returns all records, ignoring the configured date range filter.

 Scenario 2:

 1.  Log in to an Australia base instance.
2.  Navigate to **All** &gt; **Data Visualizations**.
3.  Open any visualization.
4.  Select the **Advanced Filter** button.
5.  Select the **Keyword** field.
6.  Configure the condition as 'Keyword is SLA'.
7.  Apply the filter.

 Expected behavior: Only records matching the keyword value 'SLA' are returned.

 Actual behavior: The visualization returns all records instead of only the matching records, indicating that the filter condition isn't being applied correctly.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2075362

</td><td>

The domain path is empty for many reports

</td><td>

 

</td><td>

Upgrade the Zurich instance to Australia.

 Expected behavior: The domain path is populated for all reports \(sys\_report\).

 Actual behavior: The domain path is empty for many reports.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2076990

</td><td>

The AIDE **Explore** button shown on all lists, including 'All Table Discovery' entities

</td><td>

The AIDE **Explore** button is being shown on all entity lists, including entities that should not have it. Only entities marked 'Active=true' and 'population\_source=Table configuration' should display the **Explore** button. Entities with 'population\_source = All Table Discovery' \(or inactive entities\) should not show the **Explore** button.

</td><td>

Open an entity list that is marked as 'All Table Discovery'.

 Observe that the **Explore** button is present.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2079191

 [KB3152739](https://hi.service-now.com/kb_view.do?sysparm_article=KB3152739)

</td><td>

Remove sys\_script\_fix\_ee3a858a4b8203101a31117f2974612b.xml

</td><td>

The script sys\_script\_fix\_ee3a858a4b8203101a31117f2974612b.xml introduced in Australia Patch 5 is causing upgrade delays due to the huge number of records.

</td><td>

1.  Log in to a Zurich instance.
2.  Ensure that there are more than 100K records in report\_table.
3.  Verify that the following isn't present:
    1.  The report\_table field in report\_stats table
    2.  The analytics\_visualization\_metadata table
4.  Verify that the script is not present in the instance: /nav\_to.do?uri=sys\_script\_fix.do?sys\_id=ee3a858a4b8203101a31117f2974612b.
5.  Upgrade the instance to Australia Patch 5.

 Observe that there are significant delays due to sys\_script\_fix\_ee3a858a4b8203101a31117f2974612b.xml.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1997164

</td><td>

Users are unable to sort the 'Saved Data Visualization' library when adding an element

</td><td>

A component was replaced with PresentationalListBuilder and deliberately sets enableSort to 'false' because the API doesn't support sorting.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2001651

</td><td>

Widget creation on a fresh dashboard in the second tab has unnecessary DB calls

</td><td>

 

</td><td>

1.  Create a Next Experience dashboard.
2.  Add 2 tabs.
3.  In the second tab, add a new data visualization widget.
4.  Save the dashboard.

 Expected behavior: There should be only one insert to par\_dashboard\_widget.

 Actual behavior: There is first an insert, then a delete, and then another insert. The delete is tracked in the sys\_audit\_delete table with the table name as par\_dashboard\_widget.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2004040

</td><td>

Enable dashboard logging by default as a system property

</td><td>

UI logs are not captured because it is set to 'false' by default.

</td><td>

1.  Open the Platform Analytics dashboard.
2.  Make some changes in Edit mode.
3.  Save the changes.

 Observe that in indexDB, there's no UI logs captured because it is set to 'false' by default in 'const isLoggingEnabled = getBooleanProperty\( 'com.snc.pae.dashboard.logging', false \);'

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2031048

 [KB3144237](https://hi.service-now.com/kb_view.do?sysparm_article=KB3144237)

</td><td>

Platform Analytics dashboards aren't loading and are stuck in a loading state indefinitely

</td><td>

This fix is to gracefully handle the NullPointerException \(NPE\) which Usage Analytics license entitlement engine throws. This doesn't solve the issues inside Usage Analytics license entitlement engine nor it introduces NPE exception itself. It simply doesn't send 'actions.canAccessInsights' in a dashboard payload when there's a NPE in the code. The dashboard would still load. The only consequence of this NPE from Usage Analytics license entitlement engine is now, if the user has insight access, they still can't see it.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2033980

 [KB3129184](https://hi.service-now.com/kb_view.do?sysparm_article=KB3129184)

</td><td>

Text index processing delay on analytics\_visualization\(column=type\) after upgrading to Australia

</td><td>

After upgrading to Australia, the user observed increased processing times related to text indexing events on the 'type' column of the analytics\_visualization table. This results in a backlog of index events.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2053337

 [KB3152732](https://hi.service-now.com/kb_view.do?sysparm_article=KB3152732)

</td><td>

There's an increased response time of Core UI dashboards in Australia

</td><td>

The response times of Pa\_Dashboard transactions degraded by 2000ms compared. This is coming from increase in SQL time.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2058867

 [KB3152710](https://hi.service-now.com/kb_view.do?sysparm_article=KB3152710)

</td><td>

Reduce the call cost on calling isPaPremium for every dashboard get call

</td><td>

On instances with large dashboard counts \(thousands of dashboards\), this multiplies an expensive entitlement check across the full dataset. This causes high memory usage, semaphore exhaustion, node failover, and an out of memory error.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2059204

</td><td>

Non-admin users can't read a localized tab name on PAR dashboard in a scoped application

</td><td>

A non-admin or dashboard\_admin user can't change the localized tab name on the scoped application's dashboard.

</td><td>

1.  Create a dashboard in the application scope.
2.  Add tabs.
3.  Share it with a non-admin user as an editor.
4.  Impersonate to the user.
5.  Change language except for English.
6.  Change tab names.
7.  Save the dashboard.
8.  Reload.

 Expected behavior: The tab names have been changed.

 Actual behavior: The tab names were not changed.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2037846

</td><td>

The Migration Center summary count doesn't match the list count for fully migrated dashboards

</td><td>

The Get Migration Summary Scripted API needs to be updated so that it calculates the total number of migrated dashboards in the same way as the Migrated List.

</td><td>

Scenario 1:

 1.  Create a few Core UI dashboards.2. Migrate them.
2.  Navigate to the PAR Dashboards table.
3.  Delete one or more migrated dashboards.

 Observe that the Migrated List count and the Summary count don't match.

 Scenario 2:

 1.  Create a Core UI dashboard containing a Dynamic Content widget.2. Migrate the dashboards.3. Navigate to the par\_coreui\_migration \_bridge\_dashboard table.
2.  Remove the record\(s\) associated with the dashboard that contains the Dynamic Content widget.

 Observe that the Migrated List count and the Summary count don't match.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2064612

</td><td>

Dashboard owner migration creates new pa\_dashboard records when triggered from a child domain

</td><td>

 

</td><td>

1.  Install the domain plugin with demo data.
2.  Create a core UI dashboard in TOP/MSP domain.
3.  Add a report in the global domain.
4.  Switch to the child domain TOP/MSP/MSP Technicians.
5.  Migrate it from the dashboard banner.
6.  Switch to the global domain.
7.  Open pa\_dashbaords.list and expand domains.

 Observe that there are two core UI dashboards.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2056633

</td><td>

A Playbook activity start delay doesn't work if its less than 11 seconds

</td><td>

The 12 second start delay seems to be the minimum honored threshold.

</td><td>

1.  Create a simple playbook with 1 stage and 2 instruction acts.
2.  Configure activity 2 to have a start with delay for 11 seconds.
3.  Test the playbook.
4.  Notice that the activity is set in progress after activity 1 completed and there is no 11 second delay.
5.  Configure activity 2 with a 12 second start with delay.
6.  Test the playbook

 Observe that after activity 1 is complete, the delay is honored, and activity 2 doesn't start until after 12 seconds.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2062029

</td><td>

Changes to the permission sets are not working as expected

</td><td>

The users should have the pd\_author role.

</td><td>

1.  Create a new playbook that uses 'incident' as the parent table.
2.  Add two stages. Each stage should include at least on activity.
3.  Activate it.
4.  Open the 'Process properties' side panel.
5.  Select the 'Runtime permissions' tab.
6.  Add a permission set of type users.
7.  Dot-walk to the 'Assigned to' value of the parent record
8.  Activate the playbook..
9.  Test the playbook using the incident that involves the users set up with the permissions for it.
10. View it in 'Preview'.
11. Impersonate the caller of the incident.
12. Return to the playbook preview.
13. Refresh it.

 Expected behavior: The user should see nothing.

 Actual behavior: The user can see the playbook execution.

</td></tr><tr><td>

Predictive Intelligence

 PRB2061744

</td><td>

Previous records of 'ml\_model\_artifact' are still present in the sys\_attachment table for the Data Analysis capability

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB2035128

</td><td>

Meter-based guardrails and controls

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB2035129

</td><td>

Pre-fill process configuration fields with AI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1993708

</td><td>

When moving a story from one project to another, the actual effort doubles on the story

</td><td>

When assigning a story with actual hours more than 24 hours, suppose 40 hours, the story takes it as 1 day and 16 hours. However the project only adds the hours and not the days, therefore the project actual hours become just 16 hours.

</td><td>

1.  Navigate to an existing project with a story, or create a new one.
2.  Locate another project, or create a new one.
3.  Take one of the stories with logged 'Actual Hours' and move it to a different project.
4.  Navigate to the **Stories** \[rm\_story\] list view.
5.  Delete the existing **Project** field and change it from here.
6.  Choose a project.

 Observe the 'Actual effort' has doubled on the story.

</td></tr><tr><td>

Project Management

 PRB2036275

</td><td>

ProjectTemplate.java calls extension point outside null guard, so applyTemplate\(\) silently returns zero tasks within flow execution context

</td><td>

When PTGlobalAPI\(\).applyTemplate\(\) is called within a flow action \(for example, 'Implement SPM Oversight'\), the Customer Project record is created but zero project tasks are generated. The same applyTemplate\(\) call succeeds from Background Scripts on the same project record. The ProjectTemplate scripted extension point \(sys\_script\_include.1e6e73619f001200598a5bb0657fcfc2, line 24\) performs a GlideRecord.get\(\) call where the table name resolves to null within the flow transaction context. This causes applyTemplate\(\) to silently return zero tasks. The PPM engine then attempts to recalculate the project, but the planned\_task record doesn't exist yet, producing the following error: 'com.snc.planned\_task.core.PlannedTaskAPI: PPM Unable to Recalculate Task : \[sys\_id\] Cannot invoke 'com.snc.planned\_task.core.PlannedTask.getStartDate\(\)' because 'task' is null'.

</td><td>

1.  Configure CSM Order Management project oversight with decision tables, field mappings, and project/task templates \(template tasks table = customer\_project\_task\).
2.  Submit a customer order via REST API that triggers a flow containing the 'Implement SPM Oversight' flow action.

Observe that the flow action calls OrderLinePrjUtilOOB.createProjectForOrderLine\(\), which calls PTGlobalAPI\(\).applyTemplate\(projectSysId, templateId, actualStartDate\) at line 58 of OrderLinePrjUtilOOB.js. The Customer Project is created but zero Customer Project tasks are generated. The short description remains unchanged.

3.  Check the logs for the error 'com.snc.planned\_task.core.PlannedTaskAPI: PPM Unable to Recalculate Task : \[sys\_id\] Cannot invoke 'com.snc.planned\_task.core.PlannedTask.getStartDate\(\)' because 'task' is null'.
4.  Run the identical applyTemplate\(\) call from Background Scripts on the same project record.

Observe that tasks are created successfully.


 Expected behavior: applyTemplate\(\) creates Customer Project tasks from the template within the flow action.

 Actual: Zero tasks are created. The ProjectTemplate extension point encounters a null table name because the project record isn't fully committed in the flow transaction.

</td></tr><tr><td>

Project Management

 PRB2050675

</td><td>

Allow the change of constraint date at the parent task level

</td><td>

Enure the child task start date honors both the parent task and its constraint dates.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB2052767

</td><td>

An incorrect auto-update for the multi-currency setup in the project workspace

</td><td>

Remove the logic to allow the negative budget from the business rule 'Validate Cost Breakdowns.'

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB2066164

</td><td>

Certain users do not see all the dropdown list values within a grid cell in the 'RIDAC' tab

</td><td>

This issue occurs only in the grid view.

</td><td>

1.  Open the Project Workspace.
2.  Navigate to **RIDAC**.
3.  Open a project.
4.  Expand 'Risk.

 Observe the dropdown list for the **Impact** field.

</td></tr><tr><td>

Project Management

 PRB2071094

</td><td>

Display a message if the parent change fails due to schedule conflicts

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB1950825

 [KB3148345](https://hi.service-now.com/kb_view.do?sysparm_article=KB3148345)

</td><td>

Remote Process Synchronization \(RPS\) sends more records to the target than that published into the transport queue

</td><td>

Remote Process Synchronization \(RPS\) sends more records to the target than those published into the transport queue. This results in discrepancies between outbound HTTP logs and transport queue data. The issue arises from a performance optimization feature that saves last positions for outbound jobs. When multiple capture definitions \(ih\_sync\_capture\_definition\) exceed the number of buckets, cursor backtracking occurs, leading to reprocessing of records and discrepancies in record counts. This can cause intermittent or unavailable connections between consumer applications with general usage of RPS. The issues manifest as slow response times, frequent disconnections, and periods where the connection appears down despite the RPS connection showing as 'active'. However, remote task records remain in the 'New' status and do not progress, creating a risk of transaction impact.

</td><td>

 

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB2052613

</td><td>

Extremely slow processing of the RPS queue on Impact

</td><td>

With the number of connections increasing, slow processing occurs exponentially.

</td><td>

1.  Log in to Impact.
2.  Check the transaction time.
3.  Query the sn\_transport\_queue table to get the volume of the 'ready' transaction.
4.  On a subprod instance, onboard the instance via the impact onboarding process.
5.  Run the data migration.
6.  Verify the time it takes to migrate the data.

 Notice that with one or two connections, the transaction seems fast. But as the number of connections increase, performance issues happen exponentially.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB2055484

</td><td>

ProcessSyncReplicationTable's queryShard includes null labels

</td><td>

Both labeled and unlabeled entries are returned.

</td><td>

1.  Write an unlabeled entry into a cdc\_queue\_ih shard table.
2.  Write a second entry with a valid label.
3.  Trigger an RPS outbound poll for that valid label.

 Expected behavior: Only rows matching the requested label\(s\) should be returned, unlabeled entries should never match.

 Actual behavior: Query returns both the labeled entry and the unlabeled entry.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB2066418

</td><td>

Add debug logging to OutboundQueueDao.fetchNextValidEntry

</td><td>

 

</td><td>

1.  Set up RPS on an instance.
2.  Navigate to **RPS properties**.
3.  Turn on 'Activate debug logging'.

 Notice there is no timing information for fetchNextValidEntry\(\) in the logs.

</td></tr><tr><td>

Request Management

 PRB2075931

</td><td>

Cart item hints do not get copied when ordering from a draft item

</td><td>

 

</td><td>

1.  Create a draft cart item.
2.  Add the hint to update the request parent to some incident.
3.  Checkout the cart item.

 Notice that the cart item hint doesn't gets populated to the request.

</td></tr><tr><td>

Roles

 PRB2023810

</td><td>

Instances without explicit roles throw an error when invoking agents with a 'Nobody' role mask

</td><td>

The following error appears in the logs: 'Role 'snc\_external' not found. Cannot be automatically created: no thrown error'.

</td><td>

1.  Open an instance that doesn't have the explicit roles plugin.
2.  Trigger an AI Agent that has a role mask on the **Nobody** field.

 Observe the error in the logs: 'Role 'snc\_external' not found. Cannot be automatically created: no thrown error'.

</td></tr><tr><td>

Roles

 PRB2052882

</td><td>

Inherited roles aren't added back when patcher is on and the state of 'User has role' is changed from pending\_approval to active

</td><td>

When the user updates the state of the 'User has role' record to active, no records are created for inherited roles.

</td><td>

1.  Enable the glide.security.inh\_count\_patcher.enabled property to true.
2.  Assign a user with an admin role and with the state as pending approval.

No 'User has role' records should be created for inherited roles.

3.  Update the state of the 'User has role' record to active.

 Expected behavior: 'User has role' records are created for inherited roles with the state as active.

 Current behavior: No 'User has role' records are created for inherited roles.

</td></tr><tr><td>

Schedule Optimization

 PRB2022407

</td><td>

getRefRecord\(\) scoping bypass for the 1.0.1 release

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Search Suggestions

 PRB2051556

</td><td>

The scheduled job deletes search suggestion and business rules, and should leave ones with the global namespace alone

</td><td>

The business rules created should not get deleted by the scheduled job.

</td><td>

1.  Create a business rule on some table.
2.  Set the business rule to run on the update and delete.
3.  Name it starting with 'Disable'.
4.  Set the script.
5.  Run the scheduled job, 'Remove obsolete search suggestion BRs' under sysauto\_script.

 Observe that the business rule created was deleted, and shows up in the sys\_update\_xml table.

</td></tr><tr><td>

Server-side scripts

 PRB2056793

 [KB3141731](https://hi.service-now.com/kb_view.do?sysparm_article=KB3141731)

</td><td>

ESLatest sibling scopes shouldn't use scoped sandbox scopes

</td><td>

ESLatest sibling scopes are created when 'Ecmascript 2021' mode is turned on for global scripts. When they interact with something that requires sandbox script execution, they end up inadvertently creating an isolated scope for what essentially should be the global sandbox scope. There's a specific code path in KittyScriptEvaluator that attempts to re-initialize GlideElement in a scoped sandbox where it's not available leading to re-initialization errors seen in the logs and triggering the causal chain that invokes this path.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB2076586

 [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB3151029](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3151029)

</td><td>

Plugin scripts aren't registered in some app nodes

</td><td>

On some instances, a subset of nodes can experience the mega menu in Employee Center being broken. The following error appears on the screen when navigating to Employee Center, and users are unable to use the menu: 'ErrorServer JavaScript error 'sn\_taxonomy' is not defined.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Builder

 PRB2033462

</td><td>

When creating a catalog item via Catalog Builder, UI policies configured in a previous step aren't visible on the 'Review and Submit' step

</td><td>

It appears that the GraphQL query is not being triggered for the catalog\_ui\_policy table.

</td><td>

1.  Open Catalog Builder.
2.  Create a new catalog item.
3.  Configure a UI Policy, Client Script, and any other required details.
4.  Navigate to the **Review and Submit** step.

 Notice that the UI Policy is not displayed, even though one has been configured.

</td></tr><tr><td>

Service Catalog Builder

 PRB2033565

</td><td>

A UI policy action created from Catalog Builder can't be seen in the platform

</td><td>

 

</td><td>

1.  Log in to Catalog Builder.
2.  Create a question on a catalog item.
3.  Create a UI policy and associate an action from the 'UI Policy' tab.
4.  Open the item in 'Edit in Advanced View' to get the item in the platform.
5.  Open the UI policy from the related list.
6.  Open the UI policy action.

 Notice that the variable name is empty, and the valid options are not seen on the right side.

</td></tr><tr><td>

Service Catalog Builder

 PRB2063629

</td><td>

The **UI Policy Action** field message fields re-appear after variable selection in Catalog Builder

</td><td>

 

</td><td>

1.  Open the catalog item in the CB wizard.
2.  Navigate to **UI Policy** &gt; **Add behavior** &gt; **Actions** &gt; **Add action**.
3.  Select the **Plain Label/Rich Text Label/Container Start** variable.
4.  Wait 3 seconds for onChange.

 Expected behavior: The field message should not be displayed in the UI policy.

 Actual behavior: The fields re-appear after the policy refresh.

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB2018000

</td><td>

Performance issues with the Employee Center Standard Ticket Page Widget

</td><td>

This issue was observed in Australia, but the function works as expected in Zurich. This impacts the Service Portal 'Standard Ticket Header Widget.' The user observed that the RITM 'Show details' dropdown list alignment is off, and the REQ **Show/Hide Details** dropdown list button option is shown even if there are no additional details to show.

</td><td>

1.  Open the Employee Center Portal \(esc\).
2.  Submit a Request.

On the standard ticket page, observe that the **Show/Hide Details** button is shown even if there are no additional details to show.

3.  On the 'Requested items' tab, select on **RITM** number.

Notice that it will redirect to the standard ticket page for the RITM.


 Expected result: The RITM alignment is aligned without padding-left at 0px.

 Actual result: The RITM **Show details** button alignment is off, and the REQ **Show/Hide Details** dropdown list button option is shown even if there are no additional details to show.

</td></tr><tr><td>

Service Catalog

 PRB1972924

</td><td>

The 'Generate sequence' UI action gives a missing start rule error on Playbook 28.2.1

</td><td>

This issue was observed in Playbook 28.2.1, but not in 28.0.8.

</td><td>

1.  Open any order guide.
2.  Generate the sequence.
3.  Open the playbook created.

 Observe the missing start rule errors.

</td></tr><tr><td>

Service Catalog

 PRB2033096

</td><td>

Catalog redirection throws a 404 error page when accessed from the chat responses

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2040266

</td><td>

g\_form.clearValue should clear the value of the Lookup Select Box, even when there are no reference qualifiers

</td><td>

When loading the XML files, this creates Lookup Select Boxes. One file creates an item option named 'user\_group' under the 'AWS account request' catalog item, which is a is a Lookup Select Box that references the sys\_user\_group table and its reference qualifier is 'javascript: 'manager=' + current.variables.user'. Another file creates an item option named 'user' under the 'AWS account request' catalog item, which is a Lookup Select Box that references the sys\_user table. The next file is a catalog script for the 'AWS account request' catalog item, which logs the value of the **user\_group** field when there is a change to the user field.

</td><td>

1.  Load the XML files.

Notice that these XML files create a item options named 'user\_group' and 'user' under the 'AWS account request' catalog item, and that Lookup Select Boxes are created.

2.  Navigate to the catalog item.
3.  Change the **User** field to any value.

 Expected behavior: The **User Group** field should be cleared, and the alert should show an empty value.

 Actual behavior: The **User Group** field is cleared in the UI, but the alert shows the previous value.

</td></tr><tr><td>

Service Catalog

 PRB2070973

</td><td>

Add Now Assist AI-usage tracking fields and options to the catalog\_builder\_analytics table

</td><td>

Extend the catalog\_builder\_analytics table to support tracking of Now Assist AI usage during catalog building.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2073331

</td><td>

Family changes for AIX STP

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2073333

</td><td>

Family changes for the AIX catalog item form

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2040618

 [KB3137540](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137540)

</td><td>

The 'Application Service Manual Ep Cleanup' job doesn't work

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Mapping

 PRB2052536

</td><td>

In Service Map, additional related list tabs \(Changes-current/past, Incident, Problem\) are permanently stuck on 'Loading...'

</td><td>

 

</td><td>

1.  Open any Operational Service in the Event Management View.
2.  Add indicators.
3.  Select on the added tabs for the indicator.

 Notice that it's permanently stuck on 'Loading...'.

</td></tr><tr><td>

ServiceNow Data Catalog \(Glide\)

 PRB2009278

</td><td>

Metadata collectors can generate graphs too large to upload as attachments

</td><td>

The mysql collector ran to completion, but uploading the attachment failed as the attachment was too large.

</td><td>

 

</td></tr><tr><td>

ServiceNow Data Catalog \(Glide\)

 PRB2064415

</td><td>

Update glide-process-flow to support SnowsK8s workflow action steps

</td><td>

The glide-process-flow needs to support SnowsK8s workflow action steps, and connectivity between SnowsK8s and glide requires a certificate definition to be installed.

</td><td>

 

</td></tr><tr><td>

ServiceNow Data Catalog \(Glide\)

 PRB2070138

</td><td>

Update Glide to accommodate a new ID for consolidated DCG \(dcg-app\)

</td><td>

The ServiceNow Data Catalog is being re-bundled into a new, consolidated scoped application. In order to prevent collisions with previous installations of the catalog, a new scoped application ID was used.

</td><td>

 

</td></tr><tr><td>

ServiceNow Data Catalog \(Glide\)

 PRB2070443

</td><td>

Fix MID compression for metadata collectors

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB1831844

</td><td>

Users are unable to convert a sys\_app-based application due to a company key

</td><td>

The user is unable to convert an app from an instance with the error, 'Not allowed to download application x\_taniu\_tan\_core. Check that you either have maint access or have added your company key \(e.g. sn for ServiceNow\) to the sn\_appauthor.all\_company\_keys system property.'

</td><td>

1.  Load an open source app from a third party using Studio.
2.  Verify that it can be see.
3.  Edit the sys\_app based scope in the instance.
4.  Open SDK.
5.  Attempt to convert it.

 Observe the error message.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2041355

</td><td>

The sys\_gen\_ai\_feature\_mapping and sys\_gen\_ai\_strategy\_mapping records are silently dropped during Now Assist skill installation via Studio and BuildAgent

</td><td>

All records including feature mappings and strategy mappings should be installed successfully.

</td><td>

1.  Login as an admin user.
2.  Open Servicenow Studio and Build Agent.
3.  Provide a prompt to create a Now Assist skill for any use case.
4.  Provide the necessary answers to the Build Agent.

Notice that the Build Agent will build and install the skill.

5.  Open thesys\_gen\_ai\_feature\_mappin and sys\_gen\_ai\_strategy\_mappin tables.

 Observe whether any records are created or not.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2060181

</td><td>

ListElementLoader reinserts records if the child elements has the action attribute as 'INSERT\_OR\_UPDATE;

</td><td>

 

</td><td>

1.  Create an application on the instance with the table and list metadata.
2.  Remove the list metadata.
3.  Export the app.
4.  Reinstall the application.

 Expected behavior: The app should be installed and the list metadata should still remain deleted.

 Actual behavior: The list gets re-inserted again.

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

 PRB2067936

</td><td>

GlideQuery Schema.findInvalidChoiceError throws 'Cannot find function toLowerCase in object true' for non-string \(boolean\) values on **Choice/dot-walked** fields

</td><td>

A GlideQuery.where\(field, value\) call crashes when the value is a JS boolean \(true/false\) instead of a string. This occurs if the field either has a choice list configured in schema or is dot-walked \(for example, reference.booleanField\). The dot-walked case bypasses the choice-check guard unconditionally, regardless of whether the target field actually has choices. In production, this crashes a legacy Workflow 'if condition' script mid-transaction \(via WorkflowScopedScriptRunner/WFActivityHandler\). It surfaces the error as a real exception rather than silently swallowing it, faulting the workflow activity.

</td><td>

 

</td></tr><tr><td>

ServiceNow Studio \(Family Channel\)

 PRB2063560

</td><td>

True up the Glider Store app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal Core Widgets

 PRB1819286

</td><td>

When updating the font-family in the EC theme, it doesn't update the font in the AI search results page

</td><td>

According to the 'Theming for AI Search in Service Portal' documentation, users can control the look and feel of AI search results. The user was attempting to update the default font family of the EC theme from Lato, Arial, sans-serif, to 'Segoe UI', sans-serif. When updating the EC theme CSS properties, this changed the font on the home page as expected, but failed to change font in the AI Search results page. Also, the faceted search widget doesn't change and was still using Lato, Arial, sans-serif.

</td><td>

 

</td></tr><tr><td>

Service Portal Experience

 PRB2051231

</td><td>

The user observes the error '\{0\} has been rejected' in the base instance 'Approvals' widget

</td><td>

The out of the box widget 'Approvals' displays an error info message '\{0\} has been rejected' when selecting the navigation buttons **Next** and **Previous**.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1913741

</td><td>

Guest and low-privilege users are unable to retrieve translation keys due to GlideRecordSecure Restrictions on sys\_ux\_lib\_component

</td><td>

When accessing the sys\_ux\_lib\_component table as an admin user, records are visible as expected. However, when impersonating a less privileged user \(such as a user with no roles\), the same table is not accessible, and no data is returned. Currently, one of the Service Portal widgets calls this table using GlideRecordSecure. As a result, users without the necessary roles cannot retrieve any records from sys\_ux\_lib\_component. This leads to a failure in fetching translation keys, causing translations to not work for guest or unauthenticated users. This is not the expected behavior for guest users, who should still be able to see translations.

</td><td>

1.  Log in as an admin.
2.  Open the sys\_ux\_lib\_component table.

Observe that the records are visible.

3.  Impersonate a user with no roles.
4.  Attempt to access the same table.

Observe that no records are visible.


 Observe that in the Service Portal widget \(using GlideRecordSecure\), records are not returned for users without roles, resulting in missing translation keys and broken translations.

</td></tr><tr><td>

Service Portfolio Management

 PRB2029361

</td><td>

The 'Outage calculation' business rule is not working when the date format is set to DD/MM/YYYY

</td><td>

The **Duration** field is not calculating correctly because the 'Outage Calculation' business rule does not work when the date format is set to DD/MM/YYYY.

</td><td>

 

</td></tr><tr><td>

Session Management

 PRB2038268

</td><td>

Write-once session values are lost after the second node move

</td><td>

O\\n a node move, the receiving node restores the session state from the previous node's saved record and folds it into its own baseline. Since the end-of-transaction save only persists changes relative to that baseline, values that were restored but not modified during the current session are excluded from the new node's saved record. The restore chain only reaches one hop back, so a value that was written once survives a single node move, but it's lost on the second move. Values re-written every hop survive because they always appear as a change relative to the baseline. Write-once values \(for example, session properties and client data\) are lost after the second node move.

</td><td>

1.  Authenticate through GIG.
2.  Set a write-once session property \(a value not updated after the initial write\).
3.  Force a GIG re-balance \(node A to node B\).
4.  Verify that the property is present.
5.  Force a second GIG re-balance \(node B back to node A, or to a third node\).

 Observe that the property is now null/missing.

</td></tr><tr><td>

Session Management

 PRB2077746

</td><td>

In GIG, the JSESSIONID-to-node affinity is only learned from request cookies, never from response Set-Cookie. The snc\_session\_affinity\_node is set to 'Secure-only', which breaks stickiness for fresh sessions over plain HTTP

</td><td>

GIG's session affinity for a brand-new session depends entirely on the client echoing GIG's own snc\_session\_affinity\_node cookie. GIG never learns the JSESSIONID-to-node mapping from the response that carries Set-Cookie: JSESSIONID. Additionally, snc\_session\_affinity\_node is always emitted with the secure attribute, and the plain HTTP standard cookie stores it and never sends it back. As a result, it does not echo the affinity cookie, and gets every follow-up request load-balanced, including requests that already carry a valid JSESSIONID.

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

Smart Assessment Glide Family Platform Dependencies

 PRB2074438

</td><td>

API for CSV export of assessments

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Smart Assessment Glide Family Platform Dependencies

 PRB2074439

</td><td>

Apache POI java class

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2018383

 [KB2986694](https://hi.service-now.com/kb_view.do?sysparm_article=KB2986694)

</td><td>

A Microsoft per-core license metric isn't visible after a Zurich or Australia upgrade

</td><td>

The MS per core metric was moved from the apply\_once folder to the update folder. The fix script to set the metric group was overwritten, since the update folder file insert ran after. Thus, the MS per core uploaded with no metric group.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB2071875

</td><td>

Finalize the list of license metrics to be shipped

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2073947

</td><td>

Create samp\_software\_filter and samp\_software\_custom\_filter tables in app-itam-sam for software junk filtering

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Publisher Pack for Oracle

 PRB2062263

</td><td>

The Oracle option extension for Windows not working with Oracle Wallet changes for Windows

</td><td>

 

</td><td>

1.  Create applicative credentials for the CI type 'cmdb\_ci\_db\_ora\_instance' for the Oracle Instance to the ServiceNow instance.
2.  Identify if the discovery process is utilizing the applicative credentials stored on the ServicNow instance or external credential vault.
3.  Execute the command on the target server.

 Observe that the User/Credential combo printed in plain text in the Windows server shell log is utilizing the Oracle SQL\*Plus utility.

</td></tr><tr><td>

Software Installation Deduplication

 PRB2068830

</td><td>

Each dedup UPDATE should carry at most BATCHSIZE sys\_ids, bu it carries the sum of the sys\_ids from 100 \_markActive calls, with no upper bound

</td><td>

The 'SAM - Deduplicate Install Table' scheduled job issues UPDATE statements against cmdb\_sam\_sw\_install \(SET deduplicated='1', active='1', primary\_install=NULL\). Most executions complete in roughly 200 milliseconds, but intermittently a single execution takes over 40 minutes and causes database impact. The code that produces this statement was written to cap each UPDATE at a fixed batch size, but the cap doesn't take effect. Each UPDATE can therefore carry an unbounded number of sys\_ids, which produces the intermittent long-running statements.

</td><td>

 

</td></tr><tr><td>

Software Spend Detection

 PRB2040404

</td><td>

Upgrades to spend detection

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Source Control Engine

 PRB2054438

</td><td>

A re-link of a customized Store app to git via Source Control fails with an error code '1030'

</td><td>

The application should link to the git repository without the error code 1030 occurring.

</td><td>

1.  Provision two instances \(DC/TD\) with apprepo setup and at least 1 instance with midserver.
2.  Create an application in the instance.
3.  Publish that application.
4.  Now the instance with midserver, install the published application.
5.  Make a change in that application.
6.  Source control this application to git using a MID server.
7.  Delete the sys\_repo\_config for this application this will un-link the application from git.
8.  Attempt to link to the source control again to the same repository using a mid server.

 Expected behavior: The application smoothly links to the git repository.

 Actual behavior: The error code 1030 occurs.

</td></tr><tr><td>

Stream Connect Core

 PRB2054184

</td><td>

Stream Producer update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Archiving

 PRB1974369

</td><td>

Compaction is not working for archived tables in the columnar format

</td><td>

An error occurs after migrating the columnar format, updating the compaction properties, and running the background script.

</td><td>

1.  Migrate ar\_ table to columnar format.
2.  Update the compaction properties.
3.  Run the background script, 'new GlideTableCompactor\(\).compact\('tableName'\);'

 Notice that there is an error, 'Table didn't compact as... Sys\_id not indexed on root storage table.'

</td></tr><tr><td>

System Archiving

 PRB2056839

</td><td>

Compaction should not be attempted for columnar tables

</td><td>

 

</td><td>

1.  Migrate ar\_ table to columnar format.
2.  Update compaction properties.
3.  Run the background script.

 Expected behavior: Compaction should be blocked because this is a columnar table.

 Actual behavior: The error occurs, 'Error: Table didn't compact as... Sys\_id not indexed on root storage table.'

</td></tr><tr><td>

System Events

 PRB2063610

</td><td>

For NowMQ redistribution, extend the UI-only participation property to a comma-separated, node-type exclusion list

</td><td>

Currently, UI nodes don't participate in NowMQ event redistribution/delegation by default. A property \(nowmq.allow.ui.node.redistribution, default false\) was introduced previously to let UI nodes opt in to participating in delegation. Dedicated worker nodes exclusively process P0-P4 flow engine event jobs for a tighter SLA \(~20s\). These dedicated nodes should process events routed directly to them, but must not receive delegated/redistributed events from other nodes. Accepting the delegated load would consume capacity reserved for the dedicated workload. Health-statistics and check-in from NowMQHealthMonitor currently don't account for this.

</td><td>

1.  Provision a dedicated worker node type \(for example, Worker.EmOnly.Primary\) intended to exclusively process P0-P4 flow engine jobs.
2.  Note that NowMQHealthMonitor still sends check-in/health stats for this node to the delegator.

 Observe that the delegator can still delegate other P5+ events to this node, since only UI nodes are excluded today via nowmq.allow.ui.node.redistribution. This consumes capacity reserved for the dedicated P0-P4 workload.

</td></tr><tr><td>

System Events

 PRB2068908

</td><td>

'Flow Engine Interactive Event Handler' jobs shouldn't participate in thread pool event processing

</td><td>

The flow.fire events should be processed by either two threads or by the three 'Flow Engine Event Handler' jobs. Instead, the P5 events are processed by the 'Flow Engine Interactive Event Handler' jobs that are reserved for P0-P2 event processing.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2080453

</td><td>

NowMQ events never get delegated on Worker.Default nodes due to a broken participation check

</td><td>

 

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB2053898

</td><td>

The import set telemetry is causing 3 extra queries per import set row

</td><td>

 

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB2073197

</td><td>

Parallel loading on a data source overrides scheduled import 'Run as' user context on sys\_import\_set records

</td><td>

When a scheduled\_import\_set is configured with a data source that has enable\_parallel\_loading = true, the resulting sys\_import\_set record is created with sys\_created\_by = system instead of the user specified in the **Run as** field of the scheduled\_import\_set. This causes the import to execute in global domain context, breaking domain separation for staging table records.

</td><td>

1.  Create a data source with enable\_parallel\_loading = false.
2.  Create a scheduled\_import\_set with **Run as** set to a domain-specific user.
3.  Execute the scheduled import.

Observe the sys\_import\_set record sys\_created\_by = the **Run as** user.

4.  Change the data source to enable\_parallel\_loading = true.
5.  Execute the scheduled import again.

 Observe the sys\_import\_set record sys\_created\_by = system \(incorrect\)

</td></tr><tr><td>

System Web Services

 PRB2074287

</td><td>

Telemetry Data Connector update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2074288

</td><td>

Action fabric metering for billing

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2074289

</td><td>

Update for the AF Usage Dashboard app

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Time Card Management

 PRB2051508

 [KB3139332](https://hi.service-now.com/kb_view.do?sysparm_article=KB3139332)

</td><td>

The **user.manager** field shows as empty when opening the 'Pending Approval' module for Time sheets

</td><td>

The filter is empty for the **user.manager** field.

</td><td>

1.  Impersonate a user with submitted time sheets.
2.  Navigate to **Time Sheet** &gt; **Pending Approval**.

 Notice that the filter shows empty for **User.Manager**.

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2059215

</td><td>

Azure classic trace collector doesn't consider Credential IDs for AI and ML services

</td><td>

AzureTraceCollector ignores credential IDs supplied as configuration update parameters. It only considers credential alias names.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2074229

</td><td>

Trace collector MID code for Google Cloud custom agents

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2081553

</td><td>

Convert app-domain-util app as a hosted plugin

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB2035673

</td><td>

GIG path doesn't block requests to /WEB-INF and /META-INF, which is a Servlet Spec 10.5 violation

</td><td>

It's expected that all requests return HTTP 404. Instead, requests sent through GIG pass through to the servlet/filter chain.

</td><td>

Scenario 1:

 1.  Start a Glide instance with GIG enabled.
2.  Send a request to a protected path through GIG: 'curl -v h gig-host:gig-port/WEB-INF/web.xml'.

 Observe that the request reaches the servlet layer instead of being rejected with 404.

 Scenario 2:

 1.  Start a Glide instance.
2.  Send the same request directly to the Tomcat port \(bypassing GIG\).

 Observe that Tomcat returns 404 \(blocked by StandardContextValve\).

</td></tr><tr><td>

Transaction Management

 PRB2068154

</td><td>

Remove glide.gig.enable from the property list so a default xml record can be shipped

</td><td>

The glide.gig.enable property isn't present, despite this record. Also, the com.glide.gig plugin is installed.

</td><td>

Provision a new instance on the main branch.

 Notice that the glide.gig.enable property isn't present, despite the record and the fact that the com.glide.gig plugin is installed.

</td></tr><tr><td>

Transaction Management

 PRB2070038

</td><td>

The semaphore usage metric \(semaphore mean\) reports the gateway fixed thread pool usage when Glide Ingress Gateway \(GIG\) is turned on. This inflates the value and triggers false monitoring alerts

</td><td>

When GIG is turned on, the semaphores\_used metric \(xmlstats semaphores mean; legacy cmdb\_metric\_semaphores.semaphores\_mean\) reports much higher values than in non-GIG mode. This is because the metric is measuring the shared gateway fixed thread pool instead of the legacy per-node semaphore pool. Monitoring alerts keyed on semaphore mean fire spuriously.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1948198

</td><td>

The Service Operations Workspace \(SOW\) **Template creation** field dependencies are working inconsistently

</td><td>

When users fill out templates for incidents, the behavior of the dependent fields such as **Category** and **Subcategory** are inconsistent. If the user creates the template from a pre-existing record, they will be able to see the proper subcategory options unless they attempt to change the category on the new template.

</td><td>

1.  Open a base instance.
2.  Open Service Operation Workspace.
3.  Open a new incident.
4.  From right contextual sidebar, select the **Templates** icon.
5.  Create a new template.
6.  Add the **Category** and **Subcategory** fields if it isn't already there.
7.  Set the **Category** field.
8.  Try to set the **Subcategory** field.

 Observe that the user doesn't see options that should be there, such as CPU, Disk, Mouse.

</td></tr><tr><td>

UI Field Administration

 PRB2024073

</td><td>

An **HTML type** field doesn't always display as full size when its in read-only

</td><td>

When creating an **HTML type** field and applying a UI policy or client script to make it read-only, it doesn't always show its full size. It shows in a collapsed form until the entire page is refreshed.

</td><td>

1.  Open an Australia instance.
2.  Navigate to **incident.LIST**.
3.  Open any incident which is in the 'In progress' state.
4.  Under 'Sections', navigate to **Related Records**.

 Expected behavior: The field value should get displayed fully in read-only mode.

 Actual behavior: The field doesn't show its full size, and it gets collapsed.

</td></tr><tr><td>

UI Field Administration

 PRB2040359

</td><td>

The 'Attachments' component isn't working for multiple files when the 'Show preview' modal during an upload option is turned off

</td><td>

When the option on 'properties' show the preview modal, the upload is disabled when attempting to upload multiple files, and does not work.

</td><td>

1.  Open any workspace in UI Builder.
2.  Add an attachment component.3. Leave the option.
3.  Allow 'Multiple file upload' enabled.
4.  Disable 'Show preview modal during upload.'4. Test this the workspace, attaching multiple files at once.

 Observe that only one file gets uploaded.

</td></tr><tr><td>

UI Field Administration

 PRB2073310

</td><td>

Support the **Markdown** field type in UI16, Seismic, and LIT

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2082758

</td><td>

The Advanced Qualifier Reference is getting skipped while doing a List edit operation for a **Reference** field

</td><td>

 

</td><td>

1.  In incident table, set up advanced reference qualifier for 'Assigned to field'.
2.  On SOW workspace, navigate to the incident list.
3.  Try to list edit the assigned to field.
4.  Select the **Look up** icon.

 Expected behavior: The advanced reference qualifier should be applied.

 Actual behavior: Advanced reference qualifier is getting skipped.

</td></tr><tr><td>

Upgrade Center

 PRB2016580

</td><td>

After upgrading instances from Zurich to Australia, several records show up on the skipped list belonging to the sn\_glider or sn\_build\_agent. It shows the error 'Unable to compare, unable to find a current record'

</td><td>

After upgrading a Zurich instance to Australia the upgrade monitor will have a list of skipped records. But when trying to resolved issue, users observe the error: 'Unable to compare, unable to find a current record' when trying to compare to current.

</td><td>

1.  Provision a Zurich instance.
2.  Make sure that the plugin sn\_glider and sn\_build\_agent are not on the latest version.
3.  Upgrade the instance to Australia.
4.  Post upgrade review the skipped records.
5.  Filter for scripts or records that are part of the sn\_glider or sn\_build\_agent.
6.  Open a record that is skipped and click on the UI action Compare to Current.

 Observe the error.

</td></tr><tr><td>

Upgrade Center

 PRB2075225

</td><td>

Cloning an AI-generated sys id in the client script causes zboot errors

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB2076321

</td><td>

Apply defaults on the loading of XML records with apply\_defaults=true attribute

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2028133

</td><td>

The alm\_asset form breaks when configuring the **Activity** fields due to a service worker error

</td><td>

This issue was observed when using Firefox V90.0.2 from locked down dev versions.

</td><td>

1.  Navigate to **alm\_asset.do**.
2.  Fill in the mandatory fields.
3.  Save the record.
4.  In the 'Activity tab', select the **Filter** button.
5.  Select **Configure Available Fields**.
6.  Add or remove the **Comments** field.
7.  Save it.

 Observe that the URL will stay in slushbucket.do and the form will be broken or blank. Buttons such as the **Filter** in the Activity stream and **Reference** icons will be broken, causing the test failure.

</td></tr><tr><td>

UX Framework

 PRB2054946

</td><td>

Keyboard shortcut remapping for admins and users

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Versatile Node and Cluster Configuration

 PRB2072954

</td><td>

Frontend Service for Glide POC

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Versatile Node and Cluster Configuration

 PRB2080145

</td><td>

GIG ports can reorder glide nodes and select the wrong default database

</td><td>

Multi-node Glide ITs can select a different default Glide node when GIG is enabled. GlideNodeScanner sorts nodes using GlideNode.getPort\(\), but getPort\(\) intentionally returns the effective ingress port. Because GIG ports are allocated independently, enabling GIG can reverse node order even though the Glide topology is unchanged. This caused VirtualAgentTimeoutConversationsIT on track/tsmgmtalpha to open the second isolated database through GIG, while AC\_UpdateSetIT had activated the Virtual Agent public-page records only in the first database. The browser received 302 /session\_timeout.do and stalled waiting for VA initialization.

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

 PRB2013952

</td><td>

Remove the deprecate system property 'com.glide.cs.conversation.entity.cache.enabled'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2014908

</td><td>

The unread message notification and message preview are not displayed for the users

</td><td>

The user should see the notification of the unread message on the **Engagement Messenger \(EM\) Launch** Icon. The message preview popup should be displayed when the EM is closed and then logged in again.

</td><td>

1.  Log in to the instance as admin.
2.  Navigate to **Engagement Messenger \(EM\)** &gt; **Modules**.
3.  Ensure the module is activated.
4.  Setup an asynchronous chat.
5.  As an agent, log in as Abel Tuter.
6.  Navigate to the **/now/cwf/agent/inbox**.
7.  Mark the agent status as 'Available'.
8.  Open the EM page in new window.
9.  4. Log in as Abraham Lincoln.
10. Select **Start a Chat** &gt; **Show me everything** &gt; **Live Agent Support**.
11. In the Agent window, accept the chat to start the conversation.

Observe that as Abraham Lincoln, the agent greeting message appears.

12. Close the EM window.
13. As an agent, send a message to Abraham Lincoln.

 Observe that in the EM page, Abraham Lincoln doesn't receive the notification of the unread message on the **EM Launch** icon. The message preview is also not displayed when the EM is closed and then logged in again.The user gets a notification sound, but the notification is not displayed.

</td></tr><tr><td>

Virtual Agent

 PRB2033259

</td><td>

The Language detection doesn't work properly with Agentic mode for both the standard and Enhanced chat

</td><td>

 

</td><td>

1.  Setup NAVA on latest track/bnowassist.
2.  Install 'Dynamic Translation for Virtual Agent' and the Spanish language plugins.
3.  Open the 'sys\_now\_assist\_deployment\_channel' table.
4.  Set 'experience' to 'Chat widget' for Service Portal.
5.  Navigate to **Conversation** &gt; **Settings/assistants**.
6.  Set the display experience to 'Standard' for Service Portal.
7.  Enable the language detect in **Conversation** &gt; **Settings** &gt; **Virtual-agent** &gt; **Parameters** &gt; **Ace-nav** &gt; **Virtual-agent**.
8.  Turn on Dynamic Translation in now-assist-admin/language-region.

 Notice that language detection doesn't work.

</td></tr><tr><td>

Virtual Agent

 PRB2035888

</td><td>

A Guardian-triggered async\_search early-return leaves a stale task ID in the context

</td><td>

The second utterance result becomes dropped.

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

 PRB2051719

</td><td>

Executing the topic from \_na\_max\_wait\_time\_ fails with an exception when transferred chat times out

</td><td>

An error message occurs and an exception appears in the logs.

</td><td>

1.  In Enhanced Chat, transfer to a live agent.
2.  As another agent user, accept the chat.
3.  Transfer the chat to another queue using the /tq quick action.
4.  Do not accept the chat and allow max wait time topic to trigger.
5.  When prompted, select the topic.

 Expected behavior: The topic executes successfully.

 Actual behavior: The message, 'I'm having technical issues and won't be able to continue this conversation' is shown and an exception is in the logs.

</td></tr><tr><td>

Virtual Agent

 PRB2052769

</td><td>

There's a 'sorry' message after a user tries to enter a different topic after a survey message

</td><td>

Users receive a 'sorry' error message when attempting to continue a conversation after the survey prompt appears, such as by asking a new question or creating an incident. The issue occurs because the survey handling logic incorrectly classifies non-feedback responses, causing the survey to be re-triggered and the conversation to terminate unexpectedly. This prevents users from completing their intended actions and causes the chat session to end unexpectedly.

</td><td>

1.  Enable the survey in Enhanced Chat.
2.  Run an agentic execution.
3.  After the survey is presented, continue the chat and ask something else.

Notice that the survey should not be shown again.

4.  Ask for a live agent.
5.  If the agent is not available and the incident option is shown, try to create an incident.

 Notice that it errors out and closes the conversation.

</td></tr><tr><td>

Virtual Agent

 PRB2057199

</td><td>

Follow-up questions from the APM Home **Ask Otto** button hangs indefinitely for the Q&amp;A agent

</td><td>

 

</td><td>

1.  Select the **Ask Otto** button \(ai-sparkle icon\).
2.  Notice that the greeting appears in NAP after ~12 seconds: 'Hello – I'm Enterprise Architecture Explorer for Analysis and Queries, and I'm ready to help...'
3.  Enter the following: 'list all capabilities associated with 'Deliver Services''.
4.  Hit **Enter**.

 Notice that the spinner appears briefly, then stops, and no response shown.

</td></tr><tr><td>

Virtual Agent

 PRB2058703

</td><td>

Generating a KB article throws an error

</td><td>

The following error appears: 'Configured callback URL for the KB generation topic is invalid.'

</td><td>

1.  Create an instance, following the documentation for setting up NextWave instances.
2.  Navigate to now-assist-admin.
3.  Make sure the KB Generation skill is active and the display for NAP\(OTTO\) channel is active.
4.  Give the prompt 'Create the KB for INCXXXXXXX' or 'Generate KB article'.

 Observe that there are three potential outcomes. First, the AI output could be: 'I wasn't able to generate the KB article because the configured callback URL for the KB generation topic is invalid'.

 Second, the AI output could be: 'I will help you create a knowledge article. Let me first retrieve the incident details to understand what information should be included in the KB'. Then the execution stops. It doesn't collect any information nor create any article. The error code is 200102.

 Finally, it might not use the KB Generation skill. Instead, it uses knowledge graph or basic reasoning to form a draft article in the NAP window.

</td></tr><tr><td>

Virtual Agent

 PRB2059089

</td><td>

The Otto session isn't aware of the logged-in user for 'assets managed by me' queries

</td><td>

The Otto/AICT chat session isn't aware of the logged-in user by default. When a user asks a question like 'Can you give me the assets managed by me?', the assistant returns the complete/unfiltered list of assets. Instead, it should apply a managed\_by = current user filter. The filter is only applied when the user explicitly names themselves in the query. The assistant should recognize 'me'/'my' references. It should automatically apply the logged-in session user's context without requiring explicit clarification.

</td><td>

1.  Log in as an AICT user.
2.  Ask Otto, 'Can you give me the assets managed by me?'.

Observe that the full/unfiltered asset list is returned instead of being filtered to the current user.

3.  Ask explicitly by name, for example: 'assets managed by username '.

 Observe that the managed\_by = current user filter is correctly applied.

</td></tr><tr><td>

Virtual Agent

 PRB2059128

</td><td>

In Language Detection, the loaded choices remain in the wrong language after switching from English to French via the Conversational catalog

</td><td>

When Language Detection is enabled, it automatically switches the conversation language from English to French after receiving 'Bonjour'. The user observes that the reference variable choices and loaded values appear in the wrong language \(English\) instead of French.

</td><td>

1.  Configure NextWave-Conversation-Server with Language Detection enabled.
2.  Set the Topic Block and Agent Execution priority, with Agent Execution higher priority.
3.  Use a conversational catalog item with a 'reference' variable type.
4.  Start the chat in the English profile/session language.
5.  Send the message 'Bonjour' to trigger Language Detection.
6.  Verify that the chat language switches to French.
7.  Wait for the French question to load \(with reference variable choices\).

 Observe the loaded choices for the reference variable.

</td></tr><tr><td>

Virtual Agent

 PRB2059632

</td><td>

BuildPolicyConfig should be aligned with sys\_now\_assist\_va\_persona\_detail schema

</td><td>

No policy configs are returned because buildPolicyConfig doesn't target sys\_now\_assist\_va\_persona\_detail and doesn't filter by persona\_detail\_type = Policy.

</td><td>

1.  Create an active record in sys\_now\_assist\_va\_persona\_detail:
    -   Deployment = a valid deployment sys\_id.
    -   Persona\_detail\_type = Policy.
    -   Name = Test Policy.
    -   Description = Test policy description.
    -   Prompt\_value = Test policy instruction.
2.  For the same deployment, create another active persona-detail record with persona\_detail\_type = Tone and prompt\_value = Friendly.
3.  Trigger the assistant-config handshake for that deployment via next wave.
4.  Inspect policyConfigs in the response.

 Expected behavior: One policy config entry is returned, containing the sys\_id, name, description, active, and instruction from the policy persona-detail record. Non-policy persona-detail records are excluded.

 Actual behavior: No policy configs are returned because buildPolicyConfig doesn't target sys\_now\_assist\_va\_persona\_detail and doesn't filter by persona\_detail\_type = Policy.

</td></tr><tr><td>

Virtual Agent

 PRB2060579

</td><td>

Link is broken for showing ticket details in the Otto chat

</td><td>

The URL is incorrect when the user selects the link in the card when using the Otto chat.

</td><td>

 

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

 PRB2062579

</td><td>

The OneApi/OneExtend 60-second execution timeout causes silent failures with no graceful error handling for users

</td><td>

When the OneExtend capability execution exceeds the 60-second Transaction.executeWithTimeout budget in FlowObjectExecutor.executeQuick, the platform cancels the transaction silently. The user receives no structured error response and the user sees the UI stuck with no feedback.

</td><td>

 

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

 PRB2065894

</td><td>

Topic slot filling sometimes does not work

</td><td>

 

</td><td>

1.  Open NAP.
2.  Ask, 'I want to order a coffee. Dark roast and hot.'

 Notice that it is still asking the user if it is hot or cold, when it should've been filled from the utterance.

</td></tr><tr><td>

Virtual Agent

 PRB2066077

</td><td>

Add the reduce\_items\_list\_polling toggle

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2066110

</td><td>

When ending the conversation, it moves the interaction to a 'Closed Abandoned' state without starting the conversation after creating it using CREATE\_CONVERSATION

</td><td>

The interaction moves to a 'Closed Abandoned' state instead of a 'Closed Complete' state.

</td><td>

1.  Create a conversation using the CREATE\_CONVERSATION action.
2.  Pass the context variables live\_agent only to 'true'.
3.  End the conversation using the END\_CONVERSATION action without starting the conversation

 Expected behavior: The interaction must move to 'Closed Complete' state.

 Actual behavior: It is moving to a 'Closed Abandoned' state.

</td></tr><tr><td>

Virtual Agent

 PRB2066112

</td><td>

UPDATE\_CONTEXT\_VARS is not working when used immediately after CREATE\_CONVERSATION

</td><td>

An error is thrown, and context variables must be updated with out any errors.

</td><td>

1.  Create a conversation using the CREATE\_CONVERSATION action.
2.  Try updating context variables using UPDATE\_CONTEXT\_VARS immediately after the creating conversation.

 Notice that it is throwing error.

</td></tr><tr><td>

Virtual Agent

 PRB2069447

</td><td>

Semantic filtering Virtual Agent global flags aren't set when invoked from AO via topic tool execution

</td><td>

 

</td><td>

1.  Start a NextWave conversation.
2.  Trigger sensitive detection for HR fallback.
3.  Select **Create case**.
4.  When prompted for a description on the case, provide the same utterance that triggers semantic detection.

 Expected behavior: It proceeds and creates a case.

 Actual behavior: The user utterance is flagged for semantic filtering.

</td></tr><tr><td>

Virtual Agent

 PRB2069651

</td><td>

The client hangs without feedback when exceptions are thrown in the OGCS layer during topic callback processing

</td><td>

Different exceptions throughout the flow must be caught and a feedback message has to be sent to client so that the client doesn't hang.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2069708

</td><td>

Users don't see logged in user details passed for DARE in skuld

</td><td>

 

</td><td>

From the Now Assist Portal, ask a simple question such as 'who am i'.

 Observe that it produces incorrect results along without passing user context.

</td></tr><tr><td>

Virtual Agent

 PRB2070048

</td><td>

There's an OGCS error on skillPicker due to bad sys\_gen\_ai\_skill data

</td><td>

 

</td><td>

1.  Add a sys\_gen\_ai\_skill record which doesn't have a valid skill\_document ID.
2.  Attempt to run a valid topic.

 Expected behavior: A topic should execute and log warning message that there's an invalid sys\_gen\_ai\_skill record.

 Actual behavior: A topic won't execute.

</td></tr><tr><td>

Virtual Agent

 PRB2070336

</td><td>

A guest user isn't able to upload images

</td><td>

Two issues prevent a guest user from uploading images: the conversation-server returns a 500 error due to a table level ACL on sys\_cs\_conversation and conversation-server returns a 401 error: 'unable to find guest session - Guest cookies are not passed through to upload request'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2072690

</td><td>

Support workspace tags derivation from workspace/page URL in DARE + KG

</td><td>

DARE and KG does not support workspace tags.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2073250

</td><td>

A conversation from another domain doesn't work if the user default domain doesn't have access to the current session domain

</td><td>

Whenever there is a hybrid queue into play, the worker impersonates the user and updates the session, but doesn't touch the domain. When impersonated normally, the domain will be the default domain for the user. This might no have access to the conversation because its started in a different domain. So whenever we read some data that is not accessible like conversation, the flow fails.

</td><td>

1.  Enable domain separation.
2.  Update any field on a user record.

Once updated, the default domain to the user moves to TOP/Default unless specified.

3.  Switch the domain to a different domain \(some sibling domain or a parent domain\).
4.  Start the conversation.

 Observe the responses would not be received for any query.

</td></tr><tr><td>

Virtual Agent

 PRB2073833

</td><td>

The AiAgentSecurityHelper lacks an API to create compound deny\_unless security-attribute ACLs, blocking sn\_voice\_aia from securing voice agent endpoints

</td><td>

There must be a gate for sn\_voice\_aia for certain voice agent endpoints behind a compound ACL using a custom security attribute with a deny\_unless decision policy. A compound ACL with deny\_unless requires setting 'decision\_type', 'local\_or\_existing', and 'security\_attribute' on sys\_security\_acl. Scoped apps cannot do this directly, and a global helper is required.

</td><td>

1.  Open an instance with com.sn.voice\_aia and com.glide.cs.genai installed.
2.  Attempt to configure a voice AI agent endpoint that requires compound ACL security, specifically an ACL using a custom security attribute with a deny\_unless decision policy.
3.  From the sn\_voice\_aia scope, call new AiAgentSecurityHelper\(\).createAclWithSecurityAttribute\(...\) to delegate compound ACL creation to the global helper.

 Expected behavior: sn\_voice\_aia should be able to delegate compound ACL creation to the global AiAgentSecurityHelper utility, the same as it does today for role-based ACLs via createAclAndRoles.

 Actual behavior: The method does not exist on AiAgentSecurityHelper. sn\_voice\_aia cannot create sys\_security\_acl records with compound security attributes directly from a scoped context.

</td></tr><tr><td>

Virtual Agent

 PRB2074044

</td><td>

Support 10 files and a total support of 50 MB for PDF native, PDF OCR, Word, PPTX, Excel, CSV, TXT, JPEG, PNG

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2074992

</td><td>

Handshake fails when duplicate preferred-skill entries exist for the same skill

</td><td>

An error message occurs and an exception is found in the logs.

</td><td>

1.  In Enhanced chat, transfer to a live agent.
2.  As another agent user, accept the chat.
3.  Transfer the chat to another queue using the /tq quick action. Do not accept the chat and allow max wait time topic to trigger.
4.  When prompted, select the topic.

 Expected behavior: The topic executes successfully.

 Actual behavior: The message, 'I'm having technical issues and won't be able to continue this conversation' is shown and an exception is in the logs.

</td></tr><tr><td>

Virtual Agent

 PRB2076214

</td><td>

A java.lang.NullPointerException occurs, 'Cannot invoke 'com.glide.script.GlideRecord.setValue\(String, Object\)' because 'gr' is null'

</td><td>

This issue was observed in hiprojectsc while investigating a ZTSD issue.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2076609

</td><td>

The 'Timeout conversations' job fails to close conversations on cross domains

</td><td>

 

</td><td>

1.  Enable domain separation.
2.  Check the Nextwave service user domain.
3.  Make any update on the user if needed so that the domain gets changed to TOP/Default.
4.  Start a conversation and run a topic.

 Observe that it fails.

</td></tr><tr><td>

Virtual Agent

 PRB2077222

</td><td>

An issue in the fallback logic for a re-witten query in SearchAndRerankProcessor

</td><td>

This results in the conversation erroring out.

</td><td>

1.  Open a zurichcqemonthly10 instance.
2.  Impersonate a user.
3.  Open NAP.
4.  Send 'Summarize CS0000871'.

 Notice that the conversation errors out.

</td></tr><tr><td>

Virtual Agent

 PRB2078011

</td><td>

The Virtual Agent greeting is not showing, or shows the wrong message, when the system language is non-English

</td><td>

The session saved in English is shown instead of saving and showing the greeting message created in the Japanese session.

</td><td>

1.  Set glide.sys.language to 'ja'.
2.  Open VA assistant.
3.  Update the message to something that is not base instance.
4.  In the English session, test the assistant.

Notice that no message is shown.

5.  Switch to a Japanese session and save any greeting message.
6.  In the Japanese session, test the assistant.

 Observe that the message saved in the English session was shown.

</td></tr><tr><td>

Virtual Agent

 PRB2078683

</td><td>

The Topic execution is not working if the Nextwave user is in the TOP/Default scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2081066

</td><td>

The page-not-found issue occurs with all apps and instances

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2083220

</td><td>

setCache is not honoring the **Domain** field

</td><td>

This issue occurs when impersonating the actual user.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2065785

</td><td>

The client sends uiMetadata as 'null' when selecting the 'Stop' button after a page refresh during a Dynamic Loader message

</td><td>

When a Dynamic Loader message arrives and the page is refreshed while it's still loading, selecting the 'Stop' button after reloading sends a stop\_flow action message with 'uiMetadata: null' instead of the expected contextual action metadata.

</td><td>

1.  Start a chat session.
2.  Trigger a flow/skill that sends a Dynamic Loader message.
3.  While the loader is still in progress \(before it resolves/completes\), refresh the page.
4.  Wait for the session to restore and the loading state to reappear.
5.  Select the **Stop** button.
6.  Inspect the outgoing message for the stop\_flow action.

 Expected behavior: richControl.uiMetadata should contain the contextual action metadata.

 Actual behavior: richControl.uiMetadata is null.

</td></tr><tr><td>

Visual Task Boards

 PRB2059581

</td><td>

Users are unable to move a card from one visual task board \(VTB\) to another after an Australia upgrade

</td><td>

The 'Move' dialog does not display any swimlanes.

</td><td>

1.  Set the system property glide.invalid\_query.returns\_no\_rows to 'true'.
2.  Create two Task Boards:
    -   Board A with at least one card
    -   Board B with two or more lanes
3.  Open a card on Board A and select **Move**.
4.  In the dialog, select **Board B** as the target Task Board.
5.  Select the **Lane** field and search.

 Observe that the dropdown list displays 'No matches found', even though Board B has valid lanes.

</td></tr><tr><td>

Work Order Management

 PRB2066103

</td><td>

Fix the getLocation API on FSMGeneralUtil and unit tests

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB2073259

</td><td>

Epic for glide changes for Rest connector

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Zero Trust Access

 PRB2052933

</td><td>

Users are unable to maintain session roles when accessing the VTB dashboard

</td><td>

This issue occurs when an instance has ZTA policies configured with IDP Attributes filter condition used in the Adaptive Authentication policy condition, for any user who access the VTB dashboard with the filter, filterLIKEjavascript^ORfilterLIKEDYNAMIC', and if there is no channel responder record created for it yet. The flow receives an NPE \(NullPointerException\), and the roles in the session are not loaded properly. There are no roles for the user causing the user to see the 'Security Restricts Access Prevention' message on screen.

</td><td>

1.  Ensure the instance has Zero Trust Access \(ZTA\) configured with at least one active Adaptive Authentication policy.
2.  Log in to the instance as any non-admin user.
3.  Navigate to any Visual Task Board \(VTB\) dashboard that contains a board filter matching.
4.  Confirm that no channel responder record exists for this filter combination.
5.  Load/open the VTB dashboard.

 Notice the 'Security Restricts Access Prevention' message occurs.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 5 W36](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3153999)
-   [Australia Patch 5 W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3153999)
-   [Australia Patch 5 W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152205)
-   [Australia Patch 5 W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150411)
-   [Australia Patch 5 W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147913)
-   [Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-5.md)
-   [Australia Patch 4 Hotfix 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4-hf-4-PO.md)
-   [Australia Patch 4 Hotfix 3 W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152202)
-   [Australia Patch 4 Hotfix 3 W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150410)
-   [Australia Patch 4 Hotfix 3 W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3148119)
-   [Australia Patch 4 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146432)
-   [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-4.md)
-   [Australia Patch 3 Hotfix 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3-hf-4-PO.md)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-3.md)
-   [Australia Patch 2 Hottfix 5b W36](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3153994)
-   [Australia Patch 2 Hotfix 5b](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2-hf-5b-PO.md)
-   [Australia Patch 2 Hotfix 5a W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152198)
-   [Australia Patch 2 Hotfix 5a W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150405)
-   [Australia Patch 2 Hotfix 5a W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147911)
-   [Australia Patch 2 Hotfix 5a W32](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146424)
-   [Australia Patch 2 Hotfix 4b W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152197)
-   [Australia Patch 2 Hotfix 4b W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150406)
-   [Australia Patch 2 Hotfix 4b W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147912)
-   [Australia Patch 2 Hotfix 4b W32](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146425)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/available-versions.md)


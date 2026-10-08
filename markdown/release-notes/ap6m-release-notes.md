---
title: Australia Patch 6m
description: The Australia Patch 6m release contains important problem fixes via Australia Patch 6 and updates to compatible ServiceNow Store applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/ap6m-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-09-25"
reading_time_minutes: 417
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 6m

The Australia Patch 6m release contains important problem fixes via Australia Patch 6 and updates to compatible ServiceNow Store applications.

-   **Australia Patch 6m was released on September 25, 2026.**
    -   Build date: 09-23-2026\_1551
    -   Build tag: glide-australia-02-11-2026\_\_patch6m-09-10-2026

## Monthly "m" releases

Monthly "m" releases are now available for your ServiceNow AI Platform® instances. These releases, which are identified by an "m" in the release name, contain everything from the base family patches, the latest version of all AI applications, and those apps' supporting non-AI application dependencies.

**Important:** This ServiceNow® release is not available for ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in the Australia Patch 6m release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A06m.00.xlsx).

Australia Patch 6m includes 683 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-ap6.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Australia Patch 6 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 6, refer to [KB3159480](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3159480).

## Changes in Australia Patch 6

-   ****

    Live Connect provides read-only access to your ServiceNow tables, allowing you to write SQL queries, create reports, and perform analysis while maintaining your existing security controls. This eliminates the need for data synchronization and ensures you work with current ServiceNow data.

-   **[Activate or deactivate a Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/activate-stream-producer.md)**

    Activate a Stream Producer configuration to begin capturing and streaming table changes to your Kafka topic. You can deactivate it at any time to stop streaming changes. When you deactivate a producer, any unprocessed messages in the CDC queue are discarded.

-   ****
-   ****

    Configure the JDBC driver to connect to your ServiceNow instance and query your data.

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

    Use the installation wizard to install the ODBC driver and configure the connection between your Business Intelligence tools and ServiceNow data.

-   ****

    Configure ServiceNow Live Connect drivers to connect with third-party business intelligence and database tools for direct data access and analysis.

-   ****

    Live Connect provides secure, read-only access to ServiceNow data for external BI platforms via industry-standard database APIs, while maintaining all existing security policies and role-based restrictions.

-   ****

    Live Connect supports business intelligence \(BI\) reporting, ad-hoc data analysis, and custom report development.

-   ****
-   ****

    Use Interactive SQL to verify that the ODBC driver connects to your ServiceNow instance and returns query results.

-   ****
-   ****

    This section provides details about Live Connect reference information like minimum requirements and usage limitations.

-   ****

    This section lists the minimum supported versions for ServiceNow server releases, client drivers \(ODBC and JDBC\), and Java Development Kit required for Live Connect.

-   ****
-   ****

    Common SQL functions used in Live Connect for querying and analyzing incident data.

-   **[Integration Hub plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/ih-plugins.md)**

    ServiceNow Stream Producer \[com.glide.hub.stream\_connect.stream\_producer\]: Enables Stream Producer to automatically stream changes from ServiceNow tables to Kafka topics.

-   **[Using Stream Connect for Apache Kafka](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/stream-connect-apache-kafka.md)**

    Automatically stream changes from ServiceNow tables to Kafka topics with Stream Producer.

-   **[Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/stream-producer.md)**

    Stream Producer enables you to automatically stream changes from ServiceNow tables to Kafka topics using change data capture \(CDC\), eliminating the need for custom scripts or business rules.

-   **[Create a Stream Producer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/create-stream-producer.md)**

    Create a Stream Producer configuration to automatically stream table changes to a Kafka topic. You can specify which table to monitor, which change events to capture, which fields to include, and configure keys and headers for routing and tracking.

-   **[Monitor and optimize Stream Producer performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/monitor-sc-performance.md)**

    Monitor Stream Producer performance metrics and change data capture \(CDC\) queue health to identify bottlenecks and optimize for your deployment scale and throughput requirements.

-   **[Schema management in Stream Connect](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/schema-management.md)**

    When you create or update a Stream Producer record with the serialization format set to Avro, ServiceNow automatically generates and maintains an Avro schema for the associated table.

    Stream Producer schemas are stored across two tables in the ServiceNow IntegrationHub Stream Connect Schema \[`com.glide.hub.stream_connect.schema`\] plugin. These tables are read-only for all users. No one has create, update, or delete access.

    You can also configure a Stream Producer to send messages in an Avro format. When the serialization format is set to Avro, the Stream Producer uses the auto-generated schema for the selected table to convert CDC payloads to Avro before sending them to Kafka.

    The Schema Registry REST API exposes your Stream Producer Avro schemas to external systems and consumers. External applications can use the API to retrieve schemas and decode Avro-encoded messages received from Kafka topics.

    Stream Producer schema evolution features.

-   **[Human-assisted SMS OTP authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/human-assisted-sms-otp.md)**

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

AI Agents

 PRB2088066

</td><td>

The AI Agent Studio home page link is broken and the page is not rendered, and the error message 'Core scripts failed to load' occurs on the page

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Home**.

 Observe that the URL which is generated '/aiux/aia/home' is broken and gives error 'Core scripts failed to load. Check your internet connection'.

</td></tr><tr><td>

AI Agents

 PRB2088127

</td><td>

The user is unable to change the model provider from AI Agent to NowLLM

</td><td>

In GCC, NAA currently prevents users from switching from Al Agents to NowLLM with an error that Al Agent is not supported with NowLLM.

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

AI Search \(Glide\)

 PRB2089496

</td><td>

The 'Book a meeting' Now Assist Virtual Agent \(NAVA\) test case is not working

</td><td>

The Now Assist skill discovery silently returns no sys\_gen\_ai\_skill results, even though while the same prompt works on previous versions. This issue is caused by stale AI Search index data. Upgrading the instance changes code but does not re-ingest existing documents, so the new filter matches zero documents, and the skill disappears from discovery with no error. Any record created or edited after the upgrade is re-ingested under the new converter and self-heals, so only untouched records vanish.

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

Dynamic Guidance

 PRB2089484

</td><td>

The genai\_admin role is incorrectly inherited by all ITIL users

</td><td>

 

</td><td>

1.  Upgrade the instance.
2.  Log in to the instance.
3.  Open the genai\_admin role.

 Notice that this role is now assigned to all users with the ITIL role.

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

GlideAggregate API

 PRB2090884

</td><td>

For non-admin callers, the **Aggregate/Stats API** field validation conflates 'field doesn't exist' with 'field exists but read-ACL denies it'

</td><td>

When a non-admin caller queries the Aggregate/Stats API \(/api/now/stats/\{table\}\) using sysparm\_min\_fields, sysparm\_max\_fields, sysparm\_avg\_fields, or sysparm\_sum\_fields, the API now incorrectly rejects fields the caller isn't allowed to read as if those fields didn't exist at all. A new validation step was added to close an unauthenticated XSS hole, as the field name was reflected unescaped into the XML response. To close that hole, the fix checks each requested field against the table's field dictionary using GlideRecordSecure.isValidField\(\). The problem is that GlideRecordSecure's underlying get\(\) is ACL-aware: it returns null for a field the caller lacks read access to, exactly the same thing it returns for a field that doesn't exist. isValidField\(\) can't tell the two apart, so a perfectly real field that the caller just isn't allowed to read gets reported as 'Invalid &lt;param&gt; parameter' - the same 400 error a user sees for typing a field name incorrectly. As a result, any non-admin identity that has a legitimate field-level ACL restriction on one of the fields it requests now gets a hard failure instead of the normal ACL behavior it used to get. An admin account \(or any role with read access to that field\) sees no difference at all, since it can read everything - which is what makes this look like a permissions issue rather than a validation bug.

</td><td>

1.  Pick any table \('T'\) with a field \('F'\) that has a field-level read ACL restricting a non-admin role.
2.  As the non-admin identity, get /api/now/table/T?sysparm\_fields=F,sys\_id&amp;sysparm\_limit=1 and confirm F is absent or blanked in the response.
3.  As the same non-admin identity, call: GET /api/now/stats/T?sysparm\_max\_fields=F.

 Expected behavior: Either a normal aggregate result with F omitted/blank, or a proper ACL-style denial.

 Actual behavior: HTTP 400, 'Invalid sysparm\_max\_fields parameter' - reported identically to what a user would see for a field name that doesn't exist on T at all.

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

Now Assist in Virtual Agent

 PRB2087138

</td><td>

The user is unable to activate the ServiceNow Otto Platform under 'Assistants', as there is no option to add the Unified Navigation App Shell entry on the Display Experience for GCC/NSC Fresh instances

</td><td>

 

</td><td>

1.  Navigate to **Conversational Interface** &gt; **Assistant** &gt; **ServiceNow Otto Panel-Platform**.
2.  Select **Edit**.
3.  Open the 'Display Experience' page.

 Observed that the user is being asked to add one Display Experience on the 'Display Experience' page, however there is no option to add the Unified Navigation App Shell entry to activate the **Now Assist panel \(NAP\)** icon on the instance home page.

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

On-Call Scheduling

 PRB2088799

</td><td>

On-call UI components for the Configurable Workspaces \(sn\_uib\_on\_call \) app fails to upgrade to version 9.4.2

</td><td>

 

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

Roles

 PRB2086590

</td><td>

Non-admin users were not able to view the **Manager** field because there is a read ACL on sys\_user.manager which requires the sn\_hs\_csc.contractor role. However, when trying to add this role to any user, it conflicts with the snc\_internal role

</td><td>

 

</td><td>

 

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
</table>## Fixes included in Australia Patch 6

These prior versions contain PRB fixes that are also included with Australia Patch 6. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 5 W36](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3153999)
-   [Australia Patch 5 W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3153999)
-   [Australia Patch 5 W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152205)
-   [Australia Patch 5 W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150411)
-   [Australia Patch 5 W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147913)
-   [Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-5.md)
-   [Australia Patch 4 Hotfix 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4-hf-4-PO.md)
-   [Australia Patch 4 Hotfix 3 W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152202)
-   [Australia Patch 4 Hotfix 3 W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150410)
-   [Australia Patch 4 Hotfix 3 W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3148119)
-   [Australia Patch 4 Hotfix 3](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146432)
-   [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4.md)
-   [Australia Patch 3 Hotfix 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-3-hf-4-PO.md)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-3.md)
-   [Australia Patch 2 Hottfix 5b W36](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3153994)
-   [Australia Patch 2 Hotfix 5b](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-2-hf-5b-PO.md)
-   [Australia Patch 2 Hotfix 5a W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152198)
-   [Australia Patch 2 Hotfix 5a W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150405)
-   [Australia Patch 2 Hotfix 5a W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147911)
-   [Australia Patch 2 Hotfix 5a W32](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146424)
-   [Australia Patch 2 Hotfix 4b W35](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152197)
-   [Australia Patch 2 Hotfix 4b W34](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3150406)
-   [Australia Patch 2 Hotfix 4b W33](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3147912)
-   [Australia Patch 2 Hotfix 4b W32](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3146425)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

## Store app versions included in Australia Patch 6m

|App name|Version number|Release notes|
|--------|--------------|-------------|
|@servicenow/sn-ai-engagement-experience|3.6.4|New: Fulfillers can now edit AI response outputs directly within the contextual side panel before posting. This enables more accurate replies, improves AI learning through memory, and provides greater control beyond simply accepting or rejecting outputs in the 'Ready for Review' state. Fixed: Agent-sent messages now render hyperlinks correctly and honor line breaks in the UI. Agentic Workflow notifications are now delivered correctly — resolved a misconfiguration of 'include\_originator' that was causing self-notification exclusion. AIEX now correctly respects the sessionContext prop when launched independently of the AIEL launcher.|
|@servicenow/sn-enhanced-content-editor|31.26.1|Editor features|
|Accounts Payable Invoice Processing|13.2.7|Fixed critical defects and addressed reported bugs to improve system stability and user experience|
|Accounts Payable Operations integration with Document Intelligence|13.2.5|This release includes fixes for reported defects to improve product stability.|
|Admin Experience for Hardware Asset Management|1.0.0|This release introduces an application installation option on the Admin Home page through Product Hub, along with a Configuration console for setting up the Hardware Asset Management application, helping streamline implementation: Hardware Asset Management Product Hub provides a central place to install, view, and manage all applications included in your subscription. Hardware Asset Management Configuration Console simplifies setup by bringing all Hardware Asset Management settings into one location. You can also use the Implementation agent conversational interface to configure some of the settings|
|Advanced Approval Management|2.6.0|Defect fixes|
|Advanced Approval Management AI|1.2.2|New Delta between quote versions support adding adhoc approvals Approval step and condition details|
|Advanced Response Automation for Smart assessments|23.0.2|Changed: Internal change only. The ResponseAutomationUtilsSNC script include is now accessible from all application scopes.|
|Advanced Work Assignment for Supplier Lifecycle Operations|10.0.0|Changed Migration of code to Fluent|
|Agency Support Model|4.0.1|New Public sector terminology and constituent-centric lookup in interaction pages. All interaction pages \(email, voice, chat\) now display public sector terminology, replacing commercial terms such as 'consumer' with 'constituent', 'contact' with 'business contact', and 'account' with 'business'. Lookup functionality now queries constituent records, ensuring caseworkers retrieve accurate public sector data. L3 compliance support for app-psds-agency. The app-psds-agency now supports Level 3 compliance, enabling agencies to meet advanced regulatory requirements. Fluent framework adoption for app-psds-agency. The app-psds-agency interface has been converted to use the Fluent design system, providing a consistent and accessible user experience. Configurable dictionary emission in now-sdk build. The now-sdk build for app-psds-agency now supports the \`--emitDictionary=false\` parameter, allowing admins to control dictionary file generation during builds. Changed Localization and translation improvements across core bundle. Client scripts and widgets have been updated to resolve localization text warnings, ensuring all message keys are correctly preloaded and literal strings are properly extracted for translation. Button labels and stylized text now display consistently in all supported languages. Fixed The extensible financial details table now correctly handles child tables despite lacking a class name column. Table structure issues affecting extensibility have been resolved.|
|Agent Client Collector for Investigation|9.4.2|View the metrics relevant to the incident and CI in the context of the incident for Investigation Get latest metrics and data on-demand from within investigation Visibility for when metrics exceed pre-set warning and critical threshold levels Includes support for remedial action playbooks Link into DEX console while investigating a CI \(requires separate DEX entitlement\)|
|Agent Client Collector for Visibility Content|2.0.4|New: 1. License Key Discovery : File Based Discovery Approach FBD License files scan approach aims to enhance the capability by enabling automated discovery and scanning of FBD license files. This will help users identify and manage license keys efficiently, reducing manual effort and minimizing compliance risks. 2. The agent now detects software from running processes across Windows, Mac, and Linux, surfacing applications that installation-based scans don't catch. Changed: 1. Improved Software Last Used Tracking accuracy for Windows applications \[Auto-start applications and File-association-launched applications\]|
|Agent Client Collector Framework|7.0.4|New: Maintenance Token Protection for Windows Uninstalls Implement a maintenance token system that protects ACC \(Agent Client Collector\) agents from unauthorized or accidental uninstallation on Windows. Administrators must now generate and provide a unique, agent-specific token before allowing agent uninstallation, adding a critical security layer to large-scale deployments while maintaining offline functionality and audit trails. ACC-F now provides official support for non-persistent Virtual Desktop Infrastructure \(VDI\) environments. Customers deploying agents to VDI gold images can now achieve full operational capability in under 2 minutes instead of 15–20 minutes with traditional instance push workflows. Prevented duplicate agent registrations on gold-image VM re-creation. Eliminated per-desktop TLS certificate generation for VDIs. Enabled immediate check execution upon instance connection Changes: Randomized temporary directory creation during agent upgrade to prevent symlink attacks Restricted command allow-list defaults to prevent privilege escalation Optimized policy refresh to prevent memory exhaustion by processing agents in batches \(2× max\_agents\_per\_mid, 20,000 default\) with automatic rotation Added post-upgrade sync hook to re-publish asset metadata to all active MIDs after ACC-F plugin upgrades Reordered Windows host IP selection to prioritize default-gateway interface query over generic routing Added explicit "check skipped" log entries to distinguish disabled checks from normal execution Extended policy publishing logic to support custom CI table inheritance \(u\_cmdb\_ci\_\*\) Implemented scheduled cleanup job for stale checks to auto-resolve associated error records Modified policy publish logic to update-in-place instead of delete/recreate Added detection and fix for corrupted agent\_now\_id files on ICS agent startup Added JSON5 support for allowlist parsing on ACC Updated WMI Permissions test to work on Windows 11 where wmic.exe was removed Fixed: Fixed config file sync for checks with no assets by resolving "no agent record on context" error Fixed re-registration save file format for ICS agents Out-of-memory crashes on policy push when 80K+ agents accumulated on single MID. installed\_software module hang on RHEL 10 when RPM output exceeds 64KB pipe buffer limit Asset metadata not re-synced after ACC-F plugin upgrade, breaking asset collection on MIDs Successful agent upgrade showing misleading "failed to fully fetch log" error message Windows multi-homed hosts registering with incorrect IP due to wrong interface selection ARM64 Linux CPU discovery failure when osquery CPU data unavailable Disabled checks logged as "running successfully," masking data collection outages with false health indicators Test Check UI crash/hang when agent table exceeds 28,000 records Agent crash on YAML parsing failures during initialization Policy deactivation success notification wiped by page auto-refresh Policy republish losing change history by deleting/recreating records instead of updating All agents for a particular ICS instance moving to "Unknown" state unable to transition to "down" "Clean up duplicate agent ID errors" job running indefinitely on large error volumes, consuming database resources|
|AI Admin Center|6.0.7|Agent Advisor UI enhancements improve opportunity resolution and filtering. Automation Opportunity page experience enhancements. Agent miner data set supports removal of custom data sets. Daily recommendation feature removed from Agent Advisor. Multiple cost profiles support removed; only a single cost profile is available.|
|AI Admin Hub|10.3.4|New Admins can now integrate new domain separation APIs for Data Overflow processing, enabling improved data management across domains. Changed Edited NASK skills where model providers are not switched are now displayed in the "non impacted skills" section, and admins can switch model providers directly from NASK. The Prompt Injection and Offensiveness Protection pages have been optimized to load in under 4 seconds, improving user experience. Skill List performance has been improved by removing the Skills Need Attention modal and optimizing the skill pruning process for regulated instances.|
|AI Agent Advisor|1.4.5|New Limited Availability: Detect customer intents from the Intent Library and add new intents to automation opportunities as agents are created. Limited Availability: View AI Agent Advisor recommendations directly within AI Agent Studio, surfacing relevant automation opportunities during agent building. Changed Added new error types across the mining pipeline, with configuration and pipeline execution UI enhancements for clearer visibility into run status. Fixed Resolved multiple front-end defects affecting configuration screens and pipeline execution views. Removed Nothing removed in this release.|
|AI Agents for AIOps|1.12.3|New Alert Verification AI Agent automates alert closure based on related incidents and knowledge articles. Integration Management Agent enables conversational setup and lifecycle management for top pull connectors. Express List UI enhancements for alert closure. Comprehensive logging and status tracking for alert verification workflow. Integration source tracking for connector creation. Credential creation within conversational setup. Framework for generating and associating integration setup KB articles. Advanced KB search and summarization for alert investigation. New API endpoint to trigger integration sync jobs. \* \*\*Option to install integrations with Otto from integration launchpad. Changed Closure UI enhancements for auditability and user experience.\* Worknotes formatting improved for alert closure. Assignment group handling toggle implemented.|
|AI Agents for Customer Success Management|2.7.21|AI Agent for AI Insights FLuent conversion of App|
|AI Agents for Discovery|3.2.2|Fixed Security defects in the Certificate Management Renewal AI Agent have been resolved.|
|AI Agents for Enterprise|1.0.1|New Initial release of AI Agents for Enterprise. Added a Model Category Skill that populates missing Model Category values for staged import records based on available model information. Added a Model Classification Skill that selects the classification that best suits the model from the available classification codes selected by the user. Added AI-assisted enrichment of staged model records during the Preview and Import process.|
|AI Agents for Health Log Analytics|2.5.0|Changed Internal naming conventions have been updated for improved consistency across the product.|
|AI Agents for HR Service Delivery|7.3.1|--- AI Generated Release Notes --- New HR L1 AI Specialist can now predict and transfer HR cases based on high-confidence AI and LLM predictions. Cases are automatically transferred to the predicted HR Service when confidence exceeds the threshold, and worknotes are updated with recommendations. If confidence is low, the specialist continues resolution and logs recommendations. Admins can configure automatic case transfer and prediction thresholds. The "Classify and Assign" section now allows configuration of fields to predict and the confidence threshold for automatic transfer. HR L1 AI Specialist uses indexed sources for service prediction. Predictions leverage both HR Cases and HR Service as indexed sources, improving accuracy and coverage. LLM prompt-based prediction is now supported. The system implements LLM prompts for skill-based and script-based predictions, enhancing the AI Specialist's ability to recommend services. Search Application for HR AIS Search Config is available. HR L1 AI Specialists can test search sources on HR Service and HR Case, ensuring accurate configuration and results. Unified Feature Flag Rollout Strategy enables controlled activation of AI Specialist features. Admins can manage feature availability for HR L1 AI Specialist and its template, with sandbox testing and sequencing for customer rollout. Golden data evaluation for prediction and transfer is established. Prediction accuracy is measured using curated datasets, with ongoing evaluation and tuning for best results. Model proxy for Azure OpenAI endpoints is implemented for evals. The eval suite now supports a local proxy for Azure OpenAI, enabling tool\_calls and matrix-based client/model selection without direct Azure access. Automation of Zero Touch Service Desk \(ZTSD\) functional flow is introduced. The ZTSD workflow is now automated, streamlining case handling. Changed Prediction prompts and logic have been fine-tuned for clarity and accuracy. Users experience improved guidance and outcomes from prediction features, with enhanced prompt generation and evaluation logic. Transfer flow is modularized and worknotes are updated with AI fields. After transfer, the ZTSD flow stops on the current case, and worknotes reflect AI-driven updates. Classify and Assign UI and configurations have been revisited and aligned with ITSM templates. Unused UI variables are removed, writeRoles and readRoles are updated for relevant configurations, and dropdowns now restrict selection to HR Service only. The autosubmitcatalog configuration is implemented, and automaticcasetransfer defaults to false. Testing environments for DARE and predict/transfer functionality are validated. Test results are available for both DARE and prediction/transfer workflows. Fixed Predict Services and Transfer HR Case workflow has been corrected to no longer prompt users for sys\_id input when the HR Case number is already provided.|
|AI Agents for ITAM|5.0.0|This version bundles Contract Management Pro features into the Hardware Asset Workspace for Hardware Asset Management Prime subscribers. Common contract-related functionalities are now accessible directly from your asset records \(requires Contract Management Pro to be installed\).|
|AI Agents for Meetings|1.0.10|1. Touchpoint Conversations Brief, Builder skill, Transcript skill for Post meeting and Premeeting preperation skill with recorring meetings and TOuchpoint details.|
|AI Agents for Retail Service Management|1.6.0|Fixed: Internal conversion.|
|AI agents for SLO|2.2.2|New SLO Creator Agent now supports commitment-aware SLO generation and integrated risk calculation. The SLO Creator Agent operates with updated V2 instructions, enabling new skills for generating SLOs that account for commitments and utilizing a risk calculation tool. The implementation aligns with the SLO Gap Agent to ensure consistent behavior and parity.|
|AI Agents for Telecommunications, Media and Technology|6.2.1|Maintenance only|
|AI Agents for Universal Request|1.1.3|This release contains no functional changes, code modifications, or new features. The version number has been incremented to maintain alignment with the September release schedule. All existing functionality remains unchanged and fully compatible with previous versions. This update is primarily administrative|
|AI Analytics|5.3.5|New Assist consumption analytics: Monitor entitlement health, consumption trends, and top-consuming AI assets from a consolidated analytics view. Enhanced performance analytics: Analyse skills, assistants, and agents through overview dashboards and detailed performance views with advanced filtering and date selection. Skill analytics enhancements: Filter skills by type and product, and access detailed usage, adoption, feedback, and AI Guardian insights. Agent analytics: View agent performance metrics, drill into individual agent details, and track AI resolution rates. Voice analytics insights: Analyse intent performance, resolution outcomes, guest authentication trends, tool execution trends, and CSAT trends. Changed Performance Explorer renamed to Performance across analytics experiences. Resolution metrics updated to provide intent-based session outcomes and improved visibility into AI and live-agent resolution results. Voice analytics overview redesigned with key call outcome metrics surfaced prominently and additional trend visualisations. Analytics dashboards refreshed with updated layouts, filtering, navigation, and reporting experiences for greater consistency and usability. Fixed None. Removed Legacy Voice Assistant overview metrics removed, including several older conversation, transfer, CSAT, handle-duration, and trend-based visualisations that have been replaced by the new analytics experience.|
|AI Asset Management|6.1.2|What's new Domain separation for lifecycle work items – Users now see only lifecycle requests and tasks within their current domain and child domains in Activity Center and Home views. Onboarding Playbook with dynamic, risk-based execution – Streamline lifecycle task management with intelligent playbook-driven onboarding. What's fixed Rejection comments now display correctly on AI Systems when an asset is rejected. Status updates during asset rejection are now consistent—rejected change and offboarding requests automatically set to 'Canceled' state.|
|AI Authoring for Catalog Builder|8.0.3|What's New Generate client scripts with AI Describe the behavior you want for a catalog item in plain language, and ServiceNow Otto generates the right automation for you — in case of Catalog Client Script — no coding required. AI-assisted question containers Describe how you'd like your catalog item's questions organized — for example, a two-column container with a title — and ServiceNow Otto builds the container, sets its layout, and places the questions for you. Enhancements Improved usage insights for AI-assisted catalog generation Expanded analytics now give administrators clearer visibility into how AI authoring is being used across their catalog, including generation outcomes and knowledge-base suggestion activity — supporting better adoption tracking and reporting.|
|AI Case Management|23.0.2|Changed Smart Assessment demo templates to support the Question Bank data model, including Question Bank entity types, question-level states, cross-Question Bank imports, and Question Bank-specific category roles. This ensures shipped demo templates and data remain compatible with August 2026 initialization and upgrade scenarios. Fixed Security fixes|
|AI Control Tower|7.1.1|AI Control Tower adds new capabilities across discovery, governance, security, monitoring, and measurement of AI usage. Inventory and Discovery Detect unsanctioned AI use with network detection \(Armis\) and endpoint detection \(ITOM ACC\), including model, user, department, and device details. Block AI services detected through ACC. An AI Inventory Enrichment Agent scans your inventory for incomplete records and suggests values to fill the gaps. New and enhanced connectors extend discovery to Microsoft Agent365, Azure AI Foundry, Copilot, and AWS. Govern Discovered AI systems are now risk-classified at the point of discovery, before they enter the managed workflow. An AI Risk &amp; Control Applicability Advisor recommends the most relevant risks and controls for each system, with rationale. Dynamic Playbook 2.0 tailors onboarding tasks to an asset's risk classification. ServiceNow-managed AI agents can now be published to Microsoft Agent365 and other external registries. Secure AI agent containment can be triggered automatically based on authored policies in the AI Control Tower, removing the need for manual intervention. Support is extended to Azure AI Foundry for agent runtime and Gemini Enterprise Agent Platform \(via Okta integration\). Design-time security now covers AI agents, tools, MCP servers, and system prompts, not just AI models. The Veza connector now uses OAuth 2.0 for authentication. Monitor Configure trace data retention to fit your needs. View new latency and token-usage visualizations. Set evaluation metrics at the asset level. Use custom date ranges of up to 18 months for evaluation data. Measure Product owners can now view and work with just the AI systems and metrics that matter to them. Foundations Domain separation is available across AI Control Tower, enabling MSP and multi-tenant deployments with isolated inventories, security posture, and value data for each tenant. For full details, see AI Control Tower release notes.|
|AI Control Tower Core|8.5.7|see release notes for AI Control Tower|
|AI Control Tower - Evaluations|4.0.1|New Admins can now configure trace data retention and access policies. Customers can set retention preferences for sessions, traces, spans, prompts, and outputs, choosing between auto-deletion after one day or configurable retention periods. The UI provides radio button selection and confirmation messaging for retention settings. Monitor dashboard now displays new data visualizations for agent traces. Users can view latency over time via a line graph, average latency and runtime tokens tiles, and average total spans across all dashboards. These visualizations are available on the asset record's Monitoring tab. Support for domain separation across Monitor and Evaluations. Domain context is now applied to API keys, provisioning controller calls, metric writes and reads, and evaluated session lists. Domain columns and separation guidance are displayed in relevant UI areas, and domain-scoped configuration is used for incoming sessions and metrics. Admins can configure metrics at the asset level for both Product Owner and AI Steward roles. Global metrics can be disabled for specific AI systems, asset-specific metrics can be enabled or disabled, and sample rates can be edited. Bulk operations and override management are supported. Custom date picker added to Monitor and asset-level pages. Users can select custom date ranges up to 18 months for evaluation data, with validation and consistent behavior across pages. Generic API introduced for accessing session, trace, and span tables. End-to-end testing confirms API coverage and reliability. Asset-specific metric management enhanced with new list view and side panel. Admins can add, remove, and edit asset-specific metric overrides, including sample rate adjustments and confirmation modals for metric removal. Domain fields established for session, trace, span, and trace-system records. Domain scoping ensures records are visible to users in their domain regardless of creation route. Span count field added to session records. The span count is calculated as the sum of spans in traces belonging to each session. Score explanation panels now show per-metric evaluation counts. The panel surfaces bias indicators when evaluation coverage is imbalanced, improving score transparency for Quality and Safety metrics. Changed Evaluated session UI experience adapts to retention settings. When "Don't keep traces" is selected, evaluated sessions and traces are hidden from Monitor and asset-level dashboards. Provisioning controller and metric group APIs now use domain context. Asset and metric-group requests include domain identifiers, ensuring domain uniqueness and correct scoring group resolution. Valk metric writes and reads are now domain-scoped. Metrics include domain attributes, and queries are filtered to the user's visible domains. Latency and spans metrics are displayed in session detail headers and evaluated sessions lists. Columns for latency \(ms\) and spans are added to relevant tables. Warning modal shown when excluding global metrics or removing metric overrides. The modal lists affected templates and controls, with redirect URLs and operation revoke options. Exception AI Systems column added to Evaluation Metrics Table. The table now displays exceptions for global evaluation metrics. Domain columns are displayed in evaluated session lists when domain separation is enabled. Score calculation detail panel improved with evaluation count and bias indicator. The panel now highlights when scores are skewed due to uneven metric evaluation coverage.|
|AI Control Tower for Enterprise AI Foundation|1.9.2|AI Control Tower adds new capabilities across discovery, governance, security, monitoring, and measurement of AI usage. Inventory and Discovery Block AI services detected through ACC. An AI Inventory Enrichment Agent scans your inventory for incomplete records and suggests values to fill the gaps. New and enhanced connectors extend discovery to Microsoft Agent365, Azure AI Foundry, Copilot, and AWS. Govern Discovered AI systems are now risk-classified at the point of discovery, before they enter the managed workflow. An AI Risk &amp; Control Applicability Advisor recommends the most relevant risks and controls for each system, with rationale. Dynamic Playbook 2.0 tailors onboarding tasks to an asset's risk classification. ServiceNow-managed AI agents can now be published to Microsoft Agent365 and other external registries. Secure AI agent containment can be triggered automatically based on authored policies in the AI Control Tower, removing the need for manual intervention. Support is extended to Azure AI Foundry for agent runtime and Gemini Enterprise Agent Platform \(via Okta integration\). Design-time security now covers AI agents, tools, MCP servers, and system prompts, not just AI models. The Veza connector now uses OAuth 2.0 for authentication. Monitor Configure trace data retention to fit your needs. View new latency and token-usage visualizations. Set evaluation metrics at the asset level. Use custom date ranges of up to 18 months for evaluation data. Measure Product owners can now view and work with just the AI systems and metrics that matter to them. Foundations Domain separation is available across AI Control Tower, enabling MSP and multi-tenant deployments with isolated inventories, security posture, and value data for each tenant. For full details, see AI Control Tower release notes.|
|AI Control Tower for ServiceNow Otto|7.0.3|see release notes for AI Control Tower for Enterprise AI Foundation|
|AICT UI Application|3.0.4|AINPX UI changes with Domain separation, Shadow AI and Control Framework|
|AI Data Explorer|5.2.7|Fixed: Action recommendations in AI Data Explorer no longer get incorrectly blocked when triggered.|
|AI Data Kit|9.0.4|New Ground Truth creation: a new end-to-end flow to create, label, and review ground truth data for agentic evaluation, including a dedicated labelling experience with task and project views, and guided entry from the dataset page Datasets can now be added directly as an input source to labelling projects, with a configurable data sink step Ground truth data is now available for Skill Kit to consume directly in evaluation runs Data discovery through automatically extracted dataset metadata Record-level filtering within a dataset Japanese language support for Voice Evaluation data generation, with testing across all supported languages Changed Improved synthetic data generation quality by incorporating agent instructions from Skill Kit Dataset creation now captures source details Fixed Multiple defect fixes across the ground truth and labelling experience, the dataset page, and synthetic data generation Security fixes|
|AI Desktop Actions|6.0.0|New Automate desktop and web-based adaptive tasks using the new AI Desktop Actions client application for the macOS system. Describe your task in the chat panel and the AI Desktop Actions executes it. Monitor the live execution of adaptive desktop actions in the preview window of AI Desktop Actions. Create security policies to control which files, folders, websites, and applications AI Desktop Actions can access. Take control of the execution where your input is needed. Changed Fixed Removed|
|AI Desktop Actions Core|6.0.0|New Automate desktop and web-based adaptive tasks using the new AI Desktop Actions client application for the macOS system. Describe your task in the chat panel and the AI Desktop Actions executes it. Monitor the live execution of adaptive desktop actions in the preview window of AI Desktop Actions. Create security policies to control which files, folders, websites, and applications AI Desktop Actions can access. Take control of the execution where your input is needed. Changed Fixed Removed|
|AI Discovery|2.9.7|New: Support for - Domain Separation support for AI discovery and the connectors Error Handling|
|AI Experience Framework Components|1.4.0|Here's the key features list: Updated plugin to use Pro Code format to align with AI Experience Framework Pro Code conventions. CSS fixes for kb, task and Request pages/widgets KB page: mobile responsive support enabled|
|AI Experience Framework Components for Setup Hub|1.4.0|Here's the key features list: Updated plugin to use Pro Code format to align with AI Experience Framework Pro Code conventions. Support for new macroponent loader that loads the widgets which are created with Pro Code experience, so those widgets are properly handled by the loader|
|AI Experience Framework Components for Setup Hub|1.4.0|Here's the key features list: Updated plugin to use Pro Code format to align with AI Experience Framework Pro Code conventions. Support for new macroponent loader that loads the widgets which are created with Pro Code experience, so those widgets are properly handled by the loader|
|AI Experience Framework Skills|1.4.4|Support for building widgets in the new format. Users can now build widgets compatible with the pro-code developer experience, with support for ACLs and configuration framework.|
|AI features for Deal Registration|1.0.2|New Release|
|AI for document designer|23.0.3|New AI-powered Word content generation now supports advanced third-party models Users can generate and manage Microsoft Word report content using Gemini 3.5 Flash \(with fallback to Gemini 2.5 Pro\), GPT-5.4-mini, and Claude 4.5 Haiku. Changed ServiceNow Otto Branding Updates References to Now Assist have been updated to ServiceNow Otto throughout the application, including updates to labels and user interface elements.|
|AI Help Framework|2.0.2|Changed: Enhanced AINH supported template patterns. Introduced underline, info-icons and nudges.|
|AI Insight Engine|4.0.2|New: The AI Insight Framework helps AICT workstreams deliver automatically prioritized insights, surfaced to AI Stewards and actionable with a single click.|
|AI Metric Engine|2.1.4|Support asset level metric configuration Added support for Domain Separation|
|AI Native Experience for AI Control Tower - ServicenowAI|4.0.1|AI Control Tower adds new capabilities across discovery, governance, security, monitoring, and measurement of AI usage. Inventory and Discovery Detect unsanctioned AI use with network detection \(Armis\) and endpoint detection \(ITOM ACC\), including model, user, department, and device details. Block AI services detected through ACC. An AI Inventory Enrichment Agent scans your inventory for incomplete records and suggests values to fill the gaps. New and enhanced connectors extend discovery to Microsoft Agent365, Azure AI Foundry, Copilot, and AWS. Govern Discovered AI systems are now risk-classified at the point of discovery, before they enter the managed workflow. An AI Risk &amp; Control Applicability Advisor recommends the most relevant risks and controls for each system, with rationale. Dynamic Playbook 2.0 tailors onboarding tasks to an asset's risk classification. ServiceNow-managed AI agents can now be published to Microsoft Agent365 and other external registries. Secure AI agent containment can be triggered automatically based on authored policies in the AI Control Tower, removing the need for manual intervention. Support is extended to Azure AI Foundry for agent runtime and Gemini Enterprise Agent Platform \(via Okta integration\). Design-time security now covers AI agents, tools, MCP servers, and system prompts, not just AI models. The Veza connector now uses OAuth 2.0 for authentication. Monitor Configure trace data retention to fit your needs. View new latency and token-usage visualizations. Set evaluation metrics at the asset level. Use custom date ranges of up to 18 months for evaluation data. Measure Product owners can now view and work with just the AI systems and metrics that matter to them. Foundations Domain separation is available across AI Control Tower, enabling MSP and multi-tenant deployments with isolated inventories, security posture, and value data for each tenant. For full details, see AI Control Tower release notes.|
|AIOps Agentic Workforce|2.2.5|New A new Alert Verification AI agent automatically reviews alerts against related incidents and knowledge articles, and closes them once a match confirms resolution. A new Integration agent lets you set up, browse, test, and manage integrations through natural-language conversation instead of manual configuration screens. The Integration agent can now also create credentials for an integration directly within the conversation. Express List UI enhancements for alert closure and for tracking the AI Specialist processing logic. Comprehensive logging and status tracking for alert verification workflow. Fixed AI agents no longer fail to receive a published version when an error occurs during creation, so they can run as expected. Autonomous analyses that fail are no longer marked as complete with empty insights. The flow that starts the AIOps AI Specialist now reflects the latest record data, preventing outdated information from being used.|
|AI Platform skills|3.2.2|Deprecating legacy navigation skill Removing retrieval-style commands from the navigation workflow and agent Adding record management agent for mutations to agentic workflows Widget rendering for premium chat in the navigation workflow|
|AI Policy Framework|1.0.4|New MVP release of AI Control Tower's Policy Framework and kill switch.|
|AI Readiness Evaluation|1.5.2|Fixed PRB2075907 - AI Assessment ITSM scheduled job fails with cross‑scope script error because question script field is stored as string|
|AI Risk and Asset Management for ServiceNow AI|1.5.3|New Enhanced AI Control Tower to automatically classify AI systems by risk at onboarding, helping identify managed and unmanaged assets and reducing manual review effort. Improved user experience and ability to save &amp; continue Evaluation configurations for continuous monitoring of AI assets. Enhanced AI Control Tower to support domain-separation readiness, enabling assessment and planning for client-level data segregation and multi-tenant deployments. Introduced new onboarding Playbook with dynamic &amp; risk-based execution &amp; lifecycle task management. Introduced new AI capabilities to recommend control objectives and risk statements on AI impact assessment task.|
|AI Risk and Compliance Integration with Control Tower|23.0.2|New Enhanced AI Control Tower to automatically classify AI systems by risk at onboarding, helping identify managed and unmanaged assets and reducing manual review effort. Improved user experience and ability to save &amp; continue Evaluation configurations for continuous monitoring of AI assets. Enhanced AI Control Tower to support domain-separation readiness, enabling assessment and planning for client-level data segregation and multi-tenant deployments. Introduced new onboarding Playbook with dynamic &amp; risk-based execution &amp; lifecycle task management. Introduced new AI capabilities to recommend control objectives and risk statements on AI impact assessment task. Fixed Fixed an issue where the Recommendation section was incorrectly displayed on the Risk and Compliance page. Fixed an issue where the Group Attestation action was not visible in the Attestation related list. Fixed upgrade-impact issues related to the introduction of a new field on the CCM Configuration record. Fixed an issue where the AI Asset Task state was not updated to Review after assessments were submitted.|
|AI Risk and Compliance Management|23.0.3|New Enhanced AI Control Tower to automatically classify AI systems by risk at onboarding, helping identify managed and unmanaged assets and reducing manual review effort. Improved user experience and ability to save &amp; continue Evaluation configurations for continuous monitoring of AI assets. Enhanced AI Control Tower to support domain-separation readiness, enabling assessment and planning for client-level data segregation and multi-tenant deployments. Introduced new onboarding Playbook with dynamic &amp; risk-based execution &amp; lifecycle task management. Introduced new AI capabilities to recommend control objectives and risk statements on AI impact assessment task. Fixed Fixed an issue where the Recommendation section was incorrectly displayed on the Risk and Compliance page. Fixed an issue where the Group Attestation action was not visible in the Attestation related list. Fixed upgrade-impact issues related to the introduction of a new field on the CCM Configuration record. Fixed an issue where the AI Asset Task state was not updated to Review after assessments were submitted.|
|AI sales activity association|1.2.1|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|AI Search RAG|7.0.3|New Enabled Reranker for Search Enabled RAG MCP|
|AI Security and Privacy|6.1.3|New Policy-Triggered AI Agent Containment: AI agent containment can now be triggered automatically based on authored policies in the AI Control Tower, removing the need for manual intervention. Support is extended to Azure AI Foundry for agent runtime and Gemini Enterprise Agent Platform \(via Okta integration\). Domain Separation for MSP Deployments - Managed service providers \(MSPs\) hosting AI Control Tower for multiple tenants now get strict data isolation. Each tenant's AI Steward sees only their own security posture scores, guardrail configurations, vulnerability records, and access maps. The MSP top domain retains a cross-tenant summary without exposing tenant-level details to peers. Accessibility and Internationalization - AI Control Tower Security pages are now fully WCAG 2.0 compliant and localized. Non-English users get a consistent, translated experience across all security screens. Changed Okta Token Revocation on Agent Deactivation - When an AI agent is deactivated or contained, all associated Okta refresh and active access tokens are immediately revoked. Veza Integration: OAuth Connector - The Veza connector now uses OAuth 2.0 for authentication. Admins configure an OAuth profile and alias. AI stewards select it directly from AI Control Tower Settings &gt; Integrations. Tokens are issued per user and tied to user identity, replacing the prior manual API Key approach. Extended SecOps Visibility: Design-time security now covers more metrics. In addition to AI models, AI Control Tower surfaces vulnerabilities and security findings for agents, tools, MCP servers, and system prompts, closing visibility gaps in agentic AI deployments. Asset Inventory: Security Tab Redesign - The Security tab in Asset Inventory has been streamlined for usability. The Agent Status card is replaced with Access Posture and empty state messaging is improved.|
|AI Service Graph Connector for Amazon|2.1.9|New- Certificate-based authentication support to reduce reliance on client secrets and access keys, especially for enterprise customers with stricter security requirements. Tenant-wide discovery support for discovering AI assets across an entire enterprise environment rather than requiring resource-by-resource configuration.|
|AI Service Graph Connector for Google|1.3.3|New: Google Multi-region support with parallel data loading Domain support on all staging tables Changed: Plugin name: AI Service Graph Connector for Google and SourceSystem updated to Google Agent Platform Fixed: Improved pre-validation checks for AI connection permissions and fields within playbooks in the AI Control Tower Workspace.|
|AI Service Graph Connector for LangGraph|1.1.7|Integration with LangGraph which would allow discovery and inventory of AI Agents, related models, prompts, and tool information. The AI Control Tower \(AICT\) imports the discovered artifacts into its AI inventory, where the AI steward and Product Owner can access and review them.|
|AI Service Graph Connector for Microsoft|3.1.19|New: Certificate based authentication support for setting up Microsoft connector. Support discovery across multiple Copilot environments through a single connection. Microsoft Agent365 Discovery Connector: Discover AI assets from Microsoft Agent365 registry which includes agents from Microsoft environments such as Copilot, Azure Foundry, Agent Builder etc. and non-Microsoft environment for the external AI connectors set up in Agent365 registry Catalog agents, models, tools and prompts across these environments into AICT inventory Support for automated deduplication of existing assets in AICT inventory discovered from Copilot and Azure FoundryTenant-wide support available|
|AI SGC Discovery|2.0.4|Please see release notes for AI Control Tower for Enterprise Foundations|
|AI Skill Kit|10.0.5|New Evaluate voice agents and assistants across en-US, fr-CA, de-DE, ja-JP, and es-MX to understand their performance and user experience in different languages.|
|AI Specialists for Security Incident Response|1.0.10|Fixed: Fixed an issue where non-maint users were not able to install the app.|
|AIS ZTSD Gemma|1.0.6|New Gemma embedding model integration enables automated indexing of configured data sources. The system now ingests and indexes data sources specified for Gemma embedding, triggering semantic ingestion at regular intervals and tracking indexing status for each source. Admins can now configure Gemma embedding model settings. The Gemma embedding model and its related configurations are now available for setup and management, allowing tailored embedding workflows for supported data sources. Changed The Gemma embedding ingestion trigger interval has been increased from 5 to 15 minutes. The ingestion process now handles missing configuration gracefully and reports completion status reliably. The Gemma embedding model identifier has been updated for consistency, and semantic index queries now use direct configuration lookup for improved accuracy. Ingestion tracking now preserves state and batch persistence, ensuring that already-indexed data sources are not re-ingested and status is maintained across runs.|
|AI Trace Collector|3.1.3|New Selection of log groups for AWS Cloudwatch Changed UI modifications for Microsoft Azure trace collector Fixed Defects|
|Alert Assist|3.12.2|New LLM-as-Judge pipeline enables automated quality evaluation for alert handling. Auto-closure reasoning and expanded explanations are available for alerts. Enable offglide execution for compatible alert skills. Alert verification logic for insignificant alert closed scenarios implemented. Changed Alert reasoning headers updated for all closure scenarios Autonomous Not Significant Styled Output prompt revised. Links support expanded for closure reasoning. Limit applied to insignificance reason bullets. Data handling improved for insignificance reason from summarization prompts New headers added for alert reasoning scenarios.|
|APO - Foundation|2.0.0|The application captures dependencies, updated the plugin dependencies for this release.|
|APO - Prime|2.0.0|The application captures dependencies, updated the plugin dependencies for this release.|
|app-ai-metric-ui|2.1.4|Support asset level metric configuration Added support for Domain Separation|
|app-ent-data-map-components|1.0.0|New • Added Enterprise Data Transform Components application. • Added reusable Seismic/Tectonic workspace components for Enterprise Data Transform experiences. • Added workspace components supporting guided import, column mapping, value mapping, data staging, validation, and import result experiences. • Added component framework supporting AI Assisted Asset and Model Import experiences.|
|App Studio Commons|30.1.0|Maintenance release.|
|Asset Management Common|16.0.0|New Automatic remediation of invalid ACL-role references across Core and Store applications. All plugins now enforce valid role checks, ensuring that access controls behave consistently and securely during installation and upgrade. Plugin dependencies are declared accurately, and obsolete role associations are removed. Clean instance installation and ACL behavior validation are completed for all remediated plugins. Automated shipping and loading of Query ACLs for Asset Management Common. Plugins and Store Apps now ship Query ACLs for all tables in non-track-managed Glide family repositories and Store App repositories. Query ACLs are loaded automatically during installation or upgrade, eliminating the need for manual auditor script execution. Customized ACLs are retained, and out-of-box ACLs are marked inactive when customizations are detected. Zboot and upgrade testing confirm correct loading and behavior. Changed JavaScript sandbox analysis and validation for Asset Management repositories. The JavaScript used in ACL conditions, module filters, condition checkers, GlideFilter usage, UI action conditions, and catalog variable defaults has been scanned and verified for app-itam-common, app-itam-mobile, now-mobile-assets, and app-itam-asset-audits. Automated tests now cover each distinct pattern, ensuring no functional regressions. Fixed Asset status evaluation has been corrected to prevent null values, ensuring that the "Set install date hardware &amp; enterprise" business rule is applied as expected for digital assets. Duplicate asset reclaim requests are no longer allowed; the system now prevents submission of multiple reclaim requests for the same asset. The "Create Asset" action in HAM Workspace now correctly creates assets in the intended hardware table, not in the generic asset table. Asset repair entries in HAM-only instances now populate the "Available for" field in catalog item user criteria, ensuring accurate assignment. Email notifications are now sent when contract renewal requests are submitted for approval. Related lists are now rendered correctly in Hardware Asset Workspace, restoring visibility for stockroom-related lists. Scheduled jobs for populating model and stockroom data now execute reliably for existing customers, even when HAM/EAM is not present. Asset ID mismatches in POL Receive staging rows have been resolved; purchase line write-back queries now stamp each row with the correct asset ID. Null pointer exceptions no longer occur when updating calculated formulae for hardware models with empty start date fields. Assignment group retrieval performance has been improved for troubleshooting tasks with large data sets.|
|Assist Order Management AI Agent|1.1.2|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Attribute propagation|9.4.3|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Attribute propagation|9.4.3|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|AWH for AI Control Tower|3.4.0|AI Gateway is relaunched in September 2026 after a short break in August. Users can now continue using AI Gateway for MCP Server transactions.|
|Basic Scoring for Smart Assessments|23.0.3|Fixed Corrected missing and incorrect translations for UI strings across the interface. Changed Unsaved changes now persist across all workspace tabs \(General, Questions, Automations, Scoring\). A dirty-state icon on the workspace selector indicates pending changes, letting you navigate tabs without losing work.|
|Build Agent \(Trial\)|2.6.4|New New model support Build Agent now supports the following models: Azure OpenAI GPT 5.6 Sol Anthropic Claude on AWS Opus 5 Testing Create and run ATF test suites from Build Agent. Group multiple tests under a single suite and execute the suite to run regression testing without selecting individual tests. Execution status and any errors are reported in the chat panel. Test Agent can now generate ATF tests that use list and related list test steps, including validate related list visibility and apply filter to list. List step support extends test coverage beyond form-based interactions to include the full list view experience on the ServiceNow AI Platform. Integrations &amp; metadata Build Agent now supports integrations with the Box MCP server. ServiceNow Fluent, which Build Agent uses to create apps, now supports domain separation on records and APIs. You can set the sys\_domain field and use sys\_override fields when working with records in domain-separated environments, so ServiceNow Fluent operates correctly across domains in your instance. The following metadata are now supported in Build Agent: Service Catalog dependent question support Transition condition UI style Platform &amp; availability When you right-click a record or artifact and select Configure, the metadata editor now opens in ServiceNow Studio. Build Agent \(Trial\) is available by default on all instances, without requiring installation. Build Agent now supports automatic upgrades through the ServiceNow Store. Instances running Australia Patch 5+ or Zurich Patch 12+ that have Build Agent installed receive automatic upgrades when a new version is published. Playbook support Build Agent includes the following updates to Playbook support: Consolidates all records related to a playbook into a single XML update set file. Can now generate runtime permissions at the playbook level and at the stage level. Can now generate and configure the Set Playbook Outputs activity for nested playbooks. Can now configure agentic fields on form-based and record-based activities when the AI Agent plugin is active. Can now generate on-demand playbook launcher configurations. Can now define optional activities in a playbook. Changed New agentic-first development experience ServiceNow Studio and IDE were redesigned for an agentic-first development experience with Build Agent: The central chat area on the ServiceNow Studio home page is the starting point for new Build Agent conversations. To open an existing conversation, select the Conversations icon in the Navigator panel. The Build Agent panel now opens on the Navigator panel of ServiceNow Studio.|
|Build Agent Premium|1.6.0|New New model support Build Agent now supports the following models: Azure OpenAI GPT 5.6 Sol Anthropic Claude on AWS Opus 5 Testing Create and run ATF test suites from Build Agent. Group multiple tests under a single suite and execute the suite to run regression testing without selecting individual tests. Execution status and any errors are reported in the chat panel. Test Agent can now generate ATF tests that use list and related list test steps, including validate related list visibility and apply filter to list. List step support extends test coverage beyond form-based interactions to include the full list view experience on the ServiceNow AI Platform. Integrations &amp; metadata Build Agent now supports integrations with the Box MCP server. ServiceNow Fluent, which Build Agent uses to create apps, now supports domain separation on records and APIs. You can set the sys\_domain field and use sys\_override fields when working with records in domain-separated environments, so ServiceNow Fluent operates correctly across domains in your instance. The following metadata are now supported in Build Agent: Service Catalog dependent question support Transition condition UI style Platform &amp; availability When you right-click a record or artifact and select Configure, the metadata editor now opens in ServiceNow Studio. Build Agent \(Trial\) is available by default on all instances, without requiring installation. Build Agent now supports automatic upgrades through the ServiceNow Store. Instances running Australia Patch 5+ or Zurich Patch 12+ that have Build Agent installed receive automatic upgrades when a new version is published. Playbook support Build Agent includes the following updates to Playbook support: Consolidates all records related to a playbook into a single XML update set file. Can now generate runtime permissions at the playbook level and at the stage level. Can now generate and configure the Set Playbook Outputs activity for nested playbooks. Can now configure agentic fields on form-based and record-based activities when the AI Agent plugin is active. Can now generate on-demand playbook launcher configurations. Can now define optional activities in a playbook. Changed New agentic-first development experience ServiceNow Studio and IDE were redesigned for an agentic-first development experience with Build Agent: The central chat area on the ServiceNow Studio home page is the starting point for new Build Agent conversations. To open an existing conversation, select the Conversations icon in the Navigator panel. The Build Agent panel now opens on the Navigator panel of ServiceNow Studio.|
|Business Continuity Management Advanced|2.0.3|\*\*New\*\* Report and summarize GRC issues faster . Issue Summarization and Issue Validation are available across BCM Foundation, BCM Advanced. Automated Resolution Planning is available in BCM Advanced . These capabilities enable you to track issue status from discovery through closure from the Employee Center in an instance or from plan and event records in Business Continuity Workspace. New features - Assign group ownership to business impact analysis, plan, and event records BIA owner and contributor synchronization Integration of the GRC Issue module Import and export recovery tasks from Microsoft Excel Enhance collaboration between recovery teams during a crisis \*\*Fixed\*\* Performance defects for Update dependencies, Crisis Map loading.|
|Business Continuity Management Foundation|2.0.3|\*\*New\*\* Report and summarize GRC issues faster, Issue Summarization and Issue Validation are available for BCM Foundation. New features - Assign group ownership to business impact analysis, plan, and event records BIA owner and contributor synchronization Integration of the GRC Issue module Import and export recovery tasks from Microsoft Excel Enhance collaboration between recovery teams during a crisis \*\*Fixed\*\* Performance defects for Update dependencies, Crisis Map loading.|
|Business domain|23.0.2|New Zurich platform support for GRC business domain apps Customers can now use GRC business domain, Document Designer, role mapping, and metric features on both Zurich and Australia platforms.|
|Care Team Operations AI agent collection|2.1.1|New Enhancements to provide better support for agentic engineering.|
|Case lines and workflows|4.6.1|Fixed: Security enhancement to query ACL enforcement in Case Lines application.|
|Case Management for Invoice Operations|2.1.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Case Management for Invoice Operations|2.1.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Catalog Conversational Coverage|6.2.1|Fixed Minor enhancements and defect fixes.|
|Change Management AI Orchestrator|1.0.4|Change Management AI Orchestrator introduces an AI-driven orchestration layer for Change Management that autonomously prepares change requests by coordinating multiple specialized AI agents. The objective of this release is to reduce manual effort, improve preparation quality, and deliver approval-ready changes while keeping governance and approval decisions under customer control. This release is available as a Controlled Availability \(CA\) release and is intended for selected customers participating in the CA program. New Multi-agent orchestration Provides orchestration support for the following participating capabilities: CI Identification: An intelligent CI capability analyzes the change context and recommends relevant CIs, simplifying CI selection. Change Plan Preparation: Generates implementation details, test plans, justification, and backout plans based on the change context. Risk Assessment: Automatically completes the risk assessment survey and triggers applicable risk conditions to determine the risk score. Quality Assessment: Evaluates the quality of the change based on the prepared implementation plan and supporting information. Schedule Recommendation: Identifies scheduling conflicts and guides users toward an appropriate change schedule. Change Summarization: Generates a consolidated summary of the change to provide approvers with the relevant context before approval. Overall, the Change Management AI Orchestrator coordinates these capabilities to produce a consolidated, approval-ready change record containing implementation details, readiness information, risk and quality assessments, scheduling recommendations, and an overall change summary. The Orchestrator also supports human-in-the-loop governance, pausing when user confirmation is required, such as during CI selection, while maintaining appropriate governance and auditability throughout the process.|
|Change Management for Service Operations Workspace|9.4.2|Problem fixes Standard Change Proposal Template Values are no longer editable in SOW after Submission Add schedule on a CAB definition record now correctly checks for create access Calculated Risk Score is now populated accurately if the Risk conditional rules do not match 'Risk Evaluation' section will now appear in the 'Overview' section if configured for 'New' Change Requests on the Service Operations Workspace Request Approval action is only shown on inserted records Removing unnecessary sys\_notification named 'Change notification' that could be triggered on any insert or update to a change\_request that was presented as a sys\_notification\_workspace\_content item|
|Chat Recommendation|1.9.1|New: - Chat Recommendation Search Sources configuration UI, allowing configuration of which sources feed AI-recommended responses - Custom context support in the Chat Reply Recommendation \(CRR\) prompt Changed: - Updated truncation strategy based on selected sources Fixed: - Enforced KB citation when used by the prompt|
|Chat Summarization for Virtual Agent|1.12.7|Support Sidebar Summarization to extended tables Fix empty transcript fetch during Agent 'End chat' summarization|
|Cloud Cost Management|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Cost Management Advanced|1.0.0|The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available: Foundation: AI basics to deliver insights Advanced: AI to boost productivity across relevant use cases Prime: Act autonomously with all AI assets, and create your own|
|Cloud Cost Management AWS|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Cost Management Azure|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Cost Management Core|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Cost Management GCP|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Cost Management Infra Stack|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Integrations AWS|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Integrations Azure|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Integrations Core|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Integrations GCP|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Spend Reports AWS|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Spend Reports Azure|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Spend Reports Core|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|Cloud Spend Reports GCP|11.0.0|The version 11.0 release introduces AI-powered summarization of cloud spend reports, standardized business context for unified cost reporting with total cost of ownership \(TCO\), business insights using the Unit Economics dashboard, and a reorganized Cloud Cost Management Workspace with enhanced navigation and reusable saved views. What's new Make smarter cloud cost decisions with AI-powered summarization of cloud spend Get complete cost visibility with TCO and unit economics Manage cloud spend attribution with the tag category source selection capability Streamline spend analysis with saved, shared, and reusable report views Experience reorganized Cloud Cost Management Workspace with intuitive navigation and broader visibility What's changed The Summarize button on the Monthly spend breakdown report now generates an AI-assisted summary of your cloud spend trends, top cost drivers, and optimization recommendations across all cloud service providers. The Business Insights view has been added to the Cloud Cost Management Workspace Saved views on the Cloud Cost Management Workspace Optimization view on the Cloud Cost Management Workspace|
|CMDB CI Class Models|1.94.3|New FortiManager Discovery: Added the CI class model foundation for FortiManager/Fortinet discovery. New/updated classes: cmdb\_ci\_firewall\_device\_fortinet, cmdb\_ci\_firewall\_device\_group\_fortinet, cmdb\_ci\_fortimanager\_network\_manager, cmdb\_ci\_fortinet\_firewall\_policy, and cmdb\_ci\_fortinet\_firewall\_policy\_pkg, layered onto the base firewall/policy-group classes \(cmdb\_ci\_firewall\_device, cmdb\_ci\_firewall\_device\_group, cmdb\_ci\_firewall\_policy\_group, cmdb\_ci\_firewall\_sec\_policy, cmdb\_ci\_policy\_group, cmdb\_ci\_networking\_policy\_group, cmdb\_ci\_multiservice\_network\_manager\). Includes class descriptions, identifiers/identifier entries, and containment/hosting relationship metadata. Nexus VRF Discovery: Added a new cmdb\_ci\_virtual\_routing\_forwarding class to support discovery of non-default VRFs and VRF-to-IP relations on Nexus devices, with identifier, identifier entry, and hosting-relationship metadata. MPN 5G CMDB Classes: Added new CMDB CI Class Model support for Mobile Private Network \(MPN\) 5G RAN/Core objects: New class Mobile Network Slice \(cmdb\_ci\_mobile\_network\_slice\) with slice service type/differentiator attributes and an identification rule. New class Unified Data Repository Function \(UDR\) \(cmdb\_ci\_5g\_unified\_data\_repository\_function\), rounding out the 5G core network function set alongside UDM/NRF. Extended cmdb\_ci\_sim\_card with new SIM Type/Form Factor choices. Registered the new classes in the class-model manifest and added relationship-suggestion and UI list/section records. Modified DNS Data Model: Reworked the DNS class hierarchy. Updated dictionaries for cmdb\_ci\_dns\_zone, cmdb\_ci\_dns\_resource\_record, cmdb\_ci\_provider\_dns\_zone, and the A/AAAA/CNAME/MX/NS/PTR/SRV/TXT/HTTPS DNS record classes, with refreshed class info, identifiers, identifier entries, and relationship-suggestion records. Shipped a glidefix \(fix\_update\_dns\_class\_labels\_and\_descriptions\) to correct class labels/descriptions and plural names on existing instances, plus new list/form views. os\_install field for SAMS: cmdb\_ci\_hardware now conditionally gets the os\_install field only when the SAMS plugin \(com.snc.sams\) is installed, delivered via a plugin-scoped dictionary override \(if/com.snc.sams/dictionary/cmdb\_ci\_hardware.xml\). MSSQL AG replica cleanup: Added a Table Cleaner \(sys\_auto\_flush\) rule for cmdb\_ci\_mssql\_ag\_replica \(age = 3600s, install\_status = 7\) that retires stale old-format replica CIs once the pattern's prepost script marks them retired — preventing duplicate replica records \(and the resulting "multiple primary replicas" symptom\) from accumulating. sys\_dm\_policy was deliberately not shipped, since it's platform-auto-generated. Data Model Navigator description fixes: Corrected the DMN field descriptions for cmdb\_ci.last\_discovered and cmdb\_ci.discovery\_source to accurately reflect IRE-driven update behavior. HPE Enclosure/Blade serial numbers: Added a new script include and an on-demand scheduled job \("Clear HPE Blade Serial Numbers"\) to clean up serial number values that Discovery had incorrectly concatenated with UUID for HPE Enclosures and Blades, which had been blocking customers from opening HPE support tickets.|
|CMDB MCP Server|2.0.0|Initial release.|
|CMDB Workspace|9.6.0|New Welcome to ServiceNow Otto, the new name for Now Assist! Support for 400% zoom in web browsers. Access Service Graph Workspace governance capabilities directly within CMDB Workspace, including: Insights Ingestion \(formerly SGC Central\) Data Owner View \(formerly Data Owner Home\) Explore &amp; Search Tasks Changed Show dependency maps in Unified Map for specific Service Instance CI classes, instead of using service maps. Service Graph Workspace - is being rolled back into CMDB Workspace. Any customers who have not yet adopted Service Graph Workspace, must continue using CMDB Workspace. For customers who are using Service Graph Workspace, please switch back to CMDB Workspace. Access content previously available on the Home page from the Governance page. SGC Central has been renamed to Ingestion. Data Owner Home has been renamed to Data Owner View. Fixed Various CMDB Data Manager performance and quality issues. Various Data Certification quality issues. CMDB Workspace and CI Form quality issues. Various internationalization issues. Removed The Move to Service Graph Workspace banner is no longer displayed in CMDB Workspace.|
|Collaboration Services for Service Operations Workspace|9.4.3|Ability to automate initiation of a conference call|
|Collaborative Work Management|11.0.1|New Build multiple customizable dashboards per Board with real-time charts, scores, and widgets to track delivery health at a glance. View and connect epics, defects, sprints, and other work artifacts natively within Boards, with flexible filtering, sorting, and grouping. Keep Project Workspace and CWM tasks synchronized in both directions, with statuses, dates, and comments updating in real time across platforms.|
|Collaborative Work Management - Advanced|2.2.1|New Automatically convert external documents, meeting notes, and natural-language prompts into structured, actionable tasks CWM tasks. Keep Project Workspace and CWM tasks synchronized in both directions, with statuses, dates, and comments updating in real time across platforms. View epics and other connected work across Boards natively within CWM in one view, with AI-assisted filtering for relevant results. Build multiple customizable dashboards per Board with real-time charts, scores, and widgets to track delivery health at a glance. Instantly break any CWM task into smaller, assignable child tasks with a single click, eliminating manual task drafting.|
|Common Guidances|16.0.2|New: Recommended actions now support new guidances, 'Attach Knowledge' and 'Relevant Case' for AI Search results that surface on the CRM workspace.|
|Common Service Delivery|15.0.0|New: Admins can access SPO Product Admin Home as a single entry point. Product Hub provides guided installation of SPO applications and plugins. Configuration Console provides a guided experience for configuring Procurement Case Management items, including completion tracking. From Configuration Console, admins can download update sets and upload batch update sets to higher environments. Changed: SPO configuration is now organized within the Otto for Setup framework, replacing navigation across multiple administrative tools and locations. The administrative experience is now consistent across Product Hub and Configuration Console.|
|Common Vendor Core|5.0.2|New Added third-party element assessment, issue, and task related lists to Vendor Management Workspace.|
|Compatibility Management|6.7.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Compatibility Management|6.7.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Configurable Workspace for Order Management|16.1.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Configurable Workspace for Order Management|16.1.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Content Understanding|7.1.4|Changed This release enhances stability and usability across document extraction, table configuration, and use case setup. Key enhancements include more reliable extraction when handling missing or malformed field values, extended support for typed keys in table extraction, and fixes to use case creation for Contract Analysis and localized formatting.|
|Context Rule Management|10.8.1|New Advanced reference qualifiers support in context variables, enabling complex product references Lifecycle-aware context variables now handle product offering states correctly Changed Context variable management improved for deletion and rule integration Fixed Performance regression with currency field mapping in context variables Cache invalidation issue causing stale values in pricing Fixed issue where context variables could not be deleted from eligibility rules|
|Contract Management Pro MCP Server|1.0.4|New You can now use the Contract Management Pro MCP Server to support AI-assisted contract analysis with external AI tools, with the playbook tool exposed through MCP for an external AI contract negotiation. You can now create, configure, edit, and activate or deactivate contract analysis playbooks. Changed Fixed Removed|
|Contract Management Pro - Prime|1.0.21|New N/A Changed In conversational search, introduced an option to preform in-document search after the contract metadata search results are available. Contract document-based conversational search queries now return all matching results instead of 10 results. Use show more option to load the remaining results. Contract Management Pro - Prime now uses the latest versions of its dependent platform applications for the September 2026 release. Fixed Fixed plugin names and icons for ServiceNow Otto for Contract Management Pro in AI Admin Hub. Removed N/A|
|Conversational Analytics|9.3.1|New Changed Fixed Active VA Users widget count mismatch with the drill-down users page. Broken date display \(NaN:NaN\) in conversation analytics for non-default date formats. Removed|
|Conversational Catalog Requests|8.0.2|New: Increased coverage of conversational requests served through the Catalog Agent on Premium chat, now supporting: Simple UI policies and field messages. Enhanced slotfill handling throughout the conversation, including cases where a user is changing a prior response or their response requires corrections. Fixed: More robust multi-language support. Other defect fixes.|
|Conversational Integration with Slack|6.1.0|New Multi-select support Changed Synthesis response rendering Fixed Loading indicator issues Granular feedback thumbs down issue Removed|
|Conversational Studio|12.0.7|New Bulk migration of Topics to AI Agents is now supported \(MAINT-only\). Admins can select and migrate batches of 100+ Topics to AI Agents at once using the Topics-to-AI Agents tool. The migration workflow includes progress tracking, validation, and assignment of migrated AI Agents to Assistants, with each migration status visible and actionable. Integrated evaluation and actionable insights for migrated AI Agents. The Topics-to-AI Agents tool now supports automated evaluation of migrated AI Agents, enabling admins to generate datasets, run evaluations, and compare quality metrics between Topics and AI Agents. Evaluation results surface dominant failure patterns, ranked by severity and frequency, with drill-down to scenario transcripts and issue explanations. Custom severity levels for evaluation failure patterns. Users can now customize severity levels for actionable insights failure patterns across all evaluations. Severity changes are saved automatically and apply to both past and future evaluations. Scenario drill-down and transcript access in evaluation results. Admins can view detailed scenario lists and transcripts for failed conversations, filter by detected issues, and download transcripts for further analysis. NAP Platform Assistant support in Auto Evaluation. The NAP Platform Assistant is now available as a selectable option in the Auto Evaluation creation flow, and its evaluation results are accessible in the results screen. Testing UI decoupled from Assistant "Active" state. The Test Assistant button is now enabled even when the Voice Assistant is not active, allowing testing at any time without requiring activation. Changed None Fixed MCP Servers are now hidden from the Asset Library. MCP Server assets are no longer visible in the Asset Library and can only be accessed via the Assistant create/edit flow in a dedicated section. Users cannot modify the discoverable, visible, or promoted status of MCP Servers. Removed None|
|Conversation Evaluator|3.2.1|New Changed The Conversational Evaluator now supports domain separation, enabling organizations to evaluate conversational experiences within their designated domains while keeping evaluation data appropriately isolated. Fixed Removed|
|Core Business Suite Prime for Health and Safety|3.3.3|Fixed minor defects. Resolved dependency issues for the Brazil release.|
|CPQ Config Agent A2A|1.1.7|Updated for the September 2026 platform release.|
|CPQ for Manufacturing Advanced|3.0.0|This app will be hidden on the store. No listing content is applicable for this store app.|
|CPQ for Manufacturing Foundation|3.0.0|This app will be hidden on the store. No listing content is applicable for this store app.|
|Craft.co Integration for Supplier Lifecycle Operations|9.0.0|Changed Migration of code to Fluent|
|CRM API Core|7.4.1|NEW Not Applicable Change Renamed the application|
|CRM Core|1.10.1|NEW Not Applicable Change Renamed the application|
|CRM Outlook Add-in|1.2.1|Changed The Microsoft Outlook add-in now handles edge cases more gracefully. For example, the add-in provides clearer experience and next steps when no matching records are found or when the user lacks permission to view an associated record. Fixed Minor enhancement to the email promotion rules configured.|
|CRM Touchpoint|1.6.1|Fixed: Performance improvements. When updating the related opportunity on a Tech Win or other sales interaction record, using the search function required users to select the opportunity twice before the change is applied \(PRB2060555\).|
|CTO Voice AI Agents|2.1.0|New Enhancements to provide better support for agentic engineering.|
|Custom App Record Summarization|30.1.1|Changed Maintenance release.|
|Customer Contracts and Entitlements|15.0.1|Fixed minor defects.|
|Customer Household Data Model|2.0.11|New: NA Changed: NA Fixed: Security enhancements Removed: NA|
|Customer Install Base Characteristics|2.5.4|New: None Changed: Changed the App name to Customer Install Base Characteristics Fixed: None Removed: None|
|Customer Install Base Management|4.10.3|New Sold Products now support multiple related parties with distinct roles — Bill-To, Ship-To, Sold-To, Entitled-To, Partner, End Customer, or Installed At. Sold Products now capture Deal Type \(Direct/Indirect\) and Route to Market \(Direct/Resale/Distributor\). Related parties from an Order are now automatically copied to the Sold Product created from it. Changed Deal Type, Route to Market, and related parties are now visible on the Sold Product form, on both the platform view and CSM configurable workspace. Account and related-entity access is now restricted based on each user's configured criteria. Fixed The Sold Product tab on the Account view now correctly shows only the sold products tied to that account. The Model Category list now populates correctly during Order to Install Base Item configuration. An access control role issue has been resolved to ensure proper record security. Removed NA|
|Customer Service Management AI agent collection|7.0.1|New Clarification options are now presented as selectable buttons. Users can select clarification options during an interaction, and the selected option is passed directly to the agent for recommendation. Recommendation sources are now accessible within the ServiceNow Otto panel. Agents can review source information without leaving their workspace, following platform-aligned presentation patterns. Live Agent Assist references have been updated to Live interaction recommendations AI agent. All references across the codebase, including skill names and AI Search Profile names, now match the new naming convention. Customer Service Management AI agent collection is now available in Fluent Support. The app-csm-ai-agents repository has been converted to Fluent, enabling new AI agent capabilities for customer service management. Changed Clarification options have been redesigned for improved usability. The interface now uses buttons instead of text, enhancing the selection experience for users. Widget styles for clarification options have been updated. Visual improvements have been applied to ensure consistency and clarity. ServiceNow Otto panel source display follows Horizon-aligned patterns. Source information presentation has been updated to match platform standards. Removed Legacy clarification option widget has been deleted. The previous text-based widget is no longer available, replaced by the new button-based interface.|
|Customer Service RMA AI Agents|1.1.4|Fixed: The internal implementation has been updated.|
|Cyber Physical Systems Control Tower Advanced|1.0.2|Changed The application name was changed from Industrial Control Tower to Cyber Physical Systems Control Tower|
|Cyber Physical Systems Control Tower Foundation|1.0.2|Changed The application name was changed from Industrial Control Tower to Cyber Physical Systems Control Tower|
|Cyber Physical Systems Control Tower Prime|1.0.2|Changed The application name was changed from Industrial Control Tower to Cyber Physical Systems Control Tower|
|Cyber Physical Systems Operations Advanced|1.0.5|Changed The application name was changed from Industrial Operations Suite to Cyber Physical Systems Operations|
|Cyber Physical Systems Operations Foundation|1.0.5|Changed The application name was changed from Industrial Operations Suite to Cyber Physical Systems Operations|
|Cyber Physical Systems Operations Prime|1.0.5|Changed The application name was changed from Industrial Operations Suite to Cyber Physical Systems Operations|
|Cyber Physical Systems Security Advanced|1.0.5|Changed The application title was changed from Industrial Cyber Security Suite to Cyber Physical Systems Security|
|Cyber Physical Systems Security Foundation|1.0.5|Changed The application title was changed from Industrial Cyber Security Suite to Cyber Physical Systems Security|
|Cyber Physical Systems Security Prime|1.0.7|Changed The application title was changed from Industrial Cyber Security Suite to Cyber Physical Systems Security|
|Dashboard and visualization export|1.4.1|Fixed: Ensure the Dashboard and Data visualization export skill is available from the AI Admin Hub for activation and deactivation|
|Data Foundation Model|1.13.2|New AI Agentic Client Application CI Class Introduced a new generic CMDB class cmdb\_ci\_agentic\_client\_appl \("Agentic Client Application"\), extending cmdb\_ci\_appl, to represent AI agentic client applications \(e.g. ARC, Claude Cowork, Claude Desktop\) as configuration items. Previously these existed only as alm\_ai\_system\_digital\_asset records \(model category "Agentic Client"\) with no CI representation, so they couldn't be reconciled through the standard identification flow or distinguished from generic applications in inventory/reporting. - No class-specific columns in this release — inherits standard application CI attributes \(name, version, discovery source, first/last discovered, owned by, assigned to, department\). - Added the corresponding cmdb\_class\_info record, configured as extendable with audit disabled. - Relationship to the source alm\_ai\_system\_digital\_asset record flows through the standard cmdb\_rel\_asset\_ci asset-to-CI relationship \(one-to-many\). Update - AICT 2.0 Activity Stream — Fixed AI Control Tower 2.0 inventory pages not showing the activity stream/work notes on AI asset records \(present in AICT 1.0\). Added a new "Activities" form section to alm\_ai\_system\_digital\_asset, wired via a new form-section/UI-section pair, so activity history and work notes now render consistently with the AICT 1.0 experience. - AI/Information asset table scope migration fix — Fixed a data-dictionary inconsistency on alm\_ai\_digital\_asset.servicenow\_ref\_id, whose dependent field was incorrectly pointing at now\_assist\_ref\_table instead of servicenow\_ref\_table. On instances where the AI/information asset tables were never fully migrated from the "Expanded Model and Asset Classes" \(sn\_ent\) scope to Data Foundation Model \(sn\_cmdb\_foundation\), an earlier dictionary correction never reached the customer's dictionary record. Added an apply\_once glidefix that corrects the field in the global scope regardless of which scope currently owns the table, restoring a clean, updateable baseline.|
|Data Grid UI Component|26.0.13|Fixed: Resolved an issue where screen readers did not provide correct output for complex table headers. Resolved an issue where status icons and currency information lacked programmatic representations for assistive technologies. Resolved an issue where the Total row in grid tables was not accessible via keyboard navigation. Resolved an issue where screen readers did not announce the column header sort status, including sort direction, in Strategic Planning Workspace. Resolved an issue where the Gantt chart component displayed an extra personalize column button when the toolbar was placed at the top. Resolved an issue where the visual position and programmatic structure of tables were inconsistent, causing incorrect output for screen readers. Resolved an issue where collapsed cost plans in the Project Workspace financial view did not remain collapsed after entering costs. Resolved an issue where the RIDAC side panel grid displayed an additional close button when custom headers and headings were enabled. Resolved an issue where updating the status of goals in Strategic Planning Workspace caused the workspace view to become blank. Resolved an issue where task detail tooltips in the Project Workspace Gantt chart prevented selection of dependency handles. Resolved an issue where dot-walked reference columns were incorrectly totaled in group and grand total rows. Resolved an issue where pressing Esc did not remove the new inline edit row when a reference field was edited. Resolved an issue where the close button was missing from the item side panel in the Prioritization tab. Resolved an issue where column virtualization did not work correctly with nested columns.|
|Data Model for Order Management|17.1.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Data Model Navigator|1.1.3|AI Search configurations exclude tables and field records without descriptions.|
|Data registry|23.0.1|Fixed: Addressed Cobalt Raven-related security defects.|
|Data Relationships Framework|12.0.2|Addressed minor issues in core data relationship functionality.|
|DCNAM - Advanced|2.3.0|recertification for Brazil|
|DCNAM - Advanced|2.3.0|recertification for Brazil|
|DEX Application and Device Health|5.2.3|Fixed: Reliable loading of the File Management tab in the Windows Device Overview. Correct units for the endpoint boot time display. Faster loading of the Active Devices view on the Application tab for both installed and web applications. No interference between the macOS Zscaler check and Zscaler Client Connector \(ZCC\) upgrades. Support for monitoring 90 or more applications at scale in the Installed Application historical check. Correct display of menu items in the Insights navigation menu, without truncation. Location updates for devices with static location settings when the cmn\_location record is updated, applied when a qualifying event occurs after the 7-day expiry. Validation that prevents the reuse of the same executable in multiple application configurations. Correct URL for Microsoft Outlook in the out-of-the-box application configuration. Removal of the duplicate executable from the out-of-the-box application configuration for Tanium. Correct regular expression evaluation for the Operating System Event rule.|
|DEX Content Playbook|5.2.2|See DEX Application and Device Health product for release notes. This app is a dependency of DEX Application and Device Health.|
|Dynamic Guidance|28.5.1|Changed: Dynamic Guidance tailors recommendations based on your role, ensuring relevant and contextual support.|
|Employee Center|44.3.1|Updated to support the latest version of the dependent apps.|
|Employee Profile|14.2.1|Updated to support the latest version of the dependent apps.|
|Employee Slate \(built for Now Assist\)|1.4.4|Directory template: New landing-page layout guides employees through topic subtopics for clearer content pathways. Breadcrumb navigation: Employees can now easily navigate through the topic hierarchy with contextual breadcrumb links. Ask Otto name configuration: Admins can customize the displayed assistant name while supporting the configured Moveworks bot-friendly name by default. Browse UI refinements: Visual and usability improvements across Browse deliver a more consistent and polished experience. Inline admin configuration: Admins can now edit Browse options, Quick Links, Knowledge, and Applications directly without navigating to separate configuration records. Image auto-compression: Images are automatically compressed and optimized per display context \(thumbnail, carousel, hero feed\). Task delegation: Employees can now delegate tasks to colleagues directly from the task details view. Person card report counts: Person cards in the org chart now display total report count alongside direct report count by default. Home page background theming: Admins can set home page backgrounds per theme in the Admin Console, enabling different audiences to have distinct visual experiences.|
|Enhanced Features for IRM Enterprise|23.0.1|Fixed: Otto branding and logo changes|
|Enhanced Features for IRM Professional|23.0.2|Fixed: Otto branding and logo changes|
|Enterprise Asset Management Advanced|2.0.0|New: Added support for ServiceNow Otto for Enterprise Asset Management. Added support for AI-powered asset request and repair experiences. Added support for AI-powered asset data loading experiences. Changed: None Fixed: None Removed: None|
|Enterprise Asset Management for DCNAM|2.0.0|New: None Changed: Updated compatibility with the latest Enterprise Asset Management release and dependent apps. Fixed: None Removed: None|
|Enterprise Asset Management for DCNAM Advanced|2.0.0|New: Added support for ServiceNow Otto for Enterprise Asset Management. Added support for AI-powered enterprise asset request experiences. Added support for AI-powered troubleshooting and repair assistance experiences. Changed: None Fixed: None Removed: None|
|Enterprise Asset Management for Healthcare|2.0.0|New • None. Changed • Updated application dependency versions to align with the latest supported version of Enterprise Asset Management. Fixed • None. Removed • None.|
|Enterprise Asset Management for Healthcare Advanced|2.0.1|New Added support for ServiceNow Otto for Enterprise Asset Management. Added support for AI-powered enterprise asset request experiences. Added support for AI-powered troubleshooting and repair assistance experiences.|
|Enterprise Data Transform|1.0.2|New • Added the Enterprise Data Transform scoped application. • Added import configuration records for defining supported import targets. • Added source-to-target column mapping. • Added value mapping for imported data. • Added staging and validation before final import. • Added support for reviewing staged data and resolving validation errors. • Added final import processing for Asset and Model data used by the AI Assisted Asset and Model Import experience.|
|Entitlements Verification|6.2.1|Fixed minor defect fixes.|
|Expanded Model and Asset Classes|2.17.1|New Added AI agent field hints \(labels and help text\) for ITAM and EAM tables—including enterprise content model tables, model-to-component relationships, and EAM asset import rows—to improve agent guidance. Introduced default form and list views for Multimedia Production Equipment asset and model classes. Changed The Description field is now mandatory on the Enterprise Content Model Classification table. Fixed Applied non-Glide Cobalt true-up and ACL changes for the expanded product model and asset classes.|
|Export entities|3.4.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Fallout management|8.0.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Fallout management|8.0.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Field Service Management AI agent collection|4.1.0|New No Change Changed No Change Fixed Fixed Fluent conversion issues Removed None|
|Finance and Procurement - Foundation|2.0.0|The application captures dependencies, updated the plugin dependencies for this release.|
|Finance and Procurement - Prime|2.0.0|The application captures dependencies, updated the plugin dependencies for this release.|
|Finance Common Architecture|15.0.0|New: Admins can access SPO Product Admin Home as a single entry point. Product Hub provides guided installation of SPO applications and plugins. Configuration Console offers a guided experience for configuring Procurement Case Management items with completion tracking. From Configuration Console, admins can download update sets and upload batch update sets to higher environments. Changed: SPO configuration is now organized within the Otto for Setup framework, replacing navigation across multiple admin tools and locations. The admin experience is now consistent across Product Hub and Configuration Console.|
|Financials Core|6.2.9|New You can now save your preferred timescope selection on the Financials tab of the project workspace. By default, the system retains the selected timescope for up to 50 recently accessed projects, and admins can raise this limit to up to 200 projects. When you return to a project, your previously selected timescope is restored automatically. Admins can now use a guided setup for financials configuration in Strategic Portfolio Management \(SPM\). The Implementation Accelerator walks admins through configuring labor cost plans, labor cost types, budget allocation, financial baselines, currency settings, investment object linkage, cost plan breakdown rollups, and fiscal calendar settings. You can now view in-context help for key financial fields on the Financials page. Info icons next to each field explain calculations such as planned cost, budget, estimate at completion \(EAC\), Return, ROI, and NPV directly within each widget. Changed Inline editing performance in the financials cost and benefit grid is improved. When you edit and save a single row, only that row refreshes instead of the entire grid. The edited row is locked from further changes until the save completes. This applies to both month and year timescales. Project managers and planning item owners can now recalculate planned cost and benefit values based on updated budget reference rates. A new menu option lets you recalculate all relevant breakdowns at once, with confirmation dialogs and loading overlays to show progress. The previous Recalculate resource cost action is now hidden to avoid duplicate functionality. Fixed Total budget on projects now recalculates correctly when investment budget records are deleted or updated. Multicurrency setup in the project workspace now updates automatically and accurately. Investment record linkage in cost plans and planning items is now consistent across all projects. Converting a demand to a project no longer clears cost in investment currency values. The financials console in the Project Workspace no longer has limitations related to time scope and fiscal range selection.|
|Flow Designer GenAI|30.1.4|Fixed Fixed an issue in MCP for Flow where a property parsing error caused compatibility checks to incorrectly reject non-string data types.|
|Flow troubleshooting agent|1.0.12|New Debug production errors — Surface and diagnose production flow failures that are typically hard to discover and reproduce. Troubleshoot trigger issues in context — Launch the troubleshooting agent directly from the record to investigate trigger-related problems where they occur. Resolve approval errors — Pinpoint what went wrong in approval flows and how to fix it. Answer general flow questions — Ask the agent any flow-related query and get clear, conversational answers. Root cause in minutes — Receive a plain-language summary and root cause analysis in minutes, not hours.|
|Formula builder connected|23.0.2|Removed The workspace\_user role has been removed from the Formula Builder configuration table. This role is no longer available for assignment.|
|FSM - Advanced|2.1.2|New No Change Changed No Change Fixed Fixed Fluent conversion issues Removed None|
|FSM - Foundation|2.1.2|New No Change Changed No Change Fixed Fixed Fluent conversion issues Removed None|
|FSM Scheduling AI Agent Collection|2.0.4|What's New All new AI agent interaction experience powered by ServiceNow Otto Update shifts after they're scheduled — change times, swap technicians, and adjust shift assignments Add and manage technician breaks conversationally, including single occurrences of a recurring break Interactive shift summary card directly in chat Managers/Schedulers can now create shifts directly from Agent Mobile|
|Gantt UI Builder Component|26.1.4|Fixed: Resolved an issue where focus moved unexpectedly to the first table's column headers when using the resizable panes divider handle. Resolved an issue where rollup bars did not accurately reflect the span of actual dates in multi-level hierarchies. Resolved an issue where the timeline bar did not display the label name when the Show Label check box was selected.|
|Generative AI Controller|15.0.3|New: Added support to enable domain separation for AI Control Tower \(AICT\) configurations and controls New: Added support for capability/skill level configurations for PII masking enforcements|
|Goal Framework for SPM|2.10.0|New: New targets default to quarterly check-in frequency, accelerating target creation with a standard quarterly breakdown. Status is now auto-populated when actual values are entered for a target or target breakdown during check-in actuals, streamlining data entry and improving consistency. Configure the status threshold in system properties to define how status values are derived based on actual versus planned target achievement.|
|GRC: Advanced Risk|23.0.6|New Risk assessment projects now support multiple entities. Assessors can perform assessments across several entities within the same project. Comments can now be configured as mandatory in risk assessments. Administrators can set comments as required for individual factors, group factors, and overall assessment types. GRC: Advanced Risk application is now available on IRM Foundation SKU. Changed The licensing strategy for this application has changed from an entitlement model to a plugin identifier model. To access the features you are entitled to, you must install the corresponding SKU identifier application. For example, IRM Professional customers must install the Integrated Risk Management Professional application, and IRM Enterprise customers must install Integrated Risk Management Enterprise. Fixed Fixed an issue where new Risk Event records were created with empty values after an existing Risk Event with entries was deleted. Fixed an issue where risk assessment counts, such as pending and ongoing assessments, were updated with incorrect values when two assessments completed at the same time.|
|GRC: Advanced Risk Assessment|23.0.3|New Risk assessment projects now support multiple entities. Assessors can perform assessments across several entities within the same project. Comments can now be configured as mandatory in risk assessments. Administrators can set comments as required for individual factors, group factors, and overall assessment types.|
|GRC: Approver Configurator|23.0.5|Changed Added a new public API method, evaluateApproversByConfig\(tableName, recordSysId, configSysId\), to the ApproverEvaluation script include. This method evaluates and returns the approver levels for a given record based on a specified approval configuration.|
|GRC: Business Continuity Management - Core|12.0.3|\*\*New\*\* Group ownership fields for BIAs, Plans, Events, and Action Items - Business Continuity Managers can now assign owner groups to Impact Analysis records, Plans, Events, and Action Items. Owner selection is filtered by group membership, and either owner or owner group is mandatory. Group members with edit access can manage these records. Recovery Teams management and hierarchy - Business Continuity Managers can now create, view, and manage recovery teams with configurable hierarchy levels, cycle prevention, and multi-level parent/child relationships. Recovery teams can be referenced in plans and filtered by active status. Recovery Teams are now accessible via a dedicated navigation menu under BCM administration Collaboration enhancement - Create collaboration threads within events to assign action items, track impacted assets, and communicate directly with team members. Auto-populate email recipients from recovery team membership for notifications. Propagate all team actions to the event activity stream for a complete visibility into the response timeline. Users can access inbound emails sent in response to composed emails and reply directly within the system. Issues for Events and Plans - Business Continuity Managers can now add, view, and manage issues directly from the event, plan record. Issue records now support related lists for events and plans \*\*Changed\*\* PDF and Word template updates - Export templates for Plans, BIAs, and Events have been updated to include group ownership fields, issues for plans and events, collaboration threads, Recovery teams with improved layout alignment and defect fixes. Plan and Collaboration recovery team selection - Recovery teams can be reused as they are global and not tied to plan anymore.Only active recovery teams are now shown when selecting recovery teams in Plans and Collaborations. Inactive teams are excluded from picker and server-side validation. Assignment details section in BIA and Plan forms - The owner group field is now the first field in the Assignment details section, with annotation indicating owner or owner group is mandatory. My Tasks report enhancements - The My Tasks page now includes tabs for group ownership records, showing BIAs, Plans, Events, and Recovery Tasks assigned to the user or their group. Plan contributor and BIA planner role enhancements - Plan contributors and BIA planners can now create and edit Plans and BIAs, with field write access in Draft state and improved group-member write logic. \*\*Fixed\*\* Update dependencies performance issues.|
|GRC: Business Continuity Planning|12.0.7|\*\*New\*\* Assign group ownership to business impact analysis, plan, and event records Enable group ownership for plan records along with individual ownership. Use the My group's pending tasks and My group's items tabs, added to the My Tasks page, to view group-owned records. Import and export recovery tasks from Microsoft Excel Upload recovery tasks in bulk using Microsoft Excel files, with row-level validation and error handling. Microsoft Excel columns are mapped to recovery task fields, to validate data integrity, support updates to existing tasks, and insert new tasks in the same import. Use the Export to Excel action to download current recovery tasks as a Microsoft Excel workbook for offline editing or sharing. Transform history and Import log related lists provide traceability of the most recent import run, including row-level errors and skipped records. Reorder recovery tasks using Gantt timeline and dependency links- Users can reorder tasks in Gantt view by linking dependencies, with drag-and-drop actions and error handling messages. Planners can update task order for their plans, and program managers for all plans. \*\*Changed\*\* Recovery teams can be created at global level and utilized in the plan.|
|GRC: Business Impact Analysis|12.0.5|\*\*New\*\*Group ownership for BCM records is now supported - Customers can assign a group of users as owners for Business Impact Analyses \(BIAs\), Plans, and Event records in the BCM application.Collaborator synchronization for BIAs using Smart Assessment templates. When a BIA is created from a Smart Assessment template, the group owners and contributor list are automatically sync to Smart Assessment \(SAE\) instance. The Owner group manager will map to the SAE assessment owner\(BIA owner will sync as assessment owner if exist\), and other group members , contributors added to SAE collaborators. \*\*Changed\*\*• \*\*Contributor synchronization from BIAs to Smart Assessment instances has been enhanced.\*\* When the BIA contributor list changes, the SAE collaborator list is updated to match, excluding the owner. \*\*Fixed\*\*• SAE customer-reported issues have been resolved. Synchronization from BIA owner and contributors to SAE collaborators now works as expected, including proper handling of contributor overlap and group changes.|
|GRC: Common Workspace Elements|23.0.9|Changed Otto branding and icon updates are now available across GRC Workspace experiences. References to "Now Assist" are replaced with "ServiceNow Otto" in workspace elements, including updated labels and icons in the user interface. "Now Assist" has been renamed to "ServiceNow Otto" in client scripts and base workspace experiences. All client-side scripts and UI elements now reflect the new ServiceNow Otto branding, including icon and label updates in the base workspace \(Australia version\). Fixed Security fixes close ACL-bypass and unauthorised-write holes across GRC data brokers, GlideRecord → GlideRecordSecure, or add explicit canRead/canWrite checks The Approve/Reject button is now visible on the Privacy and Compliance workspace. The policy exceptions widget in the overview now correctly displays exceptions expiring in 7 days based on the intended condition. The stepper in Compliance Workspace now displays labels based on the session language, not the system language. UI improvements. The 'Tasks' and 'Last Updated' sections no longer overlap during tab transitions in the Australia version. Task page load time has been improved by removing individual group caching from the work queue. Only "all groups" data is cached; group-specific requests are handled directly by the database.|
|GRC: Compliance Assessment|23.0.2|Changed Migrated query range access controls to conditional plugin structure for app compatibility with the Zurich release.|
|GRC: Crisis Management|12.0.5|\*\*New\*\* Enhanced Collaboration between recovery teams during crisis : BCM users can create and manage recovery teams with users, groups, and hierarchies for coordinated crisis response. Tag events by escalation level \(Site, Regional, Corporate, Global\) and link recovery teams to track who's involved at each level. Create collaboration threads within events to assign action items, track impacted assets, and communicate directly with team members. Auto-populate email recipients from recovery team membership for frictionless notifications. Propagate all team actions to the event activity stream for a complete visibility into the response timeline. \*\*Fixed\*\* • Assessment instances are cancelled when Action items are deleted. • Hardened security by updating glide record secure for MRA modal api calls.|
|GRC: Crisis Management integration with Everbridge Notifications|12.0.7|\*\*Fixed\*\* Hardened security by updating glide record secure for MRA modal api calls.|
|GRC: Crisis Map|12.0.5|\*\*Fixed\*\* Crisis Map Performance Optimization - Dismissed alerts now load efficiently using a 30-day default window. Administrators can extend the time range as needed to optimize Crisis Map loading performance.|
|GRC: Metrics|23.0.5|New Admins can now configure notification redirection for metric data tasks and composite definitions. Email notifications for metric data tasks and metric hierarchies now use the platform’s notification redirection framework, ensuring recipients land on the correct workspace or Classic view based on access. Campaign workflows now support handling unpublished states and entity/metric removal. Campaigns update data owner and first run date only after publishing, display clear messages when metrics or entities are removed, and prevent deletion of campaign cycles once published. Changed Filter count on MDT page now includes campaign filters. The filter button on the MDT page accurately reflects the total number of applied filters, including those from campaigns. Fixed Error messages caused by metric definition ACLs on the control form have been resolved. Metric data list configuration now displays distinct labels for fields from different metric definition references, eliminating ambiguity.|
|GRC: Policy and Compliance Management|23.0.2|Fixed Migrated query range access controls to conditional plugin structure for app compatibility with the Zurich release. Fixed Policy Exceptions auto-closing after the Valid to date expires Resolved 'Next run date' in IRM indicators being read-only in the Australia version Fixed error appearing in the Extension date field when extending policy exceptions Resolved error in policy review flow when adding deny listed roles Fixed incorrect role validation in Copy entity frequency UI action on Control records Fixed Policy Exception workflow to reflect extension Resolved Effective Date validation on control objectives incorrectly flagging the current date as past Granted Compliance Library Reader and Compliance Reader roles access to Policy category Added indexing to sn\_grc\_item\_generation\_action\_event\_queue queries|
|GRC: Profiles|23.0.7|New Users can now add existing standalone issues as child issues directly from the Child Issues related list. An "Add" button is available in the related list header for users with write access, opening a modal dialog to search and select multiple standalone issues to link as children. Only issues without a parent and not already grouped are shown, preventing circular references. The related list refreshes automatically after linking, and audit logs are created for both parent and child issues. Child Issues modal supports template-based filtering and bulk actions. When managing parent issues, only standalone issues with the same template are shown. When managing child issues, all standalone issues are available. Users can add or remove child issues in bulk, and previously removed issues can be re-attached. Fixed The "Close" label in Risk Workspace state steppers now translates correctly based on session language. State labels are resolved from platform choice values, ensuring proper localization. Inactive entity filters are no longer processed when the related entity type is active, preventing incorrect filter application. The function for clearing discrete fields now uses the correct parameter, ensuring robust behavior and preventing errors from undefined variables. Invalid tables in the entity filter mapping no longer cause GRC profile generation jobs to fail. The system now checks for table existence before attempting deletion. The GRC Profiles UI Action script method no longer overwrites the global UI action script method, preserving expected UI action behavior. Indicators are now properly inactivated when the associated control is manually retired, ensuring consistent indicator status.|
|GRC: Risk Management|23.0.3|New Added support for the Risk Admin role to create Smart Assessment question banks, and for the Risk Manager role to read them. Fixed Fixed an issue where Business User Lite users could not access the My Attestations module in Service Portal. Fixed translation issues on the Continuous Risk Monitoring Overview dashboard.|
|GRC: Risk Shared Common Components|23.0.5|Fixed Addressed an ACL bypass issue in the Get Table Record Fields data broker. Fixed KB article hyperlink spacing issues and empty-role ACL issues on the document version table. Resolved an issue that caused the node map to break when viewing the user hierarchy. Fixed the import progress model to display the correct tracker details.|
|GRC: taxonomy management|23.0.2|New Improved protection against unauthorised query-based data discovery. ACL behaviour across new installs, upgrades, and true-up releases. Reduced operational dependency on manual remediation activities. Zurich and Australia compatibility maintained for supported store applications.|
|GRC: Vendor Portal|23.0.5|New Added element assessment support in the Vendor Portal. Added the Vendor Portal elements grid with breadcrumbs. Migrated the SAE questionnaire widget to embeddable components. Changed Added task-type-based Manage Elements controls. Improved vendor reviewer controls and assessment reassignment. Updated localized Vendor Portal content. Fixed Corrected follow-up filter behavior \(PRB2069551\). Restored smart assessment questions for vendor issues \(PRB2060073\). Corrected questionnaire state transitions after return \(PRB2034307\).|
|GRC: Vendor Risk Management Workspace|23.0.5|New Added elements grid and element management. Added element risk ratings and improved related-list behavior. Added accessibility improvements across workspace pages. Changed Added persona-based access to elements grids. Updated task navigation and renamed Tasks to External Tasks. Improved third-party and engagement element workflows. Updated vendor, AI model, and workspace metadata behavior. Added risk-admin access controls and secure query handling. Fixed Fixed dynamic column labels and element-grid feedback \(PRB2057733\). Corrected third-party prepopulation when creating elements \(PRB2057048\). Fixed missing element actions and routes \(PRB2036126, PRB2024156, PRB2030772\). Corrected assessment attachments and questionnaire filtering \(PRB2026795, PRB2028131\). Fixed approval actions and workspace access controls \(PRB2012105, PRB2017761\). Corrected missing tooltips and UI rendering issues \(PRB2023846\).|
|GRC Case Management Core|23.0.2|New Improved protection against unauthorized query-based data discovery. Consistent ACL behavior across new installs, upgrades, and true-up releases. Reduced operational dependency on manual remediation activities. Maintained Zurich and Australia compatibility for supported store applications.|
|GRC Change Management Core|23.0.3|This is the initial version of the plugin. It is a technical plugin and should not be available in the Store.|
|GRC Common GenAI|23.0.5|Fixed: Otto branding and logo changes|
|GRC Feature roles|23.0.3|Changed Migration of query range access controls to appropriate conditional plugin structure to allow app compatibility with Zurich|
|GRC Shared GenAI|23.0.2|New Added refinement actions for risk assessment summaries: Executive Summary: Refines summaries for executive-level audiences Shorten: Produces concise summaries Added Authorization package summarization, a generative AI skill that generates summary paragraphs indicating the package's current state by combining system purpose, impact, operational status, and open Plan of Action and Milestones \(POAM\) counts. Available to users with the CAM Gen AI role with a Save to Work Notes option. AI-Powered Privacy &amp; AI Assessment Recommendations: Privacy &amp; AI Asset assessment tasks now auto-generate AI-recommended control objectives and risk statements with intelligent suggestion guides when moved to Review state Accept or reject recommendations to streamline compliance scoping. Approved items automatically map to associated processing activities or AI assets|
|Group-Action Framework|8.0.6|--- AI Generated Release Notes --- New Users can now classify items within GAF using Group Capability \(Topic\), enabling enhanced organization and management of records. System administrators can manage classification settings related to Group Capability \(Topic\). All third-party models are now supported for GAF KB Gap HR skills, expanding model selection options for skill processing. Taxonomy fields have been added and populated in the record group table for the KB GAP HR pipeline, allowing for improved categorization and searchability. Record groups are now replicated in action strategies for the KB GAP HR pipeline, ensuring consistent grouping across workflow actions. Topic generation can now run as the same user as the scheduled job, aligning execution context for automated topic creation. Changed Incremental clustering for Agent Advisor now includes a refinement handler, improving noise clustering and prediction accuracy. The workflow has been updated to support filtering of the highest group in the group record table with an optional configuration flag. Incremental clustering implementation for Agent Advisor has been enhanced with noise clustering logic, input query filtering, and threshold adjustments for improved data grouping and workflow performance. Fixed The HR GAF Group job now triggers correctly when the 'snhrcore.admin' role is removed from 'admin', ensuring group processing reliability. Field-level report view access control has been restored, allowing users with the data report viewer role to access additional data tables in dashboard visualizations. Skill Run Info for Agent Advisor has been corrected, resolving issues in the skillruninfo table query and ensuring accurate skill run data.|
|Guidance|45.0.2|New: Recommended actions now support the new Attach Knowledge and Relevant Case guidances for AI Search results that surface on CRM workspace.|
|Hardware Asset Management|16.0.1|New Automated entitlement detection and reporting for ITAM and HAM applications: Administrators can now view and export entitlement consumption reports for out-of-the-box applications, with notifications for undisclosed usage. AI Native HAM Prime SKU with bundled contract management and AI-driven asset operations: Licensed customers can access advanced contract lifecycle management, autonomous asset operations, and AI-powered asset replacement workflows, all gated by entitlement checks. NextWave ServiceNow Otto panel enablement for Hardware Asset Management: Fulfillers can now access and test the ServiceNow Otto panel in HAM workflows, with operational validation and support for accessibility standards. Visual regression testing for accessibility compliance in ITAM Asset Management Workspace: All updated components undergo systematic visual regression testing to ensure WCAG 2.2 Level AA conformance, with defect remediation prior to release. Service Catalogue migration to Angular for hardware catalogue items: End users and Service Desk agents can access, request, and process hardware catalogue items in the Angular environment, with validated workflows and UI consistency. Changed Workflow dependency removal in HAM and ITAM test projects: Test projects now create their own data and run independently of demo data workflows, improving test stability and execution time. Gradle migration for select test projects: Test projects for asset repair, reclamation, lease contract expiration, and procurement have been migrated to Gradle for improved build consistency. Java 21 compile upgrade for HAM and associated libraries: All impacted repositories and libraries now compile with Java 21, resolving method conflicts and ensuring compatibility with updated dependencies. Accessibility improvements for Classic UI and HAM workspace: UI elements such as images, table grids, and popups have been updated to conform to 400% zoom accessibility guidelines, ensuring proper rendering and usability. Demo data creation optimization for HAM workflows: Demo data creation processes for loaner, donation, disposal, contract renewal, and RMA orders have been streamlined, allowing efficient XML import and Flow Designer context management. Fixed Issues with creating shipping carriers in the Hardware Asset Workspace have been resolved. Advanced shipment notifications now auto-populate the order date on hardware assets during ASN import when a purchase order exists. Asset import no longer truncates model names; the maximum length is now correctly handled during bulk asset import. Duplicate asset creation has been resolved when the IRE property is disabled; serial number values are now set correctly. The HAM On-prem Run Import UI action now triggers the import process when the content type is application/x-zip-compressed. Orders are now processed correctly even if the start date passes without successful allocation. Out-of-box scripts no longer revert the sys\_user form to previous versions. Custom hardware models can now be created even if an inactive model with the same number exists in the Content Library. Deactivating an Inventory tab now removes both the UI element and its backend data from the Data Broker. Asset refresh utilities now correctly consider CSDM Lifecycle migration status when determining replacement models.|
|Hardware Asset Management - Advanced|1.0.11|This version enables Hardware Asset Management Advanced customers to install and upgrade through the Hardware Asset Management Product Hub.|
|Hardware Asset Management - Prime|1.0.13|This version introduces new AI native Hardware Asset Management Prime, delivering end-to-end asset lifecycle management with the following capabilities: AI-powered hardware model content and normalization Automated asset tasks—deploy, swap, and retire Asset inventory audits and performance reporting Contract renewal workflow and contract management professional integration Asset warranty integration with Lenovo and total cost of ownership tracking Remote asset receiving, stockroom receiving, and asset putaway workflows Asset attestation and inventory reports Hardware asset dashboard with operational visibility Service locations and distribution channels support for stockroom operations Indoor mapping capability for asset location tracking Shipping carrier integration for asset logistics Asset pallet management and receiving—my assets workflows Licensing support for new resource categories Hardware Asset Management maturity assessment Hardware Asset Management for Zero Touch Mobility|
|HCLS - Advanced|3.2.0|New Enhancements to provide better support for agentic engineering.|
|HCLS - Advanced|3.2.0|New Enhancements to provide better support for agentic engineering.|
|HCLS - Foundation|3.1.0|New Enhancements to provide better support for agentic engineering.|
|HCLS - Foundation|3.1.0|New Enhancements to provide better support for agentic engineering.|
|HCLS - Prime|3.1.0|New Enhancements to provide better support for agentic engineering.|
|HCLS - Prime|3.1.0|New Enhancements to provide better support for agentic engineering.|
|HRSD - Advanced|2.2.5|Licensing app for Advanced SKU|
|HRSD - Foundation|2.2.5|Licensing app for foundation SKU|
|HRSD - Prime|2.2.5|Licensing app for Prime SKU|
|HR Voice AI Agents|2.3.14|Fixed Issue where the ZoHo agent wasn't always retrieving expenses properly. Issue with the HR Case Creator agent not always finding an existing case if applicable.|
|Human Resources: Service Portal|44.3.1|Updated to support the latest version of the dependent apps.|
|Impact|11.0.3|Exception governance improvements Scan Engine's exception-handling workflow has been hardened: Draft/Submit actions replace the old "Request Approval" checkbox, with clear status badges on exception findings A dedicated exception-approver role separates approval authority from dashboard access One-click navigation from an exception record to the scanned record Exception creation is now supported directly from ACT findings raised via update sets Adoption Starter Experience enhancements Continued rollout of the Impact Adoption Starter Experience, including refreshed application/taxonomy lists, an updated Capabilities Map with editable notes, and clearer messaging when full functionality requires Service Bridge. Improvements Reprocessed and upgraded 543 legacy Health Assessment definitions into release-quality Scan Engine Definitions, improving finding accuracy and adding customer-facing "what it means" context Outcome Insights and Value Story Builder: improved metric labeling and reporting support Improved audit trail on Scan Engine findings, including tracking which update set introduced a given finding Fixed Issues Outcome Insights &amp; Capabilities Map Fixed incorrect product information displayed in Outcome Insights filters and side panels Fixed inconsistent footer length on report cards and banner message display issues Fixed duplicate capabilities appearing in the Capabilities Map Fixed inability to generate value reports Scan Engine &amp; Exception Handling Fixed a race condition allowing concurrent scan requests to bypass the running-scan check Fixed full-scan findings being created with a blank scanned record due to a filter leak Fixed real-time scans deleting finding records generated by full/delta scans Fixed Scan Engine failing an entire batch instead of skipping a table on cross-scope access denial Fixed exception reasons showing "Empty" with related records incorrectly marked "No Longer Required" Fixed exception approvals being granted from list view despite mandatory approval comments Fixed the Findings panel showing a stale "Create Exception" button after reopening a finding that already has an exception Fixed approval comments and approver not syncing from production to lower environments Fixed a broken "View Definition" link in the Developer Dashboard's exception tab Accessibility Fixed color contrast on warning messages and view-findings links Fixed missing accessible names on iframes and frames Fixed missing discernible button text Fixed the findings-panel tab bar exposing all filter buttons in the tab sequence instead of one Other fixes Fixed intermittent failures in statistical scans Fixed a data migration issue causing missing inserts on a subset of records Fixed work notes not migrating correctly Fixed meeting state not updating in Impact Fixed the Accelerator Setup Form getting stuck in a refresh loop Fixed several security vulnerabilities related to script include access control and exception-reason approval bypass \(details withheld per standard security disclosure practice\)|
|Impact Common|11.0.2|Exception governance improvements Scan Engine's exception-handling workflow has been hardened: Draft/Submit actions replace the old "Request Approval" checkbox, with clear status badges on exception findings A dedicated exception-approver role separates approval authority from dashboard access One-click navigation from an exception record to the scanned record Exception creation is now supported directly from ACT findings raised via update sets Adoption Starter Experience enhancements Continued rollout of the Impact Adoption Starter Experience, including refreshed application/taxonomy lists, an updated Capabilities Map with editable notes, and clearer messaging when full functionality requires Service Bridge. Improvements Reprocessed and upgraded 543 legacy Health Assessment definitions into release-quality Scan Engine Definitions, improving finding accuracy and adding customer-facing "what it means" context Outcome Insights and Value Story Builder: improved metric labeling and reporting support Improved audit trail on Scan Engine findings, including tracking which update set introduced a given finding Fixed Issues Outcome Insights &amp; Capabilities Map Fixed incorrect product information displayed in Outcome Insights filters and side panels Fixed inconsistent footer length on report cards and banner message display issues Fixed duplicate capabilities appearing in the Capabilities Map Fixed inability to generate value reports Scan Engine &amp; Exception Handling Fixed a race condition allowing concurrent scan requests to bypass the running-scan check Fixed full-scan findings being created with a blank scanned record due to a filter leak Fixed real-time scans deleting finding records generated by full/delta scans Fixed Scan Engine failing an entire batch instead of skipping a table on cross-scope access denial Fixed exception reasons showing "Empty" with related records incorrectly marked "No Longer Required" Fixed exception approvals being granted from list view despite mandatory approval comments Fixed the Findings panel showing a stale "Create Exception" button after reopening a finding that already has an exception Fixed approval comments and approver not syncing from production to lower environments Fixed a broken "View Definition" link in the Developer Dashboard's exception tab Accessibility Fixed color contrast on warning messages and view-findings links Fixed missing accessible names on iframes and frames Fixed missing discernible button text Fixed the findings-panel tab bar exposing all filter buttons in the tab sequence instead of one Other fixes Fixed intermittent failures in statistical scans Fixed a data migration issue causing missing inserts on a subset of records Fixed work notes not migrating correctly Fixed meeting state not updating in Impact Fixed the Accelerator Setup Form getting stuck in a refresh loop Fixed several security vulnerabilities related to script include access control and exception-reason approval bypass \(details withheld per standard security disclosure practice\)|
|Impact Content|11.0.1|Exception governance improvements Scan Engine's exception-handling workflow has been hardened: Draft/Submit actions replace the old "Request Approval" checkbox, with clear status badges on exception findings A dedicated exception-approver role separates approval authority from dashboard access One-click navigation from an exception record to the scanned record Exception creation is now supported directly from ACT findings raised via update sets Adoption Starter Experience enhancements Continued rollout of the Impact Adoption Starter Experience, including refreshed application/taxonomy lists, an updated Capabilities Map with editable notes, and clearer messaging when full functionality requires Service Bridge. Improvements Reprocessed and upgraded 543 legacy Health Assessment definitions into release-quality Scan Engine Definitions, improving finding accuracy and adding customer-facing "what it means" context Outcome Insights and Value Story Builder: improved metric labeling and reporting support Improved audit trail on Scan Engine findings, including tracking which update set introduced a given finding Fixed Issues Outcome Insights &amp; Capabilities Map Fixed incorrect product information displayed in Outcome Insights filters and side panels Fixed inconsistent footer length on report cards and banner message display issues Fixed duplicate capabilities appearing in the Capabilities Map Fixed inability to generate value reports Scan Engine &amp; Exception Handling Fixed a race condition allowing concurrent scan requests to bypass the running-scan check Fixed full-scan findings being created with a blank scanned record due to a filter leak Fixed real-time scans deleting finding records generated by full/delta scans Fixed Scan Engine failing an entire batch instead of skipping a table on cross-scope access denial Fixed exception reasons showing "Empty" with related records incorrectly marked "No Longer Required" Fixed exception approvals being granted from list view despite mandatory approval comments Fixed the Findings panel showing a stale "Create Exception" button after reopening a finding that already has an exception Fixed approval comments and approver not syncing from production to lower environments Fixed a broken "View Definition" link in the Developer Dashboard's exception tab Accessibility Fixed color contrast on warning messages and view-findings links Fixed missing accessible names on iframes and frames Fixed missing discernible button text Fixed the findings-panel tab bar exposing all filter buttons in the tab sequence instead of one Other fixes Fixed intermittent failures in statistical scans Fixed a data migration issue causing missing inserts on a subset of records Fixed work notes not migrating correctly Fixed meeting state not updating in Impact Fixed the Accelerator Setup Form getting stuck in a refresh loop Fixed several security vulnerabilities related to script include access control and exception-reason approval bypass \(details withheld per standard security disclosure practice\)|
|Impact Health Content|6.0.3|New As part of the ongoing modernization of Platform Health content, 244 Scan Engine definitions have been introduced, including migrated Health Assessment content and new platform health definitions. These definitions include a combination of system property validations, statistical analysis checks, conditional rule evaluations, and custom script-based assessments, expanding coverage across platform health, governance, and configuration standards. 150 definitions are global and apply to all customer instances. 94 definitions are associated with specific ServiceNow applications or plugins and are evaluated only when the corresponding application is installed and active.|
|Impact Value Management - APM|2.2.0|Compatible: Zurich, Australia, Brazil|
|Impact Value Management - App Engine|2.2.0|Compatible: Zurich, Australia, Brazil|
|Impact Value Management - CSM|2.2.0|Compatible: Zurich, Australia, Brazil|
|Impact Value Management - HR|4.1.0|Compatible: Zurich, Australia, Brazil|
|Impact Value Management - IRM|3.1.0|Compatible: Zurich, Australia, Brazil|
|Impact Value Management - ITAM|1.0.1|As part of this update, the HAM \(Hardware Asset Management\) and SAM \(Software Asset Management\) data collection apps are being consolidated into a single, unified ITAM app on the ServiceNow Store, listed under the new IT Asset Management product category. If you previously used the separate HAM and SAM apps, you will now find both capabilities in this one app, all of your historical data and configuration will carry over automatically, with nothing lost in the transition. This change only affects how the apps are organized and presented; the underlying data collection functionality itself remains unchanged. Compatible: Zurich, Australia, Brazil|
|Impact Value Management - ITOM|3.1.0|Compatible: Zurich, Australia, Brazil|
|Impact Value Management - ITSM|5.1.0|Compatible: Zurich, Australia, Brazil|
|Impact Value Management - SECOPS|3.1.0|Compatible: Zurich, Australia, Brazil|
|Impact Value Management - SPM|3.1.0|Compatible: Zurich, Australia, Brazil|
|Incident Communications Management for Service Operations Workspace|9.4.2|-Compatible with latest ServiceNow release|
|Incident Management for Service Operations Workspace|9.4.2|Changed: Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.|
|Industrial Core|4.1.6|Fixed Security fixes|
|Industrial Process Manager|4.2.5|Fixed Security fixes|
|Industrial Workspace Common|4.2.4|Fixed Fixed the dot-walk and extended fields view in the Industrial Workspace \(PRB1967015\)|
|Insights Clustering Utils|3.4.1|New Added detailed error messaging during precheck validation Added ITIL role support for precheck configuration Changed Intent clustering failures now surface as visible errors in Agent Miner \(previously silent/log-only\) Fixed No major fixes Removed Nothing removed in this release|
|Integrated Risk Management Advanced|23.0.1|Fixed: Otto branding changes and logo changes|
|Integrated Risk Management Enterprise|23.0.2|Fixed Entitles users to enterprise IRM features and applications such as Policy and Compliance, Risk management, Case management, Profiles and more on multiple family patch upgrades like Australia Patch 5, Zurich Patch 12 and Brazil etc|
|Integrated Risk Management Foundation|23.0.0|Fixed: Otto branding and logo changes|
|Integrated Risk Management Prime|23.0.1|Fixed: Otto branding changes.|
|Integrated Risk Management Professional|23.0.2|New Zurich Patch 12 and Australia Patch 5 and Brazil compatibility maintained for supported store applications|
|Integrated Risk Management Standard|23.0.2|Fixed Entitles users to standard IRM features and applications such as Risk management, Case management, Profiles and more on multiple family patch upgrades like Australia Patch 5, Zurich Patch 12 and Brazil etc|
|Integration Commons for CMDB|2.26.0|New Added default Data Manager template for retire and delete functions. Added Data source level error in SGC Central Error tab. Added a function to return Mac Address for SG-GCP deep discovery. Fixed Disabled edit option for fields in the sn\_cmdb\_int\_util\_cmdb\_integration\_execution\_error and sn\_cmdb\_int\_util\_service\_graph\_connections\_state tables. Fixed import error details that didn't appear in SGC Central for parallel loading. Fixed the error message for test connection failure scenario. Improved performance for software record removal for SG-Tanium. Migrated to an alternative mechanism instead of relying on sys\_flow\_context business rule. Fixed the Cleanse IP Version RTE Operation when invoked with a dash-separated IP address parameter. Fixed the scenario where non-concurrent import sets created duplicate CMDB Integration Execution \(CEX\) records. Fixed incorrect version extraction in CmdbIntegrationSoftwareModelUtil when the software name ends with a number.|
|Intelligent Approvals|3.0.10|New Human in the loop- condition builder support Knowledge Base article as a source to Intelligent approval policy Fixed Defects Tech debt|
|Interaction Management for Service Operations Workspace|9.4.2|Changed: Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.|
|Interceptor UI for Service Operations Workspace|9.4.2|Compatible with latest ServiceNow release|
|Investigation Framework|9.4.2|-Compatible with latest ServiceNow release|
|Invoice Case Management|13.2.4|Support email exclusion rules for case creation: Enable AP teams to define and auto-enforce email suppression rules that filter non-invoice emails \(confirmations, OOO replies, duplicates\) before case creation Manual Case Reopening: Reopen closed case enables AP teams to manually restore closed invoice cases to WIP status while preserving all historical context and data, eliminating the need to create duplicate cases for recurring issues.|
|Invoice Case Self-Service|1.7.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Invoice Case Self-Service|1.7.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Invoice Self-Service|1.5.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Invoice Self-Service|1.5.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|IRM Compliance GenAI|23.0.3|New Alert summarization is now enabled for all alert states. Overview now includes alert summary with additional fields and related list data. Added Prompt tuning and third-party model support for alert summarization. Changed Updated prompt logic and scope for alert summarization.|
|IRM Risk GenAI|23.0.2|New Added refinement actions for risk event summaries: Executive Summary, which refines the summary to be executive-ready. Shorten, which produces a more concise summary. Changed Risk event summaries are now fully prompt-based, replacing the earlier scripted-plus-prompt approach. This makes customization easier. The scripted approach is deprecated. By default, risk events are summarized using the latest prompt. To revert to the scripted approach, follow the steps in the KB article. Support for the scripted approach will be removed in a future release, and only the prompt-based approach will be supported.|
|ISA Equipment Model|4.1.1|N.A|
|ITOM - Advanced|1.1.5|New LEAP Multi-taxonomy automation projects LEAP can be configured to ingest and analyze incidents from multiple taxonomies to produce clusters and automation opportunities for all configured taxonomies. Existing single-taxonomy deployments are unaffected. Multi-taxonomy can be configured by admins using LEAP Properties. Generate LEAP knowledge base articles When creating a KB article from a LEAP automation opportunity, users are prompted to select a knowledge base and category before the article is published, with the author field and article metadata auto-populated from the opportunity record. Admins can configure an list of eligible knowledge bases in LEAP Properties to control which options appear in the modal. LEAP MCP Server LEAP skills are now accessible to external clients through MCP tools, enabling integration with third-party systems and workflows. AI Agents for Discovery Pattern diagnostic agentic workflow displays error codes when root causes are classified and provides enhanced remediation suggestions when the Error Framework plugin is active with mapped remediations. Pattern diagnostic agentic workflow log analysis covers the last five days and automatically expands to 30 days when no results are found in the initial period. ITOM URL Discovery You can now limit the number of URLs discovered through Broad URL Monitoring by using the new \[sn\_acc\_vis\_content.full\_url\_discovery\_daily\_max\_rows\] system property. Changed LEAP Hide archived automation opportunities Automation opportunities \(AOs\) from an earlier GAF \(Group Action Framework\) run are now hidden by default. Previously, old AOs with resolution steps remained visible in the workspace after remapping. It was difficult to distinguish actionable AOs from old ones. After a GAF re-run, the old AOs are archived and no longer appear on the homepage. The artifacts of archived AOs are mapped to relevant new AOs. LEAP value dashboard expansion The LEAP value dashboard now surfaces metrics for all automation outcome types along with existing playbook data. New sections display Ansible execution counts, agent-hours saved, and top playbooks by tickets resolved, KB article creation counts and top contributing clusters, and problem record \(PRB\) creation counts and top clusters. A summary at the top of the dashboard breaks total automation activity and savings attribution by outcome type such as LEAP playbooks, Ansible playbooks, KB articles, and PRBs, each with a trend indicator. AI Agents for Service Level Objective SLO Creator Agent now supports commitment-aware SLO generation and integrated risk calculation. The SLO Creator Agent operates with updated V2 instructions, enabling new skills for generating SLOs that account for commitments and utilizing a risk calculation tool. The implementation aligns with the SLO Gap Agent to ensure consistent behavior and parity. Fixed AI Agents for Discovery Security defects in the Certificate Management Renewal AI Agent have been resolved. ITOM URL Discovery Navigation issues with bulk upload of the URLs are resolved. Removed LEAP The Now LLM Service is no longer the default model provider for new or inactive AI assets. A third-party LLM is now selected by default, while existing configurations using the Now LLM Service continue unchanged. The Now LLM Service is still available for manual selection.|
|ITOM - Prime|1.2.2|ITOM - Prime provides the following capabilities: AIOps AI Specialist - controlled availability AI agents for AIOps - Automate alert triage, impact analysis, and root cause investigation with an AI-driven agentic workflow that transforms manual operator processes, typically 30+ clicks and 15+ minutes, into a streamlined, autonomous flow. The workflow processes incoming IT alerts end-to-end, correlating observability data, analyzing affected services, and identifying probable root causes before an operator touches the alert. Consolidated insights are surfaced through the Express List interface, giving operators immediate visibility into what happened, what's affected, and recommended next steps, enabling faster resolution while keeping humans in control of final decisions. AI agents for Observability - Helps IT operators assess business and application service impact, formulate probable cause theories, and prioritize investigations by analyzing data from ServiceNow and seamlessly collaborating with third-party AI agents from leading APM and observability vendors, including New Relic, Dynatrace, and Kentik. Using natural language, IT operators can understand the blast radius of an alert, pinpoint affected services, assess business impact, formulate probable cause theories, and help track down the right teams to drive towards problem resolution. AIOps Learning Enhanced Automation Playbooks - Leverages AI-driven insights to mine historical incident data, dynamically prioritize tasks, and generate actionable resolution playbooks. By automating workflows and enhancing knowledge sharing, AIOps Learning Enhanced Automation Playbooks empowers teams to address issues proactively and efficiently. It reduces mean time to resolution \(MTTR\), increases automation coverage, streamlines processes like certificate renewals, and improves team productivity. This ultimately leads to measurable cost savings and operational excellence. AI agents for HLA - Automate the most complex and time-consuming steps in setting up and operating HLA — mapping business context, classifying log fields, and investigating alerts. Powered by Now Assist, these agents bring AI-driven recommendations directly into HLA workflows, reducing the expertise required to configure the system and helping operators respond to alerts faster and more confidently. AI agents for SLO - Automates the creation of service level objectives \(SLOs\) based on operational data for services and configuration items \(CIs\), helping teams adopt SLOs faster and improve service reliability.|
|IT Service Management|3.3.1|New AppSee telemetry integration Track real-time usage patterns and user interactions across the ITSM Fulfiller Experience UI pages to optimize experience and identify adoption gaps.|
|IT Service Management Advanced|3.3.1|Changed No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.|
|ITSM Admin Experience|3.3.3|New AppSee telemetry integration Track real-time usage patterns and user interactions across the ITSM Fulfiller Experience UI pages to optimize experience and identify adoption gaps.|
|ITSM Admin Experience Components|3.3.1|Changed No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.|
|ITSM - Advanced|2.3.11|New - None Changed - None Fixed - None Removed - None|
|ITSM - Advanced|2.3.11|New - None Changed - None Fixed - None Removed - None|
|ITSM Advanced Admin Experience|3.3.3|Changed No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.|
|ITSM Change Admin Experience|1.3.0|Changed No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.|
|ITSM Employee Experience|3.3.1|Changed No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.|
|ITSM - Foundation|2.3.11|New - None Changed - None Fixed - None Removed - None|
|ITSM - Foundation|2.3.11|New - None Changed - None Fixed - None Removed - None|
|ITSM Fulfiller Experience|3.3.1|Changed No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.|
|ITSM - Prime|2.3.11|New - None Changed - None Fixed - None Removed - None|
|ITSM - Prime|2.3.11|New - None Changed - None Fixed - None Removed - None|
|Knowledge Capabilities in UI Builder|30.6.3|September release|
|Knowledge Center|31.26.5|defect fix|
|Knowledge Graph|8.3.3|Improved search results accuracy with enhanced Knowledge Graph integration in ServiceNow Otto Panel, ServiceNow Otto Virtual Agent, and Agentic AI applications.|
|Knowledge Graph Affinity Signals|1.0.1|Affinity Signals is a new personalization engine that automatically learns what matters to each user and personalizes search result ranking in AI Search. Search results adapt to your role, team, and activity patterns.|
|KPI Framework|7.0.0|New Supplier comparison insights are now available in the contextual side panel. Users can now compare suppliers based on industry, segment, and region, showing score, risk, spend, failing KPIs, and action plans for each supplier.|
|LEAP|4.3.1|--- AI Generated Release Notes --- New Knowledge base article improvements Admins can configure eligible knowledge bases and default KB/category for article creation. The Settings page allows selection of eligible knowledge bases, default knowledge base, and default KB category, which are automatically applied during agent-driven KB article creation. Users can select the knowledge base and category when creating KB articles. A configurable modal prompts users to choose the target KB and category, with metadata and author fields auto-populated for improved search and traceability. LEAP value dashboard The LEAP value dashboard surfaces metrics for all automation outcome types. The dashboard includes new sections and cards for Ansible executions, KB articles, problem records, and outcome breakdowns, with savings attribution by outcome type and Now Assist consumption metrics. Metrics dashboard tabs for artifacts are introduced. Users can view tabular metrics for KB articles, ServiceNow playbooks, Ansible playbooks, Problem records, and an overview of all artifacts, with project-level and system-wide calculations. Automation projects LEAP supports automation projects across multiple incident taxonomies. Admins can configure LEAP to ingest and cluster incidents from multiple taxonomies, producing unified insights and automation opportunities spanning all configured taxonomies. LEAP MCP tool LEAP MCP tool for app setup status is introduced for external AI clients to use LEAP's setup and grouping-pipeline readiness before invoking other tools. Manage archived automation opportunities Admins can view and manage archived automation opportunities\(AOs\). Old AOs with resolution steps are hidden by default after GAF re-runs, and successor/predecessor relationships are surfaced on the AO detail page. AI Sparkle indicator is shown for discovered Ansible playbooks. The LEAP homepage AO list includes an additional column to visually identify playbooks created with AI. Changed LEAP value dashboard layout is updated to tabular format. Artifacts are presented in dedicated tabs with consistent layout and improved clarity. Playbook and Ansible metrics are filtered by automation source. Aggregate metrics now distinguish between ServiceNow playbooks and Ansible playbooks for accurate reporting. Archived flag is backfilled for legacy stranded AOs. Upgrade scripts ensure previously stranded AOs are correctly marked as archived, aligning UI visibility and actions. Default AO list and homepage filters exclude archived AOs. The homepage and list views now show only active, non-archived AOs. KB article creation options and modal labels are revised. The create/view KB article actions are renamed to "Draft KB article," and modal info text is clarified. Job status and troubleshooting actions are scoped per Automation project. Job status lookups and fix-the-error navigation are filtered by the selected project. Properties reads are project-scoped with fallback to global defaults. Changing a property on one project does not affect others.|
|Legal and Contracts Common Utilities|1.2.2|New You can now create and manage contract analysis playbooks to enable negotiation and redlining from MCP compatible external AI tool. Changed Fixed Removed|
|Legal Request Management|10.3.4|New Changed Fixed In Employee Slate, the document widget on a legal request now correctly displays details of documents stored in external storage. Removed|
|Legal Service Delivery - Prime|1.0.17|New Changed Fixed Support for the latest versions of dependent platform applications for the September 2026 release. Removed|
|Licensing Engine|6.5.0|Annual Now Assist Usage reset: Now Assist usage resets on the customer's contract anniversary date, providing a fresh allocation of the full entitlement each year. Enhanced tracking capabilities allow customers to monitor consumption throughout the contract term, with underlying calculation improvements included in this release. Support for entitlement checks for all paid apps, including plugins, ServiceNow Store apps, and partner apps. Central Instance Performance Improvements. Pooled Shared Storage Reporting — The Cloud Capacity Dashboard now accurately reflects storage pooling across instances for shared environments. Instead of showing capacity at the individual instance level, the dashboard displays a unified pool view with "Total Purchased Pool Capacity" summing across all subscriptions \(instance-level and account-level\), a new "Hosting" indicator per instance, and "Used Pool Capacity" replacing the old per-instance usage columns.|
|Major Incident Management for Service Operations Workspace|9.4.2|Compatible with latest ServiceNow release|
|Manage Invoice Operations|1.3.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Manage Order Operations|2.2.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Manufacturing Commercial Operations Advanced|3.0.0|This app will be hidden on the store. No listing content is applicable for this store app.|
|Manufacturing Commercial Operations AI agents collection|4.1.0|https://www.servicenow.com/docs/r/release-notes/manufacturing-commercial-operations-rn.html|
|Manufacturing Commercial Operations Foundation|3.0.0|This app will be hidden on the store. No listing content is applicable for this store app.|
|Manufacturing Commercial Operations Prime|3.0.0|This app will be hidden on the store. No listing content is applicable for this store app.|
|MCP for Strategic Portfolio Management|1.4.0|New: Connect any MCP-compatible AI assistant to your ServiceNow instance to give strategy and PMO leaders, portfolio managers, and project managers direct access to live SPM data through natural language prompts. Access Strategic Portfolio Management data and Now Assist AI skills as MCP tools, enabling LLM agents to query and process goals, portfolio plans, and projects. The following tools are available in this release: Get Goals — Retrieves goals filtered by status, owner, or other criteria. Generate Goal Insights — Generates AI-powered insights for goals and targets. Get Portfolio Plans — Retrieves portfolio plans filtered by owner, timeline, or other criteria. Generate Portfolio Insights — Generates portfolio insights, including at-risk planning items, delayed starts and ends, and dependencies to highlight potential bottlenecks. Get Projects — Retrieves projects filtered by owner, status, state, or other criteria. Generate Project Insights — Detects project risks, analyzes status trajectory, and provides recommendations to mitigate delays. Get AI Status Report — Generates a Red, Amber, Green \(RAG\) status report for a project across resources, cost, schedule, and scope. Identify Project Risks — Detects AI-identified RIDAC risks and saves them to the risk table as AI drafts.|
|Meeting CAB|9.4.2|Problems fixed: Attachments in Service Operations Workspace CAB Meeting Activity section can now be opened and downloaded|
|Meeting Watcher - UI Builder Data Resource|9.4.2|Compatible with latest ServiceNow release|
|Metadata Search|1.2.1|Metadata search results now display consistently and accurately. Issues with incomplete or incorrect metadata listings have been resolved.|
|Metrics and CI Actions Framework|9.4.2|-Compatible with latest ServiceNow release|
|Microsoft 365 for ServiceNow Reporting|23.0.2|Changed ACLs have been restructured to enable compatibility with both Zurich and Australia platforms, allowing IRM and related apps to operate on Zurich for the September Store Release.|
|Microsoft Endpoint Configuration Manager for Investigation|9.4.2|View metrics relevant to the incident and CI in the context of the incident for investigation Get latest metrics and data on-demand from within investigation Visibility for when metrics exceed pre-set warning and critical threshold levels Support for remedial actions|
|Milestones|2.9.1|Updated: Added Deny Unless ACLs for the sn\_milestones\_milestone table, aligned with the Enterprise-Wide Deployment Security September 2026 release.|
|Model Context Protocol Client|2.4.4|- Schema changes done to support storing of Tools in the MCP server - Added support so that onboarded MCP servers can be configured in Assistants for invoking these MCP servers on demand based on ACLs|
|Model Context Protocol Server|1.8.0|--- AI Generated Release Notes --- New Domain separation for MCP servers, tools, and apps. Administrators can now restrict visibility and modification of MCP servers, tools, and apps by domain, ensuring that each population on a shared instance sees only its own content. Global servers and tools are uniquely scoped, with global servers carrying only global tools and non-global servers supporting tools from their own domain, descendants, and global. Server modification is limited to users in the server's domain and its ancestors, while tool eligibility is determined by domain hierarchy. Migration on plugin install preserves existing server URLs and assigns pre-existing servers and tools to global, maintaining uninterrupted client access.|
|News Integration for Supplier Lifecycle Operations|10.0.0|Changed Migration of code to Fluent|
|Notifications Email Agents|3.0.2|New: Omnichannel Intent Detection platform is extended: A global Intent Library, intent detection skill, resolution skill, and integration with Agent Advisor are delivered, supporting multi-channel interactions and automatic intent discovery. Intent Tracking schema and APIs are introduced: Intent tracking supports indexed storage, purge policy, ACLs, and access APIs. Intent Detection Skill and Resolution Detection Skill are available: The system detects intents and evaluates resolution outcomes for interactions, supporting load testing and multi-intent processing. Triggering of intent detection and resolution skills on interaction closure is automated: When an interaction transitions to Closed Complete or Closed Abandoned, skills execute reliably and idempotently for both voice and chat. Transformation and deduplication skills for automation opportunities: Automation clusters are transformed into candidate intents and checked for duplication against the library. Custom notification creation and management is now available for provider notifications: Users can create, edit, and delete provider notification subscriptions, including specifying delivery channels, conditions, schedules, and durations. Provider subscriptions are surfaced in the Custom notifications tab, with v2 channels supported in filters and per-channel toggling. Custom notification request workflow is introduced: Users can submit custom notification requests, which are reviewed by notification admins. Approved requests activate the notification; rejected requests delete it. Operational notifications inform admins and requestors of lifecycle events.|
|Notify UI Components for Configurable Workspaces|9.4.2|Ability to automate initiation of a conference call|
|Now Assist for Prompt Assistance|6.0.7|New: Judges now support the latest agent harness. Task Completeness now scores mission completion only. Intermediate steps and tool calls no longer affect the score.|
|observ-ai-agents-app|6.3.1|Updated Dynatrace agent entity enrichment is streamlined. A new entity-detail tool enables the Dynatrace agent to retrieve entity details in a single call, replacing the previous multi-step describe-then-fetch workflow. Dynatrace agent investigation workflow is optimized. The Dynatrace agent instruction prompt is reduced, and redundant tools are collapsed. The queryproblems and getproblembyid tools are merged into a single parameterized tool, decreasing round-trips and investigation latency. Removed The Google Gemini Cloud Assist Skill has been removed. The skill, tool, and workflow are no longer available or invoked by autonomous workflows.|
|Omnichannel Callback|2.1.0|New Add support for iOS and Android Channels for callback Changed Re-attempt and Retry callback functionality improvements Performance improvements Fixed Removed|
|Omni-Experience Standard Feature Set|8.3.1|Fixed: Security patches for Sidebar Changed Update settings page to reflect Otto rebranding|
|On Call Scheduling for Service Operations Workspace|9.4.3|Changed: Enabled Auto logging Out of the box Record details of failure of communication sent from On-call Fixed: Fixed defects around delays in notification|
|On-Call UI Components for Configurable Workspaces|9.4.2|Changed: Enabled Auto logging Out of the box Record details of failure of communication sent from On-call Fixed: Fixed defects around delays in notification|
|Operational Sustainability Management|23.0.4|New Workspace users now receive Material Topic Approval Request notifications that direct them to the relevant record in the ESG workspace, while users without workspace access are routed to Classic view. The notification leverages the platform's Email Notification Redirection framework for accurate routing. Workspace users now receive Disclosure Approval Request notifications that direct them to the relevant record in the ESG workspace, while users without workspace access are routed to Classic view. The notification leverages the platform's Email Notification Redirection framework for accurate routing.|
|Operational Sustainability Management Advanced|23.0.1|Changed Updated the dependency versions to take advantage of latest updates from the Operational Sustainability Management application. Refer to the dependency app store release notes for details.|
|Operational Sustainability Management Prime|23.0.3|New Operational Sustainability Management Prime includes all Operational Sustainability Management advanced capabilities and makes the ServiceNow platform Prime capabilities available for consumption.|
|Operational Technology Hardware Vulnerability Assessment|4.1.6|Fixed Security fixes|
|Operational Technology Manager|4.1.6|Fixed Fixed influx of duplicate syslog error messages \(PRB2058749\) Fixed the addNotNullQuery filter for cmdb\_ci\_unclassed\_hardware subclass fields \(PRB2031990\)|
|Operational Technology Setup|1.0.0|Initial release|
|Operational Technology Vulnerability Response|3.2.7|Fixed Security fixes|
|Opportunity Management Application|14.1.0|New: Sales CRM Mobile experience for Opportunities : includes opportunity list view, record view, opportunity line items, pipeline health, task management, meetings, quick access, and account record view Opportunity summarization for the mobile experience Changed: Allocation number field in Manage Allocations is now read-only to avoid confusion during split creation Primary quote field is now available as part of the core opportunity data model Internal platform upgrades to improve performance, stability, and readiness for upcoming features Fixed: Resolved "One or more property values are invalid" error when loading the Manage Allocations page Fixed allocation percentage validation incorrectly flagging totals that equal 100% Fixed issue where Opportunity Allocations \(Revenue and Overlay\) could not be set on the opportunity Net New ACV now syncs correctly from Quote to Opportunity Improved Quote-to-Opportunity sync logic and performance Resolved high response times on Economic Buyer and Champion save operations Fixed plugin dependency errors during application installation|
|Opportunity Management Data Model|14.1.0|New: Sales CRM Mobile experience for Opportunities : includes opportunity list view, record view, opportunity line items, pipeline health, task management, meetings, quick access, and account record view Opportunity summarization for the mobile experience Changed: Allocation number field in Manage Allocations is now read-only to avoid confusion during split creation Primary quote field is now available as part of the core opportunity data model Internal platform upgrades to improve performance, stability, and readiness for upcoming features Fixed: Resolved "One or more property values are invalid" error when loading the Manage Allocations page Fixed allocation percentage validation incorrectly flagging totals that equal 100% Fixed issue where Opportunity Allocations \(Revenue and Overlay\) could not be set on the opportunity Net New ACV now syncs correctly from Quote to Opportunity Improved Quote-to-Opportunity sync logic and performance Resolved high response times on Economic Buyer and Champion save operations Fixed plugin dependency errors during application installation|
|Order Case Self Service|2.2.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Order Case Self Service|2.2.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Order Management|18.3.3|Order Management now introduces a configurable Order Milestones framework, giving customers a standardized way to track key checkpoints across the order lifecycle — from initiation through fulfillment to closure.|
|Order Management|18.3.3|Order Management now introduces a configurable Order Milestones framework, giving customers a standardized way to track key checkpoints across the order lifecycle — from initiation through fulfillment to closure.|
|Order Operations Case Management|3.1.3|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Order Operations Case Management|3.1.3|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Order Qualification Management|5.2.1|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Order Qualification Management|5.2.1|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Order to cash common architecture|1.6.6|Added query ACLs as part of this Brazil directive Fluent conversion of the app|
|OT Asset Management|2.2.1|New • None. Changed • Updated application dependency versions to align with the latest supported version of Enterprise Asset Management, Hardware Asset Management, Operational Technology Core, and ISA Equipment Model releases. Fixed • None. Removed • None.|
|OT Asset Management Advanced|2.0.1|New ServiceNow Otto for Enterprise Asset Management enables AI-powered asset request submission Technicians can access AI-powered troubleshooting and repair guidance within their workflows Natural language input streamlines asset and request workflows|
|PA AI Tools|1.0.4|New Added data visualization tool for better analytics experience in Otto chat Ability to view source \(table, filter, etc.\) behind the data in response Ability to drill down to view lists/records|
|Password Reset for Service Operations Workspace|9.4.2|Changed: Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.|
|Password Reset UI components for Configurable Workspaces|9.4.2|Changed: Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.|
|Platform AI Agents and Skills|14.0.10|New Launched the Process task closure, a new agentic workflow, allowing fulfillers to auto generate resolution notes and mark records as closed Exposed the following AI skills to MCP Record summarization AI-generated record resolution notes Changed Updated configuration options for the Identify escalation signals agentic workflow Updated the logic to fetch similar records and KBs using record domain in email response generation Enabled configurable search profile for ERR Generate resolution plan agentic workflow Added an option for the fulfiller to create a new record as part of the Generate resolution plan agentic workflow Renamed the Decomposition Agent to "Resolution task generation AI agent" Analyze task trends Users can now perform analysis for a specific group by passing the exact group name in the utterance In the analysis output, we cite records for recurring issues and root causes and allow users to browse through analysed records to increase confidence in the output.|
|Playbook Experience|29.6.3|Playbook authors can preview activity UIs with live sample data in the Playbook builder. Authors can now visualize each interactive activity instance using a live preview panel in the UI Layout tab, modify experience property values, and see real-time updates. Sample data can be provided for unresolved fields, and authors can toggle between sample-driven and data-driven previews. Live UI Preview updates for Activity Actions. When authors modify activity actions such as buttons—adding, deleting, changing labels, or repositioning—the UI Preview updates immediately to reflect these changes. Actions in the Playbook Experience Picker also update in the Playbook Card. Support for fetching individual actions by action ID in Playbook Experience. The Playbook Experience component now enables targeted data retrieval for activity UI previews, allowing users to preview specific actions based on their action IDs.|
|Playbook Experience Components|29.6.2|New Playbook authors can preview activity UIs with live sample data in the Playbook builder. Authors can now visualize each interactive activity instance using a live preview panel in the UI Layout tab, modify experience property values, and see real-time updates. Sample data can be provided for unresolved fields, and authors can toggle between sample-driven and data-driven previews. Live UI Preview updates for Activity Actions. When authors modify activity actions such as buttons—adding, deleting, changing labels, or repositioning—the UI Preview updates immediately to reflect these changes. Actions in the Playbook Experience Picker also update in the Playbook Card. Support for fetching individual actions by action ID in Playbook Experience. The Playbook Experience component now enables targeted data retrieval for activity UI previews, allowing users to preview specific actions based on their action IDs.|
|POM - Prime|1.3.1|New: Automated purchase order confirmation creation from emails: Reduce manual tracking of supplier emails by automatically converting emails with purchase order details into confirmations.|
|Portfolio Planning|8.18.0|New: Added ACLs to support extended security for Enterprise-Wide Deployment partitions. Access portfolio risks, issues, decisions, actions, and changes \(RIDAC\) directly from the portfolio plan using the dedicated RIDAC page. Access program planning views from the new Programs menu. Select any program to open its dedicated plan with Prioritization, Roadmap, Kanban, and Financials views. Added automated email notifications for scenario approval. The My Demands widget is added to the Employee Slate canvas. Requesters can add the My Demands widget to their Employee Slate canvas to track the state of their demands. Requesters can view and track their demands directly from the My Demands widget. The widget lists all demands created by the requester, with filters by state and links to the standard demand tracking experience. When a demand is converted to an execution artifact, such as a project, epic, or story, requesters can view high-level status, planned and actual end dates, and the last update from the Execution Tracking widget. The demand details page includes the lifecycle tracker, activity, attachments, and edit tabs. Requesters can view the demand lifecycle, activity history, attachments, and edit key fields from the standard ticket page. Demands submitted by requesters appear in the My Requests list, alongside other requests, with consistent state and status display. Financial widgets have info icons explaining the values and how the calculation is done.|
|Portfolio Planning Core|5.13.5|New: Added ACLs to support extended security for Enterprise-Wide Deployment partitions.|
|Post Assessment Actions for Smart Assessments|23.0.3|Changed Tab switches preserve unsaved changes across General, Questions, Automations, and Scoring tabs. A dirty-state icon on the workspace selector indicates pending changes. Fixed Template copy failures no longer leave orphaned Automation rules behind. Failed copies now remove their associated Automation rules.|
|Price Management|18.0.4|New Precision is now a configurable property that admins can set, solving currency rounding issues globally Pricing Engine response now includes step-level performance timing \(perfStats\) for debugging and optimization Changed Performance improvement on large quotes and reduction in customer timeouts Fixed Improved VLP auto-generation by fixing defects, including: Incorrect VLP calculations in auto-add flows Preventing deletion of Target VLP lines during auto-add flows|
|Privacy Management Advanced|23.0.2|New New AI based reviewer assistant to recommend impacted control objectives and risk statements for Privacy Screening and Impact assessment. Changed Zurich Patch 12 and Australia Patch 5 and Brazil compatibility maintained for supported store applications|
|Privacy Management Prime|23.0.2|New AI-Powered Privacy Assessment Recommendations: Privacy assessment tasks now auto-generate AI-recommended control objectives and risk statements when moved to Review state, with intelligent suggestion guides explaining the rationale. Accept or reject recommendations to streamline compliance scoping. Approved items automatically map to associated processing activities. ServiceNow OTTO Prime capabilities: This release brings Prime-tier capabilities of platform, including GenAI summarization, automated resolutions, conversational self-service through virtual agents, multi-step agents, and AI Control Tower for asset management.|
|Proactive Engagement|5.2.0|See DEX Application and Device Health product for release notes. This app is a dependency of DEX Application and Device Health.|
|Problem Management for Service Operations Workspace|9.4.2|Changed No code updates were made in this release. The release number has been updated to maintain consistency with changes in related Service Operations Workspace applications.|
|Process Automation Designer|29.6.4|Fixed: Support for playbook summarization in off-glide environment Minor defect fixes for Playbooks as MCP tool|
|Procurement Case Management|20.0.0|New Admins can access SPO Product Admin Home as a single entry point. Product Hub provides guided installation of SPO applications and plugins. Configuration Console provides a guided experience for configuring Procurement Case Management items, including completion tracking. From Configuration Console, admins can download update sets and upload batch update sets to higher environments. Changed: SPO configuration is now organized within the Otto for Setup framework, replacing navigation across multiple administrative tools and locations. The administrative experience is now consistent across Product Hub and Configuration Console.|
|Product Catalog Advanced|10.5.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Product Catalog Advanced|10.5.0|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Product Catalog Management Core|20.0.2|New Extended product life cycle states for product offerings and specifications Channel-specific availability for product offerings Localized product catalog experiences for catalog, category, relationships, characteristics and options Customizing the display order of product offerings, categories and catalogs Changed Expanding minor updates to published product offerings and specifications with additional options such as optional characteristic association, optional child entity association with a future effective date|
|Product Conditions Core|4.6.9|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Product Inventory Advanced|14.3.3|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Product Inventory Advanced|14.3.3|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Project Workspace|7.6.2|New Doc templates now support dynamic content, similar to status reports, with two default templates that use dynamic fields: Project Charter and Project Closeout. Lists are now available in the L1 menu of Project Workspace. The My Demands widget is added to the Employee Slate canvas. Requesters can add the My Demands widget to their Employee Slate canvas to track the state of their demands. Requesters can view and track all demands they created from the My Demands widget, filter them by state, and open them in the standard demand tracking experience. When a demand is converted to an execution artifact such as a project, epic, or story, requesters can view its high-level status, planned and actual end dates, and last update in the Execution Tracking widget. The demand details page now includes the Lifecycle tracker, Activity, Attachments, and Edit tabs, so requesters can review the demand lifecycle and activity history, open attachments, and edit key fields from the standard ticket page. Demands submitted by requesters appear in the My Requests list alongside their other requests, with a consistent state and status display. You can now edit project details in the list view of the home page. The Financials tab in Project Workspace now saves your timescope selection and restores it when you return to the project, retaining it for your 50 most recently accessed projects by default and up to 200 when configured by an administrator. Administrators can now configure Strategic Portfolio Management financials through the Implementation Accelerator guided setup, which covers labor cost plans, labor cost types, budget allocation, financial baselines, currency settings, investment object linkage, cost plan breakdown rollups, and fiscal calendar issues. Info icons on the Financials page explain key fields and calculations, including planned cost, budget, EAC, return, ROI, and NPV, directly within each widget. SPM configuration setup now includes an updated Financials guided setup wizard to help administrators configure all required financials settings efficiently. Changed Projects with more than 2,000 tasks now load through concurrent batch calls, which reduces load times and improves responsiveness. The task planner now supports planned effort rollup with consistent rollup logic, Actual Effort fields are always read-only, and maximum units are supported based on your configuration. Project managers can now edit parent task constraint dates from the task planner, and child task start dates honor both the parent and child constraints. Errors in the resource assignment auto-sync flow are now logged with stack traces for easier troubleshooting. Project Diagnostics and Save as New Template are now available on the Planning page in Project Workspace, along with modal validation and navigation improvements. When you edit and save a single row in the financials cost and benefit grid, only that row refreshes instead of the entire grid, and the row is locked until the save completes on the server, on both the month and year timescales. Project managers and planning item owners can now recalculate planned cost and benefit values against updated budget reference rates across all relevant breakdowns, with confirmation dialogs and a loading overlay to show progress, and the previous Recalculate resource cost action is hidden to avoid duplication.|
|Public Sector Digital Services AI Agent Collection|2.0.4|Updated Migration of application to fluent|
|Public Sector Digital Services Core|15.0.6|New Public sector terminology and constituent lookup in interaction pages. Interaction pages for email, voice, and chat now use public sector terminology, replacing commercial terms such as 'consumer' with 'constituent', 'contact' with 'business contact', and 'account' with 'business'. Lookup functionality now queries constituent records, ensuring caseworkers retrieve accurate public sector data. L3 compliance support for app-psds-agency. The app-psds-agency now supports Level 3 compliance, enabling agencies to meet advanced regulatory requirements. Fluent framework adoption for app-psds-agency. The app-psds-agency interface has been converted to the Fluent design system, providing a consistent and accessible user experience. Configurable identity data model and access controls for multi-provider SSO. Agencies can now securely store verified identity attributes from external identity providers, with role-based access controls restricting visibility and updates to authorized users and trusted providers. Changed Localization and translation improvements across core bundle. Client scripts and widgets now preload translation keys and resolve placeholder patterns, ensuring all UI text extracts correctly for translation and displays as intended. Literal strings are passed directly for translation, and message fields are populated for synchronous getMessage calls, addressing localization warnings flagged in release readiness reports. Build configuration update for app-psds-agency. The now-sdk build process for app-psds-agency now passes the "--emitDictionary=false" parameter, optimizing build output and dictionary handling. Fixed The financial details table now correctly handles extensibility and child tables, resolving issues related to missing class name columns.|
|Purchase Order Management|3.0.4|New: Create a purchase order confirmation in Supplier Collaboration Portal: Provide buyers certainty about their orders by creating purchase order confirmations directly from the Supplier Collaboration Portal.|
|Query Generation|6.3.1|New Support all entities/dimensions when the entity is known Enhance the Query Generation Admin page|
|Quick links component for Service Operations Workspace|9.4.2|Compatible with latest ServiceNow release|
|Quote AI agent|3.0.8|The quote agent now recognises more everyday phrasings for creating, updating and discounting quotes, and tells you clearly what to do when a quote PDF cannot be generated because no document template is attached. Quote agent roles and access permissions are now included in the installed package.|
|RAG for code generation|1.1.14|Fixed Log spam removed Virtual tables are no longer indexed, preventing unnecessary data processing|
|Recommendation template|23.0.2|New Improved protection against unauthorised query-based data discovery. ACL behaviour across new installs, upgrades, and true-up releases. Reduced operational dependency on manual remediation activities. Zurich and Australia compatibility maintained for supported store applications. The application now supports updated table names for access control records, ensuring alignment with recent migration requirements.|
|Recommended Actions|44.0.4|New: Recommended actions now support new guidances, 'Attach Knowledge' and 'Relevant Case' for AI Search results that surface on CRM workspace.|
|Recommended Actions for Security Operations|2.3.6|Fixed: Fixed a translation file issue for the Otto changes.|
|Record Page for Service Operations Workspace|9.4.2|Changed: Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.|
|Record - vertical|23.0.3|New Zurich platform support for September Store Release. The application now supports both Zurich and Australia platforms by restructuring access control logic, enabling IRM and related apps to function on Zurich for the September release.|
|Regulatory Agency Library|23.0.2|New Improved protection against unauthorised query-based data discovery. ACL behaviour across new installs, upgrades, and true-up releases. Reduced operational dependency on manual remediation activities. Zurich and Australia compatibility maintained for supported store applications.|
|Request Management for Service Operations Workspace|9.4.2|Compatible with latest ServiceNow release|
|Resource Management Workspace|5.10.1|Fixed You can now edit planned effort for periods without actuals, even when the editing property is disabled. Heatmap cells follow the same behavior and remain editable unless actuals exist for the period. Resource allocation values in Resource Management Workspace are now consistent across all filters. Previously, discrepancies could occur when a user had multiple plans on the same project. Starting capacity values now round correctly when a work schedule uses decimal hours, ensuring accurate display and calculations. The allocation modal in Resource Management Workspace now excludes pending and unapproved resource assignments from allocation calculations when the relevant property is enabled, so the summary message matches the actual assignment status. You can now extend a resource assignment's end date to a date before the task end date without triggering a validation error. Operational plan hours now update correctly when changed from Resource Management Workspace, so edits to resource assignments are reflected as expected. Creating a filter on a new resource card now returns results as expected. Previously, results for referenced tables could remain stuck on Searching.... Parent resource status now accurately reflects a mix of approved and unapproved assignments, instead of incorrectly showing Pending. Copying a resource assignment now correctly carries over the original Resource status and Ready for review values. Previously, these fields defaulted unless they were added as grid view columns. Move operations now work correctly for resource assignments that have only a planning item associated with them. Previously, these operations failed because planning item dates weren't handled the same way as project and demand task dates. Group by parent and owner now displays accurate user- and group-level rollups, including for zero-allocation, task-based assignments. This also resolves rollup accuracy issues that could occur in non-English locales.|
|Retail Core|7.6.0|New Plan progress summary dashboard with complete plan hierarchy tracking added on a single page replacing the previous drill-down-only tab experience. A new "Schedule Occurrence" column has been added to the Retail Case table, referencing to the "Schedule Occurrence" table. Integration with Strategic Portfolio Management \(SPM\) through which all store opening, closing, relocation and refurbishment project tasks to be performed at the store can be made visible to store employees on Retail portal.|
|Retail MCP Server|1.0.0|New Initial Release. Exposed ServiceNow retail capabilities through Retail MCP Server tools — store context, store devices, and Store Services case creation and lifecycle management.|
|Risk Assessments for Supplier Lifecycle Operations|8.0.1|Changed Migration of code to Fluent|
|RMA Case Management|2.3.4|New None Changed The internal implementation has been updated. There is no functional or behavioral impact, and no customer action is needed. Fixed None Removed None|
|Roadmap UI Builder Component|22.14.2|New: Access roadmap keyboard shortcuts anytime from the Shortcuts modal in the side panel for a more consistent experience when viewing and managing roadmap shortcuts. Fixed: Resolved an accessibility issue where the close button on roadmap item popovers incorrectly included the aria-pressed attribute and was presented as a toggle button. Resolved an accessibility issue where the No Roadmap Milestones tooltip help button was not included in the tab order and did not respond to the Enter key.|
|Sales and Order Management for Technology Provider - Advanced|1.0.8|SKU Application Plugin - No code delievered|
|Sales and Order Management for Technology Provider - Prime|1.0.7|SKU Application Plugin - No code delievered|
|Sales and Order Management for Telecommunications, Media and Technology - Advanced|1.0.7|SKU Application Plugin - No code delievered|
|Sales and Order Management for Telecommunications, Media and Technology - Prime|1.0.9|SKU Application Plugin - No code delievered|
|Sales and Order Management for Telecommunications - Advanced|2.3.2|Changed Maintenance release — dependency updates only; no new customer-facing functionality in this version|
|Sales and Order Management for Telecommunications - Prime|2.3.2|Changed Maintenance release — dependency updates only; no new customer-facing functionality in this version|
|Sales Common|8.1.2|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Sales Development AI Agents|1.0.12|Product version upgraded to support AP6 and BP0 in line with all SOM ai apps.|
|Scan Engine|6.0.3|New Headless Scan Engine APIs for CI/CD and ReleaseOps: Scan Engine can now be triggered, monitored, and queried outside the ServiceNow UI using REST APIs. Customers can start scans, check status, retrieve results, cancel scans, and access findings programmatically. This enables integration with CI/CD pipelines such as Jenkins and GitHub Actions to implement automated quality gates. Introduced By Tracking for Findings: Added a new "Introduced By" field to findings. When a full or delta scan detects a violation, Scan Engine records the update set that introduced the issue, making it easier to trace findings back to the originating change. Changed Smoother Exception Handling and Governance: Exception handling is now more predictable and auditable. Update sets with out-of-scope findings can be resolved appropriately, approval workflows better support enterprise governance models, and reporting relationships between findings and exceptions have been improved. Dedicated Exception Approver Role \(scan\_engine\_exception\_approver\): Exception approval responsibilities are now separated from dashboard access, allowing designated non-administrators to approve exceptions without requiring broader system permissions. Fixed Finding and Exception Reporting Improvements: Resolved issues affecting the reliability of relationships between findings and their associated exceptions for reporting and auditing scenarios. General Defect Fixes and Stability Improvements: This release includes multiple defect corrections and platform stability enhancements.|
|Security Case Management common workspace components|2.1.3|Fixed Fixed the translation issues for Security Incident Response Workspace pages and components.|
|Security Incident Response|14.4.0|Fixed: Restricted 'Create Security Incident' UI action visibility for ITIL users without access. Fixed Restricted Caller Access warning on SecurityIncidentUtils execution.|
|Security Incident Response - Advanced|1.0.10|Changed: Certified with Brazil|
|Security Incident Response - Foundation|1.0.10|Changed: Certified with Brazil|
|Security Incident Response - Prime|1.0.10|Changed: Certified with Brazil|
|Security Incident Response Workspace|1.10.1|New Integration of MITRE ATLAS framework into SIR. Fixed Fixed Associated List dropdown not populating on related list config forms. Fixed Label field validation not triggering on first focus. Fixed ZTA modules displaying in workspace when plugin is not installed. Fixed the ability to create Security Incident Categories and SubCategories. Fixed translation strings hardcoded in UI messages, tooltips, and bulk action dialogs. Fixed Begin/End date selection when creating Outages on incidents. Fixed translation exposure for UI strings \("Create Incident," "Create Problem," "Create Change Request," "Details," "Activity," "Quick filters," and related text\).|
|Security Incident UI Card Component|1.0.5|Fixed UI improvements. The color contrast of priority badges in dark theme has been corrected to improve accessibility.|
|Security Support Common|30.6.5|Fixed Fixed an issue where retired configuration items \(CIs\) could be incorrectly associated with Security Incidents created from SIEM data ingestion. Fixed an issue where security capability execution flows could run all active capability implementations instead of only the ones specified. Improved upgrade performance for the Security Support Common plugin, reducing install time during instance upgrades. Resolved several packaging and translation issues in Security Support Common to improve localization coverage. Fixed a role-definition packaging issue in the Security Support Common plugin. Improved accessibility compliance across Security Support Common workspaces and forms.|
|Service Catalog AI Core|1.0.2|New Initial release primarily targeting support for conversational catalog request experiences.|
|Service Graph Connector for Microsoft Excel|4.1.5|Fixed Security fixes|
|Service Level Management Experience for Workspace|9.4.2|-|
|ServiceNow AI Lens|8.1.1|New Added three new system properties to control the visibility of the Fill with Lens button on Service Catalog forms. Changed Fixed Removed|
|ServiceNow AI Lens Core|8.1.1|New Added three new system properties to control the visibility of the Fill with Lens button on Service Catalog forms. Changed Fixed Removed|
|ServiceNow Document Designer with Word|23.0.3|New Scripted HTML column type for document designer Authors can now create data columns that return HTML through scripts, enabling rich formatting and embedded images within repeater and table iterations. Scripted HTML columns are available in the Data Column form and render formatted content in generated documents. Changed Enhanced support for scripted HTML data columns Report generation now correctly handles special characters in HTML fields, ensuring successful output and proper character escaping.|
|ServiceNow EmployeeWorks Web App Base|2.3.6|1. Directory template: New landing-page layout guides employees through topic subtopics for clearer content pathways. 2. Breadcrumb navigation: Employees can now easily navigate through the topic hierarchy with contextual breadcrumb links. 3. Ask Otto name configuration: Admins can customize the displayed assistant name while supporting the configured Moveworks bot-friendly name by default. 4. Browse UI refinements: Visual and usability improvements across Browse deliver a more consistent and polished experience. 5. Inline admin configuration: Admins can now edit Browse options, Quick Links, Knowledge, and Applications directly without navigating to separate configuration records. 6. Image auto-compression: Images are automatically compressed and optimized per display context \(thumbnail, carousel, hero feed\). 7. Task delegation: Employees can now delegate tasks to colleagues directly from the task details view. 8. Person card report counts: Person cards in the org chart now display total report count alongside direct report count by default. 9. Home page background theming: Admins can set home page backgrounds per theme in the Admin Console, enabling different audiences to have distinct visual experiences.|
|ServiceNow Enterprise Asset Management|11.0.0|New: Added AI-assisted asset and model import capabilities for enterprise models and assets. Added AI-powered column mapping and value mapping to simplify onboarding asset and model data from external sources. Added validation and review capabilities prior to import to help reduce data quality issues. Added seeded asset and model import templates with guided instructions, reference data, and validation guidance. Changed: Replaced generated enterprise model and asset import templates with improved seeded import templates. Simplified the bulk import experience with enhanced guidance and import preparation resources. Fixed: None Removed: Removed reliance on generated enterprise model and asset import templates in favor of seeded templates.|
|ServiceNow IDE|5.0.2|New: ServiceNow IDE was redesigned for an agentic-first development experience with Build Agent.|
|ServiceNow Otto Agents for requestor|3.7.6|Fixed: Approval agent is now accessible for foundation users.|
|ServiceNow Otto AI web agent|33.0.3|New Credential and dynamic parameter management - Reference credentials or other user-specific values by name in your instructions. The agent resolves them securely at execution time, so you never have to type them in yourself. File upload and download - Attach files to a web form field during a task, and the agent reports whether or not the upload succeeded and the reason of the failure. Files that a task produces are tracked through the download lifecycle \(pending, completed, or interrupted\) for each browser tab. Changed Browser startup and tab behavior - Browser session now opens to an empty page instead of Google's homepage. Automation actions within the same chat window now reuse the existing browser tab instead of opening a new tab for every action. A new tab opens only when a new chat session starts or you close the current tab. Improved security for adaptive desktop actions system properties - Adaptive desktop actions system properties now require appropriate read and write roles. This change prevents unauthorized users from viewing or modifying the configuration settings, while automation continues to work as expected. Fixed Removed|
|ServiceNow Otto context menu|3.9.0|- Defect fixes and Greenlight automation|
|ServiceNow Otto Conversational Data Collection|10.2.22|Fixed PRB2069440 – return\_to\_agent false positive causing topic execution to terminate when no agent\_instructions passed PRB2075551 – Mid Topic switch not happening during sensitive fallback PRB2061989 – gen ai message history is not being updated consistently during live agent post chat PRB2068808 – Small talk causing error during topic execution when typing "I did not like this" PRB2063924 – Invoking the Change Risk explanation skill in Now Assist returns error|
|ServiceNow Otto for Accounts Payable Operations \(APO\)|9.0.0|1. Case-to-Knowledge Article Generation Generate a knowledge article from a single resolved/closed case, with Otto AI drafting content for your review before publishing. Generate a comprehensive knowledge article from multiple related closed cases to document common issues at scale. 2. AI Data Explorer – Multi-Table Support AI Data Explorer now correlates data across APO, SPO, and SLM tables \(invoice, supplier, approval, PO, receipt\) to answer natural-language queries with a single unified result. 3. ZTSD Enhancements Case resolutions now display the supplier invoice number instead of the internal ServiceNow-generated number. Suppliers and employees can view and accept/reject the proposed resolution directly from the case ticketing page via the employee slate or supplier portal. Other minor improvements|
|ServiceNow Otto for AI Control Tower|24.0.4|Analysed slow queries and fixed AI skills failures.. Fixing data quality observations. Fixing AI agent conversation fails.|
|ServiceNow Otto for AIRC|23.0.1|New Enhanced AI Control Tower to automatically classify AI systems by risk at onboarding, helping identify managed and unmanaged assets and reducing manual review effort. Improved user experience and ability to save &amp; continue Evaluation configurations for continuous monitoring of AI assets. Enhanced AI Control Tower to support domain-separation readiness, enabling assessment and planning for client-level data segregation and multi-tenant deployments. Introduced new onboarding Playbook with dynamic &amp; risk-based execution &amp; lifecycle task management. Introduced new AI capabilities to recommend control objectives and risk statements on AI impact assessment task. Fixed Fixed an issue where the Recommendation section was incorrectly displayed on the Risk and Compliance page. Fixed an issue where the Group Attestation action was not visible in the Attestation related list. Fixed upgrade-impact issues related to the introduction of a new field on the CCM Configuration record. Fixed an issue where the AI Asset Task state was not updated to Review after assessments were submitted.|
|ServiceNow Otto for AI Search|18.0.5|New Catalog enrichment workflow enables surfacing relevant catalog items using AI. Users can now leverage an LLM-powered enrichment process to identify and highlight catalog items, with support for extending this workflow to additional tables. Enrichments are produced in a format compatible with the recommendation backend. Changed Genius Result search flow now uses advanced reranking for improved relevance. The Genius Result backend has migrated to the BGE reranker, enhancing document and passage relevance scoring. Genius Result scripts now expose a new scored\_passages key, providing passage text alongside its rerank score, while maintaining backward compatibility with existing scripts. Fixed Empty hyperlinks in synthesized answers have been resolved. Hyperlinks with no text are no longer replaced with irrelevant content, ensuring consistent and accurate answer formatting.|
|ServiceNow Otto for App Engine|30.1.1|Changed Maintenance release.|
|ServiceNow Otto for Care Team Operations|2.1.1|New Enhancements to provide better support for agentic engineering.|
|ServiceNow Otto for Care Team Operations|2.1.1|New Enhancements to provide better support for agentic engineering.|
|ServiceNow Otto for Cloud Cost Management|1.0.0|ServiceNow Otto for Cloud Cost Management enables cloud resource admins and users to use the capabilities of generative AI skills in Cloud Cost Management. The ServiceNow AI Platform now brings you a new AI experience with three licensing tiers available: Foundation: AI basics to deliver insights Advanced: AI to boost productivity across relevant use cases Prime: Act autonomously with all AI assets, and create your own|
|ServiceNow Otto for Code|28.5.32|Fixed General fixes and enhancements.|
|ServiceNow Otto for Collaborative Work Management \(CWM\)|7.0.2|New ServiceNow Otto for CWM can read external documents, meeting notes, PDFs, or open prompts to automatically generate structured CWM tasks with the appropriate fields populated. ServiceNow Otto for CWM an split any CWM task into smaller, assignable child tasks with a single click. ServiceNow Otto for CWM brings AI-assisted filter generation to lists in CWM, helping teams customize and refine their work views using natural language.|
|ServiceNow Otto for Configuration Management Database \(CMDB\)|4.4.1|New Ask questions about CMDB tables and attributes to get a better understanding of the schema. Responses are based on predefined content in the Data Model Navigator app, which contains information about the base-system CMDB schema.|
|ServiceNow Otto for Contract Management Pro|2.5.2|New N/A Changed Contract document-based conversational search queries now return all matching results instead of 10 results. Use show more option to load the remaining results. In conversational search, introduced an option to preform in-document search after the contract metadata search results are available. Fixed Fixed plugin names and icons for ServiceNow Otto for Contract Management Pro in AI Admin Hub. Removed|
|ServiceNow Otto for CPQ|1.1.8|Bundles the latest Quote AI agent and CPQ Config Agent A2A|
|ServiceNow Otto for Creator|29.6.2|Changed ServiceNow Otto branding Please click on the individual dependent apps included with this package for detailed release note information.|
|ServiceNow Otto for Customer Service Management \(CSM\)|15.0.1|New All CSM Gen AI application repositories now meet Level 3 Agent Readiness. Autonomous AI agents can contribute code across these repos, with branch protection, CI validation, and agent documentation enabling independent operation. Changed Fluent Support is enabled for ServiceNow Otto for CSM. The application is converted to Fluent, improving integration and support.|
|ServiceNow Otto for Document Voice|2.0.11|Fixed: Domain separation issue when configuring, the configuration process now maintains proper separation between domains|
|ServiceNow Otto for Enterprise Asset Management|2.0.1|New: Added an agentic workflow to help manage enterprise asset requests. Added an agentic workflow to help repair depot assets by providing guided repair assistance. Added AI-powered enterprise asset management experiences integrated with Enterprise Asset Management workflows. Changed: None Fixed: None Removed None|
|ServiceNow Otto for Error Framework|1.2.0|Changed: AI Insights now uses cache instead of refreshing every time|
|ServiceNow Otto for Field Service Management|11.1.2|New No Change Changed No Change Fixed Fixed Fluent conversion issues Removed None|
|ServiceNow Otto for Finance and Procurement|8.0.0|New: Case-to-Knowledge Article Generation: Generate a knowledge article from a single resolved or closed case, with Otto AI drafting content for review before publishing. Generate a comprehensive knowledge article from multiple related closed cases to document common issues at scale. AI Data Explorer – Multi-Table Support: AI Data Explorer can now correlate data across APO, SPO, and SLM tables \(including invoices, suppliers, approvals, purchase orders, and receipts\) to answer natural-language queries with a unified result. Changed: ZTSD Enhancements: Case resolutions now display the supplier invoice number instead of the internal ServiceNow-generated invoice number. Suppliers and employees can now view and accept or reject proposed resolutions directly from the case ticketing page through the employee slate or supplier portal. Other minor usability and experience improvements.|
|ServiceNow Otto for Hardware Asset Management|5.0.1|This version adds support for installing and upgrading ServiceNow Otto for Hardware Asset Management through the Hardware Asset Management Product Hub feature.|
|ServiceNow Otto for HRSD - Galileo Inside|2.3.7|Updated app name to ServiceNow Otto for HRSD – Galileo Inside|
|ServiceNow Otto for HR Service Delivery \(HRSD\)|13.5.2|AICT positive feedback reporting for Now Assist Skills|
|ServiceNow Otto for Impact|6.0.6|Fixed Issues Otto rebrand not reflected in Now Assist Admin plugin UI. Plugin names and icons in Now Assist Admin's Settings &gt; Plugins tabs \(Available for you / Installed\) and on the Admin overview page now correctly display ServiceNow Otto branding instead of the legacy Now Assist name and logo.|
|ServiceNow Otto for Integrated Risk Management|23.0.4|Fixed: Made logo compatible with Otto directive|
|ServiceNow Otto for IT Operations Management \(ITOM\)|2.9.4|New Alert Verification AI Agent automates alert closure based on related incidents and knowledge articles. Integration Management Agent enables conversational setup and lifecycle management for top pull connectors. Credential creation within conversational setup. Advanced KB search and summarization for alert investigation. Option to install integrations with Otto from integration launchpad Auto-closure reasoning and expanded explanations are available for alerts. Enable offglide execution for compatible alert skills. Changed Alert reasoning headers updated for all closure scenarios. Autonomous Not Significant Styled Output prompt revised. Data handling improved for insignificance reason from summarization prompts New headers added for alert reasoning scenarios.|
|ServiceNow Otto for Knowledge Management|31.6.6|September release|
|ServiceNow Otto for Legal Service Delivery|1.9.7|New Changed Fixed Fixed plugin names and icons for ServiceNow Otto for Legal Service Delivery in AI Admin Hub. Fixed the assist count consumption issue for the Legal risk evaluator skill. Removed|
|ServiceNow Otto for Manufacturing Commercial Operations \(MCO\)|4.1.0|https://www.servicenow.com/docs/r/release-notes/manufacturing-commercial-operations-rn.html|
|ServiceNow Otto for Operational Sustainability|23.0.1|Changed Updated the dependency versions to take advantage of latest updates from the Operational Sustainability application. Refer to the dependency app store release notes for details.|
|ServiceNow Otto for Opportunity Management|1.2.0|New: Conversational AI for Opportunity Management via Now Assist: enables sales reps to create, update, read, and search Opportunities, Opportunity Line Items, Tasks, Touchpoints, Meetings, Contacts, Accounts, Competitors, Associated Contacts, and Buying Groups through natural language queries in the Now Assist/Otto interface Opportunity AI Agent support with agentic workflow, asset subscription, and role-based access to the Now Assist Panel Context-aware AI responses with record/page context resolution, confirmation before saving changes, permissions enforcement, natural-language error messaging, and fallback handling for unrecognized requests Opportunity summarization via the existing summarization skill in Now Assist/Otto Changed: Otto for Opportunity Management converted to ServiceNow SDK \(Fluent\) for improved platform alignment and maintainability Internal platform upgrade for Level 3 Agent readiness on the Opportunity Management AI features app|
|ServiceNow Otto for Order Management|2.3.3|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|ServiceNow Otto for Platform|13.0.1|Updated dependencies under the application|
|ServiceNow Otto for Platform Advanced|3.0.1|Updated dependencies under the application|
|ServiceNow Otto for Platform Foundation|3.0.1|Updated dependencies under the application|
|ServiceNow Otto for Platform Prime|3.0.1|Updated dependencies under the application|
|ServiceNow Otto for Privacy Management|23.0.2|New New AI based reviewer assistant to manage and recommend impacted control objectives and risk statements for privacy screening and impact assessments. Changed ServiceNow OTTO Branding Updates Updated the application to reflect ServiceNow's new OTTO branding, replacing Now Assist references for a consistent AI experience across the platform.|
|ServiceNow Otto for Process Mining|4.1.5|New: Move all ServiceNow Otto for Process Mining skills from Now Assist \(ServiceNow Otto\) for Creator to Now Assist \(ServiceNow Otto\) for Platform. Added two ServiceNow Otto for Process Mining skills for filling in the process configuration and helping with the state field mapping. Allow Skill ACL customization. Changed: Update defaults to the latest models for 3P providers for Worknotes and Highlights. Fixed: Several fixes on 3p models, ACL customization, and task completions.|
|ServiceNow Otto for Public Sector Digital Services \(PSDS\)|2.5.3|Updated Migration of application to fluent|
|ServiceNow Otto for Purchase Order Management \(POM\)|1.4.1|New: Automated purchase order confirmation creation from emails: Reduce manual tracking of supplier emails by automatically converting emails with purchase order details into confirmations.|
|ServiceNow Otto for Retail Service Management|1.6.0|Fixed Internal conversion|
|ServiceNow Otto for Sales and Order Management for Telecommunications|4.3.3|Changed Maintenance release — dependency updates only; no new customer-facing functionality in this version|
|ServiceNow Otto for Sales Automation|1.1.7|Fixed: Version support upgraded to BP0 and AP6 Dependent app version updated to support same engines|
|ServiceNow Otto for Security Incident Response \(SIR\)|6.5.2|New: Security Incident AI ROI Summary Dashboard. Enhancements to Quality assessment. Added version tracking for report history. Duplicate reports as editable drafts. Refresh selected report sections independently by prompting in Natural language. Configurability to add additional context, KB articles for generating consistent assessments. Fixed: PRB2059317: NACM Actions not available for post incident analysis flow in UI 16.|
|ServiceNow Otto for Service Quality|2.2.0|--- AI Generated Release Notes --- New AutoQA now supports multilingual quality management. Administrators can configure and manage supported languages for quality evaluation, expanding usability for global customers. Guided configuration support is available for SwissRails Auto QA MVP setup. Configuration specialists receive step-by-step guidance tailored to their environment, ensuring correct and efficient deployment. AutoQA Service Quality Cases are now included in Maintenance &amp; Monitoring \(MAT\) profiles. Three end-to-end test cases covering Dashboard, Admin, and skill execution are annotated and available for verification and monitoring. Service Quality test cases have been added to the AutoQA dashboard and regular test profiles. Test cases for Australia, Zurich, and multiple release tracks are now visible and managed in both profiles. Changed AutoQA dashboard performance has been optimized for initial load. The Trends data broker now uses GlideAggregate for improved speed, and the Get Avg QA Score Last 30 Days broker consolidates queries for faster workspace home page loading. Reviewed cases and average QA score tiles are now consolidated into a single broker and UI component. Both metrics share one data query, reducing redundant processing and improving dashboard responsiveness. Admin UI configuration for AutoQA now supports extended tables. Administrators can select extended tables when using the Copy skill feature, and business rules from the base skill are applied to child tables. AutoQA business rule conditions have been updated. Trigger conditions are validated after any update, ensuring the AutoQA Skill is invoked correctly. Failed test cases are now validated against manual testing and signed off when confirmed working. Documentation distinguishes between actual defects and false positives. Fixed Translation errors in the AutoQA review and activate screens have been resolved. All translations now display accurately, with deterministic language selection for choice labels. Improper null checks in the Average QA Score tile client scripts have been corrected. The tile now renders its zeroed empty state without errors when broker output is absent. The empty-query guard in the Get Avg QA Score data broker has been restored. The broker now returns its empty state immediately when the query is blank, preventing slow dashboard loads. SidebarDiscussionSummarizationIT.verifySkillActivationFromNowAssistAdminPage test failure has been fixed. The test now passes successfully.|
|ServiceNow Otto for Setup|5.0.20|Changed: Layered intelligent Admin Home and navigation: Admin Home is rebuilt on the AINPX framework, introducing a layered intelligence model and a restructured navigation experience that organizes platform management around core administrative jobs. Planning agent — MVP: Initial release of the Planning agent MVP; Hierarchical Agent - content framework; Cecurity bug mitigation Seismic-to-Lit conversion utility for the AINPX Console shell: Tooling that converts existing Seismic-based Console components to Lit, enabling the Console to run inside the AINPX shell. IA BU Onboarding — automated agent and skill creation: SKU-aware generation of agents and skills for business unit onboarding, with built-in validation and a common runtime. IA BU Onboarding — DARE runtime migration: Migration of existing configuration agents to the DARE runtime, plus generation of ITSM, ESM, CBS, and ITOM skills on DARE. Fixed: Includes defect fixes across the onboarding toolchain.|
|ServiceNow Otto for Setup Core|4.0.20|Changed: Layered intelligent Admin Home and navigation: Admin Home is rebuilt on the AINPX framework, introducing a layered intelligence model and a restructured navigation experience that organizes platform management around core administrative jobs. Planning agent — MVP: Initial release of the Planning agent MVP; Hierarchical Agent - content framework; Cecurity bug mitigation Seismic-to-Lit conversion utility for the AINPX Console shell: Tooling that converts existing Seismic-based Console components to Lit, enabling the Console to run inside the AINPX shell. IA BU Onboarding — automated agent and skill creation: SKU-aware generation of agents and skills for business unit onboarding, with built-in validation and a common runtime. IA BU Onboarding — DARE runtime migration: Migration of existing configuration agents to the DARE runtime, plus generation of ITSM, ESM, CBS, and ITOM skills on DARE. Fixed: Includes defect fixes across the onboarding toolchain.|
|ServiceNow Otto for Smart Assessment Engine|23.0.6|Changed: The AI suggestion icon in section navigation now appears only when suggestions are available for visible questions. Previously it also appeared when suggestions existed only for hidden questions.|
|ServiceNow Otto for Software Asset Management \(SAM\)|11.0.0|New feature: AI-powered Software spend detection - Reduce manual effort in classifying spend transactions with AI-powered software spend detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.|
|ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)|11.0.0|New: Case-to-Knowledge Article Generation: Generate a knowledge article from a single resolved or closed case, with Otto AI drafting content for review before publishing. Generate a comprehensive knowledge article from multiple related closed cases to document common issues at scale. AI Data Explorer – Multi-Table Support: AI Data Explorer can now correlate data across APO, SPO, and SLM tables \(including invoices, suppliers, approvals, purchase orders, and receipts\) to answer natural-language queries with a unified result. Introducing Action Fabric for Sourcing and Procurement Operations - requester-specific tools delivered via the SPO MCP Server and Tools Conversational Intake: Requesters can ask how-to and knowledge article questions and get routed to a pre-filled purchase requisition or sourcing request form based on their need. Status Visibility: Requesters can search for and view the status of any sourcing request, purchase requisition, purchase order, or procurement case they've submitted, including getting details about related tasks. Task Completion: Requesters can complete approval, sourcing, and receipt/acknowledgement tasks directly in conversation, including adding comments and stakeholders to watchlists, without navigating away. Some tasks \(e.g., signing a document or watching a video\) still require completion outside the conversation — customers can configure which task types route to this off-ramp experience. Changed: ZTSD Enhancements: Case resolutions now display the supplier invoice number instead of the internal ServiceNow-generated invoice number. Suppliers and employees can now view and accept or reject proposed resolutions directly from the case ticketing page through the employee slate or supplier portal. Other minor usability and experience improvements.|
|ServiceNow Otto for Strategic Portfolio Management|9.11.0|New: Self-guided “How it works” overview info \(i\) icon for AI-Identified Risks . This explains how AI detects, evaluates, scores, rationale, and the data considered for AI-identified risk. RIDAC menu now expands by default in the Project Workspace for visibility into sub-menus. Ability to clone the demand summarization skill and change the prompt. Changed: Minor enhancements for AI Status Reports. Enhanced Auto Email Insights with refinements and functional improvements. Automatic trigger for the demand summarization skill is changed to false. The default trigger of the skill has to be set to automatic to enable auto trigger.|
|ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)|9.0.1|New 1. Case-to-Knowledge article generation Generate a knowledge article from a single resolved/closed case, with Otto AI drafting content for your review before publishing. Generate a comprehensive knowledge article from multiple related closed cases to document common issues at scale. 2. AI Data Explorer – multi-table support AI Data Explorer now correlates data across APO, SPO, and SLO tables \(invoice, supplier, approval, PO, receipt\) to answer natural-language queries with a single unified result. 3. ZTSD enhancements Case resolutions now display the supplier invoice number instead of the internal ServiceNow-generated number. Suppliers and employees can view and accept/reject the proposed resolution directly from the case ticketing page via the employee slate or supplier portal. Other minor improvements.|
|ServiceNow Otto for Telecommunications, Media and Technology \(TMT\)|6.0.15|1. Fluent conversion of APP 2. Success Play Recommendation Skill 3. Executive Briefing on Executive portfolio dashboard 4. Engagement Insights nad breifing Skill|
|ServiceNow Otto for Telecommunications Service Management|2.3.1|Maintenance Only|
|ServiceNow Otto for Third-Party Risk Management|23.0.5|Changed Updated the dependency versions to take advantage of latest updates from the Third-party Risk management application. Refer to the dependency app store release notes for details.|
|ServiceNow Otto for Threat Intelligence Security Center|2.6.1|New AI-Powered Intelligence Processing imports threat advisories from PDF and image files and extracts structured indicators of compromise \(IOCs\), threat actors, malware, and campaigns. A review pane displays confidence scores and extraction reasoning, and an audit record is generated for every import.|
|ServiceNow Otto for Voice Agents|6.0.5|New Conversations tab in Assistant Designer: Review completed voice interactions, including outcomes, intents, authentication, invoked agents and tools, assist usage, and call recordings. Language support: Use Malay and Canadian English with new voice options. SIP custom headers: Add a custom outbound SIP header to support routing, tagging, and downstream context. Changed Language selection: Let callers select a language by keypad \(DTMF\) or voice, with custom retry and goodbye messages. Testing: Test voice assistants before completing all activation prerequisites. Call records: Capture complete latency data and keep multi-agent conversations together as a single interaction for more accurate evaluation and usage reporting. Fixed Fixed missing voice-call latency and tool-execution timing data. Fixed multi-agent calls being recorded as separate interactions. Fixed an issue where voice calls in the voice testing interface of Assistant Designer sporadically failed to connect on the first attempt. This issue is resolved in ServiceNow Otto for Virtual Agent version 20.0.8. Removed None|
|ServiceNow Studio|30.1.1|This app is a dependency of ServiceNow Studio + ServiceNow IDE. Please see release notes for parent app. New ServiceNow Studio quick start — an updated set of quick start topics to learn ServiceNow Studio efficiently. ServiceNow Studio user interface — personalize the new agentic-first UI by choosing your components: Pro \(all features\), Vibe mode \(minimal\), or Custom. Access ServiceNow Studio — reach ServiceNow Studio through several new access points across the ServiceNow AI Platform. Autonomous Engineer in Build Agent — ServiceNow Studio now supports Autonomous Engineer in Build Agent, which generates a complete implementation plan from your requirements. Changed ServiceNow Studio settings: User preferences and settings moved from the top-right to the bottom-left of the interface, where you can view what's new, open the command palette and keyboard shortcuts, and update preferences. App summary generation moves to an agentic architecture: ServiceNow Otto now generates app summaries with an AI agent instead of the previous skill-based model. Installing the App summary plugin now delivers the App Summary AI agent, which is off by default \(an admin must enable it in AI Agent Studio to avoid unexpected charges\). The end-user experience is unchanged. Deployment tab: Moved from the home page to the activity bar as a separate tab \(lists all update sets, applications, and deployment requests\). Removed Experience switcher: Removed from ServiceNow Studio; IDE capabilities are now consolidated under the Explorer tab. No direct replacement, but each application remains accessible on the ServiceNow AI Platform. Tools tab: Removed from the home page with no replacement; documentation for each tool is available under Integrated development tools for ServiceNow Studio. Create menu: The Create menu in the top-right corner is removed; the Create option in the activity bar remains and has the same functionality. Resources: The Resources section is removed from the home page. No direct replacement, but Build Agent users can prompt in the main chat to access resources.|
|Service Operations Workspace Admin Center|9.4.2|Compatible with latest ServiceNow release|
|Service Operations Workspace Core|9.4.2|Defect fixes|
|Service Operations Workspace ITSM Admin Center|9.4.2|Compatible with latest ServiceNow release|
|Service Operations Workspace ITSM Advanced Applications|9.4.2|Changed: Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.|
|Service Operations Workspace ITSM Applications|9.4.2|Changed: Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.|
|Service Operations Workspace ITSM Common|9.4.2|Changed: Updated plugin dependencies to ensure compatibility with the ServiceNow latest release.|
|Setup Hub|3.0.7|Changed: Layered intelligent Admin Home and navigation: Admin Home is rebuilt on the AINPX framework, introducing a layered intelligence model and a restructured navigation experience that organizes platform management around core administrative jobs. Planning agent — MVP: Initial release of the Planning agent MVP; Hierarchical Agent - content framework; Cecurity bug mitigation Seismic-to-Lit conversion utility for the AINPX Console shell: Tooling that converts existing Seismic-based Console components to Lit, enabling the Console to run inside the AINPX shell. IA BU Onboarding — automated agent and skill creation: SKU-aware generation of agents and skills for business unit onboarding, with built-in validation and a common runtime. IA BU Onboarding — DARE runtime migration: Migration of existing configuration agents to the DARE runtime, plus generation of ITSM, ESM, CBS, and ITOM skills on DARE. Fixed: Includes defect fixes across the onboarding toolchain.|
|Setup Hub Common|5.0.7|Changed: Layered intelligent Admin Home and navigation: Admin Home is rebuilt on the AINPX framework, introducing a layered intelligence model and a restructured navigation experience that organizes platform management around core administrative jobs. Planning agent — MVP: Initial release of the Planning agent MVP; Hierarchical Agent - content framework; Cecurity bug mitigation Seismic-to-Lit conversion utility for the AINPX Console shell: Tooling that converts existing Seismic-based Console components to Lit, enabling the Console to run inside the AINPX shell. IA BU Onboarding — automated agent and skill creation: SKU-aware generation of agents and skills for business unit onboarding, with built-in validation and a common runtime. IA BU Onboarding — DARE runtime migration: Migration of existing configuration agents to the DARE runtime, plus generation of ITSM, ESM, CBS, and ITOM skills on DARE. Fixed: Includes defect fixes across the onboarding toolchain.|
|Setup Hub Config|5.0.5|Changed: Layered intelligent Admin Home and navigation: Admin Home is rebuilt on the AINPX framework, introducing a layered intelligence model and a restructured navigation experience that organizes platform management around core administrative jobs. Planning agent — MVP: Initial release of the Planning agent MVP; Hierarchical Agent - content framework; Cecurity bug mitigation Seismic-to-Lit conversion utility for the AINPX Console shell: Tooling that converts existing Seismic-based Console components to Lit, enabling the Console to run inside the AINPX shell. IA BU Onboarding — automated agent and skill creation: SKU-aware generation of agents and skills for business unit onboarding, with built-in validation and a common runtime. IA BU Onboarding — DARE runtime migration: Migration of existing configuration agents to the DARE runtime, plus generation of ITSM, ESM, CBS, and ITOM skills on DARE. Fixed: Includes defect fixes across the onboarding toolchain.|
|Setup Hub Content|5.0.7|Changed: Layered intelligent Admin Home and navigation: Admin Home is rebuilt on the AINPX framework, introducing a layered intelligence model and a restructured navigation experience that organizes platform management around core administrative jobs. Planning agent — MVP: Initial release of the Planning agent MVP; Hierarchical Agent - content framework; Cecurity bug mitigation Seismic-to-Lit conversion utility for the AINPX Console shell: Tooling that converts existing Seismic-based Console components to Lit, enabling the Console to run inside the AINPX shell. IA BU Onboarding — automated agent and skill creation: SKU-aware generation of agents and skills for business unit onboarding, with built-in validation and a common runtime. IA BU Onboarding — DARE runtime migration: Migration of existing configuration agents to the DARE runtime, plus generation of ITSM, ESM, CBS, and ITOM skills on DARE. Fixed: Includes defect fixes across the onboarding toolchain.|
|SGC Central|2.7.2|Changed Backend updates for AI Service Graph Connectors.|
|Shift Handover Application|2.1.0|Fixed The improper handling of Daylight Saving Time \(DST\) in shift handover log creation has been resolved. Shift logs now correctly account for DST transitions. The 'Change to "In Progress" State' button has been fixed and now functions as expected.|
|SLO - Foundation|2.0.2|Changed The application captures dependencies. The plugin dependencies were updated in this release.|
|SLO - Prime|2.0.0|Changed The application captures dependencies, The plugin dependencies were updated in this release.|
|Smart Assessment Core|23.0.2|New Name another user to act on your assessments on your behalf for a set period, using the standard platform delegate feature. A delegate of the primary responder can respond to and submit the assessment; a delegate of the requestor can cancel, reassign, and edit the due date. Delegation is off by default and is enabled from template category. The assessment template category form includes two new fields: QB category roles, which controls access to the question banks associated with the category, and Allow user delegation, which lets users delegate their assessments in the category.|
|Smart Assessment Migration tools|23.0.3|New Smart Assessment admins can now migrate Metric Categories and Metrics from the classic Question Bank into the Smart Assessment Engine Question Bank.|
|sn-attach-article-guidance|32.0.1|New: Recommended actions now support the new Attach Knowledge and Relevant Case guidances for AI Search results that surface on CRM workspace.|
|sn-component-guidance-experience|42.0.2|New: Recommended actions now support the new Attach Knowledge and Relevant Case guidances for AI Search results that surface on CRM workspace.|
|sn-cwm-agile|2.2.1|Fixed Security fixes. Minor fixes to the menu option for opening a record.|
|sn-docs|7.9.1|New Dynamic content and templates for Project Docs - Project Docs users can enable dynamic content in Docs and Docs Templates, using the same fields as status reports. Two default templates, project charter and project closeout, are provided. Users can select and configure dynamic templates within Docs for their projects. Customer usage metrics for Docs and Project Workspace - The system tracks the number of customers creating dynamic content in Docs and Docs Templates, exporting the RIDAC grid, and using the new list view L1 menu in Project Workspace. Configurability for default AI Status Report template - Admins can configure which AI Status Report template is used by default.|
|sn-formula-kit|1.2.2|Fixed Updated version for family compatibility.|
|sn-next-best-action-list|41.0.4|New: Recommended actions now support new guidances, 'Attach Knowledge' and 'Relevant Case' for AI Search results that surface on the CRM workspace.|
|sn-smart-assessment-connected|23.0.4|New: Review a log of every response, justification, and flag-state change made to a question throughout the lifecycle of an assessment, including who made each change and when. Consecutive changes to the same field by the same user within a configurable time window are merged into a single entry, while flag-state changes are always logged individually. Changed: Reopening a drop-down question now shows all response options again, not just the ones user had previously selected. For single-select and multi-select reference questions, when a table has more than 10 matching records, select the search icon to browse the full set. This replaces the default behavior of showing only the first 10 records. Opening an assessment now lands on the assessment instructions, if configured, or otherwise the first question of the first section or subsection. This applies even if you or a collaborator already answered later questions. Sections with an incomplete mandatory justification or attachment in one or more questions now show an exclamation-circle icon with the tooltip "Incomplete response" in navigation. Previously the section in navigation used the same flag icon used for question level flagging, which made the two indicators hard to distinguish. Fixed: Section and subsection descriptions now render line breaks correctly in assessments.|
|sn-smart-assessment-designer|23.0.5|NEW Question Bank Build a centralized library of reusable questions with full lifecycle management. Questions move seamlessly through Draft → Ready to Publish → Published → Retired states, enabling version control and compliance tracking across all assessment templates. Independent Question Copies Published questions remain isolated when added to templates. Edit a question in your template without affecting the original, and vice versa—full customization freedom with zero cross-contamination. CHANGED Unsaved Changes Across Tabs Your work is preserved instantly. Draft changes now persist across all workspace tabs—General, Questions, Automations, and Scoring. A visual dirty-state indicator on the workspace selector shows pending changes at a glance, so you never lose progress.|
|sn-task-planner|22.15.0|New: Track planned and actual effort directly on the Planning page. Planned effort rollup is available in the task planner, and the actual effort field is read-only, consistent with forms. Effort rollup logic respects business rule flow settings and avoids duplication. Maximum units are enforced based on dictionary configuration and validated against task duration. Changed: Edit parent task constraint dates directly in the task planner. Child task start dates honor both parent and parent constraint dates, supporting all combinations of child task constraint types. Fixed: Resolved an issue where planned duration did not display correctly after indenting a task created through an MPP file import. The value now updates as expected when the date format is refreshed in Project Workspace. Resolved an issue where reference qualifiers for sub-projects on the Project Workspace Planning page did not function as intended. Resolved an issue where copy-pasted project tasks were not editable as expected.|
|Software Asset Management|4.1.7|This release enhances resource value capabilities and fixes critical defects affecting deduplication and installation unlicensed reasons—ensuring consistent, reliable system behavior across these areas.|
|Software Asset Management AI Advanced|2.5.0|New feature: AI-powered Software spend detection - Reduce manual effort in classifying spend transactions with AI-powered software spend detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.|
|Software Asset Management AI Prime|2.5.0|New feature: AI-powered Software spend detection - Reduce manual effort in classifying spend transactions with AI-powered software spend detection. The Software Asset Workspace now automatically identifies software purchases from imported transactions, extracts publisher and product details, and matches them to your Software Asset Management Content Library.|
|SOM for Manufacturing Advanced|3.0.0|This app will be hidden on the store. No listing content is applicable for this store app.|
|SOM for Manufacturing Prime|3.0.0|This app will be hidden on the store. No listing content is applicable for this store app.|
|Source-to-Pay Common Architecture|25.0.0|New: Admins can access SPO Product Admin Home as a single entry point. Product Hub provides guided installation of SPO applications and plugins. Configuration Console offers a guided experience for configuring Procurement Case Management items with completion tracking. From Configuration Console, Admins can download update sets and upload batch update sets to higher environments. Changed: SPO configuration is now structured within Otto for Setup framework, replacing fragmented navigation across multiple admin tools and locations. Admin experience is consistent across Product Hub and Configuration Console.|
|Source-to-Pay Workspace|21.0.0|New: Admins can access SPO Product Admin Home as a single entry point. Product Hub provides guided installation of SPO applications and plugins. Configuration Console offers a guided experience for configuring Procurement Case Management items with completion tracking. From Configuration Console, admins can download update sets and upload batch update sets to higher environments. Changed: SPO configuration is now organized within the Otto for Setup framework, replacing navigation across multiple admin tools and locations. The admin experience is now consistent across Product Hub and Configuration Console.|
|Sourcing and Purchasing Automation|11.7.0|New: Admins can access SPO Product Admin Home as a single entry point. Product Hub provides guided installation of SPO applications and plugins. Configuration Console provides a guided experience for configuring Procurement Case Management items, including completion tracking. From Configuration Console, admins can download update sets and upload batch update sets to higher environments. Changed: SPO configuration is now organized within the Otto for Setup framework, replacing navigation across multiple administrative tools and locations. The administrative experience is now consistent across Product Hub and Configuration Console. Semantic configurations are now aligned with the applications that own the associated data tables.|
|SPM Common UI Component|4.1.1|Changed: Updated SPM Common UI Component for compatibility with the Brazil release.|
|SPM Enterprise-Wide Deployment|1.0.5|New: Control system administrator access to data across all partitions using a system property. By default, system administrators no longer have access to all partitions. Fixed: Resolved a field visibility issue for non-admin users in the Details section of the Project Type tab.|
|SPM Planning Attributes Core|1.18.3|New Error messages are now logged in the Resource assignment Auto sync flow, so administrators can review stack traces for troubleshooting. Added tests to improve reliability. Fixed Fixed an issue where the assignment type for Operational work resource assignment records was inconsistent for users with the resource manager role. Top-level operational work assignments are now correctly set to the Group assignment type. Fixed an issue where migrating resource plans to resource assignments produced incorrect booking types and aggregate categories for daily records. The booking type for daily records is now set to HARD, and aggregates display the correct Project allocated category. Fixed an issue where the Allocation modal in Resource Management Workspace included pending and unapproved resource assignments in allocation calculations when the relevant Resource Management property was enabled. The modal now excludes these assignments from calculations, and the top message accurately reflects the actual assignment status. Fixed an issue where effort values in the resource board Person days view didn't update correctly when primary attribute values were populated. The population script now excludes inactive attribute values, ensuring accurate effort calculations and display. Fixed an issue where editing the Updated on field for resource assignments in the project workspace Planning tab returned an insufficient privileges error. Permissions are now handled correctly when the Updated on and Updated by fields are added to the bottom tray for resource assignments. Fixed an issue where primary attribute value population scripts included inactive attribute values, such as groups and roles. The scripts now exclude inactive values, so only active attributes are considered during population. Fixed an issue where the Resource termination handler didn't handle resource assignments consistently. Assignments now update automatically when allocations are deleted or end dates are adjusted, including parent-child hierarchy handling and effort rollup. Assignments with start dates after an employee profile's end date are deleted automatically.|
|SPO - Foundation|2.0.0|The application captures dependencies, updated the plugin dependencies for this release.|
|SPO - Prime|2.0.0|The application captures dependencies, updated the plugin dependencies for this release.|
|Strategic Planning|4.18.0|New: Status is automatically calculated for targets based on a configurable threshold system property, and rolls up from targets to goals. Access portfolio risks, issues, decisions, actions, and changes \(RIDAC\) directly from the portfolio plan using the dedicated RIDAC page. Access program planning views from the new Programs menu. Select any program to open its dedicated plan with Prioritization, Roadmap, Kanban, and Financials views. Added automated email notifications for scenario approval. The My Demands widget is added to the Employee Slate canvas. Requesters can add the My Demands widget to their Employee Slate canvas to track the state of their demands. Requesters can view and track their demands directly from the My Demands widget. The widget lists all demands created by the requester, with filters by state and links to the standard demand tracking experience. When a demand is converted to an execution artifact, such as a project, epic, or story, requesters can view high-level status, planned and actual end dates, and the last update from the Execution Tracking widget. The demand details page includes the lifecycle tracker, activity, attachments, and edit tabs. Requesters can view the demand lifecycle, activity history, attachments, and edit key fields from the standard ticket page. Demands submitted by requesters appear in the My Requests list, alongside other requests, with consistent state and status display. Financial widgets have info icons explaining the values and how the calculation is done.|
|Strategic Portfolio Management - Advanced|1.3.0|New Added AI Native SKU support for SPM Advanced, enabling access to advanced Strategic Portfolio Management features powered by AI capabilities.|
|Strategic Portfolio Management - Prime|1.2.0|New: Added AI Native SKU support for SPM Prime, enabling access to advanced AI-driven features, workflows, and automation capabilities.|
|Summarization for Order Management|2.2.4|Maintenance release. Contains internal code updates with no impact to existing functionality or user-facing behavior.|
|Supplier Case Management|12.0.0|Changed Migration of code to Fluent|
|Supplier Collaboration Portal|12.0.0|Changed Migration of code to Fluent Provide ability to view status of supplier onboarding requests|
|Supplier Common Architecture|12.0.0|Changed Migration of code to Fluent Enhance supplier data model to capture supplier category and sub-category|
|Supplier Operations|8.0.0|Changed Migration of code to Fluent|
|Supplier Payment Optimization|7.0.0|Changed Migration of code to Fluent|
|Supplier Relationship and Performance Management|11.0.0|Changed Migration of code to Fluent|
|Task Communications Management UI Components for Configurable Workspaces|9.4.3|-Compatible with latest ServiceNow release|
|Task Plan Template AI Agents|2.0.1|New AI-powered template creation from your documents and diagrams: Upload your process documents or diagrams, and our AI agent reads through them, finds the tasks and dependencies. Template AI agent converts the identified tasks into template and template items and creates a draft template for you to review and edit. Duplicate template detection: When you create a new task plan template, the system shows you similar existing templates that already exist in your system. Review them, select one before proceeding. ServiceNow Otto panel discoverability and UI action for template creation: The template creation workflow is accessible from ServiceNow Otto panel and from the task plan template list itself. Start creating templates from wherever you are in the system.|
|Task Plan Templates|5.0.0|Admins and template authors can now configure advanced conditions on template items using referenced fields from parent or target tables. The Template Item Condition table supports both simple and advanced modes, enabling conditions based on related tables and mapping fields. Dynamic field visibility and mandatory validation are enforced, with error messages shown for missing required fields. Template authors can now define and propagate three new tracking fields for generated records. Template Item and Template Item Config forms expose item, execution, and business organization tracking fields, allowing authors to configure back-reference tracking for generated records. These fields are visible and editable in the UI, with dependent visibility and updated labels. Multi-case task dependencies and document associations are now supported at scale. Dependency relationships and document links are created for all generated records across multiple stores, with optimized insert paths to handle large volumes efficiently. Feature hooks for dependency and document association fire exactly once per execution after all workers finish. Clone feature now supports affected stores and dependencies. When cloning a template, all related features—including affected stores, scheduling details, and dependencies—are cloned, ensuring complete plans without manual setup. Cloned dependent tasks are maintained and visible in relevant tables. Document references are maintained during task generation and template cloning. Generated tasks refer to documents attached to template items, and cloned templates preserve document associations. Cascade confirmation popup added for template item configuration changes. When updating configuration fields, admins are prompted to cascade changes to existing template items, ensuring consistent tracking across linked items. Workspace and platform UI layouts updated for advanced condition fields. New fields are added to form and list layouts, with conditional visibility and proper spacing across all views. White papers available for multi-case changes and Task Plan Template features. Comprehensive documentation covers design, functionality, and usage for stakeholders.|
|Technology Advanced|1.0.12|SKU Application Plugin - No code delievered|
|Technology Foundation|1.0.15|SKU Application Plugin - No code delievered|
|Technology Prime|1.0.12|SKU Application Plugin - No code delievered|
|Telecommunications, Media and Technology - Advanced|1.0.11|SKU apps - no code delievered|
|Telecommunications, Media and Technology - Foundation|1.0.13|SKU Application Plugin - No code delievered|
|Telecommunications, Media and Technology - Prime|1.0.11|SKU apps - no code|
|Telecommunications Advanced|2.3.1|Maintenance only|
|Telecommunications Foundation|2.3.1|Maintenance Only|
|Telecommunications Prime|2.3.1|Maintenance only|
|Third-party Risk Due Diligence|23.0.5|New Added engagement and element relationship handling for due diligence. Added element collection task integration with the due diligence workflow. Added dynamic attributes, classifications, and AI model configuration for elements. Added risk-rating rollups across engagement and element relationships. Changed Added internal task support and task-type metadata. Improved third-party and engagement element access controls. Added global AI model availability for vendor contacts. Updated scheduled-rule date handling for local time zones. Added assignment-group filtering and updated due diligence workflow behavior. Fixed Corrected element-name uniqueness per vendor \(PRB2067427\). Fixed validation that engagements and elements belong to the same third party \(PRB2067085\). Corrected AI model dynamic attribute naming and classification feedback \(PRB2057733\). Fixed third-party prepopulation when creating elements \(PRB2057048\). Corrected scheduled event rules executing every other day \(PRB2055615\). Fixed assignment-group filtering and related due diligence behavior \(PRB2028131\).|
|Third-party Risk Management|23.0.7|New Added engagement and element risk-rating calculations. Added element-assessment evidence rollups and deduplication. Added internal task management and responder actions. Added SAE questionnaire notifications and assessment improvements. Added AIDE semantic configurations and SBOM-related enhancements. Changed Expanded risk-rating calculations across vendor, engagement, and element relationships. Added task types, internal-task access, and responder permissions. Updated assessment reassignment and issue-generation behavior. Improved role exclusions, ACL conditions, and secure query handling. Fixed Corrected issue-generation handling for invalid or hidden SAE questions \(PRB2021879\). Fixed vendor assessment reminder failures when due dates are missing \(PRB2029246\). Corrected document-link navigation from internal assessments \(PRB2030116\). Fixed risk ratings not being set after assessment submission \(PRB2034741\). Corrected exclusion mappings for assessment responder and business-user roles \(PRB2039159\). Fixed SBOM product-model creation after document processing \(PRB2052847\).|
|Third-party Risk Management Advanced|23.0.3|Changed Updated the dependency versions to take advantage of latest updates from the Third-party Risk management application. Refer to the dependency app store release notes for details.|
|Third-party Risk Management Professional Plus|23.0.3|Changed Updated the dependency versions to take advantage of latest updates from the Third-party Risk management application. Refer to the dependency app store release notes for details.|
|Threat and alert data feeds for Crisis Management|12.0.1|Fixed Issue – Feed Record State Transition Bug Details - Corrected the Feed state transition logic to set the process state to 'Transferred' when an Alert is successfully created from a Feed update. This ensures Feed records remain available for audit/tracking and prevents premature Alert dismissal.|
|Threat Intelligence Security Center - Advanced|3.3.1|New AI-Powered Intelligence Processing imports threat advisories from PDF and image files and extracts structured indicators of compromise \(IOCs\), threat actors, malware, and campaigns. A review pane displays confidence scores and extraction reasoning, and an audit record is generated for every import.|
|Threat Intelligence Security Center for Security Operations|4.8.1|New AI-Powered Intelligence Processing imports threat advisories from PDF and image files and extracts structured indicators of compromise \(IOCs\), threat actors, malware, and campaigns. A review pane displays confidence scores and extraction reasoning, and an audit record is generated for every import. CrowdStrike Next-Gen SIEM Integration enables analysts to search Falcon Next-Gen SIEM for observable sightings from the Threat Intelligence Library, case artifacts, or automated workflows. Matching results are saved as sighting records on the observable. CrowdStrike Vulnerability Intelligence Feed Integration ingests vulnerability intelligence data from CrowdStrike and correlates it with threat intelligence to provide enriched security context. SIR-TISC Integration lets analysts link entities to security incidents directly from the Security Incident Response workspace or an entity record, without first creating a Threat Intelligence Security Center case. Support for indicator and object creation during investigations enables analysts to create and link new indicators and intelligence objects directly within the investigation workflow. Observable extraction from STIX indicators automatically extracts observables from STIX indicator pattern values during ingestion, adds them to the Threat Intelligence Library, and relates them to the parent indicator. Changed Auto-correlation enhancements improve relationship accuracy by applying reputation-based correlation and direction-agnostic deduplication. Potential correlation rules are now more selective, requiring a reputation match and multiple shared observables. SIR-TISC Integration now supports bidirectional linking and unlinking of Threat Intelligence Security Center entities from the TISC Context tab in the Security Incident Response workspace. CrowdStrike Falcon EDR Integration now sends indicators with TISC Intelligence as the source, supports configurable indicator expiration, and adds the Prevent action in addition to Detect. Intelligence processing performance improvements accelerate the processing of imported intelligence records from the Threat Intelligence Library and cases. Relationship validation prevents the creation of self-relationships across all creation methods, including event ingestion. CrowdStrike Vulnerability Intelligence Feed configurations become read-only after activation to prevent changes that could interrupt ongoing ingestion. MITRE ATT&amp;CK ingestion now provides a review queue for revoked technique-to-tactic associations that are no longer defined in newer ATT&amp;CK versions. Fixed Resolved an issue that could cause autocorrelation processing to run indefinitely during CrowdStrike ingestion when record mismatches occurred. Updated the WHOIS Integration to support recent API changes. Fixed an issue where custom headers in Outbound Intelligence Profiles could be overwritten by default Accept and Content-Type headers. Fixed an issue where RSS tags did not consistently sync to entity tags. Entity-to-tag records older than 30 days are now cleaned up automatically. Improved webhook event processing and intelligence object processing performance. Fixed an issue where deleted indicators from the CrowdStrike feed were not imported correctly. Resolved a STIX payload processing issue caused by null values in optional fields. Fixed an issue that could cause Threat Intelligence Security Center cases to be created without a Case ID during bulk or concurrent record insertion. Fixed an issue that prevented analysts from adding observables to a security incident from a Threat Intelligence Security Center case. Fixed an issue where filtered CrowdStrike ingestion results did not match the records displayed in the CrowdStrike console.|
|Threat Intelligence Support Common|13.8.0|New: Integrated Mitre Atlas Fixed: The observable identification logic has been corrected when adding an observable. Observables are now accurately recognized and processed during creation. UI message translations have been updated to resolve previous inconsistencies. User-facing messages now display correctly in supported languages.|
|TNI - Advanced|2.3.0|recertification for Brazil|
|TNI - Advanced|2.3.0|recertification for Brazil|
|TNI and DCNAM AI Content Collection|2.3.0|recertification for Brazil|
|TNI and DCNAM AI Content Collection|2.3.0|recertification for Brazil|
|TSOM - Advanced|2.3.0|Recertification for Brazil|
|TSOM - Prime|2.3.0|Recertification for Brazil|
|UI Components of Collaboration for Configurable Workspaces|9.4.2|Compatible with latest ServiceNow release|
|Unified Content Management|23.0.5|New Regulatory content updates are now delivered dynamically via Content Delivery Service \(CDS\), decoupling content from UCM application upgrades Administrators can receive the latest regulatory framework content automatically, without manual upgrades or reconciliation. Plugin compatibility filtering is now supported for UCM content The system evaluates whether content is compatible with the current instance based on plugin and version requirements, ensuring only relevant content is installed. Error handling and rollback for content imports are now supported Failed installs aggregate errors and roll back partial inserts, with error details visible in the UI. Admins can now highlight AI-assisted records with an AI icon in list views Records generated via AI are visually distinguished for easier identification. Zurich platform support is restored for Cobalt Raven ACLs ACLs have been restructured to enable compatibility with both Zurich and Australia platforms. Boolean values and authority document handling for AI risk and compliance content have been corrected Content for these domains is now accurately captured and processed. Changed Parent-staging tables now include plugin compatibility columns New fields for target plugin, minimum, and maximum compatible version are added, inherited by child tables, with existing records unaffected. CDS client-side changes enable automated data synchronization from CDS Server Instances with UCM plugin can now pull content and store it in pre-staging tables, with updated ACLs for enhanced security. UI actions for extracting and verifying pre-staging records are now available Admins can validate content preparation directly from the interface.|
|Unified Developer Core|30.1.0|Maintenance release.|
|Usage Insights Application|6.4.2|Page properties support to get granular insights of pages. Answers business questions like : How many password-reset requests were submitted by people who visited the password-reset catalog page? How many comments were added to the knowledge article titled “Usage Insights MCP”? Which dashboards did people visit last quarter, listed by name? Page properties are now available across User Experience Analytics. A page property is a named, filterable attribute captured from a page's URL parameters or record metadata on every page view — so pages that previously shared a single page ID \(a dashboard, a knowledge article, a catalog item\) can now be distinguished by the resource a person actually viewed. Page properties behave like event properties wherever properties already appear. What's new Filters now support pages. The filter panel previously surfaced event properties only; you can now select a page and filter by its page properties alongside events. Page-property distribution in the Properties section. Each page property's value distribution renders as a pie chart, matching how event-property distributions are already shown. Dedicated page properties in the Pages menu. The Pages menu now includes a dedicated page-properties view, letting you filter by an individual page property. Page properties in Advanced filters. When you select a page in advanced filters, you can choose that page's properties from a dropdown to refine the query. Page-property filtering in Funnels. When a funnel step is set to a page, page properties become available for that step, so you can filter the step by page property.|
|Usage Insights Commons|6.4.2|Not visible on UI, internal apps.|
|Usage Insights Commons Connected|6.4.2|Not visible on UI, internal apps.|
|Usage Insights Funnel Core|6.4.2|Not visible on UI, internal apps.|
|Usage Insights in Data Visualizations|6.4.2|Page properties are not supported in Platform Analytics dashboard visualizations in this release.|
|Usage Insights Pages|6.4.2|Not visible on UI, internal apps.|
|Usage Insights Query Builder|6.4.2|Not visible on UI, internal apps.|
|Usage Insights Query Builder Core|6.4.2|Not visible on UI, internal apps.|
|Usage Insights Request Manager|6.4.2|Not visible on UI, internal apps.|
|Value dashboard for AI Control Tower|7.0.6|Added support for Domain Separation in AICT Value. Product Owners can now easily identify and work with the AI systems and key metrics that matter most to them.|
|Value Engine|7.0.6|Added support for Domain Separation in AICT Value. Product Owners can now easily identify and work with the AI systems and key metrics that matter most to them.|
|Virtual Agent API|4.4.3|New Changed Backend changes to support monthly releases. Fixed Removed|
|Walk-up Experience for Service Operations Workspace|9.4.2|Compatible with latest ServiceNow release|
|WebRTC Voice|1.0.7|Initial release|

|App name|Version number|Last updated|
|--------|--------------|------------|
|@devsnc/behavior-form-intent-translator|29.0.9|2026-03-12|
|@devsnc/behavior-list-intent-translator|29.0.9|2026-03-12|
|@devsnc/behavior-uibtk-media|29.1.71|2026-03-12|
|@devsnc/behavior-uibtk-supporting-records|29.1.71|2026-03-12|
|@devsnc/behavior-ui-interaction|29.1.14|2026-03-12|
|@devsnc/library-uibtk-caching|29.1.71|2026-03-12|
|@devsnc/library-uibtk-commons|29.1.71|2026-03-12|
|@devsnc/library-uibtk-macroponent|29.1.71|2026-03-12|
|@devsnc/library-uibtk-screen|29.1.71|2026-03-12|
|@devsnc/library-uibtk-undo-redo|29.1.71|2026-03-12|
|@devsnc/library-uibtk-uxvalue|29.1.71|2026-03-12|
|@devsnc/library-uibtk-ux-value-resolver|29.1.71|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-devops-pipeline|21.0.5|2022-08-04|
|@devsnc/sn-feedback|2.0.0|2025-12-11|
|@devsnc/sn-help-setup|29.0.0|2026-03-12|
|@devsnc/sn-interaction-builder|29.1.37|2026-03-12|
|@devsnc/sn-list-selector|26.1.3|2026-03-12|
|@devsnc/sn-uibtk-actionable-list-item|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-builder-in-builder|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-client-state-config-panel|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-conditional-renderer|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-content-tree-picker|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-create-page|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-data-navigator|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-diff-renderer|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-domain-picker|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-draggable-dialog|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-draggable-list|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-editor-header|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-element-context-menu|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-element-navigator|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-element-properties-configuration-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-events-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-experience-assistant|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-extension-point-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-features-catalog-modal|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-form-factor-controls|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-formula-builder|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-icon|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-instance-config-editor|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-is-hidden-property-input|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-json-navigator|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-loader|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-mcp-event-definitions-config-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-mcp-props-config-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-menu-elements|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-minimized-dialogs-dropdown|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-modal|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-param-row|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-placeholder|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-preset-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-props-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-replace-component|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-scope-picker|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-script-config-panel|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-shelf-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-site-map|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-stage-preview|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-stage-scale-controls|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-style-pane|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-style-provider|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-style-select|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-tabs|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-test-values-editor|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-text-link|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-toolbox|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-transaction-alert|29.1.71|2026-03-12|
|@devsnc/sn-uibtk-viewport-config-panel|29.1.71|2026-03-12|
|@devsnc/sn-ui-interaction-modals|29.1.14|2026-03-12|
|@devsnc/sn-vtb|26.0.0|2025-12-11|
|@devsnc/uibtk-api|29.1.71|2026-03-12|
|@devsnc/uibtk-uxf-assets|29.1.71|2026-03-12|
|@servicenow/sn-ai-engagement-experience|3.6.4|2026-09-10|
|@servicenow/sn-builder-core|29.1.59|2026-03-12|
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
|@servicenow/sn-component-builder|29.1.32|2026-03-12|
|@servicenow/sn-controller-builder|29.1.30|2026-03-12|
|@servicenow/sn-enhanced-content-editor|31.26.1|2026-09-10|
|@servicenow/sn-next-experience-all-menu-editor|29.1.81|2026-03-12|
|@servicenow/sn-preset-builder|29.1.28|2026-03-12|
|360 degree relationship visualization|22.3.0|2026-06-16|
|ACC Admin Workspace|1.0.0|2025-12-11|
|Access Analyzer|6.0.6|2026-05-21|
|Access Management Automation|2.1.0|2023-12-07|
|Access Management Flow Wizards|1.0.1|2021-09-16|
|Accounts Payable Invoice Processing|13.2.7|2026-09-10|
|Accounts Payable Operations integration with Document Intelligence|13.2.5|2026-09-10|
|ACL Assessment for Reports|3.1.2|2025-01-30|
|Action Status Automation|2.0.0|2026-03-12|
|Activity Timer|1.0.2|2026-03-12|
|Admin Center|6.2.1|2026-08-07|
|Admin Experience for Hardware Asset Management|1.0.0|2026-09-10|
|Admin Experience Framework|5.3.0|2026-03-12|
|Admin Workspace for Service Providers \(SPs\)|1.1.4|2025-07-31|
|Adobe Experience Platform Spoke|2.2.0|2025-01-02|
|Adobe Sign Spoke|2.7.2|2025-10-16|
|Advanced AI Search Management Tools|8.0.1|2025-12-11|
|Advanced Appointment Booking|30.0.1|2026-03-12|
|Advanced Approval Management|2.6.0|2026-09-10|
|Advanced Approval Management AI|1.2.2|2026-09-10|
|Advanced Promotion Engine|4.2.1|2025-12-11|
|Advanced Recommended actions for ITSM|8.1.0|2025-09-10|
|Advanced Response Automation for Smart assessments|23.0.2|2026-09-10|
|Advanced Work Assignment for CSM|1.0.4|2026-03-12|
|Advanced Work Assignment for Legal Service Delivery|1.1.1|2025-06-05|
|Advanced Work Assignment for Source-to-Pay Operations|3.1.1|2025-12-11|
|Advanced Work Assignment for Supplier Lifecycle Operations|10.0.0|2026-09-10|
|AES Application Object Templates|29.2.6|2026-08-07|
|AES Application Object Wizard Components|29.2.6|2026-08-07|
|AES Catalog Builder|28.2.1|2025-12-11|
|AES Catalog Builder Wizard|28.2.1|2025-12-11|
|AES Decision Table Builder Templates|4.0.0|2023-02-02|
|AES Decision Table Builder Wizard|4.0.0|2023-02-02|
|AES Flow Templates|28.2.1|2025-12-11|
|AES Flow Wizards|28.2.1|2025-12-11|
|AES Mobile Templates|28.2.1|2025-12-11|
|AES Mobile Wizards|28.2.1|2025-12-11|
|AES Notification Builder Component|28.2.1|2025-12-11|
|AES Portal UI Template|28.2.1|2025-12-11|
|AES Role Builder|28.2.1|2025-12-11|
|AES Role Builder Component|28.2.1|2025-12-11|
|AES Table Builder Wizard|28.2.1|2025-12-11|
|AES UI Template Wizards|28.2.1|2025-12-11|
|AES Workspace UI Template|28.2.1|2025-12-11|
|Agency Support Model|4.0.1|2026-09-10|
|Agent Client Collector for Investigation|9.4.2|2026-09-10|
|Agent Client Collector for Security Incident Response|20.2.0|2023-05-04|
|Agent Client Collector for Visibility Content|2.0.4|2026-09-10|
|Agent Client Collector Framework|7.0.4|2026-09-10|
|Agent Client Collector Log Analytics|3.9.1|2025-12-11|
|Agent Client Collector Monitoring|3.16.1|2026-01-20|
|Agent Client Collector Spoke|1.1.5|2024-01-04|
|Agent Forecast|5.7.0|2025-12-11|
|Agentic Contact Center for Banking|1.4.5|2026-09-04|
|Agentic Contact Center for Insurance|1.3.3|2026-09-04|
|Agent-Initiated Messaging Interface|1.0.22|2026-03-12|
|Agent Messaging Component|3.0.17|2026-03-12|
|Agent Workspace for HR Case Management|4.6.2|2026-08-07|
|Agile Development v2|1.1.0|2023-02-02|
|Agile Integrations Common|1.4.0|2025-12-11|
|Aha! Spoke|1.7.2|2026-01-20|
|AI Admin Center|6.0.7|2026-09-10|
|AI Admin Hub|10.3.4|2026-09-10|
|AI Agent Advisor|1.4.5|2026-09-10|
|AI agents and skills for Quote Management|3.0.1|2026-07-09|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for AIOps|1.12.3|2026-09-10|
|AI Agents for Core Business Suite|3.3.2|2026-08-07|
|AI Agents for Core Business Suite|3.3.2|2026-08-07|
|AI Agents for CSM - Complaint Case|1.5.1|2026-08-07|
|AI Agents for Customer Success Management|2.7.21|2026-09-10|
|AI Agents for Discovery|3.2.2|2026-09-10|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.4|2026-08-07|
|AI Agents for Enterprise|1.0.1|2026-09-10|
|AI Agents for Health and Safety|1.3.4|2026-07-09|
|AI Agents for Health Log Analytics|2.5.0|2026-09-10|
|AI Agents for HR Service Delivery|7.3.1|2026-09-10|
|AI Agents for ITAM|5.0.0|2026-09-10|
|AI Agents for Meetings|1.0.10|2026-09-10|
|AI Agents for Retail Service Management|1.6.0|2026-09-10|
|AI Agents for Service Exchange Provider|1.1.12|2026-08-13|
|AI agents for SLO|2.2.2|2026-09-10|
|AI agents for Synthetic Monitoring|1.4.4|2026-07-09|
|AI Agents for Talent|6.0.0|2026-08-07|
|AI Agents for Telecommunications, Media and Technology|6.2.1|2026-09-10|
|AI Agents for Universal Request|1.1.3|2026-09-10|
|AI Agents for Workplace Service Delivery|3.3.8|2026-08-07|
|AI Agents Platform Usecase|1.0.5|2025-03-12|
|AI Analytics|5.3.5|2026-09-10|
|AI Asset Management|6.1.2|2026-09-10|
|AI Authoring for Catalog Builder|8.0.3|2026-09-10|
|AI Case Management|23.0.2|2026-09-10|
|AI Control Tower|7.1.1|2026-09-10|
|AI Control Tower Core|8.5.7|2026-09-10|
|AI Control Tower - Evaluations|4.0.1|2026-09-10|
|AI Control Tower for Enterprise AI Foundation|1.9.2|2026-09-10|
|AI Control Tower for ServiceNow Otto|7.0.3|2026-09-10|
|AICT UI Application|3.0.4|2026-09-10|
|AI Dashboard Insights|1.3.4|2026-08-07|
|AI Data Explorer|5.2.7|2026-09-10|
|AI Data Kit|9.0.4|2026-09-10|
|AI Desktop Actions|6.0.0|2026-09-10|
|AI Desktop Actions Core|6.0.0|2026-09-10|
|AI Discovery|2.9.7|2026-09-10|
|AI Enhanced Recommended Actions|1.0.5|2026-08-07|
|AI Experience Framework|1.0.12|2026-08-07|
|AI Experience Framework Components|1.4.0|2026-09-10|
|AI Experience Framework Components for Setup Hub|1.4.0|2026-09-10|
|AI Experience Framework Components for Setup Hub|1.4.0|2026-09-10|
|AI Experience Framework Skills|1.4.4|2026-09-10|
|AI features for Deal Registration|1.0.2|2026-09-10|
|AI for document designer|23.0.3|2026-09-10|
|AI Help Framework|2.0.2|2026-09-10|
|AI Insight Engine|4.0.2|2026-09-10|
|AI Metric Engine|2.1.4|2026-09-10|
|AI Native Experience for AI Control Tower - ServicenowAI|4.0.1|2026-09-10|
|AIOps Agentic Workforce|2.2.5|2026-09-10|
|AIOps Dashboards|26.2.0|2025-12-11|
|AIOps Experience|27.0.0|2026-03-12|
|AI Platform skills|3.2.2|2026-09-10|
|AI Policy Framework|1.0.4|2026-09-10|
|AI Readiness Evaluation|1.5.2|2026-09-10|
|AI Risk and Asset Management for ServiceNow AI|1.5.3|2026-09-10|
|AI Risk and Compliance Content|21.1.1|2025-12-11|
|AI Risk and Compliance Integration with Control Tower|23.0.2|2026-09-10|
|AI Risk and Compliance Management|23.0.3|2026-09-10|
|AI sales activity association|1.2.1|2026-09-10|
|AI Search Admin Console|9.2.2|2026-08-07|
|AI Search for Customer Portals|1.1.0|2025-12-11|
|AI Search For Next Experience|5.0.2|2026-02-05|
|AI Search RAG|7.0.3|2026-09-10|
|AI Search Spoke|2.0.3|2023-09-20|
|AI Security and Privacy|6.1.3|2026-09-10|
|AI Service Graph Connector for Amazon|2.1.9|2026-09-10|
|AI Service Graph Connector for Google|1.3.3|2026-09-10|
|AI Service Graph Connector for LangGraph|1.1.7|2026-09-10|
|AI Service Graph Connector for Microsoft|3.1.19|2026-09-10|
|AI SGC Discovery|2.0.4|2026-09-10|
|AI Skill Kit|10.0.5|2026-09-10|
|AI slot-filling for catalog items|1.4.5|2026-08-07|
|AI Specialists for Security Incident Response|1.0.10|2026-09-10|
|AIS ZTSD Gemma|1.0.6|2026-09-10|
|AI Trace Collector|3.1.3|2026-09-10|
|AI Troubleshooting|4.1.4|2026-08-07|
|AI Websearch|4.1.0|2026-06-16|
|Aleph Alpha Spoke|1.0.2|2025-01-30|
|Alert Assist|3.12.2|2026-09-10|
|Alert Rules Management|18.15.9|2026-06-16|
|Amazon Alexa Spoke|1.1.0|2024-11-07|
|Amazon Bedrock Spoke|1.5.1|2026-08-07|
|Amazon CloudWatch Spoke|1.0.2|2022-12-01|
|Amazon Connect Spoke|1.2.0|2025-03-12|
|Amazon DynamoDB Spoke|1.0.1|2022-09-01|
|Amazon EBS Spoke|1.0.2|2023-09-20|
|Amazon EC2 Spoke|1.4.0|2025-09-10|
|Amazon Elastic Container Service Spoke|1.0.2|2023-09-07|
|Amazon RDS Spoke|1.0.5|2025-06-05|
|Amazon Route 53 Spoke|1.0.2|2022-12-01|
|Amazon S3 Spoke|1.2.1|2024-09-10|
|Amazon SNS Spoke|1.1.0|2023-09-07|
|Amazon SQS Spoke|1.0.1|2025-01-02|
|Amazon VPC Spoke|1.0.3|2023-09-07|
|Analytics Generation|4.1.15|2026-07-09|
|Analytics Pack for Contract Management Pro|1.2.0|2025-05-01|
|Analytics Toolkit|8.4.3|2026-07-09|
|Analytics Toolkit|8.4.3|2026-07-09|
|Ansible Spoke|2.2.9|2024-12-05|
|API Insights|2.2.1|2025-12-11|
|API Notification Management|4.0.1|2025-12-11|
|API Service Graph Connector for Apigee X|2.2.2|2025-10-16|
|API Service Graph Connector for AWS API Gateway|2.2.0|2025-09-10|
|API Service Graph Connector for Azure API Management|2.2.0|2025-07-31|
|API Service Graph Connector for Kong Gateway|2.1.0|2025-10-16|
|API Service Graph Connector for Kong Konnect|1.0.0|2025-10-16|
|APO - Foundation|2.0.0|2026-09-10|
|APO - Prime|2.0.0|2026-09-10|
|app-ai-metric-ui|2.1.4|2026-09-10|
|App AutoUpgrade Client|1.0.0|2026-07-09|
|App Best Practices Shared|29.2.0|2026-06-16|
|App Collaboration Component|28.2.1|2025-12-11|
|App Engine Management Center|29.2.1|2026-06-16|
|App Engine Notifications|29.2.6|2026-08-07|
|App Engine - Prime|29.1.8|2026-08-07|
|App Engine Studio|28.2.1|2025-12-11|
|app-ent-data-map-components|1.0.0|2026-09-10|
|App Generation|28.3.12|2026-07-09|
|Applicant Center|8.0.2|2026-07-09|
|Application Common Configuration|29.0.8|2026-03-12|
|Application Insights|2.0.3|2021-11-18|
|Application Intake|29.2.1|2026-06-16|
|Application Portfolio Management integration with Policy and Compliance|1.0.3|2023-05-04|
|Application Portfolio Management integration with Risk Management|1.0.2|2023-05-04|
|Application Service Extensions|1.1.7|2024-11-07|
|Application spoke selector|1.6.0|2026-08-07|
|App Life Cycle AI Agents|29.5.2|2026-08-07|
|Appointment calendar component|28.1.1|2025-12-11|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|App Shell Utils|29.0.0|2026-03-12|
|App Studio Commons|30.1.0|2026-09-10|
|App Summary|29.4.0|2026-07-09|
|ArcSight ESM Event Ingestion for Security Operations|10.5.0|2025-12-11|
|ArcSight Logger Integration for Security Operations|10.4.1|2024-11-07|
|Aria Systems Spoke|2.1.2|2023-04-06|
|Asana Spoke|1.0.3|2024-08-01|
|Asset Audit Response|2.0.3|2026-07-09|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Asset Audits|1.0.0|2026-03-12|
|Asset Management Common|16.0.0|2026-09-10|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management - Procurement Integration|1.0.1|2024-11-07|
|Asset Security Posture Management|5.5.1|2025-12-11|
|Asset Shipments|1.0.0|2026-03-12|
|Assist Order Management AI Agent|1.1.2|2026-09-10|
|ATF Test Generator and Cloud Runner|3.2.1|2026-08-27|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Atlassian Administration Spoke|1.0.1|2025-01-30|
|Atlassian Jira Integration for Agile Development|2.3.2|2025-12-23|
|Atlassian Jira Integrations Common|2.4.2|2025-12-23|
|Attribute Pack|5.0.0|2025-07-31|
|Attribute Pack|5.0.0|2025-07-31|
|Attribute Pack|5.0.0|2025-07-31|
|Attribute propagation|9.4.3|2026-09-10|
|Attribute propagation|9.4.3|2026-09-10|
|Audio player component|27.3.1|2026-03-12|
|Authentication for conversational channels|1.1.0|2026-03-12|
|Automation Anywhere Spoke|1.2.1|2025-05-01|
|Automation Center|15.1.1|2026-08-07|
|AWH for AI Control Tower|3.4.0|2026-09-10|
|AWS Certificate Manager Spoke|1.0.1|2022-09-21|
|AWS CloudFormation Spoke|1.1.4|2024-03-20|
|AWS Elastic Beanstalk Spoke|1.0.3|2024-06-06|
|AWS Elastic Load Balancing Spoke|1.0.1|2022-09-01|
|AWS IAM Spoke|1.1.0|2023-07-06|
|AWS Lambda Spoke|1.1.3|2023-09-07|
|AWS OpsWorks Spoke|1.0.2|2023-09-20|
|AWS Translate Spoke|1.0.0|2022-11-03|
|Azure Active Directory User Mapping|1.11.0|2025-12-11|
|Basic Scoring for Smart Assessments|23.0.3|2026-09-10|
|BCM mobile app|9.1.3|2025-12-11|
|Beans.ai Spoke|29.0.7|2026-03-12|
|BigFix Inventory Spoke|1.5.4|2023-09-07|
|Blue Prism Spoke|1.0.2|2022-09-21|
|BMC Remedy Spoke|1.4.1|2024-10-03|
|Bot Interconnect|1.7.0|2025-07-31|
|Box Spoke|3.7.1|2026-06-26|
|Breadcrumb navigation demo|27.0.0|2025-06-05|
|Breakdown Data Grid UI Component|1.4.0|2023-05-04|
|Broadcom Rally Integration with DevOps|7.0.0|2026-06-16|
|Browser Extension for Employee Center|1.1.1|2025-12-11|
|Bubble trend|1.0.0|2025-05-01|
|Build Agent \(Trial\)|2.6.4|2026-09-10|
|Build Agent Glide Tools|1.0.10|2026-03-12|
|Build Agent Premium|1.6.0|2026-09-10|
|Business Continuity Management Advanced|2.0.3|2026-09-10|
|Business Continuity Management Foundation|2.0.3|2026-09-10|
|Business domain|23.0.2|2026-09-10|
|Business Location|5.6.1|2026-08-07|
|Business Object Core|2.1.0|2025-12-11|
|Business Object Core|2.1.0|2025-12-11|
|Business Portal|2.4.0|2026-06-16|
|Calendar component|27.0.1|2026-06-16|
|Calendly Spoke|1.2.0|2023-08-03|
|Capacity Management|4.1.0|2025-12-11|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Career Assessment|3.3.0|2026-06-16|
|Career Conversations|3.11.2|2026-08-07|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Operations AI agent collection|2.1.1|2026-09-10|
|Care Team Portal|2.2.0|2026-03-12|
|Care Team Portal|2.2.0|2026-03-12|
|Care Team Portal|2.2.0|2026-03-12|
|Carousel component|28.0.1|2026-03-12|
|Case Digests|2.0.0|2026-03-12|
|Case lines and workflows|4.6.1|2026-09-10|
|Case Management for Invoice Operations|2.1.0|2026-09-10|
|Case Management for Invoice Operations|2.1.0|2026-09-10|
|Case Playbook for Complaints|9.1.1|2026-07-09|
|Case Playbook for Onboarding|8.1.0|2025-12-11|
|Case Playbook for Product Support|6.0.1|2025-07-31|
|Catalog Conversational Coverage|6.2.1|2026-09-10|
|CCG Content Pack|1.3.12|2024-11-07|
|CCO Dashboard|2.0.8|2025-12-11|
|CDM File Uploader|1.0.1|2023-11-02|
|CDO Dashboard|2.0.5|2025-12-11|
|Certificate Inventory and Management|4.3.0|2026-08-07|
|CFO Dashboard|2.0.1|2025-12-11|
|Change Management AI Orchestrator|1.0.4|2026-09-10|
|Change Management for Field Service|1.1.2|2025-01-02|
|Change Management for Service Operations Workspace|9.4.2|2026-09-10|
|Change Password Custom Component|1.3.0|2025-12-11|
|Channel Management|7.0.0|2025-12-11|
|Chat integration with Security Incident Management|1.2.10|2025-07-31|
|Chat Recommendation|1.9.1|2026-09-10|
|Chat Summarization for Virtual Agent|1.12.7|2026-09-10|
|Chat Zoom Connector|1.0.6|2023-01-12|
|Checklist component|26.0.0|2025-12-11|
|Check Point Integration for Security Operations|10.4.10|2025-07-31|
|CHRO Dashboard|2.0.4|2025-12-11|
|CIO Dashboard|2.1.1|2025-12-11|
|Cisco Webex Meetings Spoke|2.3.3|2024-08-01|
|Cisco Webex Teams Spoke|2.3.6|2025-12-11|
|CISO Dashboard|2.0.5|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Client Software Distribution 2.0|1.4.0|2025-12-11|
|CLI Metadata|1.1.2|2021-04-15|
|Cloud Access Interface|1.1.3|2026-06-23|
|Cloud Action Library|1.4.0|2024-11-07|
|Cloud Configuration Governance|1.6.0|2025-12-11|
|Cloud Cost Management|11.0.0|2026-09-10|
|Cloud Cost Management Advanced|1.0.0|2026-09-10|
|Cloud Cost Management AWS|11.0.0|2026-09-10|
|Cloud Cost Management Azure|11.0.0|2026-09-10|
|Cloud Cost Management Core|11.0.0|2026-09-10|
|Cloud Cost Management GCP|11.0.0|2026-09-10|
|Cloud Cost Management Infra Stack|11.0.0|2026-09-10|
|Cloud Deployment Automation|1.0.3|2024-12-05|
|Cloud Discovery Workspace|1.7.1|2025-05-01|
|Cloud Flow Wizards|1.2.1|2022-08-24|
|Cloudify Spoke|2.1.1|2023-04-06|
|Cloud Insights Billing|6.0.1|2024-04-04|
|Cloud Insights Billing|6.0.1|2024-04-04|
|Cloud Integrations AWS|11.0.0|2026-09-10|
|Cloud Integrations Azure|11.0.0|2026-09-10|
|Cloud Integrations Core|11.0.0|2026-09-10|
|Cloud Integrations GCP|11.0.0|2026-09-10|
|Cloud Migration Assessment|1.4.0|2024-11-07|
|Cloud Security Posture Management|2.5.0|2024-02-01|
|Cloud Services Catalog|1.5.1|2025-12-11|
|Cloud Services Catalog Terraform Connector|1.9.1|2025-12-11|
|Cloud Spend Dashboard|1.0.3|2022-06-02|
|Cloud Spend Reports AWS|11.0.0|2026-09-10|
|Cloud Spend Reports Azure|11.0.0|2026-09-10|
|Cloud Spend Reports Core|11.0.0|2026-09-10|
|Cloud Spend Reports GCP|11.0.0|2026-09-10|
|Cloud Storage|6.1.0|2026-03-12|
|Cloud Workspace|2.2.0|2025-12-11|
|CMDB and CSDM Data Foundations Dashboards|4.2.0|2025-12-11|
|CMDB Application for APIs and CLI|1.0.1|2021-07-22|
|CMDB CI Class Models|1.94.3|2026-09-10|
|CMDB MCP Server|2.0.0|2026-09-10|
|CMDB Page Templates|3.2.6|2026-06-16|
|CMDB Workspace|9.6.0|2026-09-10|
|Coaching|9.9.2|2026-09-08|
|Coaching With Learning|5.4.2|2026-03-12|
|Coaching with Learning Migration Utility|1.0.1|2021-09-16|
|Collaboration applications - common|1.1.0|2025-12-11|
|Collaboration Request|28.2.1|2025-12-11|
|Collaboration Services|3.12.2|2025-12-11|
|Collaboration Services for Service Operations Workspace|9.4.3|2026-09-10|
|Collaboration UI Component for Major Security Incident Management Workspace|1.2.1|2024-11-07|
|Collaborative Work Management|11.0.1|2026-09-10|
|Collaborative Work Management - Advanced|2.2.1|2026-09-10|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Common AI Framework|2.0.2|2026-08-07|
|Common Guidances|16.0.2|2026-09-10|
|Common Service Delivery|15.0.0|2026-09-10|
|Common UIB Wrapper Components|1.5.1|2025-12-11|
|Common Vendor Core|5.0.2|2026-09-10|
|Compatibility Management|6.7.0|2026-09-10|
|Compatibility Management|6.7.0|2026-09-10|
|Configurable Workspace for Order Management|16.1.0|2026-09-10|
|Configurable Workspace for Order Management|16.1.0|2026-09-10|
|Configuration Compliance|15.5.3|2025-12-11|
|Configuration Data Management|5.0.2|2024-03-20|
|Configuration Hub|1.0.11|2026-08-07|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Confluence Cloud Spoke|1.2.6|2026-01-20|
|Confluent Kafka REST Proxy Spoke|1.0.0|2021-03-11|
|Contact card component|26.0.0|2025-12-11|
|Contact Center Integration Core|1.4.4|2025-12-11|
|Contact Tracing|1.30.0|2025-07-31|
|Content Engagement for Employee Center Pro|1.4.1|2026-03-12|
|Content Experiences|33.1.0|2026-07-09|
|Content Experiences|33.1.0|2026-07-09|
|Content library portal|4.1.1|2026-07-09|
|Content Pack for CMDB|2.1.1|2026-08-07|
|Content Publishing|37.3.3|2026-08-07|
|Content Understanding|7.1.4|2026-09-10|
|Context Menu Component for Configuration Data Management UI|1.2.1|2023-05-04|
|Context Rule Management|10.8.1|2026-09-10|
|Contract Management for Sales and Order Management|1.1.0|2025-12-11|
|Contract Management Pro|1.6.0|2025-12-11|
|Contract Management Pro for Legal Service Delivery|3.0.2|2025-12-11|
|Contract Management Pro MCP Server|1.0.4|2026-09-10|
|Contract Management Pro - Prime|1.0.21|2026-09-10|
|Contractor Service Center|1.0.7|2025-12-11|
|Contracts and Entitlement Workflows|13.0.0|2025-12-11|
|Contracts Core components|1.4.1|2025-07-31|
|Contract Workspace|1.7.2|2025-12-11|
|Conversational Analytics|9.3.1|2026-09-10|
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
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Appointment Booking Components|2.0.5|2023-09-07|
|Conversational Catalog Requests|8.0.2|2026-09-10|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Integration with Alexa|1.5.5|2024-08-01|
|Conversational Integration with Apple Messages for Business|1.3.0|2026-03-12|
|Conversational Integration with Facebook Messenger|3.0.8|2025-12-11|
|Conversational Integration with Google Business Messages|1.1.1|2024-02-01|
|Conversational Integration with Google Chat|2.0.4|2025-12-11|
|Conversational Integration with LINE|2.0.7|2025-01-30|
|Conversational Integration with Microsoft Teams|10.6.0|2026-08-07|
|Conversational Integration with Slack|6.1.0|2026-09-10|
|Conversational Integration with WhatsApp \(powered by Twilio\)|2.0.11|2025-12-11|
|Conversational Integration with Workplace from Facebook|5.0.1|2025-01-30|
|Conversational Interfaces - Diagnostics|2.2.1|2024-11-07|
|Conversational IVR with Amazon Connect|1.6.3|2025-07-31|
|Conversational SMS Integration with AWS End User Messaging|1.0.2|2025-01-30|
|Conversational SMS Integration with Twilio|4.2.4|2025-12-11|
|Conversational SMS Service Channel|2.0.23|2026-03-12|
|Conversational Studio|12.0.7|2026-09-10|
|Conversational subflows and actions|30.0.4|2026-08-07|
|Conversation Evaluator|3.2.1|2026-09-10|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Conversation Insights|3.1.0|2026-06-16|
|Core Business Suite|3.3.2|2026-08-07|
|Core Business Suite|3.3.2|2026-08-07|
|Core Business Suite Advanced|3.3.2|2026-08-07|
|Core Business Suite Advanced|3.3.2|2026-08-07|
|Core Business Suite Advanced for Finance|3.3.2|2026-08-07|
|Core Business Suite Advanced for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Advanced for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Advanced for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Advanced for Legal|3.3.2|2026-08-07|
|Core Business Suite Advanced for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Advanced for Workplace Services|3.3.3|2026-08-07|
|Core Business Suite Analytics|3.3.1|2026-08-07|
|Core Business Suite Analytics|3.3.1|2026-08-07|
|Core Business Suite for Finance|3.3.2|2026-08-07|
|Core Business Suite for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite for Human Resources|3.3.2|2026-08-07|
|Core Business Suite for Legal|3.3.2|2026-08-07|
|Core Business Suite For Source To Pay|3.3.2|2026-08-07|
|Core Business Suite For Workplace Service Delivery|3.3.3|2026-08-07|
|Core Business Suite Foundation|3.3.2|2026-08-07|
|Core Business Suite Foundation|3.3.2|2026-08-07|
|Core Business Suite Foundation for Finance|3.3.2|2026-08-07|
|Core Business Suite Foundation for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Foundation for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Foundation for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Foundation for Legal|3.3.2|2026-08-07|
|Core Business Suite Foundation for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Foundation for Workplace Services|3.3.3|2026-08-07|
|Core Business Suite Prime|3.3.2|2026-08-07|
|Core Business Suite Prime|3.3.2|2026-08-07|
|Core Business Suite Prime for Finance|3.3.2|2026-08-07|
|Core Business Suite Prime for Health and Safety|3.3.3|2026-09-10|
|Core Business Suite Prime for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Prime for Legal|3.3.2|2026-08-07|
|Core Business Suite Prime for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Prime for Workplace Services|3.3.3|2026-08-07|
|Cornerstone Spoke|1.6.0|2026-07-09|
|Coupa Spoke|4.14.0|2025-10-16|
|COVID-19 Global Health Data Set|1.20.3|2024-05-09|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ Config Agent A2A|1.1.7|2026-09-10|
|CPQ Configurator|1.4.0|2026-06-16|
|CPQ for Manufacturing Advanced|3.0.0|2026-09-10|
|CPQ for Manufacturing Foundation|3.0.0|2026-09-10|
|CPQ - Foundation|1.0.1|2026-04-09|
|CPQ Integration|3.3.0|2026-07-09|
|CPRO Dashboard|2.0.5|2025-12-11|
|Craft.co Integration for Supplier Lifecycle Operations|9.0.0|2026-09-10|
|Craft Spoke|1.0.0|2024-11-07|
|Creator Studio|28.2.1|2025-12-11|
|Creator Studio Configurations|28.2.1|2025-12-11|
|Creator Studio Configurations|28.2.1|2025-12-11|
|Credentials Core|1.2.0|2026-06-16|
|Credly Spoke|1.1.0|2026-06-16|
|Critical Event Management|1.2.5|2026-07-09|
|CRM API Core|7.4.1|2026-09-10|
|CRM Core|1.10.1|2026-09-10|
|CRM Flow Wizards|1.0.1|2023-04-06|
|CRM Outlook Add-in|1.2.1|2026-09-10|
|CRM Territory Extensions|2.0.3|2026-03-12|
|CRM Touchpoint|1.6.1|2026-09-10|
|CRO Dashboard|2.0.10|2025-12-11|
|CrowdStrike Falcon EDR Integration for Threat Intelligence Security Center|3.0.0|2024-11-07|
|CrowdStrike Falcon Host for Security Operations|10.4.5|2024-11-07|
|CrowdStrike Falcon Insight Integration for Security Operations|1.4.1|2026-01-20|
|CrowdStrike Falcon Sandbox Integration for Security Operations|11.0.10|2024-09-10|
|CrowdStrike Spoke|1.1.0|2025-01-30|
|Cryptographic Asset Compliance|1.0.2|2026-08-07|
|CSC Content Pack|1.7.0|2025-12-11|
|CSM Account Hierarchy|30.0.3|2026-03-12|
|CSM Account Hierarchy|30.0.3|2026-03-12|
|CSM - Advanced|2.1.2|2026-08-07|
|CSM Contributor User|2.4.0|2026-06-16|
|CSM Data Classification|1.0.0|2025-07-31|
|CSM Extension for Proxy Contacts|2.0.0|2026-03-12|
|CSM - Foundation|2.1.2|2026-08-07|
|CSM MCP Server|1.2.0|2026-08-07|
|CSM - Prime|2.1.2|2026-08-07|
|CTO Voice AI Agents|2.1.0|2026-09-10|
|Custom App Record Summarization|30.1.1|2026-09-10|
|Customer Contracts and Entitlements|15.0.1|2026-09-10|
|Customer Data Models for B2B2C|2.1.0|2025-07-31|
|Customer Discovery Hub|1.2.2|2026-07-09|
|Customer Engagement Sequences|2.0.1|2025-12-11|
|Customer Household Data Model|2.0.11|2026-09-10|
|Customer Install Base Characteristics|2.5.4|2026-09-10|
|Customer Install Base Management|4.10.3|2026-09-10|
|Customer Life Cycle Management Self Service|2.1.1|2025-12-11|
|Customer Life Cycle Management Workflows|5.1.1|2025-12-11|
|Customer Project Management|2.0.0|2026-03-12|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Service Case Action Status|2.0.2|2026-06-16|
|Customer Service Case Types|4.4.2|2026-07-20|
|Customer Service Document Template|2.0.0|2026-03-12|
|Customer Service integration with Social Media Store|1.0.2|2026-03-12|
|Customer Service Management AI agent collection|7.0.1|2026-09-10|
|Customer Service NLU Model for Virtual Agent Conversations|1.0.5|2026-03-12|
|Customer Service Portal|25.3.3|2026-06-16|
|Customer Service Problem Management|5.0.2|2025-12-11|
|Customer Service RMA AI Agents|1.1.4|2026-09-10|
|Customer Service Virtual Agent Conversations|1.0.5|2026-04-09|
|Customer Service with Request Management|2.1.0|2026-04-09|
|Customer Service with Service Management|2.0.1|2026-03-12|
|Customer Service with Service Portfolio Management \(SPM\)|2.0.1|2025-01-30|
|Customer Success Advanced|2.4.10|2026-07-09|
|Customer Success Management|6.6.3|2026-07-09|
|Cyber Physical Systems Control Tower Advanced|1.0.2|2026-09-10|
|Cyber Physical Systems Control Tower Foundation|1.0.2|2026-09-10|
|Cyber Physical Systems Control Tower Prime|1.0.2|2026-09-10|
|Cyber Physical Systems Operations Advanced|1.0.5|2026-09-10|
|Cyber Physical Systems Operations Foundation|1.0.5|2026-09-10|
|Cyber Physical Systems Operations Prime|1.0.5|2026-09-10|
|Cyber Physical Systems Security Advanced|1.0.5|2026-09-10|
|Cyber Physical Systems Security Foundation|1.0.5|2026-09-10|
|Cyber Physical Systems Security Prime|1.0.7|2026-09-10|
|Cybersecurity Executive Dashboard|2.4.3|2025-05-01|
|Dashboard and visualization export|1.4.1|2026-09-10|
|Data Collection for Oracle Global Licensing and Advisory Services|1.11.0|2025-12-11|
|Data Context Engine|3.3.2|2026-06-16|
|Data Context Engine|3.3.2|2026-06-16|
|Data Discovery|8.1.3|2026-08-07|
|Data Foundation Model|1.13.2|2026-09-10|
|Data Grid UI Component|26.0.13|2026-09-10|
|Data Loss Prevention Incident Response|2.2.2|2026-02-05|
|Data Model for Order Management|17.1.0|2026-09-10|
|Data Model for SBOM|4.2.1|2025-12-11|
|Data Model Navigator|1.1.3|2026-09-10|
|Data Privacy|8.1.4|2026-08-07|
|Data registry|23.0.1|2026-09-10|
|Data Relationships Framework|12.0.2|2026-09-10|
|DCNAM - Advanced|2.3.0|2026-09-10|
|DCNAM - Advanced|2.3.0|2026-09-10|
|Decision Builder|29.1.4|2026-04-09|
|Decision Table Builder|29.1.6|2026-04-09|
|Deployment Pipeline|29.2.6|2026-08-07|
|DevOps Change Health Scan Content Pack|6.2.0|2025-12-11|
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
|DEX Application and Device Health|5.2.3|2026-09-10|
|DEX Content Playbook|5.2.2|2026-09-10|
|DEX Desktop Assistant|5.1.1|2026-08-07|
|DEX Desktop Assistant|5.1.1|2026-08-07|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Zoom|5.0.0|2026-07-09|
|DEX for Zoom|5.0.0|2026-07-09|
|DEX for Zoom|5.0.0|2026-07-09|
|DEX for Zoom|5.0.0|2026-07-09|
|DEX Self Service|5.1.1|2026-08-07|
|DEX Self Service|5.1.1|2026-08-07|
|Diagram Builder|30.0.0|2026-05-05|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Digital Experience Score|5.1.1|2026-08-07|
|Digital Experience Score|5.1.1|2026-08-07|
|Digital Integration Management|1.6.4|2026-08-07|
|Digital Portfolio Management|7.4.1|2026-01-20|
|Digital Product Release|2.3.2|2025-12-11|
|Digital Product Release Data Model|2.4.0|2026-03-12|
|Digital Product Release Policy Content Pack|2.2.0|2025-07-31|
|Digital Product Release Workspace|2.3.0|2025-12-11|
|Digital Resilience Third-party Information Register|21.1.7|2025-12-11|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital signature component|27.1.0|2025-07-31|
|Discovery Admin Workspace|1.17.0|2026-06-16|
|Discovery and Service Mapping Patterns|1.32.0|2026-08-07|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|DLP Incident Response integration with ICAP|1.1.1|2026-01-20|
|DLP Incident Response integration with Microsoft|1.3.1|2026-01-20|
|DLP Incident Response integration with Netskope|1.2.1|2026-01-20|
|DLP Incident Response integration with Proofpoint|1.1.0|2025-12-11|
|DLP Incident Response integration with Symantec|1.3.1|2026-01-20|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Docker Spoke|2.3.4|2025-07-10|
|Document Approval App Template|28.2.1|2025-12-11|
|Document display component|27.0.0|2025-05-01|
|Document Flow Wizards|2.0.2|2022-09-21|
|Document Intelligence|8.0.9|2026-08-07|
|Document Intelligence Admin|4.1.0|2025-12-11|
|Document Intelligence for Accounts Payable Operations Content Pack|2.0.0|2025-12-11|
|Document Intelligence for Contract Management Content Pack|1.5.0|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Service Framework for Google Drive|3.0.0|2025-07-31|
|Document Service Framework for OneDrive|3.0.0|2025-07-31|
|Document Template Integration with AdobeSign|1.7.0|2025-12-11|
|Document Template integration with DocuSign|1.7.1|2026-03-12|
|Document Templates|29.0.1|2026-07-09|
|DocuSign Activities for PAD|1.1.3|2023-01-12|
|Docusign eSignature Spoke|4.2.2|2026-02-05|
|Dropbox Business Spoke|1.0.5|2024-03-07|
|Dun and Bradstreet DirectPlus Spoke|1.0.0|2025-01-30|
|Dynamic Guidance|28.5.1|2026-09-10|
|Dynamic Related Records for Configurable Workspace|25.7.0|2026-06-16|
|Elasticsearch Integration for Security Operations|10.3.4|2024-11-07|
|Email Interaction Core|1.0.3|2025-12-11|
|Email Interaction for CSM|1.5.0|2025-12-11|
|Emergency Alert App Template|28.2.1|2025-12-11|
|Emergency Exposure Management|1.27.0|2025-07-31|
|Emergency Outreach|1.34.0|2025-07-31|
|Emergency Self Report|1.21.0|2025-07-31|
|Employee Center|44.3.1|2026-09-10|
|Employee Center for Microsoft Viva Connections|2.0.8|2025-07-31|
|Employee Center integration with Zoom|2.0.16|2025-12-11|
|Employee Center Pro|42.0.4|2026-07-09|
|Employee Center Pro Kiosk|2.3.4|2025-12-11|
|Employee Experience Foundation|30.0.3|2025-12-11|
|Employee experience taxonomy|28.2.5|2025-12-11|
|Employee Experience VA Components|1.0.0|2023-08-03|
|Employee Experience VA topics and topic blocks|1.1.2|2023-05-04|
|Employee Goals|1.4.3|2026-08-07|
|Employee Health Screening|1.28.0|2025-07-31|
|Employee Profile|14.2.1|2026-09-10|
|Employee Readiness Core|1.42.0|2025-12-11|
|Employee Readiness Surveys|1.5.3|2025-07-31|
|Employee Slate \(built for Now Assist\)|1.4.4|2026-09-10|
|Employee Travel Safety|1.22.0|2025-12-11|
|Engagement dashboard for AI Control Tower|3.0.11|2025-12-12|
|Engagement Messenger|5.12.1|2026-01-20|
|Enhanced Features for IRM Enterprise|23.0.1|2026-09-10|
|Enhanced Features for IRM Professional|23.0.2|2026-09-10|
|Enterprise Architecture - Advanced|1.0.1|2026-06-16|
|Enterprise Architecture Cloud Assessment|1.0.1|2025-01-30|
|Enterprise Architecture - Prime|1.0.1|2026-06-16|
|Enterprise Architecture Workspace|9.2.1|2026-08-07|
|Enterprise Asset Management Advanced|2.0.0|2026-09-10|
|Enterprise Asset Management for DCNAM|2.0.0|2026-09-10|
|Enterprise Asset Management for DCNAM Advanced|2.0.0|2026-09-10|
|Enterprise Asset Management for Facilities|1.0.0|2024-08-01|
|Enterprise Asset Management for Healthcare|2.0.0|2026-09-10|
|Enterprise Asset Management for Healthcare Advanced|2.0.1|2026-09-10|
|Enterprise Asset Management for Providers|1.0.0|2025-12-11|
|Enterprise Data Transform|1.0.2|2026-09-10|
|Enterprise Modeling and Visualization|6.2.2|2026-06-16|
|Enterprise Modeling Common|3.8.0|2026-06-16|
|Enterprise Portfolio|1.3.0|2025-12-11|
|Enterprise Service Management Integrations Framework|3.8.2|2025-07-31|
|Entitlements Verification|6.2.1|2026-09-10|
|Equifax Spoke|1.0.0|2023-08-03|
|ER integration with NAVEX|1.1.1|2024-02-01|
|ERP Customization Mining|7.0.5|2025-05-01|
|ERP Integration Framework|19.0.3|2026-06-16|
|ERP Rapid Deployment Packs|33.0.0|2026-08-07|
|ESG integration with DEX|21.1.0|2025-12-11|
|ESG Risk Management|21.0.1|2025-12-11|
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
|Event Inquiry|1.4.0|2025-07-31|
|Event Management Connectors|2.18.2|2026-03-12|
|Event Management Core|23.16.0|2026-06-16|
|Event Registration App Template|28.2.1|2025-12-11|
|Expanded Model and Asset Classes|2.17.1|2026-09-10|
|Expense Pre-Approval Template|28.2.1|2025-12-11|
|Experimentation Framework Core|1.1.14|2026-07-09|
|Export entities|3.4.0|2026-09-10|
|Export to PowerPoint|2.3.0|2025-12-11|
|Export to PowerPoint for Application Portfolio Management|1.0.1|2024-02-01|
|Export to PowerPoint for Strategic Portfolio Management|1.4.2|2025-12-11|
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
|External content connectors - ServiceNow Otto agent|1.2.0|2026-08-07|
|External Content Connectors Sharepoint Online|7.0.7|2026-05-28|
|External Content Connectors Slack|7.0.7|2026-05-28|
|External Content Connectors Smartsheet|7.0.7|2026-05-28|
|External Content Connectors SN Docs|7.0.7|2026-05-28|
|External Content Connectors Trello|7.0.7|2026-05-28|
|External Content Connectors Viva Engage|7.0.7|2026-05-28|
|External Content Connectors Wordpress|7.0.7|2026-05-28|
|External Content Connectors Workday|7.0.7|2026-05-28|
|External Content Connectors Workvivo|7.0.7|2026-05-28|
|External Content Connectors Zendesk|7.0.7|2026-05-28|
|External Content Connectors Zoom|7.0.7|2026-05-28|
|External Credential Storage and Management Application|1.3.1|2025-12-11|
|External Legal Service Center|1.2.0|2025-12-11|
|External Trigger Builder|1.1.0|2026-03-12|
|F5 BIG-IP Spoke|1.3.0|2025-09-10|
|Fallout management|8.0.0|2026-09-10|
|Fallout management|8.0.0|2026-09-10|
|FDIH Dashboard|25.0.5|2024-11-07|
|Field Service Advanced Capacity and Reservations Management|30.0.3|2026-03-12|
|Field Service Capacity and Reservations Management|30.0.3|2026-03-12|
|Field Service Contractor for mobile|4.8.3|2026-03-12|
|Field Service Contractor Management|30.0.2|2026-03-12|
|Field Service Management AI agent collection|4.1.0|2026-09-10|
|Field Service Management for Telecommunications|3.0.2|2025-12-11|
|Field Service Management Intelligent Task Recommendations|29.0.6|2026-03-12|
|Field Service Management Scheduling Automations|29.0.6|2026-03-12|
|Field Service Management Virtual Conferencing Integration|30.0.0|2026-03-12|
|Field Service Manager Mobile|1.1.0|2026-04-09|
|Field Service Manager Workforce|1.1.0|2026-04-09|
|Field Service Marketplace|30.0.1|2026-03-12|
|Field Service Mobile|29.2.3|2026-08-07|
|Field Service NLU Model for Virtual Agent Conversations|1.3.0|2025-07-31|
|Field Service Quality Management|29.1.1|2026-03-12|
|Field Service Territory Planning|30.0.3|2026-03-12|
|Field Service Virtual Agent Conversations|1.7.0|2025-07-31|
|Field Service with Service Locations support|30.0.3|2026-03-12|
|File Explorer Component for Security Operations|1.2.13|2025-08-22|
|File Explorer for Security Incident Response|1.3.0|2025-12-11|
|Finance and Procurement - Foundation|2.0.0|2026-09-10|
|Finance and Procurement - Prime|2.0.0|2026-09-10|
|Finance Case Management|1.5.1|2026-06-16|
|Finance Common Architecture|15.0.0|2026-09-10|
|Finance Operations Workspace|1.5.1|2026-06-16|
|Financials Core|6.2.9|2026-09-10|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|Financial Services Credit Operations|3.7.0|2026-03-12|
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
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Financial Services Operations AI agent collection|4.3.1|2026-08-07|
|Financial Services Operations AI agent collection|4.3.1|2026-08-07|
|Financial Services Operations AI agent collection|4.3.1|2026-08-07|
|Financial Services Operations Core|12.4.2|2026-08-07|
|Financial Services Operations Core|12.4.2|2026-08-07|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
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
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Firewall Audits and Reporting|1.8.0|2025-12-11|
|First Advantage Spoke|1.8.0|2025-11-06|
|Flow Designer - Designer|29.5.2|2026-08-07|
|Flow Designer GenAI|30.1.4|2026-09-10|
|Flow Diagramming|29.1.1|2026-08-07|
|Flow Execution Analysis|29.2.8|2026-06-16|
|Flow Generation|29.4.4|2026-08-07|
|Flow Summarization|29.4.4|2026-08-07|
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
|Flow troubleshooting agent|1.0.12|2026-09-10|
|Forecast planning analysis|21.1.0|2025-12-11|
|Form data collector|2.3.1|2026-08-07|
|Form data collector|2.3.1|2026-08-07|
|Form data collector|2.3.1|2026-08-07|
|Formula Builder|29.1.1|2026-03-12|
|Formula builder connected|23.0.2|2026-09-10|
|Fortify Application Vulnerability Integration|2.7.1|2025-09-10|
|Foundation Data Sync|2.2.25|2026-08-07|
|Foundation Data Sync for Consumers|2.2.25|2026-08-07|
|Foundation Data Sync for Providers|2.2.25|2026-08-07|
|FRISS Spoke|1.1.1|2026-03-12|
|FSM - Advanced|2.1.2|2026-09-10|
|FSM - Foundation|2.1.2|2026-09-10|
|FSM Scheduling AI Agent Collection|2.0.4|2026-09-10|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Gantt UI Builder Component|26.1.4|2026-09-10|
|GC Dashboard|2.0.5|2025-12-11|
|Generative AI Controller|15.0.3|2026-09-10|
|Geo Map component|1.2.0|2025-07-31|
|Gifts and Entertainment Compliance|1.3.0|2025-12-11|
|Github Application Vulnerability Integration|2.3.1|2025-12-11|
|GitHub Spoke|3.5.1|2026-01-20|
|GitLab Spoke|2.4.0|2025-11-06|
|Gmail Spoke|1.3.3|2025-12-11|
|Goal Framework|4.12.1|2026-04-09|
|Goal Framework for SPM|2.10.0|2026-09-10|
|Google Calendar Spoke|2.6.0|2025-09-10|
|Google Chat Spoke|1.2.0|2025-09-10|
|Google Cloud Datastore Spoke|1.0.3|2023-09-07|
|Google Cloud DNS Spoke|1.0.2|2022-09-01|
|Google Cloud Functions Spoke|1.0.3|2025-06-05|
|Google Cloud Load Balancer Spoke|1.0.2|2023-09-07|
|Google Cloud Pub Sub Spoke|1.0.4|2024-09-10|
|Google Cloud SQL Spoke|1.0.2|2023-09-07|
|Google Cloud Storage Spoke|1.1.1|2025-12-11|
|Google Cloud Translator Service Spoke|3.2.6|2025-05-01|
|Google Cloud Virtual Network Spoke|1.0.5|2023-09-07|
|Google Cloud VPC Access Spoke|1.0.1|2022-09-01|
|Google Compute Engine Spoke|1.0.5|2024-09-10|
|Google Directory Spoke|1.5.2|2024-10-03|
|Google Docs Spoke|1.3.0|2025-09-10|
|Google Drive Spoke|2.3.0|2025-09-10|
|Google Gemini Spoke|1.6.2|2026-08-07|
|Google Identity And Access Spoke|1.1.1|2022-09-01|
|Google Meet Spoke|1.2.1|2025-11-06|
|Google Persistent Disk Spoke|1.0.2|2022-09-01|
|Google Sheets Spoke|1.0.7|2023-09-20|
|Google Tasks Spoke|1.4.0|2025-09-10|
|GoTo Spoke|2.0.1|2021-08-19|
|GovNotify Spoke|1.2.0|2025-09-10|
|GRC: Advanced Core|22.0.1|2026-03-12|
|GRC: Advanced Dashboards|21.1.1|2025-12-11|
|GRC: Advanced Risk|23.0.6|2026-09-10|
|GRC: Advanced Risk Assessment|23.0.3|2026-09-10|
|GRC: Approver Configurator|23.0.5|2026-09-10|
|GRC: Audit Management|22.0.1|2026-03-12|
|GRC: Audit Management Workspace|22.0.1|2026-03-12|
|GRC: Business Continuity Management - Core|12.0.3|2026-09-10|
|GRC: Business Continuity Management User - Lite|5.0.1|2023-08-03|
|GRC: Business Continuity Planning|12.0.7|2026-09-10|
|GRC: Business Impact Analysis|12.0.5|2026-09-10|
|GRC: Business User - Lite|18.0.0|2024-02-01|
|GRC: Common Dashboard Elements|18.1.4|2024-06-06|
|GRC: Common Workspace Elements|23.0.9|2026-09-10|
|GRC: Compliance Assessment|23.0.2|2026-09-10|
|GRC: Compliance Case Management|21.1.0|2025-12-11|
|GRC: Compliance Management Workspace|21.1.3|2025-12-11|
|GRC: Compliance UCF|21.1.0|2025-12-11|
|GRC: Composite Entity|21.1.1|2025-12-11|
|GRC: Continuous Authorization and Monitoring|21.1.1|2025-12-11|
|GRC: Continuous Authorization and Monitoring Advanced|21.1.1|2025-12-11|
|GRC: Continuous Authorization and Monitoring Workspace|21.1.1|2025-12-11|
|GRC: Crisis Management|12.0.5|2026-09-10|
|GRC: Crisis Management integration with Everbridge Notifications|12.0.7|2026-09-10|
|GRC: Crisis Map|12.0.5|2026-09-10|
|GRC: Cyber Risk Institute \(CRI\) Profile Accelerator|21.1.0|2025-12-11|
|GRC: Cybersecurity Controls Accelerator|18.1.0|2024-06-06|
|GRC: Entity Based Access|21.1.4|2025-12-11|
|GRC: Financial Services Controls Accelerator|22.0.1|2026-03-12|
|GRC: integrations with third-party content|18.1.0|2024-06-06|
|GRC: Management Reporting|18.1.0|2024-06-06|
|GRC: Metrics|23.0.5|2026-09-10|
|GRC: Mobile|18.0.0|2024-02-01|
|GRC: NIST CSF Use Case Accelerator|21.1.0|2025-12-11|
|GRC: Performance Analytics Premium Integration|19.1.0|2024-11-07|
|GRC: Policy and Compliance integrator|21.1.0|2025-12-11|
|GRC: Policy and Compliance Management|23.0.2|2026-09-10|
|GRC: Predictive Intelligence|21.1.0|2025-12-11|
|GRC: Privacy Lite User|19.0.0|2024-08-01|
|GRC: Profiles|23.0.7|2026-09-10|
|GRC: Regulatory Change Management integration with RSS Feeds|21.1.0|2025-12-11|
|GRC: Risk Heatmap|22.3.2|2026-06-16|
|GRC: Risk Management|23.0.3|2026-09-10|
|GRC: Risk Management Workspace|21.1.1|2025-12-11|
|GRC: Risk Shared Common Components|23.0.5|2026-09-10|
|GRC: SIG Questionnaire Integration|21.1.0|2025-12-11|
|GRC: SOX Content Pack|21.1.0|2025-12-11|
|GRC: taxonomy management|23.0.2|2026-09-10|
|GRC: Technology Controls Monitoring Accelerator|21.1.0|2025-12-11|
|GRC: Vendor Portal|23.0.5|2026-09-10|
|GRC: Vendor Risk Management Workspace|23.0.5|2026-09-10|
|GRC: Virtual Agent|19.1.0|2024-11-07|
|GRC: Workbench|21.1.0|2025-12-11|
|GRC Case Management Core|23.0.2|2026-09-10|
|GRC Change Management Core|23.0.3|2026-09-10|
|GRC Common GenAI|23.0.5|2026-09-10|
|GRC Compliance Case Management Advanced|18.1.1|2024-06-06|
|GRC Compliance Case Management Full Access|18.1.1|2024-06-06|
|GRC Employee User|19.0.1|2024-08-01|
|GRC Feature roles|23.0.3|2026-09-10|
|GRC integration with Thomson Reuters Regulatory Intelligence|21.1.0|2025-12-11|
|GRC Privacy Case Management Integration with RadarFirst|21.1.0|2025-12-11|
|GRC Shared GenAI|23.0.2|2026-09-10|
|Group-Action Framework|8.0.6|2026-09-10|
|Group Life Servicing|2.5.0|2026-03-12|
|Group Life Servicing|2.5.0|2026-03-12|
|Group Life Servicing|2.5.0|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|Guidance|45.0.2|2026-09-10|
|Guided Decisions|38.0.2|2025-12-11|
|Guided Decisions|38.0.2|2025-12-11|
|Guided Decisions|38.0.2|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Guided Self-Service in Employee Center|3.2.2|2025-12-11|
|Guidewire Spoke|1.3.0|2026-03-12|
|Hardware Asset Management|16.0.1|2026-09-10|
|Hardware Asset Management - Advanced|1.0.11|2026-09-10|
|Hardware Asset Management for DaaS|12.1.1|2026-03-12|
|Hardware Asset Management for TNI|13.0.0|2025-11-06|
|Hardware Asset Management for Zero Touch Mobility|12.0.0|2025-01-30|
|Hardware Asset Management - Prime|1.0.13|2026-09-10|
|HCLS - Advanced|3.2.0|2026-09-10|
|HCLS - Advanced|3.2.0|2026-09-10|
|HCLS - Foundation|3.1.0|2026-09-10|
|HCLS - Foundation|3.1.0|2026-09-10|
|HCLS - Prime|3.1.0|2026-09-10|
|HCLS - Prime|3.1.0|2026-09-10|
|Header App Shell|23.0.0|2023-06-01|
|Health and Safety - Advanced|1.0.6|2026-07-09|
|Health and Safety Case Management|6.3.1|2026-08-07|
|Health and Safety Components|12.1.2|2026-07-09|
|Health and Safety Components|12.1.2|2026-07-09|
|Health and Safety Contractor Management|5.3.1|2026-08-07|
|Health and Safety Core|13.3.1|2026-08-07|
|Health and Safety - Foundation|1.0.6|2026-07-09|
|Health and Safety Incident Management|13.3.1|2026-08-07|
|Health and Safety Incident Management PA Content Pack|10.1.1|2026-07-09|
|Health and Safety Incident Management PA Content Pack|10.1.1|2026-07-09|
|Health and Safety - Prime|1.0.6|2026-07-09|
|Health and Safety Risk Management|9.3.1|2026-08-07|
|Health and Safety Testing|1.27.0|2025-07-31|
|Healthcare and Life Sciences Service Management Core|11.3.0|2026-03-12|
|Healthcare and Life Sciences Service Management Core|11.3.0|2026-03-12|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Operations Core|2.3.0|2026-03-12|
|Healthcare Operations Core|2.3.0|2026-03-12|
|Healthcare Professional Data Model|1.3.0|2025-12-11|
|Health dashboard for AI Control Tower|3.0.11|2025-12-12|
|Health Log Analytics|38.0.17|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Hiring Core|5.4.1|2026-07-09|
|Hiring tab|8.0.1|2026-07-09|
|Homepage deprecation help tool|2.0.2|2024-11-07|
|HR Flow Wizards|1.1.0|2022-05-05|
|HR License meter|1.1.6|2026-06-16|
|HR Multi Instance Integration Base|2.0.0|2025-07-31|
|HR Multi Instance Integration for Consumer|2.0.0|2025-07-31|
|HR Multi Instance Integration for Provider|2.0.0|2025-07-31|
|HRSD - Advanced|2.2.5|2026-09-10|
|HRSD - Foundation|2.2.5|2026-09-10|
|HRSD - Prime|2.2.5|2026-09-10|
|HRSD Process Mining Content Pack|6.0.3|2026-03-12|
|HR Service Delivery Advanced Integration with Oracle HCM|1.3.0|2025-12-11|
|HR Service Delivery Advanced Integration with Workday|2.2.6|2025-12-11|
|HR Service Delivery for Healthcare|1.0.4|2025-05-01|
|HR Service Delivery for Microsoft 365|3.8.0|2025-12-11|
|HR Service Delivery for mobile|21.2.9|2025-12-11|
|HR Service Delivery Integration with Cornerstone OnDemand|1.2.0|2025-12-11|
|HR Service Delivery integration with Oracle HCM|1.0.10|2024-11-07|
|HR Service Delivery Integration with Ultimate Kronos Group|2.0.6|2024-06-06|
|HR Service Delivery Integration with Workday|3.4.11|2025-12-11|
|HR Service Delivery NLU Model for Virtual Agent Conversations|22.2.0|2023-11-02|
|HR Service Delivery Portal UI Components|1.0.5|2024-05-09|
|HR Service Delivery Virtual Agent Conversations|24.2.8|2025-05-01|
|HR Success Dashboard indicators|1.0.15|2025-05-01|
|HR taxonomy|1.2.1|2022-12-01|
|HR Voice AI Agents|2.3.14|2026-09-10|
|Human Resources: Service Portal|44.3.1|2026-09-10|
|Human Resources Service Delivery Integration with Workday Learning|1.4.0|2025-07-31|
|IBM License Compliance for Software Asset Management|6.0.7|2026-03-12|
|IBM QRadar Integration for Security Operations|10.3.7|2024-11-07|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|ICW Core|1.0.4|2026-05-05|
|ICW - Foundation|1.0.3|2026-05-05|
|Idea Manager Dashboard|2.2.0|2025-12-11|
|iManage Spoke|1.1.6|2026-01-20|
|Impact|11.0.3|2026-09-10|
|Impact Common|11.0.2|2026-09-10|
|Impact Content|11.0.1|2026-09-10|
|Impact Health Content|6.0.3|2026-09-10|
|Impact Value Management - APM|2.2.0|2026-09-10|
|Impact Value Management - App Engine|2.2.0|2026-09-10|
|Impact Value Management - CSM|2.2.0|2026-09-10|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HR|4.1.0|2026-09-10|
|Impact Value Management - IRM|3.1.0|2026-09-10|
|Impact Value Management - ITAM|1.0.1|2026-09-10|
|Impact Value Management - ITOM|3.1.0|2026-09-10|
|Impact Value Management - ITSM|5.1.0|2026-09-10|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SECOPS|3.1.0|2026-09-10|
|Impact Value Management - SPM|3.1.0|2026-09-10|
|Incident Communications Management for Service Operations Workspace|9.4.2|2026-09-10|
|Incident Management for Field Service|1.1.1|2025-01-02|
|Incident Management for Service Operations Workspace|9.4.2|2026-09-10|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Servicing|2.5.0|2026-03-12|
|Individual Life Servicing|2.5.0|2026-03-12|
|Individual Life Servicing|2.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Indoor Mapping|1.16.8|2026-06-16|
|Indoor Mapping Component|1.6.1|2026-06-16|
|Indoor Mapping for Assets|1.0.2|2025-10-16|
|Indoor Mapping Service|1.0.8|2025-12-11|
|Industrial Core|4.1.6|2026-09-10|
|Industrial Process Manager|4.2.5|2026-09-10|
|Industrial Workspace Common|4.2.4|2026-09-10|
|Industry Core|1.0.9|2022-12-01|
|Infoblox Spoke|2.0.4|2024-03-20|
|Insights Clustering Utils|3.4.1|2026-09-10|
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
|Insurance claims|1.2.2|2026-03-12|
|Insurance claims|1.2.2|2026-03-12|
|Insurance claims|1.2.2|2026-03-12|
|Insurance Claims Core|3.6.2|2026-08-07|
|Insurance Claims Core|3.6.2|2026-08-07|
|Insurance Claims Core|3.6.2|2026-08-07|
|Insurance Claims Core|3.6.2|2026-08-07|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Integrated Risk Management Advanced|23.0.1|2026-09-10|
|Integrated Risk Management Enterprise|23.0.2|2026-09-10|
|Integrated Risk Management Foundation|23.0.0|2026-09-10|
|Integrated Risk Management Prime|23.0.1|2026-09-10|
|Integrated Risk Management Professional|23.0.2|2026-09-10|
|Integrated Risk Management Standard|23.0.2|2026-09-10|
|Integration Commons for CMDB|2.26.0|2026-09-10|
|IntegrationHub Enterprise Flow Wizards|1.0.0|2021-08-19|
|IntegrationHub ETL|3.3.6|2025-12-11|
|Integration Hub Usage Dashboards|3.0.0|2025-07-31|
|Intelligent Approvals|3.0.10|2026-09-10|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Intelligent Task Recommendations|29.0.7|2026-03-12|
|Intent Discovery|3.3.8|2026-05-05|
|Interaction Management for Service Operations Workspace|9.4.2|2026-09-10|
|Interceptor UI for Service Operations Workspace|9.4.2|2026-09-10|
|Interview management|4.0.2|2026-07-09|
|Inventory Number Management|5.0.0|2025-07-31|
|Inventory Number Management|5.0.0|2025-07-31|
|Inventory Number Management|5.0.0|2025-07-31|
|Inventory Tracker App Template|28.2.1|2025-12-11|
|Investigation Framework|9.4.2|2026-09-10|
|Investment Funding|1.1.1|2024-05-09|
|Invicti Application Vulnerability Integration|1.2.1|2024-11-07|
|Invoice Case Management|13.2.4|2026-09-10|
|Invoice Case Self-Service|1.7.0|2026-09-10|
|Invoice Case Self-Service|1.7.0|2026-09-10|
|Invoice Self-Service|1.5.0|2026-09-10|
|Invoice Self-Service|1.5.0|2026-09-10|
|IRM Compliance GenAI|23.0.3|2026-09-10|
|IRM Risk GenAI|23.0.2|2026-09-10|
|ISA Equipment Model|4.1.1|2026-09-10|
|Issue Auto Resolution for HR|4.0.3|2024-06-06|
|ITAM Common for DaaS|11.2.1|2026-03-12|
|ITAM common hub|1.1.0|2025-12-11|
|ITAM Health Check application|3.0.5|2026-03-12|
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
|ITOM - Advanced|1.1.5|2026-09-10|
|ITOM AI Agents For Service Mapping|1.4.1|2026-08-07|
|ITOM AIOPS Config Center|27.2.3|2026-03-12|
|ITOM Cloud Services Core|4.3.0|2026-08-07|
|ITOM Configuration Console|28.1.1|2026-06-16|
|ITOM Guided Setup - New|27.3.1|2026-06-16|
|ITOM Infra Services Workspace|2.0.3|2026-07-09|
|ITOM Line chart|27.1.1|2026-03-12|
|ITOM Mobile Agent|1.0.0|2025-05-01|
|ITOM - Prime|1.2.2|2026-09-10|
|ITOM Telemetry Ingest|1.0.0|2025-12-11|
|IT Service Management|3.3.1|2026-09-10|
|IT Service Management Advanced|3.3.1|2026-09-10|
|IT Service Management AI agent collection|11.2.2|2026-09-18|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|IT Service Management for Microsoft 365|2.11.1|2025-12-11|
|ITSM Admin Experience|3.3.3|2026-09-10|
|ITSM Admin Experience Components|3.3.1|2026-09-10|
|ITSM - Advanced|2.3.11|2026-09-10|
|ITSM - Advanced|2.3.11|2026-09-10|
|ITSM Advanced Admin Experience|3.3.3|2026-09-10|
|ITSM Autonomous Workforce|1.1.7|2026-09-18|
|ITSM Change Admin Experience|1.3.0|2026-09-10|
|ITSM Common Catalog Content|3.1.0|2026-07-09|
|ITSM Employee Experience|3.3.1|2026-09-10|
|ITSM Enterprise UI Components|3.5.0|2025-12-11|
|ITSM - Foundation|2.3.11|2026-09-10|
|ITSM - Foundation|2.3.11|2026-09-10|
|ITSM Fulfiller Experience|3.3.1|2026-09-10|
|ITSM L1 AI Specialist|1.1.10|2026-09-18|
|ITSM Mobile Agent|10.2.0|2025-12-11|
|ITSM NLU Model for Virtual Agent Conversations|8.2.0|2025-05-01|
|ITSM - Prime|2.3.11|2026-09-10|
|ITSM - Prime|2.3.11|2026-09-10|
|ITSM Process Mining Content Pack|2.0.0|2026-03-12|
|ITSM Virtual Agent Conversations|9.3.5|2026-09-08|
|Jack Henry jXchange Spoke|2.1.0|2025-07-31|
|Jamf Spoke|1.2.1|2025-12-11|
|Jenkins Spoke|2.3.0|2025-09-10|
|Jenkins v2 Spoke|1.2.0|2023-02-02|
|Jira Service Management Spoke|1.2.0|2025-10-16|
|Jira Spoke|6.0.1|2026-04-09|
|Journey Accelerator|6.10.0|2026-06-16|
|Journey designer|7.6.5|2026-08-07|
|Kanban board component|26.0.1|2026-02-05|
|Kanban Components|1.2.0|2026-03-12|
|Keyboard Shortcuts AI Skills|1.0.4|2026-08-07|
|KnowBe4 Integration for SecOps|2.3.3|2024-12-05|
|Knowledge API|29.0.1|2026-03-12|
|Knowledge Capabilities in UI Builder|30.6.3|2026-09-10|
|Knowledge Center|31.26.5|2026-09-10|
|Knowledge Graph|8.3.3|2026-09-10|
|Knowledge Graph Affinity Signals|1.0.1|2026-09-10|
|KPI Composer|4.3.1|2025-12-11|
|KPI Framework|7.0.0|2026-09-10|
|Kubernetes Spoke|1.3.0|2025-09-10|
|Kubernetes Visibility Agent|3.13.0|2025-12-11|
|Leader Hub|1.5.0|2026-03-12|
|Lead Management Application|5.0.0|2025-12-11|
|Lead Management Data Model|5.0.1|2025-12-11|
|Lead-to-Cash Process Management|2.2.2|2025-12-11|
|LEAP|4.3.1|2026-09-10|
|Learning|5.7.0|2026-06-16|
|Learning Core|9.10.0|2026-06-16|
|Legal and Contracts Common Utilities|1.2.2|2026-09-10|
|Legal Conflict of Interest|4.7.0|2025-12-11|
|Legal Content Review|1.3.0|2025-12-11|
|Legal Counsel Center|2.4.0|2026-08-07|
|Legal Mobile|5.6.0|2025-12-11|
|Legal Practice Apps Core|1.0.2|2023-02-02|
|Legal Request Management|10.3.4|2026-09-10|
|Legal Service Delivery - Prime|1.0.17|2026-09-10|
|Legal Simple Compliance|1.1.0|2025-12-11|
|Legal Simple Intellectual Property|1.6.0|2025-12-11|
|Legal Simple Privacy|1.2.5|2025-12-11|
|Legal Stock Preclearance|4.9.0|2025-12-11|
|Legal Tracker Spoke|1.0.4|2025-01-30|
|Legal Virtual Agent Conversations|1.3.2|2023-05-04|
|Licensing Engine|6.5.0|2026-09-10|
|List AI Experience|3.1.4|2026-08-07|
|Live CI View|19.1.2|2023-05-04|
|Localization Workspace|1.0.6|2025-05-01|
|Log Export Service|3.2.0|2025-05-01|
|Looker Spoke|1.0.2|2025-01-30|
|Lucidchart Diagramming Spoke|1.1.1|2024-01-04|
|Lucidchart Integration|2.4.1|2025-01-30|
|Magnit Spoke|1.2.1|2023-09-07|
|Major Incident Management for Service Operations Workspace|9.4.2|2026-09-10|
|Major Issue Management|4.1.7|2026-07-31|
|Major Security Incident Management|3.5.1|2026-01-20|
|Manage Invoice Operations|1.3.0|2026-09-10|
|Manage Order Operations|2.2.0|2026-09-10|
|Manager Hub|4.9.1|2026-06-16|
|Manage Skills Configurable Page|1.1.12|2025-01-30|
|Manufacturing Commercial Operations Advanced|3.0.0|2026-09-10|
|Manufacturing Commercial Operations AI agents collection|4.1.0|2026-09-10|
|Manufacturing Commercial Operations Foundation|3.0.0|2026-09-10|
|Manufacturing Commercial Operations Prime|3.0.0|2026-09-10|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Map Integrations for Field Service|29.0.8|2026-03-12|
|Marketplace Core|30.0.1|2026-03-12|
|Mastercard Spoke|4.0.1|2025-12-11|
|Matrix report|21.0.1|2025-07-31|
|McAfee ePO Integration for Security Operations|10.6.0|2025-12-11|
|MCP Client|1.0.1|2026-05-05|
|MCP for Strategic Portfolio Management|1.4.0|2026-09-10|
|Meeting CAB|9.4.2|2026-09-10|
|Meeting Extensions for Microsoft Teams|1.8.0|2025-12-11|
|Meeting Watcher - UI Builder Data Resource|9.4.2|2026-09-10|
|Mentoring|2.4.3|2026-08-07|
|Metadata Search|1.2.1|2026-09-10|
|Metric data table|22.5.0|2026-08-07|
|Metric Intelligence|2.7.11|2025-12-11|
|Metric Rules|1.1.4|2024-06-06|
|Metrics and CI Actions Framework|9.4.2|2026-09-10|
|Microsoft 365 for ServiceNow Reporting|23.0.2|2026-09-10|
|Microsoft Active Directory v2 Spoke|2.5.1|2025-10-16|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure Application Insights Spoke|2.0.0|2024-11-07|
|Microsoft Azure Artifacts Spoke|1.1.0|2024-11-07|
|Microsoft Azure Automation Spoke|2.0.0|2024-11-07|
|Microsoft Azure Blob Storage Spoke|2.0.0|2024-11-07|
|Microsoft Azure Cosmos DB Spoke|2.0.0|2024-11-07|
|Microsoft Azure DevOps Boards Spoke|3.1.0|2025-09-10|
|Microsoft Azure DevOps Integration for Agile Development|1.7.0|2025-12-11|
|Microsoft Azure DevOps Integrations Common|1.9.0|2025-12-11|
|Microsoft Azure DevOps Pipelines Spoke|1.0.0|2023-08-03|
|Microsoft Azure Managed Storage Spoke|2.0.1|2024-11-07|
|Microsoft Azure Notification Hub Spoke|2.0.0|2024-11-07|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure OpenAI Generative AI Spoke|3.12.3|2026-08-07|
|Microsoft Azure RBAC Spoke|1.0.2|2025-09-10|
|Microsoft Azure Resource Management Spoke|2.0.0|2024-11-07|
|Microsoft Azure Sentinel Incident Ingestion Integration For Security Operations|11.2.3|2026-05-05|
|Microsoft Azure SQL Database Spoke|2.0.0|2024-11-07|
|Microsoft Azure Traffic Manager Spoke|2.0.0|2024-11-07|
|Microsoft Azure Virtual Machine Spoke|2.0.0|2024-11-07|
|Microsoft Azure Virtual Network Spoke|2.0.0|2024-11-07|
|Microsoft Defender for Cloud Integration for Security Operations|2.8.0|2025-12-11|
|Microsoft Defender for Office365 Integration for SecOps|2.3.4|2024-12-05|
|Microsoft Dynamics 365 for Finance and Operations Spoke|2.4.3|2026-01-20|
|Microsoft Dynamics 365 Spoke|1.1.0|2025-07-31|
|Microsoft Dynamics CRM Spoke|1.9.0|2025-11-06|
|Microsoft Endpoint Configuration Manager for Investigation|9.4.2|2026-09-10|
|Microsoft Endpoint Configuration Manager Spoke|1.8.1|2025-06-05|
|Microsoft Entra ID Integration for Password Reset|3.0.3|2025-01-30|
|Microsoft Entra ID Spoke|4.7.3|2025-12-11|
|Microsoft Exchange Online for Security Operations|10.7.2|2026-01-20|
|Microsoft Exchange Online Spoke|3.12.0|2025-11-06|
|Microsoft Exchange Server Spoke|2.5.1|2025-11-06|
|Microsoft Graph Security API Alert Ingestion Integration For Security Operations|10.5.5|2026-07-09|
|Microsoft Integrations - Core|5.8.1|2025-12-11|
|Microsoft Intune Spoke|1.2.0|2025-11-06|
|Microsoft Office add-in|22.3.0|2026-06-16|
|Microsoft OneDrive Spoke|2.8.1|2025-11-06|
|Microsoft Outlook Add-In for Legal Service Delivery|1.5.0|2025-12-11|
|Microsoft Security Response Center Spoke|1.3.0|2025-09-10|
|Microsoft SharePoint File Explorer Connector for Security Incident Response integration|1.3.0|2025-12-11|
|Microsoft SharePoint Online Spoke|2.10.0|2025-09-10|
|Microsoft Teams Chat Connector for Security Incident Management|1.2.30|2025-10-16|
|Microsoft Teams Communications Spoke|1.5.0|2025-12-11|
|Microsoft Teams Graph Spoke|4.4.1|2026-02-05|
|Microsoft Word Add-in for ServiceNow Contracts|1.6.7|2025-12-11|
|MID Admin Workspace|2.0.1|2026-07-09|
|MID Guardian|1.0.4|2025-12-11|
|MID Server Infrastructure|2.0.1|2026-07-09|
|MIF Customer Instance|4.1.3|2026-08-07|
|Migration Utility for Service Operations Workspace|2.3.1|2025-05-01|
|Milestones|2.9.1|2026-09-10|
|Miro Spoke|3.3.1|2025-12-11|
|MISP integration for Security Operations|1.4.4|2026-02-05|
|Mitigation Controls Monitoring|4.1.4|2025-12-11|
|Mobile App Builder|27.11.0|2025-07-31|
|Mobile App Builder API|27.11.0|2025-07-31|
|Mobile Builder AI|27.6.0|2026-07-09|
|Mobile Card Builder|26.12.0|2025-07-31|
|Mobile Publishing|24.0.0|2025-12-11|
|Mobile SDK|2.2.0|2025-03-12|
|Mobile Time Sheets|2.3.0|2025-12-11|
|Model Context Protocol Client|2.4.4|2026-09-10|
|Model Context Protocol Server|1.8.0|2026-09-10|
|monday.com Spoke|1.1.5|2025-06-05|
|MSIM VTB Task Card|1.0.1|2024-02-01|
|MS Teams Activities for PAD|1.0.3|2023-01-12|
|Multi-case creation framework|2.1.0|2025-07-31|
|Natural Language Understanding Models for Sourcing and Procurement Operations|2.0.5|2023-05-04|
|Navex EthicsPoint Spoke|1.0.3|2025-12-11|
|News Integration for Supplier Lifecycle Operations|10.0.0|2026-09-10|
|NLU Workbench - Advanced Features|7.0.22|2025-07-10|
|Node map Experience Component|27.3.2|2026-08-07|
|Notification Flow Wizards|2.0.1|2022-09-21|
|Notifications Email Agents|3.0.2|2026-09-10|
|Notifications for Employee Center|2.2.0|2026-07-09|
|Notify Connector for Microsoft Teams|2.10.0|2025-12-11|
|Notify UI Components for Configurable Workspaces|9.4.2|2026-09-10|
|Notify Webex Connector|1.4.0|2025-12-11|
|Notify Zoom Connector|1.9.0|2025-07-31|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Prompt Assistance|6.0.7|2026-09-10|
|Now Assist for Service Graph Connectors|1.1.0|2025-01-30|
|Now Learning Integration|1.0.3|2024-02-01|
|Obligation Management|1.5.5|2025-12-11|
|Observability Commons for CMDB|1.1.0|2023-11-02|
|observ-ai-agents-app|6.3.1|2026-09-10|
|Okta Spoke|4.7.1|2025-11-06|
|Omnichannel Callback|2.1.0|2026-09-10|
|Omnichannel Callback for Customer Service Management|1.5.1|2025-12-11|
|Omni-Experience Standard Feature Set|8.3.1|2026-09-10|
|On Call Scheduling for Service Operations Workspace|9.4.3|2026-09-10|
|On-Call UI Components for Configurable Workspaces|9.4.2|2026-09-10|
|OneLogin Spoke|1.0.2|2023-09-07|
|One-time Password Generator|1.1.0|2025-12-11|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management|23.0.4|2026-09-10|
|Operational Sustainability Management Advanced|23.0.1|2026-09-10|
|Operational Sustainability Management Prime|23.0.3|2026-09-10|
|Operational Technology Change Management|4.1.4|2026-08-13|
|Operational Technology Hardware Vulnerability Assessment|4.1.6|2026-09-10|
|Operational Technology Health|4.1.2|2026-08-13|
|Operational Technology Incident Management|4.0.0|2026-06-16|
|Operational Technology Incident Management|4.0.0|2026-06-16|
|Operational Technology Incident Management|4.0.0|2026-06-16|
|Operational Technology Manager|4.1.6|2026-09-10|
|Operational Technology Setup|1.0.0|2026-09-10|
|Operational Technology Vulnerability Response|3.2.7|2026-09-10|
|Opportunity Management Application|14.1.0|2026-09-10|
|Opportunity Management Data Model|14.1.0|2026-09-10|
|Opportunity Management for Business Locations|2.0.0|2026-03-12|
|Opportunity Marketplace|2.7.0|2026-06-16|
|Oracle Autonomous DB Spoke|1.0.6|2022-12-01|
|Oracle Block Storage Spoke|1.0.4|2022-12-01|
|Oracle Boot Volume Spoke|1.0.6|2022-12-01|
|Oracle Cloud IAM Spoke|1.1.3|2022-09-21|
|Oracle Compute Engine Spoke|1.0.4|2022-12-01|
|Oracle EBS Spoke|1.13.2|2025-07-10|
|Oracle Financial Cloud Spoke|1.2.0|2025-11-06|
|Oracle HCM Cloud Spoke|4.3.0|2025-12-11|
|Oracle Netsuite Spoke|1.0.3|2025-09-10|
|Oracle Object Storage Management Spoke|1.0.3|2022-09-21|
|Oracle Peoplesoft Financial Spoke|1.1.0|2024-03-07|
|Oracle Virtual Cloud Network Spoke|1.0.4|2022-12-01|
|Order Case Playbook|1.4.1|2025-12-11|
|Order Case Playbook|1.4.1|2025-12-11|
|Order Case Self Service|2.2.0|2026-09-10|
|Order Case Self Service|2.2.0|2026-09-10|
|Order Management|18.3.3|2026-09-10|
|Order Management|5.0.0|2023-02-02|
|Order Management|18.3.3|2026-09-10|
|Order Management for Business Locations|2.0.0|2026-03-12|
|Order Management for Telecom, Media and Tech|13.1.2|2025-12-11|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Operations Case Management|3.1.3|2026-09-10|
|Order Operations Case Management|3.1.3|2026-09-10|
|Order Qualification Management|5.2.1|2026-09-10|
|Order Qualification Management|5.2.1|2026-09-10|
|Order to cash common architecture|1.6.6|2026-09-10|
|OT Asset Management|2.2.1|2026-09-10|
|OT Asset Management Advanced|2.0.1|2026-09-10|
|OT Manager Foundation|3.3.3|2026-06-16|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|Outlook Actionable Messages|4.7.0|2026-06-16|
|Outsourced Customer Service|2.1.2|2026-03-12|
|PA AI Tools|1.0.4|2026-09-10|
|PagerDuty Spoke|1.5.1|2026-01-20|
|Palo Alto Networks NGFW for Security Operations|10.5.2|2025-12-11|
|Parallel Review and Feedback|21.1.0|2025-12-11|
|PAR CoreUI Migration Scripts|4.0.3|2026-03-12|
|Participant Suggestions|2.0.1|2024-08-01|
|Password Reset for Service Operations Workspace|9.4.2|2026-09-10|
|Password Reset for Virtual Agent|5.0.6|2025-07-31|
|Password Reset integration for Microsoft Active Directory|4.0.0|2025-07-31|
|Password Reset integration with Google Directory|1.0.3|2023-06-01|
|Password Reset integration with Okta|1.1.2|2023-04-06|
|Password Reset UI components for Configurable Workspaces|9.4.2|2026-09-10|
|Patch Management Data Model|1.0.4|2025-05-01|
|Pattern Designer Enhancements|3.9.0|2025-12-11|
|Payment Card|1.5.1|2026-08-07|
|Payment Card|1.5.1|2026-08-07|
|Payment Card|1.5.1|2026-08-07|
|Payment Card|1.5.1|2026-08-07|
|Payment framework for conversational channels|1.1.0|2026-03-12|
|PDF Extractor|28.2.1|2025-12-11|
|PDF Extractor|28.2.1|2025-12-11|
|PDF Extractor|28.2.1|2025-12-11|
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
|Performance Analytics Content Pack for Agile 2.0|1.4.6|2025-12-11|
|Performance Analytics Content Pack for Cloud Resources|1.5.0|2024-11-07|
|Performance Analytics Content Pack for Essential SAFe|1.4.2|2023-09-20|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Legal Service Delivery|2.7.0|2025-12-11|
|Performance Analytics Content Pack for Public Sector Digital Services|2.0.3|2024-09-10|
|Performance Analytics - Content Pack - Guided Tours|1.4.0|2026-03-12|
|Performance Analytics for Configuration Compliance|1.5.2|2025-12-11|
|Performance Analytics for Security Incident Response|10.5.2|2025-05-01|
|Performance Analytics for Sourcing and Procurement Operations|3.0.9|2024-08-01|
|Performance Analytics for Vulnerability Response|12.16.1|2025-12-11|
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
|Performance Appraisal App Template|28.2.1|2025-12-11|
|Personal Lines Claims|4.4.0|2026-03-12|
|Personal Lines Claims|4.4.0|2026-03-12|
|Personal Lines Claims|4.4.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Physical Assets|2.3.0|2026-03-12|
|Pipeline|29.2.6|2026-08-07|
|Planned Maintenance Management|2.14.0|2026-06-16|
|Planned Task Common|1.1.0|2025-12-11|
|Planned Work Management|2.11.0|2025-12-11|
|Platform AI Agents and Skills|14.0.10|2026-09-10|
|Platform Analytics|8.4.1|2026-07-09|
|Playbook Experience|29.6.3|2026-09-10|
|Playbook Experience Components|29.6.2|2026-09-10|
|Playbooks for Customer Service Management|6.5.1|2026-06-16|
|Plivo Spoke|1.2.0|2025-11-06|
|Pluralsight Spoke|1.3.0|2026-08-07|
|Policy as Code Engine|3.3.0|2026-06-16|
|policy-as-code-engine-ui|3.3.0|2026-06-16|
|POM - Foundation|1.1.2|2026-06-16|
|POM - Prime|1.3.1|2026-09-10|
|Portal navigation demo|27.0.0|2025-06-05|
|Portal Next Experience Theme|24.3.2|2026-06-16|
|Portfolio Planning|8.18.0|2026-09-10|
|Portfolio Planning Core|5.13.5|2026-09-10|
|Portfolio Planning integrations for Shared Infrastructure|3.12.2|2026-08-07|
|Portfolio Planning with PPM, Agile 2.0, and SAFe|4.7.2|2026-08-07|
|Post Assessment Actions for Smart Assessments|23.0.3|2026-09-10|
|PPM Collaboration|2.1.0|2024-11-07|
|Predictive Intelligence for Legal Service Delivery|1.2.0|2025-12-11|
|Predictive Intelligence for User Reported Phishing|10.3.7|2024-09-10|
|Predictive Intelligence Store App|1.0.3|2025-12-11|
|Preferred tables|29.1.1|2026-03-12|
|Price Management|18.0.4|2026-09-10|
|Privacy Employee User|19.0.1|2024-08-01|
|Privacy Management Advanced|23.0.2|2026-09-10|
|Privacy Management Prime|23.0.2|2026-09-10|
|Private cloud orchestration|1.0.0|2025-12-11|
|Proactive Customer Service Operations|25.0.1|2026-03-12|
|Proactive Customer Service Operations with Event Management|25.0.2|2026-03-12|
|Proactive Engagement|5.2.0|2026-09-10|
|Proactive Prompts|3.5.1|2026-06-16|
|Proactive Service Experience Workflows|8.6.2|2026-07-09|
|Proactive Triggers|3.0.10|2025-12-11|
|Problem Management for Service Operations Workspace|9.4.2|2026-09-10|
|Problem Management Migration Utility|2.3.0|2026-03-12|
|Process Automation Content|28.1.4|2025-09-10|
|Process Automation Designer|29.6.4|2026-09-10|
|Process Automation Experience Demo|24.1.4|2024-10-03|
|Process Mining|29.7.9|2026-05-05|
|Process Mining Content Pack for CSM|23.2.0|2025-07-31|
|Process Mining Content Pack for FSM|1.5.0|2026-03-12|
|Process Mining Content Pack for SPM|1.0.2|2026-03-12|
|Process Mining for external data|29.5.0|2026-03-12|
|Process Mining for external data|29.5.0|2026-03-12|
|Process Mining for external data|29.5.0|2026-03-12|
|Process Mining for Source-to-Pay Operations|1.0.1|2024-08-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining Workspace Components|29.7.9|2026-05-05|
|Procurement Case Management|20.0.0|2026-09-10|
|Procurement File Transfer Framework|2.2.2|2023-05-04|
|Procurement for Field Service|3.0.0|2026-03-12|
|Product and pricing rules|9.0.0|2025-12-11|
|Product Capability Core|2.2.2|2026-07-09|
|Product Catalog Advanced|10.5.0|2026-09-10|
|Product Catalog Advanced|10.5.0|2026-09-10|
|Product Catalog Management Core|20.0.2|2026-09-10|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Conditions Core|4.6.9|2026-09-10|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Inventory Advanced|14.3.3|2026-09-10|
|Product Inventory Advanced|14.3.3|2026-09-10|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Support for Technology|4.3.6|2026-07-09|
|Profanity filter for agent chat|3.0.12|2024-11-07|
|Professional Data Model|1.1.0|2025-12-11|
|Project Status Report|1.1.0|2023-02-02|
|Project Workspace|7.6.2|2026-09-10|
|prompt-management|2.0.6|2026-07-09|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|Public Sector Digital Services AI Agent Collection|2.0.4|2026-09-10|
|Public Sector Digital Services Core|15.0.6|2026-09-10|
|Purchase Order Management|3.0.4|2026-09-10|
|Qualtrics Spoke|1.3.0|2025-11-06|
|Qualys Integration for Security Operations|12.19.6|2025-12-11|
|Query Generation|6.3.1|2026-09-10|
|Query Orchestrator|1.3.1|2026-08-07|
|Query Orchestrator|1.3.1|2026-08-07|
|Quick filter component|27.2.3|2026-06-16|
|Quick links component for Service Operations Workspace|9.4.2|2026-09-10|
|Quote AI agent|3.0.8|2026-09-10|
|Quote Management Application|9.1.0|2025-12-11|
|Quote Management Data Model|9.0.0|2025-12-11|
|Quote Management for Business Locations|2.0.0|2026-03-12|
|RAG for code generation|1.1.14|2026-09-10|
|Rally Spoke|1.0.3|2023-05-04|
|Rapid7 Integration for Security Operations|13.16.4|2025-12-11|
|Recommendation template|23.0.2|2026-09-10|
|Recommended Actions|44.0.4|2026-09-10|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions for Customer Service|30.0.1|2025-07-31|
|Recommended Actions for ITSM|3.4.1|2026-08-07|
|Recommended Actions for OTSM|3.1.0|2026-03-12|
|Recommended Actions for Security Operations|2.3.6|2026-09-10|
|Record lookup connected component|28.0.1|2025-12-11|
|Record Page for Service Operations Workspace|9.4.2|2026-09-10|
|Record Related Items Connected|2.2.0|2025-12-11|
|Record - vertical|23.0.3|2026-09-10|
|Recruiter Workspace|8.0.1|2026-07-09|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Regulatory Agency Library|23.0.2|2026-09-10|
|Related party|1.0.6|2023-02-02|
|Related party|1.0.6|2023-02-02|
|ReleaseOps|1.2.3|2026-02-05|
|Release Timeline Component|1.4.0|2025-12-11|
|Remedial Actions Framework|9.3.3|2026-08-07|
|Remediation Playbooks|1.1.0|2022-11-03|
|Reporting UI Component for Workspace|2.5.0|2026-07-09|
|Requester Experience Templates|1.0.0|2024-11-07|
|Request Management for Service Operations Workspace|9.4.2|2026-09-10|
|Requirement Intake Diagram|1.0.1|2024-12-05|
|Resizable panes component|28.0.3|2025-12-11|
|Resolution Shaper|29.0.10|2026-03-12|
|Resolution Shaper|29.0.10|2026-03-12|
|Resource Management Workspace|5.10.1|2026-09-10|
|Retail Core|7.6.0|2026-09-10|
|Retail MCP Server|1.0.0|2026-09-10|
|Retry Handler Framework|1.0.2|2022-09-21|
|Rich Text Editor Component for Security Operations|2.0.1|2026-06-16|
|Risk Assessments for Supplier Lifecycle Operations|8.0.1|2026-09-10|
|RMA Case Management|2.3.4|2026-09-10|
|Roadmap UI Builder Component|22.14.2|2026-09-10|
|Roadmunk Spoke|1.6.5|2024-07-11|
|RPA Hub|18.1.2|2026-08-07|
|RPA Plugin Bundle|18.0.4|2026-08-07|
|RSM - Advanced|1.1.1|2026-08-07|
|RSM - Advanced|1.1.1|2026-08-07|
|RSM - Foundation|1.1.1|2026-08-07|
|RSM - Foundation|1.1.1|2026-08-07|
|RSM - Prime|1.1.1|2026-08-07|
|RSM - Prime|1.1.1|2026-08-07|
|Saba Spoke|1.2.2|2026-06-16|
|Safe Workplace Dashboard|1.41.0|2025-07-31|
|Safe Workplace for mobile|2.10.3|2025-07-31|
|Safe Workplace suite|1.34.2|2025-07-31|
|Safe Workplace suite Professional|1.25.2|2025-07-31|
|Sales Agreement Data Model|8.0.0|2025-12-11|
|Sales Agreement Management|8.0.0|2025-12-11|
|Sales and Order Management for Technology Provider - Advanced|1.0.8|2026-09-10|
|Sales and Order Management for Technology Provider - Prime|1.0.7|2026-09-10|
|Sales and Order Management for Telecommunications, Media and Technology - Advanced|1.0.7|2026-09-10|
|Sales and Order Management for Telecommunications, Media and Technology - Prime|1.0.9|2026-09-10|
|Sales and Order Management for Telecommunications - Advanced|2.3.2|2026-09-10|
|Sales and Order Management for Telecommunications - Prime|2.3.2|2026-09-10|
|Sales and Order Management Mobile Common|29.1.2|2026-03-12|
|Sales Cart|2.1.0|2025-12-11|
|Sales Cart|2.1.0|2025-12-11|
|Sales Common|8.1.2|2026-09-10|
|Sales Development AI Agents|1.0.12|2026-09-10|
|Salesforce Marketing Cloud Spoke|1.5.1|2025-03-12|
|Salesforce Spoke|2.3.4|2025-11-06|
|Sales Forecasting|2.0.1|2025-12-11|
|Sales Quota Application|1.1.0|2025-12-11|
|Sales Quota Data Model|1.1.0|2025-12-11|
|Sales Territory Management|2.0.0|2026-03-12|
|SBOM Core|6.2.2|2025-12-11|
|SBOM Response|6.4.1|2025-12-11|
|Scan Engine|6.0.3|2026-09-10|
|SCCM Usage Metering Spoke|1.0.2|2023-09-07|
|Scenario Planning for PPM|2.4.0|2025-12-11|
|Schedule Optimization|29.0.22|2026-08-07|
|Scope 3 emissions management|21.1.1|2025-12-11|
|Screen Summarization|1.2.6|2026-08-07|
|Scrum Common|1.4.5|2025-01-30|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Secops Health Analytics|2.4.3|2025-12-11|
|Secureworks CTP Spoke|1.0.3|2022-09-21|
|Secureworks Ticket Ingestion Integration for Security Operations|11.1.2|2026-02-05|
|Security Case Management common PAD artefacts|1.1.12|2026-01-20|
|Security Case Management common workspace components|2.1.3|2026-09-10|
|Security Center|3.2.5|2026-06-16|
|Security Incident Response|14.4.0|2026-09-10|
|Security Incident Response - Advanced|1.0.10|2026-09-10|
|Security Incident Response - Foundation|1.0.10|2026-09-10|
|Security Incident Response integration with AWS SecurityHub|1.1.0|2025-12-11|
|Security Incident Response Integration with CrowdStrike Next-Gen SIEM|2.3.1|2025-12-11|
|Security Incident Response integration with FireEye HX|1.1.0|2025-12-11|
|Security Incident Response integration with Microsoft Defender for Endpoint|1.2.1|2026-02-05|
|Security Incident Response Integration with Palo Alto Networks XSIAM|3.0.2|2026-01-20|
|Security Incident Response integration with Proofpoint|1.1.0|2025-12-11|
|Security Incident Response Integration with Zscaler|11.2.3|2026-02-05|
|Security Incident Response Mobile|10.4.0|2024-11-07|
|Security Incident Response - Prime|1.0.10|2026-09-10|
|Security Incident Response Workspace|1.10.1|2026-09-10|
|Security Incident UI Card Component|1.0.5|2026-09-10|
|Security Integration Framework|13.13.0|2026-07-09|
|Security Operations 'Have I been pwned?' Integration|10.5.1|2025-03-12|
|Security Operations CrowdStrike Intelligence Integration|10.8.0|2025-12-11|
|Security Operations Hybrid Analysis Integration|10.7.0|2026-02-05|
|Security Operations LogRhythm Integration|11.2.1|2025-12-11|
|Security Operations Metadefender Integration|10.5.0|2024-08-01|
|Security Operations Palo Alto Networks - AutoFocus|10.4.0|2025-01-30|
|Security Operations Palo Alto Networks - WildFire|10.4.0|2025-01-30|
|Security Operations PhishTank Integration|10.5.0|2024-08-01|
|Security Operations Reverse WHOIS Integration|10.5.0|2025-12-11|
|Security Operations RiskIQ Integration|10.4.1|2024-08-01|
|Security Operations Setup Assistant|10.4.41|2026-06-16|
|Security Operations Shodan Integration|10.4.1|2024-08-01|
|Security Operations Spoke|10.6.7|2025-06-05|
|Security Operations VirusTotal Integration|10.4.1|2025-12-11|
|Security Posture Control Core|7.0.1|2025-12-11|
|Security Simulation and Training Integration for SecOps|2.1.3|2024-05-09|
|Security Support Common|30.6.5|2026-09-10|
|Security Support Orchestration|12.13.4|2025-01-30|
|Service Bridge for Public Sector Digital Services \(PSDS\)|1.0.2|2025-05-01|
|Service Builder|3.6.1|2025-12-11|
|Service Builder Components|2.2.0|2025-12-11|
|Service Catalog AI Core|1.0.2|2026-09-10|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Contractor Base|2.0.0|2026-03-12|
|Service Exchange - Advanced|1.1.13|2026-08-13|
|Service Exchange Base|2.3.29|2026-08-07|
|Service Exchange for Consumers|2.3.29|2026-08-07|
|Service Exchange for Providers|2.2.25|2026-08-07|
|Service Exchange - Foundation|1.1.13|2026-08-13|
|Service Exchange Health|2.3.29|2026-08-07|
|Service Exchange Order Management for Providers|2.2.25|2026-08-07|
|Service Exchange - Prime|1.1.13|2026-08-13|
|Service Exchange Remote Process Sync Transport|2.3.29|2026-08-07|
|Service Graph Connector Dependencies|1.0.0|2021-01-21|
|Service Graph Connector for Akamai API Security|1.0.0|2025-10-16|
|Service Graph Connector for AWS|2.12.1|2025-10-16|
|Service Graph Connector for ExtraHop|2.0.3|2020-09-16|
|Service Graph Connector for GCP|1.11.0|2025-10-16|
|Service Graph Connector for Google Console|1.0.0|2024-08-01|
|Service Graph Connector for Infoblox|1.4.0|2025-07-31|
|Service Graph Connector for Jamf|2.14.4|2025-09-10|
|Service Graph Connector for Microsoft Azure|1.15.0|2025-12-11|
|Service Graph Connector for Microsoft Defender Endpoint|1.2.0|2025-05-01|
|Service Graph Connector for Microsoft Defender for IoT \(Azure\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Excel|4.1.5|2026-09-10|
|Service Graph Connector for Microsoft Intune|2.7.1|2025-10-16|
|Service Graph Connector for Microsoft SCCM|3.8.0|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Service Graph Connector for Observability - AppDynamics|1.6.0|2025-12-11|
|Service Graph Connector for Observability - Datadog|1.4.0|2025-12-11|
|Service Graph Connector for Observability - Dynatrace|1.13.1|2025-09-10|
|Service Graph Connector for Observability - New Relic|1.4.0|2025-12-11|
|Service Graph Connector for OpenTelemetry|1.4.1|2024-05-09|
|Service Graph Connector for SolarWinds|2.6.0|2025-07-31|
|Service Graph Connector for Tanium|1.8.2|2025-11-06|
|Service Graph Connector for Trellix|1.0.0|2025-06-05|
|Service Graph Connector for VMware Workspace ONE UEM|1.8.0|2025-07-31|
|Service Graph Connector for Wiz|1.4.0|2025-11-06|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Licensing|1.0.0|2022-05-05|
|Service Graph Connector Support Tools|1.0.0|2024-02-01|
|Service Level Management Experience for Workspace|9.4.2|2026-09-10|
|Service Level Objective Management for Service Operations Workspace|2.0.0|2026-06-16|
|Service Mapping Plus|1.17.2|2026-01-20|
|ServiceNow Add-Ins for Microsoft Office|7.4.0|2025-12-11|
|ServiceNow AI Lens|8.1.1|2026-09-10|
|ServiceNow AI Lens Core|8.1.1|2026-09-10|
|ServiceNow Document Designer with Word|23.0.3|2026-09-10|
|ServiceNow EmployeeWorks Web App Base|2.3.6|2026-09-10|
|ServiceNow Enterprise Asset Management|11.0.0|2026-09-10|
|ServiceNow IDE|5.0.2|2026-09-10|
|ServiceNow ITOM/OT SU Licensing|3.13.1|2026-07-09|
|ServiceNow Kafka Consumer|1.0.1|2023-04-06|
|ServiceNow Otto Agents for requestor|3.7.6|2026-09-10|
|ServiceNow Otto AI Agents|9.0.11| |
|ServiceNow Otto AI web agent|33.0.3|2026-09-10|
|ServiceNow Otto context menu|3.9.0|2026-09-10|
|ServiceNow Otto Conversational Data Collection|10.2.22|2026-09-10|
|ServiceNow Otto for Accounts Payable Operations \(APO\)|9.0.0|2026-09-10|
|ServiceNow Otto for AI Control Tower|24.0.4|2026-09-10|
|ServiceNow Otto for AIRC|23.0.1|2026-09-10|
|ServiceNow Otto for AI Search|18.0.5|2026-09-10|
|ServiceNow Otto for App Engine|30.1.1|2026-09-10|
|ServiceNow Otto for Automation Center|1.3.0|2026-08-07|
|ServiceNow Otto for Care Team Operations|2.1.1|2026-09-10|
|ServiceNow Otto for Care Team Operations|2.1.1|2026-09-10|
|ServiceNow Otto for Cloud Cost Management|1.0.0|2026-09-10|
|ServiceNow Otto for Code|28.5.32|2026-09-10|
|ServiceNow Otto for Collaborative Work Management \(CWM\)|7.0.2|2026-09-10|
|ServiceNow Otto for Configuration Management Database \(CMDB\)|4.4.1|2026-09-10|
|ServiceNow Otto for Contract Analysis|1.0.15|2026-08-07|
|ServiceNow Otto for Contract Management Pro|2.5.2|2026-09-10|
|ServiceNow Otto for Conversational Spokes|1.1.2|2026-08-07|
|ServiceNow Otto for Core Business Suite|3.3.2|2026-08-07|
|ServiceNow Otto for Core Business Suite|3.3.2|2026-08-07|
|ServiceNow Otto for CPQ|1.1.8|2026-09-10|
|ServiceNow Otto for Creator|29.6.2|2026-09-10|
|ServiceNow Otto for CSM Complaint Case|2.2.1|2026-08-07|
|ServiceNow Otto for CSM Major Issue Management|1.2.4|2026-08-07|
|ServiceNow Otto for Customer Service Management \(CSM\)|15.0.1|2026-09-10|
|ServiceNow Otto for Digital End-user Experience \(DEX\)|5.2.10|2026-09-18|
|ServiceNow Otto for Document Voice|2.0.11|2026-09-10|
|ServiceNow Otto for Employee Center Pro|1.2.6|2026-09-03|
|ServiceNow Otto for Employee Experience|4.4.3|2026-08-07|
|ServiceNow Otto for Enterprise Architecture \(EA\)|7.5.2|2026-08-07|
|ServiceNow Otto for Enterprise Asset Management|2.0.1|2026-09-10|
|ServiceNow Otto for Error Framework|1.2.0|2026-09-10|
|ServiceNow Otto for Field Service Management|11.1.2|2026-09-10|
|ServiceNow Otto for Finance and Procurement|8.0.0|2026-09-10|
|ServiceNow Otto for Financial Services Operations \(FSO\)|3.4.3|2026-09-04|
|ServiceNow Otto for Hardware Asset Management|5.0.1|2026-09-10|
|ServiceNow Otto for Health and Safety|1.5.1|2026-08-07|
|ServiceNow Otto for HRSD - Galileo Inside|2.3.7|2026-09-10|
|ServiceNow Otto for HR Service Delivery \(HRSD\)|13.5.2|2026-09-10|
|ServiceNow Otto for ICW|1.1.0|2026-08-07|
|ServiceNow Otto for Impact|6.0.6|2026-09-10|
|ServiceNow Otto for Integrated Risk Management|23.0.4|2026-09-10|
|ServiceNow Otto for Integration Hub|2.3.2|2026-08-07|
|ServiceNow Otto for IT Operations Management \(ITOM\)|2.9.4|2026-09-10|
|ServiceNow Otto for IT Service Management \(ITSM\)|17.2.2|2026-09-18|
|ServiceNow Otto for Knowledge Management|31.6.6|2026-09-10|
|ServiceNow Otto for Legal Service Delivery|1.9.7|2026-09-10|
|ServiceNow Otto for Manufacturing Commercial Operations \(MCO\)|4.1.0|2026-09-10|
|ServiceNow Otto for Operational Sustainability|23.0.1|2026-09-10|
|ServiceNow Otto for Opportunity Management|1.2.0|2026-09-10|
|ServiceNow Otto for Order Management|2.3.3|2026-09-10|
|ServiceNow Otto for OT Service Management|3.1.5|2026-08-07|
|ServiceNow Otto for Platform|13.0.1|2026-09-10|
|ServiceNow Otto for Platform Advanced|3.0.1|2026-09-10|
|ServiceNow Otto for Platform Foundation|3.0.1|2026-09-10|
|ServiceNow Otto for Platform Prime|3.0.1|2026-09-10|
|ServiceNow Otto for Privacy Management|23.0.2|2026-09-10|
|ServiceNow Otto for Process Mining|4.1.5|2026-09-10|
|ServiceNow Otto for Public Sector Digital Services \(PSDS\)|2.5.3|2026-09-10|
|ServiceNow Otto for Purchase Order Management \(POM\)|1.4.1|2026-09-10|
|ServiceNow Otto for Retail Service Management|1.6.0|2026-09-10|
|ServiceNow Otto for RPA Hub|5.1.1|2026-08-07|
|ServiceNow Otto for Sales and Order Management for Telecommunications|4.3.3|2026-09-10|
|ServiceNow Otto for Sales Automation|1.1.7|2026-09-10|
|ServiceNow Otto for Security Incident Response \(SIR\)|6.5.2|2026-09-10|
|ServiceNow Otto for Security Incident Response Integration Toolkit|1.2.5|2026-08-07|
|ServiceNow Otto for Service Exchange|1.1.12|2026-08-13|
|ServiceNow Otto for Service Quality|2.2.0|2026-09-10|
|ServiceNow Otto for Setup|5.0.20|2026-09-10|
|ServiceNow Otto for Setup Core|4.0.20|2026-09-10|
|ServiceNow Otto for Smart Assessment Engine|23.0.6|2026-09-10|
|ServiceNow Otto for Software Asset Management \(SAM\)|11.0.0|2026-09-10|
|ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)|11.0.0|2026-09-10|
|ServiceNow Otto for Spoke Generation|2.0.1|2026-08-07|
|ServiceNow Otto for Strategic Portfolio Management|9.11.0|2026-09-10|
|ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)|9.0.1|2026-09-10|
|ServiceNow Otto for Talent|1.9.2|2026-08-07|
|ServiceNow Otto for Talent|1.9.2|2026-08-07|
|ServiceNow Otto for Telecommunications, Media and Technology \(TMT\)|6.0.15|2026-09-10|
|ServiceNow Otto for Telecommunications Service Management|2.3.1|2026-09-10|
|ServiceNow Otto for Third-Party Risk Management|23.0.5|2026-09-10|
|ServiceNow Otto for Threat Intelligence Security Center|2.6.1|2026-09-10|
|ServiceNow Otto for Unified Security Exposure Management|5.2.3|2026-08-07|
|ServiceNow Otto for Unified Security Exposure Management|5.2.3|2026-08-07|
|ServiceNow Otto for Vault|2.2.2|2026-08-07|
|ServiceNow Otto for Virtual Agent|22.0.17|2026-09-18|
|ServiceNow Otto for Virtual Agent Configurations|16.0.5|2026-08-20|
|ServiceNow Otto for Voice Agents|6.0.5|2026-09-10|
|ServiceNow Otto for WDF|2.3.4|2026-08-07|
|ServiceNow Otto for Workplace Service Delivery \(WSD\)|1.1.20|2026-08-07|
|ServiceNow Otto for Wrap Up|1.0.4|2026-08-07|
|ServiceNow Otto for Zero Copy Connector|2.0.6|2026-08-07|
|ServiceNow Otto in Document Management|4.0.11|2026-09-18|
|ServiceNow Remote Instance Spoke|2.2.9|2025-11-06|
|ServiceNow Studio|30.1.1|2026-09-10|
|ServiceNow Studio for App Engine|28.2.1|2025-12-11|
|ServiceNow Voice|5.0.1|2026-02-05|
|ServiceNow Voice for CSM|3.10.0|2026-02-05|
|ServiceNow Voice for HR Service Delivery \(HRSD\)|1.0.5|2025-12-11|
|ServiceNow Voice for ITSM|4.1.1|2025-12-11|
|ServiceNow Voice UI components|3.8.0|2026-02-05|
|service-observability-app|1.10.12|2025-12-11|
|Service Observability UI|1.10.12|2025-12-11|
|Service Operations Workspace Admin Center|9.4.2|2026-09-10|
|Service Operations Workspace Alert Automation|25.11.1|2026-03-12|
|Service Operations Workspace Alert Automation|25.11.1|2026-03-12|
|Service Operations Workspace Alert Automation API|25.11.0|2026-03-12|
|Service Operations Workspace Alert Automation API|25.11.0|2026-03-12|
|Service Operations Workspace Alert Automation UI|25.11.0|2026-03-12|
|Service Operations Workspace Alert Mngmt|27.0.2|2026-03-12|
|Service Operations Workspace Core|9.4.2|2026-09-10|
|Service Operations Workspace Express List|27.0.8|2026-03-12|
|Service Operations Workspace Express List App|27.0.0|2026-03-12|
|Service Operations Workspace Integrations launchpad|27.0.3|2026-03-12|
|Service Operations Workspace Integrations launchpad UI|27.0.0|2026-03-12|
|Service Operations Workspace ITOM Apps|27.0.0|2026-03-12|
|Service Operations Workspace ITSM Admin Center|9.4.2|2026-09-10|
|Service Operations Workspace ITSM Advanced Applications|9.4.2|2026-09-10|
|Service Operations Workspace ITSM Applications|9.4.2|2026-09-10|
|Service Operations Workspace ITSM Common|9.4.2|2026-09-10|
|Service Operations Workspace Link View|27.0.0|2026-03-12|
|Service Operations Workspace Log Analytics|26.5.0|2025-12-11|
|Service Operations Workspace Metric Explorer|27.0.0|2026-03-12|
|Service Operations Workspace Metric Explorer APIs|23.4.0|2025-07-31|
|Service Operations Workspace Service Dashboard|27.1.0|2025-12-11|
|Service Operations Workspace Service Map Monitoring|26.5.0|2025-07-31|
|Service Operations Workspace Service Reliability Management \(SRM\) Common|7.0.0|2026-06-16|
|Service Operations Workspace UI Components|27.0.5|2026-03-12|
|Service Organization|2.9.0|2026-08-07|
|Service Reliability Management|7.0.0|2026-06-16|
|Service Request Criteria|3.1.0|2026-06-16|
|Service Request Management App Template|28.2.1|2025-12-11|
|Service Test Management|5.0.1|2025-12-11|
|Setup Hub|3.0.7|2026-09-10|
|Setup Hub Common|5.0.7|2026-09-10|
|Setup Hub Config|5.0.5|2026-09-10|
|Setup Hub Content|5.0.7|2026-09-10|
|SGC Central|2.7.2|2026-09-10|
|Shared Library for Talent Development|2.5.0|2026-06-16|
|SharePoint Online Search Connector|6.1.2|2024-11-07|
|Shift Handover Application|2.1.0|2026-09-10|
|Shift Planning for Configurable Workspace|3.7.0|2025-12-11|
|Shodan Exploit Integration for Security Operations|10.8.0|2024-11-07|
|Shopping Hub|11.1.1|2026-06-16|
|Shopping Hub Mobile|7.6.24|2025-07-31|
|Sitemap Generator|1.2.0|2025-07-31|
|Site Mapping for Field Service Management|2.1.1|2026-03-12|
|Site Reliability Metrics|2.1.7|2023-11-02|
|Site Reliability Metrics UX|2.1.7|2023-11-02|
|Site Reliability Operations|14.2.3|2024-05-09|
|Skill Rule|1.0.3|2026-03-12|
|Skills foundation|10.1.0|2026-06-16|
|Skills Industry Data|2.2.0|2026-06-16|
|Skills Workspace|6.1.0|2025-12-11|
|Slack Activities for PAD|1.0.3|2023-01-12|
|Slack Chat Connector for Security Incident Management|1.0.1|2025-05-01|
|Slack Spoke|1.8.0|2025-09-10|
|SLO - Foundation|2.0.2|2026-09-10|
|SLO - Prime|2.0.0|2026-09-10|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Smart Assessment Core|23.0.2|2026-09-10|
|Smart Assessment Migration tools|23.0.3|2026-09-10|
|SmartRecruiters Spoke|1.0.0|2021-11-18|
|Smartsheet Spoke|2.6.1|2026-01-20|
|sn-4q-bubble|23.2.3|2026-06-16|
|sn-actionable-insights|1.2.1|2026-08-07|
|sn-apm-diagram-builder|3.7.0|2026-06-16|
|sn-app-analytics-center|8.4.1|2026-07-09|
|sn-app-analytics-center|8.4.1|2026-07-09|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-par-components-chart-drilldown-configuration|8.4.3|2026-07-09|
|sn-app-par-components-chart-drilldown-configuration|8.4.3|2026-07-09|
|sn-app-par-components-component-builder|8.4.3|2026-07-09|
|sn-app-par-components-component-builder|8.4.3|2026-07-09|
|sn-app-par-components-config-panel|8.4.3|2026-07-09|
|sn-app-par-components-config-panel|8.4.3|2026-07-09|
|sn-app-par-components-config-panel-section-message|8.4.3|2026-07-09|
|sn-app-par-components-config-panel-section-message|8.4.3|2026-07-09|
|sn-app-par-components-create-dashboard-modal|8.4.3|2026-07-09|
|sn-app-par-components-create-dashboard-modal|8.4.3|2026-07-09|
|sn-app-par-components-create-indicator-modal|8.4.3|2026-07-09|
|sn-app-par-components-create-indicator-modal|8.4.3|2026-07-09|
|sn-app-par-components-dashboard-categories|8.4.3|2026-07-09|
|sn-app-par-components-dashboard-categories|8.4.3|2026-07-09|
|sn-app-par-components-data-visualization-wrapper|8.4.3|2026-07-09|
|sn-app-par-components-data-visualization-wrapper|8.4.3|2026-07-09|
|sn-app-par-components-divider|8.4.3|2026-07-09|
|sn-app-par-components-divider|8.4.3|2026-07-09|
|sn-app-par-components-dynamic-renderer|8.4.3|2026-07-09|
|sn-app-par-components-dynamic-renderer|8.4.3|2026-07-09|
|sn-app-par-components-export-email-composer|8.4.3|2026-07-09|
|sn-app-par-components-export-email-composer|8.4.3|2026-07-09|
|sn-app-par-components-export-modal|8.4.3|2026-07-09|
|sn-app-par-components-export-modal|8.4.3|2026-07-09|
|sn-app-par-components-info-content|8.4.3|2026-07-09|
|sn-app-par-components-info-content|8.4.3|2026-07-09|
|sn-app-par-components-info-panel|8.4.3|2026-07-09|
|sn-app-par-components-info-panel|8.4.3|2026-07-09|
|sn-app-par-components-insights-panel|8.4.3|2026-07-09|
|sn-app-par-components-insights-panel|8.4.3|2026-07-09|
|sn-app-par-components-library-recommendation-widgets|8.4.3|2026-07-09|
|sn-app-par-components-library-recommendation-widgets|8.4.3|2026-07-09|
|sn-app-par-components-saved-data-visualization|8.4.3|2026-07-09|
|sn-app-par-components-saved-data-visualization|8.4.3|2026-07-09|
|sn-app-par-components-scheduled-export|8.4.3|2026-07-09|
|sn-app-par-components-scheduled-export|8.4.3|2026-07-09|
|sn-app-par-components-share-dialog|8.4.3|2026-07-09|
|sn-app-par-components-share-dialog|8.4.3|2026-07-09|
|sn-app-par-components-share-info|8.4.3|2026-07-09|
|sn-app-par-components-share-info|8.4.3|2026-07-09|
|sn-app-par-coreui-migration-center|4.0.3|2026-03-12|
|sn-app-par-coreui-migration-legacy-widget|4.0.3|2026-03-12|
|sn-app-par-nacm-component|8.4.3|2026-07-09|
|sn-app-par-nacm-component|8.4.3|2026-07-09|
|sn-attach-article-guidance|32.0.1|2026-09-10|
|sn-circuit-map|5.0.0|2025-07-31|
|sn-circuit-map|5.0.0|2025-07-31|
|sn-circuit-map|5.0.0|2025-07-31|
|sn-cmdb-nlq-search|2.3.3|2024-11-07|
|sn-component-account-hierarchy|29.0.7|2026-03-12|
|sn-component-account-hierarchy|29.0.7|2026-03-12|
|sn-component-guidance-experience|42.0.2|2026-09-10|
|sn-component-workspace-ribbon|30.0.0|2026-03-12|
|sn-component-workspace-ribbon|30.0.0|2026-03-12|
|sn-component-workspace-shn|29.0.7|2026-03-12|
|sn-component-workspace-shn|29.0.7|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|sn-cwm-agile|2.2.1|2026-09-10|
|sn-dashboard|8.4.4|2026-07-09|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-docintel-iframe|1.0.4|2024-02-01|
|sn-docs|7.9.1|2026-09-10|
|sn-experiment-ui|1.1.14|2026-07-09|
|sn-formula-kit|1.2.2|2026-09-10|
|sn-guided-action-experience|39.0.1|2025-12-11|
|sn-guided-action-experience|39.0.1|2025-12-11|
|sn-guided-action-experience|39.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-hla-admin-experience|1.0.2|2026-01-20|
|sn-hr-casecard|1.3.2|2025-12-11|
|sn-ia-summary-card|1.1.0|2026-08-07|
|sn-itom-ui-internal|27.1.1|2025-12-11|
|sn-next-best-action-list|41.0.4|2026-09-10|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Snowflake Spoke|1.0.3|2025-09-10|
|sn-quick-filter-popover|24.3.1|2026-05-05|
|sn-rack|4.0.0|2025-07-31|
|sn-rack|4.0.0|2025-07-31|
|sn-rack|4.0.0|2025-07-31|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|sn-smart-assessment-connected|23.0.4|2026-09-10|
|sn-smart-assessment-designer|23.0.5|2026-09-10|
|sn-task-planner|22.15.0|2026-09-10|
|sn-timer|2.0.1|2026-03-12|
|sn-topology-map|4.0.0|2025-07-31|
|sn-topology-map|4.0.0|2025-07-31|
|sn-topology-map|4.0.0|2025-07-31|
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
|sn-uxf-formula-parser|29.1.0|2026-03-12|
|sn-viz-designer|8.4.1|2026-07-09|
|sn-viz-designer|8.4.1|2026-07-09|
|Socure Spoke|1.2.2|2026-03-12|
|Software Asset Management|4.1.7|2026-09-10|
|Software Asset Management AI Advanced|2.5.0|2026-09-10|
|Software Asset Management AI Prime|2.5.0|2026-09-10|
|Software Asset Management for CPE support|1.0.0|2022-08-04|
|Software Asset Management Guided Experiences|7.0.1|2026-03-12|
|Software Asset Management integration with Salesforce CRM|2.0.1|2025-12-11|
|Software Asset Management integration with Salesforce Marketing Cloud|1.2.7|2025-03-12|
|Software Asset Management integration with Tableau|1.0.1|2024-08-01|
|Software Asset Management integration with Workday|1.0.12|2025-01-30|
|Software Asset Management Professional for Engineering Applications|1.0.3|2026-03-12|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM for Manufacturing Advanced|3.0.0|2026-09-10|
|SOM for Manufacturing Prime|3.0.0|2026-09-10|
|SOM - Prime|1.0.1|2026-04-09|
|Source-to-Pay Common Architecture|25.0.0|2026-09-10|
|Source-to-Pay Integration Framework|14.0.2|2026-06-16|
|Source-to-Pay Operations with Contract Management Pro|2.0.1|2025-05-01|
|Source-to-Pay Workspace|21.0.0|2026-09-10|
|Sourcing and Purchasing Automation|11.7.0|2026-09-10|
|SOW Funnel Highchart Component|28.2.0|2025-12-11|
|Special Handling Instruction|26.0.3|2026-05-05|
|Spend and Savings Management|5.0.5|2026-08-07|
|Splunk Search Integration for Security Operations|10.5.0|2025-07-31|
|SPM Benchmarking|1.0.0|2022-11-03|
|SPM Common UI Component|4.1.1|2026-09-10|
|SPM Enterprise-Wide Deployment|1.0.5|2026-09-10|
|SPM Planning Attributes Core|1.18.3|2026-09-10|
|SPM Team Member|1.0.0|2026-04-09|
|SPO - Foundation|2.0.0|2026-09-10|
|Spoke Generator|4.2.4|2026-03-12|
|SPO - Prime|2.0.0|2026-09-10|
|SPW Jira Integrations|1.0.0|2025-12-11|
|Standard ticket page summarization|1.3.3|2026-08-07|
|Status Report UI Component for MSIM Workspace|1.0.2|2024-11-07|
|Strategic Planning|4.18.0|2026-09-10|
|Strategic Portfolio Management - Advanced|1.3.0|2026-09-10|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management - Prime|1.2.0|2026-09-10|
|Strategic Spend Tracking for PPM|1.2.0|2025-12-11|
|Stream Connect Designer|5.0.1|2026-03-12|
|Subscription Management v2|6.4.3|2026-06-16|
|SuccessFactors Learning Spoke|1.0.0|2025-01-30|
|Summarization for Order Management|2.2.4|2026-09-10|
|SumTotal Spoke|1.1.0|2023-03-02|
|Supplier Case Management|12.0.0|2026-09-10|
|Supplier Collaboration Portal|12.0.0|2026-09-10|
|Supplier Common Architecture|12.0.0|2026-09-10|
|Supplier Operations|8.0.0|2026-09-10|
|Supplier Payment Optimization|7.0.0|2026-09-10|
|Supplier Relationship and Performance Management|11.0.0|2026-09-10|
|SurveyMonkey Spoke|2.0.6|2024-08-01|
|Surveys for mobile|1.0.2|2021-09-16|
|Sustainable IT|21.1.0|2025-12-11|
|Synthetic Monitoring|1.4.4|2025-12-11|
|System Events and Jobs Dashboard|3.1.5|2026-03-12|
|Tableau Spoke|1.0.2|2024-08-01|
|Table Builder|29.1.1|2026-03-12|
|Tag Based Alert Clustering Engine|18.24.0|2026-06-16|
|Tag Governance|1.8.0|2025-12-11|
|Talent Development Core|5.5.0|2026-06-16|
|Talent feedback|1.4.1|2026-08-07|
|Talent profile|7.0.1|2026-07-09|
|Task activity timeline|25.4.0|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Task Communications Management UI Components for Configurable Workspaces|9.4.3|2026-09-10|
|Task Intelligence Admin Console|5.2.1|2025-12-11|
|Task Intelligence for Customer Service|25.4.0|2025-12-11|
|Task Intelligence for ITSM|8.2.1|2025-12-11|
|Task Plan Template AI Agents|2.0.1|2026-09-10|
|Task Plan Templates|5.0.0|2026-09-10|
|Task Quality Review Management|29.1.1|2026-03-12|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Task SLA cards|26.0.0|2026-03-12|
|Task SLA cards|26.0.0|2026-03-12|
|Team Contacts App Template|28.2.1|2025-12-11|
|Team Performance|202507.0.2|2025-07-31|
|Technician driven sales with Field Service|29.1.2|2026-03-12|
|Technology Advanced|1.0.12|2026-09-10|
|Technology Core|3.8.4|2026-06-16|
|Technology Core|3.8.4|2026-06-16|
|Technology Foundation|1.0.15|2026-09-10|
|Technology Portfolio Management|1.10.0|2026-06-16|
|Technology Prime|1.0.12|2026-09-10|
|Telecom Core|6.6.2|2026-07-09|
|Telecom Discovery Patterns|1.0.2|2025-12-11|
|Telecommunication Open APIs|6.0.9|2025-12-11|
|Telecommunications, Media and Technology - Advanced|1.0.11|2026-09-10|
|Telecommunications, Media and Technology - Foundation|1.0.13|2026-09-10|
|Telecommunications, Media and Technology - Prime|1.0.11|2026-09-10|
|Telecommunications Advanced|2.3.1|2026-09-10|
|Telecommunications Alarm Management Open API|7.0.1|2025-12-11|
|Telecommunications Foundation|2.3.1|2026-09-10|
|Telecommunications Prime|2.3.1|2026-09-10|
|Telecom Service Operations Core|1.2.1|2025-12-11|
|telemetry-data-connector|2.1.0|2026-08-07|
|Territory Planning|30.0.3|2026-03-12|
|Test Generation|4.0.11|2025-12-11|
|Theme Builder|6.1.5|2026-01-22|
|Theme Builder AI|1.1.0|2026-05-05|
|Third-party Risk Due Diligence|23.0.5|2026-09-10|
|Third-party Risk Management|23.0.7|2026-09-10|
|Third-party Risk Management Advanced|23.0.3|2026-09-10|
|Third-party Risk Management Professional Plus|23.0.3|2026-09-10|
|Threat and alert data feeds for Crisis Management|12.0.1|2026-09-10|
|Threat Intelligence|13.4.4|2026-02-05|
|Threat Intelligence Security Center - Advanced|3.3.1|2026-09-10|
|Threat Intelligence Security Center for Security Operations|4.8.1|2026-09-10|
|Threat Intelligence Security Center integration with CrowdStrike Intelligence|3.0.4|2025-03-12|
|Threat Intelligence Security Center integration with Elasticsearch|3.0.4|2025-05-01|
|Threat Intelligence Security Center integration with Microsoft Defender for Endpoint|1.0.4|2025-06-05|
|Threat Intelligence Security Center Integration with Palo Alto Networks NGFW|2.0.1|2025-03-12|
|Threat Intelligence Security Center integration with Shodan|1.0.7|2025-05-01|
|Threat Intelligence Security Center integration with Splunk Search|3.0.5|2025-03-12|
|Threat Intelligence Security Center integration with VirusTotal|3.0.3|2025-03-12|
|Threat Intelligence Security Center integration with WHOIS|5.0.4|2025-03-12|
|Threat Intelligence Support Common|13.8.0|2026-09-10|
|Threat Intelligence Support Common UI Components|1.1.4|2025-12-11|
|Timeline component|29.0.0|2026-03-12|
|Time Off Request App Template|28.2.1|2025-12-11|
|TNI - Advanced|2.3.0|2026-09-10|
|TNI - Advanced|2.3.0|2026-09-10|
|TNI and DCNAM AI Content Collection|2.3.0|2026-09-10|
|TNI and DCNAM AI Content Collection|2.3.0|2026-09-10|
|Total Cost of Ownership|1.1.0|2026-06-16|
|Touchpoint Meeting|3.0.7|2026-08-07|
|Touchpoint Meeting|3.0.7|2026-08-07|
|Transporter|2.3.29|2026-08-07|
|Trello Spoke|1.4.0|2025-11-06|
|Triggers|29.0.2|2026-03-12|
|TSOM - Advanced|2.3.0|2026-09-10|
|TSOM - Prime|2.3.0|2026-09-10|
|Twilio Spoke|1.2.0|2023-02-02|
|UCF Spoke|1.1.0|2023-05-04|
|Udemy Spoke|1.0.2|2022-12-01|
|UI Builder|29.1.52|2026-03-12|
|UI Components for Customer Portals|4.2.1|2026-08-07|
|UI Components of Collaboration for Configurable Workspaces|9.4.2|2026-09-10|
|UI Generation|29.2.5|2026-05-05|
|UiPath Spoke|2.5.1|2025-11-06|
|UI shared library|1.6.2|2026-06-16|
|UKG Spoke|3.5.0|2025-12-11|
|Unified Content Management|23.0.5|2026-09-10|
|Unified Developer Core|30.1.0|2026-09-10|
|Unified Security Exposure Management \(USEM\) - Advanced|2.2.3|2026-08-07|
|Unified Security Exposure Management \(USEM\) - Advanced|2.2.3|2026-08-07|
|Unified Security Exposure Management \(USEM\) - Foundation|2.2.3|2026-08-07|
|Unified Security Exposure Management \(USEM\) - Foundation|2.2.3|2026-08-07|
|Unified Security Exposure Management \(USEM\) - Prime|2.2.3|2026-08-07|
|Unified Security Exposure Management \(USEM\) - Prime|2.2.3|2026-08-07|
|Universal Request for Source-to-Pay Operations|1.2.2|2026-06-16|
|Universal Request integration with Microsoft Teams|1.0.2|2022-12-01|
|Universal Task|2.8.0|2026-06-16|
|Urjanet ESG integration|21.1.1|2025-12-11|
|Usage Insights Application|6.4.2|2026-09-10|
|Usage Insights Commons|6.4.2|2026-09-10|
|Usage Insights Commons Connected|6.4.2|2026-09-10|
|Usage Insights Funnel|6.1.12|2026-03-12|
|Usage Insights Funnel Core|6.4.2|2026-09-10|
|Usage Insights in Data Visualizations|6.4.2|2026-09-10|
|Usage Insights Pages|6.4.2|2026-09-10|
|Usage Insights Query Builder|6.4.2|2026-09-10|
|Usage Insights Query Builder Core|6.4.2|2026-09-10|
|Usage Insights Request Manager|6.4.2|2026-09-10|
|User Experience Analytics API|3.1.2|2024-02-01|
|User Experience Redirection|1.0.1|2026-03-12|
|User Sense|1.1.13|2025-12-11|
|Utility Actions Spoke|1.3.0|2024-10-03|
|UX Commons|27.0.2|2025-07-31|
|Vaccination Status|1.25.0|2025-12-11|
|Value dashboard for AI Control Tower|7.0.6|2026-09-10|
|Value Engine|7.0.6|2026-09-10|
|Value stream artifacts|2.3.0|2026-06-16|
|Vault Console|2.2.9|2026-08-07|
|Vendor Manager Workspace|3.5.0|2024-11-07|
|Vendor Risk Management integration with EcoVadis|21.1.1|2025-12-11|
|Verifi Spoke|1.0.0|2024-08-01|
|Virtual Agent Adapter Common|6.2.5|2026-06-16|
|Virtual Agent API|4.4.3|2026-09-10|
|Virtual Agent for PPM|1.0.1|2023-05-04|
|Virtual Agent for Source-to-Pay Operations|3.11.0|2025-07-31|
|Virtual Agent Topic Recommendations|4.5.5|2024-08-01|
|Virtual Machine Management for Virtual Agent|3.0.11|2023-08-03|
|Visa Spoke|2.2.2|2025-12-11|
|Visibility Content|6.32.2|2026-07-09|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice input for Now Assist|1.5.0|2026-07-09|
|Vonage Spoke|1.2.0|2025-12-11|
|Vulnerability Crisis Management|1.0.1|2024-08-01|
|Vulnerability Exposure Assessment|5.2.3|2025-12-11|
|Vulnerability Response|26.5.3|2026-01-20|
|Vulnerability Response Common|2.15.0|2026-01-20|
|Vulnerability Response Common Workspace|1.9.0|2026-01-20|
|Vulnerability Response Integration Framework|1.3.0|2026-01-20|
|Vulnerability Response Integration with Agile Management|1.2.2|2025-07-31|
|Vulnerability Response Integration with Atlassian Jira|1.0.4|2024-05-09|
|Vulnerability Response Integration with Black Duck|1.1.1|2025-12-11|
|Vulnerability Response Integration with CISA|1.5.1|2025-07-31|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Threat and Vulnerability Management|2.8.1|2025-12-11|
|Vulnerability Response Integration with NVD|1.7.2|2025-07-31|
|Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute|3.5.0|2025-12-11|
|Vulnerability Response Integration with Palo Alto Prisma Cloud|2.8.0|2025-12-11|
|Vulnerability Response Integration with Tenable|5.2.1|2025-12-11|
|Vulnerability Response Integration with Veracode|4.7.3|2025-12-11|
|Vulnerability Response Licensing and Usage|2.9.1|2026-01-20|
|Vulnerability Response Mobile|11.1.1|2023-05-04|
|Vulnerability Response Patch Orchestration|2.2.5|2025-05-01|
|Vulnerability Response Patch Orchestration with HCL Bigfix|1.3.0|2025-05-01|
|Vulnerability Response Patch Orchestration with Microsoft SCCM|2.3.1|2025-05-01|
|Vulnerability Solution Management|10.4.3|2022-12-01|
|Walk-up Experience for Service Operations Workspace|9.4.2|2026-09-10|
|Walk-Up for CSM|2.0.1|2026-03-12|
|Watershed integration for ESG|16.0.1|2023-02-02|
|WDF Tokenization|2.0.2|2025-12-11|
|WDF Unified Hub|1.1.0|2026-07-09|
|WebRTC Voice|1.0.7|2026-09-10|
|Whats New Framework Core|1.3.1|2026-03-12|
|WHOIS Integration for Security Operations|10.4.0|2024-08-01|
|Word Document Templates|1.9.7|2026-01-20|
|Workday ESG integration|21.1.1|2025-12-11|
|Workday Financials Spoke|2.1.0|2025-07-31|
|Workday HR Spoke|2.7.0|2025-12-11|
|Workday Learning Spoke|1.1.4|2024-04-04|
|Workflow Studio|29.2.2|2026-08-07|
|Workforce Optimization Common|1.7.0|2025-12-11|
|Workforce Optimization Configurable Workspace Core|1.11.0|2025-12-11|
|Workforce Optimization Configurable Workspace UI Components|4.4.1|2025-12-11|
|Workforce Optimization for CSM Configurable Workspace|4.5.0|2025-12-11|
|Workforce Optimization for HR|1.1.2|2025-07-31|
|Workforce Optimization integration with Microsoft Outlook|1.3.0|2025-12-11|
|Workfront Spoke|1.3.0|2025-11-06|
|Work Item Integrations Common|1.15.0|2026-06-16|
|Workplace Agent for mobile|1.4.5|2026-03-12|
|Workplace Case Management|1.28.8|2026-07-09|
|Workplace Central|1.16.5|2026-07-09|
|Workplace Concierge|1.7.11|2026-07-09|
|Workplace Connectors|2.3.8|2026-08-07|
|Workplace Core|2.28.10|2026-08-07|
|Workplace from Facebook Spoke|4.2.1|2025-11-06|
|Workplace Indoor Map Component|1.1.1|2024-08-01|
|Workplace Indoor Mapping|1.18.6|2026-07-09|
|Workplace Lease Administration|1.8.5|2026-07-09|
|Workplace Maintenance Management|1.11.5|2026-07-09|
|Workplace Move Management|1.14.5|2026-07-09|
|Workplace PPE Inventory Management|1.18.0|2025-07-31|
|Workplace Reservation Management|3.6.1|2026-08-07|
|Workplace Reservations for Microsoft Outlook Add-in|1.12.2|2025-07-31|
|Workplace Service Delivery Enterprise|1.6.0|2025-12-11|
|Workplace Service Delivery for Mobile|1.16.2|2025-12-11|
|Workplace Service Delivery integration with Microsoft Places|1.2.5|2025-12-11|
|Workplace Service Delivery Professional|1.4.0|2025-12-11|
|Workplace Service Delivery Suite|2.17.2|2025-12-11|
|Workplace Services Kiosk|1.5.2|2025-12-11|
|Workplace Space Management|1.20.13|2026-08-07|
|Workplace Space Mapping|1.20.5|2026-06-16|
|Workplace Stack Plan|1.5.12|2026-06-16|
|Workplace Visitor Management|2.1.1|2026-08-07|
|Work Progress Status for Agile Teams|1.0.4|2025-06-05|
|Work Progress Status for SAFe|1.0.4|2025-06-05|
|Workspace App Shell|29.1.1|2026-03-12|
|Workspace Builder for App Engine|28.2.0|2025-12-11|
|Workspace Inspector|20.1.1|2025-05-01|
|Workspace navigation and experience demo|27.1.1|2026-03-12|
|Wrike Spoke|1.3.0|2025-09-10|
|WSD - Advanced|1.0.2|2026-06-16|
|WSD - Foundation|1.0.2|2026-06-16|
|WSD - Prime|1.0.2|2026-06-16|
|X Spoke|2.3.0|2025-09-10|
|YouTube Spoke|1.0.5|2025-07-10|
|Zendesk Spoke|1.8.0|2025-11-06|
|Zero Copy Connector for ERP|10.0.9|2026-05-05|
|Zero Copy Connector Hub|3.0.1|2026-03-12|
|Zero Touch Service Desk|3.2.8|2026-09-18|
|Zoom extension for Omnichannel Callback|1.3.6|2025-07-31|
|Zoom Spoke|4.6.2|2026-01-20|

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/available-versions.md)


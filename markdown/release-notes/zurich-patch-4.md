---
title: Zurich Patch 4
description: The Zurich Patch 4 release contains important problem fixes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-12-05"
reading_time_minutes: 114
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 4

The Zurich Patch 4 release contains important problem fixes.

-   **Zurich Patch 4 was released on December 5, 2025.**
    -   Build date: 12-03-2025\_1405
    -   Build tag: glide-zurich-07-01-2025\_\_patch4-11-14-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z04.00.xlsx).

## Overview

Zurich Patch 4 includes 476 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-zp4.png "Top 10 problem categories")

## Security-related fixes

Zurich Patch 4 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 4, refer to [KB2649723](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2649723).

## Changes in Zurich Patch 4

-   **[Sensitive data filters](https://www.servicenow.com/docs/access?context=sensitive-data-filters&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    The Discovery Sensitive Data Filters \[discovery\_sensitive\_data\_filter\] table provides a way to help prevent sensitive information from being exposed in the Configuration Management Database \(CMDB\) by applying redaction rules during data collection.

-   **[Managing Now Assist applications through Now Assist suites](https://www.servicenow.com/docs/access?context=now-assist-app-mgr&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**
-   **[Show borders between search result cards in portal search](https://www.servicenow.com/docs/access?context=show-borders-search-result-cards-portal-search&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)**

    Display borders between search result cards on the search results page for portal search applications.

-   **[Time-based one-time password \(TOTP\) authentication](https://www.servicenow.com/docs/access?context=totp-authenticator-apps&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    A time based one-time password \(TOTP\) is a secure authentication factor that verifies user identity by generating a unique, time-sensitive code.

-   **[Push notification - Okta Verify](https://www.servicenow.com/docs/access?context=push-notification-okta-verify&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    The **Okta Verify** app push notification enables users to securely approve authentication requests directly on their enrolled mobile devices.

-   **[SoftPIN authentication](https://www.servicenow.com/docs/access?context=softpin-authentication&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**
-   **[SMS One-time passcode \(OTP\) authentication](https://www.servicenow.com/docs/access?context=sms-otp-authentication&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**
-   **[Granular admin roles required to secure your instance](https://www.servicenow.com/docs/access?context=roles-within-platform-security&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    Verify proper access management by assigning roles that define user permissions and responsibilities. By doing so, organizations can maintain security, enforce conformance, and optimize their operations effectively.


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

Access Control

 PRB1902529

</td><td>

Auto-assignment feature is not working as expected

</td><td>

The auto-provisioning status displayed in the UI does not accurately reflect the current values defined in the sys\_properties \(glide.security.scripting\_role.auto\_provisioning\) table. Changes made to the relevant sys\_properties are not being propagated or updated in the UI as expected.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1952366

</td><td>

The 'Physical Table Stats Gatherer' job generates thousands of errors in the syslog

</td><td>

The following errors are logged in the syslog when the Physical Stats Gatherer job runs: Four entries are logged for each table which doesn't have peripherals attached to it, and one entry is logged per table that doesn't have stats collected by an SNC job.

</td><td>

1.  Make sure the SNC SDU job is running on the instance.
2.  Check the StatsGatherer execution for the day.
3.  Open syslog\_list.do
4.  Filter logs for message starting with: DATA MANAGEMENT TABLE STATS Gatherer.

 Observe the errors in the logs.

</td></tr><tr><td>

Encryption

 PRB1931988

 [KB2481838](https://hi.service-now.com/kb_view.do?sysparm_article=KB2481838)

</td><td>

A data migration job fails when there are no context keys and EFC's in the migration\_pending state

</td><td>

The job state changes to 'Error', with the following summary: 'Error creating job handler for type all\_data\_to\_kmf: \[The KMF cryptographic module to encryption context relationship table is empty. The 'Migrate Key Context to Module' job might not have been run or has failed.\].'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Memory: Heap Space

 PRB1636231

</td><td>

Memory exhausted by the Archiver Job Consumer due to syslog records stored in memory, and syslog\_awa is not configured as a rotated table

</td><td>

Memory exhausted by the Archiver Job Consumer reparenting records from syslog table due to a problem observed when syslog\_awa, which is a child table of syslog, is created without table rotation. The archiver job reparents records for the archive rules it triggers for, and will reparent a table that's not rotated. When syslog\_awa isn't configured as a rotated table, the reparenting process will execute on it and its parent table syslog. Query to syslog shards are then observed, and memory is consumed as the records on these shards are stored into memory. Due to the size of it, it will cause memory to become depleted. When the archiver job is running, the localhost logs will have a large query to a syslog shard where the function reparentDocumentIDRecords is running.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1954123

 [KB2594708](https://hi.service-now.com/kb_view.do?sysparm_article=KB2594708)

</td><td>

Mutual TLS \(mTLS\) is enabled on Zurich instances, causing access issues for inbound integrations

</td><td>

Due to the updates related to the Predictive Intelligence plugin, mutual TLS \(mTLS\) is enabled after a Zurich upgrade. This may result in instance access issues for inbound integrations.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog

 PRB1919964

 [KB2532880](https://hi.service-now.com/kb_view.do?sysparm_article=KB2532880)

</td><td>

The record producer **Submit** UI action should be grayed out after being hit once

</td><td>

On a catalog item in service portal, the **Submit** button re-enables after first selection.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1947987

</td><td>

CSM/FSM Workspace list filter changes when opening and closing a record

</td><td>

When opening a record through the list in the CSM/FSM Configurable Workspace, the list's filter is modified after closing the record.

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

 PRB1960686

</td><td>

Updates to who can execute Agentic Assets on AI - Access Analyzer

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1928286

</td><td>

Typed text in email reply editor disappears after selecting Reply again

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Navigate to CSM and open any incident record.
3.  Make sure there is an email entry in the AS.
4.  Select **Reply** on the email.
5.  Type some content in the email reply editor.
6.  Select **Reply** again on the same email.

 Notice that the text disappears.

</td></tr><tr><td>

Activity Stream

 PRB1928872

</td><td>

The CanReadRepo class encounters a ConcurrentModificationException

</td><td>

This concurrency issue arises because the class uses a HashMap, which is not thread-safe. The HashMap should be replaced with a ConcurrentHashMap to ensure thread-safe operations and prevent the exception.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1938976

</td><td>

ACLs prevent system administrators from running GlideActivity scriptable methods

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1947683

 [KB2631388](https://hi.service-now.com/kb_view.do?sysparm_article=KB2631388)

</td><td>

Activity Stream caches excessive records, causing sys\_activity table growth and performance degradation

</td><td>

Instead of caching only viewed entries, the platform may proactively cache all work notes and events generated on monitored tables, including those that are never accessed through the UI. This behavior results in rapid growth of the sys\_activity table, sometimes reaching tens or hundreds of millions of records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1933671

</td><td>

AWA \(Advanced Work Assignment\) uses the system locale timezone when writing to logs

</td><td>

The AWAEventUtil code changes the global locale setting, causing the 'localhost log' to be written in UTC rather than PST \(standard\).

</td><td>

1.  Log in to an instance.
2.  Install the Advanced Work Assignment \(AWA\) plugin.
3.  Navigate to **Advanced Work Assignment** &gt; **Service Channels** &gt; **New**.
4.  Enter the following values:
    1.  Name: test
    2.  Index order: 100
    3.  Table: Incident
    4.  Utilization condition: Short Description is not empty
5.  Submit it.
6.  Ensure that the channel is active.
7.  Create a new queue.
8.  Open the record created in step 3.
9.  Choose the 'Queue' related list.
10. Create a new 'Queue' record.
11. Enter in all the mandatory fields.
12. Submit it.
13. Enable Logging.
14. Open the record created in step 3.
15. Select **Queues**and **New**.
16. Name it 'test-queue'.
17. Submit it.
18. Check the localhost log.
19. Have the terminal open for all the nodes.
20. Tail the localhost log.
21. Navigate to **Incident** &gt; **Create New**.
22. Enter in something.
23. Submit it.

 Observe that the timestamp zone has changed, and some lines are in the previous timezone and others are in UTC.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1935541

</td><td>

Work item incorrectly moved to cancelled state instead of queued state

</td><td>

Without external routing, the rejected work item should move to the queued state. Instead, the work item moves to the cancelled state, and the interaction moves to closed\_abandoned.

</td><td>

1.  Change mweb sys\_cs\_channel to type 'Messaging'.
2.  Enable external routing for 'Chat - Asynchronous' Channel.
3.  Mark Chat Async Queue 'external' as true.
4.  Make two external agents available in workspace
5.  As a system admin, start a chat in the SP/CSM portal.

Once routing to live agent starts, a new work item is created.

6.  Assign the work item to the first agent using manual assignment API via REST API explorer.
7.  Change the first agent presence to offline.
8.  Send a message from admin.

The conversation is reassigned, which moves the interaction state to New and creates a new work item.

9.  Assign the new work item to the second agent using manual assignment API via REST API explorer.
10. Reject the work item.

 Expected Behavior: Without external routing, the work item is moved to the queued state, looking for new agent.

 Actual Behavior: The new work item moves to the cancelled state, and the interaction moves to closed\_abandoned.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1950558

</td><td>

Advanced Work Assignment \(AWA\) should be able to determine if the work item is rejected due to time out or Asynchronous Message Bus \(AMB\) disconnection

</td><td>

When the work item times out, the work item reason on the awa\_work\_item\_rejection table is 'Timed out' instead of 'AMB connection lost'.

</td><td>

1.  Install the Agent Chat plugin with the demo data.
2.  Open the AWA assignment rule.
3.  Update the timeout time to 15 seconds.
4.  Open a browser \(browser 1\).
5.  Log in to the workspace as an agent in browser 1.
6.  Open another browser \(browser 2\).
7.  Log in to the instance as a requestor.
8.  Open the URL $sn-va-web-client-app.do in browser 2.
9.  In browser 1, close the workspace tab completely as an agent.

Notice that the agent presence will not be set to offline immediately because the default idle check gives a 5 min buffer, and the agent is still available to receive work item at the moment.

10. In browser 2, start the live agent handoff.
11. Wait for 15 seconds so the work item will be timed out.
12. As an admin, navigate to the awa\_work\_item\_rejection table.
13. Check the rejection record for the previous interaction.

 Expected behavior: The reason should be 'AMB connection lost'.

 Actual behavior: The rejection reason is 'Timed out'.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1955936

</td><td>

The user is unable to route chats landing on external queues if agents are available on a different domain

</td><td>

The requester gets a 'No agents available' message even though there is an agent available.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1943902

</td><td>

Create a new exclusive channel to receive work items on Agent Chat

</td><td>

The inbox component should subscribe to a new Asynchronous Message Bus \(AMB\) channel other than the existing AWA/work\_item channel to reduce the chance of being interfered with by other components subscribing to the same channel. The AMB publish function used in the workItemResponder should be updated to take the trace id.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1957261

</td><td>

Invoke End Chat Summarization in 'system' topic

</td><td>

The short description and chat summary are not populated.

</td><td>

1.  Remove 'sn\_hr\_core.admin' role from the 'admin' role.
2.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** &gt; **Employee** &gt; **HRSD**.
3.  Open the 'Chat summarization' skill and activate it.
4.  Log in as an HR agent in one window and an end user in another.
5.  Connect to a live agent as an end user.
6.  Accept the chat as HR agent and have some conversation.
7.  Select the **End chat** action.

 Notice that the short description and chat summary are not populated.

</td></tr><tr><td>

Agent Chat

 PRB1959396

</td><td>

AWA workitemResponder onChange published message causes a work item card to disappear in the workspace

</td><td>

Work items disappear from the inbox even though they are still pending for acceptance.

</td><td>

1.  Log in to one browser as an agent.
2.  Have multiple sessions as the requester and start chatting with the agent.

In the agent browser, observe multiple work items pending for accept in the inbox.

3.  Navigate to the awa\_work\_item table and update one of the pending accept work item.

 Expect behavior: The agent receives an AMB message about the updated work item, but all the pending accept work items remain the same.

 Actual behavior: All the other work items disappear from the inbox even though they are still pending for acceptance. Only the one that was just updated remains in the inbox.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1949415

</td><td>

The toolID and agentID aren't passed to 'processing message' with the latest 6.0.2 snapshot

</td><td>

Due to issues with the latest AIA snapshot build, all the previous workflows stop working. Previously, users were able to see the toolID and ageintId inside the processing message, but with the latest, it's gone.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1949779

</td><td>

Update the memory format of conversation history passed to Unified Planner

</td><td>

Updates to the format of the unified planner memory with keys.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1951062

</td><td>

HTML content does not render in NAP or NAVA

</td><td>

The output is incorrectly formatted.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1951148

</td><td>

AI Agents are not responding when executed from Now Assist panel \(NAP\) and AIEL

</td><td>

The agent greeting is no longer displayed, and the execution ends without any response in NAP and AIEL.

</td><td>

1.  Open an instance.
2.  Open the browser console.
3.  Run the command.

 Notice that in the sys\_generative\_ai\_log table, the agent is executed and the model has the response also populated, but NAP doesn't display an output and the Agent execution ended.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1952331

</td><td>

The user can see additional messages in response from an agent

</td><td>

 

</td><td>

1.  Navigate to AI agent studio.
2.  Select **Workflow**.
3.  Send Text - SMS Abel to pick up laptop.

 The user can see additional message is returned in response.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1952442

</td><td>

Java tool execution doesn't send the is\_abort flag.

</td><td>

The execution of tools involving outbound is in sync mode.

</td><td>

1.  Set up AI Agents.
2.  Execute any agent with the tool that has to send a request to the outbound.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1953439

</td><td>

Crud tool doesn't work with java

</td><td>

'Lookup' fails with java.lang.SecurityException: Illegal access to method forEach\(function\) in class java.util.ArrayList. Also, 'Create' doesn't load user defined parameters\(short\_description\) on the incident record.

</td><td>

Have an AI Agent with tools for the crud operations 'Create' and 'Lookup'.

 Expected behavior: 'Lookup' queries and shows up successfully. 'Create' creates a record as per user inputs.

 Actual behavior: 'Lookup' fails with java.lang.SecurityException: Illegal access to method forEach\(function\) in class java.util.ArrayList. Also, 'Create' doesn't load user defined parameters\(short\_description\) on the incident record.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1953687

</td><td>

Datastream action based tools aren't working from the JAVA layer

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1953697

</td><td>

Sys\_meta\_graph is an internal table and shouldn't be queried outside KG

</td><td>

KG doesn't work if the sys\_meta\_graph table \(an internal KG table\) is queried directly. The exposed KG API should be used to get the schema details instead.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1955511

</td><td>

The Categorize ITSM incident is not working with AI Agents \(AIA\) 6.0.6 snapshot

</td><td>

The Categorize ITSM incident AI agent results in an execution stuck in the playground.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1955807

</td><td>

Add memory restructuring changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1956483

</td><td>

Flow actions with an error evaluation step don't propagate the error message when executed through JAVA

</td><td>

The routing does not occur as expected.

</td><td>

1.  Open the Playground and start testing Demo Next Best Action agent.
2.  Attempt to route the 'Get Similar Incidents' tool.
3.  Verify the execution log, verify the AIA Step Log.

 Observe that the routing does not occur as expected.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1957318

</td><td>

Global Graph doesn't work

</td><td>

Global Graph fails during Java layer execution. It throws an error: Error occurred while executing request validator: Cannot read property 'pre\_process\_details' from undefined\).

</td><td>

1.  Select the agent 'Get Workflow Details' configured with Global Graph and tag as use case \(sn\_aia\_use\_case\).
2.  Trigger the agent with the task 'Get details of workflow Classify tasks'.

 Observe that the Global Graph is not working and returns the error: 'Requested information not found'. And received the following error while testing from KG Designer: 'The current operation ended in state: ERROR. Detail: Cannot execute internal HTTP request. Request is not authorized.- 400001'

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1957377

</td><td>

Reduce escape characters in tool outputs in the conversation history for the Unified Planner prompt

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1957731

</td><td>

The Now Assist panel shows incorrectly formatted output from the AI Agent

</td><td>

 

</td><td>

1.  Open the sys\_atf\_test\_result page for an unsuccessful ATF test.
2.  Select the **Triage test failure** button.
3.  Check the output in the Now Assist Panel after the AI Agent response is available.

 Expected behavior: The output is properly formatted.

 Actual behavior: The output isn't properly formatted.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1958672

</td><td>

Tool processing messages are not correct for JAVA Tool Executor

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1958762

</td><td>

Subflow is not triggered for Agentic AI workflow

</td><td>

Support role masking for all the existing AI agents and workflows. Internal play records are not created after selecting any option in the Support Renewals Expansion, and the 'Get to green play sunflow' is not triggered.

</td><td>

1.  Create glide.
2.  Install the recent plan.
3.  Navigate to **Support Renewals Expansion**.
4.  Run the Agentic Workflow.
5.  Select any option.

 Expected behavior: After selecting any option, internal play records should be created successfully.

 Actual behavior: After selecting any option, internal play records are not created.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959252

</td><td>

Apply role masking to user permissions to terminate execution and send error notifications when downstream ACLs fail

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959456

</td><td>

Add ToolExecution response to memory

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959458

</td><td>

Action-type tool support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959460

</td><td>

Add support to run tools in parallel

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959461

</td><td>

AIA Tool Executor JAVA and parallel tool execution

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959463

</td><td>

KG and record lookup-type tool support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959465

</td><td>

CRUD-type tools support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959467

</td><td>

RAG-type tool support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959469

</td><td>

Add support for impersonation and session domain ensuring when handling AsyncToolMessage

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959472

</td><td>

Agentic KG Graph should use the Virtual Agent context and shouldn't query separately

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959474

</td><td>

Subflow-type tool support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959476

</td><td>

Skill-type tool support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959477

</td><td>

ReAct topic migration to the Java layer

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959478

</td><td>

Add RunAsUser impersonation support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959479

</td><td>

Add support for custom post-processing of a response

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959480

</td><td>

Add support to Store toolResponse to variableStore

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959481

</td><td>

Add support for tool deterministic input mapping

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959482

</td><td>

Java implementation of fully agentic VA for handling executionTask

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959483

</td><td>

Output refiner implementation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959484

</td><td>

Canvas message display and tool output display support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959485

</td><td>

Add support for pojos and state handling framework for AIA tool executor JAVA changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959486

</td><td>

Framework and design for Toll Executor

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959487

</td><td>

The 'React' topic changes to support Java tool execution

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1959671

</td><td>

Web Search as a tool doesn't work

</td><td>

There are issues with FDIH Tool mandatory input validation and reference type input handling, which cause execution to get stuck.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1960134

</td><td>

Resume conversations once the MCP response is received

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1961342

</td><td>

AI Agent orchestrator retries tools and agents even when it hits a guardrail

</td><td>

 

</td><td>

1.  Turn on Guardian for AI Agents.
2.  Execute the HR tuition reimbursement agent with a prompt injection.

 Notice that the the agent memory it keeps the past guardrail failure.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1963825

</td><td>

Update AI Agents \(AIA\) true-up version to 4.0.38

</td><td>

Updating the AIA true-up version to fix a potential infinite loop in an upgrade scenario.

</td><td>

 

</td></tr><tr><td>

AI Gateway - Security

 PRB1960673

</td><td>

AI Gateway \(also known as the Agentic Workflow Hub\) feature

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1913578

</td><td>

Search sources are inadvertently deleted when the indexed source is missing

</td><td>

The search source entry should remain in place. Any search profile using the search source should continue to function without throwing any error that stops the search. However, the search source entry is automatically deleted when the cleanup job runs if the underlying source is no longer accessible.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1944944

</td><td>

RAG corrupted AIS results send back the wrong sys\_id and text in results

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1953364

</td><td>

Users without permissions find truncated/dropped results and the **ext\_content\_none\_access** field is set to 'true'

</td><td>

This issue was found with AI Search version 104.0.0.9.

</td><td>

1.  Add two users to the glide instance.
2.  Use External Content Connector for SharePoint Online.
3.  Restrict crawling to a Sharepoint URLs.
4.  Start a Full document crawl.
5.  Start a User mapping crawl.
6.  Wait for the completion of both crawls.

 Expected behavior: The active user can find all documents from the site, but the deactivated user can find no documents from the site and has not been mapped.

 Actual behavior: The deactivated user is not mapped, but searching as that user returns documents that shouldn't be returned.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1954111

</td><td>

In RegressionSolutionStore, add support for enabling/disabling deprecation and setting minimum records required

</td><td>

RegressionSolutionStore currently uses a sys property to manage deprecation and minimum records required for training. Support should be added for enabling or disabling deprecation and setting minimum records required for training without relying on a sys property.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1958643

</td><td>

Search with late binding should have an additional max number of rows requested buffer 100

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1967477

</td><td>

When no Virtual Agent app is enabled, Global search with AIS enabled fails

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search for Virtual Agent

 PRB1953578

</td><td>

Pass limitColumnOutput param in apiOptions for t2r call

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1935078

</td><td>

Make the border for the Search Result card configurable

</td><td>

There are no borders for the Search Result card.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1952630

</td><td>

Malformed URLs in the streaming chunks for a synthesized response cause the UI to hang

</td><td>

The URL renders stand-alone and sometimes isn't selectable.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1961267

</td><td>

Ask-a-follow up and request in chat doesn't work on global search

</td><td>

A follow-up question is not asked and there is no Request in chat option available.

</td><td>

1.  Enable NAP on global search.
2.  Search for 'Apple Watch' or 'Loaner Laptop' \(any conversational catalog query\).

 Notice that a follow-up question is not asked. Also, when the user selects Catalog citation, notice there is no Request in chat option available.

</td></tr><tr><td>

AI Search UX

 PRB1961619

</td><td>

Synthesized response is not displaying on portal search with DW set-up

</td><td>

Only conventional list of search results is obtained when the Now Assist widget disappears.

</td><td>

1.  Log in to the instance as an admin.
2.  Open /csm.
3.  On homepage, search 'homepage errors'.

 Expected behavior: Synthesized response is displayed successfully at the top along with the list of search results.

 Actual behavior: Now Assist widget loads for a moment and then disappears, but the conversational list of search results remain.

</td></tr><tr><td>

Analytics Data API

 PRB1894963

</td><td>

Data Visualization drilldown doesn't follow previous filters

</td><td>

On Data Visualization, only the first-level drilldown honors the selected filters. This issue was observed in Xanadu and Yokohama.

</td><td>

1.  Navigate to an instance.
2.  Open a Data Visualization.
3.  Select a column.

Notice that it contains a drilldown.

4.  Select another column.

Notice that it contains a drilldown with a daily view.


 Observe that only the first-level drilldown honors the selected filters, and that subsequent drilldowns \(level 2 and beyond\) reset to the original selection context, rather than chaining the filters from the intermediate drilldown.

</td></tr><tr><td>

Analytics Data API

 PRB1921406

</td><td>

POST /api/now/charts/data returns 500 status code when the table is not valid

</td><td>

POST /api/now/charts/data should return the 400 HTTP status code, with the error message 'Table is not valid: null.' Instead, it returns the 500 HTTP status code.

</td><td>

 

</td></tr><tr><td>

App Engine Studio - Family Channel

 PRB1923756

</td><td>

The Record Producer remains as the original template's one in a newly created app

</td><td>

When using the AES Template, the Record Producer remains as the original template's one, but it should be the one in the new app.

</td><td>

1.  Create an app \(App1\).
2.  Create a new table in App1.
3.  Create a Record Producer with the table.
4.  Create a flow with the action **Get Catalog Variables**.
5.  Set the Record Producer in it.
6.  Save.
7.  Create a template with App1.
8.  Create a new app \(App2\) with the template.
9.  Check the Record Producer that was set in the action **Get Catalog Variables**.

 Expected behavior: The Record Producer is the one in the new app \(App2\).

 Actual behavior: The Record Producer is the one in the original app \(App1\).

</td></tr><tr><td>

Application Install Engine

 PRB1956758

</td><td>

Add support for needs of Golden Configuration in Install Engine

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1942235

</td><td>

When running UpdateChecker script in background or 'Sync Now' as an admin user, the error appears: 'User Not Authenticated - Required to provide Auth information'

</td><td>

Golden Configs should be in the appstore instance so they can sync to the App Manager.

</td><td>

1.  Ensure there are Golden Configs in the appstore instance to sync to the App Manager.
2.  Navigate to **App manager** on a datacenter instance as an admin.
3.  Select **Sync Now**.

Notice that the sync occurs and it shows an updated timestamp.

4.  Attempt to search for any app which is part of the Golden Config.

Notice that it is not showing the Suite Config option.

5.  Navigate to the **sys\_suite\_config** table.Notice that no new record exists.
6.  Attempt to try to run the script in background in the global scope - new sn\_appclient.UpdateChecker\(\).checkAvailableUpdates\(\);.
7.  Navigate to the **syslog** table.

Notice that it shows an error message, 'Error: Golden-Config sync: User Not Authenticated - Required to provide Auth information \(sys\_script\_include.46e8ba01eb002100d4360c505206fec3.script; line 257\)'.


 Expected behavior: When the admin user uses **Sync now** or runs a script in background, it should pull latest Golden configs available.

 Actual behavior: It is not pulling Golden Configs.

</td></tr><tr><td>

Application Manager

 PRB1956757

</td><td>

App manager changes in Golden Configuration

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1956759

</td><td>

An app manager install pop-up should display instructions to sign new company-level terms and conditions in Store

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1956771

</td><td>

For on-premise users, apps are not created in the sys\_remote\_app table after they're added to the cache

</td><td>

 

</td><td>

1.  Add an app to an offline table.
2.  Run update checker with the cache enabled.

 Observe that the app is not moved to the remote table. The test checks for an app in the remote table and fails.

</td></tr><tr><td>

Application Rationalization

 PRB1898811

</td><td>

Remove functionality doesn't work for architectural artifact related lists

</td><td>

Architectural artifacts can't be removed for Digital integration, Digital interface, TRM Product, and Business Process Lists.

</td><td>

1.  Log in as an APM user.
2.  Navigate to **Enterprise Architecture Workspace** &gt; **Portfolio** &gt; **Business process/Digital integration/Digital interface/TRM Product**.
3.  Add an architectural artifact.
4.  Select and remove the artifact.

 Expected behavior: The linked artifact is removed.

 Actual behavior: The linked artifact is not removed.

</td></tr><tr><td>

Application Rationalization

 PRB1961778

</td><td>

The info icon doesn't work properly with filters

</td><td>

The overall score for a business application is missing in the Application Rationalization grid and in the size drop-down list in bubble settings.

</td><td>

1.  Apply a filter \(BC - Leaf node is false\).
2.  Select the **Info** icon.

Attendance management BA is shown on the side panel, which is expected.

3.  Apply an indicator score filter \(overscore is empty\).
4.  Select the **Info** icon.

Observe that attendance management BA is still shown on side panel, and the first record in the grid isn't expected.

5.  Select a BA bubble in the Bubbles page.
6.  Open the side panel.
7.  Navigate to the List page.
8.  Return to the Bubbles page.

Observe that the side panel BA information disappears from the Bubbles page.

9.  Scroll inside the Info panel.
10. Select another BA.

 Observe that the Info panel opens at the previously scrolled position instead of resetting to the top.

</td></tr><tr><td>

Asset Management

 PRB1947295

 [KB2570280](https://hi.service-now.com/kb_view.do?sysparm_article=KB2570280)

</td><td>

Error while creating an asset when populating a serial number

</td><td>

Notice the error message 'onChange script error: TypeError: Cannot read properties of undefined.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Asset Management

 PRB1961195

</td><td>

The Procurement Receive function doesn't open the camera in the Agent app

</td><td>

A blank page opens.

</td><td>

1.  Open Now Agent App in mobile.
2.  Navigate to **Procurement**.
3.  Open POs next 30 days.
4.  Select a PO in the 'Ordered' state.
5.  Navigate to **Related List**.
6.  Open PO Line Items.
7.  Open an ordered PO Line Item.
8.  Select **Receive**.

 Notice that a blank page opens up.

</td></tr><tr><td>

Authentication

 PRB1936797

</td><td>

The SMS Twilio OTP message is broken

</td><td>

It should say 'Send from your Twilio trial account - Your 6-digit verification code is XXXXXX, it expires in 5 minutes. Enter the code to complete the authentication. Thank you.' Instead, it says 'Send from your Twilio trial account- Multifactor.OTPMessage'.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1943178

</td><td>

OAuth JWT Token Refresh token flow doesn't work for public client

</td><td>

OAuthTokenProcessor\#isPKCERequest should return 'true' for the JWT refresh\_token with the client ID with 'public client' checked.

</td><td>

1.  Get the OAuth client.
2.  Set the public client to 'true'.
3.  Set the token format to JWT.
4.  Get the access token or refresh the token using auth PKCE.
5.  Send the refresh\_token grant request.

 Notice that it's 401, when it should be 200.

</td></tr><tr><td>

Authentication

 PRB1960578

</td><td>

Knowledge base as Authentication Factor for Voice Agents

</td><td>

This is a product upgrade.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1960579

</td><td>

Softpin as Authentication Factor for \[Voice Agents

</td><td>

This is a product upgrade.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1960580

</td><td>

Authentication for Voice Agents

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1960581

</td><td>

Create an API to get an access token for a voice agent

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1941169

</td><td>

ATF reusable test input/output variables do not have a default form layout

</td><td>

After navigating to atf\_input\_variable\_callable.do or atf\_output\_variable\_callable.do, new form layout records are generated.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1943666

 [KB2563247](https://hi.service-now.com/kb_view.do?sysparm_article=KB2563247)

</td><td>

The ATF Page Inspector component list is empty on Portal pages with AIS enabled

</td><td>

On normal Portal pages, document.getElementById\('testFrame'\).contentWindow.uxf is not defined. When AI Search is enabled, the UX framework gets attached to the page and the PageInspector's getUxf\(\) test passes, switching the interface to Configurable Workspace mode. However, ATF mode is not enabled and no CWS components are returned by the function, so the component list is empty.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1948863

</td><td>

ATF tests with metadata tracing enabled can cause out-of-memory errors

</td><td>

Starting in the Zurich release, the ATF has the ability to trace metadata records \(business rules, script includes, etc.\) that are invoked as part of a test execution. However, this has been found to be a highly memory-intensive operation that can sometimes cause performance degradations, and in the most extreme cases, node restarts.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1951016

 [KB2579637](https://hi.service-now.com/kb_view.do?sysparm_article=KB2579637)

</td><td>

All steps in Automated Test Framework \(ATF\) pass a test, but UI tests with many console logs fail

</td><td>

This issue specifically occurs when any single UI batch in an ATF test produces more than 1 megabyte worth of console logs \(approximately 500,000 characters worth of data\).

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1956762

</td><td>

Automated Test Framework \(ATF\) Assist global utilities on the Glide-side

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1959359

</td><td>

Clean Up job for Metadata tracing OOMemory Issue

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1959362

</td><td>

zz\_all\_terms\_cache\_yy flush causes delays in test runs

</td><td>

Building a cache before and after test run takes two to four minutes.

</td><td>

 

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1946628

</td><td>

Capacity performance upgrade for appointment booking

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1955343

</td><td>

Demand Channel population inconsistencies on WOT

</td><td>

Demand Channel doesn't populate on Work Order Task in a Pending Dispatch state. However, the Demand Channel remains empty and is not being populated.

</td><td>

Create a Work Order Task and move it to the Pending Dispatch state.

 Notice that the Scheduled Start is no longer auto-populated on the WOT. The task only has Window Start set.

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1959636

</td><td>

Current query doesn't filter capacity types while fetching the aggregated agent schedule cutoff

</td><td>

When the capacity\_by is something other than aggregated agent schedule, there's no need to populate the max date while preparing the capacity event body.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1899267

</td><td>

Scope mastering should be enabled for sysapproval\_approver

</td><td>

An admin user without HR roles can see the email associated with an HR approval.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1951520

</td><td>

RCAs to support the 'HR case' table as input in NASK

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1954808

</td><td>

Unable to create articles with the 'Human Resources General Knowledge' KB

</td><td>

The user can't create articles with the 'Human Resources General Knowledge' KB because restricted caller access isn't allowed.

</td><td>

1.  Log in to a Zurich instance.
2.  Enable the KB generation skill for HRSD
3.  Add some role under ACL for defining access.
4.  Navigate to **AI Agent Studio** &gt; **Testing**.
5.  Select **KB Content Creation AI Agent**.
6.  Give the following prompt: 'Create a knowledge article for HR Case Number'. \(Make sure to give a closed case with no attached articles.\)
7.  When prompted for the knowledge base, select **Human Resources General Knowledge**.

Notice that the flow errors out, saying: 'An attempt to generate the knowledge article encountered an error: An error occurred while inserting the knowledge article'. This error is not seen if the user selects any knowledge base other than 'Human Resources General Knowledge'.

8.  Open the sys\_restricted\_caller\_access table.
9.  Search for a record that needs to be approved for the above flow to pass.
10. Manually approve the record.

 Observe that the KB creation is successful for the HR knowledge base.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1955464

</td><td>

Sentiment analysis is not determined for ER cases

</td><td>

 

</td><td>

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Skills** &gt; **Employee** &gt; **HRSD**.
2.  Open the 'Sentiment Analysis for HR Case' skill and activate it.
3.  Open 'HR Agent Workspace'.
4.  Open any ER case.

 Expected behavior: Sentiment is determined.Actual behavior: Sentiment is not determined.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1956191

</td><td>

RCA records for attachment summarization

</td><td>

 

</td><td>

Ship RCA records for attachment summarization after new changes.

</td></tr><tr><td>

Case Management

 PRB1926739

</td><td>

The user is not able to access an overview link from a customer service module

</td><td>

The user observes the message 'The dashboard was not found.'

</td><td>

1.  Log in with system admin user access to platform.
2.  Select the app navigation menu and search for customer service.
3.  Select the **Overview** link under the customer service module.

 Observe the message 'The dashboard was not found.'

</td></tr><tr><td>

Cloud Provisioning and Governance

 PRB1930444

 [KB2480996](https://hi.service-now.com/kb_view.do?sysparm_article=KB2480996)

</td><td>

The are empty execution ID entries in the sn\_cmp\_order\_step\_status table when the corresponding order record in sn\_cmp\_order is deleted

</td><td>

The user may notice many entries remaining in the sn\_cmp\_order\_step\_status table even after the corresponding order record is deleted from the sn\_cmp\_order table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Cloud Provisioning and Governance

 PRB1934389

</td><td>

An error message isn't displayed to the user if day2 actions are performed on either Stack or Resources

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Navigate to ESC Portal.
3.  Open any active stack.
4.  Test the scenario.
5.  Run any day2 actions \(like start, stop, etc.\).

 Observe that an error message isn't displayed to the user if day2 actions are performed on either Stack or Resources.

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB1955881

</td><td>

sn\_cmdb.\_\_rel\_type\_cache holds a lot of memory

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1939794

</td><td>

Guardrail scan to treat records on an instance as a base rather than signatures

</td><td>

In the guided setup UI remove orphan signature count and show missing signature count instead.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1939805

</td><td>

Signature verification process only honors the signature from one certificate

</td><td>

The validation fails because only the latest signature is considered.

</td><td>

1.  Create signatures for a record from two different certificates.
2.  Run the validation API.

Validation passes as the latest created signature was valid.

3.  Revoke the certificate that was used to create the latest signature.
4.  Run the validation API again.

 Expected behavior: It passes because the second signature for the record is still valid \(as the corresponding certificate is not revoked\).

 Actual behavior: It fails because only the latest signature is considered.

</td></tr><tr><td>

Code Signing

 PRB1939809

</td><td>

The JIT process loads signatures to a database during guardrail scan

</td><td>

Guardrail passes if a record doesn't have a signature in the sn\_kmf\_record\_signature table.

</td><td>

1.  Create a new record on TI.
2.  Don't generate a signature for it.
3.  Move the record to PI.
4.  Run a guardrail scan.

 Expected behavior: The scan should fail and the record should be flagged as missing a signature.

 Actual behavior: The scan passes.

</td></tr><tr><td>

Column Level Encryption

 PRB1919998

</td><td>

Save as Draft for catalog item does not work in portal when logged in through edge proxy

</td><td>

When trying to Save as Draft a catalog item from edge proxy, the URL generated for the catalog item contains double forward-slash items.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1927599

</td><td>

The condition builder on the presentational list displays all the options instead of the one that was searched

</td><td>

When the user searches for an option, the condition builder displays all the options in a list and highlights the one that was searched. Instead, only the option that was searched should be displayed.

</td><td>

1.  Create a UI Builder page.
2.  Configure the presentational list component.
3.  Open the page in run time.
4.  Select the filter icon.
5.  In one of the fields, search for an option.

 Expected behavior: The list displays only the option that was searched.

 Actual behavior: The list displays multiple options and highlights the one that was searched.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1949356

 [KB2616435](https://hi.service-now.com/kb_view.do?sysparm_article=KB2616435)

</td><td>

Exact count match check results in an incorrect duplicate task creation

</td><td>

After upgrading to Zurich, de-duplication \(dedupe\) tasks are created incorrectly under certain scenarios. As a result, a large number of records are created in the duplicate\_audit\_result table, causing significant database growth. Instead of updating existing entries, new records are inserted during each subsequent run. In one scenario, the de-duplication tasks are created when they were previously working. In another scenario, users with many hosts that contain cmdb\_serial\_number records with the same serial\_number and serial\_number\_type notice that the number of duplicate\_audit\_result can grow to be tens of millions daily.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Contract Management

 PRB1913448

 [KB2310704](https://hi.service-now.com/kb_view.do?sysparm_article=KB2310704)

</td><td>

The payment amount and total amount are incorrectly displayed in the local currency value under USD currency

</td><td>

When the user sets a payment amount using a local currency \(for example, NOK\) when selecting 'Adjust' on the Contract, the payment amount gets saved on the XML. When re-opening the record in Form view, it defaults to USD, but shows the amount that originally belonged to NOK. This behavior applies to both payment\_amount and total\_cost fields.

</td><td>

1.  Open a contract from the ast\_contract table.
2.  Select **Adjust**.
3.  Enter a new payment amount and currency, for example, NOK 966.00.
4.  Search and view the same Contract on List view.

Notice that payment amount and total amount are both reflected as \(NOK\)966.00 and \(USD\)96.7669 when selecting **Toggle currencies**.

5.  Open the record in Form view.

 Notice that the payment amount is USD 966.

</td></tr><tr><td>

Currency Administration

 PRB1940257

</td><td>

Real-time updates on a form display incorrect values in **currency** fields causing data loss

</td><td>

Since the Zurich upgrade, real-time updates on a form display incorrect values in all fields of type **currency**. The displayed value is always 100 times the correct value \(from the database\). After reloading the form, the correct value is displayed.

</td><td>

 

</td></tr><tr><td>

Customer Activity

 PRB1930824

</td><td>

Customer History shows the wrong day

</td><td>

Customer History shows activities under 'Yesterday', even though those activities were completed today.

</td><td>

1.  Log in to the configurable workspace \(now/cwf/agent/home\).
2.  Impersonate a frontline agent.
3.  In the list, navigate to a case.
4.  Select **New**.
5.  Add 'George Warren' as a contact.
6.  Save.
7.  Select the **Customer History side panel** icon.

 Observe that 'Customer History' shows activities under 'Yesterday', even though the time shows as 30 minutes ago.

</td></tr><tr><td>

Customer Central API

 PRB1926557

</td><td>

The filter is shown as undefined when only one facet type is present

</td><td>

The filter shows the values as undefined.

</td><td>

Prerequisites: Customer Central and Customer activity plugins.

 1.  Navigate to Activity Context Table -&gt; Open any context record \(Account and Contact or Consumer\)
2.  Select the **Facets** related list
3.  Keep only one facet active and rest of the facets inactive.
4.  Navigate to CSM/FSM Configurable workspace and open any case record.
5.  Select **Customer history**
6.  Select **Filter**.

 Expected behavior: The filter should show the values correctly.

 Actual behavior: The filter shows the values as undefined.

</td></tr><tr><td>

Customer Information

 PRB1934999

</td><td>

The addition of a new empty screen for customer Information

</td><td>

New empty screens are added for customer information when there is not an account contact or a consumer linked to the record.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1888302

</td><td>

Creating a column on a remote table throws a syntax error, which should be blocked for Workflow Data Fabric \(WDF\)

</td><td>

There is a new button in the table columns related list, which should be blocked.

</td><td>

1.  Hop into a datafabric instance.
2.  Impersonate an admin user.
3.  Navigate to x\_1234\_managerinsi\_df\_alert\_list.
4.  Configure the table.

Notice that there is an alert message that says, 'This record is in the managerinsighttest application, but Global is the current application. To edit this record click here.'

5.  Notice the new button in the table columns related list, which should be blocked.
6.  Select the **New** button on the columns related list.
7.  Create a new column called 'test type string'.
8.  Select **Save**.

 Notice a syntax error is thrown, the column is created, but the column label is empty. This should be blocked.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1893500

</td><td>

GraphTopology doesn't support references that use an explicit reference key

</td><td>

WDF tables in specific tend to use non sys\_id references.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1902218

</td><td>

For users with elevated privileges, the list view appears empty even though the data\_fabric ACL for elevated privilege users are present

</td><td>

Despite having a role with elevate privileges, the user cannot access all the data and the list view appears empty.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1907869

</td><td>

cypher2result error encountered with the unexpected token

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1922171

 [KB2617119](https://hi.service-now.com/kb_view.do?sysparm_article=KB2617119)

</td><td>

CONTAINS query interferes with the RLQUERY in hybrid table

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1925389

</td><td>

Glide queries that use a search term query in conjunction with an order-by on a date-time field return a null pointer exception

</td><td>

For instances running on RaptorDB, glide queries using search term query in conjunction with an order by on date time field return null pointer exception for matching records that have a null order field value.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1935637

</td><td>

Tie TD/view caching transaction to the transaction lifetime

</td><td>

Code sets the cached lifetimes for TD/views to a method call such as getDisplayValue, and should be tied to the longer lived transaction instead.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1935751

</td><td>

Prevent regex split on dot walk field security layer to prevent excessive object generation in GlideSecurityManager

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1936115

</td><td>

Reduce unnecessary arraylist generation when getting conditions in GlideSecurityManager

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1936372

</td><td>

Error when cypher queries for executed for a long entity \(node\) name

</td><td>

An error appears when cypher queries are generated by GraphQueryBuilder and executed for a long entity \(node\) name.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1938585

</td><td>

Creating edges between two WDF tables in KG designer results in an error

</td><td>

The error reads: 'Could not find source key column field account\_id in table u\_df\_co\_licenses for edge u\_account\_id.'

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1938967

</td><td>

Create TDs for the tables in a schema once rather than per-row when prepping the GR query condition for the final view

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1941638

</td><td>

ContainerCondition should gracefully handle getQueryConditions when no targetContainer is set

</td><td>

New code needs to check for null targetContainer conditions.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1942103

</td><td>

getForTables gives inactive columns

</td><td>

Results with inactive columns and edges are returned.

</td><td>

1.  Deactivate a column of any table \(for example, assigned\_to of incident\).
2.  Call the getForTables for the 'incident' table.

 Notice results with inactive columns and edges.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1944385

</td><td>

Add preallocate hint to the compound query conditions And/Or

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1944771

</td><td>

Incorrect state mapping passed in prompt \(-5 mapped to 'Pending' instead of 'New' for change\_request\)

</td><td>

The prompt/state-choice payload incorrectly labels -5 as 'Pending'. For change\_request, state = -5 actually represents 'New'. Because of this incorrect mapping, queries/filters and LLM prompts that depend on these choices will misclassify change\_request records. For example, requests for 'New' change requests may return incorrect results or none at all.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1944961

</td><td>

Exclusion doesn't work for upper case table names

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1945837

</td><td>

Correctly track select items that don't have aliases

</td><td>

For these cases, either get the alias from the CTE the item is defined in or create the proper tracking correlation for the field.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1946257

</td><td>

Normal \(non-aggregate\) cypher queries and response columns are returned without node alias prefixes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1946258

</td><td>

Request for API modification

</td><td>

Return some basic info for an aggregate column backing info. There is no backing information for any aggregate because there isn't actually a single record involved.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1946286

</td><td>

Failing Workflow Data Fabric \(WDF\) queries when trying to execute on connection for trino\_primary

</td><td>

When trying to get specific column instead of the entire record, the error occurs in the response.

</td><td>

1.  Log in to the instance.
2.  Impersonate a user.
3.  Run the script.

 Notice the error which includes, 'FAILED TRYING TO EXECUTE ON CONNECTION trino\_primary'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1946736

</td><td>

When users don't provide the alias to the aggregate column, it's not returning the answer

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1946743

</td><td>

In normal \(non-aggregate\) Cypher queries, aliases defined in the Return clause are not reflected in the response

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1947127

</td><td>

getDisplayValue has different values for GlideRecordDynamic and GlideRecord

</td><td>

getDisplayValue on references and choices should have the correct values.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1948171

</td><td>

Global Graph performance is slow when a large number of columns are fetched

</td><td>

KG can return all columns, which can be 200 or more in certain cases. It used to take 1880.8 milliseconds.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1948190

</td><td>

Cypher queries and response columns are returned without node aliases \(prefixes\)

</td><td>

The getBackingInformationForElement API requires prefixed column names to return sys\_id and table details. This causes the API to fail for such queries.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1949752

</td><td>

The Glide element getDisplayValue doesn't produce a formatted output for computed values like aggregates due to the lack of a schema

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1949793

</td><td>

Aggregation on a non-valid column type isn't returning an exception

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1949950

</td><td>

setLimit on Glide Record Dynamic throws null pointer exception

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1949955

</td><td>

For 'Aggregate Independent Node Match'-type cypher queries, getBackingInformationForElement isn't returning the backing information for non aggregated columns

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1950573

</td><td>

Improve performance for DatabaseViewsProviderTable\#getElementDescriptors

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1950574

</td><td>

Improve DBCypherParser execution time for same-table multi-key queries using an IN query condition

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1951964

</td><td>

Extend dot walk pattern split time performance optimization to other SecurityPatterns callers

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1953445

</td><td>

Prevent frequent TableDescriptor lookups from GSM

</td><td>

There are frequent TableDescriptor lookups in GlideSecurityManager to handle the feature behind field\_query\_restrict\_record\_access field Dictionary attribute.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1955036

</td><td>

Error messages in ElementBackingInfo

</td><td>

An error message appears during database dump creation. The error is due to the default constructor for ElementBackingInfo trying to set up the scope: 'Could not define Scriptable class ElementBackingInfo for extension point'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1955111

</td><td>

Distinguish between elements that aren't in the DB \(like sys\_tags\) vs. ones that are function fields

</td><td>

Queries are disallowed against all elements not in the database, but that excludes function fields. The criteria should be adjusted to disallow the first element types and allow the second.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1955135

</td><td>

There's an error when executing a cypher with 0 edge path length, such as '\[:manager\*0..1\]'

</td><td>

The issue is the first branch of the union only has one table, so only one key is injected while all the others have two. The key injection is going to have to special case the union code and check for situations like this.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1962540

</td><td>

report\_on is honored for aggregates in cypher

</td><td>

Currently checks are done in tableLevelAclAllowed which will return false if there is no ACL defined at all. PA used hasRightsTo which has a more permissive behavior and allows access in this case.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1964653

</td><td>

Test failures in db-test

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1942866

</td><td>

StatsGatherer shouldn't break the execution when it checks the table stats for a table in which the stats weren't collected by SNC

</td><td>

StatsGatherer breaks the loop and stops with exception trace.

</td><td>

1.  Create a table on an instance.
2.  Make sure the SNC doesn't have the table size reported. If reported, delete the entry.
3.  Run StatsGatherer.

 Expected behavior: StatsGatherer reports this table in logs and continues the execution with the next tables.

 Actual behavior: StatsGatherer breaks the loop and stops with exception trace.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1891038

</td><td>

Trino API schemas/xxxxx/tables?type=logical should not return data fabric tables

</td><td>

 

</td><td>

1.  Open an instance with Data Fabric configured.
2.  Map a remote table t\_remote to df\_t\_remote.
3.  Run the Trino API schemas/xxxxx/tables?type=logical.

 Notice that the returned list should not contain t\_remote or df\_t\_remote.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1951095

</td><td>

Set a replica pool's in-memory heartbeat to null upon failure to get heartbeat

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1959979

</td><td>

Get connections from secondary pool doesn't retry more than once

</td><td>

Retry count is capped because failImmediate is always set to true for secondary pools. This causes some issues with read replica routing.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1925955

</td><td>

Columns on the list view failed to load when dot-walk fields are present

</td><td>

 

</td><td>

1.  Navigate to **sys\_properties**.
2.  Ensure glide.db.meta.non\_sys\_id\_sparse\_storage.allow is set to true.
3.  Navigate to **All** &gt; **Manager Analytics**.
4.  Open either **Alerts**, **Journey**, or **Voice Survey** list views.

Notice that when the list view has dot-walk fields present, the user gets most of the non-dotwalked columns with empty values \(only ones showing are the primary key + reference column\).

5.  Navigate to the 'Personalize' list view and take out the dotwalk fields from the table.

The table displays all the values from the list view even with the property enabled.

6.  Navigate back to personalized list view.
7.  Select **Reset to column defaults**.
8.  Navigate back to sys\_properties and set the property to false.
9.  Navigate back to the list view.

The user should see the values load in the table even with the dot-walk fields present.


</td></tr><tr><td>

Database Persistence

 PRB1935218

</td><td>

Don't use the string replaceFirst in GlideElement and GlideRecordSecure because it causes excessive pattern compile

</td><td>

When certain scripts and profiles are run, there's noticeable memory usage for the regex compilation coming from String.replaceFirst.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1935249

</td><td>

Glide record doesn't retrieve all the records from the first pass query for Workflow Data Fabric \(WDF\)

</td><td>

Found an issue when glide.db.trino.first\_pass.window\_clause\_limit is greater than glide.db.datafabric.max\_records, the user only gets the back the number of rows based on the value of max\_records as opposed to first\_pass\_window\_clause.

</td><td>

1.  Navigate to **System properties**.
2.  Ensure glide.db.datafabric.max\_records is set to 10000.
3.  Check that glide.db.trino.first\_pass.window\_clause\_limit is greater than 10000.
4.  Run a simple glide record query script on a single pk table.

 Notice that the first pass query is 10053 records, but only 10000 records are back.

</td></tr><tr><td>

Database Persistence

 PRB1950444

</td><td>

Improve logging for CypherSQLs generated and for DatabaseViews

</td><td>

Logs are written to syslog and are not-controlled. With this change, they can be controlled and only appear on the app server logs.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1955887

</td><td>

DBQuery.addSystemReturnField\(\) isnt functioning correctly with PostgreSQL for non sys\_id tables

</td><td>

The method DBQuery.addSystemReturnField\(\) does not work as expected for Non sys\_id based tables like pa\_scores\_l1.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB1889108

</td><td>

Propagate routing category to SN Connector

</td><td>

If a routing category is set to a trino query that uses the loopback catalog, the category will not be propagated to the remote-side for routing. Currently, DBSqlParserDataFabric sets the category to 'trino' for routing.

</td><td>

Execute a trino query with a routing category.

 Notice that this results in a SN loopback query which doesn't have the routing category set.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1891891

</td><td>

Correlate all queries to the originating trino query for logging for SN Connector REST API

</td><td>

The incoming query is logged in TrinoConnectorService but the origin context is lost, and the user cannot correlate the incoming queries to REST API to the originating trino query.

</td><td>

Open a list view that involves a Glide table and a data fabric table so that it executes the query via the loopback SN Connector.

 Notice that in the logs, it should print all the queries with 'Delegating fetch request to DB for client query' and 'Time consumed to return from DB call\(ms\):' however, the user can't tell what the originating transaction is.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1929116

</td><td>

OAuth access token error occurs when data is fetched from a remote table to a physical table

</td><td>

The query tries to access a property from a remote table to physical table. The cypher throws the error, 'OAuth access token is required for loopback connector type.'

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB1941719

</td><td>

Opening the list views of manager insight tables times out when parsing is enabled

</td><td>

When the user opens the list view that has the ref field **manager\_employee\_number**, they see multiple queries and the list view times out.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB1950092

</td><td>

The WDF table eligible for sparse storage is not executing one pass query when calling get\(\) and Equals operation

</td><td>

The WDF table eligible for sparse storage now executes a two pass query when running a get\(\)/Equals operation. It should only execute a one pass query for both scenarios, similar to a glide table.

</td><td>

Scenario 1:

 1.  Ensure the property glide.db.meta.non\_sys\_id\_sparse\_storage.allow is created.
2.  Set it to 'true'.
3.  Enable SQL debug.
4.  Navigate to the list view of a WDF table with single primary key defined.
5.  Open the condition builder.
6.  Select the **Primary key** field is 'operation'.
7.  Run it.
8.  Scroll down the page when the list view has finished loading.

 Notice that in the List section, the record count query there will be two additional queries being made on the data fabric table when only one query is made.

 Scenario 2:

 1.  Ensure the property glide.db.meta.non\_sys\_id\_sparse\_storage.allow is created.
2.  Set it to 'true'.
3.  Enable SQL debug.
4.  Navigate to **Background scripts**.
5.  Execute a glide record script that call get using the encoded sys\_id of a WDF table.

 Observe that when executing the script, there are two queries being executed instead of just one.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1952581

</td><td>

Error occurs when querying both WDF and physical table attributes together

</td><td>

 

</td><td>

1.  Start a conversation with the virtual agent.
2.  Say 'I want to know some employee details'.
3.  When the agent responds, say 'I need the name and email of certain employees'.
4.  When the agent asks about a reporting manager, provide a name.
5.  When the agent asks about a specific role or job title, provide a job title.

 Observe that no response is returned.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1953550

</td><td>

List view is unable to load due to a logical query of the cmdb\_ci\_computer table

</td><td>

The list view is unable to load due to the logical query of cmdb\_ci\_computer table, which includes the '**sys\_tags**' field. DBSqlParser translates it to a query against the cmdb table that does not have the '**sys\_tags**' field. In this case, DBSqlParser should be used against a shadow table with its own ACLs, distinct from the ones at the source. The new GlideRecordDynamic should be integrated for usage in the TrinoConnectorService. This also includes defining a new DBSqlParser type that does the required security checks.

</td><td>

1.  In a local instance, create a remote SN connector to a remote instance.
2.  Create a remote df\_cmdb\_ci\_computer\_remote table, bringing all the fields that show up in the WDF Hub \(except for the **sys\_domain** field\).
3.  Load the list view of df\_cmdb\_ci\_computer\_remote.

 Observe the error that appears.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1904932

</td><td>

Connection credential should not be cloned for Workflow Data Fabric \(WDF\) after clone automation

</td><td>

After cloning, WDF connection credentials are copied to the target instance.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1945751

</td><td>

Forms with nested section choices fail due to mandatory fields

</td><td>

 

</td><td>

1.  Create a connector in the sn\_df\_connector table.
2.  Create two section choices in one of the components.
3.  Inside the section choices, create another section choice.
4.  Try to connect, filling all the visible fields.

 Observe that it fails with the error 'Complete all the required mandatory fields'.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1949350

</td><td>

Sys\_ fields are silently dropped when importing table from Local ServiceNow instance

</td><td>

No sys\_ fields exist for the WDF table that was created from remote glide.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1785169

</td><td>

ACC-V execution for Oracle GLAS Data Collection is failing because the pattern is removing 'ct\_cpuq.sh' and 'db\_queries\_to\_csv.sql' as part of the 'Target Cleanup' process

</td><td>

ServiceNow removes the files 'ct\_cpuq.sh' and 'db\_queries\_to\_csv.sql' as part of the 'Target Cleanup' process, while ignoring 'db\_queries\_to\_csv\_11g.sql' which is causing the step 23 run Ora LMS script Unix with SID to fail.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1843017

</td><td>

For patterns on agent, add all available assets that start with 'pattern-execution' to OnTheFlyCheck

</td><td>

Currently, the system looks for three plugins \(pattern-execution, pattern-execution-mapping, pattern-execution-content\) when sending a check to ACC. This can become a problem with increasing number of content Store apps as each Store app may want to ship their own ACC plugin with the script files. The current mechanism only supports three.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1934265

</td><td>

Document type and config are overridden in certain views

</td><td>

When the user loads a doc\_qna use case in table view, the 'Document Type' and 'Document Config' are reset to the default doc extraction values.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1934268

</td><td>

Document Config can't be updated on DocQnA use cases

</td><td>

Attempting to update the Document Config results in an error.

</td><td>

1.  Ensure a task with status 'Done' exists in a DocQnA use case.
2.  Attempt to update the Document Config.

 Notice the error, 'Can't update document config as there are pending document task trainings, Please update once everything is complete.'

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1951333

</td><td>

Hybrid use cases should be selectable in the **Create a Document Task** flow action

</td><td>

 

</td><td>

1.  Create a use case in the 'Extract information from documents' skill.
2.  Add a target table and integration for the created task.
3.  Open the integration in flow designer.

 Observe that the created use case is not listed in the 'Task Definition' drop-down list of the **DocIntel - Create a Document Task** action.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1955108

</td><td>

'Details' ends up in name for extraction use case

</td><td>

A sys\_di\_key record is created where name is set to the 'Details' value.

</td><td>

1.  Navigate to NowAssist Admin.
2.  In the skill 'Extract information from documents', create a new use case.
3.  Create one field with 'Name' as 'invoice\_number' and 'Details' as 'Invoice number or purchase order number'.

 Expected behavior: A sys\_di\_key record is created where display\_name and name are 'invoice\_number' \(or maybe 'invoicenumber'\).

 Actual behavior: A sys\_di\_key record is created where name is set to the 'Details' value.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1959455

</td><td>

Add a 'skipped' status to the 'DocIntel Task' table

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1959457

</td><td>

Improvement to make page-level try–catch instead of whole-PDF try–catch

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1959459

</td><td>

Delete task definition's 'read only' policy on capability

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1959464

</td><td>

DocReader local to return an info page of embedded images

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1959466

</td><td>

Integrate the image rescaling Java API for Doc Reader local Glide code

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1959468

</td><td>

Update DocReader Local to use the content type instead of the file extension

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1959471

</td><td>

Glide scale attachment summarization

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1959473

</td><td>

Code changes for a document splitting on Java-level Glide changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1959475

</td><td>

Java API to rescale the image doc-type before sending to an LLM call

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Management

 PRB1941267

</td><td>

Unable to remove document references and users for a document from scoped apps

</td><td>

 

</td><td>

1.  Create a document and version.
2.  Link this document to a core-company record.
3.  Optional: Grant access to multiple users.

 Notice that users are unable to delete the users/association from a scoped app via server scripts.

</td></tr><tr><td>

Dynamic Translation

 PRB1913176

</td><td>

A One API Service Plan feature for Virtual Agent's \(VA\) Utterance Translation has no timeout set

</td><td>

It needs a timeout set and the error policy to be set to exit the Service Plan execution. In addition, the OneAPI framework needs to prevent this error from happening in the first place.

</td><td>

1.  Set up VA Language Detection and Dynamic Translation.
2.  Enable both.
3.  Install the Appropriate Language plugin.
4.  Enable dynamic translation for VA for the installed language plugin.
5.  Change the mweb sys\_cs\_channel synchronous column to true
6.  Start a VA web client conversation in English.
7.  Type an utterance in the language of the plugin installed.

 Expected behavior: Language detection and utterance translation work as expected in synchronous mode

 Actual behavior: Observe that the language detection call or subsequent utterance translation fail to due to the stacktrace.

</td></tr><tr><td>

Email Notifications

 PRB1960674

</td><td>

Create an email/email draft record creation script include in the global scope

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Embedded Help

 PRB1942884

</td><td>

Unable to view the 'Help center' content for different roles when there's an uppercase character in the RoleName

</td><td>

 

</td><td>

1.  Try to create the embedded help.
2.  Add the roles, except admin, and have the role\_name have an uppercase character.
3.  Check on the page.

 The content isn't displaying in the 'Help center' panel.

</td></tr><tr><td>

Event Management

 PRB1895330

</td><td>

ImpactStatus isEquals tries to compare non-existent ImpactStatusKey

</td><td>

This fails in instances where the field does not exist.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1906529

</td><td>

A custom description of the Tag-cluster group definition is not assigned to the group

</td><td>

On Zurich release, Tag Based Alert Clustering definition 'Override group description' does not work for Alert Group.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1939558

</td><td>

Get related CIs should support parameters for limits and have consistent and meaningful logs for effective troubleshooting

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1941171

</td><td>

Slow query in Event Management - Process Events

</td><td>

The observed runtime is 27 ms on average. A replacement query averages 2.3 seconds or around 85x slower.

</td><td>

 

</td></tr><tr><td>

Fenix \(Family\)

 PRB1934205

</td><td>

In the Fenix plugin, scope accessibility issue in getJobStatusesByDeployments

</td><td>

Unlike other batch mode APIs, this one doesn't support cross-scope access. It supports invocation only from the global scope. For consistency and usability, it would be helpful if this could be made accessible from the global scope.

</td><td>

1.  Create a new scope.
2.  Create a batch manifest in that scope.
3.  Execute it a few times so that there are records in the fenix\_job\_status table.
4.  Run a script to get the job\_statuses, but be sure to execute the script from the new scope.

 Observe that it generates the following error: 'script execution error: Script Identifier: null.null.script, Error Description: invalid return type: org.json.JSONArray, Script ES Level: 200 Evaluator.evaluateString\(\) problem: java.lang.RuntimeException: invalid return type: org.json.JSONArray: com.glide.script.fencing. ScopedFunction ObjectTypeHandler .coerceReturnValue \(ScopedFunction ObjectTypeHandler .java:338\)'.

</td></tr><tr><td>

Field Service Task Bundling

 PRB1952595

</td><td>

Scheduling subtasks takes longer than expected

</td><td>

Scheduling subtasks and updating the **Scheduled Start** field on subtasks takes significantly longer than expected.

</td><td>

1.  Create a bundle a task with at least 500 subtasks.

Notice that the bundle task is in a pending dispatch state.

2.  Assign the created bundle task to an agent.

Notice that the bundle assignment will take a lot of time.

3.  Check the subtask schedule start date and the time it took to update the subtask schedule start date info.

 Notice that the UI is stuck or takes a long time \(5-6 minutes\).

</td></tr><tr><td>

File-based Discovery

 PRB1936524

</td><td>

File-based Discovery doesn't capture the content when the filename contains spaces

</td><td>

Discovery throws an below error in the Discovery logs for a filename that contains spaces: 'Error\(s\) during file-based discovery: base64: extra operand '/usr/share/.../IOP' Try 'base64 --help' for more information'.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1925181

 [KB2407160](https://hi.service-now.com/kb_view.do?sysparm_article=KB2407160)

</td><td>

The Script API inForeground run a subflow that calls another subflow that has an MID action step throws an exception before the outputs are ready with a message

</td><td>

The flow should complete and the outputs displayed in Scripts - Background. However, the flow executes, but an exception is thrown: 'The current execution is in the waiting state and the subflow outputs are not available'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1936210

</td><td>

High Priority events are not cached to the same node due to Yield Check

</td><td>

An event is not cached to the correct node.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1950344

</td><td>

Capability metrics are executed in a Skill Role Masking session

</td><td>

Auto evaluation breaks with the application of role masking on 'Evaluate API'.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1958181

 [KB2606177](https://hi.service-now.com/kb_view.do?sysparm_article=KB2606177)

</td><td>

Flows are intermittently not triggered after upgrade in a domain separation enabled instance

</td><td>

After upgrading a domain separated instance, some flows are no longer triggered. This is because some of the flow's records are in the domain that the flow was defined in, and other records in a different domain.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1960669

</td><td>

Use a new role context API for role masking in flows

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flow Generation \(Family\)

 PRB1949261

</td><td>

Flow Generation and Flow Designer GenAI Glide changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flow Generation \(Family\)

 PRB1957611

</td><td>

Capability response not parsable Error - Prompt LLM \(Glide Only\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1918469

</td><td>

There's an error checking availability for a flow recommendations skill

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1924455

</td><td>

The 'Skill Config' drop-down list doesn't load for the 'flow\_designer' and 'Action\_designer' roles

</td><td>

 

</td><td>

1.  Create a flow.
2.  Add an action.
3.  Add step Call Now Assist Skill.

 Observe that the 'Skill Config' drop-down does not load for the 'flow\_designer' and 'Action\_designer' role.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1938123

</td><td>

Flows using base instance actions related to the plugin 'Customer Service Spoke' fail after upgrading to Yokohama

</td><td>

The flows in question are base instance actions related to 'Customer Service Spoke': Add Work Note to Task and Add Comment To Task.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1952640

</td><td>

Unable to see AI agents for the 'Use an AI agent' action for users other than Admin

</td><td>

The AI agents are not visible on a drop-down list.

</td><td>

1.  Provision an instance with the flow-designer-genai app installed.
2.  Navigate to workflow studio.
3.  Create a new flow / subflow.
4.  Select an action - Use an AI agent.
5.  For the same action, select the **Select AI agent** drop-down list.

 Notice that the AI agents are not visible.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1960705

</td><td>

Create a scriptable API and global script includes for getting execution data

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1962584

</td><td>

'Skill Config' drop-down list doesn't load for the 'Action\_designer' role

</td><td>

The 'Skill Config' drop-down list doesn't load for the 'flow\_designer' and 'Action\_designer' role.

</td><td>

1.  Create a flow.
2.  Add an action.
3.  Add a step called Now Assist Skill.

 Notice that the 'Skill Config' drop-down list doesn't load for the 'flow\_designer' and 'Action\_designer' role.

</td></tr><tr><td>

GlideRecord

 PRB1946744

</td><td>

Querying against the 'numeric value' variable silently fails because casting to 'signed' isn't supported in postgres

</td><td>

The process silently fails and doesn't return any data.

</td><td>

1.  Create a 'Numeric value' variable for a catalog item.
2.  Using a catalog item, create a request item.
3.  Run a filter on sc\_req\_item table with the filter on a variable with either of these filters:
    1.  'is empty'
    2.  'is not empty'
    3.  'greater'
    4.  'less than'

 Expected behavior: The created sc\_req\_item is returned.

 Actual behavior: The process silently fails and doesn't return any data.

</td></tr><tr><td>

Glide Server APIs

 PRB1921133

</td><td>

Users can't query guest voice agents due to a lack of impersonation ability in a scoped app

</td><td>

The AI Voice agent application makes a call to a platform API to retrieve guest or public voice agents. These are agents that return basic public data such as company hours, location, etc. These agents have an ACL for a guest user. However, the integration user can't impersonate a guest since the app isn't in a global scope.

</td><td>

Call into the voice agent app.

 Notice in the orchestrator that the public agents aren't queried correctly.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1941250

</td><td>

In Yokohama and Zurich, assessment reporting views aren't displayed

</td><td>

 

</td><td>

1.  Create and publish a RAM.
2.  Select the **View reporting** button.

 Observe that the reporting view is not displayed.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1881376

</td><td>

BytesOut is inaccurate

</td><td>

 

</td><td>

1.  Set up a Kafka producer on a local machine using Kafka Java APIs.
2.  Produce a single, large batch of messages.
3.  Wait until the hourly aggregation job runs to populate hermes\_usage\_metrics.
4.  Check the corresponding value in 'Total MB Value Per Hour'.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1888169

</td><td>

Unnecessary logging in syslog by KafkaConsumerRegistry and GlideHermesTopicManager

</td><td>

There are unnecessary 'Information' type logs in the syslog table by the com.glide.hermes.KafkaConsumerRegistry, com.glide.hermes.TopicSynchronizer and com.glide.hermes.GlideHermesTopicManager packages.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1905820

</td><td>

Dashboard accuracy issues

</td><td>

There are two issues with the Application ID 'All' filter: The 'Total Megabytes In' value is doubled with the 'All' filter. Additionally, when there's a singular day spike in metrics, and all other values are 0, the graph itself reports a 0 value on the spike date despite the graphic implying otherwise.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1944311

</td><td>

Setting glide.sys.date\_format to dd-MMM-yy triggers 'GlideDateTime:Invalid date time' for xmlstats.do?include=hermes

</td><td>

'getLastRunTime' uses 'getDisplayValue\(\)' which can change from the non-default date-time format yyyy-MM-dd when 'glide.sys.date\_format' is updated.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1891279

</td><td>

The pop-up message \[Attachment deleted…\] is still shown on workspace after abort deletion by Business Rule

</td><td>

A pop-up message reading 'Cannot delete Attachments' is shown and deletion fails.

</td><td>

1.  Open a sys\_attachment.list and create a new business rule to disable 'Delete attachment' and in Incident table.
2.  Open the Incident.list and create a new record.
3.  Attach file to the record.
4.  Open Service Operations Workspace and Open the created Incident record.
5.  Delete the attachment.

 Expected behavior: A pop-up message reading 'Cannot delete Attachments' will be shown and deletion fails.

 Actual behavior: A pop-up message reading 'Cannot delete Attachments' is shown and deletion fails.

</td></tr><tr><td>

Horizon Component Library

 PRB1959336

</td><td>

now-highlighted-value: helperContent update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1959337

</td><td>

New and updated utility icons

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Horizon Textarea Component

 PRB1891770

</td><td>

The scrollbar does not appear for now-textarea when text is pasted

</td><td>

No scrollbar available.

</td><td>

1.  Create a component to render now-text-area with size:
    1.  Width: 50%
    2.  Height: calc \(100% - 50px\).
2.  Navigate to browser to render above component.
3.  Type a few words in the textarea, then paste large text &gt; size of textarea.
4.  Scroll content in textarea \(Don't select inside textarea after pasting, just try to scroll\).

 Expected behavior: After pasting text, the user should be able to scroll text content.

 Actual behavior: No scrollbar available.

</td></tr><tr><td>

HR Service Delivery

 PRB1934992

</td><td>

RCAs for the 'Predict and transfer' AI workflow

</td><td>

Related to ER case summarize, both in Now Assist Portal \(NAP\) and the 'Form' view.

</td><td>

1.  Impersonate as an ER case writer user.
2.  Select the **Summarize** button on the 'ER case' form page.
3.  Select the **Summarize a record** button on the ER case from NAP.

 Expected behavior: RCAs shouldn't be generated.

 Actual behavior: RCAs are generated.

</td></tr><tr><td>

HR Service Delivery

 PRB1940427

</td><td>

A user with snc\_internal not be able to access an HR checklist

</td><td>

The issue occurs when the Explicit Roles plugin is installed before the HR Core plugin.

</td><td>

1.  Create a checklist\_item record for any HR case or HR task and assign it to any user who has an snc\_internal role.
2.  Open the access analyzer and do a 'can-read' check for an snc\_internal user.

 Notice that the snc\_internal user has no access.

</td></tr><tr><td>

HR Service Delivery

 PRB1942339

</td><td>

Use case chaining is not happening in case of prediction failure

</td><td>

 

</td><td>

1.  Create a new case.
2.  Notice that the Prediction/Transfer agent is called in case prediction fails.

 Expected behavior: Another use case is triggered.

 Actual behavior: Chaining doesn't occur.

</td></tr><tr><td>

HR Service Delivery

 PRB1955226

 [KB2634960](https://hi.service-now.com/kb_view.do?sysparm_article=KB2634960)

</td><td>

Missing **Sentiment Analysis** Fields / RCA errors from Platform AI Agents and Skills

</td><td>

An RCA error appears within HR Agent Workspace on an HR Case if that Case belongs to one of the following COEs \(HR Benefits Case, HR Compensation Case, HR Corporate Communications Case, and HR Global Mobility Case\). The RCA is requesting access to the HR Case COEs on behalf of Platform AI Agents and Skills, specifically from the source of the Script Include called SentimentAnalysisProcessor.

</td><td>

1.  Navigate to the COE Configuration module.
2.  Navigate to the HR Cases list view.
3.  Create a case based on one of these COEs \(for example, a Compensation HR Case\).

 On the newly created HR Case page, observe that the **Sentiment** and **Sentiment trend** fields are missing and the RCA error at the top of the page.

</td></tr><tr><td>

Identity

 PRB1956763

</td><td>

Federated ID for roles \(Regulated Market\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Inbound IP Address Access Control

 PRB1931553

</td><td>

Database connections Pool Exhaustion issue

</td><td>

DBIs fail to establish new connections after approximately 2.5 hours.

</td><td>

 

</td></tr><tr><td>

Integrated Email Client

 PRB1959343

</td><td>

Modify on an insert click on NACM for branded templates

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Integrated Email Client

 PRB1959345

</td><td>

Identify if an email has a branded template in it

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Integrated Email Client

 PRB1959347

</td><td>

Support customization at the client side

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Integration Authentication

 PRB1960124

</td><td>

Verbose JWT logs use opaque tokens when AuthLog is enabled

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1933193

</td><td>

Configuration data is missing in REST step

</td><td>

The HTTP operation relies upon an output from the IntegrationResolverOp. If it doesn't exist, it falls through and throws an exception.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1946989

</td><td>

Async HTTP client does not honor proxy bypass settings

</td><td>

In FlowHttpContextProvider.getDefaultRequestConfigBuilder\(\) a proxy is added if the global settings are configured. However, it does not honor the 'glide.http.proxy\_bypass\_list' property setting.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1959514

</td><td>

A support server sends event step executions on MID server

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Investment Portal

 PRB1920188

</td><td>

Can't open or filter users/groups when there are a lot of records in the sys\_user table

</td><td>

In the Investment Portal, when the user opens 'Users/Groups' and add a new user, it takes about 30 seconds to load. Search doesn't work.

</td><td>

1.  Navigate to **Filter Navigator** &gt; **Investment Portal**.
2.  Open any of the bookmarked records.
3.  Select the **User** icon to open 'Users/Groups'.
4.  Select **Add users**
5.  Wait for it to load, about 30 seconds.
6.  Try to add some letters in input.

 Observe that it doesn't work and doesn't search anything.

</td></tr><tr><td>

Issue Auto Resolution for Virtual Agent

 PRB1957745

</td><td>

IAR does not work on a znowassist instance

</td><td>

Virtual agent doesn't appear in the activity log.

</td><td>

1.  Enable Incident IAR.
2.  Navigate to go /esc.
3.  Portal search for 'create incident'.
4.  Create an incident for priority 3 - 'printer issue'.

 Expected behavior: IAR should run, the Virtual Agent should reply in the activity log, and a notification should be received.

 Actual behavior: Virtual agent is not showing up in the activity log.

</td></tr><tr><td>

JVM at Scale

 PRB1959253

</td><td>

Java 21 upgrade to runtime

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1948377

</td><td>

KBversioning\(\) script isn't accessible from another scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1948582

</td><td>

The **Next** button on UI16 isn't shown until the user scrolls up after selecting template

</td><td>

The **Next** button shouldn't be moved out of focus when user selects template.

</td><td>

1.  Open the latest track/anowassist or track/znowassist instance.
2.  Log in as a user.
3.  Turn off sn\_km\_center.glide.knowman.redirect.enable or sn\_km\_center.glide.knowman.enable.
4.  Create a new KB article.
5.  Select a template.

 Notice that **Next** button in the bottom of the page is removed, but on selecting the template, there is a vertical scroll bar that automatically takes the user to bottom of the page, and the Next button on the top right of the page is not shown until user scrolls up.

</td></tr><tr><td>

Knowledge Management

 PRB1958725

</td><td>

Editing using the editor won't work for FSM users while creating KB article

</td><td>

The user is restricted when selecting 'Edit', and a security access message appears.

</td><td>

1.  Log in to the instance.
2.  Install the FSM app with sn\_fsm\_gen\_ai 8.0.0-snapshot, which installs Now Assist for Platform 10.0.1-SNAPSHOT.
3.  Impersonate a user with wm\_admin or wm\_dispatcher.
4.  Navigate to the **wm\_task** table.
5.  Select any Work Order Task with 'Completed' state.
6.  Select **Create Knowledge**.

Notice that it gives the option 'Yes, draft with Now Assist' that can be selected by the user.

7.  Select on **Edit**.

 Expected behavior: The user should be able to select the option to edit.

 Actual behavior: The user is restricted with the message, 'Security constraints prevent access to requested page.'

</td></tr><tr><td>

Knowledge Management

 PRB1959682

</td><td>

KB submission flow doesn't work after the uptake of a KB interceptor page

</td><td>

 

</td><td>

1.  Navigate to **Now Assist Admin** &gt; **Workspaces** &gt; **Service Operations Workspace**.
2.  Select the 'List' icon on the left sidebar.
3.  Navigate to **Incidents** &gt; **Closed**.
4.  Open any of the closed incidents.
5.  Select the button **Create knowledge**.

 Upon landing on the kb\_submission screen, the screen title displays 'KB Submission' in bold.

</td></tr><tr><td>

Knowledge Management

 PRB1959880

</td><td>

The user can't create Knowledge Blocks

</td><td>

In scenario 1, the URL redirects to the kb\_knowledge form page, not the kb\_knowledge\_block form page. In scenario 2, the user cannot select the block in the Article body after it is published.

</td><td>

Scenario 1:

 1.  Navigate to **Knowledge** &gt; **Knowledge Blocks** &gt; **All**.
2.  Select **New.**

 Notice that the URL is redirecting to the kb\_knowledge form page, when the URL should redirect to the kb\_knowledge\_block form page.

 Scenario 2:

 1.  Create a block by navigating to **Knowledge** &gt; **Knowledge Blocks** &gt; **Create New block**.
2.  Create any article.
3.  Add the block created in step 1.
4.  Attempt to select the block in the article body.

Observe that the user is able to select it.

5.  Publish the article.
6.  Open the same article.
7.  Select **Checkout**.

 Observe that the user isn't able to select the block in Article body, when they should be able to select it and delete it from the Article body.

</td></tr><tr><td>

Knowledge Management

 PRB1959914

</td><td>

The Knowledge Search Properties configuration page shows 'Requested resource not found'

</td><td>

 

</td><td>

1.  Open a Zurich instance that has Now Assist.
2.  Navigate to **Knowledge** &gt; **Administration** &gt; **Guided setup**.
3.  Select **Get started**.
4.  Select **Get started**for Knowledge Search.
5.  Select **Configure Knowledge Search Properties**.

 Observe that the Knowledge Search Properties aren't loading. 'Requested resource not found' is shown.

</td></tr><tr><td>

Knowledge Management

 PRB1962920

</td><td>

Version bump for KC and ECE in anowassist and Zurich track

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB1913012

</td><td>

Creating a case of any journey config doesn't show the Journey number field in the case details

</td><td>

The issue occurs due to changes that modify the form when GenAI is installed. Rather than adding the fields in an if folder, the fields should just be added to the normal form layout in the update folder; if the fields do not exist, they will not show up on the form.

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB1945674

</td><td>

Improve logging and validation in glidefix\_deprecate\_le\_workflow for when the 'sn\_hr\_le.use\_flow' property fails to update

</td><td>

The logs for the fix script doesn't re-validate the property.

</td><td>

1.  Install the following on a WDC instance:
    -   HR Core
    -   HR Lifecycle Event \(HR LE\)
    -   HR Lifecycle Event for enterprise \(HR LE Ent\)
2.  Upgrade the instance to Yokohama.
3.  Examine the logs for the glidefix\_deprecate\_le\_workflow fix script.

 Notice that it doesn't re-validate that the property was successfully updated.

</td></tr><tr><td>

Lifecycle Events

 PRB1955284

</td><td>

Bulk Task approvals are not being generated

</td><td>

BulkTaskMgmtRejectUIIT fails when run in the Zurich branch.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1911269

</td><td>

SHOW\_ALL event is dispatched on every context action click

</td><td>

 

</td><td>

1.  Create an experience.
2.  Add the record list bundle.
3.  Open the page.
4.  Select the **Row edit** icon.

 Expected behavior: The SHOW\_ALL event isn't dispatched.

 Actual behavior: The SHOW\_ALL event is dispatched.

</td></tr><tr><td>

List Administration

 PRB1944139

</td><td>

Uptake allowExtended fields property on the lists side for the sn-field-select component

</td><td>

 

</td><td>

1.  Create a system property 'glide.ui.list.allow\_extended\_fields'.
2.  Set it to 'true'.
3.  Create a UI Builder page with a list component configured.
4.  Set the table property 'task'.
5.  Open the runtime page.
6.  Select the **Personalize columns** button in the header.

 Expected behavior: The fields from all tables extending from the task are displayed.

 Actual behavior: Only fields from the task table are displayed.

</td></tr><tr><td>

List Administration

 PRB1948024

</td><td>

A reference list endpoint does not retrieve the record count when non-English languages are enabled

</td><td>

The Reference list endpoint does not retrieve the record count when non-English languages are enabled.

</td><td>

1.  Change the instance to another language.
2.  Open workspace record with a reference field with auto completer configured.
3.  Type something to filter the field with auto completion.

Observe the number of records under the type-ahead.

4.  Select the magnifying glass \(lookup\) to open the modal.

 Expected behavior: The total number of records in the modal footer should be the same as the one shown under type-ahead.

 Actual behavior: The total number of records in the modal footer is different.

</td></tr><tr><td>

List Administration

 PRB1959331

</td><td>

Implement filter assist in Zurich

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Machine Identity Management

 PRB1959515

</td><td>

Connect machine identity and request usage dashboards

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MetricBase

 PRB1943699

</td><td>

The testConnectivity\(\) couldn't determine empty endpoints and returns success

</td><td>

Instance Move should check for clotho endpoints at the preflight level itself rather than failing at the cutover stage.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1950570

</td><td>

Mobile doesn't return all results when searching for French terms when this works correctly on the platform

</td><td>

On the Create Defect screen there is a reference field Defect nature \(refers to table Defect Nature\). The referenced table's display field is Translated Text with values available in six languages. When the user's language is French, the reference list displays the list of values in French correctly, but the search does not match.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1951413

</td><td>

Search cards based on external content can't be configured on fields created on the external content table

</td><td>

Creating a search card based on an external connector based table allows only certain fields to be visible. After the configuration of the mobile search card, find that the created field for mobile\_url can't be used in the card for navigation.

</td><td>

1.  Navigate to the instance.
2.  Impersonate a user.
3.  Navigate to the portal.
4.  In the global search, search for the keyword 'lays'.

Notice that the results are displayed.

5.  Navigate to the 'News' tab to view the results.
6.  Open the Now mobile app.
7.  Log into the mobile app.
8.  Impersonate Abel Tuter in Now mobile.
9.  Search for 'lays' in global search.

 Notice that no results are seen under the 'News' tab.

</td></tr><tr><td>

Mobile Platform

 PRB1953561

</td><td>

Adding an attachment offline gets applied to other records

</td><td>

Attachments are visible in records where they shouldn't be.

</td><td>

1.  Make sure the offline functionality is enabled on the instance.
2.  Navigate to Offline mode.
3.  Open a list with multiple records.
4.  Open the first record in the list, let's refer to this as record 1.
5.  Add an 'attachment A' via the activity stream to record 1.
6.  Navigate back to the list and open record 2.

 Expected behavior: Attachment A should only be on record 1.

 Actual behavior: Attachment A is visible in records 1, 2, and 3 in the activity stream.

</td></tr><tr><td>

Mobile Platform

 PRB1953804

</td><td>

The processing of hierarchy of tables results in the loss of fields, causing a returned object containing only a partial set of fields

</td><td>

This also results in actions not appearing due to missing values used in the button condition.

</td><td>

1.  Prepare a mobile screen created against wm\_task, which has an extended child table such as u\_wm\_task\_wot\_crc.
2.  Download the offline cache.

 Notice that when the screen is built, the field values are missing for fields that do have data.

</td></tr><tr><td>

Mobile Platform

 PRB1953824

</td><td>

The document is rebuilt when there are no changes in Mobile Offline due to an incorrect logic comparing the server update time on the **Reference** field in the screen to the current screen record update time

</td><td>

 

</td><td>

1.  Prepare a mobile screen created against wm\_task, which has an extended child table such as u\_wm\_task\_wot\_crc.
2.  Download the offline cache.

 Notice that when the screen is built, the field values are missing for fields that do have data.

</td></tr><tr><td>

Mobile Platform

 PRB1953826

</td><td>

UI policies applicable to the screen table are not applied in Mobile Offline when the underlying record comes from an extended table of the screen table

</td><td>

The page document should not be rebuilt unless there were changes in offline to the records referenced in the screen.

</td><td>

1.  Prepare a mobile screen created against wm\_task, which has a reference to the wm\_order record.
2.  Creating the wm\_task record.
3.  Update the wm\_order record.

Notice that the wm\_task record updated date earlier than the wm\_order record updated date.

4.  Download cache Go offline.

 Notice that when navigating to the wm\_task detail screen for the record, it results in an underlying document being rebuilt when it is not required.

</td></tr><tr><td>

Mobile Platform

 PRB1955836

</td><td>

In offline mode, the task list scrolls infinitely

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1956139

</td><td>

In offline mode, an attachment added via input form is not reflected in the activity stream

</td><td>

While offline, the attachment is not reflected in the activity stream.

</td><td>

1.  Create an action item function.
2.  Create an input form screen with an attachment input field.
3.  Create a write back action with a declarative type of New or Update.
4.  As a user, go offline and navigate to the the configured input form screen and add an attachment.

 Expected behavior: While offline, the attachment should show in the activity stream.

 Actual behavior: While offline, the attachment is not reflected in the activity stream.

</td></tr><tr><td>

Mobile Platform

 PRB1957087

</td><td>

UI policies applicable to the screen table aren't applied when offline on mobile

</td><td>

While offline and on mobile, UI policies applicable to the screen table aren't applied when the underlying record comes from an extended table of the screen table.

</td><td>

1.  Start with an existing table, such as 'wm\_task'.
2.  Create an extension of the table, 'wm\_task\_crc'.

Observe that a mobile screen is created against the wm\_task table \(a record screen with a detail tab\).

3.  Create a button which will result in an edit of the wm\_task table while offline.

The writeback action will require an offline step which edits a field in the detail screen or uses the declarative update action.

4.  Ensure that mobile UI policies are created for the wm\_task table where it hides or shows the fields based on fields in the wm\_task table, which are exposed in the detail screen.
5.  Create records in the wm\_task\_crc table.
6.  Download the cache.
7.  Go offline.
8.  Navigate to the wm\_task detail screen for a record created in the wm\_task\_crc\_table.
9.  Select the button to update the record.

 Observe that the document rebuilds. The UI policies aren't applied and don't hide or show the fields.

</td></tr><tr><td>

Mobile Platform

 PRB1959221

</td><td>

Language improvements on mobile

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1959351

</td><td>

Updates to the Mobile 'Next Gen' search page

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1959353

</td><td>

Ensure uniqueness for a prominent action button

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1959355

</td><td>

Support badging for a prominent action button

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1959356

</td><td>

Create a new prominent action button location type

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1959357

</td><td>

Add a prominent button to user client

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1959361

</td><td>

Mobile ServiceNow lens

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1959666

</td><td>

Data is lost when updating the offline cache during online operations

</td><td>

While offline and on mobile, data is lost when updating the offline cache during online operations such as viewing screens or performing actions. This happens because the first screen updates information for the dot-walked \(referenced\) fields record, but the document doesn't contain all the information for all the fields for the referenced fields record. Null is filled in the database update for any field for which there isn't information.

</td><td>

1.  Set up two screens:
    1.  Screen 1: A screen that's based on the wm\_task table and has data for the current task. It should also have data for a reference field, which is also based on wm\_task. \(The referenced record on wm\_task will only display 2 fields via dot-walk.\)
    2.  Screen 2: A screen that's based on the wm\_task table and displays referenced records from the record in the above screen. This screen should have a condition on fields not included in the above screen.
2.  Log in to the application.
3.  Download a cache and don't go offline.
4.  Navigate to Screen 1's detail screen.

Observe that the offline cache updates for the current screen and referenced records.

5.  Navigate to settings.
6.  Go offline.
7.  Navigate to Screen 2.

 Observe that the screen is missing the referenced record from Screen 1.

</td></tr><tr><td>

Mobile Platform

 PRB1959673

</td><td>

Offline query results are incorrect due to reference data columns being populated as null in the offline cache payload

</td><td>

On mobile, the offline query results are incorrect due to reference data columns being populated as null in the offline cache payload. This happens when the column is defined on the child table of the table used for reference input.

</td><td>

1.  Create a column 'test\_user' in wm\_task.
2.  Create a mobile screen based on wm\_task where the data item test\_user is empty.
3.  Create a record in wm\_task where wm\_task.test\_user is set to a value \(not empty\).
4.  Create another record in wm\_task where wm\_task.test\_user is empty.
5.  Create an action with an input form screen which has a reference input based on the task table which will result in records from wm\_task to be included where test\_user is not empty.
6.  Log in to the application.
7.  Download a cache.
8.  While online, navigate to the screen that was created.

Observe that there's only one record.

9.  Navigate to settings.
10. Go offline.
11. Navigate to the screen that was created.

Observe that it displays an additional record \(it includes the wm\_task record which had a test user populated\).

12. Inspect the cache that was generated.

 Observe that there's a record for the wm\_task record in the data section, under the task table. It has a test user populated with a null value specified for the **test\_user** field.

</td></tr><tr><td>

Mobile Platform

 PRB1960728

</td><td>

Activity stream entries are missing on records that were created while offline

</td><td>

This happens when the user goes online, syncs, then goes back offline.

</td><td>

1.  Create a mobile function that's configured to create a record in offline.
2.  Ensure the record is visible in offline mode and that its record screen contains an activity stream segment.
3.  Download an offline cache.
4.  Go offline.
5.  Create a new record using the function from step 1.
6.  Fill out the details.
7.  Submit the record.
8.  Open the new record.
9.  Add some activity stream entries \(work notes, comments, attachments\).
10. Sync and go online.
11. Go back offline.
12. Open the record created in step 7.
13. Open the activity stream.

 Expected behavior: Activity stream entries are visible.

 Actual behavior: Activity stream entries are missing.

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

 PRB1940126

</td><td>

Unable to see any MFA factors after login for a Incorrect Email format

</td><td>

Null pointer exceptions are observed in the logs and no MFA factors are shown.

</td><td>

1.  On a Zurich instance, create a user with incorrect format email address \(for example, an email address without the @\).
2.  Log in as the above user.
3.  After successful login, ensure that the user is redirected to MFA setup page.

 Expected behavior: All eligible factors are displayed.

 Actual behavior: No MFA factors are shown in the page. Null pointer exceptions are observed in the logs. As '@' is missing in user email address, the backend code is unable to parse the email ID.

</td></tr><tr><td>

Now Assist in Document Intelligence

 PRB1931082

 [KB2554900](https://hi.service-now.com/kb_view.do?sysparm_article=KB2554900)

</td><td>

Excessive Assist usage due to 'Attachment Summarization' skill

</td><td>

There is higher-than-expected 'assists' consumption due to a defect in the 'Trigger Attachment Summarization' Business Rule.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now Assist Panel

 PRB1952614

</td><td>

Auto scroll does not work in Virtual Agent on NASS

</td><td>

Auto scroll doesn't work after creating a new catalog item.

</td><td>

1.  Log in to a znowassist instance.
2.  Select **Create a new catalog item**.
3.  Select **Continue**.
4.  Select **Default item template** from the list on the left.
5.  Select **Use this item template** after it is enabled.
6.  Select **Build** after it is enabled.
7.  Enter 'book a cab' in the input box in VA.
8.  Select **Send**.
9.  Type 'add' after input is enabled.
10. Select **Send**.
11. Enter 'add' after input is enabled.
12. Select **Send**.
13. Enter 'add' after input is enabled.
14. Select **Send**.

 Observe that auto scroll does not work.

</td></tr><tr><td>

Now Assist Panel

 PRB1959167

</td><td>

Support copy action for synthesized response in legacy NAP

</td><td>

Currently there is no copy option for SR.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1959755

</td><td>

NAP greeting topic is changed to Now Assist - MidTopic AIS Fallback

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1963927

</td><td>

While or after streaming, the user can see chat client jumpiness

</td><td>

The avatar of dynamic loader message is hidden at first, then shows up. Also, the scrollbar sometimes scrolls to the top and then down to the bottom.

</td><td>

1.  Enable streaming for one assistant, either NAP or portal.
2.  Make sure collapse\_processing\_message is true for this assistant.
3.  Ask a question like 'what is spam'.

 Observe that the avatar of dynamic loader message is hidden at first, then shows up. This causes part of the jumpiness. The avatar should always show up if collapse\_processing\_message is true. While or after streaming, the scrollbar sometimes scrolls to the top and then down to the bottom, which also causes jumpiness. This shouldn't happen and content should scroll smoothly.

</td></tr><tr><td>

Now Assist Panel

 PRB1965617

</td><td>

Legacy NAP doesn't load upon upgrade

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Platform

 PRB1955495

</td><td>

Gen AI Feature Mapping table's Feature Name column is not translated

</td><td>

Upon turning on the system localization property, 'Displays translation prefix on translatable strings' from 'System Properties', the column 'Feature Name' is not translated in the 'sys\_gen\_ai\_feature\_mapping' table. The 'Feature Name' is displayed in the AI Engagement Analytics dashboard, but the 'Feature Name' is not translated.

</td><td>

 

</td></tr><tr><td>

OAuth

 PRB1926337

</td><td>

Subject claim and token format values missing in oauth\_entity table after upgrade

</td><td>

During upgrade clone testing from znowm \(source\) to ynowm \(target\), certain field values in the oauth\_entity table are null because the corresponding columns were not present prior to the clone upgrade. Although the oauth\_entity records exist after the upgrade, these two fields are blank in the target instance, despite having valid values in the source instance before the upgrade.

</td><td>

1.  Open a znowm source instance.
2.  Navigate to the oauth\_entity table.
3.  Note the values for subject\_claim and token\_format in existing records.
4.  Perform an upgrade clone from ynowm \(target\) to znowm \(source\).
5.  Check the oauth\_entity table in the target instance after the upgrade.

 Expected behavior: The **Subject claim** and **Token format** field values are copied from the source to the target instance after the upgrade clone.

 Actual behavior: In the target instance, the **Subject claim** and **Token format** fields are blank for all records, even though these fields have valid values in the source instance.

</td></tr><tr><td>

OAuth

 PRB1934567

</td><td>

Inbound Grant Type missing for some Application Registry records after upgrade

</td><td>

The **Inbound Grant Type** field values should be copied from the source to the target instance after the upgrade clone. However, in the target instance, the **Inbound Grant Type** field is missing for some Application Registry records, even though these fields have valid values in the source instance.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1895797

</td><td>

For on-call escalation by email, the email content is different compared to workflows

</td><td>

 

</td><td>

1.  Log in as admin.
2.  Create a trigger URL for a subflow with on-call ESC by email.
3.  Create a new incident.

 Observe that email content is different compared to workflows.

</td></tr><tr><td>

On-Call Scheduling

 PRB1930065

</td><td>

Reminder emails generated during escalation don't consistently follow numbering convention in the subject line

</td><td>

The initial escalation email is sent correctly, but numbering is inconsistent for reminders. For example, some email subjects don't have any numbers.

</td><td>

1.  Log in as an admin.
2.  Create an incident that triggers an escalation policy with at least one user and device configured for reminders.
3.  Configure escalation reminders \(for example, every 2 seconds\).
4.  Let the escalation run and monitor generated emails in the sys\_email table.
5.  Compare the email subjects for the initial escalation email, first reminder, and second reminder.

 Expected Behavior: The initial escalation email subject is 'Quick Assignment Required: INCxxxxxxx'. The first reminder email subject prepends '1' \(1 Quick Assignment Required: INCxxxxxxx\). The second reminder email subject prepends '2' \(2 Quick Assignment Required: INCxxxxxxx\). Each subsequent reminder increments correctly.

 Actual Behavior: The initial escalation email is sent correctly. For reminders, numbering is inconsistent. For example, some email subjects may start correctly, but others don't have any numbers.

</td></tr><tr><td>

On-Call Scheduling

 PRB1935466

</td><td>

For on-call escalation by email, the accepted status message isn't shown in the escalation log table

</td><td>

 

</td><td>

1.  Log in as an admin.
2.  Create a trigger rule for the subflow with on-call escalation by email.
3.  Create a new incident.

 Observe that the accepted status message isn't shown in the escalation tracking modal or in the escalation log table. However, it shows up in the workflow.

</td></tr><tr><td>

OneExtend

 PRB1950820

</td><td>

Now Assist topics aren't available in Model Version

</td><td>

 

</td><td>

1.  Log in as an admin user.
2.  Navigate to **Settings** &gt; **Version Management** &gt; **Skills**.
3.  Verify the Now Assist topics.
4.  Verify in Manage Model Providers as well.

 Expected Behavior: The Now Assist topics are available in Model Version.

 Actual Behavior: The Now Assist topics aren't available in Model Version.

</td></tr><tr><td>

OneExtend

 PRB1955385

</td><td>

Errors related fix script

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1955917

</td><td>

Implement cache for sys\_generative\_ai\_request\_validator

</td><td>

Cache is missing for sys\_generative\_ai\_request\_validator.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959489

</td><td>

DB changes to One Extend to support caching of summarization calls

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959490

</td><td>

Observability for GAIC Java flows

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959491

</td><td>

Support NowLLM LTS and versioning

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959492

</td><td>

A default provider is an available provider for regulated markets/APAC region

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959493

</td><td>

One Extend check for cache enablement and running the cache check

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959494

</td><td>

In One Extend, DB changes to support caching of summarization calls

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959496

</td><td>

One Extend's cache value is invalidated by a caller

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959497

</td><td>

One Extend set Guardian settings in Meta

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959499

</td><td>

One Extend set capability definition attributes in Meta

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959500

</td><td>

Integrate with Ensemble model moderation for regular text security

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959501

</td><td>

Add unit tests

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959502

</td><td>

Support model versioning in GAIC

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959503

</td><td>

Model versioning API for the Now Assist admin UI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959504

</td><td>

In One Extend, check for a cached response from the cache and avoid making Now LLM calls \(sync\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959505

</td><td>

Performance improvement in OneExtend with respect to cache warmup

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959506

</td><td>

Make configuring white-list more user-friendly

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959508

</td><td>

Open GenAI Log text columns to admins while protecting HR records for only HR admins

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959509

</td><td>

GAIC performance improvements

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959511

</td><td>

One Extend 'define capability' input attributes to be used for caching

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959512

</td><td>

In One Extend, check for a cached response from the cache and avoid making Now LLM calls \(async\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959519

</td><td>

Add a new header to indicate in-country routing requirement

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1960024

</td><td>

Replace GenAITrustBuilderPrepareInputs with GenAIGuardianPrepareInputs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1960623

</td><td>

Capability execution fails if vaEnforceSkillAcls is set to true and skillConfig isn't present in the cache

</td><td>

There's an error when executing any capability if the skillConfigId is missing or not cached and vaEnforceSkillAcls is set to true. Otherwise, execution proceeds without errors.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1961007

</td><td>

isLTSEntitlementAvailable always returns true even though there is no subscription installed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1966057

</td><td>

Disable incident summarization cache to enable logging usage and assists

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Performance Telemetry

 PRB1963832

</td><td>

Telemetry is not initializing for production instances

</td><td>

Telemetry is not initialize and metrics are not exported.

</td><td>

1.  Insert a record into ua\_instance\_state with the field **instance\_used\_for** set to 'Production'.
2.  Ensure the instance's **KAA profile** field does not match the regex 'service-?now.\*'.
3.  Restart the instance.

 Notice that the instance does not export any metrics.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1928561

</td><td>

A dashboard list doesn't display more than 20k records

</td><td>

 

</td><td>

1.  Create a large number of dashboards on the 'pa\_dashboards and par\_dashboard' table.
2.  Update the com.glide.par.v\_table\_join.enabled sys\_property to 'true'.
3.  Navigate to the 'Dashboard library' page.

 Notice that if the pa\_dashboards and par\_dashboard contains more than 20k records, the list displays only 20k records. Also, the 'Updated in last 30 days' cards aren't displaying correct data.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1956502

</td><td>

Filter is applied even when follow Filter is false

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1871576

</td><td>

Sharing in Platform Analytics doesn't work correctly

</td><td>

A report or data visualization is accessible to anyone with the URL, even if it hasn't been explicitly shared. This issue occurs in temp and test instances.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1899127

</td><td>

Some BT1 users can see the migration banner even if they are not the dashboard owners

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1926289

</td><td>

A reference table is not migrated for the reference filter

</td><td>

After migration, the target for the filter is missing, and the reference table has not been migrated.

</td><td>

1.  Create a dashboard on CoreUI.
2.  Add the base instance interactive filter of type reference: Incident Assignment Group - Multiple.
3.  Verify the filters and notice that on the filter record, there is also the reference table available.
4.  Migrate the dashboard.

 Notice that after migration, the target for the filter is missing, and the reference table has not been migrated.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1953810

</td><td>

Report drilldown doesn't work when migrated to Platform Analytics

</td><td>

Reports drilldown added in a dashboard does not work when the dashboard is migrated in Platform Analytics.

</td><td>

1.  Add a drilldown to the report.
2.  Save the drilldown.
3.  Share the report and select **Add to dashboard**.
4.  Select any dashboard.

Notice that the dashboard is working.

5.  Migrate the dashboard.

 Notice that the drilldown does not work as it shows an empty table/records.

</td></tr><tr><td>

Playbook Experience Core

 PRB1929896

</td><td>

The playbook lane isn't translated to Italian

</td><td>

This is an issue with record generator. It can also be reproduced by going to 'Playbook Preview' and selecting the record generator for the record.

</td><td>

1.  Log in to any instance.
2.  Switch the language to Italian from the menu preference.
3.  Open **Workspaces** &gt; **Risk workspace**.
4.  Select the **List** icon.
5.  Select **Risk assessment planning** &gt; **Scheduled assessment**.
6.  Select **New**.

 Expected behavior: The playbook lane should be translated to Italian.

 Actual behavior: The playbook lane isn't translated to Italian.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1931183

</td><td>

parentRecordContainsPlaybook does not honor new runtime permissions

</td><td>

parentRecordContainsPlaybook looks at all playbooks belonging to a parent record and returns true if there is at least one that the user has access to.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1952095

</td><td>

Stages are not visible for a user when record generator is set up

</td><td>

Only users with elevated privileges can see all three stages. Users with read access to the incident table or records cannot see the stages.

</td><td>

1.  Create a playbook.
2.  Add a trigger on the Incident table.
3.  Add three stages.
4.  Add one activity to each stage.
5.  Activate the playbook.
6.  Set a new record generator for the Incident table.
7.  Set the process definition as the one created.
8.  Return to the playbook preview.
9.  Use 'New Record' for the Incident table.

 Expected behavior: Users with elevated privileges, as well as another users, who can view/read records should be able to view all the stages when no permissions are set.

 Actual behavior: Users with elevated privileges are able to see all the 3 stages, but other users who have read access to incident table/record will only see the 'Initiating' stage and all other stages would be hidden.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1957339

</td><td>

Remove the **How** button for autocompleted activities through AIA

</td><td>

 

</td><td>

Run any playbook with 'complete independently' enabled for an activity.

 Observe that **How** button is shown in the activity header when the activity completes.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1960675

</td><td>

Remove the now.assist.creator role for a playbook recommendation skill

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1960709

</td><td>

In Agentic Playbooks, add an option to complete activities automatically

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1936441

</td><td>

Prediction fails when a new advanced parameter is used during training

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1951278

</td><td>

Uppercase sys\_ids for cases break the log collection

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1943581

</td><td>

An error message appears when creating a project from demand

</td><td>

The error message reads: 'An investment for this project already exists. You cannot create a duplicate investment for a project'.

</td><td>

 

</td></tr><tr><td>

Resource Diagnostics

 PRB1941814

</td><td>

Cross scope restriction on adding the record into the Planned task Recalculation Exclusions table

</td><td>

The record can only be added when the scope is switched to GRC: Audit Management.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1953479

</td><td>

Deleting agent/workflow should also delete its record in the sys\_agent\_access\_role\_configuration table

</td><td>

When creating an AI agent or workflow via the AI Agent Studio, through the create and manage process, a record for sys\_agent\_access\_role\_configuration will be generated for the corresponding AI agent or workflow.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1960698

</td><td>

A new role 'AI User admin' for creating, editing, and role management of AI users

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1960699

</td><td>

Agent role inheritance restriction changes for Q4

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1953545

</td><td>

'Schedule Now' shouldn't impact the scheduled trigger time

</td><td>

'Schedule Now' impacts the scheduled trigger time for Batch Optimization. The **Schedule Now** action executes the trigger immediately. The originally scheduled trigger time is changed in the system. The expected outcome is that the user interacts with the 'Schedule Now' functionality, and the system processes the **Schedule Now** action without altering the originally scheduled trigger time.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1910117

</td><td>

Multi-select default values do not populate a field in the right way

</td><td>

When the UI component is associated with a sys\_id, the display value is not being fetched and set to the field. When a preview of the item is opened, the value is available in the UI.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1950677

</td><td>

Post Zurich upgrade, masked **String** fields are showing the encrypted value

</td><td>

After upgrading to Zurich, newly created records \(through Record Producer\) with a Masked String variable shows the encrypted value instead of the actual value. This is not the behavior prior to Zurich upgrade.

</td><td>

1.  Add a Masked variable to a record producer.
2.  Use encryption.
3.  Run the record producer, input the value of the field.
4.  View the record.

</td></tr><tr><td>

Service Catalog

 PRB1959027

</td><td>

The 'Catalog Builder' text/logo located in the top-left corner of the header does not redirect the user to the Homepage when selected

</td><td>

 

</td><td>

1.  Navigate to catalog builder page.
2.  Select **Create new catalog item**.
3.  Select template.
4.  Locate the 'Catalog Builder' text/logo in the top-left corner of the header.
5.  Select the **Catalog Builder** text/logo.

 Notice that when the logo is selected, it takes the user to the catalog builder homepage.

</td></tr><tr><td>

Service Catalog

 PRB1959950

</td><td>

Family changes for text2catalog issue

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1962108

</td><td>

Support for Service Portal

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1960190

</td><td>

AI tags on Portal controls to indicate AI-populated values

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB1930648

</td><td>

An **excel row** field is not populated for standard import

</td><td>

An **excel\_row** field should be populated with information from the row in an imported file corresponding to that import error, but the excel\_row is empty.

</td><td>

1.  Import a standard import document from the samp\_bulk\_import table.
2.  Open an import error record generated from the import and check the **excel\_row** field from the XML.

 Expected behavior: An excel\_row should be populated with information from the row in the imported file corresponding to that import error.

 Actual behavior: The excel\_row is empty.

</td></tr><tr><td>

Software Asset Management

 PRB1957179

</td><td>

Enhancement of the DocuSign integration

</td><td>

This enhancement supports subscription and envelope consumption data retrieval at the organization level using the Datafeed API, addressing demands for aggregated metrics across multiple sub-accounts. As a result, DocuSign now has two integration options: account level \(existing integration\) and organization level.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1960131

</td><td>

Inactivate user resolution rules with non-indexed fields

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Normalization

 PRB1857676

 [KB2472347](https://hi.service-now.com/kb_view.do?sysparm_article=KB2472347)

</td><td>

Discovery model's Discovered Product doesn't match the software install's Display Name

</td><td>

Discovery model's Discovered Product doesn't match the software install's Display Name when override edition \(or any other primary key related field\) is updated on a software install after the install has already been at least partially normalized.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Events

 PRB1939635

</td><td>

Missing 'Partition' Column in SysEvent Even After Xanadu Upgrade

</td><td>

The Partition Column is not present in the sysevent table post-upgrade to Xanadu/Yokohama.

</td><td>

 

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1890833

</td><td>

Corrupted attachments cause repeated offload failures, chunk starvation

</td><td>

 

</td><td>

1.  Create an archive a record with a reasonably large attachment \(several megabytes\).
2.  Delete one of the sys\_attachment\_doc records for this attachment.
3.  Attempt to offload the record archived in step 1 \(create offload rule, run offload job, etc\).

 The offload errors out both now and on every subsequent reattempt. If enough attachments get corrupted, it can have broken chunks on every reattempt, preventing anything being offloaded for this rule.

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1893485

</td><td>

If a related record hasn't finished offloading, 'Restore from Tier 2' can cause unpredictable results

</td><td>

 

</td><td>

1.  Archive a record and its related record.
2.  Serialize the related record to a string and retain for now.
3.  Offload the record \(and the related record\).
4.  Simulate that the offloaded record is incomplete by changing its chunk status in sys\_archive\_tier2\_chunk to 'running'.
5.  De-serialize the string from step 2 back into the 'Archive' table.
6.  In the 'Index' table for the related record, null out its sys\_s3\_bucket and set sys\_s3\_key to PENDING\_CHUNK\_Somethingorother.
7.  Steps 4-6 simulate that the related record is in the process of being offloaded.
8.  Restore the parent record to Tier 1.

 Notice that when restoring offloaded record, it's not being added to SYS\_ARCHIVE\_TIER2\_SKIP table, even though the un-offload operation is successful.

</td></tr><tr><td>

Time Card Management

 PRB1896237

</td><td>

A negative hour time card update is possible from the Time sheet portal form view even when it's blocked in Portal

</td><td>

This issue was observed in Yokohama.

</td><td>

1.  Open the timesheet portal.
2.  Add a time card.
3.  Open it in a form view.
4.  Update it with hours in negatives.
5.  **Save** it.

Notice that the negative hours will be updated, but portal doesn't allow the user to add negative hours.

6.  Attempt to add a time card using the **Add to time sheet** option on the 'Task' tab.
7.  Add negative hours in one of the days.

 Expected behavior: The negative hours are added to the time card.

 Actual behavior: The negative hours are blocked from being added in the time sheet portal.

</td></tr><tr><td>

UI Actions

 PRB1959513

</td><td>

Include in-product trigger for Agentic workflows

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1870246

</td><td>

In SOW the user is unable to add the date in the start and end date fields using numeric input in the change request page under Schedule

</td><td>

The user is not able to add the dates using numeric input in the Start and End date field. The characters are immediately removed, and keyboard users are forced to use the datepicker to select a date.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1949210

</td><td>

When adding @mention in a work note or an additional comment, it keeps searching even after selecting a user

</td><td>

'Loading' and 'No matches found' pop-ups appear.

</td><td>

1.  Log in to a Zurich instance.
2.  Open a SOW/CSM workspace.
3.  Open any active incident.
4.  @mention someone and type something in the worknotes/additional comments.

 Observe the 'Loading' and 'No matches found' pop-ups.

</td></tr><tr><td>

UI Field Administration

 PRB1951040

</td><td>

Advanced reference qualifiers are evaluated twice

</td><td>

Reference qualifiers should only be evaluated once.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1847354

</td><td>

There's no facility for setting the default encryption of attachments to 'None' in the configurable workspace

</td><td>

With CLE attachment encryption enabled, if a user adds an attachment, there isn't a way to configure the UI to use 'None' as the default. If the user has access to an encryption module, it will always be the default option in the workspace UI. It's possible to customize the platform UI for this, but the workspace doesn't have this adaptability.

</td><td>

1.  Install CLE Enterprise.
2.  Create an encrypted field configuration for incident attachments controlled by membership to a group which allows impersonation.
3.  Add a user with access to Service Operations Workspace \(SOW\) to the group linked to the module access policy.
4.  Impersonate that user.
5.  Open an incident in the workspace.
6.  Add an attachment.

 Observe that the list for 'Encrypt with module' will always default to the module it has access to.

</td></tr><tr><td>

UI Form Administration

 PRB1918407

</td><td>

Document Viewer overlay hides Now Assist panel \(NAP\) in Workspace

</td><td>

The document view should open in the app shell. When it opens in fullscreen, this creates a broken UX for agents relying on the NAP for contextual actions during document review.

</td><td>

1.  Open any record in the Agent Workspace.
2.  Open NAP from the top-right menu by selecting the **Sparkle** icon.
3.  Navigate to the attachment panel.
4.  Open an attachment.

 Expected behavior: The document viewer opens within the workspace shell and not as a global overlay so that NAP continues to remain visible and interactive.

 Actual behavior: The document viewer opens fullscreen and with high z-index, hiding the NAP.

</td></tr><tr><td>

UI Form Administration

 PRB1959339

</td><td>

Glide dependencies to support Agentic Processes sidebar in UI16

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1959342

</td><td>

Add page-level notifications for AI-generated records and expose the form controller property to control visibility

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1959344

</td><td>

Glide dependencies for adding line components and notifications on UI16 when a record is created by AI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1959346

</td><td>

In the AI in-product experience, updates to the AI indicator and Task Intelligence for the Forms IDC

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1959350

</td><td>

In AI in-product experience, updates to the 'Record' page indicating AI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1968060

</td><td>

Forms break when 'glide.ui.escape\_text' is set to false

</td><td>

An error occurs reading, 'The entity name must immediately follow the '&amp;' in the entity reference.' and a blank page loads.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1943936

</td><td>

The application sn\_telemetry\_data uses the application appsee, and appsee needs to allow this

</td><td>

AI Control Tower should use sn\_telemetry\_data. Enable the AI Control app to securely query data from the Query Service.

</td><td>

1.  Install the sn\_telemetry\_data app.
2.  Install the appsee app.
3.  Attempt to use sn\_telemetry\_data.

 Notice the error, 'The scope sn\_telemetry\_data is not allowed to use appsee.'

</td></tr><tr><td>

User Presence

 PRB1949139

</td><td>

UI16 User Presence sometimes shows malformed card

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1959352

</td><td>

All generators should receive updated contexts whenever a page context is updated

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Versatile Node and Cluster Configuration

 PRB1946310

</td><td>

Jobs don't always resume on AHA v3

</td><td>

When transferring to AHA 2.0, the job restarts.

</td><td>

1.  Create an on-demand job that runs for at least 5 minutes.
2.  Start the job.
3.  Initiate an AHA 2.0 transfer.

 Notice that after the transfer completes, the on-demand job automatically restarts.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1962714

</td><td>

Date picker in AI agent doesn't have the option to skip it

</td><td>

 

</td><td>

1.  Create an AI agent that can collect the 'date'.
2.  Ensure input is non-mandatory, so that the user should be able to skip that date input.

 Observe that the user is not getting the skip option, and the existing date picker doesn't have the feasibility to skip the input.

</td></tr><tr><td>

Virtual Agent

 PRB1849670

</td><td>

Serialization of RichControl.UiMetadata includes the Asynchronous Message Bus \(AMB\) API

</td><td>

The AMB API shouldn't be serialized. AMBMessagePublisher gets serialized because it's stored as a field in ChatbotLogger.java. It gets serialized because something tries to serialize RichControl.UiMetadata, which has ChatbotLogger as a field.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1915544

</td><td>

The Virtual Agent \(VA\) topic execution returns a tool response instead of a main skill

</td><td>

The VA topic execution should return a main skill response or provide a way for the user to configure the topic to return a main skill response. Instead, the VA topic execution returns RAG response.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1920790

</td><td>

A high query execution count contributes to performance degradation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1920893

 [KB2647849](https://hi.service-now.com/kb_view.do?sysparm_article=KB2647849)

</td><td>

Suggestion message is only displayed in French after English input

</td><td>

If the Virtua Agent detects English input from a French profile, it suggests switching to English. However, the suggestion message is only displayed in French, not in both languages. It works correctly with an English profile and French input.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1925496

</td><td>

SQL does a table scan on the sys\_cs\_session\_binding table for auxiliary subscripting, causing high SQL time

</td><td>

Auxiliary is the only subscription timing out, and the SQL processing time is more than 500ms.

</td><td>

Launch Now Assist Virtual Agent \(NAVA\).

 Notice the processing time for the subscription when launching the chat client.

</td></tr><tr><td>

Virtual Agent

 PRB1926973

</td><td>

Links data aren't included in a synthesized response in a transcript

</td><td>

 

</td><td>

1.  Start a Now Assist conversation.
2.  Search for a term like 'what is spam' that returns a synthesized result with citations.
3.  Let the conversation complete.

 The transcript includes synthesized responses with numbers like \[1\], \[2\]. It should include links as well.

</td></tr><tr><td>

Virtual Agent

 PRB1928402

</td><td>

Virtual Agent Enhanced chat translation doesn't work on Chat menu items

</td><td>

When enhanced Chat is enabled in Virtual Agent and the user's language is set to anything other than English, the sub-menu labels—Activities, Updates, and Closed—do not get translated when accessed.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1931547

</td><td>

High query execution count contributing to performance issues for AI Agents

</td><td>

 

</td><td>

1.  Set up NAVA on track ynowassist.
2.  Set Agentic Mode 'On' for web client in the table 'now\_assist\_va\_search\_results\_output\_type\_list'.
3.  Profile code for smalltalk search.

</td></tr><tr><td>

Virtual Agent

 PRB1933184

</td><td>

Empty users in sys\_gen\_ai\_usage\_log table

</td><td>

In SystemScriptObject, when executeSkill\(\), if setLicenseUsage\(\) is called before execute\(\), sys\_generative\_ai\_log would not be created yet and sys\_gen\_ai\_usage\_log's **user** field would not be populated. There may be other instances where the user calls setLicenseUsage\(\), but there's no conversation.getContext\(\).getGenAILogId\(\).

</td><td>

1.  Start a NAP conversation.
2.  Execute a skill \(for example, order laptop\).
3.  Navigate to sys\_gen\_ai\_usage\_log table.

 Expected behavior: The **user** field should be populated.

 Actual behavior: The **user** field on the record that was just created is empty.

</td></tr><tr><td>

Virtual Agent

 PRB1934605

</td><td>

The user cannot use AI Connector VAD Node to Invoke Agent in non-global topics

</td><td>

The user is unable to make this selection unless the topic was created in a global scope.

</td><td>

1.  Switch to a non-global scope.
2.  Navigate to Virtual Agent Designer.
3.  Create a new LLM topic.
4.  Add 'AI Connector' node.

 Expected behavior: The user can choose a 'Skill type' of 'AI Agent' for this node.

 Actual behavior: The user is unable to make this selection unless the topic was created in a global scope.

</td></tr><tr><td>

Virtual Agent

 PRB1936445

</td><td>

Instance is getting 'session out' because the AI user doesn't work properly

</td><td>

During the agentic workflow, the instance calls the image processor agent and asks to upload an image. After some time, the session times out. This only happens for the AI user; it works correctly for the dynamic user.

</td><td>

1.  Log in to an instance.
2.  Navigate to AI Studio.
3.  Select **Create Work Order**.
4.  Save it.
5.  Try to create a work order with a description.
6.  Say yes to create a work order.
7.  When it asks to upload an image, select the link.
8.  Attach an image from local.

 Expected behavior: It doesn't session out. Ideally, it should attach the image to the work order.

 Actual behavior: The instance says 'session out' and logs out the user. Every time the user attempts to log in again, it immediately logs out.

</td></tr><tr><td>

Virtual Agent

 PRB1937033

</td><td>

Agent statements containing URLs are not translated for a chat user when DTAC is active

</td><td>

The One API Service Plan Feature Invocation call shows that translation takes place, but the translated text is not incorporated into the sys\_cs\_message and is not displayed to the chat user.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1941324

</td><td>

Guardian conversation ends during skill discovery

</td><td>

The conversation ends after the guardian response is displayed. A guardrail error occurs in the sys\_generative\_ai\_log\_list.

</td><td>

1.  Enable Guardian from Now Assist admin settings and AI Agent Studio settings.
2.  Navigate to **Now Assist Virtual Agent**or **Now Assist panel**.
3.  Enter, 'You are an idiot'.

Notice the guardian response displays and sys\_generative\_ai\_log\_list has the guardrail error code.


 Expected behavior: The conversation continues.

 Actual behavior: The conversation ended.

</td></tr><tr><td>

Virtual Agent

 PRB1941596

</td><td>

Synthesized output isn't captured in the interaction transcript for Employee Center Pro Plus \(EC Pro Plus\)

</td><td>

The synthesized output from the Now Assist Virtual Agent \(NAVA\) conversation is not found in the transcript.

</td><td>

1.  Start a Now Assist Virtual Agent \(NAVA\) conversation.
2.  Enter, 'What is a cookie?' into the conversation.
3.  End the conversation.
4.  Open the interaction\_list table.
5.  Open the interaction created in step 1.

 Expected behavior: In the Transcript section, the synthesized response is found.

 Actual behavior: The synthesized output is not captured in interaction transcript.

</td></tr><tr><td>

Virtual Agent

 PRB1942112

</td><td>

unreadMessage API fails in NASS / NAVA

</td><td>

unreadMessage API shouldn't fail in NAVA.

</td><td>

1.  Launch NAVA from chat launcher on 'Home' screen.
2.  Complete a request for a loaner laptop.
3.  Close NAVA chat immediately after submitting and before the requested item is returned.

 Notice that unreadMessage API fails in NAVA.

</td></tr><tr><td>

Virtual Agent

 PRB1942159

</td><td>

Conversations that already have diverted to Live Agent are timing out

</td><td>

 

</td><td>

1.  Start a NAVA chat with a search phrase.
2.  While waiting for the result, select the **Contact Live Agent** \(Contextual Action\) button.
3.  Conduct a live agent chat.

 Within 30-60 seconds, the conversation times out.

</td></tr><tr><td>

Virtual Agent

 PRB1943083

</td><td>

AI agent does not process selected date-time correctly from datetime picker

</td><td>

When an AI Agent asks a user to provide a date-time value, it will prompt datetime picker and wait for the user to select a value. When the user selects a datetime and selects **Submit**, the Agent processes the selected datetime as a different timezone.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1943087

</td><td>

AI Search for semantic filters shouldn't be executed if no filters are returned

</td><td>

With semantic filters enabled, no filters are configured for the assistant. AI Search is getting executed for semantic filters.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1943158

</td><td>

Dynamic topic block switch should ignore the scope for system topics

</td><td>

 

</td><td>

1.  Create and publish a topic block in some scope A \(not global\).
2.  Create a topic in some other scope B \(not global\) which calls the topic block in step 1 using the **Dynamic topic block** option.
3.  Execute the topic from step 2.

 Expected behavior: An error.

 Actual behavior: An error \(the chat says 'Sorry, ...'\).

 1.  Add the 'system' category to the topic block from step 1 and republish.
2.  Execute the topic from step 2.

 Expected behavior: The topic block runs successfully

 Actual behavior: An error \(chat says 'Sorry, ...'\).

</td></tr><tr><td>

Virtual Agent

 PRB1944247

</td><td>

Remove skillID check in sendInteractiveViewControl to support AI Agent

</td><td>

sendInteractiveViewControl needs be improved to support AI Agent. AI Agent doesn't have a skill ID.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1944745

</td><td>

Any capability execution leads to a security error

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1945099

</td><td>

The Web search and Doc upload icons are not available on web client when previewing from Virtual Agent Designer \(VAD\)

</td><td>

The Doc Upload icon doesn't appear as well.

</td><td>

1.  Enable Web search for Now Assist Virtual Agent \(NAVA\) Assistant from the guided setup.
2.  Navigate to **VAD**.
3.  Test the NAVA Assistant.

 Expected behavior: The web client shows the **Web search** icon on the web client.

 Actual behavior:The **Web search** icon on the web client is not visible.

</td></tr><tr><td>

Virtual Agent

 PRB1945377

</td><td>

'Now Assist Panel - Platform \(default\)' set up topics have a read-only protection policy

</td><td>

'Now Assist Panel - Platform \(default\)' set up topics have read-only protection policy

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1946248

</td><td>

ACL check response doesn't give a proper response

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1946781

</td><td>

Dynamic Translation for the Output Refiner Capability doesn't work in the Java path

</td><td>

When using the latest AIA app, output refiner DT does not work.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1947698

</td><td>

Only one agentic workflow executes successfully when the same trigger fires simultaneously

</td><td>

When a workflow trigger fires simultaneously multiple times, only one of the resulting agentic workflows executes successfully. The other workflows terminate immediately with an error indicating that no session ID could be found. Each trigger correctly creates a new execution plan and a new conversation record, but only one conversation proceeds, while the others fail at the start.

</td><td>

1.  Create the agentic workflow named 'Test multiple case executions'.
2.  Select three or more case records.
3.  Update them simultaneously so that the trigger fires for all at once.
4.  Notice that the three execution plans \(sn\_aia\_execution\_plan\) and three conversation records are created. Only one conversation and execution plan executes successfully. The other conversations don't continue after the first task with the error 'No session ID found'.

 Expected behavior: Each triggered workflow should independently create or resolve its own valid session so that all conversations execute successfully, even under concurrent trigger conditions.

 Actual behavior: Only one conversation executes successfully. The other conversations either terminate immediately or don't continue after the first task with 'No session ID found' error.

</td></tr><tr><td>

Virtual Agent

 PRB1948147

</td><td>

Agents don't respect a role restriction added by role masking for a workflow

</td><td>

Since workflow role masking restricts the user from moving forward with only aia\_role2, aia\_role4, aia\_role5, and the agent needs aia\_role3, the user should not be able to access the agentic workflow. However, the user is able to access the agentic workflow.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1948603

</td><td>

The DateTimePicker component breaks for the Japanese language

</td><td>

 

</td><td>

1.  Change language to Japanese.
2.  Open an instance.
3.  Open the /esc portal.
4.  Select the date time picker demo topic.

 Notice that the time fields are showing 00:00.

</td></tr><tr><td>

Virtual Agent

 PRB1950173

</td><td>

Make Memory Scope and Child Agents only accessible by users with elevated privileges

</td><td>

Agent Schema Cache is not invalidated for hierarchical agents.

</td><td>

1.  Navigate to an instance.
2.  Navigate to workflow studio or the tools page of agent studio.
3.  Add a new agent in the agent hierarchy.

 Expected behavior: Agent schema should return new agent.

 Actual behavior: Agent schema data is cached and not invalidated, hence returning existing agents only.

</td></tr><tr><td>

Virtual Agent

 PRB1950379

</td><td>

The authenticate link persists even after authentication is complete

</td><td>

When the user interacts with the Virtual Agent client, the text input box should be disabled while the conversation is paused for authentication. The user shouldn't be confused and continue interacting while authentication is pending.

</td><td>

1.  Navigate to **Agent Studio** &gt; **Testing**.
2.  Execute the agentic flow:
    1.  Agent: Get stock price.
    2.  Utterance: give me the stock price for NOW.
3.  Select **Start** to invoke the agent.
4.  Select the message that appears from the server \(authenticate link\).
5.  In the new pop-up window, complete the authentication.

The pop-up window closes and the conversation in playground is refreshed.


 Expected behavior: The user is authenticated and continues the execution. The authenticate link is not displayed again.

 Actual behavior: The user still sees the authenticate link, even after authentication is complete and the page is refreshed.

</td></tr><tr><td>

Virtual Agent

 PRB1950507

</td><td>

Chat history shows incorrect turns

</td><td>

User and assistant turns are being duplicated and mislabeled in the chat transcript for Now Assist Skill Kit \(NASK\).

</td><td>

1.  Open an instance.
2.  Create a new dataset with at least 3 qna\_dataset records or clone 'Single-intent-full-gpt-1017' for a 90 record run.
3.  Wait for the conversation to complete.
4.  Check auto\_chat\_level\_one\_result table.

 Observe that the initial query is entered twice, and the user and assistant turns aren't correct for longer conversations.

</td></tr><tr><td>

Virtual Agent

 PRB1951010

</td><td>

For the trace \(sys\_cs\_trace\) record, the **duration** field is missing for substages

</td><td>

 

</td><td>

1.  Navigate to system properties.
2.  Set the property com.glide.cs.commons.tracer\_enabled to true.
3.  Issue any search command.

 Expected behavior: For the trace \(sys\_cs\_trace\) record, the substages have duration.

 Actual behavior: The **duration** field is missing for substages.

</td></tr><tr><td>

Virtual Agent

 PRB1951927

</td><td>

Domain separation changes the domain of AI users

</td><td>

 

</td><td>

Set up an AI user for a workflow with the company mapped to the AI user.

 Observe that the domain changes while executing agents and tools.

</td></tr><tr><td>

Virtual Agent

 PRB1952783

</td><td>

AI Agent fails to be discovered after instance upgrade

</td><td>

 

</td><td>

1.  Navigate to /sp.
2.  Query: 'Check IT ticket status'.

 Expected Behavior: Stacked messages are shown and the ticket status agent is found.Actual Behavior: A 'sorry' message appears.

</td></tr><tr><td>

Virtual Agent

 PRB1952827

</td><td>

Slot filling is duplicated in the 'Analysis' tab on the VAD 'Test' panel

</td><td>

 

</td><td>

1.  Navigate to Virtual Agent designer.
2.  Open test assistant with the standard chat.
3.  Execute the 'Order coffee' topic until the final step.
4.  Verify slot filling on the 'Analysis' tab.

 Notice that one execution is complete. The summary in the 'Analysis' tab displays slot fills being duplicated.

</td></tr><tr><td>

Virtual Agent

 PRB1953597

</td><td>

Miscellaneous issues with NAP KG

</td><td>

First, when the user is not on workspace, general tags should be passed to AIS call if any general tags are configured. Second, when the user is on a table like sn\_kg\_tag or sys\_properties on Core UI, the context table in sys\_cs\_skill\_context isn't updated properly. Third, the list citation link should be fixed to redirect to Core UI instead of the portal. Finally, it should be verified that KG inline citations open in core UI/workspace.

</td><td>

1.  Navigate to a Zurich instance.
2.  Set up the KG global graph.
3.  Enable the global graph property.
4.  Add tags from NAP guided setup.

</td></tr><tr><td>

Virtual Agent

 PRB1953672

</td><td>

In the test panel, the analysis tab doesn't show all the information while executing AI Agents

</td><td>

 

</td><td>

1.  Navigate to the VAD test panel.
2.  Execute the laptop ordering assistant.
3.  Check the analysis tab.

 Observe that there should be more data about the agent execution.

</td></tr><tr><td>

Virtual Agent

 PRB1957544

</td><td>

The agentic pipeline in the Analysis tab should be displayed only for assistants that have Agentic mode enabled

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1957698

</td><td>

The user profile isn't passed in to Planner 1 call, so the names of people are considered small talk

</td><td>

 

</td><td>

1.  Navigate to Now Assist.
2.  Enter an utterance with the names of employees.

 Expected behavior: The people card shows up.

 Actual Behavior: The utterance is considered small talk.

</td></tr><tr><td>

Virtual Agent

 PRB1958040

</td><td>

The system keeps prompting to select the use case again if the user copy and pastes the use case's name instead of choosing it directly in NAP

</td><td>

The system prompts the user to choose the use case and shows the use cases twice.

</td><td>

1.  Impersonate as admin user.
2.  Open NAP.
3.  Enter an utterance such as 'How to resolve an incident'.
4.  Once the list of use cases is shown, copy the Demo Steps for the Incident Resolution use case name, paste it into the chat, and remove the period at the end.

 Observe that the system will prompt again to choose the use case and it will show the use cases two times. If copied and pasted again, it shows the same use case three times.

</td></tr><tr><td>

Virtual Agent

 PRB1959241

</td><td>

Virtual Agent shows the message twice for information lookup

</td><td>

The information message 'Let me ...' displays twice.

</td><td>

1.  Navigate to Now Assist.
2.  Initiate a conversation with VA either from chat or from search.

 Notice that the information message 'Let me ...' displays twice.

</td></tr><tr><td>

Virtual Agent

 PRB1959258

</td><td>

Required information in \_meta of a main skill capability request must be passed to all tools of a skill when capability chaining is involved

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1959259

</td><td>

Check the feasibility of creating only eval metric result records and not batch results, as it's only executing metrics for agentic runs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1959262

</td><td>

Ability for a user to onboard their own custom models from different providers

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1959277

</td><td>

Add updateConnection API in global.OneExtendEvaluationServiceUtil

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1959278

</td><td>

Quality improvements with performance/ logging/ debugging/ telemetry for Autochat/Autoeval

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1959279

</td><td>

Backend EPICs for stand alone agent evaluation changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1959871

</td><td>

Microphone doesn't work in enhanced NAP

</td><td>

Microphone only works when NAA toggle is on. It should not be dependent on NAA.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1960129

</td><td>

Conversation abruptly ends after a cold start conversation with pre-chat survey enabled

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

 PRB1960640

</td><td>

Tracer usage cleanup

</td><td>

 

</td><td>

1.  Set up a Teams LLM.
2.  Initiate a chat.
3.  observe that there is a null pointer exception in system logs.

 Expected behavior: The search returns results.

 Actual behavior: The search doesn't return any results.

</td></tr><tr><td>

Virtual Agent

 PRB1960689

</td><td>

Missing sys UI message for transferred search results from NAP

</td><td>

Missing sys UI message: 'Let me look into this in'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1962510

</td><td>

Empty sys\_cs\_message is created when Agentic Mode is on

</td><td>

 

</td><td>

1.  Set up Now Assist Virtual Agent \(NAVA\).
2.  Make sure Agentic Mode is turned on.
3.  Search 'What is spam?'.
4.  Navigate to **sys\_cs\_message**.
5.  Check for an empty message.

</td></tr><tr><td>

Virtual Agent

 PRB1963459

</td><td>

Conversation abruptly ends after a cold start conversation with pre-chat survey enabled

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1963943

</td><td>

NAVA does not work after upgrading

</td><td>

Custom Greetings topic stopped working after upgrade. This issue may affect users with customized greetings topics if the skill picker APIs called in the greetings/ending topic are not backward compatible.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1967329

</td><td>

QnA utterances in NAVA are missing 'Let me look up information related to ...' before it generates the response

</td><td>

In NAVA, when the user enters the utterance 'What is spam?', the user should see 'Let me look up information related to ...' before a response is generated. However, it goes directly to 'View AI Steps' followed by the actual response.

</td><td>

 

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1956730

</td><td>

Live agent only mode doesn't work for third-party channels

</td><td>

The user messages aren't received by the agent. This message appears in the log: 'Couldn't find rich control, dropping current message'.

</td><td>

1.  Set up VA and a third-party channel \(for example, Teams\).
2.  Set up VA to live-agent only mode \(for example, by having a custom greeting topic that directs to LA\).
3.  Start the conversation.
4.  Accept as an agent.
5.  Attempt to send messages as a user.

 Observe that the user messages aren't received by the agent with this message in the log: 'Couldn't find rich control, dropping current message'.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1893104

</td><td>

In Now Assist Multi-Turn Catalog Ordering, the 'Data/Time' type variable isn't showing the current time, but as 00:00AM in Virtual Agent for non-English language mode

</td><td>

The 'Data/Time' type variable should be displayed as the current time across all language modes.

</td><td>

1.  Activate the following plugin/store apps to last version:
    1.  UXC Generative AI \(sn\_uxc\_gen\_ai\)
    2.  Now Assist for IT Service Management \(sn\_itsm\_gen\_ai\)
    3.  I18N: Japanese Translations \(com.snc.i18n.Japanese\)
2.  Navigate to **Conversational Interfaces** &gt; **Assistants**.
3.  Enable Now Assist for Virtual Agent with 'Now Assist Multi-Turn Catalog Ordering' skill active in the Service Portal.
4.  Create a catalog item with one 'Data/Time' type variable.
5.  Navigate to **AI Search Index** &gt; **Indexed Sources**.
6.  Open 'Name='Catalog Item Table'.
7.  Select **Index All Tables** so that the newly created catalog item will be included in the Virtual Agent search via AI Search.
8.  Switch to the Japanese language mode after the reindex is done.
9.  Navigate to Service Portal.
10. Open Virtual Agent.
11. Search the newly create catalog item.
12. Start the request.
13. Check the 'Data/Time' type variable display.

 Expected behavior: The 'Data/Time' type variable should be displayed as the current time, which is the same in the English language mode.

 Actual behavior: The 'Data/Time' type variable displays as 00:00AM in the Japanese language mode.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1948852

</td><td>

NAVA use cases non-controller time regressed by ~1 second

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1953555

</td><td>

NAP/NAVA Client does not load

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1955687

</td><td>

When minimized from any view and re-opened, DW should always open in float mode

</td><td>

DW re-opens in 90% Modal view.

</td><td>

1.  Open DW in 90% Modal view.
2.  Minimize DW.
3.  Select the FAB icon to re-open DW.

 Expected behavior: DW should always open in float mode when minimized and re-opened. Same with Pin mode.

 Actual behavior: DW re-opens in 90% Modal view.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1960702

</td><td>

Selecting a Date using the UI picker for the 'Date' variable will show a Time in the generated user response

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1961300

</td><td>

Uploaded attachments are visually compressed to fit a specific response window

</td><td>

 

</td><td>

1.  In Virtual Agent chat, request any item.
2.  Continue until the 'Final Summary' card.
3.  Select **Add Attachments**.
4.  Upload any screenshot.

 Expected behavior: The users response containing the uploaded screenshot contains the same dimensions as the original screenshot.

 Actual behavior: The users response containing the uploaded screenshot visually compresses/squished the screenshot to fit into a fixed user response dimension.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1963494

</td><td>

The synthesized response is not displayed completely

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Navigate to **/esc portal**.
3.  Perform multiple searches.

 Notice that the final response displayed incompletely on VA web client.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1964410

</td><td>

The 'Continue request' option is not displayed during MID topic switch

</td><td>

The context switches to the new search without showing the Continue Request option.

</td><td>

1.  Start a conversation from DW.
2.  Search for any topic/Catalog.
3.  During MID execution, try searching a different Topic/Catalog/KB.

 Notice that the context switches to the new search without showing the Continue Request option. The Continue Request option should be displayed.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1967339

</td><td>

Double/Triple Feedback icons in DW

</td><td>

When the user types 'What is spam' in DW, the results are generated with double or triple feedback icons at the end.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1921416

</td><td>

When the 'Populate Agents Daily Schedule' table is executed, it isn't generating records in the 'agent\_daily\_schedule' table

</td><td>

The code should honor both the time formats \[24 and 12 hour formats\] while comparing the start and end time for an agent schedule in the 'Populate Agents Daily Schedule Table' schedule job for scheduled offline downloads in mobile.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1946618

</td><td>

Dynamic Scheduling does not consider the new location from a resource table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1949306

</td><td>

Handle invalid Work Order Task \(WOT\) data when loading it uses more load and fails in Dispatcher Workspace \(DWS\)

</td><td>

The end\_gdt is empty, which is invalid. Performing the add with an invalid GlideDateTime, resulting in an error: 'Cannot invoke ''java.util.Date.getTime\(\)'' because''this.fDate'' is null: org.mozilla.javascript.JavaScriptException: java.lang.NullPointerException: Cannot invoke ''java.util.Date.getTime\('' because''this.fDat'' is null. This error occurs because of the invalid date setup. The **actual\_trave\_start** field is empty on the WOT an 'Accepted' state and an 'On Route' substate.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 3 Hotfix 2](zurich-patch-3-hf-2.md)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2 Hotfix 2](zurich-patch-2-hf-2-PO.md)
-   [Zurich Patch 2 Hotfix 1](zurich-patch-2-hf-1-PO.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1 Hotfix 1b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2612279)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


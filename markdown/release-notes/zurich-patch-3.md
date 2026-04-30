---
title: Zurich Patch 3
description: The Zurich Patch 3 release contains important problem fixes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-30"
reading_time_minutes: 27
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 3

The Zurich Patch 3 release contains important problem fixes.

-   **Zurich Patch 3 was released on October 30, 2025.**
    -   Build date: 10-24-2025\_0919
    -   Build tag: glide-zurich-07-01-2025\_\_patch3-10-16-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z03.00.xlsx).

## Overview

Zurich Patch 3 includes 109 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-zp3.png "Top 10 problem categories")

## Security-related fixes

Zurich Patch 3 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 3, refer to [KB2570965](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2570965).

## Changes in Zurich Patch 3

-   **[Conversational intake for sourcing and procurement agentic workflow](https://www.servicenow.com/docs/access?context=spo-help-fulfill-pr-agentic&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    The Conversational intake for sourcing and procurement agentic workflow addresses your procurement needs by providing product recommendations, guided checkout, off-catalog processes, and detailed product information. It also answers questions and tracks related records.

-   **[Monitor inbound API integration usage](https://www.servicenow.com/docs/access?context=inbound-api-integration-usage-dashboard&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Monitor inbound integration usage requests through the Inbound API Integration Usage dashboard.

-   **[Using agentic workflows in Now Assist for Sourcing and Procurement Operations](https://www.servicenow.com/docs/access?context=agentic-ai-now-assist-spo&version=zurich&pubname=zurich-source-to-pay-operations&ft:locale=en-US)**

    Use agentic workflows in Now Assist for Sourcing and Procurement Operations \(SPO\) to streamline procurement through intelligent product recommendations, guided checkout, off-catalog purchasing, and access to detailed product information. These workflows also assist with procurement-related inquiries and help you track associated records efficiently.


-   **[View Inbound API Integration Usage dashboard](https://www.servicenow.com/docs/access?context=view-inbound-api-integration-usage-dashboard&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    The Inbound API Integration Usage dashboard enables you to view statistics for requestors and their API calls. Filter data by application or resource requested.


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

Configuration Management Database \(CMDB\)

 PRB1930654

</td><td>

The legacy health dashboard doesn't tell the user that the dashboard is deprecated/no longer supported

</td><td>

Users have bookmarked, saved, or edited links to the legacy health dashboard, meaning they can still access it. There's a lot of confusion on why the dashboard is no longer working as intended. There should be a message to tell the user this dashboard has been migrated to CMDB Workspace.

</td><td>

1.  Check out a Washington DC instance.
2.  Make a favorite for Health Dashboard - CMDB view.
3.  Upgrade the instance to X+.
4.  Select the bookmark for the CMDB view.

 Expected behavior: When users navigate to the legacy dashboard, they should be able to see a message telling them to use the new health dashboard and that the legacy dashboard is no longer supported.

 Actual behavior: See that the legacy health dashboard has some broken widgets, no colors, etc., but there is no indication that this dashboard is retired or has been migrated.

</td></tr><tr><td>

HR Service Delivery

 PRB1943958

 [KB2570781](https://hi.service-now.com/kb_view.do?sysparm_article=KB2570781)

</td><td>

There's a 'You do not have permission to read the created record' error when creating an HR Case

</td><td>

A race condition in the UI happens when a form is submitted before the GUID is created and an empty sys\_is is passed. The server-side code was not handling this. It happens intermittently.

</td><td>

1.  Open **Create New** via Agent Workspace.
2.  Select the **Benefits Management** HR service.
3.  Select **Create case**.

 Notice the error, but the case gets created in backend with an empty case number.

</td></tr><tr><td>

List Administration

 PRB1932703

 [KB2543882](https://hi.service-now.com/kb_view.do?sysparm_article=KB2543882)

</td><td>

Display values aren't showing for reference fields within the 'List' component

</td><td>

When including a table on the 'List' component that contains reference fields, it's showing empty. Where as in platform, it shows a value.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1905962

</td><td>

Link, text and icon menu items aren't working in Virtual Agent branding in Dynamic Window

</td><td>

 

</td><td>

1.  Navigate to our branding config record and review the menu items listed at the bottom: /sys\_cs\_branding\_setup\_list.do?.
2.  Observe that there's items for links, icons and text as menu items.
3.  Navigate to the portal after impersonating a valid user.
4.  Open Virtual Agent by selecting the icon at the bottom right.
5.  Select the **Support** button at the top of virtual agent window.
6.  Observe that none of the items of links, icons and text appear.

 Expected behavior: All type of menu items should display.

 Actual behavior: Only the phone and email are working.

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

 PRB1942003

</td><td>

Work notes/Comments are unexpectedly cleared when saving a form with an empty mandatory field and the work is lost

</td><td>

When there are any unfilled mandatory fields on the form, the text in the comments/work notes is getting cleared on selecting the **Save** button. It's impacting the user experience. Verified that it works fine in Xanadu and Yokohoma and on other workspaces like CSM/FSM Configurable workspace.

</td><td>

1.  Navigate to any Zurich instance.
2.  Open Service Operations Workspace.
3.  Open any active incident record.
4.  Clear any mandatory field value.
5.  Enter something in the Work notes/Comments.
6.  Select the **Save** button.

 Expected behavior: The Comments/Work notes should remain.

 Actual behavior: The Comments/Work notes are cleared.

</td></tr><tr><td>

Advanced Work Assignment for Case Service channel

 PRB1946390

</td><td>

The case task isn't working properly for CCaaS external routing

</td><td>

The assignment isn't happening since there's no mapping field available for CCaaS partners to use and store their external ID onto the 'Case task' table.

</td><td>

1.  Configure the instance to route the case tasks through external CCaaS.
2.  Create a case task in the instance.
3.  The case task should be routed to the agent using the external routing mechanism.

 Expected behavior: The case task should be picked up by the CCaaS events and assigned to the identified agent. Further events should also be triggered for this task.

 Actual behavior: Currently the case task doesn't get assigned to the agent.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1938992

</td><td>

High AWA assignment cycle times for impact voice call routing

</td><td>

A user is uptaking in NVC and they are facing slow response times for call routing. It's taking ~12 seconds to route the call to agent. Each AWA assignment cycle is taking ~11 secs and out of which ~8 secs is being spent for Agent Map creation. Expected response times should be less than a second as there's no other load in the system.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1942061

</td><td>

Lack of ability to track end-to-end AWA Assignment times

</td><td>

There's currently a gap in performance measurement of the AWA offer work API and manual assignment API, where there is no way to accurately determine the time difference between when an external AWA assignment API call was made and when the work item assigned\_to would be updated to the assigned agent. The admin lacks context as to when the request actually gets processed and the work item gets assigned \(and by extension, the inbox card shows up in the agent's inbox\). Another limitation with the current design is that it only persists the offered\_on for the final API invocation, which led to work item acceptance. If there were multiple agents which were offered the work item via these APIs, this context is lost.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1944387

</td><td>

The 'Create Segment On WorkItem Accept' business rule runs unnecessarily when a previous accepted work item exists

</td><td>

 

</td><td>

1.  Call the 'Offer work' API on an interaction.
2.  Accept the work item.
3.  Clear out the assigned\_to on the interaction.
4.  Call the offer work API on the same interaction.

 Expected behavior: The 'Create Segment On WorkItem Accept' business rule shouldn't be triggered for the old work item.

 Actual behavior: The 'Create Segment On WorkItem Accept' business rule is triggered for the old work item.

</td></tr><tr><td>

AI Search

 PRB1940661

</td><td>

The hasPendingIndex API is broken

</td><td>

The sn\_ais.AisUtil. hasPendingIndex \(tableName, recordSysId, embeddingModelName, semanticIndexName\); call fails.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1941065

</td><td>

Response loads even after a 15 second timeout on the portal

</td><td>

The portal stops the loading sign, which means it's reached the 15 second timeout. The response to the user's query loads after that.

</td><td>

1.  Navigate to a portal with DW enabled.
2.  Search for any query, such as 'How to create a new user?'.

 Expected behavior: Once the portal times out, it doesn't load the response.

 Actual behavior: The portal stops the loading sign, which means it's reached the 15 second timeout, but the response loads after that.

</td></tr><tr><td>

Analytics Data API

 PRB1926918

</td><td>

The 'Process analytics cache prefetch queue' job leads to OutOfMemoryError and the node restarts

</td><td>

When the user runs the 'Process analytics cache prefetch queue' job, it loops in ChangeCheckConflictsSNC script include.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1945218

</td><td>

Memory leak of JSON serializer in multivis API

</td><td>

Each time a data request is processed, a new serializer is created and not released unless a GC is performed, which causes a memory leak.

</td><td>

1.  Create a dashboard.
2.  Add a tab and add 50 identical single score vis:
    1.  Source: incident.
    2.  Condition: sys\_id is empty.
3.  Duplicate the tab 9 times so there are 500 visualizations in total.
4.  Disable the property 'com.snc.dashboard.streaming.enabled'.
5.  Stop the instance and start again, but don't access the instance in the browser.
6.  Use VisualVM to capture the heapdump.
7.  Search for 'IntegerDateSerializer' in the object list.

Observe that there are 0 results.

8.  Access the dashboard created in step 1.
9.  Go over all 10 tabs.
10. Use VisualVM to capture the heapdump.
11. Search for 'IntegerDateSerializer'.

Observe that there are ~500 results.

12. Repeat steps 8 through 11 \(get the heapdump and search\).

 Observe that there are ~1000 results. Each time a data request is processed, a new serializer is created and not released unless a GC is performed, which causes a memory leak.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1922654

</td><td>

Automated Test Framework **test** UI action fails due to a timeout error

</td><td>

There appears to be a race condition introduced in Yokohama. Tests that previously passed in Xanadu are now failing some of time when waiting for a response from the intent channel.

</td><td>

1.  Navigate to **Automated Test Framework \(ATF\)** &gt; **Tests**.
2.  Create a test.
3.  Add test step by opening an existing record with values:
    -   Form UI= SOW Workspace
    -   Table=sc\_task
    -   Record= Select any record
4.  Add test step by:
    1.  Select a UI action or UI action visibility.
    2.  Select **Save** for the UI action.
5.  Clear the instance cache and browser cache.
6.  Using an incognito browser session.
7.  Log in.
8.  Navigate to the test.
9.  Run the test.

 Expected behavior: The test should pass every time.

 Actual behavior: The tests fails intermittently due to an 'Timed out waiting for intent feedback' error.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1880009

</td><td>

Attachments aren't uploaded in the 'Agent Chat' window from HR Agent Workspace

</td><td>

This is happening for HR Core.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1939399

</td><td>

The search function on the third-level panel keeps loading continuously on the now-dot-walk v2

</td><td>

When searching on the third-level panel, it enters an infinite loading state instead of displaying the client-side filtered data.

</td><td>

 

</td></tr><tr><td>

Customer Operations for Customer Service Management

 PRB1918447

</td><td>

The responsibility framework allows the selection of dot-walked fields in the UI, but in the backend it's not granting the access

</td><td>

The previous implementation used relationshipGR.isValidField\(\) for validating dot-walked field paths, but this method only validates if a field exists directly on a table and doesn't properly traverse dot-walked paths. In the responsibility framework UI, it is possible to select dot-walked fields, but the backend wasn't properly validating these paths, resulting in access being denied for records even when the configuration should allow it.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1792470

</td><td>

Some alters to increase max length are running twice during an upgrade

</td><td>

Multiple updates happen because a sys\_dictionary record has an incorrect field length after finishing the bootstrap batcher.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1907199

</td><td>

Two schemas marked as default simultaneously

</td><td>

There are two graph schemas which are marked as default. One is the Global graph and other is the newly created graph which is marked as default.

</td><td>

1.  Create a new graph.
2.  Mark it as default.
3.  Add desired nodes/edges.
4.  Save the graph.
5.  Navigate to sys\_meta\_graph.

 Notice that two graph schemas are marked as default.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1923704

</td><td>

Due to an ordering change on Raptor post migration, certificate authentications for API calls may fail and cause '500' errors

</td><td>

When mutual authentication is configured using both protocol profile and system properties, the system property takes precedence. This causes the SSL exchange to utilize the socket factory for client certificate provisioning, bypassing the keystore defined in the protocol profile. Additionally, when mutual authentication is enabled via property configuration, all certificates from the sys\_certificate table are loaded. This can lead to intermittent outbound call failures if expired certificates are cached and used for mutual authentication, resulting in HTTP 500 responses.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1936199

</td><td>

Apostrophe in the cypher query causes an error

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1944376

</td><td>

Order tables in the view deterministically

</td><td>

Currently, when constructing the view to return from a cypher call, it creates the view from the set of the tables being requested based on enumerating the keyset. This has a nondeterministic order that depends on the underlying structure and the table prefixes. While that wouldn't be an issue at some layers, it means the ACL evaluation differs based on the ordering, which is hard for debugging and also hard to configure around. Instead, it should sort the order of the tables in the view alphabetically by the table name.

</td><td>

1.  Do a cypher query with more than one return node.
2.  Examine the view definition to see which table comes first.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1946284

</td><td>

Response columns are returned without node aliases for normal non-aggregate cypher queries

</td><td>

Choice value in quotes and setFixupEdges are failing for the WDF and physical table. For choice value scenario, the cypher u.calendar\_integration is a choice column, and passing the value of the choice column on quotes is failing here. For the setFixupEdges scenario, passing setFixupEdges as a true persistence isn't honored.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1927640

</td><td>

Duplicate entries are created for extension tables in both the physical and logical tables in both SNC and information schema

</td><td>

 

</td><td>

1.  Log in to the instance with SNC is running or with information schema enabled.
2.  Run the 'Stats gather' job daily.
3.  After the job completes, navigate to the sys\_physical\_table\_stats table.
4.  Search for any extension tables, such as syslog0001.
5.  Filter by the latest date and by type as 'Primary' and 'Primary/Sharded'.

 Expected behavior: There should be only one entry for the primary database.

 Actual behavior: There are two entries for the primary database.

</td></tr><tr><td>

Database Persistence

 PRB1861812

</td><td>

EncodeQuery doesn't return the correct value on Data Fabric tables

</td><td>

After choosing 'North America' in the Region and applying, the module gets updated with North American data, but the filter box became 'unavailable option'.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1937018

</td><td>

dbi.truncateTable\(table\_name\) is truncating a table name when the table name is bigger than 29 characters and the daily schedule job isn't able to drop that table

</td><td>

In recent releases, DBTruncateUtil.truncateTable\(\) calls for tables with long names leave orphaned tables behind in the DB and causes backup to fail.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB1938101

</td><td>

The 'Database' view for Workflow Data Fabric \(WDF\) incorrectly assumes the sys\_id when caching underlying glide records

</td><td>

add/getCache in the 'Database' view has a hardcoded assumption that there's a sys\_id element in the source and doesn't check for a null result. The copyValue code calls into GlideElement, which short circuits due to the WDF table being a foreign table. This needs to skip the cross scope check but still copy the value.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1862106

 [KB2436326](https://hi.service-now.com/kb_view.do?sysparm_article=KB2436326)

</td><td>

Global IP exclusion isn't working for a cloud VM schedule

</td><td>

Not all the global exclusions are working for a Cloud Discovery.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1902780

</td><td>

The log pattern cloud errors only once

</td><td>

Currently, the cloud pattern errors are incorrectly being logged twice. It ends with two separate errors for the same pattern, one for the exception in the log and one for the 'Pattern Failed'.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1937992

</td><td>

Discovery Schedule doesn't support the Discovery of more than 5000 IPv6 addresses

</td><td>

If the user creates a Discovery Schedule with over 5000 IPv6 addresses, the Discovery Status is instantly canceled and an error message appears.

</td><td>

1.  Create a Discovery Schedule with over 5000 \(X\) IPv6 addresses to disocvery\_range\_item\_ip.
2.  Select **Discover Now**.

 Observe that the Discovery Status is created and instantly canceled with the following error message under the Discovery logs related list: 'IP lists with IPv6 addresses can only contain 5,000 IPs but have X'.

</td></tr><tr><td>

Document Management Services

 PRB1920126

</td><td>

Export to PDF for a scheduled report doesn't export in the proper alignment

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Dynamic Translation for Agent Chat

 PRB1942231

</td><td>

agent\_translated\_msg column is overwritten with empty value when the agent is in English and the chat requester is non-English

</td><td>

 

</td><td>

1.  Enable and configure DTAC.
2.  Log in to Service Operations Workspace as an English speaking agent.
3.  In another browser, log in as chat request in non-English language.
4.  Initiate an agent chat.
5.  Type an English phrase as an agent.

 Expected behavior: agent\_translated\_msg on outbound message should be populated with English text.

 Actual behavior: The agent\_translated\_msg gets overwritten with empty values.

</td></tr><tr><td>

Encryption

 PRB1923672

</td><td>

A Session API getting encryption contexts causes a performance impact

</td><td>

Flow engine performance is impacted by the database calls required to encryption contexts. This API is called billions of times per month and amounts to a pretty significant impact to performance.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1639714

</td><td>

Alerts on an Application Service have empty PRCs

</td><td>

Alerts on an Application Service appear in the list of 'Impacted Services/CIs' of some change request. These alerts have empty PRCs and they have only one change request instead of two.

</td><td>

1.  Define the Manual Application Service.
2.  Define the Change Request for the Application Service.
3.  Send the event to some CI of the Application Service.
4.  Open the generated alert.
5.  Navigate to the PRC.

Observe that the alert has the PRC 'Change on Application Service.'

6.  Send the event to the Application Service.
7.  Open the generated alert.
8.  Navigate to the PRC.

Observe that the alert has the PRC 'Change on Application Service.'

9.  Create another change request on a different CI.
10. Add the defined Application Service to the list of Impacted CIs of the change request.
11. Send the event to the Application Service.
12. Open the generated alert.
13. Navigate to the PRC.

 Observe that the alert has only one change request, but it should have two.

</td></tr><tr><td>

Event Management

 PRB1934096

</td><td>

There's a regex preview mismatch in Enrich due to Java vs JavaScript engine differences

</td><td>

In the 'Enrich' page, the regex preview incorrectly shows no match even when the regex is valid and works correctly on actual events. This discrepancy, caused by differences between Java and JavaScript regex engines, has been observed by multiple users and leads to confusion when building enrichment rules.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1891187

</td><td>

There's a high query count when running a flow as a current user

</td><td>

During performance tests of order processing, there's costly queries when flows RunAsUser. Counts can be over 40 million queries executed.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1941990

</td><td>

Trigger inputs aren't accessible after a do-until loop execution

</td><td>

This issue is caused by the changes to GlideFlowStages Updater.java \(older name GlideStage UpdateListener.java\). It's observed that, in this specific flow structure, the 'in.request\_item' flow input isn't passed to the 'Create Catalog Task' action. Querying the sys\_flow\_value table, there are 2 entries for 'in.request\_item' one for the flow input and another with the parent loop associated. As the same key 'in.request\_item' is now associated with parent loops, it can only be accessed in the loop body \(and for the specific iteration\), and all other references to it out side the loop aren't available.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1945637

</td><td>

Existing scripted fields are set to the 'fd-scripted' static value when there are more than 1 scripted inputs present in the case of templated fields on an update

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1939177

</td><td>

User can't view the attachment on a HR case

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1940947

</td><td>

Remove license meter dependency from Manager Hub in the OOB-apps properties file

</td><td>

Manager Hub apps must be dependent on EC Pro \(which is already existing\) and not on License Meter. And hence, remove the Manager Hub app dependency on License Meter.

</td><td>

 

</td></tr><tr><td>

Identity

 PRB1891185

</td><td>

There's a high query count running a flow with roles

</td><td>

During a performance load test where 50k orders were created in 1 hour, the query was a significant contributor to the overall execution time. This appears to be triggered when flows run with additional roles. When running as system user or without additional roles, this query pattern isn't observed.

</td><td>

 

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB1943106

</td><td>

Inbound API integration usage and system metadata tracking for integration requests

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB1943108

</td><td>

System metadata access tracking for GlideRecord wrapper APIs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1937947

</td><td>

Additional logging for Splunk to build more context around legitimate use cases

</td><td>

 

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1923497

</td><td>

Deadlock occurred due to two threads

</td><td>

The issue is caused by a conflict between two internal processes that manage and refresh OAuth credentials and MID Server connections. The platform periodically checks and refreshes expired OAuth tokens using a scheduled job. When this happens, the system reloads the credentials and resets all related connection data to ensure security and consistency. At the same time, if a Discovery probe or integration is trying to establish a new connection, it might attempt to access the same shared connection resources. This overlap can lead to both processes waiting for each other to finish, resulting in a temporary deadlock where neither process can proceed.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1940079

</td><td>

Add condition operators to support IN and MATCH\_RGX with the field value in the UI Rule

</td><td>

The condition operators IN and MATCH\_RGX don't work with values in a variable, which is needed to make uploading an attachment mandatory when a skip\_code in the reference list is selected.

</td><td>

1.  Add a user input in the 'Edit work' input form screen.
2.  Add a variable user Ids with a script.
3.  Modify the condition in the UI Rule 'Hide State field' to be user IN.

 Expected behavior: The **State** field is hidden when a user is selected.

 Actual behavior: The **State** field isn't hidden.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1945540

</td><td>

The 'Enable Analytics' preference property isn't passing the user\_consent property

</td><td>

The telemetry-behavior is attempting to read the value from the payload, but it's not passing a payload object when dispatched.

</td><td>

1.  Open an instance with the 'User Analytics preferences' property turned on.
2.  Open 'User Preferences'.
3.  Navigate to 'User Experience'.
4.  Attempt to turn on/off 'Enable Analytics'.

 Notice the 500 error.

</td></tr><tr><td>

Now Assist Panel

 PRB1942697

</td><td>

The Now Assist Panel \(NAP\)/NASS window can't be found after closing and not pinning it

</td><td>

On the header, the icon for NAP should be visible, but there's no option for opening it.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1943530

</td><td>

High frequency one\_extend\_rate\_ limit\_violation\_cache flushes, causing system slowness

</td><td>

During routine operations, multiple nodes experienced high memory usage and glide.cs.worker thread pressure, resulting in frequent node restarts. Investigation indicates that the one\_extend\_rate\_limit\_violation\_cache flush events were triggered at an unusually high frequency \(over 5000 times within a 30-minute window\), which may have contributed to the observed slowness. Analysis suggests that excessive cache flushes can create significant memory and performance pressure on the system.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1940891

</td><td>

The prompt field in the 'Generative AI Log' table has extra escaped characters when using Java subflow implementation

</td><td>

In Java, a prompt is converted to a string even though it's already a string before inserting it into the Generative AI Log table. There's extra escaped characters in the prompt field.

</td><td>

1.  Run a capability.
2.  Navigate to the sys\_generative\_ai\_log table.
3.  Check the **prompt** fields.

 Expected behavior: Users shouldn't see extra escaped characters in the prompt.

 Actual behavior: Valid escaped sequences are escaped unnecessarily.

</td></tr><tr><td>

Performance Analytics

 PRB1937240

</td><td>

The reports and PA widgets are displayed in the Migration Center without the bulk migration being triggered

</td><td>

 

</td><td>

1.  Take an upgrade instance from Washington to Australia.
2.  Navigate to the Migration Center.
3.  Select the **The review in the Migration Center** button.

 Notice that the artifacts for the reports and PA widgets are available on the Migration Center, without the migration being triggered.

</td></tr><tr><td>

Performance Analytics

 PRB1939257

</td><td>

Increase guardrails threshold

</td><td>

RELATIVE\_DATE\_ CONDITION\_AND\_VOLUME: Increase the default value to 300M. INSERT\_VOLUME\_EXCEEDED: Increase the default value to 10M. DATA\_VOLUME\_EXCEEDED: Increase the default value to 300M.

</td><td>

 

</td></tr><tr><td>

Performance Telemetry

 PRB1938437

</td><td>

Move db.query.summary in db.client. operation.duration to an exemplar attribute

</td><td>

The db.query.summary should be set to exemplar only to reduce cardinality.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1917370

</td><td>

Missing localization strings on the CIO Dashboard

</td><td>

On the CIO dashboard, the localization strings are missing for the tab names, rich text contents, widget titles, info, and error messages.

</td><td>

1.  Log in to the instance.
2.  Navigate to the 'Localization' page.
3.  Select the **Displays translation prefix on translatable strings** checkbox.
4.  Navigate to the CIO Dashboard.
5.  View the translation prefixes for every widget.

 Observe that the translation prefixes are missing for most of the elements on the CIO dashboard.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1946056

</td><td>

A C-suite category and error message isn't translated

</td><td>

The error message: 'Contact the administrator to review data collection jobs and the indicator configuration to display data for the selected criteria.'

</td><td>

1.  Log in to any instance with CxO dashboards.
2.  Open the CxO dashboard.
3.  Check for any widget that has zero data.
4.  Change the language.

 Expected behavior: The error message is translated.

 Actual behavior: The error message isn't translated.

</td></tr><tr><td>

Process Mining

 PRB1939181

</td><td>

Dot-walk activity log collection is broken when the dot-walk value never changes

</td><td>

If the dot-walk value doesn't change, project mining fails, saying that no audit logs are found.

</td><td>

1.  Create a project with dot-walk activity.
2.  Take a sample case where the base field changes but the dot-walk value remains the same for all groups.
3.  Mine the project with just one case and one dot-walk activity.

 Expected behavior: The project is mined and a map appears.

 Actual behavior: Mining fails, saying that no audit logs are found.

</td></tr><tr><td>

Project Management

 PRB1905989

</td><td>

The **Create Expenseline** button from the new costplan split button doesn't create a system generated costplan

</td><td>

The widget is updated, but no new system generated costplan is created.

</td><td>

1.  Create any planning item.
2.  Add a costplan intially.
3.  Select **New Expenseline** on the costplan split button.
4.  Add the details but dont associate it with any costplan.
5.  Save the expenseline side panel.

 The actuals widget is updated, but no new system generated costplan is created.

</td></tr><tr><td>

Service Mapping

 PRB1944512

</td><td>

Turn off the mapped application services limit

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1947153

</td><td>

The lookup select box with a reference qualifier in MRVS displays incorrect labels on the 'SC Catalog Item' widget

</td><td>

The lookup select box in MRVS displays labels according to only a subset of the conditions defined in the reference qualifier \("javascript: xxx"\).

</td><td>

 

</td></tr><tr><td>

Software Discovery

 PRB1579663

</td><td>

File-based discovery populates the version only on the first software install record for a DM

</td><td>

 

</td><td>

Run file-based Discovery.

 Notice the software install record \(cmdb\_sam\_sw\_install\) only has **Publisher** and **Product** \(display names\) populated. It would be good to also populate version with the normalized version if available. Some users have use cases that require a version on the install records.

</td></tr><tr><td>

Transaction Management

 PRB1947766

</td><td>

When a new token is refreshed with OAuth, the transaction.fUser property is set to 'guest' even if the GlideSession is authenticated with the correct user, which breaks the integration usage GuestUserFilter

</td><td>

With OAuth 2.0, when the first integration request is sent, it refreshes the expired token. After the transaction is complete and the notifyTransactionComplete monitor list is executed, there is a discrepancy between the **Transaction.fUser** field and the GlideSession.get\(\) .getUserName\(\) value. This occurs for a fully authenticated session. When checking if the user is a guest, Transaction.getUser\(\) isn't accurate. The check in GuestUserFilter only looks at the transaction object, when it needs to look at the GlideSession object.

</td><td>

1.  Create a regular user, and don't select webserviceaccessonly.
2.  Setup OAuth 2.0 locally.
3.  Trigger a request against the table API by authenticating with OAuth as that user.
4.  Wait until the OAuth token expires, which is approximately 30 mins.
5.  Put a break point on Transaction.notify TransactionComplete\(\).
6.  Trigger another request.

 Observe the state.

</td></tr><tr><td>

User Administration

 PRB1896603

</td><td>

There's a high sys\_user query count when running a flow as a system user

</td><td>

During a 1 hour test that processes 50k orders, there's high query counts on sys\_user for the system user.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1887044

</td><td>

The latest asset in sys\_ux\_lib\_asset isn't used when multiple asset records exist for the same asset version

</td><td>

This impacts Now Assist Panel loading and Dirty State Management in workspaces.

</td><td>

\\

</td></tr><tr><td>

UX Framework

 PRB1892094

</td><td>

An ATF test UI action fails due to a timeout error

</td><td>

The intent library delivers context on generator registration for translators that don't exist on the page.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1918913

</td><td>

The js\_atf\_instrumentation.js script is missing when asset bundling is turned on

</td><td>

js\_atf\_instrumentation.js script, which instruments pages for component load detection and rollback during Automated Test Framework \(ATF\) testing, is missing when asset bundling is turned on.

</td><td>

1.  Navigate to **Menu** &gt; **Automated Test Framework** &gt; **Tests**.
2.  **Create your own new test** &gt; **Give a name** &gt; **Save**.
3.  Add a test step to open a form in workspace for able **sc\_task** &gt; **Form** &gt; **Open a new form**.
4.  Choose **Form UI** &gt; **SOW workspace**.
5.  Choose **Table** &gt; **sc\_task** &gt; **Save the test step**.
6.  Add **Test step** &gt; **Form** &gt; **UI action visibility**.
7.  Choose **Visible close task** &gt; **Save the test step**.
8.  Navigate to the test page where it lists the 2 steps.
9.  Right click on the display name of the UI action visibility display name and select **Add breakpoint**.
10. Select **Debug Test**.

This opens the test runner in a new window.

11. Wait for the test to stop at the break point and inspect the DOM to notice the script tag for js\_atf\_instrumentation.js is missing.
12. Turn off asset bundling using glide property glide.uxf.lib.asset\_bundle\_enabled.

 Notice js\_atf\_instrumentation.js is available.

</td></tr><tr><td>

UX Framework

 PRB1927748

</td><td>

The Next Experience UI is broken when a sys\_cb\_metadata record doesn't have a macroponent associated

</td><td>

The Next Experience UI can't be used when a sys\_cb\_metadata record doesn't have a macroponent associated. After going to any Next Experience URL, the following error is seen in the console: 'SERVICE WORKER NOT FOUND'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1928396

</td><td>

Date time input when used in a topic block returns null on output parameters

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Create a topic block \(nlu/keywords\) with data time input.
3.  Add date time input to the output parameters.
4.  Run the topic block and the data time returned in the output parameters in \{\}.

</td></tr><tr><td>

Virtual Agent

 PRB1937290

</td><td>

The **New conversation** button disappears when using certain custom branding colors

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1941593

</td><td>

Using vaSystem.execute SkillWithResumeBehavior in a topic causes resume conversation to fail

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1943466

</td><td>

Now Assist Skill executing twice when running in sync mode

</td><td>

The main skill should execute only once. The main skill is executing twice. Please check the GenAI log and find two execution records.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1943976

</td><td>

Need to add expensive caches as hard reference caches to avoid GC

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1940975

</td><td>

Support more markdown for text messages and synthesized responses

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1941763

</td><td>

The **New chat** button is turned off after a flow execution is complete

</td><td>

 

</td><td>

1.  Call one of the HR flows that results in successful case creation which is the end of the flow.
2.  Try to start a new conversation.

 The **New chat** \(plus button\) is turned off.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1948623

</td><td>

Uptake new versions of Unified Experience Framework \(UXF\)

</td><td>

UXF intent library changes to Zurich and Yokohama chat-components to uptake these versions.

</td><td>

 

</td></tr><tr><td>

Workspace List Menu

 PRB1935619

</td><td>

Intermittently the L1 \(left side toolbar\) menu doesn't render in workspaces

</td><td>

 

</td><td>

1.  Impersonate any user.
2.  Open Hardware Asset Workspace.

 The user may see left side menus not displaying. If it displays, refresh a few times, it may go away. It's intermittent.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1 Hotfix 2](zurich-patch-1-hf-2-PO.md)
-   [Zurich Patch 1 Hotfix 1a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2556047)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


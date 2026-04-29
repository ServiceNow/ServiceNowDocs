---
title: Australia Patch 1
description: The Australia Patch 1 release contains important problem fixes.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-04-03"
reading_time_minutes: 97
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 1

The Australia Patch 1 release contains important problem fixes.

-   **Australia Patch 1 was released on April 03, 2026.**
    -   Build date: 03-31-2026\_1137
    -   Build tag: glide-australia-02-11-2026\_\_patch1-03-23-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This version is being evaluated for use in the ServiceNow Government Community Cloud \(GCC\) environment.

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A01.00.xlsx).

## Overview

Australia Patch 1 includes 372 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-ap1.png "Top 10 problem categories")

## Security-related fixes

Australia Patch 1 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 1, refer to [KB2914133](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2914133).

## Changes in Australia Patch 1

-   **[Access your ServiceNow data using SQL API](https://www.servicenow.com/docs/access?context=accessing-your-servicenow-data-using-sql-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    The SQL API provides read-only access to your ServiceNow tables, allowing you to write SQL queries, create reports, and perform analysis while maintaining your existing security controls. This eliminates the need for data synchronization and ensures you work with current ServiceNow data.

-   **[Associate a request header with a resource](https://www.servicenow.com/docs/access?context=associate-header-api-resource&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    \[Target &lt;context&gt; was unhandled by content reference generator.\]

    \[Target &lt;result&gt; was unhandled by content reference generator.\]

-   **[Associate query parameters with a resource](https://www.servicenow.com/docs/access?context=AssocQueryParmResource&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    \[Target &lt;context&gt; was unhandled by content reference generator.\]

-   **[Automatically generate API request definitions](https://www.servicenow.com/docs/access?context=autogenerate-api-request-definitions&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource.

-   **[Common use cases for SQL API](https://www.servicenow.com/docs/access?context=common-use-cases-for-sql-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    The SQL API supports business intelligence reporting, ad-hoc data analysis, and custom report development.

-   **[Configure ServiceNow SQL API JDBC driver on client machine](https://www.servicenow.com/docs/access?context=configure-jdbc-driver&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Configure the JDBC driver settings on your client machine to establish a connection to your ServiceNow instance and access data through the SQL API.

-   **[Configure ServiceNow SQL API ODBC driver on client machine](https://www.servicenow.com/docs/access?context=configure-odbc-driver&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Configure connection settings for the installed ODBC driver including server URL and authentication credentials to enable data access from BI tools to your ServiceNow instance.

-   **[Configuring ServiceNow Vault](https://www.servicenow.com/docs/access?context=configuring-servicenow-vault&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Learn how to install and configure ServiceNow Vault.

-   **[Configuring SQL API](https://www.servicenow.com/docs/access?context=configuring-sql-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Configure your ServiceNow instance to enable SQL API access, set up the necessary security controls, and install the appropriate drivers on your client machine.

-   **[Configure SQL API plugin on your ServiceNow instance](https://www.servicenow.com/docs/access?context=configure-sql-api-overview&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Configure your ServiceNow instance to enable SQL API access, set up the necessary security controls, and install the appropriate drivers on your client machine.

-   **[Connect DB Visualizer to JDBC driver](https://www.servicenow.com/docs/access?context=connect-dbvisualizer-jdbc&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Overview of the three-step configuration process required to enable SQL API access including prerequisites and expected outcomes.

-   **[Connect Power BI Desktop to ODBC driver](https://www.servicenow.com/docs/access?context=connect-power-bi-odbc&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.

-   **[Create Access Control Lists \(ACLs\) for SQL API](https://www.servicenow.com/docs/access?context=create-acls-sql-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Configure table-level access control using the egress\_sql and read operations to grant Service Accounts query access to specific tables through the SQL API.

-   **[Create IP filter criteria](https://www.servicenow.com/docs/access?context=create-ip-filter-criteria&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the SQL API ODBC or JDBC driver. By default, all incoming IPs are blocked until you configure the SQL API Authentication Policy with an IP filter and policy condition to allow access only from trusted client machines.

-   **[Create a Service Account and assign Roles](https://www.servicenow.com/docs/access?context=create-service-account&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Create a dedicated non-interactive Service Account in User Administration and assign the appropriate SQL API access role to enable secure, programmatic access for BI tools and analytics platforms.

-   **[Download the SQL API drivers on client machine](https://www.servicenow.com/docs/access?context=download-sql-api-drivers&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Download the ODBC and JDBC drivers from the ServiceNow store to your client machine to enable SQL API connectivity.

-   **[Define a REST API response header](https://www.servicenow.com/docs/access?context=define-scripted-api-response-header&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Define one or more REST API response headers in a REST API.

-   **[Define a REST API schema](https://www.servicenow.com/docs/access?context=define-scripted-rest-api-schema&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Specify the expected data structure for requests or responses within a REST API by defining a schema.

    The following procedure describes the process for manual schema definition. For details about automatically generating request schema definitions in non-production instances, see .

-   **[Define an API resource request structure](https://www.servicenow.com/docs/access?context=add-schema-rest-api-request&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Add a schema to a REST request record to define the request's expected data structure.

    \[Target &lt;context&gt; was unhandled by content reference generator.\]

-   **[Define an API resource response structure](https://www.servicenow.com/docs/access?context=add-schema-rest-api-response&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Add a schema and relevant response headers to a REST response to define the response's expected data structure.

-   **[Define available query parameters](https://www.servicenow.com/docs/access?context=t_DefineAvailableQueryParameters&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    \[Target &lt;context&gt; was unhandled by content reference generator.\]

-   **[Define a scripted REST API request header](https://www.servicenow.com/docs/access?context=t_DefineRESTServiceHeaders&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    a scripted REST API request header

    \[Target &lt;titlealts&gt; was unhandled by content reference generator.\]

    request

    request

    \[Target &lt;context&gt; was unhandled by content reference generator.\]

-   **[Enhanced Requests Experience](https://www.servicenow.com/docs/access?context=my-requests-update-intro&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

    **Note:** You must be on the Employee Center version 38.0 or later or have upgraded to the Australia release to use the Enhanced Requests Experience.

    The requests are displayed in a card view by default. You can the view toggle icons next to the search bar to switch between card view and list view. The toggle functionality is only available on Employee Center version 40 onwards.

-   **[Getting started with ServiceNow SQL API](https://www.servicenow.com/docs/access?context=getting-started-with-servicenow-sql-api&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    The ServiceNow SQL API provides data access to your ServiceNow instances through industry-standard ODBC and JDBC drivers, enabling direct connections from Business Intelligence \(BI\) tools and data analysis platforms.

-   **[Integrate SQL API Drivers with external BI tools](https://www.servicenow.com/docs/access?context=configure-drivers-bi-tools&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Configure ServiceNow SQL API drivers to connect with external business intelligence and database tools for direct data access and analysis.

-   **[Install ServiceNow SQL API ODBC driver on client machine](https://www.servicenow.com/docs/access?context=install-odbc-driver&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Install the ServiceNow ODBC driver on your Windows client machine to enable connectivity between your Business Intelligence \(BI\) tools and ServiceNow data through the SQL API.

-   **[Install SQL API plugin on your ServiceNow instance](https://www.servicenow.com/docs/access?context=install-sql-api-plugin&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Installing the SQL API on your instance enables secure, read-only access to your instance data from external applications. You can integrate your data with external tools and analytics platforms to enhance your reporting and data analysis capabilities.

-   **[Install ServiceNow Vault](https://www.servicenow.com/docs/access?context=install-vault&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Install the ServiceNow Vault application and assign the required roles.

-   **[Manage connected content from topic pages](https://www.servicenow.com/docs/access?context=mnge-content-topics&version=australia&pubname=australia-employee-service-management&ft:locale=en-US)**

    \[Target &lt;info&gt; was unhandled by content reference generator.\]

-   **[Minimum requirements and supported software for SQL API](https://www.servicenow.com/docs/access?context=minimum-requirements-and-supported-softwares&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    This section lists the minimum supported versions for ServiceNow server releases, client drivers \(ODBC and JDBC\), and Java Development Kit required for SQL API.

-   **[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)**

    For Now Assist new features and changes, see [Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md).

-   **[Route SQL API calls to Read Replica](https://www.servicenow.com/docs/access?context=routing-sql-api-calls-to-read-replica&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    You can route SQL API calls to Read Replica to optimize the performance of your ServiceNow instance.

-   **[Scripted REST APIs](https://www.servicenow.com/docs/access?context=c_CustomWebServices&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Schemas define a structure that can be used for API requests and responses, including data type, expected fields, and formats. You can define multiple schemas within a scripted REST API, which can be used to specify request and response contents of the resources within that API.

-   **[ServiceNow Vault roles](https://www.servicenow.com/docs/access?context=vault-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US)**

    Learn and set up the roles necessary to use ServiceNow Vault.

-   **[SQL API architecture](https://www.servicenow.com/docs/access?context=sql-api-architecture&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    The SQL API architecture demonstrates how the SQL API plugin integrates with the ServiceNow system to provide secure, read-only data access through industry-standard ODBC and JDBC drivers.

-   **[SQL API reference information](https://www.servicenow.com/docs/access?context=troubleshooting&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    This section provides details about SQL API reference information like minimum requirements and usage limitations.

-   **[Supported SQL functions](https://www.servicenow.com/docs/access?context=supported-sql-functions&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Common SQL functions used in SQL API for querying and analyzing incident data.

-   **[Test SQL API ODBC driver connection using Interactive SQL](https://www.servicenow.com/docs/access?context=test-sql-api-odbc-driver-connection-using-interactive-sql&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    Run the Interactive SQL application for quick verification of connectivity and to test query results without using a full application.

-   **[Usage Limitations for SQL API](https://www.servicenow.com/docs/access?context=usage-limitations&version=australia&pubname=australia-api-reference&ft:locale=en-US)**

    The SQL API imposes rate limits to ensure system stability and performance when querying ServiceNow data through ODBC and JDBC drivers.

-   **[Use Now Assist to search the CMDB](https://www.servicenow.com/docs/access?context=na-cmdb-awf-search&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)**

    Starting with Now Assist for CMDB v3.0, searches can include parent-child nodes spanning multiple tables and can traverse relationship graphs, for example, "Search for servers that depend on databases".


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

AI Agents \(Glide Family\)

 PRB1994390

</td><td>

After a Zurich upgrade, hundreds of thousands of log entries are generated by CacheInvalidationEventHandler

</td><td>

The message is 'No endpoints available for cache invalidation'. The source is com.glide.ui.ServletErrorListener.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1992835

 [KB2804238](https://hi.service-now.com/kb_view.do?sysparm_article=KB2804238)

</td><td>

A deprecated Classic App Manager URL causes issues on some instances

</td><td>

Users have access to the Classic App Manager by navigating to the URL '/$allappsmgmt.do'. When they switched to new app manager later, and load the 'My company applications' page, that can corrupt the App Manager checksum cache, which causes the manual sync to fail.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Cloud Encryption

 PRB1980759

</td><td>

Prevent erroneous tampered DARE Properties notifications emails from being set to users

</td><td>

The error message, 'The tampering activities for Cloud Encryption properties have been found' is found in the logs.

</td><td>

 

</td></tr><tr><td>

Performance Telemetry

 PRB2003266

 [KB2897634](https://hi.service-now.com/kb_view.do?sysparm_article=KB2897634)

</td><td>

Upgrade from Australia RTP to a later Australia release fails

</td><td>

The instance becomes stuck when upgrading from an Australia release to another Australia release \(for example, RTP to EA\). However, instances can upgrade from outside of Australia into Australia successfully \(for example, Zurich to Australia\).

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1980521

</td><td>

Dashboard filters are not applied for scriptable multivis

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Time Card Management

 PRB1988000

 [KB2760220](https://hi.service-now.com/kb_view.do?sysparm_article=KB2760220)

</td><td>

Managers are no longer able to add time cards for their direct reports in the Time Sheet Portal

</td><td>

Managers are no longer able to add time cards for their direct reports and delegates in the Time Sheet Portal.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB2002003

 [KB2901692](https://hi.service-now.com/kb_view.do?sysparm_article=KB2901692)

</td><td>

Stuck semaphore due to the call glideUxInteroperableRoutesProvider.getInteroperableRoutesByIds\(\)

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1999010

 [KB2817637](https://hi.service-now.com/kb_view.do?sysparm_article=KB2817637)

</td><td>

The scheduled job, 'Time out abandoned Virtual Agent \(VA\) conversation' closes the conversation

</td><td>

'Time out abandoned VA conversation' should not close the conversation if the idle timeout is not completed.

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

Access Analysis Instrumentation API

 PRB1990716

</td><td>

Add agentic support in access simulation and compare use access

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1981898

</td><td>

Need properties for better control of the scope where a security attribute script gets evaluated

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1996382

</td><td>

When setting glide.ui.escape\_text to 'false', forms break

</td><td>

 

</td><td>

1.  Open any Zurich instance.
2.  Upload the sys\_properties file for glide.ui.escape\_text.
3.  Run a /cache.do.
4.  Load any relevant record, such as 'Incident'.

 Expected behavior: The record should load normally with the glide.ui.escape\_text sys\_property activated.

 Actual behavior: A blank screen with a basic message at the top will call out the ampersand issue.

</td></tr><tr><td>

Activity Stream

 PRB1998124

</td><td>

Activity stream citations cause an increased page load time

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Open Service Operations Workspace.
3.  Open any incident record with a large amount of activity stream entries \(~2000 entries\).
4.  Open the browser's dev tools window.
5.  Select the 'Performance' tab.
6.  Select the **Record and reload** button.

 Expected behavior: The page load time shouldn't be affected by CitationHighlightBehavior.js and require less time.

 Actual behavior: The page takes about 6 seconds or more to fully load, and the 'Performance' tab displays that it is due to CitationHighlightBehavior.js.

</td></tr><tr><td>

Agent Chat

 PRB1989186

</td><td>

TaskUtilsSNC creates millions of sys\_cs\_collab\_chat when collaborative chat is not enabled

</td><td>

The sys prop com.glide.cs.collab.enabled is false on the instance, meaning collaborative chat is not enabled on the instance. Despite this, there are millions of sys\_cs\_collab\_chat records created.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1990618

</td><td>

Live agent connection is not established with the utterance and **Contact** button for non-admin requestors

</td><td>

Even though there is an agent available online, the requestor sees no agents available in the Agent Workspace.

</td><td>

1.  Log in as an agent.
2.  Mark the agent as online.
3.  Log in as non-admin requestor.
4.  Navigate to **/aix/employee/chat**.
5.  Enter **Live agent**.

Notice that no agent connection is established with the message 'Live agent engaged. Connecting you to a live agent now. Please hold while I transfer you to a human support representative' on the client side.

6.  Select **Support**.

 Expected behavior: The live agent is connected and the work item is displayed in the Agent workspace.

 Actual behavior: No agent is available, even when the agent is available in the workspace.

</td></tr><tr><td>

Agent Chat

 PRB1997855

</td><td>

Upgrade the i18n library to support the BCP-47 variant

</td><td>

The replacement library should support the broad specification requirements set out in IANA BCP-47, which include language, script and territory codes. This is a large file, so the library chosen may opt to contain a smaller subset.

</td><td>

1.  Have Dynamic Translation set up on Agent Chat.
2.  Start a conversation with language 'fq'.

 Expected behavior: On the agent side, observe a message 'Message will be automatically translated from Canadian French'.

 Actual behavior: The language isn't displayed at all, or in some cases, the region code isn't correctly handled.

</td></tr><tr><td>

Agent Chat

 PRB2004301

</td><td>

AI agent prioritization is not functioning correctly when the 'Include AI Agents' option is enabled

</td><td>

 

</td><td>

1.  Install glide.awa and nowassist-ai-agents plugins on a Zurich or Australia instance.
2.  Enable 'Include AI Agents' for a assignment rule which has both AI agent and manual agents.
3.  Start a incident.

 Observe that incident is not assigned to an AI agent as preference even though it is available.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1981261

</td><td>

Make agent and tool columns non-mandatory in sn\_aia\_agent\_tool\_m2m and fix the empty cacheconfig name issue

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1997916

</td><td>

The extra 'response' layer in the JSON input passed by the agent to a scripted tool, causing performance issues

</td><td>

The final tool of creating the regulatory change tasks expects the input to be in the format - \{ 'finalPlan\_json': \{...\}, 'finalPlan\_html': '...' \} But with the latest code one 'response' layer is added, which causes performance issues.

</td><td>

Scenario 1:

 1.  Log in to an instance.
2.  Navigate to **/now/risk/compliance/record/sn\_grc\_reg\_change\_regulatory\_feed**.
3.  Open a record.
4.  Navigate to **AskNowAssist** &gt; **Get action plan**.
5.  Select **Yes** after the action plan is displayed.

 Notice that number of regulatory tasks in the related list doesn't change, tasks are not being created.

 Scenario 2:

 1.  Create a skill tool that outputs a JSON object.
2.  Create a script tool that takes the skill output JSON as input.
3.  Return that input as is for displaying in VA.

 Expected behavior: The JSON object returned by the skill tool should display in VA.

 Actual behavior: The JSON object will be wrapped/contained in a format like this: \{ response: \{ model\_output: 'actual JSON object' \}\}

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2001188

</td><td>

True-up 6.0 to Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2002014

</td><td>

Data to glide from offglide is not logged with the actual user

</td><td>

When the user makes a set cache call to glide from offglide, they observe that any record updated or created does not have an actual user in the **created\_by** or **updated\_by** field.

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

AI Search \(glide\)

 PRB1925238

</td><td>

AI Search should reuse the filter generated for each request instead of generating a filter again each time

</td><td>

The pre-processing time with Genius Results takes more time.

</td><td>

1.  Navigate to **Search preview**.
2.  Select a profile.
3.  Perform a search.
4.  Record the pre-processing time for search.
5.  Navigate to that profile.
6.  Remove all the Genius Result \(GR\) configurations.
7.  Re-run the search in the 'Search' preview.
8.  Observe the pre-processing time.

 Expected behavior: The pre-processing time with GR as opposed to without GR isn't different since the filter generated from the first request is being used.

 Actual behavior: The pre-processing time is more than double with GR.

</td></tr><tr><td>

AI Search \(glide\)

 PRB1988725

</td><td>

The non-standard role name causes the KB not to be returned in early binding

</td><td>

The KB is not returned when performing the search as a non-admin user.

</td><td>

1.  Open a base instance.
2.  Create a non-stardard role containing an uppercase letter and space, such as 'CSC - Knowledge'.
3.  Create a KB.
4.  Fill the **Role** field with 'CSC - Knowledge'.
5.  Perform a search as a non-admin user targeting that KB.

 Expected behavior: The KB is returned.

 Actual behavior: The KB is not returned.

</td></tr><tr><td>

AI Search \(glide\)

 PRB1989537

</td><td>

New tables added in Knowledge Graph AI Search pipeline

</td><td>

New tables added: sn\_kg\_tag\_table, sn\_kg\_tag\_column, sn\_kg\_tag\_table\_instruction, and sn\_kg\_tag\_column\_instruction.

</td><td>

 

</td></tr><tr><td>

AI Search \(glide\)

 PRB1990639

</td><td>

Late binding API check doesn't work for child tables

</td><td>

The log contains entries like '\[ais\] AclFilterGenerator: Exception during converting ACL for table kb\_template\_faq, use late-binding'.

</td><td>

1.  In ais\_datasource, set 'force\_late\_binding' for KB to true.
2.  Make sure KB plugins are installed to get child tables.
3.  Run search using a profile that has KB as the search source.

 Observe that the log contains entries like '\[ais\] AclFilterGenerator: Exception during converting ACL for table kb\_template\_faq, use late-binding'. When the user sets force\_late\_binding to true, the KB and its child table ACLs should not be translated to filters.

</td></tr><tr><td>

AI Search \(glide\)

 PRB1991218

</td><td>

Any portal should be able to enable hybrid search

</td><td>

When the user tries to enable hybrid search on global search, enablement is blocked.

</td><td>

Try to enable hybrid search on global search.

 Observe that enablement is blocked.

</td></tr><tr><td>

AI Search \(glide\)

 PRB1992181

</td><td>

There should be a secondary index in AI search

</td><td>

There should be an auxiliary index in AIS to store pre-generated questions and the corresponding docs. This will help in improving the recall for search and suggesting queries as a user types.

</td><td>

 

</td></tr><tr><td>

AI Search \(glide\)

 PRB1996321

</td><td>

An AI Search dynamic filter makes two calls \(one extra call\) when filters are applied, and in the second call, additionalContext is null and doesn't return correct counts on pre-processing

</td><td>

When filters are set to the empty array, the additional call doesn't happen and it works as expected. The issue happens when filters are set.

</td><td>

1.  Implement AISDynamicFilter pre-processing.
2.  Make an AI Search call by setting filters and passing additional context.

 Observe that an additional call is happening per search source. For the second call, the additionalContext value is null even though the additionalContext is passed as parameter to AI Search API call. If filters aren't applied, then the additional call doesn't happen. It happens when filters are applied and additionalContext is null when it should not be.

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1916303

</td><td>

External Content REST API external\_content/importUserPrincipals/\{target\_table\}/\{source\_id\} doesn't honor updates

</td><td>

The first insert is not honored unless there is more than one group.

</td><td>

1.  Using v4 ingestion API, import the user principals payload.
2.  Import user mapping.

Notice the first one honors groups and user insert.

3.  Update the payload to include another group.
4.  Send POST.

Observe that a group or user will be missing from the update.

5.  Delete the user mapping, user script above with single group and user mapping =.
6.  Send POST.

 Observe that the first insert is not honored unless more than one group is present.

</td></tr><tr><td>

AI Search

 PRB1796676

</td><td>

Users can't create a custom AI Search matcher on an indexed column with an aliased column name

</td><td>

It's not allowed by the business rule 'Verify index for exact match field'.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1822229

</td><td>

Query Performance metrics are down because it is polluted with the Genius Result configuration, making it difficult to find required information

</td><td>

When logging performance time breakdown, E2E search takes more than 5 seconds forais\_long\_query\_log. There are missing crucial performance metrics breakdown, and is polluted with Genius Result pre-processing and post-processing scripts.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1988802

</td><td>

additionalContext is not passed through the Suggestions GQL API to AI Search, preventing DynamicFilters from working for Virtual Agent \(VA\) skills

</td><td>

When additionalContext is passed from the client to the Suggestions GQL API, it was not being threaded through the call chain to the AI Search Suggestion Reader. This causes DynamicFilters to not work properly, preventing VA Skills from being returned in suggestion results.

</td><td>

Call the Suggestions GQL API with additionalContext parameter containing DynamicFilter information.

 Observe that the VA Skills that should be filtered by DynamicFilters are not being properly filtered, and the additionalContext is lost in the call chain and never reaches the AI Search service where DynamicFilters are applied.

</td></tr><tr><td>

AI Search UX

 PRB1991226

</td><td>

Search-based suggestions should have a user-friendly label for source

</td><td>

 

</td><td>

Call the Suggestions GQL API with a term that will return search-based suggestions.

 Expected behavior: The payload has the source label field for user-friendly labels based on what is configured for the corresponding source's 'Source Facet Bucket' label on the Search Application.

 Actual behavior: There is no label based on the Source Facet Bucket.

</td></tr><tr><td>

AI Search UX

 PRB1994511

</td><td>

Label in header-section\_\_identifier-container does not reflow

</td><td>

The labels in div class 'header-section\_\_identifier-container' are truncated at 200% and 400%.

</td><td>

1.  Open a base instance with AI Search.
2.  Navigate to /sp?id=search and search for something that will return results \(for example, email, device\).
3.  Set your window size to 1280x1024.
4.  Zoom in to 200% and 400%.

 Expected behavior: Content is not cut off at 200% and 400% zoom

 Actual behavior: Content is cut off at 200% and 400% zoom

</td></tr><tr><td>

Analytics Export API

 PRB1995410

 [KB2810683](https://hi.service-now.com/kb_view.do?sysparm_article=KB2810683)

</td><td>

On demand list visualization export to .xlsx

</td><td>

An issue has been identified where on-demand exports of list data visualizations intended for XLSX format are instead exported as XLS files in the Zurich environment. This behavior differs from the Yokohama environment, which previously exported successfully in XLSX format.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1971605

</td><td>

The base version is grayed out in the new Application Manager

</td><td>

The base version is grayed out in the new Application Manager, which stops to install the custom version created on the base version 1.0.0. The new Application Manager allows to install the custom version only on the latest version.

</td><td>

 

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

Application Rationalization

 PRB1990444

</td><td>

The **Update Hierarchies** button shuffles the hierarchy randomly for sub-capabilities

</td><td>

In the Enterprise Architecture Workspace \(EAW\), the **Update Hierarchies** button shuffles the hierarchy randomly for sub-capabilities when it updates for the first time.

</td><td>

1.  Navigate to **EAW** &gt; **Business portfolio**.
2.  Create a sub-capability for some parent capability.
3.  Add a few sub-capabilities \(with names like Test 1, Test 2, Test 3, etc.\).

Notice that the capability is added to the bottom.

4.  Select **Update Hierarchies**.
5.  Refresh the page.

Notice that the order of capabilities changed randomly.

6.  Delete the current sub-capabilities.
7.  Complete steps 2-5 again \(add capabilities with the same names and order again\).

 Notice that the order changes again and doesn't follow any logic.

</td></tr><tr><td>

Asset Management

 PRB1990771

</td><td>

Asset Analyst UI changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Asset Management

 PRB1992982

</td><td>

Query-range ACLs not present asset\_parallel\_job, ast\_execution\_queue and sn\_hamp\_import\_files tables

</td><td>

There are missing query\_range ACLs on ast\_execution\_queue and asset\_parallel\_job tables, which are used by the Asset Management parallel job framework for task execution and worker coordination. Without query\_range ACLs, the parallel job framework could experience access denied errors when querying task queues, causing job execution failures, performance issues, and broken monitoring functionality.

</td><td>

 

</td></tr><tr><td>

Attachments to Records

 PRB1998825

</td><td>

RCA is generated from the script include 'AttachmentSensitive' and UI Page: attachment

</td><td>

 

</td><td>

1.  Impersonate Abel Tuter.
2.  Navigate to **sn\_hr\_core\_case\_workforce\_admin.do?sys\_id=**.
3.  Select the **Manage attachment** icon.
4.  Add an attachment.

 Observe the two RCAs generated Source as 'UI Page: attachment' and 'Script Include: AttachmentSensitive'.

</td></tr><tr><td>

Authentication Factors

 PRB2002405

</td><td>

KBA using external sources

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2002406

</td><td>

Voice input for authentication parameters for non-KBA

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1990715

</td><td>

Token Exchange API for Voice Service Agent

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1981503

</td><td>

Race condition for frontend coverage persistence and aggregation calculations

</td><td>

Sometimes the frontend aggregation data is not accurate.

</td><td>

1.  Run an ATF test with a modified client script and UI action.
2.  Immediately after the test ends, select **Calculate code coverage** on the test result page.

 Observe that sometimes the frontend aggregation data is not accurate, as all the code coverage from the frontend hasn't been fully processed and persisted.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1997825

 [KB2806020](https://hi.service-now.com/kb_view.do?sysparm_article=KB2806020)

</td><td>

When the 'glide.script.block.client.globals' property is set to false, running an ATF test throws a client error with code coverage enabled

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Benchmarks

 PRB2000082

</td><td>

Success dashboard and benchmark Australia true up

</td><td>

True up versions for the Success Dashboard in Australia: itsm-analytics, app-benchmarks, success-dashboard-common, success-dashboard-core, and success-dashboard-itsm. This change is being made so that the ITSM licensing changes that are for Core ITSM would work as expected.

</td><td>

 

</td></tr><tr><td>

Build Agent \(glide\)

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

Build Agent \(glide\)

 PRB2002327

</td><td>

Keyword search returns full field content instead of relevant passages, causing excessive token consumption

</td><td>

The keyword search handler returns content fields in their entirety or applies a naive substring from the start of the field. It has no awareness of where query terms actually appear in the text. For large fields \(**Script**, **XML**, **Template**\), the relevant matching content is often beyond what is returned and is discarded.

</td><td>

 

</td></tr><tr><td>

Build Agent \(glide\)

 PRB2002763

</td><td>

Build Agent \(BA\) freemium install is blocked to due to hosted plugin, due to which NAFC install is incomplete

</td><td>

The BA trial version fails to install due to the missing hosted plugin.

</td><td>

1.  Provision an Australia instance.
2.  Navigate to Application Manager.
3.  Select the **Sync Now** button.
4.  Search Now Assist For Creator.
5.  Select **Install**.

 Notice that the install is successful, but the **Install** button is still active because BA trial version fails due to the missing hosted plugin com.glide.app\_build\_agent\_core.global.

</td></tr><tr><td>

Cache

 PRB1991677

</td><td>

The support for bulk loaded caches and unused entries cache should be removed

</td><td>

This is to disable the bulk-loaded caches from CacheReplication, which causes large amounts of traffic.

</td><td>

 

</td></tr><tr><td>

Cache

 PRB1993310

</td><td>

Query\_cache doesn't flush on all nodes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1963168

</td><td>

The HRSD Knowledge Graph is unavailable after an upgrade

</td><td>

There's an issue with the Now Assist Knowledge graph. The user receives the error 'An unexpected error occurred. Please try again.'

</td><td>

1.  Impersonate a user who has access to the HR Portal.
2.  Navigate to the HR Portal.
3.  Initiate a Virtual Agent Chat.
4.  Enter the prompt: 'Show me my open HR cases'.

 Expected behavior: Information about the user's open HR Cases is displayed.

 Actual behavior: The user receives the error 'An unexpected error occurred. Please try again.'

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1985492

</td><td>

New RCA records for attachment summarization

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1991031

</td><td>

Attachment Summary is not working when the HR case is transferred from one HR service to another service for Now Assist

</td><td>

Attachment Summary doesn't work on the new HR case with attachments after using **Transfer case**.

</td><td>

1.  Open an HR case.
2.  Upload an attachment.

Observe that attachment summarization is working fine.

3.  Select **Transfer case** from the side menu.

Observe that modal opens.

4.  Choose any transfer type \(for example, 'transfer to a new case number'\) and any New HR service \(for example, Dental Benefits Inquiry\).
5.  Select **Ok**.

Observe that this HR case transfers to a new HR case, and all the attachments are also copied to new HR case.

6.  Select **Summarize** on the new HR case.

Observe that attachment summarization is not available even though HR case has attachments.


 Expected behavior: Attachment summarization works on the new HR case with attachments after using **Transfer case**.

 Actual behavior: Attachment summarization doesn't work after using **Transfer case** on the on new HR case with attachments.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1995357

</td><td>

New RCAs from Knowledge Center to HR Core to use Open Prompt

</td><td>

Issues are observed when using the Open Prompt in HR Agent Workspace. Users try the Advanced Knowledge editor page in HR Agent Workspace. This page contains Open Prompt, which is interactable and helps create an article using Gen AI. For the Open Prompt to work without any issues, new RCAs are required.

</td><td>

1.  Provision an instance with the Knowledge Recommendation plugin and Article Optimization plugins installed.
2.  From the Knowledge Management properties, turn on the ece.
3.  Create an article from the related list of any HR case.

 There's an RCA from KC to HR core.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1997710

</td><td>

Update base instance sn\_hr\_po version to latest 6.0.3

</td><td>

For customers upgrading from a lower version to the latest version, the changes aren't applied as all the files are present in apply-once folder. A glide-fix was created, and the new version needs to be trued-up and backported to Australia.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1997296

</td><td>

Change templates should be created from model

</td><td>

**Create new template** should be enabled only if a model is selected, and the model should be passed to the change model page for creation.

</td><td>

1.  Navigate to **All** &gt; **Change** &gt; **Create new**.
2.  Select **More actions**.

Observe that **Create new template** is enabled.

3.  Select any model.

 Observe that **Create new template** is disabled.**Create new template** should be enabled only if a model is selected, and the model should be passed to the change model page for creation.

</td></tr><tr><td>

Change Management

 PRB1997298

</td><td>

Create change page in UI16 has the wrong color background

</td><td>

The background of the create page is colored in Polaris and Coral themes. It should be neutral and match other pages.

</td><td>

Navigate to **All** &gt; **Change** &gt; **Create new**.

 Observe that the background of the create page is colored in Polaris and Coral themes.

</td></tr><tr><td>

CMDB CI Class Models

 PRB1996229

</td><td>

Adding default values takes 4.5 hours during upgrade

</td><td>

Upgrading a clone from Zurich to Australia takes over 13 hours; a default value alone takes 4.5 hours. The table is cmdb\_ci\_vm\_object, the field is **persistence\_type**, and the default value they're setting is unknown.

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB1997526

</td><td>

LRU eviction and dynamic IRE cache

</td><td>

Dynamic IRE doesn't realize that some of its elements have been LRU evicted and doesn't attempt to rebuild the cache.

</td><td>

1.  Run dynamic IRE so that the cache gets initialized.
2.  Evict some of dynamic IRE's keys from the cache manually.
3.  Try and retrieve the evicted member from cache.

 Observe that dynamic IRE runs as though that element was never configured and does not exist.

</td></tr><tr><td>

Column Level Encryption

 PRB1990541

</td><td>

Attachment upload defaults to 'None' encryption module in the workspace

</td><td>

Attachment upload defaults to 'None' encryption module in the workspace, where as in Classic View its working as expected.

</td><td>

 

</td></tr><tr><td>

Condition Builder in Core UI

 PRB1991606

</td><td>

Condition builder can't interpret encodedQuery

</td><td>

The condition builder conditions aren't rendered. When other fields in the form are updated \(**Description**, **Name**, etc.\), the condition is erased from the record.

</td><td>

1.  Create a new glide record on sys\_archive table using a glide script.
2.  Navigate to /sys\_archive\_list.do?sysparm\_query=tableSTARTSWITHtask.
3.  Find the archive rule with the name 'Created from glide script'.
4.  Open the rule.

 Observe that the condition builder conditions aren't rendered. When other fields in the form are updated \(**Description**, **Name**, etc.\), the condition is erased from the record.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1814757

</td><td>

In CI Class Manager, users without the application picker can't update entries associated with tables outside the global scope

</td><td>

Logic was added to block an update if the user scope and table scope don't match. This is correct behavior for an admin or developer, which has an application picker available, but other users operate in the global scope and therefore can't make updates. For such users, rather than block the update, the backend should instead default to the correct target scope.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2000234

</td><td>

The scoped scriptable API to convert an LLM's output from Text 2 Query to QB executable output

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2000235

</td><td>

Data structures that allow assembling Query Builder JSON in a script from an LLM response

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Content Governance

 PRB1985066

</td><td>

Unable to reject Content Request Item \(CRI\)

</td><td>

Approvers cannot reject the CRI and it remains in a 'Requested' state.

</td><td>

1.  Install sn\_cg and sn\_cp.
2.  Create a Content Request and CRI.
3.  Add any content and schedule the content request item.
4.  Add Abel Tutor as approvers to the CRI using 'Manage approvers'.
5.  Move the CRI status to 'In Review'.
6.  Impersonate the user 'Abel Tutor'.
7.  Navigate to **hrm\_todos\_page**.
8.  Find the CRI and reject it.

 Expected behavior: The approver can approve or reject the CRI successfully.

 Actual behavior: There is a console error on the page, and the CRI is not getting rejected and remains in a 'Requested' state.

</td></tr><tr><td>

Content Publishing

 PRB1897913

</td><td>

**Insert and Stay** doesn't capture changes when inserting for a new record

</td><td>

The issue is specific to the Content Publishing package. The user reports **Insert and Stay** doesn't capture changes when inserting for new record. The new record still has previous values, leading to a degraded experience.

</td><td>

1.  Ensure that the Content Publishing package is installed.
2.  Navigate to the sn\_cd\_content\_portal list view.
3.  Open any existing content type: URL - record.
4.  Change the **Title** value.
5.  Navigate to **Context Menu** &gt; **Insert and Stay**.

 Expected behavior: The changes should be captured and established in the new record.

 Actual behavior: It does not. Previous values are retained.

</td></tr><tr><td>

Content Publishing

 PRB1963246

</td><td>

Issue with content template duration calculation with a different date format

</td><td>

If the user changes the date format in sys\_property, content template duration calculation is ignored since calculation looks for specific date format of 'yyyy-DD-mm'.

</td><td>

 

</td></tr><tr><td>

Content Publishing

 PRB1967769

</td><td>

Add RCAs and KG Tag for querying News/Company Event content in Now Assist Virtual Agent \(NAVA\) for Now Assist for EC Pro

</td><td>

Ensure that the necessary RCAs and provided and approved so that NAVA returns a response.

</td><td>

1.  Navigate to **Knowledge Graph Tag** to create a new record.
2.  Add relevant Content Publishing tables.
3.  Provide a description for KG Tag.
4.  **Save**.
5.  Navigate to **Conversational Interfaces** &gt; **Assistants**.
6.  Select **Manage Assistants** &gt; **Now Assist in Virtual Agent** &gt; **Information sources** &gt; **Knowledge Graph**.
7.  Set 'Natural Language Query' with Enterprise Graph.
8.  Under Tags, add the created tag from step 3.
9.  **Save**.
10. Create some sample news articles / company events.
11. Navigate to **/esc** to ask NAVA simple queries on news, such as 'Show me a news article' or 'Show me a company event.'

 Observe that any RCA's necessary are provided/approved, and NAVA returns a response.

</td></tr><tr><td>

Content Publishing

 PRB1980740

</td><td>

Notification email content sends with an empty body when Content Analytics is not installed

</td><td>

The subject is empty when it should be filled out, and the email body is 'undefined' in HTML.

</td><td>

1.  Navigate to **Content Publishing** &gt; **Create New** &gt; **Notification** &gt; **Email**.
2.  Fill out the required details.
3.  Add some rich text to the body.
4.  Save and create a schedule content to send the email.
5.  Check that the email was logged in the event queue with a valid parm2 value of the email body.
6.  Navigate to **System Log** &gt; **Email**to find the record in the email logs once it's processed.

 Expected behavior: The subject is filled out as the email content title, along with a valid non-empty body

 Actual behavior: The subject is empty and email body has 'undefined' value in the HTML.

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1988599

</td><td>

Migrating small archive tables to columnar is not an efficient use of RaptorDB capabilities

</td><td>

 

</td><td>

1.  Set up an instance for archive table migration.
2.  Start the migration.

 Expected behavior: Only archive tables which meet a TBD threshold should be migrated. There should be a scheduled job to look for tables which were previously skipped, but can now be migrated.

 Actual behavior: All archive tables are migrated immediately.

</td></tr><tr><td>

Data Archiving to Object Store

 PRB1999471

 [KB2820738](https://hi.service-now.com/kb_view.do?sysparm_article=KB2820738)

</td><td>

otherBlobsInChunkExist includes non-storage fields in coordinate comparison, causing premature S3 object deletion

</td><td>

The Archive Destroy job permanently removes archived records after they've aged past a configured retention period. It encounters a software defect that causes it to get stuck in a loop, repeatedly failing on the same set of records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1823749

</td><td>

In GraphMetadataAPI, node/edge types should allow special characters

</td><td>

An error appears that says only alphanumeric and underscore characters are supported.

</td><td>

With JSON or GraphMetadataBuilder, create an edge with type 'Depends On:Used By'.

 Observe the error that says only alphanumeric and underscore characters are supported.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1891525

</td><td>

Error appears when querying overridden node in child graph

</td><td>

The parent graph has a node with node\_type as 'sys\_user'. The child graph has a node with node\_type 'User', which overrides the parent graph node. When the user tries to execute the cypher query, an error appears: 'java.lang.NullPointerException: Cannot invoke 'org.json.JSONObject.getString\(String\)' because 'sourceNode' is null'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1909452

</td><td>

Scriptable GraphMetadata returns an unclear error message when KG's global graph \(an extended graph\) is run on the wrong scope

</td><td>

The NullPointerException error message can be confusing. To troubleshoot the problem, the user should check if the graph exists or check if they're on matching scope.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1932176

</td><td>

OutOfMemoryError when attempting to update the graph with as a parent graph

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1942189

</td><td>

Error message doesn't say that adding a WDF table with no primary key isn't allowed

</td><td>

The error message says 'Error: Table named u\_df\_wdf\_without\_pk is not allowed in graph schema.' The user may not know that WDF with primary key is a qualification to be considered in KG.

</td><td>

1.  Create a data fabric table with no primary key.
2.  Try to create a knowledge graph with that data fabric table.

 Expected behavior: An error message says that WDF tables with no primary key aren't allowed on the graph.

 Actual behavior: The error message says 'Error: Table named u\_df\_wdf\_without\_pk is not allowed in graph schema.' The user may not know that WDF with primary key is a qualification to be considered in KG.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1960120

</td><td>

In GraphQueryBuilder, an encoded query string with a blank value for the **int** field gives cytosm exception

</td><td>

 

</td><td>

1.  Add the encoded query string 'priority=3^state' to the incident node.
2.  Execute the query from GraphQueryBuilder.

 Observe the cytosm exception.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1960791

</td><td>

Incorrect cypher results for the union of two different nodes with same return fields using glideRecordDynamic

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1963974

</td><td>

Add support for getJournalEntry for xglideRecordDynamic

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1967640

</td><td>

Clean up the dangling temp table

</td><td>

dbi.truncateTable\(\) which was fixed by PRB1820374, but created a dangling temp table without cleaning up.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1967659

</td><td>

GraphQueryBuilder fails for a specific case with dot-walking in encoded in the query condition value

</td><td>

This issue occurs with the table 'Incident' and the encoded query 'caller\_id.sys\_created\_onSAMEASassigned\_to.sys\_created\_on@week'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1968921

</td><td>

Count\(\*\) throws an exception for Workflow Data Fabric tables

</td><td>

It works fine with glide tables.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1968949

</td><td>

Parent edges aren't inherited for children

</td><td>

Parent edges aren't inherited for children, but properties are inherited. For example, task edges aren't coming for an incident.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1970704

</td><td>

getJournalEntry not working when executed through javascript

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1973087

</td><td>

GraphMetadata.get\(\) should respect node type to table migration

</td><td>

Cached JSON is returned with node\_type and the custom node type is given.

</td><td>

1.  Create a graph without specifying migratedToTable flag and custom node type \(for example, User\).
2.  Specify migratedToTable flag.
3.  Call get\(\) method.

 Expected behavior: The node\_type should be the table name \(for example, sys\_user\) and the custom node type \(for example, user\) should be given as a synonym.

 Actual behavior: Cached JSON is returned with node\_type. The custom node type is given.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1973286

</td><td>

'getForTables' throws an exception if table doesn't exist on the anowassist instance

</td><td>

This causes Enterprise Graph to break.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1977551

</td><td>

A few queries break with function not allowed error

</td><td>

The queries were tested with strict security turned on and turned off, and they don't work in both cases.

</td><td>

Run any of the following queries:

 -   Select top 10 log\(cost\) from cmdb where cost != 0;
-   Select top 10 log10\(cost\) from cmdb where cost !=0;
-   Select top 10 mod\(priority,2\) from incident;
-   Select top 10 repeat\(first\_name,2\), first\_name from sys\_user;
-   Select top 10 replace\(first\_name,''a'',''ba''\), first\_name from sys\_user;
-   Select top 10 right\(first\_name,2\), first\_name from sys\_user;
-   Select top 10 second\(sys\_created\_on\), sys\_created\_on from incident;

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1979253

</td><td>

Return a value from GRD::getTableName

</td><td>

It throws a NullPointerException error.

</td><td>

Execute the script.

 Notice that a NullPointerException error is thrown.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1980455

</td><td>

Sharing permissions are not enabled for newly created documents for the upgrade customer in the DMS Component

</td><td>

Multiple issues are observed: 1\) Permissions are not enabled for newly created documents. 2\) The version attachment size is not displaying. 3\) There are improper error messages occur for missing permission configurations. 4\) Attachments from Cloud are not working from the Connect External Cloud Check.

</td><td>

Scenario 1:

 1.  Log in to the instance.
2.  Configure the Now Document component.
3.  Navigate to **Service Operations Workspace \(SOW\)**.
4.  Open any existing incident.
5.  Create a document.
6.  Select secondary actions, such as **Edit Metadata**.

 Expected behavior: Sharing permissions are enabled for newly created documents for Upgrade customers in the DMS component.

 Actual behavior: Sharing permissions are not enabled for newly created documents for Upgrade customers in the DMS component.

 Scenario 2:

 1.  Log in to the instance.
2.  Configure the Now Document component.
3.  Navigate to **SOW**.
4.  Open any existing incident.
5.  Create a document through the Document component.
6.  Select secondary actions, such as **Track Versions**.
7.  Upload any attachment to create a version.

 Expected behavior: Version attachment size appears in the component.

 Actual behavior: Version attachment size is not appearing.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1986124

</td><td>

Filter are not getting applied on the query, 'Give me name, company name and department name of users'

</td><td>

Filters are not getting applied on C2R, and returning records for department is not empty and company is not empty.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1986459

</td><td>

The 'Add OR Clause' with multiple filters is not working as expected

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1986877

</td><td>

Graph JSON cache should respect the 'isTieredCachingEnabledForCacheable' property value

</td><td>

GraphCacheableJSONString should be used for a tiered cache instead of a regular cache.

</td><td>

1.  Disable tiered caching.
2.  Call new sn\_db.GraphMetadata\(''graphName''\).get\(\).

 Expected behavior: The tiered cache with GraphCacheableJSONString isn't used.

 Actual behavior: The GraphCacheableJSONString wrapper is used even though the value is in a regular cache.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1987871

</td><td>

Add API to get the display column name from Table Descriptor

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1990139

</td><td>

Knowledge Graph support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1990516

</td><td>

WDF queries are not returning a response when result limit API option is passed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1997902

</td><td>

DatabaseView:extractTable doesn't properly handle views with selective fields included in them

</td><td>

 

</td><td>

1.  Create a view with an explicit set of fields from a table.
2.  Run extractTable.

 Observe the value for one of the fields that wasn't included in the view.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1998050

</td><td>

glide-side changes for label population in picker tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1999075

</td><td>

Reparents are processed too late

</td><td>

This is failing the validations in TableParentChange.java where it's ensured that table parents are only triggered during an upgrade. Thus, the re-parent attempts are aborted.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1995171

</td><td>

Subject tests fail on MariaDB on track/datamanagement

</td><td>

ColumnarTableSwapConsumerTest.verifyAccepting and DBColumnarOnlineAlterTest.verifyMigratingTable\_ThrowsException unit tests fail on MariaDB.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1910342

</td><td>

Handing RR candidates present in glide.db.properties

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1987583

</td><td>

IllegalThreadStateException when restarting the AHAMonitor thread

</td><td>

The AHAMonitor.start\(\) method throws IllegalThreadStateException when attempting to restart the monitor after it has been stopped and the thread has terminated.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1990629

</td><td>

Archive table dictionary entries are left in an inconsistent state after migration to RaptorDB

</td><td>

The max length of the archive table dictionary length entry matches the actual SQL length.

</td><td>

Migrate an instance to RaptorDB.

 Expected behavior: The max length of the archive table dictionary length entry is mismatched with the actual SQL length.

 Actual behavior: The max length of the archive table dictionary length entry matches the actual SQL length.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1990845

</td><td>

Prevent aha-monitor starting in head-less glide node

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1999067

</td><td>

TopologyManager should demote after timeout when the DB is not available

</td><td>

TopologyManager should demote itself after a timeout if it can't participate in the elections.

</td><td>

1.  Create a FAILOVER request.
2.  Attempt to slowdown the new PRI promotion by 60 seconds.

 Notice that glide side considers this as operation timed-out, and does not compute any new topology or detects the next failover.

</td></tr><tr><td>

Database Persistence - Graph

 PRB1947688

</td><td>

Datetime doesn't work with WDF tables

</td><td>

If the user runs a query that uses datetime, it doesn't return any results.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1952043

</td><td>

Unable to create sys\_meta\_graph\_edge record properly with source node and target node selected

</td><td>

The nodes can't be selected from the UI or directly imported from the attachment.

</td><td>

1.  Create a sys\_meta\_graph record with two nodes added.
2.  Create an edge between these two nodes.
3.  Try to select the two nodes as source and target node.

 Observe that the nodes can't be selected from the UI or directly imported from the attachment.

</td></tr><tr><td>

Database Persistence - Graph

 PRB1973162

</td><td>

Anowassist has a huge prompt for KG\(6.0.6\) invocation, causing high processing times

</td><td>

 

</td><td>

1.  Provision an anowassist instance with GenAI set up and platform 10.0.3 version and KG 6.0.6 installed.
2.  Perform any transaction that invokes KG.

 Observe the prompt and token count.

</td></tr><tr><td>

Database Persistence - Graph

 PRB1974718

</td><td>

Null value optimization must handle a case where Genius Results are reused and null everything again

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1975734

</td><td>

Duplicate query execution for sys\_scope \(child of sys\_package\) in GraphUtils for every iteration/execution

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1975735

</td><td>

Duplicate query executions for sys\_user during sample script iteration/execution

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1975738

</td><td>

Add support for AglideRecordOptimizer in glideRecordDynamic, especially for ArrayLoader implementation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1982912

</td><td>

DBSqlParser key injection must consider both local and cte keys when deciding whether to add additional ones in finalizeKeyInjection

</td><td>

An error message appears: 'com.glide.db.DBGraphApiException: Error executing cypher: FAILED TRYING TO EXECUTE ON CONNECTION...'

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1992704

</td><td>

Getting 'com.snc.db.graph.GraphMetadataSerializationException: Edge type is required' exception on CMDB tables

</td><td>

The exception, 'com.snc.db.graph.GraphMetadataSerializationException: Edge type is required.: org.mozilla.javascript.JavaScriptException: com.snc.db.graph.GraphMetadataSerializationException: Edge type is required' occurs.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1993285

</td><td>

Simple queries are timing out on Enterprise Graph and Enterprise Graph Mini

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1997411

</td><td>

The 'C2R Paginated' API fails for aggregated queries

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1998627

</td><td>

Return empty backing info rather than 'null' if there's no key for a select item

</td><td>

When a selectitem isn't mapped to a specific table/key, produce empty 'complex' backing info rather than 'null'. Null is reserved for a return if the select item doesn't exist.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1999021

</td><td>

Always use a table rather than its parent when injecting keys

</td><td>

When doing injections, it uses the primary key value, which is present in all the tables that make up a TPC class, but it may or may not include parents based on the select items/where clause. It's best to use the sys\_id in the child class.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1992095

</td><td>

There's an error in the cypher2ResultsPaginated API

</td><td>

There's an error executing cypher: 'FAILED TRYING TO EXECUTE ON CONNECTION Syntax Error or Access Rule Violation detected by database \(\(conn=103967\) Unknown column 'sys\_user0.sys\_id' in 'order clause'\)'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB1981897

</td><td>

Unable to retrieve the proper row count from glide Aggregate when using Group By Date/Floating Point/Decimal columns

</td><td>

The issue with the count distinct query is found in Australia. When adding an aggregate on either a Date, Decimal, or Floating Point column, the user encounters an error about missing parameters for concat function. As a result, count of groups is an incorrect number of groups since the distinct count query failed. When executing the script, users observe the script output query failed and the row count does not output the proper number of groups.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2001053

</td><td>

Data Interface is generated with database views with datafabric tables that should have the ACL generated with the data\_fabric operation on the view with the composite role

</td><td>

Currently, the query on the data interface queries all the implementations which can be DB view, glide tables, and datafabric tables. However when there is a DB view as a part of the interface, it complains that there needs to be data\_fabric operation ACL for the snloopback query.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2002769

</td><td>

The default security model for loopback data fabric queries is overly strict and will prevent user adoption

</td><td>

The default behavior of data fabric should allow users to access tables with remote tables if they already have access to that table using read ACLs. Currently, the default behavior is to block all access.

</td><td>

Attempt to query an SN table with Trino.

 Expected behavior: By default, the user should have access if they have read access to the table.

 Actual behavior: The user must have specific data\_fabric access granted to that table to run the query.

</td></tr><tr><td>

Database Views

 PRB1981902

</td><td>

Raptor DB view has mixed case prefix and '.' combination errors out

</td><td>

 

</td><td>

1.  Create a DB view between task\_sla and incident, and DB view table records with prefix with mixed case \(for example, the prefix 'inC' for incident\).
2.  Have the where clause as 'task\_sla.task = inC.sys\_id'.

 Notice that the execution errors out.

</td></tr><tr><td>

Data Fabric Table glide Services

 PRB1997363

</td><td>

Sys\_fields are silently dropped when importing a table from a local instance

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB2002718

</td><td>

Handle the entitlement check of the new ZCC App

</td><td>

The new ZCC app \(sn\_zcc\_primary / sn\_data\_fabric\_zcc\) is not correctly handling the plugin ID after the ZCC app split.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table glide Services

 PRB2004392

</td><td>

Metadata collectors multi-nested section **Choice** fields are not sent to the backend properly and auto-selected

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Fabric Table glide Services

 PRB2005520

</td><td>

Fix DataFabricStatsAccumulator to support new plugin sn\_zcc\_primary

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Data Product Backend Services

 PRB2000970

</td><td>

The asset **Internationalized Resource Identifier \(IRI\)** is not captured, which is needed for editing the data product

</td><td>

The asset **IRI** is a required field for editing the data product, and its absence prevents users from performing edit operations on data products.

</td><td>

1.  Navigate to the Data Product module.
2.  Create or open an existing data product.
3.  Attempt to edit the data product.

 Observe that the asset **IRI** is not being captured/stored, and that the edit operation cannot proceed or fails due to the missing asset **IRI**.

</td></tr><tr><td>

Data Snapshots

 PRB1987076

</td><td>

When the applied filter is removed, the values in the hierarchy breakdown revert to the original values even though the hierarchy toggle is still enabled

</td><td>

When filters on the dashboard with the applied breakdown hierarchy are removed, the hierarchy toggle does not toggle 'off'.

</td><td>

1.  Install the com.snc.pa.mlb and com.snc.pa.premium plugins.
2.  Navigate to **Data snapshots**.
3.  Create a new DS source with Data frequency as 'All Activity'.
4.  Add a fact table.
5.  Add supported fields in the fields section, such as assigned\_to.
6.  Navigate to **pa\_cdc\_breakdown\_hierarchy**.
7.  Add Manager Hierarchy as a record.
8.  Ensure the scheduled jobs have run and scores are collected in pa\_cdc\_fact table and pa\_cdc\_sysuser table for the breakdown hierarchy.
9.  Navigate to **Automated Indicators - Data Snapshots**.
10. Create a new DS indicator by selecting the source created in step 2.
11. Choose the standard calendar and daily frequency.
12. Choose the 'Aggregate' as 'Count'.
13. **Save** and submit the form.
14. Navigate to **Dashboards**.
15. Add any new visualization with the source created above with DB view as facts table.
16. Add a filter on the dashboard with the breakdown hierarchy.

Observe the scores.

17. Later remove the applied breakdown hierarchy.

 Expected behavior: When all the filters are removed, the hierarchy ID is removed, but on the UI side the hierarchy toggle should toggle off.

 Actual behavior: When all the filters are removed, the hierarchy ID is removed, but on the UI side the hierarchy toggle is not toggling off.

</td></tr><tr><td>

Data Snapshots

 PRB1994726

</td><td>

Cache issue with heatmap visualization and pivot table in Dashboards

</td><td>

The pivot table shows an empty matrix and the heatmap shows previously cached data. It should show 'No data available' when scores aren't available for both visualizations.

</td><td>

1.  Create an automated indicator with some combination of fields, like **Choice**, **Boolean** and **Reference** fields.
2.  Run the data collection jobs to enable data for the created indicator \(if not available already\).
3.  Create a heatmap visualization and pivot table.
4.  Add them to created indicator.
5.  In 'group by', select any **Reference** fields \(for example, **Assigned\_to**\).
6.  Add a filter to the groupby column configured in step 5.
7.  Select a reference record for which the score is available from the filter.

Observe the scores for that record on both visualizations.

8.  Remove the previously selected record.
9.  Add a record which doesn't have any scores.

 Expected behavior: It should show 'No data available' since the multivis API returns no scores.

 Actual behavior: The pivot table shows an empty matrix and the heatmap shows previously cached data.

</td></tr><tr><td>

Data Snapshots

 PRB1996565

</td><td>

Errors appear in syslog after saving/updating a data snapshots formula indicator

</td><td>

A TableDescriptor exception is thrown in the sys log table.

</td><td>

1.  Provision an instance with com.snc.pa.mlb and com.snc.pa.premium installed.
2.  Navigate to data snapshots formula indicator.
3.  Create an indicator with any formula.

 Observe that a TableDescriptor exception is thrown in the sys log table.

</td></tr><tr><td>

Declarative Actions

 PRB1995366

</td><td>

AI gradient support in Declarative Actions \(DA\) and UI actions in Workspace and Core UI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Developer Sandboxes

 PRB1981414

</td><td>

Upgraded warning listener is not registered unless nodes are restarted

</td><td>

The listener didn't run, resulting in no message created in sys\_dsb\_message.

</td><td>

1.  Enable DSBs.
2.  Do not restart the node controller.
3.  Create a sandbox.
4.  Run the script in the controller node.
5.  Check sys\_dsb\_message.

 Notice no message was created because the listener didn't run.

</td></tr><tr><td>

Developer Sandboxes

 PRB1991734

</td><td>

Sandbox\_user can't see the sandbox list in Sandbox Management Home

</td><td>

The sandboxes list is empty, but allocated sandboxes shows '1'.

</td><td>

1.  Create a sandbox.
2.  Switch to a sandbox\_user account.

 Observe that the sandboxes list is empty, but allocated sandboxes shows '1'.

</td></tr><tr><td>

DirectSQL

 PRB1997847

</td><td>

DirectSQL doesn't support local mapped data fabric tables

</td><td>

The path fails, so a change is needed in isDataFabricEngineQuery.

</td><td>

 

</td></tr><tr><td>

DirectSQL

 PRB2000509

</td><td>

'NOT BETWEEN' is translated as 'BETWEEN' with 'NOT' dropped

</td><td>

 

</td><td>

Use the query: SELECT number, priority FROM incident WHERE priority NOT BETWEEN 2 AND 4 ORDER BY priority, number.

 Expected behavior: It returns incidents where priority is outside the range 2-4, such as 'priority = 1' or 'priority &gt;= 5'.

 Actual behavior: Returns incidents where priority is inside the range 2-4 because the 'NOT' is dropped and the condition becomes priority 'BETWEEN 2 AND 4'.

</td></tr><tr><td>

DirectSQL

 PRB2000510

</td><td>

Simple 'CASE' expression is not supported

</td><td>

The execution fails with an exception.

</td><td>

Use the query: SELECT CASE priority WHEN 1 THEN 'Critical' WHEN 2 THEN 'High' WHEN 3 THEN 'Medium' ELSE 'Low' END AS priority\_label, number FROM incident ORDER BY 1, 2.

 Expected behavior: It returns each incident's number with a human-readable priority label derived from the simple 'CASE' expression.

 Actual behavior: The execution fails with the exception, 'Switch statements in case expressions are not supported.'

</td></tr><tr><td>

Discovery

 PRB1938058

 [KB2756546](https://hi.service-now.com/kb_view.do?sysparm_article=KB2756546)

</td><td>

Slow query from the status count optimizer impacts parallel launching of cloud app patterns

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1996875

 [KB2801169](https://hi.service-now.com/kb_view.do?sysparm_article=KB2801169)

</td><td>

Cloud Infra Patterns are launched per datacenter, impacting GCP Discovery Schedules

</td><td>

GCP Discovery schedules take significantly longer to complete because the system launches one pattern execution per datacenter instead of one pattern per service account containing all datacenters. This results in a significant increase in probe executions.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB2000665

</td><td>

Translation log causes an exception, preventing Discovery completion

</td><td>

 

</td><td>

1.  Initiate the Discovery process.
2.  Trigger the translation log functionality during Discovery.

 Observe that an exception is thrown, and the Discovery process does not complete due to the exception.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1988914

</td><td>

Add functionality for Input Router to consider an entire document set

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Dynamic Translation for Agent Chat

 PRB1988564

 [KB2776693](https://hi.service-now.com/kb_view.do?sysparm_article=KB2776693)

</td><td>

If Dynamic Translation for Agent Chat \(DTAC\) translation fails from agent to requester, the original message isn't sent

</td><td>

Note that messages from the requester to the agent still get delivered in the original language even though they aren't translated. Messages from the agent to requester don't get translated and don't get delivered.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Email Notifications

 PRB2002403

</td><td>

Extend the 'NotificationsEmailAgentsUtils' global script include with methods for notification, template, and layout creation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Encryption

 PRB2000179

</td><td>

glide\_encryption.set\_value\_support\_cle.disabled property can be modified by the user

</td><td>

The property can be set to 'true' by an admin user.

</td><td>

1.  Log in as an admin user.
2.  Type sys\_properties.list.
3.  Search for the property glide\_encryption.set\_value\_support\_cle.disabled.

 Expected behavior: The admin user cannot set the property to 'true'.

 Actual behavior: The admin user can set the property to 'true'.

</td></tr><tr><td>

Encryption Support

 PRB1992606

</td><td>

Duplicate Attachment EFCs are created for tables

</td><td>

During the upgrade, the autoCLEHealthScan job in the sys\_mass\_encryption\_job table detected unmigrated attachments. As a result, the 'CLE Unmigrated Attachments Health' indicator appears red, and the 'unmigrated\_attachment\_count' shows a value greater than 0.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1923711

</td><td>

Once the maximum size limit for impacted maintenance CIs is reached, the system is unable to re-evaluate them

</td><td>

When ImpactMaintenanceHandler.executeMaintenanceCalculation is triggered and the limit is reached, the maintenance job stops, and the system does not automatically re-evaluate the maintenance impact.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1990100

</td><td>

EM disable/enable jobs fix scripts unnecessarily manipulate the upgrade\_safe value during installation and upgrades

</td><td>

During upgrades within Zurich, some Event Management \(EM\) jobs can temporarily lose the upgrade\_safe flag. This happens because the EM 'before upgrade' fix script may execute unexpectedly. When upgrade\_safe is set to false on key EM scheduled jobs \(for example, 'Event Management - process events' and related connector/coordinator jobs\), those jobs may not run during the upgrade window. This can lead to delayed event processing or backlog while the upgrade is in progress.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1996008

</td><td>

Sometimes adjacent alerts aren't grouped even if there is a matching definition

</td><td>

The problem happens in Zurich when 1\) there are two tag-based definitions \(D1 and D2\) with the same or very similar filter and grouping conditions, and 2\) the definition D1 has a lower order and shorter timeframe window, while the definition D2 has a higher order and wider timeframe window. The problem is that two adjacent alerts fit to both definitions, but they're created with interval that's greater than the timeframe of the definition D1. Instead of being grouped by the definition D2, the alerts remain ungrouped. So the cause of this error is incorrect handling of isolated alerts.

</td><td>

 

</td></tr><tr><td>

External Content Connectors glide

 PRB1902996

</td><td>

Scriptable API fails when the table is yet to be indexed

</td><td>

 

</td><td>

1.  Install NAVA.
2.  Create new connector for AWS.
3.  Don't index anything.
4.  Run the script.

 Notice the error in background scripts.

</td></tr><tr><td>

Flow Engine

 PRB1997767

</td><td>

Flow execution tracking

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1990711

</td><td>

Text2flow glide changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1990712

</td><td>

Expose subflows and actions as Model Context Protocol \(MCP\) tools

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1995799

</td><td>

AI Search semantic search results aren't appearing for a non-admin user with only the flow\_designer role

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2002799

</td><td>

AISearch stops working when upgrading to latest Australia release

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Form Controller

 PRB1987560

</td><td>

Service Locations form bundle reference lookup spinner loads infinitely

</td><td>

Service Locations form reference lookup loads infinitely for Quote/Order/Opportunity entities in Australia glide, but works as expected in Yokohama and Zurich.

</td><td>

 

</td></tr><tr><td>

Form Controller

 PRB1990803

 [KB2811745](https://hi.service-now.com/kb_view.do?sysparm_article=KB2811745)

</td><td>

Users are unable to toggle checkboxes on system properties UI pages

</td><td>

 

</td><td>

1.  Navigate to any instance.
2.  Log in as an admin.
3.  Open any system properties UI page.
4.  Attempt to toggle any checkbox.

 Expected behavior: Users should be able to turn on or off checkboxes on properties pages to modify system configurations.

 Actual behavior: Checkboxes on UI properties pages are non-functional and can't be toggled.

</td></tr><tr><td>

glideRecord

 PRB1990713

</td><td>

MID Server core logic for Collector Framework

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Help Center

 PRB2003374

</td><td>

Integrate sn-help-assistant in the Next Experience app shell

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Help Center

 PRB2003375

</td><td>

Support dynamic guidance in the Help Centre

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1986687

</td><td>

ACL prevents topics being listed in hermes\_topic\_inspector for users without elevated privileges

</td><td>

Only one topic will appear if multiple topics exist. The console tab will list a JavaScript error for loadCell.children\[2\].onclick code.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB2004216

</td><td>

Update now-avatar properties to receive styling for AI avatars for AI Specialists

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1970657

</td><td>

Rename searchSharePointDocumentsAsUser to searchKTDocumentsAsUser

</td><td>

This is an update to a more generic name.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1985984

</td><td>

Adding RCAs to app-hr for app-cbs-hr for the migration of CBS to CBS for HR \(app-cbs\)\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2002907

</td><td>

RCA is missing for ZTSD for HR

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HTML Field Type Editor

 PRB1990982

</td><td>

Predictive text assistance

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HTTP Client

 PRB1986204

</td><td>

The **Test** UI action on the sys\_soap\_message\_function table causes large table handling query against ecc\_queue and causes memory contention

</td><td>

Selecting the **Test** UI action for a 'SOAP Message Function' \[sys\_soap\_message\_function\] record that has a 'MID server' specified causes the platform to send a test request to the MID server, and then poll for a response from the ECC queue. The query does not pass a valid value for the filter on the response\_to= filter, and so it can bring back hundreds to millions of rows, depending on how many rows are in the ECC queue.

</td><td>

 

</td></tr><tr><td>

HTTP Client

 PRB1992475

</td><td>

Asynchronous HTTP client upgrade for complete feature change

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Identity

 PRB1981341

</td><td>

Include trackable attribute in Machine Identity Console and Scripting Governance Tool's plugin.xml

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB1997896

</td><td>

HttpServletRequest is recycled during long transactions, which causes unhandled exceptions in HttpRequestAttributeAccessor

</td><td>

Long-running SOAP transactions, including ODBC queries, can fail to complete on Zurich instances due to an unhandled error during telemetry collection.

</td><td>

Scenario 1:

 Attempt to query large datasets using ODBC.

 Scenario 2:

 To reproduce using only SOAP, increase the max limit and query 30k&amp;\#43; records in a single request.

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB2000222

</td><td>

Integration Filter used to measure API Access Volumes is not applied to SOAP and JSONv2 requests

</td><td>

Certain internal inbound SOAP &amp; JSONv2 integration API requests count towards a user's data egress \(API Access Volume\) usage. These APIs are used for ServiceNow products. The customer licenses separately or are for supporting internal capabilities and should not be considered data egress.

</td><td>

 

</td></tr><tr><td>

Incident Management

 PRB1978573

</td><td>

Error displayed while creating an Interaction in Service Operations Workspace \(SOW\)

</td><td>

 

</td><td>

1.  Navigate to Service Operations Workspace.
2.  Select **Create Interaction**.
3.  Fill in the required fields.
4.  Save the Interaction.

 Notice that an error banner is displayed stating insufficient access for query\_range operation on sys\_user.email.

</td></tr><tr><td>

Incident Management

 PRB1989167

</td><td>

Make SDA role available for all of the customers irrespective of ITSM Roles plugin installation

</td><td>

The SDA role is installed only if ITSM Roles plugin is active on the instance, hence there are upgrade users still missing on this role. ITSM has introduced a new AI worker as part of ZTSD uptake and that AI worker uses the SDA role, hence the user must have the SDA role.

</td><td>

 

</td></tr><tr><td>

Incident Management

 PRB1989959

</td><td>

Restrict AI-native ITSM good SKUs to 'Incident' and 'Request Management'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB1997371

</td><td>

Clone the admin console, MIF fix, and true-up to 2.1.7

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1989692

</td><td>

Page details are missing from the execution details for Datastream Actions when run via FlowAPI

</td><td>

The 'Page Details' section is missing and the user is unable to view step-by-step execution data \(Pagination Setup, Integration Metadata, Step Configuration, API request/response\).

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB2003032

</td><td>

The connection\_admin user should be able to created/edit systems from WDF Connect Hub

</td><td>

 

</td><td>

1.  Log in as user with the connection\_admin role.
2.  Navigate to WDF connect Hub from navigator.
3.  Select **New** &gt; **System**.

 Expected behavior: The user should be able to create new a system.

 Actual behavior: The user is unable to create a new system.

</td></tr><tr><td>

Knowledge Graph \(Family\)

 PRB1986786

</td><td>

Renew the descriptions and automate the shipping pipeline for new tables, which should become the default

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1981407

</td><td>

After Zurich, the **Source Task** field for knowledge articles isn't assigned

</td><td>

This issue occurs when a user creates a feedback task record for a knowledge article. The feedback task allows knowledge managers to either edit the existing article or create a new one. However, when users attempt to create a new article from the feedback task, the new article doesn't reference the originating feedback task as it does in Yokohama. The **Source Task** field, which should contain this reference, appears in the article form view, but it is grayed out and empty.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1992747

</td><td>

Now Assist KB creation pop-up is unable to continue with the KB creation when no tasks are available for search

</td><td>

This issue occurs only in Native UI. Using the **Create knowledge** UI from Native UI during KB creation shows no options available to continue without selecting tasks. This blocks KB creation.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1993428

</td><td>

Remove the dictionary for standard

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1994772

</td><td>

Navigating to 'Create Knowledge' displays the interceptor page

</td><td>

This occurs when the KCS plugin is enabled and the CSM table map is disabled.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2006452

</td><td>

Launch AI Native SKUs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Language and Translations

 PRB1991979

</td><td>

GenAI translations merge for Zurich

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB2000694

</td><td>

RCA for AttachmentSensitive script include needs to be checked in

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1990986

</td><td>

Multi-record actions for end user flows

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1990987

</td><td>

Integrate a tracked list feature into the list experience

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1990988

</td><td>

To improve the AI in-product experience, indicate a row that's been generated by AI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1998776

</td><td>

Fix for WorkspaceTabsTooltipIT.testWorkspaceTabsTooltip test failures

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Views

 PRB1979390

</td><td>

'Edit columns' is not working, and no illustration appears when selecting 'Backlog personalize panel'

</td><td>

The added columns and the illustration are not displayed.

</td><td>

1.  Navigate to **Service Portal Workspace** &gt; **EAP**.
2.  Select any team backlog.
3.  Select **Personalize columns** in the header.
4.  Select any columns and apply it.

 Notice the new columns are not added to the backlog presentational list, and when selecting **Backlog personalize panel**, notice there is no illustration is present.

</td></tr><tr><td>

MetricBase

 PRB1982775

</td><td>

Test Connection utility returns a false positive result in multi Clotho environments

</td><td>

This issue was observed in multi-sharded and HA environments, and was not observed on a single endpoint Clotho.

</td><td>

1.  Provision an instance with multiple Clotho servers.
2.  Run the Test Connection utility from the Metricbase Configuration page.
3.  Change one of the fields in any one Clotho configuration to an invalid value. For example, provide an invalid username or give an invalid port number for the URL.
4.  Note down the original value.
5.  Run the Test Connection utility again.

Notice that it returns true, when it should fail since one of the endpoints is invalid.

6.  Change all configurations to an invalid one.

Notice the Test Connection test now fails as expected.

7.  Restore all endpoints to their correct values.
8.  Run Test Connection again.

 Notice that it passes now.

</td></tr><tr><td>

MetricBase

 PRB1985056

</td><td>

aha-monitor thread blocked by ClothoClientManager synchronization during database switchover

</td><td>

It is unable to process database switchovers, causing nodes to stall.

</td><td>

 

</td></tr><tr><td>

MetricBase

 PRB1994130

</td><td>

Weekly rollups happen on Thursday and monthly rollups happen a random day within the first week of next month

</td><td>

The rollup should always be executed based on the provided endTime parameter.

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

 Actual behavior: An error occurs, 'Script execution error: Script Identifier: null.null.script, Error Description: com.snc.clotho.ClothoException: com.glide.db.glideSQLException: Element doesn't exist. Table: mb\_dex\_installed\_app\_metrics col: false.'

</td></tr><tr><td>

MID Server

 PRB2002402

</td><td>

Trace collector epic for Zurich

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1990141

</td><td>

Mobile AI gradients update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1995814

</td><td>

Offline-online-offline incidental list doesn't load after syncing records that were created offline

</td><td>

The error 'Could not find application content in offline data' appears.

</td><td>

1.  Log in to the agent app.
2.  Download an offline cache.
3.  Go offline.
4.  Create a **Work order task** &gt; **Incidental**.
5.  Open the incidental.
6.  Add activity stream attachments.
7.  Sync.
8.  Go online.
9.  Go back offline.
10. Load the **Work order task** &gt; **** &gt; **Incidental**list again.

Observe the error 'Could not find application content in offline data'.


 Expected behavior: The incidental list loads offline and displays the created incidental with activity stream entries.

 Actual behavior: The offline-online-offline incidental list doesn't load after syncing records that were created offline.

</td></tr><tr><td>

Mobile Platform

 PRB2000325

</td><td>

Cell redirection action fails in Offline Mode after completing a task when multiple conditional buttons share the same cell location

</td><td>

The user observes the error 'Cannot find application content in offline data.'

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB1990234

</td><td>

Update the MMService plugin to support MMS async backend

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB1996320

</td><td>

JWT claims generation updates

</td><td>

The attachment table name is no longer needed since using the sys\_mm\_result record ID as the claim in the JWT.

</td><td>

Create a record with an attachment on a table configured in glide.platform\_mm\_service.supported\_tables.

 Observe the results in the sys\_mm\_result table , and the error message in the 'Error message' column.

</td></tr><tr><td>

Natural Language Query \(Family Release\)

 PRB1993465

</td><td>

MetadataInvalidationListener creates a NLQ-related tables hashset for every DB action, causing an increase in young object generation and also adding to performance cost

</td><td>

In the hot code path, the isNLQRelatedTables is called and it creates a list first and converts into a hashset for every DB action.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1887581

</td><td>

Selecting a new chat desktop notification doesn't bring focus to the tab that changed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist for Retail Service Management \(RSM\)

 PRB1999697

</td><td>

True up versions correction for Retail AI Bundle in Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist for Spoke Generation

 PRB1968315

</td><td>

Adding granular roles in text2spoke

</td><td>

Adding granular roles in text2spoke, and adding wdf\_builder instead of admin.

</td><td>

 

</td></tr><tr><td>

Now Assist in Document Intelligence

 PRB1999314

 [KB2916056](https://hi.service-now.com/kb_view.do?sysparm_article=KB2916056)

</td><td>

ServiceNow Now Assist In Document Intelligence \(NADI\) skill execution is blocked for inactive skill configurations

</td><td>

NADI Store application's 'Extract information from documents' and 'Multimodal Chat' skills may experience silent failures through the NADI release due to the skills being inactive by default. No error is surfaced, but skill execution is blocked. These skills are expected to be active by default upon an upgrade. The problem affects any capability that routes through DocIntel GenAI APIs without activating the skills explicitly in Now Assist Admin.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now Assist Panel

 PRB1988915

</td><td>

Pass context from Now Assist Portal to workspace

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1995707

</td><td>

When using Now Assist sidebar to summarize an incident, formatting for bullet pointed details \(for example, LAs and CIs\) are formatted improperly in Incident Summarization

</td><td>

 

</td><td>

1.  Open an instance.
2.  Navigate to any summarizable incident record.
3.  In the Now Assist sidebar, start a new chat.
4.  Enter, 'Summarize this incident.'

 Expected behavior: It is in a well-formatted summary.

 Actual behavior: The bulleted item text appears on separate line from bullets.

</td></tr><tr><td>

Now Assist Panel

 PRB2001558

</td><td>

Script fix to migrate voice input flag from NAA to Agent Studio running even for new users

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1998719

</td><td>

Prime skills can be executed through background scripts when only foundation apps are installed for AI Native SKU\]

</td><td>

This issue occurs on an instance that has asset subscription for Sentiment analysis for procurement case and only SPO - foundation app installed, which is installing NAFP - Foundation.

</td><td>

1.  Open an instance.
2.  Open **Now Assist Admin** &gt; **Finance &amp; Supply Chain** &gt; **Sourcing &amp; procurement operations**.

Notice that the sentiment analysis skill is hidden here.

3.  Open background scripts.
4.  Run the code to execute the sentiment analysis skill.

 Notice that the record sentiment analysis invoked.

</td></tr><tr><td>

OneExtend

 PRB1999920

</td><td>

BuilderEntityCache uses 100+ MB in Australia on Now Support, and it is mostly duplicate data due to domain keys

</td><td>

The cache is using a key based on the domain, so if 100 users load the same thing it will end up with 100 of the same entries in the cache. But it does not consider that all of the domains are actually using the same object.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2002764

</td><td>

KAA policy changes for supporting wrapped token

</td><td>

Scripted rest endpoints need to support BFF wrapped tokens.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2003281

</td><td>

Install log sync service only if com.glide.cs.genai is installed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2004072

</td><td>

Mosaic execution path needs to be handled via off-glide property

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2004938

</td><td>

Metadata changes to support Data Separation

</td><td>

Mosaic currently doesn't send the domain hierarchy to mosaic as a part of the metadata sync. We need this to enforce data separation at the mosaic end.

</td><td>

 

</td></tr><tr><td>

Outsourced Customer Service \(Family Release\)

 PRB1998333

</td><td>

Remove a few UI page ACLs in cs\_base/if/ocs plugin

</td><td>

Records appear when none are supposed to appear.

</td><td>

1.  Open a list of ACL roles.
2.  Apply the filters 'Application is OCS'and 'ACL.application is global'.

 Expected behavior: No records appear.

 Actual behavior: 8 records appear.

</td></tr><tr><td>

Performance Analytics

 PRB1995310

</td><td>

Null pointer exception is returned when creating a formula indicator from background scripts

</td><td>

The user should be able create a formula indicator without any errors when valid data is passed. Instead, the error 'Cannot invoke 'java.util.Map.containsKey\(Object\)' because 'nameToSysIdMap' is null' is returned.

</td><td>

1.  Navigate to the background scripts execution page.
2.  Run a script to create a formula indicator using the automated indicator.
3.  Check whether a formula indicator is created.

 Expected behavior: The user can create the formula indicator without any errors when valid data is passed.

 Actual behavior: The error 'Cannot invoke 'java.util.Map.containsKey\(Object\)' because 'nameToSysIdMap' is null' is returned.

</td></tr><tr><td>

Performance Analytics

 PRB1999049

 [KB2828943](https://hi.service-now.com/kb_view.do?sysparm_article=KB2828943)

</td><td>

There's malformed pa-ai-canvas.properties, as they are missing commas in the entire dependency list

</td><td>

In oob-pa-ai-apps/src/main/oob\_apps/pa-ai-canvas.properties, the 3.0.14-dependencies block has no commas between any dependency entries. Every line uses backslash continuation without comma separators.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1995297

</td><td>

KPI Details artifact has missing navigation icons

</td><td>

The kp-details page doesn't have an icon next to the title that navigates back to the library page.

</td><td>

1.  Open Platform Analytics Workspace.
2.  Open library.
3.  Select **Indicators**.
4.  Select an indicator.

 Observe that the indicator opens in a new page. The kp-details page doesn't have an icon next to the title that navigates back to the library page.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1969752

</td><td>

Cached toolbox items cause options to remain in a previously selected language

</td><td>

While working on the Platform Analytics Dashboard and Data Visualization modules, users have observed that the language in the right-hand menu changes automatically without any user action. The issue occurs intermittently. Sometimes, it appears only in a single browser session, while at other times it affects multiple browsers simultaneously. No consistent trigger has been identified so far. Users report that refreshing the page or clearing the cache may temporarily resolve the issue, but it can recur unpredictably.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1970352

</td><td>

Not enforcing the ACL in DataManagerService.getWidgetProps

</td><td>

ACLs in DataManagerService.getWidgetProps should not be enforced.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1983811

</td><td>

Unexpected response format for users without assigned roles

</td><td>

The API should return properly formatted JSON with error code, but instead it returns an invalid format.

</td><td>

Run GetMobileVisualizationIT\#verifyAsNoRoleUser.

 Expected behavior: The API returns properly formatted JSON with error code.

 Actual behavior: The API returns an invalid format.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1989067

</td><td>

Remove the info banner on Core UI dashboard overview page

</td><td>

The new 'com.glide.par.coreui.migration\_banner.enabled' system property was introduced to configure the appearance of the migration banner.

</td><td>

1.  Set the system property com.glide.par.unified\_analytics.enabled to false.
2.  Navigate to the CoreUI dashboard overview page: $pa\_dashboards\_overview.do.

 The following info banner is displayed: 'If you can't find the dashboard you're looking for, try the Platform Analytics library. Visit Platform Analytics experience.'

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1989343

</td><td>

After a glide upgrade, dashboard HTML rich text widgets are missing spaces that originally separate the boldfaced text

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2000628

</td><td>

DashboardWidgetDao.update\(\) does not persist **widget\_props** field

</td><td>

When updating a dashboard widget record via DashboardWidgetDao.update\(\), the **widget\_props** field is not written to the par\_dashboard\_widget table. The create\(\) method correctly calls gr.setValue\(WIDGET\_PROPS, widget.getWidgetProps\(\)\), but the update\(\) method is missing this call. This causes widget-level property overrides \(for example, followFilters, header color, header title\) to be saved on initial widget creation but silently lost on any subsequent dashboard save.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2002612

</td><td>

Filters should expose the new filter **Custom ID** field

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1972851

</td><td>

Hide the info message if 'com.glide.par.coreui\_single\_migration.enabled' property is 'false'

</td><td>

 

</td><td>

1.  Create CoreUI dashboard \(pa\_dashboards\).
2.  Add Dynamic content block to it.
3.  Set 'com.glide.par.coreui\_single\_migration.enabled' system property to 'false.'

 Expected behavior: The info message should be hidden

 Actual behavior: The info message is shown.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1982635

</td><td>

Support for report\_group and report\_global roles to edit visualizations

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1986034

</td><td>

Unified property is not set to 'true' after all content is activated

</td><td>

 

</td><td>

1.  Set 'com.glide.par.unified\_analytics.enabled' to 'false'.
2.  Navigate to **Migration Center**.
3.  Perform bulk migration.
4.  Activate all content.
5.  Check the unified property.

 Expected behavior: Unified property is set to 'true'.

 Actual behavior: Unified property remains false.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1988855

</td><td>

Static content block in core UI after migration has HTML tags in the Next Experience rich text visualization

</td><td>

 

</td><td>

1.  Create a core UI dashboard.
2.  Add a static content block.
3.  Add some contents within them, such as an embedded URL.
4.  Select the **Migrate to Next Experience** button to migrate the dashboard to Next experience.

 Notice that in the migrated Next Experience dashboard, the rich text has HTML tags in them.

</td></tr><tr><td>

Playbook Experience Core

 PRB1988859

</td><td>

PlaybookContextSnapshotService returns a stale cache when the process definition is reactivated

</td><td>

Upon returning to the workspace after reactivating the launch properties in the playbook the UI step shows outdated information.

</td><td>

1.  Create a Playbook with launch properties.
2.  Activate it.
3.  View it in the playbook workspace demo.
4.  Return to the playbook.
5.  Modify the launch properties, such as title description.
6.  Reactivate it.
7.  Return to the workspace.
8.  Refresh it.

 Notice the record generator/launcher UI step carries stale/outdated information.

</td></tr><tr><td>

Playbook Experience Core

 PRB1995058

</td><td>

The playbook portal page briefly shows 'There is no playbooks available' when a record is triggered

</td><td>

This only happens in custom layout type.

</td><td>

1.  Navigate to a playbook with a custom layout type.
2.  Once the record generator is loaded, trigger the record by selecting **C****ontinue**.

 Expected behavior: The playbook loads properly.

 Actual behavior: The page shows 'There is no playbooks available' briefly.

</td></tr><tr><td>

Playbook Experience

 PRB1978220

</td><td>

Old record generator forms that have forms selected show 'Show Create Record Form' is false when it should be true

</td><td>

All records in the list are 'false', when they should be 'true' if a form view is selected.

</td><td>

1.  Install the Process Automation Experience Demo plugin with demo data.
2.  Navigate to **/sys\_playbook\_experience\_record\_generator\_list.do**.

 Expected behavior: In the list and on the record, all the records that have 'Show Create Record Form' as 'true' if a form view is selected.

 Actual behavior: All the records in 'Show Create Record Form' are false in the list.

</td></tr><tr><td>

Playbook Experience

 PRB1986143

</td><td>

The **Declarative** action on the workspace form is executing twice in Zurich

</td><td>

This behavior was observed from the browser console logs, where the same log entries appear multiple times during a single execution, indicating duplicate runs of the action. This is likely due to DECLARATIVE\_ACTION\#CLIENT\_SCRIPT\_EXECUTION\_REQUESTED leaking out to the parent form, so that two forms are handling the action. The playbook component should catch this and set stopPropogation to 'true' so it doesn't leak to the parent form.

</td><td>

1.  Open a Zurich base instance.
2.  Configure a record generator for any form, such as incident.
3.  Add a field decorator for a field on that form by navigating to **All** &gt; **Field decorator**.
    1.  Set the table to 'Incident'.
    2.  Set the type to 'Client script'.
    3.  Have the script console.log something.
    4.  Enable this for all configurable workspaces.
4.  Navigate to a workspace.
5.  Create a new record to see the record generator.
6.  Select the **Field decorator** within the form of the record generator.

 Expected behavior: There is only one log.

 Actual behavior: In the console, it is logged twice.

</td></tr><tr><td>

Playbook Experience

 PRB1986820

</td><td>

Form section labels are not displayed at runtime

</td><td>

With the migration to the Form Controller in Zurich, the form preset configuration was applied. This preset is designed to hide form section labels, which results in the labels not being displayed at the runtime.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1983780

</td><td>

The **Create Flow Data** action gives the error, 'Unable to get source record of Process Automation Activity type'

</td><td>

This issue occurs in the global scope.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1991515

</td><td>

After a restart, the stage is still displayed even when the conditions aren't met

</td><td>

Remnants from the previous playbook lanes remain visible, although they appear in a 'PENDING' state. However, those lanes are reached, they update correctly.

</td><td>

1.  Navigate to **Configurable Workspace** &gt; **Lists** &gt; **AGR Connections** &gt; **All**.
2.  Create a record with subcategory 'WebEDI'.
3.  Proceed with Playbook.
4.  When asked for 'Fast Follower', select **True**.
5.  Proceed with Playbook until 'Packaging Data Exchange' \(lane 7\) is reached.
6.  Perform the complete Playbook restart.
7.  Proceed with Playbook to 'Validate Connection Type' \(activity 1.4\) activity.
8.  Change the subcategory to 'ClassicEDI'.
9.  When asked for Fast Follower, select **False** and proceed.
10. Proceed with Playbook until 'Testing' \(lane 9\) is reached.
11. Perform the complete Playbook restart again.
12. Proceed with Playbook to 'Validate Connection Type' activity.
13. Change the subcategory to 'WebEDI'.13. When asked for Fast Follower, select **False** and proceed.

Observe that the 'Fast follower' phase is initiated even if the fast follower is not marked, which isn't correct. Also, observe that even if the subcategory is 'WebEDI' now, the phases / activities for 'ClassicEDI' are still initiated, which isn't correct.


 Expected behavior: If fast follower is set to true, then WebEDI and ClassicEDI don't appear on the playbook. If fast follower is set to false, then WebEDI or ClassicEDI appear on the playbook.

 Actual behavior: If fast follower is set to true, WebEDI and ClassicEDI appear on the playbook. If fast follower is set to false, then fast follower, WebEDI, and ClassicEDI appear on the playbook.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2002088

</td><td>

**Locals** field is missing the **Enable AI agent** field

</td><td>

The **Locals** field on activity context is missing the **enable\_ai\_agent** field.

</td><td>

 

</td></tr><tr><td>

Playbooks

 PRB1985747

</td><td>

The 'On-demand' checkbox should not exist for create asset page in 29.0.x

</td><td>

This shouldn't occur for 29.0 versions.

</td><td>

Create a new playbook.

 Notice that 'Is On-Demand Playbook' is present on the 'Create new playbook' page.

</td></tr><tr><td>

Process Mining

 PRB1997134

</td><td>

Finding step criteria on OR conditions doesn't work

</td><td>

When the user mines the finding, it matches more records than expected and doesn't honor the step criteria.

</td><td>

1.  Create a finding definition.
2.  Create an OR condition.
3.  Give step criteria \(not cross-step criteria\) to one or more of the OR conditions.
4.  Mine the finding.

 Expected behavior: It matches the correct number of records which qualify for the step criteria.

 Actual behavior: It matches more records than expected and doesn't honor the step criteria.

</td></tr><tr><td>

Process Mining

 PRB1998650

</td><td>

sn\_gaf dependency is blocking A NAFC true-up install

</td><td>

The sn\_gaf dependency is missing, which blocks the true-up install.

</td><td>

Navigate to **Process Mining** &gt; **sn\_icu** &gt; **sn\_gaf NAFC**.

 Notice that a true-up install is blocked due to a missing sn\_gaf dependency.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB1961089

</td><td>

The the 'Inbound' state is in error, and inbound queue processing is blocked until this is addressed

</td><td>

This issue occurs even when the setup is successful, and the 'Consumer registration' state is moved to the 'Closed Complete' state on 'Impactuat.'

</td><td>

Update the instance.

 Notice that the inbound status of the RPS connection moves to an error state with following error, 'The current operation ended in state: ERROR. Detail: Error: Cannot find function map in object .,Detail: Cannot find function map in object. Adding 'ih\_sync\_inbound\_queue\_record' in attachments.'

</td></tr><tr><td>

Request Management

 PRB1992589

</td><td>

Create workflowStageProcessor script includes for getting stages

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB2002306

</td><td>

Turn on comments for CTASKs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1981411

</td><td>

The capacity is not displaying accurately, it appears in the Estimate outside plan section in Capacity Planning

</td><td>

When the user creates a demand and creates assignments for it, and selects **Create Project** in the demand, it will create project from demand. However, the resource allocation's **planning\_item** field does not update.

</td><td>

 

</td></tr><tr><td>

REST APIs

 PRB1986190

</td><td>

Scriptable OpenAPI spec support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

REST APIs

 PRB1986192

</td><td>

OpenAPI response header support for REST services

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

REST APIs

 PRB1986194

</td><td>

OpenAPI request and response support for REST services

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Retail Core

 PRB1999694

</td><td>

True up versions correction for the Retail bundle

</td><td>

The same build shouldn't operate in different ways when it's installed via Store vs true-up. There should have been a different release record that was A specific and that should have been trued up.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1973601

</td><td>

Potential load lot of future time limited roles, which may increase memory footprint

</td><td>

 

</td><td>

1.  Create time limited role window for 'admin' role for future start and end time, assign it to abel.tuter.
2.  Log in as abel.tuter.

 Even though all future time limited roles are not needed now, it will load in heap memory as a result of below PR.

</td></tr><tr><td>

Scripted REST APIs

 PRB1996583

</td><td>

There's high latency of the REST API scriptable

</td><td>

The existing scriptable methods jsFunction\_getDetailedServices and jsFunction\_getDetailedServicesWithOAuthPolicy had the withSchemaContent flag hardcoded to true, forcing retrieval of schema information for every API resource, which the MCP team doesn't need in the first step. This fix exposes withSchemaContent as an explicit parameter, letting the caller decide based on their use case.

</td><td>

 

</td></tr><tr><td>

Scripted REST APIs

 PRB2000233

</td><td>

Autogenerate OpenAPI specification content

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Search Administration

 PRB1968215

</td><td>

Elements must only use supported ARIA attributes for the**Search catalog** field for Service Portal \(SP\)

</td><td>

 

</td><td>

1.  Ensure there are multiple requests raised in SP.
2.  Launch a base instance.
3.  Navigate to **Request** on the header menu and activate it.

Notice that multiple records will be displayed.

4.  Choose any request.
5.  Open the Request summary.
6.  Navigate to **Search catalog**.

Notice that menu items are displayed.

7.  Run 'Evinced Flow Analyzer' and AXE devtool.

Observe the issue.


 Expected behavior: The ARIA attribute is not allowed as seen in 'aria-selected='false'' and an element's role supports its ARIA attributes.

 Actual behavior: Elements only use supported ARIA attributes, as seen in the element location: sn-search-combobox,sn-search-combobox-desktop,.-search-popover\_\_item--is-active.

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

ServiceNow Data Catalog \(glide\)

 PRB1997719

</td><td>

There are generic UI defects in the data collector

</td><td>

The URL value is truncated after saving and reloading.

</td><td>

 

</td></tr><tr><td>

ServiceNow Data Catalog \(Glide\)

 PRB2003264

</td><td>

Metadata collectors can't decrypt all passwords configured by the dcg-cc store app

</td><td>

When configuring dcg-cc to store an AWS access and secret key in the aws\_credentials table, the AWS key is missing and doesn't appear on the list of **Password** fields.

</td><td>

1.  Configure dcg-cc to store a **password2-type** field in the connection.extended attributes for a collection.
2.  Deploy the app to glide.
3.  Open wdf-meta/metadata-collector.
4.  Configure a collector.
5.  Select **Run**.
6.  Set a breakpoint in the KOS SPI class 'AbstractKosCollectorProvide'.

Notice that an encrypted string for the password, encrypted with a glide-specific key, which the collector doesn't have access to.

7.  Configure dcg-cc to store an AWS access and secret key in the aws\_credentials table.
8.  Open wdf-meta/metadata-collector.
9.  Configure a collector that requires AWS credentials.
10. Select **Run**.
11. Set a breakpoint in the KOS SPI class 'AbstractKosCollectorProvider'.

 Notice that the AWS secret key is missing, and that it isn't on the list of the six **Password** fields that work.

</td></tr><tr><td>

ServiceNow Data Catalog \(glide\)

 PRB2005266

</td><td>

IllegalStateException in tableAccessCheck\(\) when executing glide RDF queries

</td><td>

The RdfGraphStoreJSIT.writeMaxSizeTriple test is failing in the eco tests for the 'dcg-rdf-api-test' project.

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1996759

</td><td>

Null check for threadMember is incomplete for CollabMessageDto

</td><td>

The user can send a message but it's greyed out in the chat window until the user refreshes. The last sent message in a collab chat record doesn't update, so the discussion card in the utility menu never updates.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB1979790

</td><td>

Fix in-field error messages for SW model and PPN

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB1991257

</td><td>

User can't select a software model if multiple are found for PPN

</td><td>

Selecting **Import** just reloads the page without automatically selecting a software model, and a software model can't be selected from the field without clearing PPN.

</td><td>

1.  Create a PPN and two software models with details matching that PPN's DMAP.
2.  Import an entitlement with that PPN.

Observe that an entitlement import error is generated with the reason 'Multiple software models found for the Publisher Part number. Please choose a software model.'


 Expected behavior: There is handling for this situation, either preventing duplicate software models from being created, picking one of the duplicates during import or after selecting the **Import** button, or allowing users to select a software model without needing to clear the **PPN** field.

 Actual behavior: Selecting **Import** just reloads the page without automatically selecting a software model, and a software model can't be selected from the field without clearing PPN.

</td></tr><tr><td>

Software Asset Data Import

 PRB1993170

</td><td>

Pass the auto-incremenator using the unique ID of the table rather than using the contract number

</td><td>

There should be automation for both scenarios: 1. Uploading the docs, finishing the flow, and importing another doc to the same contract. 2. The asset covered from both docs should be part of the same contract.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB2001908

</td><td>

Rename the **Ignore** button to **Exclude**

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB2001911

</td><td>

Update text on the content opt-in page

</td><td>

Software entitlement details are extracted from software contracts using AI. Opt-in to the content service to help improve the prediction for product, publisher, and edition values.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2000639

</td><td>

Backport workspace changes of Job Failure Troubleshooting for Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

SQL API \(Server\)

 PRB1989263

</td><td>

Cannot execute a query against a physical representation of a long table name using SqlParser in physical mode

</td><td>

SqlParser throws an exception for the long table name, when the query should instead return a response with no records.

</td><td>

1.  Create a table with a very long table name, such as u\_very\_long\_table\_name\_abcdefghijklmnopqrstuvwxyz.
2.  Send a rest request to Trino Connector API /api/now/integration/trino/query/sql?sql\_type=physical&amp;connector\_type=loopback with body containing the following: SQL query: SELECT \* FROM .

 Expected behavior: The query returns a response with no records since the table doesn't contain any data.

 Actual behavior: The SqlParser throws an exception, 'Invalid table name.'

</td></tr><tr><td>

SQL API \(Server\)

 PRB1999140

</td><td>

Update the rate limit on SQL calls to 500/hour

</td><td>

 

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

 PRB1998573

</td><td>

Installing the 'ETL Consumer Kafka' plugin shouldn't enable 'Managed Hermes'

</td><td>

This dependency should be broken.

</td><td>

Install the 'ETL Consumer Kafka' plugin.

 Observe that 'Managed Hermes' is installed.

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

System Import Sets

 PRB1981092

</td><td>

Protocol version max length is not configurable for SCP and other data source file retrieval types utilizing SSH connections

</td><td>

The protocol version reverts to the default version size.

</td><td>

1.  Create a file type data source with the retrieval method SCP.
2.  Make a connection where the protocol version is longer than the default 512 characters.

 Notice that it takes the default protocol version size because there are no parameters being set to alter the default configuration of the SSHEngine/SSHConfig from the glideSSHSessionPool.

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

 PRB1962435

</td><td>

There's an incident form load issue due to the missing macro sn\_wwna\_nacm\_component, which causes a performance issue

</td><td>

When loading an incident form, the local host log is consistently flooded with the 'DBMacro WARNING \*\*\* WARNING \*\*\* Macro missing: sn\_wwna\_nacm\_component', and this is causing the form to load slowly.

</td><td>

1.  Open any incident record in the instance.
2.  Navigate to **System Diagnostics** &gt; **Session Debug** &gt; **Enable All**.

 Observe the error in the localhost log, users notice the warning called many times: 'DBMacro WARNING \*\*\* WARNING \*\*\* Macro missing: sn\_wwna\_nacm\_component'.

</td></tr><tr><td>

UI Field Administration

 PRB1970358

</td><td>

Zboot error comes from WWNA

</td><td>

The zboot error is in the localhost logs.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1990980

</td><td>

Add backend support for the multi-section configuration and fetch configurations in the UI to create the BE layer

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1990983

</td><td>

Support core IT use cases

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1993356

</td><td>

The g\_form.addModerateMessage\(\) API should display in a purple color both in UI16 and workspace, but displays in an 'AI' color in UI16

</td><td>

 

</td><td>

In on-load client script, add the line: 'g\_form.addModerateMessage\('moderate msg'\)'.

 Expected behavior: A purple color should be displayed for alerts.

 Actual behavior: It displays an AI color.

</td></tr><tr><td>

UI Form Administration

 PRB1993929

 [KB2908761](https://hi.service-now.com/kb_view.do?sysparm_article=KB2908761)

</td><td>

RCAs are created with the source as 'sys\_ws\_operation.do? sys\_id=6986d96dff7322102ae8ffffffffff48' for HR apps

</td><td>

An RCA is generated: 'RCA triggered - 'Read operation on table 'sn\_doc\_html\_template' from scope 'Global' was denied. The application 'Document Templates' must declare a Restricted Caller Access privilege. Please contact the application admin to update their access requests'. None should be generated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1994242

</td><td>

When 'glide.ui.escape\_text' is set to false, forms break

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1998771

 [KB2898934](https://hi.service-now.com/kb_view.do?sysparm_article=KB2898934)

</td><td>

Installing the com.glide.ai\_record\_activity plugin doesn't create the sys\_ai\_record\_activity table, causing NullPointerException errors

</td><td>

The user observes errors getting records for sys\_ai\_record\_activity: java.lang.NullPointerException.

</td><td>

1.  Install the GenAI Q4 feature or upgrade an existing instance.
2.  Ensure the plugin com.glide.ai\_record\_activity is installed.

 Observe the system logs or error output about an error getting a record for sys\_ai\_record\_activity: java.lang.NullPointerException.

</td></tr><tr><td>

UI Form Administration

 PRB2003359

</td><td>

Add a presence avatar for an AI specialist

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2003360

</td><td>

Remove the badge and pop-up modal from the 'Presence' icon

</td><td>

This is a product update.

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

Upgrade Center

 PRB1991306

</td><td>

On upgrade from Xanadu or Yokohama to Zurich, a 'Before' fix script runs even though it's not supposed to

</td><td>

The syslog contains relevant log messages.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1969282

</td><td>

Performance issues on various templates on the mainline due to frame change

</td><td>

This issue was observed in templates such as 'Core UI - Polaris Direct Homepage Load', 'Direct Incident List - Configurable Workspace', and 'Direct Incident Form - Configurable Workspace'.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1990140

</td><td>

Framework support for the AI screen reader Store app

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1991443

</td><td>

Support a form alert for AI gradient

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1996169

</td><td>

Screen reader doesn't announce the status message 'Extend your session'

</td><td>

The screen reader should announce the entire message inside the timeout pop-up.

</td><td>

1.  Install NVDA screen reader.
2.  Open an instance.
3.  Wait for the timeout pop-up 'Extend Your Session' to appear \(timeout is update 'glide.ui.session\_timeout' in system property\).

 Observe that the screen reader doesn't announce the status message 'Extend Your Session'.

</td></tr><tr><td>

UX Framework

 PRB1997499

</td><td>

The sn-canvas-tabs component displays a record preview popover on hover that is inaccessible to screen reader users

</td><td>

In configurable workspaces, there's a top level tab navigation region made up of the sn-canvas-tabs component. Hovering over a record tab in this region with a mouse triggers a popover to display a short preview of key fields on the record, like **Short description**, **State** and more. This is crucial information for agents to quickly differentiate between multiple tabs at a glance, but keyboard and screen reader users can't trigger or access the popovers.

</td><td>

1.  Navigate to a configurable workspace, such as Service Operations Workspace.
2.  Open at least two records.
3.  In the top level navigation tabs, hover over a deselected record tab.
4.  Note that a popover appears with a short summary of key fields for the record, such as **Short description**, **Priority**, and **State** \(varies by table\).
5.  Attempt to navigate record tabs with the screen reader enabled.

 Expected behavior: When a tab for a record has focus, the preview popover also appears and remains visible. Screen reader users should hear the details in the preview popover announced.

 Actual behavior: When the user navigates through the tabs, screen reader users report confusion because a record number isn't enough detail for many to remember which tab is which, and they aren't aware they are missing the preview popover details.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1992505

</td><td>

HTML rendering issues in alert analysis

</td><td>

 

</td><td>

1.  Navigate to Now Assist panel.
2.  Run alert analysis.

 Notice that the response contains HTML tags.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB2002310

</td><td>

Skills applicability changes as per the AI Native guidelines

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB2006402

</td><td>

AI connector node should hide custom skills based on foundation, advanced and prime plugins

</td><td>

In scenario 1, the custom skill in the skill type should only be available when there are no platform type installations on the instance or when the installation type is prime. It should be hidden in the skill type of AI connector node for advanced and foundation. In scenario 2, when there is no custom skill in the skill type, the AI agent should be selected on default for AI connector node. In scenario 3, the AI agents that are specific to list of subscription profiles sn\_ai\_plat\_fdn, sn\_ai\_plat\_adv or sn\_ai\_plat\_prm in sys\_gen\_ai\_asset\_subscription table should also be specific in the AI agents dropdown list of the AI connector node. AI agents that are not accessible for certain subscription profile should also be restricted to select from AI connector node.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1960339

</td><td>

The **Use an AI agent** action moves to a 'Waiting' state when called inside a flow-logic component

</td><td>

In a use case where calling the agent multiple times in a single subflow/flow using the flow-logic, the agent is initially called, but the second call goes into 'Waiting' state and no other calls go through. In the second call to the same agent \(with a different objective\), the execution record's state is 'Ready' and the message 'Conversation data is not populated' occurs for the second record. This leads the action to be in 'Waiting' state. The sysevent record is also not created.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1971595

</td><td>

Click metrics and deflection log

</td><td>

 

</td><td>

1.  Ensure **Citation** can be selected in the Synthesized Results.
2.  Update the output type.
3.  Track the previous clicks in sys\_cy\_analytics.
4.  Write back the 'state' of the citation clicked/auto-started to the 'Output' type column for completed asset tracking.
5.  Ensure citation/asset selection in Virtual Agent writes the correct deflection type, such as Catalog ≠Synthesized.
6.  Update the deflection log to filter out small talk to avoid unnecessary records.

 Observe that for agentic execution, the ending state is written back to the deflection log.

</td></tr><tr><td>

Virtual Agent

 PRB1974845

</td><td>

The FDIHServiceImpl object holds significant memory

</td><td>

com.glide.cs.qlue.module.fdih.FDIHServiceImpl is holding high memory

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1976905

</td><td>

'Error parsing additional context JSONObject\[''conversation''\] not found' issue for NLU Conversations

</td><td>

The error log occurs in the syslog when the user attempts a regular NLU conversation and it goes through a search flow.

</td><td>

1.  Attempt to have a regular NLU conversation.
2.  Ensure it goes through a search flow.

 Expected behavior: Flow goes through and the user receives results.

 Actual behavior: Flow errors out and goes to the fallback topic. When checking the syslog, the error log 'Error parsing additional context: JSONObject\['conversation'\] not found' is seen.

</td></tr><tr><td>

Virtual Agent

 PRB1977219

</td><td>

The **Max wait time**/no agent message isn't rendering hyperlinks in Portal, but it's working in Teams

</td><td>

When a URL is given in the **Max wait time** message field of the awa\_queue table, it's returning a hyperlink in Virtual Agent \(VA\) but working in Teams VA.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1980625

</td><td>

Skill name is missing the serializer, which appears to affect promoted VA topics from not showing as translated in VA

</td><td>

This issue was observed for \[sys\_gen\_ai\_skill\].skill\_name.

</td><td>

1.  Change the language to any language, such as French.
2.  Navigate to **/esc**.
3.  Trigger the 'Hello' message.

 Notice the untranslated string.

</td></tr><tr><td>

Virtual Agent

 PRB1983341

</td><td>

Greeting message is displayed at the end of the topic invocation in Now Assist Virtual Agent \(NAVA\)

</td><td>

The greeting is seen after selecting **Skill execution** from the Genius results. The greetings topic skips the greeting if global\_search\_text is present, but is undefined.

</td><td>

1.  Setup NAVA Enhanced chat without full page search on Service portal \(SP\).
2.  Use a search term on SP which provides a skill execution option, such as 'notification'.
3.  Select the **Skill execution** option from the Genius results.

 Notice the greeting.

</td></tr><tr><td>

Virtual Agent

 PRB1983377

</td><td>

In Enhanced Chat, the virtual\_agent flag is always set to false

</td><td>

In Enhanced Chat, the virtual\_agent flag has never been set to true. If users are starting the conversation in Virtual Agent \(VA\), irrespective of the assistant, the flag must be set to true.

</td><td>

1.  Set up NAVA with Enhanced Chat.
2.  Start a conversation in VA.
3.  Check the virtual\_agent flag on an interaction.

</td></tr><tr><td>

Virtual Agent

 PRB1984195

</td><td>

Interactions are reused every time the startVoiceInteraction Voice API is invoked

</td><td>

The API should create a new interaction, but instead it reuses the interaction if it's active. This used to work correctly in Yokohama, but is now failing.

</td><td>

Invoke the startVoiceInteraction voice API to create an interaction.

 Expected behavior: The API creates a new interaction every time it is invoked.

 Actual behavior: The API reuses the interaction if it's active.

</td></tr><tr><td>

Virtual Agent

 PRB1987016

</td><td>

Unread message call is made even before the session is established

</td><td>

A call to get unread messages occurs before the session established. This can be seen on the console logs.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1988044

</td><td>

hasUnreadMessages value for conversations in the chat history widget does not matches with values in the 'Recent chat updates' widget using OffglideScriptObject.getConversationsByConsumerAccount\(\)

</td><td>

The chat history widget 'now-lbf-chat-client' is using cache to show an 'unread' status for conversations. The 'Recent chat updates' widget is using the OffglideScriptObject.getConversationsByConsumerAccount\(\) API to fetch the latest five active conversations from the database. The 'unread' status for conversations in both widgets do not match.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1988112

</td><td>

All the closed chats have the same name

</td><td>

This issue occurs in Now Assist panel \(NAP\).

</td><td>

1.  Select **NAP**.
2.  Select **Chat history**.

 Notice that all the closed chats have the same name.

</td></tr><tr><td>

Virtual Agent

 PRB1989830

</td><td>

Additional assistantAttribues for Knowledge Graph NLQ: knowledge\_graph\_anchor\_tables, knowledge\_graph\_focus\_table, knowledge\_graph\_focus\_record\_id

</td><td>

To execute KG-NLQ, certain attributes are needed to be passed to the tool. Presently, AO is getting following Knowledge Graph keys in assistantAttributes: knowledge\_graph\_name, knowledge\_graph\_sys\_id, knowledge\_graph\_nlq\_schema\_sys\_id, knowledge\_graph\_nlq\_tags, knowledge\_graph\_nlq\_schema, knowledge\_graph\_tags. For Now Assist panel \(NAP\) conversation, additional attributes are required: knowledge\_graph\_anchor\_tables knowledge\_graph\_focus\_table knowledge\_graph\_focus\_record\_id. This is in parity with glide implementation of kgnlq.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1990020

</td><td>

The **Show more** button appears during streaming even when it's disabled

</td><td>

The **Show more** button should be hidden, but appears for a long response for the synthesized response and is hidden after streaming is done.

</td><td>

1.  Ensure 'sn\_nowassist\_va.synthesized\_response.shorten\_response.disabled' is set to 'true' so that the **Show More** button is hidden for the synthesized response.
2.  Ensure streaming is on.

 Expected behavior: On setting the property to 'true', **Show More** is hidden even while streaming.

 Actual behavior: When a long response shows up for the synthesized response, **Show More** is still shown during streaming and gets hidden after streaming is done.

</td></tr><tr><td>

Virtual Agent

 PRB1990179

</td><td>

Language Detection from French to English doesn't show the topic name in English

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1990700

</td><td>

Clean up sys\_ui\_message for translation/update translation for contextual actions

</td><td>

When the user ends the conversation, the closing conversation message isn't translated to the user language.

</td><td>

1.  Change the user language to anything other than English.
2.  In NLU mode, end the conversation.

 Expected behavior: The closing conversation message is translated to the user language.

 Actual behavior: The 'hi' contextual action isn't translated to the user language.

</td></tr><tr><td>

Virtual Agent

 PRB1991070

</td><td>

In the middle of a topic tool execution when CLOSURE intent is detected, the conversation is stuck

</td><td>

 

</td><td>

1.  Start a topic execution, such as 'Order stationary' \(which has a couple of questions to ask to the user\).
2.  When the tool execution starts and the first question is asked to the user, give the reply, 'Exit immediately.'

 Notice that the conversation gets stuck, and no incoming payload is sent to AO.

</td></tr><tr><td>

Virtual Agent

 PRB1991780

</td><td>

Execution gets stuck in the playground and in Now Assist panel \(NAP\) with the subflow/flow tool if there is no valid input

</td><td>

This issue may occur any time a tool needs an input. There should be proper error handling in these scenarios.

</td><td>

1.  Choose an agent, such as 'Order fruit flavored chocolate.
2.  Enter an utterance, such as 'order'.

 Notice that the execution is stuck and the input returns empty, leading the execution to be stuck.

</td></tr><tr><td>

Virtual Agent

 PRB1992132

</td><td>

The Virtual Agent \(VA\) link menu items are not displayed correctly

</td><td>

In Enhanced Chat, VA link menu doesn't show the labels the way it shows on the standard chat. Instead it shows the label as plain text and shows the link below. If the link is longer, it increases the width of the 'Contact support window'. It should only show the label and shouldn't show the link.

</td><td>

1.  Open the Menu items from the branding.
2.  Add a long link.

 Notice that the width of the window increases beyond the chat window, and the label is shown in plaint text and the link shows.

</td></tr><tr><td>

Virtual Agent

 PRB1992697

</td><td>

Live agent messages need to use callback URL to send to the user

</td><td>

Live agent messages are not being sent to the requester on lab instances because the URL in the http\_connection for off glide conversation messages is not correct. Live agent requests need to have a callback URL to send to the off glide conversation so that the messages go through.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1992728

</td><td>

Request ID missing in mosaic logs for conversation server requests

</td><td>

The request ID is null in mosaic logs.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1992729

</td><td>

Add preferred skills handling for Open Graph \(OG\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1993583

</td><td>

LLM calls time out after 60,000 milliseconds

</td><td>

Even when the system property 'com.glide.cs.dynamic.capability.timeout.f6f9e6e71bc38210f4200d81ec4bcb30' is set to 180 seconds, the LLM call times out after 60 secs.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1994599

</td><td>

Off glide code introduced an issue for DTAC when the agent sends a message to the requester

</td><td>

The dynamic translation for messages doesn't work when the agent sends messages to the requester. It throws NPE.

</td><td>

1.  Create a Zurich instance.
2.  Set up NAVA.
3.  Set up DTAC.
4.  Start a conversation between a requester and agent.
5.  Make sure the requester is in a non-English language and the agent is in English.

 Observe that dynamic translation for messages doesn't work when the agent sends messages to the requester. It throws NPE.

</td></tr><tr><td>

Virtual Agent

 PRB1996246

</td><td>

Workflow transfer context isn't working on Zurich

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1997012

</td><td>

Do not allow 'backup/fallback' URLs to be used for glide messages sent to OGCS

</td><td>

The callback\_url and pod\_ip must be present in the tool execution request, or the Live Agent context, or the session context \(for session-related messages back to OGCS\).

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1999793

</td><td>

Remove admin role

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2001326

</td><td>

Bot installation throws an error

</td><td>

Admin is redirected to an error page.

</td><td>

1.  Provision an instance with the latest Google Chat plugin \(3.0.0\) installed.
2.  Navigate to CI Admin Settings page for Channels and select **Google Chat** &gt; **Integrate with Now Virtual Agent**.

 Notice that Admin is redirected to an error page.

</td></tr><tr><td>

Virtual Agent

 PRB2003421

</td><td>

When localization is enabled and the agent is triggered in a non-English language through Now Assist VIrtual Agent \(NAVA\) or Now Assist panel \(NAP\), the agent fails to execute

</td><td>

A mismatch is caused because AIA uses the untranslated English name.

</td><td>

1.  Enable localization.
2.  Start a conversation in NAVA using a non-English language

 Expected behavior: Agent is executed successfully.

 Actual behavior: Agent fails to execute because the agent name lookup in AIA always uses the English \(untranslated\) name for comparison, causing a mismatch when a translated name is returned by the Unified Planner.

</td></tr><tr><td>

Virtual Agent

 PRB2006393

</td><td>

Plan to release the disambiguation feature

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2006856

</td><td>

Serial number when conversation moves across nodes

</td><td>

Virtual Agent gets stuck. New messages are sent but the client doesn't render them until the page is reloaded.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1825407

</td><td>

Unable to change ServiceNow VA message for com.glide.cs.general.multi\_file\_size\_exceed\_msg

</td><td>

Even if the value within com.glide.cs.general.multi\_file\_size\_exceed\_msg is modified, the following message is displayed: 'Looks like that file was too big to upload. 10 MB is the max.'

</td><td>

1.  Log in to a Washington DC instance.
2.  Navigate to **sys\_property - com.glide.cs.general.multi\_file\_size\_exceed\_msg**.
3.  Modify the value.
4.  Clear the cache.
5.  Create a virtual agent topic within designer.
6.  Add a 'File Picker' component.
7.  Test it by adding a file that's more than 10MB.

 Observe that the following message is displayed, even if the value within com.glide.cs.general.multi\_file\_size\_exceed\_msg is modified: 'Looks like that file was too big to upload. 10 MB is the max.'

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

 PRB1978992

</td><td>

The Portal Banner Carousel shows multiple widgets added for a single one

</td><td>

 

</td><td>

1.  Log in with admin access.
2.  Navigate to **sp\_config** page.
3.  Select **Designer**.
4.  Add a page.
5.  Add a container.
6.  Add the Portal Banner Carousel widget.

Verify only one widget was added on the Service Portal designer based on the page carousel.

7.  Verify the widget works when opened in the new page.
8.  Add another widget \(simple list widget\) to see if it's properly added.
9.  Add the following variables in Coral theme:
    -   now-dropdown-list--background-color-focus
    -   now-assist-selfservice\_FAB\_icon
    -   now-dropdown-list--background-color.

 Notice that they are displayed on the Network tab when the page loads.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1983355

</td><td>

Markdown to HTML parsing issues when there are special characters in the payload

</td><td>

 

</td><td>

1.  Create a topic in the designer with a text node with an response message containing a \` \(backtick\) character.
2.  Test the topic.

Notice the response shows unintended HTML.


 Expected behavior: Parsing is broken and links are highlighted.

 Actual behavior: The HTML output is broken.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1992017

</td><td>

The 'Thank you' text stays in chat even after sending and receiving response

</td><td>

This issue occurs with Now Assist panel \(NAP\).

</td><td>

1.  Log in to an instance.
2.  Open NAP.
3.  Enter, 'What is spam' followed by 'Thank you.'

 Expected behavior: The 'Thank you' text disappears after the message is sent.

 Actual behavior: The 'Thank you' text says in the chat even after sending and receiving response. It is also observed that other prompts like 'What is spam' appear in the chat until a response gets generated.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1996311

</td><td>

Add the 'fetchDocuments' attribute to be passed in contextData of the session API call request data parameters when switchContextConversation is 'true' and parsed from AIEL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1997398

 [KB2817799](https://hi.service-now.com/kb_view.do?sysparm_article=KB2817799)

</td><td>

The now-chat-window library build is missing the rem multiplier, which causes tiny text in the ENHANCED\_CHAT full screen portal

</td><td>

The now-chat-window component renders with small text \(10px instead of 16px\) when loaded via the ENHANCED\_CHAT path on Service Portal pages that set the root font-size to 62.5%. This as caused by changing the font-size in full-page.scss from an absolute pixel value to a rem-based theme variable.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1997587

</td><td>

'Start a new chat' from contextual Now Assist panel \(NAP\) doesn't map the conversation with a record

</td><td>

 

</td><td>

1.  Open a Service Operations Workspace \(SOW\) incident record.
2.  Launch contextual NAP by setting switchContextConversation on AIEX launcher.
3.  Pick a non-active conversation under the 'Incident' tab in the NAP conversation picker.

Notice that 'Start a new chat' shows at bottom.

4.  Select a conversation.

 Notice that the conversation opened doesn't get mapped to a record.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1999442

</td><td>

The live agent avatar changes when an image is sent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Walk-Up Experience

 PRB1981055

</td><td>

Image on the 'Walk up reservation' page does not display for users without a walk up role

</td><td>

Users checking in via URL cannot see the logo image in the portal unless they have the role 'sn\_walkup.walkup\_manager'.

</td><td>

1.  Impersonate a user who doesn't have the Walk-Up manager role.
2.  Navigate to the **Walk-up portal** to check in.

 Notice that the image will not appear on the page.

</td></tr><tr><td>

Word Document APIs

 PRB1987080

</td><td>

Word doc APIs fall back error separation handling for shared services

</td><td>

 

</td><td>

1.  Log in to ServiceNow.
2.  Hit Word doc APIs with the wrong URL.

 Observe that the fallback doesn't happen in a 404 case.

</td></tr><tr><td>

Word Document APIs

 PRB1987850

</td><td>

Issue with document sync when paragraph properties do not exist

</td><td>

An error occurs when attempting to sync the document. This issue occurs when the document was generated using ChatGPT or other AI tools, or when content controls are positioned on blank text.

</td><td>

1.  Make changes to the content control fields with 'Track Changes' on.

Observe that the selected paragraph should not have any styling.

2.  Attempt to replace the value.

 Notice that it will throw an error.

</td></tr><tr><td>

Work Order Management

 PRB1998755

</td><td>

Analytics data in manager mobile is not consistent with manager view

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Zero Copy Connector for ERP \(Family Channel\)

 PRB2000572

</td><td>

The com.glide.erp.core plugin has a namespace 'sn\_erp\_integration' which creates the conflict for the scope name for the zccforerp app, which is blocking public script includes

</td><td>

The com.glide.erp.core plugin has a namespace 'sn\_erp\_integration' which is creating the conflict for the scope name for zccforerp app which is blocking public script includes.

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \(glide\)

 PRB1995609

</td><td>

The Trino REST API throws an exception for tables with long names \(&gt; 30 characters\), because 'nonce' is generated as the table name

</td><td>

When accessing a Workflow Data Fabric \(WDF\) table that references a glide table with a name &gt; 30 characters, the Trino REST API throws an NPE: '2026-02-19 14:52:28 \(041\) TRINO\_REST-thread-37 8ECE056F474F32105679CCA4F16D437A txid=06cec96f474f TimingLogger \*\*\* ERROR \*\*\* Problem occurred while fetching DB response: Cannot invoke 'java.util.Set.iterator\(\)' because 'sqls' is null java.lang.NullPointerException: Cannot invoke 'java.util.Set.iterator\(\)' because 'sqls' is null'.

</td><td>

1.  Create a glide table with &gt;30 characters.
2.  Create a WDF table with a column that references a column in the glide table.
3.  Open the WDF table and include the reference column in the list view.

 An error displays on the page.

</td></tr><tr><td>

Zing Text Indexing and Search Engine

 PRB1996302

</td><td>

Installed applications aren't shown in application manager when the instance is upgraded to Australia

</td><td>

After upgrading an instance to Australia, installed applications \(present in sys\_store\_app\) aren't visible in the Application Manager UI when searched by name or scope. The issue occurs because the application isn't indexed by Zing Text Indexing and the Search Engine, which is required for search results to display correctly. This issue affects instances with customizations where 1\) the root table is not marked as Text Index, 2\) a child table is marked as Text Index at Collection level, and 3\) there are no columns within the hierarchy that are marked as Text Index.

</td><td>

1.  Access the Application Manager on an upgraded instance.

2.  Search for an installed application by name or scope.


 Observe that the application doesn't appear in the search results, even though it's listed as installed in the classic view.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia EA Hotfix 1](https://www.servicenow.com/docs/r/release-notes/australia-patch-0-hf-1-PO.html)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


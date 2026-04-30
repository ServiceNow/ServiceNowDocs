---
title: Zurich Patch 8
description: The Zurich Patch 8 release contains important problem fixes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-04-07"
reading_time_minutes: 72
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 8

The Zurich Patch 8 release contains important problem fixes.

-   **Zurich Patch 8 was released on April 07, 2026.**
    -   Build date: 04-02-2026\_1528
    -   Build tag: glide-zurich-07-01-2025\_\_patch8-03-20-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z08.00.xlsx).

## Overview

Zurich Patch 8 includes 338 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-zp8.png "Top 10 problem categories")

## Security-related fixes

Zurich Patch 8 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 8, refer to [KB2925552](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2925552).

## Changes in Zurich Patch 8

-   **[SQL API Release Notes](../now-platform-administration/sql-api-rn.md)**

    The ServiceNow® SQL API enables RaptorDB Pro users to bring their Business Intelligence \(BI\) tools to ServiceNow. Users can perform BI analytics on their ServiceNow data without mass data export. SQL API is only available with RaptorDB Pro.

-   **[Getting started with ServiceNow SQL API](https://www.servicenow.com/docs/access?context=getting-started-with-servicenow-sql-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    The ServiceNow SQL API provides data access to your ServiceNow instances through industry-standard ODBC and JDBC drivers, enabling direct connections from Business Intelligence \(BI\) tools and data analysis platforms.

-   **[SQL API architecture](https://www.servicenow.com/docs/access?context=sql-api-architecture&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    The SQL API architecture demonstrates how the SQL API plugin integrates with the ServiceNow system to provide secure, read-only data access through industry-standard ODBC and JDBC drivers.

-   **[Supported SQL functions](https://www.servicenow.com/docs/access?context=supported-sql-functions&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Common SQL functions used in SQL API for querying and analyzing incident data.

-   **[Configuring SQL API](https://www.servicenow.com/docs/access?context=configuring-sql-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    This section guides you through the complete setup process for the ServiceNow SQL API, covering both instance configuration and driver installation. You will configure your ServiceNow instance to enable SQL API access, set up the necessary security controls, and install the appropriate drivers on your client machine.

-   **[Create a Service Account and assign Roles](https://www.servicenow.com/docs/access?context=create-service-account&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Create a dedicated non-interactive Service Account in User Administration and assign the appropriate SQL API access role to enable secure, programmatic access for BI tools and analytics platforms.

-   **[Create Access Control Lists \(ACLs\) for SQL API](https://www.servicenow.com/docs/access?context=create-acls-sql-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Configure table-level access control using the egress\_sql and read operations to grant Service Accounts query access to specific tables through the SQL API.

-   **[Create IP filter criteria](https://www.servicenow.com/docs/access?context=create-ip-filter-criteria&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Define which IP addresses or IP ranges are permitted to connect to your ServiceNow instance via the SQL API ODBC/JDBC driver. By default, all incoming IPs are blocked until you configure the SQL API Authentication Policy with an IP filter and policy condition to allow access only from trusted client machines.

-   **[Download the SQL API drivers on client machine](https://www.servicenow.com/docs/access?context=download-sql-api-drivers&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Download the ODBC and JDBC drivers from the ServiceNow store to your client machine to enable SQL API connectivity.

-   **[Install ServiceNow SQL API ODBC driver on client machine](https://www.servicenow.com/docs/access?context=install-odbc-driver&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Install the ServiceNow ODBC driver on your Windows client machine to enable connectivity between your Business Intelligence \(BI\) tools and ServiceNow data through the SQL API.

-   **[Configure ServiceNow SQL API ODBC driver on client machine](https://www.servicenow.com/docs/access?context=configure-odbc-driver&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Configure connection settings for the installed ODBC driver including server URL and authentication credentials to enable data access from BI tools to your ServiceNow instance.

-   **[Test SQL API ODBC driver connection using Interactive SQL](https://www.servicenow.com/docs/access?context=test-sql-api-odbc-driver-connection-using-interactive-sql&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Run the Interactive SQL application for quick verification of connectivity and to test query results without using a full application.

-   **[Configure ServiceNow SQL API JDBC driver on client machine](https://www.servicenow.com/docs/access?context=configure-jdbc-driver&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Configure the JDBC driver settings on your client machine to establish a connection to your ServiceNow instance and access data through the SQL API.

-   **[Route SQL API calls to Read Replica](https://www.servicenow.com/docs/access?context=routing-sql-api-calls-to-read-replica&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    You can route SQL API calls to Read Replica to optimize the performance of your ServiceNow instance.

-   **[Common use cases for SQL API](https://www.servicenow.com/docs/access?context=common-use-cases-for-sql-api&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    The SQL API supports business intelligence reporting, ad-hoc data analysis, and custom report development.

-   **[Integrate SQL API Drivers with third-party BI tools](https://www.servicenow.com/docs/access?context=configure-drivers-bi-tools&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Configure ServiceNow SQL API drivers to connect with third-party business intelligence and database tools for direct data access and analysis.

-   **[Connect Power BI Desktop to ODBC driver](https://www.servicenow.com/docs/access?context=connect-power-bi-odbc&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Connect Power BI Desktop to your ServiceNow instance using the ODBC driver to access and analyze ServiceNow data. Create dashboards and reports that visualize your ServiceNow data.

-   **[Connect DB Visualizer to JDBC driver](https://www.servicenow.com/docs/access?context=connect-dbvisualizer-jdbc&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Connect the DB Visualizer database tool to your ServiceNow instance using the JDBC driver to query ServiceNow data. Access authorized tables and perform read-only queries on your ServiceNow data to create visualizations, and perform ad-hoc analysis using industry-standard SQL commands.

-   **[SQL API reference information](https://www.servicenow.com/docs/access?context=troubleshooting&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    This section provides details about SQL API reference information like minimum requirements, usage limitations, configuration issues, and frequently asked questions.

-   **[Minimum requirements and supported software for SQL API](https://www.servicenow.com/docs/access?context=minimum-requirements-and-supported-softwares&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    This section lists the minimum supported versions for ServiceNow server releases, client drivers \(ODBC and JDBC\), and Java Development Kit required for SQL API.

-   **[Usage Limitations for SQL API](https://www.servicenow.com/docs/access?context=usage-limitations&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    The SQL API imposes rate limits to ensure system stability and performance when querying ServiceNow data through ODBC and JDBC drivers.

-   **[Define a REST API schema](https://www.servicenow.com/docs/access?context=define-scripted-rest-api-schema&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    The following procedure describes the process for manual schema definition. For details about automatically generating request schema definitions in non-production instances, see .

-   **[Automatically generate API request definitions](https://www.servicenow.com/docs/access?context=autogenerate-api-request-definitions&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Use sample requests made to an API resource to generate request header associations, query parameter associations, and a request schema for that resource.


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

Discovery Probes and Sensors

 PRB1960340

 [KB2611107](https://hi.service-now.com/kb_view.do?sysparm_article=KB2611107)

</td><td>

Discovery's MID Server script files for Application Dependency Mapping are deleted during clones

</td><td>

The MID Server script file \(ecc\_agent\_script\_file\) records have attachments. These attachments may go missing after the instance is cloned, breaking Discovery probes. To retain the attachments of base instance code-related records in clones, the table\_name in the sys\_attachment table must be prefixed with ZZ\_YY. Discovery's names don't have that prefix, so the attachments may not be copied depending on the preserver/exclude settings for the clone.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1969766

 [KB2664275](https://hi.service-now.com/kb_view.do?sysparm_article=KB2664275)

</td><td>

Missing MIDLogFileHandler MID Server properties cause MID servers to go into an infinite loop of restarting during start up

</td><td>

MID Servers repeatedly come up and then go back down for a few seconds before the MID Server comes back up again. This loop repeats continuously if certain MID Server Properties are missing from the ecc\_agent\_property table on the instance.

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

UX Framework

 PRB2002003

 [KB2901692](https://hi.service-now.com/kb_view.do?sysparm_article=KB2901692)

</td><td>

Stuck semaphore due to the call GlideUxInteroperableRoutesProvider.getInteroperableRoutesByIds\(\)

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1999010

 [KB2817637](https://hi.service-now.com/kb_view.do?sysparm_article=KB2817637)

</td><td>

Time Out abandoned Virtual Agent \(VA\) conversation scheduled job closes the conversation in the middle

</td><td>

'Time out Abandoned VA conversation' should not close the conversation if idle time out is not completed.

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

Analytics Data API

 PRB1986630

</td><td>

Domain isn't included while generating a key for the indicator data source

</td><td>

Visualizations that use the Analytics Cache currently omit the global key when generating cache entries. As a result, a visualization may behave inconsistently across domains, depending on which domain created the cache entry first.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1960791

</td><td>

Incorrect cypher results for the union of two different nodes with the same return fields using GlideRecordDynamic

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Cloud Encryption

 PRB1980759

</td><td>

Prevent erroneous tampered DARE Properties notification emails from being sent to users

</td><td>

The error message, 'The tampering activities for Cloud Encryption properties have been found' is found in the logs.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1570891

</td><td>

Glide does not generate correct query for PostgreSQL or MonetDB if the table name starts with a number

</td><td>

PostgreSQL and MonetDB only allow table/column names to start with a letter or an underscore.

</td><td>

 

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

Voice Input for Authentication Parameters \(non-KBA\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2004770

</td><td>

worker\_manager should be able to create/update AI User records

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Encryption Support

 PRB1993181

</td><td>

Flow session cloning \(PFSessionClone\) needs to load all roles, including snc\_internal

</td><td>

GlideSecurityManager.get\(\).getRoles\(\) has side-effect of removing snc\_internal role when explicit roles plugin is enabled. Using GlideSecurityManager.get\(\).getRoles\(true\) will prevent this side-effect.

</td><td>

 

</td></tr><tr><td>

Security Attributes

 PRB1986784

</td><td>

SecurityAttributeConditionParser resizes hashmap for ConditionResolver.fCustomTermResolvers multiple times contributing to higher CPU

</td><td>

This is showing up in CPU captures form loadsims. It is at least 1% of CPU total usage and may be more.

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

OneExtend

 PRB2004072

</td><td>

Mosaic execution path needs to be handled via off-glide property

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1971863

</td><td>

Transaction canceled: 'Failed to get database connection due to exhaustion of connection pool on the node'

</td><td>

A spike in requests can produce a demand exceeding pool max capacity. Some connections are created, but the process is slow, causing various race conditions and delays and eventually causing a timeout in one operation.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1927385

 [KB2428127](https://hi.service-now.com/kb_view.do?sysparm_article=KB2428127)

</td><td>

New counting mechanism doesn't track probes using cache

</td><td>

Discovery hangs when enabling a probe cache via 'glide.discovery.use\_probe\_results\_cache'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Time Card Management

 PRB1988000

 [KB2760220](https://hi.service-now.com/kb_view.do?sysparm_article=KB2760220)

</td><td>

Managers are no longer able to add time cards for their direct reports in the Time Sheet Portal

</td><td>

Managers are no longer able to add time cards for their direct reports and Delegates in the Time Sheet Portal.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1883306

</td><td>

In Service Operation Workspace \(SOW\), when updating the due date from the list view, the date/time is removed

</td><td>

When the user changes the system property 'glide.sys.date\_format' from base to 'dd-MM-yyyy', the field is cleared out when they attempt to change the date. This issue was observed in Yokohama.

</td><td>

1.  Access a Yokohama base instance.
2.  Navigate to **SOW**.
3.  Navigate to **List menu** &gt; **Requests** &gt; **Open Items**.
4.  In the list view for the Requested Item, add the column 'Due Date'.
5.  Change the date/time and apply it.

Notice that the date/time should update as expected.

6.  Open the system property 'glide.sys.date\_format'.
7.  Change the value to 'dd-MM-yyyy'.
8.  Save the record.
9.  Return back to the RITM with the updated due date.
10. Change the date/time to a future date and apply it.

 The value for the date/time is removed from the list view and on the form level.

</td></tr><tr><td>

List Administration

 PRB1991341

 [KB2803013](https://hi.service-now.com/kb_view.do?sysparm_article=KB2803013)

</td><td>

Unable to update **User** field / other fields at Certification Task level

</td><td>

In the Certification Task record, under the inline level, the **User** field or other editable fields are not editable. When attempting to change the value by double‑clicking on the field, the field goes into a loading state and never allows selection of another.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1843154

</td><td>

Not able to save a dashboard after editing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Filters

 PRB1967959

</td><td>

Unable to filter the **tags** field in the presentation list from CSM/FSM Configurable workspace

</td><td>

When the user selects the tag that has been added, a modal does not populate and the user is unable to select **View records with this tag**. Instead, the 'tags' column cannot be filtered.

</td><td>

1.  Access the CSM/FSM Configurable Workspace.

Notice that the variable with sys\_id '0c69dae8cc842210f87799583e1668b2' is loaded to the workspace \(order = '-10'\).

2.  Access the list of any table.
3.  Use the condition builder to add the **tags** field as a condition.

Notice that the **tags** field is not listed for selection.

4.  Add the 'tags' column to the list view.
5.  Select the added tag.

 Expected behavior: A modal is populated and the user can select **View records with this tag** to find matching records.

 Actual behavior: Nothing happens, and it says the 'tags' column can't be filtered.

</td></tr><tr><td>

UI Form Administration

 PRB1920717

</td><td>

Hyperlinks in annotations on forms are not opening in a new window

</td><td>

Hyperlinks open in the same tab instead of opening in a new tab.

</td><td>

1.  Open a base instance.
2.  Open an incident table.
3.  Open any incident.
4.  Right-click and navigate to **Configure** &gt; **Form builder**.
5.  Create an annotation with the code.
6.  Open the incident in SOW.
7.  Under 'Details,' select the link.

 Expected behavior: It opens the link in a new tab.

 Actual behavior: It opens the link in the same tab.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1966768

</td><td>

If an input contains a lifecycle stage and a lifecycle stage status, an IRE CI update is aborted by the 'Validate lifecycle combination' business rule

</td><td>

The Business Rule 'Validate lifecycle combination' which calls the script include LifeCycleUtil aborts CI update with error 'Invalid Life Cycle Stage and Stage Status combination' although the values passed are valid combinations.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1936699

</td><td>

The activity stream flickers when the work notes are in modless view

</td><td>

 

</td><td>

 

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

Virtual Agent

 PRB1994599

</td><td>

Off Glide code introduced an issue for DTAC when the agent sends a message to the requester

</td><td>

The dynamic translation for messages doesn't work when the agent sends messages to the requester. It throws NPE.

</td><td>

 

</td></tr><tr><td>

REST API Framework

 PRB1936861

</td><td>

'Requested URI does not represent any resource' is logged as an error instead of a warning

</td><td>

'Requested URI does not represent any resource' is logged as an error instead of a warning in the system Logs. Errors in the system logs represent issues that must be fixed; however, the 'Requested URI does not represent any resource' message should be displayed as a warning in the system logs because it is an error that has been handled and the user/platform can recover from.

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

Access Control

 PRB1981898

</td><td>

Need properties for better control of the scope where a security attribute script gets evaluated

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Attachments to Records

 PRB1920687

</td><td>

The user can see the **New** and **Edit** buttons in attachment attribute table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1975852

</td><td>

MetricStatsCache causes the application node to run OutOfMemory

</td><td>

QueryMetricStatsListener has a cache limit of 10K entries \(from AbstractMetricStatsListener\), but as each entry contains a query which can be up to 2MB \(hardcode limit\), the user can easily spike the memory usage and run the node OOM.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1938058

 [KB2756546](https://hi.service-now.com/kb_view.do?sysparm_article=KB2756546)

</td><td>

Slow query from status count optimizer impacting Parallel launching of cloud app patterns

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Column Level Encryption

 PRB1990541

</td><td>

Attachment upload defaults to 'None' encryption module in the workspace

</td><td>

Attachment upload defaults to 'None' encryption module in the workspace, where as in Classic View its working as expected.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1969026

</td><td>

Deferred Related list can fail the UI page ACL if the script condition checks URL parameters

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1841579

</td><td>

sn-search-combobox-desktop's use of createGraphQLEffect dispatches errorActionType due to a 401 error for public GraphQL endpoints

</td><td>

The batch request fails due to 401 even though the GraphQL request in the batch was actually successful.

</td><td>

1.  Set the Service Portal home page to public.
2.  Set the Typeahead Search widget to public.
3.  Open Service Portal without logging in.
4.  Open Developer Tools.
5.  Select the Search Box.

 Observe in Seismic Dev Tools that the batch request failed due to 401. Then, observe in the Network tab that the GraphQL request in the batch was actually successful.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1996759

</td><td>

Null check for threadMember is incomplete for CollabMessageDto

</td><td>

The user can send a message but it's greyed out in the chat window until the user refreshes. The last sent message in a collab chat record doesn't update, so the discussion card in the utility menu never updates.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1940538

</td><td>

Clone job depends on the 'dp\_rta\_ner\_request' table running successfully

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1933785

</td><td>

A Cloud Discovery schedule incorrectly maps all related service accounts even when the 'Discover all Related accounts' toggle is unchecked

</td><td>

When creating a Cloud Discovery schedule for a project and unchecking the 'Discover all Related accounts listed below' toggle, the schedule still maps to all service accounts under that folder level. This behavior is intermittent and has been reproduced on multiple environments. The UI script logic doesn't correctly handle timing between setAllSubAccSelected and getSubAccountsOfMasterAccount. As a result, subAccountsList is reset incorrectly, leading to unintended account mappings.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1917452

</td><td>

Travel time and work time validation doesn't prevent the work order tasks from being updated, and the **Close incomplete** button has unexpected results

</td><td>

Modifying the Actual travel duration to be larger than the time between Actual travel start and Actual work start triggers a business rule to display 'Total travel time must be before actual work start' and abort the change. However the change is not aborted. Moreover, if the change is saved with the button **Close incomplete** the task status will be updated to 'Closed complete'.

</td><td>

 

</td></tr><tr><td>

Analytics Export API

 PRB1995410

 [KB2810683](https://hi.service-now.com/kb_view.do?sysparm_article=KB2810683)

</td><td>

On demand list visualization export to .xlsx

</td><td>

An issue has been identified where on‑demand exports of list data visualizations intended for XLSX format are instead exported as XLS files in the Zurich environment. This behavior differs from the Yokohama environment, which previously exported successfully in XLSX format.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1715251

</td><td>

There's a syntax error when adding a dot-walked column with the type 'fx\_currency' to a report

</td><td>

The user observes: Syntax - error or Access Rule Violation detected by database \(\(conne612968\) Unknown column 'task1 .amount' in held list'\).

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1966095

 [KB2659568](https://hi.service-now.com/kb_view.do?sysparm_article=KB2659568)

</td><td>

Auto MID selection causes excessive metrics to accumulate when connection issues occur

</td><td>

The MID server during auto-mid-selection can experience excessive memory allocation and CPU spikes due to agents connecting with network connectivity issues. As part of auto-mid-selection, agents make REST based calls to the MID server querying for the number of connected agents to perform load balancing and honor the maximum number of agents connections allowed. Part of this call will generate a metric instance for tracking which accumulates and can potentially block other thread calls to the MID web server hosting the REST calls. The result is the MID server experiences heavy CPU spikes and excessive memory retention while agents attempt to find the correct MID server to connect with. Coupled with network interruptions, this can result in the MID server running out of memory.

</td><td>

 

</td></tr><tr><td>

Attachments to Records

 PRB1977787

</td><td>

Adding the prefix 'ZZ\_YY' hides all references to an attachment in a record

</td><td>

In Yokohama, the behavior for the ZZ\_YY Prefix, hides an attachment along the header of a record, but keeps the attachment in the work notes visible. In Zurich, adding the prefix ZZ\_YY hides all references to an attachment in a record, including in the work notes. This is occurring on all tables and not just sc\_req\_item.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1993929

 [KB2908761](https://hi.service-now.com/kb_view.do?sysparm_article=KB2908761)

</td><td>

RCAs are created with the source as 'sys\_ws\_operation.do? sys\_id=6986d96dff7322102ae8ffffffffff48' for HR apps

</td><td>

An RCA is generated: 'RCA triggered - 'Read operation on table 'sn\_doc\_html\_template' from scope 'Global' was denied. The application 'Document Templates' must declare a Restricted Caller Access privilege. Please contact the application admin to update their access requests'. None should be generated.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1953139

</td><td>

'My Lists' sharing doesn't display all the users in a shared option

</td><td>

In sys\_ux\_my\_list, all 25 users in the shared users but are visible, but in SOW, it show only limited users.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1965515

</td><td>

Minimize the impact of connection pool expansion throttling on scheduler jobs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1936264

</td><td>

Transactions aren't removed from TransactionManager because an exception is thrown in the http thread before transaction queuing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1956992

</td><td>

Discovery logs display an error when ci\_sys\_id doesn't exist or the value of OS field/column is NULL: 'TypeError: Cannot convert null to an object'

</td><td>

Discovery reports an error: 'Sensor error when processing Linux - Installed Software: TypeError: Cannot convert null to an object.' The error occurs because the 'Linux - Installed Software' probe is running on a Unix cluster.

</td><td>

 

</td></tr><tr><td>

List Editor

 PRB2001509

</td><td>

Inline list editing popup edit box UI is mispositioned when trying to edit a reference field by double clicking on it

</td><td>

The pop-up edit box UI is mispositioned when trying to edit any inline editable field by double clicking on it on a List Report added to a Dashboard. The dialog box that appears is positioned away from the actual field being edited and has an incorrect format: The cross is not red and the square around the magnifying glass is incomplete.

</td><td>

 

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
3.  Set window size to 1280x1024.
4.  Zoom in to 200% and 400%.

 Expected behavior: Content is not cut off at 200% and 400% zoom

 Actual behavior: Content is cut off at 200% and 400% zoom

</td></tr><tr><td>

Virtual Agent

 PRB1916016

</td><td>

The End Conversation action does not end live agent interaction when Post Chat survey is enabled

</td><td>

The interaction and conversation should close once the user responds to the Survey.

</td><td>

1.  Start a conversation with Live Agent using VA API and make sure post chat Survey is enabled with 'Requester Ended' flag.
2.  Exchange messages between agent and user.
3.  Initiate END\_CONVERSATION action from user and Survey will be presented to user.

 Expected behavior: The interaction must be closed when user ended the conversation and then Survey must be presented to the user. This behavior can be verified from webclient as well.

 Actual behavior: The interaction is kept open and Survey is presented to the user.

</td></tr><tr><td>

Virtual Agent

 PRB1960339

</td><td>

The 'Use an AI agent ' action moves to a 'Waiting' state when called inside a flow-logic component

</td><td>

In a use case where calling the agent multiple times in a single subflow/flow using the flow-logic, the agent is initially called, but the second call goes into 'Waiting' state and no other calls go through. In the second call to the same agent \(with a different objective\), the execution record's state is 'Ready' and the message 'Conversation data is not populated' occurs for the second record. This leads the action to be in 'Waiting' state. The sysevent record is also not created.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1977676

</td><td>

Variables are not wrapping correctly on CSM workspace when question length is large in Single Line Text

</td><td>

Variables are not wrapping correctly on CSM workspace when question length is large in Single Line Text

</td><td>

1.  Open a record that supports variable creation.
2.  Open the item record in a new tab.
3.  Right-click on the item name on top and select **New Variable**.
4.  Create a variable record with a very long single line text in the question.
5.  Save the variable.
6.  Check that the variable should be visible on RITM record on backend.
7.  Open the RITM record in CSM/FSM workspace and check the variable.

 Notice that the text is not wrapped and cuts off.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1994000

</td><td>

State Persistence not working in Zurich

</td><td>

Although persisted parameters are correctly updated and visible in the URL, they are not restored into state parameters on page load.

</td><td>

1.  Open any list page \(/now/sow/list\).
2.  Apply a filter \(state persistence enabled\).
3.  Refresh the page.

 Expected behavior: Persisted filter/state values from the URL should be restored and applied on page load.

 Actual behavior: Notice that the URL contains the persisted parameters. State parameters are not initialized, and filters are lost after refresh.

</td></tr><tr><td>

Encryption Support

 PRB1992606

</td><td>

Duplicate Attachment EFCs are created for tables

</td><td>

During the upgrade, the autoCLEHealthScan job in the sys\_mass\_encryption\_job table detected unmigrated attachments. As a result, the 'CLE Unmigrated Attachments Health' indicator appears red, and the 'unmigrated\_attachment\_count' shows a value greater than 0.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1887581

</td><td>

Selecting a new chat desktop notification doesn't bring focus to the tab that changed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1997697

</td><td>

Performance Issues with sa\_analytics.rca\_use\_legacy\_query = false

</td><td>

When sa\_analytics.rca\_use\_legacy\_query is set to false, the application may experience performance issues, including high resource consumption and potential OutOfMemory \(OOM\) errors. This defect arises from the new query mechanism not handling certain data scenarios efficiently, leading to degraded performance compared to the legacy mechanism.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1923677

</td><td>

The wrong record count is rendered when Record Count Limit is enabled

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1992132

</td><td>

The Virtual Agent \(VA\) link menu items are not displayed correctly

</td><td>

In Enhanced chat, VA link menu doesn't show the labels the way it shows on the standard chat. Instead it shows the label as plain text and shows the link below. If the link is longer, it increases the width of the 'Contact support window'. It should only show the label and shouldn't show the link.

</td><td>

1.  Open the Menu items from the branding.
2.  Add a long link.

 Notice that the width of the window increases beyond the chat window, and the label is shown in plain text and the link shows.

</td></tr><tr><td>

Analytics Data API

 PRB1998034

</td><td>

Single score data visualization ignores the 'Apply time series to result' indicator configuration

</td><td>

Starting in the Zurich release, the Single Score Data Visualization with AVG \(or SUM\) aggregation does not respect the 'Apply time series to result' configuration on Formula Indicators. When this option is unchecked, the Single Score continues to display the time-series-based result instead of updating accordingly.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1997461

</td><td>

NowLLMStreamReader.parse\(\) splits on 'data:' inside JSON content, corrupting LLM stream output

</td><td>

NowLLMStreamReader.parse\(\) uses data.split'data:' to split SSE \(Server-Sent Events\) frames. This splits on all occurrences of the literal 'data:' — including those embedded inside JSON string values in LLM output. When the LLM produces certain content, the split fragments the JSON into unparseable pieces. Jackson silently fails \(catches Exception in extractResults\), content is lost, and the feature invocation stays stuck in 'processing' with null output.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1971767

 [KB2678137](https://hi.service-now.com/kb_view.do?sysparm_article=KB2678137)

</td><td>

Agent Client Collector policies aren't synced to agents after MID restart and agent reconnection

</td><td>

The MID server currently has an issue where the policies and their check instances are not associated for tracking if the config\_publish ECC queue message has been processed by the MID server before the offline agents reconnect. The information will be present in the policy tracking mechanism, but the flow that processes the message sent to an agent during keep alive processing will not contain the up-to-date policies and their check instances due to the missing associations.

</td><td>

 

</td></tr><tr><td>

Service Catalog API

 PRB1946265

</td><td>

The Service Builder module gives an 'Invalid Request' error after ATF test

</td><td>

When a basic ATF test is run and the service builder module is accessed, it gives an 'invalid request' error on the page.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1932373

</td><td>

'Block relationship autocreation' business rule logic was not fixed correctly

</td><td>

Business rule 'Block relationship autocreation' needs to be corrected by AWA engineering and there is no general javascripting issue in relation to GlideRecord.operation\(\) masking the table's operation field.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1949745

</td><td>

In a newer version of the Workflow Studio filter in Yokohama, the radio choice filter that used to display a string field isn't available

</td><td>

 

</td><td>

1.  Select the filter.
2.  Navigate to advanced view.
3.  Select a radio field.

 Observe that the whole field gets disabled.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1970352

</td><td>

Not enforcing the ACL in DataManagerService.getWidgetProps

</td><td>

ACLs in DataManagerService.getWidgetProps should not be enforced, as the processes are not exposed as part of the API response.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1823355

 [KB2301356](https://hi.service-now.com/kb_view.do?sysparm_article=KB2301356)

</td><td>

When there is no scope or global for a scoped admin scoped app, an invalidate query is sent

</td><td>

AI Search doesn't work as expected and returns no results when searched with any query. On search preview, the message 'An error occurred. Check the logs for more details and contact Support if this issues continues' pops up before the query can even be triggered.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1879472

</td><td>

Sub flow context can't be opened after an upgrade to Yokohama

</td><td>

There's a deserialize error when viewing a flow context that has a static value assigned to the subflow output. The error stack can be located in the logs.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1888313

</td><td>

Time-limited role access is assigned if a user has more than one request in the future

</td><td>

Access should work as expected for users with multiple time-limited user role records, with assigning and revoking working as expected.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1906507

</td><td>

Ability to make asynchronous http request from OpenAPI/Postman

</td><td>

OpenAPI/Postman step DOES NOT support asynchronous http request. As a result, calls going through AI studio/Agents can fail.

</td><td>

 

</td></tr><tr><td>

Form Templates

 PRB1907844

</td><td>

Reference qualifiers on templates aren't supported on Service Operations Workspace \(SOW\)

</td><td>

Reference qualifiers on templates aren't supported on SOW. When the user selects the search icon, a pop-up opens.

</td><td>

1.  Navigate to **Navigator** &gt; **Standard Change** &gt; **All Proposals**.
2.  Open any active standard change proposal.
3.  Navigate to **Change Request values**.
4.  Select the **Assigned to** or the **Service offering** field.
5.  Select the **Search** icon.

 Observe that a pop-up opens.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1924501

</td><td>

Policies have a page break alignment issue

</td><td>

Policies have a page break alignment issue

</td><td>

 

</td></tr><tr><td>

Analytics Hub

 PRB1930155

</td><td>

Comments created date inside a widget display the wrong created date

</td><td>

Comments created date inside a widget are displaying a wrong created date

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1932618

</td><td>

Duplicate updates of a field in an update record action after updating the same record in a custom action using a script

</td><td>

.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1936225

</td><td>

Grouping doesn't work on a group on a dot-walk field

</td><td>

 

</td><td>

1.  Create a UIB page.
2.  Add a record-list-bundle.
3.  Add a dot-walk field to the list and a few other normal fields.
4.  Save and preview.
5.  In the preview page, try to group on the dot-walk field.

 Observe that nothing happens.

</td></tr><tr><td>

UX Framework

 PRB1942276

 [KB2661969](https://hi.service-now.com/kb_view.do?sysparm_article=KB2661969)

</td><td>

When hovering over any workspace tabs \(parent or child/secondary\), the tooltip stays on screen and doesn't disappear

</td><td>

This is an intermittent issue, but when it occurs the user can't read part of the record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1960061

</td><td>

Keywords in data pattern causes false positive discovery

</td><td>

 

</td><td>

1.  Open the base instance data pattern 'Age'
2.  Select the **Test data pattern** UI action.
3.  Set Keyword to 'age' and Keyword proximity to 30.
4.  Test the input 'The agent 13 is called to summarize the incident'.

 Notice that the pattern is discovered.

</td></tr><tr><td>

Major Incident Management

 PRB1960650

</td><td>

There's a slow SQL query on multiple instances when executing the 'ContactManagementEngine.java\#L210'

</td><td>

.

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

Search Administration

 PRB1968215

</td><td>

Elements must only use supported ARIA attributes for the **Search catalog** field for Service Portal \(SP\)

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

 Expected behavior: The ARIA attribute is not allowed as seen in 'aria-selected='false'' and an element's role supports its ARIA attributes.

 Actual behavior: Elements only use supported ARIA attributes, as seen in the element location: sn-search-combobox,sn-search-combobox-desktop,.-search-popover\_\_item--is-active.

</td></tr><tr><td>

Walk-Up Experience

 PRB1968746

</td><td>

The 'Explicit role' plugin should be enabled, assigning the snc\_internal role to a walkup user which has a conditional script writer role

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1970805

</td><td>

After transferring the chat to another queue, the previous agent is still able to send chats on the transferred interaction

</td><td>

After transferring the chat to another queue the previous agent is still able to send chats on the transferred interaction when the Polaris is off \(U16\) after upgrade to Zurich

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1972737

</td><td>

Conditions for displaying page variants don't work for web embeddable components

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1973105

 [KB2757491](https://hi.service-now.com/kb_view.do?sysparm_article=KB2757491)

</td><td>

Planned costs in demand currency and confirmed/allocated costs in demand currency aren't updated on a resource plan

</td><td>

This issue occurs in the demand currency/project currency view. It only occurs when user isn't populated on the resource assignment.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1977219

</td><td>

The max wait time/no agent message isn't rendering hyperlinks in Portal, but it's working in Teams

</td><td>

When a URL is given in the **Max wait time message** field of the awa\_queue table, it returns a selectable hyperlink in Virtual Agent \(VA\) but working in Teams VA.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1978979

</td><td>

The session should not get timed out during the execution of topic as a tool when run as an AI User

</td><td>

The user session is getting timed out after uploading the attachment.

</td><td>

 

</td></tr><tr><td>

Service Creator

 PRB1979124

</td><td>

The 'Service Task Processing' flow triggers and sets an assignment differently than a deprecated workflow

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream Compose Component

 PRB1981047

</td><td>

The **Save as draft** button is not aligned with 'Send email'

</td><td>

The '**Save as draft**' and **Send email** buttons in the workspace email composer in Zurich are not aligned. All action buttons, including **Save as Draft**, should have the same dimensions \(height, width, padding, and font size\) to maintain a consistent and aligned user interface.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1981411

</td><td>

The capacity is not displaying accurately, it appears in the Estimate outside plan section in Capacity Planning

</td><td>

When the user creates a demand and creates assignments for it, and selects Create Project in the demand, it will create project from demand. However, the resource allocation's **planning\_item** field does not update.

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

HTTP Client

 PRB1986204

</td><td>

The **Test** UI action on the sys\_soap\_message\_function table causes large table handling query against ecc\_queue and causes memory contention

</td><td>

Selecting the **Test** UI action for a 'SOAP Message Function' \[sys\_soap\_message\_function\] record that has a 'MID server' specified causes the platform to send a test request to the MID server, and then poll for a response from the ECC queue. The query does not pass a valid value for the filter on the response\_to= filter, and so it can bring back hundreds to millions of rows, depending on how many rows are in the ECC queue.

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

Platform Analytics Dashboard API

 PRB1989067

</td><td>

Remove the info banner on Core UI dashboard overview page

</td><td>

The new 'com.glide.par.coreui.migration\_banner.enabled' system property was introduced to configure the appearance of the migration banner.

</td><td>

1.  Set the system property com.glide.par.unified\_analytics.enabled to false.
2.  Navigate to the CoreUI dashboard overview page: $pa\_dashboards\_overview.do.

 Observe that the following info banner is displayed: 'If you can't find the dashboard you're looking for, try the Platform Analytics library. Visit Platform Analytics experience.'

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1989461

</td><td>

Attempts to reconcile a RH in pending\_create or pending\_initialize states should repost those events

</td><td>

A hierarchy can get stuck in a PENDING\_CREATE or PENDING\_INITIALIZE state due to a lost, failed or missing event to allow them to progress to the next state. Attempts to reconcile the hierarchies are also ignored because the user can't reconcile un-initialized hierarchies.

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

MetricBase

 PRB1989962

</td><td>

Metricbase load spikes can cause bursts of server connection errors: 'No threads are available'

</td><td>

 

</td><td>

Generate a large amount of simultaneous requests to metricbase.

 Observe the errors that appear, such as 'Connection attempt in progress - no threads are available'.

</td></tr><tr><td>

Event Management

 PRB1990100

</td><td>

EM disable/enable jobs fix scripts unnecessarily manipulate the upgrade\_safe value during installation and upgrades

</td><td>

During upgrades within Zurich, some Event Management \(EM\) jobs can temporarily lose the upgrade\_safe flag. This happens because the EM 'before upgrade' fix script may execute unexpectedly. When upgrade\_safe is set to false on key EM scheduled jobs \(for example, 'Event Management - process events' and related connector/coordinator jobs\), those jobs may not run during the upgrade window. This can lead to delayed event processing or backlog while the upgrade is in progress.

</td><td>

 

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

Application Manager

 PRB1992835

 [KB2804238](https://hi.service-now.com/kb_view.do?sysparm_article=KB2804238)

</td><td>

A deprecated Classic App Manager URL causes issues on some instances

</td><td>

Users have access to the Classic App Manager by navigating to the URI '/$allappsmgmt.do'. When they switched to new app manager later, and load the 'My company applications' page, that can corrupt the App Manager checksum cache, which causes the manual sync to fail.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1993857

</td><td>

Agent chat inbox notifications appear in HTML

</td><td>

The incident card on the agent chat appears as HTML on a desktop notification.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1995281

 [KB2800274](https://hi.service-now.com/kb_view.do?sysparm_article=KB2800274)

</td><td>

Instant alter on a large table times out after 3 minutes and enters an infinite DDL retry loop, and is an upgrade blocker

</td><td>

On MariaDB instances, upgrades to Australia fail to finish. They get stuck in a retry loop when a single alter operation takes longer than 3 minutes.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1996008

</td><td>

Sometimes adjacent alerts aren't grouped even if there is a matching definition

</td><td>

The problem happens in Zurich when 1\) there are two tag-based definitions \(D1 and D2\) with the same or very similar filter and grouping conditions, and 2\) the definition D1 has a lower order and shorter timeframe window, while the definition D2 has a higher order and wider timeframe window. The problem is that two adjacent alerts fit to both definitions, but they're created with interval that's greater than the timeframe of the definition D1. Instead of being grouped by the definition D2, the alerts remain ungrouped. So the cause of this error is incorrect handling of isolated alerts.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1997156

</td><td>

List sections under My Lists tab of Workspace do not keep their expand / collapse state

</td><td>

With the 'List Bundle SNC' screen variant, the list sections under the 'My Lists' tab, such as 'Created by me', 'Shared with me' and 'Opened by link', do not keep their expand / collapse state after reloading the browser \(or a new browser session\) while the list sections under Default list keep their expand / collapse state.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1997159

</td><td>

Lists created under 'My Lists' of Workspace requires explicitly provide the permission

</td><td>

With 'List Bundle SNC' screen variant enabled in Workspace, lists created under 'My Lists' now requires explicitly provide the permission. In the previous list screen variant 'List SNC', such permission is not required.

</td><td>

 

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB1997896

</td><td>

HttpServletRequest is recycled during long transactions, which causes unhandled exceptions in HttpRequestAttributeAccessor

</td><td>

Long-running SOAP transactions, including ODBC queries, can fail to complete on Zurich instances due to an unhandled error during telemetry collection.

</td><td>

Scenario 1: Attempt to query large datasets using ODBC.

 Scenario 2: To reproduce using only SOAP, increase the max limit and query 30k+ records in a single request.

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

OneExtend

 PRB1998199

</td><td>

NAVA gets stuck intermittently

</td><td>

 

</td><td>

1.  Ensure Response Streaming is enabled.
2.  Open NAVA.
3.  Enter 'Creator.'

 Notice that NAVA will get stuck intermittently.

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

Performance Analytics

 PRB2000268

</td><td>

The wrong formula score is shown when filtered on multiple elements

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB2000325

</td><td>

Cell redirection action fails in Offline Mode after completing a task when multiple conditional buttons share the same cell location

</td><td>

The user observes the error 'Cannot find application content in offline data.'

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2000521

</td><td>

Support for Knowledge Blocks in ECE

</td><td>

Knowledge blocks are not supported in ECE. Ideally, blocks should be supported in ECE.

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

AI Experience Framework - Glide

 PRB2004228

</td><td>

The org chart does not work in track/swarm

</td><td>

 

</td><td>

1.  Type 'Who is Abel Tuter'.
2.  Select the **View** button on the People card to open the org chart.

 Notice that the Org chart does not load.

</td></tr><tr><td>

Incident Management

 PRB1989167

</td><td>

Make SDA role available for all of the users irrespective of ITSM Roles plugin installation

</td><td>

The SDA role is installed only if ITSM Roles plugin is active on the instance, hence there are upgrade users still missing on this role. ITSM has introduced a new AI worker as part of ZTSD uptake and that AI worker uses the SDA role, hence the user must have the SDA role.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1989343

</td><td>

After a Glide upgrade, dashboard HTML rich text widgets are missing spaces that originally separate the boldfaced text

</td><td>

 

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

Integration Hub

 PRB1989692

</td><td>

Page details are missing from the execution details for Datastream Actions when run via FlowAPI

</td><td>

The Page Details section is missing and the user is unable to view step-by-step execution data \(Pagination Setup, Integration Metadata, Step Configuration, API request/response\).

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2004301

</td><td>

AI agent prioritization is not functioning correctly when the 'Include AI Agents' option is enabled

</td><td>

 

</td><td>

1.  Install glide.awa and nowassist-ai-agents plugins on a Z or A instance.
2.  Enable 'Include AI Agents' for a assignment rule which has both AI agent and manual agents.
3.  Start a incident.

 Observe that incident is not assigned to an AI agent as preference even though it is available.

</td></tr><tr><td>

Virtual Agent

 PRB2004408

</td><td>

getNearestInternalEndpoint\(\) compares endpoint names instead of URLs for DC proximity, making selection order-dependent

</td><td>

In NextwaveEndpointService.getNearestInternalEndpoint\(\), the HostnameProximityEstimator compares endpoint names \(for example, 'nextwave-fqsn-0', 'nextwave-fqsn-1'\) instead of endpoint URLs. Since the endpoint names have no datacenter segment, the proximity estimator computes identical distances for all endpoints, and min\(\) simply returns whichever endpoint appears first in stream order — not the one in the same datacenter as the Glide node.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2004737

</td><td>

Zboot errors observed for Australia changes

</td><td>

As part of Australia branching/hardening flow, zboot errors are reported.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1990179

</td><td>

Language Detection from French to English doesn't show the topic name in English

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1990260

</td><td>

The CreateSegment Scriptable API throws error when invoked from different scope that is not global

</td><td>

The error 'No implementations found for extension point: interactionSegment' is thrown.

</td><td>

1.  Log in to the instance.
2.  Install Customer Service Management demo data.

Notice two records in sys\_extension\_instance with the point ''global.InteractionSegment'' \(openframe\).

3.  Create an interaction and respective phone log record.
4.  Link the phone log record to the interaction by creating interaction related record.
5.  Run this createSegment Wrap Up Scriptable API from 'Scripts - Background' from any other scope \(sn\_openframe\)

 Expected behavior: A wrap up segment with a segment record is created, and works if run from global scope.

 Actual behavior: An error is thrown, 'No implementations found for extension point: interactionSegment.'

</td></tr><tr><td>

Virtual Agent

 PRB2004856

</td><td>

Premium chat upgrade should only apply to Zurich not Australia

</td><td>

When a user is upgrading to NAVA April \(17.0.x\) version, if they are on Australia then they should not get premium chat experience for NAP. If they are on a Zurich version, they should get the premium chat experience for NAP.

</td><td>

 

</td></tr><tr><td>

SQL API \(Server\)

 PRB1966907

</td><td>

DBSQL Parser changes are not working properly for ODBC/JDBC applications

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

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

Asset Management

 PRB1990771

</td><td>

Asset Analyst UI changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB1991257

</td><td>

The user can't select a software model if multiple are found for PPN

</td><td>

Selecting **Import** just reloads the page without automatically selecting a software model, and a software model can't be selected from the field without clearing PPN.

</td><td>

1.  Create a PPN and two software models with details matching that PPN's DMAP.
2.  Import an entitlement with that PPN.

Observe that an entitlement import error is generated with the reason 'Multiple software models found for the Publisher Part number. Please choose a software model.'


 Expected behavior: There is handling for this situation, either preventing duplicate software models from being created, picking one of the duplicates during import or after selecting the **Import** button, or allowing users to select a software model without needing to clear the **PPN** field.

 Actual behavior: Selecting **Import** just reloads the page without automatically selecting a software model, and a software model can't be selected from the field without clearing PPN.

</td></tr><tr><td>

Upgrade Center

 PRB1991306

</td><td>

On upgrade from Xanadu or Yokohama to Zurich, a 'Before' fix script runs even though it's not supposed to

</td><td>

The syslog contains relevant log messages.

</td><td>

 

</td></tr><tr><td>

ServiceNow IDE \(Family Release\)

 PRB1991336

</td><td>

Loader doesn't skip updates if the update matches the instance value

</td><td>

XML ends up in an updateset even though it's unchanged.

</td><td>

1.  Export an XML from an instance.
2.  Load the XML again using the FluentXMLLoader.

 Expected behavior: The XML shouldn't end up in updateset since it's unchanged.

 Actual behavior: The XML ends up in updateset even though it's unchanged.

</td></tr><tr><td>

SQL API \(Server\)

 PRB1966904

</td><td>

The user does not see the proper error messages for missing server-side configurations in ODBC client driver

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1991370

</td><td>

Presentational list should allow for suppressing Rows Hidden alerts via system property

</td><td>

The 'X rows removed from this list by security constraints' continues to appear to ITIL users even though the system property is set to 'true.'

</td><td>

1.  Set up an ACL that will block ITIL users from seeing some incidents.
2.  Impersonate an ITIL user.
3.  Open Service Operations Workspace \(SOW\).
4.  Open 'Incidents - All list'.

Notice that the 'X rows removed from this list by security constraints' message appears, which is expected.

5.  Stop impersonating the ITIL user and return to being an admin user.
6.  Create a system property, 'true/false' type with a value of 'true' named 'glide.ui.list.hide\_rows\_hidden\_presentational'.
7.  Impersonate the ITIL user again.
8.  Open 'Incidents - All list' again.

Notice that the message continues to appear.


 Expected behavior: With the property set to 'true', the message does not appear on the Presentational List.

 Actual behavior: With the property set to 'true', the security constraints message appears on the Presentational List.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2004901

</td><td>

Users can create widgets and AIX tables should be locked to users with elevated privileges

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1991881

</td><td>

Defect form related lists not rendering correctly when accessed from Approval list

</td><td>

The defect form renders but the Pull Requests tab is missing from the related lists section.

</td><td>

 

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

 Actual behavior: The 'Thank you' text stays in the chat even after sending and receiving response. It is also observed that other prompts like 'What is spam' appear in the chat until a response gets generated.

</td></tr><tr><td>

Database Persistence

 PRB1992095

</td><td>

There's an error in the cypher2ResultsPaginated API

</td><td>

There's an error executing cypher: 'FAILED TRYING TO EXECUTE ON CONNECTION Syntax Error or Access Rule Violation detected by database \(\(conn=103967\) Unknown column 'sys\_user0.sys\_id' in 'order clause'\)'.

</td><td>

 

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB1965678

</td><td>

The Taxonomy Selector should escape values from API before passing into the now-content-tree component

</td><td>

The HTML entity '&amp;' is incorrectly displayed.

</td><td>

1.  Create a topic name which include &amp; in its name \(for example, Mobiles&amp;Tablets under employee taxonomy\).
2.  Navigate to **All** &gt; **Catalog builder** &gt; **Create new catalog item** &gt; **Continue** &gt; **IT issues** &gt; **Use this template**.
3.  Navigate to **Location section** &gt; **Topics** &gt; **Edit selected topics**.

 Observe that in the list, instead of '&amp;' it displays the HTML entity '&amp;amp'.

</td></tr><tr><td>

Window Manager

 PRB1992484

</td><td>

In window-manager 29.2.12 , resizableBehavior is throwing errors

</td><td>

 

</td><td>

1.  Provision a Zurich instance.
2.  Install AI Data Explorer.
3.  Select the **Sparkle** icon on the Next Experience dashboard.

 Expected behavior: The pop-up appears.

 Actual behavior: Nothing happens.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1992485

</td><td>

Remove sys\_ids from Playbook-fetched telemetry metrics

</td><td>

Process definition information isn't included as part of data that is captured.

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB1992589

</td><td>

Create workflowStageProcessor script includes for getting stages

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1964847

</td><td>

In domain separated instances, the user is unable to update Agent Chat setting for user domains

</td><td>

When agents using windows machines lock their systems \(in low power mode\), there are cases where the presenceworker heartbeat graphql call is sent from client even after the awa/work\_item/agent\_sys\_id amb subscription is broken. In this case, the agent is never put to offline because of the heartbeat updates but the incoming work item card does not get rendered in Agent's workspace as AMB is disconnected.

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

AI Experience Framework - Glide

 PRB2004904

</td><td>

sys\_ux\_widget cache config does not provide translated templates

</td><td>

UX widget configs does not provide translated templates, results in missing translations for all widgets.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB1993170

</td><td>

Pass the auto-incrementor using the unique ID of the table rather than using the contract number

</td><td>

There should be automation for both scenarios: 1. Uploading the docs, finishing the flow, and importing another doc to the same contract. 2. The asset covered from both docs should be part of the same contract.

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB1993246

</td><td>

Traces not captured for agents when tracing is enabled via env variables

</td><td>

 

</td><td>

1.  Deploy and agent in vertex AI with tracing enabled.
2.  Run the agent and generate traces.

 Expected behavior: The ps should have llm\_request and llm\_response for calls to LLMs or tool calls.

 Actual behavior: Both llm\_request and llm\_response are empty.

</td></tr><tr><td>

ServiceNow IDE \(Family Release\)

 PRB1993260

</td><td>

BYOUI source artifacts are serialized as separate records

</td><td>

In order to prevent BYOUI source code from becoming orphaned or lost, they must be tracked together with their corresponding metadata in the same XML payload so that they cannot be inadvertently lost while migrating update sets.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB1993285

</td><td>

Simple queries are timing out on Enterprise Graph and Enterprise Graph Mini

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1993335

</td><td>

Chat history shows 'No conversations yet' randomly when navigating back to 'Conversation history' page

</td><td>

Users are unable to access their conversation history after navigating away from the page. Users may believe their conversations are lost, leading to confusion and potential re-creation of conversations.

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

Natural Language Query \(Family Release\)

 PRB1993465

</td><td>

MetadataInvalidationListener creates a NLQ-related tables hashset for every DB action, causing an increase in young object generation and also adding to performance cost

</td><td>

In the hot code path, the isNLQRelatedTables is called and it creates a list first and converts into a hashset for every DB action.

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

MID Server

 PRB1963685

 [KB2633251](https://hi.service-now.com/kb_view.do?sysparm_article=KB2633251)

</td><td>

MID Server File Sync doesn't sync attachments when the sys\_attachment table name is prefixed with ZZ\_YY to prevent clones deleting the attachments

</td><td>

Attachments of MID Server Synched File records, such as MID Server Script File \[ecc\_agent\_script\_file\] records, aren't synched to the MID Server when the sys\_attachment table name is prefixed with ZZ\_YY to prevent clones deleting the attachments. The MID Server platform should be expecting not only the actual table name, but also table name prefixed with ZZ\_YY when querying the instance for the attachment.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Session Management

 PRB1962465

</td><td>

Performance degradation with build 1108

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB1994093

</td><td>

'Mark all as read' isn't working due to GlideRecordSecure and updateMultiple methods being used

</td><td>

 

</td><td>

1.  Trigger notifications to any non-admin user.
2.  Log in.
3.  Navigate to a portal.
4.  Open a notification tray.
5.  Select **Mark all as read**.

 Notice that it's not marking as read in the background.

</td></tr><tr><td>

UI Form Administration

 PRB1994242

</td><td>

When 'glide.ui.escape\_text' is set to false, forms break

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow IDE \(Family Release\)

 PRB1946936

</td><td>

Restrict delete from Outside Scope while Installing a Fluent App

</td><td>

This is a product update.

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

Field Service Work Configurations \(Family\)

 PRB1939816

</td><td>

Assignment groups for new work configurations are empty

</td><td>

 

</td><td>

1.  Created new service configuration by cloning existing base instance field service configuration.
2.  Disabled Qualification and dispatch groups configurations.
3.  Created work order template and have set the Work configuration to the new configuration.
4.  Created new work plan and it has generated work order and work order tasks.
5.  Select an assignment group.

 Notice that it comes up empty.

</td></tr><tr><td>

OneExtend

 PRB2004938

</td><td>

Metadata changes to support Data Separation

</td><td>

Mosaic currently doesn't send the domain hierarchy to mosaic as a part of the metadata sync.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1995357

</td><td>

New RCAs from Knowledge Center to HR Core to use Open Prompt

</td><td>

Issues are observed when using the Open Prompt in HR Agent Workspace. Users try the Advanced Knowledge editor page in HR Agent Workspace. This page contains Open Prompt, which is interactable and helps create an article using Gen AI. For the Open Prompt to work without any issues, new RCAs are required.

</td><td>

1.  Provision an instance with the Knowledge Recommendation plugin and Article Optimization plugins installed.
2.  From the Knowledge Management properties, turn on the ECE.
3.  Create an article from the related list of any HR case.

 There's an RCA from KC to HR core.

</td></tr><tr><td>

Declarative Actions

 PRB1995366

</td><td>

AI gradient support in Declarative Actions \(DA\) and UI actions in Workspace and Core UI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1937999

</td><td>

Discovery schedule should support discovery of IPAM IPs and subnets

</td><td>

Currently Discovery Schedule only supports discovery IP address lists, IP Ranges and subnets configured in associated discovery\_range and discovery\_range\_item\_ip tables. This limits the ability to support integration of IPs from other sources such as IPAM.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1995579

</td><td>

True up versions for NAKM, KC, KCUIB and ECE

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB1995609

</td><td>

The Trino REST API throws an exception for tables with long names \(&gt; 30 characters\), because 'nonce' is generated as the table name

</td><td>

When accessing a Workflow Data Fabric \(WDF\) table that references a Glide table with a name &gt; 30 characters, the Trino REST api throws an NPE: '2026-02-19 14:52:28 \(041\) TRINO\_REST-thread-37 8ECE056F474F32105679CCA4F16D437A txid=06cec96f474f TimingLogger \*\*\* ERROR \*\*\* Problem occurred while fetching DB response: Cannot invoke 'java.util.Set.iterator\(\)' because 'sqls' is null java.lang.NullPointerException: Cannot invoke 'java.util.Set.iterator\(\)' because 'sqls' is null'.

</td><td>

1.  Create a Glide table with &gt;30 characters.
2.  Create a WDF table with a column that references a column in the Glide table.
3.  Open the WDF table and include the reference column in the list view.

 An error displays on the page.

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

Flows \(Family Channel\)

 PRB1995799

</td><td>

AI Search semantic search results aren't appearing for a non-admin user with only the flow\_designer role

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2005501

</td><td>

Make nextwave client autosuggest debounce configurable

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1996246

</td><td>

Workflow transfer context isn't working on Zurich

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1996311

</td><td>

Add the 'fetchDocuments' attribute to be passed in contextData of the session API call request data parameters when switchContextConversation is 'true' and parsed from AIEL

</td><td>

 

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

 Observe the results in the sys\_mm\_result table , and the error message in the 'Error message' column

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1996321

</td><td>

An AI Search dynamic filter makes two calls \(one extra call\) when filters are applied, and in the second call, additionalContext is null and doesn't return correct counts on preprocessing

</td><td>

When filters are set to the empty array, the additional call doesn't happen and it works as expected. The issue happens when filters are set.

</td><td>

1.  Implement AISDynamicFilter preprocessing.
2.  Make an AI Search call by setting filters and passing additional context.

 Observe that an additional call is happening per search source. For the second call, the additionalContext value is null even though the additionalContext is passed as parameter to AI Search API call. If filters aren't applied, then the additional call doesn't happen. It happens when filters are applied and additionalContext is null when it should not be.

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

Scripted REST APIs

 PRB1996583

</td><td>

There's high latency of the REST API scriptable

</td><td>

The existing scriptable methods jsFunction\_getDetailedServices and jsFunction\_getDetailedServicesWithOAuthPolicy had the withSchemaContent flag hardcoded to true, forcing retrieval of schema information for every API resource, which the MCP team doesn't need in the first step. This fix exposes withSchemaContent as an explicit parameter, letting the caller decide based on their use case.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1996750

</td><td>

Sending the incident number for the chat label in the 'History' panel in Now Assist panel \(NAP\) for ITSM not working

</td><td>

This issue occurs for Zurich.

</td><td>

1.  Start the contextual conversation in agent workspace.
2.  Search any text.

 Observe the chat label in the History panel in NAP does not appear.

</td></tr><tr><td>

System Import Sets

 PRB1935089

</td><td>

Stream blocks jdbc probes from running

</td><td>

A JDBC data source will not start writing to the import set until the JDBC data stream finishes or writes the last attachment to sys\_flow\_context.

</td><td>

1.  Create a long running JDBC data stream and run it.
2.  Try to run a JDBC data source on the same MID.

 Notice that the JDBC data source will not start writing to the import set until the JDBC data stream finishes or writes the last attachment to sys\_flow\_context.

</td></tr><tr><td>

Process Mining Workspace

 PRB1933943

</td><td>

Issues with multiple OR conditions

</td><td>

In Yokohama, the user observes an error message reading: 'An error occurred: Exception encountered processing path: /GlidePromin\_Query/scheduleModel - Relation between advanced transitions cannot be empty or NONE'. In Zurich and Australia, no error message is thrown and ST is also not created.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1997012

</td><td>

Do not allow 'backup/fallback' URLs to be used for Glide messages sent to OGCS

</td><td>

The callback\_url and pod\_ip must be present in the tool execution request, or the Live Agent context, or the session context \(for session-related messages back to OGCS\).

</td><td>

 

</td></tr><tr><td>

Now Assist Nextwave Experience

 PRB2005749

</td><td>

Issues handling live agent conversation closure

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2005902

</td><td>

Instance is missing sys\_service record for aiux-kit service discovery

</td><td>

 

</td><td>

1.  As an admin, navigate to /sys\_service\_list.do or Navigate to /xmlstats.do?include=services\_status.
2.  Look for a service record named: aiux-kit.

 Expected behavior: Instance should have an aiux-kit sys\_service record to be discovered by ADC.

 Actual behavior: Notice a missing sys\_service record.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1997363

</td><td>

**Sys\_** fields are silently dropped when importing a table from a local instance

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

Database Persistence - Data Access

 PRB1932176

</td><td>

OutOfMemoryError when attempting to update the graph with as a parent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1997499

</td><td>

The sn-canvas-tabs component displays a record preview popover on hover that is inaccessible to screen reader users

</td><td>

In configurable workspaces, there's a top level tab navigation region made up of the sn-canvas-tabs component. Hovering over a record tab in this region with a mouse triggers a popover to display a short preview of key fields on the record, like short description, state, and more. This is crucial information for agents to quickly differentiate between multiple tabs at a glance, but keyboard and screen reader users can't trigger or access the popovers.

</td><td>

1.  Navigate to a configurable workspace, such as Service Operations Workspace.
2.  Open at least two records.
3.  In the top level navigation tabs, hover over a deselected record tab.
4.  Note that a popover appears with a short summary of key fields for the record, such as short description, priority, and state \(varies by table\).
5.  Attempt to navigate record tabs with the screen reader enabled.

 Expected behavior: When a tab for a record has focus, the preview popover also appears and remains visible. Screen reader users should hear the details in the preview popover announced.

 Actual behavior:When the user navigates through the tabs, screen reader users report confusion because a record number isn't enough detail for many to remember which tab is which, and they aren't aware they are missing the preview popover details.

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

Event Management

 PRB1923711

</td><td>

Once the maximum size limit for impacted maintenance CIs is reached, the system is unable to re-evaluate them

</td><td>

When ImpactMaintenanceHandler.executeMaintenanceCalculation is triggered and the limit is reached, the maintenance job stops, and the system does not automatically re-evaluate the maintenance impact.

</td><td>

 

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

Embedded Help

 PRB2006009

</td><td>

Unable to start Dynamic Guidance

</td><td>

Dynamic guidance wouldn't start and gives the following error alert: 'Dynamic Guidance is unavailable at this time. Ask your admin to check if the skill is active before trying again.'

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1923112

</td><td>

An alert with a message is shown intermittently while generating highlights

</td><td>

The alert message reads, 'Finding Highlights - Click on the investigate drop-down list to view the results'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1998050

</td><td>

Glide-side changes for label population in picker tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2006124

</td><td>

The topic doesn't resume from where it left

</td><td>

 

</td><td>

 

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

Virtual Agent

 PRB2006256

</td><td>

After upgrading from Zurich, NAP is not working

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1998404

</td><td>

Gen AI usage is not being recorded for one-extend calls with multiple execution requests

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1998441

</td><td>

Abort duplicate Default Thinking Quota condition default = true is not getting triggered

</td><td>

Notice that the user is able to create multiple records.

</td><td>

1.  Log in to the instance.
2.  Navigate to the table sys\_gen\_ai\_model\_thinking\_quota\_config table.
3.  Insert the record with same details generative AI module and generative AI thinking quota configuration with a default value.

 Notice that the user is able to create multiple records.

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

Next Experience Unified Navigation

 PRB1998576

</td><td>

Catalog Builder home page is not loading

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

UI Form Administration

 PRB1918407

</td><td>

Document Viewer overlay hides Now Assist panel \(NAP\) in Workspace

</td><td>

The document view should open in the app shell. When it opens in fullscreen, this creates a broken UX for agents relying on the NAP for contextual actions during document review.

</td><td>

1.  Open any record in the Agent Workspace.
2.  Open NAP from the top right menu by selecting the **Sparkle** icon.
3.  Navigate to the attachment panel.
4.  Open an attachment.
5.  Observe that the document viewer opens fullscreen and hides the NAP.

 Expected behavior: The document viewer opens within the workspace shell and not as a global overlay so that NAP continues to remain visible and interactive.

 Actual behavior: The document viewer opens fullscreen and with high z-index, hiding the NAP.

</td></tr><tr><td>

ServiceNow IDE \(Family Release\)

 PRB1998945

</td><td>

Migrate an empty hosted plugin

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1918185

</td><td>

Custom defined reference fields no longer return data

</td><td>

 

</td><td>

1.  Navigate to a UIB page and/or demobook with predicate builder.
2.  Use the provided data in the engineering details to set the panelDefinition and metadataCache props.
3.  Set the source for predicate builder controller to be \`task'.
4.  On the condition row select the field **Custom Reference Field**.
5.  Operator should be 'Is'.
6.  Select the value editor.

 Observe that there are no values in the editor.

</td></tr><tr><td>

Database Persistence - Graph

 PRB1999021

</td><td>

Always use a table rather than its parent when injecting keys

</td><td>

When doing injections, it uses the primary key value, which is present in all the tables that make up a TPC class, but it may or may not include parents based on the select items/where clause. It's best to use the sys\_id in the child class.

</td><td>

 

</td></tr><tr><td>

SQL API \(Server\)

 PRB1999140

</td><td>

Update the rate limit on SQL calls to 500/hour

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1999442

</td><td>

The live agent avatar changes when an image is sent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2006393

</td><td>

Plan to release the disambiguation feature

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1999491

</td><td>

NAP Platform assistant doesn't have base instance AI native fallback button labels

</td><td>

 

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

Virtual Agent

 PRB1999793

</td><td>

Remove admin role

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1999920

</td><td>

BuilderEntityCache uses 100+ MB in Australia on Now Support, and it is mostly duplicate data due to domain keys

</td><td>

The cache is using a key based on the domain, so if 100 users load the same thing it will end up with 100 of the same entries in the cache. But it does not consider that all of the domains are actually using the same object.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2000110

</td><td>

Add post processor logic to get cardData info for FA based genAISkill execution

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB2000222

</td><td>

Integration Filter used to measure API Access Volumes is not applied to SOAP and JSONv2 requests

</td><td>

Certain internal inbound SOAP &amp; JSONv2 integration API requests count towards a user's data egress \(API Access Volume\) usage. These APIs are used for ServiceNow products. The user licenses separately or are for supporting internal capabilities and should not be considered data egress.

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

Virtual Agent

 PRB2006405

</td><td>

CustomControl response should contain the **Model** field in the payload

</td><td>

 

</td><td>

1.  Run a custom control response node in Virtual Agent.
2.  Navigate to sys\_cs\_conversation, and search for the custom control payload under Conversation Messages tab.

 Observe that the payload for the custom control response node does not contain the 'model' property.

</td></tr><tr><td>

Knowledge Management

 PRB2006452

</td><td>

Launch AI Native SKUs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2006813

</td><td>

Queries are queued on user clones due to OAuth issues

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Zero Copy Connector for ERP \(Family Channel\)

 PRB2000572

</td><td>

com.glide.erp.core plugin has a namespace 'sn\_erp\_integration' which creates the conflict for the scope name for the zccforerp app, which is blocking public script includes

</td><td>

com.glide.erp.core plugin has a namespace 'sn\_erp\_integration' which is creating the conflict for the scope name for zccforerp app which is blocking public script includes

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

AI Agents \(Glide Family\)

 PRB2001449

</td><td>

i18n cache configuration missing cache invalidation metadata

</td><td>

 

</td><td>

 

</td></tr><tr><td>

SQL API \(Server\)

 PRB1916118

</td><td>

Data volume is coming in negative when it is egressed beyond a certain limit

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB2001558

</td><td>

Script fix to migrate voice input flag from NAA to Agent Studio running even for new users

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2001595

</td><td>

Add support for web automation and desktop automation tools

</td><td>

 

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

AI Search

 PRB1796676

</td><td>

Users can't create custom AI Search matchers on an indexed column with an aliased column name

</td><td>

It's not allowed by the business rule 'Verify index for exact match field'.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2002014

</td><td>

Data to glide from offglide is not logged with the actual user

</td><td>

When the user makes a set cache call to glide from offglide, they observe that any record updated or created does not have an actual user in the created\_by or updated\_by field.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2002088

</td><td>

The **Locals** field is missing the **Enable AI agent** field

</td><td>

The **Locals** field on activity context is missing the **enable\_ai\_agent** field.

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

Virtual Agent Designer Legacy

 PRB2002310

</td><td>

Skills applicability changes as per the AI Native guidelines

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Build Agent \(Glide\)

 PRB2002327

</td><td>

Keyword search returns full field content instead of relevant passages, causing excessive token consumption

</td><td>

The keyword search handler returns content fields in their entirety or applies a naive substring from the start of the field. It has no awareness of where query terms actually appear in the text. For large fields \(**script**, **xml**, **template**\) the relevant matching content is often beyond what is returned and is discarded.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2002402

</td><td>

Trace collector epic for Zurich

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB2002403

</td><td>

Extend the 'NotificationsEmailAgentsUtils' global script include with methods for notification, template, and layout creation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2002404

</td><td>

Enhance MFA support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2002612

</td><td>

Filters should expose new filter custom ID field

</td><td>

 

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

Flows \(Family Channel\)

 PRB2002799

</td><td>

AISearch stops working when upgrading to latest Australia release

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

Virtual Agent

 PRB2002957

</td><td>

Channel user profile gets NASS instead of bot to bot

</td><td>

 

</td><td>

 

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

 PRB2003170

</td><td>

Nextwave mode gets stuck after bulk upload and never advances to the guided credential setup flow

</td><td>

In Nextwave mode, when the user asks AI Agent to perform a bulk upload — it gets stuck. There is no output from NextWave while the tool is loading. The conversation does not advance beyond the initial response.

</td><td>

 

</td></tr><tr><td>

SQL API \(Server\)

 PRB2003236

</td><td>

Usage tracking for servers for the SQL API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

SQL API \(Server\)

 PRB2003237

</td><td>

Enable a Workforce Data Fabric token for SQL API data egress

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

SQL API \(Server\)

 PRB2003238

</td><td>

Create a unified SQL API plugin for both ODBC and JDBC server plugins

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

SQL API \(Server\)

 PRB2003239

</td><td>

Enable Discovery for servers for the ODBC API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2003281

</td><td>

Install log sync service only if com.glide.cs.genai is installed

</td><td>

 

</td><td>

 

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

AI Agents \(Glide Family\)

 PRB2003366

</td><td>

Data to glide from offglide is not logged with the actual user

</td><td>

Add Impersonate role to NextWave Service User to impersonate the actual call for glide backed set operations.

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

Process Mining Workspace

 PRB1974124

</td><td>

An analyst user is not able to edit Configurable values of automated findings

</td><td>

The user notices an alert message even though fields are shown with default values.

</td><td>

1.  Create a new project from the Process Projects page.
2.  On the 'Set improvement opportunities' page, create a new automated finding.
3.  On the Configure screen, update the default values and select **Save** and exit.
4.  Select the same finding and navigate to the Configure page.

Observe that updated values are not saved and the user still sees the default values.

5.  Remove the exiting values \(Keep the field empty and select **Save** and exit\).
6.  Select the same finding and navigate to Configure page.

 Notice the error alert 'The above mandatory field is invalid or not filled in' is still displayed even though fields are shown with default values.

</td></tr><tr><td>

Service Catalog

 PRB1975065

</td><td>

Actions and 'Sparkle' icon aren't generated for UI policy and its sub-tabs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1975224

</td><td>

Inconsistent information shown in Transitions Filter panel after triggering compute of Transition Filter condition

</td><td>

When the user selects 'Transitions' and the editor opens, it will return blank.

</td><td>

1.  Create a Transition Filter with any criteria and then select **Apply**.
2.  Select the **Transitions** link to open the 'Transitions' filters.

This time, the user will see the information used when the filter in step 1 was created.

3.  Close the Transitions filter.
4.  Select the **Transitions** link to open the 'Transitions' filters.

 Notice that the filter is empty \(and not populated as it was in step 2\). Future times the user selects 'Transitions' and the editor opens, it will return blank.

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

Now Code Editor

 PRB1976964

</td><td>

Create a new MobileCallableScriptIncluded

</td><td>

The scripts in question used to work in Yokohama and stopped working from Z, when window.NOW.SyntaxEditor.sanitizeVarName was added.

</td><td>

1.  Navigate to sys\_script\_include table.
2.  Create a new script include record.
3.  Give a name to the script include.
4.  Check the 'Mobile callable' checkbox.

 Expected behavior: A relevant template should be generated in the script field.

 Actual behavior: The following error is shown 'onChange script error: TypeError: Cannot read properties of null \(reading 'NOW'\) function'.

</td></tr><tr><td>

Virtual Agent

 PRB2003371

</td><td>

Translation updates

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1977488

</td><td>

New column 'interview\_summary' to be added in ER interview table and RCAs for summary

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1968463

</td><td>

Ready for Review PWS bottom tray issues

</td><td>

 

</td><td>

 

</td></tr><tr><td>

JVM at Scale

 PRB1967652

</td><td>

Expose microsecond level print of latency to DB into stats/xmlstats for easy bigdata ingestion

</td><td>

This is a product update.

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

Next Experience Unified Navigation

 PRB1979347

</td><td>

Interactive view is not launching for the map component even though the event is fired from LBF client

</td><td>

 

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

Asynchronous Message Bus \(AMB\)

 PRB1980367

</td><td>

Collect Essential Logs on AMB Client and Ship to Server

</td><td>

Messaging events on AMB client are not visible to AMB server causing message delayed/missing events not discoverable. Major impact have been observed for AWA related AMB messages.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1980521

</td><td>

Dashboard Filters are not applied for Scriptable Multivis

</td><td>

 

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

Identity

 PRB1981341

</td><td>

Include trackable attribute in Machine Identity Console and Scripting Governance Tool's plugin.xml

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2003672

</td><td>

Unable to send attachment without typing any text

</td><td>

 

</td><td>

1.  Open NAP.
2.  Select the **+** button next to the input bar.
3.  Upload a document.

 Observe that a voice button is shown.

</td></tr><tr><td>

SQL API \(Server\)

 PRB1967359

</td><td>

Include a licensing validation for SQL API queries

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1981991

</td><td>

The **Edit Columns** button isn't working in SPM Resource Management workspace

</td><td>

The **Edit Columns** button isn't working in SPM Resource Management workspace for resource allocation tab for a resource record.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1982635

</td><td>

Support for report\_group and report\_global roles to edit visualizations

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2003812

</td><td>

Sonar Test Coverage should be 80% for Data Collector Module

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1984620

</td><td>

Loading of sys\_pd\_process\_definition\_c5142dddff37e21082a8ffffffffff2d taking two hours

</td><td>

This issue occurs when upgrading Yokohama and Zurich.

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

AI Experience Framework - Glide

 PRB1986457

</td><td>

The icon color on notifications uses a hardcoded hash value

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow IDE \(Family Release\)

 PRB1967082

</td><td>

Should allow updating multiple XML files and setting the target update set Id

</td><td>

The current upload processor fails to upload multiple XML files and upload to the desired target update set ID.

</td><td>

 

</td></tr><tr><td>

Experimentation Platform

 PRB1988332

</td><td>

The 'Experiment' preview is missing for admins

</td><td>

The preview feature is required in the activation workflow. Experiments are opt-in by default, but admins need to review and understand the impact before deciding whether to opt-out. Without preview, admins can't assess what the experiment does, leading to defensive opt-outs and poor adoption.

</td><td>

Navigate to the 'Experiment' page from a bell notification.

 Notice that there's no option to preview the variants in the experiment.

</td></tr><tr><td>

Horizon Component Library

 PRB2004216

</td><td>

Update now-avatar properties to receive styling for AI avatars for AI Specialists

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 7](zurich-patch-7.md)
-   [Zurich Patch 6](zurich-patch-6.md)
-   [Zurich Patch 5](zurich-patch-5.md)
-   [Zurich Patch 4 Hotfix 4b](zurich-patch-4-hf-4b-PO.md)
-   [Zurich Patch 4](zurich-patch-4.md)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


---
title: Xanadu security and notable fixes
description: The Xanadu release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 67
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu security and notable fixes

The Xanadu release contains important problem fixes.

-   **Xanadu was released on August 1, 2024.**
    -   Build date: 07-27-2024\_1019
    -   Build tag: glide-xanadu-07-02-2024\_\_patch0-07-16-2024

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X00.00.xlsx).

## Security-related fixes

Xanadu includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu, refer to [KB1650904](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1650904).

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

 PRB1641097

 [KB1432102](https://hi.service-now.com/kb_view.do?sysparm_article=KB1432102)

</td><td>

The user can't delete an ACL of sys\_attachment with a table name condition while deleting a type=attachment type field

</td><td>

The error message 'file.delete.failed' is generated when attempting to upload an attachment and there are no customized delete ACLs on the sys\_attachment.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Access Control

 PRB1703976

</td><td>

Users are unable to add a user to a group after elevating them to a role when the system property 'glide.ui.schedule\_slushbucket \_save\_for\_group\_roles' is set to true

</td><td>

When the system property 'glide.ui.schedule\_slushbucket \_save\_for\_group\_roles' is set to true, a user can't add users to groups if it's required that the user elevate to a role. The background job that's created doesn't add the user to the group.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1736031

 [KB1630133](https://hi.service-now.com/kb_view.do?sysparm_article=KB1630133)

</td><td>

Problems with caching 'system' security attributes

</td><td>

In some cases, especially after the user's session is idle for some time, the user might lose access to some resources, protected by the ACLs with UserIsAuthenticated security attribute.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1675128

 [KB1641686](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641686)

</td><td>

In the workspace activity stream, the email **From** field displays the sys\_id

</td><td>

The sys\_id appears in the workspace in the **From** field when an email is attached to an interaction and is displayed in the activity stream.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1736995

 [KB1642093](https://hi.service-now.com/kb_view.do?sysparm_article=KB1642093)

</td><td>

The activity stream renders differently on a workspace and UI16 with tags

</td><td>

When the activity stream is built with a workspace, it takes the latest user for the mod count. UI16 uses the oldest update and uses its user for the mod count. The issue is that when tags are added, they're added to the same user update \(sys\_mod\_count\). The update displays as the original user in UI1 and a different user in a workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1761952

</td><td>

The cursor jumps to the bottom of the text with Service Operations Workspace \(SOW\) activity stream in the 'Comments' section

</td><td>

Within SOW, when working on an incident and entering text in the 'Comments' section, the cursor intermittently moves to the bottom of the text.

</td><td>

1.  From SOW, open an incident.
2.  Apply a template with text in the 'Comments' section.
3.  Begin typing anywhere above the bottom of the text.

 Observe that randomly the cursor jumps to the bottom. The issue can be reproduced intermittently.

</td></tr><tr><td>

Activity Stream

 PRB1780340

 [KB1649222](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649222)

</td><td>

Post-Washington DC upgrade, GlideRecord for \[sys\_email\] updates all fields

</td><td>

The transaction should display that only the relevant information on the sys\_email record was updated, but extraneous fields are also updated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Agent Assist

 PRB1680218

 [KB1433227](https://hi.service-now.com/kb_view.do?sysparm_article=KB1433227)

</td><td>

The **Copy to clipboard** action isn't created for a table configuration with the searcher 'Response' templates

</td><td>

The issue with the action not copying occurs because all existing records for 'Copy to clipboard' populate the **current\_table** field. This field controls which table action is generated. If it is left empty, it would be created for any table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Agent Chat

 PRB1687713

</td><td>

The scroll bar of the agent chat doesn't work properly when the user scrolls up

</td><td>

The scroll bar is slightly pushed downwards.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1734352

</td><td>

Work item cards aren't rendering in an inbox although there's an attempt to render sn-inbox-card

</td><td>

There's an intermittent issue where agents don't see the work item card rendered in the agent's inbox although the work item is assigned to them and they do hear audio notifications.

</td><td>

1.  Log in as an agent.
2.  Navigate to a workspace.
3.  Start a chat as a requester.
4.  Enable client side logging by setting sys prop 'com.glide.awa.client \_logging.enabled' with roles 'awa\_agent' and 'awa\_manager'.

This is to enable the enhanced logging.


 Expected behavior: An agent should receive a work item card in their inbox with notifications.

 Actual behavior: Agents don't receive anything.

</td></tr><tr><td>

AI Search for Service Portal

 PRB1753189

</td><td>

Sort options in the AI search results page aren't displaying after an upgrade

</td><td>

Sort options aren't displaying after an upgrade. After selecting the 'Most relevant' menu, nothing is happening and users can't choose the other sorting options.

</td><td>

1.  Log in to the 'NL UAT Now Create' portal.
2.  Selct the **Search** button under 'Search for an asset'.
3.  Under the 'Asset/Success Pack' navigation tab, find the 'Most relevant' sort option.

</td></tr><tr><td>

AI Search

 PRB1706402

</td><td>

AI Search doesn't index translated text for 'Reference' type columns

</td><td>

Currently, the AI Search index reference column value only has one of the languages, even though translations in multiple languages are available.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1709322

</td><td>

Text seen when using AI Search can't be translated

</td><td>

The text '\[number\] results for \[keyword\]' can't be translated.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1734605

</td><td>

AI Search suggestions don't respect configurations for external URLs

</td><td>

If a user wants to use a custom URL to an external source for a result, they can configure this for search results via either a scripted post processor that overwrites the **navigation\_url** field, or create a custom declarative action. However, users are observing that neither of these methods are respected by suggestion readers.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1758577

 [KB1644179](https://hi.service-now.com/kb_view.do?sysparm_article=KB1644179)

</td><td>

JavaScript errors display on the portal after upgrading Washington DC

</td><td>

After upgrading Washington DC, JavaScript errors display on the portal and in the browser console that didn't take place in previous versions. These errors don't have any functional side effects.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1770551

 [KB1647708](https://hi.service-now.com/kb_view.do?sysparm_article=KB1647708)

</td><td>

Searching on a portal displays an empty Genius Results card at the top when no results are found

</td><td>

An empty Genius Results card is displayed at the top if no results were found. Genius results for an unsuccessful keyword search renders 'No results generated' after taking 9-10 seconds.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1779636

</td><td>

Carousel and regular search results don't appear intermittently

</td><td>

The carousel gets stuck in a loading state when a search query is performed.

</td><td>

1.  Provision an instance.
2.  Make sure Now Assist Actions and Now Assist QnA are attached to a Service Portal search profile.
3.  Perform a search for any Catalog or QnA query.

 Notice that the carousel is stuck in a loading state.

</td></tr><tr><td>

Application Install Engine

 PRB1733557

</td><td>

There's missing store\_packages when adding new nodes

</td><td>

Adding new nodes should activate required packages.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1736711

 [KB1634502](https://hi.service-now.com/kb_view.do?sysparm_article=KB1634502)

</td><td>

The 'Uninstall Application' related link isn't displayed on sys\_store\_app records

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Install Engine

 PRB1746800

 [KB1649407](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649407)

</td><td>

The host app isn't able to load the macros under 'ui.jtemplates', which breaks the openframe functionality in a non-Next Experience UI

</td><td>

The hosted plugin fails to load static content in the cache post-activation.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1714286

 [KB1646367](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646367)

</td><td>

The last sync with Store shows an invalid date in 'dd-MM-yyyy' date format

</td><td>

The last sync with Store's date and time is displayed incorrectly when the glide.sys.date\_format has been adjusted to use a different default format.

</td><td>

1.  In the filter navigator, navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.
2.  Select the **Sync apps** \(double arrow circle\) button next to the 'Last sync with store' date and time and wait for the sync to finish.

Notice that the date is displayed correctly.

3.  Set the glide.sys.date\_format to dd/MM/yyyy.
4.  In the filter navigator, navigate to **System Applications** &gt; **All Available Applications** &gt; **All**.

This should open the Application Manager.


 Observe that the 'Last sync with store' date is incorrect \(day is month and month is day\), or invalid.

</td></tr><tr><td>

Application Manager

 PRB1714732

</td><td>

Selecting the App Engine Studio application in the new Application Manager interface results in an error and the application record doesn't open

</td><td>

An error message appears: 'Product details fetch failed from instance'. The application record doesn't load.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1718754

 [KB1587314](https://hi.service-now.com/kb_view.do?sysparm_article=KB1587314)

</td><td>

In Vancouver, a plugin upgrade is stuck in the new Application Manager, even when the classic Application Manager displays the upgrade as complete

</td><td>

The classic Application Manager displays that the plugin was installed successfully, however the sys\_execution\_tracker entry still displays as running. The execution tracker wasn't updated to a complete state and progress was left to 94% due to an error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1728645

</td><td>

Dependent applications' UI is hidden on the ServiceNow Store and hinders the application installation process on production instances

</td><td>

This issue happens during application installation on production instances only. If an application requires dependency apps to be installed during the installation process and those apps \(dependency apps\) aren't mapped to an instance on the ServiceNow Store, the app installation dialog box asks users to purchase the app from the store before proceeding further. If users click the provided link, it takes them to the ServiceNow Store and they see the following message: 'No apps were found matching the selected criteria.'

</td><td>

1.  Try to install Employee Center on a production instance.
2.  Search for an app in 'System applications'.
3.  Select **Install**.
4.  Before the installation proceeds, a dialog box appears displaying a list of dependencies for the Employee Center. Employee Center Core is one of its dependencies. If this isn't installed on an instance, verify that the dialog box displays the message: 'Needs to be purchased from Store'.
5.  Select the 'Employee Center Core' link provided in the dialog box.

 It opens the Store page and displays the message: 'No apps were found matching the selected criteria'.

</td></tr><tr><td>

Application Manager

 PRB1741568

 [KB1644191](https://hi.service-now.com/kb_view.do?sysparm_article=KB1644191)

</td><td>

The user observes an internal server error on the 'App Manager' UI

</td><td>

The user observes the error: 'App info not found. Click ok to go back to home page' along with an Internal Server Error \(500\).

</td><td>

1.  Log in to an instance.
2.  Navigate to a new **Application Manager**.
3.  Sync apps to get the latest version.
4.  After sync, search 'appstore' in the search box and check the 'Updates' tab.
5.  Select **App Store**.

 Notice a blank page with an Internal Server Error \(500\) and text reading, 'App info not found. Click ok to go back to home page'. The user needs to go back and try again a few times before the page is updated, which is time consuming.

</td></tr><tr><td>

Application Scoping

 PRB1388380

 [KB0823213](https://hi.service-now.com/kb_view.do?sysparm_article=KB0823213)

</td><td>

Non-admin users don't see the 'wrong scope' message for records not in the currently selected application scope

</td><td>

Irrespective of the users and the roles, records should be read-only with the wrong scope message when the scope of the record is different from the currently selected application scope.

</td><td>

1.  Create a metadata table.
2.  Create records in different scopes, A and B, in this metadata table using an admin user.

When an admin opens a record which is in a different scope than the currently selected scope, notice that the record is displayed as read-only and the message 'This record is in the ABC application, but XYZ is the current application. To edit this record click here.' is displayed.

3.  Create a role.
4.  Add this role to the write ACL of the metadata table.
5.  Create a user with this new role.
6.  Open the records created in different scopes.

 The records are always displayed as editable and the wrong scope message isn't displayed, irrespective of the current scope of the user.

</td></tr><tr><td>

Appsee - Platform Infrastructure

 PRB1716290

</td><td>

An empty value in the **Analytics consent policy** field of the core\_country table record causes an error

</td><td>

An empty value in the **Analytics consent policy** field of the core\_country table record causes a 401 unauthorized error and breaks the navigation bar.

</td><td>

1.  Create a country in the core\_country table \(or have existing country\) with an empty **Analytics consent policy** field.
2.  Ensure that in the **Consent policy provider** field, only 'GeoIP' is enabled and the rest are turned off.
3.  Log in from a location for which the consent policy is set as empty.

Upon log in, ux-metrics flow triggers and executes the 'Get consent' API.


 Expected behavior: 'Get consent' should return the expected consent policy to ux metrics.

 Actual behavior: A null pointer error is thrown and it's not handled to return the correct response to ux metrics.

</td></tr><tr><td>

App Template Framework

 PRB1718490

</td><td>

An error was observed when creating an app out of a template

</td><td>

 

</td><td>

1.  Log in as an admin user.
2.  Navigate to App Engine Studio.
3.  Create an app, a workspace, and a portal experience.
4.  Navigate to 'Template'.
5.  Create a template using an existing app.
6.  Select an app that was previously created.
7.  Once the template has been created, create an app from the existing template.

 When the user adds an empty record \(with all the fields empty\) into sys\_translated\_text without changing the scope, and then tries to templatize it, the sys\_translated\_text record is added as one of the nodes for a few of the scan payloads.

</td></tr><tr><td>

Archive Rules

 PRB1669506

</td><td>

The 'Archive Destroy' rule isn't working and always displays 0 records

</td><td>

The 'Archive Destroy' rule isn't working and always displays 0 records, and doesn't delete records from the 'AR' table.

</td><td>

 

</td></tr><tr><td>

Audit History

 PRB1767585

</td><td>

User names in the history set and activity stream are incorrect when another user updates a target record

</td><td>

The journal history set doesn't attribute the correct user after the first record.

</td><td>

1.  Set glide.history\_set.pull\_journal\_entries\_from\_journal\_table to true.
2.  Add work notes to an incident using a script.
3.  Delete the history set for these journal entries.
4.  View the work notes in the platform view of the incident.

 Expected behavior: The first journal entry is from 'System Administrator', the next two are from 'Abraham Lincoln'

 Actual behavior: All journal entries are from 'System Administrator'.

</td></tr><tr><td>

Authentication

 PRB1667269

 [KB1329268](https://hi.service-now.com/kb_view.do?sysparm_article=KB1329268)

</td><td>

Users encounter the error 'Unable to extract Key from KeyStore' when creating JSON Web Token \(JWT\) keys

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1725399

</td><td>

The 'getHeader\(\)' call in the BasicAuth and BearerAuth scripts isn't working as expected

</td><td>

This is due to the API Key and Hmac plugins being enabled.

</td><td>

1.  Open an instance with the Washington DC release.
2.  In the basicAuth script, add a line var header = this.request.getHeader\('Authorization'\).

 Expected behavior: BasicAuth using correct credentials should work.

 Actual behavior: BasicAuth using correct credentials fails.

</td></tr><tr><td>

CMDB CI Class Manager

 PRB1756070

 [KB1644165](https://hi.service-now.com/kb_view.do?sysparm_article=KB1644165)

</td><td>

CI Class Manger views have multiple issues

</td><td>

The issues are: 1. The indicator bar in threshold setup is missing. 2. Multiple scroll bars, which isn't expected. 3. Redundant threshold setup information. 4. Redundant tables in the same page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

CMDB Data Manager

 PRB1752346

 [KB1641376](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641376)

</td><td>

CMDB Data Manager's 'Dependent CIs management' feature is enabled on an instance without warning

</td><td>

In Utah, the CMDB Data Manager is enabled by default when the instance has one or more active CSDM lifecycle rules. This has had an unintended consequence of also enabling the 'Dependent CIs management' feature of CMDB data manager.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Condition Builder

 PRB1697408

 [KB1629848](https://hi.service-now.com/kb_view.do?sysparm_article=KB1629848)

</td><td>

Loading issue of variables that are added to a column in Data Visualization list

</td><td>

On Platform Analytics Workspace and Service Operations Workspace, there's a recurring timeout issue encountered when processing a substantial amount of data for the item\_option\_new function. Despite increasing the timeout limit to 60 seconds, not all records can be loaded within the specified time frame.

</td><td>

1.  Open any of the Platform Analytics Workspace or Service Operations Workspace.
2.  Select the **Tap 2** in the page.
3.  Select the **All Active Tasks** component.
4.  Select the three dots.
5.  Configure.
6.  Select the **+Add** link in the 'Default Display' section.
7.  Try to add the questions at the bottom of the list.

 It doesn't load.

</td></tr><tr><td>

Condition Builder

 PRB1721656

 [KB1642058](https://hi.service-now.com/kb_view.do?sysparm_article=KB1642058)

</td><td>

When upgrading from Tokyo to Vancouver, the **Add custom conditions** button in the UI Builder 'Data visualization' component 'Add data source page' isn't working properly

</td><td>

A set condition doesn't display and the **Add custom conditions** button disappears.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Condition Builder

 PRB1735699

</td><td>

There's multiple issues with the reference list condition builder

</td><td>

The following issues occur: When running a query, the default conditions are appended to the query \(for example, running with 2 default conditions results in 4 conditions shown\). 'Sort By' conditions don't persist \(The user can add a sort to a column, but when they open the filter again, it's not there\). The 'Name' column is always sorted as 'Ascending' and can't be changed.

</td><td>

1.  Navigate to Service Operations Workspace.
2.  Open an incident record.
3.  Open the 'Details' tab.
4.  Select the magnifying glass for a service reference input.

 Observe the following issues when running a query: The default conditions are appended to the query, the 'Sort By' conditions don't persist, and the 'Name' column is sorted in 'Ascending' order.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1332966

</td><td>

The 'Reset Unknown Discovery Source State' business rule \(BR\) calls current.setWorkflow\(false\) and thus cancels all the BRs that should have run after it

</td><td>

The 'Convert to application service' action inserts/updates the cmdb\_ci\_service\_discovered table. But because the service had a discovery source set to 'Unknown', the 'Reset Unknown Discovery Source State' ran and the model update BR that should have been executed didn't. Thus, the service model wasn't created.

</td><td>

1.  Add a BR with an order higher than the order of 'Reset Unknown Discovery Source State' \(1010\) to the cmdb\_ci table.
2.  Update the table.
3.  Check if the new BR has ran.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1687690

</td><td>

An instance upgrade is stuck on plugin com.snc.cmdb. csdm.activation

</td><td>

In Upgrade Monitor, the upgrade progress shows that the upgrade isn't progressing.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1702705

</td><td>

During performance testing, similar symptoms to PRB1369519 were noticed

</td><td>

During performance testing, similar symptoms to PRB1369519 were noticed, 'Contention and continuous updates on the cmdb\_qb\_result\_base table'.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1728603

</td><td>

Performance issues with CMDBUtil. getRelatedServices when the user has many relationships at each level

</td><td>

'Refresh Impacted Services' is called from the ITSM change\_request UI form when the user specifies the configuration item and manually presses the button to invoke this API. For a user with a lot of CMDB data, this API consumes excessive memory, making the JVM node restart.

</td><td>

1.  Create a relationship map where a target CI has many relationships at each level \(shallow depth but wide\).
2.  When refreshing services on the CI, notice if in the node logs that the query is flagged for being large with a lot of sys\_id in the IN clause.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1729639

</td><td>

Multiple committers with the same sys\_id cause an Identification and Reconciliation Engine \(IRE\) exception when reconciliation is enabled

</td><td>

Datasource's 'last update' seems to expect a unique sys\_id in the batch of committers.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1736102

</td><td>

Multi-source updates to the code path generates several redundant update statements

</td><td>

Multisource update code path generates several redundant update statements with where clause on sys\_mod\_count for the same CI

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1742296

</td><td>

Optimizing the queries in CSDMReportProcessor causes a replication lag on csdm\_dashboard\_type\_result inserts

</td><td>

Some warnings display in the logs: 'SEVERE \*\*\* ERROR \*\*\* Exception during batch statement commit to glide...'

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1751001

</td><td>

Optimize the updates for the csdm\_dashboard\_reports\_result table

</td><td>

There's a lag.

</td><td>

 

</td></tr><tr><td>

Core Platform

 PRB1732676

 [KB1587782](https://hi.service-now.com/kb_view.do?sysparm_article=KB1587782)

</td><td>

The variable $\{comments\_and\_work\_notes\} isn't working for HR cases after an upgrade to Vancouver

</td><td>

After upgrading to Vancouver, email notifications with $\{comments\_and\_work\_notes\} are displaying as empty in the recipient's email. This works fine in Tokyo instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Core Platform

 PRB1735834

</td><td>

Users receive an error '\*\*\* ERROR \*\*\* loadRow failure java.lang.IllegalArgumentException: Unable to parse unicode value: XXX...'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Indexes

 PRB1721733

</td><td>

The cluster summary table is missing an index on the cluster ID

</td><td>

The query impacting users has an average execution time of the query is more than 1 second. The query is coming from 'Applications suggestion - ITOM Autodiscovery'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1692793

</td><td>

A datacenter instance displays an error, 'Operation not permit on a closed resultSet'

</td><td>

The error appears on Utah and later instances. This can cause problems with workflows completing.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1709781

 [KB1571178](https://hi.service-now.com/kb_view.do?sysparm_article=KB1571178)

</td><td>

Tables that meet the free space requirement but don't have more than 5,000 rows cannot be rebuilt

</td><td>

This can lead to large empty tables that require manual action to rebuild.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1719831

</td><td>

Database footprint or sys\_physical\_table\_stats doesn't display the correct table size

</td><td>

The row details for table\_name aren't equal to storage\_alias in the sys\_storage\_table\_alias table.

</td><td>

1.  Create a test table with over 40 characters.
2.  Verify that it's aliased in sys\_storage\_table\_alias.
3.  Add some records to the test table.
4.  Run the sys\_trigger for Physical Table Stats Gatherer.

 Observe that the value isn't updated in the sys\_physical\_table\_stats table.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1731252

</td><td>

ArchiveDocumentID.move DBQuery causes memory hogging

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1732094

</td><td>

The 'Physical Table Stats Gatherer' job impacts the database load

</td><td>

A job called 'Physical Table Stats Gatherer' that hosts a large amount of instances can impact the database load on the hosted database.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1765904

 [KB1647554](https://hi.service-now.com/kb_view.do?sysparm_article=KB1647554)

</td><td>

Transactions/Jobs are canceled at midnight following a Washington DC upgrade

</td><td>

DropTmpTablesJob went from cleaning 5 tmp\_ tables per day to 100, with a batch size of 5. With a long enough execution time, and since the DB is locked for some portion of the execution time, everything stops, must retry, and eventually gives up. This causes things to be canceled.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence

 PRB1731418

 [KB1645608](https://hi.service-now.com/kb_view.do?sysparm_article=KB1645608)

</td><td>

Using a related list query along with setAggregateWindow writes an invalid SQL statement

</td><td>

The node logs contain an error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence

 PRB1740957

 [KB1634707](https://hi.service-now.com/kb_view.do?sysparm_article=KB1634707)

</td><td>

Orphaned database triggers on a table prevent insert/update/delete operations until the database triggers are removed

</td><td>

The monthly job 'Dropping tmp tables' checks for leftover tmp\_\* tables and removes them from the database. If there are any triggers on the table or updates to the source table \(for example, 'task'\), it won't not work until the triggers are removed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence

 PRB1749923

</td><td>

The table join query fails to execute due to an incorrect alias name in SQL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1761025

</td><td>

A connection sharing violation can occur when StatementBatcher is used

</td><td>

Usually this issue occurs when process\_flow jobs are running.

</td><td>

 

</td></tr><tr><td>

Data Policies

 PRB1670181

</td><td>

opened\_at date/time is 4 hours in the future for an incident when created from an interaction record on a workspace

</td><td>

The created incident has a few hours difference between **Opened** and **Created** fields.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1509705

 [KB0967278](https://hi.service-now.com/kb_view.do?sysparm_article=KB0967278)

</td><td>

The Simple Network Management Protocol \(SNMP\) object identifier \(OID\) 1.3.6.1.4.1.1602.4.7 is discovered as 'Network Multi-PDL Printer Board-D1/H1' and is used by many different families and models of Canon multi-function printers

</td><td>

The SNMP Classification OID record 1.3.6.1.4.1.1602.4.7 is used by whole families of Canon multi-function printers. This OID record causes them all to be Model 'Network Multi-PDL Printer Board-D1/H1' regardless of the true family/model.

</td><td>

Discover a Canon printer with the OID 1.3.6.1.4.1.1602.4.7.

 The printer CI is created with the model 'Network Multi-PDL Printer Board-D1/H1', which is incorrect 99% of the time.

</td></tr><tr><td>

Discovery

 PRB1592609

</td><td>

Running large queries causes Cloud Discovery to cancel

</td><td>

Patterns take too long, causing Discovery to hang. The Cloud Discovery schedule hangs due to the transaction processing the results for the pattern running for too long and being canceled by the platform.

</td><td>

1.  Have a discovery with ~500 K storage volumes in a single logical datacenter \(LDC\).
2.  Delete 1 volume from the cloud.
3.  Rediscover.

 When trying to delete storage volume, it queries all volumes first.

</td></tr><tr><td>

Discovery

 PRB1640443

</td><td>

The job 'Object Source Table Integrity Check' is running long and causes high memory usage and a duplication of 'CMDB Sys Object Source Cleanup'

</td><td>

The job 'Object Source Table Integrity Check' queries sys\_object\_source with last\_scan older than 6 months. Each record returned checks if the referenced CMDB record exists. If it does, it continues to the next record. If the CMDB record doesn't exist, then it deletes sys\_object\_source. last\_scan is updated when the CMDB record is updated by the Identification and Reconciliation Engine \(IRE\). If there's no process to update the CMDB, then last\_scan is also not updated. The job could take hours to complete and consumes high memory.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1651345

</td><td>

Improve performance of L3 mapping

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1715075

 [KB1573366](https://hi.service-now.com/kb_view.do?sysparm_article=KB1573366)

</td><td>

A discovery schedule is stuck with incorrect started/completed jobs, causing the schedule to wait for a day and then canceling due to max time

</td><td>

When a transaction is canceled because of the maximum time exceeded for the sensor quota rule, the completed job count doesn't increment for that input record. This keeps the discovery active forever and is canceled when it hits the maximum run time.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1721054

</td><td>

There's a 'IP Address in payload is null' warning on Cloud Host \(cmdb\_ci\_cloud\_host\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1725044

</td><td>

URL Certificate Discovery doesn't work for some URLs

</td><td>

A message displays: 'Failed to retrieve certificate chain for URL...'.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1732616

</td><td>

There's high CPU utilization due to discovery commands running on AIX servers in the background

</td><td>

Even after the discovery finishes, the command is running on the target host and consumes most of the CPU space.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1776300

</td><td>

System event processing is held up by numerous running.process.absent events from Discovery and Agent Client Collector Visibility \(ACC-V\)

</td><td>

In Tokyo, a new type of event was added to clean up orphaned application CIs and relationships after the table cleaner had deleted the cmdb\_running\_process records. The event is triggered by the 'RunningProcessReconciler' script include, as part of Discovery sensors, and Agent Client Collector Visibility checks. It is then processed by the tcmdb\_ci\_appl CIs as a 'Absent' status, which potentially involves looping through a lot of records. Where there is a big ACC-V implementation, this is triggered for each agent install every 8 hours by default, which leads to many of these events. These events use the general event queue and the 'Events Process 0' job, which leads to backlogged event processing where all other events have to wait for these events to clear before running.

</td><td>

1.  Install ACC-V and create numerous agents.
2.  Observe the number of running.process.absent events created per day.

 In a busy instance, observe that these will account for a large proportion of any backlog, if events processing is backlogged. Impactful events such as this would normally have their own queue and events process job to avoid impacting the default queue and 'Events Process 0' job.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1743818

 [KB1646495](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646495)

</td><td>

DocIntel tasks fail

</td><td>

The docintel jobs failed at 50% with an error: 'NSE0014:Failed to initialize pipeline : No columns to parse from file' and 'nse0014:Failed to initialize pipeline : NSE0003:Failed to get pipeline json to have dataset path information'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Email Notifications

 PRB1681360

</td><td>

A scheduled report isn't including attachments on all emails

</td><td>

Email attachments aren't sent in emails that are split due to multiple recipients. The problem only occurs when the attached file size is larger than 220 KB.

</td><td>

1.  Create a scheduled email of reports that generates an .xlsx attachment over 180 KB.
2.  Add 2 recipients to the list.
3.  Set the glide.email.smtp.max\_recipients property's value to 1.
4.  Trigger the report on demand.

 The attachment is only present in one of the split emails.

</td></tr><tr><td>

Email Notifications

 PRB1763775

</td><td>

When composing an email in Service Operations Workspace \(SOW\) and copy/pasting the 'Caller' name to the **To** or **CC** field, the auto-complete for the reference field isn't appearing

</td><td>

For example, when the user copies and pastes the name 'Abraham Lincoln', it displays the error 'Local address contains control or whitespace. Characters in format \[a-z\]\[A-Z\]\[0-9\] \{-\} are accepted.'

</td><td>

1.  Navigate to Service Operations Workspace.
2.  Open any incident or RITM record.
3.  Copy the name from the **Caller** field of 'Details' tab.
4.  In the 'Compose' section, select **Email**.
5.  Paste the name in the **To** or **CC** fields of the email.
6.  Select the **\(i\)** section beside the name and observe the error.

</td></tr><tr><td>

Embedded Help

 PRB1749112

 [KB1638817](https://hi.service-now.com/kb_view.do?sysparm_article=KB1638817)

</td><td>

The Documents API is being failed as the ai\_generated column is absent in the help content table

</td><td>

The issue is observed after upgrading to Washington DC and is reproducible only when the ai\_generated column is not added to the help content table upon an upgrade to Washington DC.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1723329

</td><td>

High memory usage in Event Management Impact Tree Builder is affecting the node and causing memory manager to kill threads

</td><td>

When memory manager detects that the node is low on memory, it terminates the longest running processes.

</td><td>

 

</td></tr><tr><td>

Fiscal Calendar

 PRB1636278

</td><td>

Records outside of 'Calendar Span' don't return correctly when the fiscal period starts on a month other than 'Jan 01'

</td><td>

When creating a report that's a time series trend by fiscal calendar, the records that are outside of the fiscal period range \(before or after the generated fiscal periods\), for example on the 'Empty' bar, don't display correctly when drilled into.

</td><td>

1.  Generate fiscal periods for an instance with the start month as April \(04\) and generate a few years of fiscal periods.
2.  Validate periods to ensure the calendar is valid.
3.  Navigate to the reports menu and create a report.
    1.  Table = Incident
    2.  Type = Time series \(Column/Line\)
    3.  Configure the report to following
    4.  Calendar = Fiscal calendar
    5.  Per = year
    6.  Group by = Priority
    7.  Trend by = Created
4.  Run the report. When the report chart renders, you will see the bar for 'empty' fiscal periods for any incidents created outside of generated fiscal periods.
5.  Note the number showing on the bar.
6.  Drill into the empty column and any priority

 Expected behavior: The list view should match the number represented on the report column.

 Actual behavior: The list view shows no records.

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1519404

</td><td>

When users delete their sys\_json\_chunk data, it causes Flow Designer to fail at compilation

</td><td>

Users occasionally delete their sys\_json\_chunk data. If they delete the snapshot data, the table flows start breaking.

</td><td>

1.  Create a subflow.
2.  Publish the subflow.
3.  Run the subflow with script.
4.  Delete the sys\_json\_chunk data that is correlated to that subflows latest snapshot on sys\_hub\_snapshot.
5.  Flush CacheManager.
6.  Run the subflow with a script.

 It errors out.

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1648314

</td><td>

There is a 'LookUpRecord' error log when it gives no result

</td><td>

When 'Look up record' returns null, the sys log records an error log even if 'don't fail on error' is true.

</td><td>

 

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1658718

</td><td>

Catalog Builder generated tasks for requested items \(RITM\) have empty fields if the catalog item is updated after the RITM was submitted

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1718202

</td><td>

Error when opening up a flow context details

</td><td>

The record producer action should show the execution details as per the flow report. However, the user observes a 'Something went wrong' error on the screen and the page becomes non-responsive.

</td><td>

 

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1721354

</td><td>

Workflow stages for requested items are shown in English even in French language settings

</td><td>

Request items \(RITM\) associated to workflows are displaying stage values in English, even under French language settings. The issue doesn't happen when an RITM item is associated with a workflow.

</td><td>

1.  Install the French language plugin in a base instance.
2.  Submit a request for a catalog item that uses a workflow.
3.  Switch the language settings to French.
4.  Navigate to the sc\_req\_item table.
5.  Look for the RITM generated from Step 2.
6.  Look under the **Stage** field.

 Notice that the value is still displayed in English.

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1732451

</td><td>

The 'run\_as' flow is displaying as the user instead of the system when using the **Test** button

</td><td>

In the XML of the flow context, the 'run\_as' value is displayed correctly. However, it's displayed incorrectly in the report.

</td><td>

1.  When running a flow in foreground, create a flow with 'Run as' set to 'System'.
2.  Add a log action to the flow.
3.  Set the flow reporting to 'FULL'.
4.  Trigger the flow using the **Test** button in the foreground.
5.  Open the flow report. The 'Run as' section in the flow report displays the username of the person who triggered the flow.
6.  Modify the flow's **Trigger** &gt; **Advanced Options** &gt; **Where to run the flow** to 'Run flow in foreground'.
7.  Trigger the flow by meeting the trigger conditions.
8.  Open the flow report.

 Expected behavior: The 'Run as' section in the flow report should display 'System'.

 Actual behavior: The 'Run as' section in the flow report displays the username of the person who triggered the flow.

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1737061

</td><td>

Flow snapshots can't be deserialized when their total character length exceeds the deserialization limit

</td><td>

A subflow displays as 'payload' in the 'Flow Operations' view and the subflow context can't be opened.

</td><td>

1.  Create a large flow.
2.  Ensure that the flow uses subflows.
3.  Upgrade the instance.

 Observe that a 'Max String Length' error is reached.

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1747868

</td><td>

FlowGlideCompilerV2 isn't thread safe

</td><td>

Compilation of flows may throw an exception, or result in a corrupted flow, in the situation where multiple flows are compiled simultaneously.

</td><td>

 

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1755683

 [KB1640735](https://hi.service-now.com/kb_view.do?sysparm_article=KB1640735)

</td><td>

There's unexpected triggering of 'Run Once' flows due to the data cleaner job in 'sys\_flow\_plan\_context\_binding'

</td><td>

The data cleaner job is deleting records older than a year from the 'sys\_flow\_plan\_context\_binding' table. This is causing 'Run Once' flows to be triggered again, which is unexpected behavior.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Designer \(Family Channel\)

 PRB1761716

</td><td>

When making an update to a flow in the global domain as a user in a different domain, a duplicate flow is created

</td><td>

 

</td><td>

1.  Install the Domain Support - Domain Extensions Installer plugin.
2.  Create a user in the top domain.
3.  While logged in as an admin, create a flow in the global domain.
4.  Impersonate the user from step 2.
5.  Make sure the domain is still set to global and modify the flow created in step 3.
6.  Change user's domain to top.

 Expected behavior: The new flow should not exist in the user's domain.

 Actual behavior: A flow is created with the same name in the top domain.

</td></tr><tr><td>

Flow Engine

 PRB1743462

 [KB1638768](https://hi.service-now.com/kb_view.do?sysparm_article=KB1638768)

</td><td>

Large flows are failing with Flow Designer

</td><td>

Large flows are failing with Flow Designer with the following error: 'Rejected large REST payload with content-length = 27239395 bytes. Max allowed: 10485760 bytes.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1758754

</td><td>

The user observes a 'Unique Key violation detected by database' error when they run the flow 'Get All Occupancy by IDs'

</td><td>

The error message about 'unique key violation...' is coming from the exception stack trace.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1765110

</td><td>

The 'Get Catalog Variables' action gets the previous execution rows of multi-row variable sets

</td><td>

GetCatalogVariablesOperation adds the variable set entries to the ops CoCollection output. The output is starts out as the default value, which is then shared between subsequent executions of the compiled flow.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1772034

</td><td>

A flow remains 'In progress', isn't marked 'Presumed interrupted', and doesn't move forward

</td><td>

This defect causes flows built in Flow Designer and processes built in Process Automation Designer \(PAD\) to get stuck and not move forward even when records they're waiting on have been updated and moved forward.

</td><td>

 

</td></tr><tr><td>

Form Designer

 PRB1502906

 [KB0964319](https://hi.service-now.com/kb_view.do?sysparm_article=KB0964319)

</td><td>

A form's design can update sys\_choice records when no changes are made because of duplicate sys\_choice records

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1672671

</td><td>

Import policy text hyperlinks don't publish working links

</td><td>

When policy documents are imported in the Compliance Workspace via the **Import policy text** button, URLs are copied but when the policy is set to 'Published', the links in the document aren't clickable.

</td><td>

 

</td></tr><tr><td>

GRC Platform Plugins

 PRB1728648

 [KB1646055](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646055)

</td><td>

Vendor Risk Assessment designer makes many outbound calls, causing the browser to crash

</td><td>

There's around about ~60 outbound calls per second.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Guided Tours

 PRB1742187

</td><td>

The Service Portal header menu isn't loading in an embedded Service Portal \(/sp\) in Microsoft Teams on a browser

</td><td>

A console error is observed.

</td><td>

1.  Open any chat in Microsoft Teams app on browser.
2.  Select the **+** icon to add a new tab on the top bar in the chat.
3.  Select **See All Apps**.
4.  Select **Website**.
5.  Enter the name and URL.
6.  Select **Save**.

A tab at the top shows the newly created website that will prompt you to log in.

7.  Log in with test user credentials.

 Notice that the header menu item loads indefinitely and a console error message appears.

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

 PRB1755325

</td><td>

Line breaks are missing from the activity stream after a Washington upgrade

</td><td>

Occurs in the Service Portal widget 'Standard Ticket' tab.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1732823

</td><td>

Only the **Article body** field is displayed in a new knowledge creation form for Agent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HTML Editor

 PRB1755971

</td><td>

An HTML variable cursor returns to start with every keystroke

</td><td>

This causes backward writing.

</td><td>

 

</td></tr><tr><td>

Import Set API

 PRB1715017

 [KB1575986](https://hi.service-now.com/kb_view.do?sysparm_article=KB1575986)

</td><td>

A business rule introduced in Vancouver causes issues

</td><td>

A business rule called 'Update sheet num on change sheet name' updates all data source sheet numbers to have a default value of 1.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Import Set API

 PRB1757699

</td><td>

For a JDBC data source, a password change isn't recognized until the MID server is restarted

</td><td>

This happens in response to another problem. When upgrading to Washington and loading data on a data source using MID server for the SQL connection, users receive the following error: 'Cannot invoke "java.util.Map.keySet\(\)" because "this.fImportSourceFields" is null'.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1721309

 [KB1584953](https://hi.service-now.com/kb_view.do?sysparm_article=KB1584953)

</td><td>

An app node is throwing a java.io.IOException: 'Too many open files due to IDR/Kafka issues'

</td><td>

The node is unresponsive or having odd behavior, such as the sidedoor displaying an empty page and intermittent xmlstats.do outputs.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

JVM at Scale

 PRB1709224

 [KB1576486](https://hi.service-now.com/kb_view.do?sysparm_article=KB1576486)

</td><td>

Several of the memory graphs on the 'Performance' dashboards no longer display in Vancouver

</td><td>

One example is MemoryMaxMonitor.java. It represents the 'Max' line in 'Java Memory'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1734388

 [KB1628704](https://hi.service-now.com/kb_view.do?sysparm_article=KB1628704)

</td><td>

Users are unable to decrypt protected script errors in logs

</td><td>

Right after a Washington upgrade, users are observing a large number of Key Management Framework \(KMF\) decryption errors in the system logs.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1773544

 [KB1646553](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646553)

</td><td>

Initializing a system user before GlideProperties are loaded leads to caching an invalid system user when initializing Glide \(Glide.init\(\)\)

</td><td>

This issue occurs on instances with timezone setting's \(glide.sys.default.tz\) set to a region other than America/Los Angeles or US/Pacific. The system user is cached with an incorrect timezone during node start up. Instead of using the system property value \(glide.sys.default.tz\), it uses an incorrect value. This affects Flow, Notification, Business Rule, Schedule jobs and any processes run by a system user.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Knowledge Management

 PRB1681728

 [KB1515158](https://hi.service-now.com/kb_view.do?sysparm_article=KB1515158)

</td><td>

Two Japanese choices have the same sequence number

</td><td>

After the instance was upgraded to Utah from Tokyo, two Japanese choices have the same sequence number. This causes a disorder issue on kb\_knowledge.workflow\_state.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Knowledge Management

 PRB1733799

</td><td>

Unwanted guest user impersonation system logs are generated on KB article publish and access

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1734169

</td><td>

'You have reached the daily limit for replies posted by a user' error due to kb\_social\_qa\_answer ACLs

</td><td>

After selecting 'Post a question' and creating a question, some users are unable to post answers or comments to their own question. The observed error is 'You have reached the daily limit for replies posted by a user'.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1740935

</td><td>

A Customer Service Management \(CSM\) consumer is unable to comment on knowledge articles from the '$knowledge.do' page

</td><td>

The issue occurs even if the consumer has read access.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1783762

</td><td>

Authors that are not a member of the ownership group can no longer edit a Knowledge Base article, even if the glide.knowman.ownership \_group.override property is set to true

</td><td>

The relevant condition does not check if the user is the author of the KB article, and if the glide.knowman.ownership \_group.override property is set to true, causing the ACL to fail.

</td><td>

1.  Create an ownership group, for example 'Test Ownership Group'
2.  Add a System Administrator as the manager and add Abel Tuter as a member.
3.  Create a Knowledge Base with the itil and knowledge role in the 'Can Contribute' list.
4.  Make sure that the Publish workflow is Knowledge - Approval Publish.
5.  Set the following properties:
    1.  glide.knowman.ownership\_group.override = true
    2.  glide.knowman.ownership\_group.enabled = true
6.  Impersonate a user who is not a member of the 'Test Ownership Group', not an admin, and doesn't have a knowledge role but has an itil role.
7.  Create a knowledge article with:
    1.  Knowledge Base: General Knowledge
    2.  Ownership Group: Test Ownership Group
8.  Submit the knowledge article.

 Expected behavior: You can edit the knowledge article.

 Actual behavior: The knowledge article that was just created cannot be found in the list of knowledge articles. Therefore, the author cannot edit the knowledge article.

</td></tr><tr><td>

Language and Translations

 PRB1674206

</td><td>

The Japanese translation of 'true' and 'false' is changed to 'True' and 'False'

</td><td>

This is related to a previous issue from PRB1613806.

</td><td>

1.  Activate the I18N: Japanese Translations plugin.
2.  Switch to Japanese mode.
3.  Run sys\_ui\_message.list and check the translation of the values \[true\] and \[false\]

 Expected behavior: It should remain \[true\] and \[false\].

 Actual behavior: It is translated to \[True\] and \[False\], which is impacting some functions and causing messages like getDisplayValue\(\).

</td></tr><tr><td>

Legacy Agent Workspace

 PRB1713134

</td><td>

The activity appears in the foreground of the image sent by the end user requestor to the live agent in the workspace

</td><td>

When an agent opens an image sent by the requestor/end user in the workspace, the activity appears in the foreground of the image.

</td><td>

1.  Navigate to a Vancouver instance as an agent in one tab.
2.  Navigate to Service Operation Workspace and stay available.
3.  In an Incognito tab as an end user, log in and start a conversation from the portal '/sp' &amp; connect to a live agent.
4.  As the end user, send an image to the agent.
5.  As an agent, open the image sent by the end user.

 Expected behavior: The image should be shown properly and the activity shouldn't appear on top of the image.

 Actual behavior: When the agent opens the image, the activity is seen in the foreground of the image.

</td></tr><tr><td>

Legacy Agent Workspace

 PRB1722642

</td><td>

When two users open an HR Case in HR Agent Workspace, the second user can't see that the first is viewing

</td><td>

When user X opens a HR Case on the HR Agent Workspace, and then user Y opens the same HR Case on the HR Agent Workspace, user X can see that user Y is viewing the HR Case, but user Y can't see that user X is viewing the HR Case.

</td><td>

 

</td></tr><tr><td>

License Usage

 PRB1764672

 [KB1644243](https://hi.service-now.com/kb_view.do?sysparm_article=KB1644243)

</td><td>

License usage is slow for unlicensed entitles and progress indicator widgets are slow

</td><td>

On the 'License Usage' page, there's widgets to show counts for ignored installs, unlicensed installs, and installs requiring action on the publisher result, product result, and software model result. These aggregated counts aren't stored and instead queries are executed, which can take a long time.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1709691

 [KB1641555](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641555)

</td><td>

Each sort order of a column on 'Dashboards' acts like a separate view

</td><td>

In 'Dashboards', when a column is sorted, it seems like a new view is created with each column and its position in the list. The expected behavior is that the columns selected and their position remain the same regardless of what column is sorted.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1713894

 [KB1642444](https://hi.service-now.com/kb_view.do?sysparm_article=KB1642444)

</td><td>

List label displays the ASCII character '%20' in the place of a space

</td><td>

During periods of network or CPU throttling, a discrepancy is observed where ASCII characters like '%26' are displayed instead of their corresponding symbols, such as '&amp;', in the title. This issue pertains specifically to the display of ASCII characters and is noticeable when network or CPU throttling mechanisms are activated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1736155

 [KB1635300](https://hi.service-now.com/kb_view.do?sysparm_article=KB1635300)

</td><td>

There's a security restraints message in a workspace when selecting the 'View All' link or 'Open List in New Tab'

</td><td>

An 'X rows removed from this list by security constraints' message displays at the bottom of a list.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1752336

</td><td>

Inline editing for strings do not accept shift + enter to create lines

</td><td>

When in list view, if the user tries to add a line on a string by using the shift + enter shortcut, nothing happens. For example, the **Description** field on the incident list view. This worked as expected in the Vancouver release.

</td><td>

1.  Access any Washington DC instance.
2.  Navigate to any table list view, for example incident.list.
3.  Make sure a long string field is visible in the list, for example the **Description** field.
4.  Begin editing the field and press **Shift** + **Enter**.

 Expected behavior: The field to creates a breakline.

 Actual behavior: Nothing happens.

</td></tr><tr><td>

List Administration

 PRB1758905

</td><td>

If records are selected across multiple pages, the 'Assign to me' workspace list action assigns all records to the current user

</td><td>

 

</td><td>

1.  In Agent Workspace, or any configurable workspace, create a personal list on the task table.
2.  Navigate to the newly created list.
3.  Add the filter below:
    1.  Task type = Incident
    2.  Assigned to = empty
    3.  State = new
4.  Select any cell from the first page.
5.  Navigate to the sixth page and select any record.
6.  Navigate to any page and select any record.
7.  Navigate to page-1, do not select anything, and then navigate to page-3. SelectionQuery is empty there.
8.  Use the list action **Assign to me** to assign the three selected records to yourself.

 Expected behavior: Only the selected records should be assigned.

 Actual behavior: All records in the list are assigned / updated, as opposed to the three selected.

</td></tr><tr><td>

List Cell Menu

 PRB1757572

 [KB1645358](https://hi.service-now.com/kb_view.do?sysparm_article=KB1645358)

</td><td>

A list edit pop-up opens in a white space

</td><td>

In Vancouver, when doing a list edit, the cell edit window is opening in a white space at the bottom instead of next to the field being edited.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

ListServiceV2

 PRB1738528

</td><td>

The choice 'None' is displayed twice when editing a field in a list in the Japanese language

</td><td>

Two options of the text なし are displayed.

</td><td>

1.  Activate the I18N: Japanese Translations plugin.
2.  Run incident.list and add 'Resolution code' to list view.
3.  Switch to the Japanese language and double click 'Resolution code'.

 Notice that two options of the text なし are displayed.

</td></tr><tr><td>

Microsoft Reconciliation

 PRB1734544

</td><td>

Microsoft recon fails with StackOverflowError and IllegalStateException errors for a cluster

</td><td>

Recon fails with multiple errors.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1666031

 [KB1435403](https://hi.service-now.com/kb_view.do?sysparm_article=KB1435403)

</td><td>

In some cases, the AWS Cloud Discovery configuration can cause a StackoverFlow error

</td><td>

Specifically, when following the configuration in the reproduction steps, a StackOverflow error is reported in ecc\_queue input.

</td><td>

1.  Configure the parent account 'P' with 'Accessor' as Member Account 1.
2.  Configure the MID server with an instance profile as Member Account 2.
3.  Run Discovery on P.

</td></tr><tr><td>

MID Server

 PRB1731256

 [KB1632761](https://hi.service-now.com/kb_view.do?sysparm_article=KB1632761)

</td><td>

The MID Server is stuck while upgrading

</td><td>

Windows MID Server validation and upgrade from Utah to Washington gets stuck in an 'Upgrading' state due to missing privileges.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1734629

 [KB1646639](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646639)

</td><td>

MID Server upgrades can fail due to a file lock on wrapper.conf, leaving the MID Server down and unable to start without manual file repair

</td><td>

In a MID Server upgrade to Washington Patch 3 or lower, this may be seen in the upgrade process log: SEVERE: com.snc.dist.mid\_ upgrade.UpgradeException: java.nio.file.FileSystemException: C:\\...\\agent\\conf\\wrapper.conf: The process cannot access the file because it is being used by another process. The MID Server remains down, with missing files, and cannot be started again.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1753280

</td><td>

MID Server ConnectionCache leaks connections on the credentials\_reload event

</td><td>

When the MID Server receives a credentials\_reload event, all currently cached connections in the MID Server are orphaned without being cleanly shut down. This means that until the next garbage collection event, which sometimes can be several hours, resources are being consumed. This has been reported for JDBC connections because leaking database connections can cause bigger problems than other types of leaks, but all connection types cached by MID are affected.

</td><td>

1.  Set up glide with a MID Server with a JDBC connection.
2.  Run a database query.
3.  Using the database's diagnostics, note that the connection is still open since it's been cached.
4.  Change a credential in glide.

This causes a credentials\_reload command to be sent to all MID Servers. Notice that the database connection is still open.

5.  Run the database query again.

 Notice that the MID Server creates a connection, so there are two open connections to the database.

</td></tr><tr><td>

MID Server

 PRB1779555

 [KB1648957](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648957)

</td><td>

Due to how PRB1530694 temporarily deactivated the 'Encrypt ssh private key' business rule, PRB1665263 is skipped in Washington DC upgrades

</td><td>

The fix for PRB1530694 in San Diego involved the script action 'SSH Private Key Migration', which temporarily deactivated the business rule 'Encrypt ssh private key' on the discovery\_credentials table. As part of the update, a security.job.status event is fired, and a script action was run to migrate the data. Before old ssh\_private data could be re-encrypted, the 'Encrypt ssh private key' business rule had to be deactivated to allow the insertion of the new data without that interfering. Later, the script action activated it again, but just as a normal update, so it appears to be a customization by 'system'. When this business rule was changed again out-of-box in Washington DC, as the update for PRB1665263, it gets skipped in the upgrade and the fix is not applied.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1780511

</td><td>

The mid\_server role must inherit snc\_platform\_rest\_api\_access

</td><td>

If MID Server login users don't have the snc\_platform\_rest\_api\_access role, REST APIs used by the MID server may not work due to REST level status '403 Not Authorised' errors.

</td><td>

 

</td></tr><tr><td>

Mordor

 PRB1715771

</td><td>

Scripts that throw a lot of exceptions cause an out of memory error

</td><td>

An error is thrown: 'Couldn't decipher the stack trace resulting from the following JavaScriptException:...'

</td><td>

 

</td></tr><tr><td>

Next Experience UI16 Theming

 PRB1723262

</td><td>

The user is unable to highlight text in a form using Google Chrome

</td><td>

The user is unable to highlight text in a form using Google Chrome v121.0.6167.8.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1669623

</td><td>

Notification settings in Next Experience aren't translated in Utah

</td><td>

The notification settings aren't translated on the first load. They are translated on the advanced preferences.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1697827

 [KB1558900](https://hi.service-now.com/kb_view.do?sysparm_article=KB1558900)

</td><td>

'Show badge count' doesn't get incremented

</td><td>

The notifications badge count on the bell icon doesn't get incremented immediately when an incident is assigned to them. If a user logs out, closes the browser, and logs back in, they might see the badge count updated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1712079

 [KB1567085](https://hi.service-now.com/kb_view.do?sysparm_article=KB1567085)

</td><td>

The Application Selector displays only recently selected applications

</td><td>

All active applications in the instance should be displayed.

</td><td>

1.  Access any Vancouver instance and set the system property 'glide.ui.next\_experience .instance\_tools\_disabled' to false.
2.  Impersonate a user.
3.  Toggle **Show instance tools.**
4.  Choose an application, such as Employee Center Core.
5.  Attempt to select another application by either expanding the **Application Scope** icon or entering the name of any other currently active application on the instance.

 Expected behavior: All active applications in the instance should be displayed.

 Actual behavior: Only the recently selected application scopes are displayed.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1714303

 [KB1641644](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641644)

</td><td>

Domain picker fails to switch to 'Recent Selections' domains when the system property glide.ui.domain\_reference\_ picker.enabled is set to true

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1719513

</td><td>

An 'Error 500' message is received and the filter navigation breaks for users when logging in

</td><td>

If a user's bookmark contains a malformed URL and Next Experience is active, an 'Error 500' message appears when logging in as the user, and the navigator menus break.

</td><td>

1.  Activate Next Experience.
2.  Navigate to sys\_ui\_bookmark.do to create a new favorite for a user.
3.  On the form, select any user for the **User** field.
4.  In the **URL** field, add a malformed URL.
5.  Save the record.
6.  Log in as/impersonate the user the bookmark record was created for.

 After logging in as the user, the user immediately receives an 'Error 500' message, and the main filter navigator along with the favorites navigator is empty.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1733072

</td><td>

Global search doesn't automatically open a record when the user queries for a record number with the Enter key

</td><td>

Previously, when pasting a case or task number, the quick results would highlight the record and open it directly when the user pressed Enter. Now, if the user presses enter, a console error is thrown. The user needs to use the down arrow or the mouse to highlight the record and open it directly.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1763887

</td><td>

After upgrading to Washington DC, the 'Not Found' tab automatically opens in a workspace when the user selects a logo

</td><td>

The issue is not reproducible in Vancouver and Utah.

</td><td>

1.  Log in to an instance with a workspace as the homepage.
2.  Select a logo.
3.  Check if the 'Not Found' tab is opened every time the logo is clicked.

</td></tr><tr><td>

Notification Preferences

 PRB1610033

</td><td>

When Next Experience is enabled, a dashboard stops displaying after closing the 'Notification Preferences' pop-up window

</td><td>

After closing a modal window from 'My Notification Preferences', the dashboard in the background changes to something else. The issue only occurs when the Next Experience UI is enabled.

</td><td>

1.  Log in to a Tokyo instance.
2.  Ensure that glide.ui.polaris.experience is set to true.
3.  Type 'Dashboards' in the filter navigator.
4.  Open any dashboard, for example, 'My Assets'.
5.  After the dashboard is finished loading, type 'My Notification Preferences' in the filter navigator.
6.  Open 'My Notification Preferences'.
7.  After 4 seconds, close the 'My Notification Preferences' pop-up window.

 Expected behavior: The 'My Assets' dashboard is displayed.

 Actual behavior: The 'My Assets' dashboard isn't displayed. Some other page saying 'Manage your instance' is displayed instead.

</td></tr><tr><td>

Notification Preferences

 PRB1701164

</td><td>

The 'Notification Preferences' link on an email opens two tabs on the browser

</td><td>

 

</td><td>

1.  Navigate to **System Logs** &gt; **Emails**.
2.  Open an existing email.
3.  Select the 'Preview Email' related link.
4.  Select **Notification Preferences**.

 Expected behavior: The new tab opens, linking to the notification preferences.

 Actual behavior: Two new tabs open, one with the home page and the other with the notification preferences.

</td></tr><tr><td>

Now Code Editor

 PRB1426660

 [KB0856205](https://hi.service-now.com/kb_view.do?sysparm_article=KB0856205)

</td><td>

UI scripts are served to the client unexpectedly to replace dollar-bracket syntax

</td><td>

As a result, the UI scripts served to the client don't match the record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now Code Editor

 PRB1751768

</td><td>

A valid script throws syntax/parsing errors in the modern background scripts

</td><td>

A valid script displays the warning 'Parsing error' in background script, even though it runs fine. The background scripts editor isn't honoring the version of the scope.

</td><td>

 

</td></tr><tr><td>

Performance Analytics API

 PRB1715114

</td><td>

The selected indicator breakdown filter element is not always applied to the Performance Analytics indicator data visualisation

</td><td>

 

</td><td>

1.  Log in to any base instance.
2.  Navigate to Platform Analytics \(PA\) Workspace.
3.  Open a dashboard.

Two data visualization exist \(1 PA indicator report and 1 simple table report\) and one indicator breakdown filter.

4.  Select the element shown on the pre-populated list of indicator breakdown filters.

It is applied to both the PA indicator report and the simple table report data visualization.

5.  Select something that is not in the pre-populated list.

 It is not applied to the PA indicator report, but is applied to the simple table report data visualization.

</td></tr><tr><td>

Performance Analytics

 PRB1739397

</td><td>

The breakdown limitation isn't respected for the 'Correlation' job, resulting in high memory consumption

</td><td>

The 'PA CalculateCorrelation' job causes memory issues and the node restarts.

</td><td>

 

</td></tr><tr><td>

Platform Licensing

 PRB1697425

</td><td>

A report name is truncating for Integration Hub \(IH\) Pool licenses

</td><td>

Some of the report names are truncated because the **Title** field can contain a maximum of 100 characters.

</td><td>

Trigger a 'UA License Download' job with IH rolling contributed licenses.

</td></tr><tr><td>

Platform Licensing

 PRB1746750

 [KB1639094](https://hi.service-now.com/kb_view.do?sysparm_article=KB1639094)

</td><td>

Subscription Entitlements Service isn't accessible in a Java layer

</td><td>

This causes an error to be logged during the transaction. Transactions are incorrectly attributed as 'unlicensed'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Runtime

 PRB1770154

</td><td>

PDF generation from mobile shows invalid values in the 'Cost' column for incidentals

</td><td>

 

</td><td>

1.  As an admin user, navigate to **Field Service** &gt; **Administration** &gt; **Configuration** &gt; **Add-ons**.
2.  In the 'Signature Capture And PDF Order Summary' section, toggle all the switches to on.
3.  Log in to the ServiceNow Agent application as an agent.
4.  Navigate to **Settings** &gt; **Offline mode**.
5.  Download the cache and don't turn ON offline mode.
6.  Navigate to 'My work' and select any task.
7.  Navigate to **Related** &gt; **Incidentals**.
8.  Create an incident of the type 'Car' with a cost of $180.
9.  Navigate to **Settings** &gt; **Offline mode** and switch to offline mode.
10. Navigate to the same task and create another incident in offline mode of the type 'Rental'.
11. Switch back to online mode.
12. Navigate back to the same task and close complete the task.
13. Navigate to the work order for that task and make sure that the work order is 'Close complete'.
14. Select **Sign**, confirm, and add your signature.
15. Navigate to the activity stream. Notice that a PDF file has been generated.
16. Open the PDF file and look at 'Service Management Incidentals'

 Observe that the 'Cost' column for the first incidental shows the value 'wo\_incidentals80.00', but it should be $180.

</td></tr><tr><td>

Process Automation Designer \(Family Channel\)

 PRB1728558

</td><td>

Process Automation Designer can't select trigger for users with the 'pd\_admin' role

</td><td>

A user with the pd\_admin role is unable to select a trigger type. It says 'no results found'. If the admin role is assigned to the user, they are able to select trigger options.

</td><td>

 

</td></tr><tr><td>

Release Management

 PRB1745992

</td><td>

Release management V2 users are not able to access certain tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB1734528

 [KB1642647](https://hi.service-now.com/kb_view.do?sysparm_article=KB1642647)

</td><td>

There's an incorrect business duration calculation on sc\_task when the system date format is set to dd-MM-yyyy

</td><td>

The behavior for DurationCalculator. calcScheduleDuration hasn't changed from Utah to Vancouver.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Resource Exchange

 PRB1735826

</td><td>

There's an issue with the race conditions generateAutoKeyExchangeRequests and startKeyExchangeClone

</td><td>

The daily scheduled job \(generateAutoKeyExchangeRequests\) executes before the post clean-up script \(startKeyExchangeClone\). If this occurs, generateAutoKeyExchangeRequests erases and replaces all the cloned over template request messages, which are then consumed \(erroneously\) by startKeyExchangeClone. This causes automated key exchange to fail. The request message displays 'Error on Instance'.

</td><td>

1.  Prepare two Key Management Framework \(KMF\) Healthy instances.
2.  Navigate to one of the instances.
3.  Navigate to the 'Resource Exchange' table.
4.  Navigate to sn\_kmf\_resource\_exchange\_request.
5.  Remove the filter.
6.  There should be a set of template request messages \(Request Pending\). If there's not, navigate to the background and execute generateAutoKeyExchangeRequests to generate the template request messages.
7.  Copy all of the request messages in an XML file.
8.  Navigate to the other instance.
9.  Navigate to the 'Resource Exchange' table.
10. Navigate to sn\_kmf\_resource\_exchange\_request.
11. Remove the filter.
12. Delete all records in this table.
13. Import the XML file created from the source instance.

This state simulates what the state should be on a cloned target instance when startKeyExchangeClone runs.

14. Execute generateAutoKeyExchangeRequests.
15. Examine the 'Resource Exchange' table and verify the imported template messages from the source are gone.
16. Execute startKeyExchangeClone.
17. Re-examine the 'Resource Exchange' table.

 The messages were processed with Status = 'Error on Local Instance'.

</td></tr><tr><td>

Resource Management

 PRB1738051

</td><td>

Error when running the client script 'ShowInfoMsgIfResPlanWasCleared': ReferenceError: GlideURL is not defined

</td><td>

A client script throws an error in the browser console: 'Error while running Client Script "ShowInfoMsgIfResPlanWasCleared": ReferenceError: GlideURL is not defined when the user accesses the time card portal and tries opening the time card form.'

</td><td>

1.  Provision an instance with Resource Management and Timecard Portal installed.
2.  Navigate to the Time Sheet portal.
3.  Add a time card \(From task or the 'other' tab\).
4.  Select the three dots.
5.  Select **Open Form View**.

 Observe the error message shown at the top of the form: 'There is a JavaScript error in your browser console'.

</td></tr><tr><td>

Resource Management

 PRB1764189

</td><td>

When users try to select an **Extend** UI action on a resource plan from the project workbench, the 'Extend resource plan' pop up appears empty

</td><td>

Test.

</td><td>

1.  Navigate to the Project module.
2.  Open any project.
3.  Under the related link, select the project workbench.
4.  Under the 'Resource' tab, select any resource plan.
5.  Select the **Extend** UI action.

 A blank screen appears.

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

 PRB1741012

 [KB1635189](https://hi.service-now.com/kb_view.do?sysparm_article=KB1635189)

</td><td>

The 'Prevent invalid source &amp; target on RCA' business rule is causing duplicate records in the sys\_restricted\_caller\_access table

</td><td>

The 'Prevent invalid source &amp; target on RCA' business rule is causing the **Target** field to be set to NULL. This lets duplicate records be inserted into the sys\_restricted\_caller\_access table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Scheduled Jobs

 PRB1754295

</td><td>

Long running jobs during Scheduler V2 to V3 switchover are re-queued and run twice

</td><td>

Any jobs running when the instance upgrade is marked as fully completed and take longer than 5 minutes to complete end up being re-queued.

</td><td>

1.  Update 'glide.central\_scheduler.enable' to false.
2.  Create a job in sys\_trigger with name the 'testjob' and script - gs.sleep\(600000\).
3.  Update 'glide.central\_scheduler.enable' to true.
4.  Wait for 5 minutes.
5.  Navigate to the localhost logs.

 Expected behavior: testjob shouldn't be re-queued and not run twice.

 Actual behavior: testjob is re-queued and run twice.

</td></tr><tr><td>

Schedule Optimization

 PRB1777921

</td><td>

The end-to-end Schedule Optimization flow is not working as expected due to an update in Predictive Intelligence

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Script Includes

 PRB1761513

</td><td>

Hung semaphore thread on EmbeddedSlotMap.java

</td><td>

In Washington there has been a large increase in the number of alerts for hung semaphore threads.

</td><td>

 

</td></tr><tr><td>

Seismic Framework

 PRB1736853

</td><td>

The 'Close' icon is missing in a popover component

</td><td>

The Service Worker overrides the cache buster value, which causes library-uxf to load twice.

</td><td>

1.  Create a track instance.
2.  Set up a proactive trigger.
3.  Open the instance in incognito mode.

 Observe that the 'Close' icon is missing.

</td></tr><tr><td>

Server-side scripts

 PRB1703346

 [KB1637446](https://hi.service-now.com/kb_view.do?sysparm_article=KB1637446)

</td><td>

Script Debugger doesn't work in module scripts

</td><td>

The debugger breaks correctly when the module script is edited, but fails to break when the script is rerun \(cached\).

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Server-side scripts

 PRB1769142

</td><td>

No source handler for installation exits causes 'Error accessing descriptor for metaObject: package\_private script include function IE : no thrown error'

</td><td>

Installation exits are treated as script include objects. When getting the descriptor, it searches sys\_script\_include instead of sys\_installation\_exit. Since it can't find the installation exit, the error is thrown.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1786423

</td><td>

Transpiler doesn't respect the custom per-thread memory limit, causing an error

</td><td>

Some threads in the transpiler don't respect the value of the system property, com.glide.script.swc .memory\_threshold\_in\_kb, and instead throw an exception when memory usage exceeds the default per-thread limit of 16MB. The error is logged repeatedly and prevents a portion \(up to 1/4\) of the server-side scripts executed on the node to fail.

</td><td>

 

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1763735

</td><td>

The attachment is missing on a task record after submitting the record producer, which was saved as draft

</td><td>

This issue is observed in Washington DC instances.

</td><td>

1.  Navigate to /sp and search 'Create incident'.
2.  Complete the mandatory fields and attach a file.
3.  Select **Save as draft**.
4.  Navigate to the 'My Request' page and select the request which was saved as a draft.
5.  Select **Submit**.
6.  Select the 'Attachment tab.

 Expected behavior: The attachment is shown.

 Actual behavior: The attachment is missing.

</td></tr><tr><td>

Service Catalog

 PRB1710169

</td><td>

In Process Automation Designer \(PAD\), the UI Macro 'show\_process' has an issue

</td><td>

An error displays.

</td><td>

1.  Visit any category item guide leveraging PAD \(table 'sc\_cat\_item\_guide'\).
2.  Ensure that the **Sequencing Process** field has an entry.
3.  Select the UI Macro 'Show Sequencing Process'.

A new page opens.


 A 404 error message is displayed instead of the open record on PAD. The same error occurs for 'Generate sequence' as well.

</td></tr><tr><td>

Service Catalog

 PRB1732298

 [KB1641827](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641827)

</td><td>

Order Guide sequencing is not populating Sequencing ID in item cache in some nodes.

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog

 PRB1736392

</td><td>

Update Sets captures additional entries by 'system'

</td><td>

When updating a Catalog Client Scripts record in Vancouver, its parent record, 'Record Producer', gets added to the update set with an **Updated By** field made by the system user. There are no changes captured within this update by the system - it simply creates an extra entry.

</td><td>

1.  Provision a Vancouver instance
2.  Create a new update set and make it the current update set.
3.  Navigate to catalog\_script\_client.list and select any base instance record.
4.  Make any small update \(for example, add '//test' to the script\).
5.  Navigate to the new update set.

 Expected behavior: Observe the entry made by the user \(as expected, there is no system entry captured\).

 Actual behavior: Observe the entry made by the user and the entry captured by the system.

</td></tr><tr><td>

Service Catalog

 PRB1751304

</td><td>

Variable details aren't displaying after upgrading to the latest patch releases on the Agent Mobile app

</td><td>

Issue occurs on both iOS and Android.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1763397

 [KB1644922](https://hi.service-now.com/kb_view.do?sysparm_article=KB1644922)

</td><td>

ESC/SP Cart count isn't working for users with 'Accessibility enabled' set to true

</td><td>

When a user has the 'Accessibility enabled' option in their ESC portal profile enabled, then the count for the cart \(in ESC/SP header\) isn't visible. If a user turns off 'Accessibility enabled', then the count comes back.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog

 PRB1763535

 [KB1646316](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646316)

</td><td>

When a CRUD operation is triggered from a 'Record Producer' script in a non-global scope, business rules aren't executed due to an incorrect 'current' reference

</td><td>

Business rules that are supposed to run due to CRUD operations triggered by the 'Record Producer' script never run. This can affect multiple use cases where they don't rely on the Record Producer's natural flow to create records, but instead use the **script** field to create records in multiple tables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

ServiceNow Security Center \(Family Release\)

 PRB1711845

</td><td>

The 'API calls to Security Incident Response should use accounts with user role sn\_si' scope should be changed from 'Security Center' to 'Global'

</td><td>

From the investigations related to the 'API calls to Security Incident Response...' check, the findings generation logic of check is found to be setting the source record incorrectly.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1282090

 [KB0998082](https://hi.service-now.com/kb_view.do?sysparm_article=KB0998082)

</td><td>

If the platform UI has 'show all text', **Journal** fields \(comments and work notes\) are cut off in the 'Ticket Conversations' widget

</td><td>

**Journal** field text that is hidden in the activity because of the glide.max\_activity\_size property isn't displayed in the portal and there's no way to display it like the normal UI.

</td><td>

1.  Add the system property glide.max\_activity\_size.
2.  Set the type to 'Integer'.
3.  Set the value to '1024'.
4.  Navigate to any record in the normal platform.
5.  Add a long amount of text as a comment.
6.  Reload the form.
7.  Confirm that the text is cut off and there's a blue link to 'show all text' that, when selected, all of the text displays.
8.  Navigate to the same record in the 'Ticket Conversations' widget in the portal.

 Expected behavior: All of the text should be displayed or have an option to show more.

 Actual behavior: The text is cut off, and there's no way to expand it to display the additional text.

</td></tr><tr><td>

Service Portal

 PRB1405409

 [KB0994576](https://hi.service-now.com/kb_view.do?sysparm_article=KB0994576)

</td><td>

A Service Portal form widget loads unexpected UI scripts and includes them in the uploaded form data

</td><td>

A form widget loads UI scripts that are not added to the widget dependencies. This adds overhead time to widget loading.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1588397

</td><td>

In the 'Form' widget, a form is submitted multiple times when a user clicks CTRL + S, 'Save' repeatedly, or performs a CTRL + S long press

</td><td>

This issue could result in 100s of updates in the case form, which has repercussions in real-time applications.

</td><td>

1.  Navigate to an instance.
2.  Open any form \(Case/INT\) in Service Portal.
3.  Add any comments.
4.  Repeatedly click CTRL + S or CMD + S for Mac.

 Duplicate comments are added to the form.

</td></tr><tr><td>

Service Portal

 PRB1735271

 [KB1629628](https://hi.service-now.com/kb_view.do?sysparm_article=KB1629628)

</td><td>

The portal search bar is missing after upgrading to Vancouver

</td><td>

The issue is intermittent. It doesn't occur to all users or all instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1758218

</td><td>

A field is hidden when a read-only check box is clicked

</td><td>

In a catalog item, check box variables are selectable even though they're read-only by default. If a read-only check box is set to 'True', a situation can occur where a field is hidden when the check box is clicked even though the check mark is invisible.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1758358

</td><td>

'Show' URL type fields/variables aren't unlocked by default on a portal

</td><td>

'Show' URL type fields/variables aren't unlocked by default on a portal even after the glide.ui.unlock\_empty\_url property's value is set to true. They display as locked.

</td><td>

 

</td></tr><tr><td>

Service Portfolio Management

 PRB1731498

 [KB1587599](https://hi.service-now.com/kb_view.do?sysparm_article=KB1587599)

</td><td>

There's long loading times for Service Portal on a cold cache of catalog items

</td><td>

A large amount of data in Service Catalog is needed to reproduce the loading times. The initial load time takes 40+ seconds to render the categories and catalog items available to the user. It's a few seconds in subsequent loads with caching.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Session Log

 PRB1739637

</td><td>

The script debugger doesn't work as expected after a Vancouver upgrade

</td><td>

 

</td><td>

1.  Log in to the latest Vancouver version.
2.  Create a custom script include or open any existing script include.
3.  Set breakpoints in server side script include.
4.  Open the script debugger.
5.  Call the script include from "Scripts - Background".

 The script runner stops on the first breakpoint, but isn't able to step through the code.

</td></tr><tr><td>

Session Management

 PRB1730421

</td><td>

org.apache.coyote.http11. upgrade.UpgradeProcessorInternal consumes high memory and causes memory contention on the node

</td><td>

One node has more frequent out of memory or semaphore exhaustion than any other nodes. Heapdump displays a large object: 'org.apache.coyote.http11. Http11Nio2Protocol'.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1455184

</td><td>

Reconciliation fails with the following error, 'InternalError: String object would exceed maximum permitted size of 33554432'

</td><td>

When running reconciliation, due to a platform limitation of 32 MB for the string object, the reconciliation job fails.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1665612

 [KB1641524](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641524)

</td><td>

Purchased rights in alm\_license are limited by an integer field type

</td><td>

A user can have a value that can only be contained by a long field type, causing issues due to the limitation.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1722817

</td><td>

'SAM - Deduplication Worker' has a long running query

</td><td>

The logs show the query is slow.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1731302

 [KB1637220](https://hi.service-now.com/kb_view.do?sysparm_article=KB1637220)

</td><td>

The 'Potential Savings' drill down on the Software Asset Management \(SAM\) landing page doesn't work as expected

</td><td>

Error messages are displayed when the user navigates to other pages.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1741844

 [KB1637537](https://hi.service-now.com/kb_view.do?sysparm_article=KB1637537)

</td><td>

Reconciliation in Software Asset Management doesn't work after upgrading to Washington DC

</td><td>

The **Publisher** field of the 'Run Reconciliation' UI page doesn't retrieve any value.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB1715795

 [KB1585469](https://hi.service-now.com/kb_view.do?sysparm_article=KB1585469)

</td><td>

If on entitlements the software model has license\_under\_management = false, allocations shouldn't be processed

</td><td>

License metric results \(LMR\) aren't created for entitlements on software models that aren't under management \('license\_under\_management' = false\). However, the code is processing allocations on these entitlements. This causes downstream issues attempting to create a 'rights used by' for the allocated device/user when an LMR doesn't exist. The error arises as a downstream effect.

</td><td>

1.  Create an allocation on a 'per device' entitlement.
2.  Make the entitlement software model LUM = false.
3.  Run recon.

 The recon status is 'partially completed'. In the progress summary logs, there's the failure: 'TypeError: Cannot read property "null" from undefined'. There might be a record in 'samp\_licenses\_required\_by' with a blank LMR and 'allocated not in use' &gt; 0.

</td></tr><tr><td>

Syntax Editor

 PRB1725418

 [KB1588249](https://hi.service-now.com/kb_view.do?sysparm_article=KB1588249)

</td><td>

Auto-complete options are missing

</td><td>

Auto-complete isn't displaying all the completion options expected for g\_form and other variables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Events

 PRB1738452

</td><td>

Glide.policy.eventdelegator isn't updating, causing the event queue to not process events

</td><td>

This issue pertains to the event queue's failure to process events as expected. Despite the measures taken to delete child entities and re-establish the parent entity, there's no observable decrease in the event queue.

</td><td>

 

</td></tr><tr><td>

System Update Sets

 PRB1737199

</td><td>

An error message appears between every two update sets

</td><td>

Once every two update set commits, the user sees the following error on the UI, which prevents the commit of a second update set for almost 30 seconds \(even if the first update set is already committed\): 'Update set preview and commit are unavailable because another operation is running: Add authentication checks to empty ACLs'.

</td><td>

 

</td></tr><tr><td>

Table Administration and Data Management

 PRB1563161

</td><td>

Instant alter doesn't work if a table has columns with an old datetime format

</td><td>

This occurs when a column is created on an old engine version and the table hasn't been altered after a DB engine update

</td><td>

1.  Make sure an affected table has enough records to trigger an online alter \(5k +\)
2.  Enable instant alter.
3.  Perform an alter operation on an affected table \(for example, add a new column\).
4.  Observe that alter is online and not instant.
5.  Alter the table again.

 Observe that the second alter is instant.

</td></tr><tr><td>

Table Administration and Data Management

 PRB1703208

</td><td>

An index with a combination of synchronized and non-synchronized fields causes syntax errors

</td><td>

 

</td><td>

1.  Create a compound index with a combination of synchronized and non-synchronized fields on CMDB \(for example: name, sys\_class\_path,managed\_by\).
2.  Run a filter on cmdb list, include a condition on the field that exists on cmdb$par1 \(make sure order is on 'name'\).

 Observe the error 'Syntax Error or Access Rule Violation detected by database \(\(conn=797954\) Key 'idx2' doesn't exist in table 'cmdb\_par10'\)'.

</td></tr><tr><td>

UI Builder \(Family Channel\)

 PRB1627810

 [KB1561055](https://hi.service-now.com/kb_view.do?sysparm_article=KB1561055)

</td><td>

In UI Builder, sys\_ux\_macroponent records and newly created list IDs might be saved as 'Select...'

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Field Administration

 PRB1695552

</td><td>

For translated text reference fields, the reference pop-up list doesn't display a value when a right-to-left \(RTL\) language is used

</td><td>

 

</td><td>

1.  Have any RTL language, like Arabic, plugin installed.
2.  Create a table to be used as a reference table with at least the following fields:
    -   Name: Display column, Type: Translated Text, Display: true
    -   Name: Active, Type: True/False
    -   Name: Type, Type: Choice, Choices: Type A, Type B
3.  Create at least the following records in the new table:
    -   Display column: 'Ref - Type A - Active 1', Type: Type A, Active: true
    -   Display column: 'Ref - Type A - Inactive 1', Type: Type A, Active: false
4.  Create a reference type of field on the incident table.
5.  Make that field refer to the newly created table in step 1.
6.  Configure the incident table form layout to show this field.
7.  Change the session language to Arabic.
8.  Open any incident.

 Expected behavior: The type 'Ref' in the **Reference** field should display the 2 entries from the table created before.

 Actual behavior: The type 'Ref' in the **Reference** field displays the 'Reference' list but the list has empty entries.

</td></tr><tr><td>

UI Field Administration

 PRB1702033

</td><td>

The **Time worked** field isn't honoring system property glide.ui.timer.started

</td><td>

The field type sn-record-time-worked-connected is impacted.

</td><td>

1.  Configure the incident form.
2.  Add 'Time Worked' to the 'Workspace' view.
3.  Set the sys property glide.ui.timer.started=false
4.  Open an incident record in a Customer Service Management or Service Operations Workspace workspace.
5.  Navigate to the **time worked** field.

 Expected behavior: The **timer** field should be paused and the **play** button should be displayed.

 Actual behavior: The **timer** field is ticking and the **pause** button is displayed.

</td></tr><tr><td>

UI Field Administration

 PRB1706249

 [KB1550638](https://hi.service-now.com/kb_view.do?sysparm_article=KB1550638)

</td><td>

The **reference** field search results list blocks the field if Next Experience is turned off

</td><td>

The issue only happens if Next Experience is turned off.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1665993

</td><td>

g\_aw.closeRecord\(\) doesn't work for new records in a workspace

</td><td>

After creating a **Save and close** UI action, it isn't possible to close the current record tab for new records.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1706564

</td><td>

UI policy with a **Date/time** field condition isn't invoked on the workspace when glide.sys.date\_format is set to dd-MM-yyyy

</td><td>

When glide.sys.date\_format is set to dd-MM-yyyy, the UI policy with a **Date/time** field condition does not work as expected on workspaces. It works as expected on UI16/Next Experience. The default date format yyyy-MM-dd works on both UI16/Next Experience and workspaces.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1717921

</td><td>

Raw HTML is displayed in the 'Show other active tasks' pop up

</td><td>

In the /problem.do form page, there is a button next to 'Service' called **Show other active tasks**. When selected, it displays a pop-up with raw HTML.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1734774

</td><td>

The UI Builder 'now-record-common-attachments-connected' component doesn't work as expected on new records for non-admin users and doesn't show the '+Add File' option

</td><td>

The UI Builder attachments component \(now-record-common-attachments-connected\), when tied with a 'Glide Form' data resource, doesn't show the '+Add File' option for non-admin users.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1746953

</td><td>

In Washington DC, the value of a **reference** field is displayed as 'undefined' if it is changed to a blank \(no value\) using the OnChange client script

</td><td>

On Washington DC, the value of a **reference** field is displayed as 'undefined' if it is changed to a blank \(no value\) using OnChange client script, even though it is displayed as a blank \(no value\) in Vancouver.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1765581

</td><td>

Attachment modal behavior issue when selecting a check box with a large number of attachments present

</td><td>

When selecting a check box with large number of attachments present, the modal is cut off and moves up as more attachments are added. The issue can be reproduced in UI16.

</td><td>

1.  Login to the instance.
2.  Turn off the Next Experience UI.
3.  Open any incident or kb\_knowledge.
4.  Add around 15 attachments to the case.
5.  Select the check box of the last attachment in the modal.

 Expected behavior: The modal does not move when selecting the check boxes of attachment.

 Actual behavior: With a large amount of attachments present, selecting the check box will move the modal up and cut the top off. This only works for the attachment in the lower part of scroll.

</td></tr><tr><td>

UI Form Administration

 PRB1784983

 [KB1649352](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649352)

</td><td>

Duplicate UI scripts that have the same exact name prevent a workspace page from loading

</td><td>

Workspace pages fail to load if there are duplicate UI scripts with the same API name in the sys\_ui\_script table. This is caused by a functional change to how the workspace UI scripts are called.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Upgrade Monitor

 PRB1717068

 [KB1585080](https://hi.service-now.com/kb_view.do?sysparm_article=KB1585080)

</td><td>

Trying to 'Resolve Conflicts' for scripts coming from the Upgrade Monitor doesn't work correctly

</td><td>

Uncaught TypeError: 'Failed to execute 'observe' on 'MutationObserver': parameter 1 is not of type 'Node''.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1681503

 [KB1638974](https://hi.service-now.com/kb_view.do?sysparm_article=KB1638974)

</td><td>

BucketStats errors appear in the logs from /xmlstats.do when the user opens a workspace

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1724083

</td><td>

Switching between tabs in the workspace results in the incorrect content being displayed

</td><td>

Switching between tabs in workspace results in the incorrect content being displayed \(within the Record Tabs component\).

</td><td>

1.  Open any incident record within the SOW workspace \(or any other workspace with the older record page\).
2.  Switch between the workspace tabs.

 Notice that the incorrect content is intermittently displayed within the tab.

</td></tr><tr><td>

UX Framework

 PRB1733058

</td><td>

The macroponent doesn't load intermittently when the parent app of an experience is empty

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1737007

</td><td>

Closing multiple tabs quickly converts an existing Workspace tab to a ghost 'Details' tab that can't be closed

</td><td>

When the user closes tabs quickly, the runtime action handler attempts to process all incoming events at once. This causes the property to enter a failed state.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1758514

 [KB1641590](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641590)

</td><td>

An instance loads for a long time after upgrading to Washington due to glide.ui.polaris.theme.custom

</td><td>

After upgrading, instances don't load or load slowly, and have an empty or invalid value for glide.ui.polaris.theme.custom.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1746294

</td><td>

After selecting the item on a carousel, the link to the image is shown

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Visual Task Boards

 PRB1697799

</td><td>

More tasks are visible in a list than in the Visual Task Board \(VTB\)

</td><td>

The owner of the VTB doesn't have access to all the records in incident table, and thus only see cards that they can see. However, the number of cards for the board member is more.

</td><td>

1.  Install the plugin Agile Development 2.0.
2.  Create a group in sys\_user\_group.list with type set as 'Agile Team'.
3.  Add two users with scrum\* roles to the group.
4.  Impersonate user 1.
5.  Open the Agile Board.
6.  Create a sprint for the group and set the sprint to current.
7.  Check the Agile Board's properties.
8.  Verify that the board owner is set to user 1.
9.  Add stories to the current sprint.
10. Check the Agile Board that stories appear on it.
11. Turn off and remove all roles user 1.
12. Impersonate user 2.
13. Create a story.

 In an Agile Board, this story doesn't appear.

 If in a sprint form, the story does appear.

</td></tr><tr><td>

Web UX Runtime

 PRB1770269

</td><td>

Some buttons aren't translated

</td><td>

The buttons, **Close Tab**, **Close Other Tabs**, and **Close All Tabs** don't display their translations or MSG prefixes.

</td><td>

1.  Set up a testing environment with a language plugin installed \(for example, com.snc.i18n.french\).
2.  Sign in as a System Administrator.
3.  Enable i18n debug prefixes.
4.  Navigate to **SOW** &gt; **List** &gt; **Changes** &gt; **All**.
5.  Select a record.
6.  Change the language to French and refresh.
7.  Select the three dots in the greyed out toolbar in the top right corner.

 Observe that the strings **Close Tab**, **Close Other Tabs**, and **Close All Tabs** aren't translated.

</td></tr></tbody>
</table>## All Other Fixes

To view a list of all other PRBs fixed in Xanadu, refer to [All other Xanadu fixes](xanadu-all-other-fixes.md).

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


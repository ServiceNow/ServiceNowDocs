---
title: Yokohama Patch 4
description: The Yokohama Patch 4 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-06-06"
reading_time_minutes: 68
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 4

The Yokohama Patch 4 release contains important problem fixes.

-   **Yokohama Patch 4 was released on June 6, 2025.**
    -   Build date: 06-04-2025\_1836
    -   Build tag: glide-yokohama-12-18-2024\_\_patch4-05-14-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y04.00.xlsx).

## Overview

Yokohama Patch 4 includes 281 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp4.png "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 4 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 4, refer to [KB2150760](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2150760).

## Changes in Yokohama Patch 4

-   **QueryRangeACLAuditor**

    This patch includes the May Maintenance update script in the form of a script include \(QueryRangeACLAuditor\). This script is not triggered automatically and must be run after a patch upgrade. More details on running the QueryRangeACLAuditor and its functionality can be found in [KB2046494](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2046494).


-   **[Create multiple configurations](https://www.servicenow.com/docs/access?context=create-multiple-child-configs&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    The product configurator displays the product configuration, including the bundle product options and characteristics. Child offerings that can have multiple configurations have information icons. Select the Information icon to view a message indicating that the offering can have multiple configurations.

    Navigate to the child offering in the product hierarchy, which displays the offering summary page.

-   **[Multiple configurations](https://www.servicenow.com/docs/access?context=multiple-child-offering-configurations&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    When agents add configurable products to new opportunities, quotes, and orders, they can create multiple configurations for a child offering. They navigate to a summary page for a selected child offering. From this page, they can do the following:

    -   Change the quantity of a child offering.
    -   Clone a child offering.
    -   Split a child offering that has a quantity greater than 1, to create child offering instances with different quantities.
    Each offering instance becomes a new line item that can be configured separately.

    In the following example, the Home Automation Bundle is a child offering that has a default quantity of 2 in the Quadplay Home Tech Bundle. An information icon displays next to each child offering that can have multiple configurations. The information icon, when selected, displays a message indicating that multiple configurations can be created for the child offering.

    When agents review a bundle offering in the product configurator, they identify the child offerings that can have multiple configurations. They navigate to the summary page for the appropriate child offering to create multiple configurations.

    In the offering summary page, a message indicates that the offering supports multiple configurations and the aggregated quantity of configurations that can be created. Agents can change the quantity of the child offering on this page.

    The More options icon displays next to the **Quantity**. Selecting the icon lists the options available for creating and managing multiple configurations.

    When the child offering configurations are created, each offering name reflects the child product offering name followed by an incremental number. For example, Home Automation Hub configurations are named Home Automation Hub 2, Home Automation Hub 3, and so on. Agents can then select the appropriate offering instance to configure it. If the agent changes the **Quantity** value, the Current Selection pane reflects the new quantity and associated pricing.

    The system also uses the cardinality rules to determine when certain configuration options \(**Split** and **Delete**\) should be enabled or turned off, based on the context. For example, if the minimum child offering quantity is 1 and a child offering has a quantity of 1, the system disables the **Delete** option in the More options menu.

-   **[Create multiple configurations](https://www.servicenow.com/docs/access?context=create-multiple-child-configs&version=yokohama&pubname=yokohama-order-management&ft:locale=en-US)**

    Change the quantity of a child offering that can have multiple configurations.

    Even when the multiple configurations feature is enabled, there are scenarios in which some configuration options might not be available. The system uses the default, minimum, and maximum quantity values from the product definition to determine valid configurations and then enables or disables the **Split** or **Delete** options for managing child offering configurations. For more information on validation, see .

    Navigate to the child offering in the product hierarchy, which displays the offering summary page.

-   **[Identity Type](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US)**

    Use the Identity Type define the correct identity type while creating a user. You can select **Human**, **Machine**, or **AI Agent** based on the user identity.

    The Web service access \(WSA\) only checkbox is automatically enabled for Machine identities and read-only for Human or AI Agent identities. You can mark Identity Type as Machine for creating WSA accounts.


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

AI Search

 PRB1823459

</td><td>

AI Search indexing Topic Path Translation doesn't work for non system user preference language

</td><td>

Session users assigned as 'guest' with the sys\_user\_preference file 'name=user.language' and 'value=some\_ non\_user\_session\_language' will have topic paths indexed in this language. The set language is not effective, which is the cause of incorrect translations.

</td><td>

1.  Ensure sys\_language has two active languages, **en**for English and **de** for Deutsch.
2.  Create an entry in the sys\_user\_preference table with the following values:
    -   system = true
    -   user = empty with language as 'de'
3.  Create the catalog item with translations for topic and topic path.

 Expected behavior: AI Search should index, and be able to search with the 'en' topic value.

 Actual behavior: AI Search indexes content with Deutsch translations for documents with both English and Deutsch languages, and the search for English will fail.

</td></tr><tr><td>

Condition Builder

 PRB1843987

</td><td>

Predicate builder Date Time filter is displaying JavaScript condition with quotation marks missing around the date parameter

</td><td>

Quotation marks should be surrounded by the condition '--&gt;', causing an issue with the query.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1881286

 [KB2074932](https://hi.service-now.com/kb_view.do?sysparm_article=KB2074932)

</td><td>

In Yokohama, recipients are no longer populated in Email Client and the Major Incident Recipient list when using JavaScript

</td><td>

The **Recipient** field should be populated with all recipients.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1834406

</td><td>

App installation deletes base instance sys\_complex\_object 'FDCollection'

</td><td>

Deleting the flow does not remove the sys\_complex\_object record from the source instance, but the app installation removed the record from the target instance. Sys\_complext\_object is not listed in the application file of the app, but appears in the payload of the sys\_hub\_flow record.

</td><td>

1.  Hop onto any base instance.
2.  Create a scoped app.
3.  Create a flow \(sys\_hub\_flow\) with some actions, such as log.
4.  Confirm the sys\_id is being included in the flow.
5.  Check the payload of the captured flow from sys\_update\_xml.
6.  Delete the flow from the list view of sys\_hub\_flow.
7.  Confirm the deletion is captured in sys\_metadata\_delete.
8.  Publish the scoped app to a repo or app store.
9.  Install the app from another instance from the app store.

 Notice that after the installation, the base instance sys\_complex\_object removes a sys\_id on the instance.

</td></tr><tr><td>

Related Lists

 PRB1887019

 [KB2122691](https://hi.service-now.com/kb_view.do?sysparm_article=KB2122691)

</td><td>

Users can't edit from a related list on a **Reference** field configured to be read-only in the dictionary

</td><td>

Users are no longer able to add existing related records via the 'Edit' function on a related list when the **Reference** field on the target table is marked as read-only. This behavior was previously functioning as expected. The issue has been verified in multiple relationships. Removing the 'read-only' attribute from the reference field restores expected functionality, confirming the change in behavior post-upgrade.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Reporting

 PRB1878029

 [KB2046103](https://hi.service-now.com/kb_view.do?sysparm_article=KB2046103)

</td><td>

A drill down report isn't working as expected with sorting added to the report

</td><td>

It's impacting the filter conditions by appending 'ORDERBY' at the beginning of the condition value to the last filter condition of the report.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1502280

 [KB0994649](https://hi.service-now.com/kb_view.do?sysparm_article=KB0994649)

</td><td>

The **File attachment** field does not appear on portal form page

</td><td>

The file attachment field **My file** doesn't appear on the form page of the incident record.

</td><td>

1.  Log in as an admin user.
2.  Open the form page of the incident record.

 Notice that the file attachment field **My file** doesn't appear on portal, but shows in native view.

</td></tr><tr><td>

System Import Sets

 PRB1850436

 [KB2115235](https://hi.service-now.com/kb_view.do?sysparm_article=KB2115235)

</td><td>

There's unexpected column creation when importing an Excel file with Japanese headers

</td><td>

When importing a file with Japanese headers, a new 'u\_xxx' column is created, even though the u\_email column already exists. This issue also occurs in Washington DC.

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

Access Control List \(ACL\) Rules

 PRB1891090

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1889718

</td><td>

Addition of Query ACLs in Access Control

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1889719

</td><td>

Addition of Query ACLs in Access Control

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1892867

</td><td>

Basic query range operation is broken

</td><td>

The basic query\_range operation on allowed fields is not working, and the user sees records not applied by the filter.

</td><td>

1.  Log in as an admin user.
2.  Navigate to any table, for example: sn\_customerservice\_case.
3.  Apply any query\_range filter on any field.

 Notice that the list shows all the records instead of the filtered.

</td></tr><tr><td>

Accounts Payable Invoice Processing

 PRB1889729

</td><td>

Addition of Query ACLs in Accounts Payable Invoice Processing

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1860591

</td><td>

Work notes are presented as encrypted text within the 'Activity' section of the ServiceNow Workspace when the encryption configuration is active

</td><td>

There's column-level encryption enabled and configured for the **work\_notes** field. When a user with a target role specified in the sys\_platform\_ encryption \_configuration record is posting worknotes in workspace, they are unable to see unencrypted text. Instead, they're seeing encrypted text. When the same user posts worknotes in the native view, the text isn't encrypted.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1882348

</td><td>

Avatars are not shown for AI agent updates in the Activity Stream

</td><td>

When agents update fields and post work notes to the Activity stream the agent avatars are not shown next ot their activities.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1890397

</td><td>

Two extras in the SQL count from the activity jelly template are seen in znowassiststable, causing a DMT SQL Spike

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Advanced Risk

 PRB1891325

</td><td>

Addition of Query ACLs in Advanced Risk

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1825616

</td><td>

Enhance the log statements for capturing the time it takes to route a work item in QueueRouter.java

</td><td>

There are no timing metrics or entries present in the log statements for the time taken to route a work item.

</td><td>

1.  Install Advanced Work Assignment on any Yokohama instance.
2.  Install Agent Chat.
3.  Create a chat and a work item.

 Observe the node logs.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1888546

</td><td>

Default service channel group routing limit of 25 is too low and noticeably affects throughput

</td><td>

An instance with the service channel group's routing limit set to the default of 25 experiences steady degradation of performance, with the backlog of un-routed cases growing into the 10000s and the time between cases and work items created growing to several minutes.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1886920

</td><td>

Interaction divider shows up as 'undefined' on Agent Workspace

</td><td>

Interaction divider shows up as 'undefined' on Agent Workspace after starting a conversation as a requester and ending it as an agent.

</td><td>

1.  Enable conversation history for Agent chat.
2.  Start a conversation as a requester and accept it as an agent.
3.  End the conversation.
4.  Start a new conversation and accept it as an agent.
5.  Scroll up to see the conversation history.

 Observe that the interaction divider shows up as 'undefined' on Agent Workspace.

</td></tr><tr><td>

Agile Development

 PRB1889742

</td><td>

Addition of Query ACLs in Agile Development

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1755617

</td><td>

The **DocID** field is being populated with the wrong sys\_id in the Search Signal Result Event table results

</td><td>

The sys\_search\_signal \_result\_event table is not capturing the correct sys\_id in the result AIS DocID for the Knowledge Genius search.

</td><td>

1.  Hop into a base instance.
2.  Navigate to the /ESC portal.
3.  Search for **Microsoft outlook issues**.
4.  Select the Genius Result.
5.  Search anything else so that the previous search session data is stored.
6.  Navigate to sys\_search\_signal \_result\_event table.

 Notice that the DocID is not populating, however XML has value since the sys\_id is not valid reference field not capturing any value

</td></tr><tr><td>

AI Search

 PRB1814576

</td><td>

The property glide.search. onboarding. popover.dismissed is not created for external users

</td><td>

The property glide.search.onboarding. popover.dismissed is not being created for external users with the role snc\_external in the sys\_user\_preference table. It is being created only for internal uses, such as agents with the snc\_internal role, but does not appear for a second time once it is cancelled.

</td><td>

1.  Log in to the instance.
2.  Open /CSM.
3.  Cancel the smarter chats modal that is displayed for the first time.
4.  Reload the page.

 Expected behavior: The smarter chats modal is not shown again once it is cancelled.

 Actual behavior: The smarter chats modal continue to appear for the type-ahead search widget.

</td></tr><tr><td>

AI Search

 PRB1850651

</td><td>

The 'All' tab is selected after a page is refreshed or when using the browser **Back** button

</td><td>

When performing a search in global, the The 'Knowledge' tab and the facet should be selected even after refreshing the page or using the **Back** button on the browser.

</td><td>

Scenario 1:

 1.  Open a Xanadu or Yokohama instance.
2.  Perform search in global for an incident or knowledge.
3.  Select the 'Knowledge' tab.
4.  Select any facet.
5.  Refresh the page.

 Expected behavior: The 'Knowledge' tab and the facet should be selected.

 Actual behavior: The facet is not selected after refreshing the page, and the 'All' tab is selected.

 Scenario 2:

 1.  Perform a search in global for an incident or knowledge.
2.  Select the 'Knowledge' tab.
3.  Select any facet.
4.  Select any search result.
5.  Use the **Back** button on the browser.

 Expected behavior: The 'Knowledge' tab and the facet should be selected.

 Actual behavior: The facet is not selected after using the **Back** button on the browser, and the 'All' tab is selected.

</td></tr><tr><td>

AI Search

 PRB1857215

</td><td>

There's a KB performance issue when there are a large number of user criteria assigned to a KB

</td><td>

The AI Search on ITSP has become slow after a Washington DC upgrade. AI Search is invoking Knowledge Management without any filters on the KB bases that are associated with the profile. Once the property 'glide. ais. disable\_kbb' is set to true, response times come back to the pre-upgrade times.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1880703

</td><td>

The 'Find what you need faster with Now Assist' pop-over is displayed even though FPE is not enabled

</td><td>

The pop-over is stuck to the homepage search bar. This should only be displayed when Full Page \(FPE\) is configured for a given portal and not for Dynamic Window.

</td><td>

1.  Navigate to **sys\_now\_assist\_ deployment\_ channel\_list.do**.
2.  Set the active 'false' for self-service dialog setting for customer support portal.
3.  Set it back 'active: true'.
4.  Log in to an instance.

 Observe that the pop-over is stuck to the homepage search bar.

</td></tr><tr><td>

AI Search

 PRB1885285

</td><td>

When Zing is the search engine for global search, data broker is still executed and pollutes the syslog

</td><td>

The underlying cause is that the composite data broker resource in the UI Builder app for the global search page is wired up to use the search term from the URL as an input, and so executes every time it changes after the initial search.

</td><td>

1.  On an instance with Next Experience enabled, turn off AI Search for global search by setting the 'glide.ui.polaris. ais\_ready' system property to false.
2.  In the navigator, type **rest batch**.
3.  Select the link to **Suppress REST Batching**.
4.  Select **Confirm**.
5.  Navigate back to the landing page.
6.  Refresh the page.
7.  Execute a search.
8.  Open the 'Network' tab and clear past transactions.
9.  Filter on 'exec'.
10. Change the search term in the search bar.
11. Note how many 'exec' calls have already happened, then hit **Enter**.

 Expected behavior: No additional exec call should happen after hitting **Enter.**

 Actual behavior: A new exec call happens, and if inspected, it's a call to the composite data broker. Additionally, if users then look in the syslog when the composite data broker is executing, it's polluting the syslog.

</td></tr><tr><td>

AI Search

 PRB1885594

</td><td>

AI Search attachment results aren't redirecting to the parent record

</td><td>

The issue is reproducible in Yokohama and Xanadu instances.

</td><td>

1.  Log in to an instance.
2.  Navigate to the ESC portal.
3.  Search for **Dental**.
4.  Select the doc result of the article.

 Notice that it's not redirected to the parent record. It's redirected to the sys\_attachment.do? sys\_id=undefined&amp; searchterm=detail.

</td></tr><tr><td>

AI Search

 PRB1886467

</td><td>

AI Search results match incorrect template

</td><td>

When a View Config condition uses a reference field for a table the user doesn't have access to, AIS returns the field, but with a value of '' \(empty string\).

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1887357

</td><td>

The AI Search experience doesn't work as expected with dynamic window enabled for a portal in New Assistant

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1887375

</td><td>

'OR' conditions aren't correctly evaluated in EVAM lite

</td><td>

In SearchResultTemplate Generator, there's logic to revert to legacy EVAM template engine if the condition is complex, but it doesn't currently catch 'OR' conditions.

</td><td>

1.  Set active=false to the Service Portal default view configuration.
2.  Search for 'IPV6' in Service Portal.
    -   Observe users get 1 result \(expected\).
3.  Modify the Service Portal 'Knowledge Search Results' view config to add 'knowledge\_base is Known Error'.
4.  Search for 'IPV6' in Service Portal.
    -   Observe users get 1 result \(expected\).
5.  Add an 'OR' condition to the 'Knowledge Search Results' view config for 'knowledge\_base is IT'.
6.  Search for 'IPV6' in Service Portal.

 Observe users no longer get the result \(not expected\).

</td></tr><tr><td>

AI Search

 PRB1888274

</td><td>

Enlarged loading sign before loading synth response on portal

</td><td>

When searching on an instance with the latest znowassist build and May store apps with DW enabled on portal, an enlarged loading sign appears before results load.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1895431

</td><td>

The first 'regular' search in Full Page Experience \(FPE\) doesn't log SEARCH\_EVENT, causing subsequent clicks not to be logged

</td><td>

This issue only happens on the first search.

</td><td>

1.  Open an AI Search-enabled instance with NA4S set up.
2.  Enable Full Page Experience in a portal.
3.  Open the portal.
4.  Enter something in the search bar.
5.  Select **Enter**.
6.  Open the Network tab.
7.  Filter for **event**.
8.  Switch from the chat to the search page.
9.  Execute the search.

 Expected behavior: A call to the Signals API to log a SEARCH\_EVENT occurs.

 Actual behavior: No call is made to log the search event.

</td></tr><tr><td>

AI Service - Glide Interfaces

 PRB1858539

</td><td>

Remove 'sys\_policy' as 'read-only' for records under sys\_one\_extend\_ definition\_config table

</td><td>

Records with the sys\_policy as read-only in the sys\_one\_extend\_ definition\_config\_list table are not allowed to update with the CDS sync job.

</td><td>

 

</td></tr><tr><td>

AI Service - Glide Interfaces

 PRB1889667

</td><td>

Addition of Query ACLs in AI Service - Glide Interfaces

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Analytics Export API

 PRB1847676

</td><td>

Metrics for the export using GCF

</td><td>

Metrics include source types for the export and number of exports by export method; exports with error codes and the number of exports by artifact type.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1875817

 [KB2055547](https://hi.service-now.com/kb_view.do?sysparm_article=KB2055547)

</td><td>

Script Assets aren't getting the latest content post upgrade, even though the plugin version has the ...latest/open FrameAPI setICContext method

</td><td>

OpenFrame is a hosted plugin and brings in UI scripts as part of it. On the upgrade of the plugin, the newer methods in the UI scripts aren't showing up even though it exists in that version.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1834952

</td><td>

Service Bridge Base plugin doesn't automatically upgrade when the Service Bridge for Providers plugin is upgraded

</td><td>

This issue occurs for users in a non-global domain or scope.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1872436

</td><td>

Access to a crypto module is set to 'reject' by default for some users

</td><td>

There's a 'Issue while uploading .store file: Unwrapping failed' error due to the crypto module being set to 'reject' by default.

</td><td>

 

</td></tr><tr><td>

Application Rationalization

 PRB1885498

</td><td>

Software asset management is a dependency for Technology Portfolio Management

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Assessments

 PRB1895396

</td><td>

Query range error seen on Surveys &amp; Assessments table even for privileged users

</td><td>

Query range errors are seen on the asmt\_assessable\_record table in Surveys &amp; Assessments.

</td><td>

1.  Create a user Assessment Admin.
2.  Assign the assessment\_admin role to the user.
3.  Impersonate as the user.
4.  Open the asmt\_assessable\_record.list page.
5.  Search for 'test' in the **Type** field search.

 Expected behavior: No error should be seen.

 Actual behavior: The 'Query range' error is seen even though the user has full access to the table.

</td></tr><tr><td>

Banner Frame

 PRB1878987

 [KB2091173](https://hi.service-now.com/kb_view.do?sysparm_article=KB2091173)

</td><td>

An HTML link for a page header caption \(glide.product. description\) is broken in a logo tooltip

</td><td>

On Yokohama, an HTML href attribute \(link reference\) included into a page header caption on the 'Basic Configuration UI16' page \(glide.product. description sys property\) doesn't render the href attribute.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1877635

</td><td>

The data in the capacity console does not populate properly when the capacity is counted in buckets

</td><td>

The data in the capacity console does not give the aggregated values for the demand channels.

</td><td>

1.  Log in as a user with elevated privileges.
2.  Create a capacity definition for the territory San Francisco in buckets and add two buckets or more.

 Notice that the data in the capacity console does not give the aggregated values for the demand channels.

</td></tr><tr><td>

Career Aspirations

 PRB1890426

</td><td>

Addition of Query ACLs in Career Aspirations

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Career Conversations

 PRB1889708

</td><td>

Addition of Query ACLs in Career Conversations

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1842199

</td><td>

RCA is generated when an HR lifecycle event is created

</td><td>

 

</td><td>

Create an HR lifecycle event case.

 Expected behavior: The RCA should not be generated.

 Actual behavior: The RCA with 'source\_copre: Human Resources: Lifecycle Events' and 'target\_scope: Human Resources: Core is generated'.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1874503

</td><td>

RCAs created during Email reply recommendation \[GenAI-2025-May\]

</td><td>

The error message, 'Wrong status for RCA privilege' occurs.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1874549

</td><td>

RCAs for KMGenAISimilar TaskSearchUtil are generated during multi-case KB generation

</td><td>

RCAs from KMGenAISimilar TaskSearchUtil to HR Core, Employee Relations, Legal Entities were added as requested RCAs in app-hr-gen-ai and will be allowed with the fix script. They previously did not target app-hr-genai, but did not get added to the apps that target them. This causes RCAs to be generated when we generate multi-case KB that are in a 'Requested' state. It would need to be allowed for multi-case KB generation.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1874746

</td><td>

AI Agent Invoker topic errors out when usecase is executed from Now Assist Panel \(NAP\) with a case open

</td><td>

Selecting the usecase in NAP with an open case throws an error in NAP and the logs.

</td><td>

1.  Log in as an admin user.
2.  Open an HR case for total rewards.
3.  Open NAP.
4.  Enter **Help me resolve this tuition reimbursement case**.
5.  Open the usecase **Resolve policy for tuition reimbursement**.

 Observe the error in NAP and in the logs, and that an execution plan is not created.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1876687

</td><td>

Notification Agent is unable to fetch and update HR case details

</td><td>

The event will be generated and the notification will not be created. In some cases where the notification is generated, 'Actions' will not perform the expected operation.

</td><td>

1.  Hop on the instance.
2.  Impersonate as admin.
3.  Navigate to **AI Agent Studio** &gt; **Testing**.
4.  Test the use case 'Notification AI Agent'.
5.  Test the task.

 Notice that the event will be generated, but the notification will not be created; for generated notifications, selecting **Actions** will not perform the expected operation.

</td></tr><tr><td>

Case Management

 PRB1889703

</td><td>

Addition of Query ACLs in Case Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

CIWF UI Component

 PRB1894610

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for portal\_knowledge\_ quick\_links widget

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Cloud Cost Management

 PRB1889713

</td><td>

Addition of Query ACLs in Cloud Cost Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Cloud Cost Management

 PRB1891183

</td><td>

Addition of Query ACLs in Cloud Cost Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Cloud Provisioning and Governance

 PRB1889715

</td><td>

Addition of Query ACLs in Cloud Provisioning and Governance

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

CMDB Workspace

 PRB1894924

 [KB2181389](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2181389)

</td><td>

Remove CUD access to sn\_cmdb\_editor roles on cmdb\_ci records

</td><td>

Users with the role 'sn\_cmdb\_editor' shouldn't be able to have access to the cmdb\_ci table and edit the records.

</td><td>

Impersonate as a user with the role sn\_cmdb\_editor.

 Expected behavior: The user shouldn't be able to perform CUD access to cmdb\_ci table.

 Actual behavior: In the CMDB Workspace or in UI16, users with the role are able to edit edit any cmdb\_ci data.

</td></tr><tr><td>

Communities

 PRB1889697

</td><td>

Addition of Query ACLs in Communities

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Communities

 PRB1889700

</td><td>

Addition of Query ACLs in Communities

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Compliance Case Management

 PRB1890990

</td><td>

Addition of Query ACLs in Compliance Case Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Configuration Compliance

 PRB1891686

</td><td>

Addition of Query ACLs in Configuration Compliance

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1868458

 [KB2015207](https://hi.service-now.com/kb_view.do?sysparm_article=KB2015207)

</td><td>

The empty domain path in the cmdb\_datasource \_last\_update table causes problems with IRE Reconciliation rules in a domain separated instance

</td><td>

Typically, when users insert or update a \(Configuration Item\) CI with a higher-priority data source defined in reconciliation rules, any other data source with a lower priority can't update the existing CI for the same attributes. However, attempted to replicate this behavior in a domain separated instance, the reconciliation rules weren't honored, and the lower-priority data source was able to update the CI. The domain path in the cmdb\_datasource \_last\_update table was empty, which causes the reconciliation rules to be ignored.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1872524

</td><td>

There's an exception RTE BeforeScript when trying to replace values corresponding to an item

</td><td>

When users try to replace item values, it causes an exception, like: 'ava.lang.RuntimeException: Before script unable to process records with error message: null'. IREScopedMapValues is expecting a map instead of an object. This needs to fixed for all other places where it is expecting java native objects.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1880595

</td><td>

Some script includes marked as sandbox use APIs not compatible with sandbox

</td><td>

The issue occurs in an instance using multisource with non-cmdb ci sys\_user, and has related properties set to true. Once the sys\_user exists in the multisource table, the table cleaner seeks to remove multisource deny classes. Non-cmdb based on the sys\_property gets the wrong value for the non-cmdb sys\_property from gs.getProperty\(\) when this script runs in the sandbox. This results in non-cmdb classes being removed from the multisource table even though properties are configured to have these classes in multisource.

</td><td>

1.  Set the glide.identification\_ engine.multisource\_ non\_cmdb\_ci\_enabled property to true.
2.  Navigate to the background script.
3.  Run a critical line from the script once with the sandbox not checked, and then with the sandbox checked.

 Observe gs.getProperty fails and returns the wrong result in the sandbox environment.

</td></tr><tr><td>

Contract Management

 PRB1889710

</td><td>

Addition of Query ACLs in Contract Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1859194

</td><td>

Identified shadow tables containing 'my\_row\_id' as a primary key \(PK\), causing PK mismatch with TableCloner

</td><td>

This issue was found in Xanadu instances. When a record is deleted from the table, an error can occur because it attempts to sync schema between the original table, and the shadow table can't alter the PK. This fix ensures the PK will be a 'sys\_id' on tables where 'sys\_id' is required.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1784019

</td><td>

Unoffload is not preserving the attachment upload date and time for the record

</td><td>

The unoffloaded time of the attachment becomes the attachment's new upload time.

</td><td>

1.  Create an incident with two image attachments, audits, journals
2.  Offload the record to S3.
3.  Unoffload the record to ar\_ table.
4.  Restore the record and related records to S3.
5.  Verify the attachment's uploaded time.

 Expected behavior: The attachment's original upload time is preserved in the record.

 Actual behavior: The unoffloaded time becomes the attachment's upload time.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1859906

</td><td>

Investigating failing archive restore operation

</td><td>

This issue occurs in a Xanadu instance.

</td><td>

Run archive restore on the parent record.

 Notice that only a subset of archive related records in the original archive run are restored, and the transaction is showing high SQL counts and times.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1885210

 [KB2127357](https://hi.service-now.com/kb_view.do?sysparm_article=KB2127357)

</td><td>

Randomize the monthly/yearly physical table stats aggregator/gatherer scheduled jobs

</td><td>

The monthly and yearly jobs are randomized over the day instead of in-between an hour.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1800843

</td><td>

Orbit class loader no longer uses ParallelWebapp ClassLoader

</td><td>

Orbit class loader no longer uses ParallelWebappClassLoader likely due to resource usage. This is noticeably one of the larger concurrency bottlenecks in glide. Glide runs with reloadable='false' flag to prevent reloading class files, therefore access to cache of class files don't need to synchronized.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1844798

</td><td>

Error message for unknown system variable 'sql\_generate\_ invisible\_primary\_key' warning received

</td><td>

This issue was observed in a Xanadu instance.

</td><td>

1.  Open a Xanadu instance.
2.  Created a new table from sys\_db\_object\_list.do.

 Observe the warning error message, 'Unknown system variable 'sql\_generate\_invisible\_primary\_key''.

</td></tr><tr><td>

Data Loss Prevention

 PRB1889727

</td><td>

Addition of Query ACLs in Data Loss Prevention

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Developer Sandboxes

 PRB1866844

</td><td>

Table configurations should be preserved during cloning

</td><td>

The table configurations are overwritten when they are cloned from another instance.

</td><td>

1.  Create some custom table configurations.
2.  Clone them over from another instance.

 Notice that the table configurations should be preserved, but they are overwritten.

</td></tr><tr><td>

Discovery

 PRB1657280

</td><td>

Inaccurate error logging for application patterns failed due to running processes that have bounced or stopped before pattern process detection executes

</td><td>

Commands using the PID and PORT from the ADM Probe will return null in the pattern failures. There's no log in the Discovery Log table of what occurred during process detection, and no indication in the failure message of the HD Log that the pattern failed due to the running process having bounced with a new PID or PORT.

</td><td>

1.  Ensure access to the target server running the Application instance.
2.  Run Discovery on the target server.
3.  Open the **Discovery Status** record.
4.  Wait for the Discovery to complete.
5.  Stop the service for the app running on the target server with **command sudo systemctl stop** after the ADM Probe ECC Queue Input is returned either.
6.  Open the ADM Probe ECC Queue Input record.
7.  Select the **Run Again** related link.
8.  Check the Discovery Status related list for Discovery Logs.
9.  Wait for the newest Pattern Log for the Application to return with an error for Failed Exploring Pattern.
10. Open the HD Log record.
11. Check the logging for why the Pattern Failed.
12. Check the Process Detection section before the Identification sections ran.

 Notice that commands executed that use the PID or the PORT discovered by the ADM Probe will return null, as they no longer exist on the target server, and there's no logging to the Discovery Log table of what occurred during Process Detection.

</td></tr><tr><td>

Dynamic Translation for Virtual Agent

 PRB1884635

</td><td>

Cached dynamic translations are not cleared when exclusion framework is disabled/enabled

</td><td>

Excluded terms in a new utterance are translated when the cache should have been cleared.

</td><td>

1.  Disable Exclusion Framework via the sn\_dt.dynamic\_framework. enable\_ exclusion\_framework system property.
2.  Translate something with excluded terms 'The words apple and \(dog\) should not be translated.'
3.  Enable Exclusion Framework via the sn\_dt.dynamic\_framework. enable\_ exclusion\_framework system property.
4.  Translate the same utterance with excluded terms.

 Expected behavior: Excluded terms in the utterance are not translated 'Las palabras apple y \(dog\) no deben traducirse.'

 Actual behavior: Excluded terms in the utterance are translated 'Las palabras manzana y \(perro\) no deben traducirse.'

</td></tr><tr><td>

Edge Encryption

 PRB1887439

</td><td>

In Yokohama, when a user goes through edge proxy with a home page that includes encoded characters such as %2f as a re-direction result after login, a 400 error occurs

</td><td>

When the user's default home page contains encoded characters, or is redirected to a URL with encoded characters, edge will throw the 400 error blocking access to the home page.

</td><td>

1.  Use an edge proxy in Yokohama.
2.  Add abel.tuter as a workspace\_admin and workspace\_user.
3.  Log in as abel.tuter through edge.
4.  Navigate to **Preferences**.
5.  Set the home page to **Default**.
6.  Log out.
7.  Log in as abel.tuter through edge again.

 Observe the http 400 error.

</td></tr><tr><td>

Employee Center

 PRB1809382

</td><td>

The hrm\_todos\_page list of tasks is incorrectly defined

</td><td>

To-do tasks from the hrm\_todos\_page list are not defined as list items, impacting the user's ability to navigate through the list.

</td><td>

1.  Navigate to **hrm\_todos\_page** for any user with to-do tasks assigned to them.
2.  Inspect each list item.

 Notice that they are not defined as list items.

</td></tr><tr><td>

Employee Center

 PRB1827503

</td><td>

Accessible names are overly verbose for links in the Employee Service Center \(ESC\) portal

</td><td>

Links that appear in the 'Recommended for you' and 'Support resources' sections of the Employee Center portal are overly verbose. The accessible name format for each link is 'Item x of y, Short description, Task type, Article text'. This issue impacts screen reader users.

</td><td>

1.  Navigate to **/ESC**.
2.  Select **Popular topics** &gt; **Email Accounts**.
3.  Turn on a screen reader, such as VoiceOver for Mac.
4.  Navigate through the cards in **Support resources** using the **Tab** key.

 Expected behavior: Each card has the following accessible name format announced, 'Card short description, Task type'.

 Actual behavior: Each card has the following accessible name format announced, 'Item x of y, Short description, Task type substantial article text'.

</td></tr><tr><td>

Employee Center

 PRB1831309

</td><td>

Email returned from the HR Auto resolution test is missing some fields

</td><td>

Email script used in sysevent\_email\_template \(sn\_hr\_core\_ case.ess.general\) is not present in Washington DC and Xanadu.

</td><td>

 

</td></tr><tr><td>

Employee Center

 PRB1862534

</td><td>

Keyboard navigation in the topic page is not working as expected for accessibility

</td><td>

Using keyboard actions to focus on the **Show more** button doesn't allow the user to move to the next element.

</td><td>

1.  Log in as an admin user.
2.  Navigate to **All**.
3.  Select any topic page.
4.  Use the keyboard action.
5.  Traverse the page until the **Show more** button appears.
6.  Use **Enter** to select the **Show more** button.

 Observe that the focus is still being present on the **Show more** button instead of the next element.

</td></tr><tr><td>

Employee Document Management

 PRB1877142

</td><td>

In Employee Document Management, UI actions cause performance impact to rendering search documents

</td><td>

In Employee Document Management, UI actions cause performance impact to rendering search documents or any list load on the sn\_hr\_ef\_ employee\_document table. The following UI actions are contributing to response times: Authorize, Reject, Authorize All, and Reject All. The number of records on the sn\_hr\_ef\_ employee\_document is ~2.7 million.

</td><td>

1.  Ensure that Employee Document Management is set up on an instance and the number of records in sn\_hr\_ef\_ employee\_document is ~2 million.
2.  Select the search documents module from the filter navigator.

 Notice that the page load times exceed 200 ms and often time out. Most of the time is spent on rendering the UI actions listed above \(~ 50 seconds each\).

</td></tr><tr><td>

Employee Document Management

 PRB1888195

</td><td>

An RCA is generated in a 'Requested' state

</td><td>

An RCA is created in the requested state for sys\_attachment.file\_ name.

</td><td>

1.  Provision an instance with Employee Document Management, HR Agent Workspace installed.
2.  Create a new use, add the ef.admin role, and impersonate.
3.  Navigate to **Create new document** and create a new doc with an attachment successfully.
4.  Navigate to **HR Agent Workspace** &gt; **Employee documents** &gt; **All**.
5.  Open the document created.
6.  Update the file name and save the record.
7.  As admin, navigate to RCA table.

 Observe that an RCA is created in the requested state for sys\_attachment.file\_ name.

</td></tr><tr><td>

ESG Management

 PRB1889690

</td><td>

Addition of Query ACLs in ESG Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Finance Common Architecture

 PRB1891405

</td><td>

Addition of Query ACLs in Finance Common Architecture

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1857200

</td><td>

Flow errors out when a node is notified to shut down

</td><td>

When Node 1 is shut down, the flow should be able to execute in Node 2.

</td><td>

1.  Prepare a 2 node instance.
2.  Activate the plugin **com.glide.hub.flow\_testing**.
3.  Load the UpdateSet.
4.  Navigate to **Scripts** in Node 1.
5.  Background run the script to notify Node 1 to shut down.
6.  Confirm the run.
7.  Navigate to **REST API Explore**.
8.  Select **Flow Testing API** &gt; **Start Flow Quick \(POST\)**.
9.  Trigger the flow by entering the Request Body.

 Expected behavior: The flow should be executed on Node 2 without error.

 Actual behavior: The flow errors out.

</td></tr><tr><td>

Flow Engine

 PRB1888071

 [KB2153671](https://hi.service-now.com/kb_view.do?sysparm_article=KB2153671)

</td><td>

Deserialization issue with 'Make a decision'

</td><td>

When upgrading from a Washington DC to Yokohama instance, flow executions created with 'Decision' in both families don't resume and result in an error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1889723

</td><td>

Addition of Query ACLs in Flow Engine

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Form Templates

 PRB1848777

</td><td>

The state of the menu items 'Toggle Template Bar and Toggle annotations on/off' is not easily discernible

</td><td>

This issue impacts the following platforms: Chrome, JAWS, Edge chromium, NVDA, Safari, VoiceOver. This also impacts Windows OS and Mac OS.

</td><td>

1.  Open any base instance.
2.  Navigate to **All** &gt; **Incident**.
3.  Open any incident.
4.  Navigate to **More options**.
5.  Toggle the **Template Bar**.
6.  Toggle the **Annotations** button on or off.
7.  Verify the screen reader announcement.

 Expected behavior: The name should be 'Show/Hide Template Bar and Show/Hide annotations'.

 Actual behavior: The state of the menu items 'Toggle Template Bar and Toggle annotations on/off' is not easily discernible, and users using screen readers or magnifiers cannot see the state of the application.

</td></tr><tr><td>

GRC: Advanced Audit

 PRB1890961

</td><td>

Addition of Query ACLs in GRC: Advanced Audit

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Advanced Core

 PRB1890960

</td><td>

Addition of Query ACLs in GRC: Advanced Core

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Continuous Authorization and Monitoring

 PRB1890964

</td><td>

Addition of Query ACLs in GRC: Continuous Authorization and Monitoring

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Metrics

 PRB1891392

</td><td>

Addition of Query ACLs in GRC: Metrics

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Operational Resillience

 PRB1889673

</td><td>

Addition of Query ACLs in GRC: Operational Resillience

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Privacy Management

 PRB1890889

</td><td>

Addition of Query ACLs in GRC: Privacy Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Profiles

 PRB1889683

</td><td>

Addition of Query ACLs in GRC: Profiles

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

 PRB1889704

</td><td>

Addition of Query ACLs in Healthcare and Life Sciences Service Management Core

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1820752

</td><td>

The hermes\_cluster\_ config only has delete audits

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1879073

</td><td>

Recurrent diagnostics fix improvement for external ports check

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Horizon Checkbox Component

 PRB1820170

</td><td>

The checkbox tick mark is not properly visible when hovering over the selected file

</td><td>

The tick in the checkbox is not properly visible in both day mode and night mode when hovering over a selected file.

</td><td>

1.  Add a checkbox to the workspace page.
2.  Hover over the checkbox label.

 Notice that the tick mark on the checkbox is not properly visible, especially in dark theme.

</td></tr><tr><td>

Horizon Component Library

 PRB1881027

</td><td>

Polaris theme variable is not available in Yokohama

</td><td>

The correct banner isn't shown on Yokohama.

</td><td>

1.  Install Agent workspace for HR case.
2.  Open the HR Agent workspace home page.

 Notice that the correct banner on Yokohama isn't shown.

</td></tr><tr><td>

HR Service Delivery

 PRB1889709

</td><td>

Addition of Query ACLs in HR Service Delivery

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Identity

 PRB1889721

</td><td>

Addition of Query ACLs in Identity

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1885869

</td><td>

Legacy IDR jobs flood the logs with error messages when they can't reach Kafka via bootstrap

</td><td>

There are some scheduled jobs that are created when legacy IDR is installed and are scheduled to run frequently by design. When the cluster isn't reachable, these scheduled jobs write errors to the log each time, which happens once every few seconds. When IDR v2 is used \(all new sets created in Washington and later\), there's a new set of scheduled jobs that are used and continue to work when the infrastructure for legacy IDR is turned off. However, the jobs intended for legacy IDR aren't automatically turned off when all sets have been migrated to v2.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1834445

</td><td>

GCF Data Egress recorder should support 0 byte inputs

</td><td>

GCFDataEgressRecorder will throw an error with an Invalid event value when an event with 0 bytes is recorded, creating an error in the log.

</td><td>

Post to the instance on an endpoint

 Notice that this will return an 204 \(no content\) response a zero byte response.

</td></tr><tr><td>

Integration Hub

 PRB1857020

</td><td>

Remote Process Synch \(RPS\) outbound job can go into loop if there is an error parsing XML

</td><td>

There should be a message in the log for the Outbound Queue Job for the state table with the state error.

</td><td>

1.  Set up RPS with outbound on incident that captures a short\_description.
2.  Create an incident that meets the capture criteria with the short\_description.
3.  Set the contents of the file so that 'invlid\_short\_ description.txt' is inside the attached zip file.

 Notice that the entry is not processing and there is no error record in the Outbound Queue.

</td></tr><tr><td>

Integration Hub

 PRB1867967

</td><td>

Connection URL is populating incorrectly for JSON import

</td><td>

This occurs with Spoke Generator version 4.0.3

</td><td>

1.  Navigate to Flow Designer.
2.  Open any spoke from integrations.
3.  Navigate to **Actions** &gt; **Create Action** &gt; **Postman Collection** &gt; **Import new** &gt; **Import from JSON manually**.
4.  Import the JSON file.
5.  Notice how the postman collection is populated.
6.  Select **Create New** for Connections and Credential Alias.
7.  Give any name.
8.  Create it.
9.  Notice how the Connection URL is populated.
10. Fill in any API key.
11. Select **Submit**.
12. Select **Generate operations**.
13. Ensure published and draft actions are able to be created.

</td></tr><tr><td>

Internationalization Features

 PRB1888560

</td><td>

API to check whether a translation is available in sys\_ui\_message

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1847472

</td><td>

Fix the matching of the Bagheera configuration database URL with the cached database URL

</td><td>

App nodes compete in a vicious loop to update this database property to match with their mismatched cached property, which is affecting the instance's performance.

</td><td>

1.  Run AHA 3.0 on any instance utilizing Bagheera.
2.  Run AHA Transfer/ Failover.
3.  Notice the logs on the nodes after a successful transfer or failover.

 Expected behavior: The glide.db.url from cache should match with the file property glide.db.url.

 Actual behavior: The cached GlideProperties database URL does not match the file property glide.db.url.

</td></tr><tr><td>

Knowledge Article Templates

 PRB1855083

</td><td>

Toolbar options and plugins for the TinyMCE editor are missing in the dictionary attribute for the Knowledge **Article body** field

</td><td>

Options like A11yChecker, Clear formatting, Anchor, and others are missing.

</td><td>

1.  Create or open any knowledge record.
2.  Notice that some of the TinyMCE toolbar options are missing in **Article body** field.

</td></tr><tr><td>

Knowledge Article Templates

 PRB1863956

</td><td>

Name and role is not defined properly for the Latest Version under Knowledge Article

</td><td>

The **Latest Version** should be defined and announced as a button by the screen reader.

</td><td>

1.  Launch any base instance.
2.  Navigate to **All**.
3.  Enter **kb\_knowledge\_list.do**.
4.  Select any record from the knowledge list containing multiple versions, for example 'KB0000108'.
5.  Navigate to **Related links** &gt; **View article**.
6.  Navigate to Latest Version link for the KB article.
7.  Interact with the Latest Version link.
8.  Observe the issue.

 Expected behavior: The name of the control should be defined and announced by screen reader, and the **Latest Version** KB should be defined as a button.

 Actual behavior: Screen reader doesn't announce the name of the control and only announces it as link, and expanded links are not announced as opened by the screen reader.

</td></tr><tr><td>

Knowledge Management

 PRB1864356

</td><td>

When displaying a KB article, the breadcrumb must contain the article title

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Open the KB portal.
3.  Open any article.

 Observe that the breadcrumb doesn't have the name of the article.

</td></tr><tr><td>

Lifecycle Events

 PRB1830703

</td><td>

Base instance account notification workflow issue for Onboarding Lifecycle event

</td><td>

Account notifications are sent only occasionally for New Hire cases, when they should always be sent to the user when triggered.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1848766

</td><td>

Keyboard focus does not move to the 'Tag details' dialog after opening

</td><td>

This issue impacts the following platforms: Chrome, JAWS, Edge chromium, NVDA, Safari, VoiceOver. This also impacts Windows OS and Mac OS.

</td><td>

1.  Open a base instance.
2.  Navigate to the **All** &gt; **Incident**.
3.  Open any incident list.
4.  Select **Edit table data**.
5.  Navigate to any cells.
6.  Use **shift + space** to open the menu.
7.  Select **Assign tag** &gt; **New tag**.
8.  Verify the keyboard focus.

 Expected behavior: Keyboard focus should move to the 'Tag details' dialog after opening.

 Actual behavior: Keyboard focus does not move to the 'Tag details' dialog after opening and remains in the background after the last element focus comes.

</td></tr><tr><td>

List Administration

 PRB1894601

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for Listcount

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1894614

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for GlideAggregate

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1894616

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for Related Lists

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1863944

</td><td>

Instructions are not provided for the resizable panes divider handle

</td><td>

The screen reader doesn't provide an announcement with instructions for the resizable panes divider handle.

</td><td>

1.  Launch any base instance.
2.  Navigate to **All** &gt; **Service Operation Workspace**.
3.  Navigate to **List** &gt; **Resizable panes divider handle**.
4.  Observe the announcement of screen reader.
5.  Verify whether the instructions are provided or not.

 Expected behavior: Instructions should be provided, like left and right arrows keys, to resize the divider handle.

 Actual behavior: Instructions are not provided for the Resizable panes divider handle.

</td></tr><tr><td>

List Views

 PRB1854405

</td><td>

The Xanadu Date Picker Calendar pop-up appears below the field, making it difficult to select other dates

</td><td>

The Xanadu Date Picker Calendar opens on the below field and isn't letting users select other dates when they add a variable editor on the form configuration.

</td><td>

1.  Navigate to a Xanadu instance.
2.  Navigate to incident.LIST.
3.  Add a variable section.
4.  Add an incident variable editor to the form.
5.  Navigate to the TASK SLA related list.
6.  Select the **Start time** field.

 Notice that the calendar pop-up appears below the field, making it difficult to select other dates. The date picker should open above the field.

</td></tr><tr><td>

List Views

 PRB1865826

</td><td>

Multi-select not working in the Certification Review page for data certification

</td><td>

This issue occurs in Washington DC, Xanadu, and Yokohama. In the 'Review Completed' and 'Review not completed' lists, selecting the **Select all** button and the message **Select all x item from the list** from one list selects all the records in the other list as well.

</td><td>

1.  Select **All x item** from the list not working properly on Xanadu and Yokohama.
2.  Open any certification task in Yokohama.
3.  Certify or fail some records.
4.  Navigate to the 'Review Completed' tab.
5.  **Check** the **Select all** box.
6.  Select the 'Select all X item from the list' message.
7.  Navigate to the 'Review not completed' tab.
8.  Notice all records from the review that are not completed are also selected.
9.  Observe that the count is updated to all the records.

 Expected behavior: Only the selected records in should be in the 'Review completed' tab.

 Actual behavior: Notice that records from the 'Review not completed' tab are also in the 'Review completed' tab.

</td></tr><tr><td>

Major Incident Management

 PRB1757151

</td><td>

Base instance list control on the Affected CI related list throws an error in the syslog when incidents are accessed on the mobile app

</td><td>

An error is thrown with the following warning when any user opens an incident record while accessing the instance through the browser on a mobile device.

</td><td>

1.  Open an instance.
2.  Log in to the instance.
3.  Navigate to any available incident.
4.  Switch to desktop view.
5.  Navigate to **syslog.list**.

 Observe the error in the logs.

</td></tr><tr><td>

MID Server

 PRB1842102

</td><td>

Session mismatch on MID server when an agent experiences VPN issues

</td><td>

Host data collection also fails with MID logs showing, 'Failed to send check instance check-discovery-basic due to closed communication session'.

</td><td>

1.  Use MID in the ITOM lab.
2.  Connect the agent to MID in ITOM lab.
3.  Disconnect the agent by disconnecting from the ITOM VPN.
4.  Reconnect the agent by reconnecting to ITOM VPN.
5.  Check the MID logs.

 Expected behavior: Notice the MID logs with the agent ID mapped to the message, 'Agent registered for communication', and the agent websocket session should be different than it was before it disconnected.

 Actual behavior: Notice the MID logs with the agent ID mapped to the message, 'Agent registered for communication', and the agent websocket session is the same according to MID logs.

</td></tr><tr><td>

Mobile Platform

 PRB1840495

</td><td>

List screen presents error and doesn't present items in offline mode due to a specific input form screen configuration

</td><td>

In the case where the parameter screen is pre-fetched, the list screen shows an error and does not present items. In the case where the parameter screen is on-demand, the parameter action does not open in offline mode.

</td><td>

1.  Create a list screen.
2.  Create a swipe action such as 'fnc\_ai\_Y\_enhancements \_multi\_page'.
3.  Create an action item that uses the parameter screen such as 'ai\_Y\_enhancements \_multi\_page'.
4.  Create an action of type attachments for the parameter screen such as 'attach4str'.
5.  Add data binding to the action.
6.  See the 'attach4str' action.
7.  Configure the list screen and all components to be available offline.
8.  Check the list screen in offline mode.

 Notice that when the parameter screen is pre-fetched, the list screen shows an error and does not present the items.

</td></tr><tr><td>

Mobile Platform

 PRB1844072

</td><td>

Error when executing action in Offline for Android and iOS

</td><td>

An error occurs indicating the WBA failed.

</td><td>

1.  Download the offline cache.
2.  Turn on Offline when in offline mode.
3.  Select the **CTT-Test** icon.
4.  Select incidents ending with '0004'.
5.  Select the **CTT Scripted** footer button in the form screen.
6.  Skip all pages.
7.  Select **Submit**.

 Notice the error banner shows, indicating the WBA failed.

</td></tr><tr><td>

Mobile Platform

 PRB1844650

</td><td>

Button action that uses a scripted screen causes an error in the loading an item section

</td><td>

An error occurs and the item section is not displayed.

</td><td>

1.  Create an item section that links to the list screen.
2.  Navigate to the list item configuration for the list screen.
3.  Ensure that there is no Embedded Screen configuration.
4.  Create a new button instance with the 'list item' location.
5.  Create a button that uses the scripted screen for the button instance.
6.  Open the Android mobile application.
7.  Open ALP with the item section configured.

 Expected behavior: The item section should be displayed, and the scripted screen should open when the item is selected.

 Actual behavior: The error, 'Could not load the applet launcher' is displayed and the item section is not displayed.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1690651

</td><td>

Zing Exact Match search on workspaces intermittently navigates to an incorrect URL in Next Experience

</td><td>

Zing Exact Match search opens the record in record view instead of kb\_view.

</td><td>

1.  Log in to an instance in incognito mode.
2.  Ensure Next Experience is enabled.
3.  Ensure global and workspace searches are using zing.
4.  Select **Service Operations Workspace** in the search context.
5.  Perform an exact match search for 'KB0000001'.
6.  Notice that it should open the record in kb\_view.
7.  Wait for 5 to 10 minutes.
8.  Repeat the steps.

 Observe that the record opens in record view.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1871341

</td><td>

Text is truncated in the 'leave page' pop-up in Next Experience after upgrading to Yokohama

</td><td>

The issue isn't happening on previous releases like Washington DC or Xanadu. The issue is also not happening with UI16 on the Yokohama release.

</td><td>

1.  Turn on Next Experience.
2.  Access the 'Basic Configuration UI16' module.
3.  Modify the value of 'Browser tab title' to a longer value.
4.  Select **Save**.
5.  Re-log in the instance to make sure the change take effect.
6.  Select **Create New** under the 'Incident' or 'Knowledge' module to create a record.
7.  Make some changes on the form.
8.  Select the **Back** arrow on the left-top of the form.

 Expected behavior: The 'Leave page' pop-up appears, which displays a completed message.

 Actual behavior: The 'Leave page' pop-up appears, but it displays a truncated message.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1875808

</td><td>

The desktop notification banner doesn't display in Windows when multiple tabs are open

</td><td>

It displays the notification in the Notification Center but it doesn't display the banner.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1880894

</td><td>

On-call scheduling is randomly skipping one person for every rotation cycle

</td><td>

.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1886730

</td><td>

The 'On-call Who' API intermittently isn't returning users

</td><td>

 

</td><td>

1.  Create a one hour shift daily.
2.  Change the user session timezone to 'America/Los\_angeles'.
3.  Open the calendar so the roster payload cache is built.
4.  Change the user session timezone to 'Asia/Kolkata'.
5.  Run OnCallRotation .getEscalationPlan during a time when the on-call user is present.

 Expected behavior: The API returns the primary user.

 Actual behavior: It returns empty.

</td></tr><tr><td>

OneExtend

 PRB1884836

</td><td>

The user only observes regular search results for bot to bot in synthesis, sync mode

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Opportunity Management

 PRB1889707

</td><td>

Addition of Query ACLs in Opportunity Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Outsourced Customer Service

 PRB1889693

</td><td>

Addition of Query ACLs in Outsourced Customer Service

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1889720

</td><td>

Addition of Query ACLs in Analytics Hub

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1890020

</td><td>

Addition of Query ACLs in Analytics Hub

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Personal Data Rights

 PRB1890994

</td><td>

Addition of Query ACLs in Personal Data Rights

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1865209

</td><td>

**View dashboard** automigrates dashboards that should not be migrated when unified is 'true'

</td><td>

This behavior can be seen for Yokohama and previous families.

</td><td>

1.  Mark dashboard on pa\_dashboard list as **Do not bulk migrate**.
2.  Run bulk migration.
3.  Activate it.
4.  Return to the dashboard in pa\_dashboard.
5.  Select **View Dashboard**.

 Expected behavior: The dashboard should not be migrated since it is blocked from migration.

 Actual behavior: The dashboard is auto-migrated.

</td></tr><tr><td>

Playbook Experience Core

 PRB1841873

</td><td>

Slowness within Playbook activities when there are a large number of stages and activities

</td><td>

This issue within the Playbook activities occurs when large number of stages and activities, such as 100 to 200 activities, have condition to run on the lanes and activities.

</td><td>

1.  Create a playbook process with a large number of stages and activities.
2.  Attempt to progress through the playbook in the workspace or playbook preview.

 Notice the slowness increases as the number of stages and activities grow.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1861646

</td><td>

Questionnaire order is not synchronized in update\_set or persisted when duplicating a Playbook

</td><td>

The order of questions in the Questionnaire Activity should persist in a duplicated playbook.

</td><td>

1.  Create a new Playbook with a Questionnaire Activity.
2.  Add three questions.
3.  Select **Save**.
4.  Duplicate the playbook.

 Expected behavior: The order of questions persists in the duplicated playbook.

 Actual behavior: The order of questions is not persisted in the duplicated playbook.

</td></tr><tr><td>

Policy and Compliance Management

 PRB1889692

</td><td>

Addition of Query ACLs in Policy and Compliance Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Portfolio Management

 PRB1889736

</td><td>

Addition of Query ACLs in Portfolio Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Portfolio Management

 PRB1889740

</td><td>

Addition of Query ACLs in Portfolio Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1873662

</td><td>

Add support for top number of classes, minute records per class, and removing ServiceNow Machine Learning others as advanced parameters in Classification solution

</td><td>

The ability to apply these advanced parameters.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1879961

</td><td>

Two emails are sent for clustering when triggered from Process Mining

</td><td>

When RCA/Clustering is triggered from the process mining workspace, two emails are sent when only one email should be sent. Since the RCA or Clustering feature internally uses the show records, two ml\_solutions are created, and the system identifies both of them as separate entities, causing it to send two emails.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1885063

</td><td>

Add model parameters from model configuration as advanced parameters in classification solution

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1885952

</td><td>

Incorrect use of current.update\(\) in a base instance business rule

</td><td>

The script run by the BR includes a current.update\(\) call without setworkflow call to disable other BRs.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1890514

</td><td>

A 'Feature Importance' tab displays for java classifications

</td><td>

 

</td><td>

1.  Train a classification solution with glide.platform\_ml. api.enable\_ workflow\_classification as 'false'.
2.  Observe that the 'Feature Importance' tab appears even though it's not trained with explainability.

 Expected behavior: The 'Feature Importance' tab shouldn't appear.

 Actual behavior: The 'Feature Importance' tab is appearing.

</td></tr><tr><td>

Process Mining

 PRB1870032

</td><td>

Uppercase and lowercase sys\_ids for the same record break mining

</td><td>

A script changes the document ID in sys\_audit for records so that some document ID values are uppercase and lowercase.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1889675

</td><td>

Addition of Query ACLs in Process Mining

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1889701

</td><td>

Work order tasks are assigned from the agent schedule start time based on the agent's timezone.

</td><td>

Results should be in UTC relative to the cmn\_schedule timezone, even if the user's timezone is different.

</td><td>

 

</td></tr><tr><td>

Security Customer Actions

 PRB1873948

</td><td>

Steps can't be re-opened for a completed action due to Playbook archiving

</td><td>

The user is not able to re-open the step to continue working on it again.

</td><td>

1.  Open a Xanadu instance.
2.  Navigate to **Security Center** &gt; **Customer Actions \(Critical Updates\)**.
3.  Complete the **Enable 3DES deprecation for Password2 Fields** action.
4.  Wait 14 days on the instance to allow for playbook archiving.
5.  Navigate to the completed **Enable 3DES deprecation for Password2 Fields** action.
6.  Navigate to **Steps**.
7.  Select one of the steps.

 Expected behavior: The user is able to re-open a step by using the **Restart** button to proceed working on it again.

 Actual behavior: The user is not able to re-open the step.

</td></tr><tr><td>

Server-side scripts

 PRB1856234

</td><td>

Fetch in non-module scopes look for classes improperly

</td><td>

An error is thrown about abort controller.

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB1866781

</td><td>

When calling the CatalogItem.get API with the Catalog Item GlideRecord for a CRP record, the type on the catalog item cached object will be sc\_cat\_item\_producer

</td><td>

The type on the catalog item cached object will be sc\_cat\_item\_producer when it should be sc\_cat\_item\_composite \_producer.

</td><td>

1.  Take a sys\_id of base instance record producer.
2.  Flush the system cache.
3.  Query the sc\_cat\_item table with the CRP sys\_i from background scripts.
4.  Call the CatalogItem.get API with the glideRecord.
5.  Call the API GlideappCatalogItem.get\(\).getType\(\) from background scripts.

 Expected behavior: The type should be sc\_cat\_item\_composite\_producer.

 Actual behavior: The type will be sc\_cat\_item\_producer because of the issue, and the catalog builder subsequently doesn't work on the node where the cache is corrupted.

</td></tr><tr><td>

Service Creator

 PRB1847033

</td><td>

A user with the catalog\_editor role is able to access all records in catalog\_category\_ request table

</td><td>

In a Yokohama instance, the data filter record for the table catalog\_category\_request is not appearing automatically. It appears only after repairing the Service Creator plugin.

</td><td>

1.  Create any record in catalog\_category\_request table.
2.  Attempt to access the table records with a user with a catalog\_editor role.

 Expected behavior: The user is unable to access the records.

 Actual behavior: The user is able to access the records.

</td></tr><tr><td>

ServiceNow IDE \(Family Release\)

 PRB1878154

</td><td>

A sync notification appears after deploying an app

</td><td>

The sync mechanism should detect changes from sys\_update\_xml by default.

</td><td>

1.  Create an app.
2.  Create a Table\(\{\}\) using Fluent in index.now.ts.
3.  Deploy the app.

 Expected behavior: Changes made by Fluent shouldn't trigger a sync.

 Actual behavior: A sync notification appears immediately after deploying even though it was the user's changes that were deployed.

</td></tr><tr><td>

Service Portal Core Widgets

 PRB1862176

</td><td>

Service Portal fails to a submit catalog item when a required HTML variable is empty and re-submitted with a filled value

</td><td>

After selecting **Submit** on a Service Catalog Item widget when the required HTML variable is empty, it rejects the submission as expected. However, filling the HTML variable after the submission is rejected and still detects the HTML variable as not filled. Because of this, users are only able to submit catalog items from Service Portal when the required HTMl variables are filled properly before submission.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1861832

</td><td>

Accessibility issues on Business Portal Home Page

</td><td>

Accessibility issues regarding the **Language selection** field for users.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1884533

</td><td>

Dynamic window pinned mode causes layout issues on a catalog item

</td><td>

The catalog item overlaps with dynamic chat window.

</td><td>

1.  Navigate to \{instance\}/sp with dynamic window enabled.
2.  Navigate to the catalog page and select a catalog item.
3.  Open a dynamic window, pin it and increase the window size to half of the page.

 Notice that the catalog item overlaps with dynamic chat window.

</td></tr><tr><td>

Service Portal

 PRB1894604

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for widget-data-table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1893827

</td><td>

Revert true-up for SFS for Yokohama Patch 4

</td><td>

There should be no version true-up for SFS in Yokohama Patch 4.

</td><td>

 

</td></tr><tr><td>

Sidebar

 PRB1877077

</td><td>

Dynamic Expert Finder is not working in Yokohama instances

</td><td>

There are test failures in the Dynamic Expert Finder tests. The participants list is not loading.

</td><td>

 

</td></tr><tr><td>

Smart Assessment Engine

 PRB1890890

</td><td>

Addition of Query ACLs in Smart Assessment Engine

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Software asset analytics

 PRB1860159

</td><td>

There's an issue with the 'potential savings indicator' filter for reclamation candidates

</td><td>

By default, all new reclamations have a user subscription mapped to the 'Subscription to reclaim' M2M table. Where there's a downgrade or consolidate use case, the product and user subscription isn't stamped. Where there's a low usage use case, the product and user subscription is stamped. Due to this, some reclamation candidates are missed by the potential savings calculation.

</td><td>

1.  Create M365 integration.
2.  Run the 'Usage' job.
3.  Create entitlements.
4.  Run the 'Reclamation' job for M365.
5.  Check the user subscription and product for downgrade or consolidate case.
6.  Run the Platform Analytics indicator job 'Subscription Daily Job'.

 Some potential savings for these candidates are missing on the 'Software Asset Analytics' page.

</td></tr><tr><td>

Software Asset Management

 PRB1874410

</td><td>

CrowdStrike new license metrics are not added in SampConstants file

</td><td>

The new license metrics sys IDs are not present in SampConstants.SUPPORTED \_LICENSE\_METRICS.

</td><td>

1.  Navigate to the SampConstants Script include.
2.  Check SampConstants.SUPPORTED \_LICENSE\_METRICS.

 Notice that the new license metrics sys IDs are not present.

</td></tr><tr><td>

Software Asset Management Publisher Pack for Oracle

 PRB1876860

</td><td>

Download Oracle Glas Report changes to add new fields to VM report and Hardware report

</td><td>

This is an enhancement to uptake new requirements on Oracle Audit download reports.

</td><td>

 

</td></tr><tr><td>

Software Asset Normalization

 PRB1842256

</td><td>

The values for the 'Condition' column of the pattern rules samp\_pattern\_ normalization\_rule are not flowing to instances

</td><td>

The 'Condition' column values for samp\_pattern\_ normalization\_rule are not flowing to customer instances. These values are present on the instance, but are missing in the catalog item.

</td><td>

 

</td></tr><tr><td>

Store IRM Privacy Case Management

 PRB1890991

</td><td>

Addition of Query ACLs in Store IRM Privacy Case Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Supplier Collaboration Portal

 PRB1889728

</td><td>

Addition of Query ACLs in Supplier Collaboration Portal

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB1852694

</td><td>

Events processing is malfunctioning due to cache updates not being generated or propagated

</td><td>

The sys\_cache\_flush isn't showing entries for the updated entries of sys\_processing \_framework\_job, and other node caches are also not reflecting the latest changes.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB1874642

</td><td>

Rhino context re-used for multiple events can lead to inconsistent results

</td><td>

Reusing Rhino contexts can break code that uses lazy initialization of global variables.

</td><td>

 

</td></tr><tr><td>

System Export Sets

 PRB1872251

 [KB2022620](https://hi.service-now.com/kb_view.do?sysparm_article=KB2022620)

</td><td>

In Log Export Service, errors such as 'Producer failed to send message asynchronously' are regular in the instance

</td><td>

Some users experience this error more than 500 times in 7 days '\(ProduceMessage \{f Partition=Partition\{ fTopic='HermesTopic \{ fName='sn\_logstoanalytics. 6b559dc83becda10c97ba', fInternal=false, fOwner='sap', fNoOfPartitions= Optional.empty, fIs Replicated=false, fConsumePollingAll Clusters=null, fAppId=null, fHermesService=Hermes Service\{fName='hermes- internal'\}\}', fValue=null\}\}\) :org.apache .kafka.common. errors. TimeoutException: Topic snc.sap.sn\_ logstoanalytics. xxxxxxxxxxxxx not present in metadata after 100 ms.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Table Administration and Data Management

 PRB1850232

</td><td>

Query with the yyyy/mm/dd format does not work in RaptorDB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1889443

</td><td>

While changing the date format, the end date selection in agent relocation in Workspace throws an error

</td><td>

The user observes an error while selecting the date.

</td><td>

1.  Change the glide.sys.date\_format to MM/dd/yyyy.
2.  Open CSM/FSM configurable workspace and open any territory.
3.  Open agent relocation tab and click on end date.

 Expected behavior: The user should be able to select the end date in agent relocation tab.

 Actual behavior: The user observes an error while selecting the date.

</td></tr><tr><td>

Territory Planning

 PRB1889733

</td><td>

Addition of Query ACLs in Field Service Manager Workforce

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Transaction Logs

 PRB1827610

</td><td>

The errors and logs metrics were removed in the XMLStats servlet include, causing the Logs graph in the ServiceNow Performance dashboard to be 0 after upgrade

</td><td>

When the user goes to ServiceNow Performance Dashboards, some of the graphs are not shown, and instead show the error message 'Error:Invalid series data'.

</td><td>

1.  Create a base Vancouver instance.
2.  Navigate to the ServiceNow Performance dashboard.
3.  Let the instance run until a non-zero number in the Errors and Logs metric graphs appears.
4.  Upgrade the instance to Washington DC.
5.  Look at the Errors and Logs metric graphs again after upgrade is complete.

 Expected behavior: The graph should show values accordingly.

 Actual behavior: The graphs will flat line at 0.

</td></tr><tr><td>

Transaction Management

 PRB1883480

</td><td>

A session isn't authorized when restored by portable sessions with the Explicit Roles plugin enabled

</td><td>

This is mostly likely due to snc\_internal role not being restored.

</td><td>

1.  Provision an instance with 2+ nodes.
2.  Activate the Explicit Roles plugin \(com.glide.explicit\_roles\).
3.  Log in as an admin.
4.  Navigate to the sys\_saved\_user\_ session\_list.do.
5.  Force a node switch.
6.  Refresh the page.

 Expected behavior: The 'List' view displays no records and 'Number of rows removed from this list by Security constraints'.

 Actual behavior: There's a 'Security constraints prevent access to requested page' page.

</td></tr><tr><td>

UI Builder \(Family Channel\)

 PRB1824234

</td><td>

The 'now-date-time-interval' component in UI Builder is not working as expected when the 'same day selection flag' is toggled on

</td><td>

The 'now-date-time-interval' component in the UI Builder is not working as expected. When selecting the start date, the user cannot pick the same date for end date even though 'Enable same day' is toggled on. The user is allowed to pick the same day only if they select another date or modify the time.

</td><td>

1.  Navigate to UI Builder.
2.  Open the CSM/FSM Configurable Workspace experience.
3.  Pick any page.
4.  Add the 'now-date-time-interval'.
5.  Select **Preview**.
6.  Pick the start date.
7.  Attempt to pick the same start date as the end date.

</td></tr><tr><td>

UI Field Administration

 PRB1560731

 [KB1113102](https://hi.service-now.com/kb_view.do?sysparm_article=KB1113102)

</td><td>

The **Template Value** field can lose data if the record is updated before it is finished loading

</td><td>

Data in **Template Value** type fields are lost or cleared when they are saved.

</td><td>

1.  Navigate to **sys\_script.do**.
2.  Fill the mandatory fields.
3.  Navigate to **Actions** &gt; **Set field values**.
4.  Select **description**.
5.  Set the **value**.3. Save the record.
6.  Allow the record to load.
7.  Quickly select **Update** on the form header once the record is saved.
8.  Return back to the business rule.

 Notice that **Set field values** is empty.

</td></tr><tr><td>

UI Form Administration

 PRB1814991

</td><td>

Bulk-edit pop-up form in a presentational list won't refresh after previous transaction

</td><td>

The bulk-edit UI action pop-up form contains the input from the **Description** field from a previous transaction to other records that are opened.

</td><td>

1.  Navigate to **UI Builder** &gt; **Service Operations Workspace**.
2.  Add a variant to the List.
3.  Select **List Page Template** in the Template Picker.
4.  Ensure the new variant has a smaller order than the existing one, so it becomes the default list.
5.  Navigate to **Workspace** &gt; **Service Operations Workspace** &gt; **List** &gt; **Incident** &gt; **All**.
6.  Select any record.
7.  Select the **Edit \(1\)**UI action.
8.  Update the **Description** field in the pop-up to **ABCDE**.
9.  Select **Update**.
10. Notice the success update message.
11. Select another record.
12. Select the **Edit \(1\)** UI action.
13. Notice the **Description** field contains the user input 'ABCDE' from the last transaction.
14. Select **Cancel**.
15. **Confirm** to discard the changes.
16. Select another record.
17. Select the **Edit \(1\)** UI action.

 Notice the **Description** field still contains the user input 'ABCDE' from the previous transaction.

</td></tr><tr><td>

UI Form Administration

 PRB1829603

</td><td>

Workspace fields are cleared when using multiple tabs with an agent

</td><td>

After upgrading to the Washington DC release, an issue occurs when accessing multiple tabs during a chat with a live agent, in which already completed interaction records are cleared.

</td><td>

1.  Log in to an instance.
2.  Impersonate a user.
3.  Navigate to the **Service Operations Workspace**.
4.  Update the status to **Available** in two different tabs.
5.  Impersonate two users.
6.  Initiate a chat from portal.
7.  Fill all the fields in the interaction record.
8.  Search for 'REQ0010001' in the workspace.
9.  Attempt to open REQ0010001.
10. Navigate to **Related Record** &gt; **Requested Items** &gt; **Catalog Tasks**.
11. Add to the work notes.
12. Close the Related Record tab.
13. View the interaction records.
14. Notice that the values are cleared.

 Expected behavior: The updated values in the interaction record shouldn't be cleared after opening multiple tabs.

 Actual behavior: The updated values in the interaction record are cleared after opening multiple tabs.

</td></tr><tr><td>

UI Form Administration

 PRB1876467

</td><td>

timeAgo.js generates an incorrect string for date/time, more than 12 months in the future

</td><td>

It incorrectly indicates the past.

</td><td>

1.  Open any form in UI16/Next Experience with a **date/time** field.
2.  Set the **date/time** to 13 months in the future.
3.  Hover over the **date/time** text in the input and look at the tooltip text.

 Expected behavior: 'About a year from now'.

 Actual behavior: 'About a year ago'.

</td></tr><tr><td>

UI Policies

 PRB1894468

</td><td>

Performance degradation for Core UI performance

</td><td>

Core UI performance testing shows 250 to 300ms degradation for most direct load user actions.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1860251

</td><td>

Fix the incorrect migrated user consent decisions

</td><td>

Users who consented as 'N/A' or 'Agree' for tracking are not tracked after upgrading to Vancouver or recent families. After upgrading to the latest release, observe that if the decisions are 'N/A' or 'Agree' in the old table, they are migrated as false in the new table sys\_analytics\_user \_consent\_decision. These decisions should be migrated as true 'Y'; any decision other than 'N' should be considered as 'Y'. These decisions are migrated as false 'N' for 'N/A' and 'Agree'.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1834286

</td><td>

maxMainTabLimit is not honored on workspace tabs

</td><td>

After updating the properties 'maxCachedPageCount' and 'maxMainTabLimit' to 15, the user should be able to open 15 case tabs in the Customer Service Management/FSM Configurable Workspace.

</td><td>

1.  Log in to the instance as admin.
2.  Update the property **maxCachedPageCount** to 15.
3.  Update the property **maxMainTabLimit** to 15.
4.  Log in to the instance as a user.
5.  Navigate to the Customer Service Management/FSM Configurable Workspace.
6.  Attempt to open 15 case tabs.
7.  Attempt the scenario multiple times.

 Expected behavior: The limits set for the properties should always be honored, and the user should always be able to open a maximum of up to 15 tabs.

 Actual behavior: The user can only open 10 tabs in some cases, and 15 tabs in other cases.

</td></tr><tr><td>

UX Framework

 PRB1860400

</td><td>

Mega-menu lacks tab-panel markup on a demo Portal app

</td><td>

The list of tabs and buttons without a 'collapsed' or 'expanded' state are not announced for screen reader users.

</td><td>

1.  Open an instance.
2.  Open Demo Portal App by appending the URL using /now/demo/portal/home.
3.  Wait for the Portal Home page to open.
4.  Use a screen reader to navigate the page using the **Tab** key.
5.  Expand the **Navigation Menu 2** menu.
6.  Select a sub-menu such as **Menu Item 1**.
7.  Notice how these menu items and the subsequent content is announced for screen reader users.

 Expected behavior: The left-hand list of tabs should announce as such, and the buttons should have state information such as 'collapsed' or 'expanded'.

 Actual behavior: The left-hand list of tabs are not announced and the buttons with no state information such as 'collapsed' or 'collapsed'.

</td></tr><tr><td>

UX Framework

 PRB1866363

</td><td>

Opening more than the max limit CSM workspace tabs outside ServiceNow AI Platform does not trigger the 'Max limit reached' pop-up

</td><td>

Configuring the sys\_ux\_page\_property to not allow more than 10 tabs open in CSM workspace. When selecting '+' 11 times manually inside the CSM Workspace, 10 tabs are opened as expected. When 11 tabs are opened, a pop-up appears. When the tabs are triggered from outside the ServiceNow AI Platform using simple JavaScript, 10 tabs are open as expected, when 11 tabs are triggered, all 10 tabs are closed and a new tab is opened.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1868302

</td><td>

Interaction Related Records for 'View Knowledge Articles' in the Service Operations Workspace \(SOW\) are incorrect after upgrading Xanadu

</td><td>

Interaction related records does not map correctly when viewed from SOW.

</td><td>

1.  Hop on to a base instance.
2.  Open the Service Operations Workspace.
3.  Select **Lists** &gt; **Interactions**.
4.  Select **New**.
5.  Completed all required fields.
6.  Select **Save**.
7.  Select **Agent Assist** from the left pane.
8.  Open any KB article in full view.
9.  Navigate to **interaction\_related\_ record.LIST**.
10. Observe that the record is created, and that the ID of the related record is empty and that the table is incorrect.
11. Observe that the knowledge article is empty, and the record type should be 'Knowledge'.
12. Navigate to the **Filter navigator** &gt; **interaction\_related\_ record.LIST**.
13. Find the entry created and compare it to the pre-upgrade entries that have completed information.

</td></tr><tr><td>

UX Framework

 PRB1884646

</td><td>

There's multiple occurrences of the 'js-common-mega' bundle in the 'Asset' table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1886617

</td><td>

Dynamic Action component returns duplicate sys\_ids

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1845590

</td><td>

Phone number Generative AI regex pattern masks unwanted utterances

</td><td>

Generative AI regex pattern masks unwanted utterances such as dates.

</td><td>

1.  Install the Generative AI Controller, Data Privacy and Data Discovery plugins.
2.  Navigate to dp\_configuration\_ domain\_separated table.
3.  Activate the Phone Number GB \(Generative AI\) regex for the Now Assist Data Channel.
4.  Execute a capability with **2025-01-17 12:53:00** in the utterance.

 Observe the bug that masks the date.

</td></tr><tr><td>

Virtual Agent

 PRB1851088

</td><td>

Catalog items are not displayed in the card format in the AI Search block in non-English languages

</td><td>

This issue only occurs when the preferred language is set to non-English languages, and behaves as expected when the preferred language is English.

</td><td>

1.  Log in to an instance.
2.  Change the preferred language to German or any non-English language.
3.  Navigate to Service Portal.
4.  Initiate a chat.
5.  Search for **iPhone 13**.
6.  Select **\(Katalog\) Apple iPhone 13**.

 Notice that the result is not displayed in the card format.

</td></tr><tr><td>

Virtual Agent

 PRB1862323

</td><td>

Translate Texts subflow sending text\_type as null to DT subflow for Virtual Agent after upgrading to Xanadu

</td><td>

The 'textType': null should not be passed in additional\_parameters to the Microsoft Translate or Google Translate spoke subflow.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1868975

</td><td>

Some text in some OutputCardControls isn't translating

</td><td>

Specifically the **msg\_heading** and **heading** fields sent in custom Teams notifications aren't translated.

</td><td>

1.  Set up local instance with chat, DTVA, and MS Teams channel configuration.
2.  Install a language pack.
3.  Change the language.
4.  Create a custom notification.
5.  Trigger a notification.

 Notice the message and the message heading aren't translated.

</td></tr><tr><td>

Virtual Agent

 PRB1879865

</td><td>

Now Assist doesn't generate Japanese answers properly

</td><td>

The results are mostly in English.

</td><td>

1.  Provision an instance with the Japanese plugin, Now Assist for AI Search \(latest version 10.18\), and Now Assist for VA installed.
2.  Enable Now Assist for AI Search, Now Assist for VA, Now Assist Genius result, and include feature in the esc portal.
3.  Impersonate a user.
4.  Change the language to Japanese.
5.  Escape.
6.  Open VA chat.
7.  Input メールアドレスを追加したい.

</td></tr><tr><td>

Virtual Agent

 PRB1881762

</td><td>

Use the API introduced by STRY58769225

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881917

</td><td>

Running multiple agent chat conversations with profanity on leads to overlapping of messages between the conversations

</td><td>

 

</td><td>

1.  Provision an instance with the Glide Virtual Agent and Agent Chat plugins installed.
2.  Install the store app va-profanity-filter.
3.  Enable profanity filtering
4.  Create multiple agent chat conversations and exchange the message between them continuously.

 Notice that intermittently messages are mixed between conversations.

</td></tr><tr><td>

Virtual Agent

 PRB1885889

</td><td>

There's an error in the translation of Spanish topics

</td><td>

Internal names display on the topic picker when the topic picker cache is built for the first time when the default system language \(Spanish\) is different from the session language \(such as English\).

</td><td>

1.  Have the Spanish localization plugin installed on the instance.
2.  In VAD, create an NLU topic with different internal and display names.
3.  Publish the topic.
4.  Set glide.sys.language sys prop to es \(Spanish\).
5.  Check that com.glide.cs.cache. topic\_type\_dto.enabled sys prop is set to true.
6.  Ensure that the session language is in English.
7.  Clear the cache.
8.  In VAD, select **Test active topics**.
9.  The topic picker displays. Select **Show me everything**.

 Expected behavior: The display name of the topic should display in the list.

 Actual behavior: The internal name displays in the list.

</td></tr><tr><td>

Virtual Agent

 PRB1886592

</td><td>

Live Agent cannot send messages with Dynamic translation when Profanity is turned off

</td><td>

The requester does not receive any messages when profanity is turned off.

</td><td>

1.  Set up DTAC, profanity \(sn\_va\_profanity\), in the Spanish language.
2.  Turn profanity off \(**Conversational interfaces** &gt; **Settings** &gt; **Agent chat** &gt; **Profanity**\).
3.  Start a conversation with an agent that is using Spanish.
4.  Requester sends a message in English.
5.  Agent receives message that is translated into Spanish.
6.  Agent sends a message in Spanish.

 Expected behavior: The requester receives message that is translated into English.

 Actual behavior: The requester does not receive any messages.

</td></tr><tr><td>

Virtual Agent

 PRB1887850

</td><td>

Setting com.glide.cs.task.t ransaction.enabled sysprop to 'true' causes multiple issues

</td><td>

A sys\_generative\_ai\_log record with definition = 'Summary \(Now LLM Mixtral\)' has nothing recorded for prompt\_token\_count and response\_token\_count.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1889660

</td><td>

NowAssist in Virtual Agent errors out in hybrid mode after a skill execution

</td><td>

After a skills execution, the user should be taken to empty skill picker, but instead Virtual Agent gets stuck in a loading state indefinitely.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1893952

</td><td>

Now Assist Panel not loading on Yokohama instances

</td><td>

Now Assist Panel is not loading AI Agents not running in Playground. An error is observed in the logs.

</td><td>

 

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1837988

</td><td>

Unable to acquire conversation lock leads to repeated impersonation and excessive logging

</td><td>

Certain long-running Virtual Agent transactions, such as file uploads, can cause excessive impersonation logging.

</td><td>

1.  Start a conversation.
2.  Set the lock\_acquired and lock\_touched to current time.
3.  Set lock\_owner to something other than 'Available'.
4.  Send a custom adapter message.

 Observe the impersonation messages that occur repeatedly until the lock is acquired.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1887568

</td><td>

Implement a sys prop for admins to be able to disable the pinned mode for dynamic window

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1893493

 [KB2182131](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2182131)

</td><td>

Non-conversational catalog items can't be selected if they are preceded by external KB article citations

</td><td>

When Now Assist for Virtual Agent is enabled, catalog items can't be selected in the Virtual Agent interface.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1893493

 [KB2182131](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2182131)

</td><td>

Non-conversational catalog items can't be selected if they are preceded by external KB article citations

</td><td>

When Now Assist for Virtual Agent is enabled, catalog items can't be selected in Virtual Agent interface.

</td><td>

 

</td></tr><tr><td>

Vulnerability Response and Configuration Compliance for Containers

 PRB1891682

</td><td>

Addition of Query ACLs in Vulnerability Response and Configuration Compliance for Containers

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Vulnerability Response

 PRB1889724

</td><td>

Addition of Query ACLs in Vulnerability Response

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) 2.0 AA Compliance

 PRB1857608

</td><td>

The 'of' string is hardcoded in the mega header in i18n

</td><td>

This issue occurs after expanding the Workspace menu.

</td><td>

1.  Launch any base instance.
2.  Navigate to the Workspace menu on the header.
3.  Expand it.

 Observe that after expanding it, an issue with the suggestions appear.

</td></tr><tr><td>

Workforce Optimization for IT Service Management

 PRB1889670

</td><td>

Addition of Query ACLs in Workforce Optimization for IT Service Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1846321

</td><td>

Refactor script of remote table v\_st\_fsm\_schedule \_event

</td><td>

Querying table v\_st\_fsm\_schedule\_event with a giving sys\_id does not return a valid record, and the record is mostly empty. Remote table v\_st\_fsm\_schedule\_event generates a random sys\_id to accommodate a repeated schedule event, making the sys\_id non-deterministic.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1888734

</td><td>

The **Dispatch group** field remains empty onLoad when a work order task is manually created

</td><td>

This prevents the qualifier from progressing.

</td><td>

 

</td></tr><tr><td>

Workplace Core

 PRB1889743

</td><td>

Addition of Query ACLs in Workplace Core

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 3 Hotfix 2](yokohama-patch-3-hf-2.md)
-   [Yokohama Patch 3 Hotfix 1](yokohama-patch-3-hf-1-PO.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1b Hotfix 1](yokohama-patch-1b-hf-1.md)
-   [Yokohama Patch 1b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2143212)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


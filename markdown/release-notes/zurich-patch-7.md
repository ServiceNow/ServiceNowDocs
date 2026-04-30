---
title: Zurich Patch 7
description: The Zurich Patch 7 release contains important problem fixes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-03-10"
reading_time_minutes: 83
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 7

The Zurich Patch 7 release contains important problem fixes.

-   **Zurich Patch 7 was released on March 10, 2026.**
    -   Build date: 03-04-2026\_1012
    -   Build tag: glide-zurich-07-01-2025\_\_patch7-02-19-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z07.00.xlsx).

## Overview

Zurich Patch 7 includes 307 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-zp7.png "Top 10 problem categories")

## Security-related fixes

Zurich Patch 7 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 7, refer to [KB2797601](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2797601).

## Changes in Zurich Patch 7

-   **[Associate a request header with a resource](https://www.servicenow.com/docs/access?context=associate-header-api-resource&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    The request headers that you added are included in the exportable OpenAPI specification in the REST API Explorer with a "type: string" schema definition. For more information about exporting OpenAPI specifications, see .

-   **[Create a theme with Theme Builder](https://www.servicenow.com/docs/access?context=tb-create-theme&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US)**

    If your instance uses Zurich Patch 7, select your secondary color on the same screen before selecting **Next**. In ZP7, only primary and secondary brand colors are required.

    If your instance uses Zurich Patch 7, you can edit any part of the theme from this screen.

-   **[Define an API resource request structure](https://www.servicenow.com/docs/access?context=add-schema-rest-api-request&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Add a schema to a REST request record to define the request's expected data structure.

-   **[Define a REST API response header](https://www.servicenow.com/docs/access?context=define-scripted-api-response-header&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Define one or more REST API response headers in a REST API.

-   **[Define an API resource response structure](https://www.servicenow.com/docs/access?context=add-schema-rest-api-response&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Add a schema and relevant response headers to a REST response to define the response's expected data structure.

-   **[Define a scripted REST API request header](https://www.servicenow.com/docs/access?context=t_DefineRESTServiceHeaders&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Define scripted REST API requestheaders to control which headers the API accepts

-   **[Define a REST API schema](https://www.servicenow.com/docs/access?context=define-scripted-rest-api-schema&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Specify the expected data structure for requests or responses within a REST API by defining a schema.


-   **[Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md)**

    For Now Assist new features and changes, see [Now Assist and agentic AI release notes](../now-assist/now-assist-rn-landing.md).

-   **[Scripted REST APIs](https://www.servicenow.com/docs/access?context=c_CustomWebServices&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)**

    Schemas define a structure that can be used for API requests and responses, including data type, expected fields, and formats. You can define multiple schemas within a scripted REST API, which can be used to specify request and response contents of the resources within that API.


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

Application Manager

 PRB1889269

</td><td>

Progress worker state isn't set to complete after worker is finished

</td><td>

Installing plugins shows an error even when successfully completed. In the logs, it looks like the error comes from a script include. Previously, the code block was a part of a larger function that had appVersion and appID as parameters. The code was refactored into the forceSyncWithStore function, which doesn't have appVersion and appID as parameters. If the gs.info line is reached, it throws an error because those two fields were not passed into the function.

</td><td>

1.  Install the custom scoped app \(such as x\_conym\_atf\_sc\_req or x\_conym\_hrp\).
2.  Check 'sys\_upgrade\_history' to confirm the installation is marked as 'Complete'.
3.  Check the 'sys\_progress\_worker' list for the message 'Progress worker state is not set to complete after worker is finished.'

 Notice that the syslog has the error 'com.glide.script.RhinoEcmaError: 'appVersion' is not defined.'

</td></tr><tr><td>

Application Manager

 PRB1986694

 [KB2753355](https://hi.service-now.com/kb_view.do?sysparm_article=KB2753355)

</td><td>

App Manager and My Company Applications incorrectly shows available updates after update checker

</td><td>

When publishing a new version of the app, it doesn't appear in 'My Company Application'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Connections and Credentials

 PRB1974412

 [KB2730719](https://hi.service-now.com/kb_view.do?sysparm_article=KB2730719)

</td><td>

Certain outbound HTTP requests fail randomly with '401 unauthorized' even though valid tokens exist

</td><td>

While executing outbound HTTP request using REST step, the request misses the authorization header even though the valid oAuth token exists.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Declarative Actions

 PRB1975231

</td><td>

Field decorators for **Variable** fields are cached in a way that causes issues, causing them to not show up sometimes

</td><td>

 

</td><td>

1.  Create a variable set.
2.  Create a catalog item for specific catalogs only.
3.  Add the catalog item to the included in list for the variable set.
4.  Navigate to the catalog item.
5.  Select **Try it**.
6.  Order the item.
7.  Navigate to the request record.
8.  Navigate to the related list.
9.  Navigate to the request item record.
10. Notice the sys id and visit the record in workspace.
11. Add a reference variable to the variable set created above.
12. Navigate to the catalog item.
13. Try it again.

 Following the same steps above, users end with the **Variable** field in workspace without field decorators.

</td></tr><tr><td>

Multi-provider Single Sign-on \(SSO\)

 PRB1979071

 [KB2715489](https://hi.service-now.com/kb_view.do?sysparm_article=KB2715489)

</td><td>

SAML SP Keystore expiration

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Natural Language Query \(Family Release\)

 PRB1992648

 [KB2794876](https://hi.service-now.com/kb_view.do?sysparm_article=KB2794876)

</td><td>

com.snc.nlq.MetadataGenerator modifies GlideElement objects in TableDescriptorCache

</td><td>

This issue is observed in production.

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

Activity Stream

 PRB1923171

</td><td>

When the **Journal** field is truncated, new lines are lost

</td><td>

The new lines are not displayed.

</td><td>

1.  Using the regular text input in compose, post a long message with new lines over 16000 characters \(or whatever the glide.activity.rule.sys\_journal\_field.truncate\_threshold is set to, but the default is 16000\).

Notice the new journal entry popup, but the content has been truncated.

2.  Select **Click here to load and view content**.
3.  Load the content.

 Notice the new lines are not being displayed.

</td></tr><tr><td>

Activity Stream

 PRB1969041

</td><td>

Focus remains on the 'Email' tab after 'Save'

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Navigate to a CSM record.
3.  Open any incident record.
4.  Change the **Impact** field.
5.  Fill in the mandatory **Worknote** field.
6.  Select **Save**.

 Observe that the focus is on the 'Email' tab after refreshing, and the focus returns to Comments, which is expected.

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

Advanced Work Assignment

 PRB1938992

</td><td>

High AWA assignment cycle times for impact voice call routing

</td><td>

A user is uptaking in NVC and they are facing slow response times for call routing. It's taking ~12 seconds to route the call to agent. Each AWA assignment cycle is taking ~11 secs and out of which ~8 secs is being spent for Agent Map creation. Expected response times should be less than a second as there's no other load in the system.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1981019

</td><td>

AWA TransferToQueue shouldn't reassign a workItem to an AI Agent once rejected

</td><td>

If the interaction was previously transferred from the AI Agent, it shouldn't be transferred back to the AI Agent later \(even if the AI agent is available\).

</td><td>

1.  Make sure an AI agent \(sys\_user with identity\_type='ai\_agent'\) is part of the agent chat assignment group of the chat queue.
2.  Make it AI available.
3.  Create a workItem.
4.  Assign it to the AI agent.
5.  Use the 'Transfer to queue' API to transfer the interaction to the same chat queue where the first workItem was created.
6.  Make the agent 'Abel Tuter' available so they receive the transferred workItem.
7.  Invoke the 'Transfer To queue' quick action from Beth.
8.  Select the same chat queue.

 Observe that the interaction is transferred to the AI Agent.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1990260

</td><td>

The CreateSegment Scriptable API throws error when invoked from different scope that is not global

</td><td>

The error 'No implementations found for extension point: interactionSegment' is thrown.

</td><td>

1.  Log in to the instance.
2.  Install customer service management demo data.

Notice two records in sys\_extension\_instance with the point 'global.InteractionSegment' \(openframe\)

3.  Create an interaction and respective phone log record.
4.  Link the phone log record to the interaction by creating interaction related record.
5.  Run this createSegment Wrap Up Scriptable API from 'Scripts - Background' from any other scope \(sn\_openframe\)

 Expected behavior: A wrap up segment with a segment record is created, and works if run from global scope.

 Actual behavior: An error is thrown, 'No implementations found for extension point: interactionSegment.'

</td></tr><tr><td>

Agent Chat

 PRB1964909

</td><td>

When an agent receives a new interaction within the workspace, the non-focused tab won't blink or flash

</td><td>

The tab is focused for the agent, but not the end user.

</td><td>

1.  Log in to a Zurich instance using a regular Chrome session as the agent 'Abel Tuter'.
2.  Make the agent Abel Tuter available on the Service Operations Workspace \(SOW\).
3.  Log in to the Zurich instance using a Chrome profile session as the user 'Abraham Lincoln'.
4.  Navigate to the **/esc** portal.
5.  Log in Zurich instance using a Chrome profile session as another user.
6.  Navigate to the **/esc** portal.
7.  Request a Live Agent.

Notice that as the agent, one tab is focused, but the tab for the end user is not focused.

8.  Send a message.

 Observe that the non-focused tab won't blink or flash.

</td></tr><tr><td>

Agent Chat

 PRB1979795

</td><td>

Users can't update the agent chat status message content consistently via \[sys\_ui\_message\] records

</td><td>

When using agent chat, if an agent joins the chat, leaves the chat, or ends the conversation, a message appears indicating this. If the user wants to update these messages to display something other than 'Agent', they are only able to update the initial message through a \[sys\_ui\_message\] record, where the message for the key is updated to display the desired text. However, the other messages are displayed via business rules. If a user wishes to update these other messages, they must modify these scripts, which can cause breaking changes.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1982490

</td><td>

RECORD\#OPEN\_CALL event isn't emitted during manual reject for transferred work items

</td><td>

The flow breaks inside closeRejectModalAndCard\(\).

</td><td>

1.  For an incoming call, Agent 1 receives and accepts an inbound call.
2.  For a consultation initiation, Agent 1 initiates a consult transfer call to Agent 2.
3.  For a consult rejection, Agent 2 views the alerting popup and rejects the incoming consult call.

 Expected behavior: openframe\_awa\_workitem\_rejected should be emitted.

 Actual behavior: openframe\_awa\_workitem\_rejected isn't generated when agent selects the **Reject** button on an interaction.

</td></tr><tr><td>

Agent Chat

 PRB1990618

</td><td>

Live agent connection is not established with the Utterance and Contact button for non-admin requestors

</td><td>

Even though there is an agent available online, the requestor sees no agents available in the Agent workspace.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1994390

</td><td>

After a Zurich upgrade, hundreds of thousands of log entries are generated by CacheInvalidationEventHandler

</td><td>

The message is 'No endpoints available for cache invalidation'. The source is com.glide.ui.ServletErrorListener.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

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

AI Search \(Glide\)

 PRB1934845

</td><td>

Make query boolean mode a first class parameter for search

</td><td>

When invoking AI search API, there should be a way to override the default query boolean mode. The goal is to first make NAVA default to OR mode.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1980738

</td><td>

When using AISearch Dynamic Filter, the pre-processing doesn't filter out search results as expected

</td><td>

 

</td><td>

1.  Implement AISearch Dynamic Filters in recommended actions.
2.  Implement getFilterCondition to filter the search results with short\_description spam.
3.  Search the term 'Spam' on a case in recommended actions.

 Observe that the search results with short\_description spam aren't filtered out.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1986147

</td><td>

Extend branding properties to support the update to the dynamic landing page 'Search My Servicenow' placeholder

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1989537

</td><td>

New tables added in Knowledge Graph AI Search pipeline

</td><td>

New tables added: sn\_kg\_tag\_table, sn\_kg\_tag\_column, sn\_kg\_tag\_table\_instruction, and sn\_kg\_tag\_column\_instruction.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1990134

</td><td>

If all KBBs from one doc are removed from KB late binding, the post process stops and all following docs are returned

</td><td>

If ACL filtering removes all the embedded documents from a knowledge base article \(and there's no embedded match\), the code stops processing all subsequent documents.

</td><td>

1.  Ensure the KB is using ACL instead of UC 'glide.knowman.search.apply\_acls'=true.
2.  Create two KB articles:
    1.  For KB1, the user has ACL access, but cannot access any of the KBB.
    2.  For KB2, the user has no ACL access.
3.  As the user, search a query that matches KB1. \(Or use result improvement rule to boost KB1.\)

 Expected behavior: KB2 is not shown because the user has no ACL access.

 Actual behavior: KB2 is shown.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1992808

</td><td>

AI server response time is more

</td><td>

While comparing with baseline, slowness on the AIS server side is observed.

</td><td>

1.  Open KG Designer.
2.  Execute any query on EG.

 Notice the response time is slower.

</td></tr><tr><td>

AI Search

 PRB1808581

</td><td>

activateDatasource API can pass semantic index configuration Sys ID from a different index source

</td><td>

The semantic index configuration is activated and the table is re-indexed.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1822229

</td><td>

Query Performance metrics are down because it is polluted with the Genius Result configuration, making difficult to find required information

</td><td>

When logging performance time breakdown, E2E search takes more than 5 seconds forais\_long\_query\_log. There are missing crucial performance metrics breakdown, as it getting polluted with Genius Result pre-processing and post-processing scripts.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1896807

</td><td>

'Index All Table' from the list view of a datasource should trigger 'No block indexing' instead of 'Block re-indexing'

</td><td>

This causes an event queue pile up when the user triggers multiple re-indexing from the list view of the 'datasources' page.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1943058

</td><td>

There's a global search highlighting issue when using a Safari browser in Next Experience with Zing

</td><td>

There's a visual rendering issue affecting the search bar on the Support ServiceNow portal when accessed via Safari OS version 26. The text typed into the search bar isn't properly visible regarding the theme, making it difficult for users to interact with the search functionality.

</td><td>

1.  Log into any instance.
2.  Select any available theme.
3.  Navigate to the support portal.
4.  Select the search bar and begin typing.

 Observe that the input text isn't rendered correctly, affecting visibility and usability.

</td></tr><tr><td>

AI Search UX

 PRB1980290

</td><td>

In the Service Portal with Now Assist enabled, when the tab focus is on the link and the 'Enter' key is pressed, the link doesn't open

</td><td>

 

</td><td>

1.  Navigate to **Conversational Interfaces** &gt; **Assistants**.
2.  Under Now Assist in Virtual Agent, select **Display Experiences** &gt; **Add service Portal** &gt; **Save**.
3.  Open any instance.
4.  Navigate to the **Service Portal**.
5.  Navigate to the search's **Edit** field.
6.  Type 'email' and search for it.
7.  Navigate to the **Search results** &gt; **Select a filter**.
8.  Navigate to the **Any links** in the 'Results' section and attempt to press the 'Enter' key to select.

 Observe that when the tab focus is on the link and the 'Enter' key is pressed, the link does not open.

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

 PRB1989321

</td><td>

Logic for retrieval should support 'CONTAINS' and not just prefix matching

</td><td>

Popular query suggestions are only returned if they start with has been inputted in the Omni bar.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1991226

</td><td>

Search-based suggestions should have a user-friendly label for source

</td><td>

 

</td><td>

Call the Suggestions GQL API with a term that will return search-based suggestions.

 Expected behavior: The payload has the **Source label** field for user-friendly labels based on what is configured for the corresponding source's 'Source Facet Bucket' label on the Search Application.

 Actual behavior: There is no label based on the Source Facet Bucket.

</td></tr><tr><td>

Analytics Data API

 PRB1931476

</td><td>

Issue with Incident SLA donut translation in Service Operations Workspace \(SOW\)

</td><td>

After changing the language in SOW, the Incident SLA widget appears as 'Breached'. After clearing the cache, it then appears as 'undefined'.

</td><td>

1.  Impersonate a user.
2.  Open SOW.

Notice that the Incident SLA widget label appears as 'Breached'.

3.  Change the language to any language.

Notice that the label still appears as 'Breached'.

4.  Clear the cache by cache.do.

 Notice that the label now appears as 'undefined' while the translation is already added in the sys\_ui\_message table.

</td></tr><tr><td>

Analytics Data API

 PRB1952604

</td><td>

The data label indicators show the same unit in Platform Analytics Data Visualization

</td><td>

After creating a data visualization that uses two indicators as data sources with different units, the data labels reflect the same unit.

</td><td>

1.  Create a data visualization \(line\).
2.  Add to the data sources with different units \(\# and % for example\).
3.  Show the data label.

 Expected behavior: The data label unit in each indicator reflects the unit of the indicator.

 Actual behavior: The data label units in both indicators are the same, and not respecting the configured unit of the indicators used as a base.

</td></tr><tr><td>

Asset Management

 PRB1990771

</td><td>

Asset Analyst UI changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1913258

</td><td>

In the IP Filter Criteria Record, the user can't add a description to an existing range

</td><td>

The user is unable to save the form and gets the error message 'Duplicate IP Range entry'.

</td><td>

1.  Open a Yokohama instance.
2.  Navigate to **sys\_ip\_filter\_criteria.list**.
3.  Enter the value for IP range bot \(the start IP and end IP\).
4.  Enter the description.
5.  Select **Save**.

 Expected behavior: The user can save the form.

 Actual behavior: The user is unable to save the form and gets the error message 'Duplicate IP Range entry'.

</td></tr><tr><td>

Authentication

 PRB1975818

</td><td>

The property glide.authenticate.failed\_redirect is not working after login failure

</td><td>

The glide.authenticate.failed\_redirect property is not functioning as expected after SSO login failure. This property is configured to redirect users to a specified URL after a failed SSO attempt. The URL can be either a public knowledge article describing the error with helpful links, or a company URL. However, after login failure, the redirect is not occurring as configured.

</td><td>

1.  Configure the 'glide.authenticate.failed\_redirect' property with a valid redirect URL.
2.  Attempt an SSO login with invalid credentials or configuration.

Observe that after login failure, the user is not redirected to the configured URL.


 Expected behavior: The user should be redirected to the URL specified in glide.authenticate.failed\_redirect.

 Actual behavior: The redirect does not occur as configured.

</td></tr><tr><td>

Authentication

 PRB1990715

</td><td>

Token Exchange API for Voice Service Agent

</td><td>

This is a product update.

</td><td>

 

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

Attachment Summary doesn't work on the new HR case with attachments after using 'Transfer case.'

</td><td>

1.  Open an HR case.
2.  Upload an attachment.

Observe that attachment summarization is working fine.

3.  Select **Transfer case** from the side menu.

Observe that modal opens.

4.  Choose any transfer type \(for example, 'transfer to a new case number'\) and any New HR service\(for example, Dental Benefits Inquiry\).
5.  Select **Ok**.

Observe that this HR case transfers to a new HR case, and all the attachments are also copied to new HR case.

6.  Select **Summarize**on the new HR case.

Observe that attachment summarization is not available even though HR case has attachments.


 Expected behavior: Attachment summarization works on the new HR case with attachments after using **Transfer case**.

 Actual behavior: Attachment summarization doesn't work after using **Transfer case** on the on new HR case with attachments.

</td></tr><tr><td>

Change Management

 PRB1977634

</td><td>

Change ATF test fails/flaps due to ATF steps timeout

</td><td>

 

</td><td>

 

</td></tr><tr><td>

CI Lifecycle Management API

 PRB1772623

 [KB2518604](https://hi.service-now.com/kb_view.do?sysparm_article=KB2518604)

</td><td>

List view does not translate non-English languages for Lifecycle Stage and Lifecycle Stage status

</td><td>

This issue occurs when the user's language preference is set to a non-English language.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

CMDB Query Builder

 PRB1977703

 [KB2727703](https://hi.service-now.com/kb_view.do?sysparm_article=KB2727703)

</td><td>

Query Builder in V2 mode can cause memory issues due to a static variable

</td><td>

An internal variable which is declared as static keeps being appended and thus creates a large memory footprint. This would happen if one or more queries are executed enough times to bloat this variable.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

CMDB Query Builder

 PRB1982264

</td><td>

There's an inefficient query on cmdb\_rel\_ci - primary\_hash=-739782498

</td><td>

The query is scanning 90% of table with an odd OR condition. Also, if users split the OR condition, the first half sys\_id&gt;123 AND sys\_updated=date runs 1ms and the 2nd half sys\_updated\_on date runs in 3ms.

</td><td>

Run the scheduled 'CMDB Query Builder Suggested Relations Computation' job.

</td></tr><tr><td>

CMDB Query Builder

 PRB1984814

</td><td>

'CMDB Query Builder Suggested Rels Cleanup SysTrigger' is using DISTINCT SYS\_ID, causing the query to take very long

</td><td>

Removing DISTINCT so that the query finishes immediately.

</td><td>

 

</td></tr><tr><td>

Column Level Encryption

 PRB1892581

</td><td>

KMFCallerAccessPolicyRecordInterface\#getCLECryptoModulesFromCallerPolicyTable isn't cached, causing a performance bottleneck

</td><td>

getCLECryptoModulesFromCallerPolicyTable shows up in 1.16% of samples and should be cached. It queries sys\_kmf\_crypto\_caller\_policy table, which is a metadata table. This can be easily cached using the CacheManager.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1986775

</td><td>

IRE throws missing dependency errors for dependent CIs when glide.identification\_engine.skip\_sys\_object\_source\_matching property is enabled

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1823749

</td><td>

In GraphMetadataAPI, node/edge types should allow special characters

</td><td>

An error appears that says only alphanumeric and underscore characters are supported.

</td><td>

With JSON or GraphMetadataBuilder, create an edge with type 'Depends On::Used By'.

 Observe the error that says only alphanumeric and underscore characters are supported.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1834259

 [KB2343586](https://hi.service-now.com/kb_view.do?sysparm_article=KB2343586)

</td><td>

Syntax error or access rule violation is detected by database

</td><td>

The following error is displayed when a glidefunction column is used as a sort in a list view with a filter on a denormalized glidelist: '\(ERROR: for SELECT DISTINCT, ORDER BY expressions must appear in select list Position: 2328\)'.

</td><td>

Refer to the listed KB article for details.

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

 PRB1944043

</td><td>

Memory Consumption is significant for getForTables for most transactions in the HI clone during loadtest

</td><td>

getForTables consumes more memory due to JSON parsing.

</td><td>

1.  Setup an instance on Z mainline with Knowledge Graph enabled.
2.  Execute the load test with 6 users 1500 TPH.

 Observed that getForTables seems to be consuming more memory due to JSON parsing in the snapshot.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1951393

</td><td>

Set up a default allowed list of SQL functions for DBSqlParser to use with the existing allow list property

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1953813

</td><td>

The user doesn't get the negative value in duration.between\(\) function

</td><td>

If the first date input is more than the second date input, then the result should be negative.

</td><td>

Execute the following cypher query: 'RETURN duration.between\(date\('2017-02-02'\), datetime\('2016-01-01T00:00:00'\)\).years AS timeDuration'.

 Observe that the output is 1, but it should be -1. If the first date input is more than the second date input, then the result should be negative.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1955802

</td><td>

ScopedGraphMetadata.get\(\) issues 100 queries for sn\_kg.now\_user\_graph

</td><td>

This happens when ScopedGraphMetadata.get\(\) is used in sys\_generative\_ai\_validator \_5a6265987fb05210995810a9dc866558.

</td><td>

Ask 'What is spam?'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1960120

</td><td>

In GraphQueryBuilder, an encoded query string with a blank value for the **int** field gives a cytosm exception

</td><td>

 

</td><td>

1.  Add the encoded query string 'priority=3^state' to the incident node.
2.  Execute the query from GraphQueryBuilder.

 Observe the cytosm exception.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1963104

</td><td>

KG doesn't raise an error when the result is truncated

</td><td>

Truncated results are returned, even though there should be more or an error given.

</td><td>

Issue a query that returns over 1000 results.

 Observe that 1000 results are returned, even though there should be more or an error given.

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

 -   Select top 10 log\(cost\) from cmdb where cost !=0;
-   Select top 10 log10\(cost\) from cmdb where cost !=0;
-   Select top 10 mod\(priority,2\) from incident;
-   Select top 10 repeat\(first\_name,2\), first\_name from sys\_user;
-   Select top 10 replace\(first\_name,'a','ba'\), first\_name from sys\_user;
-   Select top 10 right\(first\_name,2\), first\_name from sys\_user;
-   Select top 10 second\(sys\_created\_on\), sys\_created\_on from incident;

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1986877

</td><td>

Graph JSON cache should respect the 'isTieredCachingEnabledForCacheable' property value

</td><td>

GraphCacheableJSONString should be used for a tiered cache instead of a regular cache.

</td><td>

1.  Disable tiered caching.
2.  Call new sn\_db.GraphMetadata\('graphName'\).get\(\).

 Expected behavior: The tiered cache with GraphCacheableJSONString isn't used.

 Actual behavior: The GraphCacheableJSONString wrapper is used even though the value is in a regular cache.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1987230

</td><td>

C2R pagination API is not working for 'cypher string with LIMIT'

</td><td>

An error occurs when executing the cypher, 'Error executing cypher: Unsupported keyword: LIMIT clause not allowed when using pagination API.'

</td><td>

 

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

Database Persistence - Data Management

 PRB1939498

</td><td>

Migration to RaptorDB brings column length changes, which could impede archive table synchronization

</td><td>

The synchronization should run quickly, but this scenario can occur and slow down the process.

</td><td>

1.  Provision an instance on MariaDB.
2.  Create some archive rules.
3.  Archive some data.
4.  Migrate the instance to RaptorDB.
5.  Install a plugin that will cause many table schema updates that will propagate to archive tables, such as 'Discovery and Service Mapping Patterns.'

Observe what happens during archive table synchronization.


 Expected behavior: The synchronization shouldn't be vulnerable to caches that take a long time to build.

 Actual behavior: The synchronization could become vulnerable to caches that take a long time to build.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1988503

 [KB2764725](https://hi.service-now.com/kb_view.do?sysparm_article=KB2764725)

</td><td>

Active subflow executions with clean parent flow executions are listed as 'Unreferenced Records' and are deleted by DMUnreferencedRecordCleaner

</td><td>

This issue was observed in Zurich. If a parent flow completes while an associated asynchronous subflow continues running, the completed parent flow context is cleaned up by the retention policy by routine system cleanup. As a result, the running subflow becomes unreferenced, and may be removed during routine system cleanup.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1875764

</td><td>

There's DBI leakage

</td><td>

The user can add some code to trap the lease/cache of the DBI and print out the stacktrace \(of where the leak came from\) when it's freed by GlideSession. In Glide without the code, the stacktraces aren't available.

</td><td>

1.  Run Glide.
2.  If the code path is hit by chance, the 'Connections active at session disconnect are being released' message is logged from GlideSession.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1970851

</td><td>

Glide enters 'Databaseless' mode after AHA failover is completed

</td><td>

This happens on an instance where the primary server is down.

</td><td>

1.  Open an instance where PG Fastaha is enabled and the primary server is down.
2.  Perform AHA failover.

 Observe that the failover is successful but app nodes aren't coming online. Glide entered 'Databaseless' mode.

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

Add support for AGlideRecordOptimizer in GlideRecordDynamic, especially for ArrayLoader implementation

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

Database Persistence

 PRB1864221

</td><td>

Glide Aggregate performs a second unrequested aggregate, doubling the DB work and response time

</td><td>

Ideally, there would be a separation of concerns. Table UI performs the queries it wants for itself, and this isn't forced into the code paths for users of Table.java or GlideAggregate.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1930261

</td><td>

DB connection recycling reduces the number of available semaphore permits

</td><td>

During recycling, the freeConnection0 method shouldn't make a connection available or release available semaphore permits.

</td><td>

1.  Find a broken connection marked for recycling.
2.  Try to obtain all available connections up to pool MAX.

 Observe warnings when trying to obtain a connection: 'No connection was obtained while semaphore was available'.

</td></tr><tr><td>

Database Persistence

 PRB1939323

</td><td>

SQLException thrown when loading the sc\_cat\_item table with language translations

</td><td>

SQLException throws an exception that 'GROUP BY' are not in 'SELECT' after changing the language to French and reloading the list view.

</td><td>

1.  Ensure there is a glide node running connected to the postgres database.
2.  Install French Translations plugin \[com.snc.i18n.french\].
3.  Ensure workers are running during the installation of this plugin.

Notice that after the plugin installations, the translations are loaded from an event processor.

4.  Log out.
5.  Log in again as an admin.
6.  Confirm from user settings that a new language is now available.
7.  Open the list view.
8.  Ensure it is ordered by the **Name** field.
9.  Return to the user profile.
10. Change the language to French and reload the list view

 Notice that there is an SQLException stating the fields in 'GROUP BY' are not in 'SELECT.'

</td></tr><tr><td>

Data Management Console

 PRB1977994

</td><td>

Remove unnecessary debug and warn logs in Stats Gatherer

</td><td>

The logs print many times in prod even though they're debug logs. The record count estimate for the table 'Optimal sys\_id prefix length' is fetched from the transaction cache for the table.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1905069

</td><td>

Discovery can fire both discovery.completed and discovery.canceled events, which results in any 'run after' schedules being triggered twice

</td><td>

Triggering both completed and canceled events is an error, but Discovery needs to be resilient when errors occur. This issue is not about both events getting fired; it's intended to handle the case where both events are fired in error.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1956011

 [KB2601907](https://hi.service-now.com/kb_view.do?sysparm_article=KB2601907)

</td><td>

ADM / ADME probes cause memory issues and take down instance nodes due to large amount of PostgreSQL processes discovered

</td><td>

When ADM / ADME sensors are running, around 150MB memory is consumed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1981940

</td><td>

Add global scope support to allow application scope to delete cmdb\_file\_information records

</td><td>

The cmdb\_file\_information table is owned by the global scope and requires global-scope handling for controlled bulk deletions.

</td><td>

1.  Create or use an existing application scope.
2.  Implement logic in the application scope that requires deletion of records from the cmdb\_file\_information table using dynamic query conditions \(based on runtime parameters\).
3.  Attempt to perform the deletion directly from the application scope.

 Observe that the deletion can't be completed due to cross-scope access restrictions and/or the lack of a global-scope utility that supports dynamic, caller-defined queries.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1988914

</td><td>

Add functionality for Input Router to consider an entire document set

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Dynamic Scheduling

 PRB1979973

</td><td>

Dynamic scheduling shows the wrong date for certain tasks when the date format is different than default

</td><td>

The date format for all tasks should align with the default date format.

</td><td>

1.  Set the date format to DD/MM/YYYY.
2.  Set the assignment method to dynamic scheduling.
3.  Drag and drop a Pending Dispatch task\(T1\) onto an Assigned task.

 Expected behavior: The date format for both tasks align with the default date format.

 Actual behavior: The original task\(T1\) has a date format that doesn't match the default date format. This causes an error when confirmed, as the date would be miscalculated.

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

Embedded Help

 PRB1975389

</td><td>

Add a check in Platform to control the access of foreign language content from Gumbo

</td><td>

Support has been extended to localized content in the Help Center framework. However, content in languages other than English isn't being published to Gumbo. There should be some control in the instance to avoid hitting the Gumbo to access the foreign language content.

</td><td>

 

</td></tr><tr><td>

Encryption

 PRB1982059

</td><td>

Migration job changes to separate Rekey issues and 3des migration failures

</td><td>

After the job execution is complete, the summary has recordsSkipped. The 3des skipped records are captured in recordsSkippedSysId.

</td><td>

1.  Open a Zurich instance that has long 3DES encrypted data that is less than 125 characters in the **password2** fields.
2.  Navigate to **Security Jobs** &gt; **Create new** &gt; **Mass encryption job**.
3.  Create a job with the type 'Password2 data migration'.
4.  Execute the job and wait for it to complete.

 Observe that the summary has recordsSkipped and the 3des skipped records are captured in recordsSkippedSysId.

</td></tr><tr><td>

Encryption Support

 PRB1973482

</td><td>

Search filter 'startsWith' is not working on a referenced column when another column with the same name has an EFC

</td><td>

This is happening due to the 'Like' operator being removed as the method 'com.glide.db.ElementDescriptor\#shouldConcealForQuery' is returning 'true'. The column 'profile.name' should be null since there is no EFC on Entity.name or Profile Name column \(reference\).

</td><td>

1.  Create Entity table with the following columns:
    1.  id \(Integer\)
    2.  name \(string\) display =true
2.  Create Profile table with the following columns:
    1.  Id \(int\)
    2.  Profile Name reference to Entity table
    3.  comments \(string\)
    4.  name \(string\)
3.  Create an EFC on the profile.name column.
4.  Enter few records into the Profile table
5.  Create a filter on the Profile table.
6.  Select the column **Profile Name**.
7.  Select the operator **startsWith**.

 Notice that the the filter didn't return matching results, and instead shows all the records in the table.

</td></tr><tr><td>

Event Management

 PRB1990235

</td><td>

Add an entry point to sanitize an **HTML** field before insert

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1907242

</td><td>

Published flow switched from CRUD trigger to email trigger doesn't create sys\_flow\_email\_trigger

</td><td>

When the trigger type has changed to email trigger, creating or updating a record-based trigger shouldn't activate the flow. It should only be triggered by inbound email.

</td><td>

1.  Create a flow with a CRUD trigger and publish it.
2.  Trigger the flow.

Observe that it works fine.

3.  Change the trigger type to inbound email.
4.  Verify that the sys\_flow\_email\_trigger record isn't created and the sys\_flow\_record\_trigger is still active.
5.  Create a record as configured in step one.

 Observe that the flow is still triggered. Since the trigger type has changed to email trigger, creating or updating a record-based trigger shouldn't activate the flow. It should only be triggered by inbound email.

</td></tr><tr><td>

Flow Engine

 PRB1935825

</td><td>

Skip\_schedule\_cleanup is not reset to false for subflows

</td><td>

The table cleaners need to be revised.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1944299

</td><td>

'Extension point not found' exception from com.glide.hub.action\_step.script plugin

</td><td>

The send\_notifications action executed on a node with new code has no error. The send\_notifications action executed on a node with old code errors out with an exception.

</td><td>

1.  Open a Yokohama or Zurich 2-nodes TD instance.2. Generate Now Assist Troubleshooting Notifications.
2.  Upgrade node 1 to a more recent release.

 Expected behavior: The send\_notifications action is executed on both node 1 and node 2 without any error.

 Actual behavior: The send\_notifications action executed on node 1 \(the new code\) has no error. The send\_notifications action executed on node 2 \(the old code\) errors out with an exception.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1952639

</td><td>

There's an error in the logs: 'com.glide.script.RhinoEcmaError: 'FlowRecommendationsSkillCheck' is not defined'

</td><td>

There are 464 error logs in the last 15 minutes. This makes it difficult to check the debug logs. Nothing is being executed on the instance.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1990495

 [KB2780048](https://hi.service-now.com/kb_view.do?sysparm_article=KB2780048)

</td><td>

The 'Update record' action updates an invalid GlideRecord and triggers business rules when the reference record is deleted while a flow is in progress

</td><td>

When the record that is passed to a subflow is deleted while the flow is in progress, any 'Update record' action in the subflow doesn't error out with 'Glide record is invalid' type errors. Instead, the 'Update record' action in the subflow falls back and iterates on all records in the table, causing substantial data impact.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1990711

</td><td>

Text2flow Glide changes

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

Form Templates

 PRB1959535

</td><td>

A Knowledge Article body isn't applied when using templates after upgrading Zurich

</td><td>

 

</td><td>

1.  Set up a template on the kb\_knowledge table to populate **Article Body** with some text.
2.  Navigate to **kb\_knowledge.list**.
3.  Create a record of type 'standard'.
4.  Apply the template.

 Expected behavior: The article body should populate with template content.

 Actual behavior: After enabling glide.ui.html.editor.use\_v5 and clearing cache, the article body remains empty.

</td></tr><tr><td>

GlideRecord

 PRB1990713

</td><td>

MID Server core logic for Collector Framework

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

GraphQL API

 PRB1971431

</td><td>

Extremely large tables are queried from GlideRecordSchema, causing out of memory errors

</td><td>

Out of memory exceptions are occurring in the GraphQL framework when GlideRecordSchema is invoked to query tables with extremely high record counts. The cause looks to be from GlideGraphQLQueryHolderImpl.getRowCount return the rowCount of the GlideRecord when it should be providing the pagination limit size. The value from that method is used to initialize an ArrayList of the provided size in the graphql-java framework ExecutionStrategy.

</td><td>

 

</td></tr><tr><td>

GRC Platform Plugins

 PRB1972072

</td><td>

The P95 response time for task page loading across all the workspaces exceeds SLA of 4 seconds

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Navigate to **Risk** &gt; **Audit** &gt; **Compliance** &gt; **ESG** &gt; **Privacy WS**.
3.  Select **Task Page Widget**.

</td></tr><tr><td>

Horizon Component Library

 PRB1984430

</td><td>

The **change-ai-sparkle** icon is blank in now-icon 29.0.45

</td><td>

If a component contains the icon, then the icon will be blank.

</td><td>

1.  Create a TD instance from track/znowassist.
2.  Sideload a component \(for example, now-list-commons\) to the TD instance that contains servicenow@now-icon version 29.0.45.
3.  Create a new experience with the Workspace App Shell in UI Builder.r
4.  Create a blank page from scratch.
5.  Add an icon with **now-button-stateful** containing **change-ai-sparkle-fill**.

 Expected behavior: The **change-ai-sparkle** icon shows up.

 Actual behavior: The icon cannot be found.

</td></tr><tr><td>

Horizon Design System

 PRB1973789

</td><td>

Agentic AI and GenAI color gradient implementation

</td><td>

This is a product update.

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

HTML Field Type Editor

 PRB1990982

</td><td>

Predictive text assistance

</td><td>

This is a product update.

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

After Zurich, the **Source task** field for knowledge articles isn't assigned

</td><td>

This issue occurs when a user creates a feedback task record for a knowledge article. The feedback task allows knowledge managers to either edit the existing article or create a new one. However, when users attempt to create a new article from the feedback task, the new article doesn't reference the originating feedback task as it does in Yokohama. The **Source task** field, which should contain this reference, appears in the article form view, but it is grayed out and empty.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1992747

</td><td>

Now Assist KB creation pop-up is unable to continue with the KB creation when no tasks are available for search

</td><td>

This issue occurs only in Native UI. Using the 'Create knowledge' UI from Native UI during KB creation shows no options available to continue without selecting tasks. This blocks KB creation.

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

 PRB1995579

</td><td>

True up versions for NAKM, KC, KCUIB and ECE

</td><td>

 

</td><td>

 

</td></tr><tr><td>

KPI Details

 PRB1972051

</td><td>

On the 'KPI Details' page, a chart isn't rendering the latest score for indicators with fiscal yearly frequency

</td><td>

 

</td><td>

1.  In system properties, set com.snc.pa.fy\_start to a month from which the fiscal year starts.
2.  Create an indicator source and its indicator \(pa\_indicator\) with the fiscal year as the frequency.
3.  Run a data collection job for the indicator.
4.  In pa\_scores\_l1 table make sure that scores are present for current p.
5.  Navigate to the created indicator, and select **Explore indicator** to navigate to the **KPI Details** page.
6.  Select **Edit scores**.
7.  Check if the scoresheet has score populated for the current fiscal year. If not, delete all scores before filling in the scores.

On the KPI 'Details' page, the chart doesn't render the content for current fiscal year.

8.  Create a single score visualization on a dashboard for this indicator.
9.  Select the visualization to navigate to the **KPI Details** page of the indicator.

 Observe that even upon changing the end date in the URL, the chart renders but the current fiscal year score is rendered beyond the chart container and isn't accessible.

</td></tr><tr><td>

Language and Translations

 PRB1975283

</td><td>

The Japanese sys\_ui\_message on the UI page 'set\_initial\_selection\_criteria' unexpectedly has HTML tags

</td><td>

There should be no HTML tags. Reproducible in Zurich and Yokohama.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1917110

</td><td>

In Yokohama, the fixed filter condition doesn't calculate the sum in list view

</td><td>

The total value calculation doesn't account for the fixed filter condition defined in the module.

</td><td>

1.  Enable the calculated list configuration for a **decimal-type** field.
    1.  Select and hold \(or right-click\) the **Column header** in the list view. For example, Sunday in the time\_card table.
    2.  Select **Total Value**.
2.  Navigate to the **sys\_app\_module** table.
3.  Create a module with a fixed filter condition using the URL from arguments. For example, time\_card\_list.do?sysparm\_fixed\_query=user=javascript:gs.getUserID\(\).
4.  Impersonate any user.
5.  Open the time\_card list view via the module.
6.  Check the sum value displayed for the configured **Decimal** field.
7.  Manually apply the same filter condition using the list filter.

 Observe that the total value calculation does not account for the fixed filter condition defined in the module. This behavior works correctly in the Xanadu instance.

</td></tr><tr><td>

List Administration

 PRB1918529

 [KB2669196](https://hi.service-now.com/kb_view.do?sysparm_article=KB2669196)

</td><td>

Export doesn't contain current view data

</td><td>

The export functionality doesn't apply the fixed filter configured in the list UI Builder's 'Fixed Filter' property. When exporting data, the exported file includes all records instead of reflecting the current view filter. This occurs when the fixed filter is configured in the 'Fixed Filter' property, as the export button ignores this configuration and only applies optional filters. The issue is reproducible in workspaces using the record-list-connected component \(NRLC\), where the fixed filter is not respected during export.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1934797

</td><td>

There's an issue configuring the Platform Analytics Scheduled Exports Library list

</td><td>

The **Time** field isn't working as intended when added to the list view.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1935030

 [KB2665434](https://hi.service-now.com/kb_view.do?sysparm_article=KB2665434)

</td><td>

Highlighted values have limited width on the initial load of the now-list

</td><td>

After resizing it's working fine; the issue is with the initial load.

</td><td>

Refer to the listed KB article for details.

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

List Administration

 PRB1991370

</td><td>

Presentational list should allow for suppressing Rows Hidden alerts via system property

</td><td>

The 'X rows removed from this list by security constraints' continues to appears to ITIL users even though the system property is set to 'true.'

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

List Administration

 PRB1991465

</td><td>

Change the header notification in the list when grouping is applied

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Localization Framework

 PRB1979838

</td><td>

Enable field labels and choices artifact support in Localization Framework for some escalations

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

MID Server

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

Mobile Experience for Field Service Management

 PRB1978601

</td><td>

Offline Mode fails with an error due to FSM Data Item query fetching assets even if the **Location** field is empty

</td><td>

 

</td><td>

1.  Configure the Field Service Mobile plugin.
2.  Have many records in wm\_task where the 'Assigned to user' has their **Location** field empty, which will be returned by the 'DI\_my\_inventory\_remove\_parts' data item.
3.  Log in to Agent Mobile with FSM active.
4.  Enable Offline mode.
5.  Attempt to download cache.

 Notice that an error occurs.

</td></tr><tr><td>

Mobile Platform

 PRB1981639

</td><td>

Support custom filter and parameterized data item

</td><td>

The custom filter doesn't work offline. The default filter is displayed instead.

</td><td>

Scenario 1:

 1.  In any instance, activate the Field Service Management Demo plugin.
2.  As an admin, configure the 'My team' screen, the **View Team Members** button, and the 'Team members' screen to be available offline.
3.  Sign in as the user 'Alex' from Agent.
4.  Download offline.
5.  Go offline.
6.  Select **More** &gt; **My team**.
7.  Select the **NoCal Technicians** item in the list to go to the 'Team members' screen.
8.  Select **Filter** to show the default filter in offline.
9.  Enter 'Alex' as the name.
10. Select **Apply**.

 Expected behavior: The filter is applied.

 Actual behavior: The filter with 'Alex' isn't applied.

 Scenario 2:

 1.  As an admin, configure a custom filter on the 'Team members' screen to filter on name.
2.  Sign in as the user 'Alex' from Agent.
3.  Verify that the custom filter works as expected online.
4.  Download the offline cache.
5.  Go offline.
6.  Select **More** &gt; **My team**.
7.  Select the **NoCal Technicians** item in the list to go to the 'Team members' screen.
8.  Select **Filter**.
9.  Enter 'Alex' as the name.
10. Select **Apply**.

 Expected behavior: The custom filter is displayed and filtering with 'Alex' works the same as online.

 Actual behavior: The default filter is displayed and filtering with 'Alex' doesn't work.

</td></tr><tr><td>

Mobile Platform

 PRB1984396

</td><td>

**Dot-walk** reference fields in filter aren't resolved

</td><td>

The filter reference list doesn't have the expected items.

</td><td>

1.  In any instance, activate the Field Service Management Demo plugin.
2.  As an admin, configure the 'My team' screen, the **View Team Members** button, and the 'Team members' screen to be available offline.
3.  As an admin, configure a custom filter on the 'Team members' screen to filter on a **dot-walked** reference field. \(For example, **User** &gt; **Manager** &gt; **Location on table sys\_user\_grmember**.\)
4.  Sign in as a user from Agent.
5.  Download offline.
6.  Go offline.
7.  4. Select **More** &gt; **My team**.
8.  Select the **NoCal Technicians** item in the list to go to the 'Team members' screen.
9.  Select **Filter** to show the custom filter in offline.
10. Select the **Reference** field to bring up reference list.

 Expected behavior: The filter reference list is rendered with the expected items.

 Actual behavior: The filter reference list doesn't have the expected items.

</td></tr><tr><td>

Mobile Platform

 PRB1987587

</td><td>

Check for the Mobile language plugin before getting the language bundle in LanguageProvider.java

</td><td>

API calls to /api/now/v1/sg/properties' and '/api/now/v2/sg/user\_client could trigger slow SQL queries, leading to semaphore exhaustion and rejected transactions. When there is a large amount of data in the sys\_translated\_text table, the code could be triggered, resulting in a slow query. The query should be run when the user has the Mobile custom language plugin installed.

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

Multimodal Service \(Family Channel\)

 PRB1990234

</td><td>

Update the MMService plugin to support MMS asynchronous backend

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

 Observe the results in the sys\_mm\_result table, and the error message in the 'Error message' column

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1979645

</td><td>

Global search in native view is not minimizing once exact match is selected

</td><td>

 

</td><td>

1.  Open a base instance.
2.  Take any active incident number and paste it in the global search.
3.  Wait until exact match appears.
4.  Select the exact match once it appears.

 Notice that once it is redirected to incident record, the search result \(exact match\) is still open and not minimized.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1998576

</td><td>

Catalog Builder home page is not loading

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Normalization Data Services

 PRB1931854

 [KB2664685](https://hi.service-now.com/kb_view.do?sysparm_article=KB2664685)

</td><td>

A core company isn't handled correctly for a domain-separated environment

</td><td>

In a domain-separated environments with Normalization Data services turned on, creating models or configuration items may fail or use an incorrect manufacturing \(publisher\) company. When selecting a manufacturer from a specific domain, the system incorrectly replaces it with a company record from the user's domain.

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

OAuth

 PRB1992657

</td><td>

Add support for OAuth-protected resource metdata and cross-origin resource sharing \(CORS\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1981295

</td><td>

OnCallRotation.getPrimaryUser returns null when there's no members on a roster and only coverage present

</td><td>

.

</td><td>

1.  Log in to instance and make sure an assignment group has the roaster with no members and has only the Primary Coverage.
2.  Execute the script.

 Expected behavior: The user id is returned.

 Actual behavior: The result is null.

</td></tr><tr><td>

OneExtend

 PRB1985682

</td><td>

The **User** field is blank in the 'Generative AI Usage Logs' table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1986680

</td><td>

Update in the CDS flow to update the Gen AI model configuration table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1989677

</td><td>

Unable to run evaluations for resolution notes Generation skill

</td><td>

Models are failing for different reasons according to the error messages that occur.

</td><td>

Create the evaluation job for security incident resolution notes prompts with 'RN Data Set New' for third party providers.

 Notice that models are failing with different reasons.

</td></tr><tr><td>

OneExtend

 PRB1990084

</td><td>

The integration\_type metadata is missing in the metadata sync that is needed to support BYOK scenarios

</td><td>

Metadata sync from glide to Mosaic is missing the integration\_type related metadata. Without this metadata, Mosaic would not know whether the user has opted in for BYOK, and therefore cannot support BYOK related use cases. The metadata sync from glide to Mosaic should be able to send all updates even when the updates were done in quick succession.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1991673

</td><td>

Add support for the Opus 4.6 model

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1991784

</td><td>

A 20,000 error occurs when the payload exceeds the input token limit for Recursive Summarization

</td><td>

 

</td><td>

1.  On latest znowassist, install the latest Gen AI controller \(13.0.0-SNAPSHOT\) and UXC \(12.0.5-SNAPSHOT\).
2.  Create an incident with 500-800 activity records.
3.  Initiate Incident summarization.

 Notice that Summarization is failing with 20,000 error.

</td></tr><tr><td>

OneExtend

 PRB1992499

</td><td>

UI automation for skill/agentic eval/custom metric features

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1992502

</td><td>

Quality improvements for performance/logging/debugging/telemetry for Autochat/Autoeval

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1993333

</td><td>

The Kafka plugin should not be enabled on the install of OneExtend for IntegrationHub ETL Consumer

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1993698

</td><td>

Link a subgraph service plan invocation to a main graph service plan

</td><td>

Currently, when users execute a skill graph that contains another subgraph \(such as, a skill having another skill as a tool and that skill as a tool has more than 1 node\), different service plan invocations are created for each graph invocation/execution, but there isn't clear way to tell the link between those invocations by looking at the one\_api\_service\_plan\_invocation table. There should be way to link them so that it would be clear and easier to debug.

</td><td>

1.  Create a skill1 with a tool.
2.  Create another skill use the first skill as a tool.
3.  Run a test.

 Expected behavior: The service plan invocation for the Skill1 tool **Parent** field should be populated with the skill2 SP invocation ID.

 Actual behavior: The **Parent** field is null.

</td></tr><tr><td>

OneExtend

 PRB1998199

</td><td>

Virtual Agent \(VA\) chat intermittently hangs with no response

</td><td>

 

</td><td>

1.  Ensure Response Streaming is enabled.
2.  Open NAVA.
3.  Enter 'Creator.'

 Notice that NAVA will get stuck intermittently.

</td></tr><tr><td>

Performance Analytics

 PRB1948103

</td><td>

After upgrading from Xanadu to Yokohama, the line chart appearance changes for the 'current year vs. last year' comparison report using data sets

</td><td>

 

</td><td>

1.  Access any Xanadu instance.
2.  Create a Line report on sys\_trend with the following:
    1.  Trend on: Created
    2.  Condition \(Dataset A –Current Year\)
    3.  Add a second dataset with the same configuration but for last year.
    4.  Condition \(Dataset B –Last Year\)
3.  Save the report.

Observe the chart appearance in Xanadu.

4.  Upgrade the instance to Yokohama.
5.  Open the same report.

 Observe the chart appearance again.

</td></tr><tr><td>

Performance Analytics

 PRB1976537

</td><td>

Incorrect Data is populated in the CDC fact table when any record is created/updated/deleted at same time

</td><td>

When the multiple updates happen during the date and time, changes are not picked up based on the latest sequence number.

</td><td>

1.  Enable NAM on indicator.
2.  Run first day and incremental jobs.
3.  Update a record multiple times for the source table of the indicator \(the date and time should be same for all the updates\).

 Observe that the latest changes are picked up from the cdc\_queue\_par based on the latest sequence number.

</td></tr><tr><td>

Performance Analytics Widgets

 PRB1967553

</td><td>

The Platform Analytics \(PA\) widget 'Word Cloud' only displays the current period \(on load\) and stops responding when selecting other periods

</td><td>

In Zurich, the PA 'Word Cloud' widgets become unresponsive when users select a new period to view. In Yokohama, the Word Cloud widget behaves as expected.

</td><td>

1.  Create a PA dashboard.
2.  Add a text widget.
3.  Select an indicator and populate the **Default** field.
4.  Submit and confirm that data is displayed.
5.  Select **Go to previous**.

 Expected behavior: The widget reloads with new data and is responsive to new changes of period.

 Actual behavior: The widget doesn't load new data and is no longer responsive.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1984668

</td><td>

There's a column filter issue in the Data Visualization library page, in which the 'Does Not contain' isn't working on the 'Owner' column

</td><td>

Applying the 'Does not contain' filter on the 'Owned by' column does not filter the records properly.

</td><td>

1.  Navigate to the **Data visualization** library page.
2.  Apply the 'Does not contain' filter on the 'Owned by' column.

 Expected behavior: All the records should be filtered by the applied filter value.

 Actual behavior: It is not filtered properly when there are multiple values.

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

 PRB1971556

</td><td>

Rich text components in the in-line dashboard editor are getting partially translated

</td><td>

It partially translates the rich text component for a few scenarios. A few words aren't translated when all should be.

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

Playbook Experience Core

 PRB1965373

</td><td>

When adding an optional activity on a playbook more than once, the playbook bugs

</td><td>

Adding a single optional activity effectively breaks playbook execution in regards to activity state logic between associated record and activity context, such as completing an associated Flow Data record leaves the corresponding activity context 'In Progress'.

</td><td>

1.  Provision an instance with the Playbook Experience plugin 28.2.1 or 28.2.2 installed.
2.  Create a playbook.
3.  Trigger this incident.
4.  Add 1 stage with any name.
5.  Add 1 instruction activity in that stage.
6.  Add an optional activity using the board view and make it available to all stages.
7.  Test the playbook.
8.  Add 1 optional activity after the existing instruction.
9.  Add again a new optional activity after the previous optional activity.

 See that the activity keeps loading and if the user refreshes, it doesn't show the same activity 2 times but instead it seems to have replaced the previous.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1967945

</td><td>

Pill picker for **Dynamic output** doesn't work for flows

</td><td>

The **Dynamic output** fields are unavailable for pill picking.

</td><td>

1.  Create a flow with dynamic outputs.
2.  Add the flow as an activity in a playbook.
3.  Add another activity.
4.  Pill pick the outputs of the activity in step 2 into step 3.

 Expected behavior: Pill picker can drill down fields of the **Dynamic output** fields.

 Actual behavior: **Dynamic output** fields are unavailable for pill picking.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1984620

</td><td>

Loading of sys\_pd\_process\_definition\_c5142dddff37e21082a8ffffffffff2d taking two hours

</td><td>

This issue occurs when upgrading Yokohama and Zurich.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1951811

</td><td>

When the user creates a project with a template, the system inserts all stakeholders defined in the table dmn\_stakeholder\_register without portfolio

</td><td>

If a portfolio exists, it should add portfolio stakeholders to the project. However, if the portfolio is null, it should not add them.

</td><td>

1.  In a Zurich instance, navigate to **pm\_project.LIST**.
2.  Select **New**.
3.  Try to create a project using the template by selecting **T****o create project from a template click here**.
4.  Use any template.
5.  **Ok**.

The project gets created to review the stakeholders related list.


 Expected behavior: The stakeholders are added those who have empty portfolio. Users can review those in the 'dmn\_stakeholder\_register' table.

 Actual behavior: This shouldn't be happening where stakeholders with empty portfolios are added.

</td></tr><tr><td>

Project Management

 PRB1976395

</td><td>

Reference qualifier behaves inconsistently in Project Workspace RIDAC risk modal

</td><td>

The **Assigned To** reference qualifier for new risks opened in the RIDAC screen of the Project Workspace fails to retrieve the SysID of the current project.

</td><td>

1.  Open the Project Workspace.
2.  Create a new project.
3.  Open the RIDAC screen for the project.
4.  Select **Add risk**.

Observe that the **Assigned To** field in the modal only lists time\_card users, regardless of project setup.

5.  Save the Risk without assigning it to anyone.
6.  Open the risk.
7.  Try to change the **Assigned To** field.

 Observe that the list is now includes more users, since current.task no longer returns null in the ref.qualifier.

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

Roles

 PRB1933185

</td><td>

Admin can't access 'Background Scripts' on partial upgrade

</td><td>

Admin access is blocked, and the user sees the 'Security Constraints' page instead.

</td><td>

1.  Log in to a Yokohama instance.
2.  As an admin user, navigate to **Background Scripts** &gt; **Scripts-Background**.
3.  Verify that the admin user has access to the 'Background Scripts' UI page.
4.  Put the instance in partially upgraded mode.
5.  Navigate to **Background Scripts** &gt; **Scripts-Background**.

 Expected behavior: The admin is able to access background scripts.

 Actual behavior: Admin access is blocked, and the user sees the 'Security Constraints' page instead.

</td></tr><tr><td>

Schedule Optimization

 PRB1985203

</td><td>

ACL issues with the Schedule Optimization \(SO\) task filter for the CSM/FSM integration for SO v1.0

</td><td>

ACL restrictions can lead to double booking.

</td><td>

1.  Verify and log canRead access to wm\_task in GraphQL resolver logic.
2.  Identify from the logs if the SO user cannot access a record/field.
3.  Review the wm\_task read ACLs installed with CSM/FSM integration plugin and for other integration plugins.
4.  Add the needed roles to the SO user as conditional plugin content.

</td></tr><tr><td>

Schedule Optimization

 PRB1986839

</td><td>

Refactor Workforce Optimization \(WFO\) API calls with Territory to improve performance for Schedule Optimization \(SO\)

</td><td>

The response times for Territory is greater than that of the assignment group, even though they contain the same users.

</td><td>

1.  Ensure Territory is installed and WFO is active.
2.  Set up a Territory and an Assignment Group with the exact same users.
3.  Set the qualifier type to 'Assignment Group'.
4.  Make a QualifierData GraphQL call for the group.

Notice the response time.

5.  Change qualifier type to 'Territory'.
6.  Make a QualifierData GraphQL call for the territory.

Notice the response time.


 Notice that when comparing the values from steps 3 and 5, the response time for Territory is far greater, even though the exact same user data is being fetched for assignment groups.

</td></tr><tr><td>

Schedule Optimization

 PRB1988877

</td><td>

Fix default skill level logic for Schedule Optimization 1.1

</td><td>

An additional validation is needed to ensure that the default skill level is returned correctly for skills.

</td><td>

 

</td></tr><tr><td>

Search Application Configurations

 PRB1949837

</td><td>

Search\_application\_admin role grants write access to sys\_dictionary through personalize\_dictionary role

</td><td>

When installing other plugins, a plugin-specific admin role was granted to the search\_application\_admin role, which granted these users the ability to write to any sys\_dictionary record through the personalize\_dictionary role. This allowed seemingly unintended write access to sys\_dictionary records.

</td><td>

1.  Log in to the instance.
2.  Create a user.
3.  Grant them the search\_application\_admin role.

Observe that they will get the personalize\_dictionary role included with it, and two base instance ACLs grant write access to sys\_dictionary through personalize\_dictionary.

4.  Impersonate a user.
5.  Attempt to change the label for any sys\_dictionary record.

 Notice that the change goes through for the sys\_dictionary record.

</td></tr><tr><td>

Service Bridge for Providers

 PRB1978019

</td><td>

Rename ServiceBridge and security fix in Yokohama and Zurich changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB1937707

</td><td>

UI Policy model pop-up shows two primary buttons

</td><td>

The UI Policy model pop-up has primary buttons in every tab. There should only be one primary button, and other buttons should be colored gray. The client script section needs to be updated to maintain uniformity across the pages.

</td><td>

1.  Log in as a Catalog Builder developer/Catalog Builder editor role user.
2.  Try to create a UI Policy using the Catalog Builder.
3.  Navigate to the **UI Policy** section.
4.  Select **Add new behavior**.

Observe that a model pop-up with four tabs opens. At the bottom, there are **Continue to conditions** and **Add behavior** buttons.


 Expected behavior: There is only one primary button, and other buttons are colored gray.

 Actual behavior: There are primary buttons in every tab.

</td></tr><tr><td>

Service Catalog Builder

 PRB1937710

</td><td>

Tool tips are missing for **UI Policy** model pop-up buttons

</td><td>

None of the buttons have tool tips. **Client Scripts** and other gray buttons also don't show any tool tips \(except the buttons on the top banner\).

</td><td>

1.  Log in to an instance using the builder\_editor or builder\_developer roles.
2.  Create a UI Policy by selecting the **Add Behavior** button.
3.  Hover over **Continue to Conditions**, **Continue to Scripts**, or **Continue to Applies To**.

 Expected behavior: All of the buttons have tool tips.

 Actual behavior: None of the buttons have tool tips.

</td></tr><tr><td>

Service Catalog Builder

 PRB1937885

</td><td>

UI policy option still shows up on questions in Catalog Builder

</td><td>

There's an option to define dynamic behaviors. Since the UI Policy creation/editing was moved to its own step, this icon should no longer appear on the question.

</td><td>

1.  Open Catalog Builder.
2.  Create or edit an item.
3.  Add a question.
4.  After adding the question, return to the 'Questions' step.
5.  Hover over the question.

 Observe that there's an option to define dynamic behaviors. Since the UI Policy creation/editing was moved to its own step, this icon should no longer appear on the question.

</td></tr><tr><td>

Service Catalog Builder

 PRB1943016

</td><td>

Stale action configurations still exist for UI policy CRP

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB1948251

</td><td>

Heading hierarchies aren't followed for the UI Policy 'Actions' tab

</td><td>

As a catalog item creator, the user should be able to add multiple action records against multiple variables in the catalog builder. This way, the user can efficiently configure complex catalog items with the necessary logic and flexibility.

</td><td>

1.  Navigate to the **Catalog Builder**.
2.  Create a catalog item using the builder.
3.  Create a couple questions.
4.  Create a UI policy and observe the 'Actions' tab.
5.  Select **Add a new action**.

 Expected behavior: It follows heading hierarchies.

 Actual behavior: The Title UI Policy height is 24px. The same height is used for the sub section 'Add New UI Policy Action', which isn't correct

</td></tr><tr><td>

Service Catalog Builder

 PRB1992076

</td><td>

Support for advanced UI policies in Catalog Builder

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1975065

</td><td>

Actions and **Sparkle** icon aren't generated for UI policy and its sub-tabs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Graph Connectors

 PRB1972771

</td><td>

A JDBC connection test times out after a Zurich upgrade

</td><td>

The JDBC Connection test times out after a Zurich upgrade. The user modified the script in the client script section of the UI page in the instance, which resolved the issue. The user is also concerned about this page customization.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1956154

</td><td>

Extra unusable scroll bars appear on all user portals when accessed from a touchscreen-enabled laptop

</td><td>

This only happens when the touch\_scroll class is added to the body element forcefully through developer tools.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1985562

</td><td>

Address issues identified during catalog embed

</td><td>

Issues include the following. The dropdown list isn't coming below the question. There's no way to select the file for attachments. For Retina icons, **Save as Draft** and the **Update Draft** icon isn't coming up. Error/info messages aren't coming when the angular widget is embedded. Upon submitting, the user isn't navigated anywhere. Options in a few dropdown lists, list collectors, reference and requested for aren't populated. A date picker isn't opening. In the case of masked input, it should 'u\_show' instead of 'show'. Unable to test 'Not available for' as when logging into Sirius as an admin. For a catalog of type KB, when selecting the article, it's redirecting to /sirius?id=kb\_article&amp;sys\_id=. The instance options aren't correctly propagated to the angular widget. An HTML question in catalog isn't coming up properly. If a widget is rendered as a question in a catalog, the widget's styles aren't applied.

</td><td>

 

</td></tr><tr><td>

Software Asset Data Import

 PRB1975879

</td><td>

PPN lookup shouldn't be performed for empty PPNs

</td><td>

If there is a corrupted PPN record where the part number value is empty, it will be returned and set in the PPN reference value.

</td><td>

Import an entitlement without a PPN.

 Expected behavior: No actions are performed using the empty PPN value.

 Actual behavior: If there is a corrupted PPN record where the part number value is empty, it will be returned and set in the PPN reference value.

</td></tr><tr><td>

Software Asset Management

 PRB1974072

</td><td>

Discovered user &gt; user\_id type is int and doesn't support all integrations

</td><td>

Sometimes user IDs are of string type. The user\_id column in the discovered user table is for external user IDs as per description, but it should be string type to provide better compatibility.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1975292

</td><td>

Contract start date parsing doesn't work as expected

</td><td>

The issue occurs when alphanumeric input is given. The **Organization ID** field should be set to read-only after successful validation.

</td><td>

1.  Open the Docusign integration profile form.
2.  Set Integration type =Org Level.
3.  Set the contract renewal date to any number.
4.  Open the Docusign integration profile form again.

Observe that the contract renewal date is checking for integers, but the functionality is different in classic and workspace. In classic, any alphanumeric value is reduced to just integers. In workspace, the value stays as-is and a warning message appears.

5.  Set Integration type =Org Level.
6.  Populate the fields.
7.  Save.
8.  Validate.
9.  Change the org ID.
10. Save again.

 Observe that the **Organization ID** field isn't set to read-only after successful connection validation.

</td></tr><tr><td>

SQL API \(Server\)

 PRB1989263

</td><td>

Cannot execute a query against a physical representation of a long table name using SqlParser in physical mode

</td><td>

SqlParser throws an exception for the long table name, when the query should instead return a response with no records.

</td><td>

1.  Create a table with a very long table name, such as u\_very\_long\_table\_name\_abcdefghijklmnopqrstuvwxyz.
2.  Send a rest request to Trino Connector API /api/now/integration/trino/query/sql?sql\_type=physical&amp;connector\_typ=loopback with body containing the following:
    -   SQL query: SELECT \* FROM.

 Expected behavior: The query returns a response with no records since the table doesn't contain any data.

 Actual behavior: The SqlParser throws an exception, 'Invalid table name.'

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

 Notice that it takes the default protocol version size because there are no parameters being set to alter the default configuration of the SSHEngine/SSHConfig from the GlideSSHSessionPool.

</td></tr><tr><td>

System Update Sets

 PRB1918257

</td><td>

When installing a product suite from the Application Manager, the app installs aren't tracked

</td><td>

 

</td><td>

1.  Create a global update set and make it current.
2.  Install a product suite.

 Expected behavior: All the installs are tracked in the update set.

 Actual behavior: Nothing is tracked.

</td></tr><tr><td>

Territory Planning

 PRB1983205

</td><td>

There are MSI issues in territory features

</td><td>

A MSI error appears in the 'Edit geography' UI in the territory console.

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1986842

</td><td>

Refactor Workforce Optimization \(WFO\) API calls with Territory to improve performance for Territory Planning

</td><td>

 

</td><td>

1.  Ensure Territory is installed and WFO is active.
2.  Set up a Territory and an Assignment Group with the exact same users.
3.  Set the qualifier type to 'Assignment Group'.
4.  Make a QualifierData GraphQL call for the group.

Notice the response time.

5.  Change qualifier type to 'Territory'.
6.  Make a QualifierData GraphQL call for the territory.

Notice the response time.


 Notice that when comparing the values from steps 3 and 5, the response time for Territory is far greater, even though the exact same user data is being fetched for assignment groups.

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

 PRB1962617

</td><td>

The plugin 'now\_assist\_context\_menu from URL /scripts/now\_assist\_context\_menu\_tinymce\_plugin.js' failed to load

</td><td>

There's an error in the log: 'This step failed because the client error 'Failed to load plugin: now\_assist\_context\_menu from URL /scripts/now\_assist\_context\_menu\_tinymce\_plugin.js'.

</td><td>

 

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

 PRB1974424

</td><td>

There's a tree picker performance issue seen with an assignment group after upgrading to Zurich

</td><td>

The load time of the page has been poorly impacted. The load time is increasing exponentially to the number of records and not linearly to it.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1976103

</td><td>

The **glide\_list** field with choices in an extension table form \(incident\) shows choices for a parent table \(task\)

</td><td>

The field type **List**' shows a parent choice list in a parent table from Zurich.

</td><td>

1.  Navigate to the **Task**' table.
2.  Create a field of type **List**.
3.  In choices, add a few random choices for parent \(task\) table and child table \(incident\).
4.  Navigate to **incident.do**.
5.  Configure the form to show the newly added **List** field.
6.  See that only choices from parent table is present in Zurich

 Expected behavior: The field type **List** shows parent choice list in the child table.

 Actual behavior: The field type **List** shows a parent choice list in the parent table from Zurich.

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

UI Field Administration

 PRB1990984

</td><td>

AI indicators should support AI gradients in UI16 and workspace

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1897661

</td><td>

Date validations don't work properly on SOW with 'Current Minute Configuration' in UI policy

</td><td>

The UI policy doesn't trigger an error on the form.

</td><td>

1.  Log in to an instance.
2.  Open Service Operations Workspace.
3.  Open a list.
4.  Create a new change request by filling all mandatory fields.
5.  Try to fill the 'Planned start date' with the current date.
6.  Try to change the current time to the past with the current date.

 Expected behavior: UI policy triggers an error on the form.

 Actual behavior: UI policy isn't triggered.

</td></tr><tr><td>

UI Form Administration

 PRB1938024

</td><td>

The 'View' context and tooltip is broken for a sn\_cmdb\_admin user

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1971158

</td><td>

A blank screen displays when a user tries to access the ast\_contract record present in another domain

</td><td>

When the user doesn't have access to the record, globals are coming as undefined, and aren't adding the default value of \{\}. This causes a JS error later in the processing, which results in the blank screen.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1972511

</td><td>

Invalid payload event for CTRL\_RECORD\#MACROPONENT\_PROPERTY\_CHANGED

</td><td>

There are properties that are defined in the CTRL\_RECORD\#MACROPONENT\_PROPERTY\_CHANGED event definition. The properties are not stored in the cached payload due to a parsing error. getProperties returns no properties due to a parsing error.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1990981

</td><td>

An alert banner in-record for Agentic Workflow updates

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1994242

</td><td>

When 'glide.ui.escape\_text' is set to false, forms break

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1947452

 [KB2601019](https://hi.service-now.com/kb_view.do?sysparm_article=KB2601019)

</td><td>

UX screen record allows the **Parent Macroponent** field to be set to the screen within the same screen collection as the current screen record

</td><td>

This results in an invalid screen configuration.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1949471

</td><td>

Users can't make the Service Operations Workspace main tab limit to open only one record, even after setting 'maxMainTabLimit' to 1

</td><td>

When users set the sys\_ux\_page\_property of workspace 'maxMainTabLimit' to 1, users are still able to open 2 tabs but not more than that. It's unclear if there's any minimum threshold the property must have.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1966630

</td><td>

Workspace tabs aren't rendering screens

</td><td>

Loading a record page via click through \(hydrate\) is missing the audience applicability check \(present in direct load\), leading to incorrect screen variant resolution.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1968071

</td><td>

Viewport content isn't refreshed if the tab is already selected before saving the record, causing the content in the tab to not populate

</td><td>

After creating a new change request and saving the record, the 'Record Information' panel doesn't reload until users switch to another tab, such as 'Recommendations' or 'Agent Assist'.

</td><td>

1.  Navigate to a Zurich instance.
2.  Open the Service Operations Workspace.
3.  Select the **+** next to the Home tab.
4.  Select **New Change Request**.
5.  Select **Normal** change.
6.  Select **Continue**.
7.  Complete the **Short Description**, **Description**, and **Justification** fields.
8.  **Save**.

Observe that the 'Record Information' panel on the right doesn't populate with data.

9.  Select **Calculate risk**.
10. **Save**.

Observe that the 'Record Information' panel on the right still doesn't populate with data.

11. Select any of the icons in the ribbon to the right of the 'Record Information' panel.
12. Select back on the **Record Information** icon in the ribbon to the right of the 'Record Information' panel.

 Observe that the 'Record Information' panel on the right now displays the relevant data.

</td></tr><tr><td>

UX Framework

 PRB1972320

</td><td>

There's an unexpected focus shift to the first focusable element on a page

</td><td>

There was a change specific to the Safari browser where anytime the screen status changed or a component was rendered, the focus would shift to the first focusable element on the page. The user was on to the top of the page on the first focusable element, which lead to the focus suddenly shifting from a part of the page.

</td><td>

1.  Log in to the affected instance.
2.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace** &gt; **Products** &gt; **Product record name**.

The 'Overview' tab is selected for the record.

3.  Try and navigate to different tabs like 'Details', 'Product Features', 'Product Enhancements', 'Versions &amp; Included products' one at a time and observe the announcement.

 Expected behavior: VoiceOver should announce the information about all the tab items in the order including their role and state information on navigation. Focus shouldn't shift to the 'Overview' tab every time a new tab is selected.

 Actual behavior: When users try to switch to a new tab, VoiceOver announces the role and state of the tab but suddenly autoshifts focus to the 'Overview' tab.

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

Virtual Agent Designer Legacy

 PRB1897174

</td><td>

Converting published LLM topics to topic blocks leaves sys\_gen\_ai\_skill records

</td><td>

The sys\_gen\_ai\_skill record remains even though it should be deleted after the LLM topic is converted to a topic block.

</td><td>

1.  Create a LLM topic
2.  Publish it.
3.  Observe that a sys\_gen\_ai\_skill record is created.
4.  Convert the LLM topic to topic block.

 Expected behavior: The topic block should never be a standalone skill, and the record from step 2 should be deleted.

 Actual behavior: The record in step 2 is still present.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1915787

</td><td>

There's a scope issue when using topic block as a tool in the AI agent

</td><td>

The AI agent internally calls the topic block 'Upload file 2', but it's not able to invoke the topic block and throws the error.

</td><td>

1.  Log in to an instance.
2.  Open the 'Testing' tab under AI agents.
3.  Test the AI agent, 'Upload attachment to the HR case'.

 Observe that it internally calls the topic block 'Upload file 2', which is used as a tool in the AI agent. It's not able to invoke the topic block and throws the error.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1964412

</td><td>

getMessage is used with an empty string when the table title is not defined

</td><td>

If the title is empty, getMessageLang shouldn't be invoked. However, getMessageLang\(\\', vaContext.getRequesterLang\(\)\) is used when the title is empty.

</td><td>

1.  Create a VA topic.
2.  Add bot response 'Table'.
3.  Leave the **Table header** field empty.
4.  Publish the topic.
5.  Open the sys\_cs\_topic file for the created topic.
6.  Check the definition.

 Expected behavior: getMessageLang isn't invoked.

 Actual behavior: getMessageLang\(\\'\\', vaContext.getRequesterLang\(\)\) is used.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1992505

</td><td>

HTML rendering issues in alert analysis

</td><td>

 

</td><td>

1.  Navigate to **Now Assist panel**.
2.  Run alert analysis.

 Notice that the response contains HTML tags.

</td></tr><tr><td>

Virtual Agent

 PRB1820705

</td><td>

Installing the plugin 'Glide Virtual Agent' \[com.glide.cs.chatbot\] throws some of the errors in the activation log

</td><td>

This issue occurs when installing Glide Virtual Agent \[com.glide.cs.chatbot\]. Errors occur related to an invalid plugin, but functionality is not affected for sys\_ux\_lib\_component\_slot and the topic\_variable table.

</td><td>

1.  Open a Washington or Xanadu base instance.
2.  Install the plugin Glide Virtual Agent \[com.glide.cs.chatbot\].

 Notice that in activation log, there are some errors related to the invalid plugin om.servicenow\_sdk\_ci and dependency unavailable. The sys\_ux\_lib\_component\_slot and topic\_variable table does not exist, and there is no functionality affected, but there are error logs in activation log.

</td></tr><tr><td>

Virtual Agent

 PRB1915355

</td><td>

Skill isn't triggered as capability in Virtual Agent Designer when tools \(such as RAG\) are added for the skill

</td><td>

A 'Runtime Exception' error appears.

</td><td>

1.  Create a custom skill with a RAG node in the flow.
2.  Create a 'sys\_one\_extend\_builder\_capability' record for the skill, with Virtual Agent Designer as the builder.
3.  Create a topic in VA that uses that capability in VA.
4.  When the capability shows up under VA capabilities, drag it into the topic.
5.  Test the topic.

 Expected behavior: The topic executes fine.

 Actual behavior: The topic errors out.

</td></tr><tr><td>

Virtual Agent

 PRB1919055

</td><td>

Add a new property to turn off the 'shorten responses' feature by default

</td><td>

After upgrading Xanadu, shorten responses were added and set as 'on' by default. There is no method to set up shorten responses to 'false' as default. The user cannot see the full test display as default as before.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1959245

</td><td>

Fluency Judge penalizes fluency for the word 'False' in the synthesized response

</td><td>

 

</td><td>

1.  Use the QnA proxy skill on Now Assist Skill kit to trigger a chat.
2.  Use aia\_artifact\_table and pick any record to generate the data from the table.
3.  Once data generation is complete, look at the generated chats in the auto\_chat\_level\_one\_result table.

 Observe the work 'False' is returned with the synthesized answer response in the conversation.

</td></tr><tr><td>

Virtual Agent

 PRB1973526

</td><td>

The business rule 'VA Phone Interaction - On Close' is not firing in the 'wrap\_up' state

</td><td>

The outcome of this issue end to end is this is causing an interaction that is intended to be closed by the agent \(so has entered wrap up\) resurfacing when the same caller makes consecutive calls before wrap up is finished.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1977262

</td><td>

Elevated roles are missing in the topic after subflow execution

</td><td>

The message says that the user has an elevated role before flow execution, but returns false for the same code after flow execution.

</td><td>

1.  Create a placeholder subflow from Flow Designer.
2.  Create a topic from Virtual Designer.
3.  Add a bot text response node to log the presence of elevated roles \(for example, '\[Pre-flow\]Has security\_admin role: '+ gs.hasRole\(\\'security\_admin'\);\).
4.  Add an action node.
5.  Call the placeholder subflow created in step 1.
6.  Add a bot text response node to log the presence of elevated roles \(for example, '\[Post-flow\]Has security\_admin role: '+ gs.hasRole\('security\_admin'\);\).
7.  Publish and promote the topic.
8.  Create a user.
9.  Assign 'security\_admin' and 'now\_assist\_panel\_user' to the user.
10. Open a new session.
11. Elevate the role.
12. Select the topic pill from the Now Assist panel.

 Observe that the text says that the user has an elevated role before flow execution, but returns false for the same code after flow execution.

</td></tr><tr><td>

Virtual Agent

 PRB1983377

</td><td>

In enhanced chat, the virtual\_agent flag is always set to false

</td><td>

In enhanced chat, the virtual\_agent flag has never been set to true. If users are starting the conversation in Virtual Agent \(VA\), irrespective of the assistant, the flag must be set to true.

</td><td>

1.  Set up NAVA with enhanced chat.
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

 PRB1985773

</td><td>

Now Assist Virtual Agent \(NAVA\) doesn't trigger the onboarding workflow

</td><td>

The onboarding workflow works as expected when running from Playground, but NAVA doesn't trigger the workflow on the journey record. An execution also doesn't appear in the sn\_aia\_execution\_plan table.

</td><td>

Generate onboarding ramp-up plan.

 Notice that it works as expected when running from Playground, but NAVA doesn't trigger the workflow when checking 'Initiate onboarding ramp-up plan' flag on the journey record.

</td></tr><tr><td>

Virtual Agent

 PRB1987536

</td><td>

Attachment upload fails for users with elevated privileges

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1988044

</td><td>

hasUnreadMessages value for conversations in the chat history widget does not matches with values in the 'Recent chat updates' widget using OffGlideScriptObject.getConversationsByConsumerAccount\(\)

</td><td>

The chat history widget 'now-lbf-chat-client' is using cache to show an 'unread' status for conversations. The 'Recent chat updates' widget is using the OffGlideScriptObject.getConversationsByConsumerAccount\(\) API to fetch the latest five active conversations from the database. The 'unread' status for conversations in both widgets do not match.

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

 PRB1988879

</td><td>

Incorrect endpoint is used for connecting to the NextWave cluster for glide

</td><td>

This issue occurs when NextWave for Microsoft Teams is set up.

</td><td>

Set up NextWave for Microsoft Teams in a deployed environment.

 Notice that requests from glide are not reaching the off glide cluster.

</td></tr><tr><td>

Virtual Agent

 PRB1989732

</td><td>

The assistant\_personalization system property should handle default case properly for branding and personalization

</td><td>

When updating the sn\_nowassist\_va.assistant\_personalization system property to a random value, it doesn't behave the same as the default value.

</td><td>

1.  Open the sn\_nowassist\_va.assistant\_personalization system property.
2.  Update the value to a random value, different from the given three choices.
3.  Run a query in the Virtual Agent portal connected to the assistant that has personalization.
4.  Navigate to the **sys\_generative\_ai\_log** table.
5.  Locate the record for either AIA Unified Planner, AIA Unified Planner Quick, or AIA Planner.
6.  Review the record and verify that the configured persona is appearing in the prompt, in between 'and'.

 Expected behavior: It behaves the same as the default value, and should return only agent\_persona from the configuration attribute table.

 Actual behavior: It behaves as TONE\_RESPONSE\_LEN\_PERSONA and returns all the details.

</td></tr><tr><td>

Virtual Agent

 PRB1989830

</td><td>

Additional assistantAttribues for Knowledge Graph NLQ: knowledge\_graph\_anchor\_tables, knowledge\_graph\_focus\_table, knowledge\_graph\_focus\_record\_id

</td><td>

To execute KG-NLQ, certain attributes are needed to be passed to the tool. Presently, AO is getting following Knowledge Graph keys in assistantAttributes: knowledge\_graph\_name, knowledge\_graph\_sys\_id, knowledge\_graph\_nlq\_schema\_sys\_id, knowledge\_graph\_nlq\_tags, knowledge\_graph\_nlq\_schema, knowledge\_graph\_tags. For Now Assist panel \(NAP\) conversation, additional attributes are required: knowledge\_graph\_anchor\_tables knowledge\_graph\_focus\_table knowledge\_graph\_focus\_record\_id. This is in parity with Glide implementation of kgnlq.

</td><td>

 

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

 PRB1991845

</td><td>

Reverting the production bot support for Google Chat while waiting for external dependency issue to be resolved

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

 Notice that the width of the window increases beyond the chat window, and the label is shown in plaint text and the link shows.

</td></tr><tr><td>

Virtual Agent

 PRB1992494

</td><td>

Now Assist Skill Kit \(NASK\) and agentic evaluations improvement

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1992496

</td><td>

In 'Bring Your Own LLM', add the ability for a user to onboard their own custom models from different providers

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1992498

</td><td>

End-to-end editing of skills in Now Assist Skill Kit \(NASK\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1992503

</td><td>

Auto-eval API updates are requested by Assistant Designer to implement Conversation Eval

</td><td>

This is a product update.

</td><td>

 

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

 PRB1992729

</td><td>

Add preferred skills handling for Open Graph \(OG\)

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

1.  Open an instance.
2.  Impersonate any user.
3.  Start a conversation in the chat interface.
4.  Observe that the conversation history shows a red dot indicator
5.  Select **Conversation History**.
6.  Verify that the conversations are displayed correctly.
7.  Navigate away by selecting **Home** or any other page in the menu.
8.  Select **Conversation History** again.

 Expected behavior: The Conversation history page should display the list of conversations for the user, consistent with the initial view before navigation.

 Actual behavior: The conversation history page displays the 'No conversations yet' message, even though the user has active conversations as indicated by the red dot.

</td></tr><tr><td>

Virtual Agent

 PRB1994599

</td><td>

Off Glide code introduced an issue for DTAC when the agent sends a message to the requester

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

Virtual Agent

 PRB1997012

</td><td>

Do not allow 'backup/fallback' URLs to be used for Glide messages sent to OGCS

</td><td>

The callback\_url and pod\_ip must be present in the tool execution request, or the Live Agent context, or the session context \(for session-related messages back to OGCS\).

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1997534

</td><td>

Survey in LLM mode errors out

</td><td>

The user gets an error after submitting a response in the pre-chat survey in Now Assist Virtual Agent \(NAVA\).

</td><td>

1.  Navigate to **sys\_cs\_survey**.
2.  Enable pre-chat and post-chat survey.
3.  Start a conversation in NAVA.
4.  Submit a response in pre-chat survey.

 Expected behavior: User is able to complete the survey with no errors.

 Actual behavior: User gets 'Sorry there was a problem on my side error.'

</td></tr><tr><td>

Virtual Agent

 PRB1999010

</td><td>

Time Out abandoned Virtual Agent \(VA\) conversation scheduled job closes the conversation in the middle

</td><td>

'Time out Abandoned VA conversation' should not close the conversation if idle time out is not completed.

</td><td>

1.  Log in as requestor.
2.  Initiate a chat. Log in as agent.
3.  Attempt to accept the chat.
4.  As the requestor and the agent are chatting, attempt to run scheduled job 'Time Out abandoned VA conversation.

 Notice that as soon as this scheduled job runs, the conversation times out even if the agent and the requestor are chatting.

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

Web UX Runtime

 PRB1983522

</td><td>

The sn-canvas-tabs component displays a record preview popup on hover that is inaccessible to keyboard and screen reader users

</td><td>

In configurable workspaces, there is a top level tab navigation region made up of the sn-canvas-tabs component. Hovering over a record tab in this region with a mouse triggers a popup to display a short preview of key fields on the record, such as a short description and state. This is crucial information for agents to quickly differentiate between multiple tabs at a glance, but keyboard and screen reader users can't trigger or access the popup. In some workspaces, an unnecessary additional tooltip appears on keyboard focus, but only repeats the record number.

</td><td>

1.  Navigate to a configurable workspace, such as Service Operations Workspace.
2.  Open at least two records \(for example, Incidents, Cases\).
3.  In the top level navigation tabs, hover over a deselected record tab.

Notice that a popup appears with a short summary of key fields for the record.

4.  Attempt to trigger the popup with a keyboard.

 Expected behavior: When a tab for a record has keyboard focus, the preview popover also appears and remains visible until the user shifts keyboard focus or dismisses the popover \(Escape key or otherwise\). Screen reader users should hear the details in the popup announced.

 Actual behavior: There is no way to trigger the popover with a keyboard alone, and the arrow and Tab keys do not trigger the popup. Screen reader users are not aware they are missing the preview popup.

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

 Expected behavior: The popup appears.

 Actual behavior: Nothing happens.

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

 PRB1973913

</td><td>

ACL restrictions can lead to double booking

</td><td>

There are ACL issues with SO task filter and CSM/FSM integration.

</td><td>

 

</td></tr><tr><td>

Zero Copy Connectors \(Glide\)

 PRB1984931

</td><td>

The WDF table throws exception when referencing glide tables with long logical table names that are greater than 30 characters

</td><td>

An error occurs when opening the WDF table and including the reference column in the list view.

</td><td>

1.  Create a glide table with more than 30 characters.
2.  Create a WDF table with a column that references a column in the glide table.
3.  Open the WDF table and include the reference column in the list view.

 Notice than an error shows on the page.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 6 Hotfix 1](zurich-patch-6-hf-1.md)
-   [Zurich Patch 6](zurich-patch-6.md)
-   [Zurich Patch 5 Hotfix 1](zurich-patch-5-hf-1-PO.md)
-   [Zurich Patch 5](zurich-patch-5.md)
-   [Zurich Patch 4 Hotfix 6](zurich-patch-4-hf-6-PO.md)
-   [Zurich Patch 4 Hotfix 3b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2774148)
-   [Zurich Patch 4](zurich-patch-4.md)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


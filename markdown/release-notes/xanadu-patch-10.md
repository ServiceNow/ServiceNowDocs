---
title: Xanadu Patch 10
description: The Xanadu Patch 10 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-08-27"
reading_time_minutes: 83
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 10

The Xanadu Patch 10 release contains important problem fixes.

-   **Xanadu Patch 10 was released on August 21, 2025.**
    -   Build date: 08-21-2025\_1913
    -   Build tag: glide-xanadu-07-02-2024\_\_patch10-08-08-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X010.00.xlsx).

## Overview

Xanadu Patch 10 includes 348problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp10.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 10 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 10, refer to [KB2428218](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2428218).

## Changes in Xanadu Patch 10

-   **[Identity Type](https://www.servicenow.com/docs/access?context=t_CreateAUser&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Use the Identity Type to define the correct identity type while creating a user. You can select **Human**, **Machine**, or **AI Agent** based on the user identity.

    The Web service access \(WSA\) only checkbox is automatically enabled for Machine identities and read-only for Human or AI Agent identities. You can mark Identity Type as **Machine** for creating WSA accounts.


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

Activity stream

 PRB1893483

 [KB2185849](https://hi.service-now.com/kb_view.do?sysparm_article=KB2185849)

</td><td>

No activity displays in UI16 when a blank journal event is added to the activity stream

</td><td>

After upgrading to Yokohama, some records display 'No Activity' on the platform view. A null pointer exception displays.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Agent Chat

 PRB1900981

 [KB2226265](https://hi.service-now.com/kb_view.do?sysparm_article=KB2226265)

</td><td>

Inbox audio is delayed when the 'Workspace' tab is inactive or out of focus before receiving the first work item

</td><td>

When the work item assigned, audio isn't heard. Audio is heard only after switching back to the workspace. The agent may not get notified at the time of assignment due to this issue, and the work item may expired by the time agent is back on the workspace tab.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1837739

</td><td>

'Physical Table Stats Gatherer' runs long due to an influx of query with hash 2136542706

</td><td>

The job runs for more than one hour. Each query takes around 239 ms but since the number of times it's being called is high, the overall job takes a longer time.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1912171

 [KB2266697](https://hi.service-now.com/kb_view.do?sysparm_article=KB2266697)

</td><td>

Yokohama MID Server upgrades do not upgrade all jar files in lib

</td><td>

Yokohama MID Server upgrades don't upgrade all jar files in lib, causing NoClassDefFoundError for various classes, and MID Server to go down.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1908169

 [KB2252998](https://hi.service-now.com/kb_view.do?sysparm_article=KB2252998)

</td><td>

An exact match for an experience with an invalid routeConfigId doesn't navigate

</td><td>

A new issue was found which results in Zing search results aren't opening properly within a workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1863573

</td><td>

A 'Scope tag not permitted' error is thrown when the UXC Generative AI plugin is active

</td><td>

The scoped UI macros are added to the UI16 form by the 'UXC Generative AI' plugin clash with scoping rules, causing a 'Scope tag not permitted' error to be thrown. Visually, users notice related lists and others macros not loading on the form.

</td><td>

1.  Navigate to sysapproval\_approver.list.
2.  Open any record still in the 'Requested' state.
3.  Right-click on the header and configure the form layout.
4.  Add the 'Test Formatter Approval Scoped' formatter to the layout after the 'Approval Summary' formatter.
5.  Configure the form.
6.  Add 1 related list to better see a broken page when reproducing.
7.  Clear the cache using cache.do.
8.  Open the record.

 Observe that the form is in a broken state. The approval \_summary form renders on the page, but everything else is missing. Related lists won't display. Users aren't able to select and hold \(or right-click\) on the header or see the scoped UI macro rendered.

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

 PRB1910480

</td><td>

Reduces ACLs generated by QueryACLAuditor for table and fields in hierarchies

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910482

</td><td>

Ensures the QueryRangeACLAuditor doesn't generate Security Attribute with blank script

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access control list \(ACL\) Rules

 PRB1910491

</td><td>

Enables QueryACLAuditor to run for a specific list of tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910494

</td><td>

Fixes QueryACLAuditor ACL generation for specific read ACL combinations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910496

</td><td>

Fixes QueryACLAuditor ACL generation for some situations involving hierarchies of tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910499

</td><td>

Augments the description of ACLs, generated by QueryACLAuditor, to classify the field ACLs retained for their datatypes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910928

</td><td>

Adds Business Rule to keep query\_range ACLs synchronized with read ACLs in case of role modification

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1918225

</td><td>

Ensures conditional\_table\_query\_range ACL customizations are honored with QueryRangeACLAuditor reruns

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1918943

</td><td>

Ensures QueryRangeACLAuditor rerun to preserve the timestamps of query ACLs created by previous audit run

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1922774

</td><td>

gen\_ai\_ prefixed ACL types should use \* ACLs for their default rule name

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1910493

 [KB2321524](https://hi.service-now.com/kb_view.do?sysparm_article=KB2321524)

</td><td>

There is slowness when loading forms with **Table Choice** fields, even after applying a 2000 record limit

</td><td>

The size of CACHE\_ARCHIVE\_TABLE\_HAS\_TERMS cache needs to be higher than 2000 since many instances have more than 1000 archive tables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Access Control

 PRB1911812

</td><td>

Ensures retain fields get the right ACLs when in table hierarchies

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1917141

</td><td>

Ensures QueryRangeACLAuditor is re-run to preserve all the query ACLs created by the previous audit run, in case of query\_range ACL customizations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1923191

</td><td>

Prevent re-generating ACLs with a different sys\_id after upgrade when ACL schema changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity stream

 PRB1743672

</td><td>

Work notes using Carriage Return aren't displaying in HR Agent Workspace when using edge encryption

</td><td>

.

</td><td>

1.  Enable Edge Encryption in the HR Workspace.
2.  Open the HR Workspace using an encrypted URL.
3.  Post a Worknote on a HR Case that uses a Carriage Return.

 Notice that the Worknote isn't visible in the Activity Log.

</td></tr><tr><td>

Activity stream

 PRB1870524

</td><td>

If user\_id is in the form of a sys\_id, then the user isn't displayed correctly in the activity stream

</td><td>

The sys\_created\_by can be a user\_id or a sys\_id or an email, so it guesses based on the format. If the user\_id is copying the sys\_id format, then this process doesn't work.

</td><td>

1.  Create a user with a user\_id in the format of a sys\_id.
2.  Give the user sufficient roles to view workspace.
3.  Impersonate the user created.
4.  Navigate to some record on workspace and add a comment or make a field change.

 Notice this user's user\_id is displayed instead of the display name.

</td></tr><tr><td>

Activity stream

 PRB1878917

</td><td>

Text doesn't persist if the user navigates away from the email composer when drafting a reply

</td><td>

Text in the email composer disappears when the user navigates to a different tab. This only occurs when replying via the activity stream tile, not when composing a new email.

</td><td>

1.  In any workspace on Xanadu or Yokohama, open an incident record and make sure to be on the 'Details' tab.
2.  Compose an email and send it.
3.  Mark the record as 'sent' in the email table so it appears on the activity stream.
4.  Select the reply icon on the activity stream email tile.

Notice that the email composer opens.

5.  Begin typing in the composer.
6.  Navigate to a different tab \(for example, 'Overview' or 'Child Incidents'\).
7.  Return to the 'Details' tab.

 Observe that the previously typed text is not displayed.

</td></tr><tr><td>

Activity stream

 PRB1881272

</td><td>

'Multiple delete' should check the condition list for archive tables

</td><td>

The 'Archive destroy' task uses multiple delete to remove sys\_journal\_field data. Users have to query the table to find which records specifically are deleted so that it can create a delete message for them. ActivityDBListener.removeMultipleEvents\(\) has to check the dbDeleteQuery. getQueryConditions\(\) for the rule's documentTable and ignore it if it isn't a table they care about.

</td><td>

 

</td></tr><tr><td>

Activity stream

 PRB1888279

</td><td>

The **Translation** button isn't turned on in a legacy Agent Workspace when dynamic translations are turned on

</td><td>

 

</td><td>

1.  Apply an update set to install, configure, and turn on dynamic translations, legacy Agent Workspace, and CSM/FSM Workspace.
2.  Open an incident in either legacy Agent Workspace \(/now/workspace/agent\) or CSM/FSM workspace \(/now/cwf/agent\).
3.  Add a comment in another language.

 Expected behavior: When hovering over the journal tile for the newly added comment, a **Translation** button should be visible and selectable.

 Actual behavior: When hovering over the journal tile for the newly added comment, there's no **Translation** button.

</td></tr><tr><td>

Activity stream

 PRB1888552

</td><td>

Attachments aren't removed from an activity stream when stored on a secondary DBI

</td><td>

In a multiple delete scenario, when the activity stream DB listener creates a DBQuery to select all activity stream records to remove, it uses the default DBQuery constructor, which selects the primary DBI by default. The DB listener needs to pass the same DBI that's used by the DB action to ensure that the correct DBI is utilized in a multiple DBI situation.

</td><td>

 

</td></tr><tr><td>

Activity stream

 PRB1895624

</td><td>

Activity stream displays sys\_id instead of the display name

</td><td>

The user's sys\_id is posted instead in the Actvity Stream event.

</td><td>

1.  Log in as an admin user.
2.  Create a new user with User ID in the format of a sys\_id.
3.  Complete the **First Name** and **Last Name** fields.
4.  Log in with new user.
5.  Navigate to **Activity stream**.
6.  Post a comment.

 Notice that the user ID \(sys\_id format\) is displayed instead of the user's display name in the activity stream event.

</td></tr><tr><td>

Activity stream

 PRB1897140

</td><td>

A workspace activity stream isn't displayed for archived records

</td><td>

Due to a misunderstanding of the requirements for archived records, a performance fix made it so that no workspace activity streams get generated for any archive tables \(for example, tables with an 'ar\_' prefix\). Instead, since archived records are read-only, all live updates for archived records should be turned off, while allowing the activity stream to be viewable.

</td><td>

 

</td></tr><tr><td>

Activity stream

 PRB1914670

</td><td>

In UI16, AI Agent posts appear as the logged-in user until the page is refreshed

</td><td>

In UI16, the entries appear as posted by the logged-in user initially. Only after a manual refresh the name changes to AI Agent. In Workspace, the entries correctly show the AI Agent as the author, which is expected.

</td><td>

 

</td></tr><tr><td>

Advanced Risk

 PRB1896933

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in Advanced Risk

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1884896

</td><td>

'Capacity' displays the incorrect value in a manual 'Allocation of Work' item from the 'Queued work' tab from Workforce Optimization

</td><td>

The user should see a list of available agents with their capacity, but instead the user always sees zero/3.

</td><td>

1.  Log in to the instance.
2.  Impersonate a user.
3.  Navigate to**Manager Workspace**.
4.  Navigate to **All agents**.
5.  Set the user presence state to 'Available'.
6.  Navigate to **Queued Work item**.
7.  Search for a document id.
8.  Select the item
9.  Select **Allocate**.

 Notice that the capacity appears as zero/3 for the user.

</td></tr><tr><td>

Agent Chat

 PRB1908263

</td><td>

Safari audio issues in inactive tabs

</td><td>

Audio doesn't work properly when the user switches to an inactive tab.

</td><td>

 

</td></tr><tr><td>

Agile Development

 PRB1909252

</td><td>

Customized story numbers are overwritten by an upgrade

</td><td>

A certain entry was offered in the com.snc.sdlc.scrum and com.snc.spm\_agile\_common packages. This entry is placed in the 'unload' folder, not the 'update' folder. Therefore, this entry becomes offending to any users who have customized it because content in the 'unload' folder is loaded during the first time activation.

</td><td>

1.  Use a Washington instance with the com.snc.sdlc.scrum plugin.
2.  Navigate to **System Definition** &gt; **Number Maintenance**.
3.  Search for the 'Story' table.
4.  Change the number of digits from '7' to '8'.
5.  Upgrade the instance to Yokohama.

 Expected behavior: The customization is retained.

 Actual behavior: The customization is reverted.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1916188

</td><td>

Update glide AI Search external content APIs to support multiple users per indexed source

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1909140

</td><td>

An API endpoint which can delete users via a GlideQuery is required for XCC

</td><td>

The XCC Scoped App can't delete users one at a time. It needs a way to query a subset of users.

</td><td>

 

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1909142

</td><td>

When a user principal is written with the DirectUserImporter and one exists, the update fails

</td><td>

Stream is wrapped mistakenly during the serialization process from a list. Not all of the principal imports do a check for the DirectPrincipalImporter vs the ImportSetImporter. The streams should be closed effectively.

</td><td>

Attempt to send a new user principal that updates an existing user.

 Updates to existing users fail. Removal of a user's group fails.

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1909146

</td><td>

The 'External Content Ingestion JS' API must do an undefined check on 'sourceId'

</td><td>

Use the newly qualified 'External Content Ingestion' APIs for ingesting principals with 'sourceId'. If 'sourceId' is undefined, see that the principals insert or updates fail.

</td><td>

 

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1909153

</td><td>

Change SOURCE\_ID\_FIELD to reference connector\_configuration\_id instead of connector\_configuration\_id\_s

</td><td>

The current licensing table process fails for some connectors because its querying the wrong field.

</td><td>

 

</td></tr><tr><td>

AI Search External User Mapping API

 PRB1913661

</td><td>

Parameters are in the wrong order when calling Java API for \(removeUser\)

</td><td>

An exception is thrown, saying that the principal ID is null. This shouldn't be the case.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1875255

</td><td>

Glide sends an 'admin' value in the **Date** field

</td><td>

There's an error in the logs.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1887375

</td><td>

'OR' conditions aren't correctly evaluated in EVAM lite

</td><td>

In SearchResultTemplateGenerator, there's logic to revert to legacy EVAM template engine if the condition is complex, but it doesn't currently catch 'OR' conditions.

</td><td>

1.  Set active=false to the Service Portal default view configuration.
2.  Search for 'IPV6' in Service Portal.

Observe that users get 1 result \(which is expected\).

3.  Modify the Service Portal 'Knowledge Search Results' view config to add 'knowledge\_base is Known Error'.
4.  Search for 'IPV6' in Service Portal.

Observe that users still get 1 result \(expected\).

5.  Add an 'OR' condition to the 'Knowledge Search Results' view config for 'knowledge\_base is IT'.
6.  Search for 'IPV6' in Service Portal.

 Observe that users no longer get the result \(not expected\).

</td></tr><tr><td>

AI Search

 PRB1889180

</td><td>

Action-type columns aren't registered on the sys\_search\_genius \_result\_event\_action table for NLQ Genius results

</td><td>

 

</td><td>

1.  Provision an instance with NLQ configured on the global search profile.
2.  Search for query-like incidents.
3.  Wait for NLQ Genius Results to load.
4.  Select **Positive feedback**buttons.
5.  Navigate to the sys\_search\_genius\_ result\_event\_action table.

 The action type column should be 'Feedback' for thumbs up and down interactions and it's not being registered on the sys\_search\_genius\_ result\_event\_action table.

</td></tr><tr><td>

AI Search

 PRB1889190

</td><td>

Shared files aren't coming up on the znowassiststable instance portal

</td><td>

 

</td><td>

1.  Open an instance with znowassiststable.
2.  Enable Dynamic Window on Portal.
3.  Set up shared files.
4.  Impersonate a user.
5.  Navigate to Service Portal.
6.  Search for 'Who is \[user\]?'.

 Notice that users can see the people card on the portal but can't see shared files.

</td></tr><tr><td>

AI Search

 PRB1892854

</td><td>

The Now Assist full-page responsive mobile is unusable

</td><td>

The pre-search box is cropped on both the left and right side. The search results search box is cropped and buttons aren't accessible.

</td><td>

Open a full page search/search results in the mobile screen size.

 Notice that the search bar is accessible when the screen size is changed to the mobile view.

</td></tr><tr><td>

AI Search

 PRB1893450

</td><td>

When there's a search application without a name, the drop-down list appears empty

</td><td>

When the user creates a search application without a name, the drop-down list for selecting search applications appears empty and displays the message 'null'.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1845187

 [KB2238953](https://hi.service-now.com/kb_view.do?sysparm_article=KB2238953)

</td><td>

Drilling down on KPIs in a Performance Analytics dashboard produces an error 'no internet connection'

</td><td>

.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1907408

</td><td>

A rollback blocking the install/upgrade for non-global scope users in a domain-separated instance

</td><td>

Non-global domain users have been blocked from being able to install/upgrade on domain-separated instances. There is now a fix to allow this behavior and hence this code change made on App Manager can now be rolled back.

</td><td>

 

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1842663

</td><td>

Persisted responders rw\_cache aren't synchronized in a cluster

</td><td>

A persisted responder for a table is cleaned up only on 2 nodes. Remaining nodes still have it in memory. Any new registration for the table on remaining nodes won't be flushed to the cluster, as they already have it in-memory.

</td><td>

1.  Use the rw\_amb\_demo.do page or use the logging responder.
2.  Have a 2 node cluster with all nodes restarted at same time.
3.  Change the property glide.record\_watcher. cleaner.orphaned\_ persisted\_responders .cleanup\_interval to 1 hour \(3600000 milliseconds\) for quick reproduction.
4.  Register a persisted responder for a custom table.
5.  Once the instance has been online for 30 minutes, then restart one node.
6.  Delete the persisted responder record from sys\_rw\_action or unregister the persisted responder to delete the record in sys\_rw\_action.

 In the next 30 minutes, observe that the cleanup runs on the other node that wasn't restarted and cleans up the custom table persisted responder from the cache. The restarted node still has the custom table persisted responder in memory.

</td></tr><tr><td>

Attachments to Records

 PRB1848449

</td><td>

The user is unable to upload an image to a field when 'glide.attachment.extensions' is not empty

</td><td>

The user is unable to upload an image to the field 'sys\_user.photo' when 'glide.attachment.extensions' is not empty an 'glide.ui.attachment.extensions.enforce' is true.

</td><td>

 

</td></tr><tr><td>

Audit Management

 PRB1896927

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in Audit Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1835271

</td><td>

IDP-initated SLO fails if 'Auto Redirect IdP' is 'True'

</td><td>

.

</td><td>

1.  Log in as an admin user.
2.  Use Azure IDP to set up Security Assertion Markup Language \(SAML\) on Service Portal \(SP\).
3.  Enable Auto to redirect IdP as 'True'.
4.  Open an incognito window.
5.  Log in to Azure IDP.
6.  Log in through an SSO user in Service Portal.
7.  Log out from Azure IDP.

 Expected behavior: The user should be logged out from both SP and IDP

 Actual behavior: The user is not logged from IDP only not from SP.

</td></tr><tr><td>

Authentication

 PRB1922769

</td><td>

Authentication agent controls

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1922770

</td><td>

Authentication agent controls

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Cache

 PRB1804575

 [KB1702700](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702700)

</td><td>

CollectingLRUCache can grow large due to fUseStats which can cause heap memory pressure

</td><td>

The memory consumption is caused by a specific cache 'syscache\_jelly\_script' which also has an internal map that stores usage statistics based on unique cache keys. In some instances with many languages, roles, domains, and unique users on a node, the count of unique keys can be very large, causing the internal usage statistics to consume enough memory to cause performance issues.

</td><td>

 

</td></tr><tr><td>

Cache

 PRB1840552

</td><td>

Reduce CPU impact from CompactCacheEntry hashCode method

</td><td>

This issue is for CompactCache CPU optimization. This was discovered from profiling, and it's a performance enhancement that improves the speed of certain cache operations and reduces the CPU cost of those cache operations.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1860702

</td><td>

The Vendor Portal 'Take-questionnaire' page stops working when the HR application is installed

</td><td>

Users observe an error on the page.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1887320

</td><td>

HTML dynamic parameters on HR templates aren't working as expected

</td><td>

HTML dynamic parameters on HR templates are not being replaced with the actual value when used in links. The issue still persists if the description contains variables only in a link.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1919807

</td><td>

Missing RCA permissions for the 'Create approval' subflow

</td><td>

This issue occurs in HR Service Delivery AI Agent Collection.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1926747

</td><td>

The vendor portal take-questionnaire page stops working when an HR application is installed

</td><td>

The user is not able to see the questionnaires associated with the assessment.

</td><td>

1.  Log in to the Instance as admin.
2.  Navigate to **All** &gt; **sn\_vdr\_risk\_asmt\_assessment.LIST** &gt; **Create new TPRA record** and save.
3.  Select **Questionnaires**.
4.  Edit the record and save.
5.  Select **Submit to third party**.
6.  Open the instance in the same browser as admin and impersonate as a third-party contact.
7.  Select **Risk assessment** for the third-party record created in step 2.

 Expected behavior: The user should be able to see and answer the questionnaires associated with the assessment.

 Actual behavior: The user is not able to see the questionnaires associated with the assessment.

</td></tr><tr><td>

Change Management

 PRB1862569

</td><td>

Change CheckConflict can cause stale reads and updates, which causes other unexpected behaviors

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1895395

</td><td>

A standard change template record producer condition builder filter operator is broken when the variable type 'List Collector' is used in conjunction with a standard change template field

</td><td>

On the 'Sample change requests' filter, after selecting a field, notice that all the operators are empty except for 'is'.

</td><td>

 

</td></tr><tr><td>

CIWF UI Component

 PRB1894610

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for portal\_knowledge\_quick\_links widget

</td><td>

 

</td><td>

 

</td></tr><tr><td>

CMDB Query Builder

 PRB1791382

 [KB1695381](https://hi.service-now.com/kb_view.do?sysparm_article=KB1695381)

</td><td>

CMDB Query Builder results' count isn't consistent

</td><td>

There's a missing result from the CMDB Query Builder query. This causes missing some records in the result with a default batchsize \(100\) without the user knowing they are missing the records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

CMDB Workspace

 PRB1894924

 [KB2181389](https://hi.service-now.com/kb_view.do?sysparm_article=KB2181389)

</td><td>

Remove CUD access to sn\_cmdb\_editor roles on cmdb\_ci records

</td><td>

Users with the role 'sn\_cmdb\_editor' shouldn't be able to have access to the cmdb\_ci table and edit the records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Column Level Encryption

 PRB1820743

</td><td>

Inactive caller policy records shouldn't be used when fetching a list of available crypto modules

</td><td>

This problem only applies to fields configured with multi-module EFCs where the field is empty or populated with cleartext data. When determining read/write access on a CLE field, available CLE crypto modules are checked to see which modules the user has access to. When building the list of crypto modules, use the query for caller policy records to find the modules. However, inactive caller policy records aren't filtered out.This causes no visible issues or access issues for users. In cases where there are many inactive caller policy records, this causes a performance issue and slows down the read/write check.

</td><td>

1.  Create a crypto module 'no\_access\_module'.
2.  Add one or more INACTIVE caller policy records for this crypto module.
3.  As a user with elevated privileges, run the crypto module script via background scripts: gs.log\(Packages.com.glide.kmf. callerpolicies.KMFCallerAccessPolicy RecordInterface.getCLECrypto ModulesFromCallerPolicyTable\(\)\);

 Expected behavior: no\_access\_module doesn't show up in the list.

 Actual behavior: no\_access\_module shows up in the list.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1825003

</td><td>

A submission through the API with the patch method doesn't work as expected for the Portuguese language

</td><td>

The user observes a response code of 403 when a patch is triggered on a Portuguese language instance.

</td><td>

1.  Provision an instance in Brazilian Portuguese.
2.  Create a CI in cmdb\_ci\_service\_auto table.
3.  Using form view, set the following values for this CI:
    1.  life\_cycle\_stage: 'Design'
    2.  life\_cycle\_stage\_status: 'Design'
    3.  install\_status: 'Pending Install'
4.  Navigate to Rest API Explorer and ensure the language is set to English.
5.  Select **Patch**.
6.  Select The sys\_id of the record created in step 2.
7.  Repeat step 2 to reset the values in form view.
8.  Change the language to Brazilian Portuguese and trigger the Patch call with the same payload.

 Observe a response code of 403.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1847131

 [KB1885852](https://hi.service-now.com/kb_view.do?sysparm_article=KB1885852)

</td><td>

The Related List condition is not used during task generation

</td><td>

CMDBScriptableAPI isn't honoring the related list condition that is stored in the encoded query field of the policy record. If the condition stored in the policy record is used in a background script, the correct count of configuration items \(CI\) comes back, so it has to be localized to the java function creating the tasks.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1893434

</td><td>

A11y bug fixes on CMDB Workspace

</td><td>

Info tooltips are identified by screen readers as 'Search Button' and there's multiple H1 elements on a page.

</td><td>

Issue 1: Info tooltips are identified by screen readers as 'Search Button'.

 1.  Start JAWS.
2.  Navigate to **Home** &gt; **All** &gt; **CMDB Workspace** &gt; **Management tab**.
3.  Move the input focus to the the info icon in excluded CIs.

 Note that the info tooltip is described as 'Search button'.

 Issue 2: Multiple H1 elements on the page.

 1.  Navigate to **Home** &gt; **All** &gt; **CMDB Workspace**.
2.  Start NVDA.
3.  Display the speech viewer in NVDA.
4.  Navigate through the page's headings.

 Notice that there are two H1s when there should only be one.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1895194

</td><td>

Multi-source doesn't set the domain path

</td><td>

If domain separation is turned on, multisource code sets the **sys\_domain** field explicitly using the logged in user's domain. However, the sys\_domain\_path is not set correctly \(default value '/' is set\). This happens because it calls setSystemFields\(\) on the corresponding DBAction before setting the sys\_domain.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1899149

 [KB2290506](https://hi.service-now.com/kb_view.do?sysparm_article=KB2290506)

</td><td>

Remove sn\_cmdb\_admin from itil\_admin, sn\_cmdb\_editor from itil, and add CUD access to sn\_cmdb\_admin / sn\_cmdb\_editor

</td><td>

An itil user should have CUD access by default and users with the itil role contains sn\_cmdb\_editor, not sn\_cmdb\_user. Remove CUD from itil, and a user with the itil role no longer has CUD access because of removing CUD from sn\_cmdb\_editor.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1909506

</td><td>

Database performance is impacted due to the ASYNC: Script job

</td><td>

De-duplication template APIs fetch unnecessary data which slows down queries, impacting database performance.

</td><td>

1.  Create a de-duplication template for any class \(for example, Linux Server\).
2.  Select the default options for Main CI, Merge Attributes, Merge Relationships, Merge Related Items and Duplicate CI Actions.
3.  Save and publish the template.
4.  Manually add de-duplication tasks to the template \(if there are no matching tasks found\).
5.  Run the template.

 Observe slow queries during the template run.

</td></tr><tr><td>

Content Experiences

 PRB1895347

 [KB2289855](https://hi.service-now.com/kb_view.do?sysparm_article=KB2289855)

</td><td>

Topic header banner images aren't displaying for users without elevated privileges

</td><td>

This happens when 'Schedule Content' records reference pointers for a widget instance \(sp\_instance\) are broken, such as when the widget instance was deleted on the instance. With these schedules in this state, the topic header widget is somehow matching to the blank **sp\_instance** field and triggering the altered UI instead of the banner.

</td><td>

1.  Create a 'Schedule Content' \[sn\_cd\_content\_visibility\] record.
2.  Select a widget instance \[sp\_instance\].
3.  Save the 'Schedule Content' record.
4.  Delete the widget instance.
5.  Open an Employee Center page \(topic\) with a banner image.

 Expected behavior: A banner image displays for all users.

 Actual behavior: A banner image doesn't display for users without elevated privileges.

</td></tr><tr><td>

Contextual Search

 PRB1868773

</td><td>

canWrite on GlideElement for variable sets returns a null pointer exception

</td><td>

There's an issue calling a canWrite on a variable set when applying form changes to be filtered. The individual variables behave correctly.

</td><td>

 

</td></tr><tr><td>

Customer Service Management for Field Service Management

 PRB1836273

</td><td>

My task map, my SLA map, agent map does not work for wm\_dispatcher due to a missing ACL

</td><td>

When a dispatcher navigates to a work order task assigned to someone from the dispatcher's group and selects 'View task on map, the map renders but the task is not shown on the map.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1894406

</td><td>

SQL error messages can't be enabled

</td><td>

If glide.db.loguser is set to 'false' by running the background scripts 'gs.setProperty\('glide.db.loguser', false\)', then only one error message appears. If glide.db.loguser is set to 'true', two error messages appear.

</td><td>

1.  Run the background script 'gs.setProperty\('glide.db.loguser', true\)'.
2.  Create a table by creating a record in the sys\_db\_object table.
3.  Navigate to the sys\_db\_object record in that table.
4.  Create a column with the type 'Auto Increment' in the Columns section.
5.  Create a new record on the table, for example put the value '1' in the new column.
6.  Create a new record with the same value.

 Expected behavior: Two error messages appear when the user should only receive one; 'Unique Key violation detected by database \(\(conn=493\) Duplicate entry '1' for key 'PRIMARY'\)' and 'Invalid insert'.

 Actual behavior: Only one error message is shown, 'Invalid insert'.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1810466

</td><td>

Physical Table Stats Table \(sys\_physical\_table\_stats\) doesn't have a cleanup mechanism that retains the table stats records daily after Xanadu changes

</td><td>

A rule will be implemented similar to the one for sys\_db\_size\_stats for sys\_physical\_table\_stats using sample\_period\_start and sys\_created\_on, or sys\_updated\_on.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1913617

</td><td>

Turn off monthly and yearly stats aggregator jobs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1793385

</td><td>

Sys\_attachment and sys\_audit aren't found when probing during SQLTableAccessibilityChecker

</td><td>

When the user moves sys\_attachment/sys\_audit to gateway and starts glide, a message appears in the console that reads '\(table\) is not on a gateway or missing, skipping the probe'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1824916

</td><td>

Query rewrites don't apply on already optimized queries by union optimization or left join coercion

</td><td>

When implementing the query rewrite for an optimized query, it doesn't apply as a query rewrite applies prior to the optimization.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1840823

</td><td>

Temporary files are left by PG-JDBC driver

</td><td>

There must be obsolete .trs files in /glide/nodes/nodeport/tmp directory. Obsolete files are created 1 hour ago or before and not touched.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1898714

</td><td>

A connection becomes vulnerable to sharing when it's marked for recycle

</td><td>

When a connection is marked for recycle, it's returned to the pool and can be picked up for allocation, where it's marked as 'Assigned'. The connection is checked for recycling and a new physical connection is established. Glide marks the connection as 'Available', which allows it to serve other requestors in the pool, causing connection sharing.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1919500

</td><td>

It takes a long time to recognize the 'DB is down' event

</td><td>

This applies to both PG and MariaDB when the primary database is brought down unexpectedly.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1921155

</td><td>

TableThrottler is broken

</td><td>

TableThrottler is broken due to the removal of lastLag and lastSleepFactor.

</td><td>

 

</td></tr><tr><td>

Declarative Actions

 PRB1839321

</td><td>

Customize flow on the 'Order' line item loads a blank screen for Order Agent/Order Admin users

</td><td>

When selecting the Customize flow action on a newly created 'Order' line item for a given Order, the page fails to load.

</td><td>

 

</td></tr><tr><td>

Declarative Actions

 PRB1914488

</td><td>

The ai-sparkle-icon doesn't animate when 'animate icon' is set to 'true'

</td><td>

This issue also occurs when setting it on the **Split** button, Related list actions, field decorator, layout items, and m2m layout items.

</td><td>

1.  Navigate to a List Declarative Action.
2.  Set the **Icon** field to 'ai-sparkle-fill'.

Notice that the **Animate icon**checkbox appears.

3.  Check the checkbox.
4.  Navigate to a list.

 Notice that the AI sparkle icon is present but doesn't animate.

</td></tr><tr><td>

Discovery

 PRB1791510

 [KB1718735](https://hi.service-now.com/kb_view.do?sysparm_article=KB1718735)

</td><td>

Discovery is hanging for certain schedules due to WMI queries failing

</td><td>

Running Discovery on Windows devices causes WMI queries to fail in Windows OS Patterns.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1800638

</td><td>

Preventing the scenario of running Simple Network Management Protocol \(SNMP\) GetNext on the same Object Identifier \(OID\) repeatedly

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1812384

 [KB2234218](https://hi.service-now.com/kb_view.do?sysparm_article=KB2234218)

</td><td>

Inclusion pattern discovery fails with a NullPointerException if one of the identifications fails for a parent pattern

</td><td>

When the main pattern identification fails, a NullPointerException exception is thrown: 'com.snc.sw.exception. PatternDebuggerException: Debug task failed to initialize parent CI for entry point: null.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1898292

</td><td>

A Discovery monitoring job should support event framework

</td><td>

Discovery to not use sys\_trigger directly, but instead utilize Platform's event framework to distribute the load among nodes.

</td><td>

1.  Make sure Discovery is using Platform's event framework \[discovery.use.event.processing system property\].
2.  Start a status and make it stuck.

</td></tr><tr><td>

Discovery

 PRB1899276

</td><td>

The start of the next Discovery schedule in a daisy chain is delayed by the time taken to complete 'discovery.complete' or 'discovery.cancel' events

</td><td>

In instances where the daisy chain is being used, the start of the next Discovery in the chain depends on the time taken to complete 'discovery.complete' or 'discovery.cancel' events. Most of the script actions for these events in their environment have the same default execution order of 100, including 'Discovery Run Next', which triggers the next Discovery. The more script actions with the order 100, the higher the possibility of delay for starting the next Discovery.

</td><td>

1.  Create a daisy chain for Discovery.
2.  Create script actions for discovery.complete and discovery.cancel events with execution order '100', which takes a few minutes to complete.
3.  Run the daisy chain for Discovery and check the time spent between the complete/cancel of one discovery schedule and the start of the next Discovery schedule.

 Notice that it is greater than the time taken by the new script actions.

</td></tr><tr><td>

Discovery

 PRB1899547

</td><td>

Make error suggestions clearer and link them to useful Knowledge Base \(KB\) articles

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1837244

</td><td>

Integration flows don't open in flow designer in the Now Assist admin document Extraction Skill

</td><td>

 

</td><td>

1.  Provision an instance with the the app-now-assist-admin app installed.
2.  Navigate to **Now assist Admin** &gt; **Feature** &gt; **DocIntel Skill** &gt; **Platform** &gt; **Q&amp;A**.
3.  Create a new use case with the target table 'Answer' and add fields with target fields.
4.  Save.
5.  Upload the document and add the integration flows Process Task and Extract Value.

 Notice that the flows are not created.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1838171

</td><td>

Duplicate names are allowed for the Q&amp;A use case from Now Assist admin

</td><td>

Duplicate names shouldn't be allowed.

</td><td>

1.  Provision an instance with the app-now-assist-admin app installed.
2.  Navigate to the **Now Assist Admin** &gt; **Feature** &gt; **Platform** &gt; **DocIntel Skill** &gt; **Documentation Q&amp;A**.
3.  Create a new use case with 'Usecase1'.
4.  Create another use case with the same name.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1839797

</td><td>

Users should be able to delete the fields under 'Data Extraction' and 'Q&amp;A Capabilities'

</td><td>

 

</td><td>

1.  Install the latest DocIntel app and Gen AI app.
2.  Create a use case under 'Data extraction' or 'Q&amp;A'.
3.  Create some fields.

 Expected behavior: The user should be able to delete the fields.

 Actual behavior: The user is not able to delete the fields.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1846148

 [KB1924055](https://hi.service-now.com/kb_view.do?sysparm_article=KB1924055)

</td><td>

Fields under table field group are not created for Document Extraction Capability

</td><td>

During the installation process, descriptions are mandatory for fields but not for field groups. However, when attempting to create a field group without providing a description, the user is blocked due to a mandatory description business rule applied to both fields and field groups.

</td><td>

1.  Navigate to **Now Assist Admin** &gt; **Features**.
2.  Select **Platform** &gt; **Document Intelligence**.
3.  Select **Document Extraction**.
4.  Create a Use case UC1.
5.  Create two fields under UC1.
6.  Fields are displaying under UC1.
7.  Create a table field group and create some fields under that field group.

 Expected behavior: Created table fields are displayed.

 Actual behavior: Table fields are not displayed.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1848551

</td><td>

Restricting the user from adding more than 150 fields for GenAI tasks

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1853246

</td><td>

Erroneous upgrade of Gen AI use cases

</td><td>

 

</td><td>

1.  Create a new Gen AI use case using Now Assist Document Intelligence.
2.  Run the upgrade job.

 Observe that use case gets upgraded when it shouldn't be.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1855732

</td><td>

DocIntel is not working properly after being trained

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1896682

</td><td>

Create a system property for max page and max field limits for GenAI use cases

</td><td>

Currently, the max page and max field limits are not customizable.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1897412

</td><td>

Enable field group name update using Glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1925940

</td><td>

The File Upload tool gets stuck at the 'Extracting data' stage

</td><td>

The file gets stuck in the 'Extracting data' stage.

</td><td>

1.  Create a new AI Agent and add the File Upload tool.
2.  Add any PDF file and save.

 Expected behavior: The file extraction should move to a 'Completed' state.

 Actual behavior: The file is stuck in the 'Extracting data' stage.

</td></tr><tr><td>

Document Viewer

 PRB1793774

</td><td>

Nodes fail to synchronize after restart

</td><td>

After restart, nodes fail to synchronize and display the message 'Could not define Scriptable class DocumentPermalink for extension point.' A code stack repeats and causes stackoverflow.

</td><td>

 

</td></tr><tr><td>

Dynamic Translation for Virtual Agent

 PRB1884635

</td><td>

Cached dynamic translations are not cleared when exclusion framework is disabled/enabled

</td><td>

Excluded terms in a new utterance are translated when the cache should have been cleared.

</td><td>

1.  Disable Exclusion Framework via the sn\_dt.dynamic\_framework.enable\_exclusion\_framework system property.
2.  Translate something with excluded terms 'The words apple and \(dog\) should not be translated.'
3.  Enable Exclusion Framework via the sn\_dt.dynamic\_framework.enable\_exclusion\_framework system property.
4.  Translate the same utterance with excluded terms.

 Expected behavior: Excluded terms in the utterance are not translated 'Las palabras apple y \(dog\) no deben traducirse.'

 Actual behavior: Excluded terms in the utterance are translated 'Las palabras manzana y \(perro\) no deben traducirse.'

</td></tr><tr><td>

Dynamic Translation

 PRB1899459

</td><td>

Dynamic Translation isn't working after upgrading in Yokohama

</td><td>

The translation feature stopped working and is now throwing the following error in 'Translate Text': 'Error: Cannot read property 'status' from undefined. Detail: Cannot read property 'status' from undefined.'

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1764089

 [KB2191121](https://hi.service-now.com/kb_view.do?sysparm_article=KB2191121)

</td><td>

The display\_ name email address set on 'Select From List' or 'text' of 'From Generation Type' doesn't work if the template is custom table based

</td><td>

When using two email templates, the oldest one gets 'error invalid' from the address when the email is sent. This error occurs when two email templates are on the same table but are from different addresses. Both email templates work if the 'from' address is set to the same value.

</td><td>

1.  Open a record in the Agent Workspace.
2.  Navigate to **Activity**.
3.  Select **Reply** on the most recently received email.
4.  Select the tab 'Pop-up email draft to new workspace'.
5.  Select **Email template**.
6.  Choose an email template.

 Notice the display\_ name format and the error message, 'The email address in the From field is invalid.'

</td></tr><tr><td>

Email Notifications

 PRB1774019

</td><td>

The Document Viewer in the Email Viewer in Workspace doesn't display certain file types

</td><td>

The document viewer does not display certain file types, including .xlxs, .docx, and .ppt.

</td><td>

1.  Open CSM/FSM configurable workspace.
2.  Open any case.
3.  Expand the contextual side panel and select the **Attachments** component.
4.  Select each of the files.

Notice that they all open in the document viewer perfectly for all file types.

5.  Select the 'Emails' tab \(related list\) and open the email record.

Notice that the attachments are displayed along the top of the record.

6.  Select the attachments.

 Notice that PDF and JPG open in the viewer, but the .xlxs, .docx, and .ppt file types display an 'Unsupported' message.

</td></tr><tr><td>

Email Notifications

 PRB1803431

</td><td>

The display\_ name email address set on 'Select From List' or 'text' of 'From Generation Type' isn't working if the client template's sender configuration is customized across multiple templates of the same table

</td><td>

An error occurs even though the display\_name format is confirmed.

</td><td>

1.  Open a sn\_customerservice\_te based record on the Agent Workspace.
2.  Select **Reply** in 'Activity' on the most recently received email.
3.  Select **Pop-up email draft to new workspace tab**.
4.  Select **Email template**.
5.  Choose **Email TE Requested for - PAR**.

 Notice that even though the field is visible to confirm the display\_ name format, the error 'The email address in the From field is invalid' still occurs.

</td></tr><tr><td>

Employee Profile

 PRB1895944

</td><td>

Encryption of attachments by users with the 'sn\_employee.admin' role after upgrading to Xanadu

</td><td>

Attachments are encrypted by 'sn\_employee.legal\_name\_for\_employee\_profile' Crypto Module. As a result, when users without 'sn\_employee.admin' role access these attachments, they get an error.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1867782

</td><td>

Slow EM Events processing due to the default value for 'evt\_mgmt.max \_characters\_in \_additional\_info' is too low

</td><td>

When there are many events with addional\_info length &gt;600,000 characters, events processing becomes slower.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1872971

 [KB2060302](https://hi.service-now.com/kb_view.do?sysparm_article=KB2060302)

</td><td>

Tag-based groups can include alerts which don't match the rule's filter

</td><td>

In the Xanadu release, a new tag-based alert correlation mechanism was introduced using the 'Query' job \(via the Service Analytics RCA/Alert Aggregation job\). There's an issue where alerts matching different tag-based definitions may not be grouped correctly if they arrive close together in time.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1877169

 [KB2096192](https://hi.service-now.com/kb_view.do?sysparm_article=KB2096192)

</td><td>

Event Management Events in certain buckets are stuck in 'Ready' for hours after migrating

</td><td>

.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1891871

</td><td>

em\_events with the Resolution state 'Closing' aren't processed correctly during the CEST clock change window

</td><td>

em\_events with the Resolution state set to 'Closing' aren't processed correctly when their timestamp falls during the CEST clock change window. This results in the alert remaining open even though the closing event is received.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1904735

</td><td>

Existing enrich rules have changes that affect binding \(draft rules\)

</td><td>

The bind simulation presents an incorrect result.

</td><td>

 

</td></tr><tr><td>

Field Service Marketplace

 PRB1874290

</td><td>

The 'Add Contractor' action is still active in lane 2 of the playbook even after moving it to lane 3

</td><td>

The issue is reproducible in Yokohama and Xanadu.

</td><td>

1.  Provision an instance with the Contractor Management and Marketplace Plugins installed.
2.  Log in as wm\_dispatcher.
3.  Create a work order task \(WOT\) in Workspace.
4.  Push to marketplace.

 The user lands on playbook experience where in the lane 1 request is created. In lane 2, after selecting contractors and moving to lane 3, if the user navigates back to lane 2, the **Add Contractor**action is still active. But when selected, it throws an error.

</td></tr><tr><td>

Field Service Marketplace

 PRB1895775

</td><td>

'Add contractor' isn't turned off in playbook lane 2 and lane 3 after the status is complete for that lane until the page is refreshed

</td><td>

 

</td><td>

1.  Create a task.
2.  Push to MP.
3.  In lane 2, select **Contractors**.
4.  Push the request.

It redirects to lane 3.


 Notice in lane 2, **Add Contractor**is still enabled until the page is manually refreshed. Similarly on lane 3, **Add contractor**is enabled even after selecting the **Close response**window.

</td></tr><tr><td>

Field Service Task Bundling

 PRB1888651

</td><td>

'Add to Bundle' fails on the latest 28.x DWS

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Field Service Task Bundling

 PRB1898283

</td><td>

Dynamic Bundling logs aren't accessible to the wm\_admin persona

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1893452

</td><td>

AI Agent context isn't properly configured for quick flows

</td><td>

The JSON structure has changed for the Attributes column of the Flow Engine Context \[sys\_flow\_context\] table. As this is an internal system field, the JSON structure may change in future releases. Avoid building custom business logic that depends on the current JSON structure.

</td><td>

Update FlowUserAgentContextIT.java to accurately count the audit.

 Expected behavior: Quick flow tests in FlowUserAgentContextIT pass.

 Actual behavior: Quick flow tests in FlowUserAgentContextIT are failing.

</td></tr><tr><td>

Flow Engine

 PRB1910437

</td><td>

Add a script for GenAI app BUs to create flow and action ACLs

</td><td>

A script utility was removed from the Flow AI Access Control effort that would create the flow or flow\_action access control rule. That utility has been readded.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1922772

</td><td>

Apply agent filters for flows that run as the user who triggered the flows

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1816646

</td><td>

The update number on the record remains the same when it is updated by the subflow and parent flow in sequence, causing inconsistencies in SLA executions

</td><td>

When the subflow updates the trigger record, and parent flow updates the same trigger record, the update number on the trigger record remains the same. This impacts respective SLA executions on the record.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1891084

</td><td>

Alias override mappings for V2 action instances aren't captured in flow update XML

</td><td>

This issue was caused by the introduction of JSON save on action instances. The FlowDesignerSychnronizer isn't syncing related records for V2 action instances.

</td><td>

1.  Ensure glide.flow.version != '1'.
2.  Provision an instance with the ID com.glide.hub.integrations.enterprise plugin installed.
3.  Add an outbound connection for the spoke being used.
4.  Create a flow.
5.  Add either the **Create a Container**action or some other action with a 'connection' action property.
6.  Pick the connection from step \#1 as the 'Docker Connection' on the 'Create a Container' action instance just added.
7.  Save the flow.
8.  Look for the most recent sys\_update\_xml for the flow.
9.  Open the XML viewer for the **sys\_update\_xml**payload field.

 Observe that the sys\_hub\_alias\_mapping is missing.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1921403

</td><td>

Tools \(actions/subflow\) do not honor ACLs/Roles if the Agent ACL is successfully validated

</td><td>

When a tool inside AI agent is executed with certain roles and its internal\_name does not match the display name, it does not honor the ACL/role and proceeds with execution.

</td><td>

1.  Create an Agent.
2.  Add a tool, such as an action with an internal\_name that is different the display name.
3.  Create an ACL for that tool with an internal\_name and a dedicated role.
4.  Execute the agent for a user who does not have the required role.

 Notice that the tool works even though it shouldn't.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1922818

</td><td>

Customer Service Spoke flows are missing an internal name

</td><td>

Most of the Customer Service Spoke flows don't have internal names.

</td><td>

 

</td></tr><tr><td>

Form Controller

 PRB1862546

</td><td>

Form with a single field of the type 'HTML' can't be aligned with the title because it has margin that can't be removed

</td><td>

The form component doesn't align with the stylized text component.

</td><td>

1.  Create a new page in UI Builder.
2.  Add a stylized text component.
3.  Add a form component pointing to a table + view that shows only one field of the type 'HTML'.

 Expected behavior: The form component left-aligns with the previous component.

 Actual behavior: The form component doesn't align.

</td></tr><tr><td>

FX Currency Conversion

 PRB1861950

 [KB1962510](https://hi.service-now.com/kb_view.do?sysparm_article=KB1962510)

</td><td>

Daily currency rates retrieval from European Central Bank \(ECB\) may fail due to a lack of response from an Online Certificate Status Protocol \(OCSP\) endpoint

</td><td>

The 'Retrieve System Rates' and the 'ECB Exchange Rate Load' jobs, which are used to capture currency exchange rates using the ECB endpoint, are failing intermittently across multiple instances because the OCSP endpoint for ecb.europa.eu isn't answering validity questions during certain times.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

GRC: Business Continuity Planning

 PRB1897810

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Business Continuity Planning

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Continuous Authorization and Monitoring

 PRB1893692

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Continuous Authorization and Monitoring

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Metrics

 PRB1894403

</td><td>

When EBA is enabled, a query range isn't working on the 'Threshold' table due to a 'deny unless' ACL

</td><td>

It throws an error, but it should be able to query the records if the user has access.

</td><td>

1.  Log in as a ESG user to the latest main instance.
2.  Open the 'Threshold table list' view.
3.  Try searching thresholds by query range.

</td></tr><tr><td>

GRC: Operational Resilience

 PRB1896635

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Operational Resilience

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Privacy Management

 PRB1900172

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Privacy Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Profiles

 PRB1894767

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Profiles

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Risk Shared Common Components

 PRB1897619

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in GRC: Risk Shared Common Components

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1898736

</td><td>

The host name resolution for IPKI certificate generation isn't successful when the instance is using an alias

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1892046

</td><td>

The auto-resize limit doesn't work when the text area is read-only

</td><td>

There's a 'now-textarea' read-only component that the user is using on a regular workspace page. The user wants to expand the text area's height, but that is only possible through the 'rows' property. The user is currently using the 'autoresize' and 'autoresizeRowsLimit' properties. However, since the field is read-only, the height of the text area isn't expanding. When they use an existing template from the UI Builder page, there's no way to directly change the property of the 'now-textarea' component. If it was a regular empty UIB page, the user would have been able to change the 'rows' property.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1874464

</td><td>

The 'Suspended Reason' is overwritten with its previous value when the case moves from 'Draft' to 'Suspended state'

</td><td>

The issue is only reproducible when: the state moves directly from 'Draft' to 'Suspended', on HR Agent Workspace and not on UI16, and when the '**Suspended reason**' \[sla\_suspended\_reason\] field is on the form.

</td><td>

1.  Log into an instance.
2.  Impersonate a system administrator.
3.  If the **Suspended reason** \[sla\_suspended\_reason\] field isn't on the HR Case 'Workspace UIB' view, add it to the form.
4.  Open HR Agent Workspace.
5.  Create an HR Case with the HR service 'General Inquiry'.

Notice how the **Suspended reason** field displays as 'User' but it's empty.

6.  Manually set the **State** field from 'Draft' to 'Suspended'.

A pop-up window displays.

7.  On the modal, set the reason to 'Group', add work notes.
8.  Select **OK**.

 Expected behavior: The 'Suspended Reason' should be 'Group'.

 Actual behavior: The 'Suspended Reason' is set to 'User'.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1897036

</td><td>

NACM auto-grow functionality doesn't work correctly for Hebrew language content

</td><td>

Selected text is incorrect and elaborate/shorten is done on empty text. When the default preset action is present along with preset actions, the user doesn't see a preset menu and instead sees a default preset action.

</td><td>

 

</td></tr><tr><td>

HTML Sanitizer

 PRB1840143

</td><td>

OpenITTicket-Web Client gets the sanitization message, 'You have inputted sensitive information and it has been cleared from the chat history'

</td><td>

This issue is observed intermittently while using Web Client.

</td><td>

1.  Setup OpenItTicket.
2.  Publish the Open IT Ticket 2.0 \(Template\) topic.
3.  Launch the Web Client.
4.  Enter 'Open' from keyboard.
5.  Select **OpenITTicket 2.0 Template Topic** from the topic picker.
6.  Enter the short description 'Issue With machine'
7.  Select **No**.
8.  Select **Urgency**.

 Notice the sanitization message, 'You have inputted sensitive information and it has been cleared from the chat history'.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1884096

</td><td>

When a consumer replication set is created, the replication entry should have 'Preserve Modified By' set to true

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1867967

</td><td>

Connection URL populates incorrectly for JSON import

</td><td>

This occurs with Spoke Generator version 4.0.3

</td><td>

1.  Navigate to Flow Designer.
2.  Open any spoke from integrations.
3.  Navigate to **Actions** &gt; **Create Action** &gt; **Postman Collection** &gt; **Import new** &gt; **Import from JSON manually**.
4.  Import the JSON file.

Notice that the postman collection is populated.

5.  Select **Create New** for Connections and Credential Alias.
6.  Give any name.
7.  Create it.

Notice that the Connection URL is populated.

8.  Fill in any API key.
9.  Select **Submit**.
10. Select **Generate operations**.
11. Ensure published and draft actions are able to be created.

 Notice that connection URL populates incorrectly for JSON import.

</td></tr><tr><td>

Internal Platform Security Services

 PRB1813597

 [KB1790767](https://hi.service-now.com/kb_view.do?sysparm_article=KB1790767)

</td><td>

There's a MIME type check error when attaching a txt \(sjis code\) file after upgrading to Xanadu

</td><td>

MIME Type check error: '\[File type not permitted or mime type does not match the file content\]'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1698906

 [KB1633481](https://hi.service-now.com/kb_view.do?sysparm_article=KB1633481)

</td><td>

The Workbench license consumption breakdown list view changes when the software product life cycle report changes

</td><td>

Editing columns in the Software Asset Workspace License Usage Report updates columns on the related lists.

</td><td>

1.  Log in to an instance.
2.  Navigate to the **Software Asset \(SAM\) Workspace**.
3.  Navigate to **License Usage** &gt; **Microsoft** &gt; **SQL Server** &gt; **Standard**.
4.  Select **License Metric Results**.
5.  Select the number link for the 'License required' column.
6.  Open the side view by selecting the number link for any 'License required' column.
7.  Select **Reports** &gt; **Software Product Lifecycle Report**.
8.  Change the column in the list view.
9.  Add some columns.
10. Refresh the License Consumption Details and Software Install Licensing.

 Notice that the details do not render in the table.

</td></tr><tr><td>

List Administration

 PRB1798031

</td><td>

The 'Edit columns' functionality isn't working as expected in Configurable Workspace

</td><td>

If the user opens the workspace the first time and does the re-column options, the user preference is saved in the format: workspace.list.columnOrder.xyz. If the user then opens a new tab in Chrome, and changes it again, the preference is saved with a different suffix: workspace.list.columnOrder.abc. If the user then navigates back to the first tab in Chrome and updates the user preference, it updates back to: workspace.list.columnOrder.xyz. The workspace latches onto one of these user preference suffixes and ignores the others.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1861358

</td><td>

The rich description appears as NULL in the 'List' view but displays correctly in the case record

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Create an HR case.
3.  Navigate to sn\_hr\_core\_case.LIST.
4.  Open the newly created case.
5.  Select the hamburger icon and configure the form layout.
6.  Add the **Description** field.
7.  Save the changes.
8.  Return to the HR case form.
9.  Enter a message in the **Description** field.
10. Save the changes.

 Observe that the same value is automatically updated in the **rich\_description** field. This behavior is due to the 'Sync Description with rich\_description' business rule that synchronizes the values of the **Description** and **rich\_description** fields. When users navigate to the list view and add the 'Description' and 'rich\_description' columns, notice that the rich\_description field doesn't contain any value. The reverse works as expected; when users update the **rich\_description** field in the HR case form, the value appears in the **rich\_description** field in the list view.

</td></tr><tr><td>

List Administration

 PRB1894601

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for List count

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

Major Incident Management

 PRB1891876

 [KB2400018](https://hi.service-now.com/kb_view.do?sysparm_article=KB2400018)

</td><td>

The **View Workbench** UI action is redirecting to a broken 'Activity' section when opening it for a second time on a major incident form on the classic UI

</td><td>

After upgrading in Yokohama, when managing a major incident \(MI\) in the classic UI and moving to the 'Workbench' view, it's not loading properly. It's redirecting to a MI management broken activity view.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MetricBase

 PRB1878006

</td><td>

A hanging Clotho server can sometimes cause glide to become unresponsive

</td><td>

A Clotho XMLStats request never returns if Clotho becomes unresponsive, leading to semaphores exhaustion on glide.

</td><td>

 

</td></tr><tr><td>

Mobile Classic app \(End of Life\)

 PRB1900493

</td><td>

A mobile browser e-signature failure due to a re-authentication error

</td><td>

This issue was found when the instance property configured for SSO and the 'Approval with e-signature' plugin.

</td><td>

1.  Create a new CHG record.
2.  Progress it so it generates an approver \(sysapproval\_approver\) record to be assigned to the user.
3.  Log in to the instance using the newest Now Mobile on an iOS device.
4.  Navigate to **My actions** &gt; **Tasks**.
5.  Select **Approve**.
6.  Add any comments.
7.  Set the item to **Approved**.

 Notice that the user will be prompted for their username and password prior to approving.

</td></tr><tr><td>

Next Experience Notifications Menu

 PRB1851718

</td><td>

A URL isn't updated when navigating from the migrated dashboard by selecting the notifications

</td><td>

There's an issue on the unified navigation side that is causing this for several releases.

</td><td>

1.  Navigate to pa\_dashboards.LIST.
2.  Select a dashboard.
3.  Choose **Migrate Dashboard** from the 'Actions' menu.
4.  Open the migrated dashboard from the message displayed on the top of the page.
5.  Search for the migrated dashboard and open it.
6.  Have a notification in the notification bell at the top-right hand corner of the Next Experience UI.
7.  Select the bell.
8.  Select the incident record in the notification list.

 Observe that while the record displays in the main window, the URL bar isn't successfully updated and the tab name is wrong.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1785796

</td><td>

Keyboard focuses on a non-interactive Profile icon in User Menu

</td><td>

Keyboard focus should not go to non-interactive Profile icon in User Menu as this icon do not have any action on it.

</td><td>

1.  Open any base instance \(impersonate or log in with system administrator\) in Chrome browser of Windows machine.
2.  Navigate to the **User menu** button present at top right corner of the page using the Tab key.
3.  Expand the menu using the Enter / Return key.
4.  Press the Tab key again.

Notice that the focus moves to the profile icon and a tool-tip with user's name pops up.

5.  Use the Enter key on this icon to see if there is any action available on this interactive control.

 Observe that the keyboard focuses on the non-interactive Profile icon in User Menu.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1875808

</td><td>

The desktop notification banner doesn't display in Windows when multiple tabs are open

</td><td>

It displays the notification in the Notification Center but it doesn't display the banner.

</td><td>

 

</td></tr><tr><td>

Next Experience User Menu

 PRB1904194

</td><td>

Filter users of type AI Agents from the 'Impersonate user' list

</td><td>

Disable users from impersonating any user of the identity\_type 'ai\_agents'.

</td><td>

 

</td></tr><tr><td>

Next Experience User Menu

 PRB1926920

</td><td>

On instances with AI Agents, some users can't be found on the impersonation list

</td><td>

Currently, users with the '**Identity type**' field set to 'AI Agent' are filtered out, but they must also be filtered by 'is empty'.

</td><td>

1.  Open an instance that has AI enabled, such as Now Assist.
2.  Try to impersonate a user by searching for their name in the 'Impersonate user' prompt of the Next Experience user menu.

 Expected behavior: They should appear in the drop-down list.

 Actual behavior: They don't appear.

</td></tr><tr><td>

Now Assist Panel

 PRB1909094

</td><td>

The **Show more** button isn't visible on NASS for Safari browsers

</td><td>

When using the Now Assist Panel \(NAP\), Now Assist for Virtual Agent \(NAVA\), or Now Assist for Request \(NASS\) on Safari, the **Show more** button isn't visible after truncation, so the user is unable to see the full message. This prevents users from accessing the complete content of responses.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1912755

</td><td>

Missing inline editing modal for existing ACLs for agentic workflows and agents

</td><td>

 

</td><td>

1.  Open any workflow or agent with an existing ACL from studio.
2.  Select **Role** pills in the 'Roles' column of the ACL listed in the 'Define who can access this agentic workflow' section.
3.  Edit roles in the appearing modal.
4.  Select **Save**.

 Expected behavior: The modal should appear, and roles can be updated and saved.

 Actual behavior: No editing modal appears.

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1913515

</td><td>

'Run As Triggers' at Agent level isn't initiating a conversation in sys\_cs\_conversation table

</td><td>

 

</td><td>

1.  Install AIA 5.1.SNAPSHOT to IT Ticket Status Agent.
2.  Add 'Run As' for any AI user with 'Admin' as a role.
3.  Configure triggers on incident table with Run AS AI User.
4.  Update the incident to initiate a trigger/conversation.

 Notice that 'Trigger Conversation' is not getting initiated.

</td></tr><tr><td>

Now User Experience

 PRB1890272

</td><td>

A custom banner logo for an instance doesn't display for unauthenticated users

</td><td>

A broken image icon displays on the 'Log in' page.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1868011

 [KB2416081](https://hi.service-now.com/kb_view.do?sysparm_article=KB2416081)

</td><td>

The 'Show Schedule' link doesn't work for a non-admin user

</td><td>

After upgrading to Xanadu, non-admin users aren't able to access the on-call schedule.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

On-Call Scheduling

 PRB1893263

</td><td>

A query range error displays when the Automated Certificate Management Environment \(ACME\) rota\_admin is accessing cmn\_rota\_member record filters

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1864500

 [KB2216882](https://hi.service-now.com/kb_view.do?sysparm_article=KB2216882)

</td><td>

Activating Now Assist skills creates unnecessary \[sys\_update\_xml\] records which shouldn't be transferred between instances

</td><td>

Unexpected customer updates are being automatically generated for one\_api\_\* tables extending \[sys\_metadata\]. This causes confusion among users as they are unaware of how the updates are generated and these records aren't intended to be transferred via an update set.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OneExtend

 PRB1920527

</td><td>

Elaborate or shortened responses load on form skills when the ACL is set to Now Assist Context Menu \(NACM\) skills

</td><td>

This issue was found in Washington DC. Responses that have been elaborated or shortened appear even though they are restricted to a particular role in the NACM ACL table. The NACM skill in the skill configuration table also becomes 'inactive' by default.

</td><td>

1.  Log in to a Washington DC instance.
2.  Ensure Gen AI is setup.
3.  Activate the Resolution Notes generation skill.
4.  Navigate to the ACL table.
5.  Add a role to the NACM ACL, such as workspace\_admin.
6.  Impersonate an ITIL user.
7.  Select the text on close\_notes.
8.  Elaborate or shorten the text on close\_notes.

 Observe that elaborate and shortened responses are loading even when it's restricted to only the workspace\_admin role, and the NACM skill in the skill configuration table is 'inactive' by default.

</td></tr><tr><td>

OneExtend

 PRB1922282

</td><td>

Enforce ACL evaluations based on client parameters

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Password2 Encryption

 PRB1893080

</td><td>

High memory consumption during SEK ReEncrypt on instances with millions of password2 data

</td><td>

 

</td><td>

1.  Generate 20 million password2 records on an instance.
2.  Run the Storage Encryption re-encrypt.

 Expected behavior: The re-encryption completes successfully.

 Actual behavior: The encryption job ends abruptly because the node ran out of memory.

</td></tr><tr><td>

Password2 Encryption

 PRB1914502

</td><td>

The 'Grant' rule is revoked even if there are SEK reEncryption failures

</td><td>

 

</td><td>

1.  Open a corrupt PW2 record.
2.  Enable V1 Rekey by creating a system property glide.crypto.core .rekey.v2.enabled: false.
3.  Navigate to Rest API Explorer.
4.  Select **Explore**.
    1.  namespace: crypto
    2.  API name: Crypto Rekey Automation API
5.  Select **Send**.
6.  Navigate to 'security jobs'.
7.  Check the latest SEK reEncryption job.

 Expected behavior: The 'Grant' rule isn't revoked due to failures in SEK reEncryption.

 Actual behavior: The 'Grant' rule is revoked despite SEK reEncryption failures.

</td></tr><tr><td>

Performance Analytics

 PRB1897313

</td><td>

Data snapshots feature should not be available in Xanadu

</td><td>

The data snapshots plugin \(com.snc.pa.mlb\) is available in Xanadu and visible to the user even if the plugin is marked 'maint' only.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1810811

</td><td>

Dashboard duplication throws an error for certain dashboards

</td><td>

The error message reads: 'Duplicating dashboard failed. Please try again.'

</td><td>

1.  Open a Data Classification dashboard.
2.  Select **Duplicate**.

 Expected behavior: There is no error message and the copy should be identical to the original dashboard.

 Actual behavior: There is an error message and a new dashboard that is empty.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1831214

</td><td>

An ITIL user is unable to view the dashboard on Workspace Builder

</td><td>

The user observes an error message reading, 'Can't display this dashboard'.

</td><td>

1.  Log in as an ITIL User.
2.  Navigate to App Engine Studio.
3.  From the AES home page, select **Create** and create an App.
4.  Once an App is created, select the **+**icon in the 'Experiences' section and create a Workspace by giving tables \(for example, incident, change\_request\).
5.  Once Workspace experience gets created, select **Edit**or **Workspace** to open Workspace Builder.
6.  Once Workspace Builder loads, select the **Home** link in the left side panel and observe the dashboard in the middle panel.

 Expected behavior: The dashboard should load to the ITIL user.

 Actual behavior: The user observes an error message reading, 'Can't display this dashboard'.

</td></tr><tr><td>

Platform Analytics Filters

 PRB1838937

</td><td>

When a non-admin user creates a Platform Analytics 'Date' filter, 'Field' flashes briefly and is then cleared when selected, depending on the table chosen

</td><td>

Depending on the table chosen in the data to filter modal, entries selected in 'Field' flash briefly and are then cleared, and don't remain selected.

</td><td>

1.  Grant a non-admin user the analytics\_filter\_admin role.
2.  Impersonate the user.
3.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Filters**.
4.  Select **New**.
5.  Navigate to **Filter Type** &gt; **Date** &gt; **Data to filter** &gt; **Add**.
6.  Select **Task** in the field **Table** in the Data to filter modal.
7.  Select **Created** under **Field**.

 Observe that 'Created' flashes briefly and is then cleared, and the selection does not remain.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1788955

</td><td>

Core UI dashboard list **Delete migrated Experience Dashboard** UI action is not working as expected

</td><td>

This problem is not related to the Next Experience migration, although it involves removing the migrated Experience dashboard.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1894148

 [KB2173216](https://hi.service-now.com/kb_view.do?sysparm_article=KB2173216)

</td><td>

Bulk migration rewrites the scope of all Core UI dashboards

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Runtime

 PRB1810985

</td><td>

Missing metrics for session and semaphore wait times at the node level

</td><td>

As part of the Yokohama release, semaphore and session wait times have been added for each semaphore pool in XMLstats. However, they have been missing semaphore and session wait times for all pools combined, for example, wait times at the node level.

</td><td>

 

</td></tr><tr><td>

Platform Runtime

 PRB1900474

</td><td>

There's a difference in the number of sys\_journal\_field records created when running GR.setDisplayValue\(\) before GR.insert\(\)

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1922316

</td><td>

After upgrading to Xanadu, playbook stages/activities disappear from the screen

</td><td>

Playbook checklist steps do not work as expected and disappear from the screen. As a result, completed activities cannot be reviewed.

</td><td>

1.  Create a playbook with three stages and 1-2 activities in each stage.
2.  Make stage 2 conditional and make sure that the condition for stage 2 gets set to 'True' at the end of stage 1.
3.  At the end of stage 2, make the run condition of stage 2 false \(this can be required for other stages or activities\).
4.  Activate the playbook and create a record.
5.  Complete stage 1.

Stage 2 appears.

6.  Complete stages 2 and 3 as well.

 Expected behavior: All completed stages should be shown.

 Actual behavior: Only Stage 3 is shown.

</td></tr><tr><td>

Process Mining

 PRB1895034

</td><td>

Verify all analyst workbench statistics having two date units

</td><td>

Stats formatting in multiple areas in the 'Process details' need to be updated.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1905387

</td><td>

Addition of Query ACLs in Process Mining

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1920054

 [KB2423567](https://hi.service-now.com/kb_view.do?sysparm_article=KB2423567)

</td><td>

Condition with transitions are failing when viewing the 'Schedule task' results

</td><td>

This issue occurs when upgrading from Xanadu to Yokohama.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Process Mining Workspace

 PRB1885485

</td><td>

The Overview page of the guided setup isn't loading for a project which is created via PA journey

</td><td>

 

</td><td>

1.  Navigate to the left navigation.
2.  Search **Data Collector**.
3.  Select **Jobs**.
4.  Open the following:
    1.  \[PA Incident\] Historic Data Collection.
    2.  \[PA Incident\] Daily Data Collection.
5.  Select **Execute now** for both.
6.  Wait for 1 minute or until the process is complete.
7.  Open the left navigation.
8.  Search **KPIs**under Platform Analytics.
9.  Open a PA indicator =.
10. Choose an indicator on the incident because the incident is a default template.
11. Select **Run Process Analysis**.

Notice that this will trigger the PA API and create a project.

12. Search **PA projects** in the left navigation.
13. Open it under 'Process mining'.

Notice that the newly created project is displayed.

14. Open it.
15. Select **Edit** in the **Project builder** button.

 Observe that it goes into a continuous loop.

</td></tr><tr><td>

Process Mining Workspace

 PRB1921809

</td><td>

Enable auditing on Process Mining config tables

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1885649

</td><td>

A cost plan roll up isn't happening for programs and portfolio

</td><td>

 

</td><td>

1.  Create a Project.
2.  Assign a program to it.
3.  Add a cost plan and a benefit plan.
4.  Select **Save**.
5.  Validate the 'Financials' tab in the program.

</td></tr><tr><td>

Remote Tables

 PRB1885282

</td><td>

There's an out of memory exception when there's JavaScript and ^NQ in the encoded query string

</td><td>

Encoded strings are saved by calling setEncodedString on the query condition. This is done per row bases. As it is checking query conditions for each row, a saved encoded query is appended to the previous one. Eventually, it eats up the memory.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1922773

</td><td>

Agent role controls for identity type

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1922778

</td><td>

Agent role inheritance restriction

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Rollback and Recovery

 PRB1809473

</td><td>

When truncating a logical non-root table in TPH or TPP, all records are stored for ancestors and siblings in a shadow table

</td><td>

 

</td><td>

1.  Create two tables using the 'Table Per Hierarchy' extension model \(u\_table1 and u\_table2 extending the former\).
2.  Seed some test data on each tables.
3.  Invoke 'DBI.tableDrop\(\)' for u\_table2 with rollback enabled.
4.  Confirm that records from u\_table1 were recorded in the shadow table 'sh$u\_table1'.

 Notice that the shadow table has records for more than just u\_table2. This can become a costly, unnecessary operation if the parent table is large.

</td></tr><tr><td>

Schedule Optimization

 PRB1891169

</td><td>

On Demand Intraday, selecting multiple territories displays an 'Optimizing' icon even when there's no optimization running

</td><td>

 

</td><td>

1.  Create an intraday configuration for multiple territories, and ensure that those are overlapping territories.
2.  In the config, set the 'On Demand' boolean to true.
3.  As a dispatcher, navigate to Dispatcher Workspace \(DWS\).
4.  From DWS settings, turn off the 'Territory single select' toggle.
5.  From the territory selection on top left, select those same territories that are present in the intradat config.

 Expected behavior: The user shouldn't see the 'Optimizing' icon when there's no optimization running.

 Actual behavior: Users are seeing the 'Optimizing' icon on the calendar for those territories even if there's no optimization running.

</td></tr><tr><td>

Schedule Optimization

 PRB1893918

</td><td>

When the task limit is exceeded, jobs stay in the 'In Progress' state, and the 'In progress' Prioritized Optimization \(PO\) job is ignored when the default job runs while it's still in progress

</td><td>

The PO job never comes out of the 'In progress' state.

</td><td>

1.  Set up data in a way that a qualifier has more than 100 tasks.
2.  Create an intraday configuration with PO set to 'True' for that qualifier.
3.  Trigger a prioritized event for that qualifier.

 Notice that the PO job created stays in the 'In progress' state even after ML solution is complete, and never comes out of the 'In progress' state.

</td></tr><tr><td>

Schedule Optimization

 PRB1898555

</td><td>

When one of overlapping territories has 0 tasks, double booking happens

</td><td>

 

</td><td>

1.  Create overlapping territories.
2.  Ensure that one or more overlapping territories have 0 tasks.
3.  Run optimization.

 Expected behavior: Double booking shouldn't happen.

 Actual behavior: None of the existing assignments for that territory are sent as locked, so it double books.

</td></tr><tr><td>

Security Attributes

 PRB1922768

</td><td>

'Are You an Agent?' security attributes

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Security Attributes

 PRB1922771

</td><td>

Create common use case security attributes

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Security Attributes

 PRB1922776

</td><td>

Default access posture security attribute

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1883153

</td><td>

Blob reaper alerts for jobs that are running for less than 48 hours

</td><td>

 

</td><td>

1.  Navigate to sys\_status.
2.  Look for records with the name 'glide.service.modeling.startSweep, glide.service.modeling.lastSweep'.
3.  Change one of them so that the value in lastSweep is 25 hours after the value in startSweep.
4.  From the browser URL, type 'https://InstanceName.service-now.com/xmlstats.do'.
5.  Look for blob\_reaper\_job\_stuck and see its value is 'true'.

</td></tr><tr><td>

Service Model Foundation - Business Location

 PRB1896747

</td><td>

Addition of Query ACLs in Service Model Foundation - Business Location

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Service Model Foundation

 PRB1806488

</td><td>

Outsource Customer Service \(OCS\) view isn't shown for OSP agents when the csm\_ppm plugin is installed

</td><td>

The user isn't able to view OCS view, and can only see the case view.

</td><td>

1.  Log in as an admin user.
2.  Install Outsource Customer Service with demo data.
3.  Install CSM\_PPM plugins.
4.  Log in as a user.
5.  Navigate to **Cases** &gt; **All**&gt;.

 Expected behavior: The user should be able to view the OCS view on both the list and form layouts of the case table.

 Actual behavior: The user is able to see the case view on both the list and form layout on case table.

</td></tr><tr><td>

Service Portal

 PRB1893869

 [KB2313113](https://hi.service-now.com/kb_view.do?sysparm_article=KB2313113)

</td><td>

EC Search widget doesn't handle overflow of text when there are more than ten navigation tabs

</td><td>

When there are more than ten navigation tabs \(sys\_search\_filter\) created for AI Search Application, the EC Search widget doesn't handle the overflow of text.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1894604

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for widget-data-table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1919036

</td><td>

Faceted Search Widget/Genius Result card doesn't have a responsive design and disappears on a mobile browser or a small browser window

</td><td>

The issue can be reproduced on mobile and on a computer browser with developer tools.

</td><td>

1.  Log in to a Xanadu instance.
2.  Turn on AI Search.
3.  Turn on Genius Results for Portal.
4.  Turn on AI Search on Portal.
5.  Navigate to the Portal where this is turned on \(/sp or /esc\).
6.  Perform a search and view that the Genius Result show.
7.  Inspect the page to view the developer tools.
8.  Set the dimensions to a phone size.

 See that Genius Results disappear.

</td></tr><tr><td>

Service Portfolio Management

 PRB1897750

</td><td>

Lifecycle rules prevent certain actions

</td><td>

Lifecycle rules prevent users from adding an offering to a service that isn't operational. The user also can't move a service or offering from operational back to an earlier stage \(for example, ideation or design\).

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1792145

</td><td>

The 'Reset dedupe' business rule on the DM table should only trigger if the norm field changes

</td><td>

The event 'samp.reset.install.deduplicated' is fired.

</td><td>

1.  On the DM table, change a non-norm-field value such as install count or lifecycle.
2.  Navigate to the event log.

 Observe that the event 'samp.reset.install.deduplicated' is fired.

</td></tr><tr><td>

Software Asset Management

 PRB1795842

</td><td>

'Created Source' is not always stamped on software models by content update jobs

</td><td>

This issue usually occurs because the scheduled jobs below don't stamp the '**Created source**' field if it's empty on the suite parent: SAM - Apply latest content changes and SAM - Create lifecycles and suites for a software model.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1823270

</td><td>

Replication lag on MariaDB due to slow updates on cmdb\_sam\_sw\_install table

</td><td>

There is replication lag on the instance due to slow updates on the cmdb\_sam\_sw\_install table. SamPublisherCalculator.reconcileLeftoverEntities updates an excessive number of installs per product, which causes the query to run slowly.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1840860

</td><td>

The scheduled job 'SAM - Apply latest content changes' fails

</td><td>

The scheduled job 'SAM - Apply latest content changes' fails with the exception 'SAM - Apply latest content changes job aborted as CDS pull has not happened for all tables'.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1845794

 [KB2186255](https://hi.service-now.com/kb_view.do?sysparm_article=KB2186255)

</td><td>

The 'ITAM License Report' module isn't displaying in upgraded instances from Washington DC / Xanadu to Yokohama releases

</td><td>

The module is missing.

</td><td>

1.  Install HAMP.
2.  Log in to the instance and check for the 'ITAM License Report' module under the 'ITAM Licensing' menu.
3.  Note that the module isn't available.

 Expected behavior: The 'ITAM License Report' module should be visible under the 'ITAM Licensing' menu.

 Actual behavior: The 'ITAM License Report' module is not visible under the 'ITAM Licensing' menu.

</td></tr><tr><td>

Software Asset Management

 PRB1857027

 [KB2214434](https://hi.service-now.com/kb_view.do?sysparm_article=KB2214434)

</td><td>

Performance enhancement for the 'Bookkeeping for dedup on delete' business rule

</td><td>

The number of records to update may be reduced if there's an additional query on primary\_install is not null and deduplicated=true.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1865376

</td><td>

Unlicensed/actionable installs list are grouped by document ID by default, which turns off pagination

</td><td>

The unlicensed and actionable installs lists are grouped by the **m2m\_entity** field by default. Since they're grouped by a document ID, pagination is turned off and the user can't access more than 20 items.

</td><td>

1.  Run recon with demo data.
2.  Navigate to any software publisher result.
3.  Select **Unlicensed install** or **Installs requiring action with a count &gt;20**.

 Observe that the list view is grouped by the **m2m\_entity** field, which is a **Document id** field. The page only displays 20 items and pagination doesn't work.

</td></tr><tr><td>

Software Asset Management

 PRB1883407

</td><td>

The default value for month in the samp\_sw\_usage table remains in the dictionary after upgrading to Xanadu

</td><td>

 

</td><td>

1.  Provision a Washington DC instance with SAMP plugins.
2.  Upgrade the instance to Xanadu.
3.  Observe the default value of **month**in the samp\_sw\_usage table.

 Actual behavior: The default value is 'January'.

 Expected behavior: The default value should be empty.

</td></tr><tr><td>

Software Asset Management

 PRB1894351

</td><td>

SamNewRedHatPerSocketPairLicenseCalculator does not consider suite installs, and SamServerLicenseCalculator needs correction

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1895339

</td><td>

The encoded query stampUndeterminedEntitiesWithReasons is incorrect

</td><td>

It will stamp all installs where the inferred suite is set to 'product', which isn't expected.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1905701

</td><td>

'SAM - Generate Windows SQL Infra Report' job fails when processing hardware CIs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1920827

</td><td>

Product install condition is not honored in the suite of suite

</td><td>

Some conditions are not honored for product install conditions.

</td><td>

1.  Create a SQL Server suite with some components.
2.  Create a Visual Studio \(VS\) suite with SQL Server as component.
3.  Create an install condition on SQL Server where 'installed\_on.environment = prod'.
4.  Create install condition on VS Studio where 'installed\_on.environment = dev'.
5.  Create some installs of SQL Server components for some devices set environment as 'prod'.
6.  Create some installs of SQL Server components for some devices set environment as 'dev'.
7.  Run recon.
8.  Check if the inferred suite honors the product install condition.

 Notice that some conditions are not honored for product install conditions.

</td></tr><tr><td>

Software Asset Management Workspace

 PRB1627323

 [KB1263692](https://hi.service-now.com/kb_view.do?sysparm_article=KB1263692)

</td><td>

The entitlements related list doesn't filter by group, subgroup, or 'in use' entitlements

</td><td>

In Software Asset Workspace, the entitlements tab on a software model result shows all entitlements that match the SMR's software model. However, reconciliation only processes 'in use' entitlements. When reconciliation is run with grouping, the entitlement's group/subgroup also matters. This tab should filter for the correct entitlements under the software model result, rather than all entitlements for the software model.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Normalization

 PRB1847748

 [KB2020463](https://hi.service-now.com/kb_view.do?sysparm_article=KB2020463)

</td><td>

Sometimes Norm product/publisher isn't cleared/stamped on a few installs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reclamation

 PRB1814389

 [KB1709585](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709585)

</td><td>

Scheduled imports and data sources for 'SG-SCCM Software Last Used' and 'SG-SCCM SAMP Usage' do not delete old records in the table samp\_sw\_usage

</td><td>

This is caused by missing cross-scope configurations and a query to the field reclamation\_rule that does not exist on the table samp\_sw\_usage.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reclamation

 PRB1882484

</td><td>

A business rule prevents duplicate reclamation candidates, causing bulk RC not to be created

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Software Asset Reclamation

 PRB1896341

 [KB2171072](https://hi.service-now.com/kb_view.do?sysparm_article=KB2171072)

</td><td>

There's reclamation candidate and reclamation rule issues

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB1637293

 [KB1226034](https://hi.service-now.com/kb_view.do?sysparm_article=KB1226034)

</td><td>

There are incorrect licensing calculations for retired hosts on clusters consuming rights

</td><td>

In reconciliation, incorrect licensing calculation for retired hosts on clusters consuming rights.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reconciliation

 PRB1855067

</td><td>

'Undetermined' unlicensed reason given to installations when installations are reconciled to a SW model that does not have entitlements

</td><td>

After a fix was applied where the required key-value pairs have been created, Azure VMs are marked with the SAMP install unlicensed reason 'Undetermined' after adding Azure BYOL Key values to fix the issue 'Missing cloud license type'. This happens because the SW model reconciled to the installations has no entitlements.

</td><td>

 

</td></tr><tr><td>

Software Entitlements

 PRB1786107

</td><td>

The 'Update total\_cost on load' client script fails on Workspace Entitlement forms

</td><td>

The user observes a console error in the browser.

</td><td>

1.  Provision an instance with com.snc.samp and com.sn\_samp\_master installed with demo data.
2.  Navigate to Software Asset Workspace.
3.  Navigate to License Operations.
4.  Open any existing entitlement.

 Notice a console error in the browser.

</td></tr><tr><td>

Software Lifecycles

 PRB1566827

</td><td>

The user is unable to create a new custom lifecycle through list view

</td><td>

The **New** button on the lifecycle table is disabled by default. When enabled, there are no modules to access the lifecycle table.

</td><td>

 

</td></tr><tr><td>

Software Models

 PRB1828999

</td><td>

'Get install count for software model' job runs a large query when the software model is corrupted in Software Asset Management \(SAM\)

</td><td>

The 'Get install count for software model' job creates an encoded query for a software model to match the corresponding discovery model. The query generated is 'null' when the software model version/edition operator is corrupted. This causes all discovery models to be picked for matching, which creates a large query and results in the job running forever.

</td><td>

 

</td></tr><tr><td>

SSH MID Server Communication Protocol

 PRB1887914

</td><td>

SSHProtocolEngine thread is overwhelmed when SSH server starts dumping instead of sending a protocol version string

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Store IRM GRC Core Case Management

 PRB1894250

</td><td>

Query range issues on certain tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Store IRM Privacy Case Management

 PRB1894359

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules in Store IRM Privacy Case Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Survey Management

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

Table Cleaner

 PRB1860821

</td><td>

TableCleaner doesn't resolve gateways

</td><td>

Since TableCleaner is uses the API 'DBConfiguration.getDBI', which can only resolve it.

</td><td>

1.  Configure a gateway for any table.
2.  Call the TableCleaner.clean API.

 Notice that gateways aren't resolved.

</td></tr><tr><td>

Template Management for Field Service

 PRB1802776

</td><td>

The 'Copy Work Order' task template does not work in the work order task template page

</td><td>

 

</td><td>

1.  Open the Work Order Task Template List.
2.  Select **New**.
3.  Select **Copy Task Template**.

 Observe that nothing happens.

</td></tr><tr><td>

Server-side scripts

 PRB1929097

</td><td>

REST API response is \{empty:false\} for some attributes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Template Management for Field Service

 PRB1920388

</td><td>

When accessing a work order template, $sm\_templates can be slow and cause memory issues on the client-side \(browser\)

</td><td>

The browser can be slow if they have a relatively large number of task templates.

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1909388

</td><td>

Drag and drop task isn't working for crew tasks when territory planning is 'active' in Dispatcher Workspace

</td><td>

 

</td><td>

1.  Create a Work Order Task \(WOT\).
2.  Check 'Needs Crew' in the WOT.
3.  Ensure that Territory Planning is installed and active.
4.  Launch the Dispatcher Workspace.
5.  Drag the task against the Crew.

 Expected behavior: The user should be able to drag or drop the task on crew.

 Actual behavior: The user isn't able to drag or drop the task on crew.

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1877226

</td><td>

Conflict on a field name when creating an offload rule

</td><td>

When configuring an offload rule, there's a conflict if a system field is set as an indexed field.

</td><td>

 

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1889818

</td><td>

The default retry period for failed offloads is too low

</td><td>

The default retry period should be 6 hours.

</td><td>

1.  Generate a record whose offload perpetually breaks.
2.  Make it fail upon offload with a 60-minute retry period.
3.  Archive other records that would get offloaded by the same rule.

 Notice that the records never get offloaded.

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1893476

</td><td>

Tier 2 Index tables don't properly store DocumentID data

</td><td>

When creating a Tier 2 offload rule, the user is able to select DocumentID columns for indexing on the cidx\_ table created to store the indexed data. Columns of DocumentID type are missing the 'Dependent Field' tab, which impacts the navigation and and readability of index tables. This results in no previews or quick links to the record on CIDX table.

</td><td>

1.  Create an archive and offload rule for sys\_email.
2.  Create or choose a sys\_email record which references some other record in its 'instance' column.
3.  Archive the record.
4.  Observe that on the archive table, the link to the referenced record is preserve on the column.
5.  Offload the record to tier 2.

Observe that the link is missing on the cidx\_ar\_sys\_email table, and the data appears '\(empty\)'.

6.  View the XML for the record on the cidx\_ar\_incident.

Observe that the sys\_id is in the instance column.

7.  Navigate to the **sys\_dictionary**table.
8.  Open the 'instance' column for cidx\_ar\_sys\_email.
9.  Select **Related links** &gt; **Advanced view** &gt;.
10. Navigate to the 'Dependent Field' tab.

Notice that the **Dependent**Field isn't selected.

11. Navigate to the **sys\_dictionary**table.
12. Open the 'instance' column for ar\_sys\_email.

 Notice that there is a **Dependent** field selected.

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1897660

</td><td>

Change the sys\_property glide. db.archive.offload. free\_storage\_max\_gb value from 100GB default to 36T

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1786721

</td><td>

The creation of a sub record using UI actions in the interaction form does not honor a domain selection

</td><td>

A domain check appears.

</td><td>

1.  Impersonate a Parent user.
2.  Navigate to base agent workspace \( append to instance url /now/demo/baseaw\), Create a list on incident
3.  Create a new incident and Provide 'Child Domain' as the domain.
4.  Save the record.
5.  Select any related list like 'Child incident'
6.  Select **New**

 Expected behavior: A related record is automatically created under the incident record domain.

 Actual behavior: A domain check appears.

</td></tr><tr><td>

UI Form Administration

 PRB1880019

</td><td>

Field labels aren't displaying horizontally even though glide.ui.form.breakpoints.enable is true

</td><td>

If the form width is more than or equal to 800 pixels, then field labels should display horizontally. If glide.ui.form.breakpoints.enable is false, the form should be in a 2 column layout and field labels should display vertically after increasing the form layout.

</td><td>

1.  Log in to a Next Experience instance with an admin user.
2.  Open the sys\_properties table.
3.  Search for glide.ui.form.breakpoints.enable and make it true.
4.  Open any configurable workspace.
5.  Open any of the record form.
6.  Increase the form layout by using the resizable pane.

 Expected behavior: Field labels should display horizontally beside the label after increasing the form layout.

 Actual behavior: Field labels aren't displaying horizontally after increasing the from layout.

</td></tr><tr><td>

UI Form Administration

 PRB1881995

</td><td>

Content on 'Special Handling Notes' isn't scrollable

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1887884

</td><td>

A dependent field onChange handler fires when the **Depends on** field changes when there's no change to the dependent field

</td><td>

There are client scripts on various task-based tables that clear the assigned\_to when assignment\_group changes. These tables can't be tested on \(for example: change\_request, incident, problem, problem\_task\) as it will appear that the dependent field onChange handlers fire when the**Depends on** field changes. A table that doesn't have existing client scripts on the **assignment\_group** field like change task \(change\_task\) must be used.

</td><td>

1.  Create a new client script with the following:
    1.  Table: Incident
    2.  UI Type: All
    3.  Type: onChange
    4.  Field name: Assigned to
    5.  Script:function onChange\(control, oldValue, newValue, isLoading, isTemplate\)
2.  Start a new Change Task \(change\_task\) record in UI16.
3.  Set an Assignment Group.

 Notice that the info message isn't displayed because onChange handlers for the dependent field \(assigned\_to\) are not fired.

</td></tr><tr><td>

UI Policies

 PRB1894468

 [KB2293905](https://hi.service-now.com/kb_view.do?sysparm_article=KB2293905)

</td><td>

Performance degradation for Core UI performance

</td><td>

Core UI performance testing shows 250 to 300ms degradation for most direct load user actions.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1871297

</td><td>

UXF pages are broken due to the duplicate assets with different versions bundled in the nds-bundle

</td><td>

The new release of the sn-datagrid brings in new versions of side-channel-weak-map, side-channle and get-intrinsic which end up pulling in call-bind-apply-helpers 1.0.2 to the instance. When nds-bundle is built, it doesn't deduplicate assets with deep import paths, so both call-bind-apply-helpers/1.0.1/functionApply and call-bind-apply-helpers/1.0.2/functionApply are added to the nds-bundle. They share the same global variable name: \_\_TECTONIC\_\_call\_bind\_apply\_helpers\_functionapply, so it ends up calling wrapTectonicVarIfNeeded\(\) twice for the same tectonic variable, which causes it to be double wrapped.

</td><td>

1.  Navigate to sn-datagrid.
2.  Build the zip of the component.
3.  Sideload the zip on to any instance.
4.  Navigate to the home page.

 Notice that the page is broken.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1896496

</td><td>

KG slot filling throws an error

</td><td>

Execution gets stuck and throws error messages on VAD test panel.

</td><td>

1.  Navigate to Store Publisher Portal.
2.  Enter an utterance such as 'Collect user information for voting' to discover and execute the User Information topic.

 Expected behavior: Input nodes in the topic must be slot filled by KG and the topic must be executed.

 Actual behavior: The Gen AI log shows 'Synthensized response' as the last log record, there are no log records for TextToTResult and Unified Slot Fill, and execution ends with multiple 'Sorry' messages on VAD test panel.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1912465

</td><td>

The Static Choice Header Card is missing in the chat client

</td><td>

A chat is loaded and a topic is discovered, but the Header Card is missing.

</td><td>

1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.
2.  Select the **Create** button located in the top-right corner of Conversational Studio.
3.  Select the Model Type: 'LLM', type: 'Topic', and fill in all the required fields.
4.  Select the **Create** button.
5.  Drag the 'Static Choice' node to the canvas and select it.
6.  In the right-side panel, under **Advanced**, select **Header Card** and toggle on 'Insert'.
7.  Under 'Would you like help', select **Yes** and select the **Add card** button.
8.  Select Card type as 'Small image with text'.
9.  Fill the required **Title** input field.
10. Under '3. Image URL link', select the **Upload Image** button.
11. In the newly opened file explorer window, select the image file to upload.

The image is uploaded, and the image URL is generated and inserted into the 'Image URL link' input field.

12. Select the auto-generated link.
13. Save the topic and select the **Test** button located in the upper-right corner of the VA Designer screen.
14. Wait until the chat is fully loaded.

 Expected behavior: The Header Card is present in the Static Choice where it was set.

 Actual behavior: The chat is loaded and the topic is discovered, but the Header Card is missing.

</td></tr><tr><td>

Virtual Agent

 PRB1826252

</td><td>

User inbound messages to a Live Agent end up in the picker pagination logic in specific scenarios for channels

</td><td>

The user inbound message to a Live Agent somehow ends up in the picker pagination logic in CAF if the last rich control before invoking the live agent was a paginated picker.

</td><td>

1.  Create a custom topic for invoking a Live Agent.
2.  Add a paginated picker nod before invoking the Live agent \(for example, choose a preferred language picker with 15 options\).
3.  Make this the default topic for Live Agent.

 Notice that user inbound messages to a Live Agent end up in the picker pagination logic

</td></tr><tr><td>

Virtual Agent

 PRB1833571

</td><td>

When \_max\_wait\_topic\_ is ended using the 'End Conversation' option, the conversation hangs and never completes

</td><td>

The 'Resume flow after topic switching' inside of the \_max\_wait\_topic\_ properties should be flipped to false.

</td><td>

1.  Install the AgentChat plugin.
2.  Navigate to the awa\_queue table.
3.  Open 'Agent Chat Queue'.
4.  Set **Max wait time** to something short like 30 seconds.
5.  Select **Queue Triggers** in the related lists and create a new one.
6.  Ensure that the queue trigger is a max wait time trigger and have the topic be anything.
7.  Navigate to the awa\_assignment\_rule and open 'Chat - Most Capacity'.
8.  Select **Rejection Handling** and set the timeout to 2 minutes.
9.  Ensure that an agent is online
10. Start a conversation and run the 'Live Agent Support' topic.
11. Let the search run until the max wait time topic appears.
12. Select **End conversation**.

 Expected behavior: The conversation ends.

 Actual behavior: The conversation hangs and never ends.

</td></tr><tr><td>

Virtual Agent

 PRB1849654

 [KB1940828](https://hi.service-now.com/kb_view.do?sysparm_article=KB1940828)

</td><td>

Synthesized output is not captured in an interaction transcript

</td><td>

In Virtual Agent, the transcripts captured on the interaction don't log the synthesized output.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1874005

</td><td>

A record in provider\_user\_map is still inactive, causing Now Virtual Agent to fail approvals

</td><td>

When a sys\_user record becomes active after being deactivated, provider\_user\_map is still inactive and there's no logic to activate the mapping. The user still receives a notification for record approval in Microsoft Teams because the mapping exists, even though provider\_user\_map is inactive. When the user attempts to approve the record, an error occurs because their record in provider\_user\_map is still inactive.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1880242

</td><td>

'interaction\_context' is overwritten with new conversation variables

</td><td>

When a requester is starting a conversation via sn\_va\_web\_client\_app with sysparm\_skip\_ load\_history=true and other parameters, the 'interaction\_context' takes the params as we'd expect. But if the requester has an ongoing chat, but starts a new conversation with different params, the initial chat's interaction\_context is overwritten with the new interaction\_context values.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881393

</td><td>

An Agent Chat new message desktop notification should be selectable and redirect to the 'Calling' tab

</td><td>

When there's an agent in the workspace doing a live chat with a user, if users move the focus to another tab, with desktop notifications turned on, they receive a notification. The need is for the notification to be selectable and redirected to the 'Chat' tab.

</td><td>

1.  Navigate to an instance.
2.  Impersonate a system admin.
3.  Open Service Operations Workspace.
4.  Navigate to the inbox and set the user to 'available'.
5.  Ensure that the desktop notifications are set up with the gear icon.
6.  Open an incognito window.
7.  Impersonate a user.
8.  Open the Service Portal.
9.  Open the chat.
10. Ask for a live agent.
11. Wait for the connection with the agent.
12. From the system admin window, open a new tab and stay on that tab.
13. From the user window, send a message.

 Users should receive a desktop notification, but it's not selectable and doesn't redirect.

</td></tr><tr><td>

Virtual Agent

 PRB1890131

</td><td>

Long-running Virtual Agent transactions are not timed out in Xanadu and prior releases

</td><td>

When a topic is created with script node that causes an infinite loop, the transaction should cancel after a period of time, but it continues to execute until the node is restarted.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1893275

</td><td>

A loading screen appears and a topic with a reference choice control isn't triggered

</td><td>

Automation scripts are also failing due to this.

</td><td>

1.  Log in to an instance.
2.  Create a topic with a reference choice control.
3.  In the reference choice control, set the filter condition to return only one record.
4.  Make the reference choice choice control skippable.
5.  Run that topic from the Web Client.

 See that the topic isn't triggered and is stuck at the loading screen.

</td></tr><tr><td>

Virtual Agent

 PRB1893952

</td><td>

A Now Assist panel isn't loading on Yokohama instances

</td><td>

Now Assist Panel is not loading AI Agents not running in Playground. An error is observed in the logs.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1896976

</td><td>

The 'Start a new conversation' pop-up box in Virtual Agent is out of the screen

</td><td>

In the instance, the padding is cut off, and the popover should be contained in the Web Client window.

</td><td>

1.  Navigate to Virtual Agent on an instance.
2.  Start a new conversation with the Now Assist' pop-up.

 Observe that when hovering over the **+**button, it's cut off on the right side.

</td></tr><tr><td>

Virtual Agent

 PRB1901626

</td><td>

'Notification' errors out if users trigger it for a user who has not had any interaction with Virtual Agent for more than 60 days

</td><td>

 

</td><td>

1.  Verify that the user doesn't have any interactions with web-client/channels for more than 60 days.
2.  Set up and trigger a non-actionable/actionable notification.

 Expected behavior: A new sys\_cs\_notification record should be created for the user.

 Actual behavior: There's an error in the notification log on the lines of 'sessionResponseV2Dto is null'.

</td></tr><tr><td>

Virtual Agent

 PRB1907383

</td><td>

Skill configuration ID is passed in meta for a chained skill at runtime

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1912588

</td><td>

AiAgentSecurityMigration and AiAgentSecurityHelper script includes needs to be in the global scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1915793

</td><td>

There's an incorrect name for flows when creating 'invoke\_from\_ai' ACLs

</td><td>

 

</td><td>

Execute this API to create ACLs for flows used as tools: 'new global. AiAgentSecurityMigration\(\) .run\( true\)'.

 Observe that for the subflow ACLs, the ACL is created with 'name' instead of 'internal\_name', which is incorrect and it's missing ACL evaluations at run time. It's defaulting to global \* ACL due to the incorrect name of the flow.

</td></tr><tr><td>

Virtual Agent

 PRB1916762

</td><td>

An ACL restriction on sys\_one\_extend \_resource\_edge prevents websearch from being accessible to users

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1918740

</td><td>

Querying on virtual column for retrieving skill metadata fails

</td><td>

 

</td><td>

1.  Navigate to AI Agent Studio.
2.  Choose an existing workflow or agent which has Now Assist Panel or Virtual Agent roles enabled.
3.  Create a new agent or workflow.
4.  Choose a role for those who can access the workflow or agent.
5.  Save and continue.

 Expected behavior: Previously associated skill applicability records should be deleted.

 Actual behavior: Previously associated skill applicability records still exists.

</td></tr><tr><td>

Virtual Agent

 PRB1923131

</td><td>

sn-chat-choice-picker appears instead of text-picker for users that enabled new sys prop

</td><td>

A choice picker with radio buttons appears for users that enabled new sys prop, instead of the expected text picker with a list of topics.

</td><td>

1.  Turn on Now Assist Virtual Agent.
2.  Create a virtual agent topic.
3.  Select static/dynamic node and populate choices.
4.  Run the topic in NAVA.

 Actual Results: A choice picker with radio buttons shows up.

 Expected Results: A text picker with a list of topics shows up if the user has enabled new sys prop.

</td></tr><tr><td>

Virtual Agent

 PRB1923828

</td><td>

Fix choicepicker branding for NAVA

</td><td>

Choice picker shows default NAVA branding even though different branding was selected.

</td><td>

1.  Navigate to the Assistants page.
2.  Create a new branding record in sys\_cs\_branding\_setup table.
3.  Change the branding of the new record to 'Polaris-dark'.
4.  Navigate to /esc portal and select a topic that uses choice-picker.

 Expected behavior: Choice picker matches the selected branding.

 Actual behavior: Choice picker shows default NAVA branding.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1869054

</td><td>

Adding the ability to customize/update the default 'FAB' icon

</td><td>

The custom 'FAB' icon is configurable by defining this variable: $now-sp-nass-FAB-icon.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1893493

 [KB2182131](https://hi.service-now.com/kb_view.do?sysparm_article=KB2182131)

</td><td>

Non-conversational catalog items can't be selected if they are preceded by external KB article citations

</td><td>

When Now Assist for Virtual Agent is enabled, catalog items can't be selected in the Virtual Agent interface.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1901424

</td><td>

Chat client lets multiple messages be sent through simple scripting

</td><td>

 

</td><td>

1.  Open any chat client.
2.  Enter a message in the text box.
3.  Inspect the browser page and in the 'Elements' tab, highlight the now-button corresponding to the **Send** button.
4.  Move to the 'Console' tab.
5.  Enter a small script to simulate clicks multiple times: 'for \(var i = 0; i 15; i++\) \{ $0.click\(\); \}'.
6.  Observe all 15 messages are sent in the chat client.

 Expected behavior: Chat client shouldn't allow multiple inbound messages.

 Actual behavior: Chat client allows multiple inbound messages.

</td></tr><tr><td>

Visual Task Boards

 PRB1852813

</td><td>

If the modal window is closed by selecting outside of the modal, VTB cards aren't refreshed automatically when updated

</td><td>

This only occurs if the modal window is closed by selecting outside of the modal. If the modal window is closed by selecting the 'X' in the top right, the record's card updates automatically as expected.

</td><td>

1.  Create a visual task board by navigating to **Self-Service** &gt; **Visual Task Boards** &gt; **New** &gt; **Data Driven Board**.
2.  Set **Task Table** to 'Incident' and the **Vertical Lane** field to 'Incident State'.
3.  Select **Next**.
4.  For the conditions, set **Assigned to is \[current user\]** and select **Create**.
5.  Select a card on the VTB to open the modal window.
6.  Unassign the record from \[current user\] in the modal window.
7.  Close the modal window by selecting outside of the modal.

Observe that the card remains on the VTB even though it no longer meets the conditions for the board.

8.  Refresh the VTB page.

 Observe that the card is no longer on the board.

</td></tr><tr><td>

Work Order Management

 PRB1895750

</td><td>

A work order task template doesn't display the skill associated/linked to it

</td><td>

Users aren't able to associate the task skills with levels to a work order task template and display the value to the UI. Also, the '**Task skills**' field isn't available from the field picker of the work order task template, even though the form layout includes the field.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1895909

</td><td>

Add the mktplace\_requestor role for wm\_task.parent

</td><td>

 

</td><td>

1.  Log in with the location contributor associated with a location, and having work order tasks associated with work orders.
2.  Navigate to the cases associated with the work order on the BLSP portal.
3.  Select **Work orders RL**.
4.  Select **Work order task**.

 Expected behavior: The user should get access to the work order tasks.

 Actual behavior: The user is getting a query\_range error.

</td></tr><tr><td>

Work Order Management

 PRB1917364

</td><td>

Update the SMCoreConfigCacheManager.getSMConfig API to make it backward compatible with latest SMConfigurationHelper code

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1921026

</td><td>

**'Status**' field choices differ from those on the 'Work Order' form view when setting up a Work Order Task \(WOT\) template

</td><td>

When setting up a WOT template, the choices that appear for the **Status \[state\]** field differ from the choices that appear on the WO form view. Also, when setting up a WO template, choices don't appear for the '**Service Request Type**' field.

</td><td>

1.  Navigate to the list of Work Order Models \[cmdb\_workorder\_product\_model\].
2.  Select the **GE ULRICH ASSEMBLY**model.

 Notice that under 'Request Information', 'Service Request Type' doesn't provide selections. Also, notice that under 'Task information', the 'Status' choices differ from the choices that are available on the WOT form view.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 9 Hotfix 1](xanadu-patch-9-hf-1-PO.md)
-   [Xanadu Patch 9a Hotfix 1](xanadu-patch-9a-hf-1-PO.md)
-   [Xanadu Patch 9a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2290356)
-   [Xanadu Patch 9](xanadu-patch-9.md)
-   [Xanadu Patch 8](xanadu-patch-8.md)
-   [Xanadu Patch 7](xanadu-patch-7.md)
-   [Xanadu Patch 6](xanadu-patch-6.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


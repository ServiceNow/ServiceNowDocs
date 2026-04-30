---
title: Yokohama Patch 6
description: The Yokohama Patch 6 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 102
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 6

The Yokohama Patch 6 release contains important problem fixes.

-   **Yokohama Patch 6 was released on July 31, 2025.**
    -   Build date: 07-27-2025\_1301
    -   Build tag: glide-yokohama-12-18-2024\_\_patch6-07-17-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

## Overview

Yokohama Patch 6 includes 330 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp6.png "Top 10 problem categories") ![Fixed issues grouped by problem categories bar chart]( "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 6 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 6, refer to [KB2309929](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2309929).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y06.00.xlsx).

## Changes in Yokohama Patch 6

-   **[Configuration Management Database \(CMDB\) release notes](../now-platform-capabilities/cmdb-rn.md)**

    Starting with Yokohama Patch 6, you can configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the necessary permissions to perform some CMDB Workspace tasks by manually running a scheduled job.

    Starting with Yokohama Patch 6 \(zbooted or upgraded\), you must manually run the scheduled job '**Remove CMDB Roles from ITIL roles and Add CUD access to sn\_cmdb\_admin/sn\_cmdb\_editor roles** to configure the sn\_cmdb\_admin and the sn\_cmdb\_editor user roles with the permissions that are necessary for performing some CMDB Workspace tasks.

-   **[Configure Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=configure-now-assist-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for Now Assist skills and AI agents. You can set skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   **[Enterprise Architecture \(formerly Application Portfolio Management\)](https://www.servicenow.com/docs/access?context=application-portfolio-management-landing-page&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    The ServiceNow® Enterprise Architecture unites strategic and operational teams, enabling organizations to achieve their business objectives. It serves as a powerful decision engine, combining robust modeling with the management of business capabilities, application portfolios, information portfolios, and technology portfolios. This product changes has for the Yokohama Patch 6 release.

-   **[Exploring Now Assist for Enterprise Architecture \(EA\)](https://www.servicenow.com/docs/access?context=exploring-now-assist-for-ea&version=yokohama&pubname=yokohama-application-portfolio-management&ft:locale=en-US)**

    You can use Now LLM Service, Azure OpenAI, Google Gemini or Anthropic Claude on AWS as the AI model provider for Now Assist skills and AI agents. You can set skill-level preferences in the [Now Assist Admin console](https://www.servicenow.com/docs/access?context=manage-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US). For more information, see [Large language models on the ServiceNow AI Platform®](https://www.servicenow.com/docs/access?context=exploring-large-language-models&version=yokohama&pubname=yokohama-intelligent-experiences&ft:locale=en-US).

-   **QueryRangeACLAuditor**

    This patch includes the May Maintenance update script in the form of a script include \(QueryRangeACLAuditor\). This script is not triggered automatically and must be run after a patch upgrade. More details on running the QueryRangeACLAuditor and its functionality can be found in [KB2046494](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2046494).


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

Column Level Encryption Enterprise

 PRB1874479

 [KB2070474](https://hi.service-now.com/kb_view.do?sysparm_article=KB2070474)

</td><td>

The security banner message 'One or more security migration jobs have failed in your instance' appears constantly and isn't dismissed after one day

</td><td>

As part of the Column Level Encryption \(CLE\) migration process from Yokohama and later, there are cases where the 'Key migration' job is failing as there's no key to migrate. As the key migration job fails, there's a security banner announcement 'One or more security migration jobs have failed in your instance', which is appearing in the instance post-migration. The red banner message for migration errors isn't dismissed. The banner message should appear only for one day and be dismissed after that. However, the banner message is displayed constantly.

</td><td>

Log in to any Yokohama instance where the key migration job failed, as there is no key to migrate.

 Observe the banner announcement, 'One or more security migration jobs have failed in your instance', and the banner announcement is shown even after one day.

</td></tr><tr><td>

Contextual Search

 PRB1868773

</td><td>

canWrite on GlideElement for variable sets returns a null pointer exception

</td><td>

There's an issue calling a canWrite on a variable set when applying form changes to be filtered. The individual variables behave correctly.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1810466

</td><td>

Physical Table Stats Table \(sys\_physical\_table\_stats\) doesn't have a cleanup mechanism that retain the table stats records daily after Xanadu changes

</td><td>

A rule will be implemented similar to the one for sys\_db\_size\_stats for sys\_physical\_table\_stats using sample\_period\_start and sys\_created\_on, or sys\_updated\_on.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1837739

</td><td>

'Physical Table Stats Gatherer' runs long due to an influx of query with hash 2136542706

</td><td>

The job runs for more than one hour. Each query takes around 239 ms but since the number of times it's being called is high, the overall job takes a longer time.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1791510

 [KB1718735](https://hi.service-now.com/kb_view.do?sysparm_article=KB1718735)

</td><td>

Discovery is hanging for certain schedules due to WMI queries failing

</td><td>

 

</td><td>

Run Discovery on Windows devices where the WMI queries fail in Windows OS Patterns.

</td></tr><tr><td>

MID Server

 PRB1912171

 [KB2266697](https://hi.service-now.com/kb_view.do?sysparm_article=KB2266697)

</td><td>

Yokohama MID Server upgrades do not upgrade all jar files in lib

</td><td>

Yokohama MID Server upgrades don't upgrade all jar files in lib, causing NoClassDefFoundError for various classes, and MID Server to go down.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1909523

 [KB2262722](https://hi.service-now.com/kb_view.do?sysparm_article=KB2262722)

</td><td>

Changes in the dashboard only appear in the session language where they were made

</td><td>

Users are experiencing inconsistent behavior in Platform Analytics dashboards depending on the selected user language. When viewed in English, the dashboard reflects the latest updates. When switched to Italian, an outdated version displays, even after clearing the cache using cache.do.

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

 PRB1911649

</td><td>

Non-record gen\_ai directive ACLs not active on zboot

</td><td>

 

</td><td>

1.  Zboot the instance.
2.  Open the sys\_security\_acl table.
3.  Search for the types:
    -   gen\_ai\_workflow
    -   gen\_ai\_agent
    -   gen\_ai\_skill, flow, flow\_action

 Expected behavior: All matching \* ACLs should be active.

 Actual behavior: All matching \* ACLs are active=false.

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1916144

</td><td>

gen\_ai\_ prefixed ACL types should use '\* ACLs' for their default rule name

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1910493

 [KB2321524](https://hi.service-now.com/kb_view.do?sysparm_article=KB2321524)

</td><td>

There is slowness when loading forms with 'Table Choice' fields, even after applying a 2000 record limit

</td><td>

The size of CACHE\_ARCHIVE\_TABLE\_HAS\_TERMS cache needs to be higher than 2000 since many instances have &gt; 1000 archive tables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1743672

</td><td>

Worknotes using Carriage Return aren't displaying in HR Agent Workspace when using edge encryption

</td><td>

 

</td><td>

1.  Enable Edge Encryption in the HR Workspace.
2.  Open the HR Workspace using an encrypted URL.
3.  Post a Worknote on a HR Case that uses a Carriage Return.

 Notice that the Worknote isn't visible in the Activity Log.

</td></tr><tr><td>

Activity Stream

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

Activity Stream

 PRB1895624

</td><td>

Activity Stream displays sys\_id instead of the display name

</td><td>

The user's sys\_id is posted instead in the Activity Stream event.

</td><td>

1.  Log in as an admin user.
2.  Create a new user with User ID in the format of a sys\_id.
3.  Complete the **First Name** and **Last Name** fields.
4.  Log in with new user.
5.  Navigate to **Activity stream**.
6.  Post a comment.

 Notice that the user ID \(sys\_id format\) is displayed instead of the user's display name in the Activity Stream event.

</td></tr><tr><td>

Activity Stream

 PRB1897140

</td><td>

A workspace activity stream isn't displayed for archived records

</td><td>

Due to a misunderstanding of the requirements for archived records, a performance fix made it so that no workspace activity streams get generated for any archive tables, i.e. tables with an 'ar\_' prefix. Instead, since archived records are read-only, all live updates for archived records should be turned off, while allowing the activity stream to be viewable.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1914670

</td><td>

In UI16, AI Agent posts appear as the logged-in user until the page is refreshed

</td><td>

In UI16, the entries appear as posted by the logged-in user initially. Only after a manual refresh the name changes to AI Agent. In Workspace, the entries correctly show the AI Agent as the author, which is expected.

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
3.  Navigate to **Manager Workspace**.
4.  Navigate to **All agents**.
5.  Set the user presence state to 'Available'.
6.  Navigate to **Queued Work item**.
7.  Search for a document id.
8.  Select the item
9.  Select **Allocate**.

 Notice that the capacity appears as zero/3 for the user.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1909214

</td><td>

Updating an agent's presence as an integration user via the Agent API fails

</td><td>

The gr.canWrite\(\) checks aren't working as expected when the API caller is an integration user. The integration user should be allowed to update the presence state. If the API caller has the awa\_integration\_user role, the request should go through. If the API caller doesn't have sufficient roles, the request should fail with a 500 error.

</td><td>

 

</td></tr><tr><td>

Agile Development

 PRB1900463

 [KB2251764](https://hi.service-now.com/kb_view.do?sysparm_article=KB2251764)

</td><td>

Global search isn't working for certain records after upgrading to Yokohama

</td><td>

After upgrading to Yokohama, pre-fix for certain records, such as Release, Feature, Phase, got updated. This prevents the global search from working as expected. The new pre-fix records are searchable, but existing records created before the upgrade using the old prefix aren't searchable.

</td><td>

Refer to the listed KB article for details.

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

 PRB1913666

</td><td>

There's a AisDisableSearchSignalEvent warning message: 'scope is not defined'

</td><td>

In the syslog table, there's an error: 'com.glide.script.RhinoEcmaError: "AisDisableSearchSignalEvent" is not defined. sys\_script.a9d8af92ff602210fbf4ffffffffffa8.script ➚ ➚ ➚ : Line\(3\) column\(0\). java.lang.SecurityException: Illegal access to package\_private script include AisDisableSearchSignalEvent: caller not in scope rhino.global.'

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1913679

</td><td>

The ExternalContentIngestion date parsing IT test fails

</td><td>

AI Search seems to be unable to parse date values correctly. Expected is 2001-01-01 00:00:00, but was 2001-01-01 00:00:01.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1916149

</td><td>

Allow AI Search admin users to invalidate crawlstore and perform a full Rrcrawl for a given indexed source

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1916150

</td><td>

Provide a Scriptable API for the External Content Connectors to get datasource-based statistics and a semantic embeddings status

</td><td>

This is a product enhancement.

</td><td>

 

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

 PRB1864807

</td><td>

Composite multi-field facets with one of the sources evaluates as late binding, then for the other source, doesn't return all facets on all tabs

</td><td>

Facets aren't consistent between the 'All' tab and the 'Article' tab for KBs.

</td><td>

1.  Create a multi-field facet for catalog and Kb\_knowledge.
2.  Force late binding for the catalog.
3.  Search by KB number.
4.  Switch between the 'All' tab and the 'Articles' Tab.
5.  Check the facets between both tabs.

 Expected behavior: The facets should be consistent between the 'All' tab and the 'Article' tab.

 Actual behavior: Some facets don't show on the 'All' tab.

</td></tr><tr><td>

AI Search

 PRB1889815

</td><td>

KBB should filter out the none-embeddedMatch docs

</td><td>

The default of KKBs sent to LLM is one.

</td><td>

1.  Create KB with two KBBs.
2.  Search for the content that only exists in KBB1.

 Expected behavior: Only KBB1 content is sent to LLM.

 Actual behavior: Both KBB1 and KBB2 content are sent to LLM.

</td></tr><tr><td>

AI Search

 PRB1911804

</td><td>

There's a null point error for the index stats reporter

</td><td>

Note the JavaScript evaluation error on 'new sn\_ais. IndexStatsReporter\(\) .reportAllDataSource EmbeddingStats\(\);'.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1904981

</td><td>

There's a console error after selecting the follow-up button for KG NLQ queries

</td><td>

There's a null citation in the chat.

</td><td>

1.  Open a ynowassist instance.
2.  Enable Dynamic Window on a portal.
3.  Search for a query, 'List of all companies'.
4.  Wait for the synthesized response to load.
5.  Select the **Followup** button.

 Notice the console error and last citation is loaded as null.

</td></tr><tr><td>

AI Search UX

 PRB1907541

</td><td>

Revert unused synthesized v2 format code

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Analyst Workbench

 PRB1868095

</td><td>

The proper user message when a project has error isn't shown

</td><td>

The correct message should be shown to the user when a project has an error.

</td><td>

1.  Create a project.
2.  Mine a project and have some error like no records like such.

 Expected behavior: The error message should be shown to the user.

 Actual behavior: The error message isn't shown to the user.

</td></tr><tr><td>

Analyst Workbench

 PRB1868099

</td><td>

Evaluation projects should have the 'Edit' option on the 'Process projects' page, even if the user is unable to edit

</td><td>

Only a user with elevated privileges can see the 'Edit' option, even though it should be seen by all users even if they're unable to edit.

</td><td>

1.  Open the 'Process projects' page.
2.  Check for an Evaluation project.
3.  Select the three dots.

 Expected behavior: The Edit option shows where ever the project is available.

 Actual behavior: The 'Edit' option is only seen by a user with elevated privileges.

</td></tr><tr><td>

API Usage Analytics Dashboard

 PRB1842140

</td><td>

API\_INT Semaphore queue depth shows a negative value in stats.do misguiding analysis and troubleshooting

</td><td>

There are two problems. First, the count shouldn't go negative when any exception happens. Second, it shouldn't throw an exception, which ultimately drops the request on the floor and never responds to the browser.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1907408

</td><td>

A rollback blocking the install/upgrade for non-global scope users in a domain-separated instance

</td><td>

Non-global domain users have been blocked from being able to install/upgrade on domain-separated instances. There is now a fix to allow this behavior and hence this code change made on App Manager can now be rolled back.

</td><td>

 

</td></tr><tr><td>

Appointment Booking

 PRB1902492

</td><td>

Issue with missing otherInputs in taskRecord parameter of rest API payload for Appointment Booking Unified UI after upgrading to Yokohama

</td><td>

In the Yokohama release, a common UI for appointment booking was implemented and otherInputs was missed from the payload. Add the otherInputs parameter in taskRecord like in the previous UI.

</td><td>

 

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1909861

</td><td>

A lazy load of AMB messages cause an additional query for every message published

</td><td>

A performance improvement implemented in Yokohoma was designed to optimize database operations by loading the actual AMB message column from the database only when subscribers for that message exist. However, this optimization has been compromised by a request that updates the redelivery cache, which inadvertently causes the new query to be triggered for every published message, regardless of subscriber status. The intended performance benefit of selective database querying is being negated, as the system is now querying the database for all messages instead of only those with subscribers.

</td><td>

 

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1910946

</td><td>

The Record Watcher \(RW\) Asynchronous Message Bus \(AMB\) message censor doesn't work when AMB lazy load is turned off

</td><td>

When glide.amb.message. lazy.load is set to 'false', having a record open in two browsers and updating it in one doesn't update it in the other browser.

</td><td>

1.  Set glide.amb.message.lazy.load to 'false'.
2.  Open a record in two different browsers.
3.  Update the record in one browser.

 Notice that the **Record** field in the other browser window isn't updated.

</td></tr><tr><td>

Authentication

 PRB1835271

</td><td>

IDP-initated SLO fails if 'Auto Redirect IdP' is 'True'

</td><td>

 

</td><td>

1.  Log in as an admin user.
2.  Use Azure IDP to set up Security Assertion Markup Language \(SAML\) on Service Portal \(SP\).
3.  Enable Auto to redirect IdP as 'True'.
4.  Open an incognito window.
5.  Log in to Azure IDP.
6.  Log in through an SSO user in Service Portal.
7.  Log out from Azure IDP.

 Expected behavior: The user should be logged out from both SP and IDP.

 Actual behavior: The user is not logged from IDP only not from SP.

</td></tr><tr><td>

Authentication

 PRB1917269

</td><td>

Authentication Agentic AI agent controls

</td><td>

This is a product enhancement.

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

 PRB1898674

</td><td>

Agentic execution runs into a permission error

</td><td>

There's an error in the logs: 'The attempt to retrieve your open tickets failed due to a permissions error \(read access to sn\_hr\_core\_case not granted\). Please advise on how to proceed or if there is an alternative method preferred to access your open tickets.'

</td><td>

1.  Get the latest ynowassist with July apps.
2.  Enable ticket status agent.
3.  From the Virtual Agent as an admin, enter 'what is the status of my tickets'.

 Observe the error.

</td></tr><tr><td>

Client Scripts

 PRB1818770

</td><td>

When an onchange script on name-value pairs with a field, the value on the field doesn't change dynamically in the Service Operations Workspace

</td><td>

The state of the NameValue field doesn't change from 'New' to 'In Progress' in the Service Operations Workspace platform UI.

</td><td>

1.  Log in to a Xanadu base instance.
2.  Created a field of type Name-Value pairs in the Incident table.
3.  Create an onchange client script with the following details:
    1.  Type: Onchange
    2.  Field: State
    3.  UI type: Script
4.  Open any incident.
5.  Navigate to SOW view.
6.  Add the field that was created in step 2.
7.  Change the state between 'New' and 'In Progress' to see the **NameValue** field change in the platform UI.
8.  Open the incident in SOW.
9.  Attempt to change the state between 'New' and 'In Progress'.

 Notice that the NameValue field doesn't change in platform UI.

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB1895738

 [KB2183302](https://hi.service-now.com/kb_view.do?sysparm_article=KB2183302)

</td><td>

A fix script causes high DB CPU load/DB backup failure/long running jobs

</td><td>

After upgrading to Yokohama, Discovery jobs querying cmdb\_rel\_ci is long running and causing high DB CPU load and DB back-up failure.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Column Level Encryption Enterprise

 PRB1879823

</td><td>

The 'Mass Decryption' job doesn't decrypt all the records in the table after EFC is turned off due to escaped and not decryptable HTML fields

</td><td>

The modified row with the HTML value that had the encryption configuration deactivated still display the encrypted value.

</td><td>

1.  Create a table with **Name** \(field type: string\) and **HTML**\(field type: html\) fields.
2.  Create an active encryption configuration on the **HTML** field of the new table.
3.  Insert some rows of data into the new table.
4.  Deactivate the encryption configuration on the table's **HTML** field.
5.  Update a record.
6.  Change the **Name** field to something else.
7.  Schedule a decryption job on the column.

 Expected behavior: Both rows are decrypted.Actual behavior: The modified row's HTML value still shows the encrypted value.

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

 Expected behavior: no\_access\_module doesn't show up in the list.Actual behavior: no\_access\_module shows up in the list.

</td></tr><tr><td>

Column Level Encryption

 PRB1837482

</td><td>

Attachment generation fails when running a flow or background job as a system user, as it tries to encrypt even though it doesn't have access to the module

</td><td>

GlideSession is being reused in background jobs/flows, which already set some values in the session such as CryptoModulePicker. Since CryptoModulePicker is already set, when it attempts to encrypt, it doesn't have access to the crypto module and fails. Any session that has been previously used by an admin user with access will lead to the error when that session is used by the system.

</td><td>

1.  Create a encryption module.
2.  Create a new role 'test123'.
3.  Add this role to the admin user.
4.  Create a MAP of the type 'Role'.
5.  Assign to 'test123' role
6.  Create an **Attachment encrypted** field configuration on the Incident table.
7.  Navigate to the sysauto\_script table.
8.  Run the scheduled script while logged in as 'System administrator'.
9.  Notice that it should be encrypted.
10. Set the 'run\_as' field value through the background script, from the scheduled job so it runs as system: var gr = new GlideRecord\('sysauto\_script'\); gr.get\('sys\_id'\);gr.setValue\("run\_as", ""\);gr.update\(\);

 Expected behavior: It shouldn't encrypt the attachment.Actual behavior: It attempts to encrypt and fails with the error, 'SEVERE \*\*\* ERROR \*\*\* Crypto module access is denied for an attachment'.

</td></tr><tr><td>

Column Level Encryption

 PRB1896503

</td><td>

Data Migration Job summary doesn't have the correct pending list for incomplete EFCs

</td><td>

 

</td><td>

1.  Migrate from Legacy CLE to KMF-CLE.
2.  Ensure there are some Migration pending EFCs after data migration job is done.

 Notice that when the job restarts, it only pick ups the migration pending EFCs from the job summary, but there EFCs marked as 'Migration Pending' on EFC table.

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

 PRB1899149

</td><td>

Remove sn\_cmdb\_admin from itil\_admin, sn\_cmdb\_editor from itil, and add CUD access to sn\_cmdb\_admin / sn\_cmdb\_editor

</td><td>

An itil user should have CUD access by default and users with the itil role contains sn\_cmdb\_editor, not sn\_cmdb\_user. Remove CUD from itil, and a user with the itil role no longer has CUD access because of removing CUD from sn\_cmdb\_editor.

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB1893694

</td><td>

On guided setup, the 'Activate customer central' page displays 'no record found'

</td><td>

There's an issue with the plugin name being hard-coded in configurations. In Yokohama, the 'Customer Central' plugin ID was changed from com.sn\_csm\_customer\_central to sn\_customercentral. The guided setup is hardcoded to point to com.sn\_csm\_customer\_central.

</td><td>

1.  Log in to an instance.
2.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup**.
3.  On the 'Getting Started' page of the guided setup, select **Get Started**.
4.  In the Customer Central - Customer Information or Customer Central - Customer Activity category, view the list of tasks to configure the feature.
5.  Scroll to 'Activate Customer Central' and select **Configure**.

 Observe that the button opens a page displaying 'Record Not Found'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1882454

</td><td>

db-dml-test failures on Yokohama for DBInsertFullUnicodeIT .testTrickyDBAction and DBInsertFullUnicodeIT .testTrickyGlideRecord

</td><td>

Data inserted via GlideRecord is encoded twice, and the SQL search query uses only one level of encoding in the 'Where' clause, causing the search to return incorrect results.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1896536

</td><td>

The 'Database' view isn't working for Workflow Data Fabric tables

</td><td>

An error is generated: 'Logic Error: No Join Found for table: sys\_user: no thrown error'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1907396

</td><td>

Graph API needs to honor data filtration/data filter rules

</td><td>

 

</td><td>

1.  Create a data filter.
2.  Query against that table.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1841958

</td><td>

Failure to clean any records on a gateway table if more than 100 records are found

</td><td>

This issue is caused by UnreferncedRecordFinder.verifyUnreferencedRecords returning no records to delete, despite initially finding all the correct records in the unreferencedRecordFinder .getChunkOfUnreferenced RecordIds call.

</td><td>

1.  Create a gateway DB.
2.  Migrate sys\_audit to the gateway DB.
3.  Orphan over 100 records.
4.  Create a new sys\_unreferenced\_record\_rule with the following values:
    1.  Tablename = Sys Audit
    2.  Conditions: tablename = cmdb\_ci\_computer
    3.  Reference type = Document ID
    4.  DocID filed = Document Key
    5.  **DocId table name** field = Table Name
5.  Run the command 'Refresh sample of unreferenced records'.

 Expected behavior: At least 1000 sample records should be visible below on the form view of the URC rule created.

 Actual behavior: No sample preview records are found.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1867090

</td><td>

Tables available in the Unreferenced Table Cleaner \(URC\) rule creation form are unconstrained

</td><td>

Configure an inclusion list for available table names when creating new URC rule, and create a new glide property 'glide.db.unreferenced\_record \_cleaner.enabled\_tables'.

</td><td>

Attempt to create a URC rule.

 Expected behavior: Only a subset of tables should be available.

 Actual behavior: All tables are available.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1913617

</td><td>

Turn off monthly and yearly stats aggregator jobs

</td><td>

 

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

Database Persistence

 PRB1906360

</td><td>

The 'Re-Activate All DF Reference Elements' UI action doesn't activate the data fabric \(DF\) reference element

</td><td>

 

</td><td>

1.  Navigate to sys\_dictionary.
2.  Find a Glide table collection that has a reference element referencing a Workflow DF table.
3.  Select the **De-Activate All DF Reference Elements** UI action.
4.  Verify that all reference elements that are referencing the DF table get de-activated \(active =false\).
5.  Select **Re-Activate All DF Reference Elements** UI action.
6.  Notice that nothing happens.

 Expected behavior: All DF reference elements should be activated again \(active = true\).

 Actual behavior: All DF reference elements remain inactive.

</td></tr><tr><td>

Database Persistence

 PRB1907489

</td><td>

Update WDF readiness system properties to be changed by users with elevated privileges only

</td><td>

 

</td><td>

Update the properties as an admin user.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1893749

</td><td>

Trail License button is not displayed on a new TD instance after installing Data Discovery and Data Privacy App

</td><td>

 

</td><td>

1.  Create a new TD instance.
2.  Install Data Discovery and the Data Privacy App.
3.  Navigate to 'Data Discovery Job' page.

 Expected behavior: The **Trial License** button is displayed.

 Actual behavior: The **Trial License** button is not displayed, and the user is able to schedule the job.

</td></tr><tr><td>

Declarative Actions

 PRB1876861

</td><td>

Customizing a flow from 'Order line item' loads a blank configuration UI screen for Order Agent and Order Admin users

</td><td>

Both Order.agent and Order.admin users are redirected to a blank page when the configuration UI page should open after selecting 'Customize' for ab order line item.

</td><td>

1.  Impersonate an Order.agent or Order.admin user.
2.  Create an order.
3.  Navigate to the 'Order line items' tab.
4.  Select **New**.
5.  Create an order line item for a product offering.
6.  Select **Customize**.

 Expected behavior: Selecting **Customize** should open the configuration UI page.

 Actual behavior: Selecting **Customize** redirects the user to a blank page.

</td></tr><tr><td>

Developer Sandboxes

 PRB1903573

</td><td>

Clone preservers need to be added for all clone profiles

</td><td>

Developer Sandboxes \(DSB\) should be present in the profile preserver list.

</td><td>

1.  Create a new custom clone profile.
2.  Search for DSB preservers in profile preserver list.

 Expected behavior: DSB preservers are there.

 Actual behavior: DSB preservers not there.

</td></tr><tr><td>

Discovery

 PRB1800638

</td><td>

Preventing the scenario of running Simple Network Management Protocol \(SNMP\) GetNext on the same Object Identifier \(OID\) repeatedly

</td><td>

 

</td><td>

 

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

 PRB1899269

</td><td>

Discovery dedicated node job criteria used for some users doesn't exclude Cloud Discovery jobs in the Yokohama release

</td><td>

 

</td><td>

1.  Create/Update a node in the sys\_cluster\_state table with the node type containing job criteria 'nameSTARTSWITH async: disco^ ORname STARTSWITH events process discovery ^ORname=Cancel Discovery^ ORdocument = discovery\_schedule ^nameNOT LIKEAzure^ nameNOT LIKEAWS'.
2.  Run Azure or AWS discovery.

 It's not expected to see the Cloud discovery traffic on the dedicated node, but it is still going to dedicated nodes.

</td></tr><tr><td>

Discovery

 PRB1899276

</td><td>

The start of the next Discovery schedule in a daisy chain is delayed by the time taken to complete 'discovery.complete' or 'discovery.cancel' events

</td><td>

In instances where the daisy chain is being used, the start of the next Discovery in the chain depends on the time taken to complete 'discovery.complete' or 'discovery.cancel' events . Most of the script actions for these events in their environment have the same default execution order of 100, including 'Discovery Run Next', which triggers the next Discovery. The more script actions with the order 100, the higher the possibility of delay for starting the next Discovery.

</td><td>

1.  Create a daisy chain for Discovery.
2.  Create script actions for discovery.complete and discovery.cancel events with execution order '100', which takes a few minutes to complete.
3.  Run the daisy chain Discovery and check the time taken spent between the complete/cancel of one discovery schedule and the start of the next Discovery schedule.

 Notice that it is greater than the time taken by the new script actions.

</td></tr><tr><td>

Discovery

 PRB1899547

</td><td>

Make error suggestions clearer and link them to useful Knowledge Base \(KB\) articles

</td><td>

After analysis, it was found that the error suggestions for the following codes are insufficient or missing: SN-5301: No sensor defined, SN-1582: Unable to classify, SN-1144: Host is not reachable, SN-1007 : Failed to establish SSH connection, SN-1556: Multiple duplicate records, SN-1561: Multi match, and SN-1558: Missing dependency.

</td><td>

1.  Navigate to the records in the automation\_error\_suggestion table for the error codes listed above.
2.  Create or update the corresponding knowledge base \(KB\) articles.
3.  Link them to their respective error codes.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1896682

</td><td>

Create a system property for max page and max field limits for GenAI use cases

</td><td>

Currently, the max page and max field limits are not customizable.

</td><td>

 

</td></tr><tr><td>

Document Viewer

 PRB1914045

</td><td>

Users are unable to view an attachment when clicking it

</td><td>

The issue is observed for all the components where attachments can be previewed.

</td><td>

1.  Navigate to a 3rd party portal.
2.  Navigate to a catalog item.
3.  Attach an image file or PDF file.
4.  Select the attachment to view.

 The 'Attachment' view fails.

</td></tr><tr><td>

Dynamic Schema

 PRB1895584

</td><td>

Upgrading from Xanadu removes the dynamic attribute store display data and querying since the fix script from PRB1895584 is not applied

</td><td>

In Xanadu, the data in the database is stored incorrectly, and the group is missing an underscore.

</td><td>

1.  Open a Xanadu instance.
2.  Install the XanaduDynamicSchemaFinal.xml update set.
3.  Populate the Incident, CMDB, and alm\_hardware tables from the X\_DS\_PoplulateDataScript.js.
4.  Ensure that on the list view, the dynamic attribute store data on the inc\_dynamic\_schema column, hardware\_dynamic\_schema column, and the cmdb\_dynamic\_schema column.
5.  Upgrade the instance to the latest master.

 Notice the display data on the the inc\_dynamic\_schema column, hardware\_dynamic\_schema column, and the cmdb\_dynamic\_schema column are now gone, and the data in the database did not get correctly changed.

</td></tr><tr><td>

Dynamic Translation

 PRB1899459

</td><td>

Dynamic Translation isn't working after upgrading in Yokohama

</td><td>

The translation feature stopped working and is now throwing the following error in 'Translate Text': 'Error: Cannot read property 'status' from undefined. Detail: Cannot read property 'status' from undefined.'

</td><td>

 

</td></tr><tr><td>

Edge Encryption

 PRB1915259

</td><td>

Users are uable to attach a 10MB file to a record when logged in with an Edge URL

</td><td>

When logged in with the Edge URL and trying to attach an attachment of 10MB to any of the records in the instance, it keeps loading. But when users load attachments with less than 10MB, it works fine. However, with a normal instance URL, the user is able to attach the larger attachments without any issues.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1782170

</td><td>

Inline images coming from encrypted and signed emails processed by the SMIME plugin are lost

</td><td>

Images sent by Outlook may not be decoded properly when both encryption and signing are used in SMIME. The processed email may also contain artifact characters after decoding.

</td><td>

 

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB1909669

</td><td>

Uptake the AI Search EVAM bundle changes for Employee Centre Pro for Web Applications

</td><td>

With this change the following are expected: 1. The image duplication shouldn't be visible for search entries, so no image should be displayed on the left side as thumbnail. 2. Icons would be introduced for category results.

</td><td>

 

</td></tr><tr><td>

Encryption

 PRB1894907

</td><td>

Data migration job doesn't report failure records

</td><td>

 

</td><td>

1.  Insert invalid data that fails data migration job.
2.  Run the data migration job.

 Expected behavior: The job reports failure records.

 Actual behavior: The job doesn't report failure records.

</td></tr><tr><td>

Encryption Support

 PRB1888374

</td><td>

Attaching a file to an incident table doesn't generate a hash value, even though the attachment isn't actually encrypted

</td><td>

Once the encryption of attachments is deactivated on the Incident table, the issue is resolved despite the fact that the attachment isn't getting encrypted when it's on.

</td><td>

1.  Log in to the instance.
2.  Impersonate a system admin.
3.  Navigate to the Incident table.
4.  Select any incident.
5.  Attach a file without an encryption module.
6.  Navigate to the sys\_attachment table.

 Notice that the user will not see the Hash value.

</td></tr><tr><td>

Event Management

 PRB1904735

</td><td>

Existing enrich rules have changes that affect binding \(draft rules\)

</td><td>

The bind simulation presents an incorrect result.

</td><td>

 

</td></tr><tr><td>

Field Service Task Bundling

 PRB1898283

</td><td>

Dynamic Bundling logs aren't accessible to the wm\_admin persona

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Field Service Task Bundling

 PRB1903547

</td><td>

Unable to create bundles with customizations

</td><td>

When a custom field is added to the task grouping policy, the data is not being retrieved.

</td><td>

1.  Create a **Custom** field on the wm\_order table.
2.  Add filter conditions based on **Custom** field on the 'Task grouping policy' table.
3.  Select **Bundle now**.

 Observe that the bundles aren't created.

</td></tr><tr><td>

Flow Engine

 PRB1855808

</td><td>

Callback is not invoked due to null pointer in FlowCallBackExecutor

</td><td>

When an evaluation run from skill kit app is triggered, an attached error log occurred for a particular flow completion, and the run was not marked as complete.

</td><td>

Trigger an evaluation run from skill kit with many dataset records.

 Notice that an attached error log occurs in the instance.

</td></tr><tr><td>

Flow Engine

 PRB1881084

</td><td>

The CurrentContextTracker reset scope and meta stack are in the wrong order

</td><td>

CurrentContextTracker attempts to clean up meta stack and script contexts after a flow execution. Both are reloaded in reverse to how they initially appeared when the flow starts. This happens because the ArrayDeque collection removes elements from the stack. The array from the queue is in the expected order \(A, B, C, etc\). When the elements are added back, the ArrayDeque adds elements at the front of the queue, so iterating from first to last on the list and pushing will result in a reversed stack. So the queue contains \(C, B, A\) instead of \(A, B, C\).

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1893452

</td><td>

AI Agent context isn't properly configured for quick flows

</td><td>

 

</td><td>

Update FlowUserAgentContextIT.java to accurately count the audit.

 Expected behavior: Quick flow tests in FlowUserAgentContextIT pass.

 Actual behavior: Quick flow tests in FlowUserAgentContextIT are failing.

</td></tr><tr><td>

Flow Engine

 PRB1903784

</td><td>

process\_flow.engine related zboot errors in the database dump logs

</td><td>

Errors in the database dump logs from Now Assist.

</td><td>

 

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

 PRB1916146

</td><td>

Callbacks invoked on the FD API in Async Quick and from an AI agent shouldn't run as 'system'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1850039

</td><td>

Code-related text is appearing in the natural language summary for the **Look up records** action

</td><td>

 

</td><td>

1.  Navigate to Workflow Studio with the latest changes.
2.  Navigate to **Create flow** &gt; **Build with Now Assist**.
3.  Use the prompt, 'Find all the logged issues yesterday, also if you find any \#Problem, report the same to manager through email'.
4.  Verify **Look up records** while the response is being generated.

 Notice there is a text present saying, 'logged\_ON\_Yesterday@javascript::gs:beginning....'.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1871518

</td><td>

In the Natural language view, the table's internal name shows up for 'Create Task' \(table problem\_task\)

</td><td>

'Create Task' is displayed as 'Create problem\_task Task'.

</td><td>

1.  Create a flow with Now Assist.
2.  Use the prompt, 'Create a flow that runs every day at midnight, and then find all the newly created problem records for the past day'.
3.  Iterate over them.
    1.  If they are not assigned, assign the problem to the level 1 triage group.
        1.  Move the state to 'triaged'.
        2.  Send a notification to the group.
    2.  If they are assigned, assign multiple records to the level 2 triage group.
        1.  Create a task for each record.
        2.  Wait for the task to be assigned.
        3.  Ask for approval from the manager of the task assignee once the task is assigned.

 Notice that the flow is created in preview, and 'Create Task' is displayed as 'Create problem\_task Task'.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1887330

</td><td>

NaN output results in 'Exception while executing request: Could not deserialize value' when opening the flow execution

</td><td>

.

</td><td>

1.  Create a flow action.
2.  Configure an output for the action of type 'Floating Point Number'.
3.  Make the output NaN via javascript '0/0'.
4.  Add this action to any test flow.
5.  Execute the flow.

 All users see the error, and won't be able to see any flow execution details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1922279

</td><td>

Glide changes for Text2flow

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Granular Delegation

 PRB1840636

</td><td>

Adhoc granular delegation isn't working on production

</td><td>

There's an error in the logs: 'Root cause of JavaScriptException: java.lang.NullPointerException: java.lang.NullPointerException: Cannot invoke 'com.glide.delegation.DelegationRule.isApprovals\(\)' because 'rule' is null: com.glide.delegation. ApprovalDelegationMapper .doesMapRule \(ApprovalDelegationMapper. java:46\)'.

</td><td>

 

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1898736

</td><td>

The host name resolution for IPKI certificate generation isn't successful when the instance is using an alias

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1860223

</td><td>

Hermes Client Metrics Collection loads large records when aggregating client metrics

</td><td>

 

</td><td>

1.  Create 15 topics for an instance.
2.  Produce and consume the message for these topics for at least 15 minutes.
3.  Validate the 'hermes\_metrics\_collection' table.
4.  Check the number of the metrics rows available to verify that the number metrics are 10k.

 Expected behavior: No errors are observed during metrics aggregation.Actual behavior: Notice the error that contains, 'WARNING \*\*\* Large Table: Table handling an extremely large result set'.

</td></tr><tr><td>

Horizon Component Library

 PRB1892046

</td><td>

The auto-resize limit doesn't work when the text area is read-only

</td><td>

There's a 'now-textarea' read-only component that the user is using on a regular workspace page. The user wants to expand the text area's height, but that is only possible through the 'rows' property. The user is currently using the 'autoresize' and 'autoresizeRowsLimit' properties. However, since the field is read-only, the height of the text area isn't expanding. When they use an existing template from the UI Builder page, there's no way to directly change the property of the 'now-textarea' component. If it was a regular empty UIB page, the user would have been able to change the 'rows' property.

</td><td>

 

</td></tr><tr><td>

HTML Field Type Editor

 PRB1881482

 [KB2291304](https://hi.service-now.com/kb_view.do?sysparm_article=KB2291304)

</td><td>

Read-only **HTML** fields aren't rendering the content properly

</td><td>

Users are unable to see the content of the field. The field becomes read-only and no content appears.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HTML Sanitizer

 PRB1840143

</td><td>

OpenITTicket-Web Client gets the santization message, 'You have inputted sensitive information and it has been cleared from the chat history'

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

</td></tr><tr><td>

HTTP Client

 PRB1916723

</td><td>

The 'Request to Now' LLM media action fails due to missing changes made to support multipart on a sync client

</td><td>

Multipart requests support should be added to ynowassist so that the Generative AI Controller \(GAIC\) can change the 'Now LLM Media' flow to use the Now LLM Connection Alias.

</td><td>

 

</td></tr><tr><td>

Identity

 PRB1894590

</td><td>

An admin user is able to change the 'Table name' while selecting the AI agent from the list

</td><td>

There's a new plugin and table for the agent role configuration.

</td><td>

1.  Ensure that 'com.glide.identity.agent.security' is installed on the instance.
2.  Log in as an admin to an instance.
3.  Open the list view for the 'sys\_agent\_access\_role\_configuration' table.
4.  Select **Add new record**.
5.  Select the **Search** icon beside 'Agent' entry.

 Expected behavior: The user shouldn't be allowed to change the 'Table name' from the pop-up window.

 Actual behavior: The agent is able to select non-default tables from the list in pop-up window.

</td></tr><tr><td>

Identity

 PRB1905443

</td><td>

Capitalization is missing for a **WSA** field notification message

</td><td>

 

</td><td>

1.  Log in to any instance on track/ynowassist.
2.  Navigate to **All** &gt; **Users** or open the sys\_user.list table.
3.  Open any user record.

 Expected behavior: The message should be 'Please use identity type field instead'.

 Actual behavior: The **WSA** field notification message doesn't start with a capital: 'please use identity type field instead'.

</td></tr><tr><td>

Incident Communications Management

 PRB1901722

</td><td>

Add a workaround variable in Resolution Communication \(Technical\) and Resolution Communication \(Business\)

</td><td>

If a skill is active, then add the 'workaround' GenAI variable in the template: Resolution Communication \(Technical\) and Resolution Communication \(Business\).

</td><td>

 

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB1908309

</td><td>

Authentication fix for recurring clones

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1844370

</td><td>

Reconstructed process plan returns incorrect information when fetching a plan containing a data stream

</td><td>

The flow executes with a data stream, even if the method returns as 'false'.

</td><td>

1.  Install IntegrationHub Enterprise Pack.
2.  Create a data stream.
3.  Publish it within a flow.
4.  Execute the flow.
5.  Retrieve the reconstructed process plan in an IDE by invoking the method 'OperationUtils.getReconstructed ProcessPlan\(contextID\). hasDataStream\(\)'.

 Notice that this method returns false, even though the flow executes with a data stream present.

</td></tr><tr><td>

Integration Hub

 PRB1901076

</td><td>

Generative AI Controller \(GAIC\) fails to handle some streaming responses due to an unexpected format

</td><td>

Not all streaming responses are being returned by GAIC. Upon investigation, the issue was traced to a class in the flow processing code. This component currently supports only SSE or JSON data formats. However, some responses are returned in a different format, which causes the consumer to error out.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1911068

</td><td>

GlideServer SQL API/Query Service limits

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1911069

</td><td>

JDBC driver REST APIs for the ServiceNow SQL API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Language and Translations

 PRB1886122

</td><td>

The user observes the wrong translation on Risk Workspace for the sn\_risk\_advanced plugin component

</td><td>

Incorrect translations on the Risk workspace for sn\_risk\_advanced plugin component.

</td><td>

1.  Navigate to Yokohama P1.
2.  Install GRC: Risk Management Workspace plugin with demo data.
3.  Install a i18n for German translations.
4.  Navigate to **Risk Workspace** &gt; **Lists** &gt; **Risk assessments** &gt; **Risk Register**.
5.  Open a record.
6.  Select **View**.
7.  Observe that all 'subtitles' are showing correctly in the open record.
8.  Change the language to German.

 Expected behavior: The text is translated.

 Actual behavior: Subtitles are shows as 'advanced\_risk\_assessment\_component...'.

</td></tr><tr><td>

License Usage

 PRB1920048

</td><td>

The 'Remove candidate' link in the Progress Indicators card of the Key Metrics section isn't working

</td><td>

In the Key Metrics, 'Removal candidates' should link to the list view of removal candidates.

</td><td>

1.  Install the plugin \(com.sn\_samp\_master\_ws\) or store app with demo data.
2.  Activate all Software Asset Management Professional plugins, including Software Asset Workspace.
3.  Navigate to **Workspaces** &gt; **Software Asset Workspace**.
4.  Select **License usage module** from the left side menu.
5.  Select **Publisher Adobe Systems**.
6.  Navigate to **Key Metrics** &gt; **Progress Indicators**.
7.  Select **Removal candidates**.

 Expected behavior: The user should be navigated to the list view of the removal candidates.

 Actual behavior: Nothing happens when the 'Removal Candidates' link is selected.

</td></tr><tr><td>

Lifecycle Events

 PRB1881856

 [KB2208698](https://hi.service-now.com/kb_view.do?sysparm_article=KB2208698)

</td><td>

When a Lifecycle Event \(LE\) case is created directly in the 'Ready' state, the message 'Case reopened by...' is added to the work notes

</td><td>

This issue only happens in Yokohama and not in Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1875957

 [KB2115689](https://hi.service-now.com/kb_view.do?sysparm_article=KB2115689)

</td><td>

The 'Personalize List' option isn't working as expected

</td><td>

When using the 'Personalize List' option, if users click anywhere on the list other than the slush bucket, the slush bucket disappears. This causes the list to get stuck, making it impossible to access any of the list elements such as filter, personalize, UI actions, or the contextual menu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1880653

</td><td>

After a Yokohama upgrade, special characters are incorrectly interpreted in a list when using 'Show column filtering row' only in workspaces

</td><td>

The issue is reproduced only on Yokohama instances in list column header filters when using workspaces.

</td><td>

1.  Log in to any Yokohama instance.
2.  Navigate to any workspaces.
3.  Open any lists.
4.  Ensure that the list is enabled with 'show column filtering row'.
5.  Enter any special character in the **Search** filter fields under any column.
6.  Notice the characters get converted to some other hard-coded characters.

 Expected behavior: Characters should remain the same and display list results based on characters matching.

 Actual behavior: Characters get converted to some other hard-coded characters. This issue is reproduced only when using workspaces and works fine in Platform UI.

</td></tr><tr><td>

MetricBase

 PRB1878006

</td><td>

A hanging Clotho server can sometimes cause glide to become unresponsive

</td><td>

A Clotho XMLStats request never returns if Clotho becomes unresponsive, leading to semaphores exhaustion on glide.

</td><td>

 

</td></tr><tr><td>

Metric Intelligence \(Family\)

 PRB1839739

</td><td>

ME queries dashboard configurations that don't filter out metrics without data, and pre-filtering should be added

</td><td>

This may cause a situation where the API returns 10 dashboard configuration with no data, causing the metric explorer to feature an empty metrics graph panel. In addition to this issue, pre-filtering should be added.

</td><td>

1.  Pick a series. \(CI+resource+metric type\) which has some data.
2.  Navigate to **Metrics view configuration**.
3.  Create 10 or more records for the CI class with no source, all with a low order \(such as 10\), for source metric types with no registered metrics.
4.  Create a record for that CI with a metric source that has a registered series with a high order \(such as 200\).
5.  Open the CI in the Service Operations Workspace \(SOW\) in another tab.
6.  Confirm that the widgets in the metric widget have the series covered by the high order metrics configuration record.
7.  Navigate to all properties.
8.  Create a property 'sa\_metric.enable\_dashboard\_query\_prefilter'.
9.  Set the property 'false'.
10. Clear the cache \(cache.do\)
11. Return to the SOW.
12. Refresh the page.
13. Re-open the CI.
14. Confirm that the widget with the order 200 is not shown in the metrics widget.

</td></tr><tr><td>

MID Server

 PRB1898155

 [KB2321207](https://hi.service-now.com/kb_view.do?sysparm_article=KB2321207)

</td><td>

Calculated checks are zero after config\_publish sent a following MID server restart

</td><td>

During policy publish via an ECC queue message, check sum calculations aren't performed on the MID server for policies that have previously been registered. These calculations are responsible for notifying agents tied with the policies and their check instances that changes have been made and a synchronization of the data must be pushed to agents via the WebSocket connection to reflect the changes. The issue arises from the MID server caching the previous policy during a config\_publish message. For agents that register after this message, the schedule message is never sent due to an error associating the cache entry in the MID server with the new agent connection. For updates to existing policies and/or check definitions, the cache isn't updated with them check sum changes indicating the state has changed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1900340

</td><td>

The SSHProviderTerminal JavaScript probe gets stuck when the client sends a large amount of data when waiting for the identification string

</td><td>

 

</td><td>

1.  Simulate a server running on port 22, which returns garbage after a successful TCP connection.
2.  Run the SSHProviderTerminal probe against that server.

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

Mobile Platform

 PRB1835448

</td><td>

Uppercase in the choice value breaks the dependency on the Mobile App

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1843125

 [KB2180787](https://hi.service-now.com/kb_view.do?sysparm_article=KB2180787)

</td><td>

Language should be part of the cache key building scripted screen cache

</td><td>

Questionnaires and Surveys translations in the Mobile Agent app are not working as expected.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Platform

 PRB1901478

</td><td>

Using UI parameters as part of a filter flow leads to a work order task \(WOT\) sys\_id not being read on Field Service Management \(FSM\)

</td><td>

The users experience an 'invalid input' error.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1904246

</td><td>

External content should be supported in standard search results

</td><td>

The user can't see the icon or select the URL without adding an admin.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1905877

</td><td>

For a single attachment case, the attachment title doesn't display

</td><td>

Attachments should be supported in standard search results. Now, for a single attachment case, the attachment title doesn't display. For a multiple attachment case, the count of attachments doesn't display.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1909655

</td><td>

External content in standard search results should be supported

</td><td>

The full URL is truncated.

</td><td>

1.  Log in to latest iOS/Android requestor 20.2 app.
2.  Search the home for a question.
3.  Check SharePoint search results.

 Expected behavior: It should redirect the user to a valid URL.

 Actual behavior: External content in standard search results redirects the user to an invalid URL.

</td></tr><tr><td>

Mobile Platform

 PRB1916140

</td><td>

Mobile Now Assist skill kit in product support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1916141

</td><td>

Attachment and external content for standard search results

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1916148

</td><td>

Mobile NASS entry point update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1919819

</td><td>

An error occurs when returning standard search results that don't have attachments associated with them

</td><td>

This problem occurs with iOS and Android requester 20.2.

</td><td>

1.  Log in as an admin user.
2.  Search for standard search results that don't have attachments associated with them \(for example, iPhone\).

 Expected behavior: Standard search results should return.

 Actual behavior: Error returning standard search results that do not have attachments associated with them.

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

Next Experience User Menu

 PRB1904194

</td><td>

Filter users of type AI Agents from the 'Impersonate user' list

</td><td>

Disable users from impersonating any user of the identity\_type 'ai\_agents'.

</td><td>

 

</td></tr><tr><td>

Now Assist in Document Intelligence

 PRB1876011

</td><td>

Conversation hangs after a topic is selected

</td><td>

In the syslogs related to DocIntel, scheduled job errors occur.

</td><td>

1.  Navigate to the Employee Service Center.
2.  Enter the prompt, 'I need to borrow a loaner laptop for work by tomorrow'.

 Notice that the topic will be selected, and 'Starting 'Loaner Laptop'...' is displayed, but then gets stuck.

</td></tr><tr><td>

Now Assist in Document Intelligence

 PRB1898239

</td><td>

extractData fails to extract text from a CSV file due to an invalid character delimiter issue

</td><td>

Error: 'An unexpected error occurred while processing CSV file: IOException reading next record: java.io.IOException: \(line 1\) invalid char between encapsulated token and delimiter: java.lang.IllegalStateException: IOException reading next record: java.io.IOException: \(line 1\) invalid char between encapsulated token and delimiter...'.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1907557

</td><td>

Modify the sys\_script\_318070047 f3012102 ff5e3136d 86653d.xml for Now Assist panel

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1914236

</td><td>

Some channels aren't supported on enhanced chat

</td><td>

These controls aren't supported on all channels: Dynamic Choice, and Script Output.

</td><td>

1.  Configure enhanced chat in **All** &gt; **Conversational Interfaces** &gt; **Assistants**.
2.  Enable data visualization generation skill in **Now Assist Admin** &gt; **Platform**.
3.  Open Now Assist Portal.
4.  Select **Create a data visualization**.

 Expected behavior: Message asking for utterance appears.

 Actual behavior: Channel not supported appears.

</td></tr><tr><td>

Now Assist Panel

 PRB1914534

</td><td>

Other components should be able to request AIEL to execute a skill

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1916147

</td><td>

AI engagement layer initiative

</td><td>

This is a product update.

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

Now Assist Panel UX for Agents

 PRB1919813

</td><td>

Changes to accommodate new AIEL and Now Assist Panel configurations

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1919814

</td><td>

Changes to accommodate new AIEL and Now Assist Panel configurations

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1919815

</td><td>

Backend changes to align with sunsetted Now Assist Panel chat component and device type

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel UX for Agents

 PRB1919816

</td><td>

Capture invocation start to sn\_aia\_execution\_plan to determine if it ran from playground, trigger, or chat discovery

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1894063

</td><td>

The sendFeedback method throws an error: 'User is not authorized to update log record'

</td><td>

 

</td><td>

1.  Log in to an instance as an admin.
2.  Initiate a conversation with LA.
3.  Log in as a user.
4.  Carry out a conversation.
5.  End the chat.
6.  Modify the LLM generated short description.

 Expected behavior: An edited response field should be updated in the sys\_generative\_ai\_log table.

 Actual behavior: An edited response field isn't updated.

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

 PRB1912079

</td><td>

The homepage deprecation tool isn't populating the correct amount of 'Homepages not deprecated' in Yokohama

</td><td>

 

</td><td>

1.  Open an instance based on Yokohama.
2.  Ensure that the following is installed and up to date: Homepage deprecation help tool \(App id: sn\_home\_page\_depr\).
3.  Add some homepages where they don't have a view that equals category\_default. Ensure that there's a bunch of homepages where the view is empty, and that both homepages aren't used in a dashboard or in a tab.
4.  Navigate to the homepage migration dashboard.
5.  Notice that there's a widget called 'Homepages not deprecated'.
6.  Create 2 pages where the view = category\_default and 5 pages where the view is empty.

 Expected behavior: The amount of homepages not deprecated should display 7.

 Actual behavior: The amount of homepages not deprecated displays the value 2.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1873441

</td><td>

The description is empty for data visualizations in a library

</td><td>

The description is empty for data visualizations in data-visualization-library when the properties 'com.glide.par.unified\_analytics.enabled' and com.glide.par.v\_table\_join.enabled' are 'True'.

</td><td>

1.  Create a data visualization with a description.
2.  Set the property 'com.glide.par.v\_table\_join.enabled' to 'True'.
3.  Notice the description is removed in the library.
4.  Search the same visualization in par\_visualization.LIST.

 Notice that the description can be seen in par\_visualization.LIST.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1863966

</td><td>

On the editing library visualization in the dashboard, the 'Save' prompt doesn't have the correct label after migration

</td><td>

This was initially fixed by PRB1713684 but no case fallback was added for visualisation without stored\_component\_name. The condition 'All stored visualisations will have name populated' is defined.

</td><td>

1.  Migrate a dashboard from the bulk migration in the Migration Center.
2.  Access the dashboard.
3.  Edit the visualization.
4.  Change a property.
5.  Save the dashboard.
6.  Notice that the save prompt appears asking to save to the library or not, or to save a cloned version on the dashboard.

 Expected behavior: The message should say 'How do you want to save your changes to 'visualization name'.

 Actual behavior: The visualization name is empty.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1869607

</td><td>

Platform Analytics Adminstration \(PAA\) always displays the 'UXA' menu

</td><td>

Customers upgrading to Yokohama without migrating won't have the PAA menu since the unified property is 'false' by default.The UXA setting menu is visible under Platform Analytics Administration whether user has run the migration or not.

</td><td>

 

</td></tr><tr><td>

Process Mining External Data Import

 PRB1870059

</td><td>

Record data generation isn't working as expected

</td><td>

The data is cleared from the import table and no records are generated after the user selects 'Create record data'.

</td><td>

Import an external dataset in the external process mining guided set-up.

 Expected behavior: The user is able to create records based on the imported dataset.

 Actual behavior: After selecting **Create record data**, the page remains stuck at the progress view until refresh. After the refresh, the data in the import table is wiped out and no records are generated.

</td></tr><tr><td>

Process Mining

 PRB1882225

</td><td>

Unexpected exceptions don't get propagated up in the log

</td><td>

 

</td><td>

Throw an exception in MdTraceService during log collection.

 Notice that the exception details or stack trace are missing from the logs.

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

 PRB1901994

</td><td>

Process Mining GenAI skills are failing for 3P models

</td><td>

 

</td><td>

1.  Change default provider to something other than the NowLLM model in sys\_one\_extend\_definition\_config.
2.  Initiate the skill.

 Expected behavior: The skill should return a LLM response.

 Actual behavior: The skill doesn't display any key reasons.

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

 PRB1912315

</td><td>

Filter set models are calculated on an incorrect number of cases when filter set conditions match more than 10k results

</td><td>

There's issues with filter sets' data upload: 1. Use the correct page size value for fetching filter set case IDs. 2. Add a header line to a filter set file upload for the second page onwards. 3. Avoid a case count query for filter sets' file names to avoid timeouts while the data file name generates for a full mine.

</td><td>

1.  Mine a project.
2.  Create a filter set on conditions that matches more than 10k cases and less than 20k cases.
3.  Re-mine the project.
4.  See that the filter set model now displays the incorrect case count.

 Expected behavior: It should mine all cases that match the filter sets and display the correct case count.

 Actual behavior: An incorrect case count is displayed for a filter set model.

</td></tr><tr><td>

Process Mining Workspace

 PRB1861801

</td><td>

The count between tables in MDM is incorrect

</td><td>

 

</td><td>

Open the project 'Incidents with Bad Change'.

 Notice that the count of records between the Incident table mine and Change table mine are incorrect.

</td></tr><tr><td>

Process Mining Workspace

 PRB1862573

</td><td>

When the **Contextual** field is used in a contextual condition and the user edits the transition, 'id' is shown in the value list

</td><td>

The user is unable to select other values from the list when 'Priority' is 'id', and the scheduled task panel shows '2' instead of '2 - High'.

</td><td>

1.  Create a project with the Activity as 'State' and contextual activity \(AOI\) as 'Priority'.
2.  Mine and open the Analyst Workbench.
3.  Add a condition with a contextual condition on Advanced Transition.
4.  View the result on the completed state.
5.  Select **Edit** from the 'Applied' filter.

 Observe that the value for 'Priority' shows 'id', and the user is not able to select any other values from the value list; and the scheduled task panel also shows '2' instead of '2 - High'.

</td></tr><tr><td>

Process Mining Workspace

 PRB1879536

</td><td>

Project copied from a Freemium project is accessible to a 'no role' user

</td><td>

The copied mined project is accessible to a 'no role' user, and the permissions itil and snc\_internal role are copied over.

</td><td>

1.  Impersonate as an Analyst User.
2.  Create a copy of the Freemium project.
3.  Observe that it also copies the permissions from the Freemium project \(itil and snc\_internal\).
4.  Mine the project.
5.  Impersonate a 'no role' user.
6.  Navigate to Process Mining workspace.

 Notice that the copied mined project is accessible to a 'no role' user with either an 'itil' or snc\_internal role, and a non-analyst is able to do RCA, Clustering, Show records and Work Notes.

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
8.  Search **KPIs** under Platform Analytics.
9.  Open a PA indicator.
10. Choose an indicator on the incident because the incident is a default template.
11. Select **Run Process Analysis**.
12. Notice that this will trigger the PA API and create a project.
13. Search **PA projects** in the left navigation.
14. Open it under 'Process mining'.
15. Notice that the newly created project is displayed. Open it.
16. Select**Edit** in the **Project builder** button.

 Observe that it goes into a continuous loop.

</td></tr><tr><td>

Process Mining Workspace

 PRB1891796

</td><td>

Show an alert instead of a modal and update tool tip for 'Get recommendations' in the Guided Process Configuration

</td><td>

This problem was observed in Yokohama.

</td><td>

Scenario 1:

 1.  Create a process configuration for an entity using 'incident'.
2.  Add a **Textual** field in the 'Process perspectives section'.
3.  Return to the 'Improvement opportunities' page.
4.  Select **Get recommendations** on the 'Automated' tab.

 Notice that the message, 'No recommendations available' appears in an alert pop-up.

 Scenario 2:

 1.  Create a process configuration without filling in 'Process perspectives' section.
2.  Create a project.
3.  Hovers on **Get recommended fields**.
4.  Notice that the tooltip says 'All recommended activity definitions have been added'.
5.  Select **Get recommended fields**.

 Notice that 'No recommendations available' appears in an alert pop-up.

</td></tr><tr><td>

Project Management

 PRB1883485

</td><td>

A demand state isn't updating to 'Completed' after a project is created from a demand

</td><td>

This problem was observed in Yokohama.

</td><td>

1.  Hop into an instance.
2.  Create a new demand
3.  Select the **Create Project** related link.
4.  Notice the 'Demand' state is not changed.
5.  Refresh the page, or reopen the same demand.

 Notice that the state is changed to 'Completed'.

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

Related List Action Model

 PRB1889099

</td><td>

When creating Attribute Adjustment for Price list line, the Price List Line id is not getting defaulted in the Attribute Adjustment form

</td><td>

This issue is noticed in Yokohama.

</td><td>

1.  Hop on or log in to a Yokohama instance.
2.  Navigate to CSM/FSM Configurable Workspace.
3.  Create new a Price List.
4.  Create new a Price list line for the Product Offering Home Automation Hub.
5.  Set the Attribute adjustment for the Home Automation Hub price list line.
6.  Check the Attribute adjustment form.

 Expected behavior: Apply to all Price lists should be unchecked and Price list line should be pre-populated with price list line id.

 Actual behavior: In the Attribute adjustment form, Price Line line is disabled and not pre-populated with price list line id.

</td></tr><tr><td>

Reporting

 PRB1892235

</td><td>

When accessing scheduled reports, users are getting an error

</td><td>

When accessing scheduled reports, users get the error: 'Part of the query on par\_coreui\_migration \_bridge\_sysauto has been ignored because of insufficient access for 'query\_match' operation' for non-admin users.

</td><td>

 

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

 PRB1894354

</td><td>

A chat attachment doesn't go through to the user's side

</td><td>

.

</td><td>

1.  Install 'Advanced Work Assignment' \(AWA\) for HR Service Delivery \(HRSD\) in any Yokohama instance.
2.  Create a queue in AWA for the HRSD scope.
3.  Log in as an agent and try to send the attachment.

 See that it is failing.

</td></tr><tr><td>

Roles

 PRB1905646

</td><td>

A upgrade fix\_script is taking more than 5 minutes to set the identity type for 8M records

</td><td>

An existing user should have an identity type.

</td><td>

1.  Take a Xanadu instance.
2.  Create/setup 8M records in the sys\_user table.
3.  Upgrade the instance to the latest track/ynowassist build.

 Notice that the total upgrade has taken 36 minutes. The fix script to update identity\_type for sys\_user records is taking 5 minutes.

</td></tr><tr><td>

Roles

 PRB1906067

</td><td>

An AI Agent's identity type should be un-editable in the 'List' view

</td><td>

'New User' creation should have an identity type.

</td><td>

1.  Create an AI-agent type record in the sys\_user table.
2.  Open that record.
3.  Observe that identity\_type is uneditable there.
4.  Open the sys\_user table in the 'List' view.
5.  Try to edit the identity\_type of AI-Agent records.

 Expected behavior: The user should be blocked from editing the identity-type of AI-Agents from the 'List' view.

 Actual behavior: The choices option displays to the admin to modify the identity-type.

</td></tr><tr><td>

Roles

 PRB1916157

</td><td>

Agent role controls for Identity type

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1916160

</td><td>

Agent role inheritance restriction

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1888111

</td><td>

Handle ignored the state update on WM jobs correctly

</td><td>

Check ml\_solution state before marking it as ignored. Jobs are marked as 'ignored' when the ml\_solution state is still 'in progress'.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1890329

</td><td>

Handle conflict API for the default intraday configuration

</td><td>

 

</td><td>

1.  Set up intraday configuration as the default.
2.  Create event for any qualifier.
3.  Open a work order task of the same qualifier when scheduled intraday job is triggered for the event.

 Expected behavior: The banner message for conflict resolution should be displayed.

 Actual behavior: The banner message will not appear when there is a default intraday configuration that will run for all the qualifiers active in the instance.

</td></tr><tr><td>

Schedule Optimization

 PRB1893394

</td><td>

Support the intraday attribute by overriding the configuration for conflict API

</td><td>

 

</td><td>

Create an Intraday configuration with 'Attribute override'.

 Notice that the conflict API doesn't consider the attribute override.

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

 PRB1897154

</td><td>

Agent Shift horizon time isn't considered correctly for an Intraday run

</td><td>

 

</td><td>

1.  Create agent shifts for today and tomorrow.
2.  With 10+ work order tasks \(WOT\) qualifying for current intraday run.
3.  Run the Intraday job.

 Expected behavior: The WOTs should be assigned within a current day. No WOTs should be assigned for next day.

 Actual behavior: WOTs are assigned to the next day.

</td></tr><tr><td>

Security Attributes

 PRB1852325

</td><td>

GlideSecurityManager. dotWalkQueryConditionToBuild QueryElementToGRMap expands dot-walked fields unnecessarily

</td><td>

When executing a query through the Table API or GlideRecordSecure, dot-walked conditions are expanded and the data is subsequently thrown out and not used if all ACLs on the target table are role-based.

</td><td>

1.  Create a rest table API or GlideRecordSecure directly against cmdb\_rel\_ci.
2.  Dot-walk to parent or child in conditions against cmdb\_rel\_ci.

 Expected behavior: GlideSecurityManager doesn't query for data that is not used.

 Actual behavior: GlideSecurityManager queries for the dot-walked condition fields, and throws them away shortly after.

</td></tr><tr><td>

Security Attributes

 PRB1916143

</td><td>

'Are You an Agent?' security attributes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Security Attributes

 PRB1916145

</td><td>

Default access posture security attribute

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1913500

</td><td>

script\_include\_names cache flushes are frequent and expensive

</td><td>

This may contribute to semaphore exhaustion during plugin install.

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB1876659

</td><td>

An admin user can't edit the catalog item in Catalog Builder

</td><td>

For an admin user, the role named 'catalog\_builder\_editor' is not mapped . Even if it's mapped manually, the user is still unable to edit the item using Catalog Builder.

</td><td>

1.  Log in as an admin user.
2.  Pick the latest track/catalogbuilder instance.
3.  Navigate to **Maintain items** &gt; **Standard Laptop**.
4.  Attempt to select **Edit in Catalog Builder**.

 Expected behavior: It should launch the catalog item for editing in Catalog Builder.

 Actual behavior: The error message appears, saying the user is not authorized.

</td></tr><tr><td>

Service Catalog Builder

 PRB1877599

</td><td>

Template is created from scratch; mask and url base instance questions are available in item level for Catalog Builder

</td><td>

 

</td><td>

1.  Create a catalog item template.
2.  Don't change any restrictions at the question level.
3.  Notice that two question types are selected, 'mask' and 'url'.
4.  Create a catalog item with this template.

 Expected behavior: 'mask' and 'url' shouldn't be available for selection in the question subtype for single lines.

 Actual behavior: 'mask' and 'url' are available.

</td></tr><tr><td>

Service Catalog Builder

 PRB1878524

</td><td>

The 'Annotation' tab is missing from all newly supported question types in Catalog Builder

</td><td>

Support new variables in catalog builder.

</td><td>

1.  Log in to the instance as catalog\_builder\_editor.
2.  Navigate to question wizard from the item creation flow.
3.  Choose a question type such as text, subytype - url, or any new type in builder.

 Expected behavior: The 'Annotation' tab should appear.

 Actual behavior: The 'Annotation' tab does not appear.

</td></tr><tr><td>

Service Catalog Builder

 PRB1879309

</td><td>

**Reference qualifier** field is displayed as a **Single line text** field in Catalog Builder

</td><td>

Additional features for existing variables in Catalog Builder.

</td><td>

1.  Log in to the instance with the catalog\_builder\_developer role.
2.  Navigate to Catalog Builder.
3.  Select**Choice** as the 'Variable type'.
4.  Select **Sub type** as a list with values from the table.
5.  Navigate to the 'Additional details' tab.
6.  Select **Advanced** as the 'Reference qualifier type'.
7.  Validate the **Reference qualifier** field.

 Expected behavior: The **Reference qualifier** field should be multi-line text field.

 Actual behavior:The **Reference qualifier** field is single line text field.

</td></tr><tr><td>

Service Catalog Builder

 PRB1879568

</td><td>

Values are auto-populated in some **Lookup** fields once the table is selected

</td><td>

Additional features for existing variables in Catalog Builder.

</td><td>

1.  Log in to the instance with the catalog\_builder\_developer/catalog\_builder\_editor role.
2.  Navigate to Catalog Builder.
3.  Select **Choice** as the variable type.
4.  Select 'Sub type' as a list with values from table.
5.  Navigate to the 'Additional details' tab.
6.  Select the table as 'cmn\_location'.
7.  Verify **Field \(what should be displayed and stored\)** and **Lookup label** field\(s\).

 Expected behavior: The **Lookup** field and lookup label should be empty.

 Actual behavior: The **Reference qualifier** field is a **Single line text** field.

</td></tr><tr><td>

Service Catalog Builder

 PRB1879613

</td><td>

Incorrect message is displayed for catalog\_builder\_editor for a variable with an Advanced reference qualifier

</td><td>

Additional features for existing variables in Catalog builder .

</td><td>

1.  Add a variable list with values from table as a catalog builder editor.
2.  Log in as an admin user.
3.  Open the same Catalog Builder item.
4.  Open the question.
5.  Navigate to **Additional details**.
6.  Select 'Advanced' as the reference qualifier type.
7.  **Save** the change.
8.  Log in with an editor role.
9.  Navigate to the same item and variable.
10. Verify the condition builder in 'Additional details'.

 Expected behavior: The condition builder should be hidden and the message, 'This question contains advanced filter conditions. You do not have the required permissions to modify it' should be displayed.

 Actual behavior: The condition builder is hidden and the message, This question contains advanced filter conditions that cannot be modified in Catalog Builder' is displayed.

</td></tr><tr><td>

Service Catalog Builder

 PRB1879905

</td><td>

Restricted question type count badge is not correct in template question page in Catalog Builder

</td><td>

Support new variables in Catalog Builder.

</td><td>

1.  Log in as an admin.
2.  Navigate to Catalog Builder
3.  Choose any existing template or create a new template.
4.  Navigate to the **Question** section.
5.  Observe that the badge with the count for the restricted question is 5.
6.  Open the selector.

 Notice that there are 8 restricted question types.

</td></tr><tr><td>

Service Catalog Builder

 PRB1879949

</td><td>

Question created through Catalog Builder isn't showing when it's opened for editing

</td><td>

The question is missing in the Catalog Builder, but can still be viewed in Platform.

</td><td>

1.  Login into Catalog Builder.
2.  Navigate to the Catalog Creation flow.
3.  Insert a new question of any type \(for example, a single line\).
4.  **Submit** the item.
5.  Open the item for editing.

 Observe that the question is missing in the Catalog Builder, but is still available in Platform.

</td></tr><tr><td>

Service Catalog Builder

 PRB1880031

</td><td>

Fields and configurations sections are missing for Custom &amp; Custom label question type in Catalog Builder

</td><td>

In addition to the issues with the 'Custom &amp; Custom' label question type, the **Macro** and **Summary Macro** fields are missing in 'Additional details' tab and the 'Default value' tab is missing.

</td><td>

1.  Login as a catalog\_builder\_developer.
2.  Navigate to **Catalog Builder**.
3.  Create from scratch.
4.  Enter an item name
5.  Navigate to the **Question** section.
6.  Create new question as 'Custom'.
7.  Observe the configuration sections.

 Notice that the 'Permissions' and 'Auto populate' tabs are displayed for the label question type 'Custom &amp; Custom', which isn't expected behavior. For catalog\_builder\_editor, the question type 'Custom &amp; Custom' label is completely missing.

</td></tr><tr><td>

Service Catalog Builder

 PRB1880041

</td><td>

Issues with the rich text label in Catalog Builder

</td><td>

In addition to issue for the rich text label, the tooltip text box is present in the 'Questions' tab, and 4 out of 5 fields in the 'Availability' section are unchecked.

</td><td>

1.  Login as a catalog\_builder\_developer.
2.  Navigate to **Catalog Builder**.
3.  Create from scratch.
4.  Enter an item name.
5.  Navigate to the **Question** section.
6.  Create a new question with the 'Rich text' label.
7.  Observe the configurations sections.

 Notice that the 'Permission' configuration section is present for rich text label, and is missing in platform.

</td></tr><tr><td>

Service Catalog Builder

 PRB1880597

</td><td>

Unable to update the default values for variables in Catalog Builder

</td><td>

The user is unable to edit the **Default value** field in these different scenarios.

</td><td>

Scenario 1:

 1.  Take the latest build instance of track/catalogbuilder.
2.  Create a new catalog item or open an existing catalog item.
3.  Navigate to the **Question** section.
4.  Attempt to create a new variable.
5.  Provide a default value for the variable
6.  Save the question.
7.  Re-open the question definition.

 Expected behavior: The variable **Default value** field can be edited.

 Actual behavior: It is disabled.

 Scenario 2:

 Open many existing catalog items to edit.

 Observe that the **Default value** field is read-only and can't be edited.

 Scenario 3:

 1.  Create a catalog item variable of any type without a default value.
2.  Re-open the variable definition.

 Observe that it's disabled and user can't edit the variable.

</td></tr><tr><td>

Service Catalog Builder

 PRB1880645

</td><td>

Unable to create client scripts for Record Producers

</td><td>

 

</td><td>

1.  Pick the latest track Catalog Builder instance.
2.  Open a record producer or create a new record producer using Catalog Builder.
3.  Try to create a client script for any variable in the record producer.

 Expected behavior: There is no provision to create a client scripts for record producers.

 Actual behavior: A new section is shown to create a client scripts on record producer variables.

</td></tr><tr><td>

Service Catalog Builder

 PRB1880798

</td><td>

The **Unique values only** checkbox isn't displaying for the variable type list with fixed values in Catalog Builder

</td><td>

Additional feature for existing variables in Catalog Builder.

</td><td>

1.  Add a variable list with fixed values as a catalog builder editor/developer.
2.  Open an existing catalog item.
3.  Enter **Choice** as the type and sub-type as a list with fixed values.
4.  Navigate to the 'Choice' tab.
5.  Verify the checkbox **Unique values only** is available.

 Expected behavior: The **Unique values only** checkbox should be available on the platform for the question type list with fixed values.

 Actual behavior: The **Unique values only** checkbox is not available.

</td></tr><tr><td>

Service Catalog Builder

 PRB1880884

</td><td>

Cannot access catalog item from Catalog Builder if a multi-select \(list collector\) question is added

</td><td>

The user is unable to access the catalog item, and error messages occur.

</td><td>

1.  Open an instance.
2.  Select **Dashboard**.
3.  Select **Build from scratch**.
4.  Select **Standard**.
5.  Enter the item name.
6.  Navigate to the 'Questions' tab.
7.  Select **Insert new question**.
8.  Select **Choice** as the question type.
9.  Select **Multi-select** as the sub question type.
10. Enter details on the 'Question' tab.
11. Enter details on the 'Additional details' tab.
12. Select **Insert question**.
13. **Submit** the form.
14. Return to the dashboard.
15. Attempt to access the newly created catalog item.

 Expected behavior: The user should be able to access and edit the catalog item through Catalog Builder.

 Actual behavior: The user is unable to access the catalog item and an error message occurs, 'You are not authorized to edit this record'. When selecting **Edit**, and another error message occurs, 'Alert level: critical.unable to fetch variable values for producer'.

</td></tr><tr><td>

Service Catalog Builder

 PRB1880949

</td><td>

The **Delete client script** button name is not appropriate

</td><td>

The **Discard** button name should be deleted in the confirmation modal when deleting the client script.

</td><td>

1.  Log in to an instance.
2.  Navigate to Catalog Builder.
3.  Navigate to the **Create catalog item** flow.
4.  Add a name.
5.  Navigate to the client script.
6.  Add some client script.
7.  Select the script.
8.  Select **Delete**.

 Notice that in the confirmation modal, the button name should be deleted.

</td></tr><tr><td>

Service Catalog Builder

 PRB1880953

</td><td>

Client script with a compilation error is also saved

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Navigate to **Catalog Builder**.
3.  Navigate to **Create catalog item flow**.
4.  Add a name.
5.  Navigate to the client script.
6.  Add to the script.
7.  **Save** the script

 Expected behavior: The script shouldn't saved as is in Platform.

 Actual behavior: The script is saved.

</td></tr><tr><td>

Service Catalog Builder

 PRB1881284

</td><td>

For list values from the table for the **Lookup** select box, the **Choice** field is updated in Platform but isn't shown in Catalog Builder

</td><td>

The first value in the **Choice** field that is updated in Platform isn't updated in Catalog Builder.

</td><td>

1.  Create a catalog item through Catalog Builder.
2.  Add a lookup select box question to it.
3.  Navigate to the 'Additional details' tab.
4.  Select **Choices for lookup source** for the lookup selection box.
5.  Select one value for the **Choice** field \(Don't select the first choice\).
6.  Insert the question.
7.  **Submit** it.
8.  Open the catalog item in Platform.
9.  Update the **Choice** field with different value for options \(Don't select the first value\).
10. **Save** it.
11. Open the catalog item in Catalog Builder.
12. Observe the **Choice** field.

 Expected behavior: The value recorded in the **Choice** field in Platform should also show in Catalog Builder.

 Actual behavior: The first value for the **Choice** field from the option is shown in Catalog Builder.

</td></tr><tr><td>

Service Catalog Builder

 PRB1881380

</td><td>

Simple reference qualifier becomes un-editable

</td><td>

The 'Conditions' section can't be seen and can't be edited by the user when the simple reference qualifier is selected.

</td><td>

1.  Log in to the instance.
2.  Navigate to Catalog Builder.
3.  Select **Dashboard**.
4.  Select **Build from scratch**.
5.  Select **Standard**.
6.  Enter the item name.
7.  Navigate to the 'Questions' tab
8.  Select **Insert new question**.
9.  Select **Choice** as the question type.
10. Select **Radio with values from a table** as the sub question type.
11. Enter details on the 'Question' tab.
12. Enter details on the 'Additional details' tab.
13. Select **Lookup source** as **Choices**.
14. Notice that the user should be able to select the simple reference qualifier and add a condition to it.
15. Change the lookup source to 'Table'.
16. Add the table.
17. Select a simple reference qualifier.
18. Add a condition as 'Active is true'.
19. Select **Insert question**.
20. Attempt to edit the question.
21. Observe additional details tab.

 Expected behavior: The user should be able to see previously added condition and should be able to edit it.

 Actual behavior: The user is not able to see the 'Conditions' section when the simple reference qualifier is selected.

</td></tr><tr><td>

Service Catalog Builder

 PRB1881535

</td><td>

Some fields are missing on Platform on the 'Type specification' tab in the list with fixed value variable types

</td><td>

When comparing the fields in the 'Type specification' tab between Catalog Builder and Platform, some fixed value variable types are missing in Catalog Builder.

</td><td>

1.  Create a catalog item on Catalog Builder.
2.  Add a question with the variable type list with a fixed value.
3.  Add details in the 'Additional details' tab.
4.  Insert the question.
5.  Open the same catalog item on Catalog Builder.
6.  Navigate to the 'Type specification' tab.
7.  Compare the fields on both Catalog Builder and Platform.

 Expected behavior: The Choice table, **Choice** field, and unique values should be present only on Catalog Builder.

 Actual behavior: The Choice table, **Choice** field, and unique values only are missing on Catalog Builder.

</td></tr><tr><td>

Service Catalog Builder

 PRB1881549

</td><td>

Some **Label variable** fields are missing on Platform

</td><td>

Some tabs are missing on Platform.

</td><td>

1.  Create catalog item on Catalog Builder.
2.  Add a question with the variable type 'Label'.
3.  Add all details.
4.  Insert the question.
5.  Open the catalog item on Platform.
6.  Observe the tab.

 Expected behavior: The 'Default value' and 'Permission' tabs should be present on Platform.

 Actual behavior: The 'Default value' and 'Permission tabs' are missing on Platform.

</td></tr><tr><td>

Service Catalog Builder

 PRB1881673

</td><td>

Editing an existing catalog item client script using Catalog Builder shows the sys\_id for the selected question

</td><td>

The selected question shows sys\_id, even though was previously blank before switching between the 'Settings' and 'Actions' tabs.

</td><td>

1.  Create a catalog item with a couple of variables in Platform.
2.  Define onLoad and onChange client scripts on variables.
3.  Open the item using Catalog Builder for editing.
4.  Open the onChange client script definition.
5.  Notice that the selected question is blank, when it should show the display value.
6.  Navigate to the 'Settings' tab.
7.  Return to the 'Actions' tab.

 Notice that it shows sys\_id in the selected question, which is not expected.

</td></tr><tr><td>

Service Catalog Builder

 PRB1881680

</td><td>

The tooltip in the 'Question' tab and checkbox in the 'Availability' tab are missing for **Rich Text Label** fields

</td><td>

Two issues occur in the problem; in the 'Compare Question' tab, the **Tooltip** field is missing on Catalog Builder, and the 'Visible on Summaries' checkbox is missing 'Compare Availablity' tab on Platform.

</td><td>

1.  Create catalog item on Catalog Builder.
2.  Add a question with the variable type 'Rich Text Label'.
3.  Add all details under the 'Question' tab and 'Availability' tab.
4.  Insert the question.
5.  Select **Submit**.
6.  Open the catalog item on Platform.

 Notice that the **Tooltip** field isn't visible in the 'Question' tab on Platform, and the 'Visible on Summaries' checkbox isn't visible on platform. Refer attached ss

</td></tr><tr><td>

Service Catalog Builder

 PRB1881716

</td><td>

For the 'Attachment' variable, the 'Default' tab is missing on Platform

</td><td>

The attachment type variable added on the catalog item in Catalog Builder doesn't appear in Platform.

</td><td>

1.  Navigate to Catalog Builder.
2.  Create a catalog item.
3.  Add an attachment type variable on the catalog item.
4.  Complete all the details.
5.  Insert the question.
6.  **Submit**.
7.  Open same catalog item on Platform.

 Expected behavior:The 'Default' tab should be visible on Platform for the attachment variable.

 Actual behavior: The 'Default' tab isn't visible on Platform for attachment variable.

</td></tr><tr><td>

Service Catalog Builder

 PRB1881725

</td><td>

For custom variables, the 'Permission' tab is missing on Platform

</td><td>

The 'Permission' tab for custom variables doesn't appear on Platform.

</td><td>

1.  Navigate to Catalog Builder.
2.  Create a catalog item.
3.  Add custom type variables on catalog item.
4.  Complete all the details.
5.  Insert the question.
6.  **Submit**.
7.  Open the same catalog item on Platform.

 Expected behavior: The 'Permission' tab should be visible on Platform for custom variables.

 Actual behavior: The 'Permission' tab isn't visible on Platform for custom variables.

</td></tr><tr><td>

Service Catalog Builder

 PRB1882070

</td><td>

Fields under the 'Type specification' tab aren't listed for all the fields for custom/custom with the label variable

</td><td>

Configuration sections of new variable types in Catalog Builder. Fields should have the search option enabled as it is in Platform.

</td><td>

1.  Log in as catalog\_builder\_developer.
2.  Navigate to Catalog Builder.
3.  Create from scratch.
4.  Enter the item name.
5.  Navigate to the 'Question' section.
6.  Create a new question as Custom.
7.  Observe the 'Additional details' section.

</td></tr><tr><td>

Service Catalog Builder

 PRB1882079

</td><td>

For a few variables, the 'Question' type isn't shown in the 'Questions' tab

</td><td>

Configuration sections of new variable types in Catalog Builder.

</td><td>

1.  Log in as catalog\_builder\_developer.
2.  Navigate to Catalog Builder.
3.  Create from scratch.
4.  Enter the item name.
5.  Navigate to the 'Question' section.
6.  Create new question for 'Masked', 'URL', 'Numeric scale', and 'Custom'.
7.  Observe the 'Questions' tab after creation.

 Expected behavior: The 'Question' type should be displayed in 'Question' tab.

 Actual behavior: For lookup multiple choice, 'Question' type is displayed before 'Subtype'.

</td></tr><tr><td>

Service Catalog Builder

 PRB1884912

</td><td>

Client script with a compilation error is also getting saved

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Navigate to Catalog Builder.
3.  Navigate to **Create catalog item flow**.
4.  Add a name.
5.  Navigate to the client script.
6.  Add script as 'mefrt;',gtyb tb,;rgwbn'.
7.  Save the script.

 Expected behavior: The script shouldn't get saved as is in Platform.

 Actual behavior: The script gets saved.

</td></tr><tr><td>

Service Catalog Builder

 PRB1890510

</td><td>

In the Catalog Builder, when the **Use confirmation** option is selected for a masked type variable, the text boxes in the question preview are highlighted in red even before any values are entered

</td><td>

Both fields are highlighted in red before any values are entered or compared in the Question preview.

</td><td>

1.  Navigate to **Catalog Builder**.
2.  Create an item from scratch.
3.  Enter the item name and short description.
4.  Insert a new question with the type 'Text' and 'masked' under 'Questions'.
5.  Select **Use confirmation** in the 'Additional details' tab.
6.  Observe the Question preview on the right hand side.

 Expected behavior: Since no values have been entered initially and both fields are empty, they shouldn't be highlighted in red by default.

 Actual behavior: Even before any values are entered or compared, both fields are highlighted in red as if they contain mismatched input.

</td></tr><tr><td>

Service Catalog Builder

 PRB1891330

</td><td>

In Catalog Builder, when creating a new lookup variable with a **Name** field that already exists, the 'Question preview' automatically displays the values of the existing variable by default

</td><td>

The 'Question preview' displays the values by default even before any tables are selected.

</td><td>

1.  Navigate to **Catalog Builder**.
2.  Create an item from scratch.
3.  Enter the item name and short description.
4.  Insert a new question in the 'Questions' tab with the type 'Choice' list \(values from table\)'.
5.  Enter the **Name** field as the same as above the question in the 'Details'.

 Expected behavior: Since no tables have been selected initially, there should not be any values on the 'Question preview'.

 Actual behavior: Even before any tables have been selected, the 'Question preview' automatically displays the values of the existing variable by default.

</td></tr><tr><td>

Service Catalog Builder

 PRB1891381

</td><td>

When the 'Add script' button is selected twice, the submission gets stuck forever for client script in Catalog Builder

</td><td>

The user is able to select the 'Add script' button again because its not disabled after the first time, resulting in the user getting stuck on the submission message.

</td><td>

1.  Login in to the instance as catalog\_builder\_developer.
2.  Navigate to **Catalog Builder** &gt; **Create new catalog item flow**.
3.  Enter the 'Details' tab into the 'Client script' section.
4.  Enter the client script name and type.
5.  Select **Add script** twice.

 Expected behavior: The client script is created.

 Actual behavior: It is stuck with the submission message forever.

</td></tr><tr><td>

Service Catalog Builder

 PRB1892257

</td><td>

Previous default value isn't cleared from the list while editing the question with new set of default values in Catalog Builder

</td><td>

Previously set default value should be cleared off from the list.

</td><td>

1.  Navigate to **Catalog Builder**.
2.  Create a question with a Numeric scale.
3.  Mention the default values as 1 to 4.
4.  Set default value as 3.
5.  **Save** it.
6.  Edit the same question to change the default value to 5 to 9.
7.  Navigate to the 'Default value' tab
8.  Observe the list values.

</td></tr><tr><td>

Service Catalog Builder

 PRB1916121

</td><td>

Create a new role and provision to create a catalog item without templates

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB1916126

</td><td>

Platform parity for Catalog Builder

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1910324

</td><td>

There's a dump error from the catalog in ynowassist

</td><td>

Notice the error: '...glide SYSTEM FailDMTUtil SEVERE \*\*\* ERROR \*\*\* File GLIDE INF/plugins/com. glideapp.servicecatalog .standard\_ticket/update/ sys\_ui\_list\_std\_ ticket\_action\_input\_ model.xml contains a record that will not correctly trigger collision detection. Expected the record to be in a file named sys\_ui\_list\_std\_ticket\_action\_input\_std\_ticket\_config\_action\_null.xml'.

</td><td>

 

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1911973

</td><td>

Unable to display the 'show more/less' menu for the 'Incident ticket' form

</td><td>

 

</td><td>

1.  Navigate to the standard ticket configuration from the navigation menu.
2.  Open the incident table ticket configuration.
3.  Under 'Info region' tab, mark the **Show description** field as 'Always'.
4.  Mark the **Description** field as 'description/short description'.
5.  Save the changes.
6.  Launch Service Portal.
7.  Search for the 'Create incident' record producer.
8.  Fill in the variables and submit the form.
9.  Observe the ticket details.

 Expected behavior: The incident standard ticket form must show the description along with the 'show more/less' toggle.

 Actual behavior: Despite of the configurations, the 'show more/less' toggle isn't displaying.

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1917271

</td><td>

Data model support for the 'Actions' framework

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1813722

</td><td>

Warning message is displayed in English in 'Fulfillment' under 'Custom task' instead of Spanish

</td><td>

 

</td><td>

1.  Navigate to **Catalog Builder**.
2.  Navigate to **User preferences**.
3.  Select any available language other than English, such as Spanish.
4.  Create a Catalog Item by adding questions or select any existing Catalog Item which has questions added.
5.  Navigate to the **Fulfillment** step.
6.  Select the Flow as **Step based request fulfillment**.
7.  Select the **Add task** list.
8.  Select **Custom approval**.
9.  Select **Add** without providing any data.

 Expected behavior: The warning message should be displayed in Spanish.

 Actual behavior: The warning message is displayed in English.

</td></tr><tr><td>

Service Catalog

 PRB1879960

</td><td>

Creating a masked variable using Catalog Builder isn't showing the **Confirmation** field in the preview

</td><td>

After going into 'Additional details' for 'Use Confirmation', the **Confirmation** field doesn't display in the 'Preview' section.

</td><td>

1.  Pick the latest track Catalog Builder instance.
2.  Create a new catalog item using Catalog Builder.
3.  Create a masked-type question using the 'Questions' section.
4.  Use 'Additional details' to try to use the options such as 'Use Confirmation'.
5.  Observe the 'Preview' section on the right side.

 Expected behavior: The **Confirmation** field should be displayed in the preview.

 Actual behavior: The **Confirmation** is not displayed in the preview.

</td></tr><tr><td>

Service Catalog

 PRB1884919

</td><td>

Invalid Catalog Builder info banner in case text to catalog is not enabled

</td><td>

The banner appears even if sn\_text2catalog isn't active or installed.

</td><td>

1.  Navigate to **Maintain items**.
2.  Select **New**.

 The banner shows 'Created using Now Assist' even if the instance doesn't have sn\_text2catalog active or installed.

</td></tr><tr><td>

Service Catalog

 PRB1888902

</td><td>

While creating a new question for the type 'Display Label', the sub type 'Plain Text' shows as the 'Default value' tab

</td><td>

 

</td><td>

1.  Launch Catalog Builder.
2.  Attempt to create a catalog item from scratch.
3.  Attempt to create a new question of the type 'Display Label'.
4.  Select the subtype as 'Plain text'.
5.  Observe the displayed tabs.

 Expected behavior: As it is a static label of plain text, it shouldn't display the 'Default value' tab.

 Actual behavior: It shows the 'Default value' tab, which is not correct in Platform UI16.

</td></tr><tr><td>

Service Catalog

 PRB1889278

</td><td>

Item links in the 'Categories' page of the Service Operation Workspace \(SOW\) aren't shown in the color blue

</td><td>

Links aren't underlined in the color blue.

</td><td>

1.  Launch SOW.
2.  Open any incident with new state.
3.  Select the **Create Request** UI action.
4.  Observe the launched sc\_categories page.

 Expected behavior: The item links shown for each category should be displayed with blue color underlined.

 Actual behavior: The links are underlined with black color which is not expected.

 Scenario 2:

 1.  Launch SOW.
2.  Open any incident with new state.
3.  Select the **Create Request** UI action.
4.  Observe the launched sc\_categories page.
5.  Search for any catalog item using the search.

 Expected behavior: The search results links should be shown in blue color underlined.

 Actual behavior: It is not shown with blue underlined color.

</td></tr><tr><td>

Service Catalog

 PRB1889281

</td><td>

In Catalog Builder, the lookup source for selectbox variable shows

</td><td>

 

</td><td>

1.  Create a new catalog item using the Catalog Builder.
2.  Create a new question of type 'Choice' and subtype as 'List' fixed values.
3.  Observe the additional detail section.

 Expected behavior: The lookup source shouldn't be there for the selectbox variable.

 Actual behavior: The lookup source is displayed for the selectbox variable, which has no significance for the selectbox variable.

</td></tr><tr><td>

Service Catalog

 PRB1890938

</td><td>

The value in the **Name** field doesn't change based on the value selected in the **Table** field for the record producer in Catalog Builder

</td><td>

The **Name** field is dependent on the value in the **Table** field with **Map to a specific field** on the table is selected.

</td><td>

1.  Log in to Catalog Builder.
2.  Create a Record producer.
3.  Select the question type **Text** and sub-type **Single-line text**.
4.  Check **Map to a specific field on the table**.
5.  Select the value from the **Table** field.
6.  Validate the value on **Name** field.
7.  Repeat the step 5 multiple times.

 Expected behavior: The **Name** field is dependent on the value selected in **Table** field when **Map to a specific field on the table** is checked.

 Actual behavior: When the value selected for the first time, the **Table** field updates the **Name** field, but the values don't change when **Map to a specific field on the table** is checked.

</td></tr><tr><td>

Service Catalog

 PRB1894620

</td><td>

The **lookup\_depends\_on** field isn't updated with the new reference on catalog item for copy/checkout

</td><td>

 

</td><td>

1.  Create a new catalog item.
2.  Add a single line text variable called var1.
3.  Add a variable as the type lookup select box \(for example: var2\).
4.  Select **Choice** as the source type.
5.  Set 'Choices depend on' to 'var1'.
6.  Use the **Copy** UI action for the catalog item.
7.  Observe that the copied item will have its own copy of the 2 variables.

 Expected behavior: The new var2 should have its **Choices depends on** field point to the new var1 copy.

 Actual behavior: It still points to the previous items var1.

</td></tr><tr><td>

Service Catalog

 PRB1904034

</td><td>

Selected link nudges aren't captured in telemetry

</td><td>

 

</td><td>

1.  Deactivate a skill.
2.  Assign the creator role to any user.
3.  Impersonate the user.
4.  Navigate to Catalog Builder.
5.  Select the 'Nudge' link.

 Expected behavior: The link should be logged to the catalog\_builder\_analytics table.

 Actual behavior: None of the link nudges are working.

</td></tr><tr><td>

Service Catalog

 PRB1916120

</td><td>

Client scripts in Catalog Builder

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1916122

</td><td>

The ability for catalog authors to control prefill behavior \(KG, user personalization API, chat history\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1916139

</td><td>

Lookup selectbox and lookup multiple choice to take values from the sys\_choice table as choices

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog Wizard

 PRB1874235

</td><td>

Scripted UI Policies don't run in the Service Catalog Wizard

</td><td>

 

</td><td>

1.  Create a scripted UI policy on the Catalog Item Builder CRP.
2.  Open the Catalog Item wizard.

 Expected behavior: Scripts of the policy must run in wizard.

 Actual behavior: Scripts of the policy don't run in wizard.

</td></tr><tr><td>

Service Catalog Wizard

 PRB1877107

</td><td>

Variable permissions are not honored on the Catalog Wizard framework

</td><td>

Two scenarios occur in this problem where variables aren't being honored. In scenario 1, the value for the **Meta** field is reset. In scenario 2, write permissions aren't honored and the script is executed.

</td><td>

Scenario 1:

 1.  Create a new field on the 'Create a catalog item' producer to map to the **Meta** field on the catalog item table.
2.  Have a default value on the question created previously, for example, 'Testing meta tag'.
3.  Navigate to the 'Permission' tab on the question created.
4.  Add Catalog Developer as the read role.
5.  Impersonate a builder editor.
6.  Attempt to create an item.
7.  Notice that the question was added to the wizard, when it shouldn't have been added.
8.  Navigate to Platform.
9.  Modify the value to 'Modified meta tag value' for the **Meta** field.
10. Edit the item again in Builder.
11. Change a field on the form that is visible.
12. **Submit** it.
13. Notice that the item published.

 Expected behavior: The value for meta should be 'Modified meta tag value'.

 Actual behavior: The value is reset the default value provided on the question. The same should be the behavior on the variables in the producer set of type one to one. Permissions are not supported if a variable is in the MRVS producer set. The behavior should remain same for MRVS producer set.

 Scenario 2:

 1.  Create a custom variable with a save script and post insert script.
2.  Navigate to the 'Permissions' tab.
3.  Add 'Catalog developer' as the read role.
4.  Add the variable to the wizard.
5.  Notice that the scripts run irrespective of the permissions when they shouldn't be executed if the read permission is not met on the variable.
6.  Give the 'Create' role.
7.  Notice that the script gets executed irrespective, when the script shouldn't be executed if the main record is inserted because the mode should consider insert and honor the 'Create' permissions.
8.  Give the 'Write' role.

 Expected behavior: The mode should be considered if the main record is updated, and should honor write permissions. The script shouldn't be executed.

 Actual behavior: The script gets executed.

</td></tr><tr><td>

Service Model Foundation - Business Location

 PRB1896747

</td><td>

Addition of Query ACLs in Service Model Foundation - Business Location

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1795842

</td><td>

'Created Source' is not always stamped on software models by content update jobs

</td><td>

This issue usually occurs because the scheduled jobs below don't stamp the **Created source** field if it's empty on the suite parent: SAM - Apply latest content changes and SAM - Create lifecycles and suites for a software model.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1807639

</td><td>

Some Software Asset Management \(SAM\) properties can be edited by a SAM admin

</td><td>

Some SAM sys properties exist in different folders and have different write roles.

</td><td>

1.  Install the plugin 'com.sn\_samp\_ master\_ws'.
2.  Navigate to **sys\_properties \_category\_m2m**.
3.  Filter by the Software Asset Management.
4.  Open 'com.snc.samp. recon.subgroup'
5.  Check that 'write\_roles = admin' and 'write\_roles = sam\_admin'.
6.  Install the plugin 'com.glide.domain.msp \_extensions.installer'.
7.  Check that 'write\_roles = admin'.

</td></tr><tr><td>

Software Asset Management

 PRB1857027

 [KB2214434](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2214434)

</td><td>

Performance enhancement for the 'Bookkeeping for dedup on delete' business rule

</td><td>

The number of records to update may be reduced if there's an additionally query on primary\_install is not null and deduplicated=true.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1916117

</td><td>

Create a reclamation rule on the License Workbench 'Product results' page

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Lifecycles \(Family Channel\)

 PRB1910582

</td><td>

There's a duplicate sys\_choice for current\_lifecycle\_phase in sam\_sw\_product\_ lifecycle\_report

</td><td>

The duplicate might be coming from the older field as they don't exist in that older field anymore.

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB1899152

</td><td>

Change the labels for the sys\_sc\_alerts table

</td><td>

UX has suggested to change labels for some of the columns in the sys\_sc\_alerts table: 1. Target ID: Affected Entity, 2. Alert Level: Severity, and 3. Type: Alert Type.

</td><td>

 

</td></tr><tr><td>

System Notifications

 PRB1838563

</td><td>

The base instance bell notification hover does not work intermittently

</td><td>

Full details are not showing whenever the pointer hovers on top of the bell notification to see the full details.

</td><td>

1.  Log in to an instance.
2.  Navigate to the bell icon of notification.
3.  Hover on the notification.

 Observe that the full details are not showing.

</td></tr><tr><td>

System Update Sets

 PRB1885422

</td><td>

Importing an update set of an upgrade plan or items also installs the applications on the instance

</td><td>

 

</td><td>

1.  Log in to a subprod instance.
2.  Navigate to **Admin Menu** &gt; **Upgrade Management**.
3.  Start the upgrade on the sub-prod instance after completing the export for update set.
4.  Import update set on prod.

 Observe that the upgrade plan/items are installing applications on the prod instance while importing it.

</td></tr><tr><td>

System Update Sets

 PRB1909130

 [KB2250914](https://hi.service-now.com/kb_view.do?sysparm_article=KB2250914)

</td><td>

An installation from an update set overwrites customized records

</td><td>

To remediate the update set, the commit should be backed out \(including a rollback of the app install\) and a different way of installing the application should be used.

</td><td>

Refer to the listed KB article for details.

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

</td></tr><tr><td>

Territory Planning

 PRB1837020

</td><td>

In Dispatcher Workspace, there's an issue with a search territory agent

</td><td>

If the agent belongs to multiple groups, and the last group returned from the glideRecord query doesn't belong to the territory, and triggers the issue.

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
2.  Make it fail on offload with a 60 minute retry period.
3.  Archive other records that would get offloaded by the same rule.

 Notice that the records never get offloaded.

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1890721

</td><td>

Tier 2 offload runs should be visible in the 'Archive rules' page

</td><td>

Users have no visibility of whether the offload is running or not. Progress should be viewed in the 'Archive rules' page.

</td><td>

1.  Configure Tier 2 offload rule.
2.  Offload some records.

 Expected behavior: On the Archive Rule form next to Archive Run, there is a tab where the users can review offload runs.

 Actual behavior: Information is not available on the Archive Run form.

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1897660

</td><td>

Change the sys\_property glide. db.archive.offload. free\_storage\_max\_gb value from 100GB default to 36T

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1871282

</td><td>

There's an IndexOutOfBounds and StringIndexOutOfBoundsException exception in transaction prioritization

</td><td>

This issue can occur under heavy load testing. This has been identified as the cause for a memory leak where HTTPTransaction objects are held onto after this exception causes the request to fail.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB1879023

</td><td>

A workspace modal with an **HTML** field doesn't render in Yokohama

</td><td>

When using g\_modal.showFields\(\) in a UI action to populate the modal from the workspace, the modal doesn't appear if it has an **HTML** type field defined.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1791024

</td><td>

The getSelectedOption breaks for records with some script type fields

</td><td>

.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1821427

</td><td>

An instance runs out of memory when there's unexpected wiki markup table syntax inside of a **Wiki** text field

</td><td>

When creating a kb\_knowledge record on a form with the **Wiki** field showing, the node runs out of memory.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1887884

</td><td>

A **Dependent** field onChange handlers fires when the **Depends on** field changes when there's no change to the **Dependent** field

</td><td>

There are client scripts on various task-based tables that clear the assigned\_to when assignment\_group changes. These tables can't be tested on \(for example: change\_request, incident, problem, problem\_task\) as it will appear that the **Dependent** field onChange handlers fire when the **Depends on** field changes. A table that doesn't have existing client scripts on the **assignment\_group** field like change task \(change\_task\) must be used.

</td><td>

1.  Create a new client script with the following:
    1.  Table: Incident
    2.  UI Type: All
    3.  Type: onChange
    4.  Field name: **Assigned to**
    5.  Script:function onChange\(control, oldValue, newValue, isLoading, isTemplate\) \{
2.  Start a new Change Task \(change\_task\) record in UI16.
3.  Set an Assignment Group.

 Notice that the info message isn't displayed because onChange handlers for the **Dependent** field **\(assigned\_to\)** are not fired.

</td></tr><tr><td>

UI Form Administration

 PRB1893949

</td><td>

A **Mandatory** field hint sometimes is missing the 'Mandatory' prefix

</td><td>

The help text \(hint\) is missing the prefix of 'Mandatory' for certain fields even when the field is mandatory.

</td><td>

1.  Log in to any Yokohama instance.
2.  Navigate to the incident record and make the **Sub-category** field mandatory on dictionary.
3.  Enable help tips in preferences/settings.
4.  Add a hint for a **Sub-category** field.
5.  Hover the '?' next to the field.

 See that the prefix 'Mandatory' is missing.

</td></tr><tr><td>

Upgrade Center

 PRB1891562

</td><td>

A user is unable to determine the purpose of a link when it has the context 'Here'

</td><td>

 

</td><td>

1.  Start JAWS.
2.  Navigate to the 'Home' screen.
3.  Navigate to the **Dashboard page** &gt; **Instance upgrade panel** &gt; **Visit Upgrade Center link**.
4.  The respective page opens in a new tab.

 Note that the screen reader announces 'here' as the link and not what the link is for.

</td></tr><tr><td>

Upgrade Center

 PRB1895609

</td><td>

Glide upgrade failed due to node getting restarted

</td><td>

This is an edge case where a certain combination of plugins trigger this behavior.

</td><td>

1.  Reset to baseline builds for Yokohama for Loadsim.
2.  Trigger an upgrade.

</td></tr><tr><td>

Usage Analytics

 PRB1898047

 [KB2306210](https://hi.service-now.com/kb_view.do?sysparm_article=KB2306210)

</td><td>

On Yokohama, User Analytics data isn't refreshing post-clone, copy, or restore

</td><td>

Cloned/Restored/Copied instances start tracking usage data and are able to see the data on the UXA Dashboard.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Usage Analytics

 PRB1904448

</td><td>

Some users don't want internal ServiceNow instances such as support, impact, or nowlearning to track their users

</td><td>

ServiceNow instances should be able to turn off the tracking of Usage Analytics data with their custom script and system property.

</td><td>

1.  Navigate to any instance.
2.  Confirm that the 'Disabled' policy is configured in Policy Script Provider.

 Actual behavior: Observe that the metric calls are still going with Essential Tracking Level.

 Expected behavior: There should be no metric calls.

</td></tr><tr><td>

Usage Analytics

 PRB1905285

</td><td>

An empty or invalid hashUserId column in the sys\_user table breaks metric call validation and user event enrichment, leading to inaccurate UXA dashboard metrics

</td><td>

Users with incorrect usage data displayed on the UI due to user table settings now have usage data being collected properly and reflected on the UXA dashboard.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1889441

</td><td>

Pagination is broken in Multi-Data source broker

</td><td>

Cursors are stored in the format of the map, which is converted to the byte stream and base64 encoded. While decoding, the cursor is expected to be JSON, and throws an exception.

</td><td>

1.  Create a state to store the cursor and page number.
2.  Create a page with multi-table data with two data sources.
3.  Bind the state variables to it.
4.  Add a button to fetch more data, which will update the state variable with the cursor from the response.

 Notice that the response doesn't have updated results.

</td></tr><tr><td>

UX Framework

 PRB1889452

</td><td>

The name/sys\_id of the data source is not returned in the response of multi-table data

</td><td>

The response of the data broker only returns the table.

</td><td>

1.  Create a page with Multi-table data broker.
2.  Add two data sources with different names and queries.

 Notice that the response of the data broker only returns the table, but, not the name/sys\_id of the data source.

</td></tr><tr><td>

UX Framework

 PRB1890019

</td><td>

Using Zing search results in wrong pagination with Multi-Source data broker

</td><td>

 

</td><td>

1.  Create a page with a multi-source data broker.
2.  Add a data source with filter condition as 'Keywords' 'are'.
3.  Pick the value such that the result count is less than a page size.
4.  Execute the databroker.

 Notice that is\_last\_page value is true, when it should've been false.

</td></tr><tr><td>

UX Framework

 PRB1901587

</td><td>

Intent Library changes cause a SEND\_INTENT\_FEEDBACK error due to no meta.generatorForFeedback

</td><td>

The NAP window eventually displays a message that reads: 'An error occurred while saving your app. Please check with your admin.' The following error can be observed in the browser console: 'IntentTranslatorBehavior: LIBRARY-INTENT-CHANNEL\#SEND\_INTENT\_FEEDBACK action is missing generatorForFeedback from meta'.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1904903

</td><td>

Results of different data sources have the same source ID

</td><td>

The datasource ID is set as static, hence all the results share the data source of the last result.

</td><td>

1.  Configure the multi-table data broker to take different data sources with different sys\_ids.
2.  Notice that the results belonging to the different data source have the same sys\_id.

</td></tr><tr><td>

UX Framework

 PRB1916142

</td><td>

Intent library updates for Gen AI Canvas

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1826252

</td><td>

User inbound messages to a Live agent end up in the picker pagination logic in specific scenarios for channels

</td><td>

The user inbound message to a Live agent somehow ends up in the picker pagination logic in CAF if the last rich control before invoking the live agent was a paginated picker.

</td><td>

1.  Create a custom topic for invoking a Live agent.
2.  Add a paginated picker nod before invoking the Live agent. For example, choose a preferred language picker with 15 options.
3.  Make this the default topic for Live agent.

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

 PRB1892416

</td><td>

Incorrect column usage when updating the One API Service Plan Invocation record

</td><td>

A warning occurs in the logs.

</td><td>

1.  Execute any simple Now Assist Virtual Agent use case \(for example: small talk, what is spam\).
2.  Notice the warning in the logs: '2025-05-13 08:59:06 \(140\) glide.cs.worker.93 SYSTEM txid=c1dfd72c876d SSI\_ef76d022b7cf9a109d63827b5e11a913 WARNING \*\*\* WARNING \*\*\* getGlideElement called for unknown field 'startedAt' in table 'one\_api\_service\_plan\_feature\_invocation' 2025-05-13 08:59:06 \(140\) glide.cs.worker.93 SYSTEM txid=c1dfd72c876d SSI\_ef76d022b7cf9a109d63827b5e11a913 WARNING \*\*\* WARNING \*\*\* setValue called for unknown field 'startedAt' in table 'one\_api\_service\_plan\_feature\_invocation''.

</td></tr><tr><td>

Virtual Agent

 PRB1892510

</td><td>

Support 'Sync' mode for Java execution path

</td><td>

Currently, the Java execution path for OE system executor capabilities are limited to just the async mode. This is limiting the ability to execute troubleshooting tools via background scripts. The 'Sync' mode execution should be fully supported for the Java path as well.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1894471

</td><td>

Virtual Agent push notifications aren't coming through on mobile

</td><td>

Noticed on Android.

</td><td>

1.  Set up a user with a push token and mobile client with NASS chat.
2.  Start a chat.
3.  Send a sequence of messages synchronously.
4.  Close the mobile client when they are sending.
5.  Wait.

 Expected behavior: Users should see a push notification.

 Actual behavior: There's no push notification in NASS.

</td></tr><tr><td>

Virtual Agent

 PRB1894545

</td><td>

LLM responses are not unmasked if streaming is enabled with java proxy enabled

</td><td>

 

</td><td>

1.  Enable NowAssist assistant with streaming.
2.  Use GPT4-0.
3.  Enable masking for email address and/or phone number types for the phrase 'what is my contact information'.

 Expected behavior: The unmasked email/phone numbers are displayed.

 Actual behavior: The email/phone numbers are displayed with masks.

</td></tr><tr><td>

Virtual Agent

 PRB1895195

</td><td>

When the user enters an invalid/partial utterance, an error appears and the conversation is closed

</td><td>

Dynamic capability executor can trigger multiple capabilities with different payloads. However, dynamic capability executor fails when duplicate capability IDs are passed.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1896593

</td><td>

Shouldn't be relying on the 'Greetings' topic for portal's Virtual Agent hand off

</td><td>

Users can have custom 'Greetings' topics. For those users, the hand off is broken.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1898661

</td><td>

Non-LLM time has increased from 2544 to 3065 milliseconds \(ms\), leading to 500-900 ms in some NAVA use cases

</td><td>

In NAVA use cases, users observed 500–900 ms degradation from 2544 to 3065 ms in non-LLM async time. For a synthesized response, the non-LLM has degraded and it's spending additional 1.2 secs on that. Hence, the overall gain on the response stands at 5.3 seconds \(6.5-1.2\).

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1903011

</td><td>

The error 'Cannot invoke 'org.apache.commons.httpclient.StatusLine.getStatusCode\(\)' because 'this.statusLine' is null' for LTM capabilities

</td><td>

The error is observed in the Gen AI logs for the conversation.

</td><td>

1.  Switch to any model.
2.  Try any utterances.

 Observe that in the Gen AI logs for that conversation, there's an error, 'Error: Cannot invoke 'org.apache.commons.httpclient.StatusLine.getStatusCode\(\)' because 'this.statusLine' is null Error Code: 200000'.

</td></tr><tr><td>

Virtual Agent

 PRB1905944

</td><td>

enableDynamicTranslation and enableNativeTranslation should be passed as boolean values

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1908511

</td><td>

Now Assist panel \(NAP\) assistants should read agentic mode from now\_assist\_ va\_search\_results \_output\_type

</td><td>

NAP assistants \(both legacy client and new dynamic window\) should read agentic mode from the Now Assist panel record on now\_assist\_ va\_search\_results \_output\_type. The new dynamic window UI for NAP has been reading from the mweb record instead.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1912380

</td><td>

Don't log agent skill execution licensing

</td><td>

It shouldn't create a licensing record when an agent skill is executed. The AIA framework does its own calculation/logging for agent execution based on the execution tasks created at runtime.

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

 PRB1913835

</td><td>

Canvas isn't displaying the Show/Hide options when executing a skill

</td><td>

While Web Agent is executing the goal, the live 'Screenshot' view isn't loaded. After the execution, it's displaying the Show/Hide view, which is displaying all the screenshots.

</td><td>

1.  Create an Agent WF.
2.  Promote it.
3.  Navigate to Now Assist Portal.
4.  Switch to the 'Maximize' view.
5.  Select the skill and start it.
6.  Verify the live 'Screenshot' view isn't loaded.

</td></tr><tr><td>

Virtual Agent

 PRB1913892

</td><td>

Validation should be added for security attribute ID in global.GenAiSkillSecurityUtils\(\).insertSkillAclBySkillid\(...\) and global.GenAiSkillSecurityUtils\(\).updateSkillAclByAclId\(...\)

</td><td>

While calling global.GenAiSkillSecurityUtils\(\).insertSkillAclBySkillid\(...\) and global.GenAiSkillSecurityUtils\(\).updateSkillAclByAclId\(...\) with invalid sys id of security attribute, the security attribute is created with an empty condition. Since it is expected to used with Background script, the user should be informed of the invalid value used for the security attribute.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1915460

</td><td>

gen\_ai\_agent and gen\_ai\_workflow advance is turned off in the ACL form16 UI

</td><td>

 

</td><td>

1.  Navigate to sys\_security\_acl.do.
2.  Select the type as gen\_ai\_agent or gen\_ai\_workflow.

 Observe that there's no option called 'advanced'.

</td></tr><tr><td>

Virtual Agent

 PRB1915751

</td><td>

Midtopic switch isn't switching to a new topic and runs into an error on the continuing existing topic

</td><td>

 

</td><td>

1.  Navigate to Dynamic Window.
2.  Type 'i want to order food'.
3.  Answer one of the prompts.
4.  Type 'i want to order coffee actually'.

 Expected behavior: The user should be given an option to switch to the 'Order coffee' topic and have an option to continue the request.

 Actual behavior: The user gets the order food topic started again and choosing 'continue' runs into an error as well.

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

1.  Set up a new instance.
2.  Enable the search for Virtual Agent \(VA\).
3.  Make /esc available for VA.
4.  As Abel Tuter, navigate to /esc.
5.  Select **globe**.
6.  Type 'who is bill clinton'.

 Observe a 'sorry' message.

</td></tr><tr><td>

Virtual Agent

 PRB1917121

</td><td>

Update the ACL name for OE skills to align with changes from the OE team

</td><td>

Update the ACL name format to use the '&lt;sys\_name.skillConfigId' format instead of the 'skillConfigId:&lt;sys\_name' format \(where skillConfigId is the sys\_id of the record, and sys\_name is the name of the record in sn\_nowassist\_skill\_config\). This is only applicable when the 'internal\_name' column in the sn\_nowassist\_skill \_config table is empty.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1917378

</td><td>

Agentic eval metric score standardization

</td><td>

It should incorporate the changes in NASK to display the label in the list view and the drill down view.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1918363

</td><td>

Canvas isn't working

</td><td>

The 'Show' button doesn't appear at end of the execution.

</td><td>

1.  Set up Canvas
2.  Go to Now Assist Panel on the instance.
3.  Select **Canvas Flow**.
4.  Enter **Yes** to answer the question that it's ready to execute Canvas.

 Expect behavior: At end of the execution, users will see the **Show** button.

 Actual behavior: Nothing appears.

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

 PRB1921142

</td><td>

Pass agentic data to the conversational pipeline

</td><td>

This is a product enhancement.

</td><td>

 

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
    3.  I18N: Japanese Translations \(com.snc.i18n.japanese\)
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

 PRB1897932

</td><td>

NAVA isn't picking interaction context variables when enhanced chat is turned on

</td><td>

Account and contact fields aren't populated on an interaction record. Note that the issue isn't reproducible when enhanced chat is turned off in Virutal Agent.

</td><td>

 

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
5.  Enter a small script to simulate clicks multiple times.
6.  Observe all 15 messages are sent in the chat client.

 Expected behavior: Chat client shouldn't allow multiple inbound messages.

 Actual behavior: Chat client allows multiple inbound messages.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1904063

</td><td>

Typing too fast in an NLU-based text choice picker for a lot of rows prevents upgrades

</td><td>

 

</td><td>

1.  Create a topic with a Dynamic choice picker in NLU.
2.  Ensure that the selected records have a lot of rows \(10K+\).
3.  Type fast in the text choice picker.

 Expected behavior: It should update the filtered items in the list.

 Actual behavior: The results never update due to 423 errors in the backend responses.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1910411

</td><td>

A user receives notifications when a notification toggle in the settings is turned off

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1920026

</td><td>

Proactive trigger topics don't launch

</td><td>

 

</td><td>

1.  Set up proactive triggers on the instance so there are topics that launch when selected.
2.  Navigate to the portal where proactive trigger is configured.
3.  Launch the associated topic when proactive trigger is received.

 Expected behavior: The topic should launch in Dispatcher Workspace.

 Actual behavior: The topic doesn't launch, and the user just sees the welcome message.

</td></tr><tr><td>

Visual Task Boards

 PRB1852813

</td><td>

If the modal window is closed by selecting outside of the modal, VTB cards aren't refreshed automatically when updated

</td><td>

This only occurs if the modal window is closed by selecting outside of the modal. If the modal window is closed by selecting the 'X' in the top right, the record's card updates automatically as expected.

</td><td>

1.  Create a visual task board by navigating to **Self-Service** &gt; **Visual Task Boards** &gt; **New** &gt; **Data Driven Board**.
2.  Set **Task Table** to 'incident' and the **Vertical Lane** field to 'Incident State'.
3.  Select **Next**.
4.  For the conditions, set **Assigned to is \[current user\]** and select **Create**.
5.  Select a card on the VTB to open the modal window.
6.  Unassign the record from \[current user\] in the modal window.
7.  Close the modal window by selecting outside of the modal.
8.  Observe that the card remains on the VTB even though it no longer meets the conditions for the board.
9.  Refresh the VTB page.

 Observe the card is no longer on the board.

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

 PRB1818332

</td><td>

The tool tip for catalog items is not announced by the screen reader for accessibility

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Window Manager

 PRB1920314

</td><td>

Upgrade to Yokohama Patch 6 is broken with the Windows Manager \(WM\) plugin

</td><td>

Adding the Windows Manager plugin to the glide-core-ui-components plugin in a patch creates a new version that uses the next commit SHA. The commit SHA is lower, and in the upgrade process, the lower version is skipped even though it is the 'new' version with the WM plugin added.

</td><td>

1.  Open a Yokohama instance.
2.  Upgrade the instance to Yokohama Patch 6.
3.  Notice that AIEX/WM is broken.
4.  Navigate to **v\_plugin.list**.
5.  Search for 'window-manager' in the name column.

 Notice that Window Manager is not activated whereas it should be.

</td></tr><tr><td>

Work Order Management

 PRB1902998

</td><td>

When re-assigning an Agent Work Schedule record from one agent to another in a collapsed group, agent blocks aren't properly reflected

</td><td>

The white markp shows an inaccurate work schedule for the agent with the updated schedule.

</td><td>

1.  Assign a Work Schedule to an agent in a collapsed group.
2.  Reassign the same Work Schedule to another agent in the collapsed group.
3.  Refresh the calendar panel.

 Expected behavior: White markp should be displayed for the updated user, and the previous user that was assigned the Work Schedule should go back to gray.

 Actual behavior: White markp now appears for the previous agent that was assigned a work schedule as well as the updated agent, and two markps are present.

</td></tr><tr><td>

Zero Trust Access

 PRB1830413

</td><td>

Zero Trust Access \(ZTA\) policy-based authentication is applied for Impersonation

</td><td>

 

</td><td>

1.  Install a ZTA policy-based plugin.
2.  Create a configuration with a condition as if role is ITIL.
3.  Remove the ITIL role.2. Log in as a user with elevated privileges.
4.  Attempt to impersonate the ITIL user.

 Expected behavior: ZTA shouldn't apply for the impersonated user.

 Actual behavior: ZTA policies are applied, and the ITIL role is relegated from impersonation.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 5 Hotfix 2](yokohama-patch-5-hf-2-PO.md)
-   [Yokohama Patch 5 Hotfix 1](yokohama-patch-5-hf-1-PO.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4 Hotfix 1](yokohama-patch-4-hf-1-PO.md)
-   [Yokohama Patch 4a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2309845)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


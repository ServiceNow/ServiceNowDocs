---
title: Xanadu Patch 11
description: The Xanadu Patch 11 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-12-11"
reading_time_minutes: 9
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 11

The Xanadu Patch 11 release contains important problem fixes.

-   **Xanadu Patch 11 was released on December 11, 2025.**
    -   Build date: 12-07-2025\_2348
    -   Build tag: glide-xanadu-07-02-2024\_\_patch11-11-27-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X011.00.xlsx).

## Overview

Xanadu Patch 11 includes 99 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp11.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 11 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 11, refer to [KB2646306](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2646306).

## Changes in Xanadu Patch 11

-   **[Sensitive data filters](https://www.servicenow.com/docs/access?context=sensitive-data-filters&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US)**

    The Discovery Sensitive Data Filters \[discovery\_sensitive\_data\_filter\] table provides a way to help prevent sensitive information from being exposed in the Configuration Management Database \(CMDB\) by applying redaction rules during data collection.


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

Discovery

 PRB1927941

 [KB2434137](https://hi.service-now.com/kb_view.do?sysparm_article=KB2434137)

</td><td>

Discovery patterns failed prematurely, causing Discovery failure

</td><td>

An example is during 'Windows OS - Server' pattern Discovery, running the Cluster pattern library throws consecutive errors, which should be expected, but the pattern engine failed the pattern instead.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1938123

</td><td>

Flows using base instance actions related to the plugin 'Customer Service Spoke' fail after upgrading to Yokohama

</td><td>

The flows in question are base instance actions related to 'Customer Service Spoke': Add Work Note to Task and Add Comment To Task.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1839297

 [KB1925168](https://hi.service-now.com/kb_view.do?sysparm_article=KB1925168)

</td><td>

A SPEntry page error 'Execute operation on script include 'SPEntryPage'' from scope occurs

</td><td>

Switching the scope and refreshing the page gives the error, 'Execute operation on script include 'SPEntryPage' from scope 'Knowledge Management - Service Portal' was denied'.

</td><td>

1.  Log in to a Xanadu instance.
2.  Create the glide.entry. first.page .script system property.
3.  Give it the value: new SPEntryPage\(\). getFirst PageURL\(\).
4.  Make 'Knowledge Management - Service Portal' as the current scope.
5.  Refresh the browser page.
6.  Notice the error, 'Execute operation on script include 'SPEntryPage' from scope 'Knowledge Management - Service Portal' was denied. The application 'Knowledge Management - Service Portal' must declare a cross scope access privilege. Please contact the application author to update their privilege requests.'
7.  Repeat step 2 and step 3 with the scopes 'CI Landing Experience' and 'Conversational Interfaces - Diagnostics'.

 Notice that the same error message occurs.

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

Analytics Export API

 PRB1853207

</td><td>

Export traffic should be migrated to K8s by default for commercial environments

</td><td>

When a user without elevated privileges logs in to ServiceNow and exports a dashboard or visualization, the traffic goes to VMs because 'glide.par.export.use.sk8s' is false. Instead, K8s traffic should be enabled by default for commercial environments.

</td><td>

 

</td></tr><tr><td>

Audit History

 PRB1938364

 [KB2531096](https://hi.service-now.com/kb_view.do?sysparm_article=KB2531096)

</td><td>

Large amount of history \(audit\) data can lead to node memory contention on node when loading a form

</td><td>

When loading a form for the first time, the node will run out of memory and crash if the history set has to be built to load the Activity Stream and if there's a lot of data to be loaded.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1923704

</td><td>

Due to an ordering change on Raptor post migration, certificate authentications for API calls may fail and cause '500' errors

</td><td>

When mutual authentication is configured using both protocol profile and system properties, the system property takes precedence. This causes the SSL exchange to utilize the socket factory for client certificate provisioning, bypassing the keystore defined in the protocol profile. Additionally, when mutual authentication is enabled via property configuration, all certificates from the sys\_certificate table are loaded. This can lead to intermittent outbound call failures if expired certificates are cached and used for mutual authentication, resulting in HTTP 500 responses.

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

Discovery

 PRB1833795

 [KB1825538](https://hi.service-now.com/kb_view.do?sysparm_article=KB1825538)

</td><td>

The credential alias doesn't work for applicative credentials

</td><td>

.

</td><td>

Refer to the listed KB article for details.

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

Incident Management

 PRB1941995

</td><td>

Problem coordinators can't associate closed incidents to problems in Service Operations Workspace \(SOW\) \(incident end\)

</td><td>

Problem coordinators can't associate closed incidents to problems in SOW due to a change in the script include 'related\_list\_edit\_helper' from using GlideRecord to GlideRecordSecure. The MRA in the workspace lists closed incidents for linking, but then ACLs block the writing of the record. This is not the case in UI16, as it uses a different script include.

</td><td>

1.  Impersonate 'Problem Coordinator A'.
2.  Open a problem in UI16 and the incident list in another tab.
3.  In the incident list, find a closed incident that was last updated by 'system' and open it.
4.  Check the 'Related Records' section of the incident form.

See that the **Problem** field is read-only.

5.  Return to tab with a problem open.
6.  In the 'Incidents' related list of the problem record, select **Add**.
7.  Find and add the previous incident.
8.  Navigate back to the tab with the incident open.

Notice that the **Problem** field has updated.

9.  Continue impersonating and try to link a closed incident in the SOW.

</td></tr><tr><td>

Integration Hub

 PRB1943215

 [KB2605052](https://hi.service-now.com/kb_view.do?sysparm_article=KB2605052)

</td><td>

ua\_ih\_usage tracking displays 'unlicensed' when used with new Workflow Data Fabric \(WDF\) SKUs in Xanadu

</td><td>

WDF bundle entitlement results in 'unlicensed' usages in Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Language and Translations

 PRB1910767

</td><td>

The question\_choice field is displaying 'um' instead of 'A' for Brazilian Portuguese language

</td><td>

This issue was observed when upgrading to Xanadu.

</td><td>

1.  Navigate to a base Xanadu or Yokohama instance.
2.  Install the I18N Brazilian Portuguese Translations plugin.
3.  Navigate to **sys\_translated.LIST**.
4.  Filter the table as 'question\_choice' is value 'a'.

 Observe in Brazilian Portuguese language Label \(translate\) is displaying as 'um'.

</td></tr><tr><td>

Lifecycle Events

 PRB1913012

</td><td>

Creating a case of any journey config doesn't show the Journey number field in the case details

</td><td>

The issue occurs due to changes that modify the form when GenAI is installed. Rather than adding the fields in an if folder, the fields should just be added to the normal form layout in the update folder; if the fields do not exist, they will not show up on the form.

</td><td>

 

</td></tr><tr><td>

Problem Management

 PRB1930428

</td><td>

Problem coordinators can't associate closed incidents to problems in Service Operations Workspace \(SOW\)

</td><td>

Problem coordinators can't associate closed incidents to problems in SOW due to a change in the script include 'related\_list\_edit\_helper' from using GlideRecord to GlideRecordSecure. The MRA in the workspace lists closed incidents for linking, but then ACLs block the writing of the record. This is not the case in UI16, as it uses a different script include.

</td><td>

1.  Impersonate 'Problem Coordinator A'.
2.  Open a problem in UI16 and the incident list in another tab.
3.  In the incident list, find a closed incident that was last updated by 'system' and open it.
4.  Check the 'Related Records' section of the incident form.

See that the **Problem** field is read-only.

5.  Return to tab with a problem open.
6.  In the 'Incidents' related list of the problem record, select **Add**.
7.  Find and add the previous incident.
8.  Navigate back to the tab with the incident open.

Notice that the **Problem** field has updated.

9.  Continue impersonating and try to link a closed incident in the SOW.

</td></tr><tr><td>

Procurement

 PRB1962139

 [KB2625821](https://hi.service-now.com/kb_view.do?sysparm_article=KB2625821)

</td><td>

Enable stockroom receiving for assets which are part of PO

</td><td>

The script include POReceiveManager is essential for receiving Purchase Orders \(PO\), but in pre-Zurich releases, it's restricted to global scope. Due to this limitation, assets associated with a PO cannot be received using the Stockroom Receiving feature. When attempting to receive assets, the following error is displayed: 'Unable to receive the asset. Use the Procurement module or update to the Zurich release or later to continue.'

</td><td>

1.  On a Xanadu or Yokohama instance, provision an instance with the following applications installed:
    1.  Hardware Asset Management 13.0
    2.  Asset Management Common 13.0
2.  Create a PO for a hardware model.
3.  Import the assets using ASN.
4.  Attempt to receive the assets using one of the following UI actions on the stockroom form:
    1.  Receive assets
    2.  Import assets

 Expected behavior: Assets are received successfully.

 Actual behavior: The error message appears, and the asset cannot be received.

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

Virtual Agent

 PRB1890944

 [KB2338484](https://hi.service-now.com/kb_view.do?sysparm_article=KB2338484)

</td><td>

Large /api/now/v1/cs/ consumerAccount /unreadMessage calls from Proactive Trigger exhausts instance API resources

</td><td>

Some users on Portal have over 1 million of /api/now/v1/cs/ consumerAccount /unreadMessage call observers in the node logs. This causes an issue as it exhausts the API rate limit and prevents people from submitting forms on the portal and other issues. The API call is constantly sent out even when the session is timed out.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Visual Task Boards

 PRB1955767

</td><td>

vtb\_card and vtb\_task ACLs cause performance issues if either table is used in a related list

</td><td>

A user created a related list on an incident form that queries vtb\_task table. After an upgrade, they started seeing performance issues when viewing incident records and automated database alerts were generated.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 10 Hotfix 1b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2604578)
-   [Xanadu Patch 10 Hotfix 1a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2566299)
-   [Xanadu Patch 10 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2524764)
-   [Xanadu Patch 10](xanadu-patch-10.md)
-   [Xanadu Patch 9b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2422684)
-   [Xanadu Patch 9](xanadu-patch-9.md)
-   [Xanadu Patch 8 Hotfix 4](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2587736)
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


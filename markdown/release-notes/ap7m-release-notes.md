---
title: Australia Patch 7m
description: The  Australia Patch 7m release contains important problem fixes via Australia Patch 7 and updates to compatible ServiceNow Store applications.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/ap7m-release-notes.html
release: australia
topic_type: reference
last_updated: "2026-10-23"
reading_time_minutes: 296
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 7m

The  Australia Patch 7m release contains important problem fixes via Australia Patch 7 and updates to compatible ServiceNow Store applications.

-   **Australia Patch 7m was released on October 23, 2026.**
    -   Build date: 10-21-2026\_1418
    -   Build tag: glide-australia-02-11-2026\_\_patch7m-10-08-2026

## Monthly "m" releases

Monthly "m" releases are now available for your ServiceNow AI Platform® instances. These releases, which are identified by an "m" in the release name, contain everything from the base family patches, the latest version of all AI applications, and those apps' supporting non-AI application dependencies.

**Important:** This ServiceNow® release is not available for ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in the Australia Patch 7 release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A07.00.xlsx).

## Overview

Australia Patch 7 includes 559 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-ap7.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Australia Patch 7 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 7, refer to [KB3152248](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228101).

## Changes in Australia Patch 7

-   **[Monitoring Now Assist usage in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-now-assist-usage.md)**

    , including Moveworks Assists,

    View Moveworks assists broken down by skill. Moveworks skill names are distinguished by the "MW" prefix.


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

Flow Engine

 PRB1989760

</td><td>

Execution details don't load during negative testing

</td><td>

The following error appears: 'There was an error loading the execution details for this flow context. Exception while executing request: Could not deserialize value from sys\_flow\_value with sys\_id 7fb6dcdbd9363a10919050c11e4ef686'.​

</td><td>

1.  Open an instance.
2.  Open the FD.
3.  Select the **Google Drive** application.
4.  Select **Look up file**.
5.  Provide a random file ID.
6.  Select the **Test** button.

 Observe that FD execution doesn't load. The following error appears: 'There was an error loading the execution details for this flow context. Exception while executing request: Could not deserialize value from sys\_flow\_value with sys\_id 7fb6dcdbd9363a10919050c11e4ef686'.​

</td></tr><tr><td>

List Administration

 PRB2031478

 [KB3074807](https://hi.service-now.com/kb_view.do?sysparm_article=KB3074807)

</td><td>

The 'List edit' pop-up is not working in UI16 view with the Next Experience disabled view

</td><td>

The user is not able to edit values from the List view, and the 'List edit' pop-up is partially or not visible at all. The 'List edit' pop-up should be visible for every row and for every column.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB2040686

</td><td>

Linux MID Server pre-checks don't check that the service user would be able to run start.sh, before committing to an upgrade that would leave the MID Server Down

</td><td>

Linux MID Servers can end up stopped during the upgrade process if start.sh is prevented from starting the service again with 'Interactive authentication required' or 'Access denied' errors. This would also cause a Restart MID command from the instance, either from the MID Server's form, or when a plugin activation/upgrade triggers a restart, to leave the MID Server down. This problem is for error handling in this situation. That scenario should be checked for on startup, and as part of the pre-upgrade checks before committing to the upgrade. Breadcrumbs should be left before a restart, so that the MID Server can know a failed start happened, maybe read the relevant logs automatically, and clearly give the next steps to the user.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2052408

 [KB3157458](https://hi.service-now.com/kb_view.do?sysparm_article=KB3157458)

</td><td>

A pinned navigation menu takes more time to load than an unpinned one

</td><td>

When the user pins any Unified Navigation Menu, it takes more time to load than when unpinned.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2065785

</td><td>

The client sends uiMetadata as 'null' when selecting the **Stop** button after a page refresh during a Dynamic Loader message

</td><td>

When a Dynamic Loader message arrives and the page is refreshed while it's still loading, selecting the **Stop** button after reloading sends a stop\_flow action message with 'uiMetadata: null' instead of the expected contextual action metadata.

</td><td>

1.  Start a chat session.
2.  Trigger a flow/skill that sends a Dynamic Loader message.
3.  While the loader is still in progress \(before it resolves/completes\), refresh the page.
4.  Wait for the session to restore and the loading state to reappear.
5.  Select the **Stop** button.
6.  Inspect the outgoing message for the stop\_flow action.

 Expected behavior: RichControl.uiMetadata should contain the contextual action metadata.

 Actual behavior: RichControl.uiMetadata is null.

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

Advanced Work Assignment

 PRB2070097

</td><td>

AWA document re-evaluation job queries archive table \(ar\_incident\) directly by sys\_id

</td><td>

Some awa\_work\_item records have document\_table = 'ar\_incident' \(the archive table\), so the job ends up running the same live-table-style, filtered, batched query directly against the archive table.

</td><td>

1.  Query awa\_work\_item where document\_table = 'ar\_incident' — records exist.
2.  Let the daily 'AWA - Trigger Document Re-evaluation For Queued/Pending Accept Work Items' job run \(or trigger it manually\).

 Observe that it queries ar\_incident directly for those work items' sys\_ids, with the channel's business conditions \(assigned\_to IS NULL, state IN \(...\)\).

</td></tr><tr><td>

Agent Chat

 PRB2053704

</td><td>

Confusing '\_​live\_​agent\_​support\_​offglide\_​' is triggered in non-off Glide LLM conversations

</td><td>

 

</td><td>

1.  Start an LLM conversation.
2.  Request a live agent transfer.
3.  Check the corresponding topic being triggered in the sys\_cs\_conversation record.

 Observe that the topic '\_​live\_​agent\_​support\_​offglide\_​' is triggered even though the conversation is not an off Glide conversation.

</td></tr><tr><td>

Agent Chat

 PRB2057904

</td><td>

When an agent's Async Message Bus \(AMB\) connection breaks, they silently stop receiving work-item events with no indication that anything is wrong

</td><td>

They appear available but never get offered work.

</td><td>

1.  Log in as an agent.
2.  Open Service Operations Workspace \(SOW\).
3.  Make the agent online.
4.  Log in as an admin in another window.
5.  Navigate to the 'sys\_amb\_channel\_presence' table and disconnect AMB.
6.  Navigate to SOW.

 Expected behavior: See a modal that AMB got disconnected. When users select**refresh**, it auto connects.

 Actual behavior: Users aren't seeing the modal that AMB got disconnected, so the agent never knows.

</td></tr><tr><td>

Agent Chat

 PRB2068933

</td><td>

A workspace error is observed when handling incoming messaging interactions in Agent Workspace

</td><td>

In both scenarios, the error modal occurs.

</td><td>

Scenario 1:

 1.  Open a messaging interaction in the CSM workspace..
2.  As an agent, Navigate to any other tab than the ongoing interaction.
3.  Send one or more messages from the requester.
4.  Ensure sure the ongoing messaging count is visible.
5.  Switch to the current interaction.

 Observe the error modal.

 Scenario 2:

 1.  Open a messaging interaction in CSM workspace.
2.  Send one or more messages from the agent/requester.
3.  Refresh the page.

 Observe the error modal.

</td></tr><tr><td>

Agent Chat

 PRB2077124

</td><td>

A tab subheading displays 'Call is in wrap-up' while a call is still active in an agent-initiated wrap-up scenario

</td><td>

When an agent selects **Open Wrap-Up** MID-call, the tab subheading immediately changes to 'Call is in wrap-up' even though the voice call is still ongoing. This is misleading. The label implies the interaction is in wrap-up state, but the call has not yet ended. UX has confirmed the label should be changed to 'Wrap-up initiated' — a generic label that works accurately for both MID-call and post-call scenarios.

</td><td>

1.  Configure an NVC/CCaaS integration with supportExternalWrapUp = true on the Wrap Up macroponent.
2.  Start a voice call as an agent.
3.  While the call is still active, select the **Open Wrap-Up** button.

 Observe the tab subheading. It immediately displays 'Call is in wrap-up' even though the call is still ongoing.

</td></tr><tr><td>

Agile Development

 PRB2060695

</td><td>

Users are unable to scroll horizontally on agile\_boards

</td><td>

The horizontal scroll bar isn't visible inside the visible area due to the newly introduced message: 'Starting with the Australia release, the Agile Board is being prepared for deprecation. For details, refer to the Deprecation Process. Collaborative Work Management is recommended for Agile teams with a modern user experience.'

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2070503

</td><td>

The Mosaic response translation to the user's preferred language is failing

</td><td>

 

</td><td>

1.  Enable domain separation.
2.  Start conversations from different domains.
3.  Ensure records are not available cross the domain.
4.  Run the abandoned conversation job.

 Notice that the conversations do not get properly faulted and throws an exception.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2074876

</td><td>

Process A2A primary asynchronous responses to offglide via Hybrid Queue

</td><td>

Currently, external agent \(A2A\) primary async responses land in sn\_​aia\_​external\_​agent\_​primary\_​async\_​responses and are forwarded to offglide via a synchronous, in-transaction path \(A2aPrimaryAsyncEventHandler\) guarded by a raw Mutex. This blocks the event-delegator thread for the duration of the DB read + offglide POST + mark-processed sequence, and doesn't benefit from the platform's existing overflow/shutdown safety net.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2085529

</td><td>

AI Agent execution tool "AIA RAG Retriever" returns faulty URLs for search result items in VA and ES

</td><td>

When the RAG/semantic-search result's URL omits the leading forward slash, the resulting link is corrupted and unusable.

</td><td>

 

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2072025

</td><td>

sys\_ux\_theme\_asset records associated 'sys\_attachment' records have an incorrect state

</td><td>

It should be 'available' and not 'available\_conditionally'.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1859571

</td><td>

A search retrieval agent returns an incorrect catalog item URL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2074141

</td><td>

Changing a retention policy on an indexed source doesn't enforce guard rail recalculation

</td><td>

 

</td><td>

1.  See that the retention policy for an 'Incident' indexed source is two years.
2.  Verify that Semantic Index configuration in enabled.
3.  Verify that there's an entry in the ais\_​guard\_​rail\_​limit\_​data\_​source table.
4.  Change the retention policy on the indexed source to three years.

 The entry isn't recalculated in ais\_​guard\_​rail\_​limit\_​data\_​source.​

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2084573

</td><td>

In the 'Live Search' API, if a userId passed in x-run-as doesn't exist, then it throws an error

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2084574

</td><td>

IncludeSources and ExcludeSources support for the 'Live Search' API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2084575

</td><td>

REST API policy configurations in Moveworks API V2

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2086827

</td><td>

Handle duplicates with version, embedding model gracefully in ServiceNow Security Center \(SSC\)

</td><td>

This is metadata, so business rules aren't guaranteed to run \(for example, when coming in through an update set\), which is why there should be graceful handling of duplicates.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2087032

</td><td>

Incorporate new fields in AIS logging following the changes in AIS backend with new feature explain methods

</td><td>

After an Australia upgrade, search doesn't work from the Service Portal page.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2089496

 [KB3160302](https://hi.service-now.com/kb_view.do?sysparm_article=KB3160302)

</td><td>

The 'Book a meeting' Now Assist Virtual Agent \(NAVA\) test case is not working

</td><td>

The Now Assist skill discovery silently returns no sys\_gen\_ai\_skill results, even though the same prompt works on previous versions. This issue is caused by stale AI Search index data. Upgrading the instance changes code but does not re-ingest existing documents, so the new filter matches zero documents, and the skill disappears from discovery with no error. Any record created or edited after the upgrade is re-ingested under the new converter and self-heals, so only untouched records vanish.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2095212

</td><td>

SSC details override Next Wave request payload when both are present

</td><td>

When a Next Wave request is made with explicit parameters/details in the payload AND SSC \(Service Search Configuration\) details exist for the same context, the SSC details are taking precedence and overriding the values passed in the Next Wave request payload.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB2064865

 [KB3151377](https://hi.service-now.com/kb_view.do?sysparm_article=KB3151377)

</td><td>

Now Assist search results overlap when keyboard tabbing is used

</td><td>

During keyboard navigation through the interactive elements in the AI component, overflowed content overlaps with other elements, making the response/answer difficult to read. This was identified as an accessibility finding during a recent audit by the Accessibility Center.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search UX

 PRB1939328

</td><td>

A 'No Answer Found' Genius Result response shouldn't cause 'Has Results' to be true

</td><td>

 

</td><td>

1.  Open Virtual Agent.
2.  Search for something that return a 'No Answer Found' \(NAF\) response.
3.  Open the sys\_cs\_fdih\_invocation table and find the recent entry that corresponds to the search.
4.  Copy the 'searchAnalyticsPayload' object from the outputs json.
5.  Send that payload as a SEARCH\_EVENT to the Signals API, either via Scriptable or the REST API.
6.  Open the sys\_search\_event table and inspect the record corresponding to the payload just submitted to Signals. In particular, look at the **Has Results** field.
7.  Open the sys\_search\_signal\_event table and find the corresponding record.
8.  Inspect the **Genius Results** field.

 Expected behavior: The **Genius Results** field on sys\_search\_signal\_event should be empty. **Has Results** should be false.

 Actual behavior: The**Genius Results** field indicates a synthesized response was displayed, and **Has Results** is true.

</td></tr><tr><td>

AI Search UX

 PRB1988057

 [KB3220629](https://hi.service-now.com/kb_view.do?sysparm_article=KB3220629)

</td><td>

Hyperlinks in synthesized responses don't open in a new tab

</td><td>

When the user attempts to open a hyperlink from the synthesized result, it fails to open.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search UX

 PRB2069550

 [KB3156770](https://hi.service-now.com/kb_view.do?sysparm_article=KB3156770)

</td><td>

Search filters infinitely load on the Now Assist full page experience

</td><td>

A search refreshes with the correct filter, but the UI shows infinite loading.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search UX

 PRB2083562

</td><td>

Support right-click behavior for Service Portal search results

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1974104

</td><td>

The 'Sort by' value does not work in time series visualizations

</td><td>

The order changes, but in a pattern that is neither ascending or descending.

</td><td>

1.  Add a timeseries column chart.
2.  Add an incident table with the following:
    1.  Trend by: Year by Activity due
    2.  Group by: Assignment group
    3.  Sort data by value: ASC
3.  Hover on a chart.

Observe the values in the legend.

4.  Change sorting to 'DESC'.
5.  Hover on a chart.

Observe the values in the legend.

6.  Repeat the steps with 'Group by: State'.
7.  Change the group by aggregation to 'Hour of day by Opened'.
8.  Change DESC to ASC in all cases.

 Observe that the sorting by value is applied incorrectly – it's sorted, but in a strange order that is not ascending or descending. By changing the order, the values position changes, but the order is still not ASC or DESC.

</td></tr><tr><td>

Analytics Data API

 PRB1978825

 [KB2923876](https://hi.service-now.com/kb_view.do?sysparm_article=KB2923876)

</td><td>

'Total value' displays in the center of donut visualization changes with a 'Group By' adjustment

</td><td>

The inconsistency of the total number in the donut with different group by's is due to the fact that all these group bys have more than 50 elements. On the chart, maximum 50 elements are displayed, and the total number is calculated based on the sum value of these 50 elements, not the sum of all the elements.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2008673

</td><td>

A single score reported on a **Time** field with an aggregation as a sum is calculated correctly in the Core/Responsive UI experience but incorrectly in the Platform Analytics Next Experience UI

</td><td>

When a field is created as a dictionary type as 'Integer' and has an attribute 'format=glide\_duration', then the aggregation of this field on a native report or a responsive/core dashboard is displaying the duration sum aggregate properly. But when migrated to the platform analytics dashboard, the same field aggregation sum does not render the result correctly.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2079089

</td><td>

TableCleaner does not remove old cache entries if flag is\_queued=true

</td><td>

Old cache entries are not removed from sys\_analytics\_cache table if the flag 'is\_queued' is set to true.

</td><td>

 

</td></tr><tr><td>

API Access Policies

 PRB2065453

</td><td>

The RESTAPIAccessScopeRepo map overwrite loses required authentication scopes when two sys\_api\_access\_scope records share the same API signature

</td><td>

A 403 'User Not Authorized' error occurs.

</td><td>

1.  Install and activate both ServiceNow Otto for Document Voice and Dynamic Guidance applications.
2.  Confirm both sys\_api\_access\_scope records are active for the SNGenerativeAI API path sn\_generative\_ai/extensions, with all apply-all flags \(apply\_all\_methods, apply\_all\_resources, apply\_all\_versions\) set to 'true'.
3.  Call GET /​api/​sn\_​generative\_​ai/​extensions/​live-​llm-​configuration?​solution​Capability=​smartdocs\_​voice\_​qna with the Document Voice token.

 Observe that if the Dynamic Guidance Authentication Scope record loads last into the RESTAPIAccessScopeRepo's map, the call returns the error, '403 User Not Authorized - Missing required API access scope: Dynamic Guidance Auth Scope'.

</td></tr><tr><td>

Application Install Engine

 PRB2033816

</td><td>

The Backfill Module Key ID in encrypted attachment ZIPs are polluting the syslog

</td><td>

It creates content that looks like a ZIP file \(by name/MIME\) but isn't a GZIP. It forces the platform to read it as GZIP, which triggers the identical ZipException and syslog error that the Backfill job produces at scale.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1975999

</td><td>

The user can not update the customized app's base version when no new customized versions are available

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB2056916

</td><td>

Skip a license-blocked status for all dependencies in DependencyProcessor

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Appointment Booking

 PRB2074894

</td><td>

An appointment isn't working correctly after an upgrade

</td><td>

When the data format is set to dd-MM-yyyy, the appointment slots aren't retrieved correctly.

</td><td>

1.  Navigate to an instance.
2.  Set the date format to dd-MM-yyyy.
3.  Open any Record Producer in the Field Service Management \(FSM\) application.

There should be a calendar variable.

4.  Select the **Calendar** icon to select an appointment.

 Observe that no available appointment time slots are displayed.

</td></tr><tr><td>

Attachments to Records

 PRB2061519

</td><td>

GlideSysAttachment attachment loop silently truncates in scoped apps due to unhandled NullPointerException in RealTimeProtectionPolicyCache

</td><td>

A server-side script that loops through a record's attachments \(while \(gr.next\(\)\)\) and calls Glide​Sys​Attachment.​get​Content\(\)​/​get​Content​Base64\(\)​ inside that loop can silently stop after the first attachment, even when several exist.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB2084125

</td><td>

Workload identity federation support

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Base Asset Management

 PRB2055589

</td><td>

Make a serial number mandatory in Identification and Reconciliation Engine \(IRE\)

</td><td>

The follow list of model categories don't have IRE rules - thus there is no check on unique identifiers: Medical General, Facility General, HVAC, Fuel Tank, Structure, Fuel Tank, Transportation General, Aircraft, Ship, Train, Vehicle, and Retail General. If there is no IRE rule, it should fall back to either a serial number or asset tag as unique identifier for assets. Currently, there's no check on unique identifier.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2071462

</td><td>

System logs have the error 'Scoped cache operation against catalog nowassist\_admin was skipped because of an invalid sysId: no thrown error'

</td><td>

There's the sys\_ws\_operation 'Get Complete State', owned by package Human Resources: Core \(sn\_hr\_core\), operation URI /​api/​sn\_​hr\_​core/​hr\_​rest\_​api/​get\_​complete\_​state.​ configGr.skill\_config returns the raw GlideElement \(backed internally by com.​glide.​script.​Field​Glide​Descriptor\)​,​ and is never converted with .toString\(\). That object is then handed straight into sn\_​nowassist\_​admin.​Now​Assist​Skill​Config.​get​Skill​Configuration\(\)​ — a call across a scope boundary \(sn\_hr\_core → sn\_nowassist\_admin\).

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2072634

</td><td>

HR cases no longer **Apply** fields set from a template when created from the 'Create New Case'/'Case Creation' page

</td><td>

Starting in the Australia release, when users have an HR template that sets the state to 'Ready' or any other state, the case still gets created with the state of 'Draft'.

</td><td>

1.  Navigate to the 'Create New Case' module.
2.  Select any user.
3.  Select **HR Service** where the template is set to the state to 'Ready'.
4.  Select the **Create Case** button.

 Expected behavior: The HR case is created in 'Ready' state.

 Actual behavior: The HR case is created in 'Draft' state.

</td></tr><tr><td>

Case Management

 PRB2075237

</td><td>

Create an implementation to setWorkflow false for a table in the Case Management Core scope

</td><td>

Currently, the multi-case creation takes too much time. To solve the issue, setWorkflow should be set as false. setWorkflow can't be set as false to case management tables from the task plan template scope. Thus, an implementation should be added in the case management scope, which sets setWorkflow false for case and case task tables.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB2082276

</td><td>

**Analyze Access** UI Action needs migration to work in UI26

</td><td>

When the user selects **Analyze Access**, it redirects to '/​sn\_​access\_​analysis\_​request.​do.​.​.​' because the Ajax request is broken. It should redirect to '/now/access-manager/...'.

</td><td>

1.  Navigate to '/aiux/ui/incident\_list.do'.
2.  Select an incident.
3.  Select and hold \(or right-click\) on the form header.
4.  Select **Analyze Access**.

 Expected behavior: It redirects to '/now/access-manager/...'.

 Actual behavior: It redirects to '/​sn\_​access\_​analysis\_​request.​do.​.​.​' because the Ajax request is broken.

</td></tr><tr><td>

Client Scripts

 PRB2083604

</td><td>

For g\_modal.showFrame, a mechanism is needed to prevent iframe modal autoclose and a way to programmatically close

</td><td>

The EMPTY\_BODY auto-close mode closes the iframe modal on any intermediate navigation with non-empty content, not just when reaching the final empty page \(blank.do\). This breaks multi-step workflows where users navigate through preview or intermediate pages.

</td><td>

1.  Open an iframe modal with autoCloseOn: FrameModalCloseOn.EMPTY\_BODY.
2.  Navigate the iframe to a page with content \(for example, the preview page\).

 Observe that the modal closes immediately as 'Canceled'. The modal should remain open and wait for further navigation. Also, selecting **Create Excel Template** within the iframe modal does nothing.

</td></tr><tr><td>

Client Scripts

 PRB2084052

</td><td>

The list v2 scripting environment doesn't have access to form globals and angular globals \(NowAPI\)

</td><td>

The existing client script APIs \(for example, g\_modal and g\_ui\_scripts\) were only included in js\_include\_ui16\_form. They need to be extracted into a dedicated js\_include and included within the list page.

</td><td>

Access NowAPI on the list action page.

 Observe that NowAPI is undefined.

</td></tr><tr><td>

Client Scripts

 PRB2084585

</td><td>

Port g\_list.refreshWithOrderBy

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

CMDB Data Manager

 PRB2030582

</td><td>

CMDB Workspace does not show correct Cis in retire policy when using Portuguese language

</td><td>

When creating a retire policy in Portuguese language, in policy filter section, the CIs are not being returned. But when changed to English, correct CIs as shown.

</td><td>

1-create a retire policy in english 2 - in Policy filter, use filter in CMDB\_CI with 'OPERATIONAL STATUS = OPERATIONAL' 3 - see result 4 - change user language to portugues 5 - follow steps 2 above and see no results

 But when going to the cmdb\_ci table, and using the filter it will show results.

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2072350

</td><td>

Create additional fields and view for Dynamic IRE comparison enhancements

</td><td>

Currently the list and form view for the cmdb\_​ire\_​output\_​comparison\_​item table is too noisy and hides the important details. Additional columns should surface the important information in a meaningful manner that can be digested by the user.

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2077883

</td><td>

DynamicIRE cache build time is incorrectly reported in stats

</td><td>

The total time is tracked as build time, even when a cache miss occurs and the cache is flushed and rebuilt.

</td><td>

1.  Make sure the cache is warm.
2.  Request the model from cmdb\_ci\_hardware.
3.  Request something from the cache that doesn't exist, like the model for the cmdb\_ci class.

Observe that a cache miss occurs.

4.  Wait a few minutes, then flush the cache.
5.  Request something else from the cache.

Observe that the cache is rebuilt after being flushed.


 Expected behavior: The cache build time is accurately reported.

 Actual behavior: The total time between steps three and five is tracked as build time.

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2080716

</td><td>

A fix script is needed to turn on dynamic IRE for no-customizations users

</td><td>

Dynamic IRE should be enabled as long as there are no customizations to cmdb\_identifier, cmdb\_identifier\_entry, or ie\_active\_config.

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2080719

</td><td>

Class Manager's UI should be updated for a default-on dynamic IRE state

</td><td>

The existing UI flows should be preserved, but there's a new default-on state. Buttons, labels, and text need to align for the default-on state. When there are results and dynamic IRE is on, difference sampling shouldn't show the dashboard or have another action to load the dashboard.

</td><td>

 

</td></tr><tr><td>

CMDB Workspace

 PRB2085730

</td><td>

When Dynamic Identification and Reconciliation Engine \(IRE\) is turned on, there should be a banner added to the 'Products Highlight' section on the CMDB Workspace home page

</td><td>

 

</td><td>

1.  Turn on Dynamic IRE.
2.  Navigate to the CMDB workspace home page.

 There should be a banner in the 'Product Highlights' section with a **View details** button that links to the Dynamic IRE home page.

</td></tr><tr><td>

Code Signing

 PRB2088648

</td><td>

UI Actions are failing after upgrade to Australia

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1997702

</td><td>

Limited number of values are shown in the 'Is one of' filter in Workspace

</td><td>

The filter is truncated and there's no way to check which values are configured. When the user wants to edit, it's also not possible to see all of the values.

</td><td>

1.  Navigate to the list view in CSM/FSM or SOW.
2.  Use the list filter settings and locate a operator which has the option to be 'is one of'.
3.  Add more than 10 values to the proper field.
4.  Select **Run**.
5.  After it's executed, check the filter again.

 Observe that the filter is truncated and there's no way to check which values are configured. When the user wants to edit, it's also not possible to see all of the values.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1995308

 [KB2935998](https://hi.service-now.com/kb_view.do?sysparm_article=KB2935998)

</td><td>

There's a CDSM sync issue between Hardware Asset and CI

</td><td>

When a CI's lifecycle stage and status are explicitly set \(for example, Deploy / Test\), those values are unexpectedly overwritten after the CI is synchronized with its associated hardware asset. The overwritten values reflect a different lifecycle stage \(for example, Inventory / Available\) that does not match what was originally configured on the CI.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2086797

</td><td>

Auto-resolve de-duplication tasks using AI

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2086798

</td><td>

Task creation, batch processing framework, staleness agent ledger-based task orchestration, and lifecycle automation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2086799

</td><td>

Retirement definition and staleness configurations

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Contract Management

 PRB2024233

 [KB3151968](https://hi.service-now.com/kb_view.do?sysparm_article=KB3151968)

</td><td>

After installing the Service Management Core plugin, users lose the ability to view fields for ast\_contract

</td><td>

After the Service Management Core plugin is installed, users without the contract\_manager role \(such as those with the snc\_internal or sam\_user roles\) can't see several fields on the ast\_contract table, including **Description**, **Number**, **Short Description**, **Vendor**, and additional fields. The new field‑level read ACLs created by the plugin require the contract\_manager role, which overrides the existing table‑level ACLs and removes read permission for those users. Affected users can't view contract information that was previously accessible. Similarly, on an instance with the SAMS plugin, contract managers can't read the contract fields due to field-level ACLs introduced by the SAMS plugin.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2016899

</td><td>

The GlideRecord loadRow0 gets the wrong TD to add on the view of off row array values

</td><td>

 

</td><td>

Create a view on the sys\_user table for a user.

 Observe whether the roles are loaded or not.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2066352

 [KB3146240](https://hi.service-now.com/kb_view.do?sysparm_article=KB3146240)

</td><td>

GlideAggregate script and reports give an incorrect result when a query business rule is active

</td><td>

With a code change, any existing dashboard that uses widgets \(such as single scores\) ends up with incorrect results. This happens if the table they perform the aggregation on has a query business rule that performs an orderBy.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2045306

 [KB3137341](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137341)

</td><td>

Live Archive should not be installed on RaptorDB Pro instances until the product is ready

</td><td>

Archive tables and attachments referencing archived records are migrated to columnar tables and RaptorDB offloads them to S3.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2074320

</td><td>

Table cleaner shouldn't run on any tables

</td><td>

Table cleaner should skip columnar tables, but it attempts to run and it's too slow.

</td><td>

1.  Create a table cleaner rule targeting a columnar table.
2.  Execute the table cleaner job.

 Expected behavior: Table cleaner doesn't run on columnar tables.

 Actual behavior: Table cleaner attempts to run and it's too slow.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB2032709

</td><td>

Adopt Raptor connection pool feature

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Views

 PRB2062667

 [KB3153669](https://hi.service-now.com/kb_view.do?sysparm_article=KB3153669)

</td><td>

Platform Analytics indicators no longer generate scores after upgrading to Australia

</td><td>

After upgrading to Australia indicators using a database view as the facts table are no longer generating scores.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2076789

</td><td>

Update the data privacy ScriptableDataProtectionJob \_start method to restrict interactive sessions only for encrypted field anonymization

</td><td>

The API new SNC.​Data​Protection​Job\(\)​.​start\(\)​ only works if it's called from an interactive session because there is an explicit check done. The check should only be done for policies where encrypted field anonymization is required, because CLE consent is needed for encrypted field anonymization to run.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2082167

</td><td>

Data Privacy anonymization clone jobs aren't executed when the clone is initiated through a Clone Profile

</td><td>

The default value of the System Profile needs to be updated from false to true so that the clean-up script is executed by default during clone operations.

</td><td>

1.  Create an anonymization policy.
2.  Mark it for cloning.

 Expected behavior: It runs once cloning completes.

 Actual behavior: The job doesn't run.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2088199

</td><td>

Domain separation support for AI Control Tower \(AICT\) features

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Demand Management

 PRB2082513

</td><td>

Conditionally allow previous assessment business rules on the 'Demand' table

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Developer Sandboxes

 PRB2075044

</td><td>

Business Rules can be faster in a DSB by pre-rendering

</td><td>

The business rule can take around 100-120 seconds to open.

</td><td>

1.  Open Studio.
2.  Open a business rule within Studio.

 Observe that Studio takes around 50 seconds to open and the business rule takes around 100-120 seconds to open.

</td></tr><tr><td>

DirectSQL

 PRB2077815

</td><td>

Implicit joins should never be added for virtual fields

</td><td>

**Virtual** fields \(such as dbfunctions\) don't exist on the database and therefore never need implicit joins to a partition. The current code sends all column references through the addNeededJoinsForColumn path and incorrectly adds a self join. This can happen when the dbfunction is on a child TPH or TPP table because the ED looks like it's on a different storage table than the base table.

</td><td>

Select **func\_field** from tph\_child.

</td></tr><tr><td>

Discovery

 PRB2058910

 [KB3156347](https://hi.service-now.com/kb_view.do?sysparm_article=KB3156347)

</td><td>

Typo in the script in Sensor SNMP

</td><td>

Classify 'his' instead of 'this.'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Dynamic Scheduling

 PRB2084923

</td><td>

Dynamic Scheduling is not embedding the break when WFO is enabled and the 'Embed Break' property is enabled

</td><td>

With the latest WFO changes, Dynamic Scheduling is not working as expected when WFO is disabled.

</td><td>

1.  Ensure WFO is disabled in sm\_config.
2.  Create or identify a Work Order Task eligible for Dynamic Scheduling.
3.  Trigger agent assignment through Dynamic Scheduling.

 Observe that the Dynamic Scheduling flow invokes the Embedded Break Flow and the task is not assigned to an agent.

</td></tr><tr><td>

Email Notifications

 PRB2062773

</td><td>

The Now Assist Email generation sparkle icon loads slowly

</td><td>

It takes long time to show the Now Assist sparkle icon.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB2083210

</td><td>

Pass the reply ID and reponse type in a payload when performing pre-send validation

</td><td>

 

</td><td>

1.  Select **Reply** in an activity stream in a configurable send-enabled instance.
2.  Try to send.

 Before sending, the validation must catch the reply ID and response type so that further custom logic can be written to the reply ID.

</td></tr><tr><td>

Embedded Help

 PRB2057373

</td><td>

Instance Observers have some http connections that breach Cryptography Standard

</td><td>

Cryptography Standard \(POL0020873\), section 2.4 Data in Transit Encryption, requires TLS for all connections. SysEng: Core is decommissioning CDN HTTP endpoints to support modern ServiceNow technologies. However, Instance Observers currently depend on HTTP for some connections and can't migrate until this dependency is removed.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB2084219

</td><td>

Excessive processing time observed for Service Analytics alert grouping job

</td><td>

The Service Analytics scheduled job 'Service Analytics group alerts using RCA/Alert Aggregation' experiences performance degradation, taking 11+ minutes to process only 2,145 alerts with 513 groups.

</td><td>

 

</td></tr><tr><td>

Experimentation Platform

 PRB2088196

</td><td>

True-up of the Experimentation Framework store app from 1.1.14 to 1.1.20

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Field Normalization

 PRB1981660

</td><td>

Field normalization creates duplicate sys\_audit records

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Field Service Task Bundling

 PRB2064856

</td><td>

Dynamic bundling creates unassigned bundles

</td><td>

 

</td><td>

1.  Verify that Dynamic Scheduling, Task Bundling, and Task Grouping plugins are active.
2.  Enable the sys\_property 'com.snc.dynamic. scheduling.bundle\_ before\_scheduling'.
3.  Set the Task Grouping rules \(Same Location\) and policy.
4.  Create two work order tasks \(WOT\) in the draft.

 Notice that once the WOTs are moved to the 'Qualified \(Pending Dispatch\)' state, the tasks should be bundled using Dynamic Bundling and Dynamic Schedule the tasks automatically.

</td></tr><tr><td>

Field Service Task Bundling

 PRB2079508

</td><td>

Changing the assignee of the child work order task \(WOT\) of a bundle task makes the bundle task disappear from Dispatcher Workspace

</td><td>

 

</td><td>

1.  Impersonate as a dispatcher.
2.  Create a work order from Customer Service Management workspace.
3.  Create two work order tasks in the work order record.
4.  Select **Ready for dispatch** for both WOTs.
5.  Open Dispatcher Workspace.
6.  Select the two WOTs and select **Bundle**.
7.  Drag and drop the bundle task to some assignee.

 Changing the assignee of the child work order task \(WOT\) of a bundle task makes the bundle task disappear from Dispatcher Workspace.

</td></tr><tr><td>

Field Service Task Bundling

 PRB2080761

</td><td>

Dynamic bundling creates unassigned bundles

</td><td>

Set assignment\_group on bundles created through dynamic bundling. When a task is added to an existing bundle, the bundle's assignment group is now carried into the task update payload, and when a new bundle is created the assignment group of the selected agent \(resolved via the new \_getGroupIDForAgent helper\) is written to both the new bundle and the task update payload. For the territory model, FSMTaskBundleSNC.\_getTasks now rolls up the assignment group from a subtask when the bundle itself has none, so territory-based bundles are no longer left without an assignment group.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2059346

</td><td>

Flow context gets completed, but the event isn't relayed to playbook engine, so the activity context doesn't get completed

</td><td>

 

</td><td>

1.  Create a playbook with one normal activity \(say instruction\).
2.  Add one optional activity \(instruction\).
3.  In runtime, add six instances of the optional activity.
4.  Start marking the optional activity complete, from the last in the list to the top.

 Observe that the corresponding activity context is in progress, but the flow context gets completed.

</td></tr><tr><td>

Flow Engine

 PRB2069407

</td><td>

Refer to the commons-glide servicetype instead of engine code

</td><td>

Currently, it's passing mcp-server as the service type for mcp, but it should use InboundServiceType to keep consistent.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2077987

</td><td>

New columns added to the sys\_flow\_plan\_context table are missing a key

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2079986

</td><td>

Add 'custom/non-custom' for the non-mcp flow metric

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1914472

</td><td>

The 'Retry policy' isn't accessible when a flow is executed by a non-admin

</td><td>

 

</td><td>

1.  Create a flow with a REST step, which has a retry policy specified inline.
2.  Invoke the flow in the background as a non-admin user.

 See messages saying 'Security constraints prevent displaying information' due to attempting to access the 'Retry' policy as a non-authorized user.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1990001

</td><td>

Calling sn\_generative\_ai. GenAIStatsUtil\(\). logStats\(inputs\); logs double entries in sys\_gen\_ai\_usage\_log

</td><td>

The are more entries than expected after calling sn\_generative\_ai. GenAIStatsUtil\(\). logStats\(inputs\);.

</td><td>

1.  Enable flow recommendations on the instance.
2.  Navigate to a flow
3.  Select a plus to add an action.
4.  Select one of the recommendations.
5.  Navigate to sys\_generative\_ai\_log. This table lists all calls to AI.
6.  Sort by 'Created', Z-A

Note that there are three records for flow recommendations, and one of them has 'Feedback=ACCEPTED'.

7.  Navigate to sys\_gen\_ai\_usage\_log.
8.  Sort by 'Created', Z-A.

 Notice that there are two records and four flow recommendations.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2019712

</td><td>

The 'See Related Flows' action in 'subflow' displays flows with no current reference to a subflow when stale sys\_hub\_sub\_flow\_instance records exist from old snapshots

</td><td>

The 'See Related Flows' action in 'subflow' displays that the subflow is referenced by other flows even though it is not.

</td><td>

1.  Open an exiting subflow that is referenced by another subflow/flow \(parent\).
2.  Create a copy of this subflow.
3.  Activate it.
4.  Edit the parent flow by adding a step calling the copied subflow.
5.  Save/activate the flow.
6.  Edit the parent flow again, and remove the step that calls the copied subflow.
7.  Save the flow.
8.  Open the copied subflow from the 'Actions'.
9.  Choose **See related flows**.

 Notice that the flow is still shown referencing the parent flow.

</td></tr><tr><td>

GlideAggregate API

 PRB2090884

</td><td>

For non-admin callers, a regression results in the **Aggregate/Stats API** field validation conflating 'field doesn't exist' with 'field exists but read-ACL denies it'

</td><td>

When a non-admin caller queries the Aggregate/Stats API \(/api/now/stats/\{table\}\) using sysparm\_min\_fields, sysparm\_max\_fields, sysparm\_avg\_fields, or sysparm\_sum\_fields, the API incorrectly rejects fields the caller is not allowed to read as if those fields did not exist. Any non-admin identity that has a field-level ACL restriction on one of the fields it requests receives a hard failure instead of the expected ACL behavior. This is a regression related to PRB2081870, which addressed reflected XSS issues.

</td><td>

1.  Pick any table \('T'\) with a field \('F'\) that has a field-level read ACL restricting a non-admin role.
2.  As the non-admin identity, get /​api/​now/​table/​T?​sysparm\_​fields=​F,​sys\_​id&amp;​sysparm\_​limit=​1 and confirm F is absent or blanked in the response.
3.  As the same non-admin identity, call: GET /​api/​now/​stats/​T?​sysparm\_​max\_​fields=​F.​

 Expected behavior: Either a normal aggregate result with F omitted/blank, or a proper ACL-style denial.

 Actual behavior: HTTP 400, 'Invalid sysparm\_max\_fields parameter' - reported identically to what a user would see for a field name that doesn't exist on T at all.

</td></tr><tr><td>

Global Ranking

 PRB2085480

</td><td>

Implement CWM Dynamic Schema Helper script include

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

GraphQL API

 PRB2074367

</td><td>

TableFieldFactory caches a list of tables causing performance degradation

</td><td>

A performance regression affects inbound GlideRecord schema GraphQL requests on busy, multi-node instances. A reference table name cache is flushed instance-wide whenever any table in the GraphQL schema changes, rather than just the affected table. On high-transaction instances this triggers frequent full cache rebuilds, and GraphQL requests must wait for the rebuild to finish. This includes other requests in flight, since the cache is shared across the node.

</td><td>

1.  Send several GlideRecord\_Query GraphQL request, observe the numerous ACL table checks for a table with many reference fields.
2.  Make a small change to a table that doesn't impact a reference field.

 Observe entire cache flush of table list cache.

</td></tr><tr><td>

GRC Platform Plugins

 PRB2061497

</td><td>

Export to PDF action is cutting off and overlapping text

</td><td>

 

</td><td>

1.  Create a policy
2.  Import a word document with a link.
3.  Publish it.
4.  Open the KB article attached to policy in classic view.
5.  Select **View article**.
6.  Print the article.

 Observe that the **Export to PDF** action cuts off and overlaps text.

</td></tr><tr><td>

Group and Action Framework - Family

 PRB2025623

 [KB3157728](https://hi.service-now.com/kb_view.do?sysparm_article=KB3157728)

</td><td>

The base instance business rule 'CSM NATT- Assign case to cluster' leads to OutofMemory heap space errors

</td><td>

Multiple 'ASYNC: CSM NATT- Assign case to cluster' jobs running on the nodes are causing OutOfMemoryError: heap space, leading to node restarts.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Horizon Component Library

 PRB2075454

</td><td>

Voice evalulation's Otto 'mic' icon is missing on the homepage in the latest skill kit

</td><td>

 

</td><td>

1.  On an instance running the Otto skill kit, navigate to the 'Agentic Evaluations' homepage.
2.  Select the **Select what you want to evaluate** modal.

 Observe that the chat agent or workflow icon renders correctly. The voice agent or assistant \(mic\) icon doesn't render.

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

 PRB2046081

</td><td>

User registration from the CSP portal is giving error, 'There was an error processing the Link. Please use a valid link.'

</td><td>

When the user enters a Norwegian phone number when registering using the CSP portal they are directed to the following error, 'Error: There was an error processing the Link. Please use a valid link as discussed over this task.'

</td><td>

 

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

 PRB2075799

</td><td>

Create definitions for cases created by external users in Portals and Engagement Messenger

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1998455

</td><td>

Choices of multi-row variable sets \(MRVS\) aren't translated in the rich description of an HR case created from a record producer

</td><td>

Stored values appear in English.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2083402

</td><td>

RCAs that were moved to ServiceNowOtto are needed for HR Core/HR LE/HR ER

</td><td>

ACLs were moved to ServiceNow Otto for HRSD. Their RCAs are needed because they're used to verify that the user can read the source record, which can come from LE, HR Core, or ER.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2084464

</td><td>

Add a new scope to scope RCAs from the new app to HR core plugin

</td><td>

A new scope needs to be added to scope RCAs from the app 'HRSD L1 AI Specialist' to 'Human resource: core app' to access HR tables and other necessary data.

</td><td>

 

</td></tr><tr><td>

HTTP Client

 PRB2031497

 [KB3137790](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137790)

</td><td>

A rest step sees Norwegian characters in the XML response body from an external API with incorrect encoding

</td><td>

The Norwegian characters are displayed incorrectly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Identification and Reconciliation API

 PRB2004173

</td><td>

A certification audit produces incorrect failed results for first and last records when a template has reference-based related list conditions

</td><td>

This only impacts audits with reference-based related list conditions \(non-REL: join\_column in cert\_related\_list\_cond\). Attribute conditions, CI/User/Group relationship conditions, and REL:-based related list conditions are unaffected as they use different code paths.

</td><td>

 

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB2055912

</td><td>

originatedFromFlow is always false in Integration​Usage​Transaction​Monitor,​ as flow-origin detection is broken for action fabric record-action metering

</td><td>

The originatedFromFlow dimension on action fabric record-action telemetry is never set to true. Integration​Usage​Transaction​Monitor decides flow origination once, at transaction start, by checking whether the transaction's usage-tracker context contains a UsageSource.FLOW event. That event doesn't exist yet at transaction start, is removed again before transaction completion, and for asynchronous/scheduled flows the monitor doesn't run at all \(background transactions are not a handled type\). As a result, record actions performed by flows are not attributed as flow-originated, degrading the accuracy of record-action metering.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1940978

</td><td>

There's many IDR-DCTComparisonJobs on an instance

</td><td>

This is likely only a cosmetic issue and not hurting performance. Instances have at least 1 IDRDCTComparisonJob per node, which seems excessive. For instances with many nodes, this ends up being the majority of IDR jobs. There's only a few consumer jobs per instance \(not per node\).

</td><td>

On an instance running a version lower than Australia and configured with multiple nodes, open the sys\_trigger table.

 Notice that there's multiple IDRDCTComparisonJob records present.

</td></tr><tr><td>

Integration Hub

 PRB2086800

</td><td>

True-up for Workflow Data Fabric credits

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

IT Asset Management for Financial Services

 PRB1908524

</td><td>

When evidence is moved to 'Complete', check that at least one attachment or one URL is provided

</td><td>

Users shouldn't be allowed to save an asset evidence task unless a URL or attachment is provided.

</td><td>

1.  Provision an instance with the required GRC plugins and the Asset Audit Response plugin installed.
2.  Create an asset evidence task.
3.  Select **Accept**.
4.  Create asset evidence.
5.  Fill in the mandatory fields.
6.  Select **Complete** and **Save**.

 Observe that the evidence is saved. The save shouldn't be allowed unless a URL or attachment is provided.

</td></tr><tr><td>

Knowledge Management

 PRB1990998

</td><td>

Selecting **Machine Translate** on a source article with knowledge blocks is overriding translated block content

</td><td>

Before selecting **Machine Translate**, there are different block numbers in the different language articles. After, the block in the targeted translation article is replaced with the English version block.

</td><td>

1.  Log in to a base instance as a user with elevated privileges.
2.  Navigate to the English version of any article that has a published translated version and has blocks in it.
3.  Navigate to the article body section of the English version.
4.  Add a test sentence.
5.  Select the **Update** button to save changes to the English version.
6.  Scroll to the 'Related Links' section.
7.  Select **Translate**.
8.  From the 'Translate to' option, select the language of the existing translated version of the article.
9.  Validate the blocks on both the language articles.

Observe that there are two different block numbers.

10. Select the **Machine Translate** button.
11. Confirm that the translated content includes the test sentence.

 Observe that the block has been replaced with the English version block in the targeted translation article.

</td></tr><tr><td>

Knowledge Management

 PRB1999848

</td><td>

Anchor tags \('\#'\) in URLs are stripped from Word document imports in knowledge articles

</td><td>

The anchor shouldn't be removed and the link should take the user to anchored area. Instead, the anchor is removed, and the link takes the user to the top of the page.

</td><td>

1.  Navigate to **Knowledge** &gt; **Import articles**.
2.  Import a Word document that has a URL with an anchor tag.
3.  Verify that the import is completed.

 Observe that the anchor tag part of the URL is removed from the link. When the user selects the URL, it navigates to the top of page instead of the anchored area.

</td></tr><tr><td>

Knowledge Management

 PRB2034553

 [KB3137475](https://hi.service-now.com/kb_view.do?sysparm_article=KB3137475)

</td><td>

When users navigate to a 'Retired' Knowledge article on Service Operations Workspace, the **Edit** button doesn't appear, meaning users can't republish the article

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2054635

</td><td>

Previous Knowledge Articles are transitioned from Outdated to Publish to Outdated when a new version is created with Publish Flow

</td><td>

When a Knowledge Article with versioning enabled is published via Publish Flow, the previous version's Workflow state displays an incorrect transition in its audit history.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2063214

</td><td>

Tables in the generated KB article are displayed with bold borders, which differs from the source document formatting

</td><td>

This logic comes from the Word to HTML conversion from the KM API.

</td><td>

1.  Navigate to **Policy and Compliance** &gt; **Compliance Workspace**.
2.  Create a new policy record \(or use an existing draft policy\).
3.  Populate the required policy fields.
4.  Assign yourself as the policy owner.
5.  Enable the policy for knowledge publication \(if applicable in the environment\).
6.  Create a .docx file that includes a table.
7.  Upload the file using the **Import Policy Text** button.
8.  Verify that the document content is imported into the policy text section.
9.  Save and update the policy record.
10. Move the policy through the life cycle: **Draft** &gt; **Review** &gt; **Awaiting Approval** &gt; **Approved**.
11. Publish the policy by selecting **Publish**.
12. Confirm the policy transitions to the 'Published' state.
13. Verify whether a corresponding Knowledge Article is automatically generated in kb\_knowledge and linked to the policy record.

 Observe that the generated Knowledge Article may incorrectly display tables with bold borders.

</td></tr><tr><td>

Knowledge Management

 PRB2070212

</td><td>

Second-level bullet points render as filled black circles instead of the expected empty/hollow circle

</td><td>

The bullet style for second-level items is incorrect. The logic comes from the Word to HTML conversion from the KM API.

</td><td>

1.  Navigate to **Policy and Compliance** &gt; **Compliance Workspace**.
2.  Create a policy record \(or use an existing draft policy\).
3.  Populate the required policy fields.
4.  Assign yourself as the policy owner.
5.  Enable the policy for knowledge publication \(if applicable in the environment\).
6.  Create a .docx file that includes a bulleted list with two levels.
7.  Upload the file using the **Import Policy Text** button.
8.  Verify that the document content is imported into the policy text section.
9.  Save and update the policy record.
10. Move the policy through the life cycle: **Draft** &gt; **Review** &gt; **Awaiting Approval** &gt; **Approved**.
11. Publish the policy by selecting **Publish**.
12. Confirm the policy transitions to the 'Published' state.
13. Verify whether a corresponding Knowledge Article is automatically generated in kb\_knowledge and linked to the policy record.

 Observe that the generated Knowledge Article may render second-level bullet points as filled black circles.

</td></tr><tr><td>

Knowledge Management

 PRB2076447

</td><td>

The Auto-fix plugin update blocks the Australia upgrade in loadsim release testing

</td><td>

The plugin upgrade thread handling becomes stuck in an error loop triggered by a null pointer. It never exits or advances, leaving the upgrade 'hung'. This happens when the upgrade plugin loader reaches the knowledge center update that adds in the auto-fix and auto-fix enable property.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2077445

</td><td>

Updating versions for the base instance Knowledge Management apps to include Australia and Brazil fixes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2082853

</td><td>

When Word documents are converted to policy text or knowledge articles, hyperlinks appear on a new line instead of remaining on the same line

</td><td>

The dom element of the hyperlink gets nested inside the paragraph for the hyperlink, which continues on the same line correctly. However, the JAVA code points to the closing of a paragraph tag before the hyperlink tag, so it becomes a sibling and not a child. This makes it jump to a new line.

</td><td>

1.  Create a document with three links in the same line.
2.  Import the document as a knowledge article.

 Observe that some of the links appear on a new line.

</td></tr><tr><td>

Knowledge Management

 PRB2083241

</td><td>

True up for Australia and Brazil

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2084586

</td><td>

True-up Store apps NAKM, KC, KCInWorkspaces and ECE versions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2085202

</td><td>

A page scroll bar isn't seen for long markdown articles, as in the case of HTML

</td><td>

The issue doesn't appear in Workspace.

</td><td>

1.  Log in to an instance.
2.  Create a markdown type article.
3.  Open the article.
4.  Navigate to the related list.
5.  Translate the article.

Observe that this opens kb\_create\_translations.do.

6.  Check the page scroll.

 Expected behavior: The content on both side should be scrollable.

 Actual behavior: The content isn't scrollable.

</td></tr><tr><td>

Knowledge Management

 PRB2086922

</td><td>

The 'KB Health score config' column is missing from the kb\_knowledge\_base table

</td><td>

 

</td><td>

1.  Provision an Australia or Zurich instance with the NAKM plugin installed.
2.  Check the kb\_knowledge\_base table.

 Observe that it doesn't have the 'KB Health score config' column.

</td></tr><tr><td>

Knowledge Management

 PRB2090439

</td><td>

Due to Generative AI Controller \(GAIC\) layer issue, multi-KB generation is broken and Mosaic migration should be reversed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2027491

</td><td>

There's a null pointer exception in List​Layout.​get​Grouped​Row​Layout​Query from a null integer auto-unbox on List​Layout​Builder.​get​Record​Count​Limit\(\)​

</td><td>

Any workspace preset that calls getListLayout / getTinyListLayout with ignoreTotalRecordCount=true and a GROUPBY query, on a table not in the omit-count property, is facing this issue.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2033991

</td><td>

The column filters are not applying as expected

</td><td>

When applying the column level filter, the select is empty for the **Short description** field, and the user observes that the list is not filtered.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2039348

</td><td>

In the List view, the first choice is shown and is not the selected choice for the lookup select box variable in the workspace

</td><td>

Irrespective of whatever option the user might have selected, it will show the first choice in the workspace List view.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2084609

</td><td>

sysparm\_filter\_only parses a query but doesn't query data

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Column Menu

 PRB2038623

</td><td>

Selecting the three dots beside State doesn't work on Risk Workspace

</td><td>

The column filter for the **risk.state** field in the Risk Management Workspace list view is unresponsive, even though the field displays values correctly.

</td><td>

1.  Navigate to the Risk Management Workspace.
2.  Open the Risk Assessment list view.
3.  Ensure the **risk.state** field is added as a column in the list.
4.  Verify that the risk.state column displays values for the records.
5.  Select the three‑dot menu \(column filter icon\) for the **risk.state** field.

 Observe that the filter menu does not appear, and the three‑dot menu remains unresponsive. Open the browser console and note the JavaScript error indicating undefined data, which prevents the filter component from rendering.

</td></tr><tr><td>

List Column Menu

 PRB2077157

</td><td>

Grouping by any field displays a '$c66360ca901b4a5387c58a30a4270909\[List​Properties.​get​Grand​Total​Rows\(\)​\]​ total $c66360ca901b4a5387c58a30a4270909\[List​Properties.​get​Title\(\)​\]​' on the list view

</td><td>

This issue was observed in an Australia instance.

</td><td>

1.  On an Australia instance, open sc\_cat\_item.list.
2.  On the **Short description** column, right click on the three dots.
3.  Use 'Group By Short description.'

 Notice on the top banner, that $c66360ca901b4a5387c58a30a4270909\[List​Properties.​get​Grand​Total​Rows\(\)​\]​ total $c66360ca901b4a5387c58a30a4270909\[List​Properties.​get​Title\(\)​\]​ is displayed at the top.

</td></tr><tr><td>

Lux List

 PRB2090647

</td><td>

Missing fListEditRefQualTag parameter from ReferenceQualifier.add\(\) in line 630 rom ReferenceFieldEvaluator.java

</td><td>

A parameter was removed while merging track/anowassistgapatch to the Australia branch.

</td><td>

 

</td></tr><tr><td>

Microsoft Reconciliation

 PRB2031719

</td><td>

Fix overly restrictive SQL Server reconciliation logic that requires pattern-based ServiceNow discovery

</td><td>

When determining whether to ignore SQL Server installs from reconciliation, the code checked for Discovery Source = ServiceNow AND Created by Application Pattern = false. This logic incorrectly forced users to use pattern-based ServiceNow discovery exclusively. This approach is overly restrictive.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1979997

</td><td>

Windows MID Server fails to upgrade because it's not installed in English

</td><td>

The process looks for STATE instead of ESTADO to find out the server status, and it does not find it.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2078177

</td><td>

RDP client fails to fetch FQDN with the error 'Unknown tag 4'

</td><td>

The agent logs FQDN lookup falls back to DNS with an error. The last four bytes are the error code STATUS\_NOT\_SUPPORTED \(0xc00000bb\).

</td><td>

1.  Configure the target windows server with the following settings: **gpedit.msc** &gt; **Computer Configuration** &gt; **Administrative Templates** &gt; **System** &gt; **Credentials Delegation** &gt; **Encryption Oracle Remediation - Enabled \(Protection level - Forced Updated Client\)**.
2.  Run windows discovery with the following MID configuration: MID.​powershell\_​api.​wmi.​fqdn\_​method = RDP.

 Observe that the agent logs FQDN lookup falls back to DNS with the error: 'DEBUG \(Worker-​Expedited:​Multi​Probe-​e43cdafc3b6ecf503886e28e53e45aa0\)​ \[RdpClient:186\] Received NTLM response 30, 0D, A0, 03, 02, 01, 06, A4, 06, 02, 04, C0, 00, 00, BB.' The last four bytes are the error code STATUS\_NOT\_SUPPORTED \(0xc00000bb\).

</td></tr><tr><td>

Mobile Platform

 PRB2070684

</td><td>

Check for SN-Client-Id in mobile request headers instead of always assuming that the user is on the lowest ordered native client

</td><td>

Mobile clients add SN-Client-Id to all request headers after the initial user\_client response. The backend should use this as the source of truth to know which experience \(native client\) the user is actively on.

</td><td>

1.  Log in to the Mobile app.
2.  Switch from the default experience to experience B.

 The backend should send responses based off of the SN-Client-Id in request headers instead of assuming the user is on the lowest ordered native client they have access to.

</td></tr><tr><td>

Mobile Platform

 PRB2084601

</td><td>

Add a logo configuration option to sys\_sg\_applet\_launcher

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB2084603

</td><td>

EmployeeWorks Mobile updates

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB2084604

</td><td>

Auto-routing AIUX links to Mobile apps

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB2087059

</td><td>

Mobile App Config Business Rule \(BR\) clears customer\_​override\_​configurations on web experience add

</td><td>

The BR reads the new configuration and directly assigns it to customer\_​override\_​configuration without first reading and merging with the existing JSON object, causing any keys not explicitly set in the current BR logic to be lost.

</td><td>

1.  Log in to any Australia instance with mobile\_admin role user.
2.  Create a new native client record \(sys\_sg\_native\_client\).
3.  Open the corresponding sys\_analytics\_app\_config record.
4.  Manually add an existing customer\_​override\_​configuration value \(for example, \{'HeartbeatInterval': 30000\}\).
5.  Return to the native client record and add a web experience \(sets SendWebEventsToMobile = true\).

This triggers the Mobile App Config BR on update.

6.  Recheck the sys\_analytics\_app\_config record's **customer\_​override\_​configuration** field.

 Expected behavior: The customer\_​override\_​configuration should preserve the existing HeartbeatInterval key and merge any new keys added by the BR.

 Actual behavior: The customer\_​override\_​configuration is completely overwritten; HeartbeatInterval and other pre-existing keys are removed.

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2073299

</td><td>

MMS Glide update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2076357

</td><td>

Update system properties default values for MMS

</td><td>

MMS is not queuing enough records. The system propertyies 'glide.​platform\_​mm\_​service.​job.​batch\_​size' should be set to '10' and 'glide.​platform\_​mm\_​service.​async\_​http\_​max\_​outstanding\_​requests' should be set to '20'.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2082821

</td><td>

Result and metadata attachments are written with no owning record

</td><td>

MMS writes its parsed-text and metadata result artifacts to sys\_attachment without a table\_name or table\_sys\_id, so those attachments have no owning record. Reference-image attachments are unaffected — they are correctly parented to sys\_mm\_reference\_image.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2084570

</td><td>

Enabling the 'Image' file type to be on by default for MMS for AI Search

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2084571

</td><td>

MMS Glide update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Next Experience All Menu

 PRB2074680

</td><td>

The Now Assist 'Launch Mode' menu label in Display Preferences is not updated to Otto

</td><td>

 

</td><td>

1.  Navigate to 'Home'.
2.  Select the user profile icon.
3.  Open 'Preferences'.
4.  Navigate to the 'Display' section.

 Observe the 'Now Assist Launch Mode' menu label.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2078176

</td><td>

The NAP notification count disappears after page refresh and also displays an incorrect count compared to the active conversation count

</td><td>

After refreshing the page, the NAP notification count disappears and doesn't reappear on subsequent refreshes. The issue isn't reproducible in SurfStage, where the counter continues to work correctly even after a page refresh. The count appears again when the same URL is opened in a new browser tab. Also, the NAP notification counter sometimes displays a higher count than the actual number of active conversations, resulting in an inconsistent and incorrect notification count.

</td><td>

1.  Navigate to the NAP notification counter area.​

Observe the counter value and compare it with actual active conversation count.

2.  Refresh the page.

 Observe that the notification count disappears and doesn't reload. Also, the counter value is inflated compared to actual active conversations.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2079464

 [KB3154841](https://hi.service-now.com/kb_view.do?sysparm_article=KB3154841)

</td><td>

Duplicate Nextwave Client REST API definition causes a 403 error on session\_info for external users, disabling lbf-chat-client

</td><td>

Some users are unable to start a chat session in the assistant/chat widget. This is caused by a backend configuration issue and doesn't require any action.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2079773

</td><td>

Set token\_exchange\_allowed to 'true' on an OffGlide AIEX oauth entity record

</td><td>

Notice that token\_exchange\_allowed is 'false' which needs to be 'true', otherwise oauth will fail for guest users.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2081424

</td><td>

Set bff\_cookie\_exchange\_allowed to 'true' on OffGlide AIEX oauth entity records

</td><td>

bff\_cookie\_exchange\_allowed is set as 'false', which need to be 'true', otherwise oauth will fail for the guest user.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2085243

</td><td>

Page context updates aren't sending the backend the current URL

</td><td>

 

</td><td>

1.  Open an instance.
2.  Open AIEX.
3.  Perform any workspace navigation that triggers a page context update to the backend.

 Expected behavior: The URL is sent in the page context payload.

 Actual behavior: The URL is not sent in the page context payload.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2087666

 [KB3159370](https://hi.service-now.com/kb_view.do?sysparm_article=KB3159370)

</td><td>

The **AI Workflow** button opens a blanket panel on the core-ui form

</td><td>

The button is expected to display the AI activities/steps performed as part of the Resolution Plan Generation use case.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

On-Call Scheduling

 PRB2081079

 [KB3155856](https://hi.service-now.com/kb_view.do?sysparm_article=KB3155856)

</td><td>

It takes a long time to load Incident Communication Plan

</td><td>

On instances with a large number of configured on-call groups and rosters, opening or refreshing the Communication Plan on a major incident takes significantly longer than expected.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OneExtend

 PRB2076738

</td><td>

Update the model display names in the Gen AI model configuration table

</td><td>

 

</td><td>

1.  Update the model display names.
2.  Make gemini pro model as 'active=false' and the 'lifecycle' state as 'deprecated'.
3.  Make gemini 3 flash as the action **Delete**.

</td></tr><tr><td>

OneExtend

 PRB2078604

</td><td>

Add caching for BYO PII

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB2072285

 [KB3159113](https://hi.service-now.com/kb_view.do?sysparm_article=KB3159113)

</td><td>

GroupBy visualizations can cause an out of memory error

</td><td>

The heap dump provided in the task clearly shows that one widget consumes 190 MB. This is too much for a user transaction that is loading a dashboard.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2050570

</td><td>

Core UI dashboards displayed in library for users without roles

</td><td>

Core UI dashboards that have not been explicitly shared are appearing in the libraries of users without roles.

</td><td>

1.  Provision an instance on which the dashboard migration has not been finished.
2.  Impersonate a user without a role.
3.  Open platform analytics library.

 Expected behavior: No dashboards are listed.

 Actual behavior: Some dashboards are listed.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2060938

</td><td>

An impersonated user sees the impersonator's bookmarked indicators, and the bookmark filter then returns no results

</td><td>

In an Indicator Scorecard, users can bookmark individual indicators \(the star on each row\) and then filter the list to 'show bookmarked only'. When an administrator impersonates another user, the scorecard incorrectly shows the admin's bookmarks as if they belonged to the impersonated user. If the bookmark filter is then applied it returns no results at all, and after turning the filter off again all bookmarks disappear from view. Impersonation is the normal way administrators and support staff verify what an end user can see. While this issue is present, that check gives the wrong answer for bookmarks, and the bookmark filter appears completely broken. Scope note: no user's bookmarks are visible to any other real user. The incorrect data is only ever shown to the administrator who is impersonating, and only within that one browser session. Logging out clears it. Verified: a different browser, or a private/incognito window, always shows the correct bookmarks.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2075538

</td><td>

In the Platform Analytics Spanish localization, search and date range filters aren't working correctly

</td><td>

Users with Spanish language settings can't search visualizations or dashboards properly, and date range filters are read-only for day selection. The problem impacts Spanish localization specifically, causing different search results and disabled date selection compared to English.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2075761

</td><td>

'sn\_app\_analytics\_w' app upgrades are inconsistent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2076990

</td><td>

**The AIDE Explore** button shown on all lists, including 'All Table Discovery' entities

</td><td>

**The AIDE Explore** button is being shown on all entity lists, including entities that should not have it. Only entities marked 'Active=true' and 'population\_source=Table configuration' should display the **Explore** button. Entities with 'population\_source = All Table Discovery' \(or inactive entities\) should not show the **Explore** button.

</td><td>

Open an entity list that is marked as 'All Table Discovery'.

 Observe that the **Explore** button is present.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2079191

 [KB3152739](https://hi.service-now.com/kb_view.do?sysparm_article=KB3152739)

</td><td>

Remove sys\_​script\_​fix\_​ee3a858a4b8203101a31117f2974612b.​xml

</td><td>

The script sys\_​script\_​fix\_​ee3a858a4b8203101a31117f2974612b.​xml introduced in Australia causes upgrade delays due to the huge number of records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2080958

</td><td>

The indicator scorecard score date should be shown instead of the 'latest score' label

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2085934

</td><td>

AIDE **Explore** button is shown on all lists, including 'All Table Discovery' entities

</td><td>

The AIDE **Explore** button is shown on all entity lists, including entities that shouldn't have it. Only entities marked Active=true and population\_source=Table Config should display the **Explore** button. Entities with population\_source = 'All Table Discovery' \(or inactive entities\) shouldn't show the **Explore** button.

</td><td>

1.  Navigate to an entity list that is marked as 'All Table Discovery'.
2.  Check whether the **Explore** button is present.

 Expected behavior: Only entities with Active=true and population\_source=Table Config show the**Explore** button.

 Actual behavior: The**Explore** button is shown on 'All Table Discovery' entity lists.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2033980

 [KB3129184](https://hi.service-now.com/kb_view.do?sysparm_article=KB3129184)

</td><td>

Text index processing delay on analytics\_​visualization\(column=​type\)​ after upgrading to Australia

</td><td>

After upgrading to Australia, the user observes increased processing times related to text indexing events on the 'type' column of the analytics\_visualization table. This results in a backlog of index events.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2035747

 [KB3120864](https://hi.service-now.com/kb_view.do?sysparm_article=KB3120864)

</td><td>

The 'Create New' and **Duplicate** buttons in the Platform Analytics \(PA\) dashboard context menu are visible to users who don't have the pa\_admin or pa\_power\_user role

</td><td>

The user requests the ability to hide the 'Create New' and 'Duplicate' options from the PA dashboard context menu \(⋮\) for regular users without removing broader role access.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2037900

</td><td>

A new dashboard widget is created for a sub-domain

</td><td>

In a user's instance, when the list-simple dashboard widgets migrated to list widget, the corresponding dashboard widgets were duplicated and new records were created in the user domain. This isn't the expected behavior, since nothing like this happens for par\_visualization record. The list-simple to analytics list migration is a background flow that executes as a system user, so when trying to do a dashboard widget update via a background script, this reproduced the same issue. This indicates that the root cause is updating a dashboard widget record while in another domain.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2058906

</td><td>

The last viewed dashboard doesn't open when going to /​now/​platform-​analytics-​workspace/​dashboards

</td><td>

Last viewed dashboard not opening when going to /​now/​platform-​analytics-​workspace/​dashboards.​

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2071627

</td><td>

Remove text indexing on required\_translations field

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2072270

</td><td>

Widgets, Permissions, and Canvas are created in the incorrect scope when a shared non-admin user edits a dashboard originally created in an application scope and leads to deletion

</td><td>

 

</td><td>

1.  Open an instance from the latest Zurich patch as an admin.
2.  Change the application scope to 'Knowledge Overview'.
3.  Duplicate the dashboard 'Knowledge Management Overview'.
4.  Validate that records created in all dashboard tables have the application scope set to 'Knowledge Overview'.
5.  Share the duplicated dashboard to the knowledge\_admin role with edit access.
6.  Switch back to the global scope.
7.  Create a user knowledge.admin with role knowledge\_admin.
8.  Impersonate as user knowledge.admin.
9.  Open the duplicated dashboard in **Edit** mode.
10. Add a single score widget to any of the existing tabs at the bottom of the tab.
11. Save the dashboard.

 Expected behavior: The new par\_dashboard\_widget entry should have the application scope as 'Knowledge Overview'.

 Actual behavior: The new par\_dashboard\_widget entry has the application scope as 'Global'.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB2074215

 [KB3222130](https://hi.service-now.com/kb_view.do?sysparm_article=KB3222130)

</td><td>

Next Experience dashboards' domain has visibility issues

</td><td>

DomainHierarchy.isInDomain\(\) only recognized a user's own domain and parent domains. It ignored visibility grants to sibling domains.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Filters

 PRB2052543

</td><td>

Interactive dashboard filters aren't applied to workbench data visualization

</td><td>

Interactive dashboard filters are not applied in workbench filters. The flag shows that the filter is applied but underlying indicators don't honor the same filter.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2066861

</td><td>

Time series widget with widget indicator filtered by choice is migrated as a compatibility mode widget

</td><td>

 

</td><td>

1.  Create a time series PA widget on indicator 'Number of open incidents'
2.  Configure a widget indicator for the above widget also on indicator 'number of open incidents', set breakdown 'priority' on element '1 - Critical
3.  Add the above pa widget to a core UI dashboard
4.  Migrate the dashboard

 Expected behavior: The widget is migrated as a data vis \(since this configuration is supported\). This occurs in the **Choice** field but doesn't happen to **Reference** field \(for example, assignment group\)

 Actual behavior: The widget is migrated as a compatibility mode widget.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2071058

</td><td>

Drilldown works on dashboards after migration if, in the CoreUI, the second drilldown has a drilldown view but that view isn't passed to the migrated reports drilldown

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Runtime

 PRB1996636

</td><td>

An orbit dist-upgrade preserves the previous version of conf/tomcat-host.xml on node upgrades for self-hosted instances

</td><td>

The host configuration file conf/tomcat-host.xml on a ServiceNow application node isn't updated during node upgrades on self-hosted instances, as the Orbit dist-upgrade function is preserving this file from the original pre-upgrade version. This happens in the same manner glide.properties, glide.db.properties, and the contents of conf/overrides.d/ are preserved, by copying them from the existing node before the upgraded node files are copied to the original location. This is a potential issue, as the tomcat-host.xml config file is occasionally modified from time to time to fix or prevent certain issues. As the file is preserved during an upgrade on a self-hosted instance, that leaves self-hosted users running with outdated versions of tomcat-host.xml and thus vulnerable to issues.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2077447

</td><td>

Nested playbook does not auto-advance to its next stage after the first stage completes when the session is impersonating a specific user

</td><td>

No activities are loaded when stage 2 is selected.

</td><td>

1.  Create a parent playbook with at least 2 stages:
    1.  Stage 1: a regular activity \(for example, an Instructional activity\).
    2.  Stage 2: a 'Launch Nested Playbook' activity that launches a child playbook.
2.  Impersonate a user.
3.  Trigger the parent playbook against a target record \(for example, an Incident\).
4.  Complete Stage 1 of the parent playbook.

Notice that the first stage is marked complete, but the second stage does not become focused automatically.

5.  Select stage 2.

 Observe that no activities are loaded.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2086543

</td><td>

When resolving overrides for AI-experiences, the first matching overrides containing aixWidget should be returned

</td><td>

PlaybookActivityOverrideRepo .initializeByPlaybook ExperienceId\(\) only populates PlaybookActivityOverride .aixWidget from the override record's **aix\_widget.id** field. If the override record itself doesn't have an AIX widget configured, but the activity's linked activity UI record does \(activity\_ui.aix\_widget.id\), then the widget is never picked up. The override ends up with an empty/null AIX widget, so the AIX experience isn't rendered even though a widget is configured at the activity UI level.

</td><td>

1.  Create a new activity UI.
2.  Populate the **AIX widget** field.
3.  Create an activity override using the above activity UI.
4.  Add conditions so that the above override is selected at runtime.

 Observe that the **AIX widget** field isn't picked from the activity UI in override at runtime. It's returned directly from the default activity UI.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2086893

</td><td>

Happy path observability backend path evaluation and runtime state services

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2096921

</td><td>

The Playbook fails to load 'Error fetching playbook' for playbooks with 'After specific stages' once a Playbook Experience record generator has previewed them, and an NullPointerExeception \(NPE\) occurs in isOnIdealPath

</td><td>

The NullPointerException shows 'Cannot invoke ''Activity.isLaneStartActivity\(\)'' because 'activity' is null.' The PlaybookContextQuery catches it as 'Error fetching playbook', and the whole playbook response is empty, including the intake. This issue is found in Brazil instances, but works as expected in Australia because isOnIdealPath is not in that build.

</td><td>

1.  Open a thunder devsnc instance.
2.  Select Opportunities. Navigate to Grant Program 1 &gt; Apply now.
3.  Complete the 'Answer eligibility question' activity with the answer 'Yes' to all the questions.
4.  Navigate to **Next** &gt; **Start Proposal**.

Notice that in portal, after selecting **Start proposal**, the case \(GPR…\) is created but the playbook area stays blank. The message 'There are no playbooks available' occurs in the workspace.


 Expected behavior: The playbook renders with all stages and activities, as it does on Australia.

 Actual behavior: There is a blank playbook panel in portal. The message 'There are no playbooks available. Please contact your system administrator.' occurs in the workspace. An NPE occurs in the syslog: 'GraphQL API - GlideGraphQL: Exception encountered processing path: /GlidePlaybookContext\_Query/getPlaybookContextsByParentRecord - Error fetching playbook \(no cause logged\).'

</td></tr><tr><td>

Process Mining

 PRB2082020

</td><td>

When a project created in Zurich is copied to Australia, criteria between steps are not copied

</td><td>

Criteria between steps is not migrated along.

</td><td>

1.  On a Zurich instance, create a project with at least one rule based finding that has a Constraint in it \(Step 1 to Step 2 between 1 and 6 days\)
2.  Migrate instance to Australia

 Observe that Criteria between steps is not migrated along.

</td></tr><tr><td>

Process Mining Workspace

 PRB2068401

</td><td>

A Root Cause Analysis \(RCA\) fails on a child entity for all MDM projects

</td><td>

 

</td><td>

1.  Create any pair of MDM projects for the incident and problem entities, or the incident and SLA task entities.
2.  Select any eligible activity in the child entity.
3.  Run 'Key contributors RCA' from the 'Investigate' section.

 Observe that the RCA scheduled task fails for the selection. Note for the same entity without MDM setup, the RCA task is working correctly.

</td></tr><tr><td>

Process Mining Workspace

 PRB2073844

</td><td>

Breakdown percentages Oppt. Details Page is relative to full project, not finding scope

</td><td>

Hovering over breakdowns should put percentages over finding scope.

</td><td>

1.  Open a finding on the improvement opportunity details page with breakdowns.
2.  Hover over a breakdown value.

 Observe that the tooltip breakdown percentages are relative to the project scope, not finding scope.

</td></tr><tr><td>

Process Mining Workspace

 PRB2079553

</td><td>

Mining fails with an error when a filter condition is applied on a reference-field breakdown \(Assigned to / Assignment group\)

</td><td>

Mining fails with the error message: 'GlideRecord.setTableName - empty table name \(sys\_​script.​74b7dfaf6bd101104e6fe1188e44afb3.​script;​ line 9\)'.

</td><td>

1.  Navigate to Set Objectives page and start creating a new project.
2.  Set Table as Incident.
3.  Navigate to the 'Scope Your Analysis' page.
4.  Add any activity definition.
5.  Navigate to the 'Breakdowns' page and add a reference field as a breakdown — either Assigned to or Assignment group.
6.  Open the breakdown and add a filter condition on this breakdown \(for example, Active is true, Active is false, or Name contains &lt;value&gt;\).
7.  Navigate to the 'Review and Mine' page and select **Mine**.

 Expected behavior: Mining should complete successfully with the filter condition applied on the reference-field breakdown.

 Actual behavior: Mining fails with following error message, 'GlideRecord.setTableName - empty table name \(sys\_​script.​74b7dfaf6bd101104e6fe1188e44afb3.​script;​ line 9\)'.

</td></tr><tr><td>

Process Mining Workspace

 PRB2086671

</td><td>

Project created in Z, migrated to A, criteria between steps are not migrated

</td><td>

On a Zurich instance, when a project is created with at least one rule based finding that has a constraint in it, and it is then migrated to Australia, criteria between steps is not migrated along.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB2052920

</td><td>

The 'Recalculate Resource Cost' function isn't updating child assignment costs because the rate model line attribute uses a comma decimal separator

</td><td>

The 'Recalculate Resource Cost' function does not update child assignment costs because the rate model line doesn' match the group's average\_daily\_fte attribute.

</td><td>

 

</td></tr><tr><td>

Pub/Sub

 PRB2086054

</td><td>

PubSubStatusCache cold-cache query re-enters the Field Normalization/TableRotation lock cycle

</td><td>

PubSubStatusCache.loadEntry\(\) issues a plain GlideRecord.query\(\) against sys\_pubsub\_status with no engine or business rule suppression. Pub​Sub​Status​Cache.​load​Entry\(\)​'s query at PubSubStatusCache.java:49 should be hardened with gr.setWorkflow\(false\) and gr.addBeforeQueryRules\(false\). This would mean the cold-cache status lookup can no longer re-enter Field Normalization / the Clotho metrics deny list / the table-rotation chain and contend for a lock this subsystem has no functional need to touch.

</td><td>

 

</td></tr><tr><td>

ReleaseOps - Family

 PRB2030613

</td><td>

The **Promote Update Set** UI action is visible even when sn\_​releaseops.​deployment\_​controller property isn't set

</td><td>

The **Promote Update Set** UI action should be hidden when the sn\_​releaseops.​deployment\_​controller property isn't set. Currently it remains visible, which can confuse users who haven't configured ReleaseOps.

</td><td>

1.  Install ReleaseOps but don't set it up.
2.  On a complete local update, set the **Promote Update Set** button to display.

 Expected behavior: The **Promote Update Set** button doesn't display if the property is not set/empty.

 Actual behavior: When the button is selected, an error message displays: 'Error MessageDeployment controller URL is not specified. Make sure that sn\_​releaseops.​deployment\_​controller is configured in system property'.

</td></tr><tr><td>

ReleaseOps - Family

 PRB2067737

</td><td>

ReleaseOps MIF handler bypasses the Instance Scan queue

</td><td>

InstanceScanHandler.java invokes the InstanceScanWorker directly. AScanWorker worker = InstanceScanWorker. generateFromSuites AndUpdateSets \(scanSuiteIds, updateSetIds\), bypassing the instance scan queue management. It should call the CICDInstance​Scan​Execution​Service as an entry point, to take advantage of queuing and possible future changes. In Zurich, the user can only execute one scan at a time. Starting in Australia, multiple scans are allowed using the current code but there are no checks on max number of scans that can be executed and the existing code could potentially overwhelm the instance with too many scans.

</td><td>

1.  Start a full instance scan.
2.  From the ReleaseOps controller, start moving a DR that needs to do an instance scan.

 Expected behavior: The Data Replication waits but then complete successfully.

 Actual behavior: The Data Replication fails the instance scan with an error: 'Failed to get scan result: Multiple scans cannot be run at the same time'.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB2080234

</td><td>

Concurrent Remote Process Synchronization \(RPS\) can create too many sysevent records

</td><td>

When the main 'IB/OB' job runs, check to see the current queue size in sysevent. If it's greater than 2x the number of active remote systems, then log a 'WARN' message without creating any sysevent records.

</td><td>

1.  Enable concurrent RPS and ensure each the job takes time to run.
2.  Set the 'OB' job to run every 5 seconds.

 Observe that the sysevent queue creates records faster than they get processed.

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

 PRB2080238

</td><td>

An outbound Remote Process Synchronization \(RPS\) job in Concurrent RPS is inefficient when it tries to filter the 'Capture Definition' map

</td><td>

This appears to be due to some inefficient coding in Outbound​Queue​Dao.​get​Remote​System​Capture​Defs​Map.​ It gets all CDs before trying to filter them with computations and comparisons. This would be more efficient if capture​Definitions.​get​All​Capture​Definitions\(\)​ took an argument that would let users filter on a remote system before looping.

</td><td>

1.  Set up Concurrent RPS.
2.  Set up 1500 remote systems.

 See how long it takes to process a single job for a remote system without any records to process.

</td></tr><tr><td>

Reporting

 PRB2055106

</td><td>

After the Australia upgrade, there are font size issues with the CoreUI-specific time series widget

</td><td>

After the Australia upgrade, the time series widgets displays scores in a font size that is not readable in the Core UI Dashboard. The Same widget in the Yokohama displays the scores with a larger font size.

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB2056087

</td><td>

Data labels are truncated when saving a report as a PNG

</td><td>

 

</td><td>

1.  In Core UI Reporting, create a report.
    -   Table: Incident
    -   Type: Bar Chart
    -   Group By: Short Description
    -   Aggregation: Count
2.  Save/Run the report.
3.  Observe that because **Short Description** can have long strings, the X axis labels are truncated.
4.  Change system property glide.​chart.​truncate.​x\_​axis\_​labels = false.
5.  Run the report again.
6.  Observe that **Short Description** is no longer truncated.
7.  Export the chart to PNG using the context menu option **Export to PNG**.

 Expected behavior: The exported PNG looks like the chart, with the labels displayed.

 Actual behavior: The exported PNG has labels truncated.

</td></tr><tr><td>

Reporting

 PRB2067688

</td><td>

Reports shared with a user with the snc\_internal role aren't loading

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB2070251

</td><td>

RequestWorkflowStageProcessor throws ClassCastException when called from a different scope, causing Requested Item Summarization to show generic content

</td><td>

js​Function\_​get​Parent​Workflow​Choices throws ClassCastException when handed a fenced object. js​Function\_​get​All​Workflow​Choices silently returns an empty ChoiceList instead of throwing. Stages are either never populated \(crash swallowed upstream\) or silently empty, so the LLM summarization payload has no real stage data, and the 'Now Assist request summary' falls back to a generic response.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1925690

 [KB3221015](https://hi.service-now.com/kb_view.do?sysparm_article=KB3221015)

</td><td>

An influx of events are generated 'resource\_daily\_hours.changed'

</td><td>

Whenever updates are happening on the 'resource\_plan' table via any job, an influx of 'resource\_daily \_hours.changed' events are generated, and it's impacting the events processing in the default queue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Resource Management

 PRB2006227

</td><td>

Project workspace throws invalid date errors when the RA being created lies within the project timelines

</td><td>

Updating an assignment adjusts the resource plan dates. If the planned start date of a project is older than the actual start date, the planned dates are copied to the resource plan. However, the resource plan dates show the actual start date of the project. Consequently, an error is thrown stating that the resource plan is outside of the project dates.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB2064402

</td><td>

Demand is supporting creation of traditional plans even if attribute based plans \(resource assignments\) are already available for that demand

</td><td>

 

</td><td>

1.  Create a demand.
2.  Create a resource assignment for that demand.
3.  Try to create a normal traditional resource plan for that demand

 Observe that the resource plan gets created despite the presence of assignments.

</td></tr><tr><td>

REST API Framework

 PRB2078090

</td><td>

Support Linear CRUD Multiplier Model for AP6 Metering

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

REST APIs

 PRB2077005

</td><td>

Exclude machine-to-machine \(non-end-user session\) requests from CSRF violation logging

</td><td>

This logic is present on Brazil but missing on the older release\(s\), where internal M2M traffic is being incorrectly logged as CSRF violations in the localhost logs \(the ALLProcessorCSRFLogging / ALLProcessorCSRFLoggingEmpty events\). This inflates the log stream with non-actionable violation noise and makes it harder to assess true enforcement readiness on those releases.

</td><td>

 

</td></tr><tr><td>

Robust Transform Engine \(RTE\)

 PRB1750431

</td><td>

Excessive processing time spent creating JSON parsers

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Rollback and Recovery

 PRB2010841

</td><td>

Rollback is slow when the context includes updates to choice fields

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Rollback Contexts

 PRB1942654

</td><td>

'Clean Expired Rollback Contexts' job runs for an extended duration

</td><td>

The 'Clean Expired Rollback Contexts' scheduled job exhibits abnormal execution duration on a clone instance, running continuously for over six hours without completion.

</td><td>

 

</td></tr><tr><td>

Scheduled Jobs

 PRB2039076

</td><td>

Need smarter calculation of job lateness for extra worker threads

</td><td>

Extra workers will not be created until the high priority jobs are at least one minute late.

</td><td>

1.  Create sleep jobs that sleep for 1m \(can just use gs.sleep\(60000\) in script\). The number should be equal to the number of worker threads available on the instance.
2.  Create several high priority jobs with the next\_action set to 5 seconds in future \(to allow the sleep jobs to run first\).

 Observe that sleep jobs start running, hogging all worker threads. Extra workers will not be created until the high priority jobs are at least 1m late. Note that it may be worse than this - as other jobs become due, the average lateness gets brought down because the lateness of other jobs are likely lower than the jobs created.

</td></tr><tr><td>

Scheduled Jobs

 PRB2054318

</td><td>

Frequent writes to sys\_status table from worker threads

</td><td>

There are frequent updates on the Updates column when jobs are run.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization \(Glide Family Channel\)

 PRB2057489

</td><td>

SO conflict resolution is unassigning locked tasks

</td><td>

A conflict resolution fix was implemented to unassign tasks from the solution when the assignee has a conflict. However, it unassigns tasks even if they were locked after solution processing began. There should be a filter to skip the unassignment if the task has transitioned to a locked state.

</td><td>

 

</td></tr><tr><td>

Search Signals

 PRB2023083

</td><td>

GenAI log IDs aren't returned for NAVA's feedback signals

</td><td>

 

</td><td>

1.  Search in NAVA, such as 'What is spam?'.
2.  Select **Thumbs up** or **Thumbs down** on the answer.
3.  Run the background job to process queued signals.
4.  Navigate to the sys\_generative\_ai\_log table.
5.  Inspect the **Feedback** field for the transactions relevant to the Genius Result feedback was provided on.

 Expected behavior: There should be a value.

 Actual behavior: No feedback is logged.

</td></tr><tr><td>

Server-side scripts

 PRB2033318

</td><td>

Test failures when turning on interpreterV2

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB2076586

 [KB3151029](https://hi.service-now.com/kb_view.do?sysparm_article=KB3151029)

</td><td>

Plugin scripts aren't registered in some app nodes

</td><td>

On some instances, a subset of nodes can experience the mega menu in Employee Center being broken. The following error appears on the screen when navigating to Employee Center, and users are unable to use the menu: 'ErrorServer JavaScript error 'sn\_taxonomy' is not defined.'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Builder

 PRB2028753

</td><td>

UI Policies in Catalog Builder are not captured within the catalog template's scope selected

</td><td>

The 'Option' UI policy introduced in Zurich isn't obeying to consider the scope of a template for Catalog UI policies. Rather, it's picking up the scope based on an application picker. Before, the option always used the scope of template for UI policies and items belonging to that catalog irrespective of what is selected in application picker.

</td><td>

1.  Log in to an Australia instance.
2.  Navigate to Catalog Builder.
3.  Select **Create a new catalog item**.
4.  Choose a template that's scoped and has the 'Use template scope for creating record' option checked.
5.  Fill in the details.
6.  When at the 'Questions' section, choose 'Dynamic behaviors' and provide the action and its condition.
7.  Submit the catalog.
8.  Navigate to 'Maintain items'.
9.  Look for the catalog just created.

 Observe the Catalog UI policies and its actions are created under the global scope instead of the template.

</td></tr><tr><td>

Service Catalog

 PRB2084606

</td><td>

Family changes to support widgets introduced to the Service Catalog LUX Widgets Store app

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2089751

 [KB3159281](https://hi.service-now.com/kb_view.do?sysparm_article=KB3159281)

</td><td>

Catalog client scripts and UI policies are blocked on requested item \(RITM\)/sc\_task forms for users who can read the record

</td><td>

The resolver throws 'User doesn't have access to the item' and returns no catalog client scripts / UI policies, so none execute on the RITM/sc\_task form, even though the user can fully read the record. Users expect catalog client scripts and UI policies load and execute for any user who has read access to the RITM / sc\_task record. The catalog item User-Criteria entitlement \(canView\) should only gate the catalog ordering context \(sc\_cat\_item / sc\_cart\_item\), not fulfillment records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Variables

 PRB2072938

</td><td>

The 'Lists and Platform Analytics' visualization shows encrypted responses for record producer variables

</td><td>

The variables in the incident list view should show decrypted values. The issue occurs because the form and the list view retrieve the variable's value in two different ways.

</td><td>

1.  Create an encrypted field configuration on the question\_answer table and **Value** field.
2.  Define a module access policy based on the crypto module of type 'Role'.
3.  Set the target role as snc\_internal and the result as track.
4.  Create a record producer on the incident with one variable.
5.  Create an incident via the record producer.
6.  Add the record producer variable to the incident list view.
7.  Load incident.list.

 Expected behavior: The variables in the list view show decrypted values.

 Actual behavior: The variables in the list view show encrypted values.

</td></tr><tr><td>

Service Mapping

 PRB2038856

</td><td>

Add isLightweightFeatureSupported condition to the lightweight routers in service-watch

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2057825

</td><td>

The \_​should​New​Services​Be​Lightweight doesn't check if the user is in a domain separated instance

</td><td>

Currently the lightweight service creation router only takes into consideration the 'sn\_​app\_​service\_​ext.​sm.​lightweight.​by\_​default' system property.

</td><td>

1.  Provision a domain separated instance.
2.  Set the sn\_​app\_​service\_​ext.​sm.​lightweight.​by\_​default system property to true.
3.  Create a new tag-based service via the UI.

 Notice that the service has an sm\_service\_calculation\_status record.

</td></tr><tr><td>

Service Mapping

 PRB2079268

</td><td>

Add isLightweight helper and isLightweightGr JS bridge to ServiceModelingUtils

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079270

</td><td>

updateDynamicNumberOfLevels: lightweight delegation gate + metadata merge fix

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079273

</td><td>

Guard convertDynamicToManual against lightweight services

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079274

</td><td>

global.​Service​Calculation​Dispatcher Script Include

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079277

</td><td>

SMService​By​Tags​Utils.​\_​create​Or​Update​Service​From​Fields​Map lightweight hook

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079279

</td><td>

ServiceModelConversionBridge script include

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079282

</td><td>

Story 9.0 — Make the existing computation engine ignore Lightweight services

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079283

</td><td>

Recalculation gate + call-site swaps to ServiceCalculationDispatcher

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079284

</td><td>

ImpactRuleDAO, ImpactRuleHandle, ImpactManager additions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079286

</td><td>

Handle lightweight services in BusinessServiceManager.addCi

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079288

</td><td>

createDynamicService + convertManualToDynamicService lightweight hooks

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2079289

</td><td>

Entry point records cannot be deleted from sn\_sm\_scoped\_app due to cross-scope access policy

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB2081806

</td><td>

Updating the lightweight dynamic service levels via CSDM corrupts service

</td><td>

The metadata doesn't contain 'modelDisabled: true', and the service has a populator.

</td><td>

1.  Create a lightweight dynamic service via CSDM with levels=3.
2.  Navigate to the second screen in CSDM.
3.  Select the **Levels** box.
4.  Change the levels to two.

 Observe that the metadata doesn't contain 'modelDisabled: true', and that the service has a populator.

</td></tr><tr><td>

ServiceNow Otto Context Menu \(Family Release\)

 PRB2075508

</td><td>

NACM components take more time to load

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal Core Widgets

 PRB1819286

</td><td>

When updating the font-family in the EC theme, it doesn't update the font in the AI search results page

</td><td>

According to the 'Theming for AI Search in Service Portal' documentation, users can control the look and feel of AI search results. The user was attempting to update the default font family of the EC theme from Lato, Arial, sans-serif, to 'Segoe UI', sans-serif . When updating the EC theme CSS properties, this changed the font on the home page as expected, but failed to change font in the AI Search results page. Also, the faceted search widget doesn't change and was still using Lato, Arial, sans-serif.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB2075083

</td><td>

'ESC' portal AI Search placeholder text customization is no longer honored after an Australia upgrade

</td><td>

After upgrading to Australia, the custom placeholder text configured for the ESC Portal search experience is no longer displayed. Instead, the platform displays the new base instance placeholder text \('Ask AI for help or search'\), causing user-configured branding and messaging to be ignored.

</td><td>

1.  Configure a custom placeholder value for AI Search.
2.  Upgrade to Australia.
3.  Open the ESC Portal search experience.

 Expected behavior: The search component continues to honor the configured placeholder values and associated sys\_ui\_message overrides after the upgrade. User customizations are reflected in the UI.

 Actual behavior: The modified placeholder text isn't shown. The base instance placeholder text is displayed instead.

</td></tr><tr><td>

Session Management

 PRB2038268

</td><td>

Write-once session values are lost after the second node move

</td><td>

On a node move, the receiving node restores the session state from the previous node's saved record and folds it into its own baseline. Since the end-of-transaction save only persists changes relative to that baseline, values that were restored but not modified during the current session are excluded from the new node's saved record. The restore chain only reaches one hop back, so a value that was written once survives a single node move, but it's lost on the second move. Values re-written every hop survive because they always appear as a change relative to the baseline. Write-once values \(for example, session properties and client data\) are lost after the second node move.

</td><td>

1.  Authenticate through GIG.
2.  Set a write-once session property \(a value not updated after the initial write\).
3.  Force a GIG rebalance \(node A to node B\).
4.  Verify that the property is present.
5.  Force a second GIG rebalance \(node B back to node A, or to a third node\).

 Observe that the property is now null/missing.

</td></tr><tr><td>

Session Management

 PRB2077746

</td><td>

In GIG, the JSESSIONID-to-node affinity is only learned from request cookies, never from response Set-Cookie, and snc\_session\_affinity\_node is set to 'Secure-only', which breaks stickiness for fresh sessions over plain HTTP

</td><td>

GIG's session affinity for a brand-new session depends entirely on the client echoing GIG's own snc\_session\_affinity\_node cookie. GIG never learns the JSESSIONID-to-node mapping from the response that carries Set-Cookie: JSESSIONID. Additionally, snc\_session\_affinity\_node is always emitted with the secure attribute, and the plain HTTP standard cookie stores it and never sends it back. As a result, it does not echo the affinity cookie, and gets every follow-up request load-balanced, including requests that already carry a valid JSESSIONID.

</td><td>

 

</td></tr><tr><td>

Software Asset Core Company

 PRB2005158

</td><td>

Improve NDS guided setup and proactively fix core company reference jobs by batching through local implementation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2051961

</td><td>

The Software Asset Management \(SAM\) Pro 'Remove Installs For Retired/Stolen CI' business rule throws 'Unknown table: samp\_citrix\_machine' when a Citrix add-on isn't installed

</td><td>

The Core SAM Pro \(com.snc.samp\) base instance Business Rule 'Remove Installs For Retired/Stolen CI' throws an unhandled 'Unknown table: 'samp\_citrix\_machine'' exception on any instance that has core SAM Pro installed but does not have the separate, optional, for-fee add-on plugin 'Software Asset Management Professional for Citrix'.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2080316

</td><td>

Generate a summary for the 'New Reclamation Candidates' job

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2082202

</td><td>

Convert 'User with elevated privileges' apps to admin \(SAM\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2100419

</td><td>

app sn\_audit\_response fails to upgrade to true-up version 2.0.6 due to a scope ID mismatch

</td><td>

2.0.6 declares a dependency on a scope called sn\_audit\_workspace. That scope can't be resolved on this instance because the Audit Workspace app is registered under the scope sn\_audit\_ws. The whole app load aborted, and sn\_audit\_response stayed on 2.0.1.

</td><td>

 

</td></tr><tr><td>

Software Asset Normalization

 PRB1703274

</td><td>

Slow queries identified during OKR 2.3 executions on reconciliation, de-duplication and normalization scenarios

</td><td>

During executions, certain slow queries take a total of at least 1 minute in the case of normalization.

</td><td>

1.  Have a discovery model \(DM\) \(cmdb\_sam\_sw\_discovery\_model\) with a non-empty **Publisher** field and a display\_name that matches an existing samp\_package\_map rule created for the publisher-less \(Add-Remove / Windows registry\) hash.
2.  Run NormalizationEngine. normalize​Discovery​Model​Record\(\)​ on that DM.

 Expected behavior: The DM with a non-empty discovered publisher shouldn't match Add-Remove rules. The status should remain 'missed' \(no match found\).

 Actual behavior: The engine falls back to the Add-Remove scenario \(blanks out the publisher\) in \_findAMatch\(\) and incorrectly matches a normalization rule intended only for publisher-less registry entries. The DM is incorrectly normalized against the wrong rule, leading to inflated/duplicate license counts for browser-hosted components \(PWAs, browser extensions\).

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2005145

</td><td>

Few software installations records have 'Install Requiring action' with the reason as 'Undetermined' for Esxi

</td><td>

During Software Asset Management \(SAM\) reconciliation, when a vCenter has a device allocation to an entitlement, the system discovers all ESXi hosts under that vCenter by traversing the CMDB relationship chain: vCenter → Datacenter → Cluster → ESXi Host. It then collects all installs from these hosts and licenses them using the allocated rights. When iterating over multiple clusters within a data center, the list of discovered ESXi hosts is overwritten on each cluster iteration instead of being accumulated. This causes only the hosts from the last-processed cluster per datacenter to be retained — hosts from all earlier clusters are silently dropped and never considered for licensing.

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2060697

</td><td>

Potential savings display incorrectly on the License Metric Result of a product for which a low usage reclamation candidate is created

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2074587

</td><td>

Reclamation code changes for app-itam-sam

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2084351

</td><td>

Domain separation doesn't work on the summary and entity table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2086017

</td><td>

Create a new AI Agent for AI Worker \(app-itam-sam\)

</td><td>

A new AI Agent should be created for the AI Worker. The implementation should follow the same pattern as the existing AI Agent. The user handover stages must be specific to the AI Worker autonomous flow.

</td><td>

 

</td></tr><tr><td>

Software Lifecycles

 PRB2002670

</td><td>

The 'Software Lifecycle Report' job fails when a child product in 'Software Product Parent-Child Relationships' isn't installed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB2001155

 [KB3151101](https://hi.service-now.com/kb_view.do?sysparm_article=KB3151101)

</td><td>

When Kafka generates many errors, processing those errors can produce Mutex contention

</td><td>

Stream Connect producers stop sending to Hermes Kafka. It publishes block for around 60 seconds and then fails, so the worker/scheduler threads back up, business rules run slow, and APIs become slow. Failed messages accumulate in the sys\_kafka\_undelivered\_messages table, and the base instance Kafka Producer Retry Job gets stuck and can't drain them.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Stream Connect Core

 PRB2079908

</td><td>

After upgrading from Zurich to Australia, the active Kafka Subscriptions are updated to REFRESHING status

</td><td>

Topic alias records are created for the Hermes topics after the upgrade, but for a few of the Kafka Subscriptions \(in the sys\_kafka\_subscription table\), the topic alias column shows empty and the status is 'REFRESHING'.

</td><td>

 

</td></tr><tr><td>

Subscription Management

 PRB2072670

</td><td>

Add sn\_entitlement scope in Glide properties to enable sending data from Glide to valk-gateway service

</td><td>

To send the metered usage data from the user and central instance to valk gateway via REST API, the valk gateway URL is accessed, which gets populated in the sys\_service table via DISH. To do so, a scope should be added in glide.properties glide.services. rest.allowed\_services to allow sys\_service to be accessed from sn\_entitlement and sn\_entitlement\_ctr scopes.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2003586

</td><td>

DB CPU spike caused by inefficient Flow Engine SLA breach event queries scanning all sysevent partitions under high load

</td><td>

During a combined load test generating 14,000 incidents/hr \(7k/hr via Event Management + 7k/hr via ITSM SOW\), the DB host CPU spiked sharply to 76% at approximately 00:30–00:45 UTC on 2026-03-17. The spike is correlated with a high-frequency, slow-executing SQL query scanning all sysevent partition tables \(sysevent0000–sysevent0006\) via a 7-way 'UNION ALL', issued by the Flow Engine's MonitorOperation while polling for SLA breach flow events.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2080045

</td><td>

Post-clone event-processing cleanup scripts \(201-204\) fail to run when a user script ahead of them errors out

</td><td>

The post-clone cleanup scripts Delete Processing Framework Triggers \(201\), Deduplicate Queues Post Clone \(202\), Deduplicate Queue Params Post Clone \(203\), and Re Provision Queues Post Clone \(204\) are failing to run. This occurs when a cleanup script at a lower order value errors during the clone. Since the clone cleanup runner stops entirely on the first failure, scripts 201-204 never execute. Event queues are left unprovisioned, backing up hundreds of thousands of events until the missing scripts are run manually via emergency change.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2080453

</td><td>

NowMQ events never get delegated on Worker.Default nodes due to a broken participation check

</td><td>

 

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB1946880

</td><td>

StreamConnect RTE Consumer misses messages when there are two consumers per node

</td><td>

When consuming messages using StreamConnect RTE consumer all the messages are not getting processed and some of the messages are getting dropped.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2037370

</td><td>

Reading of multiple records using the UI/API Call/Processor/Script/Flow fails to track multiple READs in the Record Action metric

</td><td>

Four GlideRecord operation methods are instrumented to call RecordActionRecorder.record\(\) at the point of each operation. This is the entry point for all telemetry, and every record operation on an allowlisted table flows through here. The instrumentation pattern follows Glide​Record​Protected​Data​Recorder,​ which already instruments the same methods: a single static call, no branching, no impact on the existing operation path. query\(\) is added for READ instrumentation so that data access by external agents and the NOW UI can be measured alongside writes.

</td><td>

1.  Navigate to the incident table.
2.  View the list of incidents in the ServiceNow UI.

Observe that all of the rows are visible in the UI with multiple read metrics.

3.  Execute a Query Service Query to validate that multiple metrics have been recorded in the 'sn.​glide.​action\_​fabric.​record\_​action' metric.

 Expected behavior: Multiple reads are recorded.

 Actual behavior: One read is recorded.

</td></tr><tr><td>

System Web Services

 PRB2088206

</td><td>

Platform Security changes for October GA

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2088208

</td><td>

Support Linear CRUD Multiplier Model for AP7 Metering \(GAIC Decimal Support\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Table Rotation

 PRB1954428

 [KB2590667](https://hi.service-now.com/kb_view.do?sysparm_article=KB2590667)

</td><td>

Table rotation creates too many 'Online Alter Truncate Delayed Drop Table' entires in sys\_trigger to be executed in a short span of time

</td><td>

The syslog and extended tables are supposed to be rotated weekly, which means it switches to the next rotation in the schedule and also truncates future rotation to make it available for the next week.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Time Card Management

 PRB2081643

</td><td>

Fields aren't visible on time\_sheet.do form for timecard\_user

</td><td>

Users with the timecard\_user role can't see fields on the time\_sheet.do form, preventing timesheet creation.

</td><td>

1.  Impersonate a user with the timecard\_user role.
2.  Navigate to time\_sheet.do.

 Expected behavior:**Form** fields are visible for timesheet entry.

 Actual behavior: The form loads with no fields visible.

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2081553

</td><td>

Convert app-domain-util app as a hosted plugin

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Trace Collector - Family Release

 PRB2090151

</td><td>

Netty 1.2.10 is at end-of-life

</td><td>

As recommended, upgrade Netty to 1.2.17 or newer.

</td><td>

 

</td></tr><tr><td>

Transaction Logs

 PRB2073987

</td><td>

Enable MCP server user-facing logging via the sys\_log table

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB2036507

</td><td>

Hopped-in users are logged out every 5 minutes because glide.guest.session\_timeout = 5 minutes

</td><td>

This happens because hopped-in users follow the glide.guest.session\_timeout property.

</td><td>

1.  Navigate to an instance.
2.  Change the property 'glide.guest.session\_timeout' = 5.
3.  Log out and hop in again.
4.  Navigate to /xmlstats.do?include=sessions.
5.  Look up the hopped-in user name.

 Notice inactive.timeout is set to the value of the 'glide.guest.session\_timeout' property.

</td></tr><tr><td>

UI Actions

 PRB2074979

</td><td>

GraphQL list UI actions are pulling UI actions that are list V3 compatible

</td><td>

The graphQL endpoint is pulling list UI actions that are list v3 compatible, thus creating duplicate list UI actions in the choice menu.

</td><td>

1.  Enable the 'Lit' list component to fetch UI actions for the 'Incident' table.
2.  Open the choice/menu of actions in the top right corner of the list.

 Note the duplicated list UI actions such as **Repair SLAs,** &gt; **Add to Visual Task Board**, and so on.

</td></tr><tr><td>

UI Actions

 PRB2084589

</td><td>

Handle session notifications when a page redirect occurs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB2084591

</td><td>

UI action condition evaluation should leverage virtual URIs for improved parity

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB2084593

</td><td>

Correct the behavior of server-side UI actions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Actions

 PRB2084596

</td><td>

Support handling of redirect-based processors

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB2082758

</td><td>

Advanced Qualifier Reference is skipped when doing a list edit operation for a reference field

</td><td>

Note that Advanced Qualifier Reference is working fine on a form.

</td><td>

1.  On an incident table, set up advanced reference qualifier for the **Assigned to** field.
2.  On Service Operations Workspace, navigate to the 'Incident' list.
3.  Try to list edit the **Assigned to** field.
4.  Select the **Look up** icon.

 Expected behavior: The Advanced Qualifier Reference should be applied.

 Actual behavior: The Advanced Qualifier Reference is skipped.

</td></tr><tr><td>

UI Form Administration

 PRB2084578

</td><td>

Glide changes to support form URL parameters and formatter support in UI26

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB2084598

</td><td>

Glide changes to support the form context menu and system parameters in UI26

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

User Criteria for Service Catalog

 PRB2087796

</td><td>

Scripted user criteria might return stale results via AI Search and aren't cached durably for the Moveworks Search API

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2003269

</td><td>

The 'Wrap up' modal doesn't display when users close the 'Interaction' tab and they reopen/reload it again

</td><td>

When the interaction tab is closed via SPA navigation, the wrapUp dialog element is destroyed but the entry in window.​ux\_​globals.​\_​\_​window​Manager​Config.​dialogs was never cleared. When the agent reopened the interaction from the list, the stale entry causes the create dispatch to be skipped — leaving the window manager with a detached content reference, resulting in 'No content available'.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2014549

</td><td>

getScreen is invoked twice, causing duplicate calls to the server

</td><td>

 

</td><td>

1.  Open any instance on Australia or Brazil.
2.  Open SOW workspace.
3.  Perform a hard reload.
4.  Open DevTools - Network Tab.
5.  Select the **ServiceNow Logo** present on the unified navigation bar on the top left.

Observe that the user is routed to /now/nav/ui/home.


 Expected behavior: Only one hydrate call is made.

 Actual behavior: Two hydrate calls are made.

</td></tr><tr><td>

UX Framework

 PRB2018022

</td><td>

Transaction​Additional​Info​Collector.​log​And​Remove​Instance\(\)​ is not exception-safe, causing ThreadLocal state pollution across unit tests

</td><td>

Transaction​Additional​Info​Collector.​log​And​Remove​Instance\(\)​ does not wrap its logging call in a try-finally block.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2024860

</td><td>

getInstanceValue caches are undefined and portal app shell search navigation is broken

</td><td>

The user should be navigated to the selected article and the URL should change to the article record. Instead, nothing happens.

</td><td>

1.  Navigate to the landing page.
2.  Select the search box in the top-right corner of the browser header.
3.  Type 'remo'.
4.  Select any of the suggested articles in the type-ahead list \(or press Enter\).

 Expected behavior: The user is navigated to the selected article. The URL changes to the article record.

 Actual behavior: Nothing happens. There's no navigation, error, or result list.

</td></tr><tr><td>

UX Framework

 PRB2033497

</td><td>

Next Experience app shell header remains dirty after form save when events dispatched via Controller

</td><td>

When a controller \(for example, a scripted controller, Refresh List Controller, or Lookup Record controller\) dispatches Update Form Value and Save Form events — either directly on select or via an on execution completed / on data succeeded handler — the Polaris app shell header fails to clear its dirty state even though the form values are correctly saved and the form reloads showing no unsaved changes.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2057267

</td><td>

The session expiry modal displays inside the workspace iFrame

</td><td>

 

</td><td>

1.  Navigate to the Service Operations Workspace \(SOW\) list page.
2.  Open a tab and do logout.do.
3.  Navigate back to the SOW list page and wait for the session expiry modal to show.

 Expected behavior: Session expiry handling should show the session expiry modal.

 Actual behavior: The session expiry modal shows up inside the iFrame.

</td></tr><tr><td>

UX Framework

 PRB2061413

</td><td>

Memory leak in builder tabs \(Table Builder, Playbook\)

</td><td>

Opening builder tabs \(Table Builder, Playbook, Flow Designer\) in ServiceNow Studio \(Glider SNS\) and closing them does not reclaim heap memory in the Australia family. Memory after tab close + GC remains at peak level and never returns to baseline. The same steps on the Zurich family produce no leak — memory returns to baseline cleanly.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2084577

</td><td>

Product lab and action triggers in Survey Center

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Versatile Node and Cluster Configuration

 PRB2080145

</td><td>

GIG ports can reorder glide nodes and select the wrong default database

</td><td>

Multi-node Glide ITs can select a different default Glide node when GIG is enabled. GlideNodeScanner sorts nodes using GlideNode.getPort\(\), but getPort\(\) intentionally returns the effective ingress port. Because GIG ports are allocated independently, enabling GIG can reverse node order even though the Glide topology is unchanged. This caused Virtual​Agent​Timeout​Conversations​IT on track/tsmgmtalpha to open the second isolated database through GIG, while AC\_UpdateSetIT had activated the Virtual Agent public-page records only in the first database. The browser received 302 /session\_timeout.do and stalled waiting for VA initialization.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2005164

</td><td>

Dynamic Translation in Virtual Agent is translating already translated text in catalog items

</td><td>

Dynamic Translation is translating already translated catalog item text in the Virtual Agent, causing unexpected phrasing for text that users have specifically set for a specific language.

</td><td>

1.  Create a conversational catalog item.
2.  Define a translation for one of the questions in another language via the 'Translated Text' table.
3.  Open the catalog item via Virtual Agent.

 Notice that once the question translated is presented, the exact phrasing used in the Translated Text isn't presented. This is due to the Dynamic Translation translating an already translated question.

</td></tr><tr><td>

Virtual Agent

 PRB2051719

</td><td>

Executing the topic from \_na\_max\_wait\_time\_ fails with an exception when transferred chat times out

</td><td>

An error message occurs and an exception appears in the logs.

</td><td>

1.  In Enhanced Chat, transfer to a live agent.
2.  As another agent user, accept the chat.
3.  Transfer the chat to another queue using the /tq quick action.
4.  Do not accept the chat and allow max wait time topic to trigger.
5.  When prompted, select the topic.

 Expected behavior: The topic executes successfully.

 Actual behavior: The message, 'I'm having technical issues and won't be able to continue this conversation' is shown and an exception is in the logs.

</td></tr><tr><td>

Virtual Agent

 PRB2066110

</td><td>

When ending the conversation, it moves the interaction to a 'Closed Abandoned' state without starting the conversation after creating it using CREATE\_CONVERSATION

</td><td>

The interaction moves to a 'Closed Abandoned' state instead of a 'Closed Complete' state.

</td><td>

1.  Create a conversation using the CREATE\_CONVERSATION action.
2.  Pass the context variables live\_agent only to 'true'.
3.  End the conversation using the END\_CONVERSATION action without starting the conversation

 Expected behavior: The interaction must move to 'Closed Complete' state.

 Actual behavior: It is moving to a 'Closed Abandoned' state.

</td></tr><tr><td>

Virtual Agent

 PRB2066112

</td><td>

UPDATE\_CONTEXT\_VARS is not working when used immediately after CREATE\_CONVERSATION

</td><td>

An error is thrown, and context variables must be updated with out any errors.

</td><td>

1.  Create a conversation using the CREATE\_CONVERSATION action.
2.  Try updating context variables using UPDATE\_CONTEXT\_VARS immediately after the creating conversation.

 Notice that it is throwing error.

</td></tr><tr><td>

Virtual Agent

 PRB2068417

</td><td>

When Dynamic Translation \(DT\) is turned on, it causes incorrect translations with markdown link syntax

</td><td>

Dynamic Translation \(DT\) breaks markdown links and images in Virtual Agent messages when translating to languages that use non-ASCII punctuation \(for example, Chinese, Japanese, Korean\). DT converts all ASCII punctuation to localized equivalents during translation. For example, in Chinese, parentheses \(\) become full-width （）. This is correct for plain text, but DT does not distinguish plain text from markdown syntax.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2069651

</td><td>

The client hangs without feedback when exceptions are thrown in the OGCS layer during topic callback processing

</td><td>

Different exceptions throughout the flow must be caught and a feedback message has to be sent to client so that the client doesn't hang.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2069708

</td><td>

Users don't see logged in user details passed for DARE in skuld

</td><td>

 

</td><td>

From the Now Assist Portal, ask a simple question such as 'Who am I?'.

 Observe that it produces incorrect results and it doesn't pass user context.

</td></tr><tr><td>

Virtual Agent

 PRB2070336

</td><td>

A guest user isn't able to upload images

</td><td>

Two issues prevent a guest user from uploading images: the conversation-server returns a 500 error due to a table level ACL on sys\_cs\_conversation and conversation-server returns a 401 error: 'unable to find guest session - Guest cookies are not passed through to upload request'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2073794

</td><td>

Pre-chat survey doesn't start and complete as expected

</td><td>

 

</td><td>

1.  Navigate to https:​/​/​&lt;instance&gt;​.​service-​now.​com/​csp as a guest user.
2.  Open DW chat.

 Observe that the flow doesn't start and complete as expected. With the enhanced chat experience, the flow triggers correctly.

</td></tr><tr><td>

Virtual Agent

 PRB2074992

</td><td>

Handshake fails when duplicate preferred-skill entries exist for the same skill

</td><td>

An error message occurs and an exception is found in the logs.

</td><td>

1.  In enhanced chat, transfer to a live agent.
2.  As another agent user, accept the chat.
3.  Transfer the chat to another queue using the /tq quick action.
4.  Do not accept the chat and allow max wait time topic to trigger.
5.  When prompted, select the topic.

 Expected behavior: The topic executes successfully.

 Actual behavior: The message, 'I'm having technical issues and won't be able to continue this conversation' is shown and an exception is in the logs.

</td></tr><tr><td>

Virtual Agent

 PRB2076214

</td><td>

A java.lang.NullPointerException occurs, 'Cannot invoke 'com.​glide.​script.​Glide​Record.​set​Value\(String,​ Object\)' because 'gr' is null'

</td><td>

This issue was observed while investigating a ZTSD issue.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2076609

</td><td>

The 'Timeout conversations' job fails to close conversations on cross domains

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2078678

</td><td>

The dynamic loading 'Processing new information' progress message is not translated in localized Now Assist Virtual Agent \(NAVA\) conversations

</td><td>

Even though the values are translated in Spanish when the user opens 'Testing \(En pruebas\)' in the AI Agent Studio \(Estudio de agentes de IA\), the message 'Processing new information' remains in English and is not translated to Spanish.

</td><td>

1.  Set up Dynamic Translation.
2.  Change the language to Spanish.
3.  Navigate to **AI Agent Studio \(Estudio de agentes de IA\)** &gt; **Testing \(En pruebas\)**.
4.  Observe the following values that are translated:
    -   Choose a test type AI agent or workflow \(Elegir un tipo de prueba\): Agente de IA o Flujo de trabajo
    -   Name of the AI Agent or agentic workflow \(Nombre del agente de IA o flujo de trabajo agéntico\): Agente de IA de categorizar incidentes de ITSM
    -   Version: 1 - V1 \(activo\)
    -   Task: INC0009009
5.  Select **Continuar para probar la respuesta del chat**.
6.  Watch the dynamic loading messages.

 Expected behavior: The user sees 'Processing new information' translated in Spanish, 'Procesando nueva información'.

 Actual behavior: The English text 'Processing new information' displays and is not translated to Spanish.

</td></tr><tr><td>

Virtual Agent

 PRB2078683

</td><td>

The Topic execution is not working if the Nextwave user is in the TOP/Default scope

</td><td>

 

</td><td>

1.  Enable domain separation.
2.  Check the Nextwave service user domain.
3.  Make any update on the user if needed so that the domain gets changed to TOP/Default.
4.  Start a conversation and run a topic.

 Observe that it fails.

</td></tr><tr><td>

Virtual Agent

 PRB2079671

</td><td>

The 'Expire Guest Session Identifier' scheduled job deactivates sys\_cs\_consumer records after the user either manually links or auto-link their Teams account to ServiceNow

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2081066

</td><td>

The page-not-found issue occurs with all apps and instances

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2084118

</td><td>

setCache is not honoring domain field

</td><td>

setCache is not honoring the domain field when impersonating the actual user.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2085859

</td><td>

The Prompt Library 'Topics' tab is empty because the visible skills API returns '404' for every deployment

</td><td>

When the Prompt Library is enabled on a Now Assist Panel deployment, the 'Topics' tab doesn't load any prompts. The other Prompt Library tabs are unaffected. Users expect that the 'Topics' tab lists the topics configured and marked visible for that deployment. However, the tab displays no content. The API that supplies visible skills for a deployment reports that no skills were found, even when topics and skills are configured and marked visible. Thus, the 'Topics' tab can't be used on any deployment, and there's no configuration change that corrects it.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2091490

</td><td>

Glide to OGCS requests should set X-Instance-URL header with canonical URL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2092748

</td><td>

Live agent availability doesn't work once the user selects the **Cancel** button

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2093503

</td><td>

Add support for Glide signals in Nextwave

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2095603

</td><td>

getChannelById method mapping missing in glide-plugin-members.xml

</td><td>

getChannelById calls from NW channels are failing.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2077685

</td><td>

Conversations are created in the user's default domain instead of the one they are working in

</td><td>

On an instance with domain separation enabled, starting a Now Assist conversation creates it in the user's default domain rather than the domain they are currently working in. A user who switches domains and starts a conversation can have it created against the wrong domain. Work done in that conversation then runs with the visibility of the wrong domain. This affects Now Assist across the Service Portal, the Unified Navigation panel, and the Agent workspace. Instances without domain separation are unaffected.

</td><td>

1.  Open an instance with the domain separation plugin installed for the workstream.
2.  Ensure the domain hierarchy has at least a parent and one child domain, and a user with domain picker access.
3.  Sign in and confirm the domain picker is available.
4.  Switch to a non-default domain.
5.  Open Now Assist.
6.  Start a new conversation
7.  Inspect the domain the conversation record was created in.

 Expected behavior: The correct domain is selected.

 Actual behavior: The user's default domain is selected.

</td></tr><tr><td>

Window Manager

 PRB2071474

</td><td>

Pin/Unpin doesn't work when Now Assist chat is in auto-triggered in fullscreen mode \(13' / short-viewport displays\) and in the 'Enter' modal

</td><td>

 

</td><td>

Open the chat in full screen mode.

 In full screen mode, the pin/unpin doesn't work and won't dock the chat. When the 'Enter' modal and pinned, it goes back to full screen mode instead of docking the chat.

</td></tr><tr><td>

Window Manager

 PRB2085808

</td><td>

Docking a window manager window \(Otto\) misbehaves or throws after a Polaris menu pin, due to body class/dock id desync

</td><td>

handlePolarisMenuPinned was introduced to let the bottom toolbar know when a Polaris menu occupies the left/right dock slot. It updates windowsState directly but never dispatches UPDATE\_BODY\_CLASS\_NAMES like every other dock-changing path does, so document.body's dockLeft/dockRight class can drift out of sync with the actual dock ID.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB2066296

 [KB3159814](https://hi.service-now.com/kb_view.do?sysparm_article=KB3159814)

</td><td>

wm\_agent and wm\_admin are unable to create a part requirement from a module

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Work Order Management

 PRB2084523

</td><td>

The work order rollup fails because the agent doesn't close the sn\_doc\_task

</td><td>

FSMMobileUtil.isWorkordertasksClosed \(com.snc.work\_management\) passes the work order's GlideRecord object directly into the GlideAggregate parent query instead of its sys\_id. This causes the open-task check to evaluate as 'No open tasks' and lets the 'Preview' button create a doc task prematurely. The doc task is left open and blocks the work order rollup.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included in Australia Patch 7

These prior versions contain PRB fixes that are also included with Australia Patch 7. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 6 Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-6-hf-1-PO.md)
-   [Australia Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-6.md)
-   [Australia Patch 5a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3156989)
-   [Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-5.md)
-   [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4.md)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-3.md)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

## Store app versions included in Australia Patch 7m

<table id="table_prv_2qn_ykc"><thead><tr><th>

App name

</th><th>

Version number

</th><th>

Release notes

</th></tr></thead><tbody><tr><td>

@servicenow/sn-ai-engagement-experience

</td><td>

3.7.2

</td><td>

New

 Configurable action buttons in the 'Ready for Review' state that enable Business Units to define context-specific next steps instead of a generic 'Post It' button.

 Fixed

 -   UI Actions created from AI Agent Studio are no longer set with protection policy = protected.
-   AIEX endpoints are now accessible to snc\_external and snc\_internal users.
-   Engagement Experience now displays the actual prompt text instead of the 'New message' placeholder.
-   The ServiceNow Otto panel opens according to the user's preference.
-   The IPE Feedback/State Filter popover panel aligns correctly on UI16.

 Removed

</td></tr><tr><td>

@servicenow/sn-enhanced-content-editor

</td><td>

32.7.5

</td><td>

Fixed: tooltip content not translated.

</td></tr><tr><td>

Administration for Security Exposure Management

</td><td>

30.7.1

</td><td>

Fixed

 For large environments processing high volumes of EPSS score updates, improved the NVD synchronization performance and reduced sync run times.

</td></tr><tr><td>

Advanced Approval Management

</td><td>

2.7.0

</td><td>

Fixed defects.

</td></tr><tr><td>

AES Application Object Templates

</td><td>

30.1.2

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

AES Application Object Wizard Components

</td><td>

30.1.2

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

AI Admin Center

</td><td>

6.1.6

</td><td>

New features.

 -   First release of AI Admin Center using the next generation Lux application experience and design system.
-   Instance health creates a consolidated view of AI plug-in installation and health tracking with integration back into Application Manager.
-   Upgrade planning analyzes your current instance against a targeted upgrade version allowing you to see what may be changed or impacted during the upgrade process. It covers areas such as new and deprecated features, impacts to customizations, and application compatibility changes all from one place.
-   Intent management enables creation and association of your AI agents to intents for better traceability, reporting, and case management.
-   System property registry provides an admin-facing view into AI related system properties, their descriptions, and current value. It enables transparency and better self-discovery of current config settings impacting AI on the instance.
-   Assist consumption analytics allows you to track and manage your AI usage. It supports views by asset type, usage bands, and user-attributed department.
-   Self-service troubleshooting conversational experience, including issue classification, diagnosis, and recommended remediation for core AI admin use cases.

 Other.

 -   Minor enhancements to existing capabilities related to AI Agent Advisor and settings.
-   Minor defect fixes.

</td></tr><tr><td>

AI Admin Hub

</td><td>

10.4.5

</td><td>

-   One Step Skill Activation for Out of the Box Skills.
-   Model Provider Selection Enhancements \(version lifecycle management, impact summary, version status tracking, change history, improved role based access\).
-   Notification alerts for model versions.
-   Defect fixes.

</td></tr><tr><td>

AI Agent Advisor

</td><td>

1.5.0

</td><td>

New: New frontend design for LitJS/LUX, ServiceNow's new AI UX experience.

 Changed: Automation Discovery now runs at the start of every pipeline execution instead of on a weekly schedule, so newly created or installed agents/tools are available for matching immediately. - Existing Automations table performance improved via server-side pagination. - Execution summary now includes execution IDs \(sys\_trigger / syslog\_transaction\) for easier troubleshooting. - Intent Library entries now name the intent as the user's request rather than a generic topic \(e.g., 'gift card refund' → 'request gift card refund'\). - Added support for new models.

 Fixed: Existing Automations table no longer omits installed tools that were matched during opportunity analysis. - Scheduled pipeline jobs that are interrupted \(transaction killed/aborted\) now resume automatically instead of failing with 'another execution is in progress.' - Custom Table ACL checks are now idempotent, preventing the repeated security-cache flushes a customer case flagged.

 Removed: Nothing removed in this release.

</td></tr><tr><td>

AI Agents for AIOps

</td><td>

1.13.3

</td><td>

New

 Model naming conventions updated - AI model references now follow the latest ServiceNow naming standards, improving consistency across the Autonomous Operator workflow.

 Fixed

 -   Closed a gap that allowed authenticated internal users to trigger the AMR-filter sync job without an independently verifiable role gate.
-   Resolved an issue where authenticated internal users could read AI worker, alert-rule, and agent-config state without the intended role.
-   Fixed a failure in the autonomous workflow availability check when the Workforce module \(and ZTSD\) is not installed.
-   AIOps Specialist now runs on DARE \(Data Access and Resilience Engine\), improving data handling compliance.
-   Fixed a cross-scope access error on setWorkflow when the watchdog clears stuck em\_gai/em\_alert records.
-   Alert Insights no longer incorrectly reports an alert as closed when auto-close is disabled.
-   Corrected the 'insignificant flow' logic for critical/major percentage thresholds.

</td></tr><tr><td>

AI Agents for Customer Success Management

</td><td>

2.7.22

</td><td>

Security fixes are released as Multiple root Virtual Agent topics with no role restriction, letting any authenticated user read or write arbitrary meeting, risk, touchpoint and email draft records.

</td></tr><tr><td>

AI Agents for Enterprise

</td><td>

1.1.0

</td><td>

The new Gemma model is now supported for the Now LLM Provider for the Model Category and Model Classification Skills.

</td></tr><tr><td>

AI Agents for Health and Safety

</td><td>

1.4.3

</td><td>

New

 Health and Safety users with both legacy Pro Plus and AI-Native SKUs can access AI agentic workflows. The entitlement check recognizes AI-Native subscriptions, enabling access to Health and Safety incident summarization and related agentic features for eligible accounts.

 Fixed

 The Health and Safety agentic workflow triggers correctly after an incident is assigned to a user.

</td></tr><tr><td>

AI Agents for Health Log Analytics

</td><td>

2.7.2

</td><td>

Changed

 Internal naming conventions have been updated for improved consistency across the product.

</td></tr><tr><td>

AI Agents for HR Service Delivery

</td><td>

7.4.3

</td><td>

New

 HR L1 AI Specialist can now predict and transfer HR cases based on high-confidence AI and LLM predictions. Cases are automatically transferred to the predicted HR Service when confidence exceeds the threshold, and worknotes are updated with recommendations. If confidence is low, the specialist continues resolution and logs recommendations.

 Admins can configure automatic case transfer and prediction thresholds. The 'Classify and Assign' section now allows configuration of fields to predict and the confidence threshold for automatic transfer.

 HR L1 AI Specialist uses indexed sources for service prediction. Predictions leverage both HR Cases and HR Service as indexed sources, improving accuracy and coverage.

 LLM prompt-based prediction is now supported. The system implements LLM prompts for skill-based and script-based predictions, enhancing the AI Specialist's ability to recommend services.

 Search Application for HR AIS Search Config is available. HR L1 AI Specialists can test search sources on HR Service and HR Case, ensuring accurate configuration and results.

 Unified Feature Flag Rollout Strategy enables controlled activation of AI Specialist features. Admins can manage feature availability for HR L1 AI Specialist and its template, with sandbox testing and sequencing for customer rollout.

 Golden data evaluation for prediction and transfer is established. Prediction accuracy is measured using curated datasets, with ongoing evaluation and tuning for best results.

 Model proxy for Azure OpenAI endpoints is implemented for evals. The eval suite now supports a local proxy for Azure OpenAI, enabling tool\_calls and matrix-based client/model selection without direct Azure access.

 Automation of Zero Touch Service Desk \(ZTSD\) functional flow is introduced. The ZTSD workflow is now automated, streamlining case handling.

 Changed

 Prediction prompts and logic have been fine-tuned for clarity and accuracy. Users experience improved guidance and outcomes from prediction features, with enhanced prompt generation and evaluation logic.

 Transfer flow is modularized and worknotes are updated with AI fields. After transfer, the ZTSD flow stops on the current case, and worknotes reflect AI-driven updates.

 Classify and Assign UI and configurations have been revisited and aligned with ITSM templates. Unused UI variables are removed, writeRoles and readRoles are updated for relevant configurations, and dropdowns now restrict selection to HR Service only. The autosubmitcatalog configuration is implemented, and automaticcasetransfer defaults to false.

 Testing environments for DARE and predict/transfer functionality are validated. Test results are available for both DARE and prediction/transfer workflows.

 Fixed

 Predict Services and Transfer HR Case workflow has been corrected to no longer prompt users for sys\_id input when the HR Case number is already provided.

</td></tr><tr><td>

AI Agents for ITAM

</td><td>

5.1.0

</td><td>

-   Mixed AI Native SKU scenarios now work reliably, eliminating previous conflicts and errors.
-   Third-party LLM model integration is now fully compatible, expanding your AI model options.

</td></tr><tr><td>

AI Agents for Meetings

</td><td>

1.0.11

</td><td>

Security fixes are released as Multiple root Virtual Agent topics with no role restriction, letting any authenticated user read or write arbitrary meeting, risk, touchpoint and email draft records.

</td></tr><tr><td>

AI agents for SLO

</td><td>

2.3.1

</td><td>

Fixed

 -   Improved the reliability of the SLO creator agent.
-   Fixed a formatting issue with AI-generated SLO work notes.

</td></tr><tr><td>

AI Agents for Talent

</td><td>

6.1.0

</td><td>

No Major Changes.

</td></tr><tr><td>

AI Agents for Telecommunications, Media and Technology

</td><td>

6.3.2

</td><td>

 

</td></tr><tr><td>

AI Agents for Workplace Service Delivery

</td><td>

3.3.12

</td><td>

Fixed

 Improved translation used within the AI Agents.

 Removed

</td></tr><tr><td>

AI Analytics

</td><td>

5.4.3

</td><td>

New

 -   Custom Metrics: Admins can now define custom deflection metrics and configure deflection logic. The Custom Metric page in the AI Admin Center introduces admin-configurable definitions, condition builder, and test-against-live-data functionality. Assistants can be mapped to custom or default definitions, and admins can activate or deactivate custom definitions with automatic reassignment to default.
-   Assist Consumption: Assist consumption analytics is now available in a dedicated overview page. Users can monitor total assist consumption at instance and department levels, and view users grouped by assist consumption bands. New widgets display department-by-day breakdowns and band trends over a rolling 90-day window.
-   Enhanced performance analytics dashboards: Performance analytics enhancements provide consolidated KPI cards and expanded skill metrics. The overview page now includes KPI cards categorized by skills, AI agent, and assistant. The Performance tab for skills displays new KPIs such as total skill execution, daily skill execution, average daily unique users, and department usage comparisons.

 Fixed

 Defects.

 Removed

</td></tr><tr><td>

AI Asset Management

</td><td>

6.2.7

</td><td>

What's new

 -   Domain separation for lifecycle work items - Users now see only lifecycle requests and tasks within their current domain and child domains in Activity Center and Home views.
-   Onboarding Playbook with dynamic, risk-based execution - Streamline lifecycle task management with intelligent playbook-driven onboarding.

 What's fixed.

 -   Rejection comments now display correctly on AI Systems when an asset is rejected.
-   Status updates during asset rejection are now consistent-rejected change and offboarding requests automatically set to 'Canceled' state.

</td></tr><tr><td>

AI Case Management

</td><td>

23.1.1

</td><td>

Fixed

 Handled AI case admin access issues to AI Inquiries on AI Case Management application.

</td></tr><tr><td>

AI Control Tower

</td><td>

7.1.5

</td><td>

AI Control Tower adds new capabilities across discovery, governance, security, monitoring, and measurement of AI usage.

 Inventory and Discovery.

 -   Block AI services detected through ACC.
-   An AI Inventory Enrichment Agent scans your inventory for incomplete records and suggests values to fill the gaps.
-   New and enhanced connectors extend discovery to Microsoft Agent365, Azure AI Foundry, Copilot, and AWS.

 Govern.

 -   Discovered AI systems are now risk-classified at the point of discovery, before they enter the managed workflow.
-   An AI Risk and Control Applicability Advisor recommends the most relevant risks and controls for each system, with rationale.
-   Dynamic Playbook 2.0 tailors onboarding tasks to an asset's risk classification.
-   ServiceNow-managed AI agents can now be published to Microsoft Agent365 and other external registries.

 Secure.

 -   AI agent containment can be triggered automatically based on authored policies in the AI Control Tower, removing the need for manual intervention. Support is extended to Azure AI Foundry for agent runtime and Gemini Enterprise Agent Platform \(via Okta integration\).
-   Design-time security now covers AI agents, tools, MCP servers, and system prompts, not just AI models.
-   The Veza connector now uses OAuth 2.0 for authentication.

 Monitor.

 -   Configure trace data retention to fit your needs.
-   View new latency and token-usage visualizations.
-   Set evaluation metrics at the asset level.
-   Use custom date ranges of up to 18 months for evaluation data.

 Measure.

 Product owners can now view and work with just the AI systems and metrics that matter to them.

 Foundations.

 Domain separation is available across AI Control Tower, enabling MSP and multi-tenant deployments with isolated inventories, security posture, and value data for each tenant.

 For full details, see AI Control Tower release notes.

</td></tr><tr><td>

AI Control Tower Core

</td><td>

9.0.8

</td><td>

See AI Control Tower main store listing for the complete release notes. This app is a dependency of the overall AI Control Tower product.

</td></tr><tr><td>

AI Control Tower - Evaluations

</td><td>

4.1.1

</td><td>

NEW

 \* Go directly to the traces where a mismatch was detected from the AI agent usage deviates from declared purpose recommendation. Previously, the recommendation opened the parent asset record.

 \* A new recommendation groups AI agent quality and safety score drops by severity level, so related drops across multiple assets appear on a single card rather than one card per asset.

 \* Monitor agentic AI performance over time using new filter options in the Monitor agent activity chart. View the top five lowest performing metrics, top five highest performing metrics, or view performance for a specific metric in the chart.

 \* View a list of lowest scoring metrics and the LLM judge's reasoning in the Quality and Safety score cards on the Session details page.

 \* Toggle between input and output when viewing trace details.

 FIXED

 \* Removed redundant session scores and aggregate scores because the details are inside the scores boxes.

 \* The Privileged Access Detector score is 0% but shown in red.

 \* Addressed custom date selection issues in /inventory/\[id\]/monitor.

 \* Discovery issues with Agentic Client type assets.

 \* Removed duplicate insights.

</td></tr><tr><td>

AI Control Tower for Enterprise AI Foundation

</td><td>

1.9.5

</td><td>

AI Control Tower adds new capabilities across discovery, governance, security, monitoring, and measurement of AI usage.

 Secure.

 New

 AI Security Operator role - lets teams delegate agent containment \(deactivate/reinstate\) without granting full AI Steward access.

 Changed

 -   Smarter Overview recommendations - 'Your top recommendations' now ranks agents by critical security events \(with agent name, event count, and threat categories\); Overview and Post-runtime event lists are now consistent with each other.
-   On the Overview tab, the Access issues detailed view includes a description that explains each access issue in plain language - identifying the agent, the operation, the resource, and the denial count.
-   On the Runtime tab, Sensitive data metrics are shown for ServiceNow AI systems in a domain-separated instance.
-   In Settings &gt; Rules and templates &gt; Security , the default values for Sampling rate and Max skill calls have changed on the External AI systems tab to help ensure efficient, predictable analysis. If you're upgrading, your Sampling rate and Max skill calls are updated to the new defaults. Your Detection enabled setting for each metric isn't affected. After upgrading, check your Sampling rate and Max skill calls settings and adjust if needed.

 Fixed

 -   In Policies, AWS Bedrock block and unblock actions fail without an error message when they don't succeed. \(PRB2077055\).
-   After navigating to the Security page, tabs from the previous page were sometimes still shown until the page was refreshed. \(PRB2063965\).
-   Selecting View source record from a security event's source log opened the underlying trace record directly, instead of the related page in Monitoring &gt; Traces. \(PRB2075468\).
-   In the legacy UI experience, some users couldn't see the Security and Privacy tab. \(PRB2090102\).
-   Security fixes.

 Removed

 The base system Traceloop Warehouse HTTPS connection \(sn\_ai\_security.Traceloop\_API alias\) is removed. If you're upgrading and use Traceloop-based external AI metrics, create a new HTTPS connection under that alias and re-create your credential with connection URL. \(PRB2071152\).

 Monitor.

 Changed

 -   Go directly to the traces where a mismatch was detected from the AI agent usage deviates from declared purpose recommendation. Previously, the recommendation opened the parent asset record.
-   A new recommendation groups AI agent quality and safety score drops by severity level, so related drops across multiple assets appear on a single card rather than one card per asset.
-   Monitor agentic AI performance over time using new filter options in the Monitor agent activity chart. View the top five lowest performing metrics, top five highest performing metrics, or view performance for a specific metric in the chart.
-   View a list of lowest scoring metrics and the LLM judge's reasoning in the Quality and Safety score cards on the Session details page.
-   Toggle between input and output when viewing trace details.
-   Widget customization capability support across ALL AICT pages.

 Measure.

 New

 -   Sub-vendor AI costs: Set a rate for a specific service from an integrated vendor, such as an agent platform. The sub-vendor rate takes precedence over the vendor rate. The vendor rate applies to any usage that doesn't have a sub-vendor rate.
-   Subscription AI costs: Record per-seat subscription costs for integrated and non-integrated vendors. Specify the number of licensed seats, the cost per seat, and the contract dates. Optionally, add a one-time setup fee and distribute it over a set number of months so that it's included in the estimated monthly cost.

 Changed

 Assign costs to specific services from integrated vendors.

 Include per-seat subscription costs in AI cost tracking.

 For full details, see AI Control Tower release notes.

</td></tr><tr><td>

AI Control Tower for ServiceNow Otto

</td><td>

7.1.1

</td><td>

See release notes for AI Control Tower for Enterprise AI Foundation.

</td></tr><tr><td>

AICT UI Application

</td><td>

4.0.2

</td><td>

AINPX UI changes for Widget Customizations and Policy Authoring.

</td></tr><tr><td>

AI Data Kit

</td><td>

9.1.3

</td><td>

New

 Create ground truth datasets directly within Data Kit through the Create Labelling Project flow, without requiring a Skill Kit routing path.

 Update.

 Improved synthetic data generation for Voice Agent Evals Support, including a higher domain limit, input sanitization, and record-count accuracy fixes.

</td></tr><tr><td>

AI Desktop Actions

</td><td>

7.0.0

</td><td>

New

 -   Enable the setting to automatically record adaptive desktop actions during execution and reuse them for similar tasks.
-   Automated recording captures your exact steps and converts them instantly into reusable action blocks.
-   AI-powered search automatically suggests matching desktop actions based on your current task.

</td></tr><tr><td>

AI Desktop Actions Core

</td><td>

7.0.0

</td><td>

New

 -   Enable the setting to automatically record adaptive desktop actions during execution and reuse them for similar tasks.
-   Automated recording captures your exact steps and converts them instantly into reusable action blocks.
-   AI-powered search automatically suggests matching desktop actions based on your current task.

</td></tr><tr><td>

AI Discovery

</td><td>

2.10.3

</td><td>

Trace Collector can now discover Tools from incoming traces.

 Bugs fixed in this release:

 -   Agentic Client is now supported by AiDiscoveryAssetManager.
-   Staging domain resolution will now correctly fall back to the session domain when no source group is set, instead of failing when the session domain is global or null.

</td></tr><tr><td>

AI Experience Framework Components

</td><td>

1.5.3

</td><td>

Key features.

 Resolved issues.

 -   Catalog - keyboard focus invisible on the Add attachments field.
-   Mobile native view container query CSS not applied in Karuna SSR.
-   Add attachments widget did not support native view or download of attachments.
-   Order Guide redirection broken from Quick Links due to sysId guard.
-   EmployeeWorks: external links in knowledge articles opened in the same browser tab.
-   User preference modal spanned full browser width after Karuna migration.

 Completed stories.

 -   Catalog, Standard Catalog, and Order Guides UX enhancements.
-   Usage Analytics of Knowledge page usage events maintains a relationship with the opened knowledge article number.

</td></tr><tr><td>

AI Experience Framework Components for Setup Hub

</td><td>

1.5.0

</td><td>

Key features:

 Improved move works config screen to support the 'hints' property, allowing the configuration to specify preloading of the assets.

</td></tr><tr><td>

AI features for Deal Registration

</td><td>

1.0.3

</td><td>

Changed

 Enhanced product offering capture in the submission Agent.

 Fixed: Resolved an Access Control Issue \(ACL\) on the Brazil platform that was blocking deal registration submissions.

</td></tr><tr><td>

AI for document designer

</td><td>

23.1.2

</td><td>

New

 Added support for Non - AI Native SKU.

</td></tr><tr><td>

AI Help Framework

</td><td>

2.0.5

</td><td>

-   Changed: Enabled support for Zurich release.
-   Fixed: Fixed an issue where nudge-related lists were not displayed on the corresponding parent records.

</td></tr><tr><td>

AI Insight Engine

</td><td>

4.1.0

</td><td>

AI Insights Framework is now an app independent of AI Control Tower.

</td></tr><tr><td>

AI Metric Engine

</td><td>

2.2.4

</td><td>

- Defect Fixes.

</td></tr><tr><td>

AI Native Experience for AI Control Tower - ServicenowAI

</td><td>

4.0.4

</td><td>

AI Control Tower adds new capabilities across discovery, governance, security, monitoring, and measurement of AI usage.

 Inventory and Discovery.

 Shadow AI Discovery:

 New

 -   Details about the AI service detected, including models used, users, departments, devices, and event data.
-   Guidance on unknown users/devices.
-   End-user input surfaced for AI services detected via ACC.
-   Ability to turn off this UI for data protection.
-   Block capability for departments using an AI service detected via ACC.

 Changed

 Lifetime aggregations are limited to 3 years.

 Govern.

 New

 AI and Data Marketplace : Streamline the request process for business users by allowing them to select from already approved use cases and models, reducing friction and complexity in submitting requests.

 Secure.

 New

 AI Security Operator role - lets teams delegate agent containment \(deactivate/reinstate\) without granting full AI Steward access.

 Changed

 -   Smarter Overview recommendations - 'Top Recommendations' now ranks agents by critical security events \(with agent name, event count, threat categories\) instead of mixing in the raw events list; Overview and Post-runtime event lists are now consistent with each other.
-   Four customer-reported bugs Fixed: stale tabs after navigation, 'View source record' misrouting to raw trace data, a hidden Security and Privacy tab in the legacy UI, and silent AWS Bedrock block/unblock failures.
-   Action required on upgrade: the base Traceloop Warehouse connection is Removed: customers using Traceloop-based external AI metrics must recreate the connection and credential; sampling-rate/max-skill-call defaults also reset \(existing Detection-enabled settings are untouched\).

 Monitor.

 Changed

 -   Arc dependency - Discover and Evaluate Arc traces at Asset Level for assets categorized as 'Agentic Client'.
-   Tools discovery and evaluation.
-   UI design enhancements for metric line graph and session details page.
-   Arc-Mosaic dependency to support InstanceInfoAPI.
-   TL insights enhancements \(Group insights to reduce the noise\).
-   Update EvalPurposeUsage\(Mismatch\) insight to redirect to trace-level view.
-   Add aggregated metric insight \(with categorize data\) with severity-level grouping.
-   Widget customization capability support across ALL AICT pages.

 Measure.

 New

 -   Sub-vendor AI costs: Set a rate for a specific service from an integrated vendor, such as an agent platform. The sub-vendor rate takes precedence over the vendor rate. The vendor rate applies to any usage that doesn't have a sub-vendor rate.
-   Subscription AI costs: Record per-seat subscription costs for integrated and non-integrated vendors. Specify the number of licensed seats, the cost per seat, and the contract dates. Optionally, add a one-time setup fee and distribute it over a set number of months so that it's included in the estimated monthly cost.

 Changed

 Assign costs to specific services from integrated vendors.

 Include per-seat subscription costs in AI cost tracking.

 For full details, see AI Control Tower release notes.

</td></tr><tr><td>

AIOps Agentic Workforce

</td><td>

2.2.8

</td><td>

Fixed

 -   Resolved an issue where authenticated internal users could read AI worker, alert-rule, and agent-config state without the intended role.
-   Fixed a failure in the autonomous workflow availability check when the Workforce module \(and ZTSD\) is not installed.
-   AIOps Specialist now runs on DARE \(Data Access and Resilience Engine\), improving data handling compliance.
-   Fixed a cross-scope access error on setWorkflow when the watchdog clears stuck em\_gai/em\_alert records.
-   Alert Insights no longer incorrectly reports an alert as closed when auto-close is disabled.
-   Corrected the 'insignificant flow' logic for critical and major percentage thresholds.

</td></tr><tr><td>

AI Policy Framework

</td><td>

2.0.7

</td><td>

New MVP release of AI Control Tower's Policy Framework and kill switch.

</td></tr><tr><td>

AI Risk and Asset Management for ServiceNow AI

</td><td>

1.6.2

</td><td>

New

 Implemented EA integration with AI Asset intake process. Business application can be mapped to Asset record.

 Fixed

 -   Bulk risk assessment creation issue.
-   Entity owner default user issue.
-   Implemented changes to enable improved security.

</td></tr><tr><td>

AI Risk and Compliance Integration with Control Tower

</td><td>

23.1.2

</td><td>

New

 Implemented EA integration with AI Asset intake process. Business application can be mapped to Asset record.

 Fixed

 -   Bulk risk assessment creation issue.
-   Entity owner default user issue.
-   Implemented changes to enable improved security.

</td></tr><tr><td>

AI Risk and Compliance Management

</td><td>

23.1.1

</td><td>

New

 Implemented EA integration with AI Asset intake process. Business application can be mapped to Asset record.

 Fixed

 -   Bulk risk assessment creation issue.
-   Entity owner default user issue.
-   Implemented changes to enable improved security.

</td></tr><tr><td>

AI Security and Privacy

</td><td>

6.2.3

</td><td>

See AI Control Tower main store listing for the complete release notes. This app is a dependency of the overall AI Control Tower product.

 New

 Added an AI Security Operator role that can perform AI agent containment \(kill switch\) without requiring full AI Steward-level access.

 Changed

 -   In AI agent containment \(kill switch\), Deactivate and Reinstate actions are only shown if you have the AI Security Operator or AI Steward roles.
-   On the Overview tab, Your top recommendations now shows only actionable items. In addition, the recommendations rank AI agent insights by number of critical security events and show the agent name, critical event count, and top threat categories.
-   On the Overview tab, the security events list now matches the list on the Post-runtime tab.
-   On the Overview tab, the Access issues detailed view includes a description that explains each access issue in plain language - identifying the agent, the operation, the resource, and the denial count.
-   On the Runtime tab, Sensitive data metrics are shown for ServiceNow AI systems in a domain-separated instance.
-   In Settings &gt; Rules and templates &gt; Security , the default values for Sampling rate and Max skill calls have changed on the External AI systems tab to help ensure efficient, predictable analysis. If you're upgrading, your Sampling rate and Max skill calls are updated to the new defaults. Your Detection enabled setting for each metric is not affected. After upgrading, check your Sampling rate and Max skill calls settings and adjust if needed.

 Fixed

 -   In Policies, AWS Bedrock block and unblock actions fail without an error message when they don't succeed. \(PRB2077055\).
-   After navigating to the Security page, tabs from the previous page were sometimes still shown until the page was refreshed. \(PRB2063965\).
-   Selecting View source record from a security event's source log opened the underlying trace record directly, instead of the related page in Monitoring &gt; Traces. \(PRB2075468\).
-   In the legacy UI experience, some users couldn't see the Security and Privacy tab. \(PRB2090102\).
-   Security fixes.

 Removed

 The base system Traceloop Warehouse HTTPS connection \(sn\_ai\_security.Traceloop\_API alias\) is removed. If you're upgrading and use Traceloop-based external AI metrics, create a new HTTPS connection with the sn\_ai\_security.Traceloop\_API connection alias and re-create your credential. \(PRB2071152\).

</td></tr><tr><td>

AI Service Graph Connector for Amazon

</td><td>

2.2.5

</td><td>

Integration to support discovery of assets from Amazon Quicksuite discovery of tags and additional attributes.

</td></tr><tr><td>

AI Service Graph Connector for Google

</td><td>

1.4.1

</td><td>

New

 -   Implement user-friendly functional error messaging across GCP SGC data source APIs.
-   Import Gemini Enterprise App Agents.
-   Import Gemini Enterprise App Agents Usage.

 Import the following additional attributes

 -   Platform Name information.
-   Owner / Created by - critical for classification and accountability.
-   Project / Resource ID.
-   Identity / Access information.
-   Original Creation Date.

 Import the tags of the AI agent to 'cmdb\_key\_value' table.

 Changed

 Add UX changes for Beta API usage for Gemini Enterprise App.

 Fixed

 -   The connector creates a Consumes::Consumed by relationship between AI Function CIs instead of Depends on::Used by. PRB2086636.
-   Staging table inserts are processed sequentially, causing slow performance when discovering large numbers of Vertex AI assets. PRB2075641.
-   The Gemini Enterprise discovery pipeline creates AI Function-to-Model relationships using the Consumes::Consumed by relationship type instead of Depends on::Used by. PRB2089225.
-   If a single AI asset fails to insert during discovery, the remaining assets in the same discovery run aren't processed. PRB2089224.
-   The Test IAM Permission action doesn't work correctly for connections configured with the JSON key file upload method. PRB2090569.
-   Test Connection fails with an unhandled error, instead of returning a clear error message, when run against an invalid or missing connection. PRB2089222.
-   If a data source template has a missing or deleted data source reference, provisioning stops and the remaining templates aren't provisioned. PRB2089221.

</td></tr><tr><td>

AI Service Graph Connector for Microsoft

</td><td>

3.2.4

</td><td>

-   Discovery of additional Attributes.
-   Tag based discovery.

</td></tr><tr><td>

AI SGC Discovery

</td><td>

2.1.2

</td><td>

Updates to dependencies on marker plugin.

 The plugin is installed with AI Discovery plugin which installs Hyperscaler connectors.

</td></tr><tr><td>

AI Skill Kit

</td><td>

10.1.2

</td><td>

Voice Evals: 1. Actionable Insights and Suggested Fixes for Voice Agent Evaluation: Users will get recommendations to improve agent performance. 2. Caller Behaviour: Users can now select from five caller persona types - Good, Inconsistent, Profane, Introvert, and Disobedient - when configuring voice agent simulations, driving more realistic and varied conversational test coverage.

</td></tr><tr><td>

AI Specialists for HR Service Delivery

</td><td>

1.0.0

</td><td>

This release contains - L1 HR Service Desk AI specialist with following capabilities:

 -   Assignment: Add HR L1 AI Specialist to existing or new HR assignment groups, and cases routed to those groups are picked up by it.
-   Triage: Predicts the HR service on each HR Case and auto-transfers the case to the predicted service when confidence is above your configured threshold.
-   Investigation: Runs grounded search over your HR knowledge bases, catalog items and similar past cases before proposing a resolution.
-   Modes: Works autonomously, responding to employees in 'autonomous' mode if confident, or in 'supervised mode' , where an HR agent reviews every draft before it is sent , based on configuration.
-   Communication and closure: L1 shares its analysis to work notes and resolution notes, and closes the case once the employee accepts , in autonomous mode. On rejection, or when no resolution is found, it unassigns itself and escalates to configured escalation group.

 Measurement: The out-of-the-box Performance tab shows autonomous mode KPIs :

 Resolution rate \(Count\) ; Resolution rate \(%\) ; Mean time to resolution ; L1 HR Specialist Handled All HR cases outcomes ; L1 HR Specialist Handled All HR cases Reasons for reassignment ; L1 HR Specialist handled cases that required a follow-up \(%\).

</td></tr><tr><td>

AI Websearch

</td><td>

4.1.2

</td><td>

Changed

 -   Model Upgrade - Upgraded the Gemini AI Answers model from Gemini 2.5 Flash to Gemini 3.5 Flash for answering Web Search queries.
-   Changed the type of the AI Answers capability from Web Search to Skill to enable proper ACL enforcement from the Generative AI Controller and support deeper integrations. The Web Search capability continues to function correctly with the updated type configuration.

 Fixed

 -   Fixed an issue where grounding chunks \(source citations\) were missing from the web search response when invoking the Web Search capability with Gemini OEM using context-aware queries. Grounding chunks with title and domain are now correctly returned in the response.
-   Fixed an issue where the Gemini 3.5-flash model answered obvious/general knowledge queries \(e.g., 'Why is the sky blue?'\) from parametric memory without triggering the Google Web Search tool, resulting in missing grounding chunks. The web search tool is now consistently invoked for all queries to ensure grounded responses with source citations.

</td></tr><tr><td>

Alert Assist

</td><td>

3.13.4

</td><td>

New

 -   Alert Assist has been migrated to Fluent- The em-gai scoped app now runs on the Fluent framework.
-   The underlying model is switched from Now LLM to Gemma.
-   The gemini\_small model reference is updated to gemini-3.5 to reflect the current naming.

 Fixed

 The Run Service Analysis subflow executes downstream operations with system privileges instead of the caller's identity.

</td></tr><tr><td>

Amazon Bedrock Spoke

</td><td>

1.6.0

</td><td>

Fixed

 Prompt caching support is now available in Chat Completion actions and subflows. Customers can configure a new 'Cache Point' input within the 'System' input object to enable prompt caching for generative AI workflows.

</td></tr><tr><td>

Analytics Generation

</td><td>

4.1.21

</td><td>

Changed

 -   Made Analytics Generation application scope public.
-   Improved skill details page to include key benefits and skill prerequisites.

</td></tr><tr><td>

app-ai-metric-ui

</td><td>

2.2.4

</td><td>

- Defect Fixes.

</td></tr><tr><td>

App Engine Notifications

</td><td>

30.1.2

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

App Engine - Prime

</td><td>

30.2.4

</td><td>

Maintenance release.

</td></tr><tr><td>

App Studio Commons

</td><td>

30.1.1

</td><td>

Maintenance release.

</td></tr><tr><td>

Assist Order Management AI Agent

</td><td>

2.1.5

</td><td>

New capabilities include.

 -   Generating orders from email attachments \(Word, Excel, PDF\).
-   Splitting requests \(including quotes\) into separate orders based on policies like location.
-   Generating order from zoom transcripts.
-   Creating/tracking follow-up action items when order ingestion cannot be completed without assistance.

</td></tr><tr><td>

Autonomous Engineer

</td><td>

30.1.0

</td><td>

New

 -   Generate implementations from specifications with Autonomous Engineer.
-   Automatic test generation from plans.
-   New model support for Azure OpenAI GPT 5.6 Sol and Anthropic Claude on AWS Opus 5.
-   Test suite authoring and execution.
-   ATF list step support.

</td></tr><tr><td>

Autonomous workforce for Strategic Portfolio Management

</td><td>

1.0.1

</td><td>

-   Introduces validation of demands against your organization's existing demand governance policies.
-   Adds compliance feedback that shows which policies a demand doesn't meet and why.
-   Adds policy-based conversion of qualifying demands into delivery work, such as projects or epics.
-   Applies policies consistently across all demands to reduce manual review effort.
-   Includes admin configuration for run triggers and the actions the specialist can take.
-   Logs every validation result and conversion for full auditability.

</td></tr><tr><td>

Build Agent \(Trial\)

</td><td>

2.7.1

</td><td>

New

 New model support

 Build Agent and Autonomous Engineer support the following models in the October 2026 release:

 Google Gemini 3.7 Flash.

 Additional metadata support

 The following metadata are now supported in Build Agent and Autonomous Engineer:

 -   Assessments.
-   Database views.
-   Sys wizard answers.

 Support for SPP

 Build Agent and Autonomous Engineer now support regulated markets through the ServiceNow Protected Platform for Australia, the EU, and Singapore, a cloud offering that stores and processes all customer data in-country on Microsoft Azure infrastructure.

 Expanded support for Playbooks

 Build Agent and Autonomous Engineer now include the following updates to Playbook support:

 -   Public playbooks.
-   Variants.
-   Go back to activity definition.
-   Golden path configuration.
-   Using Automation plan pills.
-   Image attachment support for Image to playbook generation.
-   Configure golden path settings and define the ideal path through decision nodes.

 Changed

 Larger input box for extended prompts

 The input field for Build Agent and Autonomous Engineer prompts and instructions now expands to accommodate longer text entries.

</td></tr><tr><td>

Build Agent Premium

</td><td>

1.7.0

</td><td>

New

 New model support

 Build Agent and Autonomous Engineer support the following models in the October 2026 release:

 Google Gemini 3.7 Flash.

 Additional metadata support

 The following metadata are now supported in Build Agent and Autonomous Engineer:

 -   Assessments.
-   Database views.
-   Sys wizard answers.

 Support for SPP

 Build Agent and Autonomous Engineer now support regulated markets through the ServiceNow Protected Platform for Australia, the EU, and Singapore, a cloud offering that stores and processes all customer data in-country on Microsoft Azure infrastructure.

 Expanded support for Playbooks

 Build Agent and Autonomous Engineer now include the following updates to Playbook support:

 -   Public playbooks.
-   Variants.
-   Go back to activity definition.
-   Golden path configuration.
-   Using Automation plan pills.
-   Image attachment support for Image to playbook generation.
-   Configure golden path settings and define the ideal path through decision nodes.

 Changed

 Larger input box for extended prompts

 The input field for Build Agent and Autonomous Engineer prompts and instructions now expands to accommodate longer text entries.

</td></tr><tr><td>

Business Continuity Management Advanced

</td><td>

2.1.2

</td><td>

Updated BCM and AI Platform apps to Oct versions.

</td></tr><tr><td>

Business Continuity Management Foundation

</td><td>

2.1.3

</td><td>

Updated BCM and AI Platform apps to Oct versions.

</td></tr><tr><td>

Business Continuity Management Prime

</td><td>

1.0.3

</td><td>

With BCM Prime, customers can create their own custom skills and agents.

</td></tr><tr><td>

Care Team Operations AI agent collection

</td><td>

2.2.0

</td><td>

New

 -   Care Team Operations AI Assistant \(chat\): A dedicated Now Assist assistant scoped to Care Team Operations. It includes the Case Creation AI Agent and the 'Request care team assistance' case intake use case, and its search context draws only from Care Team AI Search sources.
-   Care Team Operations Voice AI Assistant: A dedicated voice assistant that includes the Case Creation Voice Agent.

 Enhanced

 -   Focused conversation routing: Assistant conversations route queries directly to the right care team agent or knowledge source. Unrelated catalogs, topics, and general enterprise content are not shown.
-   Care Team Portal assignment: Administrators can assign the Care Team AI Assistant to the Care Team Portal through Portal Properties.

</td></tr><tr><td>

Chat Recommendation

</td><td>

1.10.0

</td><td>

Configuration to add kb fields.

 New models.

 Removed LTS support.

</td></tr><tr><td>

Chat Summarization for Virtual Agent

</td><td>

1.12.9

</td><td>

-   Model changes for October and removing LTS prompt configs as they are deprecated.
-   AIX experiences \(sys\_aix\_experience\) can now be selected from Chat summarization Admin experience.

</td></tr><tr><td>

Cloud Cost Management Advanced

</td><td>

1.1.0

</td><td>

This release introduces support for the Gemma model and refreshes component versions, upgrading Now Assist Platform Advanced to version 3.1.0 and CCM Now Assist to version 1.1.0.

</td></tr><tr><td>

CMDB MCP Server

</td><td>

2.0.1

</td><td>

Fixed

 Added missing tooltip descriptions to tools.

</td></tr><tr><td>

CMDB success advisor

</td><td>

3.2.0

</td><td>

New

 -   Deduplication and Stale CI remediation agents are now available in Data Foundations advisor, enabling remediation directly from advisor-generated remediation plans.
-   CMDB ingestion optimizer agent is now available in SAM advisor, recommending the best-fit ingestion sources and configuration actions to improve CI coverage and attribute completeness.
-   Enhanced principal class recommendations using weighted scoring based on class category, operational criticality, and CI footprint, with improved exclusion-based recommendations.
-   Extended KPI trends from 3 to 6 months across Data Foundations, HAM, and SAM advisor, including trend charts on remediation cards.
-   Added managed-by-group sync status visibility in Data Foundations advisor and principal class scope change confirmations in HAM and Data Foundations advisor when ITSM CI filtering is enabled.

 Changed

 -   Staleness KPI now uses the platform Staleness agent metric when available, with fallback to the legacy calculation.
-   Duplicate CI KPI now includes all duplicates with active remediation tasks.
-   Enhanced remediation action context and dashboard summaries.

 Removed

 -   Legacy 'CIs not updated in last N days' indicators when the new staleness metric is active.
-   Undo removals functionality, replaced by scope change confirmation.

</td></tr><tr><td>

CMDB Workspace

</td><td>

9.7.0

</td><td>

Fixed

 -   Unified Map correctly renders upstream references for self-referencing tables when Show Reverse is enabled.
-   Attestation tasks now accurately mark percent complete, ensuring progress tracking is reliable.

</td></tr><tr><td>

Coaching

</td><td>

9.9.3

</td><td>

Fixed an issue where some coaching-related files failed to install correctly during upgrades.

</td></tr><tr><td>

Collaborative Work Management - Advanced

</td><td>

2.2.2

</td><td>

Changed

 Gemma 4 26B A4B IT is now the default LLM \(large language model\) for ServiceNow Otto for Collaborative Work Management \(CWM\) skills, instead of the earlier Now LLM model.

</td></tr><tr><td>

Common AI Framework

</td><td>

2.1.1

</td><td>

There are no new features included with this release.

 -   The OneExtend Capability Definition \(prompt\) for the Get next steps recommendation skill is supported for Now LLM Service - Now LLM Generic.
-   Code coverage improvements.

</td></tr><tr><td>

Content Understanding

</td><td>

7.2.0

</td><td>

Changed

 -   Improved page rendering performance in document intelligence UI.
-   Updated the models for Chat with Document in Virtual Agent, Attachment Summarization, Key Value Extraction, Table Extraction and Predefined Q and A. Gemini large now uses Gemini 3.5 Flash.

</td></tr><tr><td>

Contract Management Pro - Prime

</td><td>

1.0.23

</td><td>

Changed

 Contract Management Pro - Prime now uses the latest versions of its dependent applications for the October 2026 release.

 Fixed

 -   Fixed an issue where users with AI contract configuration roles could not see the field request table when configuring use case mappings in AI Admin Hub.
-   Review analysis cards in the Word Add-in now render correctly when variation details are unavailable, instead of failing to load.

</td></tr><tr><td>

Conversational Catalog Requests

</td><td>

8.1.2

</td><td>

New

 Expanded agentic conversational support for catalog items using onLoad and onChange client scripts for dynamic behavior.

 Fixed

 Minor defect fixes.

</td></tr><tr><td>

Conversational Studio

</td><td>

13.0.4

</td><td>

New

 -   Bulk migration of Topics to AI Agents is now supported \(MAINT-only\). Admins can select and migrate batches of 100+ Topics to AI Agents at once using the Topics-to-AI Agents tool. The migration workflow includes progress tracking, validation, and assignment of migrated AI Agents to Assistants, with each migration status visible and actionable.
-   Integrated evaluation and actionable insights for migrated AI Agents. The Topics-to-AI Agents tool now supports automated evaluation of migrated AI Agents, enabling admins to generate datasets, run evaluations, and compare quality metrics between Topics and AI Agents. Evaluation results surface dominant failure patterns, ranked by severity and frequency, with drill-down to scenario transcripts and issue explanations.
-   Custom severity levels for evaluation failure patterns. Users can now customize severity levels for actionable insights failure patterns across all evaluations. Severity changes are saved automatically and apply to both past and future evaluations.
-   Scenario drill-down and transcript access in evaluation results. Admins can view detailed scenario lists and transcripts for failed conversations, filter by detected issues, and download transcripts for further analysis.
-   NAP Platform Assistant support in Auto Evaluation. The NAP Platform Assistant is now available as a selectable option in the Auto Evaluation creation flow, and its evaluation results are accessible in the results screen.
-   Testing UI decoupled from Assistant 'Active' state. The Test Assistant button is now enabled even when the Voice Assistant is not active, allowing testing at any time without requiring activation.

 Fixed

 MCP Servers are now hidden from the Asset Library. MCP Server assets are no longer visible in the Asset Library and can only be accessed via the Assistant create/edit flow in a dedicated section. Users cannot modify the discoverable, visible, or promoted status of MCP Servers.

 Removed

</td></tr><tr><td>

Conversation Evaluator

</td><td>

3.2.2

</td><td>

Notification-type conversations have no associated interaction record. They are system notifications rather than interactive conversations.

 The documentation link resolves to the correct AICT documentation page.

 Installing the Conversation Evaluator plugin created pa\_job\_indicators entries with required indicators.

</td></tr><tr><td>

Conversation Insights

</td><td>

3.2.0

</td><td>

Admins can now resolve instance URLs dynamically for GCC and NSC environments. The application supports custom domain names for GCC, GCC High, and NSC instances, ensuring compatibility with government and cloud-specific deployments.

 Certain types of errors during conversation transcript processing have been fixed. The system now correctly handles missing message sequences and strips non-numeric values from sequence identifiers.

</td></tr><tr><td>

CPQ for Manufacturing Advanced

</td><td>

4.0.0

</td><td>

This app will be hidden on the store. No listing content is applicable for this store app.

</td></tr><tr><td>

CPQ for Manufacturing Foundation

</td><td>

4.0.0

</td><td>

This app will be hidden on the store. No listing content is applicable for this store app.

</td></tr><tr><td>

Cryptographic Asset Compliance

</td><td>

1.1.1

</td><td>

Changed

 Models have been updated to support AI insights generation for cryptographic assets.

</td></tr><tr><td>

CSM MCP Server

</td><td>

1.4.6

</td><td>

New

 6 new GenAI tools for CSM MCP Server, featuring full enterprise security and intelligent plugin gating. These tools deploy only on instances where the com.sn.csm.gen.ai plugin is active-no setup dependencies.

 The tool names are:

 1. Get\_customer\_service\_cases.

 2. Get\_case\_tasks.

 3. Case\_summarization.

 4. Resolution\_notes\_generation.

 5. Sentiment\_analysis.

 6. Activity\_response.

</td></tr><tr><td>

CTO Voice AI Agents

</td><td>

2.2.0

</td><td>

New Features

 Care Team Operations Voice AI Assistant: A dedicated voice assistant scoped to Care Team Operations, built around the Case Creation Voice Agent.

 Enhanced

 Focused conversation routing: Voice conversations route directly to the right care team agent or knowledge source. Unrelated catalogs, topics, and general enterprise content are not shown.

</td></tr><tr><td>

Custom App Record Summarization

</td><td>

30.2.3

</td><td>

Changed

 Maintenance release.

</td></tr><tr><td>

Customer Service Management AI agent collection

</td><td>

8.0.4

</td><td>

New

 Usage of AI assist in Customer Service Management is now tracked across cases, chat, and voice, so admins can see how these features are being used.

 Fixed

 Subscription records were updated to support the Mixed AI Native SKU, so customers on that license get the correct entitlements.

</td></tr><tr><td>

Data Discovery

</td><td>

9.1.0

</td><td>

New

 AICT admins can now enable PII redaction for existing AI Control Tower traces and spans. Two changes made in Data Discovery to meet AICT requirements: 1. Added the Luhn Sum check logic to our Credit Card data patterns to improve detection accuracy / reduce false positives 2. Enable test functionality 3. Defined additional synthetic data for each data pattern and added synthetic data for NER data patterns.

</td></tr><tr><td>

Data Privacy

</td><td>

9.1.1

</td><td>

-   Admins can now configure policies for job-based anonymization - data/tables and catalog variables without using Active Data Patterns and Target tables: Flexibility to define anonymization policies for jobs and catalog items without referencing Active Data Patterns or Target Tables.
-   AICT Default Anonymization Policy to scrub sensitive data in traces and spans: Default anonymization policy to anonymize sensitive data in AICT span tables. The policy is defined on any AICT instance with DP or Vault license; requires user to manually trigger anonymization job before policy can act on sensitive data in the AICT tables.

</td></tr><tr><td>

Deployment Pipeline

</td><td>

30.1.2

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

Discovery and Service Mapping Patterns

</td><td>

1.35.1

</td><td>

Fixed

 Kubernetes Pattern Discovery consumed excessive memory on application nodes while retiring stale containers after a restart. Discovery now processes container data page by page, so cleanup completes in large Kubernetes environments. \(PRB2094528\).

</td></tr><tr><td>

Dynamic Guidance

</td><td>

28.6.2

</td><td>

New: Introduced keyboard shortcuts for play, pause and end Dynamic Guidance.

 Fixed

 -   Fixed an issue where custom search sources added to a Dynamic Guidance search profile were not being applied. Custom sources now save correctly and return results as configured.
-   Resolved a certification failure caused by the scoped application referencing roles that were no longer available. The role references have been corrected so the application passes certification.
-   Fixed an accessibility issue where screen readers did not announce the aria labels for the transcript and pause buttons in Dynamic Guidance. These controls now expose proper labels and are announced correctly, improving support for assistive technologies.
-   Fixed a Dynamic Guidance installation failure on internal instances that occurred because the sn\_docs 7.0.6 dependency had been withdrawn. The dependency reference has been updated so installation completes successfully.

</td></tr><tr><td>

EA MCP Server

</td><td>

2.0.2

</td><td>

New

 MCP for Enterprise Architecture is now generally available on the ServiceNow Store.

</td></tr><tr><td>

Employee Center

</td><td>

44.4.2

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Employee Profile

</td><td>

14.3.1

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Employee Slate \(built for Now Assist\)

</td><td>

1.5.3

</td><td>

Added empty state screens and other UI updates.

</td></tr><tr><td>

Enhanced Features for IRM Enterprise

</td><td>

23.1.0

</td><td>

Changed

 Added support for NowLLM gemma.

 Fixed

 Fixed skills not accessible due to AI native and Professional plus SKU.

</td></tr><tr><td>

Enhanced Features for IRM Professional

</td><td>

23.1.0

</td><td>

Changed

 Added support for NowLLM gemma.

 Fixed

 Fixed skills not accessible due to AI native and Professional plus SKU.

</td></tr><tr><td>

Enterprise Architecture for AICT

</td><td>

1.0.1

</td><td>

New

 Enterprise Architecture for AICT is now generally available.

 If you previously associated AI systems with business applications on an Enterprise Architecture Workspace version earlier than 10.1.3, run the Migrate BA Product Model Map from EA Workspace job manually after upgrading.

</td></tr><tr><td>

Enterprise Architecture Workspace

</td><td>

10.1.3

</td><td>

New:

 Added a unique Number to each TRM technical debt record in EA Workspace, making records easier to identify and reference.

 Changed:

 -   Improved the Application Rationalization bubble chart so that the business application side panel opens on the default tab that matches your ServiceNow Otto Business application insights skill configuration. When insights are triggered automatically, the panel opens on the Insights tab. Otherwise, it opens on the Details tab.
-   Updated AI system associations for business applications to use the shared relationship model from Enterprise Architecture for AI Control Tower. You can continue to add and remove AI systems on business applications, and portfolio insights and dashboard counts reflect the updated associations.

 Fixed:

 -   Fixed an issue where column personalization didn't work when the Actual Score toggle was turned on in the Application Rationalization list view side panel.
-   Fixed incorrect or misaligned Application Rationalization columns after using Autofit All Columns.
-   Removed unsupported column personalization actions from Gantt charts.
-   Strengthened query validation and access-control enforcement for Technology Reference Model lifecycle operations and workspace counts.

</td></tr><tr><td>

Exception Management for Unified Security Exposure Management

</td><td>

30.8.1

</td><td>

Fixed

 Fixed: an error \('Security constraints prevent access'\) that could occur when using the Request Exception button. - Fixed an issue where deferral counts were inflated because an approval filter counted updated records as new.

 New

 - Added bulk-edit support to close false positives, update Preferred Solution and Preferred Patch, and unassign remediation owner records. - Refreshed the UX for the Risk Adjustment and Exception Request bulk-edit experience. - Added support for scripted approver levels in exception rules, enabling more dynamic approval routing. - Updated the Exception Request and Modify Risk dialogs with UI improvements. - Improved notifications triggered by risk modification changes.

</td></tr><tr><td>

Experimentation Framework Core

</td><td>

1.1.20

</td><td>

-   New: Centralized feature-flag-driven record gating is now available. Product teams can register records for gating using a shared mapping table and API, enabling consistent feature flag control across platforms without custom logic. Teams can hide or show records based on feature flags and implement gating in their own business rules.
-   Changed: Feature rollout to general availability is now managed with enhanced filtering and opt-in behavior. Features reaching GA are enabled by default, hidden from the Feature Preview Program, and instance patch and hotfix version details are now included in filtering. Boolean values are correctly handled in context APIs.

</td></tr><tr><td>

Export entities

</td><td>

3.6.0

</td><td>

Fixed

 Catalog export requests no longer remain stuck in the Requested state without generating an attachment \(PRB209094\).

</td></tr><tr><td>

Financials Core

</td><td>

6.2.15

</td><td>

New

 -   You can now save your preferred timescope selection on the Financials tab of the project workspace. By default, the system retains the selected timescope for up to 50 recently accessed projects, and admins can raise this limit to up to 200 projects. When you return to a project, your previously selected timescope is restored automatically.
-   Admins can now use a guided setup for financials configuration in Strategic Portfolio Management \(SPM\). The Implementation Accelerator walks admins through configuring labor cost plans, labor cost types, budget allocation, financial baselines, currency settings, investment object linkage, cost plan breakdown rollups, and fiscal calendar settings.
-   You can now view in-context help for key financial fields on the Financials page. Info icons next to each field explain calculations such as planned cost, budget, estimate at completion \(EAC\), Return, ROI, and NPV directly within each widget.

 Changed

 -   Inline editing performance in the financials cost and benefit grid is improved. When you edit and save a single row, only that row refreshes instead of the entire grid. The edited row is locked from further changes until the save completes. This applies to both month and year timescales.
-   Project managers and planning item owners can now recalculate planned cost and benefit values based on updated budget reference rates. A new menu option lets you recalculate all relevant breakdowns at once, with confirmation dialogs and loading overlays to show progress. The previous Recalculate resource cost action is now hidden to avoid duplicate functionality.

 Fixed

 -   Total budget on projects now recalculates correctly when investment budget records are deleted or updated.
-   Multicurrency setup in the project workspace now updates automatically and accurately.
-   Investment record linkage in cost plans and planning items is now consistent across all projects.
-   Converting a demand to a project no longer clears cost in investment currency values.
-   The financials console in the Project Workspace no longer has limitations related to time scope and fiscal range selection.

</td></tr><tr><td>

Generative AI Controller

</td><td>

15.1.2

</td><td>

New: Enabled Admin's the ability to configure PII masking enforcement per capability/skill so latency-sensitive surfaces \(chat, search\) can bypass masking while high-risk surfaces enforce it.

 Fixed: Enabled AI Native Mixed SKU support - to help Enterprise/Pro functionality work seamlessly with AI native SKUs.

 Changed: Model lifecycle management - Model Enabled, Deprecated and Retired Models.

 -   Enabled Gemini 3.7 Flash \(for build agent use case\).
-   Enabled Gemma 4 26B A4B IT \(under Now LLM provider\).
-   Deprecated ServiceNow SLM \(Apriel\) - v2.0.
-   Deprecated ServiceNow LLM \(GPT-OSS\) - v1.0.
-   Deprecated ServiceNow LLM \(GPT-OSS Long-term Stable\) - v1.0.
-   Deprecated ServiceNow SLM \(Apriel Long-term Stable\) - v1.0.
-   Retired Gemini 2.5 Pro.
-   Retired Gemini 2.5 Flash.
-   Retired Gemini 2.5 Flash lite.
-   Retired Claude Sonnet 4.5.

</td></tr><tr><td>

Goal Framework

</td><td>

4.16.0

</td><td>

New

 -   Select Maintain above, Maintain below, or Maintain constant as the target type when defining a target to track progress based on keeping a value above, below, or within a specified range.
-   Progress is now calculated for Maintain-type targets based on the breakdown periods achieved, reflecting partial attainment for each period according to the selected target type.
-   Identify goals and targets across teams and views using the new unique identifier columns, which display a distinct number for each record.

 Changed

 -   Goal and target identifiers now use the OBJ and KR prefixes to align with OKR terminology. A scheduled migration converts existing records from the GOAL and TRGT prefixes, and new records use the updated prefixes.
-   Edit the Type field on a target even when actuals exist. A warning appears before the change is saved, and the update is recorded in the audit history.
-   Changing the Type field on a target no longer resets the unit of measure. The previously selected unit is retained across all editing surfaces and flows.
-   The Type and Unit of measure fields are now synchronized on the Create target window. The unit of measure defaults based on the selected type, reducing confusion during target creation.

 Fixed

 Resolved an issue where creating goal relationships caused errors when the sn\_align\_core plugin was installed without the sn\_align\_ws plugin.

</td></tr><tr><td>

GRC: Advanced Risk

</td><td>

23.1.2

</td><td>

\[New\].

 This release adds a GRC Advisor configuration for the Risk and Risk Event tables, which enables correctness and suggestion capabilities on records in these tables. The configuration is available with the Innovation Lab release of the Data Quality Optimization for Governance, Risk, and Compliance application and applies only when that application is installed.

</td></tr><tr><td>

GRC: Business Continuity Management - Core

</td><td>

12.1.1

</td><td>

Added Knowledge graph support for BCM apps.

</td></tr><tr><td>

GRC: Business Continuity Planning

</td><td>

12.1.2

</td><td>

Added knowledge graph support for BCM apps.

</td></tr><tr><td>

GRC: Business Impact Analysis

</td><td>

12.1.3

</td><td>

Added knowledge graph support for BCM apps.

</td></tr><tr><td>

GRC: Common Workspace Elements

</td><td>

23.1.4

</td><td>

Fixed

 Improved Metric Data Table performance.

 Resolved an issue causing the Metric Data Table to make redundant background data calls on page load, refresh, filter, and record actions, resulting in faster loading and more reliable save/submit behavior.

 Added filtering to Entity Approvals lists

 Users can now filter the Needs Review and History lists on the Entity Approvals landing page to locate specific records easily.

</td></tr><tr><td>

GRC: Crisis Management

</td><td>

12.1.2

</td><td>

Added knowledge graph support for BCM apps.

</td></tr><tr><td>

GRC: Crisis Management integration with Everbridge Notifications

</td><td>

12.1.2

</td><td>

Added knowledge graph support for BCM apps.

</td></tr><tr><td>

GRC: Crisis Map

</td><td>

12.1.1

</td><td>

Added knowledge graph support for BCM apps.

</td></tr><tr><td>

GRC: Metrics

</td><td>

23.1.2

</td><td>

New

 Historical metric data is now available. Metric records now store historical values, enabling users to track changes and trends over time.

 Changed

 -   Threshold ratings and breach status for metric data tasks now update automatically when threshold settings are modified. Pop-up confirmation dialogs appear when editing or deleting thresholds, informing users that ratings and breach status will be recalculated or cleared for associated data.
-   Threshold rating and justification fields on metric data tasks now respond to threshold changes. When a threshold is deleted or breach monitoring is disabled, the justification field is hidden. Threshold ratings update correctly when metric data or override data is changed or saved.

</td></tr><tr><td>

GRC Common GenAI

</td><td>

23.1.3

</td><td>

Changed

 Added support for NowLLM gemma.

 Fixed

 Fixed skills not accessible due to AI native and Professional plus SKU.

</td></tr><tr><td>

GRC Shared GenAI

</td><td>

23.1.1

</td><td>

Changed

 Added support for NowLLM Gemma.

 Fixed

 Resolved AI skills inaccessibility for AI Native and Professional Plus SKUs.

</td></tr><tr><td>

Group-Action Framework

</td><td>

8.1.0

</td><td>

New

 -   Input override queries are now available for incremental prediction workflows. Admins can customize input queries for incremental prediction, allowing tailored data processing.
-   Noise clustering action strategy is now implemented. Action strategy is now available for noise clustering logic, expanding clustering capabilities for more nuanced data handling. Now more BUs such as Suggested Steps ITSM, Suggested Steps CSM, ITOM LEAP can now use Noise Clustering \( recluster -1 group\) and update their existing clusters.
-   Gemma Model available for GAF Skills.
-   Action Strategy now supports additional fields for clustering, allowing more flexible grouping and subgrouping configurations beyond the default source table.

 Changed

 -   Incremental clustering now supports configurable hyperparameters. Admins can adjust clustering parameters in noise clustering configurations for improved control over data grouping.
-   Mapper batch size and parallel flow timeout are now configurable. Admins can set batch size and timeout values for mapping and reducing operations, improving workflow performance and flexibility.

</td></tr><tr><td>

Hardware Asset Management - Advanced

</td><td>

1.0.16

</td><td>

Dependency updated on ServiceNow Otto for Platform Advanced to the latest version \(3.1.0\).

</td></tr><tr><td>

Hardware Asset Management - Prime

</td><td>

1.0.16

</td><td>

ServiceNow Otto for Platform Prime is now updated to version 3.1.0, ensuring compatibility and access to the latest features.

</td></tr><tr><td>

Health and Safety - Advanced

</td><td>

1.0.9

</td><td>

Changed

 Upgraded underlying AI and Health and Safety app dependencies to October release version.

</td></tr><tr><td>

Health and Safety Components

</td><td>

12.2.2

</td><td>

Fixed

 -   Injured person body-part labels display Left/Right prefixes for symmetric body parts, ensuring accurate injury recording and display.
-   The Employee Center bundle now includes a framework de-duplication guard preventing body picker crashes on Employee Center pages.

</td></tr><tr><td>

Health and Safety Core

</td><td>

13.5.0

</td><td>

New

 Health and Safety profiles include Environmental Management and Critical Event Management roles.

 Fixed

 -   Fixed readability of 'syschoice' values after the Health and Safety Core plugin installation. Field-level access controls are updated to grant personalizechoices role users unrestricted choice value visibility.
-   Addressed sn\_ohs\_im\_action create ACL ownership check in the UI layer.
-   Resolved accessibility issue for Delete current injury record icon in Employee Center Advanced Incident Report with Injury flow.
-   Resolved Injury detail form layout issue where long Severity choice labels compressed the Description field and overflowed the multi-injury dialog.

</td></tr><tr><td>

Health and Safety - Foundation

</td><td>

1.0.9

</td><td>

Changed

 Upgraded underlying AI and Health and Safety app dependencies to October release version.

</td></tr><tr><td>

Health and Safety Incident Management

</td><td>

13.3.3

</td><td>

New

 Employees can view their Health and Safety incidents in EmployeeWorks. The My Requests page displays all incident records, enabling users to access details and updates for each incident directly within EmployeeWorks.

 Fixed

 -   The injured person body-part labels correctly include Left/Right prefixes for symmetric body parts. Individual injury selections and data-driven side-specific values are preserved, and the body picker component no longer collapses multiple injuries to a single selection.
-   The Employee Center bundle reliably injects a framework de-duplication guard, preventing crashes in the body picker on customer Employee Center pages.

</td></tr><tr><td>

Health and Safety - Prime

</td><td>

1.0.9

</td><td>

Changed

 Upgraded underlying AI and Health and Safety app dependencies to October release version.

</td></tr><tr><td>

HRSD - Advanced

</td><td>

2.3.1

</td><td>

Licensing app for Advanced SKU.

</td></tr><tr><td>

HRSD - Foundation

</td><td>

2.3.1

</td><td>

Licensing app for Foundation SKU.

</td></tr><tr><td>

HRSD - Prime

</td><td>

2.3.1

</td><td>

Licensing app for Prime SKU.

</td></tr><tr><td>

HR Voice AI Agents

</td><td>

2.4.1

</td><td>

New

 Added support to Pro Plus and Enterprise SKUs. Customers with either of these SKUs will have access to voice agents regardless of Foundation, Advanced, and Prime applications.

</td></tr><tr><td>

Human Resources: Service Portal

</td><td>

44.4.1

</td><td>

Updated to support the latest version of the dependent apps.

</td></tr><tr><td>

Impact

</td><td>

12.0.7

</td><td>

Impact Store App - October Release.

 Get more value from ServiceNow, right inside your instance. This release streamlines setup, sharpens your health score, and helps you turn insight into action.

 What's New: Starting October 8.

 Onboarding - Impact Setup Hub Setting up Impact is now faster and simpler. The new Setup Hub replaces the old linear, text-heavy Guided Setup with a modern experience where admins can:

 -   Register instances automatically or manually.
-   Verify the connection.
-   Start data migration.
-   Review your assigned squad and manage instance access.

 Platform Health - Instance Health Score Your Instance Health Score is now more reliable. It uses a risk-weighted model that evaluates five areas independently - Security, Performance, Manageability, Upgradeability, and User Experience - before combining them into one overall score. Each definition is measured against a fixed reference point, so a change to one finding won't affect unrelated checks or categories. Full and Delta scans now use the same instance-wide counting scope, giving you more stable, comparable score trends over time.

 Value

 -   IVM Data Collection App Discovery: Find all Impact Value Management \(IVM\) data collection apps in one place, grouped by product line, on both the ServiceNow Store and the Impact Store App.
-   Enhanced CSM and HR Outcomes: Explore improved outcomes for CSM and HR, built on current ServiceNow platform capabilities with updated data instrumentation and calculation logic.
-   Estimated Data Customization: Use the Impact Product Console to view and customize estimated data definitions - switch any estimated metric to real, verified data, connected directly to Manage Objectives and Outcomes.

 Accelerators - Multi-Participant Maturity Assessment and Prescriptive Action Planning

 -   Staff Multi-Participant Maturity Assessment: Invite your team to complete domain-specific surveys independently. Once collection closes, responses aggregate into comparative scores, a heat map, and question-level detail - giving you a fuller, more accurate picture than single-user input.
-   Target Maturity Level Prioritization: Set a target maturity level per domain and compare it against your current scores. The system surfaces question-level gaps so you can prioritize which domains to improve first.
-   Prescriptive Action Plan Generation and Export: Generate recommended actions for each prioritized domain, assign owners, and add notes. When your plan's ready, export it as a styled Excel workbook with a summary tab and a tab for each domain.

</td></tr><tr><td>

Impact Common

</td><td>

12.0.3

</td><td>

Impact Store App - October Release.

 Get more value from ServiceNow, right inside your instance. This release streamlines setup, sharpens your health score, and helps you turn insight into action.

 What's New: Starting October 8.

 Onboarding - Impact Setup Hub Setting up Impact is now faster and simpler. The new Setup Hub replaces the old linear, text-heavy Guided Setup with a modern experience where admins can:

 -   Register instances automatically or manually.
-   Verify the connection.
-   Start data migration.
-   Review your assigned squad and manage instance access.

 Platform Health - Instance Health Score Your Instance Health Score is now more reliable. It uses a risk-weighted model that evaluates five areas independently - Security, Performance, Manageability, Upgradeability, and User Experience - before combining them into one overall score. Each definition is measured against a fixed reference point, so a change to one finding won't affect unrelated checks or categories. Full and Delta scans now use the same instance-wide counting scope, giving you more stable, comparable score trends over time.

 Value

 -   IVM Data Collection App Discovery: Find all Impact Value Management \(IVM\) data collection apps in one place, grouped by product line, on both the ServiceNow Store and the Impact Store App.
-   Enhanced CSM and HR Outcomes: Explore improved outcomes for CSM and HR, built on current ServiceNow platform capabilities with updated data instrumentation and calculation logic.
-   Estimated Data Customization: Use the Impact Product Console to view and customize estimated data definitions - switch any estimated metric to real, verified data, connected directly to Manage Objectives and Outcomes.

 Accelerators - Multi-Participant Maturity Assessment and Prescriptive Action Planning

 -   Staff Multi-Participant Maturity Assessment: Invite your team to complete domain-specific surveys independently. Once collection closes, responses aggregate into comparative scores, a heat map, and question-level detail - giving you a fuller, more accurate picture than single-user input.
-   Target Maturity Level Prioritization: Set a target maturity level per domain and compare it against your current scores. The system surfaces question-level gaps so you can prioritize which domains to improve first.
-   Prescriptive Action Plan Generation and Export: Generate recommended actions for each prioritized domain, assign owners, and add notes. When your plan's ready, export it as a styled Excel workbook with a summary tab and a tab for each domain.

</td></tr><tr><td>

Impact Content

</td><td>

12.0.3

</td><td>

Impact Store App - October Release.

 Get more value from ServiceNow, right inside your instance. This release streamlines setup, sharpens your health score, and helps you turn insight into action.

 What's New: Starting October 8.

 Onboarding - Impact Setup Hub Setting up Impact is now faster and simpler. The new Setup Hub replaces the old linear, text-heavy Guided Setup with a modern experience where admins can:

 -   Register instances automatically or manually.
-   Verify the connection.
-   Start data migration.
-   Review your assigned squad and manage instance access.

 Platform Health - Instance Health Score Your Instance Health Score is now more reliable. It uses a risk-weighted model that evaluates five areas independently - Security, Performance, Manageability, Upgradeability, and User Experience - before combining them into one overall score. Each definition is measured against a fixed reference point, so a change to one finding won't affect unrelated checks or categories. Full and Delta scans now use the same instance-wide counting scope, giving you more stable, comparable score trends over time.

 Value

 -   IVM Data Collection App Discovery: Find all Impact Value Management \(IVM\) data collection apps in one place, grouped by product line, on both the ServiceNow Store and the Impact Store App.
-   Enhanced CSM and HR Outcomes: Explore improved outcomes for CSM and HR, built on current ServiceNow platform capabilities with updated data instrumentation and calculation logic.
-   Estimated Data Customization: Use the Impact Product Console to view and customize estimated data definitions - switch any estimated metric to real, verified data, connected directly to Manage Objectives and Outcomes.

 Accelerators - Multi-Participant Maturity Assessment and Prescriptive Action Planning

 -   Staff Multi-Participant Maturity Assessment: Invite your team to complete domain-specific surveys independently. Once collection closes, responses aggregate into comparative scores, a heat map, and question-level detail - giving you a fuller, more accurate picture than single-user input.
-   Target Maturity Level Prioritization: Set a target maturity level per domain and compare it against your current scores. The system surfaces question-level gaps so you can prioritize which domains to improve first.
-   Prescriptive Action Plan Generation and Export: Generate recommended actions for each prioritized domain, assign owners, and add notes. When your plan's ready, export it as a styled Excel workbook with a summary tab and a tab for each domain.

</td></tr><tr><td>

Impact Health Content

</td><td>

7.0.3

</td><td>

New

 This release adds 460 Scan Engine definitions as part of the ongoing Health Assessment migration initiative. The new definitions include both global and application-specific health checks across areas such as Performance Analytics, Vulnerability Response, Customer Service Management, HR Service Delivery, GRC, Risk Management, Security Operations, Discovery, Service Mapping, and more.

 -   242 Global definitions are available to all instances.
-   218 Plugin-specific definitions are evaluated only when the corresponding application or plugin is installed and active.

 This release expands Platform Health coverage by adding additional Scan Engine-based health assessments across the ServiceNow platform and supported applications.

</td></tr><tr><td>

Impact Value Management - App Engine

</td><td>

3.0.1

</td><td>

Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Impact Value Management - Customer Service Management

</td><td>

3.0.4

</td><td>

This release upgrades the Data Collection App for Customer Service Management \(CSM\) with an expanded set of value-measurement metrics.

 All existing metrics remain unchanged. No modifications have been made to current functionality. This release only adds net-new metrics that extend value-measurement capabilities across the supported products.

 For the complete list of new metrics, please refer to the Supporting Document.

 Enhanced Metrics

 Any new metric introduced with this release is classified as an Enhanced Metric. Enhanced Metrics can be collected, and their data will be visible on the data dashboard included with the Data Collection App.

 Important: Automatic data transfer of Enhanced Metrics to ServiceNow's centralized Impact Delivery Instance is not supported.

 To make Enhanced Metric data available on the Impact Delivery Instance, customers must:

 -   Install the Impact In-Platform App, and.
-   Enable ServiceBridge.
-   Configure the Estimated data definition against the enhanced metrics.

 All the steps are mandatory for Enhanced Metric data to appear on the Impact Delivery Instance.

 Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Impact Value Management - Enterprise Architecture

</td><td>

3.0.1

</td><td>

-   As part of this update, the APM data collection apps are renamed to Enterprise Architecture aligned to Product Line. This change only affects how the apps are presented; the underlying data collection functionality itself remains unchanged.
-   Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Impact Value Management - Governance, Risk, and Compliance

</td><td>

4.0.1

</td><td>

-   As part of this update, the IRM data collection apps are renamed to Governance, Risk, and Compliance aligned to Product Line. This change only affects how the apps are presented; the underlying data collection functionality itself remains unchanged.
-   Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Impact Value Management - HR Service Delivery

</td><td>

5.0.1

</td><td>

This release upgrades the Data Collection App for HR Service Delivery \(HRSD\) with an expanded set of value-measurement metrics.

 All existing metrics remain unchanged. No modifications have been made to current functionality. This release only adds net-new metrics that extend value-measurement capabilities across the supported products.

 For the complete list of new metrics, please refer to the Supporting Document.

 Enhanced Metrics

 Any new metric introduced with this release is classified as an Enhanced Metric. Enhanced Metrics can be collected, and their data will be visible on the data dashboard included with the Data Collection App.

 Important: Automatic data transfer of Enhanced Metrics to ServiceNow's centralized Impact Delivery Instance is not supported.

 To make Enhanced Metric data available on the Impact Delivery Instance, customers must:

 -   Install the Impact In-Platform App, and.
-   Enable ServiceBridge.
-   Configure the Estimated data definition against the enhanced metrics.

 All the steps are mandatory for Enhanced Metric data to appear on the Impact Delivery Instance.

 Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Impact Value Management - IT Asset Management

</td><td>

2.0.2

</td><td>

-   As part of this update, the ITAM data collection apps are renamed to IT Asset Management aligned to Product Line. This change only affects how the apps are presented; the underlying data collection functionality itself remains unchanged.
-   Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Impact Value Management - IT Operations Management

</td><td>

4.0.3

</td><td>

-   As part of this update, the ITOM data collection apps are renamed to IT Operations Management aligned to Product Line. This change only affects how the apps are presented; the underlying data collection functionality itself remains unchanged.
-   Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Impact Value Management - IT Service Management

</td><td>

6.0.2

</td><td>

This release upgrades the Data Collection App for IT Service Management \(ITSM\) with an expanded set of value-measurement metrics.

 All existing metrics remain unchanged. No modifications have been made to current functionality. This release only adds net-new metrics that extend value-measurement capabilities across the supported products.

 For the complete list of new metrics, please refer to the Supporting Document.

 Enhanced Metrics

 Any new metric introduced with this release is classified as an Enhanced Metric. Enhanced Metrics can be collected, and their data will be visible on the data dashboard included with the Data Collection App.

 Important: Automatic data transfer of Enhanced Metrics to ServiceNow's centralized Impact Delivery Instance is not supported.

 To make Enhanced Metric data available on the Impact Delivery Instance, customers must:

 -   Install the Impact In-Platform App, and.
-   Enable ServiceBridge.
-   Configure the Estimated data definition against the enhanced metrics.

 All the steps are mandatory for Enhanced Metric data to appear on the Impact Delivery Instance.

 Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Impact Value Management - Security Operations

</td><td>

4.0.4

</td><td>

-   As part of this update, the SecOps data collection apps are renamed to Security Operations aligned to Product Line. This change only affects how the apps are presented; the underlying data collection functionality itself remains unchanged.
-   Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Impact Value Management - Strategic Portfolio Management

</td><td>

4.0.3

</td><td>

-   As part of this update, the SPM data collection apps are renamed to Strategic Portfolio Management aligned to Product Line. This change only affects how the apps are presented; the underlying data collection functionality itself remains unchanged.
-   Compatible: Zurich, Australia, Brazil.

</td></tr><tr><td>

Insights Clustering Utils

</td><td>

3.5.0

</td><td>

New

 Gemma4 large language model is now supported for generative AI skills used by insights clustering.

</td></tr><tr><td>

Integrated Risk Management Advanced

</td><td>

23.1.1

</td><td>

Changed

 Added support for NowLLM gemma.

 Fixed

 Fixed skills not accessible due to AI native and Professional plus SKU.

</td></tr><tr><td>

Integrated Risk Management Foundation

</td><td>

23.1.1

</td><td>

Changed

 Added support for NowLLM gemma.

 Fixed

 Fixed skills not accessible due to AI native and Professional plus SKU.

</td></tr><tr><td>

Integrated Risk Management Prime

</td><td>

23.1.1

</td><td>

Changed

 Added support for NowLLM gemma.

 Fixed

 Fixed skills not accessible due to AI native and Professional plus SKU.

</td></tr><tr><td>

Intelligent Approvals

</td><td>

3.1.8

</td><td>

Fixed

 Fixed defects.

</td></tr><tr><td>

IRM Compliance GenAI

</td><td>

23.1.0

</td><td>

New

 -   Implemented platform directive to support mixed AI Native SKUs.
-   Upgraded NowLLM to Gemma model for improved performance.

</td></tr><tr><td>

IRM Risk GenAI

</td><td>

23.1.1

</td><td>

-   Update the supported model based on October release.
-   Added Gemma model to supported model list.

</td></tr><tr><td>

ITOM - Advanced

</td><td>

1.1.7

</td><td>

New

 AI Agents for Observability

 Added source-vendor tenant validation to the SRE investigate AI agent before processing alerts. Work notes are updated when a tenant mismatch prevents investigation.

 AI Agent Topology Mapping

 Discover AI resources deployed on Microsoft Foundry \(new\) and Microsoft Foundry Hub:

 Microsoft Foundry \(new\)

 -   Discovers AI Agents, Models, Prompts, and Tags.
-   Creates Product and Asset Models for each discovered item, with AICT populated.
-   Establishes relationships between Agent and Model.

 Microsoft Foundry Hub

 -   Discovers AI Assistants, Prompts, Models, Hub Projects, and Tags.
-   Establishes relationships between Assistant and Model, and between Assistant and Hub Project.

 LEAP \(Learning Enhanced Automation Platform\)

 October 3P model support added across all LEAP skills. Gemma 4 26B A4B IT introduced as the new default NowLLM model across all seven skills. Admins can enable/configure 3P Model support.

 Changed

 Cryptographic Asset Compliance

 Models have been updated to support AI insights generation for cryptographic assets.

 AI Agents for Observability

 -   Updated manual investigations from the AI Insights card to run regardless of alert filter conditions. Automatic investigations continue to respect configured filters.
-   Improved the performance and error handling of alert metadata retrieval and alert impact summaries.

 AI Agent Topology Mapping

 Amazon Bedrock

 -   Version is now populated in the object ID and product instance ID fields.
-   Vendor is populated in AI System Digital Asset \[alm\_ai\_system\_digital\_asset\] and AI Prompt Digital Asset \[alm\_ai\_prompt\_digital\_asset\].
-   Manufacturer now populates from the glide.appcreator.company.friendly\_name system property instead of a hardcoded value in the AI System Component Product Model \[cmdb\_ai\_system\_component\_product\_model\] and AI Prompt Product Model \[cmdb\_ai\_prompt\_product\_model\] tables.

 Microsoft Foundry \(classic\)

 Fixed

 AI Agents for Service Level Objective \(SLO\)

 -   Improved the reliability of the SLO creator agent.
-   Fixed a formatting issue with AI-generated SLO work notes.

 Removed

 LEAP \(Learning Enhanced Automation Platform\)

 -   NowLLM v2 model tier retired \(llm\_generic\_large\_v2, llm\_generic\_large\_v2-lts, llm\_generic\_small\_v2-lts\).
-   Gemini large, Gemini small, and Claude Sonnet 4.5 retired Gemini-3.5-flash and Claude Sonnet 4.6 remain as replacements. Default assignments updated accordingly.

</td></tr><tr><td>

ITOM AI Agents For Service Mapping

</td><td>

1.4.3

</td><td>

Fixed

 -   SM MCP Server role was missing the configuration needed to include referenced roles.
-   Service Map name was truncated and could contain an invalid reference.
-   CMDB MCP Server tools were not returning the expected response for Service Mapping operations.
-   Service Map name was truncated to 40 characters and contained an invalid reference.
-   Performance issue: the 'Get all application service names' tool took up to 6 seconds, exceeding the 3-second SLA. Response time now meets the SLA.

</td></tr><tr><td>

ITOM - Prime

</td><td>

1.2.5

</td><td>

ITOM - Prime provides the following capabilities:

 -   AIOps AI Specialist - controlled availability.
-   AI agents for AIOps - Automate alert triage, impact analysis, and root cause investigation with an AI-driven agentic workflow that transforms manual operator processes, typically 30+ clicks and 15+ minutes, into a streamlined, autonomous flow. The workflow processes incoming IT alerts end-to-end, correlating observability data, analyzing affected services, and identifying probable root causes before an operator touches the alert. Consolidated insights are surfaced through the Express List interface, giving operators immediate visibility into what happened, what's affected, and recommended next steps, enabling faster resolution while keeping humans in control of final decisions.
-   AI agents for Observability - Helps IT operators assess business and application service impact, formulate probable cause theories, and prioritize investigations by analyzing data from ServiceNow and seamlessly collaborating with third-party AI agents from leading APM and observability vendors, including New Relic, Dynatrace, and Kentik. Using natural language, IT operators can understand the blast radius of an alert, pinpoint affected services, assess business impact, formulate probable cause theories, and help track down the right teams to drive towards problem resolution.
-   AIOps Learning Enhanced Automation Playbooks - Leverages AI-driven insights to mine historical incident data, dynamically prioritize tasks, and generate actionable resolution playbooks. By automating workflows and enhancing knowledge sharing, AIOps Learning Enhanced Automation Playbooks empowers teams to address issues proactively and efficiently. It reduces mean time to resolution \(MTTR\), increases automation coverage, streamlines processes like certificate renewals, and improves team productivity. This ultimately leads to measurable cost savings and operational excellence.
-   AI agents for HLA - Automate the most complex and time-consuming steps in setting up and operating HLA - mapping business context, classifying log fields, and investigating alerts. Powered by Now Assist, these agents bring AI-driven recommendations directly into HLA workflows, reducing the expertise required to configure the system and helping operators respond to alerts faster and more confidently.
-   AI agents for SLO - Automates the creation of service level objectives \(SLOs\) based on operational data for services and configuration items \(CIs\), helping teams adopt SLOs faster and improve service reliability.

</td></tr><tr><td>

IT Service Management

</td><td>

3.4.0

</td><td>

Changed

 Configuration of AI agents on DARE harness

 AI agents for the IT service desk experience and Change Management workflows configuration now run on the DARE \(Decompose, Act, Recurse and Execute\) harness following backend architecture updates.

</td></tr><tr><td>

IT Service Management Advanced

</td><td>

3.4.0

</td><td>

Changed

 Configuration of AI agents on DARE harness

 AI agents for the IT service desk experience and Change Management workflows configuration now run on the DARE \(Decompose, Act, Recurse and Execute\) harness following backend architecture updates.

</td></tr><tr><td>

IT Service Management AI agent collection

</td><td>

12.0.1

</td><td>

New

 Incident Analyzer

 An agentic capability that automatically investigates new incidents and writes a summary to the incident work notes.

 The summary covers:

 -   What happened and the likely cause, with supporting evidence.
-   Who to contact and proposed assignment groups.
-   Potentially responsible CIs and changes.
-   Related active and historical incidents, events and alerts.
-   Investigation gaps.

 -   Ships inactive. Admins can activate it and configure trigger conditions, with P1 and P2 incidents as the default scope.
-   Sections are left out when the underlying data is not available on the instance, such as Major Incident Management or event and alert tables.
-   Each run consumes 4 assists.

 Changed

 Gemma 4 model support and Now LLM deprecation

 -   Gemma 4 26B-A4B is now a supported ServiceNow-hosted model for Now Assist for ITSM skills and agents, including self-hosted deployments.
-   Gemma 4 is not set as the default model.

 Gemma 4 replaces GPT-OSS for Guardian moderation. By default:

 -   Guardian is on in logging-only mode for agents and conversations.
-   Guardian is on in blocking mode for skills.

 The Now LLM models Apriel and GPT-OSS are deprecated and will not receive long-term support.

 Change AI Specialist guided conversational experience

 The Change AI Specialist now asks for human input only when needed, such as when:

 -   Mandatory fields can't be auto-populated.
-   The risk score exceeds a threshold.
-   Conflicts are detected.
-   Policy requires approval.

 -   When input is required, it asks focused questions about the specific missing information instead of presenting forms.
-   It explains why human input was needed.
-   All interactions take place in the change record's activity stream and are captured in the work notes.

 Fixed

 Investigate and resolve ITSM incidents workflow

 -   The workflow now runs after being duplicated to a subdomain with global scope.
-   Runs no longer end in a Terminated state.
-   The workflow no longer fails with a generic error asking the user to try again later.
-   The work notes tool no longer updates the wrong incident when duplicate incident numbers exist.
-   Output no longer leaves information out with certain model configurations. This affected Dutch, French, Portuguese \(Brazil\), Spanish, Japanese, Italian, and German.
-   Workflow instructions now reference the same AI agent that is configured in the workflow.

 Change quality and assessment

 In the Assess quality of a change request workflow:

 -   Users who launch it from the Assess quality UI action can now confirm recording the quality assessment summary. Previously the workflow kept waiting for this confirmation.
-   Change policy records are now retrieved correctly, so the workflow can complete.

 -   The Change Quality Assessor agent now shows display names instead of internal field names in its output.
-   The Change Quality Assessor agent now saves internal values instead of display values to the change quality score table.
-   The Change Assessor agentic workflow now runs basic validation checks on the change record before running its agentic tools.

 Incident classification and triage

 The Classify service and CI AI agent no longer overwrites a populated Service, Service offering, or Configuration item field on an incident.

 This includes cases where the agent could not read the referenced record.

 The out-of-box Triage and Categorize agentic workflow no longer occasionally asks the user for input.

 Incident record experience

 -   Incident Assist agentic workflow options now display in Japanese when the user's language is set to Japanese.
-   Post Incident Report generation now responds faster.

 SME AI agents

 -   When remedial action is disabled in the L1 worker configuration, the SharePoint SME AI agent now reports a diagnosis with resolution pending instead of no diagnosis.
-   The Zscaler SME AI agent's Action Engagement tool call no longer fails because of an invalid input format.

 Removed

</td></tr><tr><td>

ITSM Admin Experience

</td><td>

3.4.0

</td><td>

Changed

 Configuration of AI agents on DARE harness

 AI agents for the IT service desk experience configuration now run on the DARE \(Decompose, Act, Recurse and Execute\) harness following backend architecture updates.

</td></tr><tr><td>

ITSM Admin Experience Components

</td><td>

3.4.0

</td><td>

Changed

 No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.

</td></tr><tr><td>

ITSM - Advanced

</td><td>

2.4.2

</td><td>

New

 Incident Analyzer

 An agentic capability that automatically investigates new incidents and writes a summary to the incident work notes.

 The summary covers:

 -   What happened and the likely cause, with supporting evidence.
-   Who to contact and proposed assignment groups.
-   Potentially responsible CIs and changes.
-   Related active and historical incidents, events and alerts.
-   Investigation gaps.

 -   Ships inactive. Admins can activate it and configure trigger conditions, with P1 and P2 incidents as the default scope.
-   Sections are left out when the underlying data is not available on the instance, such as Major Incident Management or event and alert tables.
-   Each run consumes 4 assists.

 Changed

 Create and Edit Knowledge in the AI-native fulfiller experience

 -   Create Knowledge and Edit Knowledge are now compatible with UI 26.
-   Fulfillers working incidents and requests in this experience can create and update knowledge articles without leaving it.

 Gemma 4 model support and Now LLM deprecation

 -   Gemma 4 26B-A4B is now a supported ServiceNow-hosted model for Now Assist for ITSM skills and agents, including self-hosted deployments.
-   Gemma 4 is not set as the default model.

 Gemma 4 replaces GPT-OSS for Guardian moderation. By default:

 -   Guardian is on in logging-only mode for agents and conversations.
-   Guardian is on in blocking mode for skills.

 The Now LLM models Apriel and GPT-OSS are deprecated and will not receive long-term support.

 Fixed

 Investigate and resolve ITSM incidents workflow

 -   The workflow now runs after being duplicated to a subdomain with global scope.
-   Runs no longer end in a Terminated state.
-   The workflow no longer fails with a generic error asking the user to try again later.
-   The work notes tool no longer updates the wrong incident when duplicate incident numbers exist.
-   Output no longer leaves information out with certain model configurations. This affected Dutch, French, Portuguese \(Brazil\), Spanish, Japanese, Italian, and German.
-   Workflow instructions now reference the same AI agent that is configured in the workflow.

 Change quality and assessment

 In the Assess quality of a change request workflow:

 -   Users who launch it from the Assess quality UI action can now confirm recording the quality assessment summary. Previously the workflow kept waiting for this confirmation.
-   Change policy records are now retrieved correctly, so the workflow can complete.

 -   The Change Quality Assessor agent now shows display names instead of internal field names in its output.
-   The Change Quality Assessor agent now saves internal values instead of display values to the change quality score table.
-   The Change Assessor agentic workflow now runs basic validation checks on the change record before running its agentic tools.

 Incident classification and triage

 The Classify service and CI AI agent no longer overwrites a populated Service, Service offering, or Configuration item field on an incident.

 This includes cases where the agent could not read the referenced record.

 The out-of-box Triage and Categorize agentic workflow no longer occasionally asks the user for input.

 Requested Item Summarization

 -   Summaries now match the requested item being viewed.
-   Summaries are no longer empty when the session language is Portuguese \(Brazil\) and Now LLM is in use.

 Incident record experience

 The Assign button in the Record Information panel in Service Operations Workspace now generates hyperlinks in its output.

 The Now Assist modal now reflects the Assigned to field's mandatory state after a UI policy makes the field optional.

 -   Previously this blocked saving the form in Service Operations Workspace.
-   Previously the mandatory state was shown inconsistently in the native UI.

 -   Bullet-point formatting in work notes no longer breaks when a field such as Assignment group is changed and the record is saved.
-   Incident Assist agentic workflow options now display in Japanese when the user's language is set to Japanese.
-   Post Incident Report generation now responds faster.

 Removed

</td></tr><tr><td>

ITSM Advanced Admin Experience

</td><td>

3.4.0

</td><td>

Changed

 Configuration of AI agents on DARE harness

 AI agents for the IT service desk experience and Change Management workflows configuration now run on the DARE \(Decompose, Act, Recurse and Execute\) harness following backend architecture updates.

</td></tr><tr><td>

ITSM Autonomous Workforce

</td><td>

1.2.1

</td><td>

New

 -   Requesters get follow-up questions for mandatory catalog variables the AI Specialist couldn't fill from the incident; once all are answered, it submits the request on their behalf. AI Admins cap the exchange via Replies before reassigning, after which the requester gets a link to a draft request with answers so far.
-   Requesters who submit a drafted catalog request from the AI Specialist's link have their incident resolved automatically, with a resolution note appended to close notes.
-   Service Desk Managers get a Catalog tab on the AI Specialist Performance dashboard covering catalog items used, requests drafted and submitted, AI vs. requester submissions, and outcome cards \(Zero touch drafts, Abandoned in drafts, Cancelled after submit, Reassigned to SDA, Drafts with incomplete variables\). Hidden when the catalog slot-filling API is unavailable.
-   AI Admins can switch response templates between fixed and dynamic mode, where the AI Specialist writes activity notes, comments, work notes, and close notes from free-form admin instructions.

 Changed

 -   When a requester escalates to a human agent, catalog request items the AI Specialist submitted are closed as incomplete with a cancellation comment instead of left open.
-   Requesters reassigned after a follow-up reply get a reassignment note written by the AI Specialist instead of a generic scripted message.
-   Service Desk Managers see Coverage rate calculated as closed incidents durably resolved by the AI Specialist over those assigned to eligible groups, and Durable auto-resolve rate against incidents attempted. Subtitle and tooltips reflect the new calculations.
-   AI Admins with custom incident states get hold reasons, close codes, and cross-group routing state resets that follow the worker's state mapping.
-   AI Admins see the Auto-submit catalog requests setting reworded around drafts: the AI Specialist submits only when it filled every mandatory variable; otherwise the employee completes the draft.

 Fixed

 Performance dashboard:

 -   Incidents closed by eligible assignment groups counted every group and included canceled incidents.
-   Incident outcomes total counted only resolved, reopened, and reassigned autopilot incidents, so it didn't match the routing funnel.
-   Incident outcome counts could differ from the linked list when the viewer's time zone differed from the PA collection job's.
-   KB articles tab summary metrics didn't display because data access was granted to the worker role instead of the AI worker manager role.
-   KB articles tab took 23-28 seconds to load and didn't reliably refresh when selected.

 -   Incidents resolved after a positive requester reply left the Save activity notes step showing as ongoing for three days.
-   A 'no article found' knowledge feedback task could be created even when the AI Specialist cited a matching article whose link was removed from the customer note for access reasons.
-   KB article attachments weren't used when composing responses, and one failed knowledge search request returned empty results for every query in that search.
-   Incidents the AI Specialist reopened itself were counted as reopened by a person, marking its proposed solution as rejected.
-   Outcomes for incidents handled before the AI Specialist moved to its own application records could be downgraded from resolved to reassigned by the post-execution metrics job.
-   Coaching application files were missing after upgrading.

 Removed

 Performance dashboard

 -   Copilot gauge removed from At a glance; the section is hidden in Copilot mode.
-   Coverage autopilot numerator/denominator scorecards replaced in the detailed view by cards for incidents closed by eligible groups, attempted, and durably resolved.

</td></tr><tr><td>

ITSM Change Admin Experience

</td><td>

1.3.1

</td><td>

Changed

 Configuration of AI agents on DARE harness

 AI agents for the Change Management workflows configuration now run on the DARE \(Decompose, Act, Recurse and Execute\) harness following backend architecture updates.

</td></tr><tr><td>

ITSM Employee Experience

</td><td>

3.4.0

</td><td>

Changed

 No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.

</td></tr><tr><td>

ITSM - Foundation

</td><td>

2.4.2

</td><td>

Changed

 Create and Edit Knowledge in the AI-native fulfiller experience

 -   Create Knowledge and Edit Knowledge are now compatible with UI 26.
-   Fulfillers working incidents and requests in this experience can create and update knowledge articles without leaving it.

 Gemma 4 model support and Now LLM deprecation

 -   Gemma 4 26B-A4B is now a supported ServiceNow-hosted model for Now Assist for ITSM skills and agents, including self-hosted deployments.
-   Gemma 4 is not set as the default model.

 Gemma 4 replaces GPT-OSS for Guardian moderation. By default:

 -   Guardian is on in logging-only mode for agents and conversations.
-   Guardian is on in blocking mode for skills.

 The Now LLM models Apriel and GPT-OSS are deprecated and will not receive long-term support.

 Fixed

 Investigate and resolve ITSM incidents workflow

 -   The workflow now runs after being duplicated to a subdomain with global scope.
-   Runs no longer end in a Terminated state.
-   The workflow no longer fails with a generic error asking the user to try again later.
-   The work notes tool no longer updates the wrong incident when duplicate incident numbers exist.
-   Output no longer leaves information out with certain model configurations. This affected Dutch, French, Portuguese \(Brazil\), Spanish, Japanese, Italian, and German.
-   Workflow instructions now reference the same AI agent that is configured in the workflow.

 Incident classification and triage

 The Classify service and CI AI agent no longer overwrites a populated Service, Service offering, or Configuration item field on an incident.

 This includes cases where the agent could not read the referenced record.

 The out-of-box Triage and Categorize agentic workflow no longer occasionally asks the user for input.

 Requested Item Summarization

 -   Summaries now match the requested item being viewed.
-   Summaries are no longer empty when the session language is Portuguese \(Brazil\) and Now LLM is in use.

 Incident record experience

 The Assign button in the Record Information panel in Service Operations Workspace now generates hyperlinks in its output.

 The Now Assist modal now reflects the Assigned to field's mandatory state after a UI policy makes the field optional.

 -   Previously this blocked saving the form in Service Operations Workspace.
-   Previously the mandatory state was shown inconsistently in the native UI.

 -   Bullet-point formatting in work notes no longer breaks when a field such as Assignment group is changed and the record is saved.
-   Incident Assist agentic workflow options now display in Japanese when the user's language is set to Japanese.
-   Post Incident Report generation now responds faster.

 Removed

</td></tr><tr><td>

ITSM Fulfiller Experience

</td><td>

3.4.0

</td><td>

Changed

 No code updates were made in this release. The release number has been updated to maintain consistency with changes in related IT Service Management applications.

</td></tr><tr><td>

ITSM L1 AI Specialist

</td><td>

1.2.2

</td><td>

New

 -   Requesters get follow-up questions for mandatory catalog variables the AI Specialist couldn't fill from the incident; once all are answered, it submits the request on their behalf. AI Admins cap the exchange via Replies before reassigning, after which the requester gets a link to a draft request with answers so far.
-   Requesters who submit a drafted catalog request from the AI Specialist's link have their incident resolved automatically, with a resolution note appended to close notes.
-   Service Desk Managers get a Catalog tab on the AI Specialist Performance dashboard covering catalog items used, requests drafted and submitted, AI vs. requester submissions, and outcome cards \(Zero touch drafts, Abandoned in drafts, Cancelled after submit, Reassigned to SDA, Drafts with incomplete variables\). Hidden when the catalog slot-filling API is unavailable.
-   AI Admins can switch response templates between fixed and dynamic mode, where the AI Specialist writes activity notes, comments, work notes, and close notes from free-form admin instructions.

 Changed

 -   When a requester escalates to a human agent, catalog request items the AI Specialist submitted are closed as incomplete with a cancellation comment instead of left open.
-   Requesters reassigned after a follow-up reply get a reassignment note written by the AI Specialist instead of a generic scripted message.
-   Service Desk Managers see Coverage rate calculated as closed incidents durably resolved by the AI Specialist over those assigned to eligible groups, and Durable auto-resolve rate against incidents attempted. Subtitle and tooltips reflect the new calculations.
-   AI Admins with custom incident states get hold reasons, close codes, and cross-group routing state resets that follow the worker's state mapping.
-   AI Admins see the Auto-submit catalog requests setting reworded around drafts: the AI Specialist submits only when it filled every mandatory variable; otherwise the employee completes the draft.

 Fixed

 Performance dashboard:

 -   Incidents closed by eligible assignment groups counted every group and included canceled incidents.
-   Incident outcomes total counted only resolved, reopened, and reassigned autopilot incidents, so it didn't match the routing funnel.
-   Incident outcome counts could differ from the linked list when the viewer's time zone differed from the PA collection job's.
-   KB articles tab summary metrics didn't display because data access was granted to the worker role instead of the AI worker manager role.
-   KB articles tab took 23-28 seconds to load and didn't reliably refresh when selected.

 -   Incidents resolved after a positive requester reply left the Save activity notes step showing as ongoing for three days.
-   A 'no article found' knowledge feedback task could be created even when the AI Specialist cited a matching article whose link was removed from the customer note for access reasons.
-   KB article attachments weren't used when composing responses, and one failed knowledge search request returned empty results for every query in that search.
-   Incidents the AI Specialist reopened itself were counted as reopened by a person, marking its proposed solution as rejected.
-   Outcomes for incidents handled before the AI Specialist moved to its own application records could be downgraded from resolved to reassigned by the post-execution metrics job.
-   Coaching application files were missing after upgrading.

 Removed

 Performance dashboard

 -   Copilot gauge removed from At a glance; the section is hidden in Copilot mode.
-   Coverage autopilot numerator/denominator scorecards replaced in the detailed view by cards for incidents closed by eligible groups, attempted, and durably resolved.

</td></tr><tr><td>

ITSM MCP Server

</td><td>

3.3.2

</td><td>

New

 Tool annotations: Standard MCP tool annotations are now included on the following tool sets, so connected AI clients can read how each tool behaves.

 -   On-call tools.
-   Change tools.
-   Requester tools.
-   Incident tools.
-   Knowledge graph tool.

 Changed

 Requester actions consolidated into incident tools: The same tools now serve both fulfillers and requesters, with ACL checks governing access according to each user's permissions.

 -   Add comments: Now handled through the Modify incident tool.
-   Escalate incident: Now handled through the Modify incident tool.
-   Check incident status: Now handled through the Get incident details tool.

 Removed

</td></tr><tr><td>

ITSM - Prime

</td><td>

2.4.2

</td><td>

New

 Incident Analyzer

 Automatically investigates new incidents and writes a summary to the work notes:

 -   What happened, likely cause, and supporting evidence.
-   Who to contact and proposed assignment groups.
-   Potentially responsible CIs and changes.
-   Related incidents, events, and alerts.
-   Investigation gaps.

 -   Ships inactive. Admins can activate it and configure triggers; P1 and P2 incidents are the default scope.
-   Sections are omitted when the underlying data isn't available on the instance.
-   Each run consumes 4 assists.

 Changed

 Create and Edit Knowledge in the AI-native fulfiller experience

 Now compatible with UI 26, so fulfillers can create and update knowledge articles without leaving the experience.

 Gemma 4 model support and Now LLM deprecation

 -   Gemma 4 26B-A4B is now a supported ServiceNow-hosted model, including for self-hosted deployments. It is not the default model.
-   Gemma 4 replaces GPT-OSS for Guardian moderation. By default, Guardian logs only for agents and conversations and blocks for skills.
-   Now LLM models Apriel and GPT-OSS are deprecated and will not receive long-term support.

 Change AI Specialist guided conversational experience

 -   Asks for human input only when needed, such as when mandatory fields can't be auto-populated, risk exceeds a threshold, conflicts are detected, or policy requires approval.
-   Asks focused questions instead of presenting forms, and explains why input was needed.
-   All interactions are captured in the change record's work notes.

 Fixed

 Investigate and resolve ITSM incidents workflow

 -   Now runs after being duplicated to a subdomain with global scope.
-   No longer ends in a Terminated state or fails with a generic error.
-   The work notes tool no longer updates the wrong incident when incident numbers are duplicated.
-   No longer omits information in Dutch, French, Portuguese \(Brazil\), Spanish, Japanese, Italian, and German with certain models.
-   Instructions now reference the AI agent configured in the workflow.

 Change quality and assessment

 -   The Assess quality of a change request workflow no longer stalls waiting for confirmation when launched from the UI action.
-   The Change Quality Assessor agent now shows display names instead of internal field names, and saves internal values to the quality score table.
-   The Change Assessor workflow now validates the change record before running its tools.

 Incident classification and triage

 -   The Classify service and CI AI agent no longer overwrites populated Service, Service offering, or Configuration item fields.
-   The Triage and Categorize workflow no longer asks the user for input unexpectedly.

 Requested Item Summarization

 -   Summaries now match the requested item being viewed.
-   Summaries are no longer empty in Portuguese \(Brazil\) with Now LLM.

 Incident record experience

 -   The Assign button in Service Operations Workspace now generates hyperlinks.
-   The Now Assist modal now respects UI policies that make Assigned to optional.
-   Work notes bullet formatting no longer breaks when a field is changed and saved.
-   Incident Assist options now display in Japanese when that is the user's language.
-   Post Incident Report generation is faster.

 SME AI agents

 -   The SharePoint SME AI agent now reports a diagnosis with resolution pending when remedial action is disabled.
-   The Zscaler SME AI agent's Action Engagement tool no longer fails on invalid input format.

 Removed

</td></tr><tr><td>

ITSM Virtual Agent Conversations

</td><td>

9.3.6

</td><td>

Fixed

 A Minor string concatenation issue.

</td></tr><tr><td>

Knowledge Capabilities in UI Builder

</td><td>

32.7.5

</td><td>

Fixed: minor styling fixes back-ported to this version.

</td></tr><tr><td>

Knowledge Center

</td><td>

31.33.7

</td><td>

New

 -   Authors can now edit Knowledge Center articles using a rich markdown code editor. The new editor supports rich text input with automatic markdown conversion, code highlighting, and autocomplete, and is integrated into UI16, Seismic KC, and AIUX article editing pages.
-   Manual translation for markdown content is now enabled. Users can manually translate markdown articles in both UI16 and Workspace environments, ensuring translated content retains markdown formatting and is accessible.

 Changed

 -   The Attached Knowledge UI Macro has been modernized to an API-driven architecture.
-   The legacy Jelly/XML component is now replaced with a web component using LitJS and native CSS, improving performance, maintainability, and alignment with UI26 migration.

 Fixed

 -   Scheduled Article Optimization jobs no longer generate errors related to missing references during execution.
-   Knowledge Center Enhanced Content Editor table component labels now display correctly in Japanese-language sessions.
-   Cross-scope privilege issues for article family overview reconciliation have been resolved; Knowledge Center features now operate as expected across scopes.
-   Top Knowledge Actions on the KC Hub page now redirect correctly for non-English session languages. Navigation for 'Gap' and 'Duplicates' actions has been corrected to match locale-dependent labels and widened to cover all relevant gap types.

</td></tr><tr><td>

Knowledge Graph

</td><td>

8.4.1

</td><td>

Fixed few defects.

</td></tr><tr><td>

LEAP

</td><td>

4.4.0

</td><td>

New

 October 3P Model support is now available across all LEAP skills. The LEAP platform introduces Gemma 4 26B A4B IT as a new NowLLM model for the October release, set as the default within NowLLM's model pool for all skills. Admins can enable and configure 3P Model support, and users can utilize expanded GenAI model catalog capabilities as intended.

 Removed

 -   NowLLM v2 model tier \(llmgenericlargev2, llmgenericlargev2-lts, llmgenericsmall\_v2-lts\) has been retired and is no longer available in the model catalog.
-   Gemini large, Gemini small, and Claude Sonnet 4.5 models have been retired. Gemini-3.5-flash and Claude Sonnet 4.6 remain as replacements.

</td></tr><tr><td>

Legal and Contracts Common Utilities

</td><td>

1.2.4

</td><td>

Fixed

 Security fixes.

</td></tr><tr><td>

Legal Service Delivery - Prime

</td><td>

1.0.18

</td><td>

Changed

 Legal Service Delivery - Prime now uses the latest versions of its dependent platform applications for the October 2026 release.

</td></tr><tr><td>

Licensing Engine

</td><td>

6.6.0

</td><td>

New

 Licensing now supports decimal assist ratios for entitlement calculations. Decimal values are supplied from SKU metadata, enabling more precise allocation for AI features.

 The entitlement API now includes Program Type, Product Family 3, and Meter Type fields. These fields are extracted from entitlement payloads, persisted, and exposed in API responses to support AI Native Mixed-SKU scenarios.

 Changed

 The getAllActiveApplications API has been optimized for improved performance and compatibility with the AINPX Admin Dashboard. Existing data is automatically backfilled, and API responses now reflect updated fields without impacting other entitlement data.

</td></tr><tr><td>

List AI Experience

</td><td>

3.1.6

</td><td>

Fixed

 -   The 'Summarize recent changes' capability now generates AI summaries in the user's configured language instead of defaulting to English.
-   A security vulnerability in the AI-generated change summary rendering has been resolved.
-   Removed unused legacy code from the Grouping and Summarization skill to improve performance.

</td></tr><tr><td>

Manufacturing Commercial Operations Advanced

</td><td>

4.0.0

</td><td>

This app will be hidden on the store. No listing content is applicable for this store app.

</td></tr><tr><td>

Manufacturing Commercial Operations AI agents collection

</td><td>

5.1.0

</td><td>

Changed

 -   Introduction of new Open Weight Model: Gemma 4 26B-A4B.
-   The new Open Weight Model is now supported but is not designated as the default model for all ServiceNow Otto for Manufacturing Commercial Operations \(MCO\) capabilities.

</td></tr><tr><td>

Manufacturing Commercial Operations Foundation

</td><td>

4.0.0

</td><td>

This app will be hidden on the store. No listing content is applicable for this store app.

</td></tr><tr><td>

Manufacturing Commercial Operations Prime

</td><td>

4.0.0

</td><td>

This app will be hidden on the store. No listing content is applicable for this store app.

</td></tr><tr><td>

MCP for Strategic Portfolio Management

</td><td>

1.5.0

</td><td>

New

 -   Control access to MCP tools using role-based access control \(RBAC\) roles.
-   Added support for tool annotations, such as readOnlyHint, to describe tool behavior to MCP clients.

</td></tr><tr><td>

Microsoft Azure OpenAI Generative AI Spoke

</td><td>

3.13.0

</td><td>

Changed

 -   Prompt caching is now supported in spoke actions and subflows. Users can provide a prompt caching object as input, which is sent in the request body to optimise token utilisation and manage prompt retention. The SSE response handler has been updated to handle prompt caching parameters.
-   Vision capabilities now accept reasoning effort parameters. Users can specify reasoning effort inputs in Chat Completions \(Vision\) actions and wrapper subflows, allowing outputs to be tailored based on reasoning effort requirements.
-   Image fetching supports computer screenshot type. The system now processes images of type 'computer\_screenshot' in addition to 'inputimage' when handling Microsoft Azure OpenAI requests.

 Fixed

 Azure Guardian request body.

</td></tr><tr><td>

Model Context Protocol Client

</td><td>

2.4.5

</td><td>

- Schema changes done to support widgets for MCP tools in Assistants in the upcoming releases.

</td></tr><tr><td>

Model Context Protocol Server

</td><td>

1.9.1

</td><td>

New

 Per-tool role requirements: Administrators can now require a specific role on an individual tool, configured in MCP Server Console and enforced at both tool discovery and tool invocation, so a tool that a user is not entitled to use is neither listed to them nor callable by them.

 Independent tool activation: Authorized users can activate and deactivate tools on a server, and individual tools, independently of one another.

 Improved.

 The Monitoring dashboard has been rebuilt on the current interface, including a proper empty state when no data is available yet.

 Tool record pages load faster, removing the one-to-two second delay on opening a tool.

 The console has been remediated for WCAG accessibility, covering heading structure on tool detail and app creation pages, accessible names on category selection controls, colour contrast in Coral Dark mode, and layout integrity at 200% zoom.

 Interface strings across the console are now fully localizable, replacing hardcoded text in server creation, tool creation, OAuth setup, and navigation breadcrumbs.

 Fixed

 Tool annotations \(readOnlyHint, destructiveHint, idempotentHint, openWorldHint\) are now returned correctly by the MCP Tools API. Previously these hints were lost in transit, causing MCP clients to miscategorize tools.

 Out-of-box tool definitions can no longer be modified in place by a tools administrator, closing a path that bypassed the required clone-first governance flow.

 REST API tools created through the classic interface no longer save a null JSONPath, which previously caused a 500 error on invocation.

 Cloning a tool with Create Alike now copies input values and resolver table fields to the new tool.

 Server URLs created inside scoped applications are now allowlisted correctly, unblocking third-party identity provider configurations.

 The tools dropdown no longer lists APIs from outside the intended scope.

 Selecting a server or tool from the Monitoring section no longer returns 'Record not found'.

 MCP Apps invocation within AI clients has been corrected.

</td></tr><tr><td>

Now Assist for Prompt Assistance

</td><td>

6.1.5

</td><td>

Actionable insights pipeline now supports Voice Agents.

</td></tr><tr><td>

observ-ai-agents-app

</td><td>

6.4.1

</td><td>

New

 Added source-vendor tenant validation to the SRE investigate AI agent before processing alerts. Work notes are updated when a tenant mismatch prevents investigation.

 Changed

 -   Updated manual investigations from the AI Insights card to run regardless of alert filter conditions. Automatic investigations continue to respect configured filters.
-   Improved the performance and error handling of alert metadata retrieval and alert impact summaries.

</td></tr><tr><td>

Operational Sustainability Management

</td><td>

23.1.0

</td><td>

Fixed

 Fixed critical security vulnerabilities.

</td></tr><tr><td>

Opportunity Management Application

</td><td>

14.1.12

</td><td>

Fixed

 -   Fixed Net New ACV not syncing correctly from Quote to Opportunity.
-   Meeting occurrences now correctly populate the associated record and table.
-   Corrected touchpoint state data for Opportunity summarization.
-   Fixed source tag information being truncated on the Opportunity summary card.
-   Resolved non-related team members and product offering families appearing on the Manage Allocations page.
-   Fixed a security issue where unauthorized users could access Quote numbers and versions through the Primary Quote reference qualifier.

</td></tr><tr><td>

Opportunity Management Data Model

</td><td>

14.2.12

</td><td>

Fixed

 -   Fixed Net New ACV not syncing correctly from Quote to Opportunity.
-   Meeting occurrences now correctly populate the associated record and table.
-   Corrected touchpoint state data for Opportunity summarization.
-   Fixed source tag information being truncated on the Opportunity summary card.
-   Resolved non-related team members and product offering families appearing on the Manage Allocations page.
-   Fixed a security issue where unauthorized users could access Quote numbers and versions through the Primary Quote reference qualifier.

</td></tr><tr><td>

Pipeline

</td><td>

30.1.2

</td><td>

App is a dependency of App Engine Studio. Please see App Engine Studio for release notes.

</td></tr><tr><td>

Platform AI Agents and Skills

</td><td>

14.1.5

</td><td>

New

 Now LLM now supports the Gemma model for all platform skills \(Summarization, Resolution notes, Activity response generation, Sentiment analysis, Email \(EMC, ERR\)\).

 Changed

 -   Improvements to citations for resolution notes, ensuring consistency and a better user experience.
-   Updates to the Process task closure workflow to include additional features like creating knowledge base articles, following up with customer and generating a post-mortem report.
-   Improved quality of checklist generation for approval agent.
-   Enforced field-level access control lists under role masking, added graceful failure mechanisms and improved diagnostics for Record summarization.
-   User interface updates to intent based Activity response generation.

</td></tr><tr><td>

Playbook Experience

</td><td>

29.7.5

</td><td>

New

 See the ideal path. The stage picker and activity picker now show stages and activities that run only when their conditions are met, so playbook users can see what might come next.

 Fixed

 Nested playbook user experience issues fixed.

</td></tr><tr><td>

Playbook Experience Components

</td><td>

29.7.1

</td><td>

New

 See the ideal path. The stage picker and activity picker now show stages and activities that run only when their conditions are met, so playbook users can see what might come next.

 Fixed

 Nested playbook user experience issues fixed.

</td></tr><tr><td>

Portfolio Planning

</td><td>

8.19.0

</td><td>

New

 -   View and manage smart assessments in Demands, including an assessments list page, assessment form, database view, role-based access, automated business rules for triggering and scoring, and declarative stakeholder actions. Users can view the assessments relevant to them directly in Demands in Portfolio Planning Workspace.
-   Configure demand types with dynamic fields that render on the demand record page in Demands, supporting Enterprise-Wide Deployment. Administrators can configure a unique default dashboard for each partition.
-   View and manage resource assignments using the new Resource Board view in Demands.
-   View contextual info messages on the Actuals to Date, Progress, and Breakdown columns for Maintain-type targets.
-   Identify goals using the new unique identifier column in the goals grid of a portfolio plan.
-   Export roadmaps to PowerPoint for a date range of up to 3 years, extended from 1 year.
-   Improved program-level portfolio planning with general enhancements.

 Fixed

 -   Resolved an issue where users were unable to switch views for a demand record in Demands in Portfolio Planning Workspace.
-   Resolved an issue where selecting a single score indicator visualization on a dashboard displayed the entire record list instead of the filtered subset.
-   Resolved an issue where CPAAM efforts were not generated for unassigned resource assignments of the Task type.
-   Resolved an issue where the bottom bar of the record preview in the Roadmap view shifted when selecting a button.
-   Resolved an accessibility issue in Scenario Planning where the info icon aria-label was hardcoded as 'simulation mode'.

</td></tr><tr><td>

Portfolio Planning Core

</td><td>

5.13.6

</td><td>

Fixed

 Resolved an issue where users were unable to switch views for a demand record in Demand Workspace. The root cause was a scheduled job configuration issue.

</td></tr><tr><td>

Portfolio Planning integrations for Shared Infrastructure

</td><td>

3.12.3

</td><td>

Changed

 Updated supporting components for fixes in Strategic Planning Workspace and Portfolio Planning Workspace.

</td></tr><tr><td>

Portfolio Planning with PPM, Agile 2.0, and SAFe

</td><td>

4.7.4

</td><td>

Fixed

 Resolved an issue where view rules did not work on demands in Strategic Planning Workspace and Portfolio Planning Workspace.

</td></tr><tr><td>

Privacy Management Advanced

</td><td>

23.1.0

</td><td>

New

 -   Implemented platform directive to support mixed AI native SKU support.
-   Upgraded NowLLM to Gemma model for improved performance.

</td></tr><tr><td>

Privacy Management Prime

</td><td>

23.1.0

</td><td>

New

 -   Implemented platform directive to support mixed AI native SKU support.
-   Upgraded NowLLM to Gemma model for improved performance.

</td></tr><tr><td>

Process Automation Designer

</td><td>

29.7.10

</td><td>

New

 See the ideal path at a glance - Playbook stage and activity pickers now show conditional steps, so playbook users know which steps will run next.

 Fixed

 Playbook diagramming issues related to decision activity and stage rendering.

</td></tr><tr><td>

Process Mining

</td><td>

29.7.15

</td><td>

Fixed: Project findings migrated to Australia along with criteria between steps - RCA works on child entity for MDM projects - Breakdown percentages in the Opportunity Details Page is now relative to the finding scope - Mining issue with an error when a filter condition is applied on a reference-field breakdown.

</td></tr><tr><td>

Process Mining for external data

</td><td>

29.5.10

</td><td>

A version update.

</td></tr><tr><td>

Process Mining Workspace Components

</td><td>

29.7.15

</td><td>

Components to support process mining.

</td></tr><tr><td>

Product Catalog Management Core

</td><td>

20.2.0

</td><td>

Fixed

 -   Catalogs and categories now sort correctly by their configured display order.
-   Resolved an issue where renewal reconfigurations could incorrectly change contract line actions when only system-managed fields differed.
-   Improved catalog search performance and fixed a filtering issue for catalog hierarchies.
-   Fixed an issue preventing offering display names from being indexed for semantic search.

</td></tr><tr><td>

Project Workspace

</td><td>

7.7.3

</td><td>

New

 -   Configure which L2 menu items are visible for each project type in Project Workspace to provide tailored layouts and streamlined navigation.
-   View all project tasks assigned to you or created by you directly from your employee slate. Expand the list and load task details as needed.
-   Preview the tasks generated or extracted during the project plan generation flow on the Project Workspace home page and planning page. When an Excel document is provided, it is prioritized for task extraction over PDF, Word, and PowerPoint files.

 Changed

 -   The header now stacks elements and adapts its alignment at up to 200% zoom. Beyond 200% zoom, toolbar actions are grouped into drop-down lists for a better screen fit.
-   When a demand is converted to a project, the current offset is updated to keep assignment dates consistent, preventing auto-sync events and preserving assignment integrity.
-   The start date of a project task can no longer be moved later than the earliest actual time entered on the task, keeping task timelines accurate and preventing assignment sync errors.
-   Resource assignment data on the planning page is now retrieved based on the resource assignment toggle, improving the relevance of the data displayed.

 Fixed

 -   Resolved an issue where negative lag values entered when adding a dependency in Project Workspace were saved as zero.
-   Resolved an issue where saved project status reports appeared blank after the template was modified and published.
-   Resolved an issue where Project Workspace export logs did not correctly record exports to XML or Microsoft Project formats.

</td></tr><tr><td>

prompt-management

</td><td>

3.0.2

</td><td>

New

 -   Prompt filter management APIs are now available. Users can link and unlink prompt filters using new POST and DELETE endpoints, including an additional DELETE API that removes prompt filter records by prompt and filter value.
-   Prompt filter descriptions are now configurable. Each filter value can include a description explaining its purpose and expected prompt format, surfaced in category responses.

 Changed

 Prompt filter delete endpoint updated. The API name and 'Not found' success message have been revised for clarity.

</td></tr><tr><td>

Public Sector Digital Services AI Agent Collection

</td><td>

2.1.1

</td><td>

Changed

 Updates made for AI native SKUs.

</td></tr><tr><td>

Query Generation

</td><td>

7.0.1

</td><td>

New

 -   Formula Indicator Support.
-   Add Gemma 4 26B A4B IT Model Support.
-   Fix entity graph fragmentation in the Query Generation semantic layer.

</td></tr><tr><td>

Query Orchestrator

</td><td>

1.4.0

</td><td>

Fixed

 Fixed an issue where the Skill Config field appeared empty in the Execute Skill step of the 'Execute compound query on KG' subflow following a platform conversion.

</td></tr><tr><td>

Recommended Actions for Security Operations

</td><td>

2.3.7

</td><td>

Fixed

 Resolved the issue where Pro Plus and Enterprise Plus entitled users couldn't use some features when any Native SKU app was installed.

</td></tr><tr><td>

Record - vertical

</td><td>

23.1.2

</td><td>

New

 Form headers on vertical record pages update in real time. When users change a field value in the vertical form template for a record type with grouped secondary values, the header refreshes immediately to show the new value.

</td></tr><tr><td>

Resource Management Workspace

</td><td>

5.11.1

</td><td>

New

 -   End a resource assignment earlier than the planned end date. This action is available for assignments with resource data and works across Project Workspace, Resource Management Workspace, and Demand workspace.
-   View and manage resource assignments directly from the Demand Workspace.

 Fixed

 -   Users can now change the resource table name on the resource card.
-   Realign assignments to task is disabled for project hierarchy when autosync is enabled, and enabled for non-project tasks such as demand, epic.

</td></tr><tr><td>

Retail Core

</td><td>

7.6.1

</td><td>

New

 Retail organization lookups can now be scoped to the current user's hierarchy, via a reusable hierarchy path query on RetailOrganizationUtilsSNC.

 Changed

 Task pages in the SPM-RO portal now show a flat breadcrumb trail showing Task name \(Home &gt; \[Store\] &gt; \[Project\] &gt; \[Task\]\) instead of showing Task number \(Home &gt; \[Store\] &gt; \[Project\] &gt; \[CSPRJTAGTASK0001032\]\).

 Fixed

 The All, Open, Closed, and Overdue tab labels in the Track Plan dashboard now display in the user's locale.

</td></tr><tr><td>

Retail MCP Server

</td><td>

1.0.1

</td><td>

New

 Retail MCP Server is now generally available \(GA\). It was previously available only as a Controlled Availability release.

 Removed

</td></tr><tr><td>

Roadmap UI Builder Component

</td><td>

22.14.3

</td><td>

Fixed

 Resolved an issue where the roadmap keyboard shortcut dialog did not describe the left and right arrow row-wrap behavior.

</td></tr><tr><td>

Sales and Order Management for Technology Provider - Advanced

</td><td>

1.0.10

</td><td>

AI-native SKU plugin.

</td></tr><tr><td>

Sales and Order Management for Technology Provider - Prime

</td><td>

1.0.9

</td><td>

AI-native SKU plugin.

</td></tr><tr><td>

Sales and Order Management for Telecommunications, Media and Technology - Advanced

</td><td>

1.0.10

</td><td>

AI-native SKU plugin.

</td></tr><tr><td>

Sales and Order Management for Telecommunications, Media and Technology - Prime

</td><td>

1.0.12

</td><td>

AI-native SKU app.

</td></tr><tr><td>

Sales and Order Management for Telecommunications - Advanced

</td><td>

3.0.4

</td><td>

Changed

 Enhanced the Intent-Driven Orchestration Agent to also generate a task plan template. Once marked Active, the template can be used for order orchestration and fulfillment for that product.

</td></tr><tr><td>

Sales and Order Management for Telecommunications - Prime

</td><td>

3.0.2

</td><td>

Maintenance release - dependency updates only.

</td></tr><tr><td>

Scan Engine

</td><td>

7.0.3

</td><td>

New

 -   Category-weighted Instance Health Score: The Instance Health Score now uses a category-weighted calculation across Security, Performance, Manageability, Upgradeability, and User Experience to provide a more representative view of overall instance health.
-   Consistent scoring across scan types: Full and Delta scans now use the same instance-wide counting scope, providing consistent score calculations across both scan types.
-   Human-readable finding numbers: Each scan finding now includes a unique, human-readable number, making findings easier to reference, track, and manage.

 Changed

 Faster On-Demand Definition Scans: On-Demand Definition Scans now evaluate only the files relevant to the selected definitions, improving scan performance and reducing processing time.

 Fixed

 -   Fixed an issue where the Fix with Now Assist button remained enabled when the associated skill was deactivated.
-   Fixed an issue where on-demand scan requests did not return the correct asynchronous response code.
-   Improved input validation and error handling for Scan Engine REST API endpoints.
-   Resolved a security vulnerability in the exception modal.
-   Added the missing access control for exception reason lookups.
-   Fixed an issue where dashboard links did not open correctly in Next Experience.

</td></tr><tr><td>

Security Exposure Management Workspace

</td><td>

30.8.2

</td><td>

Fixed

 An issue where the Unassigned findings section on Cloud Security Overview drilled through without the cloud-asset filter, causing a count mismatch with the underlying list.

</td></tr><tr><td>

Security Support Common

</td><td>

30.7.1

</td><td>

Fixed

 -   Resolved the null pointer error for EmailUserReportedPhishing.
-   Resolved the issue where the Approver Level Groups field defaulted to the False Positive Approver role when the Approval Rule field was empty on Exception Management levels.

</td></tr><tr><td>

Service Catalog AI Core

</td><td>

1.1.3

</td><td>

Fixed

 Minor defect fixes.

</td></tr><tr><td>

Service Graph Experience

</td><td>

1.0.2

</td><td>

Widgets that support functionality for Stale CI remediation, De-duplication CI remediation, and Impact analysis.

</td></tr><tr><td>

ServiceNow AI Lens

</td><td>

8.2.0

</td><td>

Changed

 Enhanced performance and responsiveness in the capture workflow.

</td></tr><tr><td>

ServiceNow AI Lens Core

</td><td>

8.2.0

</td><td>

Changed

 Enhanced performance and responsiveness in the capture workflow.

</td></tr><tr><td>

ServiceNow Cowork

</td><td>

1.0.7

</td><td>

New

 Initial ServiceNow Store release for ServiceNow Cowork.

</td></tr><tr><td>

ServiceNow EmployeeWorks Web App Base

</td><td>

2.4.6

</td><td>

-   View tasks and approvals across the EmployeeWorks Web App assistant, along with the Tasks and Requests page. It includes delegated and customer-defined task types, with actions that could be completed in split view.
-   Browse topics on the mobile app as an employee. Choose from different topic templates to organize and present content as the service owner.
-   Set a single corner-radius style from the Admin Console to apply consistent branding across cards, buttons, and form fields in EmployeeWorks for your organization.

</td></tr><tr><td>

ServiceNow IDE

</td><td>

5.1.1

</td><td>

New

 ServiceNow Studio supports the Delegated admin role for ServiceNow Otto for app summary generation.

 Changed

 -   Performance improvements and maintenance.
-   Update sets and changes linked to source control both now display in the Changes tab, with clear tracking paths for both options and support for simultaneous update set and source control use.

 Deprecated

 The newly redesigned ServiceNow Studio went through several iterations before the replatform onto VS Code that occurred in March 2026. All versions before the replatform have been deprecated. Previously, turning off Build Agent returned you to the pre-VS Code version of ServiceNow Studio. Now, it stays on the VS Code version and turns off Build Agent.

</td></tr><tr><td>

ServiceNow Otto Agents for requestor

</td><td>

3.7.9

</td><td>

Fixed

 The Approval assistance AI agent now correctly executes the 'Checklist Generation' tool. Errors caused by missing Search Profile name or Portal Suffix have been resolved. The agent is accessible for foundation users, and approval assistance agents are enabled for teams. XML formatting and metadata in skill configuration files have been corrected, and display user names are now shown in the list of tools. Checklist Generation preconditions have been enriched, and error handling has been improved to ensure a profile is provided when required.

 Removed

 The AI asset subscription record has been removed. The Approval assistance agent is now discoverable and usable on the instance, and agent subscription falls back to Foundation.

</td></tr><tr><td>

ServiceNow Otto AI Agents

</td><td>

9.1.6

</td><td>

New

 Extra verification for sensitive voice actions: Your voice-enabled agents can now ask callers to confirm their identity before taking a sensitive action, such as accessing account details or completing a protected request - so higher-risk steps get an added layer of protection. Turn it on when you configure your voice agent in Agent Studio.

 Fixed

 -   Agent's current version now included in update sets. Update sets now correctly capture the agent's current version, so exports reflect the version you're actually working with.
-   Cleaned up tool records in update sets. Update sets no longer include leftover references to tools that were excluded from the set, keeping exported content consistent.

 Changed

 Past evaluation runs are now easier to access from an agent's configuration page. The Past Runs view now includes both previous test runs and evaluation runs.

</td></tr><tr><td>

ServiceNow Otto AI web agent

</td><td>

34.0.3

</td><td>

Changed

 Adaptive desktop actions now support version 4.6 of Claude Sonnet. It is now the default model for adaptive desktop actions.

</td></tr><tr><td>

ServiceNow Otto context menu

</td><td>

3.10.4

</td><td>

New

 -   ServiceNow Otto diagnostic tool enhancements. Users can now access an improved diagnostic tool that checks user access roles and provides clearer error handling for restricted operations. The tool surfaces actionable steps for resolving access denials and accurately displays skill configuration statuses.
-   Citation enhancements in modal dialogs. When accessing citations within ServiceNow Otto, opened inside a modal in UI16 or SOW, clicking a citation link now opens it in a new tab while keeping the modal open for continued interaction.
-   Gemma 4 model support and auto evaluation. The system now supports running and validating auto evaluation for the Gemma 4 model, enabling expanded capabilities for Now LLM integrations.
-   Claude Opus 4.6 and GPT 5 mini validation. The system now validates Claude Opus 4.6 and GPT 5 mini models for ServiceNow Otto context menu capabilities.

 Changed

 -   Component enhancements for ServiceNow Otto context menu The color of the ServiceNow Otto context menu otto icon now updates to text primary when it is non-interactive, improving clarity for users.
-   Prompt configuration update for Now LLM. All ServiceNow Otto context menu capabilities on the legacy Now LLM definition now use the Gemma 4 26B A4B model, replacing the previous llmgenericsmall model.

 ServiceNow Otto context menu still supports citations, but common actions like Shorten and Elaborate will no longer support citations once you start refining the output of a skill. Even when we do copy to clipboard or call actions like Insert Action, the citations were previously stripped from the response. However, while refining-such as shortening three sentences to one sentence-citations were combined, but if that is not used later, it is an unnecessary cost to support it. Still, the initial skill output before refining will retain citations to show where the data was pulled from. So, in this case, the behaviour is the same.

</td></tr><tr><td>

ServiceNow Otto Conversational Data Collection

</td><td>

10.2.31

</td><td>

PRB2029691 resolved dynamic choice lists not loading properly.

</td></tr><tr><td>

ServiceNow Otto for Advanced Approval Management

</td><td>

1.3.0

</td><td>

-   Minor defect fix.
-   Renamed app to ServiceNow Otto for Advanced Approval Management.

</td></tr><tr><td>

ServiceNow Otto for AI Control Tower

</td><td>

25.0.3

</td><td>

ServiceNow Otto for AI Control Tower features for October release.

</td></tr><tr><td>

ServiceNow Otto for AIRC

</td><td>

23.1.1

</td><td>

New

 -   Implemented platform directive to support mixed AI native SKU support.
-   Upgraded NowLLM to Gemma model for improved performance.

</td></tr><tr><td>

ServiceNow Otto for AI Search

</td><td>

18.1.2

</td><td>

New

 Default embedding settings are now automatically configured when Now Assist is installed for the first time, streamlining initial setup for administrators.

 Changed

 Genius Results now use the embedding model and document match threshold defined in Semantic Search Configuration \(SSC\), helping maintain consistent search behavior across AI Search experiences. Custom thresholds configured for individual Genius Results continue to take precedence. Applies to Otto Summary, Actions, and Knowledge Base Article Genius Results, as well as related external content and group search experiences.

 Fixed

 -   Fixed an issue where short URL placeholders could affect unrelated URLs during AI-generated response processing. URL masking and link handling now work more accurately, helping preserve URL integrity.
-   The Multi Content Portal Response Bundle is now linked to AI Search for Next Search Definition by default, regardless of Now Assist Portal status, helping ensure a consistent search experience.

</td></tr><tr><td>

ServiceNow Otto for App Engine

</td><td>

30.2.1

</td><td>

Changed

 Maintenance release.

</td></tr><tr><td>

ServiceNow Otto for Cloud Cost Management

</td><td>

1.1.0

</td><td>

This release is to support the Gemma model and version refresh of the NowAssist platform to 13.1.0.

</td></tr><tr><td>

ServiceNow Otto for Collaborative Work Management \(CWM\)

</td><td>

7.1.0

</td><td>

Changed

 Gemma 4 26B A4B IT is now the default LLM \(large language model\) for ServiceNow Otto for Collaborative Work Management \(CWM\) skills, instead of the earlier Now LLM model.

</td></tr><tr><td>

ServiceNow Otto for Configuration Management Database \(CMDB\)

</td><td>

4.5.1

</td><td>

New Stale CI remediation at scale: Use the CMDB success advisor for Data Foundations to find stale CIs in principal classes, then apply the staleness agentic workflow to remediate them. The workflow defines a single staleness threshold, then automatically rediscovers stale CIs using activity signals such as changes and incidents. It flags discovery and Service Graph Connector schedule issues, then recommends life-cycle actions such as retirement, archival, or deletion. Apply actions to a full CI group, a subset, or ignore the recommendation.

 Fixed

 -   Performance enhancements for Impact Analysis.
-   Quality enhancements for CMDB Search.

</td></tr><tr><td>

ServiceNow Otto for Contract Analysis

</td><td>

1.1.0

</td><td>

Starting from this version, Gemma 4 26B A4B IT and Gemini 3.5 flash models are now available, providing enhanced AI capabilities for Software Asset Management.

</td></tr><tr><td>

ServiceNow Otto for Contract Management Pro

</td><td>

2.6.1

</td><td>

Fixed

 -   Fixed an issue where users with AI contract configuration roles could not see the field request table when configuring use case mappings in AI Admin Hub.
-   Review analysis cards in the Word Add-in now render correctly when variation details are unavailable, instead of failing to load.

</td></tr><tr><td>

ServiceNow Otto for Creator

</td><td>

29.7.2

</td><td>

Release notes tracked at individual product level.

</td></tr><tr><td>

ServiceNow Otto for CSM Complaint Case

</td><td>

2.3.2

</td><td>

Changed: Migrated Complaint Case Summarization GenAI skill configurations from legacy model aliases to versioned model IDs for the LLM Generic \(Now LLM / gemma\) and Google Cloud Vertex AI \(gemini\) providers.

</td></tr><tr><td>

ServiceNow Otto for Customer Service Management \(CSM\)

</td><td>

16.0.7

</td><td>

Changed

 CSM skills and configurations have been migrated to newer, more efficient AI models \(Gemini 3.5 Flash and Gemma\), delivering faster responses and improved cost optimization.

</td></tr><tr><td>

ServiceNow Otto for Enterprise Architecture \(EA\)

</td><td>

7.6.1

</td><td>

New

 -   Analyze how configuration items, such as databases, servers, and storage devices, affect application services, business applications, and business capabilities by using the Enterprise Architecture query agent.
-   Added support for Gemma 4, a ServiceNow-hosted open-weight model available through Now LLM Service, for ServiceNow Otto for Enterprise Architecture skills.
-   Configure the Business application insights skill in AI Admin Hub to generate insights automatically or only on request. With automatic insights, the business application record page and the application rationalization bubble chart side panel show insights as soon as they open.

</td></tr><tr><td>

ServiceNow Otto for Hardware Asset Management

</td><td>

5.1.0

</td><td>

Updates in this version:

 -   Fixed issues in mixed AI Native SKU scenarios.
-   Improved compatibility with third-party LLM models including Gemma.

</td></tr><tr><td>

ServiceNow Otto for Health and Safety

</td><td>

1.6.2

</td><td>

New

 Mixed AI-Native SKU entitlement support for Health and Safety AI features. Accounts holding both a legacy Pro Plus SKU and an AI-Native Health and Safety SKU can access all Health and Safety AI skills, including incident summarization and pattern recommendations. The entitlement check recognizes AI-Native subscriptions and grants access accordingly.

</td></tr><tr><td>

ServiceNow Otto for HR Service Delivery \(HRSD\)

</td><td>

13.6.4

</td><td>

New

 Employee Relations Case History summarizes past employee relations cases for an involved party.

 Changed

 This version has been enabled for mixed SKU environments.

</td></tr><tr><td>

ServiceNow Otto for Impact

</td><td>

7.0.6

</td><td>

Improved accuracy of AI-assisted fix for migrated Health scan definitions.

</td></tr><tr><td>

ServiceNow Otto for Integrated Risk Management

</td><td>

23.1.1

</td><td>

Changed

 Adding support for NowLLM gemma.

 Fixed

 Fixed skills not accessible due to AI native and Professional plus SKU.

</td></tr><tr><td>

ServiceNow Otto for IT Operations Management \(ITOM\)

</td><td>

2.9.7

</td><td>

New

 -   Updated AI model references to align with current ServiceNow naming standards and improve consistency across the Autonomous Operator workflow.
-   Migrated Alert Assist to Fluent. The em-gai scoped application now runs on the Fluent framework.
-   Switched the underlying model from Now LLM to Gemma.
-   Updated the Gemini model reference from gemini\_small to gemini-3.5 to reflect the current naming conventions.

 Fixed

 -   Improved authorization controls for the AMR-filter sync job.
-   Improved authorization controls for AI worker, alert rule, and agent configuration data.
-   Fixed an issue that caused the autonomous workflow availability check to fail when the Workforce module and ZTSD were not installed.
-   Updated AIOps AI specialist to use the Data Access and Resilience Engine \(DARE\), improving data handling compliance.
-   Fixed a cross-scope access error in setWorkflow when the watchdog cleared stuck em\_gai or em\_alert records.
-   Fixed an issue where Alert Insights incorrectly reported alerts as closed when auto-close was disabled.
-   Corrected insignificant-flow calculations for critical and major percentage thresholds.
-   Updated the Run Service Analysis subflow to enforce caller-level permissions during downstream operations.

</td></tr><tr><td>

ServiceNow Otto for IT Service Management \(ITSM\)

</td><td>

18.0.2

</td><td>

New

 Incident Analyzer

 Automatically investigates new incidents and writes a summary to the work notes:

 -   What happened, likely cause, and supporting evidence.
-   Who to contact and proposed assignment groups.
-   Potentially responsible CIs and changes.
-   Related incidents, events, and alerts.
-   Investigation gaps.

 -   Ships inactive. Admins can activate it and configure triggers; P1 and P2 incidents are the default scope.
-   Sections are omitted when the underlying data isn't available on the instance.
-   Each run consumes 4 assists.

 Changed

 Create and Edit Knowledge in the AI-native fulfiller experience

 Now compatible with UI 26, so fulfillers can create and update knowledge articles without leaving the experience.

 Gemma 4 model support and Now LLM deprecation

 -   Gemma 4 26B-A4B is now a supported ServiceNow-hosted model, including for self-hosted deployments. It is not the default model.
-   Gemma 4 replaces GPT-OSS for Guardian moderation. By default, Guardian logs only for agents and conversations and blocks for skills.
-   Now LLM models Apriel and GPT-OSS are deprecated and will not receive long-term support.

 Change AI Specialist guided conversational experience

 -   Asks for human input only when needed, such as when mandatory fields can't be auto-populated, risk exceeds a threshold, conflicts are detected, or policy requires approval.
-   Asks focused questions instead of presenting forms, and explains why input was needed.
-   All interactions are captured in the change record's work notes.

 Fixed

 Investigate and resolve ITSM incidents workflow

 -   Now runs after being duplicated to a subdomain with global scope.
-   No longer ends in a Terminated state or fails with a generic error.
-   The work notes tool no longer updates the wrong incident when incident numbers are duplicated.
-   No longer omits information in Dutch, French, Portuguese \(Brazil\), Spanish, Japanese, Italian, and German with certain models.
-   Instructions now reference the AI agent configured in the workflow.

 Change quality and assessment

 -   The Assess quality of a change request workflow no longer stalls waiting for confirmation when launched from the UI action.
-   The Change Quality Assessor agent now shows display names instead of internal field names, and saves internal values to the quality score table.
-   The Change Assessor workflow now validates the change record before running its tools.

 Incident classification and triage

 -   The Classify service and CI AI agent no longer overwrites populated Service, Service offering, or Configuration item fields.
-   The Triage and Categorize workflow no longer asks the user for input unexpectedly.

 Requested Item Summarization

 -   Summaries now match the requested item being viewed.
-   Summaries are no longer empty in Portuguese \(Brazil\) with Now LLM.

 Incident record experience

 -   The Assign button in Service Operations Workspace now generates hyperlinks.
-   The Now Assist modal now respects UI policies that make Assigned to optional.
-   Work notes bullet formatting no longer breaks when a field is changed and saved.
-   Incident Assist options now display in Japanese when that is the user's language.
-   Post Incident Report generation is faster.

 SME AI agents

 -   The SharePoint SME AI agent now reports a diagnosis with resolution pending when remedial action is disabled.
-   The Zscaler SME AI agent's Action Engagement tool no longer fails on invalid input format.

 Removed

</td></tr><tr><td>

ServiceNow Otto for Knowledge Management

</td><td>

31.13.8

</td><td>

Changed: AI model updates.

</td></tr><tr><td>

ServiceNow Otto for Manufacturing Commercial Operations \(MCO\)

</td><td>

5.1.0

</td><td>

Changed

 -   Introduction of new Open Weight Model: Gemma 4 26B-A4B.
-   The new Open Weight Model is now supported but is not designated as the default model for all ServiceNow Otto for Manufacturing Commercial Operations \(MCO\) capabilities.

</td></tr><tr><td>

ServiceNow Otto for Operational Sustainability

</td><td>

23.1.2

</td><td>

New

 AI capabilities are now available in Non - AI Native OSM SKUs.

</td></tr><tr><td>

ServiceNow Otto for Opportunity Management

</td><td>

1.2.4

</td><td>

Fixed

 -   Resolved an issue where Otto confirmed a field update as successful without actually saving the change.
-   Fixed inconsistent or empty results when querying open opportunities through Otto for certain agent roles.
-   Removed the 'Delete' action from the Opportunity AI Agent to prevent unintended record deletion.
-   Fixed failures when managing contacts through Otto.
-   Improved error handling when creating an opportunity for a non-existent account - the system now validates the account earlier in the conversation instead of failing at the end.

</td></tr><tr><td>

ServiceNow Otto for Order Management

</td><td>

2.4.1

</td><td>

Changed

 Order Management AI agents and skills are now accessible to customers with Professional Plus entitlements when ServiceNow Otto for platform plugins are installed. The following agents and skills are supported:

 -   Order Exception Voice AI Agent.
-   Invoice Dispute Support Assistant.
-   Invoice Dispute Voice Agent.
-   RMA AI Agentic workflow.
-   Invoice Dispute Assist.

</td></tr><tr><td>

ServiceNow Otto for Platform

</td><td>

13.1.1

</td><td>

Application captures updated plugin dependency list.

</td></tr><tr><td>

ServiceNow Otto for Platform Advanced

</td><td>

3.1.1

</td><td>

Application captures updated plugin dependency list for Advanced Tier SKUs.

</td></tr><tr><td>

ServiceNow Otto for Platform Foundation

</td><td>

3.1.1

</td><td>

Application captures updated plugin dependency list for Foundation Tier SKUs.

</td></tr><tr><td>

ServiceNow Otto for Platform Prime

</td><td>

3.1.1

</td><td>

Application captures updated plugin dependency list for Prime Tier SKUs.

</td></tr><tr><td>

ServiceNow Otto for Privacy Management

</td><td>

23.1.1

</td><td>

New

 -   Implemented platform directive to support mixed AI native SKU support.
-   Upgraded NowLLM to Gemma model for improved performance.

</td></tr><tr><td>

ServiceNow Otto for Public Sector Digital Services \(PSDS\)

</td><td>

2.6.1

</td><td>

Changed

 Updates made for AI native SKUs.

</td></tr><tr><td>

ServiceNow Otto for Sales and Order Management for Telecommunications

</td><td>

5.0.2

</td><td>

Changed

 Enhanced the Intent-Driven Orchestration Agent to also generate a task plan template. Once marked Active, the template can be used for order orchestration and fulfillment for that product.

</td></tr><tr><td>

ServiceNow Otto for Sales Automation

</td><td>

1.2.2

</td><td>

Fixed

 -   Version support upgraded to BP0 and AP6.
-   Dependent app version updated to support same engines.

</td></tr><tr><td>

ServiceNow Otto for Security Incident Response \(SIR\)

</td><td>

6.6.1

</td><td>

No functional change.

</td></tr><tr><td>

ServiceNow Otto for Service Quality

</td><td>

2.3.2

</td><td>

Fixed: Defect fixes.

</td></tr><tr><td>

ServiceNow Otto for Setup

</td><td>

6.0.5

</td><td>

Changed

 Supported products \(October Release\).

 AI Native.

 -   ITSM \(Foundation, Advanced, Prime\).
-   CBS \(Foundation, Advanced, Prime\).
-   ITOM \(Foundation, Advanced, Prime\).
-   ESM \(Foundation\).
-   Employee Slate.
-   AICT.
-   HAM \(Advanced, Prime\).
-   CCM \(Advanced\).
-   Sourcing and Procurement \(Foundation, Prime\).
-   HRSD \(Foundation, Advanced, Prime\).
-   SPM \(Advanced, Prime\).
-   OT \(Foundation, Advanced, Prime\).
-   EAM \(Advanced\).

 Pro Plus.

 -   ITSM \(Pro Plus\).
-   HRSD \(Pro Plus\).
-   ITOM \(Pro Plus\).
-   SAM \(Pro Plus, Enterprise Plus\).
-   HAM \(Pro Plus\).
-   Sourcing and Procurement \(Plus\).
-   SPM \(Pro Plus\).

 Non-AI.

 -   ITOM \(Standard, Enterprise, Professional\).
-   SPM \(Standard, Professional\).
-   Security Vault.
-   SAM \(Professional, Enterprise\).
-   HAM \(Professional\).
-   CCM \(Professional\).
-   Sourcing and Procurement \(Standard, Professional\).
-   EAM \(Professional\).
-   Impact.

</td></tr><tr><td>

ServiceNow Otto for Setup Core

</td><td>

5.0.5

</td><td>

Changed

 Supported products \(October Release\).

 AI Native.

 -   ITSM \(Foundation, Advanced, Prime\).
-   CBS \(Foundation, Advanced, Prime\).
-   ITOM \(Foundation, Advanced, Prime\).
-   ESM \(Foundation\).
-   Employee Slate.
-   AICT.
-   HAM \(Advanced, Prime\).
-   CCM \(Advanced\).
-   Sourcing and Procurement \(Foundation, Prime\).
-   HRSD \(Foundation, Advanced, Prime\).
-   SPM \(Advanced, Prime\).
-   OT \(Foundation, Advanced, Prime\).
-   EAM \(Advanced\).

 Pro Plus.

 -   ITSM \(Pro Plus\).
-   HRSD \(Pro Plus\).
-   ITOM \(Pro Plus\).
-   SAM \(Pro Plus, Enterprise Plus\).
-   HAM \(Pro Plus\).
-   Sourcing and Procurement \(Plus\).
-   SPM \(Pro Plus\).

 Non-AI.

 -   ITOM \(Standard, Enterprise, Professional\).
-   SPM \(Standard, Professional\).
-   Security Vault.
-   SAM \(Professional, Enterprise\).
-   HAM \(Professional\).
-   CCM \(Professional\).
-   Sourcing and Procurement \(Standard, Professional\).
-   EAM \(Professional\).
-   Impact.

</td></tr><tr><td>

ServiceNow Otto for Smart Assessment Engine

</td><td>

23.1.1

</td><td>

Changed

 Gemma 4 26B A4B is now set as default model under Now LLM model provider for Smart Assessment Response Assist skill.

</td></tr><tr><td>

ServiceNow Otto for Software Asset Management \(SAM\)

</td><td>

12.0.0

</td><td>

-   The Evaluate Software Reclamation AI Agent now evaluates software subscription removal candidates at both the integration profile and software model levels using Reclamation Summary data, providing deeper visibility into optimization opportunities.
-   Gemma 4 26B A4B IT and Gemini 3.5 flash models are now available, expanding AI capabilities for Software Asset Management workflows.

</td></tr><tr><td>

ServiceNow Otto for Strategic Portfolio Management

</td><td>

9.12.0

</td><td>

New

 -   Project Data Quality Index \(DQI\): This will allow Project Managers to assess the completeness and accuracy of project data across multiple dimensions and receive actionable suggestions to improve the data quality of projects.
-   Introduced Tour Guides to Ask Otto and AI Identified Risks which help users to discover and leverage AI-powered capabilities while walking them through the streamlined process.

 Changed

 -   Project Plan Generation includes a preview stage to review AI-extracted or generated tasks from Excel documents before creating projects.
-   Goal Insights now supports Maintain type targets \(Maintain Above, Maintain Below, Maintain Constant\) for goals focused on sustaining performance levels along with enhanced prompts.

</td></tr><tr><td>

ServiceNow Otto for Talent

</td><td>

1.9.3

</td><td>

Updated talking points skill to support Mixed AI Native SKU approach for Now Assist.

</td></tr><tr><td>

ServiceNow Otto for Telecommunications, Media and Technology \(TMT\)

</td><td>

6.0.17

</td><td>

1. Fluent conversion of APP.

 2. Success Play Recommendation Skill.

 3. Executive Briefing on Executive portfolio dashboard.

 4. Engagement Insights and briefing Skill.

</td></tr><tr><td>

ServiceNow Otto for Telecommunications Service Management

</td><td>

2.4.0

</td><td>

 

</td></tr><tr><td>

ServiceNow Otto for Third-Party Risk Management

</td><td>

23.1.1

</td><td>

Changed

 -   Updated AI model configuration to support Gemma 4 26B A4B for issue recommendation and summarization skills.
-   Updated skill configuration prompts for TPRM issue summarization with Now LLM Generic model.
-   Updated AI asset subscription records to support Mixed AI Native SKU licensing.

</td></tr><tr><td>

ServiceNow Otto for Unified Security Exposure Management

</td><td>

6.0.0

</td><td>

Fixed

 Enhancements to the Security Exposure 360 agentic workflow prompt to improve workflow persistence.

</td></tr><tr><td>

ServiceNow Otto for Virtual Agent

</td><td>

23.0.6

</td><td>

New

 -   Admins can configure tool access permissions for Model Context Protocol \(MCP\) server integrations. When adding or editing an MCP server configuration, admins can select tools and set their access status as Allowed, Disallowed, or Require Approval. The interface supports bulk permission changes, search, authentication flows, and error handling for tool loading.
-   Admins can add Web applications as a communication channel under WebRTC. The WebRTC section supports adding new web applications, including an Engagement Messenger section with configuration links and read-only fields for Voice Service ID, Orchestrator Host URL, and WebSocket URL.
-   Admins can make retry attempts editable directly on the Caller Verification screen. The retry attempt value is now adjustable within the UI, improving workflow efficiency.
-   Caller verification supports a discard changes pop-up when refreshing configuration. Users are prompted to confirm before discarding unsaved changes during configuration refresh.
-   Caller verification includes a refresh configuration option. Admins can refresh configuration directly from the Assistant Designer page.
-   Caller verification now displays updated error messages for configuration issues. The UI provides clearer guidance for missing identification methods and factors.
-   Voice assistant handles form validation errors in Caller Verification. Mandatory fields not filled trigger a red card error, improving clarity.
-   Admins can select language input using DTMF or voice options. The Language and Voice page includes a new section for input selection, with links to advanced settings and retry/goodbye message configuration.
-   Admins can decouple the Testing UI from the Assistant 'Active' state. Testing can be initiated without activating the assistant, and the test button is enabled regardless of activation status.
-   Admins can turn off parametric memory by default for all assistants. Scripts auto-populate parametric memory policy, ensuring consistent behavior.
-   Admins can now create a switch to enable custom SIP options in communication channels. The custom SIP option appears in the UI when enabled.
-   ServiceNow Otto panel premium chat is the default for eligible new customers, with Now LLM restrictions. Premium chat uses V2 orchestrator, and eligibility checks prevent Now LLM selection when premium chat and V2 orchestrator are enabled.

 Changed

 Embedded script for Service Portal UI has been updated. Parameter names, OAuth client ID handling, call button visibility, and optional widget parameters have been revised for improved reliability and clarity.

 Fixed

 -   Search sources in Assistant Designer now correctly reflect the 'Include in AI Response' profile configuration. The system pulls from the correct table column, opens links in new tabs, and passes unit tests.
-   Unified Recommendations now allow cross-scope calls for typeahead suggestions, improving integration reliability.
-   The 'Response feedback' page now works for existing assistants after upgrade. Script fixes ensure feedback attributes are correctly handled.
-   The 'View org chart' feature in ServiceNow Otto for Virtual Agent now loads correctly when accessed through a custom URL or domain. The system uses relative URLs and sets appropriate roles.
-   Doc QnA now marks deflection logs as 'response provided/resolved' after uploading an attachment with a question. The fix extends to all relevant topic representations and ensures logs are updated when user input is provided.
-   Duplicate create asset modal components have been eliminated from the codebase. Only one shared modal component is used across conversation-studio and nowassist-va repositories.

 Removed

 -   The role-based configuration from the MCP Server page is removed. The role column and related logic have been eliminated, simplifying server management and ensuring backward compatibility.
-   The Web applications section in Assistant Designer is no longer controlled by a system property. The property has been removed, and the section is always available.

</td></tr><tr><td>

ServiceNow Otto for Voice Agents

</td><td>

6.1.2

</td><td>

New

 Enhanced tool-level security for voice agents with Step-Up Authentication- Sensitive tools can now require elevated, action-bound identity verification, such as Okta Push, SMS, or TOTP, before execution rather than relying solely on caller verification at the start of a session. Access Control List \(ACL\) entries are automatically removed when step-up authentication is disabled or the agent is deleted.

 Removed

</td></tr><tr><td>

ServiceNow Studio

</td><td>

30.1.3

</td><td>

This app is a dependency of ServiceNow Studio + ServiceNow IDE. Please see release notes for parent app.

</td></tr><tr><td>

Setup Hub

</td><td>

4.0.4

</td><td>

Changed

 Supported products \(October Release\).

 AI Native.

 -   ITSM \(Foundation, Advanced, Prime\).
-   CBS \(Foundation, Advanced, Prime\).
-   ITOM \(Foundation, Advanced, Prime\).
-   ESM \(Foundation\).
-   Employee Slate.
-   AICT.
-   HAM \(Advanced, Prime\).
-   CCM \(Advanced\).
-   Sourcing and Procurement \(Foundation, Prime\).
-   HRSD \(Foundation, Advanced, Prime\).
-   SPM \(Advanced, Prime\).
-   OT \(Foundation, Advanced, Prime\).
-   EAM \(Advanced\).

 Pro Plus.

 -   ITSM \(Pro Plus\).
-   HRSD \(Pro Plus\).
-   ITOM \(Pro Plus\).
-   SAM \(Pro Plus, Enterprise Plus\).
-   HAM \(Pro Plus\).
-   Sourcing and Procurement \(Plus\).
-   SPM \(Pro Plus\).

 Non-AI.

 -   ITOM \(Standard, Enterprise, Professional\).
-   SPM \(Standard, Professional\).
-   Security Vault.
-   SAM \(Professional, Enterprise\).
-   HAM \(Professional\).
-   CCM \(Professional\).
-   Sourcing and Procurement \(Standard, Professional\).
-   EAM \(Professional\).
-   Impact.

</td></tr><tr><td>

Setup Hub Common

</td><td>

6.0.3

</td><td>

Changed

 Supported products \(October Release\).

 AI Native.

 -   ITSM \(Foundation, Advanced, Prime\).
-   CBS \(Foundation, Advanced, Prime\).
-   ITOM \(Foundation, Advanced, Prime\).
-   ESM \(Foundation\).
-   Employee Slate.
-   AICT.
-   HAM \(Advanced, Prime\).
-   CCM \(Advanced\).
-   Sourcing and Procurement \(Foundation, Prime\).
-   HRSD \(Foundation, Advanced, Prime\).
-   SPM \(Advanced, Prime\).
-   OT \(Foundation, Advanced, Prime\).
-   EAM \(Advanced\).

 Pro Plus.

 -   ITSM \(Pro Plus\).
-   HRSD \(Pro Plus\).
-   ITOM \(Pro Plus\).
-   SAM \(Pro Plus, Enterprise Plus\).
-   HAM \(Pro Plus\).
-   Sourcing and Procurement \(Plus\).
-   SPM \(Pro Plus\).

 Non-AI.

 -   ITOM \(Standard, Enterprise, Professional\).
-   SPM \(Standard, Professional\).
-   Security Vault.
-   SAM \(Professional, Enterprise\).
-   HAM \(Professional\).
-   CCM \(Professional\).
-   Sourcing and Procurement \(Standard, Professional\).
-   EAM \(Professional\).
-   Impact.

</td></tr><tr><td>

Setup Hub Config

</td><td>

6.0.2

</td><td>

Changed

 Supported products \(October Release\).

 AI Native.

 -   ITSM \(Foundation, Advanced, Prime\).
-   CBS \(Foundation, Advanced, Prime\).
-   ITOM \(Foundation, Advanced, Prime\).
-   ESM \(Foundation\).
-   Employee Slate.
-   AICT.
-   HAM \(Advanced, Prime\).
-   CCM \(Advanced\).
-   Sourcing and Procurement \(Foundation, Prime\).
-   HRSD \(Foundation, Advanced, Prime\).
-   SPM \(Advanced, Prime\).
-   OT \(Foundation, Advanced, Prime\).
-   EAM \(Advanced\).

 Pro Plus.

 -   ITSM \(Pro Plus\).
-   HRSD \(Pro Plus\).
-   ITOM \(Pro Plus\).
-   SAM \(Pro Plus, Enterprise Plus\).
-   HAM \(Pro Plus\).
-   Sourcing and Procurement \(Plus\).
-   SPM \(Pro Plus\).

 Non-AI.

 -   ITOM \(Standard, Enterprise, Professional\).
-   SPM \(Standard, Professional\).
-   Security Vault.
-   SAM \(Professional, Enterprise\).
-   HAM \(Professional\).
-   CCM \(Professional\).
-   Sourcing and Procurement \(Standard, Professional\).
-   EAM \(Professional\).
-   Impact.

</td></tr><tr><td>

Setup Hub Content

</td><td>

6.0.4

</td><td>

Changed

 Supported products \(October Release\).

 AI Native.

 -   ITSM \(Foundation, Advanced, Prime\).
-   CBS \(Foundation, Advanced, Prime\).
-   ITOM \(Foundation, Advanced, Prime\).
-   ESM \(Foundation\).
-   Employee Slate.
-   AICT.
-   HAM \(Advanced, Prime\).
-   CCM \(Advanced\).
-   Sourcing and Procurement \(Foundation, Prime\).
-   HRSD \(Foundation, Advanced, Prime\).
-   SPM \(Advanced, Prime\).
-   OT \(Foundation, Advanced, Prime\).
-   EAM \(Advanced\).

 Pro Plus.

 -   ITSM \(Pro Plus\).
-   HRSD \(Pro Plus\).
-   ITOM \(Pro Plus\).
-   SAM \(Pro Plus, Enterprise Plus\).
-   HAM \(Pro Plus\).
-   Sourcing and Procurement \(Plus\).
-   SPM \(Pro Plus\).

 Non-AI.

 -   ITOM \(Standard, Enterprise, Professional\).
-   SPM \(Standard, Professional\).
-   Security Vault.
-   SAM \(Professional, Enterprise\).
-   HAM \(Professional\).
-   CCM \(Professional\).
-   Sourcing and Procurement \(Standard, Professional\).
-   EAM \(Professional\).
-   Impact.

</td></tr><tr><td>

SGC Central

</td><td>

2.7.9

</td><td>

Resolved an issue where the Continue button remained inactive after an import schedule was activated in the Configure import schedule step, which prevented users from proceeding with the setup.

</td></tr><tr><td>

sn-experiment-ui

</td><td>

1.1.20

</td><td>

-   New: Centralized feature-flag-driven record gating is now available.Product teams can register records for gating using a shared mapping table and API, enabling consistent feature flag control across platforms without custom logic. Teams can hide or show records based on feature flags and implement gating in their own business rules.
-   Changed: Feature rollout to general availability is now managed with enhanced filtering and opt-in behavior. Features reaching GA are enabled by default, hidden from the Feature Preview Program, and instance patch and hotfix version details are now included in filtering. Boolean values are correctly handled in context APIs.

</td></tr><tr><td>

sn-task-planner

</td><td>

22.16.1

</td><td>

New

 End a resource assignment using the End Assignment option in the resource assignment context menu. Select a new end date and resource status in the modal to update the assignment. Planned effort and the heatmap are recalculated automatically, and actuals remain unchanged.

 Changed

 -   When the resource assignment toggle is enabled, the resource sync icon is hidden and the Resource Assignee column is read-only. Column loading now accounts for the resource panel state for improved consistency.
-   The start date of a project task can no longer be moved later than the earliest actual time entered on the task. An error message appears if an update violates this rule, keeping assignments with actuals in sync.

</td></tr><tr><td>

Software Asset Management

</td><td>

4.1.8

</td><td>

This release lays the groundwork for the AI reclamation specialist capability and resolves defects affecting domain separation, software lifecycle reporting, SQL Server reconciliation, ESXi software installation status, and license metric result savings calculations-ensuring consistent, reliable system behavior across these areas.

</td></tr><tr><td>

Software Asset Management AI Advanced

</td><td>

2.7.0

</td><td>

Starting from this version, the Evaluate Software Reclamation AI Agent evaluates removal candidates at the integration profile and software model levels using Reclamation Summary data, providing deeper visibility into optimization opportunities.

</td></tr><tr><td>

Software Asset Management AI Prime

</td><td>

2.7.0

</td><td>

Starting from this version, the Evaluate Software Reclamation AI Agent evaluates removal candidates at the integration profile and software model levels using Reclamation Summary data, providing deeper visibility into optimization opportunities.

</td></tr><tr><td>

SOM for Manufacturing Advanced

</td><td>

4.0.0

</td><td>

This app will be hidden on the store. No listing content is applicable for this store app.

</td></tr><tr><td>

SOM for Manufacturing Prime

</td><td>

4.0.0

</td><td>

This app will be hidden on the store. No listing content is applicable for this store app.

</td></tr><tr><td>

SPM Enterprise-Wide Deployment

</td><td>

1.1.0

</td><td>

New

 -   Map dashboards to partitions in Demand Management to provide tailored layouts and settings for each partition. Administrators and users can view and manage dashboard-partition associations within the application.
-   Added partition support for portfolio and project mappings in the Portfolio Project \(pm\_m2m\_portfolio\_project\) table.
-   Users now see only the partitions they have access to when selecting from the Partition drop-down list in Demand Workspace, ensuring accurate visibility based on permissions.

</td></tr><tr><td>

SPM Planning Attributes Core

</td><td>

1.19.1

</td><td>

New

 -   Resource board in Demand records. Demand Managers and users can access the 'Resources' tab within Demand records to view and manage resource assignments.
-   Resource Managers receive smart default end dates when ending assignments. When ending a resource assignment, the End Assignment modal now automatically calculates a default end date based on current date, start date, actuals, and the associated task's planned end date.

 Fixed

 -   Errors are displayed during resource assignment operations if assignments are not aligned with the associated task. The system checks for planning item dates and alignment, ensuring assignments remain consistent with task details.
-   'Realign assignments to demand' function to correctly handle assignment, realignment, addressing previous issues with timezone handling, and to check actuals.

</td></tr><tr><td>

Subscription Management v2

</td><td>

6.6.0

</td><td>

Version update for backend only, with no customer-facing changes.

</td></tr><tr><td>

Technology Advanced

</td><td>

1.0.14

</td><td>

SKU Application Plugin - No code delivered.

</td></tr><tr><td>

Technology Foundation

</td><td>

1.0.17

</td><td>

AI Native SKU plugin.

</td></tr><tr><td>

Technology Prime

</td><td>

1.0.14

</td><td>

AI native SKU app.

</td></tr><tr><td>

Telecommunications, Media and Technology - Advanced

</td><td>

1.0.13

</td><td>

AI Native SKU plugin.

</td></tr><tr><td>

Telecommunications, Media and Technology - Foundation

</td><td>

1.0.15

</td><td>

SKU Application Plugin - No code delivered.

</td></tr><tr><td>

Telecommunications, Media and Technology - Prime

</td><td>

1.0.15

</td><td>

Its AI native SKU app.

</td></tr><tr><td>

Telecommunications Advanced

</td><td>

2.4.1

</td><td>

Maintenance only.

</td></tr><tr><td>

Telecommunications Foundation

</td><td>

2.4.1

</td><td>

Maintenance only.

</td></tr><tr><td>

Telecommunications Prime

</td><td>

2.4.1

</td><td>

Maintenance only.

</td></tr><tr><td>

Third-party Risk Management Advanced

</td><td>

23.1.0

</td><td>

Changed

 -   Updated AI model configuration to support Gemma 4 26B A4B for issue recommendation and summarization skills.
-   Updated skill configuration prompts for TPRM issue summarization with Now LLM Generic model.
-   Updated AI asset subscription records to support Mixed AI Native SKU licensing.

</td></tr><tr><td>

Third-party Risk Management Professional Plus

</td><td>

23.1.0

</td><td>

Changed

 -   Updated AI model configuration to support Gemma 4 26B A4B for issue recommendation and summarization skills.
-   Updated skill configuration prompts for TPRM issue summarization with Now LLM Generic model.
-   Updated AI asset subscription records to support Mixed AI Native SKU licensing.

</td></tr><tr><td>

Threat and alert data feeds for Crisis Management

</td><td>

12.1.1

</td><td>

Added knowledge graph support for BCM apps.

</td></tr><tr><td>

TSOM - Advanced

</td><td>

3.0.5

</td><td>

There are no specific features on agentic AI part added to TSOM as part of this release.

</td></tr><tr><td>

TSOM - Prime

</td><td>

3.0.5

</td><td>

No AI related changes or new features.

</td></tr><tr><td>

UI Generation

</td><td>

29.2.14

</td><td>

Changed

 Default LLM model for UI Generation updated to third-party provider. The system now uses a third-party large language model \(LLM\) as the default for UI Generation skills, replacing the previous default. This change applies to all relevant workflows and configurations.

 'Now Assist' renamed to 'ServiceNow Otto' in Australia region. All UI references and plugin names have been updated to reflect the new branding, and these changes are now available in the Australia region through a minor release.

</td></tr><tr><td>

Unified Developer Core

</td><td>

30.1.2

</td><td>

Maintenance release.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Advanced

</td><td>

2.3.0

</td><td>

Dependencies updates. No new features for this release.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Foundation

</td><td>

2.3.0

</td><td>

Dependencies updates. No new features for this release.

</td></tr><tr><td>

Unified Security Exposure Management \(USEM\) - Prime

</td><td>

2.3.0

</td><td>

Dependencies updates. No new features for this release.

</td></tr><tr><td>

Universal MCP Client

</td><td>

1.1.3

</td><td>

MCP Client APIs now support product-level identification and telemetry. Users can now specify a product when interacting with MCP Client APIs, enabling tracking and aggregation of usage across products. Telemetry events are emitted for both MCP operations and tool invocations, allowing measurement of adoption and usage. Each operation and tool call generates a corresponding telemetry event, capturing product, method, server, status, and tool name.

</td></tr><tr><td>

Value dashboard for AI Control Tower

</td><td>

7.0.9

</td><td>

-   Added support for Domain Separation in AICT Value.
-   Product Owners can now easily identify and work with the AI systems and key metrics that matter most to them.

</td></tr><tr><td>

Value Engine

</td><td>

7.0.9

</td><td>

-   Added support for Domain Separation in AICT Value.
-   Product Owners can now easily identify and work with the AI systems and key metrics that matter most to them.

</td></tr><tr><td>

Vulnerability Response

</td><td>

30.9.2

</td><td>

New

 -   Admins can now preview exception, assignment, classification, remediation target, calculator, auto-close, and CI lookup rules before applying them. The preview option displays the impact of rule conditions, allowing users to verify affected records and adjust rules as needed.
-   Remediation plan details are now fully automated in workspace and classic views. All fields, actions, related lists, and state transitions are covered by automated tests, ensuring consistent validation and reliability.
-   Admins can now manually select assignment groups when creating remediation tasks. Findings can be reassigned using manual group selection before remediation task creation.
-   Admins can now automate classification rules front-end test cases. Identified scenarios are fully automated for improved reliability.

 Fixed

 -   Fixed an issue that required the Vulnerability Admin role to view the Exposure and Vulnerability Assessment icons in the Unified Security Exposure Management workspace.
-   Fixed an issue that prevented the 'Transit to Closed' business rule from moving vulnerable items to the Closed state.
-   Fixed an issue where the Microsoft Security Response Center \(MSRC\) integration removed all proposed solutions when an attachment exceeded approximately 5 MB.
-   Fixed an issue that allowed a past Until date for vulnerable items closed as Closed - False Positive.
-   Corrected a dialog tab order so the Next button now follows the Cancel button as expected.
-   Improved accessibility across the application with enhanced keyboard navigation, screen reader support \(including state announcements, dialog context, and heading semantics\), focus management, and icon button labeling.

</td></tr><tr><td>

Vulnerability Response Common

</td><td>

30.6.4

</td><td>

New

 Added a new Modify Risk approval rule type, enabling administrators to define approval workflows for risk adjustment requests and prevent duplicate processing of findings.

 Changed

 Updated the 'Until date for Risk reduction' field label to 'Until date for Risk change' to reflect that risk modifications now include both reductions and adjustments.

</td></tr><tr><td>

Vulnerability Response Common Workspace

</td><td>

30.9.2

</td><td>

New

 Added preview functionality for admin rules to display the number of applicable findings before applying them.

 Fixed

 Fixed incorrect risk score calculations in admin rule evaluation.

</td></tr><tr><td>

Vulnerability Response Integration with CISA

</td><td>

30.2.7

</td><td>

Fixed

 For large environments, eliminated unnecessary lookups and reduced NVD sync times by consolidating per-entry EPSS score roll-ups into a batched process.

</td></tr><tr><td>

Workplace Core

</td><td>

2.29.9

</td><td>

New

 New API to support artificial intelligence platforms.

 Fixed

 -   The arrival time when registering guests was not updated correctly as the time format preference omitted seconds.
-   In some cases, the redirect actions on location directory cards were not working as expected.
-   Earlier, signs of life were not displayed on certain maps.
-   Security fixes.

 Removed

</td></tr><tr><td>

Zero Touch Service Desk

</td><td>

3.3.3

</td><td>

New

 -   Dynamic agent template stays aligned with the current schema: The dynamic agent template's instructions and supporting scripts now stay in sync with the current template schema.
-   Document retrieval tool is now a configurable Flow Action: The document retrieval tool runs as a configurable Flow Action instead of an embedded script, so it can be inspected and adjusted without code changes. Also adds agentic-context ID tracking.

 Changed

 Routing criteria delete ACL now enforced: Any worker manager could delete routing criteria records that the delete access rules should have blocked. The delete data broker now enforces the sn\_ztsd\_routing\_decision\_criteria delete ACL instead of bypassing it.

 Fixed

 -   Licensing tier now enforced at execution: AI agents that were correctly hidden by the mixed AI Native SKU rules could still be executed by users whose licensing tier didn't include them. The ZTSD trigger path now enforces the Now Assist AI Native tier check, so a hidden agent can no longer be run.
-   Reassignment and escalation template posts correctly on the supplier portal: The AI worker was failing to post its reassignment and escalation response template on the supplier portal. A typo in a step input was preventing the template from resolving; it now posts as expected.
-   Case resolution text included in AI Specialist quality scoring: Case resolution text was missing from AI Specialist quality scoring, so cases weren't judged on the same resolution data as incidents. Scoring now reads the correct resolution field, so cases and incidents are evaluated consistently.
-   Knowledge base and catalog citations restored in AI Specialist responses: AI Specialist responses were missing knowledge base article and catalog references. The citation input has been corrected and now reads from a synchronously written execution record, so references resolve reliably.
-   Save Activity Notes reports its real outcome: The Save Activity Notes tool reported success even when it had failed to post a note. Failure paths now return the actual outcome to the caller instead of a success message.

</td></tr></tbody>
</table>|App name|Version number|Last updated|
|--------|--------------|------------|
|@devsnc/behavior-form-intent-translator|29.0.9|2026-03-12|
|@devsnc/behavior-list-intent-translator|29.0.9|2026-03-12|
|@devsnc/behavior-uibtk-media|29.6.6|2026-09-10|
|@devsnc/behavior-uibtk-supporting-records|29.6.6|2026-09-10|
|@devsnc/behavior-ui-interaction|29.4.8|2026-09-10|
|@devsnc/library-uibtk-caching|29.6.6|2026-09-10|
|@devsnc/library-uibtk-commons|29.6.6|2026-09-10|
|@devsnc/library-uibtk-macroponent|29.6.6|2026-09-10|
|@devsnc/library-uibtk-screen|29.6.6|2026-09-10|
|@devsnc/library-uibtk-undo-redo|29.6.6|2026-09-10|
|@devsnc/library-uibtk-uxvalue|29.6.6|2026-09-10|
|@devsnc/library-uibtk-ux-value-resolver|29.6.6|2026-09-10|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-customer-information|25.2.0|2026-03-12|
|@devsnc/sn-devops-pipeline|21.0.5|2022-08-04|
|@devsnc/sn-feedback|2.0.0|2025-12-11|
|@devsnc/sn-help-setup|29.0.0|2026-03-12|
|@devsnc/sn-interaction-builder|29.4.16|2026-09-10|
|@devsnc/sn-list-selector|26.1.3|2026-03-12|
|@devsnc/sn-uibtk-actionable-list-item|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-builder-in-builder|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-client-state-config-panel|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-conditional-renderer|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-content-tree-picker|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-create-page|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-data-navigator|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-diff-renderer|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-domain-picker|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-draggable-dialog|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-draggable-list|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-editor-header|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-element-context-menu|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-element-navigator|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-element-properties-configuration-pane|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-events-pane|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-experience-assistant|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-extension-point-pane|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-features-catalog-modal|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-form-factor-controls|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-formula-builder|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-icon|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-instance-config-editor|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-is-hidden-property-input|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-json-navigator|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-loader|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-mcp-event-definitions-config-pane|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-mcp-props-config-pane|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-menu-elements|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-minimized-dialogs-dropdown|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-modal|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-param-row|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-placeholder|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-preset-pane|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-props-pane|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-replace-component|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-scope-picker|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-script-config-panel|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-shelf-pane|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-site-map|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-stage-preview|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-stage-scale-controls|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-style-pane|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-style-provider|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-style-select|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-tabs|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-test-values-editor|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-text-link|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-toolbox|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-transaction-alert|29.6.6|2026-09-10|
|@devsnc/sn-uibtk-viewport-config-panel|29.6.6|2026-09-10|
|@devsnc/sn-ui-interaction-modals|29.4.8|2026-09-10|
|@devsnc/sn-vtb|26.0.0|2025-12-11|
|@devsnc/uibtk-api|29.6.6|2026-09-10|
|@devsnc/uibtk-uxf-assets|29.6.6|2026-09-10|
|@servicenow/sn-builder-core|29.5.14|2026-09-10|
|@servicenow/sn-cb-api|27.2.29|2025-05-01|
|@servicenow/sn-cb-asset-picker|27.2.29|2025-05-01|
|@servicenow/sn-cb-commons|27.2.29|2025-05-01|
|@servicenow/sn-cb-events-navigator|27.2.29|2025-05-01|
|@servicenow/sn-cb-experiences|27.2.29|2025-05-01|
|@servicenow/sn-cb-presets|27.2.29|2025-05-01|
|@servicenow/sn-cb-property-navigator|27.2.29|2025-05-01|
|@servicenow/sn-cb-property-pane|27.2.29|2025-05-01|
|@servicenow/sn-cb-slide-modal|27.2.29|2025-05-01|
|@servicenow/sn-cb-theme-picker|27.2.29|2025-05-01|
|@servicenow/sn-cb-usage|27.2.29|2025-05-01|
|@servicenow/sn-component-builder|29.5.13|2026-09-10|
|@servicenow/sn-controller-builder|29.5.10|2026-09-10|
|@servicenow/sn-preset-builder|29.5.10|2026-09-10|
|360 degree relationship visualization|22.3.0|2026-06-16|
|ACC Admin Workspace|1.0.0|2025-12-11|
|Access Analyzer|6.0.6|2026-05-21|
|Access Management Automation|2.1.0|2023-12-07|
|Access Management Flow Wizards|1.0.1|2021-09-16|
|Accounts Payable Invoice Processing|13.2.7|2026-09-10|
|Accounts Payable Operations integration with Document Intelligence|13.2.5|2026-09-10|
|ACL Assessment for Reports|3.1.2|2025-01-30|
|Action Status Automation|2.0.0|2026-03-12|
|Activity Timer|1.0.2|2026-03-12|
|Admin Center|6.2.1|2026-08-07|
|Admin Experience for Hardware Asset Management|1.0.0|2026-09-10|
|Admin Experience Framework|5.3.0|2026-03-12|
|Admin Workspace for Service Providers \(SPs\)|1.1.4|2025-07-31|
|Adobe Experience Platform Spoke|2.2.0|2025-01-02|
|Adobe Sign Spoke|2.7.2|2025-10-16|
|Advanced AI Search Management Tools|8.0.1|2025-12-11|
|Advanced Appointment Booking|30.0.1|2026-03-12|
|Advanced Promotion Engine|4.2.1|2025-12-11|
|Advanced Recommended actions for ITSM|8.1.0|2025-09-10|
|Advanced Response Automation for Smart assessments|23.0.2|2026-09-10|
|Advanced Work Assignment for CSM|1.0.4|2026-03-12|
|Advanced Work Assignment for Legal Service Delivery|1.1.1|2025-06-05|
|Advanced Work Assignment for Source-to-Pay Operations|3.1.1|2025-12-11|
|Advanced Work Assignment for Supplier Lifecycle Operations|10.0.0|2026-09-10|
|AES Catalog Builder|28.2.1|2025-12-11|
|AES Catalog Builder Wizard|28.2.1|2025-12-11|
|AES Decision Table Builder Templates|4.0.0|2023-02-02|
|AES Decision Table Builder Wizard|4.0.0|2023-02-02|
|AES Flow Templates|28.2.1|2025-12-11|
|AES Flow Wizards|28.2.1|2025-12-11|
|AES Mobile Templates|28.2.1|2025-12-11|
|AES Mobile Wizards|28.2.1|2025-12-11|
|AES Notification Builder Component|28.2.1|2025-12-11|
|AES Portal UI Template|28.2.1|2025-12-11|
|AES Role Builder|28.2.1|2025-12-11|
|AES Role Builder Component|28.2.1|2025-12-11|
|AES Table Builder Wizard|28.2.1|2025-12-11|
|AES UI Template Wizards|28.2.1|2025-12-11|
|AES Workspace UI Template|28.2.1|2025-12-11|
|Agency Support Model|4.0.1|2026-09-10|
|Agency Support Model|4.0.1|2026-09-10|
|Agent Client Collector for Investigation|9.4.2|2026-09-10|
|Agent Client Collector for Security Incident Response|20.2.0|2023-05-04|
|Agent Client Collector for Visibility Content|2.0.4|2026-09-10|
|Agent Client Collector Framework|7.0.4|2026-09-10|
|Agent Client Collector Log Analytics|3.9.1|2025-12-11|
|Agent Client Collector Monitoring|3.16.1|2026-01-20|
|Agent Client Collector Spoke|1.1.5|2024-01-04|
|Agent Forecast|5.7.0|2025-12-11|
|Agentic Contact Center for Banking|1.4.5|2026-09-04|
|Agentic Contact Center for Insurance|1.3.3|2026-09-04|
|Agentic Usage Overview Dashboard|1.2.0|2026-09-10|
|Agent-Initiated Messaging Interface|1.0.22|2026-03-12|
|Agent Messaging Component|3.0.17|2026-03-12|
|Agent Workspace for HR Case Management|4.6.2|2026-08-07|
|Agile Development v2|1.1.0|2023-02-02|
|Agile Integrations Common|1.4.0|2025-12-11|
|Aha! Spoke|1.7.2|2026-01-20|
|AI agents and skills for Quote Management|3.0.1|2026-07-09|
|AI Agents for ACC|1.0.3|2026-04-09|
|AI Agents for Core Business Suite|3.3.2|2026-08-07|
|AI Agents for Core Business Suite|3.3.2|2026-08-07|
|AI Agents for CSM - Complaint Case|1.5.1|2026-08-07|
|AI Agents for Discovery|3.2.2|2026-09-10|
|AI Agents for Domain Separation|1.0.5|2026-04-09|
|AI Agents for Employee Experience|2.3.4|2026-08-07|
|AI Agents for Retail Service Management|1.6.0|2026-09-10|
|AI Agents for Service Exchange Provider|1.1.12|2026-08-13|
|AI agents for Synthetic Monitoring|1.4.4|2026-07-09|
|AI Agents for Universal Request|1.1.3|2026-09-10|
|AI Agents Platform Usecase|1.0.5|2025-03-12|
|AI Authoring for Catalog Builder|8.0.3|2026-09-10|
|AI Dashboard Insights|1.3.4|2026-08-07|
|AI Data Explorer|5.2.7|2026-09-10|
|AI Enhanced Recommended Actions|1.0.5|2026-08-07|
|AI Experience Framework|1.2.4|2026-09-07|
|AI Experience Framework Skills|1.4.4|2026-09-10|
|AIOps Dashboards|26.2.0|2025-12-11|
|AIOps Experience|27.0.0|2026-03-12|
|AI Platform skills|3.2.2|2026-09-10|
|AI Readiness Evaluation|1.5.2|2026-09-10|
|AI Risk and Compliance Content|21.1.1|2025-12-11|
|AI sales activity association|1.2.1|2026-09-10|
|AI Search Admin Console|9.2.4|2026-09-04|
|AI Search for Customer Portals|1.1.0|2025-12-11|
|AI Search For Next Experience|5.0.2|2026-02-05|
|AI Search RAG|7.0.3|2026-09-10|
|AI Search Spoke|2.0.3|2023-09-20|
|AI slot-filling for catalog items|1.4.5|2026-08-07|
|AI Specialists for Security Incident Response|1.0.10|2026-09-10|
|AIS ZTSD Gemma|1.0.6|2026-09-10|
|AI Trace Collector|3.1.3|2026-09-10|
|AI Troubleshooting|4.1.4|2026-08-07|
|Aleph Alpha Spoke|1.0.2|2025-01-30|
|Alert Rules Management|18.15.9|2026-06-16|
|Amazon Alexa Spoke|1.1.0|2024-11-07|
|Amazon CloudWatch Spoke|1.0.2|2022-12-01|
|Amazon Connect Spoke|1.2.0|2025-03-12|
|Amazon DynamoDB Spoke|1.0.1|2022-09-01|
|Amazon EBS Spoke|1.0.2|2023-09-20|
|Amazon EC2 Spoke|1.4.0|2025-09-10|
|Amazon Elastic Container Service Spoke|1.0.2|2023-09-07|
|Amazon RDS Spoke|1.0.5|2025-06-05|
|Amazon Route 53 Spoke|1.0.2|2022-12-01|
|Amazon S3 Spoke|1.2.1|2024-09-10|
|Amazon SNS Spoke|1.1.0|2023-09-07|
|Amazon SQS Spoke|1.0.1|2025-01-02|
|Amazon VPC Spoke|1.0.3|2023-09-07|
|Analytics Pack for Contract Management Pro|1.2.0|2025-05-01|
|Analytics Toolkit|8.4.3|2026-07-09|
|Analytics Toolkit|8.4.3|2026-07-09|
|Ansible Spoke|2.2.9|2024-12-05|
|API Insights|2.2.1|2025-12-11|
|API Notification Management|4.0.1|2025-12-11|
|API Service Graph Connector for Apigee X|2.2.2|2025-10-16|
|API Service Graph Connector for AWS API Gateway|2.2.0|2025-09-10|
|API Service Graph Connector for Azure API Management|2.2.0|2025-07-31|
|API Service Graph Connector for Kong Gateway|2.1.0|2025-10-16|
|API Service Graph Connector for Kong Konnect|1.0.0|2025-10-16|
|APO - Foundation|2.0.0|2026-09-10|
|APO - Prime|2.0.0|2026-09-10|
|App AutoUpgrade Client|1.0.0|2026-07-09|
|App Best Practices Shared|29.2.0|2026-06-16|
|App Collaboration Component|28.2.1|2025-12-11|
|App Engine Management Center|29.2.1|2026-06-16|
|App Engine Studio|28.2.1|2025-12-11|
|app-ent-data-map-components|1.0.0|2026-09-10|
|App Generation|28.3.12|2026-07-09|
|Applicant Center|8.0.2|2026-07-09|
|Application Common Configuration|29.0.8|2026-03-12|
|Application Insights|2.0.3|2021-11-18|
|Application Intake|29.2.1|2026-06-16|
|Application Portfolio Management integration with Policy and Compliance|1.0.3|2023-05-04|
|Application Portfolio Management integration with Risk Management|1.0.2|2023-05-04|
|Application Service Extensions|1.1.7|2024-11-07|
|Application spoke selector|1.6.0|2026-08-07|
|App Life Cycle AI Agents|29.5.2|2026-08-07|
|Appointment calendar component|28.1.1|2025-12-11|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|Approvals Hub integration with Workday|2.0.1|2025-07-31|
|App Shell Utils|29.0.0|2026-03-12|
|App Summary|29.4.0|2026-07-09|
|ArcSight ESM Event Ingestion for Security Operations|10.5.0|2025-12-11|
|ArcSight Logger Integration for Security Operations|10.4.1|2024-11-07|
|Aria Systems Spoke|2.1.2|2023-04-06|
|Asana Spoke|1.0.3|2024-08-01|
|Asset Audit Response|2.0.6|2026-09-10|
|Asset Audit Response AI Advanced|1.0.0|2026-04-09|
|Asset Audits|1.0.0|2026-03-12|
|Asset Management Common|16.0.0|2026-09-10|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management for mobile|27.0.2|2025-07-31|
|Asset Management - Procurement Integration|1.0.1|2024-11-07|
|Asset Security Posture Management|5.5.1|2025-12-11|
|Asset Shipments|1.0.0|2026-03-12|
|ATF Test Generator and Cloud Runner|3.2.1|2026-08-27|
|ATF troubleshooting agent|1.0.6|2026-03-12|
|Atlassian Administration Spoke|1.0.1|2025-01-30|
|Atlassian Jira Integration for Agile Development|2.3.2|2025-12-23|
|Atlassian Jira Integrations Common|2.4.2|2025-12-23|
|Attribute Pack|5.0.0|2025-07-31|
|Attribute Pack|5.0.0|2025-07-31|
|Attribute Pack|5.0.0|2025-07-31|
|Attribute propagation|9.4.3|2026-09-10|
|Attribute propagation|9.4.3|2026-09-10|
|Audio player component|27.3.1|2026-03-12|
|Authentication for conversational channels|1.1.0|2026-03-12|
|Automation Anywhere Spoke|1.2.1|2025-05-01|
|Automation Center|15.1.1|2026-08-07|
|AWH for AI Control Tower|3.4.0|2026-09-10|
|AWS Certificate Manager Spoke|1.0.1|2022-09-21|
|AWS CloudFormation Spoke|1.1.4|2024-03-20|
|AWS Elastic Beanstalk Spoke|1.0.3|2024-06-06|
|AWS Elastic Load Balancing Spoke|1.0.1|2022-09-01|
|AWS IAM Spoke|1.1.0|2023-07-06|
|AWS Lambda Spoke|1.1.3|2023-09-07|
|AWS OpsWorks Spoke|1.0.2|2023-09-20|
|AWS Translate Spoke|1.0.0|2022-11-03|
|Azure Active Directory User Mapping|1.11.0|2025-12-11|
|Basic Scoring for Smart Assessments|23.0.3|2026-09-10|
|BCM mobile app|9.1.3|2025-12-11|
|Beans.ai Spoke|29.0.7|2026-03-12|
|BigFix Inventory Spoke|1.5.4|2023-09-07|
|Blue Prism Spoke|1.0.2|2022-09-21|
|BMC Remedy Spoke|1.4.1|2024-10-03|
|Bot Interconnect|1.7.0|2025-07-31|
|Box Spoke|3.7.1|2026-06-26|
|Breadcrumb navigation demo|27.0.0|2025-06-05|
|Breakdown Data Grid UI Component|1.4.0|2023-05-04|
|Broadcom Rally Integration with DevOps|7.0.0|2026-06-16|
|Browser Extension for Employee Center|1.1.1|2025-12-11|
|Bubble trend|1.0.0|2025-05-01|
|Build Agent Glide Tools|1.0.10|2026-03-12|
|Business domain|23.0.2|2026-09-10|
|Business Location|5.7.3|2026-09-10|
|Business Object Core|2.1.0|2025-12-11|
|Business Object Core|2.1.0|2025-12-11|
|Business Portal|2.4.0|2026-06-16|
|Calendar component|27.0.1|2026-06-16|
|Calendly Spoke|1.2.0|2023-08-03|
|Capacity Management|4.1.0|2025-12-11|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Card data security|1.0.1|2025-07-31|
|Career Assessment|3.3.0|2026-06-16|
|Career Conversations|3.11.2|2026-08-07|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Mobile|1.2.0|2026-03-12|
|Care Team Portal|2.2.0|2026-03-12|
|Care Team Portal|2.2.0|2026-03-12|
|Care Team Portal|2.2.0|2026-03-12|
|Carousel component|28.0.1|2026-03-12|
|Case Digests|2.0.0|2026-03-12|
|Case lines and workflows|4.6.1|2026-09-10|
|Case Management for Invoice Operations|2.1.0|2026-09-10|
|Case Management for Invoice Operations|2.1.0|2026-09-10|
|Case Management for Invoice Operations|2.1.0|2026-09-10|
|Case Playbook for Complaints|9.1.1|2026-07-09|
|Case Playbook for Onboarding|8.1.0|2025-12-11|
|Case Playbook for Product Support|6.0.1|2025-07-31|
|Catalog Conversational Coverage|6.2.1|2026-09-10|
|CCG Content Pack|1.3.12|2024-11-07|
|CCO Dashboard|2.0.8|2025-12-11|
|CDM File Uploader|1.0.1|2023-11-02|
|CDO Dashboard|2.0.5|2025-12-11|
|Central Vulnerability Database|1.2.5|2026-09-10|
|Certificate Inventory and Management|4.5.0|2026-09-10|
|CFO Dashboard|2.0.1|2025-12-11|
|Change Management AI Orchestrator|1.0.4|2026-09-10|
|Change Management for Field Service|1.1.2|2025-01-02|
|Change Management for Service Operations Workspace|9.4.2|2026-09-10|
|Change Password Custom Component|1.3.0|2025-12-11|
|Channel Management|7.0.0|2025-12-11|
|Chat integration with Security Incident Management|1.2.10|2025-07-31|
|Chat Zoom Connector|1.0.6|2023-01-12|
|Checklist component|26.0.0|2025-12-11|
|Check Point Integration for Security Operations|10.4.10|2025-07-31|
|CHRO Dashboard|2.0.4|2025-12-11|
|CIO Dashboard|2.1.1|2025-12-11|
|Cisco Webex Meetings Spoke|2.3.3|2024-08-01|
|Cisco Webex Teams Spoke|2.3.6|2025-12-11|
|CISO Dashboard|2.0.5|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Claim Common|2.3.3|2025-12-11|
|Client Software Distribution 2.0|1.4.0|2025-12-11|
|CLI Metadata|1.1.2|2021-04-15|
|Cloud Access Interface|1.1.3|2026-06-23|
|Cloud Action Library|1.4.0|2024-11-07|
|Cloud Configuration Governance|1.6.0|2025-12-11|
|Cloud Cost Management|11.0.0|2026-09-10|
|Cloud Cost Management AWS|11.0.0|2026-09-10|
|Cloud Cost Management Azure|11.0.0|2026-09-10|
|Cloud Cost Management Core|11.0.0|2026-09-10|
|Cloud Cost Management GCP|11.0.0|2026-09-10|
|Cloud Cost Management Infra Stack|11.0.0|2026-09-10|
|Cloud Deployment Automation|1.0.3|2024-12-05|
|Cloud Discovery Workspace|1.7.1|2025-05-01|
|Cloud Flow Wizards|1.2.1|2022-08-24|
|Cloudify Spoke|2.1.1|2023-04-06|
|Cloud Insights Billing|6.0.1|2024-04-04|
|Cloud Insights Billing|6.0.1|2024-04-04|
|Cloud Integrations AWS|11.0.0|2026-09-10|
|Cloud Integrations Azure|11.0.0|2026-09-10|
|Cloud Integrations Core|11.0.0|2026-09-10|
|Cloud Integrations GCP|11.0.0|2026-09-10|
|Cloud Migration Assessment|1.4.0|2024-11-07|
|Cloud Security Posture Management|2.5.0|2024-02-01|
|Cloud Services Catalog|1.5.1|2025-12-11|
|Cloud Services Catalog Terraform Connector|1.9.1|2025-12-11|
|Cloud Spend Dashboard|1.0.3|2022-06-02|
|Cloud Spend Reports AWS|11.0.0|2026-09-10|
|Cloud Spend Reports Azure|11.0.0|2026-09-10|
|Cloud Spend Reports Core|11.0.0|2026-09-10|
|Cloud Spend Reports GCP|11.0.0|2026-09-10|
|Cloud Storage|6.1.0|2026-03-12|
|Cloud Workspace|2.2.0|2025-12-11|
|CMDB and CSDM Data Foundations Dashboards|4.2.0|2025-12-11|
|CMDB Application for APIs and CLI|1.0.1|2021-07-22|
|CMDB CI Class Models|1.94.3|2026-09-10|
|CMDB Page Templates|3.2.6|2026-06-16|
|Coaching With Learning|5.4.2|2026-03-12|
|Coaching with Learning Migration Utility|1.0.1|2021-09-16|
|Collaboration applications - common|1.1.0|2025-12-11|
|Collaboration Request|28.2.1|2025-12-11|
|Collaboration Services|3.12.2|2025-12-11|
|Collaboration Services for Service Operations Workspace|9.4.3|2026-09-10|
|Collaboration UI Component for Major Security Incident Management Workspace|1.2.1|2024-11-07|
|Collaborative Work Management|11.0.1|2026-09-10|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Commercial Lines Claims|4.4.0|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Commercial Lines Servicing|2.5.0|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Commercial Lines Underwriting|2.5.0|2026-03-12|
|Common Guidances|16.0.2|2026-09-10|
|Common Service Delivery|15.0.0|2026-09-10|
|Common UIB Wrapper Components|1.5.1|2025-12-11|
|Common Vendor Core|5.0.2|2026-09-10|
|Compatibility Management|6.7.0|2026-09-10|
|Compatibility Management|6.7.0|2026-09-10|
|Configurable Workspace for Order Management|16.1.0|2026-09-10|
|Configurable Workspace for Order Management|16.1.0|2026-09-10|
|Configuration Compliance|15.5.3|2025-12-11|
|Configuration Data Management|5.0.2|2024-03-20|
|Configuration Hub|1.0.11|2026-08-07|
|Configure, Price and Quote for Telecommunications, Media and Technology - Advanced|1.0.1|2026-04-09|
|Configure, Price and Quote for Telecommunications, Media and Technology - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Technology Provider - Foundation|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Advanced|1.0.2|2026-04-09|
|Configure, Price an Quote for Telecommunications - Foundation|1.0.1|2026-04-09|
|Confluence Cloud Spoke|1.2.6|2026-01-20|
|Confluent Kafka REST Proxy Spoke|1.0.0|2021-03-11|
|Contact card component|26.0.0|2025-12-11|
|Contact Center Integration Core|1.4.4|2025-12-11|
|Contact Tracing|1.30.0|2025-07-31|
|Content Engagement for Employee Center Pro|1.4.1|2026-03-12|
|Content Experiences|33.1.0|2026-07-09|
|Content Experiences|33.1.0|2026-07-09|
|Content library portal|4.1.1|2026-07-09|
|Content Pack for CMDB|2.1.1|2026-08-07|
|Content Publishing|37.3.3|2026-08-07|
|Context Menu Component for Configuration Data Management UI|1.2.1|2023-05-04|
|Context Rule Management|10.8.1|2026-09-10|
|Contract Management for Sales and Order Management|1.1.0|2025-12-11|
|Contract Management Pro|1.6.0|2025-12-11|
|Contract Management Pro for Legal Service Delivery|3.0.2|2025-12-11|
|Contract Management Pro MCP Server|1.0.4|2026-09-10|
|Contractor Service Center|1.0.7|2025-12-11|
|Contracts and Entitlement Workflows|13.0.0|2025-12-11|
|Contracts Core components|1.4.1|2025-07-31|
|Contract Workspace|1.7.2|2025-12-11|
|Conversational Analytics|9.3.1|2026-09-10|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Analytics UI Builder Components|3.0.5|2025-05-01|
|Conversational Appointment Booking Components|2.0.5|2023-09-07|
|Conversational Help|2.0.3|2026-03-12|
|Conversational Integration with Alexa|1.5.5|2024-08-01|
|Conversational Integration with Apple Messages for Business|1.3.0|2026-03-12|
|Conversational Integration with Facebook Messenger|3.0.8|2025-12-11|
|Conversational Integration with Google Business Messages|1.1.1|2024-02-01|
|Conversational Integration with Google Chat|2.0.4|2025-12-11|
|Conversational Integration with LINE|2.0.7|2025-01-30|
|Conversational Integration with Microsoft Teams|10.6.0|2026-08-07|
|Conversational Integration with Slack|6.1.0|2026-09-10|
|Conversational Integration with WhatsApp \(powered by Twilio\)|2.0.11|2025-12-11|
|Conversational Integration with Workplace from Facebook|5.0.1|2025-01-30|
|Conversational Interfaces - Diagnostics|2.2.1|2024-11-07|
|Conversational IVR with Amazon Connect|1.6.3|2025-07-31|
|Conversational SMS Integration with AWS End User Messaging|1.0.2|2025-01-30|
|Conversational SMS Integration with Twilio|4.2.4|2025-12-11|
|Conversational SMS Service Channel|2.0.23|2026-03-12|
|Conversational subflows and actions|30.0.4|2026-08-07|
|Conversation Improvement themes|1.0.8|2026-05-05|
|Core Business Suite|3.3.2|2026-08-07|
|Core Business Suite|3.3.2|2026-08-07|
|Core Business Suite Advanced|3.3.2|2026-08-07|
|Core Business Suite Advanced|3.3.2|2026-08-07|
|Core Business Suite Advanced for Finance|3.3.2|2026-08-07|
|Core Business Suite Advanced for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Advanced for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Advanced for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Advanced for Legal|3.3.2|2026-08-07|
|Core Business Suite Advanced for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Advanced for Workplace Services|3.3.3|2026-08-07|
|Core Business Suite Analytics|3.3.1|2026-08-07|
|Core Business Suite Analytics|3.3.1|2026-08-07|
|Core Business Suite for Finance|3.3.2|2026-08-07|
|Core Business Suite for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite for Human Resources|3.3.2|2026-08-07|
|Core Business Suite for Legal|3.3.2|2026-08-07|
|Core Business Suite For Source To Pay|3.3.2|2026-08-07|
|Core Business Suite For Workplace Service Delivery|3.3.3|2026-08-07|
|Core Business Suite For Workplace Service Delivery|3.3.3|2026-08-07|
|Core Business Suite Foundation|3.3.2|2026-08-07|
|Core Business Suite Foundation|3.3.2|2026-08-07|
|Core Business Suite Foundation for Finance|3.3.2|2026-08-07|
|Core Business Suite Foundation for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Foundation for Health and Safety|3.3.2|2026-08-07|
|Core Business Suite Foundation for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Foundation for Legal|3.3.2|2026-08-07|
|Core Business Suite Foundation for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Foundation for Workplace Services|3.3.3|2026-08-07|
|Core Business Suite Foundation for Workplace Services|3.3.3|2026-08-07|
|Core Business Suite Prime|3.3.2|2026-08-07|
|Core Business Suite Prime|3.3.2|2026-08-07|
|Core Business Suite Prime for Finance|3.3.2|2026-08-07|
|Core Business Suite Prime for Health and Safety|3.3.3|2026-09-10|
|Core Business Suite Prime for Human Resources|3.3.2|2026-08-07|
|Core Business Suite Prime for Legal|3.3.2|2026-08-07|
|Core Business Suite Prime for Source to Pay|3.3.2|2026-08-07|
|Core Business Suite Prime for Workplace Services|3.3.3|2026-08-07|
|Cornerstone Spoke|1.6.0|2026-07-09|
|Coupa Spoke|4.14.0|2025-10-16|
|COVID-19 Global Health Data Set|1.20.3|2024-05-09|
|CPQ - Advanced|1.0.1|2026-04-09|
|CPQ Config Agent A2A|1.1.7|2026-09-10|
|CPQ Configurator|1.4.0|2026-06-16|
|CPQ - Foundation|1.0.1|2026-04-09|
|CPQ Integration|3.3.0|2026-07-09|
|CPRO Dashboard|2.0.5|2025-12-11|
|Craft.co Integration for Supplier Lifecycle Operations|9.0.0|2026-09-10|
|Craft Spoke|1.0.0|2024-11-07|
|Creator Studio|28.2.1|2025-12-11|
|Creator Studio Configurations|28.2.1|2025-12-11|
|Creator Studio Configurations|28.2.1|2025-12-11|
|Credentials Core|1.2.0|2026-06-16|
|Credly Spoke|1.1.0|2026-06-16|
|Critical Event Management|1.2.5|2026-07-09|
|CRM API Core|7.4.1|2026-09-10|
|CRM Core|1.10.1|2026-09-10|
|CRM Flow Wizards|1.0.1|2023-04-06|
|CRM Outlook Add-in|1.2.1|2026-09-10|
|CRM Territory Extensions|2.0.3|2026-03-12|
|CRM Touchpoint|1.6.1|2026-09-10|
|CRO Dashboard|2.0.10|2025-12-11|
|CrowdStrike Falcon EDR Integration for Threat Intelligence Security Center|3.0.0|2024-11-07|
|CrowdStrike Falcon Host for Security Operations|10.4.5|2024-11-07|
|CrowdStrike Falcon Insight Integration for Security Operations|1.4.1|2026-01-20|
|CrowdStrike Falcon Sandbox Integration for Security Operations|11.0.10|2024-09-10|
|CrowdStrike Spoke|1.1.0|2025-01-30|
|CSC Content Pack|1.7.0|2025-12-11|
|CSM Account Hierarchy|30.0.3|2026-03-12|
|CSM Account Hierarchy|30.0.3|2026-03-12|
|CSM - Advanced|2.1.2|2026-08-07|
|CSM Contributor User|2.5.3|2026-09-10|
|CSM Data Classification|1.0.0|2025-07-31|
|CSM Extension for Proxy Contacts|2.0.0|2026-03-12|
|CSM - Foundation|2.1.2|2026-08-07|
|CSM - Prime|2.1.2|2026-08-07|
|Customer Contracts and Entitlements|15.0.1|2026-09-10|
|Customer Data Models for B2B2C|2.1.0|2025-07-31|
|Customer Discovery Hub|1.2.2|2026-07-09|
|Customer Engagement Sequences|2.0.1|2025-12-11|
|Customer Household Data Model|2.0.11|2026-09-10|
|Customer Install Base Characteristics|2.5.4|2026-09-10|
|Customer Install Base Management|4.10.3|2026-09-10|
|Customer Life Cycle Management Self Service|2.1.1|2025-12-11|
|Customer Life Cycle Management Workflows|5.1.1|2025-12-11|
|Customer Project Management|2.0.0|2026-03-12|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Request for Quote Data Model|1.0.0|2025-12-11|
|Customer Service Case Action Status|2.0.2|2026-06-16|
|Customer Service Case Types|4.5.3|2026-09-10|
|Customer Service Document Template|2.0.0|2026-03-12|
|Customer Service integration with Social Media Store|1.0.2|2026-03-12|
|Customer Service NLU Model for Virtual Agent Conversations|1.0.5|2026-03-12|
|Customer Service Portal|25.3.3|2026-06-16|
|Customer Service Problem Management|5.0.2|2025-12-11|
|Customer Service RMA AI Agents|1.1.4|2026-09-10|
|Customer Service Virtual Agent Conversations|1.0.5|2026-04-09|
|Customer Service with Request Management|2.1.0|2026-04-09|
|Customer Service with Service Management|2.0.1|2026-03-12|
|Customer Service with Service Portfolio Management \(SPM\)|2.0.1|2025-01-30|
|Customer Success Advanced|2.4.10|2026-07-09|
|Customer Success Management|6.6.3|2026-07-09|
|Cyber Physical Systems Control Tower Advanced|1.0.2|2026-09-10|
|Cyber Physical Systems Control Tower Foundation|1.0.2|2026-09-10|
|Cyber Physical Systems Control Tower Prime|1.0.2|2026-09-10|
|Cyber Physical Systems Operations Advanced|1.0.5|2026-09-10|
|Cyber Physical Systems Operations Foundation|1.0.5|2026-09-10|
|Cyber Physical Systems Operations Prime|1.0.5|2026-09-10|
|Cyber Physical Systems Security Advanced|1.0.5|2026-09-10|
|Cyber Physical Systems Security Foundation|1.0.5|2026-09-10|
|Cyber Physical Systems Security Prime|1.0.7|2026-09-10|
|Cybersecurity Executive Dashboard|2.4.3|2025-05-01|
|Dashboard and visualization export|1.4.1|2026-09-10|
|Data Collection for Oracle Global Licensing and Advisory Services|1.11.0|2025-12-11|
|Data Context Engine|3.3.2|2026-06-16|
|Data Context Engine|3.3.2|2026-06-16|
|Data Foundation Model|1.13.2|2026-09-10|
|Data Grid UI Component|26.0.13|2026-09-10|
|Data Loss Prevention Incident Response|2.2.2|2026-02-05|
|Data Model for Order Management|17.1.0|2026-09-10|
|Data Model for SBOM|4.2.1|2025-12-11|
|Data Model Navigator|1.1.3|2026-09-10|
|Data registry|23.0.1|2026-09-10|
|Data Relationships Framework|12.0.2|2026-09-10|
|DCNAM - Advanced|2.3.0|2026-09-10|
|DCNAM - Advanced|2.3.0|2026-09-10|
|Decision Builder|29.1.4|2026-04-09|
|Decision Table Builder|29.1.6|2026-04-09|
|DevOps Change Health Scan Content Pack|6.2.0|2025-12-11|
|DevOps Change Velocity|7.0.0|2026-06-16|
|DevOps Config|5.2.0|2024-11-07|
|DevOps Config Exporter Content Pack|2.3.0|2023-08-03|
|DevOps Config Policy Content Pack|1.6.0|2023-11-02|
|DevOps Data Model|7.0.0|2026-06-16|
|DevOps Feature Flag Integrations|7.0.0|2026-06-16|
|DevOps Flow Wizards|1.1.1|2022-09-21|
|DevOps Insights|7.0.0|2026-06-16|
|DevOps Integrations|7.0.0|2026-06-16|
|DevOps Integration with Argo CD|7.0.0|2026-06-16|
|DevOps Vulnerability Integrations|7.0.0|2026-06-16|
|DevOps Workspace|7.0.0|2026-06-16|
|DEX Application and Device Health|5.2.3|2026-09-10|
|DEX Content Playbook|5.2.2|2026-09-10|
|DEX Desktop Assistant|5.1.1|2026-08-07|
|DEX Desktop Assistant|5.1.1|2026-08-07|
|DEX Desktop Assistant|5.1.1|2026-08-07|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Microsoft 365|4.3.0|2026-06-16|
|DEX for Zoom|5.0.0|2026-07-09|
|DEX for Zoom|5.0.0|2026-07-09|
|DEX for Zoom|5.0.0|2026-07-09|
|DEX for Zoom|5.0.0|2026-07-09|
|DEX for Zoom|5.0.0|2026-07-09|
|DEX Self Service|5.1.1|2026-08-07|
|DEX Self Service|5.1.1|2026-08-07|
|Diagram Builder|30.0.0|2026-05-05|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Digital Experience Feedback Survey|5.0.0|2026-07-09|
|Digital Experience Score|5.1.1|2026-08-07|
|Digital Experience Score|5.1.1|2026-08-07|
|Digital Experience Score|5.1.1|2026-08-07|
|Digital Integration Management|1.6.4|2026-08-07|
|Digital Portfolio Management|7.4.1|2026-01-20|
|Digital Product Release|2.3.2|2025-12-11|
|Digital Product Release Data Model|2.4.0|2026-03-12|
|Digital Product Release Policy Content Pack|2.2.0|2025-07-31|
|Digital Product Release Workspace|2.3.0|2025-12-11|
|Digital Resilience Third-party Information Register|21.1.7|2025-12-11|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital Signature API|26.0.0|2024-08-01|
|Digital signature component|27.1.0|2025-07-31|
|Discovery Admin Workspace|1.17.0|2026-06-16|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Content Pack for US Regulations|1.1.3|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Mastercard|3.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Nacha|1.0.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|Dispute Rules Content Pack for Visa|5.5.0|2025-12-11|
|DLP Incident Response integration with ICAP|1.1.1|2026-01-20|
|DLP Incident Response integration with Microsoft|1.3.1|2026-01-20|
|DLP Incident Response integration with Netskope|1.2.1|2026-01-20|
|DLP Incident Response integration with Proofpoint|1.1.0|2025-12-11|
|DLP Incident Response integration with Symantec|1.3.1|2026-01-20|
|DocIntel Vision AI Agent|2.0.1|2026-06-16|
|Docker Spoke|2.3.4|2025-07-10|
|Document Approval App Template|28.2.1|2025-12-11|
|Document display component|27.0.0|2025-05-01|
|Document Flow Wizards|2.0.2|2022-09-21|
|Document Intelligence|8.0.9|2026-08-07|
|Document Intelligence Admin|4.1.0|2025-12-11|
|Document Intelligence for Accounts Payable Operations Content Pack|2.0.0|2025-12-11|
|Document Intelligence for Contract Management Content Pack|1.5.0|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Processor|1.8.6|2026-07-09|
|Document Service Framework for Google Drive|3.0.0|2025-07-31|
|Document Service Framework for OneDrive|3.0.0|2025-07-31|
|Document Template Integration with AdobeSign|1.7.0|2025-12-11|
|Document Template integration with DocuSign|1.7.1|2026-03-12|
|Document Templates|29.0.1|2026-07-09|
|DocuSign Activities for PAD|1.1.3|2023-01-12|
|Docusign eSignature Spoke|4.2.2|2026-02-05|
|Dropbox Business Spoke|1.0.5|2024-03-07|
|Dun and Bradstreet DirectPlus Spoke|1.0.0|2025-01-30|
|Dynamic Related Records for Configurable Workspace|25.7.0|2026-06-16|
|Elasticsearch Integration for Security Operations|10.3.4|2024-11-07|
|Email Interaction Core|1.0.3|2025-12-11|
|Email Interaction for CSM|1.5.0|2025-12-11|
|Emergency Alert App Template|28.2.1|2025-12-11|
|Emergency Exposure Management|1.27.0|2025-07-31|
|Emergency Outreach|1.34.0|2025-07-31|
|Emergency Self Report|1.21.0|2025-07-31|
|Employee Center for Microsoft Viva Connections|2.0.8|2025-07-31|
|Employee Center integration with Zoom|2.0.16|2025-12-11|
|Employee Center Pro|42.0.4|2026-07-09|
|Employee Center Pro Kiosk|2.3.4|2025-12-11|
|Employee Experience Foundation|30.0.3|2025-12-11|
|Employee experience taxonomy|28.2.5|2025-12-11|
|Employee Experience VA Components|1.0.0|2023-08-03|
|Employee Experience VA topics and topic blocks|1.1.2|2023-05-04|
|Employee Goals|1.4.3|2026-08-07|
|Employee Health Screening|1.28.0|2025-07-31|
|Employee Readiness Core|1.42.0|2025-12-11|
|Employee Readiness Surveys|1.5.3|2025-07-31|
|Employee Travel Safety|1.22.0|2025-12-11|
|Engagement dashboard for AI Control Tower|3.0.11|2025-12-12|
|Engagement Messenger|5.12.1|2026-01-20|
|Enterprise Architecture - Advanced|1.0.1|2026-06-16|
|Enterprise Architecture Cloud Assessment|1.0.1|2025-01-30|
|Enterprise Architecture - Prime|1.0.1|2026-06-16|
|Enterprise Asset Management Advanced|2.0.0|2026-09-10|
|Enterprise Asset Management for DCNAM|2.0.0|2026-09-10|
|Enterprise Asset Management for DCNAM Advanced|2.0.0|2026-09-10|
|Enterprise Asset Management for Facilities|1.0.0|2024-08-01|
|Enterprise Asset Management for Healthcare|2.0.0|2026-09-10|
|Enterprise Asset Management for Healthcare Advanced|2.0.1|2026-09-10|
|Enterprise Asset Management for Providers|1.0.0|2025-12-11|
|Enterprise Data Transform|1.0.2|2026-09-10|
|Enterprise Modeling and Visualization|6.2.2|2026-06-16|
|Enterprise Modeling Common|3.8.0|2026-06-16|
|Enterprise Portfolio|1.3.0|2025-12-11|
|Enterprise Service Management Integrations Framework|3.8.2|2025-07-31|
|Entitlements Verification|6.2.1|2026-09-10|
|Equifax Spoke|1.0.0|2023-08-03|
|ER integration with NAVEX|1.1.1|2024-02-01|
|ERP Customization Mining|7.0.5|2025-05-01|
|ERP Integration Framework|19.0.3|2026-06-16|
|ESG integration with DEX|21.1.0|2025-12-11|
|ESG Risk Management|21.0.1|2025-12-11|
|Ethoca Spoke|3.0.1|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Inquiry|1.4.0|2025-07-31|
|Event Management Connectors|2.18.2|2026-03-12|
|Event Management Core|23.16.0|2026-06-16|
|Event Registration App Template|28.2.1|2025-12-11|
|Expanded Model and Asset Classes|2.17.1|2026-09-10|
|Expense Pre-Approval Template|28.2.1|2025-12-11|
|Export to PowerPoint|2.3.0|2025-12-11|
|Export to PowerPoint for Application Portfolio Management|1.0.1|2024-02-01|
|Export to PowerPoint for Strategic Portfolio Management|1.4.2|2025-12-11|
|External Agent Management Util Pack|1.2.0|2025-07-31|
|External Content Connectors|9.0.6|2026-09-10|
|External Content Connectors Admin|9.0.6|2026-09-10|
|External Content Connectors Adobe Acrobat Sign|7.0.7|2026-05-28|
|External Content Connectors Adobe AEM|7.0.7|2026-05-28|
|External Content Connectors Aha Roadmaps|7.0.7|2026-05-28|
|External Content Connectors Amazon S3|7.0.7|2026-05-28|
|External Content Connectors Application Suite|7.0.7|2026-05-28|
|External Content Connectors Asana|7.0.7|2026-05-28|
|External Content Connectors Box|7.0.7|2026-05-28|
|External Content Connectors Confluence Cloud|7.0.7|2026-05-28|
|External Content Connectors Cornerstone|7.0.7|2026-05-28|
|External Content Connectors Docusign|7.0.7|2026-05-28|
|External Content Connectors Dropbox|7.0.7|2026-05-28|
|External Content Connectors FluidTopics|7.0.7|2026-05-28|
|External Content Connectors GitHub Enterprise Cloud|7.0.7|2026-05-28|
|External Content Connectors Gitlab|7.0.7|2026-05-28|
|External Content Connectors Google Drive|7.0.7|2026-05-28|
|External Content Connectors Hubspot|7.0.7|2026-05-28|
|External Content Connectors Jira Cloud|7.0.7|2026-05-28|
|External Content Connectors Lucid|7.0.7|2026-05-28|
|External Content Connectors Microsoft OneDrive|7.0.7|2026-05-28|
|External Content Connectors Microsoft Teams|7.0.7|2026-05-28|
|External Content Connectors Miro|7.0.7|2026-05-28|
|External Content Connectors Monday.com|7.0.7|2026-05-28|
|External Content Connectors Notion|7.0.7|2026-05-28|
|External Content Connectors SAP Document Management System|7.0.7|2026-05-28|
|External Content Connectors ServiceNow Instance|7.0.7|2026-05-28|
|External content connectors - ServiceNow Otto agent|1.2.0|2026-08-07|
|External Content Connectors Sharepoint Online|7.0.7|2026-05-28|
|External Content Connectors Slack|7.0.7|2026-05-28|
|External Content Connectors Smartsheet|7.0.7|2026-05-28|
|External Content Connectors SN Docs|9.0.6|2026-09-10|
|External Content Connectors Trello|7.0.7|2026-05-28|
|External Content Connectors Viva Engage|7.0.7|2026-05-28|
|External Content Connectors Wordpress|7.0.7|2026-05-28|
|External Content Connectors Workday|7.0.7|2026-05-28|
|External Content Connectors Workvivo|7.0.7|2026-05-28|
|External Content Connectors Zendesk|7.0.7|2026-05-28|
|External Content Connectors Zoom|7.0.7|2026-05-28|
|External Credential Storage and Management Application|1.3.1|2025-12-11|
|External Legal Service Center|1.2.0|2025-12-11|
|External Trigger Builder|1.1.0|2026-03-12|
|F5 BIG-IP Spoke|1.3.0|2025-09-10|
|Fallout management|8.0.0|2026-09-10|
|Fallout management|8.0.0|2026-09-10|
|Fallout management|8.0.0|2026-09-10|
|FDIH Dashboard|25.0.5|2024-11-07|
|Field Service Advanced Capacity and Reservations Management|30.0.3|2026-03-12|
|Field Service Capacity and Reservations Management|30.0.3|2026-03-12|
|Field Service Contractor for mobile|4.8.3|2026-03-12|
|Field Service Contractor Management|30.0.2|2026-03-12|
|Field Service Management AI agent collection|4.1.0|2026-09-10|
|Field Service Management for Telecommunications|3.0.2|2025-12-11|
|Field Service Management Intelligent Task Recommendations|29.0.6|2026-03-12|
|Field Service Management Scheduling Automations|29.0.6|2026-03-12|
|Field Service Management Virtual Conferencing Integration|30.0.0|2026-03-12|
|Field Service Manager Mobile|1.1.0|2026-04-09|
|Field Service Manager Workforce|1.1.0|2026-04-09|
|Field Service Marketplace|30.0.1|2026-03-12|
|Field Service Mobile|29.2.3|2026-08-07|
|Field Service NLU Model for Virtual Agent Conversations|1.3.0|2025-07-31|
|Field Service Quality Management|29.1.1|2026-03-12|
|Field Service Territory Planning|30.0.3|2026-03-12|
|Field Service Virtual Agent Conversations|1.7.0|2025-07-31|
|Field Service with Service Locations support|30.0.3|2026-03-12|
|File Explorer Component for Security Operations|1.2.13|2025-08-22|
|File Explorer for Security Incident Response|1.3.0|2025-12-11|
|Finance and Procurement - Foundation|2.0.0|2026-09-10|
|Finance and Procurement - Prime|2.0.0|2026-09-10|
|Finance Case Management|1.5.1|2026-06-16|
|Finance Common Architecture|15.0.0|2026-09-10|
|Finance Operations Workspace|1.5.1|2026-06-16|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Financial Services Business Deposit Operations|3.6.0|2026-03-12|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Financial Services Business Lifecycle|3.6.0|2026-03-12|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Financial Services Business Loan Operations|3.6.0|2026-03-12|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Financial Services Client Lifecycle|3.6.0|2026-03-12|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Financial Services Complaint Management|2.6.0|2026-03-12|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|Financial Services Credit Operations|3.7.0|2026-03-12|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Document Management|1.3.1|2022-02-03|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Financial Services Know Your Customer|2.5.0|2026-03-12|
|Financial Services Operations AI agent collection|4.3.1|2026-08-07|
|Financial Services Operations AI agent collection|4.3.1|2026-08-07|
|Financial Services Operations AI agent collection|4.3.1|2026-08-07|
|Financial Services Operations Core|12.4.2|2026-08-07|
|Financial Services Operations Core|12.4.2|2026-08-07|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with FRISS|1.3.0|2026-03-12|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Guidewire|1.0.1|2024-05-09|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Jack Henry jXchange|1.2.0|2025-07-31|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Mastercard|2.0.0|2025-12-11|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Socure|1.2.0|2026-03-12|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Operations Integration with Visa|3.4.0|2025-12-11|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Financial Services Payment Operations|2.6.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Financial Services Personal Deposit Operations|3.6.0|2026-03-12|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Personal Loan Operations|3.6.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Remote Tables|1.5.0|2026-03-12|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Financial Services Treasury Operations|3.6.0|2026-03-12|
|Firewall Audits and Reporting|1.8.0|2025-12-11|
|First Advantage Spoke|1.8.0|2025-11-06|
|Flow Designer - Designer|29.5.2|2026-08-07|
|Flow Designer GenAI|30.1.4|2026-09-10|
|Flow Diagramming|29.1.1|2026-08-07|
|Flow Execution Analysis|29.2.8|2026-06-16|
|Flow Generation|29.4.4|2026-08-07|
|Flow Summarization|29.4.4|2026-08-07|
|Flow Template Builder|1.0.9|2023-05-04|
|Flow Templates for Access Management|1.0.4|2023-04-06|
|Flow Templates for Cloud Services|1.2.3|2023-01-12|
|Flow Templates for CRM|1.0.3|2023-04-06|
|Flow Templates for DevOps|1.1.3|2023-04-06|
|Flow Templates for Document Management|1.1.10|2023-04-06|
|Flow Templates for HR Management|1.4.4|2023-04-06|
|Flow Templates for IntegrationHub Enterprise|1.0.2|2023-04-06|
|Flow Templates for Notifications|1.2.4|2024-06-06|
|Flow Templates for Service Desk|1.0.3|2023-04-06|
|Flow troubleshooting agent|1.0.12|2026-09-10|
|Forecast planning analysis|21.1.0|2025-12-11|
|Form data collector|2.3.1|2026-08-07|
|Form data collector|2.3.1|2026-08-07|
|Form data collector|2.3.1|2026-08-07|
|Formula Builder|29.1.1|2026-03-12|
|Formula builder connected|23.0.2|2026-09-10|
|Fortify Application Vulnerability Integration|2.7.1|2025-09-10|
|Foundation Data Sync|2.2.25|2026-08-07|
|Foundation Data Sync for Consumers|2.2.25|2026-08-07|
|Foundation Data Sync for Providers|2.2.25|2026-08-07|
|FRISS Spoke|1.1.1|2026-03-12|
|FSM - Advanced|2.1.2|2026-09-10|
|FSM - Foundation|2.1.2|2026-09-10|
|FSM Scheduling AI Agent Collection|2.0.4|2026-09-10|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Advanced|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Foundation|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO - Prime|1.0.0|2026-04-09|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|FSO Process Mining Content Pack|1.8.2|2025-07-31|
|Gantt UI Builder Component|26.1.4|2026-09-10|
|GC Dashboard|2.0.5|2025-12-11|
|Geo Map component|1.2.0|2025-07-31|
|Gifts and Entertainment Compliance|1.3.0|2025-12-11|
|Github Application Vulnerability Integration|2.3.1|2025-12-11|
|GitHub Spoke|3.5.1|2026-01-20|
|GitLab Spoke|2.4.0|2025-11-06|
|Gmail Spoke|1.3.3|2025-12-11|
|Goal Framework for SPM|2.10.0|2026-09-10|
|Google Calendar Spoke|2.6.0|2025-09-10|
|Google Chat Spoke|1.2.0|2025-09-10|
|Google Cloud Datastore Spoke|1.0.3|2023-09-07|
|Google Cloud DNS Spoke|1.0.2|2022-09-01|
|Google Cloud Functions Spoke|1.0.3|2025-06-05|
|Google Cloud Load Balancer Spoke|1.0.2|2023-09-07|
|Google Cloud Pub Sub Spoke|1.0.4|2024-09-10|
|Google Cloud SQL Spoke|1.0.2|2023-09-07|
|Google Cloud Storage Spoke|1.1.1|2025-12-11|
|Google Cloud Translator Service Spoke|3.2.6|2025-05-01|
|Google Cloud Virtual Network Spoke|1.0.5|2023-09-07|
|Google Cloud VPC Access Spoke|1.0.1|2022-09-01|
|Google Compute Engine Spoke|1.0.5|2024-09-10|
|Google Directory Spoke|1.5.2|2024-10-03|
|Google Docs Spoke|1.3.0|2025-09-10|
|Google Drive Spoke|2.3.0|2025-09-10|
|Google Gemini Spoke|1.6.2|2026-08-07|
|Google Identity And Access Spoke|1.1.1|2022-09-01|
|Google Meet Spoke|1.2.1|2025-11-06|
|Google Persistent Disk Spoke|1.0.2|2022-09-01|
|Google Sheets Spoke|1.0.7|2023-09-20|
|Google Tasks Spoke|1.4.0|2025-09-10|
|GoTo Spoke|2.0.1|2021-08-19|
|GovNotify Spoke|1.2.0|2025-09-10|
|GRC: Advanced Core|22.0.1|2026-03-12|
|GRC: Advanced Dashboards|21.1.1|2025-12-11|
|GRC: Advanced Risk Assessment|23.0.3|2026-09-10|
|GRC: Approver Configurator|23.0.5|2026-09-10|
|GRC: Audit Management|22.0.1|2026-03-12|
|GRC: Audit Management Workspace|22.0.1|2026-03-12|
|GRC: Business Continuity Management User - Lite|5.0.1|2023-08-03|
|GRC: Business User - Lite|18.0.0|2024-02-01|
|GRC: Common Dashboard Elements|18.1.4|2024-06-06|
|GRC: Compliance Assessment|23.0.2|2026-09-10|
|GRC: Compliance Case Management|21.1.0|2025-12-11|
|GRC: Compliance Management Workspace|21.1.3|2025-12-11|
|GRC: Compliance UCF|21.1.0|2025-12-11|
|GRC: Composite Entity|21.1.1|2025-12-11|
|GRC: Continuous Authorization and Monitoring|21.1.1|2025-12-11|
|GRC: Continuous Authorization and Monitoring Advanced|21.1.1|2025-12-11|
|GRC: Continuous Authorization and Monitoring Workspace|21.1.1|2025-12-11|
|GRC: Cyber Risk Institute \(CRI\) Profile Accelerator|21.1.0|2025-12-11|
|GRC: Cybersecurity Controls Accelerator|18.1.0|2024-06-06|
|GRC: Entity Based Access|21.1.4|2025-12-11|
|GRC: Financial Services Controls Accelerator|22.0.1|2026-03-12|
|GRC: integrations with third-party content|18.1.0|2024-06-06|
|GRC: Management Reporting|18.1.0|2024-06-06|
|GRC: Mobile|18.0.0|2024-02-01|
|GRC: NIST CSF Use Case Accelerator|21.1.0|2025-12-11|
|GRC: Performance Analytics Premium Integration|19.1.0|2024-11-07|
|GRC: Policy and Compliance integrator|21.1.0|2025-12-11|
|GRC: Policy and Compliance Management|23.0.2|2026-09-10|
|GRC: Predictive Intelligence|21.1.0|2025-12-11|
|GRC: Privacy Lite User|19.0.0|2024-08-01|
|GRC: Profiles|23.0.7|2026-09-10|
|GRC: Regulatory Change Management integration with RSS Feeds|21.1.0|2025-12-11|
|GRC: Risk Heatmap|22.3.2|2026-06-16|
|GRC: Risk Management|23.0.3|2026-09-10|
|GRC: Risk Management Workspace|21.1.1|2025-12-11|
|GRC: Risk Shared Common Components|23.0.5|2026-09-10|
|GRC: SIG Questionnaire Integration|21.1.0|2025-12-11|
|GRC: SOX Content Pack|21.1.0|2025-12-11|
|GRC: taxonomy management|23.0.2|2026-09-10|
|GRC: Technology Controls Monitoring Accelerator|21.1.0|2025-12-11|
|GRC: Vendor Portal|23.0.5|2026-09-10|
|GRC: Vendor Risk Management Workspace|23.0.5|2026-09-10|
|GRC: Virtual Agent|19.1.0|2024-11-07|
|GRC: Workbench|21.1.0|2025-12-11|
|GRC Case Management Core|23.0.2|2026-09-10|
|GRC Change Management Core|23.0.3|2026-09-10|
|GRC Compliance Case Management Advanced|18.1.1|2024-06-06|
|GRC Compliance Case Management Full Access|18.1.1|2024-06-06|
|GRC Employee User|19.0.1|2024-08-01|
|GRC Feature roles|23.0.3|2026-09-10|
|GRC integration with Thomson Reuters Regulatory Intelligence|21.1.0|2025-12-11|
|GRC Privacy Case Management Integration with RadarFirst|21.1.0|2025-12-11|
|Group Life Servicing|2.5.0|2026-03-12|
|Group Life Servicing|2.5.0|2026-03-12|
|Group Life Servicing|2.5.0|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|Group Life Underwriting|2.5.0|2026-03-12|
|Guidance|45.0.2|2026-09-10|
|Guidance|45.0.2|2026-09-10|
|Guided Decisions|38.0.2|2025-12-11|
|Guided Decisions|38.0.2|2025-12-11|
|Guided Decisions|38.0.2|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Guided Decisions Experience|39.0.2|2025-12-11|
|Guided Self-Service in Employee Center|3.2.2|2025-12-11|
|Guidewire Spoke|1.3.0|2026-03-12|
|Hardware Asset Management|16.0.1|2026-09-10|
|Hardware Asset Management for DaaS|12.1.1|2026-03-12|
|Hardware Asset Management for TNI|13.0.0|2025-11-06|
|Hardware Asset Management for Zero Touch Mobility|12.0.0|2025-01-30|
|HCLS - Advanced|3.2.0|2026-09-10|
|HCLS - Advanced|3.2.0|2026-09-10|
|HCLS - Foundation|3.1.0|2026-09-10|
|HCLS - Foundation|3.1.0|2026-09-10|
|HCLS - Prime|3.1.0|2026-09-10|
|HCLS - Prime|3.1.0|2026-09-10|
|Header App Shell|23.0.0|2023-06-01|
|Health and Safety Case Management|6.4.1|2026-09-10|
|Health and Safety Case Management|6.4.1|2026-09-10|
|Health and Safety Contractor Management|5.3.1|2026-08-07|
|Health and Safety Incident Management PA Content Pack|10.1.2|2026-09-10|
|Health and Safety Incident Management PA Content Pack|10.1.2|2026-09-10|
|Health and Safety Risk Management|9.3.1|2026-08-07|
|Health and Safety Testing|1.27.0|2025-07-31|
|Healthcare and Life Sciences Service Management Core|11.3.0|2026-03-12|
|Healthcare and Life Sciences Service Management Core|11.3.0|2026-03-12|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Computerized Maintenance Management System|7.0.0|2024-05-09|
|Healthcare Operations Core|2.3.0|2026-03-12|
|Healthcare Operations Core|2.3.0|2026-03-12|
|Healthcare Professional Data Model|1.3.0|2025-12-11|
|Health dashboard for AI Control Tower|3.0.11|2025-12-12|
|Health Log Analytics|38.0.17|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Hiring Connector|7.0.0|2025-12-11|
|Hiring Core|5.4.1|2026-07-09|
|Hiring tab|8.0.1|2026-07-09|
|Homepage deprecation help tool|2.0.2|2024-11-07|
|HR Flow Wizards|1.1.0|2022-05-05|
|HR License meter|1.1.6|2026-06-16|
|HR Multi Instance Integration Base|2.0.0|2025-07-31|
|HR Multi Instance Integration for Consumer|2.0.0|2025-07-31|
|HR Multi Instance Integration for Provider|2.0.0|2025-07-31|
|HRSD Process Mining Content Pack|6.0.3|2026-03-12|
|HR Service Delivery Advanced Integration with Oracle HCM|1.3.0|2025-12-11|
|HR Service Delivery Advanced Integration with Workday|2.2.6|2025-12-11|
|HR Service Delivery for Healthcare|1.0.4|2025-05-01|
|HR Service Delivery for Microsoft 365|3.8.0|2025-12-11|
|HR Service Delivery for mobile|21.2.9|2025-12-11|
|HR Service Delivery Integration with Cornerstone OnDemand|1.2.0|2025-12-11|
|HR Service Delivery integration with Oracle HCM|1.0.10|2024-11-07|
|HR Service Delivery Integration with Ultimate Kronos Group|2.0.6|2024-06-06|
|HR Service Delivery Integration with Workday|3.4.11|2025-12-11|
|HR Service Delivery NLU Model for Virtual Agent Conversations|22.2.0|2023-11-02|
|HR Service Delivery Portal UI Components|1.0.5|2024-05-09|
|HR Service Delivery Virtual Agent Conversations|24.2.8|2025-05-01|
|HR Success Dashboard indicators|1.0.15|2025-05-01|
|HR taxonomy|1.2.1|2022-12-01|
|Human Resources Service Delivery Integration with Workday Learning|1.4.0|2025-07-31|
|IBM License Compliance for Software Asset Management|6.0.7|2026-03-12|
|IBM QRadar Integration for Security Operations|10.3.7|2024-11-07|
|IBM watsonx Spoke|1.0.4|2025-01-30|
|ICW Core|1.0.4|2026-05-05|
|ICW - Foundation|1.0.3|2026-05-05|
|Idea Manager Dashboard|2.2.0|2025-12-11|
|iManage Spoke|1.1.6|2026-01-20|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - HAM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Impact Value Management - SAM|3.0.1|2025-12-11|
|Incident Communications Management for Service Operations Workspace|9.4.2|2026-09-10|
|Incident Management for Field Service|1.1.1|2025-01-02|
|Incident Management for Service Operations Workspace|9.4.2|2026-09-10|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Claims|1.4.0|2026-03-12|
|Individual Life Servicing|2.5.0|2026-03-12|
|Individual Life Servicing|2.5.0|2026-03-12|
|Individual Life Servicing|2.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Individual Life Underwriting|2.5.0|2026-03-12|
|Indoor Mapping|1.16.8|2026-06-16|
|Indoor Mapping Component|1.6.1|2026-06-16|
|Indoor Mapping for Assets|1.0.2|2025-10-16|
|Indoor Mapping Service|1.0.8|2025-12-11|
|Industrial Core|4.1.6|2026-09-10|
|Industrial Process Manager|4.2.5|2026-09-10|
|Industrial Workspace Common|4.2.4|2026-09-10|
|Industry Core|1.0.9|2022-12-01|
|Infoblox Spoke|2.0.4|2024-03-20|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Instance Security Center: NLU|3.0.1|2022-09-01|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Instance Security Center: Virtual Agent|3.0.0|2022-02-03|
|Insurance claims|1.2.2|2026-03-12|
|Insurance claims|1.2.2|2026-03-12|
|Insurance claims|1.2.2|2026-03-12|
|Insurance Claims Core|3.6.2|2026-08-07|
|Insurance Claims Core|3.6.2|2026-08-07|
|Insurance Claims Core|3.6.2|2026-08-07|
|Insurance Claims Core|3.6.2|2026-08-07|
|Insurance Claims Core|3.6.2|2026-08-07|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Insurance Special Investigations|2.5.0|2026-03-12|
|Integrated Risk Management Enterprise|23.0.2|2026-09-10|
|Integrated Risk Management Professional|23.0.2|2026-09-10|
|Integrated Risk Management Standard|23.0.2|2026-09-10|
|Integration Commons for CMDB|2.26.0|2026-09-10|
|IntegrationHub Enterprise Flow Wizards|1.0.0|2021-08-19|
|IntegrationHub ETL|3.3.6|2025-12-11|
|Integration Hub Usage Dashboards|3.0.0|2025-07-31|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Intelligent Servicing for Fraud|2.6.0|2026-03-12|
|Intelligent Task Recommendations|29.0.7|2026-03-12|
|Intent Discovery|3.3.8|2026-05-05|
|Interaction Management for Service Operations Workspace|9.4.2|2026-09-10|
|Interceptor UI for Service Operations Workspace|9.4.2|2026-09-10|
|Interview management|4.0.2|2026-07-09|
|Inventory Number Management|5.0.0|2025-07-31|
|Inventory Number Management|5.0.0|2025-07-31|
|Inventory Number Management|5.0.0|2025-07-31|
|Inventory Tracker App Template|28.2.1|2025-12-11|
|Investigation Framework|9.4.2|2026-09-10|
|Investment Funding|1.1.1|2024-05-09|
|Invicti Application Vulnerability Integration|1.2.1|2024-11-07|
|Invoice Case Management|13.2.4|2026-09-10|
|Invoice Case Self-Service|1.7.0|2026-09-10|
|Invoice Case Self-Service|1.7.0|2026-09-10|
|Invoice Case Self-Service|1.7.0|2026-09-10|
|Invoice Self-Service|1.5.0|2026-09-10|
|Invoice Self-Service|1.5.0|2026-09-10|
|Invoice Self-Service|1.5.0|2026-09-10|
|ISA Equipment Model|4.1.1|2026-09-10|
|Issue Auto Resolution for HR|4.0.3|2024-06-06|
|ITAM Common for DaaS|11.2.1|2026-03-12|
|ITAM common hub|1.1.0|2025-12-11|
|ITAM Health Check application|3.0.5|2026-03-12|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|IT Discovery for OT Networks|2.0.5|2025-05-01|
|ITOM AIOPS Config Center|27.2.3|2026-03-12|
|ITOM Cloud Services Core|4.3.0|2026-08-07|
|ITOM Configuration Console|28.1.1|2026-06-16|
|ITOM Guided Setup - New|27.3.1|2026-06-16|
|ITOM Infra Services Workspace|2.0.3|2026-07-09|
|ITOM Line chart|27.1.1|2026-03-12|
|ITOM Mobile Agent|1.0.0|2025-05-01|
|ITOM Telemetry Ingest|1.0.0|2025-12-11|
|IT Service Management AI voice agent collection|1.4.0|2026-06-16|
|IT Service Management for Microsoft 365|2.11.1|2025-12-11|
|ITSM Common Catalog Content|3.1.0|2026-07-09|
|ITSM Enterprise UI Components|3.5.0|2025-12-11|
|ITSM Mobile Agent|10.2.0|2025-12-11|
|ITSM NLU Model for Virtual Agent Conversations|8.2.0|2025-05-01|
|ITSM Process Mining Content Pack|2.0.0|2026-03-12|
|Jack Henry jXchange Spoke|2.1.0|2025-07-31|
|Jamf Spoke|1.2.1|2025-12-11|
|Jenkins Spoke|2.3.0|2025-09-10|
|Jenkins v2 Spoke|1.2.0|2023-02-02|
|Jira Service Management Spoke|1.2.0|2025-10-16|
|Jira Spoke|6.0.1|2026-04-09|
|Journey Accelerator|6.10.0|2026-06-16|
|Journey designer|7.6.5|2026-08-07|
|Kanban board component|26.0.1|2026-02-05|
|Kanban Components|1.2.0|2026-03-12|
|Keyboard Shortcuts AI Skills|1.0.4|2026-08-07|
|KnowBe4 Integration for SecOps|2.3.3|2024-12-05|
|Knowledge API|29.0.1|2026-03-12|
|Knowledge Graph Affinity Signals|1.0.1|2026-09-10|
|KPI Composer|4.3.1|2025-12-11|
|KPI Framework|7.0.0|2026-09-10|
|Kubernetes Spoke|1.3.0|2025-09-10|
|Kubernetes Visibility Agent|3.13.0|2025-12-11|
|Leader Hub|1.5.0|2026-03-12|
|Lead Management Application|5.0.0|2025-12-11|
|Lead Management Data Model|5.0.1|2025-12-11|
|Lead-to-Cash Process Management|2.2.2|2025-12-11|
|Learning|5.7.0|2026-06-16|
|Learning Core|9.10.0|2026-06-16|
|Legal Conflict of Interest|4.7.0|2025-12-11|
|Legal Content Review|1.3.0|2025-12-11|
|Legal Counsel Center|2.4.0|2026-08-07|
|Legal Mobile|5.6.0|2025-12-11|
|Legal Practice Apps Core|1.0.2|2023-02-02|
|Legal Request Management|10.3.4|2026-09-10|
|Legal Simple Compliance|1.1.0|2025-12-11|
|Legal Simple Intellectual Property|1.6.0|2025-12-11|
|Legal Simple Privacy|1.2.5|2025-12-11|
|Legal Stock Preclearance|4.9.0|2025-12-11|
|Legal Tracker Spoke|1.0.4|2025-01-30|
|Legal Virtual Agent Conversations|1.3.2|2023-05-04|
|Live CI View|19.1.2|2023-05-04|
|Localization Workspace|1.0.6|2025-05-01|
|Log Export Service|3.2.0|2025-05-01|
|Looker Spoke|1.0.2|2025-01-30|
|Lucidchart Diagramming Spoke|1.1.1|2024-01-04|
|Lucidchart Integration|2.4.1|2025-01-30|
|Magnit Spoke|1.2.1|2023-09-07|
|Major Incident Management for Service Operations Workspace|9.4.2|2026-09-10|
|Major Issue Management|4.1.7|2026-07-31|
|Major Security Incident Management|3.5.1|2026-01-20|
|Manage Invoice Operations|1.3.0|2026-09-10|
|Manage Order Operations|2.2.0|2026-09-10|
|Manager Hub|4.9.1|2026-06-16|
|Manage Skills Configurable Page|1.1.12|2025-01-30|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Core|2.3.3|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Manufacturing Dealer Management|2.3.2|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Labor Common|1.3.1|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Manufacturing Recall Claim Management|1.3.3|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Manufacturing Recall Claim Management Advanced|1.1.1|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Manufacturing Repair Claim Management|1.3.3|2025-12-11|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Manufacturing Repair Claim Management Advanced|1.3.1|2025-12-11|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Manufacturing Sales Promotion Claim Management|2.3.1|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Manufacturing Sales Promotion Management|2.3.4|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Manufacturing Sales Promotion Management Advanced|1.3.1|2025-12-11|
|Map Integrations for Field Service|29.0.8|2026-03-12|
|Marketplace Core|30.0.1|2026-03-12|
|Mastercard Spoke|4.0.1|2025-12-11|
|Matrix report|21.0.1|2025-07-31|
|McAfee ePO Integration for Security Operations|10.6.0|2025-12-11|
|Meeting CAB|9.4.2|2026-09-10|
|Meeting Extensions for Microsoft Teams|1.8.0|2025-12-11|
|Meeting Watcher - UI Builder Data Resource|9.4.2|2026-09-10|
|Mentoring|2.4.3|2026-08-07|
|Metadata Search|1.2.1|2026-09-10|
|Metric data table|22.5.0|2026-08-07|
|Metric Intelligence|2.7.11|2025-12-11|
|Metric Rules|1.1.4|2024-06-06|
|Metrics and CI Actions Framework|9.4.2|2026-09-10|
|Microsoft 365 for ServiceNow Reporting|23.0.2|2026-09-10|
|Microsoft Active Directory v2 Spoke|2.5.1|2025-10-16|
|Microsoft Azure AI Speech Spoke|1.0.1|2025-06-05|
|Microsoft Azure AI Spoke|1.0.3|2025-01-30|
|Microsoft Azure Application Insights Spoke|2.0.0|2024-11-07|
|Microsoft Azure Artifacts Spoke|1.1.0|2024-11-07|
|Microsoft Azure Automation Spoke|2.0.0|2024-11-07|
|Microsoft Azure Blob Storage Spoke|2.0.0|2024-11-07|
|Microsoft Azure Cosmos DB Spoke|2.0.0|2024-11-07|
|Microsoft Azure DevOps Boards Spoke|3.1.0|2025-09-10|
|Microsoft Azure DevOps Integration for Agile Development|1.7.0|2025-12-11|
|Microsoft Azure DevOps Integrations Common|1.9.0|2025-12-11|
|Microsoft Azure DevOps Pipelines Spoke|1.0.0|2023-08-03|
|Microsoft Azure Managed Storage Spoke|2.0.1|2024-11-07|
|Microsoft Azure Notification Hub Spoke|2.0.0|2024-11-07|
|Microsoft Azure OEM Translator Service Spoke|4.0.2|2025-07-10|
|Microsoft Azure RBAC Spoke|1.0.2|2025-09-10|
|Microsoft Azure Resource Management Spoke|2.0.0|2024-11-07|
|Microsoft Azure Sentinel Incident Ingestion Integration For Security Operations|11.2.3|2026-05-05|
|Microsoft Azure SQL Database Spoke|2.0.0|2024-11-07|
|Microsoft Azure Traffic Manager Spoke|2.0.0|2024-11-07|
|Microsoft Azure Virtual Machine Spoke|2.0.0|2024-11-07|
|Microsoft Azure Virtual Network Spoke|2.0.0|2024-11-07|
|Microsoft Defender for Cloud Integration for Security Operations|2.8.0|2025-12-11|
|Microsoft Defender for Office365 Integration for SecOps|2.3.4|2024-12-05|
|Microsoft Dynamics 365 for Finance and Operations Spoke|2.4.3|2026-01-20|
|Microsoft Dynamics 365 Spoke|1.1.0|2025-07-31|
|Microsoft Dynamics CRM Spoke|1.9.0|2025-11-06|
|Microsoft Endpoint Configuration Manager for Investigation|9.4.2|2026-09-10|
|Microsoft Endpoint Configuration Manager Spoke|1.8.1|2025-06-05|
|Microsoft Entra ID Integration for Password Reset|3.0.3|2025-01-30|
|Microsoft Entra ID Spoke|4.7.3|2025-12-11|
|Microsoft Exchange Online for Security Operations|10.7.2|2026-01-20|
|Microsoft Exchange Online Spoke|3.12.0|2025-11-06|
|Microsoft Exchange Server Spoke|2.5.1|2025-11-06|
|Microsoft Graph Security API Alert Ingestion Integration For Security Operations|10.5.5|2026-07-09|
|Microsoft Integrations - Core|5.8.1|2025-12-11|
|Microsoft Intune Spoke|1.2.0|2025-11-06|
|Microsoft Office add-in|22.3.0|2026-06-16|
|Microsoft OneDrive Spoke|2.8.1|2025-11-06|
|Microsoft Outlook Add-In for Legal Service Delivery|1.5.0|2025-12-11|
|Microsoft Security Response Center Spoke|1.3.0|2025-09-10|
|Microsoft SharePoint File Explorer Connector for Security Incident Response integration|1.3.0|2025-12-11|
|Microsoft SharePoint Online Spoke|2.10.0|2025-09-10|
|Microsoft Teams Chat Connector for Security Incident Management|1.2.30|2025-10-16|
|Microsoft Teams Communications Spoke|1.5.0|2025-12-11|
|Microsoft Teams Graph Spoke|4.4.1|2026-02-05|
|Microsoft Word Add-in for ServiceNow Contracts|1.6.7|2025-12-11|
|MID Admin Workspace|2.0.1|2026-07-09|
|MID Guardian|1.0.4|2025-12-11|
|MID Server Infrastructure|2.0.1|2026-07-09|
|MIF Customer Instance|4.1.3|2026-08-07|
|Migration Utility for Service Operations Workspace|2.3.1|2025-05-01|
|Milestones|2.9.1|2026-09-10|
|Miro Spoke|3.3.1|2025-12-11|
|MISP integration for Security Operations|1.4.4|2026-02-05|
|Mitigation Controls Monitoring|4.1.4|2025-12-11|
|Mobile App Builder|27.11.0|2025-07-31|
|Mobile App Builder API|27.11.0|2025-07-31|
|Mobile Builder AI|27.6.0|2026-07-09|
|Mobile Card Builder|26.12.0|2025-07-31|
|Mobile Publishing|24.0.0|2025-12-11|
|Mobile SDK|2.2.0|2025-03-12|
|Mobile Time Sheets|2.3.0|2025-12-11|
|monday.com Spoke|1.1.5|2025-06-05|
|MSIM VTB Task Card|1.0.1|2024-02-01|
|MS Teams Activities for PAD|1.0.3|2023-01-12|
|Multi-case creation framework|2.1.0|2025-07-31|
|Natural Language Understanding Models for Sourcing and Procurement Operations|2.0.5|2023-05-04|
|Navex EthicsPoint Spoke|1.0.3|2025-12-11|
|News Integration for Supplier Lifecycle Operations|10.0.0|2026-09-10|
|Next Experience All Menu Editing|29.6.9|2026-09-10|
|NLU Workbench - Advanced Features|7.0.22|2025-07-10|
|Node map Experience Component|27.3.2|2026-08-07|
|Notification Flow Wizards|2.0.1|2022-09-21|
|Notifications Email Agents|3.0.2|2026-09-10|
|Notifications for Employee Center|2.2.0|2026-07-09|
|Notify Connector for Microsoft Teams|2.10.0|2025-12-11|
|Notify UI Components for Configurable Workspaces|9.4.2|2026-09-10|
|Notify Webex Connector|1.4.0|2025-12-11|
|Notify Zoom Connector|1.9.0|2025-07-31|
|Now Assist for Employee Center Pro|1.1.9|2025-12-11|
|Now Assist for Platform for Requestor|3.1.0|2026-05-05|
|Now Assist for Playbook|28.0.1|2025-12-11|
|Now Assist for Service Graph Connectors|1.1.0|2025-01-30|
|Now Learning Integration|1.0.3|2024-02-01|
|Obligation Management|1.5.5|2025-12-11|
|Observability Commons for CMDB|1.1.0|2023-11-02|
|Okta Spoke|4.7.1|2025-11-06|
|Omnichannel Callback|2.1.0|2026-09-10|
|Omnichannel Callback for Customer Service Management|1.5.1|2025-12-11|
|Omni-Experience Standard Feature Set|8.3.1|2026-09-10|
|On Call Scheduling for Service Operations Workspace|9.4.3|2026-09-10|
|On-Call UI Components for Configurable Workspaces|9.4.2|2026-09-10|
|OneLogin Spoke|1.0.2|2023-09-07|
|One-time Password Generator|1.1.0|2025-12-11|
|OpenAI Generative AI Spoke|3.4.0|2025-07-31|
|Operational Sustainability Management Advanced|23.0.1|2026-09-10|
|Operational Sustainability Management Prime|23.0.3|2026-09-10|
|Operational Technology Change Management|4.1.4|2026-08-13|
|Operational Technology Hardware Vulnerability Assessment|4.1.6|2026-09-10|
|Operational Technology Health|4.1.2|2026-08-13|
|Operational Technology Incident Management|4.0.0|2026-06-16|
|Operational Technology Incident Management|4.0.0|2026-06-16|
|Operational Technology Incident Management|4.0.0|2026-06-16|
|Operational Technology Manager|4.1.6|2026-09-10|
|Operational Technology Setup|1.0.0|2026-09-10|
|Operational Technology Vulnerability Response|3.2.7|2026-09-10|
|Opportunity Management for Business Locations|2.0.0|2026-03-12|
|Opportunity Marketplace|2.7.0|2026-06-16|
|Oracle Autonomous DB Spoke|1.0.6|2022-12-01|
|Oracle Block Storage Spoke|1.0.4|2022-12-01|
|Oracle Boot Volume Spoke|1.0.6|2022-12-01|
|Oracle Cloud IAM Spoke|1.1.3|2022-09-21|
|Oracle Compute Engine Spoke|1.0.4|2022-12-01|
|Oracle EBS Spoke|1.13.2|2025-07-10|
|Oracle Financial Cloud Spoke|1.2.0|2025-11-06|
|Oracle HCM Cloud Spoke|4.3.0|2025-12-11|
|Oracle Netsuite Spoke|1.0.3|2025-09-10|
|Oracle Object Storage Management Spoke|1.0.3|2022-09-21|
|Oracle Peoplesoft Financial Spoke|1.1.0|2024-03-07|
|Oracle Virtual Cloud Network Spoke|1.0.4|2022-12-01|
|Order Case Playbook|1.4.1|2025-12-11|
|Order Case Playbook|1.4.1|2025-12-11|
|Order Case Self Service|2.2.0|2026-09-10|
|Order Case Self Service|2.2.0|2026-09-10|
|Order Case Self Service|2.2.0|2026-09-10|
|Order Management|18.3.3|2026-09-10|
|Order Management|5.0.0|2023-02-02|
|Order Management for Business Locations|2.0.0|2026-03-12|
|Order Management for Telecom, Media and Tech|13.1.2|2025-12-11|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Management Portal|2.1.0|2025-07-31|
|Order Operations Case Management|3.1.3|2026-09-10|
|Order Operations Case Management|3.1.3|2026-09-10|
|Order Operations Case Management|3.1.3|2026-09-10|
|Order Qualification Management|5.2.1|2026-09-10|
|Order Qualification Management|5.2.1|2026-09-10|
|Order Qualification Management|5.2.1|2026-09-10|
|Order to cash common architecture|1.6.6|2026-09-10|
|OT Asset Management|2.2.1|2026-09-10|
|OT Asset Management Advanced|2.0.1|2026-09-10|
|OT Manager Foundation|3.3.3|2026-06-16|
|OTSM Advanced|1.0.1|2026-04-09|
|OTSM Foundation|1.0.1|2026-04-09|
|OTSM Prime|1.0.1|2026-04-09|
|Outlook Actionable Messages|4.7.0|2026-06-16|
|Outsourced Customer Service|2.1.2|2026-03-12|
|PA AI Tools|1.0.4|2026-09-10|
|PagerDuty Spoke|1.5.1|2026-01-20|
|Palo Alto Networks NGFW for Security Operations|10.5.2|2025-12-11|
|Parallel Review and Feedback|21.1.0|2025-12-11|
|PAR CoreUI Migration Scripts|4.0.3|2026-03-12|
|Participant Suggestions|2.0.1|2024-08-01|
|Password Reset for Service Operations Workspace|9.4.2|2026-09-10|
|Password Reset for Virtual Agent|5.0.6|2025-07-31|
|Password Reset integration for Microsoft Active Directory|4.0.0|2025-07-31|
|Password Reset integration with Google Directory|1.0.3|2023-06-01|
|Password Reset integration with Okta|1.1.2|2023-04-06|
|Password Reset UI components for Configurable Workspaces|9.4.2|2026-09-10|
|Patch Management Data Model|1.0.4|2025-05-01|
|Pattern Designer Enhancements|3.9.0|2025-12-11|
|Payment Card|1.5.1|2026-08-07|
|Payment Card|1.5.1|2026-08-07|
|Payment Card|1.5.1|2026-08-07|
|Payment Card|1.5.1|2026-08-07|
|Payment Card|1.5.1|2026-08-07|
|Payment framework for conversational channels|1.1.0|2026-03-12|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics - Content Engagement Analytics|30.0.4|2025-01-30|
|Performance Analytics Content Pack for Agile 2.0|1.4.6|2025-12-11|
|Performance Analytics Content Pack for Cloud Resources|1.5.0|2024-11-07|
|Performance Analytics Content Pack for Essential SAFe|1.4.2|2023-09-20|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for FSO|1.12.1|2026-03-12|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Healthcare CDM|4.0.0|2024-05-09|
|Performance Analytics Content Pack for Legal Service Delivery|2.7.0|2025-12-11|
|Performance Analytics Content Pack for Public Sector Digital Services|2.0.3|2024-09-10|
|Performance Analytics - Content Pack - Guided Tours|1.4.0|2026-03-12|
|Performance Analytics for Configuration Compliance|1.5.2|2025-12-11|
|Performance Analytics for Security Incident Response|10.5.2|2025-05-01|
|Performance Analytics for Sourcing and Procurement Operations|3.0.9|2024-08-01|
|Performance Analytics for Vulnerability Response|12.16.1|2025-12-11|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Analytics - Portal Analytics|29.1.1|2025-05-01|
|Performance Appraisal App Template|28.2.1|2025-12-11|
|Personal Lines Claims|4.4.0|2026-03-12|
|Personal Lines Claims|4.4.0|2026-03-12|
|Personal Lines Claims|4.4.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Personal Lines Servicing|2.5.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Personal Lines Underwriting|2.5.0|2026-03-12|
|Physical Assets|2.3.0|2026-03-12|
|Planned Maintenance Management|2.14.0|2026-06-16|
|Planned Task Common|1.1.0|2025-12-11|
|Planned Work Management|2.11.0|2025-12-11|
|Platform Analytics|8.4.1|2026-07-09|
|Playbooks for Customer Service Management|6.5.1|2026-06-16|
|Plivo Spoke|1.2.0|2025-11-06|
|Pluralsight Spoke|1.3.0|2026-08-07|
|Policy as Code Engine|3.3.1|2026-09-10|
|policy-as-code-engine-ui|3.3.0|2026-06-16|
|POM - Foundation|1.1.2|2026-06-16|
|POM - Prime|1.3.1|2026-09-10|
|Portal navigation demo|27.0.0|2025-06-05|
|Portal Next Experience Theme|24.3.2|2026-06-16|
|Post Assessment Actions for Smart Assessments|23.0.3|2026-09-10|
|PPM Collaboration|2.1.0|2024-11-07|
|Predictive Intelligence for Legal Service Delivery|1.2.0|2025-12-11|
|Predictive Intelligence for User Reported Phishing|10.3.7|2024-09-10|
|Predictive Intelligence Store App|1.0.3|2025-12-11|
|Preferred tables|29.1.1|2026-03-12|
|Price Management|18.0.4|2026-09-10|
|Privacy Employee User|19.0.1|2024-08-01|
|Private cloud orchestration|1.0.0|2025-12-11|
|Proactive Customer Service Operations|25.0.1|2026-03-12|
|Proactive Customer Service Operations with Event Management|25.0.2|2026-03-12|
|Proactive Engagement|5.2.0|2026-09-10|
|Proactive Engagement|5.2.0|2026-09-10|
|Proactive Prompts|3.5.1|2026-06-16|
|Proactive Service Experience Workflows|8.6.2|2026-07-09|
|Proactive Triggers|3.0.10|2025-12-11|
|Problem Management for Service Operations Workspace|9.4.2|2026-09-10|
|Problem Management Migration Utility|2.3.0|2026-03-12|
|Process Automation Content|28.1.4|2025-09-10|
|Process Automation Experience Demo|24.1.4|2024-10-03|
|Process Mining Content Pack for CSM|23.2.0|2025-07-31|
|Process Mining Content Pack for FSM|1.5.0|2026-03-12|
|Process Mining Content Pack for SPM|1.0.2|2026-03-12|
|Process Mining for Source-to-Pay Operations|1.0.1|2024-08-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Process Mining for Telecommunications|5.0.0|2024-02-01|
|Procurement Case Management|20.0.0|2026-09-10|
|Procurement File Transfer Framework|2.2.2|2023-05-04|
|Procurement for Field Service|3.0.0|2026-03-12|
|Product and pricing rules|9.0.0|2025-12-11|
|Product Capability Core|2.2.2|2026-07-09|
|Product Catalog Advanced|10.5.0|2026-09-10|
|Product Catalog Advanced|10.5.0|2026-09-10|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Catalog Management Portal|2.2.0|2025-12-11|
|Product Conditions Core|4.6.9|2026-09-10|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Configurator|1.0.1|2024-11-07|
|Product Inventory Advanced|14.3.3|2026-09-10|
|Product Inventory Advanced|14.3.3|2026-09-10|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Offering Recommendations|1.2.0|2025-12-11|
|Product Support for Technology|4.3.6|2026-07-09|
|Profanity filter for agent chat|3.0.12|2024-11-07|
|Professional Data Model|1.1.0|2025-12-11|
|Project Status Report|1.1.0|2023-02-02|
|PSDS - Advanced|1.0.1|2026-04-09|
|PSDS - Foundation|1.0.1|2026-04-09|
|PSDS - Prime|1.0.1|2026-04-09|
|Public Sector Digital Services Core|15.0.6|2026-09-10|
|Purchase Order Management|3.0.4|2026-09-10|
|Qualtrics Spoke|1.3.0|2025-11-06|
|Qualys Integration for Security Operations|12.19.6|2025-12-11|
|Quick filter component|27.2.3|2026-06-16|
|Quick links component for Service Operations Workspace|9.4.2|2026-09-10|
|Quote AI agent|3.0.8|2026-09-10|
|Quote Management Application|9.1.0|2025-12-11|
|Quote Management Data Model|9.0.0|2025-12-11|
|Quote Management for Business Locations|2.0.0|2026-03-12|
|RAG for code generation|1.1.14|2026-09-10|
|Rally Spoke|1.0.3|2023-05-04|
|Rapid7 Integration for Security Operations|13.16.4|2025-12-11|
|Recommendation template|23.0.2|2026-09-10|
|Recommended Actions|44.0.4|2026-09-10|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions - Advanced|12.0.1|2025-12-11|
|Recommended Actions for Customer Service|30.0.1|2025-07-31|
|Recommended Actions for ITSM|3.4.1|2026-08-07|
|Recommended Actions for OTSM|3.1.0|2026-03-12|
|Record lookup connected component|28.0.1|2025-12-11|
|Record Page for Service Operations Workspace|9.4.2|2026-09-10|
|Record Related Items Connected|2.2.0|2025-12-11|
|Recruiter Workspace|8.0.1|2026-07-09|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Redox Inbound Integration|6.0.0|2024-08-01|
|Regulatory Agency Library|23.0.2|2026-09-10|
|Related party|1.0.6|2023-02-02|
|Related party|1.0.6|2023-02-02|
|ReleaseOps|1.2.3|2026-02-05|
|Release Timeline Component|1.4.0|2025-12-11|
|Remedial Actions Framework|9.3.3|2026-08-07|
|Remediation for Security Exposure Management|31.0.12|2026-09-10|
|Remediation Playbooks|1.1.0|2022-11-03|
|Reporting UI Component for Workspace|2.5.0|2026-07-09|
|Requester Experience Templates|1.0.0|2024-11-07|
|Request Management for Service Operations Workspace|9.4.2|2026-09-10|
|Requirement Intake Diagram|1.0.1|2024-12-05|
|Resizable panes component|28.0.3|2025-12-11|
|Resolution Shaper|29.0.10|2026-03-12|
|Resolution Shaper|29.0.10|2026-03-12|
|Retry Handler Framework|1.0.2|2022-09-21|
|Rich Text Editor Component for Security Operations|2.0.1|2026-06-16|
|Risk Assessments for Supplier Lifecycle Operations|8.0.1|2026-09-10|
|Risk Scoring for Security Exposure Management|30.1.9|2026-09-10|
|RMA Case Management|2.3.4|2026-09-10|
|Roadmunk Spoke|1.6.5|2024-07-11|
|RPA Hub|18.1.2|2026-08-07|
|RPA Plugin Bundle|18.0.4|2026-08-07|
|RSM - Advanced|1.1.1|2026-08-07|
|RSM - Advanced|1.1.1|2026-08-07|
|RSM - Foundation|1.1.1|2026-08-07|
|RSM - Foundation|1.1.1|2026-08-07|
|RSM - Prime|1.1.1|2026-08-07|
|RSM - Prime|1.1.1|2026-08-07|
|Saba Spoke|1.2.2|2026-06-16|
|Safe Workplace Dashboard|1.41.0|2025-07-31|
|Safe Workplace for mobile|2.10.3|2025-07-31|
|Safe Workplace suite|1.34.2|2025-07-31|
|Safe Workplace suite Professional|1.25.2|2025-07-31|
|Sales Agreement Data Model|8.0.0|2025-12-11|
|Sales Agreement Management|8.0.0|2025-12-11|
|Sales and Order Management Mobile Common|29.1.2|2026-03-12|
|Sales Cart|2.1.0|2025-12-11|
|Sales Cart|2.1.0|2025-12-11|
|Sales Common|8.1.2|2026-09-10|
|Sales Development AI Agents|1.0.12|2026-09-10|
|Salesforce Marketing Cloud Spoke|1.5.1|2025-03-12|
|Salesforce Spoke|2.3.4|2025-11-06|
|Sales Forecasting|2.0.1|2025-12-11|
|Sales Quota Application|1.1.0|2025-12-11|
|Sales Quota Data Model|1.1.0|2025-12-11|
|Sales Territory Management|2.0.0|2026-03-12|
|SBOM Core|6.2.2|2025-12-11|
|SBOM Response|6.4.1|2025-12-11|
|SCCM Usage Metering Spoke|1.0.2|2023-09-07|
|Scenario Planning for PPM|2.4.0|2025-12-11|
|Schedule Optimization|29.0.22|2026-08-07|
|Scope 3 emissions management|21.1.1|2025-12-11|
|Screen Summarization|1.2.6|2026-08-07|
|Scrum Common|1.4.5|2025-01-30|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Search Configurations for mobile|29.0.7|2025-05-01|
|Secops Health Analytics|30.2.0|2026-04-09|
|Secureworks CTP Spoke|1.0.3|2022-09-21|
|Secureworks Ticket Ingestion Integration for Security Operations|11.1.2|2026-02-05|
|Security Case Management common PAD artefacts|1.1.12|2026-01-20|
|Security Case Management common workspace components|2.1.3|2026-09-10|
|Security Center|3.2.5|2026-06-16|
|Security Incident Response|14.4.0|2026-09-10|
|Security Incident Response - Advanced|1.0.10|2026-09-10|
|Security Incident Response - Foundation|1.0.10|2026-09-10|
|Security Incident Response integration with AWS SecurityHub|1.1.0|2025-12-11|
|Security Incident Response Integration with CrowdStrike Next-Gen SIEM|2.3.1|2025-12-11|
|Security Incident Response integration with FireEye HX|1.1.0|2025-12-11|
|Security Incident Response integration with Microsoft Defender for Endpoint|1.2.1|2026-02-05|
|Security Incident Response Integration with Palo Alto Networks XSIAM|3.0.2|2026-01-20|
|Security Incident Response integration with Proofpoint|1.1.0|2025-12-11|
|Security Incident Response Integration with Zscaler|11.2.3|2026-02-05|
|Security Incident Response Mobile|10.4.0|2024-11-07|
|Security Incident Response - Prime|1.0.10|2026-09-10|
|Security Incident Response Workspace|1.10.1|2026-09-10|
|Security Incident UI Card Component|1.0.5|2026-09-10|
|Security Integration Framework|13.13.0|2026-07-09|
|Security Operations 'Have I been pwned?' Integration|10.5.1|2025-03-12|
|Security Operations CrowdStrike Intelligence Integration|10.8.0|2025-12-11|
|Security Operations Hybrid Analysis Integration|10.7.0|2026-02-05|
|Security Operations LogRhythm Integration|11.2.1|2025-12-11|
|Security Operations Metadefender Integration|10.5.0|2024-08-01|
|Security Operations Palo Alto Networks - AutoFocus|10.4.0|2025-01-30|
|Security Operations Palo Alto Networks - WildFire|10.4.0|2025-01-30|
|Security Operations PhishTank Integration|10.5.0|2024-08-01|
|Security Operations Reverse WHOIS Integration|10.5.0|2025-12-11|
|Security Operations RiskIQ Integration|10.4.1|2024-08-01|
|Security Operations Setup Assistant|10.4.41|2026-06-16|
|Security Operations Shodan Integration|10.4.1|2024-08-01|
|Security Operations Spoke|10.6.7|2025-06-05|
|Security Operations VirusTotal Integration|10.4.1|2025-12-11|
|Security Posture Control Core|7.0.1|2025-12-11|
|Security Simulation and Training Integration for SecOps|2.1.3|2024-05-09|
|Security Support Orchestration|12.13.4|2025-01-30|
|Service Bridge for Public Sector Digital Services \(PSDS\)|1.0.2|2025-05-01|
|Service Builder|3.6.1|2025-12-11|
|Service Builder Components|2.2.0|2025-12-11|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Catalog for mobile|29.0.7|2025-05-01|
|Service Contractor Base|2.0.0|2026-03-12|
|Service Exchange - Advanced|1.1.13|2026-08-13|
|Service Exchange Base|2.3.29|2026-08-07|
|Service Exchange for Consumers|2.3.29|2026-08-07|
|Service Exchange for Providers|2.2.25|2026-08-07|
|Service Exchange - Foundation|1.1.13|2026-08-13|
|Service Exchange Health|2.3.29|2026-08-07|
|Service Exchange Order Management for Providers|2.2.25|2026-08-07|
|Service Exchange - Prime|1.1.13|2026-08-13|
|Service Exchange Remote Process Sync Transport|2.3.29|2026-08-07|
|Service Graph Connector Dependencies|1.0.0|2021-01-21|
|Service Graph Connector for Akamai API Security|1.0.0|2025-10-16|
|Service Graph Connector for AWS|2.12.1|2025-10-16|
|Service Graph Connector for ExtraHop|2.0.3|2020-09-16|
|Service Graph Connector for GCP|1.11.0|2025-10-16|
|Service Graph Connector for Google Console|1.0.0|2024-08-01|
|Service Graph Connector for Infoblox|1.4.0|2025-07-31|
|Service Graph Connector for Jamf|2.14.4|2025-09-10|
|Service Graph Connector for Microsoft Azure|1.15.0|2025-12-11|
|Service Graph Connector for Microsoft Defender Endpoint|1.2.0|2025-05-01|
|Service Graph Connector for Microsoft Defender for IoT \(Azure\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Service Graph Connector for Microsoft Excel|4.1.5|2026-09-10|
|Service Graph Connector for Microsoft Intune|2.7.1|2025-10-16|
|Service Graph Connector for Microsoft SCCM|3.8.0|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA Altiplano|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Service Graph Connector for NOKIA NSP|1.2.1|2025-12-11|
|Service Graph Connector for Observability - AppDynamics|1.6.0|2025-12-11|
|Service Graph Connector for Observability - Datadog|1.4.0|2025-12-11|
|Service Graph Connector for Observability - Dynatrace|1.13.1|2025-09-10|
|Service Graph Connector for Observability - New Relic|1.4.0|2025-12-11|
|Service Graph Connector for OpenTelemetry|1.4.1|2024-05-09|
|Service Graph Connector for SolarWinds|2.6.0|2025-07-31|
|Service Graph Connector for Tanium|1.8.2|2025-11-06|
|Service Graph Connector for Trellix|1.0.0|2025-06-05|
|Service Graph Connector for VMware Workspace ONE UEM|1.8.0|2025-07-31|
|Service Graph Connector for Wiz|1.4.0|2025-11-06|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Integration for Claroty CTD|2.1.8|2025-05-01|
|Service Graph Connector Licensing|1.0.0|2022-05-05|
|Service Graph Connector Support Tools|1.0.0|2024-02-01|
|Service Level Management Experience for Workspace|9.4.2|2026-09-10|
|Service Level Objective Management for Service Operations Workspace|2.0.0|2026-06-16|
|Service Mapping Plus|1.17.2|2026-01-20|
|ServiceNow Add-Ins for Microsoft Office|7.4.0|2025-12-11|
|ServiceNow Document Designer with Word|23.0.3|2026-09-10|
|ServiceNow Enterprise Asset Management|11.0.0|2026-09-10|
|ServiceNow ITOM/OT SU Licensing|3.13.1|2026-07-09|
|ServiceNow Kafka Consumer|1.0.1|2023-04-06|
|ServiceNow Otto for Accounts Payable Operations \(APO\)|9.0.0|2026-09-10|
|ServiceNow Otto for Automation Center|1.3.0|2026-08-07|
|ServiceNow Otto for Care Team Operations|2.1.1|2026-09-10|
|ServiceNow Otto for Care Team Operations|2.1.1|2026-09-10|
|ServiceNow Otto for Code|28.5.32|2026-09-10|
|ServiceNow Otto for Conversational Spokes|1.1.2|2026-08-07|
|ServiceNow Otto for Core Business Suite|3.3.2|2026-08-07|
|ServiceNow Otto for Core Business Suite|3.3.2|2026-08-07|
|ServiceNow Otto for CPQ|1.1.8|2026-09-10|
|ServiceNow Otto for CSM Major Issue Management|1.2.4|2026-08-07|
|ServiceNow Otto for Digital End-user Experience \(DEX\)|5.2.10|2026-09-18|
|ServiceNow Otto for Document Voice|2.0.11|2026-09-10|
|ServiceNow Otto for Employee Experience|4.4.3|2026-08-07|
|ServiceNow Otto for Enterprise Asset Management|2.0.1|2026-09-10|
|ServiceNow Otto for Error Framework|1.2.0|2026-09-10|
|ServiceNow Otto for Field Service Management|11.1.2|2026-09-10|
|ServiceNow Otto for Finance and Procurement|8.0.0|2026-09-10|
|ServiceNow Otto for Financial Services Operations \(FSO\)|3.4.3|2026-09-04|
|ServiceNow Otto for HRSD - Galileo Inside|2.3.7|2026-09-10|
|ServiceNow Otto for ICW|1.1.0|2026-08-07|
|ServiceNow Otto for Integration Hub|2.3.2|2026-08-07|
|ServiceNow Otto for Legal Service Delivery|1.9.7|2026-09-10|
|ServiceNow Otto for OT Service Management|3.1.5|2026-08-07|
|ServiceNow Otto for Process Mining|4.1.5|2026-09-10|
|ServiceNow Otto for Purchase Order Management \(POM\)|1.4.1|2026-09-10|
|ServiceNow Otto for Retail Service Management|1.6.0|2026-09-10|
|ServiceNow Otto for RPA Hub|5.1.1|2026-08-07|
|ServiceNow Otto for Security Incident Response Integration Toolkit|1.2.5|2026-08-07|
|ServiceNow Otto for Service Exchange|1.1.12|2026-08-13|
|ServiceNow Otto for Sourcing and Procurement Operations \(SPO\)|11.0.0|2026-09-10|
|ServiceNow Otto for Spoke Generation|2.0.1|2026-08-07|
|ServiceNow Otto for Supplier Lifecycle Operations \(SLO\)|9.0.1|2026-09-10|
|ServiceNow Otto for Threat Intelligence Security Center|2.6.1|2026-09-10|
|ServiceNow Otto for Vault|2.2.2|2026-08-07|
|ServiceNow Otto for Virtual Agent Configurations|16.0.5|2026-08-20|
|ServiceNow Otto for WDF|2.3.4|2026-08-07|
|ServiceNow Otto for Workplace Service Delivery \(WSD\)|1.1.20|2026-08-07|
|ServiceNow Otto for Wrap Up|1.0.4|2026-08-07|
|ServiceNow Otto for Zero Copy Connector|2.0.6|2026-08-07|
|ServiceNow Otto in Document Management|4.0.11|2026-09-18|
|ServiceNow Remote Instance Spoke|2.2.9|2025-11-06|
|ServiceNow Studio for App Engine|28.2.1|2025-12-11|
|ServiceNow Voice|5.0.1|2026-02-05|
|ServiceNow Voice for CSM|3.10.0|2026-02-05|
|ServiceNow Voice for HR Service Delivery \(HRSD\)|1.0.5|2025-12-11|
|ServiceNow Voice for ITSM|4.1.1|2025-12-11|
|ServiceNow Voice UI components|3.8.0|2026-02-05|
|service-observability-app|1.10.12|2025-12-11|
|Service Observability UI|1.10.12|2025-12-11|
|Service Operations Workspace Admin Center|9.4.2|2026-09-10|
|Service Operations Workspace Alert Automation|25.11.1|2026-03-12|
|Service Operations Workspace Alert Automation|25.11.1|2026-03-12|
|Service Operations Workspace Alert Automation API|25.11.0|2026-03-12|
|Service Operations Workspace Alert Automation API|25.11.0|2026-03-12|
|Service Operations Workspace Alert Automation UI|25.11.0|2026-03-12|
|Service Operations Workspace Alert Mngmt|27.0.2|2026-03-12|
|Service Operations Workspace Core|9.4.2|2026-09-10|
|Service Operations Workspace Express List|27.0.8|2026-03-12|
|Service Operations Workspace Express List App|27.0.0|2026-03-12|
|Service Operations Workspace Integrations launchpad|27.0.3|2026-03-12|
|Service Operations Workspace Integrations launchpad UI|27.0.0|2026-03-12|
|Service Operations Workspace ITOM Apps|27.0.0|2026-03-12|
|Service Operations Workspace ITSM Admin Center|9.4.2|2026-09-10|
|Service Operations Workspace ITSM Advanced Applications|9.4.2|2026-09-10|
|Service Operations Workspace ITSM Applications|9.4.2|2026-09-10|
|Service Operations Workspace ITSM Common|9.4.2|2026-09-10|
|Service Operations Workspace Link View|27.0.0|2026-03-12|
|Service Operations Workspace Log Analytics|26.5.0|2025-12-11|
|Service Operations Workspace Metric Explorer|27.0.0|2026-03-12|
|Service Operations Workspace Metric Explorer APIs|23.4.0|2025-07-31|
|Service Operations Workspace Service Dashboard|27.1.0|2025-12-11|
|Service Operations Workspace Service Map Monitoring|26.5.0|2025-07-31|
|Service Operations Workspace Service Reliability Management \(SRM\) Common|7.0.0|2026-06-16|
|Service Operations Workspace UI Components|27.0.5|2026-03-12|
|Service Organization|2.10.1|2026-09-10|
|Service Reliability Management|7.0.0|2026-06-16|
|Service Request Criteria|3.1.0|2026-06-16|
|Service Request Management App Template|28.2.1|2025-12-11|
|Service Test Management|5.0.1|2025-12-11|
|Shared Library for Talent Development|2.5.0|2026-06-16|
|SharePoint Online Search Connector|6.1.2|2024-11-07|
|Shift Handover Application|2.1.0|2026-09-10|
|Shift Planning for Configurable Workspace|3.7.0|2025-12-11|
|Shodan Exploit Integration for Security Operations|10.8.0|2024-11-07|
|Shopping Hub|11.1.1|2026-06-16|
|Shopping Hub Mobile|7.6.24|2025-07-31|
|Sitemap Generator|1.2.0|2025-07-31|
|Site Mapping for Field Service Management|2.1.1|2026-03-12|
|Site Reliability Metrics|2.1.7|2023-11-02|
|Site Reliability Metrics UX|2.1.7|2023-11-02|
|Site Reliability Operations|14.2.3|2024-05-09|
|Skill Rule|1.0.3|2026-03-12|
|Skills foundation|10.1.0|2026-06-16|
|Skills Industry Data|2.2.0|2026-06-16|
|Skills Workspace|6.1.0|2025-12-11|
|Slack Activities for PAD|1.0.3|2023-01-12|
|Slack Chat Connector for Security Incident Management|1.0.1|2025-05-01|
|Slack Spoke|1.8.0|2025-09-10|
|SLO - Foundation|2.0.2|2026-09-10|
|SLO - Prime|2.0.0|2026-09-10|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Smart Assessment Collaboration|22.3.0|2026-06-16|
|Smart Assessment Core|23.0.2|2026-09-10|
|Smart Assessment Migration tools|23.0.3|2026-09-10|
|SmartRecruiters Spoke|1.0.0|2021-11-18|
|Smartsheet Spoke|2.6.1|2026-01-20|
|sn-4q-bubble|23.2.3|2026-06-16|
|sn-actionable-insights|1.2.1|2026-08-07|
|sn-apm-diagram-builder|3.7.0|2026-06-16|
|sn-app-analytics-center|8.4.1|2026-07-09|
|sn-app-analytics-center|8.4.1|2026-07-09|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-kpi|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-analytics-workflow-source|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-kpi-details|8.0.1|2026-03-12|
|sn-app-par-components-chart-drilldown-configuration|8.4.3|2026-07-09|
|sn-app-par-components-chart-drilldown-configuration|8.4.3|2026-07-09|
|sn-app-par-components-component-builder|8.4.3|2026-07-09|
|sn-app-par-components-component-builder|8.4.3|2026-07-09|
|sn-app-par-components-config-panel|8.4.3|2026-07-09|
|sn-app-par-components-config-panel|8.4.3|2026-07-09|
|sn-app-par-components-config-panel-section-message|8.4.3|2026-07-09|
|sn-app-par-components-config-panel-section-message|8.4.3|2026-07-09|
|sn-app-par-components-create-dashboard-modal|8.4.3|2026-07-09|
|sn-app-par-components-create-dashboard-modal|8.4.3|2026-07-09|
|sn-app-par-components-create-indicator-modal|8.4.3|2026-07-09|
|sn-app-par-components-create-indicator-modal|8.4.3|2026-07-09|
|sn-app-par-components-dashboard-categories|8.4.3|2026-07-09|
|sn-app-par-components-dashboard-categories|8.4.3|2026-07-09|
|sn-app-par-components-data-visualization-wrapper|8.4.3|2026-07-09|
|sn-app-par-components-data-visualization-wrapper|8.4.3|2026-07-09|
|sn-app-par-components-divider|8.4.3|2026-07-09|
|sn-app-par-components-divider|8.4.3|2026-07-09|
|sn-app-par-components-dynamic-renderer|8.4.3|2026-07-09|
|sn-app-par-components-dynamic-renderer|8.4.3|2026-07-09|
|sn-app-par-components-export-email-composer|8.4.3|2026-07-09|
|sn-app-par-components-export-email-composer|8.4.3|2026-07-09|
|sn-app-par-components-export-modal|8.4.3|2026-07-09|
|sn-app-par-components-export-modal|8.4.3|2026-07-09|
|sn-app-par-components-info-content|8.4.3|2026-07-09|
|sn-app-par-components-info-content|8.4.3|2026-07-09|
|sn-app-par-components-info-panel|8.4.3|2026-07-09|
|sn-app-par-components-info-panel|8.4.3|2026-07-09|
|sn-app-par-components-insights-panel|8.4.3|2026-07-09|
|sn-app-par-components-insights-panel|8.4.3|2026-07-09|
|sn-app-par-components-library-recommendation-widgets|8.4.3|2026-07-09|
|sn-app-par-components-library-recommendation-widgets|8.4.3|2026-07-09|
|sn-app-par-components-saved-data-visualization|8.4.3|2026-07-09|
|sn-app-par-components-saved-data-visualization|8.4.3|2026-07-09|
|sn-app-par-components-scheduled-export|8.4.3|2026-07-09|
|sn-app-par-components-scheduled-export|8.4.3|2026-07-09|
|sn-app-par-components-share-dialog|8.4.3|2026-07-09|
|sn-app-par-components-share-dialog|8.4.3|2026-07-09|
|sn-app-par-components-share-info|8.4.3|2026-07-09|
|sn-app-par-components-share-info|8.4.3|2026-07-09|
|sn-app-par-coreui-migration-center|4.0.3|2026-03-12|
|sn-app-par-coreui-migration-legacy-widget|4.0.3|2026-03-12|
|sn-app-par-nacm-component|8.4.3|2026-07-09|
|sn-app-par-nacm-component|8.4.3|2026-07-09|
|sn-attach-article-guidance|32.0.1|2026-09-10|
|sn-attach-article-guidance|32.0.1|2026-09-10|
|sn-circuit-map|5.0.0|2025-07-31|
|sn-circuit-map|5.0.0|2025-07-31|
|sn-circuit-map|5.0.0|2025-07-31|
|sn-cmdb-nlq-search|2.3.3|2024-11-07|
|sn-component-account-hierarchy|29.0.7|2026-03-12|
|sn-component-account-hierarchy|29.0.7|2026-03-12|
|sn-component-guidance-experience|42.0.2|2026-09-10|
|sn-component-guidance-experience|42.0.2|2026-09-10|
|sn-component-workspace-ribbon|30.0.0|2026-03-12|
|sn-component-workspace-ribbon|30.0.0|2026-03-12|
|sn-component-workspace-shn|29.0.7|2026-03-12|
|sn-component-workspace-shn|29.0.7|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|sn-csm-custom-activity-tile|4.3.1|2026-03-12|
|sn-cwm-agile|2.2.1|2026-09-10|
|sn-dashboard|8.4.4|2026-07-09|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-dashboards-view|29.0.1|2026-03-12|
|sn-docintel-iframe|1.0.4|2024-02-01|
|sn-docs|7.9.1|2026-09-10|
|sn-formula-kit|1.2.2|2026-09-10|
|sn-guided-action-experience|39.0.1|2025-12-11|
|sn-guided-action-experience|39.0.1|2025-12-11|
|sn-guided-action-experience|39.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-guided-action-playbook-card|33.0.1|2025-12-11|
|sn-hla-admin-experience|1.0.2|2026-01-20|
|sn-hr-casecard|1.3.2|2025-12-11|
|sn-ia-summary-card|1.1.0|2026-08-07|
|sn-itom-ui-internal|27.1.1|2025-12-11|
|sn-next-best-action-list|41.0.4|2026-09-10|
|sn-next-best-action-list|41.0.4|2026-09-10|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-analytics|29.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|sn-nlq-query-input|30.0.1|2026-03-12|
|Snowflake Spoke|1.0.3|2025-09-10|
|sn-quick-filter-popover|24.3.1|2026-05-05|
|sn-rack|4.0.0|2025-07-31|
|sn-rack|4.0.0|2025-07-31|
|sn-rack|4.0.0|2025-07-31|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|sn-reusable-impact-framework|22.3.2|2026-06-16|
|sn-smart-assessment-connected|23.0.4|2026-09-10|
|sn-smart-assessment-designer|23.0.5|2026-09-10|
|sn-timer|2.0.1|2026-03-12|
|sn-topology-map|4.0.0|2025-07-31|
|sn-topology-map|4.0.0|2025-07-31|
|sn-topology-map|4.0.0|2025-07-31|
|sn-ui-builder-templates|25.0.4|2024-02-01|
|sn-uxf-formula-parser|29.1.0|2026-03-12|
|sn-viz-designer|8.4.1|2026-07-09|
|sn-viz-designer|8.4.1|2026-07-09|
|Socure Spoke|1.2.2|2026-03-12|
|Software Asset Management for CPE support|1.0.0|2022-08-04|
|Software Asset Management Guided Experiences|7.0.1|2026-03-12|
|Software Asset Management integration with Salesforce CRM|2.0.1|2025-12-11|
|Software Asset Management integration with Salesforce Marketing Cloud|1.2.7|2025-03-12|
|Software Asset Management integration with Tableau|1.0.1|2024-08-01|
|Software Asset Management integration with Workday|1.0.12|2025-01-30|
|Software Asset Management Professional for Engineering Applications|1.0.3|2026-03-12|
|SOM - Advanced|1.0.1|2026-04-09|
|SOM - Prime|1.0.1|2026-04-09|
|Source-to-Pay Common Architecture|25.0.0|2026-09-10|
|Source-to-Pay Integration Framework|14.0.2|2026-06-16|
|Source-to-Pay Operations with Contract Management Pro|2.0.1|2025-05-01|
|Source-to-Pay Workspace|21.0.0|2026-09-10|
|Sourcing and Purchasing Automation|11.7.0|2026-09-10|
|SOW Funnel Highchart Component|28.3.1|2026-03-12|
|Special Handling Instruction|26.0.3|2026-05-05|
|Spend and Savings Management|5.0.5|2026-08-07|
|Splunk Search Integration for Security Operations|10.5.0|2025-07-31|
|SPM Benchmarking|1.0.0|2022-11-03|
|SPM Common UI Component|4.1.1|2026-09-10|
|SPM Team Member|1.0.0|2026-04-09|
|SPO - Foundation|2.0.0|2026-09-10|
|Spoke Generator|4.2.4|2026-03-12|
|SPO - Prime|2.0.0|2026-09-10|
|SPW Jira Integrations|1.0.0|2025-12-11|
|Standard ticket page summarization|1.3.3|2026-08-07|
|Status Report UI Component for MSIM Workspace|1.0.2|2024-11-07|
|Strategic Planning|4.18.0|2026-09-10|
|Strategic Portfolio Management - Advanced|1.3.0|2026-09-10|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management for Telecom Project Templates|2.0.0|2025-12-11|
|Strategic Portfolio Management - Prime|1.2.0|2026-09-10|
|Strategic Spend Tracking for PPM|1.2.0|2025-12-11|
|Stream Connect Designer|5.0.1|2026-03-12|
|SuccessFactors Learning Spoke|1.0.0|2025-01-30|
|Summarization for Order Management|2.2.4|2026-09-10|
|SumTotal Spoke|1.1.0|2023-03-02|
|Supplier Case Management|12.0.0|2026-09-10|
|Supplier Collaboration Portal|12.0.0|2026-09-10|
|Supplier Common Architecture|12.0.0|2026-09-10|
|Supplier Operations|8.0.0|2026-09-10|
|Supplier Payment Optimization|7.0.0|2026-09-10|
|Supplier Relationship and Performance Management|11.0.0|2026-09-10|
|SurveyMonkey Spoke|2.0.6|2024-08-01|
|Surveys for mobile|1.0.2|2021-09-16|
|Sustainable IT|21.1.0|2025-12-11|
|Synthetic Monitoring|1.4.4|2025-12-11|
|System Events and Jobs Dashboard|3.1.5|2026-03-12|
|Tableau Spoke|1.0.2|2024-08-01|
|Tag Based Alert Clustering Engine|18.24.0|2026-06-16|
|Tag Governance|1.8.0|2025-12-11|
|Talent Development Core|5.5.0|2026-06-16|
|Talent feedback|1.4.1|2026-08-07|
|Talent profile|7.0.1|2026-07-09|
|Task activity timeline|25.4.0|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Task activity timeline|25.4.0|2025-12-11|
|Task Communications Management UI Components for Configurable Workspaces|9.4.3|2026-09-10|
|Task Intelligence Admin Console|5.2.1|2025-12-11|
|Task Intelligence for Customer Service|25.4.0|2025-12-11|
|Task Intelligence for ITSM|8.2.1|2025-12-11|
|Task Plan Template AI Agents|2.0.1|2026-09-10|
|Task Plan Templates|5.0.0|2026-09-10|
|Task Quality Review Management|29.1.1|2026-03-12|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Tasks for mobile|27.1.0|2024-11-07|
|Task SLA cards|26.0.0|2026-03-12|
|Task SLA cards|26.0.0|2026-03-12|
|Team Contacts App Template|28.2.1|2025-12-11|
|Team Performance|202507.0.2|2025-07-31|
|Technician driven sales with Field Service|29.1.2|2026-03-12|
|Technology Core|3.8.4|2026-06-16|
|Technology Core|3.8.4|2026-06-16|
|Technology Portfolio Management|1.10.0|2026-06-16|
|Telecom Core|6.6.2|2026-07-09|
|Telecom Discovery Patterns|1.0.2|2025-12-11|
|Telecommunication Open APIs|6.0.9|2025-12-11|
|Telecommunications Alarm Management Open API|7.0.1|2025-12-11|
|Telecom Service Operations Core|1.2.1|2025-12-11|
|telemetry-data-connector|2.1.0|2026-08-07|
|Territory Planning|30.0.3|2026-03-12|
|Test Generation|4.0.11|2025-12-11|
|Theme Builder|6.1.5|2026-01-22|
|Theme Builder AI|1.1.0|2026-05-05|
|Third-party Risk Due Diligence|23.0.5|2026-09-10|
|Third-party Risk Management|23.0.7|2026-09-10|
|Threat Intelligence|13.4.4|2026-02-05|
|Threat Intelligence Security Center - Advanced|3.3.1|2026-09-10|
|Threat Intelligence Security Center for Security Operations|4.8.1|2026-09-10|
|Threat Intelligence Security Center integration with CrowdStrike Intelligence|3.0.4|2025-03-12|
|Threat Intelligence Security Center integration with Elasticsearch|3.0.4|2025-05-01|
|Threat Intelligence Security Center integration with Microsoft Defender for Endpoint|1.0.4|2025-06-05|
|Threat Intelligence Security Center Integration with Palo Alto Networks NGFW|2.0.1|2025-03-12|
|Threat Intelligence Security Center integration with Shodan|1.0.7|2025-05-01|
|Threat Intelligence Security Center integration with Splunk Search|3.0.5|2025-03-12|
|Threat Intelligence Security Center integration with VirusTotal|3.0.3|2025-03-12|
|Threat Intelligence Security Center integration with WHOIS|5.0.4|2025-03-12|
|Threat Intelligence Support Common|13.8.0|2026-09-10|
|Threat Intelligence Support Common UI Components|1.1.4|2025-12-11|
|Timeline component|29.0.0|2026-03-12|
|Time Off Request App Template|28.2.1|2025-12-11|
|TNI - Advanced|2.3.0|2026-09-10|
|TNI - Advanced|2.3.0|2026-09-10|
|TNI and DCNAM AI Content Collection|2.3.0|2026-09-10|
|TNI and DCNAM AI Content Collection|2.3.0|2026-09-10|
|Total Cost of Ownership|1.1.0|2026-06-16|
|Touchpoint Meeting|3.0.7|2026-08-07|
|Touchpoint Meeting|3.0.7|2026-08-07|
|Transporter|2.3.29|2026-08-07|
|Trello Spoke|1.4.0|2025-11-06|
|Triggers|29.0.2|2026-03-12|
|Twilio Spoke|1.2.0|2023-02-02|
|UCF Spoke|1.1.0|2023-05-04|
|Udemy Spoke|1.0.2|2022-12-01|
|UI Builder|29.6.11|2026-09-10|
|UI Components for Customer Portals|5.1.0|2026-09-10|
|UI Components of Collaboration for Configurable Workspaces|9.4.2|2026-09-10|
|UiPath Spoke|2.5.1|2025-11-06|
|UI shared library|1.6.2|2026-06-16|
|UKG Spoke|3.5.0|2025-12-11|
|Unified Content Management|23.0.5|2026-09-10|
|Unified Security Exposure Management|31.3.1|2026-09-10|
|Universal Request for Source-to-Pay Operations|1.2.2|2026-06-16|
|Universal Request integration with Microsoft Teams|1.0.2|2022-12-01|
|Universal Task|2.8.0|2026-06-16|
|Urjanet ESG integration|21.1.1|2025-12-11|
|Usage Insights Application|6.4.2|2026-09-10|
|Usage Insights Commons|6.4.2|2026-09-10|
|Usage Insights Commons Connected|6.4.2|2026-09-10|
|Usage Insights Funnel|6.1.12|2026-03-12|
|Usage Insights Funnel Core|6.4.2|2026-09-10|
|Usage Insights in Data Visualizations|6.4.2|2026-09-10|
|Usage Insights Pages|6.4.2|2026-09-10|
|Usage Insights Query Builder|6.4.2|2026-09-10|
|Usage Insights Query Builder Core|6.4.2|2026-09-10|
|Usage Insights Request Manager|6.4.2|2026-09-10|
|User Experience Analytics API|3.1.2|2024-02-01|
|User Experience Redirection|1.0.1|2026-03-12|
|User Sense|1.1.13|2025-12-11|
|Utility Actions Spoke|1.3.0|2024-10-03|
|UX Commons|27.0.2|2025-07-31|
|Vaccination Status|1.25.0|2025-12-11|
|Value stream artifacts|2.3.0|2026-06-16|
|Vault Console|2.2.9|2026-08-07|
|Vendor Manager Workspace|3.5.0|2024-11-07|
|Vendor Risk Management integration with EcoVadis|21.1.1|2025-12-11|
|Verifi Spoke|1.0.0|2024-08-01|
|Virtual Agent Adapter Common|6.2.5|2026-06-16|
|Virtual Agent API|4.4.3|2026-09-10|
|Virtual Agent for PPM|1.0.1|2023-05-04|
|Virtual Agent for Source-to-Pay Operations|3.11.0|2025-07-31|
|Virtual Agent Topic Recommendations|4.5.5|2024-08-01|
|Virtual Machine Management for Virtual Agent|3.0.11|2023-08-03|
|Visa Spoke|2.2.2|2025-12-11|
|Visibility Content|6.35.0|2026-09-10|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice Controls Simulator Tool|1.1.0|2025-12-11|
|Voice input for Now Assist|1.5.0|2026-07-09|
|Vonage Spoke|1.2.0|2025-12-11|
|Vulnerability Crisis Management|1.0.1|2024-08-01|
|Vulnerability Exposure Assessment|5.2.3|2025-12-11|
|Vulnerability Response Integration Framework|1.6.4|2026-09-10|
|Vulnerability Response Integration with Agile Management|1.2.2|2025-07-31|
|Vulnerability Response Integration with Atlassian Jira|1.0.4|2024-05-09|
|Vulnerability Response Integration with Black Duck|1.1.1|2025-12-11|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Defender for IoT \(On-premises Management Console\)|2.0.2|2024-11-07|
|Vulnerability Response Integration with Microsoft Threat and Vulnerability Management|2.8.1|2025-12-11|
|Vulnerability Response Integration with NVD|1.7.2|2025-07-31|
|Vulnerability Response Integration with Palo Alto Networks Prisma Cloud Compute|3.5.0|2025-12-11|
|Vulnerability Response Integration with Palo Alto Prisma Cloud|2.8.0|2025-12-11|
|Vulnerability Response Integration with Tenable|5.2.1|2025-12-11|
|Vulnerability Response Integration with Veracode|4.7.3|2025-12-11|
|Vulnerability Response Licensing and Usage|2.12.0|2026-09-10|
|Vulnerability Response Mobile|11.1.1|2023-05-04|
|Vulnerability Response Patch Orchestration|2.2.5|2025-05-01|
|Vulnerability Response Patch Orchestration with HCL Bigfix|1.3.0|2025-05-01|
|Vulnerability Response Patch Orchestration with Microsoft SCCM|2.3.1|2025-05-01|
|Vulnerability Solution Management|10.4.3|2022-12-01|
|Walk-up Experience for Service Operations Workspace|9.4.2|2026-09-10|
|Walk-Up for CSM|2.0.1|2026-03-12|
|Watershed integration for ESG|16.0.1|2023-02-02|
|WDF Unified Hub|1.1.0|2026-07-09|
|WebRTC Voice|1.0.7|2026-09-10|
|Whats New Framework Core|1.3.1|2026-03-12|
|WHOIS Integration for Security Operations|10.4.0|2024-08-01|
|Word Document Templates|1.9.7|2026-01-20|
|Workday ESG integration|21.1.1|2025-12-11|
|Workday Financials Spoke|2.1.0|2025-07-31|
|Workday HR Spoke|2.7.0|2025-12-11|
|Workday Learning Spoke|1.1.4|2024-04-04|
|Workflow Studio|29.2.2|2026-08-07|
|Workforce Optimization Common|1.7.0|2025-12-11|
|Workforce Optimization Configurable Workspace Core|1.11.0|2025-12-11|
|Workforce Optimization Configurable Workspace UI Components|4.4.1|2025-12-11|
|Workforce Optimization for CSM Configurable Workspace|4.5.0|2025-12-11|
|Workforce Optimization for HR|1.1.2|2025-07-31|
|Workforce Optimization integration with Microsoft Outlook|1.3.0|2025-12-11|
|Workfront Spoke|1.3.0|2025-11-06|
|Work Item Integrations Common|1.15.0|2026-06-16|
|Workplace Agent for mobile|1.4.5|2026-03-12|
|Workplace Case Management|1.28.8|2026-07-09|
|Workplace Central|1.16.5|2026-07-09|
|Workplace Concierge|1.7.11|2026-07-09|
|Workplace Connectors|2.3.8|2026-08-07|
|Workplace from Facebook Spoke|4.2.1|2025-11-06|
|Workplace Indoor Map Component|1.1.1|2024-08-01|
|Workplace Indoor Mapping|1.18.6|2026-07-09|
|Workplace Lease Administration|1.8.5|2026-07-09|
|Workplace Maintenance Management|1.11.5|2026-07-09|
|Workplace Move Management|1.14.5|2026-07-09|
|Workplace PPE Inventory Management|1.18.0|2025-07-31|
|Workplace Reservation Management|3.6.1|2026-08-07|
|Workplace Reservations for Microsoft Outlook Add-in|1.12.2|2025-07-31|
|Workplace Service Delivery Enterprise|1.6.0|2025-12-11|
|Workplace Service Delivery for Mobile|1.16.2|2025-12-11|
|Workplace Service Delivery integration with Microsoft Places|1.2.5|2025-12-11|
|Workplace Service Delivery Professional|1.4.0|2025-12-11|
|Workplace Service Delivery Suite|2.17.2|2025-12-11|
|Workplace Services Kiosk|1.5.2|2025-12-11|
|Workplace Space Management|1.20.13|2026-08-07|
|Workplace Space Mapping|1.20.5|2026-06-16|
|Workplace Stack Plan|1.5.12|2026-06-16|
|Workplace Visitor Management|2.1.1|2026-08-07|
|Work Progress Status for Agile Teams|1.0.4|2025-06-05|
|Work Progress Status for SAFe|1.0.4|2025-06-05|
|Workspace App Shell|29.1.1|2026-03-12|
|Workspace Builder for App Engine|28.2.0|2025-12-11|
|Workspace Inspector|20.1.1|2025-05-01|
|Workspace navigation and experience demo|27.1.1|2026-03-12|
|Wrike Spoke|1.3.0|2025-09-10|
|WSD - Advanced|1.0.2|2026-06-16|
|WSD - Foundation|1.0.2|2026-06-16|
|WSD - Prime|1.0.2|2026-06-16|
|X Spoke|2.3.0|2025-09-10|
|YouTube Spoke|1.0.5|2025-07-10|
|Zendesk Spoke|1.8.0|2025-11-06|
|Zero Copy Connector for ERP|10.0.9|2026-05-05|
|Zoom extension for Omnichannel Callback|1.3.6|2025-07-31|
|Zoom Spoke|4.6.2|2026-01-20|

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/available-versions.md)


---
title: Australia Patch 7
description: The Australia Patch 7 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/australia-patch-7.html
release: australia
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 91
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 7

The Australia Patch 7 release contains important problem fixes.

-   **Australia Patch 7 was released on October 08, 2026.**
    -   Build date: 10-06-2026\_0905
    -   Build tag: glide-australia-02-11-2026\_\_patch7-09-17-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A07.00.xlsx).

## Overview

Australia Patch 7 includes 559 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-ap7.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Australia Patch 7 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 7, refer to [KB3152248](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3221587).

## Changes in Australia Patch 7

-   **[Monitoring Now Assist usage in Subscription Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/monitoring-now-assist-usage.md)**






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
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

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

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/available-versions.md)


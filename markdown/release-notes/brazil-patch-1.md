---
title: Brazil Patch 1
description: The Brazil Patch 1 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/brazil-patch-1.html
release: brazil
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 79
breadcrumb: [Available patches and hotfixes, Learn about the Brazil release, Brazil release notes]
---

# Brazil Patch 1

The Brazil Patch 1 release contains important problem fixes.

-   **Brazil Patch 1 was released on October 08, 2026.**
    -   Build date: 10-05-2026\_1244
    -   Build tag: glide-brazil-08-25-2026\_\_patch1-09-21-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This version is being evaluated for use in the ServiceNow Government Community Cloud \(GCC\) environment.

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/brazil/rn/patches/PRBs-B01.00.xlsx).

Brazil Patch 1 includes 354 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-bp1.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Brazil Patch 1 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Brazil Patch 1, refer to [KB3220580](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3220580).

## Changes in Brazil Patch 1

-   **[Human-assisted SMS OTP authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/human-assisted-sms-otp.md)**

    Human-assisted SMS OTP lets a human agent verify an end user's identity by sending a one-time passcode via SMS during a live interaction. The agent initiates OTP generation and validation through the platform's scriptable APIs, and the consuming application \(for example, CSM or FSO workspace\) handles the agent-facing workflow and user interface.


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

IBM Authorized SAM Provider \(IASP\) integrations

 PRB2073777

 [KB3148607](https://hi.service-now.com/kb_view.do?sysparm_article=KB3148607)

</td><td>

There's out of memory issues in Software Asset Management \(SAM\)'s 'Populate vCores' job

</td><td>

The job is not able to insert any records in sam\_task\_queue, possibly because of a bug in priority calculation for cloud installs. This is due to the version upgrade for the IBM Store app.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Component API

 PRB2075538

</td><td>

In the Platform Analytics Spanish localization, search and date range filters aren't working correctly

</td><td>

Users with Spanish language settings can't search visualizations or dashboards properly, and date range filters are read-only for day selection. The problem impacts Spanish localization specifically, causing different search results and disabled date selection compared to English.

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

Survey Management

 PRB2057694

</td><td>

Incompatible guarded scripts are flagged on the UI Page assessment\_thanks \(Survey Management\), causing blocked scripts

</td><td>

Entries in the sys\_script\_execution\_log table with source page assessment\_thanks.do are marked as 'Incompatible Guarded Script'. This isn't a functional blocker and the system is working as expected.

</td><td>

1.  Open the assessment thank-you page with the injection-shaped payload in the URL.
2.  Navigate to the incompatible guarded scripts table.

 Observe the guarded scripts error and the blocked script.

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

Activity and Subscriptions

 PRB2069585

 [KB3148451](https://hi.service-now.com/kb_view.do?sysparm_article=KB3148451)

</td><td>

The 'Customer history' tab keeps loading on the front-line case page

</td><td>

The tab never loads.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB2060131

</td><td>

When table rotation is set up for sys\_audit\_relation, audit relationship events don't display in a workspace

</td><td>

 

</td><td>

1.  Navigate to **Table Rotations** \(sys\_table\_rotation\).
2.  Add a record for sys\_audit\_relation.
3.  Set the type to 'Extension' and the 'Duration' to one hour or less.
4.  Create audit relationship changes.

 Expected behavior: The audit relationship changes are displayed in the workspace activity stream.

 Actual behavior: The audit relationship changes aren't displayed.

</td></tr><tr><td>

Activity Stream

 PRB2066570

 [KB3150759](https://hi.service-now.com/kb_view.do?sysparm_article=KB3150759)

</td><td>

There's an activity stream primary journal field ordering regression — work\_notes are displayed before comments in UI16 and Service Portal

</td><td>

The activity stream on task records \(Incidents, Changes, etc.\) incorrectly defaults to the 'Work Notes' input instead of 'Comments' in both the platform UI and Service Portal. This affects user workflow as agents may inadvertently post internal work notes when intending to post user-visible comments. Additionally, custom journal fields configured on tables don't appear in the Service Portal activity stream widget.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB2073311

</td><td>

Build backend graphQL endpoint for List Activity

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2073313

</td><td>

Provide supplemental data for returned records on the new back-end for list activity

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2073315

</td><td>

Review DT APIs for security

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB2083047

</td><td>

The backend should always display a color for activity stream fields

</td><td>

The background color is blank: &lt;span class='sn-stream-input-decorator' style='background-color: '&gt;&lt;/span&gt;.

</td><td>

1.  Make sure glide.ui.activity\_stream.style.comments is set to 'transparent'.
2.  Open any case.
3.  Navigate to the 'Comments and Work Notes' section.
4.  Inspect the **Additional comments \(CUSTOMER VISIBLE\)** text field.

 Expected behavior: The background color is transparent: &lt;span class='sn-stream-input-decorator' style='background-color: transparent'&gt;&lt;/span&gt;.

 Actual behavior: The background color color is blank: &lt;span class='sn-stream-input-decorator' style='background-color: '&gt;&lt;/span&gt;.

</td></tr><tr><td>

Agent Chat

 PRB2077124

</td><td>

A tab subheading displays 'Call is in wrap-up' while a call is still active in an agent-initiated wrap-up scenario

</td><td>

When an agent selects 'Open Wrap-Up' mid-call, the tab subheading immediately changes to 'Call is in wrap-up' even though the voice call is still ongoing. This is misleading. The label implies the interaction is in wrap-up state, but the call has not yet ended. UX has confirmed the label should be changed to 'Wrap-up initiated' — a generic label that works accurately for both mid-call and post-call scenarios.

</td><td>

1.  Configure an NVC/CCaaS integration with supportExternalWrapUp = true on the Wrap Up macroponent.
2.  Start a voice call as an agent.
3.  While the call is still active, select the **Open Wrap-Up** button.

 Observe the tab subheading. It immediately displays 'Call is in wrap-up' even though the call is still ongoing.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB2085529

</td><td>

AI Agent execution tool 'AIA RAG Retriever' returns faulty URLs for search result items in VA and ES

</td><td>

When the RAG/semantic-search result's URL omits the leading forward slash, the resulting link is corrupted and unusable.

</td><td>

 

</td></tr><tr><td>

AI Gateway - Security

 PRB2088199

</td><td>

Domain separation support for AI Control Tower \(AICT\) features

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1975413

</td><td>

AI Search Dynamic filters extension point impl isn't triggered from a non-global scope

</td><td>

When an AI Search scriptable API provided is executed from both global and sn\_nb\_action scopes, the extension point implementation doesn't get triggered when the scope is not global \(sn\_nb\_action\).

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2020989

</td><td>

Performance and EVAM-related debug messages no longer appear in sys log for async GRs and Virtual Agent searches

</td><td>

When the system properties glide.search.performance .logger.enabled or glide.search.evam .logger.enabled are set to true, messages should appear in the sys log prefaced with \[SEARCH PERFORMANCE\] or \[SEARCH EVAM\] respectively. However, these messages no longer appear in the syslog when a conversation is part of the logging context.

</td><td>

1.  Open an instance that returns synth response in portal \(for example, Dynamic Window setup\).
2.  Create and set glide.search.evam.logger.enabled to true.
3.  Perform a search that returns a synthesized response in portal.
4.  Open the sys log and search for recent messages containing 'for Genius Result with table'.

 Expected behavior: There's a log entry in sys log specifying the ID of the view config that was used for each genius result.

 Actual behavior: There are no log entries for GR EVAM View Config selection.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2073308

</td><td>

Catalog enrichment for glide AIS

</td><td>

This is a product update.

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
3.  Verify that there's an entry in the ais\_guard\_rail\_ limit\_data\_source table.
4.  Change the retention policy on the indexed source to three years.

 The entry isn't recalculated in ais\_guard\_rail\_ limit\_data\_source.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2076604

</td><td>

Expose glide.ais.query.server \_side\_reranker\_enabled in BP0 for reranker to be enabled by default

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2080317

</td><td>

getNextPaginationToken\(\) and getPreviousPaginationToken\(\) method entry is removed from the glide-plugin-members.xml file

</td><td>

 

</td><td>

1.  Navigate to the track/bnowassist branch of Glide repo.
2.  Open the glide-plugin-members.xml file under the Glide folder.

 Observe that the getNextPaginationToken\(\) and getPreviousPaginationToken\(\) entry is removed for RAGRetrievalResponse.

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

During the upgrade from Australia Patch 6 to Australia Patch 7, the search doesn't work from the SP page.

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

 Actual behavior: The **Genius Results** field indicates a synthesized response was displayed, and **Has Results** is true.

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

 Expected behavior: Content is not cut off at 200% and 400% zoom.

 Actual behavior: Content is cut off at 200% and 400% zoom.

</td></tr><tr><td>

AI Search UX

 PRB2083562

</td><td>

Support right-click behavior for Service Portal search results

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

App AutoUpgrade Client

 PRB2071164

</td><td>

App Client sends all installed apps to Store instead of SN Managed only

</td><td>

App Client calls Store API/autoupgrade/poll with all the apps listed in the sys\_store\_app table instead of SN Managed only apps. The sys\_store\_app table is missing the sn\_managed column and the GlideRecord returns all apps as a result.

</td><td>

 

</td></tr><tr><td>

App AutoUpgrade Client

 PRB2082909

</td><td>

Package.json is missing the 'now' block, causing 'Verify Artifact ID' to fail for the app-autoupgrade-client HF release

</td><td>

When the user selects 'Verify Artifact ID' on the HF version record 'SR - ALM - Auto Upgrade Client 1.0.0 - HF', the following error is shown: 'Package.json is missing for: app-autoupgrade-client \(1.0.1\)'. This is because the package.json in the auto-upgrade-client repo is missing the required 'now' block. Without this block, BT1 can't read app identity, compatibility, and dependency metadata from the artifact.

</td><td>

1.  Navigate to **BT1** &gt; **Versions** &gt; **SR - ALM - Auto Upgrade Client 1.0.0 - HF**.
2.  Set the build artifact to app-autoupgrade-client-1.0.1-app.zip.
3.  Select **Verify Artifact ID**.

 Observe that the following error appears: 'Package.json is missing for: app-autoupgrade-client \(1.0.1\)'.

</td></tr><tr><td>

Application Manager

 PRB2056916

</td><td>

Skip a license-blocked status for all dependencies in DependencyProcessor

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB2074238

</td><td>

Now Assist to Otto rename for Application Manager

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2066684

</td><td>

Match KB identification phone numbers are ignoring special characters

</td><td>

Questions with the category 'phone number' aren't matched against formatted stored phone numbers during voice agent identification flow.

</td><td>

 

</td></tr><tr><td>

Base Asset Management

 PRB2064689

</td><td>

The 'Asset' role isn't able to read work orders

</td><td>

 

</td><td>

1.  Create a user temp\_asset\_only\_role with the 'Asset' role.
2.  Open the asset that has the work order in Asset Workspace or Hardware Asset Workspace.

 When there's at least one work order in the right side context pane of 'Asset Lifecycle events', the count of Work Order is displayed, but **View Records** is turned off. The reason is the user doesn't have the access to see the work orders.

</td></tr><tr><td>

Base Asset Management

 PRB2082690

 [KB3159012](https://hi.service-now.com/kb_view.do?sysparm_article=KB3159012)

</td><td>

The 'Playbook' tab for reviewing contract data extraction is missing on the 'Contract record' page in the IT Asset Management \(ITAM\) workspace for Hardware Asset Management \(HAM\) + Contract Management \(CM\) Pro instances

</td><td>

This is a product update.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2064243

</td><td>

Grant cross-scope create/update access on HR Template, HR Service, and HR Service Activity

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2086486

</td><td>

Employee certifications, licenses, and degrees

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB2075237

</td><td>

Create an implementation to setWorkflow false for a table in the Case Management Core scope

</td><td>

Currently, the multi-case creation takes too much time. To solve the issue, setWorkflow should be set as false. setWorkflow can't be set as false to case management tables from the task plan template scope. Thus, an implementation should be added in the case management scope, which sets setWorkflow false for case and case task tables.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2079091

</td><td>

The sys\_ids for 12 change lockdown files conflict with many other files in different places

</td><td>

12 lockdown files have their sys\_id genuinely reused elsewhere. The own-filename-id's match on both sides, false-positive ACL↔role refs are excluded, and high-count IDs are fully paginated so nothing's truncated.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2086715

</td><td>

The change request dynamic schema store field max length is set to 40 instead of 5000

</td><td>

The existing max\_length is defaulted to 40 when created through XML.

</td><td>

1.  Navigate to sys\_dictionary list.
2.  Filter for column name as risk\_and\_compliance\_attributes and table as change\_request.
3.  Open the record.
4.  Select **Show XML**.
5.  Validate the **max\_length** field.

 Expected behavior: The max\_length is 5000.

 Actual behavior: The existing max\_length is defaulted to 40 when created through XML.

</td></tr><tr><td>

Client Scripts

 PRB2078551

</td><td>

The base instance **Delete** UI action should be supported

</td><td>

The GlideModal logic for the **Delete** UI action needs to be converted into a widget and use g\_modal.showWidget instead.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB2082276

</td><td>

**Analyze Access** UI Action needs migration to work in UI26

</td><td>

When the user selects **Analyze Access**, it redirects to '/sn\_access\_analysis\_request.do...' because the Ajax request is broken. It should redirect to '/now/access-manager/...'.

</td><td>

1.  Navigate to '/aiux/ui/incident\_list.do'.
2.  Select an incident.
3.  Select and hold \(or right-click\) on the form header.
4.  Select **Analyze Access**.

 Expected behavior: It redirects to '/now/access-manager/...'.

 Actual behavior: It redirects to '/sn\_access\_analysis\_request.do...' because the Ajax request is broken.

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

The existing client script APIs \(for example, g\_modal and g\_ui\_scripts\) were only included in js\_include\_ui16\_form. They should be extracted into a dedicated js\_include and included within the list page.

</td><td>

Access NowAPI on the list action page.

 Observe that NowAPI is undefined.

</td></tr><tr><td>

Client Scripts

 PRB2084584

</td><td>

Port g\_list.refreshWithOrderBy

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB2084585

</td><td>

Port g\_list.refreshWithOrderBy

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2070558

</td><td>

Retired filter or filter condition filter of lookup table \(serial number\) isn't applied to main CI

</td><td>

If the main CI has an applicable filter \(like a static condition or a retired filter\), the CI found by the lookup filter condition may find the main CI, where a filter applies but the filter isn't used.

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

The existing UI flows should be preserved, but there's a new default-on state. Buttons, labels, and text should align for the default-on state. When there are results and dynamic IRE is on, difference sampling shouldn't show the dashboard or have another action to load the dashboard.

</td><td>

 

</td></tr><tr><td>

CMDB Workspace

 PRB2085730

</td><td>

When Dynamic Identification and Reconciliation Engine \(IRE\) is turned on, there should be a banner added to the 'Products Highlight' section on the CMDB Workspace home page

</td><td>

1.  Turn on Dynamic IRE.
2.  Navigate to the CMDB workspace home page.

 Observe that there should be a banner in the 'Product Highlights' section with a View details button that links to the Dynamic IRE home page.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB2082949

</td><td>

The space character intermittently drops/auto-removes while typing in the **Value** field, causing words to merge

</td><td>

In the list view for Condition Builder \(filter builder on the 'Conditions' tab\), typing continuously into a condition's **Value** input field causes the space bar presses to behave unreliably. In some instances, the space is never registered at all; in others, it's inserted and then removed a moment later. The next character then lands immediately adjacent to the previous word, merging two words into one. For example, typing 'Trigger NA FTS on priority' produces TriggerNA FTSon priority, silently losing the spaces after 'Trigger' and after 'FTS'.

</td><td>

1.  Open the Cases list \(Case Service Management\).
2.  In the list view, navigate to the 'Conditions' tab to open the Condition Builder.
3.  Add the following condition: Field = Subject, Operator = is.
4.  Select into the **Value** input.
5.  Type a multi-word phrase continuously without pausing between words \(for example, 'Trigger NA FTS on priority'\).

 Expected behavior: Every space keystroke is registered and retained exactly where typed, as in any standard text field.

 Actual result: The space keystrokes intermittently fail to persist. They're either dropped entirely or inserted and then auto-removed a frame later, causing adjacent words to merge \(TriggerNA, FTSon\).

</td></tr><tr><td>

Condition Builder

 PRB2085904

</td><td>

The related list **Filter** icon and conditions don't appear on NS tables

</td><td>

This occurs after the Brazil upgrade.

</td><td>

1.  Log in to an instance as an internal user.
2.  Open any table \(for example, core\_company or sn\_customerservice\_case\).
3.  Select the **Related list** button at the bottom.
4.  Try to apply a filter on the related list records via the **Filter** icon.

 Expected: The user can apply filters on the related list records using the **Filter** icon.

 Actual: The **Filter** icon and conditions don't appear on the related list.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB2051128

</td><td>

The com.snc.cmdb.csdm plugin and fix script takes a long time during the Australia to Brazil upgrade

</td><td>

During the Australia to Brazil upgrade, the com.snc.cmdb.csdm plugin and fix script \(sys\_script\_fix\_ 092edb07370d4310ae 55191964924bf3.xml\) take a long time, from 44 minutes to 35 hours.

</td><td>

 

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

Core UI Interactive Filters

 PRB2073810

 [KB3154499](https://hi.service-now.com/kb_view.do?sysparm_article=KB3154499)

</td><td>

Selecting the pie chart legend/label does not filter visualizations correctly

</td><td>

The pie visualization acting as an interactive filter does not apply the filter correctly when the legend items are selected.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Customer Operations for Customer Service Management

 PRB2075902

</td><td>

Cmn\_location creation fails with 'Record not found' in CSM/CSP for authorized contact/consumer

</td><td>

 

</td><td>

1.  Log in as the authorized contact/consumer.
2.  Select the **New** button to create a cmn\_location record.

 Observe that 'Record not found' is shown immediately in CSM/CSP and no form renders.

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

 PRB2017978

</td><td>

The RefCopy job experiences performance issues for columnar archive tables

</td><td>

The slow query table shows the average SQL execution time.

</td><td>

Enable the **Retain reference** option for the incident table's archive rule.

 Notice that when checking the slow query table, the user can find the average SQL execution time.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2039435

</td><td>

The URC can run slowly when executing the row count estimation on the columnar table

</td><td>

 

</td><td>

1.  Install Live Archive on an instance.
2.  Offload a large amount of data.
3.  Create a URC rule like for sys\_flow\_plan\_context\_binding which has a document table reference.

 Expected behavior: The URC runs as expected.

 Actual behavior: The row count estimation query is very slow.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2039436

</td><td>

The URC could run slowly when executing row count estimation on the columnar table

</td><td>

 

</td><td>

1.  Install Live Archive on an instance.
2.  Offload a large amount of data.
3.  Create a URC rule for sys\_flow\_plan\_context\_binding which has a document table reference.

 Observe the time it takes for the URC to run.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2054270

</td><td>

Table cleaner performance issues on columnar archive tables

</td><td>

 

</td><td>

1.  Create a table cleaner rule targeting a columnar archive table.
2.  Execute the table cleaner job.

 Observe whether the rule is deactivated or not, and if no records are cleaned.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2057672

</td><td>

Global search performance issue with columnar archive tables

</td><td>

 

</td><td>

1.  Install Live Archive on an instance.
2.  Offload a large amount of data, including some task or problem tables.
3.  Ensure glide.ui.text\_search .enable\_archive\_fallback \_number\_search is set to the base instance value \(true\).
4.  Search for a task or problem number in the global search box.

 Expected behavior: The result comes back quickly.

 Actual behavior: There can be a long delay when the record has been offloaded due to point lookup with columnar/offloaded tables.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2059007

</td><td>

Prevent Data Management jobs from operating on columnar archive tables

</td><td>

In both scenarios, the DM Delete Job is attempting to run, but it's too slow

</td><td>

Scenario 1:

 1.  Create a Data Management Delete Job targeting a columnar archive table.
2.  Execute the job.

 Expected behavior: The DM Delete Job should not run on columnar archive tables. It should be skipped.

 Actual behavior: The DM Delete Job is attempting to run and it's too slow.

 Scenario 2:

 1.  Create a Data Management Update Job targeting a columnar archive table.
2.  Execute the job.

 Expected behavior: The DM Update Job should not run on columnar archive tables. It should be skipped.

 Actual behavior: The DM Update Job is attempting to run and it's too slow.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2059138

</td><td>

Increase columnar table migration thresholds

</td><td>

 

</td><td>

1.  Set up an Australia instance with Live Archive.
2.  Let the migration start and monitor the archive tables being migrated to columnar.

 Expected behavior: Only large archive tables \(&gt;10 GB\) should migrate, reducing the amount of columnar queries in the future.

 Actual behavior: Tables as small as 100 MB are being migrated, which leads to a lot of columnar queries with minimal space benefits.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB2061236

</td><td>

Leverage local tables to locate archive records in Global Search

</td><td>

 

</td><td>

1.  Install the Live Archive on an instance.
2.  Offload a large amount of data, including some task or problem tables.
3.  Search for a task or problem number which has been offloaded in the global search box.

 Expected behavior: The result should come back.

 Actual behavior: The result doesn't come back.

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

 PRB2089608

</td><td>

DB connection exhaustion is observed

</td><td>

This happens due to JVM Lock contention between the DatafabricEngineSweeper job and WorkloadIdentification .getWorkloadFromScope.

</td><td>

1.  Upgrade all app nodes \(over 20 of them\) to Brazil.
2.  Trigger the upgrade job to start DB schema changes.

 Observe that the nodes become unresponsive.

</td></tr><tr><td>

Database Persistence - WDF

 PRB2040034

</td><td>

In Australia, all database columns that start with a number have 'yy\_' added to the start of the name, causing a syntax error

</td><td>

When querying a table in the Australia release and the DB column starts with a number, it adds a 'yy\_' to the SQL query, breaking the collection of data and making a list view show nothing. Error: 'Syntax Error or Access Rule Violation detected by database \(ERROR: column x\_snc\_potatofarm \_0\_farmers0.yy\_1stname does not exist. Hint: Perhaps you meant to reference the column 'x\_snc\_potatofarm \_0\_farmers0.1stname'. Position: 259\)'.

</td><td>

1.  Create a scoped app.
2.  Create a table.
3.  Create some data on that table.
4.  Add a column whose name starts with a number.
5.  Navigate back to the list view.

 Observe that it's blank, but the count displays that there's records.

</td></tr><tr><td>

Database Persistence - WDF

 PRB2076449

 [https://support.servicenow.com/kb?id=kb\_article\_view&amp;sysparm\_article=KB3152921](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3152921)

</td><td>

A node can't start if there's a 'Formula' field on sys\_user

</td><td>

The instance node will fail to restart if there is a formula‑calculated field on the User \[sys\_user\] table. When the issue occurs, the node does not restart and logs a stack overflow error. The failure occurs during the platform's schema loading phase, preventing the instance from coming online and impacting all users.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - WDF

 PRB2080099

</td><td>

LeadingDigitLegacyColumnIT fails on Australia

</td><td>

On an Australia patch, running against Oracle, any column rename involving a column whose logical name begins with a digit fails with: 'ORA-00957: duplicate column name'. This is because the generated statement collapses the source and target names into the same identifier.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2076789

</td><td>

Update the data privacy ScriptableDataProtectionJob \_start method to restrict interactive sessions only for encrypted field anonymization

</td><td>

The API new SNC.DataProtectionJob\(\).start\(\) only works if it's called from an interactive session because there is an explicit check done. The check should only be done for policies where encrypted field anonymization is required, because CLE consent is needed for encrypted field anonymization to run.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB2082167

</td><td>

Data Privacy anonymization clone jobs aren't executed when the clone is initiated through a Clone Profile.

</td><td>

The default value of the System Profile needs to be updated from false to true so that the clean-up script is executed by default during clone operations.

</td><td>

1.  Create an anonymization policy.
2.  Mark it for cloning.

 Expected behavior: It runs once cloning completes.

 Actual behavior: The job doesn't run.

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

DevOps Change Velocity

 PRB2086647

</td><td>

Package.json should be updated

</td><td>

 

</td><td>

 

</td></tr><tr><td>

DirectSQL

 PRB2077815

</td><td>

Implicit joins should never be added for virtual fields

</td><td>

Virtual fields \(such as **dbfunctions**\) don't exist on the database and therefore never need implicit joins to a partition. The current code sends all column references through the addNeededJoinsForColumn path and incorrectly adds a self join. This can happen when the dbfunction is on a child TPH or TPP table because the ED looks like it's on a different storage table than the base table.

</td><td>

Select func\_field from tph\_child.

</td></tr><tr><td>

Discovery

 PRB2056121

</td><td>

There are incorrect or missing SNMP OID classifications, which result in SAN / fibre switches being classified as 'IP Switch'

</td><td>

Incorrect/ missing SNMP OID Classifications which result SAN / Fibre switches classified as IP Switch

</td><td>

Discover SAN / Fibre switches.

 Observe that these are classified as 'IP switch'.

</td></tr><tr><td>

Discovery

 PRB2058910

 [KB3156347](https://hi.service-now.com/kb_view.do?sysparm_article=KB3156347)

</td><td>

Typo in the script in Sensor SNMP

</td><td>

Classify 'his' instead of 'this.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Document Viewer

 PRB2038307

</td><td>

The smart document skill doesn't invoke the agent and doesn't render anything on Now Assist Panel

</td><td>

The **Ask Now Assist** smart document button doesn't work as expected. When the user selects the button, it opens the NAP, but it just shows the topics and doesn't load the summarization of the document.

</td><td>

1.  Navigate to **Contract Workspace** &gt; **Default List** &gt; **List** &gt; **Contract Requests** &gt; **All**.
2.  Open any contract request.
3.  Select the 'Contract Documents' tab.
4.  Select **Preview Document**.
5.  Select a document to preview, which opens it in a new tab.
6.  Select the **Ask Now Assist** button, which opens the NAP.

 Observe that the NAP loads for some time and then shows topics. Selecting the button again just loads the topics.

</td></tr><tr><td>

Easy Import

 PRB1817119

</td><td>

Errors appear in logs when searching for the source table name in the transform map table

</td><td>

Easy import doesn't support Document ID type columns. Document ID type columns require the table name in addition to record details.

</td><td>

 

</td></tr><tr><td>

Embedded Help

 PRB2057373

</td><td>

Instance Observers have some http connections that breach Cryptography Standard

</td><td>

Cryptography Standard \(POL0020873\), section 2.4 Data in Transit Encryption, requires TLS for all connections. SysEng: Core is decommissioning CDN HTTP endpoints to support modern ServiceNow technologies. However, Instance Observers currently depend on HTTP for some connections and can't migrate until this dependency is removed.

</td><td>

 

</td></tr><tr><td>

Employee Relations Case Management

 PRB2086483

</td><td>

HRBP and Employee Relations case assignment

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Error Framework

 PRB2035967

</td><td>

The **Reset** button doesn't work and the 'Refined Codes' section displays error codes with error\_count=0

</td><td>

The **Reset** button on the error card list component doesn't work. When the user selects the button, the filters should be reset and the same errors should be displayed. Instead, 'No actions needed' appears and no error cards are visible. Additionally, in the Discovery Admin Workspace, the 'Refined Codes' section displays error codes that have an error\_count of 0. These zero-occurrence entries represent errors that have been fully ignored \(captured in error\_ignored\_count only\) and carry no actionable significance for the user. Showing these entries pollutes the list with noise, making it harder for users to focus on error codes that actually require attention.

</td><td>

Scenario1:

 1.  Provision an instance with:
    -   The 'Error Framework' plugin \(com.glide.error\_framework\) installed.
    -   At least one source application registered in sys\_error\_appl.
    -   Errors ingested and aggregation run \(so sys\_error\_code\_stats has records with error\_count &gt; 0\).
2.  Add the error card list component to a new workspace on the 'Error Stats' page.
3.  Verify that errors are displayed.
4.  Apply a filter to enable the **Reset** button.
5.  Select the **Reset** button.

 Expected behavior: The filters are reset to defaults. The same errors are displayed.

 Actual behavior: 'No actions needed' appears. An empty state is shown, and no error cards are visible.

 Scenario 2:

 1.  Navigate to **Discovery Admin Workspace** &gt; **Diagnostics** &gt; **Errors**.
2.  Check the Refined Codes list.

 Expected behavior: Only refined codes with error\_count &gt; 0 are displayed in the Refined Codes list.

 Actual behavior: Refined codes with error\_count = 0 are displayed in the list.

</td></tr><tr><td>

Error Framework

 PRB2052849

</td><td>

Sys\_error\_\* records aren't accessible for admin\(system administrator\) users

</td><td>

Users with the admin \(system administrator\) role can't access any sys\_error\_\* tables records \(for example, sys\_error, sys\_error\_code, sys\_error\_code\_stats, and the remaining tables\).

</td><td>

1.  Log in with the admin user role.
2.  Navigate to DAW or from navigator type sys\_error\_code.LIST.

 Observe that the 'Refined Error Codes' page under the 'Diagnostics' tab doesn't render any errors code stats. The U16 list view\(sys\_error\_code.LIST\) also doesn't show any records.

</td></tr><tr><td>

Error Framework

 PRB2058677

</td><td>

Top error codes and AI Insights should use GlideRecordSecure when presenting the results

</td><td>

The 'Refined Error Codes' page applies ACL's, but the top discovery errors and AI insights don't use GlideRecordSecure.

</td><td>

Navigate to DAW as an admin user.

 Observe that the top discovery errors and AI insights display records, but the 'Refined Error Codes' page doesn't display any records.

</td></tr><tr><td>

Error Framework

 PRB2058704

</td><td>

Allow apps to define key labels for UI Builder components \(configurable fieldLabels/columnList/sort-by\)

</td><td>

Consuming applications should be able to define UI Builder component field labels as domain-specific terms rather than generic ones. For example, if a component has a **Key** or **Source** field, a user should be able to define the field label as 'IP Address' or 'Discovery Schedule' for clarity in their implementation. Additionally, column reordering should be allowed, and so should the action for drop-down list subsections and ordering.

</td><td>

 

</td></tr><tr><td>

Error Framework

 PRB2063337

</td><td>

There's missing overrides for 'Error framework' tables

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Error Framework

 PRB2069719

</td><td>

Separate the 'Error' and 'Context' actions in EF UI Builder \(UIB\) components

</td><td>

The EF UIB error detail panel had a single combined 'Actions' drop-down list for both error-level and context-level actions. This splits them into two distinct split-buttons aligned with the redesign: 'Mark error as ▾' in the properties pane for error actions, and 'Actions ▾' in the agent context pane for context actions. App teams can configure and order actions independently for each section.

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
6.  Select the two WOTs and select **bundle**.
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

 PRB2073167

</td><td>

Add new metric for flow runtime complexity called from non-mcp

</td><td>

The system currently tracks metrics for flow runtime complexity. A new metric should be added specifically for flows called from non-mcp.

</td><td>

1.  Trigger a flow execution via a non-MCP channel \(Browser/UI, Integration channel, Mobile, or any execution path that is not MCP\).

Observe that flow runtime complexity metrics aren't being recorded with the granularity/buckets defined for non-MCP execution.

2.  Compare against expected bucket definitions: Bucket 1 \(1-2\) through Bucket 24 \(1000+\).

 Expected behavior: For all non-MCP execution paths \(Browser/UI, Integration channels, Mobile, and any non-MCP path\), flow runtime complexity metrics are recorded using the new, more granular bucket set, without affecting existing metrics.

 Actual behavior: No dedicated metric/bucket set exists for non-MCP execution paths.

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

 PRB2019712

</td><td>

The See Related Flows action in 'subflow' displays flows with no current reference to a subflow when stale sys\_hub\_sub\_flow\_instance records exist from old snapshots

</td><td>

The See Related Flows action in 'subflow' displays that the subflow is referenced by other flows even though it is not.

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

Flows

 PRB2079258

</td><td>

There's a Flow Diagramming dependency mismatch between oob.properties/bundle.properties and now.dependencies of package.json

</td><td>

In the .properties file in dev/oob-apps, sn\_flow\_diagram:30.0.1 has sn\_diagram\_builder:27.0.0 as a dependency version and is missing some dependencies defined in package.json.

</td><td>

1.  Check the **now.dependencies** field in package.json for version 30.0.1.

Observe that sn\_flow\_diagram:30.0.1 has sn\_diagram\_builder:29.1.0 as a dependency version.

2.  Check the .properties file in dev/oob-apps.

 Observe that sn\_flow\_diagram:30.0.1 has sn\_diagram\_builder:27.0.0 as a dependency version and is missing some dependencies defined in package.json.

</td></tr><tr><td>

GlideAggregate API

 PRB2090884

</td><td>

For non-admin callers, a regression results in the **Aggregate/Stats API** field validation conflating 'field doesn't exist' with 'field exists but read-ACL denies it'

</td><td>

When a non-admin caller queries the Aggregate/Stats API \(/api/now/stats/\{table\}\) using sysparm\_min\_fields, sysparm\_max\_fields, sysparm\_avg\_fields, or sysparm\_sum\_fields, the API incorrectly rejects fields the caller is not allowed to read as if those fields did not exist. Any non-admin identity that has a field-level ACL restriction on one of the fields it requests receives a hard failure instead of the expected ACL behavior. This is a regression related to PRB2081870, which addressed reflected XSS issues.

</td><td>

1.  Pick any table \('T'\) with a field \('F'\) that has a field-level read ACL restricting a non-admin role.
2.  As the non-admin identity, get /api/now/table/T?sysparm\_fields=F,sys\_id&amp;sysparm\_limit=1 and confirm F is absent or blanked in the response.
3.  As the same non-admin identity, call: GET /api/now/stats/T?sysparm\_max\_fields=F.

 Expected behavior: Either a normal aggregate result with F omitted/blank, or a proper ACL-style denial.

 Actual behavior: HTTP 400, 'Invalid sysparm\_max\_fields parameter'. The error is reported identically to what a user would see for a field name that doesn't exist on T at all.

</td></tr><tr><td>

GRC Platform Plugins

 PRB2061497

</td><td>

**Export to PDF** action is cutting off and overlapping text

</td><td>

 

</td><td>

1.  Create a policy
2.  Import a word document with a link.
3.  Publish it.
4.  Open the KB article attached to policy in classic view.
5.  Select **View article**.
6.  Print the article.

 Observe that the Export to PDF action cuts off and overlaps text.

</td></tr><tr><td>

Hermes \(Family\)

 PRB2057996

</td><td>

Setting 'hermes.kafka.disabled' to 'true' does not help to disable Hermes jobs such as 'Hermes Failover State Refresh Job'

</td><td>

This issue causes huge loads of logs.

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

 PRB2071645

</td><td>

Add required RCAs for CBS AINPX in HR Scope

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2081585

</td><td>

There are missing RCA's for the Now Assist AI Data Explorer

</td><td>

RCAs should be generated to cover all possible tables for Query Generation and AI Data Explorer. The covered tables should come directly from what is configured for Query Generation entities. Also, all RCAs should be put into the if / target app scope / update folders as appropriate for each target scope in the application's metadata.

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

Identification and Reconciliation API

 PRB2069627

</td><td>

The Dynamic IRE dashboard should display sampled data instead of the Welcome screen

</td><td>

When sampling is enabled, it collects data. When a user navigates to the Dynamic IRE dashboard, it shouldn't show the Welcome screen. It should show the data that was sampled and calculate the dashboard statistics. Also, when sampling has collected some data, it should indicate that this is sample data, and for further analysis, the user needs to enable simulation.

</td><td>

1.  Navigate to CI Class manager.
2.  Enter 'Hardware'.
3.  Select **Identification Rule**.

 Expected behavior: The Dynamic IRE sampling dashboard is displayed with actual results from CMDB, drawn from the sampling that runs in the background.

 Actual behavior: The Welcome screen is displayed.

</td></tr><tr><td>

Inbound API Integration Usage Framework

 PRB2055912

</td><td>

originatedFromFlow is always false in IntegrationUsage TransactionMonitor, as flow-origin detection is broken for action fabric record-action metering

</td><td>

The originatedFromFlow dimension on action fabric record-action telemetry is never set to true. IntegrationUsage TransactionMonitor decides flow origination once, at transaction start, by checking whether the transaction's usage-tracker context contains a UsageSource.FLOW event. That event doesn't exist yet at transaction start, is removed again before transaction completion, and for asynchronous/scheduled flows the monitor doesn't run at all \(background transactions are not a handled type\). As a result, record actions performed by flows are not attributed as flow-originated, degrading the accuracy of record-action metering.

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

 PRB2023217

</td><td>

Error when adding the trigger table 'Knowledge Feedback Task' due to read access / invalid table error

</td><td>

There is an issue while configuring triggers in AI Agent Studio. When adding a trigger table in an AI Agent, the table 'Knowledge Feedback Task' displays the error: 'You do not have read access to this table. Please select another table.' At times, it also shows: 'Table name is invalid.'

</td><td>

1.  Create a new AI agent.
2.  From the **Add Trigger** option, select the **Knowledge Feedback Task** table as the trigger table.
3.  Open the AI Agent.
4.  From the left-side panel, select the **Add Trigger** option.
5.  Attempt to select the **Knowledge Feedback Task** table as the trigger table.

 Observe the error message.

</td></tr><tr><td>

Knowledge Management

 PRB2063214

</td><td>

Tables in the generated KB article are displayed with bold borders, which differs from the source document formatting

</td><td>

This logic comes from the Word to HTML conversion from the KM API.

</td><td>

1.  Navigate to **Policy and Compliance** &gt; **Compliance Workspace**.
2.  Create a policy record \(or use an existing draft policy\).
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

1.  Navigate to &gt; **Policy and Compliance** &gt; **Compliance Workspace**.
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

 PRB2071699

</td><td>

The knowledge search returns empty results for guests users on the CSP portal

</td><td>

No search results are displayed. However, when the user navigates from Knowledge Base, they can access the article as a guest.

</td><td>

1.  Navigate to the CSP portal as a guest user.
2.  Configure the Knowledge Base for guest users.
3.  Make widgets public.
4.  Navigate to the homepage.
5.  In the search bar, search for some text that's present in an article.

 Observe that no search results are displayed. However, when the user navigates from Knowledge Base, they can access the article as a guest.

</td></tr><tr><td>

Knowledge Management

 PRB2076447

</td><td>

The Auto-fix plugin update blocks the Australia Patch 5m upgrade in loadsim release testing

</td><td>

The plugin upgrade thread handling becomes stuck in an error loop triggered by a null pointer. It never exits or advances, leaving the upgrade 'hung'. This happens when the upgrade plugin loader reaches the knowledge center update that adds in the auto-fix and auto-fix enable property.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2082853

</td><td>

When Word documents are converted to policy text or knowledge articles, hyperlinks appear on a new line instead of remaining on the same line

</td><td>

The dom element of the hyperlink gets nested inside the paragraph for the hyperlink, which continues on the same line correctly. However, the JAVA code points to the closing of a paragraph tag before the hyperlink tag, so it becomes a sibling and not a child. This makes it go to a new line.

</td><td>

1.  Create a document with three links in the same line.
2.  Import the document as a knowledge article.

 Observe that some of the links appear on a new line.

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

 PRB2084781

</td><td>

For markdown, the knowledge blocks addition shouldn't be allowed on the kb\_knowledge.do page

</td><td>

 

</td><td>

1.  Provision an instance with the plugin com.snc.knowledge\_blocks installed.
2.  Make sure the UI16 and workspace changes and the markdown changes are present.
3.  Create a knowledge article kb\_knowledge.do page with 'Knowledge' as Knowledge base.
4.  Check if the **Add blocks** UI action is visible.

 Observe that the UI action isn't visible for wiki articles.

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

Due to Generative AI Controller \(GAIC\) layer issue, multi-KB generation is broken and Mosaic migration should be reverted

</td><td>

 

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

Live Archive

 PRB2033206

</td><td>

There's no visibility into the archive migration process

</td><td>

If the user archives records across the platform, then installs the Live Archive plugin, it's unclear whether the archive data has been completely migrated to columnar storage.

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
2.  Run windows discovery with the following MID configuration: mid.powershell\_api.wmi.fqdn\_method = RDP.

 Observe that the agent logs FQDN lookup falls back to DNS with the error: 'DEBUG \(Worker-Expedited:MultiProbe -e43cdafc3b6ecf 503886e28e53e45aa0\) \[RdpClient:186\] Received NTLM response 30, 0D, A0, 03, 02, 01, 06, A4, 06, 02, 04, C0, 00, 00, BB.' The last four bytes are the error code STATUS\_NOT\_SUPPORTED \(0xc00000bb\).

</td></tr><tr><td>

MID Server

 PRB2090264

</td><td>

PW reset using legacy Orchestration doesn't work

</td><td>

An additional input parameter was added to PSScript.ps1 script file: \[string\]$SNCLogLevel = ''. Calling logic from Disco and iHub are changed accordingly to pass additional parameters to the additional input signature. However, calling codes from Orchestration aren't changed accordingly, so the command to PSScript.ps1 doesn't have the additional input.

</td><td>

1.  Open a Brazil instance.
2.  Run any Workflow Powershell Orchestration activity.
3.  Check the MID Server log.

 Observe the errors.

</td></tr><tr><td>

Mobile Platform

 PRB2068760

</td><td>

SGOfflineSyncAPI .getTempIdsMutexName allows too open of a character set and length

</td><td>

 

</td><td>

Provide tempID's that contain characters that facilitate SQL injection.

 Observe DBUtil.java\# shouldStripForSqlInjection.

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

MMS is not queuing enough records. The system propertyies 'glide.platform\_mm\_service.job.batch\_size' should be set to '10' and 'glide.platform\_mm\_service.async\_http\_max\_outstanding\_requests' should be set to '20'.

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

 PRB2082842

</td><td>

On-demand HTTP responses are correlated by result ID as an attachment token

</td><td>

On-demand \(script-submitted\) multimodal requests never report failures. A submission made through the on-demand path returns successfully and the sys\_mm\_result record is created with status 'pending'. If the Multimodal Service then rejects or fails the request, the record is never updated. There is no status change, no error\_message, no completed\_at, and no callback. The record stays 'pending' indefinitely and the calling script has no way to learn that anything went wrong. This affects every failure mode equally: a transport/connection failure, a permanent 4xx rejection, and a retriable 429/5xx are all dropped silently, with nothing written to the system log either. The 'HTTP 429 Too Many Requests' is expected when the Multimodal Service queue is full. Batch \(attachment-driven\) submissions are unaffected and continue to report failures correctly.

</td><td>

1.  Confirm the asynchronous flow is in use: glide.platform\_mm\_service.use\_sync\_flow = false \(the default\).
2.  Make the Multimodal Service return a failure for a direct/on-demand submission. For example, fill the MMS queue, or lower MMS\_QUEUE\_MAX\_DEPTH, so POST /api/v1/jobs answers '429 Too Many Requests'.
3.  Submit an on-demand request \(MultimodalRequestProcessor.submitOnDemand — a sys\_mm\_result row with direct\_submit = true\).
4.  Inspect the sys\_mm\_result record and the system log.

Notice that the status stays 'pending" indefinitely' and error\_message is empty. Also notice that completed\_at is empty, no callback fires, and nothing is logged.

5.  Repeat with a permanent 4xx \(such as 400\) and with a transport failure to point the service URL at an unreachable host.
6.  Repeat step 2-4 as a BATCH submission \(direct\_submit = false\) in the same instance.

 Notice that the failure is recorded correctly. That contrast isolates the defect to the on-demand path.

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

Multimodal Service \(Family Channel\)

 PRB2086962

</td><td>

MMS prompt verbosity configuration should be enabled for AI Search requests to MMS

</td><td>

Enable MMS prompt verbosity configuration for AI Search requests to MMS.

</td><td>

1.  Enable MMS on the instance.
2.  Attach a document \(with embedded images\) to a record with index\_mms\_attachments enabled.
3.  Trigger indexing.
4.  Inspect the sys\_mm\_result.

Observe that config.verbosity is 'medium'.

5.  Set glide.platform\_mm\_service.verbosity to high.
6.  Re-index the same document.
7.  Inspect sys\_mm\_result.

 Observe that config.verbosity is 'high'.

</td></tr><tr><td>

Next Experience All Menu

 PRB2074680

</td><td>

The Now Assist 'Launch Mode' menu label in Display Preferences is not updated to Otto

</td><td>

 

</td><td>

1.  Navigate to 'Home'.
2.  Select the **User Profile** icon.
3.  Open 'Preferences'.
4.  Navigate to the 'Display' section.

 Observe the 'Now Assist Launch Mode' menu label.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2071263

</td><td>

Menu modules don't resolve Karuna routes

</td><td>

Menu modules that offer a Karuna route alongside their platform link don't resolve the Karuna route.

</td><td>

Open a menu module whose experience is served by a Karuna route.

 Observe that the menu resolves the platform route only. The Karuna route support isn't present.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2078176

</td><td>

The NAP notification count disappears after page refresh and also displays an incorrect count compared to the active conversation count

</td><td>

After refreshing the page, the NAP notification count disappears and doesn't reappear on subsequent refreshes. The issue isn't reproducible in SurfStage, where the counter continues to work correctly even after a page refresh. The count appears again when the same URL is opened in a new browser tab. Also, the NAP notification counter sometimes displays a higher count than the actual number of active conversations, resulting in an inconsistent and incorrect notification count.

</td><td>

1.  Navigate to the NAP notification counter area \(https://surf.service-now.com\).

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

bff\_cookie\_exchange\_allowed is set as 'false', which needs to be 'true', otherwise oauth will fail for the guest user.

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

 Actual behavior: The URL is not sent in the page context payload

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

 PRB2067309

</td><td>

Callback handler error is logged for sync mode capabilities when no callback is configured

</td><td>

In the CallBackHandler .executeCallback\(\) method, the code calls callbackWithScriptable\(\) with an empty string when no callback is configured. The callbackWithScriptable\(\) method logs an error when the callback API name is null/empty and returns null. As a result, syslogs are flooded with error messages for legitimate sync executions, making it difficult to identify real errors in production.

</td><td>

Call any sync capability.

 Observe that the syslogs are flooded with the error: 'No Callback API configured at builder capability level or builder config level'.

</td></tr><tr><td>

OneExtend

 PRB2068736

</td><td>

NAP Summarize Record doesn't work

</td><td>

While running a single-user iteration, summarizing a record via NAP works the first time and creates an entry in sys\_gen\_ai\_text\_cache table. When it hits the same WOT NAP summarize, it should return the data from this cache table, but it doesn't return the summary. Instead, the message appears: 'Sorry, there was a problem on my side trying to complete this request. Try asking again later'.

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

Performance Analytics

 PRB2074730

</td><td>

Remove the KPI Composer \(sn\_kpi\_composer\) base instance app dependency from Glide, build-now, and base instance apps

</td><td>

The build fails during configuration with the following message: 'No such property: kpi for class: org.gradle.accessors.dm. LibrariesForGlideLibs $OobPaLibraryAccessors'.

</td><td>

1.  Delete the oob-pa-kpi-composer alias from build-now/gradle/glide/libs.versions.toml while leaving glide-launcher/build.gradle untouched.
2.  CD glide &amp;&amp; ./gradlew :glide-launcher:help --offline.

 Observe that the build fails during configuration with the following message: 'No such property: kpi for class: org.gradle.accessors.dm. LibrariesForGlideLibs $OobPaLibraryAccessors'.

</td></tr><tr><td>

Performance Analytics

 PRB2090722

</td><td>

Enable the **Sparkle** icon on Data Visualizations for formula indicators

</td><td>

This is a product update.

</td><td>

 

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

 Expected behavior: Only entities with Active=true and population\_source=Table Config show the **Explore** button.

 Actual: The **Explore** button is shown on 'All Table Discovery' entity lists.

</td></tr><tr><td>

Playbook Experience

 PRB2087088

</td><td>

There's a dependency mismatch between oob.properties/bundle.properties and now.dependencies of package.json

</td><td>

Install Engine reads dependencies from package.json. There are zboot DMT failures caused by version mismatches between oob.properties, bundle.properties, and package.json. The app dependencies should match across all three files.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2086543

</td><td>

When resolving overrides for AI-experiences, the first matching overrides containing aixWidget should be returned

</td><td>

PlaybookActivityOverrideRepo .initializeByPlaybook ExperienceId\(\) only populates PlaybookActivityOverride .aixWidget from the override record's **Aix\_widget.id** field. If the override record itself doesn't have an AIX widget configured, but the activity's linked activity UI record does \(activity\_ui.aix\_widget.id\), then the widget is never picked up. The override ends up with an empty/null AIX widget, so the AIX experience isn't rendered even though a widget is configured at the activity UI level.

</td><td>

1.  Create an activity UI.
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

Playbooks

 PRB2078629

</td><td>

There's a dependency content mismatch between oob.properties and packaeg.json

</td><td>

The Install Engine reads dependencies from package.json. The are zBoot DMT failures caused by version mismatches between oob.properties, bundle.properties, and package.json. The app dependencies should match across all three files.

</td><td>

 

</td></tr><tr><td>

Pub/Sub

 PRB2086054

</td><td>

PubSubStatusCache cold-cache query re-enters the Field Normalization/TableRotation lock cycle

</td><td>

PubSubStatusCache.loadEntry\(\) issues a plain GlideRecord.query\(\) against sys\_pubsub\_status with no engine or business rule suppression. PubSubStatusCache.loadEntry\(\)'s query at PubSubStatusCache.java:49 should be hardened with gr.setWorkflow\(false\) and gr.addBeforeQueryRules\(false\). This would mean the cold-cache status lookup can no longer re-enter Field Normalization / the Clotho metrics deny list / the table-rotation chain and contend for a lock this subsystem has no functional need to touch.

</td><td>

 

</td></tr><tr><td>

Pub/Sub

 PRB2094920

</td><td>

ProcessedMessageTracker \(N2N/PubSub dedup map\) grows unbounded and OOMs app nodes

</td><td>

It has been observed that com.glide.pubsub.dedup.ProcessedMessageTracker is growing unbounded, driving app nodes to 'java.lang.OutOfMemoryError: GC overhead limit exceeded'. After heap dump analysis, the map \(fProcessedMessages\) retained 1.94 GB / 47% of the total heap on an affected node. This has caused OOMs on distinct production instances, consistent with slow unbounded growth after upgrade. Three distinct gaps contribute to this: 1\) there is no guard when Samwaad/N2N is not initialized or disabled; 2\) Cleanup is gated by a hardcoded, non-exhaustive node-type allow-list instead of actual role/participation; 3\) there is no upper bound on the map's size.

</td><td>

 

</td></tr><tr><td>

Raptor Analytics Ingestion Core

 PRB2072557

</td><td>

SN connector requires a check on the **Sys\_oid** field of the Datalake

</td><td>

 

</td><td>

1.  Open the sys\_service\_identity\_definition table.
2.  Navigate to the DATALAKE record.
3.  Check the **sys\_oid** field.

 Observe that it's empty.

</td></tr><tr><td>

ReleaseOps - Family

 PRB2067737

</td><td>

ReleaseOps MIF handler bypasses the Instance Scan queue

</td><td>

InstanceScanHandler.java invokes the InstanceScanWorker directly. AScanWorker worker = InstanceScanWorker. generateFromSuites AndUpdateSets \(scanSuiteIds, updateSetIds\), bypassing the instance scan queue management. It should call the CICDInstanceScanExecutionService as an entry point, to take advantage of queuing and possible future changes. In Zurich, the user can only execute one scan at a time. In Australia and onward, multiple scans are allowed using the current code but there are no checks on max number of scans that can be executed and the existing code could potentially overwhelm the instance with too many scans.

</td><td>

1.  Start a full instance scan.
2.  From the ReleaseOps controller, start moving a DR that needs to do an instance scan.

 Expected behavior: The Data Replication waits but then completes successfully.

 Actual behavior: The Data Replication fails the instance scan with an error: 'Failed to get scan result: Multiple scans cannot be run at the same time'.

</td></tr><tr><td>

Request Management

 PRB2070251

</td><td>

RequestWorkflowStageProcessor throws ClassCastException when called from a different scope, causing Requested Item Summarization to show generic content

</td><td>

jsFunction\_ getParentWorkflowChoices throws ClassCastException when handed a fenced object. jsFunction\_ getAllWorkflowChoices silently returns an empty ChoiceList instead of throwing. Stages are either never populated \(crash swallowed upstream\) or silently empty, so the LLM summarization payload has no real stage data. The 'Now Assist request summary' falls back to a generic response.

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

Service Catalog

 PRB2070973

</td><td>

Add Now Assist AI-usage tracking fields and options to the catalog\_builder\_analytics table

</td><td>

Extend the catalog\_builder\_analytics table to support tracking of Now Assist AI usage during catalog building.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB2084606

</td><td>

Family changes to support widgets introduced to the Service Catalog LUX Widgets Store app

</td><td>

This is a product update.

</td><td>

 

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

 PRB2072469

</td><td>

There should be metric/logging for portable vs. non-portable session at login, not just pin-on-detect

</td><td>

There is metric/logging for detecting non-portable sessions. However, that coverage only reports the non\_portable\_sessions counter when a session pin-on-detect event occurs \(session pin trigger from PORTABLE to STICKY affinity, for example via GlideSessionDebug.enable\(...\)\). There should also be metric/logging that reports portable vs. non-portable session state at login time generally, not only when a pin-on-detect event is triggered. Without this, the GIG active session balancing lacks visibility into sessions that are non-portable from login but never go through the pin-on-detect path.

</td><td>

1.  Log in to a Glide node through the normal login flow with no pin-on-detect trigger \(for example, no GlideSessionDebug.enable\(...\) pin from PORTABLE to STICKY\).
2.  Query xmlstats.do?include= otel.session\_node\_transfer on that node.

 Observe that no portable/non-portable counter is incremented or reported for the login event itself. Only pin-on-detect events are captured.

</td></tr><tr><td>

Session Management

 PRB2077746

</td><td>

In GIG, the JSESSIONID-to-node affinity is only learned from request cookies, never from response Set-Cookie. Snc\_session\_affinity\_node is set to 'Secure-only', which breaks stickiness for fresh sessions over plain HTTP

</td><td>

GIG's session affinity for a brand-new session depends entirely on the client echoing GIG's own snc\_session\_affinity\_node cookie. GIG never learns the JSESSIONID-to-node mapping from the response that carries Set-Cookie: JSESSIONID. Additionally, snc\_session\_affinity\_node is always emitted with the secure attribute, and the plain HTTP standard cookie stores it and never sends it back. As a result, it does not echo the affinity cookie, and gets every follow-up request load-balanced, including requests that already carry a valid JSESSIONID.

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2072017

</td><td>

Missing CPU count / CPU core count stamped against cluster VMs with no installs and against retired CIs

</td><td>

Under the Microsoft 'Per Server' license metric, installs are left unlicensed with the reasons 'Missing CPU count' and 'Missing CPU core count'. The actionable entity reported is a configuration item that has no installation of the product being licensed, is retired \(hardware\_status = retired\), and/or has no relationship to the install's installed\_on device, because it's a VM on a different ESX host in the same vCenter cluster. Meanwhile the install's own installed\_on device has complete CPU data. Since any single failing VM sets validHost = false, no install on the host consumes rights, so the product can't be licensed at all. For products that aren't SQL Server, the 'Per Server' rights formula is a constant one and never reads CPU count or core count, so licensing is blocked on data the metric doesn't use.

</td><td>

1.  Build a vCenter cluster with two or more ESX hosts, each with VMs with the following relationships:
    1.  VM 'Virtualized by::Virtualizes' ESX host \(parent = VM, child = host\)
    2.  Cluster 'Contains::Contained by' host \(parent = cluster, child = host\)
2.  On host B, leave at least one VM with cpu\_count and cpu\_core\_count empty.
3.  Give that VM no installs of the product.
4.  Set it to retired \(hardware\_status = retired\).
5.  Install a NON-SQL Server Microsoft product on a VM on host A.
6.  Ensure that the VM has valid cpu\_count and cpu\_core\_count.
7.  Create an entitlement for the product with license metric 'Per Server' \(00bec99293032200f2 ef14f1b47ffb78\).
8.  Run Microsoft reconciliation.
9.  Navigate to **SAM Workspace** &gt; **License Usage** &gt; **Product** &gt; **Installs requiring action**.

 Expected behavior: The retired / install-less VM on host B isn't evaluated by the CPU validation, and the installs on host A's VM consume 'Per Server' rights.

 Actual behavior: The installs on host A's VM are unlicensed with reasons 'Missing CPU count' and 'Missing CPU core count'. The actionable entity on those reason records is the retired, install-less VM on host B. Nothing on the host is licensed. The actionable entity has no direct relationship to the install's installed\_on CI.

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

Stream Connect Core

 PRB2001155

</td><td>

When Kafka generates many errors, processing those errors can produce Mutex contention

</td><td>

Stream Connect producers stop sending to Hermes Kafka. It publishes block for around 60 seconds and then fails, so the worker/scheduler threads back up, business rules run slow, and APIs become slow. Failed messages accumulate in the sys\_kafka\_ undelivered\_messages table, and the base instance Kafka Producer Retry Job gets stuck and can't drain them.

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB2079908

</td><td>

After upgrading from Zurich to Australia, the active Kafka Subscriptions are updated to REFRESHING status

</td><td>

Topic alias records are created for the Hermes topics after the upgrade. However, for a few of the Kafka Subscriptions \(in the sys\_kafka\_subscription table\), the topic alias column shows empty and the status is 'REFRESHING'.

</td><td>

 

</td></tr><tr><td>

Stream Connect Core

 PRB2088720

</td><td>

The base instance apps version should be updated from 6.0.6 to 6.0.7

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Syntax Editor

 PRB2080150

</td><td>

'Find References' dialog info tooltip icon fails aria-prohibited-attr \(there's no ARIA role for aria-label/title\)

</td><td>

This is an accessibility violation. It's found in glide/plugins/ com.glide.syntax\_editor /ui.html/scripts/ classes/syntax\_editor5 /references/ GlideEditorFindReferences.js:483, in the getModalBody\(\) function's info-message-wrapper markup.

</td><td>

1.  Open a scriptable record \(for example, a Script Include\) in the Now Code Editor / classic UI's Monaco-based code editor.
2.  Select a symbol \(for example, a function or variable name\) in the editor.
3.  Invoke 'Find References' by selecting and holding \(or right-clicking\) the context menu \(or using the Find References action in syntax\_editor\).
4.  In the Find References modal that opens, locate the **Info** icon next to the results-count header.
5.  Run an accessibility scan \(axe-core\) against the open modal, or inspect the icon element's DOM directly.

 Expected behavior: The icon carries an ARIA role \(e.g. role='img'\) so its aria-label is valid and a screen reader announces the tooltip text. Axe should report no aria-prohibited-attr violation on this node.

 Actual behavior: The p-tag has aria-label and title but no role, so axe flags aria-prohibited-attr and screen reader users get no reliable accessible name for the icon.

</td></tr><tr><td>

System Archiving

 PRB1974369

</td><td>

Compaction is not working for archived tables in the columnar format

</td><td>

An error occurs after migrating the columnar format, updating the compaction properties, and running the background script.

</td><td>

1.  Migrate ar\_ table to columnar format.
2.  Update the compaction properties.
3.  Run the background script, 'new GlideTableCompactor\(\) .compact\('tableName'\);'

 Notice that there is an error, 'Table didn't compact as... Sys\_id not indexed on root storage table.'

</td></tr><tr><td>

System Archiving

 PRB2056839

</td><td>

Compaction should not be attempted for columnar tables

</td><td>

 

</td><td>

1.  Migrate ar\_ table to columnar format.
2.  Update compaction properties.
3.  Run the background script.

 Expected behavior: Compaction should be blocked because this is a columnar table.

 Actual behavior: The error occurs, 'Error: Table didn't compact as... Sys\_id not indexed on root storage table.'

</td></tr><tr><td>

System Events

 PRB2080453

</td><td>

NowMQ events never get delegated on Worker.Default nodes due to a broken participation check

</td><td>

 

</td><td>

 

</td></tr><tr><td>

System Events

 PRB2089685

</td><td>

Flow events created with a future TimeStamp are picked up and become stuck in the in-memory queue for processing

</td><td>

This issue causes the in-memory queue to be full, and does not allow other events to be processed.

</td><td>

Create a future event with a targeted node with 'p0'.

 Observe that the event is picked up by the in-memory queue without checking for the **process\_on** field, resulting in the event being picked up and shown in the sys\_nowmq\_node\_stats table. All low priority events are not picked up as high priority events \(p0\), and none of the events are processed.

</td></tr><tr><td>

System Scheduler

 PRB2076443

</td><td>

Issues with the rename dedicated node bypass property and skip reconcile job on non-dedicated node instances

</td><td>

The property 'com.snc.cluster.scheduler.dedicated\_node\_bypass' uses the 'bypass' terminology, which is inconsistent with the intent. The property controls whether child jobs are allowed on dedicated nodes, not a bypass of anything. There is also an unnecessary reconcile job execution, in which the job runs the full configuration seeding and orphan cleanup with no meaningful effect. In this scenario, sys\_scheduler\_dedicated\_job\_config creates and maintains rows on an instance that has no dedicated nodes, and will never enforce dedicated node protection.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2037370

</td><td>

Reading of multiple records using the UI/API Call/Processor/Script/Flow fails to track multiple READs in the Record Action metric

</td><td>

Four GlideRecord operation methods are instrumented to call RecordActionRecorder.record\(\) at the point of each operation. This is the entry point for all telemetry, and every record operation on an allowlisted table flows through here. The instrumentation pattern follows GlideRecordProtected DataRecorder, which already instruments the same methods: a single static call, no branching, no impact on the existing operation path. query\(\) is added for READ instrumentation so that data access by external agents and the NOW UI can be measured alongside writes.

</td><td>

1.  Navigate to the incident table.
2.  View the list of incidents in the ServiceNow UI.

Observe that all of the rows are visible in the UI with multiple read metrics.

3.  Execute a Query Service Query to validate that multiple metrics have been recorded in the 'sn.glide.action\_ fabric.record\_action' metric.

 Expected behavior: Multiple reads are recorded.

 Actual behavior: One read is recorded.

</td></tr><tr><td>

System Web Services

 PRB2088200

</td><td>

True-up Telemetry Data Connector

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Web Services

 PRB2088207

</td><td>

True-up the Action Fabric Usage Dashboard app

</td><td>

 

</td><td>

 

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

 Expected behavior: Form fields are visible for timesheet entry.

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

 PRB2074188

</td><td>

GIG gateway thread pool and polling scheduler aren't shut down when Glide shuts down, leaving non-daemon threads running

</td><td>

The JVM doesn't exit cleanly. Non-daemon threads from the gateway fixed thread pool remain alive because Glide.destroy\(\) never calls into JettyClientManager to tear down GIG resources.

</td><td>

1.  Enable GIG \(glide.gig.enable=true\) with valid glide.gig.client.endpoints so the gateway connection and gateway fixed thread pool become active.
2.  Shut down the Glide servlet \(Tomcat stop / graceful JVM shutdown\).

 Observe that the JVM doesn't exit cleanly. Non-daemon threads from the gateway fixed thread pool remain alive because Glide.destroy\(\) never calls into JettyClientManager to tear down GIG resources.

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

 Note the duplicated list UI actions such as **Repair SLAs,** **Add to Visual Task Board**, and so on.

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

UI Form Administration

 PRB2080805

</td><td>

The form for the sn\_customerservice\_task table is unresponsive when Polaris is turned off

</td><td>

The activity stream doesn't work, the context menu in the header doesn't open, and fields can't be edited.

</td><td>

1.  Provision an instance with the 'com.sn\_customerservice' plugin installed.
2.  Navigate to the sn\_customerservice\_task table.
3.  Create a record.
4.  Set the 'glide.ui.polaris.experience' property to false to turn off Polaris.
5.  Refresh the case task record.

 Expected behavior: The form is responsive.

 Actual behavior: The form is not responsive.

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

 PRB2014549

</td><td>

getScreen is invoked twice, causing duplicate calls to the server

</td><td>

 

</td><td>

1.  Open any instance on Australia or Brazil.
2.  Open SOW workspace.
3.  Perform a hard reload.
4.  Open 'DevTools - Network Tab'.
5.  Select the **ServiceNow Logo** present on the unified navigation bar on the top left.

Observe that the user is routed to /now/nav/ui/home.


 Expected behavior: Only one hydrate call is made.

 Actual behavior: Two hydrate calls are made.

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

 PRB2069094

</td><td>

Users are unable to select menu API calls on a SURF clone instance

</td><td>

The landing page is missing from the menu list. The request isn't being called on any page navigations to this: /api/now/ui/polaris/menu.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2083327

</td><td>

The UI Builder authorization iframe modal buttons are non-functional

</td><td>

The **Cancel** and **Approve** buttons don't work on the iframe. Also, there is an Otto ServiceNow pop-up that comes up initially on the iframe.

</td><td>

1.  Navigate to 'Request Clone' under the Clone Admin Console.
2.  Select **Target instance** or **Add new instance**.
3.  Configure P/E as needed.
4.  Select **Continue**.
5.  On the clone summary page, select the **Submit Clone Request** button.

 Observe that an iframe modal opens for 'Authorization Requirement'. The **Cancel** and **Approve** buttons don't work on the iframe. Also, there is an Otto ServiceNow pop-up that comes up initially on the iframe.

</td></tr><tr><td>

UX Framework

 PRB2084577

</td><td>

Product lab and action triggers in Survey Center

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2033259

</td><td>

Language detection doesn't work properly with Agentic mode for both the standard and enhanced chat

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2063992

</td><td>

The user is unable to add a portal to the Conversational AI Assistant

</td><td>

When the user attempts to add the ESC portal to domain one, it is successful. However, when the user attempts to set up the assistant to domain two with Service Portal, it fails and the portal is not set. Errors don't occur in the UI, but when it goes to the next step 'Branding', it fails saying the portal is not set. Errors occur in the logs.

</td><td>

 

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

 Notice that it is throwing an error.

</td></tr><tr><td>

Virtual Agent

 PRB2069447

</td><td>

Semantic filtering Virtual Agent global flags aren't set when invoked from AO via topic tool execution

</td><td>

 

</td><td>

1.  Start a NextWave conversation.
2.  Trigger sensitive detection for HR fallback.
3.  Select Create case.
4.  When prompted for a description on the case, provide the same utterance that triggers semantic detection.

 Expected behavior: It proceeds and creates a case.

 Actual behavior: The user utterance is flagged for semantic filtering.

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

 PRB2070048

</td><td>

There's an OGCS error on skillPicker due to bad sys\_gen\_ai\_skill data

</td><td>

 

</td><td>

1.  Add a sys\_gen\_ai\_skill record which doesn't have a valid skill\_document ID.
2.  Attempt to run a valid topic.

 Expected behavior: A topic should execute and log warning message that there's an invalid sys\_gen\_ai\_skill record.

 Actual behavior: A topic won't execute.

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

 PRB2073250

</td><td>

A conversation from another domain doesn't work if the user default domain doesn't have access to the current session domain

</td><td>

Whenever there is a hybrid queue into play, the worker impersonates the user and updates the session, but doesn't touch the domain. When impersonated normally, the domain will be the default domain for the user. This might no have access to the conversation because its started in a different domain. So whenever we read some data that is not accessible like conversation, the flow fails.

</td><td>

1.  Enable domain separation.
2.  Update any field on a user record.

Once updated, the default domain to the user moves to TOP/Default unless specified.

3.  Switch the domain to a different domain \(some sibling domain or a parent domain\).
4.  Start the conversation.

 Observe the responses would not be received for any query.

</td></tr><tr><td>

Virtual Agent

 PRB2073833

</td><td>

The AiAgentSecurityHelper lacks an API to create compound deny\_unless security-attribute ACLs, blocking sn\_voice\_aia from securing voice agent endpoints

</td><td>

There must be a gate for sn\_voice\_aia for certain voice agent endpoints behind a compound ACL using a custom security attribute with a deny\_unless decision policy. A compound ACL with deny\_unless requires setting 'decision\_type', 'local\_or\_existing', and 'security\_attribute' on sys\_security\_acl. Scoped apps can't do this directly, and a global helper is required.

</td><td>

1.  On an instance with com.sn.voice\_aia and com.glide.cs.genai installed, attempt to configure a voice AI agent endpoint that requires compound ACL security, specifically an ACL using a custom security attribute with a deny\_unless decision policy.
2.  From the sn\_voice\_aia scope, call new AiAgentSecurityHelper\(\). createAclWithSecurity Attribute\(...\) to delegate compound ACL creation to the global helper.

 Expected behavior: sn\_voice\_aia should be able to delegate compound ACL creation to the global AiAgentSecurityHelper utility, the same as it does today for role-based ACLs via createAclAndRoles.

 Actual behavior: The method does not exist on AiAgentSecurityHelper. sn\_voice\_aia can't create sys\_security\_acl records with compound security attributes directly from a scoped context.

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

A java.lang.NullPointerException occurs, 'Cannot invoke 'com.glide.script. GlideRecord.setValue\(String, Object\)' because 'gr' is null'

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

 PRB2078011

</td><td>

The Virtual Agent greeting is not showing, or shows the wrong message, when the system language is non-English

</td><td>

The session saved in English is shown instead of saving and showing the greeting message created in the Japanese session.

</td><td>

1.  Set glide.sys.language to 'ja'.
2.  Open VA assistant.
3.  Update the message to something that is not base instance.
4.  In the English session, test the assistant.

Notice that no message is shown.

5.  Switch to a Japanese session and save any greeting message.
6.  In the Japanese session, test the assistant.

 Observe that the message that was saved in the English session is shown.

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

 PRB2084118

</td><td>

setCache is not honoring domain field

</td><td>

setCache is not honoring the domain field when impersonating the actual user.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2085286

</td><td>

Selecting to execute topics isn't working

</td><td>

When the user tries to select the links, either nothing happens or there's an 'Error in' processing message.

</td><td>

1.  Navigate to the Virtual Agent.
2.  Ask 'What are my summarize options?'.
3.  Try to select any of the links.

 Observe that either nothing happens or there's an 'Error in' processing message.

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

 PRB2086482

</td><td>

Off Glide branding API returns the menu item with the type as null

</td><td>

The API returns the 'Contact Live Agent' item with the type as 'null', even though the actual type is 'chat'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2087473

</td><td>

Bring the tone/persona sys-prop at the assistant level and append the agent\_persona instruction to it

</td><td>

If the config attribute isn't 'agent persona', the system appends the agent persona to the prompt if it exists. If the attribute is 'agent persona', it uses the persona or a static fallback if empty.

</td><td>

1.  Bring the sys-prop 'sn\_nowassist\_va .assistant\_personalization' to the Now Assist deployment config table.
2.  Make the setting available at the assistant level.
3.  Append the **Agent\_persona** field in the Now Assist deployment config table to tone/persona prompt.

 Observe that, when the config attribute isn't 'agent persona', the system appends the agent persona to the prompt if it exists. If the attribute is 'agent persona', it uses the persona or a static fallback if empty.

</td></tr><tr><td>

Virtual Agent

 PRB2091490

</td><td>

Glide to OGCS requests should set X-Instance-Url header with canonical URL

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2092748

</td><td>

Live agent availability doesn't work once the user selects the **Cancel** button

</td><td>

It shows that no agents are available, even after the user selects the **Cancel** button and the live agent availability should resume.

</td><td>

1.  Start a chat as requestor from the /esc portal.
2.  Have an agent online from another browser.
3.  Connect to a live agent.
4.  Select the **Cancel** button and do not accept the workitem.
5.  Try connecting to the agent again.

 Expected behavior: The live agent transfer should stop just for that interaction when **Cancel** is selected and the live agent availability should start resuming after.

 Actual behavior: Notice that even when the agent is available, it shows that no agents are available. This happens for all the new conversations.

</td></tr><tr><td>

Virtual Agent

 PRB2095603

</td><td>

getChannelById method mapping missing in glide-plugin-members.xml

</td><td>

getChannelById calls from NW channels are failing.

</td><td>

 

</td></tr><tr><td>

Window Manager

 PRB2078184

</td><td>

The classification and protections canvas doesn't work in Securing Custom Apps with Vault Agents Otto

</td><td>

 

</td><td>

1.  Open 'Securing Custom Apps' with the Vault Agents Otto application.
2.  Navigate to the 'Classification and protections for your app' canvas.

 Observe that the canvas doesn't load or function as expected.

</td></tr><tr><td>

Window Manager

 PRB2090196

</td><td>

The closed window still consumes mouse clicks after unpinning Otto, which blocks the Polaris contextual menu pin

</td><td>

After opening and closing \(specifically pinning/unpinning\) Otto, its window element remains mounted in the DOM at full size and intercepts clicks over whatever page content is underneath it. Its DOM element remains at full size with pointer-events overridden by inner content, instead of collapsing to a 0-size box like the legacy window manager does. This prevents the user from pinning other contextual menus via Polaris in that region of the screen.

</td><td>

1.  Open a Brazil instance.
2.  Open Otto \(Now Assist chat\).
3.  Pin Otto by docking it via a contextual menu/Polaris pin action.
4.  Unpin Otto so that it closes.
5.  With Otto now closed, try to click on/pin a different contextual menu in the area of the screen where Otto's \(now invisible\) window used to be.

 Observe that the click is swallowed, and pinning other contextual menus is not possible because the closed Otto window is still consuming mouse clicks.

</td></tr><tr><td>

Work Order Management

 PRB2083257

</td><td>

Plan\_maint\_admin and plan\_work\_admin users aren't able to view work order templates

</td><td>

Since the roles already contain cmdb\_read role, the user should be able to view the records. However, when the user opens the work order template, no fields are visible.

</td><td>

1.  Log in as a user who has the plan\_maint\_admin role or plan\_work\_admin role.
2.  Select the **Preview** icon on any work order template from the list.

Observe that all the fields are visible.

3.  Open the work order template.

 Observe that no fields are visible when the template is opened in jelly page.

</td></tr><tr><td>

Zing Text Indexing and Search Engine

 PRB2083455

</td><td>

Allowlisting should be allowed for the kb\_knowledge table for text\_search v4 format

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Brazil security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/brazil-security-notables.md)
-   [All other Brazil fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/brazil-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/available-versions.md)


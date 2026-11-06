---
title: Australia Patch 8
description: The Australia Patch 8 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/australia-patch-8.html
release: australia
topic_type: reference
last_updated: "2026-11-05"
reading_time_minutes: 61
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia Patch 8

The Australia Patch 8 release contains important problem fixes.

-   **Australia Patch 8 was released on November 05, 2026.**
    -   Build date: 11-03-2026\_1626
    -   Build tag: glide-australia-02-11-2026\_\_patch8-10-22-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A08.00.xlsx).

## Overview

Australia Patch 8 includes 456 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-ap8.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Australia Patch 8 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia Patch 8, refer to [KB3229040](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3229040).

## Changes in Australia Patch 8

-   **[Provide users with powerful and flexible search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/explore-features-search-ais.md)**

    Administrators can configure display of auto-complete suggestions as standard HTML anchors that can be opened in new browser tabs using the browser's native right-click/long-press functionality.

-   **[Display relevant and actionable search results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/explore-features-results-ais.md)**

    Administrators can configure display of search results as standard HTML anchors that can be opened in new browser tabs using the browser's native right-click/long-press functionality.

-   **[Auto-complete suggestions in AI Search applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/auto-complete-ais.md)**

    When AI Search displays search suggestions for your search, it defaults to rendering suggestions as links that trigger navigation scripts when you select them. These links aren't standard HTML anchor elements, so you can't open a search suggestion in a new browser tab by right-clicking or long-pressing its link.

    Administrators can override this default behavior and configure AI Search to display search suggestions as standard HTML `a` \(anchor\) elements with `href` \(hypertext reference\) attributes. After making this change, you can right-click or long-press a search suggestion to open it in a new tab in your web browser.

-   **[Display search suggestion links as standard HTML anchors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/display-search-suggestion-links-standard.md-anchors.md)**

    Increase search flexibility by configuring AI Search to display search suggestion links as standard HTML anchors. You can open these search suggestion links in new browser tabs using your browser's right-click or long-press functionality.

-   **[Display search result links as standard HTML anchors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/display-search-result-links-standard.md-anchors.md)**

    Increase search flexibility by configuring AI Search to display search result links as standard HTML anchors. You can open these search result links in new browser tabs using your browser's right-click or long-press functionality.


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

Configuration Management Database \(CMDB\)

 PRB2095766

 [KB3227580](https://hi.service-now.com/kb_view.do?sysparm_article=KB3227580)

</td><td>

KittyScopedEvaluator rejects the CMDB Search tokenized utterance, breaking the CI name search in the global search

</td><td>

An error occurs in the logs after attempting to search for a CI name in the Global Search box.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Document Viewer

 PRB2091075

 [KB3227242](https://hi.service-now.com/kb_view.do?sysparm_article=KB3227242)

</td><td>

External users aren't able to access the new Next Experience document viewer from the Core UI

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Instance Scan

 PRB2007287

</td><td>

DB dump captures the contaminated sys\_status row \(glide.instancescan.queue .status='upgrade paused'\) when the server shutdown races with the active ScanQJob

</td><td>

DB dumps produced by the automated build process may contain a contaminated sys\_status entry \(glide.instancescan .queue.status = 'upgrade paused'\) if the dump server shutdown happens to coincide with an active instance scan queue job. Instances loaded from such dumps have their instance scan queue permanently paused with no automatic recovery — the queue won't process any items until the sys\_status row is manually cleared or a resume is triggered.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2059156

</td><td>

A new MID default user is created and produces a 'No login attempts within reporting period' message consistently

</td><td>

This problem is focused on the alert 'User mid\_server\_default with mid\_server role not associated with a MID Server. No login attempts within reporting period' that consistently displays.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB2060459

</td><td>

PA widget transactions become stuck and run for days

</td><td>

PA widget transactions become stuck causing semaphores to be held up. It is observed that the widgets are different in all cases.

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB2091274

</td><td>

Catalog Builder is missing the 'UI policy' section for users with the catalog\_builder\_editor role

</td><td>

Users with the catalog\_builder\_editor role but not the catalog\_admin role are unable to view 'UI policy' and 'Client Script' sections in Catalog Builder.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1878374

</td><td>

In Teams, conversations are stuck and run into errors after switching between instances

</td><td>

 

</td><td>

1.  Connect the Prod bot to an instance.
2.  Run a few conversations on Teams.
3.  Switch to another instance.
4.  Try running a few conversations.

 Expected behavior: The user is able to run conversations on Teams.

 Actual behavior: The user conversations are stuck and run into errors sometimes.

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

Access Control

 PRB2071424

</td><td>

Delegated developers are blocked from creating/updating records on sysevent\_email\_action due to new ACLs from the 'Notifications Email Agents' plugin

</td><td>

After upgrading the Now Assist suite, new ACLs added by the 'Notifications Email Agents' plugin prevent delegated developers from creating or updating records in the sysevent\_email\_action table within scoped applications. The ACLs require the sn\_notif\_agents .notification\_generator role, which is intended for AI notification agents, not delegated developers. Now Assist features shouldn't impact unrelated platform functionality.

</td><td>

1.  In a development instance, impersonate 'FinanceApp Admin'.
2.  Switch to 'Finance Core' application scope.
3.  Navigate to the sysevent\_email\_action table.

Observe that the **New** button is missing so the user can't create records.

4.  Open an existing record in 'Finance Core' scope.
5.  Attempt to edit the record.

Observe that editing is blocked.

6.  In a sandbox instance without the 'Notifications Email Agents' plugin, repeat the steps.

 Observe that the **New** button is available and records can be edited.

</td></tr><tr><td>

Activity Stream Compose Component

 PRB2032875

</td><td>

Highly threaded emails with multiple block quotes render as unreadable in the 'Conversation' tab

</td><td>

.

</td><td>

1.  Navigate to any workspace, such as Service Operations Workspace.
2.  Open any record from the list.
3.  Reply to that email from inbox.

This reply should appear in the 'Conversation' section.

4.  Reply back to this new email.
5.  Repeat for seven to eight replies.

 Observe that it reaches a point where users see one letter per row.

</td></tr><tr><td>

Activity Stream

 PRB2080954

</td><td>

The statement 'on behalf of AI' incorrectly displays 'AI' and not the user

</td><td>

This was introduced when Audit &amp; Logging changed the attribution model for AI-generated changes. The AuditGroup **Who** field was changed to reflect the identity of the AI agent making a change when generating history sets.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB2085418

</td><td>

The **CRR** icon isn't displayed for non-English languages

</td><td>

 

</td><td>

1.  Log in to an instance as an agent in Japanese.
2.  In another browser, navigate to esc.
3.  Initiate a chat with a live agent.
4.  As the agent, accept the work item.
5.  Type a few words \(less than five\) in Japanese.

 Expected behavior: The **CRR** icon should be displayed as for Japanese there's no constraint for words having spaces in between them.

 Actual behavior: The **CRR** icon isn't displayed as spaces aren't present and the word count is calculated to be less than five.

</td></tr><tr><td>

AI Experience Framework - Glide

 PRB2121332

</td><td>

Update the Karuna-glide managed app version in base instance apps

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2095865

</td><td>

AIS deleteSingleRecord's unconditional attachment deleteByQuery blocks the event processor, causing queue backlog and auto-shutoff

</td><td>

AIS indexing was auto-paused because the update event queue backlog grew past 1M due to IngestService.deleteSingleRecord stalling the AIS event processor. During this pause window, updated cases and records were not searchable until the backlog drained and indexing resumed.

</td><td>

1.  Open an instance with AIS/glide-ais.
2.  Configure a datasource/table pair where AIS responds slowly to deleteByQuery \(for example, a very large index or 100M+ docs\) or is intermittently unavailable.

Observe that it triggers the exponential-backoff retry path.

3.  Trigger a sustained burst of record deletes on that table via a retention/cleanup policy's bulk delete—or a scripted bulk delete through the normal GlideRecord delete path—so business rules/listeners fire normally.

 Observe that each deleted record produces one AIS delete event. The AIS event processor calls IngestService.deleteSingleRecord once per event, which unconditionally calls deleteAttachmentDocumentsByQuery to InternalContentIngestionApi .deleteByQuery. This runs synchronously and blocks the event-processing thread on the AIS network call \(and on retry backoff sleeps\)—even when the deleted records have no attachments at all. If AIS is slow/unavailable long enough, the queueShouldNotBeWritable\(\) safeguard disables the update event queue \(glide.ais.update\_event \_queue\_writable=false\). Any record changes during the paused window aren't reflected in Global Search until the queue is manually re-enabled and the backlog drains.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2096049

 [KB3226033](https://hi.service-now.com/kb_view.do?sysparm_article=KB3226033)

</td><td>

An upgrade causes the instance to log a missing column error during the upgrade due to a missing 'active' column in the ts\_configuration table

</td><td>

It seems this column is being added by the upgrade itself but it's not clear why the nodes expect it before it's being added. An instance can become unavailable in the upgrade process. An emergency schema correction was implemented by adding the missing 'active' column to the ts\_configuration table. Once the schema was corrected, the upgrade process resumed and completed successfully.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Analytics Data API

 PRB2085507

</td><td>

The FilterParser class and getFieldsFromFilter method aren't exposed

</td><td>

FilterParser class and getFieldsFromFilter should be callable from GlideScript scope. FilterParser \(repo: glide/glide\) should be exposed as a Glide Scriptable. Report conditions aren't taken into account on the scan when scanning if a report passes RVACLs.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB2084237

</td><td>

Support install engine to read the SNAPSHOT version from package.json for the app store path

</td><td>

The installation fails with the following error because the install engine is not able to resolve SNAPSHOT version from store: '\*\*\* ERROR \*\*\* Unable to find the dependency plugin sn\_ai\_csm\_fdn: 2.1.3-SNAPSHOT for sn\_ai\_csm\_advanced \*\*\* WARNING \*\*\* Unable to resolve dependency sn\_ai\_csm\_fdn: 2.1.3-SNAPSHOT for sn\_ai\_csm\_advanced as dependency is unavailable'.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB2084238

</td><td>

Download of sn\_sam\_saas\_int takes five minutes per plugin when it's not able to find the version in the store

</td><td>

 

</td><td>

1.  Provision an Australia instance with sn\_sam\_saas\_int installed and a version that is withdrawn / non-existent in the app store.
2.  Restart a node.

 Observe that the download of sn\_sam\_saas\_int takes five minutes per plugin.

</td></tr><tr><td>

Application Rationalization

 PRB2082114

</td><td>

ArtifactRelated EntityTableChoices Script Include needs client\_callable=true for tableChoicesScript to work in Enterprise Architecture \(EA\) Workspace

</td><td>

The 'Entity' drop-down list shows all tables instead of the filtered list.

</td><td>

1.  Open the EA Workspace.
2.  Navigate to **Portfolio** &gt; **Architectural Artifacts**.
3.  Open any existing artifact or create a URL type artifact.
4.  Open the 'Related Entities' related list.
5.  Select **New**.
6.  Select the **Entity** drop-down list.

Observe that all tables are shown \(25+ tables\) instead of the filtered list.


 Expected behavior: Only 6 tables should be shown \(Business Application, Business Capability, Business Process, Digital Integration, Digital Interface, TRM Product\).

 Actual behavior: All tables are shown.

</td></tr><tr><td>

Attachments

 PRB2103278

</td><td>

Fix uploader visibility and expose avatar, upload timestamp, and access fields via GraphQL

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Authentication Factors

 PRB2074637

</td><td>

The Glide Authentication API does not support the status-check endpoint for push factor verification

</td><td>

 

</td><td>

1.  Initiate authentication with push factor.
2.  Poll for the status by calling/authenticating with factorType=push, value=null.

 Observe that each poll triggers a new push notification to the user's device.

</td></tr><tr><td>

Authentication Factors

 PRB2091106

</td><td>

Unlocked caller who enters another incorrect answer doesn't get the expected further attempt

</td><td>

The user is transferred to a live agent before schedule job execution. The attempt record still shows the old, pre-expiry count instead of resetting.

</td><td>

1.  Enter an incorrect answer repeatedly until the max retry limit is reached and the caller is locked out.
2.  Wait for the configured lockout window to fully elapse.
3.  Call in again.

Observe that the user is correctly prompted for the PIN \(the lockout has expired correctly\).

4.  Enter an incorrect answer again before the table cleaner scheduled job runs.

 Expected behavior: The user gets a further attempt \(retry or secondary factor\), same as a first-time failure.

 Actual behavior: The user is transferred to a live agent before schedule job execution. The attempt record still shows the old, pre-expiry count instead of resetting.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB2069592

</td><td>

RCAs are missing in the NAE flow for HR core

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB2079977

</td><td>

Dynamic CI Groups fail to populate Affected CI records due to an issue in the Australia Dynamic CI Group unpack processing path

</td><td>

Dynamic CI Groups aren't being unpacked into the expected Affected CI records during Change Request processing. The unpack process completes, however, the resulting Affected CI records aren't created as expected due to an issue in the Australia processing path. Affected CI records aren't generated from Dynamic CI Groups, preventing downstream Change Management functionality that relies on Affected CI population from functioning as expected. This impacts processes that depend on Dynamic CI Group members being automatically added during Change Request processing.

</td><td>

1.  Create or open a Change Request.
2.  Add a Dynamic CI Group as the Configuration Item or Affected CI.
3.  Save or submit the Change Request.
4.  Allow the Dynamic CI Group unpack process to execute.

Observe that the Dynamic CI Group processing completes successfully.

5.  Review the Affected CI related list.

 Expected behavior: All applicable CI members associated with the Dynamic CI Group are unpacked and populated into the Affected CI related list.

 Actual behavior: Affected CI records associated with the Dynamic CI Group aren't populated.

</td></tr><tr><td>

Change Management

 PRB2093236

</td><td>

DF Advisor auto-activation causes regressive behavior for Inc, Chg, Prb and Req

</td><td>

The 'com.snc.task. principal\_class\_filter' property should be empty or it should contain the same value as it did prior to upgrading.

</td><td>

1.  Open an instance.
2.  Navigate to sys\_properties.do?sys\_id= 1f2f01ce878010100e3dd61e36cb0b63 \(com.snc.task. principal\_class\_filter\).

 Observe the property. On a zbooted instance, or an upgraded instance with 0 principal CI classes set up prior to upgrading, the property must be empty. On an upgraded instance with at least 1 principal CI class set up prior to upgrading, the property should contain the same value as it did prior to upgrading. The expectation is that this is the IPCR tables.

</td></tr><tr><td>

Client Scripts

 PRB2098096

</td><td>

UI16's g\_modal.showWidget's aiux-kit's aiux-core-loader doesn't support minified now-sdk generated widget files

</td><td>

g\_modal.showWidget is to be removed from the UI16 scripting environment entirely.

</td><td>

1.  Use now-sdk to generate a widget \(which minifies it by default\).
2.  Use g\_modal.showWidget in UI16 to attempt to render it.

 Observe that it fails.

</td></tr><tr><td>

Client Scripts

 PRB2107411

</td><td>

Migrate ShowConfirmUpdateDialog

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB2107412

</td><td>

Migrate 'Remove user access from table'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB2107413

</td><td>

Migrate 'resize\_user\_photo\_ie'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Cloud Encryption

 PRB2065769

</td><td>

ES12 should be disabled for EKMSApi

</td><td>

The clone/restore workflow preflight fails intermittently across DCTest, DCDev, and DCProd. The datacenter automation runs checkEKMSStats through run-node-script, and the script fails with EKMSApi is not defined. As a result, clone/restore is blocked or has to be retried whenever the failure occurs.

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2086544

</td><td>

Reading an encrypted field results in an error when IRE is invoked through scoped API from application scope

</td><td>

 

</td><td>

1.  Use field encryption and encrypt an identifier.
2.  Run an IRE payload using the scoped IRE API from the application scope.

 Observe the error.

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB2088316

</td><td>

Dynamic IRE tie breaker doesn't work as expected/designed

</td><td>

Dynamic IRE matches the unclassed hardware on name, but it matches the computer on lookup only \(serial\_number on the CI conflicts\). Each has score 1, but serial number lookup has a lower order filter condition and should break the tie in favor of the cmdb\_ci\_computer. However, unclassed hardware becomes the match instead.

</td><td>

1.  Create cmdb\_ci\_computer with name=test, serial\_number=123, lookup serial number=12345, and type=system.
2.  Create cmdb\_ci\_unclassed\_hardware with name=test.
3.  Run the payload for cmdb\_ci\_computer with \{name=test, serial\_number=12345\}, with lookup 12345/system.

 Observe that dynamic IRE matches the unclassed hardware on name, but it matches the computer on lookup only \(serial\_number on the CI conflicts\). Unclassed hardware becomes the match instead of cmdb\_ci\_computer.

</td></tr><tr><td>

Column Level Encryption

 PRB2086335

</td><td>

Edge proxy schedule upgrades fail in Brazil

</td><td>

Edge proxy doesn't upgrade and the upgrade status is stuck in 'Running'. The upgrade schedule record shows status running/failed. The failure reason is 'Failed on signature verification for distribution file'.

</td><td>

1.  Request an Australia TD instance with Edge proxy configuration.
2.  Log in as a user with elevated privileges.
3.  Authenticate Edge proxy on the node instance.
4.  Request an upgrade on the TD instance using **Run Upgrade on Existing Instance from Artifacts**.
5.  Select **AP5 or AP6 Instance requested**.
6.  Log in to the Edge instance as a user with elevated privileges.
7.  Navigate to **Edge Encryption Configuration** &gt; **Proxies** &gt; **All**.
8.  Open 'Encryption Proxy Record'.
9.  Select the **Schedule Proxy** button.
10. Schedule the proxy by providing a date and time.
11. Submit.

 Expected behavior: Schedule proxy upgrades to the latest version.

 Actual: Edge proxy doesn't upgrade and the upgrade status is stuck in 'Running'.

</td></tr><tr><td>

Condition Builder in Workspace

 PRB2051562

</td><td>

'Is a' \(Instance Of\) operator displays symbols instead of value in Condition Builder

</td><td>

.

</td><td>

1.  Navigate to **Workspaces** &gt; **CMDB workspace** &gt; **'Home' tab**.
2.  Navigate to the 'CI overview' bar graph at the bottom of the page.
3.  Select any bar in the 'CI summary' tile to open the CI list.

Observe that the CI Overview page has a bar graph and a list view.

4.  From the list view, select any record.
5.  Edit the conditional builder to include the class 'is a' filter.
6.  Run the filter.
7.  Select **12 \(or X\) conditions**.

 Observe the random characters.

</td></tr><tr><td>

Contracts Core

 PRB2101745

</td><td>

'Contract documents' and 'Amendment field changes' related lists are broken

</td><td>

Related lists are breaking and the report view ACLs need to be fixed. Add a contract user role to the contract document revision report view ACL for the 'Contract documents' tab to be working properly for fulfillers. For 'Amendment field changes' related list in, add the user role to the amendment history table report view ACL to work properly. The 'Contracts documents' tab and amendment history lists are grouped, which internally might call glideaggregate, so also add report view ACLs for these tables.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB2037003

</td><td>

TableUpgrade.update DictionaryReadOnlyOption throws NPE during source control install

</td><td>

The following error appears: 'java.lang. NullPointerException: Cannot invoke 'com.glide.update. ICollisionDetector .containsKey\(String\)' because 'collisionDetector' is null'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1999432

</td><td>

The message 'Swarm64 CapabilityCheck capability is not supported on Glide' shouldn't be logged and should be removed/stopped

</td><td>

It shouldn't be logged as an error. It should be logged as info, which is normal and valid. It's not an error. It's a note recorded during startup and completely expected when connecting to a non-RaptorDB database. However, if this is Oracle DB, the message is unnecessary. This message should not be logged at all.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2016712

</td><td>

There are performance issues when querying BigQuery tables

</td><td>

It can take over 20 seconds to load the history component \(interaction history\). In addition, the Activities table list view takes a long time to load.

</td><td>

 

</td></tr><tr><td>

Date Picker

 PRB2054724

</td><td>

A **Date** field \(glide\_date\) fails to save when the session language is French and the date format is dd-MMM-yyyy

</td><td>

The **Date** field \(glide\_date\) silently drops its value when the user's language is French and the date format is dd-MMM-yyyy. The **Date/Time** field \(glide\_date\_time\) on the same record saves correctly under identical conditions, indicating that this is a platform date-only picker/parser issue, not affecting the date-time parser.

</td><td>

1.  Create a table with one **Date** field \(glide\_date\) and one **Date/Time** field \(glide\_date\_time\).
2.  Set the instance and user date format to dd-MMM-yyyy.
3.  Open a Now Experience record page for the test table.
4.  In English, fill in both fields and save.

Observe that both values save correctly.

5.  Switch the user language to French.
6.  Open a new record.
7.  In French, fill in the **Date** and **Date\_time** fields.
8.  Save.
9.  Open an existing record.
10. Edit both fields.
11. Save.

 Expected behavior: Both the **Date** and **Date\_time** fields save/update correctly regardless of session language.

 Actual behavior: When filling in a new record, the **Date\_time** field saves correctly; the **Date** field isn't saved and stays empty. When editing an existing record, the **Date\_time** field also updates correctly; the **Date** field doesn't update and retains the old value.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB2073063

</td><td>

Unbounded 300 DPI page render in MLServiceUtil. extractDataFromPDF exhausts node heap

</td><td>

 

</td><td>

1.  Create a single-page PDF with MediaBox and no extractable text layer, so detectPdfType classifies the page as scanned.
2.  Attach it to a record.
3.  Run a DocReader task definition with multimodal input enabled, so text\_only\_mode resolves to false.
4.  Inspect the heap.

 Observe that the render produces 7917x10250 pixels, which is 81.2 MP and about 325 MB as TYPE\_INT\_RGB, plus a second full-resolution copy from the PNG round trip.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB2089285

</td><td>

The roles sn\_docintel.viewer and platform\_ml\_di.viewer should not contain the snc\_read\_only role

</td><td>

If any user inherits or contains the sn\_docintel.viewer and platform\_ml\_di.viewer roles, they would inherit the snc\_read\_only role. This would refuse the user to CREATE/WRITE ops on any table, which is likely restricting the user to complete READ/VIEW mode on the instance.

</td><td>

 

</td></tr><tr><td>

Edge Encryption

 PRB2037206

</td><td>

Form fails to load in Workspace when the encrypted string field contains line breaks

</td><td>

When a ServiceNow Workspace form contains an encrypted string field with line break characters \(such as carriage return / line feed\), the form fails to render and displays a blank page. Users are forced to manually refresh the page \(F5\) to load the form.

</td><td>

1.  Create an encrypted field \(string type\) on a custom table.
2.  Populate the field with content containing line breaks.
3.  Open the record in Workspace.

 Observe that the form displays as blank. It requires a page refresh \(F5\) to load.

</td></tr><tr><td>

Email Notifications

 PRB2054721

</td><td>

Notification bell behavior changed after an upgrade from Yokohama to Australia

</td><td>

Previously, when a new notification appeared, it would disappear after a while and no other notifications would be shown. After the upgrade, when a second notification appears and disappears, the first unread notification is displayed again.

</td><td>

 

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB2107508

</td><td>

Add multi-Instance JWT minting API in the Content Taxonomy

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2033276

 [KB3152048](https://hi.service-now.com/kb_view.do?sysparm_article=KB3152048)

</td><td>

Waiting flows that are cancelled don't cancel the queued up restart trigger/event

</td><td>

There was an architectural change in how future wait events are handled, introduced between Zurich and Australia. When a flow hits a 'Wait for Duration' action, the engine schedules a flow.fire event to resume the flow after the wait period expires. In both Zurich and Australia, this scheduled event is never cleaned up when a flow context is cancelled. The cancellation only marks the context as CANCELLED but doesn't remove the pending event. The difference between releases is where the future event is parked. In Zurich, the future event was stored in a sys\_trigger record. The actual flow.fire event in sysevent was only created at the time it was due to be processed. So for cancelled flows, the orphaned record was in sys\_trigger — not visible in sysevent. In Australia, the sys\_trigger intermediate step was removed. The flow.fire event is now created immediately in sysevent in a 'Ready' state, with a future 'Process On' date. It sits there until the scheduled time is reached. The underlying gap, cancelled flows leaving behind pending wait events, exists in both releases. The difference is that Australia's change made it visible: events now accumulate in sysevent in a 'Ready' state and are observable, whereas in Zurich they were parked in sys\_trigger and went unnoticed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB2033890

</td><td>

Absolute transform doesn't work with comparators

</td><td>

When the Abs transform is applied, PillExpressionParser.java calls String.valueOf\(outputType\), where outputType is a Java Optional\[number\] instead of 'number'. The comparator then does a lexicographic \(text\) comparison. Abs\(499\) &gt; 50 compares '499' vs '50', but since four is greater than five, it returns false.

</td><td>

1.  Create a subflow.
2.  Create an input of type integer.
3.  Create an if block with the condition input greater than 50.
4.  Apply the math.absolute transform on the input \(Abs\(input\)&gt;50\).
5.  Add a log statement in the if block.
6.  Create another if block with the condition input greater than 50 and no transformations.
7.  Add a log statement in this block as well.
8.  Test the subflow by passing a number greater than 50.

 Observe that the first condition is evaluated to false \(and the second is evaluated to true, as expected\). The first condition should also evaluate to true.

</td></tr><tr><td>

Flow Engine

 PRB2077978

</td><td>

Adjust monitoring event frequency to trigger only once after 30 minutes

</td><td>

The monitoring event currently fires more frequently than necessary. Adjust the frequency so it triggers only once within a 30-minute window instead of the current cadence, to reduce unnecessary event/queue overhead.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2081205

 [KB3228806](https://hi.service-now.com/kb_view.do?sysparm_article=KB3228806)

</td><td>

Restarting non-global flows fails with 'Flow object for 'scope\_sys\_id.flow\_name' does not exist'

</td><td>

A flow built directly in the Global scope restarts as expected; it is specifically flows in a real \(non-Global\) scoped app that fail.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB2082118

</td><td>

The uncached sys\_flow\_subflow\_plan query on every subflow invocation is inside a loop

</td><td>

When a parent flow calls the same subflow a certain amount of times in a ForEach/Do-Until loop, this produces the same number of uncached DB queries for the same plan record.

</td><td>

1.  Create a subflow with a single Log step.
2.  Publish it.
3.  Create a parent flow with a ForEach loop \(iterate over any list of 10 or more items\).
4.  Inside the loop, call the subflow.
5.  Wait for the completion to '= true'.
6.  Publish it.
7.  Run the parent flow with SQL tracing enabled.

 Expected behavior: sys\_flow\_subflow\_plan is queried once and subsequent iterations use cache.

 Actual behavior: sys\_flow\_subflow\_plan is queried once per iteration with a number of identical queries for the amount of iterations.

</td></tr><tr><td>

GlideAggregate API

 PRB1922184

</td><td>

Data isn't visible in the dashboard when using time series visualization and using keywords as a filter

</td><td>

The following error appears: 'Error: No Data Available. There is no data available for the selected criteria.' The issue doesn't occur with other visualizations.

</td><td>

 

</td></tr><tr><td>

Guided Tours

 PRB2096815

</td><td>

Unable to create tours on UI26 pages \(aiux/ui/&lt;table-name&gt;\_list.do\)

</td><td>

For https://&lt;instance-name&gt;.service-now.com/aiux/ui/incident\_list.do and https://&lt;instance-name&gt;.service-now.com/aiux/ui/list/incident, the underlying page for both of these URLs is the same, but the parsing logic fails to treat these URLs as the same context.

</td><td>

1.  Navigate to **Create new tour** page.
2.  Select **AI Experiences**.
3.  Paste this url: https://&lt;instance-name&gt;.service-now.com/aiux/ui/incident\_list.do \(with the instance name replaced\).

 Expected behavior: The **Create tour** button is enabled.

 Actual behavior: The **Create tour** button isn't enabled.

</td></tr><tr><td>

Horizon iFrame Component

 PRB2055428

</td><td>

Unable to render allow clipboard=write for the UIB iframe component

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Horizon iFrame Component

 PRB2094839

</td><td>

Unable to render 'allow clipboard-read' for the UI Builder \(UIB\) iFrame component

</td><td>

 

</td><td>

In the UIB iFrame component, manually add 'clipboard-read'.

 Observe that it isn't rendered in iFrame.

</td></tr><tr><td>

HR Integrations

 PRB2081919

</td><td>

hr-scoped-sp-ux-test .RCAPrivilegesIT is failing due to an RCA issue in the IntegrationPush TodoHelperSNC script include

</td><td>

This issue was observed in Brazil.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery Integrations Framework

 PRB2030952

</td><td>

Users with the admin role can view HR Case-related user information from the 'Email Log' table

</td><td>

Users with the admin role can view information such as the HR Case requester, assigned user, and watch list users.

</td><td>

1.  Create an HR Case.
2.  Send an HR Case-related notification.
3.  Log in as a user with the admin role.
4.  Check the 'Email Log' table.

 Observe that information such as the HR Case requester, assigned user, and watch list users can be viewed.

</td></tr><tr><td>

HR Service Delivery

 PRB2074969

</td><td>

HR Core ships record-read ACLs on 'sysapproval\_approver' but no field ACLs, blanking every field for approvers

</td><td>

RCAs should be generated to cover all possible tables for Query Generation and AI Data Explorer. The covered tables should come directly from what is configured for Query Generation entities. Also, all RCAs should be put into the if / &lt;target app scope&gt; / update folders as appropriate for each target scope in the application's metadata.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2081585

</td><td>

There are missing RCA's for the Now Assist AI Data Explorer

</td><td>

The HR Core record ACL evaluates and passes, but the 'Global' field wildcard 'sysapproval\_approver.\*' is not evaluated. The result is false because the granting scope \(HR Core\) has no field ACL for the engine to evaluate.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2086829

</td><td>

AI Search RAGRetrievalAPI can't access the HR Case **Description** field for non-admin users during retrieval, even when those users can read the field directly

</td><td>

AI Search's RAGRetrievalAPI can't access the HR Case **Description** field for any user who lacks the admin role. The affected users have legitimate read access to the underlying \[sn\_hr\_core\_case\] records and can read the **Description** field directly, yet RAGRetrievalAPI behaves as though the field is inaccessible for these users — and returns the wrong cases as a result. It appears the description is fully excluded from the retrieval. Because the wrong cases are returned, the description content is not considered during the semantic search that selects candidate records. This points to a field-level access-evaluation gap in the retrieval path: for non-admin callers, RAGRetrievalAPI fails to resolve the caller's actual read permission on the **Description** field and treats it as inaccessible, so the field is neither searched over nor returned. Admin callers, whose access resolves correctly, receive correct results — which is why the behavior is gated on the admin role rather than on real read permissions.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2089613

</td><td>

Add a reusable impersonation API in the global scope to be used by HR Service Delivery apps

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2091726

</td><td>

HR uptake of new scope main table 'sys\_email\_draft' and 'sys\_email\_draft\_attachment'

</td><td>

Admin users without access to the HR Case can read the related sys\_email\_draft and sys\_email\_draft\_attachment.

</td><td>

1.  Navigate to the 'admin' role.
2.  Remove all HR roles from its 'Contains Roles' related list.
3.  Impersonate as Fred Luddy \(who should only have the admin role and no HR roles\).
4.  Navigate to sn\_hr\_core\_case.list.
5.  Verify that Fred can't access any HR case.
6.  Impersonate as 'HR Admin' \(who has the HR admin role\).
7.  Navigate to HR Workspace /now/hr/agent/home.
8.  Open any HR Case record in the workspace.
9.  Open the email client by selecting **Compose Email** under **More Options** \(three dots\).

Observe that there's a 'sys\_email\_draft' record with the target set to the HR Case. The subject is set to the HR Case's 'number - short\_description'.

10. Validate that sys\_email\_draft can be accessed by 'HR Admin' by navigating to sys\_email\_draft.list.
11. Impersonate again as 'Fred Luddy'.
12. Navigate to sys\_email\_draft.list.

 Expected behavior: Admin users that don't have access to the HR Case should not be able to read any related sys\_email\_draft or sys\_email\_draft\_attachment.

 Actual behavior: Admin users without access to the HR Case can read the related sys\_email\_draft and sys\_email\_draft\_attachment.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1768733

</td><td>

The HTML field shows as changed even though no changes occurred

</td><td>

The HTML field shows as changed without changes being made in 'History' &gt; 'Calendar'. There are no user updates to the **Rich\_description** field, but a sys\_history\_set update record appears.

</td><td>

1.  Navigate to any open incident form view.
2.  Select **Configure** &gt; **Form Layout**.
3.  Add a field \(for example, **Rich Description**\) with HTML type.
4.  Save.
5.  Create a sample record.
6.  Navigate to Scripts - Background.
7.  Run a test script.
8.  Navigate to the incident just created via the background script.
9.  Update some field \(for example, **Caller**, **Description**, etc.\).
10. Save.
11. Select **History** &gt; **Calendar**.

</td></tr><tr><td>

Identity

 PRB2081645

</td><td>

The job 'IAM Generate Federated ID for Table-sys\_user' causes a lock timeout

</td><td>

It's caused by the job ' 'IAM Generate Federated ID for Table-sys\_user', as it's running an update on the sys\_user table with a massive record. It also locks up another API call which has an update on the same table. It's better to cut this update into smaller batches to avoid the lock issue.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB2082113

</td><td>

When the producer replication set is deactivated, the consumer replication 'active' flag is not set to false

</td><td>

 

</td><td>

1.  Have active producer and consumer replication set.
2.  Deactivate the producer.

Observe the consumer XML.


 Expected behavior: 'Active' is 'false'.

 Actual behavior: 'Active' is 'true'.

</td></tr><tr><td>

Knowledge Management

 PRB2083677

</td><td>

Embedded videos added through 'Insert/Edit Media' are removed from Knowledge Base \(KB\) articles and don't render in Service Operations Workspace \(SOW\)

</td><td>

Embedded videos don't appear in KB articles Service Operations Workspace even after pasting the embed code from the video in the Insert/Edit Media modal in the editor.

</td><td>

1.  Open Service Operations Workspace.
2.  Open the list menu.
3.  Navigate to **Knowledge** &gt; **All published articles** &gt; **New**.

Observe that the new kb\_knowledge Edit form opens in SOW.

4.  Fill in all the mandatory fields.
5.  In the article body, use the editor.
6.  Select **Insert/Edit Media**.

Observe that the Insert/Edit Media modal opens.

7.  Select the 'Embed' tab.
8.  Paste the embed code from the video.
9.  Select **Save**.
10. Save the knowledge record.
11. View the article by selecting **View Article**.

 Notice that the embedded view does not show in SOW.

</td></tr><tr><td>

Knowledge Management

 PRB2100264

</td><td>

sn\_genai\_platform true-up install failure due to sn\_generative\_ai dependency version mismatch in base instance apps

</td><td>

When attempting to install the trued-up version of the sn\_genai\_platform app, the installation fails. Going into the Application Manager's activity log shows: sn\_generative\_ai needs to be procured from store — 15.1.1. The version trued up \[sn\_generative\_ai\] in base instance apps differs from the app versions \[sn\_generative\_ai\] on other instances. The dependency links don't match between base instance apps and the trued-up app records. The dependency-version true-up was missed and only the app record itself got trued-up to a version that doesn't match its declared dependency.

</td><td>

 

</td></tr><tr><td>

Licensing Entitlement Engine

 PRB2093748

</td><td>

Review RVACLs on Stats API and GraphQL Aggregate API Calls LE

</td><td>

The Stats API and GraphQL API enforce Report View ACLs in scenarios where they previously didn't. For example, a user who previously received full results from these APIs may now see fewer results, because they lack a Report View ACL granting access to the data.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2011679

</td><td>

List data broker transform throws an error when attempting to destructure a null object

</td><td>

 

</td><td>

1.  Navigate to **SOW** &gt; **List** &gt; **Incidents - All**.
2.  In the browser developer tools network tab, find the /now/uxf/databroker/exec call that retrieves the list.
3.  Select and hold \(or right-click\) the request.
4.  Select **Copy as fetch**.
5.  Paste the fetch in the console.
6.  Modify the 'Table' property to pass an empty string or null value.
7.  Press Enter to send the request.
8.  Return to the network tab.

 Observe the error in the new request.

</td></tr><tr><td>

List Administration

 PRB2020153

</td><td>

The tab view and list view aren't working correctly

</td><td>

 

</td><td>

1.  Open a form \(for example, the Incident Form\).
2.  Add a 'Problem' tab to the Related Lists.
3.  Select the 'Problem' tab.
4.  Select and hold \(or right-click\) to configure.
5.  Select **List Control**.
6.  Select the **Omit columns if empty** option.
7.  Submit and save.
8.  Navigate to the Incident Form.
9.  Open the avatar.
10. Select **Preferences**.
11. Disable **Organize form sections and related lists into tabs in classic forms**.
12. Enable it again.

 Observe that the Related Lists aren't tabbed anymore.

</td></tr><tr><td>

List Administration

 PRB2104857

</td><td>

**Global Delete** UI actions aren't uptaking the latest changes

</td><td>

'\[Glide\] Support base instance delete action' was fixed as part of the UI16 parity effort for UI26. These changes migrate the delete-confirm UI page into a core-ui widget, which required changes to the UI action files on Glide. After the Glide changes made it in, remote instances were not picking up the fix \(regardless of mod count increases\) and therefore causing the new delete widget to fail. Upon investigation, the UI actions that got updated on Glide had duplicate files with the same sys\_id and global scope on app-cmdb. The duplicate files from CMDB get installed after Glide as plugins, so mod counts were ignored and Glide changes overridden. For these changes to get picked up, two requirements must be met on the new fix: first, CMDB deletes the duplicate files that are overriding the changes on Glide and second, the files need to get a mod count increase so the instances can install the new version.

</td><td>

 

</td></tr><tr><td>

List Filters

 PRB2031646

</td><td>

Mixed language text is displayed in the filter

</td><td>

When the session is in a language other than English, the pop up invoked from the list filter controls displays text in English.

</td><td>

1.  Provision a Zurich instance with the I18N: Brazilian Portuguese Translations plugin installed.
2.  Open the System Preferences.
3.  Switch the language to Portuguese.
4.  Open Service Operations Workspace.
5.  Select the **List** icon.
6.  Open any interaction.
7.  Select the filter control **x filtros**.

 Observe that there is English text content, such as 'Generate filters', when it should be in Portuguese, such as 'gerar filtros'.

</td></tr><tr><td>

Machine Identity Access Control

 PRB1991942

</td><td>

When trying to set up Machine Identity Access control for write access on a Table API to the 'Incident' table, the API account can create incidents, but if it tries to write to the **Comments** or **Work\_notes** fields, an error is seen

</td><td>

The message: 'Error occurred while setting field 'comments' with value testing', 'detail': 'com.glide.security .mi.access\_control. MachineIdentityAccessException: Failed machine identity validation for table sys\_attachment'.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1982535

</td><td>

An agent isn't going down when invalid characters are appended with the API key in the acc.yml file

</td><td>

 

</td><td>

1.  Install the Agent on the instances of Australia versions.
2.  Set up ACC and ACC-M.
3.  Navigate to the Virtual Machine where the Agent is installed.
4.  Append some random characters with the existing API key in the acc.yml file.
5.  Restart the Agent from services or from the instance.
6.  Verify whether the Agent goes down or not.

</td></tr><tr><td>

Mobile Platform

 PRB2090163

</td><td>

Unable to reach MobileAIUXUtils from scoped context

</td><td>

When calling SNC.MobileAIUXUtils. setExperienceSwitchEnabled from a scoped context, it is not accessible.

</td><td>

Call SNC.MobileAIUXUtils. setExperienceSwitchEnabled from a scoped context.

 Expected behavior: The sys\_properties record is created and set to true or false based on the values passed in.

 Actual behavior: The function isn't available and no property is created.

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2092679

</td><td>

The KB MMS Job gets recreated without reading from stored results

</td><td>

Checking out a KB article sends its unchanged attachments to MMS again. Checking it out copies the attachments onto the new version as new sys\_attachment rows, and the MMS upload rule treats each copy as a new upload.

</td><td>

Move the KB to the states Publish &gt; Checkout &gt; Publish.

 Observe the duplicate job creation.

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2104952

</td><td>

MMS Glide update

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Next Experience All Menu

 PRB2091536

 [KB3159690](https://hi.service-now.com/kb_view.do?sysparm_article=KB3159690)

</td><td>

The Next Experience 'All' menu fails or takes longer to load

</td><td>

The issue occurs in Zurich, Australia, and Brazil.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1997428

</td><td>

There's an incorrect CSS variable in .menu-item-header:hover .label

</td><td>

In the application menu, an incorrect CSS variable is used for the label for the :hover state. As a result, the application menu is unreadable. For the hover state, --now-unified-nav \_menu-item--color is used, even though the correct variable --now-unified- nav\_menu-item-- color--hover already exists for this purpose.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2027423

</td><td>

When Next Experience is disabled, navigation from a UXF page fails and opens a new tab instead of the expected form due to missing route configuration in the experience context

</td><td>

When users turn off the Next Experience, selecting certain buttons \(such as **New**\) doesn't open the expected page. Instead, it opens a blank or incorrect page in a new browser tab, causing confusion and disrupting normal workflow.

</td><td>

1.  Log in to an Australia instance.
2.  Navigate to **User Menu** &gt; **Preference** &gt; **User Experience**.
3.  Turn off Next Experience.
4.  Navigate to change\_request.list.
5.  Select **New** to create a change.
6.  Select the **Normal** change.
7.  Select **Continue**.

 Expected behavior: The change form opens.

 Actual behavior: A new tab opens, but not the change form.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2039347

</td><td>

Pop-up modals for elements in the Next Experience banner are misaligned to the icons

</td><td>

This issue occurs in Australia.

</td><td>

1.  Log in to an Australia instance
2.  From the banner, select the **Notifications Bell** or the **PA** icon

 Observe that the pop-up modal expands down from the **Domain** icon or the search bar, not the icon that was just selected.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2057599

</td><td>

Navigation from the action button doesn't work

</td><td>

No navigation occurs or the expected page doesn't load.

</td><td>

1.  Open the application or webpage containing the action button.
2.  Select the action button intended to trigger navigation.

 Observe that no navigation occurs or the expected page doesn't load.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2077076

</td><td>

In NextWave, the voice input keyboard shortcut doesn't work when the Otto panel is open

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  After loading, press Opt + Shift + V.

Observe that Otto opens with voice input enabled.

3.  After speaking the question, submit the query.
4.  When Otto is open, press the shortcut again.

 Observe that the voice input doesn't activate.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB2090838

</td><td>

'Say hello to ServiceNow Otto' pop-up appears over the Clone Admin Console authentication flow, disrupting the auth flow each time

</td><td>

The pop-up has no persistent dismiss option and it reappears on reload/reflow of the page. The portal-only system property doesn't suppress it in this flow.

</td><td>

1.  Trigger the Instance Clone authentication flow \(Clone Admin Console\).

Observe that the 'Say hello to ServiceNow Otto' pop-up renders over the auth UI.

2.  Attempt to dismiss it.

 Observe that the pop-up has no persistent dismiss option and it reappears on reload/reflow of the page.

</td></tr><tr><td>

OAuth

 PRB2036247

</td><td>

The user is not able to perform a cookie exchange on an aiuxpod instance

</td><td>

An authentication error occurs when the user attempts to log in to the aiuxpod instance.

</td><td>

 

</td></tr><tr><td>

OAuth

 PRB2073238

 [KB3148183](https://hi.service-now.com/kb_view.do?sysparm_article=KB3148183)

</td><td>

Model Context Protocol \(MCP\) clients that do strict issuer validation can't connect to the ServiceNow MCP Server

</td><td>

Due to an issue in which the protected resource metadata for the MCP includes the resource path in the authorization server URL, there's an issuer mismatch in which Glide is the authorization server. Furthermore, Glide doesn't advertise any metadata at the base metadata path \(https://&lt;instance&gt;.service-now.com/well-known/oauth-authorization-server/\).

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OAuth

 PRB2095958

</td><td>

Whenever someone experiences node switch and the first request their browser makes is $uxapp.do, they can't use employeeworks until they log out

</td><td>

 

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB2024542

</td><td>

The new 'Trigger Engine Handler' subflow can execute before the triggering record is committed

</td><td>

This causes a silent trigger rule processing failure.

</td><td>

Run the verifyRTREscDetailsForSMS test 5–10 times.

 Observe that the test fails intermittently with 'trigger\_rule\_wf\_context not found'.

</td></tr><tr><td>

OneExtend

 PRB2056072

</td><td>

When an agent runs a skill, there is no control on the skill chain time out

</td><td>

If it's changed in one\_api\_service \_plan\_feature, it might reset after the changes.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2082859

</td><td>

Script-include capabilities routed via FDIH engine throw FlowObjectAPIException, breaking Virtual Agent \(VA\) sensitive-data masking and blocking all outbound messages

</td><td>

There is a Virtual Agent outage whenever 'Requester to VA' sensitive-data masking is enabled in Data Privacy, because that feature synchronously invokes a script-include-backed capability on every single outbound VA message. When that capability call errors, the exception propagates uncaught up through the message-masking pipeline into MessageServerProxy .enqueueAMBMessage\(\), so the outbound message is never delivered to the client. Users see 'This message is unable to be sent' starting with the very first bot message, and the conversation never progresses—it remains stuck Open indefinitely.

</td><td>

1.  Provision an instance with an active http\_connection record that has an empty connection\_alias and use\_mid=true.
2.  Execute any OneExtend/GenAI capability backed by a script include \(api\_type= sys\_script\_include\) in sync mode.

 Observe that the notification 'This Message is unable to be sent' appears from the first bot message onward.

</td></tr><tr><td>

OneExtend

 PRB2087863

</td><td>

Sync raw value only for definition name and capability name

</td><td>

Capability definitions with translated names fail to execute against the LLM proxy whenever metadata sync runs under a non-default-language session. The translated name value \(sent as an HTTP header\) can contain non-ASCII/special characters that HTTP headers reject, causing the LLM proxy call to fail.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2121845

</td><td>

When an agents calls a skill, then calls another skill, the sub components don't get triggered

</td><td>

When the agent calls a skill, calls another skill, then calls a script, the script call \(or any other component\) doesn't happen. When triggering the parent skill from skill kit, it works.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1989421

</td><td>

Platform Analytics's historical data collection is overriding the indicator score even when 'Collect Indicator' is set to 'False'

</td><td>

When users attempted to perform a historical collection solely for the breakdown items, without collecting the indicator scores themselves by setting 'Collect Indicator' to 'false' and excluding all other breakdowns from the collection, they encountered several issues. The most critical problem was the creation of duplicate scores, which caused the indicator to either error out or reference an empty score record. Additionally, for some indicators, setting 'Collect Indicator' to 'false' did not behave as expected. Instead of collecting only the specified breakdown, the system collected the indicator score itself while completely ignoring the intended breakdown in the collection process.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB2065499

</td><td>

PostgreSQL Column related error messages appear when accessing the dashboard

</td><td>

The following error appears whenever the dashboard library page is accessed: 'DASHBOARD\_ABSTRACT\_PROVIDER: Error loading dashboardsowner group: org.postgresql. util.PSQLException: The column name sys\_user\_group.name was not found in this ResultSet.: org.postgresql.jdbc .PgResultSet.findColumn \(PgResultSet.java:3121\)'.

</td><td>

1.  Provision an instance on raptor DB with the PA Premium plugin installed.
2.  Create any dashboard.
3.  Set the dashboard's owner to a group.
4.  Run the 'PA Indicator Recommendation Calculator Job' \(Execute Now\).
5.  Check the syslog filtered on message LIKE DASHBOARD\_ABSTRACT\_PROVIDER.

 Observe that the error appears.

</td></tr><tr><td>

Platform Analytics Dashboard

 PRB2054112

</td><td>

Filters with default values aren't applied when a dashboard is loaded for the first time

</td><td>

The default value filter isn't applied when the user opens the dashboard. If the user switches tabs, then the filter is applied.

</td><td>

1.  Create a dashboard.
2.  Add bar or pie charts to different tabs in the dashboard.
3.  Add a filter and select a default value. \(For example, if the widgets are on the incident table, then add a filter on the **State** field and select 'New' as the default value.\)
4.  Share this dashboard with an itil user.
5.  Impersonate the itil user.
6.  Open the dashboard.

 Observe that the default value filter isn't applied.

</td></tr><tr><td>

Platform Analytics Filters

 PRB2052359

</td><td>

Filter preferences are received after the filter components have connected

</td><td>

The filterConfigurations from user preferences are received after the filter components have connected, by which point some visualizations have already fetched and rendered unfiltered data.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2066117

</td><td>

AbstractMigrator holds the reference to the last migrated/processed dashboard layout

</td><td>

The evaluateScript calls leave variables of about 40 MB dashboards/dashboard JSON retained by the evaluator.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2081175

</td><td>

Setting glide.par.coreui .migration.new\_coreui \_artifacts\_created to 'true' causes PAR dashboard deletion during re-migration

</td><td>

Dashboards that were migrated successfully are deleted when re-running the migration.

</td><td>

1.  Create a Core UI dashboard \(pa\_dashboards\).
2.  Open the Migration Center and run the content migration.
3.  After the migration is complete, activate all migrated content.
4.  Open System Properties.
5.  Set glide.par.coreui. migration.new\_coreui \_artifacts\_created to 'true'.
6.  Return to the Migration Center.
7.  Re-run the content migration.

 Expected behavior: Re-running the migration should not delete dashboards that have already been successfully migrated.

 Actual behavior: The previously migrated Core UI dashboard is deleted during re-migration.

</td></tr><tr><td>

Platform Runtime

 PRB2080757

</td><td>

The 'Regions' attributes are missing on a form when users create a Dynamic Translation connection

</td><td>

An error displays.

</td><td>

 

</td></tr><tr><td>

Playbook Experience Core

 PRB1975947

</td><td>

The record generator activity title doesn't translate after language translation

</td><td>

 

</td><td>

1.  Download Dynamic Translation and a couple languages in the instance.
2.  Set up Guided Playbook layout in the instance.
3.  Open the URL to preview.
4.  Change the language preference to a language other than English.
5.  Trigger the playbook.
6.  Change the language preference to English.

 Expected behavior: The title of the first activity \(record generator\) is translated to English.

 Actual behavior: The title of the first activity \(record generator\) isn't translated.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2019873

</td><td>

For playbook activities, the auto-complete and drop-down options are missing for configurable fields under the 'Automation' tab

</td><td>

.

</td><td>

1.  Create a playbook in Workflow Studio.
2.  Add the following activities to the playbook:
    -   Create New Record Activity \(configuring for a 'Group Member' record\)
    -   Update Record Activity \(configuring for a 'Requested Item' record\)
    -   Ask for Approval Activity
3.  Navigate to the 'Automation' tab for each of these activities.

 Observe that there are discrepancies, such as missing auto-complete and drop-down options, and incorrect field types.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2072254

</td><td>

No Playbook activities are displaying in Playbook Launcher \(Record Generator\)

</td><td>

There is a single line in the stepper section of a Playbook when users land on the Playbook. Usually all the steps should be visible, but after filling the first step details and selecting 'continue', all steps in the stepper are visible.

</td><td>

1.  Impersonate a user.
2.  Navigate to partner portal \(/partner\).
3.  **Create** &gt; **Create Quote**.

 Expected behavior: All playbook activities are displayed before Playbook launches.

 Actual behavior: Only the launcher activity is displayed. All other activities are hidden.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2075258

</td><td>

ConcurrentModificationException comes when two concurrent playbook executions are created

</td><td>

When two records are created together for playbook execution, it tries to race for the creation of activity contexts, resulting in one of the playbook execution records erroring out.

</td><td>

1.  Create a playbook with a trigger on the record creation.
2.  Attempt to create two records simultaneously using JSON API or Scriptable API 3.

 Expected behavior: Both playbooks run normally.

 Actual behavior: One of the playbook execution records errors out.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2096921

</td><td>

The Playbook fails to load 'Error fetching playbook' for playbooks with 'After specific stages' once a Playbook Experience record generator has previewed them, and an NullPointerException \(NPE\) occurs in isOnIdealPath

</td><td>

The NullPointerException shows 'Cannot invoke 'Activity.isLaneStartActivity\(\)' because 'activity' is null.' The PlaybookContextQuery catches it as 'Error fetching playbook', and the whole playbook response is empty, including the intake. This issue is found in Brazil instances, but works as expected in Australia because isOnIdealPath is not in that build.

</td><td>

1.  Open a thunder devsnc instance.
2.  Select Opportunities.
3.  Navigate to **Grant Program 1** &gt; **Apply now**.
4.  Complete the 'Answer eligibility question' activity with the answer 'Yes' to all the questions.
5.  Navigate to **Next**&gt; **Start Proposal**.

Notice that in portal, after selecting **Start proposal**, the case \(GPR…\) is created but the playbook area stays blank. The message 'There are no playbooks available' occurs in the workspace.


 Expected behavior: The playbook renders with all stages and activities, as it does on Australia.

 Actual behavior: There is a blank playbook panel in portal. The message 'There are no playbooks available. Please contact your system administrator.' occurs in the workspace. An NPE occurs in the syslog: 'GraphQL API - GlideGraphQL: Exception encountered processing path: /GlidePlaybookContext\_Query /getPlaybookContexts ByParentRecord - Error fetching playbook \(no cause logged\).'

</td></tr><tr><td>

Process Mining Workspace

 PRB2091109

</td><td>

The **Finding Condition** field drop-down list allows journal-type fields, causing the save to fail with the generic message 'Finding Condition save failed'

</td><td>

When configuring a rule-based finding definition's start/end condition \(snProminRuleBased FindingsConnected &gt; saveFindingDefs\), the condition builder's field drop-down list lets the user select journal-type fields on the target table \(for example, comments on sn\_customerservice\_case\). However, promin\_finding \_def\_condition doesn't support journal fields as condition fields. ProminAllowedColumns .\_getInternalTypes\(\) only allows choice, string, boolean, integer, reference, workflow, and glide\_date\_time for promin\_finding \_def\_condition \(unlike promin\_activity\_def, which explicitly allow lists journal\_input\). The 'Business Rule Validate' allowed fields are selected on promin\_finding \_def\_condition. The insert for a journal field is correctly aborted, but the failure only surfaces to the user as a generic success: false / 'Finding Condition save failed' from saveFindingDefs. There's no indication of why or which field is invalid.

</td><td>

1.  Open guided setup / condition builder for a rule-based finding definition on sn\_customerservice\_case.
2.  Set an end condition of type PROPERTY, field = comments \(or any journal field\), and predicate = ANY.
3.  Navigate to **Save** &gt; **Mutation**.

 Expected behavior: The field drop-down list in the condition builder filters out journal-type fields upfront \(mirroring the server-side allow list in ProminAllowedColumns\) so an invalid field can't be selected in the first place. This is consistent with how the platform's own 'Grouping is automatically turned on for textual or journal fields' note treats journal fields differently in the Activity Definition step.

 Actual behavior: It returns success:false, with the following message: 'Finding Condition save failed'. There's no field-level guidance.

</td></tr><tr><td>

Process Mining Workspace

 PRB2095452

</td><td>

Sample mining is blocked for sub-prod instances

</td><td>

Process Mining lets sub-production instances to sample mine. The use case is that a user gets in touch with Process Mining using the evaluation projects, and when the user needs some unique analysis, it is nice to have the option of them cloning to sub-prod with audit log data included to accommodate those scenarios in the sales cycle. The last couple of months, ServiceNow has been closing sub-production instances that were labeled as 'open'. An open instance doesn't check for licenses, where a closed instance does. Many sub-production instances are now blocked.

</td><td>

1.  Navigate to a sub-prod instance that is closed.
2.  Try to sample mine.

 Observe that the mining fails.

</td></tr><tr><td>

Project Management

 PRB2033720

</td><td>

Duplicate cost plan breakdown records are created

</td><td>

When a cost plan is created or updated, the system needs to find or create a task-type breakdown record in the cost\_plan\_breakdown table for each fiscal period and expense type combination. The logic for this lives in PPMRollup RecordFinder. findOrCreate RollupRecord ForEntity\(\). The method works as follows: Query cost\_plan\_breakdown for a record matching task + fiscal\_period + expense\_type + breakdown\_type. If no record is found, insert a new one. These are two separate database operations with no locking between them. When two threads execute this logic concurrently for the same cost plan and fiscal period — which happens when a Flow Designer flow triggers cost plan creation actions in parallel, or when two events \(resource\_plan .update\_cost\_plan\) are fired simultaneously for the same resource plan — both threads perform the existence check at the same time, both find zero records, and both proceed to insert. Since there is no unique constraint on the cost\_plan\_breakdown table for the combination of task + fiscal\_period + expense\_type + breakdown\_type, both inserts succeed and two identical logical records are created. The DB logs from the instance show two INSERT statements into cost\_plan\_breakdown for the exact same task, fiscal\_period, and expense\_type, executed two milliseconds apart on two separate scheduler worker threads \(worker.4 and worker.6\) in different transactions.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB2074908

</td><td>

The Planned End Date and Duration don't revert after moving and reverting the planned start date

</td><td>

After changing and reverting the Planned Start Date on a project, the Planned End Date and Planned Duration don't recalculate to their original values. The issue stems from the project constraint date not updating, causing child tasks and rollup dates to remain pinned.

</td><td>

1.  Open a BPI Dev instance.
2.  Create a project.
3.  Import the MSP file.
4.  Verify the initial values:
    -   Planned Start Date: 06/02/2026 08:00:00
    -   Planned End Date: 10/05/2026 12:00:00
    -   Planned Duration: 86 Days 4 Hours
5.  Use the 'Move project' function to change the Planned Start Date to  06/08/2026  08:00.

Observe that the Planned End Date becomes  10/12/2026  13:00 and the Planned Duration becomes  90  Days  4  Hours.

6.  Use the 'Move project' function again to revert the Planned Start Date to  06/02/2026  08:00.

 Expected behavior: The Planned End Date returns to 10/05/2026  12:00 and Planned Duration returns to  86  Days  4  Hours.

 Actual behavior: The Planned End Date remains  10/12/2026  13:00 and Planned Duration shows  94  Days  4  Hours.

</td></tr><tr><td>

Reporting

 PRB2089532

</td><td>

Read-only report viewer link isn't visible

</td><td>

When sharing in report designer, the read-only report viewer link isn't visible.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB2093303

</td><td>

KittyScript should check the function provenance on a call target

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB2052356

 [KB3157750](https://hi.service-now.com/kb_view.do?sysparm_article=KB3157750)

</td><td>

When web embeddables are turned on, UXF dependency assets are unavailable for a dependent component

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB2054374

</td><td>

Properties marked as 'display read only' are editable on Service Portal

</td><td>

When a property is marked as 'display read only', it properly displays as read-only in UI16, but remains editable when viewed in the Service Portal.

</td><td>

1.  Add or modify a property to a table \(for example, incident\).
2.  Configure the 'Read only option' to be 'Display Read Only'.
3.  Open the record in UI16.
4.  Confirm that the property properly displays as read-only.
5.  Open the same record in Service Portal \(id=form, etc.\).

 Expected behavior: The property is displayed as read-only, like it is in UI16.

 Actual behavior: The property is displayed as editable.

</td></tr><tr><td>

Service Portal

 PRB2063295

</td><td>

The user preference widget isn't working correctly when a user changes their language on the Employee Center

</td><td>

When selecting the language immediately above the currently selected language, the change isn't applied on the first attempt. The language is updated only after selecting it again or refreshing the page. However, selecting the language immediately below the current selection works as expected on the first attempt.

</td><td>

1.  Log in to an instance.
2.  Impersonate the System Administrator user.
3.  Navigate to the Employee Center \(ESC\) Portal.
4.  Select the **Profile** icon.
5.  Scroll down to the language preference.
6.  Open the language drop-down list.
7.  Select the language immediately above the currently selected language.

Observe that the language doesn't change on the first attempt.

8.  Select the same language again or refresh the page.

Observe that the language is updated.

9.  Select the language immediately below the currently selected language.

Observe that the language changes successfully on the first attempt.


 Expected behavior: The selected language is applied immediately on the first attempt, regardless of which language is selected.

 Actual behavior: When selecting the language immediately above the currently selected language, the change isn't applied on the first attempt. The language is updated only after selecting it again or refreshing the page. However, selecting the language immediately below the current selection works as expected on the first attempt.

</td></tr><tr><td>

Session Management

 PRB2051647

</td><td>

claimSessionSync\(\) crashes with ISE on invalidated-but-non-null HttpSession, silently canceling REST transactions with HTTP 200

</td><td>

In Transaction.claimSessionSync\(\), when getHttpSession\(\) returns an invalidated-but-non-null HttpSession—retrieved from Glide's SyncedSessions cache during a race with Tomcat's background session reaper — the null check at line 3421 is bypassed. SessionEscrow.forHttpSession\(\) correctly detects the invalid session and returns NULL\_SESSION\_ESCROW, but this signal is not acted upon. recordRequestInSession\(\) is called with the same invalidated session and throws 'IllegalStateException: Session \[...\] has already been invalidated'. The transaction is silently cancelled in the catch block \('cancel\(\)' + 'setClaimed\(\)'\), 'asyncContext.complete\(\)' is called with no response body written, and Tomcat sends HTTP 200 OK by default. The caller believes the request succeeded.

</td><td>

 

</td></tr><tr><td>

Session Management

 PRB2087070

</td><td>

'glide.gig.client.endpoints' in the deny list causes a 'skipped error' during upgrade and prevents base instance sys properties from being installed

</td><td>

During cloning, if the source instance has glide.gig.client.endpoints sys properties set, and the destination \(target\) does not, this sys property may be copied from source to target. This configuration is instance specified and should not be cloned.

</td><td>

Upgrade from Australia Patch 5 to Australia Patch 6.

 Observe the skipped error in the upgrade history.

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB2009353

</td><td>

The base instance repeat value for the sidebar notification events process is excessive

</td><td>

The job is set to run on all active nodes every two seconds. If there are 33 nodes, then it checks for new events 16.5 times every second. This is an excessive amount for base instance behavior.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB2100419

</td><td>

App sn\_audit\_response fails to upgrade to true-up version 2.0.6 due to a scope ID mismatch

</td><td>

2.0.6 declares a dependency on a scope called sn\_audit\_workspace. That scope can't be resolved on this instance because the Audit Workspace app is registered under the scope sn\_audit\_ws. The whole app load aborted, and sn\_audit\_response stayed on 2.0.1.

</td><td>

 

</td></tr><tr><td>

Software Entitlements

 PRB1961409

</td><td>

Accept the PPN suggestion 'Accept message' issue for SAMP

</td><td>

The message is confusing since the PPN is accepted. It should be an info message, not an error.

</td><td>

1.  Create a custom publisher/product/ppn /dmap/software models/ entitlements.
2.  Create a PPN suggestion.
3.  Accept the suggestion.

 Observe that the message displays.

</td></tr><tr><td>

Software Models

 PRB2002367

 [KB2837313](https://hi.service-now.com/kb_view.do?sysparm_article=KB2837313)

</td><td>

A discovery model to a software model matching job doesn't update the latest log properly

</td><td>

Currently, the 'SAM - Discovery Model to Software Model matching' job picks the latest record in samp\_job\_log by the highest number. If the log numbers are corrupted and the one with the latest created date doesn't have the highest number, the job updates an older log.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Stream Connect Core

 PRB2081573

</td><td>

MessageRetryJob never retries undelivered messages whose sc\_topic\_alias resolves to a Hermes topic \(V3 Hermes-via-alias\)

</td><td>

MessageRetryJob.execute\(\) is supposed to retry both Direct Kafka messages and Hermes \(V3, via topic alias\) messages per its own inline comment, 'Try all direct kafka messages and V3 Hermes messages'. It only builds two queries against sys\_undelivered\_messages: sc\_topic\_alias IN \(the set of Direct-Kafka-backed alias sys\_ids returned by SCTopicRepository. getDirectKafkaClusterMap\(\)\) and sc\_topic\_alias ISEMPTY \(older V2 Hermes messages with no alias at all\).

</td><td>

1.  Create a Stream Connect producer/flow that sends via a sc\_topic\_alias, whose underlying topic is Hermes-backed \(such as SCHermesTopic, not in sys\_kafka\_direct\_topic\).
2.  Force a delivery failure so a row lands in sys\_undelivered\_messages with sc\_topic\_alias populated pointing at that Hermes-backed alias.
3.  Let MessageRetryJob run \(scheduled job in glide-ih-kafka\).

Observe that for execute\(\) \(MessageRetryJob.java:70-82\), the row value sc\_topic\_alias is not in the Direct-Kafka-only set returned by SCTopicRepository .getDirectKafkaClusterMap\(\) \(SCTopicRepository .java:135-148\), and sc\_topic\_alias is not empty either, so the row matches neither of the two queries built in execute\(\).


 Observe that the row is never passed into retryMessagesForACluster\(\) and is never resent or removed. It remains in sys\_undelivered\_messages indefinitely across every job run.

</td></tr><tr><td>

System Events

 PRB2096831

</td><td>

Add a lower bound to the runtime of events for Threadpool admission

</td><td>

For now, there's only an upper bound threshold beyond which the events are rejected from the Threadpool admission for in memory processing. There's a need to add a lower bound also for the runtime below. The events shouldn't be admitted into the threadpool queue and should process as usual, flow events through jobs.

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB2052677

</td><td>

Com.glide.db.StatementBatcher functionality doesn't work as expected

</td><td>

Statements should be added to DMLActionBatcher via GlideRecord, similar to the existing StatementBatcher convenience method, glideRecord.insert Batched\(statementBatcher\).

</td><td>

1.  Enable the localhost logging to check log statements.
2.  Set glide.db.trace to true.
3.  Navigate to **System Import** &gt; **Data sources**.
4.  Create a data source of type 'Custom Load' by script.
5.  Set 'Use batch import' to true.
6.  Insert 100 records.
7.  Select the load records.

 Observe that the functionality doesn't work as expected.

</td></tr><tr><td>

System Import Sets

 PRB2054220

</td><td>

Use DMLActionBatcher instead of StatementBatcher to process batched records on import sets

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

System Update Sets

 PRB2031247

</td><td>

The update set install tracking captures a store app as 'plugin' instead of 'application' for admins without elevated privileges

</td><td>

 

</td><td>

1.  Log in as an admin without elevated privileges.
2.  Find a store app with a v\_plugin row where the 'state' is blank and 'entitled = not\_applicable' \(for example, sn-app-analytics-center or scope sn\_analytics\_cen\).
3.  Check the type produced by the capture logic.

Observe that the result is plugin.

4.  Log in as a user with elevated privileges.
5.  Check the type produced by the capture logic again.

Observe that the result is 'application'.

6.  Log in as an admin without elevated privileges again.
7.  Add the app to a global, in-progress update set.
8.  Enable application installation tracking through the update set.

Observe that the created sys\_upgrade\_plan\_item has type=plugin with a version.

9.  Retrieve or preview the update set on a target instance.

 Observe that the preview says: 'Plugin &lt;id&gt; already active on the instance'. The only option is to skip, so the app is never upgraded to the captured version.

</td></tr><tr><td>

Trace Collector \(Glide Family Channel\)

 PRB2107971

</td><td>

Trace collector MID code for Azure Hosted Agents, OAuth for New Foundry, and GCP Quota Exceed Fallback

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB2090954

</td><td>

Glide.gateway\_fixed\_thread \_pool.queue\_depth has no change listener and edits require a restart to take effect

</td><td>

ThreadPoolProvider defines three tuning properties for the gateway fixed thread pool: glide.gateway\_fixed \_thread\_pool.core\_size, .max\_size, and .queue\_depth. The first two \(fixedCorePoolSize and fixedMaxPoolSize\) override GlideProperty.notify\(\) and call reconcileGatewayFixedPool\(\) on every change, so editing them resizes the live GATEWAY\_FIXED \_THREAD\_POOL immediately. FixedQueueDepthLimit \(backing .queue\_depth\) has no notify\(\) override at all, so a change to this property is never propagated anywhere.

 The value is read exactly once, at static init, to build the pool's queue. GatewayFixedThreadPool stores it in a private final int fQueueDepthLimit and passes it directly into new LinkedBlockingQueue &lt;&gt;\(queueDepthLimit\). Neither the field nor the queue's own capacity can change after construction; GatewayFixedThreadPool exposes no setter for it, and LinkedBlockingQueue has no capacity-change API. GATEWAY\_FIXED \_THREAD\_POOL is public static final and is never recreated, so no live code path re-reads this property short of a full node restart.

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB2093345

</td><td>

GIG doesn't release an already-decided error response to the client until the entire rejected request body has been relayed and drained

</td><td>

ResponseImpl.complete\(\) waits for drain to complete before sending the response. Drain operation doesn't have a maximum size or timeout, so the client waits until all the content is read.

</td><td>

1.  With GIG enabled, POST a file larger than 25MB to /api/now/table/ecc\_queue \(or any REST Table API endpoint\).

Observe that Glide rejects it in about a second \(400, payload too large\), but gig-client doesn't get that response back for a long time, if ever.

2.  Send the same request to a GIG disabled instance hostname \(for example, the worker-node pool\).

 Observe that the 400 comes back in seconds, regardless of file size.

</td></tr><tr><td>

UI Form Administration

 PRB2097502

</td><td>

The 'for Sync' resolved view to a URL doesn't handle new records correctly

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB2090986

</td><td>

The db.client. operation.duration metric emit can call into scripting layer from DBI

</td><td>

The issue can occasionally cause increased memory usage or processing thread hangs.

</td><td>

Flush the cache \(preferably the scope provider cache and System Include Scripts cache\).

 Observe that any methods going through DBI close and call into scripting layer.

</td></tr><tr><td>

UX Framework

 PRB1996624

</td><td>

Add-on events aren't caught when a page is used as a subpage

</td><td>

For subpage 'announcements', when users select the card in 'Grid' mode, it works. But when the same subpage is embedded in another page, it doesn't work. On investigation, it was found that in the chain of events, the add-on event mapping on the target event 'Announcement ECAM action' doesn't get triggered.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB2058707

</td><td>

When a user selects **New** from a Knowledge article list in a workspace, the article interceptor/page intermittently renders blank on the second or subsequent attempt

</td><td>

Selecting the **New** button on the list side of KB articles in Service Operations Workspace \(SOW\) gives an empty interceptor when attempting to create an article for the second or third time. This issue is intermittent, and sometimes the blank interceptor page appears after multiple tries.

</td><td>

1.  Navigate to an instance.
2.  Open the SOW.
3.  Open the list.
4.  Navigate to **Knowledge Management** &gt; **All articles**.
5.  Select the **New** action.
6.  Select the interceptor and try creating the new article.
7.  Return to the list view and select the **New** action again.

 Observe that the second time interceptor page is not loading and is blank.

</td></tr><tr><td>

UX Framework

 PRB2069094

 [KB3225373](https://hi.service-now.com/kb_view.do?sysparm_article=KB3225373)

</td><td>

Users are unable to select menu API calls on a SURF clone instance

</td><td>

The landing page is missing from the menu list. The request isn't being called on any page navigations to this: /api/now/ui/polaris/menu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB2105014

</td><td>

Survey Center updates for a new release

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Versatile Node and Cluster Configuration

 PRB2021392

</td><td>

Sys\_cluster\_state entries created post instance zboot are missing the role column value

</td><td>

After zboot, all app nodes are restarted and the nodes register themselves by invoking ClusterSynchronizer.startup\(\). This calls getClusterState\(\) to get the current sys\_cluster\_state record. When it can't find one, it calls getNewLocal\(\), and ClusterStateVncc Factory.getNewLocal\(\) always passes role = null.

</td><td>

1.  Run zboot on an AHA 3.0 disabled instance.
2.  Check the sys\_cluster\_state.role value.

 Expected behavior: The sys\_cluster\_state.role value matches with the com.snc.cluster .vncc.initial\_role file-based property value.

 Actual behavior: The sys\_cluster\_state.role value is empty.

</td></tr><tr><td>

Virtual Agent

 PRB2057885

</td><td>

Feedback icons don't show in AI Agent chat messages

</td><td>

When the user hovers over the message bubble, the **Thumbs Up** and **Thumbs Down** buttons aren't present.

</td><td>

1.  Configure an AI Agent which uses show\_output\_to\_user tool as the first tool.
2.  Run the agent in playground or NAP.
3.  Hover over the message bubble.

 Observe that the **Thumbs Up** and **Thumbs Down** buttons aren't present.

</td></tr><tr><td>

Virtual Agent

 PRB2073250

</td><td>

A conversation from another domain doesn't work if the user default domain doesn't have access to the current session domain

</td><td>

Whenever there is a hybrid queue into play, the worker impersonates the user and updates the session, but doesn't touch the domain. When impersonated normally, the domain is the default domain for the user. This might not have access to the conversation because it started in a different domain. So whenever some data is read that is not accessible, like conversation, the flow fails.

</td><td>

1.  Enable domain separation.
2.  Update any field on a user record.

Observe that after it's updated, the default domain to the user moves to TOP/Default unless specified.

3.  Switch the domain to a different domain \(some sibling domain or a parent domain\).
4.  Start the conversation.

 Observe the responses aren't received for any query.

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

 PRB2091209

</td><td>

The nextwave feature flag is not invalidated on insert/update

</td><td>

The value should be invalidated, but instead the old value still shows.

</td><td>

1.  Start an offglide conversation.
2.  Check any key using a script.
3.  If a value exists, update the value.
4.  Run the script again.

 Expected behavior: The value is invalidated.

 Actual behavior: The old value still shows.

</td></tr><tr><td>

Virtual Agent

 PRB2091219

</td><td>

There's a usage log creation issue when running a tool

</td><td>

On a domain-separated instance, tool executions for AI agents running off-glide \(for example, a Zero Touch Service Desk worker triggered by an incident\) run in the run-as user's home domain instead of the conversation's domain. On-glide, the same tool executions run in the correct domain. As a result, tool execution records \(sn\_aia\_tools\_execution\) are created in the user's domain \(often global\), so they don't show up on the execution plan, which is in the correct domain. Skill usage logging fails with '\[OG\] Error while logging the usage of skill ...'. This also happens when the user's home domain can't see the conversation's domain \(for example, a sibling or child domain\).

</td><td>

1.  Enable domain separation.
2.  Log in as some user.
3.  Switch the domain to a different one.
4.  Start an offglide conversation.
5.  Select a topic.

 Observe that there's a usage log failure.

</td></tr><tr><td>

Virtual Agent

 PRB2095603

</td><td>

getChannelById method mapping is missing in glide-plugin-members.xml

</td><td>

getChannelById calls from NW channels are failing.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB2100516

</td><td>

After uploading, a text file can't be viewed

</td><td>

A 403 error is returned.

</td><td>

1.  Navigate to an instance as a guest user.
2.  Upload a plain text file.
3.  Select the text file.

 Expected behavior: The text file opens.

 Actual behavior: A blank view is opened.

</td></tr><tr><td>

Virtual Agent

 PRB2104912

</td><td>

The **Cancel** button is replaced with the **End Chat** button before the agent accepts the work item

</td><td>

 

</td><td>

1.  Start a chat from /sp.
2.  Try connecting to a live agent by having Fred Luddy online on a different browser.

 Observe that the **Cancel** button disappears and is replaced with the **End Chat** button before the work item is accepted.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2033799

</td><td>

Ci-chat-components doesn't post a message to the parent window on session-call failure, breaking the documented single sign-on \(SSO\) redirect

</td><td>

Users can embed the Portable VA web-client iframe in the external OpenText interface with SSO. The documented integration has the parent page listen for a message event and redirect to SSO when it receives type SESSION\_CREATED with authenticated false. However, when the session call fails \(401\), the client doesn't post that message \(or any message\) to the parent, so the redirect never fires and the embed loops.

</td><td>

1.  Embed the Portable VA web client iframe in an external page \(OpenText\), using the documented SSO integration that listens for a postMessage and redirects to SSO on type SESSION\_CREATED with authenticated false.
2.  Load it in a context where the session / Consumer Account call returns 401 \(no established session\).

 Observe that the client shows the middle-panel error inside the iframe but posts nothing to the parent window. SESSION\_CREATED \(authenticated false\) never fires, the parent's SSO redirect never runs, and the embed loops.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Australia Patch 7m W44](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228441)
-   [Australia Patch 7 Hotfix 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-7-hf-2-PO.md)
-   [Australia Patch 7 Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-7-hf-1-PO.md)
-   [Australia Patch 7 W44](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228440)
-   [Australia Patch 7 W42](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3225387)
-   [Australia Patch 7](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-7.md)
-   [Australia Patch 6m W44](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228439)
-   [Australia Patch 6m W42](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3225386)
-   [Australia Patch 6 W44](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228438)
-   [Australia Patch 6 W42](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3225385)
-   [Australia Patch 6 W40 Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-6-W40-hf-1-PO.md)
-   [Australia Patch 6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-6.md)
-   [Australia Patch 5m W44](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228437)
-   [Australia Patch 5m W42](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3225384)
-   [Australia Patch 5b Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228732)
-   [Australia Patch 5b W44](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228436)
-   [Australia Patch 5b](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3226079)
-   [Australia Patch 5a W44](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228435)
-   [Australia Patch 5a W42](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3225383)
-   [Australia Patch 5a](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3156989)
-   [Australia Patch 5 W43](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3227387)
-   [Australia Patch 5 W42](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3225380)
-   [Australia Patch 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-5.md)
-   [Australia Patch 4](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-4.md)
-   [Australia Patch 3](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-3.md)
-   [Australia Patch 2](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-2.md)
-   [Australia Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/australia-patch-1.md)
-   [Australia security and notable fixes](https://www.servicenow.com/docs/r/release-notes/australia-security-notables.html)
-   [All other Australia fixes](https://www.servicenow.com/docs/r/release-notes/australia-all-other-fixes.html)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/available-versions.md)


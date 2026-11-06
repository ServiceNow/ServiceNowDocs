---
title: Brazil Patch 2
description: The Brazil Patch 2 release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/release-notes/brazil-patch-2.html
release: australia
topic_type: reference
last_updated: "2026-11-05"
reading_time_minutes: 67
breadcrumb: [Available patches and hotfixes, Learn about the Brazil release, Brazil release notes]
---

# Brazil Patch 2

The Brazil Patch 2 release contains important problem fixes.

-   **Brazil Patch 2 was released on November 05, 2026.**
    -   Build date: 11-03-2026\_2245
    -   Build tag: glide-brazil-08-25-2026\_\_patch2-10-22-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This version is being evaluated for use in the ServiceNow Government Community Cloud \(GCC\) environment.

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/brazil/rn/patches/PRBs-B02.00.xlsx).

Brazil Patch 2 includes 348 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

\[Omitted image "prb-chart-bp2.png"\] Alt text: Fixed issues grouped by problem categories bar chart

## Security-related fixes

Brazil Patch 2 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Brazil Patch 2, refer to [KB3228372](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB3228372).

## Changes in Brazil Patch 2

-   ****

    Used to enhance cross-scope access controls for the**getRefRecord\(\)** JavaScript API method to ensure authorization rules are followed consistently when retrieving information from other another application scope via the JavaScript method **getRefRecord\(\)**

    glide.sys.fencing.restricted\_caller\_access.invalidation\_mode: Controls how the system invalidates Restricted Caller Access records when a source code record, such as a script include, in a cross-scope access table is committed in an update set. For more information about RCA privileges, see 

-   ****

    Some indexed source fields change so frequently that repeatedly reindexing them adds load to AI Search without adding search value. AI Search automatically identifies these high-churn fields and lets an admin decide whether to continue indexing them or to exclude them from the index going forward.

-   ****

    Field descriptions for the AI Search Datasource Churn Audit table, which lists fields that AI Search has flagged as high-churn.

-   ****

    Review fields that AI Search flagged as high-churn and decide whether to keep indexing them or exclude them from the index.


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

MID Server

 PRB2012665

 [KB2953193](https://hi.service-now.com/kb_view.do?sysparm_article=KB2953193)

</td><td>

MID Server upgrades fail because the MID.max.extract .file.size property default is too low

</td><td>

The MID Server property MID.max.extract .file.size property default of 500MB is too low for MID Server upgrades. Upgrades fail at the download/extract stage with the following errors, after the MID-core zip file has been successfully downloaded: '...Exceeds the maximum size \(500000000\). Unable to download package The size of uncompressed files is too big or too many entries in the zip file'. This fails before the MID Server is shut down, avoiding outages, but causes repeated failed upgrades, and the risks of running with an instance vs MID Server incompatibility, that generally has been known to break some features and cause data loss.

</td><td>

Refer to the listed KB article for details.

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

Service Catalog

 PRB2089751

 [KB3159281](https://hi.service-now.com/kb_view.do?sysparm_article=KB3159281)

</td><td>

Catalog client scripts and UI policies are blocked on requested item \(RITM\)/sc\_task forms for users who can read the record

</td><td>

The resolver throws 'User doesn't have access to the item' and returns no catalog client scripts / UI policies, so none execute on the RITM/sc\_task form, even though the user can fully read the record. Users expect catalog client scripts and UI policies load and execute for any user who has read access to the RITM / sc\_task record. The catalog item User-Criteria entitlement \(canView\) should only gate the catalog ordering context \(sc\_cat\_item / sc\_cart\_item\), not fulfillment records.

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

 PRB2080954

</td><td>

The statement 'on behalf of AI' incorrectly displays 'AI' and not the user

</td><td>

This was introduced when Audit &amp; Logging changed the attribution model for AI-generated changes. The AuditGroup **Who** field was changed to reflect the identity of the AI agent making a change when generating history sets.

</td><td>

 

</td></tr><tr><td>

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

AI Experience Framework - Glide

 PRB2121332

</td><td>

Update the Karuna-glide managed app version in base instance apps

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2087032

</td><td>

Incorporate new fields in AIS logging following the changes in AIS backend with new feature explain methods

</td><td>

After an Australia patch upgrade, search doesn't work from the Service Portal page.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2095865

</td><td>

AIS deleteSingleRecord's unconditional attachment deleteByQuery blocks the event processor, causing queue backlog and auto-shutoff

</td><td>

AIS indexing was auto-paused because the update event queue backlog grew past 1M due to Ingest​Service.​delete​Single​Record stalling the AIS event processor. During this pause window, updated cases and records were not searchable until the backlog drained and indexing resumed.

</td><td>

1.  Open an instance with AIS/glide-ais.
2.  Configure a datasource/table pair where AIS responds slowly to deleteByQuery \(for example, a very large index or 100M+ docs\) or is intermittently unavailable.

Observe that it triggers the exponential-backoff retry path.

3.  Trigger a sustained burst of record deletes on that table via a retention/cleanup policy's bulk delete, or a scripted bulk delete through the normal GlideRecord delete path, so business rules/listeners fire normally.

 Observe that each deleted record produces one AIS delete event. The AIS event processor calls Ingest​Service.​delete​Single​Record once per event, which unconditionally calls delete​Attachment​Documents​By​Query to Internal​Content​Ingestion​Api.​delete​By​Query.​ This runs synchronously and blocks the event-processing thread on the AIS network call \(and on retry backoff sleeps\) - even when the deleted records have no attachments at all. If AIS is slow/unavailable long enough, the queueShouldNotBeWritable\(\) safeguard disables the update event queue \(glide.​ais.​update\_​event\_​queue\_​writable=​false\)​.​ Any record changes during the paused window aren't reflected in Global Search until the queue is manually re-enabled and the backlog drains.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB2096049

 [KB3226033](https://hi.service-now.com/kb_view.do?sysparm_article=KB3226033)

</td><td>

An upgrade caused the instance to log a missing column error during the upgrade due to a missing **Active** column in the ts\_configuration table

</td><td>

It seems this column is being added by the upgrade itself but it's not clear why the nodes expect it before it's being added. An instance can become unavailable in the upgrade process. An emergency schema correction was implemented by adding the missing **Active** column to the ts\_configuration table. Once the schema was corrected, the upgrade process resumed and completed successfully.

</td><td>

Refer to the listed KB article for details.

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

 PRB2083562

</td><td>

Support right-click behavior for Service Portal search results

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB2085507

</td><td>

The FilterParser class and getFieldsFromFilter method aren't exposed

</td><td>

FilterParser class and getFieldsFromFilter should be callable from GlideScript scope. FilterParser \(repo: glide/glide\) should be exposed as a glide Scriptable. Report conditions aren't taken into account on the scan when scanning if a report passes RVACLs.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB2084237

</td><td>

Support install engine to read the SNAPSHOT version from package.json for the app store path

</td><td>

The installation fails with the following error because the install engine is not able to resolve SNAPSHOT version from store: '\*\*\* ERROR \*\*\* Unable to find the dependency plugin sn\_ai\_csm\_fdn:2.1.3-SNAPSHOT for sn\_ai\_csm\_advanced \*\*\* WARNING \*\*\* Unable to resolve dependency sn\_ai\_csm\_fdn:2.1.3-SNAPSHOT for sn\_ai\_csm\_advanced as dependency is unavailable'.

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

Application Install Engine

 PRB2101357

</td><td>

The PPL Batch installation doesn't report upgrade failures properly and doesn't upgrade dependencies properly

</td><td>

The batch installation reports a success even though the dependency wasn't upgraded.

</td><td>

1.  Open an Australia instance.
2.  Install a sys\_suite\_config.
3.  Upgrade an app in the suite to a higher version with dependencies also on a higher version than current.

 Observe that the dependency is not an upgrade and the user sees the following log: 'PluginFilter registrar says plugin sn\_itsm\_va is already at that version, assigned version : 9.3.2.'.

</td></tr><tr><td>

Application Rationalization

 PRB2082114

</td><td>

Artifact​Related​Entity​Table​Choices Script Include needs client\_callable=true for tableChoicesScript to work in Enterprise Architecture \(EA\) Workspace

</td><td>

The 'Entity' drop-down list shows all tables instead of the filtered list.

</td><td>

1.  Open the EA Workspace.
2.  Navigate to **Portfolio** &gt; **Architectural Artifacts**.
3.  Open any existing artifact or create a new URL type artifact.
4.  Open the 'Related Entities' related list.
5.  Select **New**.
6.  Select the **Entity** drop-down list.

Observe that all tables are shown \(25+ tables\) instead of the filtered list.


 Expected behavior: Only 6 tables should be shown \(Business Application, Business Capability, Business Process, Digital Integration, Digital Interface, TRM Product\)

 Actual behavior: All tables are shown.

</td></tr><tr><td>

Attachments

 PRB2103278

</td><td>

Fix the uploader visibility and expose the avatar, upload timestamp, and access fields via GraphQL

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

Automated Test Framework \(ATF\)

 PRB2080594

</td><td>

Add gating for enable/disable code coverage in server side steps

</td><td>

ATFCodeCoverageProcessingJob is inserted after disabling code coverage.

</td><td>

1.  Disable code coverage.
2.  Run an ATF test.

 Expected behavior: The ATFCodeCoverageProcessingJob should not be in the sys\_trigger.

 Actual behavior: The ATFCodeCoverageProcessingJob is inserted.

</td></tr><tr><td>

Cache

 PRB2076313

</td><td>

Query caching metric adjustment

</td><td>

 

</td><td>

Open 'xmlstats.​do?​include=​query\_​cache&amp;​query\_​pool\_​details=​true'.​

 Observe that it is not segregating the data as per platform and custom metadata.

</td></tr><tr><td>

Cache

 PRB2108823

</td><td>

Disable by default and make it as an opt-in feature in Ambient Query Caching

</td><td>

 

</td><td>

1.  Update the glide.query\_cache.enabled to be false by default.
2.  Check the instance to ensure that the QC is disabled by default.
3.  Enable the property.

 Observe if the QC is enabled after the change.

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

Case and Knowledge Management for HR Service Delivery

 PRB2089112

</td><td>

RCA is not visible after the plugin installation

</td><td>

The expected RCA record is not created or loaded on the instance after the plugin installation.

</td><td>

1.  Install the sn\_hr\_core and sn\_hr\_ia plugins on an instance.
2.  Allow the plugin installation and any associated post-installation jobs to complete successfully.
3.  Verify the scope-to-scope RCA configured to migrate records from the sn\_hr\_ia source scope to the sn\_hr\_core target scope.

 Expected behavior: The scope-to-scope RCA should be automatically loaded during plugin installation, and the corresponding RCA record should be present on the instance after the installation is complete.

 Actual behavior: The scope-to-scope RCA migration is not executed as expected, and the required RCA record is missing from the instance after the installation of the sn\_hr\_core and sn\_hr\_ia plugins.

</td></tr><tr><td>

Change Management

 PRB2079977

</td><td>

Dynamic CI Groups fail to populate Affected CI records due to an issue in the Australia Dynamic CI Group unpack processing path

</td><td>

Dynamic CI Groups are not being unpacked into the expected Affected CI records during Change Request processing. The unpack process completes, however, the resulting Affected CI records are not created as expected due to an issue in the Australia processing path. Affected CI records are not generated from Dynamic CI Groups, preventing downstream Change Management functionality that relies on Affected CI population from functioning as expected. This impacts processes that depend on Dynamic CI Group members being automatically added during Change Request processing.

</td><td>

1.  Create or open a Change Request.
2.  Add a Dynamic CI Group as the Configuration Item or Affected CI.
3.  Save or submit the Change Request.
4.  Allow the Dynamic CI Group unpack process to execute.

Observe that the Dynamic CI Group processing completes successfully.

5.  Review the Affected CI related list.

 Expected behavior: All applicable CI members associated with the Dynamic CI Group are unpacked and populated into the Affected CI related list.

 Actual behavior: Affected CI records associated with the Dynamic CI Group are not populated.

</td></tr><tr><td>

Change Management

 PRB2093236

</td><td>

DF Advisor auto-activation causes regressive behavior for Inc, Chg, Prb and Req

</td><td>

The 'com.​snc.​task.​principal\_​class\_​filter' property should be empty or it should contain the same value as it did prior to upgrading.

</td><td>

1.  Open an instance.
2.  Navigate to sys\_properties.do?sys\_id= 1f2f01ce878010100e3dd61e36cb0b63 \(com.snc.task. principal\_class\_filter\).

 Observe the property. On a zbooted instance, or an upgraded instance with 0 principal CI classes set up prior to upgrading, the property must be empty. On an upgraded instance with at least one principal CI class set up prior to upgrading, the property should contain the same value as it did prior to upgrading. The expectation is that this is the IPCR tables.

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

CMDB Identification and Reconciliation

 PRB2086544

</td><td>

Reading an encrypted field results in an error when IRE is invoked through scoped API from application scope

</td><td>

 

</td><td>

1.  **Use** field encryption and encrypt an identifier.
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

Edge proxy schedule upgrades fail on Brazil

</td><td>

Edge proxy doesn't upgrade and the upgrade status is stuck in 'Running'. The upgrade schedule record shows status running/failed. The failure reason is 'Failed on signature verification for distribution file'.

</td><td>

1.  Request a TD instance on AP5 JDK 17 or AP6 JDK 21 with Edge proxy configuration.
2.  Log in as a user with elevated privileges.
3.  Authenticate Edge proxy on the node instance.
4.  Request an upgrade on the TD instance using **Run Upgrade on Existing Instance from Artifacts**.
5.  Select **AP5 or AP6 Instance requested**.
6.  Log in to the Edge instance as a user with elevated privileges.
7.  Navigate to **Edge Encryption Configuration** &gt; **Proxies** &gt; **All**.
8.  Open 'Encryption Proxy Record'.
9.  Select the**Schedule Proxy** button.
10. Schedule the proxy by providing a date and time.
11. Submit.

 Expected behavior: Schedule proxy upgrades to the latest version.

 Actual behavior: Edge proxy doesn't upgrade and the upgrade status is stuck in 'Running'.

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

After the Service Management Core plugin is installed, users without the contract\_manager role \(such as those with the snc\_internal or sam\_user roles\) can't see several fields on the ast\_contract table, including 'Description', 'Number', **Short Description**, 'Vendor', and additional fields. The new field‑level read ACLs created by the plugin require the contract\_manager role, which overrides the existing table‑level ACLs and removes read permission for those users. Affected users can't view contract information that was previously accessible. Similarly, on an instance with the SAMS plugin, contract managers can't read the contract fields due to field-level ACLs introduced by the SAMS plugin.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Contract Management

 PRB2053611

</td><td>

In i18n: Contract Management, 'Yes/No' are hardcoded

</td><td>

After changing the language to a non-English language and selecting **Cancel Contract**, 'Yes/No' appear hardcoded.

</td><td>

1.  Open ast\_contract.list.
2.  Choose an Active record.
3.  Change the language to any non-English language.
4.  Select **Cancel Contract**.

 Observe that 'Yes/No' are hardcoded.

</td></tr><tr><td>

Contracts Core

 PRB2101746

</td><td>

The Contract documents and **Amendment** field changes related lists are broken

</td><td>

 

</td><td>

1.  Impersonate as a contract fulfiller user.
2.  Create a CMR.
3.  Navigate to the Contract Documents related list.
4.  Observe that it says 'Can't display the list'.
5.  Sign the contract.
6.  Create the AST contract.
7.  Open the contract.
8.  Navigate to **Amendment field changes**.

 Notice that this list is broken.

</td></tr><tr><td>

Core Business Suite for Workplace Services

 PRB2096283

</td><td>

WSD Visitor Management inadvertent true-up version bump

</td><td>

The WSD version is CBS dependency version v2.1.1 when it should be the same as WSD v1.19.0.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1999432

</td><td>

The message 'Swarm64CapabilityCheck capability is not supported on Glide' shouldn't be logged and should be removed/stopped

</td><td>

It shouldn't be logged as an error. It should be logged as info, which is normal and valid. It's not an error. It's a note recorded during startup and completely expected when connecting to a non-RaptorDB database. However, if this is Oracle DB, the message is unnecessary. This message should not be logged at all.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB2089608

</td><td>

DB connection exhaustion is observed

</td><td>

This happens due to JVM Lock contention between the DatafabricEngineSweeper job and Workload​Identification.​get​Workload​From​Scope.​

</td><td>

1.  Upgrade all app nodes \(over 20 of them\) to Brazil.
2.  Trigger the upgrade job to start DB schema changes.

 Observe that the nodes become unresponsive.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB2126688

</td><td>

Passing MetaAttributes is causing Concurrent​Modification​Exception in Postgres JDBCdriver. Disable the feature on the Glide side

</td><td>

The error is happening all over Brazil installations.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Graph

 PRB2064975

</td><td>

The sub graph time increased ~200ms

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB2076449

 [KB3152921](https://hi.service-now.com/kb_view.do?sysparm_article=KB3152921)

</td><td>

A node can't start if there's a **Formula** field on sys\_user

</td><td>

The instance node will fail to restart if there is a formula‑calculated field on the User \[sys\_user\] table. When the issue occurs, the node does not restart and logs a stack overflow error. The failure occurs during the platform's schema loading phase, preventing the instance from coming online and impacting all users.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Decision Table \(Family\)

 PRB2037235

</td><td>

High response timings for the 'Save Price Adjustment' transaction

</td><td>

 

</td><td>

1.  Log in to the application.
2.  Create an Opportunity.
3.  Add line items.
4.  Initiate a manual Price Adjustment.
5.  **Save** it.

 Observe the response timing.

</td></tr><tr><td>

Developer Sandboxes

 PRB2065864

</td><td>

The DSB Pool Balancer is over queuing during the upgrade

</td><td>

 

</td><td>

Upgrade the instance.

 Observe that after the upgrade, sys dsb pool records are in the 'Queued' state.

</td></tr><tr><td>

Developer Sandboxes

 PRB2098871

 [KB3227181](https://hi.service-now.com/kb_view.do?sysparm_article=KB3227181)

</td><td>

Enabling the sandbox plugin with default controller=2 on the plugin installation will potentially handicap instances with less than 2 nodes

</td><td>

In this issue only two nodes are in rotation for the base instance URL instead of five.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

DirectSQL

 PRB2077040

</td><td>

SQL API JDBC queries are returning the sys\_id as 'null' for some records

</td><td>

A majority of the sys\_ids will be 'null' even though all records should return the sys\_id value.

</td><td>

1.  Provide the test user read access to the target table through a table-level ACL. For example, sys\_choice \(create new ACL for table read\).
2.  Query the table using the V2 JDBC endpoint, or even v1.
3.  Inspect the returned records and the **sys\_id** field.

 Expected behavior: All records should return the corresponding sys\_id value.

 Actual behavior: One a few records will have the sys\_id, and the majority of the sys\_id will be set to 'null'.

</td></tr><tr><td>

DirectSQL

 PRB2098984

</td><td>

The query rewrite adds the PK column to SELECT but not to GROUP BY, so GROUP BY queries fail in Trino

</td><td>

After adding primary keys to the tables and disabling privileged mode, Pyramid Analytics queries that use GROUP BY to select distinct values fail.

</td><td>

1.  Use a table with a primary key defined \(sid, primary='true'\) and privileged mode disabled.
2.  Run the query through DirectSQL from Pyramid Analytics: SELECT issue\_type FROM servicenow.sn\_dna\_cdi\_soo\_df\_dl\_gold\_da\_case\_issue\_type\_d GROUP BY issue\_type.

 Observe that the query fails with: 'xsndnacdisoodfdlgolda15u100.'sid' must be an aggregate expression or appear in GROUP BY clause Expected: the query returns the distinct issue\_type values.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB2073063

</td><td>

Unbounded 300 DPI page render in MLService​Util.​extract​Data​From​PDF exhausts node heap

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

If any user inherits or contains the sn\_docintel.viewer and platform\_ml\_di.viewer roles, it would inherit the snc\_read\_only role. This would refuse the user to CREATE/WRITE ops on any table, which is likely restricting the user to complete READ/VIEW mode on the instance.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB2054721

</td><td>

Notification bell behavior changed after an upgrade from Yokohama to Australia

</td><td>

Previously, when a new notification appeared, it would disappear after a while and no other notifications would be shown. After the upgrade, when a second notification appears and disappears, the first unread notification is displayed again.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB2081390

</td><td>

Email Open Tracking stopped working

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Employee Relations Case Management

 PRB2093397

</td><td>

The HRBP ER Case Assignment Schedule job does not run

</td><td>

After creating an ER case for a user, the ER case does not get assigned the HRBP ER Schedule job isn't triggered.

</td><td>

1.  Install HRBP and ER.
2.  Enable auto-assignment for an ER service.
3.  Set up scope rules.
4.  Create an ER case from that service for a user that fits the scope.

 Notice that the ER case is never assigned, and the HRBP ER Schedule job trigger doesn't exist.

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB2107508

</td><td>

Add multi-Instance JWT minting API in the Content Taxonomy

</td><td>

This is a product update.

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

Field Encryption Starter

 PRB2078372

</td><td>

A cross scope error occurs when selecting the **+** sign on Service Operations Workspace \(SOW\) to create a new incident

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB2081205

 [KB3228806](https://hi.service-now.com/kb_view.do?sysparm_article=KB3228806)

</td><td>

Restarting non-global flows fails with 'Flow object for 'scope\_sys\_id.flow\_name does not exist'

</td><td>

A flow built directly in the Global scope restarts as expected, it is specifically flows in a real \(non-Global\) scoped app that fail.

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
3.  Create a parent flow with a ForEach loop \(iterate over any list of 10+ items\).
4.  Inside the loop, call the subflow.
5.  Wait for the completion to '= true'.
6.  Publish it.
7.  Run the parent flow with SQL tracing enabled.

 Expected behavior: Sys\_flow\_subflow\_plan queried once and subsequent iterations use cache.

 Actual behavior: Sys\_flow\_subflow\_plan queried once per iteration with number of identical queries for the amount of iterations.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB2095468

</td><td>

Fixing the double quote escaping logic in the Call Now Assist Skill step

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GlideAggregate API

 PRB2090884

</td><td>

For non-admin callers, a regression results in the **Aggregate/Stats API** field validation conflating 'field doesn't exist' with 'field exists but read-ACL denies it'

</td><td>

When a non-admin caller queries the Aggregate/Stats API \(/api/now/stats/\{table\}\) using sysparm\_min\_fields, sysparm\_max\_fields, sysparm\_avg\_fields, or sysparm\_sum\_fields, the API incorrectly rejects fields the caller is not allowed to read as if those fields did not exist. Any non-admin identity that has a field-level ACL restriction on one of the fields it requests receives a hard failure instead of the expected ACL behavior.

</td><td>

1.  Pick any table \('T'\) with a field \('F'\) that has a field-level read ACL restricting a non-admin role.
2.  As the non-admin identity, get /​api/​now/​table/​T?​sysparm\_​fields=​F,​sys\_​id&amp;​sysparm\_​limit=​1 and confirm F is absent or blanked in the response.
3.  As the same non-admin identity, call: GET /​api/​now/​stats/​T?​sysparm\_​max\_​fields=​F.​

 Expected behavior: Either a normal aggregate result with F omitted/blank, or a proper ACL-style denial.

 Actual behavior: HTTP 400, 'Invalid sysparm\_max\_fields parameter' occurs, reported identically to what a user would see for a field name that doesn't exist on T at all.

</td></tr><tr><td>

HR Integrations

 PRB2081919

</td><td>

hr-​scoped-​sp-​ux-​test.​RCAPrivileges​IT is failing due to an RCA issue in the IntegrationPushTodoHelperSNC script include

</td><td>

This issue was observed in Brazil.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2074969

</td><td>

HR Core ships record-read ACLs on 'sysapproval\_approver' but no field ACLs, blanking every field for approvers

</td><td>

The HR Core record ACL evaluates and passes, but the 'Global' field wildcard 'sysapproval\_approver.\*' is not evaluated. The result is false because the granting scope \(HR Core\) has no field ACL for the engine to evaluate.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB2086829

</td><td>

AI Search RAGRetrievalAPI can't access the HR Case description field for non-admin users during retrieval, even when those users can read the field directly

</td><td>

AI Search's RAGRetrievalAPI can't access the HR Case description field for any user who lacks the admin role. The affected users have legitimate read access to the underlying \[sn\_hr\_core\_case\] records and can read the description field directly, yet RAGRetrievalAPI behaves as though the field is inaccessible for these users — and returns the wrong cases as a result. It appears the description is fully excluded from the retrieval. Because the wrong cases are returned, the description content is not considered during the semantic search that selects candidate records. This points to a field-level access-evaluation gap in the retrieval path: for non-admin callers, RAGRetrievalAPI fails to resolve the caller's actual read permission on the description field and treats it as inaccessible, so the field is neither searched over nor returned. Admin callers, whose access resolves correctly, receive correct results — which is why the behavior is gated on the admin role rather than on real read permissions.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB2082113

</td><td>

When the producer replication set is deactivated, the consumer replication **Active** flag is not set to false

</td><td>

 

</td><td>

1.  Have active producer and consumer replication set.
2.  Deactivate the producer.

Observe the consumer XML.


 Expected behavior:**Active** should be 'false'.

 Actual behavior:**Active** is 'true'.

</td></tr><tr><td>

Integration Hub

 PRB2086800

</td><td>

True-up for Workflow Data Fabric credits

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

ISA Equipment Model

 PRB2108745

</td><td>

Brazil compatibility fix for OT main bundle

</td><td>

 

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

 PRB2083677

</td><td>

Embedded videos added through 'Insert/Edit Media' are removed from Knowledge Base \(KB\) articles and do not render in Service Operations Workspace \(SOW\)

</td><td>

Embedded videos do not appear in KB articles Service Operations Workspace even after pasting the embed code from the video in the Insert/Edit Media modal in the editor.

</td><td>

1.  Open Service Operations Workspace.
2.  Open the list menu.
3.  Navigate to **Knowledge** &gt; **All published articles** &gt; **New**.

Observe that the new kb\_knowledge Edit form opens in SOW.

4.  Fill in all the mandatory fields.
5.  In the article body, use the editor.
6.  Select **Insert/Edit Media**.

Observe that the Insert/Edit Media modal opens.

7.  Select the **Embed** tab.
8.  Paste the embed code from the video.
9.  Select **Save**.
10. Save the knowledge record.
11. View the article by selecting **View Article**.

 Notice that the embedded view does not show in SOW.

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

 PRB2090439

</td><td>

Due to Generative AI Controller \(GAIC\) layer issue, multi-KB generation is broken and Mosaic migration should be rolled back

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB2100264

</td><td>

sn\_genai\_platform true-up install failure due to sn\_generative\_ai dependency version mismatch in base instance apps

</td><td>

When attempting to install the trued-up version of the sn\_genai\_platform app, the installation fails. Going into the Application Manager's activity log shows: sn\_generative\_ai needs to be procured from store 15.1.1. The version trued up \[sn\_generative\_ai\] in oob-apps differs from the app versions \[sn\_generative\_ai\] on other instances. The dependency links don't match between oob-apps and the trued-up app records. The dependency-version true-up was missed and only the app record itself got trued-up to a version that doesn't match its declared dependency.

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

Lifecycle Events

 PRB2091568

</td><td>

Include RCAs for the AIUX journey

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2083488

</td><td>

The RITM 'Previous/Next' record navigation fails and the record count becomes incorrect

</td><td>

The 'Previous Record/Next Record' arrows in the ITIL form do not successfully navigate to another record.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB2104857

</td><td>

**Global Delete** UI actions aren't uptaking the latest changes

</td><td>

'\[Glide\] Support base instance delete action' was fixed as part of the UI16 parity effort for UI26. These changes migrate the delete-confirm UI page into a core-ui widget, which required changes to the UI action files on Glide. After the Glide changes made it in, remote instances were not picking up the fix \(regardless of mod count increases\) and therefore causing the new delete widget to fail. Upon investigation, the UI actions that got updated on Glide had duplicate files with the same sys\_id and global scope on app-cmdb. The duplicate files from CMDB get installed after Glide as plugins, so mod counts were ignored and Glide changes overridden. For these changes to get picked up, two requirements must be met on the new fix: 1. CMDB deletes the duplicate files that are overriding the changes on Glide and 2. The files need to get a mod count increase so the instances are able to install the new version.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB2099254

 [KB3228411](https://hi.service-now.com/kb_view.do?sysparm_article=KB3228411)

</td><td>

MID Servers are marked as 'Down' on instances with Language Packs enabled on Brazil

</td><td>

After an instance is upgraded to the Brazil release, MID Server\(s\) may be incorrectly marked as 'Down' even when they are available. This issue affects Brazil instances where a non-English Language Pack is enabled and the instance's default language is set to a non-English language in the glide.sys.language system property. It may cause the MID Server dependent functions, including integrations, imports, Discovery, and event/metric ingestion, to fail because no MID Server is considered available.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Platform

 PRB2090163

</td><td>

Unable to reach MobileAIUXUtils from scoped context

</td><td>

When calling SNC.​Mobile​AIUXUtils.​set​Experience​Switch​Enabled from a scoped context, it is not accessible.

</td><td>

Call SNC.​Mobile​AIUXUtils.​set​Experience​Switch​Enabled from a scoped context.

 Expected behavior: The sys\_properties record is created and set to true or false based on the values passed in.

 Actual behavior: The function isn't available and no property is created.

</td></tr><tr><td>

Mobile Platform

 PRB2093548

</td><td>

The Voice Launcher is not included in the Mobile user client

</td><td>

The configured **Prominent action** button may not appear.

</td><td>

1.  Configure a **Prominent action** button to use the voice launcher feature.
2.  Open the Mobile client.
3.  Look for the **Prominent action** button.

 Expected behavior: The**Prominent action** button should be available and start a voice session.

 Actual behavior: The voice configuration in the user client is not returned, and the**Prominent action** button may not appear. If it does appear, it won't work.

</td></tr><tr><td>

Mobile Platform

 PRB2098428

</td><td>

Disabling 'Check ACL on Parameter Field' in the URL silently drops the URL button parameter in the V2 path

</td><td>

The field value does not get substituted in the URL.

</td><td>

1.  Create a **Mobile URL** button \(context = Record\) whose URL template references that field on a table.
2.  Explicitly add the button attribute 'check\_​acl\_​on\_​url\_​parameter\_​field = false'.
3.  Request the record's mobile document via the V2/separated-metadata endpoint.
4.  Look at the button's rendered URL/parameters.

 Expected behavior: The field value is substituted into the URL.

 Actual behavior: The field value is not substituted into the URL.

</td></tr><tr><td>

Mobile Platform

 PRB2098626

</td><td>

Intercepting a form screen using the universal link does not work properly

</td><td>

 

</td><td>

1.  Send or simulate a universal link request sent to a mobile device for a specific mobile form screen with a specific sys\_id.
2.  Ensure the user has access to the table and the record.

 Notice the incorrect record for the table, which the user has access to, is opened, no matter the sys\_id.

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

5.  Set glide.​platform\_​mm\_​service.​verbosity to high.
6.  Re-index the same document.
7.  Inspect sys\_mm\_result.

 Observe that config.verbosity is 'high'.

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2091483

</td><td>

The Multimodal Captioning skill not visible in Now Assist Admin

</td><td>

When attempting to deactivate skills, the platform displays the following error: 'Error occurred while deactivating skill. Please contact administrator.' Remaining skills not visible and identifiable in the Now Assist Skills section, even though the Now summary reports active skills.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB2092679

</td><td>

The KB MMS Job gets recreated without reading from stored results

</td><td>

Checking out a KB article sends its unchanged attachments to MMS again. Checking it out copies the attachments onto the new version as new sys\_attachment rows, and the MMS upload rule treats each copy as a new upload.

</td><td>

Move the KB to the states **Publish** &gt; **Checkout** &gt; **Publish**.

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

Next Experience Unified Navigation

 PRB2057599

</td><td>

Navigation from the **Action** button doesn't work

</td><td>

No navigation occurs or the expected page doesn't load.

</td><td>

1.  Open the application or web page containing the **Action** button.
2.  Select the action button intended to trigger navigation.

 Observe that no navigation occurs or the expected page doesn't load.

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

Due to an issue in which the protected resource metadata for the MCP includes the resource path in the authorization server URL, there's an issuer mismatch in which Glide is the authorization server. Further, Glide does not advertise any metadata at the base metadata path /​well-​known/​oauth-​authorization-​server/​​.​

</td><td>

 

</td></tr><tr><td>

OAuth

 PRB2095958

</td><td>

Whenever someone experiences node switch and the first request their browser makes is $uxapp.do, they can't use EmployeeWorks until they log out

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB2121845

</td><td>

When an agent calls a skill, then calls another skill, the sub components don't get triggered

</td><td>

When the agent calls a skill, calls another skill, then calls a script, the script call \(or any other component\) doesn't happen. When triggering the parent skill from skill kit, it works.

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

Platform Analytics Dashboard

 PRB2072165

</td><td>

The 'Dashboard' tab in the workspace is not persisting the filters when switching to another tab

</td><td>

The filters are not applied after switching to another tab, even though they should persist and not be reset automatically when switching back to the tab.

</td><td>

1.  Open a dashboard.
2.  Switch to the tab 'Portfolio TCO'.
3.  Apply any filters.
4.  Choose a drill-down or refresh the page.

 Expected behavior: The applied filters should persist and should not be reset automatically when switching back to the original dashboard tab.

 Actual behavior: Filters are not applied anymore.

</td></tr><tr><td>

Platform Analytics Filters

 PRB2071614

</td><td>

The UI Builder filter throws an error if the user does not have the pa\_viewer role

</td><td>

The user can see the filter list populated with the indicator breakdown only with the pa\_viewer role.

</td><td>

1.  Create a UI Builder 'Experience' page with the filter component.
2.  Add an indicator for the datasource property.
3.  Create a user without assigning the pa-viewer role.
4.  Impersonate that user.
5.  Open the 'Experience' page in preview mode.

 Expected behavior: The user should see the filter list populated with indicator breakdown.

 Actual behavior: It is showing an error message, 'Error occurred while loading filter data'.

</td></tr><tr><td>

Platform Analytics Libraries

 PRB2084791

</td><td>

The Core UI creation flow should not be possible for fully migrated users or for users past Xanadu

</td><td>

Once an element is created, it cannot be found in the libraries because Core UI tables are not queried. The flow should not be possible in fully migrated instances past Xanadu.

</td><td>

1.  Set up a new TD on Australia or Brazil.
2.  Manually create the Core UI creation properties:
    -   com.​snc.​par.​coreui.​dashboard\_​create.​enabled = true
    -   com.​snc.​par.​coreui.​report\_​create.​enabled = true
3.  Create new dashboard.

 Notice the Core UI flow is present while 'v\_table' is false.

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

 PRB2066861

</td><td>

The time series widget with the widget indicator filtered by 'Choice' is migrated as a compatibility mode widget

</td><td>

 

</td><td>

1.  Create a time series PA widget on the indicator, 'Number of open incidents'.
2.  Configure a widget indicator for the widget indicator, 'Number of open incidents'.
3.  Set the breakdown priority on the element as '1 - Critical'.
4.  Add the PA widget to a core UI dashboard.
5.  Migrate the dashboard.

 Expected behavior: The widget is migrated as a data visualization since this configuration is supported. This only happens to the**Choice** field but doesn't happen to **Reference** field \(such as 'assignment group'\).

 Actual behavior: The widget is migrated as a compatibility mode widget.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB2081175

</td><td>

Setting glide.​par.​coreui.​migration.​new\_​coreui\_​artifacts\_​created to 'true' causes PAR dashboard deletion during re-migration

</td><td>

Dashboards that were migrated successfully are deleted when re-running the migration.

</td><td>

1.  Create a Core UI dashboard \(pa\_dashboards\).
2.  Open the Migration Center and run the content migration.
3.  After the migration is complete, activate all migrated content.
4.  Open System Properties.
5.  Set glide.​par.​coreui.​migration.​new\_​coreui\_​artifacts\_​created to 'true'.
6.  Return to the Migration Center.
7.  Re-run the content migration.

 Expected behavior: Re-running the migration should not delete dashboards that have already been successfully migrated.

 Actual behavior: The previously migrated Core UI dashboard is deleted during re-migration.

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

 Expected behavior: The title of first activity \(record generator\) is translated to English.

 Actual behavior: The title of first activity \(record generator\) isn't translated.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB2075258

</td><td>

Concurrent​Modification​Exception comes when two concurrent playbook executions are created

</td><td>

When two records are created together for playbook execution, it tries to race for the creation of activity contexts, resulting in one of the playbook execution records to error out.

</td><td>

1.  Create new playbook with a trigger on the record creation.
2.  Attempt to create two records simultaneously using JSON API or Scriptable API 3.

 Expected behavior: Both playbooks should run normally.

 Actual behavior: One of the playbook execution records will error out.

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

 PRB2096921

</td><td>

The Playbook fails to load 'Error fetching playbook' for playbooks with 'After specific stages' once a Playbook Experience record generator has previewed them, and a NullPointerExeception \(NPE\) occurs in isOnIdealPath

</td><td>

The NullPointerException shows 'Cannot invoke ''Activity.​is​Lane​Start​Activity\(\)​'' because 'activity' is null.' The PlaybookContextQuery catches it as 'Error fetching playbook', and the whole playbook response is empty, including the intake. This issue is found in Brazil instances, but works as expected in Australia because isOnIdealPath is not in that build.

</td><td>

Refer to the listed KB article for details.

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

 PRB2056538

</td><td>

The breakdown filter values display a grouped activity label after refreshing the page

</td><td>

When a project has a field configured as both the Activity Definition and a breakdown, and the 'Group values into a single activity step' option is enabled. The breakdown filter values in the scheduled task panel's applied-filters section initially render correctly. After a full page refresh, the labels are replaced by the grouped activity name, such as 'Category changed' for every selected value.

</td><td>

1.  Configure the project with a field as the 'Activity Definition'.
2.  Enable the 'Group values into a single activity' step.
3.  Configure the same field as a breakdown.
4.  Apply a breakdown filter on that field with at least two values.
5.  Inspect the scheduled task panel and the 'Applied filters' section.

Observe that the label is correct, For example, 'Category: Database, Network, Software'.

6.  Refresh the page fully.
7.  Inspect the same section again.

 Expected behavior: The applied filter section continues to show the correct breakdown value labels after refresh, such as 'Category: Database, Network, Software'.

 Actual behavior: Each selected value is replaced by the grouped activity label. For example, 'Category: Category changed, Category changed, Category changed'.

</td></tr><tr><td>

Process Mining Workspace

 PRB2068401

</td><td>

A RCA fails on a child entity for all MDM projects

</td><td>

 

</td><td>

1.  Create any pair of MDM projects for the incident and problem entities, or the incident and SLA task entities.
2.  Select any eligible activity in the child entity.
3.  Run 'Key contributors RCA' from the 'Investigate' section.

 Observe that the RCA scheduled task fails for the selection. Note for the same entity without MDM setup, the RCA task is working correctly.

</td></tr><tr><td>

Process Mining Workspace

 PRB2069087

</td><td>

Update the Usage Metric Definition Id and guardrail changes for Meter Based

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB2073844

</td><td>

Breakdown percentages in the 'Opportunity Details' page is relative to full project, not finding scope

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

1.  Navigate to the 'Set Objectives' page and start creating a new project.
2.  Set the table as 'Incident'.
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

Project created in Zurich, migrated to Australia, criteria between steps are not migrated

</td><td>

On a Zurich instance, when a project is created with at least one rule based finding that has a constraint in it, and it is then migrated to Australia, criteria between steps is not migrated along.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB2091109

</td><td>

The **Finding Condition** field drop-down list allows journal-type fields, causing the save to fail with the generic message 'Finding Condition save failed'

</td><td>

When configuring a rule-based finding definition's start/end condition \(sn​Promin​Rule​Based​Findings​Connected &gt; saveFindingDefs\), the condition builder's field drop-down list lets the user select journal-type fields on the target table \(for example, comments on sn\_customerservice\_case\). However, promin\_finding\_def\_condition doesn't support journal fields as condition fields. Promin​Allowed​Columns.​\_​get​Internal​Types\(\)​ only allows choice, string, boolean, integer, reference, workflow, and glide\_date\_time for promin\_finding\_def\_condition \(unlike promin\_activity\_def, which explicitly allow lists journal\_input\). The 'Business Rule Validate' allowed fields are selected on promin\_finding\_def\_condition. The insert for a journal field is correctly aborted, but the failure only surfaces to the user as a generic success: false / 'Finding Condition save failed' from saveFindingDefs. There's no indication of why or which field is invalid.

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

Process Mining allows sub-production instances to sample mine.A user can get in touch with Process Mining using the evaluation projects, and when the user needs some unique analysis, they can have the option to clone to sub-prod with audit log data included to accommodate those scenarios in the sales cycle. Lately sub-production instances that were labeled as **Open** are closed. An open instance doesn't check for licenses, where a closed instance does. Many sub-production instances are now blocked.

</td><td>

1.  Navigate to a sub-prod instance that is closed.
2.  Try to sample mine.

 Observe that the mining fails.

</td></tr><tr><td>

Process Mining Workspace

 PRB2096791

</td><td>

'Launch Process Mining' appears for all non-task related tables on workspaces

</td><td>

The **Launch Process Mining** button appears on the workspace list when it should only appear for task extended tables.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB2074908

</td><td>

The Planned End Date and Duration do not revert after moving and reverting the planned start date

</td><td>

After changing and reverting the Planned Start Date on a project, the Planned End Date and Planned Duration do not recalculate to their original values. The issue stems from the project constraint date not updating, causing child tasks and rollup dates to remain pinned.

</td><td>

1.  Open a BPI Dev instance.
2.  Create a new project.
3.  Import the MSP file.
4.  Verify the initial values:
    -   Planned Start Date: 06/02/2026 08:00:00
    -   Planned End Date: 10/05/2026 12:00:00
    -   Planned Duration: 86 Days 4 Hours
5.  Use the 'Move project' function to change the Planned Start Date to 06/08/2026 08:00.

Observe that the Planned End Date becomes 10/12/2026 13:00 and the Planned Duration becomes 90 Days 4 Hours.

6.  Use the 'Move project' function again to revert the Planned Start Date to 06/02/2026 08:00.

 Expected behavior: The Planned End Date returns to 10/05/2026 12:00 and Planned Duration returns to 86 Days 4 Hours.

 Actual behavior: The Planned End Date remains 10/12/2026 13:00 and Planned Duration shows 94 Days 4 Hours.

</td></tr><tr><td>

Pub/Sub

 PRB2094920

</td><td>

ProcessedMessageTracker \(N2N/PubSub dedup map\) grows unbounded and OOMs app nodes

</td><td>

It has been observed that com.​glide.​pubsub.​dedup.​Processed​Message​Tracker \(a singleton ConcurrentHashMap&lt;String, Long&gt; used to dedupe cache-flush messages arriving via both the N2N fast-push path and the sys\_cache\_flush DB-polling path\) is growing unbounded, driving app nodes to 'java.lang.OutOfMemoryError: GC overhead limit exceeded'. After heap dump analysis, the map \(fProcessedMessages\) retained 1.94 GB / 47% of the total heap on an affected node. This has caused OOMs on distinct production instances, consistent with slow unbounded growth after upgrade. Three distinct gaps contribute to this: There is no guard when Samwaad/N2N is not initialized or disabled; cleanup is gated by a hardcoded, non-exhaustive node-type allow-list instead of actual role/participation; there is no upper bound on the map's size.

</td><td>

 

</td></tr><tr><td>

Record Watcher

 PRB2083306

</td><td>

Support for public usable APIs on Filter.checkRecord\(\) for Decision Table performance

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB2067688

</td><td>

Reports shared with a user with the snc\_internal role aren't loading

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB2089532

</td><td>

Read-only report viewer link isn't visible

</td><td>

When sharing in report designer, the read-only report viewer link isn't visible.

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB2089828

</td><td>

The stage history is not displayed for a Requested Item when the related request is canceled using the **Cancel Request** UI action

</td><td>

The user should see the full, expandable stage history but only the non-expandable line 'Request canceled' appears.

</td><td>

1.  Log in to the instance as admin or as any user who can order and approve catalog items.
2.  Order a catalog item that requires approval and has a multi-stage fulfillment process.
3.  Approve the request via Approvals or sysapproval\_approver.
4.  Wait/allow the RITM to progress into a later stage, such as 'Fulfillment'.
5.  Open the Request \(sc\_request\) form in Classic UI.
6.  Select the **Cancel Request** UI action.
7.  Confirm the cancellation.

Observe that the Request and Request Item are now 'Closed canceled'.

8.  Navigate to the **Employee Center**.
9.  Open the 'Request Summary' page for the canceled request, or the 'My Request' page for the canceled RITM.

Observe the 'Stage' column/section for the requested item.


 Expected behavior: The stage tracker should show the full, expandable stage history — the same multi-stage list shown before cancellation \(Waiting for Approval, Fulfillment, Awaiting Delivery, Configuration, Delivery, Completed\) — with an expand/collapse toggle available, so the user can see exactly which stages were completed and which stage was active when the request was canceled.

 Actual behavior: Only a single, non-expandable line reading 'Request canceled' is displayed. There is no expand/collapse toggle and no way to view the underlying stage history, and the user cannot tell which stages were completed or which stage was active at the time of cancellation.

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

 PRB2109946

 [KB3229093](https://hi.service-now.com/kb_view.do?sysparm_article=KB3229093)

</td><td>

Update set artifacts imported to Brazil instances are assigned random scopes instead of global

</td><td>

This issue may cause records/artifacts imported via Update Sets to be assigned to the wrong application scope. This occurs when the previous update set applied to an instance on Brazil included Restricted Caller Access \(RCA\) Source Types.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Security Incident Response Workspace

 PRB2069672

</td><td>

Most dashboards are not loading and displayed a 'Page not found' message

</td><td>

This issue occurred after upgrading to the Brazil release.

</td><td>

1.  Open the instance.
2.  Navigate to the Security Incident Response Workspace.
3.  Select the left side dashboard menu item.
4.  Attempt to select a dashboard.

 Observe the 'Page not found' message.

</td></tr><tr><td>

Server-side scripts

 PRB2093303

</td><td>

KittyScript should check the function provenance on a call target

</td><td>

 

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

Service Catalog

 PRB1977691

</td><td>

The search box in the 'SC categories' page is not honoring the dark theme in Service Operations Workspace \(SOW\)

</td><td>

The dark theme is not honored and the search box and text fields appear with a white background. The text the user enters in these fields appears in white, making the text not visible.

</td><td>

1.  Open SOW.
2.  Open any new incident.
3.  Trigger the **Create request** UI action.
4.  Observe that the 'Catalog categories' page is displayed.
5.  Try to search any item name in the search box.

 Expected behavior: The search box is shown with a black background and in white text.

 Actual behavior: The search box is shown with a white background. As a result, user-entered text is not visible.

 Scenario 2:

 Search for the catalog item named 'Standard Laptop'

 Expected behavior: All text input fields are shown in a black background.

 Actual behavior:**Text** fields are shown in a white background, which is not expected.

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

Service Portal Core Widgets

 PRB2082183

</td><td>

The **Send** button in the search bar is enabled even when the cursor is pointed outside search bar with no text in it

</td><td>

The **Send** button inside the 'Typeahead search' widget in the Employee Center homepage remains enabled after the search text is cleared and the mouse pointer is moved outside of the **Search** field.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB2070851

</td><td>

The sp-tinymce-editor fails to render on the ESC portal, and ais-ux-bundle corrupts global tinymce object after sp\_min.jsx load

</td><td>

The TinyMCE rich-text editor \(sp-tinymce-editor\) does not render on any ESC portal page that uses it. The 'Add notes' label appears but the editor area is blank. This issue affects WSD Reservation Details \(Add Notes\) and ESC KB Article View \(Add Comment\).

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB2075083

</td><td>

The ESC portal AI Search placeholder text customization is no longer honored after an Australia upgrade

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

 PRB2087070

</td><td>

'glide.gig.client.endpoints' in the deny list causes a 'skipped error' during upgrade and prevents base instance sys properties from being installed

</td><td>

During cloning, if the source instance has glide.gig.client.endpoints sys properties set, and the destination \(target\) does not, this sys property may be copied from source to target. This configuration is instance specified and should not be cloned.

</td><td>

Upgrade Australia.

 Observe the skipped error in the upgrade history.

</td></tr><tr><td>

Software Asset Management

 PRB2100419

</td><td>

The app sn\_audit\_response fails to upgrade to true-up version 2.0.6 due to a scope ID mismatch

</td><td>

2.0.6 declares a dependency on a scope called sn\_audit\_workspace. That scope can't be resolved on this instance because the Audit Workspace app is registered under the scope sn\_audit\_ws. The whole app load aborted, and sn\_audit\_response stayed on 2.0.1.

</td><td>

 

</td></tr><tr><td>

Software Asset Reconciliation

 PRB2071332

</td><td>

A performance issue in which the dedup Job times out after approximately 5 hours

</td><td>

 

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

 PRB2052842

</td><td>

Gen AI logs are not visible for AI Control Tower \(AICT\) executions

</td><td>

The Gen AI logs related to the DARE execution capability had conversations with successful execution tasks, indicating there were LLM calls for the DARE agent.

</td><td>

1.  Open AICT.
2.  Look at the conversation IDs.

 Observe that the Gen AI logs related to the DARE execution capability are not visible.

</td></tr><tr><td>

Stream Connect Core

 PRB2081573

</td><td>

MessageRetryJob never retries undelivered messages whose sc\_topic\_alias resolves to a Hermes topic \(V3 Hermes-via-alias\)

</td><td>

MessageRetryJob.execute\(\) is supposed to retry both Direct Kafka messages and Hermes \(V3, via topic alias\) messages per its own inline comment, 'Try all direct kafka messages and V3 Hermes messages'. It only builds two queries against sys\_undelivered\_messages: sc\_topic\_alias IN \(the set of Direct-Kafka-backed alias sys\_ids returned by SCTopic​Repository.​get​Direct​Kafka​Cluster​Map\(\)​\)​ and sc\_topic\_alias ISEMPTY \(older V2 Hermes messages with no alias at all\).

</td><td>

1.  Create a Stream Connect producer/flow that sends via a sc\_topic\_alias, whose underlying topic is Hermes-backed \(such as SCHermesTopic, not in sys\_kafka\_direct\_topic\).
2.  Force a delivery failure so a row lands in sys\_undelivered\_messages with sc\_topic\_alias populated pointing at that Hermes-backed alias.
3.  Let MessageRetryJob run \(scheduled job in glide-ih-kafka\).

Observe that for execute\(\) \(MessageRetryJob.java:70-82\), the row value sc\_topic\_alias is not in the Direct-Kafka-only set returned by SCTopic​Repository.​get​Direct​Kafka​Cluster​Map\(\)​ \(SCTopic​Repository.​java:​135-​148\)​,​ and sc\_topic\_alias is not empty either, so the row matches neither of the two queries built in execute\(\).


 Observe that the row is never passed into retryMessagesForACluster\(\) and is never resent or removed. It remains in sys\_undelivered\_messages indefinitely across every job run.

</td></tr><tr><td>

System Events

 PRB2080045

 [KB3221356](https://hi.service-now.com/kb_view.do?sysparm_article=KB3221356)

</td><td>

Post-clone event-processing cleanup scripts \(201-204\) fail to run when a user script ahead of them errors out

</td><td>

The post-clone cleanup scripts Delete Processing Framework Triggers \(201\), Deduplicate Queues Post Clone \(202\), Deduplicate Queue Params Post Clone \(203\), and Re Provision Queues Post Clone \(204\) are failing to run. This occurs when a cleanup script at a lower order value errors during the clone. Since the clone cleanup runner stops entirely on the first failure, scripts 201-204 never execute. Event queues are left unprovisioned, backing up hundreds of thousands of events until the missing scripts are run manually via emergency change.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Events

 PRB2087104

</td><td>

An uncached sysevent\_queue contributes to a huge volume of periodic queries against the sysevent\_queque table for flow\_engine, auto\_chat\_queue, platform\_analytics\_export queues

</td><td>

This was noticed in Automated Query Caching. Queries are cached against the sysevent\_queue table for the following queues: flow\_engine, auto\_chat\_queue, platform\_analytics\_export queues. They seem to run at a very high volume and frequency.

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

System Events

 PRB2096831

</td><td>

Add a lower bound to the runtime of events for Threadpool admission

</td><td>

For now, there's only an upper bound threshold beyond which the events are rejected from the Threadpool admission for in memory processing. There's a need to add a lower bound also for the runtime below. The events shouldn't be admitted into the threadpool queue and should process as usual, flow events through jobs.

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB2054220

</td><td>

Use DMLActionBatcher instead of StatementBatcher to process batched records on import sets

</td><td>

This is a product update.

</td><td>

 

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

ThreadPoolProvider defines three tuning properties for the gateway fixed thread pool: glide.​gateway\_​fixed\_​thread\_​pool.​core\_​size,​ .max\_size, and .queue\_depth. The first two \(fixedCorePoolSize and fixedMaxPoolSize\) override GlideProperty.notify\(\) and call reconcileGatewayFixedPool\(\) on every change, so editing them resizes the live GATEWAY\_FIXED\_THREAD\_POOL immediately. FixedQueueDepthLimit \(backing .queue\_depth\) has no notify\(\) override at all, so a change to this property is never propagated anywhere. The value is read exactly once, at static init, to build the pool's queue. GatewayFixedThreadPool stores it in a private final int fQueueDepthLimit and passes it directly into new Linked​Blocking​Queue&lt;&gt;​\(queue​Depth​Limit\)​.​ Neither the field nor the queue's own capacity can change after construction; GatewayFixedThreadPool exposes no setter for it, and LinkedBlockingQueue has no capacity-change API. GATEWAY\_FIXED\_THREAD\_POOL is public static final and is never recreated, so no live code path re-reads this property short of a full node restart.

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

Transaction Management

 PRB2097102

</td><td>

Disable loanable semaphores by default in Brazil

</td><td>

 

</td><td>

 

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

The db.client.operation.duration metric emit can call into scripting layer from DBI

</td><td>

The issue can occasionally cause increased memory usage or processing thread hangs.

</td><td>

Flush the cache \(preferably the scope provider cache and System Include Scripts cache\).

 Observe that any methods going through DBI close and call into scripting layer.

</td></tr><tr><td>

User Criteria for Service Catalog

 PRB2087796

</td><td>

Scripted user criteria might return stale results via AI Search and aren't cached durably for the Moveworks Search API

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1973486

</td><td>

Alert for sys\_user\_presence.user access

</td><td>

An error occurs when the user selects the Contact card icon under 'Record Information'.

</td><td>

1.  As a non-admin user, open any interaction or incident in Service Operations Workspace.
2.  Select the **Contact card** icon under 'Record Information'.
3.  Refresh the page.

 Expected behavior: No error occurs.

 Actual behavior: An error alert appears.

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
5.  Select on the **New** action.
6.  Select the interceptor and try creating the new article.
7.  Return to the list view and select the **New** action again.

 Observe that the second time interceptor page is not loading and is blank.

</td></tr><tr><td>

UX Framework

 PRB2061413

</td><td>

Memory leak in builder tabs \(Table Builder, Playbook\)

</td><td>

Opening builder tabs \(Table Builder, Playbook, Flow Designer\) in ServiceNow Studio \(Glider SNS\) and closing them does not reclaim heap memory in the Australia family. Memory after tab close + GC remains at peak level and never returns to baseline. The same steps on the Zurich family produce no leak — memory returns to baseline cleanly.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB2066912

</td><td>

The 'Corrective action' AI agent is not working on track/bnowassist DC instance

</td><td>

 

</td><td>

1.  Under the Virtual Topic Designer, search for the topic 'Corrective action creator'.
2.  Open it.
3.  Select the **Test** button

 Observe that it will trigger under the topic.

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

 PRB2057885

</td><td>

Feedback icons don't show in AI Agent chat messages

</td><td>

When the user hovers over the message bubble, the 'Thumbs Up' and **Thumbs Down** buttons aren't present.

</td><td>

1.  Configure an AI Agent which uses show\_output\_to\_user tool as the first tool.
2.  Run the agent in playground or NAP.
3.  Hover over the message bubble.

 Observe that the **Thumbs Up** and **Thumbs Down** buttons aren't present.

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

 PRB2073250

</td><td>

A conversation from another domain doesn't work if the user default domain doesn't have access to the current session domain

</td><td>

Whenever there is a hybrid queue into play, the worker impersonates the user and updates the session, but doesn't touch the domain. When impersonated normally, the domain will be the default domain for the user. This might no have access to the conversation because its started in a different domain. When data that is not accessible like in the conversation, the flow fails.

</td><td>

1.  Enable domain separation.
2.  Update any field on a user record.

Observe that once it is updated, the default domain to the user moves to TOP/Default unless specified.

3.  Switch the domain to a different domain \(some sibling domain or a parent domain\).
4.  Start the conversation.

 Observe the responses would not be received for any query.

</td></tr><tr><td>

Virtual Agent

 PRB2076609

</td><td>

The 'Timeout conversations' job fails to close conversations on cross domains

</td><td>

 

</td><td>

 

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

 PRB2087473

</td><td>

Bring the tone/persona sys-prop at the assistant level and append the agent\_persona instruction to it

</td><td>

If the configuration attribute isn't 'agent persona', the system appends the agent persona to the prompt if it exists. If the attribute is 'agent persona', it uses the persona or a static fallback if empty.

</td><td>

1.  Bring the sys-prop 'sn\_​nowassist\_​va.​assistant\_​personalization' to the Now Assist deployment configurationtable.
2.  Make the setting available at the assistant level.
3.  Append the **Agent\_persona** field in the Now Assist deployment configurationtable to tone/persona prompt.

 Observe that, when the configurationattribute isn't 'agent persona', the system appends the agent persona to the prompt if it exists. If the attribute is 'agent persona', it uses the persona or a static fallback if empty.

</td></tr><tr><td>

Virtual Agent

 PRB2091209

</td><td>

The Nextwave feature flag is not invalidated on insert/update

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

 Expected behavior: The live agent transfer should stop just for that interaction when**Cancel** is selected and the live agent availability should start resuming after.

 Actual behavior: Notice that even when the agent is available, it shows that no agents are available. This happens for all the new conversations.

</td></tr><tr><td>

Virtual Agent

 PRB2094745

</td><td>

There's an ArrayIndexOutOfBoundsException in Agent​Tool​M2​MCache.​get​Cache​Value when cache key parts are all empty

</td><td>

AgentToolM2MCache. getCacheValue\(String key\) \(AgentToolM2MCache.java:32-33\) throws 'java.​lang.​Array​Index​Out​Of​Bounds​Exception:​ Index 0 out of bounds for length 0' when key.split\(DELIMITER\) is called on a key composed entirely of delimiter sequences. String.split\(\) strips all trailing empty strings from its result by default. If every field \(sysId, name, agentId, language\) passed into getCacheKey\(...\) is blank, the resulting key contains only delimiter text, and split\(DELIMITER\) collapses to a zero-length array. The subsequent keyParts\[0\] access on line 33 then throws the error.

</td><td>

1.  On an instance with an assistant configured for NextWave/premium chat, add a survey fallback.
2.  Save.
3.  Blank out the survey.
4.  Save.

This creates a record in the sys\_cs\_context\_profile\_tool table with an empty tool column.

5.  Navigate to **Configured Assistant**.
6.  Try to start a conversation.
7.  Expected behavior: The conversation starts correctly
8.  Actual behavior: Handshake fails with an ArrayIndexOutOfBounds exception.

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

 Expected behavior: The text file should open.

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

Ci-chat-components doesn't post a message to the parent window on session-call failure, breaking the documented SSO redirect

</td><td>

Users can embed the Portable VA web-client iframe in the external OpenText front end with SSO. The documented integration has the parent page listen for a message event and redirect to SSO when it receives type SESSION\_CREATED with authenticated false. However, when the session call fails \(401\), the client doesn't post that message \(or any message\) to the parent, so the redirect never fires and the embed loops.

</td><td>

1.  Embed the Portable VA web client iframe in an external page \(OpenText\), using the documented SSO integration that listens for a postMessage and redirects to SSO on type SESSION\_CREATED with authenticated false.
2.  Load it in a context where the session / Consumer Account call returns 401 \(no established session\).

 Observe that the client shows the middle-panel error inside the iframe but posts nothing to the parent window. SESSION\_CREATED \(authenticated false\) never fires, the parent's SSO redirect never runs, and the embed loops.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB2092886

</td><td>

NLU Chat is unusable at 400% zoom

</td><td>

 

</td><td>

1.  Navigate to any standard chat implementation.
2.  Set the browser to 400%.
3.  Select the chat launcher to open the chat.

 Expected behavior: Users should be able to see messages.

 Actual behavior: The chat is unusable because the launcher takes up half the screen, then in the popover the header and input eat the other half.

</td></tr><tr><td>

Vulnerability Response

 PRB2069210

</td><td>

Invalid ACLs in the Exception Management configuration in Configuration Compliance

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Window Manager

 PRB2090196

</td><td>

The closed window still consumes mouse selects after unpinning Otto, which blocks the Polaris contextual menu pin

</td><td>

After opening and closing \(specifically pinning/unpinning\) Otto, its window element remains mounted in the DOM at full size and intercepts selects over whatever page content is underneath it. Its DOM element remains at full size with pointer-events overridden by inner content, instead of collapsing to a 0-size box like the legacy window manager does. This prevents the user from pinning other contextual menus via Polaris in that region of the screen.

</td><td>

1.  Open a Brazil instance.
2.  Open Otto \(Now Assist chat\).
3.  Pin Otto by docking it via a contextual menu/Polaris pin action.
4.  Unpin Otto so that it closes.
5.  With Otto now closed, try to select/pin a different contextual menu in the area of the screen where Otto's \(now invisible\) window used to be.

 Observe that the select is swallowed, and pinning other contextual menus is not possible because the closed Otto window is still consuming mouse selects.

</td></tr><tr><td>

Work Order Management

 PRB2075229

</td><td>

External agents are not able to access wm\_task records after the new query\_range ACL

</td><td>

An error is thrown and the tasks are not appearing.

</td><td>

1.  Open a TD instance.
2.  Impersonate the user 'test.agent1'.
3.  Navigate to **FSMCP**.
4.  Navigate to **My Lists** &gt; **My Tasks** &gt; **Today's Tasks**.

 Expected behavior: Today's tasks \(expected\_start on today\) should be displayed in the list.

 Actual behavior: An error is thrown, 'Part of the query on wm\_task has been ignored because of insufficient access for 'query\_range' operation on wm\_task.expected\_start'. The tasks are also not shown as expected.

</td></tr><tr><td>

Workplace Visitor Management

 PRB2099708

</td><td>

The visitor is using the wrong version in a Brazil base instance

</td><td>

The visitor version has to be 1.19.20 in Brazil, now it is installing v2.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Brazil Patch 1 Hotfix 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/brazil-patch-1-hf-1.md)
-   [Brazil Patch 1](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/brazil-patch-1.md)
-   [Brazil security and notable fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/brazil-security-notables.md)
-   [All other Brazil fixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/brazil-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/release-notes/available-versions.md)


---
title: Zurich Patch 5
description: The Zurich Patch 5 release contains important problem fixes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2026-01-12"
reading_time_minutes: 76
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 5

The Zurich Patch 5 release contains important problem fixes.

-   **Zurich Patch 5 was released on January 12, 2026.**
    -   Build date: 01-05-2026\_2218
    -   Build tag: glide-zurich-07-01-2025\_\_patch5-12-17-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z05.00.xlsx).

## Overview

Zurich Patch 5 includes 338 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-zp5.png "Top 10 problem categories")

## Security-related fixes

Zurich Patch 5 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 5, refer to [KB2700349](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2700349).

## Changes in Zurich Patch 5

-   **[Cloning and upgrading considerations for Developer Sandboxes](https://www.servicenow.com/docs/access?context=dev-sbx-clone-upgrade-info&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    As of Zurich Patch 5, Developer Sandboxes will back up any update sets from the sandboxes and export them to the main instance.

-   **[Retire Developer Sandboxes](https://www.servicenow.com/docs/access?context=retire-sandboxes&version=zurich&pubname=zurich-application-development&ft:locale=en-US)**

    However, if you are on Zurich Patch 5 or later, update sets on the instance may be automatically backed up.

-   **[Exploring Code Signing](https://www.servicenow.com/docs/access?context=explore-code-signing&version=zurich&pubname=zurich-platform-security&ft:locale=en-US)**

    All the metadata tables with valid configurations are signed at build time using the Code Signing metadata plugin​ \(com.glide.code\_signing\). Installing this plugin automatically installs the Code Signing OOB App Signatures plugin \(com.glide.code\_signing.oob\_apps\_signatures\) which contains build time signatures for all relevant records in the trued-up ServiceNow® Store application versions. If you choose to sign tables, admin users with the Security administrator role have access to Code Signing job​s:


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

AI Search \(Glide\)

 PRB1937244

</td><td>

java.lang.SecurityException: AisDisableSearchSignalEvent is undefined and may be missing a global qualifier

</td><td>

java.lang.SecurityException: AisDisableSearchSignalEvent undefined, maybe missing global qualifier.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1921408

 [KB2659810](https://hi.service-now.com/kb_view.do?sysparm_article=KB2659810)

</td><td>

The sys\_hub\_flow\_version record of a flow is not captured in the update set when updating the flow

</td><td>

The user must manually capture the sys\_hub\_flow\_version record in update set to avoid a preview error.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1946446

 [KB2601161](https://hi.service-now.com/kb_view.do?sysparm_article=KB2601161)

</td><td>

Filtering issues on a **Date** field in Workspace

</td><td>

Filter options on the field for dates on workspace are updated to an invalid date after selecting a date.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1970979

</td><td>

Help text is misaligned in portal forms after upgrading to Zurich

</td><td>

After upgrading to Zurich, the help text in portal catalog items are not aligned correctly. They are shifted to the right of the label above it.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1894995

 [KB2438505](https://hi.service-now.com/kb_view.do?sysparm_article=KB2438505)

</td><td>

A requested item \(RITM\) created from an interaction in Service Operations Workspace \(SOW\) with an HTML variable automatically re-attaches images from the variable as the current user

</td><td>

When a user copy-pastes text and images from Word, email, etc. to an RITM created from an interaction in a SOW HTML variable, reloading the RITM automatically re-attaches images to the record and gets displayed in the activity stream as a new attachment.

</td><td>

1.  Navigate to an Xanadu instance.
2.  Create a catalog item with one HTML variable.
3.  Open an interaction record from SOW.
4.  Locate and select the **Create Request** button.
5.  Create a request for the catalog item created in the second step.
6.  In the HTML variable, copy-paste text and images from a Word document or email.
7.  Submit the request.
8.  From SOW, open the RITM just created.

 Expected behavior: The RITM opens normally and images aren't reattached.

 Actual behavior: Images from the variable are reattached every time a user opens the RITM record. Newly re-attached images are shown in the activity stream. These images can also be found in the sys\_attachment table with Table sys ID = RITM sys\_id.

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

 PRB1964011

</td><td>

AllTermsCache has an increased live set of close to 20 MB in Zurich

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1836275

</td><td>

ScriptClassifier .isScriptUsingCurrent\(\) returns true despite the passed in string not being current

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1928472

</td><td>

Unable to assign a 'User' admin role to a contact from the contact view page from CSM portal

</td><td>

An error is thrown reading, 'User has conflicting role 'snc\_required\_script\_writer\_permission'. All explicit role collisions must be addressed in the hierarchy.'

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1938077

</td><td>

Unable to troubleshoot slow ACLs due to batched logging

</td><td>

Batched logging impacts troubleshooting ability and affects users that rely on inline logging.

</td><td>

1.  Navigate to syslog\_list.do.
2.  Search for a message that starts with 'Slow ACL'.

 Observe that batched log messages may not be logged at the time they are generated, and that there may be a delay before a slow ACL is logged.

</td></tr><tr><td>

Access Control

 PRB1943406

</td><td>

The **Article Body** \('text'\) field is read only for new users that inherit the 'knowledge' Role from a Group

</td><td>

This issue is only observed in the Zurich family release.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1960642

</td><td>

Remove Datatype ACLs created for HTML and translated\_html datatypes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Activity stream

 PRB1899572

</td><td>

The 'Activity' section of the 'Details' tab doesn't show field changes upon incident creation

</td><td>

The Activity stream doesn't show events when the user creates a record from the record page, the 'Details' tab doesn't load in the first position, and the user switches to the 'Details' tab.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1914953

 [KB2481528](https://hi.service-now.com/kb_view.do?sysparm_article=KB2481528)

</td><td>

The user is unable to enter more than 4000 characters in length on the **Journal** field after upgrading

</td><td>

Users are unable to copy or paste the text with more than 4000 characters on the **Journal** field after upgrading from Washington DC to Yokohama.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1970818

</td><td>

Add support for AI Agents in AWA

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Agent Assist

 PRB1910542

</td><td>

The window pane doesn't resize when composing an email in a configurable workspace

</td><td>

When the user composes an email in a configurable workspace, the window pane doesn't resize for the email body. The 'Email Templates' frame is expanded and not scrollable, and the **Send email** button isn't visible.

</td><td>

1.  In Yokohama, navigate to an instance.
2.  Open any workspace \(SOW/CSM/FSM\).
3.  Open any incident in the workspace.
4.  Compose an email.

Notice a new tab opens.

5.  Verify that the 'Email Templates' frame is opened.

 Expected behavior: The 'Email Templates' frame is collapsed and scrollable. The Email Client Body is the same size as the window, and the **Send email** button is visible.

 Actual behavior: The 'Email Templates' frame is expanded and not scrollable. The Email Client Body is the same height as the 'Email Templates' frame, and the **Send email** button only appears after scrolling down.

</td></tr><tr><td>

Agent Chat

 PRB1970504

</td><td>

Skip read-only states that are not the current state

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1963825

 [KB2649969](https://hi.service-now.com/kb_view.do?sysparm_article=KB2649969)

</td><td>

Update AI Agents \(AIA\) true-up version to four.0.38

</td><td>

Updating the AIA true-up version to fix a potential infinite loop in an upgrade scenario.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1970451

</td><td>

ACL cache retrieval behaves differently for hierarchies; the returned value is not the same as the one stored in the cache

</td><td>

Behavior differs between no cache runs and cache-filled runs.

</td><td>

 

</td></tr><tr><td>

AI Agents \(Glide Family\)

 PRB1971370

</td><td>

Mandatory inputs are not checked prior to tool execution to handle missing inputs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1926964

</td><td>

E5 encoding does not work when a non-base instance English \(EN\) record is created in the sys\_language table

</td><td>

The issue occurs because E5 model config references sys\_language records for supported languages. It saves sys\_id of the record. However, if the user's instance has a non-base instance language record, it will not work with E5.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1932287

</td><td>

Null Pointer Exception occurs during catalog variable indexing when **Choice Text** is empty

</td><td>

 

</td><td>

1.  Create or edit a catalog variable with choice options.
2.  Leave the **Choice Text** field empty for one or more options.
3.  Trigger the indexing process for the Catalog variable.

 Observe that a Null Pointer Exception \(NPE\) occurs during indexing.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1936969

</td><td>

Spinner or loader still shown when Genius Result \(GR\) isn't linked to the search application

</td><td>

 

</td><td>

1.  Launch any instance.
2.  Remove any GRs if present.
3.  Attempt to search for a term.

 Expected behavior: The GR spinner and empty state should show up only if GRs are configured.

 Actual behavior: The GR Spinner animation shows up even if GRs aren't configured.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1954965

</td><td>

The Query Timeout property doesn't configure application level timeout

</td><td>

 

</td><td>

1.  Adjust glide.ais.query.timeout higher than ten seconds.
2.  Issue a query that runs longer than ten seconds, but shorter than what was configured for glide.ais.query.timeout.

 Notice that a timeout response is returned.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1961490

</td><td>

The user cannot ingest semantic fields for skills in a non-global domain

</td><td>

The topic is not discoverable in NAVA when the corresponding skill is created in a non-global domain.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1967477

</td><td>

When no Virtual Agent app is enabled, Global search with AIS enabled fails

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1972985

</td><td>

Multimodal Captioning for AIS Glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search for Virtual Agent

 PRB1953578

</td><td>

Pass limitColumnOutput param in apiOptions for t2r call

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1883371

</td><td>

AI Search XMLstats should return AIS connections irrespective of the 'Aggregate Health Data for AIS Partition' sys\_trigger execution

</td><td>

This blocks monitoring capability of checking if ais.nodes exists on the instance.

</td><td>

1.  Disable or delete the 'Aggregate Health Data for AIS Partition' sys\_trigger execution.
2.  Add /xmlstats.do?include=ais to the URL.

 Expected behavior: This returns ais.nodes.

 Actual behavior: ais.nodes is empty.

</td></tr><tr><td>

AI Search

 PRB1893450

</td><td>

When there's a search application without a name, the drop-down list appears empty

</td><td>

When the user creates a search application without a name, the drop-down list for selecting search applications appears empty and displays the message 'null'.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1912867

</td><td>

Unable to style search result title highlighting

</td><td>

The title \(now-text-link\) highlighting isn't altered.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1913656

</td><td>

Dot-walked genius result fields are returned with dots instead of underscores

</td><td>

 

</td><td>

1.  Search for Company Policies in /esc portal.
2.  Select the Company Policies genius result.

 Observe that the navigated page has no sys\_id.

</td></tr><tr><td>

AI Search UX

 PRB1918092

</td><td>

Now Assist synthesized response cards should not show a price for a non-billable catalog item

</td><td>

When the LLM generates answers containing a catalog item, the tool tip for this item shows a price of $0.00 for non-billable item instead of showing nothing.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1928007

</td><td>

An empty GR result is shown when a multi-content GR response is returned for a different search

</td><td>

Notice that an empty GR result is displayed.

</td><td>

1.  Enable multi-content response GR on a portal \(/sp\) search profile.
2.  Unlink multi-content GR from another portal \(/esc\) search profile.
3.  Perform search on portal one \(/esc\) \(for example, what is spam\).

Multi-content response GR is not returned.

4.  Open portal two \(/sp\) in a new browser tab.
5.  Perform a search \(for example, 'what is spam'\).

This returns a multi-content response GR result.

6.  View the portal one \(/esc\) browser tab from step 3.

 Notice that an empty GR result is displayed on portal one.

</td></tr><tr><td>

AI Search UX

 PRB1952630

</td><td>

Malformed URLs in the streaming chunks for a synthesized response cause the UI to hang

</td><td>

The URL renders stand-alone and sometimes isn't selectable.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1959826

</td><td>

Search select events are not tracked when applying any facet that contains 'UNION'

</td><td>

The select event is not captured on sys\_search\_signal\_result\_event table. It gets captured once the facet is removed.

</td><td>

1.  Visit any search page which has facets whose values contain 'UNION'
2.  Apply the same facet.
3.  Select any search result.

 The select event is not captured on sys\_search\_signal\_result\_event table. It gets captured once the facet is removed.

</td></tr><tr><td>

AI Search UX

 PRB1961267

</td><td>

Ask-a-follow up and Request in chat doesn't work on global search

</td><td>

A follow up question is not asked and there is no Request in chat option available.

</td><td>

1.  Enable NAP on global search.
2.  Search for 'Apple Watch' or 'Loaner Laptop' \(any conversational catalog query\).

 Notice that a follow up question is not asked. Also, when the user selects **Catalog citation**, notice there is no Request in chat option available.

</td></tr><tr><td>

AI Search UX

 PRB1963505

</td><td>

URLs towards the end of the streaming are rendered as plain text

</td><td>

 

</td><td>

1.  Open an instance where synthesized answers are working.
2.  Search a query that would have a URL towards the end of the answer.

 Observe that the URL is rendered as plain text.

</td></tr><tr><td>

AI Search UX

 PRB1963984

</td><td>

Streaming fails when there's a response with numerous citations

</td><td>

When the user searches for a term with ten or more citations, streaming sometimes gets stuck. It indirectly pushes component into halt and doesn't show feedback options.

</td><td>

1.  Provision an instance with Synth GR.
2.  Search for a term that would result in ten or more citations.

 Observe that the streaming is intermittently stuck, indirectly pushing component into halt and not showing feedback options.

</td></tr><tr><td>

AI Search UX

 PRB1966920

</td><td>

The 'Now Assist detected and ...' alert is shown on the top results card when sensitivityFilter.hasMatch is false

</td><td>

Sometimes, the payload of final MESSAGE\_RECEIVED event has the sensitivityFilter.hasMatch value as a string false. In such cases, the Genius card is hidden and an alert is shown.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1971350

</td><td>

When Hybrid Search is enabled, total count is missing

</td><td>

With Hybrid Search on, only facet count should not be shown.

</td><td>

1.  Enable DW/Hybrid Search on /sp on any Now Assist instance.
2.  Query 'what is spam'.

 Observe that the total count is missing.

</td></tr><tr><td>

AI Search UX

 PRB1972080

</td><td>

Console errors on Service Portal \(SP\) for non-synthesized GRs \(although functionally everything works as expected\)

</td><td>

 

</td><td>

1.  On a Yokohama or Zurich instance, disable Synthesized GRs for SP.
2.  Search for a term with which there is more than one GRs.

 Observe errors in the console such as 'Failed to load @devsnc/sn-search-genius-card-assist'.

</td></tr><tr><td>

AI Search UX

 PRB1972964

</td><td>

Make the search input bar responsive to long prompt for full page

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1892623

</td><td>

Data visualization on a pivot table shows 0 or incorrect/inconsistent data

</td><td>

Issue happens on both. Plugin sn\_app\_analytics\_w Version: six.0.six and six.0.eight.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1963964

 [KB2684464](https://hi.service-now.com/kb_view.do?sysparm_article=KB2684464)

</td><td>

The install/update modal for any Now Assist app that loads the new 'Now assist suite' UX opens takes over two minutes to load

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1964007

</td><td>

Sys\_prop polluting the update set

</td><td>

 

</td><td>

1.  Open App Manager.
2.  Select **Sync**.
3.  Check the current update set record.

 Observe that it records the current value of sn\_appclient.apps\_sync\_progress.

</td></tr><tr><td>

Application Rationalization

 PRB1921023

</td><td>

EA indicator framework generates the wrong score for the minimize indicator

</td><td>

When the absolute value is empty or not available, the EA indicator framework generates the wrong score for the minimize indicator.

</td><td>

1.  Navigate to a business application without any incidents.
2.  Generate the score for the incident indicator.

 Expected behavior: Since there are no incidents for the business application for the given fiscal period, and the incident indicator is minimize, the expected score is ten.

 Actual behavior: It generates 0.

</td></tr><tr><td>

Application Rationalization

 PRB1942817

</td><td>

Issues with Dependency View in Enterprise Architecture Workspace

</td><td>

In the Enterprise Architecture Workspace, the action **Open Dependency View** does not respond. No modal/tab opens, there's no redirection, and no error message is displayed. The page remains unchanged.

</td><td>

1.  Navigate to the Enterprise Architecture Workspace.
2.  In the left menu, navigate to **Portfolio** &gt; **Business Architecture** &gt; **Business Process**.
3.  Open any Business Process record.
4.  In the form, select **Open Dependency View** under More Actions \(⋯ icon\).

 Observe that nothing happens; nothing loads and there's no message.

</td></tr><tr><td>

Application Rationalization

 PRB1945947

</td><td>

Deletion of TRM product doesn't delete the associate life cycle record

</td><td>

 

</td><td>

1.  Navigate to the life cycle product table \(sn\_apm\_trm\_standards\_product\).
2.  Create a new record and populate the mandatory fields.
3.  Use the related list TRM Product Lifecycle \(sn\_apm\_trm\_standards\_product\_lifecycle\).
4.  Select **New**.
5.  Populate the mandatory fields.
6.  Submit.
7.  Open the sn\_apm\_trm\_standards\_product record that was created.
8.  Use the 'Delete UI' action.
9.  Navigate to the sn\_apm\_trm\_standards\_product\_lifecycle table.
10. Search for the record that was originally associated with the sn\_apm\_trm\_standards\_product that was deleted.

 Observe that the record is there, but its **TRM Product** field \(mandatory\) is empty.

</td></tr><tr><td>

Asset Management

 PRB1963341

</td><td>

The 'sn\_itam\_common.CommonMobileUtils' script include doesn't exist in the system

</td><td>

Asset Management Common plugins aren't activated as a dependency of IT Asset Management mobile. Even when activated, the script include used in the mobile action item is missing.

</td><td>

 

</td></tr><tr><td>

Audit History

 PRB1938364

 [KB2531096](https://hi.service-now.com/kb_view.do?sysparm_article=KB2531096)

</td><td>

Large amount of history \(audit\) data can lead to node memory contention on node when loading form

</td><td>

When loading a form for the first time, the node may run out of memory and crash. This happens if the history set has to be built to load the activity stream and if there's a lot of data to be loaded.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1961074

</td><td>

External users are not able to view the Soft PIN Enrollment page in portal

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1959359

</td><td>

Clean Up job for Metadata tracing OOMemory Issue: sysauto\_script.do?sys\_id=26c1592cff442210940effffffffff0b

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Batch API

 PRB1911987

</td><td>

Search sources in UI Builder's Source to Pay workspace Experience setting is null

</td><td>

Batch API calls don't accept special characters \(spaces, commas, pipes etc.\) in BatchItem URL fields in the payload in Zurich release.

</td><td>

1.  Navigate to UI builder.
2.  Select the experience page and select **Source to pay workspace**.
3.  Select the **View experience** setting.
4.  Change the scope to source to pay workspace.
5.  Scroll down to the global search.

 Observe that the search source drop-down list contains nothing to select.

</td></tr><tr><td>

Cache

 PRB1955869

 [KB2595527](https://hi.service-now.com/kb_view.do?sysparm_article=KB2595527)

</td><td>

The ScriptEnginesTables cache is undersized in Zurich release causing increased processing time

</td><td>

If an instance has more than 50 script engines installed \(via plugins and applications\), setting the current size to 50 for the ScriptEnginesTables cache may lead to an increase in processing times. This could lead to semaphore contention and/or exhaustion, resulting in a significant increase in total transaction time and processing time and script time.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1961987

</td><td>

HR case and ER case transfer with an attachment is showing up as JSON in AI Case summary

</td><td>

Issue is that style tags are present in a summary. In an AI summary card component, these style tags are rendered, but in a transfer case modal these are not rendered because it is a textarea.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1964899

</td><td>

Proof of grade and proof of payment are text boxes rather than attachments

</td><td>

 

</td><td>

Navigate to HR cases table \(Workspace/ UI16\) as an HR agent and select **New**.

 Observe that the fields shown in the UI are Tuition Reimbursement pre-approval fields. Proof of grade and proof of payment are text boxes rather than attachments.

</td></tr><tr><td>

Change Management

 PRB1946871

 [KB2671810](https://hi.service-now.com/kb_view.do?sysparm_article=KB2671810)

</td><td>

A user with a new role added to the 'change.conflict.role' system property gets a security constraint preventing access to requested page when checking conflicts

</td><td>

Custom roles for Change Management are unable to use the **Check Conflicts** button on the Change Request Conflict form section. This is because the UI Page and AJAX processor for this feature are restricted to itil and sn\_change\_write roles.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Change Management

 PRB1953175

 [KB2675721](https://hi.service-now.com/kb_view.do?sysparm_article=KB2675721)

</td><td>

The 'Notify assessment' user notification is triggered unnecessarily for Change risk assessments

</td><td>

The email notification is triggered by the subflow 'Notify Assessment user' at the time when Risk Assessment is opened \(where in theory the user will complete the risk assessment\). By the time the email notification is received, this message becomes unnecessary.

</td><td>

1.  Navigate to a Change Request.
2.  Save the Change Request.
3.  Open a risk assessment and complete it.

 Observe a notification saying the user has been assigned an assessment \(event 'assessment.received' in 'sysevent' table\).

</td></tr><tr><td>

CMDB Data Manager

 PRB1964689

</td><td>

CMDBRetirementScriptableAPI doesn't handle policies targeting tables that don't begin with 'CMDB'

</td><td>

Data Manager policies that target only tables without 'CMDB' in the start of the table name can't be published or run due to the CMDBRetirementScriptableApi not correctly handling the search for those tables' defined retirement state.

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB1955881

</td><td>

sn\_cmdb.\_\_rel\_type\_cache holds a lot of memory

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1969590

</td><td>

Import of updateset with signature reports errors

</td><td>

The user observes an error message and a prompt to manually override the errors.

</td><td>

1.  Create an updateset on TI with signatures.
2.  Import this update set on protected instance.

 Observe an error message and a prompt to manually override the errors.

</td></tr><tr><td>

Code Signing

 PRB1970032

</td><td>

Store app versions don't have base instance signatures

</td><td>

Base instance store app versions should contain signatures for all contained relevant records.

</td><td>

 

</td></tr><tr><td>

Column Level Encryption Enterprise

 PRB1957091

</td><td>

Sys attachments zip data and Column Level Encryption jobs are not completed

</td><td>

Sys attachments zip data and Column Level Encryption jobs not completed even when the CLE Migration Dashboard correctly reads this property and shows 'migration success' and com.glide.cle.allow\_ec\_key\_deletion is set to 'true'.

</td><td>

1.  Navigate to filter navigator.
2.  Remove triple DES usage.

 Observe that column level encryption data migration is not completed. Notice that sys\_property 'com.glide.cle.allow\_ec\_key\_deletion' is set to true. CLE Migration Dashboard correctly reads this property and shows 'migration success'

</td></tr><tr><td>

Communities

 PRB1952833

</td><td>

Blog posts within Community forums have all been reformatted

</td><td>

The HTML code not showing properly on blog in community portal.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1943552

</td><td>

dotWalkConnectedDataBehavior cannot be imported in version 27.0.four

</td><td>

The behavior source files aren't where exports exists after the import.

</td><td>

1.  Open a project where now-dot-walk 27.0.four is a dependency.
2.  Attempt to import dotWalkConnectedDataBehavior from '/now-dot-walk'.

 Expected: The import provides the consuming application with the behavior.

 Actual: The import doesn't provide the behavior source files where exports exist.

</td></tr><tr><td>

Content Publishing

 PRB1963246

</td><td>

Issue with content template duration calculation with a different date format

</td><td>

If the user changes the date format in sys\_property, content template duration calculation is ignored since calculation looks for specific date format of 'yyyy-DD-mm'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1864866

</td><td>

The CMDB table record on sys\_db\_object is not loading, and the transaction is canceled due to the large number of CMBD columns and indexes on the CMBD table

</td><td>

The CMDB table record on sys\_db\_object is not loading, and the transaction is getting canceled due to the large number of CMDB columns and indexes on the CMDB table supported by Oracle DB. The slowness is observed on MariaDB hosted instances as well.

</td><td>

1.  Log in to an instance as a user with elevated privileges.
2.  Open sys\_db\_object table.
3.  Search for the name 'CMDB'.

 Notice that the transaction keeps loading for five minutes and eventually cancels out. A similar call stack is observed when loading the 'v\_index\_creator\_list' with the filters as 'reference table' is 'Base Configuration Item'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1922171

 [KB2617119](https://hi.service-now.com/kb_view.do?sysparm_article=KB2617119)

</td><td>

CONTAINS query interferes with the RLQUERY in hybrid table

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1949762

</td><td>

The getBackingInformationForElement method returns null when the Cypher query returns entire nodes in aggregation queries for the sys\_user\_group/sys\_user table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1951553

</td><td>

Aggregate usage is not supported in WHERE clauses

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1952824

</td><td>

RecordHierachies fail to initialize on Oracle due to unique indexes found

</td><td>

Base instance hierarchies on Oracle are failing to initialize due to a failed check.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1959169

</td><td>

A datetime 'more than' query Business Rule throws a null pointer exception

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1960869

</td><td>

Tracking fails for select \* cases and is overly aggressive on security check failures

</td><td>

The select item tracking improperly categorizes accesses as complex so access check failures result in the whole row being rejected.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1962540

</td><td>

report\_on is honored for aggregates in cypher

</td><td>

Currently checks are done in tableLevelAclAllowed which will return false if there is no ACL defined at all. PA used hasRightsTo which has a more permissive behavior and allows access in this case.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1964653

</td><td>

Test failures in db-test

</td><td>

Tests are failing in db-test.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1928008

 [KB2428930](https://hi.service-now.com/kb_view.do?sysparm_article=KB2428930)

</td><td>

Upgrade to Yokohama releases can hang

</td><td>

Upgrades to Yokohama releases may hang for certain instances because of contention on the query registrar.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1942175

</td><td>

Thread goes into an infinite loop on DBQueryExecutor.executeStatement for broken queries that were rewritten

</td><td>

When the broken query is executed, StackOverflowException is thrown and com.glide.db.DBQueryExecutor.executeStatement goes into an infinite loop. Instead, SQLException should be thrown.

</td><td>

1.  Create the table u\_test with u\_test\_column.
2.  Create any valid query rewrite for the 'select u\_test\_column from u\_test' query.
3.  Drop the column u\_test\_column.
4.  Execute the query 'select u\_test\_column from u\_test' via DBQuery, or use a script with GlideRecord equivalent.

 Expected behavior: SQLException is thrown and com.glide.db.DBQueryExecutor.executeStatement doesn't go into an infinite loop.

 Actual behavior: StackOverflowException is thrown and com.glide.db.DBQueryExecutor.executeStatement goes into an infinite loop.

</td></tr><tr><td>

Database Persistence

 PRB1848049

</td><td>

Add support for new RaptorDB feature to prevent DDL locking

</td><td>

DDL locking occurs when a long-running query is executed.

</td><td>

1.  Execute a long-running query against Postgres.
2.  Attempt to alter a table using an instant operation.

 Notice that DDL blocks all traffic until the long-running query finishes.

</td></tr><tr><td>

Database Persistence - WDF

 PRB1890199

</td><td>

REST APIs to enable Trino connector /schemas/xxxxx/tables?type=physical to return physical table names

</td><td>

With current implementation, the returned results might contain logical table names such as sys\_atf\_test\_result\_performance. A physical name should be returned for it, such as sys\_atf\_test\_result\_p9e. Physical table names can be found in sys\_storage\_table\_alias.

</td><td>

 

</td></tr><tr><td>

Database Persistence - WDF

 PRB1950092

</td><td>

The WDF table eligible for sparse storage is not executing one pass query when calling get\(\) and Equals operation

</td><td>

The WDF table eligible for sparse storage now executes a two-pass query when running a get\(\)/Equals operation. It should only execute a one-pass query for both scenarios, similar to a glide table.

</td><td>

Scenario one:

 1.  Ensure the property glide.db.meta.non\_sys\_id\_sparse\_storage.allow is created.
2.  Set it to 'true'.
3.  Enable SQL debug.
4.  Navigate to the list view of a WDF table with single primary key defined.
5.  Open the condition builder.
6.  Set the **Primary key** field to 'Operation'.
7.  Run it.
8.  Scroll down the page when the list view has finished loading.

 Notice that in the List section, the record count query there will be two additional queries being made on the data fabric table when only one query is made.

 Scenario two:

 1.  Ensure the property glide.db.meta.non\_sys\_id\_sparse\_storage.allow is created.
2.  Set it to 'true'.
3.  Enable SQL debug.
4.  Navigate to **Background scripts**.
5.  Execute a glide record script that calls get using the encoded sys\_id of a WDF table.

 Observe that when executing the script, there are two queries being executed instead of just one.

</td></tr><tr><td>

Data Snapshots

 PRB1953187

</td><td>

DataSnapshot is not supported and causes errors in the System Log / Error Log

</td><td>

Users receive the following errors even in the Data Snapshot plugin is not installed: 'DataSnapshotEnablementApi: DataSnapshot is not supported for Raptor standard database: no thrown error' and 'DataSnapshot is not supported for Raptor standard database.'

</td><td>

 

</td></tr><tr><td>

Decision Table \(Family\)

 PRB1971318

</td><td>

Users are unable to publish decision tables

</td><td>

The decision table isn't published and a 'Could not update the decision table' message is displayed.

</td><td>

1.  Create a decision table with a result column of type choice and capture it in update set.
2.  Create new choice and add couple of choices.
3.  Import the decision table into another instance.
4.  Publish the decision table to move it from draft to publish.
5.  Then move it draft state and publish again.

 Expected behavior: The decision table should be published.

 Actual behavior: The decision table isn't published and the 'Could not update the decision table' message is displayed.

</td></tr><tr><td>

Developer Sandboxes

 PRB1952880

</td><td>

Upgrading a sandbox instance could result in loss of work in a sandbox

</td><td>

When a sandbox instance is upgraded, all sandboxes are destroyed, which could result in loss of work if the user hasn't saved off their work from the sandbox yet.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1636956

 [KB1224543](https://hi.service-now.com/kb_view.do?sysparm_article=KB1224543)

</td><td>

Perform Refresh Member accounts discovery is stuck in active state because of service\_account\_reload system commands in ECC queue

</td><td>

This is not related to the **Refresh Member Accounts** UI action. 'Perform Refresh Member accounts' is triggered by Cloud Schedule when glide.discovery.cdu.auto\_refresh\_sub\_accounts\_and\_ldcs is set to 'true'.

</td><td>

Refer to the listed KB article for details.

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

Discovery

 PRB1919668

 [KB2588245](https://hi.service-now.com/kb_view.do?sysparm_article=KB2588245)

</td><td>

Error during new certificate request creation for letsencrypt

</td><td>

Discovery's Business Rule 'Discovery - Update status started count' runs for ecc\_queue output inserts that are not actually from Discovery. This causes an error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1946099

</td><td>

AWS Cloud schedules are not working as expected

</td><td>

Cloud discovery Schedule did not update MID selection configuration properly.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1964303

</td><td>

Remove windows path from 'configuration console' on base instance

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1942585

</td><td>

Straight-through processed documents with tables will generate an extra row of predictions if the use case is on a version older than 27.one

</td><td>

This issue occurs on a glide instance with Yokohama and has DocIntel Store app version 7 or later installed, for example, version 25.0. With a table key and has straight-through processing and autofill enabled, it is trained to have straight-through processing triggers. When the user submits a document that gets straight-through processed, there will be an extra empty row of extracted values.

</td><td>

 

</td></tr><tr><td>

Dynamic Scheduling

 PRB1925058

</td><td>

Dynamic scheduling issues from case tasks

</td><td>

An issue found in scenario two is that certain FSM work order tasks are not scheduled right after the last job.

</td><td>

Scenario one:

 1.  Enable dynamic scheduling.
2.  Enable 'Ignore travel' in both dynamic scheduling property and task.
3.  Enable the 'Onsite arrival' status in sm\_config.
4.  Enable 'Show log' in the dynamic scheduling property.
5.  Open a pending dispatch task.
6.  Select **Auto assign**.

 Expected behavior: The user sees all dynamic scheduling logs.

 Actual behavior: There is no log displayed, and there is error message logged in system log: 'DynamicSchedulingProcessor: \_populateTravelTimeForAgentWorkBlock ReferenceError: 'GlideDataTime' is not defined.'

 Scenario two:

 1.  Enable 'Auto assign' with interval immediate.
2.  Create work order task1.
3.  Assign task1 to agent1, with an estimated end time of 'one'.
4.  Create work order task2, which can only be assigned to agent1, and window start can only be after task1.expected\_start. This ensures task2 can only be dynamic scheduling assigned after task1 When task2 is in 'Draft' state.
5.  Select the **Qualified** UI action.

 Expected behavior: Task2 is assigned right after task1.

 Actual behavior: There is gap between task1 and task2, and the gap size is the task2 travel duration and task2 work duration.

</td></tr><tr><td>

Dynamic Scheduling

 PRB1951019

</td><td>

Dynamic scheduling doesn't assign tasks to agents

</td><td>

When the user runs dynamic scheduling, one agent's workblock appears in both the sorted and response sections. If the user assigns a second task to one of the agents that overlaps with the original task's time window, the task is not reassigned.

</td><td>

Scenario one:

 1.  Enable the following features:
    1.  Dynamic Scheduling
    2.  Workforce Optimization \(WFO\)
    3.  Territory Management
2.  Create a task with a short time window that's eligible for assignment to two agents.
3.  Create entries in wm\_agent\_schedule\_attribute\_plan for both agents.
4.  Ensure each agent has distinct start and end locations.
5.  Generate schedules for both agents.
6.  Make sure each agent is able to do the following within the defined schedule window:
    1.  Travel to the task location from start location.
    2.  Complete the task.
    3.  Return to their respective end locations.
7.  Run dynamic scheduling.

 Expected Behavior: The dynamic scheduling report shows sorted workblocks and a response section with workblocks for both agents.

 Actual Behavior: Only one agent's workblock appears in both the sorted and response sections.Scenario two:

 1.  Repeat steps one-six from Scenario one.
2.  Assign a second task to one of the agents that overlaps with the original task's time window.
3.  Run dynamic scheduling.

 Expected Behavior: The pending dispatch task is assigned to the other agent.

 Actual Behavior: The task is not reassigned.

</td></tr><tr><td>

Email Notifications

 PRB1950667

 [KB2572580](https://hi.service-now.com/kb_view.do?sysparm_article=KB2572580)

</td><td>

The **Apply** button is not found in the Apply Email Templates icon in CSM Workspace

</td><td>

When 'Compose email' is used and the **Apply email template** icon is selected in a Case record, the **Apply** button is not visible for email templates that contain a large body.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Email Notifications

 PRB1960674

</td><td>

Create an email/email draft record creation script include in the global scope

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1970015

</td><td>

The Sparkle icon hides text in the email composer

</td><td>

It shouldn't hide text.

</td><td>

1.  Open the email composer.
2.  Generate text using Email recommendation skill.
3.  Place the cursor in between a sentence, the sparkle hides the text in the editor.

 Expected behavior: The NACM Sparkle is positioned at the bottom of the cursor so that it doesn't hide text.

 Actual behavior: The Sparkle icon hides text in the email composer.

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB1967663

</td><td>

API for attaching CBS taxonomy to Employee Center portal

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Enterprise Architecture

 PRB1945436

</td><td>

When creating a business application, the model\_id is set to 'Unknown'

</td><td>

The business rule 'Populate Application Model' is skipped.

</td><td>

Create a new business application \(cmdb\_ci\_business\_app\).

 Observe that the model\_id is set to 'Unknown'.

</td></tr><tr><td>

Event Management

 PRB1927888

</td><td>

Make date selection more flexible to improve PRC data selection performance

</td><td>

The CR selection should support the actual start date in addition to the change time. Use a single joined query with a filter instead of two separate queries.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1939564

</td><td>

If there is a change request on the same CI as in the alert, the reason for the PRC should always be 'Change on CI'

</td><td>

Even if the change request is on the same CI as in the alert, the reason for the PRC is 'Change on application service'. Instead, the reason for the PRC should be 'Change on CI'.

</td><td>

1.  Add application service \(S1\).
2.  Add a change request \(CR\).
3.  Make S1 a configuration item of the CR.
4.  Add S1 as an impacted service of the CR.
5.  Send an alert to S1.

</td></tr><tr><td>

Event Management

 PRB1953971

</td><td>

There are two columns named 'text' in the table sa\_agg\_alert\_filter, but one of them should be network\_traffic

</td><td>

The table is 'Network Traffic', but the column name is 'text', so there is no separated flag for network traffic.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1954172

 [KB2615509](https://hi.service-now.com/kb_view.do?sysparm_article=KB2615509)

</td><td>

Automated group is created even if some of the alerts does not match aggregated alerts filter

</td><td>

Defined alert aggregation filter sa\_agg\_alert\_filter is not working and alerts are still grouped.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Field Service Scheduling

 PRB1949408

</td><td>

Incorrect Google travel duration when number of locations exceed matrix\_size

</td><td>

The GoogleMapRestConstants.STANDARD\_MATRIX\_SIZE = ten and GoogleMapRestConstants.PREMIUM\_MATRIX\_SIZE = 25.

</td><td>

1.  Configure a Google key.
2.  Ensure there is no Google error.
3.  With a standard account, create more than ten src and destination locations.

With a premium account, create more than 25 src and dest locations.

4.  Run the background script.

 Notice that the first call has all elements in resourceLocations and taskLocations, and the second call only has the first element from each array. The result should be the same for the same pair of src/destination.

</td></tr><tr><td>

Flow Engine

 PRB1913968

</td><td>

High query count on sys\_flow\_record\_trigger

</td><td>

 

</td><td>

Flow triggers run queries repeatedly for tables that have any flow trigger defined.

</td></tr><tr><td>

Flow Engine

 PRB1923566

 [KB2489703](https://hi.service-now.com/kb_view.do?sysparm_article=KB2489703)

</td><td>

Yielding to the high priority flows feature causes several issues

</td><td>

Pausing should only occur before a flow element has started executing. If a pause occurs during the execution of a flow element, then it will cause an error for the cursor location and reporting.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1954872

</td><td>

Subflow is not fetching the location from the HR profile

</td><td>

This issue occurs when running the AI Agent Integration Gateway Wrapper.

</td><td>

1.  Log in as an admin.
2.  Open Workflow Studio.
3.  Run the AI Agent Integration Gateway Wrapper.

 Observe that there is an error in fetching the location from HR profile.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1918469

</td><td>

There's error checking availability for a flow recommendations skill

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1938123

</td><td>

Flows using base instance actions related to the plugin 'Customer Service Spoke' fail after upgrading to Yokohama

</td><td>

The flows in question are base instance actions related to 'Customer Service Spoke': Add Work Note to Task and Add Comment To Task.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1962584

</td><td>

The 'Skill Config' drop-down list doesn't load for the action\_designer role

</td><td>

The 'Skill Config' drop-down list doesn't load for the flow\_designer and action\_designer role.

</td><td>

1.  Create a flow.
2.  Add an action.
3.  Add a step called Now Assist Skill.

 Notice that the 'Skill Config' drop-down list doesn't load for the flow\_designer and action\_designer role.

</td></tr><tr><td>

Granular Delegation

 PRB1914000

</td><td>

Adhoc Granular Delegation intermittently doesn't work

</td><td>

This issue only happens when the delegation rule condition is added on the child table of the task field, which is added on the delegation rule.

</td><td>

1.  Activate the Granular Delegation plugin.
2.  Create the delegation rule table on the change\_request table.
3.  Choose the second step table.
4.  Set the filter to active = true.
5.  Select the **Assignments** and **Approvals** check boxes.
6.  Log in as an admin.
7.  Navigate to **All** &gt; **change\_request.list**.
8.  Create a new change request \(Normal\) with the Assignment group as 'Hardware'.
9.  Assign it to a user.
10. Change the state of the change request to 'Assess'.
11. Impersonate the user Abraham Lincoln.
12. Navigate to **All** &gt; **Employee Center**.
13. Select **My Tasks**.
14. In the Open Tasks list, find the newly created change request.
15. Select **Delegate this task**.
16. Delegate it to the user Abel Tuter, with the start date as yesterday and the end date as tomorrow.

 Expected behavior: The UI shows the task as delegated to Abel Tuter with an option to edit.

 Actual behavior: The user sees a 'Success', but the UI still shows the 'Delegate this task' link.

</td></tr><tr><td>

HR Integrations

 PRB1967664

</td><td>

Deactivate all existing notifications

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery Case Management

 PRB1967665

</td><td>

Deactivate all existing notifications

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1955210

</td><td>

The TR Catalog Item in Workspace is missing fields in Reimbursement

</td><td>

The second part of the TR flow requires the employee to create a new case, filling out a new catalog item.

</td><td>

Navigate to HR cases table \(Workspace/ UI16\) as an HR agent and select **New**.

 Observe that the fields shown in the UI are Tuition Reimbursement pre-approval fields.

</td></tr><tr><td>

HR Service Delivery

 PRB1956115

</td><td>

AIA cannot access the HR agents unless the attached RCAs are allowed

</td><td>

RCAs are created while running HR AI Agents with a recent release of NAP. Check if these RCAs have already been added by someone before adding.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1964158

</td><td>

New RCAs for Predict and transfer workflow

</td><td>

With the new changes for similar records from GAF, there are new RCAs to be included for Predict and transfer workflow work properly.

</td><td>

 

</td></tr><tr><td>

HTTP Client

 PRB1959206

</td><td>

Introduce Mechanism to Set Connection Pool Timeout on the Instance to Prevent Semaphore Exhaustion

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Identity

 PRB1949855

</td><td>

The 'system' user is not allowed to modify scripts because of missing snc\_required\_script\_writer\_permission role

</td><td>

Batch jobs and async bus.rules that are running as 'system' are not allowed to modify scripts if using Rest APIs or GlideRecordSecure.

</td><td>

 

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

 Notice that incident is closed for linking and the ACL blocks the writing of the record.

</td></tr><tr><td>

Incident Management

 PRB1958480

</td><td>

After selecting the **New** button, the user is navigated to a new incident record form where the caller file gets auto-populated with the logged in user name

</td><td>

When the user selects the search icon on a field, nothing happens.

</td><td>

 

</td></tr><tr><td>

Integration Authentication

 PRB1960124

</td><td>

Verbose JWT logs use opaque tokens when AuthLog is enabled

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1905216

 [KB2601538](https://hi.service-now.com/kb_view.do?sysparm_article=KB2601538)

</td><td>

Base instance script includes have duplicate names

</td><td>

The following script includes have duplicates: RestStepMultipartUtil \(Package - ServiceNow IntegrationHub Action Step - REST\), and RestStepFormUrlEncodedUtil \(\(Package - ServiceNow IntegrationHub Action Step - REST\)\).

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Integration Hub

 PRB1960313

</td><td>

True up changes for the WDF Tokenization Dashboard

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1923432

</td><td>

ScopedKMFModuleKeyImporter\#jsFunction\_createRequest API should be in global scope

</td><td>

This issue impacts some Zurich and Yokohama instances.

</td><td>

1.  Log in to datacentertest.
2.  Get the admin access request.
3.  Navigate to **Service Catalog.**
4.  Open the 'Create User Level Crypto Module' catalog.
5.  Select a user who has Zurich and Yokohama instances.
6.  Order the request.
7.  Open the Request Item.
8.  Open the Work Flow item for the request.
9.  Wait until the workflow is executed.
10. Open the u\_customer\_level\_module\_log table.

 Notice that the key exchange request creation failed for some Zurich and Yokohama instances where the global scoped evaluator fix was available.

</td></tr><tr><td>

Knowledge Management

 PRB1956227

</td><td>

The 'Known Error' template preview shows incorrect data in Knowledge Center interceptor for Knowledge, Knowledge Manager and ITIL role

</td><td>

The preview section displays incorrect data for the 'Known Error' template in any Knowledge Base.

</td><td>

1.  Impersonate a Knowledge, Knowledge Manager, or ITIL role user.
2.  Navigate to **Now** &gt; **Knowledge-center** &gt; **kb\_interceptor**.
3.  Select any Knowledge Base in the first column.
4.  Select the **Known Error** article template in the second column.
5.  Observe the preview panel.

 Expected behavior: The preview section should display accurate 'Known Error' template data corresponding to the selected Knowledge Base and template.

 Actual behavior: The article template preview section shows incorrect data for the 'Known Error' template type across any selected Knowledge Base.

</td></tr><tr><td>

Knowledge Management

 PRB1962920

</td><td>

Version bump for KC and ECE in anowassist and Zurich track

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Licensing Entitlement Engine

 PRB1952965

</td><td>

Long-term fix for the Licensing Engine Job out of memory issue related to the unconfirmed user's logic

</td><td>

 

</td><td>

1.  Provision an instance with over 500,000 user\_has\_role records and over 100 sys\_group\_has\_role records.
2.  Run the LE job.

</td></tr><tr><td>

Lifecycle Events

 PRB1951272

</td><td>

sn\_hr\_le.use\_flow property may be reset to 'true' after upgrade

</td><td>

A fix script update does not cause a 'sys\_update\_xml' record to be written for the property, so the property will be reset back to 'true' after the next upgrade or plugin repair.

</td><td>

1.  Create WDC build.
2.  Install HR Core, HR LE.
3.  Upgrade to Yokohama.

Notice that the use\_flow property was updated to false.

4.  Upgrade to Zurich \(or just repair the plugin\).

 Notice the use\_flow property is now true again.

</td></tr><tr><td>

Lifecycle Events

 PRB1956890

</td><td>

User evaluation against audience on activity fails during rescind

</td><td>

This occurs because from the BR: Rescind Case Cleanup flow, 'current.subject\_person' is passed, which is considered a reference record in the initial flow \(Activity Launcher\).

</td><td>

1.  Create HR Criteria and add conditions on HR Profile \(on Any column and set user field on condition\)
2.  Create **Audience,** set the Audience Type = HR Criteria, and add the Criteria from Step 1.
3.  Make sure to add the created Audiences in Any Activity from Rescind Activity Set.
4.  Create a **New Hire Onboarding** case with subject person \(the person must pass the conditions in HR Criteria\).
5.  Make the case Ready for work and Assign this Case to an Agent.
6.  Impersonate as Agent.
7.  Navigate to the case and start work.
8.  After sometime select **Rescind**.
9.  Open the SubFlow: Evaluate Audience and open Recent executions.

 Observe that Flow Expects userID \(Subject\_person sys\_id\) as a string but instead gets Subject\_person GlideRecord. This subFlow later calls a method to evaluate subject\_person against Audience which also fails and gives the wrong result because of this.

</td></tr><tr><td>

List Administration

 PRB1932331

</td><td>

Word wrap doesn't work for NRLC list

</td><td>

Content in the **Short Description** field does not break into new lines when line breaks are added.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1971195

</td><td>

Events are not being created through the MID server post Zurich upgrade due to a weak password in the previous instance

</td><td>

When the MID server upgrades or restarts, the Web Server extension initiates. MID then attempts to clear an error message in the MID web server context, which in turn triggers the password validation logic. If the existing password \(which might be years old\) is 'weak', the Business Rule executes current.setAbortAction\(true\), and the update is rejected.

</td><td>

 

</td></tr><tr><td>

Mobile Studio

 PRB1974465

</td><td>

Mobile AI Builder \(id = sn\_maib\) plugin oob\_apps/now-mobile-ai-builder.properties should have mode = optional to ensure it is not installed out of the box

</td><td>

Mobile AI Builder \(id = sn\_maib\) is installed as it is marked as mode = core in oob\_apps/now-mobile-ai-builder.properties.

</td><td>

 

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

 PRB1930438

</td><td>

MFA can be bypassed by users who should be required to use MFA

</td><td>

A user required to use MFA when logging in using username/password can log in without SSO and bypass MFA.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB1972473

</td><td>

MMS Plugin reads from the wrong key in response JSON

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB1972984

</td><td>

Build Multimodal Glide Service to support AIS multimodal document search

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB1973035

</td><td>

PPT type documents not sent to MMS

</td><td>

No record is queued up for processing.

</td><td>

 

</td></tr><tr><td>

Multimodal Service \(Family Channel\)

 PRB1973355

</td><td>

Attachments linked to Child Tables of KBS \(for example, kb\_template\_faq\) are not sent to MMS

</td><td>

No record is queued up for processing.

</td><td>

 

</td></tr><tr><td>

Now Assist in Document Intelligence

 PRB1931082

 [KB2554900](https://hi.service-now.com/kb_view.do?sysparm_article=KB2554900)

</td><td>

Excessive Assist usage due to 'Attachment Summarization' skill

</td><td>

There is higher-than-expected 'assists' consumption due to a defect in the 'Trigger Attachment Summarization' Business Rule.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now Assist Panel

 PRB1952614

</td><td>

Auto scroll does not work in Virtual Agent on NASS

</td><td>

Auto scroll doesn't work after creating a new catalog item.

</td><td>

1.  Log in to a znowassist instance.
2.  Select **Create a new catalog item**.
3.  Select **Continue**.
4.  Select **Default item template** from the list on the left.
5.  Select **Use this item template** after it is enabled.
6.  Select **Build** after it is enabled.
7.  Enter 'book a cab' in the input box in VA.
8.  Select **Send**.
9.  Type 'add' after input is enabled.
10. Select **Send**.
11. Enter 'add' after input is enabled.
12. Select **Send**.
13. Enter 'add' after input is enabled.
14. Select **Send**.

 Observe that auto scroll does not work.

</td></tr><tr><td>

Now Assist Panel

 PRB1963927

</td><td>

While or after streaming, the user can see chat client jumpiness

</td><td>

The avatar of dynamic loader message is hidden at first, then shows up. Also, the scrollbar sometimes scrolls to the top and then down to the bottom.

</td><td>

1.  Enable streaming for one assistant, either NAP or portal.
2.  Make sure collapse\_processing\_message is true for this assistant.
3.  Ask a question like 'what is spam'.

 Observe that the avatar of dynamic loader message is hidden at first, then shows up. This causes part of the jumpiness. The avatar should always show up if collapse\_processing\_message is true. While or after streaming, the scrollbar sometimes scrolls to the top and then down to the bottom, which also causes jumpiness. This shouldn't happen and content should scroll smoothly.

</td></tr><tr><td>

Now Assist Panel

 PRB1965617

</td><td>

Legacy NAP doesn't load upon upgrade

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1971138

</td><td>

No tags are passed from the Now Assist Panel

</td><td>

When NAP is queried, the user is not getting the correct response and no records are displayed even when the data exists.

</td><td>

 

</td></tr><tr><td>

Now Assist Platform

 PRB1955495

</td><td>

Gen AI Feature Mapping table's Feature Name column is not translated

</td><td>

Upon turning on the system localization property, 'Displays translation prefix on translatable strings' from 'System Properties', the column 'Feature Name' is not translated in the 'sys\_gen\_ai\_feature\_mapping' table. The 'Feature Name' is displayed in the AI Engagement Analytics dashboard, but the 'Feature Name' is not translated.

</td><td>

 

</td></tr><tr><td>

OAuth

 PRB1962299

</td><td>

Error in logs: com.glide.script.RhinoEcmaError: 'FlowRecommendationsSkillCheck' is not defined

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1959519

</td><td>

Add a new header to indicate in-country routing requirement

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1966057

</td><td>

Disable incident summarization cache to enable logging usage and assists

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1966097

</td><td>

Duplicate Service Plan records are created

</td><td>

sys\_one\_extend\_usage contains a cached reference to a service plan record. If that service plan is deleted it can lead to duplicate service plan creations and potentially cause functional issues.

</td><td>

1.  Run any Generative AI capability.
2.  Verify that there's a new entry in sys\_one\_extend\_usage table with a valid service plan \(one\_api\_service\_plan\).
3.  Delete that service plan.
4.  Re-run the same capability.
5.  Check the sys\_one\_extend\_usage table again.

 Expected behavior: A new sys\_one\_extend\_usage cache record and a new service plan is created but the sys\_one\_extend\_usage record with the empty plan is deleted.

 Actual behavior: A new sys\_one\_extend\_usage cache record and a new service plan are create, but the sys\_one\_extend\_usage record with the empty plan is still there. This can cause potential issues since the code may keep picking up the stale service plan.

</td></tr><tr><td>

OneExtend

 PRB1972356

</td><td>

Provide flexibility to allow the users to provide feedback on the responses generated from Now Assist Skill execution

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1972976

</td><td>

One Extend capability is unable to pass the variable value from one capability to another capability in Capabilities chaining

</td><td>

Users notice that the One Extend chaining fails at the size 9001502.

</td><td>

Execute the RAG chaining from background scripts.

 Notice that in the background script, the result shows one API exception with an exception message.

</td></tr><tr><td>

OneExtend

 PRB1973586

</td><td>

A newly changed LLM provider setting is reset after upgrading

</td><td>

After upgrading an instance to Zurich but not upgrading Generative AI Controller and Now Assist Admin apps to the compatible latest available versions, the LLM provider setting reverts to its pre-upgrade value within two hours or less after being changed through the 'Edit Model Provider' option in Now Assist Admin. This behavior may cause configuration instability after the upgrade.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1974084

</td><td>

Error during zboot due to a 'where' clause on sys\_db\_view\_table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Performance Analytics API

 PRB1917953

 [KB2703941](https://hi.service-now.com/kb_view.do?sysparm_article=KB2703941)

</td><td>

Analytics Center doesn't have guardrails in its NLQ Service, causing Java heap space out-of-memory errors

</td><td>

An NLQ with the combination of 'AC' and an empty 'table' parameter is fired, leading to excessive scans across the instance and eventually causing an out of memory error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Performance Analytics API

 PRB1966859

</td><td>

All visualizations stop loading when sn\_nowassist\_skill\_config\_status is not available on the instance

</td><td>

The table sn\_nowassist\_skill\_config\_status comes from com.sn\_nowassist\_admin, which is a base instance plugin and comes with Glide. However, during instance upgrades, this table is removed by an unknown process. This causes API queries to get the AI skill statuses within the Data Visualization API to encounter Null Pointer Exception. As a result, all visualizations are not rendered properly.

</td><td>

 

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB1832437

</td><td>

The count for DASHBOARD\_LAYOUT jumps significantly upon page refresh

</td><td>

The DASHBOARD\_LAYOUT cache count increases even when the same dashboard is refreshed.

</td><td>

1.  Log in as a user with elevated privileges.
2.  Navigate to **Performance Analytics** &gt; **Library** &gt; **Dashboards**.
3.  Open /cache\_inspect.do in another tab.
4.  Clear the cache in this tab.
5.  Open any dashboard \(for example, Incident Management\) in the first tab.
6.  Notice that the DASHBOARD\_LAYOUT cache only increases by one in the cache\_inspect.do tab.
7.  Refresh the dashboard tab.

 Notice that the DASHBOARD\_LAYOUT cache increases in count even when the same dashboard is refreshed.

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB1906120

</td><td>

User preferences \(com.snc.par.dashboards.UI.preferences\) are never cleared and causing out of memory errors and node restarts

</td><td>

'WARNING \*\*\* WARNING \*\*\* error processing REST data broker: Exception while executing request: Java heap space...'.

</td><td>

1.  Navigate to an instance.
2.  Open the dashboard.
3.  Select **Filter** &gt; **Assignment group**.
4.  Wait for a couple of seconds and navigate to **User Preferences**.

 Observe that the latest preference has large text and lot of applies to values in JSON.

</td></tr><tr><td>

Performance Telemetry

 PRB1963832

</td><td>

Telemetry is not initializing for production instances

</td><td>

Telemetry is not initialize and metrics are not exported.

</td><td>

1.  Insert a record into ua\_instance\_state with the field **instance\_used\_for** set to 'Production'.
2.  Ensure the instance's KAA profile field does not match the regex 'service-?now.\*'.
3.  Restart the instance.

 Notice that the instance does not export any metrics.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1934435

</td><td>

Dashboard view count doesn't update for Core UI dashboards

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1948336

</td><td>

Option to disable 'Welcome to Platform Analytics' pop-up / modal for migrated dashboards

</td><td>

When a Responsive Dashboard is migrated to PA dashboard, a pop-up / modal is shown to all users accessing the migrated dashboard: 'Welcome to the Platform Analytics experience'.

</td><td>

1.  Migrate responsive dashboards to PA.
2.  Navigate to the migrated dashboards.

 Notice that a 'Welcome to the Platform Analytics experience' pop-up is shown for all migrated dashboards and all users. If the users selects **Do not show this message again...** the pop-up will not be shown for that specific dashboard but for all other migrated dashboards.

</td></tr><tr><td>

Platform Analytics Component API

 PRB1952208

</td><td>

The dashboard list doesn't display and can't filter properly

</td><td>

The Dashboard Library on Platform Analytics \(Zurich\) generates an invalid query when any of the built-in filters are used and thus generate no queries due to the sys property glide.invalid\_query.returns\_no\_rows being set to true.

</td><td>

Navigate to **Platform Analytics** &gt; **Dashboards**.

 Notice that when 'Filter active' is true, no records are displayed even when there are numerous active dashboards. Using any filters removes all records from the list.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1905382

</td><td>

Dashboard tab names do not have unique keys for translations in a sys\_translated table

</td><td>

CoreUI dashboard tab names contain sysId of the pa\_tab record then sometimes a BEL char then the string. But PAE dashboard tab name does not have this sysId prefix.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1909232

</td><td>

Platform Analytics Dashboard can't be saved due to colliding components that have the same positions

</td><td>

Performance Analytics Reporting dashboard can't be saved if multiple components are colliding. An error occurs in the logs.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1936902

</td><td>

Saving changes to Library is not working as expected in the Platform Analytics Dashboard

</td><td>

In dashboard A, a saved visualization \(visualization one\) is added as an element and the visualization is also added to the dashboard B. Visualization one in dashboard A has been unlinked from the library and the same visualization has been added as new element \(visualization two\) to dashboard A. When a change is made to the visualization in dashboard B and the changes are saved to library, the changes are not reflected in visualization two of the dashboard A, even though the change is reflected in the visualization in the visualization designer. It should reflect the change as 'Save changes to library' to indicate that the change is saved to the library so that when it is reused, the change would be reflected. This issue is found in Yokohama.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1946249

</td><td>

User with the 'snc\_external' role is unable to see choice values for filters in a Performance Analytics Reporting \(PAR\) dashboard

</td><td>

When selecting the filter, it doesn't load the choices and gets stuck at loading.

</td><td>

1.  Open any Yokohama instance.
2.  Install the Customer Service Management plugin package.
3.  Create a new sample 'sys\_user' record.
4.  two. Assign below roles to the new user:
    -   snc\_external gets assigned as part of the inheritance
    -   sn\_customerservice.case\_viewer
    -   sn\_customerservice.user
    -   sn\_customerservice.customer\_admin.
5.  Create a Test Experience in UI Builder \(UIB\) with the roles snc\_external and snc\_internal.
6.  Create a simple page on this experience.
7.  Add a filter on it. For example, the filter can be created on any field of 'sn\_customerservice\_case' table.
8.  Impersonate the new user.
9.  Access the UIB experience page.
10. Open the filter.

 Notice that the element stays loading and the choices are not displayed.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1954949

</td><td>

Dashboard is duplicated when first opened if the user is in different domain

</td><td>

The dashboard is duplicated when is duplicated in another domain with the domain separation plugin.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1964706

</td><td>

Errors found in a system log caused by daily automated list

</td><td>

After upgrading to Zurich, system log entries show below errors every day at 08:00 related to the automatic migration of List - Simple to Analytics List.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1967567

</td><td>

Widgets inside the group are reordered when the dashboard is modified

</td><td>

Widgets are reordered.

</td><td>

1.  Open any existing dashboard with group.
2.  Modify the dashboard.
3.  Once saved, observe the position of the widgets inside the group.

 Expected behavior: Widgets in the group should remain in the same position.

 Actual behavior: Widgets are reordered.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1970055

</td><td>

Remove 'formVizDesigner' parameter from PARVisDesignerVisualizationQuery

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Filters

 PRB1900864

</td><td>

Filter loads the same string entry multiple times

</td><td>

This occurs because the filter has pagination logic and there is de-duplication logic in the API.

</td><td>

1.  Select a model in the 'Model' filter.
2.  One model is set, open the 'Input field' filter.

 Expected behavior: only a few unique choices should be available.

 Actual behavior: Multiple GraphQL calls occur and many repetitive choices are displayed.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1935002

</td><td>

When upgrading to Yokohama, the initial screen shows the **Start moving** button in the Migration Center

</td><td>

 

</td><td>

1.  Create an instance on Washington DC Migrate.
2.  Activate Next Experience.
3.  Verify that the Migration Center page shows the **Take me to library** button.
4.  Upgrade to the Yokohama release.

 Notice that the Migration Center screen resets back to initial state with the **Start moving** button.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1936887

</td><td>

Dashboard redirection is incorrect for the user if the dashboard is migrated from the library by admin/analytics manager and not activated

</td><td>

The user observes a message that the dashboard has been migrated to Next Experience or is redirected to a random dashboard.

</td><td>

 

</td></tr><tr><td>

Playbook Experience Core

 PRB1952214

</td><td>

The 'Restart' stage doesn't show up until page reload and restart playbook DA still shows when playbook is complete

</td><td>

'Restart activity' DA is displayed.

</td><td>

1.  Create/update the playbook and enable 'Allow this playbook to be restarted during runtime' to enable playbook restart.
2.  Set up the restartable option for at least one playbook stage.
3.  Navigate to the playbook workspace demo and trigger the playbook.
4.  Complete the playbook.
5.  Navigate to sys\_pd\_context and archive the playbook record.
6.  Navigate to the playbook workspace demo and refresh the page.

 Expected behavior: Restart activity DA is not displayed anymore.

 Actual behavior: Restart activity DA is still displayed.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1936566

</td><td>

On a Playbook Duplicate the Deferred Evaluation Point still refers to the original playbook activity

</td><td>

The user doesn't see the Evaluation Point after the activity and in the modal, and the activity field is empty.

</td><td>

1.  Create a playbook and set the Evaluation Point.
2.  Create a duplicate playbook out of it.

 Expected behavior: The user sees the EP and in modal should see the activity.

 Actual behavior: The user doesn't see the EP after the activity and in the modal, and the activity field is empty.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1936766

</td><td>

Playbook properties don't auto-select after a guided setup upgrade or re-publish

</td><td>

The existing playbook context is canceled, but a new playbook does not re-trigger unless the 'Trigger on unique change' checkbox is manually enabled. BUs cannot view the updated changes without manually selecting the playbook properties.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1965465

 [KB2674332](https://hi.service-now.com/kb_view.do?sysparm_article=KB2674332)

</td><td>

Snapshot clean up job doesn't work when there are restricted caller access requests

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Problem Management

 PRB1930428

</td><td>

Problem coordinators can't associate closed incidents to problems in Service Operations Workspace \(SOW\)

</td><td>

Problem coordinators can't associate closed incidents to problems in SOW due to a change in the script include 'related\_list\_edit\_helper' from using GlideRecord to GlideRecordSecure. The MRA in the workspace lists closed incidents for linking, but then ACLs block the writing of the record. This is not the case in UI16, as it uses a different script include.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1933335

</td><td>

Worknotes clusters have stop words in the result

</td><td>

Cluster concepts have stop words in the results.

</td><td>

1.  Initiate Work notes analysis without Gen AI.
2.  Select **View results** once scheduled tasks complete.

 Expected behavior: The cluster concepts should not have stop words defined in default English stop words.

 Actual behavior: The cluster concepts have stop words in the results.

</td></tr><tr><td>

Process Mining

 PRB1945720

</td><td>

Mining Agentic AI Tasks

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1938591

</td><td>

Deleting a Parent Project Task with a Child Project Task does not record the Child Project Task in Audit Deleted Records \(sys\_audit\_delete\) and Rollback Sequences \(sys\_rollback\_sequence\) in Project Workspace

</td><td>

Deleting a Parent Project Task with a Child Project Task does not record the Child Project Task in Audit Deleted Records \(sys\_audit\_delete\) and Rollback Sequences \(sys\_rollback\_sequence\) in Project Workspace. The Child Project Task should be audited. This occurs with other related tables as well, and not just the project task table.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1940869

</td><td>

Cost plans aren't visible in the EAC widget for the role it\_project\_manager

</td><td>

Only actuals are visible in the EAC/forecast widget. Planned cost values aren't considered, so the widget shows the incorrect value. An error message also appears.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1961677

</td><td>

When editing the 'Resource rate' and 'Rate override' for the parent RA, it is not reflected in the child RA

</td><td>

A few issues were observed. In scenario one, editing the 'Resource rate' and 'Rate override' for the parent RA, it is not reflecting to child RA. In scenario two, when the project start date is changed to Sunday, the Sync resources option is not updating the RA start date to the next working day and the icon keeps showing. In scenario three, changing the date prior to the task start date shows error message in the platform but not in the RMW grid inline edit.

</td><td>

 

</td></tr><tr><td>

REST API Framework

 PRB1951838

</td><td>

Enhance CSRF violation logging

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

 PRB1968390

</td><td>

AI Agent tool is unable to generate RCAs and GlideScopedEvaluator is not honored

</td><td>

When an AI Agent tool in 'scope x' accesses a table from a different 'scope y', the tool in 'scope x' is unable to access the scope of the table in 'scope y'.

</td><td>

 

</td></tr><tr><td>

Scheduled Jobs

 PRB1941198

</td><td>

Slow query when JobExecutor is updating status

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1959121

</td><td>

Schedule Optimization with Dependent task is not running

</td><td>

Empty string values for crew in territory\_membership table and missing schedules for crews, resulting in an error during graphql calls.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1959246

</td><td>

Logging inconsistencies for prioritized optimization

</td><td>

Message prefix for job ID is not properly set for some messages during PO run, causing messages to not appear when selecting **Show log entries** on the Intraday Job form.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1964665

</td><td>

Fix optimization errors and inconsistencies

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1968292

</td><td>

Tasks are not assigned even though ML Predictor results say that a task should be assigned

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Seismic Framework

 PRB1961401

</td><td>

Add a header to identify requests originating from sn-HTTP-request

</td><td>

There is unnecessary noise in the CSRF violation logs.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1960493

</td><td>

Regexp regression in invalid unicode sequences

</td><td>

When running gs.info\('about'.replace\(/\[\\u\]/g, '\\\\u'\)\). in background scripts, it should print 'about' in legacy and es5 scopes, and 'abo\\ut' in es\_latest scopes.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1972229

</td><td>

Static analysis for sandbox security

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1972733

</td><td>

Field translations for security integrations are failing and return a null value

</td><td>

The field translations aren't working. On changing the field evaluator.withEnforcedSecurity\(false\), field translations work as expected.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1974676

</td><td>

Guest sandbox logging has the potential to overwhelm system logs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1974683

</td><td>

Rules for static analysis feature are locked behind no\_db\_override

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1957018

</td><td>

CSS Styling / variable behavior issues in Zurich

</td><td>

In Service Portal catalog items, a random white pixel appears next to some fields. Specifically this is originating from the style sheet css\_includes\_$sp.CSS?v=6f2f28fbc3747210df5db512b401317e.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1963662

</td><td>

The 'Choose how to build' page preserves the old state

</td><td>

 

</td><td>

1.  Navigate to any Zurich instance.
2.  Navigate to catalog builder and try to edit an item with published reference.
3.  On the 'Choose how to build' page, edit with Now Assist will be readonly.
4.  Navigate back to the home page and try to create a new item.

 Expected behavior: It should be selectable for new items.

 Actual behavior: The 'Choose how to build' page preserves the old state 'Create with now assist' still read only.

</td></tr><tr><td>

Service Portal

 PRB1893333

</td><td>

After the first log in with MFA authentication, the user is redirected to the Platform UI page instead of the Portal page

</td><td>

The user lands on the platform page instead of the Service Portal page after MFA setup.

</td><td>

1.  Log in as a user with MFA enabled.

Notice that after a successful login, the user will be redirected to setup MFA.

2.  Complete the MFA setup.

 Expected behavior: The user is expected to land back on the Service Portal page.

 Actual behavior: The user lands on to the platform page.

</td></tr><tr><td>

Service Portal

 PRB1970008

</td><td>

When a dialog opens, immediate keyboard focus moves to the input field and VoiceOver announces the value only

</td><td>

Catalog variables are not visible for a standalone RITM when configured fields are less than or equal to six.

</td><td>

1.  Navigate to /sp.
2.  Open any RITM.

 Expected behavior: No matter the count of configured fields in the approval configuration table, all the catalog variables should be visible.

 Actual behavior: Catalog variables are not visible for a standalone RITM when configured fields are less than or equal to six.

</td></tr><tr><td>

Session Management

 PRB1916580

</td><td>

A deadlock is encountered at instance start-up involving GlideSession

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1954394

</td><td>

Attachment is not displayed in thread window side by side

</td><td>

An attachment is not displayed from a thread.

</td><td>

1.  Open a sidebar chat in WD.
2.  Open a thread view and upload an attachment in the thread.

 Expected behavior: The attachment should be uploaded displayed.

 Actual behavior: The attachment is not displayed from thread.

</td></tr><tr><td>

Software Asset Data Import

 PRB1967199

</td><td>

Invalid delete for contract import causes no records to be imported

</td><td>

An empty column 'A' is deleted when importing MLS documents. However, this deletion incorrectly occurs for contract imports as well.

</td><td>

1.  Initiate the contract analysis flow through SAM workspace by creating a software license contract and import a contract document.
2.  Once extraction completes, move to step 2.
3.  Select **Submit**
4.  Move to step 3.

 Expected behavior: Entitlements from the contract document should be processed and imported.

 Actual behavior: No entitlements are imported.

</td></tr><tr><td>

Software Asset Management Content Service

 PRB1966116

</td><td>

On-prem export does not have the capability to export content payloads filtered by content version

</td><td>

 

</td><td>

 

</td></tr><tr><td>

System Export Sets

 PRB1926120

</td><td>

Node errors due to messages sent when /Kafka is unavailable or slow

</td><td>

When /Kafka clusters are down or running slowly, LES can't check their health before sending messages. As a result, the producer client keeps retrying, and without any pause or queue in place, these repeated attempts can eventually push the node into an error state.

</td><td>

 

</td></tr><tr><td>

Table Rotation

 PRB1937356

</td><td>

The 'Truncate base table' job continues to run on the table even after it has been removed from Table rotation, regardless of whether the rotation exists or not

</td><td>

The 'Truncate base table' job is created by a business rule: 'Table Rotation: Clean Base Table' on the sys\_table\_rotation table and it's scheduled to run in the future when all the rotations are completed. The job is also scheduled in sys\_trigger and will have its next\_action set to the clean\_base\_rotation value. When rotation is removed, no one checks for this job. As a result, the scheduled job may still truncate data from the table based on the original clean\_base\_rotation timing, regardless of whether the rotation is there or not.

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1962239

</td><td>

When the territory model is active, the MP auto push events are generated endlessly

</td><td>

When the territory model is active and auto push in MP is enabled, duplicate auto push events are generated endlessly.

</td><td>

1.  Enable the territory model.
2.  Create WO and WOT.
3.  Make sure auto push is enabled and progressive push is disabled.
4.  Qualify the WOT to update the state from **Draft** &gt; **Pending dispatch**.

 Expected behavior: One event per WOT is created for auto push.

 Actual behavior: Duplicate auto push events are created endlessly.

</td></tr><tr><td>

Transaction Management

 PRB1965103

</td><td>

On 2GB nodes, a Unified Semaphore Pool exacerbates memory issues

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1965105

</td><td>

Reduce Memory Usage from DynamicHistogram

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1966462

</td><td>

FORKED\_TRANSACTIONS shows NaN for semaphore service\_saturation metric in /load\_stat.sdo

</td><td>

This causes the weighted load balancer to break its ability to parse the service saturation.

</td><td>

1.  Ensure that forked\_transactions are in sys\_semaphore\_set with max\_concurrency = 0.
2.  Navigate to instance\_url/load\_stats.do.
3.  Search the response payload for 'nan'.

 Expected behavior: No 'NaN' in the response payload, as this causes issues with Weight Load Balancer \(in the load balancer\).

 Actual behavior: There is a 'NaN' in the response payload.

</td></tr><tr><td>

UI Field Administration

 PRB1887661

</td><td>

Records are not being added based on the selected Configuration Class item

</td><td>

 

</td><td>

1.  Navigate to the SOW module.
2.  Open any Incident record.
3.  Select **Related Records** &gt; **Affected CI's** &gt; **Add**.
4.  Update the Configuration Class \(for example, change from Configuration Item to Software\).
5.  Select all the records and select the **Add** button.

 Observe that records related to the Configuration Item are added instead of the expected Software records.

</td></tr><tr><td>

UI Field Administration

 PRB1937530

</td><td>

Reference fields do not display correctly

</td><td>

When creating an incident using the **Create Incident** UI Action from a record page that uses UI Builder form components, reference fields may not display correctly.

</td><td>

1.  Navigate to Service operations workspace.
2.  Select the plus icon.

Notice that the interaction form page appears.

3.  Populate the below fields in the interaction form.
    1.  **Caller**: Select any caller.
    2.  **Configuration item**: Select any CI.
    3.  **Service**: Select any service.
4.  Select **Save**.
5.  In the interaction form view populate the **Short description** field and select **Create incident**.

 Notice in the incident workspace view under the assignment section that the configuration item field and service field are missing.

</td></tr><tr><td>

UI Field Administration

 PRB1941078

</td><td>

related\_list\_edit\_helper.processMRARecords doesn't apply contextual ACLs

</td><td>

This issue occurs after installing the Enterprise Asset Management plugin.

</td><td>

1.  Install Enterprise Asset Management plugin.
2.  Navigate to **Asset Workspace**.
3.  Create a pallet.
4.  Create asset.
5.  Log in as a technician.
6.  Select **Add assets**.
7.  Select an asset.
8.  Select the **Add on MRA** popup.

 Observe that the asset didn't get added.

</td></tr><tr><td>

UI Field Administration

 PRB1945077

</td><td>

Click-to-call ignores the E.164 country code and defaults to +one

</td><td>

The 'Click-to-call' feature is incorrectly dialing US numbers instead of international numbers such as the UK or India, regardless of the country code. Dialing from the contact card works correctly, but using the 'Click-to-call' icon always defaults to US numbers.

</td><td>

1.  Navigate to the CSM Workspace
2.  Open a Case record.
3.  Select the **Information** icon of the **Contact** field. The User account will open.
4.  Select the phone icon of the **Business phone** field

 An outbound call is placed, and an interaction record is created.

</td></tr><tr><td>

UI Field Administration

 PRB1959307

</td><td>

Notes text area does not auto expand when a new interaction/incident is created in Workspace

</td><td>

The Journal field work notes do not resize automatically as they did in previous versions.

</td><td>

1.  Open SOW.
2.  Notice the + icon in the workspace.
3.  Select new interaction/incident.
4.  Start typing until content exceeds the visible area.

 Notice that the text area is not resized and the user is unable to see the text written.

</td></tr><tr><td>

UI Form Administration

 PRB1935372

</td><td>

In Catalog Builder, UXF Notifications are rendered behind the client script or UI policy wizard modal

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1950676

 [KB2622641](https://hi.service-now.com/kb_view.do?sysparm_article=KB2622641)

</td><td>

Approval Summarizer formatter is not displayed after upgrade to Zurich

</td><td>

An issue has been identified after upgrading to Zurich with the Approval Summarizer formatter where the approval record doesn't display the summary of the item being approved.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1968060

</td><td>

Forms break when 'glide.UI.escape\_text' is set to false

</td><td>

An error occurs reading, 'The entity name must immediately follow the '&amp;' in the entity reference' and a blank page loads.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB1889948

</td><td>

The pop-up 'Edit box' UI is mispositioned when trying to edit a field by double selecting it on a hierarchical list

</td><td>

This issue is found in Washington DC, Xanadu, and Yokohama.

</td><td>

1.  Open a base instance.

2.  Navigate to the **change\_request** table.
3.  Enable the hierarchical list for this table.
4.  Open any change record.
5.  Add at least 20 records to the first related list on that change record.
6.  Return to the change list.
7.  Expand the hierarchical list for the same change record from step 2.
8.  Try to edit the 15th or later cell on that expanded list.

 Notice that the **Edit box**UI is mispositioned.

</td></tr><tr><td>

Upgrade Center

 PRB1927990

</td><td>

Full cache flush occurs during on-demand installations/upgrades, cause performance issues

</td><td>

 

</td><td>

1.  Select any store app with some dependencies which are also store apps.
2.  Notice that after each store app is loaded, all the caches are flushed and reloaded.
3.  Continue loading this on any instance with multiple nodes.

 Notice that a significant load on the database as all the nodes keep reloading all the caches.

</td></tr><tr><td>

User Authentication

 PRB1944133

</td><td>

There's a login page \(login.do\) presentation issue after a Zurich upgrade

</td><td>

There's a login page \(login.do\) presentation issue after a Zurich upgrade when changing the language to French.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1886937

</td><td>

Issue with QCO closing out without a selection

</td><td>

The QCO modal should stay open unless a select is initiated from outside of the dialogue box.

</td><td>

1.  Check out an item using QCO.
2.  In any free text box \(for example, 'Reason for Purchase'\), highlight the entered value without releasing the mouse button.
3.  Navigate outside of the dialogue box and release.

 Expected behavior: The QCO modal stays open unless a selection is initiated from outside of the dialogue box.

 Actual behavior: The QCO modal disappears and all info is lost.

</td></tr><tr><td>

UX Framework

 PRB1966606

</td><td>

Make UXF Caches Hard references to mitigate long build times from cache reclaims

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1962714

</td><td>

Date picker in AI agent doesn't have the option to skip it

</td><td>

 

</td><td>

1.  Create an AI agent that can collect the 'date'.
2.  Ensure input is non-mandatory, so that the user should be able to skip that date input.

 Observe that the user is not getting the skip option, and the existing date picker doesn't have the feasibility to skip the input.

</td></tr><tr><td>

Virtual Agent

 PRB1768573

</td><td>

Profanity filter keyword issues

</td><td>

Profanity filter keyword mode flags non-profane words that contain otherwise profane words.

</td><td>

 

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

 PRB1829786

</td><td>

A card response of type 'Small image with text' doesn't display the data on the card in Virtual Agent from Xanadu version

</td><td>

Output is not displayed in the card response. Instead technical names are displayed.

</td><td>

1.  Log in to a Xanadu instance.
2.  Navigate to VA Designer and open the TOPIC created
3.  Select the **Test** button without **Include in Topic Discovery** so that only that topic is tested.

 Notice that output is not displayed in the card response. Instead technical names are displayed.

</td></tr><tr><td>

Virtual Agent

 PRB1897152

</td><td>

Unexpected badge for an unread notification displays on the chat history icon after loading a citation and navigating back

</td><td>

The badge for unread messages displays on the chat history icon when there are no additional unread messages.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1899038

</td><td>

The bot text response script message is skipped if there is a space in the start of it

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Navigate to **Topic Designer**.
3.  Create a NLU/keyword topic.
4.  Add two text bot responses.
5.  Insert a blank line at the start of the script in the first response.
6.  Save and test the topic.

 Notice that the first text bot response is skipped.

</td></tr><tr><td>

Virtual Agent

 PRB1920893

</td><td>

Suggestion message is only displayed in French after English input

</td><td>

If the VA detects English input from a French profile, it suggests switching to English. However, the suggestion message is only displayed in French, not in both languages. It works correctly with an English profile and French input.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1921731

</td><td>

Post chat survey allows the user to switch topics

</td><td>

In an LLM conversation, the requester gets a live agent transfer message immediately before the conversation ends.

</td><td>

1.  Configure LLM conversation / assistant to have a post chat survey.
2.  Start an LLM conversation.
3.  Transfer to a live agent.
4.  As the live agent, accept the chat.
5.  As the requester, end the chat.

Observe that the post chat survey runs.

6.  Type an utterance that would trigger the live agent, or select the hamburger menu and transfer to a live agent.

 Expected behavior: Live agent option should not be available in the hamburger menu, and any utterance typed should not go through LLM and trigger topic switch.

 Actual behavior: requester gets a live agent transfer message, followed immediately by the conversation ending.

</td></tr><tr><td>

Virtual Agent

 PRB1927206

</td><td>

Sensitive data for agent chat does not work with URLs

</td><td>

Bad words for sensitive data aren't masked in URLs for agents.

</td><td>

1.  Add a regex within sensitive data detection.
2.  Navigate to **Now** &gt; **Conversation** &gt; **Settings** &gt; **Sensitive-data**.
3.  Enable the following options:
    -   Requester to agent
    -   Agent to requester
    -   Requester to Virtual Agent
4.  Log in to Yokohama in two sessions.
5.  Impersonate an agent.
6.  Set the agent as 'Available' in the workspace.
7.  Initiate chat in /sp.
8.  As an end-user, enter a URL containing a bad word.
9.  As agent type, enter a URL containing a bad word.

 Notice that from the agent side, the word is not masked when in URL.

</td></tr><tr><td>

Virtual Agent

 PRB1939062

</td><td>

Tracer breaks before a Teams response is sent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1939997

</td><td>

Non-actionable notifications in Virtual Agent aren't cleared when load\_active\_only is set to true

</td><td>

Non-actionable notifications in Virtual Agent appear to only get cleared when skip\_load\_history is true.

</td><td>

1.  Log in to a Yokohama instance.
2.  Impersonate an ITIL User.
3.  On one tab, navigate to incident.list.
4.  Assign any incident record to ITIL User.three. On another tab, navigate to /sp.
5.  Open the VA.

 Observe that the non-actionable notifications remain present.

</td></tr><tr><td>

Virtual Agent

 PRB1940559

</td><td>

Virtual Agent topic 'Check Case Status \(Template\)' stuck at '. . .' in the Virtual Agent Chat

</td><td>

There is an error in the log stating 'Script evaluation error at \[topic\_Check Case Status \(Template\)\_field\_your\_case\_enum\_list\]'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1940858

</td><td>

RITM/REQ isn't mapped to an interaction when a conversational catalog item is submitted

</td><td>

RITM/REQ isn't mapped to an interaction and the link isn't added to the transcript when a conversational catalog item is submitted.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1947698

</td><td>

Only one agentic workflow executes successfully when the same trigger fires simultaneously

</td><td>

When a workflow trigger fires simultaneously multiple times, only one of the resulting agentic workflows executes successfully. The other workflows terminate immediately with an error indicating that no session ID could be found. Each trigger correctly creates a new execution plan and a new conversation record, but only one conversation proceeds, while the others fail at the start.

</td><td>

1.  Create the agentic workflow named 'Test multiple case executions'.
2.  Select three or more case records.
3.  Update them simultaneously so that the trigger fires for all at once.
4.  Notice that the three execution plans \(sn\_aia\_execution\_plan\) and three conversation records are created. Only one conversation and execution plan executes successfully. The other conversations don't continue after the first task with the error 'No session ID found'.

 Expected behavior: Each triggered workflow should independently create or resolve its own valid session so that all conversations execute successfully, even under concurrent trigger conditions.

 Actual behavior: Only one conversation executes successfully. The other conversations either terminate immediately or don't continue after the first task with 'No session ID found' error.

</td></tr><tr><td>

Virtual Agent

 PRB1954676

</td><td>

Fallback is not working for Now Assist Virtual Agent \(NAVA\)

</td><td>

 

</td><td>

1.  Set sn\_nowassist\_va.show\_view\_more\_for\_synthesized = regular.
2.  Search for a skill book.
3.  Select **Search for more results**.
4.  Select the topic **Book a meeting room**.

 Notice that VA fails with, 'Sorry, there was a problem on my side trying to complete this request. Try asking again later.'

</td></tr><tr><td>

Virtual Agent

 PRB1956188

</td><td>

Translation issue on 'View AI Steps'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1959445

</td><td>

Now Assist Panel shows 'Unable to load'

</td><td>

 

</td><td>

1.  Set up track/znowassist.
2.  Set up Now Assist panel \(NAP\).
3.  Navigate **Conversational interfaces** &gt; **Assistants**.
4.  Ensure 'Now Assist in Virtual Agent' is off.
5.  Attempt to load NAP.

 Notice that NAP shows 'Unable to load'.

</td></tr><tr><td>

Virtual Agent

 PRB1959534

</td><td>

Virtual Agent is not considering the user's timezone preference on the date/time variable while submitting a catalog item

</td><td>

The system timezone is used when submitting a catalog item instead of the user's preferred timezone.

</td><td>

1.  Create a catalog item with a date/time variable.
2.  Make it conversational.
3.  Impersonate any user.
4.  Set the profile timezone to different than the system timezone.
5.  Attempt to submit the catalog item from Virtual Agent.

 Expected behavior: The date/time variable should have user's timezone preference.

 Actual behavior: The date/time variable has the system timezone set instead of user's timezone preference.

</td></tr><tr><td>

Virtual Agent

 PRB1960184

</td><td>

glide-cs unit test failures

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1962100

</td><td>

Interactions related to deleted conversations are updated with the 'Unable to generate Transcript' string in transcript fields

</td><td>

The delete conversation API deletes the conversation context, conversation messages, and transcript fields on an interaction record. The job 'sysauto\_script\_8d996a4b530812104129ddeeff7b1218' checks for interactions in a closed state with no transcripts, picks up these deleted data interactions and tries to generate the transcript again but fails as no data is available.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1962876

</td><td>

Interaction Record form does not always pop up when receiving an inbound call

</td><td>

Interaction Record form does not always pop up when receiving inbound calls from multiple sources in short time.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1963407

</td><td>

For no\_answer=true, use the message from Planner two and not hard coded fallback message

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1963459

</td><td>

Conversation abruptly ends after a cold start conversation with pre-chat survey enabled

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1963943

</td><td>

NAVA does not work after upgrading

</td><td>

Custom Greetings topic stopped working after upgrade. This issue may affect users with customized greetings topics if the skillpicker APIs called in the greetings/ending topic are not backward compatible.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1965604

</td><td>

An interaction is moved to 'Closed/abandoned' after a manual reassignment to an offline agent

</td><td>

Notice 'Interaction state - 'Closed abandoned', Assigned to - 'Virtual Agent'.'

</td><td>

1.  Set an agent as online \(admin\) and another as an offline user.
2.  Start a LA conversation.
3.  Do not accept the work item as admin.
4.  As an offline user, open the interaction on service workspace and assign it manually to yourself.
5.  Send a few messages between the offline user and the requester.
6.  Close the chat from the requester side.

 Expected behavior: Interaction state - 'Closed complete', Assigned to - '\[Offline user\]'

 Actual behavior: Interaction state - 'Closed abandoned', Assigned to - 'Virtual Agent'

</td></tr><tr><td>

Virtual Agent

 PRB1966041

</td><td>

Virtual Agent iframe is rendering with a blank screen

</td><td>

Trying to execute before document.body is available hence lands into an error and breaks the page.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1967329

</td><td>

QnA utterances in NAVA are missing 'Let me look up information related to ...' before it generates the response

</td><td>

In NAVA, when the user enters the utterance 'What is spam?', the user should see 'Let me look up information related to ...' before a response is generated. However, it goes directly to 'View AI Steps' followed by the actual response.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1967594

</td><td>

LastReadMessageDaoImpl causes n+one queries due to dot walking in sys\_script.do?sys\_id=318070047f3012102ff5e3136d86653d

</td><td>

Queries consumer account ID and conversation.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1969087

</td><td>

¶ is getting converted to the paragraph symbol in sys\_cs\_conversation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1969962

</td><td>

Link unfurling doesn't work as expected

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1970662

</td><td>

Gemini web search does not work on Yokohama Now Assist and the latest Zurich builds

</td><td>

Web search response is not generated in the UI, but the GenAI log shows a 'Gemini AI answer' received response.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1971595

</td><td>

Click metrics and deflection log

</td><td>

 

</td><td>

1.  Ensure **Citation** can be selected in the Synthesized Results.
2.  Update the output type.
3.  Track the previous selects in sys\_cy\_analytics.
4.  Write back the 'state' of the citation clicked/auto-started to the 'Output' type column for completed asset tracking.
5.  Ensure citation/asset selection in Virtual Agent writes the correct deflection type, such as Catalog ≠ Synthesized.
6.  Update the deflection log to filter out small talk to avoid unnecessary records.

 Observe that for agentic execution, the ending state is written back to the deflection log.

</td></tr><tr><td>

Virtual Agent

 PRB1974845

</td><td>

FDIHServiceImpl object holds significant memory

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1975158

</td><td>

Conversational catalog does not run in NAVA in Zurich mainline and anowassist

</td><td>

 

</td><td>

1.  Navigate to /esc portal.
2.  Query: 'I want Miro access'.
3.  Start the conversational catalog.

 Expected behavior: The Miro catalog flow will run.

 Actual behavior: DW ends abruptly, and NAVA ends the conversation after starting the request.

</td></tr><tr><td>

Virtual Agent

 PRB1975746

</td><td>

Add a 'source' column in sys\_one\_extend\_batch\_run

</td><td>

When the user creates a batch run with the **Source** field from NASK seven.one.0 \(Innovation Lab release\), the **Source** field is not populated as it does not exist in the dictionary of the sys\_one\_extend\_batch\_run table.

</td><td>

 

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1956730

 [KB2683059](https://hi.service-now.com/kb_view.do?sysparm_article=KB2683059)

</td><td>

Live agent only mode doesn't work for third-party channels

</td><td>

The user messages aren't received by the agent. This message appears in the log: 'Couldn't find rich control, dropping current message'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1927910

</td><td>

When initiating a chat with Enhanced Chat active in a portal, the **+** button to start a new chat remains disabled after the chat times out

</td><td>

Users must refresh the page to re-enable the **+** button.

</td><td>

1.  Ensure the Enhanced Chat bot is added to the portal by navigate to **Conversational Interfaces** &gt; **Assistants** &gt; **Now Assist in Virtual Agent** &gt; **Display Experience**.
2.  Confirm that the portal \(for example, Employee Center\) has Enhanced Chat enabled.
3.  Navigate to **Employee Service Center**.
4.  Initiate a chat session.
5.  Observe that the **+** button for starting a new chat is disabled.
6.  Leave the chat open until the abandon timeout occurs, or manually trigger the timeout. five. After timeout, observe that the **+** button remains disabled.

 Expected behavior: The **+** button is enabled after a chat times out, allowing users to start a new conversation without refreshing the page.

 Actual behavior: The **+** button remains disabled after timeout, and users must refresh the page to initiate a new chat.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1933376

</td><td>

Custom protocol links such as kolauncher:// are not rendered to be selected in Virtual Agent Genius responses

</td><td>

In Now Assist Virtual Agent \(NAVA\), protocol links such as KO Launcher links \(kolauncher://\) included in Genius Search responses are displayed as plain text and are not recognized as links that can be selected. This impacts workflows where links are critical for launching KO solutions directly from the chatbot.

</td><td>

1.  Log in to a Yokohama instance.
2.  Impersonate a user.
3.  Navigate to /ghd Service Portal.
4.  Start a conversation with Virtual Agent.
5.  Skip the first question, 'Please select your issue.'
6.  Enter a query that returns a KO Launcher link, such as 'Open KO1XXX'.

 Observe the Genius Search response for the kolauncher://KO1XXX link appears as plain text and cannot be selected.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1943211

</td><td>

A custom image for a FAB icon doesn't occupy the entire button

</td><td>

The current implementation uses a now-circular-button, but the custom image passed is set to the icon property of the button, which only occupies part of the button.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1955687

</td><td>

When minimized from any view and re-opened, DW should always open in float mode

</td><td>

DW re-opens in 90% Modal view.

</td><td>

1.  Open DW in 90% Modal view.
2.  Minimize DW.
3.  Select the FAB icon to re-open DW.

 Expected behavior: DW should always open in float mode when minimized and re-opened. Same with Pin mode.

 Actual behavior: DW re-opens in 90% Modal view.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1957770

</td><td>

Streaming is slow or frozen when performing continuous searches within the same conversation for Now Assist Virtual Agent \(NAVA\)

</td><td>

 

</td><td>

1.  Start a NAVA conversation.
2.  Perform multiple searches \(15-20\) within same conversation.

 Notice that streaming is slow or frozen.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1963494

</td><td>

The synthesized response is not displayed completely

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Navigate to **/esc portal**.
3.  Perform multiple searches.

 Notice that the final response is displayed incompletely on VA web client.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1964410

</td><td>

The 'Continue request' option is not displayed during MID topic switch

</td><td>

The context switches to the new search without showing the Continue Request option.

</td><td>

1.  Start a conversation from DW.
2.  Search for any topic/Catalog.
3.  During MID execution, try searching a different Topic/Catalog/KB.

 Notice that the context switches to the new search without showing the Continue Request option. The Continue Request option should be displayed.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1964923

</td><td>

'There is a JavaScript error in your browser console' errors in ESC landing page

</td><td>

A banner with the error message 'There is a JavaScript error in your browser console' appears randomly when it gets to the 'Generating the response' step.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1964982

</td><td>

Web client needs to honor the 'format': 'markdown' in synthesized response

</td><td>

The message is being parsed as HTML instead of markdown.

</td><td>

Have a synthesized response that results in a message with an HTML tag in the response.

 Expected behavior: Should be parsed as markdown.

 Actual behavior: Observe that the message is being parsed as HTML instead of markdown.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1965054

</td><td>

Virtual Agent messages are displayed twice

</td><td>

When summary and example questions are displayed once, VA displays documents, summaries and example questions one additional time.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1967339

</td><td>

Double/Triple Feedback icons in DW

</td><td>

When the user types 'What is spam' in DW, the results are generated with double or triple feedback icons at the end.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1974007

</td><td>

Synthesized responses disappear on NAVA, NAP, DW

</td><td>

Responses disappear after they are produced.

</td><td>

 

</td></tr><tr><td>

Visual Task Boards

 PRB1955767

</td><td>

vtb\_card and vtb\_task ACLs cause performance issues if either table is used in a related list

</td><td>

A user created a related list on an incident form that queries vtb\_task table. After an upgrade, they started seeing performance issues when viewing incident records and automated database alerts were generated.

</td><td>

 

</td></tr><tr><td>

Walk-Up Experience

 PRB1954978

</td><td>

The Walk up experience doesn't show any walk up locations due to error related to Query Range ACLs

</td><td>

walkup experience was not showing any walk up locations due to error related to Query Range ACLs.

</td><td>

1.  Open an instance.
2.  Impersonate walkup.technician.
3.  Navigate to **All** &gt; **Walk Up Experience** &gt; **My walkup locations**.

 Notice that any walk up experiences don't appear.

</td></tr><tr><td>

Walk-Up Experience

 PRB1962674

</td><td>

Remove 'Book Walk-up Appointment' Action from the drop-down list for Core It user

</td><td>

The drop-down list shows the option 'Book Walk-up Appointment.

</td><td>

Log in as a Core IT user and open a record page.

 Expected behavior: This option should not show up for a Core IT user.

 Actual behavior: The drop-down list shows the option 'Book Walk-up Appointment.

</td></tr><tr><td>

Window Manager

 PRB1945010

</td><td>

When the user uses the keyboard to navigate DW they are unable to resize or move the window

</td><td>

The user should be able to resize the DW with \(+\) key and should be able to decrease the size with shift \(+\) keys.

</td><td>

Issue one:

 Navigate to DW and Tab through the options.

 Notice that when user selects **Enter** to move the DW, nothing happens user is not able to move the DW to a different position.

 Issue two:

 Navigate to DW and Tab through the options.

 Notice that when user selects enter for resize options, it only works for one selection.

</td></tr><tr><td>

Work Order Management

 PRB1964615

</td><td>

The Dispatcher Workspace Agents calendar shows availability on holidays

</td><td>

When the system property sn\_fsm.use\_wm\_weekly\_resource\_p is set to true and the work schedule is connected to the holidays schedule through a child schedule, the holidays do not appear correctly on the DWS calendar.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 4 Hotfix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2695162)
-   [Zurich Patch 4](zurich-patch-4.md)
-   [Zurich Patch 3 Hotfix 1](zurich-patch-3-hf-1-PO.md)
-   [Zurich Patch 3](zurich-patch-3.md)
-   [Zurich Patch 2 Hotfix 3](zurich-patch-2-hf-3-PO.md)
-   [Zurich Patch 2](zurich-patch-2.md)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


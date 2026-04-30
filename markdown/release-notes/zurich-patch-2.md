---
title: Zurich Patch 2
description: The Zurich Patch 2 release contains important problem fixes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-10-15"
reading_time_minutes: 106
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich Patch 2

The Zurich Patch 2 release contains important problem fixes.

-   **Zurich Patch 2 was released on October 15, 2025.**
    -   Build date: 10-12-2025\_0904
    -   Build tag: glide-zurich-07-01-2025\_\_patch2-09-24-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z02.00.xlsx).

## Overview

Zurich Patch 2 includes 375 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-zp2.png "Top 10 problem categories")

## Security-related fixes

Zurich Patch 2 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich Patch 2, refer to [KB2533678](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2533678).

## Changes in Zurich Patch 2

-   **[AWS discovery using patterns](https://www.servicenow.com/docs/access?context=data-discovered-aws-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**
-   **[Discover datacenters only for new cloud accounts](https://www.servicenow.com/docs/access?context=discover-datacenter-only-new-account&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

    If you have multiple cloud accounts and datacenters in AWS and Azure, you can discover datacenters for new cloud accounts only, instead of refreshing the entire list.

-   **[Microsoft Azure Cloud discovery using patterns](https://www.servicenow.com/docs/access?context=azure-cloud-discovery-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US)**

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

Access Control

 PRB1893600

 [KB2178333](https://hi.service-now.com/kb_view.do?sysparm_article=KB2178333)

</td><td>

RecordFamilyResolver.archiveTableHasACLTerms needs more optimization

</td><td>

Performance issues with reports on instances with a high number of archive tables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Access Control

 PRB1915184

 [KB2400619](https://hi.service-now.com/kb_view.do?sysparm_article=KB2400619)

</td><td>

Security constraints prevent access to a requested page when visiting task.list

</td><td>

Failing a Deny ACL from anywhere in the hierarchy prevents table access to the list of a parent table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Email Notifications

 PRB1930940

</td><td>

Email parts are deleted when moving to a draft in workspace

</td><td>

Email issues are observed in the workspace. After copying and pasting the information, it's deleted.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1929229

 [KB2515183](https://hi.service-now.com/kb_view.do?sysparm_article=KB2515183)

</td><td>

Theme changes when opening an HR Case record page

</td><td>

There's user theme preference changes automatically when creating/opening an HR Case form from the workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Usage Analytics

 PRB1925359

 [KB2423777](https://hi.service-now.com/kb_view.do?sysparm_article=KB2423777)

</td><td>

Multiple out of memory \(OOM\) errors are triggered on the nodes from the 'User Property Change Sync' job

</td><td>

Multiple OOM errors were triggered on the nodes at different times whenever the 'User Property Change Sync' job was running. As a result, the node restarts.

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

Activity stream

 PRB1931494

</td><td>

RepresentedBy is missing from the event payload

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1929864

</td><td>

The chat card remains in the Agent inbox after the guest ends conversation

</td><td>

 

</td><td>

1.  Create a chat from the Virtual Agent \(VA\) web client as a guest user.
2.  Wait for it to be assigned to an agent.
3.  End the conversation from the VA web client.

 Notice that the chat card still appears in the Agent Inbox.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1921724

</td><td>

Improve ResponsePostProcessor time when the table is early binding

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1927798

</td><td>

Missing compound index on sys\_translated causes slowness in AI Search indexing

</td><td>

getTranslation in CatalogVariablesUtil can be as slow as 500ms, causing a performance issue when indexing sc\_cat\_item.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1930534

</td><td>

When used on service portals, 'Exact Match' should honor search sources

</td><td>

When using the 'Exact Match' feature on a service portal, the results of the exact match lookups should be limited to the sources which are included in the search profile, and honor the filters set on the search sources.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1938069

</td><td>

Optimize glide post processing for KG metadata tables

</td><td>

Suboptimal processing and delays in handling KG metadata tables.

</td><td>

Execute glide post processing on KG metadata tables.

 Observe performance and processing efficiency and notice suboptimal processing or delays in handling KG metadata tables.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1942680

</td><td>

Web search isn't working in Zurich and recent store apps

</td><td>

 

</td><td>

1.  Navigate to **/esc**.
2.  Start the web search by selecting the **Globe** icon.
3.  Query, 'Who is the president of the US'.

 Expected behavior: The web search query goes through.

 Actual behavior: The user receives a 'Sorry there was a problem' message.

</td></tr><tr><td>

AI Search for Next Experience

 PRB1857879

</td><td>

Regular catalog item results should use a 'Pencil' icon for consistency

</td><td>

 

</td><td>

1.  Open an AI Search \(AIS\)-enabled instance with AIS for global search.
2.  Search for a catalog item that doesn't have a picture, like 'laptop'.

 Notice that the Genius Results use the 'Pencil' icon, but the regular results use the 'Book' outline. Notice that in Portal, both regular and Genius results use the 'Pencil' icon. The icon should be consistent between regular and Genius results for the same record.

</td></tr><tr><td>

AI Search for Next Experience

 PRB1859890

</td><td>

There's improper use for current.update in a business rule

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search for Next Experience

 PRB1917747

</td><td>

Zing Migration Tool does not let users select unused SACs from base instance migration records

</td><td>

The tool only allows the user to select SACs currently used in a workspace. If one of the SACs from the base instance records is not being used in a workspace, it cannot be selected for migration in the tool.

</td><td>

 

</td></tr><tr><td>

AI Search for Virtual Agent

 PRB1932162

</td><td>

Marking KG 'None' in the Conversational Interface invokes the 'Text To Result' call

</td><td>

 

</td><td>

1.  Setup VA + KG.
2.  Open an instance.
3.  In the Conversational Interface, mark KG as 'None'.
4.  Trigger NLQ from any portal.

 Notice the text-to-result call.

</td></tr><tr><td>

AI Search

 PRB1708476

</td><td>

Issues logging signals in non-global scriptable environment

</td><td>

The user is unable to get the search analytics payload from the response \(even in a global scope\), and unable to log to signals API in a non-global scope.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1931645

</td><td>

AIS listens to events such as 'sys\_cache\_flush' and can cause stack overflow exception

</td><td>

AIS listens to events such as 'sys\_cache\_flush' and can cause a stack overflow exception by running a DBQuery, which can insert a record to sys\_cache\_flush.

</td><td>

1.  Enable glide.sys.domain.delegated\_administration and glide.sys.domain.partitioning.
2.  Create two separated domains.
3.  Clear the cache.
4.  Update any record.

 Observe the stack overflow exception in the logs.

</td></tr><tr><td>

AI Search UX

 PRB1917739

 [KB2347684](https://hi.service-now.com/kb_view.do?sysparm_article=KB2347684)

</td><td>

Add a mechanism to resend recent AMB messages on a created subscription

</td><td>

Under certain circumstances, it's possible that the component establishes the AMB connection after the Genius results are sent through the channel, since both the connection subscription and the Genius results being sent are asynchronous.

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1930672

</td><td>

Service Portal Genius Result \(GR\) synthesized response flashes and changes text size

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1932120

</td><td>

Non-conversational catalogs shouldn't have an option to request in a chat

</td><td>

 

</td><td>

1.  Provision an instance with September GenAI apps.
2.  Turn on Dynamic Window \(DW\) on portal.
3.  Search for a non-conversational catalog, like an Apple iPhone.

 Notice there's a pop-up on the citation for an Apple iPhone 13 with an option to request in chat. A citation for a non-conversational catalog should open in a new tab automatically.

</td></tr><tr><td>

AI Search UX

 PRB1936251

</td><td>

KG citation list view is empty

</td><td>

A message says 'Found no records' when a query should produce results.

</td><td>

1.  Navigate to **/sp**.
2.  Query 'What asset does Abel Tuter have' in the portal search box.
3.  View the assets info and multiple assets citations.
4.  Select **View Records**.

 Expected behavior: The user is direct to KG citation list view and assets show up in the list.

 Actual behavior: A message says, 'Found no records'.

</td></tr><tr><td>

AI Search UX

 PRB1937984

</td><td>

The caller is not in the scope rhino.global when called from Now Assist in Virtual Agent

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search UX

 PRB1942589

</td><td>

Increased timeout from 15s to resolve frequent no Genius Results on Portal

</td><td>

This issue occurs on Dispatcher Workspace enabled on Portal with Model GPT OSS, and takes longer for a response to return than in any other models.

</td><td>

 

</td></tr><tr><td>

AI Service - Glide Interfaces

 PRB1900176

</td><td>

ExtractItems\(\) pops the solutionIds from the original array

</td><td>

On an instance with more than 40\(JOB\_REQUEST\_COUNT\_LIMIT\) solutions in Waiting For Training State at present, once the sys\_trigger is triggered, all these solutions will be moved to the Training is Cancelled state and new solutions will be created and retried again.

</td><td>

 

</td></tr><tr><td>

AI Service - Glide Interfaces

 PRB1902435

</td><td>

In handleWaitingForTrainingState, there is a missing second argument in isJobSubmitted\(\)

</td><td>

In handleWaitingForTrainingState, a solution ID is not passed to the isJobSubmitted\(\) function, resulting in an execution of the 'if' condition. Even if the job is submitted, the solution is cancelled and retried until it reaches its last retry.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1900544

</td><td>

Uninstalling sn\_vul leaves sys\_metadata\_delete records that cause the uninstall to report as failed

</td><td>

 

</td><td>

1.  Provision an instance with sn\_vul installed.
2.  If on a local instance, set the sn\_appclient.app.install.offline property to true and sync on the app manager page.
3.  Uninstall sn\_vul.

 Observe that the uninstall failed with two records left in sys\_metadata living as sys\_metadata\_delete records.

</td></tr><tr><td>

Application Install Engine

 PRB1903785

</td><td>

Check if a package exists in the store\_package directory of node before downloading it

</td><td>

An error appears that includes the text 'Exception reading zip stream, falling back to old cipher' and 'java.io.FileNotFoundException'.

</td><td>

1.  Install any app from the store.
2.  Check that the temp directory is created for the first time.
3.  Delete the temp directory that was created.
4.  Let the system continue installation process, during which it downloads a package again and create a temp directory.

 Observe the error that appears, which includes the text 'Exception reading zip stream, falling back to old cipher' and 'java.io.FileNotFoundException'.

</td></tr><tr><td>

Application Install Engine

 PRB1904959

</td><td>

Some business rules cause install issues \(such as 'Prevent duplicate attachments'\), so the workflow should be disabled

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1911704

</td><td>

An error appears while selecting optional spokes and installing SaaS int app

</td><td>

During the pre-processing operation, the user receives an error while selecting optional spokes and installing SaaS int app. After a second attempt, the 'locate remote offering' plugin record for com.sn\_sam\_saas\_int can't be located.

</td><td>

1.  Provision an instance with com.sam.saas.int installed on a multi-node environment and optional plugins installed on another node.
2.  Try to repair the app.

 Observe that an error appears.

</td></tr><tr><td>

Application Install Engine

 PRB1934177

</td><td>

Node is not expanding the artifact

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1936285

</td><td>

During node restart, the system downloads version expects a higher store version

</td><td>

After a node restarts, the user sees the soft dependencies in the dependency manager are populated by the versions. The root cause is the artifacts are loaded from a file during node restart, and that is overwriting the active plugins information in Dependency Manager.

</td><td>

1.  Open a multi-node instance that has 15.0.5 as a version.
2.  Install 15.0.5 and other optional plugins.
3.  Upgrade to 15.0.17.

</td></tr><tr><td>

Application Manager

 PRB1920459

</td><td>

Nodes aren't coming online, and java.lang.Class CastException in the wrapper logs a boot

</td><td>

When nodes are booting up there is a ClassCaseException thrown, causing the nodes to boot, resulting in performance issues on the instance.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1926863

</td><td>

Uploading artifacts from Nexus doesn't work

</td><td>

The Nexus server was updated from Nexus2 to Nexus3, which caused an issue for artifact uploads from Nexus in all instances.

</td><td>

1.  Log in to any instance.
2.  In the navigator filter, search for **System Applications** &gt; **Install Application**.
3.  Select an option from Nexus to populate the repository URL.

 Observe that this URL isn't functional anymore due to the changes to the Nexus server.

</td></tr><tr><td>

Approvals

 PRB1928314

</td><td>

Retriggered change approvals aren't routing to the user who rejected them previously

</td><td>

After a Change approval is rejected, retriggering the approval doesn't route back to the original rejecting approver. Instead, the approval remains in a 'Rejected' state. This issue was observed after upgrading to Yokohama, and occurs with an e-signature enabled for Change requests.

</td><td>

1.  Deactivate normal Change request flows in Flow Designer.
2.  Create a new normal Change request.
3.  Give it any assignment group and request approval.
4.  Navigate to the **Change request list** view.
5.  Add the **Approval** field.
6.  Manually change the **Approval** field state to 'Requested'.
7.  Notice that this will trigger the workflow to move past the 'Wait' condition.
8.  Reject one of the approvals.

Notice that the other approvals move to 'No longer required'.

9.  Return to the Change request in list view.
10. Change the **Approval** field state to 'Requested'.

 Notice that the rejected approval remains in a 'Rejected' state while the others are requested.

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1919844

</td><td>

GCF Metrics for Asynchronous Message Bus \(AMB\) publishes are inaccurate starting in Yokohama

</td><td>

Only one message is counted by the GCF DEFN.

</td><td>

1.  Publish a server to client message via AMB.
2.  Publish client to server message via AMB.
3.  Check the GCF Metrics for a DEFN by creating an equivalent DEFN on a local instance.

 Expected behavior: Both messages should be counted by the GCF DEFN.

 Actual behavior: Only one of the messages is logged in the GCF counts for the DEFN.

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1934812

</td><td>

App Tier CPU increased during loadsim test executions

</td><td>

App tier CPU on a server increased by 4 times of the baseline numbers.

</td><td>

 

</td></tr><tr><td>

Async HTTP Client

 PRB1937994

</td><td>

Async HTTP client connection pool isn't optimized

</td><td>

Connection pooling is limited to 60 per host and 180 total, when it should host 300-900.

</td><td>

1.  Log in to an instance.
2.  Navigate to **/sp endpoint**.
3.  Enter 'What is spam'.
4.  Select **New conversation** after 35s.
5.  Enter 'What is spam' again.

 Notice that second set of requests don't benefit from connection pooling, and limits it to 60 per host and 180 total.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1932771

</td><td>

ATF Step UI action Visibility fails to find UI action when sys\_ui\_action.client = true

</td><td>

ATF Step UI action Visibility fails to validate UI actions that have client = true

</td><td>

 

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1932842

</td><td>

The user observes two summaries after selecting the section level **Load more** button

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1939150

</td><td>

When the user opens a capacity definition of type 'hours/tasks', it is changed to an Aggregated agent schedule.

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1918917

</td><td>

Ship an ACL for the Case summarization skill from the source Now Assist skill kit

</td><td>

 

</td><td>

1.  Log in as an admin user.
2.  Install the latest skill kit plugin.
3.  Install Now Assist for Employee Experience and Now Assist for HR Service Delivery.
4.  Activate the skill 'Case summary for approvals'.
5.  Navigate to **All** &gt; **Skill kit.**.
6.  Select **Case summarization for approvals** &gt; **Skill** &gt; **Prompt performance** &gt; **Create dataset**.

 Notice that while creating the data set, the error 'Failed to create dataset' occurs due to the ACL attached.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1923443

</td><td>

Journey Designer **Name** field in sn\_hr\_core\_email\_content table is non-translatable type

</td><td>

 

</td><td>

1.  Navigate to sn\_hr\_core\_email\_content.
2.  Open any record.
3.  Right-click Name.

 Observe that it is type String.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1929387

</td><td>

The **Name** field in the 'n\_hr\_core\_service\_approval\_option' table is a non-translatable type

</td><td>

 

</td><td>

1.  Navigate to HR **Workspace** &gt; **Create New HR Task** &gt; **Parent case users**.
2.  Change the language to German.

 Notice that the pills are not translated.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1932910

</td><td>

NowAssist Guardian flags the wrong prompts as 'Sensitive'

</td><td>

NowAssist Guardian's Offensiveness filters interpret simple prompts as sensitive. Phrases such as, 'How is my HR' and 'I want to call HR' trigger Guardian response, when they should not.

</td><td>

1.  Ensure the instance has Now Assist for Virtual Agent \(NAVA\).
2.  Ensure the instance has Guardian enabled.
3.  Navigate to **Now Assist Admin** &gt; **Settings** &gt; **Filters**.
4.  Enable the filter, 'Employee Personal issues'.
5.  Test the virtual agent by entering the prompt, 'how is my HR'.

 Notice that the sample filters shipped in this filter aren't even related to the phrase.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1933236

</td><td>

Add RCA to support 'Ask a question' with enhanced chat

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1931749

</td><td>

The **Impact** field isn't updated after running risk calculation

</td><td>

When a change\_request has the **Impact** choice field with 'None' enabled, the riskCondition should update the change\_request.impact field, but it doesn't. RiskCalculatorSNC is checking the wrong impact field. Instead of the one in the risk\_condition table, it's checking the one in the change\_request table.

</td><td>

 

</td></tr><tr><td>

CMDB Data Manager

 PRB1892066

 [KB2217546](https://hi.service-now.com/kb_view.do?sysparm_article=KB2217546)

</td><td>

Policy form doesn't honor retirement definitions correctly in enforced conditions when multiple retirement definitions are enabled

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

CMDB Data Manager

 PRB1914541

</td><td>

Fallback to V1 for 'or' query unsupported formats

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1789703

</td><td>

E2E Code Signing Setup gives an invalid signature for the 'Turn Off code signing property' record in Guardrail check

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1918750

</td><td>

Code signing code leaks GlideRecord

</td><td>

Code signing code is saving glide record in static, causing a leak.

</td><td>

1.  Create a CodeSigningField ValueGetter object by passing a glide record and field as parameters.
2.  Perform a heap dump.

 Expected behavior: The glide record passed in the steps should have been group changed.

 Actual behavior: The glideRecord object remains in the memory until a restart of node, or until another CodeSigningField ValueGetter object is created.

</td></tr><tr><td>

Code Signing

 PRB1926191

</td><td>

Malformed regex pattern prevents sys\_script and sys\_script\_include files from being code signed during build time

</td><td>

The code signing configuration in build-now contains a malformed regex pattern with an invalid trailing 'lesser than' character. This syntax error prevents the pattern from matching sys\_script\_include\_\*.xml and sys\_script\_\*,xml files, causing them to be excluded from the code signing process during the build time.

</td><td>

 

</td></tr><tr><td>

Condition Builder

 PRB1913121

</td><td>

Selecting a sn-value-editor-date-trend value causes issues

</td><td>

Selecting a sn-value-editor-date-trend value on a Chromium-based browser that has a scrollbar doesn't allow the user to go back after the animation finishes.

</td><td>

 

</td></tr><tr><td>

Content Experiences

 PRB1920414

</td><td>

All radio buttons in the new content record are grouped in one field set and in separate field sets with no legends

</td><td>

This issue occurs when using NVDA.

</td><td>

1.  Navigate to an instance.
2.  Activate the 'All' submenu.
3.  Enter content to publish.
4.  Activate the **Create New** link from the search results.
5.  Choose a portal from **Select the Platform**.
6.  Choose **Styled content** from the select content format.
7.  Select **Activate** and **Continue**.

 Expected behavior: The **Banner**, **Block**, and **Video** radio buttons should be grouped with a field set and 'Content style' as the legend. This also happens with the **Dark** and **Light** radio buttons with the legend 'Text color', and 'Left,' 'Center,' and 'Right' with the legend 'Text alignment', and 'None,' Button,' and 'Link' with the legend 'Call to action.'

 Actual behavior: NVDA announces 'Banner radio button checked 1 of 11' but doesn't announce the radio buttons' purpose when tabbing through the form. It is also announcing all radio buttons in the form belonging to the same group.

</td></tr><tr><td>

Content Experiences

 PRB1929367

</td><td>

'Add Item' for the RCE Accordion is creates disjointed tabs

</td><td>

New accordian tabs that are created aren't connected to the parent accordian, and properties set to it aren't affected.

</td><td>

1.  Install the Content Publishing and Employee Experience foundations app.
2.  Navigate to **Rich Content**.
3.  Enter a title.
4.  Select **Open editor**.
5.  Add the accordion component.
6.  Select **Add item**.

 Expected behavior: New accordion tabs are linked to the parent accordion and properties set to parent accordion should affect them.

 Actual behavior: New accordion tabs are not linked to the parent accordion, and properties set to parent accordion are not affecting them.

</td></tr><tr><td>

Content Experiences

 PRB1929445

 [KB2484781](https://hi.service-now.com/kb_view.do?sysparm_article=KB2484781)

</td><td>

The Copy Link action doesn't include HTTPS for news articles

</td><td>

When using the **Copy Link** UI action on the 'News Info' widget in the portal, the link that's copied doesn't include 'https://'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Content Experiences

 PRB1930250

 [KB2494389](https://hi.service-now.com/kb_view.do?sysparm_article=KB2494389)

</td><td>

When selecting the **Previous** or **Next** buttons on the 'Rich Content' widget, the page scrolls to the top

</td><td>

The position should remain unchanged.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Content Publishing

 PRB1884298

</td><td>

The state of a button is not conveyed to screen reader users

</td><td>

The active device setting is only visually indicated by a border. Screen reader users are not able to identify for which devices the content is being created.

</td><td>

1.  Open any instance and navigate to Application **Navigator** &gt; **Content Publishing** &gt; **Create New** &gt; **Rich Content**.
2.  Fill the input fields and Open in Editor.
3.  Navigate to the **Desktop**, **Tablet**, and **Mobile** buttons on the panel.
4.  Note the screen reader announcement for these buttons.

 Expected behavior: The value of the aria-checked attribute should be set to true after a user activates the corresponding element.

 Actual behavior: The active device setting is only visually indicated by a border. Screen reader users will not be able to identify for which devices the content is being created.

</td></tr><tr><td>

Content Publishing

 PRB1891292

</td><td>

The names of controls are not descriptive enough in Author View

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Content Publishing

 PRB1930169

</td><td>

The focus is very difficult to recognize on some elements

</td><td>

The focus hardly recognizes the scrollable text section and the switches. The focus frame should be clearly visible on the section and the switches, and the scrollable area should be labeled to indicate that it is scrollable.

</td><td>

 

</td></tr><tr><td>

Database Connection

 PRB1928984

</td><td>

'Stop' retries if the connection pool has waited for a connection for longer time

</td><td>

Repeated errors messages 'The connection attempt failed' occur when the TXID is the same for hours. Connection creation requests can be unreasonably slow. When the PostgreSQL service is stopped in a lab, almost instant failures are experienced and it takes 13 seconds to exhaust all retries. In a production environment, when a DB host becomes unavailable due to hardware failure, it can take hours to exhaust all retries because each request takes ~100 seconds per request.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1871451

</td><td>

Query business rules are not honored in GraphQueryExecutors

</td><td>

Knowledge Graph queries do not execute Query Business rules associated with a table. So, a query through NowAssist about incidents assigned to the user will include resolved incidents, whereas a query on incident assigned to the user through list view will not show resolved incidents.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1889238

</td><td>

**Function** fields containing dot walks when using the ^NQ operator return an incorrect query

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1889632

</td><td>

Improve performance of RecordHierarchyInvalidRecordFinder on large tables using SysId partitioning

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1907199

</td><td>

Two schemas marked as default simultaneously

</td><td>

There are two graph schemas which are marked as default. One is the Global graph and other is the newly created graph which is marked as default.

</td><td>

1.  Create a new graph.
2.  Mark it as default.
3.  Add desired nodes/edges.
4.  Save the graph.
5.  Navigate to sys\_meta\_graph.

 Notice that two graph schemas are marked as default.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1914258

</td><td>

Performance issue with getConnectedTableList

</td><td>

Using includeInboundEdges increases response time.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1929018

</td><td>

C2R isn't working when query has '\\'

</td><td>

An example cypher: \`MATCH \(u:User\)-\[:HAS\_MANAGER\]-&gt;\(m:User\) WHERE u.user\_name = 'abel\\tuter' RETURN m\`.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1929610

</td><td>

Cypher with a WDF and physical table isn't working

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Impersonate a user.
3.  Ask the query, 'last bonus and department of Abel Tuter'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1930031

</td><td>

The user doesn't get results from a Child table\(sn\_lg\_cnt\_repository\) of Parent\(ast\_contract\)

</td><td>

When the user queries for contractsSome records are skipped from the child table.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1931834

</td><td>

Static compile the regular expression alphanumeric pattern in ReductionEngine

</td><td>

Regex compilation is expensive and this shows in performance traces. It should move the member from per instance to static since it's constant.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1932266

</td><td>

Make regex patterns static

</td><td>

There are non-static patterns in DBCypherParser and DBSqlParserForCypher. Regex is expensive enough that it's worth converting.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1932532

</td><td>

The Cypher2Result API isn't returning the sys\_id of a Workflow Data Fabric record

</td><td>

The sys\_id doesn't exist. This is inherent in the general database views as well.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1932542

</td><td>

The Auto triggering of the KG Description Generator scheduled job fails when the Preshipping Job Status payload is in a failed state for the new instance

</td><td>

The run fails with an error message on the logs, and the preshipping job is not initiated.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1932785

</td><td>

No response for the queries executed via a non-admin role

</td><td>

The user doesn't get a response for queries when trying to run them as a non-admin user, even when the generated cypher is correct and there is data to be fetched.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1933012

</td><td>

Process domain separation and BQ rules work per alias rather than per table

</td><td>

This is only noticeable if the same table is used twice in a query.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1933585

</td><td>

getForTables on KG global graph doesn't return base object on overridden edges/nodes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1934684

</td><td>

getForTables on KG Global Graph isn't returning all the edges from contribution graph

</td><td>

 

</td><td>

1.  Create a contribution graph 'cont1' having sys\_user and cmn\_schedule nodes.
2.  Save the edge by using the script.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1935637

</td><td>

Tie TD/view caching transaction to the transaction lifetime

</td><td>

Code sets the cached lifetimes for TD/views to a method call such as getDisplayValue, and should be tied to the longer lived transaction instead.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1936492

</td><td>

Simple Queries take ~18-19s on Claude

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1936938

</td><td>

Leverage graph metadata cache in GraphTopology

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1940453

</td><td>

getForTables called with a depth of zero returns referenced tables

</td><td>

When getForTables is called with a depth of zero, the number of nodes returned should be the same as the number of tables passed in. However, extra nodes are returned for reference fields found on tables passed in.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1944805

 [KB2552260](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2552260)

</td><td>

getDisplayValue\(\) throws NullPointerException on many types of catalog variables

</td><td>

There is a "java.lang.NullPointerException" error.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1946284

</td><td>

Normal \(non-aggregate\) Cypher queries, response columns are returned without node aliases

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1762209

</td><td>

ITERATIVE\_CHUNK\_PROCESSOR creates too many chunk entries in the sys\_dm\_chunks table

</td><td>

 

</td><td>

1.  Set the property 'glide.db.unreferenced\_record\_cleaner.large\_table\_threshold' to a smaller value so that the unreferenced table cleaner process type is ITERATIVE\_CHUNK\_PROCESSOR.
2.  Bulk up the data in sys\_object\_source with unreferenced records from six physical reference tables.
3.  Run the 'DMScheduler' to process the unreferenced table cleaner.
4.  Verify the data that gets inserted in the sys\_dm\_chunk table.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1824584

</td><td>

The latest collection date is incorrect in sys\_db\_size\_stats

</td><td>

If SNC hasn't run for a few days, the latest data date doesn't change. But since Stats Gatherer still runs daily, it keeps adding duplicate entries for that same date in sys\_physical\_table\_stats and sys\_db\_size\_stats. This causes the table details page to show incorrect totals by adding up all the duplicates.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1896049

</td><td>

When there's no data in the tables, they should display as 'Uo data to display' but it shows as 'Unable to display content'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1898106

</td><td>

The values in the peripheral tables and those returned by the STAS API values for the particular table are mismatched

</td><td>

There is a mismatch between the values stored in the sys\_peripheral\_table\_stats table and those returned by the Table Stats API.

</td><td>

1.  Log in to the instance.
2.  Run the Table Stats API for the specific table to be analyzed \(for example, task or incident\).
3.  Open the corresponding table \(either physical or logical\), copy its sys\_id, and paste it into the sys\_peripheral\_table\_stats table.

 Expected behavior: The values for the selected table \(for example, task or incident\) in the sys\_peripheral\_table\_stats table should match the values returned by the Table Stats API response.

 Actual behavior: There appears to be a mismatch between the values stored in the sys\_peripheral\_table\_stats table and those returned by the Table Stats API.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1916418

</td><td>

The 'Unreferenced Record Cleaner' only creates a single chunk per run when there is still a large amount of orphan records to be removed

</td><td>

The 'Unreferenced Record Cleaner' \(URC\) creates multiple chunks for the first run for a rule, but only create a single chunk for subsequent runs. The threshold for the change in behavior is when the number of orphan records still left to be removed is less than 1 million records for any specific rule.

</td><td>

1.  Create a URC rule for a table that has a filter and more than 1 million orphan records in the result set.
2.  Trigger the URC job.

 Observe that the first run creates multiple chunks, but the next run creates a single chunk as soon as the number of orphan records drops below 1 million for the rule.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1925421

</td><td>

ServiceIdentity records are missing for RaptorDB

</td><td>

All services in the instance topology need to have ServiceIdentity records to turn on some authentication between services.

</td><td>

Zboot any instance.

 Observe there's no records in ServiceIdentity or ServiceOld tables for RaptorDB, unlike other DB services.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1929305

</td><td>

An acceptable table name for DB isn't used when fetching in-place updatable fields in Glide

</td><td>

The user observes an error.

</td><td>

Use the method DBInPlaceUpdateUtils \#getEnabledInPlace UpdateFields with a table name that is longer than 30 characters.

 This results in an exception that indicates the table doesn't exist.

</td></tr><tr><td>

Database Persistence

 PRB1901056

</td><td>

Remove redundant pool expansion rejected messages for background operations

</td><td>

Logs continue to grow in xmlstats, and are expected to grow even. Only logs should be removed.

</td><td>

Configure a DB pool to be small \(less than number of worker threads\).

 Observe logs such as 'Pool: glide: pool expansion rejected' also growing in xmlstats.

</td></tr><tr><td>

Database Persistence

 PRB1920823

</td><td>

Data is lost on updateMultiple with the type 'phone number E164'

</td><td>

In sys\_dictionary, the user can set the 'mobile\_phone' element of 'sys\_user' to 'Phone Number E164.' If the user later updates the company for someone in the base instance data set, the mobile\_phone field gets set to null.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1937163

</td><td>

Implement a duplicate-record check in the KG Description pre-ship API to avoid insertion and update errors.

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Views

 PRB1900333

</td><td>

Querying a database view using an IN query on the view's sys\_id uses a list of encoded sys\_id values, resulting in an invalid query in Yokohama

</td><td>

When a database view is queried a sys\_id, a unique value is generated by encoding the sys\_ids from the matching joined records from each view table, which result in the row being returned.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1923285

</td><td>

Users can't create reference on columns of the type 'Int/BigInt' from DataBricks

</td><td>

DataBricks integer columns are mapped as 'BIGINT' in Trino and eventually 'Long' in ServiceNow tables. When users try to change one of the column mapping to a reference to another DataBricks DF Table reference key of type 'Long', it throws the error 'Reference column 'c\_nationkey' mapped to remote column 'c\_nationkey' is using type longint which is not supported for reference columns'.

</td><td>

1.  Create a DataBricks Connection and 2 DF tables \(Customers and Nations\).
2.  On a user's table, select the 'Nation key' columns as a reference.
3.  Try to select **Finish**.

 Observe an error: 'Reference column 'c\_nationkey' mapped to remote column 'c\_nationkey' is using type longint which is not supported for reference columns'.

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1937036

</td><td>

Data Fabric memory usage of GlideTableInfo

</td><td>

Performance testing on an instance experiences Out of Memory issues and node restart when a long running transaction or a high number of transactions are executed. About 6.1% of the total memory is used by the JVM in a heap dump using GlideTableInfo.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1930243

</td><td>

Clone Job License Check issue

</td><td>

Data Privacy \(Classic\) on an instance can create anonymization clone policies to create anonymization jobs. When cloning from one instance to another, the PostClone script picks up the anonymization clone policy and creates a federated job on the target instance, which then anonymizes the data on the cloned instance using the configurations in the policy.

</td><td>

1.  Activate the data privacy plugin \(sn\_dp\_store\_app\) on the source instance.
2.  Elevate the data\_privacy\_admin role.
3.  Navigate to **System Security** &gt; **Data Privacy** &gt; **Anonymization**.
4.  Select **Create new policy**.
5.  Select **Data tables** or **columns**.
6.  Select **Create**.
7.  Enter a name.
8.  Select a data class.
9.  Select **Activate the policy** during cloning.
10. Select the policy order to run if there are multiple clone policies.
11. Select **Continue**.
12. Complete the policy configuration.
13. Publish the policy.
14. Back up the data privacy configurations.
15. Schedule the anonymization job.
16. Submit a clone request as a data privacy admin.

 Notice that the data privacy PostClone script executes on the target instance, creating a data privacy federated job record on it. The federated job creates and executes a data privacy job for each post-clone policy in Application Order on the target instance, and the backup source is also cloned there. The data privacy PostClone script creates and executes data privacy jobs for configured policies on the target instance. The elevated data privacy clone processor can log on to the target instance and monitor the post-clone federated job state on the dp\_federated\_job.list and dp\_job.list.

</td></tr><tr><td>

Decision Table \(Family\)

 PRB1930728

</td><td>

Adding a new choice to choice type results in a decision table

</td><td>

The user should be able to create choice type result with a new choice result, or add a new choice to the choice type result in a decision table. However, there is an error.

</td><td>

1.  Create a decision table and add at least one input and one condition.
2.  Create a choice type result with a new choice list.

 Notice that the user can create a result type choice, but it gives an error whenever they try to add new choice in choice list.

</td></tr><tr><td>

Declarative Actions

 PRB1819856

</td><td>

Declarative actions \(Move, Add, Change, Delete\) aren't enabled when 'group by' is applied on any column for active PI records

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Demand Management

 PRB1922736

</td><td>

Inappropriate tooltip provided for Close button in a Demand record

</td><td>

 

</td><td>

1.  Navigate to **Self-service** &gt; **Demands** &gt; **Open a record** \(In Approved state\).
2.  Select the **Close** button and observe the announcement.

 Expected behavior: Provide tooltip as 'Close the approved demand'

 Actual behavior: Screen reader announces 'Close button, close the completed demand'

</td></tr><tr><td>

DEX Application &amp; Device Health

 PRB1927593

</td><td>

For a fresh DEX installation in a Zurich instance, topics present in mb\_topic are not synced to mb\_shard\_mapping

</td><td>

Because the topics are not linked, data flow from the itom\_cloto\_metrics topic is not read by the metric base.

</td><td>

 

</td></tr><tr><td>

DEX Application &amp; Device Health

 PRB1931462

</td><td>

The user list breaks when the dex\_user\_device\_loc\_detail table has empty dex\_user fields

</td><td>

 

</td><td>

1.  Set up DEX with 3.0.9 or upgrade DEX to 3.0.9.
2.  Log in as a DEX user.
3.  Navigate to **SOW** &gt; **Users List**.
4.  Validate that the list loads properly.
5.  Check the dex\_user\_device\_loc\_detail table and find one record with the **dex\_user** field that contains an empty value.
6.  Navigate to the user details page
7.  Navigate to the list using pagination where the above user exists.

 Notice that while trying to navigate to the list pagination where this user exists, it shows a list error as in the attachment.

</td></tr><tr><td>

Discovery

 PRB1893089

</td><td>

The 'Discovery::getScheduleContainingAnyIP\(\)' API causes slow pressing of 'change\_request.trigger.discovery' sysevents

</td><td>

Each API call can take one to two minutes. Instead, the API should query DH only.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1898321

 [KB2260681](https://hi.service-now.com/kb_view.do?sysparm_article=KB2260681)

</td><td>

Logs for patterns execution on Discovery Log need to be less alarming

</td><td>

Discovery log for pattern indicates a pattern failure 'Failed Exploring CI Pattern', even though the pattern brought data back.

</td><td>

1.  Run lab and cloud discoveries.

Notice that this should give a variety of errors or use attached update set, which has dummy patterns that fail in different use cases

2.  Look at the discovery log.

 Notice that 'Failed Exploring CI Pattern' occur for discoveries that actually brought data.

</td></tr><tr><td>

Discovery

 PRB1925275

</td><td>

Inconsistent behavior in the Discovery Status Started and Completed counts and **State** fields

</td><td>

When the user runs quick discovery, the Discovery Status State is either stuck in Active or Starting states. The Started or Completed counters stay on count 0 and there is no progress despite successful discovery.

</td><td>

 

</td></tr><tr><td>

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

Discovery

 PRB1930200

 [KB2474013](https://hi.service-now.com/kb_view.do?sysparm_article=KB2474013)

</td><td>

Protected Tables Plugin will block DiscoverySensorJob logging, and cause warnings about syslog inserts from ProtectedTableAccessHandler instead

</td><td>

When the Protected Tables Plugin is active, which is recommended, the source= DiscoverySensorJob GlideRecord inserts made directly to the syslog table by Discovery's 'DiscoverySensorJob' script include are blocked, and flood the syslog table with logs from source=ProtectedTableAccessHandler instead.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Dynamic Translation for Virtual Agent

 PRB1927624

</td><td>

Dynamic translation with live agent conversation in page

</td><td>

A message says it will be automatically translated from English but the history from the requestor is still in Spanish.

</td><td>

1.  Set the user's preferred language to Spanish.
2.  Start a conversation in portal with Now Assist Virtual Agent.
3.  Connect with a Live Agent whose language is set to English.

 Observe that a message says it will be automatically translated from English but the history from the requester is still in Spanish.

</td></tr><tr><td>

Edge Encryption

 PRB1927436

 [KB2434303](https://hi.service-now.com/kb_view.do?sysparm_article=KB2434303)

</td><td>

After an upgrade to Yokohama, a lot of 'MultiPartXXX' files are created under the 'tmp' folder

</td><td>

This causes full disk space issues on the machine.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Edge Encryption

 PRB1934717

</td><td>

The edge decryption job doesn't check the correct column for journal/audit fields

</td><td>

When deciding to column level encrypt data or not, the edge decryption job doesn't check the correct column for journal/audit fields. As a result, the journal field and audit entries aren't CLE encrypted.

</td><td>

1.  Configure the **Journal** field to be edge encrypted.
2.  Run an edge mass encryption job to encrypt the data.
3.  Configure the CLE module/map/configuration on the same field.
4.  Ensure that the configuration is active.
5.  Ensure that the edge user has access to this CLE module.

The edge user is configured in its edgeencryption.properties file \(edgeencryption.target.username property\). The user that's configured to connect to the instance must have access to the CLE module or else the decryption job won't attempt to encrypt with it.

6.  Disable the edge encryption configuration for the field.
7.  Run the edge decryption job on the field.
8.  Check the process historical records.

 Expected behavior: The **Journal** field entries in sys\_journal\_field are CLE encrypted. **Audit** field entries are also CLE encrypted.

 Actual behavior: The journal field and audit entries aren't CLE encrypted.

</td></tr><tr><td>

Employee Center

 PRB1891020

</td><td>

MyItems widget receives redundant keyboard focus in the Employee Service Center \(ESC\)

</td><td>

When navigating the 'My Active Items' section using keyboard, the focus behavior is not optimal for accessibility. The entire card and the **View Details** button receive focus, which is redundant since both lead to the same destination. The screen reader announces only the 'View details' which lacks context about which item's details are being viewed.

</td><td>

1.  Log in to any base instance.
2.  Append /esc in the URL to launch Employee Center portal.
3.  Navigate to 'Cards' under 'My Active Items \(My Items widget\)' using the 'Tab' key.

 Observe the keyboard focus.

</td></tr><tr><td>

Employee Center

 PRB1893416

</td><td>

The **Save as Draft** button is hidden for HR Catalog Items in the HRM Catalog Item Widget

</td><td>

When filling out the a form in the HRM Catalog Item widget, the **Save as Draft** button is not available when configured with an HR Catalog Item.

</td><td>

1.  Open /ESC.
2.  Open the 'General Benefits Inquiry' catalog item.

 Expected behavior: The **Save as Draft** button is available.

 Actual behavior: The **Save as Draft** button isn't available.

</td></tr><tr><td>

Employee Relations Case Management

 PRB1909215

</td><td>

There's no base instance scoped ACL for sn\_hr\_er and asmt\_assessment\_instance\_question

</td><td>

The user can't read a specific asmt\_assessment\_instance\_question record, even though the user has the required role. There isn't a base instance scoped ACL for sn\_hr\_er, but there is one for sn\_hr\_core.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1909720

</td><td>

Error shows while attempting to open the alert tags table \(query\_range error\)

</td><td>

 

</td><td>

1.  Connect as an evt\_admin user.
2.  Navigate to **sn\_em\_ai\_alert\_tags**.
3.  Run the filter for alert tags containing 'query\_range'.

 Notice the error that appears in the UI.

</td></tr><tr><td>

Event Management

 PRB1918087

</td><td>

Poor performance of building business service trees in 'Services Dashboard'

</td><td>

The /api/sn\_nocpit/nocpit/GroupTree REST endpoint inefficiently queries the sa\_service\_group\_member table twice during each transaction, reading all of the rows each time.

</td><td>

1.  Impersonate a user.
2.  Navigate to the Service Operations Workspace.
3.  Select the **Services Dashboard** icon.

 Observe that the /api/sn\_nocpit/nocpit/GroupTree transactions are periodically slow.

</td></tr><tr><td>

Event Management

 PRB1934829

</td><td>

getMap runs indefinitely when it has an alert path on a service map with a cycle

</td><td>

A halting criterion reaches null while traversing the hashmap, but the hashmap contains a cycle, so the loop never terminates.

</td><td>

 

</td></tr><tr><td>

External Triggers

 PRB1927717

</td><td>

Copy Event Source copies an old event source ID in HMAC configuration

</td><td>

 

</td><td>

1.  Create an event source of type HMAC config.
2.  Copy the event source.
3.  Make sure new event source is created.
4.  Navigate to HMAC config and check that the event source ID is populated.

 Expected behavior: For the new event source, HMAC config should have event source id of new event source.

 Actual behavior: The old event source id is copied to HMAC config of new event source.

</td></tr><tr><td>

Flow Engine

 PRB1927282

</td><td>

Sync requests are failing in the NowLLM Media action

</td><td>

sn\_ml.MLServiceUtil.parse TritonResponse\(headerContentLength, responseBody\); throws an exception and the flow to fails. This only occurs when the One Extend call is synced.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1923234

</td><td>

Add FDCollection complex object after all applications are installed

</td><td>

When the user installs the Open Line - Predictive Intelligence app, they notice that FDCollection complex object doesn't exist.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1923788

</td><td>

Activating plugin and corrupted flow plugin converts to a corrupted flow when added to a flow

</td><td>

 

</td><td>

1.  Navigate to WorkFlow Studio.
2.  Create a new Flow/Subflow.
3.  Add the Activate Plugin and/or Rollback Plugin subflows.

 Expected behavior: Subflows are added successfully to the flow.

 Actual behavior: Subflows convert to a Corrupted Flow when added.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1931588

</td><td>

Opening a flow and closing it without editing will update the **Updated** and **Updated by** fields

</td><td>

 

</td><td>

1.  Navigate to WorkFlow Studio.
2.  Select any flow and note the values of the **Updated** and **Updated by** fields.
3.  Close the flow without making any changes.

 Expected behavior: The **Updated** and **Updated by** fields are unchanged

 Actual behavior: The **Updated** and **Updated by** fields change to the current date/time and the user who opened the flow.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1934643

</td><td>

Auto-save fails when the user updates the same inline script multiple times

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Glide Server APIs

 PRB1933958

</td><td>

'Cannot use Gateway as tables are distributed for the view:u\_product\_application' warning in Zurich

</td><td>

Post Zurich Upgrade, the warning, 'Cannot use Gateway as tables are distributed for the view:u\_product\_application', appears for some transactions.

</td><td>

 

</td></tr><tr><td>

Glide Server APIs

 PRB1946733

</td><td>

setStartDateTime API behavior change for Strings passed in

</td><td>

It used to be internal date format. Now it goes through setDisplayValue, breaking various formats.

</td><td>

 

</td></tr><tr><td>

Health and Safety Incident Management

 PRB1916809

 [KB2324070](https://hi.service-now.com/kb_view.do?sysparm_article=KB2324070)

</td><td>

The Injury illness 'Create' page is blank

</td><td>

This issue was observed in Zurich, but works in previous families.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Health and Safety Risk Management

 PRB1918530

</td><td>

The search function under Hazards in Health and Safety advanced in the Employee Service Center \(ESC\) is not working

</td><td>

This issue occurs for Health and Safety versions v10 and v11.

</td><td>

1.  Navigate to ESC.
2.  Create Health and Safety advanced.
3.  Select **Hazards**.
4.  Input a Hazard name under the search bar.

 Expected behavior: The search function should work as expected under 'Hazards'.

 Actual behavior: A server error appears.

</td></tr><tr><td>

Health and Safety Risk Management

 PRB1921969

</td><td>

Under the Health and Safety Inspection survey result, the question order is incorrectly displayed in the NowAgent app

</td><td>

The question order should be displayed the same as the original survey.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1924627

</td><td>

Kafka producer usage is not released after IP ACL message is published

</td><td>

Not making a call to endUsage will make the cleaning up of the registry wait for at least one minute.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1925871

</td><td>

Instance PKI Certificate Generator is displaying KMF error

</td><td>

The IPKI Certificate Generator displays an error even when all required components are functioning and healthy.

</td><td>

 

</td></tr><tr><td>

Horizon Component Library

 PRB1818590

</td><td>

now-pagination-control resets the first page \(page 0\) unnecessarily

</td><td>

Pagination control resets to the first page after decreasing the count.

</td><td>

1.  Create an example pagination control with 22 total items.
2.  Navigate to the last page.
3.  Simulate deletion of an item by changing the total to 21.

 Notice that the pagination control resets to the first page because the count decreased, even though it didn't need to.

</td></tr><tr><td>

Horizon Component Library

 PRB1925233

</td><td>

Text selection fails when selecting the sparkle icon on workspace

</td><td>

This issue was also found in UI16.

</td><td>

1.  Navigate to **Now Assist Admin** \(NAA\).
2.  Activate the Resolution note generation skill with the user trigger on in ITSM.
3.  Open Service Operations Workspace \(SOW\).
4.  Open any open incident record.
5.  Switch to the 'Details' tab.
6.  Select the **Resolution note** text box.
7.  Select the **sparkle** icon.
8.  Insert the generated resolution note.
9.  Select the **sparkle** icon in the text box again.

Notice that it shows a 'Quick action' option.


 Expected behavior: It should select whole text in **Resolution note** text box.

 Actual behavior: Observe that it isn't selecting the text when selecting the **sparkle** icon.

</td></tr><tr><td>

HR Service Delivery

 PRB1910181

</td><td>

Changes related to app-esm

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1920738

 [KB2525534](https://hi.service-now.com/kb_view.do?sysparm_article=KB2525534)

</td><td>

HR Case description \(rich\_description\) doesn't copy over data, and the rich description is left empty

</td><td>

Rich Description appears as null in List View but displays correctly in the case record. The reverse works as expected— when updating the **rich\_description** field in the HR case form, the value will appear in the **rich\_description** field in the list view.

</td><td>

1.  Log in to the instance.
2.  Create an HR case.
3.  Navigate to **sn\_hr\_core\_case.LIST**.
4.  Open the newly created case.
5.  Select the **Hamburger** icon.
6.  Configure the form layout.
7.  Add the **Description** field.
8.  Save the changes.
9.  Return to the HR case form.
10. Enter a message in the **Description** field, but don't enter anything in the **rich\_description** field.
11. Save the changes.

Observe that the same value is automatically updated in the **rich\_description** field due to a business rule that syncs values between the two fields.

12. Open the list view.
13. Add the Description and rich\_description columns.

 Notice that the **rich\_description** field doesn't contain a value.

</td></tr><tr><td>

HR Service Delivery

 PRB1931448

</td><td>

The **Suspend Reason** field isn't present on a form by default

</td><td>

This causes a discrepancy in populating the suspend reason in the work notes in an HR case.

</td><td>

 

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB1930639

</td><td>

Clone Admin console 'Request' page performance

</td><td>

 

</td><td>

Navigate to **Clone Admin** &gt; **Request Clone**.

 Notice that the 'Request' page takes an average of 20 secs to load.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1934310

</td><td>

Data\_lag is not present in xmlstats and dashboards on Zurich and later

</td><td>

Looks like heartbeat values are not being recorded in idr\_system\_status.

</td><td>

 

</td></tr><tr><td>

Instance Scan

 PRB1927870

</td><td>

Instance Scan excludes inactive records, even when the system property 'glide.scan.base\_system\_records' is enabled

</td><td>

When running a custom Instance Scan table check, inactive records are not included in the scan results, even if no conditions are set on the scan check record. This occurs even after setting the system property 'glide.scan.base\_system\_records = true'. For example, creating a scan against sc\_cat\_item with the condition 'active = false' returns no findings, despite the existence of inactive, custom-created records.

</td><td>

1.  Create a new Table Instance Scan Check.
2.  Set the target table to 'sys\_app' or 'sc\_cat\_item'.
3.  Add the script in the 'Advanced' tab.
4.  **Save** it.
5.  Run a Test Scan.

 Observe that inactive records are not scanned and Boolean conditions such as 'active = false' return zero results.

</td></tr><tr><td>

Integration Hub

 PRB1928792

</td><td>

Unable to connect to ServiceNow MCP Server using ServiceNow MCP Client

</td><td>

'Apply Default Headers' is being called before ApplyHeaders which always adds the 'Accept: text/event-stream' header. Any headers added in the step are added as well, causing the duplicate headers. The text/event-stream header shouldn't be added if there is an accept header added in the step.

</td><td>

1.  Create an SSE step to any endpoint.
2.  Add a header with the value 'Accept: application/json,text/event-stream'.
3.  Test the SSE step.
4.  Ensure results show the Accept header as the value 'application/json,text/event-stream'.

</td></tr><tr><td>

Integration Hub

 PRB1931168

</td><td>

SSE step does not run on MID

</td><td>

 

</td><td>

1.  Create an action with an SSE step and check the run on the MID checkbox.
2.  Test the action.

 Notice the error 'SSE is only available on instance'. Individual chunks are not processed by the handler.

</td></tr><tr><td>

JVM at Scale

 PRB1932145

</td><td>

Existing automation is unable to capture heap dumps for short spikes in GC pressure

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

JVM at Scale

 PRB1938155

</td><td>

glide.memory.watcher is being too aggressive after upgrade

</td><td>

Changing the memory watcher to use old gen usage percentage over the whole heap usage percentage kicks in remediator logic early.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB1916372

</td><td>

A module key rekey job fails for asymmetric keys

</td><td>

 

</td><td>

1.  Navigate to the Crypto module.
2.  Open glide\_usage\_analytics\_token\_signing.
3.  Ensure that the key pair is generated in both instances with the same key alias.
4.  Perform a clone.

 Expected behavior: Users should be able to rekey and deactivate the asymmetric key pair and associated cert if it exists on the sys\_certificate table of the source instance

 Actual behavior: The module key rekey job fails for asymmetric keys.

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB1917107

</td><td>

Asymmetric module keys with Multiple Active keys won't always pick up the current instance keys

</td><td>

The CryptoOperations API picks the active key ordered by date whether that key is generated on that instance or not. When automations like clone run on the instance, there appears to be a brief period where both the source and target instance's module keys are present on the target instance. For Asymmetric operations like signing, before rekey is successful, a CryptoOperations API might use keys that don't belong to that instance. After rekey is complete, the same operation uses keys that belong to the current instance.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1913708

</td><td>

The KMF customer action page no longer displays the latest certificate vulnerability due to a missing experience\_properties field

</td><td>

The KMF has a 'Customer Action' page with a custom script that uses the experience\_properties field. This field is not populated in Zurich, which causes the feature to break.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1915319

</td><td>

The underline is not available by default for the 'Your PC Browser' and 'Microsoft' links in Knowledge article.

</td><td>

 

</td><td>

1.  Open an instance in Internet Explorer 10 for Windows 8.
2.  Navigate to **Service portal** &gt; **Knowledge** &gt; **Applications** &gt; **Microsoft** &gt; **IE** &gt; **Managing Settings**.
3.  Navigate to the Manage Your PC Browser and Microsoft links.
4.  Verify whether the underlining is defined by default on these links.

 Notice that the underline is not available by default for the 'Your PC Browser' and 'Microsoft' links.

</td></tr><tr><td>

KPI Details

 PRB1885024

</td><td>

Some error messages do not assist with troubleshooting the error

</td><td>

The error message 'You cannot perform this action' is not descriptive. It does not tell the user what is the error and which field has this error.

</td><td>

 

</td></tr><tr><td>

Language and Translations

 PRB1934636

</td><td>

Translations merge for Yokohama and Zurich

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1900179

</td><td>

JavaScript error on a portal UI page when components are loaded using getEmbeddables

</td><td>

The error reads, 'There is a JavaScript error in your browser console'.

</td><td>

1.  Log in as an admin user.
2.  Create a new portal page
3.  Configure the Portal Advanced List widget.
4.  Save the change and open the widget on CSM page context.

 Observe the browser error, 'There is a JavaScript error in your browser console'.

</td></tr><tr><td>

List Administration

 PRB1916174

</td><td>

The header notification doesn't render when SN\_RECORD\_LIST\_DATA\_BROKER\#ADD\_NOTIFICATIONS is dispatched

</td><td>

When repeating in NRLC, the error occurs as well. The error message comes from a Data Policy that prevents 'Assigned to' from being empty.

</td><td>

1.  Create a new list against the problem\_task table.
2.  Attempt to remove the value in 'Assigned to' in the new list.

 Expected behavior: Notice the error message.

 Actual behavior: No error message appears.

</td></tr><tr><td>

List Administration

 PRB1917660

</td><td>

When fuzzy is enabled, UI actions on a list show a negative number once all the items are selected and de-selected

</td><td>

When the user selects some items in a list and then hits the 'Select all' option in the banner, then deselect more than five of the items in current page, the number displayed on the UI action is negative.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1923987

</td><td>

Unable to edit dot-walked choice fields and remove commas from the display

</td><td>

The user can't edit dot-walked choice fields or remove commas from the display on the integer value on the 'Presentation List' component. It's supported in the List component, but when the user hovers on the List component, it shows that it will be deprecated soon and the 'Record List' component should be used instead \(which also uses the 'Presentation List' component\).

</td><td>

1.  Navigate to the UI Builder.
2.  Create an experience.
3.  In a page variant, add 'Record List Bundle' and set a table to it.
4.  Add a dot-walked choice field to the list view and a field with integer.
5.  Preview the page.

 Observe that the dot-walked field is not editable. The integer value field also has commas, even after setting format:none attribute in sys\_dictionary. The same process works fine with the List component.

</td></tr><tr><td>

List Administration

 PRB1926404

</td><td>

The sys\_dictionary attribute isn't honored on integer value on the 'Presentation List' component, which is part of 'Record List Bundle' of UI Builder

</td><td>

An integer/number field is always shown with commas, even though the attribute format is set as none in the sys\_dictionary record of the field.

</td><td>

1.  Navigate to the UI Builder.
2.  Create an experience.
3.  In a page variant, add 'Record List Bundle' and set a table to it.
4.  Add an integer field to the list view.
5.  Navigate to the sys\_dictionary record of the field and set the attribute as format=none.
6.  Preview the page.

 Observe that the dot-walked field is not editable on the list view.

</td></tr><tr><td>

Major Incident Management

 PRB1931736

</td><td>

Optimize the business rule \(BR\) 'Attach Communication Plan'

</td><td>

The 'Attach Communication Plan' BR is async and triggered on the insert/update of task. The BR has the condition CommunicationPlanEngine\(current\).canRun\(\), which can run a query on comm\_plan\_definition for the class name of the task, and returns 'true' if a row is found. The constructor also runs a query on comm\_task\_handler by calling CommunicationManagemen tBridgeSNC.getHandler Instance\(\) for the task record class name.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1916650

 [KB2421892](https://hi.service-now.com/kb_view.do?sysparm_article=KB2421892)

</td><td>

Patterns on agent commands are randomly failing with allow list errors

</td><td>

Collecting MSSQL DB details using ACC discovery fails to fetch DB details with an error message. The exception occurred when executing a command on Agent. The error occurs when processing the adhoc check request: 'command failed due to allow list exclusion: Check command denied by the agent allow list. Context: Asset allow list empty, using agent config file allow list.'

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1930548

</td><td>

OfflineGlideRecord.get throws exception because generated SQL has mismatched table names

</td><td>

An error states that an action can't be performed offline.

</td><td>

1.  Create an extension of the wm\_task table called wm\_task\_2 and an extension of wm\_task\_2 called wm\_task\_3.
2.  Ensure there are some tasks that were created as wm\_task\_3.
3.  Download the offline cache and go offline.
4.  Navigate to a wm\_task\_3 task in the work order task list.
5.  Perform an action such as **Close Complete** on the task.

 Observe an error stating that the action can't be performed offline.

</td></tr><tr><td>

Mobile Platform

 PRB1931576

</td><td>

Offline-mode payload generation has excessive memory retention, causing performance degradation due to an SG offline document job

</td><td>

The Yokohama release introduced major changes to the way in which mobile offline payloads are generated, most notably embedded forms are now transformed into redirected forms. This removes the embedded forms from list screen documents and turns them into separate documents. With that change resulted in an increase in the number of documents that are processed during offline payload generation. This number can spike to as large as twice or three times as many documents processed compared to previous releases. As such, this results in an excessive number of GlideRecord instances being retained in memory. This has been seen to cause memory issues, node restarts, and severe performance degradation for users.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1931867

</td><td>

Cache generation timeout should be passed to client for polling timeout

</td><td>

The client stops polling five minutes into a large offline cache. As a result, offline cache generation is not retrieved by the client.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1897388

</td><td>

Content page fails to load via module after upgrade to Yokohama

</td><td>

The configured content page isn't loaded to a new browser tab. Instead, a blank page is loaded with view\_content.do?sysparm\_sys\_id=null at the end of the URL.

</td><td>

1.  Provision a Yokohama instance with the CMS plugin \(com.glide.cms\) installed.
2.  Open any base instance content page or custom content page.
3.  Select the **View Page** link, which loads the page content successfully.
4.  Open**System Definition** &gt; **Modules**.
5.  Select **New**.
6.  Enter the new module title information.
7.  Select the app in the **Application menu** field.
8.  Open the 'Link Type' tab.
9.  In the **Link Type** field, select **Content Page**.
10. In the **Content Page** field, look up to the content page that validated earlier.
11. Save the record.
12. Log in to the instance again or reload the home page of the instance to make sure the new module is visible via the navigator.
13. Select the module.

 Expected behavior: The configured content page is loaded to a new browser tab successfully.

 Actual behavior: A blank page is loaded with view\_content.do?sysparm\_sys\_id=null at the end of the URL.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1930430

</td><td>

An additional GraphQL request from nowAssistUtility has been observed to result in a 300ms slowdown during direct load scenarios

</td><td>

This occurs even when the plugin is not turned on.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1935679

</td><td>

Now Assist panel \(NAP\) shows blank screen after upgrading to Zurich

</td><td>

NAP loads blank after the user logs out of the instance and logs back in when using an incognito browser.

</td><td>

1.  Log in to an instance in an incognito browser.
2.  Load NAP.
3.  Keep NAP open.
4.  Log out of the instance without clearing the cache.
5.  Log in to the instance.

 Expected behavior: NAP loads without any issues.

 Actual behavior: NAP loads blank.

</td></tr><tr><td>

Now Assist Context Menu

 PRB1941573

</td><td>

Excessive occurrence of 'Security restricted: Unexpected Jelly Expression' warning in Zurich EA Release

</td><td>

Post Zurich Upgrade,there is an excessive occurrence of 'Security restricted: Unexpected Jelly Expression' Warning for some transactions.

</td><td>

1.  Hop to surfperfupg.
2.  Open Sales\_Opportunity.list.
3.  Select **New Note**.

 Notice that the warning does not appear on all transactions, it randomly appears on few transactions.

</td></tr><tr><td>

Now Assist Panel

 PRB1911693

</td><td>

Text in the 'Reply text' box is cut off

</td><td>

 

</td><td>

1.  Select **Now Assist panel \(NAP\)**.
2.  Verify the text in the reply text box.

 Expected behavior: The 'Assist' text is displayed.

 Actual behavior: The 'Assist' text is cut off.

</td></tr><tr><td>

Now Assist Panel

 PRB1916658

</td><td>

The hand cursor isn't displayed when hovering over the **Chat history** button

</td><td>

When the user hovers over the **Chat history** button, the I icon is displayed instead of hand symbol.

</td><td>

1.  Select **NAP**.
2.  Hover over the **Chat history** icon.

 Observe that the I icon is displayed instead of hand symbol.

</td></tr><tr><td>

Now Assist Panel

 PRB1929041

</td><td>

SKILL\_EXECUTION\_STARTED passes aiaExecutionPlanId as empty in its payload

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Select the sparkling icon to trigger AIEX.
3.  Keep the debugger at the SKILL\_EXECUTION\_STARTED' action handler.
4.  Trigger the 'Canvas flow' use case.

Observe that SKILL\_EXECUTION\_STARTED is passing 'aiaExecutionPlanId' as an empty value.


 Expected behavior: The aiaExecutionPlanId payload value should have execution planId of execution.

 Actual behavior: The aiaExecutionPlanId value is empty.

</td></tr><tr><td>

Now Assist Panel

 PRB1933709

</td><td>

Live agent is stuck in Now Assist panel \(NAP\)

</td><td>

The loading message continues when an error message should display instead.

</td><td>

1.  Select **NAP**.
2.  Enter 'Can you connect me to live agent'.

 Expected behavior: The message 'Hmm sorry live agent is not supported' should display.

 Actual behavior: The loading message keeps on loading.

</td></tr><tr><td>

Now Assist Panel

 PRB1934744

</td><td>

Selecting the skill doesn't work in NAP

</td><td>

 

</td><td>

1.  Select **NAP**.
2.  Enter 'Generate resolution notes'.
3.  Select **Generate resolution notes**.

 Observe that selecting the skill doesn't work; there's no response.

</td></tr><tr><td>

Now Assist Panel

 PRB1936169

</td><td>

Citation links are missing for the KB in the follow-up

</td><td>

 

</td><td>

1.  Open Now Assist panel \(NAP\).
2.  Enter 'What is spam'.
3.  Enter 'How to avoid it'.

 Expected behavior: The citation should be displayed as a link.

 Actual behavior: The citations are missing.

</td></tr><tr><td>

Now Assist Panel

 PRB1936922

</td><td>

Skills aren't turned off after being selected in the Now Assist Portal

</td><td>

Selecting skills doesn't turn them off.

</td><td>

1.  Open Now Assist Portal.
2.  Enter 'Summarize a record'.

 Expected behavior: 'Summarize a record' should be turned off after the record number question

 Actual behavior: The 'What is a record number' question is displayed but still summarize a record is turned on. It turns off after refreshing the page.

</td></tr><tr><td>

Now Assist Panel

 PRB1938963

</td><td>

Text is cut off in Now Assist panel \(NAP\) in the text area in Spanish

</td><td>

 

</td><td>

1.  Impersonate a user.
2.  Set the language as 'Spanish'.
3.  Select the **NAP** icon.

 Notice that the message in the text area is cut off.

</td></tr><tr><td>

Now Assist Panel

 PRB1941558

</td><td>

Now Assist panel \(NAP\) Assistant Information sources changes aren't saved in the guided setup

</td><td>

The NAP assistant default schema is set to 'None'.

</td><td>

1.  Navigate to **Conversational interface** &gt; **Assistants** &gt; **NAP assistant** &gt; **Information Sources**.
2.  Change the KG schema to an NLQ user graph.
3.  Select **Save and continue**.
4.  Return back to the tab to ensure the changes are saved.

 Expected behavior: The changes made in Information Sources saved.

 Actual behavior: The KG schema returns to 'None'.

</td></tr><tr><td>

Now User Experience

 PRB1925420

</td><td>

'Remove condition: \{0\} \{1\} \{2\}' doesn't get externalized

</td><td>

There's a 'Do not enter' icon in the row for each condition, which will delete the condition row. This is the value that's not being translated.

</td><td>

1.  Provision an instance with the German language pack installed.

To see all the language plugins, navigate to the v\_plugin\_list.do and search for '\*i18n'.

2.  Select the user profile.
3.  Select **Preferences**.
4.  Choose the German language.
5.  To turn on i8ln indicators, navigate to sys\_properties\_list.do and set glide.ui.i18n\_test to true.
6.  Navigate to sys\_report\_template.do.
7.  Add details for the report name.
8.  Select **Table** in the drop-down list.
9.  Select any table.
10. In the right nav, select the **Filter** icon to open the angular condition builder.

 Observe that there's a **Do not enter** icon in the row for each condition, which will delete the condition row. This is the value that's not being translated.

 The user can also inspect the source with dev tools or turn on the screen reader to validate the values for the delete row icon. There are then 2 scenarios for the screen reader value: An empty row, or a row with a field/operator/value \(which will also be translated\).

</td></tr><tr><td>

On-Call Scheduling

 PRB1930061

 [KB2498816](https://hi.service-now.com/kb_view.do?sysparm_article=KB2498816)

</td><td>

Rejection is not honored for email and Mobile push

</td><td>

For Email - remaining reminders are sent even after rejecting, but for MP the remaining reminders are not sent but the status is not updated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

On-Call Scheduling

 PRB1935013

</td><td>

Short description and Priority don't appear in the Teams notification modal for workflows

</td><td>

 

</td><td>

1.  Log in as admin.
2.  Create a shift and keep Contact Pre as Teams.
3.  Create a trigger rule For Workflows.
4.  Create an incident.
5.  Check the notification in Teams.

 Observe that the short description and priority don't appear in the Teams notification modal.

</td></tr><tr><td>

On-Call Scheduling

 PRB1938623

</td><td>

The Teams notification card does not show the incident number as a link when using subflows

</td><td>

 

</td><td>

1.  Log in as admin.
2.  Create a subflow trigger rule with assign by acknowledgment.
3.  Create a user with teams as the preference.
4.  Create an incident that triggers the trigger rule and sends a Teams notification to the user.

 Notice that the Teams notification card does not show the incident number as link

</td></tr><tr><td>

OneExtend

 PRB1925347

</td><td>

sys\_one\_extend\_definition\_attribute records aren't cached

</td><td>

AI Agent also queries for the records to execute tool type capabilities. When caching the records in One-Extend to get scriptable API to access the cached records in the AI Agent store app, the cache can be used.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1928470

</td><td>

Abnormal GAIC async submission duration

</td><td>

When the user calls certain code with an async request, the response time should be around 0-200 milliseconds. However, the reponse time can be as high as five seconds because the Builder Entity cache frequently gets reclaimed.

</td><td>

1.  Enable logging sn\_ais\_assist. AISearchNA4S GeniusResultLogger .level=INFO.
2.  Run NAVA QnA flow.
3.  Look at the Splunk log pattern 'AISearchNA4S GeniusResultLogger response received! duration'.

 Observe that the submission time can reach two to five seconds.

</td></tr><tr><td>

OneExtend

 PRB1929432

</td><td>

Improved accuracy of security detectors by leveraging attributes exclusion list

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1929447

</td><td>

Must increase prompt size to 40k

</td><td>

sys\_generative\_ai\_config and prompt \(Prompt Template\) is a max length of 4000 and clips on Oracle clients \(or any with strict column validation\).

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1931779

</td><td>

Single call for Guardian \(for Virtual Agent and agentic flows\)

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1933309

</td><td>

CheckLLMModelAvailability takes longer than usual

</td><td>

 

</td><td>

1.  Delete a record from sys\_gen\_ai\_model\_availability for gpt\_small.
2.  Trigger the script.

</td></tr><tr><td>

OneExtend

 PRB1934983

</td><td>

Few shot detector \(FSD\) is executing via Flow Designer \(FD\) sometimes in case of ASYNC + BLOCK

</td><td>

FSD is executing via FD sometimes even if the main capability is executing via proxy. When triggering AI Search, each capability execution FSD is triggered. FSD execution is happening via FD, and main capability execution occurs via JAVA. FSD should also execute via JAVA for ASYNC + BLOCK case.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1938158

</td><td>

Providers are restored to the default when plugins are repaired or when a new version is updated

</td><td>

After updating the provider to another, it gets set to the default again.

</td><td>

1.  Log in to the instance as an admin.
2.  Navigate to **Now Assist admin** &gt; **Settings** &gt; **Manage Model Providers**.
3.  Select **Edit Model Provider** &gt; **Customize** &gt; **Edit provider for skill**.
4.  Select a skill such as 'Incident summarization'.
5.  Update the provider to any other provider, such as Google or Amazon, except for the default one.
6.  Verify that the provider has been updated for the record summarization to Google in in sys\_one\_extend\_capability.
7.  Repair the UXC plugin or install the latest version.

 Notice that the provider is set to the default again.

</td></tr><tr><td>

OneExtend

 PRB1938540

</td><td>

Strange JSON format sources displayed in Now Assist Virtual Agent \(NAVA\) chatbot for certain queries

</td><td>

Issue is intermittent.

</td><td>

1.  Navigate to **/sp**.
2.  Enter the utterance **Create incident** in the NAVA chatbot.

 Observe the Planner 2 response displayed but with unexpected JSON-style sources output at the bottom.

</td></tr><tr><td>

OneExtend

 PRB1939640

</td><td>

Incident summarization doesn't work if the user enables Guardian in znowassiststable

</td><td>

 

</td><td>

1.  Enable offensiveness, block and log.
2.  Enable Prompt Inject Block and log.
3.  Navigate to any incident and update the short description as 'Lets kill all.'
4.  Select the **Summarize** button.
5.  Verify that it should get blocked with the error code in generative AI log table.

 Observe that summarizing the record in the incident is stuck and works fine if disabled.

</td></tr><tr><td>

OneExtend

 PRB1941124

</td><td>

Claude and streaming yields significantly malformed output

</td><td>

When the user enters the query in French for the first time, the streamed output has words stuck together. For example, 'basede' should be 'base de' and 'vousavez' should be 'vous avez'. When the user runs the query again, the issue doesn't persist.

</td><td>

1.  Ensure the instance has Claude, has streaming on, and has Dynamic Translation off.
2.  Navigate to **/sp**.
3.  Open the Now Assist Virtual Agent \(NAVA\) chatbot.
4.  Enter the utterance, 'Quelles sont les options pour créer une base de connaissances?'.

Observe that the streamed output has several words mashed together. Also observe that in the sys\_generative\_ai\_log planner 2 output, the response from LLM itself is this way.

5.  Disable streaming.
6.  Repeat the query.

 Notice that there is no issue with the words being stuck together in the output.

</td></tr><tr><td>

OneExtend

 PRB1942490

</td><td>

KB generation isn't working when requested from Now Assist panel \(NAP\)

</td><td>

 

</td><td>

1.  Log in to the instance.
2.  Activate all FSM skills.
3.  Ensure the credentials for Now LLM are updated with proxy.
4.  Navigate to **NAP**.
5.  Select **Generate KB Article**.

 Expected behavior: KB generation happens successfully.

 Actual behavior: Notice the error message, 'Sorry, there was a problem on my side trying to complete this request. Try asking again later,' and that there's an error in the sys\_generative\_ai\_log.

</td></tr><tr><td>

OneExtend

 PRB1942618

</td><td>

Script include-based capabilities aren't executed as a subflow though the required sys property is enabled

</td><td>

 

</td><td>

1.  Create a Gen AI capability with it's definition pointing to script include.
2.  Ensure the sys prop 'com.glide.oneapi.run\_ script\_include\_on\_fdih \_engine' is set to 'True'.
3.  Ensure flow debugging is turned on for the subflow.
4.  Run the script include as an FDIH subflow.
5.  Execute the capability from 1 using OneExtendUtil. execute api.

 Expected behavior: The script include is executed as a subflow and subflow executions should execute.

 Actual behavior: The subflow 'Run script include as FDIH subflow' won't show any executions.

</td></tr><tr><td>

OneExtend

 PRB1944861

</td><td>

Revert NASK licensing charge by token to not include input tokens

</td><td>

The assist charge logged in sys\_gen\_ai\_usage\_log is based on 1 assist per 1000 tokens, where tokens = input tokens + 3 \* output tokens.

</td><td>

Invoke the custom skill created in the NA Skill Kit.

 Observe that the assist charge logged in sys\_gen\_ai\_usage\_log is based on 1 assist per 1000 tokens, where tokens = input tokens + 3 \* output tokens.

</td></tr><tr><td>

Performance Analytics

 PRB1930855

</td><td>

An incremental mining job does not transfer changes to delta changes for the first time

</td><td>

Changes are not transferred to pa\_dm\_delta\_changes.LIST.

</td><td>

1.  Enable Data snapshots for an indicator on incident table or create a Data snapshot source on incident table.
2.  Run first day mining.
3.  Insert/update records in the incident table and
4.  Verify that changes are being tracked in the cdc\_queue\_par table.
5.  Run Incremental mining job.

 Observe that changes are not transferred to pa\_dm\_delta\_changes.LIST

</td></tr><tr><td>

Performance Analytics

 PRB1932734

</td><td>

Remove Guard Rails

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Performance Analyzer

 PRB1917732

</td><td>

Performance Analyzer has incorrect data required for data broker visualization

</td><td>

The data retrieved by performance analyzer incorrectly queries for the keys 'd' and 'cex' in the additional data column on the syslog\_transaction table. These two values were updated to 'du' and 'ce' respectively, resulting in invalid data in the application.

</td><td>

1.  Navigate to Performance Analyzer.
2.  Navigate to the trace page.

Notice that every data broker entry shows a 0ms execution time.

3.  Open developer tools and inspect network tab.
4.  Open the trace network call.

 Notice that every data broker JSON entry has the value of 'null' for the duration.

</td></tr><tr><td>

Performance Analyzer

 PRB1928791

</td><td>

Performance Analyzer is not accessible via Application Navigator on Yokohama or Xanadu instances

</td><td>

Performance Analyzer is not accessible via Application Navigator on Y or X instances.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1890523

</td><td>

Committing update sets with dashboard changes doesn't clear the par\_dashboard\_cache

</td><td>

After the user commits the update set, the dashboard changes don't show up in the new instance because the par\_dashboard\_cache isn't cleared.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Filters

 PRB1907093

</td><td>

Filter doesn't work in Yokohama for users without elevated privileges

</td><td>

After upgrading to Yokohama, users without elevated privileges can't filter a list if the table/data source is a DB view. The list doesn't follow the filter and continues to show all records.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1905573

</td><td>

Migrated Spline time series with drilldown does not work inside PAE dashboard but works in viz designer

</td><td>

The user observes an error.

</td><td>

1.  Set 'com.glide.par.unified\_analytics.enabled' property to false.
2.  Create a spline report add the drilldown to pie report.
3.  Add it to a Core UI dashboard.
4.  Use migration center to migrate.
5.  Open **Compare** in dashboard.
6.  Select the spline chart.

 Observe an error.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1910729

</td><td>

Setting the property com.glide.par.coreui\_single\_migration.enabled to false causes the message 'Cannot migrate icon' to display

</td><td>

The icon and the banner should not be shown when the property is false.

</td><td>

1.  Set the unified property to false.
2.  Create a Core UI dashboard with a pie report.

Observe that it has banner to switch Next Experience.

3.  Change the value of the 'com.glide.par.coreui\_single\_migration.enabled' property to false.
4.  Refresh the Core UI dashboard.

 Notice a question mark icon and a message stating that this dashboard cannot be migrated to Next Experience as it has unsupported widgets.

</td></tr><tr><td>

Platform Encryption

 PRB1886119

</td><td>

Protect your data applied, available protection issues for FE, anonymization and ZTA.

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Platform Licensing

 PRB1920415

</td><td>

During instance startup, Zurich far nodes take extra time

</td><td>

Node startup is slowed by inefficient database queries during the licensing cache initialization. The root cause is the repeated invocation of the TableDescriptor cache, which is especially impactful on standby nodes where DB access is slower. In environments with ~2000 custom DB object entries, this compounds to create significant restart delays.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1934746

</td><td>

Playbooks archived in Xanadu don't work in newer releases

</td><td>

New fields that get added to the deserializer need to handle the keys not existing, which, as of now, is snapshot\_id and variant\_id.

</td><td>

1.  Create an X instance.
2.  Trigger a playbook.
3.  Complete/cancel the playbook.
4.  Archive the playbook.
5.  Upgrade the instance to Yokohama.
6.  Open the playbook.

 Expected behavior: The playbook loads.

 Actual behavior: The playbook doesn't load - 'No stages available'.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1935764

</td><td>

Playbook and Stage permissions aren't evaluated by Record Generator Provider

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1913757

</td><td>

No warning message is displayed when the **Update and Retrain** button is selected for clustering

</td><td>

When the user selects the **Update and Retrain** button for clustering, a new version is created for the capability and no warning message is displayed.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1920120

</td><td>

The size limit for unassigned records causes data loss in the clustering output

</td><td>

 

</td><td>

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Clustering**.
2.  Select **Create a Solution Definition**.
3.  Test it.
4.  Run it.

</td></tr><tr><td>

Process Mining

 PRB1921496

</td><td>

The scheduled task name is reset to default if it's renamed when the task is being processed on glide

</td><td>

If the user renames the scheduled task while it's being pre-processed to send to trainer, the name is reset. When the system updates the scheduled task state, it also updates the task with the older, default name.

</td><td>

1.  Apply a transition filter.

Notice that a scheduled task is created and pre-processing starts. The scheduled task is loaded in memory with the default name.

2.  Update the scheduled task name.

 Observe that the schedule task pre-processing completes and the trainer job is submitted. When the system updates the schedule task state, it also updates the name with the older, default name.

</td></tr><tr><td>

Process Mining

 PRB1928656

</td><td>

Meter-based licensing should count only parent entity cases when collecting data for metering

</td><td>

Case id entries appear for both parent and child entities.

</td><td>

1.  Enable a meter-based license.
2.  Configure an MDM project.
3.  Mine a project.

 Notice that the promin\_meterd\_usage table has entries for case ids of both parents and child entities.

</td></tr><tr><td>

Project Management

 PRB1905989

</td><td>

The **Create Expenseline** button from the new costplan split button doesn't create a system generated costplan

</td><td>

The widget is updated, but no new system-generated costplan is created.

</td><td>

1.  Create any planning item.
2.  Add a costplan initially.
3.  Select **New Expenseline** on the costplan split button.
4.  Add the details but don't associate it with any costplan.
5.  Save the expenseline side panel.

 The actuals widget is updated, but no new system-generated costplan is created.

</td></tr><tr><td>

Project Management

 PRB1918462

 [KB2532380](https://hi.service-now.com/kb_view.do?sysparm_article=KB2532380)

</td><td>

The system throws an error and a Resource Allocation record is not created upon creation of a Resource Assignment record on a Project Task

</td><td>

The user observes an error while generating a resource allocation record during the creation of a resource assignment record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Project Management

 PRB1921008

</td><td>

Without integrations, updated costplans for planning items aren't reflected on the portfolio plan page

</td><td>

 

</td><td>

1.  Make sure the integrations are not enabled.
2.  Create a portfolio.
3.  Create a demand.
4.  Add a costplan into the demand.
5.  Navigate back to the portfolio plan page.

Observe that the values are reflected appropriately.

6.  Open the same demand and update the costplan.

 Observe that the values are not reflected in the portfolio plan page.

</td></tr><tr><td>

Related List Action Model

 PRB1890337

</td><td>

The button to change the fields for the related list is grayed out

</td><td>

The declarative action \(DA\) is not enabled.

</td><td>

1.  Log in to a base instance.
2.  Identify any declarative action on a related list in a configurable workspace.
3.  Open the DA record in the backend.
4.  Set 'Enable Dynamic Condition' to 'True'.
5.  Add a filter condition with a dot-walked field.
6.  Save the record.
7.  Open the workspace.
8.  Select **Select all x records**.

 Notice that when the user selects **Select All**, the DA with the dynamic evaluation condition is grayed out.

</td></tr><tr><td>

Reporting

 PRB1916106

</td><td>

Loading is slow for synchronous calls by related list from a report on sys\_user table

</td><td>

When a user tries to open a report, the related list call is synchronous, which results in slow loading times. Instead, the related list call should be asynchronous, which wouldn't block the main list or prevent access to it.

</td><td>

1.  Create or open a report on sys\_user.
2.  In the 'Network' tab of the Developer Console, add '/api/now/ui/related\_list/related/sys\_user/all' in the filter.
3.  Perform a /cache.do in another tab.
4.  Refresh the report.

Notice that the API call is in a pending state for over a minute.

5.  Select **Run**.

 Observe that 'Loading Report' is shown until the status of API call is finished.

</td></tr><tr><td>

Roles

 PRB1890898

</td><td>

UserHasRole PatchJob may inadequately update user role inheritance if it processes a user prior to original transaction \(M2MSlushbucketSaveJob\) completion

</td><td>

After performing an action that impacts a large number of role inheritances, the expectation is that operation will be required to process a considerable number of users. This results in M2MSlushbucketSaveJob running for several minutes to allow UserHasRolePatchJob to run while M2MSlushbucketSaveJob is still in progress.

</td><td>

1.  Set up an instance to take advantage of fix provided in PRB1744106.
2.  Set the system property 'glide.security.inh\_count\_patcher.enabled' to 'true'.
3.  Generate a relatively complex user-group-roles structure.
4.  Perform an action that is expected to impact a large number of user roles inheritances \(sys\_user\_has\_role\), for example, removing a contain relationship between two roles.
5.  Review user role inheritance post completion of M2MSlushbucketSaveJob.
6.  Run the new RoleManagementVerify\(\).verifyInheritedRoles\(\); via scripts background.

 Observe that role inheritance mismatches occur related to the role involved in the operation performed in step 3.

</td></tr><tr><td>

Scan Engine

 PRB1934227

</td><td>

Create a global family release plugin

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Seismic Framework

 PRB1919027

</td><td>

Document requests end up using outstanding child prefetch promise

</td><td>

In certain scenarios, the Service Worker incorrectly fulfills a main page request using a pending iframe request. This occurs when the Service Worker matches the main page request to an existing pending iframe request, resulting in the main page loading the iframe's content instead of its own. This leads to incorrect rendering and potential functional issues on the main page.

</td><td>

1.  Open any UI16 page on a Next Experience enabled instance.
2.  Wait for the page to load.
3.  Reload the same page several times \(5+\).

 Expected behavior: The navigation bar and shell to show up with UI16 content all the time.

 Actual behavior: Only UI16 content is shown on the page. The navigation bar and shell are missing.

</td></tr><tr><td>

Server-side scripts

 PRB1881845

</td><td>

globalThis isn't correctly shared between separate imports of the same module

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1895613

 [KB2215450](https://hi.service-now.com/kb_view.do?sysparm_article=KB2215450)

</td><td>

There's different behavior in the JSUtil.isEmpty function after the upgrade from Washington to Yokohama

</td><td>

In Xanadu and later, the scripting engine doesn't properly iterate over the characters of strings. The JSUtil.isEmpty function uses iteration as a generic way to check both array and string inputs for emptiness, and the underlying change in string iteration breaks this pattern.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog

 PRB1929611

</td><td>

E2E time for catalog generation use case is greater than 10 seconds \(SLA\)

</td><td>

 

</td><td>

1.  Consider the latest track and complete the setup for text to catalog with latest snapshot versions.
2.  Consider a prompt which would create a 8–9 questions.
3.  Measure the time taken for the API to create the item \(The 'Generation of Catalog Item' scripted rest resource\).

 Notice that the time is greater than 10 seconds.

</td></tr><tr><td>

Service Catalog

 PRB1935961

</td><td>

Change 'va\_render\_type' from a Calculated to Static field

</td><td>

Change 'conversational\_render\_type' to non-calculated field

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1936035

</td><td>

Modify mapped application services limit to only apply to records with type != 0

</td><td>

The system limits the total number of mapped application services.

</td><td>

 

</td></tr><tr><td>

ServiceNow Voice for IT Service Management

 PRB1899268

</td><td>

Upgrade the Node.js version to 22

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1924949

</td><td>

On i18n, "Of" is hardcoded

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portfolio Management

 PRB1907918

</td><td>

Display name is changed from asset availability to configuration Item after running a scheduled job

</td><td>

The display name should be Asset Name.

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1928878

</td><td>

Private conversations are visible to users on the sidebar

</td><td>

This issue occurs when impersonating a user who is in the discussion ends the impersonation, and then impersonates a user that isn't a participant in the discussion.

</td><td>

1.  Impersonate any user.
2.  Navigate to any workspace.
3.  Open an incident that is in an 'Open' state.
4.  Select **Discuss**.
5.  Enter necessary mandatory info.
6.  Add a user as a participant.
7.  End the impersonation.
8.  Impersonate a different user not participating in the discussion.
9.  Load the same Incident with the discussion.

Notice that there's an entry for the discussion that the user isn't a participant in is visible in the record's activity stream .

10. Select **Open Discussion**.

 Expected behavior: Only users who are a participant should see the chat conversation.

 Actual behavior: Users that aren't participants in a private chat are still able to see the chat conversation.

</td></tr><tr><td>

Software Asset Management

 PRB1909356

 [KB2247602](https://hi.service-now.com/kb_view.do?sysparm_article=KB2247602)

</td><td>

The recon job fails when custom products don't have the **Publisher** field stamped

</td><td>

The recon job fails when custom products don't have the **Publisher** field stamped due to some data corruption. All custom products usually have a publisher stamped, because the business rule 'Process before create or update action' stamps the **Publisher** field by resolving it from the **Manufacturer** field.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1915761

 [KB2517876](https://hi.service-now.com/kb_view.do?sysparm_article=KB2517876)

</td><td>

An 'Install' table has a cross-scope issue since the code is moved to Store

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1936688

</td><td>

Add-On Publisher values are not populated properly

</td><td>

When Content is shipping Add-On Publisher lifecycles, it gets defaulted to Publisher value instead of Add-On Publisher.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1938025

</td><td>

Label for ELP Grouping results table misnamed as 'Extended License Position Results' instead of 'Effective License Position Results'

</td><td>

 

</td><td>

Navigate to the license workbench, then ELP Grouping tab.

 Observe the label of the table starts with Extended instead of Effective.

</td></tr><tr><td>

Software Asset Normalization

 PRB1862904

 [KB1968357](https://hi.service-now.com/kb_view.do?sysparm_article=KB1968357)

</td><td>

The 'SAM - Find Normalization Suggestions' job fails when there are Discovery models with an empty version

</td><td>

.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Normalization

 PRB1938991

</td><td>

clearNormFieldsForNonLicensableInstalls is called for every DM during normalization of DM

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Models

 PRB1902396

</td><td>

Query errors display on a Software Model record due to a client-side GlideRecord query

</td><td>

There's a discrepancy in a client script with the 'Show/Hide Suggestion' icon between the roles that can access cmdb\_model\_software records and those that can access samp\_software\_model\_suggestion records.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB1933518

 [KB2515608](https://hi.service-now.com/kb_view.do?sysparm_article=KB2515608)

</td><td>

Default queue provisioning fails during upgrade

</td><td>

Default queue provisioning fails during the upgrade process with the message 'invalid table: sysevent\_queue\_provider\_param, state: Failed'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Telemetry Glide Infrastructure

 PRB1920545

</td><td>

CDC replication disables batch DB update operations on replicated tables causing increased upgrade time on instances

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1934015

</td><td>

A user with the role of territory\_resource\_manager and added in territory can view a territory membership record

</td><td>

 

</td><td>

1.  In an existing territory X, add User X is added as territory manager.
2.  Give User X role of territory\_resource\_manager \(do not give it territory\_basic\).
3.  Impersonate as User X, and check any territory membership record of territory X.
4.  Verify User X is actually able to view the territory\_membership record.

 This should not happen as User X doesn't have territory\_basic role \(stamped to territory model\). Similar doesn't happen if User X has territory\_read role instead \(territory\_membership record is denied access as it doesn't have territory\_basic\).

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1915159

</td><td>

Failed tier two chunks can block additional chunks for a rule from being processed

</td><td>

If tier two chunks continue to fail when retried, they can block additional chunks for a rule from being processed.

</td><td>

1.  Generate a record with an offload that perpetually breaks.
2.  Make it fail on offload with a 60-minute retry period.
3.  Archive other records that would get offloaded by the same rule.

 Observe that the records in step three never get offloaded.

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1920238

</td><td>

Cloning instances to/from the instance where the Tier 2 plugin is enabled can lead to loss of configuration, metadata, and orphaned data

</td><td>

Cloning instances can lead to the loss of Tier 2 configuration, metadata, and orphaned data, especially when Tier 2 is only partially configured across environments. The clone behavior should be improved so that the Tier 2 bucket configurations, plugin state, and offload capabilities are preserved and validated appropriately, ensuring no data/configuration work is unintentionally lost.

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1923245

</td><td>

The IllegalMonitorStateException in WaiterCountManager can prevent locked threads from being unlocked and lead to a deadlock

</td><td>

There's a race condition between a new thread pool addition during a specific plugin installation and locking thread-pool queues to claim a transaction for processing. This could cause a potential deadlock.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1926606

</td><td>

On i18n, "Of" is hardcoded

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1901518

</td><td>

Tree structure does not function as expected

</td><td>

The tree structure should receive focus only once via the Tab key. Pressing Tab again should move focus to the next element instead of navigating within the tree structure. Navigation within the tree structure must be with arrow keys. However, the tree nodes are accessible using Tab key and arrow keys.

</td><td>

1.  Launch any base instance.
2.  Navigate to **Application navigator** &gt; **All** &gt; **Email content**.
3.  Open a record.
4.  Navigate to the folder structure in the record and access using the keyboard.

 Expected behavior: The tree structure should receive focus only once via the Tab key. Pressing Tab again should move focus to the next element instead of navigating within the tree structure. Navigation within the tree structure must be with arrow keys.

 Actual behavior: Notice that the tree nodes are accessible using Tab key and arrow keys

</td></tr><tr><td>

UI Form Administration

 PRB1918236

</td><td>

Child Incidents Related List gets populated with All available incidents

</td><td>

When a query for a related list row count is disabled, the Child Incidents Related List gets populated with all available incidents. This issue works as expected in Yokohama, but not in Zurich.

</td><td>

1.  Add a few records to the Child Incidents related list.
2.  Check the same incident in both UI16 and Service Operations Workspace \(SOW\).Notice that the related list count is correct.
3.  Navigate to **sys\_ui\_list\_control.list**.
4.  Open a record for 'Table=incident' and 'Label=Child Incidents'.
5.  Navigate to the 'Performance' tab.
6.  Select the boxes **Remove pagination count** and **Omit related list count**.
7.  Open the incident via SOW.
8.  Select the 'Related records' tab.

Notice that without selecting the Child incidents list, the count remains 0.


 Expected behavior: The count is correct.

 Actual behavior: All incidents are appearing on the list.

</td></tr><tr><td>

UI Form Administration

 PRB1920499

</td><td>

The snFormDataConnected\{headerConfig...\} GQL call occurs during the 'Create case' flow

</td><td>

When the user creates a case, the snFormDataConnected\{headerConfig...\} call goes out, even though it isn't needed during this flow.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1926448

</td><td>

After upgrading to Yokohama, the 'Before Query' business rule doesn't filter records in the Workspace using an encoded query

</td><td>

Adding an encoded query on a 'Before Query' business rule to a filter record restricts the record on UI16, but fails to filter the record in Workspace. The record doesn't open in UI16, but opens successfully in Workspace. This issue was found in Yokohama and Zurich.

</td><td>

1.  Create a 'Before Query' business rule on the incident table.
2.  Create an incident with a short\_description.
3.  Set it to 'test'.
4.  Attempt to open the record in UI16 and Workspace.

 Notice that the record doesn't open or filter the record properly.

</td></tr><tr><td>

Upgrade Center

 PRB1897157

</td><td>

Load order is not maintained for duplicate files in global hosted plugins

</td><td>

Certain global hosted plugins may share duplicate files with other distribution plugins and global hosted plugins. The problem is that their information is not available in upgrade\_manifest.csv but rather available in the package\_inventory.csv files contained in the host app packages.

</td><td>

1.  Install hosted plugins.
2.  Upgrade an instance.

 Expected behavior: Load order is maintained during plugin loading for hosted plugins for duplicate files.

 Actual behavior: Load order is different.

</td></tr><tr><td>

Upgrade Center

 PRB1933942

</td><td>

Skipped error after upgrading \(sys\_properties\_9c6e0280ff3122101b7fffffffffffd9\)

</td><td>

The user gets a skipped error after upgrading the instance from Xanadu to Yokohama. The reason is 'Skipping unavailable system property glide.db.df\_engine.enabled. Users cannot configure this property.' It's included in the plugin 'com.snc.db.df\_engine'.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1904647

</td><td>

Support for invoking the Valk API is missing through the Service proxy

</td><td>

Enable the UXA Service proxy to securely query data from the Query Service efficiently

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1915455

</td><td>

Upon resizing the window, the alert content from viewport doesn't change in accordance with the dimensions

</td><td>

An alert comes from viewport Link labelLink that opens in new window or tab.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1890524

</td><td>

Increase in heap utilization due to expression cache for search

</td><td>

This issue occurs from a script include expression cache from platform.

</td><td>

1.  Set up Now Assist Virtual Agent \(NAVA\) on a Yokohama instance.
2.  Perform search actions from the chat window.

 Notice that the load of 25 users on a single node for one hour for the search action performed occupies more than 500MB.

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

 PRB1911010

</td><td>

With DTAC enabled and an agent name showing in the Virtual Agent Header, VA uses an incorrect name

</td><td>

From the end-user perspective, an Agent's full name is displayed.

</td><td>

1.  Modify the 'Name' column for an Agent \(for example, Abel Tuter\) in the live\_profile table.
2.  Verify that the Live Profile name is changed to something like 'abel@example'
3.  With the Agent user, navigate to CSM/FSM or SOW.
4.  Make the agent 'Available for chat' with the agent's language set to English.
5.  Connect with another user in another window with the language preference set to a language other than English.
6.  Navigate to /sp and Open Virtual Agent.
7.  Start a Live Agent conversation.
8.  Check the title on the chat window.
9.  Accept the chat as the agent.

 Observe the chat title is changed from 'Abel@example' to 'ABEL TUTER'.

</td></tr><tr><td>

Virtual Agent

 PRB1913154

</td><td>

Non-actionable notifications under regular cases create interaction records for channels and NASS

</td><td>

For channels and NASS, it creates a conversation and does a silent handshake for NASS/NAVA. This creates a conversation and an interaction internally, which is incorrect.

</td><td>

1.  Make sure that the user has had some conversation with NASS/Channel.
2.  Trigger a non-actionable notification.

 Expected behavior: A conversation associated with the notification shouldn't have an interaction record.

 Actual behavior: An interaction record is created.

</td></tr><tr><td>

Virtual Agent

 PRB1915544

</td><td>

The Virtual Agent \(VA\) topic execution returns a tool response instead of a main skill

</td><td>

The VA topic execution should return a main skill response or provide a way for the user to configure the topic to return a main skill response. Instead, the VA topic execution returns RAG response.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1915775

</td><td>

Tool editor execution time impacts the performance for flow generation requests

</td><td>

The tool editor execution time can take over 2000 milliseconds. As the flow generation oneExtend requests are under 10 seconds, this additional time causes an impact to the performance and bumps up the performance metrics by 20%.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1917144

</td><td>

Non-LLM time takes an extra 120–581 milliseconds for NAVA use cases and 500–900 milliseconds for NAP Skill/Topic execution

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1922205

</td><td>

Planner1 output displays multiple times when only dynamic translation is on

</td><td>

 

</td><td>

1.  Navigate to Service Portal.
2.  In the NAVA chatbot, enter the utterance 'Mi portátil ha sido arruinado por las cookies. ¿Qué son siquiera las cookies? ¿Puedo pedir un portátil nuevo?'.

 Observe that the transition message is displayed multiple times in Virtual Agent. This is consistently reproducible.

</td></tr><tr><td>

Virtual Agent

 PRB1922860

</td><td>

Auto-chat with September agentic pipeline has issue with follow-ups

</td><td>

There's a difference in behavior with the new September agentic pipeline when compared to the July pipeline. With the older pipeline, the auto-chat asks follow-ups for several turns until the objective is satisfied. With the new pipeline, it often stops after a few queries, even if the response doesn't satisfy the objective. This is causing scores to decline.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1923219

</td><td>

The live agent conversation banner stays on 'Cancel request' even after the user has canceled the request

</td><td>

On ending a live agent conversation, users get an empty skill picker topic and the client is able to understand that there's a new message coming in and ends the spinner display. However, no such message comes in and users are stuck in the routing to the live agent spinner.

</td><td>

1.  Navigate to Dynamic Window.
2.  Type and connect to a live agent.
3.  From the user side, select **Cancel**.

 Expected behavior: The chat is canceled and the banner changes to the requested query title.

 Actual behavior: When the requester selects the **Cancel** button, the original created work item is canceled but 'routing to live agent' won't disappear from the chat window.

</td></tr><tr><td>

Virtual Agent

 PRB1924015

</td><td>

There's a missing chunk during the AmazonBedrockStream process

</td><td>

There are some missing chunks when the build agent tries to create an app and provides any instructions to the Amazon Bedrock in stream mode. Because of this, the subsequent request fails.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1925332

</td><td>

Processing messages APIs are slow

</td><td>

The processing messages APIs take more than 400 milliseconds.

</td><td>

1.  Create a topic.
2.  Add the following statements in it: vaSystem.sendProcessingMessageDirectly\('testing'\) and vaSystem.updateDynamicProgressMessage\('COMPLETED'\)./

 Observe that both APIs take more than 400 milliseconds, approximately.

</td></tr><tr><td>

Virtual Agent

 PRB1925501

</td><td>

Default context profile 'Default Experience for Now Assist' is missing a guardian message

</td><td>

The context profile that was set up doesn't contain a guardian message, and when attempting to get it from the default context profile which also doesn't have a guardian message, no message appears.

</td><td>

1.  Set up a context profile without a guardian message.
2.  Set up an assistant with the context profile setup in Step 1.
3.  Open Now Assist Virtual Agent \(NAVA\).
4.  Enter something that is restrictive so it goes through the guardian flow.

 Expected behavior: The user should see a guardian message, and an empty skill picker should be shown.

 Actual behavior: The user doesn't see the guardian message, but sees empty skill picker.

</td></tr><tr><td>

Virtual Agent

 PRB1926480

</td><td>

SQL does a table scan on sys\_cs\_message table, causing 150 milliseconds non-LLM time degradation

</td><td>

SQL does a table scan on sys\_cs\_message table for serial number, resulting in 150 milliseconds of non-LLM time degradation. This can be seen when the user performs load testing or creates a conversation with a large number of records in the sys\_cs\_message table \(1000K\).

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1926804

</td><td>

Investigate 300ms delta before the AI agent executor invocation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1926867

</td><td>

The skillParams in a session context isn't persisted

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1927571

</td><td>

SessionManager and MacMessageBatchingSession is caching rhino objects contributing to higher heap usage

</td><td>

With a cache using around 150+ MB, storing rhino scope objects within a cache make it unexpectedly large depending on the GlideRecord queries that they run or JavaScript objects stored in the scope.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1927978

</td><td>

Change the column type from 'Name-Value Pairs' to 'String' in the table sys\_cs\_one\_extend\_invocation

</td><td>

 

</td><td>

1.  Set up NAVA.
2.  Turn on Agentic Mode.
3.  Execute 'What is spam?'
4.  Check the profiler stack trace.

</td></tr><tr><td>

Virtual Agent

 PRB1927985

</td><td>

The synthesized response doesn't get sent immediately due to the message batching causing visual time degradation

</td><td>

There's a delay in sent time and AMB received time in the web client.

</td><td>

1.  Set up NAVA.
2.  Search 'What is spam?'

 Observe that there is a delay in sent time \(get sendTime from 'Serialized cometd message' column payload in sys\_amb\_message table\) and AMB received time in the web client.

</td></tr><tr><td>

Virtual Agent

 PRB1928257

</td><td>

Virtual Agent API needs to be fixed so that roles are assigned correctly

</td><td>

Messages are labeled as 'user', even if sent by a bot.

</td><td>

1.  Start a conversation with the bot \(for example, through Voice Agent\).
2.  Send a few messages as the user and let the bot respond.
3.  Call an API for that conversation.
4.  Check the API response and look at the role field for each message

 Notice that messages are labeled as 'user', even if sent by a bot.

</td></tr><tr><td>

Virtual Agent

 PRB1928390

</td><td>

Executing the Live Agent skill from the picker with Agentic runs into a fallback error

</td><td>

When the user selects the **Now Assist Live Agent** skill from the picker, the message 'there are no Live agents available' appears, followed by a fallback error.

</td><td>

1.  Navigate to NAVA.
2.  Select the **Now Assist Live Agent** skill from the picker.

 Expected behavior: The user gets the message 'there are no Live agents available' and the chat closes.

 Actual behavior: The user gets the message 'there are no Live agents available', followed by a fallback error.

</td></tr><tr><td>

Virtual Agent

 PRB1930014

</td><td>

The true-up version in repo files needs to be updated post-sign off

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1930434

</td><td>

Multilingual functionality is broken, and the complete flow is not working as expected

</td><td>

This issue was observed in Yokohama with RAG 3.0.4 after the ynowassist nightly build occurred.

</td><td>

1.  Impersonate as user with Japanese session language.
2.  Ensure 'glide.sys.language' system property is in Japanese with the system property value would be 'ja'.
3.  Create a skill.
4.  Add RAG as tool.
5.  Execute the skill.

 Expected behavior: The skill and RAG tool should execute successfully.

 Actual behavior: RAG is failing with attached error.

</td></tr><tr><td>

Virtual Agent

 PRB1931090

</td><td>

A conversation gets stuck when Planner 1 fails an action with 'Unknown finish type'

</td><td>

If 'ITSM incident resolution agent' can't find the resources it needs, it gives a fallback response and returns control to Planner 1. Planner 1 gives a reply but this is never shown to user and control never returns to user in chat. It's stuck on 'formulating a final response'.

</td><td>

1.  Navigate to an instance.
2.  Query 'create a resolution plan for INC0000055'.
3.  An ITSM incident resolution agent can't find similar KBs so it gives a fallback message.

 Expected behavior: Planner 1 returns control to the user and possibly displays a 'if you need further assistance' message.

 Actual behavior: It's stuck forever with a spinning wheel 'formulating a final response'.

</td></tr><tr><td>

Virtual Agent

 PRB1931649

</td><td>

The mid-topic switch doesn't work in full agentic mode

</td><td>

The user can't return to the previous topic. Instead, the message 'Sorry, there was a problem on my side' appears.

</td><td>

1.  Navigate to /sp.
2.  Query 'I want to order coffee'.
3.  Start the topic, then in mid-topic query: 'I actually want Miro access.'
4.  Select the **Continue request: Order Coffee** card.

 Expected behavior: The user is able to go back to the order coffee topic.

 Actual behavior: The user receives the message 'Sorry, there was a problem on my side'.

</td></tr><tr><td>

Virtual Agent

 PRB1931987

</td><td>

The **Search** button doesn't show up on DW

</td><td>

On a portal with DW enabled, the **Search** button doesn't appear next to the feedback icons.

</td><td>

1.  Navigate to a portal with DW enabled.
2.  Enter 'What is spam?'

 Expected behavior: The **Search** button appears next to the feedback icons.

 Actual behavior: The **Search** button doesn't appear.

</td></tr><tr><td>

Virtual Agent

 PRB1932193

</td><td>

An auto-evaluation run is stuck on 'In progress' when the language is set to Japanese

</td><td>

The evaluation run is stuck on 'In progress' even though the metric result and batch result has completed.

</td><td>

1.  Install the Japanese translation app.
2.  Set up the Azure OpenAI connection/endpoint.
3.  Navigate to **sys\_properties**.
4.  Set the 'glide.sys.language' value as 'ja'.
5.  Navigate to **Preferences**.
6.  Change the language to Japanese.
7.  Create an Azure Open AI skill with the prompt 'generate trivia: \{\{context\}\}' where the context is the skill input of the type string.
8.  Finalize the prompt.
9.  Create a dataset using 'sys\_user' records mapping to the name.
10. Create a new evaluation run enabling all the available evaluation methods.

Observe that the evaluation run is not completing.

11. Check the sys\_one\_extend\_batch\_run.

 Observe that the metric result and batch result has completed.

</td></tr><tr><td>

Virtual Agent

 PRB1932275

</td><td>

Processing messages APIs are slow

</td><td>

The processing messages APIs take more than 400 milliseconds.

</td><td>

1.  Create a topic.
2.  Add the following statements in it: vaSystem.sendProcessingMessageDirectly\('testing'\) and vaSystem.updateDynamicProgressMessage\('COMPLETED'\)./

 Observe that both APIs take more than 400 milliseconds, approximately.

</td></tr><tr><td>

Virtual Agent

 PRB1932396

</td><td>

Add processing messages for QnA to handle scenarios where Planner1 returns a response in an older format

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1933049

</td><td>

Conversation errors out

</td><td>

The conversation errors out in three scenarios.

</td><td>

Scenario 1:

 1.  Start a conversation from Dispatcher Workspace \(DW\).
2.  Search for Order Laptop with accessories with an agent.
3.  Execute the agent.

 Notice that the conversation errors out mid-way.

 Scenario 2:

 1.  Start a conversation from DW.
2.  Search for any catalog.
3.  Attempt to execute the catalog from the Search Result.

 Notice that the conversation errors.

 Scenario 3:

 1.  Start a conversation from DW.
2.  Search for any Virtual Agent topic.

 Notice that the conversation errors.

</td></tr><tr><td>

Virtual Agent

 PRB1933055

</td><td>

Race condition occurs in a full agentic instance

</td><td>

The response generation step doesn't occur when multiple responses arrive at the same time.

</td><td>

Fire a few of parallel LLM calls during the planner invocation.

 Notice that when multiple responses arrive approximately at the same time, the response generation never ends up getting fired because each parallel invocation thinks there are steps left.

</td></tr><tr><td>

Virtual Agent

 PRB1933102

</td><td>

Follow up search abruptly ends the conversation

</td><td>

When performing a second search immediately after the first search, the conversation ends but the search continues.

</td><td>

1.  Search for a KB/catalog/topic.
2.  Search for another KB/Catalog/topic after getting the response.

 Expected behavior: The user gets a response related to the search from step 2.

 Actual behavior: The conversation ends and then the search continues.

</td></tr><tr><td>

Virtual Agent

 PRB1933142

</td><td>

Language detection isn't being honored

</td><td>

In the sys\_generative\_ai\_log, the Unified Planner capability doesn't honor language detection. Also, in one\_api\_service\_plan\_feature\_invocation, the Unified Planner was not invoked with any of the language flags.

</td><td>

1.  Open an instance with language detection turned on.
2.  Navigate to the SP page.
3.  In chat bot, enter the utterance '¿Qué son las leguminosas?'

Observe that the transition message is in English.

4.  Navigate to sys\_generative\_ai\_log and look at the Unified Planner capability.

 Expected behavior: It says 'Generate the response in language Spanish. Do not return any translation. You are allowed to respond only in Spanish.'

 Actual behavior: It says 'Generate the response in language English. Do not return any translation. You are allowed to respond only in English.'

</td></tr><tr><td>

Virtual Agent

 PRB1933169

</td><td>

Now Assist Virtual Agent \(NAVA\) Search isn't working with NowLLM

</td><td>

 

</td><td>

1.  Set up NAVA.
2.  Change the model to NowLLM.
3.  Search with any utterance.

</td></tr><tr><td>

Virtual Agent

 PRB1933571

</td><td>

The 'No answer found' response should always head to fallback

</td><td>

This should occur for both a single and multi-intent query.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1933589

</td><td>

Agents aren't discovered

</td><td>

 

</td><td>

1.  Start a conversation from Dispatcher Workspace or Now Assist Virtual Agent.
2.  Enter, 'I would like to order a laptop with accessories.'

 Observe that no agents are discovered, and only tools are displayed in the Search Result.

</td></tr><tr><td>

Virtual Agent

 PRB1933604

</td><td>

Increase in QueueWait Times under load

</td><td>

 

</td><td>

1.  Setup Now Assist Virtual Agent \(NAVA\).
2.  Execute a load test for a use case.

</td></tr><tr><td>

Virtual Agent

 PRB1933690

</td><td>

The people card only returns the first user in a multi-user query

</td><td>

 

</td><td>

1.  Navigate to NAVA.
2.  Search 'Tell me about Abel Tuter and Abraham Lincoln'.

 Expected behavior: The user gets a people card for each user in the query.

 Actual behavior: The user only gets a response for the first user.

</td></tr><tr><td>

Virtual Agent

 PRB1933716

</td><td>

Stacked messages appear during websearch

</td><td>

 

</td><td>

1.  Navigate to /esc.
2.  Enable websearch by selecting the **Globe** icon.
3.  Query 'Who is the president of the US?'

 Expected behavior: No stacked messages are shown.

 Actual behavior: Stacked messages are shown.

</td></tr><tr><td>

Virtual Agent

 PRB1933783

</td><td>

'Found 10 documents' message shows in web search mode

</td><td>

The 'Found 10 documents' message is irrelevant in web search mode.

</td><td>

1.  Open /esc.
2.  Enable Web Search mode.
3.  Enter, 'What is the weather today.'

 Notice the 'Found 10 documents message'.

</td></tr><tr><td>

Virtual Agent

 PRB1933907

</td><td>

Only the LTM Identify memories capability is called when dynamic translation is turned on

</td><td>

 

</td><td>

1.  On the home page, navigate to **Preferences** &gt; **Language &amp; Region**.
2.  Select the language 'Francais \(Canada\)'.
3.  Navigate to /esc.
4.  Launch DW.
5.  Enter a French Canadian query. For example, enter 'vérification du solde des vacances' \(holiday balance check\).

 Expected behavior: Agentic capabilities are called, such as Unified Planner, Planner 2 along with TexttoResult, and BGE Reranker.

 Actual behavior: Only the LTM Identify memories capability is getting called. This issue blocks fr-CA model quality evaluations with dynamic translation turned on.

</td></tr><tr><td>

Virtual Agent

 PRB1934004

</td><td>

Agents and use cases aren't getting discovered when giving the utterance as 'Resolve an incident' in Now Assist panel \(NAP\)

</td><td>

Agents should be discovered and show to the user, and should be picked up automatically to begin execution.

</td><td>

1.  Navigate to the instance.
2.  Open NAP.
3.  Give the utterance, 'How to resolve an incident'.

Observe that agents are getting discovered and are shown to the user.

4.  Give utterance as 'resolve an incident INC000XXXX'.

 Observe that the agent is picked automatically and begins execution.

</td></tr><tr><td>

Virtual Agent

 PRB1934159

</td><td>

Update live agent message to 'There aren't any live agents available at the moment. I'm able to handle a wide range of requests, though. How can I help?'

</td><td>

When processing messages for QnA, the handle scenario Planner1 returns the response in the older format.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1934196

</td><td>

Planner2ResponseHandler fills up the expression cache on the Rhino Engine

</td><td>

Under a load of 25 users on a single node \(one hour\) for only search actions performed, it occupies more than 500MB.

</td><td>

1.  Set up NAVA.
2.  Perform search actions from the chat window.

 Observe that the expression cache is filled up due to this. Under a load of 25 users on a single node \(one hour\) for only search actions performed, observe that it occupies more than 500MB.

</td></tr><tr><td>

Virtual Agent

 PRB1934247

</td><td>

Sometimes the processing message is not shown in the header of a stack of messages

</td><td>

When using the sendProcessingMessageDirectly API, the processing message is shown as a single message rather than as a header in the stack of messages \(if the stack is empty\). In the past, after a response was shown in the conversation, the processing message header got updated to a message like 'View AI agent messages'. Now it shows the last message added to the stack or the last message sent to the header.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1934294

</td><td>

The ticket status agent is not being discovered

</td><td>

The ticket status agent doesn't run; instead, the message 'sorry there was a problem on my side' appears.

</td><td>

1.  Navigate to /esc
2.  Query 'Check IT ticket status'.

 Expected behavior: The ticket status agent runs.

 Actual behavior: The message 'sorry there was a problem on my side' appears.

</td></tr><tr><td>

Virtual Agent

 PRB1934342

</td><td>

Markdown content does not render as a rich text output

</td><td>

The server has a logic to determine the output message type. When the message content contains an HTML tag, it's treated as HTML output.

</td><td>

1.  Create a topic.
2.  Add rich text response node.
3.  Use the string in engineering details as the rich text content.
4.  Run the topic.

 Notice that the content is displayed as plain text instead of markdown.

</td></tr><tr><td>

Virtual Agent

 PRB1934578

</td><td>

Agents selected by planner 1 are not always passed to planner 2

</td><td>

When the user runs a certain query, there is no answer from planner 2, even though planner 1 consistently picks two agents.

</td><td>

1.  Navigate to /esc.
2.  Query 'As a ServiceNow sales person, help me prepare for a customer meeting where I can pitch to the CIO on why they should upgrade from ITSM Pro to ITSM Pro Plus.'

 Observe that there is no answer by planner 2, but planner 1 consistently picks two agents.

</td></tr><tr><td>

Virtual Agent

 PRB1934685

</td><td>

AI Agent \(AIA\) 'Unified Planner Quick' and 'Unified Planner Prompt' instructions contain specific names such as ServiceNow

</td><td>

 

</td><td>

1.  Navigate to **sys\_generative\_ai\_log\_list.do**.
2.  Open one of the Unified Planner Quick or Unified Planner Generative AI log records.

 Expected behavior: AIA Unified Planner for all the models don't to have specific company names in its prompt template.

 Actual behavior: AIA Unified Planner for all the models have specific names such as ServiceNow.

</td></tr><tr><td>

Virtual Agent

 PRB1934741

</td><td>

NASS doesn't respond correctly when entering initial utterances from the **Input search** field

</td><td>

When initially entering an utterance from the **Input search** field, the user receives the message, 'Hello! How can I assist you with ServiceNow today?' instead of a response to answer the question in the utterance.

</td><td>

1.  Set up NASS on an instance.
2.  Navigate to a portal with NASS.

Notice that this shouldn't be in full-page experience.

3.  Enter in the **Input search** field, 'What is the definition of spam?'.

Notice that this should redirect to the full-page experience.


 Expected behavior: The user receives a response to answer 'What is the definition of spam?'.

 Actual behavior: The message is displayed, 'Hello! How can I assist you with ServiceNow today?'.

</td></tr><tr><td>

Virtual Agent

 PRB1934761

</td><td>

The conversation doesn't end after the completion of topic discovery and execution on standard chat

</td><td>

The conversation doesn't end after execution and the input text area remains open. This occurs when the topic is executed via discovery, but it works correctly via topic picker.

</td><td>

1.  Navigate to a NAVA portal with standard chat enabled.
2.  Execute a topic such as 'order coffee' by discovery instead of the topic picker.
3.  Finish the execution.

 Expected behavior: The conversation ends after execution.

 Actual behavior: The conversation doesn't end. The input text area remains open. However, the conversation ends correctly when the topic is executed via topic picker.

</td></tr><tr><td>

Virtual Agent

 PRB1934818

</td><td>

Multi-intent query gets an 'Answer from history' response that doesn't reflect

</td><td>

The Virtual Agent \(VA\) ends the execution after answering the first part of the multi-intent query.

</td><td>

1.  Enter 'What is spam?'
2.  On getting the response, enter 'First, tell me what is spam? Then, help me order a coffee'.

 Expected behavior: The VA answers the first part from memory, then proceeds to execute the order coffee skill.

 Actual behavior: The VA ends the execution after answering the first part.

</td></tr><tr><td>

Virtual Agent

 PRB1934820

</td><td>

Multi-intent query gets stuck in NAVA

</td><td>

After answering the first part of a multi-intent query, NAVA displays the 'Thank you for chatting' message. It tries to execute the second part, but gets stuck generating an answer.

</td><td>

1.  Navigate to /esc.
2.  Navigate to NAVA.
3.  Enter 'what is spam and order a loaner laptop'.

 Observe that NAVA gives a response for spam, then displays the 'Thank you for chatting' message. It tries to execute the second part, but gets stuck generating an answer.

</td></tr><tr><td>

Virtual Agent

 PRB1935109

</td><td>

The catalog name isn't displayed on 'Continue request'

</td><td>

This issue only occurs in a previous Now Assist Virtual Agent \(NAVA\) version.

</td><td>

1.  Start a conversation from with a previous NAVA version.
2.  Execute any topic.
3.  Enter 'I need a standard laptop' mid-topic.

 Notice that the 'Continue request' control shows the previous topic instead of the catalog name.

</td></tr><tr><td>

Virtual Agent

 PRB1935143

</td><td>

Malformed JSON fixer isn't handled in the API

</td><td>

The new API 'Dynamic Capability Executor' isn't handling the malformed JSON fixer.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1935215

</td><td>

Java implementation of fully agentic Virtual Agent

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1935791

</td><td>

A dynamically changing script unnecessarily eats up space in the sys\_expression cache

</td><td>

 

</td><td>

1.  Set up NAVA.
2.  Run a load test for 1 hour \(agent use case\).
3.  Check the heap memory during the run where more than 500MB is the expression cache.

</td></tr><tr><td>

Virtual Agent

 PRB1935944

</td><td>

Post chat survey results are not stored in assessment instance table

</td><td>

There should be a record of the feedback asmt\_assessment\_instance given in the post chat survey. However, there is no feedback given by the user in the post chat survey is stored.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1936166

</td><td>

Add scriptable API in VASystemObject to fetch user preferences

</td><td>

vaSystem.get UserPreferences\(\) should return LTM memories of the user which have categories that are linked to the context\_profile of the conversation.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1936171

</td><td>

Add scriptable API in VASystemObject to fetch user preferences

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1936344

</td><td>

Web search isn't working in full agentic mode

</td><td>

 

</td><td>

1.  Navigate to **/esc** or **/sp**.
2.  Attempt any query on web search.

 Notice the error message thrown, 'Sorry, there was a problem on my side trying to complete this request. Try asking again later.'

</td></tr><tr><td>

Virtual Agent

 PRB1936780

</td><td>

Add the ability to send top n skills in Planner1 for quick skill discovery

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1936820

</td><td>

Lock exceptions are noticed for Now Assist Portal \(NAP\) and NAVA

</td><td>

 

</td><td>

1.  Set up the latest ynowassiststable instance for NAP/NAVA.
2.  Execute load tests for any use case of Virtual Agent.

 Notice the exceptions are logged in the log.

</td></tr><tr><td>

Virtual Agent

 PRB1936882

</td><td>

A follow-up question is executed twice after coming from portal

</td><td>

 

</td><td>

1.  Open an instance with October Store app versions and Dynamic Window enabled.
2.  Search for 'what is cookie' in Portal.
3.  Wait for the response to load.
4.  Select **Ask a follow-up**.
5.  Wait for the chat to load.
6.  Search for 'how to block them?'.
7.  Wait for the response to load.

 Notice the response is displayed twice for the follow-up question. The GenAI log has double entries for that call as well.

</td></tr><tr><td>

Virtual Agent

 PRB1936985

</td><td>

A conversation is stuck in 'thinking' after web search searches and reaching web search fallback

</td><td>

 

</td><td>

1.  Navigate to Service Portal.
2.  Start a web search by selecting the **Globe** icon.
3.  Query 'who is the president of the US'.
4.  End the web search.
5.  Query: 'what is a cookie'.
6.  Query: 'what is the capital of Texas and what is the weather like there?'.
7.  Enter web search fallback.
8.  After the fallback message is received, it says 'All done! Is there anything else I can help you with?'. Reply with 'No thank you'.

 Expected behavior: The conversation should end.

 Actual behavior: Virtual Agent is stuck at 'Thinking'.

</td></tr><tr><td>

Virtual Agent

 PRB1936987

</td><td>

One issue is found with a synthesized response in NAVA when dynamic translation is on

</td><td>

 

</td><td>

1.  Log in with a Spanish user.
2.  Navigate to the esc portal.
3.  Search for 'Pedir Cafe' in portal.
4.  Start the 'Order coffee' topic in Spanish.
5.  Once the results come again, search for 'Necesito ayuda para crear incidente' in the portal.
6.  Verify that the MID topic message is in Spanish.

 Notice that it is in English, which is incorrect.

</td></tr><tr><td>

Virtual Agent

 PRB1937454

</td><td>

Catalog and skill execution in CEA gets stuck

</td><td>

 

</td><td>

1.  Navigate to CEA.
2.  Search for the topic/catalog 'What is spam' 'I want Miro access'.
3.  Start topic/skill.

 Expected behavior: Skills/topics start and execution is completed.

 Actual behavior: Skills and topics are stuck at 'thinking'.

</td></tr><tr><td>

Virtual Agent

 PRB1937589

</td><td>

Abnormal GAIC Async submission duration

</td><td>

SkillDetailsCache is reclaimed and cache building can be as high as 3.5s.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1937597

</td><td>

AIA ResponseGeneration scripts aren't cached

</td><td>

When invoking the following scripts, they're currently invoked as 'dynamic' and hence not cached: 'AIAResponseGenerator', 'AISWebSearchCallbackWrapper', and 'AISPlanner2ResponseHandler'. They should be invoked as simple scripts and pass the necessary variables to evaluate them so that they're cached properly.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1937694

</td><td>

Web search fallback isn't working

</td><td>

 

</td><td>

1.  Set up a ynowassistable instance with the slack:6.0.1 SNAPSHOT installed.
2.  Connect the slack to the assistant.
3.  Open the slack and type 'What is spam?'.
4.  When the results are shown, type 'I am not happy'.
5.  When the fallback is shown, select **Web search**.

 Notice that the same fallback options are repeated.

</td></tr><tr><td>

Virtual Agent

 PRB1938022

</td><td>

AI Agent \(AIA\) Unified Planner 1 is taking up to 1.5 to 2 seconds in the Gen AI log with a single user.

</td><td>

The Hybrid queue takes up to 500 ms.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1938273

</td><td>

Multi-intent utterances are not working in Now Assist panel \(NAP\)

</td><td>

This issue was observed when using Azure and Gemini. Workflows are available for example both utterances, and individually both utterances are work as expected.

</td><td>

Enter the utterance 'Book a flight and order coffee'.

 Notice that the first workflow completed for both Azure and Gemini, but general react responses occur instead of triggering the next flow in Azure, and a message occurs that the workflow can't proceed in Gemini.

</td></tr><tr><td>

Virtual Agent

 PRB1938620

</td><td>

The **Go to search results** button isn't visible in Dynamic Window \(DW\)

</td><td>

The **Go to search results** button isn't visible for chat-to-search transition. It should be visible, as this functionality worked in the previous release.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1938658

</td><td>

Second intent is not going to planner 1 in continuous conversations

</td><td>

 

</td><td>

1.  Navigate to the**ESC** portal.
2.  Open Virtual Agent \(VA\).
3.  Enter utterance which can match multiple agents.
4.  Instead of selecting an agent, enter the next utterance that can give fallback options such as 'What is ServiceNow stock price'.
5.  Select **Web search** in the fallback option.

 Observe that web search gives an answer for incident resolution, and not for ServiceNow stock price.

</td></tr><tr><td>

Virtual Agent

 PRB1940872

</td><td>

Too many conversation server exceptions for any conversation created

</td><td>

 

</td><td>

1.  Set up latest instance for Now Assist panel \(NAP\)/Now Assist Virtual Agent \(NAVA\).
2.  Execute load tests for any use case of VA.

 Notice the exceptions logged in the log.

</td></tr><tr><td>

Virtual Agent

 PRB1941025

</td><td>

Conversation doesn't end after catalog execution completes on standard chat

</td><td>

 

</td><td>

1.  Execute the Miro access catalog item in standard chat.
2.  Finish the flow.

 Expected behavior:The conversation ends after the execution completes.

 Actual behavior: The conversation doesn't ended.

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1941102

</td><td>

Typing a response before a previous response has completed can lead to a 'technical error' in the conversation

</td><td>

 

</td><td>

1.  In a teams bot with LLM enabled send any message.
2.  Type another message immediately after.

 Notice an error.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1896390

</td><td>

Console errors for va\_web\_client API failures are displayed when launching a chat in the CSM portal and Engagement Messenger

</td><td>

Two console errors related to va\_web\_client are observed: '/api/now/ va\_web\_client\_settings /get\_va\_web\_ client\_settings' api results 403 error' and '\[SNAnalytics\] Invalid property name'. Console errors shouldn't be displayed and chat functionality should work as expected.

</td><td>

1.  Log in to an instance.
2.  Navigate to CSM portal or Engagement Messenger.
3.  Launch Virtual Agent chat/start a chat.

 Observe the browser console.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1916061

</td><td>

Now Assist Virtual Agent \(NAVA\) response returns incorrectly when the user enters the same utterance twice

</td><td>

When searching for the utterance twice, the first response returns correctly, but the second response is incorrect and null.

</td><td>

1.  Log in to a Zurich instance.
2.  Navigate to the ESC portal.
3.  Search for 'I need help in creating an incident.'

Notice that the response is as expected.

4.  Search the same utterance again, 'i need help in creating an incident.'

 Expected behavior: The correct synthesized response appears.

 Actual behavior: The response showing is incorrect, and 'null' displays.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1920035

</td><td>

The 'VTT' icon isn't available in previous model of Now Assist Portal \(NAP\)

</td><td>

The issue occurs when the user switches from the new model to the previous model with VTT turned on.

</td><td>

1.  Install any of the BU skills.
2.  Turn on NAP with VTT.
3.  Turn on the microphone from the browser preferences.
4.  Toggle 'on' accessibility settings.
5.  Select the **NAP icon**.
6.  Ensure the VTT icon is available in the new model.
7.  Change the model to old model \(Self service modal dialog\).
8.  Refresh the page.

 Expected behavior: The VTT icon should be available.

 Actual behavior: The VTT icon is not available in the old model of NAP when the user switches from the new model to old model with VTT enabled.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1923459

</td><td>

Context variables aren't accessible in the enhanced chat

</td><td>

Context variables aren't accessible in the enhanced chat, whereas they are accessible in the standard chat using either 'vaContext.liveagent\_' or 'vaVars.liveagent\_'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1924991

</td><td>

**Like**/ **Dislike** buttons do not have discernible text

</td><td>

 

</td><td>

1.  Open 'Now Assist' from navigation bar or navigate to ESC and open 'Now Assist' from the bottom-right corner.
2.  Start the conversation.
3.  Turn on-screen reader.
4.  Navigate on the chat and pay attention to what the screen reader reads at the **Like**/ **Dislike** buttons.

 Notice that the **Like**/ **Dislike** buttons don't have discernible text.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1928501

</td><td>

Context variables are not accessible in the enhanced chat

</td><td>

The context variables are not accessible in enhanced chat, but they are accessible in standard chat using either 'vaContext.liveagent\_' or 'vaVars.liveagent\_'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1933058

</td><td>

Skills are disabled in Now Assist panel \(NAP\)

</td><td>

 

</td><td>

1.  Select on **NAP**.
2.  Enter 'Summarize a record.'

 Expected behavior: The discovered skill can be selected.

 Actual behavior: The skill is disabled.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1933088

</td><td>

Processing loader is displayed even after getting a response

</td><td>

 

</td><td>

1.  Select **NAP**.
2.  Enter 'Summarize a record/conversation'.
3.  Select the discovered skill.

 Observe that the loader is still displayed, even after getting the record number question.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1933706

</td><td>

The conversation history doesn't save for document QnA

</td><td>

 

</td><td>

1.  Select **NAP/DW NAVA**.
2.  Upload a document.
3.  Ask a question about the document.
4.  Enter 'Thanks for the info'.
5.  Select **Cancel** for the document QnA.
6.  Select the three lines to see the conversation history.

 Observe that the document QnA conversation is not displayed.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1933741

</td><td>

Stacked messages appear during websearch

</td><td>

 

</td><td>

1.  Navigate to **/esc**.
2.  Enable websearch by selecting the **Globe icon**.
3.  Query, 'Who is the president of the US'.

 Expected behavior: No stacked messages should appear when web searching.

 Actual behavior: Stacked messages appear.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1935212

</td><td>

Fix the remaining VX for processing message changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1935820

</td><td>

The user isn't directed to a live agent when selecting **Contact live agent** for the second time in the same chat

</td><td>

The work item isn't created when the user selects **Contact live agent**, cancels it, and then selects it again in the same chat.

</td><td>

1.  Navigate to **/sp** portal.
2.  Impersonate a user on a different browser.
3.  In Dispatcher Workspace \(DW\), select **Contact live agent** for a new chat.
4.  Select **Cancel**.
5.  Select **Contact live agent** again.

 Expected behavior: The user request is directed to an agent and the work item is visible on the agent workspace.

 Actual behavior: A work item isn't created for that agent and nothing happens in DW.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1936255

</td><td>

Turn off audio notifications by default in Now Assist Portal and Virtual Agent

</td><td>

As processing execution occurs, there's continuous beeps. The audio should be turned off by default.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1936912

</td><td>

The user isn't directed to a live agent upon selecting **Contact live agent** after the user ends the chat with the agent

</td><td>

This issue occurs in Dispatcher Workspace \(DW\).

</td><td>

1.  Navigate to **DW**.
2.  Select **Contact live agent for first time**.
3.  Accept the work item as agent.
4.  Select **End live chat** as user.
5.  Select **Contact live agent** again in the same conversation.

 Notice that there's no work item created for the agent and nothing happens in DW.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1937016

</td><td>

Fixing VX spacing issues

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1937432

</td><td>

Fixing VX spacing issues

</td><td>

Issues with spacing observed Assist Virtual Agent \(NAVA\) and Dispatcher Workspace \(DW\). In issue 1, there's an extra space under 'Generating a response' for NAVA while it seems to be fixed for DW. In issue 2, spacing between the processing message container and the sparkle icon should be 24px but it's 12px in NAVA and 24px in DW. In issue 3, processing step spacing should be 8px at the top and bottom in both NAVA and DW.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1940018

</td><td>

Spacing not matching Figma for Conversational UX enhancements

</td><td>

Spacing issues in Now Assist Virtual Agent \(NAVA\), Dispatcher Workspace \(DW\), and Now Assist panel \(NAP\).

</td><td>

1.  Enter **Hello**.

Notice that the space between 'Hello' and the sparkle icon should be 12px, and is currently 24px in both NAVA, DW and NAP. Also notice the space between 'Let me look up for information'.

2.  Hover the copy icon to next Sparkle icon.Notice that it should be 12px, has a 4px margin in DW and NAP.
3.  Select **Show Sources**.

 Notice that the space between the Synthesized results and the links should be 8px, and that it's 4px in DW and NAP.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1941773

</td><td>

Portal page shifts occasionally when **Ask for a follow-up** is selected

</td><td>

The portal page shifts to the left then returns back to its original place when the user dismisses the pop-up.

</td><td>

1.  Ensure Dispatcher Workspace \(DW\) is enabled for Service Portal \(SP\) from the 'Assistants page'
2.  Navigate to **SP portal**.
3.  Enter **What is spam** in portal search.
4.  Select **Ask for a follow up** once the Results page displays.

 Notice that DW opens with the pop-up 'Your previous chat was saved' and the portal page shifts to the left, but when the user when the user dismisses the **Your previous chat was saved** button, the page returns to its original place.

</td></tr><tr><td>

Workflow Studio

 PRB1922988

</td><td>

A banner message to install the latest PAD should be displayed on Workflow Studio

</td><td>

To inform users to install the latest PAD when the new Now Assist for Platform version is available, there should be a banner message in Workflow Studio advising them to upgrade PAD for the Agentic Playbook feature.

</td><td>

1.  Navigate to a Zurich instance.
2.  Install Workflow Studio.
3.  Launch Workflow Studio.

 Expected behavior: There's an info banner message to install the latest PAD to get an Agentic Playbook feature..

 Actual behavior: No banner is available.

</td></tr><tr><td>

Work Order Management

 PRB1929109

</td><td>

Upon page reload, the value in the decimal input field disappears

</td><td>

 

</td><td>

1.  Open Work Order Template.
2.  Input any value in the **Enter decimal value** field.
3.  **Save** it.
4.  Reload the page.

 Notice that the value in the decimal input field has disappeared.

</td></tr><tr><td>

Work Order Management

 PRB1930398

</td><td>

The user is unable to perform 'Remove parts' on agent app as an external agent

</td><td>

The user is unable to view used parts under **My Tasks** &gt; **WIP Task** &gt; **Parts** &gt; **Remove Part** on the mobile app due to a missing ACL on alm\_asset.parent.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1935240

</td><td>

Duplicate events appear when the schedule of a personal event changes

</td><td>

When using the flat table for personal events, duplicate events appear when the schedule of a personal event changes. The old user still has the personal event displayed on DW.

</td><td>

1.  Make sure the flat table is turned on.
2.  Open the cmn\_schedule\_p table.
3.  Add the **Schedule** field on the form \(if needed\).
4.  Open DW.
5.  Create a personal event for the user Alex Ray.
6.  Double-click \(or use the keyboard shortcut\) on the event.

Observe that the cmn\_schedule\_p record opens in a new tab.

7.  Change the schedule to Anthony Roy's personal schedule.
8.  Navigate to DW.
9.  Select the **Refresh** button.

 Expected behavior: The personal event is only shown for the user based on the update.

 Actual behavior: Two personal events are shown. After the schedule changes to a different user, the old user still has the personal event displayed on DW.

</td></tr><tr><td>

Workplace Case Management

 PRB1927638

</td><td>

Moving bars aren't working in Scenario Planning

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Workplace Central

 PRB1919180

</td><td>

When selecting **Create schedule**, it takes more time open the 'Schedule' page and sometimes it doesn't open

</td><td>

When the user selects **Create Schedule** it should open directly, and they should be able to view the schedule before publishing the plan. This issue occurs on new instances from Xanadu to Zurich, and has been observed in existing instances as well.

</td><td>

 

</td></tr><tr><td>

Workplace Maintenance Management

 PRB1919220

</td><td>

Unable to copy the schedule because the list appears empty when it's selected for Maintenance Plans

</td><td>

When a schedule is previously created for a Maintenance Plan, it can't be copied over to a new plan because the list appears empty and the previously created plan doesn't appear.

</td><td>

1.  Create a Maintenance Plan.
2.  Navigate to **Workspaces** &gt; **Workplace Central** &gt; **Preventive Maintenance icon**.
3.  Navigate to **All Plans** &gt; **New**.
4.  Give any plan name.
5.  Choose a start date in the future.
6.  Choose an end date in the future.
7.  Select the location.
8.  Select any building.
9.  Select **Next**.
10. Select one maintenance item.
11. Select **Next**.
12. Select **Create schedule**.
13. Create schedules with the following:
    1.  Schedule: 1
    2.  Name: Schedule 1
    3.  Trigger: Duration
    4.  Trigger type: Interval
    5.  Repeat: Days - 1
14. Select **Save**.
15. Select **Publish**.
16. Create Plan 2 with the previous steps up to the maintenance items selection.
17. Do not select **Create Schedule**.
18. Attempt to copy the schedule.

 Notice that the previously created schedule does not appear.

</td></tr><tr><td>

Zing Text Indexing and Search Engine

 PRB1919510

</td><td>

Slow queries that time out go unhandled and leave the global search in an infinite loading state

</td><td>

Even though the search times out from the back end, the UI doesn't process it correctly, and it shows an infinite loading state.

</td><td>

1.  Provision an instance with Polaris enabled and Zing used for Global Search.
2.  Make sure one of the tables used as a global search source has a large amount of data in it.
3.  Set the maximum time for global search queries to the lowest number possible, one second.
    1.  De-activate the 'Text Search Property Change Rationally' business rule.
    2.  Set the 'glide.ts.max\_duration' system property to one.
4.  Do a query that takes some time \(at least one second\).

 Expected behavior: The search times out. Global search shows either a 'No results' message or the results that were returned from the batches that finished in time.

 Actual behavior: Even though the search times out from the back end, the UI doesn't process it correctly, and it shows an infinite loading state.

</td></tr><tr><td>

Zing Text Indexing and Search Engine

 PRB1943229

</td><td>

Exact match always returns the same KB on service portal

</td><td>

Exact match should only show KBs that pass certain conditions, but queries always lead to one specific KB number.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Zurich Patch 1 Hotfix 1](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2524158)
-   [Zurich Patch 1](zurich-patch-1.md)
-   [Zurich security and notable fixes](zurich-security-notables.md)
-   [All other Zurich fixes](zurich-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


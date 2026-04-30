---
title: Yokohama Patch 8
description: The Yokohama Patch 8 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-09-19"
reading_time_minutes: 105
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 8

The Yokohama Patch 8 release contains important problem fixes.

-   **Yokohama Patch 8 was released on October 14, 2025.**
    -   Build date: 10-11-2025\_0527
    -   Build tag: glide-yokohama-12-18-2024\_\_patch8-09-17-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y08.00.xlsx).

## Overview

Yokohama Patch 8 includes 332 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp8.png "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 8 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 8, refer to [KB2521419](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2521419).

## Changes in Yokohama Patch 8

-   **[MID Server parameters](https://www.servicenow.com/docs/access?context=mid-server-parameters&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**
    -   **mid.ssh.disable\_history**

        Controls whether the shell session history is saved on the target host and if the `HISTFILE=/dev/null` command is executed. Set this property to **false** to retain history on the target host, ensuring the `HISTFILE=/dev/null` command is not sent to the target device.

        -   Type: true \| false
        -   Default value: true
        **Important:** This parameter requires Yokohama 8 or later.


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

 PRB1942680

</td><td>

Web search isn't working in Zurich and recent store apps

</td><td>

 

</td><td>

1.  Navigate to **/esc.**
2.  Start the web search by selecting the **Globe**icon.
3.  Query, 'Who is the president of the US'.

 Expected behavior: The web search query goes through.

 Actual behavior: The user receives a 'Sorry there was a problem' message.

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

Application Install Engine

 PRB1911704

</td><td>

An error appears while selecting optional spokes and installing SaaS int app

</td><td>

During the preprocessing operation, the user receives an error while selecting optional spokes and installing SaaS int app. After a second attempt, the locate remote offering plugin record for com.sn\_sam\_saas\_int can't be located.

</td><td>

1.  Provision an instance with com.sam.saas.int installed on a multi node environment and optional plugins installed on another node.
2.  Try to repair the app.

 Observe that an error appears.

</td></tr><tr><td>

CMDB Query Builder

 PRB1889722

 [KB2127777](https://hi.service-now.com/kb_view.do?sysparm_article=KB2127777)

</td><td>

The 'CMDB Query Builder Suggested Relations' job can fail to process all CMDB\_REL\_CI records

</td><td>

The 'CMDB Query Builder Suggested Relationships' job changed in Yokohama to use a new batched approach to improve memory consumption and processing speed. However, there are two scenarios \(Invalid relationship data and Environment date format\) under which it doesn't proceed to the next batch, resulting in an incomplete data set in cmdb\_class\_relationships.

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

Flow Engine

 PRB1846526

 [KB2472659](https://hi.service-now.com/kb_view.do?sysparm_article=KB2472659)

</td><td>

A scripted sub-flow behaves differently with a stage set in a parent flow for Flow Engine v2

</td><td>

If the user has a sub-flow that carries out a scripted action, there's a difference in execution when using Engine v2, which can interfere with previously published flows.

</td><td>

Refer to the listed KB article for details.

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

List Controller

 PRB1872228

</td><td>

Upgrading an instance from Washington to Yokohama is breaking the **New** button

</td><td>

Upgrading an instance from Washington to Yokohama is breaking the **New** button in Service Operations Workspace when the 'Knowledge' template isn't activated.

</td><td>

1.  Log in to a newly upgraded instance.
2.  Navigate to **SOW** &gt; **List tab** &gt; **Knowledge** &gt; **Navigate to any of the 3: Your unpublished articles \| Knowledge - Your published articles \| All articles** &gt; **New button**.

 Expected behavior: The form loads.

 Actual behavior: The 'knowledge record not found' error message appears.

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

Activity Stream

 PRB1928323

</td><td>

Add sparkle to the AI username

</td><td>

AI user names should be preceded by the AI sparkle icon \(ai-sparkle-outline\).

</td><td>

1.  Navigate any relevant workspace \(CSM, SOW, etc.\).
2.  Open any incident record with an AI-generated entry.

 Expected behavior: AI user names should be preceded by the AI sparkle icon \(ai-sparkle-outline\).

 Actual behavior: The AI username doesn't have a sparkle in front of it.

</td></tr><tr><td>

Agent Chat

 PRB1839064

</td><td>

Refreshing the page causes the active chat shell to disappear, but refocusing on the live agent in a separate window restores the chat shell

</td><td>

This issue is observed in version 24.4.2 of Workspace App Shell TD.

</td><td>

1.  Ensure the Agent Chat plugin is installed.
2.  Open Service Operation Workspace as an admin in a window.
3.  Set the admin as available as a chat agent.
4.  Attempt to log in to Service Operations Workspace as Abel Tuter in an incognito window.
5.  Attempt to connect to a live agent.
6.  Accept the chat as an admin.
7.  End the chat.
8.  Keep the tab open.
9.  Initiate the chat again as Abel Tuter.
10. Accept the chat as an admin.
11. Refresh the admin page

 Observe that the active chat shell window isn't opening unless the live agent is not in focused by Abel Tuter.

</td></tr><tr><td>

Agent Chat

 PRB1922878

</td><td>

The agent chat's audio alert for inbox should stop playing when the agent has responded even if the alert's mp3 has not finished playing

</td><td>

 

</td><td>

1.  Add a 20 or more seconds mp3 ring tone to the **System UI** &gt; **Audio Files**.
2.  Update the 'connect.notification.audio\_alert' to the new mp3 name.
3.  Sign in as an agent.
4.  Ensure that the 'Inbox Audio Alerts' is turned on.
5.  Have a customer request for a chat with a live agent.
6.  On the Agent Workspace, the newly added alert is played.
7.  Accept the chat as the agent.

 Expected behavior: The alert should stop playing as the agent accepts the incoming chat.

 Actual behavior: The alert continues to play until the end of the ring tone file, regardless of if the agent has already picked up the call.

</td></tr><tr><td>

Agent Chat

 PRB1925414

</td><td>

There's issues with the 'Start Voice' API call in a domain-separated environment

</td><td>

There are issues with the 'Start Voice' API call in a domain-separated environment, both inbound and outbound calls and impersonation due to a guest user.

</td><td>

1.  Initiate an inbound or outbound call that triggers the 'Start Voice Interaction' API in a domain-separated environment.
    -   Observe that the API is logged under the user 'guest' \(see Splunk logs\) and an interaction record is created in the default domain instead of the user's domain.
2.  Attempt to retrieve interaction using getInteractionRecord.

 Observe that it fails due to a domain mismatch.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1927798

 [KB2426374](https://hi.service-now.com/kb_view.do?sysparm_article=KB2426374)

</td><td>

Missing compound index on sys\_translated causes slowness in AI Search indexing

</td><td>

getTranslation in CatalogVariablesUtil can be as slow as 500ms, causing a performance issue when indexing sc\_cat\_item.

</td><td>

Refer to the listed KB article for details.

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

 PRB1888752

</td><td>

The KB sources number is cut off for Now Assist QnA Genius Results

</td><td>

This is observed on global and portal both.

</td><td>

1.  Open an instance with the latest znowassist version.
2.  Attach a Now Assist QnA to the search profile.
3.  Search for 'what is cookie?'.

 Notice that the KB number is cut off in sources and when a user hovers over the sources, it doesn't display the pop-up with the KB number and name.

</td></tr><tr><td>

AI Search

 PRB1892031

</td><td>

ais\_country\_to\_search\_language doesn't work

</td><td>

When the user sets the language to Japanese and searches a Japanese word, many KBs are found. However, if the user sets the language to English and searches the same word, only one KB is found.

</td><td>

1.  Set the language to Japanese \(日本語\).
2.  Open the employee center \(/esc\).
3.  Search the word IT資産'.
4.  Observe that many KBs are found.
5.  Set the language to English.
6.  Open the employee center \(/esc\).
7.  Search the word 'IT資産'.

 Observe that only one KB is found.

</td></tr><tr><td>

AI Search

 PRB1931645

</td><td>

AIS listens to events such as 'sys\_cache\_flush' and can cause stack overflow exception

</td><td>

AIS listens to events such as 'sys\_cache\_flush' and can cause a stack overflow exception by running a DBQuery, which can insert a record to sys\_cache\_flush.

</td><td>

1.  Enable glide.sys.domain. delegated\_administration and glide.sys.domain .partitioning.
2.  Create two separated domains.
3.  Clear the cache.
4.  Update any record.

 Observe the stack overflow exception in the logs.

</td></tr><tr><td>

AI Search UX

 PRB1917739

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

 Actual behavior. A message says, 'Found no records'.

</td></tr><tr><td>

AI Search UX

 PRB1942589

</td><td>

Increased timeout from 15s to resolve frequent no Genius Results on Portal

</td><td>

This issue occurs on Dispatcher Workspace enabled on Portal with Model GPT OSS, and takes longer for a response to return than in any other models.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1840570

</td><td>

In Platform Analytics, a filter is only applied on one field when there are multiple entries for the same table

</td><td>

In Platform Analytics, multiple entries for the same table but different fields doesn't work as a classic interactive filter functionality. For example, when this scenario occurs in the interactive filter, the reports apply the same element for all the fields from that table with an 'AND' operation. In Platform Analytics, however, it applies the filter on only one field.

</td><td>

 

</td></tr><tr><td>

Analytics Export API

 PRB1853207

</td><td>

Export traffic should be migrated to K8s by default for commercial environments

</td><td>

When a user without elevated privileges logs in to ServiceNow and exports a dashboard or visualization, the traffic goes to VMs because 'glide.par.export.use.sk8s' is false. Instead, K8s traffic should be enabled by default for commercial environments.

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

 PRB1934177

</td><td>

Node is not expanding the artifact

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1936285

</td><td>

During node re-start, the system downloads version expects a higher store version

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

1.  Log in to any instance
2.  In the navigator filter, search for **System Applications** &gt; **Install Application**.
3.  Select an option from Nexus to populate the repository URL.

 Observe that this URL isn't functional anymore due to the changes to the Nexus server.

</td></tr><tr><td>

Approvals

 PRB1928314

</td><td>

Re-triggered change approvals aren't routing to the user who rejected them previously

</td><td>

After a Change approval is rejected, re-triggering the approval doesn't route back to the original rejecting approver. Instead, the approval remains in a 'Rejected' state. This issue was observed after upgrading to Yokohama, and occurs with an e-signature enabled for Change requests.

</td><td>

1.  Deactivate normal Change request flows in Flow Designer.
2.  Create a new normal Change request.
3.  Give it any assignment group and request approval.
4.  Navigate to the **Change request list** view.
5.  Add the **Approval** field.
6.  Manually change the **Approval** field state to 'Requested'.
7.  Notice that this will trigger the workflow to move past the 'Wait' condition.
8.  Reject one of the approvals.
9.  Notice that the other approvals move to 'No longer required'.
10. Return to the Change request in list view.
11. Change the **Approval** field state to 'Requested'.

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

Attachments to Records

 PRB1848449

</td><td>

The user is unable to upload an image to a field when 'glide.attachment.extensions' is not empty

</td><td>

The user is unable to upload an image to the field **sys\_user.photo** when 'glide.attachment .extensions' is not empty and 'glide.ui.attachment .extensions.enforce' is true.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1903721

</td><td>

Automated Test Framework \(ATF\) tests can't run in parallel due to indirect updates to ml\_solution

</td><td>

Since ml\_solution is modified every time a user makes an ML call, it causes any test that makes an ML call to be unable to run in parallel with other similar tests. It shouldn't be tracked as a modified record, since ml\_solution appears to be an administrative table.

</td><td>

1.  Create an ATF test.
2.  Add a Record Update step.
3.  Choose any record on ml\_solution.
    1.  Uncheck **Enforce security**.
    2.  Set the update to 'Active = false'.
4.  Run the test.

 Expected behavior: No records modified are generated for ml\_solution.

 Actual behavior: A record modified is generated for ml\_solution.

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

 PRB1848541

</td><td>

Choice List cache invalidation doesn't work properly

</td><td>

Choice List cache invalidation isn't working correctly. The script that shows when using the table change\_request and the field risk, it clears the cached value so that it will be rebuilt by the next valid request.

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
5.  Navigate to **All** &gt; **Skill kit.**
6.  Select **Case summarization for approvals** &gt; **skill** &gt; **Prompt performance** &gt; **Create dataset**.

 Notice that while creating the data set, the error 'Failed to create dataset' occurs due to the ACL attached.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1926747

</td><td>

The vendor portal take-questionnaire page stops working when an HR application is installed

</td><td>

The user is not able to see the questionnaires associated with the assessment.

</td><td>

1.  Log in to the Instance as admin.
2.  Navigate to **All** &gt; **sn\_vdr\_risk\_asmt\_assessment.LIST** &gt; **Create new TPRA record** &gt; **Save**.
3.  Select **Questionnaires**.
4.  Edit the record and save.
5.  Select **Submit to third party**.
6.  Open the instance in the same browser as admin and impersonate as a third-party contact.
7.  Select **Risk assessment** for the third-party record created in step 2.

 Expected behavior: The user should be able to see and answer the questionnaires associated with the assessment.

 Actual behavior: The user is not able to see the questionnaires associated with the assessment.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1928914

</td><td>

There's a RCA issue for email reply recommendation

</td><td>

The sparkle icon is missing because this RCA isn't in an allowed state.

</td><td>

 

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

Change Management

 PRB1867284

</td><td>

A JavaScript error 'TypeError: model.mandatoryFields is not a function' occurs in the console on approving a change request, which causes Automated Test Framework \(ATF\) tests to fail

</td><td>

The 'TypeError: model.mandatoryFields is not a function' error message occurs when the change request is moved to the next state after approving the system administrator approval request.

</td><td>

1.  Log in as a system administrator user.
2.  Create a normal or Emergency change request.
3.  Use the Assignment group 'CAB Workbench'.
4.  **Save** it.
5.  Select **Request Approval**.
6.  Open developer console.
7.  Open the 'Approvers' related list.
8.  Approve the system administrator approval request from the right-click context menu.

 Expected behavior: The change request state is moved to the next state without errors occurring.

 Actual behavior: The change request state moved to the next state with the error, 'Uncaught TypeError: model.mandatoryFields is not a function', and causing ATF tests to fail.

</td></tr><tr><td>

Change Management

 PRB1931749

</td><td>

The **Impact** field isn't updated after running risk calculation

</td><td>

When a change\_request has the **Impact** choice field with 'None' enabled, the riskCondition should update the **change\_request.impact** field, but it doesn't. RiskCalculatorSNC is checking the wrong impact field. Instead of the one in the risk\_condition table, it's checking the one in the change\_request table.

</td><td>

 

</td></tr><tr><td>

Client Scripts

 PRB1889628

</td><td>

List declarative actions aren't working

</td><td>

 

</td><td>

1.  Create a list declarative action.
2.  Implement as a client script.
3.  Set the client script to 'console.log\('Test'\);'.
4.  Set the table as 'incident'.
5.  Navigate to the incident list.
6.  Select the declarative action.

 Notice that no console logs are outputted.

</td></tr><tr><td>

Code Signing

 PRB1918750

</td><td>

Code signing code leaks GlideRecord

</td><td>

Code signing code is saving gliderecord in static, causing a leak.

</td><td>

1.  Create a CodeSigningField ValueGetter object by passing a gliderecord and field as parameters.
2.  Take a heapdump.

 Expected behavior: The gliderecord passed in the steps should have been group changed.

 Actual behavior: The glideRecord object remains in the memory until a restart of node, or until another CodeSigningField ValueGetter object is created.

</td></tr><tr><td>

Code Signing

 PRB1921400

</td><td>

Update the signature timestamp on JIT-loading when the signature isn't present in the table, and compare the signature timestamp with the plugin upgrade timestamp before loading

</td><td>

During instance patch upgrades, many update events are generated for the sn\_kmf\_record\_signature table as the JIT loads many build-time signatures from the plugin to the table. The signature is considered stale, so the signature is loaded again into the table, after which its timestamp is updated. So, a signature which is not present in the table initially is loaded 2 times. The signature is already present in the table as its loaded 1 time.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1846249

</td><td>

Identification and Reconciliation Engine \(IRE\) throws a NullPointerException \(NPE\) when there is a cache flush during IRE processing

</td><td>

 

</td><td>

1.  Run the payload with a break point after 'setIndependentQueryFromPayload' method locally.
2.  Create a new break point after the 'setIndependentQueryFromPayload' to stop the thread.
3.  Open another window.
4.  Log in to /cache.do.
5.  Perform the cache flush.
6.  Resume the execution of thread stopped in step 2.

 Observe NPE.

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

Database Connection

 PRB1928984

</td><td>

'Stop' retries if the connection pool has waited for a connection for longer time

</td><td>

Repeated errors messages 'The connection attempt failed' occur when the txid is the same for hours. Connection creation requests can be unreasonably slow. When the PostgreSQL service is stopped in a lab, almost instant failures are experienced and it takes 13 seconds to exhaust all retries. In a production environment, when a DB host becomes unavailable due to hardware failure, it can take hours to exhaust all retries because each request takes ~100 seconds per request.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1881821

</td><td>

Unable to recognize the alias DBI quote in SqlJoinOptimizerV2

</td><td>

SqlJoin OptimizerV2 throws an IllegalArg Exception for the log file.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1916672

</td><td>

Use a primary key rather than the sys\_id for the **Target key** field when creating edges for subgraphs

</td><td>

The current code assumes its sys\_id, but with Workflow Data Fabric \(WDF\), that's no longer always the case.

</td><td>

1.  Create a WDF table with a primary key column that's name is something other than the sys\_id.
2.  Create a reference to that table from another table.
3.  Create a name subgraph with the tables in them.
4.  Try to traverse the edge for that reference.

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

 PRB1932785

</td><td>

No response for the queries executed via a non-admin role

</td><td>

The user doesn't get a response for queries when trying to run them as an non-admin user, even when the generated cypher is correct and there is data to be fetched.

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

 PRB1934684

</td><td>

getForTables on KG Global Graph isn't returning all the edges from contribution graphs

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

Time regular cypher execution times.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1762209

</td><td>

ITERATIVE\_CHUNK \_PROCESSOR creates too many chunk entries in the sys\_dm\_chunks table

</td><td>

 

</td><td>

1.  Set the property 'glide.db.unreferenced\_ record\_cleaner.large \_table\_threshold' to a smaller value so that the unreferenced table cleaner process type is ITERATIVE\_CHUNK\_PROCESSOR.
2.  Bulk up the data in sys\_object\_source with unreferenced records from six physical reference tables.
3.  Run the 'DMScheduler' to process the unreferenced table cleaner.

 Notice the data that gets inserted in the sys\_dm\_chunk table.

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

 PRB1800838

</td><td>

The GLIDE\_ELEMENT\_EXTENSIONS cache access is slow due to CacheManager

</td><td>

There's no need for this to use CacheManager. Extensions don't need to be flushed when using extension point listeners.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1901056

</td><td>

Remove redundant pool expansion rejected messages for background operations

</td><td>

Logs continue to grow in xmlstats, and are expected to grow even. Only logs should be removed.

</td><td>

1.  Configure a DB pool to be small \(less than number of worker threads\).
2.  Observe logs such as 'Pool: glide: pool expansion rejected lowest\_ratio=0.030901287553648068 is\_bg\_op=true 2\)' also growing in xmlstats.

</td></tr><tr><td>

Database Persistence

 PRB1920823

</td><td>

Data is lost on updateMultiple with the type 'phone number E164'

</td><td>

In sys\_dictionary, the user can set the 'mobile\_phone' element of 'sys\_user' to 'Phone Number E164.' If the user later updates the company for someone in the base instance data set, the **mobile\_phone** field gets set to null.

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
2.  On a user's table, select the **Nation key** columns as a reference.
3.  Try to select **Finish**.

 It throws an error: 'Reference column 'c\_nationkey' mapped to remote column 'c\_nationkey' is using type longint which is not supported for reference columns'.

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

Declarative Actions

 PRB1819856

</td><td>

Declarative actions \(Move, Add, Change, Delete\) aren't enabled when 'group by' is applied on any column for active PI records

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1839235

 [KB2477345](https://hi.service-now.com/kb_view.do?sysparm_article=KB2477345)

</td><td>

Too many inserts into 'discovery\_cloud\_temp\_results' for static data contributes to replication lag

</td><td>

Having too many cloud discovery schedules, such as 1 for each account, can potentially cause replication lag due to too many inserts into discovery\_cloud\_temp\_results for the 'cmdb\_ci\_cloud \_hardware\_type' ci type.

</td><td>

1.  Have DB replication.
2.  Have 30 nodes in a cluster.
3.  Have thousands of service accounts.
4.  Configure 1 disco schedule for each service account.
5.  Run the schedules at close intervals.

</td></tr><tr><td>

Discovery

 PRB1842017

</td><td>

Unnecessary DMLs run by HostIdentificationUtil.findHostByIp\(\) for Cloud Discovery, which add a load to the database and prolong the Discovery schedule

</td><td>

When discovering hundreds of service accounts in Cloud Discovery, potentially hundreds of thousands of unnecessary queries are ran, adding load to the DB and prolonging the Discovery Scan.

</td><td>

1.  Have many nodes in the cluster.
2.  Have many cloud resources which ideally have a resource that all Cloud Patterns would return.
3.  Create a single Discovery schedule that would discover 500+ service accounts.
4.  Instrument HostIdentificationUtil.findHostByIp\(\).
5.  Verify the number of times this method is unnecessarily executed, running hundred of thousands of queries, slowing down the DB.

</td></tr><tr><td>

Discovery

 PRB1893089

</td><td>

The 'Discovery::getScheduleContainingAnyIP\(\)' API causes slow pressing of 'change\_request. trigger.discovery' sysevents

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
2.  Notice that this should give a variety of errors.
3.  Look at the discovery log.

 Notice that 'Failed Exploring CI Pattern' occur for discoveries that actually brought data.

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

 PRB1933778

</td><td>

Add MID configuration parameter names in commons for the integration to store private keys

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1919853

</td><td>

Issue with system properties not parsing numbers 0.1 vs 0,1

</td><td>

When an instance is set up with European formatting, such as the decimal being written 0,5 as opposed to the US format of 0.5, the system properties for the threshold values aren't parsed properly, returning an error.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1923569

</td><td>

A flow creates duplicate records in IT Asset Management \(ITAM\) target tables

</td><td>

An extracted table displays 3 rows but the flow ends up creating 6 rows in the ITAM table.

</td><td>

 

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

The edge decryption job doesn't check the correct column for **journal/audit** fields

</td><td>

When deciding to column level encrypt data or not, the edge decryption job doesn't check the correct column for **journal/audit** fields. As a result, the **journal** field and audit entries aren't CLE encrypted.

</td><td>

1.  Configure the **Journal** field to be edge encrypted.
2.  Run an edge mass encryption job to encrypt the data.
3.  Configure the CLE module/map/configuration on the same field.
4.  Ensure that the configuration is active.
5.  Ensure that the edge user has access to this CLE module.
6.  Notice that the edge user is configured in its edgeencryption .properties file \(edgeencryption .target.username property\). The user that's configured to connect to the instance must have access to the CLE module or else the decryption job won't attempt to encrypt with it.
7.  Disable the edge encryption configuration for the field.
8.  Run the edge decryption job on the field.
9.  Check the process historical records.

 Expected behavior: The **Journal** field entries in sys\_journal\_field are CLE encrypted. **Audit** field entries are also CLE encrypted.

 Actual behavior: The **Journal** field and audit entries aren't CLE encrypted.

</td></tr><tr><td>

Edit List Columns

 PRB1844708

</td><td>

Changes to 'My Lists' from the 'List' bundle SNC variant aren't saved

</td><td>

When the user creates a list under 'My lists' in Service Operations Workspace and configures the columns or changes the filters, the changes reflect immediately. But if the user switches over to another page or list, the changes are reverted.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1833179

</td><td>

The **Send Email** button in an email draft doesn't work

</td><td>

In the CSM Workspace, the **Send Email** button doesn't work for an email draft that's opened via the 'Open Draft in a Tab' icon.

</td><td>

1.  Open an instance.
2.  Navigate to the CSM Workspace.
3.  Open an incident record.
4.  From the 'Activity Stream Compose' section, select the 'Email' tab in the compose area.
5.  Enter content in the email compose area.
6.  Select the **Open draft in a tab** icon.

 Observe that the **Send Email** button does not work in the new tab that opened for the email draft. The email can't be sent.

</td></tr><tr><td>

Employee Relations Case Management

 PRB1909215

</td><td>

There's no base instance scoped ACL for sn\_hr\_er and asmt\_assessment \_instance\_question

</td><td>

The user can't read a specific asmt\_assessment \_instance\_question record, even though the user has the required role. There isn't a base instance scoped ACL for sn\_hr\_er, but there is one for sn\_hr\_core.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1838299

 [KB1906970](https://hi.service-now.com/kb_view.do?sysparm_article=KB1906970)

</td><td>

Incident impact is not set due to out-of-sync jobs

</td><td>

Alert priority group calculation isn't updating system fields on an alert.

</td><td>

1.  Open an 'Alert Management' rule.
2.  Activate 'Create Incident'.
3.  Send events every few seconds for around 30-40 seconds.
4.  Wait until all alerts and incidents have been created.
5.  Verify that for some incidents, the impact is not set.
6.  To verify, set the property evt\_mgmt.enable\_ alert\_priority\_group \_explicit\_update to true.

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

Flow Engine

 PRB1927282

</td><td>

Sync requests are failing in the NowLLM Media action

</td><td>

sn\_ml.MLServiceUtil.parse TritonResponse \(headerContentLength, responseBody\); throws an exception and the flow to fails. This is only occurs when the One Extend call is synced.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1927401

</td><td>

Yield should only occur between flow element executions

</td><td>

If a flow has been compiled on one node \(the new version\) and then executes on another node \(the old version\), the flow fails because it doesn't have the new Java code.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1923234

</td><td>

Add FDCollection complex object after all applications are installed

</td><td>

 

</td><td>

Install the Open Line - Predictive Intelligence app.

 Expected behavior: FDCollection complex object exists.

 Actual behavior: FDCollection complex object doesn't exist.

</td></tr><tr><td>

Form Templates

 PRB1907844

</td><td>

Reference qualifiers on templates aren't supported on SOW

</td><td>

Reference qualifiers on templates aren't supported on SOW. When the user selects the search icon, a pop-up opens.

</td><td>

1.  Navigate to **Navigator** &gt; **Standard Change** &gt; **All Proposals**.
2.  Open any active standard change proposal.
3.  Navigate to **Change Request values**.
4.  Select the **Assigned to** or the **Service offering** field.
5.  Select the **Search** icon.

 Observe that a pop-up opens.

</td></tr><tr><td>

History Set

 PRB1892171

</td><td>

setJournalEntry\(data, 'user name'\) API doesn't work as expected

</td><td>

When the API setJournalEntry\(data, 'user name'\) is used, the sys\_audit.user correctly reflects the user passed into the API, but sys\_created\_by captures the user that's currently logged in.

</td><td>

 

</td></tr><tr><td>

Horizon Button Stateful Component

 PRB1842512

</td><td>

The **Button Stateful** component isn't displayed in the UIB or the run time

</td><td>

 

</td><td>

1.  In a Xanadu instance, open any experience in UIB.
2.  Create a page from scratch or open an existing page.
3.  Add the **Button Stateful** component to the stage.
4.  Save the changes in the UIB page.

 Expected behavior: The **Button Stateful** component should be displayed in the UIB and the run time.

 Actual behavior: The component isn't displayed.

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

HR Service Delivery

 PRB1920738

 [KB2525534](https://hi.service-now.com/kb_view.do?sysparm_article=KB2525534)

</td><td>

HR Case description \(**rich\_description**\) doesn't copy over data, and the rich description is left empty

</td><td>

Rich Description appears as null in List View but displays correctly in the case record. The reverse works as expected--when updating the **rich\_description** field in the HR case form, the value will appear in the **rich\_description** field in the list view.

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
12. Observe that the same value is automatically updated in the **rich\_description** field due to a business rule that syncs values between the two fields.
13. Open the list view.
14. Add the Description and rich\_description columns.

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

HTTP Client

 PRB1833182

</td><td>

The outbound HTTP request log for async HTTP Client doesn't accurately account for request execution time

</td><td>

The timer starts from the first response byte received. The actual response timer should start right after the request is sent to the endpoint. It should have a total time which includes connection setup, request writing, and response time. It can show distribution \(Connection Setup, Request Write and Response time\).

</td><td>

Run async requests from Virtual Agent or the Now Assist panel.

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB1930639

</td><td>

Clone Admin console 'Request' page performance

</td><td>

 

</td><td>

Navigate to **Clone Admin** &gt; **Request Clone**

 Notice that the 'Request' page takes an average of 20 secs to load.

</td></tr><tr><td>

Instance Scan

 PRB1927870

</td><td>

Instance Scan excludes inactive records, even when the system property 'glide.scan.base \_system\_records' is enabled

</td><td>

When running a custom Instance Scan table check, inactive records are not included in the scan results, even if no conditions are set on the scan check record. This occurs even after setting the system property 'glide.scan.base \_system\_records = true'. For example, creating a scan against sc\_cat\_item with the condition 'active = false' returns no findings, despite the existence of inactive, custom-created records.

</td><td>

1.  Create a new Table Instance Scan Check.
2.  Set the target table to 'sys\_app' or 'sc\_cat\_item'.
3.  Add the script in the 'Advanced' tab.
4.  **Save** it.
5.  Run a Test Scan.

 Observe that inactive records are not scanned and boolean conditions such as 'active = false' return zero results.

</td></tr><tr><td>

Integration Hub

 PRB1928792

</td><td>

Unable to connect to ServiceNow MCP Server using ServiceNow MCP Client

</td><td>

'Apply Default Headers' is being called before ApplyHeaders which always adds the 'Accept: text/event-stream' header. Any headers added in the step are added as well, causing the duplicate headers. The text/event-stream header shouldn't be added if there is an accept header added in the step.

</td><td>

1.  Create a SSE step to any endpoint.
2.  Add a header with the value 'Accept: application/json,text/event-stream'.
3.  Test the SSE step.

 Notice that the results show the Accept header as the value 'application/json,text/event-stream'.

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

Integration Hub

 PRB1931511

</td><td>

Support WS-security profiles in a Flow Designer SOAP step on MID

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Integration Hub Remote Process Sync

 PRB1881251

</td><td>

Inbound queue processing sticks if there's a corrupted inbound queue record

</td><td>

The records are stuck in a 'Ready' state after running the Remote Process Sync Inbound Job.

</td><td>

1.  Create two process event, P1 and P2, in instance A \(sender\) and instance B \(receiver\).
2.  Including the process definitions.
3.  Create an outbound flow for both P1 and P2 events in instance A \(sender\).
4.  Configure everything in the sender instance.
5.  Create an inbound flow for event P1 in instance B \(receiver\).
6.  Don't create an inbound flow for event P2 in the instance B \(receiver\).
7.  Trigger the P2 event first from the sender instance.
8.  Trigger multiple P1 events after that.
9.  Ensure that the data is captured and sent from the instance A \(sender\), and it appears in the inbound queue of the instance B \(receiver\) in sequence, so that there's one P2 event first and 5-10 P1 events later.
10. Navigate to **sys\_trigger table**.
11. Run 'Remote Process Sync Inbound Job'.
12. Navigate to the **ih\_sync\_inbound\_queue\_record table**.

 Notice that all the records are stuck in the 'Ready' state.

</td></tr><tr><td>

Key Management Framework \(KMF\) for Platform Encryption

 PRB1917107

</td><td>

Asymmetric module keys with Multiple Active keys won't always pick up the current instance keys

</td><td>

The CryptoOperations API picks the active key ordered by date whether that key is generated on that instance or not. When automations like clone run on the instance, there appears to be a brief period where both the source and target instance's module keys are present on the target instance. For Asymmetric operations like signing, before re-key is successful, CryptoOperations API might use keys that don't belong to that instance. After re-key is complete, the same operation uses keys that belong to the current instance.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1913708

</td><td>

The KMF customer action page no longer displays the latest certificate vulnerability due to a missing **experience\_properties** field

</td><td>

The KMF has a 'Customer Action' page with a custom script that uses the **experience\_properties** field. This field is not populated in Zurich, which causes the feature to break.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1913382

</td><td>

The 'Close' tooltip is hard-coded and untranslated

</td><td>

The 'Close' tool tip is translated on the GenAI Modal pop-up, however it remains hardcoded in Task Selector, Language Pop-up, and in the Drafting article dialog.

</td><td>

Scenario 1:

 1.  Create an article from Incident or Case using Agent Flow from UI16.
2.  Select **Create Knowledge**.
3.  Wait for the pop-up to display.
4.  Notice that the 'Close' tool tip is now translated.
5.  Select **Continue**.
6.  Wait for the language pop-up to display.
7.  Hover over the cross icon.
8.  Check the untranslated tool tip.
9.  Select **Continue**.
10. Hover over the cross icon on the drafting icon pop-up.

 Notice that the 'Close' tooltip is hard-coded and untranslated.

 Scenario 2:

 1.  Create an Article from Author flow from UI16.
2.  Wait for the pop-up to display.
3.  Notice that the 'Close' tool tip is now translated.
4.  Select **Continue**.
5.  Wait for the 'Task' selection to display.
6.  Hover over the cross icon.
7.  Check the untranslated tool tip.
8.  Select **Continue**.
9.  Wait for the language pop-up to display.
10. Hover over the cross icon.
11. Check the untranslated tool tip.
12. Select **Continue**.
13. Hover over the cross icon on drafting icon pop-up.

 Notice that the 'Close' tooltip is hard-coded and untranslated.

</td></tr><tr><td>

List Administration

 PRB1237246

 [KB0752370](https://hi.service-now.com/kb_view.do?sysparm_article=KB0752370)

</td><td>

String values displayed in list V2 and list V3 automatically remove or truncate more than one empty space to one empty space

</td><td>

This issue causes inconsistency to users when they copy the string from the display of the list, as the actual value isn't truncated, and only the displayed value is truncated.

</td><td>

1.  Log in the latest base instance.
2.  Navigate to **Incident** &gt; **Create New**.
3.  Create a new incident with short description containing more than one empty space between words, for example, 'test 123'.
4.  Include the **Short description** field in the Incident list.
5.  Filter the incident list with short description 'test 123'.
6.  Observe that the system will fetch and display the new incident record which was created with short description, and this short description is displayed on the list.

 Expected behavior: The data should be displayed without any auto truncation, and the short description should be displayed as 'test 123'.

 Actual behavior: The data is displayed with auto truncation, and the short description is displayed as 'test 123'.

</td></tr><tr><td>

List Administration

 PRB1837569

</td><td>

Inline edit doesn't pop up after double-clicking in the list page

</td><td>

Inline edit doesn't pop up after double-clicking \(or using the keyboard shortcut\) in the list page / presentational list component created through the list page template in UI builder.

</td><td>

1.  Open the UI builder.
2.  Create a workspace experience.
3.  Add a page using the 'List page' template, which implements the 'Presentational list' component.
4.  Preview and open the URL path for this page.
5.  If you don't see a record for the first selected table, create a list from the sys\_user table so that there's a record in the first load page.
6.  Record the URL of the above page.
7.  Close the existing workspace tab.
8.  Open the tab again.
9.  Double-click \(or use the keyboard shortcut\) on any field to enable the inline edit in list.

 Expected behavior: The inline edit appears.

 Actual behavior: The inline edit isn't enabled after the first load. When you do pagination \(or navigate to another list\) and then return, the inline edit is enabled.

</td></tr><tr><td>

List Administration

 PRB1843211

</td><td>

Only the 'Save a copy' option should be available for the 'Shared with me' and 'Opened by link' sections

</td><td>

The rename, delete, save, and share options are all available for a list in the 'Shared with me' or 'Opened by link' sections. Only the 'Save a copy' option should be available.

</td><td>

1.  Navigate to **UI Builder** &gt; **List page template**.
2.  Add the filters to the default list.
3.  Copy and paste the URL in a new tab.
4.  Save the list in the 'Created by me' section.
5.  Share the list with a user.
6.  Impersonate that user.
7.  Load the list in the 'Shared with me' section.
8.  Select the **three dots**.

 Expected behavior: Only the 'Save a copy' option is available.

 Actual behavior: The rename, delete, save, and share options are available.

</td></tr><tr><td>

List Administration

 PRB1847192

</td><td>

Inline edit doesn't work for reference dot-walked fields.

</td><td>

The updated value shows as 'Action,' and when it's refreshed, the values aren't updated.

</td><td>

1.  Create a UIB page with a record list header and a presentation list with the list controller preset.
2.  Use the incident table's default view.
3.  Add a dot walked reference field to the default view \(for example, navigate to**Configuration item** &gt; **Company**\).
4.  Try to do a cell edit on the **Company** field.
5.  Select the **Reference search** button.

 Observe that the updated value shows as 'Action.' When it's refreshed, the values aren't updated.

</td></tr><tr><td>

List Administration

 PRB1856664

</td><td>

Inline editing of a newly added choice type column isn't allowed

</td><td>

 

</td><td>

1.  Take any existing table \(for example, an incident table\).
2.  Create a new column type choice.
3.  For values, select the **Without none** option.
4.  Create an experience.
5.  Add an RLB to the page.
6.  In runtime, try inline editing the new column.

 Observe that the pop-up isn't displayed.

</td></tr><tr><td>

List Administration

 PRB1916174

</td><td>

The header notification doesn't render when SN\_RECORD\_LIST\_DATA\_ BROKER\#ADD\_ NOTIFICATIONS is dispatched

</td><td>

When repeating in NRLC, the error occurs as well. The error message comes from a Data Policy that prevents 'Assigned to' from being empty.

</td><td>

1.  Create a new list against the problem\_task table.
2.  Attempt to remove the value in 'Assigned to' in the new list.

 Expected behavior: Notice the error message.

 Actual behavior: No error message appears.

</td></tr><tr><td>

List Administration

 PRB1917110

</td><td>

In Yokohama, the fixed filter condition doesn't calculate the sum in list view

</td><td>

The total value calculation doesn't account for the fixed filter condition defined in the module.

</td><td>

1.  Enable the calculated list configuration for a decimal-type field.
    1.  Select and hold \(or right-click\) the column header in the list view. For example, Sunday in the time\_card table.
    2.  Select **Total Value**.
2.  Navigate to the sys\_app\_module table.
3.  Create a module with a fixed filter condition using the URL from arguments. For example, time\_card\_list.do? sysparm\_fixed\_query =user=javascript: gs.getUserID\(\).
4.  Impersonate any user.
5.  Open the time\_card list view via the module.
6.  Check the sum value displayed for the configured decimal field.
7.  Manually apply the same filter condition using the list filter.

 Observe that the total value calculation does not account for the fixed filter condition defined in the module. This behavior works correctly in the Xanadu instance.

</td></tr><tr><td>

List Administration

 PRB1923987

</td><td>

Unable to edit dot-walked choice fields and remove commas from the display

</td><td>

The user can't edit dot-walked choice fields or remove commas from the display on the integer value on the 'Presentation List' component. It's supported in the List component, but when the user hovers on the List component, it shows that it will be deprecated soon and the 'Record List' component should be used instead \(which also uses the 'Presentation List' component\).

</td><td>

1.  Navigate to **UI Builder**.
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

An **integer/number** field is always shown with commas, even though the attribute format is set as none in the sys\_dictionary record of the field.

</td><td>

1.  Navigate to **UI Builder**.
2.  Create an experience.
3.  In a page variant, add 'Record List Bundle' and set a table to it.
4.  Add an **integer** field to the list view.
5.  Navigate to the sys\_dictionary record of the field and set the attribute as format=none.
6.  Preview the page.

 Observe that the dot-walked field is not editable on the list view.

</td></tr><tr><td>

List Configuration

 PRB1835341

</td><td>

The editRowActions transform script fails when 'quick edit' is turned off

</td><td>

The actions property of rowDefinitions isn't initialized when all the default actions are disabled.

</td><td>

1.  Open a Xanadu instance.
2.  In the UI Builder, create a list with the record list bundle.
3.  In the list controller, disable all the base instance end user edit capabilities.
4.  In the advanced section of the list controller, add a new customization script to run on data fetch.
5.  Add an '.editRowDefintions' line to the script with valid add inputs.
6.  Attempt to navigate to the page the record list bundle is placed on.

</td></tr><tr><td>

List Configuration

 PRB1862590

</td><td>

Non-admin users see ACL errors when using suggestions on form fields

</td><td>

Non-admin users who do not have sufficient access to the **sys\_choice table** fields encounter ACL errors when selecting the **Suggestion** icon on a form field.

</td><td>

 

</td></tr><tr><td>

List Configuration

 PRB1865237

</td><td>

Checking **Hide quick edit** in a UX List record doesn't hide the **Quick edit** button

</td><td>

After checking **Hide quick edit** in a UX List record, the **Quick edit** button isn't hidden in Service Operations Workspace.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1916650

 [KB2421892](https://hi.service-now.com/kb_view.do?sysparm_article=KB2421892)

</td><td>

Patterns on agent commands are randomly failing with allow list errors

</td><td>

Collecting MSSQL DB details using ACC discovery fails to fetch DB details with an error message. The exception occurred when executing a command on Agent. The error occurs when processing the adhoc check request: 'command failed due to allow list exclusion: check command denied by the agent allow list. Context: Asset allow list empty, using agent config file allow list.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

ML Normalization for SAM

 PRB1815525

</td><td>

ML Normalization doesn't try to normalize the discovery models that were missed by an older ML model version

</td><td>

The discovery model isn't picked up by ML Normalization, and the value of the **model\_version** field is still the previous model number.

</td><td>

1.  Provision an instance with com.snc.samp and the ML normalization plugin installed.
2.  Create a discovery model that can be normalized with only a product map, such that the status of this DM is 'Partially Normalized'.
3.  Set the value of the **model\_version** field to a previous model number.
4.  Run the SAM - Normalize discovery models using the machine learning scheduled job.

 Expected behavior: The discovery model you created is normalized by this job. This can be verified by checking if the **model\_version** field corresponds to the latest model or not.

 Actual behavior: The discovery model isn't picked up by ML Normalization. The value of the **model\_version** field is still the previous model number you set in step three.

</td></tr><tr><td>

Mobile Platform

 PRB1858372

</td><td>

Activity stream doesn't work if it's missing a participant

</td><td>

This issue occurs when logging into the Agent app as a normal user.

</td><td>

1.  Create an activity with empty participant for an existing Work order task.
2.  Log in to the Agent app.
3.  Navigate to the Work order task.

 Expected behavior: The activity stream should be loaded in 'Activity Stream' tab.

 Actual behavior: No activity is displayed in 'Activity Stream' tab.

</td></tr><tr><td>

Mobile Platform

 PRB1889072

</td><td>

The ScriptedUnsavedChanges ConfirmationJsBuilder causes a stack overflow exception

</td><td>

The ScriptedUnsavedChanges ConfirmationJsBuilder causes a stack overflow exception due to a race condition from DeferredClassNamespace.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1916821

</td><td>

The prefetch logic for the parameter screen is broken when using scripted variables

</td><td>

When using scripted variables, the prefetch logic for the parameter screen is broken. As a result, the input form screen contains an empty input.

</td><td>

Scenario 1:

 1.  Create a button with an input form screen.
2.  Add an input and a scripted variable to the input form screen.
3.  Make the script of the scripted variable execute longer than ten milliseconds.
4.  Auto-fill the input with the scripted variable.
5.  Add the button to the 'Navigation' section.
6.  In the online mode, select the button.

 Expected behavior: The input form screen contains the input with the auto-filled value.

 Actual behavior: The input form screen contains an empty input.

 Scenario 2:

 1.  Provision an instance with the following applications installed: app-wsd-core, app-wsd-reservation, app-wsd-mobile, and app-wsd-space-mgmt.
2.  Log in to the instance using the requestor mobile application.
3.  Select the top menu.
4.  Create a new reservation with the building and floor.
5.  Open the 'My Reservations' list screen.
6.  Swipe an item.
7.  Select the **Edit** button.
8.  View the input form.

 Expected behavior: The building input is prefilled with the selected floor.

 Actual behavior: The building input is empty. This problem occurs because the building or floor calculation occasionally times out and is skipped. In the previous logic, the prefetch mechanism was used for evaluation.

</td></tr><tr><td>

Mobile Platform

 PRB1919819

</td><td>

An error occurs when returning standard search results that don't have attachments associated with them

</td><td>

This problem occurs with iOS and Android requestor 20.2.

</td><td>

1.  Log in as an admin user.
2.  Search for standard search results that don't have attachments associated with them \(for example, iPhone\).

 Expected behavior: Standard search results should return.

 Actual behavior: Error returning standard search results that do not have attachments associated with them.

</td></tr><tr><td>

Mobile Platform

 PRB1931576

</td><td>

Offline-mode payload generation has excessive memory retention, causing performance degradation due to an SG offline document job

</td><td>

The Yokohama release introduced major changes to the way in which mobile offline payloads are generated, most notably embedded forms are now transformed into redirected forms. This removes the embedded forms from list screen documents and turns them into separate documents. With that change resulted in an increase in the number of documents that are processed during offline payload generation. This number can spike to as large as twice or three times as many documents processed compared to previous releases. As such, this results in an excessive number of GlideRecord instances being retained in memory. This has been seen to cause memory issues, node restarts, and severe performance degradation for users.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1867699

</td><td>

A Filter navigator doesn't change nor update for typing input after an application scope has been changed

</td><td>

The Filter navigator doesn't change or update when entering an input after the application scope has been changed. This issue occurs after upgrading to Yokohama.

</td><td>

1.  Log in to an instance.
2.  Ensure the application scope is set as 'Global'.
3.  Pin the Filter navigator.
4.  Enter in the Filter navigator, 'local update \(set\)'.
5.  Observe that it has updated the panel.
6.  Set the application scope to anything else, such as Admin Center or Access Analyzer.
7.  Enter in the Filter Navigator, 'local update \(set\)'.

 Expected behavior: The Filter navigator should update the panel with relevant results, or let the user no results are returned.

 Actual behavior: The Filter navigator is frozen and doesn't do anything.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1897388

</td><td>

Content page fails to load via module after upgrade to Yokohama

</td><td>

The configured content page isn't loaded to a new browser tab. Instead, a blank page is loaded with /view\_content.do? sysparm\_sys\_id=null at the end of the URL.

</td><td>

1.  Provision a Yokohama instance with the CMS plugin \(com.glide.cms\) installed.
2.  Open any base instance content page or custom content page.
3.  Select the **View Page** link, which loads the page content successfully.
4.  Open **System Definition** &gt; **Modules**.
5.  Select **New**.
6.  Enter the new module title information.
7.  Select the app in the **Application menu** field
8.  Open the 'Link Type' tab.
9.  In the **Link Type** field, select **Content Page**.
10. In the **Content Page** field, look up to the content page that validated earlier.
11. Save the record.
12. Log in to the instance again or reload the home page of the instance to make sure you see the new module via the navigator.
13. Select the module.

 Expected behavior: The configured content page is loaded to a new browser tab successfully.

 Actual behavior: A blank page is loaded with view\_content.do?sysparm\_sys\_id=null at the end of the URL.

</td></tr><tr><td>

Next Experience User Menu

 PRB1926920

 [KB2442915](https://hi.service-now.com/kb_view.do?sysparm_article=KB2442915)

</td><td>

On instances with AI Agents, some users can't be found on the impersonation list

</td><td>

Currently, users with the **Identity type** field set to 'AI Agent' are filtered out, but they must also be filtered by 'is empty'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now Assist Panel

 PRB1909094

</td><td>

The **Show more** button isn't visible on NASS for Safari browsers

</td><td>

When using the Now Assist Panel \(NAP\), Now Assist for Virtual Agent \(NAVA\), or Now Assist for Request \(NASS\) on Safari, the **Show more** button isn't visible after truncation, so the user is unable to see the full message. This prevents users from accessing the complete content of responses.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1911693

</td><td>

Text in the 'Reply text' box is cut off

</td><td>

 

</td><td>

1.  Select **Now Assist panel** \(NAP\).
2.  Verify the text in the reply text box.

 Expected behavior: The 'Assist' text is displayed.

 Actual behavior: The 'Assist' text is cut off.

</td></tr><tr><td>

Now Assist Panel

 PRB1916658

</td><td>

The hand cursor isn't displayed when hovering over the **chat history** button

</td><td>

When the user hovers over the **chat history** button, the **I** icon is displayed instead of hand symbol.

</td><td>

1.  Select **NAP**.
2.  Hover over the **Chat history** icon.

 Observe that the **I** icon is displayed instead of hand symbol.

</td></tr><tr><td>

Now Assist Panel

 PRB1929041

</td><td>

SKILL\_EXECUTION\_STARTED passes aiaExecutionPlanId as empty in its payload

</td><td>

 

</td><td>

1.  Navigate to an instance.
2.  Select the **Sparkling** icon to trigger AIEX.
3.  Keep the debugger at the SKILL\_EXECUTION\_STARTED' action handler.
4.  Trigger the 'Canvas flow' use case.
5.  Observe that SKILL\_EXECUTION\_STARTED is passing 'aiaExecutionPlanId' as an empty value.

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

Citation links are missing for the KB in the follow up

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

Skills aren't turned off after selecting in Now Assist Portal

</td><td>

 

</td><td>

1.  Open Now Assist Portal.
2.  Enter 'summarize a record'.

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

OAuth

 PRB1927389

</td><td>

Support JWT Token format for OAuth access tokens

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1855080

</td><td>

The 'Reminder Report' displays in the incorrect format when multiple shifts are created in US/Central

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1923685

</td><td>

When executing a couple of Zoom Agents, an IllegalAccess error is thrown

</td><td>

The same issue is observed for the 'Create Meeting' Agent.

</td><td>

1.  Log in to an instance.
2.  Navigate to Virtual Agent UI.
3.  Provide the prompt, 'Please create a user having an email ID as the username. The user should be a basic user only.

 Expected behavior: A user should be created in Zoom.

 Actual behavior: The message appears, '\{'message':'Invalid inputs for tools execution: JavaException: java.lang.SecurityException: Illegal access to package\_private script include function AIAFdihDataTypeConstants: caller not in scope sn\_aia'\}'.

</td></tr><tr><td>

OneExtend

 PRB1925075

</td><td>

Flow Designer retries aren't working with async non-quick mode capability executions

</td><td>

The OneExtend API returns an error without doing the retries.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1925347

</td><td>

sys\_one\_extend\_ definition\_attribute records aren't cached

</td><td>

AI Agent also queries for the records to execute tool type capabilities. When caching the records in One-Extend to get scriptable API to access the cached records in the AI Agent store app, the cache can be used.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1927150

</td><td>

User gets a script error for an execution request

</td><td>

The script execution error: 'Script Identifier: null.null.script, Error Description: java.lang.NullPointerException: Cannot invoke 'String.equalsIgnoreCase \(String\)' because the return value of 'com.glide.one \_extend.resource. dto.v2.MultiCapability ExecutionRequestDto .getMode\(\)' is null, Script ES Level: 0...'

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1928470

</td><td>

Abnormal GAIC async submission duration

</td><td>

When the user calls certain code with an async request, the response time should be around 0-200 milliseconds. However, the response time can be as high as five seconds because the Builder Entity cache frequently gets reclaimed.

</td><td>

1.  Enable logging sn\_ais\_assist. AISearchNA4S GeniusResultLogger .level=INFO.
2.  Run NAVA QnA flow.
3.  Look at the splunk log pattern 'AISearchNA4S GeniusResultLogger response received! duration'.

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

CheckLLM ModelAvailability takes longer than usual

</td><td>

 

</td><td>

1.  Delete a record from sys\_gen\_ai\_model \_availability for gpt\_small.
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
4.  Select a skill such as **Incident summarization**.
5.  Update the provider to any other provider, such as Google or Amazon, except for the default one.
6.  Verify that the provider has been updated for the record summarization to Google in in sys\_one\_ extend\_capability.
7.  Repair the UXC plugin or install the latest version.

 Notice that the provider is set to the default again.

</td></tr><tr><td>

OneExtend

 PRB1938406

</td><td>

QnA Planner2 call failing with the path /v2/models/ llm\_generic\_large\_v2/infer

</td><td>

 

</td><td>

 

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

 Observe the Planner 2 response displayed but with unexpected JSON style sources output at the bottom.

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
5.  Observe that the streamed output has several words mashed together.
6.  Observe that in the sys\_generative\_ai\_log planner 2 output, the response from LLM itself is this way
7.  Disable streaming.
8.  Repeat the query.

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

Script include-based capabilities aren't executed as a subflow though the required system property is enabled

</td><td>

 

</td><td>

1.  Create a Gen AI capability with it's definition pointing to script include.
2.  Ensure the sys prop 'com.glide.oneapi.run\_ script\_include\_on\_fdih \_engine' is set to 'True'.
3.  Ensure flow debugging is turned on for the subflow.
4.  Run the script include as a FDIH subflow.
5.  Execute the capability from 1 using OneExtend Util.execute API.

 Expected behavior: The script include is executed as a subflow and subflow executions should execute.

 Actual behavior: The subflow 'Run script include as FDIH subflow' won't show any executions.

</td></tr><tr><td>

OneExtend

 PRB1944861

 [KB2556128](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2556128)

</td><td>

Revert NASK licensing charge by token to not include input tokens

</td><td>

The assist charge logged in sys\_gen\_ai\_usage\_log is based on 1 assist per 1000 tokens, where tokens = input tokens + 3 \* output tokens.

</td><td>

Invoke the custom skill created in the NA Skill Kit.

 Observe that the assist charge logged in sys\_gen\_ai\_usage\_log is based on 1 assist per 1000 tokens, where tokens = input tokens + 3 \* output tokens.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1865224

</td><td>

The first modal displays despite **Don't show me this message again** being checked

</td><td>

After migrating a CoreUI dashboard to Next Experience, the message 'Welcome to the Platform Analytics experience' appears when the user opens the migrated dashboard. This modal continues to appear even if the user selects **Don't show me this message again**.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1873596

</td><td>

Hardcoded string 'Ask a question about your data' and 'No results found' for i18n: Platform Analytics

</td><td>

 

</td><td>

1.  Set up a testing environment.
2.  Install French from the Application Manager \(com.snc.i18n.french\).
3.  Navigate to **incident.LIST**.
4.  Show the Natural Language Filter.

 Observe the hardcoded strings for 'Ask a question about your data' and 'No results found'.

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

Playbooks \(Family Channel\)

 PRB1934746

</td><td>

Playbooks archived in X don't work in newer releases

</td><td>

New fields that get added to the deserializer need to handle the keys not existing, which, as of now, is snapshot\_id and variant\_id.

</td><td>

1.  Create an X instance.
2.  Trigger a playbook.
3.  Complete/cancel the playbook.
4.  Archive the playbook.
5.  Upgrade the instance to Y.
6.  Open the playbook.

 Expected behavior: The playbook loads.

 Actual behavior: The playbook doesn't load - 'No stages available'.

</td></tr><tr><td>

Predictive Intelligence

 PRB1892456

</td><td>

Workflow predictions fail when the attachment is missing for word vector corpus in the ml\_model\_artifact table

</td><td>

After deleting the attachment created in the word vector record in the ml\_model\_artifact table, the predictions fail with a bad URL and the word corpus artifact is referenced incorrectly.

</td><td>

1.  Set glide.platform\_ml .api.enable\_workflow\_ similarity to 'false'.
2.  Create a word corpus record.
3.  Create a similarity definition.
4.  Select the word **corpus** created in step 2.
5.  Select **Submit and Train**.
6.  Notice that after successful training, the word vector record is created in ml\_model\_artifact table with an attachment.
7.  Perform the predictions.
8.  Ensure the predictions are successful.
9.  Set glide.platform\_ml. api.enable\_workflow\_ similarity to 'true'.
10. Delete the attachment from the word vector created in step 5.
11. Re-trigger the training.
12. Perform the predictions after successful training.

 Notice that the predictions fail with a malformed URL, and the workflow predictions are incorrectly referencing the word corpus artifact.

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

Predictive Intelligence

 PRB1921497

</td><td>

For similarity, an empty column in the 'Test' table causes an error during predictions

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1921496

</td><td>

The scheduled task name is reset to default if it's renamed when the task is being processed on glide

</td><td>

If the user renames the scheduled task while it's being pre-processed to send to trainer, the name is reset. When the system updates the scheduled task state, it also updates the task with the older, default name.

</td><td>

1.  Apply a transition filter.
2.  Notice that a scheduled task is created and pre-processing starts. The scheduled task is loaded in memory with the default name.
3.  Update the scheduled task name.

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
2.  Configure a MDM project.
3.  Mine a project.

 Notice that the promin\_meterd\_usage table has entries for case ids of both parents and child entities.

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
5.  Go back to the portfolio plan page.
6.  Observe that the values are reflected appropriately.
7.  Open the same demand and update the costplan.

 Observe that the values are not reflected in the portfolio plan page.

</td></tr><tr><td>

Related List Action Model

 PRB1890337

</td><td>

Button to change the fields for the related list is grayed out

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

Related Lists

 PRB1884173

 [KB2075174](https://hi.service-now.com/kb_view.do?sysparm_article=KB2075174)

</td><td>

Users can't add/remove the first option in the slushbucket from side to side when accessibility is enabled in Classic \(Core UI\)

</td><td>

Users can't move the first 'Available' option to the 'Selected' side with a double-click or by using the **Add** button. Selecting one option but then double-clicking another moves both over. If users shift-click to select multiple options, they don't all move over - one remains. CTRL+A doesn't select all options; rather, it appears to toggle the set of selected options.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Reporting

 PRB1870937

</td><td>

The 'Show real-time updates' checkbox isn't shown for non-DF tables

</td><td>

DF tables don't support the real-time mechanism that the platform provides for regular tables. The real-time option should be disabled for single score, dial and gauge in dashboard widget preferences. Also, when using a remote table, the option of real-time is not hidden at all. So instead of only hiding it for DF tables, it can be hidden generically for all remote tables since they don't support real-time updates.

</td><td>

1.  Open any dashboard where the widget was created with a non-DF table.
2.  Select the **Settings** icon.

 Expected behavior: The checkbox should not be removed for non-DF tables.

 Actual behavior: The checkbox is removed for 'Show real-time updates'.

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
5.  Notice that the API call is in a pending state for over a minute.
6.  Select **Run**.

 Observe that 'Loading Report' is shown until the status of API call is finished.

</td></tr><tr><td>

Roles

 PRB1890898

</td><td>

UserHasRole PatchJob may inadequately update user role inheritance if it processes a user prior to original transaction \(M2MSlushbucketSaveJob\) completion

</td><td>

After performing an action that impacts a large number of role inheritances, the expectation is that operation will be required to process a considerable number of users. This results in M2MSlush bucketSaveJob running for several minutes to allow UserHasRolePatchJob to run while M2MSlushbucketSaveJob is still in progress.

</td><td>

1.  Setup an instance to take advantage of fix provided in PRB1744106 \(Yokohama+ or Xanadu Patch 8+\).
2.  Set the system property 'glide.security.inh\_ count\_patcher.enabled' to 'true'.
3.  Generate a relatively complex user-group-roles structure.
4.  Perform an action that is expected to impact a large number of user roles inheritances \(sys\_user\_has\_role\), for example, removing a contain relationship between two roles.
5.  Review user role inheritance post completion of M2MSlush bucketSaveJob.
6.  Run the new RoleManagementVerify\(\) .verifyInheritedRoles\(\); via scripts background.

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

Schedule Optimization

 PRB1894420

</td><td>

Jobs get stuck in progress even when the count matches

</td><td>

The jobs get stuck in progress when two split solution files are processed for the same qualifier at the same time.

</td><td>

1.  Provision an instance with 'Schedule Optimization' installed.
2.  Activate the scheduled intraday flow.
3.  Reduce the processing window to five minutes.
4.  Create intraday events, which triggers intraday to run continuously.
5.  Monitor the intraday jobs.

 Expected behavior: The jobs are completed and processed successfully.

 Actual behavior: The jobs get stuck in progress.

</td></tr><tr><td>

Schedule Optimization

 PRB1895416

</td><td>

'Pause scheduled runs next day' has a reset issue

</td><td>

When intraday is configured with 'On Demand' as true for a qualifier, the option 'Pause scheduled runs next day' has a reset issue. Qualifiers that were paused for optimization on one day are still treated as paused on the next day, because the paused flag is not unset at the end of the day.

</td><td>

1.  Configure intraday with 'On Demand' as true for a qualifier.
2.  Impersonate or log in as a dispatcher for that qualifier.
3.  In DWS, navigate to CSP.
4.  Select **Pause scheduled runs**.
5.  Notice that the paused label is reset on DWS the next day.
6.  Create an intraday event for the same qualifier.

 Observe that the scheduled intraday job doesn't run.

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

 PRB1831404

</td><td>

Multiple dynamic behavior record is generated for a regenerate action

</td><td>

The ability for dynamic behavior enables the creation of AI-generated properties for questions. The design should include a clear indication when these properties are generated by AI.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1929611

</td><td>

E2E time for catalog generation use case is more than 10 seconds \(SLA\)

</td><td>

 

</td><td>

1.  Consider the latest track and complete the set up for text to catalog with latest snapshot versions.
2.  Consider a prompt which would create a 8-9 questions.
3.  Measure the time taken for the API to create the item \(The 'Generation of Catalog Item' scripted rest resource\).

</td></tr><tr><td>

Service Catalog

 PRB1935961

</td><td>

Change 'va\_render\_type' from a **Calculated** to **Static** field

</td><td>

 

</td><td>

Change 'conversational\_render\_type' to **Static/non-calculated** field.

</td></tr><tr><td>

Service Portal

 PRB1935238

</td><td>

Portal page shifts occasionally when **Ask a follow-up** is selected

</td><td>

 

</td><td>

1.  Ensure Agentic AI is set up on the instance.
2.  Enable Dispatcher Workspace \(DW\) on portal.
3.  Search for 'Loaner Laptop'.
4.  Wait for the response to load.
5.  Select the **Loaner laptop** citation.
6.  Select **Request in chat**.
7.  Wait for the chat to open.

 Notice that the Portal page shifts occasionally.

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
10. Notice that there's an entry for the discussion that the user isn't a participant in is visible in the record's Activity Stream.
11. Select **Open Discussion**.

 Expected behavior: Only users who are a participant should see the chat conversation

 Actual behavior: Users that aren't participants in a private chat are still able to see the chat conversation.

</td></tr><tr><td>

Software Asset Management

 PRB1632141

 [KB1346310](https://hi.service-now.com/kb_view.do?sysparm_article=KB1346310)

</td><td>

The scheduled job 'SAM - Normalize discovery models using content library rules' fails when the Content Data Service \(CDS\) library is not complete

</td><td>

The scheduled job 'SAM - Normalize discovery models using content library rules' fails with the following errors: '08:14:33.158 Warning worker. 1 worker.1 txid=9df7afed1b47 WARNING \*\*\* WARNING \*\*\* Get for non-existent record: samp\_sw\_package: 78a1f708db96ef0 0c41a10825 b9619c4, initializing 08:14:33.159 Error worker.1 worker.1 txid=9df7afed1b47 SEVERE \*\*\* ERROR \*\*\* NormalizationEngine: Error: No Match found for in samp\_sw\_publish'.

</td><td>

Refer to the listed KB article for details.

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

An 'Install' table has a cross scope issue since the code is moved to Store

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1920322

</td><td>

On Red Hat, an undetermined reason is caused by an incorrect 'Virtualized By' relationship

</td><td>

A virtual device should have a 'Virtualized By' relationship to a host, but if the 'Virtualized By' is connected to a virtual instance, it's considered as an incorrect relationship. When a virtual install of Red Hat is on a Virtual Machine with an incorrect virtualized by relationship, there's an undetermined reason created for the install. This is because the incorrect VM-host relationship prevented the install to be added in the 'samp\_vminstall\_on\_pinstall' view, so it can't be found when processing the installs in SamNewRedHat PerSocketPair LicenseCalculator. As a result, the install cannot be reconciled by the calculator and is stamped as 'undetermined'.

</td><td>

1.  Create a VM with 'virtualized by' set to a VMWare Virtual Machine instance.
2.  Create a Red Hat Enterprise Linux install and set 'installed on' to the VM created in step 1.
3.  Create an entitlement for a Red Hat Enterprise Linux \(license metric should be per socket pair\).
4.  Run recon.

 Observe the undetermined reason created for the install.

</td></tr><tr><td>

Software Asset Management

 PRB1927168

</td><td>

Duplicated sys\_user and csm\_consumer\_user causes error 'Incorrect Subscription Assignment in SAMPro for M365/Adobe: Licenses Linked to External Role Accounts'

</td><td>

Two users can exist with the same name, one on the 'sys\_user' table and the other on the 'csm\_consumer\_user' table; also, one of them can have the role 'snc\_internal,' while the other has the role 'snc\_external.' Consumer users are external users \(client users\) who can sign up, and the system also allows the employees of the company to sign up as external users. As a result, the SAMPro module for M365/Adobe subscriptions pull works incorrectly. When we collect SaaS license subscribers, as user profiles are picked at random from either of these two tables rather than always using sys\_user.

</td><td>

Make sure that two users exist with the same email, one on the 'sys\_user' table, and the other on the 'csm\_consumer\_user' table.

 Observe that the user resolution randomly picks one.

</td></tr><tr><td>

Software Asset Management

 PRB1932110

</td><td>

SAM Estate Management gets CI Counts PA job, resulting in 17 hour executions in Yokohama

</td><td>

The 'SAM - Software Estate Weekly' job can take up to 17 hours to complete in Yokohama, as opposed to three minutes in Xanadu.

</td><td>

1.  Open a Yokohama instance.
2.  Run the 'SAM - Software Estate Weekly' job.

 Observe that the job takes more than 12 hours to complete.

</td></tr><tr><td>

Software Asset Normalization

 PRB1847357

</td><td>

Users with the sam\_admin role can't view custom software product and custom software product suggestions lists on License Operations

</td><td>

The custom software product and custom software product suggestions lists aren't shown. The custom software products module is available in the nav menu, but it redirects to the table in the classic view.

</td><td>

 

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

Software Asset Reclamation

 PRB1859713

 [KB2058566](https://hi.service-now.com/kb_view.do?sysparm_article=KB2058566)

</td><td>

Reclamation rules to product mappings are added for invalid products

</td><td>

Due to invalid parent values, there are many incorrect product-to-rule records in samp\_m2m\_rule\_product.

</td><td>

1.  For the Microsoft Office 365 Model, add a child suite component where the product is empty.
2.  Add other models where the product is empty.
3.  Add a child suite component where the product does not belong to Microsoft Publisher.
4.  Create a new Microsoft Integration Profile.
5.  Run the 'Import subscription' job
6.  Check the samp\_m2m\_rule\_product table for products added to Microsoft 365.

 Notice that the Software Product column is empty in samp\_m2m\_rule\_product.

</td></tr><tr><td>

Software Models

 PRB1902396

 [KB2289933](https://hi.service-now.com/kb_view.do?sysparm_article=KB2289933)

</td><td>

Query errors display on a Software Model record due to a client side GlideRecord query

</td><td>

There's a discrepancy in a client script with the 'Show/Hide Suggestion' icon between the roles that can access cmdb\_model\_software records and those that can access samp\_software\_model\_suggestion records.

</td><td>

1.  Impersonate any user who can't read the 'Software Model Suggestions' table, but can read the 'Software Model' table.
2.  View a 'Software Model' record.

 Note the error messages which appear on the form.

</td></tr><tr><td>

System Export Sets

 PRB1857489

</td><td>

Export to XLSX contains empty string for blank cells which return FALSE when using =ISBLANK\(\) macro

</td><td>

When exporting some records as .xlsx and using the 'ISBLANK' function in Microsoft Excel, the data that the function is displaying is wrong. The 'ISBLANK' function returns 'false' even though the cell is empty.

</td><td>

 

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

 PRB1915159

</td><td>

Failed tier two chunks can block additional chunks for a rule from being processed

</td><td>

If tier two chunks continue to fail when retried, they can block additional chunks for a rule from being processed.

</td><td>

1.  Generate a record with an offload that perpetually breaks.
2.  Make it fail on offload with a 60 minute retry period.
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

Time Card Management

 PRB1890157

</td><td>

On the Time Sheet Portal, tooltips sometimes remain stuck on the screen in Yokohama

</td><td>

If a user hovers over another tooltip, the original one remains in most cases.

</td><td>

1.  Open a Yokohama instance with Time Card Management.
2.  Impersonate 'System Administrator'.
3.  Open the Time Sheet Portal.
4.  Add some operational time cards from the 'Other' section.
5.  Hover over the operational labels or the numbers for the daily totals.

 Notice the tooltips remain for a prolonged time or indefinitely.

</td></tr><tr><td>

Time Card Management

 PRB1896237

</td><td>

A negative hour time card update is possible from the Time sheet portal form view even when it's blocked in Portal

</td><td>

This issue was observed in Yokohama.

</td><td>

1.  Open the timesheet portal.
2.  Add a time card.
3.  Open it in a form view.
4.  Update it with hours in negatives.
5.  **Save** it.
6.  Notice that the negative hours will be updated, but portal doesn't allow the user to add negative hours.
7.  Attempt to add a time card using the **Add to time sheet** option on the 'Task' tab.
8.  Add negative hours in one of the days.
9.  Notice that it's not allowed.

 Expected behavior: The negative hours are added to the time card.

 Actual behavior: The negative hours is blocked from being added in the time sheet portal.

</td></tr><tr><td>

Transaction Management

 PRB1913194

</td><td>

Unhandled Exceptions in GlideTransactionProcessor may leak HTTPTransaction objects, causing memory issues

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Transaction Management

 PRB1923245

</td><td>

The IllegalMonitor StateException in WaiterCountManager can prevent locked threads from being unlocked and lead to a deadlock

</td><td>

There's a race condition between a new thread pool addition during a specific plugin installation and locking thread-pool queues to claim a transaction for processing. This could cause a potential deadlock.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1827405

</td><td>

A UI16 form loads slowly when the **Composite Name** type field is added and the instance has a lot of metadata

</td><td>

If a form has a **Composite Name** type field on it and there's much metadata present, the form can take upwards of 15-20 seconds to load.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1840516

</td><td>

When using an absolute value for a lifecycle stage, it moves to empty, but it accepts and saves a string value with a 'contains an' operator

</td><td>

On that policy form, the filter is using the **Lifecycle stage** reference field where the dictionary is configured to use 'reference key' = 'name'. The record lookup is done using the **Name** field instead of default **Sys\_id**.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1875982

</td><td>

Now Assist Context Menu \(NACM\) isn't rendered on a few form fields on an INC form

</td><td>

After creating and activating a new skill on an **Incident form** field, the NACM isn't rendered for some fields.

</td><td>

1.  Log in to a Washington DC instance.
2.  Ensure Gen AI is set up.
3.  Navigate to **Now Assist Admin \(NAA\)** &gt; **NACM experiences**.
4.  Create a new skill configuration on the **Incident form** field.
5.  Add **Record form** fields such as **Subcategory**, **Short description**, and **Service**.
6.  Activate the skill.
7.  Open an INC record.

 Observe that the NACM sparkle isn't rendered on the form for the fields **Subcategory** and **Short description**.

</td></tr><tr><td>

UI Form Administration

 PRB1819502

 [KB1900700](https://hi.service-now.com/kb_view.do?sysparm_article=KB1900700)

</td><td>

Adding an **Attachment** field to workspace view gives inconsistent results in platform and workspace

</td><td>

A canvas error in ServiceNow can occur when attempting to perform certain actions, such as activating a decision tree or searching for a record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1920499

</td><td>

The snFormDataConnected \{headerConfig...\} GQL call occurs during the create case flow

</td><td>

When the user creates a case, the snFormDataConnected \{headerConfig...\} call goes out, even though it isn't needed during this flow.

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

</td></tr><tr><td>

UXF Components

 PRB1826745

</td><td>

Highlighting and copying data from related records or any list results in additional help text being copied

</td><td>

In the Service Operations Workspace, when highlighting and copying rows of data from related records or any list, additional help text appears. The copied data includes the message: 'Press and hold Shift then press Enter to edit'.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1918618

</td><td>

Session tabs above the maxCachedPageCount stay in DOM

</td><td>

 

</td><td>

1.  Open the Service Operations Workspace incident records list.
2.  Open at least 7 record tabs.
3.  Select one of the opened tabs.

 Expected behavior: There should be only 6 \(1 active + 5 chrome\_main. maxCachedPageCount\) session tab content in the DOM, the rest of tabs should have their sn-canvas-screen \#shadow-root nodes detached.

 Actual behavior: All 7 tabs are open and all their shadow-root nodes are stored in DOM.

</td></tr><tr><td>

UX Framework

 PRB1925967

</td><td>

Engagement Messenger isn't loading chats after upgrading

</td><td>

The chat box in Engagement Messenger is blank, and loads no content. The errors occurs, 'SecurityError: Failed to read a named property 'uxfIntentLibrary' from 'Window'.

</td><td>

1.  Launch the Engagement Messenger.
2.  Select the chat box.
3.  Observe that the chat box is blank.
4.  Navigate to a Yokohama instance.
5.  Navigate to Agentic Portal in a separate browser tab.
6.  Don't attempt to log in.
7.  Open up the dev console.
8.  Execute the script.
9.  Execute the code.
10. Select the chat bubble that appears after the code finishes executing.

 Expected behavior: The chat loads with content.

 Actual behavior: The chat load is blank and a security error appears in console.

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
3.  Notice that the expression cache is filled due to this.

 Notice that the load of 25 users on a single node for one hour for the search action performed occupies more than 500MB.

</td></tr><tr><td>

Virtual Agent

 PRB1896418

</td><td>

Generative AI Controller \(GAIC\) Timing on for App Generation on XP3 with NAFC NAFC26.4.0

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1910141

</td><td>

Duplicate messages are seen after receiving multiple notifications in NAVA

</td><td>

This issue is observed in the standard chat experience.

</td><td>

1.  Open a conversation in NAVA with the system admin.
2.  Impersonate another user \(Abraham Lincoln\).
3.  Update the HR case: HRC0001023 state multiple times with the Abraham Lincoln user.
4.  This triggers multiple notifications in Virtual Agent.
5.  Impersonate the system admin user.
6.  Navigate to the ESC portal.

 Observe the same message appearing in NAVA after all notifications have been received.

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

Non-LLM time takes an extra 120-581 milliseconds for NAVA use cases and 500-900 milliseconds for NAP Skill/Topic execution

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1920529

</td><td>

Skip define access in guided setup doesn't clone the NACM default ACL

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
2.  In the NAVA chatbot, enter the utterance 'Mi portátil ha sido arruinado por las cookies. ¿Qué son siquiera las cookies? ¿Puedo pedir un portátil nuevo?'

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

 PRB1924015

</td><td>

There's a missing chunk during the AmazonBedrockStream process

</td><td>

There are some missing chunks when the build agent tries to create an app and provides any instructions to the Amazon Bedrock in stream mode. Because of this, the subsequent request fails.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1924923

</td><td>

Slow API queries for NowAssistConversation History\(\).\_getTranscriptFor ConversationHistory API

</td><td>

The first hit to the NowAssistConversationHistory\(\) .\_getTranscriptFor ConversationHistory API can take over 500 milliseconds.

</td><td>

1.  Open an instance.
2.  Navigate to the **ESC portal**.
3.  In the NASS chat, type an utterance like 'Hello!'
4.  Check the system logs for keywords starting with 'NowAssist ConversationHistory: Time taken to retrieve transcripts for conversation history is.'

 For a new conversation, observe that the first hit to this API takes over 500 milliseconds.

</td></tr><tr><td>

Virtual Agent

 PRB1925332

</td><td>

Processing messages APIs are slow

</td><td>

The processing messages APIs take more than 400 milliseconds.

</td><td>

1.  Create a topic.
2.  Add the following statements in it: vaSystem.send Processing MessageDirectly\('testing '\) and vaSystem.updateDynamic ProgressMessage\('COMPLETED'\)./

 Observe that both APIs take more than 400 milliseconds, approximately.

</td></tr><tr><td>

Virtual Agent

 PRB1925496

</td><td>

SQL does a table scan on the sys\_cs\_session\_binding table for auxiliary subscripting, causing high SQL time

</td><td>

Auxiliary is the only subscription timing out, and the SQL processing time is more than 500ms.

</td><td>

Launch Now Assist Virtual Agent \(NAVA\).

 Notice the processing time for the subscription when launching the chat client.

</td></tr><tr><td>

Virtual Agent

 PRB1925600

</td><td>

Users are unable to remove prod bot integration from an instance

</td><td>

 

</td><td>

1.  Connect prod bot to an instance.
2.  Send a few messages in Teams.
3.  Try to remove the Teams integration for prod bot.

 Expected behavior: The integration is removed from an instance.

 Actual behavior: The user gets the error 'failed to remove integration...' and the integration isn't removed.

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

 PRB1926867

</td><td>

The skillParams in a session context isn't persisted

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1927087

</td><td>

Cold starts on Teams/CEA and LA handoffs are running into a fallback error

</td><td>

 

</td><td>

1.  Navigate CEA.
2.  Enter 'hi'.
3.  Enter 'i want to connect to a live agent'.
4.  After getting an LA card, select **Connect to agent** for handoff.

 Expected behavior: The handoff works without any error.

 Actual behavior: After handoff, the user runs into a fallback error.

</td></tr><tr><td>

Virtual Agent

 PRB1927417

</td><td>

Fallback in NAVA returns a technical error

</td><td>

 

</td><td>

1.  Navigate to NAVA.
2.  Send a gibberish message or anything that returns fallback as a user.

 Expected behavior: The user should get a fallback response.

 Actual behavior: The user gets a fallback response and then a technical error.

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

 Notice the profiler stack trace.

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

 Observe that there is a delay in sent time \(get sendTime from 'Serialized cometd message' colun payload in sys\_amb\_message table\) and AMB received time in the web client.

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

 PRB1931987

</td><td>

The **Search** button doesn't show up on DW

</td><td>

On a portal with DW enabled, the **Search** button doesn't appear next to the feedback icons.

</td><td>

1.  Navigate to a portal with DW enabled.
2.  Enter 'What is spam?'

 Expected behavior: The **Search** button appear next to the feedback icons.

 Actual behavior: The **Search** button to show regular results doesn't appear.

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
11. Observe that the evaluation run is not completing.
12. Check the sys\_one\_extend\_batch\_run.

 Observe that the metric result and batch result has completed.

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
3.  Execute the agent

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

Fire a few of parallel LLM calls during the planner invocation

 Notice that when multiple responses arrive approximately at the same time, the response generation never ends up getting fired because each parallel invocation thinks there are steps left.

</td></tr><tr><td>

Virtual Agent

 PRB1933102

</td><td>

Follow up search abruptly ends the conversation

</td><td>

When performing a second search immediately after the first search, the conversation ends but the search continues.

</td><td>

1.  Search for a KB/catalog/topic
2.  Search for another KB/Catalog/topic after getting the response.

 Expected behavior: The user gets a response related to the search from step 2.

 Actual behavior: The conversation ends and then the search continues.

</td></tr><tr><td>

Virtual Agent

 PRB1933142

</td><td>

Language detection isn't being honored

</td><td>

In the sys\_generative\_ai\_log, the Unified Planner capability doesn't honor language detection. Also, in one\_api\_service\_plan \_feature\_invocation, the Unified Planner was not invoked with any of the language flags.

</td><td>

1.  Open an instance with language detection turned on.
2.  Navigate to the SP page.
3.  In chat bot, enter the utterance '¿Qué son las leguminosas?'
4.  Observe that the transition message is in English.
5.  Navigate to sys\_generative\_ai\_log and look at the Unified Planner capability.

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

1.  Navigate to **NAVA**.
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

1.  Navigate to **/esc**.
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
2.  Select the language **Francais \(Canada\)**.
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
4.  Observe that agents are getting discovered and are shown to the user.
5.  Give utterance as 'resolve an incident INC000XXXX'.

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

 PRB1934294

</td><td>

The ticket status agent is not being discovered

</td><td>

The ticket status agent doesn't run; instead, the message 'sorry there was a problem on my side' appears.

</td><td>

1.  Navigate to **/esc**.
2.  Query 'Check IT ticket status'.

 Expected behavior: The ticket status agent runs.

 Actual behavior: The message 'sorry there was a problem on my side' appears.

</td></tr><tr><td>

Virtual Agent

 PRB1934342

</td><td>

Markdown content does not render as a rich text output

</td><td>

The server has a logic to determine the output message type. When the message content contains an HTML tag it's treated as htmloutput.

</td><td>

1.  Create a topic.
2.  Add rich text response node.
3.  Use a string as the rich text content.
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

1.  Navigate to **/esc**.
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
3.  Notice that this shouldn't be in full-page experience.
4.  Enter in the **Input search** field, 'What is the definition of spam?'.
5.  Notice that this should re-direct to the full-page experience.

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

1.  Navigate to **/esc**.
2.  Navigate to **NAVA**.
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

 PRB1935791

</td><td>

A dynamically changing script unnecessarily eats up space in the sys\_expression cache

</td><td>

 

</td><td>

1.  Set up NAVA.
2.  Run a load test for 1 hour \(agent use case\).
3.  Check the heap memory.

 Notice that there's more than 500MB is the expression cache.

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

 Notice the response is displayed twice for the followup question. The GenAI log has double entries for that call as well.

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
8.  After the fallback message is received, it says 'all done! is there anything else i can help you with?'. Reply with 'no thank you'.

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
2.  Navigate to the ESC portal.
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

1.  Navigate to **CEA**.
2.  Search for the topic/catalog 'what is spam' 'i want miro access'.
3.  Start topic/skill.

 Expected behavior: Skills/topics start and execution is completed.

 Actual behavior: Skills and topics are stuck at 'thinking'.

</td></tr><tr><td>

Virtual Agent

 PRB1937597

</td><td>

AIA ResponseGeneration scripts aren't cached

</td><td>

When invoking the following scripts, they're currently invoked as 'dynamic' and hence not cached: 'AIAResponseGenerator', 'AISWebSearch CallbackWrapper', and 'AISPlanner2 ResponseHandler'. They should be invoked as simple scripts and pass the necessary variables to evaluate them so that they're cached properly.

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

The Hybrid queue take up to 500 ms.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1938273

</td><td>

Multi-intent utterances are not working in Now Assist panel \(NAP\)

</td><td>

This issue was observed when using Azure and Gemini. Workflows are available for example both utterances, and individually both utterances are work as expected.

</td><td>

Enter the utterance 'Book a flight and order coffee'

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

1.  Navigate to the **ESC** portal.
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

Virtual Agent

 PRB1941206

</td><td>

Cloned metrics aren't appearing in the list after creation

</td><td>

The metric appears to be created successfully, but the cloned metric doesn't appear up in the list in the home page.

</td><td>

1.  Create a custom metric.
2.  Open the created custom metric.
3.  Select **Copy** on the top right corner to clone the metric.
4.  Select **Finish setup**.
5.  Navigate to the home page.

 Observe that the metric is not available.

</td></tr><tr><td>

Virtual Agent

 PRB1941618

</td><td>

The same workflow is displayed twice in Now Assist panel \(NAP\)

</td><td>

There is only one workflow with the 'Order items' name.

</td><td>

Enter the utterance, 'I want to order below the list of items: Coffee, Laptop, Book a flight, Pizza'.

 Notice that the coffee agent is completed and the same workflow is displayed twice.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1896390

</td><td>

Console errors for va\_web\_client API failures are displayed when launching a chat in the CSM portal and Engagement Messenger

</td><td>

Two console errors related to va\_web\_client are observed: '/api/now/ va\_web\_client\_settings /get\_va\_web\_ client\_settings' api results 403 error' and '\[SNAnalytics\] Invalid property name'. Console errors shouldn't be displayed and chat functionality should work as expected.

</td><td>

1.  Log in to an instance.
2.  Navigate to **CSM portal** or **Engagement Messenger**.
3.  Launch Virtual Agent chat/start a chat.

 Observe that the browser console displays errors.

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

 PRB1927881

</td><td>

Virtual Agent topic options for dynamic choice input aren't displayed in Now Assist Portal \(NAP\)

</td><td>

For dynamic choice input, the options aren't appearing for the first time on NAP. If users enter a random string that isn't one of the expected options, it repeats the question and then displays the options on the second or third attempt.

</td><td>

 

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

 PRB1933741

</td><td>

Stacked messages appear during websearch

</td><td>

 

</td><td>

1.  Navigate to **/esc**.
2.  Enable websearch by selecting the **Globe** icon.
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
2.  Notice that the space between 'Hello' and the sparkle icon should be 12px, and is currently 24px in both NAVA, DW and NAP.
3.  Notice the space between 'Let me look up for information'.
4.  Hover the copy icon to next Sparkle icon.
5.  Notice that it should be 12px, has a 4px margin in DW and NAP.
6.  Select **Show Sources**.

 Notice that the space between the Synthesized results and the links should be 8px, and that it's 4px in DW and NAP.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1941773

</td><td>

Portal page shifts occasionally when **Ask a follow-up** is selected

</td><td>

The portal page shifts to the left then returns back to its original place when the user dismisses the pop-up.

</td><td>

1.  Ensure Dispatcher Workspace \(DW\) is enabled for Service Portal \(SP\) from the 'Assistants page'
2.  Navigate to **SP portal**.
3.  Enter **What is spam** in portal search.
4.  Select **Ask for follow up** once the Results page displays.

 Notice that DW opens with the pop-up 'Your previous chat was saved' and the portal page shifts to the left, but when the user when the user dismisses the **Your previous chat was saved** button, the page returns to its original place.

</td></tr><tr><td>

Work Order Management

 PRB1929109

</td><td>

Upon page reload, the value in the **decimal input** field disappears

</td><td>

 

</td><td>

1.  Open Work Order Template.
2.  Input any value in the **Enter decimal value** field.
3.  **Save** it.
4.  Reload the page.

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

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama Patch 7 Hotfix 3](yokohama-patch-7-hf-3-PO.md)
-   [Yokohama Patch 7 Hotfix 2](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2524621)
-   [Yokohama Patch 7 Hotfix 1](yokohama-patch-7-hf-1-PO.md)
-   [Yokohama Patch 7](yokohama-patch-7.md)
-   [Yokohama Patch 6](yokohama-patch-6.md)
-   [Yokohama Patch 5](yokohama-patch-5.md)
-   [Yokohama Patch 4](yokohama-patch-4.md)
-   [Yokohama Patch 3](yokohama-patch-3.md)
-   [Yokohama Patch 2](yokohama-patch-2.md)
-   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


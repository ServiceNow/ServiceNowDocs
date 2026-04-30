---
title: Yokohama Patch 1
description: The Yokohama Patch 1 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-03-12"
reading_time_minutes: 93
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 1

The Yokohama Patch 1 release contains important problem fixes.

-   **Yokohama Patch 1 was released on March 12, 2025.**
    -   Build date: 03-05-2025\_2133
    -   Build tag: glide-yokohama-12-18-2024\_\_patch1-02-21-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y01.00.xlsx).

## Overview

Yokohama Patch 1 includes 289 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp1.png "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 1 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 1, refer to [KB1953930](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1953930).

## Changes in Yokohama Patch 1

-   **[Testing LLM topics](https://www.servicenow.com/docs/access?context=test-llm-topics&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Under the skills search results,a **Matching** badge appears next to the skill discovered, whilevariables and values may also be listed \(such as the variable **@laptop\_make** and the value **macbook**\), depending on the topic


-   **[Topic Flow tab](https://www.servicenow.com/docs/access?context=vad-topic-flow-tab&version=yokohama&pubname=yokohama-conversational-interfaces&ft:locale=en-US)**

    Various updates, including:

    -       -       -   
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

AI Search

 PRB1825963

 [KB1763961](https://hi.service-now.com/kb_view.do?sysparm_article=KB1763961)

</td><td>

Index KBB throws an exception about journal peekahead

</td><td>

An error is thrown: 'IngestService: Unable to index Glide Record \[9b85baaa3bf11a10c 4589c8c24e45a2b\] u\_kb\_template\_topic\_category. fa8191f6fb059e 507863f46b5eefdc1d : Cannot invoke "java.util.Map.get\(Object\)" because "journalElementToValuesMap" is null java.lang.NullPointerException: Cannot invoke "java.util.Map.get\(Object\)" because "journalElementToValuesMap" is null...'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1847092

</td><td>

A part of the query on sys \_generative \_ai \_config has been ignored because of insufficient access for 'query\_match operation on sys\_generative\_ai\_config definition

</td><td>

Results in warning message pop-ups.

</td><td>

 

</td></tr><tr><td>

Approvals

 PRB1845668

 [KB1810362](https://hi.service-now.com/kb_view.do?sysparm_article=KB1810362)

</td><td>

Multi-Level approval skips steps due to race conditions

</td><td>

Overlapping transactions on the sc\_req\_item table cause race conditions allowing approval steps to be skipped.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1402594

 [KB0956006](https://hi.service-now.com/kb_view.do?sysparm_article=KB0956006)

</td><td>

Unable to edit a field in the list view when it is dependent on another field that is read-only for the user

</td><td>

This issue has been observed since New York. Users are not able to edit a field on list view when it is dependent on another field that is read-only or has an ACL making it read-only.

</td><td>

1.  Open any incident record.
2.  Set the field **Contact type** in the dictionary definition to be dependent on 'Configuration Item.Asset', which is read-only by default.

 Expected behavior: The field should not be editable only when there is a list\_view ACL preventing the field from being edited.

 Actual behavior: In the form view, the field **Contact type** is editable, but in the list view it is not.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1760775

</td><td>

There's an issue with reports on a workspace dashboard

</td><td>

Legends display duplicate values when translated into non-English language.

</td><td>

1.  Provision an instance with the 'Install Platform Analytics workspace' plugin installed.
2.  Create a Platform Analytics dashboard with a column report with 2 data sources.
3.  Change the language to Brazilian Portuguese.

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

 PRB1850716

</td><td>

There should be a check for customization before the removal of the snc\_internal ACL role from a set of ACLs

</td><td>

If a snc\_internal acl role record has an entry in the sys\_update\_xml table, then the record shouldn't be deleted.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1834293

</td><td>

Activity stream activity events with empty **event\_created\_by** field values cause the activity stream screen on mobile to crash

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1835318

</td><td>

'Fit-to-parent' for emails doesn't work as expected

</td><td>

Observe that the email compose text area does not expand as expected because the 'fitToParent' property already exists as an option on the composer.

</td><td>

1.  Log in to the instance.
2.  Navigate to CSM workspace.
3.  Select any incident record.
4.  Navigate to the Activity Stream settings and toggle the 'Side by Side' view.
5.  Select the 'Email' tab.

 Observe that the email compose text area does not expand as expected.

</td></tr><tr><td>

Activity Stream

 PRB1837845

</td><td>

A **File Attachment** type field isn't added in the activity log in Workspace

</td><td>

A **File Attachment** type field isn't added in the activity log in Workspace when attaching from a field. It's a ZZ\_YY prefix problem.

</td><td>

1.  Create a **New file attachment** type field for some record type.
2.  Ensure that the field is visible in some view.
3.  Attach an image to an existing record via the **New file attachment** field.
4.  View the activity stream for the existing record in any workspace.

 Expected behavior: The image appears in the workspace activity stream.

 Actual behavior: The image doesn't appear in the workspace activity stream.

</td></tr><tr><td>

Activity Stream

 PRB1843408

</td><td>

If a user deletes drafts after sending mail, the last sent email disappears in the filtered 'Activity Stream' section

</td><td>

 

</td><td>

1.  Open an email page record.
2.  Select the 'Email' tab.
3.  Compose an email with valid recipients.
4.  Select the **Send** button.
5.  Once the email history is updated, select the 'Email drafts' icon and delete all drafts.
6.  Close the dialog/modal.

 Expected behavior: Sent email logs should be displayed on the email's history.

 Actual behavior: The last sent email has disappeared from the email's history.

</td></tr><tr><td>

Activity Stream

 PRB1843720

</td><td>

The activity log captures changes but aren't displaying them as the newest entry in Workspace

</td><td>

For a field with name and label of length more than 40 characters, any changes made to the field aren't reflected in the activity stream as a new entry.

</td><td>

1.  Create a new field name and label of length of more than 40 characters.
2.  Add the newly created field in the Service Operations Workspace \(SOW\) view and configure the activity stream filter to display that field in SOW.
3.  Open SOW.
4.  Try updating the value in the field.
5.  **Save**.

 Expected Behavior: The field change should be added as a entry in activity stream.

 Actual Behavior: The change doesn't reflect in the workspace activity stream but reflects in the UI16 activity stream. Instead, the field change appears to overwrite the first initial field change record. If users follow the steps with a field name and label of less than 40 characters, the change would reflect in both workspace and UI16 activity stream.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1857820

</td><td>

Agent Outside Workspaces that use OpenFrame soft phone are set to an 'Offline' presence state within a minute after the agent moves to an available state

</td><td>

If an agent isn't also on a workspace, the presence reverts to 'Offline' within about a minute. Since the agent is using OpenFrame to manage capacity, it shouldn't automatically revert to 'Offline'. The issue occurs after an Xanadu upgrade.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1846351

</td><td>

Audio notifications don't play intermittently when the browser has 'Allow All Auto-Play' configured

</td><td>

On a Safari browser, when the user doesn't allow the Auto-Play for ServiceNow site, audio notifications intermittently don't play for an agent. This is applicable for inbox and conversation notifications. For example, if an agent doesn't hear an audio notification for an incoming inbox notification, it's possible the following conversation's audio alert to play or not play. Once audio notifications begin to play, proceeding audio notifications usually play. The audio state can be 'interrupted'.

</td><td>

1.  In a Safari browser, as an agent, open Service Operations Workspace.
2.  Change the status to 'Available'.
3.  Using a Chrome browser, impersonate a requester.
4.  Turn off audio notifications in the web client.
5.  Initiate a chat and attempt to connect to a live agent.
6.  In the Safari browser, as an agent, accept the incoming work item.

The audio notification plays.

7.  From the Chrome browser, as a requester, send a message to ensure an audio notification plays on the agent's side.
8.  In the same Safari browser, as an agent, open a new tab with a random URL. Keep this as the active tab and workspace tab in background.
9.  In Chrome, as the requester, wait for the timeout reminder and observe if the audio notification plays.
10. In Chrome, as the requester, send a message.

Observe at this time, the audio notification stopped working, even though the console log says it successfully played audio.


</td></tr><tr><td>

Agile Development

 PRB1845010

</td><td>

Add the spm\_agile\_common\_user role to the plannedtask.\* ACL to view a rm\_story form

</td><td>

A spm\_agile\_common\_user should be able to have CURD access on the rm\_story table.

</td><td>

 

</td></tr><tr><td>

AI Search for Virtual Agent

 PRB1855428

</td><td>

Synthesized answer responses intermittently fail with error 400001

</td><td>

The flow engine log shows the entry 'Cancelling flow due to timeout' and the error in the flow execution says 'Prompt generation failed'.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1827624

</td><td>

A search doesn't return any results

</td><td>

After configuring the search profiles and the user, the search results don't appear, but if the **location.state** field is changed for the user, search results appear.

</td><td>

1.  Download and import the search profiles.
2.  Ensure the search profiles were uploaded.
3.  Find the 'Location boost' risk intelligence report.
4.  Select the 'Location boost' risk intelligence report.
5.  Navigate to **positive**.
6.  Change the match field from **location.city** to **location.state**.
7.  Publish the profile.
8.  Set up a user.
9.  Assign the user the knowledge\_admin and ITIL roles.
10. Ensure the values in the **Company** field are empty.
11. Change the **location** field to 'California'.
12. Select **Save**.
13. Select the value 'California'.
14. Ensure that the column 'state' is 'California'.
15. Ensure that the 'name' is 'California'.
16. Run this query 'Employee benefits?' on Global, Service Portal, and Now Assist Virtual Agent.
17. Navigate to 'sys\_generative\_ai\_log.list'.
18. Check the response.

 Expected behavior: The Knowledge Base article, 'Employee Benefit - US' should be at the top.

 Actual behavior: The search results don't appear, but if the user changes the **location.state** field, the Knowledge Base article appears.

</td></tr><tr><td>

AI Search

 PRB1832851

</td><td>

There's no hover over for a Q&amp;A source citation

</td><td>

 

</td><td>

1.  Get a Q&amp;A result.
2.  Hover over the source citation.

 There's no hover over of the source title.

</td></tr><tr><td>

AI Search

 PRB1835340

</td><td>

sys\_updated\_on for ais\_datasource isn't updated upon changes in Advanced Configuration, Field Configuration and Semantic Index Configurations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1838451

</td><td>

AisJournalFieldPeekAhead throws NullPointerException \(NPE\)

</td><td>

Leaving the value empty when adding a journal value column to kb\_knowledge throws an NPE.

</td><td>

1.  Add a journal value column to kb\_knowledge.
2.  Leave the value empty.
3.  Attempt to ingest the document.

 Observe the NPE.

</td></tr><tr><td>

AI Search

 PRB1843005

</td><td>

The text '\(number\) results for \(keyword\)' text is not translated when using AI Search

</td><td>

After installing a language plugin and switching the language to a non-English language, the text '\(number\) results for \(keyword\)' is not translated when using AI Search. This occurs when a keyword is misspelled when using AI Search.

</td><td>

1.  Install any language plugin.
2.  Install AI Search.
3.  Log in to the instance.
4.  Switch the language to non-English.
5.  Open an Employee Service Center portal.
6.  Search for any misspelled keyword.

 Expected behavior: The text '\(number\) results for \(keyword\)' text is translated to the non-English language.

 Actual behavior: The text '\(number\) results for \(keyword\)' text is seen in English and is not translated.

</td></tr><tr><td>

AI Search

 PRB1843571

</td><td>

AI Search's NLQ Genius result 'None of the above' option doesn't work as expected

</td><td>

 

</td><td>

1.  Enable the NLQ Genius result for a search application.
2.  Search for an utterance that contains multiple table names.
3.  Select **None of the above** in one of the menus of the Genius result card.

 Observe that there's no result in the table. The NLQ query didn't properly remove the table which had **None of the above** selected for it. An error shouldn't display.

</td></tr><tr><td>

AI Search

 PRB1850631

 [KB1949808](https://hi.service-now.com/kb_view.do?sysparm_article=KB1949808)

</td><td>

The table field for EVAM view configuration matching of a search record is always the parent table

</td><td>

With the new EVAM-lite implementation, there are 3 gaps in the logic for determining which view configuration to use for a given search result. 1. If a view configuration has a condition based on a field that isn't included in the list of table fields, that field won't be returned from AIS, and so the condition never matches. Even if the field is included on the 'Table Fields' list, if it's a field that only exists on a child table of the table the indexed source is based on, the field won't be returned from AIS and so the condition never matches. If the first view configuration for a particular table comes after the default/global view config, it is never used. Whereas, EVAM had a more nuanced selection process that would look for all view configuration that matched on the table before falling back to those for ancestor tables or the global/default table.

</td><td>

1.  Set the system property glide.search.evam.logger.enabled to true.
2.  Open the Service Portal and search for 'new hire'.
3.  Open the syslog.
4.  Filter on 'Created'.
5.  Notice there's a message that contains: '\[SEARCH EVAM\] SearchResultTemplateGenerator: Using View Config 633c3b5d53a710 10968addeeff7b1218 for Result with table sc\_cat\_item and sys\_id 6690750f4f7b 4200086eeed18110c761'.

 Expected behavior: Service Portal's EVAM Def'n has a view configuration called 'Catalog Search Results - Order Guides', which has a condition of 'sys\_class\_name = sc\_cat\_item\_guide^EQ'. This is the view configuration that should be used, and the syslog entry should contain: '\[SEARCH EVAM\] SearchResultTemplateGenerator: Using View Config 44c37371c3202010 825039b06e40dd4b for Result with table sc\_cat\_item and sys\_id 6690750f4f7b 4200086eeed18110c761'.

 Actual behavior: The incorrect view config is being used. 633c3b5d53a710 10968addeeff7b1218 is the sys\_id of the view configuration called 'Catalog Search Results', which is the generic view configuration for catalog items, and doesn't have any conditions beyond table. But the 'New Hire' category item is an 'Order Guide', and there's an EVAM view configuration specifically for that.

</td></tr><tr><td>

AI Search

 PRB1852129

</td><td>

Selecting a search result in the Portal adds the parameter 'SearchTerm', leading to a 404 error

</td><td>

With AI Search enabled, searches in the Portal lead to a '404 page not found' error. This occurs when search results that are external links are presented in the search results. When a search result is selected, an additional parameter is added to the URL '&amp;searchTerm=', which causes the 404 error.

</td><td>

1.  Navigate to a Xanadu instance.
2.  Add an external link to the AI Search source.
3.  Navigate to the Employee Portal.
4.  Search for the external link.
5.  Select the top search result.
6.  Observe that 'searchTerm=' is added to the URL.

 Expected behavior: The user lands on the external link after selecting the search result.

 Actual behavior: The user lands on an page with the error message '404 Page not found'.

</td></tr><tr><td>

AI Search

 PRB1852402

 [KB1909618](https://hi.service-now.com/kb_view.do?sysparm_article=KB1909618)

</td><td>

SearchAnalyticsService. pruneSearchSignalEvents occasionally purges events with the wrong application ID

</td><td>

The sysauto\_script scheduled job, 'Prune Search Signal Events', may cause sys\_search\_events and its related tables to be incorrectly pruned.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1857237

</td><td>

Images aren't returned for Now Assist actions on Service Portal

</td><td>

 

</td><td>

1.  On a Yokohama instance with Now Assist for search 10.0.14, navigate to Service Portal.
2.  Search for 'Apple' or 'Laptop'.

 Expected behavior: Images should be returned for the Now Assist actions Genius Results.

 Actual behavior: Notice that the images aren't coming back for Genius Results.

</td></tr><tr><td>

Analytics Data API

 PRB1834167

</td><td>

Slow indicator based PA widgets

</td><td>

 

</td><td>

1.  Navigate to the SaaS Overview page of SAM workspace.
2.  Monitor network calls and slow patterns and leverage WPT for further analysis.

 Notice stale subscriptions by instance.

</td></tr><tr><td>

Analytics Export API

 PRB1842896

</td><td>

The legends of visualizations are too small and null text appears for the heading and description

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Antivirus Scanning

 PRB1835660

</td><td>

The antivirus job updates all columns instead of only the 'State' column

</td><td>

The antivirus job updates all columns in some scenarios. It should only update the state column when attachment.setState\(advice\) is called. However a forceUpdate is occurs, which ultimately updates the entire row, including the state data. Additionally, when the old table name and table sys\_id are updated, the attached file is moved to the previous table.

</td><td>

1.  Log in to a Washington DC instance.
2.  Navigate to **All** &gt; **Self service** &gt; **Service catalog**
3.  Select &gt; **Mobiles** &gt; **Add to cart**
4.  Upload a 10MB file.
5.  Select **Order nowb**
6.  Navigate to sys\_attachment.list.

 Expected behavior: The table name should be sc\_req\_item on the available 'State'.

 Actual behavior: The antivirus job updates all columns instead of only the 'State' column.

</td></tr><tr><td>

Application Install Engine

 PRB1836818

</td><td>

A parent application installs successfully despite missing dependencies

</td><td>

A parent application \(for example, Generative AI Controller 9.0.1-Snapshot\) is installed successfully even though its dependencies \(for example, Microsoft Azure AI Speech Spoke\) were not installed during the process

</td><td>

1.  Attempt to install a parent application with known dependencies.
2.  Simulate a scenario where the dependency \(for example, Microsoft Azure AI Speech Spoke\) fails to install.

 Observe that the parent application still installs, creating a record in the sys\_store\_app table, but dependencies remain missing.

</td></tr><tr><td>

Attachments to Records

 PRB1849752

 [KB1885864](https://hi.service-now.com/kb_view.do?sysparm_article=KB1885864)

</td><td>

There's an issue with archive table clean-up using the 'PurgeOrphanAttachments' job

</td><td>

There's an issue that may result in the unintentional removal of records from the sys\_attachment table under specific conditions. The issue may impact instances on Washington DC and later releases.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1852376

</td><td>

The user observes an error banner when a test is generated

</td><td>

An error is posted in a banner reading: 'Not allowing update of property: glide.lastplugin.'

</td><td>

1.  Log in to an instance as a user with the now.assist.creator and atf\_test\_admin roles.
2.  2. Navigate to **ATF** &gt; **Steps** &gt; **Create with Now Assist**.
3.  3. Enter a prompt and select **Generate Test Preview**
4.  Check page after preview is loaded.

 An error is posted in a banner reading: 'Not allowing update of property: glide.lastplugin.'

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1827858

</td><td>

Ship RCA for a KB search in the target scope

</td><td>

 

</td><td>

1.  Set up Now Assist for HR.
2.  Enter a query in Virtual Agent: 'Tell me about parental leave policy' or any other KB related query.

 Expected behavior: The numbers should be visible and clickable.

 Actual behavior: The numbers aren't displayed in the KB result.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1842923

</td><td>

An RCA is generated when a contact is added on the My Profile page in ESC portal

</td><td>

An RCA error is shown and no details are displayed on page.

</td><td>

1.  Log in as admin and navigate to ESC portal.
2.  Select the Avatar icon and select a profile.

The HR contact widget is displayed.

3.  Select **Add contact** and enter the details.
4.  Save.

 Observation that although a record is created, an RCA error is shown and no details are displayed on page.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1844302

</td><td>

Ad hoc tasks generated from a flow aren't supported in the playbook on HR Agent Workspace

</td><td>

 

</td><td>

1.  Create a test LE event.
2.  Add several activity sets to it.
3.  Create a subflow in Flow Designer.
4.  Create activities in all of the activity sets of as many different activity types.
5.  For flow activities, make sure to define 'Activity Field Mappings'.
6.  Tie the LE event to HR service.
7.  Create a case of that HR service.

 Notice that LE activities can't be closed and closing all activities in an activity set triggers the next activity set \(if it is a dependent activity set\).

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1850236

</td><td>

RCA issues with tuition reimbursement AI agents

</td><td>

There are RCA records that are needed in app-hr to let tuition reimbursement request AI agents to function.

</td><td>

Scenario 1:

 1.  Test the query: SELECT customer\_contact0.\`sys\_id\` FROM \(customer\_contact customer\_contact0 INNER JOIN sys\_user sys\_user0 ON customer\_contact0.\`sys\_id\` = sys\_user0.\`sys\_id\` \) WHERE \(sys\_user0.\`home\_phone\` = 'ani' OR sys\_user0.\`mobile\_phone\` = 'ani' OR sys\_user0.\`phone\` = 'ani'\)
2.  Notice that the query response time is approximately 5.5 seconds.

 Scenario 2:

 1.  Test the query: SELECT sys\_user0.\`sys\_id\` FROM sys\_user sys\_user0 WHERE \(sys\_user0.\`home\_phone\` = 'ani' OR sys\_user0.\`mobile\_phone\` = 'ani' OR sys\_user0.\`phone\` = 'ani'\)
2.  Notice that the query response time is approximately 3 seconds.

 Scenario 3:

 1.  Test the query: SELECT csm\_consumer0.\`sys\_id\` FROM csm\_consumer csm\_consumer0 WHERE \(csm\_consumer0.\`business\_phone\` = 'ani' OR csm\_consumer0.\`home\_phone\` = 'ani' OR csm\_consumer0.\`mobile\_phone\` = 'ani'\)
2.  Notice that the query response time is approximately 1 second.

</td></tr><tr><td>

Case Card Component for HRSD Agent Workspace

 PRB1828093

</td><td>

Tooltips aren't working

</td><td>

After upgrading to Xanadu, the tooltips stopped working on all the workspaces.

</td><td>

1.  Access any Xanadu instance that was upgraded from Utah or Washington DC.
2.  Navigate to sys\_ux\_lib\_asset\_list.
3.  Observe if the instance has the file sys\_ux\_lib\_asset\_ 4eca5b08258a2192 915e9d083b0bf32e.xml.
4.  Open any workspace.
5.  Observe that there's no tooltip.
6.  Remove the file mentioned on step 3.
7.  Observe that the tooltips are working.

</td></tr><tr><td>

Case Management

 PRB1854268

</td><td>

Slow queries on Voice Interaction Creation for Consumer Discovery Flow

</td><td>

Queries are taking almost 10 seconds when testing Voice Interaction Creation.

</td><td>

 

</td></tr><tr><td>

Communities

 PRB1843991

</td><td>

Date pickers are not loading in communities

</td><td>

Changes to support the yyyy-MM-dd date format is not supported in portal.

</td><td>

1.  Log in to an instance as an admin user.
2.  Open a community.
3.  Create an event.
4.  Select dates from the date picker.

 Expected behavior: The date picker functionality should work without issues.

 Actual behavior: The date picker is not working.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1838429

</td><td>

The Configuration Management Database \(CMDB\) cleanup job deletes valid records from sys\_object\_source while cleaning up invalid records in the table

</td><td>

The CMDB cleanup job deletes all rows from sys\_object\_source, both valid and invalid, instead of deleting only invalid records.

</td><td>

1.  Create multiple CIs with respective SysObjectSourceInfo.
2.  Duplicate where needed based on the data setup.
3.  Run the script to make target\_table.
4.  Run the sysauto\_script job: CMDB Sys Object Source Cleanup.

 Expected behavior: Only some rows are deleted.

 Actual behavior: All rows get deleted at each run of the clean up job.

</td></tr><tr><td>

Content Analytics

 PRB1837889

 [KB1899731](https://hi.service-now.com/kb_view.do?sysparm_article=KB1899731)

</td><td>

Content Analytics daily processing job evaluates all non-campaign data

</td><td>

Only recently added records should be updated, however all records in the sn\_cd\_analytics\_stat table were updated after several days.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Content Experiences

 PRB1846722

</td><td>

Software Composition Analysis \(SCA\) form doesn't save after 'Use a content template' is unchecked

</td><td>

Publish plans generated by the Content Template should be generated even again after being deleted and unchecking 'Use a content template'.

</td><td>

1.  Install the latest Content Publishing.
2.  Navigate to **Create New** &gt; **Articles &amp; Pages** &gt; **Company Event**.
3.  Complete the required fields.
4.  Select **Save and Continue**.
5.  Enter in the default schedule.
6.  Select **Save Availability**.
7.  Select **Activate Generated Plans**.
8.  Delete the publish plans generated by the Content Template in the Publish tab.
9.  Select the **Design** tab.
10. Uncheck 'Use a content template'.
    1.  Re-enable it.
    2.  Select **Save in the modal \(Change templates modal\)**.
    3.  Select **Save and Continue**.

 Expected behavior: The Content Template publish plans should be generated again when the user wants to use the same plan after deleting it without needing to switch to another content template.

 Actual behavior: Content Template publish plans are not generated.

</td></tr><tr><td>

Content Publishing

 PRB1831890

</td><td>

The publish plan is missing for audience groups other than active users in the content record view

</td><td>

The publish plan for the 'Active users' audience group shows up in the related list, when it should display all publish plans associated with the content.

</td><td>

 

</td></tr><tr><td>

Content Publishing

 PRB1833603

</td><td>

A category from a new content template doesn't appear in a list in the design panel

</td><td>

The category from content template doesn't appear in the list, but it appears in the SCA preview.

</td><td>

1.  Add a category to the news content template.
2.  Create news content with the above content template.

 Expected behavior: All categories are displayed in the design panel list.

 Actual behavior: The category from content template doesn't appear in the list, but it appears in the SCA preview.

</td></tr><tr><td>

Content Publishing

 PRB1837860

</td><td>

The Event Calendar widget 'Holiday Calendar' isn't generating the correct .ICS file

</td><td>

Users are unable to import all events from that .ICS file into Mac Calendar or MS Outlook.

</td><td>

1.  This issue can be reproduced using either Mac Calendar or MS Outlook. Using Mac Calendar:
2.  Navigate to /esc?id=esc\_dashboard.
3.  Find the Holiday Calendar.
4.  Select **Add all to Calendar**.
5.  Double click on the downloaded .ICS file.
6.  Open the file by double-clicking it.
7.  When adding a new event, select **New Calendar...**.
8.  Select **OK**.
9.  Verify that a new calendar named 'Holidays\_2025' has been added to the Mac Calendar.
10. Browse through the months and observe that only one entry is present, while all other entries are missing.

 Expected behavior: The import for all events should work in the calendar.

 Actual behavior: Users can't import all events into the calendar. It only imports the first entry.

</td></tr><tr><td>

Customer Service Management

 PRB1838688

</td><td>

The Agent email address is displayed to the customer in the history instead of the distribution list when an agent replies

</td><td>

The Agent email address is displayed to the customer in the Activity Stream Observation instead of the distribution list

</td><td>

1.  Log in as an agent.
2.  Navigate to any case or email interaction record.
3.  Send an email from workspace.
4.  Select **Reply** or **Reply All** from the Activity Stream Observation once a customer replies.

 Notice that the Agent email address is displayed to the customer when an agent replies in the history.

</td></tr><tr><td>

Customer Service Management

 PRB1855041

</td><td>

Unable to create an email draft in an application scope

</td><td>

The sys\_email\_draft table has table-level access limitation. Only 'Can Read' is allowed in the application scope.

</td><td>

1.  **AI Agent** &gt; **Testing**.
2.  Select the AI agent 'CSM Response Handler'.
3.  Enter the task detail as:
    1.  record\_table = 'sn\_customerservice\_case'
    2.  record\_sysid = '5078cc9a2be71210f980f0aef291bf0b'
    3.  email\_reply\_content = 'We can't complete this case until missing fields and missing documents are added'

 Observe the email response tool 'Draft Email' returns an error message 'Email draft is failed created'.

</td></tr><tr><td>

Data Archiving

 PRB1826830

</td><td>

Rearchiver runs for few days due to incorrect query logic when the archive rule has an 'OR' condition

</td><td>

Re-archiver can run for over 4 days without completion. In the localhost log, there can be a long query result set, such as 1409626 rows.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1840224

</td><td>

Upgrading an instance with many sys\_user records results in significant unresponsiveness

</td><td>

RecordHierarchyPathComputation makes a database call to fetch data for 100 users from the sys\_user table. Because this table contains around 10 milllion records, this could slow down performance significantly.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1842119

</td><td>

The ViewWhereClausePostgresSanitizer method isn't handling NOT LIKE correctly

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1842672

</td><td>

After renaming columns of a staging table to under 63 bytes for applicable ones, the staging table has syntax errors when accessing the list view

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1855418

</td><td>

Check enabled property before listening to source record changes

</td><td>

Java code should check for glide.db.record\_ hierarchy.hierarchical \_record\_support.enabled property. If disabled, no events should be created when the manager value changes on sys\_user.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1808866

</td><td>

Inefficient chunk production for a document ID type reference

</td><td>

For a document ID type reference, the 'Unreferenced Record Cleaner' producer first computes the list of unique table names and then produces the chunks. The SQL query to compute the list of unique table names can timeout leading to no chunks being produced.

</td><td>

1.  Create a large table with a document ID type reference.
2.  Have a large number of unique table names in the table name field.
3.  Set the SQL timeout \(sysrule\_quota\) to a small value.

 Observe that 'Unreferenced Record Cleaner' producer times out computing the list of unique table names, thus producing no chunks.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1820795

</td><td>

DMJob allows the restarting of timed out DM runs

</td><td>

This issue was seen in an unreferenced record cleaner cleanup. Runs are left in a 'processing' state.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1827006

</td><td>

An invalid GlideLogLogger query detected

</td><td>

This invalid GlideLogLogger query detected was detected in Yokohama.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1840970

</td><td>

Monthly/Yearly scheduled jobs named 'Physical Table Stats Aggregator/Gatherer' causes slow CPU and instance responses

</td><td>

This problem manifested primarily on demo instances that have more than 300 DBIs, but it isn't necessarily isolated to demo hosts.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1845280

</td><td>

Users see a null point error when turning on archive debugging

</td><td>

The error caused archive reparenting process to fail and the state to be in 'error'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1807483

</td><td>

Track the number of total/dropped messages per SqlType

</td><td>

Currently, the number of dropped messages is already being tracked and the stats are exposed in xmlstats. When a capture is run, one can hit the xmlstats to get the state/health of the capture, which includes the number of dropped messages. However, the dropped messages are not tracked per SqlType, which makes it impossible to know the percentage of the dropped messages.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1834412

</td><td>

Make JDBC driver properties load dynamically from the DB so nodes don't need to be bounced

</td><td>

This property currently requires updating file properties and bouncing of nodes, which is hard on instances.

</td><td>

Update the sys\_properties table with glide.db.postgresql. jdbc.largeResult SetProtectionMethod = disk.

 Observe JDBC driver still uses stream mode.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1834816

</td><td>

Send txn-level SQL execution time in micros

</td><td>

Currently, TransactionMessage.sql\_time is being sent to indicate the total SQL time for the transaction. The value comes from Transaction\#getSQLTime and the unit is in milliseconds. The total transaction-level SQL time should be measured and sent in microseconds.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1841215

</td><td>

Restrict primary key-ordering injection for Postgres only

</td><td>

Primary key ordering was dynamically added for certain kinds of queries \(i.e., REST/BATCH\_REST, non-referred, non-interactive queries with windowing\). The change could adversely impact query performance for MySQL.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1849730

 [KB1901158](https://hi.service-now.com/kb_view.do?sysparm_article=KB1901158)

</td><td>

Oracle prepared statements leaked for sys\_attachment\_doc queries

</td><td>

When running Glide with an Oracle database, when loading an attachment, a PreparedStatement leaks. This leak eventually cleans up when its database connection is recycled. However, if enough attachments are loaded before the connection is recycled, an OutOfMemoryError can occur, resulting in the application node restarting.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1844781

</td><td>

Raise max limit of characters for Data Privacy APIs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Decision Table Builder

 PRB1849431

</td><td>

The filter list shows SysIDs for Incident reference types

</td><td>

Te sys\_id is shown instead of the number.

</td><td>

1.  Add a reference type input and select the Incident/task or problem \(any table with display value as number\).
2.  Try to apply filter and select value.

 Notice that the sys\_id is shown instead of the number.

</td></tr><tr><td>

Decision Table Builder

 PRB1849433

</td><td>

Referencing sys\_choice table in DT causes the sys\_choices to be deleted

</td><td>

Publishing a decision table causes deletion in sys\_choice table.​

</td><td>

 

</td></tr><tr><td>

Declarative Actions

 PRB1839321

</td><td>

Customize flow on the 'Order' line item loads a blank screen for Order Agent/Order Admin users

</td><td>

When selecting the Customize flow action on a newly created 'Order' line item for a given Order, the page fails to load.

</td><td>

 

</td></tr><tr><td>

Declarative Actions

 PRB1843195

</td><td>

Field decorators for 'Search for Records' and 'Open Records' do not work

</td><td>

The icons are visible but no action occurs when selected.

</td><td>

1.  Create a user with role sn\_esg.data\_owner.
2.  Navigate ESG workspace.
3.  Select **List view** &gt; **Manual metric definition list**
4.  Create a MD and add a data owner.
5.  Add entities from the related lists.

This auto-generates the metrics.

6.  Refresh the record page and select **Execute**.
7.  Log in as Data owner.
8.  In ESG workspace, select **Metric tasks** on the breadcrumb.

This shows the data task.

9.  Select the cell under the entity column to open the side panel.

 Expected behavior: The **i** icon and search icons are not visible.

 Actual behavior: The icons are visible and no action occurs when selected.

</td></tr><tr><td>

DevOps \(Family\)

 PRB1839002

</td><td>

A DevOps event isn't honoring load checks on the sys\_flow\_context table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1837810

</td><td>

vCenter Discovery doesn't go through IRE

</td><td>

As vCenter discover doesn't go through IRE, users can't leverage reconciliation rules. The actual source for a correlation ID is a third party integration. However, Discovery is overriding this field after integration updates the correlation ID. If not planning for IRE rules on vCenter Discovery, there should be configurable functionality to skip some fields.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1843022

</td><td>

Simple Network Management Protocol \(SNMP\) GetTable commands during pattern execution no longer exit the pattern when errors occur that exceed the limit

</td><td>

SNMP GetTable commands no longer exit pattern when errors occur that exceed the limit, and the failure count continues to increase.

</td><td>

1.  Setup a Discovery.
2.  Run a Discovery against an SNMP device that will return errors running 'getTable' requests.

Ensure this sets the MID properties 'mid.sa.snmp.allowable\_f ailures\_before\_success' and 'mid.sa.snmp.allowable\_ failures\_after\_success' to 0.

3.  Check the logs after the Discovery.
4.  Observe messages such as, 'SNMP command failure count is 1 and allowable failures before success is 0. Exiting pattern execution'.

 Expected behavior:The pattern should exit after the first failure.

 Actual behavior: The pattern doesn't exit, and the failure count continues to increase on subsequent errors.

</td></tr><tr><td>

Discovery

 PRB1860779

</td><td>

True-up licensing app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1838171

</td><td>

Integration should be hidden or disabled for Q&amp;A or doc extraction use case for NowAssist Admin

</td><td>

Integrations should be hidden if target tables don't appear.

</td><td>

1.  Install the app-now-assist-admin app.
2.  Navigate to the **Now Assist Admin** &gt; **Feature** &gt; **Platform** &gt; **DocIntel Skill** &gt; **Documentation Q&amp;A**.
3.  Create a new use case without the target table.
4.  Hide integration or disable **Add Integration** if the target table doesn't appear.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1838171

</td><td>

Duplicate names are allowed for the Q&amp;A usecase from Now Assist admin

</td><td>

 Duplicate names shouldn't be allowed.

</td><td>

1.  Provision an instance with the app-now-assist-admin app installed.
2.  Navigate to the **Now Assist Admin** &gt; **Feature** &gt; **Platform** &gt; **DocIntel Skill** &gt; **Documentation Q&amp;A**.
3.  Create a new use case with 'Usecase1'.
4.  Create another usecase with the same name.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1845138

</td><td>

The 'Create field group' page displays tax fields that are still not implemented

</td><td>

The fields '**Sub Field Group Taxes** and **Non Table Taxes types** can be selected even though they are not implemented.

</td><td>

1.  Create a use case.
2.  Open the 'Create field group' view.

 Notice that the fields **Sub Field Group Taxes** and **Non Table Taxes types** can be selected.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1846148

 [KB1924055](https://hi.service-now.com/kb_view.do?sysparm_article=KB1924055)

</td><td>

Fields under table field group are not created for Document Extraction Capability

</td><td>

During the installation process, descriptions are mandatory for fields but not for field groups. However, when attempting to create a field group without providing a description, the user is blocked due to a mandatory description business rule applied to both fields and field groups.

</td><td>

1.  Navigate to **Now Assist Admin** &gt; **Features**.
2.  Select **Platform** &gt; **Document Intelligence**.
3.  Select **Document Extraction**.
4.  Create a Use case UC1.
5.  Create two fields under UC1.
6.  Fields are displaying under UC1.
7.  Create a table field group and create some fields under that field group.

 Expected behavior: Created table fields are displayed.

 Actual behavior: Table fields are not displayed.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1850474

</td><td>

Model reverts to an old version after upgrade due to a race condition

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1853246

</td><td>

Erroneous upgrade of Gen AI use cases

</td><td>

 

</td><td>

1.  Create a new Gen AI use case using Now Assist Document Intelligence.
2.  Run the upgrade job.

 Observe that use case gets upgraded when it shouldn't be.

</td></tr><tr><td>

Document Management Services

 PRB1841221

</td><td>

PDF generation is failing and unable to print the QR code

</td><td>

This issue was observed in Yokohama.

</td><td>

1.  Hop into an instance.
2.  Navigate to the Spaces table.
3.  Open any space.
4.  Select on **Create QR code**.
5.  Notice this navigates to the 'Print QR codes' page.
6.  Select **Print QR codes**.

 Notice that the QR code is unable to print, the job is stuck in 'work in progress', and the PDF is not generated.

</td></tr><tr><td>

Document Management Services

 PRB1847231

</td><td>

PDF error while scheduling reports with the type donut or graph on classic dashboards

</td><td>

Scheduled PDF type reports are failing for donut, graph, and bar chart report types.

</td><td>

 

</td></tr><tr><td>

Dynamic Translation for Virtual Agent

 PRB1853153

</td><td>

Virtual Agent responses are in English when Dynamic Translations are on

</td><td>

This impacts Brazilian Portuguese, French, German, Italian, Japanese, and Spanish.

</td><td>

1.  Ensure Dynamic Translation is enabled and Native LLM is turned off.
2.  Set the language session to Japanese.
3.  Navigate to 'https://&lt;instance name&gt;.service-now.com/sp'.
4.  Open the Virtual Agent chatbot.
5.  Request for '社内在庫管理' and, once the item is found, start the request.
6.  Begin entering Serial ID item inputs.
7.  Continue responding to any additional questions prompted by the chatbot.
8.  Observe the language of the chatbot's responses.

 Expected behavior: All chatbot responses, including those for Serial ID item inputs and other user-provided answers, should be entirely in Japanese.

 Actual behavior: The chatbot responds in English for every input provided by the user, including Serial ID item inputs and any other follow-up responses in the process.

</td></tr><tr><td>

Dynamic Translation

 PRB1847469

</td><td>

A Spanish user runs skills and gets a response in English

</td><td>

 

</td><td>

1.  Set up Dynamic Translation.
2.  Impersonate an agent.
3.  Change the language to Spanish.
4.  Type or select a skill pill.

 Expected behavior: The user gets the entire response in Spanish

 Actual behavior: The user gets a response in English and Spanish.

</td></tr><tr><td>

Dynamic Translation

 PRB1859540

</td><td>

Missing functionality for inbound text from Virtual Agent \(VA\) to bypass DT for an LLM conversation

</td><td>

 

</td><td>

1.  Provision an instance with VA LLM installed.
2.  Install one of the native languages supported by LLM.
3.  Switch a user preferred language to the language.
4.  Start a VA conversation in the language.

 Expected behavior: VA shouldn't DT the user utterance before sending to LLM.

 Actual behavior: VA DTs the user text to English and sends to the LLM, which responds in English. This isn't expected since the user language is different than English.

</td></tr><tr><td>

Edge Encryption

 PRB1844471

</td><td>

After a Vancouver upgrade, a scheduled upgrade is blocked from appearing on a Washington DC or Xanadu's instance for a Vancouver proxy

</td><td>

The **Schedule** button doesn't appear on the edge proxy page, so users are unable to schedule an upgrade.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1846432

</td><td>

SMIME Configuration with encryption doesn't work for the outbound flow

</td><td>

An email sent with encryption enabled is set to send-ignored and throws an error.

</td><td>

1.  Provision an instance with the SMIME plugin installed.
2.  Configure the CA, issuing and recipients certificates in the instance.
3.  As a user with elevated privileges, install the email account certificates.
4.  Enable the SMIME properties for both inbound and outbound flows.
5.  Open an incident.
6.  Send a email with encryption enabled.

 Expected behavior: The email is sent with encryption.

 Actual behavior: The email is set to send-ignored with an error: 'Exception while encrypting the mime message: No default SecureRandom specified and one requested - use CryptoServices Registrar.set SecureRandom\(\) or CryptoServices Registrar.setSecure RandomProvider\(\).'

</td></tr><tr><td>

Email Notifications

 PRB1848037

</td><td>

Email client template doesn't register external users as recipients

</td><td>

In Yokohama, email clients aren't registering external users with email addresses that aren't part of the sys\_user table from the client template.

</td><td>

 

</td></tr><tr><td>

Employee Center

 PRB1800350

</td><td>

Web Content Accessibility Guidlines \(WCAG\) issue for the widgets on the Portal is not announcing a section or groups

</td><td>

The screen reader is not announcing the concerned group as the user tabs through widgets with subsections.

</td><td>

1.  Use a screen reader.
2.  Go to the Employee Service Center or Service Portal.
3.  Tab through a widget that has subsections.

 Expected: The screen reader should announce the group name when user navigate to any group or section, and the user will come to know in which group the focused element is in.

 Actual: The screen reader is not announcing the concerned group as the user navigates any of the sections or groups in the home page, and instead announces just the focused element details.

</td></tr><tr><td>

Employee Center

 PRB1806589

 [KB1704673](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704673)

</td><td>

Employee Center autocomplete suggestions don't work in Xanadu

</td><td>

The autocomplete suggestions of a base instance ESC AI Search doesn't work in Xanadu.

</td><td>

1.  Open a base instance ESC Portal in Xanadu.
2.  In the Search box, type 'What is spam?'.

 Expected behavior: There are suggestions in the typeahead widget.

 Actual behavior: There are no suggestion results.

</td></tr><tr><td>

Employee Center

 PRB1817222

</td><td>

Level 2 subcategories don't follow a tree form in the 'Categories' widget

</td><td>

The 'SC Categories' widget doesn't display the proper indentation for the Level 2 categories. The tree structure of the second level is the same as the parent and this creates confusion of where the categories end.

</td><td>

1.  Navigate to any Washington DC instance.
2.  Navigate to esc?id=sc\_category.
3.  Select the second level catalogs.

 Expected behavior: The second level content under the tree should get aligned similarly to the first level.

 Actual behavior: The content under the first level is properly aligned below the tree. The second level content isn't aligned properly under the tree.

</td></tr><tr><td>

Employee Center

 PRB1820904

 [KB1705991](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705991)

</td><td>

A missing semi-colon in the EC Theme breaks the CSS resolution

</td><td>

A missing semi colon at the end of a new theme variable in EC Theme causes the CSS resolution to break.

</td><td>

1.  Log in to an instance with the latest EC apps.
2.  Create an incident using the 'Create Incident' catalog item on the ESC Portal.
3.  Navigate to 'My Requests'.
4.  Open the newly created incident.

 Observe that the 'Start' text isn't encircled in a green color.

</td></tr><tr><td>

Employee Center

 PRB1827901

</td><td>

On the EC homepage, the 'My items' widget displays 'You don't have any items yet', then loads

</td><td>

The text 'You don't have any items yet' shouldn't come up unless there aren't any active activity configurations on the instance.

</td><td>

 

</td></tr><tr><td>

Employee Center

 PRB1835498

 [KB1778952](https://hi.service-now.com/kb_view.do?sysparm_article=KB1778952)

</td><td>

The 'Delegate this task' on a Journey Task is missing on the jny\_task\_details page if the same task is not part of any to-do configuration

</td><td>

Under certain circumstances, 'Delegate this task' might not be visible on the jny\_task\_details page for some Journey Tasks.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Employee Center

 PRB1843331

</td><td>

The ACL for kb\_knowledge in Employee Center Core provides admins access to edit the knowledge article in the 'Retired' Workflow

</td><td>

Users are able to edit knowledge articles that are in the 'Retired' Workflow when the Employee Center Core application is installed.

</td><td>

1.  Navigate to an Xanadu instance with the Employee Center Core application installed.
2.  Navigate to any knowledge article in the 'Retired' workflow state.

 Observe that an article is editable with the workflow state as read-only.

</td></tr><tr><td>

Employee Center

 PRB1846423

</td><td>

HTML fields on published articles are minimized in Native UI even when they contain content in Yokohama

</td><td>

The content of the article cannot be seen unless the field window is manually expanded.

</td><td>

1.  Create an article using an article template.
2.  Add a line to each of the HTML fields.
3.  Complete the publishing process.
4.  Navigate to the article in Native UI once it is published.

 Notice that the content cannot be seen unless each field is manually expanded.

</td></tr><tr><td>

Event Management Connectors

 PRB1842835

 [KB1775976](https://hi.service-now.com/kb_view.do?sysparm_article=KB1775976)

</td><td>

AWS SNS basic authentication isn't working with the Rest API Access policy for the inbound\_event rest API used by push connectors

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management Connectors

 PRB1846463

</td><td>

Events are not generated using Azure authorization

</td><td>

 

</td><td>

1.  Navigate to a Xanadu or Yokohama instance.
2.  Create Azure authorization.
3.  Send an event.

 Notice that events are not generated.

</td></tr><tr><td>

Event Management

 PRB1822392

</td><td>

After an upgrade to Xanadu, if automated grouping is turned off, \(sa\_analytics.aggregation\_enabled=false\) tag-based grouping isn't working

</td><td>

The sa\_analytics.aggregation \_enabled property should be responsible only for automated, CMDB and text grouping. In addition, there should be a feature flag property on the entire query job \(sa\_analytics.query\_job\_enabled\). When set to false, no logic inside the query job executes.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1833315

</td><td>

Update itom-noc-app version

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1834020

</td><td>

A user with the role evt\_team\_operator can read all records from the em\_root\_cause table.

</td><td>

In the em\_root\_cause table, a user with the role evt\_team\_operator should only be able to read root\_cause\_alert or parant\_alert records that are part of their groups.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1835099

</td><td>

evt\_team\_operator has no access to flow information

</td><td>

evt\_team\_operator has no access to flow information and evt\_team\_operator doesn't know when the flow of playbook is done.

</td><td>

1.  Log in / impersonate evt\_team\_operator.
2.  Open express list and open an alert.
3.  Activate the playbook button.
4.  Run remediation - Create incident.

 Notice that the incident is created but remains 'In progress' rather than 'Complete'.

</td></tr><tr><td>

Event Management

 PRB1835604

</td><td>

Impact path in Service Map not showing alerts

</td><td>

An evt\_team operator user cannot see alerts in an impact path.

</td><td>

1.  Impersonate an evt\_team\_operator.
2.  Open Service Map.
3.  Open an impact path.

 Notice that alerts cannot be seen by the user.

</td></tr><tr><td>

Event Management

 PRB1838597

 [KB1743614](https://hi.service-now.com/kb_view.do?sysparm_article=KB1743614)

</td><td>

Event Rule changes can cause event\_rule.update\_events to block system events processing, causing a performance issue in the instance

</td><td>

When Event Rules are inserted or updated, an 'event\_rule.update\_events' system event is fired in the default events queue to re-check any event records not yet covered by any previously existing event rule. The script action 'Update event rules for empty events/Update rules after deletion of ER' runs for the event, which processes batches of system events from the platform and other features. When an instance has a large number of em\_event records matching the new rule criteria, this causes a long running transaction. Events can take several minutes to process, blocking the 'Events process 0' job of the app node, delaying the processing of other important events that should be processed in near real time.

</td><td>

1.  Open an instance with Event Management installed.
2.  Insert, update, or delete an Event Rule in which there will be a considerable number of existing em\_event record that will match it.

</td></tr><tr><td>

Event Management

 PRB1840955

</td><td>

Network traffic groups are created when the property sa\_analytics.aggregation \_enabled is set to 'false'

</td><td>

 

</td><td>

1.  Open a track instance.
2.  Install the event management plugin.
3.  Install the Tag Based Clustering Engine scoped app \(sn\_em\_tbac\), Service Management plugin, and the Service Mapping Plus app \(sn\_sm\_scoped\_app\).
4.  Set the property sa\_analytics.aggregation \_enabled to 'false'.
5.  Run the script to create service mapping data.
6.  Make sure the 'hash sm\_is\_data\_training\_complete' in the sa\_hash table is 'true'.
7.  Execute the scheduled job 'Event Management - Populate Service candidate process to process mapping'.
8.  Navigate to the table em\_service\_candidate\_ process\_mapping.
    1.  Choose a record in that table.
    2.  Send alerts on the 'first ci in connection' and 'second ci in connection'.
9.  Notice that a network traffic group was created.

</td></tr><tr><td>

Event Management

 PRB1842565

</td><td>

Simulation results are not being displayed

</td><td>

When there are no matches in the first bulk query of 300 alerts, the simulation results appear but then disappear after a few seconds.

</td><td>

1.  Create a new grouping automation where alerts with the node not containing a name are excluded.
2.  Run the simulation.

 Observe several results in the total, then the number disappears and is replaced by "No matching alerts. There are no alerts that match the defined conditions and filters for this simulation."

</td></tr><tr><td>

Flow Engine

 PRB1843277

</td><td>

Users get an error when creating a flow from Table Builder or from logic and automation on a partially upgraded instance

</td><td>

An error is thrown: 'java.lang.NullPointerException: Cannot invoke "com.glide.db. PrimaryKey.addQuery \(com.glide.db. meta.Query, String\)...'

</td><td>

1.  Provision an instance having Washington DC installed.
2.  Partially upgrade it to Yokohama.
3.  Navigate to AES.
4.  Create an app or use existing an app.
5.  Create a table in it.
6.  Edit the table.
7.  Create a flow in it.

 Expected behavior: The user must be able to create the flow in it.

 Actual behavior: The user is getting an error.

</td></tr><tr><td>

Flow Engine

 PRB1856307

</td><td>

Use VA-threads in Flow Engine

</td><td>

 

</td><td>

This is a product update.

</td></tr><tr><td>

Flow Engine

 PRB1856308

</td><td>

Flow Engine Glide tracing

</td><td>

 

</td><td>

This is a product update.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1827921

 [KB1809423](https://hi.service-now.com/kb_view.do?sysparm_article=KB1809423)

</td><td>

The 'String to Date' function is not working as expected after upgrading to Xanadu

</td><td>

On Flow Engine v2, when an invalid transformation such as 'String to Date' is applied to a field which returns a date value \(ex. Duration\), it returns the display value of Duration.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1844406

</td><td>

The IntermediateFlow. processIntermediateFlow\(\) API doesn't work properly with the trigger type 'sla\_task'

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1850367

</td><td>

Enable a generation\_source value other than 'text2flow' in Flow Generation

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC Platform Plugins

 PRB1789050

</td><td>

When importing policy text, images don't render and there's misalignment

</td><td>

In Compliance Workspace with O365 Integration enabled, 'Import Policy Text - Images' don't render and there's misalignment.

</td><td>

1.  Impersonate a user.
2.  Open a policy in the Compliance Workspace​.
3.  Create a policy in 'Draft'.
4.  Navigate to 'Policy text'.
5.  Select **Import Policy** text.​
6.  Add a file in attachment.
7.  Select **Import**.
8.  Navigate back to the 'Policy text' tab.

 Observe the misalignment.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1842928

</td><td>

The **Revised by** field is empty when a policy is re-published in Policy and Compliance

</td><td>

Re-publishing a policy after moving it into a 'Draft' state displays an empty **Revised by** field.

</td><td>

1.  Navigate to an instance.
2.  Create a policy.
3.  Publish the policy.
4.  Move the policy into the 'Draft' state.
5.  Re-publish the policy.

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1838418

</td><td>

Elasticsearch fails with parsing errors due to automatic numeric\_detection

</td><td>

When Elasticsearch Datainput has the **Timestamp field format** field populated, any value set to "Delay in reading current timestamp" creates an exception in the code and the data input fails.

</td><td>

1.  Create ES data input.
2.  Set a 'Timestamp field format'.
3.  Start it and verify that everything is working.
4.  Add any value to "Delay in reading current timestamp".
5.  Save and publish.

 Expected behavior: Data input runs and the feature works.

 Actual behavior: Data input fails and MID throws an exception.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1832870

</td><td>

'Potential infinite loop' errors in the 'MIF Consumer' job

</td><td>

The 'MIF Consumer' job fails when attempting to poll for new messages on the MIF topic.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1833592

</td><td>

Topic sync fails as a result of moving an instance between two clusters within the same data center

</td><td>

The topic sync job fails to create topics on destination cluster because the three letter code is the same.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1841698

 [KB1809311](https://hi.service-now.com/kb_view.do?sysparm_article=KB1809311)

</td><td>

There's duplicate entries in hermes\_cluster\_config

</td><td>

Duplicate entries in hermes\_cluster\_config table are causing dependant plugins to not work as expected, causing node failure during upgrades.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1845171

</td><td>

After upgrading from Washington DC to Yokohama, the number of topics in the sys\_kafka\_topic table is doubled

</td><td>

For example, there is a topic 'sn\_streamconnect. scriptconsumertopic' in W in sys\_kafka\_topic table. After the upgrade to Y, there is additional topic record 'scriptconsumertopic' is noticed in sys\_kafka\_topic table.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1845208

</td><td>

Hermes tables aren't being audited

</td><td>

 

</td><td>

Modify hermes\_topics\_state or hermes\_app\_services.

 Notice that it's not being audited.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1845224

</td><td>

There's no warning that deleting sys\_kafka\_topic deletes the topic in a cluster

</td><td>

Deleting a topic in sys\_kafka\_topic deletes it in the cluster. Users should be warned about that.

</td><td>

Delete a sys\_kafka\_topic record in Xanadu or later.

 Notice that it's deleted in a cluster and no warning was given.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1847936

</td><td>

Reduce DB query for producing to shared topic

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1850227

</td><td>

Topic sync runs for apps that don't need it

</td><td>

TopicSynchronizer only syncs snc.\* topics, so it is not needed for apps like MIF \(Multi-nstance Framework\).

</td><td>

Run a topic sync job with MIF installed.

 Observe that it makes a list topic call unnecessarily.

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

 PRB1827623

</td><td>

'\[Add to Wishlist\]' isn't displayed in the CSM portal after upgrading to Xanadu

</td><td>

It can be added in Service Portal, but in the CSM portal, the 'CSM SC Cat item' widget doesn't have \[Show Add/Update Wish List buttons\] as an instance option.

</td><td>

1.  Provision an instance with the Customer Service Management plugin to have a CSM portal.
2.  Find one sc\_cat\_item with 'Catalogs' and 'Category' defined and 'Catalog' enabled with Wishlist=true.
3.  Confirm it in the CSM portal.

 Expected behavior: It should be with the \[Add to Wishlist\] option, same as Vancouver.

 Actual behavior: \[Add to Wishlist\] isn't displayed in Washington and Xanadu.

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

 PRB1848928

</td><td>

There's an RCA error on creating LE and ER Cases for summarization

</td><td>

An error is thrown: 'Read operation on table 'sn\_hr\_le\_case' from scope 'Now Assist context menu' was denied. The application 'Now Assist context menu' must declare a cross scope access'.

</td><td>

1.  Log in to an instance.
2.  Create an LE case as an agent with the sn\_hr\_le.case\_writer role.

 Observe that an RCA error is thrown.

</td></tr><tr><td>

HR Service Delivery for Healthcare

 PRB1782987

</td><td>

Relocation assistance and work visa transfer request are missing in pre-boarding

</td><td>

Relocation assistance and work visa transfer request are missing in pre-boarding when the checkboxes are checked during onboarding, and the record producer do not trigger the cases.

</td><td>

1.  Open the healthcare onboarding catalog as a manager.
2.  Fill the required details.
3.  Check the checkboxes for **relocation assistance** and **work visa transfer request**.

 Expectation behavior: These record producer variables should trigger respective cases.

 Actual behavior: The variables are not triggering the respective cases.

</td></tr><tr><td>

HR Service Delivery for Healthcare

 PRB1783004

</td><td>

The **specialty** field is not populated

</td><td>

The **specialty** field is not populated in the adhoc update request form for education and trainings when an existing record is selected by the user.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery for Healthcare

 PRB1832614

</td><td>

Stage1 of healthcare onboarding is getting errored out New Hire notification activity

</td><td>

 

</td><td>

1.  As an manager, navigate to **ESC portal** &gt; **Human resources** &gt; **Onboarding**.
2.  Open the 'Healthcare onboarding' catalog item and fill in the required details.
3.  Submit the catalog item.

 Observe the case is getting created but stage1 is in an error state.

</td></tr><tr><td>

HR Service Delivery for Healthcare

 PRB1832614

</td><td>

Stage1 of healthcare onboarding errors out a New Hire notification activity

</td><td>

 

</td><td>

1.  As an manager, navigate to **ESC portal** &gt; **Human resources** &gt; **Onboarding**.
2.  Open a 'Healthcare onboarding' catalog item and fill in the required details.
3.  Submit the catalog item.

 Observe that the case is created but stage1 is in an error state.

</td></tr><tr><td>

HR Service Delivery for Healthcare

 PRB1832662

</td><td>

Duplicate RCAs are present in app-hr and app-hr-healthcare

</td><td>

When searching for RCAs for Healthcare application, there are no duplicate RCAs found.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1830128

</td><td>

Quotes aren't correct in HTML in HR Workspace and Playbook after upgrading from Vancouver to Xanadu

</td><td>

Special characters are rendered in an encoded format.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1837460

</td><td>

Using the 'Email recommendations elaborate' functionality generates RCAs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1840325

</td><td>

The **State** field is read-only for the Agent in an interaction

</td><td>

When an interaction is created, the **State** field is read-only when it shouldn't be.

</td><td>

1.  Provision an instance with Agent Chat and sn\_hr\_agent\_ws 4.0 installed.
2.  Log in to the instance as an agent.
3.  Create an interaction in Human Core scope or create an appointment from esc that creates an interaction in Human Core scope.

 Expected behavior: The **State** field should not be read-only.

 Actual behavior: The **State** field is read-only.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1826985

</td><td>

The 'depends on' column is empty for manually added dependencies

</td><td>

The issue is found only in Yokohama instances.

</td><td>

1.  Install Business Continuity Management 7.1.0 apps on a Yokohama instance.
2.  Log in as a BCM Manager.
3.  Navigate to the BCM Workspace.
4.  Create a Business Impact Analysis on Adobe Acrobat.
5.  Navigate to the 'Assessment' tab.
6.  Navigate to **Dependency assessment**.
7.  Navigate to **Hardware** &gt; **Add dependencies**.
8.  Verify that the 'depends on' column is empty for manually added dependency.
9.  Verify that status in source is 'valid'.
10. Select **Update dependency**.
11. Verify that the dependency added through the Configuration Management Database has the 'depends on' column filled.
12. Verify that all manually added dependency statuses in the source are invalid.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1841733

 [KB1813433](https://hi.service-now.com/kb_view.do?sysparm_article=KB1813433)

</td><td>

There's warnings seen in syslogs on visiting a classic form with an html-editor on it

</td><td>

'com.glide.script.RhinoEcmaError: null is not a function. : Line\(1\) column\(0\) ==&gt; 1: null\(\)' warnings are displayed in sys logs after upgrading to Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1795757

</td><td>

The IDR queue dashboard displays an incorrect value for the remaining messages that are to be processed for V2 sets

</td><td>

The queue dashboard displays the end offset of partition 1 as remaining messages, even though from the topic inspector it's evident that there are no new messages arriving there \(current and end offset same\). The logic for remaining messages should account for an active partition and then calculate the remaining messages based on the current and end offset values.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1838458

</td><td>

Selected fields in 'Outbound Entry' aren't replicated to 'Inbound Entry' when a transformation is enabled \(specifically sys\_fields\)

</td><td>

When a user creates a 'Replication Entry' with transformation enabled, this freezes the selected/deselected sys\_ fields. Specifically, it freezes the ones that are gated by the 'Preserved Modified By' checkbox.

</td><td>

1.  On a 'Producer Replication' set, have sys\_ fields included and enable transformation on any table.
2.  Establish a 'Consumer' set.
3.  Ensure replication works.
4.  Remove/add a sys\_ field on a 'Producer Entry' set.
5.  Synchronize on the consumer side.

 Observe that the removal/addition isn't present on the 'Consumer Inbound Entry'.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1846711

</td><td>

If the legacy cluster is offline, the 'IDR Producer' job is in a 'doNothing' state

</td><td>

This prevents processing for Hermes sets too, even if the Hermes cluster is online.

</td><td>

Have the legacy cluster offline.

 Notice errors in the log and observe that the Hermes replication sets are also not processed.

</td></tr><tr><td>

Integration Hub

 PRB1827642

</td><td>

Incorrect encoding of the URL in a REST step

</td><td>

A new action created in Flow Designer with a REST step is encoded unnecessarily.

</td><td>

1.  Open an instance.
2.  Navigate to Flow Designer.
3.  Create a new action.
4.  Add a REST step.
5.  Configure the REST step.

 Notice that spaces around the EQ operator are being replaced with incorrect characters and are encoded unnecessarily.

</td></tr><tr><td>

Integration Hub

 PRB1830991

</td><td>

'Grouped by' records aren't shown when the user navigates to list view from a dashboard

</td><td>

An invalid TRENDBY condition in the chart's data source results in records not being shown when the user navigates to list view from a dashboard.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1836492

</td><td>

After upgrading to Xanadu, a 'No valid MID server' error is outputted by OAuthTokenRefreshJob

</td><td>

The error 'No valid MID server with REST capability available to obtain new access token' is outputted. The **use\_mid** field doesn't exist on the discovery\_credentials table until the 'com.snc.mid. enhanced\_security.oaut' plugin is installed.

</td><td>

1.  Prepare an instance which doesn't install the 'com.snc.mid. enhanced\_security.oauth' plugin.
2.  Allow OAuthTokenRefreshJob to run.
3.  Check the syslog to see if the error message is outputted.

</td></tr><tr><td>

Integration Hub

 PRB1843074

</td><td>

The configurability of call chain debug logging for Integration Hub is insufficiently granular

</td><td>

There should be a couple more properties for if users only want to log certain scenarios.

</td><td>

1.  Enable glide.sys.client.call\_chain.debug=true on an instance.
2.  Run a REST step as well as a RMv2.

 See that users get logging statements for each of the following: Flow Engine starting, posting a usage to ua\_ih\_usage, and posting a transaction to outbound\_request\_usage\_metrics. If users only care about one of these scenarios, this is more logging than is needed if users want to leave the logging on for something that might only happen a few times per month.

</td></tr><tr><td>

JVM at Scale

 PRB1838848

</td><td>

User preference glide aggregate query ignores setWorkflow and setRunEngines

</td><td>

The cache is flushed which causes the table descriptor cache to rebuild.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1839570

</td><td>

Upgrading to Xanadu causes module keys that are wrapped with a deactivated IKEK to be rekeyed with the active IKEK and then deactivated

</td><td>

This is an issue in KMF that causes module keys that are wrapped with a deactivated IKEK to be rekeyed with the active IKEK and then deactivated. The user is using a specific filter to find the correct module key to use for CLE, based on the sys\_id. However, because that key was deactivated, CLE failed.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1841667

</td><td>

An incomplete CRL Distribution Point is inserted to a leaf certificate

</td><td>

When a leaf certificate is generated from a CSR, the CRL Distribution Point is inserted into the X.509 certificate. However, due to a flipped condition in KMFInstancePKIProvider, the serial number of the issuing certificate is not included, causing the distribution point to fall back to the default "fallback" endpoint.

</td><td>

1.  Setup IPKI.
2.  Generate CSR.
3.  Navigate to "sys\_kmf\_certificate" and select **Request certificate**.
4.  Upload the generated CSR.
5.  Download the newly generated certificate and inspect the CRL distribution within.

 Notice that the serial number is not included at the end of the URL.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1847887

</td><td>

Support Bagheera-Phase2 enablement

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1830531

</td><td>

Post-Xanadu upgrade, changing a KB's article length makes the article unsearchable

</td><td>

The issue can be reproducible on any Xanadu instance.

</td><td>

 

</td></tr><tr><td>

Language and Translations

 PRB1835314

</td><td>

Search is not working in the sc\_cat\_item table when a catalog item is created in a non-English language, and is then updated to an English language in an Oracle DB instance

</td><td>

When the user creates a catalog item in a non-English language, it can be searched by its name in the sc\_cat\_item table. However, when the name of the catalog item is updated to an English language, it cannot be searched in the sc\_cat\_item table in a non-English language.

</td><td>

 

</td></tr><tr><td>

Legacy Agent Workspace

 PRB1830362

</td><td>

Links are not parsed correctly for external users

</td><td>

Links are not parsed correctly and 403 errors are seen in the browser console for external users.

</td><td>

1.  Embed Knowledge Article View Components on the third Party page.
2.  Log in to a third party page.

Observe that the Knowledge Article View component is loaded once authenticated.

3.  Embed the article which has some links in the article body or has some notifications in links.

 Expected behavior: Links in the notification/article body should be parsed correctly.

 Actual behavior: Links are not getting parsed correctly and 403 errors are seen in the browser console for external users.

</td></tr><tr><td>

Lifecycle Events

 PRB1840971

</td><td>

A workflow errors out after reaching the maximum number of retries in a voluntary separation flow

</td><td>

The Voluntary Separation Confirmation activity gets stuck for a long time and errors out after max retries.

</td><td>

1.  Navigate to **All** &gt; **Manage lifecycle events** and open the offboarding \(demo\) event.
2.  Change the trigger condition of all activity sets to immediate.
3.  Select the **Test activity sets** icon.
4.  Select the subject person \(they should have an employment type and employment start date in their HR profile\) and select **Test**.

A case is created.

5.  Open the case and open the activity set **Coordinate Separation Activities**​.

 Observe that the Voluntary Separation Confirmation activity gets stuck for a long time and errors out after max retries.

</td></tr><tr><td>

Lifecycle Events

 PRB1847452

</td><td>

The 'Check Activity closure - Flow' business rule \(BR\) may run and query more often than necessary

</td><td>

Notice that the 'Check Activity closure - Flow' business rule runs and queries for all sys\_flow\_context updates where 'state=COMPLETE'. This can lead to performance issues with an excessive number of sys\_trigger records created and unnecessary queries run by this BR.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1767773

</td><td>

The list calculation shows an incorrect count when applying 'Group by' on the list

</td><td>

After ensuring the total sum at the bottom of the list is the sum of all the priority values added together, applying 'Group by' results in the total sum at the bottom of the list to be incorrect.

</td><td>

1.  Open any list that contains more than 100 records.
2.  Add the priority column.
3.  Navigate to **Configure** &gt; **List Calculations** &gt; **Total Value for the Priority list**.
4.  Ensure that the total sum at the bottom of list should be the sum of all the priority values added together.
5.  Apply 'Group by Short Description or by Number'.

 Expected behavior: The total sum should be sum of all the priority values.

 Actual behavior : The total sum at the bottom of the list is incorrect.

</td></tr><tr><td>

List Administration

 PRB1838932

</td><td>

Workspace list header disappears on reload

</td><td>

The list header is not shown.

</td><td>

1.  Navigate to CSM/FSM Configurable Workspace.
2.  Open any list view.
3.  Refresh the page.

 Expected behavior: The list heading is shown on refresh.

 Actual behavior: The list heading disappears.

</td></tr><tr><td>

List Administration

 PRB1840323

</td><td>

The **Resume / cancel** UI component doesn't show the **Date** field

</td><td>

Selecting the **Resume / Cancel** buttons doesn't show the date field.

</td><td>

 

</td></tr><tr><td>

List Filters

 PRB1839491

</td><td>

Issue with filter query on Record List component when used from UIB

</td><td>

When a list view with the Record List component is created using UIB, and the table query is passed as a parameter, the filter is applied but doesn't appear the conditions set.

</td><td>

1.  Navigate to provided URL.
2.  Select the record preview icon.

This navigates to another page with the filter applied and filters the record as per the applied filter.

3.  Open the conditions set.

 Expected behavior: Conditions from the applied filter should be present.

 Actual behavior: The conditions set is empty.

</td></tr><tr><td>

Major Incident Management

 PRB1851629

</td><td>

Major Incident Management \(MIM\) is not loading when the Digital End-User Experience \(DEX\) plugin is installed

</td><td>

When the DEX plugin is installed, MIM functionalities do not load.

</td><td>

1.  Log in as an admin.
2.  Install MIM.
3.  Install the DEX plugin.
4.  Create a new Major Incident.
5.  Select**View Workbench**.

 Observe that the workbench is not loading.

</td></tr><tr><td>

MID Server

 PRB1760614

</td><td>

SudoProcessor doesn't properly support commands with file paths

</td><td>

When configuring certain commands used by 'Parse File', they fail with 'Permission Denied' errors if configured in Sudo with a filepath specified, such as: /bin/cat /path/to/file.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1842068

</td><td>

Removing 'Check instance' from the policy does not remove it from the agent's check list for that policy

</td><td>

When the list of checks on a policy is updated \(checks are removed/added\), the list of checks on the agent is only updated with the checks that have been added to the policy list, while checks that were removed from the policy list are not updated on the agent.

</td><td>

1.  Create a policy running check-discovery-basic check definition.
2.  Publish the policy and wait for it to start executing on the agent.
3.  Edit the policy in sandbox and replace check-discovery-basic with check-read-log.
4.  Republish the policy and wait for policy to sync to agent.

 Expected behavior: The agent logs that the check list for the policy is just check-read-log. The agent only executes check-read-log as part of the policy run.

 Actual behavior: The agent logs that the check list for the policy is check-read-log and check-discovery-basic. The agent executes both check instances as part of the policy run.

</td></tr><tr><td>

Mobile Experience for Field Service Management

 PRB1840564

</td><td>

A map doesn't load when users tap 'set location'

</td><td>

Users see a blank screen.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1826545

</td><td>

Unable to source a part from the part requirement flow for Mobile iOS

</td><td>

An error message occurs when the user sources a part in the part requirement flow for Field Service Management \(FSM\) in iOS only.

</td><td>

1.  Navigate to **All** &gt; **System logs** &gt; **Emails** &gt; **Open recent email** for a user with the role wm\_agent.
2.  Select **Enter**.
3.  Log in as the user with the wm\_agent role.
4.  Navigate to **My Inventory** &gt; **My part requirements** &gt; **Create part requirement** &gt; **Model : 3com cat 5 cable**.
    1.  Enter any required details.
    2.  Select **Submit**.
5.  Select **Create part requirement** in the list view.
6.  Select **Find part** &gt; **Give radius** &gt; **Submit**.
7.  Select any card on the map.
8.  Select a stockroom as a 'personal stockroom' for the user.

 Expected behavior: It should be submitted and the success message should be seen.

 Actual behavior: Notice the error message.

</td></tr><tr><td>

Mobile Platform

 PRB1843738

</td><td>

Field parameters for the URL button type that are used for the URL template are always encoded even when it's not needed

</td><td>

When selecting the options below on the Now Mobile app, the page doesn't navigate as expected. Instead, it is taken to a 'The page you are looking for could not be found' search screen. After selecting 'Go', the page is redirected correctly. Options: 'Open my Reservation » mesp?id=wsd\_reservations' and 'Create a new general reservation »mesp?id=wsd\_search'.

</td><td>

1.  Access the instance via Now Mobile.
2.  Select the following options and notice the issue described:
    1.  Open my Reservation » mesp?id=wsd\_reservations
    2.  Create a new general reservation »mesp?id=wsd\_search
3.  Select **Go**.

 Notice that the page redirects correctly after selecting **Go**.

</td></tr><tr><td>

Mobile Platform

 PRB1844740

</td><td>

If a **dot-walk** field references a column in the parent table, document data isn't saved

</td><td>

Document data isn't displayed offline because it isn't saved in SQLite DB.

</td><td>

1.  Create a Table A extending task.
2.  Add a reference column.
3.  Create a child Table B extending from Table B.
4.  Add a few columns.
5.  Add a form screen to display the Table B record to show the reference field defined in Table A.
6.  Verify that the form screen is displayed correctly in the mobile app.
7.  Go offline.

 Notice that the form screen can't be displayed offline because the document data for Table B isn't saved in an SQLite database.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1836091

</td><td>

There's a 'Session Expired 401' modal on public pages

</td><td>

The 'sn-banner-announcement-list' component emits an HTTP\_ERROR\_OCCURRED event causing a CANVAS\_GLOVAL\_ERROR event to open the 401 alert dialog.

</td><td>

1.  Create a page in UI Builder.
2.  Make it public.
3.  Log out.
4.  Open that public page.

 Notice a 'Session Expired \(401\)' dialog displays.

</td></tr><tr><td>

Now Assist Panel

 PRB1852531

</td><td>

The latency feedback messages are cut at the bottom

</td><td>

The problem likely stems from a height issue for the container.

</td><td>

1.  Navigate to NAP.
2.  Type 'summarize a record'.
3.  Check the latency feedback messages.

 Expected behavior: The message text is displayed whole in the container.

 Actual behavior: The bottom part of the messages are cut.

</td></tr><tr><td>

OneExtend

 PRB1856501

</td><td>

Non-integer temperature value in sys\_generative\_ai\_config record results in NumberFormatException during OneExtend processing

</td><td>

For TextToApp, our Azure OpenAI prompts have a temperature setting of 0.7. This results in a NumberFormatException being thrown in the console, and a generic error being written to the system log.

</td><td>

1.  Configure an Azure OpenAI prompt with a non-integer temperature value \(for example, 0.7\).
2.  Ensure system property sn\_vad\_genai.com.glide.cs. one\_extend.auto\_proxy\_enabled = true.
3.  Execute the prompt via OneExtend.

 Expected behavior: The prompt executes successfully.

 Actual behavior: The prompt is never sent to the LLM, and errors are present in the logs.

</td></tr><tr><td>

Performance Analytics

 PRB1837861

</td><td>

Incorrect Data is populated in CDC fact table when any record is created / updated / deleted at same time

</td><td>

Mining occurs for the inserted record but not the updated record.

</td><td>

1.  Enable NAM on indicator and run first day and incremental jobs.
2.  Insert and update a record for the source table of the indicator at same time.

 Observe that mining occurs for the inserted record but not the updated record.

</td></tr><tr><td>

Performance Analytics

 PRB1854242

</td><td>

Turn off data snapshots on instances that are Raptor standard

</td><td>

From the 'pa\_indicators' list view and 'indicator' form view, users shouldn't see data snapshots. MLB-related buttons shouldn't be visible to users. Users shouldn't be able to modify them via the MLB system property.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1843769

</td><td>

Dashboard metadata broker is not evaluating early

</td><td>

DashboardSysId is a CLIENT\_TRANSFORM\_SCRIPT, which makes it impossible for UXF to early evaluate this data broker.

</td><td>

1.  Open Platform Analytics Dashboards.
2.  Open any dashboard.
3.  Refresh the page.
4.  Observe network calls.

 Expected behavior: Dashboard metadata is evaluated early and is a part of the macroponent call.

 Actual behavior: A new batch request is made which includes the metadata data broker.

</td></tr><tr><td>

Playbook Experience

 PRB1833127

</td><td>

Playbook doesn't display new cards when previous cards are completed in the HR Workspace

</td><td>

New activities will appear only appear when the page is refreshed, instead of automatically appearing upon completing and closing the previous activity.

</td><td>

1.  Setup a lifecycle event.
2.  Select the Additional Actions icon at the top right of the page.
3.  Select **Preview**.
4.  Select **Test**.
5.  Observe that an HR case record was created.
6.  Open the created record in the HR Agent Workspace.
7.  Observe that Activity Set 1 in the Playbook tab created four activities.
8.  Complete the four activities.
9.  Observe that a fifth activity will appear.
10. Open the fifth activity.
11. Set the state to 'Closed complete'.

 Expected behavior: A sixth activity will automatically appear.

 Actual behavior: The sixth activity appears only when the page is refreshed.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1842669

</td><td>

Data definition synchronization slows down Playbook activation even when Playbook has no questionnaire activities

</td><td>

Activating Playbook can take over 1 hour to complete on a Xanadu instance. After setting a system property to turn off flow data variable sync, the activation time decreased to 40 minutes. When running a background script to activate, the process took 19 minutes. Previously, activation time took between 8 and 10 minutes.

</td><td>

1.  Create a Playbook with 100 activities but without any questionnaire activities, adding a trigger and filling all required fields.
2.  Activate the Playbook.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1848445

</td><td>

A PD update set generation takes a long time and/or timeouts for large playbooks with many conditions to run

</td><td>

This can happen with large processes. In extreme cases, update set generation takes 60+ minutes, where the entire process errors out.

</td><td>

1.  Create a large process \(e.g. 200 activities\), where all activities have a condition to run.
2.  Activate.

 Notice how long it takes to generate the update set, and if it fails.

</td></tr><tr><td>

Predictive Intelligence

 PRB1843673

</td><td>

The 'ML Cluster Detail Purge' scheduled job causes out of memory issues

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence Similarity Solution

 PRB1826156

</td><td>

Untranslated annotations with the i18n language plugin

</td><td>

The annotation, 'STEP 1: Please select the table &amp; field\(s\) you want to use to retrieve your similarity results, and the table and fields you want compared' is left untranslated and in English.

</td><td>

1.  Set up a Xanadu testing environment.
2.  Install an i18n language plugin for French.
3.  Navigate to **now/nav/ui/classic/params/target /ml\_capability\_definition\_similarity.do**.

 Observe the hardcoded string, 'STEP 1: Please select the table &amp; field\(s\) you want to use to retrieve your similarity results, and the table and fields you want compared'.

</td></tr><tr><td>

Process Mining

 PRB1834245

</td><td>

Workbench loading times out for a 'Case' table

</td><td>

The change made part of PRB1834245 times out the workbench because it takes time to query the records in a table that has huge data.

</td><td>

1.  Mine a project.
2.  Share to a user that doesn't have a process mining role and has access to incidents.
3.  Ensure the user can see at least one incident in the table.

 Observe that the user can't see the workbench.

</td></tr><tr><td>

Project Management

 PRB1829307

</td><td>

A project actual isn't populated in the resource aggregated monthly for October, though it's populated for September and November

</td><td>

A category project actual isn't populated in table resource\_aggregate\_monthly for October. It does populate for September and November. There is one record for a project actual in October. If looking in resource\_aggregate\_weekly, all project actual records are there.

</td><td>

1.  Open the resource aggregate monthly \[resource\_aggregate\_monthly\] table.

Only 1 record displays under the monthly table and it excludes the month of October.

2.  Check in resource aggregate weekly \[resource\_aggregate\_weekly\].

Records are displayed as expected including the month of October.


</td></tr><tr><td>

Project Management

 PRB1829721

</td><td>

For a group-based ORA, if users update allocation dailies, it's rolling up to only immediate user-based allocation but not rolling up to group allocation without a user

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Remote Tables

 PRB1833193

</td><td>

There is a spike in performance when trying to get the display value of st\_sys\_design\_system\_icon

</td><td>

In the class ScriptableTableDataCacheHelper, the method getSingleRowQuerySysId tries to retrieve cached rows for non-editable tables which causes the issue.

</td><td>

 

</td></tr><tr><td>

Resizable Panes Component

 PRB1830568

</td><td>

Resizable panes divider handle is not working properly in the CSM Configurable Workspace

</td><td>

When adding an iFrame component in the tab sidebar, it causes an issue while trying to adjust the size of the panes in the workspace.

</td><td>

1.  Duplicate a page variant from the base instance page 'CSM default record page' in the CSM Configurable Workspace in the UI builder.
2.  Add a new tab in the tab sidebar.
3.  Add an iFrame component.
4.  Open a Case that applies the duplicated variant.
5.  Verify that the sidebar resizing issue occurs when the iFrame tab is open

</td></tr><tr><td>

Resource Management

 PRB1841076

</td><td>

After an Xanadu upgrade, there's a resource reports issue

</td><td>

Resource reports are broken after an Xanadu upgrade when the glide.sys.date\_format is dd-MM-yyyy.

</td><td>

1.  On Xanadu, set the date format to dd-MM-yyyy or dd/MM/yyyy.
2.  Navigate to **All** &gt; **Resource** &gt; **Resource Reports** &gt; **Resource Reports**.
    1.  Start date auto populates = today's date.
    2.  End date auto populates = 1 year from today's date - 1 day.
3.  Update the start date to 10/12/2024 and end date to 11/11/2025.
4.  Select **Run**.

 Observe the error message 'Report duration can't be more than 12 months'. The system considers the start date as being 12th of October and not 10th of December.

</td></tr><tr><td>

Rollback Contexts

 PRB1844400

 [KB1803428](https://hi.service-now.com/kb_view.do?sysparm_article=KB1803428)

</td><td>

The 'Clean Expired Rollback Contexts' job causes memory issues and node restarts

</td><td>

The job is streaming through large rowblocks of data and causing node restarts. The heap dump shows 1.2GB of memory taken by this job.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

SaaS integration with Adobe Cloud \(Glide\)

 PRB1843443

 [KB1913878](https://hi.service-now.com/kb_view.do?sysparm_article=KB1913878)

</td><td>

sn\_samp. UpdateReclamationCandidates &gt; getUserSubscriptionCost code issue

</td><td>

The **potential\_savings** field is only present on the samp\_sw\_ reclamation\_candidate table, and not in samp\_sw\_rc\_m2m\_subscription. This is causing the 'SAM - Updating Existing Reclamation Candidates' job to fail when updating the hybrid subscription cost.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Scheduled Jobs

 PRB1851796

</td><td>

Intermittent errors in GenAI calls due to missing startDate in transaction

</td><td>

JobYieldCheck fails with a Null Pointer Exception \(link\) because fJobYieldInfo.getStartDate\(\) is null.

</td><td>

1.  Set up NAVA with latest versions on yselfservice track.
2.  Launch a chat window and enter "What is spam" with streaming enabled.
3.  Execute a load test for the same flow \(5/10 users\).

 Notice the exceptions in the error logs, sys\_generative\_ai\_log table. The log file says failed due to "date must not be null".

</td></tr><tr><td>

Schedule Optimization

 PRB1837461

</td><td>

Overlapping territories don't work as expected when file caching is enabled

</td><td>

When file caching is enabled, the work order tasks of the qualifying territories are not sent for optimization.

</td><td>

1.  Enable territory model in the instance.
2.  Add an agent to more than one 'Territory' group \(for example, Sunnyvale and Cupertino\).
3.  Add one of the above territories as the qualifier in the scope.
4.  Add the same scope to the 'Batch'.
5.  Trigger a batch run.
6.  Validate for an intraday run.

 Expected behavior: Both overlapping territory groups should be considered for optimization, and two solution files should be generated for each territory group.

 Actual behavior: When file caching is enabled, the work order tasks of the qualifying territories are not sent for optimization.

</td></tr><tr><td>

Schedule Optimization

 PRB1844169

</td><td>

Errors such as Request Timeout, Syntax Error/Access Rule Violation, and Insufficient Access are seen on the Dispatcher Workspace

</td><td>

Error messages occur in the Dispatcher Workspace as a result of server response timeout, SQL syntax errors, and queries being ignored due to insufficient access.

</td><td>

Scenario 1:

 1.  Request a Timeout Leave in the Dispatcher Workspace.
2.  Idle for sometime.
3.  Notice the alert message, 'Request Timeout: The server took too long to respond. Please try again later'.

 Scenario 2:

 1.  Open the 'My Crews' page.
2.  Notice the Syntax Error or Access Rule Violation message due to an SQL syntax error.

 Scenario 3:

 1.  Assign a crew task to a crew in the Dispatcher Workspace by dragging and dropping the task.
2.  Notice the Syntax Error or Access Rule Violation due to an SQL syntax error.

 Scenario 4:

 1.  Open the Work Order Task record page.
2.  Notice the Insufficient Access error due to the query on sn\_fsm\_map\_integr\_usage being ignored because of insufficient access.

</td></tr><tr><td>

Schedule Optimization

 PRB1846785

</td><td>

A performance issue with beans symmetric travel time and flaten response

</td><td>

This issue introduces symmetric travel time and flatten response for beans calls in Yokohama.

</td><td>

 

</td></tr><tr><td>

Schedules

 PRB1831078

</td><td>

The 'Timeline' page isn't displaying properly with sub items after an Xanadu upgrade

</td><td>

When there is a \[cmn\_timeline\_sub\_item\] record attached, 'View Timeline' doesn't seem to work. The issue is only there when there's a timeline sub item in the 'Timeline' page. If there's no timeline, there's no issue.

</td><td>

1.  Navigate to **All** &gt; **Timeline Pages**.
2.  Select **ServiceNow Roadmap**.
3.  Select the **View Timeline** button.

</td></tr><tr><td>

Server-side scripts

 PRB1841707

</td><td>

Turn on ECMAScript 2021 \(ES12\) mode is not toggled after upgrade/zboot

</td><td>

Turn on ECMAScript 2021 \(ES12\) mode is off.

</td><td>

1.  Unload a sys\_script\_include xml with Turn on ECMAScript 2021 \(ES12\) mode toggled.
2.  Make sure sys\_es\_latest\_script=true.
3.  Add the script include to the 'update' folder in the com.glide.sg plugin.
4.  Zboot the instance.
5.  Spin the instance with Zboot.
6.  Check the record.

 Expected behavior: Turn on ECMAScript 2021 \(ES12\) mode is on.

 Actual behavior: Turn on ECMAScript 2021 \(ES12\) mode is off.

</td></tr><tr><td>

Service Catalog

 PRB1834958

</td><td>

The onLoad Mandatory and Visible UI policies aren't working

</td><td>

For the onLoad Mandatory policy, questions can be skipped. For the onLoad Visible UI policy, an incorrect question is prompted indicating that the policy didn't hide the correct variables.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1835283

</td><td>

A UI policy script is running in Virtual Agent though the UI type is set to 'Desktop'

</td><td>

 

</td><td>

In Virtual Agent chat, request the item 'Seating Arrangement for Onboarding.' This has an onLoad UI Policy to make will\_this\_employee \_be\_ seated\_flex\_or\_remote' read only.

 Expected behavior: The first question should be about a desk request.

 Actual behavior: The question 'Will this employee have a reserved desk, flexible desk, or work remotely?' is asked. This indicated that this isn't a read only question, and the onLoad UI Policy did run.

</td></tr><tr><td>

Service Mapping

 PRB1836767

</td><td>

When deleting a solution in ml\_solution table, a cascade delete is triggered on ml\_cluster\_detail, but the records are not deleted

</td><td>

When deleting a solution in ml\_solution table, a cascade delete is triggered on ml\_cluster\_detail, and it times out and does not delete all of the records because there are too many records in the table to handle a cascade delete.

</td><td>

 

</td></tr><tr><td>

ServiceNow Security Center \(Family Release\)

 PRB1843476

</td><td>

At upgrade time with updated content, the completed steps of a customer action keeps the action status as 'ready', which turns off the action's **Complete** button

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1834196

</td><td>

The **New** button on the 'Changes assigned to me' page doesn't navigate to the SOW change landing page

</td><td>

 

</td><td>

1.  Log in as an admin role user.
2.  Enable the property 'glide.ux.user\_criteria\_enabled'.
3.  Navigate to **Change** &gt; **Create** and create a new change request assigned to 'Change Manager' user.
4.  Impersonate Change Manager \[tier 2 user\].
5.  Navigate to the SOW Home landing page.
6.  Select the **View all** button of the 'Changes assigned to me' donut section.
7.  Switch to the List view of the records display section.
8.  Select the **New** button.

 Expected behavior: The user is navigated to the Change landing page. All **New** buttons on the list page should work.

 Actual behavior: The **New** button on the 'Changes assigned to me' page navigates to the change landing page. The **New** button on other donut lists doesn't work.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1838664

</td><td>

Create standard change on the Service Operations Workspace \(SOW\) shouldn't have the **Model** field populated when the compatibility property is set to 'true'

</td><td>

Flow is attached instead of workflow when the **Model** field is populated as a result of the compatibility property being set to 'true'.

</td><td>

1.  Login as an admin role user.
2.  Go to sys\_properties.LIST.
3.  Set 'com.snc.change\_management. change\_model.type\_compatibility' to **True**.
    1.  Set 'com.snc.change\_management. change\_model.manage\_workflow' to **True**.
    2.  Select **Save**.
4.  Navigate to **SOW** &gt; **Change**.
5.  Create any pre-approved standard change.

 Expected: The **Model** field shouldn't be populated.

 Actual: The **Model** field is populated, as a result flow is attached instead of workflow.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1840201

</td><td>

Typing multiple lines of text in dialogue triggered by the **Make approval decision** button fails to process approvals and rejections

</td><td>

The record is not approved after entering multiple lines of text in the approval notes for a approval decision in the Service Operations Workspace \(SOW\).

</td><td>

1.  Log in to an instance.
2.  Navigate to SOW.
3.  Open a record with an outstanding approval request.
4.  Impersonate a user to approve the record.
5.  Select **Make Approval Decision**.
6.  Select **Approve**.
7.  Enter multiple lines of text as approval notes.
8.  Select **Submit.**

 Notice that the record is not approved.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1841223

</td><td>

Users with the ITIL, change\_manager, or sn\_change\_write roles are not able to propose single change on Service Operations Workspace \(SOW\)

</td><td>

This impacts instances with SOW 6.1 apps installed.

</td><td>

1.  Login as user with ITIL, change\_manager, sn\_change\_write roles in Yokohama or on any instance with SOW 6.1 apps installed.
2.  Navigate to SOW.
3.  Create a new change with the short description populated.
4.  Save the change.
5.  Navigate to **Overview** &gt; **Add scope**.
6.  Select the 'Affected CIs' card.
7.  Add some configuration items to the list.
8.  Select the **Propose single change** icon of any affected CI added.

 Expected behavior: The user is able to edit or propose the change.

 Actual behavior: The user is not able to edit or propose the change.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1841357

</td><td>

The **Propose** button on the Mass CI Update modal is not enabled when multiple fields are added after proposing a single change

</td><td>

The **Propose** button becomes disabled after adding multiple fields to a new change following proposing a single change, and the user can only cancel or exit out of the modal.

</td><td>

1.  Open the Service Operation Workspace \(SOW\).
2.  Create a new change with short description populated.
3.  Select **Save**.
4.  Select the **Add scope** button in the **Overview** tab.
5.  Selected the **Affected CIs** card.
6.  Add some configuration items to the list.
7.  Select **Propose mass CI update**.
8.  Add 'Asset Tag' from the list.
9.  Select **Propose**.

</td></tr><tr><td>

Service Operations Workspace for Change Management

 PRB1851103

</td><td>

The 'Change Overview' data broker needs to have role access defined

</td><td>

Roles are not associated in the Access Control \(ACL\) record.

</td><td>

 

</td></tr><tr><td>

Service Operations Workspace for Incident Management

 PRB1825743

</td><td>

The 'Upcoming' sidebar in the Service Operations Workspace home does not display data to users after upgrading to Xanadu

</td><td>

Overdue tasks are displayed in the 'Upcoming' tab, while users with incidents with breached Service Level Agreements \(SLA\) are not.

</td><td>

1.  Open any Xanadu instance.
2.  Verify that the sn\_incident\_read role does not exist in the instance.
3.  Impersonate an ITIL user.
4.  Navigate to the SOW.
5.  Ensure the user has an incident with a breached Service Level Agreement \(SLA\) visible on the Overview Dashboard.
6.  Check the 'Upcoming' tab.

 Notice that only overdue tasks are displayed, while incidents with breached SLAs are not.

</td></tr><tr><td>

Service Operations Workspace for Incident Management

 PRB1841972

</td><td>

The new Service Operations Workspace \(SOW\) landing page have Performance and Analytics Reporting \(PAR\) variants update entries from SOW version 6.1

</td><td>

Observed after installing SOW 7.0 after SOW 6.1.

</td><td>

1.  Install SOW 6.1 on an instance.
2.  Observe that the PAR variants on the landing page have update entries.
3.  Install SOW 7.0 with some changes to the sys\_ux\_screen record corresponding to the variants.

 Expected behavior: Changes are applied.

 Actual behavior: Changes are skipped.

</td></tr><tr><td>

Service Operations Workspace for Incident Management

 PRB1843168

</td><td>

Donuts are not visible after upgrading SOW Technical Dashboard customization

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Operations Workspace for On-Call Scheduling

 PRB1836197

</td><td>

gs.addErrorMessage fails to appear in Service Operation Workspace \(SOW\) schedules

</td><td>

The error message does not appear as gs.addErrorMessage\(\) for SOW Schedules. However, the business rule that prevents users from selecting SMS as a channel if they are not assigned to the group also includes gs.addErrorMessage\(\), which reminds the user of the failure reason if they do not have the required role.

</td><td>

1.  Log in to an instance.
2.  Open the Service Operations Workspace.
3.  Select **Schedules** in the left sidebar.
4.  Select the tab **On-Call notification preferences**.
5.  Navigate to **My escalation notification rules**.
6.  Edit the preferred communication channel in **Attempt**.
7.  Select **SMS**as the communication channel.
8.  Select **Save**.

 Notice that the message 'On-call user preference has been updated successfully' appears, however SMS is not stored successfully as the preferred communication method in 'Attempt' because it already detects the failure due to the business rule, and the error message doesn't appear in SOW when the user saves the preferences.

</td></tr><tr><td>

Service Operations Workspace ITSM Admin Center

 PRB1825127

</td><td>

Dashboard is not visible after selecting 'Configure' on 'Landing page configurations'

</td><td>

The error message 'Can't display this dashboard' occurs and the dashboard is not visible, even though the user should be able to view it in edit mode after configuring the landing page.

</td><td>

1.  Log in to the instance as an admin user.
2.  Navigate to **All** &gt; **Service Operations Workspace** &gt; **Configuration**.
3.  Open **Landing page configurations**.
4.  Select **Configure** from the donut configurations from the tier 1 or tier 2 sections.

 Expected behavior: Dashboard should be visible to the user in edit mode.

 Actual behavior: Observe the message 'Can't display this dashboard', and notice that the dashboard is not visible.

</td></tr><tr><td>

Service Operations Workspace

 PRB1799519

</td><td>

An event team operator user received the 'Page not found' message when selecting the Service Operations Workspace \(SOW\)

</td><td>

An event team operator user doesn't see the SOW and encounters a 'Page not found' message.

</td><td>

1.  Open the instance.
2.  Log in as an Event Management admin.
3.  Impersonate an event team operator.
4.  Select SOW.
5.  Observe the application.

 Expected Result: The 'Page not found' message is not displayed for the user.

 Actual result: The 'Page not found' message is displayed for the user.

</td></tr><tr><td>

Service Operations Workspace

 PRB1837413

</td><td>

Dynamic translation is not enable on Service Operations Workspace \(SOW\)

</td><td>

This issue can be observed in the Activity Stream in SOW. After configuring dynamic translation with Microsoft Translation, the dynamic translation icon doesn't appear when switching from Customer Service Management \(CSM\) to SOW.

</td><td>

1.  Activate the dynamic translation plugin \(com.glide.dynamic\_translation\).
2.  Navigate to **Connection &amp; credential aliases**.
3.  Open Microsoft Translation.
4.  Navigate to Connection.
5.  Select **New**.
6.  Configure 'Name=MS connection'.
7.  Search 'Credential'.
8.  Select **Create new**.
9.  Configure the API key credential.
10. Configure the connection URL.
11. Select **Submit**.
12. Navigate to the Translator Configuration.
13. Select **Open Microsoft**.
14. Configure 'Active=true'.
15. Check 'Mark as default for translation and detection'.
16. Activate dynamic translation.
17. Ensure it is configured.
18. Post a work note or a comment in a non-English language in Customer Service Management.
19. Verify that the translation icon appears.
20. Switch to SOW.

 Notice that the dynamic translation icon doesn't appear.

</td></tr><tr><td>

Service Portal

 PRB1829670

</td><td>

Genius results shows both catalog items and knowledge articles even when the user is filtering with the navigation tabs

</td><td>

Searching in a portal displays Now Assist Genius results, including catalog items and knowledge search results. Selecting a catalog navigation pane or a knowledge navigation pane, the filtered results display both a catalog item and Now Assist QnA instead of displaying respective filtered results.

</td><td>

1.  Set up Now Assist in AI Search in the instance.
2.  Activate it for the portal /esc.
3.  Enable AI Search in portal.
4.  Map the Genius result configuration in the Genius result related list tab.
5.  Select the existing link.

A new form appears after entering a catalog item in a Genius result configuration.

6.  Navigate to /esc.
7.  Search in the search widget for **Password reset**.

It displays some Genius results, including a knowledge article summary and catalog item.

8.  Select on navigation's **Requests**.
9.  It displays the same Genius results, including the knowledge summary as well.

 Expected behavior: When selecting the **Requests** navigation pane, it should only display a catalog item Genius result and not knowledge. If users select the knowledge navigation pane, it should display only knowledge and not a catalog Genius result.

 Actual behavior: Irrespective of the navigation pane, the Genius result displays both a catalog item and a knowledge summary.

</td></tr><tr><td>

Service Portal

 PRB1840878

</td><td>

The display of the Genius Results card using Now Assist and Knowledge Base articles are not aligned properly after resizing the browser

</td><td>

This issue also impacts the display in mobile devices.

</td><td>

1.  Navigate to a Xanadu instance with Now Assist configured.
2.  Ensure the Portal has AI search enabled.
    1.  Set the Genius search results limit to ten in the Search Application Configuration of the Portal Record.
    2.  Ensure the Search Profile has the Genius Results configuration 'Now Assist Q&amp;A' set in 'Related List'.
3.  Navigate to the Portal.
4.  Search for any keyword.
5.  Notice that catalog items populate in Genius Results.
6.  Resize the browser.
7.  Notice that the alignment of the Genius Results are not correct.
8.  Navigate to the **Knowledge** tab in the search results.
9.  Notice that the alignment of the Knowledge Base results are also not properly aligned.

</td></tr><tr><td>

Session Validation

 PRB1846625

 [KB1812394](https://hi.service-now.com/kb_view.do?sysparm_article=KB1812394)

</td><td>

Deeplinks redirection failed with a node switch from an unauthenticated session to an authenticated session

</td><td>

On opening a deeplink URL, the user should authenticate and redirect to a specific resource.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1840899

 [KB1801232](https://hi.service-now.com/kb_view.do?sysparm_article=KB1801232)

</td><td>

New License Metrics for CrowdStrike

</td><td>

This is a product update.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1842738

</td><td>

Auto-select a metric group based on the CrowdStrike software model

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1853225

</td><td>

Remediation options buttons aren't triggering a scheduled job immediately if date\_format is different

</td><td>

Scheduled job should be scheduled to run immediately.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Workspace

 PRB1833497

</td><td>

There's a workspace functionality issue where filtering products under license usage isn't working

</td><td>

There's an issue with filter products under license usage. All records are displayed if users select a record for any particular version for a product while entering the name of the product in the search field. All the products display again.

</td><td>

 

</td></tr><tr><td>

Special Handling Notes

 PRB1836082

</td><td>

Simplify 'Refresh SHN' conditionals for readability and backportability

</td><td>

In Xanadu, if users set the Special Handling Notes \(SHN\) property 'Display special handling notes only once per session' to false, then the SHN pop-up window isn't displayed at all each time a user accesses a record. However, in Xanadu, once the property is set to false, the SHN pop-up window isn't displayed at all each time a user accesses a record. According to the documentation, the SHN pop-up window should be displayed each time a user accesses a record.

</td><td>

1.  Ensure that the plugin 'Special Handling Notes' \(com.sn\_shn\) is activated.
2.  Ensure to upgrade the Store apps to the latest versions.
3.  Create a 'Special Handling Notes' \(sn\_shn\_notes\) for the 'Incident' table.
4.  Specify a condition, such as 'Short description', that contains something.
5.  Open the SHN 'Properties' page and set the property 'Display special handling notes only once per session' to false.
6.  Open an 'Incident' record which matches the condition in Service Operations Workspace or CSM Workspace.

 Notice that the 'Special Handling Notes' pop-up window isn't displayed at all each time a user accesses the record in either workspace.

</td></tr><tr><td>

Stream Connect Core

 PRB1845639

</td><td>

Kafka Consumer stops consuming messages once it receives a 'null' message from Producer

</td><td>

When a 'null' message error is observed from the source, the Kafka stream no longer consumes the messages.

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB1847486

</td><td>

Multiple concurrent import sets are created for one data source

</td><td>

 

</td><td>

1.  Install an AWS version with parallel loading.
2.  Configure AWS.
3.  Run import.
4.  Check the concurrent import set attached to the imports sets.

</td></tr><tr><td>

Table Cleaner

 PRB1836111

</td><td>

The dot walk in the **Match** field isn't working

</td><td>

There's no unintended data deletion. Table Cleaner thinks the **Match** field with dot walk isn't valid, and therefore doesn't clean anything for that invocation.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1820922

</td><td>

The display business rule causes info messages to not display on quick-edit of records in the Service Operations Workspace \(SOW\)

</td><td>

An info message doesn't display the message when using the 'i' quick-edit feature in SOW or any other workspace. When selecting the 'i' icon to edit a record in quick edit from the list view in the Workspace, the info message is not shown. However, the info message appears correctly when previewing a record using the 'i' icon in the Native UI.

</td><td>

1.  Open any Xanadu or Washington DC instance.
2.  Create a business rule for the incident table that executes on 'Display'.
3.  Add an info message in the script section of the business rule.
4.  Open the incident list in the Native UI.
5.  Select on the **i** preview of a record.

Observe that the business rule is executed and displays the info message.

6.  Open SOW or any workspace.
7.  Select the **i**icon for the quick view edit of a record in the list view.

 Expected behavior: The info message should be displayed upon triggering the business rule in the workspace.

 Actual behavior: The info message is not displayed in the quick-edit view in the workspace.

</td></tr><tr><td>

UI Form Administration

 PRB1836016

</td><td>

Fields in the Metric Data Task of the ESG Workspace are displayed in a single column

</td><td>

This issue occurs when the screen is opened at 100% zoom. If the screen is displayed at approximately 75% zoom, the fields are displayed in two columns according to the defined view. The affected view is as follows: Metric Data Task \[sn\_grc\_metric\_data\_task\] - View: Data task info. This issue doesn't occur in Vancouver, but it occurs after upgrading to Xanadu.

</td><td>

1.  Navigate to a Next Experience instance.
2.  Open the 'sys prop' table and set the value of the property glide.ui.form. breakpoints.enable as false.
3.  Open any configurable workspace.
4.  Open any form record.
5.  Select the 'Details' tab.
6.  Select the resizable panes divider handle and drag this on to left side

 Expected behavior: The form layout should display as a two column layout.

 Actual behavior: The form layout displaying as a single column layout.

</td></tr><tr><td>

UI Form Administration

 PRB1848506

</td><td>

List Control Form has duplicate fields preventing updates

</td><td>

The form should update with changes, but duplicate fields prevent the value from being applied.

</td><td>

1.  On a Xanadu instance modify the form layout and save.
2.  Upgrade the instance to Yokohama.

Notice that there are duplicate fields on the form.

3.  Try to update one \(but not both\) of the duplicate fields, for example, **Hierarchical Lists**.
4.  Save the Form.

 Expected behavior: The form updates with the change.

 Actual behavior: Duplicate fields are preventing the value from being applied.

</td></tr><tr><td>

Upgrade Center

 PRB1844300

</td><td>

sys\_claims customization protection behaves differently than sys\_update\_xml during upgrades when the sys\_policy of the file changes

</td><td>

The installer has no historic knowledge and can't tell if a record was previously unprotected and just became protected in a subsequent release version. This applies both to sys\_claims as well as sys\_update\_xml as a protection mechanism for changes.

</td><td>

1.  Open a Washington DC instance.
2.  Install the sn\_hr\_agent\_ws app.
3.  Customize the 'sys\_ux\_macroponent\_ 1d033475eb3011106eb96bf3a252287f' file.
4.  Publish to the app repo.
5.  Create a customization pack.
6.  Open another instance.
7.  Install the above app along with the app customization.
8.  Ensure the entry for that file is present in the sys\_claim table.
9.  Upgrade the instance to Xanadu's latest patch.
10. Check the upgrade history log for that file.

 Notice that it should be 'SKIPPED', but instead is 'UPDATED'.

</td></tr><tr><td>

Usage Analytics

 PRB1834523

</td><td>

Remove dependency on old Appsee

</td><td>

UXA user session data is not tracked when the collection mode is 'Both' and old appsee is not configured for the instance.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1844882

</td><td>

The user is unable to perform an aggregate query on the table paf\_evt\_aggregate due to an empty ACL role

</td><td>

When a user with elevated privileges generates a report view of the table paf\_evt\_aggregate and shares it with an admin user, that usr can't view the report due to a security exception.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1851575

</td><td>

Mark glide.telemetry.trace. session\_debug\_trace\_enabled as false

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1853847

</td><td>

Switching a non-signed \(anonymous\) user to LoggedIn User Tracking isn't working

</td><td>

Also, impersonating one user to another results in incorrect data tracking.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1854383

</td><td>

Backport for UX Analytics store app dashboard issues

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1840354

</td><td>

When a maintenance item is selected and the **Next** button is selected, it automatically redirects to the new creation plan page

</td><td>

 

</td><td>

1.  Log in with the user contains "sn\_wsd\_maintenance.manager".
2.  Navigate to **Workspaces** &gt; **Workplace Central**.
3.  Select the **Preventive Maintenance** icon on the side bar.
4.  Navigate to **All Plans** &gt; **New**.
5.  Give the plan a name.
6.  Choose today's date in the start date.
7.  Choose an end date in the future.
8.  Select a location \(Plan type\).
9.  Select any building \(Ams - B1\).
10. Select **Next**.

 When a maintenance item is selected and the **Next** button is selected, it automatically redirects to the new creation plan page.

</td></tr><tr><td>

UX Framework

 PRB1843697

</td><td>

The user is unable to tab to side panel on Safari in Yokohama

</td><td>

The 'Questions' tab is not hiding at all when clicked, and the 'Questions' tab hides only when clicked.

</td><td>

1.  Open Assessment Workspace.
2.  Search and click on Operation Risk Management list item.
3.  Select the **Copy** button on the top right.
4.  Select Copy in the modal.

Notice that the page redirects to a new screen.

5.  Wait until the "Copy in progress. This may take a while..." info message appears

 Notice on that screen that the Questions tab hides when clicked in Washington DC and Xanadu instances but not in Yokohama. After a couple of seconds page will again refresh and the tab will be visible again.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1854102

</td><td>

Application scope is not copied over on a duplicate topic in Yokohama

</td><td>

Duplication fails with an error message: 'Application scope is required.'

</td><td>

1.  Navigate to Conversational Studio \(CS\).
2.  Create the topic \(by default Global is the selection for the Application scope\).
3.  In the canvas, duplicate the topic and provide the name.

 Observe that the duplication fails with an error message: 'Application scope is required.'

</td></tr><tr><td>

Virtual Agent

 PRB1833334

</td><td>

A script added as a tool, the execution of the tool fails

</td><td>

If the user adds a script as a tool, and the script include has the **Accessible From** field set to 'This application scope only'. The execution of the tool fails with the error, 'Illegal access to private script include'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1838336

</td><td>

The **Created On** field is missing a value in its response for getCapability and getSkill

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1840741

</td><td>

Plan is generated on NAP for agent from a random use case

</td><td>

A plan should be generated from a use case that is related to the context of the incident.

</td><td>

1.  Configure the same trigger condition on multiple use cases.
2.  Navigate to **incident.list.**
3.  Assign the incident to an agent.
4.  Impersonate the agent.

 Expected behavior: On NAP, a plan should be generated from a use case that is related to the context of the incident when opened by an agent.

 Actual behavior: Plan is generated on NAP for agent from a random use case selected due to race condition.

</td></tr><tr><td>

Virtual Agent

 PRB1843924

</td><td>

KB generation does not work from NAP

</td><td>

 

</td><td>

1.  Activate the Knowledge skill from NAAC.
2.  Navigate to SOW and open any incident in a resolved state that doesn't have a KB attached to it.
3.  Select on NAP and Zboot.

 Expected behavior: KB article is created from NAP.

 Actual behavior: Failure to create the knowledge article with the message, "I'm having technical issues and won't be able to continue this conversation."

</td></tr><tr><td>

Virtual Agent

 PRB1844284

</td><td>

A multi-case KB GenAI call errors out for the agent persona

</td><td>

 

</td><td>

1.  Log in as a user.
2.  Create a KB.
3.  Draft an article with Now Assist.
4.  Enter a search term to search for HR cases.
5.  Select 2 or more cases and continue.

 Observe an error in the Generative AI log for the 'Multi-knowledge article generate' call.

</td></tr><tr><td>

Virtual Agent

 PRB1847222

</td><td>

If a payload has any input with a null value, OE throws a

</td><td>

When the user sends a non-mandatory input with a value of 'null' to OneExtendUtil.execute, the request fails with a null pointer exception.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1847443

</td><td>

Virtual Agent topic with Dynamic Capability node fails during execution

</td><td>

The node fails with a 400001 error.

</td><td>

1.  Open an instance with GAIC 9.1.0-SNAPSHOT installed on a latest track/yselfservice.
2.  Set com.glide.oneapi .fdih.va.execution=true.
3.  Create a Virtual Agent topic with a Dynamic Capability node.
4.  Pass a Capability ID and input an attribute/value.
5.  Run the topic.

 Observe that topic execution fails with 'Sorry, there was a problem...' and 'Error - 400001' in the logs.

</td></tr><tr><td>

Virtual Agent

 PRB1847828

</td><td>

Plan Generation use case only works with incidents

</td><td>

The Plan Generation use case does not work to resolve a case. It only works for incidents

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1850648

</td><td>

During failure scenarios in Virtual Agent, sys\_generative\_ai\_log records not created

</td><td>

An error during post processing does not lead to a sys\_generative\_ai\_log to be created.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1851004

</td><td>

Skill discovery and execution fails with the proxy sys\_prop enabled in Yokohama

</td><td>

Discovery and execution fails when the sysprop com.glide.cs.one\_extend. auto\_proxy\_enabled = false. This is enabled by default.

</td><td>

1.  Open a NAVA portal.
2.  Execute a topic.

The topic executes with error messages in each stage.

3.  Try to perform a topic discovery.

 Observe that discovery fails with a sorry message.

</td></tr><tr><td>

Virtual Agent

 PRB1851248

</td><td>

In sync mode, skill execution involving RAG is failing

</td><td>

For the skill mentioned, RAG tool is failing in 'sync' mode due to an empty query input. It looks like it's not able to fetch and resolve 'query' from the previous tool output.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1853056

</td><td>

An API call should return a response in French, but the response is in English

</td><td>

The API is called with dtTargetLanguage = 'en' and enableDT = false, which is wrong. The correct response should have dtTargetLanguage = 'fr' and enableDT = true.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1854031

</td><td>

Fix the 'licensing usage' log

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1854061

</td><td>

OptimisticLockException when executing dynamic capability

</td><td>

The output refiner response is proper, but it fails to return a response to the dynamic capability node in the topic.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1854081

</td><td>

GAIC Licensing should charge assists instead of trial assists even when the 'Licensing' API returns that a feature isn't configured in pricing

</td><td>

When a GAIC capability is executed, as part of licensing, a call is made to the 'Licensing' API to get the assists configured for that capability. If it is not present in pricing, users get an empty response. In that case, trial assists are configured in GAIC \(sys\_gen\_ai\_license \_metadata\_trial\) and set as trial assists. This needs to be changed that the trial assists should still be charged as real assists when inserting into sys\_gen\_ai\_usage\_log.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1855393

</td><td>

User KnowledgeGraph data should be applied for search

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1855479

</td><td>

Intermittent lock version mismatch for conversation ID in Conversation Catalog

</td><td>

The user experiences intermittent "Lock version mismatch" errors when executing the Conversation Catalog in the Service Portal, causing abrupt conversation terminations.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1855555

</td><td>

Bot exits with an error when a query contains double quotes

</td><td>

When any query with double quotes is entered in the chatbot, it exits immediately with the below message: "Sorry, there was a problem on my side trying to complete this request. Try asking again later."

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1856043

</td><td>

Add the LLMProxy and LLMProxy-GeoLicensed and DynamicTranslation sys\_service records

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1856309

</td><td>

Create a metadata table for AI agents's skill discovery

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1856323

</td><td>

An NSA admin user is unable to switch LLMs

</td><td>

The issue exists during activating a skill.

</td><td>

1.  Impersonate with an NSA admin user.
2.  **Now Assist admin** &gt; **Settings** &gt; **Manage LLMs**.
3.  Switch the LLM from Azure to Now LLM.
4.  Verify the success modal.
5.  Verify the 'sys one extend capability' table.
6.  Observe that no capability is switched.

 Expected behavior: An NSA admin user unable to switch the LLMs.

 Actual behavior: An NSA admin user should be able to switch the LLMs.

</td></tr><tr><td>

Virtual Agent

 PRB1856492

</td><td>

Chat bot errors out due to a mismatched lock version

</td><td>

The chat bot errors out and exits the chat.

</td><td>

1.  In a chat bot conversation, enter the query: "General Request for a Storage VM" to request this catalog item.
2.  Go through the flow.

 Observe that bot throws the error, 'Syslog error: Lock version mismatch for conversationId 14c1dcb92b371a 1009f2f22ffe91bf1c - expected 13 and encountered 14'.

</td></tr><tr><td>

Virtual Agent

 PRB1857085

</td><td>

Fallback with create incident with a Virtual Agent \(VA\) conversation gets stuck

</td><td>

The NAVA fallback option is 'Record producer' with 'Create incident using VA'.

</td><td>

1.  On NAVA, search for 'I need Miro'.
2.  After synthesized response is returned, select **Show more** to see the fallback option.
3.  Select **Create incident** using VA.

 Expected behavior: Incident creation is completed.

 Actual behavior: The conversation gets stuck and there are errors in the log.

</td></tr><tr><td>

Virtual Agent

 PRB1857219

</td><td>

Skill discovery fails on xselfservice upgraded instance

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1857900

</td><td>

A deflection log table doesn't set a 'no response' state when AI Search returns 'no answer found'

</td><td>

 

</td><td>

1.  Navigate to NAVA.
2.  Type in a search term that has no synthesized result and no regular result.
3.  Navigate to the deflection log table \(sys\_cs\_deflection\_log\).
4.  Check the record corresponding to this search.

 Notice that the **State** field isn't set to 'no response'.

</td></tr><tr><td>

Virtual Agent

 PRB1858305

</td><td>

GAIC doesn't handle response max tokens of NULL for sys\_generative\_ai\_config

</td><td>

If sn\_vad\_genai.com. glide.cs.one\_extend .auto\_proxy\_enabled is set to false, the issue isn't reproducible.

</td><td>

1.  Provision an instance with Now Assist For Creator \(nowassist-creator\) plugin version 27.1.1 installed.
2.  As a user with elevated privileges, open Service Now Studio.
3.  Select **NAP** in ServiceNow Studio.
4.  Type anything as a prompt. For example, 'I want to create an app to track new employee hires'.

 Expected behavior: Users get a response from the LLM.

 Actual behavior: There's a GAIC Error complaining about missing data.

</td></tr><tr><td>

Virtual Agent

 PRB1858954

</td><td>

Follow-up after a navigation skill isn't working

</td><td>

 

</td><td>

1.  Select **NAP**.
2.  Enter 'show me list of unassigned incidents'.
3.  Select **incident**.
4.  Enter 'show list of open incidents'.

 Observe that a processing message keeps loading and no response is displayed.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1847374

</td><td>

Messages in the user chat box are hard to read

</td><td>

 

</td><td>

1.  Navigate to NAVA.
2.  Open the chat.

 Observe that messages like 'Click here to start' inside the user typing box are almost unreadable.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1861185

</td><td>

An animated icon isn't visible in NAVA when enabled

</td><td>

 

</td><td>

1.  Enable sn\_nowassist\_va.nass \_animated\_avatar\_enabled.
2.  Navigate to NAVA.
3.  Type an utterance like 'what is spam'.

 Expected behavior: An animated icon is visible next to the loading messages.

 Actual behavior: No icon loads next to loading messages.

</td></tr><tr><td>

Walk-Up Experience

 PRB1848443

</td><td>

A badge reader throws an error: 'Could not find location queue associated with badge reader'

</td><td>

Starting from Xanadu, users who have the badge reader configuration set up are facing the issue where it states 'Could not find location queue associated with badge reader', even though there is a location queue defined with the badge reader.

</td><td>

1.  Log in as an admin.
2.  Run the badgeReaderAPI.

 Expected behavior: The API should give a success message: 'User has been checked in'.

 Actual behavior: The API is throwing 'Could not find location queue associated with badge reader', even though there is a location available.

</td></tr><tr><td>

Word Document APIs

 PRB1840050

</td><td>

The Docx4j version should be updated to support ServiceNow WordDocumentAPIs after a recent update of Microsoft Office Word 16.91

</td><td>

There's a new XML tag that is added in to docx format by Microsoft. The respective docx4j library has updated \(8.3.13\), which has to be updated in the WordDocumentAPIs services.

</td><td>

1.  Create a Word template document with MS Office Word with the 16.91.x version.
2.  Add it to the 'Contract' template.
3.  Parse it.
4.  Initiate a contract with this template document.

 Observe that the document is generated, but if it's downloaded and opened, it displays the document as corrupted.

</td></tr><tr><td>

Work Order Management

 PRB1838614

</td><td>

Logic fails to check for conflicts if the assignment group selected on the work order task \(WOT\) contains multiple group types

</td><td>

The business rule date checks for table sm\_task fails to correctly check for conflicts if the assignment group on the WOT contains multiple group types.

</td><td>

1.  Impersonate a dispatcher and assign a task to an agent in a group with multiple types.
2.  Assign a second task to the same agent at the same time.

The time-conflict that should be displayed isn't displayed.

3.  Unassign the task assigned in step 2.
4.  Remove one of the types from the agent's group.
5.  Execute step 2 again.

 The assignment fails because of the conflict.

</td></tr><tr><td>

Work Order Management

 PRB1839337

</td><td>

The time displayed in the 'Task' panel and CSP is in the UTC format

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Navigate to DWS.
3.  Select any work order task \(WOT\) from the 'Task' panel and verify the scheduled start date and time.
4.  Open the same WOT in a record page and verify the scheduled start date and time.
5.  Select a WOT from the 'Calendar' panel and hover over it to verify the scheduled start date and time displayed.
6.  Select the WOT and verify the scheduled start and time displayed in the CSP.

 Observe that the time displayed in 'Task' panel as well as the CSP is converted to UTC time instead of the user's timezone.

</td></tr><tr><td>

Work Order Management

 PRB1841899

</td><td>

Observe higher response times for dispatcher workspace transactions during 1x load test

</td><td>

When executing a 1x load test with WFO data, the response times of few transactions are above SLA.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1842749

</td><td>

Remove client callable script include

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1853746

</td><td>

Unable to source a part from the part requirement flow from Work Order Tasks \(WOT\) in the Mobile Agent App

</td><td>

An error message occurs when the user sources a part in the part requirement flow from Work Order Task for Field Service Management \(FSM\) in the Mobile Agent App.

</td><td>

1.  Navigate to **All** &gt; **system logs** &gt; **Emails** &gt; **Open recent email** for a user with the role wm\_agent.
2.  Select **Enter**.
3.  Log in as the user with the wm\_agent role on the Mobile Agent App.
4.  Navigate to **My Work** &gt; **My Tasks**.
5.  Select a work order task \(WOT\).
6.  Navigate to **Parts** &gt; **Part Requirements** &gt; **.**
7.  Select **Create Part Requirement**
8.  Enter 'Model: 3Com Cat 5 Cable \(10ft\) Quantity: 1'.
9.  Select **Submit**.
10. Open the newly created part requirement.
11. Select **Find Part**.
    1.  Enter 'Enter Radius: 50000'.
    2.  Select **Search**.
12. Notice that that it navigates to the Map Screen.
13. Select on the **Asset**card.
14. Select **Source Part**.
    1.  Enter 'To Stockroom: Personal Stockroom'.
    2.  Enter 'Quantity: 1'.
    3.  Select **Submit**.

 Expected behavior:It should be submitted and the success message, 'Parts have been sourced, and transfer orders have been created' should be seen.

 Actual behavior: Issue: Notice the error message, 'Source part failed'.

</td></tr><tr><td>

Work Order Management

 PRB1853754

</td><td>

Schedule conflicts aren't displayed for wm\_manager when the contractor management plugin is installed

</td><td>

A conflict error message should be displayed when scheduled Work Order Tasks \(WOT\) conflict and are assigned to the same user with the wm\_manager role.

</td><td>

1.  Provision an instance with the Field Service Management Contractor Management plugin installed.
2.  Create a WOT.
3.  Assign the WOT to a wm\_manager.
4.  Create another task that conflicts with the previous task.
5.  Assign the WOT to a same wm\_manager.

 Expected behavior: The conflict error is displayed.

 Actual behavior: The conflict errors aren't displayed.

</td></tr><tr><td>

Work Order Questionnaires

 PRB1836194

</td><td>

Removal of sn\_smart\_asmt.assessment\_admin from inherited roles of questionnaire\_admin

</td><td>

This is a product update.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Yokohama EA Hotfix 1](yokohama-patch-0-hf-1-PO.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


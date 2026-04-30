---
title: Yokohama Patch 2
description: The Yokohama Patch 2 release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-04-04"
reading_time_minutes: 43
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# Yokohama Patch 2

The Yokohama Patch 2 release contains important problem fixes.

-   **Yokohama Patch 2 was released on April 4, 2025.**
    -   Build date: 04-02-2025\_0516
    -   Build tag: glide-yokohama-12-18-2024\_\_patch2-03-20-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y02.00.xlsx).

## Overview

Yokohama Patch 2 includes 159 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-yp2.png "Top 10 problem categories")

## Security-related fixes

Yokohama Patch 2 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Yokohama Patch 2, refer to [KB2002785](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2002785).

## Changes in Yokohama Patch 2

-   **[Create a decision tree for troubleshooting a failed transaction](https://www.servicenow.com/docs/access?context=create-decision-tree-credit-card-transaction-failure&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Question font sizeEnter the desired font size for the questions in the guided decision tree. Example: `14`

-   **[Create a guidance in the Core UI](https://www.servicenow.com/docs/access?context=create-guidances&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Hide completed guidance

    Hides the guidance recommended for a case resolution.

    In other words, the completed guidance in the View my response section of a Decision Tree is not displayed for the agent.

    **Note:** This field is visible only when the Guided Decision Experience plugin is installed. You may need to configure the form to add this field.

-   **[Create a decision tree in Core UI](https://www.servicenow.com/docs/access?context=configure-decision-trees-gdb&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Question font size

    The font size of the questions in the guided decision tree. It reflects in the workspace and service portal.

    The font size defined in the parent decision tree is inherited by the child decision tree even though the Question font size for the child decision tree has its own Question font size defined.

    You may need to configure the form to add this field.

-   **[Create a guidance in Recommended Actions](https://www.servicenow.com/docs/access?context=ra-csm-guidances-create&version=yokohama&pubname=yokohama-customer-service-management&ft:locale=en-US)**

    Select **Hide completed guidance** to hide the guidance recommended for a case resolution.

-   **[Exploring Instance Data Replication](https://www.servicenow.com/docs/access?context=exploring-instance-data-replication&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    You can only create one scheduled replication set in IDR, with only one outbound entry in that set.

-   **[Set up scheduled replication](https://www.servicenow.com/docs/access?context=set-up-scheduled-replication-idr&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)**

    You can only create one scheduled replication set, with only one outbound entry in that set.

    If a table that you select has child tables, create one or more continuous replication sets and add outbound entries for each child table to maintain data integrity.


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

User Criteria for Service Catalog

 PRB1819841

</td><td>

Semaphore exhaustion is caused by the getAllUserCriteria function getting called in widgets

</td><td>

When a public page is accessed by a guest user or web crawler, this prompts a call to the getAllUserCriteria API, which causes semaphore exhaustion.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1839341

 [KB1891818](https://hi.service-now.com/kb_view.do?sysparm_article=KB1891818)

</td><td>

**Update Set with Playbook** change failed to install

</td><td>

The invalid preview error, 'Could not find a record in sys\_pd\_snapshot for column snapshot referenced in this update' occurs when moving changes to related to Playbook via update set from one instance to another.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1825217

 [KB1709497](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709497)

</td><td>

When applying inline scripting to pass the value in an input of a dynamic template, it's not working, and the field appears empty

</td><td>

When users create a new action from scratch with one input of a dynamic template and apply inline scripting to pass the value to this input in the flow, it doesn't work.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1859358

 [KB1968830](https://hi.service-now.com/kb_view.do?sysparm_article=KB1968830)

</td><td>

The orphan cleaner does not check both the primary and archive tables to determine if a record is an orphan

</td><td>

Orphan cleaner is enabled by setting property 'glide.db.orphan\_cleaner.peripheral\_tables' to clean records from the peripheral tables sys\_attachment, sys\_attachment\_doc, and sys\_audit, sys\_journal\_field. It only checks if a record exists based on the document ID reference's tablename. When the document ID reference's tablename is not updated after archiving records during archive reparenting, the orphan cleaner deletes non-orphan records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Standard Change Catalog

 PRB1856886

 [KB1931818](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1931818)

</td><td>

**Value** is not populated from the template if a new text area field is added when creating or modifying a standard change proposal

</td><td>

The **template\_value** field contains 'STARTSWITH' instead of the '=' operator, which doesn't allow the field to be populated with the value when the template is applied to the change request record.

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

 PRB1858896

</td><td>

Posts generated by Agentic AI or Now Assist should be posted as an 'AI' user vs ServiceNow

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1857820

</td><td>

Agent Outside Workspaces that use OpenFrame soft phone are set to an 'Offline' presence state within a minute after the agent moves to an available state

</td><td>

If an agent isn't also on a workspace, the presence reverts to 'Offline' within about a minute. Since the agent is using OpenFrame to manage capacity, it shouldn't automatically revert to 'Offline'. The issue occurs after an Xanadu upgrade.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1858547

</td><td>

Flow Designer interactive mode should be base instance for phone, video, chat, and messaging service channel types

</td><td>

 

</td><td>

1.  Install agent chat and external AWA plugins. Do not add or change the com.glide.awa.external\_event\_interactive\_channels property value.
2.  Implement an external provider or use the demo data provider.
3.  Set up an external queue on a 'Chat' type service channel.
4.  Route a chat, then check the resulting flow context.

 Expected behavior: The 'new' and other external event subflows that are executed should indicate that they were run in interactive mode.

 Actual behavior: The subflows are executed using the standard FDIH jobs, not in interactive mode.

</td></tr><tr><td>

AI Search

 PRB1849325

</td><td>

thumbnailHeader in the mini Genius Result Card is not translated

</td><td>

This problem occurs in both global and portal search.

</td><td>

1.  Enable AI Search.
2.  Ensure the instance has Now Assist Q&amp;A enabled.
3.  Turn on translation prefix in **All** &gt; **System Localization**.
4.  Search the query 'request computer' in either global or portal search.
5.  Wait for Genius Results to load.

 Notice that the thumbnailHeader in the mini Genius Result cards are not tagged with the translation prefix except for 'Catalog'.

</td></tr><tr><td>

AI Search

 PRB1850218

</td><td>

ais\_child\_table cache is not flushed when glide.ais.disable\_kbb property is changed

</td><td>

KBBs \(knowledge blocks\) should not be indexed as separate document. Instead, they are indexed with the KB document as embedded documents. When only KBB is enabled, the KBB table is removed from the tables.

</td><td>

1.  Enable the knowledge block \(KBB\) flag.
2.  Navigate to cache\_inspect.do.
3.  Check that CACHE\_AIS\_CHILD\_TABLE has kb\_knowledge\_block.
4.  Disable the flag.
5.  Index kb\_knowledge datasource.

 Observe that the KBB is indexed as separate documents.

</td></tr><tr><td>

AI Search

 PRB1851725

</td><td>

Typo Handling blocked terms state doesn't change from **New** to **Published** when publishing a search profile

</td><td>

Blocked terms are published, and the UI did not change the state from **New** to **Published**.

</td><td>

1.  Add a new blocked term to the Typo Handling dictionary.
2.  Publish the parent profile.

 Observe that the new term still has a **New** state, the blocked term is actually published, but the UI did not change the state.

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

AI Search

 PRB1861957

</td><td>

Duplicate migration requests for a model upgradation is allowed for same target version of a model upgrade request

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1863971

</td><td>

RAGRertirval API throws an error if the searchSource given request is not present

</td><td>

When the user submits a RAGRetrieval API request with a search source that is not part of the search profile or is not an indexed source, RAGRetrievalAPI fails with no search results.

</td><td>

 

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

Appointment Booking

 PRB1853892

</td><td>

When the daily capacity is reached, the appointment booking modal shows a slot for that day, but throws an error upon booking

</td><td>

Even though the capacity definition is set, appointment slots still appear even if the day if fully booked. When a user attempts to book an appointment on a fully booked day, the error 'ErrorAppointment window is no longer available. Please select another appointment' occurs.

</td><td>

1.  Create a capacity definition of type, **Task and 1 task** as capacity.
2.  Tag the definition to an assignment group for a 20 day period.
3.  Create a Work Order Task \(WOT\).
4.  Assign the task to an agent in the assignment group.
5.  Notice that capacity usage records recorded that '1 out of 1 task' is used.
6.  Log into the CSM portal.
7.  Attempt to book an appointment for the same catalog.

 Expected behavior: Since the capacity is already booked for that particular day, slots should not appear.

 Actual behavior: Slots are visible for that day and upon booking, and the page throws as error 'ErrorAppointment window is no longer available. Please select another appointment'.

</td></tr><tr><td>

Appointment Booking

 PRB1860174

</td><td>

The appointment calendar does not work in **Request a replacement catalog**

</td><td>

**Select appointment** is displayed as blank.

</td><td>

 

</td></tr><tr><td>

Appointment Booking

 PRB1860844

</td><td>

In Portal, when unified UI and week view is enabled, if a holiday falls in the next week, that holiday isn't considered

</td><td>

When **Consider holidays** in leadtime is checked in at the service configuration level, the holidays aren't honored properly to recalculate the leadtime. Users are still seeing the slots in the next week.

</td><td>

1.  Enable unified UI and week view.
2.  Set the lead time such that slots are available from next week.
3.  Create a holiday in next week.

Observe that the holiday isn't considered in this case and slots are shown for holidays as well.

4.  Set **Consider holidays** for the lead time flag as true and set a holiday within a lead time.

Observe that the holiday isn't considered for lead time calculation.


</td></tr><tr><td>

Cache

 PRB1860082

</td><td>

CacheMetricsManager causes a performance bottleneck at high workloads

</td><td>

Enhance the performance of the Cache Metrics API to accommodate a high volume of concurrent requests.

</td><td>

 

</td></tr><tr><td>

Calendar Component

 PRB1837613

</td><td>

A robot calendar isn't working on Y trueup instances

</td><td>

On nightly builds, the robot calendar isn't loading and timezones aren't associating with the calendar.

</td><td>

1.  Navigate to an instance.
2.  Navigate to a workspace.
3.  Open a robot linked to a bot process.
4.  Select the **Robot calendar** button.

 Expected behavior: The calendar should be loaded to show the schedules of robots.

 Actual behavior: The calendar doesn't load.

</td></tr><tr><td>

Capacity and Reservations Management

 PRB1847774

</td><td>

There's a performance issue in the capacity console

</td><td>

For **Group by demand channel**, all territory data is fetched for the expanded demand channel. When adding a customization function for a summary, the event alt text should be labeled but it'd coming as a field name.

</td><td>

 

</td></tr><tr><td>

Cloud Provisioning and Governance

 PRB1852065

</td><td>

Stack state is changed to**Terminated** when deployment fails, and no task is created

</td><td>

The stack status is changed to **Terminated** instead of **Resolving Error**.

</td><td>

1.  Log in to an instance.
2.  Create an Azure Resource Manager \(ARM\) or Cloud Formation Template \(CFT\) catalog.
3.  Navigate to the ESC Portal.
4.  Launch the CFT catalog created.
5.  Provide all required parameters and give any invalid values.
6.  Order the catalog.

 Observe that if deployment fails, stack status is changes to **Terminated** instead of a **Resolving Error**PFA.

</td></tr><tr><td>

CMDB CI Class Manager

 PRB1845236

</td><td>

Update CMDB table descriptions based on current documentation

</td><td>

The CMDB table descriptions are not updated based on current documentation.

</td><td>

1.  Navigate to CI \(configuration item\) class manager.
2.  Select any class.
3.  Open the Info tab.

 Notice that the descriptions are not updated based on the current CMDB table description documentation on the ServiceNow Documentation site.

</td></tr><tr><td>

Code Signing

 PRB1857413

</td><td>

Signatures created by **Signing** jobs have the **update\_name** field empty

</td><td>

 

</td><td>

Run the **Signing** job to generate a signature for records.

 Expected behavior: Generated signatures should populate the **update\_name** field.

 Actual behavior: The **update\_name** field is empty for a generated signature. This prevents records from Git check-in and the 'Publish to App' repo.

</td></tr><tr><td>

Code Signing

 PRB1857416

</td><td>

Signatures created by signing jobs have an empty **update\_name** field

</td><td>

The record field **update\_name** is empty for generated signatures to prevent records from being checked in to git and to be published to the App repo. Generated signatures should populate the 'update\_name' field.

</td><td>

Run a signing job to generate a signature for the record field **update\_name**.

</td></tr><tr><td>

Customer Service Management

 PRB1855041

</td><td>

Unable to create an email draft in an application scope

</td><td>

The sys\_email\_draft table has table-level access limitation. Only **Can Read** is allowed in the application scope.

</td><td>

1.  **AI Agent** &gt; **Testing**.
2.  Select the AI agent **CSM Response Handler.**
3.  Enter the task detail as:
    1.  record\_table = 'sn\_customerservice\_case'
    2.  record\_sysid = '5078cc9a2be71210f980f0aef291bf0b'
    3.  email\_reply\_content = 'We can't complete this case until missing fields and missing documents are added'

 Observe the email response tool 'Draft Email' returns an error message 'Email draft is failed created'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1857656

 [KB1935234](https://hi.service-now.com/kb_view.do?sysparm_article=KB1935234)

</td><td>

A Glide function with a substring function may return a 'negative substring length not allowed' error if the arguments are negative

</td><td>

A Glide function with a substring function may return a 'General Data Exception detected by database \(ERROR: negative substring length not allowed\)' error if the arguments are negative.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1844907

</td><td>

Orphan Archive Related Records \(sys\_archive\_related\) with empty **Archive\_Map** values are not ignored by the archive job

</td><td>

When instance has orphaned archive related records, the archive job does try to find orphan related records, and archives them as a part of the archive run being processed by the archive job. Archive related records should not be created without an archive\_map defined, and every archive related record should be linked to an archive rule.

</td><td>

1.  Log in to the instance.
2.  Create a new archive rule on incident with any conditions.
3.  Add an archive related record for **incident\_task**.
    1.  Save the archive rule.
    2.  Delete the new archive rule.
    3.  Notice the archive related record becomes orphaned.
4.  Create a parent incident.
    1.  Create a new incident task for the incident.
    2.  Create a new incident with the parent incident created, where the relationship is incident.parent\_incident.
    3.  Create incident tasks for this new incident.
5.  Create a new archive rule on incident with conditions so that it archives the previously incident created, so that if the parent incident is archived, the child incident will also be archived.
6.  Create an archive related record for the archive rule created with the metadata:
    1.  Action – archive.
    2.  Reference – incident.parent\_incident.
    3.  Reference table – Incident \[incident\].
    4.  Reference element – parent\_incident
    5.  Reference table rule – empty.
7.  Activate the new archive rule created.
8.  Run it.
9.  Notice it will archive both incidents created as expected, but it also archives the incident task created in the parent incident due to the orphan incident task sys\_archive\_related.

 Expected behavior: The archive job should ignore invalid archive related records, and only linked archive related rules should be picked up and processed.

 Actual behavior: The archive job is finding and processing orphaned archive related records for all the archive rules the job runs.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1850816

</td><td>

z\_tmp tables should not be eligible for compaction

</td><td>

Compaction is running on z\_tmp tables when they should not be.

</td><td>

Generate a z\_tmp table that is eligible for compaction.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1854621

</td><td>

Archive reparenting issue occurs when sys\_attachment is configured as a related record for an archive rule

</td><td>

The table name 'incident' remains instead of being renamed to 'incident\_task' after running the archive rule.

</td><td>

1.  Create an archive rule for the **incident** table.
2.  Define archive the related records incident\_task and sys\_attachment.
3.  Set up test data.
    1.  Ensure incident\_task records references incident.
    2.  Ensure sys\_attachment records references incident and incident task.
4.  Run the archive rule.
5.  Verify that both incident and incident tasks are moved to ar\_incident and ar\_incident\_task.
6.  Check that the sys\_attachment records reference to the incident record are moved to ar\_system\_attachement.
7.  Check that the sys\_attachment records for the archived incident\_task,

 Notice that the table name is still 'incident' instead of 'incident\_task'.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1855929

</td><td>

Investigating sys\_attachment records that are not reparented correctly in Vancouver

</td><td>

Reparenting issue for records in sys\_attachment in the gateway DB.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1859358

 [KB1968830](https://hi.service-now.com/kb_view.do?sysparm_article=KB1968830)

</td><td>

The orphan cleaner does not check both the primary and archive tables to determine if a record is an orphan

</td><td>

Orphan cleaner is enabled by setting property 'glide.db.orphan\_cleaner.peripheral\_tables' to clean records from the peripheral tables sys\_attachment, sys\_attachment\_doc, and sys\_audit, sys\_journal\_field. It only checks if a record exists based on the document ID reference's tablename. When the document ID reference's tablename is not updated after archiving records during archive reparenting, the orphan cleaner deletes non-orphan records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1840597

</td><td>

Admins are unable to see the rollback record fields

</td><td>

After installing the data privacy application, security ACLs were installed for the sys\_rollback\_context table. The user is unable to see anything in the table even though they have admin access.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1850400

</td><td>

End user cannot use Privacy APIs to redact sensitive data during chat session

</td><td>

An error in the logs occurs and the message is unable to send, when chat messages should say, 'Message not send as it contains sensitive data'.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1860779

</td><td>

True-up licensing app

</td><td>

This problem is for true-up licensing.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1855732

</td><td>

DocIntel is not working properly after being trained

</td><td>

 

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
3.  Navigate to the ServiceNow instance.
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

 Expected behavior: The user gets the entire response in Spanish.

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

Employee Center Pro

 PRB1814341

 [KB1704519](https://hi.service-now.com/kb_view.do?sysparm_article=KB1704519)

</td><td>

The 'Give Feedback' text in Experience Feedback Drawer widget is upside down for the Chinese/Japanese/Korean languages

</td><td>

All the vertical languages are considered and are read from top to bottom.

</td><td>

1.  Install EC Pro.
2.  Install Chinese, Japanese or Korean languages.
3.  Switch to the above installed language.
4.  Open /esc?id=hri\_user\_profile.

 Expected behavior: The 'Give feedback' text displays vertically.

 Actual behavior: The 'Give feedback' text displays upside down.

</td></tr><tr><td>

Event Management

 PRB1829897

</td><td>

**Description** field of the Event Rule transform tab execute JavaScript code

</td><td>

In cases when the Event has spacial characters, using the marker for those inputs won't work and the regular expression has to be written manually.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1852761

</td><td>

NullPointerException \(NPE\) in Impact Calculation after topology change

</td><td>

NPE occurs after performing a topology change in Event Management.

</td><td>

1.  Navigate to Application Services.
2.  Navigate to ServiceNow Event Management.
3.  Select **View Map**.
4.  Add a Linux \(lnux100\) server under Alert Processing.
5.  Send a minor alert on lnux100.
6.  Select the Impact Tree.
7.  Navigate to **Impact Calculation** &gt; **Impact**.
8.  Change the influence for impact rule to 50 to perform a topology change.

 Observe the following NPE, 'Exception at executeImpactCalculation. Msg: Cannot invoke 'java.lang.Integer.toString\(\)' because 'this.fContributedSeverity' is nulllastImpactCalcDate: nullImpactSyncHandler'.

</td></tr><tr><td>

External Triggers

 PRB1848664

</td><td>

Change the spoke sys\_id to the spoke ID in the definition for external triggers telemetry

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1825217

 [KB1709497](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709497)

</td><td>

When applying inline scripting to pass the value in an input of a dynamic template, it's not working, and the field appears empty

</td><td>

When users create a new action from scratch with one input of a dynamic template and apply inline scripting to pass the value to this input in the flow, it doesn't work.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1828174

 [KB1709903](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709903)

</td><td>

Do-In-Parellel branch remains on a 'Waiting' state after MID action

</td><td>

Flow should go to a 'Complete' state after it returns from MID, but it remains in a 'Waiting' state with only one of the parallel branches having been executed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1865703

</td><td>

Support retries for interactive, non-quick flows

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

GRC Platform Plugins

 PRB1843595

</td><td>

The **Details** field is missing in Attestation Designer after Xanadu upgrade

</td><td>

The**Details** field is missing in the attestation designer after the upgrade to Xanadu from Washington.

</td><td>

1.  Navigate to attestation designer.
2.  Select the gear icon for any of the questions.

Observe that no **Details** field is present.

3.  View the same attestation designer in a Washington DC instance.

 Observe that the **Details** field is present.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1854275

</td><td>

Risk Assessment Designer doesn't launch or open a saved assessment

</td><td>

The session hangs and causes the browser to time out when using Risk Assessment Designer.

</td><td>

1.  Impersonate a user.
2.  Enter assessment types in the Filter Navigator.
3.  Navigate to **GRC Risk** &gt; **Administration** &gt; **Assessment Types**.
4.  Open an Assessment.
5.  Select **Risk Assessment Designer UI**.
6.  Notice that the session hangs and eventually causes the browser to time out.
7.  Close the browser.
8.  Wait two minutes.
9.  Relaunch the browser.
10. Impersonate the same user.
11. Enter assessment types in the Filter Navigator.
12. Navigate to **GRC Risk** &gt; **Administration** &gt; **Assessment Types**.
13. Select **Risk Assessment Designer UI** from the list.
14. Select **New Assessment New Assessment Load Assessment** &gt; **Load Assessment** when the designer opens.
15. Search for the assessment in the search modal.

 Notice that it hangs and eventually times out the session.

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1846612

</td><td>

MID server stops when it fails to format a log message

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1836241

</td><td>

Topic sync deactivates topics when the topic is deleted

</td><td>

The topic sync job deactivates a topic when it is known and not in one cluster.

</td><td>

1.  Create a topic via sys\_kafka\_topic.
2.  Delete the topic from one cluster via command-line interface \(CLI\).
3.  Run the sync job.

 Notice that the sys\_kafka\_topic record has 'active' = false.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1849037

</td><td>

Backport revert of glide.graphql.gliderecord.maxResults.limit

</td><td>

The property ensures the GraphQL engine is not overconsuming resources for GlideRecord\_Query requests.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1856357

</td><td>

syncTopics sets service incorrectly on non-managed clusters

</td><td>

Topic sync job will attempt to get topic metadata on some clusters and will run into an error.

</td><td>

Run topic sync job using any non-default cluster.

 Notice the error, 'Note that the topics will eventually be synced through updateKnownTopicsAndNotify\(\)'.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1857188

</td><td>

When DISH sends back an empty response for a Hermes Service \(e.g, MIF-Hermes\) the preexisting hermes\_cluster\_config records are not cleared

</td><td>

Instances connected that have called the Hermes callback listener and set up the hermes\_cluster\_config table cannot be removed by returning an empty response to those instances from MIMIR.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1819942

</td><td>

HTML tags are seen in the **Description\(description\)** field of an HR case

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Inbound Email Actions

 PRB1841147

</td><td>

Sensitive data redaction problem

</td><td>

This issue impacts inbound email actions even if 'stop processing' is enabled.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1829495

</td><td>

High turn around time to send scheduled seeding through metadata topic

</td><td>

After schedule seeding data has been processed, the system should not send data to the consumer and block the metadata topic.

</td><td>

1.  Create a schedule seeding replication set for a 12 hour interval.
2.  Load data up to 3 mil.
3.  Verify turnaround time grows with large amounts of data.

 Expected behavior: Once data is processed, the turnaround time should be quick.

 Actual behavior: The turnaround time is long.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1829496

</td><td>

**Retry** shows duplicate run log records

</td><td>

When **Retry** is initiated, the DCT result and run log should not have duplicates.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1858358

</td><td>

Excessive KMF traffic on some instances

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1863650

</td><td>

There is a limit to sets and entries

</td><td>

One replication set with one outbound entry can be scheduled for Yokohama. Scheduled seeding should work for five replication sets each with a single outbound entry.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1839006

 [KB1952753](https://hi.service-now.com/kb_view.do?sysparm_article=KB1952753)

</td><td>

OpenAPI Step with MID is failing

</td><td>

When following the OpenAPI Step document to create an action to make an API to an OpenAPI Step, a Guice configuration error occurs.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Integration Hub

 PRB1865702

</td><td>

Support Retry policy when using Async HTTP

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Issue Auto Resolution for Virtual Agent

 PRB1862157

</td><td>

IAR Simulation does not use the correct API

</td><td>

Custom intents are returned when the regular IAR flow is executed. Custom intents are not returned when simulation is used, because the API takes in a list of objects instead of a single object. The simulation feature is using the single prediction instead of the bulk one, so the custom IAR's are not being returned.

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

Knowledge Article Templates

 PRB1852356

</td><td>

Articles in the 'Published' state are not changed state to 'Pending retirement' when retired

</td><td>

Knowledge Base \(KB\) articles that have the retire policy set to 'Knowledge - Approval Retire' cannot be changed to the state 'Pending review'. This problem is found in Yokohama.

</td><td>

1.  Locate any KB that has the retire policy set to 'Knowledge - Approval Retire'.
2.  Find any article in the 'Published' state within that KB.
3.  Select **Retire action**.
4.  Select **No** in the pop up dialog for the option to replace the current article with a new article.
5.  Return to the article.

 Notice that the workflow state has not been updated yet.

</td></tr><tr><td>

Knowledge Management

 PRB1827639

</td><td>

Selecting a knowledge base from 'Explore our Knowledge Bases' in a portal redirects to the wrong URL

</td><td>

A strange URL with incorrect seach results is returned when selecting a knowledge base from /esc?id=kb\_home with AI Search enabled on the application 'Knowledge Management - Service Portal' version 1.0.0.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1849608

 [KB1906766](https://hi.service-now.com/kb_view.do?sysparm_article=KB1906766)

</td><td>

Knowledge Management \(KM\) notifications are unable to be triggered

</td><td>

Email notifications aren't triggered for Knowledge Articles because some KM artifact records in the Knowledge Advance plugin are overridden by the Activity Subscription plugin. This occurs in Xanadu and Yokohama.

</td><td>

1.  Select any Knowledge Base \(KB\) that is under subscription.
2.  Publish any Knowledge Article from the KB.
3.  Notice that the published article is not triggered to the subscriber in the KM subscription.
4.  Attempt to trigger the published article by navigating to **Notification** &gt; **Related list** &gt; **Email log**.

 Notice that the notification is not getting triggered for 'KM Subscription: Article published'.

</td></tr><tr><td>

List Administration

 PRB1866920

</td><td>

Support export to Google sheets functionality in UI16

</td><td>

This is a product enhancement.

</td><td>

 

</td></tr><tr><td>

List Controller

 PRB1826487

</td><td>

Record watcher stops working if more than 1000 records exist in the query

</td><td>

Records don't appear on the list if there are more than 1000 records.

</td><td>

1.  Create a list.
2.  2. Toggle the 'Live' list to be on.
3.  3. Create new record or wait for new record to appear in the list.

 Expected behavior: When a new record is created, it should appear on the list.

 Actual behavior: The new record doesn't appear because the list contains more than 1000 records.

</td></tr><tr><td>

MID Server

 PRB1840424

 [KB1772428](https://hi.service-now.com/kb_view.do?sysparm_article=KB1772428)

</td><td>

MID Server ECCSender thread gives an 'Invalid byte 2 of 4-byte UTF-8 sequence' error, blocking sending of valid ecc\_queue inputs to an instance

</td><td>

This is most likely to be seen in LDAP user imports, or Import Set JDBC Data Sources, where large data is involved. Large data is likely to include extended unicode characters such as emojis. For LDAP probes, emojis have been seen in OU/CN group names and user details data. For REST integrations synching incidents, emojis have been seen in comments of cases. They could potentially appear anywhere, for any feature's probe result data.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1840424

 [KB1772428](https://hi.service-now.com/kb_view.do?sysparm_article=KB1772428)

</td><td>

MID Server ECCSender thread gives an 'Invalid byte 2 of 4-byte UTF-8 sequence' error, blocking sending of valid ecc\_queue inputs to an instance

</td><td>

This is most likely to be seen in LDAP user imports, or Import Set JDBC Data Sources, where large data is involved. Large data is likely to include extended unicode characters such as emojis. For LDAP probes, emojis have been seen in OU/CN group names and user details data. For REST integrations synching incidents, emojis have been seen in comments of cases. They could potentially appear anywhere, for any feature's probe result data.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Platform

 PRB1845305

</td><td>

Issues with **Edit event** on Field Service Management mobile

</td><td>

The schedule event can't get a record from context.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1852531

</td><td>

The latency feedback messages are cut at the bottom

</td><td>

The problem likely stems from a height issue for the container.

</td><td>

1.  Navigate to NAP.
2.  Type **Summarize a record**.
3.  Check the latency feedback messages.

 Expected behavior: The message text is displayed whole in the container.

 Actual behavior: The bottom part of the messages are cut.

</td></tr><tr><td>

Now Code Editor

 PRB1813293

</td><td>

Editor Keyboard Shortcuts in i18n

</td><td>

Shortcuts are different across different editors.

</td><td>

1.  Navigate to the Script Include Page.
2.  Select **Help**.

 Observe that some are not the recommended in an A-Z alphabetical order based on i18n best practices.

</td></tr><tr><td>

Performance Analytics

 PRB1835575

</td><td>

NAM tables access changes

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1850078

</td><td>

References to deleted tables should be removed

</td><td>

Ensure that all references to deleted tables are removed from the codebase, including fix scripts, ACLs, and any other related configurations.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1862995

</td><td>

Increase the Raptor Pro limit to 30M from the current 10M on source tables

</td><td>

 

</td><td>

1.  Provision an instance with the MLB plugin installed.
2.  Try to activate NAM on tables with more than 10M records.

 Instead of an 'unsupported' message, the user should be able to activate it for up to 30M records.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1839341

 [KB1891818](https://hi.service-now.com/kb_view.do?sysparm_article=KB1891818)

</td><td>

**Update Set with Playbook** change failed to install

</td><td>

The invalid preview error, 'Could not find a record in sys\_pd\_snapshot for column snapshot referenced in this update' occurs when moving changes to related to Playbook via update set from one instance to another.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1847073

</td><td>

Questionnaire data definition and flow data variable \(questions\) are missing after duplicating a playbook

</td><td>

 

</td><td>

1.  Create a playbook.
2.  Add a lane and a questionnaire activity.
3.  Open the configuration panel and add a questionnaire \(data definition\).
4.  Add a question \(flow data var\).
5.  Save and close the configuration panel.
6.  Duplicate the playbook.

 Expected behavior: The questionnaire is duplicated.

 Actual behavior: The questionnaire isn't duplicated.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1857887

</td><td>

sys\_flow\_data\_definition is missing sys\_update\_name in sys\_update\_xml payload

</td><td>

This PR makes sys\_flow\_data\_definition use FlowDesignerSuppress which blanket returns 'true' for suppressNameAndUpdateName.

</td><td>

1.  Navigate to sys\_flow\_data\_definition.
2.  Create new record with just name.
3.  Navigate to sys\_update\_xml, sort by created.
4.  Open record for the data definition created.

 Expected behavior: The payload has non-empty sys\_update\_name and sys\_name and sys\_package.

 Actual behavior: The payload has empty sys\_update\_name and sys\_name and sys\_package.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1861572

</td><td>

Exporting a playbook between instances results in missing activities, though stages appear

</td><td>

When editing a Playbook \(sys\_pd\_process\_definition\) on Yokohama, and then exporting update sets or using source control to move the playbook to another instance, the playbook will be missing its activities. Observe that the sys\_update\_xml itself for the sys\_pd\_process\_definition is missing proper sys\_pd\_activity elements, resulting in incorrect playbooks when moving them between instances.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1861824

</td><td>

Localized UI messages are not generated on Playbook activation

</td><td>

No translation UI Messages are generated.

</td><td>

1.  Create a playbook with a few activities.
2.  Ensure each activity has a label and description.
3.  Activate Playbook.
4.  View the Process Definition record in Jelly \(sys\_pd\_process\_definition\).
5.  Select the 'Translations' related list tab.

 Expected behavior: Translation records \(UI Messages\) for Playbook label, Stage label and each Activity Label, Activity Description.

 Actual behavior: No translation UI Messages are generated.

</td></tr><tr><td>

Process Mining

 PRB1852247

</td><td>

Work Notes results shows HTML code in cluster concepts

</td><td>

Work notes are collected from sys\_journal\_field table which stores results with HTML tags.

</td><td>

1.  Initiate work notes analysis without LLM.
2.  Select **View Results**.

 Notice that HTML tags are present in cluster concepts.

</td></tr><tr><td>

Process Mining

 PRB1860897

</td><td>

Allow sample mining on an evaluation project from workbench

</td><td>

Sample mining an evaluation project works from a KPI but not from the workbench.

</td><td>

1.  Go to workbench.
2.  Attempt to sample mine.

 Notice that the user receives mining exception.

</td></tr><tr><td>

Process Mining Workspace

 PRB1832584

</td><td>

The 'Top 3 KPIs by \# records &amp; opportunities' widget always displays one record even though there are many

</td><td>

 

</td><td>

1.  Mine a project with findings attached to more than one KPIs.
2.  Observe the third widget.

</td></tr><tr><td>

Process Mining Workspace

 PRB1834072

</td><td>

**OR** conditions don't work in transitions

</td><td>

An error occurrs: 'Exception encountered processing path: /GlidePromin\_Query/scheduleModel - Relation between advanced transitions cannot be empty or NONE'.

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1834143

</td><td>

Projects have duplicate child tables shown as use cases

</td><td>

This is found with both process configuration and templates.

</td><td>

1.  Have a content pack template with child tables in the Process Details page.
2.  Import it into a custom configuration.
3.  Check the project use cases in 'Scope your analysis'.

 Observe that all tables are doubled.

</td></tr><tr><td>

Process Mining Workspace

 PRB1834213

</td><td>

On an archived data table on the 'Scope your analysis' page, activities are grouped by default

</td><td>

 

</td><td>

1.  Create a project for an archived data table.
2.  On the 'Scope your analysis page', select **Activities** &gt; **New** .
3.  Select fields like **State** and **Category**.

 Observe that the fields are grouped automatically. If users add the same field from the platform, they aren't grouped automatically.

</td></tr><tr><td>

Process Mining Workspace

 PRB1834656

</td><td>

Freemium RCA and clustering is not being disabled on Summary &amp; Insights with more than 100 records

</td><td>

In some scenarios, an error message occurs, and RCA and clustering are disabled.

</td><td>

Scenario 1:

 1.  Trigger process mining from the Freemium for KPI list.
2.  Open the 'Summary &amp; Insights' page after mining is successful.
3.  Select **Action** for opportunities with more than 100 records.
4.  Observe that the Show Records, RCA, and Clustering actions are in enabled state.

 Notice the error message, 'RCA, Clustering are disabled for the try-out project version' with the option being disabled.

 Scenario 2:

 1.  Trigger process mining from the Freemium for KPI list.
2.  Navigate to the Analyst Workbench.
3.  Select a node with less than 100k records.

</td></tr><tr><td>

Process Mining Workspace

 PRB1835539

</td><td>

Only users with elevated privileges users can see the **Copy as process configuration** button in the header in the Process Configuration template

</td><td>

 

</td><td>

1.  Log in as any user without elevated privileges.
2.  Open the process configuration template.

 Observe that process configuration does not exist, and the **Process Configuration** button in the header is missing.

</td></tr><tr><td>

Process Mining Workspace

 PRB1835680

</td><td>

Transition condition on project setup doesn't allow for the process start or end

</td><td>

Attempting to add a transition condition allow for the process start or end.

</td><td>

1.  Open any project.
2.  Scope the analysis.
3.  Attempt to add a transition condition.

</td></tr><tr><td>

Process Mining Workspace

 PRB1838225

</td><td>

**Limit control** flow fields to one for Process Configuration Guided Setup

</td><td>

Control fields should be limited to one, but multiple fields can be added.

</td><td>

1.  Open Process configuration.
2.  Navigate to **Process details** &gt; **Perspectives** &gt; **Question 1**.

 Expected behavior:The user can add only one and remove the option to group control flow.

 Actual behavior: Up to three fields can be added.

</td></tr><tr><td>

Process Mining Workspace

 PRB1839094

</td><td>

Full mining is enabled for a freemium project on the 'Project list' page

</td><td>

No users should be able to edit the evaluation project. No users should be able to delete the evaluation project\(s\). Users with a Process Mining role \(analyst, power or admin\) role can copy any project, including an evaluation project\(s\). The copied project is handled as a regular project and follows regular license check validation. No users should be able to do a full mine on evaluation project\(s\). The option shouldn't be available on UI16 and project card list

</td><td>

 

</td></tr><tr><td>

Process Mining Workspace

 PRB1842762

</td><td>

The **Go to process details** button is not working in Guided Process Configuration

</td><td>

When the user doesn't complete the Process Prospectives section, they are prompted with the message, 'No recommendations available' when creating a process configuration for a project or entity such as 'incident' after selecting 'Get recommendations'.

</td><td>

Scenario 1:

 1.  Create process configuration for 'incident'.
2.  Without completing Process Perspectives, navigate to **Improvement Opportunities** &gt; **Get recommendations**.
3.  Notice that the **Process details** button is not working.
4.  Add a textual field in process perspectives section.
5.  Return to the Improvement opportunities page.
6.  Select **Get recommendations** in the 'Automated' tab.

 Expected behavior: The message, 'No recommendations available' should be displayed.

 Actual behavior: The message, 'All recommended definitions are already included in the library' is displayed when there are actually no findings added.

 Scenario 2:

 1.  Create a process configuration without completing the Process Perspectives section.
2.  Create a project.
3.  Select **Get recommended fields**.

 Expected behavior: The message, 'No recommendations available' should be displayed.

 Actual behavior: The message, 'All recommended fields are already in use in other activity definitions' is displayed.

</td></tr><tr><td>

Process Mining Workspace

 PRB1848238

</td><td>

Transitions freeze when max constrains are set to 0

</td><td>

The max duration in the constraints set is automatically handled as 0 when not filled in. This results in 0 matched records. Second, the UI freezes when the transition as 0 records, making it impossible to set a max duration field manually. This can also happen when a filter set has a transition with an activity from a previous version, which isn't present in the current version.

</td><td>

1.  Create a project with any AD
2.  In the analyst workbench, open the **Transition** field.
3.  Configure 2 conditions/activity.
4.  Configure a constraint with
    -   Start = step 1
    -   End = step 2
    -   Min duration = 1 min
    -   max duration: Keep empty

 Expected behavior: When the max duration is left empty, the max duration should be set to infinite \(so all records longer than the min duration should match\). Also, the user should be able to use the transition UI to add/remove fields and constraints.

 Actual behavior: When applying the transition, zero records match despite some matches. The max duration fields are set to 0 rather than kept empty. Also, when zero records match the condition, the user isn't able to change anything in the transition.

</td></tr><tr><td>

Process Mining Workspace

 PRB1850566

</td><td>

Histograms show odd percentages in the pop-up values

</td><td>

 

</td><td>

1.  Mine any project.
2.  Open any node or arc.

 Observe the percentages in the modal for the values.

</td></tr><tr><td>

Process Mining Workspace

 PRB1857498

</td><td>

The **Full mining** and **Deletion** option is enabled for evaluation projects on the project list page

</td><td>

Users should not be able to edit the evaluation project except those with a role with elevated privileges. The **Edit** option in the project card list is still be visible, but users cannot save or add any new configuration in the guided setup for the evaluation project. Users with a Process Mining role \(analyst, power or admin\) can copy any project, including evaluation projects. However, users without a Process Mining role can sample mine evaluation projects such as KPI Details, Project card list, Guided setup when they shouldn't be able to do a full mine on evaluation projects.

</td><td>

1.  Notice that 'Show Record' should be enabled.
2.  Notice that 'Sample mine' on non-evaluation projects should be allowed.
3.  Mine the project **\(Sample\)' option**.

 Expected behavior: The message should be 'Full: 'Generating full model'', 'Sample 'Generating sample model'', or 'Evaluation project\(s\): 'Generating sample model''.

 Actual behavior: The mine project \(Sample\) option shows it is doing a full model when actually a sample model is taking place.

</td></tr><tr><td>

Project Management

 PRB1864892

</td><td>

The **Time Constraint** field dictionary default value does not work in Project Workspace while creating the Project Task

</td><td>

The default value for the **Time Constraint** field is set to 'ASAP' irrespective of Default value.

</td><td>

1.  Set the Default value for the **Time Constraint** field through dictionary from Project Task form.
2.  Open the Project Workspace.
3.  Open any project.
4.  Create a Project Task.

 Observe that the default value for the **Time Constraint** field is set to 'ASAP' irrespective of Default value.

</td></tr><tr><td>

RPA Hub

 PRB1848733

 [KB1826897](https://hi.service-now.com/kb_view.do?sysparm_article=KB1826897)

</td><td>

pickWorkItem component is throwing error when reducing the number of robots running automation in the robot pool

</td><td>

The pickWorkItem component throws the error, 'the object parameter passed does not contain any sys\_id attribute'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

RPA Hub

 PRB1849100

</td><td>

Ignore RPA license property default value should be 'True'

</td><td>

The property sn\_rpa\_fdn.ignore\_license\_verification should be 'true'.

</td><td>

1.  Hop into the instance as a user with elevated privileges.
2.  Open **System properties**.
3.  Open the **sn\_rpa\_fdn.ignore\_license\_verification** property.

 Expected behavior: Default value of the property should be 'True'.

 Actual behavior: Default value of the property should be 'False'.

</td></tr><tr><td>

Security Data Filters

 PRB1854682

</td><td>

Dot walks are not working as expected in Business Rules, ACLs, and UI actions in both condition builder and scripts

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Seismic Framework

 PRB1859951

</td><td>

ClientInteraction aggregate transactions creates a performance bottleneck

</td><td>

Setting glide.client\_metrics. aggregation.enabled=true on a fully loaded system will cause performance to decrease significantly.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1836577

</td><td>

Hoisting is broken within try blocks in global

</td><td>

Global throws a ReferenceError on referring to \_sortGyoBango. This was observed in Xanadu.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1847921

</td><td>

Fetch is not properly detecting the scope

</td><td>

The user receives an error about a whitelist, but it will say module.parent rather than the current scope name.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1816925

</td><td>

Service Mapping \(SM\) Discovery state always remains 'Active' if entry points are not reachable

</td><td>

When SM scheduler is run, the Discovery status for SM Discovery and end point status is created. The host is not in CMDB, so the end point status runs 'Host detection'. Host detection creates a new prob with agent\_correlator with horizontal Discovery. When host detection is finished, it updates the end point and the state becomes 'Complete'. However, SM Discovery doesn't update, so the business rule was not triggered to set the Discovery status to 'Completed'.

</td><td>

1.  Created the service with two unreachable entry points.
2.  Create scheduled discovery that runs on this service by name attribute.
3.  Run a discovery scheduler.

 Notice that the discovery state will always remain 'Active'.

</td></tr><tr><td>

Service Mapping

 PRB1851972

</td><td>

Updating the same **last\_mark** in blob table during recomputation

</td><td>

During recomputation, the blob tables \(svc\_model\_obj\_relation for example\) are updated with today's date in the **last\_mark** field. The code is using 'date time' instead of the date to update the field.

</td><td>

1.  Open the SQL debug.
2.  Change a CI that connects to a service.

Users see an update to the **last\_mark** field with 'date time' instead of just the date.

3.  Repeat the process.

 Observe the same record updating with the same date.

</td></tr><tr><td>

Service Portal

 PRB1855070

</td><td>

Post-Upgrade to Yokohama EA, an error is caused by the business rule 'Create SP Communication ChannelList'

</td><td>

An error found in the logs after upgrading to Yokohama EA 'Recursive business rule call for 'Create SP Communication ChannelList' on sp\_portal'. A number of simple transaction results in this error.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1854090

</td><td>

Cross product downgrade rights should exclude inactive downgrade relationships

</td><td>

There's no behavior change for the users on recon. This is intended to exclude inactive products in the backend.

</td><td>

1.  Create cross product downgrade rights in samp\_downgrade\_model.
2.  Set the Active column to **False**.
3.  Run reconciliation.

 Although the reconciliation result is as expected, it was found that inactive cross products downgrade rights been processed during recon logs, which is incorrect.

</td></tr><tr><td>

Standard Change Catalog

 PRB1856886

 [KB1931818](https://hi.service-now.com/kb_view.do?sysparm_article=KB1931818)

</td><td>

Value is not populated from the template if a new text area field is added when creating or modifying a standard change proposal

</td><td>

The **template\_value** field contains 'STARTSWITH' instead of the '=' operator, which doesn't allow the field to be populated with the value when the template is applied to the change request record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Stream Connect Core

 PRB1859532

</td><td>

Producer Retry job fails to run

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Survey Management

 PRB1842390

 [KB1832412](https://hi.service-now.com/kb_view.do?sysparm_article=KB1832412)

</td><td>

The HR case number is not displayed completely on the survey card on the My surveys page

</td><td>

The HR case number is not displayed completely on the survey card rendered using the 'My surveys' widget on My surveys page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Survey Management

 PRB1855459

</td><td>

Additional service and service endpoint needed for clotho as part of Digital End-User Experience \(DEX\)

</td><td>

 

</td><td>

Navigate to sys\_service and sys\_service\_endpoint table.

 Notice the records for this service.

</td></tr><tr><td>

Territory Planning

 PRB1848653

</td><td>

Problems on Capacity Console

</td><td>

 

</td><td>

 

</td></tr><tr><td>

User Criteria for Service Catalog

 PRB1819841

</td><td>

Semaphore exhaustion is caused by the getAllUserCriteria function getting called in widgets

</td><td>

When a public page is accessed by a guest user or web crawler, this prompts a call to the getAllUserCriteria API, which causes semaphore exhaustion.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1833790

</td><td>

There's a 'Max Tab Reached' message on Workspace

</td><td>

The user has Next Experience off and has a link in the menu to open the workspace. This issue happens only when a user opens a workspace from the link directly.

</td><td>

1.  Open an Xanadu instance.
2.  Navigate to any workspace.
3.  Try to open more than 10 tabs.

 Expected behavior: Opening more than 10 tabs should work.

 Actual behavior: Opening more than 10 tabs isn't working in workspace after an Xanadu upgrade. Users get the message 'Max Tab Reached: You have reached max number of tabs you can have open at one time. Close tabs in order to open more.'

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1817185

</td><td>

In an LLM-enabled user input, the enforced user prompt isn't translated

</td><td>

 

</td><td>

1.  Open Virtual Agent designer.
2.  Open the 'Pizza order' topic
3.  Select the **customer name** node.
4.  See the 'Enforce User' prompt on the right side.
5.  Run the test.

 Expected behavior: There should be a prefix 'MSG: May I know your name?'.

 Actual behavior: There's no prefix 'MSG' for the customer name prompt.

</td></tr><tr><td>

Virtual Agent

 PRB1849287

</td><td>

Topic reduction causes some unexpected errors when selecting an action

</td><td>

 

</td><td>

Check the topic execution from the skill picker, by clicking from a synthesized response, and on auto launch.

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

 PRB1852222

</td><td>

'Time Out Abandoned Virtual Agent \(VA\) Conversations' is not respecting the timeout configured for NAP in sys\_cs\_channel

</td><td>

VA conversations are not closed out according to the timeout configured for NAP.

</td><td>

1.  Set the timeout on NAP channel to four hours.
2.  Create a conversation.
3.  Don't update the conversation

 Expected behavior: Conversation should be closed after four hours.

 Actual behavior: Conversation is closed after two hours.

</td></tr><tr><td>

Virtual Agent

 PRB1855393

</td><td>

User KnowledgeGraph data should be applied for search

</td><td>

 

</td><td>

 

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

Virtual Agent

 PRB1859339

</td><td>

An attachment icon isn't aligning with the rest of the other icons in the chat box

</td><td>

 

</td><td>

1.  Navigate to an Xanadu instance.
2.  Log in as a user and then open Service Portal.
3.  Initiate a chat to see the attachment icon.

 Expected behavior: All the icons in the chat box should align.

 Actual behavior: The attachment icon is slightly above the other icons and doesn't align with the rest.

</td></tr><tr><td>

Virtual Agent

 PRB1866633

</td><td>

In APAC data center instances, AI agents are not working even after accepting the Global Routing Consent information message

</td><td>

Global routing is not working even after consenting on the info message for data center instances in the Asia-Pacific region.

</td><td>

1.  Deploy a new instance from the APAC data center.
2.  In an APAC region instance, select **Agree on the Global Routing Consent info message**.

 Expected behavior: The AI Orchestrator should be invoked.

 Actual behavior: Even after accepting the consent, AI agents are not functioning, and the error message occurs: 'Sorry, there was a problem on my side trying to complete this request. Try asking again later'.

</td></tr><tr><td>

Virtual Agent

 PRB1866635

</td><td>

Trail Assists are incorrectly loaded for 6 or more tools triggered from Now Assist Panel \(NAP\) with skill Discovery

</td><td>

This problem doesn't occur with playground and NAP triggers.

</td><td>

1.  Have a use case with 6 or more tools.
2.  Navigate to NAP.
3.  Enter an utterance for the use case with 6 tools and skill Discovery.
4.  Invoke AI Agents use case:
    -   Utterance: Get me price of
    -   Washing machine - 2
    -   Refrigerator – 3
    -   Monitor – 2
    -   Toaster – 1
    -   Vacuum cleaner – 2
    -   Dishwasher – 2

 Expected behavior: Trail Assists should be 50.

 Actual behavior: Trail Assists are loaded as 25.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1861185

</td><td>

An animated icon isn't visible in NAVA when enabled

</td><td>

 

</td><td>

1.  Enable **sn\_nowassist\_va.nass \_animated\_avatar\_enabled**.
2.  Navigate to NAVA.
3.  Type an utterance like 'what is spam'.

 Expected behavior: An animated icon is visible next to the loading messages.

 Actual behavior: No icon loads next to loading messages.

</td></tr><tr><td>

Workspace App Shells

 PRB1838088

</td><td>

A breadcrumb isn't updating when updating the corresponding record page data

</td><td>

This issue is specific to the master version of Glide.

</td><td>

1.  Create a fresh UI Builder experience from scratch.
2.  Create a standard record page in it.
3.  Use the table 'sn\_align\_core\_feature' or any table where the record page update does update a breadcrumb item.
4.  Update the name of the feature record and save.

 Expected behavior: The breadcrumb should reflect the new name.

 Actual behavior: The breadcrumb isn't updated.

</td></tr><tr><td>

Workspace App Shells

 PRB1839369

</td><td>

SCREEN\_STATUS\_CHANGED isn't working for a breadcrumb app shell

</td><td>

The functionality for the SCREEN\_STATUS\_CHANGED event to close a page in breadcrumb app shell workspace is broken.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   -   [Yokohama Patch 1](yokohama-patch-1.md)
-   [Yokohama security and notable fixes](yokohama-security-notables.md)
-   [All other Yokohama fixes](yokohama-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


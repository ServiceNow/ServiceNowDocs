---
title: Xanadu Patch 4
description: The Xanadu Patch 4 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-12-05"
reading_time_minutes: 42
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 4

The Xanadu Patch 4 release contains important problem fixes.

-   **Xanadu Patch 4 was released on December 05, 2024.**
    -   Build date: 12-02-2024\_1408
    -   Build tag: glide-xanadu-07-02-2024\_\_patch4-11-22-2024

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X04.00.xlsx).

## Overview

Xanadu Patch 4 includes 170 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp4.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 4 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 4, refer to [KB1710163](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1710163).

## Changes in Xanadu Patch 4

-   **[Upgrade legacy replication sets in Instance Data Replication](https://www.servicenow.com/docs/access?context=upgrade-legacy-replication-sets&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US)**

    Complete the upgrade by activating the V2 consumer replication set with or without data integrity checks.


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

Attachments to Records

 PRB1823698

 [KB1709552](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709552)

</td><td>

Out Of Memory \(OOM\) caused by the misuse of BufferedInputStream when creating attachments

</td><td>

Attachments created from previously prepared TMP files are read with BufferedInputStream and have an internal buffer of 512M.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1818225

 [KB1705517](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705517)

</td><td>

Using 'order by' on a single field with a limit clause produces error messages

</td><td>

Users are experiencing Syntax Error or Access Rule Violation messages when they use an 'order by' function on a single field with a limit clause. This error occurs in the within the CMDB workspaces and CMDB hierarchy when viewing tables in the list view. This also occurs if the ordered list displays no data yet indicates a valid, non-zero row count.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1813141

 [KB1706138](https://hi.service-now.com/kb_view.do?sysparm_article=KB1706138)

</td><td>

fd\_data does not read the object from the **Create Task** action

</td><td>

After upgrading from Vancouver with the v1 flow engine to Washington DC or Xanadu with the v2 flow engine, any inline script with fd\_data does not read the object from the **Create and Update Task** action, resulting in failure and an error thrown.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Predictive Intelligence

 PRB1777777

 [KB1702121](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702121)

</td><td>

Similarity calculation from Predictive Intelligence slows down the instance

</td><td>

An issue with Predictive Intelligence similarity calculation slows down alert record loading.

</td><td>

1.  Change the property evt\_mgmt.similarity\_use\_ml to true.
2.  Open an alert record through Express List Records.

Notice that it takes a few minutes to open.

3.  Change the property evt\_mgmt.similarity\_use\_ml to false.
4.  Refresh the alert record.

 Notice that the alerts query takes an average of 35,655 milliseconds.

</td></tr><tr><td>

Rollback Contexts

 PRB1772992

 [KB1648911](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648911)

</td><td>

The 'Shadow' table chunk delete has performance issues

</td><td>

The time taken for deleting shadow records can be derived from the logs. When users delete data from the 'Shadow and snapshot' table, a log statement is printed. First, 'Shadow' table records are deleted, then the 'Snapshot' table. Time between log statements would be the time taken to delete shadow records. It takes more than one minute to delete records from a 'Shadow' table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Web UX Runtime

 PRB1776097

 [KB1709413](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709413)

</td><td>

Chats close automatically on the workspace after they are opened within a few seconds

</td><td>

This issue was introduced in Washington DC. Chats are closed automatically in the workspace after they are opened within a few seconds. Shortly after the chat window is opened, it is then closed, and the chat state is set to 'Closed Complete'.

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

 PRB1778010

</td><td>

The SysActivityRule should filter its query on the fields that workspace can only see

</td><td>

The SysAuditRule does not need to pull all of the fields changes. It only needs to pull the fields that the front end can filter on.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1796571

</td><td>

'Archive Destroy Run' is excessively slow when deleting activities due to the overhead incurred by publishing AMB messages

</td><td>

After upgrading to Washington DC, 'Archive Destroy Run's may take longer than in previous releases due to slowness incurred by publishing messages to the AMB channel for related activities.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1816292

</td><td>

An attachment is not visible in the activity stream in workspaces

</td><td>

When an attachment is added to a Record Producer, it can't be found in the Activity Stream.

</td><td>

1.  Add a variable with Type = 'Attachment' to a Record Producer \(for example, create a case for CSM Outlook\).
2.  Open the record producer in Service Portal.
3.  Attach a file to the field created in step 1 and submit.
4.  Navigate to CSM and FSM Configurable workspace and search for the item created after submitting.
5.  Check the Activity Stream.

 Expected behavior: The attachment should be visible in the Activity Stream in workspace.

 Actual behavior: The attachment is not visible in Activity Stream in workspace.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1820154

</td><td>

An assignment API fails with Genesys

</td><td>

An assignment request API intermittently fails because of server time differences between Genesys and ServiceNow.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1789973

</td><td>

Empty **Short description** and **Description** fields when an incident is created from Quick Action, and the user has to load demo data from the Agent chat plugin to generate these fields

</td><td>

After upgrading to Xanadu, the **Short description** and **Description** fields are empty when an incident is created from the Quick Action function. The user has to load the demo data from the Agent chat group to generate the short description and description for the incident.

</td><td>

1.  Log in to the instance.
2.  Initiate the chat between the Requester and Agent 3.
3.  Navigate to **Quick Action** &gt; **Create incident** from the Agent window.

Notice that it will create an incident.

4.  Open the incident.

Notice that the short description and description is missing in that incident, when it should have the short description and description for incident created from a Quick Action.

5.  Load the demo data for Agent chat group.
6.  Open the incident again.

 Notice that the incident created from Quick action now has the short description and description.

</td></tr><tr><td>

Agent Chat

 PRB1823530

</td><td>

Input text is occasionally truncated in 'now-textarea'

</td><td>

Characters are truncated when typing quickly as an agent.

</td><td>

1.  Set up Agent Chat and accept a chat as an agent in Agent Chat.
2.  Type quickly in the input text area

 Observe that characters are truncated.

</td></tr><tr><td>

Agent Chat

 PRB1830383

</td><td>

Recommendation text is not inserted into a chat window

</td><td>

 

</td><td>

1.  Log in to an instance as an admin.
2.  Initiate a chat with a live agent.
3.  Log in as an agent on other browser and accept the chat.
4.  Select the Sparkle icon.
5.  In the recommendation dialog, select **Insert**.

 Expected behavior: Inserted text should be inserted.

 Actual behavior: Inserted text is not shown in the chat area.

</td></tr><tr><td>

AI Search

 PRB1735195

</td><td>

The range facet and facet with compound table.column set in the facet fields is filtered out when one of the tables is late-binding

</td><td>

A function doesn't parse table.column correctly and results in a bucket match to zero. The facet is then filtered out.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1738123

</td><td>

AisUtils doesn't refresh its search connection \(HaApiClient\) after the search connections are updated

</td><td>

Errors display: 'ScriptableAisUtil: Exception during dump AI search document request: com.glide.ais.error .SearchRuntimeException: NOW-AI\_SEARCH-SEARCH\_QUERY\_ERROR: Additional information - No more read-only connections to try for search...'

</td><td>

1.  Set up AI Search \(AIS\) to use one connection.
2.  Background write any script that uses 'new sn\_ais.AisUtil\(\)'.
3.  Change the AIS Connection to a different endpoint.
4.  Ensure that the AIS backend at the original endpoint is no longer a valid endpoint \(shutdown the original AIS\).
5.  Re-run the same script using 'new sn\_ais.AisUtil\(\)'.

 Observe that the script fails attempting to connect to the old connection.

</td></tr><tr><td>

AI Search

 PRB1811885

</td><td>

A risk intelligence report \(RIR\) doesn't boost for a language match

</td><td>

The AI search log shows that it's matching the language to the session, but the dump shows differently.

</td><td>

1.  Create a RIR action that boosts kb\_knowledge.language matches with the user context language.
2.  Search.

 Expected behavior: Documents are boosted based on the language.

 Actual behavior: No document is boosted.

</td></tr><tr><td>

AI Search

 PRB1818535

</td><td>

Placeholder \(Search\) is missing in the **Global search** field on first login

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1821606

</td><td>

Incorrect semantic ingestion state

</td><td>

Records are stuck in an indexing state.

</td><td>

1.  Search indexed sources.
2.  Navigate to ais\_datasource.
3.  Open the records of Skill, Knowledge Base, and Catalog.
4.  Navigate to the **Indexing History**tab.

 Notice that a few records are struck in an indexing state.

</td></tr><tr><td>

AI Search

 PRB1823539

</td><td>

Filtering search results isn't supported in NASK, although it's supported by the RAGRetrieval API

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1824858

</td><td>

Query rewrite calls aren't being made

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Analytics Center

 PRB1781561

</td><td>

The user observes a 'Data visualization 404 bad request' message

</td><td>

A 'Bad Request 400' is generated when shifting between 'Data Visualization' and 'Dashboard' tabs.

</td><td>

1.  Log in to an instance.
2.  Navigate to CSM/FSM Workspace.
3.  Navigate to 'Data Visualization' then to 'Dashboards' and again back to 'Data Visualization'.

</td></tr><tr><td>

Analytics Data API

 PRB1769933

</td><td>

A bar chart displays different values for the same applied 'group by'

</td><td>

This is an issue with the dot-walking 'group by'.

</td><td>

1.  Navigate to a migrated dashboard.
2.  Navigate to the 'Total Targeted Defects Waiting to be Fixed' visualization.

 Expected behavior: The visualization should display the same data in both dashboards when the same 'group by' is applied.

 Actual behavior: The same visualization displays different results in the Core UI dashboard when the same 'group by' is applied.

</td></tr><tr><td>

Analytics Data API

 PRB1808453

</td><td>

Sorting does not work for value and element order

</td><td>

Values are not sorted by descending and ascending order in Time Series Visualization.

</td><td>

1.  Create a new dashboard.
2.  Add visualization to it.
3.  Select **Time Series Visualization**.
4.  Add a data source as an indicator.

    1.  Use 'group by' as 'priority'.
    2.  Sort by the element order and descending.
Notice that the elements are not sorted by descending order.

5.  Add another time series visualization to the dashboard.
    1.  Select the data source as incident.
    2.  Use 'group by' as 'priority'.
6.  Sort by value and descending/ascending order.

 Notice the values are not getting sorted by descending and ascending order.

</td></tr><tr><td>

Application Manager

 PRB1770423

</td><td>

There is different behavior in a product page versus an app page \(update/installed\) for applications

</td><td>

There can be a version mismatch from the UI between the 'New App' manager page and classics app manger.

</td><td>

 

</td></tr><tr><td>

Asset Management

 PRB1789417

</td><td>

Asset and CI synchronization might not work properly on domain separated instances in the Washington DC release due to the scoped cache mechanism

</td><td>

In domain separated instances, if users have different asset-ci field mappings for different domains, Asset and CI synchronization won't work properly because the currently scoped cache isn't supported for domain separation. Sometimes users observe that the **Asset** and **CI** fields are synchronized for different fields, depending on the first user's domain that generate the cache.

</td><td>

 

</td></tr><tr><td>

Asset Management

 PRB1791993

</td><td>

There are hundreds of errors daily in the system logs reading 'Cannot call sendRedirect\(\) after the response has been committed'

</td><td>

When a Return on Transfer Order Line is performed, the system does not redirect to the newly created Return Transfer Order. The system logs show numerous errors reading 'Cannot call sendRedirect\(\) after the response has been committed'.

</td><td>

 

</td></tr><tr><td>

Attachments to Records

 PRB1823018

</td><td>

Android file type attachments with extension '.aab' cannot be uploaded to or downloaded from the App Store

</td><td>

Files with the extension '.aab' cannot be attached to any record after upgrading to Xanadu. Attachment fails with a MIME type related error 'File type not permitted or mime type does not match the file content'.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1791895

</td><td>

When an explicit role plugin is installed and the property 'glide.security.explicit \_roles.do\_not\_fix'= true, SSO login fails if the post auth policy requires an snc\_internal role

</td><td>

 

</td><td>

1.  Install an explicit role plugin.
2.  Set the property 'glide.security.explicit \_roles.do\_not\_fix'= true.
3.  Set up SSO.
4.  Set up a post auth policy which requires that a login user has the snc\_internal role.

 Expected behavior: Login succeeds.

 Actual behavior: Login fails in post-auth role policy check.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1788452

</td><td>

ATF Field State Validation doesn't work via Service Operations Workspace

</td><td>

The Field State Validation ATF Step to check if fields are not visible does not work in Service Operations Workspace. The ATF Test results in failure showing that a field shout not be visible, but it is visible.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1793151

</td><td>

Screenshots are blank when certain characters appear in Service Portal HTML

</td><td>

context.drawImage\(\) is unable to properly parse the end of a comment that goes for multiple lines and includes extra dashes. Standalone commas in an element's attributes also prevent rendering of the document image.

</td><td>

1.  Create a Service Portal widget \(sp\_widget\).
2.  Add a comment to the body HTML template with extra dashes and new lines, or add a comma character inside an element's attributes.
3.  Add the widget to an sp\_instance in an sp\_column, and add that column to an sp\_page.
4.  Create an ATF test with the 'Open Service Portal Page' step that opens the sp\_page from step 3 in any portal.
5.  Run the test with GlideScreenshot capturing the full page.

 Expected behavior: The screenshot is captured successfully

 Actual behavior: The screenshot is blank and a client test runner console error appears.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1819557

</td><td>

Remove deprecated entitlement code and APIs in HR Plugins

</td><td>

HR Core sys\_app\_modules aren't installed.

</td><td>

Provision and instance with the HR Core and LE plugins installed.

 Notice sys\_app\_modules aren't installed and HRModuleTestIT is failing.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1823948

</td><td>

Some RCA's were removed from global scripts and must be added back

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB1808057

</td><td>

ACL's are missing for base instance model similarity as a result of a training model failure

</td><td>

A model errors out because an ACL is missing.

</td><td>

1.  Entitle the latest Task Intelligence for CSM version and sn\_nb\_action\_adv from TPP.
2.  Provision an instance wth cwf-workspace- 24.3.8-SNAPSHOT installed.
3.  Navigate to **All** &gt; **Task intelligence** &gt; **Setup**.

Notice that a similar open case and a similar closed case model is present in the base instance.

4.  Select any model and select **Launch training**.

 Actual behavior: The model errors out because an ACL is missing.

 Expected behavior: The model should be trained successfully.

</td></tr><tr><td>

Change Management

 PRB1816569

</td><td>

Standard Change Properties should not have been modified on upgrade from Washington DC to Xanadu

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1672625

 [KB1364738](https://hi.service-now.com/kb_view.do?sysparm_article=KB1364738)

</td><td>

Choices for the **Life Cycle Stage** and **Life Cycle Stage Status** fields are not translated

</td><td>

In list view, both translations do not work. In form view, **Life Cycle Stage** translations do not work.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1824939

</td><td>

Change the health dashboard failure threshold max value to 10M

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Continual Improvement Management

 PRB1816181

</td><td>

Add 'dex-notify-svc' service within glide.services .rest.allowed\_services

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1785305

</td><td>

If an optimization is performed, SqlJoinOptimizer silently drops CTE statements

</td><td>

This impacts anything that extends ASqlOptimizer.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1826425

</td><td>

An Application Menu Module \(sys\_app\_module\) with a space character causes a display failure in the Filter Navigator

</td><td>

An Application Menu Module \(sys\_app\_module\) may not be visible in the Filter Navigator if there is a whitespace character \(non-null value\) in the **Query** field.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1772039

</td><td>

Archiving 1000 records takes approximately four minutes, which is two minutes more than in Washington DC

</td><td>

With this current rate, it takes ~17 hours to archive 1M records. In BT1, sdlc\_test\_result table is loaded with ~50 million records everyday. If users want to archive this table, then this would be a BT1 blocker.

</td><td>

1.  Create 1M or 100K records in an instance.
2.  Keep the archive chunk\_size as '1000' in sys\_properties.
3.  Create an archive rule and trigger the 'Archive' job.
4.  Verify the 'Archive' job's execution time.

 Expected behavior: 1000 records archiving shouldn't take much time, since 1000 records archiving takes approximately two minutes in the Washington DC release.

 Actual behavior: 1000 records archiving takes about four minutes.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1782312

</td><td>

API calls using sysparm\_offset +sysparm\_limit parameters run the query without a defined 'Order by', causing results to not return consistently in RaptorDB

</td><td>

API calls using sysparm\_offset +sysparm\_limit parameters will run the query without a defined 'Order by'. This will not return the results consistently in RaptorDB, as it did in MariaDB. MariaDB returned results in the same order, even if the 'order by' is not defined, but its randomness caused a return of inconsistent results.

</td><td>

1.  Run a Rest API call with sysparm\_offset+ sysparm\_limit parameter on a table with a high amount of records.
2.  Compare the number of duplicate sys\_ids pulled in Maria compared to PG.

 Notice that PG will have more duplicates than MariaDB.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1784967

 [KB1706117](https://hi.service-now.com/kb_view.do?sysparm_article=KB1706117)

</td><td>

A NullPointException \(NPE\) was thrown while invoking the getAvailableConnection

</td><td>

An NPE occassionally occurs during the AHA 3.0 switchover. The failure to load the scripts database is because the return value of com.glide.db.pool. DBConnectionPool. getDBConnection\(int\) is null.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1815761

</td><td>

Running app nodes should continue to run even after other databases become RW

</td><td>

Running app nodes should continue to run even after DB1 \(primary\) becomes RW if the intended primary is set to DB2.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1813934

</td><td>

Restricting queries to a primary-only configuration isn't honored by Glide

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1786484

</td><td>

RunningProcessReconciler marks redundant update processes as absent

</td><td>

When ADM fetches running process information, if a process is no longer active on the host, the cmdb\_running\_process record is marked as absent. With the current behavior, if the same ADM payload is processed again, the system marks the same running process as absent.

</td><td>

1.  Run discovery on host.

Notice that running processes are populated.

2.  Turn off one of the running process on the host and rerun discovery.

Notice that the event 'running.process.absent' is logged.

3.  Run discovery again.

 Notice that the event is logged with the same data.

</td></tr><tr><td>

Discovery

 PRB1804276

 [KB1702685](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702685)

</td><td>

Discovery Application Dependency Mapping \(ADM\) Process Classifiers put incorrect Configuration Items \(CI\) in the probe ecc\_queue outputs, leading to data from the application only to be updated in the computer CI

</td><td>

When the ADM probe is runs, matching process classifiers will trigger probes specific to applications. The code involved in specifying the CI to put in the probe output is in the script include Application DependencyMapping, which puts the parent computer CI in instead of the application CI. As a result, the computer CI becomes updated and overwritten rather than the application CI, and the application CI is not updated.

</td><td>

1.  Open NGINX on a Linux server to use as an example.
2.  Open a Vancouver instance.
3.  Discover a host to create a NGINX CI is created.
4.  Upgrade the instance to Washington DC.
5.  Clear out the version value from the existing application CI.
6.  Discover the Linux host.

 Notice that the example version is not repopulated in the NGINX CI.

</td></tr><tr><td>

Discovery

 PRB1817735

</td><td>

Shazzam should always use 'glide.discovery .shazzam\_simplify\_ranges', and this should be true

</td><td>

This property should be set to true, or it shouldn't check for this property and always use simplify ranges.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1817799

</td><td>

Starting a Discovery takes a while when there's a sizable global exclusion IP address list and inclusion list

</td><td>

Discovery and Shazzam Sensor processing takes a long time when there is a sizable global exclusion IP address and inclusion list.

</td><td>

1.  Open a Washington DC instance.
2.  Add 430K IP addresses to the global exclusion list.
3.  Create a Discovery schedule with the inclusion list of 50k IP addresses.
4.  Start Discovery.

 Notice a long runtime.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1703041

</td><td>

Checkbox values are not copied to a target record

</td><td>

Checkbox values are normalized but not handled by the flow.

</td><td>

1.  Create a Use Case.
2.  Assign a Target Table to the Use Case.
3.  On that Target Table, create **True**/ **False** fields to store the values of the checkboxes.
4.  On the Use Case, create a checkbox list and a few checkboxes. Leave the Target Table blank and select the **True**/ **False** fields as 'Target' for the checkbox fields.
5.  Create the Flows.
6.  Proceed with extracting a document.

 Observe that the checkbox values are not copied to the target record. The value is captured in the metadata field of the Extracted Value but the flow doesn't handle setting the value as a True/False

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1794325

</td><td>

A use case upgrade fails when the use case is copied from a pre-trained model

</td><td>

When copying from the pre-trained use case, it makes a call to a certain component to migrate the model of the pre-trained task definition. As of Xanadu, this component is no longer needed and shouldn't be used. The job fails and this blocks the upgrade.

</td><td>

1.  Have an instance on Washington DC that has a use case copied from a pre-trained model.
2.  Upgrade the instance to Xanadu.
3.  Execute the 'Task definition upgrade' scheduled job.

 Notice that the task definition upgrade fails for the copied use case.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1818140

</td><td>

Parent-Child Relationship is missing in Field Group Configurations

</td><td>

The following items are missing from the schema: the 'parent' reference field within line-item level field groups; the new field group type non\_table\_list\_field\_group for document-level data; and the parent\_index field in the structure of extracted values.

</td><td>

Attach a PDF file with a name with more than 100 characters.

 Notice that the process task does not create entries in the di\_genai\_output tables.

</td></tr><tr><td>

Email Notifications

 PRB1791495

</td><td>

In inbound email processing, the 'Disabling Subject' classification disables the 'In-Reply-To' header classification

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1798974

</td><td>

There' is an issue in custom notifications where the affected record field isn't saving a CI with a special character

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1812566

</td><td>

Subflow outputs aren't passed to a callback when a subflow ends on MID

</td><td>

A callback is called with no outputs.

</td><td>

1.  Create a subflow which goes to MID and sets subflow outputs.
2.  Call the subflow via interactive mode with a callback requested.

 Expected behavior: The callback is called with the outputs that were set by the subflow.

 Actual behavior: The callback is called with no outputs.

</td></tr><tr><td>

Flow Engine

 PRB1816146

</td><td>

An interrupted flow marker shouldn't run during the 'Interactive' job

</td><td>

The issue is caused by excess time being consumed by the interactive flow marker, preventing the 'Interactive' job from taking interactive work.

</td><td>

1.  Turn off all Flow Engine Event Handlers \(com.glide.hub.flow\_ engine.event\_ handler.workers = 0\).
2.  Run a long running flow.
3.  Update the transaction ID on the flow context to an already completed transaction ID.

 Expected behavior: The flow context shouldn't be marked 'Presumed Interrupted' by the Flow Engine Interactive Event Handler because this isn't critical work.

 Actual behavior: The flow context is marked 'Presumed Interrupted' by the Flow Engine Interactive Event Handler.

</td></tr><tr><td>

Flow Engine

 PRB1818147

</td><td>

Enqueue logic for queueing an interactive flow job doesn't work if there are more than one interactive jobs

</td><td>

 

</td><td>

1.  Set com.glide.hub.flow\_ engine.event\_handler. interactive\_workers = 2.
2.  Trigger a long running interactive flow.
3.  Trigger one more interactive flow.

 Expected behavior: The second interactive flow should run in milliseconds.

 Actual behavior: The second interactive flow starts in 1-2 seconds whenever the second job is triggered.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1806316

</td><td>

Selecting 'Advanced Options' in a flow with run users results in a blank screen

</td><td>

A box should appear to the right of the screen that allows user selection, but instead a blank screen appears.

</td><td>

1.  Create any flow with Advanced options \(add at least one user\).
2.  Activate the flow.
3.  Open the same flow and select **Edit flow**.
4.  Select **Advanced Options**.

 Observe the broken UI page.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1820117

</td><td>

Flow recommendations are not showing up on a 26.2 instance

</td><td>

Adding triggers and actions to a new flow does not prompt any flow recommendations.

</td><td>

1.  Log in to Flow Designer.
2.  Create a new flow.
3.  Add triggers and actions.

 Notice that no recommendations appear.

</td></tr><tr><td>

GRC Platform Plugins

 PRB1823897

</td><td>

Smart Assessment global plugin changes

</td><td>

Functionality for fetching and saving of dynamic values in impact automation is not present.

</td><td>

 

</td></tr><tr><td>

Haraka \(Glide\)

 PRB1824231

 [KB1709920](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709920)

</td><td>

sys\_kagami\_query\_engine has an error on the column decision\_last\_msg

</td><td>

Queries are not routing to postgreSQL after upgrading to Xanadu. Queries with 'group by' are attempting to route to Haraka, but are failing due to a syntax error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1825365

 [KB1709665](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709665)

</td><td>

Health Log Analytics breaks after upgrading to Xanadu

</td><td>

MID Server distribution is missing a bundled dependency \(mid-loom.jar\).

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

History Set

 PRB1806563

 [KB1706740](https://hi.service-now.com/kb_view.do?sysparm_article=KB1706740)

</td><td>

Duplicate comments are observed intermittently even after enabling a fix

</td><td>

With a fix, the history set loader flow was modified to utilize the system property glide.history\_ set.pull\_journal \_entries\_from\_journal\_table. However, there are new instances of intermittent duplication issues, even with this property enabled. In these cases, duplicate records in the sys\_history\_line table originate from the sys\_journal\_field table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

 PRB1793474

</td><td>

There is a discrepancy between instances related to the dictionary field 'Restricted access / Locked' deployed from sn\_hr\_er

</td><td>

The dictionary 'Read only' should be set to false in a base instance, but it is set to true in some base instances.

</td><td>

 

</td></tr><tr><td>

HTML Field Type Editor

 PRB1782444

 [KB1648540](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648540)

</td><td>

When the 'close unordered list' tag is used in a template, a non-breaking space element gets added to the HTML field

</td><td>

When a template is created on an HTML field and '/ul' tag is included , the issue occurs. Applying the template adds a space to the HTML field. The value is seen as; /ul.

</td><td>

 

</td></tr><tr><td>

Incident Management

 PRB1818913

</td><td>

The 'Create Knowledge' function on the incident table does not open the KCS-HTML template

</td><td>

After changing the name of the article template from 'Incident-KCS article - HTML' to 'Incident-KCS article - HTML2' and attempting to create a Knowledge Base article for a closed or resolved incident, the article template does not open. Instead, users are re-routed to the default Knowledge Base page.

</td><td>

1.  Open the article template.
2.  Search for kb\_template\_incident\_ kcs\_article\_html.
3.  Change the name from 'Incident-KCS article - HTML' to 'Incident-KCS article - HTML2'.
4.  Save the record.
5.  Open the closed/resolved incident.
6.  Select **Create Knowledge**.

 Expected behavior: It should open knowledge in kb\_template\_incident \_kcs\_article\_html.

 Actual behavior: It redirects to the default Knowledge Base page.

</td></tr><tr><td>

Innovation Management

 PRB1824475

</td><td>

An HTML type field toolbar option is missing in Xanadu upgrade

</td><td>

In the TinyMCE field toolbar in the Idea Portal, there is no option for font or size selection.

</td><td>

1.  Provision an instance with the Innovation Management and Idea Manager Dashboard plugins installed.
2.  Navigate to **All** &gt; **Idea Portal**.
3.  Once Idea Portal opens, choose one of the ideas.
4.  Scroll down to leave a comment.

 Notice that the TinyMCE toolbar does not allow font selection.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1804034

</td><td>

A bidirectional set is rolled back during upgrade, causing the upgrade to get stuck

</td><td>

The user observes the error: 'Upgrade rolled back. A replication delay caused a synchronization issue, which could lead to data loss. Retry the upgrade after allowing replication to catch up.'

</td><td>

 

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1818163

</td><td>

Caching issues with idr\_instance\_info upon upgrade

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1812412

</td><td>

After publishing, users observe an error in the 'Spoke activity' log

</td><td>

After publishing, users observe an error in the 'Spoke activity' log: 'Invalid field name: \[\*\]Unknown error. Check system logs for more details.'

</td><td>

1.  Create a spoke.
2.  Select **Now Assist**.
3.  Enter the context.
4.  Publish.

 After publishing, the user observes an error in the 'Spoke activity' log: 'Invalid field name: \[\*\]Unknown error. Check system logs for more details.' Also the action is in 'Draft', not in 'Publish'.

</td></tr><tr><td>

Integration Hub Stream Connect

 PRB1822182

</td><td>

Allow read, update in kafka producer for read/updates from other application scope

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1695875

</td><td>

Make Key Management Framework \(KMF\) diagnostics page error messages more readable

</td><td>

The error code or title, 'VAULT\_SHOULD \_BE\_DISABLED\_ WITH\_FIPS\_APPROVED \_MODE', is not user-friendly.

</td><td>

1.  Check KMF Diagnostics a in FIPS \(Federal Information Processing Standards\) approved instance.
2.  Notice the errors in Vault Section.

 Expected behavior: Error code or title is end-user readable.

 Actual behavior: The error code or title is long and not user-friendly, and has the message 'VAULT\_SHOULD \_BE\_DISABLED\_ WITH\_FIPS\_APPROVED \_MODE'.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1782883

</td><td>

The **Rotate IRK** button is missing for active IRKs \(Instance Root Key\) in sys\_kmf\_external\_key

</td><td>

 

</td><td>

1.  Provision an instance with the track/jdkupgradecompile build.
2.  Run the script to generate the IRK in the sys\_kmf\_external\_key table new: sn\_kmf\_ns.KMFRootKey API\(\).updateAllI RKMetadata\(\);.
3.  Open the newly generated IRK.

 Expected behavior: The **Rotate IRK** button should be available to rotate the Active IRK.

 Actual behavior: The **Rotate IRK** button is missing.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1795479

</td><td>

A region isn't updated in the glide.crypto.core .config.cache post-move

</td><td>

A source datacenter is impacted even though the instance is moved to a different region. An error is thrown.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1800400

</td><td>

IRK rotation fails after a cross-region move

</td><td>

The user is unable to rotate an IRK when an instance with Bagheera is moved from one region to another.

</td><td>

1.  Perform a cross region move in the Washington DC and Xanadu instances.
2.  Verify that the move was successful.
3.  Navigate to the sys\_kmf\_external\_key table.
4.  Try rotating the current IRK.

 Observe a failure to rotate IRK.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1810219

</td><td>

The auto-resolve workflow doesn't wait for the timeout when checking the clone status

</td><td>

The 'Instance rekey' job doesn't have the instance ID in the context, which results in the clone completing but the rekey status returning as a failure without waiting for the timeout. The clone exits with success, but the rekey isn't complete.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1819556

</td><td>

Automations executing scripts through the run-node-script shouldn't cause excessive instance key deactivation

</td><td>

Everytime the run-node-script executes, all instance keys fail to unwrap and are deactivated by the auto-resolution logic on the startup path. At scale, this causes an excessive growth of records in sys\_kmf\_instance\_key.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1810451

</td><td>

The **Preview Article with Blocks** UI action does not work as expected

</td><td>

The UI action **Preview Article with Blocks** on a published knowledge article opens a page that doesn't show the knowledge blocks listed in the right side panel under 'Blocks in Article'.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1818222

</td><td>

Hide or disable ES12 toggle for MID tables

</td><td>

ES12 is turned on by default starting Xanadu, and the MID server doesn't support ES12 features.

</td><td>

1.  Navigate to the MID script include
2.  Notice the **Toggle** button.

</td></tr><tr><td>

MID Server

 PRB1819817

</td><td>

Reduce default SFTP read/write buffer to 32768 from 32868

</td><td>

There are cases of import/export where the environment has some issues in handling the SFTP buffer size of 32868. Since import/export has not exposed any SSH configuration, users aren't able to reduce the buffer size.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1811954

</td><td>

DocumentData aren't saved to the SQLlite database

</td><td>

When customized table metadata does not have a reference column for the dotwalk first field, mobile script throws instead of break, which causes the rest of the DocumentData not to be processed.

</td><td>

1.  Create a custom table extend task.
2.  Add a dotwalk condition in data item, like cmdb\_ci.name.
3.  Navigate to offline, and ensure that cmdb\_ci column is not the in the custom table definition.

 Observe that offline list of the custom table is empty.

</td></tr><tr><td>

Mobile Platform

 PRB1828958

</td><td>

Update mobile client script version in Xanadu

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1805368

 [KB1703778](https://hi.service-now.com/kb_view.do?sysparm_article=KB1703778)

</td><td>

Use of home keyboard cursor navigation is broken in the Next Experience navigation filter input and end keyboard buttons in Xanadu

</td><td>

Left, Right, Home, End, Shift+Home, Shift+End, Shift-Left, and Shift-Right don't move the cursor or select text.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1806148

</td><td>

Extra long contextual pill is pushing search, help, notification, and the user menu out of viewport

</td><td>

Extra long text in the contextual menu is not truncated and causes spillover of the search and other icons.

</td><td>

1.  Log in to any instance.
2.  Navigate to any page that has a long title.

 Notice that the extra long text in the contextual menu is not truncated and causes spillover of the search and other icons.

</td></tr><tr><td>

On-Call Scheduling

 PRB1819083

</td><td>

The 'On-call schedules' \(all on-call schedules\) tab isn't loading

</td><td>

The 'All on-call schedules' tab gets stuck at 'Loading'. The following error message displays in the console: 'TypeError: Cannot read properties of undefined \(reading 'name'\)...'

</td><td>

1.  Navigate to on-call schedules.

The 'All on-call schedules' tab is stuck in a 'Loading' state.

2.  Select **My on-call schedules**.

 Notice that if a user selects the 'All on-call schedules' tab, the display doesn't change and still displays 'My on-call schedules' tiles.

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB1807347

</td><td>

Report widget titles are truncated on smaller widgets in dashboards

</td><td>

The space for the refresh and other control buttons is reserved and left blank as of Washington DC, but this was not the case in Vancouver and prior versions.

</td><td>

1.  Navigate to any dashboard.
2.  Resize any widget to shorten the title.

 Observe that not all the space is used to display the title as of Washington DC.

</td></tr><tr><td>

Performance Analytics

 PRB1816393

</td><td>

Duplicating a shared visualization does not allow the owner to configure the visualization in VIZ-Designer

</td><td>

An ITIL user with view access to a visualization can't configure the visualization.

</td><td>

1.  Create a visualization in VIZ-Designer as an admin and share it with an ITIL User with view access.
2.  Log in as an ITIL user and open the visualization that was shared with view access.

 The ITIL user gets a message that they can't configure it. They continue to be unable to configure it when they: duplicate the visualization, add the duplicated visualization to dashboard, unlink the duplicated visualization from the library from the widget options, and make a duplicated copy for above widget that is unlinked.

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1821090

</td><td>

Flickering and no data to display issue with Agile dashboards after migration

</td><td>

Custom content blocks flicker and display a 'no data to display' error message after switching from the Agile 2.0 Team dashboard to the Agile 2.0 Sprint dashboard.

</td><td>

1.  Provision an instance with the family plugin Agile development 2.0 installed and the store apps scrum-common and scrum-dashboards installed.
2.  Set up test data for the custom content blocks.
3.  Use the dashboard change list to switch to the Agile 2.0 Team dashboard to Agile 2.0 Sprint dashboard.

Notice that custom content blocks are flickering before loading the data completely.

4.  Reload the page.

 Observe that some of the custom content blocks show a 'no data to display' error.

</td></tr><tr><td>

Platform Analytics Migration Center

 PRB1814444

</td><td>

Admins should observe confirmation messages when triggering migration and activation

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration Center

 PRB1820289

</td><td>

Widgets are reloading after tab switch for dashboards with multiple tabs after the Core UI Dashboard migration to Next Experience

</td><td>

After migrating Agile development 2.0 core UI dashboards to Next Experience, widgets are reloading after switching between tabs for dashboards with multiple tabs.

</td><td>

1.  Install the family plugin Agile development 2.0.
2.  Install store apps scrum-common and scrum-dashboards. \(View the attached the zips\)
3.  Set up test data for the custom content blocks with the attached data setup scripts.
4.  Navigate to **Platform Analytics** &gt; **Dashboards**.
5.  Navigate to the Agile 2.0 Team dashboard.
6.  Select PriorDB-Group in the top level filter.
7.  Navigate to **Sprint Performance** &gt; **Cycle time**.
8.  Return to Sprint Performance.

 Expected behavior: They should not reload unnecessarily.

 Actual behavior: Widgets at sprint performance are reloading.

</td></tr><tr><td>

Platform Runtime

 PRB1811012

</td><td>

Selecting **Take Questionnaire** for a Work Order Task does nothing

</td><td>

A questionnaire should be opened and agent should be able to answer and submit the questionnaire.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1817167

</td><td>

The max length of field form fields on an activity definition is set to 255, which doesn't match the matching subflow's length of 2000

</td><td>

 

</td><td>

1.  Create a process with a 'User Form' activity.
2.  Add 25+ fields in the UI layout tab's **Form fields** field.
3.  Save.
4.  Refresh the page.
5.  Reopen the activity.

 Expected behavior: All fields should still be specified.

 Actual behavior: Some of the fields were cut off. During runtime, the cut off is seen in the activity context record.

</td></tr><tr><td>

Predictive Intelligence

 PRB1802044

</td><td>

The enable\_workflow\_similarity property is set to false in system properties

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1813440

</td><td>

There is a training failure at the pre-processing stage when using numeric columns with sparse embeddings

</td><td>

On a training workflow capability solution with numeric columns and TF-IDF\(Sparse\) embedding, training fails in the pre-processing stage.

</td><td>

Train any workflow capability solution with at least one numeric column and TF-IDF enabled in the advanced solution settings.

 Observe that the training fails at pre-processing stage with column not found error.

</td></tr><tr><td>

Reporting

 PRB1769845

</td><td>

An email report has two attachments, one with the data and one with an error

</td><td>

The user creates a scheduled report with a 'run as user' set who is a non-admin user and doesn't have access to the report. However, the user has access to the actual data the report is querying. The user selects 'Execute Now' and there is an email triggered with two attachments, one that says 'Access to this content denied based on report\_view ACLs.', and the other with the data.

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB1815240

</td><td>

Multi-pivot in Service Poral throws 'ERROR: An error occurred while generating chart'

</td><td>

There's also an error in the logs: 'Uncaught Error: TypeError: leftMostRowValue \[key\].escapeHTML is not a function'.

</td><td>

1.  Navigate to the classic reporting module.
2.  Create a report:
    -   Table: incident
    -   Type: Multi-level pivot table
    -   Selected columns: Assignment Group
    -   Selected rows: Short description, Number
3.  Navigate to **Service Portal** &gt; **Service Portal Configuration**.
4.  Select **Designer**.
5.  Add a page.
6.  Select any container.
7.  Under 'Widgets', select **Report** and drag it into the container.
8.  Select the recently created multi-pivot chart.

 Expected behavior: The chart renders.

 Actual behavior: 'ERROR: An error occurred while generating chart' displays.

</td></tr><tr><td>

Resource Management

 PRB1784311

</td><td>

When trying to select the **Request Extension** button on a resource plan from the project workbench, the 'Extend resource plan' pop-up appears empty

</td><td>

A blank pop-up screen appears.

</td><td>

1.  Navigate to the project module and open any project.
2.  Under the related links, select something in the project workbench.
3.  Under the resource tab, select any resource plan.
4.  Select the **Request Extension** button.

 Observe that a blank screen appears.

</td></tr><tr><td>

Resource Management

 PRB1805513

</td><td>

When the property com.snc.resource \_management. generate\_daily\_aggregates is true, records aren't generated in 'Resource Aggregates Daily'

</td><td>

This is reproducible when resource aggregates is created for the first time with 1FTE.

</td><td>

1.  Set the 'com.snc.resource \_management .generate\_daily\_aggregates' property to true.
2.  Create a resource assignment for a user.

 Observe that on the resource aggregate daily table, availability records aren't displayed correctly.

</td></tr><tr><td>

Resource Management

 PRB1820666

</td><td>

Resource reports are broken after Xanadu upgrade when the glide.sys.date\_format is dd-MM-yyyy

</td><td>

Before the upgrade, the resource report start date and end date was in dd-mm-yyyy format, but after upgrading to Xanadu it is in yyyy-mm-dd format.

</td><td>

1.  Navigate to **Resource** &gt; **Resource reports**.
2.  Set **Entity type** to 'User', and select a user.

 Notice that the start date and end dates get populated automatically in yyyy-mm-dd format, and the end date cannot be changed.

</td></tr><tr><td>

Search Administration

 PRB1776348

</td><td>

The AI Search results page doesn't display translated values

</td><td>

Translation prefixes are not populated when i18n debugging is enabled.

</td><td>

1.  Log in to Washington or Vancouver instance.
2.  Make sure to install AI Search and the German \(or Any\) language plugin.
3.  Search for a random keyword that fetches results from different tables such as change, incident, problem.
4.  Switch the language to German.

 Notice that the facet values in the left side panel and in the results are not translated.

</td></tr><tr><td>

Seismic Framework

 PRB1807578

</td><td>

A race condition comes out of multiple single sign-ons

</td><td>

Users are intermittently taken to the incorrect URL.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1796259

</td><td>

Failure to instantiate a GlideElement during a sandboxed script execution can take down a node

</td><td>

It should obtain the global scope to reinitialize GlideController instead of trying to traverse to global from the current GlideElement and, potentially, grabbing the sandbox scope instead.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1821549

</td><td>

'Undefined' isn't supported when using ScriptRuntime .evalSpecial

</td><td>

 

</td><td>

 

</td></tr><tr><td>

ServiceNow Security Center \(Family Release\)

 PRB1812452

</td><td>

The due date for critical update records 'End of Support: GlideEncrypter API' and 'Enable 3DES deprecation for Password2 Fields' should be updated

</td><td>

The due dates for the following should be in future: 'Enable 3DES deprecation for Password2 Fields: 2025-01-30' and 'End of Support: GlideEncrypter API: 2025-07-31'.

</td><td>

1.  Log in as an admin.
2.  Navigate to the 'Customer action' page in the Security Center.

 Expected behavior: The due dates should be in the future.

 Actual behavior: Two customer actions have a due date that is too soon.

</td></tr><tr><td>

Software Asset Management

 PRB1770287

</td><td>

True-up cost calculation isn't correct for software model/ product/publisher results for single currency instances when the currency is set to anything other than USD

</td><td>

True-up cost calculation isn't correct for software model/ product/publisher results for single currency instances when the currency is set to anything other than USD for employee license metrics. The true-up cost in the license metric result is correct. For multi-currency instances, the true-up cost calculation is as expected.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1819212

</td><td>

There's a localization issue in 'Potential savings' on single currency instances

</td><td>

The issue arises from incorrect handling of currency settings during reconciliation, leading to localization issues in potential savings, calculations on removal candidates, and license metric results. The issue occurs because GlideAggregate calculations and dot-walks to the **fx\_currency** fields return values in the system's reference currency, whereas GlideRecord's setValue function enters values in a user's session currency.

</td><td>

 

</td></tr><tr><td>

Software Asset Reclamation

 PRB1815883

</td><td>

There is a localization issue in potential savings, true up cost, over-licensed amount, and total spend calculation

</td><td>

The defect arises from incorrect handling of currency settings during reconciliation, leading to localization issues in potential savings, calculations on removal candidates, and license metric results. The issue occurs because GlideAggregate calculations and dot walks to the **fx\_currency** fields return values in the system's reference currency, whereas GlideRecord's setValue function enters values in a user's session currency.

</td><td>

 

</td></tr><tr><td>

Source Control Engine

 PRB1789863

 [KB1652375](https://hi.service-now.com/kb_view.do?sysparm_article=KB1652375)

</td><td>

There is a failure to install an app with a dependency that was converted to 'application repository' mode

</td><td>

Trying to install an app with a dependency on another app that was converted from a Store app into a developer app with 'application repository mode' results in failure.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Syntax Editor

 PRB1788757

</td><td>

Upgrades/side loads are impacted when old JavaScript code is still being used by browser cache

</td><td>

 

</td><td>

On an instance with an old release of Code Assist, upgrade or side load the latest version.

 Notice that the browser still has the JavaScript files from the old version cached, and it requires a hard refresh to load the latest code.

</td></tr><tr><td>

System Events

 PRB1792583

</td><td>

Flow Engine is unable to move a sysevent in the ready.node state back to ready when the sysevent table rotation record is deleted

</td><td>

When the flow engine encounters sysevent records older than five minutes in the state ready.node, it should move them back to 'Ready' so they can be picked up by another node. This does not happen when the Table Rotation for sysevent has been deleted.

</td><td>

1.  Delete the record for Table Rotation of sysevent.
2.  Generate enough flow.fire event to load one node over its capacity so that an event can't be executed before five minutes.

 Expected behavior: The sysevent should go back to the ready state and be picked up by another node.

 Actual behavior: The sysevent stays in ready.node\# state.

</td></tr><tr><td>

Territory Planning

 PRB1810729

</td><td>

An inactive adhoc agent appears on search and date change

</td><td>

 

</td><td>

1.  Navigate to CSM / FSM configurable workspace.
2.  Add an agent as adhoc in a territory until a date.
3.  Add the same agent to a different territory until a later date.
4.  Search / filter for the agent and change the date.

 Expected behavior: The agent should only be visible only under the second territory added.

 Actual behavior: The agent appears under both territories.

</td></tr><tr><td>

UI Actions

 PRB1826799

 [KB1709928](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709928)

</td><td>

setRedirectURL\(\) does not work in Xanadu

</td><td>

After upgrading to Xanadu, 'action.setRedirectURL\(\)' does not redirect the user to the appropriate URL or page after UI actions are executed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1797566

</td><td>

There is an empty payload in some events emitted by Attachment UIB component

</td><td>

An attachment payload is not captured on download and preview events in workspaces.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1825488

</td><td>

Workspace incorrectly saves FX currency fields when the locale is nl.NL

</td><td>

When saving an **fx\_currency** field value in workspace, the value is saved incorrectly. This does not occur when performing the same operation outside workspace.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1758068

</td><td>

Hidden tab labels are visible

</td><td>

The tab-set 'hideLabel' property isn't honored in Washington DC, which results in tabs not being hidden.

</td><td>

1.  Open an instance with UIB / UXF installed.
2.  From any UIB workspace, navigate to a 'tabs' component with one or more existing tabs.
3.  Update the tab property by setting 'hide tabs label' to true and save.

 Expected behavior: Tab labels are hidden.

 Actual behavior: Tab labels still visible, seemingly no change.

</td></tr><tr><td>

UX Framework

 PRB1818682

</td><td>

UIB data broker sends empty context props as 'null' \[type string\] instead of null \[type object\].

</td><td>

 

</td><td>

1.  Navigate to Guided Setup module under Adoption Services Application.
2.  Select the **Service Operations Workspace for ITSM** product in the Configure Products tab.
3.  Select **Continue**.

 Observe an error notification reading: 'Please remove interaction ID from URL for single run guided setup.'

</td></tr><tr><td>

Virtual Agent Designer

 PRB1826226

</td><td>

LLM conversations should not make queries to sys\_cs\_topic\_language

</td><td>

Queries should not be made to sys\_cs\_topic\_language, which is an NLU-only table.

</td><td>

1.  Start any LLM topic.
2.  Go through the topic by answering the questions.

 Expected behavior: There should not be any queries made to sys\_cs\_topic\_language.

 Actual behavior: There are slow queries made to sys\_cs\_topic\_language.

</td></tr><tr><td>

Virtual Agent

 PRB1785278

</td><td>

When the user filters a search, the exact search item shows up but the option to **Show 10 more** results appears

</td><td>

The user should not observe **Show 10 more** unless the searched record count is more than 10.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1816479

 [KB1705481](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705481)

</td><td>

A choice list turns to English after expanding the list for more options

</td><td>

The issue occurs in all eight languages.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1818411

</td><td>

When search input is empty for a RAG search term and a test is run, eval is stuck in 'In progress'

</td><td>

Parent skill does not receive the response of the child skill.

</td><td>

1.  Create a child skill which takes input as skill input and publish it.
2.  Create a parent skill and add the child skill as tool.
3.  The prompt of the parent skill should contain the response obtained from the child skill.
4.  Publish the parent skill.
5.  Run the test and verify that the response in successful as expected.
6.  Run the same parent skill using an API.
7.  Observe the response of parent skill.

 Expected behavior: The parent skill input prompt should contain the response of the child skill and use it to generate a final response.

 Actual behavior: Parent skill does not receive the response of the child skill.

</td></tr><tr><td>

Virtual Agent

 PRB1818624

</td><td>

Search is down while the Washington DC xnowassiststable to upgrade is in progress

</td><td>

This impacts Washington DC instances upgrading to xnowassiststable. It was noticed that Now Assist GRs were not returned during the upgrade until the end of the loading plugins stage. During the upgrade perform search from the service portal, the search is down and regular search results show, but not GRs. GRs should be returned during upgrade.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1819306

</td><td>

Retry mechanism for evaluation on large datasets

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1819726

</td><td>

Invoke FDIH API in non-interactive mode if request coming from NASK

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1822999

</td><td>

CS\_NODE\_DETAILS cache size is inadequate

</td><td>

After running performance tests against Now Assist Virtual Agent conversational catalogs, there is latency because the subject cache is small.

</td><td>

1.  Set up Now Assist Virtual Agent with conversational catalogs.
2.  Run a performance test against these topics.

 Notice that there is latency due to the subject cache being too small.

</td></tr><tr><td>

Virtual Agent

 PRB1825262

</td><td>

Attributes are not mapped as expected in sync mode of capability chaining

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1825821

</td><td>

A legal disclaimer isn't translated when Virtual Agent is launched

</td><td>

 

</td><td>

1.  Provision an instance with Virtual Agent \(VA\) for LLM enabled and language plugins installed.
2.  Impersonate a user.
3.  Set the language preference to Japanese.
4.  Turn DT off.
5.  Launch the Virtual Agent chat.

 Expected behavior: The legal disclaimer should be displayed in Japanese.

 Actual behavior: Notice that the static text 'Answers generated by AI. Review for accuracy' isn't translated. It is displayed in English.

</td></tr><tr><td>

Virtual Agent

 PRB1826752

</td><td>

The RAG tool throws an error when passing the '$' symbol in a query from a skill kit

</td><td>

 

</td><td>

1.  Add RAG as a tool to any skill.
2.  Pass '$' in the search query.

 Expected behavior: It should execute without any error.

 Actual behavior: It throws an error.

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1801347

</td><td>

Inbound/Outbound images aren't sent/received

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1817416

</td><td>

UI alignment issue on Now Assist Virtual Agent \(NAVA\) mobile responsiveness

</td><td>

This a UI alignment issue in which the VA window cuts off to the left hand side of the site, and cannot be viewed properly.

</td><td>

1.  Open Customer Service Managment \(CSM\) portal in Android with a Chrome browser.
2.  Select the **Virtual Agent** \(VA\) icon.

 Observe that part of VA window is unaligned and is cut off on the left side of the site, and cannot be viewed properly.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1817637

</td><td>

'Reply' and 'Start new conversation' branding isn't translated

</td><td>

 

</td><td>

1.  Set up NAVA.
2.  Install Spanish.
3.  Set up DT and language detection.
4.  Log in to Service Portal as a Spanish user.

 Observe that the 'Reply' and 'Start new conversation' branding isn't translated.

</td></tr><tr><td>

Work Order Management

 PRB1823305

</td><td>

Work Order Template assignment groups are not honored

</td><td>

When using Work Order templates and setting a specific assignment group, the group is not set and a different group is assigned. Additional fields that are configured on the work order templates can not be processed properly. As a result, fields like **assignment\_group** that will be defined in the WOT of the work order template are not applied properly.

</td><td>

Open a WO using a template with a defined Dispatch and Assignment group of type wm\_dispatch.

 Notice that if the WOT template is viewed separately, there are no choice values in the select box for assignment group.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 3 Hotfix 1](xanadu-patch-3-hf-1.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2 Hotfix 2](xanadu-patch-2-hf-2-PO.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1 Hotfix 3b](xanadu-patch-1-hf-3b.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


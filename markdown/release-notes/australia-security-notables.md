---
title: Australia security and notable fixes
description: The Australia release contains important problem fixes.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 108
breadcrumb: [Available patches and hotfixes, Learn about the Australia release, Australia release notes]
---

# Australia security and notable fixes

The Australia release contains important problem fixes.

-   **Australia was released on March 12, 2026.**
    -   03-04-2026\_1355
    -   glide-australia-02-11-2026\_\_patch0-02-24-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This version is being evaluated for use in the ServiceNow Government Community Cloud \(GCC\) environment.

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/australia/rn/patches/PRBs-A00.00.xlsx).

## Security-related fixes

Australia includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Australia, refer to [KB2770681](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2770681).

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

Access Analysis Instrumentation API

 PRB1904862

</td><td>

MySQL has an out of memory issue due to a complex SQL query

</td><td>

In the RecordInspector class, the fGlideRecord variable is defined as a class-level variable, causing the same query to be reused across all operations. In certain scenarios, this leads to the query reaching the exhaustion limit.

</td><td>

 

</td></tr><tr><td>

Access Control List \(ACL\) Rules

 PRB1910482

</td><td>

Ensures the QueryRangeACLAuditor doesn't generate a security attribute with a blank script

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1836275

</td><td>

ScriptClassifier .isScriptUsingCurrent\(\) returns true despite the 'passed in' string not being current

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1893366

 [KB2476029](https://hi.service-now.com/kb_view.do?sysparm_article=KB2476029)

</td><td>

Query range ACL executes for dynamic filter conditions

</td><td>

When a list is querying for dynamic filter, the query\_range ACL's are executed, resulting in unexpected behavior.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Access Control

 PRB1893600

 [KB2178333](https://hi.service-now.com/kb_view.do?sysparm_article=KB2178333)

</td><td>

RecordFamilyResolver. archiveTable HasACLTerms needs more optimization

</td><td>

There's performance issues with reports on instances with a large number of archive tables.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Access Control

 PRB1900620

</td><td>

An ACL isn't working as expected

</td><td>

A data condition is impacting the list\_edit ACL, but can't be seen or updated due to an introduction to a UI Policy.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1902529

</td><td>

The auto-assignment feature isn't working as expected

</td><td>

The auto-provisioning status displayed in the UI doesn't accurately reflect the current values defined in the sys\_properties \(glide.security. scripting\_role. auto\_provisioning\) table. Changes made to the relevant sys\_properties aren't propagated or updated in the UI as expected.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1907444

</td><td>

An error message occurs randomly on pages related to the AI agent security attribute

</td><td>

This issue occurs in both a global and non-global scope, such as sn\_kb\_social\_qa.

</td><td>

1.  Create an ACL using AI agent security attributes.
2.  Navigate to the ACL form.
3.  Attempt to update the AI agent security attribute.

 Expected behavior: No error message appears on the security attribute pop up window.

 Actual behavior: An error message appears.

</td></tr><tr><td>

Access Control

 PRB1910493

 [KB2321524](https://hi.service-now.com/kb_view.do?sysparm_article=KB2321524)

</td><td>

There is slowness when loading forms with **Table Choice** fields, even after applying a 2000 record limit

</td><td>

The size of CACHE\_ARCHIVE\_TABLE\_HAS\_TERMS cache needs to be higher than 2000 since many instances have &gt; 1000 archive tables.

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

Access Control

 PRB1939961

</td><td>

An incorrect class is passed as context to an ACL

</td><td>

The record expansion for DB view changes between X and Y, resulting in the incorrect class being passed as context to an ACL.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1943406

</td><td>

The **Article Body** \('text'\) field is read-only for new users that inherit the 'knowledge' role from a group.

</td><td>

This issue is only observed in the Zurich family release.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1960642

</td><td>

Remove Datatype ACLs created for HTML and translated\_html datatypes

</td><td>

After upgrading to the Zurich release or later, users without the scripting role \(snc\_required\_script\_writer\_permission\) may be unable to edit HTML and translated HTML fields. Also, non-admin fulfillers can't move problem records from the 'Root cause analysis' state to the next state because they can't input values in specific mandatory fields. Finally, users experience difficulty when updating knowledge base articles following an upgrade, as the article body becomes read-only when attempting to edit.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1981898

</td><td>

Need properties for better control of the scope where a security attribute script gets evaluated

</td><td>

 

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

Activity Stream

 PRB1928872

 [KB2709314](https://hi.service-now.com/kb_view.do?sysparm_article=KB2709314)

</td><td>

The CanReadRepo class encounters a ConcurrentModificationException

</td><td>

This concurrency issue arises because the class uses a HashMap, which is not thread-safe. The HashMap should be replaced with a ConcurrentHashMap to ensure thread-safe operations and prevent the exception.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1942003

</td><td>

Work notes/Comments are unexpectedly cleared when saving a form with an empty mandatory field and the work is lost

</td><td>

When there are any unfilled mandatory fields on the form, the text in the comments/work notes is getting cleared on selecting the **Save** button. It's impacting the user experience. Verified that it works fine in Xanadu and Yokohoma and on other workspaces like CSM/FSM Configurable Workspace.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1946412

 [KB2555553](https://hi.service-now.com/kb_view.do?sysparm_article=KB2555553)

</td><td>

Default AWA chat capacity isn't honored after a Zurich upgrade

</td><td>

After upgrading to a Zurich instance, the default AWA chat capacity isn't honored. Agents are assigned more chats than the defined maximum limit.

</td><td>

Refer to the listed KB article for details.

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

Agile Development

 PRB1924500

</td><td>

No access to portal sections in 'Agile 2.0 Epic Dashboard' for users with the scrum master role

</td><td>

The user with a scrum\_master role should be able to see the Agile 2.0 Epic Dashboard, however they receive a query\_match error on sys\_portal\_ preferences. portal\_section.

</td><td>

1.  Open an instance.
2.  Impersonate the user abel.tuter \(scrum\_user\).
3.  Navigate to **Agile Development** &gt; **Dashboards** &gt; **Agile 2.0 Epic Dashboard**.

 Observe the error message, 'Part of the query on sys\_portal\_preferences has been ignored because of insufficient access for 'query\_match' operation on sys\_portal\_preferences.portal\_section.'

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

AI Search \(Glide\)

 PRB1932287

</td><td>

A null pointer exception \(NPE\) occurs during catalog variable indexing when the choice text is empty

</td><td>

 

</td><td>

1.  Create or edit a catalog variable with choice options.
2.  Leave the **Choice Text** field empty for one or more options.
3.  Trigger the indexing process for the catalog variable.

 Observe that a NPE occurs during indexing.

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1935842

</td><td>

A citation can be dropped when the Genius Results limit is set to 1

</td><td>

When performing AI search on NAVA, the user occasionally doesn't get any response back on NAVA. It shows a blank response.

</td><td>

 

</td></tr><tr><td>

AI Search \(Glide\)

 PRB1937244

</td><td>

java.lang.SecurityException: AisDisableSearchSignalEvent is undefined and may be missing a global qualifier

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search for Service Portal

 PRB1942272

 [KB2608116](https://hi.service-now.com/kb_view.do?sysparm_article=KB2608116)

</td><td>

Users are unable to select multiple facets even when 'multi-select or' is selected in the facet settings

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1765391

</td><td>

A comma-separated list in the **dot\_walk\_fields** field setting causes validation to fail on a facet form

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1823355

</td><td>

When there is no scope or global for a scoped admin scoped app, an invalidate query is sent

</td><td>

AI Search doesn't work as expected and returns no results when searched with any query. On search preview, the message 'An error occurred. Check the logs for more details and contact Support if this issues continues' pops up before the query can even be triggered.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1841579

</td><td>

sn-search-combobox-desktop's use of createGraphQLEffect dispatches errorActionType due to a 401 error for public GraphQL endpoints

</td><td>

The batch request fails due to 401 even though the GraphQL request in the batch was actually successful.

</td><td>

1.  Set the Service Portal home page to public.
2.  Set the Typeahead Search widget to public.
3.  Open Service Portal without logging in.
4.  Open Developer Tools.
5.  Select the 'Search' box.

 Observe in Seismic Dev Tools that the batch request failed due to 401. Then, observe in the Network tab that the GraphQL request in the batch was actually successful.

</td></tr><tr><td>

AI Search

 PRB1888352

 [KB2399571](https://hi.service-now.com/kb_view.do?sysparm_article=KB2399571)

</td><td>

AISearch Conversational CatalogHelpers adds extra overhead on a cs.worker thread, causing performance degradation

</td><td>

The AISearchConversationalCatalogHelpers script include adds additional overhead on cs.worker thread causing performance degradation up to 600ms. The degradation varies based on the number of catalogs for a given search.

</td><td>

Refer to the listed KB article for details.

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

 PRB1910311

</td><td>

NLQ Genius Results \(GR\) doesn't work in portal in ynowassist and znowassist tracks

</td><td>

 

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

Dot-walked **Genius Result** fields are returned with dots instead of underscores

</td><td>

 

</td><td>

1.  Search for Company Policies in /esc portal.
2.  Select the **Company Policies** genius result.

 Observe that the navigated page has no sys\_id.

</td></tr><tr><td>

AI Search UX

 PRB1917739

</td><td>

Add a mechanism to resend recent Asynchronous Message Bus \(AMB\) messages on a created subscription

</td><td>

Under certain circumstances, it's possible that the component establishes the AMB connection after the Genius results are sent through the channel, since both the connection subscription and the Genius results being sent are asynchronous.

</td><td>

 

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

 PRB1952630

</td><td>

Malformed URLs in the streaming chunks for a synthesized response cause the UI to hang

</td><td>

The URL renders stand-alone and sometimes isn't selectable.

</td><td>

 

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

 PRB1972080

</td><td>

Console errors on Service Portal \(SP\) for non-synthesized Genius Results \(GR\) \(although functionally everything works as expected\)

</td><td>

 

</td><td>

1.  On a Yokohama or Zurich instance, disable Synthesized GRs for SP.
2.  Search for a term with which there is more than 1 GR.

 Observe errors in the console such as 'Failed to load @devsnc/sn-search-genius-card-assist'.

</td></tr><tr><td>

Analytics Data API

 PRB1920837

</td><td>

A Platform Analytics dashboard displays 'No data available' when 'Enable Data Cache' is enabled for Indicator Scorecard visualizations

</td><td>

After an upgrade, dashboards widgets of type 'Indicator Scorecard' aren't loading as expected. The error message says 'No Data Available. No content available for the selected criteria'. This issue occurs for both new visualizations and saved visualizations.

</td><td>

 

</td></tr><tr><td>

Analytics Data API

 PRB1926918

</td><td>

The 'Process analytics cache prefetch queue' job leads to OutOfMemoryError and the node restarts

</td><td>

When the user runs the 'Process analytics cache prefetch queue' job, it loops in ChangeCheckConflictsSNC script include.

</td><td>

1.  Create a 'test\_breakdown' table.
2.  Add a field:
    1.  Name: Name.
    2.  Type: String.
    3.  Length: 50.
3.  Populate two million records in the table with names such as Name1, Name2, etc.
4.  Create a breakdown source on test\_breakdown without any condition.
5.  Create a breakdown of the above breakdown source.
6.  Create a 'test\_indicator' table.
7.  Add a field:
    1.  Name: ref\_breakdown.
    2.  Type: Reference.
    3.  Reference: test\_breakdown.
8.  Populate two million records in test\_indicator with reference to all the records in test\_breakdown, respectively.
9.  Create an indicator source based on test\_indicator, without any condition.
10. Create an indicator based on the above indicator source.
11. Navigate to the breakdown created in step five.
12. Add a breakdown mapping on the **test\_incident** and **ref\_breakdown** field.
13. Navigate back to the indicator.
14. Add the breakdown.
15. Change the system properties:
    1.  com.snc.pa.dc.hsql.max\_row\_count\_indicator\_source =&gt; 10000000.
    2.  com.snc.pa.dc.max\_breakdown\_elements\_limit =&gt; 10000000.
16. Collect 1-day score for the indicator.
17. Create a new dashboard.
18. Add a visualization:
    1.  Type: Single score.
    2.  Source: Indicator created in step 10.
19. Add a filter:
    1.  Type: Single select.
    2.  Source: Breakdown created in step five.
20. Open any memory inspection tool and check the current memory footprint.
21. Open the filter and select a value.

 Notice that the memory footprint steadily increases by about 800 million until the score is displayed.

</td></tr><tr><td>

Analytics Data API

 PRB1945218

 [KB2611116](https://hi.service-now.com/kb_view.do?sysparm_article=KB2611116)

</td><td>

There's a memory leak of JSON serializer in the Multivis API

</td><td>

Each time a data request is processed, a new serializer is created and not released unless a GC is performed, which causes a memory leak.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Analytics Data API

 PRB1952604

</td><td>

The data label indicators show the same unit in Platform Analytics Data Visualization

</td><td>

After creating a data visualization that uses two indicators as data sources with different units, the data labels reflect the same unit.

</td><td>

1.  Create a data visualization \(line\).
2.  Add to the data sources with different units \(\# and % for example\).
3.  Show the data label.

 Expected behavior: The data label unit in each indicator reflects the unit of the indicator.

 Actual behavior: The data label units in both indicators are the same, and not respecting the configured unit of the indicators used as a base.

</td></tr><tr><td>

Analytics Export API

 PRB1977069

 [KB2732975](https://hi.service-now.com/kb_view.do?sysparm_article=KB2732975)

</td><td>

Users are unable to schedule data visualizations

</td><td>

This issue occurs when the user is attempting to schedule and send data visualizations as a PPT or PDF file. The mail is not generated after entering the reoccurrence, recipients, and subject and selecting **Save** and **Send Now**. An error is observed in the syslog.

</td><td>

Refer to the listed KB article for details.

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
4.  Let the system continue installation process, during which it downloads a package again and creates a temp directory.

 Observe the error that appears, which includes the text 'Exception reading zip stream, falling back to old cipher' and 'java.io.FileNotFoundException'.

</td></tr><tr><td>

Application Install Engine

 PRB1911704

</td><td>

An error appears while selecting optional spokes and installing SaaS int app

</td><td>

During the preprocessing operation, the user receives an error while selecting optional spokes and installing the SaaS int app. After a second attempt, the locate remote offering plugin record for com.sn\_sam\_saas\_int can't be located.

</td><td>

1.  Provision an instance with com.sam.saas.int installed on a multi node environment and optional plugins installed on another node.
2.  Try to repair the app.

 Observe that an error appears.

</td></tr><tr><td>

Application Manager

 PRB1889269

</td><td>

Progress worker state isn't set to complete after worker is finished

</td><td>

Installing plugins shows an error even when successfully completed. In the logs, it looks like the error comes from a script include. Previously, the code block was a part of a larger function that had appVersion and appID as parameters. The code was refactored into the forceSyncWithStore function, which doesn't have appVersion and appID as parameters. If the gs.info line is reached, it throws an error because those two fields were not passed into the function.

</td><td>

1.  Install the custom scoped app \(e.g., x\_conym\_atf\_sc\_req, x\_conym\_hrp\).
2.  Check 'sys\_upgrade\_history' to confirm the installation is marked as 'complete'.
3.  Check 'sys\_progress\_worker' list for the message 'Progress worker state is not set to complete after worker is finished.'
4.  Check 'syslog' for the error 'com.glide.script.RhinoEcmaError: 'appVersion' is not defined.'

</td></tr><tr><td>

Application Manager

 PRB1907408

</td><td>

A rollback is blocking the install/upgrade for non-global scope users in a domain-separated instance

</td><td>

Non-global domain users have been blocked from being able to install/upgrade on domain-separated instances. There is now a fix to allow this behavior and hence this code change made on App Manager can now be rolled back.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1981044

 [KB2719949](https://hi.service-now.com/kb_view.do?sysparm_article=KB2719949)

</td><td>

The latest version in the sys\_store\_app table is updated to the installed version after an install, thereby causing the **Upgrade** button to be unavailable in App Manager

</td><td>

Two functions \(\_fixLatestVersion ForWithdrawn InstalledApps, \_fixLatestVersion ForWithdrawn InstalledCustomizations\) in Application Manager's UpdateChecker. checkAvailableUpdates API \(aka Sync in the UI\) were missing a required GlideRecord.addQuery constraint when the 'sn\_appclient. enable\_app\_ manager\_checksums \_cache' sys\_property was set to true \(default\). This issue led to the latest\_version being set to the incorrect values on Install/Sync.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1986694

 [KB2753355](https://hi.service-now.com/kb_view.do?sysparm_article=KB2753355)

</td><td>

App Manager and My Company Applications incorrectly shows available updates after update checker

</td><td>

When publishing a new version of the app, it doesn't appear in 'My Company Application'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Appointment Booking

 PRB1940645

</td><td>

A datepicker isn't selectable until the page is refreshed

</td><td>

If the user loads an appointment booking on a portal home page and then uses the Service Portal \(SP\) date picker on a different portal page, the datepicker won't be selectable until the page is refreshed.

</td><td>

 

</td></tr><tr><td>

Asset Management

 PRB1894759

 [KB2609881](https://hi.service-now.com/kb_view.do?sysparm_article=KB2609881)

</td><td>

The **Currency** field on the 'Contract' form multiplies with 100 for some currencies

</td><td>

In the user's instance, the user profile has the country code set to one that uses a comma as the decimal separator, specifically Europe/Sweden \(SE\). Because of this, each time the form is loaded, the value gets multiplied by 100 due to the logic in the onLoad client script.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Asset Management

 PRB1947295

 [KB2570280](https://hi.service-now.com/kb_view.do?sysparm_article=KB2570280)

</td><td>

There's an error when creating an asset when populating a serial number

</td><td>

Notice the error message: 'onChange script error: TypeError: Cannot read properties of undefined'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Asset Management

 PRB1963341

</td><td>

The 'sn\_itam\_common.CommonMobileUtils' script include doesn't exist in the system

</td><td>

Asset Management Common plugins aren't activated as a dependency of IT Asset Management mobile. Even when activated, the script include used in the mobile action item is missing.

</td><td>

 

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1909861

</td><td>

A lazy load of Asynchronous Message Bus \(AMB\) messages cause an additional query for every message published

</td><td>

A performance improvement implemented in Yokohoma was designed to optimize database operations by loading the actual AMB message column from the database only when subscribers for that message exist. However, this optimization has been compromised by a request that updates the redelivery cache, which inadvertently causes the new query to be triggered for every published message, regardless of subscriber status. The intended performance benefit of selective database querying is being negated, as the system is now querying the database for all messages instead of only those with subscribers.

</td><td>

 

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

 PRB1910946

</td><td>

The Record Watcher \(RW\) Asynchronous Message Bus \(AMB\) message censor doesn't work when AMB lazy load is turned off

</td><td>

When glide.amb.messages.lazy.load.data is set to 'false', having a record open in two browsers and updating it in one doesn't update it in the other browser.

</td><td>

1.  Set glide.amb.messages.lazy.load.data to 'false'.
2.  Open a record in two different browsers.
3.  Update the record in one browser.

 Notice that the **Record** field in the other browser window isn't updated.

</td></tr><tr><td>

Attachments to Records

 PRB1889947

</td><td>

Instance nodes do not appear and this error appears: javax.crypto.AEADBadTagException: Error finalising cipher data: mac check in GCM failed

</td><td>

Instance JVMs won't start after the error, ' java.io.IOException: javax.crypto.AEADBadTagException: Error finalising cipher data: mac check in GCM failed'.

</td><td>

 

</td></tr><tr><td>

Attachments to Records

 PRB1950689

 [KB2612680](https://hi.service-now.com/kb_view.do?sysparm_article=KB2612680)

</td><td>

After upgrading to Zurich, the attachment variable within the record producer isn't incorporated into the activity stream

</td><td>

This issue was verified by modifying the 'Ask a question' record producer in a base instance. An attachment variable is added and the attachment appears in the activity stream. However, performing the same test in the Zurich release did not result in the attachment being shown in the activity stream.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Audit History

 PRB1938364

 [KB2531096](https://hi.service-now.com/kb_view.do?sysparm_article=KB2531096)

</td><td>

A large amount of history \(audit\) data can lead to node memory contention on a node when loading a form

</td><td>

When loading a form for the first time, the node may run out of memory and crash. This happens if the history set has to be built to load the activity stream and if there's a lot of data to be loaded.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1927594

 [KB2423799](https://hi.service-now.com/kb_view.do?sysparm_article=KB2423799)

</td><td>

Oauth token calls fail from an API authenticated sessions

</td><td>

As part of multi-factor authentication enforcement for local internal user logins, adaptive authentication is enabled and configured the MFA context policy. Once an API authenticated session is established, it's expected to make only API integration \(or non-interactive\) related calls, and the '/oauth\_token.do' call falls outside of integration calls.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1947882

</td><td>

After upgrading within Yokohama, the email MFA option is missing and only TOTP is shown

</td><td>

After upgrading, users are no longer able to see the email multi-factor authentication \(MFA\) option during login. Only the Authenticator App \(TOTP\) is displayed, even after selecting **Try another way to verify**.

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1960277

</td><td>

An Supplier Lifecycle Operations \(SLO\) error displays when the SLO URL is empty in Identity Provider \(IdP\) configuration

</td><td>

When the **SLO \(single logout\) URL** field is left empty in the IdP configuration, the system redirects to external\_logout\_complete with an error code slo\_error. However, this behavior is incorrect. Since SLO is optional, the absence of an SLO URL shouldn't trigger an error. This issue also appears in mobile.

</td><td>

1.  Navigate to the 'IdP Configuration' page.
2.  Ensure that the SLO URL is left empty.
3.  Log in using the configured IdP.
4.  Log out.

 Expected behavior: The system should successfully log out and redirect to the external\_logout\_complete page without any error code, since SLO is optional.

 Actual behavior: The system redirects to external\_logout\_complete with error code slo\_error, implying a failure even though SLO wasn't configured.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1900486

</td><td>

'Run Server Side Validation Script' is not supported by reusable tests

</td><td>

The main test fails with the message, 'Unable to find step configuration 'Execute Test: reusable \(multi steps\)' with sys\_id '' for step with order 1.'

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1924154

</td><td>

Attempting to run a non-UI test in Cloud Runner results in the individual tests being 'Pending' forever

</td><td>

This also occurs if running through the CICD Run ATF Suites API and setting 'run in cloud' to true.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1951016

 [KB2579637](https://hi.service-now.com/kb_view.do?sysparm_article=KB2579637)

</td><td>

All steps in Automated Test Framework \(ATF\) pass a test, but UI tests with many console logs fail

</td><td>

This issue specifically occurs when any single UI batch in an ATF test produces more than 1 megabyte worth of console logs \(approximately 500,000 characters worth of data\).

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1959359

</td><td>

There's an issue with the clean-up job for metadata tracing out of memory: sysauto\_script.do? sys\_id=26c1592 cff442210940 effffffffff0b

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Cache

 PRB1955869

 [KB2595527](https://hi.service-now.com/kb_view.do?sysparm_article=KB2595527)

</td><td>

The ScriptEnginesTables cache is undersized in the Zurich release, causing increased processing time

</td><td>

If an instance has more than 50 script engines installed \(via plugins and applications\), setting the current size to 50 for the ScriptEnginesTables cache may lead to an increase in processing times. This could lead to semaphore contention and/or exhaustion, resulting in a significant increase in total transaction time and processing time and script time.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1880009

</td><td>

Attachments aren't uploaded in the 'Agent Chat' window from HR Agent Workspace

</td><td>

This is happening for HR Core.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1905312

 [KB2415334](https://hi.service-now.com/kb_view.do?sysparm_article=KB2415334)

</td><td>

The 'Feedback definition' table doesn't display any feedback records

</td><td>

Feedback definitions aren't visible. Also, users can't create a feedback definition.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

CI Lifecycle Management API

 PRB1772623

 [KB2518604](https://hi.service-now.com/kb_view.do?sysparm_article=KB2518604)

</td><td>

List view does not translate non-English languages for Lifecycle Stage and Lifecycle Stage status

</td><td>

This issue occurs when the user's language preference is set to a non-English language.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

CMDB Data Manager

 PRB1892066

 [KB2217546](https://hi.service-now.com/kb_view.do?sysparm_article=KB2217546)

</td><td>

A policy form doesn't honor retirement definitions correctly in enforced conditions when multiple retirement definitions are enabled

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

CMDB Data Manager

 PRB1943938

</td><td>

The Data Manager policy jobs experience increasing slowness creating tasks when processing large data sets

</td><td>

The CMDB Data Manager policy for running jobs keep running for a long time because the underlying SQL query has pattern of LIMIT and OFFSET on the CMDB table. The table has a lot of data, and thus those SQL queries start showing increased execution time, effectively slowing the job running them.

</td><td>

 

</td></tr><tr><td>

CMDB Data Manager

 PRB1964689

</td><td>

CMDBRetirementScriptableAPI doesn't handle policies targeting tables that don't begin with 'CMDB'

</td><td>

Data Manager policies that target only tables without 'CMDB' in the start of the table name can't be published or run due to the API not correctly handling the search for those tables' defined retirement state.

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB1955881

</td><td>

sn\_cmdb.\_\_rel\_type\_cache holds a lot of memory

</td><td>

 

</td><td>

 

</td></tr><tr><td>

CMDB Identification and Reconciliation

 PRB1957741

</td><td>

On the CMDB Health Dashboard, a parent metric, like completeness, displays a total count of less than one of the sub-metric \(required or recommended\)

</td><td>

This causes totals to be incorrect.

</td><td>

 

</td></tr><tr><td>

CMDB Query Builder

 PRB1952766

 [KB2634786](https://hi.service-now.com/kb_view.do?sysparm_article=KB2634786)

</td><td>

Calls to QueryBuilder from ServiceMapping return no results when executing in the new V2 mode

</td><td>

In Zurich, processes that call into Query Builder can have no results returned. There are two scenarios where this occurs. Firstly, a service CI populated via CMDB Group containing a saved query \(as constructed in Query Builder\) can have no 'svc\_ci\_assoc' records, even when rerunning the service population. However, the expected CIs will appear when viewing the CMDB Group or the saved query directly. Secondly, instances configured to use 'Zing' for Global Search don't return any CI records in the findings. These different methods both rely on the 'CMDBGroup' API, which may not return results of query execution when using the 'v2' execution mode introduced in Zurich. Instances are at risk if they use dynamic CI groups which are built using Query Builder, they're on an impacted Zurich Version, and the system property glide.cmdb.query.execution\_mode = 'v2'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

CMDB Query Builder

 PRB1977703

 [KB2727703](https://hi.service-now.com/kb_view.do?sysparm_article=KB2727703)

</td><td>

Query Builder in V2 mode can cause memory issues due to a static variable

</td><td>

An internal variable which is declared as static keeps being appended and thus creates a large memory footprint. This would happen if one or more queries are executed enough times to bloat this variable.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Column Level Encryption Enterprise

 PRB1957091

</td><td>

Sys attachments zip data and Column Level Encryption jobs aren't completed

</td><td>

Sys attachments zip data and Column Level Encryption jobs aren't completed even when the CLE Migration Dashboard correctly reads this property and displays 'migration success' and com.glide.cle.allow\_ec\_key\_deletion is set to 'true'.

</td><td>

1.  Navigate to the filter navigator.
2.  Remove triple DES usage.

 Observe that column level encryption data migration isn't completed. Notice that the sys\_property 'com.glide.cle.allow\_ec\_key\_deletion' is set to true. The CLE Migration Dashboard correctly reads this property and displays 'migration success'.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1909893

 [KB2250398](https://hi.service-now.com/kb_view.do?sysparm_article=KB2250398)

</td><td>

The 'Run' filter can apply an old condition and not pick up the newly applied filter conditions

</td><td>

In the CMDB Relationship editor, the filter can apply old conditions and not pick up the newly applied filter conditions. This issue isn't consistently reproducible but there's a problematic API call made.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1924215

</td><td>

The 'Owned By' \(search\) reference dialog doesn't close, and nothing happens after selecting the selected user

</td><td>

This occurs in the CSDM Application Service form view.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1930654

</td><td>

The legacy health dashboard doesn't tell the user that the dashboard is deprecated/no longer supported

</td><td>

Users have bookmarked, saved, or edited links to the legacy health dashboard, meaning they can still access it. There's a lot of confusion on why the dashboard is no longer working as intended. There should be a message to tell the user this dashboard has been migrated to CMDB Workspace.

</td><td>

1.  Check out a Washington DC instance.
2.  Make a favorite for Health Dashboard - CMDB view.
3.  Upgrade your instance to X+.
4.  Select the bookmark for the CMDB view.

 Expected behavior: When users navigate to the legacy dashboard, they should be able to see a message telling them to use the new health dashboard and that the legacy dashboard is no longer supported.

 Actual behavior: Observe that the legacy health dashboard has some broken widgets, no colors, etc. but there is no indication that this dashboard is retired or has been migrated.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1949356

</td><td>

The exact count match check results in an incorrect duplicate task creation

</td><td>

After upgrading to Zurich, de-duplication \(dedupe\) tasks are created incorrectly under certain scenarios. As a result, a large number of records are created in the duplicate\_audit\_result table, causing significant database growth. Instead of updating existing entries, new records are inserted during each subsequent run. In one scenario, the de-duplication tasks are created when they were previously working. In another scenario, users with many hosts that contain cmdb\_serial\_number records with the same serial\_number and serial\_number\_type notice that the number of duplicate\_audit\_result can grow to be tens of millions daily.

</td><td>

 

</td></tr><tr><td>

Connections and Credentials

 PRB1974412

 [KB2730719](https://hi.service-now.com/kb_view.do?sysparm_article=KB2730719)

</td><td>

Certain outbound HTTP requests fail randomly with '401 unauthorized' even though valid tokens exist

</td><td>

While executing outbound HTTP request using REST step, the request misses the authorization header even though the valid OAuth token exists.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Contract Management

 PRB1913448

</td><td>

The payment amount and total amount are incorrectly displayed in the local currency value under USD currency

</td><td>

When the user sets a payment amount using a local currency \(for example, NOK\) when selecting **Adjust** on the contract, the payment amount gets saved on the XML. When re-opening the record in the 'Form' view, it defaults to USD, but shows the amount that originally belonged to NOK. This behavior applies to both **payment\_amount** and **total\_cost** fields.

</td><td>

1.  Open a contract from the ast\_contract table.
2.  Select **Adjust**.
3.  Enter a new payment amount and currency, for example, NOK 966.00.
4.  Search and view the same Contract on List view.
5.  Notice that payment amount and total amount are both reflected as \(NOK\)966.00 and \(USD\)96.7669 when selecting **Toggle currencies**.
6.  Open the record in the 'Form' view.

 Notice that the payment amount is USD 966.

</td></tr><tr><td>

Core Platform

 PRB1593473

</td><td>

Performance Dashboard requests time out for instances with a large number of MID servers

</td><td>

It requests a time out when they call new Diagnostics\(\) on the widgets in the Diagnostics dashboard because that script include accumulates all the data from each node's **node\_stats** field. When there are many MID servers and nodes, parsing XML files can take longer than timing out. The mid-server portion is coming from the 'instance' XML stats include, which is part of the list of includes that is stored in the referenced node\_stats record and one of the includes in the 'glide.cluster.xmlstats' property. XMLStatsInstance.java is the class for this.

</td><td>

 

</td></tr><tr><td>

Core Platform

 PRB1644827

 [KB1648914](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648914)

</td><td>

There's errors when committing an update set that creates a child table with a **Function** field

</td><td>

Version loading is stopped by DictionaryUpdateLoader for sys\_dictionary\_table\_name\_null. Committing an update set that creates a child table with a **Function** field fails. The update set log produces errors.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Currency Administration

 PRB1930077

 [KB2481239](https://hi.service-now.com/kb_view.do?sysparm_article=KB2481239)

</td><td>

The 'Exchange Rate Schedule' job has been replaced by the 'Update Currency Conversion Rates' job in Yokohama

</td><td>

Updating the steps to use currency conversion rates.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Compaction

 PRB1816028

</td><td>

The 'Unexpected Compactor' job runs on the sys\_attachment\_doc table, causing an outage

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Database Indexes

 PRB1901971

 [KB2206973](https://hi.service-now.com/kb_view.do?sysparm_article=KB2206973)

</td><td>

A missing index on the 'sys\_id' column of the 'cmdb\_qb\_result\_base' table causes a replication lag when the table size is large

</td><td>

The index on the 'sys\_id' column of the 'cmdb\_qb\_result\_base' table is missing on 14000+ instances. Due to this missing index, when the 'Table Cleanup on Query Status' \(qb\_query\_status\) table is triggered on such instances, it can lead to replication lag issues, especially when large volumes of records need to be deleted from the qb\_query\_status table. This can lead to memory exhaustion, and records are not properly cleaned up.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1829096

</td><td>

There's an incorrect timeref display value for ISO week 53

</td><td>

It's cosmetic as only the axis labels are affected and the real values are preserved.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1834259

</td><td>

A syntax error or access rule violation is detected by a database

</td><td>

The following error is displayed when a glidefunction column is used as a sort in a list view with a filter on a denormalized glidelist: '\(ERROR: for SELECT DISTINCT, ORDER BY expressions must appear in select list Position: 2328\)'.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1864866

</td><td>

The CMDB table record on sys\_db\_object is not loading, and the transaction is cancelled due to the large number of CMBD columns and indexes on the CMBD table

</td><td>

The slowness is observed on MariaDB hosted instances as well.

</td><td>

1.  Log in to an instance as a user with elevated privileges.
2.  Open sys\_db\_object table.
3.  Search for the name 'cmdb'.

 Notice that the transaction keeps loading for 5 minutes and eventually cancels out. A similar call stack is observed when loading the 'v\_index\_creator\_list' with the filters as 'reference table' is 'Base Configuration Item'.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1922171

 [KB2617119](https://hi.service-now.com/kb_view.do?sysparm_article=KB2617119)

</td><td>

The CONTAINS query interferes with the RLQUERY in a hybrid table

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1924708

</td><td>

'Show Matching' a list and 'order by' **ref\_** fields throws a null pointer exception

</td><td>

After the user orders the list, the records disappear.

</td><td>

1.  Navigate to task.list.
2.  Open **Configure** &gt; **List Layout**.
3.  Add the planned start date \[change request\] to the list of columns.
4.  Save.
5.  Add watch list to the view.
6.  Populate the watch list of some records.
7.  Show Match watch list.
8.  Order by the planned start date \[change request\].

 Expected behavior: The records show.

 Actual behavior: The records disappear.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1925389

</td><td>

Glide queries that use a search term query in conjunction with an order-by on a **Date-time** field return a null pointer exception

</td><td>

For instances running on RaptorDB, Glide queries that use a search term query in conjunction with an order-by on a **Date-time** field return a null pointer exception for matching records that have a null order field value.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1944805

 [KB2552260](https://hi.service-now.com/kb_view.do?sysparm_article=KB2552260)

</td><td>

getDisplayValue\(\) throws a null pointer exception on many types of catalog variables

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Access

 PRB603878

 [KB0621061](https://hi.service-now.com/kb_view.do?sysparm_article=KB0621061)

</td><td>

Condition Builder causes an exception when using a 'matches regex' condition

</td><td>

When the user tries to use a 'matches regex' condition, the following error appears: 'Syntax Error or Access Rule Violation detected by database \(You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'MATCH\_RGX 'pmon'' at line 1\)'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1868796

 [KB2071053](https://hi.service-now.com/kb_view.do?sysparm_article=KB2071053)

</td><td>

Updating a record in the sn\_vul\_vulnerability table via 'Data Management Update' jobs \(sys\_dm\_update\) throws an error

</td><td>

The user can open a record in the sn\_vul\_vulnerability table and update it, but when the same user tries to update it via the sys\_dm\_update job, it throws an error. Error: 'The user does not have the necessary permissions to update records in table sn\_vul\_vulnerability'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1891527

</td><td>

Workflows aren't properly evaluating conditions to determine if tasks should fire

</td><td>

Filter conditions work differently between Xanadu and Yokohama instances.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1904961

 [KB2328103](https://hi.service-now.com/kb_view.do?sysparm_article=KB2328103)

</td><td>

DB compaction fails when there's a table with more than the MAX\_INT number of rows

</td><td>

A user has a sys\_audit table that has almost 8 billion rows. The query that fetches the size of tables parses out the number of rows as integer, which causes this error. There isn't a way to prevent it from reading the results for certain tables: '...worker.2 worker.2 txid=9f2eff89c30a CompactionQualificationJob SEVERE \*\*\* ERROR \*\*\* Compaction qualification failed java.sql.SQLException: Out of range value for column 'table\_rows' : value 7854795901 is not in class java.lang.Integer range...'.

</td><td>

1.  Insert more than the largest value of a Java integer number of rows into a table.
2.  Run the 'DB compaction' job.
3.  Check that the job completes.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1908446

 [KB2256996](https://hi.service-now.com/kb_view.do?sysparm_article=KB2256996)

</td><td>

Turn off the 'Collect Reliability Metrics for Data Management' job

</td><td>

'Collect Reliability Metrics for Data Management' leads to long running queries when the TableStatsService API / Reliability metrics API is called on large tables with conditions. It causes performance issues.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1949832

</td><td>

The 'Physical Table Stats Gatherer' job runs long due to an influx of query with hash 943940198

</td><td>

This occurs after the user upgrades to Zurich. Due to the slow query, the job ran more than two days.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1988503

 [KB2764725](https://hi.service-now.com/kb_view.do?sysparm_article=KB2764725)

</td><td>

Active subflow executions with clean parent flow executions are listed as 'Unreferenced Records' and are deleted by DMUnreferencedRecordCleaner

</td><td>

This issue was observed in Zurich. If a parent flow completes while an associated asynchronous subflow continues running, the completed parent flow context is cleaned up by the retention policy by routine system cleanup. As a result, the running subflow becomes unreferenced, and may be removed during routine system cleanup.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1860663

</td><td>

An index is created without a size limit for some unbounded fields, which leads to errors while creating an index or adding data

</td><td>

The 'AWS Service Catalog Connector' \( x\_126749\_aws\_sc\) installation is left with an invalid index in the 'Task' table in RaptorDB. There's an error: 'SEVERE \*\*\* ERROR \*\*\* Exception executing deferred indexes for class: task...'

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1906463

</td><td>

Excessive DBConnectionPools messages in logs results in multiple default semaphores

</td><td>

Both UI and worker nodes are impacted.

</td><td>

1.  Make DB connection open requests slow \(10+ seconds wait\).
2.  Generate some load to exceed connection pool size/UI transaction semaphore count.

 Observe that UI threads are getting stuck on a connection pool while it's blocked waiting for a connection to be created.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1928008

 [KB2428930](https://hi.service-now.com/kb_view.do?sysparm_article=KB2428930)

</td><td>

An upgrade to Yokohama hangs

</td><td>

Upgrades to Yokohama releases may hang for certain instances because of contention on the query registrar.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1959979

</td><td>

'Get connections from secondary pool' doesn't retry more than once

</td><td>

The retry count is capped because failImmediate is always set to true for secondary pools. This causes some issues with read replica routing.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1848049

</td><td>

Add support for a new RaptorDB feature to prevent DDL locking

</td><td>

DDL locking occurs when a long running query is executed.

</td><td>

1.  Execute a long running query against Postgres.
2.  Attempt to alter a table using an instant operation.

 Notice that DDL blocks all traffic until the long running query finishes.

</td></tr><tr><td>

Database Persistence

 PRB1937018

</td><td>

dbi.truncateTable\(table\_name\) is truncating a table name when the table name is &gt;29 characters and the 'Daily schedule' job isn't able to drop that table

</td><td>

In recent releases, DBTruncateUtil.truncateTable\(\) calls for tables with long names leave orphaned tables behind in the DB and causes backups to fail.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1971863

</td><td>

Transaction canceled: 'Failed to get database connection due to exhaustion of connection pool on the node'

</td><td>

A spike in requests can produce a demand exceeding pool max capacity. Some connections are created, but the process is slow, causing various race conditions and delays and eventually causing a timeout in one operation.

</td><td>

 

</td></tr><tr><td>

Database Views

 PRB1826155

 [KB2243925](https://hi.service-now.com/kb_view.do?sysparm_article=KB2243925)

</td><td>

Boolean string literals in a view table produce an error or cause the wrong results to be returned

</td><td>

The fix for PRB1764595 does not address the issues caused by boolean string literals in a view table that produce an error or cause the wrong results to be returned.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Views

 PRB1900333

</td><td>

Querying a database view using an IN query on the view's sys\_id uses a list of encoded sys\_id values, resulting in an invalid query in Yokohama

</td><td>

When a database view is queried a sys\_id, a unique value is generated by encoding the sys\_ids from the matching joined records from each view table, which results in the row being returned.

</td><td>

 

</td></tr><tr><td>

Data Fabric Table Glide Services

 PRB1937036

</td><td>

Data Fabric memory usage of GlideTableInfo

</td><td>

Performance testing on an instance experiences out of memory issues and node restarts when a long running transaction or a high number of transactions are executed. About 6.1% of the total memory is used by the JVM in a heap dump using GlideTableInfo.

</td><td>

 

</td></tr><tr><td>

Data Privacy \(Classic\)

 PRB1881041

</td><td>

The **New** button displays on related lists where it isn't configured

</td><td>

 

</td><td>

1.  Provision an instance with the GRC: Advanced Risk and GRC: Risk Management Workspace plugins installed.
2.  Open the 'Lists' page in the Risk Workspace.
3.  Navigate to 'Risk assessment project' section.
4.  Select the **New** button visible at the top right on the list page.
5.  Fill all of the required fields.
6.  Make sure the impersonating user is set as the owner.
7.  Move the project to the 'Risk scoping stage'.

 Observe the **New** button that's visible on the 'Risks' related list.

</td></tr><tr><td>

Decision Table \(Family\)

 PRB1930728

</td><td>

Adding a new choice to a choice type results in a decision table

</td><td>

The user should be able to create a choice type result with a new choice result, or add a new choice to the choice type result in a decision table. However, there's an error.

</td><td>

1.  Create a decision table and add at least one input and one condition.
2.  Create a choice type result with a new choice list.

 Notice that the user can create a result type choice, but it gives an error whenever they try to add new choice in choice list.

</td></tr><tr><td>

Decision Table \(Family\)

 PRB1971318

</td><td>

Users are unable to publish decision tables

</td><td>

The decision table isn't published and a 'Could not update the decision table' message is displayed.

</td><td>

1.  Create a decision table with a result column of type choice and capture it in update set.
2.  Create new choice and add a couple of choices.
3.  Import the decision table into another instance.
4.  Publish the decision table to move it from draft to publish.
5.  Then move it draft state and publish again.

 Expected behavior: The decision table should be published.

 Actual behavior: The decision table isn't published and the 'Could not update the decision table' message is displayed.

</td></tr><tr><td>

Declarative Actions

 PRB1975231

</td><td>

Field decorators for variable fields are cached in a way that causes issues, causing them to not show up sometimes

</td><td>

 

</td><td>

1.  Create a variable set.
2.  Create a catalog item for specific catalogs only.
3.  Add the catalog item to the included in list for the variable set.
4.  Navigate to the catalog item.
5.  Select **Try it**.
6.  Order the item.
7.  Navigate to the request record.
8.  Navigate to the related list.
9.  Navigate to the request item record.
10. Note the sys id and visit the record in workspace.
11. Add a reference variable to the variable set created above.
12. Navigate to the catalog item.
13. Try it again.

 Following the same steps above, users end with the variable fields in workspace without field decorators.

</td></tr><tr><td>

Discovery

 PRB1509705

 [KB0967278](https://hi.service-now.com/kb_view.do?sysparm_article=KB0967278)

</td><td>

The Simple Network Management Protocol \(SNMP\) object identifier \(OID\) 1.3.6.1.4.1.1602.4.7 is discovered as 'Network Multi-PDL Printer Board-D1/H1' and is used by many different families and models of Canon multi-function printers

</td><td>

The SNMP Classification OID record 1.3.6.1.4.1.1602.4.7 is used by whole families of Canon multi-function printers. This OID record causes them all to be model 'Network Multi-PDL Printer Board-D1/H1' regardless of the true family/model.

</td><td>

Discover a Canon printer with the OID 1.3.6.1.4.1.1602.4.7.Expected behavior: Either the make/model needs to be extracted from the other OID data, such as sysDesc, or no model name entered in this OID.

Actual behavior: The Printer CI will be created with Model 'Network Multi-PDL Printer Board-D1/H1', which is incorrect.

</td></tr><tr><td>

Discovery

 PRB1636956

 [KB1224543](https://hi.service-now.com/kb_view.do?sysparm_article=KB1224543)

</td><td>

Perform Refresh Member accounts' Discovery is stuck in active state because of service\_account\_reload system commands in ECC queue

</td><td>

This is not related to the **Refresh Member Accounts** UI action. 'Perform Refresh Member accounts' is triggered by Cloud Schedule when glide.discovery.cdu.auto\_ refresh\_sub\_accounts\_and\_ldcs is set to 'true'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1681006

 [KB1641144](https://hi.service-now.com/kb_view.do?sysparm_article=KB1641144)

</td><td>

Object identifier \(OID\) records for Cisco ASA-55xx Firewalls are not consistently using the Next-Generation Cisco Firewall Discovery pattern and Cisco Firewall Device \[cmdb\_ci\_firewall\_device\_cisco\] CI class

</td><td>

There are 111 OID records included out-of-box for Cisco ASA 5500 series Firewalls. Only 7 of these are set for the correct classifier/table and Next-Generation Cisco Firewall Discovery pattern. Of the remaining, 26 are set to the generic IP Firewall \(cmdb\_ci\_ip\_firewall\) class and probe, which is acceptable, but doesn't fully discover the device. However, 27 are set as routers, and 51 as switches, which is incorrect.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1752501

 [KB1639128](https://hi.service-now.com/kb_view.do?sysparm_article=KB1639128)

</td><td>

Different certificate checks between VMWareVCenterVMTagsProbe and VMWarevCenterVMsProbec / cVMWarevCenterDatastoresProbe

</td><td>

When doing VMWare Discovery currently, there are different certificate checks between VMWareVCenterVMTagsProbe and VMWarevCenterVMsProbe/ VMWarevCenterDatastoresProbe. Certificate checks are only being done when one wants to discover VMWareVCenterVM tags.

</td><td>

1.  Run VMWare Discovery.
2.  Discover tags.

 Expected behavior: The MID Server platform's MID Security policy should be left to define whether certificate checks are needed or wanted for the vCenter endpoint.

 Actual behavior: VMWareVCenterVMTagsProbe does a certificate check itself, which isn't needed.

</td></tr><tr><td>

Discovery

 PRB1833795

 [KB1825538](https://hi.service-now.com/kb_view.do?sysparm_article=KB1825538)

</td><td>

The credential alias doesn't work for applicative credentials

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1862106

 [KB2436326](https://hi.service-now.com/kb_view.do?sysparm_article=KB2436326)

</td><td>

Global IP exclusion isn't working for a cloud VM schedule

</td><td>

Not all the global exclusions are working for a Cloud Discovery.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1898321

 [KB2260681](https://hi.service-now.com/kb_view.do?sysparm_article=KB2260681)

</td><td>

Logs for patterns execution on Discovery logs need to be less alarming

</td><td>

Discovery logs for patterns indicate a pattern failure 'Failed Exploring CI Pattern', even though the pattern brought data back.

</td><td>

1.  Run lab and cloud discoveries.

Notice that this should give a variety of errors or use attached update set, which has dummy patterns that fail in different use cases.

2.  Look at the Discovery log.

 Notice that 'Failed Exploring CI Pattern' occurs for discoveries that actually brought data.

</td></tr><tr><td>

Discovery

 PRB1919668

 [KB2588245](https://hi.service-now.com/kb_view.do?sysparm_article=KB2588245)

</td><td>

There's an error during a new certificate request creation for letsencrypt

</td><td>

Discovery's 'Discovery - Update status started count' business rule runs for ecc\_queue ouput inserts that aren't actually from Discovery. This causes an error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1925275

</td><td>

Inconsistent behavior in Discovery's status **Started** and **Completed** counts and **State** fields

</td><td>

When the user runs quick Discovery, the Discovery status' **State** is either stuck in 'Active' or 'Starting' states. The **Started** or **Completed** counters stay on count 0 and there is no progress despite successful Discovery.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1927941

 [KB2434137](https://hi.service-now.com/kb_view.do?sysparm_article=KB2434137)

</td><td>

Discovery patterns failed prematurely, causing Discovery failure

</td><td>

An example is during 'Windows OS - Server' pattern Discovery running the Cluster pattern library throws consecutive errors, which should be expected, but the pattern engine failed the pattern instead.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1930200

 [KB2474013](https://hi.service-now.com/kb_view.do?sysparm_article=KB2474013)

</td><td>

The 'Protected Tables' plugin blocks DiscoverySensorJob logging and causes warnings about syslog inserts from ProtectedTableAccessHandler instead

</td><td>

When the 'Protected Tables' Plugin is active, which is recommended, the source= DiscoverySensorJob GlideRecord inserts made directly to the syslog table by Discovery's 'DiscoverySensorJob' script include are blocked, and flood the syslog table with logs from source=ProtectedTableAccessHandler instead.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1933785

</td><td>

A Cloud Discovery schedule incorrectly maps all related service accounts even when the 'Discover all Related accounts' toggle is unchecked

</td><td>

When creating a Cloud Discovery schedule for a project and unchecking the 'Discover all Related accounts listed below' toggle, the schedule still maps to all service accounts under that folder level. This behavior is intermittent and has been reproduced on multiple environments. The UI script logic doesn't correctly handle timing between setAllSubAccSelected and getSubAccountsOfMasterAccount. As a result, subAccountsList is reset incorrectly, leading to unintended account mappings.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1953520

 [KB2718488](https://hi.service-now.com/kb_view.do?sysparm_article=KB2718488)

</td><td>

ecc\_queue input records are stuck in IP jail, causing status cancellation

</td><td>

IPs are placed in a jail if it is suspected that multiple IPs on a schedule belong to the same device. IPs are supposed to be released from jail when the Discovery of the device is complete. When this occurs, the IPs are never released from jail.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery Probes and Sensors

 PRB1960340

 [KB2611107](https://hi.service-now.com/kb_view.do?sysparm_article=KB2611107)

</td><td>

Discovery's MID Server script files for Application Dependency Mapping are deleted during clones

</td><td>

The MID Server script file \(ecc\_agent\_script\_file\) records have attachments. These attachments may go missing after the instance is cloned, breaking Discovery probes. To retain the attachments of base instance code-related records in clones, the table\_name in the sys\_attachment table must be prefixed with ZZ\_YY. Discovery's names don't have that prefix, so the attachments may not be copied depending on the preserver/exclude settings for the clone.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1876011

</td><td>

A conversation hangs after a topic is selected

</td><td>

In the syslogs related to DocIntel, scheduled job errors occur.

</td><td>

1.  Navigate to the Employee Service Center.
2.  Enter the prompt, 'I need to borrow a loaner laptop for work by tomorrow'.

 Notice that the topic will be selected, and 'Starting 'Loaner Laptop'...' is displayed, but then gets stuck.

</td></tr><tr><td>

Document Management Services

 PRB1920126

</td><td>

'Export to PDF' for a scheduled report doesn't export in the proper alignment

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Viewer

 PRB1947203

</td><td>

After upgrading to Yokohama, there's an issue during the generation of a PDF file for a custom audit process using the PDFGenerationAPI library

</td><td>

The URL of an image or some function of the style of the HTML text used as the basis for the PDF file isn't converted or supported.

</td><td>

1.  Take the **Corporate FSQ Audit engagement** field \(engagement\_type\) with the status \(state\) as 'Follow Up' \(5\).
2.  Verify that the **Report** field \(kb\_article\) is populated.
3.  Verify that the **Audit Report State** field \(u\_audit\_report\_state\) is 'Final Report Delivery' \(final\_review\).
4.  Select the **Preview Audit Report** UI action that appears.

 An attachment should automatically be generated and be attached to the engagement in question, but nothing happens.

</td></tr><tr><td>

Dynamic Translation for Agent Chat

 PRB1942231

</td><td>

The 'agent\_translated\_msg' column is overwritten with an empty value when the agent is in English and the chat requester is non-English

</td><td>

An issue has been identified and introduced in Yokohama that impacts Dynamic Translation for Agent Chat \(DTAC\). When an agent is using English and the chat requester is using a non-English language, the 'agent\_translated\_msg' column in the database is overwritten with an empty value.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1898761

</td><td>

Email Client has a rendering issue in Next Experience due to '--now-accordion \_divider--color'

</td><td>

The issue doesn't happen in UI 16 or in Next Experience without Frame. The issue only happens in Next Experience with Frame.

</td><td>

1.  Provision an instance with sn\_csm\_gen\_ai installed.
2.  Set the email recommendation skill to active.
3.  Set the system property 'glide.ui.load\_ seismic\_email\_client' == true1.
4.  Navigate to an instance.
5.  Switch to Next Experience via personal settings.
6.  Navigate to any incident record.
7.  Select the 3 dots menu on the form header menu.
8.  Select **Email**.

 Expected behavior: The pop-up Email Client window should be rendered correctly.

 Actual behavior: The pop-up Email Client window is missing some CSS resources.

</td></tr><tr><td>

Email Notifications

 PRB1930940

 [KB2465116](https://hi.service-now.com/kb_view.do?sysparm_article=KB2465116)

</td><td>

Email parts are deleted when moving to a draft in workspace

</td><td>

Email issues are observed in the workspace. After copying and pasting the information, it's deleted.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Email Notifications

 PRB1942395

</td><td>

The cursor moves to the end of an input field when the CPU throttling is 4\* slower and 6\* slower

</td><td>

 

</td><td>

1.  Log in as an admin user.
2.  Navigate to CSM Workspace.
3.  Open a case record.
4.  Navigate to **Compose email**.
5.  Change CPU throttling in the 'Network' tab to 4\*slower/6\*slower.
6.  Type continuously.

 Expected behavior: Drafting an email shouldn't encounter unexpected cursor placement to the end.

 Actual behavior: The cursor jumps to the end while typing.

</td></tr><tr><td>

Email Notifications

 PRB1950667

 [KB2572580](https://hi.service-now.com/kb_view.do?sysparm_article=KB2572580)

</td><td>

The **Apply** button isn't found in the **Apply Email Templates** icon in CSM Workspace

</td><td>

When the compose email is used and the 'Apply Email Template' icon is selected in a case record, the **Apply** button isn't visible for email templates that contain a large body.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Email Notifications

 PRB1951516

</td><td>

When using email client, drag and drop functionality isn't including an attachment on sending

</td><td>

In the current UI16 email client, users can add attachments using the **paper-clip** icon or by dragging and dropping files into the email body. However, drag-and-drop doesn't work outside the email body because a background field was not properly defined, which causes this limitation.

</td><td>

1.  Log in to a Zurich instance.
2.  Navigate to the incident.list.
3.  Open Email Client.
4.  Drag and drop an attachment.

 When an email is sent, notice that the attachment isn't included. When users manually add the attachment, it's being added in to the email and is being sent.

</td></tr><tr><td>

Email Notifications

 PRB1952527

 [KB2743221](https://hi.service-now.com/kb_view.do?sysparm_article=KB2743221)

</td><td>

An email template isn't applied when users select **Apply template** in the mini/full composer

</td><td>

The template isn't applied.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Email Notifications

 PRB1964152

</td><td>

Email Client template behavior changed after upgrading to Zurich

</td><td>

After upgrading to Zurich, the behavior of Email Client template selection has changed. In Xanadu and Yokohama, the system always reverted to the default template when showing the 'Email' tab again. However, in Zurich, the system keeps the last used template \(template2\) instead of returning to the default.

</td><td>

1.  Log in to an instance.
2.  Open Service Operations Workspace.
3.  Open an incident record from the list.
4.  Select the **Detail** tab.
5.  Select the **More** menu on the right of 'Work notes', then select **Email** \(template1 is applied\).
6.  Confirm that template1 is currently applied.
7.  Select the **Email Template** icon on the right-side menu.
8.  Select **template2**, then select **Apply Template**.
9.  After template2 is applied, enter an email address in the **To** field and select **Send Email**.
10. Repeat Step 5.

 Expected behavior: Template1 is applied again \(returns to the initial status\).

 Actual behavior: Template2 remains applied \(the last used template is applied\).

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB1894626

 [KB2547515](https://hi.service-now.com/kb_view.do?sysparm_article=KB2547515)

</td><td>

Repetitive subtopics display in a subtopic widget

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Employee Taxonomy Framework

 PRB1930747

</td><td>

EVAM view config records are skipped in Yokohama

</td><td>

Four EVAM view config records are skipped when upgrading to Yokohama: sys\_ux\_composite\_data\_ template\_predicate\_ 28f0a2ffc30320102ec1a589a840ddea, sys\_ux\_composite\_data\_ template\_predicate\_ 44b0a2ffc30320102ec1a589a840dd8d, sys\_ux\_composite\_data\_ template\_predicate\_ 5de0a2ffc30320102ec1a589a840dde5, and sys\_ux\_composite\_data\_ template\_predicate\_ d5a062ffc30320102ec1a589a840ddd3. This happens because the view template is changed to xxxx v2 and 'child\_docs' is missing from custom fields.

</td><td>

Check the skipped records in an upgraded Yokohama base instance.

</td></tr><tr><td>

Encryption

 PRB1931988

 [KB2481838](https://hi.service-now.com/kb_view.do?sysparm_article=KB2481838)

</td><td>

A 'Data migration' job fails when there are no context keys and EFC's in the migration\_pending state

</td><td>

The job state changes to 'Error', with the following summary: 'Error creating job handler for type all\_data\_to\_kmf: \[The KMF cryptographic module to encryption context relationship table is empty. The 'Migrate Key Context to Module' job might not have been run or has failed.\].'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1955277

</td><td>

ConnectedBSGraphHandler needs additional guardrails, as this is leading to out of memory errors and node restarts

</td><td>

The issue is happening as part of the 'Event Management - Impact Calculator for BS\_3' job.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1864438

</td><td>

The flow action 'Submit Catalog Item Request' is not working when populating the HTML type variable

</td><td>

The HTML variable is populated as a data pill, when it should be populated as a variable data.

</td><td>

1.  Log in to an instance.
2.  Open the catalog item '3M Privacy Filter - Lenovo X1 Carbon'.
3.  Submit it with the HTML data.
4.  Check the flow execution 'Test Html Variable Flow'.

Notice that two new RITMs are created.


 Expected behavior: The variable 'HTML Variable' populates as Variable Data.

 Actual behavior: The variable 'HTML Variable' populates as a Data Pill.

</td></tr><tr><td>

Flow Engine

 PRB1879472

</td><td>

Sub flow context can't be opened after an upgrade to Yokohama

</td><td>

There's a deserialize error when viewing a flow context that has a static value assigned to the subflow output. The error stack can be located in the logs.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1896563

 [KB2250326](https://hi.service-now.com/kb_view.do?sysparm_article=KB2250326)

</td><td>

A stage\_state orphan record is created after a flow is cancelled

</td><td>

Numbers of stage\_state records with 'column\_renderer'=Legacy and empty **field**, **id**, **source** and **table** fields exist in the stage\_state table.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1923566

</td><td>

Yielding to the high priority flows feature causes several issues

</td><td>

Pausing should only occur before a flow element has started executing. If a pause occurs during the execution of a flow element, then it will cause an error for the cursor location and reporting.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1932618

</td><td>

Duplicate updates of a field in an update record action after updating the same record in a custom action using a script

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1941990

 [KB2605563](https://hi.service-now.com/kb_view.do?sysparm_article=KB2605563)

</td><td>

Trigger inputs aren't accessible after a do-until loop execution

</td><td>

This issue is caused by the changes to GlideFlowStages Updater.java \(older name GlideStage UpdateListener.java\). It's observed that, in this specific flow structure, the 'in.request\_item' flow input isn't passed to the 'Create Catalog Task' action. Querying the sys\_flow\_value table, there are 2 entries for 'in.request\_item' one for the flow input and another with the parent loop associated. As the same key 'in.request\_item' is now associated with parent loops, it can only be accessed in the loop body \(and for the specific iteration\), and all other references to it out side the loop aren't available.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1958181

 [KB2606177](https://hi.service-now.com/kb_view.do?sysparm_article=KB2606177)

</td><td>

Flows are intermittently not triggered after upgrading in a domain separation enabled instance

</td><td>

After upgrading a domain separated instance, some flows are no longer triggered. This is because some of the flow's records are in the domain that the flow was defined in, and other records in a different domain.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1984516

 [KB2741852](https://hi.service-now.com/kb_view.do?sysparm_article=KB2741852)

</td><td>

Flows with record triggers intermittently aren't triggering after a Zurich upgrade

</td><td>

The root cause of the issue lies in the record trigger cache preparation, which isn't thread safe. This may result in returning incomplete triggers that cause flows/playbooks not to trigger.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1821536

 [KB2144795](https://hi.service-now.com/kb_view.do?sysparm_article=KB2144795)

</td><td>

Inline script dot-walk doesn't work as expected

</td><td>

The issue happens when there are three or more dot-walks, the engine major version is two, and com.glide. hub.flow.inline\_ script.dotwalk. enabled is set to true.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1921408

 [KB2659810](https://hi.service-now.com/kb_view.do?sysparm_article=KB2659810)

</td><td>

The sys\_hub\_flow\_version record of a flow is not captured in the update set when updating the flow

</td><td>

The user must manually capture the sys\_hub\_flow\_version record in update set to avoid a preview error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1923234

</td><td>

Add the FDCollection complex object after all applications are installed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1931588

</td><td>

Opening a flow and closing it without editing updates the **Updated** and **Updated by** fields

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1938123

</td><td>

Flows using base instance actions related to the plugin 'Customer Service Spoke' fail after upgrading to Yokohama

</td><td>

The flows in question are base instance actions related to 'Customer Service Spoke': 'Add Work Note to Task' and 'Add Comment To Task'.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1952639

</td><td>

There's an error in the logs: 'com.glide.script.RhinoEcmaError: "FlowRecommendationsSkillCheck" is not defined'

</td><td>

There are 464 error logs in the last 15 minutes. This makes it difficult to check the debug logs. Nothing is being executed on the instance.

</td><td>

 

</td></tr><tr><td>

Form Templates

 PRB1968784

</td><td>

Users aren't able to update certain fields using templates in Service Operations Workspace \(SOW\)

</td><td>

When a field depends on another field, if a user is attempting to clear the dependent field value via a template while the parent field is populated, the system validates if the new value exists within the parent field's reference. The validation fails, preventing the field from being cleared.

</td><td>

1.  Navigate to an instance.
2.  Impersonate any users who have roles to control incident along with SOW and to use a template.
3.  Navigate to **SOW** &gt; **incident record** to apply a template.
4.  Fill out values in an assignment group and 'assigned to' columns.
5.  Select the **template** icon in the far right panel and choose it to update a field for instance 'Assigned to'.

 Expected behavior: A warning message shouldn't appear. And the **Assigned to** field should be updated.

 Actual behavior: A warning 'unable to update field Assigned to' message appears and users are unable to update the **Assigned to** field.

</td></tr><tr><td>

GlideAggregate API

 PRB1674129

</td><td>

Pagination for grouped lists in workspaces is not working correctly

</td><td>

This pagination issue hides the last rows of the list in Agent Workspace.

</td><td>

1.  Open an instance.
2.  Navigate to Incident.LIST.
3.  GroupBy assignment group.

Notice that there are 23 rows in the list.

4.  Navigate to Agent workspace.
5.  Open All incidents.
6.  GroupBy assignment group.

 Notice that the pagination shows 6 rows when there are actually more than 6 rows. Additionally, the last 3 rows that are seen in native UI are not present in Agent workspace.

</td></tr><tr><td>

Granular Delegation

 PRB1914000

</td><td>

Adhoc Granular Delegation intermittently doesn't work

</td><td>

This issue only happens when the delegation rule condition is added on the child table of the **task** field, which is added on the delegation rule.

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

History Set

 PRB1910202

</td><td>

Admin overrides are enabled in the ACL, but the admin user was denied access to History &gt; List view

</td><td>

After the Yokohama upgrade, or when upgrading between patches, users with the 'admin' role are no longer able to access History &gt; List view of all the tables/records. Prior to upgrading, the admin user was able to access the 'History List' menu as expected, and should have access to the 'History List' by default. This issue occurs even when the system property 'glide.security. admin.override. accessterm' is set to 'true'. Admin users can verify that they were blocked by the ACL with the 'Analyze Permissions' tool in the test instance. Only users who having the 'sn\_hr\_core.admin' role are able to see the History &gt; List menu.

</td><td>

1.  Open a Yokohama instance.
2.  Impersonate System Administrator user.
3.  Open an incident record.
4.  Select the 'form contact' menu.

 Expected behavior: The admin user accesses the History List menu by default.

 Actual behavior: History &gt; List is not visible to the impersonated admin user.

</td></tr><tr><td>

Horizon Alert Component

 PRB1912990

</td><td>

Now-alert doesn't render HTML that is not wrapped in an outer tag

</td><td>

 

</td><td>

1.  Create a now-alert component.
2.  Use the HTML and partial markup.

 Notice that the HTML is not rendered.

</td></tr><tr><td>

Horizon Component Library

 PRB1929229

 [KB2515183](https://hi.service-now.com/kb_view.do?sysparm_article=KB2515183)

</td><td>

A theme changes when opening an HR Case record page

</td><td>

The user's theme preference changes automatically when creating/opening an HR Case form from the workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery

 PRB1920738

 [KB2525534](https://hi.service-now.com/kb_view.do?sysparm_article=KB2525534)

</td><td>

HR Case description \(rich\_description\) doesn't copy over data, and the rich description is left empty

</td><td>

**Rich Description** appears as null in the 'List' view but displays correctly in the case record. The reverse works as expected— when updating the **rich\_description** field in the HR case form, the value will appear in the **rich\_description** field in the list view.

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

 [KB2503620](https://hi.service-now.com/kb_view.do?sysparm_article=KB2503620)

</td><td>

The **Suspend Reason** field isn't present on a form by default

</td><td>

This causes a discrepancy in populating the suspend reason in the work notes in an HR case.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery

 PRB1943958

 [KB2570781](https://hi.service-now.com/kb_view.do?sysparm_article=KB2570781)

</td><td>

There's a 'You do not have permission to read the created record' error when creating an HR Case

</td><td>

A race condition in the UI happens when a form is submitted before the GUID is created and an empty sys\_is is passed. The server-side code was not handling this. It happens intermittently.

</td><td>

1.  Open **Create New** via Agent Workspace.
2.  Select the **Benefits Management** HR service.
3.  Select **Create case**.

 Notice the error, but the case gets created in backend with an empty case number.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1950682

</td><td>

The character count in HTML box is half cut in Zurich

</td><td>

After the Zurich upgrade, the character count/words in the HTML editor are cut in half. In Yokohama, the character count/words are seen clearly.

</td><td>

1.  Navigate to kb\_knowledge.LIST.
2.  Open any record that is in the draft state.
3.  Check the **description** field HTML editor.

 Observe that the character count isn't clearly visible.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1953216

</td><td>

URL links added in HTML fields no longer change color when the **Toggle Theme** button on the TinyMCE editor is selected

</td><td>

The issue is observed in Zurich. It was tested in both light and dark themes, Next Experience, and coral.

</td><td>

1.  In a Zurich instance, navigate to kb\_knowledge.do.
2.  Copy and paste a URL link into the **Article body** HTML field.
3.  Select the **Toggle theme** button.

Observe no color changes.

4.  Repeat the same steps in a Yokohama instance.

 Observe the color of the URL link.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1897813

 [KB2287977](https://hi.service-now.com/kb_view.do?sysparm_article=KB2287977)

</td><td>

Shared key recovery doesn't happen when attempting to seed

</td><td>

Incorrect symmetric keys are observed in mostly incorrect post clone scenarios. This breaks the entire IDR and no data or metadata can be decrypted successfully.

</td><td>

Refer to the listed KB article for details.

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

Internationalization Features

 PRB1892286

 [KB2277705](https://hi.service-now.com/kb_view.do?sysparm_article=KB2277705)

</td><td>

A non-admin user can't change a dashboard name by specific steps when the system language is set to Japanese

</td><td>

The dashboard name should be updated correctly and reflected in both the primary record and its translated fields, as it is in the Washington and Xanadu versions. In the Yokohama version, the update to the dashboard name fails silently when the Japanese language is enabled and the sys\_translated record exists.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Internationalization Features

 PRB1911538

 [KB2266945](https://hi.service-now.com/kb_view.do?sysparm_article=KB2266945)

</td><td>

The 'Translated Text Synchronize' business rule has an infinite loop against v\_plugin

</td><td>

The 'Translated Text Synchronize' business rule goes in an infinite loop. The virtual table v\_plugin \(or any virtual table\) can refresh \(delete and insert of records\) the table upon query. Since v\_plugin has translated fields, glideRecord insert tries to insert into the sys\_translated\_text table, which runs the 'Translated Text Synchronize' business rule. This business rule tries to query the owner table i.e., v\_plugin again, which can trigger the refresh again and this goes on in an infinite loop. This is causing performance impact against many instances.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Internationalization Features

 PRB1912273

</td><td>

After a Yokohama upgrade, catalog admins can't create sys\_translated records

</td><td>

Since the upgrade to Yokohama, it's no longer possible for catalog\_admin users to create new records in table \[sys\_translated\], only update existing ones.

</td><td>

1.  Provision a Yokohama base instance with a language plugin installed.
2.  Create a testuser with the role catalog\_admin to access the catalog items and their variable sets and variables \(but not the sys\_translated table directly\).
3.  As sys\_admin, create two variables for any catalog item.
4.  Add a translation for one of the two variables.
5.  Switch to testuser.
6.  Open the catalog item.
7.  Change the preferred language to the one associated with the plugin \(make sure that the translation exists\).
8.  Change the English value to a translation for the variable that wasn't translated yet.
9.  As sys\_admin, check on the sys\_translated table directly.

Observe that the change is instantly reverted after trying to save it and isn't saved.

10. As testuster, adjust the existing translation of the variable question text for the translation that already exists.

 Observe that the adjustment is saved correctly and can be found in the sys\_translated table, with 'updated' and 'updated by' correctly updated to the testuser.

</td></tr><tr><td>

JVM at Scale

 PRB1938155

 [KB2532115](https://hi.service-now.com/kb_view.do?sysparm_article=KB2532115)

</td><td>

glide.memory.watcher is too aggressive after a Zurich upgrade

</td><td>

Change the memory watcher to use old gen usage percentage over the whole heap usage percentage kicks in remediator logic early.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1906571

</td><td>

Password2 system properties return an encrypted value after a node restart for on-prem instances

</td><td>

In on-premises environments, database \(DB\) properties aren't being correctly decrypted and remain encrypted in memory.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1913708

</td><td>

The KMF 'Customer Action' page no longer displays the latest certificate vulnerability due to a missing **experience\_properties** field

</td><td>

The KMF has a 'Customer Action' page with a custom script that uses the **experience\_properties** field. This field is not populated in Zurich, which causes the feature to break.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1944097

 [KB2654904](https://hi.service-now.com/kb_view.do?sysparm_article=KB2654904)

</td><td>

Users are unable to upload push certificates into the sys\_certificate table

</td><td>

An error is thrown.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Knowledge Management

 PRB1922665

</td><td>

The source numbers in Q&amp;A responses should be unique

</td><td>

In some situations, the numbers from the Now Assist synthesized answers can display '0' for all the citations, or sometimes use the same number for different references.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1973365

 [KB2733684](https://hi.service-now.com/kb_view.do?sysparm_article=KB2733684)

</td><td>

The 'Article Template Selector' page is not visible in UI16 in master

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

LDAP integration

 PRB1931311

</td><td>

Removing demo data removes the LDAP record producer

</td><td>

Removing demo data from an instance removes the LDAP Server record producer as well.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1353818

 [KB1700738](https://hi.service-now.com/kb_view.do?sysparm_article=KB1700738)

</td><td>

The **Dependent Choice** field can display different labels in a list row vs form when two dependent choices have the same value

</td><td>

On the list view of a record, a particular field displays one value incorrectly, but another correct value when looking at the records form or 'showXML'. This occurs when the dictionary record of the field uses choices and field dependencies, and when there are two choice records for the field that have the same 'value' \(not label\). When they have the same value but different labels, the label shown in the list view defaults to whatever dependent field value is first in alphabetical order with the same value.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1883306

</td><td>

In Service Operation Workspace \(SOW\), when updating the due date from the list view, the date/time is removed

</td><td>

When the user changes the system property 'glide.sys.date\_format' from base to 'dd-MM-yyyy', the field is cleared out when they attempt to change the date. This issue was observed in Yokohama.

</td><td>

1.  Access a Yokohama base instance.
2.  Navigate to **SOW**.
3.  Navigate to **List menu** &gt; **Requests** &gt; **Open Items**.
4.  In the list view for the Requested Item, add the column 'Due Date'.
5.  Change the date/time and apply it.

Notice that the date/time should update as expected.

6.  Open the system property 'glide.sys.date\_format'.
7.  Change the value to 'dd-MM-yyyy'.
8.  Save the record.
9.  Return back to the RITM with the updated due date.
10. Change the date/time to a future date and apply it.

 The value for the date/time is removed from the list view and on the form level.

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
3.  Create a module with a fixed filter condition using the URL from arguments. For example, time\_card\_ list.do? sysparm\_fixed\_query =user=javascript: gs.getUserID\(\).
4.  Impersonate any user.
5.  Open the time\_card list view via the module.
6.  Check the sum value displayed for the configured decimal field.
7.  Manually apply the same filter condition using the list filter.

 Observe that the total value calculation does not account for the fixed filter condition defined in the module. This behavior works correctly in the Xanadu instance.

</td></tr><tr><td>

List Administration

 PRB1918529

 [KB2669196](https://hi.service-now.com/kb_view.do?sysparm_article=KB2669196)

</td><td>

**Export** doesn't contain current view data

</td><td>

The **export** functionality doesn't apply the fixed filter configured in the list UI Builder's 'Fixed Filter' property. When exporting data, the exported file includes all records instead of reflecting the current view filter. This occurs when the fixed filter is configured in the 'Fixed Filter' property, as the **export** button ignores this configuration and only applies optional filters. The issue is reproducible in workspaces using the record-list-connected component \(NRLC\), where the fixed filter is not respected during export.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1932331

</td><td>

Word wrap doesn't work for NRLC list

</td><td>

Content in the **Short Description** field does not break into new lines when line breaks are added.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1932703

 [KB2543882](https://hi.service-now.com/kb_view.do?sysparm_article=KB2543882)

</td><td>

Display values aren't showing for reference fields within the 'List' component

</td><td>

When including a table on the 'List' component that contains reference fields, it's showing empty. Where as in platform, it shows a value.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1934797

</td><td>

There's an issue configuring the Platform Analytics Scheduled Exports Library list

</td><td>

The **Time** field isn't working as intended when added to the list view.

</td><td>

1.  On any Zurich instance, navigate to **PA** &gt; **Library** &gt; **Scheduled export**.
2.  Try to add **Time** field.

 Observe the error.

</td></tr><tr><td>

List Administration

 PRB1944139

</td><td>

Uptake allowExtended fields property on the lists side for the sn-field-select component

</td><td>

Tracking the changes for PRB1935534.

</td><td>

1.  Create a system property 'glide.ui.list.allow\_extended\_fields'.
2.  Set it to 'true'.
3.  Create a UI Builder page with a list component configured.
4.  Set the table property 'task'.
5.  Open the runtime page.
6.  Select the **Personalize columns** button in the header.

 Expected behavior: The fields from all tables extending from the task are displayed.

 Actual behavior: Only fields from the task table are displayed.

</td></tr><tr><td>

List Administration

 PRB1946446

 [KB2601161](https://hi.service-now.com/kb_view.do?sysparm_article=KB2601161)

</td><td>

Filtering issues on a **Date** field in workspace

</td><td>

After selecting a date, the filter options on the **Date** field in workspace are updated to an invalid date.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Filters

 PRB1967959

</td><td>

Unable to filter the **Tags** field in the presentation list from CSM/FSM Configurable workspace

</td><td>

When the user selects on the tag that has been added, a modal does not populate and the user is unable to select **View records with this tag**. Instead, the 'tags' column cannot be filtered.

</td><td>

1.  Access the CSM/FSM Configurable Workspace.

Notice that the variable with sys\_id '0c69dae8cc842210f87799583e1668b2' is loaded to the workspace \(order = '-10'\).

2.  Access the list of any table.
3.  Use the condition builder to add the **Tags** field as a condition.

Notice that the **Tags** field is not listed for selection.

4.  Add the 'tags' column to the list view.
5.  Select on the added tag.

 Expected behavior: A modal is populated and the user can select **View records with this tag** to find matching records.

 Actual behavior: Nothing happens, and it says the 'tags' column can't be filtered.

</td></tr><tr><td>

Memory: Heap Space

 PRB1636231

</td><td>

Memory is exhausted by the archiver job 'Consumer' due to syslog records stored in the memory, and syslog\_awa isn't configured as a rotated table

</td><td>

Memory is exhausted by the archiver job 'Consumer' reparenting records from the syslog table due to a problem observed when syslog\_awa, which is a child table of syslog, is created without table rotation. The archiver job reparents records for the archive rules it triggers for, and reparents a table that's not rotated. When syslog\_awa isn't configured as a rotated table, the reparenting process executes on it and its parent table syslog. Query to syslog shards are then observed, and memory is consumed as the records on these shards are stored into memory. Due to the size of it, it causes memory to become depleted. When the archiver job is running, the localhost logs have a large query to a syslog shard where the function reparentDocumentIDRecords is running.

</td><td>

 

</td></tr><tr><td>

MetricBase

 PRB1738054

</td><td>

The MetricBase Connectivity helper script for the MB Health Dashboard can construct an incorrect URL for a request for XML stats

</td><td>

In this script, it gets the hostname through a Glide property. If the host is null, it defaults to localhost:8080, but not all Glide instances run on 8080. This script runs every 10 minutes, so it can clutter the logs with errors.

</td><td>

 

</td></tr><tr><td>

MetricBase

 PRB1913485

</td><td>

Clotho system series should be inserted into the v\_clotho\_series table using a global scope rather than null scope

</td><td>

The 'Application' column for v\_clotho\_series metrics should have a global scope.

</td><td>

1.  Navigate to the sys\_metric table.
2.  Filter for records on tablename v\_clotho\_series.
3.  Update the table list view in the UI by selecting the **Gear** icon to show the 'Application' column.

 Notice that the 'Application' column for all v\_clotho\_series metrics should have a global scope.

</td></tr><tr><td>

MID Server

 PRB1504483

 [KB0964389](https://hi.service-now.com/kb_view.do?sysparm_article=KB0964389)

</td><td>

File-based Discovery on a Windows host might fail with 'AuthorizationManager check failed' due to hard coded network path \\\\127.0.0.1

</td><td>

When running a file-based Discovery on a Windows host, the following error may occur in the Discovery log: ​'Error: &amp; : AuthorizationManager check failed.' When running the PowerShell script, PowerShell believes that the script is coming from the internet since the path to the file is a network path that starts with an ip\_address, resulting in the 'AuthorizationManager check failed' error.

</td><td>

1.  Activate the 'File Based Discovery' plugin.
2.  Run it on a Windows host with a certain security policy.

 Observe the returned error.

</td></tr><tr><td>

MID Server

 PRB1863551

 [KB1972022](https://hi.service-now.com/kb_view.do?sysparm_article=KB1972022)

</td><td>

Mid Web Server/ACC API Key can't be viewed on instances provisioned in 2017 or earlier without creating a Module Access policy

</td><td>

Older instances can use a different KMF module to encrypt the **password2** field used to store the API key due to a change of packaging that occurred in 2017 on the base table, discovery\_credentials. On these instances, the **View API key** UI action on mid\_webserver\_api\_key\_credentials returns encrypted data unless the customer configures a Module Access policy manually.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1892912

 [KB2763600](https://hi.service-now.com/kb_view.do?sysparm_article=KB2763600)

</td><td>

MID tries to download signatures for synced file attachments when code signing is turned off

</td><td>

During file sync when code signing is off, the MID still attempts to fetch the attachment's signature along with the attachment. When the record signature doesn't exist, an error message beginning with 'Unable to find the signature with the sys id' appears in the Glide system logs.

</td><td>

1.  Ensure code signing isn't enabled on the Glide instance.
2.  Ensure that there is an attachment record that is downloaded by MID file sync but does not have a signature record in the sn\_kmf\_record\_signature table \(for example, a MIB\).
3.  Start the MID.

 Notice an error message in the Glide system logs.

</td></tr><tr><td>

MID Server

 PRB1898139

 [KB2398708](https://hi.service-now.com/kb_view.do?sysparm_article=KB2398708)

</td><td>

The MID Server doesn't start due to a parenthesis in the home folder's path, leaving the MID Server down after upgrades

</td><td>

If there's a parenthesis in the MID server path, the upgrade from the Yokohama version fails. This problem is specific to the Set-FolderPermissions.ps1 script.

</td><td>

1.  Create a MID server with a parenthesis in the path.
2.  Run start.bat.

 Notice that it fails with this line: '\\ was unexpected at this time.' The upgrade log also includes a 'was unexpected at this time' syntax error specific to the Set-FolderPermissions.ps1 path.

</td></tr><tr><td>

MID Server

 PRB1912171

 [KB2266697](https://hi.service-now.com/kb_view.do?sysparm_article=KB2266697)

</td><td>

Yokohama MID Server upgrades do not upgrade all jar files in lib

</td><td>

Yokohama MID Server upgrades don't upgrade all jar files in lib, causing NoClassDefFoundError for various classes, and MID Server to go down.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1916650

 [KB2421892](https://hi.service-now.com/kb_view.do?sysparm_article=KB2421892)

</td><td>

Patterns on agent commands are randomly failing with allow list errors

</td><td>

Collecting MSSQL DB details using ACC Discovery fails to fetch DB details with an error message. The exception occurred when executing a command on Agent. The error occurs when processing the adhoc check request: 'command failed due to allow list exclusion: check command denied by the agent allow list. Context: Asset allow list empty, using agent config file allow list.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

MID Server

 PRB1923497

</td><td>

A deadlock occurred due to two threads

</td><td>

The issue is caused by a conflict between two internal processes that manage and refresh OAuth credentials and MID Server connections. The platform periodically checks and refreshes expired OAuth tokens using a scheduled job. When this happens, the system reloads the credentials and resets all related connection data to ensure security and consistency. At the same time, if a Discovery probe or integration is trying to establish a new connection, it might attempt to access the same shared connection resources. This overlap can lead to both processes waiting for each other to finish, resulting in a temporary deadlock where neither process can proceed.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1969766

 [KB2664275](https://hi.service-now.com/kb_view.do?sysparm_article=KB2664275)

</td><td>

Missing MIDLogFileHandler MID Server properties cause MID servers to go into an infinite loop of restarting during start up

</td><td>

MID Servers repeatedly come up and then go back down for a few seconds before the MID Server comes back up again. This loop repeats continuously if certain MID Server Properties are missing from the ecc\_agent\_property table on the instance.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Platform

 PRB1908491

 [KB2243641](https://hi.service-now.com/kb_view.do?sysparm_article=KB2243641)

</td><td>

mobile-client-scripts don't take the user's date/time format into account when parsing data in V2Transform

</td><td>

In DateTimeFormatter.ts getUserDateTimeFormatter, it calls globalThis.userDateTimeFormat, but this is never set.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Mobile Platform

 PRB1931576

 [KB2466952](https://hi.service-now.com/kb_view.do?sysparm_article=KB2466952)

</td><td>

Offline-mode payload generation has excessive memory retention, causing performance degradation due to an SG offline document job

</td><td>

The Yokohama release introduced major changes to the way in which mobile offline payloads are generated, most notably embedded forms are now transformed into redirected forms. This removes the embedded forms from list screen documents and turns them into separate documents. With that change resulted in an increase in the number of documents that are processed during offline payload generation. This number can spike to as large as twice or three times as many documents processed compared to previous releases. As such, this results in an excessive number of GlideRecord instances being retained in memory. This has been seen to cause memory issues, node restarts, and severe performance degradation for users.

</td><td>

 

</td></tr><tr><td>

Mobile Studio

 PRB1974465

</td><td>

Mobile AI Builder \(id = sn\_maib\) plugin oob\_apps/now-mobile-ai-builder.properties should have mode = optional to ensure it is not an installed base instance

</td><td>

Mobile AI Builder \(id = sn\_maib\) is installed as it is marked as mode = core in oob\_apps/now-mobile-ai-builder.properties.

</td><td>

 

</td></tr><tr><td>

Multi-provider Single Sign-on \(SSO\)

 PRB1979071

 [KB2715489](https://hi.service-now.com/kb_view.do?sysparm_article=KB2715489)

</td><td>

SAML SP Keystore expiration

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1908169

 [KB2252998](https://hi.service-now.com/kb_view.do?sysparm_article=KB2252998)

</td><td>

An exact match for an experience with an invalid routeConfigId doesn't navigate

</td><td>

A new issue was found which results in Zing search results aren't opening properly within a workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now Assist Panel

 PRB1867538

</td><td>

Copy for synthesized responses \(auto start\) on Now Assist panel \(NAP\) doesn't work and copies 'undefined'

</td><td>

When using the Now Assist panel \(NAP\) and entering 'Summarize a record', the **copy** icon on the auto-started synthesized response doesn't copy the content, and instead, 'undefined' is copied. When 'undefined' is copied instead of the content and the synthesized response isn't auto-started, there is no **copy** icon and a 'Like/dislike' displays instead.

</td><td>

 

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

 PRB1965617

 [KB2768233](https://hi.service-now.com/kb_view.do?sysparm_article=KB2768233)

</td><td>

Legacy Now Assist Portal doesn't load upon upgrade

</td><td>

The Now Assist panel bubble opens when selected, but the panel doesn't fully load. The interface remains stuck in a loading state, and no content is displayed to the user.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OAuth

 PRB1963296

 [KB2624687](https://hi.service-now.com/kb_view.do?sysparm_article=KB2624687)

</td><td>

Users aren't displaying in OAuth application user

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OneExtend

 PRB1920515

 [KB2493973](https://hi.service-now.com/kb_view.do?sysparm_article=KB2493973)

</td><td>

LLM usage domain separation application properties aren't installed by default

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OneExtend

 PRB1925002

</td><td>

Agentic Workflow's trigger sys\_user is taking precedence over run as 'AI User'

</td><td>

When trigger conditions are met, the workflow should be executed with workflow's 'Run As' user for the new incident. However, the workflow is actually executed with the trigger's sys\_user and the execution is terminated with the error 'Access Denied'.

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1944861

 [KB2566151](https://hi.service-now.com/kb_view.do?sysparm_article=KB2566151)

</td><td>

Assists consumption for custom skills created in the Now Assist Skill kit

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

OneExtend

 PRB1963582

</td><td>

Opening Flow Designer triggers errors in logs

</td><td>

Opening Flow Designer triggers flow generation and flow summarization skills. However, since the skills aren't active in the customer instance, they're throwing errors in syslog table, such as 'Failed to get skill config for skillConfigId: 0472be2434131100b7b556ababf25d, capabilityId:'.

</td><td>

1.  Log in to a Zurich base instance.
2.  Open Flow Designer.
3.  Open syslogs.

 Observe the 'Failed to get skill\*' messages.

</td></tr><tr><td>

Password Reset

 PRB1932368

</td><td>

Massive flood of 'sys\_user\_grmember.delete' and 'sys\_user\_grmember.insert' events cause a huge delay on platform event processing

</td><td>

Mass import or deletion of a user group membership will generate large number of 'sys\_user\_grmember.delete' and 'sys\_user\_grmember.insert' events, causing a huge delay on platform event processing.

</td><td>

 

</td></tr><tr><td>

PDF Generation

 PRB1829301

</td><td>

System Trigger-PDFReportExportJob causes nodes to go out of memory

</td><td>

One user had slowness in the instance when the trigger on PDFReportExportJobs was executed. This trigger was consuming a lot of memory which forced support to turn off the execution. This was observed multiple times in the instance.

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

Performance Analytics Dashboards

 PRB1906120

</td><td>

User preferences \(com.snc.par.dashboards.ui.preferences\) are never cleared and causing out of memory errors and node restarts

</td><td>

'WARNING \*\*\* WARNING \*\*\* error processing rest data broker: Exception while executing request: Java heap space...'.

</td><td>

1.  Navigate to an instance.
2.  Open the dashboard.
3.  Select **Filter** &gt; **Assignment group**.
4.  Wait for a couple of seconds and navigate to **User Preferences**.

 Observe that the latest preference has large text and lot of applies to values in JSON.

</td></tr><tr><td>

Performance Analytics

 PRB1964068

</td><td>

Empty dashboards are repeatedly duplicating from the 'Migrate Homepages' scheduled script

</td><td>

'com.glideapp.home.deprecate\_homepages' has been set to false. After upgrading the instance from Xanadu to Zurich, a script called 'Migrate homepages' was introduced which created duplicated empty dashboards every time it runs.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1907336

</td><td>

The 'Created By' column values truncates after 10 characters in the Data Visualization library for Platform Analytics

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1934435

</td><td>

'Dashboard view count' doesn't update for Core UI dashboards

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1948336

</td><td>

Option to turn off the 'Welcome to Platform Analytics' pop-up / modal for migrated dashboards

</td><td>

When a responsive dashboard is migrated to PA dashboard, a pop-up / modal is shown to all users accessing the migrated dashboard: 'Welcome to the Platform Analytics experience'.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1952208

</td><td>

The dashboard list doesn't display and can't filter properly

</td><td>

The Dashboard Library on Platform Analytics \(Zurich\) generates an invalid query when any of the built-in filters are used and thus generate no queries due to the sys property glide.invalid\_ query.returns\_ no\_rows being set to true.

</td><td>

Navigate to **Platform Analytics** &gt; **Dashboards**.

 Notice that when 'Filter active' is true, no records are displayed even when there are numerous active dashboards. Using any filters removes all records from the list.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1843154

</td><td>

Not able to save a dashboard after editing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1890523

</td><td>

Committing update sets with dashboard changes doesn't clear the par\_dashboard\_cache

</td><td>

After the user commits the update set, the dashboard changes don't show up in the new instance because the par\_dashboard\_cache isn't cleared.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1905382

</td><td>

Dashboard tab names do not have unique keys for translations in a sys\_translated table

</td><td>

Core UI dashboard tab names contain the sysId of the pa\_tab record, and sometimes a BEL character and the string. Performance Analytics Experience dashboard tab names do not have this sysID prefix. In the Core UI dashboard, the sysID prefix enabled gives a different translation to the same string so multiple tabs can have 'New Tab 2,' but each can have different translation because real key is 'd6a290139 368b5107249 b9d86cba 1081New Tab 2'.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1909232

</td><td>

Platform Analytics dashboards can't be saved due to colliding components that have the same positions

</td><td>

Performance Analytics Reporting dashboard can't be saved if multiple components are colliding. An error occurs in the logs: 'DEBUG: DASHBOARD\_SERVICE: Dashboard with sys\_id is Dirty. Need to update DashboardsService DEBUG: DASHBOARD\_SERVICE: Dashboard updated true DashboardsService SEVERE \*\*\* ERROR \*\*\* DASHBOARD\_SERVICE: An error happened editing the layout. DashboardsResource SEVERE \*\*\* ERROR \*\*\* DASHBOARD\_API: Edit API - Widget Collision WidgetCollisionException - Colliding Widgets are.'

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1909523

 [KB2262722](https://hi.service-now.com/kb_view.do?sysparm_article=KB2262722)

</td><td>

Changes in the dashboard only appear in the session language where they were made

</td><td>

Users are experiencing inconsistent behavior in Platform Analytics dashboards depending on the selected user language. When viewed in English, the dashboard reflects the latest updates. When switched to Italian, an outdated version displays, even after clearing the cache using cache.do.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1964706

</td><td>

Errors found in a system log caused by daily automated list

</td><td>

After upgrading to Zurich, system log entries show below errors every day at 08:00 related to the automatic migration of List - Simple to Analytics List.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1926289

</td><td>

A reference table isn't migrated for the reference filter

</td><td>

After migration, the target for the filter is missing, and the reference table hasn't been migrated.

</td><td>

1.  Create a dashboard on CoreUI.
2.  Add the base instance interactive filter of type reference: Incident Assignment Group - Multiple.
3.  Verify the filters.

Notice that on the filter record, there's also the reference table available.

4.  Migrate the dashboard.

 Notice that after migration, the target for the filter is missing, and the reference table hasn't been migrated.

</td></tr><tr><td>

Playbook Experience Core

 PRB1929896

</td><td>

The playbook lane isn't translated to Italian

</td><td>

This is an issue with record generator. It can also be reproduced by going to 'Playbook Preview' and selecting the record generator for the record.

</td><td>

1.  Log in to any instance.
2.  Switch the language to Italian from the menu preference.
3.  Open **Workspaces** &gt; **Risk workspace**.
4.  Select the **List** icon.
5.  Select **Risk assessment planning** &gt; **Scheduled assessment**.
6.  Select **New**.

Observe that the playbook lane is still coming in the English language.


 Expected behavior: The playbook lane should be translated to Italian.

 Actual behavior: The playbook lane isn't translated to Italian.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1934746

 [KB2592048](https://hi.service-now.com/kb_view.do?sysparm_article=KB2592048)

</td><td>

Playbooks archived in Xanadu don't work in newer releases

</td><td>

New fields that get added to the deserialiser need to handle the keys not existing, which, as of now, is snapshot\_id and variant\_id.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Portfolio Management

 PRB1936553

 [KB2503548](https://hi.service-now.com/kb_view.do?sysparm_article=KB2503548)

</td><td>

The condition of the business rule 'Update Total Plan Cost In Proj Currency' evaluates to undefined when the com.snc.ppm\_multicurrency plugin isn't installed

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Predictive Intelligence

 PRB1617925

</td><td>

Async NLU request fails with a close connection error

</td><td>

Some calls within a batch of NLU async calls don't reach the predictor and a connection error is reported by Glide.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1954123

 [KB2594708](https://hi.service-now.com/kb_view.do?sysparm_article=KB2594708)

</td><td>

Mutual TLS \(mTLS\) is enabled on Zurich instances, causing access issues for inbound integrations

</td><td>

Due to the updates related to the Predictive Intelligence plugin, mutual TLS \(mTLS\) is enabled on user instances after a Zurich upgrade. This may result in instance access issues for inbound integrations.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Procurement

 PRB1675022

</td><td>

The user can't allocate the rights for an Unlimited Software license through a source request

</td><td>

 

</td><td>

1.  Activate the 'SAMP Master and Procurement' plugin.
2.  Create an entitlement with **Unlimited License** checked.
3.  Create a Service Catalog request.
4.  Add the same software model to cart.
5.  Checkout the cart.
6.  In SCTASK, select **Source Request**.

 In the 'Source Request' page, see that 'available rights' is 0 and the **Allocate** button is turned off.

</td></tr><tr><td>

Record Watcher

 PRB1894715

 [KB2345405](https://hi.service-now.com/kb_view.do?sysparm_article=KB2345405)

</td><td>

ChecklistItemResponder is too slow to effectively scale with normal usage of the platform, leading to the record watcher queue becoming backlogged

</td><td>

A performance issue has been identified related to checkLitsItem responders and ACL \(Access Control List\) checks while creating checkListItems in Visual Task Board's cards. These issues caused delays, especially when tasks had more than 50 checklist items. This is primarily because getItemsByChecklistId\(\) is invoked every time a checklist item is added or a card is moved between lanes. It loops through all items under a checklist and performs individual ACL evaluations \(read/delete access\). These checks result in: Repeated database lookups, redundant ACL checks for the same parent checklist, and slower response times, especially when checklist items exceed 50.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Reporting

 PRB1910065

</td><td>

Reports with multiple datasets throw an error: 'ERROR: Cannot generate the report. JSONObject\[''original\_xvalue''\] not found'

</td><td>

This issue was noticed when using the 'Time series' type and Gregorian Calendar per month.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1941447

 [KB2552237](https://hi.service-now.com/kb_view.do?sysparm_article=KB2552237)

</td><td>

The assignment FTE falls to an incorrect value due to lack of availability adjustment to 24 hours in the monthly view of RMWS

</td><td>

The issue is caused by not adjusting availability to 24 hours. It should adjust availability to 24 hours and redistribute hours evenly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

REST API Framework

 PRB1936861

</td><td>

'Requested URI does not represent any resource' is logged as an error instead of a warning

</td><td>

'Requested URI does not represent any resource' is logged as an error instead of a warning in the system Logs. Errors in the system logs represent issues that must be fixed; however, the 'Requested URI does not represent any resource' message should be displayed as a warning in the system logs because it is an error that has been handled and the user/platform can recover from.

</td><td>

 

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

 PRB1967269

</td><td>

Unable to update status of restricted caller access privileges

</td><td>

Multiple restricted caller access entries are changed from 'Allow' to 'Requested' after the Zurich upgrade. The user has re-allowed what was possible, but some applications are private and can't be manually updated.

</td><td>

 

</td></tr><tr><td>

Roles

 PRB1888313

</td><td>

Time-limited role access is assigned if a user has more than one request in the future

</td><td>

Access should work as expected for users with multiple time-limited user role records, with assigning and revoking working as expected.

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

Seismic Framework

 PRB1961091

</td><td>

The seismic placeholders 'nowPlaceholderHeight' and 'nowPlaceholderWidth' aren't rendering components

</td><td>

When both events in a starting position are visible on the screen, the templates render correctly. When the starting positions of both the events aren't visible on the screen but still they are in view port \(gets hidden due to the section header\), only one template renders and the other doesn't.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1825872

</td><td>

ES12 support in global script includes isn't working

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1972733

</td><td>

Field translations for security integrations are failing and return a null value

</td><td>

The field translations aren't working. On changing the field **evaluator.with EnforcedSecurity\(false\)**, field translations work as expected.

</td><td>

 

</td></tr><tr><td>

Service Catalog Portal Widgets

 PRB1939681

</td><td>

The 'SC Category' page doesn't display catalog items correctly if the portal doesn't have AI Search turned on

</td><td>

The portal is associated to many catalogs. The portal is only meant to show the categories/items that are part of the catalogs it is associated to. The URL to show the categories is constructed manually. The URL is using the sc\_category page. Since the portal doesn't contain the catalog that has the category, it behaves strangely.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1919964

 [KB2532880](https://hi.service-now.com/kb_view.do?sysparm_article=KB2532880)

</td><td>

The Record Producer **Submit** UI action should be grayed out after being selected once

</td><td>

On a catalog item in service portal, the **Submit** button re-enables after the first selection.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Catalog Variables

 PRB1855812

</td><td>

While changing the language from English to Norwegian, the user can't see all options under Lifecycle status 'End of life'

</td><td>

The getValue method on the GlideRecord that takes the column name behaves differently from the scriptable getValue on the gliderecord when the column is of type translated\_text. It works fine for the translated\_field types.

</td><td>

 

</td></tr><tr><td>

Service Graph Connectors

 PRB1972771

</td><td>

A JDBC connection test times out after a Zurich upgrade

</td><td>

The JDBC Connection test times out after a Zurich upgrade. The user modified the script in the client script section of the UI page in the instance, which resolved the issue. The user is also concerned about this page customization.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1710808

 [KB1576904](https://hi.service-now.com/kb_view.do?sysparm_article=KB1576904)

</td><td>

In a tag-based service, the sys\_property svc\_by\_tags.install\_status.blacklist isn't used to filter out CIs brought by traversal rules

</td><td>

SMServiceByTagsTopologyUtils, in the logic of walking by traversal rules, should apply the filter by the CI install\_status according to svc\_by\_tags.install\_status.blacklist. There are some issues with the tag-based population invoker. One thing to make sure is to force service recalculation even when the checksum hasn't changed, for cases when the service contains retired CIs.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Mapping

 PRB1912099

</td><td>

List CI list view doesn't allow copying the filter

</td><td>

List CI list view used to have a visible filter of CI sys\_ids. The list uses fixed\_query, which doesn't allow changing or copying of the list of CI sys\_ids.

</td><td>

 

</td></tr><tr><td>

Service Portal Core Widgets

 PRB1953795

</td><td>

The **Subscribe to update** button doesn't work for non- admin users after a Zurich upgrade

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1886667

</td><td>

Korean consonants and vowels are separately returned when the user types into a variable using a keyboard in a portal page

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1893333

</td><td>

After the first login with MFA authentication, the user is redirected to the Platform UI page instead of the Portal page

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

 PRB1893869

 [KB2313113](https://hi.service-now.com/kb_view.do?sysparm_article=KB2313113)

</td><td>

The EC Search widget doesn't handle the overflow of text when there are more than ten navigation tabs

</td><td>

When there are more than ten navigation tabs \(sys\_search\_filter\) created for the AI Search Application, the EC Search widget doesn't handle the overflow of text.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Service Portal

 PRB1914199

</td><td>

Portal throws unnecessary success messages when adding an attachment

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1956154

</td><td>

Extra unusable scroll bars appear on all user portals when accessed from a touchscreen-enabled laptop

</td><td>

This only happens when the .touch\_scroll class is added to the body element forcefully through developer tools.

</td><td>

1.  Use a Windows laptop with a surface touch screen enabled.
2.  Log in to any instance.
3.  Open any portal.

 Observe the redundant scroll bar.

</td></tr><tr><td>

Service Portal

 PRB1970979

 [KB2706155](https://hi.service-now.com/kb_view.do?sysparm_article=KB2706155)

</td><td>

Help text is misaligned in portal forms after upgrading to Zurich

</td><td>

After upgrading to Zurich, the help text in portal catalog items is not aligned correctly. It is shifted to the right of the label above it.

</td><td>

Refer to the listed KB article for details.

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

Notice that there's an entry for the discussion that the user isn't a participant in is visible in the record's Activity Stream.

10. Select **Open Discussion**.

 Expected behavior: Only users who are a participant should see the chat conversation

 Actual behavior: Users that aren't participants in a private chat are still able to see the chat conversation.

</td></tr><tr><td>

Software Asset Management

 PRB1913658

 [KB2290496](https://hi.service-now.com/kb_view.do?sysparm_article=KB2290496)

</td><td>

On an upgrade to Yokohama, new entitlements may get created from entitlement import errors

</td><td>

Users may observe the issue as duplicate entitlements found after an upgrade to Yokohama, or, after an upgrade to Yokohama, a number of entitlements were added that were created by 'system'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management Publisher Pack for Microsoft

 PRB1908686

 [KB2243700](https://hi.service-now.com/kb_view.do?sysparm_article=KB2243700)

</td><td>

Windows OS Server Pattern is failing at the extension section 'collect CAL info' with duplicate DUPLICATE\_RELATED\_PAYLOAD errors for samp\_user\_device\_license\_consumption

</td><td>

Windows OS Server Pattern did not update or populate the IP address for the host. In the payload, duplicate related items for the table 'msft\_ual\_user' in 'Collect CAL info' causes IRE issues.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Normalization

 PRB1862904

 [KB1968357](https://hi.service-now.com/kb_view.do?sysparm_article=KB1968357)

</td><td>

The 'SAM - Find Normalization Suggestions' job fails when there are Discovery models with an empty version

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reclamation

 PRB1937128

 [KB2514421](https://hi.service-now.com/kb_view.do?sysparm_article=KB2514421)

</td><td>

Return value issue with SAMPReclamationUtil &gt; getMetricAttributeFromLMR

</td><td>

The job 'SAM - Identifying New Reclamation Candidates' job fails with error: 'Cannot read property 'unlimitedLicense' from null.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Syntax Editor

 PRB1533082

</td><td>

The fonts defined on the system property 'glide.ui.html.editor .v4.font.collection' aren't displayed on the font list of the HTML editor on Agent Workspace

</td><td>

The list should show only the fonts defined in the value of system property 'glide.ui.html.editor .v4.font.collection', but it shows all the fonts mentioned on the system property 'Description'. On the native UI HTML editor, it's working as expected.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB1933518

 [KB2515608](https://hi.service-now.com/kb_view.do?sysparm_article=KB2515608)

</td><td>

Default queue provisioning fails during an upgrade

</td><td>

Default queue provisioning fails during the upgrade process with the message 'invalid table: sysevent\_queue\_provider\_param, state: failed'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Export Sets

 PRB1926120

</td><td>

There are node errors due to messages sent when Hermes/Kafka is unavailable or slow

</td><td>

When Hermes/Kafka clusters are down or running slowly, LES can't check their health before sending messages. As a result, the producer client keeps retrying, and without any pause or queue in place, these repeated attempts can eventually push the node into an error state.

</td><td>

 

</td></tr><tr><td>

System Update Sets

 PRB1909130

 [KB2250914](https://hi.service-now.com/kb_view.do?sysparm_article=KB2250914)

</td><td>

An installation from an update set overwrites customized records

</td><td>

To remediate the update set, the commit should be backed out \(including a rollback of the app install\) and a different way of installing the application should be used.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Table Administration and Data Management

 PRB1819751

</td><td>

There's a shadow table alter error when deleting a record after changing the string type field size from 50 to 100

</td><td>

Deleting a record from a form \(not a list\) results in the following error: 'Error Message\(conn=258502\) ALGORITHM=NOCOPY is not supported. Reason: Cannot change column type. Try ALGORITHM=COPY'.

</td><td>

 

</td></tr><tr><td>

Time Card Management

 PRB1901454

</td><td>

'Week starts on' doesn't work in Time Sheet Portal

</td><td>

The calender does not open for the **Week start** field on a form in the Time Sheet Portal.

</td><td>

1.  Provision an instance with the 'Time card management' plugin installed.
2.  Impersonate a system admin.
3.  Open time\_cad\_list.do.
4.  Create an entry.
5.  Select the **hamburger** icon and configure the form in form design.
6.  Add the field **Week start** in the time sheet portal view.
7.  Open the time sheet portal.

Observe the created record.

8.  Select the three dots option.
9.  Select **open** in the 'form' view.

 Notice in the form that the **Week start** field is not opening the date picker.

</td></tr><tr><td>

Transaction Management

 PRB1909722

</td><td>

Forked transactions close the async context immediately on an error

</td><td>

A few users have reported encountering a blank screen.

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

 PRB1157537

 [KB0685847](https://hi.service-now.com/kb_view.do?sysparm_article=KB0685847)

</td><td>

User presence works only if the browser cache is cleared

</td><td>

The user turned on the system property for user presence, but the user presence functionality doesn't work as expected. The user presence works when the user clears the browser cache.

</td><td>

1.  Using Chrome, log in to an instance as an admin user.
2.  Disable the presence.
3.  Using Firefox, log in to the instance as an ITIL user.
4.  In Chrome, as admin, enable the presence.

Notice that the **Presence** icon becomes available.

5.  Navigate to the Firefox session.

Notice that the **Presence** icon isn't reflected. If the user logs out and logs back in, the presence still doesn't show.

6.  Clear the browser cache in Firefox.

 Observe that the **Presence** icon works.

</td></tr><tr><td>

UI Field Administration

 PRB1774082

</td><td>

The glide.phone\_number\_e164.strict system property, which is false, doesn't seem to apply in the workspace form

</td><td>

The field type Phone Number \(E164\) displays an error in HR workspace but not in platform when the **Phone** field has incorrect digits and when the following system properties are set to false: glide.phone\_number\_e164.strict : false and glide.phone\_number\_e164. display\_territory\_selector: false.

</td><td>

1.  Open an HR record with a field type **Phone Number \(E164\)**.
2.  Put 11 digits instead of 10 in the platform view.
3.  Save the record.
4.  Open the same record in HR workspace.

 Observe that the same field now has an error in the HR workspace.

</td></tr><tr><td>

UI Field Administration

 PRB1881510

</td><td>

The category under 'change request values' on the standard change template isn't reflected in Service Operations Workspace

</td><td>

This issue is present in the base instance as well. The **category** field is visible, but the value set for the category isn't visible under 'change template values'.

</td><td>

1.  In the application navigator, navigate to **Change** &gt; **Standard Change** &gt; **My Proposals** &gt; **New**.
2.  Create a template with the change request values filled in.
3.  Request approval.
4.  In Service Operations Workspace, navigate to **List** &gt; **Tasks** &gt; **Assigned to you** \(remove the filter if required\).
5.  Open the standard change template.

 Observe that the category under 'change request values' isn't reflected.

</td></tr><tr><td>

UI Field Administration

 PRB1882475

</td><td>

Change request values on change templates aren't visible on Service Operations Workspace \(SOW\)

</td><td>

 

</td><td>

1.  Navigate to the std\_change\_producer table.
2.  Open an existing change template or create a new one.
3.  Ensure that the view is SOW.
4.  Ensure that the form layout has the **Change Request values** field present.
5.  Navigate to SOW.
6.  Open the standard change template.

 Observe that the change request values aren't visible.

</td></tr><tr><td>

UI Field Administration

 PRB1894570

</td><td>

HTML height is read-only with client script changes when a section is changed

</td><td>

 

</td><td>

1.  Navigate to incident.list.
2.  Create an HTML field on the dictionary.
3.  Save a record with random text.
4.  Navigate to client script and create a client script so that the field is read-only.
5.  Navigate to the record.

Observe that HTML read only height is small.

6.  Change section and note the HTML height.

 Notice that the HTML height is read-only.

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
8.  Select the **Add on MRA** pop-up.

 Observe that the asset didn't get added.

</td></tr><tr><td>

UI Field Administration

 PRB1945077

</td><td>

Click-to-call ignores the E.164 country code and defaults to +1

</td><td>

The 'Click-to-call' feature incorrectly dials US numbers instead of international numbers like the UK or India, regardless of the country code. Dialing from the contact card works correctly, but using the **Click-to-call** icon always defaults to US numbers.

</td><td>

1.  Navigate to the CSM Workspace.
2.  Open a case record.
3.  Select the **Information** icon of the **Contact** field.

The user account opens.

4.  Select the **phone** icon of the **Business phone** field.

 An outbound call is placed, and an interaction record is created.

</td></tr><tr><td>

UI Field Administration

 PRB1959307

</td><td>

Notes text area does not auto expand when a new interaction/incident is created in Workspace

</td><td>

The **Journal** field work notes do not resize automatically as they did in previous versions.

</td><td>

1.  Open SOW.
2.  Notice the **+** icon in the workspace.
3.  Select a new interaction/incident.
4.  Start typing until the content exceeds the visible area.

 Notice that the text area is not resizing and the user is unable to see the text written.

</td></tr><tr><td>

UI Form Administration

 PRB1894995

 [KB2438505](https://hi.service-now.com/kb_view.do?sysparm_article=KB2438505)

</td><td>

A requested item \(RITM\) created from an interaction in Service Operations Workspace \(SOW\) with an HTML variable automatically re-attaches images from the variable as the current user

</td><td>

When a user copy-paste text + images from Word, email, etc. to an RITM created from an interaction in a SOW HTML variable, reloading the RITM automatically re-attaches images to the record and gets displayed in the activity stream as a new attachment.

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

 Actual behavior: Images from the variable are reattached every time a user opens the RITM record. Newly re-attached images are show in the activity stream. These images can also be found in the sys\_attachment table with Table sys ID = RITM sys\_id.

</td></tr><tr><td>

UI Form Administration

 PRB1919041

</td><td>

An empty and read-only **Template value** input field causes an error when saving a record: 'Cannot read properties of null \(reading 'hasChildNodes'\)\)'

</td><td>

To reproduce, users need a record with an input field of type **Template value**, that is empty and also read-only. The error shows when saving the record.

</td><td>

1.  Log in as an admin.
2.  Navigate to **All** &gt; **incident.CONFIG**.
3.  Add a field called **Test Template**.
4.  Make it of the type 'Template Value' and save.
5.  Select the 'Advanced' view and the 'Dependent Field' tab.
6.  Select **Use dependent field** and a field, such as 'Channel'.
7.  Save the changes.
8.  Navigate to **All** &gt; **incident.CONFIG**.
9.  Create a UI Policy that will always make the new template value field read-only.
10. Pick an existing incident.
11. Make a change to the **Short description** field and save.

 Expected behavior: The record should save without error.

 Actual behavior: There's an error: 'Cannot read properties of null \(reading 'hasChildNodes'\)'.

</td></tr><tr><td>

UI Form Administration

 PRB1920717

</td><td>

Hyperlinks in annotations on forms are not opening in a new window

</td><td>

Hyperlinks open in the same tab instead of opening in a new tab.

</td><td>

1.  Open a base instance.
2.  Open an incident table.
3.  Open any incident.
4.  Select and hold \(or right-click\) and navigate to **Configure** &gt; **Form builder**.
5.  Create an annotation with the code.
6.  Open the incident in SOW.
7.  Under 'Details,' select the link.

 Expected behavior: It opens the link in a new tab.

 Actual behavior: It opens the link in the same tab.

</td></tr><tr><td>

UI Form Administration

 PRB1926448

</td><td>

After upgrading to Yokohama, the 'Before Query' business rule doesn't filter records in the workspace using an encoded query

</td><td>

Adding an encoded query on a 'Before Query' business rule to a filter record restricts the record on UI16, but fails to filter the record in the workspace. The record doesn't open in UI16, but opens successfully in the workspace. This issue was found in Yokohama and Zurich.

</td><td>

1.  Create a 'Before Query' business rule on the incident table.
2.  Create an incident with a short\_description.
3.  Set it to 'test'.
4.  Attempt to open the record in UI16 and workspace.

</td></tr><tr><td>

UI Form Administration

 PRB1938024

</td><td>

The 'View' context and tooltip is broken for a sn\_cmdb\_admin user

</td><td>

 

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1950676

 [KB2622641](https://hi.service-now.com/kb_view.do?sysparm_article=KB2622641)

</td><td>

The Approval Summarizer formatter isn't displayed after upgrading to Zurich

</td><td>

An issue has been identified after upgrading to Zurich with the Approval Summarizer formatter where the approval record doesn't display the summary of the item being approved.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Upgrade Center

 PRB1889948

</td><td>

The pop-up 'Edit box' UI is mispositioned when trying to edit a field by double-clicking \(or using the keyboard shortcut\) on it on a hierarchical list

</td><td>

This issue is found in Washington DC, Xanadu, and Yokohama.

</td><td>

1.  Open a base instance.
2.  Navigate to the **change\_request** table.
3.  Enable the hierarchical list for this table.
4.  Open any change record.
5.  Add at least 20 records to the first related list on that change record.
6.  Return to the change list.
7.  Expand the hierarchical list for the same change record from step 4.
8.  Try to edit the 15th or later cell on that expanded list.

 Notice that the **Edit box** UI is mispositioned.

</td></tr><tr><td>

Upgrade Center

 PRB1933942

</td><td>

Skipped error after upgrading

</td><td>

The user gets a skipped error after upgrading the instance from Xanadu to Yokohama. The reason is 'Skipping unavailable system property glide.db.df\_engine.enabled. Customers cannot configure this property.' It's included in the plugin 'com.snc.db.df\_engine'.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1819883

</td><td>

Null pointer exceptions occur when running 'UACountPersistorMessageEnqueueJob' and 'UsageAnalytics Count Persistor V2'

</td><td>

 

</td><td>

 

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

</td></tr><tr><td>

Usage Analytics

 PRB1931446

</td><td>

GCC/On-Prem/Self-Hosted users get exceptions and errors when using User Property Sync and Usage Tracking - Migration

</td><td>

For the first issue, the user property sync is turned on for on-prem/self-hosted instances and is trying to sync the user property like in TrackLongInactiveUserLogin. TrackLongInactiveUserLogin should actually check if instance is self-hosted and job should not run. There's an error. For the second issue, migration jobs aren't respecting on-prem constraints, and are attempting to sync from appsee via host URL. This URL is empty for on prem instances. Jobs like apps/funnel/cohort migration are running regardless of the instance type, leading to errors.

</td><td>

1.  Navigate to any on-prem instance.
2.  Try to run the 'User Property sync' job by navigating to **scheduled jobs**.

This should not run.

3.  Try to run the 'App Migration' job by navigating to **scheduled jobs**.

This should not run.

4.  Check if metric calls are going.

They should.

5.  Try to run the 'Config downloader' job.

This should not run.


</td></tr><tr><td>

Usage Analytics

 PRB1960875

</td><td>

The UXAAppMigrationJob job throws an error

</td><td>

The UXAAppMigrationJob job throws an error reading, 'Script: UXAAppMigration : inserting into sys\_analytics\_app table failed with error:ReferenceError: "APIKEY" is not defined.: no thrown error com.glide.ui.ServletErrorListener'.

</td><td>

 

</td></tr><tr><td>

User Administration

 PRB1930929

 [KB2468450](https://hi.service-now.com/kb_view.do?sysparm_article=KB2468450)

</td><td>

Updates on the sys\_user table are aborted by business rules, breaking functionality

</td><td>

The business rules are too restrictive. The following business rules contain 'Abort action' in the script if an invalid country code or language code is present: 'Prevent invalid country code' and 'Prevent invalid language code'. However, they don't have any conditions to trigger. If the country code or language code was already invalid due to historic imports/updates, then all transactions on the sys\_user records \(and extended tables like customer\_contact\) is aborted. This breaks functionality such as data import, updating the user profile, password reset application, and administering the sys\_user record via the UI. There is also insufficient logging presented to the user to indicate why the transaction failed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

User Authentication

 PRB1944133

</td><td>

There's a login page \(login.do\) presentation issue after a Zurich upgrade

</td><td>

There's a login page \(login.do\) presentation issue after a Zurich upgrade when changing the language to French.

</td><td>

 

</td></tr><tr><td>

UXF Components

 PRB1919730

 [KB2505771](https://hi.service-now.com/kb_view.do?sysparm_article=KB2505771)

</td><td>

UXF page components aren't loading properly post-upgrade due to a page fragment not updating during the upgrade

</td><td>

When users upgrade minor patches, if there are no changes to the metadata related to macroponents, page fragment caches won't be flushed. During the upgrade process, if any user accesses pages that have asset bundles, a problem occurs. During the upgrade, asset bundling is turned off, so the macroponent page fragment doesn't have assetsInBundle, but once the upgrade is completed, asset bundling will be turned on. However, the backend is serving the old page fragment without the asset bundle context, and the macroponent asset bundle is not loaded, so components in the page won't load.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UXF Macroponent

 PRB1909733

</td><td>

A thread is stuck because there are multiple threads accessing the same page with the same macroponent

</td><td>

There is a stuck semaphore transaction related to the function createCacheable PageFragment FromShell in CacheablePage FragmentFactory.java. This can lead to multiple threads stuck with no other option than to restart the node to provide relief. This may occur when there is no cache entry for the requested macroponent on the server, and multiple users are trying to access the same page with the same macroponent simultaneously.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1886861

</td><td>

There's an Automated Test Framework \(ATF\) error

</td><td>

A syntax error or access rule violation is detected by database: '\(\(conn == xxxxx\) Table 'xxxxx\_1.sys\_uxf\_snapshot' doesn't exist\)'.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1887044

 [KB2541971](https://hi.service-now.com/kb_view.do?sysparm_article=KB2541971)

</td><td>

The latest asset in sys\_ux\_lib\_asset isn't used when multiple asset records exist for the same asset version

</td><td>

This impacts Now Assist Panel loading and Dirty State Management in workspaces.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1892094

</td><td>

An ATF test UI action fails due to a timeout error

</td><td>

The intent library delivers context on generator registration for translators that don't exist on the page.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1924256

</td><td>

In Service Operations Workspace \(SOW\), the Change Overview page loads blank on the first normal change creation in a new session

</td><td>

After creating a new normal change and saving the record, the 'Overview' page is displayed as blank.

</td><td>

1.  Log in to an instance.
2.  Impersonate a user.
3.  Open SOW.
4.  Navigate to **Change** in List.
5.  Create a new normal change.
6.  Save the record.

 Notice that the 'Overview' page is displayed empty.

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

Don't attempt to log in.

6.  Open up the dev console.
7.  Execute the script.
8.  Execute the code.
9.  Select the chat bubble that appears after the code finishes executing.

 Expected behavior: The chat loads with content.

 Actual behavior: The chat load is blank and a security error appears in console.

</td></tr><tr><td>

UX Framework

 PRB1942276

 [KB2661969](https://hi.service-now.com/kb_view.do?sysparm_article=KB2661969)

</td><td>

When hovering over any workspace tabs \(parent or child/secondary\), the tooltip stays on screen and doesn't disappear

</td><td>

This is an intermittent issue, but when it occurs the user can't read part of the record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1947987

 [KB2649894](https://hi.service-now.com/kb_view.do?sysparm_article=KB2649894)

</td><td>

CSM/FSM Workspace list filter changes when opening and closing a record

</td><td>

When opening a record through the list in the CSM/FSM Configurable Workspace, the list's filter is modified after closing the record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1966606

</td><td>

Make UXF Caches Hard references to mitigate long build times from cache reclaims

</td><td>

This is a product update.

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

</td></tr><tr><td>

Virtual Agent

 PRB1890944

 [KB2338484](https://hi.service-now.com/kb_view.do?sysparm_article=KB2338484)

</td><td>

Large /api/now/v1/cs/ consumerAccount /unreadMessage calls from Proactive Trigger exhaust instance API resources

</td><td>

Some users on Portal have over 1 million of /api/now/v1/cs/ consumerAccount /unreadMessage call observers in the node logs. This causes an issue as it exhausts the API rate limit and prevents people from submitting forms on the portal and other issues. The API call is constantly sent out even when the session is timed out.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1893137

</td><td>

The Virtual Agent LLM survey displays a question twice

</td><td>

It's observed that there's LLM support for a survey, and the questions asked in the survey are populated twice.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1896593

</td><td>

Shouldn't be relying on the 'Greetings' topic for portal's Virtual Agent hand off

</td><td>

Users can have custom 'Greetings' topics. For those users, the hand off is broken.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1905962

</td><td>

Link, text and icon menu items aren't working in Virtual Agent branding in Dynamic Window

</td><td>

 

</td><td>

1.  Navigate to our branding config record and review the menu items listed at the bottom: /sys\_cs\_branding\_setup\_list.do?.

Observe that there's items for links, icons and text as menu items.

2.  Navigate to the portal after impersonating a valid user.
3.  Open Virtual Agent by selecting the icon at the bottom right.
4.  Select the **Support** button at the top of virtual agent window.

Observe that none of the items of links, icons and text appear.


 Expected behavior: All type of menu items should display.

 Actual behavior: Only the phone and email are working.

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

 PRB1927571

 [KB2586834](https://hi.service-now.com/kb_view.do?sysparm_article=KB2586834)

</td><td>

SessionManager and MacMessageBatchingSession is caching rhino objects contributing to higher heap usage

</td><td>

With a cache using around 150+ MB, storing rhino scope objects within a cache make it unexpectedly large depending on the GlideRecord queries that they run or JavaScript objects stored in the scope.

</td><td>

Refer to the listed KB article for details.

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

 PRB1933184

</td><td>

There's empty users in the sys\_gen\_ai\_usage\_log table

</td><td>

In SystemScriptObject, when executeSkill\(\), if setLicenseUsage\(\) is called before execute\(\), sys\_generative\_ai\_log would not be created yet and sys\_gen\_ai\_usage\_log's user field wouldn't be populated. There may be other instances where the user calls setLicenseUsage\(\), but there's no conversation.getContext\(\).getGenAILogId\(\).

</td><td>

1.  Start a NAP conversation.
2.  Execute a skill \(for example, order laptop\).
3.  Navigate to sys\_gen\_ai\_usage\_log table.

 Expected behavior: The **User** field should be populated.

 Actual behavior: The **User** field on the record that was just created is empty.

</td></tr><tr><td>

Virtual Agent

 PRB1935944

</td><td>

Post-chat survey results aren't stored in the 'Assessment instance' table

</td><td>

There should be a record of the feedback asmt\_assessment\_instance given in the post-chat survey. However, no feedback given by the user in the post-chat survey is stored.

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

Notice that the three execution plans \(sn\_aia\_execution\_plan\) and three conversation records are created. Only one conversation and execution plan executes successfully. The other conversations don't continue after the first task with the error 'No session ID found'.


 Expected behavior: Each triggered workflow should independently create or resolve its own valid session so that all conversations execute successfully, even under concurrent trigger conditions.

 Actual behavior: Only one conversation executes successfully. The other conversations either terminate immediately or don't continue after the first task with 'No session ID found' error.

</td></tr><tr><td>

Virtual Agent

 PRB1954972

</td><td>

Teams conversations time out due to a slow tracer query as the sys\_cs\_fdih\_invocation table becomes too large

</td><td>

The sys\_cs\_fdih\_invocation table can become large with 99.9999% records without a trace\_id \(trace\_id=Null\). A slow query can be triggered: 'QueryWarning \*\*\* WARNING \*\*\* Large Table: Table handling an extremely large result set: 2194898. Query that got us here is: TABLENAME = sys\_cs\_fdih\_invocation ENCODED\_QUERY = trace\_id=NULL'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1956231

</td><td>

vaVars or vaInputs variables set in a script include from an LLM input script area aren't unwrapped

</td><td>

The value should be unwrapped and stored as base type \(i.e. java.lang.String\) in task context. Instead, the value is sent as NativeJavaObject, which leads to an xstream serialization exception.

</td><td>

1.  Create a script include that takes vaVars as a variable.
2.  In that script include, set a variable on vaVars: vaVars.time = global.VAClickMetrics.getCurrentTime\(\); from an LLM input node script area \(like Dynamic Choice Picker\).
3.  Create an instance of this object.

 Expected behavior: The value is unwrapped and stored as base type \(i.e. java.lang.String\) in task context.

 Actual behavior: The value is sent as NativeJavaObject, which leads to an xstream serialization exception.

</td></tr><tr><td>

Virtual Agent

 PRB1976846

</td><td>

SessionManager/ qlueSessionToChannelSessionMap caches rhino objects, contributing to higher heap memory usage

</td><td>

Even if it's using a cache of 100, each item takes between 8-10 MB, causing the overall memory consumption to spike to over 800 MB.

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

 PRB1896591

</td><td>

Emoji panel loading is slow in Windows OS

</td><td>

Chrome and Edge browsers freeze for one minute after the user selects an **Emoji** icon in the Virtual Agent Web Client.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1920035

</td><td>

The 'VTT' icon isn't available in previous model of Now Assist Portal \(NAP\)

</td><td>

The issue occurs when the user switches from the new model to the previous model with VTT turned on.

</td><td>

1.  Provision an instance with any of the BU skills installed.
2.  Turn on NAP with VTT.
3.  Turn on the microphone from the browser preferences.
4.  Toggle 'on' accessibility settings.
5.  Select the **NAP icon**.
6.  Ensure the **VTT** icon is available in the new model.
7.  Change the model to old model \(Self service modal dialog\).
8.  Refresh the page.

 Expected behavior: The **VTT** icon should be available.

 Actual behavior: The **VTT** icon is not available in the old model of NAP when the user switches from the new model to old model with VTT enabled.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1942157

</td><td>

The KB article displays an 'undefined' avatar for a guest user

</td><td>

 

</td><td>

1.  Open the /csp portal in an instance without logging in.
2.  Initiate a chat with the Virtual Agent \(VA\).
3.  Fill in all the details like First Name, Last Name, and Email.
4.  Select **Product Issue**.
5.  When the VA prompts to describe the issue, enter 'dishwasher'.
6.  Select **Yes** for summary accurate.
7.  Select **Show me everything** &gt; **Get Help \(Template\)**.
8.  Enter 'dishwasher'.

 Observe that the VA comes back with the KB article, but the avatar of the KB is undefined.

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

 PRB1972561

 [KB2787591](https://hi.service-now.com/kb_view.do?sysparm_article=KB2787591)

</td><td>

Enhanced chat does not pick up custom tokens in portal

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr></tbody>
</table>## All Other Fixes

To view a list of all other PRBs fixed in Australia, refer to [All other Australia fixes](australia-all-other-fixes.md).

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


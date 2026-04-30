---
title: Xanadu Patch 1
description: The Xanadu Patch 1 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-09-10"
reading_time_minutes: 65
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 1

The Xanadu Patch 1 release contains important problem fixes.

-   **Xanadu Patch 1 was released on September 10, 2024.**
    -   Build date: 09-01-2024\_1853
    -   Build tag: glide-xanadu-07-02-2024\_\_patch1-08-24-2024

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X01.00.xlsx).

## Overview

Xanadu Patch 1 includes 255 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp1.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 1 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 1, refer to [KB1700380](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1700380).

## Changes in Xanadu Patch 1

-   **[Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE](https://www.servicenow.com/docs/access?context=connect-git-provider-oauth-2&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Set up an OAuth 2.0 application registry and credentials to connect to your Git provider from the ServiceNow IDE.

-   **[Configure OAuth 2.0 credentials to connect to a Git provider with the ServiceNow IDE](https://www.servicenow.com/docs/access?context=connect-git-provider-oauth-2&version=xanadu&pubname=xanadu-application-development&section=authenticate-git-repository-oauth&ft:locale=en-US)**

    Connect to a Git domain using OAuth 2.0 credentials to manage applications in source control from the ServiceNow IDE.

-   **[Configure an OAuth 2.0 application registry for the ServiceNow IDE](https://www.servicenow.com/docs/access?context=connect-git-provider-oauth-2&version=xanadu&pubname=xanadu-application-development&section=connect-git-oauth&ft:locale=en-US)**

    Configure how the client ID and secret are sent to the OAuth 2.0 provider associated with your Git provider.

-   **[ServiceNow SDK release notes](../now-platform-app-engine/servicenow-sdk-rn.md)**

    Create and convert commands include project-type and template parameters

-   **[Considerations for switching JavaScript modes](https://www.servicenow.com/docs/access?context=considerations-switching-javascript-mode&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)**

    Switching the JavaScript mode for an application or script might change the behavior of existing scripts.


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

 PRB1778235

 [KB1647662](https://hi.service-now.com/kb_view.do?sysparm_article=KB1647662)

</td><td>

There's an 'Invalid or unexpected token' error message on a browser console when accessing any page on a portal after upgrading to a Washington DC version

</td><td>

The issue can be seen on any portal, like 'SP' or 'ESC, as well as an empty testing page. There shouldn't be an error message on the browser console.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1779119

 [KB1650596](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650596)

</td><td>

After upgrading to Washington DC, the user sees a red banner ACL message when viewing incidents or case tasks

</td><td>

The user observes an error with the banner, 'Part of the query on live\_message has been ignored because of read security rules on live\_message.chat\_message', or 'Part of the query on live\_message has been ignored because of read security rules on live\_message.state'.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1779636

 [KB1651332](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651332)

</td><td>

Carousel and regular search results do not appear intermittently

</td><td>

The carousel gets stuck in a loading state when a search query is performed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1781787

 [KB1695712](https://hi.service-now.com/kb_view.do?sysparm_article=KB1695712)

</td><td>

Dependencies are not loading on Now Assist for Creator

</td><td>

The dependency processor repeatedly adds the same dependency for further processing, causing the list to grow continuously in an infinite loop.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Authentication

 PRB1782128

</td><td>

Error messages reading 'CSRF validation failed' are logged even though the validation property is false

</td><td>

After upgrading to Washington DC errors related to failed CSRF validation appear in the syslog table.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1717895

 [KB1629327](https://hi.service-now.com/kb_view.do?sysparm_article=KB1629327)

</td><td>

The 'OR' logical operator in a related list condition query behaves as the 'AND' operator

</td><td>

When reporting over a table, using a related list condition with the 'OR' logical operator, it seems to have the same effect as using 'AND'.

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

Access Control List \(ACL\) Rules

 PRB1787441

</td><td>

Empty ACL modal shows up even when the script contains a valid script

</td><td>

When trying to save an ACL with no roles, conditions or security attribute, but only a script the 'Empty ACL' modal shows up preventing from saving that valid ACL. This will happen when the script contains a \`//\` style comment on its first line.

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1781366

</td><td>

The 'AWA send external routing event' subflow is in a 'Draft' state

</td><td>

The subflow should be in a 'Published' state.

</td><td>

1.  Open **Flow designer** &gt; **Subflows**.
2.  Notice that 'AWA send external routing event' is in a 'Draft' state. It should be 'Published'.

</td></tr><tr><td>

Advanced Work Assignment

 PRB1789902

</td><td>

The scriptable API ExternalAWAService.pushEvent is not working when called from a scoped application to push custom events.

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Advanced Work Assignment

 PRB1793955

</td><td>

The user can't create a record in awa\_queue from application scope

</td><td>

On a base instance, only read application access is provided on awa\_queue. This prevents the record creation in awa\_queue from other than global scope.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1788201

</td><td>

Resolve copy-paste and debounce issues for chat input text area in Agent Chat and sidebar

</td><td>

There are two issues. The **Send** button enables after a 250s delay. On sending a message which is typed extremely fast, the message is cut off.

</td><td>

1.  Initiate an agent chat.
2.  Type some text in the text area.

</td></tr><tr><td>

Agent Chat

 PRB1797451

</td><td>

The textAreaRef doesn't get instantiated correctly on hook-insert, so the 'Enter' key and **Send** button in the input area don't work

</td><td>

The issue is intermittent.

</td><td>

1.  Create a chat as a requester.
2.  As an agent, before the entire chat renders, select the input text area.
3.  Type something quickly and hit the 'Enter' key.

 Expected behavior: Hitting the 'Enter' key or selecting the **Send** button sends the messages.

 Actual behavior: Hitting the 'Enter' key creates new lines and selecting the **Send** button does nothing.

</td></tr><tr><td>

Agile Development

 PRB1795981

</td><td>

True up Now assist for SPM

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1720477

</td><td>

Translated Field Helper generates unexpected AI Search documents for installed languages

</td><td>

Translated Field Helper generates unexpected AI Search documents by searching preferred\_language of sys\_choice table for installed languages of the sys\_user.

</td><td>

1.  Provision an instance without the i18n pack plugin.
2.  Navigate to sys\_choice.
3.  Create entries on the sys\_user table in the 'preferred\_language' column.
4.  Ingest a sc\_cat\_item record with language.

 Observe that two documents are generated for one glide record.

</td></tr><tr><td>

AI Search

 PRB1755160

</td><td>

The SysID of a record is displayed as a title in recently viewed items and exact match in Zing search

</td><td>

The SysID is displayed as the title after the **short\_description** field is removed and added back.

</td><td>

1.  On a base instance, make sure to have global search pointing to Zing.
2.  Export an XML.
3.  Remove the **short\_description** field and reimport it back.
4.  Search for the KB.
5.  Select the search input box and notice recently viewed items.

Notice that the SysId is displayed as the title.

6.  Try an exact match search.

Notice that the SysId is displayed as the title.

7.  Switch to Global search to use AI search.
8.  Search for the same KB and perform clicks.

 Notice that this KB doesn't show up in the 'Recently viewed' or 'Suggestions' section.

</td></tr><tr><td>

AI Search

 PRB1760249

</td><td>

User roles are not updated on changing user impersonation for data broker

</td><td>

 

</td><td>

1.  Log in as admin.
2.  Navigate to Search Preview UI.
3.  Select the Search Profile from the list and search for a keyword.

Verify that search results are visible for a selected search profile.

4.  'Search as' another user using the last tab in search preview.

 Notice that roles are not updated on changing user impersonation for a data broker.

</td></tr><tr><td>

AI Search

 PRB1774826

</td><td>

AIS update event queue writable property gets disabled with GenAI semantic tables indexing

</td><td>

Because GenAI table indexing is really slow, if ais\_index queued events happen to be more than 1M this can also happen during ais\_index.init.

</td><td>

1.  Create a 1M event in ais\_index queue.
2.  Kb\_knowledge DPR ingestion in progress with 10k+ documents.

 Expected: glide.ais.update\_event \_queue\_writable property is not disabled and eventually event processing lag gets caught up.

 Actual behavior: glide.ais.update\_event\_queue\_writable is disabled and unnecessary alerts and cases are created on user instances.

</td></tr><tr><td>

AI Search

 PRB1779590

</td><td>

UX issue in GR section

</td><td>

The user observes the message: 'No content to display. Please add components to carousel'.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1779622

</td><td>

'Attachment' is not translated in the suggested search popover

</td><td>

 

</td><td>

1.  Install a language.
2.  Add an attachment to a KB.
3.  Publish the KB.
4.  Search in service portal suggestion box to see attachment.

 Observe that 'Attachment' is not translated.

</td></tr><tr><td>

AI Search

 PRB1780839

</td><td>

Incorrect values are logged for triggered Genius Results \(GR\) in an async case

</td><td>

When the async mode is 'GR\_ONLY', 'GR Placeholders' are returned for every async GR that is executing when returning the initial search response. These placeholders end up in the searchAnalyticsPayload on that response, which is used to log the initial SEARCH\_EVENT. As part of the logging of that SEARCH\_EVENT signal, those placeholder GRs are then logged to the triggered GRs table. However, there's no guarantee any of them actually resulting in valid GRs, and if they do, there's no guarantee they were shown to the user.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1783414

</td><td>

Modify SAC cloning script so it can be called from admin console scope

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1785294

</td><td>

Suggestions for recently viewed results \(PERSONAL\_CLICK suggestions\) with external URLs don't navigate correctly in portal

</td><td>

 

</td><td>

1.  Open Service Portal on an AI Search-enabled instance.
2.  Search for 'Change Password'.
3.  Select the regular \(non-Genius\) search result for 'Change Password'.

Observe that it brings the user to a page outside of the portal \(for example, $pwd\_change\_error.do\).

4.  Run the scheduled job to process the queued click signals, to get 'Recently Viewed' suggestions.
5.  Return to the portal home or search page, and type 'Change' in the search box.
6.  Select the **Recently Viewed** suggestion that says 'Catalog Item' underneath it.

 Expected behavior: The user should be taken to the same URL used when selecting the regular search result.

 Actual behavior: The user is taken to the generic portal form page.

</td></tr><tr><td>

AI Search

 PRB1785913

</td><td>

Collapse Section, Filters, Hide filters are not translated in sn-search-facets

</td><td>

 

</td><td>

1.  On track/xnowassist, enable AIS.
2.  Turn on System Localization translation prefix.
3.  Search '\*\*\*'.
4.  Navigate to Incidents or any other tabs.

 Filters and Hide filters are not tagged with a translation prefix. Hover over the **+** expand sign, see **Collapse Section** doesn't have translation prefix.

</td></tr><tr><td>

AI Search

 PRB1786056

</td><td>

The carousel Genius Result position isn't added to the signal

</td><td>

When a term that triggers the carousel is searched for, and an action is taken on the carousel, the Genius Result position is not added to the signal.

</td><td>

1.  Navigate to the Next Experience homepage.
2.  Search for a term that triggers a carousel with more than one result.
3.  Provide feedback or do an action like a request for one of the items from the multiple items on the carousel.

 The carousel Genius Result position should be added to the signal, but isn't.

</td></tr><tr><td>

AI Search

 PRB1786362

</td><td>

AI Search on the Natural Language Understanding \(NLU\) portal doesn't work during platform and schema upgrade

</td><td>

 

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1787268

</td><td>

Query Locale on search preview UI is not working

</td><td>

Search results are not displayed in the correct language.

</td><td>

1.  Navigate to Search Preview UI \(New\).
2.  Select **Search Profile** from the list options.
3.  Change the Query Locale to Spanish under the 'Users' tab.
4.  Perform a search for a term \(for example, iPad\).

 Notice that the search result language is still in English.

</td></tr><tr><td>

AI Search

 PRB1788062

</td><td>

Search is down for some time when upgrading from Vancouver to Xanadu

</td><td>

An error is seen: 'AISearchService: Error is thrown from searchQueryService.search\(\) : : java.lang.NullPointerException: Cannot invoke 'com.glide.db.meta.Table.getTableIterator\(\)' because 'result' is null: com.glide.ais.configuration. Datasource.loadSemantic SearchMappings\(Datasource.java:351\) com.glide.ais. configuration.Datasource. loadFromDB\(Datasource.java:250\)'.

</td><td>

1.  On a Vancouver instance, provision an instance with Now Assist ITSM installed.
2.  Attach Now Assist actions and Now Assist Q&amp;A to the Service Portal search profile.
3.  Perform queries on the portal.
4.  Upgrade Glide to Xanadu.

 Notice that the regular search is down during the upgrade.

</td></tr><tr><td>

AI Search

 PRB1788078

</td><td>

sys\_search\_event doesn't include grConfig in gr\_results for Genius Result feedback and clicks

</td><td>

 

</td><td>

1.  Select **Feedback** or the **Genius Result** action.
2.  Wait for the search event to be flushed from the sys\_signal\_event\_queue.

 Observe that the entry in sys\_search\_event.gr\_results has an empty 'grConfig' value.

</td></tr><tr><td>

AI Search

 PRB1789527

</td><td>

Dense passage retrieval ingestion should continue to support property sn\_ais\_assist.dpr\_enabled to be enabled or disabled

</td><td>

In the August 2024 release, dense passage retrieval ingestion became a core feature of the Now Assist Creator. The property sn\_ais\_assist.dpr\_enabled moved to the glide family release and renamed glide.ais.dpr\_enabled, causing a regression for users with the June 2024 or earlier versions of Now Assist for AI Search. Instances with DPR ingestion disabled should remain disabled after an upgrade unless the user enables it manually.

</td><td>

1.  Install Now Assist for AI Search on Washington or older release.
2.  Disable DPR ingestion with hidden property 'sn\_ais\_assist.dpr\_enabled' to 'false'.
3.  Upgrade to Xanadu EA version.

 Notice that DPR ingestion is enabled.

</td></tr><tr><td>

AI Search

 PRB1789837

</td><td>

Attachments aren't indexed

</td><td>

The sys\_event for an attachment is present and processes without an issue, but nothing is in the index when queried. The attachment to AI Search backend isn't being sent.

</td><td>

1.  Enable attachment indexing from an indexed source.
2.  Attach an attachment to a knowledge record.

 Observe that a sysevent for the attachment/record is processed, but there is nothing in the index.

</td></tr><tr><td>

AI Search

 PRB1793717

</td><td>

The Natural Language Query \(NLQ\) 'Switch' table and 'Show' table doesn't emit feedback from sn-search-top-results

</td><td>

 

</td><td>

In Washington DC, select any non-feedback button on an NLQ result.

 Observe that no feedback is returned through the network calls tab, and that no genius result event was logged in the search's sys\_search\_event.

</td></tr><tr><td>

AI Search

 PRB1795072

</td><td>

Requesting dot-walked translated text fields in the Search API causes a null point error \(NPE\)

</td><td>

 

</td><td>

1.  Add a dot walked translated text field to an indexed source.
2.  Re-index the data source.
3.  Call the Scriptable Search API without dot-walked translated text field in the requested fields.

Observe that it's functional.

4.  Call the Scriptable Search API with dot-walked translated text field in the requested fields.

 Observe the empty response and the NPE in the logs.

</td></tr><tr><td>

Analytics Data API

 PRB1788888

</td><td>

Data broker calls fail after an upgrade

</td><td>

The Analytics Data API needs to sanitize the request coming from data brokers, and remove placeholder values.

</td><td>

1.  Create a UI Builder \(UIB\) page.
2.  Add a data visualization data broker \(table\).
3.  Fill out the properties of the broker so that the response is a correct data visualization response.
4.  Save the page.
5.  Navigate to the page definition.
6.  In the **Data** field, remove the useDataCache property value from the data broker.
7.  Navigate back to UIB and refresh the page.
8.  Open the data broker.

 Expected behavior: The response is the same as in step 3.

 Actual behavior: There's an error.

</td></tr><tr><td>

Antivirus Scanning

 PRB1734157

</td><td>

Update com.glide.snap.url to snap-v2 for the release of Glide

</td><td>

The virus scan isn't working when attaching a file to the **File Attachment** field.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1753470

</td><td>

App customizations still have sys\_claim after being reverted to base instance

</td><td>

App customizations still have sys\_claim after being reverted back to base instance, even after the app customizations are installed when using app customization v1 in instance 1 and instance 2.

</td><td>

1.  Install base app v2 in instance 1.
2.  Revert a customized file to base app v2.
3.  Publish app customization v2.
4.  Install app v2 and app customization v2 in instance 2.

 Expected behavior: Sys\_claim is removed.

 Actual behavior: Sys\_claim is not removed.

</td></tr><tr><td>

Application Install Engine

 PRB1782930

</td><td>

Plugin dependency incorrectly classified as app dependency for base instance plugins

</td><td>

The wrong type of plugin dependency is identified in the logs.

</td><td>

1.  Install a base instance plugin with a plugin dependency
2.  Check the logs

 Expected behavior: Observe 'Registering plugin dependency from %s to %s' .

 Actual behavior: The wrong type of plugin dependency is identified: 'Registering app dependency from %s to %s'.

</td></tr><tr><td>

Application Install Engine

 PRB1786797

</td><td>

Batch Install doesn't handle circular dependencies for non-app V2 apps

</td><td>

The BatchInstallDependencyMap.java class doesn't handle circular dependencies when the app being installed isn't a V2 app. The shouldEvaluateDependencies method incorrectly returns true when a circular dependency is encountered. When loading a non-V2 app and there's a dependency pair that's already seen, shouldEvaluateDependencies returns true because it checks the list of V2 plugins visited, which is empty because it's not a V2 app.

</td><td>

1.  Open a Washington DC instance.
2.  Attempt to batch install App Engine Studio.

 Observe that the progress bar doesn't go beyond 0%, and eventually a StackOverflow message appears.

</td></tr><tr><td>

Application Install Engine

 PRB1786807

</td><td>

Conditional applications weren't installed via new app management

</td><td>

 

</td><td>

1.  Provision a new Washington DC instance.
2.  Navigate to Store.
3.  Request the 'Healthcare and Life Sciences Service Management Core' application.
4.  Complete the installation of 'Healthcare and Life Sciences Service Management Core' V 8.0.0 on the instance via system applications.
5.  Navigate to system applications.
6.  Verify sn\_cwf\_wrkspc install's status.

 Expected behavior: sn\_cwf\_wrkspc should be installed or CSM/FSM Configurable Workspace is available in the instance.

 Actual behavior: sn\_cwf\_wrkspc isn't installed or CSM/FSM Configurable Workspace isn't accessible in the instance.

</td></tr><tr><td>

Application Manager

 PRB1780803

 [KB1649374](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649374)

</td><td>

Remote app table entries are populated with 'undefined' in the 'sys\_code' column

</td><td>

Installer copies sys\_code values from sys\_remote\_app table to sys\_store\_app table and used it for all app installations. However, it didn't account for records which have 'undefined' legacy values. As a result, the existing records with 'undefined' values causes failure to load conditional content in the plugin.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Appointment Booking

 PRB1789260

</td><td>

Personal events on a technician calendar are ignored when booking an appointment for an appointment booking user

</td><td>

There's also an error in the CSM/CSP portal when booking/rescheduling an appointment as an appointment booking user.

</td><td>

1.  Create a personal event for an agent.
2.  Ensure that only that agent is available in the group, so that DS check availability and events for that user alone.
3.  Log in as a user in the CSM portal.
4.  Book an appointment.

 Expected behavior: An appointment slot shouldn't be visible when an agent is on timeoff, or when booked for an appointment for any other available slot. The appointment should be booked with no error thrown.

 Actual behavior: Appointment booking/reschedule doesn't honor the time where a technician is on timeoff and displays slots. Also, users observe an error message on the screen.

</td></tr><tr><td>

Asset Management

 PRB1778297

 [KB1649341](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649341)

</td><td>

The Hardware Asset Management \(HAM\) 'Incident' view rule within Asset Management Workspace targets Agent Workspace

</td><td>

The **Workspace** field is set to 'Agent Workspace'. The HAM 'Incident' view rule shouldn't target Agent Workspace. The **Agent Workspace** field should remain empty.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Asset Management

 PRB1781337

 [KB1648741](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648741)

</td><td>

The 'Stock Runner' job is failing with an error

</td><td>

The 'Stock Runner' job is failing with an error: 'ProcessStockRules: ReferenceError: 'sn\_eam' is not defined.: no thrown error.'

</td><td>

 

</td></tr><tr><td>

Asset Management

 PRB1789460

</td><td>

On an instance that's in Swedish language, there's an issue when publishing a catalog item for a model

</td><td>

When publishing a Catalog Item for model on an instance in Swedish language, the name of the Catalog Item doesn't include manufacturer or model number.

</td><td>

 

</td></tr><tr><td>

Audit History

 PRB1772442

 [KB1651482](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651482)

</td><td>

When choosing logs to be exported in Log Export Service \(LES\), sys\_audit is not forwarded when the non-cancelable audit functionality is enabled

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Authentication

 PRB1788307

</td><td>

Dot-walking on list view is broken

</td><td>

Dot-walked fields \(such as Target Version, Parent Defect, etc.\) are blank. This issue only occurs after the 'Zero Trust - Policy Based Session Access' plugin is installed.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1764100

</td><td>

ATF steps that execute without explicitly setting 'Success' or 'Failed' statuses can leave pending suite results and stuck cloud run executions

</td><td>

Even after all tests are finished, the suite and progress tracker both stay in a 'Running' state. The cloud runner stays active even though there's nothing left to run, until it eventually times out much later. This can happen any time an ATF test step doesn't get set to a 'finalized' state \(for example Success/Failed/Error\), including because the step author simply forgot to do it, or because an error was thrown.

</td><td>

 

</td></tr><tr><td>

Automated Test Framework \(ATF\)

 PRB1769587

</td><td>

ATF scheduled client test runners can sometimes get unimpersonation errors

</td><td>

This can cause other tests in the same test runner to also have unimpersonation errors.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1779894

</td><td>

Launch restricted caller access plugin for the sidebar discussion summarization in the HR Service Delivery

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1785629

 [KB1698772](https://hi.service-now.com/kb_view.do?sysparm_article=KB1698772)

</td><td>

The 'Manage Human Resource' catalog page isn't loading

</td><td>

An error displays in the console: 'Uncaught SyntaxError: Unexpected token '\)...'

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1788858

</td><td>

Ship RCA for target: hr\_CoreUtils from source scope - Now assist for HR

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1790004

</td><td>

ProposedChangesExist and SNC.CMBDUtil can't be accessed outside of global scope

</td><td>

The change script includes need to be accessible to all scopes.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1790024

</td><td>

A review flow should only attach one post-implementation review task

</td><td>

Review flow's configuration needs to be corrected. Because the creation of the task doesn't mean the flow waits until the task is complete, it creates the task and then the flow ends. Based on the trigger condition of the flow, this means that when a user updates the record while it's in the review state, it keeps triggering the flow and creating new tasks.

</td><td>

1.  Make an unauthorized change model available in 'Create New'.
2.  Create an unauthorized change.

Notice that a single post-implementation review task is associated.

3.  Update the change request's short description.

 Observe that an additional task is associated because another flow was attached.

</td></tr><tr><td>

Cloud Encryption

 PRB1792686

</td><td>

DARE key is not visible in list view

</td><td>

When the cloud encryption plugin is activated the default 'dare\_key\_metadata' record gets created, but it isn't visible in the list view.

</td><td>

 

</td></tr><tr><td>

CMDB Integration Commons

 PRB1787552

</td><td>

Scheduled job executions are grouped in a single sn\_cmdb\_int\_util\_ cmdb\_integration\_execution record

</td><td>

Multiple scheduled job executions are condensed to compress into a single record in the sn\_cmdb\_int\_util \_cmdb\_integration\_execution table. Previously each scheduled job/data source would have a record in the sn\_cmdb\_int\_util\_ cmdb\_integration\_execution. Now there is one record based on the parent scheduled job in sn\_cmdb\_int \_util\_cmdb\_integration\_execution and it will have the scheduled import, concurrent import set, and import set of the latest scheduled job to run.

</td><td>

 

</td></tr><tr><td>

Column Level Encryption

 PRB1781726

 [KB1648610](https://hi.service-now.com/kb_view.do?sysparm_article=KB1648610)

</td><td>

Duplicate **Encryption Configuration** field records for tables in the CMDB hierarchy cause errors when the tables are queried

</td><td>

Duplicate **Encryption Configuration** field records for tables in the CMDB hierarchy can lead to new tables not having the correct number of clone descendant records, causing errors when the tables are queried.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1768078

 [KB1651520](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651520)

</td><td>

Class matches the keyword will be whiten after the focus gets moved to it and then moved off of it by using the 'tab' key

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1789033

</td><td>

Application Services chart issue in Xanadu

</td><td>

Selecting the Application Services chart does not navigate the user the Application Services page.

</td><td>

1.  Navigate to **Home** &gt; **CI Overview** &gt; **Cloud vs Non-cloud resources** &gt; **Application Services**.
2.  Select the chart \(for example, Hybrid service\).

 Expected behavior: Selecting the chart should take the user to the Application Services page.

 Actual behavior: The user is not navigated to the Application Services page.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1794682

</td><td>

The metrics in the CSDM Data Foundations Dashboard are showing a score of 0

</td><td>

Metrics such as the Hardware S. No. missing and technical service offering are showing a score of 0 as a result in the CDSM Data Foundations Dashboard.

</td><td>

Navigate to **All** &gt; **CSDM Data Foundations Dashboard** &gt; **Walk**.

 Observe that the indicator 'Technical Service Offering with Reference to Technical Service' result shows a score of 0 despite no technical service offerings existing with a missing reference to technical service.

</td></tr><tr><td>

Contract Management

 PRB1789324

 [KB1698586](https://hi.service-now.com/kb_view.do?sysparm_article=KB1698586)

</td><td>

Condition Check with global scope doesn't work when using any role

</td><td>

When a contract is created in a specific domain other than the global domain, checks present in the global domain aren't applied to the contract.

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB1788745

</td><td>

True-Up defect for DEF0533101

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1786888

</td><td>

Reparenting fails with 'Index 0 out of bounds for length 0' when column-store index pre-exists

</td><td>

Notice that in Xanadu, the value of the column-store index is missing. In Washington DC, the value is \{0\}, but in Xanadu, the value is empty.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1789910

</td><td>

'Order by' columns are not added to the 'Group by' clause when joined on a denormalized table with aggregation via 'RLQuery'

</td><td>

An SQLException error is thrown.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1765105

</td><td>

Filters for widgets in Data Usage Visualization Console to be updated

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1765554

</td><td>

Restoring of archived related records is not happening as expected

</td><td>

Some incident\_task and task\_sla records do not get properly restored.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1770139

</td><td>

StatsGatherer duplicates databases and table states records when re-running yearly and monthly stats for sys\_db\_pool\_size

</td><td>

 

</td><td>

1.  Ensure there are records from the previous month with the last collection start time in sys\_db\_pool\_size.
2.  Run the Physical Table Monthly Stats Gatherer.
3.  Check the records created in the sys\_db\_pool\_size tables.
4.  Run the Physical Table Monthly Stats Gatherer again.

 Observe that a second monthly record has been created for the databases and tables.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1773124

</td><td>

Destroy job is failing and unable to delete objects from S3 when safe mode is ON

</td><td>

Records are not deleted from S3 \(Access denied to delete from S3\).

</td><td>

1.  Create 20K records with attachments, audits and journals.
2.  Archive the Records to ar\_ table.
3.  Offload the records to S3.
4.  Create a 'Destroy' rule on the same archive rule and execute.

 Expected behavior: Records should be deleted from S3 and corresponding tables \(Cidx, archive\_log\).

 Actual behavior: Records are not getting deleted from S3 \(Access denied to delete from S3\).

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1782295

</td><td>

Job ID is not preserved for gateway stats records

</td><td>

When the gateway records are stored in the primary DB they get a new sys\_id assigned by default. Therefore, the gateway stats records have an invalid collection job sys\_id.

</td><td>

1.  Run the scripted Storage API in the background script: gs.print\(new sn\_disk\_usage. StorageDiskUsageService\(\). getStorageTierDiskUsages\(\)\);
2.  Navigate to sys\_storage\_disk\_usage and observe the gateway records.

 Expected behavior: The job ID column points to the correct record in sys\_sdu\_colleciton\_job table.

 Actual behavior: The job ID column displays 'null' and the value is an invalid sys\_id.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1786870

</td><td>

Remove the **Toggle DMTableCleaner** button

</td><td>

 

</td><td>

1.  Navigate to the list view of the sys\_dm\_job table.
2.  Navigate to the form view of the 'DMTableCleaner' job.

 Expected behavior: The **Toggle DMTableCleaner**button should be removed along with the script include it calls.

 Actual behavior: The **Toggle DMTableCleaner** button displays.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1790371

</td><td>

Storage API exception on archiving related pages when the sys\_sdu\_collection\_job table is not created on Gateway

</td><td>

The user observes an error message.

</td><td>

1.  Add Gateway in an instance.
2.  Make sure there are no disk usage tables created on Gateway yet.
3.  Navigate to any archive rule.

 Observe the error message: 'Syntax Error or Access Rule Violation detected by database \(\(conn=354245\) Table 'test\_gw\_gw.sys\_sdu\_collection\_job' doesn't exist\).'

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1790372

</td><td>

Inefficient scriptable API used to retrieve Tier 2 storage disk info

</td><td>

The scriptable API retrieves disk info for Primary, Gateway and Tier 2 storage info. However, there is no need to access Gateway and Primary if the only usage needed is Tier 2.

</td><td>

1.  Open the archive rule page.
2.  Observe that it takes a long time to attach the stack trace because it accesses Primary and Gateway storage info.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1773739

</td><td>

Cutover action to be triggered to flush caches on DB engine change

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1788006

</td><td>

DBLazy writer accumulates messages in an unlimited fashion in a thread stack

</td><td>

In DBLazyWriter.process, it accumulates messages dequeued for triggering listeners later. If the queue isn't empty, it continues the loop forever and keeps adding messages to the arraylist. This is unbounded and runs into an out of memory error.

</td><td>

1.  Write to DBLazyWriter at a high rate to keep the queue full.
2.  Ensure that the DBLazywrite process runs slower so the queue is always full.

 Observe the memory usage of the Glide instance.

</td></tr><tr><td>

Database Persistence

 PRB1762563

</td><td>

On a migrated instance, 'List' view queries on unicode values in the String UTF field do not work

</td><td>

'List' view shows empty results.

</td><td>

 

</td></tr><tr><td>

Data Filtration

 PRB1768454

</td><td>

In Vancouver's data filteration, the IP filter criteria provided in the subject condition isn't considered

</td><td>

The IP filter criteria provided is not considered. Thus, the results are not displayed / filtered properly.

</td><td>

1.  In any Vancouver instance or above.
2.  Create a data filteration with IP filter criteria provided in the subject condition.
3.  Check if the IP filteration criteria is being respected and the results are being filtered.

 Expected behavior: IP \[network\] filter criteria provided in the subject condition should be considered and the results should be filtered /displayed accordingly.

 Actual behavior: IP \[network\] filter criteria provided in subject condition is not considered.

</td></tr><tr><td>

Developer Sandboxes

 PRB1774289

</td><td>

Sandbox login doesn't support SSO \(Single sign-on\)

</td><td>

SSO is not supported for logging into a sandbox.

</td><td>

1.  Set up a sandbox instance with SSO login.
2.  Create a sandbox.
3.  Try to log in to the sandbox.

 Expected behavior: The user is able to log in using SSO.

 Actual behavior: SSO doesn't work properly.

</td></tr><tr><td>

Developer Sandboxes

 PRB1787278

</td><td>

SQLException errors prevent Sandbox from working properly

</td><td>

The user notices red banners with syntax errors when visiting different tables.

</td><td>

1.  Have an instance with several nodes with the sandbox feature fully enabled.
2.  Create a new sandbox and let it finish initializing.
3.  Once ready, try visiting different tables like incident, problem, cmdb\_ci\_computer, alm\_asset.

Notice that there are a lot of red banners with syntax errors.

4.  Turn on SQL Debug \(Detailed\)
5.  Try visiting different tables again and check what queries were made when.

 Notice that the tables visited are actually the original tables, so the node is not correctly sandboxed.

</td></tr><tr><td>

Developer Sandboxes

 PRB1790087

</td><td>

Condition built from sys\_dsb\_query\_condition is incorrect when including ORs

</td><td>

The QueryConditionUtil joins queries pulled from sys\_dsb\_query\_condition using ^OR. The outcome is not as expected.

</td><td>

1.  Create a new sys\_dsb\_query\_condition for any partial copy table of the form 'a AND \(b OR c\)'.
2.  Create another sys\_dsb\_query\_condition on the same partial copy table with any filter.
3.  Create a DSB.

 Notice the partially copied table does not as expected given the query conditions provided in step 1 and 2 \(should be OR'd together\).

</td></tr><tr><td>

DEX Application &amp; Device Health

 PRB1794322

</td><td>

Running process page shows all the data from the table on page refresh

</td><td>

It shows all the data present in the running process table \(dex\_running\_process\) so the device filter is getting applied.

</td><td>

1.  Log in as dex-admin/user.
2.  Navigate to any device.
3.  Navigate to running process from left nav.
4.  Refresh the browser.

 Expected behavior: It should show the list of running process on that device.

 Actual behavior: It shows all the data present in the running process table \(dex\_running\_process\) so the device filter is getting applied.

</td></tr><tr><td>

Discovery

 PRB1784351

</td><td>

The pattern plugin is not listing out by default as a part of CDW dependency

</td><td>

The pattern plugin should be listed by default.

</td><td>

1.  Open an instance with the sn\_cloud\_ops\_ws app installed.
2.  Check the dependencies list that was installed as a part of the CDW dependency.

 Expected behavior: The pattern plugin should be listed by default as a part of the CDW dependency.

 Actual behavior: The pattern plugin is not listing out by default as a part of CDW dependency.

</td></tr><tr><td>

Document Management

 PRB1790213

</td><td>

Add telemetry changes for PDF generation

</td><td>

Add the following telemetry changes for PDF generation: export functionality and Html2PDF conversion, including number of pages, the output PDF file size, and generation time.

</td><td>

 

</td></tr><tr><td>

Domain Separation

 PRB1786824

</td><td>

The Domain Migration tool is unable to update a status for a table migration that's in progress

</td><td>

There's no impact on the functionality of the migration tool due to this issue; the tool is running successfully. The only issue is reporting the results on the UI.

</td><td>

1.  Provision an instance with both Domain Support and the Domain Migration tool plugin installed with demo data.
2.  Navigate to the Domain Migration tool table.
3.  Create a migration job with the target domain as 'Cisco'.
4.  Save.
5.  Start the migration.

 Expected behavior: The migration status for each table should be available in the 'domain\_separated\_ tables\_migration\_status' table.

 Actual behavior: The 'domain\_separated\_ tables\_migration\_status' table has no data.

</td></tr><tr><td>

Dynamic Schema

 PRB1786796

</td><td>

The Dynamic Schema Writer role cannot insert a new dynamic attribute from dynamic\_attribute.list because the group is set to read only

</td><td>

 

</td><td>

1.  Navigate to sys\_user.list.
2.  Log into abel\_tuter and give the user the dynamic schema writer role.
3.  Save.
4.  Impersonate abel\_tuter.
5.  Navigate to dynamic\_attribute.list and create new.

 Notice that the group field is read only. After filling in the information, observe a 'Failed to insert' error because of the missing filed, which can't be entered because it is set to read only.

</td></tr><tr><td>

Edge Encryption

 PRB1773542

 [KB1651231](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651231)

</td><td>

A scheduled upgrade fails for a proxy running on Windows

</td><td>

It appears that the upgrade mostly completes. There's no errors in any of the logs, but the new Edge proxy service isn't started.

</td><td>

 

</td></tr><tr><td>

Edge Encryption

 PRB1776720

</td><td>

On BT1 Production, 'Show records' on the KPI details page is broken

</td><td>

The user observes, 'The provided BatchRESTRequest was not formatted correctly'.

</td><td>

1.  Log in to BT1 Production.
2.  Navigate to any KPI Details page of any KPI that has data collected and snapshots available.
3.  Enable the **Show record** toggle button.

 Observe that 'Unable to load records - Try refreshing the page.' is shown and the batch API call shows '400 Bad Request' with an error 'The provided BatchRESTRequest was not formatted correctly'.

</td></tr><tr><td>

Email Notifications

 PRB1783999

</td><td>

The 'Instance Email Reader' job stalls when only deleting \(not retrieving\) messages from POP3

</td><td>

When an instance is collecting mail, it retrieves messages at a significant rate under normal operations. When choosing only to delete messages \(and not retrieve them\), each mail reader job processes only 20 messages and then exits, forcing the instance to wait for the next scheduled email reader job 2 minutes later. This cycle repeats until the instance finds messages it chooses to retrieve, instead of just delete.

</td><td>

 

</td></tr><tr><td>

Encryption Support

 PRB1790352

</td><td>

'Failed to download Wrapped Key' error observed during Build Your Own Key \(BYOK\)

</td><td>

A module key should be generated for 'byok\_mod' module, but an error shows instead.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1760429

</td><td>

A race condition in tag based clustering engine when multi job/node event processing is enabled is causing multiple tag clusters to be created

</td><td>

This causes multiple tag cluster groups to be created for the same alerts.

</td><td>

1.  Set 'not for correlation' from the query job \(set the property as false\).
2.  Enable multi-job \(4\)/node event processing.
3.  Create a TBAC definition.
4.  Send several events at the same time with different message keys.

 Observe that multiple tag cluster groups containing the same alerts are created.

</td></tr><tr><td>

Event Management

 PRB1772901

</td><td>

There's an out of memory error in Alert Priority when an alert has high number of child alerts

</td><td>

In the warning logs, there's a message: 'Size of Alert group has reached limit of...'

</td><td>

1.  Create 3 million events that would generate 3 million alerts.
2.  Configure the alert correlation such that 30k alerts would have a single parent and around 100 parent alerts each have 30k child alerts.
3.  Ensure that the parent alerts are in 'em\_alert\_trigger\_queue'.
4.  Run the 'Event Management - Alert Priority Queue' job.

 Observe a message in the warning logs: 'Size of Alert group has reached limit of...'

</td></tr><tr><td>

Event Management

 PRB1784143

</td><td>

Events are created for unwanted SNMP traps in MID SNMP listener

</td><td>

SNMP traps can't be filtered from the MID server which prevents them from creating events in the instance.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1784562

</td><td>

Setting the main alert for Virtual Alert isn't consistent with the ACR script

</td><td>

The ACR script chooses the main alert to be the first one \(by initial\_remote\_time\) with the lowest number but ignores severity. Setting the main alert for Virtual Alert in VirtualAlertHandler.java is based on severity, but the alert number is ignored. This is causing redundant Virtual Alert groups to open.

</td><td>

1.  Enable the TBAC property for debugging: 'evt\_mgmt.sn\_em\_ tbac.log\_acr\_script\_debugging'
2.  Send multiple events at once with the severity set to 'Critical', that eventually should be grouped together in a tag cluster.

 Observe that in the 'Activity' notes of the created Virtual Alert that the main alert is consistent and doesn't change.

</td></tr><tr><td>

Event Management

 PRB1786275

 [KB1650970](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650970)

</td><td>

On the 'Link' view, getHopsBetweenCIs fails on CMDB grouping

</td><td>

Users are also receiving an error.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1789030

</td><td>

In Xanadu, the default order of an alert grouping is incorrect

</td><td>

In Xanadu default order of alert grouping is not correct

</td><td>

1.  Create a tag based definition - exact match on the same description.
2.  Send two events with same description and the same node and metric name.

 Observe that an automated group is created while the expectation is to have a tag cluster

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1769794

 [KB1650762](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650762)

</td><td>

The Flow Designer sets the true/false input parameter to 'false' in Xanadu

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1779812

</td><td>

Data pills on the flow canvas are incorrectly evaluated after republishing an existing flow

</td><td>

 

</td><td>

1.  Navigate to Flow Designer and open any base instance subflow \(for example, Create Child Task or Create Child Case\).
2.  Add a log at the end.
3.  Publish.

 Notice the data pills on the UI.

</td></tr><tr><td>

GlideRecord

 PRB1786468

 [KB1651472](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651472)

</td><td>

A transaction runs in an infinite loop when the user evaluates the condition that has 'Contains'

</td><td>

As a result of this issue, the entire session becomes unusable.

</td><td>

 

</td></tr><tr><td>

GRC: Vendor Risk Management Workspace

 PRB1772944

</td><td>

Non-interactive elements of the vendor portal page can be navigated using the **Tab** button

</td><td>

Tabbing for accessibility should only be for clickable objects on the page.

</td><td>

1.  Impersonate as any vendor contact.
2.  Navigate to a questionnaire in /svdp and switch to the notes or comments tab.

 Notice that the user can tab though the Activity stream for previous comments but can't navigate it with the arrow keys.

</td></tr><tr><td>

Health Log Analytics \(Family\)

 PRB1784922

</td><td>

There is an MID deadlock on HLA streaming threads while getting a fatal error

</td><td>

Deadlock exceptions in the MID wrapper log.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1786830

</td><td>

Updating the partition count in a topic causes the associated 'SUBSCRIPTIONS' to fail

</td><td>

 

</td><td>

1.  Create a topic and keep the number of partitions as 1.
2.  Create a consumer.
3.  Create a Kafka stream with the topic created in the previous step.

A subscription is created.

4.  Produce messages to the topic.
5.  Confirm the messages are consumed by the consumer.
6.  Update the number of partitions from 1 to 4.
7.  Save the topic record.

 This changed value appears well in the topic page. Navigate to the 'Topic Inspector' page, and there's the increased number of partitions. But, in sys\_kafka\_subscription, the number of partitions still displays 1. Also, the subscription that is created in step 3 gets deleted and a new one gets created every minute or so. The column 'Has Error' value changes from 'false' to 'true' and vice versa.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1787225

</td><td>

The **Synchronize Partition Count** button does not work on sys\_kafka\_topic

</td><td>

A null pointer exception error is thrown.

</td><td>

1.  Navigate to a sys\_kafka\_topic record.
2.  Select **Synchronize Partition Count**.

 Notice that nothing happens and observe a null pointer exception in the logs.

</td></tr><tr><td>

Horizon Component Library

 PRB1782771

</td><td>

Copy-paste isn't working as expected in the chat text area

</td><td>

This is reproducible both in Agent Chat and sidebar.

</td><td>

1.  Create a sidebar discussion or start a live agent conversation.
2.  Send a message: 'abcd'.
3.  Try to copy and paste an incident number into the chat text area.

 Expected behavior: Copied text should be pasted in the text area.

 Actual behavior: Pasted text is replaced by the last chat message.

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

 PRB1782130

</td><td>

Update the licensing definition to account for external embeddable sessions

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Incident Management

 PRB1781039

</td><td>

The **Create Request** action is available to users with the sn\_request\_role on the incident form in UI16

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Install Base Management

 PRB1786211

 [KB1650430](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650430)

</td><td>

The 'Account Page \(Case View\) Sold Product' related list must be updated with the default filter condition

</td><td>

The 'Sold Product' related list displays as empty when upgrading from Vancouver to Washington due to additional filters. The issue is observed only when the records are associated with a product offer that has a specification set.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Instance Clone \(Family\)

 PRB1774663

</td><td>

The user observes the alert 'General Data Exception detected by Database \(No value specified for parameter 1.\)' after submitting a clone on the 'clone\_instance' page

</td><td>

This isn't impacting clone progress, but it gives false alarm.

</td><td>

Submit a clone via the 'Legacy clone request' page.

 An error warning displays on the top of the page.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1766400

</td><td>

Users encounter a null offset

</td><td>

Currently, the **Clear Error and Retry** button tries to recover from a null offset issue, but it fails if the offset is missing or null in the topic.

</td><td>

1.  In a table with a boolean field with an 'empty' value \(neither true nor false\).
2.  Make changes to any field that is tracked via the CDC/IDR plugin.
3.  Observe the boolean field in the payload.

 Expected behavior: The value should be empty, not true or false.

 Actual behavior: The boolean value is represented as false.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1780168

</td><td>

Instance Data Replication \(IDR\) xmlstats do not show replication sets properly

</td><td>

 

</td><td>

1.  Create an active producer and consumer replication sets.
2.  Navigate to xmlstats.

 Observe that the replication sets are not shown.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1787215

</td><td>

For conserving disk space, remove the functionality of the seeding producer job waiting for ACK messages from the 'consumer' to 'publish next batches of data'

</td><td>

It adds an unnecessary point of failure of, if the ACK messages aren't received or sent without errors, then jobs hang. The only benefit of the ACK message exchange was controlling the disk size. Disk size unchecked growth can be controlled at the kafka level with data retention policy settings.

</td><td>

1.  In QA environment, stop the metadata consumer job on producer.
2.  Request new seeding on the consumer.
3.  Reset the metadata topic offset to end on the consumer.

 Notice that the 'Seeding produce' job hangs.

</td></tr><tr><td>

Integration Hub

 PRB1782980

</td><td>

The script-side StrictReject map for the glide\_hub\_flow\_ engine\_glideencrypter crypto module causes an 'access denied' error

</td><td>

Strict reject should be turned off for password2 or encryption support.

</td><td>

1.  Create an action with a script step.
2.  Decrypt the password field using GlideEncrypter in the script step.

 Expected behavior: The flow with the script step should be executed by creating a map for 'global.com\_glide\_hub \_flow\_engine\_glideencrypter'.

 Actual behavior: Access is denied to the cryptographic module with a 'global.com\_glide\_hub\_ flow\_engine\_glideencrypter' error on the flow execution.

</td></tr><tr><td>

Integration Hub Stream Connect

 PRB1781839

</td><td>

Only named Avro schemas are automatically imported from a schema registry

</td><td>

The automatic importing of schemas from a schema registry fails to consume an encoded message when the top-level type is unnamed. As a result, the schema record is not imported, and the script consumer receives an empty list of messages.

</td><td>

1.  Add a schema with an unnamed top-level type, such as an array, union or primitive, to the registry.
2.  Publish a valid message encoded with the schema to the topic.
3.  Use a script consumer to consume the message to trigger an attempt to automatically import the schema.

 Notice that the schema record will not be imported, and the script consumer prompts an empty array of messages.

</td></tr><tr><td>

Inter-Instance Data Comparison Tool

 PRB1772226

</td><td>

Remove the reseeding records limitation

</td><td>

This is a product update

</td><td>

 

</td></tr><tr><td>

Journey Designer

 PRB1752603

</td><td>

The user observes an 'Unable to get the task list' error while opening a catalog task

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1762398

</td><td>

The database view 'sn\_kmf\_crypto\_user\_policy' fails on Postgres instances

</td><td>

The database view 'sn\_kmf\_crypto\_user\_policy', which joins sys\_user\_has\_role and sys\_kmf\_crypto\_caller\_policy, fails on Postgres instances. Users can't correct the view manually, as the view is protected.

</td><td>

1.  On a Postgres instance, navigate to sn\_kmf\_crypto\_user\_policy.list.
2.  Verify that no records are returned.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1777352

 [KB1649414](https://hi.service-now.com/kb_view.do?sysparm_article=KB1649414)

</td><td>

Cloned data encrypted by a revoked key on source is not properly decrypted on target

</td><td>

A module key being imported 'inherits' the algorithm from the associated crypto specification rather than its original algorithm.

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1778142

</td><td>

Public keys are exchanged even when the key exchange is disabled

</td><td>

This issue occurs when new IA-Crypto Core workflows are enabled and Bagheera is enabled on an instance.

</td><td>

1.  Provision two instances with Bagheera.
2.  Generate asymmetric encryption and decryption keys on the source instance.
3.  Ensure the crypto configs of the keys are enrolled in the key exchange.
4.  Navigate to sys\_properties.
5.  Set the glide\_encryption.auto\_ key\_exchange.enabled to false.
6.  Schedule a clone from the source instance to the target instance.

 Expected: Module keys are not exchanged because the key exchange is disabled via property.

 Actual: Public module keys are exchanged even though the key exchange is disabled via property.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1786832

</td><td>

ad-hoc/ one-time/ recurring-clone KE does not work on Bagheera enabled instances

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1789932

 [KB1652642](https://hi.service-now.com/kb_view.do?sysparm_article=KB1652642)

</td><td>

A node is not reachable due to a race condition while decrypting system properties

</td><td>

A race condition occurs at the time of initializing the system properties cache. This can happen when the node is starting up and trying to decrypt system properties of type password/password2 that were encrypted with KMF.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1794684

</td><td>

The CID crypto core health workflow fails for Bagheera clones, showing the error message'IRK\_SOURCE\_INSTANCE\_ID\_MISMATCH'

</td><td>

 

</td><td>

Perform a clone using new IA workflows on DCTEST between two Bagheera auto config instances.

 Notice that the clone shows the error 'IRK\_SOURCE\_INSTANCE\_ID\_MISMATCH' because the rekey jobs did not complete their execution.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1794830

</td><td>

Instance node doesn't start after a cross-region move with AutoConfig Enabled = True

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1788025

</td><td>

Upgrading an instance from Washington DC to Xanadu with a true-up version breaks the knowledge base article creation flow

</td><td>

An error message appears when trying to create a knowledge article.

</td><td>

1.  As Admin, navigate to **Now Assist Admin Console** &gt; **Feature** &gt; **Customer**.
2.  Select **Knowledge** &gt; **Activate KB generation skill**.
3.  Choose any closed case.
4.  Create a knowledge article.

 Expected behavior: A Gen AI flow is triggered.

 Actual behavior: Observe an error message reading: 'There was a problem generating this article with Now Assist.'.

</td></tr><tr><td>

Knowledge Management

 PRB1795644

</td><td>

Update true up version of app-knowledge-gen-ai in Xanadu

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Local DB Login

 PRB1785794

</td><td>

The sys\_ux\_lib\_component file is missing required translation keys

</td><td>

Translations were present in Washington DC. However, in Xanadu, the sys\_ux\_lib\_component file is missing the required\_translation\_keys for now-login.

</td><td>

 

</td></tr><tr><td>

MetricBase

 PRB1728947

</td><td>

Registering a large number of triggers with Clotho causes some triggers to not get registered

</td><td>

Series references are appending to a request URL when syncing triggers between Glide and Clotho. If there are too many series registered at once \(for example 20k\), the header becomes too large. Series references should be included in the request body so things are scalable.

</td><td>

 

</td></tr><tr><td>

MetricBase

 PRB1785413

</td><td>

'Accumulate' calls result in double counting

</td><td>

A typo in GlideClothoClient results in a known series being resent alongside an unknown series. This causes the value doubling for them during 'Accumulate' calls.

</td><td>

 

</td></tr><tr><td>

MetricBase

 PRB1788301

</td><td>

Provision Plus workflow 'setupGateway: run instance script' times out after 600 seconds on Xanadu instances

</td><td>

A workflow fails in run-node-script, due to it timing out. The run-node-script.sh logs show that code is successfully executed and glide shuts down successfully, then it hangs for up to 10 minutes before it returns an error code for timeout.

</td><td>

 

</td></tr><tr><td>

Mobile Experience for Field Service Management

 PRB1789508

</td><td>

The user is unable to add events using the '+' icon

</td><td>

When the icon is selected, a new page should be opened, but it doesn't load.

</td><td>

1.  Provision an instance with WFO 4.0 installed and enabled.
2.  Log in to the Agent app.
3.  Select **My schedule**.
4.  Select the **+** icon.

 Observe that the page doesn't load.

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

 PRB1785277

</td><td>

The sys\_ux\_lib\_component file is missing required translation keys

</td><td>

Translations were present in the Washington payload. However, in Xanadu, the sys\_ux\_lib\_component file is missing the required\_translation\_keys for: sn-mfa-validate and sn-mfa-setup.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1787356

 [KB1652699](https://hi.service-now.com/kb_view.do?sysparm_article=KB1652699)

</td><td>

Some pages don't load when the property 'glide.ui.next\_experience. instance\_tools\_disabled' is set it to false and Next Experience is turned off

</td><td>

Pages such as 'Plugins', 'NLU Workbench models', 'Service Operations Workspace', and 'CSM-Configurable Workspace' don't load when the property 'glide.ui.next\_experience. instance\_tools\_disabled' is set it to false and Next Experience is turned off. Admin role users are unable to access these modules: Plugins \(now/app-manager/home\), NLU Workbench models, Service Operations Workspace, CSM-Configurable Workspace. ITIL role users are unable to access Service Operations Workspace and CSM-Configurable Workspace.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Now Assist for Code

 PRB1788701

</td><td>

Upgrades/side loads are impacted when old JS code is still being used by browser cache

</td><td>

The action prop is sent as null when old JS code is still being used by browser cache.

</td><td>

1.  On an instance with an older release of Code Assist, upgrade or side load the latest version.
2.  Trigger code assist on another page without hard reloading.

 Notice that the browser still has the JS files from the old version cached, so the action prop is not sent by the API call, and will cause an error since the new model requires this property to be either 'Suggest' or 'Edit'.

</td></tr><tr><td>

Now Assist for Code

 PRB1790715

</td><td>

Admins are unable to update to the new version of Now Assist for Code when the latest Creator app is already installed

</td><td>

In version 2.6.0, there is an issue with the NA4Code 26.0.4 version which is hiding the update from users that are already on the latest NA4Creator app.

</td><td>

 

</td></tr><tr><td>

Now Assist Panel

 PRB1787174

</td><td>

A record card with a KB gives a bad content error

</td><td>

 

</td><td>

1.  Create a topic with a record card and KB.
2.  Select **NAP**.
3.  Select the topic create in step 1.

 Expected behavior: The KB card should be displayed with the button to open KB.

 Actual behavior: Bad content card error.

</td></tr><tr><td>

On-Call Scheduling

 PRB1787870

</td><td>

Issue with Create/Edit Schedule Wizard localization for week names

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Order Management

 PRB1788283

</td><td>

The time duration of family upgrades have increased from 1 hour and 23 minutes to 2 hour and 43 minutes

</td><td>

 

</td><td>

1.  Ensure the Order Management plugins are installed in the instance with the Washington build.
2.  Upgrade to the Xanadu RC1 build.

 Observe the time duration of the upgrade from the batch\_alter operation, and compare it to the time duration of the previous family upgrade.

</td></tr><tr><td>

Performance Analytics API

 PRB1781079

</td><td>

Server error on certain indicators with groupby and 'separate/aggregate' option

</td><td>

On certain indicators, when enabling filter and 'filter as separate groups' \(splitView = true\), the server returns n error 500.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1740986

</td><td>

Core UI dashboards are not migrated automatically when com.glide.par.v \_table\_join.enabled is false

</td><td>

Setting com.glide.par.v\_table\_join.enabled to false disables combined dashboards, resulting in core UI dashboard not being migrated automatically on the first request.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1771293

</td><td>

Internal error upon creating a filter condition with Date and Duration

</td><td>

The user observes a 'RelativeDatesQueryGenerator' error.

</td><td>

1.  Add a condition to the number of resolved incidents indicator source.
2.  Set it to: 'Resolved on Today' or 'Business duration Less than 1 day'.

 Observe the error: 'RelativeDatesQueryGenerator: NAM Stats Error: Invalid ID for ZoneOffset, invalid format'.

</td></tr><tr><td>

Performance Analytics

 PRB1778421

</td><td>

Null pointer exception while retrieving scores for formula indicator with group-by

</td><td>

A null pointer exception is observed in the logs.

</td><td>

1.  Provision an instance with the com.snc.pa.premium and com.snc.pa.mlb plugins installed.
2.  Enable MLB for all base instance indicators related to the incident table.
3.  Do not enable MLB for the formula indicator: '% of incidents resolved on same day opened'.
4.  Make sure that the involving indicators are enabled with MLB.
5.  Create a new dashboard.
6.  Add the above formula indicator to the pie or donut visualization with group by as 'Assignment group'.
7.  Make sure that the cache is enabled.
8.  Retrieve scores for the indicator and observe logs.

 A null pointer exception is observed.

</td></tr><tr><td>

Performance Analytics

 PRB1780038

</td><td>

The cascading filter m2m migration datasource reference field isn't set as expected

</td><td>

The issue is that the migrated cascading filter works in runtime, but it doesn't work in configuration time.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1781018

</td><td>

A legacy widget doesn't publish filters

</td><td>

When the user has a custom filter in compatibility mode and tries to interact with it, the filter doesn't get applied.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1781006

</td><td>

Dashboards, Data Visualisations, and Scheduled Exports are set to have been created by the user who ran 'Platform Analytics Migration' instead of the original

</td><td>

The 'created by' user was the user before migration who actually created the dashboards and scheduled exports. But post-migration, the 'created by' is changed to the person who initiated the migration.

</td><td>

1.  Navigate to a Washington DC instance.
2.  Impersonate a non-admin user with roles like itil + report\_scheduler
3.  Create a report.
4.  Schedule the report and add it to the new dashboard.

Notice that entries in pa\_dashboards, sys\_report, sysauto\_report should are created and updated by the user from step 2.

5.  End the impersonation.
6.  Impersonate a user with an admin role.
7.  Trigger 'Platform Analytics Migration', which should be completed without issues.
8.  Validate the new records created post migration in par\_dashboard, par\_visualization, par\_export, par\_export\_visualization.

 Expected behavior: Dashboards, Data Visualizations, and Scheduled Exports shouldn't have 'created by' set by the user who ran 'Platform Analytics Migration'. Instead, the original creator names should persist.

 Actual behavior: Dashboards, Data Visualizations, and Scheduled Exports are set by the user who ran 'Platform Analytics Migration' instead of keeping the original user.

</td></tr><tr><td>

Platform Analytics Filters

 PRB1777094

</td><td>

Washington DC-migrated cascading filters need to be adjusted

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Filters

 PRB1782599

</td><td>

Default selection for 'View by' is wrong for the highest number of software installations widget in discovered inventory

</td><td>

On page load for each filter, the event handler is getting called with empty values in the array.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1793305

</td><td>

If individual dashboards have been rolled back, migration rollback fails an activation step

</td><td>

 

</td><td>

1.  On a Washington DC instance, migrate all dashboards.
2.  Rollback a couple dashboards from the par\_dashboard table.
3.  Set the rollback property to true.
4.  Perform a bulk rollback.

 Expected behavior: Bulk rollback actives everything properly.

 Actual behavior: The rollback fails.

</td></tr><tr><td>

Playbook Experience Core

 PRB1789670

</td><td>

Duplicating a process does not assign the correct variantId to activities

</td><td>

The new duplicate process should be a replica of the original process, but it is not.

</td><td>

1.  Create a process with activities.
2.  Add some variant and variant activities.
3.  Duplicate process.

 Expected behavior: The new duplicate process should have same replica of original process with all base and variant activities.

 Actual behavior: The variant activities are not associated with variant.

</td></tr><tr><td>

Predictive Intelligence Clustering Solution

 PRB1769445

</td><td>

An error is thrown in the syslog by the job 'Application Suggestion - ITOM discovery'

</td><td>

An 'Illegal parameter: null:' error is thrown in the syslog by the job 'Application Suggestion - ITOM discovery'. There's no impacts to processing. It's a redundant error message thrown 4 times every time the job runs.

</td><td>

1.  Run the scheduled job 'Application Suggestion - ITOM discovery'.
2.  Observe errors in the system log.

</td></tr><tr><td>

Process Mining

 PRB1785033

</td><td>

Sample Mining fails in a support instance

</td><td>

The user observes an error while doing sample mining in a ServiceNow support instance.

</td><td>

1.  Log in to a support instance.
2.  Navigate to Process Mining.
3.  Create a project.
4.  Try sample mining on the same project.

 Observe the following error: 'Entitlement issue: Not able to perform full mining or sample mining on 'sn\_customerservice\_case'. Please contact your ServiceNow representative for further details'.

</td></tr><tr><td>

Process Mining

 PRB1793521

</td><td>

External Data Full mine throws License error even if license is available

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Record Watcher

 PRB1788115

</td><td>

In rare cases, ResponderRegistryCleanerThread can remove all persisted responders from the memory when the database returns null on an exception

</td><td>

RW Cleaner Thread wakes up every 10 seconds and does some cleanup tasks. As part of this, it tries to remove all orphaned persisted responders from memory. It gets all persisted responders from the database and compares them with what's in the memory. It removes those which are in memory but not in DB. In this case, because of an exception from the DB query, the database layer has returned null. The cleaner code understood this as there are no responders in database and removed all of them from memory, which has caused RW to not call the responder on a matching condition.

</td><td>

1.  Set glide.record\_watcher.debug.extra to true.
2.  Ensure that 'sys\_rw\_action' contains a few entries. If not, create them.
3.  Shorten the interval glide.record\_watcher.cleaner. orphaned\_persisted\_responders. cleanup\_interval to 10 \(seconds\) for testing \(so the breakpoint below 1 can be hit more often\).
4.  Put a debug pointer at getPersistedRespondersFromDatabase before the actual query.
5.  When breakpoint hits, shut down the DB.
6.  Resume the program.
7.  Check the logs.

 Expected behavior: Responders are kept in the memory.

 Actual behavior: A log message like 'removing persisted watchers for tables: \[list of all tables in memory\]'.

</td></tr><tr><td>

Request Management

 PRB1781853

</td><td>

Catalog task related records issues

</td><td>

When the user has the sn\_request\_read and sn\_request\_write roles, they cannot see records in the 'Related records' section of the SOW list view page.

</td><td>

1.  Log in with the sn\_request\_read and sn\_request\_write roles.
2.  Navigate to the SOW list view page.
3.  From the Catalog tasks - Assigned to your groups, select the SCTASK0010004 record.
4.  Select the **Related records** section.

 Notice that the affected CI section shows an exception error page and the group approval section count shows 1 with no record displayed.

</td></tr><tr><td>

Request Management

 PRB1781908

</td><td>

A request created for a field value is assigned to a logged in user name automatically

</td><td>

After the request is created, it is assigned to a logged-in user instead of the specified user.

</td><td>

 

</td></tr><tr><td>

Request Management

 PRB1784152

</td><td>

sn\_request\_read doesn't contain the interaction agent role

</td><td>

incident\_read, problem\_read, and change\_read all contain the interaction agent role. But sn\_request\_read doesn't contain an interaction agent role.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1792462

</td><td>

When an assigned task is canceled, it's returned as part of locked\_tasks

</td><td>

A locked task query was getting both canceled and closed tasks. Upon investigation, only closed tasks should be sent as locked.

</td><td>

1.  Create a work order task in the 'Pending Dispatch' state with the window\_end date as the future.
2.  Perform a graph QL query for the batch.

The task should be returned as part of 'tasks'.

3.  Assign it an agent either manually or run SO.
4.  Cancel the same task.
5.  Perform a graph QL query for the batch.

 Observe that the task is returned as part of 'locked\_tasks', which isn't expected.

</td></tr><tr><td>

Script Includes

 PRB1769195

</td><td>

A fix script takes a long time when upgrading from Washington DC to Xanadu

</td><td>

The fix script, 'DEF0458037\_set\_client\_ callable\_script\_includes\_sandbox \_callable\_part\_2.xml' takes a long time to load.

</td><td>

 

</td></tr><tr><td>

Script Includes

 PRB1785008

</td><td>

Many RCAS are invalidated after upgrading to Xanadu due to a fix script issue

</td><td>

Script includes are modified after upgrading to Xanadu which invalidates the RCAs. This only happens on RCAs with 'Source Type: Script Include'.

</td><td>

 

</td></tr><tr><td>

Search Administration

 PRB1731361

 [KB1695005](https://hi.service-now.com/kb_view.do?sysparm_article=KB1695005)

</td><td>

Global text search is broken in /buildtools1 for UI16

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Search Administration

 PRB1789281

</td><td>

There's cache issues across domains when performing a global search

</td><td>

There's cache issues across domains when performing a global search if the 'text\_search' view on a list contains a short description in one domain and doesn't contain it in another domain.

</td><td>

1.  Navigate to any instance in a Washington DC version.
2.  Ensure that in the global domain there's a text\_search view on the incident table.
3.  Set up a text\_search view on the incident table in a domain other than global. Be sure not to include any string fields in the list layout.
4.  In this new domain, execute a global search against an incident that has previously not been searched on.
5.  Validate if 'No Title' or the sys\_ID is displayed in the search preview.
6.  Switch to global domain.
7.  Complete a search for the same incident.
8.  Validate if 'No Title' or the sys\_ID is still displayed.
9.  Try vice versa across both the domains.

 Notice that Verify that there is an issue after clearing the cache \(after cache.do\).

</td></tr><tr><td>

Server-side scripts

 PRB1783318

</td><td>

The **sandbox\_callable** field does not work for scoped applications

</td><td>

The **sandbox\_callable** field is not enforced for scoped applications, so scoped app developers cannot make use of it.

</td><td>

1.  Navigate to base instance Script Include GoalFrameworkAjaxProcessor and uncheck 'sandbox enabled'.
2.  Navigate to Background Scripts and run the following script in sandbox: 'sn\_gf.GoalFrameworkAjaxProcessor\(\)'.

 Expected behavior: Observe an error about the script include not being available in sandbox.

 Actual behavior: Script include is still callable from the sandbox.

</td></tr><tr><td>

Service Catalog Builder

 PRB1793077

</td><td>

When creating template from catalog builder, changing questions in the 'Available for' list marks them as AI generated

</td><td>

The AI 'sparkle' icon appears, indicating that questions are AI generated when they are not.

</td><td>

1.  Open catalog builder.
2.  Select **Create a Catalog item template**.
3.  Give a name to a template and navigate to the 'Questions' step.
4.  Select the gear icon and shuffle some variable types in the slush bucket between the left and right slush bucket.
5.  Select **Save Selections**.

 Actual behavior: Notice that the AI sparkle icon appears before the questions step.

 Expected behavior: The AI sparkle icon shouldn't appear as this is not AI generated.

</td></tr><tr><td>

Service Catalog

 PRB1788268

</td><td>

Dot-walking to the second level with g\_form in the Catalog Client script makes the catalog non-conversational

</td><td>

There's a steep drop in the conversational catalog coverage due to client scripts, which involves second level dot walking on g\_form object.

</td><td>

 

</td></tr><tr><td>

Service Level Management

 PRB1790083

</td><td>

Some field values are wrong when using the CheckpointWalker random access walkTo\(checkpoint\)

</td><td>

This occurs when the pointer to current history is closer to the end, and History walks backwards.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1745336

</td><td>

The property that limits the number of lookup items added to the service model should include cmdb\_ci\_network\_adapter

</td><td>

'sa.lookup\_tables. tables\_for\_limited\_query' is a comma-separated list of table names to limit the lookup query. A limit is added to the table list, and all tables are inherited from them. The default value is cmdb\_ci,cmdb\_serial\_number. 'sa.lookup\_tables. exclusion\_tables\_f or\_limited\_query' is intended to complement 'sa.lookup\_tables. tables\_for\_limited\_query'. It's a comma-separated list of table names to unlimited lookup query. The table list is unlimited, and all tables are inherited from them. The default value is empty. 'sa.lookup\_tables.max\_records\_to\_check' involves the numbers of records to limit the lookup query. The default value is 100.

</td><td>

1.  Create many records \(7-9K\) for a network adapter on any switch in cmdb\_ci\_network\_adapter.
2.  Add this switch to an application server.
3.  Run recomputation of the service with this switch.

 An error displays: 'WARNING \*\*\* WARNING \*\*\* Large Table: Table handling an extremely large result set: 45321...'

</td></tr><tr><td>

Service Mapping

 PRB1791752

</td><td>

Put a hard limit on properties that can be destructive

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Service Mapping

 PRB1795145

 [KB1700187](https://hi.service-now.com/kb_view.do?sysparm_article=KB1700187)

</td><td>

Changes to ServiceMappingScript Engine\#runEngine incurs &gt;9% performance overhead for App CPU for GlideRecord inserts on cmdb\_rel\_ci table

</td><td>

There is some degradation in the CPU usage when inserting a new relation \(cmdb\_rel\_ci\). Any insert action may consume more CPU. If application\_extension application is installed, the degradation may be even worse.

</td><td>

 

</td></tr><tr><td>

ServiceNow Studio \(Legacy\)

 PRB1788174

</td><td>

Update the SnS URL in Studio

</td><td>

If a developer using ServiceNow Studio launches the legacy Studio application, they can launch the new ServiceNow Studio. If they are already working on an application, then ServiceNow Studio will open with the corresponding application open.

</td><td>

1.  Navigate to the studio.
2.  Try to open SnS from the banner.

 Expected behavior: The user can navigate to SNS from the legacy studio entry point.

 Actual behavior: The URL is not working.

</td></tr><tr><td>

Service Reliability Management \(Family release\)

 PRB1787187

</td><td>

Duplicate copies of ACL files that were moved to a hosted plugin still exist in the global scope

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1763064

</td><td>

Change access to the Microsoft Teams Sidebar documentation to an internal document

</td><td>

When the Microsoft Teams Sidebar fails to add participants to the discussion due to the max limit of participants reached, an error message with a link to the documentation appears. The link accessing the Microsoft Teams Sidebar documentation must be changed to an internal document link.

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1789913

</td><td>

The glide.collab.group \_search\_limit property is not honored during candidate search

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1782652

 [KB1698516](https://hi.service-now.com/kb_view.do?sysparm_article=KB1698516)

</td><td>

The Summary section of the Publishers overview page is taking too long to load due to the 'Actual savings' query

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Models

 PRB1785844

 [KB1651223](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651223)

</td><td>

com.snc.sams plugin takes a long time to load during Washington DC to Xanadu upgrade

</td><td>

The fix script takes approximately 32 mins to upgrade com.snc.sams plugin from Washington DC to Xanadu.

</td><td>

 

</td></tr><tr><td>

Syntax Editor

 PRB1771372

</td><td>

The scripting window is missing a button

</td><td>

The scripting panel is missing a button that gives the user access to scripting variables.

</td><td>

1.  Open an instance with the orchestration plug-in installed.
2.  Open the Workflow Editor.
3.  On the right side-panel, select the 'Custom' tab.
4.  Select the **+** next to the filter box and select **REST Web Service**.
5.  Give it any name and select **Continue**.
6.  Select the **Outputs** tab.
7.  Select **Navigate to Post-Processing**.

 Expected behavior: The scripting panel has an adjacent button to give access to scripting variables.

 Actual behavior: The scripting window no longer has the **&gt;** button.

</td></tr><tr><td>

System Events

 PRB1789717

</td><td>

On upgrade, job difference is not honored for newly migrated queues

</td><td>

 

</td><td>

1.  Log in to a pre-Xanadu instance with two nodes.
2.  Navigate to the SYS\_TRIGGER table and verify the job 'events process 0'.
3.  Create another job by cloning the Parent job.
4.  Upgrade the instance to Xanadu.
5.  For testing purpose, navigate to Table Rotations and synchronize the shards for the SYS\_EVENT table.
6.  Navigate to **All** &gt; **System Policy** &gt; **Queue Registry** and search for the Default queue.
7.  Open the default queue and wait until it gets provisioned.
8.  Validate the jobs in the Queue Configuration table.
9.  Navigate to the SYS\_TRIGGER table and verify the job 'events process 0'.

 Expected behavior: Four jobs should be available for the Default Queue.

 Actual behavior: Only two jobs are available.

</td></tr><tr><td>

System Export Sets

 PRB1792544

 [KB1699358](https://hi.service-now.com/kb_view.do?sysparm_article=KB1699358)

</td><td>

If Log Export Service \(LES\) is enabled and the LES source is configured with syslog in a global scope filter, there's a null pointer exception when using gs.log after a Washington DC upgrade

</td><td>

There's an error: 'Script execution error: Script Identifier: null.null.script, Error Description: java.lang.NullPointerException, Script ES Level: 0 Couldn't decipher the stack trace resulting from the following JavaScriptException...'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Import Sets

 PRB1786846

</td><td>

The JDBC data source on the MID server does not process JDBCProbeCompleted response

</td><td>

The 'MID Server Cluster Management' business rule supports the JDBC data source to support fail-over and load balancing. This results in the MID server to be unable to process the JDBCProbeCompleted response, because the JDBCProbe loader query is in the JDBC data source.

</td><td>

1.  Create a TD instance with the MID server.
2.  Run a local MID server to connect to TD instance to create two MID server instances.
3.  Create a MID cluster.
4.  Add the two MID servers.
5.  Add the equal capabilities.
6.  Configure a JDBC data source to load data into the MID server to ensure data can load through the local MID server.
7.  Set the state of the TD MID server to 'down'.
8.  Set the JDBC data source MID server to the original TD MID server.
9.  Load all records.

 Notice that data is loaded properly and the JDBCProbeCompleted record remains. After five minutes, the JDBCProbeError message is visible in ecc\_queue.

</td></tr><tr><td>

Table Cleaner

 PRB1792186

</td><td>

Table Cleaner chunkDelete\(\) stops after only a few loops

</td><td>

The check to prevent Table Cleaner from 'spinning' when it is trying to delete non-existent records immediately stops chunkDelete\(\) when conditions are met, even if there are additional records that still need to be deleted.

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1777951

</td><td>

Unassigning a task on Dispatcher Workspace sets the assigned group to an empty string literal

</td><td>

When a work order task has been unassigned using a content menu on a Workspace event, a task on Customer Service Portal, or a task card on the left task panel, the assignment group is set to an empty string literal. This empty string literal breaks the auto-assign / dynamic scheduling flow for the same task.

</td><td>

1.  Install the FSM Configurable Dispatcher Workspace Version 25.0.7 store application.
2.  Install the Field Service Territory Planning plugin.
3.  Navigate to the Dispatcher Workspace.
4.  Assign a Work Order Task that has a territory field set to a value.
5.  Unassign the Work Order Task.
6.  Open the Work Order Task in native UI.
7.  Navigate to **History** &gt; **Calendar**.

 Observe that the assignment group is set to an empty string literal.

</td></tr><tr><td>

Territory Planning

 PRB1791695

</td><td>

Adhoc agents are not loaded under a territory if the territory doesn't cover an assignment group and only has adhoc agents

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1763233

</td><td>

Changing the default values of archives, attachments, audits and journals for job offloading to improve instrumentation and detect lag

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1790724

</td><td>

Tables in the tier 2 storage offload are not excluded from cloning

</td><td>

The tables SYS\_ARCHIVE\_TIER2\_CHUNK, SYS\_ATTACHMENT\_INDEX, sys\_attachment\_tier2\_chunk, sys\_journal\_field\_tier2\_chunk, sys\_audit\_tier2\_chunk are not excluded from cloning. The tables should not be cloned because a cloned instance may reference different S3 buckets and clusters from its source.

</td><td>

 

</td></tr><tr><td>

Tier 2 Storage Offload

 PRB1791750

</td><td>

Destroying offloaded related records silently fails if parent and child are in different destroy chunks

</td><td>

Not all records are removed from S3 and index tables.

</td><td>

Note: the ability to reproduce this bug is dependent on the order in which the tables come up in destroy chunking, so it is best to use these exact table names.

 1.  Create two tables: u\_archive\_test and u\_archive\_test\_detail, such that one field in u\_archive\_test\_detail references the sys\_id of u\_archive\_test.
2.  Populate u\_archive\_test with two records.
3.  Populate u\_archive\_test\_detail with one record that points to one of the u\_archive\_test records.
4.  Create an archive rule on u\_archive\_test and an archive related record so that the record in u\_archive\_test\_detail gets archived by the archive rule.
5.  Archive and offload all records.
6.  Set the property glide.db.archive\_destroy.batch\_size to '1'.
7.  Create a destroy rule on u\_archive\_test with near-zero duration and enable the destroying of related records.
8.  Run the destroy job.

 Expected behavior: All records are removed from S3 and the index tables.

 Actual behavior: The u\_archive\_test\_detail record does not get removed from the index table \(and S3\).

</td></tr><tr><td>

Time Card Management

 PRB1785263

</td><td>

Managers are unable to copy timecards

</td><td>

When a manager attempts to copy time cards for one of their reports, the system returns \{0\} time cards created.

</td><td>

1.  Impersonate a manager in an instance.
2.  Select a user from the user list.
3.  Select the **Copy time card** button.
4.  Select the date for the time sheet.
5.  Select **Okay**.

 Observe the error message.

</td></tr><tr><td>

UI Field Administration

 PRB1753031

</td><td>

The user observes an error when accessing the 'Manage Human Resource Catalog' page

</td><td>

The error reads: 'Unexpected token '\)' \(at js\_includes\_ng\_dc.jsx'.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1789428

</td><td>

Content on the **TinyMCE** field fails to load upon selecting a value from the dependent field unless refreshed

</td><td>

Links do not appear in HTML fields and other content issues.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1783850

 [KB1651462](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651462)

</td><td>

High memory usage by viewrule\_all\_cache \(Workspace View Rules\)

</td><td>

The viewrule\_all\_cache can consume excessive memory on application nodes. This can cause memory contention/increased garbage collection/application node performance degradation.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB1776398

</td><td>

After a family upgrade and activating the Store app, conditional content isn't being installed

</td><td>

 

</td><td>

1.  Provision an instance in Washington DC.
2.  Upgrade the instance from Washington DC to Xanadu.
3.  Upgrade the Security Center \(SC\) Store app from 1.5.3 - 1.6

 Expected behavior: The 'Client push notifications' table exists and the glide.cmdb.canonical.url property is displayed.

 Actual behavior: The sn\_vsc\_client\_push\_notifications table, and others, are missing.

</td></tr><tr><td>

Usage Analytics

 PRB1771870

</td><td>

Generate a token using private/public key pair in the instance instead of getting it from Gateway

</td><td>

Glide should sign the JWT token with its own private key for specific app-id and expose the API to return a public key.

</td><td>

 

</td></tr><tr><td>

Usage Analytics

 PRB1778725

</td><td>

SDK changes to support the change in the security mechanism to send the token in the cookies

</td><td>

Metric API is incorrect and should be /uxa/now/web/metric instead of /uxa/web/metric.

</td><td>

1.  Log in to an AppSee-enabled instance as a user with elevated privileges.
2.  Navigate to the service portal \(/sp\).
3.  Inspect the request headers of the first metric API call.

 Expected behavior: The **channelType** field should be populated with appropriate values in the request headers, even for the initial call.

 Actual behavior: The **channelType** field is an empty string \(''\).

</td></tr><tr><td>

UXF Components

 PRB1792110

</td><td>

Forms in configurable workspaces do not display template values if the field has an attribute of staticDependent

</td><td>

If the dictionary entry has an attribute for staticDependent then that template value field does not display in any form within configurable workspaces, but if a table field is defined and the template value is then set to use that table field as its dependent then the field displays.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1792196

</td><td>

The 'Extend your session' option isn't occurring for single sign-on \(SSO\) users

</td><td>

After upgrading an SSO-enabled instance to Washington DC, users no longer see the 'Extend your session' modal on the 'Platform' view. Instead, users are logged out after their session times out. This causes work to be lost. The modal still appears in the /esc and /sp portals, however. For the 'Extend session' modal to appear for SSO users, glide.ui.session.show \_modals.override must be created if it doesn't exist and set to 'true' in the system properties 'All' menu.

</td><td>

1.  Navigate to an instance with read/write access via SSO.
2.  From the filter navigator, navigate to **Content Library** &gt; **View All**.
3.  On the next screen, select **New** in the top-hand corner.
4.  In the modal that pops up, select **Rich Content**.
5.  Select **Continue**.
6.  In the left-hand column, in the **Content name** field, enter any value.
7.  Select **Open Editor**.
8.  Select and type in the card.

 Observe that after 15 minutes, the user is logged out automatically and no modal populates.

</td></tr><tr><td>

Virtual Agent Designer

 PRB1786655

</td><td>

Virtual Agent LLM notification actions are not displayed and the conversation gets stuck

</td><td>

When actionable notifications are triggered, the actions are not displayed or conversation gets stuck and the user cannot take any action.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Designer

 PRB1793134

</td><td>

A user without elevated privileges can't create a large language model \(LLM\) sys\_cs\_context\_profile

</td><td>

 

</td><td>

1.  Impersonate a user that doesn't have elevated privileges, but has the virtual\_agent\_admin role.
2.  Navigate to /sys\_cs\_context\_profile.do.

 Observe the **model\_type** field is NLU/keyword and can't be set to LLM.

</td></tr><tr><td>

Virtual Agent Designer

 PRB1793793

</td><td>

NAVA topic execution doesn't populate the 'API' column in a sys\_cs\_fdih\_invocation table, causing ETL job failure

</td><td>

For regular Virtual Agent conversations, topic execution populates an 'API' column in a sys\_cs\_fdih\_invocation table, which is used by the ETL job to process the conversations. However, for NAVA conversations, topic execution doesn't populate the 'API' column, which leads to ETL job failure, causing the Virtual Agent dashboard to not display all conversations.

</td><td>

1.  Set up NAVA.
2.  Search 'What is spam'.
3.  Check the sys\_cs\_fdih\_invocation table for the 'API' column of the newly generated record.

 Expected behavior: The 'API' column is populated.

 Actual behavior: The 'API' column is empty.

</td></tr><tr><td>

Virtual Agent

 PRB1782232

</td><td>

Utterance length isn't checked at topic discovery, which allows large utterances that cause a slow down

</td><td>

In topic discovery, no input length is checked, so large utterances can be passed into the search. Also, USER\_INPUT\_MAX\_LENGTH isn't checked and is also too large for topic discovery.

</td><td>

1.  Provision an instance with the glide.cs.chatbot plugin.
2.  Start a conversation with a virtual agent.
3.  Enter a large utterance at topic discovery.

 Observe slowness.

</td></tr><tr><td>

Virtual Agent

 PRB1784826

</td><td>

A JavaScript console error appears when the Virtual Agent chat is open in the Service Portal UI

</td><td>

A JavaScript console error appears in the Service Portal UI as a result of a keyboard shortcut API returning with a code in the 400-500 range.

</td><td>

1.  Select **Track your Tickets**.
2.  Open any case.
3.  Select the chat option to launch the Virtual Assistant in the Engagement Messenger.

 Notice that the console error appears on the browser and in JavaScript.

</td></tr><tr><td>

Virtual Agent

 PRB1787170

 [KB1650880](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650880)

</td><td>

The VA in Now Assist is unresponsive when reaching the variable maximum in client scripts

</td><td>

The VA in Now Assist for the Platform is unresponsive and does not populate values when it reaches the variable maximum in client scripts, especially when a client script sets values for 100 variables for a catalog item.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1787404

</td><td>

Reloading the page causes the carousel to vanish

</td><td>

When a query is typed into Virtual Agent chat, a carousel related to the query is shown. If the user refreshes the page, the carousel vanishes.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1787965

</td><td>

Now LLM summary input and total tokens is incorrectly displayed

</td><td>

Now LLM Summary prompt response shows a valid response but input tokens = 1 and total tokens = 1

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1789855

 [KB1651479](https://hi.service-now.com/kb_view.do?sysparm_article=KB1651479)

</td><td>

In Virtual Agent after a Washington DC upgrade, every input that matches more than one keyword throws an error

</td><td>

Virtual Agent should display all topics that match a keyword, but it displays a technical error message or occasionally hangs.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1791763

</td><td>

The GetSkillDetails API of oneextendUtil is not populating tableName and query for attributes of type glide\_record

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1791956

</td><td>

Multiple entities for slot filling cause a conversation to crash

</td><td>

When an NLU-based user has multiple entities in a conversation being filled during NLU topic switching, a choice picker is presented. After a choice is made VA displays 'I'm having technical issues and won't be able to continue this conversation'.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1793069

</td><td>

Some dependencies are missed during installation of the Now Assist for Creator \(NAFC\) 26.1.1 bundle

</td><td>

The user observes an error message when an utterance is sent on the Now Assist Panel \(NAP\).

</td><td>

1.  Provision an instance with 'Now Assist for Creator' \(26.1.1\) installed.
2.  Make sure sn\_text2analytics \(1.0.5\) is installed along with the NAFC installation.
3.  Enable 'Data visualization skill' from 'Now assist skill for creator' under Now Assist feature \(**All** &gt; **Now assist admin** &gt; **Now Assist features** &gt; **Creator**.
4.  Enable NAP under settings \(**All** &gt; **Now assist admin** &gt; **Settings** &gt; **Now assist panel**\).
5.  Open NAP and send an utterance \(for example, 'number of open incidents by category'\).

 Observe the message: 'Sorry, there was a problem on my side trying to complete this request. Try asking again later.' Also, the sys\_cs\_fdih\_invocation\_list table logs show 'response state' as 'TIMED\_OUT'.

</td></tr><tr><td>

Word Document APIs

 PRB1789946

</td><td>

A corrupted Word document generates from the WordDocumentAPIs after a recent update in Microsoft Office Word

</td><td>

This is happening because of a recent update in Microsoft Office. If a template is created out of this version, it adds a few new tags into the document. These aren't handled yet in the APIs.

</td><td>

1.  Create a Word template document with MS Office Word with the 16.85.x version.
2.  Add it to the 'Contract' template.
3.  Parse it.
4.  Initiate a contract with this template document.

 Observe that the document is generated, but if it's downloaded and opened, the document is corrupted.

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu EA Hotfix 1](xanadu-patch-0-hf-1-PO.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


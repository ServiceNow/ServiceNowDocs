---
title: Xanadu Patch 9
description: The Xanadu Patch 9 release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2025-06-16"
reading_time_minutes: 90
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# Xanadu Patch 9

The Xanadu Patch 9 release contains important problem fixes.

-   **Xanadu Patch 9 was released on June 05, 2025.**
    -   Build date: 06-04-2025\_0434
    -   Build tag: glide-xanadu-07-02-2024\_\_patch9-05-21-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X09.00.xlsx).

## Overview

Xanadu Patch 9 includes 406 problem fixes in various categories. The chart below shows the top 10 problem categories included in this patch.

![Fixed issues grouped by problem categories bar chart](../image/prb-chart-xp9.png "Top 10 problem categories")

## Security-related fixes

Xanadu Patch 9 includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Xanadu Patch 9, refer to [KB2189031](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2189031).

## Changes in Xanadu Patch 9

-   **[Activate indexing of catalog variable content on Catalog Item records](https://www.servicenow.com/docs/access?context=activate-catalog-variable-indexing&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Activate indexing of searchable content from variables on Catalog Item records. Configure the set of Catalog Items eligible for catalog variable indexing and the set of variables to index.

-   **[AI Search system properties](https://www.servicenow.com/docs/access?context=system-properties-ais&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    **glide.ais.ingestion.catalog\_variables\_filter\_query**

    **glide.ais.ingestion.ignore\_catalog\_variables\_read\_roles**

    **glide.ais.ingestion.index\_catalog\_variables**

-   **[Variable types supported by AI Search indexing](https://www.servicenow.com/docs/access?context=variable-types-ais-index&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)**

    Service Catalog variable types indexed from Catalog Items

-   **[Field Service Management release notes](../field-service-management/field-service-management-rn.md)**

    Google Maps APIs for Field Service CapabilitiesUpgrade to the new Places API \(new\) and Routes API for Field Service Capabilities.Effective March 1, 2025, Google has designated the Places API, Directions API, and Distance Matrix API as Legacy services. The newer versions of these services are Places API \(New\) and Routes API.: You can’t enable or generate new API keys for these legacy services. However, you can continue using these services with the existing API keys. Enable the new APIs from Google Console to continue using the API services without any issues.If you create a new Google API key after March 1, 2025, enable the new APIs from Google Console to use these services with the new API keys.For more information see, [KB2111488](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=3b86844293516210f538fb2d6cba10bf), [KB2112054](https://support.servicenow.com/nav_to.do?uri=kb_knowledge.do?sys_id=47952c8a93556210f538fb2d6cba1026), and [Changes to Google Maps Platform automatic volume discounts, monthly credit, and services transitioning to Legacy status](https://developers.google.com/maps/billing-and-pricing/faq#legacy).


-   **QueryRangeACLAuditor**

    This patch includes the May Maintenance update script in the form of a script include \(QueryRangeACLAuditor\). This script is not triggered automatically and must be run after a patch upgrade. More details on running the QueryRangeACLAuditor and its functionality can be found in [KB2046494](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2046494).


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

Form Builder

 PRB1820975

 [KB1987480](https://hi.service-now.com/kb_view.do?sysparm_article=KB1987480)

</td><td>

A form isn't saved on a cross scope in ServiceNow studio

</td><td>

There's an error in the networking calls.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Integration Hub

 PRB1834445

</td><td>

GCF Data Egress recorder should support 0 byte inputs

</td><td>

GCFDataEgressRecorder will throw an error with an Invalid event value when an event with 0 bytes is recorded, creating an error in the log.

</td><td>

Post to the instance on an endpoint.

 Notice that this will return an 204 \(no content\) response a zero byte response.

</td></tr><tr><td>

MID Server

 PRB1870465

 [KB2022624](https://hi.service-now.com/kb_view.do?sysparm_article=KB2022624)

</td><td>

ECCSender does not use the correct character set when reading XML queue files

</td><td>

ECCSender uses the default file encoding/character set when reading XML queue files from a disk. This results in incorrect characters in the response for some special characters. ECCSender should use UTF-8 when reading these files, as XML queue files on disk are always UTF-8.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Related Lists

 PRB1887019

 [KB2122691](https://hi.service-now.com/kb_view.do?sysparm_article=KB2122691)

</td><td>

Users can't edit from a related list on a reference field configured to be read-only in the dictionary

</td><td>

Users are no longer able to add existing related records via the 'Edit' function on a related list when the reference field on the target table is marked as read-only. This behavior was previously functioning as expected. The issue has been verified in multiple relationships. Removing the 'read-only' attribute from the reference field restores expected functionality, confirming the change in behavior post-upgrade.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Import Sets

 PRB1850436

 [KB2115235](https://hi.service-now.com/kb_view.do?sysparm_article=KB2115235)

</td><td>

There's unexpected column creation when importing an Excel file with Japanese headers

</td><td>

When importing a file with Japanese headers, a new 'u\_xxx' column is created, even though the u\_email column already exists. This issue also occurs in Washington DC.

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

 PRB1891090

</td><td>

Addition of Query ACLs in Access Control List \(ACL\) Rules

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1889272

</td><td>

GlideSearch\_Query/suggestions user context gathering triggers role creation

</td><td>

When gathering user context, the platform triggers role creation

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1889718

</td><td>

Addition of Query ACLs in Access Control

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1889719

</td><td>

Addition of Query ACLs in Access Control

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1892867

</td><td>

The basic query range operation is broken

</td><td>

The basic query\_range operation on allowed fields isn't working, and the user sees records not applied by the filter.

</td><td>

1.  Log in as an admin user.
2.  Navigate to any table, for example sn\_customerservice\_case.
3.  Apply any query\_range filter on any field.

 Notice that the list shows all the records instead of the filtered.

</td></tr><tr><td>

Accounts Payable Invoice Processing

 PRB1889729

</td><td>

Addition of Query ACLs in Accounts Payable Invoice Processing

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1830587

</td><td>

Activity Stream doesn't limit the size of journal fields

</td><td>

The maximum size of journal entry appears to be either 50Kb or 100Kb by default. UI16 has a 10MB limit on the total journal field size. Once this limit was reached it truncates every journal entry to 50K. The entry cap is 250 by default. The entry cap is 30 for attachments. The size cap + entry cap is what ensured no out of memory errors in UI16.

</td><td>

1.  Create a script that creates a 10MB work note. This can be a 100 character string that is appended to the work note 100,000 times in a loop.
2.  Add 2-3 of these to a single incident.
3.  Request the incident in Service Operations Workspace \(SOW\).

 Expected behavior: The incident should load with these massive strings.

 Actual behavior: Chrome and Edge crash as the browser runs out of memory.

 1.  Add 100 of the 10MB work notes from \#1.
2.  Request the incident.

 Expected behavior: The incident should load in SOW.

 Actual behavior: The Glide server crashes with an out of memory error.

</td></tr><tr><td>

Activity Stream

 PRB1882348

</td><td>

Avatars are not shown for AI agent updates in the Activity Stream

</td><td>

When agents update fields and post work notes to the Activity stream the agent avatars are not shown next to their activities.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1890397

</td><td>

Two extras in the SQL count from the activity jelly template are seen in znowassiststable, causing a DMT SQL Spike

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1894361

</td><td>

Timeago elements \(sn-time-ago\) should display a tooltip when accessed via the keyboard

</td><td>

 

</td><td>

1.  Navigate to any instance.
2.  Launch the Employee Service Center \(ESC\) portal by appending '/esc' to the URL.
3.  Navigate to the 'My Requests' menu item in the header.

The 'My Requests' page opens.

4.  Using the keyboard, navigate through the list of requests. Select 'Tab' until the time focus goes on a sn-time-ago element.

 Expected behavior: If the focus should move to the non-interactive elements for sighted users who use the keyboard, then the tooltip should appear without hovering over it.

 Actual behavior: The tooltip isn't visible when the focus moves to the 'created/updated' elements using the tab key.

</td></tr><tr><td>

Advanced Risk

 PRB1891325

</td><td>

Addition of Query ACLs in Advanced Risk

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1766052

</td><td>

An incorrect chat workspace tab is highlighted when closing one of the chat tabs

</td><td>

One of several open chats is highlighted as if it contains a new message, but no message appears.

</td><td>

1.  Log in to an instance in a browser tab.
2.  Impersonate an Agent and stay available in Service Operation Workspace.
3.  Initiate three separate chats \[Chat 1, Chat 2 and Chat 3\] as an end user in three separate incognito tab sessions, and connect all of them to the live agent.
4.  As the Agent, accept all three chats and initiate conversations with them.
5.  As the end user, end chat 1.
6.  As the agent, close the chat 1 tab in Agent Workspace.

 Observe that as soon as the chat 1 tab is closed, the chat 2 tab reloads and the chat 3 tab highlights as if there is a new message, but there is no new message in the chat 3 tab.

</td></tr><tr><td>

Agile Development

 PRB1889742

</td><td>

Addition of Query ACLs in Agile Development

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1823459

</td><td>

AI Search indexing Topic Path Translation doesn't work for non system user preference language

</td><td>

Session users assigned as 'guest' with the sys\_user\_preference file 'name=user.language' and 'value=non\_user\_session\_language' will have topic paths indexed in this language. The set language is not effective, which is the cause of incorrect translations.

</td><td>

1.  Ensure sys\_language has two active languages, **en**for English and **de** for Deutsch.
2.  Create an entry in the sys\_user\_preference table with the following values:
    -   system = true
    -   user = empty with language as 'de'
3.  Create the catalog item with translations for topic and topic path.

 Expected behavior: AI Search should index, and be able to search with the 'en' topic value.

 Actual behavior: AI Search indexes content with Deutsch translations for documents with both English and Deutsch languages, and the search for English will fail.

</td></tr><tr><td>

AI Search

 PRB1824166

</td><td>

A translated reference field is indexed in a different language in a single record update vs a full table index

</td><td>

The peekahead is using the same value for different langauges.

</td><td>

1.  Enable i18n Spanish.
2.  Insert a KB record kb\_knowledge\_base=knowledge, language=es.
3.  Wait for incremental index and dump the document.
4.  Verify that kb\_knowledge\_base is in Spanish.
5.  Re-index kb\_knowledge.
6.  Wait for incremental index and dump the document.

 Expected behavior: kb\_knowledge\_base is in Spanish.

 Actual behavior: kb\_knowledge\_base is in English.

</td></tr><tr><td>

AI Search

 PRB1850651

</td><td>

The 'All' tab is selected after a page is refreshed or when using the browser **Back** button

</td><td>

When performing a search in global, the The 'Knowledge' tab and the facet should be selected even after refreshing the page or using the **Back** button on the browser.

</td><td>

Scenario 1:

 1.  Open a Xanadu or Yokohama instance.
2.  Perform search in global for an incident or knowledge.
3.  Select the 'Knowledge' tab.
4.  Select any facet.
5.  Refresh the page.

 Expected behavior: The 'Knowledge' tab and the facet should be selected.

 Actual behavior: The facet is not selected after refreshing the page, and the 'All' tab is selected.

 Scenario 2:

 1.  Perform a search in global for an incident or knowledge.
2.  Select the 'Knowledge' tab.
3.  Select any facet.
4.  Select any search result.
5.  Use the **Back** button on the browser.

 Expected behavior: The 'Knowledge' tab and the facet should be selected.

 Actual behavior: The facet is not selected after using the **Back** button on the browser, and the 'All' tab is selected.

</td></tr><tr><td>

AI Search

 PRB1856064

</td><td>

NAP displays the error, 'Trouble processing your request' while promoted skills are working correctly

</td><td>

The skill is not being identified and indexing is not occurring automatically on the Skill table. Skill discovery is not happening, and the following error message is displayed, 'We're having trouble processing your request right now due to a temporary system issue. Please try again later.' However, when the Skill table is manually indexed, the skill gets discovered.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1857215

</td><td>

There's a KB performance issue when there are a large number of user criterias assigned to a KB

</td><td>

The AI Search on ITSP has become slow after a Washington DC upgrade. AI Search is invoking Knowledge Management without any filters on the KB bases that are associated with the profile. Once the property 'glide. ais. disable\_kbb' is set to true, response times come back to the pre-upgrade times.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1871798

</td><td>

Dynamic Window chat returns an error reading 'Sorry there was a problem on my side'

</td><td>

 

</td><td>

1.  Enable dynamic window on Service Portal
2.  Perform a search in chat.

 Notice an error that reads 'Sorry there was a problem on my side'.

</td></tr><tr><td>

AI Search

 PRB1882832

</td><td>

Fix tracer functionality end-to-end for search use cases

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1883872

</td><td>

A FPE new search isn't routed to the 'All' tab

</td><td>

 

</td><td>

1.  Open an instance with a May Store app.
2.  Ensure that FPE is enabled on the ESC portal.
3.  Search for the query 'what is cookie?'.
4.  Toggle the search.
5.  Perform the search again.
6.  Navigate to the 'Knowledge' tab.
7.  Perform a new search 'Apple iPhone' while still on the 'Knowledge' tab.

 Notice that no results are found.

</td></tr><tr><td>

AI Search

 PRB1883953

</td><td>

Signals aren't being captured for a carousel on the Portal

</td><td>

This isn't working for synthesized Genius results either.

</td><td>

1.  Open an instance with May store apps.
2.  Enable Now Assist QnA and Now Assist Actions on portal.
3.  Perform search for queries 'Apple iPhone' and 'What is spam?'.
4.  Perform actions like 'Open source'.
5.  Trigger the 'Process Queued Signals' job.

 Expected behavior: Signals should be logged in the sys\_search\_genius \_result\_event\_action\_list table.

 Actual behavior: Notice no entries are found in the sys\_search\_genius \_result\_event\_action table.

</td></tr><tr><td>

AI Search

 PRB1885285

 [KB2182142](https://hi.service-now.com/kb_view.do?sysparm_article=KB2182142)

</td><td>

When Zing is the search engine for global search, data broker is still executed and pollutes the syslog

</td><td>

The underlying cause is that the composite data broker resource in the UI Builder app for the global search page is wired up to use the search term from the URL as an input, and so executes every time it changes after the initial search.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1885594

</td><td>

AI Search attachment results aren't redirecting to the parent record

</td><td>

The issue is reproducible in Yokohama and Xanadu instances.

</td><td>

1.  Log in to an instance.
2.  Navigate to the ESC portal.
3.  Search for 'Dental'.
4.  Select the doc result of the article.

 Notice that the page not redirected to the parent record. It's redirected to the sys\_attachment.do? sys\_id=undefined&amp; searchterm=detail.

</td></tr><tr><td>

AI Search

 PRB1886467

</td><td>

AI Search results match incorrect template

</td><td>

When a View Config condition uses a reference field for a table the user doesn't have access to, AIS returns the field, but with a value of '' \(empty string\).

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1887375

</td><td>

'OR' conditions aren't correctly evaluated in EVAM lite

</td><td>

In SearchResultTemplateGenerator, there's logic to revert to legacy EVAM template engine if the condition is complex, but it doesn't currently catch 'OR' conditions.

</td><td>

1.  Set active=false to the Service Portal default view configuration.
2.  Search for 'IPV6' in Service Portal.

Observe that users get one result

3.  Modify the Service Portal 'Knowledge Search Results' view config to add 'knowledge\_base is Known Error'.
4.  Search for 'IPV6' in Service Portal.

Observe that users still get one result.

5.  Add an 'OR' condition to the 'Knowledge Search Results' view config for 'knowledge\_base is IT'.
6.  Search for 'IPV6' in Service Portal.

 Observe that users no longer get the result.

</td></tr><tr><td>

AI Search

 PRB1889190

</td><td>

Shared files aren't coming up on the znowassiststable instance portal

</td><td>

 

</td><td>

1.  Open an instance with znowassiststable.
2.  Enable Dynamic Window on Portal.
3.  Set up shared files.
4.  Impersonate a user.
5.  Navigate to Service Portal.
6.  Search for 'Who is \[User\]?'.

 Notice that users can see the people card on the portal but can't see shared files.

</td></tr><tr><td>

AI Search

 PRB1892850

</td><td>

Follow-up questions shouldn't start a new conversation in a chat

</td><td>

The issue occurs on Service Portal with Dynamic Window turned on when a user selects 'Follow-up', the 'Conversational catalog - request' in the chat, or selecting the topic on the portal. The issue only occurs in Xanadu.

</td><td>

1.  Open an instance with the latest build and Store apps.
2.  Enable Dynamic Window on Portal.
3.  Search for 'What is spam?', 'Order coffee', or 'Loaner laptop'.
4.  Wait for the synthesis response to load.
5.  Select the follow up question button/catalog citation or topic.

 Notice that on Service Portal with Dynamic Window turned on, the chat opens up starts a new conversation.

</td></tr><tr><td>

AI Search

 PRB1892854

</td><td>

The Now Assist full-page responsive mobile is unusable

</td><td>

The pre-search box is cropped on both the left and right side. The search results search box is cropped and buttons aren't accessible.

</td><td>

Open a full page search/search results in the mobile screen size.

 Notice that the search bar is accessible when the screen size is changed to the mobile view.

</td></tr><tr><td>

AI Service - Glide Interfaces

 PRB1889667

</td><td>

Addition of Query ACLs in AI Service - Glide Interfaces

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1846815

</td><td>

Admins users aren't able to repair/install all dependencies when domain separation is enabled

</td><td>

A parent application \(for example, Now Assist For CSM\) is installed successfully even though its dependencies \(for example, sn\_genai\_platform\) aren't installed during the process.

</td><td>

1.  Open an instance where domain separation is enabled.
2.  Create an admin user in a different domain.
3.  Log in or impersonate as that admin user.
4.  Change the domain to global.
5.  Attempt to install a parent application with known dependencies.

Notice that new dependencies aren't installed and there's domain related errors in plugin logs.

6.  Try to repair the same plugin.
7.  Verify that the new dependencies are still not installed and the domain related errors in plugin logs are still present.

 Notice that not all dependencies are be installed with the parent app.

</td></tr><tr><td>

Application Install Engine

 PRB1869500

</td><td>

The user is unable to upgrade a base app version when a batch install hosts a customized app

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1875817

 [KB2055547](https://hi.service-now.com/kb_view.do?sysparm_article=KB2055547)

</td><td>

Script Assets aren't getting the latest content post upgrade, even though the plugin version has the ...latest/openFrameAPI setICContext method

</td><td>

OpenFrame is a hosted plugin and brings in UI scripts as part of it. On the upgrade of the plugin, the newer methods in the UI scripts aren't showing up even though it exists in that version.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Application Manager

 PRB1834952

</td><td>

Service Bridge Base plugin doesn't automatically upgrade when the Service Bridge for Providers plugin is upgraded

</td><td>

This issue occurs for users in a non-global domain or scope.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1872436

</td><td>

Access to a crypto module is set to 'reject' by default for some users

</td><td>

There's a 'Issue while uploading .store file: Unwrapping failed' error due to the crypto module being set to 'reject' by default.

</td><td>

 

</td></tr><tr><td>

Application Manager

 PRB1886735

</td><td>

The 'Switch to Virtual Agent Web Client' link isn't receiving the keyboard tab focus

</td><td>

This impacts keyboard users who navigate documents sequentially and expect the focus order to be consistent with the sequential reading order.

</td><td>

1.  Navigate to any instance.
2.  Append sys\_store\_app\_list.do to the instance URL.
3.  Search for any Store plugin app, such as 'Virtual Agent Web Client'.
4.  Change the application scope to 'global'.
5.  Open the form.
6.  Tab to the 'Switch to Virtual Agent Web Client' link.

 Expected behavior: The 'Switch to Virtual Agent Web Client' link should be receiving the keyboard tab focus.

 Actual behavior: The 'Switch to Virtual Agent Web Client' link isn't receiving the keyboard tab focus.

</td></tr><tr><td>

Application Manager

 PRB1891971

</td><td>

The 'How Search works' info icon tooltip details are not announced by the screen reader

</td><td>

The JAWS screen reader doesn't read the tooltip content.

</td><td>

1.  Start JAWS.
2.  Navigate to the Home screen.
3.  Navigate to **Dashboard** &gt; **Entitled ServiceNow apps** &gt; **View all Applications**.
4.  Tab to the 'How Search works' info icon.

 Notice that JAWS does not read the tooltip content.

</td></tr><tr><td>

Application Manager

 PRB1892000

</td><td>

There's a focus management issue on selecting 'view more'

</td><td>

On selecting 'View More', more content is loaded. When pressing the tab key, the focus is going to the 'Skip to Main Content' link and not to the newly loaded items.

</td><td>

1.  Launch an instance in a Chrome browser.
2.  Navigate to **Filter** &gt; **All**.
3.  Navigate to **Admin center** &gt; **application manager** &gt; **View all Applications link.**.
4.  Scroll down and press **Enter** on the 'View more' link.
5.  Check where the keyboard focus is placed when the view more link is activated.

 Once more options are loaded and the user presses the tab key, the keyboard focus should go to the updated content and not to the 'Skip' link. However, when pressing the tab key, the focus is going to the 'Skip to Main Content' link and not to the newly loaded items.

</td></tr><tr><td>

Application Manager

 PRB1892002

</td><td>

The 'Sync in progress' and 'Sync completed' details aren't announced to screen reader users

</td><td>

On selecting 'Enter' on the **Sync Now** button, the sync starts progressing. That isn't communicated to the screen reader users.

</td><td>

1.  Launch an instance in a Chrome browser.
2.  Navigate to **Filter** &gt; **All**&gt;.
3.  Navigate to **Admin center** &gt; **Application manager**.
4.  Turn the screen reader on.
5.  Press enter on the **Sync** button.
6.  Check whether the screen reader communicates the sync in progress/complete state.

 Expected behavior: The 'Sync in progress' and 'Sync completed' details should be announced to screen reader users.

 Actual behavior: The 'Sync in progress' and 'Sync completed' details aren't announced to screen reader users.

</td></tr><tr><td>

Application Rationalization

 PRB1885498

</td><td>

Software asset management is a dependency for Technology Portfolio Management

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Career Aspirations

 PRB1890426

</td><td>

Addition of Query ACLs in Career Aspirations

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Career Conversations

 PRB1889708

</td><td>

Addition of Query ACLs in Career Conversations

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1852603

</td><td>

A record handling agent is unable to fetch HR case details

</td><td>

The record handling agent gives an error: 'The system is unable to get the record information'.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1874503

</td><td>

RCAs created during Email reply recommendation

</td><td>

An error message appears reading, 'Wrong status for RCA privilege'.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1874549

</td><td>

RCAs for KMGenAISimilarTaskSearchUtil are generated during multi-case KB generation

</td><td>

RCAs from KMGenAISimilarTaskSearchUtil to HR Core, Employee Relations, Legal Entities were added as requested RCAs in app-hr-gen-ai and will be allowed with the fix script. They previously did not target app-hr-genai, but did not get added to the apps that target them. This causes RCAs to be generated when generating multi-case KB that are in a 'Requested' state. It would need to be allowed for multi-case KB generation.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1874746

</td><td>

AI Agent Invoker topic errors out when usecase is executed from Now Assist Panel \(NAP\) with a case open

</td><td>

Selecting the use case in NAP with an open case throws an error in NAP and the logs.

</td><td>

1.  Log in as an admin user.
2.  Open an HR case for total rewards.
3.  Open NAP.
4.  Enter **Help me resolve this tuition reimbursement case**.
5.  Open the use case **Resolve policy for tuition reimbursement**.

 Observe the error in NAP and in the logs, and that an execution plan is not created.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1876687

</td><td>

Notification Agent is unable to fetch and update HR case details

</td><td>

The event will be generated and the notification will not be created. In some cases where the notification is generated, 'Actions' will not perform the expected operation.

</td><td>

1.  Hop on the instance.
2.  Impersonate an admin.
3.  Navigate to **AI Agent Studio** &gt; **Testing**.
4.  Test the use case 'Notification AI Agent'.
5.  Test the task.

 Notice that the event will be generated, but the notification will not be created; for generated notifications, selecting **Actions** will not perform the expected operation.

</td></tr><tr><td>

Case Management

 PRB1872131

</td><td>

Clustering isn't triggered because of a missing ACL

</td><td>

 

</td><td>

1.  Navigate to **All** &gt; **Now Assist Admin** &gt; **Feature** &gt; **Now Assist Skills**.
2.  Select **Suggested steps generation skills**.
3.  Select **Clustering progress**.

 Observe that the clustering progress bar is stuck.

</td></tr><tr><td>

Case Management

 PRB1889703

</td><td>

Addition of Query ACLs in Case Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Case Management

 PRB1892871

</td><td>

Cases RL on PI is not accessible to customer contact on business portal due to query match and query range ACLs

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Change Management Collision Detector

 PRB1868251

</td><td>

The 'Conflict Detection' job, especially the ChangeCheckConflictsSNC script include, can lead to an OutOfMemoryError and node restarts

</td><td>

This seems to happen when the Affected CIs \[task\_ci\] table has a large number of records on it. In one of the cases, there were 93,685,849 records.

</td><td>

Run the 'Conflict Detection' job and notice it loops in the ChangeCheckConflictsSNC script include.

</td></tr><tr><td>

Change Management

 PRB1849821

</td><td>

The **Closed Change Count** field under the 'std\_change\_ record\_producer' table is calculated incorrectly when multiple template records are created with the same template name

</td><td>

This is caused because the 'group by' query defined in the script 'StdChangeUtilsSNC' inside the function 'calculateVersionAndTemplateStats' is attempting to group by on the name rather than the sysID, which is leading to the incorrect calculation of the closed change count.

</td><td>

 

</td></tr><tr><td>

Change Management

 PRB1862569

</td><td>

Change CheckConflict can cause stale reads and updates, which causes unexpected other behaviors

</td><td>

 

</td><td>

 

</td></tr><tr><td>

CIWF UI Component

 PRB1894610

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for portal\_knowledge\_quick\_links widget

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Cloud Cost Management

 PRB1889713

</td><td>

Addition of Query ACLs in Cloud Cost Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Cloud Provisioning and Governance

 PRB1889715

</td><td>

Addition of Query ACLs in Product Service

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

CMDB Workspace

 PRB1894924

 [KB2181389](https://hi.service-now.com/kb_view.do?sysparm_article=KB2181389)

</td><td>

Remove CUD access to sn\_cmdb\_editor roles on cmdb\_ci records

</td><td>

Users with the role 'sn\_cmdb\_editor' shouldn't be able to have access to the cmdb\_ci table and edit the records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Code Signing

 PRB1761365

</td><td>

Trusted CS cert fails to validate

</td><td>

In the jsFunction\_validate\(Scriptable scr\) in CertificateValidator 'trusted\_code\_signing\_cert' is an unsupported type for validating certificate.

</td><td>

1.  Attach a cert to code\_attest module and install the leaf cert as trusted CS cert.
2.  From the related link, select **Validate certificate**.

 Expected behavior: The certificate should be validated.

 Actual behavior: The certificate is not validated and an error is thrown.

</td></tr><tr><td>

Code Signing

 PRB1854759

</td><td>

Frequent updates on the 'sn\_kmf\_record\_signature' table leads to excessive generation of text index events

</td><td>

Frequent updates on the 'sn\_kmf\_record\_signature' table leads to excessive generation of text index events, delaying the text index events processing on the instances.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1860810

</td><td>

Generate signatures for sys\_auto\_script table with wildcard mode

</td><td>

Generating signatures for sys\_suto\_script table records as they are invoking scripts writing to ecc\_queue directly from sys\_auto\_Script.

</td><td>

 

</td></tr><tr><td>

Code Signing

 PRB1869613

</td><td>

Guardrails should respect filter conditions on the signature configuration

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Communities

 PRB1889697

</td><td>

Addition of Query ACLs in Communities

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Communities

 PRB1889700

</td><td>

Addition of Query ACLs in Communities

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Compliance Case Management

 PRB1890990

</td><td>

Addition of Query ACLs in Compliance Case Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Configuration Compliance

 PRB1891686

</td><td>

Addition of Query ACLs in Configuration Compliance

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1868458

 [KB2015207](https://hi.service-now.com/kb_view.do?sysparm_article=KB2015207)

</td><td>

The empty domain path in the cmdb\_datasource\_last\_update table causes problems with IRE Reconciliation rules in a domain separated instance

</td><td>

Typically, when users insert or update a \(Configuration Item\) CI with a higher-priority data source defined in reconciliation rules, any other data source with a lower priority can't update the existing CI for the same attributes. However, attempted to replicate this behavior in a domain separated instance, the reconciliation rules weren't honored, and the lower-priority data source was able to update the CI. The domain path in the cmdb\_datasource\_last\_update table was empty, which causes the reconciliation rules to be ignored.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1872524

</td><td>

There's an exception RTE BeforeScript when trying to replace values corresponding to an item

</td><td>

When users try to replace item values, it causes an exception, like: 'ava.lang.RuntimeException: Before script unable to process records with error message: null'. IREScopedMapValues is expecting a map instead of an object. This needs to fixed for all other places where it is expecting java native objects.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1893434

</td><td>

A11y bug fixes on CMDB Workspace

</td><td>

Info tooltips are identified by screen readers as 'Search Button' and there's multiple H1 elements on a page.

</td><td>

Issue 1: Info tooltips are identified by screen readers as 'Search Button'.

 1.  Start JAWS.
2.  Navigate to **Home** &gt; **All** &gt; **CMDB Workspace** &gt; **Management tab**.
3.  Move the input focus to the info icon in excluded CIs.

 Note that the info tooltip is described as 'Search button'.

 Issue 2: Multiple H1 elements on the page.

 1.  Navigate to **Home** &gt; **All** &gt; **CMDB Workspace**.
2.  Start NVDA.
3.  Display the speech viewer in NVDA.
4.  Navigate through the page's headings.

 Notice that there are two H1s when there should only be one.

</td></tr><tr><td>

Content Management System

 PRB1880403

</td><td>

The CMS portal is corrupted after a Yokohama upgrade

</td><td>

It looks like there are CSS files for the portal that aren't loaded as expected.

</td><td>

 

</td></tr><tr><td>

Contextual Search

 PRB1872960

</td><td>

An external link can no longer be accessed in the cxs\_new\_window UI page

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Contextual Search

 PRB1883021

</td><td>

Addition of Query ACLs in Contextual Search

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Contract Management

 PRB1889710

</td><td>

Addition of Query ACLs in Contract Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Core Platform

 PRB1741148

</td><td>

Change SampleAccumulator fSamples into long\[\]

</td><td>

Instead of using an ArrayList of boxed longs, use a long\[\]. Also deduplicate the CompactStats objects that are empty using a non-mutable version.

</td><td>

 

</td></tr><tr><td>

Core Platform

 PRB1762070

</td><td>

ServiceNow Performance Dashboards have errors for some graphs

</td><td>

When the user navigates to Service Now Performance Dashboards, some of the graphs are not shown and instead the following error message appears: 'Error:Invalid series data'.

</td><td>

 

</td></tr><tr><td>

Core Platform

 PRB1775831

 [KB1818197](https://hi.service-now.com/kb_view.do?sysparm_article=KB1818197)

</td><td>

When the user accesses a CTI record URL before SSO or local login, they are redirected to an incident.do record

</td><td>

When the user is logged in to an instance, a CTI link takes them to the correct record. However, when they are logged out, they are directed to the incident.do page.

</td><td>

 

</td></tr><tr><td>

Core Platform

 PRB1881092

</td><td>

In an activity stream, be able to determine actions performed by an AI Agent on behalf of a user

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB1832361

</td><td>

When CSM is installed in Xanadu, the 'Overview' dashboard isn't appearing

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Customer Service Management

 PRB1848565

</td><td>

Creating a consumer user from a consumer form doesn't work

</td><td>

Creating a consumer user from a consumer form creates a sys\_user, not a csm\_consumer\_user. As a result, this user can't be linked with a consumer. This process should work according to documentation.

</td><td>

1.  Open any csm\_consumer record.
2.  Navigate to the 'Login Details' related list.
3.  Select the **User lookup** icon.
4.  Select **New** to create a user.

 Expected behavior: The user created should be csm\_consumer\_user, so this user can be linked with csm\_consumer.

 Actual behavior: The user created is sys\_user, so users can't select this user to link it with csm\_consumer.

</td></tr><tr><td>

Data Archiving

 PRB1865429

</td><td>

Infinite recursion is possible in the Archive Reparent Retry Job

</td><td>

In the reparent retry job \(though not in the reparenting code in the archive job itself\), a cycle in the sys\_archive\_related records causes infinite recursion. This can obstruct reparenting of other rules.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1833232

</td><td>

There's an incomplete 'NULLS FIRST' clause in multi-column indexes on new \(non-migrated\) RaptorDB instances

</td><td>

This means that all multicolumn indexes can't leverage their natural sort order.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1859194

</td><td>

Identified shadow tables containing 'my\_row\_id' as a primary key \(PK\) are causing PK mismatch with TableCloner

</td><td>

This issue was found in Xanadu instances. When a record is deleted from the table, an error can occur because it attempts to sync schema between the original table, and the shadow table can't alter the PK. This fix ensures the PK will be a 'sys\_id' on tables where 'sys\_id' is required.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Access

 PRB1881074

</td><td>

Provide introspection methods to get back the table/prefixes for views in the Genius Results returned from cypher2Results

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1784019

</td><td>

Un-offload is not preserving the attachment upload date and time for the record

</td><td>

The un-offloaded time of the attachment becomes the attachment's new upload time.

</td><td>

1.  Create an incident with two image attachments, audits, journals
2.  Offload the record to S3.
3.  Un-offload the record to ar\_ table.
4.  Restore the record and related records to S3.
5.  Verify the attachment's uploaded time.

 Expected behavior: The attachment's original upload time is preserved in the record.

 Actual behavior: The un-offloaded time becomes the attachment's upload time.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1859906

</td><td>

Investigating failing archive restore operation

</td><td>

This issue occurs in a Xanadu instance.

</td><td>

Run archive restore on the parent record.

 Notice that only a subset of archive related records in the original archive run are restored, and the transaction is showing high SQL counts and times.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1885210

</td><td>

Randomize the monthly/yearly physical table stats aggregator/gatherer scheduled jobs

</td><td>

The monthly and yearly jobs are randomized over the day instead of in-between an hour.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1706241

</td><td>

Table sys\_mutex has too many records

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1844798

</td><td>

Error message for unknown system variable 'sql\_generate\_invisible\_primary\_key' warning received

</td><td>

This issue was observed in a Xanadu instance.

</td><td>

1.  Open a Xanadu instance.
2.  Created a new table from sys\_db\_object\_list.do.

 Observe the warning error message, 'Unknown system variable 'sql\_generate\_invisible\_primary\_key''.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1881949

</td><td>

Fast lock aren't released if a Tx is cancelled

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Data Loss Prevention

 PRB1889727

</td><td>

Addition of Query ACLs in Data Loss Prevention

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Discovery

 PRB1657280

</td><td>

Inaccurate error logging for application patterns failed due to running processes that have bounced or stopped before pattern process detection executes

</td><td>

Commands using the PID and PORT from the ADM Probe will return null in the pattern failures. There's no log in the Discovery Log table of what occurred during process detection, and no indication in the failure message of the HD Log that the pattern failed due to the running process having bounced with a new PID or PORT.

</td><td>

1.  Ensure access to the target server running the Application instance.
2.  Run Discovery on the target server.
3.  Open the **Discovery Status** record.
4.  Wait for the Discovery to complete.
5.  Stop the service for the app running on the target server with **command sudo systemctl stop**after the ADM Probe ECC Queue Input is returned either.
6.  Open the ADM Probe ECC Queue Input record.
7.  Select the **Run Again**related link.
8.  Check the Discovery Status related list for Discovery Logs.
9.  Wait for the newest Pattern Log for the Application to return with an error for Failed Exploring Pattern.
10. Open the HD Log record.
11. Check the logging for why the Pattern Failed.
12. Check the Process Detection section before the Identification sections ran.

 Notice that commands executed that use the PID or the PORT discovered by the ADM Probe will return null, as they no longer exist on the target server, and there's no logging to the Discovery Log table of what occurred during Process Detection.

</td></tr><tr><td>

Discovery

 PRB1843083

</td><td>

Discovery monitoring job to search for future jobs before deciding to terminate a status

</td><td>

The monitoring job cancels the status even though the instance has a job for it but hasn't pick it up yet

</td><td>

1.  Have a status that is 'stuck' - input ECC queue in 'ready' state for more than 20mins.
2.  Have a record for that ECC queue in sys\_trigger table that is for the future.

 The job should cancel the status even though the instance has a job for it but didn't pick it up yet.

</td></tr><tr><td>

Discovery

 PRB1884527

 [KB2078932](https://hi.service-now.com/kb_view.do?sysparm_article=KB2078932)

</td><td>

A pattern on Agent Client Collector \(ACC\) requires MID specific configurations to the target device

</td><td>

When running a pattern on ACC, it requires the MID server to have discovery-specific port connectivity to the target instead of only using the ACC specific port.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1802663

</td><td>

A reference qualifier isn't applied for reference fields in the Agent Viewer experience

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1823462

</td><td>

Document Q&amp;A should skip .docx processing once it started using Document Reader Processing API

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1862011

</td><td>

Brief description shows a space in the General Details page

</td><td>

Fields are showing empty when referred, as the display name is empty.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1862455

</td><td>

An extraction flow throws an error for a use case that has only a field group

</td><td>

Users get an error message: 'java.lang.IllegalArgumentException: objectToMap: invalid type class com.snc.process\_flow.engine.serialization.GRProxy$1 for object property targetRecord \(sys\_script\_include.4a035a2beb771110f2549bf12a522841.script; line 530'.

</td><td>

1.  Create a use case with a target table.
2.  Create fields that have a field group.
3.  Create integration flows and activate them.
4.  Create a record in the target table.
5.  Test the extraction flow with the created document task.

 Observe the error message.

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881095

</td><td>

Add 'description' and 'autogenerated\_summary' to a task definition

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881127

</td><td>

Turn off the embedded image extraction option for PDFs and Docx

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881128

</td><td>

Introduce the docx4j library to Glide env

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881129

</td><td>

Fix 'fileId' null issue in Glide Java

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881130

</td><td>

In 'Chat with doc', classify if it's a scanned or digital PDF

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881131

</td><td>

Move Docx4j to 8.3.13 in Xanadu and Yokohama Now Assist

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881132

</td><td>

In Docx4j, create a scriptable extractText Java function which takes a docx file and gives an attachment ID for a text file

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881133

</td><td>

Support the .txt file format

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881134

</td><td>

Adding a PDF &gt; IMG null pointer exception to Xanadu and Yokohama Now Assist

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881135

</td><td>

Extract text and embedded images using Docx4j for docx and pdfbox for PDFs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881136

</td><td>

Glide API to convert a PDF to an image

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Document Intelligence Unified Backend

 PRB1881137

</td><td>

Fix the docx path for custom XML so extraction of the text is successful

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Elasticsearch Integration

 PRB1711742

</td><td>

Elastic index creation fails when clining from an instance with HA elastic search to non-HA

</td><td>

The user observes the error 'Failed to create surrounding logs' and all index creation fails.

</td><td>

1.  Request two instances with HLA \(one with HA Elastic and the other non-HA\).
2.  On startup, the surrounding logs index will be created.
3.  Clone the HA instance to a non-HA instance.

 On startup, observe the error 'Failed to create surrounding logs'. In general, all index creation fails.

</td></tr><tr><td>

Email Notifications

 PRB1887674

</td><td>

ERR does not work in Xanadu

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Embedded Help

 PRB1870178

</td><td>

The embedded help link redirects to the page 'not\_allowed.do' instead of the documentation site

</td><td>

The issue occurs in the Yokohama release.

</td><td>

1.  Open a Yokohama instance.
2.  Open the 'cmdb\_ci\_business\_app' or 'incident' table.
3.  In top right corner, select the **?**or the 'Show help' icon.
4.  Scroll down to link.
5.  Select the link.

 Expected behavior: Users are redirected to the documentation.

 Actual behavior: Users are redirected to the 'not\_allowed.do' page.

</td></tr><tr><td>

Employee Center

 PRB1809382

</td><td>

The hrm\_todos\_page list of tasks is incorrectly defined

</td><td>

To-do tasks from the hrm\_todos\_page list are not defined as list items, impacting the user's ability to navigate through the list.

</td><td>

1.  Navigate to **hrm\_todos\_page** for any user with to-do tasks assigned to them.
2.  Inspect each list item.

 Notice that they are not defined as list items.

</td></tr><tr><td>

Employee Center

 PRB1831309

</td><td>

Email returned from the HR Auto resolution test is missing some fields

</td><td>

Email script used in sysevent\_email\_template \(sn\_hr\_core\_case.ess.general\) is not present in Washington DC and Xanadu.

</td><td>

 

</td></tr><tr><td>

Employee Document Management

 PRB1877142

</td><td>

In Employee Document Management, UI actions cause performance impact to rendering search documents

</td><td>

In Employee Document Management, UI actions cause performance impact to rendering search documents or any list load on the sn\_hr\_ef\_ employee\_document table. The following UI actions are contributing to response times: Authorize, Reject, Authorize All, and Reject All. The number of records on the sn\_hr\_ef\_employee\_document is ~2.7 million.

</td><td>

1.  Ensure that Employee Document Management is set up on an instance and the number of records in sn\_hr\_ef\_employee\_document is ~2 million.
2.  Select the search documents module from the filter navigator.

 Notice that the page load times exceed 200 ms and often time out. Most of the time is spent on rendering the UI actions listed above \(~ 50 seconds each\).

</td></tr><tr><td>

Encryption

 PRB1854358

</td><td>

Protected script decryption fails for a cloned instance which is upgraded before the 'Protected Script Values Migration' job is executed

</td><td>

 

</td><td>

1.  Create a Xanadu/Yokohama instance.
2.  Create a 3des data.
3.  Clone the instance into other instance.
4.  After the clone is successful, verify the key exchange won't happen and the cm\_glide\_protected \_script\_encrypter module key isn't present in the instance.
5.  Upgrade the instance before the 'Protected Script Values Migration' job runs and keys are created.

 After an upgrade is successful, as the static key is removed and the key isn't available, protected script decryptions fail.

</td></tr><tr><td>

ESG Management

 PRB1889690

</td><td>

Addition of Query ACLs in ESG Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1786196

</td><td>

Prevent duplicate Impact hashes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1842971

</td><td>

Service Dashboard doesn't load due to a slow API

</td><td>

When there are many services \(~2 million\) on cmdb\_ci\_serice\_auto and cmdb\_ci\_service\_auto\_cache is empty, Service Dashboard doesn't load.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1884824

 [KB2082291](https://hi.service-now.com/kb_view.do?sysparm_article=KB2082291)

</td><td>

Tag-based groups can include alerts which don't match the tag-based alert clustering definitions tags

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1884862

</td><td>

Tag-based groups are not created, if there is an automatic group filter for automated groups

</td><td>

The alerts that are supposed to be grouped will not be grouped.

</td><td>

1.  Create a TAG definition or use a base instance definition.
2.  Create an automatic group filter for automated groups with something illogical so that the automated groups won't be created.
3.  Send at least two events that fit the definition.
4.  Wait for grouping job to run.
5.  Verify that alert exists in sa\_agg\_group\_alert\_staging table.

 Notice that alerts that should be grouped are not grouped.

</td></tr><tr><td>

Event Management

 PRB1886771

</td><td>

Alerts with the same CI metric name are not grouped together in the CMDB group if Automated alert grouping is disabled

</td><td>

When Automated \(ML based grouping\) is disabled, the CMDB group is not created for alerts with the same CI metric name.

</td><td>

1.  Disable Automated \(ML based\) alert grouping.
2.  Send two events with same CI metric name to create two alerts.

 Observe that CMDB group is not created.

</td></tr><tr><td>

Event Management

 PRB1889397

</td><td>

If there's an alert with its initial event generated time in the future, an alert isn't added to tag-based group or alerts are split into a different group

</td><td>

 

</td><td>

1.  Create a tag definition.
2.  Create several events, whose alerts may be grouped by tag according to the definition above.
3.  Create another event.
4.  Change via script the initial event generated time \(initial\_remote\_time\) to the future of the relevant alert.
5.  Create one more event and don't change the time. It should be added to the exiting group.

 All events should be in the staging table, but aren't.

</td></tr><tr><td>

External Triggers

 PRB1878365

</td><td>

Change sys IDs to readable values in GCF definitions of external triggers

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Field Service Quality Management

 PRB1860999

</td><td>

The dictionary override on wm\_task causes issues

</td><td>

In a Washington DC instance, there's no override attribute for the **State** field at the wm\_task. In the Xanadu, the override attribute is introduced for the **State** field at the wm\_task.

</td><td>

 

</td></tr><tr><td>

Finance Common Architecture

 PRB1891405

</td><td>

Addition of Query ACLs in Finance Common Architecture

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1867133

</td><td>

The 'Summarize' quick action gives a 'The current execution is in the waiting state' message

</td><td>

The flow caller is present. Async HTTP is used and that causes flows to go to a waiting state while waiting for the Async HTTP response. The 'The current execution is in the waiting state' exception is expected when Async HTTP is used.

</td><td>

1.  Log in to the instance as an admin.
2.  Navigate to ESC portal.
3.  Initiate a chat with LA.
4.  Log in as a user and accept the work item.
5.  Trigger the **Summarize** quick action.

 Expected behavior: The **Summarize** action should show the chat summary.

 Actual behavior: The quick action gives a 'The current execution is in the waiting state' message and an error in the sys\_log.

</td></tr><tr><td>

Flow Engine

 PRB1889723

</td><td>

Addition of Query ACLs in Flow Engine

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1762672

</td><td>

The base instance action **Create or Update Record** doesn't work for the reference type 'Template Values'

</td><td>

The caller should be replaced by 'System Admin' but instead it is empty.

</td><td>

1.  Create a subflow.
2.  Add one input of type 'Template Value.incident'.
3.  Add the action **Create or Update Record** as step 1 of the subflow.
4.  Map 'Fields' in the action with the **Subflow inputs** &gt; **Field** pill.

The table Name' is auto-populated with the 'Incident'.

5.  Select **Add field value**, add a Sys ID, and check the 'Determines uniqueness' box.
6.  Test the subflow, select **Caller** as 'System Admin' and **Run test**.
7.  Check the incident.

 Expected behavior: The caller should be replaced by 'System Admin'.

 Actual behavior: The caller is empty.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1794619

</td><td>

Reference values in 'Template' fields aren't properly stored

</td><td>

Certain values are not set.

</td><td>

1.  Create an action with a 'Template Value.incident' input.
2.  Add a 'Create' or 'Update' action step.
3.  Assign the action input to the fields of that action.
4.  Test the action, providing values for short\_description, description, and caller.

 Observe that 'Caller' does not get set.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1834406

</td><td>

App installation deletes base instance sys\_complex\_object 'FDCollection'

</td><td>

Deleting the flow does not remove the sys\_complex\_object record from the source instance, but the app installation removed the record from the target instance. Sys\_complext\_object is not listed in the application file of the app, but appears in the payload of the sys\_hub\_flow record.

</td><td>

1.  Hop onto any base instance.
2.  Create a scoped app.
3.  Create a flow \(sys\_hub\_flow\) with some actions, such as log.
4.  Confirm the sys\_id is being included in the flow.
5.  Check the payload of the captured flow from sys\_update\_xml.
6.  Delete the flow from the list view of sys\_hub\_flow.
7.  Confirm the deletion is captured in sys\_metadata\_delete.
8.  Publish the scoped app to a repo or app store.
9.  Install the app from another instance from the app store.

 Notice that after the installation, the base instance sys\_complex\_object removes a sys\_id on the instance.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1865407

</td><td>

Mismatching data on an action instance can cause issues with flow execution

</td><td>

Actions don't perform as expected in various ways.

</td><td>

 

</td></tr><tr><td>

Form Builder

 PRB1836580

</td><td>

Selecting 'Edit in Original Scope' from the Form Builder banner enables the override properties of the field for editing

</td><td>

When a field is inherited from a parent table, it has the ability to override field properties. Previously, override properties were controlled by isFormReadOnly. However, with this PR update, the implementation has been refined how readability is determined.

</td><td>

 

</td></tr><tr><td>

Form Controller

 PRB1876936

</td><td>

GFORM\#ADD\_DECORATION isn't working in forms workspace like in they are in UI16 as g\_form.addDecoration

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC: Advanced Audit

 PRB1890961

</td><td>

Addition of Query ACLs in GRC: Advanced Audit

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Advanced Core

 PRB1890960

</td><td>

Addition of Query ACLs in GRC: Advanced Core

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Business Continuity Planning

 PRB1894009

</td><td>

Query match error for BCM planner persona to access sn\_bcp\_plan\_asset table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

GRC: Continuous Authorization and Monitoring

 PRB1890964

</td><td>

Addition of Query ACLs in GRC: Continuous Authorization and Monitoring

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Metrics

 PRB1891392

</td><td>

Addition of Query ACLs in GRC: Metrics

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Operational Resillience

 PRB1889673

</td><td>

Addition of Query ACLs in GRC: Operational Resillience

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Privacy Management

 PRB1890889

</td><td>

Addition of Query ACLs in GRC: Privacy Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Profiles

 PRB1889683

</td><td>

Addition of Query ACLs in GRC: Profiles

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Regulatory Change Management

 PRB1890993

</td><td>

Addition of Query ACLs in GRC: Regulatory Change Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

GRC: Vendor Portal

 PRB1889689

</td><td>

Addition of Query ACLs in GRC: Vendor Portal

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Healthcare and Life Sciences Service Management Core

 PRB1889704

</td><td>

Addition of Query ACLs in Healthcare and Life Sciences Service Management Core

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Hermes \(Family\)

 PRB1833479

</td><td>

Upgrade a fix by removing previous sys\_choice records for the 'Application Id' list

</td><td>

In Washington DC, a release application ID was originally configured as a list that relied on sys\_choice list. In the later releases, this was changed to be a drop-drown that relied a new table that defined the configured applications which are associated to its respective Hermes service.

</td><td>

1.  Configure an instance on a Washington DC release.
2.  Note the sys\_choice list entries for 'Application ID'.
3.  Upgrade the instance to.

 Notice that the 'Application ID' list uses the reference table, but the sys\_choice\_list entries still exist on the instance, but they aren't used.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1846241

</td><td>

The Hermes metrics dashboard displays data off by 1

</td><td>

 

</td><td>

1.  Open an instance with data in the hermes\_usage\_metrics table.
2.  Switch the preference timezone to GMT in preference settings.
3.  Compare the data points on the graph vs the table.

 Expected behavior: It shows the same date as the table.

 Actual behavior: The date is one day behind.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1847005

</td><td>

The 'Hermes Metric Aggregation' job is joining dates together due to a job skew

</td><td>

The job should be moved further into the day with the GMT timezone to avoid a skew. Also, add limits so that the aggregation is only picking updates of the previous day's start and end and not have it depend on when the job is run. There should be similar limits for clean-up jobs and monthly aggregation.

</td><td>

1.  Have an instance with Hermes installed.
2.  Create a topic and produce and consume it.
3.  Verify usage metrics are logged every one hour.

 The next day, verify that all hourly metrics are aggregated to the daily metrics of the previous day and that hourly metrics are clear.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1856021

</td><td>

Data in throughput shown on hermes\_usage\_metrics when producing data in inconsistent patterns

</td><td>

Inaccuracies in 'Total MB Value Per Hour' when data flows in an inconsistent pattern. When producing data at a relatively constant rate, hermes\_usage\_metrics values closely matched the actual value, but when producing data in large spikes, the values in hermes\_usage\_metrics are significantly above or below the actual value.

</td><td>

1.  Set up Kafka producer on a local machine using Kafka Java APIs.
2.  Produce a large batch of messages.
3.  Wait until the hourly aggregation job runs to populate hermes\_usage\_metrics.
4.  Check the corresponding value in 'Total MB Value Per Hour'.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1876312

</td><td>

There's a missing call to refresh clients when clusters are removed

</td><td>

When clusters are removed during a 'Retire' request, the deletion should also refresh the clients. A recently added function was missing that refresh call.

</td><td>

 

</td></tr><tr><td>

History Set

 PRB1844946

 [KB1923828](https://hi.service-now.com/kb_view.do?sysparm_article=KB1923828)

</td><td>

Intermittent duplicate comments in activity stream due to sys\_email records

</td><td>

Some comments are duplicated due to the presence of sys\_email records. This duplication occurs when a comment is added in a way that causes the incident's sys\_updated\_on timestamp to be one second earlier than the corresponding sys\_journal\_field record. If emails are triggered by the incident update, the loading of sys\_email records within the related sys\_history\_set interferes with the **last\_update\_recorded** field in sys\_history\_set. This disruption ultimately results in the duplication of the comment whenever the next update to the incident occurs.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Horizon Component Library

 PRB1881075

</td><td>

HDS net new components: animated carousel and animated button

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

HR Service Delivery

 PRB1805904

 [KB1702845](https://hi.service-now.com/kb_view.do?sysparm_article=KB1702845)

</td><td>

Field ACLs on the 'Interaction' table in the 'Advanced Work Assignment for HRSM' application scope aren't present on the instance

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery

 PRB1817290

</td><td>

HTML is stripped when using 'Copy to Clipboard' on the Response Template

</td><td>

HTML formatting is not applied. However, when the Response body is copied from the response template configuration and pasted into the Email body, the formatting is applied.

</td><td>

1.  Open any Response Template.
2.  Modify the HTML text and add some formatting, for example, make a word or sentence in bold.
3.  Save the Response template.
4.  Navigate to HR Agent workspace.
5.  Open an HR case where the response template is available.
6.  Select **Compose Email**.
7.  Select the response template and use 'Copy to Clipboard'.
8.  Paste it on the email body.

 Notice that the HTML formatting is not applied.

</td></tr><tr><td>

HR Service Delivery

 PRB1831301

</td><td>

Renaming an attachment isn't working for an agent

</td><td>

 

</td><td>

1.  Provision an instance with sn\_hr\_agent\_ws 3.3.1/4.0.0-SNAPSHOT installed.
2.  Log in as an agent.
3.  Open an HR case in HR Agent Workspace.
4.  Attach a document in the attachments side panel.
5.  Try to rename it.

 Observe that the attachment isn't renamed.

</td></tr><tr><td>

HR Service Delivery

 PRB1889709

</td><td>

Addition of Query ACLs in HR Service Delivery

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Identity

 PRB1889721

</td><td>

Addition of Query ACLs in Identity

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Incident Communications Management

 PRB1849039

</td><td>

Update the email client template from the mail script

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Incident Communications Management

 PRB1849469

</td><td>

Filter Major Incident Management \(MIM\) email templates in MIM Comm based on a template condition in Classic

</td><td>

MIM templates follow a reference qualifier and don't respect conditions set within the templates.

</td><td>

1.  Open major incident in Service Operations Workspace.
2.  Select the 'Communicate' tab.
3.  Select the **Compose** button on a communication plan.

 Expected behavior: A user can all see all templates

 Actual behavior: Based on a condition within the templates, filtering should be applied. It currently follows the reference qualifier.

</td></tr><tr><td>

Incident Communications Management

 PRB1860756

</td><td>

Resolving variables isn't working in UI16

</td><td>

 

</td><td>

1.  Install com.snc.incident.mim and sn\_itsm\_gen\_ai plugins.
2.  Open any major incident communication plan from UI16.
3.  Select **Compose**.

 Expected behavior: The email should display as per the variables defined under the email client template.

 Actual behavior: No email is displayed in UI16.

</td></tr><tr><td>

Instance Data Replication \(IDR\)

 PRB1885869

</td><td>

Legacy IDR jobs flod the logs with error messages when they can't reach Kafka via bootstrap

</td><td>

There are some scheduled jobs that are created when legacy IDR is installed and are scheduled to run frequently by design. When the cluster isn't reachable, these scheduled jobs write errors to the log each time, which happens once every few seconds. When IDR v2 is used \(all new sets created in Washington DC and later\), there's a new set of scheduled jobs that are used and continue to work when the infrastructure for legacy IDR is turned off. However, the jobs intended for legacy IDR aren't automatically turned off when all sets have been migrated to v2.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1857020

</td><td>

A Remote Process Synch \(RPS\) outbound job can go into a loop if there's an error parsing the XML

</td><td>

There should be a message in the log for the Outbound Queue Job for the state table with the state error.

</td><td>

1.  Set up RPS with outbound on incident that captures a short\_description.
2.  Create an incident that meets the capture criteria with the short\_description.
3.  Set the contents of the file so that 'invlid\_short\_description.txt' is inside the attached zip file.

 Notice that the entry is not processing and there is no error record in the Outbound Queue.

</td></tr><tr><td>

Integration Hub Remote Process Sync

 PRB1874002

</td><td>

Remote Process Sync \(RPS\) is triggered by changes from non-captured fields

</td><td>

RPS captures changes to a record when any changes are made to the fields selected by the user as part of the CDC Definition \(change data capture\). Even though changes are being made to fields that are not part of the CDC Definition, RPS still captures these changes.

</td><td>

1.  Set up RPS.
2.  Create a record that syncs.
3.  Modify a field on that record that isn't part of the CDC Definition.

 Observe that this creates an update record on cdc\_queue\_ih, which should not be created.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1792500

 [KB2164143](https://hi.service-now.com/kb_view.do?sysparm_article=KB2164143)

</td><td>

The u\_crypto\_specification\_list reference qualifier condition is not updated upon upgrade

</td><td>

An incorrect reference qualifier in the sys\_dictionary record for sys\_kmf\_resource\_exchange\_request.u\_crypto\_specification\_list causes issues with key exchanges after clones or 'restore from backup' automations.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1847472

</td><td>

Fix the matching of the Bagheera configuration database URL with the cached database URL

</td><td>

App nodes compete in a vicious loop to update this database property to match with their mismatched cached property, which is affecting the instance's performance.

</td><td>

1.  Run AHA 3.0 on any instance utilizing Bagheera.
2.  Run AHA Transfer/ Failover.
3.  Notice the logs on the nodes after a successful transfer or failover.

 Expected behavior: The glide.db.url from cache should match with the file property glide.db.url.

 Actual behavior: The cached GlideProperties database URL does not match the file property glide.db.url.

</td></tr><tr><td>

Key Management Framework \(KMF\)

 PRB1854256

</td><td>

Legacy SEK rekey fails due to the password2 field size not being large enough

</td><td>

Instance rekey use sys\_dictionary.max\_length for field size detection, leading to rekey failure.

</td><td>

1.  Provision an instance.
2.  Populate the oauth\_credential. token\_received with a large value.
3.  Clone the instance from step 1.

 Expected behavior: Legacy SEK rekey completes successfully.

 Actual behavior: Legacy SEK complains that the field isn't large enough.

</td></tr><tr><td>

Knowledge Management

 PRB1864356

</td><td>

When displaying a KB article, the breadcrumb must contain the article title

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Open the KB portal.
3.  Open any article.

 Observe that the breadcrumb doesn't have the name of the article.

</td></tr><tr><td>

KPI Details

 PRB1813576

</td><td>

Issues with the KPI Details' 'On View &gt; select' query

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Language and Translations

 PRB1870970

</td><td>

Translations Merge for the GenAI translation update

</td><td>

Standard translations merge process for the GenAI translation update and StoreApps SP2 translation update.

</td><td>

 

</td></tr><tr><td>

Lifecycle Events

 PRB1830703

</td><td>

Base instance account notification workflow issue for Onboarding Lifecycle event

</td><td>

Account notifications are sent only occasionally for New Hire cases, when they should always be sent to the user when triggered.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1808314

</td><td>

The user is unable to personalize list columns for Oracle DB instances

</td><td>

A related list renders with old columns.

</td><td>

1.  Log in to Oracle DB Instance as Admin User.
2.  Open an incident on SOW Workspace.
3.  Select **Related records**.
4.  Select any of the related lists \(for example, Task SLAs\).
5.  Select the gear icon and **Edit Column**.
6.  Select some new columns and select **Ok**.

 Expected behavior: The related list should render with new columns.

 Actual behavior: The related list renders with old columns.

</td></tr><tr><td>

List Administration

 PRB1810106

</td><td>

'Opened by' different states are overridden with the latest state value

</td><td>

When a new 'Opened by' timestamp is created, the **State** field is changed and overrides the previous state value.

</td><td>

1.  Open the UI Builder.
2.  Add the **List page** template.
3.  Select **Incidents** &gt; **All**.
4.  Apply a filter matching Priority 4.
5.  Load the URL.

Notice that in output 1, a new 'Opened by' timestamp is created with the Priority 4 filter.

6.  Apply a filter matching the **State** field.
7.  Load the URL.

Notice that in output 2, a new 'Opened by' timestamp is created with the Priority 4 filter and the **State** field is changed.

8.  Navigate to the list containing output 1.

 Expected behavior: A new 'Opened by' timestamp is created with the Priority 4 filter.

 Actual behavior: A new 'Opened by' timestamp is created with the Priority 4 filter and **State** field changes, and the previous state values are overridden.

</td></tr><tr><td>

List Administration

 PRB1835599

</td><td>

The 'Records per page' setting is not permanent

</td><td>

'Records per page' on any list in SOW reverts when the page is refreshed.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1894601

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for Listcount

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1894614

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for GlideAggregate

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1894616

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for Related Lists

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Column Sort

 PRB1782504

</td><td>

Sorting of any column is not retained after refreshing a page in Xanadu

</td><td>

The sorted column is not retained.

</td><td>

1.  Navigate to UI builder, create a new experience and create new page.
2.  Add a record list component.
3.  Change the table name to Incident from List controller.
4.  Open the page in new tab.
5.  Sort any column
6.  Refresh the page.

 Observe that the sorted column is not retained.

</td></tr><tr><td>

List Controller

 PRB1872717

</td><td>

When the user ceates a new My List and edits the columns, the list does not show personalized columns until the page is refreshed

</td><td>

 

</td><td>

 

</td></tr><tr><td>

List Filters

 PRB1801767

</td><td>

Japanese names cannot be filtered by a Japanese term but can be filtered by an English term under the Japanese setting

</td><td>

Unable to filter lists by Translated Text fields in non-English languages when using the non-English translation

</td><td>

 

</td></tr><tr><td>

List Views

 PRB1854405

</td><td>

The Xanadu Date Picker Calendar pop-up appears below the field, making it difficult to select other dates

</td><td>

The Xanadu Date Picker Calendar opens on the below field and isn't letting users select other dates when they add a variable editor on the form configuration.

</td><td>

1.  Navigate to a Xanadu instance.
2.  Navigate to incident.LIST.
3.  Add a variable section.
4.  Add an incident variable editor to the form.
5.  Navigate to the TASK SLA related list.
6.  Select the **Start time** field.

 Notice that the calendar pop-up appears below the field, making it difficult to select other dates. The date picker should open above the field.

</td></tr><tr><td>

List Views

 PRB1865826

</td><td>

Multi-select not working in the Certification Review page for data certification

</td><td>

This issue occurs in Washington DC, Xanadu, and Yokohama. In the 'Review Completed' and 'Review not completed' lists, selecting the **Select all** button and the message 'Select all x item from the list' from one list selects all the records in the other list as well.

</td><td>

1.  Select **All x item** from the list not working properly on Xanadu and Yokohama.
2.  Open any certification task in Yokohama.
3.  Certify or fail some records.
4.  Navigate to the 'Review Completed' tab.
5.  **Check** the **Select all** box.
6.  Select the 'Select all X item from the list' message.
7.  Navigate to the 'Review not completed' tab.

Notice all records from the review that are not completed are also selected.


 Expected behavior: Only the selected records in should be in the 'Review completed' tab.

 Actual behavior: Notice that records from the 'Review not completed' tab are also in the 'Review completed' tab.

</td></tr><tr><td>

Major Incident Management

 PRB1757151

</td><td>

Base instance list control on the Affected CI related list throws an error in the syslog when incidents are accessed on the mobile app

</td><td>

An error is thrown with the following warning when any user opens an incident record while accessing the instance through the browser on a mobile device.

</td><td>

1.  Open an instance.
2.  Log in to the instance.
3.  Navigate to any available incident.
4.  Switch to desktop view.
5.  Navigate to **syslog.list**.

 Observe the error in the logs.

</td></tr><tr><td>

MID Server

 PRB1864193

</td><td>

Upgrading a Linux MID Server to Xanadu reverts mid.shconf\_override to the default setting

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1883251

</td><td>

Block Mobile Attachment Sharing property for Mobile doesn't support exemption based on user roles

</td><td>

Changing the property glide.sg.block\_mobile\_attachment\_sharing from 'false' to 'true' should exempt some users based on their roles for the security property.

</td><td>

1.  Navigate to **sys\_properties.list**.
2.  Change the property glide.sg.block\_mobile\_attachment\_sharing from 'false' to 'true'.

 Notice that this applies to all users, when only some users require the ability to download or view attachments on Mobile based on their role.

</td></tr><tr><td>

Mobile Virtual Agent

 PRB1881114

</td><td>

Mobile NASS GenAI visual uplift

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1690651

</td><td>

Zing Exact Match search on workspaces intermittently navigates to an incorrect URL in Next Experience

</td><td>

Zing Exact Match search opens the record in record view instead of kb\_view.

</td><td>

1.  Log in to an instance in incognito mode.
2.  Ensure Next Experience is enabled.
3.  Ensure global and workspace searches are using zing.
4.  Select **Service Operations Workspace** in the search context.
5.  Perform an exact match search for KB0000001.

Notice that it should open the record in kb\_view.

6.  Wait for 5 to 10 minutes.
7.  Repeat the steps.

 Observe that the record opens in record view.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1785796

</td><td>

Keyboard focuses on a non-interactive Profile icon in User Menu

</td><td>

Keyboard focus should not go to non-interactive Profile icon in User Menu as this icon do not have any action on it.

</td><td>

1.  Open any base instance \(impersonate or login with system administrator\) in Chrome browser of Windows machine.
2.  Navigate to the **User menu** button present at top right corner of the page using the Tab key.
3.  Expand the menu using the Enter / Return key.
4.  Press the Tab key again.

Notice that the focus moves to the profile icon and a tool-tip with user's name pops up.

5.  Use the Enter key on this icon to see if there is any action available on this interactive control.

 Observe that the keyboard focuses on the non-interactive Profile icon in User Menu.

</td></tr><tr><td>

On-Call Scheduling

 PRB1823075

</td><td>

Daily rotation is skipped on DST start dates

</td><td>

 

</td><td>

1.  Log in as admin.
2.  Navigate to create/edit schedule.
3.  Create a shift: 03-11-2024 02:00:00 to 04-11-2024 20:00:00, Mon, Wed, Fri.
4.  Add Primary - 1 week, Secondary - 1 daily.
5.  Publish the shift.

 Observe the secondary roster data in March and notice that daily rotation is skipped from March.

</td></tr><tr><td>

On-Call Scheduling

 PRB1880894

</td><td>

On-call scheduling is randomly skipping one person for every rotation cycle

</td><td>

.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1886730

</td><td>

The 'On-call Who' API intermittently isn't returning users

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Opportunity Management

 PRB1889707

</td><td>

Addition of Query ACLs in Opportunity Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Oracle Reconciliation

 PRB1794653

</td><td>

The Oracle licenses required value set hits the max integer limit

</td><td>

The issue occurs due to a datatype mismatch during reconciliation calculations. One of the values is returned as a string instead of an integer, resulting in concatenation of values instead of aggregation. This causes the licenses required value to hit max integer limit.

</td><td>

 

</td></tr><tr><td>

Outsourced Customer Service

 PRB1889693

</td><td>

Addition of Query ACLs in Outsourced Customer Service

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1817989

</td><td>

The 'Daily Data Collection' job takes longer after upgrading to Xanadu

</td><td>

When the user runs the data collection job, they notice that the logs contain 'Processed ∞% \(8\) records'.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1889720

</td><td>

Addition of Query ACLs in Analytics Hub

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Performance Analytics

 PRB1890020

</td><td>

Addition of Query ACLs in Analytics Hub

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Component API

 PRB1783660

</td><td>

A search isn't giving the expected results when the user language is set to non-English

</td><td>

The localization of the title of 'Visualisations' is also not working.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1807150

</td><td>

If a dashboard has no creator in the ACLs, there is a null pointer exception

</td><td>

If the **Owner** field of a dashboard is empty or the owner is no longer an active user \(for example, they have left the company\), an error is thrown when trying to update the dashboard.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Migration API

 PRB1820684

</td><td>

Some legacy dashboard widgets don't render

</td><td>

Legacy dashboard widgets don't render after the dashboard has been migrated to Platform Analytics and setting sys\_property glide.ui.choices.show\_missing to 'false'.

</td><td>

1.  Navigate to **sys\_widgets**.
2.  Open the 'Filters' record.
3.  Check **Active**.
4.  Save the record.
5.  Create a new dashboard.
6.  Navigate to the **Add Widgets icon** &gt; **Widget Category** &gt; **Filters**.
7.  Add the record previously created to the dashboard.
8.  Migrate the dashboard to Platform Analytics.
9.  Open the migrated dashboard.
10. Observe the legacy widget loads.
11. Set sys\_property glide.ui.choices.show\_missing to 'false'.
12. Refresh the migrated dashboard.

 Notice that now it will not render the legacy widget, and will only show \{\}.

</td></tr><tr><td>

Playbook Experience Core

 PRB1841873

</td><td>

Slowness within Playbook activities when there are a large number of stages and activities

</td><td>

This issue within the Playbook activities occurs when large number of stages and activities, such as 100 to 200 activities, have condition to run on the lanes and activities.

</td><td>

1.  Create a playbook process with a large number of stages and activities.
2.  Attempt to progress through the playbook in the workspace or playbook preview.

 Notice the slowness increases as the number of stages and activities grow.

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1861646

</td><td>

The questionnaire order isn't synchronized in update\_set or persisted when duplicating a Playbook

</td><td>

The order of questions in the Questionnaire Activity should persist in a duplicated playbook.

</td><td>

1.  Create a new Playbook with a Questionnaire Activity.
2.  Add three questions.
3.  Select **Save**.
4.  Duplicate the playbook.

 Expected behavior: The order of questions persists in the duplicated playbook.

 Actual behavior: The order of questions is not persisted in the duplicated playbook.

</td></tr><tr><td>

Policy and Compliance Management

 PRB1889692

</td><td>

Addition of Query ACLs in Policy and Compliance Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Portfolio Management

 PRB1889736

</td><td>

Addition of Query ACLs in Portfolio Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Portfolio Management

 PRB1889740

</td><td>

Addition of Query ACLs in Portfolio Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1832015

</td><td>

The training failed because the solution has a table as an input field, but the platform\_ml\_read role is missing from the input table

</td><td>

This issue occurs because the scheduler worker is logged in with a user that has the platform\_ml\_read role. If this role is missing from the table, the scheduler worker is unable to read the table data, causing the training to fail.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1873662

</td><td>

Add support for top number of classes, minute records per class, and removing ServiceNow Machine Learning others as advanced parameters in Classification solution

</td><td>

The ability to apply these advanced parameters.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1879961

</td><td>

Two emails are sent for clustering when triggered from Process Mining

</td><td>

When RCA/Clustering is triggered from the process mining workspace, two emails are sent when only one email should be sent. Since the RCA or Clustering feature internally uses the show records, two ml\_solutions are created, and the system identifies both of them as separate entities, causing it to send two emails.

</td><td>

 

</td></tr><tr><td>

Predictive Intelligence

 PRB1885952

</td><td>

Incorrect use of current.update\(\) in a base instance business rule

</td><td>

The script run by the BR includes a current.update\(\) call without setworkflow call to disable other BRs.

</td><td>

 

</td></tr><tr><td>

Problem Management

 PRB1762651

</td><td>

PMMU \(Physical Memory Management Unit\) issues found during London to Xanadu upgrade testing

</td><td>

There are several issues. There's incorrect code and problem models for customizations. The demo data needs to be remapped. There's an outdated info message. The **Next** button doesn't appear until reloading when requesting to activate a plugin. Some of the problems and problem tasks failed to migrate. The 'Problem overview' dashboard should not be deleted on upgrading.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1870032

</td><td>

Uppercase and lowercase sys\_ids for the same record break mining

</td><td>

A script changes the document ID in sys\_audit for records so that some document ID values are uppercase and lowercase.

</td><td>

 

</td></tr><tr><td>

Process Mining

 PRB1889675

</td><td>

Addition of Query ACLs in Process Mining

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1859066

</td><td>

Resource Assignment \(RA\) is associated to a new Resource Plan upon migration

</td><td>

The resource plan associated with an RA is in the 'Completed' state. When the effort value is updated, a new resource place is created and attaches the RA to the new resource plan. A new plan shouldn't be created, and the resource assignment should be pointing to the initial completed resource plan.

</td><td>

1.  Create a resource plan.
2.  Allocate it.
3.  Complete the plan.
4.  Migrate the plan to resource assignment.

 Notice that upon migrating the plan, the newly created resource assignment will be linked to the completed resource plan; when attempting to change the effort type on the resource assignment record, a new resource plan with an allocated state is created.

</td></tr><tr><td>

Project Management

 PRB1889859

</td><td>

Actuals for planning item are not rolled up to the task type breakdown

</td><td>

Enable actual costs from expense lines to rollup to the 'Actual cost' on associated cost plans related to planning items without the core table integration. When user creates a new expense line for a planning item in the 'New financials' page for a planning item, the actual cost value on the cost plan breakdown should add up to the total amount from processed expense lines.

</td><td>

1.  Create a planning item without integrations.
2.  Add cost plans and expense lines.
3.  Validate the actual roll up to task type breakdown.
4.  Validate the roll up to investment entity.

 Notice that actuals for planning item are not rolled up to the task type breakdown.

</td></tr><tr><td>

Reporting

 PRB1853349

</td><td>

Visualizations in non-global domains aren't displayed in the list of visualizations

</td><td>

When trying to add a dashboard to a library, it's not saved in any sub domains. It's saved only in the global domain. In the sub domains, when they try to save the dashboard, it says it's saved but it's not.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1860646

</td><td>

A top task isn't updated for existing resource assignments when a project is made or removed from being a child of another project

</td><td>

When a project that has an existing resource assignment is added to another project as a child project the top task of the resource assignment isn't being updated. Additionally, when a project with an existing resource is removed from being a child of another project, the top task of the resource assignment isn't being updated.

</td><td>

 

</td></tr><tr><td>

Resource Management

 PRB1877603

</td><td>

In Resource Management Workspace, there's a NullPointer exception

</td><td>

In Resource Management Workspace, users get nullpointer exception when changing resource status for an allocation.

</td><td>

1.  Open Resource Management Workspace.
2.  Open a card.
3.  Change the status of the assignments for a user.

 Observe the null pointer exception.

</td></tr><tr><td>

Rollback and Recovery

 PRB1809473

</td><td>

When truncating a logical non-root table in TPH or TPP, all records are stored for ancestors and siblings in a shadow table

</td><td>

 

</td><td>

1.  Create two tables using the 'Table Per Hierarchy' extension model \(u\_table1 and u\_table2 extending the former\).
2.  Seed some test data on each tables.
3.  Invoke 'DBI.tableDrop\(\)' for u\_table2 with rollback enabled.
4.  Confirm that records from u\_table1 were recorded in the shadow table 'sh$u\_table1'.

 That shadow table should only have records for u\_table2 since those are the ones that were deleted and therefore the only ones that could be restored by rolling back the truncate of the logical table 'u\_table2'. This can become a costly, unnecessary operation if the parent table is large.

</td></tr><tr><td>

SaaS integration with Office 365 \(Glide\)

 PRB1784710

</td><td>

Potential savings calculation at the LMR level for bulk reclamation candidates

</td><td>

In SAM license workbench, potential savings for Microsoft shows 0 when it has removal candidates with potential saving values greater than 0.

</td><td>

 

</td></tr><tr><td>

Schedule Optimization

 PRB1875270

</td><td>

Prevent the fallback of retrieving the schedule from the sys\_user record when there's no schedule in the 'Agent schedule' table

</td><td>

Remove the 'Agent schedule' but add a schedule to the sys\_user record. The agent shouldn't be returned in the getQualifierData response. Add the 'Agent schedule' only, it should be returned in the getQualifierData response.

</td><td>

1.  Enable a territory model.
2.  For the qualifying agent, verify that no schedule is present in cmn\_schedule.
3.  Add a schedule at the agent level in the sys\_user record.
4.  Create SO batch with the 'Territory' qualifier.
5.  Perform Graph QL for agents.

 Expected behavior: No schedule should be returned.

 Actual behavior: A schedule from the sys\_user record is returned.

</td></tr><tr><td>

Security Customer Actions

 PRB1873948

</td><td>

Steps can't be re-opened for a completed action due to Playbook archiving

</td><td>

The user is not able to re-open the step to continue working on it again.

</td><td>

1.  Open a Xanadu instance.
2.  Navigate to **Security Center** &gt; **Customer Actions \(Critical Updates\)**.
3.  Complete the **Enable 3DES deprecation for Password2 Fields** action.
4.  Wait 14 days on the instance to allow for playbook archiving.
5.  Navigate to the completed **Enable 3DES deprecation for Password2 Fields** action.
6.  Navigate to **Steps**.
7.  Select one of the steps.

 Expected behavior: The user is able to re-open a step by using the **Restart** button to proceed working on it again.

 Actual behavior: The user is not able to re-open the step.

</td></tr><tr><td>

Server-side scripts

 PRB1808973

</td><td>

Turn On ECMAScript 2021 \(ES12\) mode is not toggled in certain scenarios

</td><td>

Turn On ECMAScript 2021 \(ES12\) mode is toggled off after zbooting an instance.

</td><td>

1.  Unload a sys\_script\_include XML with Turn On ECMAScript 2021 \(ES12\) mode toggled.
2.  Make sure sys\_es\_latest\_script=true.
3.  Save it to the repository.
4.  Zboot the instance.
5.  Check the record.

 Expected behavior: Turn On ECMAScript 2021 \(ES12\) mode is on.

 Actual behavior: Turn On ECMAScript 2021 \(ES12\) mode is off.

</td></tr><tr><td>

Server-side scripts

 PRB1848232

</td><td>

TD instance gets hung up and unresponsive due to recursive calls while capturing Generic Collection Framework \(GCF\) metics

</td><td>

While publishing the GCF metrics for scripts, MInMaxPriorityQueue is used for collecting 20 longest executions. It attempts to access indexes more than 20, causing ArrayIndexOutofBound exceptions.

</td><td>

 

</td></tr><tr><td>

Server-side scripts

 PRB1883239

</td><td>

ESLatestScriptLoader returns a warning message

</td><td>

The message reads, 'Version loading was stopped by ESLatestScriptLoader for sys\_es\_latest\_script...'.

</td><td>

 

</td></tr><tr><td>

Service Catalog Builder

 PRB1756914

</td><td>

Modifying the catalog item task step through builder doesn't work as expected

</td><td>

Modifying the catalog item task step through catalog builder in the scoped application doesn't capture the 'Update name' in the application files of the scoped app.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1835397

</td><td>

Users are unable to clear a value on a date type question from a client script/UI Policy

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Level Management

 PRB1843470

 [KB1777517](https://hi.service-now.com/kb_view.do?sysparm_article=KB1777517)

</td><td>

SLA engine reset condition may fail in certain circumstances

</td><td>

SLA Engine reset condition fails if the advanced conditions changes, changesFrom or changesTo are used in conjunction with the table in com.snc.sla.get\_ task\_from\_db and the walker is CHECKPOINT.

</td><td>

1.  Create an SLA Definition on the table sc\_req\_item:
    1.  start condition active=true
    2.  stop condition active=false
    3.  reset condition due\_date changes \(advanced condition\)
2.  Check that the property com.snc.sla.get\_task\_from\_db contains sc\_req\_item.
3.  Check that property com.snc.walker.default=CHECKPOINT.
4.  Update any value on an existing sc\_req\_item or create one and verify task\_sla is created for SLA Definition created in \#1.
5.  Update the **due\_date** field to anything if it is empty or change it to any value if it has a value.

 Expected behavior: task\_sla is canceled and new task\_sla is created.

 Actual behavior: task\_sla isn't canceled. The error log contains 'CheckpointHistoryWalker does not support walk to update: \#'.

</td></tr><tr><td>

Service Level Management

 PRB1849627

</td><td>

Improve SLA Calculator's handling of very large sets of Task SLA records during trigger processing

</td><td>

Under certain circumstances, bulk SLA calculations can cause node memory issues if the set of Task SLAs being calculated is very large.

</td><td>

1.  Open the script include SLACalculatorNG.
2.  Look at the function SLACalculatorNG.calculateSLArange.

 Note that it first processes the list of Task SLA and adds them to an array. This is consumes memory unnecessarily.

</td></tr><tr><td>

ServiceNow IDE \(Family Release\)

 PRB1878154

</td><td>

A sync notification appears after deploying an app

</td><td>

The sync mechanism should detect changes from sys\_update\_xml by default.

</td><td>

1.  Create an app.
2.  Create a Table\(\{\}\) using Fluent in index.now.ts.
3.  Deploy the app.

 Expected behavior: Changes made by Fluent shouldn't trigger a sync.

 Actual behavior: A sync notification appears immediately after deploying even though it was the user's changes that were deployed.

</td></tr><tr><td>

ServiceNow IDE \(Family Release\)

 PRB1878166

</td><td>

Integrated development environment \(IDE\) source files should not be deleted using a business rule on sys\_app table

</td><td>

This business rule is triggered on every delete action for a sys\_app. All associated IDE source files could potentially be deleted unintentionally from the instance, which is irreversible.

</td><td>

1.  Provision a ServiceNow Instance with ServiceNow IDE 2.0.4 installed.
2.  Bump IDE to 2.1.0.
3.  Create an app in Service Now IDE.
4.  Build and deploy the newly created app.

Observe all the source files being shown in IDE.

5.  Navigate to the sys\_app record.
6.  Delete the sys\_app record.

 Expected: ServiceNow IDE should not show any source files when app is deleted.

 Actual: A purge occurs due to a business rule.

</td></tr><tr><td>

Service Portal

 PRB1502280

 [KB0994649](https://hi.service-now.com/kb_view.do?sysparm_article=KB0994649)

</td><td>

The file attachment field does not appear on portal form page

</td><td>

The file attachment field **My file** doesn't appear on the form page of the incident record.

</td><td>

1.  Log in as an admin user.
2.  Open the form page of the incident record.

 Notice that the file attachment field **My file** doesn't appear on portal, but shows in native view.

</td></tr><tr><td>

Service Portal

 PRB1839297

 [KB1925168](https://hi.service-now.com/kb_view.do?sysparm_article=KB1925168)

</td><td>

SPEntry page error 'Execute operation on script include 'SPEntryPage'' from scope occurs

</td><td>

Switching the scope and refreshing the page gives the error, 'Execute operation on script include 'SPEntryPage' from scope 'Knowledge Management - Service Portal' was denied'.

</td><td>

1.  Log in to a Xanadu instance.
2.  Create the glide.entry.first.page.script system property.
3.  Give it the value: new SPEntryPage\(\).getFirstPageURL\(\).
4.  Make 'Knowledge Management - Service Portal' as the current scope.
5.  Refresh the browser page.

Notice the error, 'Execute operation on script include 'SPEntryPage' from scope 'Knowledge Management - Service Portal' was denied. The application 'Knowledge Management - Service Portal' must declare a cross scope access privilege. Please contact the application author to update their privilege requests.'

6.  Repeat step 2 and step 3 with the scopes 'CI Landing Experience' and 'Conversational Interfaces - Diagnostics'.

 Notice that the same error message appears.

</td></tr><tr><td>

Service Portal

 PRB1894604

</td><td>

To reduce regressions, query ACLs are only enforced when certain conditions are met for widget-data-table

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Sidebar \(Family Release\)

 PRB1849937

 [KB2131098](https://hi.service-now.com/kb_view.do?sysparm_article=KB2131098)

</td><td>

When sn\_hr\_core.impersonateCheck is set to 'true', users are unable to add users to the sidebar

</td><td>

When sn\_hr\_core.impersonateCheck is set to 'true', users can't add users to the sidebar discussion for sn\_hr\_core\_case\_payroll records. There's instead an error message: 'Participants can't join the discussion because they don't have access to this record.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software asset analytics

 PRB1860159

</td><td>

There's an issue with the 'potential savings indicator' filter for reclamation candidates

</td><td>

By default, all new reclamations have a user subscription mapped to the 'Subscription to reclaim' M2M table. Where there's a downgrade or consolidate use case, the product and user subscription isn't stamped. Where there's a low usage use case, the product and user subscription is stamped. Due to this, some reclamation candidates are missed by the potential savings calculation.

</td><td>

1.  Create M365 integration.
2.  Run the 'Usage' job.
3.  Create entitlements.
4.  Run the 'Reclamation' job for M365.
5.  Check the user subscription and product for downgrade or consolidate case.
6.  Run the Platform Analytics indicator job 'Subscription Daily Job'.

 Some potential savings for these candidates are missing on the 'Software Asset Analytics' page.

</td></tr><tr><td>

Software Asset Management

 PRB1780888

</td><td>

Potential savings do not appear in LWB for hybrid software

</td><td>

Potential savings calculations for license metric results do not consider reclamation candidates for hybrid products.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1874410

</td><td>

CrowdStrike new license metrics are not added in SampConstants file

</td><td>

The new license metrics sys IDs are not present in SampConstants.SUPPORTED\_LICENSE\_METRICS.

</td><td>

1.  Navigate to the SampConstants Script include.
2.  Check SampConstants.SUPPORTED\_LICENSE\_METRICS.

 Notice that the new license metrics sys IDs are not present.

</td></tr><tr><td>

Software Asset Management

 PRB1885911

</td><td>

Subscription SuiteEngine performance optimizations

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1887365

</td><td>

There is a bug inserting 'Undetermined' unlicensed reasons for more than 'glide.db.max\_view\_records' records for the same product

</td><td>

In SamsProductCalculator.stampUndeterminedEntitiesWithReasons, keep inserting batches of unlicensed installs until there are no more left to insert.

</td><td>

 

</td></tr><tr><td>

Software Asset Management

 PRB1887372

</td><td>

Replication lag caused by AutomaticSMRCreation.stampExistingSoftwareModels

</td><td>

Chunking the large update is the only solution to reduce replication lag.

</td><td>

 

</td></tr><tr><td>

Software Asset Management Publisher Pack for Oracle

 PRB1876860

</td><td>

Download Oracle Glas Report changes to add new fields to VM report and Hardware report

</td><td>

This is an enhancement to uptake new requirements on Oracle Audit download reports.

</td><td>

 

</td></tr><tr><td>

Software Asset Normalization

 PRB1840383

</td><td>

For a software product type other than the licensable normalization engine, it keeps the version empty and marks it as normalized using only the product map

</td><td>

For a software product type other than the licensable normalization engine, it doesn't pick a pattern rule that has a potential to stamp the version, and rather keeps the version empty and marks it as normalized using only the product map. When a discovery model undergoes normalization, in cases for software product types other than licensable, the normalization engine doesn't select a pattern rule that could assign a version. Instead, it leaves the version field empty and designates it as normalized using only the product map.

</td><td>

 

</td></tr><tr><td>

Software Asset Normalization

 PRB1842256

</td><td>

The values for the 'Condition' column of the pattern rules samp\_pattern\_normalization\_rule are not flowing to instances

</td><td>

The 'Condition' column values for samp\_pattern\_normalization\_rule are not flowing to instances. These values are present on the instance, but are missing in the catalog item.

</td><td>

 

</td></tr><tr><td>

Software Entitlements

 PRB1787017

 [KB1650157](https://hi.service-now.com/kb_view.do?sysparm_article=KB1650157)

</td><td>

In Software Asset Workspace, the 'Total cost' is generated incorrectly when the 'glide.sys.date\_format' property value is set to anything other than the default format 'yyyy-MM-dd'

</td><td>

In Software Asset Workspace, the 'Total cost' is generated incorrectly when the 'glide.sys.date\_format' property value is set to dd-MM-yyyy. The Entitlement Total Cost functions properly in the classic view of the alm\_license table, but not in the workspace view. When the default format is used \(yyyy-MM-dd\), the Total Cost calculation is correct on both Software Asset Workspace and the alm\_license table. The root cause of this issue is the base instance client script 'Update total cost onChange subscription', which does not recognize date formats other than 'yyyy-MM-dd' for the start date and end date of the software entitlement in the workspace view.

</td><td>

1.  Set the 'glide.sys.date\_format' property value to dd-MM-yyyy.
2.  Navigate to **Software Asset Workspace** &gt; **License Operations**, and open any Entitlement with License type as 'Subscription'.
3.  Attempt to change the 'Subscription period' to something other than 'Entire Subscription Period'.

 Notice that the 'Total cost' is generated incorrectly due to the new date format preference.

</td></tr><tr><td>

SSH MID Server Communication Protocol

 PRB1887914

</td><td>

SSHProtocolEngine thread is overwhelmed when SSH server starts dumping instead of sending a protocol version string

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Store IRM GRC Core Case Management

 PRB1892851

</td><td>

Inadequate ACLs to prevent range query access to unauthenticated users corecase

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Store IRM Privacy Case Management

 PRB1890991

</td><td>

Addition of Query ACLs in Store IRM Privacy Case Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Supplier Collaboration Portal

 PRB1889728

</td><td>

Addition of Query ACLs in Supplier Collaboration Portal

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Syntax Editor

 PRB1790034

</td><td>

Syntax editor macros do not work reliably

</td><td>

The macro is not rendered upon selecting the Tab button after help or for functions.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB1807367

</td><td>

A processing job should do a ready check while moving events with SysIDs into a queued state

</td><td>

Two jobs targeting a common range work on the same set of queued SysIDs simultaneously, causing events to be processed twice.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB1852694

</td><td>

Events processing is malfunctioning due to cache updates not being generated or propagated

</td><td>

The sys\_cache\_flush isn't showing entries for the updated entries of sys\_processing\_framework\_job, and other node caches are also not reflecting the latest changes.

</td><td>

 

</td></tr><tr><td>

System Events

 PRB1874642

</td><td>

Rhino context re-used for multiple events can lead to inconsistent results

</td><td>

Reusing Rhino contexts can break code that uses poor initialization of global variables.

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB1639586

</td><td>

All import sets are deleted when concurrent data source calls are executed

</td><td>

In the script include ExchangeScopedUtils, the ImportSetCleaner is trying to get the table\_name from importSetGr. In case ImportSetGr is already deleted due to concurrent executions, table\_name is not passed as a parameter and the ImportSetCleaner deletes all the import sets from the instance for all applications.

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB1808239

</td><td>

JDBC connection for authentication=ActiveDirectoryPassword is not working properly

</td><td>

com.microsoft.azure:adal4j:jar:1.6.4 is not compatible with com.nimbusds:oauth2-oidc-sdk:jar:9.10.1.

</td><td>

 

</td></tr><tr><td>

Table Administration and Data Management

 PRB1850232

</td><td>

Query with the yyyy/mm/dd format does not work in RaptorDB

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Territory Planning

 PRB1889733

</td><td>

Addition of Query ACLs in Field Service Manager Workforce

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Third-party Risk Management

 PRB1889679

</td><td>

Addition of Query ACLs in Third-party Risk Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Transform Maps

 PRB1847878

</td><td>

Slow loading of related lists for particular transform maps

</td><td>

It takes several minutes to load a related list from a sys\_transform\_map record.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1892439

</td><td>

When a preset action is selected and autogrow is false, there's infinite loading

</td><td>

 

</td><td>

1.  Have a quickAction with autogrow as false.
2.  Have this quickAction configured on a **Form** field as a default or normal preset action.

 Observe that when this quick action is selected, the modeless dialogue opens but nothing happens.

</td></tr><tr><td>

UI Form Administration

 PRB1781725

</td><td>

Move Attachments doesn't work when a special handling pop-up is displayed

</td><td>

The Move Attachments dialog box is not closeable if it is overlapped by the special handling notes.

</td><td>

1.  Install the Employee Document Management Plugin.
2.  Create a new special handling note for the sn\_hr\_core\_case\_operations table.
3.  Open HR Agent Workspace.
4.  Open an HR case that satisfies the SHN condition.
5.  Add an attachment to the case.
6.  Refresh the page
7.  Select the **Move attachment** button.

The special handling note also pops up.

8.  Close the SHN popup.

 Notice that the page gets stuck with the **Move attachment** dialog box with only the **Close** button visible, which does not work.

</td></tr><tr><td>

UI Form Administration

 PRB1814991

</td><td>

Bulk-edit pop-up form in a presentational list won't refresh after previous transaction

</td><td>

The bulk-edit UI action pop-up form contains the input from the **Description** field from a previous transaction to other records that are opened.

</td><td>

1.  Navigate to **UI Builder** &gt; **Service Operations Workspace**.
2.  Add a variant to the List.
3.  Select **List Page Template** in the Template Picker.
4.  Ensure the new variant has a smaller order than the existing one, so it becomes the default list.
5.  Navigate to **Workspace** &gt; **Service Operations Workspace** &gt; **List** &gt; **Incident** &gt; **All**.
6.  Select any record.
7.  Select the **Edit \(1\)**UI action.
8.  Update the **Description** field in the pop-up to **ABCDE**.
9.  Select **Update**.
10. Notice the success update message.
11. Select another record.
12. Select the **Edit \(1\)** UI action.
13. Notice the **Description** field contains the user input 'ABCDE' from the last transaction.
14. Select **Cancel**.
15. **Confirm** to discard the changes.
16. Select another record.
17. Select the **Edit \(1\)** UI action.

 Notice the **Description** field still contains the user input 'ABCDE' from the previous transaction.

</td></tr><tr><td>

UI Form Administration

 PRB1829603

</td><td>

Workspace fields are cleared when using multiple tabs with an agent

</td><td>

After upgrading to the Washington DC release, an issue occurs when accessing multiple tabs during a chat with a live agent, in which already completed interaction records are cleared.

</td><td>

1.  Log in to an instance.
2.  Impersonate a user.
3.  Navigate to the **Service Operations Workspace**.
4.  Update the status to **Available** in two different tabs.
5.  Impersonate two users.
6.  Initiate a chat from portal.
7.  Fill all the fields in the interaction record.
8.  Search for 'REQ0010001' in the workspace.
9.  Attempt to open REQ0010001.
10. Navigate to **Related Record** &gt; **Requested Items** &gt; **Catalog Tasks**.
11. Add to the work notes.
12. Close the Related Record tab.
13. View the interaction records.

 Notice that the updated values in the interaction record are cleared after opening multiple tabs.

</td></tr><tr><td>

UI Form Administration

 PRB1843602

</td><td>

There's an issue with the date picker position

</td><td>

The date picker position doesn't change when scrolling through the page.

</td><td>

1.  Open a form with a **Date** field.
2.  Select the date picker.
3.  Scroll the page.

 Notice that the date picker remains in the same position on the screen even when scrolling.

</td></tr><tr><td>

UI Form Administration

 PRB1860501

</td><td>

A form's cache key doesn't account for roles with external and internal users

</td><td>

A generated cache key does not contain roles.

</td><td>

1.  Enable the Explicit Roles plugin.
2.  Modify ACL's to incident to allow read access to the snc\_external role.
3.  As an external user, navigate to any given incident.
4.  As an admin, navigate to the sys\_db\_cache table.

 Expected behavior: The cache entry created by the external user, should include the users roles in the cache key.

 Actual behavior: The cache key generated does not contain roles.

</td></tr><tr><td>

UI Form Administration

 PRB1866407

</td><td>

Activity Stream attachment tile actions don't work when a page has been set up to use the multi-controller template

</td><td>

Attachments can't be downloaded from the Activity Stream.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1868782

</td><td>

While composing an email in Vendor Operations, the cursor occasionally jumps, making it difficult to continue typing

</td><td>

When the user types rapidly, the position event is triggered multiple times, resulting in the cursor unexpectedly jumping to the end.

</td><td>

1.  On a base instance, enable email reply recommendations on any table.
2.  Add a line to the end of the email's last line.
3.  Start typing in the first line quickly.

 Observe that the cursor jumps to the end of the file.

</td></tr><tr><td>

UI Policies

 PRB1894468

</td><td>

Performance degradation for Core UI performance

</td><td>

Core UI performance testing shows 250 to 300ms degradation for most direct load user actions.

</td><td>

 

</td></tr><tr><td>

Upgrade Center

 PRB1891562

</td><td>

A user is unable to determine the purpose of a link when it has the context 'Here'

</td><td>

 

</td><td>

1.  Start JAWS.
2.  Navigate to the 'Home' screen.
3.  Navigate to the **Dashboard page** &gt; **Instance upgrade panel** &gt; **Visit Upgrade Center link**.

The respective page opens in a new tab.


 Notice that the screen reader announces 'here' as the link and not what the link is for.

</td></tr><tr><td>

User Presence

 PRB1767417

</td><td>

Multiple threads can unnecessarily race to build the user presence cache adding load to the primary database

</td><td>

Multiple long running SQL queries run against the sys\_user\_presence table.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1834547

</td><td>

An additional HR case creation form opens when selecting the 'View All' details of 'Cases for Subjected Person', 'Cases for Opened For', or 'Interactions' in a some scenarios

</td><td>

Occurs on the HR Agent Workspace 'HR Case creation' page.

</td><td>

1.  Log in as an HR Agent.
2.  Navigate to the HR Agent workspace.
3.  Select the **New HR Case** creation button.
4.  Search for and select an employee.
5.  Select the **Next** button.
6.  Refresh the page.
7.  Enter the employee name again.
8.  Once the 'Create a New Case' page loads, select **View All** for 'Cases for Subjected Person', 'Cases for Opened For', or 'Interactions'.

 Observe the issue where an additional HR case creation form appears.

</td></tr><tr><td>

UX Framework

 PRB1866363

</td><td>

Opening more than the max limit of CSM Workspace tabs outside the ServiceNow Platform doesn't trigger the 'Max limit reached' pop-up

</td><td>

Configuring the sys\_ux\_page\_property to not allow more than 10 tabs open in CSM workspace. When selecting '+' 11 times manually inside the CSM Workspace, 10 tabs are opened as expected. When 11 tabs are opened, a pop-up appears. When the tabs are triggered from outside the ServiceNow Platform using simple JavaScript, 10 tabs are open as expected, when 11 tabs are triggered, all 10 tabs are closed and a new tab is opened.

</td><td>

 

</td></tr><tr><td>

UX Framework

 PRB1868302

</td><td>

Interaction Related Records for 'View Knowledge Articles' in the Service Operations Workspace \(SOW\) are incorrect after upgrading Xanadu

</td><td>

Interaction related records does not map correctly when viewed from SOW.

</td><td>

1.  Hop on to a base instance.
2.  Open the Service Operations Workspace.
3.  Select **Lists** &gt; **Interactions**.
4.  Select **New**.
5.  Completed all required fields.
6.  Select **Save**.
7.  Select **Agent Assist** from the left pane.
8.  Open any KB article in full view.
9.  Navigate to **interaction\_related\_record.LIST**.

Observe that the record is created, and that the ID of the related record is empty and that the table is incorrect, and the knowledge article is empty, and the record type should be 'Knowledge'.

10. Navigate to the **Filter navigator** &gt; **interaction\_related\_record.LIST**.
11. Find the entry created and compare it to the pre-upgrade entries that have completed information.

 Interaction related records does not map correctly when viewed from SOW.

</td></tr><tr><td>

UX Framework

 PRB1869757

 [KB2105389](https://hi.service-now.com/kb_view.do?sysparm_article=KB2105389)

</td><td>

There's a performance degradation when loading the home page on Xanadu

</td><td>

When the system property glide.ux.user\_criteria\_enabled=true, there's a performance degradation between Washington DC and Xanadu when loading the home page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1884471

</td><td>

Incorrect page variant is displayed when the variant audience is mapped to user criteria and glide.ux.user\_criteria\_enabled=true

</td><td>

There is performance degradation between the two versions when the system property glide.ux.user\_criteria\_enabled is to 'true'. The incorrect page variant is displayed when the variant audience is mapped to user criteria.

</td><td>

Scenario 1:

 1.  Open a Washington DC instance.
2.  Set glide.ux.user\_criteria\_enabled to 'true'.
3.  Navigate to a list in the Service Operations Workspace.
4.  Measure the page load times.

 Notice that the average page load time is less than 5 seconds.

 Scenario 2:

 1.  Open a Xanadu instance.
2.  Set glide.ux.user\_criteria\_enabled to 'true'.
3.  Navigate to a list in the Service Operations Workspace.
4.  Measure the page load times.

 Scenario 3:

 1.  Create two page variants which have two respective audience records, which are mapped to two distinct user criteria.
2.  In the user criteria, use two different groups to map two different users.
3.  Open the SOW landing page.

 Expected behavior: The user should see the variant, 'Variant Landing Page Demo Level 2'.

 Actual behavior: The user should see the variant, 'Variant Landing Page Demo Level 1'.

</td></tr><tr><td>

Virtual Agent Designer Legacy

 PRB1896496

</td><td>

KG slot filling is erroring out

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1821950

</td><td>

Now Assist Virtual Agent \(NAVA\) webclient unread message appears on Natural Language Understanding \(NLU\) webclient

</td><td>

Unread messages from the Employee Service Center \(ESC\) webclient appear on the NLU webclient in the Service Portal when it is open in another tab in the browser.

</td><td>

1.  Set up NAVA on an ESC portal.
2.  Keep open NLU AI Search in the Service Portal \(SP\).
3.  Open an ESC portal in one tab of the browser.
4.  Log in.
5.  Open SP in another tab.
6.  Open the ESC portal webclient.
7.  Start any LLM topic.
8.  Complete the topic flow.
9.  Wait for the summary card to appear.
10. Select **Submit**.
11. Open the SP tab.

 Notice that all the unread messages applicable only to the ESC webclient appears on the NLU based webclient.

</td></tr><tr><td>

Virtual Agent

 PRB1853608

</td><td>

NAP isn't loading after 10+ cases notification have been triggered

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1864394

</td><td>

When a user selects the 'None of these' option on the Submit Request \(Template\) topic in Virtual Agent, it generates empty catalog item page

</td><td>

When the user selects the option 'None of these' and selects the link, they are directed to an empty catalog item page. The user should not be asked to submit a request after selecting the option 'None of these'.

</td><td>

1.  Hop into a base Xanadu instance.
2.  Ensure the plugin 'Customer Service Virtual Agent Conversations' is installed on the instance.
3.  Ensure the topic 'Submit Request \(Template\)' is published and visible in Virtual Agent.
4.  Navigate to the Customer Service Management \(CSM\) portal.
5.  Select **Show me everything** &gt; **Submit Request \(Template\)**.
6.  Enter **Create case**.
7.  Select **None of these**.
8.  Select **Yes** for the query 'Do you want to proceed with?'.
9.  Select the link.

 Expected behavior: The user selects the link and they are either directed to the correct catalog item page, a case is created, or for 'None of these' options they are not asked to submit a request.

 Actual behavior: The user is able to submit the 'None of these' option, and it gives an empty link for the catalog item.

</td></tr><tr><td>

Virtual Agent

 PRB1867769

</td><td>

Users can't activate a trigger for a Virtual Agent channel and profile

</td><td>

Instead of calling getChannelByName and hard-coding the channel, it should be grabbed by the channel ID. There's also a missing context profile.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1868975

</td><td>

Some text in some OutputCardControls isn't translating

</td><td>

Specifically the **msg\_heading** and **Heading** fields sent in custom Teams notifications aren't translated.

</td><td>

1.  Set up local instance with chat, DTVA, and MS Teams channel configuration.
2.  Install a language pack.
3.  Change the language.
4.  Create a custom notification.
5.  Trigger a notification.

 Notice the message and the message heading aren't translated.

</td></tr><tr><td>

Virtual Agent

 PRB1881076

</td><td>

Self-Service phase 2 - Dynamic Window experience

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881106

</td><td>

Global changes for auto chat in Glide

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881107

</td><td>

Enhance the async mode error response format in one API

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881108

</td><td>

A capability should have a new type called 'Predictive Intelligence'

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881109

</td><td>

Deep clone of some skills and multiple default prompt bug fixes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881110

</td><td>

Truncation support for tool outputs

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881111

</td><td>

Support 'Cancel' for AutoEval Run

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881112

</td><td>

Enhance APIs to support for creating a dataset and processing a dataset to avoid creating dataset skill mapping

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881113

</td><td>

Auto-prompt tuning check due to a backend name change

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881115

</td><td>

Extend Metric Result's schema and API to persist results per group

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881116

</td><td>

Clone Agentic Eval Run

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881118

</td><td>

Support Agentic AI Eval execution without a proxy skill

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881121

</td><td>

API support for new schema changes

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881123

</td><td>

Adding to an update set should generate child update sets with a unique name

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881125

</td><td>

As an AI Practitioner, users should be able to select a solution, and be able to navigate to additional configurations sections

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1881126

</td><td>

Create a new API for getTestDatasets for agentic-type datasets

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1883338

</td><td>

Skill discovery for a non-agent topic \(caller's assets\) redirects to a AI Agent workflow in NAP

</td><td>

In NAP, skill discovery sometimes redirects to the default Virtual Agent workflow \(AI Agent\) instead of starting the caller assets skill.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1893275

</td><td>

A loading screen appears and a topic with a reference choice control isn't triggered

</td><td>

Automation scripts are also failing due to this.

</td><td>

1.  Log in to an instance.
2.  Create a topic with a reference choice control.
3.  In the reference choice control, set the filter condition to return only one record.
4.  Make the reference choice control skippable.
5.  Run that topic from the Web Client.

 See that the topic isn't triggered and is stuck at the loading screen.

</td></tr><tr><td>

Virtual Agent

 PRB1893952

</td><td>

A Now Assist panel isn't loading on Yokohama instances

</td><td>

Now Assist Panel is not loading AI Agents not running in Playground. An error is observed in the logs.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1896418

</td><td>

Gaic Timing on for App Generation with NAFC NAFC26.4.0

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent third-party integrations

 PRB1837988

</td><td>

Unable to acquire conversation lock leads to repeated impersonation and excessive logging

</td><td>

Certain long-running Virtual Agent transactions, such as file uploads, can cause excessive impersonation logging.

</td><td>

1.  Start a conversation.
2.  Set the lock\_acquired and lock\_touched to current time.
3.  Set lock\_owner to something other than 'Available'.
4.  Send a custom adapter message.

 Observe the impersonation messages that occur repeatedly until the lock is acquired.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1887568

</td><td>

Implement a sys prop for admins to be able to disable the pinned mode for dynamic window

</td><td>

This is a product update.

</td><td>

 

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1893493

 [KB2182131](https://hi.service-now.com/kb_view.do?sysparm_article=KB2182131)

</td><td>

Non-conversational catalog items can't be selected if they are preceded by external KB article citations

</td><td>

When Now Assist for Virtual Agent is enabled, catalog items can't be selected in the Virtual Agent interface.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Vulnerability Response and Configuration Compliance for Containers

 PRB1891682

</td><td>

Addition of Query ACLs in Vulnerability Response and Configuration Compliance for Containers

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Vulnerability Response

 PRB1889724

</td><td>

Addition of Query ACLs in Vulnerability Response

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Workforce Optimization for IT Service Management

 PRB1889670

</td><td>

Addition of Query ACLs in Workforce Optimization for IT Service Management

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1853346

</td><td>

Upgrading to the 'New Places' API

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Work Order Management

 PRB1855599

</td><td>

A work order task \(WOT\) isn't assigned to a vendor/contractor when assigning a WOT to a vendor/contractor group

</td><td>

A work order task \(WOT\) isn't assigned to a vendor/contractor when assigning a WOT to a vendor/contractor group, so the **Assigned to** field is empty in CSM/FSM Configurable Workspace.

</td><td>

1.  Navigate to **Dispatcher workspace** &gt; **Workspace setting**.
2.  Check 'Enable task assignment modal' to ensure an assignment model opens when drag and dropping.
3.  Install the 'Field service territory planning' plugin.
4.  Navigate to a territory model module and set the territory model as true.
5.  Navigate to the **WOT Form page** &gt; **Form layout**.
6.  Add a **Territory** field in the 'DispatcherWorkspace' view if the it isn't already added.
7.  Create a WOT and assign it to some territory that manages at least one contractor group.
8.  Move it in a pending dispatch. Don't give values to **assignment group** or **assigned\_to** fields.
9.  Impersonate as a dispatcher that manages the territory where users assign a work order task.
10. Select the territory from the territory filter.
11. Drag and drop the WOT created in step 7 to the contractor group under 'Contractor Groups'.

 Expected behavior: The **Assigned\_to** field should be populated with the contractor manager.

 Actual behavior: The **Assigned\_to** field comes up as empty.

</td></tr><tr><td>

Work Order Management

 PRB1889505

</td><td>

Fix script is not being executed while upgrade

</td><td>

The fix script is not being executed when upgrading from Washington DC to Yokohama.

</td><td>

1.  Create an instance in Washington DC
2.  Upgrade the instance from Washington DC to Yokohama.
3.  Check for the logs for execution of fix script: sys\_script\_fix\_6e154ec7c3d13010a0cd587c1f40ddd1

 Expected behavior: The sys\_script\_fix\_6e154ec7c3d13010a0cd587c1f40ddd1 must be executed.

 Actual behavior: The sys\_script\_fix\_6e154ec7c3d13010a0cd587c1f40ddd1 is not being executed.

</td></tr><tr><td>

Work Order Management

 PRB1890343

</td><td>

In the CSM portal, the user is unable to see the Worker Order Task \(WOT\) details in the fsm\_ticket page

</td><td>

The WOT details are not shown and an error message on the **wm\_task.parent** field appears.

</td><td>

1.  Create a Work Order \(WO\) with a user as a contact.
2.  Select **Ready for qualification**.
3.  Notice that WOT gets created for WO in the RL.
4.  Impersonate the user set as the contact in the WO.
5.  Access the CSM portal.
6.  Select the WO from the Work orders list.

 Expected behavior: The user should be able to see the WOT details on WO page.

 Actual behavior: The WOT details are not shown and a query\_match error message on the **wm\_task.parent** field is appearing.

</td></tr><tr><td>

Work Order Management

 PRB1893187

</td><td>

The location contributor staff lost access to the work order tasks associated to the work orders on the portal

</td><td>

Error message: 'org.openqa.selenium.TimeoutException: Expected condition failed: waiting for visibility of element located by By.xpath: //\*\[@id='related-wot'\]//table/tbody/tr/td\[1\]/a \(tried for 20 second\(s\) with 500 milliseconds interval\)'.

</td><td>

1.  Log in with the location contributor associated with a location having work order tasks associated with work orders.
2.  Navigate to the cases associated to the work order on the BLSP Portal.
3.  Select work orders RL.
4.  Select the work order task.

 Expected behavior: The user should get access to the work order tasks.

 Actual behavior: The user is getting a query\_range error.

</td></tr><tr><td>

Workplace Core

 PRB1889743

</td><td>

Addition of Query ACLs in Workplace Core

</td><td>

This change adds new Query ACLs on certain table\(s\) and field\(s\) to grant query\_range access.

</td><td>

 

</td></tr></tbody>
</table>## Fixes included

Unless any exceptions are noted, you can safely upgrade to this release version from any of the versions listed below. These prior versions contain PRB fixes that are also included with this release. Be sure to upgrade to the latest listed patch that includes all of the PRB fixes you are interested in.

-   [Xanadu Patch 8 Hotfix 3](xanadu-patch-8-hf-3-PO.md)
-   [Xanadu Patch 8 Hotfix 2](xanadu-patch-8-hf-2-PO.md)
-   [Xanadu Patch 8 Hotfix 1](xanadu-patch-8-hf-1-PO.md)
-   [Xanadu Patch 8](xanadu-patch-8.md)
-   
-   [Xanadu Patch 7a Hotfix 1](xanadu-patch-7a-hf-1-PO.md)
-   xp7b
-   [Xanadu Patch 7](xanadu-patch-7.md)
-   [Xanadu Patch 6 Hotfix 2](xanadu-patch-6-hf-2-PO.md)
-   [Xanadu Patch 6 Hotfix 1](xanadu-patch-6-hf-1-PO.md)
-   [Xanadu Patch 6](xanadu-patch-6.md)
-   [Xanadu Patch 5](xanadu-patch-5.md)
-   [Xanadu Patch 4](xanadu-patch-4.md)
-   [Xanadu Patch 3](xanadu-patch-3.md)
-   [Xanadu Patch 2](xanadu-patch-2.md)
-   [Xanadu Patch 1](xanadu-patch-1.md)
-   [Xanadu security and notable fixes](xanadu-security-notables.md)
-   [All other Xanadu fixes](xanadu-all-other-fixes.md)

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


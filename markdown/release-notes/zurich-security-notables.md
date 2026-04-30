---
title: Zurich security and notable fixes
description: The Zurich release contains important problem fixes.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 109
breadcrumb: [Available patches and hotfixes, Learn about the Zurich release, Zurich release notes]
---

# Zurich security and notable fixes

The Zurich release contains important problem fixes.

-   **Zurich was released on July 31, 2025.**
    -   07-23-2025\_1759
    -   glide-zurich-07-01-2025\_\_patch0-07-15-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform® major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/zurich/rn/patches/PRBs-Z00.00.xlsx).

## Security-related fixes

Zurich includes fixes for security-related problems that affected certain ServiceNow® applications and the ServiceNow AI Platform®. We recommend that customers upgrade to this release for the most secure and up-to-date features. For more details on security problems fixed in Zurich, refer to [KB2249737](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2249737).

## Notes for Zurich

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

Access Control

 PRB1833782

 [KB1721153](https://hi.service-now.com/kb_view.do?sysparm_article=KB1721153)

</td><td>

There's slowness when loading forms with **TableChoice** fields related to the RecordFamilyResolver .archiveTableHas ACLTerms code path

</td><td>

Accessing any form with a **TableChoice** field where the instance has more than 250 archive tables can result in slowness due to RecordFamilyResolver .archiveTableHasACLTerms code path and a change to CACHE\_ARCHIVE\_TABLE \_HAS\_ACL\_TERMS in Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Access Control

 PRB1840256

</td><td>

Excessive syslog logging from AccessTerm 'Slow ACL'

</td><td>

Excessive logging from AccessTerm 'Slow ACL' is detected in syslog shards.

</td><td>

 

</td></tr><tr><td>

Access Control

 PRB1840787

</td><td>

itil role users receive an error on short description suggestions

</td><td>

itil role users observe several errors when selecting the **Suggestion** button on short descriptions on incident records.

</td><td>

1.  Access a base Xanadu instance.
2.  Impersonate an itil user.
3.  Navigate to **All** &gt; **Incident** &gt; **Create New**.
4.  Select the **Suggestion** button next to **Short description**.

 Observe errors regarding the 'sys\_choice' table.

</td></tr><tr><td>

Access Control

 PRB1868511

</td><td>

Adding other roles to the 'Contains role' tab in the 'snc\_internal' role causes unexpected behavior

</td><td>

Newly created users don't receive the 'snc\_internal' role when logging in, or getting impersonated, for the first time.

</td><td>

1.  Provision an instance with 'sn\_dlir' installed.
2.  Add the 'sn\_dlir.secure\_file\_download' role to the 'Contains role' related list in the 'snc\_internal'.
3.  Create a new user.
4.  Impersonate or log in under the newly created user.

 Expected behavior: Roles can't be added to the 'Contains role' related list in the 'snc\_internal', or there's a business role or another check that informs the user when they are doing it.

 Actual behavior: A newly created user doesn't receive 'snc\_internal'. In node logs, users can observe: '\*\*\* WARNING\*\*\* RoleAccessHandler: User does not have the role...'

</td></tr><tr><td>

Action Bar Component

 PRB1840507

</td><td>

An incorrect action bar intermittently displays

</td><td>

 

</td><td>

1.  Navigate to /now/cwf/agent/home.
2.  Impersonate a user.
3.  In the list, select **My cases** &gt; **New**.
4.  Select **Accept UI Action**.

 Expected behavior: The action bar shouldn't change.

 Actual behavior: The action bar changes in a few seconds after the case is accepted.

</td></tr><tr><td>

Activity Stream Compose Component

 PRB1897434

</td><td>

The 'Email' tab in the Activity Stream in the CSM Configurable Workspace doesn't resize when the text is larger than the vertical limit

</td><td>

This issue is found in Yokohama, but works as expected in Xanadu.

</td><td>

1.  Navigate to a Yokohama instance as an admin user.
2.  Navigate to the **Activity Stream** &gt; **More** &gt; **Email**.
3.  Select **Return past vertical limit**.

 Expected behavior: The email text box auto-resizes vertically.

 Actual behavior: The email text box doesn't auto-resize.

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

 PRB1858894

 [KB2027692](https://hi.service-now.com/kb_view.do?sysparm_article=KB2027692)

</td><td>

Application Programming Interface \(API\), Now Platform, and GraphQL are slow due to the Table Cleaner being throttled causing heavy replication lag

</td><td>

API, Now Platform, and GraphQL calls are slow specifically because of the Table Cleaner on sys\_activity shards. ​Using Instant Alter added an index, and as a result, all records were replicated with the load causing replication lag. When replication lag is detected, Table Cleaners are throttled, which can exacerbate the amount of data that is being replicated and cause timeouts. Timeouts are caused by the Table Cleaner running synchronously in the Activity Stream load request.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Activity Stream

 PRB1860591

</td><td>

Work notes are presented as encrypted text within the 'Activity' section of the ServiceNow Workspace when the encryption configuration is active

</td><td>

There's column-level encryption enabled and configured for the **work\_notes** field. When a user with a target role specified in the sys\_platform\_ encryption\_configuration record is posting worknotes in workspace, they are unable to see unencrypted text. Instead, they're seeing encrypted text. When the same user posts worknotes in the native view, the text isn't encrypted.

</td><td>

 

</td></tr><tr><td>

Activity Stream

 PRB1870524

</td><td>

If user\_id is in the form of a sys\_id, then the user isn't displayed correctly in the activity stream

</td><td>

The sys\_created\_by can be a user\_id or a sys\_id or an email, so it guesses based on the format. If the user\_id is copying the sys\_id format, then this process doesn't work.

</td><td>

1.  Create a user with a user\_id in the format of a sys\_id.
2.  Give the user sufficient roles to view workspace.
3.  Impersonate the user created.
4.  Navigate to some record on workspace and add a comment or make a field change.

 Notice this user's user\_id is displayed instead of the display name.

</td></tr><tr><td>

Activity Stream

 PRB1893483

</td><td>

No activity displays in UI16 when a blank journal event is added to the Activity Stream

</td><td>

After upgrading to Yokohama, some records display 'No Activity' on the platform view. A null pointer exception displays.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1862727

</td><td>

A 'Show audio' modal appears when an agent presence state is changed to 'Available' for Safari users

</td><td>

A user interaction is required on the page for the audio to work, especially in inactive tabs. This was enforced by a modal when the audioContext was detected to be suspended, which occurs when a new AudioContext is created in the page. Now, the modal appears for Safari whenever the presence changes in the inbox to 'Available' to avoid having users refresh the browser to see the modal.

</td><td>

 

</td></tr><tr><td>

Agent Chat

 PRB1887118

</td><td>

The 'new message' sound and desktop notification aren't working in legacy workspace

</td><td>

 

</td><td>

1.  As an agent, navigate to the legacy workspace with the url /workspace/agent.
2.  As a requestor, start a chat.
3.  After an agent accepts the work item, as a requestor, start sending some messages.

 Expected behavior: When desktop and sound notifications are turned on, an agent should hear the sound for a new message and receive desktop notifications for the new message.

 Actual behavior: There's no sound or desktop notification.

</td></tr><tr><td>

Agent Chat

 PRB1900981

 [KB2226265](https://hi.service-now.com/kb_view.do?sysparm_article=KB2226265)

</td><td>

Inbox audio is delayed when the 'Workspace' tab is inactive or out of focus before receiving the first work item

</td><td>

When the work item assigned, audio isn't heard. Audio is heard only after switching back to the workspace. The agent may not get notified at the time of assignment due to this issue, and the work item may expired by the time agent is back on the workspace tab.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Agile Development

 PRB1900463

 [KB2251764](https://hi.service-now.com/kb_view.do?sysparm_article=KB2251764)

</td><td>

Global search isn't working for certain records after upgrading to Yokohama

</td><td>

After upgrading to Yokohama, pre-fix for certain records, such as Release, Feature, Phase, got updated. This prevents the global search from working as expected. The new pre-fix records are searchable, but existing records created before the upgrade using the old prefix aren't searchable.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search Glide

 PRB1590070

</td><td>

Index events take a long time when there's a substantial amount of data in the sys\_translated table

</td><td>

When indexing the **Translated** field from the sys\_translated table, all the data for a particular table is cached at once. When there's a frequent update or insert to the sys\_translated table, the rebuild cache takes an average of 5 seconds to 8 seconds per event.

</td><td>

1.  Enable a language plugin.
2.  Index a record with a **Translated** field with a translation in the sys\_translated table \(e.g. sys\_ui\_list, title field\)
3.  Navigate to **cache\_inspect.do**.
4.  Observe that all data for the same table will be loaded into the private TS\_TRANSLATED\_MAP cache.
5.  Flush the cache.
6.  Reindex one record.

 Observe the cache was rebuilt with all data from that table.

</td></tr><tr><td>

AI Search

 PRB1823459

</td><td>

AI Search indexing 'Topic Path Translation' doesn't work for a non-system user preference language

</td><td>

Session users assigned as 'guest' with the sys\_user\_preference file 'name=user.language' and 'value=some\_non\_ user\_session\_language' have topic paths indexed in this language. The set language isn't effective, which is the cause of incorrect translations.

</td><td>

1.  Ensure sys\_language has two active languages, **en** for English and **de** for Deutsch.
2.  Create an entry in the sys\_user\_preference table with the following values:
    -   system = true
    -   user = empty with language as 'de'
3.  Create the catalog item with translations for topic and topic path.

 Expected behavior: AI Search should index, and be able to search with the 'en' topic value.

 Actual behavior: AI Search indexes content with Deutsch translations for documents with both English and Deutsch languages, and the search for English fails.

</td></tr><tr><td>

AI Search

 PRB1824166

</td><td>

A translated reference field is indexed in a different language in a single record update instead of a full table index

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

 PRB1825963

 [KB1763961](https://hi.service-now.com/kb_view.do?sysparm_article=KB1763961)

</td><td>

Index KBB throws an exception about journal peekahead

</td><td>

An error is thrown: 'IngestService: Unable to index Glide Record \[9b85baaa3bf11a10 c4589c8c24e45a2b\] u\_kb\_template\_topic\_category. fa8191f6fb059 e507863f46b5eefdc1d : Cannot invoke "java.util.Map.get\(Object\)" because "journalElementToValuesMap" is null java.lang.NullPointerException: Cannot invoke "java.util.Map.get\(Object\)" because "journalElementToValuesMap" is null...'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1836358

 [KB1790348](https://hi.service-now.com/kb_view.do?sysparm_article=KB1790348)

</td><td>

A race condition causes an incorrect deleteMultiple\(\) query to be generated on the v\_search\_genius\_result and sys\_variable\_value tables

</td><td>

When the AI Search Genius Result is requested and processed in a multi-threaded, high-concurrency environment, such as when multiple users simultaneously perform search functions on a portal or virtual assistant \(VA\), a thread safety issue arises. This issue may cause an incorrect deleteMultiple\(\) query to be generated, potentially leading to the deletion of excessive records from the sys\_variable\_value table. As a result, various components, including the Integration Hub, Service Catalog items, and workflows, may malfunction due to the absence of these critical records.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1837035

 [KB2187724](https://hi.service-now.com/kb_view.do?sysparm_article=KB2187724)

</td><td>

Catalog item access isn't evaluated correctly when there is service\_portfolio in some cases

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1837962

</td><td>

When a query is performed in 'OR' mode, the pagination breaks

</td><td>

0 results are returned.

</td><td>

1.  Change the property 'glide.ais.query.search\_operator' to 'OR'.
2.  Perform a search on Service Portal that returns more than 12 results.
3.  Select the **Next page** arrow button.

 Observe that there's no matches.

</td></tr><tr><td>

AI Search

 PRB1841283

</td><td>

There's errors in logs during ingestion for users without GAIC or Semantic Search

</td><td>

If there's no semantic search configured, the log shouldn't be polluted with errors.

</td><td>

 

</td></tr><tr><td>

AI Search

 PRB1843005

</td><td>

The text '\(number\) results for \(keyword\)' text is not translated when using AI Search

</td><td>

After installing a language plugin and switching the language to a non-English language, the text '\(number\) results for \(keyword\)' is not translated when using AI Search. This occurs when a keyword is misspelled when using AI Search.

</td><td>

1.  Provision an instance with the 'Language' plugin and AI Search installed.
2.  Log in to the instance.
3.  Switch the language to non-English.
4.  Open an Employee Service Center portal.
5.  Search for any misspelled keyword.

 Expected behavior: The text '\(number\) results for \(keyword\)' text is translated to the non-English language.

 Actual behavior: The text '\(number\) results for \(keyword\)' text is seen in English and is not translated.

</td></tr><tr><td>

AI Search

 PRB1844340

 [KB2084368](https://hi.service-now.com/kb_view.do?sysparm_article=KB2084368)

</td><td>

The AI Search class can't handle a non-rotated table

</td><td>

If the \[sysevent\] table isn't configured for table rotation, AI Search can't process indexing events and an error is seen in the system logs.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

AI Search

 PRB1850631

 [KB1949808](https://hi.service-now.com/kb_view.do?sysparm_article=KB1949808)

</td><td>

The **Table** field for EVAM view configuration matching of a search record is always the parent table

</td><td>

With the new EVAM-lite implementation, there are 3 gaps in the logic for determining which view configuration to use for a given search result. 1. If a view configuration has a condition based on a field that isn't included in the list of table fields, that field won't be returned from AIS, and so the condition never matches. Even if the field is included on the 'Table Fields' list, if it's a field that only exists on a child table of the table the indexed source is based on, the field won't be returned from AIS and so the condition never matches. If the first view configuration for a particular table comes after the default/global view config, it is never used. Whereas, EVAM had a more nuanced selection process that would look for all view configuration that matched on the table before falling back to those for ancestor tables or the global/default table.

</td><td>

1.  Set the system property glide.search.evam .logger.enabled to true.
2.  Open the Service Portal and search for 'new hire'.
3.  Open the syslog.
4.  Filter on 'Created'.
5.  Notice there's a message that contains: '\[SEARCH EVAM\] SearchResultTemplateGenerator: Using View Config 633c3b5d53a 71010968a ddeeff7b1218 for Result with table sc\_cat\_item and sys\_id 6690750 f4f7b4200086 eeed18110c761'.

 Expected behavior: Service Portal's EVAM Def'n has a view configuration called 'Catalog Search Results - Order Guides', which has a condition of 'sys\_class\_name = sc\_cat\_item\_guide^EQ'. This is the view configuration that should be used, and the syslog entry should contain: '\[SEARCH EVAM\] SearchResultTemplateGenerator: Using View Config 44c37371 c32020108 25039b06 e40dd4b for Result with table sc\_cat\_item and sys\_id 6690750 f4f7b4200086 eeed18110c761'.

 Actual behavior: The incorrect view config is being used. 633c3b5 d53a71010968 addeeff7b1218 is the sys\_id of the view configuration called 'Catalog Search Results', which is the generic view configuration for catalog items, and doesn't have any conditions beyond table. But the 'New Hire' category item is an 'Order Guide', and there's an EVAM view configuration specifically for that.

</td></tr><tr><td>

AI Search

 PRB1862241

</td><td>

There's an error in the logs when using a catalog Genius Result

</td><td>

One generates every time that a user requests a Catalog Genius result when the mode is async.

</td><td>

1.  Ensure Catalog Genius Results are enabled for a Service Portal \(SP\) search profile.
2.  Navigate to SP.
3.  Search for 'Miro'.

 Observe the error: '\[SEARCH API\] SearchCheckpointService: Unable to post checkpoint, Callback name missing: no thrown error'.

</td></tr><tr><td>

AI Search

 PRB1875775

</td><td>

Field-level permissions should only apply when building template props

</td><td>

 

</td><td>

1.  As a user with elevated privileges, navigate to AIS-enabled Service Portal \(SP\) and search for 'new hire order'.
2.  Select the first regular result.

Observe that the user is taken to the 'sc\_cat\_item\_guide' portal page.

3.  Impersonate a non-admin user.
4.  Open SP and search 'new hire order'.
5.  Select the first regular result \(should be the same result as Step 2\).

 Expected behavior: The user is taken to the 'sc\_cat\_item' guide page.

 Actual behavior: The user is taken to the 'sc\_cat\_item' portal page.

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

 Notice that it's not redirected to the parent record. It's redirected to the sys\_attachment.do? sys\_id=undefined&amp; searchterm=detail.

</td></tr><tr><td>

Analytics Data API

 PRB1845187

 [KB2238953](https://hi.service-now.com/kb_view.do?sysparm_article=KB2238953)

</td><td>

Drilling down on KPIs in a Performance Analytics dashboard produces an error 'no internet connection"'

</td><td>

Drilling down on any value redirects the user to the KPI details page with a 'No Internet connection' error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

API Usage Analytics Dashboard

 PRB1842140

</td><td>

API\_INT Semaphore queue depth shows a negative value in stats.do misguiding analysis and troubleshooting

</td><td>

There are two problems. First, the count shouldn't go negative when any exception happens. Second, it shouldn't throw an exception, which ultimately drops the request on the floor and never responds to the browser.

</td><td>

 

</td></tr><tr><td>

Application Install Engine

 PRB1846815

</td><td>

Admins users aren't able to repair/install all dependencies when domain separation is enabled

</td><td>

An issue was observed where a parent application \(e.g., Now Assist For CSM\) was installed successfully, even though its dependencies \(e.g., sn\_genai\_platform\) weren't installed during the process. This behavior is unexpected.

</td><td>

1.  Open an instance where domain separation is enabled.
2.  Create an admin user in a different domain.
3.  Log in or impersonate as that admin user.
4.  Change the domain to global.
5.  Attempt to install a parent application with known dependencies.

New dependencies aren't installed and there's domain related errors in plugin logs.

6.  Try to repair the same plugin.
7.  Verify that the new dependencies are still not installed and the domain related errors in plugin logs are still present.

 All the dependencies should be installed with the parent app.

</td></tr><tr><td>

Application Manager

 PRB1834952

</td><td>

The Service Bridge Base plugin doesn't automatically upgrade when the Service Bridge for Providers plugin is upgraded

</td><td>

This issue occurs for users in a non-global domain or scope.

</td><td>

 

</td></tr><tr><td>

Appointment Booking

 PRB1894193

</td><td>

The scope of the Appointment Booking service's configuration was changed in Yokohama, which leads to a scope access issue

</td><td>

After upgrading to Yokohama from Washington, the value of the 'Availability' table changed from wu\_appointment to empty in some Appointment Booking service configuration records.

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

Audit History

 PRB1795159

</td><td>

Business rules aren't running on the 'Audit delete' table

</td><td>

The issue was reproduced in a Washington instance.

</td><td>

1.  Create a business rule \(BR\) on the sys\_audit\_delete table and make it to execute before the insert.
2.  Write a simple script gs.log to know the BR trigger.
3.  Delete an entry from the cmdb\_ci table so that it creates an entry in sys\_audit\_delete.

 Expected behavior: The BR triggers and creates a log.

 Actual behavior: The BR isn't triggering.

</td></tr><tr><td>

Authentication

 PRB1889955

</td><td>

The new banner menu of Yokohama refers to glide.multifactor. enforcement. acknowledged by the sys\_id instead of the property name

</td><td>

This causes an issue if the sys\_id has already been used by the instance.

</td><td>

1.  Log in as an admin.
2.  Turn on MFA, AA and MFA Context.
3.  Set 'Role Based MFA' to a role like 'Admin'.
4.  Set the glide.multifactor. enforcement. acknowledged property as false.
5.  Set the property of SWP and MAX SWP as '30' and '90'.
6.  Log in via an admin user who hasn't enforced MFA.
7.  Navigate to an admin profile.
8.  Select the **Acknowledge** link in the message.

 Expected behavior: Verify that the admin should be able to acknowledge the message and the glide.multifactor. enforcement. acknowledged property should be true now.

 Actual behavior: The **Acknowledgment** link does not work.

</td></tr><tr><td>

Banner Frame

 PRB1679019

</td><td>

UX Banner announcements appear for users with orphaned roles when they don't belong to the group needed to view the announcement

</td><td>

UX Banner announcements appear for the user even though they have an orphaned sys\_user\_has\_role record and don't belong to the banner group.

</td><td>

1.  Create a new group named 'banner group'.
2.  Create a banner announcement.
3.  Navigate to the **Show for** field.
4.  Select **Users with specific role/groups**.
5.  Associate the banner group with the banner announcement.
6.  Associate the banner announcement with the Unified Navigation configuration.
7.  Create an orphaned record in sys\_user\_has\_role.
8.  Find a user with records in with the sys\_user\_has\_role.
9.  Open the sys\_user\_has\_role records for that user.
10. Export as XML.
11. Change the following fields:
    1.  Set 'inherited' to 'false'.
    2.  Change the role sys\_id to one that doesn't exist in the sys\_user\_role table.
    3.  Change the 'role' display\_value.
    4.  Change 'name' to non-existent roles in the sys\_user\_role table.
    5.  Change the **sys\_id** field to one that doesn't exist in the sys\_user\_has\_role table.
12. Import the record back into the instance.
13. Observe that in the sys\_user\_has\_role, the record imported says 'empty' for the **Role** field.
14. Impersonate the user with the orphaned sys\_user\_has\_role record.

 Notice that the UX Banner announcement created appears for the user even though they belong to the group.

</td></tr><tr><td>

Banner Frame

 PRB1878987

 [KB2091173](https://hi.service-now.com/kb_view.do?sysparm_article=KB2091173)

</td><td>

An HTML link for a page header caption \(glide.product. description\) is broken in a logo tooltip

</td><td>

On Yokohama, an HTML href attribute \(link reference\) included into a page header caption on the 'Basic Configuration UI16' page \(glide.product.description sys property\) doesn't render the href attribute.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Business rules \(Classic\)

 PRB1759349

</td><td>

The child table of the cmn\_location table doesn't trigger the business rule for full names

</td><td>

The business rule doesn't populate for child tables for cmn\_locations, 'Location - generate full name'. The business rule on the table just calls the 'HierarchicalReference \#generate\(\)' function, and the changes need to happen in the function.

</td><td>

1.  Make a cmn\_location table extendable.
2.  Create a child table for cmn\_location.
3.  Create a record on the child table.
4.  Choose the parent from the cmn\_location table.

 Expected behavior: The full name 'Apac/India/Hyderabad/test' is populated.

 Actual behavior: The full name doesn't populate accurately.

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1860702

</td><td>

The Vendor Portal 'Take-questionnaire' page stops working when the HR application is installed

</td><td>

Users observe an error on the page.

</td><td>

 

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

 PRB1905312

</td><td>

Feedback definition table doesn't display any feedback records

</td><td>

Feedback definitions aren't visible. Also, users can't create a feedback definition.

</td><td>

1.  Log in to an instance.
2.  Navigate to the feedback definitions \(sn\_ex\_sp\_pro\_feedback\_definition\) table.

 Actual behavior: Feedback definitions aren't visible.

 Expected behavior: Feedback definitions should be displayed.

 1.  Log in to the instance.
2.  Navigate to the feedback definitions \(sn\_ex\_sp\_pro\_feedback\_definition\) table.
3.  Select the **new** button.

 Actual behavior: Users are unable to create a feedback definition.

 Expected behavior: Users should be able to create a feedback definition.

</td></tr><tr><td>

Change Management Collision Detector

 PRB1868251

</td><td>

The 'Conflict Detection' job, especially the ChangeCheck ConflictsSNC script include, can lead to an OutOfMemoryError and node restarts

</td><td>

This seems to happen when the Affected CIs \[task\_ci\] table has a large amount of records on it. In one of the cases, there were 93,685,849 records.

</td><td>

Run the 'Conflict Detection' job and notice it loops in the ChangeCheckConflictsSNC script include.

</td></tr><tr><td>

Change Management

 PRB1880887

 [KB2116476](https://hi.service-now.com/kb_view.do?sysparm_article=KB2116476)

</td><td>

com.snc.change\_management .standard\_change\_catalog is activated on an upgrade

</td><td>

com.snc.change\_management. standard\_change\_flows is installed on an upgrade and zboot. This has a dependency on the standard change catalog. The dependency needs to be removed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Cloud Provisioning and Governance with Amazon Web Services

 PRB1788540

 [KB1709741](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709741)

</td><td>

The API transaction '/api/now/cloud\_event' triggered by 'AWS events-driven discovery' is overloading Default Semaphores and should be routed to Integration Semaphores

</td><td>

These transactions are processing on Default Semaphores instead of Integration Semaphores, leading to semaphore exhaustions impacting the user experience. During a severe influx, these transactions can take more time for processing due to DB locks, and a single transaction can take 45 seconds to execute due to the wait time. This can potentially cause an outage.

</td><td>

Refer to the listed KB article for details.

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

Column Level Encryption Enterprise

 PRB1874479

 [KB2070474](https://hi.service-now.com/kb_view.do?sysparm_article=KB2070474)

</td><td>

The security banner message 'One or more security migration jobs have failed in your instance' appears constantly and isn't dismissed after one day

</td><td>

As part of the Column Level Encryption \(CLE\) migration process from Yokohoma and later, there are cases where the 'Key migration' job is failing as there's no key to migrate. As the key migration job fails, there's a security banner announcement 'One or more security migration jobs have failed in your instance', which is appearing in the instance post-migration. The red banner message for migration errors isn't dismissed. The banner message should appear only for one day and be dismissed after that. However, the banner message is displayed constantly.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Communities

 PRB1865845

</td><td>

Some characters are displayed as unicode in blog titles

</td><td>

When a blog article in posted in the Community portal, some characters are encoded in unicode and then are displayed without being decoded.

</td><td>

1.  With the Communities plugin installed, set up a forum and put 'blog' in the 'Content type' related list.
2.  Navigate to the Community portal.
3.  Navigate to **Community** &gt; **All forums**.
4.  Select the created forum.
5.  On the right-hand side menu, select **Post Content** &gt; **Blog**.
6.  In the blog title, input something like 'test漢字テストﾃｽﾄ７7'.
7.  Input a description.
8.  Select **Save as draft** or **Publish**.

 Observe that the title is now 'test漢字テスト&amp;\#xff83;&amp;\#xff7d;&amp;\#xff84;&amp;\#xff17;7'.

</td></tr><tr><td>

Condition Builder

 PRB1843987

 [KB2153113](https://hi.service-now.com/kb_view.do?sysparm_article=KB2153113)

</td><td>

Predicate Builder's 'Date Time' filter displays a JavaScript condition with quotation marks missing around the date parameter

</td><td>

Quotation marks should be surrounded by the condition '--&gt;', causing an issue with the query.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1830256

</td><td>

If eligible records are more than the batch size, certification audit results are duplicated for failed CIs

</td><td>

The checkTableAttributesAgainstTemplate method doesn't respect the current batch it is running in. It instead queries the entire CI class tables and logs the failed results.

</td><td>

1.  Create more than 1000 records in CI tables, like cmdb\_ci\_linux\_server or cmdb\_ci\_business\_app.
2.  Update any of the attributes, like cmdb\_ci\_linux\_server.os\_version or cmdb\_ci\_business\_app.active\_user\_count, to a particular value for half of the records
3.  Configure cert\_audit where certification attributes match half the records updated in step 2. Use only 1 attribute to certify.
4.  Run the audit.

 Expected behavior: The number of records in the cert\_audit\_results table shouldn't be more than one.

 Actual behavior: The total\_num\_records/1000 +1 times the results get duplicated for failed results.

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1840516

</td><td>

When using an absolute value for a lifecycle stage, it moves to empty, but it accepts and saves a string value with a 'contains an' operator

</td><td>

On that policy form, the filter is using the **Lifecycle stage** reference field where the dictionary is configured to use 'reference key' = 'name'. The record lookup is done using the **Name** field instead of default 'sys\_id'.

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1893468

</td><td>

The 'Sync Managed By Group from CI Class' script action has an infinite loop edge case

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

 PRB1895685

</td><td>

If a CI's sys\_mod\_count value is empty, CMDB Health jobs become stuck

</td><td>

The platform allows the autoSysFields function to be used when inserting and updating CIs from a script. A script turns on or off the update to the fields sys\_updated\_by, sys\_updated\_on, sys\_mod\_count, sys\_created\_by, and sys\_created\_on. This is often used for manually updating field values on a record while leaving historical information unchanged. CMDB Health jobs becomes stuck if a CI's sys\_mod\_count value is empty due to being inserted like that.

</td><td>

 

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

 PRB1868773

</td><td>

canWrite on GlideElement for variable sets returns a null pointer exception

</td><td>

There's an issue calling a canWrite on a variable set when applying form changes to be filtered. The individual variables behave correctly.

</td><td>

 

</td></tr><tr><td>

Core Platform

 PRB1775831

 [KB1818197](https://hi.service-now.com/kb_view.do?sysparm_article=KB1818197)

</td><td>

When the user accesses a CTI record URL before SSO or a local login, they are redirected to an incident.do record

</td><td>

When the user is logged in to an instance, a CTI link takes them to the correct record. However, when they are logged out, they are directed to the incident.do page.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Indexes

 PRB1788235

</td><td>

Redundant indexes are created on a column with a non-unique index when a unique index is created on it

</td><td>

Creating a unique index on a column that already has a non-unique index on it leads to duplicate indexes on the same column.

</td><td>

Scenario 1:

 1.  Log in to any base instance.
2.  Create a non-unique index on a column of any table using the Tables &amp; Columns module.
3.  Once the index is created, create a unique index on the same column of the table using the tables &amp; columns module.
4.  Validate the indexes on the table.

 Notice that there are two indexes on the same column, where one is unique and the other one is non-unique.

 Scenario 2:

 1.  Login to any base instance.
2.  Create a non-unique index on a column of any table using the Tables &amp; Columns module.
3.  Navigate to **Dictionary**.
4.  Open the table/column with the created index.
    1.  Attempt to set the unique flag to 'True'.
    2.  Notice a pop-up stating, 'A non-unique index exists on this column. To create a unique index for this column use IndexCreator in the Tables &amp; Columns page or in this column's Table record'.
5.  Navigate to Tables &amp; Columns module.
6.  Create a unique index on the same column.
    1.  Attempt to set the unique flag to 'True'.
    2.  Notice that the same a pop-up appears stating, 'A non-unique index exists on this column. To create a unique index for this column use IndexCreator in the Tables &amp; Columns page or in this column's Table record'.
7.  Drop the non-unique from the backend.
8.  Invalidate the table cache.
9.  Attempt to set the unique flag to 'True' in sys\_dictionary for that record.

 Notice that the activity will be successfully completed.

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

 PRB1840970

 [KB2007890](https://hi.service-now.com/kb_view.do?sysparm_article=KB2007890)

</td><td>

Monthly/Yearly scheduled jobs named 'Physical Table Stats Aggregator/Gatherer' causes slow CPU and instance responses

</td><td>

This problem manifested primarily on demo instances that have more than 300 DBIs, but it isn't necessarily isolated to demo hosts.

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

Database Persistence - Data Management

 PRB1868796

 [KB2071053](https://hi.service-now.com/kb_view.do?sysparm_article=KB2071053)

</td><td>

Updating a record in the sn\_vul\_vulnerability table via Data Management Update Jobs \(sys\_dm\_update\) throws an error

</td><td>

The user can open a record in the sn\_vul\_vulnerability table and update it, but when the same user tries to update it via the sys\_dm\_update job, it throws an error. Error: 'The user does not have the necessary permissions to update records in table sn\_vul\_vulnerability'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Management

 PRB1881515

</td><td>

The 'Collect Reliability Metrics for Data Management' job causes history lest length \(HLL\)

</td><td>

The instance experiences resource constraints.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1266075

 [KB0728469](https://hi.service-now.com/kb_view.do?sysparm_article=KB0728469)

</td><td>

If all tables that are part of a database view are on the same gateway database, Glide should be able to redirect the query to the gateway

</td><td>

Database views that are connecting to tables that are sharded aren't working. They aren't honoring the gateway configuration and still look in the base database.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1759098

</td><td>

A Glide connection gets stuck when statement cancelation response from the server is lost

</td><td>

When a statement is canceled, Glide sends a request to the Oracle server, which replies with 'break', and sometimes the reply doesn't return due to some error.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1829039

</td><td>

Users are unable to add query rewrite if the execution time greater than 10 seconds

</td><td>

Trying to add a index hint/rewrite on Xanadu where the total execution time is greater than 10 seconds rewrites if the execution time is greater than 10 seconds.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1840823

</td><td>

Temporary files are left by PG-JDBC driver

</td><td>

There must be obsolete .trs files in /glide/nodes/node port/tmp directory. Obsolete files are created 1 hour ago or before and not touched.

</td><td>

 

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1844798

</td><td>

An error message for an unknown system variable 'sql\_generate\_invisible\_primary\_key' warning is received

</td><td>

This issue was observed in a Xanadu instance.

</td><td>

1.  Open a Xanadu instance.
2.  Created a new table from sys\_db\_object\_list.do.

 Observe the warning error message, 'Unknown system variable 'sql\_generate\_invisible \_primary\_key''.

</td></tr><tr><td>

Database Persistence - Data Scale

 PRB1846741

</td><td>

Adjust tuple size thresholds to avoid failing legitimate queries

</td><td>

Adjusting the threshold to a reasonable value to avoid failing some queries.

</td><td>

 

</td></tr><tr><td>

Database Persistence

 PRB1593310

</td><td>

Updating an application from the application repository to change the column type from 'Date' to 'String' doesn't change the column type in the database

</td><td>

.

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

Discovery

 PRB1648843

 [KB1282470](https://hi.service-now.com/kb_view.do?sysparm_article=KB1282470)

</td><td>

Active processes from Windows ADM fails to collect active processes on some devices

</td><td>

The issue may present itself as process classifiers not being triggered, for example vCenter or MSSQL patterns not being triggered. The 'Active Processes' table isn't populated, causing the classifiers to not be triggered.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1657280

</td><td>

There's inaccurate error logging for failed application patterns due to running processes that have bounced or stopped before pattern process detection executes

</td><td>

Commands using the PID and PORT from the ADM Probe return null in the pattern failures. There's no log in the 'Discovery Log' table of what occurred during process detection, and no indication in the failure message of the HD Log that the pattern failed due to the running process having bounced with a new PID or PORT.

</td><td>

1.  Ensure access to the target server running the application instance.
2.  Run Discovery on the target server.
3.  Open the **Discovery Status** record.
4.  Wait for the Discovery to complete.
5.  Stop the service for the app running on the target server with **command sudo systemctl stop** after the ADM Probe ECC Queue Input is returned either.
6.  Open the ADM Probe ECC Queue Input record.
7.  Select the **Run Again** related link.
8.  Check the Discovery Status related list for Discovery Logs.
9.  Wait for the newest Pattern Log for the Application to return with an error for Failed Exploring Pattern.
10. Open the HD Log record.
11. Check the logging for why the pattern failed.
12. Check the Process Detection section before the Identification sections ran.

 Notice that commands executed that use the PID or the PORT discovered by the ADM Probe will return null, as they no longer exist on the target server. There's no logging to the Discovery Log table of what occurred during Process Detection.

</td></tr><tr><td>

Discovery

 PRB1681149

 [KB1500612](https://hi.service-now.com/kb_view.do?sysparm_article=KB1500612)

</td><td>

The Storage Server \(SMIStorageServer\) probe causes a MID server OutOfMemoryError

</td><td>

When running storage discovery, multiple SMIStorageServer probes are triggered. Each probe uses large amount of memory, eventually causing an 'OutOfMemoryError: Java heap space' error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1791510

 [KB1718735](https://hi.service-now.com/kb_view.do?sysparm_article=KB1718735)

</td><td>

Discovery is hanging for certain schedules due to WMI queries failing

</td><td>

 

</td><td>

Run Discovery on Windows devices where the WMI queries fail in Windows OS Patterns.

</td></tr><tr><td>

Discovery

 PRB1812384

 [KB2234218](https://hi.service-now.com/kb_view.do?sysparm_article=KB2234218)

</td><td>

Inclusion pattern discovery fails with a NullPointerException if one of the identifications fails for a parent pattern

</td><td>

When the main pattern identification a fails, a NullPointerException exception is thrown: 'com.snc.sw.exception. PatternDebuggerException: Debug task failed to initialize parent CI for entry point: null.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1843836

 [KB1821378](https://hi.service-now.com/kb_view.do?sysparm_article=KB1821378)

</td><td>

There must be guardrails/warnings for 'mid.sm.discolog. max\_object\_size' properties

</td><td>

Setting 'mid.sm.discolog.max\_object\_size' too high can lead to a ECC Queue payload too large and can cause an instance to run into memory errors when processing the results.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1843863

 [KB2061931](https://hi.service-now.com/kb_view.do?sysparm_article=KB2061931)

</td><td>

Shazzam Insights doesn't display any data in Discovery Admin Workspace

</td><td>

Shazzam Insights information isn't populated in the table 'Shazzam\_Insights' and an error appears in the system logs related to 'com.glide.util' usage.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Discovery

 PRB1874074

</td><td>

A slow query with the hash '874618095' is triggered from the script include 'ShazzamInsights'

</td><td>

There's a slow query with the hash '874618095' is triggered from the script include 'ShazzamInsights' while processing the event with the name 'discovery.complete'.

</td><td>

1.  Ensure that the discovery\_device\_history table has at least more than 50M records.
2.  Ensure that there isn't any index on the source column present in discovery\_device\_history.
3.  Set the property value glide.discovery.shazzaminsights value to true.
4.  Create a new discovery schedule with an IP range of 1k to 2k.
5.  Run the discovery.
6.  Check the shazzam\_status and shazzam\_summary tables for the records being created.
7.  Note the discovery completed event for the Shazzam Insights.
8.  Apply the defect.
9.  Run the schedule created in step 4.
10. Once the discovery completes, note down the discovery event for the Shazzam Insights.

 Observe that when comparing the two noted times, the discovery completed event of Shazzam insights is much less.

</td></tr><tr><td>

Document Management

 PRB1884923

</td><td>

Users can't preview or publish to a case, and a null pointer exception \(NPE\) is thrown: 'Cannot invoke "java.io. ByteArrayOutput Stream.toByteArray\(\)" because "pdfOS" is null: HtmlToPdf ConversionController'

</td><td>

In this process, if the HTML has images fetched from the db\_image table then shared service, it's unable to process it. In a few scenarios, it's throwing a NPE.

</td><td>

 

</td></tr><tr><td>

Document Management Services

 PRB1847231

</td><td>

There's a PDF error when scheduling reports with the donut or graph types on classic dashboards

</td><td>

Scheduled PDF type reports are failing for donut, graph, and bar chart report types.

</td><td>

 

</td></tr><tr><td>

Dynamic Translation

 PRB1875022

 [KB2033255](https://hi.service-now.com/kb_view.do?sysparm_article=KB2033255)

</td><td>

Users observe /&gt; tags when translating

</td><td>

A translation displays /&gt; tags instead of line breaks.

</td><td>

1.  Navigate to a Yokohama instance using Dynamic Translator.
2.  Open an incident or record with a translate option in the activity log.
3.  Select **Translate**.

 Observe that /&gt; prints.

</td></tr><tr><td>

Edge Encryption

 PRB1887439

</td><td>

In Yokohama, when a user goes through an Edge proxy with a home page that includes encoded characters such as %2f as a re-direction result after login, a 400 error occurs

</td><td>

When the user's default home page contains encoded characters, or is redirected to a URL with encoded characters, Edge throws a 400 error, blocking access to the home page.

</td><td>

1.  Use an Edge proxy in Yokohama.
2.  Add abel.tuter as a workspace\_admin and workspace\_user.
3.  Log in as abel.tuter through edge.
4.  Navigate to **Preferences**.
5.  Set the home page to **Default**.
6.  Log out.
7.  Log in as abel.tuter through Edge again.

 Observe the http 400 error.

</td></tr><tr><td>

Email Notifications

 PRB1764089

 [KB2191121](https://hi.service-now.com/kb_view.do?sysparm_article=KB2191121)

</td><td>

The display\_ name 'email address' set on 'Select From List' or 'text' of 'From Generation Type' doesn't work if the template is custom table based

</td><td>

When using two email templates, the oldest one gets 'error invalid' from the address when the email is sent. This error occurs when two email templates are on the same table but are from different addresses. Both email templates work if the 'from' address is set to the same value.

</td><td>

1.  Open a record in the Agent Workspace.
2.  Navigate to **Activity**.
3.  Select **Reply** on the most recently received email.
4.  Select the tab 'Popup email draft to new workspace'.
5.  Select **Email template**.
6.  Choose an email template.

 Notice the display\_ name format and the error message, 'The email address in the **From** field is invalid.'

</td></tr><tr><td>

Email Notifications

 PRB1778099

</td><td>

The inbound action **Update comments and attachments** doesn't account for email image filtering, and copies all attachments from the email

</td><td>

Email image filtering should filter out unwanted images smaller than a specific size, such as images in email signatures. Images and attachments should be filtered out based on the properties 'glide.email.inbound. image\_sys\_attachment. filter.action' and 'glide.email.inbound. image\_sys\_attachment. filter.minimum\_bytes'.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1815750

</td><td>

The instance doesn't generate the access token for push applications

</td><td>

 

</td><td>

1.  Log in to an instance.
2.  Navigate to the push application.
3.  Open any push application update the fields.
4.  Push as Direct and Google authentication type as HTTP V1.
5.  Try creating a new token.

 Expected behavior: The token is added to the instance.

 Actual behavior: It is throwing insert error.

</td></tr><tr><td>

Email Notifications

 PRB1878510

</td><td>

'Could not process unsupported sys\_attachment' isn't properly logged by sn\_sec\_cmn

</td><td>

When a user reports a phishing email with an unsupported attachment, the instance receives the email and discards the attachment without logging the issue properly. The issue is only logged in node logs even though it should properly be logged in the syslog\_email and sys\_email\_attachment tables.

</td><td>

 

</td></tr><tr><td>

Email Notifications

 PRB1881286

 [KB2074932](https://hi.service-now.com/kb_view.do?sysparm_article=KB2074932)

</td><td>

In Yokohama, recipients are no longer populated in Email Client and the Major Incident Recipient list when using JavaScript

</td><td>

The **Recipient** field should be populated with all recipients.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Event Management

 PRB1838597

 [KB1743614](https://hi.service-now.com/kb_view.do?sysparm_article=KB1743614)

</td><td>

Event Rule changes can cause event\_rule.update \_events to block system events processing, causing a performance issue in the instance

</td><td>

When Event Rules are inserted or updated, an 'event\_rule.update\_events' system event is fired in the default events queue to re-check any event records not yet covered by any previously existing event rule. The script action 'Update event rules for empty events/Update rules after deletion of ER' runs for the event, which processes batches of system events from the platform and other features. When an instance has a large number of em\_event records matching the new rule criteria, this causes a long running transaction. Events can take several minutes to process, blocking the 'Events process 0' job of the app node, delaying the processing of other important events that should be processed in near real time.

</td><td>

1.  Open an instance with Event Management installed.
2.  Insert, update, or delete an Event Rule in which there will be a considerable number of existing em\_event record that will match it.

</td></tr><tr><td>

Event Management

 PRB1840029

</td><td>

There's an out of memory error due to glide.db. DBLazyWriter

</td><td>

com.glide.db.DBLazyWriter causes an 'OutOfMemoryError: GC overhead limit exceeded' error.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1844087

</td><td>

SCOM Connector goes down sporadically and the configuration file content becomes blank

</td><td>

A SCOM Connector goes down with the following error: 'Error running SCOM client: The system cannot execute the specified program.SCOM connector failed. The system cannot execute the specified program'.

</td><td>

 

</td></tr><tr><td>

Event Management

 PRB1877169

</td><td>

Event Management Events in certain buckets are stuck in 'Ready' for hours after migrating

</td><td>

.

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

File-based Discovery

 PRB1843684

 [KB1779115](https://hi.service-now.com/kb_view.do?sysparm_article=KB1779115)

</td><td>

Since Xanadu, Discovery runs 'Fire FBD Probes for Java Processes' even though FBD discovery is turned off

</td><td>

Since FBD is turned off, it should not run any FDB probes.

</td><td>

1.  Provision a Xanadu instance with Discovery, SAMP, and File-based Discovery \(FBD\) installed.
2.  Set system property glide.discovery. file\_discovery.enabled=false to turn off FBD.
3.  Run discovery against a Windows server \(which may need to have java processes\).

 Expected behavior: Since FBD is turned off, it should not run any FDB probes.

 Actual behavior: The discovery\_log in the discovery\_status logs 'Fire FBD Probes for Java Processes', even though it doesn't actually fire any probes.

</td></tr><tr><td>

Flow Engine

 PRB1751544

 [KB1710818](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710818)

</td><td>

There's a change in behavior from V1 to V2 in handling JS arrays

</td><td>

This change in behavior causes the failure of a following REST step in a Surf action where the 'If\_Matches' header whose value is 'etag' isn't matching.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1818766

</td><td>

There's flow issues when rejecting an approval

</td><td>

The flow becomes problematic when the person who requested the approval is a non-admin and the approval is rejected by a non-admin user and goes to the 'Send Email' activity. The following are the problematic flows: Change - Cloud Infrastructure - Authorize, Change - Emergency - Authorize, Change - Normal - Assess, Change - Normal - Authorize, and Change - Unauthorized - Authorize.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1825217

 [KB1709497](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709497)

</td><td>

When applying inline scripting to pass the value in an input of a dynamic template, it's not working, and the field appears empty

</td><td>

When users create an action from scratch with one input of a dynamic template and apply inline scripting to pass the value to this input in the flow, it doesn't work.

</td><td>

Refer to the Jira spoke action 'create issue'.

</td></tr><tr><td>

Flow Engine

 PRB1828174

 [KB1709903](https://hi.service-now.com/kb_view.do?sysparm_article=KB1709903)

</td><td>

The 'Do-In-Parellel' branch remains in a 'Waiting' state after a MID action

</td><td>

The flow should go to a 'Complete' state after it returns from MID, but it remains in a 'Waiting' state with only one of the parallel branches having been executed.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1829297

</td><td>

Sub-flow updates aren't reflected in the parent flow

</td><td>

When a subflow updates a record which was passed to it as a reference type, those updates are available in the calling flow if the 'Wait for completion' checkbox is checked.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1832599

</td><td>

There's an unparsable date when a transform is applied on the 'Date/time' pill in a condition string

</td><td>

There's a strict type check for date comparison in V2, but the 'Year' transform applied on the date is giving the year as an integer, which is an unparsable date.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1834120

</td><td>

A flow variable is changed when the flow variable is set from values in MRVS

</td><td>

This issue occurs when there's three or more Date/Time variables used in MRVS. It arises when the smallest date among the entered variables is retrieved using a For Each loop and then set to a flow variable.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1840526

</td><td>

The **Submit Catalog Item Request** action fails if a multiline text variable is populated with a string containing '\\"'

</td><td>

Appears to be the same behavior as PRB1718202, but this affects multi-line text.

</td><td>

1.  Create a catalog item with a multi-line text variable.
2.  Create a subflow that accepts a string as an input and passes it to the multi-line variable when requesting a catalog item.
3.  Test the subflow using a string containing '\\"'.

</td></tr><tr><td>

Flow Engine

 PRB1846526

</td><td>

A scripted sub-flow behaves differently with a stage set in a parent flow for Flow Engine v2

</td><td>

If the user has a sub-flow that carries out a scripted action, there's a difference in execution when using Engine v2, which can interfere with previously published flows.

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1861062

</td><td>

A dot-walk in a custom action fails when executing on MID server

</td><td>

This is related to MID, since this works as expected if the flow is forced to move back to the instance, either by adding a lookup record or waiting before the action using the value is executed.

</td><td>

1.  Provision an instance with com.glide.hub.integrations installed.
2.  Have a valid MID server.
3.  Create an action that goes to MID.
4.  Create simple custom action that takes the 'Reference.User' as input.
5.  Add a log step that prints the sys\_id of that user.
6.  Create a flow that is triggered by incident record CRUD operation.
7.  Add the MID action created in 3.
8.  Add log action create in 4. The input for should be **Trigger** &gt; **Incident** &gt; **Opened By**.
9.  Run the flow with an incident that has a valid 'opened by' user.

 Expected behavior: The 'Opened by' user sys\_id is in the log.

 Actual behavior: The log is empty.

</td></tr><tr><td>

Flow Engine

 PRB1863274

 [KB2019495](https://hi.service-now.com/kb_view.do?sysparm_article=KB2019495)

</td><td>

There's a unique key violation error in Integration Hub steps when its ran in a loop

</td><td>

The error\_message key is written in to runtime values in case of a failure \(non-null error\_message ouptut\) in retryable integration operations. The duplicate key violation error is causing the flow context to terminate with an error when checked for errors during the OutputRepository.writeToDB call.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1874873

 [KB2042735](https://hi.service-now.com/kb_view.do?sysparm_article=KB2042735)

</td><td>

A deserialization issue occurs to flows when upgrading from Washington DC to Yokohama

</td><td>

Flows containing the 'Make a decision' logic don't resume and error out after upgrading to Yokohama. This is caused by a deserialization issue in Flow Engine V2, which prevents the flow from progressing.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flow Engine

 PRB1881084

</td><td>

The CurrentContext Tracker reset scope and meta stack are in the wrong order

</td><td>

CurrentContextTracker attempts to clean up meta stack and script contexts after a flow execution. Both are reloaded in reverse to how they initially appeared when the flow starts. This happens because the ArrayDeque collection removes elements from the stack. The array from the queue is in the expected order \(A, B, C, etc\). When the elements are added back, the ArrayDeque adds elements at the front of the queue, so iterating from first to last on the list and pushing will result in a reversed stack. So the queue contains \(C, B, A\) instead of \(A, B, C\).

</td><td>

 

</td></tr><tr><td>

Flow Engine

 PRB1888071

 [KB2153671](https://hi.service-now.com/kb_view.do?sysparm_article=KB2153671)

</td><td>

Deserialization issue with 'Make a decision'

</td><td>

When upgrading from a Washington DC to Yokohama instance, flow executions created with 'Decision' in both families don't resume and result in an error.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1774269

</td><td>

When a catalog item's flow has an 'Error' state set, the message 'Set current stage state to : \[Error\]' occurs upon submitting the item on the 'Request Summary' page

</td><td>

If a flow has the 'Error' state set, an item using that flow is submitted from portal and the error message, 'Set current stage state to : \[Error\]', occurs on the 'Request Summary' page.

</td><td>

1.  Open any flow that has the 'Service catalog' trigger.
2.  Add an 'Error' state within this flow.
3.  Open portal.
4.  Submit the item that uses this flow.

 Observe the message 'Set current stage state to : \[Error\]' on the Request Summary page; when the page is re-loaded, the message goes away.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1816646

</td><td>

The update number on the record remains the same when it is updated by the subflow and parent flow in sequence, causing inconsistencies in SLA executions

</td><td>

When the subflow updates the trigger record, and parent flow updates the same trigger record, the update number on the trigger record remains the same. This impacts respective SLA executions on the record.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1834406

</td><td>

App installation deletes the base instance sys\_complex\_object 'FDCollection'

</td><td>

Deleting the flow doesn't remove the sys\_complex\_object record from the source instance, but the app installation removed the record from the target instance. Sys\_complext\_object isn't listed in the application file of the app, but appears in the payload of the sys\_hub\_flow record.

</td><td>

1.  Navigate to any base instance.
2.  Create a scoped app.
3.  Create a flow \(sys\_hub\_flow\) with some actions, such as log.
4.  Confirm the sys\_id is being included in the flow.
5.  Check the payload of the captured flow from sys\_update\_xml.
6.  Delete the flow from the list view of sys\_hub\_flow.
7.  Confirm the deletion is captured in sys\_metadata\_delete.
8.  Published the scoped app to a repo or app store.
9.  Install the app from another instance from the app store.

 Notice that after the installation, the base instance sys\_complex\_object removes a sys\_id on the instance.

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1834495

</td><td>

On a save, a flow is sending extraneous/corrupt data to the backend

</td><td>

After upgrading to Xanadu, flows with extraneous/corrupt data are being exposed by the stricter v2 engine data model.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1841737

</td><td>

Users are unable to make changes to a flow after deleting a flow variable

</td><td>

The variable is broken once it is used as a reference in the **Send Email** action and later removed. The **Save** button is also turned off when trying to remove the variable.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1849882

</td><td>

The sysapproval\_ approver. source\_table changes after upgrading

</td><td>

The source table shows the child table after addressing PRB1780076. Before addressing PRB1780076, the source table showed the parent table.

</td><td>

 

</td></tr><tr><td>

Flows \(Family Channel\)

 PRB1887330

</td><td>

NaN output results in 'Exception while executing request: Could not deserialize value' when opening the flow execution

</td><td>

.

</td><td>

1.  Create a flow action.
2.  Configure an output for the action of type 'Floating Point Number'.
3.  Make the output NaN via javascript '0/0'.
4.  Add this action to any test flow.
5.  Execute the flow.

 All users see the error, and won't be able to see any flow execution details.

</td></tr><tr><td>

Form Builder

 PRB1820975

 [KB1987480](https://hi.service-now.com/kb_view.do?sysparm_article=KB1987480)

</td><td>

A form isn't saved on a cross scope in ServiceNow Studio

</td><td>

There's an error in the networking calls. When 'Form layout' is opened in the Form Builder, if the form belongs to a Xanadu scope while the session scope is set to Yokohama, a cross-scope banner appears. However, after selecting 'Edit in original scope' from the banner, any changes made in the Form Builder aren't saved.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Form Controller

 PRB1812174

</td><td>

The Glide form saves the previous date

</td><td>

 

</td><td>

1.  Provision an instance with the Project Workspace store app installed.
2.  Navigate to Workspace.
3.  Select **/project workspace**.
4.  Select any project.
5.  From the side panel, select **Status report**.
6.  Select the bottom **Create page** button.
7.  From the open Glide form, don't change anything on the form and submit.

 The report generates for the previous day.

</td></tr><tr><td>

FX Currency Conversion

 PRB1861950

 [KB1962510](https://hi.service-now.com/kb_view.do?sysparm_article=KB1962510)

</td><td>

Daily currency rates retrieval from European Central Bank \(ECB\) may fail due to a lack of response from an Online Certificate Status Protocol \(OCSP\) endpoint

</td><td>

The 'Retrieve System Rates' and the 'ECB Exchange Rate Load' jobs, which are used to capture currency exchange rates using the ECB endpoint, are failing intermittently across multiple instances because the OCSP endpoint for ecb.europa.eu isn't answering validity questions during certain times.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

GlideAggregate API

 PRB1827509

</td><td>

The Platform Analytics Experience Migration tool creates a dashboard data visualizations error: ''No data available' after migration'

</td><td>

When using the Platform Analytics Experience Migration tool to move a dashboard to the Platform Analytics Workspace, reports seem to break when using this tool. For certain reports, the Data Visualization returns the following message: '"No Data Available" There is no data available for the selected criteria'.

</td><td>

1.  Provision an instance with the latest sn\_par\_mig\_center plugin installed.
2.  Create a bar chart report.
3.  Create a dashboard using **Self-Service** &gt; **Dashboard**.
4.  Add the report from step 1 to the dashboard.
5.  Navigate to **Performance Analytics** &gt; **Migration Center** &gt; **Try with selected content**.
6.  Once it pulls up pa\_dashboards\_list.do, select the most recent dashboard with the report created in step 1.
7.  Select the newly created report.
8.  Select **Actions on selected rows...**.
9.  Select **Migrate Dashboard**.
10. Open the dashboard and observe the message: '"No Data Available" There is no data available for the selected criteria'.

</td></tr><tr><td>

GlideRecord

 PRB1796984

</td><td>

The event alert 'Inactive Delegator' triggers a message inserted into sys\_status, which can lead to a downstream impact as sys\_status isn't designed to contain thousands of records

</td><td>

There's a 'FAILED TRYING TO EXECUTE ON CONNECTION' error on select query results in a GlideRecord API return false when next\(\) is invoked. Subsequently an insert is invoked, and it succeeds. This resulted in excessive inserting of glide.policy.eventdelegator records into sys\_status. This results in the slow loading of xmlstats.do.

</td><td>

 

</td></tr><tr><td>

GlideRecord

 PRB1837475

</td><td>

There's a NullPointerException in GlideElement Compressed. setValue\(\)

</td><td>

Users may notice that upgrades may fail to populate details on the upgrade history when running the 'Upgrade summary' job.

</td><td>

 

</td></tr><tr><td>

Granular Delegation

 PRB1840636

</td><td>

Adhoc granular delegation isn't working on production

</td><td>

There's an error in the logs: 'Root cause of JavaScriptException: java.lang.NullPointerException: java.lang.NullPointerException: Cannot invoke "com.glide.delegation. DelegationRule.isApprovals\(\)" because "rule" is null: com.glide.delegation. ApprovalDelegationMapper .doesMapRule \(ApprovalDelegationMapper. java:46\)'.

</td><td>

 

</td></tr><tr><td>

GRC Platform Plugins

 PRB1843595

</td><td>

The **Details** field is missing in Attestation Designer after an Xanadu upgrade

</td><td>

.

</td><td>

1.  Navigate to Attestation Designer.
2.  Select the gear icon for any of the questions.

Observe that no **Details** field is present.

3.  View the same attestation designer in a Washington DC instance.

 Observe that the **Details** field is present.

</td></tr><tr><td>

Hermes \(Family\)

 PRB1834407

 [KB1818607](https://hi.service-now.com/kb_view.do?sysparm_article=KB1818607)

</td><td>

Reduce DB calls during initialization for Hermes

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

History Set

 PRB1844946

 [KB1923828](https://hi.service-now.com/kb_view.do?sysparm_article=KB1923828)

</td><td>

There's intermittent duplicate comments in an activity stream due to sys\_email records

</td><td>

Some comments are duplicated due to the presence of sys\_email records. This duplication occurs when a comment is added in a way that causes the incident's sys\_updated\_on timestamp to be one second earlier than the corresponding sys\_journal\_field record. If emails are triggered by the incident update, the loading of sys\_email records within the related sys\_history\_set interferes with the **last\_update\_recorded** field in sys\_history\_set. This disruption ultimately results in the duplication of the comment whenever the next update to the incident occurs.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery

 PRB1819942

 [KB1783588](https://hi.service-now.com/kb_view.do?sysparm_article=KB1783588)

</td><td>

HTML tags are seen in the **Description** field of an HR case

</td><td>

This issue occurs using a single method to populate both the rich **Description** field and the **Description** field.

</td><td>

Refer to the listed KB article for details.

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

 PRB1831691

 [KB2043348](https://hi.service-now.com/kb_view.do?sysparm_article=KB2043348)

</td><td>

HTML dynamic parameters on HR templates don't work as expected

</td><td>

There's an issue in Xanadu and Yokohama where HTML dynamic parameters aren't replaced with their actual values when used in links. The issue arises in the HTML-sanitizer enabled HTML and translated HTML fields during template replacement with HTML data.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

HR Service Delivery

 PRB1874464

</td><td>

The 'Suspended Reason' is overwritten with its previous value when the case moves from 'Draft' to 'Suspended state'

</td><td>

The issue is only reproducible when: the state moves directly from 'Draft' to 'Suspended', on HR Agent Workspace and not on UI16, and when the 'Suspended reason' \[sla\_suspended\_reason\] field is on the form.

</td><td>

1.  Log into an instance.
2.  Impersonate a system administrator.
3.  If the **Suspended reason** \[sla\_suspended\_reason\] field isn't on the HR Case 'Workspace UIB' view, add it to the form.
4.  Open HR Agent Workspace.
5.  Create an HR Case with the HR service 'General Inquiry'.

Notice how the **Suspended reason** field displays as 'User' but it's empty.

6.  Manually set the **State** field from 'Draft' to 'Suspended'.

A pop-up window displays.

7.  On the modal, set the reason to 'Group', add work notes.
8.  Select **ok**.

 Expected behavior: The 'Suspended Reason' should be 'Group'.

 Actual behavior: The 'Suspended Reason' is set to 'User'.

</td></tr><tr><td>

HTML Field Type Editor

 PRB1881482

</td><td>

Read-only HTML fields aren't rendering the content properly

</td><td>

Users are unable to see the content of the field. The field becomes read-only and no content appears.

</td><td>

1.  Navigate to any Yokohama instance.
2.  Ensure that the user preference for Next Experience is turned off.
3.  Type 'kb\_knowledge.do' in the filter navigator.
4.  Enter the text in the article body.
5.  Open the browser console and run the command: g\_form.setReadonly\('text',true\);.

 Expected behavior: The article body should be read-only and the content should appear.

 Actual behavior: The article body is read-only and the content doesn't appear.

</td></tr><tr><td>

Inbound Email Actions

 PRB1841147

</td><td>

Sensitive Data Redaction doesn't work for inbound email actions if 'Stop processing' is turned on

</td><td>

This issue impacts inbound email actions even if 'Stop processing' is turned on.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1775255

</td><td>

Increase the attachment limit in the SFTP step in Integration Hub

</td><td>

There's a hard-coded value of 100,000 KB for SFTP imports. When the user attempts to import more than the hard-coded limit, it fails. Even though it lets the user to set a limit, if it is higher than 100,000 KB, it isn't allowed.

</td><td>

 

</td></tr><tr><td>

Integration Hub

 PRB1834445

</td><td>

GCF Data Egress recorder should support 0 byte inputs

</td><td>

GCFDataEgressRecorder throws an error with an invalid event value when an event with 0 bytes is recorded, creating an error in the log.

</td><td>

Post to the instance on an endpoint.

 Notice that this returns an 204 \(no content\) zero byte response.

</td></tr><tr><td>

Interactive Filters

 PRB1837354

</td><td>

Filters no longer support reference list types

</td><td>

It used to be possible \(up until Xanadu\) to select 'Incident."Watch List"' as the data to filter in the filter configuration. This seems to no longer be possible.

</td><td>

 

</td></tr><tr><td>

Internal Platform Security Services

 PRB1813597

 [KB1790767](https://hi.service-now.com/kb_view.do?sysparm_article=KB1790767)

</td><td>

There's a MIME type check error when attaching a txt \(sjis code\) file after upgrading to Xanadu

</td><td>

MIME Type check error: '\[File type not permitted or mime type does not match the file content\]'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

JVM at Scale

 PRB1810485

</td><td>

Memory remediator is killing transactions and restarting glide

</td><td>

Notice the log 'low.memory.remediation.restart No transactions were cancelled' are on standby nodes only.

</td><td>

 

</td></tr><tr><td>

Knowledge Article Templates

 PRB1852356

</td><td>

Articles in the 'Published' state aren't changed to the 'Pending retirement' state when retired

</td><td>

Knowledge Base \(KB\) articles that have the retire policy set to 'Knowledge - Approval Retire' can't be changed to the state 'Pending review'. This problem is found in Yokohama.

</td><td>

1.  Locate any KB that has the retire policy set to 'Knowledge - Approval Retire'.
2.  Find any article in the 'Published' state within that KB.
3.  Select **Retire action**.
4.  Select **No** in the pop up dialog for the option to replace the current article with a new article.
5.  Return to the article.

 Notice that the workflow state hasn't been updated yet.

</td></tr><tr><td>

Knowledge Article Templates

 PRB1855083

</td><td>

Toolbar options and plugins for the TinyMCE editor are missing in the dictionary attribute for the Knowledge **Article body** field

</td><td>

Options like A11yChecker, Clear formatting, Anchor, and others are missing.

</td><td>

1.  Create or open any knowledge record.
2.  Notice that some of the TinyMCE toolbar options are missing in **Article body** field.

</td></tr><tr><td>

Knowledge Management

 PRB1819563

</td><td>

Some keystrokes aren't recognized when typing in the **Post Comment** field of a knowledge article, resulting in typing errors

</td><td>

The issue is intermittent.

</td><td>

 

</td></tr><tr><td>

Knowledge Management

 PRB1827639

</td><td>

Selecting a knowledge base from 'Explore our Knowledge Bases' in a portal redirects to the incorrect URL

</td><td>

A URL with incorrect search results is returned when selecting a knowledge base from /esc?id=kb\_home with AI Search enabled on the application 'Knowledge Management - Service Portal' version 1.0.0.

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

Language and Translations

 PRB1750563

</td><td>

The translation of notes is updated when installing the plugin sn\_doc

</td><td>

The record sys\_ui\_message.list notes is updated and translated when installing the plugin sn\_doc.

</td><td>

1.  Provision an instance with the the plugin com.snc.i18n.japanese installed.
2.  Open sys\_ui\_message.list.
3.  Find the record by searching the following:
    1.  Key: Notes
    2.  Language = ja
    3.  Message = メモ
4.  Install the plugin sn\_doc.

 Expected behavior: The record sys\_ui\_message.list isn't updated.

 Actual behavior: The record sys\_ui\_message.list is updated with the key, notes, and message values.

</td></tr><tr><td>

Language and Translations

 PRB1814149

</td><td>

'AND' isn't translated into Japanese in the list for Condition Builder

</td><td>

In Condition Builder, 'AND' is not translated in Japanese after upgrading from Washington DC to Xanadu.

</td><td>

1.  Install Washington DC.
2.  Enable the Japanese plugin.
3.  Navigate to **incident.list**.
4.  Switch the language to Japanese.
5.  Select **Show/Hide** filter icon.

Observe 'AND' is translated as 'および'.

6.  Upgrade the instance to Xanadu.
7.  Navigate to **incident.list**.

 Expected behavior: 'AND' is translated as 'および'.

 Actual behavior: 'AND' is shown as 'AND'.

</td></tr><tr><td>

Lifecycle Events

 PRB1881856

 [KB2208698](https://hi.service-now.com/kb_view.do?sysparm_article=KB2208698)

</td><td>

When a Lifecycle Event \(LE\) case is created directly in the 'Ready' state, the message 'Case reopened by...' is added to the work notes

</td><td>

This issue only happens in Yokohama and not in Xanadu.

</td><td>

Refer to the listed KB article for details.

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

 PRB1402594

 [KB0956006](https://hi.service-now.com/kb_view.do?sysparm_article=KB0956006)

</td><td>

Users are unable to edit a field in the list view when it is dependent on another field that is read-only for the user

</td><td>

This issue has been observed since New York. Users aren't able to edit a field on a list view when it's dependent on another field that is read-only or has an ACL making it read-only.

</td><td>

1.  Open any incident record.
2.  Set the field **Contact type** in the dictionary definition to be dependent on 'Configuration Item.Asset', which is read-only by default.

 Expected behavior: The field should not be editable only when there is a list\_view ACL preventing the field from being edited.

 Actual behavior: In the form view, the field 'Contact type' is editable, but in the list view it is not.

</td></tr><tr><td>

List Administration

 PRB1698906

 [KB1633481](https://hi.service-now.com/kb_view.do?sysparm_article=KB1633481)

</td><td>

The Workbench license consumption breakdown list view changes when the software product life cycle report changes

</td><td>

Editing columns in the Software Asset Workspace License Usage Report updates columns on the related lists.

</td><td>

1.  Log in to an instance.
2.  Navigate to the **Software Asset \(SAM\) Workspace**.
3.  Navigate to **License Usage** &gt; **Microsoft** &gt; **SQL Server** &gt; **Standard**.
4.  Select **License Metric Results**.
5.  Select the number link for the 'License required' column.
6.  Open the side view by selecting the number link for any 'License required' column.
7.  Select **Reports** **Software Product Lifecycle Report**.
8.  Change the column in the list view.
9.  Add some columns.
10. Refresh the License Consumption Details and Software Install Licensing.

 Notice that the details do not render in the table.

</td></tr><tr><td>

List Administration

 PRB1801160

 [KB1710229](https://hi.service-now.com/kb_view.do?sysparm_article=KB1710229)

</td><td>

In the calendar picker, the start of the week isn't the same on the Workspace list and form

</td><td>

Changing the day format to 'Monday to Sunday' doesn't work, and the 'start of the week' system property glide.ui.date\_ picker.first\_ day\_of\_week isn't honored.

</td><td>

1.  Navigate to any Vancouver instance.
2.  Create the following system properties:
    1.  glide.ui.filter.first\_day\_of\_week = 2
    2.  glide.ui.date\_format.first\_day\_of\_week= 2
    3.  glide.ui.date\_picker.first\_day\_of\_week = 2
3.  Navigate to the incident.
4.  Add a **Date** field.
5.  Attempt to edit it so the day format is from Monday to Sunday.
6.  Edit the day format to from Monday to Sunday on the Form.
7.  Open the CSM Configurable Workspace.
8.  Open any incident.
9.  Notice that the calendar the format is Monday to Sunday.
10. Open the incident in list view.
11. Add the date column.

 Notice that the format is Sunday to Saturday.

</td></tr><tr><td>

List Administration

 PRB1840299

</td><td>

The user is unable to dot-walk via column selection for lists

</td><td>

Dot-walking doesn't work in column editing.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1844708

</td><td>

Changes to 'My Lists' from the 'List' bundle SNC variant aren't saved

</td><td>

When the user creates a list under 'My Lists' in Service Operations Workspace and configures the columns or changes the filters, the changes reflect immediately. But if the user switches over to another page or list, the changes are reverted.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1862590

</td><td>

Non-admin users see ACL errors when using suggestions on form fields

</td><td>

Non-admin users who do not have sufficient access to the **sys\_choice** table fields encounter ACL errors when selecting the suggestion icon on a form field.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1865237

</td><td>

Checking 'Hide quick edit' in a UX List record doesn't hide the **Quick edit** button

</td><td>

After checking 'Hide quick edit' in a UX List record, the **Quick edit** button isn't hidden in Service Operations Workspace.

</td><td>

 

</td></tr><tr><td>

List Administration

 PRB1875957

 [KB2115689](https://hi.service-now.com/kb_view.do?sysparm_article=KB2115689)

</td><td>

The 'Personalize List' option isn't working as expected

</td><td>

When using the 'Personalize List' option, if users click anywhere on the list other than the slush bucket, the slush bucket disappears. This causes the list to get stuck, making it impossible to access any of the list elements such as filter, personalize, UI actions, or the contextual menu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Administration

 PRB1880653

</td><td>

After a Yokohama upgrade, special characters are incorrectly interpreted in a list when using 'show column filtering row' only in workspaces

</td><td>

The issue is reproduced only on Yokohama instances in list column header filters when using workspaces.

</td><td>

1.  Log in to any Yokohama instance.
2.  Navigate to any workspaces.
3.  Open any lists.
4.  Ensure that the list is enabled with 'show column filtering row'.
5.  Enter any special character in the search filter fields under any column.
6.  Notice the characters get converted to some other hard-coded characters.

 Expected behavior: Characters should remain the same and display list results based on characters matching.

 Actual behavior: Characters get converted to some other hard-coded characters. This issue is reproduced only when using workspaces and works fine in Platform UI.

</td></tr><tr><td>

List Administration

 PRB1881066

</td><td>

A list editor pop-up disappears as users scroll down on a dashboard/report

</td><td>

It's not working in the case of snListEditContainer, where a list is in some parent container.

</td><td>

1.  Log in to an instance.
2.  Create a list report on any table.
3.  Add it to a dashboard.
4.  Try editing a cell in the **Short Description** field.

 Notice that as users scroll down the list and attempt to edit additional cells, the selection context is lost, and some fields don't even populate the editable input, making it impossible to edit them.

</td></tr><tr><td>

List Controller

 PRB1847141

</td><td>

Lists in Service Operations Workspace \(SOW\) aren't automatically refreshing

</td><td>

When users enable the glide.lists.live\_ list\_enabled property and make any changes in any record of the list, then the list refreshes in SOW version 5.0.1 but not in version 6.1.1.

</td><td>

1.  Navigate to an instance.
2.  Open Service Operations Workspace version 6.1.1.
3.  Navigate to any list in the SOW.
4.  Select the record number, and make some change to the record that should be visible on the list.
5.  Save and close the record.
6.  Observe that the record still displays in the list without the changes that were just made.
7.  Open a new browser session in a different browser.
8.  Navigate to the same list and make a change.
9.  Save.

 Observe that the list on the first browser session doesn't change. Eventually, a number appears on the **refresh** button at the top of the list. Select the button, and the data refreshes.

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

List Editor

 PRB1842085

 [KB1803766](https://hi.service-now.com/kb_view.do?sysparm_article=KB1803766)

</td><td>

A 'Discard your changes?' modal displays when quick editing and the record was already saved

</td><td>

This issue isn't reproducible in Xanadu.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

List Filters

 PRB1764233

 [KB1706870](https://hi.service-now.com/kb_view.do?sysparm_article=KB1706870)

</td><td>

The 'Report' filter isn't working on the Workspace Dashboard when selecting 'View all'

</td><td>

This issue occurs in the CSM/FSM Configurable Workspace for Vancouver and Washington DC instances.

</td><td>

1.  Open any Washington DC or Vancouver instance.
2.  Ensure CSM/FSM Configurable Workspace enabled.
3.  Open the CSM/FSM Configurable workspace experience in UI Builder
4.  Add a **Simple list** widget or component to the body of landing page.
5.  Take the 'Incident' table as a reference.
6.  Add the following filters:
    1.  'Active=true'
    2.  'Priority is high'
7.  Add columns to display from the 'Default display' section under the configuration panel.
8.  Navigate to the 'Events' tab.
9.  Create event mapping with 'View all clicked'.
10. Create an event handler with 'link to destination'.
11. Use dynamic binding to bind data from the table.
12. Save the changes.
13. Navigate to the workspace landing page.
14. Check the count of incidents filtered on the widget.
15. Select **View all**.

 Observe that the count changes and the list containing all the incidents doesn't respect the filters.

</td></tr><tr><td>

List Filters

 PRB1801767

</td><td>

Japanese names can't be filtered by a Japanese term but can be filtered by an English term under the Japanese setting

</td><td>

Users are unable to filter lists by **Translated Text** fields in non-English languages when using the non-English translation.

</td><td>

 

</td></tr><tr><td>

List Filters

 PRB1818705

</td><td>

**Group By** tags are not working in extensible lists

</td><td>

The **Group By** column action won't be available for certain column types like 'Tags' \(internal\_type: related\_tags\). **Group By** tags works in UI16, but it's not supported in NRLC and **Group By** and filtering options are turned off.

</td><td>

1.  Log in to any instance.
2.  Navigate to the /now/lists-demo/record-list-bundle demo page.
3.  Edit columns to add a 'Tags' column.
4.  Inline edit and add tags to a few rows.
5.  Select the column action **Group By** for the 'Tags' column.

 Expected behavior: If **Group By** isn't supported for the 'Tags' column, the **Group by** column action shouldn't be available for 'Tags'.

 Actual behavior: It doesn't return results based on **Group by** for tags. Returns 'No data to display'.

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

Major Incident Management

 PRB1891876

</td><td>

The **View Workbench** UI action is redirecting to a broken 'Activity' section when opening it for a second time on a major incident form on the classic UI

</td><td>

After upgrading in Yokohama, when managing a major incident \(MI\) in the classic UI and moving to the 'Workbench' view, it's not loading properly. It's redirecting to a MI management broken activity view.

</td><td>

1.  Open any major incident.
2.  Select **View workbench**.

MI workbench loads.

3.  Select **View form**.
4.  Once the form is loaded, select **View workbench** again and wait.

 See that a different form view is loaded instead of workbench. It seems to be that the redirection URL is changing to this form view.

</td></tr><tr><td>

Metric Intelligence \(Family\)

 PRB1784201

</td><td>

'ITOM model building' jobs cause CPU spikes on Clotho, which causes processing metrics issues

</td><td>

A ITOM fitter class uses a parallel stream for model fitting, this parallel stream uses all the resources available in the JVM settings which causes CPU spikes and issues in the metric processing pipeline of Clotho.

</td><td>

 

</td></tr><tr><td>

MID Server

 PRB1777909

</td><td>

Container-based MIDs fail to upgrade from Utah or Vancouver to Washington DC

</td><td>

Since the Washington DC release, MID servers deployed through the docker recipe stop working when self-upgrading after each restart.

</td><td>

 

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

 PRB1842102

</td><td>

Session mismatch on MID server when an agent experiences VPN issues

</td><td>

Host data collection also fails with MID logs showing, 'Failed to send check instance check-discovery-basic due to closed communication session'.

</td><td>

1.  Use MID in the ITOM lab.
2.  Connect the agent to MID in ITOM lab.
3.  Disconnect the agent by disconnecting from the ITOM VPN.
4.  Reconnect the agent by reconnecting to ITOM VPN.
5.  Check the MID logs.

 Expected behavior: Notice the MID logs with the agent ID mapped to the message, 'Agent registered for communication', and the agent websocket session should be different than it was before it disconnected.

 Actual behavior: Notice the MID logs with the agent ID mapped to the message, 'Agent registered for communication', and the agent websocket session is the same according to MID logs.

</td></tr><tr><td>

MID Server

 PRB1864193

</td><td>

Upgrading a Linux MID Server to Xanadu reverts mid.shconf\_override to the default setting

</td><td>

mid.shconf\_override has an empty setting. It's reverted to default setting after upgrading.

</td><td>

 

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

MID Server

 PRB1912171

</td><td>

Yokohama MID Server upgrades do not upgrade all jar files in lib

</td><td>

Yokohama MID Server upgrades don't upgrade all jar files in lib, causing NoClassDefFoundError for various classes, and MID Server to go down.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1835448

</td><td>

Uppercase in the choice value breaks the dependency on the Mobile App

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Mobile Platform

 PRB1840375

</td><td>

InputFormScreen doesn't work when the function containing the InputFormScreen comes from a list

</td><td>

An InputFormScreen with Fetch Type = Prefetch/OnDemand doesn't display the dependent parameter of level three \(parameter3 depends on parameter2 which depends on parameter1\).

</td><td>

1.  Open the mobile \(requestor\) app.
2.  Log in to an instance.
3.  **Tap 'ALP List' tab** &gt; **'AppletList' section** &gt; **ListSegmentsWotInc**.
4.  Swipe left on item from the list.
5.  Choose 3LevelsParamsNotInline\_IFSPrefetch / 3LevelsParamsNotInline\_IFSOnDemand.

 Expected behavior: Choice three shows the option 'None', and when picking values in choice one and choice three, choice three shows the values configured to it.

 Actual behavior: Choice three doesn't show value at all, and when picking values in choice one and choice three, choice three does not show the values configured to it.

</td></tr><tr><td>

Mobile Platform

 PRB1843738

</td><td>

Field parameters for the URL button type that are used for the URL template are encoded even when it's not needed

</td><td>

When selecting the options on the Now Mobile app, the page doesn't navigate as expected. Instead, it is taken to a 'The page you are looking for could not be found' search screen. After selecting **Go**, the page is redirected correctly. Options: 'Open my Reservation » mesp?id=wsd\_reservations' and 'Create a new general reservation »mesp?id=wsd\_search'.

</td><td>

 

</td></tr><tr><td>

Next Experience Notifications Menu

 PRB1851718

</td><td>

A URL isn't updated when navigating from the migrated dashboard by clicking the notifications

</td><td>

There's an issue on the unified navigation side that is causing this for several releases.

</td><td>

1.  Navigate to pa\_dashboards.LIST.
2.  Select a dashboard.
3.  Choose **Migrate Dashboard** from the 'Actions' menu.
4.  Open the migrated dashboard from the message displayed on the top of the page.
5.  Search for the migrated dashboard and open it.
6.  Have a notification in the notification bell at the top-right hand corner of the Next Experience UI.
7.  Select the bell.
8.  Select the incident record in the notification list.

 Observe that while the record displays in the main window, the URL bar isn't successfully updated and the tab name is wrong.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1690651

</td><td>

Zing Exact Match search on workspaces intermittently navigates to an incorrect URL in Next Experience

</td><td>

Zing Exact Match search opens the record in the record view instead of the kb\_view.

</td><td>

1.  Log in to an instance in incognito mode.
2.  Ensure that Next Experience is enabled.
3.  Ensure that global and workspace searches are using Zing.
4.  Select **Service Operations Workspace** in the search context.
5.  Perform an exact match search for [KB0000001](https://hi.service-now.com/kb_view.do?sysparm_article=KB0000001).
6.  Notice that it should open the record in kb\_view.
7.  Wait for 5 to 10 minutes.
8.  Repeat the steps.

 Observe that the record opens in the record view.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1814384

</td><td>

Adding a parent application and child module to the configurable menu breaks the menu API

</td><td>

 

</td><td>

1.  Create a configurable menu.
2.  Add the application 'Benchmark' to the configured items of the menu.
3.  Add a child module of 'Benchmark' to the configured menu.

 Expected behavior: The API should return the menu items' response.

 Actual behavior: The API returns 500.

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

Next Experience Unified Navigation

 PRB1871341

</td><td>

Text is truncated in the 'leave page' pop-up in Next Experience after upgrading to Yokohama

</td><td>

The issue isn't happening on previous releases like Washington DC or Xanadu. The issue is also not happening with UI16 on the Yokohama release.

</td><td>

1.  Turn on Next Experience.
2.  Access the 'Basic Configuration UI16' module.
3.  Modify the value of 'Browser tab title' to a longer value.
4.  Select **Save**.
5.  Re-log in the instance to make sure the change take effect.
6.  Select **Create New** under the 'Incident' or 'Knowledge' module to create a record.
7.  Make some changes on the form.
8.  Select the **Back** arrow on the left-top of the form.

 Expected behavior: The 'Leave page' pop-up appears, which displays a completed message.

 Actual behavior: The 'Leave page' pop-up appears, but it displays a truncated message.

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1875808

</td><td>

The desktop notification banner doesn't display in Windows when multiple tabs are open

</td><td>

It displays the notification in the Notification Center but it doesn't display the banner.

</td><td>

 

</td></tr><tr><td>

Next Experience Unified Navigation

 PRB1908169

</td><td>

An exact match for an experience with an invalid routeConfigId doesn't navigate

</td><td>

A new issue was found which results in Zing search results aren't opening properly within a workspace.

</td><td>

 

</td></tr><tr><td>

Now User Experience

 PRB1890272

</td><td>

A custom banner logo for an instance doesn't display for unauthenticated users

</td><td>

A broken image icon displays on the 'Log in' page.

</td><td>

 

</td></tr><tr><td>

On-Call Scheduling

 PRB1868011

</td><td>

The 'Show Schedule' link doesn't work for a non-admin user

</td><td>

After upgrading to Xanadu, non-admin users aren't able to access the on-call schedule.

</td><td>

1.  Impersonate a non-admin user.
2.  Open any on-call schedule for the group.
3.  Select the 'Schedule' column for any schedule.
4.  Select the UI action **Show Schedule**.

 Observe that an error is thrown.

</td></tr><tr><td>

On-Call Scheduling

 PRB1886730

</td><td>

The 'On-call Who' API intermittently isn't returning users

</td><td>

 

</td><td>

 

</td></tr><tr><td>

OneExtend

 PRB1864500

 [KB2216882](https://hi.service-now.com/kb_view.do?sysparm_article=KB2216882)

</td><td>

Activating Now Assist skills creates unnecessary \[sys\_update\_xml\] records which shouldn't be transferred between instances

</td><td>

Unexpected customer updates are being automatically generated for one\_api\_\* tables extending \[sys\_metadata\]. This causes confusion among users as they are unaware of how the updates are generated and these records aren't intended to be transferred via an update set.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

PDF Generation

 PRB1890095

 [KB2184477](https://hi.service-now.com/kb_view.do?sysparm_article=KB2184477)

</td><td>

A PDF created from a view with dot-walked fields aren't displaying those fields or the exported PDF \(30B size\) is corrupted

</td><td>

When exporting a form, if the form contains dot-walking fields, then the value of those fields are empty in the exported PDF file. If the parent of the dot-walking field isn't present and dot-walking fields are present, then a corrupted PDF is generating with an error: 'Failed to load PDF document.'

</td><td>

1.  Navigate to a Yokohama instance.
2.  Find a record with dot-walked fields.
3.  Right-click the form header and export to PDF.

 Notice that the dot0walked fields **Model.model\_number** and **Model catergory.Name** aren't displaying. Also, if the parent of the dot -walking field is missing, then the corrupted PDF is generated with 30 bytes. The exported file \(30B size\) displays 'Failed to lad PDF attachment'.

</td></tr><tr><td>

Performance Analytics Dashboards

 PRB1900147

</td><td>

Users are unable to open responsive CoreUI dashboards

</td><td>

An error message appears: 'Sorry! The requested dashboard has not been shared with you.'

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1760775

</td><td>

There's an issue with reports on a workspace dashboard

</td><td>

Legends display duplicate values when translated into a non-English language.

</td><td>

1.  Provision an instance with the 'Install Platform Analytics workspace' plugin installed.
2.  Create a Platform Analytics dashboard with a column report with 2 data sources.
3.  Change the language to Brazilian Portuguese.

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1865224

</td><td>

The first modal displays despite 'Don't show...' being checked

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Platform Analytics Dashboard API

 PRB1909523

</td><td>

Changes in the dashboard only appear in the session language where they were made

</td><td>

Users are experiencing inconsistent behavior in Platform Analytics dashboards depending on the selected user language. When viewed in English, the dashboard reflects the latest updates. When switched to Italian, an outdated version displays, even after clearing the cache using cache.do.

</td><td>

 

</td></tr><tr><td>

Platform Analytics Filters

 PRB1838937

</td><td>

When a non-admin user creates a Platform Analytics 'Date' filter, 'Field' flashes briefly and is then cleared when selected, depending on the table chosen

</td><td>

Depending on the table chosen in the data to filter modal, entries selected in 'Field' flash briefly and are then cleared, and don't remain selected.

</td><td>

1.  Grant a non-admin user the analytics\_filter\_admin role.
2.  Impersonate the user.
3.  Navigate to **Platform Analytics** &gt; **Library** &gt; **Filters**.
4.  Select **New**.
5.  Navigate to **Filter Type** &gt; **Date** &gt; **Data to filter** &gt; **Add**.
6.  Select **Task** in the field **Table** in the Data to filter modal.
7.  Select **Created** under **Field**.

 Observe that 'Created' flashes briefly and is then cleared, and the selection does not remain.

</td></tr><tr><td>

Platform Runtime

 PRB1855493

</td><td>

Nodes are closing the TCP socket after 20 seconds of being idle and ignoring the property tomcat.connector.all. keepAliveTimeout, causing ADC to generate a HTTP 502 response

</td><td>

Application nodes are closing the TCP socket after 20 seconds of being idle and ignoring the property tomcat.connector.all. keepAliveTimeout, which is set to 70000 in the file '/glide/nodes/ NODE\_NAME/conf/ overrides.d/03-custom.properties'. This causes the ADC load balancer to generate an HTTP 502 response.

</td><td>

 

</td></tr><tr><td>

Playbooks \(Family Channel\)

 PRB1839341

 [KB1891818](https://hi.service-now.com/kb_view.do?sysparm_article=KB1891818)

</td><td>

An update set with a Playbook change failed to install

</td><td>

The invalid preview error, 'Could not find a record in sys\_pd\_snapshot for column snapshot referenced in this update' occurs when moving changes to related to Playbook via an update set from one instance to another.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Process Mining

 PRB1903878

 [KB2229304](https://hi.service-now.com/kb_view.do?sysparm_article=KB2229304)

</td><td>

After upgrading from the Xanadu to Yokohama release, process mining filter sets and scheduled tasks are deleted

</td><td>

During the upgrade from Xanadu to Yokohama, the process mining filter set conditions and scheduled tasks are being deleted. Due to a backend issue, the upgrade script execution unintentionally deletes saved filter sets and scheduled tasks of Process Mining Projects. This particularly affects configurations with 'transition filters' linked to scheduled tasks. Although no other user data was affected, this issue may disrupt functionality where the deleted filter sets or scheduled tasks were actively used.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Project Management

 PRB1829307

</td><td>

A project actual isn't populated in the resource aggregated monthly for October, though it's populated for September and November

</td><td>

A category project actual isn't populated in table resource\_aggregate\_monthly for October. It does populate for September and November. There's one record for a project actual in October. When looking in resource\_aggregate\_weekly, all project actual records are there.

</td><td>

1.  Open the resource aggregate monthly \[resource\_aggregate\_monthly\] table.

Only 1 record displays under the monthly table and it excludes the month of October.

2.  Check in resource aggregate weekly \[resource\_aggregate\_weekly\].

Records are displayed as expected including the month of October.


</td></tr><tr><td>

Project Management

 PRB1850637

</td><td>

Duplicate resource\_aggregate\_weekly and resource\_aggregate\_monthly records are created intermittently

</td><td>

Code in the UpdateActualsFromTimeCard function of the ResourceActuals SI raises an event to update aggregates for each day when a time card is approved or recalled, causing duplicate resource\_aggregate\_weekly and resource\_aggregate\_monthly records to be created intermittently.

</td><td>

 

</td></tr><tr><td>

Project Management

 PRB1880926

</td><td>

The **Overall health** field and other related fields aren't displaying as per the option selected on the project status report on a project form

</td><td>

For example, when selecting values in the **Overall health** field, the color should be displayed as per the value selected.

</td><td>

 

</td></tr><tr><td>

Related Lists

 PRB1884173

</td><td>

Users can't add/remove the first option in the slushbucket from side to side when accessibility is enabled in Classic \(Core UI\)

</td><td>

Users can't move the first 'Available' option to the 'Selected' side with a double-click or by using the **Add** button. Selecting one option but then double-clicking another moves both over. If users shift-click to select multiple options, they don't all move over - one remains. CTRL+A doesn't select all options; rather, it appears to toggle the set of selected options.

</td><td>

 

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

Reporting

 PRB1324625

 [KB0855859](https://hi.service-now.com/kb_view.do?sysparm_article=KB0855859)

</td><td>

Stack trace error 'No matching records: com.glideapp.report. charting\_v2. exceptions. ChartDataGenException' is thrown when no data is returned for a multi-level pivot report

</td><td>

When a multi-level pivot report doesn't have any data to return, the following error is logged to the syslog table: 'No matching records: com.glideapp.report.charting\_v2.exceptions. ChartDataGenException: No matching records...'

</td><td>

1.  Create a new report with the following values:
    1.  Source Type: Table
    2.  Table: Incident
    3.  Type: Multi-level pivot table
    4.  Select Columns: Active to Incident table
    5.  Select Rows: Assigned to
2.  Open the filter conditions.
3.  Add the following filter to ensure zero rows are returned:
    1.  Created
    2.  After
    3.  Today
4.  Run the report.

 Expected behavior: The error message appears, 'Cannot generate the report. No matching records'.

 Actual behavior: The error message appears on screen, 'Cannot generate the report. No matching records' and an error is generated in syslog table: 'No matching records: com.glideapp.report.charting\_v2.exceptions. ChartDataGenException: No matching records...'.

</td></tr><tr><td>

Reporting

 PRB1853349

</td><td>

Visualizations in non-global domains aren't displayed in the list of visualizations

</td><td>

When trying to add some dashboard to a library, it's not saved in any sub domains. It's getting saved only in the global domain. In the sub domains, when they try to save the dashboard, it says it's saved but it's not.

</td><td>

 

</td></tr><tr><td>

Reporting

 PRB1874881

</td><td>

A calendar report doesn't display Japanese characters correctly

</td><td>

The issue is reproducible in Yokohama.

</td><td>

1.  Create a record on the vtb\_task table with short description '保守：YokohamaへVerUpリグレ開始'.
2.  Create a CoreUI Calendar report based on the vtb\_task table and the **Updated** field.
3.  On the Calendar report, Japanese characters aren't displayed correctly.

 Expected behavior: '保守：YokohamaへVerUpリグレ開始'.

 Actual behavior: '20:36 保守&amp;\#xff1a;YokohamaへVerUpリグレ開始 - 保守&amp;\#xff1a;YokohamaへVerUpリグレ開始'.

</td></tr><tr><td>

Reporting

 PRB1878029

 [KB2046103](https://hi.service-now.com/kb_view.do?sysparm_article=KB2046103)

</td><td>

A drill down report isn't working as expected with sorting added to the report

</td><td>

It's impacting the filter conditions by appending 'ORDERBY' at the beginning of the condition value to the last filter condition of the report.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Reporting

 PRB1881863

 [KB2064621](https://hi.service-now.com/kb_view.do?sysparm_article=KB2064621)

</td><td>

Drilling down into a multi-level pivot report that is following an interactive filter isn't working as expected

</td><td>

Multi-level pivot report drill down functionality isn't working as expected when a report is added to a dashboard or when a report has 'Follow Interactive Filter' turned on for the 'Report' widget.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Reporting

 PRB1892235

</td><td>

When accessing scheduled reports, users are getting an error

</td><td>

When accessing scheduled reports, users get the error: 'Part of the query on par\_coreui\_migration \_bridge\_sysauto has been ignored because of insufficient access for 'query\_match' operation' for non-admin users.

</td><td>

 

</td></tr><tr><td>

Role Delegation

 PRB1828712

 [KB2248225](https://hi.service-now.com/kb_view.do?sysparm_article=KB2248225)

</td><td>

Updating sys\_user\_group.parent is done on the frontend, which causes a timeout of the transaction and leaves sys\_group\_has\_role inconsistent

</td><td>

Since updating sys\_user\_group.parent is done on the front side, a transaction can timeout. As the result, the sys\_group\_has\_role records become inconsistent.

</td><td>

Refer to the listed KB article for details.

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

sn\_samp. UpdateReclamation Candidates &gt; getUser SubscriptionCost code issue

</td><td>

The **potential\_savings** field is only present on the samp\_sw\_ reclamation\_candidate table, and not in samp\_sw\_rc\_m2m\_subscription. This is causing the 'SAM - Updating Existing Reclamation Candidates' job to fail when updating the hybrid subscription cost.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Scheduled Jobs

 PRB1794747

</td><td>

The **Updated** field on the 'Progress workers' table isn't updating after a node restart

</td><td>

The **Updated** field on the 'Progress workers' table isn't updated when the node on which the job is executing gets restarted.

</td><td>

1.  Log in to any instance after the Vancouver release.
2.  Trigger a fix script to run the script in the background.
3.  Restart the node on which the fix script job is running.

 Notice the log: '2024-08-15 04:11:21 \(685\) worker.5 worker.5 txid=5827be15c30c JobExecutor Starting: Fix Script: Test: Script.8427fa15c30c961044093806050131d2, Trigger Type: Once, Priority: 25, Upgrade Safe: true, Repeat: Name: Fix Script: Test: Script Job Context: . . 2024-08-15 04:16:03 \(189\) glide.scheduler SYSTEM SchedulerThread \[Scheduler Graceful Shutdown\] Shutting down thread...No database connection pool available for name glide org.mozilla.javascript.JavaScriptException: java.lang.IllegalStateException: No database connection pool available for name glide'. Notice that the progress worker state is changed to 'Cancelled' but the **Updated** field is not updated. Review if the 'Update hung running progress controllers on startup' job has run. Notice that is the 'Update hung running progress controllers on startup' job has run, it updates the progress worker records.

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

Seismic Framework

 PRB1878687

</td><td>

Users are getting an error message on a few instances sometimes: 'An Unknown Error Occurred, Please try after sometime'

</td><td>

User accessible roles are fetched and used further to determine the 'Run with Roles' list. This issue is due to a large payload size. The qualifier string is big.

</td><td>

1.  Enable flow generation.
2.  Enable image2flow skill.
3.  Navigate to the Workflow Studio homepage.
4.  Create a flow with an image.
5.  Navigate to the homepage.

 A user can see the 'An Unknown Error Occurred, Please try after sometime'. This is not happening all the times.

</td></tr><tr><td>

Server-side scripts

 PRB1794568

 [KB1699139](https://hi.service-now.com/kb_view.do?sysparm_article=KB1699139)

</td><td>

Xanadu ES12 JavaScript in global scope isn't working for fix scripts and fails with a 'Script compilation error'

</td><td>

Apart from 'const' and 'let', no new ES features seem to be working. There's a script compilation error: 'Script Identifier: null.null.script, Error Description: syntax error \(null.null.script; line 4\), Script ES Level: 0, Interpreted Mode: true'. This issue doesn't exist in scoped apps.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Server-side scripts

 PRB1848232

</td><td>

A TD instance hangs and is unresponsive due to recursive calls when capturing Generic Collection Framework \(GCF\) metrics

</td><td>

While publishing the GCF metrics for scripts, MInMaxPriorityQueue is used for collecting 20 longest executions. It attempts to access indices more than 20, causing ArrayIndexOutofBound exceptions.

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

Service Catalog

 PRB1761951

</td><td>

An error in AI Search occurs, 'ERROR \*\*\* dot-walk column doesn't exist sc\_cat\_item.ref \_sc\_cat\_item\_content. content\_type'

</td><td>

After upgrading the instance to Washington DC, an error occurs in the system log: 'SEVERE \*\*\* ERROR \*\*\* dot-walk column doesn't exist sc\_cat\_item.ref \_sc\_cat\_item\_content. content\_type'.

</td><td>

 

</td></tr><tr><td>

Service Catalog

 PRB1857685

</td><td>

g\_user.userID isn't returning a string but a native object in the Virtual Agent conversational catalog item

</td><td>

It gives an error.

</td><td>

 

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

ServiceNow Security Center \(Family Release\)

 PRB1843476

</td><td>

At upgrade time with updated content, the completed steps of a user action keeps the action status as 'ready', which turns off the action's **Complete** button

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Service Portal Core Widgets

 PRB1862176

</td><td>

Service Portal fails to a submit catalog item when a required HTML variable is empty and re-submitted with a filled value

</td><td>

After pressing 'Submit' on a Service Catalog Item widget when the required HTML variable is empty, it rejects the submission as expected. However, filling the HTML variable after the submission is rejected and still detects the HTML variable as not filled. Because of this, users are only able to submit catalog items from Service Portal when the required HTMl variables are filled properly before submission.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1502280

 [KB0994649](https://hi.service-now.com/kb_view.do?sysparm_article=KB0994649)

</td><td>

The file attachment field doesn't appear on a Portal 'form' page

</td><td>

The file attachment field **My file** doesn't appear on the 'form' page of an incident record.

</td><td>

1.  Log in as an admin user.
2.  Open the form page of the incident record.

 Notice that the file attachment field **My file** doesn't appear on portal, but shows in native view.

</td></tr><tr><td>

Service Portal

 PRB1537370

</td><td>

Field messages styling \(using showFieldMsg\(\)\) for types of errors isn't consistent between Portal and Platform

</td><td>

The use of showFieldMsg\(\) to display the error type isn't consistent between the Portal and Platform views. On the Platform view, the error is displayed in a red background. However, in Portal, the error is displayed as a red string in italic form without a red background.

</td><td>

1.  Open any service catalog item.
2.  Add three new variables to test the field message for info, warning, and error.
3.  Create an onLoad catalog client script.
4.  Add the following field messages to each of the three variables for info, warning, and error:
    1.  Info: g\_form.showFieldMsg\('var1', 'info msg', 'info'\)
    2.  Warning: g\_form.showFieldMsg\('var2', 'warning msg', 'warning'\)
    3.  Error: g\_form.showFieldMsg\('var3', 'error msg', 'error'\)
5.  Navigate to the catalog item in the portal.

 Expected behavior: The styling of the field messages is same for info, warning, and error.

 Actual behavior: The styling of the field message for error is different from info and warning, and there's no background color for the error message.

</td></tr><tr><td>

Service Portal

 PRB1765867

</td><td>

The 'Widget' form throws an error when trying to save

</td><td>

An error appears after attempting to save changes to the 'Widget' form.

</td><td>

1.  Navigate to the 'Widget' form.
2.  Modify the **Roles** field, such as adding the user\_admin role.
3.  **Save** the changes.

 Expected behavior: The form should save successfully.

 Actual behavior: An error is seen under the **Client controller** field: 'Could not save record because of a compile error: JavaScript parse error at line \(25\) column \(25\) problem = missing name after . operator \(; line 25\)'.

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

 PRB1839297

 [KB1925168](https://hi.service-now.com/kb_view.do?sysparm_article=KB1925168)

</td><td>

A SPEntry page error 'Execute operation on script include 'SPEntryPage'' from scope occurs

</td><td>

Switching the scope and refreshing the page gives the error, 'Execute operation on script include 'SPEntryPage' from scope 'Knowledge Management - Service Portal' was denied'.

</td><td>

1.  Log in to a Xanadu instance.
2.  Create the glide.entry.first. page.script system property.
3.  Give it the value: new SPEntryPage\(\) .getFirstPageURL\(\).
4.  Make 'Knowledge Management - Service Portal' as the current scope.
5.  Refresh the browser page.
6.  Notice the error, 'Execute operation on script include 'SPEntryPage' from scope 'Knowledge Management - Service Portal' was denied. The application 'Knowledge Management - Service Portal' must declare a cross scope access privilege. Please contact the application author to update their privilege requests.'
7.  Repeat step 2 and step 3 with the scopes 'CI Landing Experience' and 'Conversational Interfaces - Diagnostics'.

 Notice that the same error message occurs.

</td></tr><tr><td>

Service Portal

 PRB1854147

</td><td>

'Popular Items' display a blue font on the SWP Portal

</td><td>

Popular items display a blue font and are a larger size after the Xanadu upgrade.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1855070

</td><td>

Post-upgrade to Yokohama EA, an error is caused by the business rule 'Create SP Communication ChannelList'

</td><td>

An error found in the logs after upgrading to Yokohama EA 'Recursive business rule call for 'Create SP Communication ChannelList' on sp\_portal'. A number of simple transaction results in this error.

</td><td>

 

</td></tr><tr><td>

Service Portal

 PRB1875043

</td><td>

In the 'Canada - French' language, submitting a date in 'dd-MM-yy' format causes an error

</td><td>

When a user sets their language to 'Canada - French' and attempts to submit a date in the format 'dd-MM-yy', the date doesn't apply correctly, resulting in an error.

</td><td>

1.  Install the plugin com.snc.i18n.french-canada \(French - Canada\).
2.  In the instance, navigate to **All** &gt; **Basic Config** &gt; **Date Format**.
3.  Set the system date format to 'dd-MMM-yy'.
4.  Mark the 'Sample Item' catalog item as active.
5.  Assign it a category so it displays in the service catalog for users.
6.  Set the date variable to 'mandatory'.
7.  Navigate to the /sp \(Service Portal\).
8.  Search for 'Sample Item'.
9.  Ensure that the language is set to French - Canada.
10. Fill in the date variable.
11. Submit.

 Observe that there's an error, and the date doesn't apply to the field.

</td></tr><tr><td>

Session Management

 PRB1704076

 [KB1645930](https://hi.service-now.com/kb_view.do?sysparm_article=KB1645930)

</td><td>

XMLStates can throw an 'Attempt to use GlideSession owned by another thread' error while retrieving statistics related to sessions

</td><td>

Statistics related to GlideSessions iterate over all the sessions and access gs.getClientDataMap\(\), which throws the 'Attempt to use GlideSession owned by another thread' error at the same time the user claims ownership of the session while running the transaction.

</td><td>

Refer to the listed KB article for details.

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

Sidebar \(Family Release\)

 PRB1849937

 [KB2131098](https://hi.service-now.com/kb_view.do?sysparm_article=KB2131098)

</td><td>

When sn\_hr\_core. impersonateCheck is set to true, users are unable to add users to the sidebar

</td><td>

When sn\_hr\_core.impersonateCheck is set to 'true', users can't add users to the sidebar discussion for sn\_hr\_core\_case\_payroll records. There's instead an error message: 'Participants can't join the discussion because they don't have access to this record.'

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1632141

 [KB1346310](https://hi.service-now.com/kb_view.do?sysparm_article=KB1346310)

</td><td>

The scheduled job 'SAM - Normalize discovery models using content library rules' fails when the Content Data Service \(CDS\) library is not complete

</td><td>

The scheduled job 'SAM - Normalize discovery models using content library rules' fails with the following errors: '08:14:33.158 Warning worker. 1 worker.1 txid= 9df7afed1b47 WARNING \*\*\* WARNING \*\*\* Get for non-existent record: samp\_sw\_package: 78a1f708db96ef0 0c41a10825 b9619c4, initializing 08:14:33.159 Error worker.1 worker.1 txid=9df7afed1b47 SEVERE \*\*\* ERROR \*\*\* NormalizationEngine: Error: No Match found for in samp\_sw\_publish'.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management

 PRB1794370

 [KB1699116](https://hi.service-now.com/kb_view.do?sysparm_article=KB1699116)

</td><td>

Deprecated fields are not deactivated

</td><td>

There are various fields across Software Asset Management which are deprecated but not deactivated.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Management Publisher Pack for Microsoft

 PRB1871730

</td><td>

The 'Collect CAL Info' extension section causes a huge payload for Windows discovery

</td><td>

When running Windows OS - Servers patterns, if the server has a large amount of records in the MsftUal\_DeviceAccess and MsftUal\_UserAccess through WMI queries, then the payload is substantial. Such large payloads may cause mutex locks and impact performance.

</td><td>

Run discovery against a Windows server with a large number of devices/users returned from the WMI queries in the 'Collect CAL Info' extension section.

</td></tr><tr><td>

Software Asset Normalization

 PRB1847748

 [KB2020463](https://hi.service-now.com/kb_view.do?sysparm_article=KB2020463)

</td><td>

Sometimes Norm product/publisher isn't cleared/stamped on a few installs

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Software Asset Reclamation

 PRB1896341

 [KB2171072](https://hi.service-now.com/kb_view.do?sysparm_article=KB2171072)

</td><td>

There's reclamation candidate and reclamation rule issues

</td><td>

 

</td><td>

Refer to the listed KB article for details.

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

Standard Change Catalog

 PRB1856886

 [KB1931818](https://hi.service-now.com/kb_view.do?sysparm_article=KB1931818)

</td><td>

A value isn't populated from the template if a new text area field is added when creating or modifying a standard change proposal

</td><td>

The **template\_value** field contains 'STARTSWITH' instead of the '=' operator, which doesn't allow the field to be populated with the value when the template is applied to the change request record.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

System Archiving

 PRB1815571

</td><td>

Archive runs can be stuck in an active state when the process times out when creating ar\_\* tables

</td><td>

Archive runs can be stuck in active state when the archive rule on CMDB is run for the first time and if the CMDB hierarchy is big. While creating all the ar\_\* table in this hierarchy, it could timeout.

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB1753408

</td><td>

The 'Import Set Deleter' job is contributing to replication lag due to long running DELETE statements and batch executions

</td><td>

.

</td><td>

 

</td></tr><tr><td>

System Import Sets

 PRB1804838

 [KB1705523](https://hi.service-now.com/kb_view.do?sysparm_article=KB1705523)

</td><td>

New fields with double byte characters aren't created automatically on loading data

</td><td>

If the loading file or data source contains headers that don't match the fields in the import set table, when loading data, new fields are created. Since the Xanadu release, new fields aren't created when headers contain double byte characters, and a warning message is logged in the import log. This occurs even if the com.glide.use\_ column\_name \_optimizer property is 'true'.

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

</td></tr><tr><td>

Table Administration and Data Management

 PRB1681343

</td><td>

convertToPDF WithHeaderFooter is slow to convert with a business rule

</td><td>

.

</td><td>

 

</td></tr><tr><td>

Table Administration and Data Management

 PRB1852726

 [KB2068808](https://hi.service-now.com/kb_view.do?sysparm_article=KB2068808)

</td><td>

Users get an error: 'Syntax Error or Access Rule Violation detected by database \(\(conn=316832\) Unknown column 'ba.a\_ref\_10' in 'on clause'\)'

</td><td>

 

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Tags

 PRB1767453

</td><td>

The 'Group by' tag list view count isn't accurate

</td><td>

The 'Group by' tag in the list view count isn't accurate on the 'Task' table when a tag is added to newly created records from a custom extended table.

</td><td>

1.  Open a Vancouver instance.
2.  Navigate to **System definition** &gt; **Tables**.
3.  Create a new table with the following example:
    1.  Label: Adhoc ticket
        1.  Name: u\_adhoc\_ticket
        2.  Extends table: Task
    2.  Navigate to the 'Controls' tab:
        1.  Prefix change to: AR
        2.  Create access controls: True
        3.  User role: itil
    3.  Navigate to the 'Application Access' tab:
        1.  Create, update, read: True
        2.  Allow access to this table via web service: True
        3.  Allow configuration: True
4.  Save the table.
5.  Add the 'test' tag on a newly created record.
6.  Navigate to the 'Task' table.
7.  Choose two records from the table.
8.  Group the 'Task' table the by **Tags** field.

 Expected behavior: The group counter amount is the same as the number of records in the list.

 Actual behavior: The group counter is two even though there are three records in the list.

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

Transaction Logs

 PRB1827610

</td><td>

The errors and logs metrics were removed in the XMLStats servlet include, causing the 'Logs' graph in the ServiceNow Performance dashboard to be 0 after an upgrade

</td><td>

When the user goes to ServiceNow Performance Dashboards, some of the graphs aren't displayed, and instead display the error message 'Error:Invalid series data'.

</td><td>

1.  Create a base Vancouver instance.
2.  Navigate to the ServiceNow Performance dashboard.
3.  Let the instance run until a non-zero number in the 'Errors and Logs' metric graphs.
4.  Upgrade the instance to Washington DC.
5.  Look at the 'Errors and Logs' metric graphs again after the upgrade is complete.

 Expected behavior: The graph should display values accordingly.

 Actual behavior: The graph flatlines at 0.

</td></tr><tr><td>

UI Actions

 PRB1879023

</td><td>

A workspace modal with an HTML field doesn't render in Yokohama

</td><td>

When using g\_modal.showFields\(\) in a UI action to populate the modal from the workspace, the modal doesn't appear if it has an 'html' type field defined.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1779043

</td><td>

There's an error inputting a decimal value into a decimal field when glide.system.locale has a value set

</td><td>

This issue is reproducible on any workspace and when the system property glide.system.locale isn't empty.

</td><td>

1.  Log in to an instance.
2.  Navigate to Agent Workspace.
3.  Open any incident.
4.  Enter '123456789.09' on the **Test** field.
5.  Select out of the field.

 Notice that the message is seen: 'Could not parse 123.456.789,6 as a number'.

</td></tr><tr><td>

UI Field Administration

 PRB1791024

</td><td>

The getSelectedOption breaks for records with some script type fields

</td><td>

.

</td><td>

 

</td></tr><tr><td>

UI Field Administration

 PRB1821427

</td><td>

An instance runs out of memory when there's unexpected wiki markup table syntax inside of a **wiki** text field

</td><td>

When creating a kb\_knowledge record on a form with the **wiki** field showing, the node runs out of memory.

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

 PRB1877769

 [KB2182152](https://hi.service-now.com/kb_view.do?sysparm_article=KB2182152)

</td><td>

The info \(i\) icon for reference catalog variables is missing on requested items and the 'SCTASK' form under Service Operations Workspace

</td><td>

The issue is seen with all the workspaces since Yokohama.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Field Administration

 PRB1879955

</td><td>

The sys\_user record isn't retaining the phone number format on the **Phone number** type fields

</td><td>

 

</td><td>

1.  Navigate to any Yokohama instance.
2.  Ensure that the glide.ui.format\_phone property is set to false.
3.  Open any sys\_user record.
4.  Update the **Mobile phone** field with a value.
5.  Save the record.

 Expected behavior: The value in the field shouldn't get formatted.

 Actual behavior: The value in the field gets formatted.

</td></tr><tr><td>

UI Field Administration

 PRB717514

 [KB2092173](https://hi.service-now.com/kb_view.do?sysparm_article=KB2092173)

</td><td>

A dotwalked **glide\_list** field with choices doesn't display dropdown choices

</td><td>

Users are unable to adjust/administer a list as expected.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UI Form Administration

 PRB1814991

</td><td>

A bulk-edit pop-up form in a presentational list won't refresh after the previous transaction

</td><td>

The bulk-edit UI action pop-up form contains input from the **Description** field from a previous transaction to other records that are opened.

</td><td>

1.  Navigate to **UI Builder** &gt; **Service Operations Workspace**.
2.  Add a variant to the List.
3.  Select **List Page Template** in the Template Picker.
4.  Ensure the new variant has a smaller order than the existing one, so it becomes the default list.
5.  Navigate to **Workspace** &gt; **Service Operations Workspace** &gt; **List** &gt; **Incident** &gt; **All**.
6.  Select any record.
7.  Select the **Edit \(1\)** UI action.
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

 PRB1824242

</td><td>

The **Add/remove multiple** button on list fields doesn't work if required fields are present

</td><td>

When selecting the **Add/remove multiple** button in a **glide\_list** type field while there are other required fields on the form \(that are not filled in\) the slushbucket popup doesn't open and all required fields flash red. This includes the list collector itself \(if it is mandatory\).

</td><td>

1.  Open an instance.
2.  Open incident.LIST or any table.
3.  Open a record.
4.  Clear text from one of the mandatory fields.
5.  Select the **Add/Remove multiple** button.

 Observe that this throws an error.

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
12. Close the 'Related Record' tab.
13. View the interaction records.
14. Notice that the values are cleared.

 Expected behavior: The updated values in the interaction record shouldn't be cleared after opening multiple tabs.

 Actual behavior: The updated values in the interaction record are cleared after opening multiple tabs.

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

 PRB1847059

</td><td>

Formatting on the special handling notes header is aligned to the left in Xanadu

</td><td>

Special Handling Notes aren't aligned properly and is formatted completely to the left.

</td><td>

 

</td></tr><tr><td>

UI Form Administration

 PRB1859837

</td><td>

UX View Rule Configuration isn't applied in the Workspace when a record is opened from a reference field

</td><td>

UX View Rule Configurations aren't applied when a record is opened in a Workspace from a reference field on a form, but when opening the same record from a related list in a Workspace, the UX View Rule Configuration is applied.

</td><td>

1.  Open a cmdb\_ci\_computer table.
2.  Create a custom view.
3.  Create a Workspace view rule on the sysrule\_view\_workspace table with the values:
    -   Table: cmdb\_ci\_computer
    -   View: Use the Custom View created
    -   Experience Restricted: Uncheck
    -   Workspace: Empty
    -   Execution Order: 1
4.  Create a UX View Rule Configuration on the sys\_ux\_view\_rules\_configuration table with the value:
    -   Active: True
5.  Navigate to **Workspace View Rules** &gt; **Related list**.
6.  Add the Workspace view rule created.
7.  Open the Service Operations Workspace.
8.  Create an incident where the **Configuration Item** field references a cmdb\_ci\_computer record.
9.  Save the new incident.
10. Navigate to **Incident** &gt; **Details** &gt; **Open Record** in the **Configuration Item** field.
11. Select **Open Record** on the modal that appears.

 Observe that the Custom View created in isn't applied.

</td></tr><tr><td>

UI Form Administration

 PRB1863573

</td><td>

A 'Scope tag not permitted' error is thrown when the UXC Generative AI plugin is active

</td><td>

The scoped UI macros are added to the UI16 form by the 'UXC Generative AI' plugin clash with scoping rules, causing a 'Scope tag not permitted' error to be thrown. Visually, users notice related lists and others macros not loading on the form.

</td><td>

1.  Navigate to sysapproval\_approver.list.
2.  Open any record still in the 'Requested' state.
3.  Right-click on the header and configure the form layout.
4.  Add the 'Test Formatter Approval Scoped' formatter to the layout after the 'Approval Summary' formatter.
5.  Configure the form.
6.  Add 1 related list to better see a broken page when reproducing.
7.  Clear the cache using cache.do.
8.  Open the record.

 Observe that the form is in a broken state. The approval \_summary form renders on the page, but everything else is missing. Related lists won't display. Users aren't able to right-click on the header or see the scoped UI macro rendered.

</td></tr><tr><td>

UI Form Administration

 PRB1866407

 [KB2119192](https://hi.service-now.com/kb_view.do?sysparm_article=KB2119192)

</td><td>

Activity Stream attachment tile actions don't work when a page has been set up to use the multi-controller template

</td><td>

Attachments aren't downloadable from the Activity Stream.

</td><td>

Refer to the listed KB article for details.

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

UI Form Administration

 PRB1870603

</td><td>

A read-only HTML field displays a horizontal and vertical scroll

</td><td>

The field shouldn't have a scroll bar.

</td><td>

1.  Open any problem record.
2.  On the **fix\_notes** field, input text at least for 11 lines.
3.  Close the record.
4.  Impersonate a non-admin user.
5.  Open that record again to check the **fix\_notes** field.

</td></tr><tr><td>

UI Form Administration

 PRB1894995

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

 Actual behavior: Images from the variable are reattached every time a user opens the RITM record. Newly re-attached images are show in the activity stream. These images can also be found in the sys\_attachment table with Table sys ID = &lt;RITM sys\_id&gt;.

</td></tr><tr><td>

User Criteria for Service Catalog

 PRB1819841

 [KB1773413](https://hi.service-now.com/kb_view.do?sysparm_article=KB1773413)

</td><td>

Semaphore exhaustion is caused by the getAllUserCriteria function getting called in widgets

</td><td>

When a public page is accessed by a guest user or web crawler, this prompts a call to the getAllUserCriteria API, which causes semaphore exhaustion.

</td><td>

Refer to the listed KB article for details.

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

 PRB1788084

 [KB1721199](https://hi.service-now.com/kb_view.do?sysparm_article=KB1721199)

</td><td>

Using g\_aw.openRecord on a new record in the Service Operations Workspace \(SOW\) doesn't work if a tab to the right of the UI action is selected

</td><td>

Using the UI action on g\_aw.openRecord doesn't function correctly if it is used on a tab that has other tabs to the right of it. For example, if there are multiple tabs opened for a new interaction and the UI action is used to open a new incident record to escalate it, the UI action doesn't work.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

UX Framework

 PRB1827900

</td><td>

The **New** button is missing in the 'Cases for Opened for User' related list

</td><td>

 

</td><td>

1.  Provision an instance with sn\_hr\_core sn\_hr\_agent\_ws 4.0.0-SNAPSHOT latest build installed.
2.  Open a HR case.
3.  Access cases for the opened 'For User' related list.
4.  Observe the list actions.

 See that the **New** button is missing.

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

Virtual Agent

 PRB1825597

</td><td>

The user is unable to select a subflow in a Virtual Agent flow with the action activity

</td><td>

The action utility pulls the first 100 records into the query by the category sorted by name for each spoke.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1833571

</td><td>

When \_max\_wait\_topic\_ is ended using the 'End Conversation' option, the conversation hangs and never completes

</td><td>

The 'Resume flow after topic switching' inside of the \_max\_wait\_topic\_ properties should be flipped to false.

</td><td>

1.  Install the AgentChat plugin.
2.  Navigate to the awa\_queue table.
3.  Open 'Agent Chat Queue'.
4.  Set **Max wait time** to something short like 30 seconds.
5.  Select **Queue Triggers** in the related lists and create a new one.
6.  Ensure that the queue trigger is a max wait time trigger and have the topic be anything.
7.  Navigate to the awa\_assignment\_rule and open 'Chat - Most Capacity'.
8.  Select **Rejection Handling** and set the timeout to 2 minutes.
9.  Ensure that an agent is online
10. Start a conversation and run the 'Live Agent Support' topic.
11. Let the search run until the max wait time topic appears.
12. Select **End conversation**.

 Expected behavior: The conversation ends.

 Actual behavior: The conversation hangs and never ends.

</td></tr><tr><td>

Virtual Agent

 PRB1850815

</td><td>

In NLU conversations following language switch control, the search term is always 'null'

</td><td>

When Language Detection is enabled for NLU Virtual Agent conversations, any initial search term provided by the requester results in a search of 'null' and associated results.

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1862370

</td><td>

Skill executions are stuck when Now Assist guardian settings \(prompt injection, offensiveness\) are enabled

</td><td>

Skill test runs aren't working from the skill kit, whereas executions outside of the skill kit \(for example: OneExtend.execute\(\) in async mode\) are working fine for the same settings. This is due an unsupported operation exception coming from EvaluationServiceImpl.java.

</td><td>

1.  Create a skill from the Now Assist Skill Kit.
2.  Enable prompt injection from the Now Assist Guardian settings \(use option as 'Block'\).
3.  Select **Run Test** on that skill.

 Expected behavior: **Run Test** should work irrespective of the guardian setting because users can execute the same One Extend capability outside of the skill kit.

 Actual behavior: **Run Test** is stuck due to an exception \(Error Execution of evaluation request failed for batch result: fbb3afc4c348 e2149e83d62 f0501312b due to error: null\).

</td></tr><tr><td>

Virtual Agent

 PRB1866633

</td><td>

In APAC data center instances, AI agents aren't working even after accepting the Global Routing Consent information message

</td><td>

Global routing is not working even after consenting on the info message for data center instances in the Asia-Pacific region.

</td><td>

1.  Deploy a new instance from the APAC data center.
2.  In an APAC region instance, select **Agree on the Global Routing Consent info message**.

 Expected Behavior: The AI Orchestrator should be invoked.

 Actual Behavior: Even after accepting the consent, AI agents are not functioning, and the error message occurs: 'Sorry, there was a problem on my side trying to complete this request. Try asking again later'.

</td></tr><tr><td>

Virtual Agent

 PRB1866702

</td><td>

'Summarize a record card' isn't displaying when reactivating the case summarisation in Workspace when domain separation is turned on

</td><td>

 

</td><td>

 

</td></tr><tr><td>

Virtual Agent

 PRB1866717

</td><td>

In Agent Chat, there's an oversized **New messages below** button

</td><td>

In Virtual Agent \(VA\) UI Experience, the **New messages below** button is disproportionately large compared to the rest of the text within the VA.

</td><td>

1.  Start a new conversation in VA in an incognito session with an available awa\_agent in a normal session.
2.  As an agent, enter a number of messages into the chat.
3.  Return to the incognito session to view as an end user in VA.

 Expected behavior: See the down arrow with the 'New messages below' hint text when hovered over displayed, and of a size appropriate to the rest of the VA conversation text.

 Actual behavior: See the new button display the down arrow and the 'New messages below' text, which is fine, only the size of the arrow and text is disproportionate to the rest of the text within the VA chat.

</td></tr><tr><td>

Virtual Agent

 PRB1878360

 [KB2092161](https://hi.service-now.com/kb_view.do?sysparm_article=KB2092161)

</td><td>

'Show more' links are displayed, even for a topic which doesn't have any additional lines in an Edge browser

</td><td>

.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Virtual Agent

 PRB1879865

</td><td>

Now Assist doesn't generate Japanese answers properly

</td><td>

The results are mostly in English.

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

 PRB1824151

</td><td>

A message preview shows the NLU preview message or doesn't show any message even when the user has switched to LLM

</td><td>

The user sees the first message from the previous NLU mode conversation with LA.

</td><td>

1.  Navigate to SP portal in NLU mode.
2.  Start a conversation with LA.
3.  Minimize the webclient and send a few messages from LA to User.
4.  Refresh the SP portal page and confirm that user sees first message from the list of messages sent by LA in preview.
5.  End the conversation on LA side \(on the user side conversation is still open because post chat is active\).
6.  Switch the SP portal in LLM mode.
7.  Refresh the portal page and start a new conversation on NAVA.
8.  Minimize the web client and send a bunch of messages.
9.  Refresh the SP portal page.

 Expected behavior: The user should see the first message in the list of message sent by LA to user for the interaction in LLM mode.

 Actual behavior: The user still continues to see the first message from the previous NLU mode conversation with LA.

</td></tr><tr><td>

Virtual Agent Web Client

 PRB1869658

</td><td>

There's an error: 'TypeError: Cannot destructure property 'clientContext' of 'y.properties' as it is undefined.'

</td><td>

When this issue happens, users don't see any proactive message, just a create\_request call in a 'Network' tab in developer tools. If users have rules and actions setup properly for a URL or portal home pages, users should first see create\_request and then get\_action calls. The getACtions endpoint should get called and display respective proactive message.

</td><td>

 

</td></tr><tr><td>

Visual Task Boards

 PRB1852813

</td><td>

If the modal window is closed by selecting outside of the modal, VTB cards aren't refreshed automatically when updated

</td><td>

This only occurs if the modal window is closed by selecting outside of the modal. If the modal window is closed by selecting the 'X' in the top right, the record's card updates automatically as expected.

</td><td>

1.  Create a visual task board by navigating to **Self-Service** &gt; **Visual Task Boards** &gt; **New** &gt; **Data Driven Board**.
2.  Set **Task Table** to 'incident' and the **Vertical Lane** field to 'Incident State'.
3.  Select **Next**.
4.  For the conditions, set **Assigned to is \[current user\]** and select **Create**.
5.  Select a card on the VTB to open the modal window.
6.  Unassign the record from \[current user\] in the modal window.
7.  Close the modal window by selecting outside of the modal.

Observe that the card remains on the VTB even though it no longer meets the conditions for the board.

8.  Refresh the VTB page.

 Observe the card is no longer on the board.

</td></tr><tr><td>

Walk-Up Experience

 PRB1873610

 [KB2046788](https://hi.service-now.com/kb_view.do?sysparm_article=KB2046788)

</td><td>

After an Yokohama upgrade, the walk-up queue isn't displaying any users who are checked in for any location

</td><td>

The issue occurs because the Rest API contains the snc\_internal role and as the user has snc\_external role, so it disqualifies the walkup user and doesn't render any users in the queue.

</td><td>

Refer to the listed KB article for details.

</td></tr><tr><td>

Web UX Runtime

 PRB1799951

</td><td>

Saving a field change on a form doesn't update the screen status once changes are saved

</td><td>

A warning message appears because changes to the incident record aren't saved despite the user saving the changes.

</td><td>

1.  Open any incident record in the Service Operations Workspace \(SOW\).
2.  Open the 'Overview' tab on the record.
3.  Modify any field by selecting the pencil icon to edit.
4.  Select **Save**.
5.  Notice that the degree symbol that appears before the Incident record number in the SOW record tab, indicating that the record has not been saved.
6.  Closed the record tab.

 Notice that a warning appears, 'Closing this tab will cause your changes to be lost. Do you want to continue?'.

</td></tr></tbody>
</table>## All Other Fixes

To view a list of all other PRBs fixed in Zurich, refer to [All other Zurich fixes](zurich-all-other-fixes.md).

**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


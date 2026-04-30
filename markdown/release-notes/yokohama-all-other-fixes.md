---
title: All other Yokohama fixes
description: The Yokohama release contains important problem fixes.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 109
breadcrumb: [Available patches and hotfixes, Learn about the Yokohama release, Yokohama release notes]
---

# All other Yokohama fixes

The Yokohama release contains important problem fixes.

-   **Yokohama was released on January 30, 2025.**
    -   Build date: 01-22-2025\_0439
    -   Build tag: glide-yokohama-12-18-2024\_\_patch0-01-14-2025

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](../upgrades/reference/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb_view.do?sysparm_article=KB0743854).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/yokohama/rn/patches/PRBs-Y00.00.xlsx)

## All other fixes

<table id="all-other-fixes" class="custom-rows"><thead><tr><th class="filter">

Problem category

</th><th>

Problem

</th><th>

Short description

</th></tr></thead><tbody><tr><td>

\[Deprecated\] Classic HR Service Delivery Agent Workspace

</td><td>

PRB1799637

</td><td>

Unable to complete an HR Task when 'Assigned to' is populated from an HR Template

</td></tr><tr><td>

Access Control

</td><td>

PRB1802864

</td><td>

The result of GlideRecordSecure.get\(\) changes when preceded by a GlideRecord.get\(\) call

</td></tr><tr><td>

Access Control

</td><td>

PRB1717880

</td><td>

The base instance object UI Action **Assign to me** uses the itil role instead of the ITSM/CMDB fine-grained roles or a combined condition

</td></tr><tr><td>

Access Control

</td><td>

PRB1744106

</td><td>

Concurrent updates to the group/role assignment results in an incorrect inheritance count

</td></tr><tr><td>

Access Control

</td><td>

PRB1773126

</td><td>

An ACL for the 'Database' view isn't working as expected for accessible tables

</td></tr><tr><td>

Access Control

</td><td>

PRB1839587

</td><td>

A current object in the REST\_Endpoint type ACL is empty starting from Xanadu

</td></tr><tr><td>

Access Control

</td><td>

PRB1797654

</td><td>

Using @mention from the **Requested for** field on a sc\_task table record shows an incorrect UI message if Glide.ui.mentions .check\_record\_visibility is active

</td></tr><tr><td>

Access Control

</td><td>

PRB1801856

</td><td>

The ACL 'list\_edit' isn't visible in an instance

</td></tr><tr><td>

Access Control List \(ACL\) Rules

</td><td>

PRB1790131

</td><td>

HasRightsToReadIsTrue is missing from the ACL and DF forms

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1832293

</td><td>

There's an exception in the activity stream when creating a new case

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1796571

</td><td>

'Archive Destroy Run' is excessively slow when deleting activities due to the overhead incurred by publishing Asynchronous Message Bus \(AMB\) messages

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1778010

</td><td>

SysActivityRule should filter its query on the fields that Workspace can only see

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1757803

</td><td>

In a VTB activity, the Japanese translation of '\{0\} was \{1\}' is incorrect

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1799614

</td><td>

An activity stream dynamic translation error 'Unable to Translate. Try again' occurs when the detected language is the same as the user language

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1819078

</td><td>

Relationship changes aren't appearing and there's a number in the Workspace in the activity stream

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1793496

</td><td>

When selecting 'Show full conversation' in an activity and when the email body is empty, an infinite loop is shown as 'Loading Email Content'

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1775777

</td><td>

g\_form.setValue\(\) isn't working as expected on Workspace when applied to the **Comments** field

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1793499

</td><td>

In Configurable Workspace, the multi-line in case and task activity **Description** field is displayed as one long string

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1778571

</td><td>

A username is missing on 'Relationship Change' entries in the Workspace activity stream

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1784714

</td><td>

Advanced Work Assignment \(AWA\) responders fall out of sync if a service channel record is reverted to an earlier version

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1802799

</td><td>

Duplicate entry for an attachment in a **Transcript** field

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1821208

</td><td>

When using the Advanced Work Assignment \(AWA\) Inbox Actions API to accept a chat on behalf of a user, the agent name and avatar doesn't match the actual agent name and avatar

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1796013

</td><td>

Advanced Work Assignment \(AWA\) doesn't assign non-interaction or non-messaging work items if the max\_wait\_time is defined in the queue after upgrading to Washington DC

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1824092

</td><td>

Work items aren't counting towards the capacity recalculation total when they are matched with an agent but not yet offered

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1791870

</td><td>

Update Service Channel Util Condition's hint

</td></tr><tr><td>

Agent Assist

</td><td>

PRB1819434

</td><td>

Agent Assist recommendation common reference doesn't show a result card

</td></tr><tr><td>

Agent Assist

</td><td>

PRB1818474

</td><td>

Newly trained Similarity Solution Definitions can't be selected to be used in Agent Assist recommendations

</td></tr><tr><td>

Agent Assist

</td><td>

PRB1784219

</td><td>

SOW \(Service Operations Workspace\) Agent Assist doesn't show proper results if there are multiple fields mapped

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1801904

</td><td>

The conversation panel appears for a closed interaction even after setting inactive.interaction. conversation.history .panel.enabled to 'false'

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1801087

</td><td>

Screen readers don't announce new messages in the Virtual Agent \(VA\) chat window

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1788201

</td><td>

Resolve copy-paste and debounce issues for chat input text area in Agent Chat and sidebar

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1766118

</td><td>

sys\_cs\_conversational state is stuck at a translating state when the sys\_cs\_conversation goes to faulted state

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1825429

</td><td>

Dynamic translated messages aren't displayed correctly after aggressive message fetching is enabled in Agent Chat

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1766052

</td><td>

The incorrect chat Workspace tab is highlighted when closing one of the chat tabs

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1797451

</td><td>

The textAreaRef doesn't get instantiated correctly on hook-insert, so the 'Enter' key and **Send** button in the input area don't work

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1802338

</td><td>

Auto-flush on the 'Conversation' table \(sys\_cs\_conversation\) causes issues with displaying the conversation history for agents in the chat window

</td></tr><tr><td>

Agile Development

</td><td>

PRB1789584

</td><td>

DEFN1003811 calculates worker subscription roles differently for SMV1 versus SMV2

</td></tr><tr><td>

AI Search

</td><td>

PRB1720477

</td><td>

Translated Field Helper generates unexpected AI Search documents for installed languages

</td></tr><tr><td>

AI Search

</td><td>

PRB1774826

</td><td>

The AI Search 'Update event queue' writable property is turned off with GenAI semantic tables indexing

</td></tr><tr><td>

AI Search

</td><td>

PRB1799201

</td><td>

The 'Suggested results' page continuously loads for guest user searches in the Service Portal

</td></tr><tr><td>

AI Search

</td><td>

PRB1797714

</td><td>

Autocomplete suggestions aren't returned

</td></tr><tr><td>

AI Search

</td><td>

PRB1808879

</td><td>

Now Assist Q&amp;A doesn't return Glide Record \(GR\) results

</td></tr><tr><td>

AI Search

</td><td>

PRB1756872

</td><td>

Users are unable to create an action name in AI Search results action configuration

</td></tr><tr><td>

AI Search

</td><td>

PRB1735195

</td><td>

The range facet and facet with compound table.column set in the facet fields is filtered out when one of the tables is late-binding

</td></tr><tr><td>

AI Search

</td><td>

PRB1755160

</td><td>

The SysID of a record is displayed as a title in 'recently viewed items' and 'exact match' in Zing search

</td></tr><tr><td>

AI Search

</td><td>

PRB1817875

</td><td>

Search Preview\(New\) doesn't filter all users

</td></tr><tr><td>

AI Search

</td><td>

PRB1766750

</td><td>

UX should respect timeouts on asynchronous Genius results

</td></tr><tr><td>

AI Search

</td><td>

PRB1836358

</td><td>

A race condition causes an incorrect deleteMultiple\(\) query to be generated on the v\_search\_genius\_result and sys\_variable\_value tables

</td></tr><tr><td>

AI Search

</td><td>

PRB1805031

</td><td>

The Global Search icon is incorrectly colored when a dark banner is used

</td></tr><tr><td>

AI Search

</td><td>

PRB1837962

</td><td>

When a query is performed in 'OR' mode, the pagination breaks

</td></tr><tr><td>

AI Search

</td><td>

PRB1795021

</td><td>

Add a check to replace a new line with \\n when generating ais\_sn\_components\_i18n.xml

</td></tr><tr><td>

AI Search

</td><td>

PRB1779119

</td><td>

Users are getting red banner ACL messages when viewing incidents or a case task after a Global Search

</td></tr><tr><td>

AI Search

</td><td>

PRB1757882

</td><td>

AI Search results takes time to show results for specific words

</td></tr><tr><td>

AI Search

</td><td>

PRB1785294

</td><td>

Suggestions for recently viewed results \(PERSONAL\_CLICK suggestions\) with external URLs don't navigate correctly in Portal

</td></tr><tr><td>

AI Search

</td><td>

PRB1759730

</td><td>

Databroker calls for AI Search/Semantic Search are added in the outbound logs

</td></tr><tr><td>

AI Search

</td><td>

PRB1785471

</td><td>

Multiple 'opens in a new tab' links on voiceover using AI Search on portal \(accessibility issues\)

</td></tr><tr><td>

AI Search

</td><td>

PRB1792436

</td><td>

Empty ais\_search\_profile\_ais\_s earch\_source\_m2m can be created through a form

</td></tr><tr><td>

AI Search

</td><td>

PRB1823794

</td><td>

If valid\_to is marked as no\_text\_index = true in ais\_datasource, an exception is thrown when searching

</td></tr><tr><td>

AI Search

</td><td>

PRB1808466

</td><td>

AI Search yields a 'No results found' message on the Now Mobile app, but works as expected in the Service Portal

</td></tr><tr><td>

AI Search

</td><td>

PRB1779622

</td><td>

'Attachment' isn't translated in the suggested search pop-up

</td></tr><tr><td>

AI Search

</td><td>

PRB1832346

</td><td>

Selecting search results adds a parameter 'SearchTerm', which leads to a 404 error

</td></tr><tr><td>

AI Search

</td><td>

PRB1802419

</td><td>

The autocomplete suggested result navigates to the backend record for a Request Item, Incident, Change, or Problem

</td></tr><tr><td>

AI Search

</td><td>

PRB1791896

</td><td>

Search Evam Data Resource returns the error 'Duplicate key title \(attempted merging values com.Glide.ux.runtime. data\_broker.composite .model.IterableItem$Field\)'

</td></tr><tr><td>

AI Search

</td><td>

PRB1811885

</td><td>

Risk Intelligence Report \(RIR\) doesn't boost for a language match

</td></tr><tr><td>

AI Search

</td><td>

PRB1726217

</td><td>

Global search fails with a 400 error for custom Workspace applications with the application administration flag set to true

</td></tr><tr><td>

AI Search

</td><td>

PRB1770996

</td><td>

The preview link on an AI Search source breaks if any special characters are present in the conditions

</td></tr><tr><td>

AI Search

</td><td>

PRB1792826

</td><td>

The search preview link doesn't take into account a 'New Condition' from an indexed source

</td></tr><tr><td>

AI Search

</td><td>

PRB1831427

</td><td>

A browser refresh doesn't work when searching with an integer in Global Search, and it throws a 'r.trim isn't a function' error

</td></tr><tr><td>

AI Search Assist

</td><td>

PRB1787918

</td><td>

In AI Search results for a knowledge article, only view counts and ratings are visible

</td></tr><tr><td>

AI Search for Virtual Agent

</td><td>

PRB1771693

</td><td>

Videos incorporated into topics in My Bot load slowly, such as the topic 'Email Setup on Phone'

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1778742

</td><td>

Some breakdown elements filters aren't applied to the widget

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1826719

</td><td>

The 'Walk-Ups by Hour' and 'Walk-Ups by Day of the Week' widgets on the Customer Service Management \(CSM\) Walk-Up Experience Dashboard fail to display the data

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1769933

</td><td>

A bar chart displays different values for the same applied 'group by'

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1790714

</td><td>

'Group by' doesn't work in database view reports

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1815564

</td><td>

Platform Analytics doesn't correctly interpret the &gt; symbol in the title and instead displays '&amp;glt;' or '&amp;gt;'

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1794715

</td><td>

Breakdown elements are repeatedly queried when fetched with a PAR filter

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1820588

</td><td>

Vendor Management Workspace performance reports display: 'error'

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1725658

</td><td>

The filter generates an incorrect query for fields with a different reference key

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB1809223

</td><td>

Enabling the **Export** button only if there are valid entries of recipients for manual export

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB1810971

</td><td>

In Platform Analytics, '\[embedded list\]' doesn't work on a scheduled export

</td></tr><tr><td>

Analytics Hub

</td><td>

PRB1785933

</td><td>

Multiple translations are missing in the Performance Analytics Hub for the Dutch language

</td></tr><tr><td>

Antivirus Scanning

</td><td>

PRB1734157

</td><td>

Update com.Glide.snap.url to snap-v2 for the release of Glide

</td></tr><tr><td>

Antivirus Scanning

</td><td>

PRB1813543

</td><td>

Certain file types aren't scanned \(available\) by antivirus scanning

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1785858

</td><td>

When an application customization is installed, there might be only a 'history' version for a customized record and no 'current' \(in sys\_update\_version\)

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1785858

</td><td>

When an application customization is installed, there might be only a 'history' version for a customized record and no 'current' \(in sys\_update\_version\)

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1753470

</td><td>

App customizations still have sys\_claim after being reverted to a base instance

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1789108

</td><td>

Upgrading the base app when a customization is present results in a mix of custom and base choices

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1769363

</td><td>

Unpublished customizations are reverted after upgrading to the base application

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1802004

</td><td>

A cluster message processing other nodes throws a NullPointerException \(NPE\) after app installation

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1792512

</td><td>

Translations are loaded repeatedly when loading conditional content for sn\_vul

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1776624

</td><td>

The host app isn't able to load the macros under 'ui.jtemplates', so openframe isn't loading with Next Experience turned off

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1822879

</td><td>

In the case of a combination of hosted plugins with app customization, the existing higher version host app store plugin object isn't used

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1788335

</td><td>

Remote app table entries are populated with 'undefined' in the 'sys\_code' column

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1789812

</td><td>

Uninstalling an application that added fields to an existing table removes the metadata for the field but won't drop the column in the database

</td></tr><tr><td>

Application Manager

</td><td>

PRB1780803

</td><td>

Remote app table entries are populated with 'undefined' in the 'sys\_code' column

</td></tr><tr><td>

Application Manager

</td><td>

PRB1770423

</td><td>

There's different behavior in a product page versus an app page \(update/installed\) for applications

</td></tr><tr><td>

Application Manager

</td><td>

PRB1792061

</td><td>

The schedule install/update of the application isn't working as expected in both new and classic Application Manager

</td></tr><tr><td>

Application Rationalization

</td><td>

PRB1790822

</td><td>

When an empty object is given as input in a source field, docs aren't loaded

</td></tr><tr><td>

Application Vulnerability Response

</td><td>

PRB1828326

</td><td>

The GitHub AVI 'First found' and 'Last found' dates are swapped

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1802606

</td><td>

An appointment booking cancellation error email doesn't respect timezones

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1789260

</td><td>

Personal events on a technician calendar are ignored when booking an appointment for an appointment booking user

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1792635

</td><td>

When the last day of bookable days falls on the first day of the upcoming month, the AB modal doesn't load the first day of month

</td></tr><tr><td>

Appsee - Platform Infrastructure

</td><td>

PRB1802917

</td><td>

GeoIP has an error while retrieving the country/policy, and a null pointer exception error displays

</td></tr><tr><td>

App Template Framework

</td><td>

PRB1763884

</td><td>

Payloads with multiple sys\_complex\_object records with same sys\_id aren't loaded properly

</td></tr><tr><td>

Archive Rules

</td><td>

PRB1789753

</td><td>

A Table Cleaner rule for sys\_archive\_run impacts the restoration of records older than one year

</td></tr><tr><td>

Archive Rules

</td><td>

PRB1764487

</td><td>

Related records are inserted with a display value instead of a sys\_id when they are archived

</td></tr><tr><td>

Archive Rules

</td><td>

PRB1762255

</td><td>

Archived approvals aren't displaying because of a broken ACL

</td></tr><tr><td>

Ask for Approval - Flow Action

</td><td>

PRB1779799

</td><td>

A stage column on a Requested Item \(RITM\) list incorrectly shows 'guest' as an approver in the 'Waiting For Approval' stage

</td></tr><tr><td>

Asset Management

</td><td>

PRB1791993

</td><td>

Hundreds of errors display in the system log reading: 'Cannot call sendRedirect\(\) after the response has been committed'

</td></tr><tr><td>

Asset Management

</td><td>

PRB1781337

</td><td>

The 'Stock Runner' job is failing with an error

</td></tr><tr><td>

Asset Management

</td><td>

PRB1784173

</td><td>

When deploying an asset, the location file isn't set properly

</td></tr><tr><td>

Asset Management

</td><td>

PRB1789417

</td><td>

Asset and CI synchronization might not work properly on domain separated instances in the Washington DC release due to the scoped cache mechanism

</td></tr><tr><td>

Asset Management

</td><td>

PRB1778297

</td><td>

The Hardware Asset Management \(HAM\) 'Incident' view rule within Asset Management Workspace targets Agent Workspace

</td></tr><tr><td>

Asset Management

</td><td>

PRB1802625

</td><td>

While retiring a consumable, the related Stockroom options aren't all visible at once on the pop-up

</td></tr><tr><td>

Asset Management

</td><td>

PRB1822129

</td><td>

The order of the substate choices in the 'Retire Asset' modal aren't displayed in the order defined in the dictionary entry of the field

</td></tr><tr><td>

Asset Management

</td><td>

PRB1770430

</td><td>

Attachments uploaded from the Now Agent app get mapped to the parent table \(alm\_asset\) instead of the child table \(alm\_hardware\)

</td></tr><tr><td>

Asset Management

</td><td>

PRB1805243

</td><td>

Email client isn't showing on Assets Workspace in compose

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

</td><td>

PRB1833926

</td><td>

ExecutorQueue consumes large memory by copying GlideSnapShotSession, which has large a fCache filed in 'Transaction'

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

</td><td>

PRB1822973

</td><td>

Record Watcher \(RW\) exceptions out when it encounters an invalid record and fails to execute repsonders, which can cause flows to stall

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1769071

</td><td>

There's an error when trying to attach a BMP file to a record manually or via the REST API

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1801182

</td><td>

The **Attach File** field 'Pencil/Edit' icon disappears for an attachment after saving a record

</td></tr><tr><td>

Audit History

</td><td>

PRB1793551

</td><td>

A null object returned by HistoryChangeList Iterator should be handled

</td></tr><tr><td>

Audit History

</td><td>

PRB1837362

</td><td>

NoBroadcast\(\) logs are consumed by Log Export Service \(LES\) topics

</td></tr><tr><td>

Authentication

</td><td>

PRB1764389

</td><td>

After single sign-on \(SSO\) login in and logout, navigating to the /log page shows 'Security constraints prevent access to requested page'

</td></tr><tr><td>

Authentication

</td><td>

PRB1756224

</td><td>

When a user is locked out and then unlocked in the user profile, the search displays a blank page

</td></tr><tr><td>

Authentication

</td><td>

PRB1775791

</td><td>

View rules on customer\_contact makes the **Set Password** UI action change the Password Needs Reset of the admin user instead of the changed user

</td></tr><tr><td>

Authentication

</td><td>

PRB1782128

</td><td>

Error messages reading 'CSRF validation failed' are logged even though the validation property is false

</td></tr><tr><td>

Authentication

</td><td>

PRB1799507

</td><td>

Provide better logging / diagnostics / debugging to show details of why IP access was allowed or denied

</td></tr><tr><td>

Authentication

</td><td>

PRB1764318

</td><td>

OIDC Authenticating Clients doesn't take the client secret into account

</td></tr><tr><td>

Authentication

</td><td>

PRB1753368

</td><td>

Information link for Rest API Access Policy Prioritization directs to the ServiceNow staging documentation site during an upgrade case

</td></tr><tr><td>

Authentication

</td><td>

PRB1763499

</td><td>

Session timeout doesn't work as expected in the Engagement Messenger

</td></tr><tr><td>

Authentication

</td><td>

PRB1791895

</td><td>

When an explicit role plugin is installed and the property 'Glide.security.explicit \_roles.do\_not\_fix'= true, single sign-on \(SSO\) login fails if the post auth policy requires an snc\_internal role

</td></tr><tr><td>

Authentication

</td><td>

PRB1800758

</td><td>

The URL is incorrectly decoded after session timeout for Next Experience when the user logs back in within the top navigation

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1764100

</td><td>

ATF \(Automated Test Framework\) steps that execute without explicitly setting 'Success' or 'Failed' statuses can leave pending suite results and stuck cloud run executions

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1772058

</td><td>

ATF \(Automated Test Framework\) tests can sometimes generate modified records for 'label\_history', which can block tests from running in parallel

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1769587

</td><td>

ATF \(Automated Test Framework\) scheduled client test runners can sometimes get unimpersonation errors

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1788452

</td><td>

ATF \(Automated Test Framework\) Field State Validation doesn't work in Service Operations Workspace

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1787222

</td><td>

If a server error is ignored, it appears to prevent the execution of later tests in the batch

</td></tr><tr><td>

Automated Test Framework for Service Catalog

</td><td>

PRB1687069

</td><td>

The script include 'VariableQueryParser' is causing the evaluation of **javascript:\*** field values to be skipped in Automated Test Framework \(ATF\)

</td></tr><tr><td>

Baseline CMDB

</td><td>

PRB1789027

</td><td>

Update all CMDB / CSDM table and column labels to reflect the current verbiage in dictionary definitions

</td></tr><tr><td>

Cache

</td><td>

PRB1804575

</td><td>

CollectingLRUCache isn't synchronized so the number of entries can exceed the max size

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1768199

</td><td>

Names aren't updated between the 'Allegations and Associated Allegations' table

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1805956

</td><td>

Users are unable to create Knowledge Base \(KB\) articles for HR Cases in UI16 and in the HR Agent Workspace

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1819557

</td><td>

Remove deprecated entitlement code and APIs in HR plugins

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1762562

</td><td>

hr\_caseMyRequestFilterUtil doesn't restrict queries on inactive sysapproval\_approver records

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1791894

</td><td>

Inadequate localization for Platform Analytics Dashboards - HR Manager

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1803855

</td><td>

Issue with a base instance relative duration 'x business days by 4pm' and the script include DurationCalculator

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1784071

</td><td>

'Retake a survey in HR: Core scope' creates duplicate metric result records

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1791728

</td><td>

A response template isn't appearing in certain cases in Customer Service Management \(CSM\) Workspace

</td></tr><tr><td>

Case API

</td><td>

PRB1784496

</td><td>

Case API gives an incorrect result count when role-based filters are applied

</td></tr><tr><td>

Case Management

</td><td>

PRB1743786

</td><td>

The 'New case type' selector and 'related file' aren't installing on a requested instance

</td></tr><tr><td>

Case Management

</td><td>

PRB1802936

</td><td>

'Publish With Approval' doesn't work as expected

</td></tr><tr><td>

Case Management

</td><td>

PRB1810610

</td><td>

The **Consumer** field is empty and can't be populated on a case task in Customer Service Management \(CSM\) Agent Workspace

</td></tr><tr><td>

Case Management

</td><td>

PRB1826477

</td><td>

For the base instance 'Set Reassigned To Count' business rule, the incorrect trigger condition is configured

</td></tr><tr><td>

Case Management

</td><td>

PRB1826618

</td><td>

An email with a recipient list of more than 1000 users isn't sent

</td></tr><tr><td>

Case Management

</td><td>

PRB1791957

</td><td>

An unnecessary space is added to the name of 'Primary Support Agent' in sn\_customerservice \_responsibility\_def

</td></tr><tr><td>

Catalog Client Scripts

</td><td>

PRB1808595

</td><td>

Lookup Select Box doesn't show the selected value in the variable editor in the RITM form if an onLoad catalog client script adds an option

</td></tr><tr><td>

Catalog Portal Pages

</td><td>

PRB1802926

</td><td>

The DateTime Picker modal for the 'Register a Visitor' form isn't accessible through the tab key

</td></tr><tr><td>

Change Advisory Board \(CAB\) Workbench

</td><td>

PRB1809993

</td><td>

An encrypted field isn't displayed correctly in CAB workbench

</td></tr><tr><td>

Change Management

</td><td>

PRB1793295

</td><td>

Transition states from state models aren't ordered by sequence, as they are configured

</td></tr><tr><td>

Change Management

</td><td>

PRB1790024

</td><td>

A review flow should only attach one post-implementation review task

</td></tr><tr><td>

Change Management

</td><td>

PRB1793725

</td><td>

Standard change template proposal properties \(sys\_app\_module\) isn't found under Intelligent Solution Configuration

</td></tr><tr><td>

Change Management

</td><td>

PRB1827180

</td><td>

The 'canModifyCI' change model attribute check has a typo and it affects modification when transitioning from the initial state

</td></tr><tr><td>

Change Management

</td><td>

PRB1816569

</td><td>

Standard change properties should not have been modified on upgrade from Washington DC to Xanadu

</td></tr><tr><td>

Change Management

</td><td>

PRB1819915

</td><td>

CAB workbench is stuck in loading state when the user doesn't have read access to one of the changes due to a domain restriction

</td></tr><tr><td>

Change Management

</td><td>

PRB1810280

</td><td>

Some change risk assessments no longer match which allows for risk evaluation without the completion of other risk assessments

</td></tr><tr><td>

Change Management

</td><td>

PRB1801143

</td><td>

There is a URL truncation issue in change request copies

</td></tr><tr><td>

Change Management

</td><td>

PRB1801450

</td><td>

**Copy change function** isn't working as expected

</td></tr><tr><td>

Change Management

</td><td>

PRB1815169

</td><td>

A standard change template \(std\_change\_record\_producer\) doesn't show the column 'Additional comments'

</td></tr><tr><td>

Change Management

</td><td>

PRB1807818

</td><td>

TaskUtilSNC notifies the user with a connect message, but the user doesn't see the connect message in the Next Experience interface

</td></tr><tr><td>

Change Management

</td><td>

PRB1788178

</td><td>

Incorrect German text in a change request on a base instance's Scheduling Assistant

</td></tr><tr><td>

Change Management

</td><td>

PRB1778031

</td><td>

A standard change template URL is available/visible to users that are restricted from it as configured in 'Available for' user criteria

</td></tr><tr><td>

Change Management

</td><td>

PRB1803186

</td><td>

Accented characters aren't rendered in the conflict calendar's short description

</td></tr><tr><td>

Change Management

</td><td>

PRB1827022

</td><td>

Automatically-created translated text isn't updated when the user modifies the 'Standard Change' template name

</td></tr><tr><td>

Change Management - Risk Assessment and Intelligence

</td><td>

PRB1787948

</td><td>

A risk assessment is set to 'Canceled' and stays canceled when filled in

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1760271

</td><td>

**Set Value** doesn't work properly in Workspace

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1685901

</td><td>

A scripted event handler on a controller causes a page to not display

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1806077

</td><td>

A delegated developer is unable to create a client callable script include

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1794520

</td><td>

Newly populated **on\_hold\_reason** field data doesn't display for a duplicate tab

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1787156

</td><td>

On a client script form, script auto-population doesn't switch from onLoad to onChange when the type is changed

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1782733

</td><td>

Client script 'SNC - default template name check' isn't inherited and causes confusion

</td></tr><tr><td>

Cloud Encryption

</td><td>

PRB1762861

</td><td>

The business rule, 'Abort changes on group' doesn't prevent regular admins from viewing the 'Cloud Encryption Quorum Control Approvers' group

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1790534

</td><td>

Improve a script to prevent slow ACL execution

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1797798

</td><td>

'sn\_cmp.cloud\_service\_user role' prevents itil users from updating Service Catalog tasks

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1749132

</td><td>

AWS CreateStack status 400 error says: 'The provided token has expired.'

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1794338

</td><td>

There is a discrepancy between DeleteStrategy for Cloud events and Cloud Discovery for vm\_instance

</td></tr><tr><td>

CMDB 360

</td><td>

PRB1790347

</td><td>

The job 'Multisource Dashboard Collection' runs twice daily

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1767484

</td><td>

'Cleanup Orphan CIs' job runs but doesn't inspect all the records in the table when they are processing in batches

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1772502

</td><td>

DbBatchProcessor doesn't resource cleanup properly resulting in high memory contention on the node

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1775491

</td><td>

The **Export query** UI action fails because it must pass the Cross-Site Request Forgery \(CSRF\) token

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1830100

</td><td>

The 'Dynamic CI' group is missing a few CIs

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1822218

</td><td>

CMDB Query Builder results in table creation fails

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1787319

</td><td>

CMDB Group 'Show All CI' results are incomplete when using multiple saved queries and a relationship type

</td></tr><tr><td>

CMDB to CSDM Data Synchronization

</td><td>

PRB1822499

</td><td>

Life Cycle Control records are missing for a CMDB base table to allow the use of the 'End of Operation' stage

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB1766321

</td><td>

Attachment API via REST tries to encrypt a file when sending a request with an empty encryption\_context query parameter

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB1790376

</td><td>

Excessive amount of data\_free on the table sys\_mass\_encryption\_job

</td></tr><tr><td>

Communities

</td><td>

PRB1793133

</td><td>

The user is able to add an image to the activity stream that takes over the entire page and covers all other notes

</td></tr><tr><td>

Communities

</td><td>

PRB1831681

</td><td>

The **Gamification Badge** description field is sanitizing language special characters

</td></tr><tr><td>

Communities

</td><td>

PRB1793564

</td><td>

The video preview isn't displayed to users for the video content type posts in the community activity feed

</td></tr><tr><td>

Communities

</td><td>

PRB1830455

</td><td>

Sn\_communities.community\_user encounters an error when requesting membership for a forum

</td></tr><tr><td>

Communities

</td><td>

PRB1819875

</td><td>

A space in the aria-label for 'すべて' causes the user's customized process to fail

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1776650

</td><td>

Unable to dot-walk into a reference field when configuring report conditions

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1786619

</td><td>

Report filter condition fields aren't aligned properly in the Classic UI

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1768500

</td><td>

When the user selects the **Save** button to save a filter on a list in the Next Experience UI when there are many filters with a scrollbar, the saving options aren't visible

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1827190

</td><td>

The luminosity contrast ratio of reconciliation rule types is less than the required 4.5:1

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1787231

</td><td>

Identification and Reconciliation Engine \(IRE\) is targeting duplicated CIs and clearing the **duplicate\_of** field

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1730677

</td><td>

CI's of the domain B/C/D can be added to a CMDB group created under domain A

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1784870

</td><td>

Tasks aren't getting generated in Xanadu after running the Retire Policy in the data manager

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1784818

</td><td>

cmdb\_ci\_network\_ adapter.mac\_manufacturer column label is 'Mac Manufacturer' instead of 'MAC Manufacturer'

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1792093

</td><td>

CMDBUtil doesn't work as expected in the filter condition to the non-admins \(itil\)

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1580009

</td><td>

CIRelationByServiceCache.getRelations\(\) causes high memory consumption

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1620855

</td><td>

An error is displayed when the user changes the instance language to Japanese

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1798671

</td><td>

**Lifecycle** fields on a CI are flipped due to a difference in payloads from multi-sources

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1825388

</td><td>

The Xanadu CMDB Workspace health dashboard for health group CIs evaluated value is incorrect when there is a health inclusion rule

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1803275

</td><td>

The submetrics page for groups doesn't have a task column available on the UI for duplicate metrics

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1815246

</td><td>

Some CMDB logging properties have debug or debugVerbose enabled by default, causing syslog performance issues

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1760552

</td><td>

The user isn't able to edit the reference qualifier of the **Owned By** field in $csdm\_app\_service view

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1809366

</td><td>

The Service Graph Connecter \(SGC\) Central menu link is missing in the Configuration Management Database \(CMDB\) Workspace after upgrading to Xanadu

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1689097

</td><td>

There's a color contrast failure for a selected item under the 'ciModel.do' page

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1819137

</td><td>

Data Manager doesn't support dot-walk fields for task assignment

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1768662

</td><td>

The business rule 'Sync Ops Status for CMDB CI' incorrectly sets the operational status to 'Non-operational' instead of 'Operational'

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1811948

</td><td>

Prevent individual updates duplicating CI values during remediation

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1770891

</td><td>

Newly created tasks stay in the 'Open' State while the 'Needs Review' checkbox is set on false in the policy

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1819941

</td><td>

Delete the 'CMDB Health Dashboard - Top Task Generating CIs Calculation' job

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1778012

</td><td>

Validate the inclusive filter in DBQuery when computing the getTotals with an inclusive condition for health scores

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1770084

</td><td>

Identification and Reconciliation Engine \(IRE\) creates multiple sys\_object\_source records for the same source \(source\_native\_key\)

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1810238

</td><td>

Identification and Reconciliation Engine \(IRE\) throws a 'MULTIPLE\_DEPENDENCIES' error when there are duplicate relationships in the database

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1767284

</td><td>

Update a reference during the insertion of records in a payload, avoiding an extra update on the 'referenced by' record

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1805007

</td><td>

Knowledge article results are shown in the Virtual Agent for a knowledge base not exposed to this portal

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1779661

</td><td>

Contextual Search conditions fails when a newline character is part of the encoded query

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1799474

</td><td>

In the Service Portal, a variable with contextual search enabled removes the space after typing text, and the cursor goes back to the last typed letter when using the spacebar

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1805505

</td><td>

There's knowledge search related slowness when a KB article is large

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1788670

</td><td>

The 'Inline Results' widget on the Record Producer doesn't display full details for kb\_template\_known \_error\_article or kb\_template\_faq records

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1793559

</td><td>

There's incorrect translations in KB articles for 'Attach to Incident' in Washington DC

</td></tr><tr><td>

Continual Improvement Management

</td><td>

PRB1780068

</td><td>

The 'View KPI details' and 'Show scorecard' icons should open the Performance Analytics chart in a new tab

</td></tr><tr><td>

Continual Improvement Management

</td><td>

PRB1816181

</td><td>

Add the 'dex-notify-svc' service within Glide.services .rest.allowed\_services

</td></tr><tr><td>

Contract Management

</td><td>

PRB1766988

</td><td>

End date calculation is incorrect in the 'Build renewal task' of the contract renewal flow

</td></tr><tr><td>

Contract Management

</td><td>

PRB1806594

</td><td>

Client script error on a 'Contract' form in Hardware Asset Workspace: '\(g\_env\) \[SCRIPT:EXEC\] Error while running Client Script 'Update tax and total cost currency '

</td></tr><tr><td>

Contract Management

</td><td>

PRB1784095

</td><td>

The currency type on the **Yearly cost** and **Monthly cost** fields changes to $ when updating the payment amount on contracts

</td></tr><tr><td>

Contract Management

</td><td>

PRB1803637

</td><td>

Performance issues with the contract unit cost calculation business rule

</td></tr><tr><td>

Core Platform

</td><td>

PRB1761876

</td><td>

A QuotaManager null point exception is printed in the logs multiple times

</td></tr><tr><td>

Core Platform

</td><td>

PRB1659462

</td><td>

Navigating to a deep link URL doesn't work as expected when the field contains '&amp;' in the query and the user isn't logged in

</td></tr><tr><td>

Core Platform

</td><td>

PRB1762254

</td><td>

A display value is empty in process mining field pickers

</td></tr><tr><td>

Core Platform

</td><td>

PRB1779358

</td><td>

The printer friendly version view doesn't display complete data from the article body

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1832803

</td><td>

There's an incorrect exchange rate conversion from IDR to USD due to truncation

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1793515

</td><td>

Problems with g\_form.clearValue\(\) and g\_form.setValue\(\) on **Currency** fields

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1762554

</td><td>

**FX currency** fields cause dot-walked or derived reference fields break in list view with the value 'null' for the sys\_id

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1785272

</td><td>

in-ID locale \(Indonesia\) doesn't convert currency values

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1822862

</td><td>

Empty rates in 'Custom currency rate' tables cause a NumberFormatException

</td></tr><tr><td>

Custom Chat Chatbot Interoperability Framework \(CCCIF\) Media Resource API

</td><td>

PRB1780681

</td><td>

Custom Chat Chatbot Interoperability Framework \(CCCIF\) should honor the com.Glide.cs.upload.attachment .to.interaction sys\_properties setting

</td></tr><tr><td>

Customer Information

</td><td>

PRB1793361

</td><td>

Unable to edit/remove dictionary override for the **last\_name** field on the customer\_contact table

</td></tr><tr><td>

Customer Operations for Customer Service Management

</td><td>

PRB1779242

</td><td>

The business rule 'Domain - Set Domain - Location' doesn't see the domain correctly, resulting in records on the cmn\_location table being created in the global domain

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB1779338

</td><td>

Recipient list supports the 'Reference Variables' but doesn't support any list variables

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB1832361

</td><td>

When Customer Service Management \(CSM\) is installed in Xanadu, the 'Overview' dashboard isn't appearing

</td></tr><tr><td>

Customer Service Management for Field Service Management

</td><td>

PRB1817415

</td><td>

'My Dispatch Map' doesn't load

</td></tr><tr><td>

Data Archiving

</td><td>

PRB1773987

</td><td>

'Restore related' fails when the reference field is for the parent table in a hierarchy

</td></tr><tr><td>

Database Indexes

</td><td>

PRB1719709

</td><td>

A slow query on sn\_cmp\_order is missing a supportive database index covering discovery\_status

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1736140

</td><td>

Auto-increment fields with a default value of 0 aren't corrected after migration using an early Utah build

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1776634

</td><td>

GlideQueryString warnings should provide exception details and stack trace

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1508047

</td><td>

Failing a copy during DB alter prevents an update set from using bootstrap batching, and results in multiple table alters

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1605677

</td><td>

Adding 'Tags' in the column view for a table on the gateway database throws an error

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1699977

</td><td>

A **Function** field with Glidefunction:concat\(\) shows an error when opening the table list in other languages

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1825857

</td><td>

Unused and missing joins in query generation for a TS query with many 'contains' conditions

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1636284

</td><td>

There's an inaccurate group count in a reference field with duplicate display values when results are paginated

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1751743

</td><td>

Parsing the FromItem type '\[SubSelect\]' isn't supported

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1789910

</td><td>

'Order by' columns aren't added to the 'Group by' clause when joined on a denormalized table with aggregation via 'RLQuery'

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1801384

</td><td>

Orphan archive-related records \(Archive\_Map NULL\) aren't ignored by the archive job

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1747815

</td><td>

Issue with the ArchiveResolver resolve\(\) method

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1756534

</td><td>

Enabling shadow tables for compaction

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1757852

</td><td>

An exclusion rule for a table with mixed cases and spaces is producing an invalid truncate statement

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1805133

</td><td>

Can't delete sys\_attachment/ sys\_attachment\_doc orphans without turning off ACLs

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1779767

</td><td>

Using 'Null' as a value in the != ALL operator set fails

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1688084

</td><td>

New categories aren't mapped to secondary DB \(database\) pools

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1726762

</td><td>

SQLCancel doesn't kill some queries that stream data

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1796286

</td><td>

Remove usage of Cleaner from PreparedStatementWrapper

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1812306

</td><td>

DBLazyWriter Dead Lock can lead to semaphore exhaustion on nodes

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1648956

</td><td>

Union replacement throws the error 'Unknown column 'count\_of\_676361911' in 'field list''

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1721884

</td><td>

Tables without PK cause group replication errors in MySQL 8

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1757535

</td><td>

Null pointer exception in ConnectionWrapper when trying to commit/rollback a connection

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1782312

</td><td>

API calls using sysparm\_offset+sysparm\_limit parameters run the query without a defined 'Order by', causing results to not return consistently in RaptorDB

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1749770

</td><td>

The size of tuple values received from the server should be limited

</td></tr><tr><td>

Data Collection for Oracle Global Licensing and Advisory Services for Software Asset Management

</td><td>

PRB1652619

</td><td>

The **Download Glass Report** UI action doesn't render CVS spreadsheet correctly and contains empty rows

</td></tr><tr><td>

Data Filtration

</td><td>

PRB1768454

</td><td>

In Vancouver's data filteration, the IP filter criteria provided in the subject condition isn't considered

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1767497

</td><td>

Declarative actions aren't working with a random key in the payload definition

</td></tr><tr><td>

Delegated Development and Deployment

</td><td>

PRB1657555

</td><td>

When creating an app on Studio with Japanese characters, the app name only generates sn\_dd\_\_ roles

</td></tr><tr><td>

Delete Records Safely

</td><td>

PRB1740509

</td><td>

Data Management jobs provide no indication to the user that operations on sys\_email or sys\_email\_log will never be recorded for rollback

</td></tr><tr><td>

DevOps \(Family\)

</td><td>

PRB1797729

</td><td>

Reducing excessive logging in DevOps Util global plugin

</td></tr><tr><td>

Discovery

</td><td>

PRB1739443

</td><td>

The user can use Service Mapping without activating Discovery and is unable to use 'Visibility' scheduled jobs and listing jobs

</td></tr><tr><td>

Discovery

</td><td>

PRB1744428

</td><td>

Discovery Home or Service Error Management is broken for the discovery\_admin role user

</td></tr><tr><td>

Discovery

</td><td>

PRB1781249

</td><td>

A child schedule is kicked off twice in a daisy chain after the parent is finished/cancelled

</td></tr><tr><td>

Discovery

</td><td>

PRB1806722

</td><td>

Oracle OCI Discovery fails with a sensor error

</td></tr><tr><td>

Discovery

</td><td>

PRB1766931

</td><td>

When adding a step in the Discovery pattern using 'Parse File' as the operation and 'JSON File' as defined parsing, a single quote \('\) present in the attribute value of the JSON file is replaced with 'quta'

</td></tr><tr><td>

Discovery

</td><td>

PRB1792552

</td><td>

A pattern doesn't terminate for WMI and SNMP queries even if the user ticks the 'terminate if not found' checkbox

</td></tr><tr><td>

Discovery

</td><td>

PRB1833443

</td><td>

Files supported for the 'put file' operation should be extensible as a MID server property

</td></tr><tr><td>

Discovery

</td><td>

PRB1766180

</td><td>

vCenter Event Collection fails with the following error, 'Expected 1 relationship but found 2 for Provides storage for::Stored'

</td></tr><tr><td>

Discovery

</td><td>

PRB1817799

</td><td>

Starting a Discovery takes a while when there's a sizeable global exclusion IP address list and inclusion list

</td></tr><tr><td>

Discovery

</td><td>

PRB1619082

</td><td>

Slowness in scheduled job Licensing Hardware Count sysauto\_script\_ dd3716460b3320 101af90bdb35673a3a

</td></tr><tr><td>

Discovery

</td><td>

PRB1783411

</td><td>

GCP Discovery with 'Glide.discovery.cdu.auto \_refresh\_sub\_accounts \_and\_ldcs' = 'true' triggers looping Discovery statuses for 'Perform Refresh Datacenters for scheduleundefined'

</td></tr><tr><td>

Discovery

</td><td>

PRB1780156

</td><td>

A Test Credential pop-up doesn't do any verification for the IP Address and allows anything through to the probe, with either non-specific errors or event successful test results back

</td></tr><tr><td>

Discovery

</td><td>

PRB1785461

</td><td>

The DeviceL3Mapping script include has an invalid query, resulting in Layer 3 IP-IP relation not being created

</td></tr><tr><td>

Discovery

</td><td>

PRB1791352

</td><td>

The External Communication Channel \(ECC\) queue related list count is a mismatch for a Discovery status

</td></tr><tr><td>

Discovery

</td><td>

PRB1725762

</td><td>

Discovery remains active if one of the multipage inputs is skipped

</td></tr><tr><td>

Discovery

</td><td>

PRB1786484

</td><td>

RunningProcessReconciler marks redundant update processes as absent

</td></tr><tr><td>

Discovery

</td><td>

PRB1764921

</td><td>

Master account details are missing from pre-pattern execution details, causing it to make additional API calls

</td></tr><tr><td>

Discovery

</td><td>

PRB1821160

</td><td>

A scripted deletion strategy is triggered for the keep strategy

</td></tr><tr><td>

Discovery

</td><td>

PRB1761883

</td><td>

Discovery perf metrics rollup by build doesn't handle multipage correctly

</td></tr><tr><td>

Discovery

</td><td>

PRB1744198

</td><td>

Not being able to debug a Discovery pattern results in the error 'This field is required: cloud\_cred\_alias'

</td></tr><tr><td>

Discovery

</td><td>

PRB1794900

</td><td>

AWS Oracle RDS License 'value' is empty during AWS RDS Discovery for the Oracle database

</td></tr><tr><td>

Discovery

</td><td>

PRB1787816

</td><td>

AIX Server os\_version is populated incorrectly by the UNIX - OS sensor script

</td></tr><tr><td>

Discovery

</td><td>

PRB1814647

</td><td>

Missing condition for service Discovery in DiscoveryStatus ExternalDependencies.does ServiceMappingHaveWorkLeft

</td></tr><tr><td>

Discovery

</td><td>

PRB1807630

</td><td>

HTTPClassyProbe creates bad credential affinities

</td></tr><tr><td>

Discovery

</td><td>

PRB1833735

</td><td>

Azure Cloud Discovery schedules aren't considering the member accounts that are selected when creating the Discovery schedule via the 'Discovery configuration' page

</td></tr><tr><td>

Discovery

</td><td>

PRB1808843

</td><td>

ApplicationDependency Mapping.map\(\) is called for each Discovery device history

</td></tr><tr><td>

Discovery

</td><td>

PRB1799862

</td><td>

Applicative credentials are logged as clear text in acc.log

</td></tr><tr><td>

Discovery

</td><td>

PRB1789364

</td><td>

'Discover Datacenter' isn't working post-Washington DC upgrade

</td></tr><tr><td>

Discovery

</td><td>

PRB1835802

</td><td>

Discovery is incorrectly classifying Cisco routers as switches for OID 1.3.6.1.4.1.9.1.469

</td></tr><tr><td>

Discovery

</td><td>

PRB1773369

</td><td>

Model for set Cisco SNS 3500 Series Appliance set to IP Switch

</td></tr><tr><td>

Discovery

</td><td>

PRB1782252

</td><td>

Enhances ADM \(ADME\) running linux\_netstat\_command.sh is unable to capture 'listening on' details for running processes

</td></tr><tr><td>

Discovery

</td><td>

PRB1779642

</td><td>

CIM probe for storage servers isn't triggered when wbem\_delay=true and there are more IPs for other types of devices \(switches, Linux OS, etc.\) in the schedule

</td></tr><tr><td>

Discovery

</td><td>

PRB1614055

</td><td>

Uninterruptable power supply \(UPS\) Discovery doesn't populate 'Discovery Source' and 'Most Recent Discovery' for alarms, inputs, and outputs

</td></tr><tr><td>

Discovery

</td><td>

PRB1779627

</td><td>

Added logic which would cause Enhanced ADM \(ADME\) to error out

</td></tr><tr><td>

Discovery

</td><td>

PRB1761894

</td><td>

The 'response canceled' error string noted in input ecc\_queue despite successful orchestrated pattern executions

</td></tr><tr><td>

Discovery

</td><td>

PRB1833554

</td><td>

IP exclusion doesn't work as expected when the schedule contains an IP net-mask alone

</td></tr><tr><td>

Discovery Probes and Sensors

</td><td>

PRB1790391

</td><td>

HP-UX Server object identifiers \(OID\) try to launch switch/router patterns

</td></tr><tr><td>

Discovery Probes and Sensors

</td><td>

PRB1785994

</td><td>

Serial-to-Ethernet devices and should not trigger a 'Network Switch' pattern

</td></tr><tr><td>

Document Intelligence Unified Backend

</td><td>

PRB1703041

</td><td>

Checkbox values aren't copied to a target record

</td></tr><tr><td>

Document Management

</td><td>

PRB1792931

</td><td>

In Application Portfolio Management, and on artifacts, the share document link isn't working

</td></tr><tr><td>

Document Management Services

</td><td>

PRB1823978

</td><td>

When placing the SVG only next to the low left corner, the x and y size seem to default to 0 when they grow beyond a certain limit inside the page

</td></tr><tr><td>

Document Management Services

</td><td>

PRB1719201

</td><td>

PDFGeneratorUtils Paragraph is unable to handle long URLs

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1766441

</td><td>

A Japanese translation of Key='download' in the sys\_ui\_message table has an additional halfwidth space from Vancouver

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1772759

</td><td>

The UI Action for **Delete modal of Attachment** in a Workspace isn't translated

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1799202

</td><td>

**Export Database View** leads to an empty PDF

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1793774

</td><td>

Nodes failing to synchronize after nodes restart with the message 'Could not define Scriptable class DocumentPermalink for extension point'

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1774417

</td><td>

Document Viewer doesn't reset the page when opening the same PDF with a different user

</td></tr><tr><td>

Dynamic Scheduling

</td><td>

PRB1811377

</td><td>

Process failure when using the Workforce Optimization \(WFO\) feature to schedule a task under dynamic scheduling

</td></tr><tr><td>

Dynamic Scheduling

</td><td>

PRB1827613

</td><td>

An error occurs when auto-assigning the Work Order Table \(WOT\) from the list

</td></tr><tr><td>

Dynamic Translation

</td><td>

PRB1801958

</td><td>

Localization and missing sys\_ui\_messages configuration issues

</td></tr><tr><td>

Dynamic Translation

</td><td>

PRB1801796

</td><td>

A pre-topic Discovery topic shouldn't be discoverable

</td></tr><tr><td>

Dynamic Translation

</td><td>

PRB1805756

</td><td>

A message containing a URL should be translatable

</td></tr><tr><td>

Dynamic Translation

</td><td>

PRB1825179

</td><td>

Users get an error message when creating the setting as part of the localization framework

</td></tr><tr><td>

Dynamic Translation for Virtual Agent

</td><td>

PRB1809302

</td><td>

Some NLU Virtual Agent topics use gs.getMessage instead of gs.getMessageLang which result in mixed translations with Dynamic Translation

</td></tr><tr><td>

Dynamic Translation for Virtual Agent

</td><td>

PRB1800384

</td><td>

Adapter conversations with Dynamic Translation for Virtual Agent \(DTVA\) and Dynamic Translation for Agent Chat \(DTAC\) enabled, images or links sent by an agent in Chat Agent aren't delivered until the conversation is closed

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1798974

</td><td>

There's an issue in custom notifications where the affected **record** field isn't saving a CI with a special character

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1784027

</td><td>

Japanese numbers display as symbols in the filenames of successfully attached files via email

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1814755

</td><td>

The **list-unsubscribe** field isn't encoded properly, breaking RFC \(Remote Function Call\) with lines exceeding 1000 characters, which breaks DKIM \(DomainKeys Identified Mail\) signing for outbound mail

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1800853

</td><td>

The condition of a subscribed notification doesn't support the OR clause

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1774019

</td><td>

The Document Viewer in the Email Viewer in the Workspace doesn't display certain file types

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1791495

</td><td>

In inbound email processing, 'Disabling Subject' classification disables the 'In-Reply-To' header classification

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1769083

</td><td>

Email Digest on HR cases encounter an email validation error

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1647321

</td><td>

MIME-type restrictions don't check attachments added by email

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1787517

</td><td>

Setting an event name in notification records also updates the **Event** field

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1766694

</td><td>

Email reply separators don't work for HR related emails

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1793964

</td><td>

Notification variables that use the :n parameter don't correctly display SMS data

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1782506

</td><td>

Copying and pasting the 'caller' email to the **Recipient** or **Cc** field shows the error, 'Some problem in fetching details of recipient' when composing an email in Workspaces

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1788940

</td><td>

Sent mailbox has emails with Type=sent but State=Ready

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1792310

</td><td>

Inbound emails that are signed and encrypted have an invalid signature with the S/MIME plugin

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1739540

</td><td>

EmailClientTemplate doesn't populate the Recipient List record on the Email Client

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1788790

</td><td>

Emails are set to 'send-ignored' when an email personal name has non-ascii characters

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1775851

</td><td>

Email Client loads a sys\_id in the **CC** field in a sc\_task form

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1775442

</td><td>

The tooltip isn't translated when hovering over 'Quick Messages' in the Workspace Email Client

</td></tr><tr><td>

Embedded Help

</td><td>

PRB1825324

</td><td>

Default values for properties in the base instance need to change due to the docs sites' URL change

</td></tr><tr><td>

Employee Service Center

</td><td>

PRB1828671

</td><td>

The 'Populate Taxonomy Content Order' job generates a large and long running query leading to high history lest length \(HLL\)

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB1766037

</td><td>

The 'Search within Topic' page doesn't return results in the Employee Center when the topic name has special characters

</td></tr><tr><td>

Encryption Support

</td><td>

PRB1788684

</td><td>

The module key isn't generated after the import token is uploaded for Column Level Encryption Bring Your Own Key \(CLE BYOK\)

</td></tr><tr><td>

Encryption Support

</td><td>

PRB1826849

</td><td>

Admin users are unable to write into a script field on the sysauto\_script table

</td></tr><tr><td>

Enterprise Architecture

</td><td>

PRB1711624

</td><td>

An upload version isn't working for an architectural artifact to create an architectural artifact version

</td></tr><tr><td>

Event Management

</td><td>

PRB1789620

</td><td>

Using the percent symbol in an event rule breaks the description

</td></tr><tr><td>

Event Management

</td><td>

PRB1786642

</td><td>

Characters like '\\n' \(new line\) are ignored and multiple consecutive spaces are replaced by one in the string value of the Description Event payload attribute

</td></tr><tr><td>

Event Management

</td><td>

PRB1796928

</td><td>

IT alerts are created or updated from anomaly events instead of anomaly alerts

</td></tr><tr><td>

Event Management

</td><td>

PRB1768681

</td><td>

Add protection when processing alerts with large additional info

</td></tr><tr><td>

Event Management

</td><td>

PRB1688635

</td><td>

System Center Operations Manager \(SCOM\) limits the value of 'context' to 540 characters

</td></tr><tr><td>

Event Management

</td><td>

PRB1794227

</td><td>

The Business Rule 'Close associated incident' creates an empty task if the incident attached to the alert is deleted during execution

</td></tr><tr><td>

Event Management

</td><td>

PRB1786196

</td><td>

Service map shows an 'OK' severity while severity is actually critical

</td></tr><tr><td>

Event Management

</td><td>

PRB1730330

</td><td>

Missing option to disable calculation of probable root cause based on change requests on application services

</td></tr><tr><td>

Event Management

</td><td>

PRB1814491

</td><td>

SCOM Bi-directional Connector fails with the message 'failed to run 3PC java.lang.ClassCastException: class org.mozilla. javascript.Undefined can't be cast '

</td></tr><tr><td>

Event Management

</td><td>

PRB1782165

</td><td>

Duplicate base instance buttons on cmdb\_ci\_query\_based\_service

</td></tr><tr><td>

Event Management

</td><td>

PRB1786266

</td><td>

metric\_value isn't populated properly

</td></tr><tr><td>

Event Management

</td><td>

PRB1784855

</td><td>

Stale em\_monitor\_state once monitored entries are regenerated

</td></tr><tr><td>

Event Management

</td><td>

PRB1772901

</td><td>

There's an out of memory error in Alert Priority when an alert has high number of child alerts

</td></tr><tr><td>

Fenix \(Family\)

</td><td>

PRB1803849

</td><td>

The Fenix job isn't working when an instance has a vanity URL set up

</td></tr><tr><td>

Field Normalization

</td><td>

PRB1817181

</td><td>

The coalescer job reads an arbitrary number of sys\_ids into memory

</td></tr><tr><td>

Field Service Management

</td><td>

PRB1827771

</td><td>

Sm\_config records are updated randomly with new versions

</td></tr><tr><td>

Financial Management

</td><td>

PRB1785604

</td><td>

'Update CI List' for a CI Rate Card doesn't show the 'Items to be Added' list

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1797502

</td><td>

Excess records are kept in sys\_flow\_value when reporting isn't set to 'FULL'

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1792828

</td><td>

Possible data leak and race condition due to a mutation in the compiled flow

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1733404

</td><td>

Users can't access the multi-answer records when iterating thorough the decision answers

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1820808

</td><td>

EventInfo should be mutable and EventInfo parameters can have null values

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1794867

</td><td>

Encountered 'error while parsing metadata for attachment' when invoking consecutive REST calls with MID in a flow

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1761922

</td><td>

Low priority flows can consume all workers and block high priority flows

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1773799

</td><td>

Decision table output throws an error reading, 'java.lang.Index OutOfBoundsException: Index 1 out of bounds for length 1'

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1713515

</td><td>

Some of the orders don't move to 'In progress' from the 'Acknowledged' state with auto-approval enabled when the rate of order creation is high

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1817474

</td><td>

An error message exists even after a retry is successful and the status code is 200

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1812566

</td><td>

Subflow outputs aren't passed to a callback when a subflow ends on MID

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1770528

</td><td>

A flow can start on another node before the flow inputs are persisted to the database

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1790120

</td><td>

If the sys\_flow\_context table size is above 100 million during an upgrade from Vancouver, Flow Engine V2 new columns aren't added

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1832181

</td><td>

Password2 decryption fails in Engine V2 after returning from the MID server

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1814015

</td><td>

A template isn't applied properly on the corresponding table fields through Flow Designer

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1791609

</td><td>

A 'Script: undefined' error message appears when the user selects the **Restart** button from the sys\_flow\_context record

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1794986

</td><td>

The table cleaner rule on 'sys\_flow\_context\_inputs\_chunk' isn't deleting records due to the 'disable table cleaner' dictionary attribute

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1783625

</td><td>

The data pill of the 'If' condition inside 'For Each' doesn't renumber when a new step is added before 'For Each'

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1813141

</td><td>

fd\_data doesn't read the object from the Create Task action

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1783808

</td><td>

In Flow Designer's UI, an unformatted JSON string is used as a message\_body, throwing: 'Content Not Found - Your flow can't be found. Flow sys\_id: Inv'' error

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1784060

</td><td>

The 'System logs' table is flooded with the message 'Flow Designer: Credentials sys\_id'

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1789319

</td><td>

XML output isn't in the correct order on a payload builder step

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1821838

</td><td>

Users can't have scripted values for inputs of dynamic flow logic

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1730817

</td><td>

The flow enters an error state when it returns from the MID server and executes the 'wait for condition' action

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1806316

</td><td>

Selecting 'Advanced Options' in a flow with run users results in a blank screen

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1828754

</td><td>

The 'Update record' action on the V26.1.3 didn't display record information as expected

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1749511

</td><td>

An error occurs in a log when trying to create a template by adding Slack Actions, such as 'Look Up User', and is unable to save the action

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1818098

</td><td>

A flow with SLA task trigger runs 3 times, and executions display 1 complete and 2 errors

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1793363

</td><td>

After applying an upgrade plan, the script include 'FlowDesignerContentFiltering' doesn't work

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1794619

</td><td>

Reference values in **Template** fields aren't properly stored

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1782149

</td><td>

The warning message 'Encountered undeclared output variable' appears when executing an action

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1775013

</td><td>

The changed fields data pill, 'Previous Display Value', aren't working as expected for Glide\_list

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1787937

</td><td>

In the Flow Designer execution log, users are unable to see all the iterations in a nested 'for' loop

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1769794

</td><td>

The Flow Designer sets the true/false input parameter to 'false' in Xanadu

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1770864

</td><td>

A slushbucket is displaying as empty in Flow Designer

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1820918

</td><td>

A flow warning when completing a change task displays a warning: 'Runtime value key must be non-null'

</td></tr><tr><td>

Form Builder

</td><td>

PRB1779701

</td><td>

An analytics form-field decorator icon isn't aligning as expected on incident forms when Next Experience is enabled

</td></tr><tr><td>

Form Controller

</td><td>

PRB1800307

</td><td>

Agent Workspace links are defined as buttons in the 'Profile' page

</td></tr><tr><td>

Form Controller

</td><td>

PRB1801102

</td><td>

A screen reader announces an incorrect search result count when typing in the 'Search by name or case number' combo box

</td></tr><tr><td>

Form Controller

</td><td>

PRB1788200

</td><td>

A UI policy on fields with a default value isn't working properly in the portal but is working fine in the native UI

</td></tr><tr><td>

Form Designer

</td><td>

PRB1769298

</td><td>

The **Publish Translations** button on the sn\_lf\_comparison\_ui UI page is stuck if the content preference of GlideModal is a large size

</td></tr><tr><td>

Form Designer

</td><td>

PRB1775459

</td><td>

A menu field search in a form in a Workspace is different than in the platform

</td></tr><tr><td>

Form Designer

</td><td>

PRB1789133

</td><td>

A form-embedded table selection pop-up is hidden upon upgrading to Washington DC

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1732507

</td><td>

GlideRecord.updateMultiple\(\) can generate a different SQL query compared to GlideRecord.query\(\) when an encoded query is used

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1775257

</td><td>

GlideRecord.applyEncodedQuery\(\) with a translated text field can result in a non-English translation to be stored in the base table instead of the sys\_translated\_text table

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1649954

</td><td>

Irregular filtering on reports that follow a report \(pie chart\) interactive filter

</td></tr><tr><td>

GRC Platform Plugins

</td><td>

PRB1817099

</td><td>

Knowledge articles created for policy records have the author value set to 'System'

</td></tr><tr><td>

GRC Platform Plugins

</td><td>

PRB1711138

</td><td>

Audit Management has an incorrect language attribute for non-English users

</td></tr><tr><td>

Guided Application Creator

</td><td>

PRB1772070

</td><td>

Custom application logos break when moving between instances

</td></tr><tr><td>

Guided Tour Designer

</td><td>

PRB1763958

</td><td>

After enabling Next Experience, the guided tour fails at the 'Click on Run' step

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1793649

</td><td>

A tour isn't triggered from the portal and a console error is displayed

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1675866

</td><td>

Tooltips and UI messages aren't translated

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1774385

</td><td>

VoiceOver doesn't announce the name and role of the 'Stop Guided Tour' dialog

</td></tr><tr><td>

Hardware Support and Reliability

</td><td>

PRB1803070

</td><td>

There's inconsistencies in keyboard shortcuts

</td></tr><tr><td>

Health Log Analytics \(Family\)

</td><td>

PRB1808558

</td><td>

Some Health Log Analytics \(HLA\) poller data inputs aren't using the proxy configured for MID

</td></tr><tr><td>

Health Log Analytics \(Family\)

</td><td>

PRB1827423

</td><td>

Elasticsearch \(ES\) data input \(DI\) has slow read throughput

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1805189

</td><td>

Info logging in KafkaConsumerRegistry \(create/close\) is estimated to cost $20K/year in Splunk costs

</td></tr><tr><td>

History Set

</td><td>

PRB1807607

</td><td>

ErrorLogStatsCollector and SyslogStatsCollector prints warning messages for JRobin database

</td></tr><tr><td>

History Set

</td><td>

PRB1806563

</td><td>

Duplicate comments are observed intermittently even after enabling a fix

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1750876

</td><td>

The UI Builder 'Date-time' component partially displays data in the system's preferred language, but not in the user's preferred language

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1764015

</td><td>

The **Collab Chat** &gt; **Discussion Info** &gt; **Subject** tooltip doesn't close unless the user presses 'escape'

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1727953

</td><td>

A Workspace page is stuck when trying to move from 'Home' to 'List' on the landing page

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1741381

</td><td>

The full path to a selected value doesn't display

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1779062

</td><td>

ML solution record in the cluster definition 'ml\_sn\_global\_cases\_need \_knowledge\_cluster' isn't generated even when the job ' \[Knowledge Curation\]: Generate Case Clusters' is executed

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1820502

</td><td>

The **Employee number** field doesn't sync from the user to the HR profile

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1763509

</td><td>

The **Name** field in the sys\_template dictionary is moved to the HR scope

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1803832

</td><td>

When an employee relations case is closed, the **Description** field is hidden

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1773812

</td><td>

An activity set triggers when not expected

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1701340

</td><td>

With the system property 'sn\_hr\_core.impersonateCheck' set to true, users @mentioned in the comments or work notes can't see the record

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1664859

</td><td>

gs.getUser.hasRole\(\) returns false for elevated roles

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1805904

</td><td>

Field ACLs on the 'Interaction' table in the 'Advanced Work Assignment for HRSM' application scope aren't present on the instance

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1817290

</td><td>

HTML is stripped when using **Copy to Clipboard** on the 'Response' template

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1768618

</td><td>

An HR Agent Workspace checklist doesn't refresh after adding a checkbox element

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1788794

</td><td>

The 'Scratchpad: Show HR Service Fields' business rule is causing errors in system logs

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1773138

</td><td>

There's a performance issue on an HR Case form due to the related lists 'Cases for Subject Person' and 'Cases Opened for User'

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1758471

</td><td>

If the user doesn't have access to the parent case, 'Assigned to' and 'assignment group' HR cases are changing when the HR task is moving from 'Ready' to 'WIP' using the UI action **Start Work**

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1786475

</td><td>

The **Create case** button isn't displaying for employee relations cases in Agent Workspace for users in case restriction configurations

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1806235

</td><td>

The Lifecycle Enterprise scope isn't readable for sn\_hr\_le.case\_writer users

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1769848

</td><td>

There's an empty **Element ID** field in the sys\_journal\_field table when creating an incident from Universal Request

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1789021

</td><td>

Performance issue when there are many sysapproval\_approver records assigned to one user

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1811105

</td><td>

Users are unable to create accommodation \[sn\_hr\_er\_accommodation\] records referencing non-Employee Relations cases

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1760021

</td><td>

Inconsistent behavior of column level ACL of the admin override property for sn\_hr\_core\_case table

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1713564

</td><td>

The 'SC Categories' widget's count number is incorrect

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1793474

</td><td>

A discrepancy between instances related to the dictionary field **Restricted access / Locked** deployed from sn\_hr\_er

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1768769

</td><td>

In HR Agent Workspace, playbook cards of the untriggered activities don't reflect the current system's language

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1781549

</td><td>

There's a Canvas error when opening an email attachment from an HR LE Case in HR Agent Workspace

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1793794

</td><td>

'Editing Assigned To' via a list isn't editable for HR agents for HR lifecycle events' cases

</td></tr><tr><td>

HR Service Delivery integration with Adobe Sign

</td><td>

PRB1784154

</td><td>

The 'Create And Send Adobe Sign Agreement' subflow uses a deprecated action

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1796117

</td><td>

The **copy and paste** function isn't working as desired

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1810476

</td><td>

An extra space displays when a client script makes an HTML field read-only

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1773479

</td><td>

Users are unable to attach an image to a KB article template in Service Operations Workspace

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1798036

</td><td>

A null point error should be fixed in PayloadDeduplicator.java, the logging related to failures caused by multiple items in the same payload with the same source native key should be improved

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1780344

</td><td>

Reconciliation rules with a filter aren't working

</td></tr><tr><td>

Identity

</td><td>

PRB1833655

</td><td>

A SCIM user who gets an endpoint has performance issues

</td></tr><tr><td>

Import Set API

</td><td>

PRB1655725

</td><td>

Base instance business rule, 'Update Import Set Complete', appears to be run unnecessarily, causing performance degradation for Synchronous Imports, due to the filter conditions of the query generated

</td></tr><tr><td>

Inbound Email Actions

</td><td>

PRB1790639

</td><td>

Attachments aren't displaying in 'Manage attachments' in the HR records for inbound emails

</td></tr><tr><td>

Inbound Email Actions

</td><td>

PRB1770070

</td><td>

A sys\_attachment is adding '\[object GlideRecord\]' under the table name for universal requests

</td></tr><tr><td>

Incident Management

</td><td>

PRB1779720

</td><td>

The **Open in Dependency Views** button doesn't have role=button

</td></tr><tr><td>

Incident Management

</td><td>

PRB1820577

</td><td>

In Xanadu, the email scripts incident\_assigned\_to and incident\_assigned\_to\_you don't consider language translation

</td></tr><tr><td>

Incident Management

</td><td>

PRB1792555

</td><td>

A base instance email notification triggered in the Workspace is invisible when the dark theme is enabled

</td></tr><tr><td>

Incident Management

</td><td>

PRB1801533

</td><td>

The 'Cascade closure of Incident Tasks' business rule increments \[incident\_task\] records for the **Number** field

</td></tr><tr><td>

Incident Management

</td><td>

PRB1806120

</td><td>

The 'Application Service Populated by Dynamic' CI group is unpacked

</td></tr><tr><td>

Innovation Management

</td><td>

PRB1824475

</td><td>

An HTML type field toolbar option is missing in an Xanadu upgrade

</td></tr><tr><td>

Install Base Management

</td><td>

PRB1786211

</td><td>

The 'Account Page \(Case View\) Sold Product' related list must be updated with the default filter condition

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1780273

</td><td>

There's a NullPointerException \(NPE\) in the IDRProducerJob which prevents the cursor from advancing and halts all replication

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1726801

</td><td>

A consumer replication entry isn't found for a table sys\_attachment or sys\_attachment\_doc

</td></tr><tr><td>

Instance Scan

</td><td>

PRB1797592

</td><td>

Running a scoped app scan through the Continuous Integration/Continuous Delivery \(CICD\) spoke returns different results than running it manually

</td></tr><tr><td>

Instance Scan

</td><td>

PRB1769556

</td><td>

The **State** field on 'Scan Task' records mark the form inactive when changing to the 'On Hold' state

</td></tr><tr><td>

Instance Security Center \(no longer supported\)

</td><td>

PRB1812211

</td><td>

A flow isn't coming in the scan finding even though Glide Encrypter is present

</td></tr><tr><td>

Integration Authentication

</td><td>

PRB1817367

</td><td>

Authentication isn't working when a KID isn't received in a token but is available in a well-known configuration

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1821284

</td><td>

The 'Transform' script isn't executed in engine v2

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1780194

</td><td>

A data stream action fails with 'Undefined Schema' when a dynamic object is used as an output in a Washington release

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1784518

</td><td>

The 'Retry' policy doesn't retry for a connection timeout

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1780698

</td><td>

There's JDBC step connections issues with the Sybase database

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1733045

</td><td>

The error 'JSONObject\['value'\] not found' appears when using the Slack webhook with Flow Designer for the **Post a message** action

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1832371

</td><td>

Unable to decrypt a password which is encrypted with ParameterEncrypter

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1792336

</td><td>

An HR task is closed with a 'Closed Incomplete' state instead of 'Closed Complete', unlike its parent HR case

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1780355

</td><td>

The **Override Default Port** field value in an ADv2 connection record isn't picked up in flows and actions with the PowerShell step

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1775463

</td><td>

There's a data stream action when JDBC requests retrieves more than 20 records when run from the **Test** button

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1774674

</td><td>

There's an incorrect data type for an action output, which returns a blank output

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1782980

</td><td>

The script-side StrictReject map for the Glide\_hub\_flow\_ engine\_Glideencrypter crypto module causes an 'access denied' error

</td></tr><tr><td>

Integration Hub Stream Connect

</td><td>

PRB1826240

</td><td>

Logging from HubKafkaProducer is building up disk space for a syslog table

</td></tr><tr><td>

Interaction Management API

</td><td>

PRB1813985

</td><td>

On an interaction record, the **Create incident** UI action doesn't copy all of the attachments

</td></tr><tr><td>

Interactive Filters

</td><td>

PRB1765505

</td><td>

There's numerous RhinoEcmaErrors posted in the logs

</td></tr><tr><td>

Interactive Filters

</td><td>

PRB1837354

</td><td>

Filters no longer support reference list types

</td></tr><tr><td>

Interactive Filters

</td><td>

PRB1779331

</td><td>

Incremental search doesn't work in 'Select Multiple Input' when using the 'OR' condition

</td></tr><tr><td>

Internationalization Features

</td><td>

PRB1787388

</td><td>

After upgrading to Washington DC, getDisplayValueLang\(\) doesn't return the expected results

</td></tr><tr><td>

Internationalization Features

</td><td>

PRB1773540

</td><td>

The sys\_documentation plural is set to 's' if an instance is set in a language other than default

</td></tr><tr><td>

Internationalization Features

</td><td>

PRB1794234

</td><td>

'Gs.getMessage\(\)' returns the incorrect record when a similar record exists where the **CODE** field is populated

</td></tr><tr><td>

Internationalization Features

</td><td>

PRB1809283

</td><td>

getDisplayValueLang\(\) isn't returning translated records from the sys\_choice table

</td></tr><tr><td>

Investment Portal

</td><td>

PRB1793722

</td><td>

The **Budget** field displays the value in GBP instead of USD on the Investment Portal

</td></tr><tr><td>

JVM at Scale

</td><td>

PRB1783344

</td><td>

MetaspaceSize is set instead of MaxMetaspaceSize

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1681795

</td><td>

There's a response time spike for an authorization check during a 20 K agents' test

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1777352

</td><td>

Cloned data encrypted by a revoked key on a source isn't properly decrypted on target

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1771941

</td><td>

The existing script include in the Smart Operations application requires access to the Key Management Framework script include 'sn\_kmf.ScopedRevokeCertificate'

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1762398

</td><td>

The database view 'sn\_kmf\_crypto\_user\_policy' fails on Postgres instances

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1610580

</td><td>

Next Experience dark theme issues

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1794818

</td><td>

Vancouver instances with Washington DC data may fail to come online after being upgraded to Xanadu

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1798919

</td><td>

A null pointer exception is observed when the input text for SYMMETRIC\_ENCRYPTION contains ':'

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1792500

</td><td>

The u\_crypto\_specification\_list Reference Qualifier Condition isn't being updated upon upgrade

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1831035

</td><td>

A KB isn't displaying the latest category updates

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1761530

</td><td>

'Articles updated in the last 30 days' displays an incorrect number of knowledge base articles

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1810451

</td><td>

The **Preview Article with Blocks** UI action doesn't work as expected

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1793096

</td><td>

Agent Assist isn't opening an attachment as expected

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1796353

</td><td>

The Knowledge Base 'Most recent tasks' has duplicate tasks

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1815949

</td><td>

Screen readers fail to announce the group label 'Most viewed articles'

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1815536

</td><td>

There's an incorrect ACL description for activating/deactivating knowledge base categories, and it should include CanContribute and CanRead users

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1799957

</td><td>

'Add a comment/leave a comment' is displayed on the kb\_view page \(itil view\) when the KB article is in the 'Published' state only

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1758385

</td><td>

The 'Update Replacement Article References' business rule runs recursive

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1790956

</td><td>

The replacement article feature isn't working with versioning when a URL contains a sys\_id

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1770500

</td><td>

A knowledge version dropdown isn't visible when an article is in the 'Draft/review' state

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1791996

</td><td>

Fix for empty attributes in the TinyMCE Version 6 upgrade

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1768407

</td><td>

The **Request Translation** UI action can be used multiple times for the same language on any knowledge article that has a version higher than 1

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1797234

</td><td>

Two sections on a knowledge template are displaying in the same paragraph

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1786651

</td><td>

The user hasn't updated a Knowledge Base \(KB\) article, but it shows as 'updated a while ago'

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1787754

</td><td>

The **Ignore collection** button on the demand insight dashboard isn't updating records

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1798961

</td><td>

The 'Demand Insight' dashboard for incidents isn't displaying for Xanadu

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1802359

</td><td>

The 'Knowledge Management Overview' dashboard is missing

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1799143

</td><td>

An external user using the supplier portal in a Chrome browser visiting the 'Knowledge' page sees the list of knowledge articles along with a book icon that's alt text is read by a screen reader

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1820355

</td><td>

A knowledge record isn't found when using a record number in a sysparm\_article in an URL and the record is a child table of kb\_knowledge

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1770302

</td><td>

In Customer Service Management Workspace, article translation isn't working

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1805967

</td><td>

The **View as user** functionality doesn't display the language picker on the 'Article' form if the manager doesn't have access to the parent article

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1780330

</td><td>

When deleting a ranting record in kb\_feedback, the article still has the ranting value

</td></tr><tr><td>

Knowledge Management Advanced

</td><td>

PRB1746023

</td><td>

There's a navigation issue when using 'Article Template Selector' to create an article on the platform

</td></tr><tr><td>

KPI Details

</td><td>

PRB1824277

</td><td>

There's an error in target configurations on Analytics Hub

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1759629

</td><td>

The Japanese translation for 'In Review' is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1745536

</td><td>

The Japanese translation for the **Close Task** button is incorrect after upgrading Service Operations Workspace ITSM Applications's version to 4.1.0

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1799672

</td><td>

Unable to translate tooltips 'Submit Search' and 'Clear recent search:' in the Typeahead Search widget on the portal

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1767102

</td><td>

There's an incorrect translation for a tab label

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1785458

</td><td>

The German translation isn't as expected for 'users'

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1758530

</td><td>

Field labels aren't as expected for German translations

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1732908

</td><td>

There's a French language translation issue with the word 'Corriger' after upgrading

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1732930

</td><td>

There's French language translation issues with the word 'Terminer' after upgrading

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1730640

</td><td>

The translation of the label 'State' in German is incorrect, displaying 'Bundesland/Kanton'

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1787884

</td><td>

There's a translation error on automatic session expiry in the activated German language package

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1767782

</td><td>

In the Japanese translation of the sys\_ui\_message table, the 'key: completed' message is translated incorrectly from '完了' to '完了日時'

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1790479

</td><td>

The field label 'To' isn't translated into Japanese on the 'Announcement' table

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1766928

</td><td>

The Japanese translation of 'sys\_mod\_cont' is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1835314

</td><td>

Search isn't working as expected in the sc\_cat\_item table when a catalog item is created in non-English, and is updated in the English language only in an Oracle DB instance

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1771285

</td><td>

There's an incorrect German translation of 'content' in the sys\_ui\_message table

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1767922

</td><td>

On the dashboard calendar element, the German translation for 'day' and 'month' aren't given anymore

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1791541

</td><td>

There's an incorrect German translation for 'Last sync with store'

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1791464

</td><td>

There's multiple mistranslations in Environmental, Social, and Governance \(ESG\) Workspace

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1782092

</td><td>

In the Thai language, there's extra brackets for the **Rename** button in both the prefix and suffix

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1734668

</td><td>

On a change request form, 'Authorize' has different Japanese translations displayed on Flow formatter and the **State** field

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1657392

</td><td>

The French translation of 'todos' is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1769027

</td><td>

Kyrilian letters in a Swedish translation

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1790665

</td><td>

Date picker variables in portal glitch when making a selection in a French language session when 'Day of week' is set to Monday

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1773807

</td><td>

In Catalog Builder, the choices for the name of the **Submit** button aren't correctly translated in German

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1772198

</td><td>

A 'YYYY-MM-DD' message is translated incorrectly in French

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1777958

</td><td>

There's a missing Norwegian translation for 'Lists' in Configurable Workspace

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1778076

</td><td>

There's an incorrect translation for the 'next maintenance schedule' key for the French - Canada language

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1738398

</td><td>

Incorrect translation of the UX List Category \(sys\_ux\_list\_category\) 'Tasks' as 'Problemer' instead of 'Oppgaver' in the Norwegian language

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1790953

</td><td>

There's a discrepancy in translation entries for a sys\_user with preferred\_language choices for different languages

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1740940

</td><td>

The translation for '\{0\} y ago' is incorrect in the Norwegian language

</td></tr><tr><td>

LDAP integration

</td><td>

PRB1769261

</td><td>

LDAP errors are reported as 'INFO' in the agent0.log file

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1797927

</td><td>

When activity set context records are inaccessible, activity sets with the date type 'trigger' are triggered even when the conditions aren't met

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1816966

</td><td>

Script include hr\_ActivitySet triggers a slow query

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1781489

</td><td>

A reference qualifier on the **Catalog item** field on the 'Activity' table allows Record Producer to be selected

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1797841

</td><td>

Reports can't be shared in the Lifecycle Events Enterprise scope

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1828561

</td><td>

The Lifecycle Event testing feature may error when there are a large number of activities or activity sets

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1794815

</td><td>

Activity sets error out when the activity field mapping refers to a menu with no value set

</td></tr><tr><td>

List Administration

</td><td>

PRB1817887

</td><td>

The Ctrl + A shortcut doesn't work for selecting choices in a filter for Windows

</td></tr><tr><td>

List Administration

</td><td>

PRB1724625

</td><td>

A hint displays a value of a different line in a Workspace when moving the cursor through the up/down key on the keyboard

</td></tr><tr><td>

List Administration

</td><td>

PRB1787584

</td><td>

The multiple-sorting feature isn't working in a Workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB1809729

</td><td>

When opening the database view record from a list, the view isn't the same as the list

</td></tr><tr><td>

List Administration

</td><td>

PRB1831052

</td><td>

A screen reader fails to announce the loading status and filtered results

</td></tr><tr><td>

List Administration

</td><td>

PRB1790302

</td><td>

The user isn't able to toggle the currency on Workspaces

</td></tr><tr><td>

List Administration

</td><td>

PRB1783350

</td><td>

In Service Operations Workspace, header info isn't announced for the **Cell Filter** button when navigating in a list

</td></tr><tr><td>

List Administration

</td><td>

PRB1826163

</td><td>

A list declarative action isn't working in the 'New List' page template

</td></tr><tr><td>

List Administration

</td><td>

PRB1790759

</td><td>

For extensible lists, removing a filter on the GroupBy list returns an error

</td></tr><tr><td>

List Administration

</td><td>

PRB1800573

</td><td>

GlideTransaction isn't allowed in scoped applications when trying to access any record in the 'My UX' list \(sys\_ux\_my\_list\)

</td></tr><tr><td>

List Administration

</td><td>

PRB1817332

</td><td>

Non-admin users are unable to remove tags from the list view for Workspaces

</td></tr><tr><td>

List Administration

</td><td>

PRB1778664

</td><td>

In a Workspace list, an error is thrown even though there's no issue: 'rows removed from this list by security constraints'

</td></tr><tr><td>

List Administration

</td><td>

PRB1818512

</td><td>

The list UI action **Remove Tag** isn't working

</td></tr><tr><td>

List Administration

</td><td>

PRB1784038

</td><td>

When navigating **Dashboard** &gt; **List** &gt; **Simple widget**, users are unable to add more than 5 columns to the list

</td></tr><tr><td>

List Administration

</td><td>

PRB1821700

</td><td>

On an extensible list, users are unable to create an incident

</td></tr><tr><td>

List Administration

</td><td>

PRB1823795

</td><td>

The **Assigned to** field incorrectly accepts arbitrary email addresses when list editing in a Workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB1766624

</td><td>

The term '\_Copy' that is appended to the end of Workspace lists' titles isn't translated when using 'Save as'

</td></tr><tr><td>

List Administration

</td><td>

PRB1795815

</td><td>

Sum isn't working on the list type reports and isn't aligned properly

</td></tr><tr><td>

List Administration

</td><td>

PRB1776103

</td><td>

Column personalization isn't working

</td></tr><tr><td>

List Administration

</td><td>

PRB1795793

</td><td>

A concatenation issue causes a grammar error in some target languages

</td></tr><tr><td>

List Editor

</td><td>

PRB1708419

</td><td>

Edit of choice list fails at cmdb\_ci list on the extended table's field

</td></tr><tr><td>

List Filters

</td><td>

PRB1776207

</td><td>

The translation of sys\_filter is stuck in one language

</td></tr><tr><td>

List Search

</td><td>

PRB1763145

</td><td>

Search behavior changed to 'Starts with' in Washington DC when adding columns to a list view in Configurable Workspace

</td></tr><tr><td>

List Views

</td><td>

PRB1799889

</td><td>

Users aren't able to set a view for a 'Quick edit' form

</td></tr><tr><td>

List Views

</td><td>

PRB1805254

</td><td>

A Workspace list displays a truncated date/time value when the month token is 'MMM'

</td></tr><tr><td>

Localization Framework

</td><td>

PRB1792674

</td><td>

The string 'updated\_capital' is incorrectly disambiguated

</td></tr><tr><td>

Localization Framework

</td><td>

PRB1833815

</td><td>

The **Source Code** button in translations doesn't display code and is blank in Xanadu

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1780126

</td><td>

The read ACL 'incident.actions\_taken' is using an itil role instead of fine-grained roles

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1791586

</td><td>

A blank choice appears when adding a collaborative communication task in the Major Incident Workbench after upgrading the Service Operations Workspace \(SOW\)

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1800008

</td><td>

Sn\_incident\_read + comm\_plan\_admin / Sn\_incident\_read+comm\_plan\_manager aren't able to compose a communication task but are able to initiate a 'Collaborate' task

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1790971

</td><td>

Resolution code choices aren't in the correct sequence/order

</td></tr><tr><td>

Managed Documents

</td><td>

PRB1774735

</td><td>

Focus isn't working as expected on dialog boxes in managed documents

</td></tr><tr><td>

MetricBase

</td><td>

PRB1728947

</td><td>

Registering a large number of triggers with Clotho causes some triggers to not get registered

</td></tr><tr><td>

Metric Intelligence \(Family\)

</td><td>

PRB1766872

</td><td>

The exception thrown during TimeSeriesModelLearner Service.runModelComparisonJob\(\) prevents the training results from being saved

</td></tr><tr><td>

MID Server

</td><td>

PRB1763232

</td><td>

'Host core count' MID Server displays the number of processors as opposed to the number of cores

</td></tr><tr><td>

MID Server

</td><td>

PRB1791982

</td><td>

Configure.sh doesn't consider proxy server settings

</td></tr><tr><td>

MID Server

</td><td>

PRB1801758

</td><td>

The JEAUtils MID Server script reports that a certificate is available even if it's not found

</td></tr><tr><td>

MID Server

</td><td>

PRB1790075

</td><td>

MID Server fails to process config\_publish, raising a null pointer exception

</td></tr><tr><td>

MID Server

</td><td>

PRB1796306

</td><td>

The Windows Installed Software probe doesn't honor the wmi\_timeout when using the WMI protocol

</td></tr><tr><td>

MID Server

</td><td>

PRB1825232

</td><td>

The reload\_credentials event triggers a flush and the close of all in use connections in ConnectionCache

</td></tr><tr><td>

MID Server

</td><td>

PRB1813788

</td><td>

MID Servers go down when loading the ecc\_agent\_property table

</td></tr><tr><td>

MID Server

</td><td>

PRB1793947

</td><td>

SessionLimitHandler leaks 'sessions' after Discovery cancellation

</td></tr><tr><td>

MID Server

</td><td>

PRB1823815

</td><td>

MID Server resource reservation doesn't work for PowerShell

</td></tr><tr><td>

MID Server

</td><td>

PRB1799161

</td><td>

A Windows-hosted MID Server can't discover itself

</td></tr><tr><td>

MID Server

</td><td>

PRB1771741

</td><td>

Discovery of a device via WinRM fails with invalid credentials

</td></tr><tr><td>

Mobile Experience for Field Service Management

</td><td>

PRB1817140

</td><td>

Menu choices are displaying all the values regardless of the logged in user's language in the Mobile app

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1801412

</td><td>

Using deprecated **FCM** field time\_to\_live results in a silent push not being delivered to Android devices

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1813775

</td><td>

In Mobile Virtual Agent, Chathandshake has an issue with global context data passing

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1806539

</td><td>

In incremental mode, a situation may arise in which the same incremental generation task for the same screen and the same offline result is executed multiple times, one after another

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1649489

</td><td>

Selecting **Submit** navigates to the sys\_id in the 'add to drop off list' flow

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1801996

</td><td>

Input form screens with scripted autofill variables aren't properly supported in the mobile 'offline' mode

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1819193

</td><td>

'Screen field' isn't displayed in the ServiceNow Mobile Agent due to truncation

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1767562

</td><td>

The Mobile URL function with record context re-encodes the parameters of URLs

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1794493

</td><td>

Offline cache attachment docs aren't deleted by the sys\_auto\_flush job after deleting the respective attachments

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1787462

</td><td>

Buttons/function instances that use scripted variables causes instance outages when in 'offline' mode

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1811954

</td><td>

DocumentData aren't saved to the SQLlite database

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1818461

</td><td>

A list screen with the data item/list configuration with the 'IS' condition on a string field isn't displaying records that match it in when in offline mode

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1830851

</td><td>

The UI rule action with the operation type 'Set Mandatory' isn't reversible on the Agent App

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB1799411

</td><td>

Multi-factor authentication locks out users

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB1814364

</td><td>

Multi-factor authentication's flow is broken after cloning from Vancouver to Xanadu

</td></tr><tr><td>

Next Experience Favorites Menu

</td><td>

PRB1789009

</td><td>

Users are unable to drag and drop items in a new custom group of the 'Edit your Favorites' dialog

</td></tr><tr><td>

Next Experience integration with Help

</td><td>

PRB1823980

</td><td>

HTML wraps elements in &lt;div&gt; tags instead of semantic tags, which affects accessibility

</td></tr><tr><td>

Next Experience integration with Help

</td><td>

PRB1789530

</td><td>

Multiple button and link controls lack an accessible label

</td></tr><tr><td>

Next Experience Notifications Menu

</td><td>

PRB1774792

</td><td>

There's a Next Experience notification style issue

</td></tr><tr><td>

Next Experience Notifications Menu

</td><td>

PRB1786375

</td><td>

The **Message heading** field isn't required in the 'sys\_notification\_ next\_experience\_content' form, but the feature breaks without it

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1792732

</td><td>

Next Experience's impersonate is much slower than UI16's impersonate

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1825781

</td><td>

An error isn't identified when a required field is empty in the 'Favorite added' pop-up

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1816636

</td><td>

There's an inaccurate name provided and the state is missing for the **Notification** button

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1798771

</td><td>

A screen reader announces a lot of information when the domain scope pop-up is opened

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1832975

</td><td>

Pressing the **Back** button shows two pop-up boxes after upgrading to Xanadu

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1825876

</td><td>

Snc\_external users can't pin their navigation menus like 'All', 'Favorites', 'History', or 'Workspaces'

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1768697

</td><td>

Avatar tooltip in Next Experience isn't translated \(or translatable\)

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1820116

</td><td>

Applications in a configured menu don't display after the user switches domains

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1767291

</td><td>

Dictionary entry override records have text and backgrounds in a white color in the dark theme

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1774879

</td><td>

Next Experience keyboard shortcuts for applying focus aren't working, including 'Global search', 'Main content of a page', and 'Breadcrumb navigation'

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1822620

</td><td>

The system timezone sys\_choice value isn't updated from the update set

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1779558

</td><td>

A domain with children whose entire hierarchy is turned off still appears in the domain picker

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1827934

</td><td>

Next Experience App Shell doesn't navigate to an external URL from SN\_SEARCH\_INPUT \_WRAPPER\#ITEM\_SELECTED

</td></tr><tr><td>

Next Experience User Menu

</td><td>

PRB1798238

</td><td>

The 'Enable Keyboard Shortucts' tooltip contains several accessibility issues for non-sighted/keyboard-only users

</td></tr><tr><td>

Normalization Data Services

</td><td>

PRB1763244

</td><td>

Core\_company records are updated without an actual data change in CanonicalUpdater

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1744300

</td><td>

A notification badge doesn't appear until the tray \(sn-contextual-menu\) is opened with Next Experience turned off

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1806559

</td><td>

A complete list of subscription notifications isn't displayed in the drop down list

</td></tr><tr><td>

Notify

</td><td>

PRB1772835

</td><td>

An invalid user isn't highlighted in red on the 'Notify conference call' modal

</td></tr><tr><td>

Notify integration with Twilio Direct

</td><td>

PRB1792157

</td><td>

The TimeOut attribute isn't passed over in a dial action \(Forward Call\) action to Twilio

</td></tr><tr><td>

Now Experience Framework

</td><td>

PRB1794726

</td><td>

In Service Operations Workspace, the removal of tags from a record isn't working as expected

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1761257

</td><td>

There's a missing translation for the words 'Approve' and 'Reject' on a pop-up message

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1817203

</td><td>

Users are unable to open a module when the **sys\_app\_module .window\_name** field has a value

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1781438

</td><td>

On-call workflows aren't updating the **assigned\_to** field when an incident escalation is accepted

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1821423

</td><td>

On-call message numbers records are deleted when a group escalates to another group

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1806718

</td><td>

On-call reminders are set up for 4 days lead time, but people are sent reminders both 4 days and 11 days ahead of their on-call assignment

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1808531

</td><td>

If a Twilio call fails during on-call scheduling, errors aren't reported in the work notes

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1788633

</td><td>

Selecting the 'Primary user' icon opens multiple cards in on-call schedules

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1815212

</td><td>

Users get duplicate members in the 'Schedule' report

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1805914

</td><td>

Daily, weekly or biweekly rotation is skipped in November

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1814433

</td><td>

The 'Reminder Report' displays in an incorrect format

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1791835

</td><td>

Escalation step window dimensions aren't displaying correctly

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1807599

</td><td>

On-call escalation acknowledgments are sporadically not recorded

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1822244

</td><td>

OnCallCommonSNC getGroupMemberCount\(\) doesn't scale when cmn\_rota\_member has large record counts

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1822461

</td><td>

An incorrect member count is displayed for the 'On-Call Scheduling' group

</td></tr><tr><td>

Oracle Reconciliation

</td><td>

PRB1788175

</td><td>

Processor factor mapping is missing the Oracle core factor entry for a CPU name containing 'EPYC'

</td></tr><tr><td>

Oracle Reconciliation

</td><td>

PRB1773579

</td><td>

Oracle recon fails if the normalized version/edition is empty

</td></tr><tr><td>

Oracle Reconciliation

</td><td>

PRB1782004

</td><td>

Oracle DB option's 'Unlicensed options' list view filter is incorrect when accessed from the publisher result

</td></tr><tr><td>

Oracle Reconciliation

</td><td>

PRB1794653

</td><td>

Oracle per processer licenses require a value set to be too large and hit the max integer limit \(2,147,483,647 \)

</td></tr><tr><td>

Oracle Reconciliation

</td><td>

PRB1790926

</td><td>

Some cmdb\_sam\_sw\_install tables with more than 100 K installed\_on devices for the same software product is reconciled unlicensed when there's available rights

</td></tr><tr><td>

Password Reset

</td><td>

PRB1830139

</td><td>

SMS verification isn't working in 'Service Desk Password Reset' and enrollment modules after an Xanadu upgrade

</td></tr><tr><td>

PDF Generation

</td><td>

PRB1811475

</td><td>

When com.snc.pdf.chinese\_fonts.enabled is turned off, certain Japanese characters are broken on a PDF export

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1807990

</td><td>

The itil role isn't available when attempting to share a dashboard to users with itil

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1817989

</td><td>

The 'Daily Data Collection' job takes longer after upgrading to Xanadu

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1814716

</td><td>

Calendar reports aren't displaying variables \(questions\) in Platform Analytics Workspace dashboards

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1793513

</td><td>

The filter on the 'Word cloud' widget doesn't work when users select a special character

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1774395

</td><td>

Setting a date period with the start after the end in an indicator breaks the page

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1784482

</td><td>

Users who have more then 40 characters in their username can't edit a dashboard

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1826829

</td><td>

A formula on formula indicator displays a breakdown element in a different language \(pb\) and can't be changed

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1782062

</td><td>

A bar chart / pie chart created from list view of a table shows the info message 'This report has been migrated to a visualization.'

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1775894

</td><td>

In HSQL Data Collector, there's an incorrect score value calculation for COUNT DISTINCT on the scripted indicator

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1781598

</td><td>

Dashboard groups aren't visible to no-role users

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1813576

</td><td>

There's issues with KPI Details's 'On View &gt; select' query

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1824024

</td><td>

Platform Analytics's 'Administration' menu is missing when upgraded from Vancouver to Xanadu

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1769317

</td><td>

The homepage deprecation tool skips pages for conversion

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1798784

</td><td>

The default month on 'KPI Details' isn't the same on Analytics Hub

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1781569

</td><td>

pa\_tabs.name is changed after update set transfers

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1796348

</td><td>

There's an issue with redirecting to home.do in the Core Ul dashboard after enabling the migration of the Core Ul analytics artifacts to Platform Analytics Experience

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1807347

</td><td>

Report widget titles are truncated on smaller widgets in dashboards

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1767652

</td><td>

A reference field from a dashboard doesn't respect the current theme colors

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1819922

</td><td>

The 'Last visited dashboard' feature isn't working in Platform Analytics

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1807150

</td><td>

If a dashboard has no creator in the ACLs, there's a null pointer exception

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1806689

</td><td>

Users are unable to translate a visualization title as a part of localization

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1779020

</td><td>

Emojis are displayed as encoded text in the Platform Analytics dashboard's title

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1781006

</td><td>

Dashboards, Data Visualizations, and Scheduled Exports are set to have been created by the user who ran 'Platform Analytics Migration' instead of the original

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1820860

</td><td>

Chart titles and dates on the Platform Analytics dashboard \(migrated dashboards\) aren't translated to Brazilian Portuguese

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1797830

</td><td>

Dashboard visibility filtering isn't working

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1796809

</td><td>

Platform Analytics \(PA\) filters don't apply to the compatibility mode PA widgets in migrated dashboards

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1823136

</td><td>

Reference fields are displayed as choice fields for some filters configurations

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1716392

</td><td>

Changing the sorting direction reset unapplies the value selection

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1788647

</td><td>

Users are unable to create a scripted filter in UI Builder

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1746111

</td><td>

Filter is unable to apply to data visualization amid reducing the system property value 'com.snc.pa.scorecards. max\_breakdown\_elements'

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1799486

</td><td>

A filter pop-up window opens when selecting an empty area

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1790312

</td><td>

Visualizations don't display visualization types' values \(for migrated visualizations\) when a report is migrated

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1793305

</td><td>

If individual dashboards have been rolled back, migration rollback fails an activation step

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1788955

</td><td>

The Core UI dashboard list **Delete migrated Experience Dashboard** action isn't working as expected

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1792035

</td><td>

Scheduled export migration for Excel files instead becomes a PDF in the output

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1794750

</td><td>

The legacy component 'Edit' is disabled for some widgets

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1802121

</td><td>

com.Glide.par.coreui .migration.enabled doesn't block migration activation

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1820684

</td><td>

Some legacy dashboard widgets don't render

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1797230

</td><td>

There's an incorrect color configuration migration for a pivot chart

</td></tr><tr><td>

Platform Licensing

</td><td>

PRB1772092

</td><td>

Move updateTableLicensingConfig outside the 'Upgrade' thread

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1799122

</td><td>

There's false-positive notifications about memory pressure after switching to ParallelGC

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1723055

</td><td>

add-user.sh fails with a java.lang.ClassCastException error in some self-hosted environments in Vancouver

</td></tr><tr><td>

Playbook Experience Core

</td><td>

PRB1815880

</td><td>

The 'UI Message' table should be populated during the activation of a playbook

</td></tr><tr><td>

Playbook Experience Core

</td><td>

PRB1800290

</td><td>

The **Playbook** UI action throws the error 'Process Definition is missing or inactive' when creating the playbook under the custom application's global scope

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1790392

</td><td>

Inactive fields still display in dotwalk data

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1801892

</td><td>

The modify condition list is empty in Playbooks

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1817167

</td><td>

The max length of field form fields \(table : sys\_pd\_activity\_type\_prop\) on an activity definition is set to 255, which doesn't match the matching subflow's length of 2000

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1811034

</td><td>

Decision branches aren't evaluated if activities use 'Start with delay' with an explicit duration of over 10 seconds

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1781302

</td><td>

Processes created in Paris and opened post-Paris have a lane order set to -1

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1834463

</td><td>

Process Automation Designer isn't able to pass a previous activity state as a subflow input

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB1806671

</td><td>

The cluster detail purge logic is deleting less records set by the MAX\_ML\_CLUSTER\_ DETAIL\_PURGE\_COUNT

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB1821890

</td><td>

The 'Cluster Concept' text isn't aligned/missing inside the 'Cluster Concept' tile

</td></tr><tr><td>

Predictive Intelligence for Knowledge Management

</td><td>

PRB1783818

</td><td>

The 'Related Article' widget isn't displaying knowledge articles from the 'Knowledge Similar Articles' solution

</td></tr><tr><td>

Predictive Intelligence Workbench

</td><td>

PRB1648059

</td><td>

There is a time out due to a high volume of data

</td></tr><tr><td>

Proactive Analytics

</td><td>

PRB1800161

</td><td>

Signal insights aren't generated for large data sets

</td></tr><tr><td>

Problem Management

</td><td>

PRB1821400

</td><td>

Unable to turn off an interceptor when creating a problem task from the 'problem record' related list

</td></tr><tr><td>

Problem Management

</td><td>

PRB1777062

</td><td>

There's a duplicate link to problem actions

</td></tr><tr><td>

Process Mining

</td><td>

PRB1799323

</td><td>

There's a time out during a filter set data upload to a trainer

</td></tr><tr><td>

Process Mining

</td><td>

PRB1829338

</td><td>

Full mining isn't triggered from platform when localization is enabled

</td></tr><tr><td>

Process Mining

</td><td>

PRB1782656

</td><td>

The saved filter that sets the containing 'findingId' causes mining to fail

</td></tr><tr><td>

Procurement

</td><td>

PRB1774520

</td><td>

Received items's 'Select All/Unselect All' isn't working

</td></tr><tr><td>

Procurement

</td><td>

PRB1808248

</td><td>

A purchase order can't handle an empty value with a currency code

</td></tr><tr><td>

Procurement

</td><td>

PRB1812830

</td><td>

'PO receive' displays in-transit assets that are already received

</td></tr><tr><td>

Project Management

</td><td>

PRB1819562

</td><td>

There's a dark mode list issue on 'First' and 'New Project Status Report'

</td></tr><tr><td>

Project Management

</td><td>

PRB1789953

</td><td>

After configuring 'Planning Console Column Advanced' for two custom fields, both fields on the Investment Portal are displaying the fiscal year data instead of the cost budget values

</td></tr><tr><td>

Project Management

</td><td>

PRB1786638

</td><td>

The pm\_project\_task \(planned\_task\) end date calculation when changing the duration is incorrect in any other system time zone besides GMT

</td></tr><tr><td>

Project Management

</td><td>

PRB1813072

</td><td>

If users try to create a cost plan while in the expense line, they are given an 'Invalid Update' error

</td></tr><tr><td>

Project Management

</td><td>

PRB1783283

</td><td>

Highest order implementation overwrites the lower of the taskFormatter method when there are multiple implementations of the extension point MSProjectImportTaskFormatter

</td></tr><tr><td>

Project Management

</td><td>

PRB1790355

</td><td>

An investment portal 'view project' link results in a blank page

</td></tr><tr><td>

Project Management

</td><td>

PRB1791942

</td><td>

In Project Management resource planning, domain separation isn't working as expected

</td></tr><tr><td>

Project Management

</td><td>

PRB1786998

</td><td>

Remove sn\_spm\_financial\_user to project\_manager and demand\_manager

</td></tr><tr><td>

Project Management

</td><td>

PRB1781954

</td><td>

The UI policy 'Mark Capex/Opex Cost Read Only if Stories are Linked' throws error on the Service Portal

</td></tr><tr><td>

Project Management

</td><td>

PRB1711919

</td><td>

Values under 1000 don't copy into the 'Benefit Plan' grid in the Planning Console

</td></tr><tr><td>

Project Management

</td><td>

PRB1804384

</td><td>

There's an issue with the **Business Unit** field and the **Department** field in a 'Demand' record

</td></tr><tr><td>

Project Management

</td><td>

PRB1798787

</td><td>

Copying a project task using the **Copy Partial Project** UI action displays an incorrectly calculated **Duration** field on the copied project task​

</td></tr><tr><td>

Project Management

</td><td>

PRB1770899

</td><td>

The **Expense Type** field isn't carried over when converting 'Demand' to 'Project'

</td></tr><tr><td>

Project Management

</td><td>

PRB1787721

</td><td>

Missing file extension \(.xls\) when a project name contains \(.\)

</td></tr><tr><td>

Project Management

</td><td>

PRB1773177

</td><td>

The **Actual benefits in project currency** field isn't using the project currency after creation from 'Demand'

</td></tr><tr><td>

Project Management

</td><td>

PRB1825183

</td><td>

Incorrect currency conversion when rolling-up costs

</td></tr><tr><td>

Project Management

</td><td>

PRB1797917

</td><td>

The user is unable to create a project template via the 'Save as New Template' related link with the project\_manager role

</td></tr><tr><td>

Project Management

</td><td>

PRB1812212

</td><td>

The **Percentage completed** field doesn't load when exporting projects to MS project

</td></tr><tr><td>

Project Management

</td><td>

PRB1768726

</td><td>

The classic 'Project Financials' page doesn't use the project currency symbol on some widgets

</td></tr><tr><td>

Project Portfolio Management

</td><td>

PRB1801674

</td><td>

In the program workbench, 'zoom level' &gt; 'auto fit' doesn't work until a column is resized

</td></tr><tr><td>

Project Portfolio Management

</td><td>

PRB1775917

</td><td>

'Print a planning console' in the first level is broken

</td></tr><tr><td>

Project Portfolio Management

</td><td>

PRB1795829

</td><td>

GlideScriptedExtension DemandConversionFieldMap isn't working

</td></tr><tr><td>

Related Lists

</td><td>

PRB1773093

</td><td>

Cannot add multiple records in the slush bucket when 'Enable accessibility in classic' is turned on

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

</td><td>

PRB1682672

</td><td>

Users report bugs in the Remote Process Synchronization official documentation

</td></tr><tr><td>

Remote Tables

</td><td>

PRB1772531

</td><td>

An aggregate query with a condition doesn't work for a remote table with enhanced capacity enabled

</td></tr><tr><td>

Remote Tables

</td><td>

PRB1768173

</td><td>

Runaway regex match kill operations take a long time

</td></tr><tr><td>

Report Designer

</td><td>

PRB1792138

</td><td>

There's an incorrect role provided for 'Day', 'Week', 'Month', and 'Year' controls

</td></tr><tr><td>

Report Designer

</td><td>

PRB1819673

</td><td>

Viewing reports as a non-admin can create unnecessary syslog entries

</td></tr><tr><td>

Reporting

</td><td>

PRB948578

</td><td>

When using reporting, it uses GMT instead of the local time zone when accessing the 'Calendar' report functionality and viewing it in the 'Day' view

</td></tr><tr><td>

Reporting

</td><td>

PRB1745543

</td><td>

An interactive report displays extra records in the report drill-down

</td></tr><tr><td>

Reporting

</td><td>

PRB1770032

</td><td>

Clicking the **Score** of a single score report created with a parameterised script include with an encoded query breaks due to the trimming of encoded characters in the URL

</td></tr><tr><td>

Reporting

</td><td>

PRB1761750

</td><td>

When a bar report is grouped by a dot walk column, it correctly displays results, but selecting the resulting bar doesn't list any records when the language is Brazilian Portuguese

</td></tr><tr><td>

Reporting

</td><td>

PRB1782603

</td><td>

Events ending at the time 23:59:59 appear as 'All day' events in calendar reports

</td></tr><tr><td>

Reporting

</td><td>

PRB1751862

</td><td>

A PDF export of a report that is grouped by and filtered by tags is displaying all of the selected table records, which have tags

</td></tr><tr><td>

Reporting

</td><td>

PRB1732890

</td><td>

A single color definition of a UI14 green isn't green but orange

</td></tr><tr><td>

Reporting

</td><td>

PRB1769845

</td><td>

Email report generates two attachments, one attachment with the data and other with an error

</td></tr><tr><td>

Report Visualization

</td><td>

PRB1792399

</td><td>

A selected tab should be distinguishable from a non-selected tab

</td></tr><tr><td>

Report Visualization

</td><td>

PRB1795711

</td><td>

The pop-up in the 'Report' widget isn't displaying when a mouse is hovering over an item for the 'Calendar' report type in Service Portal

</td></tr><tr><td>

Report Visualization

</td><td>

PRB1790952

</td><td>

Percentages in pie charts aren't perceptible to screen reader users

</td></tr><tr><td>

Request Management

</td><td>

PRB1763436

</td><td>

Base instance notification, 'Request Item commented \(all assignees\)', has both events 'parm 1' and 'parm 2' unchecked

</td></tr><tr><td>

Request Management

</td><td>

PRB1784462

</td><td>

For a RITM record, if a workflow context is already attached, and the catalog item is updated with Flow Designer, the flow context replaces the workflow context

</td></tr><tr><td>

Request Management

</td><td>

PRB1782693

</td><td>

The 'Request Survey' notification isn't working

</td></tr><tr><td>

Request Management

</td><td>

PRB1782333

</td><td>

The transaction can time out when approving an item with many approvers

</td></tr><tr><td>

Resource Management

</td><td>

PRB1797783

</td><td>

Resource plan logs display 'Resource plan is allocated for NaN hours after confirming/allocating the hours after enabling the property 'com.snc.resource\_ management.allocate \_more\_than\_24hours \_per\_day'

</td></tr><tr><td>

Resource Management

</td><td>

PRB1778886

</td><td>

A cost plan is zeroed out when a resource plan is allocated from the Allocation Workbench

</td></tr><tr><td>

Resource Management

</td><td>

PRB1820666

</td><td>

Resource reports are broken after an Xanadu upgrade when the Glide.sys.date\_format is dd-MM-yyyy

</td></tr><tr><td>

Resource Management

</td><td>

PRB1788697

</td><td>

The 'Rate\_model' column doesn't filter records based on the reference qualifier

</td></tr><tr><td>

Resource Management

</td><td>

PRB1822356

</td><td>

A 'Resource Assignment' related list isn't visible post-migration of 'Resource Plans on Demand'

</td></tr><tr><td>

Resource Management

</td><td>

PRB1798520

</td><td>

There's inconsistent behavior on custom currencies for a certain field in 'Resource Plan \[actual\_cost\_project\_currency\]'

</td></tr><tr><td>

Resource Management

</td><td>

PRB1816860

</td><td>

Users are unable to update resource assignments created with 'Effort 0' from resource plans migration

</td></tr><tr><td>

Resource Management

</td><td>

PRB1791568

</td><td>

There's a resource aggregate monthly issue when a story is reassigned from a project to a different project

</td></tr><tr><td>

REST API Framework

</td><td>

PRB1768591

</td><td>

The 'API Monthly Requestor Stats' job doesn't aggregate all records when there's more than 100 K

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

</td><td>

PRB1751767

</td><td>

The 'Prevent invalid source &amp; target on RCA' business rule can create numerous amounts of duplicates that must be cleaned up

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

</td><td>

PRB1768689

</td><td>

RCAPs aren't invalidated after an update set is deployed with an updated source record

</td></tr><tr><td>

Roles

</td><td>

PRB1798228

</td><td>

Inconsistencies with role inheritance leads to orphaned records

</td></tr><tr><td>

Rollback Contexts

</td><td>

PRB1706257

</td><td>

A rollback with a large number of records triggers a large delete query, causing replication lag

</td></tr><tr><td>

Rollback Contexts

</td><td>

PRB1844400

</td><td>

The 'Clean Expired Rollback Contexts' job causes memory issues and node restarts

</td></tr><tr><td>

SaaS integration with Office 365 \(Glide\)

</td><td>

PRB1784710

</td><td>

Potential savings calculation at the LMR level for bulk reclamation candidates

</td></tr><tr><td>

Scaled Agile Framework \(SAFe\)

</td><td>

PRB1833357

</td><td>

Sprints aren't created via ServicenNow ADO integration

</td></tr><tr><td>

Schedule Calendar

</td><td>

PRB1794379

</td><td>

The Next UI Schedule Calendar doesn't save updates to the 'Repeat Until' date in the schedule entry

</td></tr><tr><td>

Schedule Calendar

</td><td>

PRB1802373

</td><td>

The Next UI Calendar doesn't allow for creating/editing schedule entries for custom roles

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1782901

</td><td>

A high number of values in the 'Job classification' column can prevent scheduled jobs from being processed due to a StackOverflowError in a SchedulerThread

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1771051

</td><td>

Jobs are executing twice during a rescheduler restart

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1746752

</td><td>

Removing a member from a group adds several more users

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1792821

</td><td>

Concurrent updates on sys\_trigger causes intermittent HLL spikes on instances with large node counts

</td></tr><tr><td>

Schedule Optimization

</td><td>

PRB1825269

</td><td>

The 'Optimization Solution Processor' business rule trigger is to be changed

</td></tr><tr><td>

Schedule Optimization

</td><td>

PRB1823732

</td><td>

A personal event start date is later than the end date, causing SO to fail

</td></tr><tr><td>

Schedules

</td><td>

PRB1783342

</td><td>

Schedule entries aren't functioning correctly for the 'Last Weekday of the Month' setting

</td></tr><tr><td>

Script Debugger API

</td><td>

PRB1764788

</td><td>

There's a documentation error about the 'Session Log' tab being unavailable for users with the 'script\_debugger' role

</td></tr><tr><td>

Scripted Web Services

</td><td>

PRB1749935

</td><td>

An extra response / request in Scripted Web Service results in 'Cannot map object' and potential StackOverflowError

</td></tr><tr><td>

Script Includes

</td><td>

PRB1785008

</td><td>

Many RCAS are invalidated after upgrading to Xanadu due to a fix script issue

</td></tr><tr><td>

Search Administration

</td><td>

PRB1731361

</td><td>

Global text search is broken in BuildTools1 for UI16

</td></tr><tr><td>

Search Administration

</td><td>

PRB1789281

</td><td>

There's cache issues across domains when performing a global search

</td></tr><tr><td>

Search Administration

</td><td>

PRB1776348

</td><td>

The AI Search results page doesn't display translated values

</td></tr><tr><td>

Search Suggestions

</td><td>

PRB1768021

</td><td>

Unable to relink an auto-complete suggestion type to an AI Search application

</td></tr><tr><td>

Secrets Management Core

</td><td>

PRB1793938

</td><td>

ECC Queue records aren't populated to re-encrypt the secrets

</td></tr><tr><td>

Secrets Management Core

</td><td>

PRB1756628

</td><td>

Hide the 'include all' checkbox from the UI from an Identity Group member

</td></tr><tr><td>

Seismic Framework

</td><td>

PRB1809377

</td><td>

A console error is caused by an invalid service worker registration

</td></tr><tr><td>

Seismic Framework

</td><td>

PRB1783295

</td><td>

There is an empty Service Operations Workspace incident form after upgrading from Vancouver to Washington DC

</td></tr><tr><td>

Seismic Framework

</td><td>

PRB1792811

</td><td>

Service workers don't cache non-200 Glide requests

</td></tr><tr><td>

Seismic Framework

</td><td>

PRB1807578

</td><td>

A race condition comes out of multiple single sign-ons

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1793296

</td><td>

When a script include cache is rebuilding, there's log messages: 'Error accessing descriptor for metaObject: package\_private script include function'

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1821549

</td><td>

'Undefined' isn't supported when using ScriptRuntime .evalSpecial

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1773223

</td><td>

Regex timeout doesn't work correctly

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1783318

</td><td>

The **sandbox\_callable** field doesn't work for scoped applications

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1783385

</td><td>

Add rights for java.lang.NullPointerException .getMessage

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1808973

</td><td>

Turning on ECMAScript 2021 \(ES12\) mode isn't toggled in certain scenarios

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1777353

</td><td>

There's an issue compiling a script using a map iterator in a 'for' loop

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1790567

</td><td>

Enabling ModuleSupport breaks on scopes with compiled scripts

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1818172

</td><td>

Records are unloading sys\_es\_latest\_script records even when the toggle is turned off

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1782856

</td><td>

A business rule executes in the 'module' scope

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1767574

</td><td>

Unable to use the **require** function in an ESLatest script include if invoked cross-scope from an ES5 scope

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1809275

</td><td>

An SVG-type picture doesn't appear for a catalog item on the platform

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1781043

</td><td>

The selection state of 'Submitted requests' and 'Drafts' tab items present on the 'My Requests' screen isn't announced by a screen reader

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1771270

</td><td>

Issue with a job that runs forever

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1790528

</td><td>

Images that are added to Service Catalog order guides appear stretched out in Washington DC

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1785302

</td><td>

Catalog client scripts don't work properly for Multi-Turn Catalog Ordering experience when all the records are scoped

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1769527

</td><td>

The 'Item diagnostics' job runs slow because it loads all choice options to count them

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1825185

</td><td>

The 'Taxonomy Topic' value isn't updating on the catalog item form when updating the value by using the **Edit in catalog builder** UI action on the catalog form

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1823783

</td><td>

The 'Help' icon isn't at the end of the question text when rendering a catalog item on Mobile Employee Service portal \(MESP\) or Service Portal

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1751291

</td><td>

A choice value from the 'com.Glideapp.servicecatalog .order\_guide\_sequencing' plugin isn't transformed when the French translation plugin is used

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1814987

</td><td>

Mobile Employee Service portal \(MESP\) web view issues on the Now Mobile application if there are many reference and select box variables on the form

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1793500

</td><td>

The scroll bar is moved downwards on the SWP portal in Service Operations Workspace when there are more catalog categories, making the search bar invisible

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1818368

</td><td>

The condition \(reference variable\) in different variable sets isn't evaluated without an itil role

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1814311

</td><td>

It's not possible to insert data in database views, but users are able to create a record producer for database views

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1788268

</td><td>

Dot-walking to the second level with g\_form in the Catalog Client script makes the catalog non-conversational

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1777834

</td><td>

The field message of the catalog UI policy actions aren't translated to a non-English language in Service Portal

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1815638

</td><td>

**Activate** and **Deactivate** buttons on the sc\_cat\_item table create an empty record

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1799840

</td><td>

The 'Migrate clear value actions' script action to update the UI policy actions resulted in the catalog item version being increased during the upgrade

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1811236

</td><td>

A newly created catalog item using the wizard is available to edit in existing templates without edit access defined on the catalog item creation, so making any modification to the template locks the field after publishing again

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1794884

</td><td>

The **Back** button in a category item or order guide view on platform redirects to 'Page not found'

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1779033

</td><td>

g\_form.setValue\(\) isn't working in the platform for multi-row variable sets \(MRVS\), when used in a ClientScript

</td></tr><tr><td>

Service Catalog API

</td><td>

PRB1782677

</td><td>

UI policies using the 'OR' clause don't work as expected in Now Assist in Virtual Agent

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1813682

</td><td>

The catalog item for non-English users is taking up the details from English users when publishing/submitting the item

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1793265

</td><td>

The 'catalog\_builder\_ editor\_blank\_template' role, which is used to create a catalog item directly, should be removed

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1756914

</td><td>

Modifying the catalog item task step through builder isn't working as expected

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1751174

</td><td>

Unable to remove the dynamic behavior filter condition in Catalog Builder

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1771626

</td><td>

A Catalog Builder item isn't publishing when two containers are split with the same name is added to the catalog item, with one inside the variable set and one as a normal variable

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1801524

</td><td>

The **Create a catalog item template** button in Catalog Builder is enabled even if the user doesn't have the required roles to create/edit a catalog template

</td></tr><tr><td>

Service Catalog Components

</td><td>

PRB1793214

</td><td>

After changing the instance date format, an 'Invalid date' error message displays in a multi-row variable set preview window in a Workspace

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1791330

</td><td>

ServiceNow components fail an accessibility test, selecting the 'Escape' key should allow the modal to close

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1786383

</td><td>

The 'Recent &amp; Popular Item' widget rolls over data on a quarterly basis and creates a negative user experience

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1775964

</td><td>

A variable name displays in the error message rather than the question when users select **Save as draft**

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1815205

</td><td>

In Service Operations Workspace, the 'Popular items' section in an interaction record displays 7 items instead of 6

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1747935

</td><td>

'Add to Wishlist' isn't working on Service Portal when a category is missing

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1788024

</td><td>

A catalog item outline/grid overlaps in the 'Recent &amp; popular items' widget in Employee Center

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1810653

</td><td>

There's an issue with saving drafts when the **Requested for** field is empty

</td></tr><tr><td>

Service Catalog Variables

</td><td>

PRB1814252

</td><td>

The sys\_name of the UI policy action record isn't updated when the MRVS internal name is updated, and the UI policy doesn't work as expected when it is transferred by update set

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1793364

</td><td>

Content in the 'Stage Details' section isn't marked up as a list

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1830032

</td><td>

SLA processing generates multiple warnings 'WARNING \*\*\* WARNING \*\*\* Invalid query string received:xxxx: null'

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1790083

</td><td>

Some field values are wrong when using the CheckpointWalker random access walkTo\(checkpoint\)

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1802370

</td><td>

'Start', 'Pause' and 'Stop' conditions are removed from the SLA definition when the **Repair SLA's** UI action \(related link\) is selected on the case record

</td></tr><tr><td>

Service Management Virtual Agent Topic Blocks

</td><td>

PRB1779505

</td><td>

The 'Knowledge and pinned' searcher doesn't work when used in a Workspace

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1780124

</td><td>

There's problems with tag-based Service Mapping in domain separated environments

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1824257

</td><td>

ProcessToProcess LBAFPProviderEnhanced fails with cmdb\_tcp records containing source\_process=null

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1764304

</td><td>

Clone tables and all tables with the prefix 'automation\_error', including meta-data tables, should be able to be excluded

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1746027

</td><td>

The ServiceDiscoveryProbe iterates through all the Windows CyberArk credentials, resulting in temporary system access locks

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1791752

</td><td>

Put a hard limit on properties that can be destructive

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1803746

</td><td>

The file name in the 'sm\_flapper\_exclusion' table can be truncated because the max length of the field name is 40, but the column name max length is 80

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1807935

</td><td>

The 'Service Model Auto Remediation' job isn't removing the records from a model that were removed from CMDB

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1795155

</td><td>

The replication lag protection in recomputation doesn't support standby lag

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1794723

</td><td>

'Refresh processes and connections' marks all cmdb\_running\_process as absent true

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1785551

</td><td>

In the Map UI, the action **Open in Dependency Views** should be removed from the 'CI' group

</td></tr><tr><td>

ServiceNow Security Center \(Family Release\)

</td><td>

PRB1812452

</td><td>

The due date for critical update records 'End of Support: GlideEncrypter API' and 'Enable 3DES deprecation for Password2 Fields' should be updated

</td></tr><tr><td>

Service Portal

</td><td>

PRB1837541

</td><td>

Massive logs are generated with a 'com.Glide.script. RhinoEcmaError: 'RP' isn't defined' warning

</td></tr><tr><td>

Service Portal

</td><td>

PRB1782259

</td><td>

The **Delete** button in a 'My Requests' draft item doesn't have a name

</td></tr><tr><td>

Service Portal

</td><td>

PRB1784705

</td><td>

The 'Skip to chat' link fails to land focus on the Virtual Agent chat button

</td></tr><tr><td>

Service Portal

</td><td>

PRB1834496

</td><td>

Users can't input a value into a widget

</td></tr><tr><td>

Service Portal

</td><td>

PRB1799575

</td><td>

In some cases, filter labels change to a value in Service Portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1794691

</td><td>

The 'Business Services Status' widget displays different dates for Japanese and English modes

</td></tr><tr><td>

Service Portal

</td><td>

PRB1801407

</td><td>

The 'Standard Ticket Conversations' widget creates duplicate comments when dragging and dropping an image

</td></tr><tr><td>

Service Portal

</td><td>

PRB1787466

</td><td>

Screen reader reads multi-line in the attachments modal, even though there is no multi-line input field

</td></tr><tr><td>

Service Portal

</td><td>

PRB1823261

</td><td>

JAWS fails to announce list items as links in the header navigation menus

</td></tr><tr><td>

Service Portal

</td><td>

PRB1801362

</td><td>

In the 'Ask HR' portal, the 'Choose a file' feature appears to be a link but focus doesn't move there

</td></tr><tr><td>

Service Portal

</td><td>

PRB1810935

</td><td>

The 'Remove draft item' tooltip isn't removed automatically after deleting the draft item

</td></tr><tr><td>

Service Portal

</td><td>

PRB1774213

</td><td>

The **Preview** button in the **list** field has the text 'New preview button has been generated before the current element to preview', and isn't translated properly when the language is changed to non-English

</td></tr><tr><td>

Service Portal

</td><td>

PRB1728528

</td><td>

In many locations, there is no pointer cancellation allowed for **Clear field** buttons

</td></tr><tr><td>

Service Portal

</td><td>

PRB1771140

</td><td>

Mandatory attachment isn't working as expected in Service Portal when attachments aren't saved in a draft or a wishlist

</td></tr><tr><td>

Service Portal

</td><td>

PRB1785993

</td><td>

On Service Portal in a knowledge article page, upon deletion of a comment, the black 'Delete' pop-up box remains visible until selected

</td></tr><tr><td>

Service Portal

</td><td>

PRB1768976

</td><td>

The date picker retains old values for buttons that don't trigger the update of the date/time when read by screen readers

</td></tr><tr><td>

Service Portal

</td><td>

PRB1735808

</td><td>

The 'Glyph alt text' in an announcement isn't read by JAWS and NVDA screen readers

</td></tr><tr><td>

Service Portal

</td><td>

PRB1749601

</td><td>

Elements in esc\_knowledge\_home page don't have an aria parent

</td></tr><tr><td>

Service Portal

</td><td>

PRB1789288

</td><td>

Using the date format E yyyy-MM-dd throws an error in Portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1720732

</td><td>

The **Long in &lt;identity\_provider&gt;** button on the login\_page isn't visible when the page is accessed from mobile browser

</td></tr><tr><td>

Service Portal

</td><td>

PRB1634201

</td><td>

Color alone is used to indicate the state of toggle switches, which is an accessibility issue

</td></tr><tr><td>

Service Portal

</td><td>

PRB1789181

</td><td>

Past the second row of nested rows aren't cloned when selecting the 'Clone' page

</td></tr><tr><td>

Service Portal

</td><td>

PRB1828005

</td><td>

The 'Simple List' widget's footer breaks when using a non-English translation

</td></tr><tr><td>

Service Portal

</td><td>

PRB1813731

</td><td>

When an onChange client script modifies a value and copies it to an integer field, the value doesn't isn't saved when saving from a portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1376471

</td><td>

sp-editable-field directive doesn't support HTML field types

</td></tr><tr><td>

Service Portal

</td><td>

PRB1800664

</td><td>

Extra character in Service Portal widget HTML causes blank Automated Test Framework \(ATF\) screenshots

</td></tr><tr><td>

Service Portal

</td><td>

PRB1778588

</td><td>

Attachments can't be downloaded when accessed from the 'lf' page in a portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1799699

</td><td>

The selected options for 'select box type' variables are reset in the portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1756221

</td><td>

The new portal and theme aren't honored by the widget CSS dependency

</td></tr><tr><td>

Service Portal

</td><td>

PRB1770309

</td><td>

A screen reader reads incorrect variable names for the date-picker variable

</td></tr><tr><td>

Service Portal

</td><td>

PRB1791816

</td><td>

A pop-up message is concatenated, causing readability issues in languages such as Japanese

</td></tr><tr><td>

Service Portal

</td><td>

PRB1817086

</td><td>

Required information field pop-ups aren't WCAG 2.2 complaint under section 1.4.13

</td></tr><tr><td>

Service Portal

</td><td>

PRB1716137

</td><td>

When the name of a user has a comma, Survey Designer doesn't display the name of the user correctly

</td></tr><tr><td>

Service Portal Announcements

</td><td>

PRB1808665

</td><td>

Keyboard focus lands on the static text of the announcements banner

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1807235

</td><td>

There's accessibility issues for the keyboard and voice over in the 'Hiring' tab

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1822245

</td><td>

If an outage doesn't have end date, it isn't displayed on the Service Status widget

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1798111

</td><td>

Users are unable to copy and paste text and images from an external source in Service Portal - Standard Ticket

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1808916

</td><td>

The checkbox variable in a catalog item can't print correctly

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1802357

</td><td>

The 'Preview' form announces the button word twice

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1788988

</td><td>

Support user\_id parameter in checkAllowedExplicit\(\) and checkDeniedExplicit\(\) of ICatalogSecurityMask

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1807004

</td><td>

Unrelated improvement initiatives associated with application services

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1791670

</td><td>

The 'Edit Weights' related link isn't working in a 'Service' form

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1823722

</td><td>

Users that are subscribers to an offering are returned in a query when they are active = false

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1797800

</td><td>

Existing services won't publish when both service and offering\(s\) change to the status 'Operational'

</td></tr><tr><td>

Session Management

</td><td>

PRB1774686

</td><td>

Potential uncaught exception when the session is invalidated and getAttributes is accessed

</td></tr><tr><td>

Session Management

</td><td>

PRB1817651

</td><td>

User.getUser causes deadlock while the session lock is taken out

</td></tr><tr><td>

Session Window Timeout

</td><td>

PRB1778553

</td><td>

Selecting the cross icon in the 'Session expired' pop-up doesn't log out the user and remains on the same page, and the 'invalidated' column in sys\_user\_session isn't updated instantly

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1821306

</td><td>

The **Discuss** button is missing on a domain-separated instance

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1799644

</td><td>

Subject data populates slowly for an incident after launching the start side bar chat modal in Service Operations Workspace

</td></tr><tr><td>

Sign Your Own Certificate \(SYOC\)

</td><td>

PRB1747791

</td><td>

Platform resolution ambiguity in namespace and scope

</td></tr><tr><td>

Software Asset Core Company

</td><td>

PRB1689224

</td><td>

Evaluate the unique index on the core company

</td></tr><tr><td>

Software Asset Data Import

</td><td>

PRB1725404

</td><td>

'SAMPremiumUtils.getInstalledOnRelationship' is called out of scope

</td></tr><tr><td>

Software Asset Data Import

</td><td>

PRB1578765

</td><td>

Additional warning and error messages in the system log while the entitlements import is stuck in the 'Processing' state

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1628611

</td><td>

The samp\_entitlement\_import table doesn't have 'audit = true' out of the box, so it is unable to track worknote updates

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1802887

</td><td>

The 'Software product lifecycles for all versions' link doesn't work as expected on the software model table

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1819212

</td><td>

There's a localization issue in 'Potential savings' on single currency instances

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1627323

</td><td>

The 'Entitlements' related list isn't filtering by group, subgroup, or 'in use' entitlements

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1823587

</td><td>

Optimization doesn't work as expected when the named user type is empty

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1818910

</td><td>

Software Asset Management job scripts populate a status value that doesn't match with the definition on the sys\_choice table

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1773201

</td><td>

Subscription inference should only infer direct components of Office 365 to Microsoft 365

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1779646

</td><td>

Subscription installs have preference rank of 999 and cause performance issues

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1728221

</td><td>

Selecting 'Number of reclamations' doesn't open the correct drill down

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1822003

</td><td>

The 'Bookkeeping for dedup on delete' business rule doesn't handle installs with different versions or editions

</td></tr><tr><td>

Software Asset Management Licensing and Compliance

</td><td>

PRB1807335

</td><td>

Daily subscription counts intermittently get zero counts

</td></tr><tr><td>

Software Asset Management Plugin Framework

</td><td>

PRB1785996

</td><td>

Custom product references aren't cleaned when a product is deleted

</td></tr><tr><td>

Software Asset Management Publisher Pack for SAP

</td><td>

PRB1788912

</td><td>

A Software Asset Management SAP import job fails due to a 'NULL' character

</td></tr><tr><td>

Software Asset Management Workspace

</td><td>

PRB1774425

</td><td>

There's issues with currency conversion in Platform Analytics and the Publisher 'Results' page

</td></tr><tr><td>

Software Asset Management Workspace

</td><td>

PRB1781351

</td><td>

The 'End of life products' widget on the SAM landing page isn't working

</td></tr><tr><td>

Software Asset Management Workspace

</td><td>

PRB1679155

</td><td>

Software Asset Management \(SAM\) Health check widgets and drill downs display duplicate records if a check failed in a previous scan

</td></tr><tr><td>

Software Asset Normalization

</td><td>

PRB1728928

</td><td>

Users aren't informed of scenarios when suggested normalized values are the same as normalized values

</td></tr><tr><td>

Software Asset Normalization

</td><td>

PRB1808233

</td><td>

The 'SAM - Normalize Discovery models using content library rules' scheduled job isn't robust because a single corrupted samp\_package\_map record can make the job fail

</td></tr><tr><td>

Software Asset Reclamation

</td><td>

PRB1815883

</td><td>

Localization issue in potential savings, true-up cost, over-licensed amount, and total spend calculation

</td></tr><tr><td>

Software Asset Reclamation

</td><td>

PRB1778060

</td><td>

SAMPReclamationUtil code change from Vancouver misses out corner cases and causes a job to fail

</td></tr><tr><td>

Software Asset Reclamation

</td><td>

PRB1786501

</td><td>

Blacklisted reclamation candidates are created and closed without reclaiming install

</td></tr><tr><td>

Software Asset Reclamation

</td><td>

PRB1814389

</td><td>

Scheduled imports and data sources for 'SG-SCCM Software Last Used' and 'SG-SCCM SAMP Usage' aren't deleting old records in the table samp\_sw\_usage

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1780888

</td><td>

Potential savings don't appear in LWB for hybrid software

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1794331

</td><td>

Performance issue in clearing LMRs for entitlements

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1779794

</td><td>

License pools consumption breakdown is incorrect for Per User and Per Device metrics

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1792145

</td><td>

The 'reset dedupe' business rule on the DM table should only trigger if the norm field changes

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1808379

</td><td>

Downstream tables aren't updated if exception rules are marked as inactive by content

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1791385

</td><td>

ignoreNonBYOLInstalls should not insert a reason for 'Missing Cloud License Type'

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1775411

</td><td>

SA entitlements should not be considered as suite candidates

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1776017

</td><td>

The same installs are listed under 'unlicensed installs' and 'installs requiring action'

</td></tr><tr><td>

Software Lifecycles

</td><td>

PRB1756991

</td><td>

A lifecycle report should be able to handle empty lifecycle dates

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1790669

</td><td>

Continuous Integration and Continuous Delivery \(CICD\) app customization doesn't fail for apps linked to source control and erroneously reports success

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1774720

</td><td>

An absent bootstrap XML in the source control diff should not drop the column when the bootstrap XML exists in the base application

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1829444

</td><td>

sys\_ui\_message additional coalesce value can break an app customization install

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1771610

</td><td>

sys\_claim list breaks due to an invalid entry in the **time claimed\(claim\_timestamp\)** field

</td></tr><tr><td>

Survey Management

</td><td>

PRB1797560

</td><td>

An error message appears when the date type field isn't updated when retaking a survey

</td></tr><tr><td>

Survey Management

</td><td>

PRB1788346

</td><td>

The **View user's response** UI action doesn't show all dependent responses

</td></tr><tr><td>

Survey Management

</td><td>

PRB1779860

</td><td>

When trying to access the 'Getting Started' module for a survey from the instance, users are redirected to the documentation site but a 'Not found' message is shown

</td></tr><tr><td>

Survey Management

</td><td>

PRB1782966

</td><td>

Text mentioned in the **Description** field doesn't appear while hovering over the field in Assessment Metric

</td></tr><tr><td>

Survey Management

</td><td>

PRB1781447

</td><td>

Survey questions using the out-of-box NPS template splits the label incorrectly

</td></tr><tr><td>

Syntax Editor

</td><td>

PRB1790034

</td><td>

Syntax editor macros don't work reliably

</td></tr><tr><td>

Syntax Editor API

</td><td>

PRB1792891

</td><td>

The Completion API has a longer response time due to the inclusion of shadow tables

</td></tr><tr><td>

Syntax Editor API

</td><td>

PRB1789193

</td><td>

Missing type definition for the GlideSysAttachment class

</td></tr><tr><td>

System Archiving

</td><td>

PRB1742225

</td><td>

The archiver is archiving fewer records per archive run if the restored records are equal to or greater than 'Glide.db.archive .max.rule.records'

</td></tr><tr><td>

System Archiving

</td><td>

PRB1789660

</td><td>

Restoring records with multiple related rules for the same table throws a NullPointerException if at least one rule points to an empty field

</td></tr><tr><td>

System Events

</td><td>

PRB1818627

</td><td>

The 'Slow Delete DML's from text index events process' job is contributing towards a replication lag on the standby db

</td></tr><tr><td>

System Events

</td><td>

PRB1762956

</td><td>

The name for the 'Processed' column in the event log table documentation is misleading

</td></tr><tr><td>

System Events

</td><td>

PRB1792583

</td><td>

Flow Engine is unable to move a sysevent in the ready.node state back to ready when the sysevent table rotation record is deleted

</td></tr><tr><td>

System Events

</td><td>

PRB1725049

</td><td>

NowMQ v1 size estimator improvements

</td></tr><tr><td>

System Export Sets

</td><td>

PRB1623235

</td><td>

Messaging on the PDF export screen to reflect what is shown on the list view of the widget instance

</td></tr><tr><td>

System Export Sets

</td><td>

PRB1792544

</td><td>

If Log Export Service \(LES\) is enabled and the LES source is configured with syslog in a global scope filter, there's a null pointer exception when using gs.log after a Washington DC upgrade

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1639586

</td><td>

All import sets are deleted when concurrent data source calls are executed

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1808239

</td><td>

JDBC connection for authentication= ActiveDirectoryPassword isn't working properly

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1736448

</td><td>

The following error is logged even though the import set is processed and the record is inserted successfully: 'Unable to format undefined using format string yyyy-MM-dd for field **&lt;column\_name&gt;**'

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1792166

</td><td>

Xlsx files with a namespace prefix don't load

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1757948

</td><td>

Transform mapping can't target reference fields with translated values, and only works in English

</td></tr><tr><td>

System Scheduler

</td><td>

PRB1788785

</td><td>

Instruments in AssignerOTelObserver constructor are re-registered when SchedulerThread restarts

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1808271

</td><td>

When an update set that deletes an extended child table is retrieved, it is rewritten to delete the related list of the extended parent table

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1794841

</td><td>

Sys\_update\_set\_log doesn't reflect errors found while committing an update set

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1809728

</td><td>

Deleting a user preference record for a system-wide value isn't stored in an update set

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1769433

</td><td>

A reference field in a 'Database' view isn't a selectable link

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1735482

</td><td>

Packages.com.glide .db.ddl.Table Hybridizer.hybridize aborts on false-positive checks for fields already glommed to **mediumtext** fields where the max\_length will not reflect the true max length of a **mediumtext** field

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1828517

</td><td>

There's an SQL error when inserting invalid or var\_\_ tables as a dependent field for document it

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1769979

</td><td>

Database view doesn't display the **list** field type choices correctly

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1800174

</td><td>

Missing collection record in sys\_dictionary for the open\_nlu\_predict\_intent\_feedback table

</td></tr><tr><td>

Table API

</td><td>

PRB1727095

</td><td>

GlideElementResolver sets invalid record values for non-existent references and choices

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB1783267

</td><td>

There's uncontrolled growth of table sys\_cluster\_message

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB1792483

</td><td>

Non-nibble table cleaners are cleaning data even when the **child match** field passes

</td></tr><tr><td>

Tables and Columns Data Dictionary

</td><td>

PRB1754043

</td><td>

sys\_update\_name is null for a label with sys\_\* column

</td></tr><tr><td>

Template Management for Field Service

</td><td>

PRB1802776

</td><td>

The 'Copy Work Order' task template doesn't work in the work order task template jelly page

</td></tr><tr><td>

Territory Planning

</td><td>

PRB1777951

</td><td>

Unassigning a task on Dispatcher Workspace sets the assigned group to an empty string literal

</td></tr><tr><td>

Territory Planning

</td><td>

PRB1793222

</td><td>

The agent or group doesn't satisfy the task qualification criteria

</td></tr><tr><td>

Test Management 2.0

</td><td>

PRB1831655

</td><td>

The 'Pass' checkmark \(green\) fails the minimum contrast ratio requirements

</td></tr><tr><td>

Test Management 2.0

</td><td>

PRB1800579

</td><td>

Test execution suites don't appear in test phases in projects

</td></tr><tr><td>

Test Management 2.0

</td><td>

PRB1806757

</td><td>

The 'Block' icon blinks when hovered over on a test execution in Test Management 2.0

</td></tr><tr><td>

Test Management 2.0

</td><td>

PRB1794880

</td><td>

Deleting a record from sn\_test\_management \_test\_plan \(installed with Test Management 2.0\) creates two sys\_audit\_delete records

</td></tr><tr><td>

Test Management 2.0

</td><td>

PRB1798817

</td><td>

Line-breaks \(paragraph / carriage returns\) in steps aren't honored

</td></tr><tr><td>

Third-party Software

</td><td>

PRB1792933

</td><td>

Washington DC column tags have bullet points, whereas Vancouver column tags don't

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1823458

</td><td>

A 'Your time Card has been modified with your time worked' message displays despite there not being an update in the respective time card

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1809013

</td><td>

The widget 'timesheet-week-breakdown' doesn't display hours on the Time Sheet portal

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1817054

</td><td>

Users can't recall time card/sheet when only Time Card Management is installed

</td></tr><tr><td>

Transaction Logs

</td><td>

PRB1738233

</td><td>

In a localhost log, transaction timing appears incorrectly

</td></tr><tr><td>

Transaction Management

</td><td>

PRB1780795

</td><td>

Null pointer exception when attempting to retrieve and use a GlideSession object in TransactionVTable.getSessionUser

</td></tr><tr><td>

UI Actions

</td><td>

PRB1816586

</td><td>

The **Show dictionary record** UI action no longer opens a collection record

</td></tr><tr><td>

UI Actions

</td><td>

PRB1826799

</td><td>

setRedirectURL\(\) doesn't work in Xanadu

</td></tr><tr><td>

UI Actions

</td><td>

PRB1787504

</td><td>

The **Submit/Save** button takes two clicks to create the record on the Document References \[ds\_document\_references\] table

</td></tr><tr><td>

UI Actions

</td><td>

PRB1821330

</td><td>

In the Knowledge V3 kb\_view, the **Was it helpful =&gt; yes** button has no border in Washington and Xanadu

</td></tr><tr><td>

UI Actions

</td><td>

PRB1828008

</td><td>

MFA-configured with single sign-on \(SSO\) users are incorrectly redirected to a page that can't be found

</td></tr><tr><td>

UI Builder \(Family Channel\)

</td><td>

PRB1791858

</td><td>

An alert error isn't translating to German

</td></tr><tr><td>

UI Builder \(Family Channel\)

</td><td>

PRB1797756

</td><td>

The **Save and Close** UI action switches tabs instead of closing them

</td></tr><tr><td>

UI Builder \(Family Channel\)

</td><td>

PRB1828407

</td><td>

Users are unable to add new data visualizations and set the data sources in Agent Workspace when opened in UI Builder

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1809507

</td><td>

The sys\_user table on classic view \(UI16\) doesn't retain the phone number format when it is updated from the Workspace like Service Operations Workspace \(SOW\)

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1799389

</td><td>

Display issue for a **File Attachment** type field in forms

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1795149

</td><td>

Filtering on a dot-walked field incorrectly queries and results in no records being fetched

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1802778

</td><td>

When a dot-walked field that depends on another dot-walked field is updated, the dependent field might temporarily display as 'None' in the Workspace UI

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1799414

</td><td>

The **decimal** field doesn't register the user's country code and system language, and uses a period instead of a comma as a decimal separator in the legacy Workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1793631

</td><td>

Automatic completion of the fields by the browser

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1747824

</td><td>

In the Workspace, the **Glide List** field type isn't honoring the ref\_ac\_order\_by dictionary attribute

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1753031

</td><td>

The user observes an error when accessing the 'Manage Human Resource Catalog' page

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1810329

</td><td>

Issue with translation when kb\_category is changed, even after adding the translation on the sys\_translated table

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1763183

</td><td>

In Configurable Workspace, the advanced filter condition 'is one of' doesn't always populate choices correctly

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1759424

</td><td>

Field decorators aren't displaying for some fields in a Workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1578048

</td><td>

The **FX Currency** field unexpectedly clears when quickly saving a form

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1804238

</td><td>

The Service Operations Workspace **Phone** field doesn't call the selected number

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1789011

</td><td>

Character limit \(maxlength\) isn't implemented in the **UTC Time** field in a Workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1801223

</td><td>

A GraphQL API -GlideGraphQL error when using the **Compose Email** button in Configurable Workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1799424

</td><td>

There's a 'Recent selections' sorting issue on Workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1772813

</td><td>

Entering a negative value in the **decimal** field shows a 'Couldn't parse the value' error

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1696422

</td><td>

The **Toggle Domain Scope** UI action doesn't work in a Workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1782462

</td><td>

Policy and Compliance Management grid display issues

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1752782

</td><td>

When using showFieldMsg on a form, the text doesn't wrap within the box and comes outside the box

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1740015

</td><td>

A section breaks when the HTML field contains a form tag

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1823455

</td><td>

The 'Personalize form' feature for a record on workspaces has inconsistencies

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1790795

</td><td>

The modal box **Close** button can't be hidden

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1784568

</td><td>

The business rule of setAbortAction sys\_attachment doesn't show the message

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1787509

</td><td>

The attaching encryption option isn't visible in the HR Agent Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1770695

</td><td>

g\_form.setSectionDisplay isn't working as expected on the Workspace, and displays any mandatory fields on the section

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1768345

</td><td>

A null condition in a UI policy prevents Service Operations Workspace from loading the UI policy list

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1821039

</td><td>

Discrepancy in behavior of related lists between the native UI and Workspaces when the 'ignore\_filter\_on \_new=true' attribute is present on a field

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1784386

</td><td>

A subject person with an empty first and last name in their sys\_user table record isn't saving in Service Operations Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1771929

</td><td>

VTB cards \(pop-up/modal\) unexpectedly close when trying to select text when the cursor is outside the card

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1801483

</td><td>

Issues with the behavior of Glide.ui.scroll\_ to\_message\_field \(scroll the form down to field error or info messages\)

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1764123

</td><td>

Images attached in the HTML type field aren't visible in the activity formatter in a Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1737490

</td><td>

Global ACLs stop processing after a role check in Vancouver

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1769932

</td><td>

Multi-line read-only variables can't be expanded in a Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1787600

</td><td>

Manually added questions to the record variable break the form in the Workspace, and the record never fully loads

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1791019

</td><td>

A help tip shows 'Mandatory' twice for glide\_list fields

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1766041

</td><td>

The resolution form section on incident forms isn't visible as mandatory in Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1798001

</td><td>

The 'Leave Page' modal displays an unexpected message

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1781725

</td><td>

**Move Attachments** isn't working when a special handling pop-up is displayed

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1726723

</td><td>

On a field normalization rule form, the 'Rule' conditions on extended tables don't display the complete condition

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1767131

</td><td>

OnChange client scripts don't trigger when the tab key is used quickly in Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1797566

</td><td>

There is an empty payload in some events emitted by the Attachment UI Builder component

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1799395

</td><td>

Fields overlap annotation on the form in Service Operations Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1822779

</td><td>

When a user tries to fill in the affected **The Location** field on a change request and Edge's auto-fill suggests the browser's saved address location, it opens and is stuck in a loop trying to fill all reference fields on the screen

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1810910

</td><td>

In Xanadu, the onChange client script executes twice on the 'Record Default' UX screen of Customer Service Management \(CSM\) Configurable Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1802708

</td><td>

After configuring reference qualifier conditions in an M2M table, all active records are shown instead of filtering correctly

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1815936

</td><td>

Workspace UI policies using an 'Ends with' condition incorrectly evaluate to true if the condition value is greater than the field value

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1765759

</td><td>

Record pages in UI Builder don't honor the 'no labels' = true attribute to prevent the rendering of the tags icon

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1794562

</td><td>

Opening the incident description via VTB causes a field update and white space removal

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1808174

</td><td>

Interactions and incident forms don't load properly

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1754094

</td><td>

The **menu** button is incorrectly labeled, which leads to confusion

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1738430

</td><td>

When Workspace tabs lose connection, they don't receive updates or sync

</td></tr><tr><td>

Universal Request

</td><td>

PRB1823185

</td><td>

UR state mapping fails

</td></tr><tr><td>

Universal Request

</td><td>

PRB1798522

</td><td>

It isn't possible to 'accept resolution' or 'not accept resolution' on the Service Portal from an iPhone on Safari, Edge and Chrome browsers

</td></tr><tr><td>

Universal Request

</td><td>

PRB1789807

</td><td>

Universal request state mapping doesn't update additional comments or work notes

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1776398

</td><td>

After a family upgrade and activating the Store app, conditional content isn't being installed

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1734661

</td><td>

Some records are reporting as skipped in a builder instance, but have no sys\_update\_xml, and those records show as inserted in the upgrade preview

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1804085

</td><td>

MetadataCustomization Population job creates a high volume of \*package\_inventory.csv files and occupies terabytes of app server disk space

</td></tr><tr><td>

Upgrade Monitor

</td><td>

PRB1784452

</td><td>

Slow queries observed for Upgrade Monitor that aren't using any index

</td></tr><tr><td>

Upgrade Plans

</td><td>

PRB1765329

</td><td>

'Auto Resolved by Upgrade plan' comments are seen in 'Skipped changes'

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1807002

</td><td>

Errors while processing certain definition IDs in Xanadu

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1806983

</td><td>

Errors while processing certain definition IDs in Xanadu

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1764330

</td><td>

An 'Abrupt verify' error while checking for entitlements during initializing of Appsee UX Metrics Configuration

</td></tr><tr><td>

UXF Components

</td><td>

PRB1790783

</td><td>

Filtering on the 'Plans' tab in the 'Crisis Event' page and adding the selected list of items adds the entire BCP plan table record to the event in BCM Workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1792196

</td><td>

The 'Extend your session' option isn't occurring for single sign-on \(SSO\) users

</td></tr><tr><td>

UX Framework

</td><td>

PRB1764138

</td><td>

Landmark focus \(Back\), a new feature of 'keyboard shortcuts', isn't working

</td></tr><tr><td>

UX Framework

</td><td>

PRB1798658

</td><td>

The **To** recipient field isn't displayed because of the email header in Customer Service Management \(CSM\) Configurable Workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1688293

</td><td>

On the Customer Service Management \(CSM\) Workspace 'Interaction' page, there's a mismatch between the selected tab and the tab content that's displayed

</td></tr><tr><td>

UX Framework

</td><td>

PRB1745759

</td><td>

Tooltips on the timeline component don't load translations

</td></tr><tr><td>

UX Framework

</td><td>

PRB1819244

</td><td>

Duplicate properties in sys\_ux\_data\_broker table records cause a white screen on page load for Next Experience pages and Workspaces

</td></tr><tr><td>

UX Framework

</td><td>

PRB1792042

</td><td>

The REST API errors with an obtrusive 503 error modal pop-up on a Workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1788948

</td><td>

Upon reload, dependent macroponents of a subpage aren't rendering

</td></tr><tr><td>

UX Framework

</td><td>

PRB1818682

</td><td>

UI Builder data broker sends empty context props as 'null' \[type string\] instead of null \[type object\].

</td></tr><tr><td>

UX Framework

</td><td>

PRB1762374

</td><td>

Viewport modal content overflows outside of the modal and the resize icon doesn't align with the border when 'Resize Enabled' and 'Bare' are true

</td></tr><tr><td>

UX Framework

</td><td>

PRB1804008

</td><td>

'Create New Case' and the 'Loading' tab appears after the browser or session is closed

</td></tr><tr><td>

UX Framework

</td><td>

PRB1768742

</td><td>

When the user opens attachments on the Strategic Planning Workspace they have no way of navigating back to the Workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1784434

</td><td>

Databroker 'Fetch EVAM Data' executes a query twice when it is used on millions of data

</td></tr><tr><td>

UX Framework

</td><td>

PRB1729754

</td><td>

A duplicate of a browser tab in Configurable Workspace isn't giving consistent results

</td></tr><tr><td>

UX Framework

</td><td>

PRB1807412

</td><td>

A Chrome page title isn't reflecting properly

</td></tr><tr><td>

UX Framework

</td><td>

PRB1818604

</td><td>

Inconsistent behavior in views displayed when navigating between interaction records in Customer Service Management \(CSM\) Workspace and the browser

</td></tr><tr><td>

UX Framework

</td><td>

PRB1795533

</td><td>

Hover pop-ups on the calendar don't disappear after upgrading to Washington DC

</td></tr><tr><td>

UX Framework

</td><td>

PRB1786454

</td><td>

For keyboard shortcuts, landmark focus \(backward and forward\) and **Open user menu** isn't working as expected

</td></tr><tr><td>

UX Framework

</td><td>

PRB1778611

</td><td>

In the 'Customer Success' Workspace, adding a comment or a work note to a case causes a hidden contextual side panel to unhide itself

</td></tr><tr><td>

UX Framework

</td><td>

PRB1720237

</td><td>

A case tab preview doesn't work for some case tabs

</td></tr><tr><td>

UX Framework

</td><td>

PRB1814114

</td><td>

An instance is significantly slower when zoomed in to 400% at a lower resolution

</td></tr><tr><td>

UX Framework

</td><td>

PRB1822144

</td><td>

After upgrading to Xanadu, Workspace date fields display an inaccurate date format error

</td></tr><tr><td>

UX Framework

</td><td>

PRB1804605

</td><td>

Service Operations Workspace has a 'Record Not Found' error message

</td></tr><tr><td>

UX Framework

</td><td>

PRB1762431

</td><td>

In Workspace when the tabs component position is changed from 'Top' to 'Start', and tabs are trimmed if there are multi-line text fields with long descriptions

</td></tr><tr><td>

UX Framework

</td><td>

PRB1824580

</td><td>

Optimize V1 SRC conditions to filter out macroponent properties \(input properties\) based on the **parameter mapping** field

</td></tr><tr><td>

UX Framework

</td><td>

PRB1832759

</td><td>

Enabling the resize configuration for modals isn't working on a Standard Record Page \(SRP\)

</td></tr><tr><td>

UX-Metrics

</td><td>

PRB1781625

</td><td>

Users observe an error in ClientInteractionRepository when running an Automated Test Framework \(ATF\) test for HR Agent Workspace

</td></tr><tr><td>

Versatile Node and Cluster Configuration

</td><td>

PRB1804671

</td><td>

SystemI\_d and Node\_Id are interchanged in sys\_cluster\_state when VNCC is off

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1792782

</td><td>

When generating an HTML OutputCard an extra conversation task is unnecessarily loaded

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1795927

</td><td>

Flow error with the 'OneExtend Profanity Filter' subflow

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1818121

</td><td>

The state of the Virtual Agent chat window isn't announced to screen reader users

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1767515

</td><td>

Trailing spaces in Virtual Agent feedback survey metrics definitions are causing issues in the CI Analytics Dashboard

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1775276

</td><td>

There is a Virtual Agent custom text input validation error when the user inputs text with a double quote that fails validation

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1733386

</td><td>

The business rule, 'update predict outcome for conversation' is triggered even after a conversation has been completed and closed

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1799405

</td><td>

The custom bot profile of the Virtual Agent chat changes when a topic is created using the 'Grouped choice' user input component

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1783451

</td><td>

An API replaces each Japanese character with '?' in the Content-Disposition response header

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1784935

</td><td>

OIDC token verification failure as JTI is enabled by default

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1783965

</td><td>

The Virtual Agent conversation isn't ended immediately when Dynamic Translation for Virtual Agent is enabled

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1819627

</td><td>

Glide.cs.disable. show\_me\_everything doesn't work as expected when the topic picker is empty

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1765722

</td><td>

The Virtual Agent table bot response card doesn't display all data properly after upgrading to Washington DC or Vancouver

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1819265

</td><td>

Follow-up queries that aren't in English intermittently hang

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1776622

</td><td>

The post-chat survey displays in the agent's language rather than the requester's language

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1766344

</td><td>

The 'Interaction State' reason is improperly set after a post-chat survey

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1793069

</td><td>

Some dependencies are missed during installation of the Now Assist for Creator \(NAFC\) 26.1.1 bundle

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1791956

</td><td>

Multiple entities for slot filling cause a conversation to crash

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1812011

</td><td>

Domain-specific users don't see topics from their domain

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1787170

</td><td>

The Virtual Agent in Now Assist is unresponsive when reaching the variable maximum in client scripts

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1783612

</td><td>

An error occurs while transcribing the message for the 'Record Card' adapter card

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1776548

</td><td>

Deleting a sys\_user and adding them back with the same user\_id can cause Virtual Agent AMB authorization issues

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1790051

</td><td>

Virtual Agent error in Microsoft Teams

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1781543

</td><td>

A survey returns an incorrect value in Virtual Agent

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1823688

</td><td>

ACL prevents read access on the field level, despite a non-matching record condition

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1820780

</td><td>

The Voice Interaction Resource API fails to look up the user by user ID unless it's the same as the user email

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1806955

</td><td>

Sanitized text should not be accepted during a live agent chat

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1718858

</td><td>

'Internal Server Error - 500' when attempting to save a Virtual Agent test case

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1781835

</td><td>

Unable to create a new Now Assist deployment channel record for the provider channel 'Identity'

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1771872

</td><td>

Outdated URL when accessing the content item 'Implement advanced analytics with Performance Analytics from Virtual Agent'

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1821162

</td><td>

Voice transcript API reopens a closed conversation when calling a save voice transcript API

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1777529

</td><td>

Selecting **Continue this topic** doesn't resume the topic but closes the conversation

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1781037

</td><td>

The chatbot in Virtual Agent can't be closed without using a mouse

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1800743

</td><td>

SensitiveDataHandling unmasking won't work if the value contains a '$' character

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1803180

</td><td>

NowLLM connection alias should not be set in the capability definition for other providers

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1822221

</td><td>

A return after topic selection isn't a linguistic sentence

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1782232

</td><td>

Utterance length isn't checked at topic Discovery, which allows large utterances that cause a slow down

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1795646

</td><td>

Changing the chat body text font isn't applied for the card rendered in the Virtual Agent header

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1788742

</td><td>

The Talent Development helper topic isn't discovered

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1800264

</td><td>

Virtual Agent Designer crashes when removing a field from Record Action Utility

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1793793

</td><td>

NAVA topic execution doesn't populate the 'API' column in a sys\_cs\_fdih\_invocation table, causing ETL job failure

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1793134

</td><td>

A user without elevated privileges can't create a large language model \(LLM\) sys\_cs\_context\_profile

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1799111

</td><td>

A conversation errors out when slot-filling returns slots that don't have matching field definitions

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1816687

</td><td>

The base instance 'Record action utility' in Virtual Agent Designer is unsafe to use if updating the user

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1799095

</td><td>

Unable to see the test results for the 'walk-up check-in' topic

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1807451

</td><td>

Disabling 'new message below/above' doesn't work as expected

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1813366

</td><td>

NAVA loading state text and avatar is missing

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1811601

</td><td>

There's multiple UI issues in NAVA

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1765103

</td><td>

The **X** button on the 'Response' tab overlaps with the **X** button on card on the Virtual Task Board

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1772001

</td><td>

Visual Task Board swimlane reorder doesn't work when non-consecutive lanes are selected under lane configuration

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1822106

</td><td>

When using the **Move** button to move a card between existing Visual Task Boards, the performance of the pop-up gradually decreases as more boards are added and as more cards are added to the boards

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1633785

</td><td>

Fields configured for Visual Task Board \(VTB\) view doesn't display all the time if 'Show Card Info' is enabled or disabled multiple times

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1658015

</td><td>

Report view field ACL error when accessing a report while only 'group by' conditions are applied for the vtb\_card\* table

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1827999

</td><td>

Implement an advanced activity configuration script so walk-up visit counts are visible again

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1801862

</td><td>

The Badge Reader API throws the error message: 'Could not find location queue associated with badge reader'

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1791373

</td><td>

When a user schedules appointment and it fails, the system still creates the interaction against the user appointment request

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1805976

</td><td>

An 'Error while fetching List View' error is visible in the 'My Items' widget when users make walk-up visits as primary in the activity configuration

</td></tr><tr><td>

Walk-up Experience Portal

</td><td>

PRB1781252

</td><td>

Inconsistency with the walk-up date translation

</td></tr><tr><td>

Walk-up Experience Surveys

</td><td>

PRB1809389

</td><td>

Walk-up survey options aren't fully displayed for tablet devices

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1799156

</td><td>

Accessibility issues on a 'Reservation' form \(Book a desk\)

</td></tr><tr><td>

Word Document APIs

</td><td>

PRB1789946

</td><td>

A corrupted Word document generates from the WordDocumentAPIs after a recent update in Microsoft Office Word

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1820564

</td><td>

The 'Populate Group - Dispatch/Work' business rule triggers an update on the finance task record from unregistered external users

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1784924

</td><td>

Updates made to the wm\_task.state label in the platform aren't reflected in 'My Map'

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1835428

</td><td>

The preferred date and time format isn't honored in the dispatcher Workspace task panel

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1786639

</td><td>

customerservice\_agent can view all records in a time worked table

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1798406

</td><td>

Updating 'Assigned to \(Assign Group change\)' assigns the 'Assigned to', even though the g\_scratchpad.v endor\_group\_type is null or undefined

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1816836

</td><td>

The workforce module in the Customer Service Management \(CSM\) and Field Service Management \(FSM\) Configurable Dispatcher Workspaces takes a long time to display data

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1782808

</td><td>

A manual update doesn't update the travel time

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1781421

</td><td>

The **Request more information** button on the work order task table doesn't work in Workspace

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1797615

</td><td>

The estimated end isn't calculated when 'Assign across the schedule entries' is true and the scheduled start date is edited manually and saved

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1768649

</td><td>

Exact match search result is showing a column value as 'None'

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1655206

</td><td>

After selecting 'View all knowledge matches' from the global search results, the search group conditions aren't honored in the knowledge.do results

</td></tr></tbody>
</table>**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


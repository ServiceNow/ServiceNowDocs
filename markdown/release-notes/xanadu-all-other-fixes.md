---
title: All other Xanadu fixes
description: The Xanadu release contains important problem fixes.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 133
breadcrumb: [Available patches and hotfixes, Learn about the Xanadu release, Xanadu release notes]
---

# All other Xanadu fixes

The Xanadu release contains important problem fixes.

-   **Xanadu was released on August 01, 2024.**
    -   Build date: 07-27-2024\_1019
    -   Build tag: glide-xanadu-07-02-2024\_\_patch0-07-16-2024

**Important:** For more information about how to upgrade an instance, see [ServiceNow Upgrades](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0547244).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This ServiceNow AI Platform major family release is now available in ServiceNow's Regulated Market environments. For more information about services available in isolated environments, see [KB0743854](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0743854&_ga=2.238511747.200430442.1684856845-2052949275.1611611591).

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/xanadu/rn/patches/PRBs-X00.00.xlsx)

## All other fixes

<table id="all-other-fixes" class="custom-rows"><thead><tr><th class="filter">

Problem category

</th><th>

Problem

</th><th>

Short description

</th></tr></thead><tbody><tr><td>

Access Control

</td><td>

PRB1685081

</td><td>

The business rule 'Check group member privilege' is present when it should have been removed

</td></tr><tr><td>

Access Control

</td><td>

PRB1592670

</td><td>

The 'Session invalidator' job runs and invalidates an older session, causing instance unavailability

</td></tr><tr><td>

Access Control

</td><td>

PRB1717869

</td><td>

The ACL 'asmt\_assessable\_record' \[read\] uses the ITIL role instead of the ITSM/CMDB fine-grained roles or using a combined condition

</td></tr><tr><td>

Access Control

</td><td>

PRB1718132

</td><td>

Conditions don't work on a read 'ui\_page' type ACL rule

</td></tr><tr><td>

Access Control

</td><td>

PRB1718210

</td><td>

snc\_access\_control generates many 'Session invalidator -&lt;USER&gt;' entries on the sys\_trigger table

</td></tr><tr><td>

Access Control

</td><td>

PRB1728431

</td><td>

sys\_security\_acl\_role records are created after installing the 'Explicit roles' plugin that has empty sys\_scope and sys\_package fields

</td></tr><tr><td>

Access Control

</td><td>

PRB1735671

</td><td>

A user can't view variables on reports with Business Stakeholder/ITSM roles

</td></tr><tr><td>

Access Control List \(ACL\) Rules

</td><td>

PRB1713026

</td><td>

tableLevelACLAllow throws an error for a few tables on an instance

</td></tr><tr><td>

Access Control List \(ACL\) Rules

</td><td>

PRB1729095

</td><td>

An ACL name is overwritten with an asterisk \(\*\) on the load of an ACL form when glide.ui.choices.show\_missing is false

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1755658

</td><td>

Downloading attachments from an activity pane in Agent Workspace kills the browsing tab in Chrome, Firefox, Edge

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1748492

</td><td>

The journal tile in now-activity-stream-connected doesn't pick up the correct language after language preference gets changed

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1709271

</td><td>

The user is unable to select email hyperlinks in the Activity Stream of Service Operations Workspace \(SOW\)

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1743075

</td><td>

After Washington DC upgrade, the work notes show extra line breaks

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1736287

</td><td>

If multiple templates are applied, the activity stream composer and form field fail to sync

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1694567

</td><td>

An error message appears in the logs when a task is created on configurable workspaces

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1725845

</td><td>

Text in the 'Comment' section clears on entering text in the required 'Work notes' section

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1763824

</td><td>

A space/line break is observed in UI15's activity stream for emails

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1734763

</td><td>

When @ mentioning someone, removing the first word results in a 400 error on workspace

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1738631

</td><td>

Posting plain text comments and work notes doesn't clear compose text on a case and task

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1754987

</td><td>

The background color of work notes is not yellow when the Next Experience UI is disabled

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1697171

</td><td>

Email details links are not read correctly by the screen reader

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1722795

</td><td>

glide.ui.html.editor. contextmenu=false doesn't work for HTML fields on an activity stream

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1726314

</td><td>

Scrolling should be fixed to not display all the Document Object Model \(DOM\) elements

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1733485

</td><td>

Emails created from an activity stream using 'Reply All' and 'Reply' don't work as expected on UI16

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1736171

</td><td>

When a record is accessed in the workspace during activity stream processing , 'SEVERE \*\*\* ERROR \*\*\* Unparseable date:' displays

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1739271

</td><td>

Email content loses its formatting when long text is used within a table row in Vancouver

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1757111

</td><td>

The user preference for the side by side compose settings aren't saved when creating new records

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1760804

</td><td>

The user avatar is not visible for attachment activity entries on configurable workspaces

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1733920

</td><td>

User preference for the 'Compose' settings is not saved when creating records

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1763981

</td><td>

Activity Streams need a maximum length to guard against tables with excessive audit relations

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1735889

</td><td>

Avoid duplicate awa/work\_item message accumulation on resubscribe

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1735007

</td><td>

AWA assigns multiple cases, exceeding the maximum Agent capacity

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1745788

</td><td>

isLiveAgentAvailable isn't working for domain-separated instances when the requestor and the agent are in different domains

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1707250

</td><td>

Slow query from the AWA work item repository 'getWorkItemsForAgent'

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1702695

</td><td>

A utilization condition interferes with queue routing decisions

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1712555

</td><td>

The Advanced Work Assignment \(AWA\) group queue's priority table is out of synchronization

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1720565

</td><td>

For the interactions that are closed with the state set as 'closed abandoned' due to a transfer fail, the state reason isn't populated

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1727244

</td><td>

Live updates that happen after saving a form but before snFormDataConnected retrieval completes aren't factored into the form after the save completes

</td></tr><tr><td>

Agent Assist

</td><td>

PRB1726805

</td><td>

The cursor jumps around

</td></tr><tr><td>

Agent Assist

</td><td>

PRB1734162

</td><td>

Agent Assist requires multiple attempts at hitting 'Enter' to search in Service Operation Workspace

</td></tr><tr><td>

Agent Assist

</td><td>

PRB1745339

</td><td>

In Service Operations Workspace's Agent Assist, the 'flag' option is present even though 'disabled' suggesting is 'true' for the Knowledge Base

</td></tr><tr><td>

Agent Assist

</td><td>

PRB1769967

</td><td>

Users are unable to add 'Only Knowledge' articles on Agent Assist

</td></tr><tr><td>

Agent Calendar \[Legacy\]

</td><td>

PRB1736903

</td><td>

The Agent is not allowed to create a meeting

</td></tr><tr><td>

Agent Calendar \[Legacy\]

</td><td>

PRB1757720

</td><td>

The business rule 'Restrict only one Primary Work schedule' prevents inserting 'Other' type agent work schedules for one user with a primary work schedule

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1734421

</td><td>

An agent's second chat window appears empty after the agent closes the first chat window

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1753757

</td><td>

The chatbot hover-over text is in the incorrect language

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1762590

</td><td>

Promoted topics text does not show in bold format after a Washington DC upgrade

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1733013

</td><td>

The summary card has a missing **i** icon on the chat panel

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1736749

</td><td>

Avatar initials and the agent-side chat window show inconsistent Initials depending on differences between the user ID and user name

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1771911

</td><td>

Agents who leave themselves available don't get signed out after closing the 'Workspace' tab

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1752938

</td><td>

When creating an interaction, a refresh browser pop-up window opens unless the user selects the **Cancel** button

</td></tr><tr><td>

Agile Development

</td><td>

PRB1742974

</td><td>

A story with a 'Short description' between 35 and 42 characters causes an overlap of UI Actions and **Close Form** \(X/Cross\) button in Agile Board modal

</td></tr><tr><td>

AI Search

</td><td>

PRB1743942

</td><td>

A search profile is updated by a non ais\_admin

</td></tr><tr><td>

AI Search

</td><td>

PRB1732660

</td><td>

The AI Search 'All' tab count does not match the number of returned results

</td></tr><tr><td>

AI Search

</td><td>

PRB1734185

</td><td>

Exact match is skipped if a user hits 'Enter' very quickly

</td></tr><tr><td>

AI Search

</td><td>

PRB1772860

</td><td>

Messages are sent over Asynchronous Message Bus \(AMB\), but the geniusResultsTemplates are null and errors when running genius results through Entity View Action Mapper \(EVAM\)

</td></tr><tr><td>

AI Search

</td><td>

PRB1687420

</td><td>

There's an inaccurate click rank recorded when late binding security is applied in AI Search

</td></tr><tr><td>

AI Search

</td><td>

PRB1724666

</td><td>

AI Search-enabled portal returns inactive catalog items for suggested results

</td></tr><tr><td>

AI Search

</td><td>

PRB1745648

</td><td>

Some of the CSS variables for theming AI Search in Service Portal no longer work

</td></tr><tr><td>

AI Search

</td><td>

PRB1622116

</td><td>

AI Search shows the catalog when the user doesn't have access with the subscriber plugin installed

</td></tr><tr><td>

AI Search

</td><td>

PRB1716502

</td><td>

AI Search \(AIS\) failover replication recovery shouldn't reprocess multiple 'no block' AIS events for the same data source stats

</td></tr><tr><td>

AI Search

</td><td>

PRB1746727

</td><td>

External Content Suggestions from Non-search based suggestions don't open a URL

</td></tr><tr><td>

AI Search

</td><td>

PRB1726781

</td><td>

New translation is not indexed

</td></tr><tr><td>

AI Search

</td><td>

PRB1730043

</td><td>

There's a discrepancy in card type between triggered and clicked Genius Results \(GR\)

</td></tr><tr><td>

AI Search

</td><td>

PRB1730209

</td><td>

An entire article's body displays when hovering over an article in the search results on Employee Center

</td></tr><tr><td>

AI Search

</td><td>

PRB1734894

</td><td>

An AI Search's 'Source Preview' link is incorrect for tables that don't have the 'sys\_class\_name' column

</td></tr><tr><td>

AI Search

</td><td>

PRB1686165

</td><td>

Global search groups results appear in a different order intermittently

</td></tr><tr><td>

AI Search

</td><td>

PRB1699235

</td><td>

AI Search Widget, when used in Portals, does not provide Windows High Contrast Mode Focus Indication

</td></tr><tr><td>

AI Search

</td><td>

PRB1699352

</td><td>

When there are multiple categories in the Service Portal AI search list, screen readers don't announce the name of the category as the user navigates to a result under it

</td></tr><tr><td>

AI Search

</td><td>

PRB1712183

</td><td>

Refreshing the page of global search results sends 2 search requests

</td></tr><tr><td>

AI Search

</td><td>

PRB1713687

</td><td>

AI Search in Service Portal suggests items that aren't available to the user due to the user criteria

</td></tr><tr><td>

AI Search

</td><td>

PRB1714472

</td><td>

A user can't create AI search field settings for fields with names of a length greater than 40 characters

</td></tr><tr><td>

AI Search

</td><td>

PRB1722030

</td><td>

Facets are encoded incorrectly when there's multiple sources

</td></tr><tr><td>

AI Search

</td><td>

PRB1724955

</td><td>

Updates to ais\_genius\_ result\_configuration.request\_ processor\_script aren't applied when the update set is committed

</td></tr><tr><td>

AI Search

</td><td>

PRB1726532

</td><td>

Search fails if the department's parent column is anything other than the same department

</td></tr><tr><td>

AI Search

</td><td>

PRB1726710

</td><td>

Cascade update events are still created when an indexed source is set to false

</td></tr><tr><td>

AI Search

</td><td>

PRB1726721

</td><td>

'Recently viewed suggestions' display the **Description** field even though the model returns aisearch\_teaser\_title

</td></tr><tr><td>

AI Search

</td><td>

PRB1727056

</td><td>

Domain-separated user criteria isn't honored by AisCatalogItemQuery

</td></tr><tr><td>

AI Search

</td><td>

PRB1727142

</td><td>

The range facet isn't displaying for late-binding indexed sources

</td></tr><tr><td>

AI Search

</td><td>

PRB1728608

</td><td>

An aria label for the **clear\{\}** button isn't translated

</td></tr><tr><td>

AI Search

</td><td>

PRB1729952

</td><td>

ingestSingleRecord causes a record to be deleted, as the filter check on an indexed source is case-sensitive

</td></tr><tr><td>

AI Search

</td><td>

PRB1737451

</td><td>

Upon upgrading, global search is missing when hash-map based upgrade optimizer is used

</td></tr><tr><td>

AI Search

</td><td>

PRB1737517

</td><td>

AIS Init should reindex datasources asynchronously when AIS is already initialized

</td></tr><tr><td>

AI Search

</td><td>

PRB1747038

</td><td>

Action payload mapping data in the UI is different than in the XML

</td></tr><tr><td>

AI Search

</td><td>

PRB1748854

</td><td>

No results for any search terms are returned on global, search portal, and ESC

</td></tr><tr><td>

AI Search

</td><td>

PRB1748983

</td><td>

Sorting a list doesn't work in Service Portal

</td></tr><tr><td>

AI Search

</td><td>

PRB1758639

</td><td>

When using a screen reader, the focus indicator does not advance past the first entry when attempting to scroll through the list of recent searches

</td></tr><tr><td>

AI Search Assist

</td><td>

PRB1732784

</td><td>

Attachments in the search results break the AI Search Assist widget's pagination \(Up/Down arrows\)

</td></tr><tr><td>

AI Search Assist

</td><td>

PRB1734491

</td><td>

An external URL isn't displayed for a content item using AI Search Assist

</td></tr><tr><td>

AI Search Assist

</td><td>

PRB1765456

</td><td>

How-To template articles do not render body content in the 'Create incident' contextual search in Employee Center

</td></tr><tr><td>

AI Search Glide

</td><td>

PRB1578586

</td><td>

User criteria late binding and early binding contradict access when the category level is not available

</td></tr><tr><td>

AI Search Glide

</td><td>

PRB1594303

</td><td>

Incremental updates aren't working for dot-walked reference fields

</td></tr><tr><td>

Analytics Hub

</td><td>

PRB1718540

</td><td>

In Analytics Hub, there's an issue displaying a week's numbers in the French language

</td></tr><tr><td>

Analytics Hub

</td><td>

PRB1739877

</td><td>

The pa\_admin role cannot add a comment to the Analytics Hub

</td></tr><tr><td>

Analytics Hub

</td><td>

PRB1763326

</td><td>

In Performance Analytics, the 'Cancel' \(x\) icon in the search isn't aligned correctly

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1768085

</td><td>

Overriding glide.cache.hard\_references can cause the dependency cache to be garbage collected when upgrading to Washington DC

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1695862

</td><td>

sys\_ui\_view and sys\_ui\_form records are not deleted when the change is published to AppRepo from Source and the app is installed on the Target

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1716980

</td><td>

UI form sections in app packages delete the default view instead of deleting the targeted view

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1723518

</td><td>

A portal taxonomy record's **Active** field is set to false when users install EC Pro

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1735394

</td><td>

When the App Operation Queue Health Monitor \(scheduled job\) is missing or inactive the Application Operation Queue doesn't execute

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1740567

</td><td>

Installing a global application results in a skip to review for a record with no claim in the package, but a base claim exists on the instance

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1743934

</td><td>

Activating plugins using the new application manager logs as 'system', whereas the old manager logs as the user who activated the plugin

</td></tr><tr><td>

Application Manager

</td><td>

PRB1719552

</td><td>

AppClient displays a 'pending' state even when the application successfully installs

</td></tr><tr><td>

Application Manager

</td><td>

PRB1681825

</td><td>

The user observes a '404 page not found' error after closing a pop-up from the repair modal

</td></tr><tr><td>

Application Manager

</td><td>

PRB1723206

</td><td>

sn\_appclient.apps\_last\_sync\_time property changes are being tracked in update sets

</td></tr><tr><td>

Application Manager

</td><td>

PRB1728977

</td><td>

Buttons on an application manager page don't show text with theme builder in Next experience

</td></tr><tr><td>

Application Manager

</td><td>

PRB1737218

</td><td>

When using Application Manager to review application updates, an error occurs when trying to review the list of Customized Files for a customized application

</td></tr><tr><td>

Application Manager

</td><td>

PRB1736510

</td><td>

An admin user isn't able to install a framework app when app updates of only framework apps are shipped from store

</td></tr><tr><td>

Application Manager

</td><td>

PRB1719299

</td><td>

When installing an application with a large number of dependencies, the batch installer returns '414 URI too long'

</td></tr><tr><td>

Application Manager

</td><td>

PRB1722187

</td><td>

Studio Git is switching branches and not automatically discarding ACL changes as expected based on the rights of the developer

</td></tr><tr><td>

Application Manager

</td><td>

PRB1734718

</td><td>

The search results for already installed applications are incorrect

</td></tr><tr><td>

Application Manager

</td><td>

PRB1754629

</td><td>

The 'Proceed to Update' option does not appear, even though there are app updates under some products

</td></tr><tr><td>

Application Manager

</td><td>

PRB1756440

</td><td>

The 'Attachment' script include had accessibility changed from 'All Application Scopes' to 'This Application Scope Only'

</td></tr><tr><td>

Application Navigator

</td><td>

PRB1716876

</td><td>

'\*\*\* ERROR \*\*\* NavigatorHistory No such column: ui\_type' appears when the sys\_ui\_navigator\_history table doesn't have the 'ui\_type' column

</td></tr><tr><td>

Application Navigator

</td><td>

PRB1750960

</td><td>

It is difficult for screen-reader and keyboard-only users to navigate a page when the 'All' menu is pinned

</td></tr><tr><td>

Application Portfolio Management

</td><td>

PRB1729500

</td><td>

In the new Application Manager, the 'Install Details' pop-up can have the 'Demo Data' check box checked by default

</td></tr><tr><td>

Application Portfolio Management

</td><td>

PRB1715173

</td><td>

Application Portfolio Management \(APM\) Performance Analytics issue

</td></tr><tr><td>

Application Portfolio Management

</td><td>

PRB1715689

</td><td>

Application services associated with SDLC components are not shown in TPM lifecycles view

</td></tr><tr><td>

Application Portfolio Management

</td><td>

PRB1720559

</td><td>

The sn\_apm\_generate\_assessments page isn't adjusted to support the 'Dark' mode properly

</td></tr><tr><td>

Application Scoping

</td><td>

PRB1667466

</td><td>

Business Logic Flaws in Application Scoping

</td></tr><tr><td>

Application Scoping

</td><td>

PRB1687716

</td><td>

Users can edit metadata in private scopes since the sys\_store\_app license change

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1740485

</td><td>

Availability API throws an error when selecting a calender icon from a walk-up record producer

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1756203

</td><td>

Month and day are not translated in the appointment booking modal

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1758818

</td><td>

Appointment tasks aren't assigned immediately after booking

</td></tr><tr><td>

Appointment Booking

</td><td>

PRB1773412

</td><td>

When submitting a record producer with an appointment booking configuration, 'Appointment window is no longer available. Please select another appointment' displays

</td></tr><tr><td>

Approvals

</td><td>

PRB1729612

</td><td>

There's a performance issue when querying a sc\_req\_item when the request is deleted for a **Stage** field

</td></tr><tr><td>

Archive Rules

</td><td>

PRB1762255

</td><td>

Archived approvals aren't displaying because of a broken ACL

</td></tr><tr><td>

Archive Rules

</td><td>

PRB1732196

</td><td>

The RefCopyJob doesn't complete if the table doesn't have records

</td></tr><tr><td>

Archive Rules

</td><td>

PRB1693969

</td><td>

Glide.db.archiving .max\_consumer\_workers is not immediately honored when it decreases

</td></tr><tr><td>

Assessments

</td><td>

PRB1770524

</td><td>

An ACL isn't functioning correctly because of a syntax issue

</td></tr><tr><td>

Assessments

</td><td>

PRB1733138

</td><td>

When the assessment response in grouped and attestation is minimized the dependent fields are not displayed when it is expanded back

</td></tr><tr><td>

Assessments

</td><td>

PRB1748845

</td><td>

Assessment is submitted with mandatory fields when submitted through Printer Friendly Version

</td></tr><tr><td>

Asset Management

</td><td>

PRB1723307

</td><td>

SAM Foundation code is present in the 'Base Asset Management' business rule

</td></tr><tr><td>

Asset Management

</td><td>

PRB1757504

</td><td>

Some thumbnail attachments for pc\_hardware\_cat\_item get ZZ\_YYZZ\_YY prefix in attachment table

</td></tr><tr><td>

Asset Management

</td><td>

PRB1701884

</td><td>

The original transfer order stays 'Work In Progress' even though 'Transfer Order Return' is initiated and completed

</td></tr><tr><td>

Asset Management

</td><td>

PRB1714849

</td><td>

On Asset Workspace, the important actions count is incorrect in domain-separated instances that have domain visibilities

</td></tr><tr><td>

Asset Management

</td><td>

PRB1717913

</td><td>

UI actions under the Asset Management application use the ITIL role instead of the ITSM fine-grained roles

</td></tr><tr><td>

Asset Management

</td><td>

PRB1738355

</td><td>

The Vendor Management Workspace **Renew** button is not functional

</td></tr><tr><td>

Asset Management

</td><td>

PRB1742587

</td><td>

CIs created without a manufacturer and model link to 'Unknown' models, but models with a manufacturer entered may get used, adding that to the model name

</td></tr><tr><td>

Asset Management

</td><td>

PRB1757082

</td><td>

The **Requested For** field on a 'Reclaim Asset' catalog item is not set to required

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

</td><td>

PRB1738465

</td><td>

AMB cluster synchronizer can fail to start when it encounters an invalid channel name

</td></tr><tr><td>

ATG - Glide Interfaces

</td><td>

PRB1762735

</td><td>

Italian stopwords are not removed from the 'Visualization' tab when training a workflow clustering definition

</td></tr><tr><td>

ATG - Glide Interfaces

</td><td>

PRB1735703

</td><td>

Update 'Fix ITSM Predictor Results' fix script to make it more generic to set finalOutputValue as per predictedOutput value type

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1733053

</td><td>

The 'Remove' and 'Rename' options aren't available on an Employee Document Management \(EDM\) attachment

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1737426

</td><td>

Unable to attach .ics file extension to records

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1739760

</td><td>

Loading an XML attachment in an XMLDocument2 object via GlideScriptableInputStream does not work as expected

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1761911

</td><td>

There's an issue with encryption when attachments are copied from a task to a requested item

</td></tr><tr><td>

Audit History

</td><td>

PRB1740373

</td><td>

Deleting records on old sys\_audit shards results in inserts into the current sys\_audit tables and leads to disk growth

</td></tr><tr><td>

Authentication

</td><td>

PRB1718457

</td><td>

The login component in UI builder doesn't redirect the user to Single Sign On

</td></tr><tr><td>

Authentication

</td><td>

PRB1742755

</td><td>

Security Assertion Markup Language \(SAML\) single sign-on \(SSO\) log in fails for MultiSSOv1 during an upgrade to Washington DC

</td></tr><tr><td>

Authentication

</td><td>

PRB1713173

</td><td>

There's a user mismatch error that occurs due to a camelcase difference between the user\_name in sys\_user and the received user\_name in the OpenID Connect \(OIDC\) response claim

</td></tr><tr><td>

Authentication

</td><td>

PRB1726569

</td><td>

glide.basicauth.update \_last\_login\_time, which sets the last log in time of users, also updates sys\_updated\_on, sys\_updated\_by, and sys\_mod\_count

</td></tr><tr><td>

Authentication

</td><td>

PRB1732623

</td><td>

IMAP access tokens are expiring during an upgrade

</td></tr><tr><td>

Authentication

</td><td>

PRB1751459

</td><td>

Some messages displayed on the password change screen are not translated into Japanese

</td></tr><tr><td>

Authentication

</td><td>

PRB1756765

</td><td>

The Now Login widget does not show the language picker

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1717536

</td><td>

Setting a value in the select2 element fails on a Service Portal page

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1760564

</td><td>

Missing test data in the parameterized test will fail the suite and leave it in a 'Running' state

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1761012

</td><td>

When a child transaction is terminated by memory watcher, the root tracker remains running

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1729292

</td><td>

An embedded list that's present in a form causes a test with 'Validate Related List Visibility' to fail

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1710308

</td><td>

A large snapshot causes a test to succeed

</td></tr><tr><td>

Cache

</td><td>

PRB1709933

</td><td>

Cache synchronization doesn't work on restarted nodes for catalogs that get updated after the node restart timestamp

</td></tr><tr><td>

Cache

</td><td>

PRB1709834

</td><td>

The cached scriptable API still queries for inputs during decision table evaluation

</td></tr><tr><td>

Cache

</td><td>

PRB1724751

</td><td>

sys\_choice causes cache issues when the number element values are large

</td></tr><tr><td>

Cache

</td><td>

PRB1741630

</td><td>

Role cache has stale entries in a scenario where one node caches a non-existing role and another node imports that role via XML

</td></tr><tr><td>

Cache

</td><td>

PRB1744271

</td><td>

If attempting to populate a large map from the database takes longer than 5 seconds, another thread could enter and attempt to do the same thing, causing multiple threads to create separate large hash maps and memory pressure

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1735647

</td><td>

When a catalog item title is long, the 'Edit' icons aren't visible and a user must zoom out to see them

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1756562

</td><td>

Unnecessary 'sys\_scoped\_admin\_acl\_inheritance' records on the non-sys\_metadata table 'sys\_attachment'

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1760617

</td><td>

The 'Query' business rule should add a bypass for the system user

</td></tr><tr><td>

Case Management

</td><td>

PRB1725822

</td><td>

'Find Agents' shouldn't include non-ITIL assignment groups

</td></tr><tr><td>

Case Management

</td><td>

PRB1746238

</td><td>

The **New** button from the 'Publication' related list should be removed

</td></tr><tr><td>

Case Management

</td><td>

PRB1750553

</td><td>

The Account and Contact field data often disappears upon updating the case

</td></tr><tr><td>

Catalog Client Scripts

</td><td>

PRB1734165

</td><td>

The g\_user method is not working for a catalog item pop-up

</td></tr><tr><td>

Change Management

</td><td>

PRB1702068

</td><td>

Identify a Dynamic CI group from common CIs added into the 'affected CIs' of the task

</td></tr><tr><td>

Change Management

</td><td>

PRB1727062

</td><td>

The 'Conflict' calendar in Scheduling Assistance displays an error

</td></tr><tr><td>

Change Management

</td><td>

PRB1742266

</td><td>

The 'Change - Unauthorized - Review' flow is missing

</td></tr><tr><td>

Change Management

</td><td>

PRB1746451

</td><td>

The default value of glide.approval\_engine.change\_task is still 'Process Guides', which is deprecated and should not be used

</td></tr><tr><td>

Change Management

</td><td>

PRB1747938

</td><td>

The Change Advisory Board \(CAB\) workbench blocks one hour for CAB meetings that are scheduled for less than one hour

</td></tr><tr><td>

Change Management

</td><td>

PRB1754593

</td><td>

When com.snc.change\_management. change\_model.hide and com.snc.change\_management. change\_model.type\_compatibility are true, the change request is redirected two levels when a change request is created

</td></tr><tr><td>

Change Management

</td><td>

PRB1756173

</td><td>

Approving a change record via the CAB Workbench without providing a comment in the pop-up modal still creates an activity for comments in the sysapproval\_approver record

</td></tr><tr><td>

Change Management

</td><td>

PRB1759338

</td><td>

The calculated risk score updates the impact in the database during risk/impact evaluation, kicking off a new transaction and resulting in incorrect messaging

</td></tr><tr><td>

Change Management

</td><td>

PRB1768653

</td><td>

When creating a change request, the 'State' of tabs is confusing to visually impaired users

</td></tr><tr><td>

Change Management

</td><td>

PRB1768655

</td><td>

Change models' buttons are read out incorrectly when using JAWS

</td></tr><tr><td>

Change Management

</td><td>

PRB1772868

</td><td>

If users use HTML syntax in 'Change Model' templates, users are unable to create a change request through change models

</td></tr><tr><td>

Change Management Collision Detector

</td><td>

PRB1718631

</td><td>

The Conflict Status reverts back to 'Not Run' if the Assessment State is skipped

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1745770

</td><td>

'showFieldMsg' of 'On change client script' disappears quickly on workspace

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1724306

</td><td>

The setvalue for a check box variable differs between the UI and the record after using the **Back** and **Forward** button in the browser

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1759330

</td><td>

The client script 'WS1 UEM Open new tab for assist' does not trigger

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1714508

</td><td>

g\_form.submit\(\) client-side code in workspace isn't allowing the 'promise' functionality using .then\(\) in the code

</td></tr><tr><td>

Client Scripts

</td><td>

PRB1759667

</td><td>

g\_form.setReadOnly for 'link', 'script', and 'client\_script' in the header and footer \(sp\_header\_footer\) doesn't work

</td></tr><tr><td>

Client Software Distribution

</td><td>

PRB1762221

</td><td>

Client Software Distribution \(CSD\) 1.0 software revoke issue

</td></tr><tr><td>

Cloud Encryption

</td><td>

PRB1740559

</td><td>

With quorum control on, if there is an error creating the Quorum Control Request record, throw the exception and prevent the dare\_key\_request from being stuck in processing state

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1633842

</td><td>

After Cloud Provisioning and Governance \(CPG\) to 'Patterns Migration Cloud Discovery' still launches Cloud API \(CAPI\) orders, causing a performance impact

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1729820

</td><td>

There's multiple performance issues with AWS Cloud Event processing

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1716781

</td><td>

Exception handling is incorrect when provisioning takes a long time

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1540112

</td><td>

When a user name has Japanese Strings, the tag value becomes garbled

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1707089

</td><td>

The Data Center doesn't load due to a large number of records in the 'Storage Volume' related list being associated with the data center, causing the execution time to max out

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1770243

</td><td>

Discoveries triggered from Cloud.account via DiscoverNow don't trigger the infra patterns

</td></tr><tr><td>

CMDB CI Class Manager

</td><td>

PRB1730839

</td><td>

When the scope of global ACL records is changed to 'Global Customization - Upgrade Plan', REST API throws a '403 Forbidden' error

</td></tr><tr><td>

CMDB CI Class Manager

</td><td>

PRB1669983

</td><td>

The Basic Info page takes ~5 minutes to display in the first attempt and re-run takes ~35 seconds

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1717464

</td><td>

The condition filter count, 'records match condition' link, and 'Preview' list in CMDB Data Manager may use an incorrect retirement definition

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1758088

</td><td>

Archive tasks with CI counts above 1,000 may error out and not archive the full list

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1709874

</td><td>

CMDBRetirementScriptableApi .getFullEncodedQuery API throws ArrayIndexOutOfBoundsException

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1729974

</td><td>

Dependent CI deletion tasks don't have attachment for deleted CIs

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1668702

</td><td>

The display name in cmdb\_rel\_type table is not the combination of the parent descriptor and child descriptor when the language is Japanese

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1693656

</td><td>

The life cycle field and value calculated column does not respect children values in the CMDB hierarchy

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1727234

</td><td>

The 'Dependent CI Deletion' policy doesn't accept customization of subflows

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1729909

</td><td>

Users can't remove policy descriptions when editing a policy via CMDB Data Manager

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1732983

</td><td>

Fields being compared for 'no-change' during an insert can cause payload values to not be set on those fields

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1733575

</td><td>

There's a broken default script coming from the cert\_audit's table's default\_value for a script field, which makes cert\_audits unable to run

</td></tr><tr><td>

Code Signing

</td><td>

PRB1722766

</td><td>

A database safe override property without a safe value is skipped during upgrade

</td></tr><tr><td>

COE Legacy Family Component

</td><td>

PRB1753063

</td><td>

The Asia/Almaty timezone continues to display as UTC+6 since March 1st, 2024 on the calendar UX component

</td></tr><tr><td>

Communities

</td><td>

PRB1727794

</td><td>

There's slowness when opening a topic consisting of many, around 2400, forums in communities

</td></tr><tr><td>

Communities

</td><td>

PRB1754041

</td><td>

User community profiles are not removed when a user is deactivated

</td></tr><tr><td>

Communities

</td><td>

PRB1761664

</td><td>

After cloning the community\_create\_event page, the DIV 'create-event-container' is hidden by default and does not appear

</td></tr><tr><td>

Communities

</td><td>

PRB1774977

</td><td>

The 'Featured' tab in a community user profile displays text from other tabs

</td></tr><tr><td>

Community Service Portal

</td><td>

PRB1744322

</td><td>

The short description of the Knowledge title is not displayed in the Community search result

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1777164

</td><td>

Change Advisory Board \(CAB\) workbench displays an extra backslash in the **Planned start date** field

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1750793

</td><td>

There's an incorrect label in the 'is one of' comparison type

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1722622

</td><td>

A filter in Workspace shows sys\_id in place of the variable name

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1593149

</td><td>

A dot-walking component sticks in a loading state when selecting variables

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1611325

</td><td>

A new condition builder is not working correctly for the **Other** date field type

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1716021

</td><td>

addEncodedQuery changes the URL query from 'Not like' to 'Does not contain'

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1689206

</td><td>

Users should be informed to press the right arrow to open a dot-walk expanded list

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1690879

</td><td>

The **Amount** field is wiped off in the condition builder in workspace view

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1718166

</td><td>

The filter for a configuration item pop-up search isn't working in Service Operations Workspace

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1718773

</td><td>

A permissions label that's associated with a radio button isn't announced by a screen reader

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1738408

</td><td>

Filter conditions 'is more than' and 'is less than' do not work as expected in the Platform Analytics Workspace

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1538972

</td><td>

CMDB Query Builder has high memory utilization with queries containing operator nodes

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1751775

</td><td>

Reduce the writes to the cmdb\_datasource\_last\_update table

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1748280

</td><td>

Incorrect log message 'Stopped processing partial payloads.' even where there are no partial payloads to process

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1666448

</td><td>

Life Cycle API allows the creation of Duplicate Stages/Statuses

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1687147

</td><td>

Custom life cycle mapping doesn't work as expected

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1701048

</td><td>

CMDBTASK creation sends duplicate notifications

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1565197

</td><td>

When the business rule 'Sync Ops Status for CMDB CI' is customized, the legacy fix script that created it completely ignores any updates

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1673894

</td><td>

CertificationProcessing uses too much memory and performs very slowly

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1689097

</td><td>

There's a color contrast failure for a selected item under the 'ciModel.do' page

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1708243

</td><td>

The default semaphore is impacted due to a large number of application service records in cmdb\_ci\_service\_auto while running the job 'Calculate App Services Missing Data'

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1708303

</td><td>

The number of CIs in the 'svc\_ci\_assoc' table do not match the number of CIs in the result of the encoded query in the related Dynamic CI group's CMDB group

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1709507

</td><td>

The 'Sync Ops Status for CMDB CI' business rule isn't working as expected when the language is Japanese

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1743081

</td><td>

Unused index on the cmdb\_datasource\_last\_update table

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1754898

</td><td>

Improve the health jobs scoring in domain separation

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1508482

</td><td>

Partial payloads merge causes MULTIPLE\_DEPENDENCIES error

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1669388

</td><td>

Only Istanbul or later instances should have 'Ready' and 'Retired' operational status values 5/6, but language packs add all the choices

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1732485

</td><td>

The data manager archival policy fails if trigger\_type is anything other than 'Interval'

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1734920

</td><td>

Dark theme doesn't show the icons properly on CMDB CI Services

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1741163

</td><td>

The 'Sync Managed By Group from CI Class' script action is not batched

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1688963

</td><td>

Reverse Sync Choice duplicates

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1709386

</td><td>

The 'Relationship editor' page fires two identical pagination requests on each **Next** pagination click

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1714712

</td><td>

The 'Modify Relationship' pop-up in the 'Dependency' view is left-aligned in Utah and Vancouver, but is center-aligned in Tokyo

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1719623

</td><td>

The legacy CI relations' formatter doesn't link to the correct task lists when in 'tree' mode

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1722001

</td><td>

Reconciliation rules aren't letting users update an empty value in attributes

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1722636

</td><td>

The widget 'Cloud Requests Tabs' uses the ITIL role instead of the ITSM/CMDB fine-grained roles or using a combined condition

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1725941

</td><td>

The CMDB Workspace record page's 'CI timeline' component fails to load when there's too many audit history records

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1730333

</td><td>

On service recalculation, dependent application services are deleted

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1730795

</td><td>

Identification and Reconciliation Engine \(IRE\) simulator/the identifyCIEnhanced API returns a NO\_IDENTIFIER\_KEYS error in an insert scenario for a dependent item

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1731438

</td><td>

Multisource records should be cleaned up when multi-source for non-CMDB is turned off

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1732243

</td><td>

The 'Enforce 1-1 reverse mappings' business rule prevents reverse sync=true for different legacy fields, which should be allowed

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1734586

</td><td>

Hardware servers that aren't in an 'Application Service' report don't display servers that have a relationship to services that aren't classified as an 'Application' service

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1735603

</td><td>

Reconciliation definition mappings \(cmdb\_reconciliation\_ definition\_mapping\) don't get added to an update set

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1747749

</td><td>

The custom batch size property for data managers does not work as expected

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1749714

</td><td>

After a CI is deleted in accordance with the delete policy, cmdb\_ci\_state\_ management\_task\_to\_ci still retains a reference to the deleted CI

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1749921

</td><td>

When a CI is inserted, its life cycle values are set to the default value instead of being derived from legacy values

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1750915

</td><td>

Incorrect behavior in base instance client script 'Clear begin and end'

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1754392

</td><td>

Record.java queries items from sys\_dictionary, which are available in the table descriptor cache

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1754547

</td><td>

The 'Sort by' list on the CMDB Query Builder page only sorts as descending

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1757075

</td><td>

While adding new life cycle mapping, the UI does not let the user select 'None' as a subfield value

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1757510

</td><td>

As per CSDM, CI relationships from business application to the application service should be 'Consumes::Consumed By', but when a user creates an application service in CSDM, it shows 'Consumed by :: Consumes'

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1761907

</td><td>

Domains should be validated before persisting into the cmdb\_health\_processor status table

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1773826

</td><td>

onBefore and onAfter scripts don't work when initialized from setRun\(\) and when the data source is null

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1736182

</td><td>

Multi-source code updates records with the same sys\_updated\_on through multiple DB updates

</td></tr><tr><td>

Connect Chat

</td><td>

PRB1692098

</td><td>

An influx of queries on live\_group\_member causes a high CPU load on a DB server

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1747453

</td><td>

The article navigation shows as 'HOME/Null' in Washington DC

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1731850

</td><td>

The 'Related Search' results header overlaps with the search results

</td></tr><tr><td>

Contextual Search

</td><td>

PRB1746563

</td><td>

Login events are created for users when 'Search As' is initiated

</td></tr><tr><td>

Continual Improvement Management

</td><td>

PRB1718946

</td><td>

The script include 'CIMUtil' uses the ITIL role instead of the ITSM/CMDB fine-grained roles or using a combined condition

</td></tr><tr><td>

Continual Improvement Management

</td><td>

PRB1753753

</td><td>

Common Information Model \(CIM\) Indicators don't respect glide.system.locale

</td></tr><tr><td>

Contractor Management

</td><td>

PRB1729666

</td><td>

Questionnaire image upload error for contractors on mobile app

</td></tr><tr><td>

Core Platform

</td><td>

PRB1707194

</td><td>

xmlstats.do and/or PortScanGlideServiceStatusProvider hits port 80 on service endpoints beginning with https

</td></tr><tr><td>

Core Platform

</td><td>

PRB1425002

</td><td>

Reference fields that are referencing a Date/Time field get converted to GMT when a record is saved

</td></tr><tr><td>

Core Platform

</td><td>

PRB1644827

</td><td>

There's errors when committing an update set that creates a child table with a **Function** field

</td></tr><tr><td>

Core Platform

</td><td>

PRB1758692

</td><td>

NativeRecordMutex should not consider domains during 'get' or 'release'

</td></tr><tr><td>

Core Platform

</td><td>

PRB1594189

</td><td>

Decompiling JavaScript to pass compiled functions, as strings can lead to high memory churn

</td></tr><tr><td>

Core Platform

</td><td>

PRB1696571

</td><td>

A node's scheduler changes to 'any' from 'specified' after node restart

</td></tr><tr><td>

Core Platform

</td><td>

PRB1704668

</td><td>

A node log is missing the SessionID and txID in the localhost log, causing an incorrect date format

</td></tr><tr><td>

Core Platform

</td><td>

PRB1705439

</td><td>

Non-thread safe operation

</td></tr><tr><td>

Core Platform

</td><td>

PRB1763492

</td><td>

The expression cache size increases to up to 1GB due to some scheduled jobs that are calling script includes with large sized JSON data to process

</td></tr><tr><td>

Core Platform

</td><td>

PRB1642006

</td><td>

A list doesn't sort by rating properly when adding filter conditions for knowledge articles

</td></tr><tr><td>

Core Platform

</td><td>

PRB1718789

</td><td>

The 'Show Log Entries' UI action isn't displaying the corresponding log

</td></tr><tr><td>

Core Platform

</td><td>

PRB1735417

</td><td>

GlideJellyContext's parser cache \(fParserStack\) may retain a lot of states

</td></tr><tr><td>

Core Platform

</td><td>

PRB1741869

</td><td>

Delegation clean-up should not have an end date if the delegation is already ended

</td></tr><tr><td>

Core Platform

</td><td>

PRB1744149

</td><td>

The Security Assertion Markup Language \(SAML\) transform map has a gs.log statement

</td></tr><tr><td>

Core Platform

</td><td>

PRB1754999

</td><td>

'\_log\_table' is included twice in the 'sys\_outbound\_http\_log' message exported by Log Export Service

</td></tr><tr><td>

Core Platform

</td><td>

PRB1760524

</td><td>

The IP normalization job fails if there are any blank values in the field being normalized

</td></tr><tr><td>

Crew Operations

</td><td>

PRB1758968

</td><td>

Error when changing the crew leader 'Access to API 'setWorkflow' from scope 'sn\_fsm\_crew' has been refused due to the API's cross-scope access policy'

</td></tr><tr><td>

Crew Operations

</td><td>

PRB1763496

</td><td>

Reassigning the crew leader to a different crew member results in a crew with 2 duplicated crew leaders in the Dispatcher Workspace

</td></tr><tr><td>

Crew Operations for Dispatcher Workspace

</td><td>

PRB1764931

</td><td>

When the user sets the **Needs crew** field to false and saves, duplicate WOT cards appear in the calendar of the Dispatcher Workspace

</td></tr><tr><td>

Critical Security Update Manager \(Family Release\)

</td><td>

PRB1733701

</td><td>

The 'Enable 3DES Deprecation' link is broken in **Security Center** &gt; **Critical Updates**

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1746302

</td><td>

When updating a record via GlideRecord, the reference amount updates are based on the latest currency rate even if the input/session amount has not changed

</td></tr><tr><td>

Customer Operations for Customer Service Management

</td><td>

PRB1749397

</td><td>

Unexpected behavior while configuring the form layout for the customer\_account table in the default view, but not for other views

</td></tr><tr><td>

Customer Operations for Customer Service Management

</td><td>

PRB1711621

</td><td>

There's an issue with the 'Primary Contact' association in the 'sn\_customerservice\_ m2m\_asset\_contact' table

</td></tr><tr><td>

Data Archiving

</td><td>

PRB1743164

</td><td>

Record estimate times out upon selecting a recalculate estimate in the archive destroy rule

</td></tr><tr><td>

Database Indexes

</td><td>

PRB1694114

</td><td>

Creating a unique index on sys\_user\(sys\_id, active\) can lead to data loss in sys\_user table

</td></tr><tr><td>

Database Indexes

</td><td>

PRB1699808

</td><td>

Allow the creation of indexes with online setting in an 'Enterprise edition' database

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1732151

</td><td>

Using TableDescriptor.isValid or GlideRecord.isValid to check if a string is a table fills up the Table Descriptor Cache with things that are not tables causing an Out of Memory \(OOM\) error

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1760592

</td><td>

Prepared queries are not formed correctly on Rotation Tables

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1714908

</td><td>

GlideAggregate queries against table rotations generate incorrect results

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1739880

</td><td>

Ignore forcePrimaryKeyOrdering for 'TS' queries

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1514936

</td><td>

Union replacement isn't adding the table alias in the 'ORDER BY' value, causing the platform to not apply the union replacement

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1643974

</td><td>

A general data exception error detected by the database occurs when a report uses a 'more than' condition on the **Date** field

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1749083

</td><td>

On migration, an automatic activation of the 'Low connection' mode should be turned off

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1757110

</td><td>

On a Glide upgrade from Vancouver to Washington, there's an error

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1670286

</td><td>

A query does not direct the user to the gateway database for tables with long table names

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1688148

</td><td>

StorageColumnResetter causes table locking when deleting columns while it inserts null data

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1736307

</td><td>

GlideRecord methods jsFunction\_updateMultiple and jsFunction\_deleteMultiple should guard against query conditions with invalid field names

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1742990

</td><td>

Typo observed in the deleteDuplicates fix script

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1747247

</td><td>

Use DropTmpTablesJob to clean orphaned update staging tables

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1763146

</td><td>

If GlideFilter has a new query \(NQ\) to add multiple conditions, it generates different JavaScript from the same encoded query

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1647519

</td><td>

Localhost logs do not print 'MySQL thread id' in local host logs

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1777345

</td><td>

Out of memory \(OOM\) Error due to domain separation plugin installation

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1734995

</td><td>

Nodes are restarted due to an out of memory error

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1730026

</td><td>

'0' should be returned on a record addJoinQuery for an email to a case

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1744977

</td><td>

Creating a function field through sys\_dictionary incorrectly creates a storage alias metadata for the field

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1751743

</td><td>

Parsing the FromItem type '\[SubSelect\]' isn't supported

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1766707

</td><td>

Reference fields to child tables of third-party contract \(TPC\) hierarchies with names prefixed with 'ref\_' produce an invalid SQL

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1781863

</td><td>

If a column is stored in the CMDB partition, the RLQuery related list condition isn't working

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1723302

</td><td>

ArchiveJob incorrectly updates record\_estimate upon exception

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1737526

</td><td>

The 'Update' UI action for the sys\_dm\_delete table does not work correctly if the user has set the Date Format \(in the user table\) to yyyy-MM-dd.

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1713164

</td><td>

In TableCleaner, if a rule is active during the restart, the rule is skipped for 2 days post the node restart

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1733299

</td><td>

CloneDBAPI\(\).getExcludeStatements fails at exclusion with an error: 'sys\_term02.sys\_class\_name doesn't exist'

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1734637

</td><td>

A newly added node on an instance has '\{\}' added to the glide\_build\_tag and some of the node has a null/empty glide\_build\_tag

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1718003

</td><td>

UNION statement changes in Utah for Oracle instances impact execution times

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1671297

</td><td>

Review whether more tables need to be added to TableCheckpointExclusionList

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1731352

</td><td>

The likelihood of dropping critical messages needs to be reduced

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1744444

</td><td>

Do not retry timed out read replica queries on the primary database

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1752213

</td><td>

The replication lag throttler pauses at 4 hours 41 minutes when the longest lag detected was 11 minutes

</td></tr><tr><td>

Database Views

</td><td>

PRB1730383

</td><td>

Records are missing in the database views with **Function** fields

</td></tr><tr><td>

Data Certification

</td><td>

PRB1742248

</td><td>

The base instance email template 'certification.task.reminder.inserted' is not populating the cmdb\_ci.URI\_REF while sending the notification

</td></tr><tr><td>

Data Certification

</td><td>

PRB1735000

</td><td>

closed\_at of cert\_task isn't updated when the record is closed a second time

</td></tr><tr><td>

Data Collection for Oracle Global Licensing and Advisory Services for Software Asset Management

</td><td>

PRB1743059

</td><td>

After downloading the Global License Advisory Services \(GLAS\) Data Collection zip folder, users observe the Windows error 'Windows cannot open the folder and zip file is invalid'

</td></tr><tr><td>

Data Filtration

</td><td>

PRB1768454

</td><td>

In Vancouver's data filteration, IP filter criteria provided in the subject condition isn't considered

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB1759020

</td><td>

Plugin 'sn\_dp\_store\_app' adds a new field level ACL which prevents access to fields of table sys\_filter

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB1732467

</td><td>

An incorrect message is shown when scheduling user-based jobs when a primary reference isn't set

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB1772904

</td><td>

When scheduling the 'Data privacy' job with input for a column more than the allowed character length of the column in sys\_dictionary, the job errors out

</td></tr><tr><td>

Decision Table \(Family\)

</td><td>

PRB1758837

</td><td>

An imported reference record is not honored after saving for some restricted roles

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1695335

</td><td>

The **Configuration Item** field filter condition doesn't get applied to the pop-up modal

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1707531

</td><td>

A list's grouped actions appear as secondary even when they're configured to be primary

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1754553

</td><td>

Declarative actions throw a 'JSONObject\['value'\] not found ' error if the variable editor is added to the form

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1759017

</td><td>

There's an error on some builds

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1767497

</td><td>

Declarative actions aren't working with a random key in the payload definition

</td></tr><tr><td>

Declarative Actions

</td><td>

PRB1767859

</td><td>

Server script list actions on Configurable Workspace are executed multiple times when the list has a filter

</td></tr><tr><td>

Demand Management

</td><td>

PRB1770378

</td><td>

The UI action Submit Demand's name causes issues on Automated Test Framework \(ATF\) and the Platform API

</td></tr><tr><td>

Demand Management

</td><td>

PRB1732855

</td><td>

The **Edit** button appears on the 'Idea details' page, but selecting it does not save the content

</td></tr><tr><td>

Demand Management

</td><td>

PRB1754035

</td><td>

The 'Approved Start Date' background color does not change to white until the form is saved

</td></tr><tr><td>

Demand Management

</td><td>

PRB1768990

</td><td>

Activity logs aren't captured when a demand task is created from a workspace

</td></tr><tr><td>

DevOps \(Family\)

</td><td>

PRB1769655

</td><td>

The Performance Analytics job '\[DevOps\] Daily Data Collection' fails due to 'could not execute query'

</td></tr><tr><td>

Discovery

</td><td>

PRB1726066

</td><td>

The vCenter Cloud probe is triggered every time the web server \(http.https\) is determined as open

</td></tr><tr><td>

Discovery

</td><td>

PRB1661511

</td><td>

Metaspace runs out of memory during the transaction /PatternDesignerManager.do

</td></tr><tr><td>

Discovery

</td><td>

PRB1713075

</td><td>

There are no entries in the itom\_lu\_discovery\_mapping table

</td></tr><tr><td>

Discovery

</td><td>

PRB1712133

</td><td>

Large Table Handling \(LTH\) warning in queryPrivAffinity in the business rule 'Insert Discovery Affinity &amp; Cred Aliases' when cmdb.name is null

</td></tr><tr><td>

Discovery

</td><td>

PRB1702370

</td><td>

Cloud Discovery is marked completed after the validate accounts pattern completes

</td></tr><tr><td>

Discovery

</td><td>

PRB1752501

</td><td>

Different certificate checks between VMWareVCenterVMTagsProbe and VMWarevCenterVMsProbec / cVMWarevCenterDatastoresProbe

</td></tr><tr><td>

Discovery

</td><td>

PRB1636480

</td><td>

When manually overriding the '\_getCIs' in deletion scripts, related entries are not cleaned from non-stale CIs

</td></tr><tr><td>

Discovery

</td><td>

PRB1668660

</td><td>

Some discovery pattern logs do not have statuses set if the status returns 'Mixed'

</td></tr><tr><td>

Discovery

</td><td>

PRB1714427

</td><td>

In the existing functions for finding TCP connections, pfiles is not returning a lower number of TCP connections than the number of TCP connections opened in the server

</td></tr><tr><td>

Discovery

</td><td>

PRB1733245

</td><td>

If a virtual machine \(VM\) is converted to a template in vCenter, then discovery creates a new cmdb\_ci\_vmware\_template record and the old VM record isn't marked as retired

</td></tr><tr><td>

Discovery

</td><td>

PRB1736034

</td><td>

Pattern log messages duplicated for multipage payload

</td></tr><tr><td>

Discovery

</td><td>

PRB1742222

</td><td>

The 'Probe to Patterns' migration gets stuck for Windows due to excessive logging when there are many records in the network adapter table

</td></tr><tr><td>

Discovery

</td><td>

PRB1759521

</td><td>

An exception in DiscoveryIDSensor can cause the 'started' count to be incorrect in discovery\_status

</td></tr><tr><td>

Discovery

</td><td>

PRB1611015

</td><td>

SMIStorageServer sensor does not remove or mark stale old storage volumes for storage servers

</td></tr><tr><td>

Discovery

</td><td>

PRB1635588

</td><td>

Error 'Invalid UUID' when creating a new cloud operations schedule using uppercase UUID

</td></tr><tr><td>

Discovery

</td><td>

PRB1686698

</td><td>

Cloud MID selection is not working as expected

</td></tr><tr><td>

Discovery

</td><td>

PRB1701762

</td><td>

Invalid data is being populated in TCP Connections for Unix

</td></tr><tr><td>

Discovery

</td><td>

PRB1706081

</td><td>

When an Agent host is a member of a windows workgroup, FQDN parsing fails and the hostname includes the workgroup name

</td></tr><tr><td>

Discovery

</td><td>

PRB1715437

</td><td>

There's a typo in the process classification 'Nginx'

</td></tr><tr><td>

Discovery

</td><td>

PRB1721760

</td><td>

Non-host items from partial payloads are inserted into discovery\_device\_history

</td></tr><tr><td>

Discovery

</td><td>

PRB1729133

</td><td>

The Solaris Application Dependency Mapping \(ADM\) probe executes part of a commented line as if it were a full command

</td></tr><tr><td>

Discovery

</td><td>

PRB1730011

</td><td>

The snapshot-based delete strategy isn't working well with logical datacenter \(LDC\) batching

</td></tr><tr><td>

Discovery

</td><td>

PRB1731277

</td><td>

If a user has the 'Discovery Admin' role with elevated privileges activated, the 'Cloud Discovery' page isn't loading

</td></tr><tr><td>

Discovery

</td><td>

PRB1732051

</td><td>

FileBasedDiscoverySensor doesn't handle wildCardPaths properly

</td></tr><tr><td>

Discovery

</td><td>

PRB1734170

</td><td>

When a CI has multiple IP addresses and when those IPs are part of different discovery schedules, then the discovery status triggered via the CI 'Discover now' UI related link gets stuck

</td></tr><tr><td>

Discovery

</td><td>

PRB1735766

</td><td>

Application Dependency Mapping \(ADM\) creates a 'Depends on::Used by' relationship to remote address listening on a loopback interface

</td></tr><tr><td>

Discovery

</td><td>

PRB1739753

</td><td>

Credentials-less discovery is not working for AWS Master / Member via MID profile scenario or accessor role scenario

</td></tr><tr><td>

Discovery

</td><td>

PRB1740533

</td><td>

Too many retired VMs can cause a sensor error when processing VMware - vCenter Datacenters

</td></tr><tr><td>

Discovery

</td><td>

PRB1743219

</td><td>

True up Licensing App v3.4.0

</td></tr><tr><td>

Discovery

</td><td>

PRB1755084

</td><td>

SNMP OID records still have a broken reference to a deleted 'Generic Host' classifier

</td></tr><tr><td>

Discovery

</td><td>

PRB1759950

</td><td>

The DiscoveryCloudConfig datacenter 'getter' function does not check if the region it receives IP data from is active, resulting in Shazzam touching IPs which were not intended

</td></tr><tr><td>

Discovery

</td><td>

PRB1761955

</td><td>

Discovery doesn't recover on an SSH socket idle timeout when using Maverick SSH

</td></tr><tr><td>

Discovery

</td><td>

PRB1764379

</td><td>

There's Windows Management Instrumentation \(WMI\) query failures in pattern debugger that carry over to subsequent WMI query steps, affecting debug usability

</td></tr><tr><td>

Discovery Probes and Sensors

</td><td>

PRB1760828

</td><td>

The MID Server script include 'CimQuery' does not work as expected

</td></tr><tr><td>

Document Management

</td><td>

PRB1750158

</td><td>

Workspace document viewer is unable to render PDFs with the content type application/pdf;charset=UTF-8

</td></tr><tr><td>

Document Management Services

</td><td>

PRB1740264

</td><td>

There's an incorrect default sys\_service\_endpoint URL and issues with handling error codes for failed requests properly

</td></tr><tr><td>

Document Management Services

</td><td>

PRB1637082

</td><td>

HTML to PDF generation throws a 'PDFGenerationService: Index 1 out of bounds for length 1' error

</td></tr><tr><td>

Document Management Services

</td><td>

PRB1756312

</td><td>

Related lists should not be exported when glide property is set to false

</td></tr><tr><td>

Document Management Services

</td><td>

PRB1678512

</td><td>

Non-admin users are unable to generate a PDF from HTML

</td></tr><tr><td>

Document Management Services

</td><td>

PRB1757005

</td><td>

Workspace List's PDF export doesn't honor glide.pdf.max\_rows when querying for records for export

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1747952

</td><td>

Document viewer is not showing the document name for jpg and png type files

</td></tr><tr><td>

Edge Encryption

</td><td>

PRB1729586

</td><td>

There's a resource leak in EdgeLatencyAPI

</td></tr><tr><td>

Edge Encryption

</td><td>

PRB1730076

</td><td>

A phantom error is logged from an inappropriate execution of an Edge rule

</td></tr><tr><td>

Edge Encryption

</td><td>

PRB1737568

</td><td>

Edge encryption configurations aren't applied when creating a case within HR Agent's workspace

</td></tr><tr><td>

Edge Encryption

</td><td>

PRB1763202

</td><td>

The long running business rule 'Calculate key status' is triggered multiple times and causes the edge proxy to stall from starting up

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1732389

</td><td>

Translated Notifications are sent in a delay

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1726155

</td><td>

There should be support for Gmail's one-click unsubscribe feature

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1715483

</td><td>

A pagination spinner at the end of a notification is always on

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1723145

</td><td>

In a workspace, selecting 'Reply All' on a received email sets only one of the recipients as 'To:'

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1771175

</td><td>

Post-Washington DC upgrade, an email template isn't applying the **Assigned** field when sending an email

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1715280

</td><td>

Duplicate email IDs are added after selecting 'Reply all' via the email client

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1726824

</td><td>

Email filters run repeatedly

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1730423

</td><td>

If the value of a content-type is a quoted string, emails aren't recognized as e-signed

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1732093

</td><td>

There's a discrepancy in behavior when sending emails to users with turned off email notifications on devices between Service Operations Workspace \(SOW\) and the native workspace UI16

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1746013

</td><td>

Email templates are not available for interview records for an HR case

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1762409

</td><td>

When the **Mandatory** field of a notification is checked, users still do not receive the notification

</td></tr><tr><td>

Embedded Help

</td><td>

PRB1742478

</td><td>

The table in Embedded Help does not display properly in Firefox

</td></tr><tr><td>

Embedded Help

</td><td>

PRB1748376

</td><td>

When changing the arguments to /sp in the Service Catalog module, a 400 error is thrown

</td></tr><tr><td>

Employee Document Management

</td><td>

PRB1764655

</td><td>

The **Move attachment** button is not loading topic details in UI16

</td></tr><tr><td>

Employee Experience Framework

</td><td>

PRB1719474

</td><td>

The path separator of a topic path is missing in Hebrew translations after updating the topic name

</td></tr><tr><td>

Employee Service Center

</td><td>

PRB1738643

</td><td>

Approving Knowledge Articles causes an error, 'Content cannot be associated to the same topic more than once.'

</td></tr><tr><td>

Employee Service Center

</td><td>

PRB1728117

</td><td>

End impersonation does not work as expected on the portal when a user is impersonated from a user with elevated privileges

</td></tr><tr><td>

Employee Service Center

</td><td>

PRB1735683

</td><td>

Knowledge articles favorites are displaying the incorrect version of an article

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB1731660

</td><td>

An error occurs when publishing a knowledge article associated with multiple topics

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB1726526

</td><td>

The 'Connected Content' display value isn't updated when a Catalog Item name changes

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB1739682

</td><td>

Unable to add more than two featured content items after changing the system property taxonomy.content. featured\_content\_limit to 10

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB1755519

</td><td>

Catalog items with no catalog mapping are not filtered by the taxonomy content configuration

</td></tr><tr><td>

Entity View Action Mapper \(EVAM\)

</td><td>

PRB1747238

</td><td>

Now-data-row inner content overflows when the container has a padding or margin

</td></tr><tr><td>

Event Management

</td><td>

PRB1735920

</td><td>

A test connection on pull connectors gives an undefined error

</td></tr><tr><td>

Event Management

</td><td>

PRB1740996

</td><td>

Connectors without debug parameters fail and throw an error that 'isDebug' is not defined

</td></tr><tr><td>

Event Management

</td><td>

PRB1626676

</td><td>

If a payload sent is empty or invalid, a request fails on getting events in the Event Management default rest, which API Add logs don't indicate

</td></tr><tr><td>

Event Management

</td><td>

PRB1674744

</td><td>

Event rule regex designer does not support '\\' character

</td></tr><tr><td>

Event Management

</td><td>

PRB1701487

</td><td>

Conflict between base instance Subflow 'Create Incident' and base instance business rule 'Sync CI with Affected CIs'

</td></tr><tr><td>

Event Management

</td><td>

PRB1712416

</td><td>

The re-opening of an 'Alert' group \(primary alert\) doesn't re-open the related incident in a domain separated instance

</td></tr><tr><td>

Event Management

</td><td>

PRB1719307

</td><td>

An unexpected sys\_ui\_related\_list item is added when users install the Event Management plugin

</td></tr><tr><td>

Event Management

</td><td>

PRB1725183

</td><td>

The 'Priority' tab on the em\_alert table displays the priority to be '0' for certain alerts when glide.system.locale is 'nl.NL'

</td></tr><tr><td>

Event Management

</td><td>

PRB1732558

</td><td>

The 'Insights Explorer' page is found empty after selecting the UI action 'Open in Insight Explorer' on certain alert anomalies

</td></tr><tr><td>

Event Management

</td><td>

PRB1732824

</td><td>

The self health alert isn't created for all duplicate hashes

</td></tr><tr><td>

Event Management

</td><td>

PRB1733215

</td><td>

If priority\_group is part of the filter, Alert Management Rules \(AMR\) doesn't process for some alerts

</td></tr><tr><td>

Event Management

</td><td>

PRB1735071

</td><td>

Memory protections are needed in the 'Connected Business Services' impact calculation

</td></tr><tr><td>

Event Management

</td><td>

PRB1739212

</td><td>

Event binding failure for a node with double spaces

</td></tr><tr><td>

Event Management

</td><td>

PRB1745041

</td><td>

The Service Operation Workspace 'Open alerts' list has inefficient conditions

</td></tr><tr><td>

Event Management

</td><td>

PRB1768322

</td><td>

The short description isn't filled during the creation of virtual alerts for tag-based groups

</td></tr><tr><td>

Event Rules

</td><td>

PRB1688527

</td><td>

The old 'Event Rules' form view should be blocked

</td></tr><tr><td>

File Signature Normalization

</td><td>

PRB1749282

</td><td>

The 'Find Normalization Suggestions' job has an extremely long runtime

</td></tr><tr><td>

Finance Service Management \(Legacy\)

</td><td>

PRB1738329

</td><td>

Base instance UI actions throw an error on domain override on the table 'itfm\_budget\_task'

</td></tr><tr><td>

Financial Management

</td><td>

PRB1743328

</td><td>

An expense line is not generated for all mapped applications

</td></tr><tr><td>

Fixed List Queries

</td><td>

PRB1721024

</td><td>

Users are unable to create a record on a fixed query list

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1744936

</td><td>

The Admin cannot deactivate a read-only flow

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1747210

</td><td>

After upgrading to Washington DC, a new sys\_hub\_snapshot was not created for the 'Create Catalog Task' action

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1731825

</td><td>

SetFlowVariables won't increment if its present loop with a timer is set after that flow logic

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1755867

</td><td>

Saving flow stages is throwing an internal server error

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1713385

</td><td>

Flow Designer action step icons are removed from sys\_attachment after cloning

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1737097

</td><td>

Error in logs 'com.glide.script.RhinoEcmaError: Cannot read property 'length' from null'

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1729404

</td><td>

There's a warning for subflow, PAD, and DATA\_STREAM\_ACTION: 'Flow Element is of unknown category'

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1733023

</td><td>

Flows don't work for catalog items using an 'if' condition with the user input field

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1738138

</td><td>

A sys\_trigger\_runner\_mapping record that's updated and combined with a flow deletion or activation isn't collected by an update set

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1738330

</td><td>

The 'Make Decision' result of order IDs is not displayed with the real values, but rather with a truncated message

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1750937

</td><td>

Flows become read-only when feature access is enabled

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1757305

</td><td>

Errors while trying to use the transform functions of flow designer as a delegated developer

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1757401

</td><td>

Users are unable to get the flow preview when testing with a Flow Designer role

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1698998

</td><td>

Exceptions other than ProcessAutomationException are not being handled

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1713552

</td><td>

The user preference 'showDraftActions' causes an issue and should be removed

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1715010

</td><td>

Repeat triggers aren't functioning as expected

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1723249

</td><td>

The plugin 'com.glide.pad.core.runtime' causes excessive 'Process Automation Event Handler' jobs to be recreated

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1727712

</td><td>

In the flow output, a name isn't auto-populated when users fill in the label

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1731548

</td><td>

A level value isn't entered when a user tests the flow about MetricBase

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1733976

</td><td>

In Flow Designer, users are unable to add REST API headers that have a '-' in it

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1734105

</td><td>

Flow Designer generates warnings when opening

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1736329

</td><td>

A subflow doesn't display completed steps on a nested 'For each' loop

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1736753

</td><td>

Ghost \(non-commented\) GR records are unable pass to subflows

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1742679

</td><td>

For 'Save As JSON, the 'Submit Catalog Item Request' action with a catalog item with variables goes into the waiting state

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1744954

</td><td>

Performance degradation in Dynamic Template when selecting a record on a glide list object

</td></tr><tr><td>

Flow Designer \(Family Channel\)

</td><td>

PRB1716852

</td><td>

The 'Recompile' API uses an outdated snapshot to generate the latest snapshot

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1751604

</td><td>

When creating a change from the playbook 'Playbook for Changes' in CSM Workspace, an error occurs

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1725467

</td><td>

Flow operation view times out due to orphaned sys\_flow\_report\_doc records

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1763738

</td><td>

A 'For-Each' loop under 'Else' terminates prematurely, causing a null point error

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1758414

</td><td>

If the trigger condition's field value is set from another subflow, a flow isn't triggered on the update of a record

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1781775

</td><td>

The FlowCallbackExecutor callback throws a null pointer exception

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1747447

</td><td>

Users observe an issue when async HTTP is called inside a child subflow

</td></tr><tr><td>

Form Controller

</td><td>

PRB1731381

</td><td>

In an issue record page, 'Activity' and 'Setting' sections display as empty

</td></tr><tr><td>

Form Controller

</td><td>

PRB1761801

</td><td>

A page is unresponsive when opening a list that is part of an activity stream in a legacy workspace

</td></tr><tr><td>

Form Designer

</td><td>

PRB1719316

</td><td>

Form Designer can unexpectedly auto-create a label override \(sys\_documentation\) for an extension table when duplicate labels exist

</td></tr><tr><td>

Form Templates

</td><td>

PRB1760565

</td><td>

The 'Undo changes' link on applying a template disappears when a user hovers over it

</td></tr><tr><td>

Form Templates

</td><td>

PRB1739995

</td><td>

Reference Qualifier applies to template\_value.reference in Workspace but not in Platform view

</td></tr><tr><td>

Form Templates

</td><td>

PRB1740403

</td><td>

The **Number** field is populated to edit when creating and applying incident templates from the Service Operations Workspace

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1714230

</td><td>

When using dot walk fields, system logs SEVERE \*\*\* ERROR \*\*\* loadRow failure will be generated

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1738303

</td><td>

Unexpected behavior for **date/time** fields, every update is captured in audit without an old value and the new value is being updated to the same value as before

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1732249

</td><td>

Double escaping occurs and breaks a query when carets and forward slashes are both used

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1736736

</td><td>

GlideRecordSecure.update does not update values when a document ID is dependent on an invalid field

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1762359

</td><td>

GlideRecord get\(\) with an invalid field name returns a record from the target table, even with glide.invalid\_query.returns\_no\_rows enabled

</td></tr><tr><td>

Google Maps OOB integration

</td><td>

PRB1733649

</td><td>

'Map' pages aren't loading for Google Maps API Version 3.55

</td></tr><tr><td>

GraphQL API

</td><td>

PRB1604366

</td><td>

The user is unable to set their preference to dark theme for OSP agent \(snc\_external\)

</td></tr><tr><td>

GraphQL API

</td><td>

PRB1745262

</td><td>

AsyncSerialExecutionStrategy doesn't handle throwables correctly

</td></tr><tr><td>

GRC Platform Plugins

</td><td>

PRB1748143

</td><td>

Adding a related list action doesn't work on a Vancouver instance with new form controller changes

</td></tr><tr><td>

Guided Application Creator

</td><td>

PRB1664046

</td><td>

Issue with '&amp;' character in scope- Example 'Order management for Telecom, Media and Tech'

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1748595

</td><td>

Autolaunch tour doesn't start when the user refreshes the page after the tour is started

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1722731

</td><td>

A guided tour aria-label isn't translated for non-English languages, which causes an issue when using a screen reader

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1726992

</td><td>

Guided Tour steps on the Employee Center header are positioned slightly to the left of the configured location

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1729295

</td><td>

VoiceOver isn't announcing the label for 'Tours' menu items from the primary navigation menu

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1737729

</td><td>

Unable to save settings that the user does not want in the Planning Console Guided Tour

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1770566

</td><td>

Revoking IPKI certificates throws a JS error

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1734239

</td><td>

In a replication set with fully activated producer and consumer, not all records are replicated and seeding becomes stuck with a stack trace

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1748050

</td><td>

Hermes is installed but not configured

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1755317

</td><td>

Topic Inspector fails to load consumer group info when 'subscribe by pattern' is used in consumer client

</td></tr><tr><td>

Hierarchical Lists

</td><td>

PRB1603968

</td><td>

Concatenated strings cause grammatical errors in Japanese

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1663860

</td><td>

Typing in a long compose text field causes a scroll to the top

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1733120

</td><td>

The 'Customer activity' page loads slowly in a workspace

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1727953

</td><td>

A workspace page sticks when trying to move from 'Home' to 'List' on the landing page

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1740271

</td><td>

Service Operation Workspace navigation icon tabs do not have a visible focus indicator

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1750876

</td><td>

The UI Builder 'Date-time' component partially displays data in the system's preferred language, but not in the user's preferred language

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

</td><td>

PRB1745441

</td><td>

Input comments are cleared when adding an attachment in the CSM ticket page

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

</td><td>

PRB1765258

</td><td>

A list name can't be updated properly via the 'My list filters' widget when the data load time exceeds 1000 milliseconds under 'csm\_my\_lists' page

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1772519

</td><td>

After upgrading to Vancouver, COE Security has different behavior

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1726178

</td><td>

The selection box for HR PDF templates isn't working when on the 'Mark Signature Blocks' page

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1726645

</td><td>

When creating a new Evidence record the **Parent** field is set to 'Empty' and is not auto-populating

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1734098

</td><td>

The **rich\_description** field destroys the table structure when submitting any item from the portal

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1710767

</td><td>

The dynamic filter 'One of My Assignments' doesn't work with a Granular Delegation

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1718216

</td><td>

Playbook's activity order isn't working in Agent Workspace

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1725924

</td><td>

An HR Task Description is not populated after marking the HR Checklist task type as Completed

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1733328

</td><td>

The sn\_hr\_core.impersonateCheck property impacts scheduled reports

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1739141

</td><td>

The Summary Report UI action is using hardcoded pdfName and cannot overwrite it because ERDocTemplatesUtils is read-only

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1744663

</td><td>

Bulk Case Creation is stuck after updating a user segment more than twice

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1748144

</td><td>

Images pasted in Rich description of the HR Case during case creation appear as broken images to the user

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1757704

</td><td>

The **Topic Detail** and **Topic Category** fields are not auto populating after selecting HR service

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1702511

</td><td>

The **rich\_description** field is truncated if the '^' sign or '=' sign is added to the field in HR scope

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1704171

</td><td>

There's a client-side issue on an HR task 'Form' page when selecting the HR task type

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1707722

</td><td>

In the 'Glance' view, the office location isn't updated when sn\_hr\_core\_profile is created

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1709857

</td><td>

An error message not translated for the setAbortAction method in the business rule

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1714909

</td><td>

There's an issue with the 'Resubmit Approvals' UI action

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1722548

</td><td>

A user with the sn\_hr\_core.manager role is unable to mark signatures in an HR PDF template

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1728268

</td><td>

Archiving HR records is removing the attachments, causing even admin users to not be able to see the attachment on archive HR records

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1730983

</td><td>

The **COE** field in HR Agent Workspace is highlighted in red even though it's been populated with a value

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1734937

</td><td>

Attachments aren't copied to an HR case from a chat

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1735207

</td><td>

Some script includes in Human Resources have a core scope without a caller restriction

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1736121

</td><td>

HR Employee Relations \(ER\) admins aren't able to add or update the **Collaborator** field on an HR ER case

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1739949

</td><td>

Employee Relations has broken UI action behaviors

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1739950

</td><td>

When creating an employee document in HR Agent Workspace, HR agents are presented all user profiles for a given name rather than just user profiles that have an associated HR profile

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1739969

</td><td>

The Employee Relations case table is not auto-populated on the evidence form

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1741522

</td><td>

The hr\_Utils.\_cancelRequestedItems API may incorrectly update records with an empty parent

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1743184

</td><td>

Once the attachment is uploaded for some documents, the document owner admin user is not able to view or download the uploaded document

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1744431

</td><td>

The 'Before Update' business rule addInfoMessage\(\) appears twice in HR Agent Workspace

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1744978

</td><td>

Slowness when trying to open requests in a new tab in the portal

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1753439

</td><td>

Internal server error 500 on HR Agent Workspace when the user cannot view the **opened\_at** field on HR cases

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1755082

</td><td>

Missing translation for error messages

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1757799

</td><td>

'Suspend Reason' displays choices from children tables \(other COEs\)

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1759013

</td><td>

Data policy exception on the close notes field occurring in workspace

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1781562

</td><td>

Unable to update the 'interaction.state' ACL

</td></tr><tr><td>

HR Service Delivery Case Management

</td><td>

PRB1633415

</td><td>

HR Case header details don't display or are empty when loaded

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1712418

</td><td>

If it contains a list field with no set value, a response template displays as empty

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1732550

</td><td>

NQ issue in the activity set trigger conditions, causing the conditions to fail

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1738109

</td><td>

Bulk banner and functionality do not work as expected when the Delegation plugin is active

</td></tr><tr><td>

HTML Editor

</td><td>

PRB1727046

</td><td>

If the glide.html.enable \_media\_sites system property has a line break, then all the HTML fields break

</td></tr><tr><td>

HTML Editor

</td><td>

PRB1728095

</td><td>

The JAWS edit box list displays '\{​\{textarea\}\} Edit undefined' as an **Edit** field item

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1761702

</td><td>

If className and sys\_class\_name are different for a payload item, IRE should use the className value for both

</td></tr><tr><td>

Identity

</td><td>

PRB1722897

</td><td>

Checking for a user by federated ID when the ID is null results in a large query that returns hundreds of thousands of rows

</td></tr><tr><td>

Identity

</td><td>

PRB1739422

</td><td>

The 'Save' UI action on the form context menu no longer appears when the com.snc.integration.scim2.client plugin is installed

</td></tr><tr><td>

Identity

</td><td>

PRB1744985

</td><td>

A time-limited user role assignment should be restricted for licensing compliance

</td></tr><tr><td>

Inbound Email Actions

</td><td>

PRB1720030

</td><td>

The inbound actions 'Update Incident' and 'Update Incident \(BP\)' use the ITIL role instead of the ITSM/CMDB fine-grained roles

</td></tr><tr><td>

Incident Communications Management

</td><td>

PRB1751178

</td><td>

Errors in logs for using 'instanceof' for ConferenceParticipantsTCM0

</td></tr><tr><td>

Incident Communications Management

</td><td>

PRB1744121

</td><td>

The **Compose** button isn't working on an incident communication task and workbench

</td></tr><tr><td>

Incident Management

</td><td>

PRB1670366

</td><td>

'Show other active tasks' and 'UI Macro Right click to open menu' are non-functional on an incident form

</td></tr><tr><td>

Incident Management

</td><td>

PRB1775234

</td><td>

Post-Washington DC upgrade, the **Proposed By** field isn't populated on major incidents

</td></tr><tr><td>

Innovation Management

</td><td>

PRB1692413

</td><td>

The 'Idea' portal's search field doesn't have sufficient contrast against the background color

</td></tr><tr><td>

Install Base Management

</td><td>

PRB1764835

</td><td>

When the Install Base plugin is not installed and Customer service plugin is installed, there is an error Unknown field install\_base in table sn\_customerservice\_case

</td></tr><tr><td>

Install Base Management

</td><td>

PRB1731646

</td><td>

A field referencing the sn\_install\_ base\_sold\_product table is slow to load due to the 'SoldProductFilter' script include

</td></tr><tr><td>

Install Base Management

</td><td>

PRB1746144

</td><td>

'isLoggedinUserValidConsumer' in the script include 'SoldProductAndInstallBaseFilterSNC' causes a significant volume of errors

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1679559

</td><td>

IDR Diagnostics indicates malfunction when legacy components are working

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1684566

</td><td>

IDR Replication is working properly, but IDR Diagnostics shows a malfunction in Root Chain Management

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1736093

</td><td>

The **Track in Update Set** button doesn't add transformations to the update set

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1684672

</td><td>

Replication sets are not easily recreated

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1721515

</td><td>

In Instance Data Replication \(IDR\), reevaluate the replication of sys\_ fields and 'Preserve Modified By'

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1725366

</td><td>

There's a StackOverflowError initializing ScopedReplicationEntryInspector \(IDRReplicationEntryInspector\)

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1745789

</td><td>

Instance Data Replication \(IDR\) Record Transformer must be clear when it's in a draft state

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1754363

</td><td>

Users are unable to add a filter to a partial seeding request with only the idr\_admin role

</td></tr><tr><td>

Instance Scan

</td><td>

PRB1733963

</td><td>

The **Run As** field shouldn't be present on Instance Scan 'Schedule' forms

</td></tr><tr><td>

Integration Authentication

</td><td>

PRB1742161

</td><td>

A download request fails due to a possible credential error

</td></tr><tr><td>

Integration Authentication

</td><td>

PRB1766086

</td><td>

The history policy rule isn't visible on the 'login\_cpw' page in case of an advanced password policy

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1681003

</td><td>

The user observes an error due to MID-to-instance communication overload

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1710047

</td><td>

A REST step is appending charset=UTF-8 to the content type

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1668651

</td><td>

Retry Policies for Connection Timeout don't work over HTTPS

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1690294

</td><td>

Usages are being created with the Artifact Name = 'Unknown'

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1720896

</td><td>

JDBC connection throws the error 'Invalid connection parameter name allowLocalInfile' for DataBricks source

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1730794

</td><td>

The PowerShellUtils class throws a parsing error with strings containing a backslash

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1682415

</td><td>

The family plugin com.glide.hub .integrations.professional depends on a store application

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1736348

</td><td>

Mid plan saving can cause double gzipping

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1740218

</td><td>

IntegrationHubStatsCollector can't be turned off

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1744483

</td><td>

The REST step 'Save As Attachment' is not working as expected

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1757262

</td><td>

Flow Designer fails with the error 'Size of the rows retrieved exceeded maximum payload' in the JDBC step

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1764212

</td><td>

Not able to fetch operation for specs that contain 'anyof' and 'Oneof'

</td></tr><tr><td>

Integration Hub - Import

</td><td>

PRB1710992

</td><td>

The script to clean orphan rows from sys\_import\_set\_row doesn't work for the generic version of the cleaner

</td></tr><tr><td>

Integration Hub Stream Connect

</td><td>

PRB1740633

</td><td>

Partition groups get stuck with a 'LOCKED' owner

</td></tr><tr><td>

Interactive Filters

</td><td>

PRB1728220

</td><td>

Choice list interactive filter widget controls have insufficient accessible names and the associated input has no visible label

</td></tr><tr><td>

Interactive Filters

</td><td>

PRB1728601

</td><td>

A non-admin user isn't able to save the element of a breakdown source on a legacy dashboard

</td></tr><tr><td>

Interactive Filters

</td><td>

PRB1730182

</td><td>

Choices defined for inherited choice fields don't display in Platform Analytics' dashboard filters

</td></tr><tr><td>

Internationalization Features

</td><td>

PRB1618316

</td><td>

**day\_of\_week** field type options are no longer translated and required sys\_translation records are no longer loaded on plugin activation

</td></tr><tr><td>

Journal Field Types

</td><td>

PRB1716022

</td><td>

setJournalEntry isn't working correctly and displays the logged in user's name in the activity stream when a work note is updated from a background script

</td></tr><tr><td>

JVM at Scale

</td><td>

PRB1734899

</td><td>

There's significant memory consumed in a table descriptor cache from an online table alter

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1716042

</td><td>

Adhoc Key Exchange is successful with the incorrect status 'Error on Local Instance' on target

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1735756

</td><td>

Diagnostics indicate a certificate may not be valid or doesn't exist

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1737448

</td><td>

Business rule shows sys\_updated\_on in the year 2025, when the current year is 2024

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1692981

</td><td>

Modules that have multiple active keys need to be deactivated

</td></tr><tr><td>

Knowledge Article Templates

</td><td>

PRB1762185

</td><td>

The exact match shows the sys ID of the record as the title for the kb\_template\_how\_to record \(Zing search\)

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1711281

</td><td>

Changes to ts\_query\_kb acl after Vancouver

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1712553

</td><td>

The UI page kb\_translation\_ language\_picker doesn't show more than 14 languages

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1742967

</td><td>

ViewAs articles are skipped as the manager doesn't have access

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1474932

</td><td>

HTML field \(tinyMCE\) margin / border / padding / styling is not applied on the View article and / or the Service Portal KB view page

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1695323

</td><td>

Issue with KB article which does not show bold text when published

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1719166

</td><td>

User criteria isn't working as expected

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1732162

</td><td>

There's a 'File parsing error' message when importing document files with tables

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1749371

</td><td>

Issues with enabling 'I18N: Knowledge Management Internationalization Plugin v2'

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1756423

</td><td>

Knowledge feedback worknotes \(kb\_feedback\) are not allowed for a knowledge\_manager role when write access is allowed

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1711960

</td><td>

If the text size is the same as the default font size, then no font size is applied to the text

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1715178

</td><td>

When performing user diagnostic criteria in a domain-separation enabled instance, an impersonation causes the last login time to be updated

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1715184

</td><td>

In knowledge keywords, the **New** button is missing

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1717344

</td><td>

When the glide.ITIL.assign. number.on.insert property is set to true and an article is created in the Word add-in, the article is in a 'Draft' state

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1718153

</td><td>

The text 'Most Viewed' and 'Most Useful' are defined as heading level 3 \(h3\) in the main content area

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1725593

</td><td>

The 'Knowledge Field Facet' widget doesn't work as expected

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1731351

</td><td>

There's a performance issue with the Knowledge API with 100 articles per batch

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1732303

</td><td>

In Manager Hub, searching as an employee isn't displaying the expected results/knowledge article

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1738540

</td><td>

Console errors are displayed when a user selects the comments box in a Knowledge Base page

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1742810

</td><td>

Confusing handling of the comment toolbar

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1745009

</td><td>

The 'Most Useful' and 'Most Viewed' Service Portal widgets show KB articles from other knowledge bases

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1753662

</td><td>

Knowledge articles do not show the reference in the Virtual Agent

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1767594

</td><td>

Users are unable to set the default sort order on the 'Knowledge Result Sort' widget

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1771819

</td><td>

Knowledge clustering solutions are erroring out

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1615848

</td><td>

There are bugs in the Finnish translation after the Tokyo upgrade

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1730863

</td><td>

Portfolio Planning's workspace's **Currency** field abbreviation isn't working in non-English languages

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1739340

</td><td>

The Japanese translation for 'second' is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1759621

</td><td>

The Japanese translation for 'on' is incorrect in the condition builder

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1728997

</td><td>

sys\_choice of priority field has different separators

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1657482

</td><td>

Incorrect Japanese translation of 'Purchased' in the sys\_documentation table

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1727009

</td><td>

The translation for the word 'Cancel' in French Canada \(FQ\) language has been changed from 'annuler' in Utah to 'interrompre' in Vancouver

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1747254

</td><td>

The French translation of label text is incorrect for the sys\_choice record for the change\_task record state field value 1

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1675927

</td><td>

The Dutch Translation for the **Short Description** field label is incorrect/truncated since Tokyo

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1682554

</td><td>

The Japanese translation of Table='alm\_asset' and Element='sys\_created\_on' in sys\_documentation table is incorrect after installing the com.sn\_samp\_master plugin

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1693537

</td><td>

The German translation of 'Subject Person' is wrong and different from the rest of the platform when added to the 'At a glance' section of HR Agent Workspace

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1701662

</td><td>

Incorrect French Walk-Up Experience translation for the key 'calendar\_day\_wednesday\_2char'

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1701786

</td><td>

The Spanish translation of state field is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1709514

</td><td>

A date translation is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1731619

</td><td>

The info message on a UI action isn't translated

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1731846

</td><td>

When using the Dutch language, there's a typo in Employee Center

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1740163

</td><td>

The German translation for 'users' is incorrectly set to 'gruppen' instead of 'benutzer' in the navigator under 'Benutzeradministration,' 'System Security,' and 'Organization' in Vancouver

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1752932

</td><td>

The Japanese translation of 'view' is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1769645

</td><td>

Japanese translation of Key='new tab \{0\}' in sys\_ui\_message table displays in French

</td></tr><tr><td>

LDAP integration

</td><td>

PRB1732031

</td><td>

LDAP Listener doesn't transform the changes when multiple organizational unit definitions share the same relative distinguished name under the same LDAP server for the same target table

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1512256

</td><td>

The **glide\_list** field with choices and an empty reference table is not working

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1757927

</td><td>

Email pages only display the value instead of displayValue for created\_on information

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1686676

</td><td>

A Related List record always shows 20 when the system property 'glide.ui.fetch.list.record .count.asynchronously' is set to true

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1740656

</td><td>

User observes a 'Loading last reply...' while viewing an email in the activity stream

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1689053

</td><td>

Form graphql request provides the incorrect value for **datetime** fields

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1719776

</td><td>

A field isn't expanding all the way in a workspace

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1736226

</td><td>

In Agent Workspace, the activity stream displays backend names instead of label names for custom fields

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1737483

</td><td>

In Service Operations Workspace, email addresses added to the watch list when a non-email user is already on the list are updated to the previous user's name

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1739512

</td><td>

The subject in the email client template truncates a space after using ','

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1756344

</td><td>

Text within multiline fields appears behind section headers in workspaces

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB1769340

</td><td>

ServiceNow keyboard shortcuts are interfering with browser shortcuts in Washington DC in the Norwegian language

</td></tr><tr><td>

Legacy Workflow

</td><td>

PRB1736438

</td><td>

Checking the workflow property updates sys\_updated\_xxx fields

</td></tr><tr><td>

License Usage

</td><td>

PRB1725703

</td><td>

After upgrading to Vancouver, the Software Asset Management \(SAM\) Pro 'Software model' page \(i\) doesn't open

</td></tr><tr><td>

License Usage

</td><td>

PRB1717748

</td><td>

In Software Asset Workspace, the 'Top 5 publishers true-up cost' widget locks the filter on the 'Publishers' view on the 'License usage' tab

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1731097

</td><td>

Skipped activity sets are cancelled when closing LE case

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1726402

</td><td>

An 'Employee' form isn't completed when the form is created in the Lifecycle Enterprise scope, even if it says it's been submitted

</td></tr><tr><td>

List Administration

</td><td>

PRB1737130

</td><td>

Grouping by the 'Tags' column isn't working on the sc\_req\_item table

</td></tr><tr><td>

List Administration

</td><td>

PRB1771202

</td><td>

'Put line breaks in lists' is broken in the Washington DC release

</td></tr><tr><td>

List Administration

</td><td>

PRB1778664

</td><td>

In a workspace list, an error is thrown even though there's no issue: 'rows removed from this list by security constraints'

</td></tr><tr><td>

List Administration

</td><td>

PRB1686235

</td><td>

Pagination in a form can be broken for database view

</td></tr><tr><td>

List Administration

</td><td>

PRB1713911

</td><td>

When the **DateTime** field is set as display = true, it doesn't reflect the user's time zone

</td></tr><tr><td>

List Administration

</td><td>

PRB1717255

</td><td>

The **View All** button isn't displaying in Platform Analytics Workspace's dashboard

</td></tr><tr><td>

List Administration

</td><td>

PRB1718119

</td><td>

The Workspace 'OR all of these conditions must be met' condition in sys\_ux\_my\_list causes the 'Show All' function to break after sorting the list

</td></tr><tr><td>

List Administration

</td><td>

PRB1722284

</td><td>

Users are unable to hide the list actions using the 'Hide List Action' check box

</td></tr><tr><td>

List Administration

</td><td>

PRB1732838

</td><td>

When selecting records across all pages, NRLC and 'Presentation List' display 0 records

</td></tr><tr><td>

List Administration

</td><td>

PRB1735047

</td><td>

The filter icon shows '1' when there is no filter defined

</td></tr><tr><td>

List Administration

</td><td>

PRB1735472

</td><td>

A related list doesn't function when the 'Applies To' table in the relationship record is in a database view

</td></tr><tr><td>

List Administration

</td><td>

PRB1661521

</td><td>

A keyboard's focus moves outside the filter dialog when using the tab and shift-tab keys

</td></tr><tr><td>

List Administration

</td><td>

PRB1672117

</td><td>

The screen reader \(NVDA\) doesn't announce the state as 'Expanded/Collapsed' after invoking the column headers more options list

</td></tr><tr><td>

List Administration

</td><td>

PRB1685955

</td><td>

During reordering of 'My Lists', the 'Lists' section displays as empty after selection

</td></tr><tr><td>

List Administration

</td><td>

PRB1710753

</td><td>

Choices on a filter in a new added related list 'User Incidents' are not fully shown in the first loading

</td></tr><tr><td>

List Administration

</td><td>

PRB1716453

</td><td>

The selection indicator of a selected pagination link doesn't meet the required contrast ratio

</td></tr><tr><td>

List Administration

</td><td>

PRB1723111

</td><td>

A screen reader isn't announcing the table's information after applying a filter on the table

</td></tr><tr><td>

List Administration

</td><td>

PRB1726472

</td><td>

The URL is changed when the **Refresh list** button is selected in the list from Agent Workspace, and the list isn't displaying

</td></tr><tr><td>

List Administration

</td><td>

PRB1731560

</td><td>

When performing **Workspace Lists** &gt; **Filter** &gt; **Restore Defaults**, the focus doesn't return to the **Filter** button

</td></tr><tr><td>

List Administration

</td><td>

PRB1732648

</td><td>

Characters are missing when list editing the **Tags** field in a configurable workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB1732961

</td><td>

The 'List' view in a workspace isn't displaying correct content

</td></tr><tr><td>

List Administration

</td><td>

PRB1733901

</td><td>

Navigate to/search a query on a **Number** field unexpectedly does a 'greater than' query after rollover when a new digit is needed

</td></tr><tr><td>

List Administration

</td><td>

PRB1735866

</td><td>

Pagination for grouped lists in Workspace does not work correctly

</td></tr><tr><td>

List Administration

</td><td>

PRB1736123

</td><td>

When list editing a reference field from a workspace/Software Operations Workspace \(SOW\), the pop-up modal is closed unexpectedly after applying a filter

</td></tr><tr><td>

List Administration

</td><td>

PRB1736837

</td><td>

In workspace, when a dictionary record is inactive and has a **Dependent on** field, this field still shows in the in-line list edit

</td></tr><tr><td>

List Administration

</td><td>

PRB1743222

</td><td>

Screen reader users aren't given any confirmation when a user selects a menu item form from the filter menu

</td></tr><tr><td>

List Administration

</td><td>

PRB1750095

</td><td>

In a configurable workspace, when a choice field is added in the child table, the filter on the field of the list view does not show the choice field values

</td></tr><tr><td>

List Administration

</td><td>

PRB1751256

</td><td>

When using 'Group by' with the UI in Hebrew, the names are aligned to the left and the arrows to the right

</td></tr><tr><td>

List Administration

</td><td>

PRB1751324

</td><td>

The 'Select All' check-box is not translated when using screen readers

</td></tr><tr><td>

List Administration

</td><td>

PRB1752118

</td><td>

List layouts in sub-domains do not inherit the list layout from parent domains and create entries in the sys\_ui\_list table when opening a report

</td></tr><tr><td>

List Administration

</td><td>

PRB1767453

</td><td>

The 'Group by' tags list view count is not accurate

</td></tr><tr><td>

List Administration

</td><td>

PRB1783350

</td><td>

In Service Operations Workspace, header info isn't announced for the **Cell Filter** button when navigating in a list

</td></tr><tr><td>

List Administration

</td><td>

PRB1735539

</td><td>

The presentation list Highlighted Value field and Tag field are not updated after inline editing needs a refresh

</td></tr><tr><td>

List Editor

</td><td>

PRB1719428

</td><td>

Selecting a reference value on a list of drafts doesn't redirect the user and leads to an error

</td></tr><tr><td>

List Editor

</td><td>

PRB1720036

</td><td>

The keyboard focus isn't staying on the pagination buttons after invoking them

</td></tr><tr><td>

List Filters

</td><td>

PRB1731003

</td><td>

In List view in case of multiple filters applied, the calendar moves from its correct placement to a blank space and the filter button disappears

</td></tr><tr><td>

List Filters

</td><td>

PRB1716029

</td><td>

The translation of dynamic filters in a configurable workspace isn't working

</td></tr><tr><td>

List Filters

</td><td>

PRB1730190

</td><td>

**List - Close Filter** buttons don't specify which filter is cleared

</td></tr><tr><td>

Live Feed

</td><td>

PRB1655252

</td><td>

An @-mention causes a user to switch domains

</td></tr><tr><td>

Localization Framework

</td><td>

PRB1750438

</td><td>

Auto-translate and auto-publish does not work as expected in the XTM Translation spoke

</td></tr><tr><td>

Localization Framework

</td><td>

PRB1755925

</td><td>

Virtual Agent topics are not translated, even though the topic translation is present within the sys\_translated\_text table

</td></tr><tr><td>

Machine Learning APIs

</td><td>

PRB1763422

</td><td>

One of the machine learning definitions 'Change Risk' solutions gives the error 'Error while training solution' when it is trained in upgraded environments

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1717798

</td><td>

The script include 'MIMListActionsUtil' uses the ITIL role instead of the ITSM/CMDB fine-grained roles or using a combined condition

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1720379

</td><td>

The object UI page 'workbench' uses the ITIL role instead of the ITSM/CMDB fine-grained roles or using a combined condition

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1726280

</td><td>

Major Incident Workbench communication's required field '\*' displays as grey instead of red

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1745580

</td><td>

The 'getMIMWorkbenchUrl' email script redirects to the old workbench

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB1768365

</td><td>

**Post-incident Report \(PIR\)** fields aren't behaving properly when the 'Before Insert' business rule is applied on an incident table

</td></tr><tr><td>

Managed Documents

</td><td>

PRB1774735

</td><td>

Focus isn't working as expected on dialog boxes in managed documents

</td></tr><tr><td>

Memory: Heap Space

</td><td>

PRB1751913

</td><td>

PDF generation causes memory issues on multiple nodes of the instance

</td></tr><tr><td>

Metric Intelligence \(Family\)

</td><td>

PRB1742956

</td><td>

On the 'Metrics view' configuration table, there's a business rule that prevents editing when there's no active series for those metric types

</td></tr><tr><td>

Metric Intelligence \(Family\)

</td><td>

PRB1728798

</td><td>

In the 'Metrics' view configuration, users can't choose the CI type

</td></tr><tr><td>

Metrics

</td><td>

PRB1712256

</td><td>

The job 'Metric update events process' triggers the query with a hash that performs UNION ALL on all sys\_audit shards

</td></tr><tr><td>

Microsoft Reconciliation

</td><td>

PRB1715614

</td><td>

Allocated devices with non-licensable installs shouldn't cause StackOverflow exceptions

</td></tr><tr><td>

Microsoft Reconciliation

</td><td>

PRB1728883

</td><td>

A product result for an install isn't stamped

</td></tr><tr><td>

MID Server

</td><td>

PRB1710037

</td><td>

If the MID Server gives up waiting for the Upgrade process to start, but it does eventually start, binaries are deleted and the MID Server stays down

</td></tr><tr><td>

MID Server

</td><td>

PRB1759604

</td><td>

ECCSender gets stuck in a loop sending size 0 files

</td></tr><tr><td>

MID Server

</td><td>

PRB1730670

</td><td>

The error level of the message for an App Engine Studio \(AES\) failed decrypt should be lowered

</td></tr><tr><td>

MID Server

</td><td>

PRB1729573

</td><td>

MID clears out encryption keys early during the shutdown process while probes are still running

</td></tr><tr><td>

MID Server

</td><td>

PRB1732428

</td><td>

MID disconnects agents on a null pointer exception

</td></tr><tr><td>

MID Server

</td><td>

PRB1717409

</td><td>

Discovery with Cyberark integration doesn't work when Amazon Web Services' \(AWS\) access key ID and password rotates

</td></tr><tr><td>

MID Server

</td><td>

PRB1725231

</td><td>

MID server's TrustStore migration fails when the same certificate had been added twice, causing integration outages

</td></tr><tr><td>

MID Server

</td><td>

PRB1746470

</td><td>

The Online Certificate Status Protocol \(OCSP\) revocation check is failed on endpoints, even after adding complete certificates in trust store/cacerts

</td></tr><tr><td>

MID Server

</td><td>

PRB1757421

</td><td>

If a file is locked in the first attempt and released in the next, backup can't be executed

</td></tr><tr><td>

MID Server

</td><td>

PRB1707413

</td><td>

There are two parameters related to ACC-F on MID that require a restart in case of update

</td></tr><tr><td>

MID Server

</td><td>

PRB1710122

</td><td>

AWS Credentialless discovery fails with the Pattern plugin v1.8

</td></tr><tr><td>

MID Server

</td><td>

PRB1715027

</td><td>

Updating the config.xml for CyberArk produces a red bar message since Utah

</td></tr><tr><td>

MID Server

</td><td>

PRB1728569

</td><td>

MID server restarts during discoveries when 'mTLS' is configured

</td></tr><tr><td>

MID Server

</td><td>

PRB1743685

</td><td>

There's a failure during key exchange, as SNCSSH doesn't support ED25519

</td></tr><tr><td>

MID Server

</td><td>

PRB1749975

</td><td>

Unable to install a MID Server using a group Managed Service Account \(gMSA\) with Windows installer

</td></tr><tr><td>

MID Server

</td><td>

PRB1750910

</td><td>

Uploading two MID Server JAR Files with the same name causes an endless loop of file deletion and replacement, resulting in all MID Servers going offline on Windows

</td></tr><tr><td>

MID Server

</td><td>

PRB1757228

</td><td>

In the MID Server, records are generated without a MID Server assigned

</td></tr><tr><td>

MID Server

</td><td>

PRB1758560

</td><td>

Containerized MID Server does not come back up after being re-instantiated by Kubernetes

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1693840

</td><td>

A parameterized screen with an input of type reference does not load the reference list

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1717693

</td><td>

The 'Unassigned Incidents' list applet isn't loading in the Agent Mobile app

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1728314

</td><td>

In the 'Questionnaires' survey, the boolean type variable isn't working in Mobile

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1736727

</td><td>

Mobile Agent app displays only the notifications and the 'Settings' tab if a custom value is set in the glide.sys.default.tz property

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1763577

</td><td>

For mobile publishing, assetlinks.json files for ServiceNow instances should be supported

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1640755

</td><td>

Filtering list screen records in offline mode doesn't find all relevant records

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1673307

</td><td>

Improve screen dependency to add necessary input variable param map only

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1711983

</td><td>

The 'Mobile Colors Default' UX style is created in the global scope and is thus editable

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1714394

</td><td>

There's a walk-up appointment error when changing a slot on the Now Mobile app

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1716091

</td><td>

An empty page ID occurs when the input form screen's 'Advanced' is off because each input is passed as its own page/section without adding the ID to the page

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1721387

</td><td>

An input form screen's list displays choices from child tables instead of just the records table, which is different from the platform's behavior

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1721417

</td><td>

Users are unable to edit in the script editor on the sys\_sg\_write\_ back\_action\_step table

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1733689

</td><td>

A misconfigured sys\_sg\_screen\_field causes the mobile app to not load

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1734915

</td><td>

The 'SG Media' section text is truncated when its more than 255 characters due to the sys\_translated character limit

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1737086

</td><td>

Offline mode does not work on the Agent app due to misconfiguration of the **sys\_sg\_input** field, leading to a null pointer exception and inability to configure the offline payload

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1739817

</td><td>

The GPS coordinates variable is always empty when used in a Mobile UI rule condition

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1739867

</td><td>

The user can't flag a Knowledge Base article when on an iOS browser

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1742032

</td><td>

The Mobile calendar shows the day of the PTO start date on the day before for both iOS and Android

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1742243

</td><td>

For a reference field, the 'starts with' condition does not work as expected

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1744438

</td><td>

Using the 'Image in Icon' section for an applet makes it appear distorted, even using the base instance recommended dimensions

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1747793

</td><td>

The item list for a scripted data item or declarative data item with a parameter is not ordered

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1762289

</td><td>

Mobile client script 'genAIUtils.ts' causes a mobile UI rules failure

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1774419

</td><td>

There's a problem with the autofill multi-select input parameter

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB1734747

</td><td>

Users are unable to log in using FIDO when the multi-factor authentication 'Remember browser' feature is turned off

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB1740829

</td><td>

The 'Continue' button shown in /validate\_multifactor\_ auth\_code.do is not translated

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB1753034

</td><td>

Authentication Bypass in Multi-factor Authentication \(MFA\)

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB1755019

</td><td>

When logging in again after a timeout occurs, the system redirects to the MFA setup page '/multi\_factor\_ auth\_setup\_page.do'

</td></tr><tr><td>

Next Experience Center Pill

</td><td>

PRB1731562

</td><td>

The buttons from the 'Remove favorite' modal don't have accessible names

</td></tr><tr><td>

Next Experience History Menu

</td><td>

PRB1743762

</td><td>

When navigating to the 'History' tab and opening it, all elements in the list are read out with all information as part of the element's name when using assistive technologies like JAWS

</td></tr><tr><td>

Next Experience Landing Page

</td><td>

PRB1744537

</td><td>

Upon landing on '/now/nav/ui/home', all section headings except the main heading 'Review your work' are implemented as &lt;h3&gt;, although some of them are nested both visually and semantically

</td></tr><tr><td>

Next Experience UI16 Theming

</td><td>

PRB1743437

</td><td>

In the de-duplication task remediation action window, the **Next** button does not honor Next Experience styling

</td></tr><tr><td>

Next Experience UI16 Theming

</td><td>

PRB1751904

</td><td>

Journal list fields are not styled properly in the Next Experience UI

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1720035

</td><td>

The 'Cancel' pop-up isn't visible for long-running transactions

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1755359

</td><td>

Application Pill does not show the complete table name in a Washington DC release even when the screen is zoomed out

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1706807

</td><td>

A customized company logo is not reflected on the Identity Center page when using UI16

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1743909

</td><td>

There's a trailing space in sys\_app\_module records that cause a 500 error on Next Experience

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1629109

</td><td>

The global search results page is not language translated when using Next Experience

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1712674

</td><td>

Next Experience UI with 'Always show top navigation' on has an issue with custom URLs

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1754311

</td><td>

The 'No records to display' image is missing on Washington instances

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1597183

</td><td>

An unexpected module remains highlighted in the navigator after selecting

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1709822

</td><td>

Next Experience Dark theme causes the **Activities \(filtered\)** field text to be unreadable when the property 'glide.ui16.live\_forms.enabled' is set to 'false'

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1723742

</td><td>

In Next Experience UI, the recipient field highlight is missing in the Vancouver release

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1728207

</td><td>

The Next Experience landing page load spams the system logs with an error

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1740454

</td><td>

Selecting the **Back** button from the search screen that reads 'Service operations Workspace' creates a new interaction or incident

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1752326

</td><td>

When 'te%t' entered into the Global search from Platform the relevant results returned, but selecting 'Go to list view' shows a blank page

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1754198

</td><td>

After impersonating any user and hovering on the user's icon, there's no tooltip that displays the complete user name

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1630109

</td><td>

Remove the 'Configure Page' option from user's profile menu pop-up

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1671182

</td><td>

A user with the role 'sn\_cmp.cloud\_root\_admin' is able to configure a business rule even with errors displayed on top of records

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1709513

</td><td>

The glide.ui.polaris. login.logo.height isn't working for the percentage value

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1709841

</td><td>

Editing multiple records in a list does not highlight the selected cells when using List v3 on Vancouver

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1715543

</td><td>

List markup in the header section is missing contents that are present in the navigation bar, such as 'All', 'Favorites', 'History', and so on

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1715894

</td><td>

In the top navigation, a separator is announced by the screen reader

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1718433

</td><td>

NVDA isn't announcing the header of the modal that appears after invoking the **Open Preview** button

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1722728

</td><td>

Notifications can be from different sources, but the same target is de-duped

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1727925

</td><td>

When using Next Experience, the context picker 'Globe' icon in the header isn't visible for a non-admin user with multiple encryption module access

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1729720

</td><td>

The URL parameter sysparm\_notification is causing the system to open a new tab with the 'Notification preferences' page

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1732569

</td><td>

If AI Search is enabled and the user lacks visibility to the 'Workspaces' menu, search contexts are missing

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1736838

</td><td>

The Next Experience domain picker search does not work as expected

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1743329

</td><td>

The 'Landing page approvals' widget displays the opened\_by value instead of the requested\_for value of the requested item

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1743781

</td><td>

Notification of the currently selected update set is not visible in an instance with the Next Experience UI enabled

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1749880

</td><td>

A workspace without the globalSearchDataConfigId sys\_ux\_page\_property defined defaults to the original Unified Navigation configuration

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1757088

</td><td>

The cursor loses focus within the user notification preferences 'Add/Edit Schedule' when using the 'contains' condition

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1758972

</td><td>

The **Currency** field borders are cut off when they are made read-only via the client side

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1761432

</td><td>

In Next Experience, the list of domains is not populated in the domain picker

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1762435

</td><td>

Links to ServiceNow records direct to a blank record

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1763207

</td><td>

'All', 'Favorites', and 'History' shouldn't utilize 'WAI-ARIA Live Region'

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1768410

</td><td>

Service Operations Workspace \(SOW\) tabs are less descriptive in Washington, with the workspace name missing

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1779558

</td><td>

A domain with children whose entire hierarchy is turned off still appears in the domain picker

</td></tr><tr><td>

Normalization Data Services

</td><td>

PRB1714526

</td><td>

The 'Make Canonical Company' business rule's default logging is excessive, fragmented, and not useful, except when debugging

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1723984

</td><td>

My Notification Preferences opens a blank page

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1757886

</td><td>

Issue when trying to send a push notification to users whose Firebase token has expired

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1721741

</td><td>

In the advanced preferences of 'Notification Preferences', the translations of the categories aren't working

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1725599

</td><td>

After logging into an instance, users receive a 'Bad Request 400' when attempting to access 'Notifications' under the 'Preferences' UI action

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1727713

</td><td>

Mobile number validation isn't available on the 'Notification Preferences' component, which was previously possible in UI16

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1730698

</td><td>

Translated notification creation intermittently stops

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1731196

</td><td>

Notification preference filters aren't honored after saving the form

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1747621

</td><td>

The digest version of notifications will contain a watermark pointing to a specific record, but not always the watermark the digest email relates to

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1752158

</td><td>

Users observe a 400 error in the Next Experience UI when trying to toggle notification preferences in French

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1762798

</td><td>

Users aren't able to toggle off SMS devices if the notification doesn't have an SMS alternate

</td></tr><tr><td>

Notify integration with Twilio Direct

</td><td>

PRB1738058

</td><td>

The default created messaging service that is registered as a campaign by users is deleted on disconnect

</td></tr><tr><td>

Notify integration with Twilio Direct

</td><td>

PRB1768557

</td><td>

A number already added to 'MSG Service' at Twilio isn't added on the ServiceNow side

</td></tr><tr><td>

Now Code Editor

</td><td>

PRB1715803

</td><td>

A code editor doesn't display correct suggestions on an initial load

</td></tr><tr><td>

Now Experience Framework

</td><td>

PRB1738082

</td><td>

The input field for the Field List field type does not respond or update in the Configurable Workspace UI

</td></tr><tr><td>

NowMQ

</td><td>

PRB1759010

</td><td>

There is a redistribution of events to other nodes when one node is full

</td></tr><tr><td>

ServiceNow AI Platform Security

</td><td>

PRB1484329

</td><td>

Loading a form with the roles field takes a very long time due to the many sys\_user\_roles on the instance

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1712249

</td><td>

An error message is not translated to the selected language

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1725963

</td><td>

When using UI16, the vertical scroll bar doesn't appear on the filter criteria section

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1739774

</td><td>

Headers in high contrast mode in Windows do not have a black background

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1745233

</td><td>

The 'Create Favorites' bookmark for KB articles works differently after turning on the Next Experience UI

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1750313

</td><td>

The race condition in PageTimingProcessor should not generate a 'SEVERE \*\*\*ERROR\*\*\*' message in the log

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1753893

</td><td>

The UI16 Magellan Navigator 'Favorites' list has nested interactive elements that are not read by screen readers

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1769604

</td><td>

com.glide.script. RhinoEcmaError exception in the 'Update multiple experience flag' business rule on the sys\_properties table

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1747212

</td><td>

The on-call workflow is intermittently cancelled at the Timer activity without any error

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1729558

</td><td>

The canRead check on a table throws an error from a non-global scope

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1737415

</td><td>

Records in table on\_call\_escalations are not updated accurately

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1712083

</td><td>

The daily data job collection of 'Escalations' generates errors due to scripted breakdown mappings when processing non-task sources

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1728370

</td><td>

The 'On-call Create/Edit Schedule' \(wizard\) page isn't rendering properly

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1749524

</td><td>

Remove usage of notify.getPhoneNumbers\(\) for every SMS request

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1712151

</td><td>

The 'On-call' module isn't able to provide coverage for a shift on 11/5/23, when daylight savings happens

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1724115

</td><td>

If a user presses '1' before the input prompt, input isn't captured for an assignment

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1725818

</td><td>

Escalation acknowledgments fail via SMS

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1725934

</td><td>

A client script displays an error on trigger rules

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1729096

</td><td>

Updating an escalation set to 'default' is failing

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1732504

</td><td>

In On-Call Scheduling, the whole team primary escalation step does not work as expected with a single primary shift gap

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1735689

</td><td>

There are on-call scheduling gaps but they display as covered in a roster

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1736907

</td><td>

User on-call notification preferences that are created in a different domain are not honored during on-call escalation

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1744098

</td><td>

Schedule reports show the start and end times incorrectly and show previously selected groups

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1765309

</td><td>

User on-call preferences aren't honored as expected 30 minutes before the end time for the Asia/Kuala\_Lumpur timezone

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1773982

</td><td>

Users with rota\_admin/rota\_manager can't view an inactive user, so they can't use the 'Remove member' feature as documented

</td></tr><tr><td>

Oracle Reconciliation

</td><td>

PRB1759697

</td><td>

Recon fails if an entitlement has active maintenance set as true

</td></tr><tr><td>

Orchestration

</td><td>

PRB1760522

</td><td>

The JDBC probe doesn't work from Orchestration

</td></tr><tr><td>

Orchestration

</td><td>

PRB1718427

</td><td>

The MID server property mid.property.jms.command .allowed\_factory\_names contains a misspelt value: 'topicConnectionFactry'

</td></tr><tr><td>

Outbound REST Web Service

</td><td>

PRB1698360

</td><td>

The platform logs an incorrect message for an outbound connection when an OCSP check fails

</td></tr><tr><td>

Password Reset

</td><td>

PRB1727878

</td><td>

If users enter an invalid user, Virtual Agent conversations with 'Unlock Account' or 'Reset Password' template topics become stuck

</td></tr><tr><td>

Password Reset

</td><td>

PRB1728532

</td><td>

On the 'Password Reset Overview' page, under 'Password Reset - Failed Verifications \(last 7 days\)' it only displays 'No data to display'

</td></tr><tr><td>

Password Reset

</td><td>

PRB1734426

</td><td>

Password rules hints aren't displayed on the 'Reset Password' page when a password rule hint field is empty on the cred store

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1754203

</td><td>

Migrated Report data visualizations do not migrate the 'Created by' info to the Owner

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1732426

</td><td>

The com.snc.pa.dc.max\_records property is overridden while collecting snapshots

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1493147

</td><td>

X-Axis labels are not displayed with Week Number when a TimeSeries widget is applied with multiple breakdown elements

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1739870

</td><td>

Issues with Platform Analytics Migration after Washington DC Upgrade

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1760487

</td><td>

Performance Analytics \(PA\) score migration causes pa\_snapshots to contain an odd subset of records

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1716114

</td><td>

Performance Analytics and Reporting \(PAR\) dashboards are visible outside of a domain scope

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1759358

</td><td>

The homepage deprecation tool API ignores homepages without a view

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1715188

</td><td>

The dictionary's default value in the **Color** field in pa\_dashboard isn't removed as expected on upgrade instances

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1721739

</td><td>

In Performance Analytics, 'Admin console' dashboard tab records aren't loading

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1725535

</td><td>

Performance Analytics's **Indicators** field labels are invisible in dark mode

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1738638

</td><td>

Duplication API expects a top layout to always be present, but sometimes it is not

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1744336

</td><td>

Indicator scorecard visualization does not show data for previous scores when the indicator unit is 'time'

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1749825

</td><td>

Dashboard-level group/role/user permissions aren't migrated during bulk migration

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1755501

</td><td>

A scheduled export of the type 'Embed PNG' doesn't work

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1764014

</td><td>

The Performance Analytics Task.Location breakdown has a potential script recursion that can cause timeouts

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1775894

</td><td>

In HSQL Data Collector, there's an incorrect score value calculation for COUNT DISTINCT on the scripted indicator

</td></tr><tr><td>

Performance Analytics API

</td><td>

PRB1733050

</td><td>

A single score component on the Agent Workspace homepage isn't changed correctly

</td></tr><tr><td>

Performance Analytics API

</td><td>

PRB1732023

</td><td>

Changes in the color values for target\_color\_scheme record are not reflected in the scorecard API

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1690620

</td><td>

Interactive filters all checkbox is not functioning as expected

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1722196

</td><td>

Tabs aren't accessible through the keyboard

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1730655

</td><td>

Deleted filter values are persisted for a visualization in a dashboard

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1751347

</td><td>

After turning off Next Experience on an instance, the home page is forced to display 'now/platform-analytics-workspace/dashboard-library'

</td></tr><tr><td>

Performance Analytics Dashboards

</td><td>

PRB1774493

</td><td>

Saving a report as a PNG/JPEG on a dark theme makes the text appear light grey in the downloaded file

</td></tr><tr><td>

Performance Analytics Diagnostics

</td><td>

PRB1719297

</td><td>

If any Performance Analytics \(PA\) scripts don't contain fields, the diagnostics encounter a 'com.glide.script .RhinoEcmaError: Cannot convert null to an object' exception

</td></tr><tr><td>

Performance Analytics Widgets

</td><td>

PRB1761413

</td><td>

The 'pa-ui' component is not refreshed in client browsers when a new version of it is released

</td></tr><tr><td>

Performance Dashboards

</td><td>

PRB1747942

</td><td>

Performance Dashboard graphs are blank \(Garbage Collection Activity and Metaspace\)

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1712454

</td><td>

A colon in cache\_nature\_id breaks XMLStats and throws an error

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1764334

</td><td>

Some files aren't consumed when some plugins are activated through automated plugin activation

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1742590

</td><td>

A colon in the name for a sys\_status record causes unparseable xmlstats.do

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1752341

</td><td>

Thread yield on close timeout can delay node recovery

</td></tr><tr><td>

Portal App Shell

</td><td>

PRB1660512

</td><td>

Exact Keyword search is not working from Chrome header by UI Builder

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB1612544

</td><td>

The 'Calculate Row Count' business rule triggers slow queries that could be offloaded to a secondary database

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB1629897

</td><td>

The user is unable to train classification solution definitions that have a filter condition for keywords

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB1646823

</td><td>

For system clean-up phase one, instituting adoption of data retention policies

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB1689172

</td><td>

In Predictive Intelligence, there's a DxC\_ML: Error 'no summary found for' when inserting clustering details

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB1756981

</td><td>

Server-side code should use GlideAgregate instead of GlideRecord.getRowCount\(\) for sysevent\_script\_action

</td></tr><tr><td>

Predictive Intelligence for Case Management \(CSM\)

</td><td>

PRB1744081

</td><td>

Using the CSMPredictionHelper extension point does not find the Customer Service Management \(CSM\) custom tables and solutions for predictions

</td></tr><tr><td>

Predictive Intelligence for Knowledge Management

</td><td>

PRB1783818

</td><td>

The 'Related Article' widget isn't displaying knowledge articles from the 'Knowledge Similar Articles' solution

</td></tr><tr><td>

Proactive Analytics

</td><td>

PRB1769634

</td><td>

Correlation analysis' sys\_log error message displays the variable name instead of its value

</td></tr><tr><td>

Problem Management

</td><td>

PRB1716410

</td><td>

The inbound email action 'Update Problem' uses the ITIL role instead of the ITSM/CMDB fine-grained roles or using a combined condition

</td></tr><tr><td>

Problem Management

</td><td>

PRB1739264

</td><td>

The field label for 'closed\_at' of the problem and problem task is mismatch when a non-English language is selected

</td></tr><tr><td>

Problem Management

</td><td>

PRB1740981

</td><td>

There's a localization issue for problem labels in Service Operations Workspace \(SOW\)

</td></tr><tr><td>

Problem Management

</td><td>

PRB1746566

</td><td>

A problem.fixes event is triggered when a change request created from an incident is canceled

</td></tr><tr><td>

Process Automation Designer \(Family Channel\)

</td><td>

PRB1731083

</td><td>

There's a false error when previewing a remote update set

</td></tr><tr><td>

Process Automation Designer \(Family Channel\)

</td><td>

PRB1751565

</td><td>

An existing record with a playbook displays a configuration error post-upgrade

</td></tr><tr><td>

Process Mining

</td><td>

PRB1724052

</td><td>

A scheduled task mining fails for transitions with contextual conditions with the predicate 'is one of'

</td></tr><tr><td>

Process Mining

</td><td>

PRB1733621

</td><td>

Creating a new or changing existing custom 'start stop' conditions doesn't set the project as dirty

</td></tr><tr><td>

Process Mining

</td><td>

PRB1740197

</td><td>

If ExecutionTracker times out while the actual schedule task completes, the user is not able to create a schedule task for the same condition and does not see results even though results exists

</td></tr><tr><td>

Process Mining

</td><td>

PRB1745642

</td><td>

Checking licensing for subprod/open instances

</td></tr><tr><td>

Process Mining

</td><td>

PRB1745780

</td><td>

Finding rule validations can potentially cause timeouts

</td></tr><tr><td>

Procurement

</td><td>

PRB1692608

</td><td>

A special character in the POL short description prevents Asset orders from moving to the 'Received' state

</td></tr><tr><td>

Procurement

</td><td>

PRB1756804

</td><td>

There's an issue with transfer order line stage processing in the 'Push Status to Asset/Consumable' business rule due to the 'Transfer order Line SM core' workflow

</td></tr><tr><td>

Project Management

</td><td>

PRB1581610

</td><td>

In Project Workspace, the planned end date isn't updated accordingly

</td></tr><tr><td>

Project Management

</td><td>

PRB1758365

</td><td>

The **Hide/Show**, **Manage**, and **New** buttons on the resource plan related list have issues

</td></tr><tr><td>

Project Management

</td><td>

PRB1642449

</td><td>

Error while fetching data on program workbench

</td></tr><tr><td>

Project Management

</td><td>

PRB1711601

</td><td>

Fields in fm\_expense\_line

</td></tr><tr><td>

Project Management

</td><td>

PRB1711834

</td><td>

In project planning console, it is not possible to copy a project with an empty Start date

</td></tr><tr><td>

Project Management

</td><td>

PRB1727258

</td><td>

No content is loaded after selecting the **Edit** button in related list for projects

</td></tr><tr><td>

Project Management

</td><td>

PRB1753033

</td><td>

Projects closed via the planning console or Project Workspace from sub-tasks do not update the **closed\_at** and **close\_by** fields

</td></tr><tr><td>

Project Management

</td><td>

PRB1711296

</td><td>

Users are not allowed to create a Project Task for an Agile Phase record via the classic UI but can in Project Workspace

</td></tr><tr><td>

Project Management

</td><td>

PRB1714424

</td><td>

A business stakeholder isn't able to see risk, issue, decision, action, or request changes \(RIDAC\) in a project status report

</td></tr><tr><td>

Project Management

</td><td>

PRB1715240

</td><td>

In Next Experience, selecting the 'Program Workbench' link after changing the related list filter causes a 404 error

</td></tr><tr><td>

Project Management

</td><td>

PRB1715879

</td><td>

An ACL condition has the script check on 'is\_labor\_cost\_plan' despite a user not having the dictionary in the instance

</td></tr><tr><td>

Project Management

</td><td>

PRB1722933

</td><td>

'Undefined' displays on a custom column via the Planning Console

</td></tr><tr><td>

Project Management

</td><td>

PRB1724020

</td><td>

CSMProjectDomainSeparationUtils is missing a global qualifier for JSUtil

</td></tr><tr><td>

Project Management

</td><td>

PRB1724938

</td><td>

When users have a column-level ACL, the classic Project Workspace doesn't load

</td></tr><tr><td>

Project Management

</td><td>

PRB1725974

</td><td>

'Program Planned End Date' calculates incorrectly when users close the child project task

</td></tr><tr><td>

Project Management

</td><td>

PRB1727831

</td><td>

Modifying the value of 'Entered benefit' in 'Monetary Benefit Plan Breakdowns' creates a duplicate audit

</td></tr><tr><td>

Project Management

</td><td>

PRB1728048

</td><td>

Project Workspace isn't displaying risk records in the 'Risk, Issue, Decision, Action, or Request Change \(RIDAC\)' view

</td></tr><tr><td>

Project Management

</td><td>

PRB1729864

</td><td>

Changing project tasks' start dates throws an error: 'The task start date cannot be earlier than the predecessor's end date'

</td></tr><tr><td>

Project Management

</td><td>

PRB1731897

</td><td>

When a subtask with a duration is created under a parent task milestone record, the 'Key milestone' is still unticked on the parent task record

</td></tr><tr><td>

Project Management

</td><td>

PRB1732061

</td><td>

A missing semicolon in the 'InvstFunding RequestClientBase' UI script causes an issue

</td></tr><tr><td>

Project Management

</td><td>

PRB1732300

</td><td>

The **entered\_currency** field of a **Cost plan breakdown** record is set to empty

</td></tr><tr><td>

Project Management

</td><td>

PRB1732469

</td><td>

The program tab does not display correctly from the 'Agile Planning and Tracking' link on a project

</td></tr><tr><td>

Project Management

</td><td>

PRB1732568

</td><td>

PDF formatting issue with displaying long paragraphs in portrait mode for project status reports

</td></tr><tr><td>

Project Management

</td><td>

PRB1735526

</td><td>

There's a spelling error in the Project Workspace 'Configuration' column

</td></tr><tr><td>

Project Management

</td><td>

PRB1739943

</td><td>

The 'Move Project' UI action is not working as expected

</td></tr><tr><td>

Project Management

</td><td>

PRB1746714

</td><td>

Projects are reopened when stories are unrelated to a closed project

</td></tr><tr><td>

Project Management

</td><td>

PRB1749505

</td><td>

Cannot modify pm\_project\_task under the Employee Service Center portal, and the **Save** button does not respond due to the base instance onSubmit client script 'Complete Agile phase'

</td></tr><tr><td>

Project Management

</td><td>

PRB1749859

</td><td>

Schedule entries for a project's schedule may contribute to incorrect calculation of dates from durations

</td></tr><tr><td>

Project Management

</td><td>

PRB1750798

</td><td>

Access is not provided to the sn\_ppm\_read role on teamspace tables

</td></tr><tr><td>

Project Management

</td><td>

PRB1752174

</td><td>

The 'PercentCompleteRollupHandler' takes time to execute due to dot-walking on the field in function call

</td></tr><tr><td>

Project Management

</td><td>

PRB1755315

</td><td>

The 'Actual Duration' project behaves unexpectedly when the 'Allow dates outside schedule' checkbox is selected

</td></tr><tr><td>

Project Management

</td><td>

PRB1755801

</td><td>

Users are added to the backlog by a UI action and are added multiple times to the 'Visible to' list

</td></tr><tr><td>

Project Management

</td><td>

PRB1761595

</td><td>

'Save as new template' failed in creating a template

</td></tr><tr><td>

Project Management

</td><td>

PRB1768915

</td><td>

Migrating 'Demand' UI actions

</td></tr><tr><td>

Project Portfolio Management

</td><td>

PRB1591115

</td><td>

Loading a subproject in a project form is taking more than 2 minutes

</td></tr><tr><td>

Record Watcher

</td><td>

PRB1742660

</td><td>

The record watcher clean-up query takes up to 15% of total DB time according to 'Slow Queries'

</td></tr><tr><td>

Related Lists

</td><td>

PRB1716667

</td><td>

In Next Experience, a hierarchical list aligns UI actions to the right for child records

</td></tr><tr><td>

Related Lists

</td><td>

PRB1748522

</td><td>

The related list **Edit** button on 'Contract - Contact' shows only sys IDs instead of usernames

</td></tr><tr><td>

Release Management

</td><td>

PRB1777399

</td><td>

The 'release\_v2\_admin' role doesn't contain the 'release\_v2\_user' role

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

</td><td>

PRB1734587

</td><td>

The Remote Process Sync 'Update Correlation State' action updates the state to an invalid value

</td></tr><tr><td>

Renewal Calendar

</td><td>

PRB1714202

</td><td>

'Jump to section navigator' doesn't work on a form component that's inside a roadmap component

</td></tr><tr><td>

Renewal Calendar

</td><td>

PRB1748516

</td><td>

Unnecessary filter for active = true on the list view for entitlements and contracts in the renewals calendar

</td></tr><tr><td>

Reporting

</td><td>

PRB1736998

</td><td>

Tooltip text doesn't disappear even after drilling down the report in the dashboard

</td></tr><tr><td>

Reporting

</td><td>

PRB1743283

</td><td>

Inconsistent trend results observed between the report data label and the report results when the first day of the week property is amended

</td></tr><tr><td>

Reporting

</td><td>

PRB1762400

</td><td>

When translated to French, reports of the type 'Time Series' generate an error

</td></tr><tr><td>

Reporting

</td><td>

PRB1554166

</td><td>

When a list report is grouped by a **Choice** field and when opening the group in a list view, extra filters are added

</td></tr><tr><td>

Reporting

</td><td>

PRB1730161

</td><td>

Data table grid columns aren't mirrored in Hebrew and Arabic PDF files

</td></tr><tr><td>

Reporting

</td><td>

PRB1733795

</td><td>

Users can't open or create reports when the system property glide.ui.escape\_text is false or removed

</td></tr><tr><td>

Reporting

</td><td>

PRB1742675

</td><td>

The word 'empty' is not translated in the data visualization in a configurable workspace

</td></tr><tr><td>

Request Management

</td><td>

PRB1734807

</td><td>

The **New** button on a catalog task in a requested item form's related list is always visible

</td></tr><tr><td>

Resource Management

</td><td>

PRB1741778

</td><td>

An error displays when syncing RA's

</td></tr><tr><td>

Resource Management

</td><td>

PRB1724290

</td><td>

The end date on a resource plan isn't populated correctly from the 'Form' view

</td></tr><tr><td>

Resource Management

</td><td>

PRB1730205

</td><td>

If an operational resource plan is updated post-allocation, the 'task' and 'top\_task' resource allocation daily records are set to 'undefined'

</td></tr><tr><td>

Resource Management

</td><td>

PRB1733111

</td><td>

There's incorrect monthly actual data in the resource\_aggregate\_monthly table as compared with the hours on the expense line breakdowns

</td></tr><tr><td>

Resource Management

</td><td>

PRB1736328

</td><td>

When using a different language than English, 'Resource' reports display a unit in the description that's not expected

</td></tr><tr><td>

Resource Management

</td><td>

PRB1738670

</td><td>

If a resource plan is allocated immediately after being confirmed, the availability does not update correctly on resource\_aggregate\_weekly

</td></tr><tr><td>

Resource Management

</td><td>

PRB1739888

</td><td>

'FTE' is calculated differently in allocation workbench because the user timezone is not respected when computing allocation details through the allocation workbench

</td></tr><tr><td>

Resource Management

</td><td>

PRB1744509

</td><td>

Time Cards are incorrectly associated with project-related resource plans

</td></tr><tr><td>

Resource Management

</td><td>

PRB1757925

</td><td>

Doing a 'Show Matching' operation on the **Created by** field for resource plans via the related list causes an 'Invalid Resource Plan ID' error message when trying to move the state to 'Complete' with the 'Action on selected rows...' option

</td></tr><tr><td>

Resource Management

</td><td>

PRB1759244

</td><td>

RMUtil.getTaskSub TreeRootDataFromRP uses getDate\(\) instead of getLocalDate\(\)

</td></tr><tr><td>

REST API Explorer

</td><td>

PRB1744904

</td><td>

A user with the rest\_api\_explorer role isn't able to access REST API Explorer

</td></tr><tr><td>

REST APIs

</td><td>

PRB1753606

</td><td>

An extra query is issued for table API requests resolving reference fields for inserts and updates, causing a transaction timeout

</td></tr><tr><td>

RESTMessageV2 API

</td><td>

PRB1734419

</td><td>

Cloud Provisioning and Governance \(CPG\) catalogs are triggered multiple times when triggered from **Business Rule** &gt; **REST Message**

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

</td><td>

PRB1746226

</td><td>

Restricted Caller Access \(RCA\) should be checked even when the script include is already included

</td></tr><tr><td>

Robust Transform Engine \(RTE\)

</td><td>

PRB1725594

</td><td>

There's a Robust Transform Engine \(RTE\) index out of bound exception when a collection's first object doesn't have a complete schema structure

</td></tr><tr><td>

Rollback and Recovery

</td><td>

PRB1755024

</td><td>

Delete operations with 'Rollback' enabled trigger a mass DELETE FROM sys\_rollback\_sequence and causes replication lag

</td></tr><tr><td>

Rollback and Recovery

</td><td>

PRB1543140

</td><td>

ATF tests don't roll back records if logged-in users' domains don't match the selection in the domain picker

</td></tr><tr><td>

Rollback and Recovery

</td><td>

PRB1742336

</td><td>

Duplicate 'Clean Expired Rollback Contexts' sys\_trigger records are created when an instance is provisioned

</td></tr><tr><td>

Rollback and Recovery

</td><td>

PRB1731832

</td><td>

When deleting CMDB \(cmdb\_ci\) records using GlideMultipleDelete in a background script, it doesn't successfully restore data from fields specific to CMDB child tables

</td></tr><tr><td>

Rollback Contexts

</td><td>

PRB1706257

</td><td>

A rollback with a large number of records triggers a large delete query causing replication lag

</td></tr><tr><td>

Schedule Calendar

</td><td>

PRB1776450

</td><td>

When the user updates the system property \(glide.sys.date\_format\) to dd-MMM-yyyy, the month isn't displayied correctly in the schedule calendar

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1723650

</td><td>

Scheduled jobs are stuck in a running state due to connection issues or node restarts and should be reset

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1709703

</td><td>

Post-clone, multiple text index jobs are executed even though there's should only be one of these per instance running at a time

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1729518

</td><td>

The 'Restrict non-admin on Run-As field' business rule on a sys\_auto error message isn't visible to the user

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1734625

</td><td>

Business Calendars with a floating timezone are not taking into account DST

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1708724

</td><td>

The 'Archive' job schedules 1 'Re-Archiver' job every hour, so if one job runs long, it causes scheduler contention

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1771051

</td><td>

Jobs are executed twice during a rescheduler restart

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB1782901

</td><td>

High cardinality of the 'Job classification' column can prevent scheduled jobs from being processed due to a StackOverflowError in SchedulerThread

</td></tr><tr><td>

Schedules

</td><td>

PRB1717977

</td><td>

The on-call calendar doesn't display correctly when a shift starts from 8:30:00 to 08:29:59 the next day

</td></tr><tr><td>

Schedules

</td><td>

PRB1724036

</td><td>

In System Scheduler, the 'Show Schedule' page is completely hardcoded

</td></tr><tr><td>

Schedules

</td><td>

PRB1746190

</td><td>

Schedule entries \(cmn\_schedule\_span\) that are not marked as 'ALL DAY' change time zones in read-only mode

</td></tr><tr><td>

Schedules

</td><td>

PRB1758236

</td><td>

The node restarts when inputting a particular date in the **To** and **Repeat until** fields

</td></tr><tr><td>

Script Includes

</td><td>

PRB1731369

</td><td>

Setting a default value for a reference field fails when invoking a script include

</td></tr><tr><td>

Secondary Database Management

</td><td>

PRB1754273

</td><td>

There's gateway password decryption failures due to a premature attempt to use Key Management Framework \(KMF\)

</td></tr><tr><td>

Seismic Framework

</td><td>

PRB1751888

</td><td>

Cache busting doesn't occur on pages routed through the UxPageProcessor

</td></tr><tr><td>

Seismic Framework

</td><td>

PRB1752772

</td><td>

The instance redirects to /welcome.do or /session\_timeout.do before authenticating via SSO when the user selects any instance-specific link

</td></tr><tr><td>

Seismic Framework

</td><td>

PRB1783295

</td><td>

There's an empty Service Operations Workspace incident form after upgrading from Vancouver to Washington

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1777353

</td><td>

There's an issue compiling a script using a map iterator in a 'for' loop

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1714731

</td><td>

After a Vancouver upgrade from Utah, GlideRecord.getElement\(\).getDisplayValue\(\) doesn't honor the user locale preferences

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1754391

</td><td>

Scope.isIVSScope\(\) is incorrectly marking internal Servicenow scopes as ISV scopes

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1653850

</td><td>

A script debugger throws an error when referencing the 'this' object

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1692959

</td><td>

Number.prototype.toLocaleString fails, as it treats the first argument as the base

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1715580

</td><td>

GlideRecord API improperly passes an integer addOrCondition\(\) value as a decimal

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1717170

</td><td>

Installing a third party dependency in a module and requiring it in a script results in a JVM crash

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1730509

</td><td>

In Firefox, after running a background script, the browser's **Back** button doesn't return to the script page

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1737150

</td><td>

Related list conditions in JavaScriptGenerator require an encoded query or it generates a null pointer exception

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1737649

</td><td>

There's a noticed performance impact with the scheduled job 'Set VA Supported Flag'

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1752131

</td><td>

External users are not able to add an attachment on a catalog item macroponent

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1729616

</td><td>

Upon submitting a Service Catalog order, the 'Thank you, your request has been submitted' is not read out by screen readers

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1736019

</td><td>

Updates to field translations made with the **Edit Translations** button on the Catalog Item screen are not displayed on Service Portal

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1743369

</td><td>

Stale recurring frequency stored in the cache

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1658678

</td><td>

Catalog item images on Portal are not displayed on domain-separated instances

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1720343

</td><td>

The user criteria cache isn't consistent across all nodes on catalog items with subscriptions

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1734166

</td><td>

Localization framework publishes translations in the global scope although the artifact record is created in a different scope

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1751251

</td><td>

Attachments are disappearing when attached to the service catalog forms

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1757001

</td><td>

Not possible to customize 'Ticket Action' widgets

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1515076

</td><td>

In the portal, the currency symbol in the reference field list is not displayed

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1671988

</td><td>

Screen reader doesn't announce the label name of the combo box 'Title size'

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1710997

</td><td>

sc\_category items with child nodes incorrectly report their list placement

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1720309

</td><td>

Request summary content isn't marked up programmatically

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1720615

</td><td>

The visual text of a link isn't associated with a component programmatically

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1726998

</td><td>

The 'Close' icon on the categories selector in 'Manage HR Catalog' doesn't work

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1733864

</td><td>

A copy request isn't copying a request for an 'in' variable

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1735197

</td><td>

Some Service Catalog variable's field translations aren't copied

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1735254

</td><td>

Variables in variable sets can't be updated by an open catalog item from a wish list

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1736674

</td><td>

A check box's read only and visibility settings are incorrect via Service Script

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1737431

</td><td>

The related list sys\_ui\_related\_sc\_ cat\_item\_producer\_null is overwritten during an upgrade

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1744529

</td><td>

Multiple versions are created/displayed when importing XML

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1749981

</td><td>

Demo data removal script delets 'sc\_catalog' Service Catalog with its categories

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1752628

</td><td>

'Copy Attachment' isn't working for Record Producer in an order guide

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1755418

</td><td>

The condition script is not evaluated in the execution plan

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1758469

</td><td>

The translation of the name of the catalog elements to the Service Portal does not work as expected

</td></tr><tr><td>

Service Catalog API

</td><td>

PRB1782677

</td><td>

UI Policies using the 'OR' clause not working in NowAssist in VA

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1742298

</td><td>

Catalog build does not support READ field ACLs

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1748023

</td><td>

Warning messages observed in the Washington DC release for invalid control characters \(^M\) in XML

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1760494

</td><td>

The Catalog Builder fulfillment step list isn't working as expected

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB1761456

</td><td>

When logged in as a Catalog Builder editor, the fulfillment step throws a security rule-related error

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1764839

</td><td>

The **Date** field isn't set using sc\_item\_ variable\_assignment in an order guide rule

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1609965

</td><td>

The parent case field on a case task list view on the Customer Service management \(CSM\) portal is empty, even when it's displayed on the form view

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1746017

</td><td>

A standard ticket screen bounces when submitting the catalog item 'Register a Business Application' when there are many approvers

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1746815

</td><td>

Files added in the attachment type variable are not retained after selecting 'Add to wishlist'

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1758896

</td><td>

The 'My Requests' widget \(cloned version\) cannot be updated

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1715031

</td><td>

In the Customer Service Management \(CSM\) portal, the TinyMCE HTML editor system font doesn't translate in Portuguese

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1734447

</td><td>

Multi-row variable set row icons are displayed underneath each other instead of next to each other on a Service Portal catalog item

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1740257

</td><td>

A cross-scope error is seen on an HR table, causing the Virtual Agent case details card to show empty fields

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1744103

</td><td>

Dynamic Translation does not appear in Employee Center for 'Approval History' in the activity stream

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1744236

</td><td>

The tab title on the portal page sc\_cat\_item does not fetch the item name as expected for customer\_contact

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1745077

</td><td>

The CSM Standard Ticket Configuration widget does not render the HTML code style

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1745173

</td><td>

File attachments are missing when submitting a request from a draft

</td></tr><tr><td>

Service Catalog Variables

</td><td>

PRB1720613

</td><td>

Decimal places for a price are displayed unexpectedly in select box variables even when the currency is a zero-decimal

</td></tr><tr><td>

Service Creator

</td><td>

PRB1733343

</td><td>

There are long-running 'Init Service Designer Form' jobs on the standby nodes of an instance

</td></tr><tr><td>

Service Creator

</td><td>

PRB1715639

</td><td>

The **Description** field disappears when creating Service Designer

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1728854

</td><td>

Setting the property com.snc.sla.condition\_ class.caching.enabled to false prevents the SLA Engine from attaching SLAs

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1734205

</td><td>

'SLA Repair' and 'SLA Timeline' using HistoryWalker give undesired results when audit data has a split transaction

</td></tr><tr><td>

Service Management Virtual Agent Topic Blocks

</td><td>

PRB1712119

</td><td>

The vaVars.\_topic\_sorry\_msg \(va script block\)/com.glide.cs.no \_topic \_ sorry\_message property isn't translated in Virtual Agent \(VA\) chats

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1717472

</td><td>

The Application Service Wizard increments the **Number** field on a new record multiple times during creation

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1725024

</td><td>

Excessive and unnecessary logging of 'Executing Update Entry Point Candidates BR' causes usability and performance issues for the syslog table

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1688161

</td><td>

Service-mapping workspace doesn't show ML powered candidates due to a bad record of the sm\_admin role in the sys\_ux\_applicability record

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1734706

</td><td>

The scheduled job 'Service Mapping - Traffic Process to Process' introduces long runs when updating the p2p\_extension table

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1723151

</td><td>

The 'Application Service Manual Ep Cleanup' job triggers unnecessary recomputations

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1734462

</td><td>

The 'Create Pattern from Generic Application' action sticks on loading when running a generic application process command is missing or empty

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1536950

</td><td>

The MID Server crashes with an Out of Memory \(OOM\) error when handling a large number of file systems

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1705211

</td><td>

Uploading indicators tabs based on a large database view takes a long time

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1733108

</td><td>

Adding a check whether endpoint\_id=='null' as a string is part of the null check condition

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1736183

</td><td>

Recalculating the 'Service' UI action for tag-based services that are executed in the foreground can cause a timeout for large services

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1738279

</td><td>

There's a memory leak in the 'Service Mapping Recomputation' job due to the ServiceImplementationCache not clearing

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1738372

</td><td>

Change info logging in SAProcessTopologyClassifier to 'debug'

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1748880

</td><td>

When creating an inclusion discovery task, it is created with discovery\_status = null

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1751897

</td><td>

The network path is calculated even if the target node is marked as a boundary

</td></tr><tr><td>

Service Model Foundation

</td><td>

PRB1768842

</td><td>

Contributors should be able to comment and assign the case tasks that are visible to them

</td></tr><tr><td>

ServiceNow Studio \(Legacy\)

</td><td>

PRB1741989

</td><td>

A user who has access to a protected script cannot find the content inside the script via the code search feature in ServiceNow Studio

</td></tr><tr><td>

Service Portal

</td><td>

PRB1719006

</td><td>

If it's set via the onChange catalog client script, a read-only HTML variable isn't visible

</td></tr><tr><td>

Service Portal

</td><td>

PRB1745184

</td><td>

'Service catalog' in breadcrumb is not translated consistently

</td></tr><tr><td>

Service Portal

</td><td>

PRB1725506

</td><td>

Attachments are not displayed in the ServicePortal Activity stream

</td></tr><tr><td>

Service Portal

</td><td>

PRB1732434

</td><td>

After the Vancouver upgrade, an attachment base instance pop-up is not similar to what is on PDI

</td></tr><tr><td>

Service Portal

</td><td>

PRB1733037

</td><td>

Changes are not saved on form reload when the network is slow

</td></tr><tr><td>

Service Portal

</td><td>

PRB1715252

</td><td>

Color alone is used to distinguish a link

</td></tr><tr><td>

Service Portal

</td><td>

PRB1733620

</td><td>

A logged in user can't see their profile in their organization chart on the profile page

</td></tr><tr><td>

Service Portal

</td><td>

PRB1743912

</td><td>

A base instance Search Page widget cannot be saved, and **Server Script** field yields error

</td></tr><tr><td>

Service Portal

</td><td>

PRB1746097

</td><td>

Null pointer exception observed when accessing $sp.do

</td></tr><tr><td>

Service Portal

</td><td>

PRB1754534

</td><td>

Incorrect favicon appears in Google searches

</td></tr><tr><td>

Service Portal

</td><td>

PRB1758275

</td><td>

Service Portal Related List Attachment doesn't work and redirects to a blank page

</td></tr><tr><td>

Service Portal

</td><td>

PRB1635895

</td><td>

A widget with a query doesn't work post session time-out if it's directed from the header menu item right after login

</td></tr><tr><td>

Service Portal

</td><td>

PRB1669934

</td><td>

Related documents widget does not allow upload when there is **Date/Time** Field on the pop-up

</td></tr><tr><td>

Service Portal

</td><td>

PRB1685905

</td><td>

When browsing KB Categories with a screen reader, the Article Badge counts are not announced

</td></tr><tr><td>

Service Portal

</td><td>

PRB1688882

</td><td>

Service Portal Date Picker has the improper markup role='application'

</td></tr><tr><td>

Service Portal

</td><td>

PRB1696903

</td><td>

The focus indicator doesn't reside on the correct item and the knowledge article count is not announced

</td></tr><tr><td>

Service Portal

</td><td>

PRB1699792

</td><td>

Date picker \(sn-date-picker\) doesn't automatically close when selectbox is selected in Service Portal causing an overlap issue when the browser window is resized

</td></tr><tr><td>

Service Portal

</td><td>

PRB1714454

</td><td>

A user can't select a date in the calendar picker on the Mobile App and on the Mobile Service Portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1719087

</td><td>

Catalog item annotations don't expand when at a certain length

</td></tr><tr><td>

Service Portal

</td><td>

PRB1723919

</td><td>

The 'Approval' widget displays incorrect information

</td></tr><tr><td>

Service Portal

</td><td>

PRB1732351

</td><td>

Tracking an impersonated user should be allowed according to UCM Decision

</td></tr><tr><td>

Service Portal

</td><td>

PRB1732644

</td><td>

In a Knowledge Base filter on the 'Mobile' view, the focus doesn't return to the **Filter** button when a user selects 'done'

</td></tr><tr><td>

Service Portal

</td><td>

PRB1733272

</td><td>

On Service Portal's list collector, variables are still visible after exiting the page

</td></tr><tr><td>

Service Portal

</td><td>

PRB1737463

</td><td>

The 'Back to Top' link does not work as expected in the Knowledge Base articles in the Knowledge Base portal and Employee Service Center

</td></tr><tr><td>

Service Portal

</td><td>

PRB1738182

</td><td>

Long\_label doesn't work on /csm

</td></tr><tr><td>

Service Portal

</td><td>

PRB1743178

</td><td>

The advanced view rule does not work on Service Portal after creating a record or transition

</td></tr><tr><td>

Service Portal

</td><td>

PRB1743596

</td><td>

The select box is missing the required accessibility attribute in Service Portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1745256

</td><td>

On CSM Portal, users can see related lists that do not exist in the backend

</td></tr><tr><td>

Service Portal

</td><td>

PRB1747389

</td><td>

Certain text in the Employee Service Center for the Faceted Search widget are not translated

</td></tr><tr><td>

Service Portal

</td><td>

PRB1748379

</td><td>

Selecting a list selection causes a pop-up to be displayed in the top left of the frame

</td></tr><tr><td>

Service Portal

</td><td>

PRB1748592

</td><td>

Users are unable to reach the reference field after calling the clearValue\(\) method

</td></tr><tr><td>

Service Portal

</td><td>

PRB1751266

</td><td>

When reviewing skipped records for Washington DC, a spelling error is observed in the code related to a function

</td></tr><tr><td>

Service Portal

</td><td>

PRB1755061

</td><td>

In Service Portal, when list collector variables are read-only, they are skipped by keyboard navigation

</td></tr><tr><td>

Service Portal

</td><td>

PRB1757924

</td><td>

After attaching files to a catalog item in the portal, if the attachments are renamed, the extension is removed

</td></tr><tr><td>

Service Portal

</td><td>

PRB1760641

</td><td>

The portal catalog item offers attachment encryption options even though attachment encryption has been turned off in 'Encrypted Field Configurations'

</td></tr><tr><td>

Service Portal

</td><td>

PRB1761633

</td><td>

The portal console log gives an icon pre-load error

</td></tr><tr><td>

Service Portal

</td><td>

PRB1763318

</td><td>

Knowledge article anchor tags do not jump to the specific element \(\#id\) of the page by selecting the icon link widget or carousel widget

</td></tr><tr><td>

Service Portal

</td><td>

PRB1767137

</td><td>

'Insert' and 'Stay' on a sp\_portal record prevents updates to the **Logo** field on a newly created record

</td></tr><tr><td>

Service Portal

</td><td>

PRB1763054

</td><td>

The date/time picker does not translate to Arabic

</td></tr><tr><td>

Service Portal

</td><td>

PRB1711713

</td><td>

Comboboxes are described as unavailable

</td></tr><tr><td>

Service Portal

</td><td>

PRB1770510

</td><td>

In Safari browsers, there is a UI scroll issue on the 'Track all your tickets' page

</td></tr><tr><td>

Service Portal Announcements

</td><td>

PRB1762268

</td><td>

The announcement for the **More** button has no function when using a zoom factor of at least 400x

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1702851

</td><td>

On a Portal page with more than two data table widgets, the user is unable to edit/add a filter condition on the second widget of the page

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1734641

</td><td>

On the 'Organization Chart' widget, changes on instance options are causing the widget to crash

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1737559

</td><td>

Is\_multi\_text = false does not work as expected in Service Portal

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1744433

</td><td>

The activity stream always displays the first activity stream entry of records created by 'system' in English and is not translated

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1757571

</td><td>

On a data table from an instance definition, users are unable to filter the list when a field is blank due to an ACL

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1739773

</td><td>

Duplicate availability calculations occurring

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1767688

</td><td>

There's incorrect lifecycle mappings for business service and technical service

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1731037

</td><td>

The 'Handle Performance Score' business rule aborts a transaction and causes 'Publish Service Approval subflow' to error

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1734440

</td><td>

A service offering update is blocked when changing the parent

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1736011

</td><td>

When retiring a service, the service offerings aren't retired automatically

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1750190

</td><td>

The document ID does not handle the table extension transparently

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1756415

</td><td>

Issue with referencing fields after switching from the legacy structure to the standard portfolio structure

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1777498

</td><td>

If a parent is of a different value, an offering shouldn't be marked as 'duplicate of'

</td></tr><tr><td>

Session Management

</td><td>

PRB1741142

</td><td>

An uncaught exception causes stale records in the 'Active Transactions \(All Nodes\)' table

</td></tr><tr><td>

Session Management

</td><td>

PRB1757612

</td><td>

An uncaught null pointer exception causes stale records in the 'Active transactions \(all nodes\)' table

</td></tr><tr><td>

Session Management

</td><td>

PRB1714960

</td><td>

The Frequent list\_history.do error appears to extend user sessions

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1719184

</td><td>

current.member\_type isn't evaluated as expected in the business rule script on the first insert into the sys\_cs\_collab\_member table

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1719893

</td><td>

In the workspace 'Discuss Sidebar' chat, the size of the chat text entry window is smaller after an upgrade to Vancouver

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1755062

</td><td>

Translation errors in the Sidebar omni-experience standard feature set plugin and incorrect time format for 'now-message-timestamp'

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1770062

</td><td>

An updated KB record doesn't reflect on a record card from a sidebar discussion

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1764002

</td><td>

Screen Readers \(NVDA and JAWS\) announce both the 'Select Emoji' label and tooltip 'Insert Emoji' when focused

</td></tr><tr><td>

Skills Management Dashboard

</td><td>

PRB1742662

</td><td>

In the Skills Management Dashboard, a 'Request failed with status code 401' error is visible

</td></tr><tr><td>

SOAP Web Service

</td><td>

PRB1748918

</td><td>

The serialization of XMLNode in the SOAP response uses a string representation instead of XML elements

</td></tr><tr><td>

Software Asset Data Import

</td><td>

PRB1672814

</td><td>

SAM Pro - Issue on Software Entitlement Import with the **Lease Contract** field

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1638689

</td><td>

The business rule 'Bookkeeping for dedup on delete' does not check the normalization status of installs

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1773110

</td><td>

SAMCoreCompanyUtil\(sams\) uses the **use\_when\_reporting** field introduced in Software Asset Management - Professional \(SAMP\)

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1605569

</td><td>

Microsoft License Statement \(MLS\) imports result in entitlement import errors for most per-core product definitions even when the rights per license is specified

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1748866

</td><td>

The sys\_object\_source table grows indefinitely with invalid records as records are deleted from the cmdb\_sam\_sw\_install table

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1754090

</td><td>

When assigned\_to is changed on CI it doesn't update in software installations when assigned\_to changes are empty

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1756212

</td><td>

Discovery models normalized using pattern rules do not get updated when a new package rule is shipped

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1666851

</td><td>

The condition field doesn't recognize 'custom' field choices in the 'Software Install Condition' from the Software Model form

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1745015

</td><td>

Issues with 'CancelExistingWorkflow' in 'sn\_samp.SAMPReclamationUtil' querying the field type 'Document ID'

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1746299

</td><td>

The **Run As** field is not empty in the 'Proactively fix core company reference' scheduled job

</td></tr><tr><td>

Software Asset Management Content Service

</td><td>

PRB1705952

</td><td>

Default values on the sam\_sw\_product\_lifecycle table are not set for source, lifecycle\_type, risk, and active fields

</td></tr><tr><td>

Software Asset Management Content Service

</td><td>

PRB1718826

</td><td>

Users are unable to opt in to the Software Asset Management content service

</td></tr><tr><td>

Software Asset Management Publisher Pack for SAP

</td><td>

PRB1762414

</td><td>

Users observe the error 'Script: SAPImportWorker: Connection name CUQ failed with error \[com.ctc.wstx.exc .WstxLazyException\]'

</td></tr><tr><td>

Software Asset Management Workspace

</td><td>

PRB1719783

</td><td>

samp\_sw\_client\_access\_installed\_device doesn't have required ACLs

</td></tr><tr><td>

Software Asset Management Workspace

</td><td>

PRB1731963

</td><td>

License usage doesn't display publisher cards for recon results when the 'Publisher' filter is applied

</td></tr><tr><td>

Software Asset Management Workspace

</td><td>

PRB1732877

</td><td>

There's a new button on the 'list-report' page in Software Asset Management Workspace

</td></tr><tr><td>

Software Asset Management Workspace

</td><td>

PRB1761023

</td><td>

The Oracle DB options 'Unlicensed options' list view filter is misconfigured and displays no results

</td></tr><tr><td>

Software Asset Management Workspace

</td><td>

PRB1768651

</td><td>

The Oracle DB 'Unlicensed options' list view filter is incorrect when accessed from the product result

</td></tr><tr><td>

Software Asset Normalization

</td><td>

PRB1663147

</td><td>

'SAM - Normalize discovery models using machine learning' job fails for unavailable or mismatched content, even though the other models normalized properly

</td></tr><tr><td>

Software Asset Reclamation

</td><td>

PRB1747941

</td><td>

The 'SAM - Apply latest content changes' job fails when the reclamation candidate's description is empty

</td></tr><tr><td>

Software Asset Reclamation

</td><td>

PRB1748558

</td><td>

The 'SAM - Identify Blacklisted Software' job sets all the deny-listed or closed complete candidates to 'Awaiting revocation'

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1732207

</td><td>

After an upgrade to Utah or later, Delete SampRecord from Source Control caused a workday recon failure for an existing user

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1743395

</td><td>

The suite engine fails during suite processing in reconciliation

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1751750

</td><td>

Read replica lag on install table caused by Reconciliation

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1724665

</td><td>

There's an out of memory issue when generating a Windows SQL Infra report for Microsoft

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1734593

</td><td>

Microsoft recon fails when combos differ for virtual machines

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1734615

</td><td>

SuiteEngine performance improvement

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1765646

</td><td>

Visual Studio installs are inferred to Visual Studio 2022 due to missing suite components

</td></tr><tr><td>

Software Asset Reconciliation

</td><td>

PRB1762816

</td><td>

Stamp Cloud provider and cloud host type columns only for delta records on install table

</td></tr><tr><td>

Software Asset Success Portal

</td><td>

PRB1712038

</td><td>

Remove filters from the 'Health check' widget in Success Portal

</td></tr><tr><td>

Software Discovery

</td><td>

PRB1749963

</td><td>

The sa\_pattern\_prepost\_script 'Sync Installed Software' creates software installs records via discovery, even when the glide.discovery.software\_sccm\_managed system property is true

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1715780

</td><td>

Allocations on maintenance entitlement

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1728056

</td><td>

MLS bulk Import creates more records than needed for a suite

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1704061

</td><td>

CSM fields are displayed by default in the base instance Software Asset Workspace view for contracts

</td></tr><tr><td>

Software License Compliance Checker

</td><td>

PRB1691508

</td><td>

Display only Software Asset Management \(SAM\) Pro or SAM Enterprise in IT Asset Management licensing resource counts

</td></tr><tr><td>

Software Lifecycles

</td><td>

PRB1722917

</td><td>

Filters in the 'Lifecycle report' table aren't properly applied and no records are populated in a workspace

</td></tr><tr><td>

Software Lifecycles

</td><td>

PRB1739133

</td><td>

The 'End of Life products' widget in Software Asset Overview dashboard has an incorrect filter

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1741485

</td><td>

Changes to various records aren't available for the 'Compare with committed' operation when committing changes

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1772875

</td><td>

Operation latch wasn't released after importing an application through Source Control

</td></tr><tr><td>

Standard Change Catalog

</td><td>

PRB1702225

</td><td>

Operator selection in the condition builder is not displayed for the 'List Collector' variable when there is a 'custom with label' type variable next to it

</td></tr><tr><td>

Standard Change Catalog

</td><td>

PRB1740549

</td><td>

In Next Experience, the introduction of a variable formatter to a standard change proposal results in editable change request values in 'Closed' and distorted change request values' styling

</td></tr><tr><td>

Subscription Management

</td><td>

PRB1694629

</td><td>

Users without BCM roles are shown in 'ua\_app\_usage' that they accessed tables

</td></tr><tr><td>

Survey Management

</td><td>

PRB1724829

</td><td>

If the user is using a different time format, incorrect dates are saved when a survey is submitted

</td></tr><tr><td>

Survey Management

</td><td>

PRB1724844

</td><td>

Survey Designer creates copies of a survey

</td></tr><tr><td>

Survey Management

</td><td>

PRB1737733

</td><td>

Inactive metrics are still visible in the native UI, but not in the portal

</td></tr><tr><td>

Survey Management

</td><td>

PRB1750502

</td><td>

The Outlook actionable messages checkbox in Quiz Designer does not work as expected

</td></tr><tr><td>

Survey Management

</td><td>

PRB1761114

</td><td>

There's inconsistency between the native UI and portal/mobile in the **percent\_answered** field in the 'Assessment instance' table

</td></tr><tr><td>

Survey Management

</td><td>

PRB1781172

</td><td>

Selecting the 'Next' button on the Survey Deprecated widget doesn't progress to the next question

</td></tr><tr><td>

Syntax Editor

</td><td>

PRB1717790

</td><td>

With the new scripting tools in Vancouver, syntax editor macros aren't loading correctly all the time

</td></tr><tr><td>

Syntax Editor

</td><td>

PRB1622389

</td><td>

There is no way to format an XML field in Script Editor

</td></tr><tr><td>

Syntax Editor

</td><td>

PRB1680139

</td><td>

Word wrap does not work in script editor

</td></tr><tr><td>

Syntax Editor

</td><td>

PRB1711483

</td><td>

Typedefs for known parameters aren't loaded in an editor

</td></tr><tr><td>

System Archiving

</td><td>

PRB1660184

</td><td>

Filter out a restored record when creating an archive chunk

</td></tr><tr><td>

System Archiving

</td><td>

PRB1751060

</td><td>

Job Consumer runs for days in all environments \(Chunks are marked incorrectly with error state\)

</td></tr><tr><td>

System Archiving

</td><td>

PRB1590786

</td><td>

Creation of a new archive rule on larger tables times out before completion

</td></tr><tr><td>

System Archiving

</td><td>

PRB1711734

</td><td>

ACL inheritance on archived tables isn't working as expected

</td></tr><tr><td>

System Events

</td><td>

PRB1773866

</td><td>

Event XMLstats Endpoint errors out due to an incorrect structure

</td></tr><tr><td>

System Export Sets

</td><td>

PRB1729204

</td><td>

When a null point error is thrown in an export set execution, an export's set state and logs aren't reflected in the export history

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1727212

</td><td>

Data Loader and some other fields are removed from the form section in sys\_data\_source

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1694394

</td><td>

ImportSetCleaner Script include performs gs.print to syslog excessively

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1754292

</td><td>

The import job transformer is stuck in the 'Running' state when the node restarts

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1736383

</td><td>

A data stream action field doesn't populate in the Data Source page

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1717629

</td><td>

sys\_documentation records are not deleted when the change is published to AppRepo from the source and the app is installed on the target

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1764439

</td><td>

An update set preview is canceled when there are duplicate names within the hierarchy and the instance uses a Postgres database

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1752200

</td><td>

Form sections defined in a domain do not coalesce when deployed via update set

</td></tr><tr><td>

System Web Services

</td><td>

PRB1515820

</td><td>

Table API adds 'api=api' to queries which causes issues when a table has a column named 'api'

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1650626

</td><td>

**Data Management** &gt; **Update with Preview** doesn't work on journal fields

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1755862

</td><td>

There should be a default ordering by sys\_id on all metadata tables and a few non-metadata tables

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1513819

</td><td>

Utterances' text is not formatted when tokenized languages are exported

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1655722

</td><td>

The 'Updated' date on LDAP Scheduled Imports updates to today when using 'Execute Now' for the first time after Tokyo upgrade

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1719787

</td><td>

The condition checker for the **Table** field is set to empty when the maximum length of the table is more than 40 characters

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1725932

</td><td>

Users can assign delegates or users to inactive users even though the fields' reference qualifier condition is set to 'active=true^EQ'

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB1706024

</td><td>

When read replicas are configured and there is replication lag, a table cleaner can 'spin' for long periods of time trying to delete non-existent records

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB1722902

</td><td>

TableCleaner isn't deleting sys\_audit and the **sys\_journal\_field** for the 'TPH' table when the options are enabled

</td></tr><tr><td>

Technology Reference Model

</td><td>

PRB1737818

</td><td>

When users fetch the product models from the application service, the software product does not appear even if there are technical debts

</td></tr><tr><td>

Territory Planning

</td><td>

PRB1732080

</td><td>

There are issues with adding matching attributes in the geography type in workspace

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1711394

</td><td>

Using Time Sheet Portal on FireFox prevents users from selecting the 'dropdown' menu for the resource plan field

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1724449

</td><td>

A recalled time card uses the wrong exchange rates

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1746965

</td><td>

Users are unable to update the 'Time Card Grid' widget

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1676673

</td><td>

The previous month button on the calendar pop-up is not labeled

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1677471

</td><td>

Days of the week are announced by assistive technology as 'Sun', 'Mon', etc.

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1708797

</td><td>

A warning isn't displayed when a time card is recalled

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1731868

</td><td>

An update in 'Planned hours' on a resource allocation updates the actual cost in 'Project currency'

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1737941

</td><td>

JAWS does note read out task card fields in the Time Sheet Portal

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1759941

</td><td>

Time Sheet Portal tasks show all tasks when using priority sorting

</td></tr><tr><td>

Transaction Management

</td><td>

PRB1674646

</td><td>

API Response is 200, however the API call doesn't reach the application node

</td></tr><tr><td>

Transformer API

</td><td>

PRB1733790

</td><td>

TransformerStats grow unbounded, causing heap memory pressure

</td></tr><tr><td>

Transformer API

</td><td>

PRB1722879

</td><td>

ComplexObjectCollection serializes empty arrays with an empty element

</td></tr><tr><td>

Transformer API

</td><td>

PRB1712812

</td><td>

The JSON parser drops negative numbers in arrays

</td></tr><tr><td>

Transformer API

</td><td>

PRB1759136

</td><td>

The Integration Hub DataStream Action Rest API pagination for XML Response does not work as expected

</td></tr><tr><td>

UI Actions

</td><td>

PRB1696768

</td><td>

Workspace View rules are not applied when form is reloaded with g\_form.reload\(\) in UI action

</td></tr><tr><td>

UI Actions

</td><td>

PRB1667469

</td><td>

An override is created automatically when the user opens a UI Action

</td></tr><tr><td>

UI Actions

</td><td>

PRB1667945

</td><td>

action.setredirect isn't working on a Workspace list

</td></tr><tr><td>

UI Actions

</td><td>

PRB1765220

</td><td>

In Next Experience, the **Remove** button in an attachment dialog no longer has a border

</td></tr><tr><td>

UI Builder

</td><td>

PRB1734100

</td><td>

Group assigned roles aren't honored by UI Builder

</td></tr><tr><td>

UI Builder \(Family Channel\)

</td><td>

PRB1737069

</td><td>

Agent Assist in a configurable workspace does not have scroll bars for knowledge articles containing tables in the article body

</td></tr><tr><td>

UI Builder \(Family Channel\)

</td><td>

PRB1711393

</td><td>

In Utah and Vancouver, the same theme styling appears differently for dashboard tabs than in Tokyo

</td></tr><tr><td>

UI Builder \(Family Channel\)

</td><td>

PRB1717633

</td><td>

**Expand**, **collapse**, and **Show all** buttons in the table aren't accessible through the keyboard

</td></tr><tr><td>

UI Builder \(Family Channel\)

</td><td>

PRB1732414

</td><td>

Pages load slowly with 150+ elements

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1695153

</td><td>

The date and time picker are not displayed in forms where the user has set the preference for date format as dd.MM.yyyy

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1763085

</td><td>

Differences in autocomplete sorting for reference fields in Workspace vs Platform view

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1737805

</td><td>

@ mention doesn't work in Workspace with RTE off

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1683899

</td><td>

The user can't add an image to a mandatory field of type 'Image' or 'Attachment'

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1742370

</td><td>

Resizing the modal of 'Assignment group' will collapse the layout

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1710200

</td><td>

The 'Total time' and 'Time worked' history is not displayed correctly upon updating 'Time Worked'

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1727082

</td><td>

In the article type 'Wiki', an &lt;h2&gt; header is not visible in edit/preview mode

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1731070

</td><td>

The **Time worked** field doesn't work properly in Workspaces when two users are working on the same Task simultaneously, and one user saves the Task

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1674332

</td><td>

Screen readers won't narrate any information when the focus moves to link content

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1739850

</td><td>

In Workspace \(both legacy and configurable\), the tree picker for a reference look-up field shows an empty modal when glide.invalid\_ query.returns\_no\_rows is set to true

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1752376

</td><td>

When viewing a KB article in Edit view, selecting any of the tabs at the bottom jumps to the KB content instead of staying down at the tabs

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1756977

</td><td>

'Index 1 out of bounds for length 1' error in Workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1596670

</td><td>

Invalid input isn't announced by assistive technologies

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1648730

</td><td>

The mandatory asterisk appears for a field that is set as read-only via the ACL

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1698505

</td><td>

The **Phone number** type field saves inconsistently in Platform but not in Workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1699158

</td><td>

Section heading is announcing additional items being concatenated with Screenreader \(NVDA\)

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1711497

</td><td>

A reference variable's 'preview' window size in the 'Variables' editor is smaller than the other reference field's 'preview' window sizes in the 'Requested Item' form

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1714549

</td><td>

The value of the **Short Description** field doesn't display when the value starts with '@' and contains '/'

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1715716

</td><td>

A live update doesn't work as expected on a list field when the field is set to read-only via the dictionary entry override

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1717782

</td><td>

e164 phone numbers on any table fail to save correctly when 'Other/Unknown' is selected

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1718953

</td><td>

Reference field type-ahead transactions aren't cancelable in Customer Service Management \(CSM\)/Field Service Management \(FSM\) configurable workspaces

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1721196

</td><td>

The field label of a wiki type field is displayed with a grey background color

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1731626

</td><td>

In Vancouver, a script include isn't called for the reference dictionary entry if the choice list specification is 'Dropdown' set with 'None'

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1731871

</td><td>

When updating the **Phone Number \(E164\)** field, the prefix \(country code\) unexpectedly loses focus and scrolls to the next form section in a configurable workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1734859

</td><td>

@Mentions don't let users search for users with '\(' as a special character in their name

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1734907

</td><td>

The **Phone Number \(E164\)** field type is broken for non-admin users

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1736621

</td><td>

While closing the problem to the 'Risk Accepted' state, the field name **Risk Accepted Reason** label is misaligned

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1737421

</td><td>

Unable to select a date before 1970 from the calendar popover in UI16

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1737453

</td><td>

The **Life Cycle Stage** and **Life Cycle Status** fields do not accept values when entered in a language other than English

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1737778

</td><td>

The Currency2 field value completes itself with the value 'true'

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1740210

</td><td>

The list collector 'None' placeholder is recognized as an option when the language is switched to German

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1742055

</td><td>

Double-clicking on the date picker in the **Date/Time** field selects an invalid date

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1742230

</td><td>

Long field labels are truncated/hidden in UI16

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1750483

</td><td>

When viewing user records as a non-admin ITIL user in Service Operations Workspace, the phone number and mobile phone number fields prefix the phone number with an extra 1

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1756737

</td><td>

@mentions are not selected when users tab-press, but they are selected through arrow buttons

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1758221

</td><td>

'Index x out of bounds for length x' error and users are unable to save or update a record when a **Glide\_List** field is modified with a value lacking a display value

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1642153

</td><td>

Dependent choices do not work as expected in Agent Workspace when using a Client Script to set and clear options

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1734435

</td><td>

The cursor jumps around when trying to rename an attachment name while attaching it to a record in workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1745712

</td><td>

Different behavior ACL evaluation template Workspaces/UI16 forms \(native\) in relation to the current object

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1757057

</td><td>

The **Applies to** field doesn't display any values in Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1721247

</td><td>

In CSM/FSM Workspace, the 'After' business rule doesn't insert records when the field is hidden

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1735528

</td><td>

Form onChange doesn't work properly in Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1742034

</td><td>

The 'Copy Permalink' pop-up \(Copied to Clipboard\) is not translated when selected within the Knowledge Article that is opened from the Knowledge home

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1746742

</td><td>

The **Entity View Action Mapper \(EVAM\)** table field list doesn't populate for tables extending 'Variable'

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1753812

</td><td>

The length of the 'Handled events' column on the 'sys\_ux\_macroponent' table needs to be increased to avoid truncation of data on Oracle DB

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1774006

</td><td>

In a workspace, the 'onLoad' UI policy isn't working on a save

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1670764

</td><td>

When a pop-up modal is closed, the page loads twice in a configurable workspace if the instance is domain separated

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1686691

</td><td>

New Form layouts are dynamically created by opening a record

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1700565

</td><td>

Resolve UI Action does not save the **Time Worked** field value

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1703974

</td><td>

Special handling notes with a large amount of text cause overflow beyond the modal container

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1717532

</td><td>

Using a base instance variable formatter on a custom table \(not extended from a Task\) does not open the form in Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1718533

</td><td>

The g\_user.getClientData\(\) API doesn't work properly on Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1723383

</td><td>

A missing empty table check is causing an undefined page route on 'Create article'

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1730199

</td><td>

'Reload form' in workspace doesn't load special handling notes \(SHN\)

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1754719

</td><td>

Failure to load Planning Items with a custom Scoring Framework where the attribute name contains '/'

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1708619

</td><td>

There's an advanced reference qualifier issue in the Playbook experience

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1708645

</td><td>

If a user enters 'NULL' in a string field and saves it, the field is empty even if it's a required field

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1708689

</td><td>

setError\(\) doesn't work in configurable workspaces

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1711630

</td><td>

user.view events are created unexpectedly for the 'DB' view and go into an error state

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1712024

</td><td>

The focus on the first field on a form isn't working as expected

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1718196

</td><td>

The read-only 'Time worked' value isn't displayed correctly after a live update

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1720326

</td><td>

Attributes that begin with 'aria-' aren't valid ARIA attributes

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1721805

</td><td>

There's an unexpected update to a read-only HTML field

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1727325

</td><td>

Tooltips aren't hoverable and can't be dismissed using the keyboard

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1727883

</td><td>

A required dot-walk reference field causes an issue in Agent Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1728214

</td><td>

Modifying an annotation on a 'Extension table' form can break the annotation for the 'Parent table' form

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1731022

</td><td>

The dictionary entry of the **Attributes** field is incorrect for the 'Rate Model' attribute

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1731624

</td><td>

The error messages when uploading deny-listed attachments aren't translated to the session language

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1732230

</td><td>

The UI Builder form's configuration panel's 'View' parameter is overridden by the Form Controller 'View' parameter

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1734086

</td><td>

A required **Date** field can be submitted in the incorrect format with no validation error

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1738564

</td><td>

A ribbon component displays the page title as 'Contact'

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1744130

</td><td>

G\_form.clearvalue does not set the radio button value to its initial value

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1746695

</td><td>

The read-only URL field in a form allows focus and an inaccurate read out of the URL

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1751109

</td><td>

The focus on the 'Save changes' box is different when selecting the **Back** button and the **Open record** button on a preview window

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1754500

</td><td>

Table column headers are implemented incorrectly

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1769443

</td><td>

Event handling doesn't work on a 'UI action selected' event on an action bar component

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1773340

</td><td>

A field hint no longer displays for a boolean field when a field label URL is configured

</td></tr><tr><td>

UI Policies

</td><td>

PRB1714781

</td><td>

Selecting the **Add/Remove Multiple** button in a glide\_list type field lets users save the record with an empty value for a required field

</td></tr><tr><td>

UI Policies

</td><td>

PRB1728303

</td><td>

When adding an attachment for the **File Attachment** type field through the form level, required field values are wiped due to a UI policy which isn't related to the file attachment

</td></tr><tr><td>

Unified Filter

</td><td>

PRB1733858

</td><td>

Users aren't able to apply a value of a string field on a runtime filter

</td></tr><tr><td>

Universal Request

</td><td>

PRB1728269

</td><td>

Archiving universal records is removing the attachments, causing admin users to not be able to see the attachment on archive universal records

</td></tr><tr><td>

Universal Request

</td><td>

PRB1733855

</td><td>

In the 'Universal request' ACL, there's a typo in the script

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1708147

</td><td>

Selecting 'Save Merge' when resolving a skipped record doesn't save the changes

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1733935

</td><td>

The progress bar on upgrade monitor page doesn't refresh

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1734654

</td><td>

Records in an upgrade preview display as 'Predicted Update' or 'Insert', but in the builder instance display as 'Skipped'

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1750401

</td><td>

Frequent warnings during an upgrade

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1770432

</td><td>

Whitelists that contain a list of elements that can be edited on a merge form don't include CSS variables and quick start configurations

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1741917

</td><td>

GCFCollector code throws many errors due to incorrect parsing of transaction sources

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1764167

</td><td>

When users upgrade from a pre-Vancouver release to the Vancouver release, User Consent Migration encounters a null pointer exception \(NPE\) in some scenarios

</td></tr><tr><td>

User Criteria for Service Catalog

</td><td>

PRB1766975

</td><td>

Default roles such as snc\_internal and snc\_external aren't honored properly for user criteria in portals, when roles are relegated in a session with the 'Zero Trust Access' feature

</td></tr><tr><td>

User Criteria for Service Catalog

</td><td>

PRB1771899

</td><td>

Using an email address denies access to a catalog item on a portal

</td></tr><tr><td>

User Role Inheritance API

</td><td>

PRB1692615

</td><td>

Marking inherits to false for a sys\_group\_has\_role may temporarily leave sys\_user\_has\_role records with an inheritance count of 0 ​

</td></tr><tr><td>

UX Framework

</td><td>

PRB1736722

</td><td>

A portion of the pom file for glide-ux-builder/pom.xml no longer exists when moved, and is causing a partial upgrade issue

</td></tr><tr><td>

UX Framework

</td><td>

PRB1745673

</td><td>

The 'New HR Case' tab is not closed once users selects the Cancel and discard option in HR Agent Workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1713439

</td><td>

Associating records in Service Operations Workspace isn't working as expected

</td></tr><tr><td>

UX Framework

</td><td>

PRB1735486

</td><td>

Activity logs provide intermittently incorrect information

</td></tr><tr><td>

UX Framework

</td><td>

PRB1732332

</td><td>

When a user opens a service map from the 'Service' dashboard, the page turns into 'Service details'

</td></tr><tr><td>

UX Framework

</td><td>

PRB1736030

</td><td>

'Audiences' on a landing page does not work as expected

</td></tr><tr><td>

UX Framework

</td><td>

PRB1652455

</td><td>

In a configurable workspace, a dirty form message is encountered on a form due to its modal, even when the modal is already closed

</td></tr><tr><td>

UX Framework

</td><td>

PRB1688293

</td><td>

On the CSM Workspace 'Interaction' page, there's a mismatch between the selected tab and the tab content that's displayed

</td></tr><tr><td>

UX Framework

</td><td>

PRB1718386

</td><td>

The template tab misaligns in the side panel when 'Show the sidebar' is disabled in CSM Workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1720924

</td><td>

On Service Operations Workspace's Agent Assist, the resource list title and contextual search resets after navigating to another contextual sidebar component

</td></tr><tr><td>

UX Framework

</td><td>

PRB1604829

</td><td>

sys\_ux\_page\_registry.title isn't translatable

</td></tr><tr><td>

UX Framework

</td><td>

PRB1662699

</td><td>

The nav menu is missing the available green checkmark icon when the page loads if the agent has not checked all service channels in configurable workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1678831

</td><td>

UIB Login component doesn't allow for switch to SSO properly

</td></tr><tr><td>

UX Framework

</td><td>

PRB1695799

</td><td>

Failed 4xx/5xx HTTP requests display an obtrusive modal in Vancouver

</td></tr><tr><td>

UX Framework

</td><td>

PRB1697508

</td><td>

Isolate the UIScript query from Form GQL and cache the response

</td></tr><tr><td>

UX Framework

</td><td>

PRB1697766

</td><td>

Leave the site pop-up when trying to download an attachment in workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1714039

</td><td>

The **Back** button in iFrame doesn't work when opened in a configurable workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1718453

</td><td>

Users are unable to create domain-specific UX page properties in a domain-separated instance

</td></tr><tr><td>

UX Framework

</td><td>

PRB1719613

</td><td>

The CONTENT\_UPDATED event isn't updating the URL parameters from the second time

</td></tr><tr><td>

UX Framework

</td><td>

PRB1720621

</td><td>

sn-canvas-toolbar is hidden after resizing in Asset Workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1721676

</td><td>

A screen reader isn't announcing the selected state of the tab controls with the role of 'Menu items'

</td></tr><tr><td>

UX Framework

</td><td>

PRB1722451

</td><td>

The UX add-on 'Event Mapping' is cached, but shouldn't be

</td></tr><tr><td>

UX Framework

</td><td>

PRB1724469

</td><td>

Screen macroponents are created without data 'nowAppProps'

</td></tr><tr><td>

UX Framework

</td><td>

PRB1727218

</td><td>

There's a layout issue in Software Operations Workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1727277

</td><td>

Aria-hidden elements are focusable and contain focusable elements

</td></tr><tr><td>

UX Framework

</td><td>

PRB1727683

</td><td>

The **Home** and **Cart** buttons lack accessible names

</td></tr><tr><td>

UX Framework

</td><td>

PRB1732250

</td><td>

Sidebar tabs are cut/hidden when the browser width shrinks, or when a user zooms in

</td></tr><tr><td>

UX Framework

</td><td>

PRB1733426

</td><td>

In the Hebrew version of an instance, the **Currency** field on the 'Payroll' table isn't accepting a number even if it's a real number

</td></tr><tr><td>

UX Framework

</td><td>

PRB1742312

</td><td>

The test step to open a new form gives the error 'GraphQL API - GlideGraphQL: documents list does not contain valid document records: com.glide.graph'

</td></tr><tr><td>

UX Framework

</td><td>

PRB1747422

</td><td>

The inactive tab label is not able to switch to the correct language after the user changes the language

</td></tr><tr><td>

UX Framework

</td><td>

PRB1749701

</td><td>

'Cannot deserialize value of type Lcom.glide.ux.runtime.model.v\_1\_0\_0.MacroponentProperty' warning when creating a user session or navigating to the workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1752849

</td><td>

The 'Close Dialog' modal isn't translated

</td></tr><tr><td>

UX Framework

</td><td>

PRB1757522

</td><td>

The cache does not watch the changes made on the **extension\_point** field of the sys\_ux\_app\_route table

</td></tr><tr><td>

UX Framework

</td><td>

PRB1760476

</td><td>

In Agent Workspace for HR Case Management, highlighted value colors are faded in the form header

</td></tr><tr><td>

UX Framework

</td><td>

PRB1762333

</td><td>

Selecting 'Open issues' from a risk assessment's reference information causes an internal server error \(500\)

</td></tr><tr><td>

UX Framework

</td><td>

PRB1778611

</td><td>

In the 'Customer Success' workspace, adding a comment or a work note to a case causes a hidden contextual side panel to unhide itself

</td></tr><tr><td>

UX Framework

</td><td>

PRB1776899

</td><td>

Keyboard shortcuts aren't working in Service Operation Workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB1773935

</td><td>

Workflow Studio displays an empty page when opening in a private Firefox browser

</td></tr><tr><td>

UX-Metrics

</td><td>

PRB1717321

</td><td>

Data for Total UI Time and Interruption aren't populated \(neither in list nor form layout\) on the Client Interaction

</td></tr><tr><td>

Vendor Management Workspace \(Family\)

</td><td>

PRB1733000

</td><td>

The status should be 'positive' in VendorInsightsUtil .getKPIGroupThreshold\(\)

</td></tr><tr><td>

Vendor Management Workspace \(Family\)

</td><td>

PRB1736751

</td><td>

Activities on some vendors run every night and fill up the log tab

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1586394

</td><td>

In a Virtual Agent topic, getDisplayValue does not work for the reference input when the count is more than 10

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1748942

</td><td>

A reference question with a single choice erroneously shows the question type in the label

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1645117

</td><td>

The 'Conversation Task' table name is incorrect

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1732454

</td><td>

The LiveAgent\_interaction\_id variable is not populated when a conversation is initiated via contextual action

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1741509

</td><td>

ActiveTopicTypesCache consumes a lot of memory

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1720318

</td><td>

A Virtual Agent topic with a text response node that contains a rich text message with a text link generates a mismatched token when an ATF test step is executed, causing a test step failure

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1753464

</td><td>

An initial search text is encoded in Agent Chat and the conversation context

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1723142

</td><td>

ServiceNow Accessibility Topics to be compliant with WCAG 2.1 Level A

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1731428

</td><td>

Loading dots for Live Agent are static and don't jump when waiting for the agent to pick up chat

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1732726

</td><td>

RuntimeUtils fetches conversations with tasks

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1745771

</td><td>

Users that do not have a consumer account do not receive a pop-up or indicator that a notification has arrived

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1748960

</td><td>

Sys\_one\_extend\_ builder\_capability records are mistakenly deleted during upgrade

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1765722

</td><td>

The Virtual Agent table bot response card isn't displaying all data properly after upgrading to Washington/Vancouver

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1770638

</td><td>

Agent chat is unable to render a chat when json cards are in a Virtual Agent conversation

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1720128

</td><td>

LinkUnfurlingMessageResponse messages aren't marked as processed

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1726791

</td><td>

Web Client can send multiple contextual action requests

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1730730

</td><td>

The multi-link output has a link header followed by description text, but the description text is truncated to a single line and only hovering over it displays the full content

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1731157

</td><td>

The VAAISearchHelperUtah. calculateResultsTo DisplayWithContext\(\) method is missing in Vancouver

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1731831

</td><td>

In Virtual Agent, users are unable to translate the node name of a topic step

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1733286

</td><td>

An utterance isn't translated after going through language detection

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1735922

</td><td>

Virtual Agent 'Lite' topics are editable

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1740562

</td><td>

The 'Disconnected Chat Timeout' scheduled job should run as system, not admin

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1741127

</td><td>

Console warning logs caused by Virtual Agent not sending UI preferences to Next Experience Design System \(NDS\)

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1742734

</td><td>

The Agent Chat pop-up card uses an incorrect version of the KB article when using the copied permalink

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1745704

</td><td>

On-change handlers are always running, even if the changed variable does not exist in the conditions

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1746854

</td><td>

The chat is ended abruptly while initiating the autopilot topic during a live agent conversation through Virtual Agent Designer

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1746867

</td><td>

Virtual Agent's \(VA\) 'Abandoned chat' scheduled job short-circuits if it is unable to fault a conversation

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1747075

</td><td>

The greeting message passed in 'vaSystem.send TopicPickerControl \(greetingMessage\)' is present in the transcript of a chat initiated from the portal but not in the chat initiated from the team

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1757702

</td><td>

Conversations with empty device types are not faulted

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1760141

</td><td>

Users are unable to enable 'Make this input secure' on topic block

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1760676

</td><td>

Actionable notifications for 'LLM' mode with an LLM topic in action are received in non-LLM mode as well

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1762623

</td><td>

When multiple topic blocks are called, the topic block does not return to the parent topic

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1766440

</td><td>

The Virtual Agent conversation fails when a topic block that contains an apostrophe in the name is called

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1767655

</td><td>

The feature name in sys\_gen\_ai\_usage\_log is shown as 'Case Summarization'

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1767767

</td><td>

Chat summarization displays an empty agent message screen when transferring to a live agent

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1770948

</td><td>

In Virtual Agent, an action utility doesn't display all the relevant flow actions

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1770961

</td><td>

A transcript/internal transcript displays 'Unable to generate transcript' when the request catalog item inline-seismic topic block is used in Live Agent's auto-pilot

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1777529

</td><td>

Selecting 'Continue this topic' doesn't resume the topic but closes the conversation

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1781543

</td><td>

Survey returns an incorrect value in Virtual Agent

</td></tr><tr><td>

Virtual Agent Actionable Notifications

</td><td>

PRB1766713

</td><td>

If the previous notification conversation didn't have the global\_requester \_session\_language context variable, notifications aren't triggered

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1732898

</td><td>

The 'Properties' page is loading slowly in Virtual Agent Designer

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1761215

</td><td>

Highest-scored intent isn't picked up by the Virtual Agent \(VA\)

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1677132

</td><td>

The base instance topic 'Open IT Ticket 2.0 \(Template\)' doesn't work when it is being cloned

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1731958

</td><td>

Users shouldn't need to turn on the 'NAP' panel to create large language models \(LLM\) topics

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1750902

</td><td>

Virtual Agent directs to an error topic after receiving a response with Array.Object from Flow Designer

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1751801

</td><td>

The topic node name with special characters does not appear in 'Task Context,' causing non-availability of the topic node for funnel creation on the Virtual Agent Dashboard

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1758646

</td><td>

An LLM dynamic choice node needs to access the variable's value through getValue\(\)

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1761780

</td><td>

The 'Saved test' badge in the test window is cut off

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1762445

</td><td>

Virtual Agent uses variable names in the conversation instead of node names

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1766448

</td><td>

Carousel cards with translations don't display on Virtual Agent

</td></tr><tr><td>

Virtual Agent Designer

</td><td>

PRB1773483

</td><td>

A warning message displays 'Now Assist in Virtual Agent' instead of 'Now Assist in Virtual Agent Designer'

</td></tr><tr><td>

Virtual Agent for Service Portal

</td><td>

PRB1714291

</td><td>

A Virtual Agent screen reader is unable to announce the full response coming from the virtual agent

</td></tr><tr><td>

Virtual Agent third-party integrations

</td><td>

PRB1762476

</td><td>

The Virtual Agent/Microsoft Teams connection is unable to find records and options when an interaction is started

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1743948

</td><td>

VA Web client shows a blank screen when multiple tabs are open

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1772481

</td><td>

Reducing the browser width &lt;600 makes the web-client full-screen

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1744826

</td><td>

The **End Conversation** button is not disabled after the user selects it

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1745475

</td><td>

The Virtual Agent **Close** icon is cut off when using on mobile

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1761699

</td><td>

When the user begins typing in the chat of Engagement Messenger on an iOS device, the page automatically zooms in

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1762856

</td><td>

The Virtual Agent 'Show 10 More' UI control isn't responding to Automated Test Framework \(ATF\)'s custom UI 'Click on Component'

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1763654

</td><td>

Setting glide.vtb.card\_select\_ due\_date.dst\_convert to false doesn't prevent an extra hour from unexpectedly adding

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1632630

</td><td>

HTML special characters are not shown correctly

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1747150

</td><td>

Visual Task Boards \(VTB\) have no limits on attachments, which can lead to slow loading, memory issues, and semaphore exhaustion with excessive attachments

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1729596

</td><td>

An activity stream is stuck when opening a card from a virtual task board \(VTB\)

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1739939

</td><td>

Visual Task Board \(VTB\) cards display an inaccurate number of tasks

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1744873

</td><td>

The **Conditions** type field does not honor the operators 'does not have' and 'excluding' for a Tags field on the form view even when these options are available in the condition builder v2

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1722390

</td><td>

In a scheduled job, the interaction state change for a walk-up is executed, but the script remains in the sysauto\_script table

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1737053

</td><td>

In Walk-up Experience, the walk-up appointment state is updated twice

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1738315

</td><td>

Walkup experience fields are loading slowly in the Now Mobile app

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1761510

</td><td>

The carousel is broken on the Onsite 'Queue' page

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1769107

</td><td>

The **Schedule appointment** button isn't available when right-clicking then pasting for the **Reason description** field

</td></tr><tr><td>

Walk-up Experience Appointment Booking

</td><td>

PRB1746504

</td><td>

The function logError is not allowed in scope sn\_walkup, with gs.error\(\) used instead

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1737763

</td><td>

Accessibility section of settings menu - Screen reader is not announcing the correct Name for 'Info button'. It is announced as 'section'

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1716138

</td><td>

List mark-up is used incorrectly

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1724967

</td><td>

In Virtual Agent, focus is lost when selecting a choice

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1748991

</td><td>

The JAWS reader does not announce the title and text within dialog content, other than the interactive elements like 'Close,' 'Cancel,' and 'Remove'

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1759881

</td><td>

The user interface for sidebar discussions and discussion chats are not fully accessible

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1759886

</td><td>

The chat-bubble-icon has its own tab index even though it cannot be interacted with, leading to the user not being able to open the discussion chat using only the Tab key

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1759888

</td><td>

The user interface for Sidebar discussion and discussion chat is not fully accessible

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1759889

</td><td>

The user interface for a sidebar discussion and discussion chat isn't handicapped accessible

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB1763812

</td><td>

The user interface for a sidebar discussion and discussion chat is not fully accessible

</td></tr><tr><td>

Web UX Runtime

</td><td>

PRB1739325

</td><td>

A user with elevated privileges can't edit glide.ui.restore.previous.session.tabs

</td></tr><tr><td>

Workflow Contexts

</td><td>

PRB1725402

</td><td>

The Workflow Scratchpad Encryption plugin does not work properly after migration in a Vancouver upgrade

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1747917

</td><td>

The travel line indicator for 'Closed Complete' tasks and 'Incomplete' tasks aren't visible on Dispatcher Workspace \(DWS\)

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1719047

</td><td>

Users are unable to suspend HR cases after upgrading to Vancouver

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1739619

</td><td>

When a user attempts to update the **Assignment Group** and **Assigned to** fields, they are cleared out

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1761006

</td><td>

The Field Service Management \(FSM\) Configurable Workspace plugin adds functions and function instances to the FSM application

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1768728

</td><td>

Users are unable to publish existing work order document templates after editing

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1744192

</td><td>

Some of the 'Closed Complete' or 'Incomplete' tasks with expected\_travel\_start are out of range of endDate

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1754204

</td><td>

'Copy Task Template...' fails when too many tasks are added on the work order template

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1759426

</td><td>

The Field Service Management plugin takes a long time to install when the sys\_user table is large

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1762739

</td><td>

Field Service Management \(FSM\) work task flows aren't in English

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1765374

</td><td>

The 'Remove' business rule restricts agent schedule users on creation

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1769179

</td><td>

There is an error message for community users on the community\_profile page when the user timezone is updated

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1770620

</td><td>

Work order tasks that are created from work plans don't have with the correct window end date

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1776096

</td><td>

A bundle created by bundling work order tasks have the same short description of 'Bundle\_'

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1762854

</td><td>

The Global Search display message is broken in Core UI

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1628953

</td><td>

For the global search in Agent Workspace, the column label's translation ignores special characters and upper cases

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1655206

</td><td>

After selecting 'View all knowledge matches' from the global search results, the search group conditions are not honored in the knowledge.do results

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1677355

</td><td>

Text Index Group Configuration

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1724173

</td><td>

Text indexing on a PDF attachment causes an out of memory error

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1731509

</td><td>

Add the capability to turn off the zing binary operator 'AND/OR/NOT'

</td></tr></tbody>
</table>**Parent Topic:**[Available patches and hotfixes](../available-versions.md)


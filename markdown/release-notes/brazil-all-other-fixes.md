---
title: All other Brazil fixes
description: The Brazil release contains important problem fixes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/brazil-all-other-fixes.html
release: brazil
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 188
breadcrumb: [Available patches and hotfixes, Learn about the Brazil release, Brazil release notes]
---

# All other Brazil fixes

The Brazil release contains important problem fixes.

-   **Brazil was released on September 24, 2026.**
    -   09-22-2026\_1636
    -   glide-brazil-08-25-2026\_\_patch0-08-26-2026

**Important:** For more information about how to upgrade an instance, see [ServiceNow upgrades](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/upgrade.md).

For more information about the release cycle, see the [ServiceNow Release Cycle](https://support.servicenow.com/kb_view.do?sysparm_article=KB0547244).

**Note:** This version is being evaluated for use in the ServiceNow Government Community Cloud \(GCC\) environment.

For a downloadable, sortable version of the fixed problems in this release, click [here](https://downloads.docs.servicenow.com/enus/brazil/rn/patches/PRBs-B00.00.xlsx)

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

PRB1939961

</td><td>

An incorrect class is passed as context to an ACL

</td></tr><tr><td>

Access Control

</td><td>

PRB2001648

</td><td>

A 'Decision' type field is missing from an ACL form on an Australia zboot instance

</td></tr><tr><td>

Access Control

</td><td>

PRB1959980

</td><td>

The Wildcard field ACL in the scoped app automatically changes the field from .\* to none when switching scopes to edit

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2022330

</td><td>

Custom journal\_input field values are not displayed on Service Portal Ticket Conversational widget after Australia upgrade

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2040417

</td><td>

The **Copy** button on the VTB view can't access copyJournalContent or GlideUIDefault

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2010277

</td><td>

Text is removed when typing fast in Robust Transform Engine \(RTE\) in Service Operations Workspace \(SOW\)

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2015217

</td><td>

An @mentioned user in the activity stream is appearing as having access, even though they don't have access to the record

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2032409

</td><td>

Activity generation does not comply with the carriage return on the generated text

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2010203

</td><td>

SysUserRepo should add setWorkflow\(false\) when querying the sys\_user table

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1865166

</td><td>

Empty comments are added to the Activity Stream on Service Operations Workspace and Agent Workspace

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2011352

</td><td>

The editor.config attribute isn't supported in Activity Stream RTE

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2013162

</td><td>

Add filter a configuration, such as a slushbucket

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2014091

</td><td>

Activity Stream field changes from different users can erroneously be grouped together on workspace under certain conditions

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2015105

</td><td>

A small race window was introduced in SysActivityRepo

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2019754

</td><td>

When copying rich text into the TinyMCE editor from the clipboard, some formatting isn't preserved

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2020348

</td><td>

A user profile pop-up isn't displaying on a comment after refreshing for previous comments

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2027954

</td><td>

An activity filter's field's slushbucket initially has every field selected when the glide.ui.\{table\}\_activity.fields property doesn't exist

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2029963

</td><td>

The **Copy** button for Journal entries does not work in List Activity Stream view

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2032977

</td><td>

A different user name is displayed on workspace when multiple users\[sys\_user\] have the same email address

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2060131

</td><td>

When table rotation is set up for sys\_audit\_relation, audit relationship events don't display in a workspace

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1905898

</td><td>

A hint for 'Comments' is announced for the Work Notes on CSM Workspace and on Service Operations Workspace \(SOW\)

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1987460

</td><td>

Use activity fields to control displaying emails, audit relations, and attachments

</td></tr><tr><td>

Activity Stream

</td><td>

PRB1999713

</td><td>

A date is cut off on emails in an activity stream in the printer friendly version

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2000899

</td><td>

An activity stream's heading wraps into a single column at 150%

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2003313

</td><td>

The @mention in the journal input does not appropriately respond to assistive technologies in workspaces

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2004286

</td><td>

A user's filter is incorrectly keying the supplemental map with translated keys, leading to an empty activity stream after changing the language

</td></tr><tr><td>

Activity Stream

</td><td>

PRB2008384

</td><td>

The **Copy** button on journal entries doesn't always copy text or notify users correctly

</td></tr><tr><td>

Activity Stream Activity Component

</td><td>

PRB2023026

</td><td>

The **Show Less** button in Workspace Activity lacks specific context for screen reader users

</td></tr><tr><td>

Activity Stream Compose Component

</td><td>

PRB2032875

</td><td>

Highly threaded emails with multiple block quotes render as unreadable in the 'Conversation' tab

</td></tr><tr><td>

Adaptive Authentication

</td><td>

PRB1950104

</td><td>

An extra sys\_decision\_question record iscreated with an empty condition and empty answer, impacting the 'Zero Trust Access' configuration

</td></tr><tr><td>

Adaptive Authentication

</td><td>

PRB1950104

</td><td>

An extra sys\_decision\_question record iscreated with an empty condition and empty answer, impacting the 'Zero Trust Access' configuration

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2028123

</td><td>

An initial agent response isn't translated even if sys\_translated has a match for the entry

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2010201

</td><td>

The script action 'Set logged out agent offline' creates an offline Advanced Work Assignment \(AWA\) presence record for non-agent users

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2060584

</td><td>

The 'Set logged out agent offline' script action shouldn't touch presence states when 'disable\_inactivity\_check' is set to true

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2013875

</td><td>

Wrap-up modeless dialog is only visible to Interaction Admin users in ITSM Service Operations Workspace

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2026914

</td><td>

Duplicate work items when the service channel's work\_item\_table is a parent class of the routed record

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1969903

</td><td>

The interaction assigned\_to is empty and state is 'new', even though when the live agent is available, the fields are not updating immediately

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2007529

</td><td>

Alert audio continues playing after rejecting a work item

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1975706

</td><td>

Standby node takes 1.5 hours to launch online

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2025053

</td><td>

Missing validation allows AWA queue save with floating schedule

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB1987766

</td><td>

GraphQL calls for snAgentPresenceState are continuing after session expiration

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2003621

</td><td>

Node restarts are caused by the 'AWA - Trigger Document Re-evaluation For Queued/Pending Accept Work Items' job

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2007748

</td><td>

AWAQueueTimeoutUtility.timeoutWorkItems\( is skipped if one work item stays in 'pending\_accept' and bypass sys\_property is on

</td></tr><tr><td>

Advanced Work Assignment

</td><td>

PRB2007789

</td><td>

When separate work items are created within AWA, one work item is correctly assigned, but the other work item is disqualified

</td></tr><tr><td>

Agent Assist

</td><td>

PRB2012771

</td><td>

The error 'TypeError: Cannot read properties of undefined \(reading 'displayValue'\)' appears when the 'Fields' property arrives after the config is loaded

</td></tr><tr><td>

Agent Assist

</td><td>

PRB2035255

</td><td>

A comment is not populated when using 'Link to Incident' from Agent Assist

</td></tr><tr><td>

Agent Assist

</td><td>

PRB2035934

</td><td>

The UI is broken when searching in the Agent Assist search box

</td></tr><tr><td>

Agent Assist

</td><td>

PRB2038420

</td><td>

Agent Assist creates orphaned m2m records for knowledge articles when the Attach action is invoked on tables not extending tasks

</td></tr><tr><td>

Agent Assist

</td><td>

PRB2007824

</td><td>

Agent Assist gives the error 'Link action is unavailable because the field is not present on current record form'

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1707213

</td><td>

Virtual Agent hover message doesn't translate when the language is switched

</td></tr><tr><td>

Agent Chat

</td><td>

PRB2031080

</td><td>

Setting 'Disable agent inactivity check for API' to true makes the presence states disappear from the presence state picker in workspace's inbox

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1992614

</td><td>

Dirty screens in Document Object Model \(DOM\) experience data loss if one of the middle tabs are closed, triggering a screen reorder and refresh

</td></tr><tr><td>

Agent Chat

</td><td>

PRB2013571

</td><td>

Pre-chat survey question title isn't displayed for the agent chat

</td></tr><tr><td>

Agent Chat

</td><td>

PRB2013947

</td><td>

Inbox Advanced Work Assignment \(AWA\) interactions are not presented according to the 'Configuration' field and order for the walkup experience

</td></tr><tr><td>

Agent Chat

</td><td>

PRB2022397

</td><td>

A browser freezes when rendering a chat message containing a long unbroken text token

</td></tr><tr><td>

Agent Chat

</td><td>

PRB2030602

</td><td>

The error 'TypeError: Cannot read properties of undefined \(reading 'output'\)' occurs in the Console Browser

</td></tr><tr><td>

Agent Chat

</td><td>

PRB2032198

</td><td>

When an agent opens an image shared during a live chat, the image shows a vertical line on it which is the border line of interaction page

</td></tr><tr><td>

Agent Chat

</td><td>

PRB2032799

</td><td>

Chat messages sent from an agent are sent out after a conversation is already closed completed

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1989186

</td><td>

TaskUtilsSNC creates millions of sys\_cs\_collab\_chat when collaborative chat is not enabled

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1990618

</td><td>

Live agent connection is not established with the utterance and **Contact** button for non-admin requestors

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1993857

</td><td>

Agent chat inbox notifications appear in HTML

</td></tr><tr><td>

Agent Chat

</td><td>

PRB1998974

</td><td>

There's a 'View All Options' rendering issue on Agent Chat

</td></tr><tr><td>

Agent Chat

</td><td>

PRB2000390

</td><td>

The date format is incorrect in the Active Chat window

</td></tr><tr><td>

Agent Chat

</td><td>

PRB2007792

</td><td>

Date format is incorrect in the Active chat window

</td></tr><tr><td>

Agile Development

</td><td>

PRB2060695

</td><td>

Users are unable to scroll horizonally on agile\_boards

</td></tr><tr><td>

Agile Development

</td><td>

PRB2020539

</td><td>

The **Add to backlog** button creates multiple records when selected multiple times at once

</td></tr><tr><td>

Agile Development

</td><td>

PRB2020877

</td><td>

The 'Story information' tab displays a blank page on the agile board when navigating from SCTASK to 'Story information'

</td></tr><tr><td>

Agile Development

</td><td>

PRB2052806

</td><td>

A story gets unassociated with a catalog task when added to the sprint

</td></tr><tr><td>

Agile Development

</td><td>

PRB1990704

</td><td>

There's a visibility issue with stories associated to original tasks in the Agile backlog

</td></tr><tr><td>

AI Agents \(Glide Family\)

</td><td>

PRB2059390

</td><td>

Role masking isn't unset when running a workflow

</td></tr><tr><td>

AI Agents \(Glide Family\)

</td><td>

PRB2003366

</td><td>

Data to glide from offglide is not logged with the actual user

</td></tr><tr><td>

AI Agents \(Glide Family\)

</td><td>

PRB2034699

</td><td>

GenAIMetadataM2MDaoImpl createAIAGenAIMetadataM2M doesn't assert that the genAILogId parameter is not NULL

</td></tr><tr><td>

AI Agents \(Glide Family\)

</td><td>

PRB2039174

</td><td>

Gen AI Filter is bypassed if utterance contains a new line

</td></tr><tr><td>

AI Agents \(Glide Family\)

</td><td>

PRB2004770

</td><td>

The worker\_manager should be able to create/update AI User records

</td></tr><tr><td>

AI Experience Framework - Glide

</td><td>

PRB2034919

</td><td>

The rich control widget read operation is blocked by the 'Widget Query' business rule

</td></tr><tr><td>

AI Gateway - Security

</td><td>

PRB2041348

</td><td>

The autogenerated fake sys\_ids in AIG should be fixed

</td></tr><tr><td>

AI Search

</td><td>

PRB1875924

</td><td>

AI search ingestion sticks when the 'Size in Bytes' column has an empty value in sys\_attachment for an attachment that has a size more than 25MB

</td></tr><tr><td>

AI Search

</td><td>

PRB1822339

</td><td>

Order Guides aren't functional when accessed from Service Operations Workspace

</td></tr><tr><td>

AI Search

</td><td>

PRB1946791

</td><td>

The user cannot create Semantic Index Fields records for the attachment type

</td></tr><tr><td>

AI Search

</td><td>

PRB1787984

</td><td>

The search preview has the Service Portal Entity View Action Mapper \(EVAM\) configuration hardcoded

</td></tr><tr><td>

AI Search

</td><td>

PRB1842604

</td><td>

The dot walk facet is removed if the user has no table to access another table

</td></tr><tr><td>

AI Search

</td><td>

PRB1893398

</td><td>

Attempting to recreate a scenario where entries in the search term is empty in the sys\_search\_event table

</td></tr><tr><td>

AI Search

</td><td>

PRB1902419

</td><td>

The conversation ID isn't logged to the sys\_search\_event table

</td></tr><tr><td>

AI Search

</td><td>

PRB1914180

</td><td>

On the Employee Service Center \(ESC\) portal, the Genius Result is not returning any data in the German language while it's visible in the AI search preview

</td></tr><tr><td>

AI Search

</td><td>

PRB1989158

</td><td>

Users are unable to edit the font of the AI search widget

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB2033435

</td><td>

TSTranslationReference loads all sys\_translated rows for a field instead of filtering to the indexed record's value

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1859571

</td><td>

A search retrieval agent returns an incorrect catalog item URL

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB2008247

</td><td>

A negative offset isn't handled properly, which causes no results after moving to the next page

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1986147

</td><td>

Extend branding properties to support the update to the dynamic landing page 'Search My Servicenow' placeholder

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1990134

</td><td>

If all KBBs from one doc are removed from KB late binding, the post process stops and all following docs are returned

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB2052168

</td><td>

No\_answer Genius Result is streamed intermittently

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1955992

</td><td>

Catalog Item translations in Catalog Builder are not triggering AI Search ingestion

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1976935

</td><td>

The user context's country in search request is a displayed value instead of an internal value

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1925238

</td><td>

AI Search should reuse the filter generated for each request instead of generating a filter again each time

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1925971

</td><td>

The 'Category' and 'Catalog' facets for catalog items are not using the translated values

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB2032763

</td><td>

DefaultListBasedColumnFinder.getColumns issues unfiltered list\_id IS NULL query against sys\_ui\_list\_element, retaining 500MB+ per cached table entry

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1918638

</td><td>

Indexing fails for the batch due to a corrupted GZIP trailer error

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1950896

</td><td>

The 'Before Query' business rule with the sys\_mod\_count condition generates an invalid query

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1951585

</td><td>

There is a NullPointerExeception \(NPE\) in getConnectedTopicsInformation during ingestion

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1978142

</td><td>

When a portal has Dynamic Window enabled, typeahead on the homepage displays the 'Chat enter' icon and tooltip instead of the search magnifying icon

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB1999484

</td><td>

KBB \(Knowledge Block\) checks break incremental indexing for some catalog child tables

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB2002346

</td><td>

When a KB only has an embedded KBB with embedded\_match = false, the KB should send itself instead of the KBB

</td></tr><tr><td>

AI Search \(Glide\)

</td><td>

PRB2005798

</td><td>

Dictionary term isn't in a published state even though it's actually published to backend

</td></tr><tr><td>

AI Search for Service Portal

</td><td>

PRB1998368

</td><td>

AI Search in Enhanced Chat's full page experience throws a console error

</td></tr><tr><td>

AI Search for Service Portal

</td><td>

PRB1936523

</td><td>

When attempting to sort AI search results by 'Most Relvant' or 'Most Recent', the user gets zero results returned in Yokohama

</td></tr><tr><td>

AI Search for Service Portal

</td><td>

PRB2062818

</td><td>

The sparkle/Otto icon in a portal search input has an incorrect color when Enhanced Chat is turned on

</td></tr><tr><td>

AI Search for Service Portal

</td><td>

PRB2030568

</td><td>

'Filter' controls are inaccessible on mobile view when search results produce no facet matches

</td></tr><tr><td>

AI Search for Service Portal

</td><td>

PRB2067568

</td><td>

Service Portal's faceted search truncates long identifier labels in search result headers due to now-label-value-inline component rendering

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1991431

</td><td>

The right-hand side panel in Zing search is not scrollable

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2017282

</td><td>

In Zing Search, the 'Exact Match' section is missing

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2013005

</td><td>

An error appears: 'ResultTemplateMapper: No composite data found for evamDefinitionId: undefined'

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1981121

</td><td>

Global search isn't working with zoom in/zoom out

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1995624

</td><td>

An exact match doesn't render and loads infinitely when a title isn't returned

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1989246

</td><td>

When records are searched in global search, it isn't opening the form directly

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2006060

</td><td>

Now Assist AI Search summary links \(catalog item references\) are non-functional, but appear active due to the text styling

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1991340

</td><td>

Search input intermittently skips characters

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1994511

</td><td>

Label in header-section\_\_identifier-container does not reflow

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2069550

</td><td>

Search filters infinitely load on the Now Assist full page experience

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2072005

</td><td>

The fix for PRB1935844 was overwritten during a merge

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2016024

</td><td>

Synthesized responses on a mobile sized screen don't display 'Show full answer' after truncation in Zurich on Safari

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1999304

</td><td>

The 'Search My ServiceNow' text is hardcoded

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1942039

</td><td>

Unable to select the 'Search Context' in the global search when zoomed to 150% in Edge

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2002479

</td><td>

URLs wrapped in parenthesis aren't formatted properly in Genius results when the language is set to Japanese

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2006200

</td><td>

Synthesized answer loading card status text isn't fully visible in a narrow viewport when non-English locale text exceeds container bounds

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2038703

</td><td>

Instance creation failure for com.glide.search.graphql.query.Suggestions from service portal's typeahead AIS Suggestions API

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1951853

</td><td>

The 'Learn more' KB link update via EVAM is not working when the streaming synthesized Genius Result

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2015031

</td><td>

Text field highlighting exposes raw markdown syntax in search responses for KB articles

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2016007

</td><td>

Search-based AI Search suggestions should include record\_class\_name

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2021873

</td><td>

Facets aren't rendered as the sensitivity filter fails quietly

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2027205

</td><td>

Logged Search Event 'Has Results' and 'First page results' are incorrectly populated only based on the first RAG Source

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2027945

</td><td>

In Employee Center's mobile web, unintended tooltip/mouse-over text blocks the UI on iOS

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2040015

</td><td>

Differences in the UI displayed on the Global Search page when there are 0 search results

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2054213

</td><td>

URLs with special characters like $ break streaming for non-VA clients

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2068007

</td><td>

Global Search's 'Open list view' returns no results when the search keyword begins with '\#'

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2073716

</td><td>

For non-admin users, search results and suggestion navigation on portals are redirecting to platform view

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1943113

</td><td>

Results generated by Now Assist Genius Result does not show the option to toggle to see 'Show less Answer' once it is expanded

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1954967

</td><td>

The Facet filter has multiple duplicate options appearing for 'Sort'

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1967356

</td><td>

The search API returns a negative result count when hybrid search is turned on

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1975257

</td><td>

There's an invalid sysparm\_search \_context\_config\_id value on an exact match call in a Zing global search

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1993790

</td><td>

The typeahead search results panel doesn't close and the search state becomes inconsistent after selecting a catalog item

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1994212

</td><td>

The hidden description in the source code is visible in the chatbot for 'Order guide' and not for 'Catalog item' in Now Assist Virtual Agent \(NAVA\)

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1997987

</td><td>

The 'Last Updated' time differs when viewed on the portal search page versus the KB article page

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2054952

</td><td>

Rename Now Assist to Otto within AI Search components

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2000828

</td><td>

The 'Async Genius Result Processor' Asynchronous Message Bus \(AMB\) channel subscription is delayed by session sync contention

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2001311

</td><td>

The top-results component doesn't render catalog item citations

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2004210

</td><td>

A Zing component isn't loaded with an error on the console: '\_\_dyImp0\(...\).then is not a function'

</td></tr><tr><td>

AI Search UX

</td><td>

PRB2005193

</td><td>

Exact Match, when configured to honor conditions of search sources, should be configurable for a single application and not the entire instance

</td></tr><tr><td>

AI Search UX

</td><td>

PRB1951160

</td><td>

'Open Link in New Tab' doesn't work/is inconsistent for Genius results and regular results

</td></tr><tr><td>

AI Service - Glide Interfaces

</td><td>

PRB1970597

</td><td>

Machine Learning \(ML\) trainings fail with a 401 error due to ACL errors, unless the 'Predictive Intelligence' plugin is explicitly repaired

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2029673

</td><td>

Data Visualization Library quick-access cards return '0' under the 'Bookmarked' scope when the grid sees bookmarks correctly

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1998034

</td><td>

Single score data visualization ignores the 'Apply time series to result' indicator configuration

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2008673

</td><td>

A single score reported on a 'Time' field with an aggregation as a sum is calculated correctly in the Core/Responsive UI experience but incorrectly in the Platform Analytics Next Experience UI

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2019716

</td><td>

Multiple elements from a single filter can't be applied to an 'COUNT DISTINCT' or 'AVERAGE' indicator with 'Show filter as separate series'

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1978825

</td><td>

'Total value' displays in the center of donut visualization changes with a 'Group By' adjustment

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2002190

</td><td>

The error log should be suppressed in a prefetch job

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2018043

</td><td>

Invalid links are created on trend-type data visualizations in non-English environments

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1849840

</td><td>

Data visualization on the pivot table shows zero or incorrect data when the top number values are selected in the 'Group by Row' filter

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2030053

</td><td>

Add a feature flag for auto cache of PA indicators

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2050497

</td><td>

The report.view events are generated with the wrong sys\_id and are erroring out in Australia

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1943501

</td><td>

The multi-pivot visualization on the classic PA indicator is not properly filtered by the 'Indicator' filter

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2028758

</td><td>

The 'Create a Data Visualization' column type has a 'Unable to display content' error

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2006192

</td><td>

'Score on Single Score' visualization doesn't render when the metric is against currency type field, data cache is enabled, and a certain condition is added for the metric field

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2006685

</td><td>

When selecting multiple breakdown filters, the target for the indicator doesn't display correctly

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1996433

</td><td>

An indicator search doesn't work with Japanese names when adding a data source to a data visualization even if the instance language is Japanese

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2035591

</td><td>

In a Platform Analytics dashboard, the sorting behavior is incorrect

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2039649

</td><td>

The Platform Analytics dashboard ignores the data source filter

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB1923997

</td><td>

The timeseries drilldown to records have an incorrect filter

</td></tr><tr><td>

Analytics Data API

</td><td>

PRB2005078

</td><td>

When using dynamic date ranges, appliedFilters returns incorrect dates

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB1971222

</td><td>

'Omit if no records' isn't honored for score visualizations

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB1996615

</td><td>

Scheduled export with omit if no records enabled, no attaching the exported file in Email log

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB2019161

</td><td>

The export option is not working for sub domain dashboards

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB2009168

</td><td>

Visualization export doesn't work if the data source is User Experience Analytics

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB2002135

</td><td>

An export failed using the PARExport server due to records containing a backslash character

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB2006196

</td><td>

Heatmap report colours aren't retained when exporting to PowerPoint

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB2009827

</td><td>

There are encrypted columns with blank data when exporting a report to an excel file

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB2021342

</td><td>

The email layout in an Platform Analytics scheduled export doesn't match the received email format

</td></tr><tr><td>

Analytics Export API

</td><td>

PRB2023200

</td><td>

Hide the export option when it's disabled or the roles list is empty

</td></tr><tr><td>

Anonymous Report Center \(ARC\)

</td><td>

PRB2052999

</td><td>

There's missing translations in Anonymous Report Center \(ARC\)

</td></tr><tr><td>

API Key and HMAC Token Based Authentication

</td><td>

PRB1993928

</td><td>

There's an error \(assignment to undefined 'gr' in strict mode\) in a business rule

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1979295

</td><td>

Plugins deferred during a jumbo app install aren't supported in Parallel Plugin Loading \(PPL\)

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB1938034

</td><td>

The 'Resolution Code' column is missing after the Yokohama release

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB2012544

</td><td>

An app package dropping a table and creating a database view in the same name inside can lead to catastrophic drops against system tables

</td></tr><tr><td>

Application Install Engine

</td><td>

PRB2019775

</td><td>

InstallationPlan.java's fixAssignedVersion ForStoreApps method can overwrite the assigned\_version in the middle of a batch install

</td></tr><tr><td>

Application Manager

</td><td>

PRB1986694

</td><td>

App Manager and My Company Applications incorrectly show available updates after update checker

</td></tr><tr><td>

Application Manager

</td><td>

PRB1975999

</td><td>

The user can not update the customized app's base version when no new customized versions are available

</td></tr><tr><td>

Application Manager

</td><td>

PRB2022268

</td><td>

The application manager sys\_app\_version displays duplicate records for the same application and version, which is causing the app to be 'Installation blocked'

</td></tr><tr><td>

Application Manager

</td><td>

PRB1951033

</td><td>

Inconsistent behavior with app version V15.0.18 in Store and instance installation

</td></tr><tr><td>

Application Manager

</td><td>

PRB1999973

</td><td>

Searching by app name returns excessive results and an exact match isn't surfaced on the first page

</td></tr><tr><td>

Application Manager

</td><td>

PRB2000273

</td><td>

The 'Dark' theme hides text in several parts of the system

</td></tr><tr><td>

Application Manager

</td><td>

PRB2009100

</td><td>

Unable to change the color of header links from the theme builder as other styles are overriding

</td></tr><tr><td>

Application Manager

</td><td>

PRB2020279

</td><td>

Users can't uninstall the 'Universal Request' application

</td></tr><tr><td>

Application Manager

</td><td>

PRB2022459

</td><td>

Suite install fails for customized apps with 'none' passed as requested\_customization \_version in an install plan

</td></tr><tr><td>

Application Manager

</td><td>

PRB1979149

</td><td>

Now Assist for Configuration Management Database \(CMDB\) 2.5.2 certification/installation fails with conflicting versions

</td></tr><tr><td>

Application Manager

</td><td>

PRB1992033

</td><td>

Incorrect Dependencies showing up for an app with customizations on Install Modal

</td></tr><tr><td>

Application Manager

</td><td>

PRB2005376

</td><td>

The 'Activity log' link in the header doesn't render if selected slightly away from the text itself

</td></tr><tr><td>

Application Manager

</td><td>

PRB2008679

</td><td>

The list of uninstall conflicts doesn't provide valid data

</td></tr><tr><td>

Application Rationalization

</td><td>

PRB1977007

</td><td>

Generate Assessment takes too long to load because of excessive sys\_user\_group records

</td></tr><tr><td>

Application Rationalization

</td><td>

PRB1990444

</td><td>

The **Update Hierarchies** button shuffles the hierarchy randomly for sub-capabilities

</td></tr><tr><td>

Application Rationalization

</td><td>

PRB1994022

</td><td>

A few dashboards display the message: 'You do not have the required permissions to view this content. Access is restricted by the report\_view ACL'

</td></tr><tr><td>

Application Rationalization

</td><td>

PRB2000392

</td><td>

An empty role record is created when sn\_gf.goal\_user\_read is added to the Application Portfolio Management \(APM\) read role without the 'Goal Framework' plugin

</td></tr><tr><td>

Approvals

</td><td>

PRB2000988

</td><td>

Granular delegate functionality isn't working for approvals via email

</td></tr><tr><td>

Approvals

</td><td>

PRB2005187

</td><td>

Approval summarizer CSS/formatting breaks for users when viewed in non-English languages

</td></tr><tr><td>

Approval with E-signature

</td><td>

PRB2004288

</td><td>

After installing an approval with e-signature plugin, there's no active 'Reject' list UI action

</td></tr><tr><td>

Ask for Approval - Flow Action

</td><td>

PRB1976552

</td><td>

WFC can't retrieve a runtime value rw\_ids when it resumes from a record update and caused RWs to not be cleaned properly

</td></tr><tr><td>

Assessments

</td><td>

PRB2037741

</td><td>

Assessment on Tags condition is failing

</td></tr><tr><td>

Asset Management

</td><td>

PRB2025075

</td><td>

A catalog task isn't created in Hardware Asset's refresh flow

</td></tr><tr><td>

Asset Management

</td><td>

PRB1993884

</td><td>

The script include AssetAndCI has a typo in the function\_createBatchAsset QueueRecords at the method call addQuey\(\)

</td></tr><tr><td>

Asset Management

</td><td>

PRB2010495

</td><td>

'Update Record' action updates an invalid asset GlideRecord and triggers business rules when the reference record is deleted while the flow is in progress

</td></tr><tr><td>

Asset Management

</td><td>

PRB2036478

</td><td>

Creating new record when base instance Asset Management shows 'Record not found'

</td></tr><tr><td>

Asset Management

</td><td>

PRB1985129

</td><td>

Consumables are doubling when being received

</td></tr><tr><td>

Asynchronous Message Bus \(AMB\)

</td><td>

PRB1995214

</td><td>

A websocket session should be closed when the HttpSession or cometD session expires

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB2061519

</td><td>

GlideSysAttachment attachment loop silently truncates in scoped apps due to unhandled NullPointerException in RealTimeProtectionPolicyCache

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1970427

</td><td>

The attachment can be attached in the Project Workspace although glide.attachment.role is 'nobody' in Yokohama

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB2057344

</td><td>

An attachment preview overlay is missing a background color when Document Viewer is turned off, and it causes 'Close', 'Delete', and **Download** buttons to become imperceivable in Workspace

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1929507

</td><td>

Uploading an image with setValidateMime TypeDuringWrite=true throws a stream closed exception

</td></tr><tr><td>

Attachments to Records

</td><td>

PRB1990612

</td><td>

The cursor occasionally jumps to the end of text when renaming attachment in the 'Upload a file' menu

</td></tr><tr><td>

Audit History

</td><td>

PRB1999538

</td><td>

AuditStringBuilder accepts an invalid value from fx\_currency fields

</td></tr><tr><td>

Audit History

</td><td>

PRB2023535

</td><td>

AI agent user context isn't cleared out after the GenAI skill call is completed

</td></tr><tr><td>

Audit History

</td><td>

PRB1992569

</td><td>

Audit Management Console creates incorrect dictionary overrides for non-inherited fields and overwrites existing attributes

</td></tr><tr><td>

Authentication

</td><td>

PRB2016648

</td><td>

The location header isn't parsed correctly during mobile login for /sg/pre\_auth API

</td></tr><tr><td>

Authentication

</td><td>

PRB1964259

</td><td>

When OpenID Connect \(OIDC\) authentication fails, users are redirected to /not\_allowed.do

</td></tr><tr><td>

Authentication

</td><td>

PRB2017246

</td><td>

IDP initiated logout doesn't receive the POST call with relay state

</td></tr><tr><td>

Authentication

</td><td>

PRB2024736

</td><td>

The user is unable to disable performance analyzer on the app login page

</td></tr><tr><td>

Authentication

</td><td>

PRB2030127

</td><td>

Client script 'Check Certificate Auth Flag Enabled' contains a 'More Details' link that appears empty and only refreshes the page

</td></tr><tr><td>

Authentication

</td><td>

PRB2037962

</td><td>

The MCP Server registration with the Client Credentials grant fails when created via AI Agent Studio

</td></tr><tr><td>

Authentication

</td><td>

PRB2050056

</td><td>

ACR user can't access OIDC SSO login configurations

</td></tr><tr><td>

Authentication

</td><td>

PRB2050056

</td><td>

An ACR user can't access OIDC SSO login configurations

</td></tr><tr><td>

Authentication Factors

</td><td>

PRB2066684

</td><td>

Match KB identification phone numbers are ignoring special characters

</td></tr><tr><td>

Authentication Factors

</td><td>

PRB2052206

</td><td>

There's an error: 'sys\_now\_assist\_deployment\_config table is not valid '

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2008295

</td><td>

When an RT \(reusable test\) calls another RT \(nested\), the inner RT's input variables that reference the outer RT's inputs via GEM pills resolve incorrectly

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2054701

</td><td>

A 'Host CPU Load Critical' alert is caused by ATF Scheduler jobs with a large amount of sys\_atf\_modified\_record\_m2m records generated

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2002662

</td><td>

All Software Asset Management \(SAM\) Automated Test Framework \(ATF\) tests fail with an error: 'JS error 'SyntaxError: unexpected token: identifier' found during Step 'null''

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2017479

</td><td>

ATF client error 'Cannot read properties of undefined \(reading 'toString'\)' occurs in Australia when the client script has comments and isolate script = false

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2021406

</td><td>

Code coverage instrumentation errors shouldn't fail test runs

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1979777

</td><td>

Automated Test Framework \(ATF\) performance comparisons are incomplete due to poorly formed URLs

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2017949

</td><td>

There's stuck execution trackers due to Automated Test Framework \(ATF\)'s new feature metadata tracing

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2012913

</td><td>

Tests fail with an error: 'Timed out waiting for intent feedback &lt;Intermittent, slow loading forms, SAP&gt;'

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2015508

</td><td>

Workspace load time performance fixes in Automated Test Framework \(ATF\) cache

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2024167

</td><td>

When a fetch never completes GAW gets stuck and will wait full 60 seconds on each step

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2027425

</td><td>

ATF confirm capture fails when page redirects during test

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2032820

</td><td>

Cross origin iframe in shadow root causes GlideAutomateWait to never report calm

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1978668

</td><td>

An Automated Test Framework \(ATF\) test result email doesn't display all tests

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB1997372

</td><td>

If default value is empty in a reusable test, then it sets to the GEM pill

</td></tr><tr><td>

Automated Test Framework \(ATF\)

</td><td>

PRB2005213

</td><td>

If glide.ui.escape\_all\_script is set to the unsafe value of false, metadata tracing in ATF steps causes the UI action visibility steps to fail

</td></tr><tr><td>

Base Asset Management

</td><td>

PRB2018526

</td><td>

The fix script 'Add reference qualifiers for Manufacture' impacts the Software Asset Management \(SAM\) software model, and potentially all models extending cmdb\_model

</td></tr><tr><td>

Business Calendar

</td><td>

PRB2004850

</td><td>

'Duration' fields display negative values due to ERA contamination in cached SimpleDateFormatEx instances

</td></tr><tr><td>

Business Calendar Filter Options

</td><td>

PRB1977276

</td><td>

Filter values included with the 'Fiscal Calendar' \(com.snc.fiscal\_calendar\) plugin aren't translated

</td></tr><tr><td>

Cache

</td><td>

PRB2003357

</td><td>

A cache flush is triggered from the 'Scoped application client environment' \(sn\_appclient\) package

</td></tr><tr><td>

Canonicalization Data Services \(CDS\)

</td><td>

PRB2053470

</td><td>

Data uploaded to cds\_server\_staging table is blocked within instances

</td></tr><tr><td>

Canonicalization Data Services \(CDS\)

</td><td>

PRB2053455

</td><td>

Data sync fails for users who are on-prem and have proxy configured

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2024293

</td><td>

The HR ACL script hasHRApprovalAccess fails to resolve a source table for non-task approvals

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2027153

</td><td>

HR Templates not applying as expected from Flows

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2004389

</td><td>

The TableChoiceList cache is susceptible to corruption

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2006367

</td><td>

Unable to deactivate 'HR Lifecycle Events Case' COE due to cross-scope error

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2009518

</td><td>

Script in the ACL for sn\_hr\_er\_accommodation table is impacting scheduled jobs

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2015924

</td><td>

Action buttons are visible to users without write access in Native Platform and Agent Workspace in Employee Relations cases

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2028789

</td><td>

The HR case 'Close Incomplete' UI action doesn't handle info messages in the classic UI

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2071462

</td><td>

System logs have the error 'Scoped cache operation against catalog nowassist\_admin was skipped because of an invalid sysId: no thrown error'

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1826631

</td><td>

A playbook displays an activity set as 'pending' when all tasks are optional

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1963168

</td><td>

The HRSD Knowledge Graph is unavailable after an upgrade

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB1992913

</td><td>

A user with a Catalog Builder editor role isn't able to create a record producer from a template coming from a different scope

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2007826

</td><td>

Fields are missing on a base instance LE form

</td></tr><tr><td>

Case and Knowledge Management for HR Service Delivery

</td><td>

PRB2008310

</td><td>

On the sn\_hr\_core\_case\_creation page, rich\_description doesn't hold/contain html for rich description formatting \(for example, &lt;br/ &gt;\)

</td></tr><tr><td>

Case Management

</td><td>

PRB1954277

</td><td>

'Assign to Me' in the Incident form is checked if the logged in user belongs to the assignment group, but if they are part of multiple groups, it prompts for group selection, and this logic is missing in the Case form

</td></tr><tr><td>

Case Management

</td><td>

PRB1956961

</td><td>

Multiple **Create Case** buttons appear in a interaction record in Workspace

</td></tr><tr><td>

Change Management

</td><td>

PRB2052987

</td><td>

NewChangeRedirectProcessor only checks the system-wide glide.ui.polaris.experience property and ignores per-user glide.ui.polaris.use preference when deciding Next Experience redirect for Create Change

</td></tr><tr><td>

Change Management

</td><td>

PRB2032620

</td><td>

CAB Workbench Meeting Calendar API returns empty array when a month contains both ACL-accessible and ACL-restricted CAB meetings

</td></tr><tr><td>

Change Management

</td><td>

PRB2037302

</td><td>

Sequence of change states are not in order based on Change Model in proces flow in service operations workspace

</td></tr><tr><td>

Change Management

</td><td>

PRB2014057

</td><td>

The 'Change Schedule' filter doesn't work for records not shown on the screen

</td></tr><tr><td>

Change Management

</td><td>

PRB2030123

</td><td>

Intermittent Issue with Change Task Auto-Cancellation on Production

</td></tr><tr><td>

Change Management

</td><td>

PRB2032087

</td><td>

The Change Models onChange client script 'Change Model: read only state On hold' fires if a value hasn't changed

</td></tr><tr><td>

Change Management

</td><td>

PRB2035924

</td><td>

Standard changes created from a problem aren't linked to the parent task

</td></tr><tr><td>

Change Management

</td><td>

PRB2037424

</td><td>

CreateChangeLandingSNC.\_getStdChgSubCategories bypasses ACL and catalog user criteria for Standard Change category filter

</td></tr><tr><td>

Change Management

</td><td>

PRB2057998

</td><td>

'No slots found for 90 days' info message displays in the Change Management API

</td></tr><tr><td>

Change Management

</td><td>

PRB2067778

</td><td>

The change manager and change owner can't clear the checkbox for an unauthorized change

</td></tr><tr><td>

Change Management

</td><td>

PRB1994240

</td><td>

Translation issues in the Conflict Checker Progress modal window

</td></tr><tr><td>

Change Management

</td><td>

PRB1997537

</td><td>

Attachments added on the 'Modify standard change template' form are lost and don't display on the template or change request

</td></tr><tr><td>

Change Management

</td><td>

PRB2000859

</td><td>

There's incorrect 'State' values when using 'Copy Change' on emergency changes

</td></tr><tr><td>

Change Management

</td><td>

PRB2004568

</td><td>

There's a 'Change Schedule' filter issue

</td></tr><tr><td>

Change Management

</td><td>

PRB2005865

</td><td>

When users run the playwright test 'ChangeRiskAsmtDirtyForm\_IT', after saving, it redirects to a blank page

</td></tr><tr><td>

Change Management

</td><td>

PRB2061434

</td><td>

There's duplicate task record reloads and unexpected list view queries during change request creation/updates

</td></tr><tr><td>

Client Scripts

</td><td>

PRB2023743

</td><td>

Client script behavior isn't the same in Australia and Yokohama

</td></tr><tr><td>

Client Scripts

</td><td>

PRB2023743

</td><td>

Client script behavior isn't the same in Australia and Yokohama

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1982662

</td><td>

There's an inefficient query to the cmdb\_rel\_ci table in the script include 'ServiceAccountLDCMapping', which causes a performance bottleneck during cloud event processing

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1992231

</td><td>

In Cloud Provisioning and Governance, a change request remains in an 'open' state, but close notes should be updated like before

</td></tr><tr><td>

Cloud Provisioning and Governance

</td><td>

PRB1994016

</td><td>

Using parentheses in an order form's data values breaks Json processing during provisioning

</td></tr><tr><td>

CMDB CI Class Manager

</td><td>

PRB1937991

</td><td>

CI Class manager behavior for domain separation

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB2030582

</td><td>

CMDB Workspace does not show correct Cis in retire policy when using Portuguese language

</td></tr><tr><td>

CMDB Data Manager

</td><td>

PRB1980074

</td><td>

Data Manager's 'Retire', 'Archive', and 'Delete' policy execution times are degraded by at least &gt;8%

</td></tr><tr><td>

CMDB Health Dashboard

</td><td>

PRB2022903

</td><td>

OOM/High memory utilization in Orphan Health Job

</td></tr><tr><td>

CMDB Health Dashboard

</td><td>

PRB2057249

</td><td>

There's integer overflow in RequiredProcessor/RecommendedProcessor when failure\_threshold is set to Integer.MAX\_VALUE

</td></tr><tr><td>

CMDB Health Dashboard

</td><td>

PRB1976306

</td><td>

The Health Dashboard displays only 1,000 configuration items \(CIs\) for services

</td></tr><tr><td>

CMDB Health Dashboard

</td><td>

PRB1999729

</td><td>

CMDB Health Dashboard data isn't displayed in the 'Service' view for Business Service, Technology Management Service and Service Offering, even though they are selectable options

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1975531

</td><td>

Include extra checks on the 'Add Certification Role To Manager' business rule

</td></tr><tr><td>

CMDB Identification and Reconciliation

</td><td>

PRB1993104

</td><td>

In CMDB Health Scores, it displays 100% on the pie chart when the main number is 99%

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB2004460

</td><td>

Queries created in custom scopes have missing report columns

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB2020428

</td><td>

CMDBGroup. getAllCIByDomainId silently under-populates svc\_ci\_assoc when start-node pagination crosses multiple batches

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB2019871

</td><td>

CMDB Query Builder doesn't support ^NQ \(Global OR\) inside a node filter

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB1986239

</td><td>

A CMDB group with saved query V2 execution only loads two batches with 'Load More Results'

</td></tr><tr><td>

CMDB Query Builder

</td><td>

PRB2003920

</td><td>

Calls to the 'CMDBGroup' API don't include Query Builder results for any query exceeding glide.cmdb.query.max\_results

</td></tr><tr><td>

CMDB to CSDM Data Synchronization

</td><td>

PRB2036380

</td><td>

Legacy mapping fields are not part of the update set in PRB1999885, so the CI is updated back to wrong life cycle combination after an update to the CI

</td></tr><tr><td>

CMDB to CSDM Data Synchronization

</td><td>

PRB1999885

</td><td>

Re-activation of several life\_cyle\_control records must support user requests

</td></tr><tr><td>

CMDB to CSDM Data Synchronization

</td><td>

PRB2000037

</td><td>

ActionRecordList.setReferenceValue rejects valid autocomplete selections for translated reference\_key fields in non-English languages

</td></tr><tr><td>

Code Signing

</td><td>

PRB2014768

</td><td>

Increase the code signing validity window maximum from 60 minutes to 4 hours

</td></tr><tr><td>

Code Signing

</td><td>

PRB2014831

</td><td>

Scheduled scripts incorrectly appear in 'Update Set Signature States'

</td></tr><tr><td>

Code Signing

</td><td>

PRB2014833

</td><td>

Enable digest creation for users with the code signing role

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB2006384

</td><td>

Attachments from the sn\_si\_incident table are created with a different hash

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB1978716

</td><td>

Encryption isn't applied correctly for comma separated list values in a Glide record query for IN and NOT\_IN clauses

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB1979815

</td><td>

An encryption state fails to set be set to '6' when installing the FEE plugin

</td></tr><tr><td>

Column Level Encryption

</td><td>

PRB2005360

</td><td>

On an encrypted HTML field, getElement\(fieldName\) returns a GlideElement with a value of 'null' instead of an empty string \(''\), causing the condition ge == null to evaluate as true

</td></tr><tr><td>

Communities

</td><td>

PRB2009909

</td><td>

Forum and forum permissions list pages are slow to load

</td></tr><tr><td>

Communities

</td><td>

PRB1487727

</td><td>

'Moderation Banned Keyword Filter' isn't working for keywords in other language

</td></tr><tr><td>

Communities

</td><td>

PRB2003810

</td><td>

Views in Event Content are displaying as '2,147,483,648'

</td></tr><tr><td>

Communities

</td><td>

PRB2012517

</td><td>

Community filter prevents French words from being used, but it shouldn't

</td></tr><tr><td>

Communities

</td><td>

PRB2014706

</td><td>

Search at community doesn't work for a particular user

</td></tr><tr><td>

Communities

</td><td>

PRB2023547

</td><td>

Accessibility\_Community Portal\_My community Profile - 4.1.2 'Name', 'Role', 'Value\_Tabs' are announced as 'selected' on focus when navigating with the tab key

</td></tr><tr><td>

Communities

</td><td>

PRB2023596

</td><td>

On the 'Community' portal, 'Ask a Question' and 'Info and Relationship' label association issues and a verbose screen reader announcement

</td></tr><tr><td>

Communities

</td><td>

PRB2025205

</td><td>

Topics options cannot be deselected using mouse

</td></tr><tr><td>

Communities

</td><td>

PRB2025267

</td><td>

The **Browse forums** button fails to describe its expanded/collapsed state

</td></tr><tr><td>

Communities

</td><td>

PRB2025489

</td><td>

2.1.1 Keyboard\_ESC key does not close the dialog

</td></tr><tr><td>

Communities

</td><td>

PRB2025841

</td><td>

Selected state of **Grid/List view** buttons is not announced

</td></tr><tr><td>

Communities

</td><td>

PRB2025886

</td><td>

In the Community portal, the focus indicator isn't clearly visible on the **Email User** button

</td></tr><tr><td>

Communities

</td><td>

PRB2032101

</td><td>

Accessibility\_Community Portal\_My community Profile - 4.1.2 Name, Role, Value\_Incorrect role announced

</td></tr><tr><td>

Communities

</td><td>

PRB2058056

</td><td>

Community Blog table cell padding is silently reset to 0px when a post is viewed, even though the padding is saved correctly in the underlying data

</td></tr><tr><td>

Communities

</td><td>

PRB2058595

</td><td>

In the Community portal, headings skip levels on the 'Earning Points' page

</td></tr><tr><td>

Communities

</td><td>

PRB1773760

</td><td>

The scale of an image becomes longer in the vertical mode of a mobile browser

</td></tr><tr><td>

Communities

</td><td>

PRB1994813

</td><td>

Adding HTML in a community question using TinyMCE causes the content to take over the entire page

</td></tr><tr><td>

Condition Builder

</td><td>

PRB2033581

</td><td>

Data visualization in Condition Builder isn't displaying fields for dates as it does in the Core UI

</td></tr><tr><td>

Condition Builder

</td><td>

PRB2009232

</td><td>

Angular directive, which is part of the NG Filter Widget, has duplicate elements IDs in Condition Builder

</td></tr><tr><td>

Condition Builder

</td><td>

PRB2031746

</td><td>

'??' appears when saving filter criteria

</td></tr><tr><td>

Condition Builder

</td><td>

PRB2033984

</td><td>

When the user filters between last year and one year ago, the last two years are displayed

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1958222

</td><td>

There is a missing an unordered list mark-up for breadcrumb links on the 'Incident\_list.do' page

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1967309

</td><td>

Filter conditions on a list isn't correct when the link from Platform Analytics dashboard has filter conditions saved in another language

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1972846

</td><td>

Show a message to the user when there is a postgreSQL exception on running a filter with over 65k records

</td></tr><tr><td>

Condition Builder

</td><td>

PRB1996851

</td><td>

An AI Agent tool condition doesn't support relative operators in filter queries

</td></tr><tr><td>

Condition Builder

</td><td>

PRB2000227

</td><td>

There's CSS misalignment on the **Save Filters** button

</td></tr><tr><td>

Condition Builder

</td><td>

PRB2002711

</td><td>

'Duration' fields throw a warning error for any operator with values between 12~31 days

</td></tr><tr><td>

Condition Builder in Core UI

</td><td>

PRB2032005

</td><td>

The dot‑walk \(branch\) icon is not visible when the reference field label exceeds a certain length

</td></tr><tr><td>

Condition Builder in Core UI

</td><td>

PRB1936913

</td><td>

Filter condition 'Created on last Month' is not working properly

</td></tr><tr><td>

Condition Builder in Workspace

</td><td>

PRB2026306

</td><td>

Issue with translations in Variables Lookup for platform analytics Data Visualization

</td></tr><tr><td>

Condition Builder in Workspace

</td><td>

PRB2051562

</td><td>

'Is a' \(Instance Of\) operator in Condition Builder

</td></tr><tr><td>

Condition Builder in Workspace

</td><td>

PRB2005883

</td><td>

In the Workplace Central schedule view, users can access filters that they're not supposed to

</td></tr><tr><td>

Condition Builder in Workspace

</td><td>

PRB2008223

</td><td>

The sn-editor-textarea component duplicates ^ when used in a javascript: prefix

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2037178

</td><td>

A relationship editor \(child\) entry incorrectly displays a '\*' suggested marker when only the parent direction is configured in cmdb\_rel\_type\_suggest

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1992684

</td><td>

CMDB Query Builder with the system language set as Japanese displays empty results

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2020295

</td><td>

INSERT\_NOT\_ALLOWED\_FOR\_SOURCE incorrectly classified as a partial error causes the cmdb\_ire\_partial\_payloads table to bloat and an out of memory \(OOM\) error

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2017567

</td><td>

There is an infinite loop in PartialPayloadProcessor when the payload size limit is exceeded on the first record of a batch

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1944067

</td><td>

Unexpected behavior from the field after submitting the condition in the certification 'Template for Desired state audit' type

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2017461

</td><td>

There's MULTI\_MATCH errors when duplicate rows exist in cmdb\_rel\_ci for non-dependency relationships

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1981400

</td><td>

Support skipping gateway DB tables when fetching the related item count from de-duplication tasks

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1942648

</td><td>

The 'Calculate app services missing data' job runs for an extended duration

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1996218

</td><td>

sys\_object\_source table indexes grow to extreme sizes \(one to four TB combined\) within days of a rebuild due to continuous last\_scan timestamp updates on every scan cycle

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2010187

</td><td>

CIUtils \_getImpactedServicesFromAffectedCIs\(\) performs unbounded aggregation against svc\_ci\_assoc, causing JVM out of memory at scale

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2011691

</td><td>

IRE doesn't update the 'Duplicate\_of' field when CIs are identified on lookup rules

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2016876

</td><td>

There's no supported way to fully disable the Dependent CI Management feature

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2018505

</td><td>

The multiSource last\_discovered field is not updated even when the CI is updated

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2021367

</td><td>

Implement totals calculation for the group view when applying a class filter qualifier configuration

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2028831

</td><td>

Switching to Service Graph Workspace breaks UI macros to open CIs in CMDB Workspace

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2029435

</td><td>

Application Service Wizard error when creating relationships

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2034768

</td><td>

CMDB Health AuditProcessor has long-running queries/sys\_idINnull

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2051060

</td><td>

CIUtils \_getImpactedServicesFromAffectedCIs\(\) performs unbounded aggregation against svc\_ci\_assoc, causing JVM OOM at scale

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2051917

</td><td>

There's an error: 'Element type 'javascript:gs.beginningOfYesterday' must be followed by either attribute specifications, '&gt;' or '/&gt;''

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2057723

</td><td>

Duplicate sys\_properties record causes csdm.lifecycle.sync.between.ci.and.asset.activated to default to true instead of false

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2059184

</td><td>

Identification and Reconciliation Engine \(IRE\) switches existing CI classes

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2063266

</td><td>

The 'CMDB Data Management' task remained active even though the state is 'Closed Incomplete'

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1814757

</td><td>

In CI Class Manager, users without the application picker can't update entries associated with tables outside the global scope

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1969944

</td><td>

The business rule 'CSDM Data Sync on removed association' is overrided by managedByGroup on a CI

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1973978

</td><td>

In the 'Dependency' view, the CI context menu isn't translated

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1980267

</td><td>

There's a cmdb\_data\_source \_last\_update discrepancy

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1981182

</td><td>

Identification and Reconciliation Engine \(IRE\) reclassification tasks don't include internal payload values

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1986775

</td><td>

IRE throws missing dependency errors for dependent CIs when glide.identification\_engine.skip\_sys\_object\_source\_matching property is enabled

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB1992630

</td><td>

The 'Relationship' formatter displays duplicate entries in the 'Tree' view due to manual endpoint connections

</td></tr><tr><td>

Configuration Management Database \(CMDB\)

</td><td>

PRB2002478

</td><td>

For a CMDB task in the Data Manager policy, approvals are sent to inactive users

</td></tr><tr><td>

Consumable Assets

</td><td>

PRB1985572

</td><td>

New images added via Consumable Model aren't returned in a portal's AI search

</td></tr><tr><td>

Contextual Search

</td><td>

PRB2010418

</td><td>

An admin user isn't able to add more additional resources to the search context \(cxs\_res\_context\_config\) table

</td></tr><tr><td>

Continual Improvement Management

</td><td>

PRB1988563

</td><td>

A Continual Improvement Management \(CIM\) manager/coordinator is unable to see options for the type field on a new improvement initiative \(sn\_cim\_register\) record

</td></tr><tr><td>

Continuous Integration/Continuous Delivery \(CI/CD\) API

</td><td>

PRB2004839

</td><td>

Publishing a scoped application to the app repo that contains a delete to sys\_ui\_form doesn't generate the correct payload, and when the application is installed, it doesn't delete the record

</td></tr><tr><td>

Contract Management

</td><td>

PRB2040201

</td><td>

Assets covered on a contract aren't added through an Multiple Record Associator \(MRA\) pop-up

</td></tr><tr><td>

Contract Management

</td><td>

PRB1988765

</td><td>

The Hardware Asset Workspace 'Renew Contract' pop-up isn't working as expected

</td></tr><tr><td>

Contract Management

</td><td>

PRB2005081

</td><td>

The 'Life Cycle Stage' and 'Life Cycle Stage Status' fields aren't correctly imported from the source Excel file if the fields are in Japanese

</td></tr><tr><td>

Contract Management

</td><td>

PRB2032028

</td><td>

The currency field 'Payment Amount' on ast\_contract adds two decimal places \(x100\)

</td></tr><tr><td>

Contract Management

</td><td>

PRB2051900

</td><td>

'Please verify or update the conditions of this contract renewal:' is hardcoded

</td></tr><tr><td>

Core UI Interactive Filters

</td><td>

PRB2007031

</td><td>

Applying the filter in the Dashboard shows 'Some applied options are currently unavailable' when the filter options have a comma ',' in the value

</td></tr><tr><td>

Core UI Interactive Filters

</td><td>

PRB1996683

</td><td>

Support of dependent fields in cascading filters for both reference and choice type-fields

</td></tr><tr><td>

Core UI Interactive Filters

</td><td>

PRB2008024

</td><td>

Support for dependent fields in cascading filters for both 'Reference' and 'Choice' fields

</td></tr><tr><td>

Core UI Responsive Dashboards

</td><td>

PRB2019649

</td><td>

Exclude legacy dashboards from the 'PA Indicator Recommendation Calculator Job'

</td></tr><tr><td>

Core UI Responsive Dashboards

</td><td>

PRB2052870

</td><td>

Every login session creates a error log: 'Could not find portal page with ID: null' '\*\*\* Script: Could not find portal page with ID: null: no thrown error''

</td></tr><tr><td>

Core UI Responsive Dashboards

</td><td>

PRB1993682

</td><td>

'This report has been migrated to a visualization' banner is shown when the unified property is false

</td></tr><tr><td>

Core UI Responsive Dashboards

</td><td>

PRB2004289

</td><td>

After a dashboard is duplicated, translated tab names disappear and add one more tab

</td></tr><tr><td>

Core UI Responsive Dashboards

</td><td>

PRB2005720

</td><td>

The CoreUI dashboard selector triggers excessive ACL checks

</td></tr><tr><td>

Cost Management

</td><td>

PRB1907331

</td><td>

Expense lines record against the wrong cost plan, expense type, and cost type, which causes a difference between exported reports and tables in SPM

</td></tr><tr><td>

Crew Operations

</td><td>

PRB1988513

</td><td>

Users are unable to remove or add crew members from a 'Crew' list in Customer Service Management workspace, and it throws 'Record selection required'

</td></tr><tr><td>

Currency Administration

</td><td>

PRB2055746

</td><td>

The 'Currency' field value is multiplied by 100 in the advanced filter in workspace

</td></tr><tr><td>

Currency Administration

</td><td>

PRB2057817

</td><td>

After the Australia upgrade, the currency component forces a minimum of two decimal places for zero-decimal currencies \(for example, VND\)

</td></tr><tr><td>

Currency Administration

</td><td>

PRB1985059

</td><td>

ChoiceListGenerator.getChoiceList\(\) doesn't retrieve the choices of a child domain for a user on its parent domain

</td></tr><tr><td>

Customer Operations for Customer Service Management

</td><td>

PRB2051783

</td><td>

The 'Account query for customer' Business Rule is recursive

</td></tr><tr><td>

Customer Service Core

</td><td>

PRB2060592

</td><td>

Screen reader announces the content information in Guided Setup as a table, needs role='presentation'

</td></tr><tr><td>

Customer Service Core

</td><td>

PRB1978133

</td><td>

Query rules on the alm\_asset table restrict record access to users with the wm\_agent role in Field Service Management

</td></tr><tr><td>

Customer Service Core

</td><td>

PRB2003966

</td><td>

The 'Description' field on a case is read-only for all users

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB2033708

</td><td>

'Interactions' is applied to the sn\_customerservice\_case table instead of 'Interaction' resulting in an invalid query

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB2028756

</td><td>

While upgrading from Yokohama to Zurich, a skipped error occurs

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB2056140

</td><td>

The user can't delete forum permissions using the 'Delete' option

</td></tr><tr><td>

Customer Service Management

</td><td>

PRB2062954

</td><td>

Creating knowledge from a case doesn't populate the kb\_issue field

</td></tr><tr><td>

Database Compaction

</td><td>

PRB1922509

</td><td>

The 'DB Compaction' job left triggers and the 'TMP' table behind after a node restart stopped the job

</td></tr><tr><td>

Database Compaction

</td><td>

PRB1972914

</td><td>

The 'DB Compaction' job doesn't support tables without the sys\_id column

</td></tr><tr><td>

Database Indexes

</td><td>

PRB1975183

</td><td>

Creating an index on a few columns with an already existing column causes a drop of the redundant index and a 'AccessExclusiveLock' on a table

</td></tr><tr><td>

Database Indexes

</td><td>

PRB1938499

</td><td>

If an element is in a compound index, modifying the max\_length on a table to &gt; 255 throws a SQLException

</td></tr><tr><td>

Database Indexes

</td><td>

PRB2051109

</td><td>

ColumnStore index creation fails to create via UI

</td></tr><tr><td>

Database Indexes

</td><td>

PRB1891295

</td><td>

'Drop Index' functionality wasn't following the complete drop index process

</td></tr><tr><td>

Database Indexes

</td><td>

PRB1966408

</td><td>

There should be validation or guardrails on Index via UI

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1853004

</td><td>

Oracle 'GroupBy a reference field' in Korean fails and throws a syntax error

</td></tr><tr><td>

Database Persistence

</td><td>

PRB2052093

</td><td>

There's a three-way deadlock between Preferences, TableDescriptor, and TableRotationExtension, which causes node restarts in production

</td></tr><tr><td>

Database Persistence

</td><td>

PRB2052227

</td><td>

The fix for PRB1939323 does not cover when sorting on a translated field that is not directly on the table

</td></tr><tr><td>

Database Persistence

</td><td>

PRB2034868

</td><td>

GlideAggregate setWindow\(\), setLocation\(\), and getLocation\(\) are ineffective on Zing \(TEXTQUERY\) keyword search queries

</td></tr><tr><td>

Database Persistence

</td><td>

PRB1962784

</td><td>

Property glide.db.alter\_large\_table\_threshold can't be set large enough

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1969193

</td><td>

SELECT isn't generated correctly for a script when a business rule is active with ORDER BY for Postgres

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1985672

</td><td>

Executing a 'Select' statement with more than 64K items inside of an 'in' clause fails

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB2037003

</td><td>

TableUpgrade.updateDictionaryReadOnlyOption throws NPE during source control install

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1928920

</td><td>

ScheduleDateTime extending String \(and mapped to VARCHAR\) causes string comparison instead of DateTime comparison in SQL queries

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1982857

</td><td>

An incorrect RLQuery SQL is generated when a hybridized table is included

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1769558

</td><td>

Reparenting should poll up to 60 seconds, checking every 5 seconds for fields to become valid when deleting from the alias table

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB2005985

</td><td>

Dot-walk queries with identical field names generate incorrect SQL when the referenced field is a synchronized field in CMDB

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1939121

</td><td>

WhereClause isn't correctly identified when language translations are enabled for a catalog variable with reference to sc\_cat\_item

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB2000129

</td><td>

In RaptorDB, there's a syntax error or access rule violation detected by the database: 'ERROR: cannot cast type timestamp with time zone to numeric Position: 23'

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1967640

</td><td>

Clean up the dangling temp table

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1988680

</td><td>

While initializing a RecordHierarchy, path update events should not be recorded for processing

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB2011712

</td><td>

Gs.now\(\) generates incorrect SQL if glide.sys.date\_format property is dd-MM-yyyy

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB2012968

</td><td>

Syntax error or access rule violation is detected by the database when ordering by GlideDBFunctionCaseBuilder

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB2021472

</td><td>

A text-search query combined with a HAVING-based related-list condition \(count = 0\) silently logs an SqlException but returns 0 results

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB2032070

</td><td>

TableChunkCopier.java doesn't update Postgres sequences in copy\(\)

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1752546

</td><td>

There's a splunk error: 'column 'sys\_trigger0.sys\_id' must appear in the GROUP BY clause or be used in an aggregate function'

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1922843

</td><td>

The CMDB Data Manager Policy and Attributes view are not showing

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1943465

</td><td>

'Is Not' with multiple 'OR' Conditions results in incorrect results

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1965015

</td><td>

QueryBreadcrumbs ChoiceList generation can lead to memory issues when ran on a very large QueryStrings

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1969971

</td><td>

The postgress database function fails if it needs to cast string to an integer

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1976716

</td><td>

Querying and ordering by a reference field when referencing a rotated table doesn't work

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1980790

</td><td>

The 'SUBSTR' function is case sensitive on RaptorDB

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1989461

</td><td>

Attempts to reconcile a RH in pending\_create or pending\_initialize states should repost those events

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1995000

</td><td>

The generated SQL based on variables 'variable\_sys\_id' CONTAINS 'value' doesn't join the referenced table

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1995281

</td><td>

Instant alter on a large table times out after 3 minutes and enters an infinite DDL retry loop, and is an upgrade blocker

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1995482

</td><td>

Filters aren't applied on some cyphers

</td></tr><tr><td>

Database Persistence - Data Access

</td><td>

PRB1887006

</td><td>

Duplicate tables with different capitilization cause migration validation failures

</td></tr><tr><td>

Database Persistence - Data Dictionaries

</td><td>

PRB2015274

</td><td>

Enhancing VIndexCreatorTable to allow read-only access in v\_index\_creator.do

</td></tr><tr><td>

Database Persistence - Data Dictionaries

</td><td>

PRB2030283

</td><td>

Failure to insert a record into sys\_trigger leads to clogging of the DB with temporary tables

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB2076226

</td><td>

Automated Test Framework \(ATF\) test\_execution rollback context is set to 'invalid/error' for runtime execeptions

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB2026557

</td><td>

The 'Delete All Records' UI action uses legacy RecordUtils script include \(deleteMultiple\) to delete data instead of creating a Data Management Delete Job

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1971093

</td><td>

One-time update/delete job conditions shouldn't contain Javascript

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB2016600

</td><td>

DmRuleBacklogEstimationJob has a count timeout and causes outdated 'Records in Backlog' in the Data Management console

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB2016927

</td><td>

Avoid reparenting the 'Columnar' archive table with a documentID reference after restoring a record

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB2022327

</td><td>

Data Management Console fails to load live archive object storage data

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB2045306

</td><td>

Live Archive should not be installed on RaptorDB Pro instances until the product is ready

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB2052226

</td><td>

CompactionUtil table exclusion for doesn't exclude cmdb$par1/cmdb$par2

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1894495

</td><td>

The 'Glide clone' API isn't generating delete statements for a hybrid table

</td></tr><tr><td>

Database Persistence - Data Management

</td><td>

PRB1989825

</td><td>

The Data Management 'Delete' job isn't changing state even when the job fails due to lack of permissions with the temporary user 'data.management.admin.user'

</td></tr><tr><td>

Database Persistence - Data Queries

</td><td>

PRB2036970

</td><td>

Contains / Does Not Contain filter operator returns no results on string-with-choices fields in child table lists on PostgreSQL instances

</td></tr><tr><td>

Database Persistence - Data Queries

</td><td>

PRB2000631

</td><td>

A large sys\_id optimization returns incorrect results \(glide.db. first\_pass\_ sys\_id\_list.enable\)

</td></tr><tr><td>

Database Persistence - Data Queries

</td><td>

PRB2015830

</td><td>

UpdateMIUserLastUsedTime scheduled job is failing with GlideSQLException in postgres instance

</td></tr><tr><td>

Database Persistence - Data Queries

</td><td>

PRB1983339

</td><td>

QueryTermParser shouldn't throw a null pointer exception on a bad input

</td></tr><tr><td>

Database Persistence - Data Queries

</td><td>

PRB1988313

</td><td>

'Group by' doesn't work in the 'List' view for inactive choice values for choice columns

</td></tr><tr><td>

Database Persistence - Data Queries

</td><td>

PRB1998163

</td><td>

When CMDB has over 1664 columns across all partitions, RaptorDB won't support a fully hydrated 'SELECT' projection

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1998815

</td><td>

Default semaphore get stuck on org.postgresql.jdbc.ResourceLock.obtain

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB2025452

</td><td>

Query routing categories are not mapped to a RR pool are disregarded, and queries tagged with the category get routed to 'primary' by default

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1986698

</td><td>

A query is routed to a read replica even though the table has been migrated to gateway

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1974343

</td><td>

A query hint isn't including the change number and is causing the hint to be ignored

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB2074822

</td><td>

A node thread is hung in setTimerTask within reentrant lock MariaDB

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1920786

</td><td>

There is an excessive WARN message from DBResourceUsageSyncSweeperJob for a pool without sys\_status

</td></tr><tr><td>

Database Persistence - Data Scale

</td><td>

PRB1941471

</td><td>

Logging for only the primary\_hash in the application logs

</td></tr><tr><td>

Database Persistence - Graph

</td><td>

PRB2017435

</td><td>

The cypher graph query generates an invalid SQL JOIN ordering when the 'Before Query' rule injects dot-walk conditions on extended tables

</td></tr><tr><td>

Database Persistence - Graph

</td><td>

PRB2021889

</td><td>

GlideRecord.setCategory\(\) is used in a way that prevents routing to read-replica databases

</td></tr><tr><td>

Database Persistence - Graph

</td><td>

PRB1975735

</td><td>

Duplicate query executions for sys\_user during sample script iteration/execution

</td></tr><tr><td>

Database Persistence - Graph

</td><td>

PRB2007566

</td><td>

com.glide.db.DBGraphApiException has an error executing cypher

</td></tr><tr><td>

Database Persistence - Graph

</td><td>

PRB2064975

</td><td>

The sub graph time increased ~200ms

</td></tr><tr><td>

Database Persistence - WDF

</td><td>

PRB2076449

</td><td>

A node can't start if there's a 'Formula' field on sys\_user

</td></tr><tr><td>

Database Persistence - WDF

</td><td>

PRB1971442

</td><td>

\[Non\_Sys\_ID\_Support\] IllegalStateException thrown when executing GlideDBQuery on non\_sys\_id table

</td></tr><tr><td>

Database Persistence - WDF

</td><td>

PRB2040034

</td><td>

In Australia, all database columns that start with a number have 'yy\_' added to the start of the name, causing a syntax error

</td></tr><tr><td>

Database Rotation

</td><td>

PRB1954418

</td><td>

A sys\_created\_on filter doesn't work for a shard-type rotation

</td></tr><tr><td>

Database Views

</td><td>

PRB2062500

</td><td>

In the 'Database' view, a 'Where' clause validator incorrectly flags boolean-to-boolean field comparisons as invalid, causing an error and a hung report filter picker

</td></tr><tr><td>

Database Views

</td><td>

PRB1971341

</td><td>

'Before query' business rules don't run on database views on a domain separated environment

</td></tr><tr><td>

Database Views

</td><td>

PRB1981902

</td><td>

The Raptor DB view has mixed case prefix and '.' combination errors out

</td></tr><tr><td>

Data Fabric Table Glide Services

</td><td>

PRB2002718

</td><td>

Handle the entitlement check of the new ZCC App

</td></tr><tr><td>

Data Management Console

</td><td>

PRB1949832

</td><td>

The 'Physical Table Stats Gatherer' job runs long due to an influx of a query with the hash 943940198

</td></tr><tr><td>

Data Management Console

</td><td>

PRB1979259

</td><td>

The data on Data Management Console \(DMC\) is inconsistent when the 'Stats gatherer' job runs

</td></tr><tr><td>

Data Management Console

</td><td>

PRB2030039

</td><td>

'Physical Table Stats Gatherer' is triggered, which does 'UNION ALL' for rotated tables

</td></tr><tr><td>

Data Management Console

</td><td>

PRB2069750

</td><td>

The 'Driver' table list for sys\_attachement in Data Management Console \(DMC\) doesn't refect actual attachement sizes

</td></tr><tr><td>

Data Management Console

</td><td>

PRB2077418

</td><td>

'Physical Table Stats Gatherer' job logs handled per-table failures at ERROR

</td></tr><tr><td>

Data Management Console

</td><td>

PRB1974031

</td><td>

A repeated query with the hash -423529530 comes up when running stats gatherer

</td></tr><tr><td>

Data Management Console

</td><td>

PRB1976888

</td><td>

StatsGatherer isn't collecting stats when it runs in parallel with a SNC provision job

</td></tr><tr><td>

Data Management Console

</td><td>

PRB1995608

</td><td>

The 'Attachment' table size is not shown, or is shown incorrectly, in the top 10 largest tables

</td></tr><tr><td>

Data Policies

</td><td>

PRB1987139

</td><td>

The Data Policy 'required fields' message doesn't use table extension field label overrides

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB2019088

</td><td>

The deAnonymize API non-deterministically leaves anonymized tokens \(for example, GAIC\_xx\) when overlapping patterns are configured

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB2040595

</td><td>

Post-clone anonymization of child workers is incorrectly cancelled due to parent job type mismatch

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB2025404

</td><td>

DataPrivacyCacheManager cache refresh holds Preferences lock and waits on ReplicationAdvisor causing instance to hang in Glide.init

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB2031271

</td><td>

Rollback of a scheduled anonymization job doesn't refresh the activity stream UI for 'Journal' fields \(work\_notes, comments\)

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB2001965

</td><td>

'Run once' Data Privacy jobs take a long time to complete on large tables

</td></tr><tr><td>

Data Privacy \(Classic\)

</td><td>

PRB2003489

</td><td>

Validation throwing DATA\_PRIVACY\_API\_ERROR\_001 should only be performed if there's an active privacy policy

</td></tr><tr><td>

Data Snapshots

</td><td>

PRB2009990

</td><td>

'Show records' shows scores one day ahead for a daily source

</td></tr><tr><td>

Data Snapshots

</td><td>

PRB1999238

</td><td>

There's a node outage due to an out-of-memory error as a result of a memory bloat in ScriptableCDCDataCollector .jsFunction\_mineAllChanges\(\)

</td></tr><tr><td>

Date Picker

</td><td>

PRB2064283

</td><td>

Date picker in indicator in Platform Analytics doesn't work as expected when the language is changed to German in Australia

</td></tr><tr><td>

Date Picker

</td><td>

PRB2054724

</td><td>

A date field \(glide\_date\) fails to save when the session language is French and the date format is dd-MMM-yyyy

</td></tr><tr><td>

Decision Table \(Family\)

</td><td>

PRB2015239

</td><td>

A decision table Excel export fails when input column names contain special characters

</td></tr><tr><td>

Decision Table \(Family\)

</td><td>

PRB1974061

</td><td>

Delegated developer \(sn\_dd\_XXXXX\_decisiontables\) can't add the 'Result' column

</td></tr><tr><td>

Delegated Development and Deployment

</td><td>

PRB2061071

</td><td>

GlideRecordSecure is slow when querying \[sys\_email\] as a non-admin user with the delegated\_developer role

</td></tr><tr><td>

Demand Management

</td><td>

PRB2020276

</td><td>

The 'Create Epic' UI action doesn't work in Australia

</td></tr><tr><td>

Demand Management

</td><td>

PRB2015551

</td><td>

Assessment Notification for Demand doesn't trigger as expected

</td></tr><tr><td>

Demand Management

</td><td>

PRB2018621

</td><td>

The 'Identify Similar Demands' UI action fails to find similar demands because the AI Search table indexes don't work

</td></tr><tr><td>

Demand Management

</td><td>

PRB2035713

</td><td>

There's issues creating monetary benefits from a non-monetary benefits related records

</td></tr><tr><td>

Demand Management

</td><td>

PRB2000827

</td><td>

When deleting a decision \(dmn\_decision\) record in a project, the fields 'WBS' and 'WBS Order' are calculated for the remaining decision records

</td></tr><tr><td>

Dependency Views

</td><td>

PRB1882781

</td><td>

The relationship between nodes always shows up as 'Depends on::Used by' even though the relationship in cmdb\_rel\_ci is different for Dependency View

</td></tr><tr><td>

Developer Sandboxes

</td><td>

PRB2054240

</td><td>

The scheduler claim mutex \(sys\_mutex\) isn't sandbox-aware and forces DSB nodes to contend for a cluster-wide lock, causing scheduled-job pickup delay

</td></tr><tr><td>

Developer Sandboxes

</td><td>

PRB1982247

</td><td>

The 'DSB oauth' flow fails for instances with a custom url configured as an instance URL

</td></tr><tr><td>

Developer Sandboxes

</td><td>

PRB1844461

</td><td>

Sandbox initialization errors may cause the inability to create sandboxes on RaptorDB

</td></tr><tr><td>

Developer Sandboxes

</td><td>

PRB1995018

</td><td>

NowMQ messages can be claimed by an unexpected recipient

</td></tr><tr><td>

Developer Sandboxes

</td><td>

PRB2015080

</td><td>

The scheduled flow inherited from the main instance does not run automatically on the sandbox instance

</td></tr><tr><td>

Developer Sandboxes

</td><td>

PRB2029089

</td><td>

Users are rerouted to a base instance when using the 'Change update set' link

</td></tr><tr><td>

Developer Sandboxes

</td><td>

PRB1978622

</td><td>

Post clone DSB recovery fails to start

</td></tr><tr><td>

Discovery

</td><td>

PRB1746232

</td><td>

Schedules attempt app/basic authentication credentials outside of the credential alias configuration

</td></tr><tr><td>

Discovery

</td><td>

PRB2012212

</td><td>

Discovery status stale path skips the phase transition for multi-phase behaviors

</td></tr><tr><td>

Discovery

</td><td>

PRB1898499

</td><td>

ColdFusion application server discovery error

</td></tr><tr><td>

Discovery

</td><td>

PRB1669009

</td><td>

PatternSummaryLogger produces too many logs, causing unnecessary RAM \(Risk Assessment Methodology\) usage

</td></tr><tr><td>

Discovery

</td><td>

PRB2023232

</td><td>

Some Sybase processes running on Linux don't meet the classifier conditions to trigger the sybase pattern, resulting in an incomplete Discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB1885616

</td><td>

During the serverless Nutanix PrismCentrals schedule discovery, the execution of all the patterns with the same IP are shown in the discovery log

</td></tr><tr><td>

Discovery

</td><td>

PRB1614055

</td><td>

Uinterruptible power supply \(UPS\) discovery does not populate 'Discovery Source' and 'Most Recent Discovery' for alarms, inputs, and outputs

</td></tr><tr><td>

Discovery

</td><td>

PRB1998432

</td><td>

The 'Create OS SW Record' business rule fails because the cmdb\_sam\_sw\_install table is missing

</td></tr><tr><td>

Discovery

</td><td>

PRB1936267

</td><td>

The warning log 'Other TCP connection states found: \['TIME\_WAIT','SYN\_SENT'\]' appears during Windows Discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB2009621

</td><td>

Sub account \(LP\) deletion strategy is retiring logical datacenter CIs

</td></tr><tr><td>

Discovery

</td><td>

PRB1988150

</td><td>

The IP duplicate/jail mechanism interferes with the new counting mechanism

</td></tr><tr><td>

Discovery

</td><td>

PRB1988376

</td><td>

Pattern log errors are inserted into an automation\_error\_msg without checking automation\_error\_msg\_blacklist

</td></tr><tr><td>

Discovery

</td><td>

PRB1979188

</td><td>

DeviceL3Mapping SI is ignoring the 'glide.discovery. L3\_mapping.use\_location' property

</td></tr><tr><td>

Discovery

</td><td>

PRB2059465

</td><td>

Discovery patterns fail to launch for sub-accounts/datacenters when glide.discovery.retire\_stale\_accounts is turned on

</td></tr><tr><td>

Discovery

</td><td>

PRB1998033

</td><td>

A cluster\_status is marked offline when the CIs under this cluster are discoverable

</td></tr><tr><td>

Discovery

</td><td>

PRB1982938

</td><td>

Discovery via Just Enough Administration \(JEA\) isn't working when the CNG certificate is used

</td></tr><tr><td>

Discovery

</td><td>

PRB1677745

</td><td>

The 'Virtual Computer Check' business rule is not creating 'Virtualized by:: Virtualizes' relationship

</td></tr><tr><td>

Discovery

</td><td>

PRB2028276

</td><td>

Errors in the System Log / Error Log observed since Zurich reading 'Failed trying to execute on connection– Duplicate Key Violation in discovery\_cloud\_temp\_results Table'

</td></tr><tr><td>

Discovery

</td><td>

PRB2029131

</td><td>

Discovery isn't updating the install status of VMware vCenter instances \[cmdb\_ci\_vcenter\] to 'installed'

</td></tr><tr><td>

Discovery

</td><td>

PRB2031465

</td><td>

APC UPS sensor incorrectly populatrs battery\_last\_replaced on cmdb\_ci\_ups with the discovery run date instead of the value returned by the device

</td></tr><tr><td>

Discovery

</td><td>

PRB2004209

</td><td>

An itil user gets a CloudWizardDiscovery permission error on a change request state change

</td></tr><tr><td>

Discovery

</td><td>

PRB1918575

</td><td>

Users need visibility into the 'full' version on windows systems, including revision

</td></tr><tr><td>

Discovery

</td><td>

PRB1950473

</td><td>

The VMware vCenter VM Tags probe fails SSL certificate validation when Discovery is run directly against the vCenter instead of a host, as the FQDN is not discovered and the probe enforces SAN validation using the IP address

</td></tr><tr><td>

Discovery

</td><td>

PRB2009180

</td><td>

The 'Parse File' operation fails with unparseable date on AIX hosts using istat

</td></tr><tr><td>

Discovery

</td><td>

PRB2011984

</td><td>

The refresh member accounts process doesn't correct broken cmp\_discovery\_ldc\_config references

</td></tr><tr><td>

Discovery

</td><td>

PRB2015096

</td><td>

There's excessive MID logging due to sensitive data redaction

</td></tr><tr><td>

Discovery

</td><td>

PRB2018247

</td><td>

Incorrect handling of install status for VDIs in the 'Cascade deprovisioned status to server' business rule

</td></tr><tr><td>

Discovery

</td><td>

PRB2020524

</td><td>

There's duplicate Runs On :: Runs relationships created between the Application CI \(cmdb\_ci\_appl\_generic\) and the host server \(Windows server\)

</td></tr><tr><td>

Discovery

</td><td>

PRB2022233

</td><td>

The UI actions 'Export VMs Information ZIP' and 'Export vCenter Hardware ZIP' cause out of memory errors and the node restarts when the GLAS plugin isn't installed

</td></tr><tr><td>

Discovery

</td><td>

PRB2022485

</td><td>

MID Server fails to parse CI Types payload due to label attribute type conflict caused by CMDB tables containing a label column

</td></tr><tr><td>

Discovery

</td><td>

PRB2024628

</td><td>

TLS/SSL certificate probes for FTP servers on port 21 are never triggered

</td></tr><tr><td>

Discovery

</td><td>

PRB2030659

</td><td>

Amazon AWS Resource Inventory Pattern is not LP and takes long to run

</td></tr><tr><td>

Discovery

</td><td>

PRB2031993

</td><td>

SVC storage server duplication via discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB2033794

</td><td>

SNMP Discovery does not create or update printer supply records for CIs classified as cmdb\_ci\_mfp\_printer

</td></tr><tr><td>

Discovery

</td><td>

PRB2034157

</td><td>

NetApp Storage Cluster-Mode delay caused by credential cycling in NetAppConnectionFactory.java

</td></tr><tr><td>

Discovery

</td><td>

PRB2039407

</td><td>

Azure Cloud Discovery processes retired LDCs, causing duplicate AKS pattern triggers and schedule cancellation

</td></tr><tr><td>

Discovery

</td><td>

PRB2053688

</td><td>

When cascasing 'Operational Status' from a virtual machine instance to a server, it won't work for 'onInsert' and the relationship types 'Instantiates' and 'Instantiated by'

</td></tr><tr><td>

Discovery

</td><td>

PRB1573302

</td><td>

Cloud Discovery for vCenter with multiple datacenters creates a duplicate relationship

</td></tr><tr><td>

Discovery

</td><td>

PRB1647808

</td><td>

Prevent the CIM identity sensor from setting an incorrect IP address and location for remote devices

</td></tr><tr><td>

Discovery

</td><td>

PRB1658857

</td><td>

Discovery infra should provide a way for the pattern to detect whether an error occured

</td></tr><tr><td>

Discovery

</td><td>

PRB1698977

</td><td>

Discovery is not fully supporting Solaris LDOM server discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB1880029

</td><td>

The installed software retrieval process for Windows Discovery is breaking even if one software component has a registry issue, resulting in an inefficient way of pulling data

</td></tr><tr><td>

Discovery

</td><td>

PRB1924560

</td><td>

The SDK is out of date

</td></tr><tr><td>

Discovery

</td><td>

PRB1924698

</td><td>

Improve the memory usage of Shazzam when discovering tens of thousands of devices that have the WBEM port open and 'delay\_wbem = true \(default\)'

</td></tr><tr><td>

Discovery

</td><td>

PRB1930417

</td><td>

Solaris software installed via IPS are not discovered by base instance Solaris installed software

</td></tr><tr><td>

Discovery

</td><td>

PRB1950428

</td><td>

Improvements needed in the credential-less NMAP discovery to add additional options for receiving better guesses/results

</td></tr><tr><td>

Discovery

</td><td>

PRB1957772

</td><td>

The IP collection summary is unable to reflect the new subnet after the update

</td></tr><tr><td>

Discovery

</td><td>

PRB1971406

</td><td>

The 'Get Process' step doesn't work when the 'Command Line' filter and 'Use ACC connection' is used

</td></tr><tr><td>

Discovery

</td><td>

PRB1975580

</td><td>

The 'Discovery - Update Range Item IP List' business rule is slow

</td></tr><tr><td>

Discovery

</td><td>

PRB1980172

</td><td>

Discovery creates software install records with blank display names

</td></tr><tr><td>

Discovery

</td><td>

PRB1993041

</td><td>

The Application Dependency Mapping \(ADM\) probe returns a malformed payload with an error: 'EvaluatorException\(new ProbePostProcessor\('

</td></tr><tr><td>

Discovery

</td><td>

PRB1993522

</td><td>

There's broken doc links on the Discovery configuration console

</td></tr><tr><td>

Discovery

</td><td>

PRB1994473

</td><td>

CI-type information on a Discovery's patterns' table list view doesn't match what is found when users open the pattern in Pattern Designer

</td></tr><tr><td>

Discovery

</td><td>

PRB1998440

</td><td>

Users are unable to populate the 'Name' field for Dynamic Resource Scheduling \(DRS\) Virtual Machine \(VM\) configuration CIs via Discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB2001732

</td><td>

discovery\_status is set to 'Complete' when launching cloud probes

</td></tr><tr><td>

Discovery

</td><td>

PRB2002210

</td><td>

There's an invalid query during Oracle GLAS discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB2003122

</td><td>

The Amazon Web Services \(AWS\) resource inventory box pattern stopped launching after Zurich for a non-US date format

</td></tr><tr><td>

Discovery

</td><td>

PRB2005671

</td><td>

Citrix License Server is recognized on non-Citrix devices

</td></tr><tr><td>

Discovery

</td><td>

PRB2005737

</td><td>

ACL is blocking a base instance table after installing the Discovery Core application

</td></tr><tr><td>

Discovery

</td><td>

PRB2006310

</td><td>

VMware License Keys are incorrectly associated with retired vCenter during Standalone ESXi Discovery

</td></tr><tr><td>

Discovery

</td><td>

PRB2007003

</td><td>

Discovery Anomaly Detection incorrectly adds 24 hours to the reported duration if the time format is 12 hour and the discovery schedule spans midnight

</td></tr><tr><td>

Discovery

</td><td>

PRB2007308

</td><td>

IIS Discovery Pattern incorrectly maps multiple hostnames to a different virtual directory due to a substring match in the 'Filter by Hostname' step

</td></tr><tr><td>

Discovery

</td><td>

PRB2007670

</td><td>

Discovery Schedule is consistently stuck for over two hours at SSHTerminalInteractiveCommand

</td></tr><tr><td>

Discovery

</td><td>

PRB2008329

</td><td>

When Discovery fires discovery.completed and discovery.canceled events multiple times, any 'run after' schedules are triggered twice

</td></tr><tr><td>

Discovery

</td><td>

PRB2008562

</td><td>

Citrix Discovery pattern doesn't populate the 'Version' field

</td></tr><tr><td>

Discovery and Service Mapping Patterns

</td><td>

PRB1917730

</td><td>

Collect middleware data for the weblogic pattern extension for Oracle GLAS because it times out when running 'find commands in some environments

</td></tr><tr><td>

Discovery and Service Mapping Patterns

</td><td>

PRB1956770

</td><td>

WMQ On the Unix pattern \(Step 3: Check process name to match runmqlsr\) is not finding two IBM MQ manager instances

</td></tr><tr><td>

Discovery Probes and Sensors

</td><td>

PRB1762069

</td><td>

StorageReconciler for Fibre Channel \(FC\) is chatty, consider having this toggleable with a system property

</td></tr><tr><td>

Discovery Schedule

</td><td>

PRB2004914

</td><td>

Slow queries observed with query hashes 1628558267 and 1211341402

</td></tr><tr><td>

Document Intelligence Unified Backend

</td><td>

PRB2018937

</td><td>

Local naively checks for empty text rather than 'blank' when classifying PDF pages for DocReader

</td></tr><tr><td>

Document Management

</td><td>

PRB1972043

</td><td>

The Document Template PDF creation throws a Null Pointer Exception when the template contains a table of contents

</td></tr><tr><td>

Document Management

</td><td>

PRB1973823

</td><td>

The redaction tool is failing to apply the blackout to the specified section, and instead places it randomly

</td></tr><tr><td>

Document Management Services

</td><td>

PRB2033668

</td><td>

The 'Document Display' component displays different message button tooltips

</td></tr><tr><td>

Document Viewer

</td><td>

PRB2021741

</td><td>

When printing a PDF from the $viewer.do UI page, an extra page is appended to the end of the PDF in the print dialog.

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1609880

</td><td>

The 'Attachments' content in Knowledge Articles is misaligned for IOS device Mobile view

</td></tr><tr><td>

Document Viewer

</td><td>

PRB1707280

</td><td>

A small lag while loading the document in an iFrame while using the Document Viewer in Now Mobile

</td></tr><tr><td>

Domain Separation

</td><td>

PRB2039046

</td><td>

Domain Selector displays duplicate domain names in Recent Selections after re-opening the domain picker

</td></tr><tr><td>

Dynamic Scheduling

</td><td>

PRB2052021

</td><td>

Auto-assignment doesn't work if locations from the task or agents don't have a valid latitude/longitude

</td></tr><tr><td>

Dynamic Translation for Agent Chat

</td><td>

PRB2032934

</td><td>

Agent Chat is unable to identify if Dynamic Translation is enabled/not \(only\) when the Live Agent is in a non-global domain

</td></tr><tr><td>

Dynamic Translation for Agent Chat

</td><td>

PRB1988564

</td><td>

If Dynamic Translation for Agent Chat \(DTAC\) translation fails from agent to requester, the original message isn't sent

</td></tr><tr><td>

Dynamic Translation for Agent Chat

</td><td>

PRB1973276

</td><td>

Dynamic translations aren't working in Agent Chat at the end of a conversation in the 'Internal Transcript' field

</td></tr><tr><td>

Dynamic Translation for Agent Chat

</td><td>

PRB2030959

</td><td>

When using the live agent in Now Assist Virtual Agent \(NAVA\), the disclaimer message at the bottom is dynamically translated based on the agent's session language

</td></tr><tr><td>

Dynamic Translation for Agent Chat

</td><td>

PRB1973276

</td><td>

Dynamic translations aren't working in Agent Chat at the end of a conversation in the 'Internal Transcript' field

</td></tr><tr><td>

Edge Encryption

</td><td>

PRB2052514

</td><td>

Service Operations Workspace displays an error when a task is saved which contains an empty multi-row variable set, making saving impossible

</td></tr><tr><td>

Edge Encryption

</td><td>

PRB2016789

</td><td>

Edge Encryption mass decryption job doesn't support tables with edge encrypted data inside a field value

</td></tr><tr><td>

Edge Encryption

</td><td>

PRB2037206

</td><td>

Form fails to load in Workspace when encrypted String field contains line breaks

</td></tr><tr><td>

Edit List Columns

</td><td>

PRB2033875

</td><td>

After removing columns from the 'Personalize fields' on the Project Workspace 'All Projects' list, the 'Number' field hyperlink disappears

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1948259

</td><td>

**Select All** and **Delete** buttons aren't working in Email Viewer

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1997659

</td><td>

There's duplicate recipients in email notifications in HR Records

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2019162

</td><td>

Introduce batch support for subscriptions in NotificationRecipientBuilder

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2036855

</td><td>

Agent workspace case emails display multiple 'To' names if the email recipient has multiple contact records

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2010416

</td><td>

In CSM/FSM configurable workspace, adding attachments from the record within compose email doesn't work

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1994854

</td><td>

For an inbound action, required roles isn't working as expected

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2016579

</td><td>

The email body disappears when the email is composed from workspace

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1998487

</td><td>

In an HR scoped application in the Workspace UI, the Email Client configuration 'recipient qualifier' displays all the domain user email addresses instead of displaying the specific email domain as configured in Recipient Qualifier

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2003838

</td><td>

The size of the **Send email** button was reduced after a Zurich upgrade in legacy Agent Workspace

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2034124

</td><td>

Empty error message when sending an email reply from Workspace with too many attachments

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2054658

</td><td>

Users report receiving notifications regardless of if they're turned off in user preferences

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2009860

</td><td>

Users subscribed to a notification aren't included in the recipient list

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2017604

</td><td>

Opening the notification window from the Preferences profile takes a long time

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2031156

</td><td>

Email notification header contains space

</td></tr><tr><td>

Email Notifications

</td><td>

PRB2035138

</td><td>

A delegated user doesn't receive emails in which they are CC'd

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1905337

</td><td>

The **Send email** button is not workin and no error is shown

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1970107

</td><td>

There's an issue with adding an email template in Zurich

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1971931

</td><td>

glide.smtp.fail\_message\_ids is not honored if the email server sends 'SendFailedException'

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1984794

</td><td>

Ignored inbound emails are updated in the target table

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1985232

</td><td>

Emails are continually processed when using the 'glide.email.test.user' property

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1988946

</td><td>

'Compose email' in a workspace isn't updating the font family and size on the editor toolbar when a email client template is applied

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1995722

</td><td>

A user is getting a 'Not Authorized' message to send an email error on Email Client

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1996368

</td><td>

A Now Assist pop-up model header doesn't get translated

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1997184

</td><td>

Duplicate cmn\_notif\_message records are created from the 'Preview Notification' functionality

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1997575

</td><td>

When updating attachments in the 'Email compose' window, the 'Email saved' event isn't triggered

</td></tr><tr><td>

Email Notifications

</td><td>

PRB1997699

</td><td>

The 'Approval Activity' section on a requested item approval request email is incorrect

</td></tr><tr><td>

Embedded Help

</td><td>

PRB2036697

</td><td>

Plugin dependency 'com.glide.scope.access.restricted\_caller' missing in the app-help-setup plugin file

</td></tr><tr><td>

Embedded Help

</td><td>

PRB1912461

</td><td>

Default values for properties in an instance must change due to the docs' site URL change

</td></tr><tr><td>

Employee Relations Case Management

</td><td>

PRB2028528

</td><td>

The ER case with the 'Agent Can Add An Approval' HR Service case option functionality does not work

</td></tr><tr><td>

Employee Taxonomy Framework

</td><td>

PRB2007083

</td><td>

Users can't edit the system property taxonomy.category.new\_content\_job\_last\_run

</td></tr><tr><td>

Encryption

</td><td>

PRB1996287

</td><td>

When the set\_value property is turned off, several CLE data types \(journal field, translated field, phone number, etc.\) might get clear text data

</td></tr><tr><td>

Encryption

</td><td>

PRB1995748

</td><td>

A migration job incorrectly creates an active EFC when there's unmigrated data and the EFC has been inactivated by the user

</td></tr><tr><td>

Encryption Support

</td><td>

PRB1992606

</td><td>

Duplicate Attachment EFCs are created for tables

</td></tr><tr><td>

Encryption Support

</td><td>

PRB1993181

</td><td>

Flow session cloning \(PFSessionClone\) needs to load all roles, including snc\_internal

</td></tr><tr><td>

Event Management

</td><td>

PRB1975037

</td><td>

An impact calculation throws an exception when a parent isn't inherenting cmdb\_ci\_service\_auto

</td></tr><tr><td>

Event Management

</td><td>

PRB2022546

</td><td>

Tag based group is created with single Alerts where em\_agg\_group points at two alerts

</td></tr><tr><td>

Event Management

</td><td>

PRB1994838

</td><td>

The EIF Listener 'Source' field isn't correctly set for incoming events, and the extParam variable is inaccessible in JavaScript

</td></tr><tr><td>

Event Management

</td><td>

PRB1999707

</td><td>

An app node crash occurs due to OutOfMemory \(OOM\), and GroupingDebugLogger accumulates log messages even if logging is disabled

</td></tr><tr><td>

Event Management

</td><td>

PRB2015198

</td><td>

Alert activities aren't displaying correctly for the 'Maintenance' field

</td></tr><tr><td>

Event Management

</td><td>

PRB2017829

</td><td>

A fix script incorrectly marks event rules as UI16 incompatible

</td></tr><tr><td>

Event Management

</td><td>

PRB2034593

</td><td>

An event field mapping rule from the type 'Map field' using regex causes an error in event processing

</td></tr><tr><td>

Event Management

</td><td>

PRB2034657

</td><td>

An alert can be reopened automatically and be active while its CI is in maintenance, but the maintenance flag stays false

</td></tr><tr><td>

Event Management

</td><td>

PRB2037796

</td><td>

Impact calculation throws an exception when parent isn't inherenting cmdb\_ci\_service\_auto

</td></tr><tr><td>

Event Management

</td><td>

PRB2040257

</td><td>

Maintenance reset to false by CMDB maintenance check on alerts with no CI associated

</td></tr><tr><td>

Event Management

</td><td>

PRB2053994

</td><td>

There's a null pointer exception in AlertWorkNotesHandler .updateWorkNotesAnd SilentSaveOfClosedAlert

</td></tr><tr><td>

Event Management

</td><td>

PRB1927273

</td><td>

The cleanup job does not delete em\_alert\_history records that have no 'Alert' reference

</td></tr><tr><td>

Event Management

</td><td>

PRB1930730

</td><td>

The graph reuse mechanism in CMDB grouping saves graphs that can contain CIs of more than 4 hops distance

</td></tr><tr><td>

Event Management

</td><td>

PRB1949662

</td><td>

An error is logged when building tag-based services

</td></tr><tr><td>

Event Management

</td><td>

PRB1971718

</td><td>

Slow query in the 'EvtMgmtAlertActions' script include from lines 35-40

</td></tr><tr><td>

Event Management

</td><td>

PRB1980951

</td><td>

When text-based grouping is turned on, tag-based grouping doesn't work consistently

</td></tr><tr><td>

Event Management

</td><td>

PRB1990100

</td><td>

EM disable/enable jobs fix scripts unnecessarily manipulate the upgrade\_safe value during installation and upgrades

</td></tr><tr><td>

Event Management

</td><td>

PRB1990107

</td><td>

EvtMgmtAssignment GroupChoiceListBuilder fails when there are user groups with an empty name

</td></tr><tr><td>

Event Management

</td><td>

PRB1996008

</td><td>

Sometimes adjacent alerts aren't grouped even if there is a matching definition

</td></tr><tr><td>

Event Management

</td><td>

PRB1997290

</td><td>

Alert binding fails with an error: 'CI Reclassification not allowed from class: \[cmdb\_ci\_service\_by\_tags\] to \[cmdb\_ci\_service\_auto\]'

</td></tr><tr><td>

Event Management

</td><td>

PRB1998979

</td><td>

A Dynatrace alert correlation rule script makes long running queries

</td></tr><tr><td>

Event Management

</td><td>

PRB2008110

</td><td>

MID Server isn't processing V1 traps

</td></tr><tr><td>

Event Rules

</td><td>

PRB1892804

</td><td>

Multiple event rules are not always overriding the first binding rule

</td></tr><tr><td>

Excel Web Service

</td><td>

PRB2010401

</td><td>

The number of records in the exported Excel file is greater than in the list view \(sp\_rectangle\_menu\_item\) under certain conditions

</td></tr><tr><td>

External User Self-Registration

</td><td>

PRB2028497

</td><td>

The id = sn\_user\_registration page is missing vertical paddings on mobile view

</td></tr><tr><td>

External User Self-Registration

</td><td>

PRB1980450

</td><td>

For external user self-registration, ACL records created at configuration weren't registered into an update set

</td></tr><tr><td>

Field Normalization

</td><td>

PRB1981660

</td><td>

Field normalization creates duplicate sys\_audit records

</td></tr><tr><td>

Field Normalization

</td><td>

PRB1997370

</td><td>

Field Normalization cuts the version number, such as 8.1.0 turning into 8.1

</td></tr><tr><td>

File-based Discovery

</td><td>

PRB1928550

</td><td>

The FBD doesn't run on onprem instances until properties are manually updated

</td></tr><tr><td>

File-based Discovery

</td><td>

PRB2014793

</td><td>

File-based discovery doesn't terminate the background PowerShell process on the target host containing undefined environment variables \(%JAVA\_PATHS%\)

</td></tr><tr><td>

Filter Conditions

</td><td>

PRB2052369

</td><td>

Translation isn't rendered correctly in the breadcrumb

</td></tr><tr><td>

Filter Conditions

</td><td>

PRB1967809

</td><td>

The 'Edit condition' query always shows zero results until the workspace is refreshed

</td></tr><tr><td>

Flow Engine

</td><td>

PRB2003199

</td><td>

Flow execution reporting level reverts to BASIC on sub-production instances

</td></tr><tr><td>

Flow Engine

</td><td>

PRB2033276

</td><td>

Waiting flows that are cancelled do not cancel the queued up restart trigger/event

</td></tr><tr><td>

Flow Engine

</td><td>

PRB2034281

</td><td>

Flow remains in synchronous execution mode after quiescence, preventing background resumption if the flow goes to MID

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1982949

</td><td>

A dot-walked value returns a string instead of a reference when it fails on MID

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1944199

</td><td>

The slow query hash 177839002 against sys\_flow\_context\_inputs\_chunk is triggered by the table cleaner

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1943894

</td><td>

Looping over records using 'built in iterator' is significantly slower than the normal GlideRecord iteration

</td></tr><tr><td>

Flow Engine

</td><td>

PRB2033890

</td><td>

Absolute transform doesn't work with comparators

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1957527

</td><td>

The cmn\_location 'Changed' fields are empty when the name changes

</td></tr><tr><td>

Flow Engine

</td><td>

PRB2012194

</td><td>

When submitting a catalog item request, the assigned data-pill that contains a double-quote value on a single-line-text variable throws an OpException error

</td></tr><tr><td>

Flow Engine

</td><td>

PRB2037518

</td><td>

On the 'Foreground' API, the strict release thread 'should' logic should be revisited

</td></tr><tr><td>

Flow Engine

</td><td>

PRB2058235

</td><td>

The flow action 'Wait For Email Reply' output returns blank email content in subsequent flow steps

</td></tr><tr><td>

Flow Engine

</td><td>

PRB2073745

</td><td>

Revert the change to sys-property so users can enable full reporting for flow executions in production

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1898270

</td><td>

The action error evaluation is failing for Engine-V2

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1903832

</td><td>

'Not defined' is returned from fd\_data in Flow Designer

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1909229

</td><td>

The SubFlow Output value not retrieved properly in the main flow for the output type 'True/False' when the output is not assigned

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1913532

</td><td>

The approval policy input type 'reference' causes decision failure in the 'Apply change approval policy' flow action when used in a sub-flow

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1929065

</td><td>

The Engine V2 FlowPlanRetriever compiles and runs the main snapshot when it should really only compile and run the latest snapshots

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1978315

</td><td>

There's a RunTimeException on an incorrect value set to 'property' with the Mutex 'Retry' feature

</td></tr><tr><td>

Flow Engine

</td><td>

PRB1983279

</td><td>

A subflow fails when 'Run as role' contains a missing/empty child role

</td></tr><tr><td>

Flows

</td><td>

PRB1849850

</td><td>

JDBC Step results cannot be used in in-line scripts with Engine V2

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1961996

</td><td>

The flow record update action updates sys\_translated\_text only after the instance is updated to Zurich

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB2004148

</td><td>

In ServiceNow Studio, editing custom scoped git-enabled flows results in an error: 'Flow failed to autosave. Use Force save to save your work'

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB2030036

</td><td>

Error handler is not working for a particular flow

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1865994

</td><td>

A new 'p tag' line is added to the HTML Field from the flow

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB2027716

</td><td>

After changing the 'Decision' table result label, the flow still uses the previous result's label

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1819248

</td><td>

A newly added transform pill breaks compilation when run from the FlowPlanRetriever

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1861007

</td><td>

Unable to fetch the Lookup select box variable value in the flow

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1920739

</td><td>

The 'Template Value' type subflow input fields along with other fields are not all applying when the input is used later in the flow

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1944355

</td><td>

The 'Wait for' condition should not register the monitor event when it failed to register the record watcher

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1954202

</td><td>

Nested complex objects don't preserve dropped pills

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1969548

</td><td>

The subflow output with an array object is corrupted after the Zurich upgrade

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1970251

</td><td>

This script is filling in Array.Object with mandatory children, and fails to publish

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1975298

</td><td>

After moving a flow from one instance to another using an update set, the flow variable label changes to match the variable name

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1984442

</td><td>

A deeply nested DataStream action causes a property update to fail due to the size

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB1990001

</td><td>

Calling 'sn\_generative\_ai. GenAIStatsUtil\(\). logStats\(inputs\);' logs double entries in sys\_gen\_ai\_usage\_log

</td></tr><tr><td>

Flows \(Family Channel\)

</td><td>

PRB2014125

</td><td>

Remove the use of javascript prefixed reference qualifiers

</td></tr><tr><td>

Form Controller

</td><td>

PRB1798884

</td><td>

The sys\_highlighted\_value\_condition translated name / field doesn't work in the Service Operation Workspace

</td></tr><tr><td>

Form Controller

</td><td>

PRB1974940

</td><td>

An incorrect flow stage is displayed in Service Operations Workspace

</td></tr><tr><td>

Form Controller

</td><td>

PRB1990803

</td><td>

Users are unable to toggle checkboxes on system properties UI pages

</td></tr><tr><td>

Form Controller

</td><td>

PRB1945740

</td><td>

The focus does not automatically shift to the error message in Operational Technology Service Management

</td></tr><tr><td>

Form Controller

</td><td>

PRB1971831

</td><td>

There's inconsistent use of 'sysId' vs 'sys\_id' for multiInstField, which causes confusion and issues

</td></tr><tr><td>

Form Controller

</td><td>

PRB1984646

</td><td>

In Service Operations Workspace, an info message saying 'Article expired…' populates twice when opening approval records

</td></tr><tr><td>

Form Templates

</td><td>

PRB1833484

</td><td>

A workspace template with a currency-type field fails to apply

</td></tr><tr><td>

Form Templates

</td><td>

PRB1974503

</td><td>

The 'List Edit' sidebar in a workspace fails to load when a form has an html\_script field

</td></tr><tr><td>

Form Templates

</td><td>

PRB1867105

</td><td>

There's a template issue on the sn\_csm\_case\_digest\_cas table

</td></tr><tr><td>

GlideAggregate API

</td><td>

PRB1854398

</td><td>

Date filter and drilldown are not working for Business Calendar

</td></tr><tr><td>

GlideAggregate API

</td><td>

PRB1886789

</td><td>

GlideAggregate and enableSessionLanguageJoin is not consistent for Reference and Translated Text field defaults

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1958518

</td><td>

A Null Pointer Exception is thrown if a table has a GlideElement WikiText type field and queries at startup before extension points are loaded

</td></tr><tr><td>

GlideRecord

</td><td>

PRB2019311

</td><td>

An empty sys\_class\_name causes a GlideRecord\(''\) exception, breaking workspace cascade delete

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1784511

</td><td>

insertOrUpdate isn't working with optional field names

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1943503

</td><td>

Unexpected behavior when selecting tags as conditions in an SLA

</td></tr><tr><td>

GlideRecord

</td><td>

PRB1983484

</td><td>

isNewRecord always returns true for Glide Vars

</td></tr><tr><td>

Global Ranking

</td><td>

PRB2035527

</td><td>

Users aren't able to delete a scrum task from cross-scope

</td></tr><tr><td>

GraphQL API

</td><td>

PRB2014020

</td><td>

Transactions are cancelled by other transactions in the manager landing page on CSM/FSM workspace

</td></tr><tr><td>

GraphQL API

</td><td>

PRB2036180

</td><td>

GlideGraphQL exception encountered processing path: /GlideRecord\_Mutation/

</td></tr><tr><td>

GRC Platform Plugins

</td><td>

PRB2019351

</td><td>

On final approval of policy, a generated KB article is not published

</td></tr><tr><td>

GRC Platform Plugins

</td><td>

PRB2029047

</td><td>

Users are unable to create m2m records between business process and business application

</td></tr><tr><td>

Guided Tour Designer

</td><td>

PRB2036938

</td><td>

While using the guided tour for Accessibility Preferences, the tour fails when navigating to the Theme step

</td></tr><tr><td>

Guided Tour Designer

</td><td>

PRB2039102

</td><td>

Guided Tours don't auto-launch for context $pa\_dashboards\_overview

</td></tr><tr><td>

Guided Tours

</td><td>

PRB2026800

</td><td>

Content is output multiple times within a dialog, resulting in a redundant announcement of the same information for screen reader users

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1849439

</td><td>

The keyboard tab focus on the homepage is moving outside of the tour dialog, causing the dialog remains open, which is incorrect

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1868181

</td><td>

The arrow symbol \(triangular shape\) on the 'Tour' boxes is displayed as a square in high contrast mode for Guided Tours

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1976416

</td><td>

Guided tour cancelation makes it so users can't tab through the page

</td></tr><tr><td>

Guided Tours

</td><td>

PRB1978526

</td><td>

In Guided Tours, sys\_embedded\_tour\_guide.name isn't using a translatable field type, and is therefore hardcoded

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB2027080

</td><td>

KafkaTopicManager does not unwrap ExecutionException to check for TopicExistsException

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1922260

</td><td>

External port test runs when it shouldn't

</td></tr><tr><td>

Hermes \(Family\)

</td><td>

PRB1986687

</td><td>

ACL prevents topics being listed in hermes\_topic\_inspector for users without elevated privileges

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB2034563

</td><td>

Localization support is needed for unsupported locale

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1972389

</td><td>

Specific date values are announced in an incorrect language in the workspace

</td></tr><tr><td>

Horizon Component Library

</td><td>

PRB1998471

</td><td>

Strings interpolated in the parameters of the message '\{fieldType\} is \{error\}' are hardcoded

</td></tr><tr><td>

Horizon Dropdown Component

</td><td>

PRB1997821

</td><td>

The cursor isn't a pointer on dropdown items

</td></tr><tr><td>

Horizon iFrame Component

</td><td>

PRB2074065

</td><td>

Users get an error when trying to access the iFrame related configurations

</td></tr><tr><td>

Horizon Tabs Component

</td><td>

PRB2040694

</td><td>

Ribbon tab title hidden in workspace when using Hebrew language

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

</td><td>

PRB2046081

</td><td>

User registration from the CSP portal is giving error, 'There was an error proccessing the Link. Please use a valid link.'

</td></tr><tr><td>

Horizontal Portal Capabilities for Customer Service

</td><td>

PRB1995963

</td><td>

The portal language picker isn't turned on in Business Portal and Consumer Portal

</td></tr><tr><td>

Horizon Textarea Component

</td><td>

PRB2035441

</td><td>

SOW issue with scrolling on worknotes on ticket, the behavior works fine in any yokohama Instance

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2004808

</td><td>

checkForActiveActivitySets\(\) doesn't treat skipped dependencies as complete in combination and trigger, and there's a permanent journey stall after a Zurich upgrade

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1998455

</td><td>

Choices of multi-row variable sets \(MRVS\) aren't translated in the rich description of an HR case created from a record producer

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1980586

</td><td>

The 'Short Description' and 'Description' are wiped/removed when trying to mark the HR Case as 'closed incomplete' from HR Agent Workspace

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1970902

</td><td>

'Mark When Complete' is hardcoded in the Agent Workspace for HR Case Management for i18n

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1990683

</td><td>

Dot-walked fields are automatically updated with '&lt;span class='errored-field' style='color:\#ff0000;'&gt;'

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2008764

</td><td>

HR case SLA fields \(sla, sla\_breached\) updated via seperate Business Rules can cause values to become out of sync due to race conditions in some environments

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2011430

</td><td>

When attempting to perform any save action, HR Tasks aren't being saved becuase the Business Rule 'Prevent wrong catalog item on HR tasks' aborts the action

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2012496

</td><td>

Optional signing of HR Documents doesn't work as expected

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2021314

</td><td>

The 'Cancel' UI action in an HR case checks for 'mandatory' after the case is canceled

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2023321

</td><td>

In HR Agent Workspace, an HR case can be cancelled without adding a work note, causing 'undefined' to be automatically logged in the conversation section

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2027103

</td><td>

After PRB1887400, some locales are still not working

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2028166

</td><td>

There's a hard-coded sys\_id in the script include 'hr\_case'

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2035975

</td><td>

Email resolution isn't working for some sn\_hr\_core\_case\_benefits tables

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2037504

</td><td>

Unable to deactivate HR Total Rewards COE due to cross-scope access policy error

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2037937

</td><td>

HRI Ticket Attachments Widget Enforces 24 MB, ignoring system attachment size property

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2052632

</td><td>

The 'header\_config\_\*' fields are missing from the sn\_hr\_core\_service table in Zurich and Australia

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2055531

</td><td>

HR tasks are created even though the HR case is closed

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2059380

</td><td>

The pop-up message that displays when selecting the **Close complete** button or when closing the parent HR case needs to be changed

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2069346

</td><td>

HR Agents are able to see ER cases in Workspace

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1938687

</td><td>

Changes face upgrade issues from PRB1832992

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1970021

</td><td>

Slow ACL time on a case

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1979275

</td><td>

There's HR Agent Workspace performance issues for non-admin HR users

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1987521

</td><td>

Matching knowledge\_base file names causes upgrade issues

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB1998977

</td><td>

On HR Agent Workspace, there's a checklist item duplication issue

</td></tr><tr><td>

HR Service Delivery

</td><td>

PRB2006529

</td><td>

HR Cases aren't included in the average prediction precision indicator

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1992914

</td><td>

The wf\_activity 'Check if there is at least one recipient' returns false, causing the notification not to be sent

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB2006348

</td><td>

HR case number is occasionally empty due to missing global qualifer

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1974924

</td><td>

The HR Case form shows unnecessary lifecycle activities when using the 'Update Selected' menu

</td></tr><tr><td>

HR Service Delivery Case Management for Lifecycle Events

</td><td>

PRB1997601

</td><td>

Skipping an HR task then selecting any hyperlink or refresh page incorrectly redirects to the skipped HR task form

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB2010848

</td><td>

The Crtl+Shift+F shortcut for fullscreen rich text field also tries to create a favorite when used in a workspace

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB2016008

</td><td>

Images added via drag and drop into an HTML field don't automatically render height and width, causing the images to display incorrectly

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB2021973

</td><td>

Cross-origin email links are unable to be loaded and displayed

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB2038473

</td><td>

Read-only HTML fields on forms display raw HTML

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB2039485

</td><td>

Unexpected behaviour observed In HTML Field Editor when font family is changed to Verdana

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1977891

</td><td>

For HTML-type fields, the field size of the columns appear to be shrunk on forms after an upgrade to Zurich from Xanadu

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1979148

</td><td>

There's an Otto context menu UI issue for a read-only field

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB1988905

</td><td>

When a link is selected from the Incident Variable Editor, it doesn't work and throws a console error

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB2000052

</td><td>

The first letter in an HTML field in a modal disappears

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB2000167

</td><td>

In HTML-type fields, help text at the bottom is truncated depending on the window or screen size

</td></tr><tr><td>

HTML Field Type Editor

</td><td>

PRB2008279

</td><td>

In the Business Continuity Workspace, when a user selects 'Undo' in any tab in the documentation, it replaces the data from another tab

</td></tr><tr><td>

HTML Sanitizer

</td><td>

PRB2060677

</td><td>

GlideElementTranslatedHTML doesn't sanitize HTML content when saved in a non-default language via setDisplayValue\(\)

</td></tr><tr><td>

HTTP Client

</td><td>

PRB2023445

</td><td>

Outbound requests failures caused by certificate validation errors aren't propogated transparently to the REST step

</td></tr><tr><td>

HTTP Client

</td><td>

PRB2031497

</td><td>

A rest step sees Norwegian characters in the XML response body from an external API with incorrect encoding

</td></tr><tr><td>

HTTP Client

</td><td>

PRB2062121

</td><td>

MID Server REST calls fail with 'No issuer certificate found for the MID server' after upgrading to Australia, which is caused by single leaf validation

</td></tr><tr><td>

HTTP Client

</td><td>

PRB1914462

</td><td>

There's a warning log 'Invalid cluster size -1, will return'

</td></tr><tr><td>

HTTP Client

</td><td>

PRB1986204

</td><td>

The 'Test' UI action on the sys\_soap\_message\_function table causes large table handling query against ecc\_queue and causes memory contention

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB2004173

</td><td>

A certification audit produces incorrect failed results for first and last records when a template has reference-based related list conditions

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB2051724

</td><td>

Unreferenced records in cmdb\_ire\_partial\_payloads\_index

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB2026445

</td><td>

Dark Mode renders unreadable text in Duplicate CI Remediator

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1968047

</td><td>

The sys\_object\_source lookup/IRE de-duplication forces re-identification instead of using source\_native\_key

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB1988933

</td><td>

Identification and Reconciliation Engine \(IRE\) logging debug level logs as 'warn level' logs in the syslog table

</td></tr><tr><td>

Identification and Reconciliation API

</td><td>

PRB2034883

</td><td>

Users can add or edit identification rules for hardware's child classes while dynamic IRE is enabled

</td></tr><tr><td>

Identity

</td><td>

PRB2001109

</td><td>

There's a high CPU load on DB due to primary\_hash = -1114401198 and primary\_hash = 96485436 SQl queries from sys\_security\_table \_level\_audit\_ %\_processor job

</td></tr><tr><td>

Identity

</td><td>

PRB1988754

</td><td>

NHIUserTrackerDAO has a cache \(sys\_mi\_user\_cache \) which is storing GlideDateTime objects

</td></tr><tr><td>

Identity

</td><td>

PRB1995909

</td><td>

An inheritance role map link is missing on sys\_user\_has\_role

</td></tr><tr><td>

Import Set API

</td><td>

PRB1891108

</td><td>

Provide a property to easily import a transform map

</td></tr><tr><td>

Inbound API Integration Usage Framework

</td><td>

PRB1997896

</td><td>

HttpServletRequest is recycled during long transactions, which causes unhandled exceptions in HttpRequestAttributeAccessor

</td></tr><tr><td>

Inbound API Integration Usage Framework

</td><td>

PRB2000222

</td><td>

Integration Filter used to measure API Access Volumes is not applied to SOAP and JSONv2 requests

</td></tr><tr><td>

Inbound Email Actions

</td><td>

PRB2005410

</td><td>

Inline PDFs aren't visible via CSM Workspace Activity for sn\_customerservice\_case records

</td></tr><tr><td>

Incident Communications Management

</td><td>

PRB1991657

</td><td>

Communication tasks are unable to send when recipients are populated in the 'BCC' field

</td></tr><tr><td>

Incident Management

</td><td>

PRB2019059

</td><td>

Child incidents aren't reopened upon reopening the parent incident without the plugin 'Incident Management Best Practice - Kingston', but the message indicates otherwise

</td></tr><tr><td>

Incident Management

</td><td>

PRB2021749

</td><td>

The 'incident autoclose' business rule Major Incident Management plugin check returns false

</td></tr><tr><td>

Incident Management

</td><td>

PRB1978573

</td><td>

Error displayed while creating an Interaction in Service Operations Workspace \(SOW\)

</td></tr><tr><td>

Incident Management

</td><td>

PRB2002744

</td><td>

A business rule on the incident\_alert table references a non-existent 'incident\_manager' field

</td></tr><tr><td>

Indicator Management

</td><td>

PRB2052998

</td><td>

When the indicator library name ='None' with no data, sometimes data displays intermittently on some columns and rows

</td></tr><tr><td>

Innovation Management

</td><td>

PRB1600044

</td><td>

Have the 'Cross button' functionality to delete the category on idea portal if the user wants to remove the particular category from the list

</td></tr><tr><td>

Install Base Management

</td><td>

PRB1995911

</td><td>

There's a cross-scope issue with Product Catalog Management Core and Customer Service Install Base Management for the 'setWorkflow' API

</td></tr><tr><td>

Instance Clone \(Family\)

</td><td>

PRB1710330

</td><td>

When grouping by profile on clone profile exclusions, the grouping is not getting the name as its a calculated field

</td></tr><tr><td>

Instance Clone \(Family\)

</td><td>

PRB1905909

</td><td>

When setting a script in clone\_cleanup\_script table to active=false, the same script remains active=true in the clone\_profile\_cleanup\_scripts\_list table

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1780273

</td><td>

There's a NullPointerException \(NPE\) in the IDRProducerJob which prevents the cursor from advancing and halts all replication

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1629098

</td><td>

Make futures synchronous to avoid batch timeout errors

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1980394

</td><td>

'Active' turned off replication sets aren't properly turned off

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB2004240

</td><td>

Instance Data Replication \(IDR\) issues with batched seeding with CDATA-embedded declarations

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB2004487

</td><td>

Can't produce on 'Bidirectional Discrete Replication Set' \(Producer Side\) after failover

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1866436

</td><td>

Payload errors sometimes overrun the replication status, causing seeding to not process properly

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1885869

</td><td>

Legacy IDR jobs flod the logs with error messages when they can't reach Kafka via bootstrap

</td></tr><tr><td>

Instance Data Replication \(IDR\)

</td><td>

PRB1994487

</td><td>

There's log message flooding: 'java.net.UnknownHostException'

</td></tr><tr><td>

Instance Scan

</td><td>

PRB2022691

</td><td>

Instance Scan Linter Check fails on sys\_module with an error: 'Rhino error: missing ; before statement'

</td></tr><tr><td>

Instance Scan

</td><td>

PRB2009023

</td><td>

In Australia, an instance scan executed with an update set option doesn't get considered and runs a full instance scan

</td></tr><tr><td>

Instance Scan

</td><td>

PRB2063319

</td><td>

The check 'Deprecated API: Encrypter usages in Dictionary table' can sometimes time out on larger sys\_dictionary row sizes

</td></tr><tr><td>

Instance Scan

</td><td>

PRB1981277

</td><td>

An instance scan table check returns significantly fewer results than actual matching records

</td></tr><tr><td>

Instance Scan

</td><td>

PRB2007287

</td><td>

DB dump captures the contaminated sys\_status row \(glide.instancescan.queue.status='upgrade paused'\) when the server shutdown races with the active ScanQJob

</td></tr><tr><td>

Integration Authentication

</td><td>

PRB2017510

</td><td>

API policies aren't applying to scripted REST message

</td></tr><tr><td>

Integration Hub

</td><td>

PRB2027484

</td><td>

wdf\_operator &gt; sn\_mcp\_client.viewer should be under the condition 'if plugin'

</td></tr><tr><td>

Integration Hub

</td><td>

PRB2034438

</td><td>

Terminal attachment is processed before non-terminal attachments

</td></tr><tr><td>

Integration Hub

</td><td>

PRB1960752

</td><td>

Set skip\_scheduled\_cleanup to 'false' after the data stream completes

</td></tr><tr><td>

Integration Hub

</td><td>

PRB2006931

</td><td>

The error message is not cleared out when the retry is successful and the retry status code is 200

</td></tr><tr><td>

Integration Hub - Import

</td><td>

PRB1820505

</td><td>

Complex object parsing doesn't un-escape JSON

</td></tr><tr><td>

Integration Hub - Import

</td><td>

PRB1898557

</td><td>

Issue using the **Scheduling - Advanced Setup** button from the ellipsis \(...\)

</td></tr><tr><td>

Integration Hub Spokes

</td><td>

PRB2032333

</td><td>

Docker Spoke gets installed without a license and the user is unable to upgrade or uninstall

</td></tr><tr><td>

Integration Hub Steps for Action Designer

</td><td>

PRB1948807

</td><td>

The REST step resource path is not automatically encoded when certain characters are used, and throws a 'Malformed URL encountered' error

</td></tr><tr><td>

Integration Hub Steps for Action Designer

</td><td>

PRB1982989

</td><td>

In a Secure Shell \(SSH\) step in Flow Designer, it isn't possible to set the checkbox 'Long Running' from a data pill

</td></tr><tr><td>

Internationalization Features

</td><td>

PRB2036601

</td><td>

Fix country entries in core\_country table to be UTF-8 compliant

</td></tr><tr><td>

Internationalization Features

</td><td>

PRB2027846

</td><td>

Changing the country in the user preferences doesn't check the user's permission

</td></tr><tr><td>

Internationalization Features

</td><td>

PRB1977673

</td><td>

The timezone in the user's preference isn't synched with the user profile's timezone

</td></tr><tr><td>

Issue Auto Resolution for Virtual Agent

</td><td>

PRB1909776

</td><td>

Issue Auto Resolution \(IAR\) for HR links takes points to incorrect pages

</td></tr><tr><td>

ITOM Cloud Services

</td><td>

PRB2056002

</td><td>

'sn\_itom\_cloud\_svc.itomgateway\_url' and 'sn\_itom\_cloud\_svc.hermes\_topic\_config\_state' system properties do not set 'ignore cache'

</td></tr><tr><td>

IT Service Management Foundation License Control

</td><td>

PRB2021436

</td><td>

Instances should not get license restriction ACLs

</td></tr><tr><td>

JVM at Scale

</td><td>

PRB1993002

</td><td>

The add SecurityLogFileHandler stale lock recovery logs to a system log for improved visibility

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1986102

</td><td>

Fix/disable IPKI KMF diagnostics job to reduce the performance impact on downstream services

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB2007037

</td><td>

A duplicate Instance Key Encryption Key \(IKEK\) is active in the instance after a future rotation date

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1920598

</td><td>

The update set is creating a new entry upon re-loading the 'Health' page

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB2010589

</td><td>

Scheduled script \(sysauto\_script\) fails to access the Crypto Module when the default module result is track and no module access policy is present

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB2014313

</td><td>

Nodes taking long time to load CrytpoCore initialisation during startup

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB2037034

</td><td>

Instance PKI Certificate Generator fails with 'badly formatted directory string' due to non-RFC-compliant DN escaping in X500ValueEscaper

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB2039893

</td><td>

Crypto Specification record is incorrectly created in Global scope instead of the active customer-created application scope

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1844755

</td><td>

The wrong Dare key is supplied to Bagheera and it doesn't return a clear error message

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB1876955

</td><td>

The usage of glide encrypter is disallowed on the instance, and arror message is shown while decrypting the KMF data

</td></tr><tr><td>

Key Management Framework \(KMF\)

</td><td>

PRB2001586

</td><td>

Asymmetric module key generation produces a certificate in sys\_certificate, which is named either in the vault \(or self-signed\) format

</td></tr><tr><td>

Knowledge Base Self-service Portal

</td><td>

PRB2009324

</td><td>

Top category panel doesn't initially announce its state as expanded or collapsed

</td></tr><tr><td>

Knowledge Base Self-service Portal

</td><td>

PRB1992681

</td><td>

The category facet widget has nested interactive controls

</td></tr><tr><td>

Knowledge Document Management

</td><td>

PRB2008412

</td><td>

Out of memory issue occurs due to a recursive call in KnowledgeImportDocxExtractor.java

</td></tr><tr><td>

Knowledge Graph \(Family\)

</td><td>

PRB2021133

</td><td>

Knowledge Graph \(KG\) description deactivator triggers long-running queries, causing HLL spikes

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1988597

</td><td>

An article body displays an improper view when sn\_km\_center. glide.knowman .ece.enable is turned on

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2031464

</td><td>

The Knowledge Base Article \(KBA\) text is not visible in the workspace

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2009818

</td><td>

The **Recall** button isn't displayed for the author of the article in Service Operations Workspace

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2033473

</td><td>

An article title isn't displayed in the Knowledge Article print view \(sysparm\_media=print\) from Service Portal on the Australia release

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1981519

</td><td>

When opening a KB from a widget \(Knowledge Article Content\), it spins and doesn't open the article

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1980011

</td><td>

Article template creation displays an error message: 'The u\_kb\_template\_kcstemplatenew table extends the kb\_knowledge table. Please update the 'Text Index' field on kb\_knowledge to apply it to ALL tables that extend it'

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1999255

</td><td>

A Knowledge article search doesn't work correctly after a Zurich upgrade

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1982194

</td><td>

The Word add-in displays a blank white panel when an associated Knowledge Article is retired

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1982380

</td><td>

kb\_knowledge ACLs with dot walk conditions throw an exception with AI Search

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2023217

</td><td>

Error when adding the trigger table 'Knowledge Feedback Task' due to read access / invalid table error

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2000452

</td><td>

The **Edit** button isn't visible in any of the previous versions of the articles in workspaces

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1984675

</td><td>

An error is observed when accessing an AQI survey via Knowledge Center

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2031718

</td><td>

In Localization Workspace, the Translation State displays as 'Untranslated' when it's already translated

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1989283

</td><td>

m2m\_kb\_to\_ block\_history\_list displays the state of article as 'outdated' instead of 'published'

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2034553

</td><td>

When users navigate to a 'Retired' Knowledge article on Service Operations Workspace, the **Edit** button doesn't appear, meaning users can't republish the article

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2036133

</td><td>

An insert of a translated version of a KB article doesn't work even after a successful translation

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1990998

</td><td>

Selecting 'machine translate' on a source article with knowledge blocks is overriding translated block content

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1991565

</td><td>

When the 'glide.knowman. allow\_retire\_block' property is set as false, the **Retire** button in Service Operations Workspace isn't working but works in the backend

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2054635

</td><td>

Previous Knowledge Articles are transitioned from Outdated to Publish to Outdated when a new version is created with Publish Flow

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2058707

</td><td>

When a user selects 'New' from a Knowledge article list in a workspace, the article interceptor/page intermittently renders blank on the second or subsequent attempt

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2010512

</td><td>

The visible label is missing for the rich text editor of the 'Post comment' control

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2014935

</td><td>

KB Portal's image dimensions don't match with the Native UI

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2015462

</td><td>

Knowledge curation tasks don't get the frequently appearing words in this collection

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2015975

</td><td>

Service Portal KB article comments don't update in real time for non-admin users, so a manual refresh is required to see new comments

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2018387

</td><td>

For 'How To' Knowledge articles, the 'View Version' action for an older version displays the more recent version's contents

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2020599

</td><td>

The ACL m2m\_kb\_task.read contains incorrect JavaScript

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2031997

</td><td>

A knowledge article's expiring URL has to be encoded prior to setting in the email notification

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2032910

</td><td>

File Attachment field doesn't display 'Update'/'Delete' after checkout knowledge record

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2033275

</td><td>

Users with the knowledge\_manager and knowledge\_admin role cannot retire KBs if they are granted the kcs\_candidate or kcs\_contributor roles

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2034151

</td><td>

Back link on Portal \(Widget: HRM **Back** button\) doesn't work in certain situations

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2035570

</td><td>

There's a typo in the 'Knowledge Article Content' widget

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2037078

</td><td>

When try to create a translation of a KBB knowledge block in fire wind water, the system redirects to a KB article creation page

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2037824

</td><td>

The pop-up to select relevant tasks doesn't appear after selecting 'Yes, draft with Now Assist' from the knowledge base

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2041434

</td><td>

Images get misaligned when creating Knowledge Base articles from Word using the ServiceNow Knowledge plugin, resulting in formatting differences compared to the original document

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2056155

</td><td>

The template in Platform UI doesn't get a part of the string after the specific characters in the created Knowledge Article

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2056884

</td><td>

Stars aren't inline when the 'Rate this article' string is long and text spacing adjustments are applied

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2059555

</td><td>

In the kb\_2\_kb table, it's possible to link an outdated version of a Knowledge article with its published version

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2061599

</td><td>

When populating the set default 'Knowledge' field values field in Knowledge Base for the 'Article Body' field, it's reflecting raw HTML in the Knowledge records

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2061624

</td><td>

Knowledge articles are rendered with H1 and then H3 HTML tags, skipping H2 tags and breaking the conventions for semantic HTML

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1931158

</td><td>

Knowledge Management's Microsoft Word add-in date has format issues

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1932445

</td><td>

The article body is read-only when the article is in the 'Published' state for the Knowledge Management MS Word add-in

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1947403

</td><td>

The order of headings is not semantically correct in the 'Knowledge article' page

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1969189

</td><td>

In Zurich, the uploaded CSM portal logo is not being scaled proportionally

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1971125

</td><td>

The replacement article re-direction in workspace is not working when a user does not have 'Can Contribute' rights to the retired article

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1975028

</td><td>

A Knowledge article view isn't properly aligned

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1976461

</td><td>

The Knowledge Platform Analytics' dashboard \(sys\_id= b3574e38d b038740 c4f2f9151 d9619d2\) is missing

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1976775

</td><td>

A KB's article title is empty under the 'Event property values' column in the 'Article Title' report

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1982918

</td><td>

The 'Leave a comment' input is hidden off-screen on smaller screen sizes

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1985569

</td><td>

The knowledge\_admin role is required to create an article in KB Submission

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1988136

</td><td>

Users can associate the same article as a related article from kb\_knowledge

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1989983

</td><td>

There's a text alignment issue in a knowledge article's comment box on a portal

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1992747

</td><td>

Now Assist KB creation pop-up is unable to continue with the KB creation when no tasks are available for search

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1994363

</td><td>

In Service Operations Workspace, an article type 'wiki' displays blocks on a contexual panel, but in the in classic UI, if an article type is 'wiki', users don't see the 'Add block' option for knowledge articles

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1994541

</td><td>

In a KB search, the **Language Filter icon** button is unlabeled

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1995114

</td><td>

The media player doesn't have a visible keyboard focus indicator

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1996425

</td><td>

The KnowledgeUIActionSNC script include \(lines 147–149\) incorrectly references the current object instead of the articleGR GlideRecord object

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1997383

</td><td>

KFT Metrics display many records for a feedback task created from Knowledge Center

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB1999848

</td><td>

Anchor tags \('\#'\) in URLs are stripped from Word document imports in Knowledge articles

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2005385

</td><td>

Users are unable to preselect a knowledge base

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2007067

</td><td>

Knowledge articles with read access and without any user criteria configured aren't shown in the AI search results

</td></tr><tr><td>

Knowledge Management

</td><td>

PRB2008515

</td><td>

In CSM/FSM Workspace, duplicate knowledge article attachments are allowed on a case record

</td></tr><tr><td>

Knowledge Management for mobile

</td><td>

PRB1994919

</td><td>

There's duplicate tab focuse in a knowledge query facet

</td></tr><tr><td>

KPI Details

</td><td>

PRB2017652

</td><td>

Selecting KPI 'Details' records in Platform Analytics redirects to a blank page when glide.ui.polaris.experience is set to false

</td></tr><tr><td>

KPI Details

</td><td>

PRB2034337

</td><td>

Inconsistent Rounding for .5 Decimal Values Between Chart Tooltip and Score Display

</td></tr><tr><td>

KPI Details

</td><td>

PRB1997119

</td><td>

There's a discrepancy in KPI details when the time aggregation is set to 'By month AVG +' and has 'Include incomplete periods' checked

</td></tr><tr><td>

KPI Signals

</td><td>

PRB1794942

</td><td>

Excess logging is generated by pa.dc.collect. predictive.completed events

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1790665

</td><td>

Date picker variables in portal glitch when making a selection in a French language session when 'Day of week' is set to Monday

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1967655

</td><td>

The translation meaning, as seen with the Korean language, across all activity streams have become incorrect after upgrading to Yokohama

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1968320

</td><td>

Tooltips in Virtual Agent icon labels have an extra space for Simplified Chinese and Japanese languages

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1926412

</td><td>

The Japanese translation of 'not applicable' is '適用外' on scggrcplatformtest2 after upgrading to Xanadu

</td></tr><tr><td>

Language and Translations

</td><td>

PRB2038861

</td><td>

After Australia upgrade, the browser page tab doesn't translate when a user switches from English to another language

</td></tr><tr><td>

Language and Translations

</td><td>

PRB2056617

</td><td>

French translations are not working for base instance fields

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1799497

</td><td>

Incorrect translation of 'Assign to me' to French-Canada in Service Operations Workspace in Washington DC

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1883937

</td><td>

Incorrect translation TPRM for simplified Chinese

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1910363

</td><td>

Translation correction for sys\_message with the key value 'all agenda items' in the Candian French \(Français\) language

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1921541

</td><td>

The **Update Draft** button is displayed incorrectly in the French Canada language for i18N Translation

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1929651

</td><td>

Inconsistent German language translations in Service Operations Workspace \(for example, 'Checkout'\)

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1935676

</td><td>

The French Canada translation is incorrect when navigating to Portal User Preferences &gt; Accessibility Enabled Option

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1936568

</td><td>

The translation for the field opened\_by in the task table in the French Canada language shows as 'Demandé par' instead of 'Ouvert par' in Yokohoma

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1940200

</td><td>

French translations that could be reworked or that are not the right translations for i18n

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1946134

</td><td>

The Workplace Service Delivery \(WSD\) space picker widget is not translating the 'Space' field correctly in the German language, and show as 'Leertaste' instead of 'Platz'

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1950551

</td><td>

Wrong error message in French

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1950834

</td><td>

The translation is incorrect for the Norwegian langauge

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1951975

</td><td>

On the HR Agent Workspace homepage, the 'My team' tab label should be 'Mon équipe' in the French Canada language and 'Mi equipo' in the Spanish language because the translation is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1952106

</td><td>

When upgrading to Yokohama from Xanadu, the 'cat\_item' field was translated from 'élément' to 'article' in the sc\_req\_item table

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1955559

</td><td>

The translation is wrong by default

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1962583

</td><td>

Several Spanish localization issues in the platform that impact usability and clarity

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1965317

</td><td>

There's an incorrect German translation for the word 'as' in sys\_ui\_message

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1966040

</td><td>

The German translation for 'Ist leer' must be corrected

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1975283

</td><td>

The Japanese sys\_ui\_message on the UI page 'set\_initial\_selection\_criteria' unexpectedly has HTML tags

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1978205

</td><td>

After Zurich, the Portugese translation of 'all' is 'Tudo' instead of 'Todos'

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1981007

</td><td>

The German translation for 'like' with the key 'like:to\_like\_a \_comment\_on \_knowledge\_article' is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB1989996

</td><td>

There's an incorrect capitalization in the French tooltip for the 'List' view on the Employee Center 'Favorites' page

</td></tr><tr><td>

Language and Translations

</td><td>

PRB2000881

</td><td>

The Japanese translation on the 'Accept/Reject' pop-up is incorrect

</td></tr><tr><td>

Language and Translations

</td><td>

PRB2001057

</td><td>

Request for clarification on '%d' minutes translation to Português \(Brasil\)

</td></tr><tr><td>

Language and Translations

</td><td>

PRB2002782

</td><td>

In Now Assist, a chat deleted alert isn't properly localized

</td></tr><tr><td>

Language and Translations

</td><td>

PRB2004163

</td><td>

In Now Assist, the 'Delete chat' pop-up is untranslated

</td></tr><tr><td>

LDAP integration

</td><td>

PRB2033478

</td><td>

LDAP Browse displays incorrect record on first attempt due to null agent\_correlator in LDAPDetailProcessor

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB2020081

</td><td>

A workspace's sidebar preference doesn't persist

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB2041402

</td><td>

Character counter issues in Workspace

</td></tr><tr><td>

Legacy Agent Workspace

</td><td>

PRB2001487

</td><td>

The 'Mandatory timer' field has a saving error in a workspace

</td></tr><tr><td>

Legacy Workflow

</td><td>

PRB1935953

</td><td>

An inconsistent workflow status is display for KB articles between template and parent tables

</td></tr><tr><td>

Legacy Workflow

</td><td>

PRB2035969

</td><td>

An extra '?' icon is displayed in the workflow context after an Australia upgrade

</td></tr><tr><td>

License Usage \(Family Channel\)

</td><td>

PRB1671807

</td><td>

There's no **Reclaim** button in the 'Removal Candidates' list view

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB2026077

</td><td>

Dependent activity sets are not getting triggered when completing activities after upgrade to Zurich

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB2013721

</td><td>

The 'Resume Case' UI Action doesn't work as expected for certain users

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB2018859

</td><td>

Ampersand '&amp;' in Activity Field Mapping is not decoded as expected

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1966460

</td><td>

Lifecycle Events builder tab focus via arrow keys moves to all interactive elements within the 'Activities' section

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1966463

</td><td>

The keyboard focus moves outside the 'Are you sure you want to delete?' dialog when using the tab key

</td></tr><tr><td>

Lifecycle Events

</td><td>

PRB1976770

</td><td>

There's a dotwalking error: 'checkCompletionOfActivities \#\# Cannot find function isValid in object...'

</td></tr><tr><td>

List Administration

</td><td>

PRB2058580

</td><td>

Stage details pop-up does not align with workflow stage icons in workspace presentational list cell

</td></tr><tr><td>

List Administration

</td><td>

PRB1970036

</td><td>

List type data visualization doesn't show new lines \(multi-lines\)

</td></tr><tr><td>

List Administration

</td><td>

PRB2004140

</td><td>

Platform Analytics Report \(PAR\) data visualizations don't display data when grouped by tags

</td></tr><tr><td>

List Administration

</td><td>

PRB1890217

</td><td>

Selecting the dot-walked 'Document id' field from the list is emitting out the empty table in the payload

</td></tr><tr><td>

List Administration

</td><td>

PRB1582349

</td><td>

Currency values aren't displaying in the entered currency in a workspace hierarchical 'List' view

</td></tr><tr><td>

List Administration

</td><td>

PRB2007777

</td><td>

Grids contain an unnecessary tab, so when screen reader is enabled the arrow keys don't work until the user presses tab

</td></tr><tr><td>

List Administration

</td><td>

PRB1990590

</td><td>

'Table name cannot be null: java.lang.IllegalStateException' displays when opening the m2m 'Selection' page

</td></tr><tr><td>

List Administration

</td><td>

PRB2005018

</td><td>

There's a 'Show Matching' issue for date type fields on a workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB1814129

</td><td>

Column filtering for tags should be supported

</td></tr><tr><td>

List Administration

</td><td>

PRB1991605

</td><td>

Date and time selection issues during inline edits

</td></tr><tr><td>

List Administration

</td><td>

PRB1999160

</td><td>

In Customer Service Management/Field Service Management workspace, a saved copy of an existing list does reflect the personalized columns without a refresh

</td></tr><tr><td>

List Administration

</td><td>

PRB2032077

</td><td>

Live Update doesn't work for workspace record list component with a dynamic filter on Assignment group

</td></tr><tr><td>

List Administration

</td><td>

PRB2011679

</td><td>

List data broker transform throws an error when attempting to destructure a null object

</td></tr><tr><td>

List Administration

</td><td>

PRB2019532

</td><td>

The left side list menu doesn't load if a user doesn't have access to the first list in Customer Service Management workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB2054698

</td><td>

A timer-type field isn't editable on the list visualization, even when it's allowed to be edited on native list view and native reporting

</td></tr><tr><td>

List Administration

</td><td>

PRB2019383

</td><td>

Tags are blank/empty after a list report is migrated to Platform Analytics when the tags are dot-walked

</td></tr><tr><td>

List Administration

</td><td>

PRB1977296

</td><td>

When a user sets the system time to 'hh:mm:ss:a' and the date/time user preference to 'YYYY-MM-DD 09:00', the date fields aren't displayed correctly on the 'List' view

</td></tr><tr><td>

List Administration

</td><td>

PRB2017389

</td><td>

In HR Agent Workspace, the pagination buttons have redundant page numbers in accessible labels

</td></tr><tr><td>

List Administration

</td><td>

PRB1998281

</td><td>

The datepicker's first day of the week isn't applied consistently for the non-English languages

</td></tr><tr><td>

List Administration

</td><td>

PRB1940372

</td><td>

A cache issue where the influx of hash = -1962423347 SELECT sys\_ui\_list0.\`sys\_id\` FROM \(\(sys\_ui\_list sys\_ui\_list0 query when incident\_list.do transactions are active

</td></tr><tr><td>

List Administration

</td><td>

PRB1984847

</td><td>

The group divider 'Show all' text overlaps the group label in narrow lists, including in mobile

</td></tr><tr><td>

List Administration

</td><td>

PRB2002279

</td><td>

A cell edit on any URL field type asks for 'Enter Label' and 'URL', but the 'Enter Label' field isn't functional

</td></tr><tr><td>

List Administration

</td><td>

PRB1986209

</td><td>

When a list is grouped, users are unable to remove tags via cell edit

</td></tr><tr><td>

List Administration

</td><td>

PRB2036189

</td><td>

Live list not auto-refreshing as expected

</td></tr><tr><td>

List Administration

</td><td>

PRB2007422

</td><td>

ListLayout.getGroupedRowLayoutQuery\(\) and SecurityAttribute.loadFromDB\(\) lead to node restarts due to out of memory issues

</td></tr><tr><td>

List Administration

</td><td>

PRB1995275

</td><td>

There's duplicate 'You've reached the end of the list' messages displayed when 'Live Updates' is turned on in Service Operations Workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB2060084

</td><td>

The 'User Preference' workspace.list.columnOrder.&lt;table&gt;.&lt;sys\_id&gt; fails to save if the table name is too long

</td></tr><tr><td>

List Administration

</td><td>

PRB1978441

</td><td>

Workspace-based reference fields aren't working correctly when the sys\_user table has multiple reference fields pointing to sys\_user\_group

</td></tr><tr><td>

List Administration

</td><td>

PRB1995997

</td><td>

List cell editing isn't working for reference fields in list visualizations

</td></tr><tr><td>

List Administration

</td><td>

PRB2014997

</td><td>

In Service Operations Workspace, live updates of Alert Express List displays en 'Invalid Row Data, Duplicate Row Keys' error on auto-refresh

</td></tr><tr><td>

List Administration

</td><td>

PRB1996999

</td><td>

In List Collector, '-- none --' doesn't disappear when in the non-English UI

</td></tr><tr><td>

List Administration

</td><td>

PRB2009056

</td><td>

The **Back** button after grouping isn't working

</td></tr><tr><td>

List Administration

</td><td>

PRB2013968

</td><td>

Changing the column layout in one table affects other tables

</td></tr><tr><td>

List Administration

</td><td>

PRB2015114

</td><td>

The user is unable to load the results table frame on the same page

</td></tr><tr><td>

List Administration

</td><td>

PRB2017610

</td><td>

The filter on all lists isn't available when a user is provided with the roles 'admin' and 'snc\_read\_only' via Time-Limited User Roles

</td></tr><tr><td>

List Administration

</td><td>

PRB2020786

</td><td>

Dynamic Filter does not work when loaded through Module instead of manually building the filter

</td></tr><tr><td>

List Administration

</td><td>

PRB2024204

</td><td>

Screen readers announce Shift+Enter instructions on non-editable cells in Row Actions column

</td></tr><tr><td>

List Administration

</td><td>

PRB2024845

</td><td>

The ListHighlighted ValueService cache key is missing highlightedValueConfigId, and causes cache collisions between requests with different configuration IDs

</td></tr><tr><td>

List Administration

</td><td>

PRB2031517

</td><td>

In some workspaces, when a user views a list of requests that spans multiple pages, the scroll bar position from page 1 carries over to page 2 and does not reset to the top

</td></tr><tr><td>

List Administration

</td><td>

PRB2031676

</td><td>

After the drop down is loaded, previously input values in Time and Option fields are removed

</td></tr><tr><td>

List Administration

</td><td>

PRB2034118

</td><td>

In lists, there's an incorrect plural form for 'values'

</td></tr><tr><td>

List Administration

</td><td>

PRB2035585

</td><td>

There's a 'The page you are looking for could not be found' error when opening a sub page collection from the view port

</td></tr><tr><td>

List Administration

</td><td>

PRB2040663

</td><td>

'Turn on live updates' is hardcoded

</td></tr><tr><td>

List Administration

</td><td>

PRB2040925

</td><td>

In list view, when the export process starts, keyboard focus is automatically set to the **Close** button in the loading dialog, while the ongoing export status is not announced to screen reader users

</td></tr><tr><td>

List Administration

</td><td>

PRB2051103

</td><td>

The **Add Filter** and **Run Filter** button aria-labels are hardcoded

</td></tr><tr><td>

List Administration

</td><td>

PRB2052742

</td><td>

Screen readers announce Shift + Enter edit instructions on all cells in lists

</td></tr><tr><td>

List Administration

</td><td>

PRB2055207

</td><td>

The 'Checkbox' field always displays 'true' in the dashboard view when switching to a non-English language

</td></tr><tr><td>

List Administration

</td><td>

PRB2055447

</td><td>

Now-grid record preview buttons trigger dialogs to open, but they're missing aria-haspopup='dialog'

</td></tr><tr><td>

List Administration

</td><td>

PRB2055606

</td><td>

The 'Apply' translation is missing when creating a list copy in the agent workspace based on a shared link

</td></tr><tr><td>

List Administration

</td><td>

PRB2056865

</td><td>

In the 'Tag Details' modal, the read-only tag name has insufficient contrast

</td></tr><tr><td>

List Administration

</td><td>

PRB2058445

</td><td>

A 'Date' field displays the previous day in a pop-over when inline editing

</td></tr><tr><td>

List Administration

</td><td>

PRB2060016

</td><td>

The focus indicator on tag controls has insufficient color contrast

</td></tr><tr><td>

List Administration

</td><td>

PRB2062127

</td><td>

For a catalog item flow with no stages defined, the 'Stage' in Service Operation Workspace displays 'No workflow stages available'. Used to be 'Request Approved'

</td></tr><tr><td>

List Administration

</td><td>

PRB1968312

</td><td>

For all the controls such as 'All applications', 'Favorites', 'Show/ hide filter', 'Next page', 'Table headers' for the landing page, an additional text is provided in tooltip, but when user hover on the tooltip, the tooltip disappears immediately

</td></tr><tr><td>

List Administration

</td><td>

PRB1976358

</td><td>

There's a large empty space in list visualization when there are less rows of a record in a Zurich version

</td></tr><tr><td>

List Administration

</td><td>

PRB1978363

</td><td>

There's an issue with expanding items when there's a global 'OR' query with nestBy

</td></tr><tr><td>

List Administration

</td><td>

PRB1980675

</td><td>

List links have an incorrect primary color variable

</td></tr><tr><td>

List Administration

</td><td>

PRB1987163

</td><td>

Filters are accumulating instead of replacing when on the same field

</td></tr><tr><td>

List Administration

</td><td>

PRB1989782

</td><td>

Inconsistent naming of the three-dot menu on 'My Lists' \(Show Options vs. Menu Item Actions\)

</td></tr><tr><td>

List Administration

</td><td>

PRB1989840

</td><td>

There's unintended creation of temporary list copies when refreshing a default list via address bar

</td></tr><tr><td>

List Administration

</td><td>

PRB1991100

</td><td>

Attempting to remove tags from rm\_story dependent stories isn't persisting

</td></tr><tr><td>

List Administration

</td><td>

PRB1991370

</td><td>

Presentational list should allow for suppressing Rows Hidden alerts via system property

</td></tr><tr><td>

List Administration

</td><td>

PRB1992695

</td><td>

When a calendar\_date\_time type field is double-clicked to edit it in a list, it's displayed in UTC time

</td></tr><tr><td>

List Administration

</td><td>

PRB1995408

</td><td>

The inline editing pop-over lacks proper accessibility when a field can't be edited

</td></tr><tr><td>

List Administration

</td><td>

PRB1995575

</td><td>

The 'Select All Rows' checkbox isn't hidde on the pop-up after an upgrade to Zurich in a workspace

</td></tr><tr><td>

List Administration

</td><td>

PRB1997156

</td><td>

List sections under My Lists tab of Workspace do not keep their expand / collapse state

</td></tr><tr><td>

List Administration

</td><td>

PRB1997159

</td><td>

Lists created under 'My Lists' of Workspace requires explicitly provide the permission

</td></tr><tr><td>

List Administration

</td><td>

PRB1998065

</td><td>

The 'Share' icon isn't visible after copying a list and sharing it

</td></tr><tr><td>

List Administration

</td><td>

PRB1998370

</td><td>

Cursor navigation in an Arabic interface is inverted for table cell navigation

</td></tr><tr><td>

List Administration

</td><td>

PRB1999574

</td><td>

The user has no information about who shared a list with them

</td></tr><tr><td>

List Administration

</td><td>

PRB2001027

</td><td>

A screen reader doesn't announce a role in focus mode

</td></tr><tr><td>

List Administration

</td><td>

PRB2002126

</td><td>

There's incorrect bar sizing for 'Business Elapsed Percentage'

</td></tr><tr><td>

List Administration

</td><td>

PRB2002352

</td><td>

There's a mismatch between the number of records being listed when expanding a grouped list

</td></tr><tr><td>

List Administration

</td><td>

PRB2003558

</td><td>

Users are unable to select 'presentational' variables when using the list selector to build out list configurations

</td></tr><tr><td>

List Administration

</td><td>

PRB2004824

</td><td>

The 'Save a copy' dialog doesn't have a title

</td></tr><tr><td>

List Administration

</td><td>

PRB2005435

</td><td>

Focus doesn't move to the 'Edit item' form panel after activating the **Edit** UI action button

</td></tr><tr><td>

List Administration

</td><td>

PRB2008294

</td><td>

When using the filter search with wildcard \(\*\) for contains it instead filters it with 'is one of' rule.

</td></tr><tr><td>

List Administration

</td><td>

PRB2008389

</td><td>

Random offset is added in the filter condition when the property 'glide.sys.time\_format' is set to HH:mm

</td></tr><tr><td>

List Column Menu

</td><td>

PRB2038623

</td><td>

Selecting the three dots beside State doesn't work on Risk Workspace

</td></tr><tr><td>

List Configuration

</td><td>

PRB1984207

</td><td>

On a Portal experience, the middle click opens the record in a new tab with the Platform UI

</td></tr><tr><td>

List Configuration

</td><td>

PRB1982419

</td><td>

An approval record for a service request doesn't display all the details under the 'Request' tab

</td></tr><tr><td>

List Configuration

</td><td>

PRB1990298

</td><td>

Links aren't displaying when a user selects 'Save' on a list visualization

</td></tr><tr><td>

List Configuration

</td><td>

PRB2015609

</td><td>

'Yes/No' variable isn't translated into Spanish in the results of a data visualization

</td></tr><tr><td>

List Configuration

</td><td>

PRB1854942

</td><td>

A user with the correct roles is unable to create a new personal list on the workspace

</td></tr><tr><td>

List Controller

</td><td>

PRB2061282

</td><td>

Articles' 'List' view isn't loading in Knowledge Center and workspaces

</td></tr><tr><td>

List Controller

</td><td>

PRB1975958

</td><td>

Non-admins are unable to access the 'LIST' page in the CSM/ FSM workspace when the user does not have access to the first category displayed on the list

</td></tr><tr><td>

List Controller

</td><td>

PRB1990422

</td><td>

A relative timestamp \(time ago\) in a workspace's 'List' view doesn't refresh unless the record itself is updated

</td></tr><tr><td>

List Controller

</td><td>

PRB2020825

</td><td>

When declarative actions are allowed, value binding doesn't work

</td></tr><tr><td>

List Controller

</td><td>

PRB2056620

</td><td>

Selecting records and using the bulk options from the action group is not updating all the records

</td></tr><tr><td>

List Controller

</td><td>

PRB1989084

</td><td>

In Platform Analytics, a loading indicator appears in the mid-page of the scheduled export list after applying filters

</td></tr><tr><td>

List Editor

</td><td>

PRB2034715

</td><td>

Enable default row actions only for Service Operations Workspace

</td></tr><tr><td>

List Filters

</td><td>

PRB1886434

</td><td>

Duplicate filters are added in the Seismic filters on the group rows after using 'Group by'

</td></tr><tr><td>

List Filters

</td><td>

PRB2035499

</td><td>

There's an error when updating/filtering data from a list in Service Operations Workspace

</td></tr><tr><td>

List Filters

</td><td>

PRB1952724

</td><td>

When searching for text on a list that contains diacritics \(such as accents, umlauts, etc.\), it will return records that match the text without the diacritics

</td></tr><tr><td>

List Filters

</td><td>

PRB1974240

</td><td>

Users are able to share a workspace list with inactive users and groups, and the 'before query' business rules aren't run for those two queries

</td></tr><tr><td>

List Filters

</td><td>

PRB2031646

</td><td>

Mixed Language displays in filter

</td></tr><tr><td>

List Filters

</td><td>

PRB2052593

</td><td>

On a 'Choice' column, a column filter appears to be applied on the list load although the user didn't add any filter

</td></tr><tr><td>

List Multi-Field Edit

</td><td>

PRB2023568

</td><td>

The 'Detail' row won't allow a bulk list edit

</td></tr><tr><td>

List Views

</td><td>

PRB1979390

</td><td>

'Edit columns' is not working, and no illustration appears when selecting 'Backlog personalize panel'

</td></tr><tr><td>

List Views

</td><td>

PRB2031162

</td><td>

Wrap text functionality doesn't work when the property 'glide.lists.preserve\_whitespace'=true'

</td></tr><tr><td>

List Views

</td><td>

PRB1923875

</td><td>

The translation not being honored for calculated values in the List view

</td></tr><tr><td>

List Views

</td><td>

PRB2032604

</td><td>

Accessibility issue with the analytics platform when navigating using the JAWS screen reader software

</td></tr><tr><td>

List Views

</td><td>

PRB2054376

</td><td>

sys\_ui\_view isn't captured for report views in an update set

</td></tr><tr><td>

Live Archive

</td><td>

PRB1999471

</td><td>

otherBlobsInChunkExist includes non-storage fields in coordinate comparison, causing premature S3 object deletion

</td></tr><tr><td>

Live Archive

</td><td>

PRB1983498

</td><td>

Migration fails with ava.util.ArrayList.iterator\(\)

</td></tr><tr><td>

Live Archive

</td><td>

PRB1976776

</td><td>

There's an error when restoring to long table name aliased tables

</td></tr><tr><td>

Machine Identity Access Control

</td><td>

PRB1991942

</td><td>

When trying to set up Machine Identity Access control for write access on Table API to the 'Incident' table, the API account can create incidents, but if it tries to write to the 'comments' or 'work\_notes' fields, an error is seen

</td></tr><tr><td>

Machine Identity Access Control

</td><td>

PRB1991426

</td><td>

The 'Machine Identity Access Control' table list loads slowly and is missing certain system tables

</td></tr><tr><td>

Machine Identity Management

</td><td>

PRB2035817

</td><td>

The com.snc.sa.metric package contains script includes that have duplicated names

</td></tr><tr><td>

Machine Identity Management

</td><td>

PRB2022181

</td><td>

Users with internal\_integration\_user=true are displayed in the 'No login for 100 days' metric

</td></tr><tr><td>

Machine Learning APIs

</td><td>

PRB2027231

</td><td>

Excessive syslog volume and near-indefinite runtime due to missing early-exit condition and unconditional gs.sleep\(1000\)

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB2030990

</td><td>

The Major Incident Management \(MIM\) plugin is installed automatically after upgrading in Australia

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB2019347

</td><td>

In a Major Incident, the name is of the type 'String'

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB2028440

</td><td>

'Reject Major Incident Candidate' UI Action fails and incorrectly logs rejection on Save

</td></tr><tr><td>

Major Incident Management

</td><td>

PRB2061521

</td><td>

In Major Incident outage creation, a task number is populated in workbench but not from a related list

</td></tr><tr><td>

MetricBase

</td><td>

PRB2008126

</td><td>

The rollup scheduling script has a race condition that allows duplicate event queuing in MetricRaptor

</td></tr><tr><td>

MetricBase

</td><td>

PRB1584883

</td><td>

GlideRecord can pull excessive volumes of Clotho data into the application node heap, causing memory contention and performance issues

</td></tr><tr><td>

MetricBase

</td><td>

PRB2032195

</td><td>

Thread pile-up on JVM locks in the metric dictionary system \(in GlideRecord.addMetricFields\(\) call stack\)

</td></tr><tr><td>

MetricBase

</td><td>

PRB1989962

</td><td>

Metricbase load spikes can cause bursts of server connection errors: 'No threads are available'

</td></tr><tr><td>

Metric Intelligence \(Family\)

</td><td>

PRB1998729

</td><td>

A REST API script that retrieves models sometimes causes an out of memory error

</td></tr><tr><td>

Metric Intelligence \(Family\)

</td><td>

PRB1998731

</td><td>

A REST API script to fetch models performs an inefficient query on sa\_metric\_map, which sometimes causes an out of memory error

</td></tr><tr><td>

Metric Intelligence \(Family\)

</td><td>

PRB1976891

</td><td>

Updates to 'Operational Intelligence - Combined Model Learner' job in the apply\_once folder

</td></tr><tr><td>

Metric Intelligence \(Family\)

</td><td>

PRB1998271

</td><td>

Remove 'View Metrics' from the CI menu in the 'Dependency' view

</td></tr><tr><td>

MID Server

</td><td>

PRB1973287

</td><td>

The CyberArk Credential resolution fails if the credential ID is empty, when it should allow 'null' to enable the IP-based lookup

</td></tr><tr><td>

MID Server

</td><td>

PRB1979997

</td><td>

Windows MID Server fails to upgrade because it's not installed in English

</td></tr><tr><td>

MID Server

</td><td>

PRB1974583

</td><td>

There's a potentially misleading MID Server error: 'User XXX associated with down MID Server: sysID. No login attempts within reporting period'

</td></tr><tr><td>

MID Server

</td><td>

PRB2063491

</td><td>

'LinkedHashMap$Entry' objects connected to the LRU take a couple MB

</td></tr><tr><td>

MID Server

</td><td>

PRB2024847

</td><td>

ACC agent WSS upgrade returns HTTP 500 \(URISyntaxException\) when MID is fronted by LB with underscore in hostname

</td></tr><tr><td>

MID Server

</td><td>

PRB1972027

</td><td>

The silentinstall.ps1 script currently doesn't support group managed service accounts \(gMSA\)

</td></tr><tr><td>

MID Server

</td><td>

PRB2011363

</td><td>

MID Server runs the same probe twice if it completes during a MID Server shutdown and the result is prevented from being written to the ECCSender folder

</td></tr><tr><td>

MID Server

</td><td>

PRB2011987

</td><td>

A typo in wrapper.conf means the capability to load unnamed modules doesn't work

</td></tr><tr><td>

MID Server

</td><td>

PRB2011944

</td><td>

A MID Server with an ampersand character '&amp;' in the name goes down after failing the GetMIDInfo.do requests for ECCSenderCache

</td></tr><tr><td>

MID Server

</td><td>

PRB2022588

</td><td>

Windows Discovery takes ~3 minutes due to inefficient PowerShell module existence check using Get-Module -List when setting mid.windows.management\_protocol=WinRM

</td></tr><tr><td>

MID Server

</td><td>

PRB2061457

</td><td>

App node reporting older build version causes the 'MID Server Version' job to assign incorrect Zurich packages, causing all MIDs to downgrade

</td></tr><tr><td>

MID Server

</td><td>

PRB1783689

</td><td>

The 'SWITCH' command on Citrix-NetScalar is not working from the pattern

</td></tr><tr><td>

MID Server

</td><td>

PRB1893758

</td><td>

SSHSharedSessionCache can sometimes fail to return a borrowed connection to the pool

</td></tr><tr><td>

MID Server

</td><td>

PRB1895102

</td><td>

The JDBC probe retries fail because a single quote is missing around fLastRunDateTime in SQL statements

</td></tr><tr><td>

MID Server

</td><td>

PRB1968376

</td><td>

The Install Directory being passed with invalid characters during the Windows MID server silent installation leads to an autoupgrade failure

</td></tr><tr><td>

MID Server

</td><td>

PRB1968743

</td><td>

The basic authentication credential does not contain the MID Servers field selection

</td></tr><tr><td>

MID Server

</td><td>

PRB2007733

</td><td>

The /xmlstats.do?include=ecc\_queue sometimes reports an agent with no name

</td></tr><tr><td>

MID Server

</td><td>

PRB1982535

</td><td>

An agent isn't going down when invalid characters are appended with the API key in the acc.yml file

</td></tr><tr><td>

MID Server

</td><td>

PRB2032808

</td><td>

PowerShell processes launched by MID Server Discovery via the WMI protocol are missing the -NoProfile flag

</td></tr><tr><td>

ML Normalization for SAM

</td><td>

PRB1815525

</td><td>

ML Normalization doesn't try to normalize the Discovery models that were missed by an older ML model version

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB2033117

</td><td>

In Now Agent, the work order task questionnaire is truncated if the questionnaire is more than 100 characters

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1895679

</td><td>

The arrow navigation for Genius Results is not working as expected in the Mobile responsive mode

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1987587

</td><td>

Check for the Mobile language plugin before getting the language bundle in LanguageProvider.java

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB2021795

</td><td>

The checklist string value ampersand is saved as '&amp;amp;'

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB2024364

</td><td>

The list screen returns empty in Now Mobile / Mobile Agent when the sys\_sg\_item\_parameter.name is set to a Japanese value

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB2033722

</td><td>

'Parts to Drop off' is zero even though there are defective items for drop off

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB2033906

</td><td>

Setting sp\_theme.navbar\_fixed to true doen't fix the header menu to the top in a mobile browser after upgrading to Australia

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB2035860

</td><td>

A mobile writeback button on a reference-field cell on a details screen fails with 'Invalid update' because the server sends the referenced record as the action context instead of the host record

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB2050960

</td><td>

Dependent reference list in IFS returns empty

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1973106

</td><td>

Search results do not get filtered by selected facet options

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1984781

</td><td>

Incremental offline caching does not sync related records for newly created Work Order Tasks \(WOT\) after the initial offline payload is downloaded

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1989348

</td><td>

Filtering with a date range doesn't work in offline

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1995291

</td><td>

Now Mobile reports an incorrect date for the 'Opened' attribute of a request, ignoring the user's timezone preference

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB1995836

</td><td>

Hide functions aren't working in offline mode

</td></tr><tr><td>

Mobile Platform

</td><td>

PRB2000325

</td><td>

Cell redirection action fails in Offline Mode after completing a task when multiple conditional buttons share the same cell location

</td></tr><tr><td>

Model Management

</td><td>

PRB2010766

</td><td>

Enhance checks for hiding the 'Software model' tab and removing the **Software** radio button under Model Management

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB2021496

</td><td>

A new user with the snc\_read\_only role couldn't use email one-time passcode \(OTP\) at first login

</td></tr><tr><td>

Multi-factor Authentication \(MFA\)

</td><td>

PRB2037125

</td><td>

In non-Polaris UI, the step 1 in the multi\_factor\_auth\_setup\_page.do page lacks URL from Australia

</td></tr><tr><td>

Multi-Instance Framework

</td><td>

PRB2066107

</td><td>

DB listener MIFVTableListener fails with IAE before/after DB actions and breaks the normal upgrade flow

</td></tr><tr><td>

Multi-Instance Framework

</td><td>

PRB2019094

</td><td>

Async messages from a JavaScript layer aren't signed so they aren't validated on a receipt

</td></tr><tr><td>

Next Experience All Menu

</td><td>

PRB2017623

</td><td>

The 'Reduce Motion' function feature doesn't work after reloading the page for the first few times

</td></tr><tr><td>

Next Experience All Menu

</td><td>

PRB2035354

</td><td>

A 'Now Assist Launch Mode' drop-down list appears in Display Preferences even when Now Assist is not in use

</td></tr><tr><td>

Next Experience All Menu

</td><td>

PRB1957877

</td><td>

Unnecessary navigation landmark is defined inside the 'All' menu

</td></tr><tr><td>

Next Experience All Menu

</td><td>

PRB2003312

</td><td>

The **Pin** button in the chat panel header isn't taking styling values from Theme Builder

</td></tr><tr><td>

Next Experience Favorites Menu

</td><td>

PRB2006292

</td><td>

Keyboard-only users aren't provided instructions on how to reorder their favorites using just a keyboard

</td></tr><tr><td>

Next Experience Landing Page

</td><td>

PRB2005972

</td><td>

The Next Experience homepage has multiple H1 headings

</td></tr><tr><td>

Next Experience Notifications Menu

</td><td>

PRB1951100

</td><td>

Multiple notifications toasts do not properly disappear

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1997428

</td><td>

There's an incorrect CSS variable in .menu-item-header:hover .label

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2013936

</td><td>

In UI16 experience Australia, the **Close Message** button for any info message renders below the message box

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1976505

</td><td>

When users open SCTASKs or incidents in new tabs, the ServiceNow tab header title displays 'Classic \| Unified Navigation App \| ServiceNow' instead of the number of the SCTASK/incident record

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1971847

</td><td>

The default ServiceNow logo appears briefly in Next Experience before switching to the user's logo

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2027423

</td><td>

When Next Experience is disabled, navigation from a UXF page fails and opens a new tab instead of the expected form due to missing route configuration in the experience context

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2026091

</td><td>

The **Back** button does not take users to global search page, and instead takes users to dashboard page intermittently

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1769375

</td><td>

The highlighted values do not work for the child tables when configured for the parent/base tables

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2034126

</td><td>

A collapsible menu \(for example, 'Self Service' or similar\) text color does not change when the user hovers over it in the navigation filter menu

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1994000

</td><td>

State Persistence not working in Zurich

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2013383

</td><td>

The form / list border styling changed after upgrading to Zurich

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2010012

</td><td>

Form Field Hover background fill doesn't come into effect after saving the form

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2015882

</td><td>

Notification tooltip doesn't appear on hover in configurable workspace

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2018850

</td><td>

The **Form Back** and **Save/Update** buttons redirect to the wrong page when multiple browser tabs are open

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2018942

</td><td>

The 'Time Worked' field is not displayed properly in the dark theme

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2019648

</td><td>

The notification 'Toast' subtext has insufficient contrast in dark mode

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2023414

</td><td>

There's a duplicate dashboard header on back navigation

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2025301

</td><td>

The 'History' tab doesn't always work

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2033901

</td><td>

.jpg favicon isn't displayed on mobile Chrome/Edge

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2033990

</td><td>

Desktop navigation selection redirects to the wrong window instead of SOW workspace

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2039347

</td><td>

Pop-up modals for elements in the Next Experience banner are misaligned to the icons

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1720952

</td><td>

The 'Not Found' tab on workspace

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1887581

</td><td>

Selecting a new chat desktop notification doesn't bring focus to the tab that changed

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1931226

</td><td>

Unnecessary navigation landmarks are defined for the **All**, **Favorites**, **History**, **Workspaces**, and **Admin menu** buttons for Unified Navigation

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1942696

</td><td>

The update set name shows '\\' in the 'History' tab

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1947312

</td><td>

After upgrading to Zurich, issues with using the Dragon software have been identified

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1974955

</td><td>

Changing the user language doesn't update the header and navigation menus after changing the language from the user's preference

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1978700

</td><td>

Read-only fields doesn't have the defined theme color standards are inconsistent across the UI

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1979645

</td><td>

Global search in native view is not minimizing once exact match is selected

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1986111

</td><td>

Clicking a profile link doesn't lead to the 'sys\_user' page

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1987000

</td><td>

The Computer Telephony Integration \(CTI\) window stops dragging when the cursor leaves the CTI header and only resumes after a re-hover

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1996956

</td><td>

When a user updates glide.product.image and glide.product.image.light with the name of an image in the db\_image table, it clears the 'My Company' image

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1997600

</td><td>

Now Assist Panel Performance Issue

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1999017

</td><td>

On Platform Analytics, the **Back** button redirects to a different dashboard

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2052408

</td><td>

A pinned navigation menu takes more time to load than an unpinned one

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB1999717

</td><td>

In Theme Builder, button tertiary styling isn't applied correctly on the Help Center

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2001127

</td><td>

LargeContentDiskCache is used for maintaining the server cache and to avoid caching the null value, it should be explicitly initialized with storeNoContent as false

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2005364

</td><td>

There are many unnecessary logs in console when the 'glide.ui.keyboard.shortcuts.enabled' user preference is set to false

</td></tr><tr><td>

Next Experience Unified Navigation

</td><td>

PRB2087666

</td><td>

The 'AI Workflow' button opens a blanket panel on the core-U form

</td></tr><tr><td>

Normalization Data Services

</td><td>

PRB1969406

</td><td>

Prevent the creation of cds\_client\_mapping records where the discovered name and normalized name are identical

</td></tr><tr><td>

Normalization Data Services

</td><td>

PRB1975351

</td><td>

Duplicate records exists in the cds\_client\_mapping table

</td></tr><tr><td>

Normalization Data Services

</td><td>

PRB1984858

</td><td>

If Normalization Data Services guided setup isn't run, existing core\_company records aren't normalized/canonical, which leads to duplicate records and a potentially out-of-memory issue

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1978423

</td><td>

There's a notification from a changing scope that's not part of an accessibility feature: 'Do not auto-dismiss page alerts preference'

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB1894224

</td><td>

The 'Notification Preferences' \(sys\_platform\_notification\_preferences\) widget's usual length is maintained when selecting the notification preferences

</td></tr><tr><td>

Notification Preferences

</td><td>

PRB2028817

</td><td>

Delivery channels should expose translations

</td></tr><tr><td>

Notify integration with Twilio Direct

</td><td>

PRB2029210

</td><td>

On-call voice intermittently skips an incident description when the description length is ~100 characters or more

</td></tr><tr><td>

Now Assist Panel

</td><td>

PRB2000118

</td><td>

Headings present in the 'Chats' panel aren't defined as headings in the code

</td></tr><tr><td>

Now Assist Panel

</td><td>

PRB1946969

</td><td>

Ensure that lists are structured properly for the 'Resolve non-critical HR cases' flow

</td></tr><tr><td>

Now Assist Panel

</td><td>

PRB1972875

</td><td>

The Knowledge Graph skill \(T2R\) is not passed in the prompt

</td></tr><tr><td>

Now Assist Panel

</td><td>

PRB2012699

</td><td>

Now Assist Panel conversation timeout doesn't honor the configured value

</td></tr><tr><td>

Now Assist Panel

</td><td>

PRB2029323

</td><td>

Vertical and horizontal scroll on the Now Assist Panel

</td></tr><tr><td>

Now Assist Panel

</td><td>

PRB1946939

</td><td>

The keyboard focus is moving away after expanding 'Chats'

</td></tr><tr><td>

Now Assist Panel

</td><td>

PRB1964280

</td><td>

Now Assist Portal fails to open external source links

</td></tr><tr><td>

Now Assist Panel

</td><td>

PRB2003390

</td><td>

The **New Chat** button is disabled on Now Assist panel \(NAP\) when launched through AI Engagement Experience Layer \(AIEL\)

</td></tr><tr><td>

Now Assist Platform

</td><td>

PRB2017379

</td><td>

Role masking on Agent Access Role Configuration doesn't expand the inherited/contained roles into the narrowed session

</td></tr><tr><td>

Now User Experience

</td><td>

PRB2037238

</td><td>

i18n attachment hardcoded string

</td></tr><tr><td>

Now User Experience

</td><td>

PRB1993765

</td><td>

There's a behavioral difference in the module visibility under 'System Web Services' between Zurich and Yokohama

</td></tr><tr><td>

OAuth

</td><td>

PRB1996064

</td><td>

In Client Credentials, there's a 'No results found' message for an OAuth application user

</td></tr><tr><td>

OAuth

</td><td>

PRB2038592

</td><td>

java.lang.NullPointerException reading 'Cannot read the array length because '' is null'

</td></tr><tr><td>

OAuth

</td><td>

PRB2040136

</td><td>

Null age in sys\_auto\_flush rule for oauth\_external\_token causes DMTableCleaner to skip cleanup

</td></tr><tr><td>

OAuth

</td><td>

PRB1984077

</td><td>

The 'Copy Client Secret UI' macro doesn't work on Safari, but works in Chrome

</td></tr><tr><td>

OAuth

</td><td>

PRB1995025

</td><td>

An access policy isn't applied to the Rest API call if 'Apply to all resource' is set to true

</td></tr><tr><td>

OAuth 2.0 integration

</td><td>

PRB2032073

</td><td>

Chat-Input is available to requester when conversation ends

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2001156

</td><td>

If domain separation is turned on, with the new trigger engine set to true, escalations don't happen when the assignment group changes

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1975559

</td><td>

On-call contact information isn't visible for some users for some attempts

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2013156

</td><td>

Garbled characters are displayed when placing the cursor over a shift name that contains multi-byte characters

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2020269

</td><td>

There's an on-call schedule abnormality when adding a coverage

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2023419

</td><td>

There are different 'accessible from' settings for individual on-call actions

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2024542

</td><td>

New Trigger Engine Handler subflow can execute before triggering record is committed - silent trigger rule processing failure

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2030962

</td><td>

The On-Call Scheduling family plugin is installed on upgrading to Australia.

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2034496

</td><td>

In a SMS action in the subflow 'On-Call', the 'Check Assignment Response' doesn't use Notify

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2055640

</td><td>

'On-Call: Send Notification - Email' fails when a user without the itil role tries to run the subflow

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1986992

</td><td>

After a Zurich upgrade, the 'Trigger fields' field in the trigger rules is a list reference field, but only allows one field at a time

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1988467

</td><td>

After a Zurich upgrade, schedule\_formatted\_report for 'On call Rota' isn't working when using the date format 'dd-MM-yyyy'

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB1989775

</td><td>

There's a performance Issue when rejecting an on-call acknowledgement in a Zurich upgrade

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2002610

</td><td>

On-Call scheduling Twilio integration has silent calls and endpoint errors

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2004625

</td><td>

On‑call escalation isn't triggered on a P1 priority update

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2005795

</td><td>

On-call communication workflow returns the internal table name \(sys\_class\_name\) instead of the label

</td></tr><tr><td>

On-Call Scheduling

</td><td>

PRB2008505

</td><td>

When the subflow 'On-Call: Send Notification - SMS' is triggered, the 'Source' field isn't set in the notify\_message table

</td></tr><tr><td>

OneExtend

</td><td>

PRB2059503

</td><td>

Summarization records aren't displaying a proper response

</td></tr><tr><td>

OneExtend

</td><td>

PRB1845600

</td><td>

The sys\_gen\_ai\_usage\_log table should not have 'user=system' for asynchronous quick mode executions, even for callbacks

</td></tr><tr><td>

OneExtend

</td><td>

PRB2014491

</td><td>

Predictive Intelligence \(PI\) fails due to an API restriction by the PI team

</td></tr><tr><td>

OneExtend

</td><td>

PRB2067309

</td><td>

Callback handler error is logged for sync mode capabilities when no callback is configured

</td></tr><tr><td>

OneExtend

</td><td>

PRB2016612

</td><td>

Com.glide.oneextend.dao.optimized\_default\_builder\_capability\_load should be set to false if glide.db.max\_view\_records is &lt;= 2000

</td></tr><tr><td>

OneExtend

</td><td>

PRB2037039

</td><td>

Tool/feature placeholders resolve to empty in grounded GenAI prompts during async capability execution

</td></tr><tr><td>

OneExtend

</td><td>

PRB2056165

</td><td>

The guardian exclusion list for 3P excludes the attribute from the main capability request

</td></tr><tr><td>

OneExtend

</td><td>

PRB2014261

</td><td>

ACL rules from the Glide OneExtend \(com.glide.one\_extend\) plugin incorrectly set replace\_on\_upgrade = false, causing skipped records in subsequent upgrades

</td></tr><tr><td>

OneExtend

</td><td>

PRB2025209

</td><td>

The 'thanks for chatting...' message appears in level-2 but not level-1 intermittently

</td></tr><tr><td>

OneExtend

</td><td>

PRB2029681

</td><td>

Files in an update set are generated with Replace on Upgrade as false, blocking future changes to be applied

</td></tr><tr><td>

OneExtend

</td><td>

PRB2062938

</td><td>

Add early-exit in getOEUsage\(\) when OneApiServicePlan cache is empty \(don't cascade deleteMultiple\)

</td></tr><tr><td>

OneExtend

</td><td>

PRB1964693

</td><td>

There's inconsistency in token count estimation in recursive summarization edge cases

</td></tr><tr><td>

OneExtend

</td><td>

PRB1974651

</td><td>

The cloned skill 'Email Response recommendation' shouldn't have a protection policy

</td></tr><tr><td>

OneExtend

</td><td>

PRB1993333

</td><td>

The Kafka plugin should not be enabled on the install of OneExtend for IntegrationHub ETL Consumer

</td></tr><tr><td>

OneExtend

</td><td>

PRB1997461

</td><td>

NowLLMStreamReader.parse\(\) splits on 'data:' inside JSON content, corrupting LLM stream output

</td></tr><tr><td>

OneExtend

</td><td>

PRB2003867

</td><td>

Skill evaluation is stuck

</td></tr><tr><td>

OneExtend

</td><td>

PRB2003994

</td><td>

No active model request transformer is found for a configuration error in the logs

</td></tr><tr><td>

OneExtend

</td><td>

PRB2037775

</td><td>

Across multiple app nodes, streaming parser fails on the content\_filter\_results field and a '\{0\}' placeholder is unsubstituted in the error message

</td></tr><tr><td>

Oracle Reconciliation

</td><td>

PRB1947071

</td><td>

The vCenter license consumption for Oracle databases show zero although its ESX servers are requiring licenses

</td></tr><tr><td>

Password Reset

</td><td>

PRB2018445

</td><td>

Large table handling of the sys\_user\_grmember table from the PwdVerificationManager getVerificationIdsForUser function

</td></tr><tr><td>

PDF Generation

</td><td>

PRB2016254

</td><td>

There's an intermittent PDF generation issue

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB2014881

</td><td>

Core UI widget date settings aren't retained on dashboards

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1993498

</td><td>

Multiple errors are observed in the sys\_log table related to the PACorrelationCalculator job

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB2000268

</td><td>

The wrong formula score is shown when filtered on multiple elements

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB2032037

</td><td>

The Platform Analytics dashboard filters ignore Element Security Lists and display 'Nothing is available'

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1999245

</td><td>

Discrepancies with Core UI on change and change percentage

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1990900

</td><td>

The system property com.snc.pa.dm.enable.mlb is set to true on non-Raptor DB Pro instances

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB2009821

</td><td>

System log shows the error message 'Analytics framework send status not success, instead is 7'

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB2035061

</td><td>

Core UI widgets render blank data for fiscal and business calendar indicators

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB2069060

</td><td>

Performance Analytics Word Cloud does not refresh when navigating between months using forward/backward arrows

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1949829

</td><td>

Breakdown elements aren't displaying consistently on the 'workbench' widget

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1989421

</td><td>

Platform Analytics's historical data collection is overriding the indicator score even when 'Collect Indicator' is set to 'False'

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1995131

</td><td>

There are Query Builder \(QB\) and Workspace UI error popup clips in the surrounding UI if a query fails for CMDB NLQ

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB1997535

</td><td>

The Platform Analytics Workspace KPI Library is visible to users with no permission

</td></tr><tr><td>

Performance Analytics

</td><td>

PRB2054497

</td><td>

Data snapshot indicator charts fail to render

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2032319

</td><td>

Localized names on the Performance Analytics and Reporting \(PAR\) dashboard are no longer displayed

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2065499

</td><td>

PostgreSQL Column related error messages when accessing dashboard

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB1993725

</td><td>

Dashboard events are stuck due to an invalid user ID in the DashboardStats class

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2040129

</td><td>

Optimize the reparenting script

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2035261

</td><td>

Advanced Filter doesn't work as expected for certain filters in the Data Visualization dashboard in Platform Analytics

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2036145

</td><td>

In data visualization, the 'Type' column in the 'Count' table isn't using translations

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2036516

</td><td>

A calendar report of some Platform Analytics dashboards isn't displaying for specific users

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2050570

</td><td>

Core UI dashboards displayed in library for users without roles

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2014826

</td><td>

There's missing indicator values in Performance Analytics dashboard/Data Visualization

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2021109

</td><td>

Indicator scorecard visualization does not show the previous score for 'Sort by' as 'Name'

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2031447

</td><td>

A data visualization type is duplicated post-Australia upgrade

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2060938

</td><td>

Bookmarked filter not working correctly in Platform Analytics

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB2079191

</td><td>

Remove sys\_script\_fix\_ee3a858a4b8203101a31117f2974612b.xml

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB1793036

</td><td>

The PA\_Contributor role can't get to the 'Scoresheet' module

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB1966987

</td><td>

There's a column filter issue in the data visualization library page, 'Does Not contain' isn't working on the 'Owner' column

</td></tr><tr><td>

Platform Analytics Component API

</td><td>

PRB1992199

</td><td>

'Not used in any dashboard' displays incorrect results

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2008600

</td><td>

Platform Analytics Experience \(PAE\) tab translations don't work in non-English instances

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1989067

</td><td>

Remove the info banner on Core UI dashboard overview page

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2058867

</td><td>

Reduce the call cost on calling isPaPremium for every dashboard get call

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2037426

</td><td>

scoreType is forced to 'latest' for non-aggregate indicators due to an undefined aggregateIndicator check

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2031048

</td><td>

Platform Analytics dashboards aren't loading and are stuck in a loading state indefinitely

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1999703

</td><td>

A dashboard can't be shared to all internal users, or with users with at least one role

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1998865

</td><td>

Sys ID is automatically populated for the value in sys\_translated

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2037900

</td><td>

New dashboard widget created for sub-domain

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2037993

</td><td>

Searching a dashboard in English does not display any results when the instance is set on Finnish

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2019318

</td><td>

The 'hideNewMigratedDashboardModal' boolean is ignored in the 'Preference' JSON field of the dashboard API whenever there is a broken filter component in the migrated dashboard

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2002552

</td><td>

Due to VCS update set collision, a dashboard save fails with a generic error: 'Your dashboard could not be saved'

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1970352

</td><td>

Not enforcing the ACL in DataManagerService.getWidgetProps

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1846141

</td><td>

Certain missing properties for a visualization can cause side effects

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2050660

</td><td>

Par\_dashboard\_tab records are created unintentionally when a non-admin user accesses an inactive dashboard

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2035747

</td><td>

The **Create New** and **Duplicate** buttons in the Platform Analytics dashboard context menu are visible to users who don't have the pa\_admin or pa\_power\_user role

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2038900

</td><td>

Platform Analytics Release \(PAR\) dashboard's saved filters drop on 'GET' \(200, empty filters\) when a referenced saved/library filter is unresolvable \(deleted or cross-domain\)

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2053337

</td><td>

There's an increased response time of Core UI dashboards in Australia

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2059204

</td><td>

Non-admin users can't read a localized tab name on PAR dashboard in a scoped application

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2074215

</td><td>

Next Experience dashboards' domain has visibility issues

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1969752

</td><td>

Cached toolbox items cause options to remain in a previously selected language

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1974613

</td><td>

Color cache for mobile visualizations doesn't evict when there is a database update

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1983811

</td><td>

Unexpected response format for users without assigned roles

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1989343

</td><td>

After a Glide upgrade, dashboard HTML rich text widgets are missing spaces that originally separate the boldfaced text

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1992984

</td><td>

Can't share a dashboard to all internal users \(users with at least one role\)

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1995194

</td><td>

Widget collisions aren't checked when importing new widgets using update sets

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB1997164

</td><td>

Users are unable to sort the 'Saved Data Visualization' library when adding an element

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2000095

</td><td>

The Guided Tour does not populate route parameters for 'default' dashboards, which breaks the functionality

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2001651

</td><td>

Widget creation on a fresh dashboard in the second tab has unnecessary DB calls

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2005163

</td><td>

Rich text styles defined using &lt;style&gt; tags are not retained in Next Experience dashboards.

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2005188

</td><td>

Override the scope of any par\_dashboard\_\* record with the scope received from the dashboard

</td></tr><tr><td>

Platform Analytics Dashboard API

</td><td>

PRB2007784

</td><td>

DomainService uses DomainSupport.hasAccess instead of DomainHierarchy for validation

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB2031506

</td><td>

The 'Follow' filter toggle option is missing in a cascading filter

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB2052543

</td><td>

Interactive dashboard filters aren't applied to workbench data visualization

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB2019783

</td><td>

The 'Copy link with filters' feature is broken for some filters

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1976646

</td><td>

A hierarchical filter isn't working

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB2013316

</td><td>

Additional controls for single and multi select

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB2014365

</td><td>

JavaScript-based sys\_choice labels are rendered as raw text in dashboard filters

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB2018497

</td><td>

When using a date/time filter, the 'Today' predefined range incorrectly starts from the current hour instead of all of today.

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB2021606

</td><td>

An interactive filter can be cleared via a double-click even when the 'Allow User to Clear Filter' option is turned off

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB2057654

</td><td>

Unable to access any filter except for the first filter using the keyboard

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1972756

</td><td>

When adding a filter to a dashboard, the data source doesn't appear until changes are made

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1989369

</td><td>

The REST API '/api/now /da/unifilter /da\_data/calendars' fails with an error when accessed from a user with a snc\_external role

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB1993721

</td><td>

A dashboard's Year to Date \(YTD\) filter fails to apply on a list unless it's reset

</td></tr><tr><td>

Platform Analytics Filters

</td><td>

PRB2003187

</td><td>

The Resource Management Workspace date for the dynamic filter 'this year' defaults to 2025

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1989820

</td><td>

Users with the itil role are shown reports in read-only mode

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2064612

</td><td>

Dashboard owner migration creates new pa\_dashboard records when triggered from a child domain

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2013849

</td><td>

The scheduled report recipient user list might contain email addresses

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1982635

</td><td>

Support for report\_group and report\_global roles to edit visualizations

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2034116

</td><td>

Upgrading from Yokohama to Zurich causes all pa\_widgets to be migrated after upgrade

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1997683

</td><td>

Partial dashboard migration and rollback from a non-global domain creates duplicate records inside the domain

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2035131

</td><td>

Scheduled report XLSX file type migrates as XLS in Platform Analytics Scheduled Export

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2009064

</td><td>

The calendar report event displays fields that are not migrated correctly for all tables

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2003609

</td><td>

After migration, widget settings are lost

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1988855

</td><td>

Static content block in core UI after migration has HTML tags in the Next Experience rich text visualization

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2037846

</td><td>

The Migration Center summary count doesn't match the list count for fully migrated dashboards

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2010427

</td><td>

Turn off auto-conversion of homepages to CoreUI dashboards after upgrades

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2016359

</td><td>

After the full migration, Core UI reports are not automatically redirecting to their newly migrated versions

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2022611

</td><td>

After Dashboard migration to PAR Dashboard, the par\_dashboard\_tab.active doesn't show expected value \(Default value: true\)

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2051951

</td><td>

A scheduled report banner link leads to 'Page not found'

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2062351

</td><td>

The 'Welcome to Platform Analytics' modal reappears when a dashboard is opened with a nonexistent filter sys\_id, and preferences are entirely omitted from a dashboard GET response

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2064550

</td><td>

A dashboard group role is migrated incorrectly

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1986070

</td><td>

When migrating from a dashboard library active experience, the value should be empty until activation

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB1998821

</td><td>

The Platform Analytics Migration Center summary window isn't counting all domain dashboards when doing migration in the global domain

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2000963

</td><td>

Selecting 'Data Visualization \[Open Incidents older than 30 Days' displays '\{\}'

</td></tr><tr><td>

Platform Analytics Migration API

</td><td>

PRB2071058

</td><td>

Drilldown works on dashboards after migration if, in the CoreUI, the second drilldown has a drilldown view but that view isn't passed to the migrated reports drilldown

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB2036838

</td><td>

Prevent inserting invalid macronames into sys\_allowlist\_macro\_template table

</td></tr><tr><td>

Platform Runtime

</td><td>

PRB1996636

</td><td>

An orbit dist-upgrade preserves the previous version of conf/tomcat-host.xml on node upgrades for self-hosted instances

</td></tr><tr><td>

Playbook Experience

</td><td>

PRB1975947

</td><td>

The record generator activity title doesn't translate after language translation

</td></tr><tr><td>

Playbook Experience Core

</td><td>

PRB1990565

</td><td>

In RestartValidator.java, there's no size limit to the fLaneEndActivityCache object, which causes memory issues

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB2000782

</td><td>

Playbook instructions and 'wait for' conditions don't reflect updates when running

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB2026890

</td><td>

Playbook translations are broken if messages cost more than 255 tokens and some changes are made to them

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB2063408

</td><td>

PDSynchronizer isn't capturing trigger deletion when committing update sets on an existing playbook

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB2036445

</td><td>

Activating a playbook for the first time doesn't include a snapshot in the update set, but it's added in future activations

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB2056633

</td><td>

A Playbook activity start delay doesn't work if its less than 11 seconds

</td></tr><tr><td>

Playbooks \(Family Channel\)

</td><td>

PRB1991515

</td><td>

After a restart, the stage is still displayed even when the conditions aren't met

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB2034169

</td><td>

ML Prediction fails for solutions trained with Database View when predicted using predictionAPI

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB2061744

</td><td>

Previous records of 'ml\_model\_artifact' are still present in the sys\_attachment table for the Data Analysis capability

</td></tr><tr><td>

Predictive Intelligence

</td><td>

PRB1995939

</td><td>

An exception was caught when getting the Glide record iteratorCannot invoke 'com.glide.script. GlideRecord. getQueryString\(\)', because 'gr' is null

</td></tr><tr><td>

Problem Management

</td><td>

PRB2007965

</td><td>

Selecting 'Submit' on a new problem task leads to the page 'The page you are looking for could not be found. null.do?sys\_id=null'

</td></tr><tr><td>

Problem Management

</td><td>

PRB2052896

</td><td>

When running the Problem Management migration utility, the 'New' UI action on the problem\_task table persists as a blocker in the migrate step post-plugin activation

</td></tr><tr><td>

Problem Management

</td><td>

PRB2039358

</td><td>

Reference qualifier for the problem field on the problem task table is not working

</td></tr><tr><td>

Problem Management

</td><td>

PRB1981716

</td><td>

On Service Operations Workspace, when creating a problem task from a problem, it throws query match errors

</td></tr><tr><td>

Problem Management

</td><td>

PRB1998899

</td><td>

The 'Duplicate of' field remains visible and editable on a 'Problem' form after closing the 'Mark Duplicate' dialog

</td></tr><tr><td>

Process Mining

</td><td>

PRB1984640

</td><td>

'AND' isn't translated into Japanese in a list in Condition Builder

</td></tr><tr><td>

Process Mining

</td><td>

PRB2022864

</td><td>

Users are unable to edit access for Now Assist creator's 'Work Notes Analysis' skill

</td></tr><tr><td>

Procurement

</td><td>

PRB1675022

</td><td>

The user can't allocate the rights for an Unlimited Software license through a source request

</td></tr><tr><td>

Product Catalog

</td><td>

PRB1974010

</td><td>

'Publish to Software Catalog' inserts many records to the 'Software Model' table when 'OK' is selected many times

</td></tr><tr><td>

Product Catalog

</td><td>

PRB2055388

</td><td>

'Publish to Software Catalog' inserts many records to the Software Model Table when 'OK' is selected many times

</td></tr><tr><td>

Project Management

</td><td>

PRB1971422

</td><td>

The project workspace grid view is broken with the property 'glide.sys.time\_format' is set to HH:mm'

</td></tr><tr><td>

Project Management

</td><td>

PRB2014422

</td><td>

Copying a partial project in Project Workspace doesn't work as expected after upgrading to Australia

</td></tr><tr><td>

Project Management

</td><td>

PRB2033720

</td><td>

Duplicate cost plan breakdown records are created

</td></tr><tr><td>

Project Management

</td><td>

PRB2031214

</td><td>

Date formats switch, causing future/past dates

</td></tr><tr><td>

Project Management

</td><td>

PRB1887401

</td><td>

The Project Task has discrepancies in numbers between 'Actual Effort' and 'Total' hours from the time cards

</td></tr><tr><td>

Project Management

</td><td>

PRB2021806

</td><td>

Add a 'No status' option to the 'Project status' field

</td></tr><tr><td>

Project Management

</td><td>

PRB2051138

</td><td>

A blank project is created when a project template is applied to a project that has parent set as a task record, such as an incident or case

</td></tr><tr><td>

Project Management

</td><td>

PRB2063176

</td><td>

When a project task is created that's associated to a parent project, it displays info messages such as: 'cost plan not moved as it has actuals recorded against it'

</td></tr><tr><td>

Project Management

</td><td>

PRB2009176

</td><td>

Opening the Project Status Report in the Project Workspace triggers an update to the 'Overall Health' field on the corresponding project record

</td></tr><tr><td>

Project Management

</td><td>

PRB2009837

</td><td>

In Project Workspace, the checkbox 'Derive time component from planned dates' shows as unchecked, but in project form it's checked

</td></tr><tr><td>

Project Management

</td><td>

PRB2023802

</td><td>

The PowerPoint export service loses the connection

</td></tr><tr><td>

Project Management

</td><td>

PRB2031066

</td><td>

Custom date fields move by one day prior when the short description or any related fields are edited from the planning page of the project

</td></tr><tr><td>

Project Management

</td><td>

PRB2033458

</td><td>

Incorrect 'planned start and end date' on a new Program record

</td></tr><tr><td>

Project Management

</td><td>

PRB2034293

</td><td>

In project\_key\_milestone\_baseline, 'Key Milestone' = false when it should be true

</td></tr><tr><td>

Project Management

</td><td>

PRB2035917

</td><td>

The Project Portfolio Management \(PPM\) gs.nowDateTime\(\) isn't working as expected

</td></tr><tr><td>

Project Management

</td><td>

PRB2036275

</td><td>

ProjectTemplate.java calls extension point outside null guard, so applyTemplate\(\) silently returns zero tasks within flow execution context

</td></tr><tr><td>

Project Management

</td><td>

PRB2038762

</td><td>

Remove the logging found in the 'ProjectTaskManagerUtil' Script Include

</td></tr><tr><td>

Project Management

</td><td>

PRB2051929

</td><td>

The view of the 'Status' report from the Native UI still reflects the previous planning console instead of the new project workspace

</td></tr><tr><td>

Project Management

</td><td>

PRB2052920

</td><td>

The 'Recalculate Resource Cost' function isn't updating child assignment costs because the rate model line attribute uses a comma decimal separator

</td></tr><tr><td>

Project Management

</td><td>

PRB1946863

</td><td>

The pmview.do doesn't re-direct to the copied project status report

</td></tr><tr><td>

Project Management

</td><td>

PRB1993708

</td><td>

When moving a story from one project to another, the actual effort doubles on the story

</td></tr><tr><td>

Project Management

</td><td>

PRB1993709

</td><td>

Fix the 'Identify discrepancies in project budget' diagnostic for the project\_funding budget

</td></tr><tr><td>

Project Management

</td><td>

PRB1996888

</td><td>

A business rule doesn't run during an import of a .mpp file via the Planning Console

</td></tr><tr><td>

Project Management

</td><td>

PRB1998954

</td><td>

The cost-type field is empty at the cost plan breakdown level when they're created manually

</td></tr><tr><td>

Project Management

</td><td>

PRB2004980

</td><td>

The 'Deny unless' confidentiality ACL on rm\_story has no empty top\_task check

</td></tr><tr><td>

Project Portfolio Management

</td><td>

PRB1992034

</td><td>

There's slowness in the 'my funds' page

</td></tr><tr><td>

Record Hierarchy

</td><td>

PRB2011614

</td><td>

When a record hierarchy status record is deleted, performing reconciliation should correct it

</td></tr><tr><td>

Record Hierarchy

</td><td>

PRB2014979

</td><td>

Allow RecordHierarchies to always be usable optionally unless it is disabled

</td></tr><tr><td>

Record Watcher

</td><td>

PRB2016869

</td><td>

IndirectRecordCollector. setPreviousValueFrom PreviousRecord throws an error on a null ElementDescriptor in a dotwalked path, aborting Record Watcher enqueue and stalling flows

</td></tr><tr><td>

Record Watcher

</td><td>

PRB2025399

</td><td>

RW table check fires after ACL work has already completed, not before

</td></tr><tr><td>

Record Watcher

</td><td>

PRB2001765

</td><td>

Record Watcher \(RW\) indirect responders register expensive dot-walk RW conditions causing thread saturation, and auto-disable threshold \(1000ms\) fails to protect in time

</td></tr><tr><td>

Record Watcher

</td><td>

PRB2051122

</td><td>

The filter 'Created on last 15 minutes' on the All Alerts list causes issues with live updates

</td></tr><tr><td>

Record Watcher

</td><td>

PRB1922737

</td><td>

The dotwalk condition causes a StringIndexOutOfBoundsException

</td></tr><tr><td>

Related Lists

</td><td>

PRB2052094

</td><td>

Slushbucket doesn't respond in an understandable way to a reflow condition

</td></tr><tr><td>

ReleaseOps - Family

</td><td>

PRB1966100

</td><td>

Deployment Analyzer forms are broken

</td></tr><tr><td>

ReleaseOps - Family

</td><td>

PRB1951541

</td><td>

update\_set\_admin needs access to 'Promote Update Set'

</td></tr><tr><td>

ReleaseOps - Family

</td><td>

PRB1953573

</td><td>

The 'Integrate DR' subflow should fail on an unexpectedly already-committed update set

</td></tr><tr><td>

ReleaseOps - Family

</td><td>

PRB2054099

</td><td>

Deployment Analyzer scans can hang indefinitely, and there's no watchdog, unbounded update-set cursor, or incomplete cleanup on failure

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

</td><td>

PRB1950825

</td><td>

Remote Process Synchronization \(RPS\) sends more records to the target than that published into the transport queue

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

</td><td>

PRB2029287

</td><td>

The ProcessSyncUtil script include contains an HTML comment in the JavaScript

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

</td><td>

PRB1961089

</td><td>

The the 'Inbound' state is in error, and inbound queue processing is blocked until this is addressed

</td></tr><tr><td>

Remote Process Synchronization \(Family Release\)

</td><td>

PRB1989445

</td><td>

DBAttachmentEntries are captured in cdc\_queue\_ih when the record they are intended for doesn't exist yet when using a gateway for sys\_attachment

</td></tr><tr><td>

Remote Tables

</td><td>

PRB1797945

</td><td>

Flow Triggers don't work on scoped applications

</td></tr><tr><td>

Reporting

</td><td>

PRB2051420

</td><td>

Scheduled Report condition script is ignored and a report is sent outside the configured execution window

</td></tr><tr><td>

Reporting

</td><td>

PRB2055106

</td><td>

After the Australia upgrade, there are font size issues with the CoreUI-specific time series widget

</td></tr><tr><td>

Reporting

</td><td>

PRB2012300

</td><td>

ReportSaveProcessor reads all orphaned sys\_report\_mpivot\_rule rows into memory when saving a new report, causing an out of memory error

</td></tr><tr><td>

Reporting

</td><td>

PRB2056087

</td><td>

Data labels are truncated when saving a report as a PNG

</td></tr><tr><td>

Reporting

</td><td>

PRB2005733

</td><td>

Issue with drilldown Map in Reporting on Australia release

</td></tr><tr><td>

Request Management

</td><td>

PRB1996727

</td><td>

There's a duplicate stage and state in a requested item

</td></tr><tr><td>

Request Management

</td><td>

PRB1977545

</td><td>

The 'SC Order Status' and 'Standard Ticket Header' widgets display an incorrect stage

</td></tr><tr><td>

Request Management

</td><td>

PRB2010503

</td><td>

In Requested Items \(sc\_req\_item\), the 'Stage' field value differs between the list filter \(breadcrumb\), list view, and form view

</td></tr><tr><td>

Request Management

</td><td>

PRB2026831

</td><td>

Dot-walk fields from sysapproval\_approver are not shown on workspace due to an ACL evaluation issue

</td></tr><tr><td>

Request Management

</td><td>

PRB1987147

</td><td>

Users aren't able to see an approver's name in Employee Center for Catalogs during the Flow Designer 'waiting for approval' stage, though it works when the request has a workflow attached

</td></tr><tr><td>

Request Management

</td><td>

PRB1999123

</td><td>

The stage of a requested item isn't updated on the portal when a related REQ is canceled using the UI action 'Cancel Request'

</td></tr><tr><td>

Resource Management

</td><td>

PRB1981411

</td><td>

The capacity is not displaying accurately, it appears in the Estimate outside plan section in Capacity Planning

</td></tr><tr><td>

Resource Management

</td><td>

PRB2007697

</td><td>

There's a variable without initialization on the 'PlanningAttributesServiceSNC' Script Include

</td></tr><tr><td>

Resource Management

</td><td>

PRB2013218

</td><td>

The 'Extend' UI action isn't responsive when using it from the list context menu

</td></tr><tr><td>

Resource Management

</td><td>

PRB2024520

</td><td>

Fetching choices with their dependent field values to prepare criteria

</td></tr><tr><td>

Resource Management

</td><td>

PRB2032582

</td><td>

After changing the schedule, and we perform edit, allocation dailies are not deleted on traditional resource plan

</td></tr><tr><td>

Resource Management

</td><td>

PRB2033669

</td><td>

Adding or removing multiple users from the resource plan displays an empty window

</td></tr><tr><td>

Resource Management

</td><td>

PRB1939335

</td><td>

When using Resource Reports, the Resource Plan record cannot have 'Role' and specific members of that role selected, then have that member show up in the Resource list of the report

</td></tr><tr><td>

Resource Management

</td><td>

PRB1944575

</td><td>

The 'Project Member Allocation Details' monthly report should calculate correctly

</td></tr><tr><td>

Resource Management

</td><td>

PRB2006227

</td><td>

Project workspace throws invalid date errors when the RA being created lies within the project timelines

</td></tr><tr><td>

RESTMessageV2 API

</td><td>

PRB2008277

</td><td>

Using saveResponseBodyAsAttachment\(\) for application/vnd.ms-outlook response body leads to a stream closed error

</td></tr><tr><td>

Restricted Caller Access \(RCA\)

</td><td>

PRB1965463

</td><td>

A Restricted Caller Access \(RCA\) invalidation updated XML created in a target scope update set

</td></tr><tr><td>

Robust Transform Engine \(RTE\)

</td><td>

PRB1895585

</td><td>

The 'use strict' causes error while re-binding the default variables 'input' and 'answer' during script evalution

</td></tr><tr><td>

Roles

</td><td>

PRB2028915

</td><td>

Individual read and write operations on sys\_user\_has\_role records during sys\_user\_role\_contains processing can lead to increased upgrade time

</td></tr><tr><td>

Roles

</td><td>

PRB2018637

</td><td>

updateAgentRoleConfig removes all existing roles when an empty roleList is passed

</td></tr><tr><td>

Rollback and Recovery

</td><td>

PRB1741896

</td><td>

Rollback class change on TPC hierarchy records may result in orphan records on the parent table

</td></tr><tr><td>

Rollback and Recovery

</td><td>

PRB1864816

</td><td>

Users can't undelete a record from sys\_audit\_delete

</td></tr><tr><td>

Rollback and Recovery

</td><td>

PRB2010841

</td><td>

Rollback is slow when the context includes updates to choice fields

</td></tr><tr><td>

Rollback and Recovery

</td><td>

PRB2065713

</td><td>

Attempting to undelete from a large-named dropped table results in garbage SQL

</td></tr><tr><td>

Rollback Contexts

</td><td>

PRB1942654

</td><td>

'Clean Expired Rollback Contexts' job runs for an extended duration

</td></tr><tr><td>

SAML 2.0 integration

</td><td>

PRB2001729

</td><td>

A SAML request is cached and resent due to a missing header in session\_timeout.do response: 'Cache-Control: no-cache, no-store'

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB2010972

</td><td>

There's a problem with scheduled job configuration when using the 'Starting' field

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB2015240

</td><td>

Create a guard rail to protect the scheduler against misconfigured nodes to avoid impact to critical jobs

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB2034827

</td><td>

There should be visibility into when a job is scheduled to run via the 'Execute Now' related link

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB2039840

</td><td>

Offline/zombie node can acquire and hold the centralized scheduler assigner mutex indefinitely, halting job processing

</td></tr><tr><td>

Scheduled Jobs

</td><td>

PRB2065793

</td><td>

Sysauto\_report is missing a check for evaluating conditions with return error

</td></tr><tr><td>

Schedules

</td><td>

PRB2001720

</td><td>

When using GlideSchedule.isInSchedule\(\), it gets unexpected results if the user running the script doesn't have the same timezone as the schedule

</td></tr><tr><td>

Schedules

</td><td>

PRB2002192

</td><td>

The start date and end date are incorrect in the 'Form' and 'List' view of a record in the cmn\_schedule\_span table

</td></tr><tr><td>

SCIM Provider

</td><td>

PRB1973214

</td><td>

The user endpoint API does not support 'Not Specified' value in the 'Gender' field

</td></tr><tr><td>

Script Actions

</td><td>

PRB2070387

</td><td>

A previous fix impacts the 'Events' script action execution when the 'Script' field type is 'String'

</td></tr><tr><td>

Script Includes

</td><td>

PRB1842668

</td><td>

Sandboxed scripts calling the global script includes with the ESLatest toggle as 'enabled' do not do properly transition scopes

</td></tr><tr><td>

Scripting Governance Tool

</td><td>

PRB2031550

</td><td>

The Scripting Governance tool doesn't detect changes made to HTML fields within Response Templates

</td></tr><tr><td>

Search Administration

</td><td>

PRB1968215

</td><td>

Elements must only use supported ARIA attributes for the 'Search catalog' field for Service Portal \(SP\)

</td></tr><tr><td>

Security Data Filters

</td><td>

PRB1995962

</td><td>

A filtered list count is incorrect when moving from the next record arrow icon on a form header

</td></tr><tr><td>

Seismic Framework

</td><td>

PRB1973114

</td><td>

Add support for the content-length header in PUT, POST, and PATCH HTTP requests

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2076586

</td><td>

Plugin scripts aren't registered in some app nodes

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2035844

</td><td>

An apparent scope stack corruption leads to global code running under an app scope

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1886574

</td><td>

StackOverFlowError is caused by ScriptedUnsavedChangesConfirmationJsBuilder constructor

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2051345

</td><td>

Automatically created KittyScript exemptions are incorrect when using 'new GlideRecord'

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2026899

</td><td>

gs.calDateDiff throws 'java. lang-NullPointerException: date must not be null' for specific date when the timezone is set to Egypt in user preference

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1971520

</td><td>

ESLatest flag is not respected by sysauto\_scripts

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1853345

</td><td>

Using eslatest classes in script includes with caller restrictions can cause an RCA record saving error

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2051626

</td><td>

com.glide.script.sandbox.ks.watchdog.phase.duration.days reuses a sys\_id and cannot be instantiated on some instances

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2022516

</td><td>

Namespaced platform API not available in SDK runtime

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2033661

</td><td>

There's different behavior of 'instanceof Array' between Zurich and Australia

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2034671

</td><td>

Static methods of String such as String.trim are broken in Australia

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2054619

</td><td>

Instances are killed because of metaspace

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2056793

</td><td>

ESLatest sibling scopes shouldn't use scoped sandbox scopes

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB2064116

</td><td>

The user encounters a scriptable of unknown type JavaObject when passing GlideDateTime from global to ES5 applications scope

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1936658

</td><td>

The sys\_es\_latest\_script is not present in XML even when turning on ECMAScript 2021 \(ES12\) mode on 'Insert &amp; Stay'

</td></tr><tr><td>

Server-side scripts

</td><td>

PRB1967683

</td><td>

The asynchronous business rules ignores the 'Turn on ECMAScript 2021 \(ES12\) mode' flag

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2013330

</td><td>

The 'Catalog Conditions' field drop-down menu doesn't display for users with the catalog\_editor role

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1962241

</td><td>

The errors 'ReferenceError: 'sn\_scmobile' is not defined' occur during a mixed load test

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2021127

</td><td>

After upgrading to Australia, links on the catalog items description don't work

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2040266

</td><td>

g\_form.clearValue should clear the value of the Lookup Select Box, even when there are no reference qualifiers

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2009446

</td><td>

Catalog breadcrumb navigates to a blank page due to hardcoded sysparm\_view=text\_search in the search form template

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2010774

</td><td>

In the service portal the click of the categories does not do anything

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2011868

</td><td>

Stage isn't deleted from sc\_service\_fulfillment\_stage\_list after removing all its steps

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2023305

</td><td>

The related lists in the default view of sc\_cat\_item table is not visible when using time-limited roles

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2033096

</td><td>

Catalog redirection throws a 404 error page when accessed from the chat responses

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2034895

</td><td>

A draft item isn't working as expected, as an attachment isn't restored and the 'mandatory' indicator isn't working and has a blank asterisk

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2056109

</td><td>

getDisplayValue of a NoneChoice returns the label '-- None --' instead of an empty string

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2057019

</td><td>

Variable set mandatory message behavior is changed from Australia

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2070159

</td><td>

A UI Policy isn't working

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1902988

</td><td>

Service Catalog trigger does not put a call chain

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1918518

</td><td>

The **Show more** button on the standard ticket header appears invisible because the text color is' $brand-primary color' and is the same as the background

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1936696

</td><td>

The UI policy in Virtual Agent does not support the 'contains' condition

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1969157

</td><td>

Catalog items that the user doesn't have access to are displaying in search results

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1977442

</td><td>

Order guides aren't selectable in Service Catalog's Automated Test Framework \(ATF\) steps

</td></tr><tr><td>

Service Catalog

</td><td>

PRB1989265

</td><td>

The submission confirmation page has many concatenations from multiple irrelevant applications

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2004988

</td><td>

While searching for catalog items, there's no need to evaluate if at least one item is visible in category for determining the accessible categories

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2005268

</td><td>

Standard ticket action inputs ignore multi-line configuration

</td></tr><tr><td>

Service Catalog

</td><td>

PRB2006743

</td><td>

The requested\_for variable on RITM is set to a logged-in user instead of the selected user after order guide interaction

</td></tr><tr><td>

Service Catalog API

</td><td>

PRB1958054

</td><td>

There are constant 404 errors when making the call to the table API

</td></tr><tr><td>

Service Catalog API

</td><td>

PRB2040163

</td><td>

Service Catalog API returns HTTP 200 instead of error when sysparm\_item\_guid is duplicate

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB2033565

</td><td>

A UI policy action created from Catalog Builder can't be seen in the platform

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB2028753

</td><td>

UI Policies in Catalog Builder are not captured within the catalog template's scope selected

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB2030878

</td><td>

'Mode' defaults incorrectly when not specified in the catalog item configuration, blocking item submission from Builder

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB2033462

</td><td>

When creating a catalog item via Catalog Builder, UI policies configured in a previous step aren't visible on the 'Review and Submit' step

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB2053622

</td><td>

In Catalog Builder, there's an issue when multiple fields on a table have the same label

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB2060726

</td><td>

Publishing the catalog builder item deletes unrelated question choices

</td></tr><tr><td>

Service Catalog Builder

</td><td>

PRB2006808

</td><td>

The **Ask Now Assist** button doesn't work on the catalog in App Engine Studio

</td></tr><tr><td>

Service Catalog Components

</td><td>

PRB2015374

</td><td>

Ensure that &lt;iframe&gt; and &lt;frame&gt; elements have an accessible name

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1966196

</td><td>

There's an issue with 'Also Request for'

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1968570

</td><td>

Aria-required = 'true' isn't provided to the mandatory input fields

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1855054

</td><td>

Selecting the **Required Information** button in Service Portal on the iPhone doesn't focus the Input field

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1991914

</td><td>

Opening a TinyMCE PDF link in a new tab is blocked by Chrome when users click from a catalog item in a workspace where a Service Portal page is rendered in an iFrame

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB2012609

</td><td>

'Lookup Select Box' in MRVS displays the incorrect label and case-different values are rendered in widget

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB2014075

</td><td>

The Service Portal status of buttons isn't recognizable

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB2019459

</td><td>

In Service Portal, the 'My Saved Bundles' section isn't available on the 'Catalog' page at higher zoom levels

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB2021505

</td><td>

The 'SC Scroll to top' widget isn't displayed in a mobile browser after upgrading to Australia

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1968198

</td><td>

In a Catalog item with an order guide, the pages are represented as tabs, but it is not possible to navigate between the tabs

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1972660

</td><td>

The tooltip appears for the **View Cart** button but is missing for the **Proceed to Checkout** button in SC Shopping Cart base instance widget

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1976453

</td><td>

A Service Portal order guide review hides the description from a screen reader

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1976761

</td><td>

In Service Portal, a standard ticket rich text editor has an incorrect keyboard focus order

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1977104

</td><td>

When glide.attachment.extensions is set any value, like xlsx, it's not displaying as 'Supported: xlsx' in catalog pages

</td></tr><tr><td>

Service Catalog Portal Widgets

</td><td>

PRB1988371

</td><td>

There's labels that are too long on the 'Catalog' page

</td></tr><tr><td>

Service Catalog Variables

</td><td>

PRB1963743

</td><td>

Making the HTML variable read-only using the catalog client script still shows the editor bar and the large text box on the variable section

</td></tr><tr><td>

Service Catalog Variables

</td><td>

PRB2063234

</td><td>

The 'Lookup Select' box value is set to a random value when the reference qualifier condition returns no records

</td></tr><tr><td>

Service Catalog Variables

</td><td>

PRB2001459

</td><td>

g\_form.addDecoration isn't working on a multi-row variable set \(MRVS\) after a Zurich upgrade

</td></tr><tr><td>

Service Level Management

</td><td>

PRB2001036

</td><td>

In SLACalculatorNG, an unbounded schedule/DurationCalculator cache causes memory growth during bulk SLA recalculation

</td></tr><tr><td>

Service Level Management

</td><td>

PRB2009173

</td><td>

SLA Timer countdown time drifts out of sync when displayed in an inactive tab of the browser

</td></tr><tr><td>

Service Level Management

</td><td>

PRB2062232

</td><td>

The SLAAsyncQueueSNC script include retrieves a large result set from the sys\_audit table

</td></tr><tr><td>

Service Level Management

</td><td>

PRB1990465

</td><td>

HistoryWalker in CHECKPOINT mode cannot walkBackward to get the last update of task and hw.walkTo\(0\) to effectively reset itself

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2052536

</td><td>

In Service Map, additional related list tabs \(Changes-current/past, Incident, Problem\) are permanently stuck on 'Loading...'

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2040618

</td><td>

The 'Application Service Manual Ep Cleanup' job doesn't work

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1981739

</td><td>

The calculation status of tag-based services can be stuck on calculating the value

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2018275

</td><td>

'Traffic Process to Process' job can cause out of memory issues if there are many connections from LB service in the TCP table

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1998724

</td><td>

'Create Layer 2' connections causes Out of Memory \(OOM\) errors if the device has many router interfaces

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1998727

</td><td>

In the case of duplicate relation records in CMDB, not all CIs are populated in Manual Service

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1971609

</td><td>

Service Mapping Discovery runs an instance out of memory during the rediscovery process in case there are 100K discovered services in Operational Status

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2011756

</td><td>

The Service Mapping Properties pane displays raw values instead of choice labels

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2015977

</td><td>

Cmdb\_ci\_qualifier\_crud isn't recognized as a valid qualifier class in the CMDB hierarchy, leading to exceptions during recomputation

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2036299

</td><td>

After upgrading to Australia, parent.process.pid fails to resolve, which causes the 'Get Process' operation to return the full process list instead of the targeted parent process

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2036912

</td><td>

When services with the same name are created, the CreateOrUpdateITService API can fail

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2052358

</td><td>

There's an incorrect request type of 'Send for Review' action

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1536950

</td><td>

The MID Server crashes with an Out of Memory \(OOM\) error when handling a large number of file systems

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1968404

</td><td>

Excluded Ci types are being populated in tag-based services

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1971172

</td><td>

Old reconciliation rules are preventing Cloud Load Balancer CIs from being updated by a different discovery/data source

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1976036

</td><td>

Limit CIs in tag-based services count relations instead of CIs

</td></tr><tr><td>

Service Mapping

</td><td>

PRB1998862

</td><td>

Blocking a flapper value isn't working if one of the affected strategies wasn't configured to 'Block' from a Service Model

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2004318

</td><td>

The 'Create new service from here' feature causes memory issues in case there are many groups and services

</td></tr><tr><td>

Service Mapping

</td><td>

PRB2006053

</td><td>

There's a missing conditional\_table\_ query\_range ACL for the cmdb\_ci\_service\_discovered in the plugin com.snc.cmdb.it\_service

</td></tr><tr><td>

Service Model Foundation

</td><td>

PRB2066228

</td><td>

A business rule restriction to update a case for an unsupported user isn't enforced when a restriction on the criteria is turned on

</td></tr><tr><td>

ServiceNow MCP Server Security

</td><td>

PRB2050682

</td><td>

The token claim and metadata endpoints reflect a static instance URL instead of instance host

</td></tr><tr><td>

ServiceNow Otto for Code \(Family Release\)

</td><td>

PRB1884654

</td><td>

Incorrect translation in Now Assist Summarize in Canadian French

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

</td><td>

PRB2033218

</td><td>

Fluent App metadata deletions aren't propagated when installing from the app repo

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

</td><td>

PRB2013533

</td><td>

There's an unhelpful error when installing an app with an invalid scope prefix

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

</td><td>

PRB2067936

</td><td>

GlideQuery Schema.findInvalidChoiceError throws 'Cannot find function toLowerCase in object true' for non-string \(boolean\) values on choice/dot-walked fields

</td></tr><tr><td>

ServiceNow SDK \(Glide\)

</td><td>

PRB1831844

</td><td>

Users are unable to convert a sys\_app-based application due to a company key

</td></tr><tr><td>

ServiceNow Studio \(Family Channel\)

</td><td>

PRB1912330

</td><td>

Unable to grant access to manage update sets to delegated developers with App Collab

</td></tr><tr><td>

Service Portal

</td><td>

PRB2028255

</td><td>

The **Skip to chat** link fails to land its focus on the Virutal Agent **Chat** button

</td></tr><tr><td>

Service Portal

</td><td>

PRB2050574

</td><td>

Two 'Data Table from Instance Definition' widgets on the same portal page share pagination

</td></tr><tr><td>

Service Portal

</td><td>

PRB2013342

</td><td>

In Australia, the Mission Control \(/mc\) portal fails to load the Bootstrap CSS \(sp-bootstrap-rem.scss\), while the same configuration works correctly in Zurich

</td></tr><tr><td>

Service Portal

</td><td>

PRB1982105

</td><td>

'End Live Chat' isn't translated for Now Assist in the Virtual Agent window

</td></tr><tr><td>

Service Portal

</td><td>

PRB1951481

</td><td>

The text 'フィルター' \(filters\) in the Faceted Search widget wraps in the Japanese language mode

</td></tr><tr><td>

Service Portal

</td><td>

PRB2020265

</td><td>

The 'Homepage Search' section isn't available at higher zoom levels

</td></tr><tr><td>

Service Portal

</td><td>

PRB1986159

</td><td>

Sorting on a reference field doesn't work in the portal for a non-English language

</td></tr><tr><td>

Service Portal

</td><td>

PRB2075083

</td><td>

'ESC' portal AI Search placeholder text customization is no longer honored after an Australia upgrade

</td></tr><tr><td>

Service Portal

</td><td>

PRB1935624

</td><td>

'Hide filters' and 'Clear All' in a facet search aren't properly aligned

</td></tr><tr><td>

Service Portal

</td><td>

PRB1935843

</td><td>

In Windows 11, from any web browsers \(i.e. Chrome or Edge\), two Korean alphabet letters are returned despite a user entering one Korean alphabet letter into a base instance Select box in base instance Service Portal and ESC portal pages

</td></tr><tr><td>

Service Portal

</td><td>

PRB1999112

</td><td>

The **Edit file name** button isn't displayed for a non-admin user

</td></tr><tr><td>

Service Portal

</td><td>

PRB2021794

</td><td>

In Service Portal, a portal title isn't visible on hover/ focus when the navbar background is white

</td></tr><tr><td>

Service Portal

</td><td>

PRB1744773

</td><td>

When copying and pasting screenshots, the mouse focus jumps to the beginning of the HTML field in the service portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB2029717

</td><td>

Selecting the tabs under 'More' of the 'Standard Ticket Tab' widget in mobile view blocks scrolling of the page

</td></tr><tr><td>

Service Portal

</td><td>

PRB2032670

</td><td>

A new tooltip appears on the ESC portal every time the user selects 'Add attachments'

</td></tr><tr><td>

Service Portal

</td><td>

PRB2009637

</td><td>

In the Enhanced Chat search bar, the up and down arrow icons are visible

</td></tr><tr><td>

Service Portal

</td><td>

PRB2058433

</td><td>

On Focus\_Open in a new tab isn't announced by a screen reader

</td></tr><tr><td>

Service Portal

</td><td>

PRB2063295

</td><td>

The user preference widget isn't working correctly when a user changes their language on the Employee Center

</td></tr><tr><td>

Service Portal

</td><td>

PRB2011240

</td><td>

Headerlist is improperly exposed to screen reader users

</td></tr><tr><td>

Service Portal

</td><td>

PRB2011496

</td><td>

When glide.invalid\_query.returns\_no\_rows is set to 'true', the user can't change the Search Application for a record producer and the reference list shows no results

</td></tr><tr><td>

Service Portal

</td><td>

PRB2013905

</td><td>

The Service Portal needs the aria-haspopup='dialog' attribute on the **Add Attachment** button

</td></tr><tr><td>

Service Portal

</td><td>

PRB2013931

</td><td>

The Service Portal renders the decorative field label element with role='button', causing WCAG violations

</td></tr><tr><td>

Service Portal

</td><td>

PRB2014571

</td><td>

Alignment of the Now Assist search results gets overflow

</td></tr><tr><td>

Service Portal

</td><td>

PRB2022012

</td><td>

In the 'Idea' portal, menu items overlap when navigating with a keyboard at 200% zoom

</td></tr><tr><td>

Service Portal

</td><td>

PRB2026359

</td><td>

The related lists label is shown in a form widget

</td></tr><tr><td>

Service Portal

</td><td>

PRB2026504

</td><td>

Setting User Preferences does not get rid of console messages

</td></tr><tr><td>

Service Portal

</td><td>

PRB2026788

</td><td>

Accessibility defect violating WCAG 2.4.1

</td></tr><tr><td>

Service Portal

</td><td>

PRB2031688

</td><td>

Multiple keyword filters on Data Table from URL widget

</td></tr><tr><td>

Service Portal

</td><td>

PRB2032297

</td><td>

When the user selects 'Clear All' \(Clear all notifications\) in the Service Portal, the tooltip remains on the screen

</td></tr><tr><td>

Service Portal

</td><td>

PRB2034084

</td><td>

In Service Portal, an incorrect role is defined for search

</td></tr><tr><td>

Service Portal

</td><td>

PRB2036450

</td><td>

Date and Date-Time variables will not add separators/auto-format unless the entered format is YYYYMMDD, even if the configured system date format is different

</td></tr><tr><td>

Service Portal

</td><td>

PRB2036660

</td><td>

The ServiceNow Portal URL is case sensitive when entered in lower case, but works properly with upper case and doesn't work in incognito mode

</td></tr><tr><td>

Service Portal

</td><td>

PRB2038007

</td><td>

When all image scale options are removed from an image scale survey question, the control is hidden in the web experience but continues to display as an empty box in the Mobile App, resulting in inconsistent behavior across platforms

</td></tr><tr><td>

Service Portal

</td><td>

PRB2039519

</td><td>

When JAWS users navigate backwards through the top navigation menu items, the screen reader does not announce the item that has cursor focus

</td></tr><tr><td>

Service Portal

</td><td>

PRB2054374

</td><td>

Properties marked as 'display read only' are editable on Service Portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB2055154

</td><td>

The 'Star' icon of knowledge articles and the 'Attachment' icon of catalog items are missing from the portal after adding the font family css incude in the portal theme

</td></tr><tr><td>

Service Portal

</td><td>

PRB2068051

</td><td>

Duplicate comments display when using the 'Ticket Conversations' widget

</td></tr><tr><td>

Service Portal

</td><td>

PRB2069512

</td><td>

There's missing focus management and screen reader announcements on expand/collapse

</td></tr><tr><td>

Service Portal

</td><td>

PRB2074191

</td><td>

In Australia, the header in Service Portal is no longer fixed at the top

</td></tr><tr><td>

Service Portal

</td><td>

PRB1589604

</td><td>

The Ticket Fields widget shows the message 'Agent working on this Incident' even when the state of the ticket is 'Pending Closure' or 'Closed', which is incorrect

</td></tr><tr><td>

Service Portal

</td><td>

PRB1839325

</td><td>

There's focus navigation issues in the login dialog after a timeout prevents screen reader users from logging back in

</td></tr><tr><td>

Service Portal

</td><td>

PRB1841663

</td><td>

Arrow key navigation in Service Portal date pickers triggers unconfirmed field value updates

</td></tr><tr><td>

Service Portal

</td><td>

PRB1938486

</td><td>

On Service Portal, the dotwalked field on the Reference field shows the time in GMT

</td></tr><tr><td>

Service Portal

</td><td>

PRB1947453

</td><td>

The Genius result 'Source' link text is overflowing in smaller devices, such as the Mobile responsive view on portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1957485

</td><td>

The 'Form' widget is not working correctly in Zurich, as it scrolls after using ctr + s to save

</td></tr><tr><td>

Service Portal

</td><td>

PRB1975222

</td><td>

In the Customer Service Management portal, a group combobox label isn't programmatically associated with an input field on the 'Save Filter' dialog

</td></tr><tr><td>

Service Portal

</td><td>

PRB1976076

</td><td>

On a record producer, after selecting a link that contains '\#' in the URL and opening a browser tab followed by going back to the previous browser tab, the page scrolls back to the top

</td></tr><tr><td>

Service Portal

</td><td>

PRB1980119

</td><td>

Update/Review dark theme uxf mappings for the search, login, and modal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1980456

</td><td>

The DateTimePicker month and year selection views are marked up incorrectly and can't be accessed via keyboard with NVDA

</td></tr><tr><td>

Service Portal

</td><td>

PRB1986569

</td><td>

Menus in the Customer Service Management and Service Operations Workspace portals aren't readable

</td></tr><tr><td>

Service Portal

</td><td>

PRB1995615

</td><td>

The '**Add Attachment Modal**' close button's label is too generic

</td></tr><tr><td>

Service Portal

</td><td>

PRB1997326

</td><td>

There's an issue when selecting an empty name in the list collector variable

</td></tr><tr><td>

Service Portal

</td><td>

PRB1998060

</td><td>

Knowledge Base icons overflow the border of the 'Knowledge Bases Browse' widget in a portal

</td></tr><tr><td>

Service Portal

</td><td>

PRB1998933

</td><td>

The language picker doesn't change the language on a Service Portal page the when user isn't logged in

</td></tr><tr><td>

Service Portal

</td><td>

PRB1999608

</td><td>

The 'Online' status has too low of a contrast

</td></tr><tr><td>

Service Portal

</td><td>

PRB2000146

</td><td>

The data picker opens in another location

</td></tr><tr><td>

Service Portal

</td><td>

PRB2000251

</td><td>

In a portal, the 'Additional Details' tab label is truncated with an ellipsis at 200% zoom and the tooltip isn't displayed on the keyboard's focus

</td></tr><tr><td>

Service Portal

</td><td>

PRB2001359

</td><td>

'●' is displayed on the 'Icon' menu list when changing the view of an sp\_instance\_menu record to the default view

</td></tr><tr><td>

Service Portal

</td><td>

PRB2002200

</td><td>

Template literals aren't working on widgets

</td></tr><tr><td>

Service Portal

</td><td>

PRB2002539

</td><td>

In Now Assist, the **Skip to Chat** link fails to land focus on the **Now Assist** button

</td></tr><tr><td>

Service Portal

</td><td>

PRB2002874

</td><td>

The 'Add Attachment' window doesn't automatically close after a second attachment is uploaded after a large attachment

</td></tr><tr><td>

Service Portal

</td><td>

PRB2002954

</td><td>

There's portal language inconsistency across tabs without a refresh

</td></tr><tr><td>

Service Portal

</td><td>

PRB2005224

</td><td>

The **Add attachments** paperclip button lacks a visual boundary at 400% zoom, appearing as a decorative icon

</td></tr><tr><td>

Service Portal

</td><td>

PRB2005660

</td><td>

Tooltips on 'Date' fields aren't shown when one of the fields in the record producer isn't visible on the form

</td></tr><tr><td>

Service Portal

</td><td>

PRB2005800

</td><td>

The attachment window continues to load when dragging / dropping an opened One Drive file

</td></tr><tr><td>

Service Portal

</td><td>

PRB1972674

</td><td>

An accessibility issue violates WCAG 2.4.1

</td></tr><tr><td>

Service Portal Announcements

</td><td>

PRB2059143

</td><td>

Service Portal announcements don't announce that they open in a new browser window/tab, because they don't provide a'click behavior for links that open in a new tab

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1989200

</td><td>

The Service Portal Core 'Categories' widget isn't displaying the badges

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB2024329

</td><td>

Post-Zurich upgrade, the date info in the CSM portal notification shifts inward when the notification card exceeds a certain width

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB2033702

</td><td>

Images in Outage descriptions do not scale on the ESC system status page

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1974442

</td><td>

The 'My Requests' widget corrupts non-English characters when switching tabs

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB1999720

</td><td>

The **Clear** button on the reference variables aren't aligned in mobile

</td></tr><tr><td>

Service Portal Core Widgets

</td><td>

PRB2000724

</td><td>

A Service Catalog item widget button's text is clipped without a tooltip on focus/hover

</td></tr><tr><td>

Service Portal Experience

</td><td>

PRB2051231

</td><td>

The user observes the error '\{0\} has been rejected' in the base instance 'Approvals' widget

</td></tr><tr><td>

Service Portal Experience

</td><td>

PRB2007912

</td><td>

The 'Approval Info Record' widget doesn't post rejection comments

</td></tr><tr><td>

Service Portal Experience

</td><td>

PRB2037025

</td><td>

Tooltip label text does not wrap for calendar date type variable

</td></tr><tr><td>

Service Portal Experience

</td><td>

PRB1827576

</td><td>

Service Portal priority data lookups don't work

</td></tr><tr><td>

Service Portal Experience

</td><td>

PRB2040365

</td><td>

The base instance 'Request and Approvals' widget is misoriented

</td></tr><tr><td>

Service Portal Experience

</td><td>

PRB2055656

</td><td>

In Australia, mandatory fields hidden by a UI Policy aren't visible on the change form in the portal, but submitting the form results in an error requiring them to be completed

</td></tr><tr><td>

Service Portal Experience

</td><td>

PRB1962633

</td><td>

Datepicker selected and current date are not announced in Portal surveys for Service Portal

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB2020351

</td><td>

AvailabilityOutageProcessor. processOutages\(\) aborts an entire CI calculation when a zero-duration outage is encountered

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB1902176

</td><td>

Five 'Subscribed by' tables have unlimited CRUD access

</td></tr><tr><td>

Service Portfolio Management

</td><td>

PRB2018406

</td><td>

The global variable answer is modified in ServiceSubscriptionUtilsSNC and that causes Automated Test Framework \(ATF\) to crash when users open the 'Variable State Validation \(SP\)' step

</td></tr><tr><td>

Session Management

</td><td>

PRB2051647

</td><td>

claimSessionSync\(\) crashes with ISE on invalidated-but-non-null HttpSession, silently cancelling REST transactions with HTTP 200

</td></tr><tr><td>

Session Management

</td><td>

PRB1941160

</td><td>

The session is invalidated when the portable Virtual Agent web client is configured on the user website

</td></tr><tr><td>

Session Management

</td><td>

PRB1985477

</td><td>

When attempting to update glide.guest.active. session.life\_span, a check is done against glide.ui. session\_timeout instead of glide.guest. session\_timeout

</td></tr><tr><td>

Session Management

</td><td>

PRB1856354

</td><td>

Clearing the affinity cookie on logout.do impacts the logout redirection flow in MultiSSO v1 and v2 flows

</td></tr><tr><td>

Session Management

</td><td>

PRB2003725

</td><td>

An unhandled exception occurs when getAttribute is called after a Glide session invalidation

</td></tr><tr><td>

Session Management

</td><td>

PRB1769499

</td><td>

Excessive guest sessions in the sys\_user\_session table

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB2009353

</td><td>

Base instance repeat value for the sidebar notification events process is excessive

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1908427

</td><td>

The 'Util' menu keeps loading if there are no conversations yet

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1993075

</td><td>

Sidebar collaboration tables aren't scope main enabled

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB2019090

</td><td>

The cached RecordCard is returned without checking if the user has access to record

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB2023462

</td><td>

Turn off the sidebar collab chat scope main enablement

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1983263

</td><td>

Users who don't have access to sys\_cs\_channel \_user\_profile can't see discussion cards in the unread tab

</td></tr><tr><td>

Sidebar \(Family Release\)

</td><td>

PRB1994558

</td><td>

When a Slack user leaves a discussion, the Slack channel is auto-deleted

</td></tr><tr><td>

Software Asset Core Company

</td><td>

PRB2005158

</td><td>

Improve NDS guided setup and proactively fix core company reference jobs by batching through local implementation

</td></tr><tr><td>

Software Asset Core Company

</td><td>

PRB1689224

</td><td>

Evaluate the unique index on the core company

</td></tr><tr><td>

Software Asset Data Import

</td><td>

PRB1921113

</td><td>

Issues with handling PPNs in the entitlement import flow

</td></tr><tr><td>

Software Asset Data Import

</td><td>

PRB2006846

</td><td>

Entitlements are created against the wrong software model when there are multiple products with the same name in the products library and an invalid publisher in the Excel sheet

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1994601

</td><td>

Subscription period field gets updated on page load for Entitlement

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2010303

</td><td>

Unable to Add software products in the Software Asset Management \(SAM\) workspace in published products list

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2017405

</td><td>

There's a missing fix script to update the label of cmdb\_model\_lifecycle

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2026233

</td><td>

Orphaned sys\_object\_source records are created when cmdb\_sam\_sw\_install records are deleted via CI retire/stolen Business Rule

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2030768

</td><td>

Content normalization seems to ignore Business Rules

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2039852

</td><td>

Missing pa\_indicators related to SAM jobs

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2040399

</td><td>

Deleting entities for absent/retired applications should trigger a Business Rule in cmdb\_sam\_sw\_install

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2043455

</td><td>

Discovery Model to Software Model causing replication lag

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2051961

</td><td>

The Software Asset Management \(SAM\) Pro 'Remove Installs For Retired/Stolen CI' business rule throws 'Unknown table: samp\_citrix\_machine' when a Citrix add-on isn't installed

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2055852

</td><td>

Downgrade rights on retired/expired entitlements still influence reconciliation grouping

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1531245

</td><td>

Generate, create, and remove allocation remediation options for CAL records

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1633805

</td><td>

Instead of splitting installs across multiple server license metrics, the highest license metric should be used

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1711856

</td><td>

BYOL for Windows Server AWS tags

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1919859

</td><td>

Allowing cross scope access to various SAM global tables

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1945220

</td><td>

Total cost calculation on a license record isn't happening on the server side

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1959048

</td><td>

De-book SAM Pro, but keep SAM Foundation features like 'Reconciliation'

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1981043

</td><td>

User resolution rules aren't working if the subscriptions don't have a UPN

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1990723

</td><td>

Multiple deletions lead to installs not deduping again

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1997126

</td><td>

A system field of Custom Software Product Lifecycles is modified by Zurich

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB1999926

</td><td>

If multiple suite children share the same discovery map \(DMAP\), it should prefer the conditionless one in content sync

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2004617

</td><td>

There's an issue with the 'SAM - identify deny list software' scheduled job

</td></tr><tr><td>

Software Asset Management

</td><td>

PRB2007293

</td><td>

Reclamation candidates don't show up in SAM workspace for hybrid products

</td></tr><tr><td>

Software Asset Management Content Service

</td><td>

PRB2048721

</td><td>

A display name on an entitlement or software model are truncated when the edition is more than 40 characters

</td></tr><tr><td>

Software Asset Management Publisher Pack for SAP

</td><td>

PRB1964218

</td><td>

There's a Software Asset Management Publisher \(SAP\) null character exception when pulling data

</td></tr><tr><td>

Software Asset Normalization

</td><td>

PRB1703274

</td><td>

Slow queries identified during OKR 2.3 executions on reconciliation, de-duplication and normalization scenarios

</td></tr><tr><td>

Software Discovery

</td><td>

PRB1815641

</td><td>

'Sync Installed Software' pre-post sensor scripts append a whitespace to Discovered Product if the edition is empty

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1670276

</td><td>

Select all functionality to be implemented in the backend along with other changes based on the UX/sprint demo feedback for copy allocations

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1961409

</td><td>

Accept the PPN suggestion 'Accept message' issue for SAMP

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1834815

</td><td>

Non-English samp\_entitlement\_import template cannot be imported from Software Asset Workspace

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1957593

</td><td>

Entitlement Import via the template fails, and the error message is, 'These custom columns do not exist on the Entitlement table: \[ 'product\(product\)', 'publisher\(publisher\)' \]'

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB1978705

</td><td>

The 'Purchase right' field allows an invalid data type

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB2001277

</td><td>

The currency on 'Total cost' is changed from USD to GBP and viceversa when a record in alm\_license is viewed

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB2004452

</td><td>

Allow users to create user subscription downgrades

</td></tr><tr><td>

Software Entitlements

</td><td>

PRB2005051

</td><td>

Attaching a SA to a P+SA entitlement doesnt work as expected

</td></tr><tr><td>

Software Lifecycles \(Family Channel\)

</td><td>

PRB2039617

</td><td>

Typo in SamLifeCycleUtils script include

</td></tr><tr><td>

Software Models

</td><td>

PRB2002367

</td><td>

A discovery model to a software model matching job doesn't update the latest log properly

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB2010080

</td><td>

'Stash Local Changes' silently fails when duplicate sys\_update\_name exists, and the phase 2 restore failure isn't surfaced in Source Control UI

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB2010981

</td><td>

getDuplicateLocalUserSpecificUpdateSet\(\) is missing sys\_created\_by filter, which causes stash changes to be written into another user's update set

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB2014590

</td><td>

Stale sys\_remote\_app record from AppRepo publish blocks source control commits with 'An App Customization already exists' error

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB2054438

</td><td>

A re-link of a customized Store app to git via Source Control fails with an error code '1030'

</td></tr><tr><td>

Source Control Engine

</td><td>

PRB1969425

</td><td>

The business rule for sys\_choice is unexpectedly triggered during the source control import

</td></tr><tr><td>

SSH MID Server Communication Protocol

</td><td>

PRB1999773

</td><td>

The SSH connection fails with an error: 'Protocol version ID is too long'

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB2012125

</td><td>

There's no tooltip on the Standard Ticket header for the caller when the text is truncated due to text spacing/language

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB1995556

</td><td>

There's an error in the console log from std\_ticket\_conversations when a user closes a ticket

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB2013271

</td><td>

Screen reader announces 'hyphen hyphen' for the 'Price and Total' value in the My Requests page of the Esc portal

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB2016653

</td><td>

Hidden list elements are announced by the screen reader after the **Publish** button

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB2025957

</td><td>

Truncation in details section of portal ticket pages does not gain input focus

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB2036119

</td><td>

A standard ticket action order isn't working

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB1866256

</td><td>

The control automatically moves to the 'Order case lines' tab when the user posts something on the 'Activity' tab or makes any attachment on the 'Attachments' tab of the 'Order case details' page for Order Case on Business Portal

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB1961511

</td><td>

The menu changes from 'More' to a task upon receiving the focus for the PSDS Grants RSP Workflow Merit View task reflow

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB2002490

</td><td>

Tooltips are cropped on the 'My requests' page

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB2006602

</td><td>

There's additional padding in the standard ticket tab in portal in Australia

</td></tr><tr><td>

Standard Ticket Page

</td><td>

PRB2006776

</td><td>

User profile links \(Caller, Assigned to, etc.\) open in a new tab without any visual or programmatic indication

</td></tr><tr><td>

Stream Connect Core

</td><td>

PRB2021509

</td><td>

There's a null pointer exception in MessagePollSubscriptions. stopSubscription when a subscription isn't present

</td></tr><tr><td>

Stream Connect Core

</td><td>

PRB2001155

</td><td>

When kafka generates many errors, processing those errors can produce mutex contention

</td></tr><tr><td>

Survey Management

</td><td>

PRB1957101

</td><td>

The image added in the section 'Details' field from Survey designer does not scale to screen size when viewed from a mobile screen

</td></tr><tr><td>

Survey Management

</td><td>

PRB2013131

</td><td>

The icon is missing on the GRC classic attestation

</td></tr><tr><td>

Survey Management

</td><td>

PRB2020355

</td><td>

A French \(Canadian\) translation is missing in Risk Workspace: Assessment Instance Questions

</td></tr><tr><td>

Survey Management

</td><td>

PRB2023751

</td><td>

Service Portal $sp.getAssessmentRecord\(\) loads all custom UI Scripts regardless of the global = false flag

</td></tr><tr><td>

Survey Management

</td><td>

PRB2035926

</td><td>

In Survey Designer, icons in the 'Controls palette' take a while to load due to excessive 3,000 individual angular.do?sysparm\_type=message POSTs in a few seconds

</td></tr><tr><td>

Survey Management

</td><td>

PRB2036503

</td><td>

'Displayed when' doesn't get cleared when 'Depends on' changes on the Metric

</td></tr><tr><td>

Survey Management

</td><td>

PRB2050124

</td><td>

Customer rating feedback smiles are not displayed in survey preview or public survey link

</td></tr><tr><td>

Survey Management

</td><td>

PRB1976868

</td><td>

On a survey, the labels are concatenated together for question 1's **Very Dissatisfied** radio button

</td></tr><tr><td>

Survey Management

</td><td>

PRB2001256

</td><td>

There's long processing time when loading an assessment on a portal

</td></tr><tr><td>

Syntax Editor

</td><td>

PRB2003291

</td><td>

There's a parsing error about an unexpected token when trying to save a modern JavaScript

</td></tr><tr><td>

System Archiving

</td><td>

PRB1968962

</td><td>

Archive chunks are not processed due to 'ArchiveJob Source Record has been changed and no longer match the archive rule conditions'

</td></tr><tr><td>

System Archiving

</td><td>

PRB1988156

</td><td>

Archive reparenting doesn't work with peripherals and large table names

</td></tr><tr><td>

System Archiving

</td><td>

PRB1973927

</td><td>

An added Mutex doesn't solve problems in glommed tables

</td></tr><tr><td>

System Archiving

</td><td>

PRB1643629

</td><td>

The error 'ORA-01843: not a valid month' occurs when the user is using a non-default glide.sys.date\_format due to a missing TO\_DATE function

</td></tr><tr><td>

System Archiving

</td><td>

PRB1862202

</td><td>

The Retain Reference \(DM-Retain Reference\) doesn't migrate the inherited reference filed to the 'Reference' type in the archived child table

</td></tr><tr><td>

System Archiving

</td><td>

PRB2019849

</td><td>

ReArchiveJob fails to rearchive any records when the restored related table records exceed the GlideAggregate max limit

</td></tr><tr><td>

System Archiving

</td><td>

PRB2077698

</td><td>

Archive Restore skips related records archived from the table-rotation shard tables

</td></tr><tr><td>

System Archiving

</td><td>

PRB1924051

</td><td>

The Destroy Rule estimate recalculations triggered from the UI Transaction run synchronously

</td></tr><tr><td>

System Archiving

</td><td>

PRB1942129

</td><td>

The 'Enhance Rearchive' job to handle a large number of restored records no longer exists or matches the archive conditions

</td></tr><tr><td>

System Archiving

</td><td>

PRB1971082

</td><td>

The 'Archive Reparent Run Retry' job is causing app node reboots

</td></tr><tr><td>

System Archiving

</td><td>

PRB2007746

</td><td>

ArchiveRefJob is missing a null check

</td></tr><tr><td>

System Events

</td><td>

PRB1998319

</td><td>

A 'No Active Processor' alert generates for queues that are processing correctly

</td></tr><tr><td>

System Events

</td><td>

PRB2007066

</td><td>

Check to correct Legacy and Delegated Flow Engine jobs that are created during Upgrade

</td></tr><tr><td>

System Events

</td><td>

PRB2013207

</td><td>

The mutex contention in PerformanceStatsPersisterizor should be fixed

</td></tr><tr><td>

System Events

</td><td>

PRB1980615

</td><td>

Granular delegations with specific future start times aren't created

</td></tr><tr><td>

System Events

</td><td>

PRB2001375

</td><td>

The next discovery in the daisy chain is not triggered when the current discovery is cancelled

</td></tr><tr><td>

System Export Sets

</td><td>

PRB2052040

</td><td>

There's an Excel export page \(sheet\) grouping issue in Australia

</td></tr><tr><td>

System Export Sets

</td><td>

PRB1893148

</td><td>

Export Set limits are not applied from the sys\_property if the max\_rows field is not set in the Export Set record

</td></tr><tr><td>

System Export Sets

</td><td>

PRB1902474

</td><td>

The delta export in the Export Set may fail to extract all expected data

</td></tr><tr><td>

System Export Sets

</td><td>

PRB2002031

</td><td>

Export to Excel from the UI with glide.excel.use\_user\_date\_format set to true does not export in UTC date time

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1981092

</td><td>

Protocol version max length is not configurable for SCP and other data source file retrieval types utilizing SSH connections

</td></tr><tr><td>

System Import Sets

</td><td>

PRB2010797

</td><td>

SFTP scheduled imports fail, and JSch sends SSH\_MSG\_REQUEST\_FAILURE in response to SSH\_MSG\_GLOBAL\_REQUEST with want\_reply=FALSE

</td></tr><tr><td>

System Import Sets

</td><td>

PRB2033737

</td><td>

role mis\_server can't read database credentials for a JDBC data source when it uses an alias

</td></tr><tr><td>

System Import Sets

</td><td>

PRB2038233

</td><td>

JDBC connections are left dangling and unclosed

</td></tr><tr><td>

System Import Sets

</td><td>

PRB2041445

</td><td>

Missing column names from the mapping UI when importing Excel files through IntegrationHub import UI

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1920195

</td><td>

There's a scaling issue with concurrent import sets

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1939583

</td><td>

The delegated developer \(app collaborator\) is not able to edit data import integrations whenthe role is inherited from the user group

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1981401

</td><td>

Users can't write to the path '/glide/nodes/&lt;node&gt;/bin../tmp/' due to a java.io.IOException: 'Separation boundary was not specified: com.glide.ui.multipart.MultipartParser'

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1994594

</td><td>

The custom parse by script option doesn't support custom content types

</td></tr><tr><td>

System Import Sets

</td><td>

PRB1946880

</td><td>

StreamConnect RTE Consumer misses messages when there are two consumers per node

</td></tr><tr><td>

System Notifications

</td><td>

PRB1857726

</td><td>

label.notify event isn't triggered when creating a change request and the change notification email is never sent

</td></tr><tr><td>

System Notifications

</td><td>

PRB2012118

</td><td>

Meeting invites in Outlook Calendar don't obey the due date in the reminder

</td></tr><tr><td>

System Notifications

</td><td>

PRB2014459

</td><td>

In chunked emails with BCC addresses, only the first email has a To: address, and the other chunks have no To: address

</td></tr><tr><td>

System Notifications

</td><td>

PRB1938027

</td><td>

A new notification makes all other notifications unread in Next Experience

</td></tr><tr><td>

System Scheduler

</td><td>

PRB2021066

</td><td>

Child jobs for active nodes trigger propagation to standby nodes

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1759437

</td><td>

The sys\_nlu\_model related link action 'Add model to update set' captures records from 'NLU BatchTest set' and 'NLU Batch Test Utterances' in the global scope to the parent batch update set

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1897281

</td><td>

Loading the 'Details' page for an app that has excessive number of customizations fails due to having to load too many rows

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1982348

</td><td>

An update set commit schedules multiple upgrade summary jobs

</td></tr><tr><td>

System Update Sets

</td><td>

PRB2004557

</td><td>

MetadataListener.handleScopeOrPackageUpdate\(\) calls getFileName\(\) without the isLoadingFile\(\) guard, causing 'FileInfoStack is empty' errors during update set commits

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1976017

</td><td>

When a child table was deleted, the update set deletes the parent table's sys\_ui\_list\_elements records

</td></tr><tr><td>

System Update Sets

</td><td>

PRB2016304

</td><td>

An error appears when the user backs out an update set, repairs the application, commits the same update set again, then backs out again

</td></tr><tr><td>

System Update Sets

</td><td>

PRB2031247

</td><td>

Update set install tracking captures a store app as 'plugin' instead of 'application' for admins without elevated privileges

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1972147

</td><td>

The 'Publish Customizations to Update Set' UI action is not working when app customization is not installed

</td></tr><tr><td>

System Update Sets

</td><td>

PRB1983964

</td><td>

If the update set sources are part of any related lists, 'Retrieve Completed Update Sets' doesn't work

</td></tr><tr><td>

System Web Services

</td><td>

PRB2029605

</td><td>

There's hourly recurring OAuth authentication failures on an outbound REST from ST ServiceNow to CG ServiceNow: 'User is not authenticated. OAuth token has expired or has not been retrieved'

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1950018

</td><td>

When changing the string column max\_length from 256 to 255, it converts MEDIUMTEXT to VARCHAR\(255\) on the source, but when applying it on a target instance, the DB type remains MEDIUMTEXT

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1934831

</td><td>

Multi-row variable set values are not visible in the German language

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB2018419

</td><td>

Tables with definitions that have multiple 'primary = True' keys fail to create a table on RaptorDB / Postgres

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB2021330

</td><td>

Guid.build\(metadataId, UNIQUE\_KEY\) in MetadataDelete.java produces deterministic collisions causing unique key constraint violations on sys\_metadata and sys\_metadata\_delete during deleteMultiple\(\) operations

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1757717

</td><td>

addValue \(string field, number value\) isn't working as expected on the 'number' field in the 'sys\_number\_counter' table

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB1704723

</td><td>

TPP partitions created during an application install are created in the scope of application with the risk of having the tables dropped during application uninstall

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB2020960

</td><td>

Selecting 'Advanced view' on a dictionary record with choice=0 causes new updates on records

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB2051151

</td><td>

In List filter, the Watch List does not map correctly in Database View

</td></tr><tr><td>

Table Administration and Data Management

</td><td>

PRB2074481

</td><td>

The max length is set incorrectly for columns created with an update set

</td></tr><tr><td>

Table Builder \(Family Release Channel\)

</td><td>

PRB1934309

</td><td>

A new form section is created instead in the 'Modify form' section interaction of the 'Service Operations Workspace New Record' view via Form Builder

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB2033264

</td><td>

DMTableCleaner doesn't honor the 'glide.db.tablecleaner.chunk\_delete\_size' value when deleting records from the sys\_attachment\_doc table

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB2060180

</td><td>

A stuck data management run reactivation breaks table cleaner's slow rule check

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB2077554

</td><td>

The URC audit cleanup query on sys\_audit uses the low-selectivity \(tablename\) index instead of the unique documentkey index

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB1962520

</td><td>

Slow DM Table Clean performance when there are a lot of records to clean up

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB1966084

</td><td>

Cascade delete fails when the table is audited and record serialization fails

</td></tr><tr><td>

Table Cleaner

</td><td>

PRB1976491

</td><td>

DMJob Table Cleaner doesn't delete attachments for shared/extended tables

</td></tr><tr><td>

Table Rotation

</td><td>

PRB1959672

</td><td>

Shard tables aren't created on an initial plugin install

</td></tr><tr><td>

Table Rotation

</td><td>

PRB1925500

</td><td>

Sync lock is held when running a blocking operation

</td></tr><tr><td>

Tables and Columns Data Dictionary

</td><td>

PRB2015281

</td><td>

Dependent choices filter on a session domain instead of a record domain

</td></tr><tr><td>

Tables and Columns Data Dictionary

</td><td>

PRB2002096

</td><td>

A null pointer exception \(NPE\) occurs in ChoiceList\#addNoCheck when the cache contains a null value, causing a 500 error on service portals

</td></tr><tr><td>

Tables and Columns Data Dictionary

</td><td>

PRB1667567

</td><td>

Lists load slowly

</td></tr><tr><td>

Tables and Columns Data Dictionary

</td><td>

PRB2036958

</td><td>

A Reference field with a coalesce function causes multiple issues including missing records in the List View

</td></tr><tr><td>

Test Management 2.0

</td><td>

PRB2005090

</td><td>

When the test plan of a test cycle is changed, the related test execution suites don't update their top task accordingly

</td></tr><tr><td>

Text Indexes

</td><td>

PRB1922239

</td><td>

TS Search Stats should use rollups

</td></tr><tr><td>

Time Card Management

</td><td>

PRB2012627

</td><td>

Base instance timesheet portal has an error when copying a previous timesheet and submitting

</td></tr><tr><td>

Time Card Management

</td><td>

PRB2026225

</td><td>

Performance Analytics Widget 'Time Card Count' only shows Capex Time Cards

</td></tr><tr><td>

Time Card Management

</td><td>

PRB2035011

</td><td>

An incompatibility was found in the 'Time card functions' business rule

</td></tr><tr><td>

Time Card Management

</td><td>

PRB2065815

</td><td>

The max hours per day is not properly validating on time card submissions/approvals

</td></tr><tr><td>

Time Card Management

</td><td>

PRB2068605

</td><td>

Base instance client callable script include AjaxaUserRateTypeSetting doesn't have an execute ACL defined

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1978766

</td><td>

There's an empty row below the last 'insert' row in the Time Sheet Portal

</td></tr><tr><td>

Time Card Management

</td><td>

PRB1989255

</td><td>

There's a slow response loading the group tasks of the Time Sheet Portal

</td></tr><tr><td>

Time Card Management

</td><td>

PRB2004591

</td><td>

The time card 'Recall' functionality updates unqualified time cards if they're selected together with qualified ones in the list

</td></tr><tr><td>

Transform Maps

</td><td>

PRB1680756

</td><td>

Enforcing the 'Mandatory' field because they are not showing in an import set

</td></tr><tr><td>

UI Actions

</td><td>

PRB2019114

</td><td>

A UI action with g\_modal in a workspace client script isn't working after switching the record tabs in the Workspace UI

</td></tr><tr><td>

UI Actions

</td><td>

PRB2033622

</td><td>

showFrame method throws the error 'GlideWindow.locate: window not found'

</td></tr><tr><td>

UI Actions

</td><td>

PRB2054405

</td><td>

The **Delete** button on sysapproval\_approver is displayed to a normal user

</td></tr><tr><td>

UI Builder \(Family Channel\)

</td><td>

PRB1991548

</td><td>

Empty roles are created in the sys\_user\_ has\_role table due to the ui\_builder\_ admin role containing the empty role reference

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2024073

</td><td>

An HTML type field doesn't always display as full size when its in read-only

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2022658

</td><td>

On the Effort Type = FTE field on the Resource Assignment form, when the user enters the Effort value using a dot, the system automatically converts it to a different value

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1948198

</td><td>

The Service Operations Workspace \(SOW\) 'Template creation' field dependencies are working inconsistently

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1998962

</td><td>

Mandatory fields marked with an asterisk should provide a persistent explanatory note on any form that explains what the asterisk signifies

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2039055

</td><td>

Australia upgrade, 'unsaved field indicator' tooltip is not translated

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2002879

</td><td>

A staged value change isn't working for styling changes to content in the html-editor field

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2000648

</td><td>

The 'Community' activity feed is empty for very active community members

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1982868

</td><td>

The pop-up related to the Comment/Work Note web link only displays in the boundary of the 'Compose' tab

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1554026

</td><td>

The sys\_id of a dot-walked record is unavailable, and the include\_sys\_id\_in\_fieldlist attribute is not honored

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2006816

</td><td>

In Brazilian Portuguese, the 'Paste Formatting Options' modal isn't translated in workspaces

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1976513

</td><td>

showFieldMsg is unexpectedly dismissed for the 'Date' and 'Date/time' fields in workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2052871

</td><td>

Field autocomplete issue

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2009135

</td><td>

There is a filter anomaly on Affected CIs

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2015937

</td><td>

Table name can't be null: java.lang.IllegalStateException

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2021202

</td><td>

'Is not a valid time. Please use format: HH:mm:ss' is hardcoced

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2021320

</td><td>

Now Assist Context Menu does not work in Workspace, specifically in the Safari browser

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2026157

</td><td>

Editing reference fields display no records found when blank in Service Operations Workspace Lists

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2027117

</td><td>

Choices are not populated on dependent fields in Workspace but are working in the native view

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2035391

</td><td>

JPY currency is displayed with an unnecessary decimal field in workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2040359

</td><td>

The 'Attachments' component isn't working for multiple files when the 'Show preview' modal during an upload option is turned off

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2041432

</td><td>

After upgrading to Australia, when editing a template record the template field is narrow \(almost half the page width\)

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1858709

</td><td>

Grouped inputs \(sn-record-duration\) should be in a 'fieldset' with an appropriate 'legend' because they are all related to each other

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1921278

</td><td>

When using a playbook content item on a portal, users are unable to change the date once it is selected

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1962677

</td><td>

Text in string fields in a modal window are cut off under certain conditions in Safari

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1969092

</td><td>

The read-only/dependent/dotwalked 'Choice' field does not show the value when the reference is updated, and only shows when saving

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1971188

</td><td>

'Select variables' indicates that it is mandatory in Response Templates

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1971256

</td><td>

Horizontal layout columns cause the annotation section separator line to display as a box

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1973611

</td><td>

The field type 'URL' is blocked at 1024 characters in the Platform due to the table definition, but it's possible to go above 1024 characters when entering the value from a workspace

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1974338

</td><td>

Elements are missing accessible labels in the 'Show in Menu' formatter on the sys\_db\_object form

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1975244

</td><td>

There's incomplete error messaging on an invalid form field entry

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1976223

</td><td>

Role='status' and aria-label='Field annotation' is incorrectly provided to the 'Note' and 'Contact Information' sections

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1978859

</td><td>

The phone number format in Japanese isn't correct as Google's libphonenumber

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1979600

</td><td>

There's an unexpected query in a reference field lookup after using a 'contains' \(asterisk\) wildcard for auto-complete

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1982469

</td><td>

If hours are incremented in a workspace in the Asia/Almaty timezone, an onChange client script for the 'Time' field doesn't trigger

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1982845

</td><td>

Form &gt; Schedule Tab &gt; Date errors have aria-live=olite, but it should be aria-live=assertive

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1984741

</td><td>

There's an attachment size limit mismatch between a workspace and the backend view

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1986121

</td><td>

Phone number from Côte d'Ivoire invalid

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB1987974

</td><td>

When having two records in a table with the same name and different values, using a record of one in a reference field might overwrite the other

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2005159

</td><td>

The 'sr-only' element on the login page isn't announced or exposed

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2005754

</td><td>

Override risk score message 'Prevents automatic recalculation of risk score' isn't announced to screen readers when the checkbox is selected

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2006777

</td><td>

The reference field **Magnifying glass** button fails to load records

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2007058

</td><td>

The label or instructions for the 'Watch list' field uses unexpected terms, such as 'pill\(s\)'

</td></tr><tr><td>

UI Field Administration

</td><td>

PRB2007398

</td><td>

Autosize level doesn't work as expected in Workspace as compared to the native UI

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2040665

</td><td>

Section Separator form annotation with no annotation text wrongly shows a DIV with blue background

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2057308

</td><td>

A workspace view rule causes Service Operations Workspace's 'Incident Overview Summary' section contents to not display

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1963251

</td><td>

The UI action with an empty onClick field causes a parsing error when the form and related lists load

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1915534

</td><td>

Dictionary files need to be updated to reflect the sys\_metadata extension

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1789457

</td><td>

The Advanced Reference Qualifier for reference fields is not working

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1931422

</td><td>

Focus does not move to the first erroneous field once error comes up and all fields with an error are highlighted

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2022872

</td><td>

Workspace contact preview displays a logged-in user's country code in empty phone number fields

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1986098

</td><td>

Saving a record created from a related list can revert a previous saved update for a parent record

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1986450

</td><td>

The 'Presence' icon displays a **Review** button, but selecting it performs no action

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1987643

</td><td>

Warning messages are observed in logs: 'Encountered undeclared output variable: status'

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1988524

</td><td>

The copy/paste functionality is not working in the 'Email' section of the workspace.

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2032655

</td><td>

After upgrade to Australia, custom form annotation type style doesn't render correctly

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1849250

</td><td>

Screen reader announcements for read-only and mandatory active fields are unnecessarily long

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1958867

</td><td>

Approving the approval record from the Change Request is not refreshing the state of the change record in Service Operations Workspace \(SOW\)

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2062289

</td><td>

In Australia, when checking the condition/criteria for the attached file's name, the 'Attachment' UI box is loads forever

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2013101

</td><td>

The 'Attachment' tab item on the side panel doesn't filter the attachments based on the query business rule

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2017669

</td><td>

Mandatory fields are prematurely highlighted in red when creating a new incident in SOW Workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2019097

</td><td>

XMLParser instances retain excessive amounts of heap space

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2020159

</td><td>

The focus on the workspace form goes to the 'Save' UI action after the notification message is cleared from the form

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2027393

</td><td>

Previewing a Workflow Data Fabric \(WDF\) record on a Glide table form view displays nothing

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2027597

</td><td>

When creating a template on a record, the fields that have the same column name don't have any identifiers to distinguish in workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2068691

</td><td>

It navigates to a new form when adding an email on a watchlist

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1728612

</td><td>

There's no confirmation message provided to users who update a form field

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1894863

</td><td>

Inconsistent behavior occurs when changing the 'Date/time' field in the workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1933190

</td><td>

The Change request form scrolls up and down, with the header expanding and contracting, on the key press within a multi-line string field within the CAB Workbench

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1948838

</td><td>

The multi-lingual user search and tagging for Kanji, Romaji, Hangul, and Pinyin

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1954804

</td><td>

The translated text-type fields aren't displaying the '\(Encrypted\)' label for encrypted fields in a workspace

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1981726

</td><td>

There's a styling issue with the accordion header overlapping with the 'Form' section

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1999708

</td><td>

In Service Operation Workspace, the string 'Sort by' in the modified templates panel is hardcoded

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2000610

</td><td>

The 'Edit' form in Service Operations Workspace isn't displaying a message when the field is mandatory

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2001319

</td><td>

The group edit in Compliance Workspace and Controls List displays an error due to logic modifying respondents

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB1915534

</td><td>

Dictionary files need to be updated to reflect the sys\_metadata extension

</td></tr><tr><td>

UI Form Administration

</td><td>

PRB2025980

</td><td>

A reference list displays an error if the user opens it without access

</td></tr><tr><td>

UI Policies

</td><td>

PRB2028073

</td><td>

The UI policy for turning off a filter condition doesn't work when selecting reference fields

</td></tr><tr><td>

Universal Request

</td><td>

PRB1988790

</td><td>

When glide.ui.security. allow\_codetag is set to false, comments are copied over wrapped in HTML and aren't displaying correctly

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB2025624

</td><td>

sys\_script\_fix\_12641201206d45e1867a434635e93997 skip record is created

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB2022878

</td><td>

Glide list field type export and import does not account for tables that use non-sys\_id coalescing strategies

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1960119

</td><td>

Execution tracker issues for plugins during Zurich upgrades

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1965821

</td><td>

Upgrade syslog error messages should be warnings: 'Could not load the Out Of Band App'

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB2039540

</td><td>

The 'Upgrade complete' notification does not retry

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB2050680

</td><td>

Store certification failure for the newly added field 'merge\_base\_payload\_hash'

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1843409

</td><td>

Records with skipped error disposition are part of the com.sn\_shell\_parts plugin

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1958321

</td><td>

Ensure schema changes occur before parallel plugin upgrades when Parallel Plugin Loading \(PPL\) is turned on

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1968094

</td><td>

A static reference to a scriptable object in MetadataCustomizationStateAPI

</td></tr><tr><td>

Upgrade Center

</td><td>

PRB1998674

</td><td>

There's an error when attempting a 'Save Merge': '\#Could not save record because of a compile error: JavaScript parse error at line \(432\) column \(7\) problem = invalid property id'

</td></tr><tr><td>

Upgrade Monitor

</td><td>

PRB1982307

</td><td>

There's an Upgrade Monitor message displayed while the system is actively performing table alterations: 'Batch altering table: waiting for exclusive lock'

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB2021289

</td><td>

Long session durations are observed for few Usage Insights Sessions, causing inaccurate session duration metrics

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB2034497

</td><td>

There's errors in the system log/the error log observed UsageAnalytics App Persistor

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB2012658

</td><td>

Inactive records from the table usageanalytics\_count\_cfg are executed as part of UAComplianceEngineJob

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB2028292

</td><td>

Add System Property or User Preference to hide menu item without disabling telemetry collection

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB2059358

</td><td>

Warning messages are displayed in the console for unregistered applications

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1982016

</td><td>

Usage Analytics's 'Usage Status Download' causes a replication lag

</td></tr><tr><td>

Usage Analytics

</td><td>

PRB1999525

</td><td>

'Additional Metrics' displays a blank page

</td></tr><tr><td>

User Authentication

</td><td>

PRB2017890

</td><td>

'Works with ServiceNow' branding is visible with the base instance ServiceNow logo

</td></tr><tr><td>

User Authentication

</td><td>

PRB2055791

</td><td>

There's a CSS layout issue on the login page when French language is selected

</td></tr><tr><td>

User Authentication

</td><td>

PRB2003653

</td><td>

SAML certificate validation prematurely sets an error flag on the first certificate failure

</td></tr><tr><td>

User Authentication

</td><td>

PRB2010133

</td><td>

Password requirements on login\_cpw.do render as &lt;p&gt; tags instead of semantic list markup

</td></tr><tr><td>

User Criteria for Service Catalog

</td><td>

PRB1985455

</td><td>

Adding user criteria via Catalog Builder isn't working as expected

</td></tr><tr><td>

User Criteria for Service Portal

</td><td>

PRB1961376

</td><td>

Alumni users aren't able to view the base instance pages which pages need only the snc\_internal and snc\_external roles

</td></tr><tr><td>

UXF Components

</td><td>

PRB2017748

</td><td>

Semantic headings are improperly used and the heading hierarchy is incorrect

</td></tr><tr><td>

UXF Components

</td><td>

PRB1998062

</td><td>

A keyboard tab key is unresponsive when a new tab opens on selecting the **Open record** button in the modal

</td></tr><tr><td>

UXF Macroponent

</td><td>

PRB1899084

</td><td>

The technical dashboard override isn't applied when switching domains in UI Builder \(UIB\)

</td></tr><tr><td>

UX Framework

</td><td>

PRB2018044

</td><td>

If sys\_attachments is excluded during cloning, UXF pages aren't loading correctly after cloning

</td></tr><tr><td>

UX Framework

</td><td>

PRB1913831

</td><td>

Breadcrumb is breaking when refreshing the page

</td></tr><tr><td>

UX Framework

</td><td>

PRB2002772

</td><td>

Preset for the presentational list \(nested inside the record list bundle\) wasn't discovered during pre-population

</td></tr><tr><td>

UX Framework

</td><td>

PRB2005020

</td><td>

Aria-orientation='vertical' attribute isn't provided to tablist and the user can't navigate with both right/left and up/down arrow keys

</td></tr><tr><td>

UX Framework

</td><td>

PRB1996624

</td><td>

Add-on events aren't caught when a page is used as a subpage

</td></tr><tr><td>

UX Framework

</td><td>

PRB2021488

</td><td>

Selected buttons do not have sufficient color contrast with adjacent buttons

</td></tr><tr><td>

UX Framework

</td><td>

PRB2018504

</td><td>

For workspace tabs, the selected tab has insufficient color contrast against adjacent colors

</td></tr><tr><td>

UX Framework

</td><td>

PRB1963187

</td><td>

Keyboard focus is lost on tabbing from 'More Options \(...\)'

</td></tr><tr><td>

UX Framework

</td><td>

PRB2020895

</td><td>

Cleanup viewports and now-trigger-library memory leaks

</td></tr><tr><td>

UX Framework

</td><td>

PRB1982045

</td><td>

Repeated invoking of sn-canvas-tabsdata reducer causes outdated data in tabsdata processing

</td></tr><tr><td>

UX Framework

</td><td>

PRB1969174

</td><td>

The aria-label for the 'Dot' icon doesn't have a proper name and ia defined as the 'Dirty' state in the Service Operations Workspace \(SOW\)

</td></tr><tr><td>

UX Framework

</td><td>

PRB2003269

</td><td>

The 'Wrap up' modal doesn't display when users close the 'Interaction' tab and they reopen/reload it again

</td></tr><tr><td>

UX Framework

</td><td>

PRB2033497

</td><td>

Next Experience app shell header remains dirty after form save when events dispatched via Controller

</td></tr><tr><td>

UX Framework

</td><td>

PRB2039110

</td><td>

Lazy-loading defaultNodeStyles retains detached ShadowRoots due to missing disconnect cleanup

</td></tr><tr><td>

UX Framework

</td><td>

PRB2011296

</td><td>

There's a null pointer exception in GlideUxComponentDefProvider when sys\_ux\_lib\_component has a null tag

</td></tr><tr><td>

UX Framework

</td><td>

PRB2016056

</td><td>

Focus doesn't set to the element inside the alert dialog which displayed an error

</td></tr><tr><td>

UX Framework

</td><td>

PRB2020299

</td><td>

An OpenFrame API race condition causes incorrect tab content rendering in Customer Service Management workspace

</td></tr><tr><td>

UX Framework

</td><td>

PRB2024860

</td><td>

getInstanceValue caches are undefined and portal app shell search navigation is broken

</td></tr><tr><td>

UX Framework

</td><td>

PRB2035397

</td><td>

After typing in an input field on record page load, the focus shifts intermittently

</td></tr><tr><td>

UX Framework

</td><td>

PRB2039203

</td><td>

\(UIB\) Browser title is showing as URL path instead of Label configured in side navigation when open page or switch side navigation

</td></tr><tr><td>

UX Framework

</td><td>

PRB2041370

</td><td>

Record list shows task table data even if list broker's table is null/ empty

</td></tr><tr><td>

UX Framework

</td><td>

PRB2055248

</td><td>

'Change Task' tab labels show the last character\(s\) as dimmed/faded

</td></tr><tr><td>

UX Framework

</td><td>

PRB2069094

</td><td>

Users are unable to select menu API calls on a SURF clone instance

</td></tr><tr><td>

UX Framework

</td><td>

PRB1798479

</td><td>

There's a misplaced closed dialog **X** button in an email body's full view

</td></tr><tr><td>

UX Framework

</td><td>

PRB1943950

</td><td>

The custom style breaks when enabling 'glide.ux.user\_criteria\_enabled'

</td></tr><tr><td>

UX Framework

</td><td>

PRB1958355

</td><td>

Insufficient color contrast for focus indicators of the options

</td></tr><tr><td>

UX Framework

</td><td>

PRB1979671

</td><td>

When an optional parameter is removed from the URL, 'MCP Prop Changed' isn't fired

</td></tr><tr><td>

UX Framework

</td><td>

PRB1990602

</td><td>

There's problems with UI Builder

</td></tr><tr><td>

UX Framework

</td><td>

PRB1993526

</td><td>

A tooltip isn't provided for the ServiceNow logo

</td></tr><tr><td>

UX Framework

</td><td>

PRB1995723

</td><td>

convertUrlToPayload generates an incorrect payload, causing routing issues to incident records

</td></tr><tr><td>

UX Framework

</td><td>

PRB1998648

</td><td>

URL field links don't work in a workspace reference preview

</td></tr><tr><td>

UX Framework

</td><td>

PRB2004013

</td><td>

Filters aren't appearing in the dashboard

</td></tr><tr><td>

UX Framework

</td><td>

PRB2004739

</td><td>

The link text overflows the card on the login page in some non-English languages

</td></tr><tr><td>

UX Framework

</td><td>

PRB2007769

</td><td>

Two asterisks are displayed for mandatory 'True/False' fields with hint/help text added and the 'Show help tips on Forms' preference enabled

</td></tr><tr><td>

Versatile Node and Cluster Configuration

</td><td>

PRB1918829

</td><td>

The api/run-node-script.sh doesn't honor overrides.d properties

</td></tr><tr><td>

Versatile Node and Cluster Configuration

</td><td>

PRB2002618

</td><td>

There's an AHA check failure due to a node\_id mismatch from capitalizing the host name

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1980327

</td><td>

A chat dynamic greeting isn't localized correctly

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2051861

</td><td>

NPE in ResponseGenerationProcessor.handleRegularResults when TextToResult returns null response

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2056495

</td><td>

Central cache doesn't return the correct entry if the cache is updated from a different cluster

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2033881

</td><td>

Executing a catalog item or a skill from searched results fails silently after canceling the live agent request

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2033038

</td><td>

When an agent is triggered from the planner2 flow with localization enabled, the skillId is missing in the iterationContext

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1993583

</td><td>

LLM calls time out after 60,000 milliseconds

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1968407

</td><td>

Chat window issue with IT Virtual Agent

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2035888

</td><td>

A Guardian-triggered async\_search early-return leaves a stale task ID in the context

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2033400

</td><td>

vaSystem.getTranscript\(\) returns empty when Dynamic Translation is turned on and messages are in the 'Pending' or 'Translating' status

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2058728

</td><td>

Chat summary isn't generated on instances with the Spanish translation plugin

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1985280

</td><td>

Duplicate attachment is displayed in Virtual Agent after portal refresh

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2034975

</td><td>

Interactions are throwing an error of 'technical issues' intermittently

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1974845

</td><td>

The FDIHServiceImpl object holds significant memory

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2024316

</td><td>

Stuck Virtual Agent conversations from FDIH async\_search race condition cause infinite retry loop consuming worker threads

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2019099

</td><td>

Starting '\{0\}' sys\_cs\_context\_profile\_message isn't translated per user session language

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2020252

</td><td>

The Virtual Agent goes into a loop after selecting the feedback survey

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2021983

</td><td>

Null GlideRecord in conversation context causes IllegalArgumentException during deserialization in TypedValueDeserializationUtil

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2022995

</td><td>

Referenced sources are missing from the chat transcript

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1940553

</td><td>

Unable to toggle the 'Show more' accordion in text responses outside of Virtual Agent topics

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2025952

</td><td>

The value of the of the 'shorten response' field on text nodes in VA Designer cannot be set globally or per topic

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2026682

</td><td>

Conversation history of language detection confirmation disrupts a user response

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1985767

</td><td>

There's no response from a live agent after a user request and an unexpected system message displays

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2003424

</td><td>

External users are unable to delete closed chats from the Virtual Agent chat history

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2003757

</td><td>

The 'Search' icon on a synthesized response in Virtual Agent redirects to an old search page

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1916016

</td><td>

The End Conversation action does not end live agent interaction when the Post Chat survey is enabled

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1992132

</td><td>

The Virtual Agent \(VA\) link menu items are not displayed correctly

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2052769

</td><td>

There's a 'sorry' message after a user tries to enter a different topic after a survey message

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2013952

</td><td>

Remove the deprecate system property 'com.glide.cs.conversation.entity.cache.enabled'

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1929534

</td><td>

The Virtual Agent line break \(\\n\) is not working in the header card in a 'Static Choice' or 'Dynamic Choice' control

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2010886

</td><td>

A session expires in the middle of a conversion with the agent

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2024076

</td><td>

Pickers aren't honoring pre-selected options

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2028065

</td><td>

Timestamps sent from Amazon Connect to Virtual Agent's server leave messages out of order

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2029216

</td><td>

Channels's typing indicator breaks AIA execution

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2029289

</td><td>

The format for the variable type 'List Collector' and 'Reference' isn't displaying the same as on the portal in NAVA

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2031583

</td><td>

Non-topic skills are dropped from the skill picker when all applicable topic skills have a visible design category

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2031991

</td><td>

'Get details of problem agent' returns additional duplicate closure messages along with the expected closing message

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2033259

</td><td>

Language detection doesn't work properly with Agentic mode for both the standard and enhanced chat

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2033480

</td><td>

Virtual Agent stores some translations in sys\_ui\_message Key with a 'va:topic:' prefix and sys\_cb\_topic sys\_id, and doesn't translate the newly added text

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2033680

</td><td>

REST inbound message removes the character value within certain symbols

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2037636

</td><td>

Agent messages containing URLs aren't displaying correctly in the internal transcript

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2055748

</td><td>

In Virtual Agent Web Client, the 'Contact Support' menu icon disappears when an option is selected because the icon color and background both bind to search\_icon\_color

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2057596

</td><td>

Rename 'Now Assist Virtual Agent' to Otto for topics in Glide

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2057885

</td><td>

Feedback icons not showing in AI Agent chat messages

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2064355

</td><td>

Auto Chat executions are faulted

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2064833

</td><td>

A domain is set to null after user input

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2069447

</td><td>

Semantic filtering Virtual Agent global flags aren't set when invoked from AO via topic tool execution

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2072565

</td><td>

When a user starts a conversation with 'end' or 'bye' as the first query and later pivots to the actual query after presented the feedback message, the new intent never is captured and Virtual Agent keeps asking for feedback

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2073250

</td><td>

A conversation from another domain doesn't work if the user default domain doesn't have access to the current session domain

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2074992

</td><td>

Handshake fails when duplicate preferred-skill entries exist for the same skill

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2076609

</td><td>

The 'Timeout conversations' job fails to close conversations on cross domains

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1943976

</td><td>

Need to add expensive caches as hard reference caches to avoid GC

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1943977

</td><td>

The Virtual Agent chat bot input box border is cut

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1959245

</td><td>

Fluency Judge penalizes fluency for the word 'False' in the synthesized response

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1959445

</td><td>

Now Assist Panel shows 'Unable to load'

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1959782

</td><td>

Live agent support fails in the Now Mobile app when callback is enabled

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1960339

</td><td>

The 'Use an AI agent ' action moves to a 'Waiting' state when called inside a flow-logic component

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1968120

</td><td>

Dynamic Translation \(DT\) does not work in Now Assist from mobile devices

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1972520

</td><td>

Behavior for time stamps on interaction.transcript dialog lines can cause confusion

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1976905

</td><td>

'Error parsing additional context JSONObject\[''conversation''\] not found' issue for NLU Conversations

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1977219

</td><td>

The max wait time/no agent message isn't rendering hyperlinks in Portal, but it's working in Teams

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1983377

</td><td>

In enhanced chat, the virtual\_agent flag is always set to false

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1985773

</td><td>

Now Assist Virtual Agent \(NAVA\) doesn't trigger the onboarding workflow

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1990020

</td><td>

The **Show more** button appears during streaming even when it's disabled

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1990700

</td><td>

Clean up sys\_ui\_message for translation/update translation for contextual actions

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1992051

</td><td>

There's emoji panel UI issues in the chat bot

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1992368

</td><td>

A fallback message script seems broken with unterminated comment and incomplete code in LANGUAGE\_SWITCH\_CONTROL

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB1999511

</td><td>

Message preview and unread badge count don't work upon page refresh

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2001624

</td><td>

It should handle a hand-off scenario for 'view more record'

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2003421

</td><td>

When localization is enabled and the agent is triggered in a non-English language through Now Assist VIrtual Agent \(NAVA\) or Now Assist panel \(NAP\), the agent fails to execute

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2006208

</td><td>

The Virtual Agent avatar is displayed as a square, but it was round prior to the upgrade to Zurich

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2014396

</td><td>

AO results don't distinguish order guides from regular catalog items and sends sc\_cat\_item instead of sc\_cat\_item\_guide

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2077222

</td><td>

An issue in the fallback logic for a re-witten query in SearchAndRerankProcessor

</td></tr><tr><td>

Virtual Agent

</td><td>

PRB2024715

</td><td>

Async tool executions are stuck in processing

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB2012951

</td><td>

Parsing error appears when the value from the text input node is used to trigger NLU topic discovery with dialog acts on

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB2031236

</td><td>

AI Connector utility AI Agent drop-down list is empty due to improper URL encoding triggering connectSupportRouting processor

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1752802

</td><td>

The virtual agent designer page isn't accessible on Safari

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1949441

</td><td>

'Closing Message' is displayed when testing the assistant enabled with Enhanced Chat in the VA Designer Conversational Studio

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1949979

</td><td>

Unable to pass inputs to AI Agent in Virtual Agent topic using AI Connector utility

</td></tr><tr><td>

Virtual Agent Designer Legacy

</td><td>

PRB1992505

</td><td>

HTML rendring issues in alert analysis

</td></tr><tr><td>

Virtual Agent for Service Catalog

</td><td>

PRB1979804

</td><td>

Text is truncated when filling a catalog request on a request catalog item inline-seismic component

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1983355

</td><td>

Markdown to HTML parsing issues when there are special characters in the payload

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1961626

</td><td>

The record producer form opens behind an expanded chat window

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1997398

</td><td>

The now-chat-window library build is missing the rem multiplier, which causes tiny text in the ENHANCED\_CHAT fullscreen portal

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1982379

</td><td>

Massive /api/now/v1/cs/consumerAccount/\{sys\_id\}/sync calls after a user is logged out but has the Virtual Agent standalone page '$sn-va-web-client-app' open

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1825407

</td><td>

Unable to change ServiceNow VA message for com.glide.cs.general.multi\_file\_size\_exceed\_msg

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2030775

</td><td>

Topic Picker fails to dismiss when rendered immediately after the user response due to mismatched message\_type \(text instead of topic\_picker\)

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2031585

</td><td>

Synthesized response markdown to HTML render inserts spurious break elements for blank lines and inconsistently splits/merges block boundaries

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2004802

</td><td>

Now Assist is incorrectly displaying HTML when trying to display table data from KBs

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1974628

</td><td>

In Enhanced Chat, a theme hasn't been applied to support pop-up models

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1993741

</td><td>

When live\_agent\_only is set to true, the agent chat triggers the greetings topic instead of going to the live agent

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1976753

</td><td>

Messages sent in the new chat are some times getting merged with messages in the previous chat

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2014164

</td><td>

Additional columns in a reference variable aren't rendered correctly in Now Assist in Virtual Agent

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2021136

</td><td>

Selecting the **Stop** button during synthesized results streaming causes an error

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2030565

</td><td>

When selecting a link type menu item in Now Assist in Virtual Agent Enhanced Chat, it does not open a link in a new tab

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2031682

</td><td>

Web Client doesn't display it correctly if a synthesized response markdown contains a URL that has a parenthesis

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2032099

</td><td>

New chat contains messages from the old chat

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2034934

</td><td>

The 'Chat list' panel displays multiple tabs' conversations stacked together when switching tabs

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2055245

</td><td>

Detected Language Translation isn't applied to the expected wait time message during the Virtual Agent to Live Agent handoff

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2058202

</td><td>

In NAVA for the proactive trigger, the TAB Focus is falling on the invisible 'You have a chat recommendation. Tab to view the message'

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2070841

</td><td>

Missing branding font configuration produces url\(undefined\) in generated CSS, causing browser requests to /undefined

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1850499

</td><td>

Mobile needs to support the device trust token when running web Virtual Agent

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1899714

</td><td>

The Virtual Agent's IAR steals the focus and captures user input while minimized for Safari browsers

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1934241

</td><td>

The 'Estimated Wait Time' cannot be hidden in Virtual Agent when using Enhanced Chat

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1946823

</td><td>

The luminosity contrast ratio of the link text in Now Assist panel is less than required, and is 4.5:1

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1972526

</td><td>

The **Now Assist chat** button lacks a descriptive accessible label

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1974428

</td><td>

A response with multiple sources displays the same citation numbers/misplaced citation

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1990148

</td><td>

The Virtual Agent branding menu icon's color isn't working for the 'plus' icon to start a conversation

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB1998643

</td><td>

While requesting a catalog item in Now Assist Virtual Agent \(NAVA\), selecting the **Skip** button for a date/time question does not clear the date/time value in the **Input** field

</td></tr><tr><td>

Virtual Agent Web Client

</td><td>

PRB2008383

</td><td>

The 'Audio notifications' toggle for Web Client affects Now Assist Portal with no way to turn them off

</td></tr><tr><td>

Visibility Content

</td><td>

PRB2003240

</td><td>

Cloud discovery is spending 40% runtime on the query hash 164915272

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB2059581

</td><td>

Users are unable to move a card from one visual task board \(VTB\) to another after an Australia upgrade

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB2036858

</td><td>

'Copy journal content' does not function on the activity stream, within VTB cards

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB1991131

</td><td>

Elevated roles are removed when accessing a virtual task board

</td></tr><tr><td>

Visual Task Boards

</td><td>

PRB2001739

</td><td>

In a visual task board, the **Close** button on a modal has an incorrect aria label

</td></tr><tr><td>

VMware Discovery

</td><td>

PRB2009124

</td><td>

ESX OS Software Install Records \(display\_name hardcoded and last\_scanned\) aren't updating, and stale version records aren't deactivated on Discovery

</td></tr><tr><td>

VMware Discovery

</td><td>

PRB1678256

</td><td>

VMware Discovery doesn't remove relations from Server CI records once the server is moved to a new VM \(Virtual Machine\) instance

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1997626

</td><td>

An error message appears across various catalog items when they are opened

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB2006201

</td><td>

Database response time takes longer becuase of an influx of /api/sn\_walkup/walk\_up/queue/ transactions

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB2030122

</td><td>

WalkUp queue shows the incorrect date for Banglore location check-in queue window

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1803713

</td><td>

'To' as a sys\_ui\_message key needs to be disambiguated for target languages, such as Ja

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB1981055

</td><td>

Image on the 'Walk up reservation' page does not display for users without a walk up role

</td></tr><tr><td>

Walk-Up Experience

</td><td>

PRB2000279

</td><td>

The 'My Walkup' inbox redirects to the Agent Workspace inbox instead of the Service Operations Workspace inbox

</td></tr><tr><td>

Walk-up Experience Portal

</td><td>

PRB1986566

</td><td>

There's an issue with walk-up check-in date translations

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) 2.0 AA Compliance

</td><td>

PRB2013386

</td><td>

On the Idea Portal, the description text for an idea record overflows its description container instead of staying within the expected boundaries

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB2019324

</td><td>

List view tables in Next Experience workspaces don't preserve cell/row borders in Windows' high contrast \(forced-colors\) mode

</td></tr><tr><td>

Web Content Accessibility Guidelines \(WCAG\) Conformance

</td><td>

PRB2051806

</td><td>

The backend start page menu and global search controls are clipped at 400% zoom

</td></tr><tr><td>

Window Manager

</td><td>

PRB2041392

</td><td>

There's a UI bug when opening the Now Assist panel

</td></tr><tr><td>

Window Manager

</td><td>

PRB1962518

</td><td>

The HTML code is shown in the preview of the minimized Modeless Compose Editor

</td></tr><tr><td>

Word Document APIs

</td><td>

PRB1973625

</td><td>

Support unzipped font size up to 20 MB in Word Doc API

</td></tr><tr><td>

Word Document APIs

</td><td>

PRB1987850

</td><td>

Issue with document sync when paragraph properties do not exist

</td></tr><tr><td>

Workflow Editor

</td><td>

PRB1956774

</td><td>

Workflow inputs of string \(Full UTF-8\) types are missing a value

</td></tr><tr><td>

Work Order Management

</td><td>

PRB2011569

</td><td>

Scheduling method is empty

</td></tr><tr><td>

Work Order Management

</td><td>

PRB2017308

</td><td>

Flat table records aren't invalidated when location attributes are inserted to Workforce Operations \(WFO\) events

</td></tr><tr><td>

Work Order Management

</td><td>

PRB2027073

</td><td>

Unable to give read access for sm\_template form when Work Order Template is without any associated tasks

</td></tr><tr><td>

Work Order Management

</td><td>

PRB2031481

</td><td>

When the Schedule Start Date is updated from the List view, the record throws errors on the Work Order Task form

</td></tr><tr><td>

Work Order Management

</td><td>

PRB2035553

</td><td>

The system does not automatically release parts from closed WOTs, preventing status change to 'Available' and blocking further utilization

</td></tr><tr><td>

Work Order Management

</td><td>

PRB2064250

</td><td>

The 'Estimated End' field displays an incorrect datetime in Service Operations Workspace when 'Estimated Work Duration' is updated

</td></tr><tr><td>

Work Order Management

</td><td>

PRB1988499

</td><td>

The 'AutoAssign' UI action on a work order task form for fynamic fails with a message: 'Something went wrong. Please Rerun'

</td></tr><tr><td>

Work Order Management

</td><td>

PRB2003061

</td><td>

On Field Service Management \(FSM\) Mobile Agent, 'Accept' on an agent-to-agent part request fails with a 'Failed!' error

</td></tr><tr><td>

Work Order Management

</td><td>

PRB2005279

</td><td>

The **Copy Task Template** button within a Work Order Template doesn't populate the **Work Type** field

</td></tr><tr><td>

Work Order Management

</td><td>

PRB2066296

</td><td>

wm\_agent and wm\_admin are unable to create a part requirement from a module

</td></tr><tr><td>

Workspace List Menu

</td><td>

PRB1985821

</td><td>

The floating point variable type values are rounded off to two digits after a decimal in a workspace

</td></tr><tr><td>

Workspace List Menu

</td><td>

PRB1995101

</td><td>

The tooltip for the slider to control a workspace column's width doesn't contain sufficient information for a keyboard user

</td></tr><tr><td>

Zero Trust Access

</td><td>

PRB1974949

</td><td>

The property glide.authenticate.session\_access.user\_info\_message doesn't support translation

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1996302

</td><td>

Installed applications aren't shown in application manager when the instance is upgraded to Australia

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB1982399

</td><td>

The Choice field is not indexed if there is no language configured for Zing

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB2018016

</td><td>

The 'TS Index Stats' job shouldn't check a table that's not indexed

</td></tr><tr><td>

Zing Text Indexing and Search Engine

</td><td>

PRB2008761

</td><td>

Unable to disable exact match

</td></tr></tbody>
</table>**Parent Topic:**[Available patches and hotfixes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/available-versions.md)

